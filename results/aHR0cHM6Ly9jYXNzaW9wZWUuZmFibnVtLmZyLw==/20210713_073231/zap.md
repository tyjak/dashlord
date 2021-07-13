
# ZAP Scanning Report

Generated on Tue, 13 Jul 2021 07:26:08


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 5 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| Source Code Disclosure - Java | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 2 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 3 | 
| Permissions Policy Header Not Set | Low | 6 | 
| Strict-Transport-Security Header Not Set | Low | 9 | 
| X-Content-Type-Options Header Missing | Low | 8 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 3 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 7 | 
| Storable but Non-Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class w{constructor(e,t){this.ctx=e,this.options=t,this._initState()}setUniversal(e,t){return h(t)?this.removeUniversal(e):(this.setCookie(e,t),this.setLocalStorage(e,t),this.setState(e,t),t)}getUniversal(e){let t;return h(t)&&(t=this.getCookie(e)),h(t)&&(t=this.getLocalStorage(e)),h(t)&&(t=this.getState(e)),t}syncUniversal(e,t){let c=this.getUniversal(e);return h(c)&&d(t)&&(c=t),d(c)&&this.setUniversal(e,c),c}removeUniversal(e){this.removeState(e),this.removeLocalStorage(e),this.removeCookie(e)}_initState(){if(r.set(this,"_state",{}),this._useVuex=this.options.vuex&&!!this.ctx.store,this._useVuex){const e={namespaced:!0,state:()=>this.options.initialState,mutations:{SET(e,t){r.set(e,t.key,t.value)}}};this.ctx.store.registerModule(this.options.vuex.namespace,e,{preserveState:Boolean(this.ctx.store.state[this.options.vuex.namespace])}),this.state=this.ctx.store.state[this.options.vuex.namespace]}else r.set(this,"state",{}),console.warn("[AUTH] The Vuex Store is not activated. This might cause issues in auth module behavior, like redirects not working properly.To activate it, see https://nuxtjs.org/docs/2.x/directory-structure/store")}setState(e,t){return"_"===e[0]?r.set(this._state,e,t):this._useVuex?this.ctx.store.commit(this.options.vuex.namespace+"/SET",{key:e,value:t}):r.set(this.state,e,t),t}getState(e){return"_"!==e[0]?this.state[e]:this._state[e]}watchState(e,t){if(this._useVuex)return this.ctx.store.watch((t=>x(t[this.options.vuex.namespace],e)),t)}removeState(e){this.setState(e,void 0)}setLocalStorage(e,t){if(h(t))return this.removeLocalStorage(e);if("undefined"==typeof localStorage||!this.options.localStorage)return;const c=this.options.localStorage.prefix+e;try{localStorage.setItem(c,M(t))}catch(e){if(!this.options.ignoreExceptions)throw e}return t}getLocalStorage(e){if("undefined"==typeof localStorage||!this.options.localStorage)return;const t=this.options.localStorage.prefix+e;return C(localStorage.getItem(t))}removeLocalStorage(e){if("undefined"==typeof localStorage||!this.options.localStorage)return;const t=this.options.localStorage.prefix+e;localStorage.removeItem(t)}getCookies(){const e=document.cookie;return o.parse(e||"")||{}}setCookie(e,t,c={}){if(!this.options.cookie)return;const n=(void 0!==c.prefix?c.prefix:this.options.cookie.prefix)+e,r=Object.assign({},this.options.cookie.options,c),l=M(t);h(t)&&(r.maxAge=-1),"number"==typeof r.expires&&(r.expires=new Date(Date.now()+864e5*r.expires));const f=o.serialize(n,l,r);return document.cookie=f,t}getCookie(e){if(!this.options.cookie)return;const t=this.options.cookie.prefix+e,c=this.getCookies();return C(c[t]?decodeURIComponent(c[t]):void 0)}removeCookie(e,t){this.setCookie(e,void 0,t)}}class H{constructor(e,t){this.strategies={},this._errorListeners=[],this._redirectListeners=[],this.ctx=e,this.options=t;const c=new w(e,{...t,initialState:{user:null,loggedIn:!1}});this.$storage=c,this.$state=c.state}get state(){return this._stateWarnShown||(this._stateWarnShown=!0,console.warn("[AUTH] $auth.state is deprecated. Please use $auth.$state or top level props like $auth.loggedIn")),this.$state}get strategy(){return this.getStrategy()}getStrategy(e=!0){if(e){if(!this.$state.strategy)throw new Error("No strategy is set!");if(!this.strategies[this.$state.strategy])throw new Error("Strategy not supported: "+this.$state.strategy)}return this.strategies[this.$state.strategy]}get user(){return this.$state.user}get loggedIn(){return this.$state.loggedIn}get busy(){return this.$storage.getState("busy")}async init(){if(this.options.resetOnError&&this.onError(((...e)=>{("function"!=typeof this.options.resetOnError||this.options.resetOnError(...e))&&this.reset()})),this.$storage.syncUniversal("strategy",this.options.defaultStrategy),!this.getStrategy(!1)&&(this.$storage.setUniversal("strategy",this.options.defaultStrategy),!this.getStrategy(!1)))return Promise.resolve();try{await this.mounted()}catch(e){this.callOnError(e)}finally{this.options.watchLoggedIn&&this.$storage.watchState("loggedIn",(e=>{z(this.ctx.route,"auth",!1)||this.redirect(e?"home":"logout")}))}}getState(e){return this._getStateWarnShown||(this._getStateWarnShown=!0,console.warn("[AUTH] $auth.getState is deprecated. Please use $auth.$storage.getState() or top level props like $auth.loggedIn")),this.$storage.getState(e)}registerStrategy(e,t){this.strategies[e]=t}setStrategy(e){if(e===this.$storage.getUniversal("strategy"))return Promise.resolve();if(!this.strategies[e])throw new Error(`Strategy ${e} is not defined!`);return this.reset(),this.$storage.setUniversal("strategy",e),this.mounted()}mounted(...e){return this.getStrategy().mounted?Promise.resolve(this.getStrategy().mounted(...e)).catch((e=>(this.callOnError(e,{method:"mounted"}),Promise.reject(e)))):this.fetchUserOnce()}loginWith(e,...t){return this.setStrategy(e).then((()=>this.login(...t)))}login(...e){return this.getStrategy().login?this.wrapLogin(this.getStrategy().login(...e)).catch((e=>(this.callOnError(e,{method:"login"}),Promise.reject(e)))):Promise.resolve()}fetchUser(...e){return this.getStrategy().fetchUser?Promise.resolve(this.getStrategy().fetchUser(...e)).catch((e=>(this.callOnError(e,{method:"fetchUser"}),Promise.reject(e)))):Promise.resolve()}logout(...e){return this.getStrategy().logout?Promise.resolve(this.getStrategy().logout(...e)).catch((e=>(this.callOnError(e,{method:"logout"}),Promise.reject(e)))):(this.reset(),Promise.resolve())}setUserToken(e,t){return this.getStrategy().setUserToken?Promise.resolve(this.getStrategy().setUserToken(e,t)).catch((e=>(this.callOnError(e,{method:"setUserToken"}),Promise.reject(e)))):(this.getStrategy().token.set(e),Promise.resolve())}reset(...e){return this.getStrategy().reset||(this.setUser(!1),this.getStrategy().token.reset(),this.getStrategy().refreshToken.reset()),this.getStrategy().reset(...e)}refreshTokens(){return this.getStrategy().refreshController?Promise.resolve(this.getStrategy().refreshController.handleRefresh()).catch((e=>(this.callOnError(e,{method:"refreshTokens"}),Promise.reject(e)))):Promise.resolve()}check(...e){return this.getStrategy().check?this.getStrategy().check(...e):{valid:!0}}fetchUserOnce(...e){return this.$state.user?Promise.resolve():this.fetchUser(...e)}setUser(e){this.$storage.setState("user",e);let t={valid:Boolean(e)};t.valid&&(t=this.check()),this.$storage.setState("loggedIn",t.valid)}request(e,t={}){const c="object"==typeof t?Object.assign({},t,e):e;if(""===c.baseURL&&(c.baseURL=n(this.ctx.req)),this.ctx.app.$axios)return this.ctx.app.$axios.request(c).catch((e=>(this.callOnError(e,{method:"request"}),Promise.reject(e))));console.error("[AUTH] add the @nuxtjs/axios module to nuxt.config file")}requestWith(e,t,c){const n=this.getStrategy().token.get(),r=Object.assign({},c,t),o=this.strategies[e].options.token.name||"Authorization";return r.headers||(r.headers={}),!r.headers[o]&&d(n)&&n&&"string"==typeof n&&(r.headers[o]=n),this.request(r)}wrapLogin(e){return this.$storage.setState("busy",!0),this.error=null,Promise.resolve(e).then((e=>(this.$storage.setState("busy",!1),e))).catch((e=>(this.$storage.setState("busy",!1),Promise.reject(e))))}onError(e){this._errorListeners.push(e)}callOnError(e,t={}){this.error=e;for(const c of this._errorListeners)c(e,t)}redirect(e,t=!1){if(!this.options.redirect)return;const c=this.options.fullPathRedirect?this.ctx.route.fullPath:this.ctx.route.path;let n=this.options.redirect[e];if(n){if(this.options.rewriteRedirects&&("login"===e&&v(c)&&!m(this.ctx,n,c)&&this.$storage.setUniversal("redirect",c),"home"===e)){const e=this.$storage.getUniversal("redirect");this.$storage.setUniversal("redirect",null),v(e)&&(n=e)}n=this.callOnRedirect(n,c)||n,m(this.ctx,n,c)||(t?(v(n)&&!n.includes(this.ctx.base)&&(n=y("/"+this.ctx.base+"/"+n)),window.location.replace(n)):this.ctx.redirect(n,this.ctx.query))}}onRedirect(e){this._redirectListeners.push(e)}callOnRedirect(e,t){for(const c of this._redirectListeners)e=c(e,t)||e;return e}hasScope(e){const t=this.$state.user&&x(this.$state.user,this.options.scopeKey);return!!t&&(Array.isArray(t)?t.includes(e):Boolean(x(t,e)))}}const S=async e=>{if(z(e.route,"auth",!1))return;if(!function(e,t=[]){return[].concat(...e.matched.map((function(e,c){return Object.keys(e.components).map((function(n){return t.push(c),e.components[n]}))})))}(e.route,[]).length)return;const{login:t,callback:c}=e.$auth.options.redirect,n=z(e.route,"auth","guest"),r=t=>y(e.route.path,e)===y(t,e);if(e.$auth.$state.loggedIn){const{tokenExpired:c,refreshTokenExpired:o,isRefreshable:l}=e.$auth.check(!0);if((!t||r(t)||n)&&e.$auth.redirect("home"),o)e.$auth.reset();else if(c)if(l)try{await e.$auth.refreshTokens()}catch(t){e.$auth.reset()}else e.$auth.reset()}else n||c&&r(c)||e.$auth.redirect("login")};class k extends Error{constructor(){super("Both token and refresh token have expired. Your request was aborted."),this.name="ExpiredAuthSessionError"}}class L{constructor(e){this.scheme=e,this._refreshPromise=null,this.$auth=e.$auth}handleRefresh(){return this._refreshPromise?this._refreshPromise:this._doRefresh()}_doRefresh(){return this._refreshPromise=new Promise(((e,t)=>{this.scheme.refreshTokens().then((t=>{this._refreshPromise=null,e(t)})).catch((e=>{this._refreshPromise=null,t(e)}))})),this._refreshPromise}}var N,A;(A=N||(N={})).UNKNOWN="UNKNOWN",A.VALID="VALID",A.EXPIRED="EXPIRED";class D{constructor(e,t){this._status=this._calculate(e,t)}unknown(){return N.UNKNOWN===this._status}valid(){return N.VALID===this._status}expired(){return N.EXPIRED===this._status}_calculate(e,t){const c=Date.now();try{if(!e||!t)return N.UNKNOWN}catch(e){return N.UNKNOWN}return c<(t-=500)?N.VALID:N.EXPIRED}}class O{constructor(e,t){this.scheme=e,this.$storage=t}get(){const e=this.scheme.options.refreshToken.prefix+this.scheme.name;return this.$storage.getUniversal(e)}set(e){const t=V(e,this.scheme.options.refreshToken.type);return this._setToken(t),this._updateExpiration(t),t}sync(){const e=this._syncToken();return this._syncExpiration(),e}reset(){this._setToken(!1),this._setExpiration(!1)}status(){return new D(this.get(),this._getExpiration())}_getExpiration(){const e=this.scheme.options.refreshToken.expirationPrefix+this.scheme.name;return this.$storage.getUniversal(e)}_setExpiration(e){const t=this.scheme.options.refreshToken.expirationPrefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncExpiration(){const e=this.scheme.options.refreshToken.expirationPrefix+this.scheme.name;return this.$storage.syncUniversal(e)}_updateExpiration(e){let t;const c=Date.now(),n=1e3*Number(this.scheme.options.refreshToken.maxAge),r=n?c+n:0;try{t=1e3*l(e+"").exp||r}catch(e){if(t=r,!e||"InvalidTokenError"!==e.name)throw e}return this._setExpiration(t||!1)}_setToken(e){const t=this.scheme.options.refreshToken.prefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncToken(){const e=this.scheme.options.refreshToken.prefix+this.scheme.name;return this.$storage.syncUniversal(e)}}class T{constructor(e,t){this.scheme=e,this.axios=t,this.interceptor=null}setHeader(e){this.scheme.options.token.global&&this.axios.setHeader(this.scheme.options.token.name,e)}clearHeader(){this.scheme.options.token.global&&this.axios.setHeader(this.scheme.options.token.name,!1)}initializeRequestInterceptor(e){this.interceptor=this.axios.interceptors.request.use((async t=>{if(!this._needToken(t)||t.url===e)return t;const{valid:c,tokenExpired:n,refreshTokenExpired:r,isRefreshable:o}=this.scheme.check(!0);let l=c;if(r)throw this.scheme.reset(),new k;if(n){if(!o)throw this.scheme.reset(),new k;l=await this.scheme.refreshTokens().then((()=>!0)).catch((()=>{throw this.scheme.reset(),new k}))}const f=this.scheme.token.get();if(!l){if(!f&&this._requestHasAuthorizationHeader(t))throw new k;return t}return this._getUpdatedRequestConfig(t,f)}))}reset(){this.axios.interceptors.request.eject(this.interceptor),this.interceptor=null}_needToken(e){const t=this.scheme.options;return t.token.global||Object.values(t.endpoints).some((t=>"object"==typeof t?t.url===e.url:t===e.url))}_getUpdatedRequestConfig(e,t){return"string"==typeof t&&(e.headers[this.scheme.options.token.name]=t),e}_requestHasAuthorizationHeader(e){return!!e.headers.common[this.scheme.options.token.name]}}class _{constructor(e,t){this.scheme=e,this.$storage=t}get(){const e=this.scheme.options.token.prefix+this.scheme.name;return this.$storage.getUniversal(e)}set(e){const t=V(e,this.scheme.options.token.type);return this._setToken(t),this._updateExpiration(t),"string"==typeof t&&this.scheme.requestHandler.setHeader(t),t}sync(){const e=this._syncToken();return this._syncExpiration(),"string"==typeof e&&this.scheme.requestHandler.setHeader(e),e}reset(){this.scheme.requestHandler.clearHeader(),this._setToken(!1),this._setExpiration(!1)}status(){return new D(this.get(),this._getExpiration())}_getExpiration(){const e=this.scheme.options.token.expirationPrefix+this.scheme.name;return this.$storage.getUniversal(e)}_setExpiration(e){const t=this.scheme.options.token.expirationPrefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncExpiration(){const e=this.scheme.options.token.expirationPrefix+this.scheme.name;return this.$storage.syncUniversal(e)}_updateExpiration(e){let t;const c=Date.now(),n=1e3*Number(this.scheme.options.token.maxAge),r=n?c+n:0;try{t=1e3*l(e+"").exp||r}catch(e){if(t=r,!e||"InvalidTokenError"!==e.name)throw e}return this._setExpiration(t||!1)}_setToken(e){const t=this.scheme.options.token.prefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncToken(){const e=this.scheme.options.token.prefix+this.scheme.name;return this.$storage.syncUniversal(e)}}class P{constructor(e,...t){this.$auth=e,this.options=t.reduce(((p,e)=>f(p,e)),{})}get name(){return this.options.name}}const j={name:"local",endpoints:{login:{url:"/api/auth/login",method:"post"},logout:{url:"/api/auth/logout",method:"post"},user:{url:"/api/auth/user",method:"get"}},token:{property:"token",type:"Bearer",name:"Authorization",maxAge:1800,global:!0,required:!0,prefix:"_token.",expirationPrefix:"_token_expiration."},user:{property:"user",autoFetch:!0},clientId:!1,grantType:!1,scope:!1};class F extends P{constructor(e,t,...c){super(e,t,...c,j),this.token=new _(this,this.$auth.$storage),this.requestHandler=new T(this,this.$auth.ctx.$axios)}check(e=!1){const t={valid:!1,tokenExpired:!1};if(!this.token.sync())return t;if(!e)return t.valid=!0,t;return this.token.status().expired()?(t.tokenExpired=!0,t):(t.valid=!0,t)}mounted({tokenCallback:e=(()=>this.$auth.reset()),refreshTokenCallback:t}={}){const{tokenExpired:c,refreshTokenExpired:n}=this.check(!0);return n&&"function"==typeof t?t():c&&"function"==typeof e&&e(),this.initializeRequestInterceptor(),this.$auth.fetchUserOnce()}async login(e,{reset:t=!0}={}){if(!this.options.endpoints.login)return;t&&this.$auth.reset({resetInterceptor:!1}),this.options.clientId&&(e.data.client_id=this.options.clientId),this.options.grantType&&(e.data.grant_type=this.options.grantType),this.options.scope&&(e.data.scope=this.options.scope);const c=await this.$auth.request(e,this.options.endpoints.login);return this.updateTokens(c),this.requestHandler.interceptor||this.initializeRequestInterceptor(),this.options.user.autoFetch&&await this.fetchUser(),c}setUserToken(e){return this.token.set(e),this.fetchUser()}fetchUser(e){return this.check().valid?this.options.endpoints.user?this.$auth.requestWith(this.name,e,this.options.endpoints.user).then((e=>{const t=x(e.data,this.options.user.property);if(!t){const e=new Error(`User Data response does not contain field ${this.options.user.property}`);return Promise.reject(e)}return this.$auth.setUser(t),e})).catch((e=>(this.$auth.callOnError(e,{method:"fetchUser"}),Promise.reject(e)))):(this.$auth.setUser({}),Promise.resolve()):Promise.resolve()}async logout(e={}){return this.options.endpoints.logout&&await this.$auth.requestWith(this.name,e,this.options.endpoints.logout).catch((()=>{})),this.$auth.reset()}reset({resetInterceptor:e=!0}={}){this.$auth.setUser(!1),this.token.reset(),e&&this.requestHandler.reset()}updateTokens(e){const t=!this.options.token.required||x(e.data,this.options.token.property);this.token.set(t)}initializeRequestInterceptor(){this.requestHandler.initializeRequestInterceptor()}}const I={name:"refresh",endpoints:{refresh:{url:"/api/auth/refresh",method:"post"}},refreshToken:{property:"refresh_token",data:"refresh_token",maxAge:2592e3,required:!0,tokenRequired:!1,prefix:"_refresh_token.",expirationPrefix:"_refresh_token_expiration."},autoLogout:!1};class E extends F{constructor(e,t){super(e,t,I),this.refreshToken=new O(this,this.$auth.$storage),this.refreshController=new L(this)}check(e=!1){const t={valid:!1,tokenExpired:!1,refreshTokenExpired:!1,isRefreshable:!0},c=this.token.sync(),n=this.refreshToken.sync();if(!c||!n)return t;if(!e)return t.valid=!0,t;const r=this.token.status();return this.refreshToken.status().expired()?(t.refreshTokenExpired=!0,t):r.expired()?(t.tokenExpired=!0,t):(t.valid=!0,t)}mounted(){return super.mounted({tokenCallback:()=>{this.options.autoLogout&&this.$auth.reset()},refreshTokenCallback:()=>{this.$auth.reset()}})}refreshTokens(){if(!this.options.endpoints.refresh)return Promise.resolve();if(!this.check().valid)return Promise.resolve();if(this.refreshToken.status().expired())throw this.$auth.reset(),new k;this.options.refreshToken.tokenRequired||this.requestHandler.clearHeader();const e={data:{client_id:void 0,grant_type:void 0}};return this.options.refreshToken.required&&this.options.refreshToken.data&&(e.data[this.options.refreshToken.data]=this.refreshToken.get()),this.options.clientId&&(e.data.client_id=this.options.clientId),this.options.grantType&&(e.data.grant_type="refresh_token"),function(e){for(const t in e)void 0===e[t]&&delete e[t]}(e.data),this.$auth.request(e,this.options.endpoints.refresh).then((e=>(this.updateTokens(e,{isRefreshing:!0}),e))).catch((e=>(this.$auth.callOnError(e,{method:"refreshToken"}),Promise.reject(e))))}setUserToken(e,t){return this.token.set(e),t&&this.refreshToken.set(t),this.fetchUser()}reset({resetInterceptor:e=!0}={}){this.$auth.setUser(!1),this.token.reset(),this.refreshToken.reset(),e&&this.requestHandler.reset()}updateTokens(e,{isRefreshing:t=!1,updateOnRefresh:c=!0}={}){const n=!this.options.token.required||x(e.data,this.options.token.property),r=!this.options.refreshToken.required||x(e.data,this.options.refreshToken.property);this.token.set(n),r&&(!t||t&&c)&&this.refreshToken.set(r)}initializeRequestInterceptor(){this.requestHandler.initializeRequestInterceptor(this.options.endpoints.refresh.url)}}},81:function(e,t,c){"use strict";var n={name:"NoSsr",functional:!0,props:{placeholder:String,placeholderTag:{type:String,default:"div"}},render:function(e,t){var c=t.parent,n=t.slots,r=t.props,o=n(),l=o.default;void 0===l&&(l=[]);var f=o.placeholder;return c._isMounted?l:(c.$once("hook:mounted",(function(){c.$forceUpdate()})),r.placeholderTag&&(r.placeholder||f)?e(r.placeholderTag,{class:["no-ssr-placeholder"]},r.placeholder||f):l.length>0?l.map((function(){return e(!1)})):e(!1))}};e.exports=n},9:function(e,t,c){"use strict";c.d(t,"a",(function(){return o}));var n=c(2),r=c(1),o={props:{size:String,expanded:Boolean,loading:Boolean,rounded:Boolean,icon:String,iconPack:String,autocomplete:String,maxlength:[Number,String],useHtml5Validation:{type:Boolean,default:function(){return r.c.defaultUseHtml5Validation}},validationMessage:String,locale:{type:[String,Array],default:function(){return r.c.defaultLocale}},statusIcon:{type:Boolean,default:function(){return r.c.defaultStatusIcon}}},data:function(){return{isValid:!0,isFocused:!1,newIconPack:this.iconPack||r.c.defaultIconPack}},computed:{parentField:function(){for(var e=this.$parent,i=0;i<3;i++)e&&!e.$data._isField&&(e=e.$parent);return e},statusType:function(){var e=(this.parentField||{}).newType;if(e){if("string"==typeof e)return e;for(var t in e)if(e[t])return t}},statusMessage:function(){if(this.parentField)return this.parentField.newMessage||this.parentField.$slots.message},iconSize:function(){switch(this.size){case"is-small":return this.size;case"is-medium":return;case"is-large":return"mdi"===this.newIconPack?"is-medium":""}}},methods:{focus:function(){var e=this.getElement();void 0!==e&&this.$nextTick((function(){e&&e.focus()}))},onBlur:function(e){this.isFocused=!1,this.$emit("blur",e),this.checkHtml5Validity()},onFocus:function(e){this.isFocused=!0,this.$emit("focus",e)},getElement:function(){for(var e=this.$refs[this.$data._elementRef];Object(n.l)(e);)e=e.$refs[e.$data._elementRef];return e},setInvalid:function(){var e=this.validationMessage||this.getElement().validationMessage;this.setValidity("is-danger",e)},setValidity:function(e,t){var c=this;this.$nextTick((function(){c.parentField&&(c.parentField.type||(c.parentField.newType=e),c.parentField.message||(c.parentField.newMessage=t))}))},checkHtml5Validity:function(){if(this.useHtml5Validation){var e=this.getElement();if(void 0!==e)return e.checkValidity()?(this.setValidity(null,null),this.isValid=!0):(this.setInvalid(),this.isValid=!1),this.isValid}}}}}}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class w{constructor(e,t){this.ctx=e,this.options=t,this._initState()}setUniversal(e,t){return h(t)?this.removeUniversal(e):(this.setCookie(e,t),this.setLocalStorage(e,t),this.setState(e,t),t)}getUniversal(e){let t;return h(t)&&(t=this.getCookie(e)),h(t)&&(t=this.getLocalStorage(e)),h(t)&&(t=this.getState(e)),t}syncUniversal(e,t){let c=this.getUniversal(e);return h(c)&&d(t)&&(c=t),d(c)&&this.setUniversal(e,c),c}removeUniversal(e){this.removeState(e),this.removeLocalStorage(e),this.removeCookie(e)}_initState(){if(r.set(this,"_state",{}),this._useVuex=this.options.vuex&&!!this.ctx.store,this._useVuex){const e={namespaced:!0,state:()=>this.options.initialState,mutations:{SET(e,t){r.set(e,t.key,t.value)}}};this.ctx.store.registerModule(this.options.vuex.namespace,e,{preserveState:Boolean(this.ctx.store.state[this.options.vuex.namespace])}),this.state=this.ctx.store.state[this.options.vuex.namespace]}else r.set(this,"state",{}),console.warn("[AUTH] The Vuex Store is not activated. This might cause issues in auth module behavior, like redirects not working properly.To activate it, see https://nuxtjs.org/docs/2.x/directory-structure/store")}setState(e,t){return"_"===e[0]?r.set(this._state,e,t):this._useVuex?this.ctx.store.commit(this.options.vuex.namespace+"/SET",{key:e,value:t}):r.set(this.state,e,t),t}getState(e){return"_"!==e[0]?this.state[e]:this._state[e]}watchState(e,t){if(this._useVuex)return this.ctx.store.watch((t=>x(t[this.options.vuex.namespace],e)),t)}removeState(e){this.setState(e,void 0)}setLocalStorage(e,t){if(h(t))return this.removeLocalStorage(e);if("undefined"==typeof localStorage||!this.options.localStorage)return;const c=this.options.localStorage.prefix+e;try{localStorage.setItem(c,M(t))}catch(e){if(!this.options.ignoreExceptions)throw e}return t}getLocalStorage(e){if("undefined"==typeof localStorage||!this.options.localStorage)return;const t=this.options.localStorage.prefix+e;return C(localStorage.getItem(t))}removeLocalStorage(e){if("undefined"==typeof localStorage||!this.options.localStorage)return;const t=this.options.localStorage.prefix+e;localStorage.removeItem(t)}getCookies(){const e=document.cookie;return o.parse(e||"")||{}}setCookie(e,t,c={}){if(!this.options.cookie)return;const n=(void 0!==c.prefix?c.prefix:this.options.cookie.prefix)+e,r=Object.assign({},this.options.cookie.options,c),l=M(t);h(t)&&(r.maxAge=-1),"number"==typeof r.expires&&(r.expires=new Date(Date.now()+864e5*r.expires));const f=o.serialize(n,l,r);return document.cookie=f,t}getCookie(e){if(!this.options.cookie)return;const t=this.options.cookie.prefix+e,c=this.getCookies();return C(c[t]?decodeURIComponent(c[t]):void 0)}removeCookie(e,t){this.setCookie(e,void 0,t)}}class H{constructor(e,t){this.strategies={},this._errorListeners=[],this._redirectListeners=[],this.ctx=e,this.options=t;const c=new w(e,{...t,initialState:{user:null,loggedIn:!1}});this.$storage=c,this.$state=c.state}get state(){return this._stateWarnShown||(this._stateWarnShown=!0,console.warn("[AUTH] $auth.state is deprecated. Please use $auth.$state or top level props like $auth.loggedIn")),this.$state}get strategy(){return this.getStrategy()}getStrategy(e=!0){if(e){if(!this.$state.strategy)throw new Error("No strategy is set!");if(!this.strategies[this.$state.strategy])throw new Error("Strategy not supported: "+this.$state.strategy)}return this.strategies[this.$state.strategy]}get user(){return this.$state.user}get loggedIn(){return this.$state.loggedIn}get busy(){return this.$storage.getState("busy")}async init(){if(this.options.resetOnError&&this.onError(((...e)=>{("function"!=typeof this.options.resetOnError||this.options.resetOnError(...e))&&this.reset()})),this.$storage.syncUniversal("strategy",this.options.defaultStrategy),!this.getStrategy(!1)&&(this.$storage.setUniversal("strategy",this.options.defaultStrategy),!this.getStrategy(!1)))return Promise.resolve();try{await this.mounted()}catch(e){this.callOnError(e)}finally{this.options.watchLoggedIn&&this.$storage.watchState("loggedIn",(e=>{z(this.ctx.route,"auth",!1)||this.redirect(e?"home":"logout")}))}}getState(e){return this._getStateWarnShown||(this._getStateWarnShown=!0,console.warn("[AUTH] $auth.getState is deprecated. Please use $auth.$storage.getState() or top level props like $auth.loggedIn")),this.$storage.getState(e)}registerStrategy(e,t){this.strategies[e]=t}setStrategy(e){if(e===this.$storage.getUniversal("strategy"))return Promise.resolve();if(!this.strategies[e])throw new Error(`Strategy ${e} is not defined!`);return this.reset(),this.$storage.setUniversal("strategy",e),this.mounted()}mounted(...e){return this.getStrategy().mounted?Promise.resolve(this.getStrategy().mounted(...e)).catch((e=>(this.callOnError(e,{method:"mounted"}),Promise.reject(e)))):this.fetchUserOnce()}loginWith(e,...t){return this.setStrategy(e).then((()=>this.login(...t)))}login(...e){return this.getStrategy().login?this.wrapLogin(this.getStrategy().login(...e)).catch((e=>(this.callOnError(e,{method:"login"}),Promise.reject(e)))):Promise.resolve()}fetchUser(...e){return this.getStrategy().fetchUser?Promise.resolve(this.getStrategy().fetchUser(...e)).catch((e=>(this.callOnError(e,{method:"fetchUser"}),Promise.reject(e)))):Promise.resolve()}logout(...e){return this.getStrategy().logout?Promise.resolve(this.getStrategy().logout(...e)).catch((e=>(this.callOnError(e,{method:"logout"}),Promise.reject(e)))):(this.reset(),Promise.resolve())}setUserToken(e,t){return this.getStrategy().setUserToken?Promise.resolve(this.getStrategy().setUserToken(e,t)).catch((e=>(this.callOnError(e,{method:"setUserToken"}),Promise.reject(e)))):(this.getStrategy().token.set(e),Promise.resolve())}reset(...e){return this.getStrategy().reset||(this.setUser(!1),this.getStrategy().token.reset(),this.getStrategy().refreshToken.reset()),this.getStrategy().reset(...e)}refreshTokens(){return this.getStrategy().refreshController?Promise.resolve(this.getStrategy().refreshController.handleRefresh()).catch((e=>(this.callOnError(e,{method:"refreshTokens"}),Promise.reject(e)))):Promise.resolve()}check(...e){return this.getStrategy().check?this.getStrategy().check(...e):{valid:!0}}fetchUserOnce(...e){return this.$state.user?Promise.resolve():this.fetchUser(...e)}setUser(e){this.$storage.setState("user",e);let t={valid:Boolean(e)};t.valid&&(t=this.check()),this.$storage.setState("loggedIn",t.valid)}request(e,t={}){const c="object"==typeof t?Object.assign({},t,e):e;if(""===c.baseURL&&(c.baseURL=n(this.ctx.req)),this.ctx.app.$axios)return this.ctx.app.$axios.request(c).catch((e=>(this.callOnError(e,{method:"request"}),Promise.reject(e))));console.error("[AUTH] add the @nuxtjs/axios module to nuxt.config file")}requestWith(e,t,c){const n=this.getStrategy().token.get(),r=Object.assign({},c,t),o=this.strategies[e].options.token.name||"Authorization";return r.headers||(r.headers={}),!r.headers[o]&&d(n)&&n&&"string"==typeof n&&(r.headers[o]=n),this.request(r)}wrapLogin(e){return this.$storage.setState("busy",!0),this.error=null,Promise.resolve(e).then((e=>(this.$storage.setState("busy",!1),e))).catch((e=>(this.$storage.setState("busy",!1),Promise.reject(e))))}onError(e){this._errorListeners.push(e)}callOnError(e,t={}){this.error=e;for(const c of this._errorListeners)c(e,t)}redirect(e,t=!1){if(!this.options.redirect)return;const c=this.options.fullPathRedirect?this.ctx.route.fullPath:this.ctx.route.path;let n=this.options.redirect[e];if(n){if(this.options.rewriteRedirects&&("login"===e&&v(c)&&!m(this.ctx,n,c)&&this.$storage.setUniversal("redirect",c),"home"===e)){const e=this.$storage.getUniversal("redirect");this.$storage.setUniversal("redirect",null),v(e)&&(n=e)}n=this.callOnRedirect(n,c)||n,m(this.ctx,n,c)||(t?(v(n)&&!n.includes(this.ctx.base)&&(n=y("/"+this.ctx.base+"/"+n)),window.location.replace(n)):this.ctx.redirect(n,this.ctx.query))}}onRedirect(e){this._redirectListeners.push(e)}callOnRedirect(e,t){for(const c of this._redirectListeners)e=c(e,t)||e;return e}hasScope(e){const t=this.$state.user&&x(this.$state.user,this.options.scopeKey);return!!t&&(Array.isArray(t)?t.includes(e):Boolean(x(t,e)))}}const S=async e=>{if(z(e.route,"auth",!1))return;if(!function(e,t=[]){return[].concat(...e.matched.map((function(e,c){return Object.keys(e.components).map((function(n){return t.push(c),e.components[n]}))})))}(e.route,[]).length)return;const{login:t,callback:c}=e.$auth.options.redirect,n=z(e.route,"auth","guest"),r=t=>y(e.route.path,e)===y(t,e);if(e.$auth.$state.loggedIn){const{tokenExpired:c,refreshTokenExpired:o,isRefreshable:l}=e.$auth.check(!0);if((!t||r(t)||n)&&e.$auth.redirect("home"),o)e.$auth.reset();else if(c)if(l)try{await e.$auth.refreshTokens()}catch(t){e.$auth.reset()}else e.$auth.reset()}else n||c&&r(c)||e.$auth.redirect("login")};class k extends Error{constructor(){super("Both token and refresh token have expired. Your request was aborted."),this.name="ExpiredAuthSessionError"}}class L{constructor(e){this.scheme=e,this._refreshPromise=null,this.$auth=e.$auth}handleRefresh(){return this._refreshPromise?this._refreshPromise:this._doRefresh()}_doRefresh(){return this._refreshPromise=new Promise(((e,t)=>{this.scheme.refreshTokens().then((t=>{this._refreshPromise=null,e(t)})).catch((e=>{this._refreshPromise=null,t(e)}))})),this._refreshPromise}}var N,A;(A=N||(N={})).UNKNOWN="UNKNOWN",A.VALID="VALID",A.EXPIRED="EXPIRED";class D{constructor(e,t){this._status=this._calculate(e,t)}unknown(){return N.UNKNOWN===this._status}valid(){return N.VALID===this._status}expired(){return N.EXPIRED===this._status}_calculate(e,t){const c=Date.now();try{if(!e||!t)return N.UNKNOWN}catch(e){return N.UNKNOWN}return c<(t-=500)?N.VALID:N.EXPIRED}}class O{constructor(e,t){this.scheme=e,this.$storage=t}get(){const e=this.scheme.options.refreshToken.prefix+this.scheme.name;return this.$storage.getUniversal(e)}set(e){const t=V(e,this.scheme.options.refreshToken.type);return this._setToken(t),this._updateExpiration(t),t}sync(){const e=this._syncToken();return this._syncExpiration(),e}reset(){this._setToken(!1),this._setExpiration(!1)}status(){return new D(this.get(),this._getExpiration())}_getExpiration(){const e=this.scheme.options.refreshToken.expirationPrefix+this.scheme.name;return this.$storage.getUniversal(e)}_setExpiration(e){const t=this.scheme.options.refreshToken.expirationPrefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncExpiration(){const e=this.scheme.options.refreshToken.expirationPrefix+this.scheme.name;return this.$storage.syncUniversal(e)}_updateExpiration(e){let t;const c=Date.now(),n=1e3*Number(this.scheme.options.refreshToken.maxAge),r=n?c+n:0;try{t=1e3*l(e+"").exp||r}catch(e){if(t=r,!e||"InvalidTokenError"!==e.name)throw e}return this._setExpiration(t||!1)}_setToken(e){const t=this.scheme.options.refreshToken.prefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncToken(){const e=this.scheme.options.refreshToken.prefix+this.scheme.name;return this.$storage.syncUniversal(e)}}class T{constructor(e,t){this.scheme=e,this.axios=t,this.interceptor=null}setHeader(e){this.scheme.options.token.global&&this.axios.setHeader(this.scheme.options.token.name,e)}clearHeader(){this.scheme.options.token.global&&this.axios.setHeader(this.scheme.options.token.name,!1)}initializeRequestInterceptor(e){this.interceptor=this.axios.interceptors.request.use((async t=>{if(!this._needToken(t)||t.url===e)return t;const{valid:c,tokenExpired:n,refreshTokenExpired:r,isRefreshable:o}=this.scheme.check(!0);let l=c;if(r)throw this.scheme.reset(),new k;if(n){if(!o)throw this.scheme.reset(),new k;l=await this.scheme.refreshTokens().then((()=>!0)).catch((()=>{throw this.scheme.reset(),new k}))}const f=this.scheme.token.get();if(!l){if(!f&&this._requestHasAuthorizationHeader(t))throw new k;return t}return this._getUpdatedRequestConfig(t,f)}))}reset(){this.axios.interceptors.request.eject(this.interceptor),this.interceptor=null}_needToken(e){const t=this.scheme.options;return t.token.global||Object.values(t.endpoints).some((t=>"object"==typeof t?t.url===e.url:t===e.url))}_getUpdatedRequestConfig(e,t){return"string"==typeof t&&(e.headers[this.scheme.options.token.name]=t),e}_requestHasAuthorizationHeader(e){return!!e.headers.common[this.scheme.options.token.name]}}class _{constructor(e,t){this.scheme=e,this.$storage=t}get(){const e=this.scheme.options.token.prefix+this.scheme.name;return this.$storage.getUniversal(e)}set(e){const t=V(e,this.scheme.options.token.type);return this._setToken(t),this._updateExpiration(t),"string"==typeof t&&this.scheme.requestHandler.setHeader(t),t}sync(){const e=this._syncToken();return this._syncExpiration(),"string"==typeof e&&this.scheme.requestHandler.setHeader(e),e}reset(){this.scheme.requestHandler.clearHeader(),this._setToken(!1),this._setExpiration(!1)}status(){return new D(this.get(),this._getExpiration())}_getExpiration(){const e=this.scheme.options.token.expirationPrefix+this.scheme.name;return this.$storage.getUniversal(e)}_setExpiration(e){const t=this.scheme.options.token.expirationPrefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncExpiration(){const e=this.scheme.options.token.expirationPrefix+this.scheme.name;return this.$storage.syncUniversal(e)}_updateExpiration(e){let t;const c=Date.now(),n=1e3*Number(this.scheme.options.token.maxAge),r=n?c+n:0;try{t=1e3*l(e+"").exp||r}catch(e){if(t=r,!e||"InvalidTokenError"!==e.name)throw e}return this._setExpiration(t||!1)}_setToken(e){const t=this.scheme.options.token.prefix+this.scheme.name;return this.$storage.setUniversal(t,e)}_syncToken(){const e=this.scheme.options.token.prefix+this.scheme.name;return this.$storage.syncUniversal(e)}}class P{constructor(e,...t){this.$auth=e,this.options=t.reduce(((p,e)=>f(p,e)),{})}get name(){return this.options.name}}const j={name:"local",endpoints:{login:{url:"/api/auth/login",method:"post"},logout:{url:"/api/auth/logout",method:"post"},user:{url:"/api/auth/user",method:"get"}},token:{property:"token",type:"Bearer",name:"Authorization",maxAge:1800,global:!0,required:!0,prefix:"_token.",expirationPrefix:"_token_expiration."},user:{property:"user",autoFetch:!0},clientId:!1,grantType:!1,scope:!1};class F extends P{constructor(e,t,...c){super(e,t,...c,j),this.token=new _(this,this.$auth.$storage),this.requestHandler=new T(this,this.$auth.ctx.$axios)}check(e=!1){const t={valid:!1,tokenExpired:!1};if(!this.token.sync())return t;if(!e)return t.valid=!0,t;return this.token.status().expired()?(t.tokenExpired=!0,t):(t.valid=!0,t)}mounted({tokenCallback:e=(()=>this.$auth.reset()),refreshTokenCallback:t}={}){const{tokenExpired:c,refreshTokenExpired:n}=this.check(!0);return n&&"function"==typeof t?t():c&&"function"==typeof e&&e(),this.initializeRequestInterceptor(),this.$auth.fetchUserOnce()}async login(e,{reset:t=!0}={}){if(!this.options.endpoints.login)return;t&&this.$auth.reset({resetInterceptor:!1}),this.options.clientId&&(e.data.client_id=this.options.clientId),this.options.grantType&&(e.data.grant_type=this.options.grantType),this.options.scope&&(e.data.scope=this.options.scope);const c=await this.$auth.request(e,this.options.endpoints.login);return this.updateTokens(c),this.requestHandler.interceptor||this.initializeRequestInterceptor(),this.options.user.autoFetch&&await this.fetchUser(),c}setUserToken(e){return this.token.set(e),this.fetchUser()}fetchUser(e){return this.check().valid?this.options.endpoints.user?this.$auth.requestWith(this.name,e,this.options.endpoints.user).then((e=>{const t=x(e.data,this.options.user.property);if(!t){const e=new Error(`User Data response does not contain field ${this.options.user.property}`);return Promise.reject(e)}return this.$auth.setUser(t),e})).catch((e=>(this.$auth.callOnError(e,{method:"fetchUser"}),Promise.reject(e)))):(this.$auth.setUser({}),Promise.resolve()):Promise.resolve()}async logout(e={}){return this.options.endpoints.logout&&await this.$auth.requestWith(this.name,e,this.options.endpoints.logout).catch((()=>{})),this.$auth.reset()}reset({resetInterceptor:e=!0}={}){this.$auth.setUser(!1),this.token.reset(),e&&this.requestHandler.reset()}updateTokens(e){const t=!this.options.token.required||x(e.data,this.options.token.property);this.token.set(t)}initializeRequestInterceptor(){this.requestHandler.initializeRequestInterceptor()}}const I={name:"refresh",endpoints:{refresh:{url:"/api/auth/refresh",method:"post"}},refreshToken:{property:"refresh_token",data:"refresh_token",maxAge:2592e3,required:!0,tokenRequired:!1,prefix:"_refresh_token.",expirationPrefix:"_refresh_token_expiration."},autoLogout:!1};class E extends F{constructor(e,t){super(e,t,I),this.refreshToken=new O(this,this.$auth.$storage),this.refreshController=new L(this)}check(e=!1){const t={valid:!1,tokenExpired:!1,refreshTokenExpired:!1,isRefreshable:!0},c=this.token.sync(),n=this.refreshToken.sync();if(!c||!n)return t;if(!e)return t.valid=!0,t;const r=this.token.status();return this.refreshToken.status().expired()?(t.refreshTokenExpired=!0,t):r.expired()?(t.tokenExpired=!0,t):(t.valid=!0,t)}mounted(){return super.mounted({tokenCallback:()=>{this.options.autoLogout&&this.$auth.reset()},refreshTokenCallback:()=>{this.$auth.reset()}})}refreshTokens(){if(!this.options.endpoints.refresh)return Promise.resolve();if(!this.check().valid)return Promise.resolve();if(this.refreshToken.status().expired())throw this.$auth.reset(),new k;this.options.refreshToken.tokenRequired||this.requestHandler.clearHeader();const e={data:{client_id:void 0,grant_type:void 0}};return this.options.refreshToken.required&&this.options.refreshToken.data&&(e.data[this.options.refreshToken.data]=this.refreshToken.get()),this.options.clientId&&(e.data.client_id=this.options.clientId),this.options.grantType&&(e.data.grant_type="refresh_token"),function(e){for(const t in e)void 0===e[t]&&delete e[t]}(e.data),this.$auth.request(e,this.options.endpoints.refresh).then((e=>(this.updateTokens(e,{isRefreshing:!0}),e))).catch((e=>(this.$auth.callOnError(e,{method:"refreshToken"}),Promise.reject(e))))}setUserToken(e,t){return this.token.set(e),t&&this.refreshToken.set(t),this.fetchUser()}reset({resetInterceptor:e=!0}={}){this.$auth.setUser(!1),this.token.reset(),this.refreshToken.reset(),e&&this.requestHandler.reset()}updateTokens(e,{isRefreshing:t=!1,updateOnRefresh:c=!0}={}){const n=!this.options.token.required||x(e.data,this.options.token.property),r=!this.options.refreshToken.required||x(e.data,this.options.refreshToken.property);this.token.set(n),r&&(!t||t&&c)&&this.refreshToken.set(r)}initializeRequestInterceptor(){this.requestHandler.initializeRequestInterceptor(this.options.endpoints.refresh.url)}}},81:function(e,t,c){"use strict";var n={name:"NoSsr",functional:!0,props:{placeholder:String,placeholderTag:{type:String,default:"div"}},render:function(e,t){var c=t.parent,n=t.slots,r=t.props,o=n(),l=o.default;void 0===l&&(l=[]);var f=o.placeholder;return c._isMounted?l:(c.$once("hook:mounted",(function(){c.$forceUpdate()})),r.placeholderTag&&(r.placeholder||f)?e(r.placeholderTag,{class:["no-ssr-placeholder"]},r.placeholder||f):l.length>0?l.map((function(){return e(!1)})):e(!1))}};e.exports=n},9:function(e,t,c){"use strict";c.d(t,"a",(function(){return o}));var n=c(2),r=c(1),o={props:{size:String,expanded:Boolean,loading:Boolean,rounded:Boolean,icon:String,iconPack:String,autocomplete:String,maxlength:[Number,String],useHtml5Validation:{type:Boolean,default:function(){return r.c.defaultUseHtml5Validation}},validationMessage:String,locale:{type:[String,Array],default:function(){return r.c.defaultLocale}},statusIcon:{type:Boolean,default:function(){return r.c.defaultStatusIcon}}},data:function(){return{isValid:!0,isFocused:!1,newIconPack:this.iconPack||r.c.defaultIconPack}},computed:{parentField:function(){for(var e=this.$parent,i=0;i<3;i++)e&&!e.$data._isField&&(e=e.$parent);return e},statusType:function(){var e=(this.parentField||{}).newType;if(e){if("string"==typeof e)return e;for(var t in e)if(e[t])return t}},statusMessage:function(){if(this.parentField)return this.parentField.newMessage||this.parentField.$slots.message},iconSize:function(){switch(this.size){case"is-small":return this.size;case"is-medium":return;case"is-large":return"mdi"===this.newIconPack?"is-medium":""}}},methods:{focus:function(){var e=this.getElement();void 0!==e&&this.$nextTick((function(){e&&e.focus()}))},onBlur:function(e){this.isFocused=!1,this.$emit("blur",e),this.checkHtml5Validity()},onFocus:function(e){this.isFocused=!0,this.$emit("focus",e)},getElement:function(){for(var e=this.$refs[this.$data._elementRef];Object(n.l)(e);)e=e.$refs[e.$data._elementRef];return e},setInvalid:function(){var e=this.validationMessage||this.getElement().validationMessage;this.setValidity("is-danger",e)},setValidity:function(e,t){var c=this;this.$nextTick((function(){c.parentField&&(c.parentField.type||(c.parentField.newType=e),c.parentField.message||(c.parentField.newMessage=t))}))},checkHtml5Validity:function(){if(this.useHtml5Validation){var e=this.getElement();if(void 0!==e)return e.checkValidity()?(this.setValidity(null,null),this.isValid=!0):(this.setInvalid(),this.isValid=!1),this.isValid}}}}}}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 2
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000`
  
  
  
  
Instances: 3
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd0c700.js](https://cassiopee.fabnum.fr/_nuxt/bd0c700.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd0c700.js](https://cassiopee.fabnum.fr/_nuxt/bd0c700.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/favicon.ico](https://cassiopee.fabnum.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/robots.txt](https://cassiopee.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd0c700.js](https://cassiopee.fabnum.fr/_nuxt/bd0c700.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/favicon.ico](https://cassiopee.fabnum.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `e6e-awcc0KMaGM0vIYjkhzBhacoKbW0`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `UklGRiQAAABXRUJQVlA4IBgAAAAwAQCdASoBAAEAAwA0JaQAA3AA/vuUAAA=`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `e6e-awcc0KMaGM0vIYjkhzBhacoKbW0`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>{��k\x0007\x001cУ\x001a\x0018�/!��0ai�</p><p>mm</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(window.webpackJsonp=window.webpackJsonp||[]).push([[2],[,,,,,,function(t,e,n){"use strict";n.r(e),function(t,n){var r=Object.fr", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>window.addEventListener('error', function () {  var e = document.getElementById('nuxt-loading');  if (e) {e.className += ' error';  }});</script>`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>window.addEventListener('error', function () {  var e = document.getElementById('nuxt-loading');  if (e) {e.className += ' error';  }});</script>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/robots.txt](https://cassiopee.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 1
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/bd0c700.js](https://cassiopee.fabnum.fr/_nuxt/bd0c700.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json](https://cassiopee.fabnum.fr/_nuxt/manifest.23112669.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/3267b60.js](https://cassiopee.fabnum.fr/_nuxt/3267b60.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/favicon.ico](https://cassiopee.fabnum.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://cassiopee.fabnum.fr/](https://cassiopee.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `23112669`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23112669`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33333337`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/366f947.js](https://cassiopee.fabnum.fr/_nuxt/366f947.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/sitemap.xml](https://cassiopee.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `23112669`
  
  
  
  
* URL: [https://cassiopee.fabnum.fr/_nuxt/2a059cb.js](https://cassiopee.fabnum.fr/_nuxt/2a059cb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `66666674`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>23112669, which evaluates to: 1970-09-25 12:11:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Wed, 15 Sep 2021 15:16:42


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Source Code Disclosure - Java | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 3 | 
| X-Frame-Options Header Not Set | Medium | 2 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 3 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 3 | 
| Permissions Policy Header Not Set | Low | 12 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 5 | 
| Content-Type Header Missing | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 3 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 3 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/start-28b178f4.js](https://dora.beta.gouv.fr/_app/start-28b178f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class at{constructor({base:t,routes:e,trailing_slash:r,renderer:s}){this.base=t,this.routes=e,this.trailing_slash=r,this.renderer=s,s.router=this,this.enabled=!0,document.body.setAttribute("tabindex","-1"),history.replaceState(history.state||{},"",location.href)}init_listeners(){let t;"scrollRestoration"in history&&(history.scrollRestoration="manual"),addEventListener("beforeunload",(()=>{history.scrollRestoration="auto"})),addEventListener("load",(()=>{history.scrollRestoration="manual"})),addEventListener("scroll",(()=>{clearTimeout(t),t=setTimeout((()=>{const t=(s=i({},history.state||{}),o={"sveltekit:scroll":ot()},e(s,r(o)));var s,o;history.replaceState(t,document.title,window.location.href)}),50)}));const s=t=>{const e=nt(t.target);e&&e.href&&e.hasAttribute("sveltekit:prefetch")&&this.prefetch(new URL(e.href))};let o;addEventListener("touchstart",s),addEventListener("mousemove",(t=>{clearTimeout(o),o=setTimeout((()=>{s(t)}),20)})),addEventListener("click",(t=>{if(!this.enabled)return;if(t.button||1!==t.which)return;if(t.metaKey||t.ctrlKey||t.shiftKey||t.altKey)return;if(t.defaultPrevented)return;const e=nt(t.target);if(!e)return;if(!e.href)return;const r="object"==typeof e.href&&"SVGAnimatedString"===e.href.constructor.name,s=String(r?e.href.baseVal:e.href);if(s===location.href)return void(location.hash||t.preventDefault());const o=(e.getAttribute("rel")||"").split(/\s+/);if(e.hasAttribute("download")||o&&o.includes("external"))return;if(r?e.target.baseVal:e.target)return;const n=new URL(s);if(!this.owns(n))return;const a=e.hasAttribute("sveltekit:noscroll");history.pushState({},"",n.href),this._navigate(n,a?ot():null,!1,[],n.hash),t.preventDefault()})),addEventListener("popstate",(t=>{if(t.state&&this.enabled){const e=new URL(location.href);this._navigate(e,t.state["sveltekit:scroll"],!1,[])}}))}owns(t){return t.origin===location.origin&&t.pathname.startsWith(this.base)}parse(t){if(this.owns(t)){const e=t.pathname.slice(this.base.length)||"/",r=decodeURI(e),s=this.routes.filter((([t])=>t.test(r))),o=new URLSearchParams(t.search);return{id:`${e}?${o}`,routes:s,path:e,query:o}}}async goto(t,{noscroll:e=!1,replaceState:r=!1,keepfocus:s=!1,state:o={}}={},n){const a=new URL(t,function(t){let e=t.baseURI;if(!e){const r=t.getElementsByTagName("base");e=r.length?r[0].href:t.URL}return e}(document));return this.enabled&&this.owns(a)?(history[r?"replaceState":"pushState"](o,"",t),this._navigate(a,e?ot():null,s,n,a.hash)):(location.href=a.href,new Promise((()=>{})))}enable(){this.enabled=!0}disable(){this.enabled=!1}async prefetch(t){const e=this.parse(t);if(!e)throw new Error("Attempted to prefetch a URL that does not belong to this app");return this.renderer.load(e)}async _navigate(t,e,r,s,o){const n=this.parse(t);if(!n)throw new Error("Attempted to navigate to a URL that does not belong to this app");if("/"!==n.path){const t=n.path.endsWith("/");(t&&"never"===this.trailing_slash||!t&&"always"===this.trailing_slash&&!(n.path.split("/").pop()||"").includes("."))&&(n.path=t?n.path.slice(0,-1):n.path+"/",history.replaceState({},"",`${this.base}${n.path}${location.search}`))}this.renderer.notify({path:n.path,query:n.query}),await this.renderer.update(n,s,!1),r||document.body.focus();const a=o&&document.getElementById(o.slice(1));e?scrollTo(e.x,e.y):a?a.scrollIntoView():scrollTo(0,0)}}function it(t){const e=D(t);let r=!0;return{notify:function(){r=!0,e.update((t=>t))},set:function(t){r=!1,e.set(t)},subscribe:function(t){let s;return e.subscribe((e=>{(void 0===s||r&&e!==s)&&t(s=e)}))}}}function lt(t,e){let r=`script[data-type="svelte-data"][data-url="${"string"==typeof t?t:t.url}"]`;e&&"string"==typeof e.body&&(r+=`[data-body="${function(t){let e=5381,r=t.length;if("string"==typeof t)for(;r;)e=33*e^t.charCodeAt(--r);else for(;r;)e=33*e^t[--r];return(e>>>0).toString(36)}(e.body)}"]`);const a=document.querySelector(r);if(a&&a.textContent){const t=JSON.parse(a.textContent),{body:e}=t,r=((t,e)=>{var r={};for(var a in t)o.call(t,a)&&e.indexOf(a)<0&&(r[a]=t[a]);if(null!=t&&s)for(var a of s(t))e.indexOf(a)<0&&n.call(t,a)&&(r[a]=t[a]);return r})(t,["body"]);return Promise.resolve(new Response(e,r))}return fetch(t,e)}class ct{constructor({Root:t,fallback:e,target:r,session:s,host:o}){this.Root=t,this.fallback=e,this.host=o,this.router,this.target=r,this.started=!1,this.session_id=1,this.invalid=new Set,this.invalidating=null,this.current={page:null,session_id:null,branch:[]},this.cache=new Map,this.loading={id:null,promise:null},this.stores={page:it({}),navigating:D(null),session:D(s)},this.$session=null,this.root=null;let n=!1;this.stores.session.subscribe((async t=>{if(this.$session=t,!n||!this.router)return;this.session_id+=1;const e=this.router.parse(new URL(location.href));e&&this.update(e,[],!0)})),n=!0}async start({status:t,error:e,nodes:r,page:s}){const o=[];let n,a,l={};try{for(let n=0;n<r.length;n+=1){const c=n===r.length-1,u=await this._load_node({module:await r[n],page:s,context:l,status:c?t:void 0,error:c?e:void 0});if(o.push(u),u&&u.loaded)if(u.loaded.error){if(e)throw u.loaded.error;a={status:u.loaded.status,error:u.loaded.error,path:s.path,query:s.query}}else u.loaded.context&&(l=i(i({},l),u.loaded.context))}n=a?await this._load_error(a):await this._get_navigation_result_from_branch({page:s,branch:o})}catch(u){if(e)throw u;n=await this._load_error({status:500,error:(c=u,c instanceof Error?c:new Error(JSON.stringify(c))),path:s.path,query:s.query})}var c;n.redirect?location.href=new URL(n.redirect,location.href).href:this._init(n)}notify({path:t,query:e}){dispatchEvent(new CustomEvent("sveltekit:navigation-start")),this.started&&this.stores.navigating.set({from:{path:this.current.page.path,query:this.current.page.query},to:{path:t,query:e}})}async update(t,e,r){const s=this.token={};let o=await this._get_navigation_result(t,r);if(s!==this.token)return;if(this.invalid.clear(),o.redirect){if(!(e.length>10||e.includes(t.path)))return void(this.router?this.router.goto(o.redirect,{replaceState:!0},[...e,t.path]):location.href=new URL(o.redirect,location.href).href);o=await this._load_error({status:500,error:new Error("Redirect loop"),path:t.path,query:t.query})}if(o.reload?location.reload():this.started?(this.current=o.state,this.root.$set(o.props),this.stores.navigating.set(null),await 0):this._init(o),dispatchEvent(new CustomEvent("sveltekit:navigation-end")),this.loading.promise=null,this.loading.id=null,!this.router)return;const n=o.state.branch[o.state.branch.length-1];n&&!1===n.module.router?this.router.disable():this.router.enable()}load(t){return this.loading.promise=this._get_navigation_result(t,!1),this.loading.id=t.id,this.loading.promise}invalidate(t){return this.invalid.add(t),this.invalidating||(this.invalidating=Promise.resolve().then((async()=>{const t=this.router&&this.router.parse(new URL(location.href));t&&await this.update(t,[],!0),this.invalidating=null}))),this.invalidating}_init(t){this.current=t.state;const e=document.querySelector("style[data-svelte]");e&&e.remove(),this.root=new this.Root({target:this.target,props:i({stores:this.stores},t.props),hydrate:!0}),this.started=!0}async _get_navigation_result(t,e){if(this.loading.id===t.id)return this.loading.promise;for(let r=0;r<t.routes.length;r+=1){const s=t.routes[r];if(1===s.length)return{reload:!0,props:{},state:this.current};let o=r+1;for(;o<t.routes.length;){const e=t.routes[o];if(e[0].toString()!==s[0].toString())break;1!==e.length&&e[1].forEach((t=>t())),o+=1}const n=await this._load({route:s,path:t.path,query:t.query},e);if(n)return n}return await this._load_error({status:404,error:new Error(`Not found: ${t.path}`),path:t.path,query:t.query})}async _get_navigation_result_from_branch({page:t,branch:e}){const r=e.filter(Boolean),s={state:{page:t,branch:e,session_id:this.session_id},props:{components:r.map((t=>t.module.default))}};for(let a=0;a<r.length;a+=1){const t=r[a].loaded;t&&(s.props[`props_${a}`]=await t.props)}this.current.page&&t.path===this.current.page.path&&t.query.toString()===this.current.page.query.toString()||(s.props.page=t);const o=r[r.length-1],n=o.loaded&&o.loaded.maxage;if(n){const e=`${t.path}?${t.query}`;let r=!1;const o=()=>{this.cache.get(e)===s&&this.cache.delete(e),i(),clearTimeout(a)},a=setTimeout(o,1e3*n),i=this.stores.session.subscribe((()=>{r&&o()}));r=!0,this.cache.set(e,s)}return s}async _load_node({status:t,error:e,module:r,page:s,context:o}){const n={module:r,uses:{params:new Set,path:!1,query:!1,session:!1,context:!1,dependencies:[]},loaded:null,context:o},a={};for(const i in s.params)Object.defineProperty(a,i,{get:()=>(n.uses.params.add(i),s.params[i]),enumerable:!0});const l=this.$session;if(r.load){const{started:c}=this,u={page:{host:s.host,params:a,get path(){return n.uses.path=!0,s.path},get query(){return n.uses.query=!0,s.query}},get session(){return n.uses.session=!0,l},get context(){return n.uses.context=!0,i({},o)},fetch(t,e){const r="string"==typeof t?t:t.url,{href:o}=new URL(r,new URL(s.path,document.baseURI));return n.uses.dependencies.push(o),c?fetch(t,e):lt(t,e)}};e&&(u.status=t,u.error=e);const d=await r.load.call(null,u);if(!d)return;n.loaded=function(t){const e=t.status&&t.status>=400&&t.status<=599&&!t.redirect;if(t.error||e){const r=t.status;if(!t.error&&e)return{status:r||500,error:new Error};const s="string"==typeof t.error?new Error(t.error):t.error;return s instanceof Error?!r||r<400||r>599?(console.warn('"error" returned from load() without a valid status code — defaulting to 500'),{status:500,error:s}):{status:r,error:s}:{status:500,error:new Error(`"error" property returned from load() must be a string or instance of Error, received type "${typeof s}"`)}}if(t.redirect){if(!t.status||3!==Math.floor(t.status/100))return{status:500,error:new Error('"redirect" property returned from load() must be accompanied by a 3xx status code')};if("string"!=typeof t.redirect)return{status:500,error:new Error('"redirect" property returned from load() must be a string')}}return t}(d),n.loaded.context&&(n.context=n.loaded.context)}return n}async _load({route:t,path:e,query:r},s){const o=`${e}?${r}`;if(!s){const t=this.cache.get(o);if(t)return t}const[n,a,l,c]=t,u=c?c(n.exec(e)):{},d=this.current.page&&{path:e!==this.current.page.path,params:Object.keys(u).filter((t=>this.current.page.params[t]!==u[t])),query:r.toString()!==this.current.page.query.toString(),session:this.session_id!==this.current.session_id},h={host:this.host,path:e,query:r,params:u},p=[];let f,g={},_=!1,m=200;a.forEach((t=>t()));t:for(let $=0;$<a.length;$+=1){let t;try{if(!a[$])continue;const e=await a[$](),r=this.current.branch[$];if(!r||e!==r.module||d.path&&r.uses.path||d.params.some((t=>r.uses.params.has(t)))||d.query&&r.uses.query||d.session&&r.uses.session||r.uses.dependencies.some((t=>this.invalid.has(t)))||_&&r.uses.context){t=await this._load_node({module:e,page:h,context:g});const r=$===a.length-1;if(t&&t.loaded){if(t.loaded.error&&(m=t.loaded.status,f=t.loaded.error),t.loaded.redirect)return{redirect:t.loaded.redirect,props:{},state:this.current};t.loaded.context&&(_=!0)}else if(r&&e.load)return}else t=r}catch(y){m=500,f=y}if(f){for(;$--;)if(l[$]){let t,e,r=$;for(;!(e=p[r]);)r-=1;try{if(t=await this._load_node({status:m,error:f,module:await l[$](),page:h,context:e.context}),t&&t.loaded&&t.loaded.error)continue;p.push(t);break t}catch(y){continue}}return await this._load_error({status:m,error:f,path:e,query:r})}t&&t.loaded&&t.loaded.context&&(g=i(i({},g),t.loaded.context)),p.push(t)}return await this._get_navigation_result_from_branch({page:h,branch:p})}async _load_error({status:t,error:e,path:r,query:s}){const o={host:this.host,path:r,query:s,params:{}},n=await this._load_node({module:await this.fallback[0],page:o,context:{}}),a=[n,await this._load_node({status:t,error:e,module:await this.fallback[1],page:o,context:n&&n.loaded&&n.loaded.context||{}})];return await this._get_navigation_result_from_branch({page:o,branch:a})}}async function ut({paths:t,target:e,session:r,host:s,route:o,spa:n,trailing_slash:a,hydrate:i}){const l=new ct({Root:Y,fallback:rt,target:e,session:r,host:s}),c=o?new at({base:t.base,routes:et,trailing_slash:a,renderer:l}):null;U(c),function(t){st=t.base,t.assets}(t),i&&await l.start(i),c&&(n&&c.goto(location.href,{replaceState:!0},[]),c.init_listeners()),dispatchEvent(new CustomEvent("sveltekit:start"))}export{ut as start}`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class sd{constructor(e,t){this.editor=e,this.commands=t}createCommands(){const{commands:e,editor:t}=this,{state:n,view:r}=t,{tr:o}=n,i=this.buildProps(o);return Object.fromEntries(Object.entries(e).map((([e,t])=>[e,(...e)=>{const n=t(...e)(i);return o.getMeta("preventDispatch")||r.dispatch(o),n}])))}createChain(e,t=!0){const{commands:n,editor:r}=this,{state:o,view:i}=r,s=[],l=!!e,u=e||o.tr,p=c(a({},Object.fromEntries(Object.entries(n).map((([e,n])=>[e,(...e)=>{const r=this.buildProps(u,t),o=n(...e)(r);return s.push(o),p}])))),{run:()=>(l||!t||u.getMeta("preventDispatch")||i.dispatch(u),s.every((e=>!0===e)))});return p}createCan(e){const{commands:t,editor:n}=this,{state:r}=n,o=void 0,i=e||r.tr,s=this.buildProps(i,o),l=Object.fromEntries(Object.entries(t).map((([e,t])=>[e,(...e)=>t(...e)(c(a({},s),{dispatch:o}))])));return c(a({},l),{chain:()=>this.createChain(i,o)})}buildProps(e,t=!0){const{editor:n,commands:r}=this,{state:o,view:i}=n;o.storedMarks&&e.setStoredMarks(o.storedMarks);const s={tr:e,editor:n,view:i,state:this.chainableState(e,o),dispatch:t?()=>{}:void 0,chain:()=>this.createChain(e),can:()=>this.createCan(e),get commands(){return Object.fromEntries(Object.entries(r).map((([e,t])=>[e,(...e)=>t(...e)(s)])))}};return s}chainableState(e,t){let{selection:n}=e,{doc:r}=e,{storedMarks:o}=e;return c(a({},t),{schema:t.schema,plugins:t.plugins,apply:t.apply.bind(t),applyTransaction:t.applyTransaction.bind(t),reconfigure:t.reconfigure.bind(t),toJSON:t.toJSON.bind(t),get storedMarks(){return o},get selection(){return n},get doc(){return r},get tr(){return n=e.selection,r=e.doc,o=e.storedMarks,e}})}}function ad(e,t,n={}){if(void 0===e.config[t]&&e.parent)return ad(e.parent,t,n);if("function"==typeof e.config[t]){return e.config[t].bind(c(a({},n),{parent:e.parent?ad(e.parent,t,n):null}))}return e.config[t]}function cd(e){return{baseExtensions:e.filter((e=>"extension"===e.type)),nodeExtensions:e.filter((e=>"node"===e.type)),markExtensions:e.filter((e=>"mark"===e.type))}}function ld(e){const t=[],{nodeExtensions:n,markExtensions:r}=cd(e),o=[...n,...r],i={default:null,rendered:!0,renderHTML:null,parseHTML:null,keepOnSplit:!0};return e.forEach((e=>{const n=ad(e,"addGlobalAttributes",{name:e.name,options:e.options});if(!n)return;n().forEach((e=>{e.types.forEach((n=>{Object.entries(e.attributes).forEach((([e,r])=>{t.push({type:n,name:e,attribute:a(a({},i),r)})}))}))}))})),o.forEach((e=>{const n={name:e.name,options:e.options},r=ad(e,"addAttributes",n);if(!r)return;const o=r();Object.entries(o).forEach((([n,r])=>{t.push({type:e.name,name:n,attribute:a(a({},i),r)})}))})),t}function ud(...e){return e.filter((e=>!!e)).reduce(((e,t)=>{const n=a({},e);return Object.entries(t).forEach((([e,t])=>{n[e]?n[e]="class"===e?[n[e],t].join(" "):"style"===e?[n[e],t].join("; "):t:n[e]=t})),n}),{})}function pd(e,t){return t.filter((e=>e.attribute.rendered)).map((t=>t.attribute.renderHTML?t.attribute.renderHTML(e.attrs)||{}:{[t.name]:e.attrs[t.name]})).reduce(((e,t)=>ud(e,t)),{})}function dd(e,t){return e.style?e:c(a({},e),{getAttrs:n=>{const r=e.getAttrs?e.getAttrs(n):e.attrs;if(!1===r)return!1;const o=t.filter((e=>e.attribute.rendered)).reduce(((e,t)=>{const r=t.attribute.parseHTML?t.attribute.parseHTML(n)||{}:{[t.name]:(o=n.getAttribute(t.name),"string"!=typeof o?o:o.match(/^\d*(\.\d+)?$/)?Number(o):"true"===o||"false"!==o&&o)};var o;const i=Object.fromEntries(Object.entries(r).filter((([,e])=>null!=e)));return a(a({},e),i)}),{});return a(a({},r),o)}})}function hd(e,t,...n){return"function"==typeof e?t?e.bind(t)(...n):e(...n):e}function fd(e){return Object.fromEntries(Object.entries(e).filter((([e,t])=>("attrs"!==e||!function(e={}){return 0===Object.keys(e).length&&e.constructor===Object}(t))&&null!=t)))}function md(e,t){return t.nodes[e]?t.nodes[e]:t.marks[e]?t.marks[e]:null}class gd{constructor(e,t){this.splittableMarks=[],this.editor=t,this.extensions=gd.resolve(e),this.schema=function(e){var t;const n=ld(e),{nodeExtensions:r,markExtensions:o}=cd(e),i=null===(t=r.find((e=>ad(e,"topNode"))))||void 0===t?void 0:t.name,s=Object.fromEntries(r.map((t=>{const r=n.filter((e=>e.type===t.name)),o={name:t.name,options:t.options},i=e.reduce(((e,n)=>{const r=ad(n,"extendNodeSchema",o);return a(a({},e),r?r(t):{})}),{}),s=fd(c(a({},i),{content:hd(ad(t,"content",o)),marks:hd(ad(t,"marks",o)),group:hd(ad(t,"group",o)),inline:hd(ad(t,"inline",o)),atom:hd(ad(t,"atom",o)),selectable:hd(ad(t,"selectable",o)),draggable:hd(ad(t,"draggable",o)),code:hd(ad(t,"code",o)),defining:hd(ad(t,"defining",o)),isolating:hd(ad(t,"isolating",o)),attrs:Object.fromEntries(r.map((e=>{var t;return[e.name,{default:null===(t=null==e?void 0:e.attribute)||void 0===t?void 0:t.default}]})))})),l=hd(ad(t,"parseHTML",o));l&&(s.parseDOM=l.map((e=>dd(e,r))));const u=ad(t,"renderHTML",o);return u&&(s.toDOM=e=>u({node:e,HTMLAttributes:pd(e,r)})),[t.name,s]}))),l=Object.fromEntries(o.map((t=>{const r=n.filter((e=>e.type===t.name)),o={name:t.name,options:t.options},i=e.reduce(((e,n)=>{const r=ad(n,"extendMarkSchema",o);return a(a({},e),r?r(t):{})}),{}),s=fd(c(a({},i),{inclusive:hd(ad(t,"inclusive",o)),excludes:hd(ad(t,"excludes",o)),group:hd(ad(t,"group",o)),spanning:hd(ad(t,"spanning",o)),attrs:Object.fromEntries(r.map((e=>{var t;return[e.name,{default:null===(t=null==e?void 0:e.attribute)||void 0===t?void 0:t.default}]})))})),l=hd(ad(t,"parseHTML",o));l&&(s.parseDOM=l.map((e=>dd(e,r))));const u=ad(t,"renderHTML",o);return u&&(s.toDOM=e=>u({mark:e,HTMLAttributes:pd(e,r)})),[t.name,s]})));return new Js({topNode:i,nodes:s,marks:l})}(this.extensions),this.extensions.forEach((e=>{var t;const n={name:e.name,options:e.options,editor:this.editor,type:md(e.name,this.schema)};if("mark"===e.type){(null===(t=hd(ad(e,"keepOnSplit",n)))||void 0===t||t)&&this.splittableMarks.push(e.name)}const r=ad(e,"onBeforeCreate",n);r&&this.editor.on("beforeCreate",r);const o=ad(e,"onCreate",n);o&&this.editor.on("create",o);const i=ad(e,"onUpdate",n);i&&this.editor.on("update",i);const s=ad(e,"onSelectionUpdate",n);s&&this.editor.on("selectionUpdate",s);const a=ad(e,"onTransaction",n);a&&this.editor.on("transaction",a);const c=ad(e,"onFocus",n);c&&this.editor.on("focus",c);const l=ad(e,"onBlur",n);l&&this.editor.on("blur",l);const u=ad(e,"onDestroy",n);u&&this.editor.on("destroy",u)}))}static resolve(e){return gd.sort(gd.flatten(e))}static flatten(e){return e.map((e=>{const t=ad(e,"addExtensions",{name:e.name,options:e.options});return t?[e,...this.flatten(t())]:e})).flat(10)}static sort(e){return e.sort(((e,t)=>{const n=ad(e,"priority")||100,r=ad(t,"priority")||100;return n>r?-1:n<r?1:0}))}get commands(){return this.extensions.reduce(((e,t)=>{const n=ad(t,"addCommands",{name:t.name,options:t.options,editor:this.editor,type:md(t.name,this.schema)});return n?a(a({},e),n()):e}),{})}get plugins(){return[...this.extensions].reverse().map((e=>{const t={name:e.name,options:e.options,editor:this.editor,type:md(e.name,this.schema)},n=[],r=ad(e,"addKeyboardShortcuts",t);if(r){const e=function(e){return new pc({props:{handleKeyDown:_p(e)}})}(Object.fromEntries(Object.entries(r()).map((([e,t])=>[e,()=>t({editor:this.editor})]))));n.push(e)}const o=ad(e,"addInputRules",t);if(this.editor.options.enableInputRules&&o){const e=o(),t=e.length?[(i={rules:e},s=i.rules,a=new pc({state:{init:function(){return null},apply:function(e,t){var n=e.getMeta(this);return n||(e.selectionSet||e.docChanged?null:t)}},props:{handleTextInput:function(e,t,n,r){return wp(e,t,n,r,s,a)},handleDOMEvents:{compositionend:function(e){setTimeout((function(){var t=e.state.selection.$cursor;t&&wp(e,t.pos,t.pos,"",s,a)}))}}},isInputRules:!0}),a)]:[];n.push(...t)}var i,s,a;const c=ad(e,"addPasteRules",t);if(this.editor.options.enablePasteRules&&c){const e=c();n.push(...e)}const l=ad(e,"addProseMirrorPlugins",t);if(l){const e=l();n.push(...e)}return n})).flat()}get attributes(){return ld(this.extensions)}get nodeViews(){const{editor:e}=this,{nodeExtensions:t}=cd(this.extensions);return Object.fromEntries(t.filter((e=>!!ad(e,"addNodeView"))).map((t=>{const n=this.attributes.filter((e=>e.type===t.name)),r={name:t.name,options:t.options,editor:e,type:Yp(t.name,this.schema)},o=ad(t,"addNodeView",r);if(!o)return[];return[t.name,(r,i,s,a)=>{const c=pd(r,n);return o()({editor:e,node:r,getPos:s,decorations:a,HTMLAttributes:c,extension:t})}]})))}get textSerializers(){const{editor:e}=this,{nodeExtensions:t}=cd(this.extensions);return Object.fromEntries(t.filter((e=>!!ad(e,"renderText"))).map((t=>{const n=ad(t,"renderText",{name:t.name,options:t.options,editor:e,type:Yp(t.name,this.schema)});if(!n)return[];return[t.name,e=>n(e)]})))}}function vd(e){return"Object"===function(e){return Object.prototype.toString.call(e).slice(8,-1)}(e)&&(e.constructor===Object&&Object.getPrototypeOf(e)===Object.prototype)}function yd(e,t){const n=a({},e);return vd(e)&&vd(t)&&Object.keys(t).forEach((r=>{vd(t[r])?r in e?n[r]=yd(e[r],t[r]):Object.assign(n,{[r]:t[r]}):Object.assign(n,{[r]:t[r]})})),n}class _d{constructor(e={}){this.type="extension",this.name="extension",this.parent=null,this.child=null,this.config={name:this.name,defaultOptions:{}},this.config=a(a({},this.config),e),this.name=this.config.name,this.options=this.config.defaultOptions}static create(e={}){return new _d(e)}configure(e={}){const t=this.extend();return t.options=yd(this.options,e),t}extend(e={}){const t=new _d(e);return t.parent=this,this.child=t,t.name=e.name?e.name:t.parent.name,t.options=e.defaultOptions?e.defaultOptions:t.parent.options,t}}const bd=_d.create({name:"editable",addProseMirrorPlugins(){return[new pc({key:new fc("clipboardTextSerializer"),props:{clipboardTextSerializer:()=>{const{editor:e}=this,{from:t,to:n}=e.state.selection;return((e,t,n,r,o)=>{let i="",s=!0;return e.state.doc.nodesBetween(t,n,((a,c)=>{var l;const u=e.extensionManager.textSerializers[a.type.name];u?(i+=u({node:a}),s=!r):a.isText?(i+=null===(l=null==a?void 0:a.text)||void 0===l?void 0:l.slice(Math.max(t,c)-c,n-c),s=!r):a.isLeaf&&o?(i+=o,s=!r):!s&&a.isBlock&&(i+=r,s=!0)}),0),i})(e,t,n,"\n")}}})]}});var wd=Object.freeze({__proto__:null,blur:()=>({editor:e,view:t})=>(requestAnimationFrame((()=>{e.isDestroyed||t.dom.blur()})),!0)});var kd=Object.freeze({__proto__:null,clearContent:(e=!1)=>({commands:t})=>t.setContent("",e)});var xd=Object.freeze({__proto__:null,clearNodes:()=>({state:e,tr:t,dispatch:n})=>{const{selection:r}=t,{ranges:o}=r;return o.forEach((r=>{e.doc.nodesBetween(r.$from.pos,r.$to.pos,((e,r)=>{if(e.type.isText)return;const o=t.doc.resolve(t.mapping.map(r)),i=t.doc.resolve(t.mapping.map(r+e.nodeSize)),s=o.blockRange(i);if(!s)return;const a=Ma(s);if(e.type.isTextblock&&n){const{defaultType:e}=o.parent.contentMatchAt(o.index());t.setNodeMarkup(s.start,e)}(a||0===a)&&n&&t.lift(s,a)}))})),!0}});var Sd=Object.freeze({__proto__:null,command:e=>t=>e(t)});var Md=Object.freeze({__proto__:null,createParagraphNear:()=>({state:e,dispatch:t})=>jp(e,t)});var Ed=Object.freeze({__proto__:null,deleteNode:e=>({tr:t,state:n,dispatch:r})=>{const o=Yp(e,n.schema),i=t.selection.$anchor;for(let e=i.depth;e>0;e-=1){if(i.node(e).type===o){if(r){const n=i.before(e),r=i.after(e);t.delete(n,r).scrollIntoView()}return!0}}return!1}});var Od=Object.freeze({__proto__:null,deleteRange:e=>({tr:t,dispatch:n})=>{const{from:r,to:o}=e;return n&&t.delete(r,o),!0}});var Td=Object.freeze({__proto__:null,deleteSelection:()=>({state:e,dispatch:t})=>Sp(e,t)});var Cd=Object.freeze({__proto__:null,enter:()=>({commands:e})=>e.keyboardShortcut("Enter")});var Ad=Object.freeze({__proto__:null,exitCode:()=>({state:e,dispatch:t})=>Dp(e,t)});function Nd(e,t,n={}){return e.find((e=>e.type===t&&ed(e.attrs,n)))}function zd(e,t,n={}){return!!Nd(e,t,n)}function Pd(e,t,n={}){if(!e||!t)return;const r=e.parent.childAfter(e.parentOffset);if(!r.node)return;const o=Nd(r.node.marks,t,n);if(!o)return;let i=e.index(),s=e.start()+r.offset,a=i+1,c=s+r.node.nodeSize;for(Nd(r.node.marks,t,n);i>0&&o.isInSet(e.parent.child(i-1).marks);)i-=1,s-=e.parent.child(i).nodeSize;for(;a<e.parent.childCount&&zd(e.parent.child(a).marks,t,n);)c+=e.parent.child(a).nodeSize,a+=1;return{from:s,to:c}}var Id=Object.freeze({__proto__:null,extendMarkRange:(e,t={})=>({tr:n,state:r,dispatch:o})=>{const i=Xp(e,r.schema),{doc:s,selection:a}=n,{$from:c,from:l,to:u}=a;if(o){const e=Pd(c,i,t);if(e&&e.from<=l&&e.to>=u){const t=Ka.create(s,e.from,e.to);n.setSelection(t)}}return!0}});var Dd=Object.freeze({__proto__:null,first:e=>t=>{const n="function"==typeof e?e(t):e;for(let e=0;e<n.length;e+=1)if(n[e](t))return!0;return!1}});function jd(e=0,t=0,n=0){return Math.min(Math.max(e,t),n)}function Rd(e){return(t=e)&&"object"==typeof t&&!Array.isArray(t)&&!function(e){var t;return"class"===(null===(t=e.constructor)||void 0===t?void 0:t.toString().substring(0,5))}(t)&&e instanceof Ka;var t}var Ld=Object.freeze({__proto__:null,focus:(e=null)=>({editor:t,view:n,tr:r,dispatch:o})=>{const i=()=>{requestAnimationFrame((()=>{t.isDestroyed||n.focus()}))};if(n.hasFocus()&&null===e||!1===e)return!0;if(o&&null===e&&!Rd(t.state.selection))return i(),!0;const{from:s,to:a}=function(e,t=null){if(!t)return null;if("start"===t||!0===t)return{from:0,to:0};if("end"===t){const{size:t}=e.doc.content;return{from:t,to:t}}return{from:t,to:t}}(t.state,e)||t.state.selection,{doc:c,storedMarks:l}=r,u=Ua.atStart(c).from,p=Ua.atEnd(c).to,d=jd(s,u,p),h=jd(a,u,p),f=Ka.create(c,d,h),m=t.state.selection.eq(f);return o&&(m||r.setSelection(f),m&&l&&r.setStoredMarks(l),i()),!0}});var Bd=Object.freeze({__proto__:null,forEach:(e,t)=>n=>e.every(((e,r)=>t(e,c(a({},n),{index:r}))))});var $d=Object.freeze({__proto__:null,insertContent:(e,t)=>({tr:n,commands:r})=>r.insertContentAt({from:n.selection.from,to:n.selection.to},e,t)});var Hd=Object.freeze({__proto__:null,insertContentAt:(e,t,n)=>({tr:r,dispatch:o,editor:i})=>{if(o){const o=od(t,i.schema,a({parseOptions:{preserveWhitespace:"full"}},n||{}));if("<>"===o.toString())return!0;const{from:s,to:c}="number"==typeof e?{from:e,to:e}:e;r.replaceWith(s,c,o),function(e,t,n){const r=e.steps.length-1;if(r<t)return;const o=e.steps[r];if(!(o instanceof wa||o instanceof ka))return;const i=e.mapping.maps[r];let s=0;i.forEach(((e,t,n,r)=>{0===s&&(s=r)})),e.setSelection(Ua.near(e.doc.resolve(s),n))}(r,r.steps.length-1,1)}return!0}});var Fd=Object.freeze({__proto__:null,joinBackward:()=>({state:e,dispatch:t})=>Mp(e,t)});var Vd=Object.freeze({__proto__:null,joinForward:()=>({state:e,dispatch:t})=>Cp(e,t)});const qd="undefined"!=typeof navigator&&/Mac/.test(navigator.platform);var Ud=Object.freeze({__proto__:null,keyboardShortcut:e=>({editor:t,view:n,tr:r,dispatch:o})=>{const i=function(e){const t=e.split(/-(?!$)/);let n,r,o,i,s=t[t.length-1];"Space"===s&&(s=" ");for(let a=0;a<t.length-1;a+=1){const e=t[a];if(/^(cmd|meta|m)$/i.test(e))i=!0;else if(/^a(lt)?$/i.test(e))n=!0;else if(/^(c|ctrl|control)$/i.test(e))r=!0;else if(/^s(hift)?$/i.test(e))o=!0;else{if(!/^mod$/i.test(e))throw new Error(`Unrecognized modifier name: ${e}`);qd?i=!0:r=!0}}return n&&(s=`Alt-${s}`),r&&(s=`Ctrl-${s}`),i&&(s=`Meta-${s}`),o&&(s=`Shift-${s}`),s}(e).split(/-(?!$)/),s=i.find((e=>!["Alt","Ctrl","Meta","Shift"].includes(e))),a=new KeyboardEvent("keydown",{key:"Space"===s?" ":s,altKey:i.includes("Alt"),ctrlKey:i.includes("Ctrl"),metaKey:i.includes("Meta"),shiftKey:i.includes("Shift"),bubbles:!0,cancelable:!0}),c=t.captureTransaction((()=>{n.someProp("handleKeyDown",(e=>e(n,a)))}));return null==c||c.steps.forEach((e=>{const t=e.map(r.mapping);t&&o&&r.maybeStep(t)})),!0}});var Wd=Object.freeze({__proto__:null,lift:(e,t={})=>({state:n,dispatch:r})=>!!td(n,Yp(e,n.schema),t)&&zp(n,r)});var Jd=Object.freeze({__proto__:null,liftEmptyBlock:()=>({state:e,dispatch:t})=>Rp(e,t)});var Kd=Object.freeze({__proto__:null,liftListItem:e=>({state:t,dispatch:n})=>Kp(Yp(e,t.schema))(t,n)});var Gd=Object.freeze({__proto__:null,newlineInCode:()=>({state:e,dispatch:t})=>Pp(e,t)});function Yd(e,t){const n="string"==typeof t?[t]:t;return Object.keys(e).reduce(((t,r)=>(n.includes(r)||(t[r]=e[r]),t)),{})}var Xd=Object.freeze({__proto__:null,resetAttributes:(e,t)=>({tr:n,state:r,dispatch:o})=>{let i=null,s=null;const a=Gp("string"==typeof e?e:e.name,r.schema);return!!a&&("node"===a&&(i=Yp(e,r.schema)),"mark"===a&&(s=Xp(e,r.schema)),o&&n.selection.ranges.forEach((e=>{r.doc.nodesBetween(e.$from.pos,e.$to.pos,((e,r)=>{i&&i===e.type&&n.setNodeMarkup(r,void 0,Yd(e.attrs,t)),s&&e.marks.length&&e.marks.forEach((o=>{s===o.type&&n.addMark(r,r+e.nodeSize,s.create(Yd(o.attrs,t)))}))}))})),!0)}});var Zd=Object.freeze({__proto__:null,scrollIntoView:()=>({tr:e,dispatch:t})=>(t&&e.scrollIntoView(),!0)});var Qd=Object.freeze({__proto__:null,selectAll:()=>({state:e,dispatch:t})=>Lp(e,t)});var eh=Object.freeze({__proto__:null,selectNodeBackward:()=>({state:e,dispatch:t})=>Op(e,t)});var th=Object.freeze({__proto__:null,selectNodeForward:()=>({state:e,dispatch:t})=>Ap(e,t)});var nh=Object.freeze({__proto__:null,selectParentNode:()=>({state:e,dispatch:t})=>function(e,t){var n,r=e.selection,o=r.$from,i=r.to,s=o.sharedDepth(i);return 0!=s&&(n=o.before(s),t&&t(e.tr.setSelection(Ya.create(e.doc,n))),!0)}(e,t)});var rh=Object.freeze({__proto__:null,setContent:(e,t=!1,n={})=>({tr:r,editor:o,dispatch:i})=>{const{doc:s}=r,a=id(e,o.schema,n),c=Ka.create(s,0,s.content.size);return i&&r.setSelection(c).replaceSelectionWith(a,!1).setMeta("preventUpdate",!t),!0}});var oh=Object.freeze({__proto__:null,setMark:(e,t={})=>({tr:n,state:r,dispatch:o})=>{const{selection:i}=n,{empty:s,ranges:c}=i,l=Xp(e,r.schema);if(o)if(s){const e=Zp(r,l);n.addStoredMark(l.create(a(a({},e),t)))}else c.forEach((e=>{const o=e.$from.pos,i=e.$to.pos;r.doc.nodesBetween(o,i,((e,r)=>{const s=Math.max(r,o),c=Math.min(r+e.nodeSize,i);e.marks.find((e=>e.type===l))?e.marks.forEach((e=>{l===e.type&&n.addMark(s,c,l.create(a(a({},e.attrs),t)))})):n.addMark(s,c,l.create(t))}))}));return!0}});var ih=Object.freeze({__proto__:null,setMeta:(e,t)=>({tr:n})=>(n.setMeta(e,t),!0)});var sh=Object.freeze({__proto__:null,setNode:(e,t={})=>({state:n,dispatch:r})=>{const o=Yp(e,n.schema);return(i=o,s=t,function(e,t){var n=e.selection,r=n.from,o=n.to,a=!1;return e.doc.nodesBetween(r,o,(function(t,n){if(a)return!1;if(t.isTextblock&&!t.hasMarkup(i,s))if(t.type==i)a=!0;else{var r=e.doc.resolve(n),o=r.index();a=r.parent.canReplaceWith(o,o+1,i)}})),!!a&&(t&&t(e.tr.setBlockType(r,o,i,s).scrollIntoView()),!0)})(n,r);var i,s}});var ah=Object.freeze({__proto__:null,setNodeSelection:e=>({tr:t,dispatch:n})=>{if(n){const{doc:n}=t,r=Ua.atStart(n).from,o=Ua.atEnd(n).to,i=jd(e,r,o),s=Ya.create(n,i);t.setSelection(s)}return!0}});var ch=Object.freeze({__proto__:null,setTextSelection:e=>({tr:t,dispatch:n})=>{if(n){const{doc:n}=t,{from:r,to:o}="number"==typeof e?{from:e,to:e}:e,i=Ua.atStart(n).from,s=Ua.atEnd(n).to,a=jd(r,i,s),c=jd(o,i,s),l=Ka.create(n,a,c);t.setSelection(l)}return!0}});var lh=Object.freeze({__proto__:null,sinkListItem:e=>({state:t,dispatch:n})=>{const r=Yp(e,t.schema);return(o=r,function(e,t){var n=e.selection,r=n.$from,i=n.$to,s=r.blockRange(i,(function(e){return e.childCount&&e.firstChild.type==o}));if(!s)return!1;var a=s.startIndex;if(0==a)return!1;var c=s.parent,l=c.child(a-1);if(l.type!=o)return!1;if(t){var u=l.lastChild&&l.lastChild.type==c.type,p=Gi.from(u?o.create():null),d=new ns(Gi.from(o.create(null,Gi.from(c.type.create(null,p)))),u?3:1,0),h=s.start,f=s.end;t(e.tr.step(new ka(h-(u?3:1),f,h,f,d,1,!0)).scrollIntoView())}return!0})(t,n);var o}});function uh(e,t,n){return Object.fromEntries(Object.entries(n).filter((([n])=>{const r=e.find((e=>e.type===t&&e.name===n));return!!r&&r.attribute.keepOnSplit})))}function ph(e,t){const n=e.storedMarks||e.selection.$to.parentOffset&&e.selection.$from.marks();if(n){const r=n.filter((e=>null==t?void 0:t.includes(e.type.name)));e.tr.ensureMarks(r)}}var dh=Object.freeze({__proto__:null,splitBlock:({keepMarks:e=!0}={})=>({tr:t,state:n,dispatch:r,editor:o})=>{const{selection:i,doc:s}=t,{$from:a,$to:c}=i,l=uh(o.extensionManager.attributes,a.node().type.name,a.node().attrs);if(i instanceof Ya&&i.node.isBlock)return!(!a.parentOffset||!Ta(s,a.pos))&&(r&&(e&&ph(n,o.extensionManager.splittableMarks),t.split(a.pos).scrollIntoView()),!0);if(!a.parent.isBlock)return!1;if(r){const r=c.parentOffset===c.parent.content.size;i instanceof Ka&&t.deleteSelection();const s=0===a.depth?void 0:function(e){for(let t=0;t<e.edgeCount;t+=1){const{type:n}=e.edge(t);if(n.isTextblock&&!n.hasRequiredAttrs())return n}return null}(a.node(-1).contentMatchAt(a.indexAfter(-1)));let u=r&&s?[{type:s,attrs:l}]:void 0,p=Ta(t.doc,t.mapping.map(a.pos),1,u);if(u||p||!Ta(t.doc,t.mapping.map(a.pos),1,s?[{type:s}]:void 0)||(p=!0,u=s?[{type:s,attrs:l}]:void 0),p&&(t.split(t.mapping.map(a.pos),1,u),s&&!r&&!a.parentOffset&&a.parent.type!==s)){const e=t.mapping.map(a.before()),n=t.doc.resolve(e);a.node(-1).canReplaceWith(n.index(),n.index()+1,s)&&t.setNodeMarkup(t.mapping.map(a.before()),s)}e&&ph(n,o.extensionManager.splittableMarks),t.scrollIntoView()}return!0}});var hh=Object.freeze({__proto__:null,splitListItem:e=>({tr:t,state:n,dispatch:r,editor:o})=>{var i;const s=Yp(e,n.schema),{$from:a,$to:c}=n.selection,l=n.selection.node;if(l&&l.isBlock||a.depth<2||!a.sameParent(c))return!1;const u=a.node(-1);if(u.type!==s)return!1;const p=o.extensionManager.attributes;if(0===a.parent.content.size&&a.node(-1).childCount===a.indexAfter(-1)){if(2===a.depth||a.node(-3).type!==s||a.index(-2)!==a.node(-2).childCount-1)return!1;if(r){let e=Gi.empty;const n=a.index(-1)?1:a.index(-2)?2:3;for(let t=a.depth-n;t>=a.depth-3;t-=1)e=Gi.from(a.node(t).copy(e));const r=a.indexAfter(-1)<a.node(-2).childCount?1:a.indexAfter(-2)<a.node(-3).childCount?2:3,o=uh(p,a.node().type.name,a.node().attrs),c=(null===(i=s.contentMatch.defaultType)||void 0===i?void 0:i.createAndFill(o))||void 0;e=e.append(Gi.from(s.createAndFill(null,c)||void 0));const l=a.before(a.depth-(n-1));t.replace(l,a.after(-r),new ns(e,4-n,0));let u=-1;t.doc.nodesBetween(l,t.doc.content.size,((e,t)=>{if(u>-1)return!1;e.isTextblock&&0===e.content.size&&(u=t+1)})),u>-1&&t.setSelection(Ka.near(t.doc.resolve(u))),t.scrollIntoView()}return!0}const d=c.pos===a.end()?u.contentMatchAt(0).defaultType:null,h=uh(p,u.type.name,u.attrs),f=uh(p,a.node().type.name,a.node().attrs);t.delete(a.pos,c.pos);const m=d?[{type:s,attrs:h},{type:d,attrs:f}]:[{type:s,attrs:h}];return!!Ta(t.doc,a.pos,2)&&(r&&t.split(a.pos,2,m).scrollIntoView(),!0)}});function fh(e,t){const{nodeExtensions:n}=cd(t),r=n.find((t=>t.name===e));if(!r)return!1;const o=hd(ad(r,"group",{name:r.name,options:r.options}));return"string"==typeof o&&o.split(" ").includes("list")}var mh=Object.freeze({__proto__:null,toggleList:(e,t)=>({editor:n,tr:r,state:o,dispatch:i,chain:s,commands:a,can:c})=>{const{extensions:l}=n.extensionManager,u=Yp(e,o.schema),p=Yp(t,o.schema),{selection:d}=o,{$from:h,$to:f}=d,m=h.blockRange(f);if(!m)return!1;const g=(v=e=>fh(e.type.name,l),e=>function(e,t){for(let n=e.depth;n>0;n-=1){const r=e.node(n);if(t(r))return{pos:n>0?e.before(n):0,start:e.start(n),depth:n,node:r}}}(e.$from,v))(d);var v;if(m.depth>=1&&g&&m.depth-g.depth<=1){if(g.node.type===u)return a.liftListItem(p);if(fh(g.node.type.name,l)&&u.validContent(g.node.content)&&i)return r.setNodeMarkup(g.pos,u),!0}return c().wrapInList(u)?a.wrapInList(u):s().clearNodes().wrapInList(u).run()}});var gh=Object.freeze({__proto__:null,toggleMark:(e,t={})=>({state:n,commands:r})=>{const o=Xp(e,n.schema);return nd(n,o,t)?r.unsetMark(o):r.setMark(o,t)}});var vh=Object.freeze({__proto__:null,toggleNode:(e,t,n={})=>({state:r,commands:o})=>{const i=Yp(e,r.schema),s=Yp(t,r.schema);return td(r,i,n)?o.setNode(s):o.setNode(i,n)}});var yh=Object.freeze({__proto__:null,toggleWrap:(e,t={})=>({state:n,dispatch:r})=>{const o=Yp(e,n.schema);return td(n,o,t)?zp(n,r):$p(o,t)(n,r)}});var _h=Object.freeze({__proto__:null,undoInputRule:()=>({state:e,dispatch:t})=>function(e,t){for(var n=e.plugins,r=0;r<n.length;r++){var o=n[r],i=void 0;if(o.spec.isInputRules&&(i=o.getState(e))){if(t){for(var s=e.tr,a=i.transform,c=a.steps.length-1;c>=0;c--)s.step(a.steps[c].invert(a.docs[c]));if(i.text){var l=s.doc.resolve(i.from).marks();s.replaceWith(i.from,i.to,e.schema.text(i.text,l))}else s.delete(i.from,i.to);t(s)}return!0}}return!1}(e,t)});var bh=Object.freeze({__proto__:null,unsetAllMarks:()=>({tr:e,state:t,dispatch:n})=>{const{selection:r}=e,{empty:o,ranges:i}=r;return o||n&&Object.entries(t.schema.marks).forEach((([,t])=>{i.forEach((n=>{e.removeMark(n.$from.pos,n.$to.pos,t)}))})),!0}});var wh=Object.freeze({__proto__:null,unsetMark:e=>({tr:t,state:n,dispatch:r})=>{const{selection:o}=t,i=Xp(e,n.schema),{$from:s,empty:a,ranges:c}=o;if(r){if(a){let{from:e,to:n}=o;const r=Pd(s,i);r&&(e=r.from,n=r.to),t.removeMark(e,n,i)}else c.forEach((e=>{t.removeMark(e.$from.pos,e.$to.pos,i)}));t.removeStoredMark(i)}return!0}});var kh=Object.freeze({__proto__:null,updateAttributes:(e,t={})=>({tr:n,state:r,dispatch:o})=>{let i=null,s=null;const c=Gp("string"==typeof e?e:e.name,r.schema);return!!c&&("node"===c&&(i=Yp(e,r.schema)),"mark"===c&&(s=Xp(e,r.schema)),o&&n.selection.ranges.forEach((e=>{const o=e.$from.pos,c=e.$to.pos;r.doc.nodesBetween(o,c,((e,r)=>{i&&i===e.type&&n.setNodeMarkup(r,void 0,a(a({},e.attrs),t)),s&&e.marks.length&&e.marks.forEach((i=>{if(s===i.type){const l=Math.max(r,o),u=Math.min(r+e.nodeSize,c);n.addMark(l,u,s.create(a(a({},i.attrs),t)))}}))}))})),!0)}});var xh=Object.freeze({__proto__:null,wrapIn:(e,t={})=>({state:n,dispatch:r})=>{const o=Yp(e,n.schema);return!td(n,o,t)&&$p(o,t)(n,r)}});var Sh=Object.freeze({__proto__:null,wrapInList:(e,t={})=>({state:n,dispatch:r})=>Jp(Yp(e,n.schema),t)(n,r)});const Mh=_d.create({name:"commands",addCommands:()=>a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a(a({},wd),kd),xd),Sd),Md),Ed),Od),Td),Cd),Ad),Id),Dd),Ld),Bd),$d),Hd),Fd),Vd),Ud),Wd),Jd),Kd),Gd),Xd),Zd),Qd),eh),th),nh),rh),oh),ih),sh),ah),ch),lh),dh),hh),mh),gh),vh),yh),_h),bh),wh),kh),xh),Sh)}),Eh=_d.create({name:"editable",addProseMirrorPlugins(){return[new pc({key:new fc("editable"),props:{editable:()=>this.editor.options.editable}})]}}),Oh=_d.create({name:"focusEvents",addProseMirrorPlugins(){const{editor:e}=this;return[new pc({key:new fc("focusEvents"),props:{attributes:{tabindex:"0"},handleDOMEvents:{focus:(t,n)=>{e.isFocused=!0;const r=e.state.tr.setMeta("focus",{event:n}).setMeta("addToHistory",!1);return t.dispatch(r),!1},blur:(t,n)=>{e.isFocused=!1;const r=e.state.tr.setMeta("blur",{event:n}).setMeta("addToHistory",!1);return t.dispatch(r),!1}}}})]}}),Th=_d.create({name:"keymap",addKeyboardShortcuts(){const e=()=>this.editor.commands.first((({commands:e})=>[()=>e.undoInputRule(),()=>e.deleteSelection(),()=>e.joinBackward(),()=>e.selectNodeBackward()])),t=()=>this.editor.commands.first((({commands:e})=>[()=>e.deleteSelection(),()=>e.joinForward(),()=>e.selectNodeForward()]));return{Enter:()=>this.editor.commands.first((({commands:e})=>[()=>e.newlineInCode(),()=>e.createParagraphNear(),()=>e.liftEmptyBlock(),()=>e.splitBlock()])),"Mod-Enter":()=>this.editor.commands.exitCode(),Backspace:()=>e(),"Mod-Backspace":()=>e(),Delete:()=>t(),"Mod-Delete":()=>t()}}});var Ch=Object.freeze({__proto__:null,ClipboardTextSerializer:bd,Commands:Mh,Editable:Eh,FocusEvents:Oh,Keymap:Th});class Ah extends class{constructor(){this.callbacks={}}on(e,t){return this.callbacks[e]||(this.callbacks[e]=[]),this.callbacks[e].push(t),this}emit(e,...t){const n=this.callbacks[e];return n&&n.forEach((e=>e.apply(this,t))),this}off(e,t){const n=this.callbacks[e];return n&&(t?this.callbacks[e]=n.filter((e=>e!==t)):delete this.callbacks[e]),this}removeAllListeners(){this.callbacks={}}}{constructor(e={}){super(),this.isFocused=!1,this.options={element:document.createElement("div"),content:"",injectCSS:!0,extensions:[],autofocus:!1,editable:!0,editorProps:{},parseOptions:{},enableInputRules:!0,enablePasteRules:!0,onBeforeCreate:()=>null,onCreate:()=>null,onUpdate:()=>null,onSelectionUpdate:()=>null,onTransaction:()=>null,onFocus:()=>null,onBlur:()=>null,onDestroy:()=>null},this.isCapturingTransaction=!1,this.capturedTransaction=null,this.setOptions(e),this.createExtensionManager(),this.createCommandManager(),this.createSchema(),this.on("beforeCreate",this.options.onBeforeCreate),this.emit("beforeCreate",{editor:this}),this.createView(),this.injectCSS(),this.on("create",this.options.onCreate),this.on("update",this.options.onUpdate),this.on("selectionUpdate",this.options.onSelectionUpdate),this.on("transaction",this.options.onTransaction),this.on("focus",this.options.onFocus),this.on("blur",this.options.onBlur),this.on("destroy",this.options.onDestroy),window.setTimeout((()=>{this.isDestroyed||(this.commands.focus(this.options.autofocus),this.emit("create",{editor:this}))}),0)}get commands(){return this.commandManager.createCommands()}chain(){return this.commandManager.createChain()}can(){return this.commandManager.createCan()}injectCSS(){this.options.injectCSS&&document&&(this.css=function(e){const t=document.querySelector("style[data-tiptap-style]");if(null!==t)return t;const n=document.createElement("style");return n.setAttribute("data-tiptap-style",""),n.innerHTML=e,document.getElementsByTagName("head")[0].appendChild(n),n}('.ProseMirror {\n  position: relative;\n}\n\n.ProseMirror {\n  word-wrap: break-word;\n  white-space: pre-wrap;\n  -webkit-font-variant-ligatures: none;\n  font-variant-ligatures: none;\n}\n\n.ProseMirror [contenteditable="false"] {\n  white-space: normal;\n}\n\n.ProseMirror [contenteditable="false"] [contenteditable="true"] {\n  white-space: pre-wrap;\n}\n\n.ProseMirror pre {\n  white-space: pre-wrap;\n}\n\n.ProseMirror-gapcursor {\n  display: none;\n  pointer-events: none;\n  position: absolute;\n}\n\n.ProseMirror-gapcursor:after {\n  content: "";\n  display: block;\n  position: absolute;\n  top: -2px;\n  width: 20px;\n  border-top: 1px solid black;\n  animation: ProseMirror-cursor-blink 1.1s steps(2, start) infinite;\n}\n\n@keyframes ProseMirror-cursor-blink {\n  to {\n    visibility: hidden;\n  }\n}\n\n.ProseMirror-hideselection *::selection {\n  background: transparent;\n}\n\n.ProseMirror-hideselection *::-moz-selection {\n  background: transparent;\n}\n\n.ProseMirror-hideselection * {\n  caret-color: transparent;\n}\n\n.ProseMirror-focused .ProseMirror-gapcursor {\n  display: block;\n}\n\n.tippy-box[data-animation=fade][data-state=hidden] {\n  opacity: 0\n}'))}setOptions(e={}){this.options=a(a({},this.options),e),this.view&&this.state&&!this.isDestroyed&&(this.options.editorProps&&this.view.setProps(this.options.editorProps),this.view.updateState(this.state))}setEditable(e){this.setOptions({editable:e})}get isEditable(){return this.options.editable&&this.view&&this.view.editable}get state(){return this.view.state}registerPlugin(e,t){const n="function"==typeof t?t(e,this.state.plugins):[...this.state.plugins,e],r=this.state.reconfigure({plugins:n});this.view.updateState(r)}unregisterPlugin(e){if(this.isDestroyed)return;const t="string"==typeof e?`${e}$`:e.key,n=this.state.reconfigure({plugins:this.state.plugins.filter((e=>!e.key.startsWith(t)))});this.view.updateState(n)}createExtensionManager(){const e=[...Object.entries(Ch).map((([,e])=>e)),...this.options.extensions].filter((e=>["extension","node","mark"].includes(null==e?void 0:e.type)));this.extensionManager=new gd(e,this)}createCommandManager(){this.commandManager=new sd(this,this.extensionManager.commands)}createSchema(){this.schema=this.extensionManager.schema}createView(){this.view=new ep(this.options.element,c(a({},this.options.editorProps),{dispatchTransaction:this.dispatchTransaction.bind(this),state:ac.create({doc:id(this.options.content,this.schema,this.options.parseOptions)})}));const e=this.state.reconfigure({plugins:this.extensionManager.plugins});this.view.updateState(e),this.createNodeViews();this.view.dom.editor=this}createNodeViews(){this.view.setProps({nodeViews:this.extensionManager.nodeViews})}captureTransaction(e){this.isCapturingTransaction=!0,e(),this.isCapturingTransaction=!1;const t=this.capturedTransaction;return this.capturedTransaction=null,t}dispatchTransaction(e){if(this.isCapturingTransaction)return this.capturedTransaction?void e.steps.forEach((e=>{var t;return null===(t=this.capturedTransaction)||void 0===t?void 0:t.step(e)})):void(this.capturedTransaction=e);const t=this.state.apply(e),n=!this.state.selection.eq(t.selection);this.view.updateState(t),this.emit("transaction",{editor:this,transaction:e}),n&&this.emit("selectionUpdate",{editor:this,transaction:e});const r=e.getMeta("focus"),o=e.getMeta("blur");r&&this.emit("focus",{editor:this,event:r.event,transaction:e}),o&&this.emit("blur",{editor:this,event:o.event,transaction:e}),e.docChanged&&!e.getMeta("preventUpdate")&&this.emit("update",{editor:this,transaction:e})}getAttributes(e){return Qp(this.state,e)}isActive(e,t){const n="string"==typeof e?e:null,r="string"==typeof e?t:e;return function(e,t,n={}){if(!t)return td(e,null,n)||nd(e,null,n);const r=Gp(t,e.schema);return"node"===r?td(e,t,n):"mark"===r&&nd(e,t,n)}(this.state,n,r)}getJSON(){return this.state.doc.toJSON()}getHTML(){return function(e,t){const n=sa.fromSchema(t).serializeFragment(e.content),r=document.implementation.createHTMLDocument().createElement("div");return r.appendChild(n),r.innerHTML}(this.state.doc,this.schema)}get isEmpty(){return function(e){var t;const n=null===(t=e.type.createAndFill())||void 0===t?void 0:t.toJSON(),r=e.toJSON();return JSON.stringify(n)===JSON.stringify(r)}(this.state.doc)}getCharacterCount(){return this.state.doc.content.size-2}destroy(){var e;this.emit("destroy"),this.view&&this.view.destroy(),this.removeAllListeners(),(e=this.css)&&e.parentNode&&e.parentNode.removeChild(e)}get isDestroyed(){var e;return!(null===(e=this.view)||void 0===e?void 0:e.docView)}}class Nh{constructor(e={}){this.type="node",this.name="node",this.parent=null,this.child=null,this.config={name:this.name,defaultOptions:{}},this.config=a(a({},this.config),e),this.name=this.config.name,this.options=this.config.defaultOptions}static create(e={}){return new Nh(e)}configure(e={}){const t=this.extend();return t.options=yd(this.options,e),t}extend(e={}){const t=new Nh(e);return t.parent=this,this.child=t,t.name=e.name?e.name:t.parent.name,t.options=e.defaultOptions?e.defaultOptions:t.parent.options,t}}class zh{constructor(e={}){this.type="mark",this.name="mark",this.parent=null,this.child=null,this.config={name:this.name,defaultOptions:{}},this.config=a(a({},this.config),e),this.name=this.config.name,this.options=this.config.defaultOptions}static create(e={}){return new zh(e)}configure(e={}){const t=this.extend();return t.options=yd(this.options,e),t}extend(e={}){const t=new zh(e);return t.parent=this,this.child=t,t.name=e.name?e.name:t.parent.name,t.options=e.defaultOptions?e.defaultOptions:t.parent.options,t}}function Ph(e,t,n){return new bp(e,((e,r,o,i)=>{const s=n instanceof Function?n(r):n,{tr:a}=e,c=r[r.length-1],l=r[0];let u=i;if(c){const n=l.search(/\S/),r=o+l.indexOf(c),p=r+c.length;if(function(e,t,n){let r=[];return n.doc.nodesBetween(e,t,((e,t)=>{r=[...r,...e.marks.map((n=>({from:t,to:t+e.nodeSize,mark:n})))]})),r}(o,i,e).filter((e=>{const{excluded:n}=e.mark.type;return n.find((e=>e.name===t.name))})).filter((e=>e.to>r)).length)return null;p<i&&a.delete(p,i),r>o&&a.delete(o+n,r),u=o+n+c.length,a.addMark(o+n,u,t.create(s)),a.removeStoredMark(t)}return a}))}function Ih(e,t,n){const r=(o,i)=>{const s=[];return o.forEach((o=>{if(o.isText&&o.text){const{text:r}=o;let a,c=0;for(;null!==(a=e.exec(r));){const e=Math.max(a.length-2,0),r=Math.max(a.length-1,0);if(null==i?void 0:i.type.allowsMarkType(t)){const i=a.index+a[0].indexOf(a[e]),l=i+a[e].length,u=i+a[e].lastIndexOf(a[r]),p=u+a[r].length,d=n instanceof Function?n(a):n;if(!d&&void 0!==d)continue;i>0&&s.push(o.cut(c,i)),s.push(o.cut(u,p).mark(t.create(d).addToSet(o.marks))),c=l}}c<r.length&&s.push(o.cut(c))}else s.push(o.copy(r(o.content,o)))})),Gi.fromArray(s)};return new pc({key:new fc("markPasteRule"),props:{transformPasted:e=>new ns(r(e.content),e.openStart,e.openEnd)}})}const Dh=/^\s*>\s$/gm,jh=Nh.create({name:"blockquote",defaultOptions:{HTMLAttributes:{}},content:"block*",group:"block",defining:!0,parseHTML:()=>[{tag:"blockquote"}],renderHTML({HTMLAttributes:e}){return["blockquote",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({setBlockquote:()=>({commands:e})=>e.wrapIn("blockquote"),toggleBlockquote:()=>({commands:e})=>e.toggleWrap("blockquote"),unsetBlockquote:()=>({commands:e})=>e.lift("blockquote")}),addKeyboardShortcuts(){return{"Mod-Shift-b":()=>this.editor.commands.toggleBlockquote()}},addInputRules(){return[kp(Dh,this.type)]}}),Rh=/(?:^|\s)((?:\*\*)((?:[^*]+))(?:\*\*))$/gm,Lh=/(?:^|\s)((?:\*\*)((?:[^*]+))(?:\*\*))/gm,Bh=/(?:^|\s)((?:__)((?:[^__]+))(?:__))$/gm,$h=/(?:^|\s)((?:__)((?:[^__]+))(?:__))/gm,Hh=zh.create({name:"bold",defaultOptions:{HTMLAttributes:{}},parseHTML:()=>[{tag:"strong"},{tag:"b",getAttrs:e=>"normal"!==e.style.fontWeight&&null},{style:"font-weight",getAttrs:e=>/^(bold(er)?|[5-9]\d{2,})$/.test(e)&&null}],renderHTML({HTMLAttributes:e}){return["strong",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({setBold:()=>({commands:e})=>e.setMark("bold"),toggleBold:()=>({commands:e})=>e.toggleMark("bold"),unsetBold:()=>({commands:e})=>e.unsetMark("bold")}),addKeyboardShortcuts(){return{"Mod-b":()=>this.editor.commands.toggleBold()}},addInputRules(){return[Ph(Rh,this.type),Ph(Bh,this.type)]},addPasteRules(){return[Ih(Lh,this.type),Ih($h,this.type)]}}),Fh=/^\s*([-+*])\s$/,Vh=Nh.create({name:"bulletList",defaultOptions:{HTMLAttributes:{}},group:"block list",content:"listItem+",parseHTML:()=>[{tag:"ul"}],renderHTML({HTMLAttributes:e}){return["ul",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({toggleBulletList:()=>({commands:e})=>e.toggleList("bulletList","listItem")}),addKeyboardShortcuts(){return{"Mod-Shift-8":()=>this.editor.commands.toggleBulletList()}},addInputRules(){return[kp(Fh,this.type)]}}),qh=/(?:^|\s)((?:`)((?:[^`]+))(?:`))$/gm,Uh=/(?:^|\s)((?:`)((?:[^`]+))(?:`))/gm,Wh=zh.create({name:"code",defaultOptions:{HTMLAttributes:{}},excludes:"_",parseHTML:()=>[{tag:"code"}],renderHTML({HTMLAttributes:e}){return["code",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({setCode:()=>({commands:e})=>e.setMark("code"),toggleCode:()=>({commands:e})=>e.toggleMark("code"),unsetCode:()=>({commands:e})=>e.unsetMark("code")}),addKeyboardShortcuts(){return{"Mod-e":()=>this.editor.commands.toggleCode()}},addInputRules(){return[Ph(qh,this.type)]},addPasteRules(){return[Ih(Uh,this.type)]}}),Jh=/^```(?<language>[a-z]*)? $/,Kh=/^~~~(?<language>[a-z]*)? $/,Gh=Nh.create({name:"codeBlock",defaultOptions:{languageClassPrefix:"language-",HTMLAttributes:{}},content:"text*",marks:"",group:"block",code:!0,defining:!0,addAttributes(){return{language:{default:null,parseHTML:e=>{var t;const n=null===(t=e.firstElementChild)||void 0===t?void 0:t.getAttribute("class");if(!n)return null;const r=new RegExp(`^(${this.options.languageClassPrefix})`);return{language:n.replace(r,"")}},renderHTML:e=>e.language?{class:this.options.languageClassPrefix+e.language}:null}}},parseHTML:()=>[{tag:"pre",preserveWhitespace:"full"}],renderHTML({HTMLAttributes:e}){return["pre",this.options.HTMLAttributes,["code",e,0]]},addCommands:()=>({setCodeBlock:e=>({commands:t})=>t.setNode("codeBlock",e),toggleCodeBlock:e=>({commands:t})=>t.toggleNode("codeBlock","paragraph",e)}),addKeyboardShortcuts(){return{"Mod-Alt-c":()=>this.editor.commands.toggleCodeBlock(),Backspace:()=>{const{empty:e,$anchor:t}=this.editor.state.selection,n=1===t.pos;return!(!e||t.parent.type.name!==this.name)&&(!(!n&&t.parent.textContent.length)&&this.editor.commands.clearNodes())}}},addInputRules(){return[xp(Jh,this.type,(({groups:e})=>e)),xp(Kh,this.type,(({groups:e})=>e))]}}),Yh=Nh.create({name:"doc",topNode:!0,content:"block+"});var Xh=function(e,t){var n=this;this.editorView=e,this.width=t.width||1,this.color=t.color||"black",this.class=t.class,this.cursorPos=null,this.element=null,this.timeout=null,this.handlers=["dragover","dragend","drop","dragleave"].map((function(t){var r=function(e){return n[t](e)};return e.dom.addEventListener(t,r),{name:t,handler:r}}))};Xh.prototype.destroy=function(){var e=this;this.handlers.forEach((function(t){var n=t.name,r=t.handler;return e.editorView.dom.removeEventListener(n,r)}))},Xh.prototype.update=function(e,t){null!=this.cursorPos&&t.doc!=e.state.doc&&(this.cursorPos>e.state.doc.content.size?this.setCursor(null):this.updateOverlay())},Xh.prototype.setCursor=function(e){e!=this.cursorPos&&(this.cursorPos=e,null==e?(this.element.parentNode.removeChild(this.element),this.element=null):this.updateOverlay())},Xh.prototype.updateOverlay=function(){var e,t=this.editorView.state.doc.resolve(this.cursorPos);if(!t.parent.inlineContent){var n=t.nodeBefore,r=t.nodeAfter;if(n||r){var o=this.editorView.nodeDOM(this.cursorPos-(n?n.nodeSize:0)).getBoundingClientRect(),i=n?o.bottom:o.top;n&&r&&(i=(i+this.editorView.nodeDOM(this.cursorPos).getBoundingClientRect().top)/2),e={left:o.left,right:o.right,top:i-this.width/2,bottom:i+this.width/2}}}if(!e){var s=this.editorView.coordsAtPos(this.cursorPos);e={left:s.left-this.width/2,right:s.left+this.width/2,top:s.top,bottom:s.bottom}}var a,c,l=this.editorView.dom.offsetParent;if(this.element||(this.element=l.appendChild(document.createElement("div")),this.class&&(this.element.className=this.class),this.element.style.cssText="position: absolute; z-index: 50; pointer-events: none; background-color: "+this.color),!l||l==document.body&&"static"==getComputedStyle(l).position)a=-pageXOffset,c=-pageYOffset;else{var u=l.getBoundingClientRect();a=u.left-l.scrollLeft,c=u.top-l.scrollTop}this.element.style.left=e.left-a+"px",this.element.style.top=e.top-c+"px",this.element.style.width=e.right-e.left+"px",this.element.style.height=e.bottom-e.top+"px"},Xh.prototype.scheduleRemoval=function(e){var t=this;clearTimeout(this.timeout),this.timeout=setTimeout((function(){return t.setCursor(null)}),e)},Xh.prototype.dragover=function(e){if(this.editorView.editable){var t=this.editorView.posAtCoords({left:e.clientX,top:e.clientY});if(t){var n=t.pos;if(this.editorView.dragging&&this.editorView.dragging.slice&&null==(n=Aa(this.editorView.state.doc,n,this.editorView.dragging.slice)))return this.setCursor(null);this.setCursor(n),this.scheduleRemoval(5e3)}}},Xh.prototype.dragend=function(){this.scheduleRemoval(20)},Xh.prototype.drop=function(){this.scheduleRemoval(20)},Xh.prototype.dragleave=function(e){e.target!=this.editorView.dom&&this.editorView.dom.contains(e.relatedTarget)||this.setCursor(null)};const Zh=_d.create({name:"dropCursor",defaultOptions:{color:"currentColor",width:1,class:null},addProseMirrorPlugins(){return[(e=this.options,void 0===e&&(e={}),new pc({view:function(t){return new Xh(t,e)}}))];var e}});var Qh=function(e){function t(t){e.call(this,t,t)}return e&&(t.__proto__=e),t.prototype=Object.create(e&&e.prototype),t.prototype.constructor=t,t.prototype.map=function(n,r){var o=n.resolve(r.map(this.head));return t.valid(o)?new t(o):e.near(o)},t.prototype.content=function(){return ns.empty},t.prototype.eq=function(e){return e instanceof t&&e.head==this.head},t.prototype.toJSON=function(){return{type:"gapcursor",pos:this.head}},t.fromJSON=function(e,n){if("number"!=typeof n.pos)throw new RangeError("Invalid input for GapCursor.fromJSON");return new t(e.resolve(n.pos))},t.prototype.getBookmark=function(){return new ef(this.anchor)},t.valid=function(e){var t=e.parent;if(t.isTextblock||!function(e){for(var t=e.depth;t>=0;t--){var n=e.index(t);if(0!=n)for(var r=e.node(t).child(n-1);;r=r.lastChild){if(0==r.childCount&&!r.inlineContent||r.isAtom||r.type.spec.isolating)return!0;if(r.inlineContent)return!1}}return!0}(e)||!function(e){for(var t=e.depth;t>=0;t--){var n=e.indexAfter(t),r=e.node(t);if(n!=r.childCount)for(var o=r.child(n);;o=o.firstChild){if(0==o.childCount&&!o.inlineContent||o.isAtom||o.type.spec.isolating)return!0;if(o.inlineContent)return!1}}return!0}(e))return!1;var n=t.type.spec.allowGapCursor;if(null!=n)return n;var r=t.contentMatchAt(e.index()).defaultType;return r&&r.isTextblock},t.findFrom=function(e,n,r){e:for(;;){if(!r&&t.valid(e))return e;for(var o=e.pos,i=null,s=e.depth;;s--){var a=e.node(s);if(n>0?e.indexAfter(s)<a.childCount:e.index(s)>0){i=a.child(n>0?e.indexAfter(s):e.index(s)-1);break}if(0==s)return null;o+=n;var c=e.doc.resolve(o);if(t.valid(c))return c}for(;;){var l=n>0?i.firstChild:i.lastChild;if(!l){if(i.isAtom&&!i.isText&&!Ya.isSelectable(i)){e=e.doc.resolve(o+i.nodeSize*n),r=!1;continue e}break}i=l,o+=n;var u=e.doc.resolve(o);if(t.valid(u))return u}return null}},t}(Ua);Qh.prototype.visible=!1,Ua.jsonID("gapcursor",Qh);var ef=function(e){this.pos=e};ef.prototype.map=function(e){return new ef(e.map(this.pos))},ef.prototype.resolve=function(e){var t=e.resolve(this.pos);return Qh.valid(t)?new Qh(t):Ua.near(t)};var tf=_p({ArrowLeft:nf("horiz",-1),ArrowRight:nf("horiz",1),ArrowUp:nf("vert",-1),ArrowDown:nf("vert",1)});function nf(e,t){var n="vert"==e?t>0?"down":"up":t>0?"right":"left";return function(e,r,o){var i=e.selection,s=t>0?i.$to:i.$from,a=i.empty;if(i instanceof Ka){if(!o.endOfTextblock(n)||0==s.depth)return!1;a=!1,s=e.doc.resolve(t>0?s.after():s.before())}var c=Qh.findFrom(s,t,a);return!!c&&(r&&r(e.tr.setSelection(new Qh(c))),!0)}}function rf(e,t,n){if(!e.editable)return!1;var r=e.state.doc.resolve(t);if(!Qh.valid(r))return!1;var o=e.posAtCoords({left:n.clientX,top:n.clientY}).inside;return!(o>-1&&Ya.isSelectable(e.state.doc.nodeAt(o)))&&(e.dispatch(e.state.tr.setSelection(new Qh(r))),!0)}function of(e){if(!(e.selection instanceof Qh))return null;var t=document.createElement("div");return t.className="ProseMirror-gapcursor",Vu.create(e.doc,[Bu.widget(e.selection.head,t,{key:"gapcursor"})])}const sf=_d.create({name:"gapCursor",addProseMirrorPlugins:()=>[new pc({props:{decorations:of,createSelectionBetween:function(e,t,n){if(t.pos==n.pos&&Qh.valid(n))return new Qh(n)},handleClick:rf,handleKeyDown:tf}})],extendNodeSchema(e){var t;return{allowGapCursor:null!==(t=hd(ad(e,"allowGapCursor",{name:e.name,options:e.options})))&&void 0!==t?t:null}}}),af=Nh.create({name:"hardBreak",defaultOptions:{HTMLAttributes:{}},inline:!0,group:"inline",selectable:!1,parseHTML:()=>[{tag:"br"}],renderHTML({HTMLAttributes:e}){return["br",ud(this.options.HTMLAttributes,e)]},addCommands(){return{setHardBreak:()=>({commands:e})=>e.first([()=>e.exitCode(),()=>e.insertContent({type:this.name})])}},addKeyboardShortcuts(){return{"Mod-Enter":()=>this.editor.commands.setHardBreak(),"Shift-Enter":()=>this.editor.commands.setHardBreak()}}}),cf=Nh.create({name:"heading",defaultOptions:{levels:[1,2,3,4,5,6],HTMLAttributes:{}},content:"inline*",group:"block",defining:!0,addAttributes:()=>({level:{default:1,rendered:!1}}),parseHTML(){return this.options.levels.map((e=>({tag:`h${e}`,attrs:{level:e}})))},renderHTML({node:e,HTMLAttributes:t}){return[`h${this.options.levels.includes(e.attrs.level)?e.attrs.level:this.options.levels[0]}`,ud(this.options.HTMLAttributes,t),0]},addCommands(){return{setHeading:e=>({commands:t})=>!!this.options.levels.includes(e.level)&&t.setNode("heading",e),toggleHeading:e=>({commands:t})=>!!this.options.levels.includes(e.level)&&t.toggleNode("heading","paragraph",e)}},addKeyboardShortcuts(){return this.options.levels.reduce(((e,t)=>a(a({},e),{[`Mod-Alt-${t}`]:()=>this.editor.commands.toggleHeading({level:t})})),{})},addInputRules(){return this.options.levels.map((e=>xp(new RegExp(`^(#{1,${e}})\\s$`),this.type,{level:e})))}});var lf=function(){};lf.prototype.append=function(e){return e.length?(e=lf.from(e),!this.length&&e||e.length<200&&this.leafAppend(e)||this.length<200&&e.leafPrepend(this)||this.appendInner(e)):this},lf.prototype.prepend=function(e){return e.length?lf.from(e).append(this):this},lf.prototype.appendInner=function(e){return new pf(this,e)},lf.prototype.slice=function(e,t){return void 0===e&&(e=0),void 0===t&&(t=this.length),e>=t?lf.empty:this.sliceInner(Math.max(0,e),Math.min(this.length,t))},lf.prototype.get=function(e){if(!(e<0||e>=this.length))return this.getInner(e)},lf.prototype.forEach=function(e,t,n){void 0===t&&(t=0),void 0===n&&(n=this.length),t<=n?this.forEachInner(e,t,n,0):this.forEachInvertedInner(e,t,n,0)},lf.prototype.map=function(e,t,n){void 0===t&&(t=0),void 0===n&&(n=this.length);var r=[];return this.forEach((function(t,n){return r.push(e(t,n))}),t,n),r},lf.from=function(e){return e instanceof lf?e:e&&e.length?new uf(e):lf.empty};var uf=function(e){function t(t){e.call(this),this.values=t}e&&(t.__proto__=e),t.prototype=Object.create(e&&e.prototype),t.prototype.constructor=t;var n={length:{configurable:!0},depth:{configurable:!0}};return t.prototype.flatten=function(){return this.values},t.prototype.sliceInner=function(e,n){return 0==e&&n==this.length?this:new t(this.values.slice(e,n))},t.prototype.getInner=function(e){return this.values[e]},t.prototype.forEachInner=function(e,t,n,r){for(var o=t;o<n;o++)if(!1===e(this.values[o],r+o))return!1},t.prototype.forEachInvertedInner=function(e,t,n,r){for(var o=t-1;o>=n;o--)if(!1===e(this.values[o],r+o))return!1},t.prototype.leafAppend=function(e){if(this.length+e.length<=200)return new t(this.values.concat(e.flatten()))},t.prototype.leafPrepend=function(e){if(this.length+e.length<=200)return new t(e.flatten().concat(this.values))},n.length.get=function(){return this.values.length},n.depth.get=function(){return 0},Object.defineProperties(t.prototype,n),t}(lf);lf.empty=new uf([]);var pf=function(e){function t(t,n){e.call(this),this.left=t,this.right=n,this.length=t.length+n.length,this.depth=Math.max(t.depth,n.depth)+1}return e&&(t.__proto__=e),t.prototype=Object.create(e&&e.prototype),t.prototype.constructor=t,t.prototype.flatten=function(){return this.left.flatten().concat(this.right.flatten())},t.prototype.getInner=function(e){return e<this.left.length?this.left.get(e):this.right.get(e-this.left.length)},t.prototype.forEachInner=function(e,t,n,r){var o=this.left.length;return!(t<o&&!1===this.left.forEachInner(e,t,Math.min(n,o),r))&&(!(n>o&&!1===this.right.forEachInner(e,Math.max(t-o,0),Math.min(this.length,n)-o,r+o))&&void 0)},t.prototype.forEachInvertedInner=function(e,t,n,r){var o=this.left.length;return!(t>o&&!1===this.right.forEachInvertedInner(e,t-o,Math.max(n,o)-o,r+o))&&(!(n<o&&!1===this.left.forEachInvertedInner(e,Math.min(t,o),n,r))&&void 0)},t.prototype.sliceInner=function(e,t){if(0==e&&t==this.length)return this;var n=this.left.length;return t<=n?this.left.slice(e,t):e>=n?this.right.slice(e-n,t-n):this.left.slice(e,n).append(this.right.slice(0,t-n))},t.prototype.leafAppend=function(e){var n=this.right.leafAppend(e);if(n)return new t(this.left,n)},t.prototype.leafPrepend=function(e){var n=this.left.leafPrepend(e);if(n)return new t(n,this.right)},t.prototype.appendInner=function(e){return this.left.depth>=Math.max(this.right.depth,e.depth)+1?new t(this.left,new t(this.right,e)):new t(this,e)},t}(lf),df=lf,hf=function(e,t){this.items=e,this.eventCount=t};hf.prototype.popEvent=function(e,t){var n=this;if(0==this.eventCount)return null;for(var r,o,i=this.items.length;;i--){if(this.items.get(i-1).selection){--i;break}}t&&(r=this.remapping(i,this.items.length),o=r.maps.length);var s,a,c=e.tr,l=[],u=[];return this.items.forEach((function(e,t){if(!e.step)return r||(r=n.remapping(i,t+1),o=r.maps.length),o--,void u.push(e);if(r){u.push(new ff(e.map));var p,d=e.step.map(r.slice(o));d&&c.maybeStep(d).doc&&(p=c.mapping.maps[c.mapping.maps.length-1],l.push(new ff(p,null,null,l.length+u.length))),o--,p&&r.appendMap(p,o)}else c.maybeStep(e.step);return e.selection?(s=r?e.selection.map(r.slice(o)):e.selection,a=new hf(n.items.slice(0,i).append(u.reverse().concat(l)),n.eventCount-1),!1):void 0}),this.items.length,0),{remaining:a,transform:c,selection:s}},hf.prototype.addTransform=function(e,t,n,r){for(var o=[],i=this.eventCount,s=this.items,a=!r&&s.length?s.get(s.length-1):null,c=0;c<e.steps.length;c++){var l,u=e.steps[c].invert(e.docs[c]),p=new ff(e.mapping.maps[c],u,t);(l=a&&a.merge(p))&&(p=l,c?o.pop():s=s.slice(0,s.length-1)),o.push(p),t&&(i++,t=null),r||(a=p)}var d,h,f,m=i-n.depth;return m>gf&&(h=m,(d=s).forEach((function(e,t){if(e.selection&&0==h--)return f=t,!1})),s=d.slice(f),i-=m),new hf(s.append(o),i)},hf.prototype.remapping=function(e,t){var n=new ha;return this.items.forEach((function(t,r){var o=null!=t.mirrorOffset&&r-t.mirrorOffset>=e?n.maps.length-t.mirrorOffset:null;n.appendMap(t.map,o)}),e,t),n},hf.prototype.addMaps=function(e){return 0==this.eventCount?this:new hf(this.items.append(e.map((function(e){return new ff(e)}))),this.eventCount)},hf.prototype.rebased=function(e,t){if(!this.eventCount)return this;var n=[],r=Math.max(0,this.items.length-t),o=e.mapping,i=e.steps.length,s=this.eventCount;this.items.forEach((function(e){e.selection&&s--}),r);var a=t;this.items.forEach((function(t){var r=o.getMirror(--a);if(null!=r){i=Math.min(i,r);var c=o.maps[r];if(t.step){var l=e.steps[r].invert(e.docs[r]),u=t.selection&&t.selection.map(o.slice(a+1,r));u&&s++,n.push(new ff(c,l,u))}else n.push(new ff(c))}}),r);for(var c=[],l=t;l<i;l++)c.push(new ff(o.maps[l]));var u=this.items.slice(0,r).append(c).append(n),p=new hf(u,s);return p.emptyItemCount()>500&&(p=p.compress(this.items.length-n.length)),p},hf.prototype.emptyItemCount=function(){var e=0;return this.items.forEach((function(t){t.step||e++})),e},hf.prototype.compress=function(e){void 0===e&&(e=this.items.length);var t=this.remapping(0,e),n=t.maps.length,r=[],o=0;return this.items.forEach((function(i,s){if(s>=e)r.push(i),i.selection&&o++;else if(i.step){var a=i.step.map(t.slice(n)),c=a&&a.getMap();if(n--,c&&t.appendMap(c,n),a){var l=i.selection&&i.selection.map(t.slice(n));l&&o++;var u,p=new ff(c.invert(),a,l),d=r.length-1;(u=r.length&&r[d].merge(p))?r[d]=u:r.push(p)}}else i.map&&n--}),this.items.length,0),new hf(df.from(r.reverse()),o)},hf.empty=new hf(df.empty,0);var ff=function(e,t,n,r){this.map=e,this.step=t,this.selection=n,this.mirrorOffset=r};ff.prototype.merge=function(e){if(this.step&&e.step&&!e.selection){var t=e.step.merge(this.step);if(t)return new ff(t.getMap().invert(),t,this.selection)}};var mf=function(e,t,n,r){this.done=e,this.undone=t,this.prevRanges=n,this.prevTime=r},gf=20;function vf(e){var t=[];return e.forEach((function(e,n,r,o){return t.push(r,o)})),t}function yf(e,t){if(!e)return null;for(var n=[],r=0;r<e.length;r+=2){var o=t.map(e[r],1),i=t.map(e[r+1],-1);o<=i&&n.push(o,i)}return n}function _f(e,t,n,r){var o=kf(t),i=xf.get(t).spec.config,s=(r?e.undone:e.done).popEvent(t,o);if(s){var a=s.selection.resolve(s.transform.doc),c=(r?e.done:e.undone).addTransform(s.transform,t.selection.getBookmark(),i,o),l=new mf(r?c:s.remaining,r?s.remaining:c,null,0);n(s.transform.setSelection(a).setMeta(xf,{redo:r,historyState:l}).scrollIntoView())}}var bf=!1,wf=null;function kf(e){var t=e.plugins;if(wf!=t){bf=!1,wf=t;for(var n=0;n<t.length;n++)if(t[n].spec.historyPreserveItems){bf=!0;break}}return bf}var xf=new fc("history"),Sf=new fc("closeHistory");function Mf(e){return e={depth:e&&e.depth||100,newGroupDelay:e&&e.newGroupDelay||500},new pc({key:xf,state:{init:function(){return new mf(hf.empty,hf.empty,null,0)},apply:function(t,n,r){return function(e,t,n,r){var o,i=n.getMeta(xf);if(i)return i.historyState;n.getMeta(Sf)&&(e=new mf(e.done,e.undone,null,0));var s=n.getMeta("appendedTransaction");if(0==n.steps.length)return e;if(s&&s.getMeta(xf))return s.getMeta(xf).redo?new mf(e.done.addTransform(n,null,r,kf(t)),e.undone,vf(n.mapping.maps[n.steps.length-1]),e.prevTime):new mf(e.done,e.undone.addTransform(n,null,r,kf(t)),null,e.prevTime);if(!1===n.getMeta("addToHistory")||s&&!1===s.getMeta("addToHistory"))return(o=n.getMeta("rebased"))?new mf(e.done.rebased(n,o),e.undone.rebased(n,o),yf(e.prevRanges,n.mapping),e.prevTime):new mf(e.done.addMaps(n.mapping.maps),e.undone.addMaps(n.mapping.maps),yf(e.prevRanges,n.mapping),e.prevTime);var a=0==e.prevTime||!s&&(e.prevTime<(n.time||0)-r.newGroupDelay||!function(e,t){if(!t)return!1;if(!e.docChanged)return!0;var n=!1;return e.mapping.maps[0].forEach((function(e,r){for(var o=0;o<t.length;o+=2)e<=t[o+1]&&r>=t[o]&&(n=!0)})),n}(n,e.prevRanges)),c=s?yf(e.prevRanges,n.mapping):vf(n.mapping.maps[n.steps.length-1]);return new mf(e.done.addTransform(n,a?t.selection.getBookmark():null,r,kf(t)),hf.empty,c,n.time)}(n,r,t,e)}},config:e})}const Ef=_d.create({name:"history",defaultOptions:{depth:100,newGroupDelay:500},addCommands:()=>({undo:()=>({state:e,dispatch:t})=>function(e,t){var n=xf.getState(e);return!(!n||0==n.done.eventCount||(t&&_f(n,e,t,!1),0))}(e,t),redo:()=>({state:e,dispatch:t})=>function(e,t){var n=xf.getState(e);return!(!n||0==n.undone.eventCount||(t&&_f(n,e,t,!0),0))}(e,t)}),addProseMirrorPlugins(){return[Mf(this.options)]},addKeyboardShortcuts(){return{"Mod-z":()=>this.editor.commands.undo(),"Mod-y":()=>this.editor.commands.redo(),"Shift-Mod-z":()=>this.editor.commands.redo(),"Mod-я":()=>this.editor.commands.undo(),"Shift-Mod-я":()=>this.editor.commands.redo()}}}),Of=Nh.create({name:"horizontalRule",defaultOptions:{HTMLAttributes:{}},group:"block",parseHTML:()=>[{tag:"hr"}],renderHTML({HTMLAttributes:e}){return["hr",ud(this.options.HTMLAttributes,e)]},addCommands(){return{setHorizontalRule:()=>({chain:e})=>e().command((({tr:e,dispatch:t})=>{const{selection:n}=e,{empty:r,$anchor:o}=n,i=o.parent.isTextblock&&!o.parent.type.spec.code&&!o.parent.textContent;if(!r||!i||!t)return!0;const s=o.before();return e.deleteRange(s,s+1),!0})).insertContent({type:this.name}).command((({tr:e,dispatch:t})=>{var n;if(t){const{parent:t,pos:r}=e.selection.$from,o=r+1;if(!e.doc.nodeAt(o)){const r=null===(n=t.type.contentMatch.defaultType)||void 0===n?void 0:n.create();r&&(e.insert(o,r),e.setSelection(Ka.create(e.doc,o)))}e.scrollIntoView()}return!0})).run()}},addInputRules(){return[(e=/^(?:---|—-|___\s|\*\*\*\s)$/,t=this.type,new bp(e,((e,r,o,i)=>{const s=n instanceof Function?n(r):n,{tr:a}=e;return r[0]&&a.replaceWith(o-1,i,t.create(s)),a})))];var e,t,n}}),Tf=/(?:^|\s)((?:\*)((?:[^*]+))(?:\*))$/gm,Cf=/(?:^|\s)((?:\*)((?:[^*]+))(?:\*))/gm,Af=/(?:^|\s)((?:_)((?:[^_]+))(?:_))$/gm,Nf=/(?:^|\s)((?:_)((?:[^_]+))(?:_))/gm,zf=zh.create({name:"italic",defaultOptions:{HTMLAttributes:{}},parseHTML:()=>[{tag:"em"},{tag:"i",getAttrs:e=>"normal"!==e.style.fontStyle&&null},{style:"font-style=italic"}],renderHTML({HTMLAttributes:e}){return["em",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({setItalic:()=>({commands:e})=>e.setMark("italic"),toggleItalic:()=>({commands:e})=>e.toggleMark("italic"),unsetItalic:()=>({commands:e})=>e.unsetMark("italic")}),addKeyboardShortcuts(){return{"Mod-i":()=>this.editor.commands.toggleItalic()}},addInputRules(){return[Ph(Tf,this.type),Ph(Af,this.type)]},addPasteRules(){return[Ih(Cf,this.type),Ih(Nf,this.type)]}}),Pf=Nh.create({name:"listItem",defaultOptions:{HTMLAttributes:{}},content:"paragraph block*",defining:!0,parseHTML:()=>[{tag:"li"}],renderHTML({HTMLAttributes:e}){return["li",ud(this.options.HTMLAttributes,e),0]},addKeyboardShortcuts(){return{Enter:()=>this.editor.commands.splitListItem("listItem"),Tab:()=>this.editor.commands.sinkListItem("listItem"),"Shift-Tab":()=>this.editor.commands.liftListItem("listItem")}}}),If=/^(\d+)\.\s$/,Df=Nh.create({name:"orderedList",defaultOptions:{HTMLAttributes:{}},group:"block list",content:"listItem+",addAttributes:()=>({start:{default:1,parseHTML:e=>({start:e.hasAttribute("start")?parseInt(e.getAttribute("start")||"",10):1})}}),parseHTML:()=>[{tag:"ol"}],renderHTML({HTMLAttributes:e}){const t=e,{start:n}=t,s=((e,t)=>{var n={};for(var s in e)o.call(e,s)&&t.indexOf(s)<0&&(n[s]=e[s]);if(null!=e&&r)for(var s of r(e))t.indexOf(s)<0&&i.call(e,s)&&(n[s]=e[s]);return n})(t,["start"]);return 1===n?["ol",ud(this.options.HTMLAttributes,s),0]:["ol",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({toggleOrderedList:()=>({commands:e})=>e.toggleList("orderedList","listItem")}),addKeyboardShortcuts(){return{"Mod-Shift-7":()=>this.editor.commands.toggleOrderedList()}},addInputRules(){return[kp(If,this.type,(e=>({start:+e[1]})),((e,t)=>t.childCount+t.attrs.start===+e[1]))]}}),jf=Nh.create({name:"paragraph",priority:1e3,defaultOptions:{HTMLAttributes:{}},group:"block",content:"inline*",parseHTML:()=>[{tag:"p"}],renderHTML({HTMLAttributes:e}){return["p",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({setParagraph:()=>({commands:e})=>e.setNode("paragraph")}),addKeyboardShortcuts(){return{"Mod-Alt-0":()=>this.editor.commands.setParagraph()}}}),Rf=/(?:^|\s)((?:~~)((?:[^~]+))(?:~~))$/gm,Lf=/(?:^|\s)((?:~~)((?:[^~]+))(?:~~))/gm,Bf=zh.create({name:"strike",defaultOptions:{HTMLAttributes:{}},parseHTML:()=>[{tag:"s"},{tag:"del"},{tag:"strike"},{style:"text-decoration",consuming:!1,getAttrs:e=>!!e.includes("line-through")&&{}}],renderHTML({HTMLAttributes:e}){return["s",ud(this.options.HTMLAttributes,e),0]},addCommands:()=>({setStrike:()=>({commands:e})=>e.setMark("strike"),toggleStrike:()=>({commands:e})=>e.toggleMark("strike"),unsetStrike:()=>({commands:e})=>e.unsetMark("strike")}),addKeyboardShortcuts(){return{"Mod-Shift-x":()=>this.editor.commands.toggleStrike()}},addInputRules(){return[Ph(Rf,this.type)]},addPasteRules(){return[Ih(Lf,this.type)]}}),$f=Nh.create({name:"text",group:"inline"}),Hf=_d.create({name:"starterKit",addExtensions(){var e,t,n,r,o,i,s,a,c,l,u,p,d,h,f,m,g,v;const y=[];return!1!==this.options.blockquote&&y.push(jh.configure(null===(e=this.options)||void 0===e?void 0:e.blockquote)),!1!==this.options.bold&&y.push(Hh.configure(null===(t=this.options)||void 0===t?void 0:t.bold)),!1!==this.options.bulletList&&y.push(Vh.configure(null===(n=this.options)||void 0===n?void 0:n.bulletList)),!1!==this.options.code&&y.push(Wh.configure(null===(r=this.options)||void 0===r?void 0:r.code)),!1!==this.options.codeBlock&&y.push(Gh.configure(null===(o=this.options)||void 0===o?void 0:o.codeBlock)),!1!==this.options.document&&y.push(Yh.configure(null===(i=this.options)||void 0===i?void 0:i.document)),!1!==this.options.dropcursor&&y.push(Zh.configure(null===(s=this.options)||void 0===s?void 0:s.dropcursor)),!1!==this.options.gapcursor&&y.push(sf.configure(null===(a=this.options)||void 0===a?void 0:a.gapcursor)),!1!==this.options.hardBreak&&y.push(af.configure(null===(c=this.options)||void 0===c?void 0:c.hardBreak)),!1!==this.options.heading&&y.push(cf.configure(null===(l=this.options)||void 0===l?void 0:l.heading)),!1!==this.options.history&&y.push(Ef.configure(null===(u=this.options)||void 0===u?void 0:u.history)),!1!==this.options.horizontalRule&&y.push(Of.configure(null===(p=this.options)||void 0===p?void 0:p.horizontalRule)),!1!==this.options.italic&&y.push(zf.configure(null===(d=this.options)||void 0===d?void 0:d.italic)),!1!==this.options.listItem&&y.push(Pf.configure(null===(h=this.options)||void 0===h?void 0:h.listItem)),!1!==this.options.orderedList&&y.push(Df.configure(null===(f=this.options)||void 0===f?void 0:f.orderedList)),!1!==this.options.paragraph&&y.push(jf.configure(null===(m=this.options)||void 0===m?void 0:m.paragraph)),!1!==this.options.strike&&y.push(Bf.configure(null===(g=this.options)||void 0===g?void 0:g.strike)),!1!==this.options.text&&y.push($f.configure(null===(v=this.options)||void 0===v?void 0:v.text)),y}}),Ff=_d.create({name:"placeholder",defaultOptions:{emptyEditorClass:"is-editor-empty",emptyNodeClass:"is-empty",placeholder:"Write something …",showOnlyWhenEditable:!0,showOnlyCurrent:!0},addProseMirrorPlugins(){return[new pc({props:{decorations:({doc:e,selection:t})=>{const n=this.editor.isEditable||!this.options.showOnlyWhenEditable,{anchor:r}=t,o=[];if(n)return e.descendants(((e,t)=>{const n=r>=t&&r<=t+e.nodeSize,i=!e.isLeaf&&!e.childCount;if((n||!this.options.showOnlyCurrent)&&i){const n=[this.options.emptyNodeClass];this.editor.isEmpty&&n.push(this.options.emptyEditorClass);const r=Bu.node(t,t+e.nodeSize,{class:n.join(" "),"data-placeholder":"function"==typeof this.options.placeholder?this.options.placeholder({editor:this.editor,node:e}):this.options.placeholder});o.push(r)}return!1})),Vu.create(e,o)}}})]}});export{Ko as $,pe as A,u as B,Ke as C,Vo as D,l as E,se as F,P as G,No as H,zr as I,w as J,ae as K,v as L,S as M,M as N,x as O,b as P,Fo as Q,Xo as R,We as S,ge as T,O as U,E as V,re as W,F as X,ve as Y,_e as Z,Be as _,J as a,V as a0,Me as a1,Lo as a2,Fi as a3,_ as a4,qi as a5,f as a6,R as a7,Se as a8,oe as a9,oi as aA,T as aB,Go as aC,Yo as aD,Wo as aE,si as aF,ai as aG,$o as aH,Ir as aI,je as aJ,Uo as aK,ni as aL,Zo as aM,Jo as aN,ti as aO,ne as aa,C as ab,h as ac,ie as ad,ce as ae,ee as af,Ho as ag,Ah as ah,Hf as ai,Ff as aj,he as ak,zo as al,Po as am,Io as an,Do as ao,jo as ap,Ro as aq,fe as ar,U as as,W as at,qo as au,Qo as av,ei as aw,Bo as ax,ii as ay,ri as az,q as b,Y as c,j as d,L as e,D as f,X as g,te as h,Ue as i,$e as j,$ as k,H as l,He as m,Z as n,Fe as o,Re as p,Le as q,ze as r,m as s,B as t,De as u,Ve as v,Pe as w,Ie as x,me as y,de as z}`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class at{constructor({base:t,routes:e,trailing_slash:r,renderer:s}){this.base=t,this.routes=e,this.trailing_slash=r,this.renderer=s,s.router=this,this.enabled=!0,document.body.setAttribute("tabindex","-1"),history.replaceState(history.state||{},"",location.href)}init_listeners(){let t;"scrollRestoration"in history&&(history.scrollRestoration="manual"),addEventListener("beforeunload",(()=>{history.scrollRestoration="auto"})),addEventListener("load",(()=>{history.scrollRestoration="manual"})),addEventListener("scroll",(()=>{clearTimeout(t),t=setTimeout((()=>{const t=(s=i({},history.state||{}),o={"sveltekit:scroll":ot()},e(s,r(o)));var s,o;history.replaceState(t,document.title,window.location.href)}),50)}));const s=t=>{const e=nt(t.target);e&&e.href&&e.hasAttribute("sveltekit:prefetch")&&this.prefetch(new URL(e.href))};let o;addEventListener("touchstart",s),addEventListener("mousemove",(t=>{clearTimeout(o),o=setTimeout((()=>{s(t)}),20)})),addEventListener("click",(t=>{if(!this.enabled)return;if(t.button||1!==t.which)return;if(t.metaKey||t.ctrlKey||t.shiftKey||t.altKey)return;if(t.defaultPrevented)return;const e=nt(t.target);if(!e)return;if(!e.href)return;const r="object"==typeof e.href&&"SVGAnimatedString"===e.href.constructor.name,s=String(r?e.href.baseVal:e.href);if(s===location.href)return void(location.hash||t.preventDefault());const o=(e.getAttribute("rel")||"").split(/\s+/);if(e.hasAttribute("download")||o&&o.includes("external"))return;if(r?e.target.baseVal:e.target)return;const n=new URL(s);if(!this.owns(n))return;const a=e.hasAttribute("sveltekit:noscroll");history.pushState({},"",n.href),this._navigate(n,a?ot():null,!1,[],n.hash),t.preventDefault()})),addEventListener("popstate",(t=>{if(t.state&&this.enabled){const e=new URL(location.href);this._navigate(e,t.state["sveltekit:scroll"],!1,[])}}))}owns(t){return t.origin===location.origin&&t.pathname.startsWith(this.base)}parse(t){if(this.owns(t)){const e=t.pathname.slice(this.base.length)||"/",r=decodeURI(e),s=this.routes.filter((([t])=>t.test(r))),o=new URLSearchParams(t.search);return{id:`${e}?${o}`,routes:s,path:e,query:o}}}async goto(t,{noscroll:e=!1,replaceState:r=!1,keepfocus:s=!1,state:o={}}={},n){const a=new URL(t,function(t){let e=t.baseURI;if(!e){const r=t.getElementsByTagName("base");e=r.length?r[0].href:t.URL}return e}(document));return this.enabled&&this.owns(a)?(history[r?"replaceState":"pushState"](o,"",t),this._navigate(a,e?ot():null,s,n,a.hash)):(location.href=a.href,new Promise((()=>{})))}enable(){this.enabled=!0}disable(){this.enabled=!1}async prefetch(t){const e=this.parse(t);if(!e)throw new Error("Attempted to prefetch a URL that does not belong to this app");return this.renderer.load(e)}async _navigate(t,e,r,s,o){const n=this.parse(t);if(!n)throw new Error("Attempted to navigate to a URL that does not belong to this app");if("/"!==n.path){const t=n.path.endsWith("/");(t&&"never"===this.trailing_slash||!t&&"always"===this.trailing_slash&&!(n.path.split("/").pop()||"").includes("."))&&(n.path=t?n.path.slice(0,-1):n.path+"/",history.replaceState({},"",`${this.base}${n.path}${location.search}`))}this.renderer.notify({path:n.path,query:n.query}),await this.renderer.update(n,s,!1),r||document.body.focus();const a=o&&document.getElementById(o.slice(1));e?scrollTo(e.x,e.y):a?a.scrollIntoView():scrollTo(0,0)}}function it(t){const e=D(t);let r=!0;return{notify:function(){r=!0,e.update((t=>t))},set:function(t){r=!1,e.set(t)},subscribe:function(t){let s;return e.subscribe((e=>{(void 0===s||r&&e!==s)&&t(s=e)}))}}}function lt(t,e){let r=`script[data-type="svelte-data"][data-url="${"string"==typeof t?t:t.url}"]`;e&&"string"==typeof e.body&&(r+=`[data-body="${function(t){let e=5381,r=t.length;if("string"==typeof t)for(;r;)e=33*e^t.charCodeAt(--r);else for(;r;)e=33*e^t[--r];return(e>>>0).toString(36)}(e.body)}"]`);const a=document.querySelector(r);if(a&&a.textContent){const t=JSON.parse(a.textContent),{body:e}=t,r=((t,e)=>{var r={};for(var a in t)o.call(t,a)&&e.indexOf(a)<0&&(r[a]=t[a]);if(null!=t&&s)for(var a of s(t))e.indexOf(a)<0&&n.call(t,a)&&(r[a]=t[a]);return r})(t,["body"]);return Promise.resolve(new Response(e,r))}return fetch(t,e)}class ct{constructor({Root:t,fallback:e,target:r,session:s,host:o}){this.Root=t,this.fallback=e,this.host=o,this.router,this.target=r,this.started=!1,this.session_id=1,this.invalid=new Set,this.invalidating=null,this.current={page:null,session_id:null,branch:[]},this.cache=new Map,this.loading={id:null,promise:null},this.stores={page:it({}),navigating:D(null),session:D(s)},this.$session=null,this.root=null;let n=!1;this.stores.session.subscribe((async t=>{if(this.$session=t,!n||!this.router)return;this.session_id+=1;const e=this.router.parse(new URL(location.href));e&&this.update(e,[],!0)})),n=!0}async start({status:t,error:e,nodes:r,page:s}){const o=[];let n,a,l={};try{for(let n=0;n<r.length;n+=1){const c=n===r.length-1,u=await this._load_node({module:await r[n],page:s,context:l,status:c?t:void 0,error:c?e:void 0});if(o.push(u),u&&u.loaded)if(u.loaded.error){if(e)throw u.loaded.error;a={status:u.loaded.status,error:u.loaded.error,path:s.path,query:s.query}}else u.loaded.context&&(l=i(i({},l),u.loaded.context))}n=a?await this._load_error(a):await this._get_navigation_result_from_branch({page:s,branch:o})}catch(u){if(e)throw u;n=await this._load_error({status:500,error:(c=u,c instanceof Error?c:new Error(JSON.stringify(c))),path:s.path,query:s.query})}var c;n.redirect?location.href=new URL(n.redirect,location.href).href:this._init(n)}notify({path:t,query:e}){dispatchEvent(new CustomEvent("sveltekit:navigation-start")),this.started&&this.stores.navigating.set({from:{path:this.current.page.path,query:this.current.page.query},to:{path:t,query:e}})}async update(t,e,r){const s=this.token={};let o=await this._get_navigation_result(t,r);if(s!==this.token)return;if(this.invalid.clear(),o.redirect){if(!(e.length>10||e.includes(t.path)))return void(this.router?this.router.goto(o.redirect,{replaceState:!0},[...e,t.path]):location.href=new URL(o.redirect,location.href).href);o=await this._load_error({status:500,error:new Error("Redirect loop"),path:t.path,query:t.query})}if(o.reload?location.reload():this.started?(this.current=o.state,this.root.$set(o.props),this.stores.navigating.set(null),await 0):this._init(o),dispatchEvent(new CustomEvent("sveltekit:navigation-end")),this.loading.promise=null,this.loading.id=null,!this.router)return;const n=o.state.branch[o.state.branch.length-1];n&&!1===n.module.router?this.router.disable():this.router.enable()}load(t){return this.loading.promise=this._get_navigation_result(t,!1),this.loading.id=t.id,this.loading.promise}invalidate(t){return this.invalid.add(t),this.invalidating||(this.invalidating=Promise.resolve().then((async()=>{const t=this.router&&this.router.parse(new URL(location.href));t&&await this.update(t,[],!0),this.invalidating=null}))),this.invalidating}_init(t){this.current=t.state;const e=document.querySelector("style[data-svelte]");e&&e.remove(),this.root=new this.Root({target:this.target,props:i({stores:this.stores},t.props),hydrate:!0}),this.started=!0}async _get_navigation_result(t,e){if(this.loading.id===t.id)return this.loading.promise;for(let r=0;r<t.routes.length;r+=1){const s=t.routes[r];if(1===s.length)return{reload:!0,props:{},state:this.current};let o=r+1;for(;o<t.routes.length;){const e=t.routes[o];if(e[0].toString()!==s[0].toString())break;1!==e.length&&e[1].forEach((t=>t())),o+=1}const n=await this._load({route:s,path:t.path,query:t.query},e);if(n)return n}return await this._load_error({status:404,error:new Error(`Not found: ${t.path}`),path:t.path,query:t.query})}async _get_navigation_result_from_branch({page:t,branch:e}){const r=e.filter(Boolean),s={state:{page:t,branch:e,session_id:this.session_id},props:{components:r.map((t=>t.module.default))}};for(let a=0;a<r.length;a+=1){const t=r[a].loaded;t&&(s.props[`props_${a}`]=await t.props)}this.current.page&&t.path===this.current.page.path&&t.query.toString()===this.current.page.query.toString()||(s.props.page=t);const o=r[r.length-1],n=o.loaded&&o.loaded.maxage;if(n){const e=`${t.path}?${t.query}`;let r=!1;const o=()=>{this.cache.get(e)===s&&this.cache.delete(e),i(),clearTimeout(a)},a=setTimeout(o,1e3*n),i=this.stores.session.subscribe((()=>{r&&o()}));r=!0,this.cache.set(e,s)}return s}async _load_node({status:t,error:e,module:r,page:s,context:o}){const n={module:r,uses:{params:new Set,path:!1,query:!1,session:!1,context:!1,dependencies:[]},loaded:null,context:o},a={};for(const i in s.params)Object.defineProperty(a,i,{get:()=>(n.uses.params.add(i),s.params[i]),enumerable:!0});const l=this.$session;if(r.load){const{started:c}=this,u={page:{host:s.host,params:a,get path(){return n.uses.path=!0,s.path},get query(){return n.uses.query=!0,s.query}},get session(){return n.uses.session=!0,l},get context(){return n.uses.context=!0,i({},o)},fetch(t,e){const r="string"==typeof t?t:t.url,{href:o}=new URL(r,new URL(s.path,document.baseURI));return n.uses.dependencies.push(o),c?fetch(t,e):lt(t,e)}};e&&(u.status=t,u.error=e);const d=await r.load.call(null,u);if(!d)return;n.loaded=function(t){const e=t.status&&t.status>=400&&t.status<=599&&!t.redirect;if(t.error||e){const r=t.status;if(!t.error&&e)return{status:r||500,error:new Error};const s="string"==typeof t.error?new Error(t.error):t.error;return s instanceof Error?!r||r<400||r>599?(console.warn('"error" returned from load() without a valid status code — defaulting to 500'),{status:500,error:s}):{status:r,error:s}:{status:500,error:new Error(`"error" property returned from load() must be a string or instance of Error, received type "${typeof s}"`)}}if(t.redirect){if(!t.status||3!==Math.floor(t.status/100))return{status:500,error:new Error('"redirect" property returned from load() must be accompanied by a 3xx status code')};if("string"!=typeof t.redirect)return{status:500,error:new Error('"redirect" property returned from load() must be a string')}}return t}(d),n.loaded.context&&(n.context=n.loaded.context)}return n}async _load({route:t,path:e,query:r},s){const o=`${e}?${r}`;if(!s){const t=this.cache.get(o);if(t)return t}const[n,a,l,c]=t,u=c?c(n.exec(e)):{},d=this.current.page&&{path:e!==this.current.page.path,params:Object.keys(u).filter((t=>this.current.page.params[t]!==u[t])),query:r.toString()!==this.current.page.query.toString(),session:this.session_id!==this.current.session_id},h={host:this.host,path:e,query:r,params:u},p=[];let f,g={},_=!1,m=200;a.forEach((t=>t()));t:for(let $=0;$<a.length;$+=1){let t;try{if(!a[$])continue;const e=await a[$](),r=this.current.branch[$];if(!r||e!==r.module||d.path&&r.uses.path||d.params.some((t=>r.uses.params.has(t)))||d.query&&r.uses.query||d.session&&r.uses.session||r.uses.dependencies.some((t=>this.invalid.has(t)))||_&&r.uses.context){t=await this._load_node({module:e,page:h,context:g});const r=$===a.length-1;if(t&&t.loaded){if(t.loaded.error&&(m=t.loaded.status,f=t.loaded.error),t.loaded.redirect)return{redirect:t.loaded.redirect,props:{},state:this.current};t.loaded.context&&(_=!0)}else if(r&&e.load)return}else t=r}catch(y){m=500,f=y}if(f){for(;$--;)if(l[$]){let t,e,r=$;for(;!(e=p[r]);)r-=1;try{if(t=await this._load_node({status:m,error:f,module:await l[$](),page:h,context:e.context}),t&&t.loaded&&t.loaded.error)continue;p.push(t);break t}catch(y){continue}}return await this._load_error({status:m,error:f,path:e,query:r})}t&&t.loaded&&t.loaded.context&&(g=i(i({},g),t.loaded.context)),p.push(t)}return await this._get_navigation_result_from_branch({page:h,branch:p})}async _load_error({status:t,error:e,path:r,query:s}){const o={host:this.host,path:r,query:s,params:{}},n=await this._load_node({module:await this.fallback[0],page:o,context:{}}),a=[n,await this._load_node({status:t,error:e,module:await this.fallback[1],page:o,context:n&&n.loaded&&n.loaded.context||{}})];return await this._get_navigation_result_from_branch({page:o,branch:a})}}async function ut({paths:t,target:e,session:r,host:s,route:o,spa:n,trailing_slash:a,hydrate:i}){const l=new ct({Root:Y,fallback:rt,target:e,session:r,host:s}),c=o?new at({base:t.base,routes:et,trailing_slash:a,renderer:l}):null;U(c),function(t){st=t.base,t.assets}(t),i&&await l.start(i),c&&(n&&c.goto(location.href,{replaceState:!0},[]),c.init_listeners()),dispatchEvent(new CustomEvent("sveltekit:start"))}export{ut as start}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer data-domain="dora.beta.gouv.fr" src="https://plausible.io/js/plausible.js" data-svelte="svelte-jlms0z"></script>`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer data-domain="dora.beta.gouv.fr" src="https://plausible.io/js/plausible.js" data-svelte="svelte-jlms0z"></script>`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer data-domain="dora.beta.gouv.fr" src="https://plausible.io/js/plausible.js" data-svelte="svelte-jlms0z"></script>`
  
  
  
  
Instances: 3
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
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

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="svelte-8o8quc">`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="svelte-8o8quc">`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "" "city" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://plausible.io/js/plausible.js`
  
  
  * Evidence: `<script defer data-domain="dora.beta.gouv.fr" src="https://plausible.io/js/plausible.js" data-svelte="svelte-jlms0z"></script>`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://plausible.io/js/plausible.js`
  
  
  * Evidence: `<script defer data-domain="dora.beta.gouv.fr" src="https://plausible.io/js/plausible.js" data-svelte="svelte-jlms0z"></script>`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://plausible.io/js/plausible.js`
  
  
  * Evidence: `<script defer data-domain="dora.beta.gouv.fr" src="https://plausible.io/js/plausible.js" data-svelte="svelte-jlms0z"></script>`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
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
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/robots.txt](https://dora.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/singletons-12a22614.js](https://dora.beta.gouv.fr/_app/chunks/singletons-12a22614.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js](https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/start-28b178f4.js](https://dora.beta.gouv.fr/_app/start-28b178f4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/button-9cc95553.js](https://dora.beta.gouv.fr/_app/chunks/button-9cc95553.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/navigation-2ffed81e.js](https://dora.beta.gouv.fr/_app/chunks/navigation-2ffed81e.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/pages/index.svelte-5d3734d0.js](https://dora.beta.gouv.fr/_app/pages/index.svelte-5d3734d0.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js](https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/error.svelte-b457f2f4.js](https://dora.beta.gouv.fr/_app/error.svelte-b457f2f4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/stores-a6817ccd.js](https://dora.beta.gouv.fr/_app/chunks/stores-a6817ccd.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/link-button-cf8a317c.js](https://dora.beta.gouv.fr/_app/chunks/link-button-cf8a317c.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/centered-grid-c53c6d76.js](https://dora.beta.gouv.fr/_app/chunks/centered-grid-c53c6d76.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/start-28b178f4.js](https://dora.beta.gouv.fr/_app/start-28b178f4.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.png](https://dora.beta.gouv.fr/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js](https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/singletons-12a22614.js](https://dora.beta.gouv.fr/_app/chunks/singletons-12a22614.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/robots.txt](https://dora.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js](https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/stores-a6817ccd.js](https://dora.beta.gouv.fr/_app/chunks/stores-a6817ccd.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.ico](https://dora.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.svg](https://dora.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10zm-1-11H7v2h4v4h2v-4h4v-2h-4V7h-2v4z`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20h-2v-7H4v7H2V4h2v7h7V4h2v16zm8-12v12h-2v-9`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `10zm-1-11H7v2h4v4h2v-4h4v-2h-4V7h-2v4z`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/assets/pages/index.svelte-b61f03b2.css](https://dora.beta.gouv.fr/_app/assets/pages/index.svelte-b61f03b2.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0ibm9uZSIgZD0iTTAgMGgyNHYyNEgweiIvPjxwYXRoIHN0cm9rZT0iI2ZmZiIgZD0ibTEwIDE1LjE3MiA5LjE5Mi05LjE5MyAxLjQxNSAxLjQxNEwxMCAxOGwtNi4zNjQtNi4zNjQgMS40MTQtMS40MTR6Ii8+PC9zdmc+`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `10zm-1-11H7v2h4v4h2v-4h4v-2h-4V7h-2v4z`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�L��_��~��\x001e/�\x001d���x����{���</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.ico](https://dora.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/stores-a6817ccd.js](https://dora.beta.gouv.fr/_app/chunks/stores-a6817ccd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js](https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/button-9cc95553.js](https://dora.beta.gouv.fr/_app/chunks/button-9cc95553.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js](https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/link-button-cf8a317c.js](https://dora.beta.gouv.fr/_app/chunks/link-button-cf8a317c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/navigation-2ffed81e.js](https://dora.beta.gouv.fr/_app/chunks/navigation-2ffed81e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/start-28b178f4.js](https://dora.beta.gouv.fr/_app/start-28b178f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bTODO\b and was detected in the element starting with: "<script type="module"></p><p>			import { start } from "/_app/start-28b178f4.js";</p><p>			start({</p><p>				target: document.querySelector("#svelt", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="flex flex-row items-center justify-center py-2 text-sm text-center rounded outline-none  focus:shadow-focus text-gray-text-alt2" href="" >Plan du site
  
  <div class="h-2 mx-2 border-l border-gray-03"></div></a>`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="flex flex-row items-center justify-center py-2 text-sm text-center rounded outline-none  focus:shadow-focus text-gray-text-alt2" href="" >Plan du site
  
  <div class="h-2 mx-2 border-l border-gray-03"></div></a>`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/?city=ZAP](https://dora.beta.gouv.fr/?city=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="flex flex-row items-center justify-center py-2 text-sm text-center rounded outline-none  focus:shadow-focus text-gray-text-alt2" href="" >Plan du site
  
  <div class="h-2 mx-2 border-l border-gray-03"></div></a>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.ico](https://dora.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js](https://dora.beta.gouv.fr/_app/pages/__layout.svelte-d30ebabf.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/singletons-12a22614.js](https://dora.beta.gouv.fr/_app/chunks/singletons-12a22614.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.svg](https://dora.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/robots.txt](https://dora.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js](https://dora.beta.gouv.fr/_app/chunks/vendor-5a3c78fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/favicon.png](https://dora.beta.gouv.fr/favicon.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js](https://dora.beta.gouv.fr/_app/chunks/auth-8aedfa63.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/start-28b178f4.js](https://dora.beta.gouv.fr/_app/start-28b178f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Other information
<p>In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.</p>
  
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
  
  
  
* URL: [https://dora.beta.gouv.fr/sitemap.xml](https://dora.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `48008496`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/_app/start-28b178f4.js](https://dora.beta.gouv.fr/_app/start-28b178f4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `48008496`
  
  
  
  
* URL: [https://dora.beta.gouv.fr/](https://dora.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `48008496`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>48008496, which evaluates to: 1971-07-10 15:41:36</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

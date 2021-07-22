
# ZAP Scanning Report

Generated on Thu, 22 Jul 2021 00:36:59


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 2 |
| Low | 4 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 4 | 
| Permissions Policy Header Not Set | Low | 9 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 7 | 
| Non-Storable Content | Informational | 4 | 
| Storable and Cacheable Content | Informational | 7 | 
| Timestamp Disclosure - Unix | Informational | 28 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `5686274509803921`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 568627</p><p>Brand: MAESTRO</p><p>Category: STANDARD</p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/sitemap.xml](https://anais.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/robots.txt](https://anais.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr](https://anais.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/](https://anais.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js](https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class a{constructor(e,t){this._parent=e,this._name=t?t.name||"unnamed":"<root>",this._properties=t&&t.properties||{},this._zoneDelegate=new l(this,this._parent&&this._parent._zoneDelegate,t)}static assertZonePatched(){if(e.Promise!==P.ZoneAwarePromise)throw new Error("Zone.js has detected that ZoneAwarePromise `(window|global).Promise` has been overwritten.\nMost likely cause is that a Promise polyfill has been loaded after Zone.js (Polyfilling Promise api is not necessary when zone.js is loaded. If you must load one, do so before loading zone.js.)")}static get root(){let e=a.current;for(;e.parent;)e=e.parent;return e}static get current(){return C.zone}static get currentTask(){return j}static __load_patch(t,o){if(P.hasOwnProperty(t)){if(s)throw Error("Already loaded patch: "+t)}else if(!e["__Zone_disable_"+t]){const i="Zone:"+t;n(i),P[t]=o(e,a,x),r(i,i)}}get parent(){return this._parent}get name(){return this._name}get(e){const t=this.getZoneWith(e);if(t)return t._properties[e]}getZoneWith(e){let t=this;for(;t;){if(t._properties.hasOwnProperty(e))return t;t=t._parent}return null}fork(e){if(!e)throw new Error("ZoneSpec required!");return this._zoneDelegate.fork(this,e)}wrap(e,t){if("function"!=typeof e)throw new Error("Expecting function got: "+e);const n=this._zoneDelegate.intercept(this,e,t),r=this;return function(){return r.runGuarded(n,this,arguments,t)}}run(e,t,n,r){C={parent:C,zone:this};try{return this._zoneDelegate.invoke(this,e,t,n,r)}finally{C=C.parent}}runGuarded(e,t=null,n,r){C={parent:C,zone:this};try{try{return this._zoneDelegate.invoke(this,e,t,n,r)}catch(o){if(this._zoneDelegate.handleError(this,o))throw o}}finally{C=C.parent}}runTask(e,t,n){if(e.zone!=this)throw new Error("A task can only be run in the zone of creation! (Creation: "+(e.zone||k).name+"; Execution: "+this.name+")");if(e.state===_&&(e.type===O||e.type===D))return;const r=e.state!=w;r&&e._transitionTo(w,T),e.runCount++;const o=j;j=e,C={parent:C,zone:this};try{e.type==D&&e.data&&!e.data.isPeriodic&&(e.cancelFn=void 0);try{return this._zoneDelegate.invokeTask(this,e,t,n)}catch(i){if(this._zoneDelegate.handleError(this,i))throw i}}finally{e.state!==_&&e.state!==S&&(e.type==O||e.data&&e.data.isPeriodic?r&&e._transitionTo(T,w):(e.runCount=0,this._updateTaskCount(e,-1),r&&e._transitionTo(_,w,_))),C=C.parent,j=o}}scheduleTask(e){if(e.zone&&e.zone!==this){let t=this;for(;t;){if(t===e.zone)throw Error(`can not reschedule task to ${this.name} which is descendants of the original zone ${e.zone.name}`);t=t.parent}}e._transitionTo(b,_);const t=[];e._zoneDelegates=t,e._zone=this;try{e=this._zoneDelegate.scheduleTask(this,e)}catch(n){throw e._transitionTo(S,b,_),this._zoneDelegate.handleError(this,n),n}return e._zoneDelegates===t&&this._updateTaskCount(e,1),e.state==b&&e._transitionTo(T,b),e}scheduleMicroTask(e,t,n,r){return this.scheduleTask(new u(Z,e,t,n,r,void 0))}scheduleMacroTask(e,t,n,r,o){return this.scheduleTask(new u(D,e,t,n,r,o))}scheduleEventTask(e,t,n,r,o){return this.scheduleTask(new u(O,e,t,n,r,o))}cancelTask(e){if(e.zone!=this)throw new Error("A task can only be cancelled in the zone of creation! (Creation: "+(e.zone||k).name+"; Execution: "+this.name+")");e._transitionTo(E,T,w);try{this._zoneDelegate.cancelTask(this,e)}catch(t){throw e._transitionTo(S,E),this._zoneDelegate.handleError(this,t),t}return this._updateTaskCount(e,-1),e._transitionTo(_,E),e.runCount=0,e}_updateTaskCount(e,t){const n=e._zoneDelegates;-1==t&&(e._zoneDelegates=null);for(let r=0;r<n.length;r++)n[r]._updateTaskCount(e.type,t)}}a.__symbol__=i;const c={name:"",onHasTask:(e,t,n,r)=>e.hasTask(n,r),onScheduleTask:(e,t,n,r)=>e.scheduleTask(n,r),onInvokeTask:(e,t,n,r,o,i)=>e.invokeTask(n,r,o,i),onCancelTask:(e,t,n,r)=>e.cancelTask(n,r)};class l{constructor(e,t,n){this._taskCounts={microTask:0,macroTask:0,eventTask:0},this.zone=e,this._parentDelegate=t,this._forkZS=n&&(n&&n.onFork?n:t._forkZS),this._forkDlgt=n&&(n.onFork?t:t._forkDlgt),this._forkCurrZone=n&&(n.onFork?this.zone:t._forkCurrZone),this._interceptZS=n&&(n.onIntercept?n:t._interceptZS),this._interceptDlgt=n&&(n.onIntercept?t:t._interceptDlgt),this._interceptCurrZone=n&&(n.onIntercept?this.zone:t._interceptCurrZone),this._invokeZS=n&&(n.onInvoke?n:t._invokeZS),this._invokeDlgt=n&&(n.onInvoke?t:t._invokeDlgt),this._invokeCurrZone=n&&(n.onInvoke?this.zone:t._invokeCurrZone),this._handleErrorZS=n&&(n.onHandleError?n:t._handleErrorZS),this._handleErrorDlgt=n&&(n.onHandleError?t:t._handleErrorDlgt),this._handleErrorCurrZone=n&&(n.onHandleError?this.zone:t._handleErrorCurrZone),this._scheduleTaskZS=n&&(n.onScheduleTask?n:t._scheduleTaskZS),this._scheduleTaskDlgt=n&&(n.onScheduleTask?t:t._scheduleTaskDlgt),this._scheduleTaskCurrZone=n&&(n.onScheduleTask?this.zone:t._scheduleTaskCurrZone),this._invokeTaskZS=n&&(n.onInvokeTask?n:t._invokeTaskZS),this._invokeTaskDlgt=n&&(n.onInvokeTask?t:t._invokeTaskDlgt),this._invokeTaskCurrZone=n&&(n.onInvokeTask?this.zone:t._invokeTaskCurrZone),this._cancelTaskZS=n&&(n.onCancelTask?n:t._cancelTaskZS),this._cancelTaskDlgt=n&&(n.onCancelTask?t:t._cancelTaskDlgt),this._cancelTaskCurrZone=n&&(n.onCancelTask?this.zone:t._cancelTaskCurrZone),this._hasTaskZS=null,this._hasTaskDlgt=null,this._hasTaskDlgtOwner=null,this._hasTaskCurrZone=null;const r=n&&n.onHasTask;(r||t&&t._hasTaskZS)&&(this._hasTaskZS=r?n:c,this._hasTaskDlgt=t,this._hasTaskDlgtOwner=this,this._hasTaskCurrZone=e,n.onScheduleTask||(this._scheduleTaskZS=c,this._scheduleTaskDlgt=t,this._scheduleTaskCurrZone=this.zone),n.onInvokeTask||(this._invokeTaskZS=c,this._invokeTaskDlgt=t,this._invokeTaskCurrZone=this.zone),n.onCancelTask||(this._cancelTaskZS=c,this._cancelTaskDlgt=t,this._cancelTaskCurrZone=this.zone))}fork(e,t){return this._forkZS?this._forkZS.onFork(this._forkDlgt,this.zone,e,t):new a(e,t)}intercept(e,t,n){return this._interceptZS?this._interceptZS.onIntercept(this._interceptDlgt,this._interceptCurrZone,e,t,n):t}invoke(e,t,n,r,o){return this._invokeZS?this._invokeZS.onInvoke(this._invokeDlgt,this._invokeCurrZone,e,t,n,r,o):t.apply(n,r)}handleError(e,t){return!this._handleErrorZS||this._handleErrorZS.onHandleError(this._handleErrorDlgt,this._handleErrorCurrZone,e,t)}scheduleTask(e,t){let n=t;if(this._scheduleTaskZS)this._hasTaskZS&&n._zoneDelegates.push(this._hasTaskDlgtOwner),n=this._scheduleTaskZS.onScheduleTask(this._scheduleTaskDlgt,this._scheduleTaskCurrZone,e,t),n||(n=t);else if(t.scheduleFn)t.scheduleFn(t);else{if(t.type!=Z)throw new Error("Task is missing scheduleFn.");v(t)}return n}invokeTask(e,t,n,r){return this._invokeTaskZS?this._invokeTaskZS.onInvokeTask(this._invokeTaskDlgt,this._invokeTaskCurrZone,e,t,n,r):t.callback.apply(n,r)}cancelTask(e,t){let n;if(this._cancelTaskZS)n=this._cancelTaskZS.onCancelTask(this._cancelTaskDlgt,this._cancelTaskCurrZone,e,t);else{if(!t.cancelFn)throw Error("Task is not cancelable");n=t.cancelFn(t)}return n}hasTask(e,t){try{this._hasTaskZS&&this._hasTaskZS.onHasTask(this._hasTaskDlgt,this._hasTaskCurrZone,e,t)}catch(n){this.handleError(e,n)}}_updateTaskCount(e,t){const n=this._taskCounts,r=n[e],o=n[e]=r+t;if(o<0)throw new Error("More tasks executed then were scheduled.");0!=r&&0!=o||this.hasTask(this.zone,{microTask:n.microTask>0,macroTask:n.macroTask>0,eventTask:n.eventTask>0,change:e})}}class u{constructor(t,n,r,o,i,s){if(this._zone=null,this.runCount=0,this._zoneDelegates=null,this._state="notScheduled",this.type=t,this.source=n,this.data=o,this.scheduleFn=i,this.cancelFn=s,!r)throw new Error("callback is not defined");this.callback=r;const a=this;this.invoke=t===O&&o&&o.useG?u.invokeTask:function(){return u.invokeTask.call(e,a,this,arguments)}}static invokeTask(e,t,n){e||(e=this),z++;try{return e.runCount++,e.zone.runTask(e,t,n)}finally{1==z&&m(),z--}}get zone(){return this._zone}get state(){return this._state}cancelScheduleRequest(){this._transitionTo(_,b)}_transitionTo(e,t,n){if(this._state!==t&&this._state!==n)throw new Error(`${this.type} '${this.source}': can not transition to '${e}', expecting state '${t}'${n?" or '"+n+"'":""}, was '${this._state}'.`);this._state=e,e==_&&(this._zoneDelegates=null)}toString(){return this.data&&void 0!==this.data.handleId?this.data.handleId.toString():Object.prototype.toString.call(this)}toJSON(){return{type:this.type,state:this.state,source:this.source,zone:this.zone.name,runCount:this.runCount}}}const f=i("setTimeout"),p=i("Promise"),h=i("then");let d,g=[],y=!1;function v(t){if(0===z&&0===g.length)if(d||e[p]&&(d=e[p].resolve(0)),d){let e=d[h];e||(e=d.then),e.call(d,m)}else e[f](m,0);t&&g.push(t)}function m(){if(!y){for(y=!0;g.length;){const t=g;g=[];for(let n=0;n<t.length;n++){const r=t[n];try{r.zone.runTask(r,null,null)}catch(e){x.onUnhandledError(e)}}}x.microtaskDrainDone(),y=!1}}const k={name:"NO ZONE"},_="notScheduled",b="scheduling",T="scheduled",w="running",E="canceling",S="unknown",Z="microTask",D="macroTask",O="eventTask",P={},x={symbol:i,currentZoneFrame:()=>C,onUnhandledError:I,microtaskDrainDone:I,scheduleMicroTask:v,showUncaughtError:()=>!a[i("ignoreConsoleErrorUncaughtError")],patchEventTarget:()=>[],patchOnProperties:I,patchMethod:()=>I,bindArguments:()=>[],patchThen:()=>I,patchMacroTask:()=>I,setNativePromise:e=>{e&&"function"==typeof e.resolve&&(d=e.resolve(0))},patchEventPrototype:()=>I,isIEOrEdge:()=>!1,getGlobalObjects:()=>{},ObjectDefineProperty:()=>I,ObjectGetOwnPropertyDescriptor:()=>{},ObjectCreate:()=>{},ArraySlice:()=>[],patchClass:()=>I,wrapWithCurrentZone:()=>I,filterProperties:()=>[],attachOriginToPatched:()=>I,_redefineProperty:()=>I,patchCallbacks:()=>I};let C={parent:null,zone:new a(null,null)},j=null,z=0;function I(){}r("Zone","Zone"),e.Zone=a}("undefined"!=typeof window&&window||"undefined"!=typeof self&&self||global),Zone.__load_patch("ZoneAwarePromise",(e,t,n)=>{const r=Object.getOwnPropertyDescriptor,o=Object.defineProperty,i=n.symbol,s=[],a=!0===e[i("DISABLE_WRAPPING_UNCAUGHT_PROMISE_REJECTION")],c=i("Promise"),l=i("then");n.onUnhandledError=e=>{if(n.showUncaughtError()){const t=e&&e.rejection;t?console.error("Unhandled Promise rejection:",t instanceof Error?t.message:t,"; Zone:",e.zone.name,"; Task:",e.task&&e.task.source,"; Value:",t,t instanceof Error?t.stack:void 0):console.error(e)}},n.microtaskDrainDone=()=>{for(;s.length;){const t=s.shift();try{t.zone.runGuarded(()=>{throw t})}catch(e){f(e)}}};const u=i("unhandledPromiseRejectionHandler");function f(e){n.onUnhandledError(e);try{const n=t[u];"function"==typeof n&&n.call(this,e)}catch(r){}}function p(e){return e&&e.then}function h(e){return e}function d(e){return D.reject(e)}const g=i("state"),y=i("value"),v=i("finally"),m=i("parentPromiseValue"),k=i("parentPromiseState");function _(e,t){return n=>{try{T(e,t,n)}catch(r){T(e,!1,r)}}}const b=i("currentTaskTrace");function T(e,r,i){const c=function(){let e=!1;return function(t){return function(){e||(e=!0,t.apply(null,arguments))}}}();if(e===i)throw new TypeError("Promise resolved with itself");if(null===e[g]){let f=null;try{"object"!=typeof i&&"function"!=typeof i||(f=i&&i.then)}catch(u){return c(()=>{T(e,!1,u)})(),e}if(!1!==r&&i instanceof D&&i.hasOwnProperty(g)&&i.hasOwnProperty(y)&&null!==i[g])E(i),T(e,i[g],i[y]);else if(!1!==r&&"function"==typeof f)try{f.call(i,c(_(e,r)),c(_(e,!1)))}catch(u){c(()=>{T(e,!1,u)})()}else{e[g]=r;const c=e[y];if(e[y]=i,e[v]===v&&!0===r&&(e[g]=e[k],e[y]=e[m]),!1===r&&i instanceof Error){const e=t.currentTask&&t.currentTask.data&&t.currentTask.data.__creationTrace__;e&&o(i,b,{configurable:!0,enumerable:!1,writable:!0,value:e})}for(let t=0;t<c.length;)S(e,c[t++],c[t++],c[t++],c[t++]);if(0==c.length&&0==r){e[g]=0;let r=i;if(!a)try{throw new Error("Uncaught (in promise): "+((l=i)&&l.toString===Object.prototype.toString?(l.constructor&&l.constructor.name||"")+": "+JSON.stringify(l):l?l.toString():Object.prototype.toString.call(l))+(i&&i.stack?"\n"+i.stack:""))}catch(u){r=u}r.rejection=i,r.promise=e,r.zone=t.current,r.task=t.currentTask,s.push(r),n.scheduleMicroTask()}}}var l;return e}const w=i("rejectionHandledHandler");function E(e){if(0===e[g]){try{const n=t[w];n&&"function"==typeof n&&n.call(this,{rejection:e[y],promise:e})}catch(n){}e[g]=!1;for(let t=0;t<s.length;t++)e===s[t].promise&&s.splice(t,1)}}function S(e,t,n,r,o){E(e);const i=e[g],s=i?"function"==typeof r?r:h:"function"==typeof o?o:d;t.scheduleMicroTask("Promise.then",()=>{try{const r=e[y],o=!!n&&v===n[v];o&&(n[m]=r,n[k]=i);const a=t.run(s,void 0,o&&s!==d&&s!==h?[]:[r]);T(n,!0,a)}catch(r){T(n,!1,r)}},n)}const Z=function(){};class D{static toString(){return"function ZoneAwarePromise() { [native code] }"}static resolve(e){return T(new this(null),!0,e)}static reject(e){return T(new this(null),!1,e)}static race(e){let t,n,r=new this((e,r)=>{t=e,n=r});function o(e){t(e)}function i(e){n(e)}for(let s of e)p(s)||(s=this.resolve(s)),s.then(o,i);return r}static all(e){return D.allWithCallback(e)}static allSettled(e){return(this&&this.prototype instanceof D?this:D).allWithCallback(e,{thenCallback:e=>({status:"fulfilled",value:e}),errorCallback:e=>({status:"rejected",reason:e})})}static allWithCallback(e,t){let n,r,o=new this((e,t)=>{n=e,r=t}),i=2,s=0;const a=[];for(let l of e){p(l)||(l=this.resolve(l));const e=s;try{l.then(r=>{a[e]=t?t.thenCallback(r):r,i--,0===i&&n(a)},o=>{t?(a[e]=t.errorCallback(o),i--,0===i&&n(a)):r(o)})}catch(c){r(c)}i++,s++}return i-=2,0===i&&n(a),o}constructor(e){const t=this;if(!(t instanceof D))throw new Error("Must be an instanceof Promise.");t[g]=null,t[y]=[];try{e&&e(_(t,!0),_(t,!1))}catch(n){T(t,!1,n)}}get[Symbol.toStringTag](){return"Promise"}get[Symbol.species](){return D}then(e,n){let r=this.constructor[Symbol.species];r&&"function"==typeof r||(r=this.constructor||D);const o=new r(Z),i=t.current;return null==this[g]?this[y].push(i,o,e,n):S(this,i,o,e,n),o}catch(e){return this.then(null,e)}finally(e){let n=this.constructor[Symbol.species];n&&"function"==typeof n||(n=D);const r=new n(Z);r[v]=v;const o=t.current;return null==this[g]?this[y].push(o,r,e,e):S(this,o,r,e,e),r}}D.resolve=D.resolve,D.reject=D.reject,D.race=D.race,D.all=D.all;const O=e[c]=e.Promise,P=t.__symbol__("ZoneAwarePromise");let x=r(e,"Promise");x&&!x.configurable||(x&&delete x.writable,x&&delete x.value,x||(x={configurable:!0,enumerable:!0}),x.get=function(){return e[P]?e[P]:e[c]},x.set=function(t){t===D?e[P]=t:(e[c]=t,t.prototype[l]||j(t),n.setNativePromise(t))},o(e,"Promise",x)),e.Promise=D;const C=i("thenPatched");function j(e){const t=e.prototype,n=r(t,"then");if(n&&(!1===n.writable||!n.configurable))return;const o=t.then;t[l]=o,e.prototype.then=function(e,t){return new D((e,t)=>{o.call(this,e,t)}).then(e,t)},e[C]=!0}if(n.patchThen=j,O){j(O);const t=e.fetch;"function"==typeof t&&(e[n.symbol("fetch")]=t,e.fetch=(z=t,function(){let e=z.apply(this,arguments);if(e instanceof D)return e;let t=e.constructor;return t[C]||j(t),e}))}var z;return Promise[t.__symbol__("uncaughtPromiseErrors")]=s,D});const e=Object.getOwnPropertyDescriptor,t=Object.defineProperty,n=Object.getPrototypeOf,r=Object.create,o=Array.prototype.slice,i=Zone.__symbol__("addEventListener"),s=Zone.__symbol__("removeEventListener"),a=Zone.__symbol__("");function c(e,t){return Zone.current.wrap(e,t)}function l(e,t,n,r,o){return Zone.current.scheduleMacroTask(e,t,n,r,o)}const u=Zone.__symbol__,f="undefined"!=typeof window,p=f?window:void 0,h=f&&p||"object"==typeof self&&self||global,d=[null];function g(e,t){for(let n=e.length-1;n>=0;n--)"function"==typeof e[n]&&(e[n]=c(e[n],t+"_"+n));return e}function y(e){return!e||!1!==e.writable&&!("function"==typeof e.get&&void 0===e.set)}const v="undefined"!=typeof WorkerGlobalScope&&self instanceof WorkerGlobalScope,m=!("nw"in h)&&void 0!==h.process&&"[object process]"==={}.toString.call(h.process),k=!m&&!v&&!(!f||!p.HTMLElement),_=void 0!==h.process&&"[object process]"==={}.toString.call(h.process)&&!v&&!(!f||!p.HTMLElement),b={},T=function(e){if(!(e=e||h.event))return;let t=b[e.type];t||(t=b[e.type]=u("ON_PROPERTY"+e.type));const n=this||e.target||h,r=n[t];let o;if(k&&n===p&&"error"===e.type){const t=e;o=r&&r.call(this,t.message,t.filename,t.lineno,t.colno,t.error),!0===o&&e.preventDefault()}else o=r&&r.apply(this,arguments),null==o||o||e.preventDefault();return o};function w(n,r,o){let i=e(n,r);if(!i&&o&&e(o,r)&&(i={enumerable:!0,configurable:!0}),!i||!i.configurable)return;const s=u("on"+r+"patched");if(n.hasOwnProperty(s)&&n[s])return;delete i.writable,delete i.value;const a=i.get,c=i.set,l=r.substr(2);let f=b[l];f||(f=b[l]=u("ON_PROPERTY"+l)),i.set=function(e){let t=this;t||n!==h||(t=h),t&&(t[f]&&t.removeEventListener(l,T),c&&c.apply(t,d),"function"==typeof e?(t[f]=e,t.addEventListener(l,T,!1)):t[f]=null)},i.get=function(){let e=this;if(e||n!==h||(e=h),!e)return null;const t=e[f];if(t)return t;if(a){let t=a&&a.call(this);if(t)return i.set.call(this,t),"function"==typeof e.removeAttribute&&e.removeAttribute(r),t}return null},t(n,r,i),n[s]=!0}function E(e,t,n){if(t)for(let r=0;r<t.length;r++)w(e,"on"+t[r],n);else{const t=[];for(const n in e)"on"==n.substr(0,2)&&t.push(n);for(let r=0;r<t.length;r++)w(e,t[r],n)}}const S=u("originalInstance");function Z(e){const n=h[e];if(!n)return;h[u(e)]=n,h[e]=function(){const t=g(arguments,e);switch(t.length){case 0:this[S]=new n;break;case 1:this[S]=new n(t[0]);break;case 2:this[S]=new n(t[0],t[1]);break;case 3:this[S]=new n(t[0],t[1],t[2]);break;case 4:this[S]=new n(t[0],t[1],t[2],t[3]);break;default:throw new Error("Arg list too long.")}},P(h[e],n);const r=new n(function(){});let o;for(o in r)"XMLHttpRequest"===e&&"responseBlob"===o||function(n){"function"==typeof r[n]?h[e].prototype[n]=function(){return this[S][n].apply(this[S],arguments)}:t(h[e].prototype,n,{set:function(t){"function"==typeof t?(this[S][n]=c(t,e+"."+n),P(this[S][n],t)):this[S][n]=t},get:function(){return this[S][n]}})}(o);for(o in n)"prototype"!==o&&n.hasOwnProperty(o)&&(h[e][o]=n[o])}function D(t,r,o){let i=t;for(;i&&!i.hasOwnProperty(r);)i=n(i);!i&&t[r]&&(i=t);const s=u(r);let a=null;if(i&&!(a=i[s])&&(a=i[s]=i[r],y(i&&e(i,r)))){const e=o(a,s,r);i[r]=function(){return e(this,arguments)},P(i[r],a)}return a}function O(e,t,n){let r=null;function o(e){const t=e.data;return t.args[t.cbIdx]=function(){e.invoke.apply(this,arguments)},r.apply(t.target,t.args),e}r=D(e,t,e=>function(t,r){const i=n(t,r);return i.cbIdx>=0&&"function"==typeof r[i.cbIdx]?l(i.name,r[i.cbIdx],i,o):e.apply(t,r)})}function P(e,t){e[u("OriginalDelegate")]=t}let x=!1,C=!1;function j(){try{const e=p.navigator.userAgent;if(-1!==e.indexOf("MSIE ")||-1!==e.indexOf("Trident/"))return!0}catch(e){}return!1}function z(){if(x)return C;x=!0;try{const e=p.navigator.userAgent;-1===e.indexOf("MSIE ")&&-1===e.indexOf("Trident/")&&-1===e.indexOf("Edge/")||(C=!0)}catch(e){}return C}Zone.__load_patch("toString",e=>{const t=Function.prototype.toString,n=u("OriginalDelegate"),r=u("Promise"),o=u("Error"),i=function(){if("function"==typeof this){const i=this[n];if(i)return"function"==typeof i?t.call(i):Object.prototype.toString.call(i);if(this===Promise){const n=e[r];if(n)return t.call(n)}if(this===Error){const n=e[o];if(n)return t.call(n)}}return t.call(this)};i[n]=t,Function.prototype.toString=i;const s=Object.prototype.toString;Object.prototype.toString=function(){return this instanceof Promise?"[object Promise]":s.call(this)}});let I=!1;if("undefined"!=typeof window)try{const e=Object.defineProperty({},"passive",{get:function(){I=!0}});window.addEventListener("test",e,e),window.removeEventListener("test",e,e)}catch(ae){I=!1}const R={useG:!0},M={},A={},N=new RegExp("^"+a+"(\\w+)(true|false)$"),L=u("propagationStopped");function B(e,t){const n=(t?t(e):e)+"false",r=(t?t(e):e)+"true",o=a+n,i=a+r;M[e]={},M[e].false=o,M[e].true=i}function H(e,t,r){const o=r&&r.add||"addEventListener",i=r&&r.rm||"removeEventListener",s=r&&r.listeners||"eventListeners",c=r&&r.rmAll||"removeAllListeners",l=u(o),f="."+o+":",p=function(e,t,n){if(e.isRemoved)return;const r=e.callback;"object"==typeof r&&r.handleEvent&&(e.callback=e=>r.handleEvent(e),e.originalDelegate=r),e.invoke(e,t,[n]);const o=e.options;o&&"object"==typeof o&&o.once&&t[i].call(t,n.type,e.originalDelegate?e.originalDelegate:e.callback,o)},h=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,r=n[M[t.type].false];if(r)if(1===r.length)p(r[0],n,t);else{const e=r.slice();for(let r=0;r<e.length&&(!t||!0!==t[L]);r++)p(e[r],n,t)}},d=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,r=n[M[t.type].true];if(r)if(1===r.length)p(r[0],n,t);else{const e=r.slice();for(let r=0;r<e.length&&(!t||!0!==t[L]);r++)p(e[r],n,t)}};function g(t,r){if(!t)return!1;let p=!0;r&&void 0!==r.useG&&(p=r.useG);const g=r&&r.vh;let y=!0;r&&void 0!==r.chkDup&&(y=r.chkDup);let v=!1;r&&void 0!==r.rt&&(v=r.rt);let k=t;for(;k&&!k.hasOwnProperty(o);)k=n(k);if(!k&&t[o]&&(k=t),!k)return!1;if(k[l])return!1;const _=r&&r.eventNameToString,b={},T=k[l]=k[o],w=k[u(i)]=k[i],E=k[u(s)]=k[s],S=k[u(c)]=k[c];let Z;function D(e,t){return!I&&"object"==typeof e&&e?!!e.capture:I&&t?"boolean"==typeof e?{capture:e,passive:!0}:e?"object"==typeof e&&!1!==e.passive?Object.assign(Object.assign({},e),{passive:!0}):e:{passive:!0}:e}r&&r.prepend&&(Z=k[u(r.prepend)]=k[r.prepend]);const O=p?function(e){if(!b.isExisting)return T.call(b.target,b.eventName,b.capture?d:h,b.options)}:function(e){return T.call(b.target,b.eventName,e.invoke,b.options)},x=p?function(e){if(!e.isRemoved){const t=M[e.eventName];let n;t&&(n=t[e.capture?"true":"false"]);const r=n&&e.target[n];if(r)for(let o=0;o<r.length;o++)if(r[o]===e){r.splice(o,1),e.isRemoved=!0,0===r.length&&(e.allRemoved=!0,e.target[n]=null);break}}if(e.allRemoved)return w.call(e.target,e.eventName,e.capture?d:h,e.options)}:function(e){return w.call(e.target,e.eventName,e.invoke,e.options)},C=r&&r.diff?r.diff:function(e,t){const n=typeof t;return"function"===n&&e.callback===t||"object"===n&&e.originalDelegate===t},j=Zone[u("BLACK_LISTED_EVENTS")],z=e[u("PASSIVE_EVENTS")],L=function(t,n,o,i,s=!1,a=!1){return function(){const c=this||e;let l=arguments[0];r&&r.transferEventName&&(l=r.transferEventName(l));let u=arguments[1];if(!u)return t.apply(this,arguments);if(m&&"uncaughtException"===l)return t.apply(this,arguments);let f=!1;if("function"!=typeof u){if(!u.handleEvent)return t.apply(this,arguments);f=!0}if(g&&!g(t,u,c,arguments))return;const h=I&&!!z&&-1!==z.indexOf(l),d=D(arguments[2],h);if(j)for(let e=0;e<j.length;e++)if(l===j[e])return h?t.call(c,l,u,d):t.apply(this,arguments);const v=!!d&&("boolean"==typeof d||d.capture),k=!(!d||"object"!=typeof d)&&d.once,T=Zone.current;let w=M[l];w||(B(l,_),w=M[l]);const E=w[v?"true":"false"];let S,Z=c[E],O=!1;if(Z){if(O=!0,y)for(let e=0;e<Z.length;e++)if(C(Z[e],u))return}else Z=c[E]=[];const P=c.constructor.name,x=A[P];x&&(S=x[l]),S||(S=P+n+(_?_(l):l)),b.options=d,k&&(b.options.once=!1),b.target=c,b.capture=v,b.eventName=l,b.isExisting=O;const N=p?R:void 0;N&&(N.taskData=b);const L=T.scheduleEventTask(S,u,N,o,i);return b.target=null,N&&(N.taskData=null),k&&(d.once=!0),(I||"boolean"!=typeof L.options)&&(L.options=d),L.target=c,L.capture=v,L.eventName=l,f&&(L.originalDelegate=u),a?Z.unshift(L):Z.push(L),s?c:void 0}};return k[o]=L(T,f,O,x,v),Z&&(k.prependListener=L(Z,".prependListener:",function(e){return Z.call(b.target,b.eventName,e.invoke,b.options)},x,v,!0)),k[i]=function(){const t=this||e;let n=arguments[0];r&&r.transferEventName&&(n=r.transferEventName(n));const o=arguments[2],i=!!o&&("boolean"==typeof o||o.capture),s=arguments[1];if(!s)return w.apply(this,arguments);if(g&&!g(w,s,t,arguments))return;const c=M[n];let l;c&&(l=c[i?"true":"false"]);const u=l&&t[l];if(u)for(let e=0;e<u.length;e++){const r=u[e];if(C(r,s))return u.splice(e,1),r.isRemoved=!0,0===u.length&&(r.allRemoved=!0,t[l]=null,"string"==typeof n)&&(t[a+"ON_PROPERTY"+n]=null),r.zone.cancelTask(r),v?t:void 0}return w.apply(this,arguments)},k[s]=function(){const t=this||e;let n=arguments[0];r&&r.transferEventName&&(n=r.transferEventName(n));const o=[],i=F(t,_?_(n):n);for(let e=0;e<i.length;e++){const t=i[e];o.push(t.originalDelegate?t.originalDelegate:t.callback)}return o},k[c]=function(){const t=this||e;let n=arguments[0];if(n){r&&r.transferEventName&&(n=r.transferEventName(n));const e=M[n];if(e){const r=t[e.false],o=t[e.true];if(r){const e=r.slice();for(let t=0;t<e.length;t++){const r=e[t];this[i].call(this,n,r.originalDelegate?r.originalDelegate:r.callback,r.options)}}if(o){const e=o.slice();for(let t=0;t<e.length;t++){const r=e[t];this[i].call(this,n,r.originalDelegate?r.originalDelegate:r.callback,r.options)}}}}else{const e=Object.keys(t);for(let t=0;t<e.length;t++){const n=N.exec(e[t]);let r=n&&n[1];r&&"removeListener"!==r&&this[c].call(this,r)}this[c].call(this,"removeListener")}if(v)return this},P(k[o],T),P(k[i],w),S&&P(k[c],S),E&&P(k[s],E),!0}let y=[];for(let n=0;n<t.length;n++)y[n]=g(t[n],r);return y}function F(e,t){if(!t){const n=[];for(let r in e){const o=N.exec(r);let i=o&&o[1];if(i&&(!t||i===t)){const t=e[r];if(t)for(let e=0;e<t.length;e++)n.push(t[e])}}return n}let n=M[t];n||(B(t),n=M[t]);const r=e[n.false],o=e[n.true];return r?o?r.concat(o):r.slice():o?o.slice():[]}function G(e,t){const n=e.Event;n&&n.prototype&&t.patchMethod(n.prototype,"stopImmediatePropagation",e=>function(t,n){t[L]=!0,e&&e.apply(t,n)})}function U(e,t,n,r,o){const i=Zone.__symbol__(r);if(t[i])return;const s=t[i]=t[r];t[r]=function(i,a,c){return a&&a.prototype&&o.forEach(function(t){const o=`${n}.${r}::`+t,i=a.prototype;if(i.hasOwnProperty(t)){const n=e.ObjectGetOwnPropertyDescriptor(i,t);n&&n.value?(n.value=e.wrapWithCurrentZone(n.value,o),e._redefineProperty(a.prototype,t,n)):i[t]&&(i[t]=e.wrapWithCurrentZone(i[t],o))}else i[t]&&(i[t]=e.wrapWithCurrentZone(i[t],o))}),s.call(t,i,a,c)},e.attachOriginToPatched(t[r],s)}const V=["absolutedeviceorientation","afterinput","afterprint","appinstalled","beforeinstallprompt","beforeprint","beforeunload","devicelight","devicemotion","deviceorientation","deviceorientationabsolute","deviceproximity","hashchange","languagechange","message","mozbeforepaint","offline","online","paint","pageshow","pagehide","popstate","rejectionhandled","storage","unhandledrejection","unload","userproximity","vrdisplayconnected","vrdisplaydisconnected","vrdisplaypresentchange"],W=["encrypted","waitingforkey","msneedkey","mozinterruptbegin","mozinterruptend"],Y=["load"],X=["blur","error","focus","load","resize","scroll","messageerror"],q=["bounce","finish","start"],K=["loadstart","progress","abort","error","load","progress","timeout","loadend","readystatechange"],J=["upgradeneeded","complete","abort","success","error","blocked","versionchange","close"],Q=["close","error","open","message"],$=["error","message"],ee=["abort","animationcancel","animationend","animationiteration","auxclick","beforeinput","blur","cancel","canplay","canplaythrough","change","compositionstart","compositionupdate","compositionend","cuechange","click","close","contextmenu","curechange","dblclick","drag","dragend","dragenter","dragexit","dragleave","dragover","drop","durationchange","emptied","ended","error","focus","focusin","focusout","gotpointercapture","input","invalid","keydown","keypress","keyup","load","loadstart","loadeddata","loadedmetadata","lostpointercapture","mousedown","mouseenter","mouseleave","mousemove","mouseout","mouseover","mouseup","mousewheel","orientationchange","pause","play","playing","pointercancel","pointerdown","pointerenter","pointerleave","pointerlockchange","mozpointerlockchange","webkitpointerlockerchange","pointerlockerror","mozpointerlockerror","webkitpointerlockerror","pointermove","pointout","pointerover","pointerup","progress","ratechange","reset","resize","scroll","seeked","seeking","select","selectionchange","selectstart","show","sort","stalled","submit","suspend","timeupdate","volumechange","touchcancel","touchmove","touchstart","touchend","transitioncancel","transitionend","waiting","wheel"].concat(["webglcontextrestored","webglcontextlost","webglcontextcreationerror"],["autocomplete","autocompleteerror"],["toggle"],["afterscriptexecute","beforescriptexecute","DOMContentLoaded","freeze","fullscreenchange","mozfullscreenchange","webkitfullscreenchange","msfullscreenchange","fullscreenerror","mozfullscreenerror","webkitfullscreenerror","msfullscreenerror","readystatechange","visibilitychange","resume"],V,["beforecopy","beforecut","beforepaste","copy","cut","paste","dragstart","loadend","animationstart","search","transitionrun","transitionstart","webkitanimationend","webkitanimationiteration","webkitanimationstart","webkittransitionend"],["activate","afterupdate","ariarequest","beforeactivate","beforedeactivate","beforeeditfocus","beforeupdate","cellchange","controlselect","dataavailable","datasetchanged","datasetcomplete","errorupdate","filterchange","layoutcomplete","losecapture","move","moveend","movestart","propertychange","resizeend","resizestart","rowenter","rowexit","rowsdelete","rowsinserted","command","compassneedscalibration","deactivate","help","mscontentzoom","msmanipulationstatechanged","msgesturechange","msgesturedoubletap","msgestureend","msgesturehold","msgesturestart","msgesturetap","msgotpointercapture","msinertiastart","mslostpointercapture","mspointercancel","mspointerdown","mspointerenter","mspointerhover","mspointerleave","mspointermove","mspointerout","mspointerover","mspointerup","pointerout","mssitemodejumplistitemremoved","msthumbnailclick","stop","storagecommit"]);function te(e,t,n){if(!n||0===n.length)return t;const r=n.filter(t=>t.target===e);if(!r||0===r.length)return t;const o=r[0].ignoreProperties;return t.filter(e=>-1===o.indexOf(e))}function ne(e,t,n,r){e&&E(e,te(e,t,n),r)}function re(e,t){if(m&&!_)return;if(Zone[e.symbol("patchEvents")])return;const r="undefined"!=typeof WebSocket,o=t.__Zone_ignore_on_properties;if(k){const e=window,t=j?[{target:e,ignoreProperties:["error"]}]:[];ne(e,ee.concat(["messageerror"]),o?o.concat(t):o,n(e)),ne(Document.prototype,ee,o),void 0!==e.SVGElement&&ne(e.SVGElement.prototype,ee,o),ne(Element.prototype,ee,o),ne(HTMLElement.prototype,ee,o),ne(HTMLMediaElement.prototype,W,o),ne(HTMLFrameSetElement.prototype,V.concat(X),o),ne(HTMLBodyElement.prototype,V.concat(X),o),ne(HTMLFrameElement.prototype,Y,o),ne(HTMLIFrameElement.prototype,Y,o);const r=e.HTMLMarqueeElement;r&&ne(r.prototype,q,o);const i=e.Worker;i&&ne(i.prototype,$,o)}const i=t.XMLHttpRequest;i&&ne(i.prototype,K,o);const s=t.XMLHttpRequestEventTarget;s&&ne(s&&s.prototype,K,o),"undefined"!=typeof IDBIndex&&(ne(IDBIndex.prototype,J,o),ne(IDBRequest.prototype,J,o),ne(IDBOpenDBRequest.prototype,J,o),ne(IDBDatabase.prototype,J,o),ne(IDBTransaction.prototype,J,o),ne(IDBCursor.prototype,J,o)),r&&ne(WebSocket.prototype,Q,o)}Zone.__load_patch("util",(n,i,s)=>{s.patchOnProperties=E,s.patchMethod=D,s.bindArguments=g,s.patchMacroTask=O;const l=i.__symbol__("BLACK_LISTED_EVENTS"),u=i.__symbol__("UNPATCHED_EVENTS");n[u]&&(n[l]=n[u]),n[l]&&(i[l]=i[u]=n[l]),s.patchEventPrototype=G,s.patchEventTarget=H,s.isIEOrEdge=z,s.ObjectDefineProperty=t,s.ObjectGetOwnPropertyDescriptor=e,s.ObjectCreate=r,s.ArraySlice=o,s.patchClass=Z,s.wrapWithCurrentZone=c,s.filterProperties=te,s.attachOriginToPatched=P,s._redefineProperty=Object.defineProperty,s.patchCallbacks=U,s.getGlobalObjects=()=>({globalSources:A,zoneSymbolEventNames:M,eventNames:ee,isBrowser:k,isMix:_,isNode:m,TRUE_STR:"true",FALSE_STR:"false",ZONE_SYMBOL_PREFIX:a,ADD_EVENT_LISTENER_STR:"addEventListener",REMOVE_EVENT_LISTENER_STR:"removeEventListener"})});const oe=u("zoneTask");function ie(e,t,n,r){let o=null,i=null;n+=r;const s={};function a(t){const n=t.data;return n.args[0]=function(){try{t.invoke.apply(this,arguments)}finally{t.data&&t.data.isPeriodic||("number"==typeof n.handleId?delete s[n.handleId]:n.handleId&&(n.handleId[oe]=null))}},n.handleId=o.apply(e,n.args),t}function c(e){return i(e.data.handleId)}o=D(e,t+=r,n=>function(o,i){if("function"==typeof i[0]){const e=l(t,i[0],{isPeriodic:"Interval"===r,delay:"Timeout"===r||"Interval"===r?i[1]||0:void 0,args:i},a,c);if(!e)return e;const n=e.data.handleId;return"number"==typeof n?s[n]=e:n&&(n[oe]=e),n&&n.ref&&n.unref&&"function"==typeof n.ref&&"function"==typeof n.unref&&(e.ref=n.ref.bind(n),e.unref=n.unref.bind(n)),"number"==typeof n||n?n:e}return n.apply(e,i)}),i=D(e,n,t=>function(n,r){const o=r[0];let i;"number"==typeof o?i=s[o]:(i=o&&o[oe],i||(i=o)),i&&"string"==typeof i.type?"notScheduled"!==i.state&&(i.cancelFn&&i.data.isPeriodic||0===i.runCount)&&("number"==typeof o?delete s[o]:o&&(o[oe]=null),i.zone.cancelTask(i)):t.apply(e,r)})}function se(e,t){if(Zone[t.symbol("patchEventTarget")])return;const{eventNames:n,zoneSymbolEventNames:r,TRUE_STR:o,FALSE_STR:i,ZONE_SYMBOL_PREFIX:s}=t.getGlobalObjects();for(let c=0;c<n.length;c++){const e=n[c],t=s+(e+i),a=s+(e+o);r[e]={},r[e][i]=t,r[e][o]=a}const a=e.EventTarget;return a&&a.prototype?(t.patchEventTarget(e,[a&&a.prototype]),!0):void 0}Zone.__load_patch("legacy",e=>{const t=e[Zone.__symbol__("legacyPatch")];t&&t()}),Zone.__load_patch("timers",e=>{ie(e,"set","clear","Timeout"),ie(e,"set","clear","Interval"),ie(e,"set","clear","Immediate")}),Zone.__load_patch("requestAnimationFrame",e=>{ie(e,"request","cancel","AnimationFrame"),ie(e,"mozRequest","mozCancel","AnimationFrame"),ie(e,"webkitRequest","webkitCancel","AnimationFrame")}),Zone.__load_patch("blocking",(e,t)=>{const n=["alert","prompt","confirm"];for(let r=0;r<n.length;r++)D(e,n[r],(n,r,o)=>function(r,i){return t.current.run(n,e,i,o)})}),Zone.__load_patch("EventTarget",(e,t,n)=>{(function(e,t){t.patchEventPrototype(e,t)})(e,n),se(e,n);const r=e.XMLHttpRequestEventTarget;r&&r.prototype&&n.patchEventTarget(e,[r.prototype]),Z("MutationObserver"),Z("WebKitMutationObserver"),Z("IntersectionObserver"),Z("FileReader")}),Zone.__load_patch("on_property",(e,t,n)=>{re(n,e)}),Zone.__load_patch("customElements",(e,t,n)=>{!function(e,t){const{isBrowser:n,isMix:r}=t.getGlobalObjects();(n||r)&&e.customElements&&"customElements"in e&&t.patchCallbacks(t,e.customElements,"customElements","define",["connectedCallback","disconnectedCallback","adoptedCallback","attributeChangedCallback"])}(e,n)}),Zone.__load_patch("XHR",(e,t)=>{!function(e){const p=e.XMLHttpRequest;if(!p)return;const h=p.prototype;let d=h[i],g=h[s];if(!d){const t=e.XMLHttpRequestEventTarget;if(t){const e=t.prototype;d=e[i],g=e[s]}}function y(e){const r=e.data,c=r.target;c[a]=!1,c[f]=!1;const l=c[o];d||(d=c[i],g=c[s]),l&&g.call(c,"readystatechange",l);const u=c[o]=()=>{if(c.readyState===c.DONE)if(!r.aborted&&c[a]&&"scheduled"===e.state){const n=c[t.__symbol__("loadfalse")];if(n&&n.length>0){const o=e.invoke;e.invoke=function(){const n=c[t.__symbol__("loadfalse")];for(let t=0;t<n.length;t++)n[t]===e&&n.splice(t,1);r.aborted||"scheduled"!==e.state||o.call(e)},n.push(e)}else e.invoke()}else r.aborted||!1!==c[a]||(c[f]=!0)};return d.call(c,"readystatechange",u),c[n]||(c[n]=e),T.apply(c,r.args),c[a]=!0,e}function v(){}function m(e){const t=e.data;return t.aborted=!0,w.apply(t.target,t.args)}const k=D(h,"open",()=>function(e,t){return e[r]=0==t[2],e[c]=t[1],k.apply(e,t)}),_=u("fetchTaskAborting"),b=u("fetchTaskScheduling"),T=D(h,"send",()=>function(e,n){if(!0===t.current[b])return T.apply(e,n);if(e[r])return T.apply(e,n);{const t={target:e,url:e[c],isPeriodic:!1,args:n,aborted:!1},r=l("XMLHttpRequest.send",v,t,y,m);e&&!0===e[f]&&!t.aborted&&"scheduled"===r.state&&r.invoke()}}),w=D(h,"abort",()=>function(e,r){const o=e[n];if(o&&"string"==typeof o.type){if(null==o.cancelFn||o.data&&o.data.aborted)return;o.zone.cancelTask(o)}else if(!0===t.current[_])return w.apply(e,r)})}(e);const n=u("xhrTask"),r=u("xhrSync"),o=u("xhrListener"),a=u("xhrScheduled"),c=u("xhrURL"),f=u("xhrErrorBeforeScheduled")}),Zone.__load_patch("geolocation",t=>{t.navigator&&t.navigator.geolocation&&function(t,n){const r=t.constructor.name;for(let o=0;o<n.length;o++){const i=n[o],s=t[i];if(s){if(!y(e(t,i)))continue;t[i]=(e=>{const t=function(){return e.apply(this,g(arguments,r+"."+i))};return P(t,e),t})(s)}}}(t.navigator.geolocation,["getCurrentPosition","watchPosition"])}),Zone.__load_patch("PromiseRejectionEvent",(e,t)=>{function n(t){return function(n){F(e,t).forEach(r=>{const o=e.PromiseRejectionEvent;if(o){const e=new o(t,{promise:n.promise,reason:n.rejection});r.invoke(e)}})}}e.PromiseRejectionEvent&&(t[u("unhandledPromiseRejectionHandler")]=n("unhandledrejection"),t[u("rejectionHandledHandler")]=n("rejectionhandled"))})})?r.call(t,n,t,e):r)||(e.exports=o)},pg82:function(e,t){var n=null,r=null;function o(e,t,n){e.addEventListener(t,function(e){var o=new MouseEvent(n,e);o.pointerId=1,o.isPrimary=!0,o.pointerType="mouse",o.width=1,o.height=1,o.tiltX=0,o.tiltY=0,o.pressure="buttons"in e&&0!==e.buttons?.5:0;var i=e.target;null!==r&&(i=r,"mouseup"===t&&(r=null)),i.dispatchEvent(o),o.defaultPrevented&&e.preventDefault()})}function i(e,t,r){e.addEventListener(t,function(e){for(var o=e.changedTouches,i=o.length,s=0;s<i;s++){var a=new CustomEvent(r,{bubbles:!0,cancelable:!0});a.ctrlKey=e.ctrlKey,a.shiftKey=e.shiftKey,a.altKey=e.altKey,a.metaKey=e.metaKey;var c=o.item(s);a.clientX=c.clientX,a.clientY=c.clientY,a.screenX=c.screenX,a.screenY=c.screenY,a.pageX=c.pageX,a.pageY=c.pageY;var l=c.target.getBoundingClientRect();a.offsetX=c.clientX-l.left,a.offsetY=c.clientY-l.top,a.pointerId=1+c.identifier,a.button=0,a.buttons=1,a.movementX=0,a.movementY=0,a.region=null,a.relatedTarget=null,a.x=a.clientX,a.y=a.clientY,a.pointerType="touch",a.width=1,a.height=1,a.tiltX=0,a.tiltY=0,a.pressure=1,"touchstart"===t&&null===n&&(n=c.identifier),a.isPrimary=c.identifier===n,"touchend"===t&&a.isPrimary&&(n=null),e.target.dispatchEvent(a),a.defaultPrevented&&e.preventDefault()}})}"PointerEvent"in window||(Element.prototype.setPointerCapture=Element.prototype.setCapture,Element.prototype.releasePointerCapture=Element.prototype.releaseCapture,"TouchEvent"in window||(o(document,"mousedown","pointerdown"),o(document,"mousemove","pointermove"),o(document,"mouseup","pointerup")),i(document,"touchstart","pointerdown"),i(document,"touchmove","pointermove"),i(document,"touchend","pointerup"))},ppGB:function(e,t){var n=Math.ceil,r=Math.floor;e.exports=function(e){return isNaN(e=+e)?0:(e>0?r:n)(e)}},rmf8:function(e,t,n){var r=n("KPYQ");e.exports=r},sQkB:function(e,t,n){var r=n("2oRo"),o=n("A2ZE"),i=Function.call;e.exports=function(e,t,n){return o(i,r[e].prototype[t],n)}},tiKp:function(e,t,n){var r=n("2oRo"),o=n("VpIT"),i=n("UTVS"),s=n("kOOl"),a=n("STAE"),c=n("/b8u"),l=o("wks"),u=r.Symbol,f=c?u:u&&u.withoutSetter||s;e.exports=function(e){return i(l,e)||(l[e]=a&&i(u,e)?u[e]:f("Symbol."+e)),l[e]}},wE6v:function(e,t,n){var r=n("hh1v");e.exports=function(e,t){if(!r(e))return e;var n,o;if(t&&"function"==typeof(n=e.toString)&&!r(o=n.call(e)))return o;if("function"==typeof(n=e.valueOf)&&!r(o=n.call(e)))return o;if(!t&&"function"==typeof(n=e.toString)&&!r(o=n.call(e)))return o;throw TypeError("Can't convert object to primitive value")}},xDBR:function(e,t){e.exports=!1},xrYK:function(e,t){var n={}.toString;e.exports=function(e){return n.call(e).slice(8,-1)}},xs3f:function(e,t,n){var r=n("2oRo"),o=n("zk60"),i=r["__core-js_shared__"]||o("__core-js_shared__",{});e.exports=i},yoRg:function(e,t,n){var r=n("UTVS"),o=n("/GqU"),i=n("TWQb").indexOf,s=n("0BK2");e.exports=function(e,t){var n,a=o(e),c=0,l=[];for(n in a)!r(s,n)&&r(a,n)&&l.push(n);for(;t.length>c;)r(a,n=t[c++])&&(~i(l,n)||l.push(n));return l}},zBJ4:function(e,t,n){var r=n("2oRo"),o=n("hh1v"),i=r.document,s=o(i)&&o(i.createElement);e.exports=function(e){return s?i.createElement(e):{}}},zk60:function(e,t,n){var r=n("2oRo"),o=n("kRJp");e.exports=function(e,t){try{o(r,e,t)}catch(n){r[e]=t}return t}}}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class a{constructor(e,t){this._parent=e,this._name=t?t.name||"unnamed":"<root>",this._properties=t&&t.properties||{},this._zoneDelegate=new l(this,this._parent&&this._parent._zoneDelegate,t)}static assertZonePatched(){if(e.Promise!==P.ZoneAwarePromise)throw new Error("Zone.js has detected that ZoneAwarePromise `(window|global).Promise` has been overwritten.\nMost likely cause is that a Promise polyfill has been loaded after Zone.js (Polyfilling Promise api is not necessary when zone.js is loaded. If you must load one, do so before loading zone.js.)")}static get root(){let e=a.current;for(;e.parent;)e=e.parent;return e}static get current(){return C.zone}static get currentTask(){return j}static __load_patch(t,o){if(P.hasOwnProperty(t)){if(s)throw Error("Already loaded patch: "+t)}else if(!e["__Zone_disable_"+t]){const i="Zone:"+t;n(i),P[t]=o(e,a,x),r(i,i)}}get parent(){return this._parent}get name(){return this._name}get(e){const t=this.getZoneWith(e);if(t)return t._properties[e]}getZoneWith(e){let t=this;for(;t;){if(t._properties.hasOwnProperty(e))return t;t=t._parent}return null}fork(e){if(!e)throw new Error("ZoneSpec required!");return this._zoneDelegate.fork(this,e)}wrap(e,t){if("function"!=typeof e)throw new Error("Expecting function got: "+e);const n=this._zoneDelegate.intercept(this,e,t),r=this;return function(){return r.runGuarded(n,this,arguments,t)}}run(e,t,n,r){C={parent:C,zone:this};try{return this._zoneDelegate.invoke(this,e,t,n,r)}finally{C=C.parent}}runGuarded(e,t=null,n,r){C={parent:C,zone:this};try{try{return this._zoneDelegate.invoke(this,e,t,n,r)}catch(o){if(this._zoneDelegate.handleError(this,o))throw o}}finally{C=C.parent}}runTask(e,t,n){if(e.zone!=this)throw new Error("A task can only be run in the zone of creation! (Creation: "+(e.zone||k).name+"; Execution: "+this.name+")");if(e.state===_&&(e.type===O||e.type===D))return;const r=e.state!=w;r&&e._transitionTo(w,T),e.runCount++;const o=j;j=e,C={parent:C,zone:this};try{e.type==D&&e.data&&!e.data.isPeriodic&&(e.cancelFn=void 0);try{return this._zoneDelegate.invokeTask(this,e,t,n)}catch(i){if(this._zoneDelegate.handleError(this,i))throw i}}finally{e.state!==_&&e.state!==S&&(e.type==O||e.data&&e.data.isPeriodic?r&&e._transitionTo(T,w):(e.runCount=0,this._updateTaskCount(e,-1),r&&e._transitionTo(_,w,_))),C=C.parent,j=o}}scheduleTask(e){if(e.zone&&e.zone!==this){let t=this;for(;t;){if(t===e.zone)throw Error(`can not reschedule task to ${this.name} which is descendants of the original zone ${e.zone.name}`);t=t.parent}}e._transitionTo(b,_);const t=[];e._zoneDelegates=t,e._zone=this;try{e=this._zoneDelegate.scheduleTask(this,e)}catch(n){throw e._transitionTo(S,b,_),this._zoneDelegate.handleError(this,n),n}return e._zoneDelegates===t&&this._updateTaskCount(e,1),e.state==b&&e._transitionTo(T,b),e}scheduleMicroTask(e,t,n,r){return this.scheduleTask(new u(Z,e,t,n,r,void 0))}scheduleMacroTask(e,t,n,r,o){return this.scheduleTask(new u(D,e,t,n,r,o))}scheduleEventTask(e,t,n,r,o){return this.scheduleTask(new u(O,e,t,n,r,o))}cancelTask(e){if(e.zone!=this)throw new Error("A task can only be cancelled in the zone of creation! (Creation: "+(e.zone||k).name+"; Execution: "+this.name+")");e._transitionTo(E,T,w);try{this._zoneDelegate.cancelTask(this,e)}catch(t){throw e._transitionTo(S,E),this._zoneDelegate.handleError(this,t),t}return this._updateTaskCount(e,-1),e._transitionTo(_,E),e.runCount=0,e}_updateTaskCount(e,t){const n=e._zoneDelegates;-1==t&&(e._zoneDelegates=null);for(let r=0;r<n.length;r++)n[r]._updateTaskCount(e.type,t)}}a.__symbol__=i;const c={name:"",onHasTask:(e,t,n,r)=>e.hasTask(n,r),onScheduleTask:(e,t,n,r)=>e.scheduleTask(n,r),onInvokeTask:(e,t,n,r,o,i)=>e.invokeTask(n,r,o,i),onCancelTask:(e,t,n,r)=>e.cancelTask(n,r)};class l{constructor(e,t,n){this._taskCounts={microTask:0,macroTask:0,eventTask:0},this.zone=e,this._parentDelegate=t,this._forkZS=n&&(n&&n.onFork?n:t._forkZS),this._forkDlgt=n&&(n.onFork?t:t._forkDlgt),this._forkCurrZone=n&&(n.onFork?this.zone:t._forkCurrZone),this._interceptZS=n&&(n.onIntercept?n:t._interceptZS),this._interceptDlgt=n&&(n.onIntercept?t:t._interceptDlgt),this._interceptCurrZone=n&&(n.onIntercept?this.zone:t._interceptCurrZone),this._invokeZS=n&&(n.onInvoke?n:t._invokeZS),this._invokeDlgt=n&&(n.onInvoke?t:t._invokeDlgt),this._invokeCurrZone=n&&(n.onInvoke?this.zone:t._invokeCurrZone),this._handleErrorZS=n&&(n.onHandleError?n:t._handleErrorZS),this._handleErrorDlgt=n&&(n.onHandleError?t:t._handleErrorDlgt),this._handleErrorCurrZone=n&&(n.onHandleError?this.zone:t._handleErrorCurrZone),this._scheduleTaskZS=n&&(n.onScheduleTask?n:t._scheduleTaskZS),this._scheduleTaskDlgt=n&&(n.onScheduleTask?t:t._scheduleTaskDlgt),this._scheduleTaskCurrZone=n&&(n.onScheduleTask?this.zone:t._scheduleTaskCurrZone),this._invokeTaskZS=n&&(n.onInvokeTask?n:t._invokeTaskZS),this._invokeTaskDlgt=n&&(n.onInvokeTask?t:t._invokeTaskDlgt),this._invokeTaskCurrZone=n&&(n.onInvokeTask?this.zone:t._invokeTaskCurrZone),this._cancelTaskZS=n&&(n.onCancelTask?n:t._cancelTaskZS),this._cancelTaskDlgt=n&&(n.onCancelTask?t:t._cancelTaskDlgt),this._cancelTaskCurrZone=n&&(n.onCancelTask?this.zone:t._cancelTaskCurrZone),this._hasTaskZS=null,this._hasTaskDlgt=null,this._hasTaskDlgtOwner=null,this._hasTaskCurrZone=null;const r=n&&n.onHasTask;(r||t&&t._hasTaskZS)&&(this._hasTaskZS=r?n:c,this._hasTaskDlgt=t,this._hasTaskDlgtOwner=this,this._hasTaskCurrZone=e,n.onScheduleTask||(this._scheduleTaskZS=c,this._scheduleTaskDlgt=t,this._scheduleTaskCurrZone=this.zone),n.onInvokeTask||(this._invokeTaskZS=c,this._invokeTaskDlgt=t,this._invokeTaskCurrZone=this.zone),n.onCancelTask||(this._cancelTaskZS=c,this._cancelTaskDlgt=t,this._cancelTaskCurrZone=this.zone))}fork(e,t){return this._forkZS?this._forkZS.onFork(this._forkDlgt,this.zone,e,t):new a(e,t)}intercept(e,t,n){return this._interceptZS?this._interceptZS.onIntercept(this._interceptDlgt,this._interceptCurrZone,e,t,n):t}invoke(e,t,n,r,o){return this._invokeZS?this._invokeZS.onInvoke(this._invokeDlgt,this._invokeCurrZone,e,t,n,r,o):t.apply(n,r)}handleError(e,t){return!this._handleErrorZS||this._handleErrorZS.onHandleError(this._handleErrorDlgt,this._handleErrorCurrZone,e,t)}scheduleTask(e,t){let n=t;if(this._scheduleTaskZS)this._hasTaskZS&&n._zoneDelegates.push(this._hasTaskDlgtOwner),n=this._scheduleTaskZS.onScheduleTask(this._scheduleTaskDlgt,this._scheduleTaskCurrZone,e,t),n||(n=t);else if(t.scheduleFn)t.scheduleFn(t);else{if(t.type!=Z)throw new Error("Task is missing scheduleFn.");v(t)}return n}invokeTask(e,t,n,r){return this._invokeTaskZS?this._invokeTaskZS.onInvokeTask(this._invokeTaskDlgt,this._invokeTaskCurrZone,e,t,n,r):t.callback.apply(n,r)}cancelTask(e,t){let n;if(this._cancelTaskZS)n=this._cancelTaskZS.onCancelTask(this._cancelTaskDlgt,this._cancelTaskCurrZone,e,t);else{if(!t.cancelFn)throw Error("Task is not cancelable");n=t.cancelFn(t)}return n}hasTask(e,t){try{this._hasTaskZS&&this._hasTaskZS.onHasTask(this._hasTaskDlgt,this._hasTaskCurrZone,e,t)}catch(n){this.handleError(e,n)}}_updateTaskCount(e,t){const n=this._taskCounts,r=n[e],o=n[e]=r+t;if(o<0)throw new Error("More tasks executed then were scheduled.");0!=r&&0!=o||this.hasTask(this.zone,{microTask:n.microTask>0,macroTask:n.macroTask>0,eventTask:n.eventTask>0,change:e})}}class u{constructor(t,n,r,o,i,s){if(this._zone=null,this.runCount=0,this._zoneDelegates=null,this._state="notScheduled",this.type=t,this.source=n,this.data=o,this.scheduleFn=i,this.cancelFn=s,!r)throw new Error("callback is not defined");this.callback=r;const a=this;this.invoke=t===O&&o&&o.useG?u.invokeTask:function(){return u.invokeTask.call(e,a,this,arguments)}}static invokeTask(e,t,n){e||(e=this),z++;try{return e.runCount++,e.zone.runTask(e,t,n)}finally{1==z&&m(),z--}}get zone(){return this._zone}get state(){return this._state}cancelScheduleRequest(){this._transitionTo(_,b)}_transitionTo(e,t,n){if(this._state!==t&&this._state!==n)throw new Error(`${this.type} '${this.source}': can not transition to '${e}', expecting state '${t}'${n?" or '"+n+"'":""}, was '${this._state}'.`);this._state=e,e==_&&(this._zoneDelegates=null)}toString(){return this.data&&void 0!==this.data.handleId?this.data.handleId.toString():Object.prototype.toString.call(this)}toJSON(){return{type:this.type,state:this.state,source:this.source,zone:this.zone.name,runCount:this.runCount}}}const f=i("setTimeout"),p=i("Promise"),h=i("then");let d,g=[],y=!1;function v(t){if(0===z&&0===g.length)if(d||e[p]&&(d=e[p].resolve(0)),d){let e=d[h];e||(e=d.then),e.call(d,m)}else e[f](m,0);t&&g.push(t)}function m(){if(!y){for(y=!0;g.length;){const t=g;g=[];for(let n=0;n<t.length;n++){const r=t[n];try{r.zone.runTask(r,null,null)}catch(e){x.onUnhandledError(e)}}}x.microtaskDrainDone(),y=!1}}const k={name:"NO ZONE"},_="notScheduled",b="scheduling",T="scheduled",w="running",E="canceling",S="unknown",Z="microTask",D="macroTask",O="eventTask",P={},x={symbol:i,currentZoneFrame:()=>C,onUnhandledError:I,microtaskDrainDone:I,scheduleMicroTask:v,showUncaughtError:()=>!a[i("ignoreConsoleErrorUncaughtError")],patchEventTarget:()=>[],patchOnProperties:I,patchMethod:()=>I,bindArguments:()=>[],patchThen:()=>I,patchMacroTask:()=>I,setNativePromise:e=>{e&&"function"==typeof e.resolve&&(d=e.resolve(0))},patchEventPrototype:()=>I,isIEOrEdge:()=>!1,getGlobalObjects:()=>{},ObjectDefineProperty:()=>I,ObjectGetOwnPropertyDescriptor:()=>{},ObjectCreate:()=>{},ArraySlice:()=>[],patchClass:()=>I,wrapWithCurrentZone:()=>I,filterProperties:()=>[],attachOriginToPatched:()=>I,_redefineProperty:()=>I,patchCallbacks:()=>I};let C={parent:null,zone:new a(null,null)},j=null,z=0;function I(){}r("Zone","Zone"),e.Zone=a}("undefined"!=typeof window&&window||"undefined"!=typeof self&&self||global),Zone.__load_patch("ZoneAwarePromise",(e,t,n)=>{const r=Object.getOwnPropertyDescriptor,o=Object.defineProperty,i=n.symbol,s=[],a=!0===e[i("DISABLE_WRAPPING_UNCAUGHT_PROMISE_REJECTION")],c=i("Promise"),l=i("then");n.onUnhandledError=e=>{if(n.showUncaughtError()){const t=e&&e.rejection;t?console.error("Unhandled Promise rejection:",t instanceof Error?t.message:t,"; Zone:",e.zone.name,"; Task:",e.task&&e.task.source,"; Value:",t,t instanceof Error?t.stack:void 0):console.error(e)}},n.microtaskDrainDone=()=>{for(;s.length;){const t=s.shift();try{t.zone.runGuarded(()=>{throw t})}catch(e){f(e)}}};const u=i("unhandledPromiseRejectionHandler");function f(e){n.onUnhandledError(e);try{const n=t[u];"function"==typeof n&&n.call(this,e)}catch(r){}}function p(e){return e&&e.then}function h(e){return e}function d(e){return D.reject(e)}const g=i("state"),y=i("value"),v=i("finally"),m=i("parentPromiseValue"),k=i("parentPromiseState");function _(e,t){return n=>{try{T(e,t,n)}catch(r){T(e,!1,r)}}}const b=i("currentTaskTrace");function T(e,r,i){const c=function(){let e=!1;return function(t){return function(){e||(e=!0,t.apply(null,arguments))}}}();if(e===i)throw new TypeError("Promise resolved with itself");if(null===e[g]){let f=null;try{"object"!=typeof i&&"function"!=typeof i||(f=i&&i.then)}catch(u){return c(()=>{T(e,!1,u)})(),e}if(!1!==r&&i instanceof D&&i.hasOwnProperty(g)&&i.hasOwnProperty(y)&&null!==i[g])E(i),T(e,i[g],i[y]);else if(!1!==r&&"function"==typeof f)try{f.call(i,c(_(e,r)),c(_(e,!1)))}catch(u){c(()=>{T(e,!1,u)})()}else{e[g]=r;const c=e[y];if(e[y]=i,e[v]===v&&!0===r&&(e[g]=e[k],e[y]=e[m]),!1===r&&i instanceof Error){const e=t.currentTask&&t.currentTask.data&&t.currentTask.data.__creationTrace__;e&&o(i,b,{configurable:!0,enumerable:!1,writable:!0,value:e})}for(let t=0;t<c.length;)S(e,c[t++],c[t++],c[t++],c[t++]);if(0==c.length&&0==r){e[g]=0;let r=i;if(!a)try{throw new Error("Uncaught (in promise): "+((l=i)&&l.toString===Object.prototype.toString?(l.constructor&&l.constructor.name||"")+": "+JSON.stringify(l):l?l.toString():Object.prototype.toString.call(l))+(i&&i.stack?"\n"+i.stack:""))}catch(u){r=u}r.rejection=i,r.promise=e,r.zone=t.current,r.task=t.currentTask,s.push(r),n.scheduleMicroTask()}}}var l;return e}const w=i("rejectionHandledHandler");function E(e){if(0===e[g]){try{const n=t[w];n&&"function"==typeof n&&n.call(this,{rejection:e[y],promise:e})}catch(n){}e[g]=!1;for(let t=0;t<s.length;t++)e===s[t].promise&&s.splice(t,1)}}function S(e,t,n,r,o){E(e);const i=e[g],s=i?"function"==typeof r?r:h:"function"==typeof o?o:d;t.scheduleMicroTask("Promise.then",()=>{try{const r=e[y],o=!!n&&v===n[v];o&&(n[m]=r,n[k]=i);const a=t.run(s,void 0,o&&s!==d&&s!==h?[]:[r]);T(n,!0,a)}catch(r){T(n,!1,r)}},n)}const Z=function(){};class D{static toString(){return"function ZoneAwarePromise() { [native code] }"}static resolve(e){return T(new this(null),!0,e)}static reject(e){return T(new this(null),!1,e)}static race(e){let t,n,r=new this((e,r)=>{t=e,n=r});function o(e){t(e)}function i(e){n(e)}for(let s of e)p(s)||(s=this.resolve(s)),s.then(o,i);return r}static all(e){return D.allWithCallback(e)}static allSettled(e){return(this&&this.prototype instanceof D?this:D).allWithCallback(e,{thenCallback:e=>({status:"fulfilled",value:e}),errorCallback:e=>({status:"rejected",reason:e})})}static allWithCallback(e,t){let n,r,o=new this((e,t)=>{n=e,r=t}),i=2,s=0;const a=[];for(let l of e){p(l)||(l=this.resolve(l));const e=s;try{l.then(r=>{a[e]=t?t.thenCallback(r):r,i--,0===i&&n(a)},o=>{t?(a[e]=t.errorCallback(o),i--,0===i&&n(a)):r(o)})}catch(c){r(c)}i++,s++}return i-=2,0===i&&n(a),o}constructor(e){const t=this;if(!(t instanceof D))throw new Error("Must be an instanceof Promise.");t[g]=null,t[y]=[];try{e&&e(_(t,!0),_(t,!1))}catch(n){T(t,!1,n)}}get[Symbol.toStringTag](){return"Promise"}get[Symbol.species](){return D}then(e,n){let r=this.constructor[Symbol.species];r&&"function"==typeof r||(r=this.constructor||D);const o=new r(Z),i=t.current;return null==this[g]?this[y].push(i,o,e,n):S(this,i,o,e,n),o}catch(e){return this.then(null,e)}finally(e){let n=this.constructor[Symbol.species];n&&"function"==typeof n||(n=D);const r=new n(Z);r[v]=v;const o=t.current;return null==this[g]?this[y].push(o,r,e,e):S(this,o,r,e,e),r}}D.resolve=D.resolve,D.reject=D.reject,D.race=D.race,D.all=D.all;const O=e[c]=e.Promise,P=t.__symbol__("ZoneAwarePromise");let x=r(e,"Promise");x&&!x.configurable||(x&&delete x.writable,x&&delete x.value,x||(x={configurable:!0,enumerable:!0}),x.get=function(){return e[P]?e[P]:e[c]},x.set=function(t){t===D?e[P]=t:(e[c]=t,t.prototype[l]||j(t),n.setNativePromise(t))},o(e,"Promise",x)),e.Promise=D;const C=i("thenPatched");function j(e){const t=e.prototype,n=r(t,"then");if(n&&(!1===n.writable||!n.configurable))return;const o=t.then;t[l]=o,e.prototype.then=function(e,t){return new D((e,t)=>{o.call(this,e,t)}).then(e,t)},e[C]=!0}if(n.patchThen=j,O){j(O);const t=e.fetch;"function"==typeof t&&(e[n.symbol("fetch")]=t,e.fetch=(z=t,function(){let e=z.apply(this,arguments);if(e instanceof D)return e;let t=e.constructor;return t[C]||j(t),e}))}var z;return Promise[t.__symbol__("uncaughtPromiseErrors")]=s,D});const e=Object.getOwnPropertyDescriptor,t=Object.defineProperty,n=Object.getPrototypeOf,r=Object.create,o=Array.prototype.slice,i=Zone.__symbol__("addEventListener"),s=Zone.__symbol__("removeEventListener"),a=Zone.__symbol__("");function c(e,t){return Zone.current.wrap(e,t)}function l(e,t,n,r,o){return Zone.current.scheduleMacroTask(e,t,n,r,o)}const u=Zone.__symbol__,f="undefined"!=typeof window,p=f?window:void 0,h=f&&p||"object"==typeof self&&self||global,d=[null];function g(e,t){for(let n=e.length-1;n>=0;n--)"function"==typeof e[n]&&(e[n]=c(e[n],t+"_"+n));return e}function y(e){return!e||!1!==e.writable&&!("function"==typeof e.get&&void 0===e.set)}const v="undefined"!=typeof WorkerGlobalScope&&self instanceof WorkerGlobalScope,m=!("nw"in h)&&void 0!==h.process&&"[object process]"==={}.toString.call(h.process),k=!m&&!v&&!(!f||!p.HTMLElement),_=void 0!==h.process&&"[object process]"==={}.toString.call(h.process)&&!v&&!(!f||!p.HTMLElement),b={},T=function(e){if(!(e=e||h.event))return;let t=b[e.type];t||(t=b[e.type]=u("ON_PROPERTY"+e.type));const n=this||e.target||h,r=n[t];let o;if(k&&n===p&&"error"===e.type){const t=e;o=r&&r.call(this,t.message,t.filename,t.lineno,t.colno,t.error),!0===o&&e.preventDefault()}else o=r&&r.apply(this,arguments),null==o||o||e.preventDefault();return o};function w(n,r,o){let i=e(n,r);if(!i&&o&&e(o,r)&&(i={enumerable:!0,configurable:!0}),!i||!i.configurable)return;const s=u("on"+r+"patched");if(n.hasOwnProperty(s)&&n[s])return;delete i.writable,delete i.value;const a=i.get,c=i.set,l=r.substr(2);let f=b[l];f||(f=b[l]=u("ON_PROPERTY"+l)),i.set=function(e){let t=this;t||n!==h||(t=h),t&&(t[f]&&t.removeEventListener(l,T),c&&c.apply(t,d),"function"==typeof e?(t[f]=e,t.addEventListener(l,T,!1)):t[f]=null)},i.get=function(){let e=this;if(e||n!==h||(e=h),!e)return null;const t=e[f];if(t)return t;if(a){let t=a&&a.call(this);if(t)return i.set.call(this,t),"function"==typeof e.removeAttribute&&e.removeAttribute(r),t}return null},t(n,r,i),n[s]=!0}function E(e,t,n){if(t)for(let r=0;r<t.length;r++)w(e,"on"+t[r],n);else{const t=[];for(const n in e)"on"==n.substr(0,2)&&t.push(n);for(let r=0;r<t.length;r++)w(e,t[r],n)}}const S=u("originalInstance");function Z(e){const n=h[e];if(!n)return;h[u(e)]=n,h[e]=function(){const t=g(arguments,e);switch(t.length){case 0:this[S]=new n;break;case 1:this[S]=new n(t[0]);break;case 2:this[S]=new n(t[0],t[1]);break;case 3:this[S]=new n(t[0],t[1],t[2]);break;case 4:this[S]=new n(t[0],t[1],t[2],t[3]);break;default:throw new Error("Arg list too long.")}},P(h[e],n);const r=new n(function(){});let o;for(o in r)"XMLHttpRequest"===e&&"responseBlob"===o||function(n){"function"==typeof r[n]?h[e].prototype[n]=function(){return this[S][n].apply(this[S],arguments)}:t(h[e].prototype,n,{set:function(t){"function"==typeof t?(this[S][n]=c(t,e+"."+n),P(this[S][n],t)):this[S][n]=t},get:function(){return this[S][n]}})}(o);for(o in n)"prototype"!==o&&n.hasOwnProperty(o)&&(h[e][o]=n[o])}function D(t,r,o){let i=t;for(;i&&!i.hasOwnProperty(r);)i=n(i);!i&&t[r]&&(i=t);const s=u(r);let a=null;if(i&&!(a=i[s])&&(a=i[s]=i[r],y(i&&e(i,r)))){const e=o(a,s,r);i[r]=function(){return e(this,arguments)},P(i[r],a)}return a}function O(e,t,n){let r=null;function o(e){const t=e.data;return t.args[t.cbIdx]=function(){e.invoke.apply(this,arguments)},r.apply(t.target,t.args),e}r=D(e,t,e=>function(t,r){const i=n(t,r);return i.cbIdx>=0&&"function"==typeof r[i.cbIdx]?l(i.name,r[i.cbIdx],i,o):e.apply(t,r)})}function P(e,t){e[u("OriginalDelegate")]=t}let x=!1,C=!1;function j(){try{const e=p.navigator.userAgent;if(-1!==e.indexOf("MSIE ")||-1!==e.indexOf("Trident/"))return!0}catch(e){}return!1}function z(){if(x)return C;x=!0;try{const e=p.navigator.userAgent;-1===e.indexOf("MSIE ")&&-1===e.indexOf("Trident/")&&-1===e.indexOf("Edge/")||(C=!0)}catch(e){}return C}Zone.__load_patch("toString",e=>{const t=Function.prototype.toString,n=u("OriginalDelegate"),r=u("Promise"),o=u("Error"),i=function(){if("function"==typeof this){const i=this[n];if(i)return"function"==typeof i?t.call(i):Object.prototype.toString.call(i);if(this===Promise){const n=e[r];if(n)return t.call(n)}if(this===Error){const n=e[o];if(n)return t.call(n)}}return t.call(this)};i[n]=t,Function.prototype.toString=i;const s=Object.prototype.toString;Object.prototype.toString=function(){return this instanceof Promise?"[object Promise]":s.call(this)}});let I=!1;if("undefined"!=typeof window)try{const e=Object.defineProperty({},"passive",{get:function(){I=!0}});window.addEventListener("test",e,e),window.removeEventListener("test",e,e)}catch(ae){I=!1}const R={useG:!0},M={},A={},N=new RegExp("^"+a+"(\\w+)(true|false)$"),L=u("propagationStopped");function B(e,t){const n=(t?t(e):e)+"false",r=(t?t(e):e)+"true",o=a+n,i=a+r;M[e]={},M[e].false=o,M[e].true=i}function H(e,t,r){const o=r&&r.add||"addEventListener",i=r&&r.rm||"removeEventListener",s=r&&r.listeners||"eventListeners",c=r&&r.rmAll||"removeAllListeners",l=u(o),f="."+o+":",p=function(e,t,n){if(e.isRemoved)return;const r=e.callback;"object"==typeof r&&r.handleEvent&&(e.callback=e=>r.handleEvent(e),e.originalDelegate=r),e.invoke(e,t,[n]);const o=e.options;o&&"object"==typeof o&&o.once&&t[i].call(t,n.type,e.originalDelegate?e.originalDelegate:e.callback,o)},h=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,r=n[M[t.type].false];if(r)if(1===r.length)p(r[0],n,t);else{const e=r.slice();for(let r=0;r<e.length&&(!t||!0!==t[L]);r++)p(e[r],n,t)}},d=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,r=n[M[t.type].true];if(r)if(1===r.length)p(r[0],n,t);else{const e=r.slice();for(let r=0;r<e.length&&(!t||!0!==t[L]);r++)p(e[r],n,t)}};function g(t,r){if(!t)return!1;let p=!0;r&&void 0!==r.useG&&(p=r.useG);const g=r&&r.vh;let y=!0;r&&void 0!==r.chkDup&&(y=r.chkDup);let v=!1;r&&void 0!==r.rt&&(v=r.rt);let k=t;for(;k&&!k.hasOwnProperty(o);)k=n(k);if(!k&&t[o]&&(k=t),!k)return!1;if(k[l])return!1;const _=r&&r.eventNameToString,b={},T=k[l]=k[o],w=k[u(i)]=k[i],E=k[u(s)]=k[s],S=k[u(c)]=k[c];let Z;function D(e,t){return!I&&"object"==typeof e&&e?!!e.capture:I&&t?"boolean"==typeof e?{capture:e,passive:!0}:e?"object"==typeof e&&!1!==e.passive?Object.assign(Object.assign({},e),{passive:!0}):e:{passive:!0}:e}r&&r.prepend&&(Z=k[u(r.prepend)]=k[r.prepend]);const O=p?function(e){if(!b.isExisting)return T.call(b.target,b.eventName,b.capture?d:h,b.options)}:function(e){return T.call(b.target,b.eventName,e.invoke,b.options)},x=p?function(e){if(!e.isRemoved){const t=M[e.eventName];let n;t&&(n=t[e.capture?"true":"false"]);const r=n&&e.target[n];if(r)for(let o=0;o<r.length;o++)if(r[o]===e){r.splice(o,1),e.isRemoved=!0,0===r.length&&(e.allRemoved=!0,e.target[n]=null);break}}if(e.allRemoved)return w.call(e.target,e.eventName,e.capture?d:h,e.options)}:function(e){return w.call(e.target,e.eventName,e.invoke,e.options)},C=r&&r.diff?r.diff:function(e,t){const n=typeof t;return"function"===n&&e.callback===t||"object"===n&&e.originalDelegate===t},j=Zone[u("BLACK_LISTED_EVENTS")],z=e[u("PASSIVE_EVENTS")],L=function(t,n,o,i,s=!1,a=!1){return function(){const c=this||e;let l=arguments[0];r&&r.transferEventName&&(l=r.transferEventName(l));let u=arguments[1];if(!u)return t.apply(this,arguments);if(m&&"uncaughtException"===l)return t.apply(this,arguments);let f=!1;if("function"!=typeof u){if(!u.handleEvent)return t.apply(this,arguments);f=!0}if(g&&!g(t,u,c,arguments))return;const h=I&&!!z&&-1!==z.indexOf(l),d=D(arguments[2],h);if(j)for(let e=0;e<j.length;e++)if(l===j[e])return h?t.call(c,l,u,d):t.apply(this,arguments);const v=!!d&&("boolean"==typeof d||d.capture),k=!(!d||"object"!=typeof d)&&d.once,T=Zone.current;let w=M[l];w||(B(l,_),w=M[l]);const E=w[v?"true":"false"];let S,Z=c[E],O=!1;if(Z){if(O=!0,y)for(let e=0;e<Z.length;e++)if(C(Z[e],u))return}else Z=c[E]=[];const P=c.constructor.name,x=A[P];x&&(S=x[l]),S||(S=P+n+(_?_(l):l)),b.options=d,k&&(b.options.once=!1),b.target=c,b.capture=v,b.eventName=l,b.isExisting=O;const N=p?R:void 0;N&&(N.taskData=b);const L=T.scheduleEventTask(S,u,N,o,i);return b.target=null,N&&(N.taskData=null),k&&(d.once=!0),(I||"boolean"!=typeof L.options)&&(L.options=d),L.target=c,L.capture=v,L.eventName=l,f&&(L.originalDelegate=u),a?Z.unshift(L):Z.push(L),s?c:void 0}};return k[o]=L(T,f,O,x,v),Z&&(k.prependListener=L(Z,".prependListener:",function(e){return Z.call(b.target,b.eventName,e.invoke,b.options)},x,v,!0)),k[i]=function(){const t=this||e;let n=arguments[0];r&&r.transferEventName&&(n=r.transferEventName(n));const o=arguments[2],i=!!o&&("boolean"==typeof o||o.capture),s=arguments[1];if(!s)return w.apply(this,arguments);if(g&&!g(w,s,t,arguments))return;const c=M[n];let l;c&&(l=c[i?"true":"false"]);const u=l&&t[l];if(u)for(let e=0;e<u.length;e++){const r=u[e];if(C(r,s))return u.splice(e,1),r.isRemoved=!0,0===u.length&&(r.allRemoved=!0,t[l]=null,"string"==typeof n)&&(t[a+"ON_PROPERTY"+n]=null),r.zone.cancelTask(r),v?t:void 0}return w.apply(this,arguments)},k[s]=function(){const t=this||e;let n=arguments[0];r&&r.transferEventName&&(n=r.transferEventName(n));const o=[],i=F(t,_?_(n):n);for(let e=0;e<i.length;e++){const t=i[e];o.push(t.originalDelegate?t.originalDelegate:t.callback)}return o},k[c]=function(){const t=this||e;let n=arguments[0];if(n){r&&r.transferEventName&&(n=r.transferEventName(n));const e=M[n];if(e){const r=t[e.false],o=t[e.true];if(r){const e=r.slice();for(let t=0;t<e.length;t++){const r=e[t];this[i].call(this,n,r.originalDelegate?r.originalDelegate:r.callback,r.options)}}if(o){const e=o.slice();for(let t=0;t<e.length;t++){const r=e[t];this[i].call(this,n,r.originalDelegate?r.originalDelegate:r.callback,r.options)}}}}else{const e=Object.keys(t);for(let t=0;t<e.length;t++){const n=N.exec(e[t]);let r=n&&n[1];r&&"removeListener"!==r&&this[c].call(this,r)}this[c].call(this,"removeListener")}if(v)return this},P(k[o],T),P(k[i],w),S&&P(k[c],S),E&&P(k[s],E),!0}let y=[];for(let n=0;n<t.length;n++)y[n]=g(t[n],r);return y}function F(e,t){if(!t){const n=[];for(let r in e){const o=N.exec(r);let i=o&&o[1];if(i&&(!t||i===t)){const t=e[r];if(t)for(let e=0;e<t.length;e++)n.push(t[e])}}return n}let n=M[t];n||(B(t),n=M[t]);const r=e[n.false],o=e[n.true];return r?o?r.concat(o):r.slice():o?o.slice():[]}function G(e,t){const n=e.Event;n&&n.prototype&&t.patchMethod(n.prototype,"stopImmediatePropagation",e=>function(t,n){t[L]=!0,e&&e.apply(t,n)})}function U(e,t,n,r,o){const i=Zone.__symbol__(r);if(t[i])return;const s=t[i]=t[r];t[r]=function(i,a,c){return a&&a.prototype&&o.forEach(function(t){const o=`${n}.${r}::`+t,i=a.prototype;if(i.hasOwnProperty(t)){const n=e.ObjectGetOwnPropertyDescriptor(i,t);n&&n.value?(n.value=e.wrapWithCurrentZone(n.value,o),e._redefineProperty(a.prototype,t,n)):i[t]&&(i[t]=e.wrapWithCurrentZone(i[t],o))}else i[t]&&(i[t]=e.wrapWithCurrentZone(i[t],o))}),s.call(t,i,a,c)},e.attachOriginToPatched(t[r],s)}const V=["absolutedeviceorientation","afterinput","afterprint","appinstalled","beforeinstallprompt","beforeprint","beforeunload","devicelight","devicemotion","deviceorientation","deviceorientationabsolute","deviceproximity","hashchange","languagechange","message","mozbeforepaint","offline","online","paint","pageshow","pagehide","popstate","rejectionhandled","storage","unhandledrejection","unload","userproximity","vrdisplayconnected","vrdisplaydisconnected","vrdisplaypresentchange"],W=["encrypted","waitingforkey","msneedkey","mozinterruptbegin","mozinterruptend"],Y=["load"],X=["blur","error","focus","load","resize","scroll","messageerror"],q=["bounce","finish","start"],K=["loadstart","progress","abort","error","load","progress","timeout","loadend","readystatechange"],J=["upgradeneeded","complete","abort","success","error","blocked","versionchange","close"],Q=["close","error","open","message"],$=["error","message"],ee=["abort","animationcancel","animationend","animationiteration","auxclick","beforeinput","blur","cancel","canplay","canplaythrough","change","compositionstart","compositionupdate","compositionend","cuechange","click","close","contextmenu","curechange","dblclick","drag","dragend","dragenter","dragexit","dragleave","dragover","drop","durationchange","emptied","ended","error","focus","focusin","focusout","gotpointercapture","input","invalid","keydown","keypress","keyup","load","loadstart","loadeddata","loadedmetadata","lostpointercapture","mousedown","mouseenter","mouseleave","mousemove","mouseout","mouseover","mouseup","mousewheel","orientationchange","pause","play","playing","pointercancel","pointerdown","pointerenter","pointerleave","pointerlockchange","mozpointerlockchange","webkitpointerlockerchange","pointerlockerror","mozpointerlockerror","webkitpointerlockerror","pointermove","pointout","pointerover","pointerup","progress","ratechange","reset","resize","scroll","seeked","seeking","select","selectionchange","selectstart","show","sort","stalled","submit","suspend","timeupdate","volumechange","touchcancel","touchmove","touchstart","touchend","transitioncancel","transitionend","waiting","wheel"].concat(["webglcontextrestored","webglcontextlost","webglcontextcreationerror"],["autocomplete","autocompleteerror"],["toggle"],["afterscriptexecute","beforescriptexecute","DOMContentLoaded","freeze","fullscreenchange","mozfullscreenchange","webkitfullscreenchange","msfullscreenchange","fullscreenerror","mozfullscreenerror","webkitfullscreenerror","msfullscreenerror","readystatechange","visibilitychange","resume"],V,["beforecopy","beforecut","beforepaste","copy","cut","paste","dragstart","loadend","animationstart","search","transitionrun","transitionstart","webkitanimationend","webkitanimationiteration","webkitanimationstart","webkittransitionend"],["activate","afterupdate","ariarequest","beforeactivate","beforedeactivate","beforeeditfocus","beforeupdate","cellchange","controlselect","dataavailable","datasetchanged","datasetcomplete","errorupdate","filterchange","layoutcomplete","losecapture","move","moveend","movestart","propertychange","resizeend","resizestart","rowenter","rowexit","rowsdelete","rowsinserted","command","compassneedscalibration","deactivate","help","mscontentzoom","msmanipulationstatechanged","msgesturechange","msgesturedoubletap","msgestureend","msgesturehold","msgesturestart","msgesturetap","msgotpointercapture","msinertiastart","mslostpointercapture","mspointercancel","mspointerdown","mspointerenter","mspointerhover","mspointerleave","mspointermove","mspointerout","mspointerover","mspointerup","pointerout","mssitemodejumplistitemremoved","msthumbnailclick","stop","storagecommit"]);function te(e,t,n){if(!n||0===n.length)return t;const r=n.filter(t=>t.target===e);if(!r||0===r.length)return t;const o=r[0].ignoreProperties;return t.filter(e=>-1===o.indexOf(e))}function ne(e,t,n,r){e&&E(e,te(e,t,n),r)}function re(e,t){if(m&&!_)return;if(Zone[e.symbol("patchEvents")])return;const r="undefined"!=typeof WebSocket,o=t.__Zone_ignore_on_properties;if(k){const e=window,t=j?[{target:e,ignoreProperties:["error"]}]:[];ne(e,ee.concat(["messageerror"]),o?o.concat(t):o,n(e)),ne(Document.prototype,ee,o),void 0!==e.SVGElement&&ne(e.SVGElement.prototype,ee,o),ne(Element.prototype,ee,o),ne(HTMLElement.prototype,ee,o),ne(HTMLMediaElement.prototype,W,o),ne(HTMLFrameSetElement.prototype,V.concat(X),o),ne(HTMLBodyElement.prototype,V.concat(X),o),ne(HTMLFrameElement.prototype,Y,o),ne(HTMLIFrameElement.prototype,Y,o);const r=e.HTMLMarqueeElement;r&&ne(r.prototype,q,o);const i=e.Worker;i&&ne(i.prototype,$,o)}const i=t.XMLHttpRequest;i&&ne(i.prototype,K,o);const s=t.XMLHttpRequestEventTarget;s&&ne(s&&s.prototype,K,o),"undefined"!=typeof IDBIndex&&(ne(IDBIndex.prototype,J,o),ne(IDBRequest.prototype,J,o),ne(IDBOpenDBRequest.prototype,J,o),ne(IDBDatabase.prototype,J,o),ne(IDBTransaction.prototype,J,o),ne(IDBCursor.prototype,J,o)),r&&ne(WebSocket.prototype,Q,o)}Zone.__load_patch("util",(n,i,s)=>{s.patchOnProperties=E,s.patchMethod=D,s.bindArguments=g,s.patchMacroTask=O;const l=i.__symbol__("BLACK_LISTED_EVENTS"),u=i.__symbol__("UNPATCHED_EVENTS");n[u]&&(n[l]=n[u]),n[l]&&(i[l]=i[u]=n[l]),s.patchEventPrototype=G,s.patchEventTarget=H,s.isIEOrEdge=z,s.ObjectDefineProperty=t,s.ObjectGetOwnPropertyDescriptor=e,s.ObjectCreate=r,s.ArraySlice=o,s.patchClass=Z,s.wrapWithCurrentZone=c,s.filterProperties=te,s.attachOriginToPatched=P,s._redefineProperty=Object.defineProperty,s.patchCallbacks=U,s.getGlobalObjects=()=>({globalSources:A,zoneSymbolEventNames:M,eventNames:ee,isBrowser:k,isMix:_,isNode:m,TRUE_STR:"true",FALSE_STR:"false",ZONE_SYMBOL_PREFIX:a,ADD_EVENT_LISTENER_STR:"addEventListener",REMOVE_EVENT_LISTENER_STR:"removeEventListener"})});const oe=u("zoneTask");function ie(e,t,n,r){let o=null,i=null;n+=r;const s={};function a(t){const n=t.data;return n.args[0]=function(){try{t.invoke.apply(this,arguments)}finally{t.data&&t.data.isPeriodic||("number"==typeof n.handleId?delete s[n.handleId]:n.handleId&&(n.handleId[oe]=null))}},n.handleId=o.apply(e,n.args),t}function c(e){return i(e.data.handleId)}o=D(e,t+=r,n=>function(o,i){if("function"==typeof i[0]){const e=l(t,i[0],{isPeriodic:"Interval"===r,delay:"Timeout"===r||"Interval"===r?i[1]||0:void 0,args:i},a,c);if(!e)return e;const n=e.data.handleId;return"number"==typeof n?s[n]=e:n&&(n[oe]=e),n&&n.ref&&n.unref&&"function"==typeof n.ref&&"function"==typeof n.unref&&(e.ref=n.ref.bind(n),e.unref=n.unref.bind(n)),"number"==typeof n||n?n:e}return n.apply(e,i)}),i=D(e,n,t=>function(n,r){const o=r[0];let i;"number"==typeof o?i=s[o]:(i=o&&o[oe],i||(i=o)),i&&"string"==typeof i.type?"notScheduled"!==i.state&&(i.cancelFn&&i.data.isPeriodic||0===i.runCount)&&("number"==typeof o?delete s[o]:o&&(o[oe]=null),i.zone.cancelTask(i)):t.apply(e,r)})}function se(e,t){if(Zone[t.symbol("patchEventTarget")])return;const{eventNames:n,zoneSymbolEventNames:r,TRUE_STR:o,FALSE_STR:i,ZONE_SYMBOL_PREFIX:s}=t.getGlobalObjects();for(let c=0;c<n.length;c++){const e=n[c],t=s+(e+i),a=s+(e+o);r[e]={},r[e][i]=t,r[e][o]=a}const a=e.EventTarget;return a&&a.prototype?(t.patchEventTarget(e,[a&&a.prototype]),!0):void 0}Zone.__load_patch("legacy",e=>{const t=e[Zone.__symbol__("legacyPatch")];t&&t()}),Zone.__load_patch("timers",e=>{ie(e,"set","clear","Timeout"),ie(e,"set","clear","Interval"),ie(e,"set","clear","Immediate")}),Zone.__load_patch("requestAnimationFrame",e=>{ie(e,"request","cancel","AnimationFrame"),ie(e,"mozRequest","mozCancel","AnimationFrame"),ie(e,"webkitRequest","webkitCancel","AnimationFrame")}),Zone.__load_patch("blocking",(e,t)=>{const n=["alert","prompt","confirm"];for(let r=0;r<n.length;r++)D(e,n[r],(n,r,o)=>function(r,i){return t.current.run(n,e,i,o)})}),Zone.__load_patch("EventTarget",(e,t,n)=>{(function(e,t){t.patchEventPrototype(e,t)})(e,n),se(e,n);const r=e.XMLHttpRequestEventTarget;r&&r.prototype&&n.patchEventTarget(e,[r.prototype]),Z("MutationObserver"),Z("WebKitMutationObserver"),Z("IntersectionObserver"),Z("FileReader")}),Zone.__load_patch("on_property",(e,t,n)=>{re(n,e)}),Zone.__load_patch("customElements",(e,t,n)=>{!function(e,t){const{isBrowser:n,isMix:r}=t.getGlobalObjects();(n||r)&&e.customElements&&"customElements"in e&&t.patchCallbacks(t,e.customElements,"customElements","define",["connectedCallback","disconnectedCallback","adoptedCallback","attributeChangedCallback"])}(e,n)}),Zone.__load_patch("XHR",(e,t)=>{!function(e){const p=e.XMLHttpRequest;if(!p)return;const h=p.prototype;let d=h[i],g=h[s];if(!d){const t=e.XMLHttpRequestEventTarget;if(t){const e=t.prototype;d=e[i],g=e[s]}}function y(e){const r=e.data,c=r.target;c[a]=!1,c[f]=!1;const l=c[o];d||(d=c[i],g=c[s]),l&&g.call(c,"readystatechange",l);const u=c[o]=()=>{if(c.readyState===c.DONE)if(!r.aborted&&c[a]&&"scheduled"===e.state){const n=c[t.__symbol__("loadfalse")];if(n&&n.length>0){const o=e.invoke;e.invoke=function(){const n=c[t.__symbol__("loadfalse")];for(let t=0;t<n.length;t++)n[t]===e&&n.splice(t,1);r.aborted||"scheduled"!==e.state||o.call(e)},n.push(e)}else e.invoke()}else r.aborted||!1!==c[a]||(c[f]=!0)};return d.call(c,"readystatechange",u),c[n]||(c[n]=e),T.apply(c,r.args),c[a]=!0,e}function v(){}function m(e){const t=e.data;return t.aborted=!0,w.apply(t.target,t.args)}const k=D(h,"open",()=>function(e,t){return e[r]=0==t[2],e[c]=t[1],k.apply(e,t)}),_=u("fetchTaskAborting"),b=u("fetchTaskScheduling"),T=D(h,"send",()=>function(e,n){if(!0===t.current[b])return T.apply(e,n);if(e[r])return T.apply(e,n);{const t={target:e,url:e[c],isPeriodic:!1,args:n,aborted:!1},r=l("XMLHttpRequest.send",v,t,y,m);e&&!0===e[f]&&!t.aborted&&"scheduled"===r.state&&r.invoke()}}),w=D(h,"abort",()=>function(e,r){const o=e[n];if(o&&"string"==typeof o.type){if(null==o.cancelFn||o.data&&o.data.aborted)return;o.zone.cancelTask(o)}else if(!0===t.current[_])return w.apply(e,r)})}(e);const n=u("xhrTask"),r=u("xhrSync"),o=u("xhrListener"),a=u("xhrScheduled"),c=u("xhrURL"),f=u("xhrErrorBeforeScheduled")}),Zone.__load_patch("geolocation",t=>{t.navigator&&t.navigator.geolocation&&function(t,n){const r=t.constructor.name;for(let o=0;o<n.length;o++){const i=n[o],s=t[i];if(s){if(!y(e(t,i)))continue;t[i]=(e=>{const t=function(){return e.apply(this,g(arguments,r+"."+i))};return P(t,e),t})(s)}}}(t.navigator.geolocation,["getCurrentPosition","watchPosition"])}),Zone.__load_patch("PromiseRejectionEvent",(e,t)=>{function n(t){return function(n){F(e,t).forEach(r=>{const o=e.PromiseRejectionEvent;if(o){const e=new o(t,{promise:n.promise,reason:n.rejection});r.invoke(e)}})}}e.PromiseRejectionEvent&&(t[u("unhandledPromiseRejectionHandler")]=n("unhandledrejection"),t[u("rejectionHandledHandler")]=n("rejectionhandled"))})})?r.call(t,n,t,e):r)||(e.exports=o)},pg82:function(e,t){var n=null,r=null;function o(e,t,n){e.addEventListener(t,function(e){var o=new MouseEvent(n,e);o.pointerId=1,o.isPrimary=!0,o.pointerType="mouse",o.width=1,o.height=1,o.tiltX=0,o.tiltY=0,o.pressure="buttons"in e&&0!==e.buttons?.5:0;var i=e.target;null!==r&&(i=r,"mouseup"===t&&(r=null)),i.dispatchEvent(o),o.defaultPrevented&&e.preventDefault()})}function i(e,t,r){e.addEventListener(t,function(e){for(var o=e.changedTouches,i=o.length,s=0;s<i;s++){var a=new CustomEvent(r,{bubbles:!0,cancelable:!0});a.ctrlKey=e.ctrlKey,a.shiftKey=e.shiftKey,a.altKey=e.altKey,a.metaKey=e.metaKey;var c=o.item(s);a.clientX=c.clientX,a.clientY=c.clientY,a.screenX=c.screenX,a.screenY=c.screenY,a.pageX=c.pageX,a.pageY=c.pageY;var l=c.target.getBoundingClientRect();a.offsetX=c.clientX-l.left,a.offsetY=c.clientY-l.top,a.pointerId=1+c.identifier,a.button=0,a.buttons=1,a.movementX=0,a.movementY=0,a.region=null,a.relatedTarget=null,a.x=a.clientX,a.y=a.clientY,a.pointerType="touch",a.width=1,a.height=1,a.tiltX=0,a.tiltY=0,a.pressure=1,"touchstart"===t&&null===n&&(n=c.identifier),a.isPrimary=c.identifier===n,"touchend"===t&&a.isPrimary&&(n=null),e.target.dispatchEvent(a),a.defaultPrevented&&e.preventDefault()}})}"PointerEvent"in window||(Element.prototype.setPointerCapture=Element.prototype.setCapture,Element.prototype.releasePointerCapture=Element.prototype.releaseCapture,"TouchEvent"in window||(o(document,"mousedown","pointerdown"),o(document,"mousemove","pointermove"),o(document,"mouseup","pointerup")),i(document,"touchstart","pointerdown"),i(document,"touchmove","pointermove"),i(document,"touchend","pointerup"))},ppGB:function(e,t){var n=Math.ceil,r=Math.floor;e.exports=function(e){return isNaN(e=+e)?0:(e>0?r:n)(e)}},rmf8:function(e,t,n){var r=n("KPYQ");e.exports=r},sQkB:function(e,t,n){var r=n("2oRo"),o=n("A2ZE"),i=Function.call;e.exports=function(e,t,n){return o(i,r[e].prototype[t],n)}},tiKp:function(e,t,n){var r=n("2oRo"),o=n("VpIT"),i=n("UTVS"),s=n("kOOl"),a=n("STAE"),c=n("/b8u"),l=o("wks"),u=r.Symbol,f=c?u:u&&u.withoutSetter||s;e.exports=function(e){return i(l,e)||(l[e]=a&&i(u,e)?u[e]:f("Symbol."+e)),l[e]}},wE6v:function(e,t,n){var r=n("hh1v");e.exports=function(e,t){if(!r(e))return e;var n,o;if(t&&"function"==typeof(n=e.toString)&&!r(o=n.call(e)))return o;if("function"==typeof(n=e.valueOf)&&!r(o=n.call(e)))return o;if(!t&&"function"==typeof(n=e.toString)&&!r(o=n.call(e)))return o;throw TypeError("Can't convert object to primitive value")}},xDBR:function(e,t){e.exports=!1},xrYK:function(e,t){var n={}.toString;e.exports=function(e){return n.call(e).slice(8,-1)}},xs3f:function(e,t,n){var r=n("2oRo"),o=n("zk60"),i=r["__core-js_shared__"]||o("__core-js_shared__",{});e.exports=i},yoRg:function(e,t,n){var r=n("UTVS"),o=n("/GqU"),i=n("TWQb").indexOf,s=n("0BK2");e.exports=function(e,t){var n,a=o(e),c=0,l=[];for(n in a)!r(s,n)&&r(a,n)&&l.push(n);for(;t.length>c;)r(a,n=t[c++])&&(~i(l,n)||l.push(n));return l}},zBJ4:function(e,t,n){var r=n("2oRo"),o=n("hh1v"),i=r.document,s=o(i)&&o(i.createElement);e.exports=function(e){return s?i.createElement(e):{}}},zk60:function(e,t,n){var r=n("2oRo"),o=n("kRJp");e.exports=function(e,t){try{o(r,e,t)}catch(n){r[e]=t}return t}}}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bypassSecurityTrustHtml`
  
  
  
  
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
  
  
  
* URL: [https://anais.beta.gouv.fr/](https://anais.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/robots.txt](https://anais.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://anais.beta.gouv.fr](https://anais.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/sitemap.xml](https://anais.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/sitemap.xml](https://anais.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/runtime-es2015.a4dadbc03350107420a4.js](https://anais.beta.gouv.fr/runtime-es2015.a4dadbc03350107420a4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/runtime-es5.a4dadbc03350107420a4.js](https://anais.beta.gouv.fr/runtime-es5.a4dadbc03350107420a4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/](https://anais.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr](https://anais.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js](https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/robots.txt](https://anais.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/runtime-es2015.a4dadbc03350107420a4.js](https://anais.beta.gouv.fr/runtime-es2015.a4dadbc03350107420a4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/sitemap.xml](https://anais.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr](https://anais.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/runtime-es5.a4dadbc03350107420a4.js](https://anais.beta.gouv.fr/runtime-es5.a4dadbc03350107420a4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/assets/images/favicon_anais.png](https://anais.beta.gouv.fr/assets/images/favicon_anais.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/](https://anais.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/styles.2251a8b7f7c063556b97.css](https://anais.beta.gouv.fr/styles.2251a8b7f7c063556b97.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/robots.txt](https://anais.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js](https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.18.0`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAAJYAAAAQCAYAAAD06IYnAAAABmJLR0QA/wD/AP+gvaeTAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH4AIWDwkUFWbCCAAAAFxJREFUaN7t0kEKg0AQAME2x83/n2qu5qCgD1iDhCoYdpnbQC9bbY1qVO/jvc6k3ad91s7/7F1/csgPrujuQ17BDYSFsBAWwgJhISyEBcJCWAgLhIWwEBYIi2f7Ar/1TCgFH2X9AAAAAElFTkSuQmCC`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x0000�\x0000\x0000\x0000\x0010\x0008\x0006\x0000\x0000\x0000��'\x0000\x0000\x0000\x0006bKGD\x0000�\x0000�\x0000�����\x0000\x0000\x0000	pHYs\x0000\x0000\x000b\x0013\x0000\x0000\x000b\x0013\x0001\x0000��\x0018\x0000\x0000\x0000\x0007tIME\x0007�\x0002\x0016\x000f	\x0014\x0015f�\x0008\x0000\x0000\x0000\IDATh���A</p><p>�@\x0010\x0000�6����j�栠\x000fX��*\x0018v��@/[m�jT��Τݧ}����]r�\x000f���C^�
���\x0010\x0016�\x0002a!,�\x0005�BX\x0008\x000b���\x0010\x0016\x0008�g�\x0002��L(\x0005\x001fe�\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es2015.153c6affb3ef3c75b08306b254d0a4f6fd8be68e.js](https://anais.beta.gouv.fr/main-es2015.153c6affb3ef3c75b08306b254d0a4f6fd8be68e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js](https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: "!function(){function t(t,n){var r;if("undefined"==typeof Symbol||null==t[Symbol.iterator]){if(Array.isArray(t)||(r=function(t,n)", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/](https://anais.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    Veuillez activer le JavaScript pour utiliser cette application.
  </noscript>`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>>>0))break t;i=i+1|0}if(0|N(o,0|r[l>>2]))for(i=1;u=0|xt(7,0,0|(l=3*(15-i|0)|0)),h=e&~(0|w()),e=0|wt(0|t,0|e,0|l),w(),t=t&~u|(e=0|xt(0|le(7&e),0,0|l)),e=0|h|w(),i>>>0`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/robots.txt](https://anais.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    Veuillez activer le JavaScript pour utiliser cette application.
  </noscript>`
  
  
  
  
* URL: [https://anais.beta.gouv.fr](https://anais.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    Veuillez activer le JavaScript pour utiliser cette application.
  </noscript>`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/sitemap.xml](https://anais.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
    Veuillez activer le JavaScript pour utiliser cette application.
  </noscript>`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js](https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 7
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/](https://anais.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/robots.txt](https://anais.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://anais.beta.gouv.fr](https://anais.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/sitemap.xml](https://anais.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/runtime-es5.a4dadbc03350107420a4.js](https://anais.beta.gouv.fr/runtime-es5.a4dadbc03350107420a4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/assets/images/favicon_anais.png](https://anais.beta.gouv.fr/assets/images/favicon_anais.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=7200`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js](https://anais.beta.gouv.fr/polyfills-es2015.9c6b185d9749aeb5fdb2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/runtime-es2015.a4dadbc03350107420a4.js](https://anais.beta.gouv.fr/runtime-es2015.a4dadbc03350107420a4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/styles.2251a8b7f7c063556b97.css](https://anais.beta.gouv.fr/styles.2251a8b7f7c063556b97.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
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

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `100663296`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `369098752`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62425156`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2146435072`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15728640`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `117440513`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2130706432`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2013265920`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `536870912`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777215`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js](https://anais.beta.gouv.fr/polyfills-es5.0e6a0b9c0a11bcded2d1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777216`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1431655768`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15728641`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2130706433`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `318767104`
  
  
  
  
* URL: [https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js](https://anais.beta.gouv.fr/main-es5.ba9759eec904f42a7da42e599be45e26bdfcae69.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `094395102`
  
  
  
  
Instances: 28
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>2147483647, which evaluates to: 2038-01-19 03:14:07</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

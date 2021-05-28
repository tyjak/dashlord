
# ZAP Scanning Report

Generated on Fri, 28 May 2021 01:36:59


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 4 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Application Error Disclosure | Medium | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 2 | 
| Feature Policy Header Not Set | Low | 3 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 6 | 
| Strict-Transport-Security Header Not Set | Low | 9 | 
| X-Content-Type-Options Header Missing | Low | 8 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 2 | 
| Storable and Cacheable Content | Informational | 1 | 
| Storable but Non-Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 30 | 

## Alert Detail


  
  
  
  
### Application Error Disclosure
##### Medium (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `invalid query`
  
  
  
  
Instances: 1
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com"/>`
  
  
  
  
Instances: 2
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 2
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Feature-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 6
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml](https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/favicon.ico](https://catalogue.apprentissage.beta.gouv.fr/favicon.ico)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/favicon.ico](https://catalogue.apprentissage.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1016905377VD4HZ1NfAj4HalM1CmRXdwY4DjMKKwNqDGdQbQFgXW4COA88B2MDZVFk`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�Mz�Nw�C�vu5�#�v�3P�Ewpc��0��6��u\x0006�\x0016\x0005��#���v06U\x0016</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bTODO\b and was detected in the element starting with: "(this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[]).push([[2],[function(", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,a,i=t[0],l=t[1],p=t[2],c=0,s=[];c<i.length;c++)a=i[c],Object.prototype.hasOwnProperty.call(o,a)&&o[a]&&s.push(o[a][0]),o[a]=0;for(n in l)Object.prototype.hasOwnProperty.call(l,n)&&(e[n]=l[n]);for(f&&f(t);s.length;)s.shift()();return u.push.apply(u,p||[]),r()}function r(){for(var e,t=0;t<u.length;t++){for(var r=u[t],n=!0,i=1;i<r.length;i++){var l=r[i];0!==o[l]&&(n=!1)}n&&(u.splice(t--,1),e=a(a.s=r[0]))}return e}var n={},o={1:0},u=[];function a(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,a),r.l=!0,r.exports}a.m=e,a.c=n,a.d=function(e,t,r){a.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},a.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},a.t=function(e,t){if(1&t&&(e=a(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(a.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)a.d(r,n,function(t){return e[t]}.bind(null,n));return r},a.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return a.d(t,"a",t),t},a.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},a.p="/";var i=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],l=i.push.bind(i);i.push=t,i=i.slice();for(var p=0;p<i.length;p++)t(i[p]);var f=l;r()}([])</script>`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function t(t){for(var n,a,i=t[0],l=t[1],p=t[2],c=0,s=[];c<i.length;c++)a=i[c],Object.prototype.hasOwnProperty.call(o,a)&&o[a]&&s.push(o[a][0]),o[a]=0;for(n in l)Object.prototype.hasOwnProperty.call(l,n)&&(e[n]=l[n]);for(f&&f(t);s.length;)s.shift()();return u.push.apply(u,p||[]),r()}function r(){for(var e,t=0;t<u.length;t++){for(var r=u[t],n=!0,i=1;i<r.length;i++){var l=r[i];0!==o[l]&&(n=!1)}n&&(u.splice(t--,1),e=a(a.s=r[0]))}return e}var n={},o={1:0},u=[];function a(t){if(n[t])return n[t].exports;var r=n[t]={i:t,l:!1,exports:{}};return e[t].call(r.exports,r,r.exports,a),r.l=!0,r.exports}a.m=e,a.c=n,a.d=function(e,t,r){a.o(e,t)||Object.defineProperty(e,t,{enumerable:!0,get:r})},a.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},a.t=function(e,t){if(1&t&&(e=a(e)),8&t)return e;if(4&t&&"object"==typeof e&&e&&e.__esModule)return e;var r=Object.create(null);if(a.r(r),Object.defineProperty(r,"default",{enumerable:!0,value:e}),2&t&&"string"!=typeof e)for(var n in e)a.d(r,n,function(t){return e[t]}.bind(null,n));return r},a.n=function(e){var t=e&&e.__esModule?function(){return e.default}:function(){return e};return a.d(t,"a",t),t},a.o=function(e,t){return Object.prototype.hasOwnProperty.call(e,t)},a.p="/";var i=this["webpackJsonpmna-catalogue-apprentissage-ui"]=this["webpackJsonpmna-catalogue-apprentissage-ui"]||[],l=i.push.bind(i);i.push=t,i=i.slice();for(var p=0;p<i.length;p++)t(i[p]);var f=l;r()}([])</script>`
  
  
  
  
Instances: 2
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml](https://catalogue.apprentissage.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr](https://catalogue.apprentissage.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/manifest.json](https://catalogue.apprentissage.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/](https://catalogue.apprentissage.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/favicon.ico](https://catalogue.apprentissage.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/2.b14468aa.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/main.79b78e6c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css](https://catalogue.apprentissage.beta.gouv.fr/static/css/main.58c16a26.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/robots.txt](https://catalogue.apprentissage.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `47045881`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `35831808`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `45435424`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `40353607`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `52521875`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `39135393`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62748517`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `000000000`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11390625`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `60466176`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `28629151`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `17210368`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000000`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20511149`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777215`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11881376`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `19487171`
  
  
  
  
* URL: [https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js](https://catalogue.apprentissage.beta.gouv.fr/static/js/2.97e9e433.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `14348907`
  
  
  
  
Instances: 30
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>47045881, which evaluates to: 1971-06-29 12:18:01</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

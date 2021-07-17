
# ZAP Scanning Report

Generated on Sat, 17 Jul 2021 07:27:22


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 3 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: Wildcard Directive | Medium | 4 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 5 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 3 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 1 | 

## Alert Detail


  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/](https://rh-marine.chatbot.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' 'unsafe-inline'; img-src 'self' data:;`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/sitemap.xml](https://rh-marine.chatbot.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' 'unsafe-inline'; img-src 'self' data:;`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/robots.txt](https://rh-marine.chatbot.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' 'unsafe-inline'; img-src 'self' data:;`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/](https://rh-marine.chatbot.fabnum.fr/chatbot/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' 'unsafe-inline'; img-src 'self' data:;`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821)
  
  
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
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/](https://rh-marine.chatbot.fabnum.fr/chatbot/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/](https://rh-marine.chatbot.fabnum.fr/chatbot/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/runtime.734ca5ca4583a14f2d0d.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/runtime.734ca5ca4583a14f2d0d.js?1422070821)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x0000\x0010�\x0010Q� ��0ӏA\x0014�QU�a��qן�\x0018��Y�����ۯ�\x001c��]�㞻�߿</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/main.0d842ee62ecbf7038b02.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(self.webpackChunkchatbot_front=self.webpackChunkchatbot_front||[]).push([[179],{41362:function(e){function t(e){this.ms=(e=e||{", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/](https://rh-marine.chatbot.fabnum.fr/chatbot/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="runtime.734ca5ca4583a14f2d0d.js?1422070821" defer></script>`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/manifest.webmanifest](https://rh-marine.chatbot.fabnum.fr/chatbot/manifest.webmanifest)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/sitemap.xml](https://rh-marine.chatbot.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/](https://rh-marine.chatbot.fabnum.fr/chatbot/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/assets/icons/icon.png](https://rh-marine.chatbot.fabnum.fr/chatbot/assets/icons/icon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills-es5.03d9c12ecdcf79382a18.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `Mon, 19 Jul 2021 07:27:10 GMT`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/runtime.734ca5ca4583a14f2d0d.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/runtime.734ca5ca4583a14f2d0d.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `Mon, 19 Jul 2021 07:27:10 GMT`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/robots.txt](https://rh-marine.chatbot.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/styles.c96bc7e20db9abdff610.css?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/styles.c96bc7e20db9abdff610.css?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `Mon, 19 Jul 2021 07:27:10 GMT`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/](https://rh-marine.chatbot.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821](https://rh-marine.chatbot.fabnum.fr/chatbot/polyfills.83321f0c0c58627a0a91.js?1422070821)
  
  
  * Method: `GET`
  
  
  * Evidence: `Mon, 19 Jul 2021 07:27:11 GMT`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://rh-marine.chatbot.fabnum.fr/chatbot/](https://rh-marine.chatbot.fabnum.fr/chatbot/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1422070821`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1422070821, which evaluates to: 2015-01-24 03:40:21</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

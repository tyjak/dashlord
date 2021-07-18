
# ZAP Scanning Report

Generated on Sun, 18 Jul 2021 01:03:49


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 4 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 6 | 
| Vulnerable JS Library | Medium | 1 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 3 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 4 | 
| Permissions Policy Header Not Set | Low | 6 | 
| Base64 Disclosure | Informational | 5 | 
| Information Disclosure - Suspicious Comments | Informational | 15 | 
| Modern Web Application | Informational | 4 | 
| Retrieved from Cache | Informational | 11 | 
| Storable and Cacheable Content | Informational | 8 | 
| Storable but Non-Cacheable Content | Informational | 3 | 
| Timestamp Disclosure - Unix | Informational | 84 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
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

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `create
function n`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>create</p><p>function n</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600|Roboto:300,400,500|Roboto+Mono" rel="stylesheet" type="text/css" media="all">`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600|Roboto:300,400,500|Roboto+Mono" rel="stylesheet" type="text/css" media="all">`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,600|Roboto:300,400,500|Roboto+Mono" rel="stylesheet" type="text/css" media="all">`
  
  
  
  
Instances: 6
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 3.4.1 is vulnerable.</p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* jQuery JavaScript Library v3.4.1`
  
  
  
  
Instances: 1
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p></p>
  
### Reference
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://analytics.pix.fr/js/container_fNoTNeFZ.js`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://analytics.pix.fr/js/container_fNoTNeFZ.js`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://analytics.pix.fr/js/container_fNoTNeFZ.js`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-287c24c184abe16a29d1583c391e53b1.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-287c24c184abe16a29d1583c391e53b1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `net/v1/AUTH_27c5a6d3d35841a5914c7fb9a8e96345/pix-images/badges/CleA_Num_certif`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `22PAR_pix_cac26b28c15971f8fda41f5a94b1b81647c7b5780582bb169467988b9233c757`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `22PAR_pix_cac26b28c15971f8fda41f5a94b1b81647c7b5780582bb169467988b9233c757`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `22PAR_pix_cac26b28c15971f8fda41f5a94b1b81647c7b5780582bb169467988b9233c757`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�]�㞻�֛qן�\x0018��Y�����ۯ�\x001c�\x0000\x0010�\x0010Q� ��0ӏA\x0014�QU�a</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `BUG`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
Instances: 15
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bLATER\b and was detected 12 times, the first in the element starting with: "Object.defineProperty(e,"__esModule",{value:!0}),e.getCurrentRunLoop=function(){return o},e.run=l,e.join=f,e.begin=function(){u.", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" async defer src="https://analytics.pix.fr/js/container_fNoTNeFZ.js"></script>`
  
  
  
  
Instances: 4
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://app.pix.fr/assets/vendor-b6ad56c488d1991372cc8135cd25943d.css](https://app.pix.fr/assets/vendor-b6ad56c488d1991372cc8135cd25943d.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif](https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-287c24c184abe16a29d1583c391e53b1.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-287c24c184abe16a29d1583c391e53b1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 54790`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/apple-touch-icon-pix_app.png](https://app.pix.fr/apple-touch-icon-pix_app.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 54685`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-17b08228dd0667f208ab881f733d594b.css](https://app.pix.fr/assets/mon-pix-17b08228dd0667f208ab881f733d594b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://app.pix.fr/robots.txt](https://app.pix.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-17b08228dd0667f208ab881f733d594b.css](https://app.pix.fr/assets/mon-pix-17b08228dd0667f208ab881f733d594b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-287c24c184abe16a29d1583c391e53b1.js](https://app.pix.fr/ember-cli-matomo-tag-manager/start-matomo-event-287c24c184abe16a29d1583c391e53b1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif](https://app.pix.fr/images/interwind-5fe40c7fe159b0f34afe8360ab8ae303.gif)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/apple-touch-icon-pix_app.png](https://app.pix.fr/apple-touch-icon-pix_app.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-b6ad56c488d1991372cc8135cd25943d.css](https://app.pix.fr/assets/vendor-b6ad56c488d1991372cc8135cd25943d.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://app.pix.fr/](https://app.pix.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr/sitemap.xml](https://app.pix.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://app.pix.fr](https://app.pix.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1094730640`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `421815835`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1873313359`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16711680`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1126891415`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `165796510`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `01234567`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `660478335`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1560198380`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1859775393`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1530992060`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `187363961`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `536870913`
  
  
  
  
* URL: [https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js](https://app.pix.fr/assets/mon-pix-648c53b93c7c35d605a653c94551ab05.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `315360000`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1926607734`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `315360000`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2054922799`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `701558691`
  
  
  
  
* URL: [https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js](https://app.pix.fr/assets/vendor-0746cbf50120368062ca39aac7c69e5c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1416354905`
  
  
  
  
Instances: 84
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1094730640, which evaluates to: 2004-09-09 11:50:40</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

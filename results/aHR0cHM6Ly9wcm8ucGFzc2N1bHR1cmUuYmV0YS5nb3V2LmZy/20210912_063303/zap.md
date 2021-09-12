
# ZAP Scanning Report

Generated on Sun, 12 Sep 2021 06:28:00


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 3 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 3 | 
| Permissions Policy Header Not Set | Low | 6 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 4 | 
| Retrieved from Cache | Informational | 9 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 34 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
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

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public,max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public,max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public,max-age=3600`
  
  
  
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdskleDLetjgBs_AvO2ythKTidOw16MHOcsc16XjLMdj-4fd6EO6e8nJrfs1cCIptzWZGynbS3-kmpolp4CfoMD5H4ifVw`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycduzckWD4ySxx1Zx8PtGqcS2hpj5EVUUOUnLFk2bU-hcrXs_v2SEcspBjL7R0ThXI0i5CpFhQ1bUX4hahqnL7tk`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdsG84BreadrIoZR9tW6_1smd5YtyovtO-Eyq8A_j_KmuRVl8ZNAaphzTaJkKiqDfOZw_uH6FkZTTk3kNSD17w`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdv9H-9XodXU6e6t1JvmuwKMaqAVf_L4b63d747aqozwwH5-y6U2oBxuHzi64AYuj8ftEszs5XK4DhXLGaEREdA`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.b8153a6e.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.b8153a6e.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdvOn8CmGL3mKzw-v7IDk_87oYsMzfADf9DWLKdOI-2RkNuz4sGjB808VLE_MwCa38vIke7ARH5K_ah2EmEkiOU`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdubOGXy4kTCYFGTZ5ZGD2e39pU9uIpG5MiNRqylzlJEtlv8mHNJtATz-xmZ3LeN47ml3apCFjVCqE3NIwLc8UKvSvzfZQ`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdskleDLetjgBs_AvO2ythKTidOw16MHOcsc16XjLMdj-4fd6EO6e8nJrfs1cCIptzWZGynbS3-kmpolp4CfoMD5H4ifVw`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdsDBGD5lvo2TIt6qz_mSEMGasY5e--sMzZC33SduMm_PfH9Ow75slR4hLHKerT24V0e23mlUxJE5X6ESN06v90`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycds3NFnAjtk36pMlDia8XhT5IwpNyGElD9Kf4hqhHkfa5rqn21QA0jxE-vs1n9GlSKi8TuAX1Bpg-xD2qX3dO6ALsL73MQ`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdtnwwgQmFXV8TJT9fsrQymgy2F9xyfI_LOyLClVNoN5l-MzNfE8lYdPLi5L7gzhdYr8MoanKYGXnOoxT6wDjA`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `ADPycdvPm8ifHbyYK68k2YS7wRXSHVOM30AFi6dgfe8Xa24V5T_eU4hb_9OZIKobiCnsJiqDOxshSRTlHaXyzlUdpsX6X6qasA`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x00003�q�$���z��\x0006����\x0012��Ӱף\x00079�\x001cץ�,�c����C�{�ɭ�5p")�5�\x001b)�K���%������\x001f��W</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "(this["webpackJsonppass-culture-pro"]=this["webpackJsonppass-culture-pro"]||[]).push([[2],[function(e,t,n){"use strict";e.export", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq=window._paq||[];_paq.push([function(){var e,t,a,p=this;this.setVisitorCookieTimeout((e=new Date,t=Math.round(e.getTime()/1e3),a=p.getVisitorInfo(),parseInt(a[2])+33696e3-t))}]),_paq.push(["trackPageView"]),_paq.push(["enableLinkTracking"]),function(){var e="https://matomo.passculture.app/";_paq.push(["setTrackerUrl",e+"matomo.php"]),_paq.push(["setSiteId","1"]);var t=document,a=t.createElement("script"),p=t.getElementsByTagName("script")[0];a.type="text/javascript",a.async=!0,a.defer=!0,a.src=e+"matomo.js",p.parentNode.insertBefore(a,p)}()</script>`
  
  
  
  
Instances: 4
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 80`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 48885`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 44804`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 44804`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 9537`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 82`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 44805`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 48886`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/main.aa032ecf.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/](https://pro.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/main.b8153a6e.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/main.b8153a6e.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/manifest.json](https://pro.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png](https://pro.passculture.beta.gouv.fr/icon/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0511287798`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16711680`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `010101010`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr](https://pro.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631093822`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `01021030`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `314245179`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18764656`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23592600`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435455`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/sitemap.xml](https://pro.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631093822`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/robots.txt](https://pro.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631093822`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `03964659`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123423232`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777216`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0121212121`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css](https://pro.passculture.beta.gouv.fr/static/css/2.53ab2394.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631093822`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `01232425`
  
  
  
  
* URL: [https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js](https://pro.passculture.beta.gouv.fr/static/js/2.17a3e8ed.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012324256`
  
  
  
  
Instances: 34
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0511287798, which evaluates to: 1986-03-15 16:23:18</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

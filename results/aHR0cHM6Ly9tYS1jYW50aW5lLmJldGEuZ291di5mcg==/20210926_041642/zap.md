
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 03:58:02


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cookie No HttpOnly Flag | Low | 11 | 
| Cookie Without Secure Flag | Low | 11 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 6 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 6 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 124 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/s-identifier](https://ma-cantine.beta.gouv.fr/s-identifier)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/s-identifier](https://ma-cantine.beta.gouv.fr/s-identifier)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/s-identifier](https://ma-cantine.beta.gouv.fr/s-identifier)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/s-identifier](https://ma-cantine.beta.gouv.fr/s-identifier)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/app.c7ae86f1.css](https://ma-cantine.beta.gouv.fr/static/css/app.c7ae86f1.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/s-identifier](https://ma-cantine.beta.gouv.fr/s-identifier)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/materialdesignicons.min.css](https://ma-cantine.beta.gouv.fr/static/css/materialdesignicons.min.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/logo_transparent.png](https://ma-cantine.beta.gouv.fr/static/images/logo_transparent.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/app.c7ae86f1.css](https://ma-cantine.beta.gouv.fr/static/css/app.c7ae86f1.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/auth.css](https://ma-cantine.beta.gouv.fr/static/css/auth.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/materialdesignicons.min.css](https://ma-cantine.beta.gouv.fr/static/css/materialdesignicons.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/s-identifier](https://ma-cantine.beta.gouv.fr/s-identifier)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Ku7Uk5RvaJwgONvXQXOlWDyRulJlFaQRQhAWpYKQETLlElTxguf8lp8eZqNTp2fm`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  * Evidence: `kInsStHLdAIrcVhNrDPA2xsafmSz3LtnCan6gyzx3wlgcYeF4CY2LoEw56YDLVg1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>���J��t\x0002+qXM�3��\x001b\x001a~d�ܻg	���,��	`q���&6.�0�\x0003-X5</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 6
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected 3 times, the first in the element starting with: "(function(t){function e(e){for(var n,r,a=e[0],s=e[1],o=0,l=[];o<a.length;o++)r=a[o],Object.prototype.hasOwnProperty.call(i,r)&&i", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d'AURE--17/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGRIA--41/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/](https://ma-cantine.beta.gouv.fr/nos-cantines/RIAB--31/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cuisine%20centrale%20de%20Brian%C3%A7on--43/](https://ma-cantine.beta.gouv.fr/nos-cantines/Cuisine%20centrale%20de%20Brian%C3%A7on--43/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/](https://ma-cantine.beta.gouv.fr/nos-cantines/AGESSO%20RIA%20de%20Caen--33/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/](https://ma-cantine.beta.gouv.fr/nos-cantines/Restaurant%20Interadministratif%20de%20Lyon--40/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"> window.$crisp=[];window.CRISP_WEBSITE_ID="071cca61-bd5f-4950-a5ed-c02238666a5c";(function(){ d=document;s=d.createElement("script"); s.src="https://client.crisp.chat/l.js"; s.async=1;d.getElementsByTagName("head")[0].appendChild(s);})(); </script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/materialdesignicons.min.css](https://ma-cantine.beta.gouv.fr/static/css/materialdesignicons.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d%27AURE--17](https://ma-cantine.beta.gouv.fr/nos-cantines/Coll%C3%A8ge%20Val%20d%27AURE--17)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/app.c7ae86f1.css](https://ma-cantine.beta.gouv.fr/static/css/app.c7ae86f1.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14](https://ma-cantine.beta.gouv.fr/nos-cantines/Cantine%20de%20Misson--14)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `343485551`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1732584193`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `30611744`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `421097727`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1839030562`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `512819199`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `718787259`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147472639`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16843009`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12582911`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `198630844`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `155497632`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1724754687`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `52200625`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `568446438`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `378350505`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777216`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1120210379`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js](https://ma-cantine.beta.gouv.fr/static/js/app.26fbcd6f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1019803690`
  
  
  
  
Instances: 124
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>343485551, which evaluates to: 1980-11-19 12:39:11</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `POST`
  
  
  * Parameter: `first_name`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `POST`
  
  
  * Parameter: `password1`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `POST`
  
  
  * Parameter: `password2`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `POST`
  
  
  * Parameter: `username`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/creer-mon-compte](https://ma-cantine.beta.gouv.fr/creer-mon-compte)
  
  
  * Method: `POST`
  
  
  * Parameter: `last_name`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://ma-cantine.beta.gouv.fr/creer-mon-compte</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>first_name=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

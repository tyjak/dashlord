
# ZAP Scanning Report

Generated on Wed, 23 Jun 2021 02:32:44


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 6 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| Sub Resource Integrity Attribute Missing | Medium | 4 | 
| Cookie No HttpOnly Flag | Low | 4 | 
| Cookie Without Secure Flag | Low | 4 | 
| Incomplete or No Cache-control Header Set | Low | 4 | 
| Permissions Policy Header Not Set | Low | 5 | 
| Strict-Transport-Security Header Not Set | Low | 7 | 
| X-Content-Type-Options Header Missing | Low | 3 | 
| Base64 Disclosure | Informational | 6 | 
| Information Disclosure - Suspicious Comments | Informational | 5 | 
| Modern Web Application | Informational | 6 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 57 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@mdi/font@latest/css/materialdesignicons.min.css">`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@mdi/font@latest/css/materialdesignicons.min.css">`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@mdi/font@latest/css/materialdesignicons.min.css">`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@mdi/font@latest/css/materialdesignicons.min.css">`
  
  
  
  
Instances: 4
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
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
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
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
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/app.43bee420.css](https://ma-cantine.beta.gouv.fr/static/css/app.43bee420.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/app.43bee420.css](https://ma-cantine.beta.gouv.fr/static/css/app.43bee420.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `69rVSECTqO3NwmkjmpGoe4mIzGAduHLV2drSm80gcho16VKguCi9nytdQDr8V80T`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `FSoqfOr0TddOdNjmNdLIEAh0o2cIbC2f1uZUmaclMomCc7m6aMYkW8Y6SWDkiIBB`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  * Evidence: `FSoqfOr0TddOdNjmNdLIEAh0o2cIbC2f1uZUmaclMomCc7m6aMYkW8Y6SWDkiIBB`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `FSoqfOr0TddOdNjmNdLIEAh0o2cIbC2f1uZUmaclMomCc7m6aMYkW8Y6SWDkiIBB`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `FSoqfOr0TddOdNjmNdLIEAh0o2cIbC2f1uZUmaclMomCc7m6aMYkW8Y6SWDkiIBB`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>���H@�����i#���{���`\x001d�r���қ� r\x001a5�R��(��+]@:�W�\x0013</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected 2 times, the first in the element starting with: "var i=Object.freeze({});function n(t){return void 0===t||null===t}function r(t){return void 0!==t&&null!==t}function a(t){return", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">
        window.CSRF_TOKEN = "clUEnAZsljNQqjkAeIQZtvmsTsqRBkLXyXv8uWKNeuWEpDnkBh3BL33ynmRtIqkj";
        window.MATOMO_ID = "162";
    </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">
        window.CSRF_TOKEN = "5cVYSwBRlG1pHtE95kTSCxCGDNUI48sErOwsZSmceRadGNHTsT6uU5jM7Hlkbe10";
        window.MATOMO_ID = "162";
    </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">
        window.CSRF_TOKEN = "qpjbO5mlQgQtGG8onuAAwJmTED0DEgjUmtj8izKICJbHgfylvHclFdtoVARy5HyS";
        window.MATOMO_ID = "162";
    </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">
        window.CSRF_TOKEN = "RYOFoRdk6xojIz7XEn6bDVBx7IYgaiJXdAp9vdYFZIx7HTaH1WjNVtiDBCpShoij";
        window.MATOMO_ID = "162";
    </script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">
        window.CSRF_TOKEN = "mrBFoIcAoVGwhkesKOfGLeHZbberstLxI3c9v4XVh6PkgEhc7nsi3Mo5F5F3zzkT";
        window.MATOMO_ID = "162";
    </script>`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/static/images/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/css/app.43bee420.css](https://ma-cantine.beta.gouv.fr/static/css/app.43bee420.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt/](https://ma-cantine.beta.gouv.fr/robots.txt/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml/](https://ma-cantine.beta.gouv.fr/sitemap.xml/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `536870912`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `548580095`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `175875602`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1088475391`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1724754687`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1687547391`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `275899379`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147472639`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1211993087`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `780883967`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `707106781`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `52882544`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777216`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `793726975`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1097458175`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16711680`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16744447`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js](https://ma-cantine.beta.gouv.fr/static/js/app.8a418e01.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `579543807`
  
  
  
  
Instances: 57
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>536870912, which evaluates to: 1987-01-05 18:48:32</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

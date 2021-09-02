
# ZAP Scanning Report

Generated on Thu, 2 Sep 2021 14:21:20


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 6 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Sub Resource Integrity Attribute Missing | Medium | 6 | 
| X-Frame-Options Header Not Set | Medium | 3 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 5 | 
| Permissions Policy Header Not Set | Low | 4 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 9 | 
| Strict-Transport-Security Header Not Set | Low | 9 | 
| X-Content-Type-Options Header Missing | Low | 10 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 4 | 
| Storable and Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 129 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons"/>`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons"/>`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons"/>`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro&display=swap" rel="stylesheet">`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/robots.txt](https://lesalpps.defense.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/manifest.json](https://lesalpps.defense.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/robots.txt](https://lesalpps.defense.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/img/Favicon.png](https://lesalpps.defense.gouv.fr/img/Favicon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css](https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css](https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/manifest.json](https://lesalpps.defense.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.20.1`
  
  
  
  
Instances: 9
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/img/Favicon.png](https://lesalpps.defense.gouv.fr/img/Favicon.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css](https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/manifest.json](https://lesalpps.defense.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/robots.txt](https://lesalpps.defense.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css](https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/img/Favicon.png](https://lesalpps.defense.gouv.fr/img/Favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/robots.txt](https://lesalpps.defense.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css](https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/manifest.json](https://lesalpps.defense.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css](https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAABsAAAAGCAYAAAAynOUQAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAEpSURBVHgBpZIxUsNADEVXNgUNUOUAbulyjXAAZ4aCdB5o4lyA2fUFslAAodqGIjkAcAt3tD5AaEJtr5BWa0/SZSaa+SOtn7+0HhkURVm/alQ4VxLuafywiLXarSYaFETm3WXxNbDtdKoBxYfkG63XAzPGaADxee+d1noBZf1icWgmQUb9PL43u/eJBVQHDIhdFJ/mN8/Jd8gUoh5tNjTH2H7QXuiEDHdcPV7fBklDLENGCKzzPmPFi5QxB9YCZKzYUHwQfV2XsXp2pk6M85jbI96lL0stF9XPR1B87MINFQaWJknD4pp268QorEVsWNHoYhZfmjYsrnlvwMW8flvScSbNwPK++tv8rW6WNGAmJ2+viu+BbfOcfEoYDed99ayqqoHRIEs/iPkHZw+J/ijnAroAAAAASUVORK5CYII=`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x0000\x001b\x0000\x0000\x0000\x0006\x0008\x0006\x0000\x0000\x00002��\x0010\x0000\x0000\x0000	pHYs\x0000\x0000\x000b\x0013\x0000\x0000\x000b\x0013\x0001\x0000��\x0018\x0000\x0000\x0000\x0001sRGB\x0000��\x001c�\x0000\x0000\x0000\x0004gAMA\x0000\x0000��\x000b�a\x0005\x0000\x0000\x0001)IDATx\x0001��1R�@\x000cEW6\x0005
P�\x0000n�r�p\x0000g��t\x001eh�\���\x0005�P\x0000�چ"9\x0000p\x000bw�>@hBm��VkO�e&��#����\x001e\x0019\x0014EY�jT8W\x0012�i����ڭ&\x001a\x0014D��e�5��t�\x0001Ň�\x001b��\x00033�h\x0000�y��z\x0001e�bqh&AF�<�7���\x0005T\x0007\x000c�]\x0014��7��w�\x0014�\x001em64��~�^�\x000cw\=^�\x0006IC,CF\x0008��>cŋ�1\x0007�\x0002d��P|\x0010}]��zv�N���#ޥ/K-\x0017��GP|��
\x0015\x0006�&I��v��(�ElX��b\x0016_�6,�yo�ż~[�q&�������n�4`&'o���m�|J\x0018
�}������ K?��\x0007g\x000f��(�\x0002�\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "(this.webpackJsonpfrontend=this.webpackJsonpfrontend||[]).push([[0],{183:function(e,t,n){},280:function(e,t,n){"use strict";n.r(", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function r(r){for(var n,i,a=r[0],c=r[1],l=r[2],s=0,p=[];s<a.length;s++)i=a[s],Object.prototype.hasOwnProperty.call(o,i)&&o[i]&&p.push(o[i][0]),o[i]=0;for(n in c)Object.prototype.hasOwnProperty.call(c,n)&&(e[n]=c[n]);for(f&&f(r);p.length;)p.shift()();return u.push.apply(u,l||[]),t()}function t(){for(var e,r=0;r<u.length;r++){for(var t=u[r],n=!0,a=1;a<t.length;a++){var c=t[a];0!==o[c]&&(n=!1)}n&&(u.splice(r--,1),e=i(i.s=t[0]))}return e}var n={},o={1:0},u=[];function i(r){if(n[r])return n[r].exports;var t=n[r]={i:r,l:!1,exports:{}};return e[r].call(t.exports,t,t.exports,i),t.l=!0,t.exports}i.e=function(e){var r=[],t=o[e];if(0!==t)if(t)r.push(t[2]);else{var n=new Promise((function(r,n){t=o[e]=[r,n]}));r.push(t[2]=n);var u,a=document.createElement("script");a.charset="utf-8",a.timeout=120,i.nc&&a.setAttribute("nonce",i.nc),a.src=function(e){return i.p+"static/js/"+({}[e]||e)+"."+{2:"85939541",4:"5e19e800"}[e]+".chunk.js"}(e);var c=new Error;u=function(r){a.onerror=a.onload=null,clearTimeout(l);var t=o[e];if(0!==t){if(t){var n=r&&("load"===r.type?"missing":r.type),u=r&&r.target&&r.target.src;c.message="Loading chunk "+e+" failed.\n("+n+": "+u+")",c.name="ChunkLoadError",c.type=n,c.request=u,t[1](c)}o[e]=void 0}};var l=setTimeout((function(){u({type:"timeout",target:a})}),12e4);a.onerror=a.onload=u,document.head.appendChild(a)}return Promise.all(r)},i.m=e,i.c=n,i.d=function(e,r,t){i.o(e,r)||Object.defineProperty(e,r,{enumerable:!0,get:t})},i.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},i.t=function(e,r){if(1&r&&(e=i(e)),8&r)return e;if(4&r&&"object"==typeof e&&e&&e.__esModule)return e;var t=Object.create(null);if(i.r(t),Object.defineProperty(t,"default",{enumerable:!0,value:e}),2&r&&"string"!=typeof e)for(var n in e)i.d(t,n,function(r){return e[r]}.bind(null,n));return t},i.n=function(e){var r=e&&e.__esModule?function(){return e.default}:function(){return e};return i.d(r,"a",r),r},i.o=function(e,r){return Object.prototype.hasOwnProperty.call(e,r)},i.p="/",i.oe=function(e){throw console.error(e),e};var a=this.webpackJsonpfrontend=this.webpackJsonpfrontend||[],c=a.push.bind(a);a.push=r,a=a.slice();for(var l=0;l<a.length;l++)r(a[l]);var f=c;t()}([])</script>`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function r(r){for(var n,i,a=r[0],c=r[1],l=r[2],s=0,p=[];s<a.length;s++)i=a[s],Object.prototype.hasOwnProperty.call(o,i)&&o[i]&&p.push(o[i][0]),o[i]=0;for(n in c)Object.prototype.hasOwnProperty.call(c,n)&&(e[n]=c[n]);for(f&&f(r);p.length;)p.shift()();return u.push.apply(u,l||[]),t()}function t(){for(var e,r=0;r<u.length;r++){for(var t=u[r],n=!0,a=1;a<t.length;a++){var c=t[a];0!==o[c]&&(n=!1)}n&&(u.splice(r--,1),e=i(i.s=t[0]))}return e}var n={},o={1:0},u=[];function i(r){if(n[r])return n[r].exports;var t=n[r]={i:r,l:!1,exports:{}};return e[r].call(t.exports,t,t.exports,i),t.l=!0,t.exports}i.e=function(e){var r=[],t=o[e];if(0!==t)if(t)r.push(t[2]);else{var n=new Promise((function(r,n){t=o[e]=[r,n]}));r.push(t[2]=n);var u,a=document.createElement("script");a.charset="utf-8",a.timeout=120,i.nc&&a.setAttribute("nonce",i.nc),a.src=function(e){return i.p+"static/js/"+({}[e]||e)+"."+{2:"85939541",4:"5e19e800"}[e]+".chunk.js"}(e);var c=new Error;u=function(r){a.onerror=a.onload=null,clearTimeout(l);var t=o[e];if(0!==t){if(t){var n=r&&("load"===r.type?"missing":r.type),u=r&&r.target&&r.target.src;c.message="Loading chunk "+e+" failed.\n("+n+": "+u+")",c.name="ChunkLoadError",c.type=n,c.request=u,t[1](c)}o[e]=void 0}};var l=setTimeout((function(){u({type:"timeout",target:a})}),12e4);a.onerror=a.onload=u,document.head.appendChild(a)}return Promise.all(r)},i.m=e,i.c=n,i.d=function(e,r,t){i.o(e,r)||Object.defineProperty(e,r,{enumerable:!0,get:t})},i.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},i.t=function(e,r){if(1&r&&(e=i(e)),8&r)return e;if(4&r&&"object"==typeof e&&e&&e.__esModule)return e;var t=Object.create(null);if(i.r(t),Object.defineProperty(t,"default",{enumerable:!0,value:e}),2&r&&"string"!=typeof e)for(var n in e)i.d(t,n,function(r){return e[r]}.bind(null,n));return t},i.n=function(e){var r=e&&e.__esModule?function(){return e.default}:function(){return e};return i.d(r,"a",r),r},i.o=function(e,r){return Object.prototype.hasOwnProperty.call(e,r)},i.p="/",i.oe=function(e){throw console.error(e),e};var a=this.webpackJsonpfrontend=this.webpackJsonpfrontend||[],c=a.push.bind(a);a.push=r,a=a.slice();for(var l=0;l<a.length;l++)r(a[l]);var f=c;t()}([])</script>`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>!function(e){function r(r){for(var n,i,a=r[0],c=r[1],l=r[2],s=0,p=[];s<a.length;s++)i=a[s],Object.prototype.hasOwnProperty.call(o,i)&&o[i]&&p.push(o[i][0]),o[i]=0;for(n in c)Object.prototype.hasOwnProperty.call(c,n)&&(e[n]=c[n]);for(f&&f(r);p.length;)p.shift()();return u.push.apply(u,l||[]),t()}function t(){for(var e,r=0;r<u.length;r++){for(var t=u[r],n=!0,a=1;a<t.length;a++){var c=t[a];0!==o[c]&&(n=!1)}n&&(u.splice(r--,1),e=i(i.s=t[0]))}return e}var n={},o={1:0},u=[];function i(r){if(n[r])return n[r].exports;var t=n[r]={i:r,l:!1,exports:{}};return e[r].call(t.exports,t,t.exports,i),t.l=!0,t.exports}i.e=function(e){var r=[],t=o[e];if(0!==t)if(t)r.push(t[2]);else{var n=new Promise((function(r,n){t=o[e]=[r,n]}));r.push(t[2]=n);var u,a=document.createElement("script");a.charset="utf-8",a.timeout=120,i.nc&&a.setAttribute("nonce",i.nc),a.src=function(e){return i.p+"static/js/"+({}[e]||e)+"."+{2:"85939541",4:"5e19e800"}[e]+".chunk.js"}(e);var c=new Error;u=function(r){a.onerror=a.onload=null,clearTimeout(l);var t=o[e];if(0!==t){if(t){var n=r&&("load"===r.type?"missing":r.type),u=r&&r.target&&r.target.src;c.message="Loading chunk "+e+" failed.\n("+n+": "+u+")",c.name="ChunkLoadError",c.type=n,c.request=u,t[1](c)}o[e]=void 0}};var l=setTimeout((function(){u({type:"timeout",target:a})}),12e4);a.onerror=a.onload=u,document.head.appendChild(a)}return Promise.all(r)},i.m=e,i.c=n,i.d=function(e,r,t){i.o(e,r)||Object.defineProperty(e,r,{enumerable:!0,get:t})},i.r=function(e){"undefined"!=typeof Symbol&&Symbol.toStringTag&&Object.defineProperty(e,Symbol.toStringTag,{value:"Module"}),Object.defineProperty(e,"__esModule",{value:!0})},i.t=function(e,r){if(1&r&&(e=i(e)),8&r)return e;if(4&r&&"object"==typeof e&&e&&e.__esModule)return e;var t=Object.create(null);if(i.r(t),Object.defineProperty(t,"default",{enumerable:!0,value:e}),2&r&&"string"!=typeof e)for(var n in e)i.d(t,n,function(r){return e[r]}.bind(null,n));return t},i.n=function(e){var r=e&&e.__esModule?function(){return e.default}:function(){return e};return i.d(r,"a",r),r},i.o=function(e,r){return Object.prototype.hasOwnProperty.call(e,r)},i.p="/",i.oe=function(e){throw console.error(e),e};var a=this.webpackJsonpfrontend=this.webpackJsonpfrontend||[],c=a.push.bind(a);a.push=r,a=a.slice();for(var l=0;l<a.length;l++)r(a[l]);var f=c;t()}([])</script>`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script >`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/manifest.json](https://lesalpps.defense.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js](https://lesalpps.defense.gouv.fr/static/js/main.093ab984.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/logo192.png](https://lesalpps.defense.gouv.fr/logo192.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css](https://lesalpps.defense.gouv.fr/static/css/main.570535e8.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/img/Favicon.png](https://lesalpps.defense.gouv.fr/img/Favicon.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/robots.txt](https://lesalpps.defense.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css](https://lesalpps.defense.gouv.fr/static/css/3.05172ee9.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/sitemap.xml](https://lesalpps.defense.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/](https://lesalpps.defense.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1804603682`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1163531501`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `30611744`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `512819199`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `421097727`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000000`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1768516095`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `343485551`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1958414417`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16843009`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12582911`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `718787259`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `306562965`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1732584193`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1735328473`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2070474495`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `187363961`
  
  
  
  
* URL: [https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js](https://lesalpps.defense.gouv.fr/static/js/3.b895c170.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13554175`
  
  
  
  
Instances: 129
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>2147483647, which evaluates to: 2038-01-19 03:14:07</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

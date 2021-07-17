
# ZAP Scanning Report

Generated on Sat, 17 Jul 2021 07:56:57


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
| Application Error Disclosure | Medium | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| X-Frame-Options Header Not Set | Medium | 1 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 5 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
| Modern Web Application | Informational | 5 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Application Error Disclosure
##### Medium (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_error-731f356b399cb5b12adf.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_error-731f356b399cb5b12adf.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
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
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
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

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 1
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js)
  
  
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

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
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
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_error-731f356b399cb5b12adf.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_error-731f356b399cb5b12adf.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/image?q=75&url=%2Fstatic%2Fimages%2Fmes-adresses.svg&w=640](https://mes-adresses.data.gouv.fr/_next/image?q=75&url=%2Fstatic%2Fimages%2Fmes-adresses.svg&w=640)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js)
  
  
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
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `leftRotate360InAnimation_1uxpfmf`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/image?q=75&url=%2Fstatic%2Fimages%2Fmes-adresses.svg&w=640](https://mes-adresses.data.gouv.fr/_next/image?q=75&url=%2Fstatic%2Fimages%2Fmes-adresses.svg&w=640)
  
  
  * Method: `GET`
  
  
  * Evidence: `Rcm9Psr4oSno8Thfn7UlTAv2qD6RpfOEQEJL-E1yibo=`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `leftRotate360InAnimation_1uxpfmf`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `leftRotate360InAnimation_1uxpfmf`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>���F�Z���Љ��)��*'�[����</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 9
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "(self.webpackChunk_N_E=self.webpackChunk_N_E||[]).push([[5405],{50736:function(e,n,t){"use strict";t.d(n,{Z:function(){return g}", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" nomodule="" src="/_next/static/chunks/polyfills-b69b38e0e606287ba003.js"></script>`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" nomodule="" src="/_next/static/chunks/polyfills-b69b38e0e606287ba003.js"></script>`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/main-afe9a336274088386655.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/_app-99ac6f84b68dfdc07e9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_ssgManifest.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/polyfills-b69b38e0e606287ba003.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/robots.txt](https://mes-adresses.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/webpack-37127a7fa72495b077f5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/framework-336caa3f6419768205fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js](https://mes-adresses.data.gouv.fr/_next/static/chunks/pages/index-a7b90c9d8042bc5013f1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/sitemap.xml](https://mes-adresses.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js](https://mes-adresses.data.gouv.fr/_next/static/pihnpXjolZIeHE1UGgsmr/_buildManifest.js)
  
  
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
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `96931717`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000000`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `75130096`
  
  
  
  
* URL: [https://mes-adresses.data.gouv.fr/](https://mes-adresses.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `23333333`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>96931717, which evaluates to: 1973-01-26 21:28:37</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

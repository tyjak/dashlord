
# ZAP Scanning Report

Generated on Sun, 6 Jun 2021 02:00:21


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
| Content Security Policy (CSP) Header Not Set | Medium | 5 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 7 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 9 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 2 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 6 | 
| Non-Storable Content | Informational | 5 | 
| Storable and Cacheable Content | Informational | 6 | 
| Timestamp Disclosure - Unix | Informational | 162 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.c740d73b.chunk.js](https://datapass.api.gouv.fr/static/js/main.c740d73b.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css](https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.7509bdb2.chunk.css](https://datapass.api.gouv.fr/static/css/main.7509bdb2.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 9
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css](https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css](https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `org/TR/2001/REC-SVG-20010904/DTD/svg10`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.c740d73b.chunk.js](https://datapass.api.gouv.fr/static/js/main.c740d73b.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/loda/article_lc/LEGIARTI000039755126`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��?M\x001f��MD@�IQ��M5��8�4�����</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.c740d73b.chunk.js](https://datapass.api.gouv.fr/static/js/main.c740d73b.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `xxx`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bXXX\b and was detected in the element starting with: "(this.webpackJsonpdatapass=this.webpackJsonpdatapass||[]).push([[0],{134:function(e,t,n){},158:function(e,t,n){},225:function(e)", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css](https://datapass.api.gouv.fr/static/css/2.a84d3c63.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `680876936`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `530742520`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16770229`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16758465`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `643717713`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `373897302`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1926607734`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1272893353`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741824`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `271733878`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16119260`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16113331`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15308410`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11119017`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10025880`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `358537222`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js](https://datapass.api.gouv.fr/static/js/2.88b996b2.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16775885`
  
  
  
  
Instances: 162
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>268435456, which evaluates to: 1978-07-04 21:24:16</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

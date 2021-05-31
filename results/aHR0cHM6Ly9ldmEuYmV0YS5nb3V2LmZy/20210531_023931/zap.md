
# ZAP Scanning Report

Generated on Mon, 31 May 2021 02:35:12


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 4 |
| Informational | 3 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 7 | 
| X-Frame-Options Header Not Set | Medium | 6 | 
| Feature Policy Header Not Set | Low | 7 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Modern Web Application | Informational | 6 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 3 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cgu/](https://eva.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/statistiques/](https://eva.beta.gouv.fr/statistiques/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/statistiques/](https://eva.beta.gouv.fr/statistiques/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cgu/](https://eva.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cgu/](https://eva.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/statistiques/](https://eva.beta.gouv.fr/statistiques/)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/favicon.svg](https://eva.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/objectif1.svg](https://eva.beta.gouv.fr/objectif1.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap.xml](https://eva.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/marianne.svg](https://eva.beta.gouv.fr/marianne.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/eva.svg](https://eva.beta.gouv.fr/eva.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/fleche.svg](https://eva.beta.gouv.fr/fleche.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/eva.svg](https://eva.beta.gouv.fr/eva.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/marianne.svg](https://eva.beta.gouv.fr/marianne.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap.xml](https://eva.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/fleche.svg](https://eva.beta.gouv.fr/fleche.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/favicon.svg](https://eva.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/favicon.svg](https://eva.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/objectif1.svg](https://eva.beta.gouv.fr/objectif1.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap.xml](https://eva.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/marianne.svg](https://eva.beta.gouv.fr/marianne.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/eva.svg](https://eva.beta.gouv.fr/eva.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/fleche.svg](https://eva.beta.gouv.fr/fleche.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
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

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="lien-menu font-weight-bold">Menu</a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="lien-menu font-weight-bold">Menu</a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="lien-menu font-weight-bold">Menu</a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="lien-menu font-weight-bold">Menu</a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/statistiques/](https://eva.beta.gouv.fr/statistiques/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="lien-menu font-weight-bold">Menu</a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cgu/](https://eva.beta.gouv.fr/cgu/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="lien-menu font-weight-bold">Menu</a>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/statistiques](https://eva.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous](https://eva.beta.gouv.fr/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cas-usage/](https://eva.beta.gouv.fr/cas-usage/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/favicon.svg](https://eva.beta.gouv.fr/favicon.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/cgu](https://eva.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap.xml](https://eva.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `66666667`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `33333333`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css](https://eva.beta.gouv.fr/sass/main.min.b6708017847ea20b8e48f9f9e2480b92587a48c92fe0e91c92273928fe337f54.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `85714286`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>66666667, which evaluates to: 1972-02-11 14:31:07</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

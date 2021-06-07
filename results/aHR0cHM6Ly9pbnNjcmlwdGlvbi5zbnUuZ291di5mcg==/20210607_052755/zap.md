
# ZAP Scanning Report

Generated on Mon, 7 Jun 2021 05:08:59


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 4 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Application Error Disclosure | Medium | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| X-Frame-Options Header Not Set | Medium | 3 | 
| Feature Policy Header Not Set | Low | 3 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 4 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 6 | 
| X-Content-Type-Options Header Missing | Low | 6 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 3 | 
| Storable but Non-Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 21 | 

## Alert Detail


  
  
  
  
### Application Error Disclosure
##### Medium (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/robots.txt](https://inscription.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
Instances: 4
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/robots.txt](https://inscription.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/favicon.ico](https://inscription.snu.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/robots.txt](https://inscription.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/favicon.ico](https://inscription.snu.gouv.fr/favicon.ico)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FROM`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 2 times, the first in the element starting with: "var _typeof2="function"==typeof Symbol&&"symbol"==typeof Symbol.iterator?function(e){return typeof e}:function(e){return e&&"fun", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type=text/javascript>window.$crisp = [];
      window.CRISP_WEBSITE_ID = "9a0b4de6-fa09-4356-9db0-15d4c3a40f42";
      (function () {
        d = document;
        s = d.createElement("script");
        s.src = "https://client.crisp.chat/l.js";
        s.async = 1;
        d.getElementsByTagName("head")[0].appendChild(s);
      })();</script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type=text/javascript>window.$crisp = [];
      window.CRISP_WEBSITE_ID = "9a0b4de6-fa09-4356-9db0-15d4c3a40f42";
      (function () {
        d = document;
        s = d.createElement("script");
        s.src = "https://client.crisp.chat/l.js";
        s.async = 1;
        d.getElementsByTagName("head")[0].appendChild(s);
      })();</script>`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type=text/javascript>window.$crisp = [];
      window.CRISP_WEBSITE_ID = "9a0b4de6-fa09-4356-9db0-15d4c3a40f42";
      (function () {
        d = document;
        s = d.createElement("script");
        s.src = "https://client.crisp.chat/l.js";
        s.async = 1;
        d.getElementsByTagName("head")[0].appendChild(s);
      })();</script>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://inscription.snu.gouv.fr/](https://inscription.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/robots.txt](https://inscription.snu.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr](https://inscription.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/favicon.ico](https://inscription.snu.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/sitemap.xml](https://inscription.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1540483477`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62425156`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13456789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012356789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2146828260`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12356789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012345689`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `01235678`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `45945784`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `57186127`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `279091964`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `880078594`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `99999999`
  
  
  
  
* URL: [https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js](https://inscription.snu.gouv.fr/b208b39610b88e3dcc84.index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `123456789`
  
  
  
  
Instances: 21
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1540483477, which evaluates to: 2018-10-25 16:04:37</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Fri, 30 Apr 2021 02:58:09


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 5 | 
| Reverse Tabnabbing | Medium | 5 | 
| X-Frame-Options Header Not Set | Medium | 5 | 
| Absence of Anti-CSRF Tokens | Low | 5 | 
| Cookie Without Secure Flag | Low | 8 | 
| Feature Policy Header Not Set | Low | 5 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 7 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 10 | 
| X-Content-Type-Options Header Missing | Low | 10 | 
| Base64 Disclosure | Informational | 12 | 
| Modern Web Application | Informational | 3 | 
| Non-Storable Content | Informational | 4 | 
| Storable and Cacheable Content | Informational | 3 | 
| Storable but Non-Cacheable Content | Informational | 3 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 13 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://doc.incubateur.net/communaute/outils/emails#jai-un-email-beta-comment-me-connecter" target="_blank" title="lien vers la documentation pour se connecter à sa boite mail">documentation de l'incubateur</a>`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://doc.incubateur.net/communaute/outils/emails#jai-un-email-beta-comment-me-connecter" target="_blank" title="lien vers la documentation pour se connecter à sa boite mail">documentation de l'incubateur</a>`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://doc.incubateur.net/communaute/outils/emails#jai-un-email-beta-comment-me-connecter" target="_blank" title="lien vers la documentation pour se connecter à sa boite mail">documentation de l'incubateur</a>`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/communaute/" target="_blank">Communauté</a>`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/communaute/" target="_blank">Communauté</a>`
  
  
  
  
Instances: 5
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 5
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/login?next=/robots.txt" method="POST" id="login_form" onsubmit="event.submitter && (event.submitter.disabled = true);">`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/login" method="POST" id="login_form" onsubmit="event.submitter && (event.submitter.disabled = true);">`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form action="/onboarding" method="POST" onsubmit="event.submitter && (event.submitter.disabled = true);">`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/onboarding" method="POST" onsubmit="event.submitter && (event.submitter.disabled = true);">`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/login?next=/sitemap.xml" method="POST" id="login_form" onsubmit="event.submitter && (event.submitter.disabled = true);">`
  
  
  
  
Instances: 5
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "username" "secondary_email_input" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://secretariat.incubateur.net](https://secretariat.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/](https://secretariat.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/robots.txt](https://secretariat.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/sitemap.xml](https://secretariat.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `POST`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `POST`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
Instances: 8
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/site.webmanifest](https://secretariat.incubateur.net/static/favicon/site.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/css/main.css](https://secretariat.incubateur.net/static/css/main.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://secretariat.incubateur.net/robots.txt](https://secretariat.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/sitemap.xml](https://secretariat.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/favicon-16x16.png](https://secretariat.incubateur.net/static/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/](https://secretariat.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/favicon-32x32.png](https://secretariat.incubateur.net/static/favicon/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net](https://secretariat.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/apple-touch-icon.png](https://secretariat.incubateur.net/static/favicon/apple-touch-icon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/css/main.css](https://secretariat.incubateur.net/static/css/main.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/apple-touch-icon.png](https://secretariat.incubateur.net/static/favicon/apple-touch-icon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/favicon-16x16.png](https://secretariat.incubateur.net/static/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/favicon-32x32.png](https://secretariat.incubateur.net/static/favicon/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/site.webmanifest](https://secretariat.incubateur.net/static/favicon/site.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://secretariat.incubateur.net/static/css/main.css](https://secretariat.incubateur.net/static/css/main.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKBAMAAAB/HNKOAAAAD1BMVEUAAACjo6Pn5+fDw8P///8mXC3WAAAABHRSTlMAfb49zZRSvgAAADBJREFUCNdjAAIXFxBicmFwYGAQUQGSjI4sQFJEgIHBgdmRAUgyGAAxUBZOugCBAwCrDAY9nvSvKAAAAABJRU5ErkJggg==`
  
  
  
  
* URL: [https://secretariat.incubateur.net/sitemap.xml](https://secretariat.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3Ab3getnHBqvq-mbBWxcyfsD_-SkGwUoX-`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `POST`
  
  
  * Evidence: `3Ab3getnHBqvq-mbBWxcyfsD_-SkGwUoX-`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `116d-GnFUEiiuFkRSKLBEcy2eRDR7KFc`
  
  
  
  
* URL: [https://secretariat.incubateur.net/robots.txt](https://secretariat.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3A0W1FjEQJOoB1zRlk7BmlNB-qo1ax11VE`
  
  
  
  
* URL: [https://secretariat.incubateur.net/](https://secretariat.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `3A4qwmI0zuYMrRyWW0R5BaYilJJ5PYdrss`
  
  
  
  
* URL: [https://secretariat.incubateur.net](https://secretariat.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `3Ab3getnHBqvq-mbBWxcyfsD_-SkGwUoX-`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `10b6-AydOOq0SiSF08Nr71ncgFZmXVuY`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `POST`
  
  
  * Evidence: `3Ab3getnHBqvq-mbBWxcyfsD_-SkGwUoX-`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `10c8-yk1EaEpWO89HcUjEKWAIQwbZpsQ`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `10c7-y1u3xPmtRE0gYK4qWCqVurEi6ho`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `POST`
  
  
  * Evidence: `3Ab3getnHBqvq-mbBWxcyfsD_-SkGwUoX-`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x0000</p><p>\x0000\x0000\x0000</p><p>\x0004\x0003\x0000\x0000\x0000\x001cҎ\x0000\x0000\x0000\x000fPLTE\x0000\x0000\x0000������������&\-�\x0000\x0000\x0000\x0004tRNS\x0000}�=͔R�\x0000\x0000\x00000IDAT\x0008�c\x0000\x0002\x0017\x0017\x0010brap``\x0010Q\x0001���,@RD����ّ\x0001H2\x0018\x00001P\x0016N�\x0000�\x0003\x0000�\x000c\x0006=���(\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="secondary_email_button">
            Recevoir le lien de connexion sur mon adresse secondaire
          </a>`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="secondary_email_button">
            Recevoir le lien de connexion sur mon adresse secondaire
          </a>`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="secondary_email_button">
            Recevoir le lien de connexion sur mon adresse secondaire
          </a>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://secretariat.incubateur.net](https://secretariat.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://secretariat.incubateur.net/sitemap.xml](https://secretariat.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://secretariat.incubateur.net/robots.txt](https://secretariat.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://secretariat.incubateur.net/](https://secretariat.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://secretariat.incubateur.net/login](https://secretariat.incubateur.net/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/robots.txt](https://secretariat.incubateur.net/login?next=/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://secretariat.incubateur.net/login?next=/sitemap.xml](https://secretariat.incubateur.net/login?next=/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/favicon-16x16.png](https://secretariat.incubateur.net/static/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/apple-touch-icon.png](https://secretariat.incubateur.net/static/favicon/apple-touch-icon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://secretariat.incubateur.net/static/favicon/favicon-32x32.png](https://secretariat.incubateur.net/static/favicon/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
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

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `start`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `status`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `startup`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `end`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `employer`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `lastName`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `role`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `website`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `github`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `referentList`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `badge`
  
  
  
  
* URL: [https://secretariat.incubateur.net/onboarding](https://secretariat.incubateur.net/onboarding)
  
  
  * Method: `POST`
  
  
  * Parameter: `firstName`
  
  
  
  
Instances: 13
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://secretariat.incubateur.net/onboarding</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>email=foo-bar@example.com</p><p></p><p>The user-controlled value was:</p><p>foo-bar@example.com</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

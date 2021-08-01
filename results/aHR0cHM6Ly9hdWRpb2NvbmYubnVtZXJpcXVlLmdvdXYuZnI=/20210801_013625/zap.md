
# ZAP Scanning Report

Generated on Sun, 1 Aug 2021 01:25:17


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 6 |
| Informational | 3 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: Wildcard Directive | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 6 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| Cookie without SameSite Attribute | Low | 11 | 
| Cookie Without Secure Flag | Low | 11 | 
| Incomplete or No Cache-control Header Set | Low | 6 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 1 | 

## Alert Detail


  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/robots.txt](https://audioconf.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/sitemap.xml](https://audioconf.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 6
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/valider-email" method="POST">`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/valider-email" method="POST">`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "email" "userTimezoneOffset" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-16x16.png](https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/sitemap.xml](https://audioconf.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css](https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/css/custom.css](https://audioconf.numerique.gouv.fr/static/css/custom.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/robots.txt](https://audioconf.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/sitemap.xml](https://audioconf.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/robots.txt](https://audioconf.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `connect.sid`
  
  
  * Evidence: `Set-Cookie: connect.sid`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/robots.txt](https://audioconf.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `sc-sticky-session`
  
  
  * Evidence: `Set-Cookie: sc-sticky-session`
  
  
  
  
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
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 6
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/sitemap.xml](https://audioconf.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/robots.txt](https://audioconf.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/css/custom.css](https://audioconf.numerique.gouv.fr/static/css/custom.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-16x16.png](https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css](https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-16x16.png](https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/remixicon/remixicon.css](https://audioconf.numerique.gouv.fr/static/remixicon/remixicon.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-32x32.png](https://audioconf.numerique.gouv.fr/static/images/favicon/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css](https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/css/custom.css](https://audioconf.numerique.gouv.fr/static/css/custom.css)
  
  
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

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/questions-frequentes](https://audioconf.numerique.gouv.fr/questions-frequentes)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/stats](https://audioconf.numerique.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/contact](https://audioconf.numerique.gouv.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/mentions-legales](https://audioconf.numerique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
Instances: 6
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bTODO\b and was detected in the element starting with: "<!-- todo(estellecomment) : import min css and js -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr](https://audioconf.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/gouvfr/js/dsfr.nomodule.min.js](https://audioconf.numerique.gouv.fr/static/gouvfr/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/](https://audioconf.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/gouvfr/js/dsfr.module.min.js](https://audioconf.numerique.gouv.fr/static/gouvfr/js/dsfr.module.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script></p><p>  // Fill in the hidden input with the user's timezoneOffset</p><p>  document.getElementById('userTimezoneOffset').value = ne", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css](https://audioconf.numerique.gouv.fr/static/gouvfr/css/dsfr.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>23000091, which evaluates to: 1970-09-24 04:54:51</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

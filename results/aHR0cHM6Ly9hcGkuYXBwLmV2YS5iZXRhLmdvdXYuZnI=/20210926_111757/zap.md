
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 11:10:11


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 5 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 10 | 
| Reverse Tabnabbing | Medium | 10 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| Dangerous JS Functions | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 10 | 
| Permissions Policy Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 13 | 
| Modern Web Application | Informational | 1 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 2 | 
| Storable but Non-Cacheable Content | Informational | 4 | 
| Timestamp Disclosure - Unix | Informational | 8 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 9 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures](https://api.app.eva.beta.gouv.fr/pro/structures)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password/new](https://api.app.eva.beta.gouv.fr/pro/admin/password/new)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=58a5e24c-2a68-42a8-9b2c-d021211454b1](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=58a5e24c-2a68-42a8-9b2c-d021211454b1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=40832e76-b3e4-4c54-8f12-fa2e3168cd03](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=40832e76-b3e4-4c54-8f12-fa2e3168cd03)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=7e85d45c-901e-48e5-999f-9a6469ab1438](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=7e85d45c-901e-48e5-999f-9a6469ab1438)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/fonts/fonts/quicksand-v21-latin-ext-600.eot](https://api.app.eva.beta.gouv.fr/fonts/fonts/quicksand-v21-latin-ext-600.eot)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures](https://api.app.eva.beta.gouv.fr/pro/structures)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password/new](https://api.app.eva.beta.gouv.fr/pro/admin/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=7e85d45c-901e-48e5-999f-9a6469ab1438](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=7e85d45c-901e-48e5-999f-9a6469ab1438)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=58a5e24c-2a68-42a8-9b2c-d021211454b1](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=58a5e24c-2a68-42a8-9b2c-d021211454b1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=40832e76-b3e4-4c54-8f12-fa2e3168cd03](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=40832e76-b3e4-4c54-8f12-fa2e3168cd03)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=86c6e6aa-89ae-4499-a4c5-5b63fe807a77](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=86c6e6aa-89ae-4499-a4c5-5b63fe807a77)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://beta.gouv.fr/startups/eva.html' target='_blank'>l'équipe</a>`
  
  
  
  
Instances: 10
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select an item if the close event was triggered from a select or`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>select an item if the close event was triggered from a select or</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/pro/structures" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures](https://api.app.eva.beta.gouv.fr/pro/structures)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/pro/structures" accept-charset="UTF-8" method="get">`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "code_postal" "commit" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=40832e76-b3e4-4c54-8f12-fa2e3168cd03](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=40832e76-b3e4-4c54-8f12-fa2e3168cd03)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=58a5e24c-2a68-42a8-9b2c-d021211454b1](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=58a5e24c-2a68-42a8-9b2c-d021211454b1)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password/new](https://api.app.eva.beta.gouv.fr/pro/admin/password/new)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/robots.txt](https://api.app.eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures](https://api.app.eva.beta.gouv.fr/pro/structures)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=7e85d45c-901e-48e5-999f-9a6469ab1438](https://api.app.eva.beta.gouv.fr/pro/admin/sign_up?structure_id=7e85d45c-901e-48e5-999f-9a6469ab1438)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/crisp-0cdb52e97a8175967589f459e6a7a00ab05237e189bb8ee7f43234841affadce.js](https://api.app.eva.beta.gouv.fr/assets/crisp-0cdb52e97a8175967589f459e6a7a00ab05237e189bb8ee7f43234841affadce.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/tarteaucitron-init-8366dce1b7076969e2f62221b4f268870e53182b28ac0083f38ca69dfb3e407f.js](https://api.app.eva.beta.gouv.fr/assets/tarteaucitron-init-8366dce1b7076969e2f62221b4f268870e53182b28ac0083f38ca69dfb3e407f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures](https://api.app.eva.beta.gouv.fr/pro/structures)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password/new](https://api.app.eva.beta.gouv.fr/pro/admin/password/new)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/matomo-75b4015c59015d5b7d36ba83f4e4cd865f731ef31a7d7d087ff8d76e6887ad05.js](https://api.app.eva.beta.gouv.fr/assets/matomo-75b4015c59015d5b7d36ba83f4e4cd865f731ef31a7d7d087ff8d76e6887ad05.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/hotjar-6a996681b3ba34095a6aebd9c022c7b7372f0d32a1b8ece49b973faa138a1e7e.js](https://api.app.eva.beta.gouv.fr/assets/hotjar-6a996681b3ba34095a6aebd9c022c7b7372f0d32a1b8ece49b973faa138a1e7e.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-02693b852d7e3124d36a8082c54eaa895c0cc864c3019dc5eca6e4832d4c7d4c.eot](https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-02693b852d7e3124d36a8082c54eaa895c0cc864c3019dc5eca6e4832d4c7d4c.eot)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/matomo-75b4015c59015d5b7d36ba83f4e4cd865f731ef31a7d7d087ff8d76e6887ad05.js](https://api.app.eva.beta.gouv.fr/assets/matomo-75b4015c59015d5b7d36ba83f4e4cd865f731ef31a7d7d087ff8d76e6887ad05.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/hotjar-6a996681b3ba34095a6aebd9c022c7b7372f0d32a1b8ece49b973faa138a1e7e.js](https://api.app.eva.beta.gouv.fr/assets/hotjar-6a996681b3ba34095a6aebd9c022c7b7372f0d32a1b8ece49b973faa138a1e7e.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-fcf21b10ffc47ced95e268ebf538f2cefe1e7dca0584b866013421d48eb43148.woff](https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-fcf21b10ffc47ced95e268ebf538f2cefe1e7dca0584b866013421d48eb43148.woff)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/tarteaucitron-init-8366dce1b7076969e2f62221b4f268870e53182b28ac0083f38ca69dfb3e407f.js](https://api.app.eva.beta.gouv.fr/assets/tarteaucitron-init-8366dce1b7076969e2f62221b4f268870e53182b28ac0083f38ca69dfb3e407f.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-161d778549da0741b52bffa3f79cab31c2c4fdc5b8e1cf65e0ce5fe5dc3eb1a8.woff2](https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-161d778549da0741b52bffa3f79cab31c2c4fdc5b8e1cf65e0ce5fe5dc3eb1a8.woff2)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/favicon-9cb00fa57f14c3f09addede84483c24aeaafc57ab4c7b11442907120c0492d95.svg](https://api.app.eva.beta.gouv.fr/assets/favicon-9cb00fa57f14c3f09addede84483c24aeaafc57ab4c7b11442907120c0492d95.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-807d23576d9cd898ddaf40f14bb42fcac7c2add44211f87357bd82dbebfb38d9.css](https://api.app.eva.beta.gouv.fr/assets/active_admin-807d23576d9cd898ddaf40f14bb42fcac7c2add44211f87357bd82dbebfb38d9.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/robots.txt](https://api.app.eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/crisp-0cdb52e97a8175967589f459e6a7a00ab05237e189bb8ee7f43234841affadce.js](https://api.app.eva.beta.gouv.fr/assets/crisp-0cdb52e97a8175967589f459e6a7a00ab05237e189bb8ee7f43234841affadce.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Evidence: `H3bV2eq8gRDiUGJt73Gv47jq1TeLvF33bFN`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password/new](https://api.app.eva.beta.gouv.fr/pro/admin/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BhAZL6YCG4n3NSKTpESGHGPCDlIPJnfauBhbIO8`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  * Evidence: `2BXi5koLvpu77c3zbXzqNeLuYPyZJa`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `5vLynxYtfKnmZVBtMlwQ4HCIAMLB9WRLgyMQsRprgCe7T3HIvoCz7X`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FfCOd0BtqwcYhiJN8G0moUxoYRIKRtwB0fNHNrjfTX6JOSX7jkceb0e`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures](https://api.app.eva.beta.gouv.fr/pro/structures)
  
  
  * Method: `GET`
  
  
  * Evidence: `ai6FNUDidT43i2G9RGCEuybc1LErPj8p5Q5xhSt6anxhsVRVFZ9`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  * Evidence: `ZXFUYRKchKEm_kw0z6JFqWY_pLHeVKxoOz1UB1JC2kTxozM_DNVtqoZ_ZHIUX9eW5Sf5N4iCpL9l8-NCQst3Lw`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4NCjxzdmcgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWw6c3BhY2U9InByZXNlcnZlIiB3aWR0aD0iMTI5OXB4IiBoZWlnaHQ9IjEyOTlweCIgdmVyc2lvbj0iMS4xIiBzdHlsZT0ic2hhcGUtcmVuZGVyaW5nOmdlb21ldHJpY1ByZWNpc2lvbjsgdGV4dC1yZW5kZXJpbmc6Z2VvbWV0cmljUHJlY2lzaW9uOyBpbWFnZS1yZW5kZXJpbmc6b3B0aW1pemVRdWFsaXR5OyBmaWxsLXJ1bGU6ZXZlbm9kZDsgY2xpcC1ydWxlOmV2ZW5vZGQiDQp2aWV3Qm94PSIwIDAgMTI5OSAxMjk5Ig0KIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIg0KIGRhdGEtbmFtZT0iTGF5ZXIgMSI+DQogPGRlZnM+DQogIDxzdHlsZSB0eXBlPSJ0ZXh0L2NzcyI+DQogICA8IVtDREFUQVsNCiAgICAuc3RyMCB7c3Ryb2tlOiM0OTM1Mjc7c3Ryb2tlLXdpZHRoOjQ4LjQ0O3N0cm9rZS1saW5lam9pbjpyb3VuZDtzdHJva2UtbWl0ZXJsaW1pdDoyMi45MjU2fQ0KICAgIC5maWwxIHtmaWxsOm5vbmV9DQogICAgLmZpbDIge2ZpbGw6I0Q2QzE3NX0NCiAgICAuZmlsMCB7ZmlsbDojRUZFMkIyfQ0KICAgXV0+DQogIDwvc3R5bGU+DQogPC9kZWZzPg0KIDxnIGlkPSJQbGFuX3gwMDIwXzEiPg0KICA8bWV0YWRhdGEgaWQ9IkNvcmVsQ29ycElEXzBDb3JlbC1MYXllciIvPg0KICA8cGF0aCBjbGFzcz0iZmlsMCIgZD0iTTExOTEuOTggNjQ5LjVjMCwwLjE2IDAsMC40MyAwLDAuNTYgMCwyOTkuNTUgLTI0Mi45Myw1NDIuNDggLTU0Mi40OCw1NDIuNDggLTI2Ny45NiwwIC00OTUuODUsLTE5NS44NCAtNTM2LjI1LC00NjAuNjkgMCwtMC43MiAtMC4yNSwtMS40NSAtMC4yOSwtMi4xOCAtMy45NiwtMjYuNDYgLTUuOTUsLTUzLjMyIC01Ljk1LC04MC4xMSAwLC00NC4wOCA1LjM4LC04OC4xIDE1Ljk1LC0xMzAuODUgNC45NiwtMjAuNDIgMTEuMzcsLTQwLjYzIDE4Ljc2LC02MC4zMiA3OS41MywtMjExLjMgMjgxLjg1LC0zNTEuMzcgNTA3LjY5LC0zNTEuMzcgMCwwIDAuMDcsMCAwLjA3LDBsMS4wOSAwYzExLjEsMTYyLjQxIDE0Ni4xNCwyODguNDggMzA4LjkyLDI4OC40OCA5LjAxLDAgMTcuODcsLTAuMzggMjYuNjksLTEuMTYgMi4wOSwxNS43IDUuNTEsMzEuMjkgMTAuMDcsNDYuNDMgMjguNjIsOTUuNTUgMTAxLjQ2LDE3MS42MSAxOTUuNzIsMjA0LjI0IDAuMDEsMS40OSAwLjAxLDIuOTkgMC4wMSw0LjQ5eiIvPg0KICA8cGF0aCBjbGFzcz0iZmlsMSBzdHIwIiBkPSJNMTE5MS45OCA2NDkuNWMwLDI5OS41NSAtMjQyLjkzLDU0Mi40OCAtNTQyLjQ4LDU0Mi40OCAtMjk5LjU1LDAgLTU0Mi40OCwtMjQyLjkzIC01NDIuNDgsLTU0Mi40OCAwLC0yOTkuNTUgMjQyLjkzLC01NDIuNDggNTQyLjQ4LC01NDIuNDhsMS4wNyAwYzExLjEsMTYyLjQxIDE0Ni4xNCwyODguNDggMzA4LjkyLDI4OC40OCA5LjAxLDAgMTcuODcsLTAuMzggMjYuNjksLTEuMTYgMi4wOSwxNS43IDUuNTEsMzEuMjkgMTAuMDcsNDYuNDMgMjguNTMsOTUuNTkgMTAxLjQ2LDE3MS42NiAxOTUuNzMsMjA0LjI0IDAsMS40OSAwLDIuOTkgMCw0LjQ5eiIvPg0KICA8cGF0aCBjbGFzcz0iZmlsMiBzdHIwIiBkPSJNNDIwLjg4IDg2MS42Yy0yLjQ2LDAuMjIgLTQuOTYsMC4zMyAtNy40MywwLjMzIC00My4wMiwwIC03OS4xMiwtMzIuNDkgLTgzLjYzLC03NS4yNiAtMC4yOSwtMi40MiAtMC40NSwtNC44NSAtMC40NSwtNy4yOCAwLC00LjM4IDAuNDksLTguNzUgMS40NywtMTMuMDIgNC4yMiwtMTcuMjQgMTguMjIsLTMwLjcxIDMzLjkxLC0zOC43NSAxMy41MiwtNi45MSAyOC41MywtMTAuNTMgNDMuNzMsLTEwLjUzIDUzLjAzLDAgOTYuMDQsNDMuMDIgOTYuMDQsOTYuMDUgMCwyLjY1IC0wLjExLDUuMzMgLTAuMzIsNy45NmwwIDAuNTRjLTIuNDcsMjMuMzYgLTIyLjE4LDQxLjExIC00NS42Nyw0MS4xMSAtMC42LDAgLTEuMjEsLTAuMDEgLTEuODEsLTAuMDNsLTM1Ljg0IC0xLjEyeiIvPg0KICA8cGF0aCBjbGFzcz0iZmlsMiBzdHIwIiBkPSJNOTEwLjI4IDY5NC44OGMtMS43NiwtMC4xMSAtMy41NSwtMC4xOSAtNS4zMSwtMC4xOSAtOC4wNywwIC0xNi4xMSwxLjMyIC0yMy43NSwzLjg4IC0xNy4wNCw1LjcxIC0zMy44MiwxMi43IC00OS45MSwyMC42NyAtMTQuNTksNi42NCAtMjguMDQsMTUuNzEgLTM5LjY2LDI2Ljc1IC0yOS4wNiwyOS45NCAtMzIuODksNzcuNSAtMjEuMzYsMTE3LjY1IDAuOTUsNC4yOSAyLjg0LDguMzMgNS41MywxMS44MSAzLjQ5LDMuNDMgNy44Nyw1Ljg0IDEyLjY0LDYuOTMgNy4xOSwxLjk0IDE0LjYxLDIuOTIgMjIuMDUsMi45MiA4LjQzLDAgMTYuODMsLTEuMjcgMjQuODgsLTMuNzQgMjkuMDcsLTguNjMgNTcuNjgsLTE4LjMxIDg1LjgzLC0yOS4wNyAxMS42NSwtMy41OSAyMi40NywtOS41NiAzMS43MywtMTcuNDggOC4wOSwtOC43MiAxNC4wNCwtMTkuMjQgMTcuMzQsLTMwLjY2IDIuOTMsLTguNiA1LjE3LC0xNy40NyA2LjU1LC0yNi40NCAwLjUsLTMuNSAwLjc2LC03LjA2IDAuNzYsLTEwLjYgMCwtMzguMTQgLTI5LjQ4LC02OS43OSAtNjcuNTEsLTcyLjQ4bDAuMTkgMC4wNXoiLz4NCiAgPHBhdGggY2xhc3M9ImZpbDIgc3RyMCIgZD0iTTU5OC4xNiAzNTUuNjljLTQuMTksLTAuNDcgLTguNDIsLTAuNzEgLTEyLjY0LC0wLjcxIC0yMy40MywwIC00Ni4yOSw3LjM2IC02NS4zNCwyMS4wMWwtMC4zOCAwLjI5Yy0xOC40NiwxMy4yNyAtMzguMTcsMjkuNzQgLTM0LjY4LDU1LjA3IDEuOTUsMTIuMzEgOC42MSwyMy40MSAxOC41NCwzMC45NSAyMC43MywxNi41MSA0Ny4xOCwxOC40IDcyLjY2LDIwLjA1bDM2LjgxIDIuMzdjMTQuNTMsMC45NyAzMC44LDEuMzEgNDEuNTYsLTguNDMgNC45MiwtNC45NCA4LjY2LC0xMC45NyAxMC44OSwtMTcuNTggNS4wNCwtMTEuODUgNy42NCwtMjQuNTkgNy42NCwtMzcuNDYgMCwtMy44OSAtMC4yNSwtNy44IC0wLjcxLC0xMS42NSAtMi4xOCwtMTYuODIgLTExLjM0LC0zMS45NyAtMjUuMjQsLTQxLjcxIC0xMy44NSwtOS4wMSAtMzEuMDQsLTEwLjY1IC00Ny41MSwtMTIuMDZsLTEuNiAtMC4xNHoiLz4NCiA8L2c+DQo8L3N2Zz4NCg==`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-600-af30cbb84e9b2873b6c81cc3963c7b1804540954b2cf1e88e70d68c1c6c4b64e.svg](https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-600-af30cbb84e9b2873b6c81cc3963c7b1804540954b2cf1e88e70d68c1c6c4b64e.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `40-18t13-44l-22-393q-2-32-31-32zM115`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-807d23576d9cd898ddaf40f14bb42fcac7c2add44211f87357bd82dbebfb38d9.css](https://api.app.eva.beta.gouv.fr/assets/active_admin-807d23576d9cd898ddaf40f14bb42fcac7c2add44211f87357bd82dbebfb38d9.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAAGQAAAAeCAYAAADaW7vzAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6Q0NBRjI1NjM0M0UwMTFFNDk4NkFGMzJFQkQzQjEwRUIiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6Q0NBRjI1NjQ0M0UwMTFFNDk4NkFGMzJFQkQzQjEwRUIiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDpDQ0FGMjU2MTQzRTAxMUU0OTg2QUYzMkVCRDNCMTBFQiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDpDQ0FGMjU2MjQzRTAxMUU0OTg2QUYzMkVCRDNCMTBFQiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PoNEP54AAAIOSURBVHja7Jq9TsMwEMcxrZD4WpBYeKUCe+kTMCACHZh4BFfHO/AAIHZGFhYkBBsSEqxsLCAgXKhbXYOTxh9pfJVP+qutnZ5s/5Lz2Y5I03QhWji2GIcgAokWgfCxNvcOCCGKqiSqhUp0laHOne05vdEyGMfkdxJDVjgwDlEQgYQBgx+ULJaWSXXS6r/ER5FBVR8VfGftTKcITNs+a1XpcFoExREIDF14AVIFxgQUS+h520cdud6wNkC0UBw6BCO/HoCYwBhD8QCkQ/x1mwDyD4plh4D6DDV0TAGyo4HcawLIBBSLDkHeH0Mg2yVP3l4TQMZQDDsEOl/MgHQqhMNuE0D+oBh0CIr8MAKyazBH9WyBuKxDWgbXfjNf32TZ1KWm/Ap1oSk/R53UtQ5xTh3LUlMmT8gt6g51Q9p+SobxgJQ/qmsfZhWywGFSl0yBjCLJCMgXail3b7+rumdVJ2YRss4cN+r6qAHDkPWjPjdJCF4n9RmAD/V9A/Wp4NQassDjwlB6XBiCxcJQWmZZb8THFilfy/lfrTvLghq2TqTHrRMTKNJ0sIhdo15RT+RpyWwFdY96UZ/LdQKBGjcXpcc1AlSFEfLmouD+1knuxBDUVrvOBmoOC/rEcN7OQxKVeJTCiAdUzUJhA2Oez9QTkp72OTVcxDcXY8iKNkxGAJXmJCOQwOa6dhyXsOa6XwEGAKdeb5ET3rQdAAAAAElFTkSuQmCC`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-b16d9da044113656922083fea969e9b0b3d8b2d97e07b86c82e52784b7265e9a.svg](https://api.app.eva.beta.gouv.fr/assets/quicksand-v21-latin-ext-regular-b16d9da044113656922083fea969e9b0b3d8b2d97e07b86c82e52784b7265e9a.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `24-11t7-30l-11-442q-1-21-20-21zM90`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `org/TR/2011/REC-css3-selectors-20110929/`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x001fv��꼁\x0010�Pbm�q����7��]�lS</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bugs`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
Instances: 13
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 110 times, the first in the element starting with: "	select,", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='" + expando + "'></a>`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password/new](https://api.app.eva.beta.gouv.fr/pro/admin/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/dashboard](https://api.app.eva.beta.gouv.fr/pro/admin/dashboard)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/robots.txt](https://api.app.eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/sitemap.xml](https://api.app.eva.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin](https://api.app.eva.beta.gouv.fr/pro/admin)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/](https://api.app.eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro](https://api.app.eva.beta.gouv.fr/pro)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr](https://api.app.eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `86400000`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10000000`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20030331`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20201017`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js](https://api.app.eva.beta.gouv.fr/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `86400000`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/roue-dentee-78cf0c751d0efd586ebaaf1b1860607a851bf7c87c138a26109c02bf7faaa6b0.svg](https://api.app.eva.beta.gouv.fr/assets/roue-dentee-78cf0c751d0efd586ebaaf1b1860607a851bf7c87c138a26109c02bf7faaa6b0.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `00209415`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js](https://api.app.eva.beta.gouv.fr/assets/active_admin-c9e084abd21507c94e4edb3ece783bd4b777d10c1c174f1fe135e822584a8633.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20110929`
  
  
  
  
Instances: 8
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>86400000, which evaluates to: 1972-09-27 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `compte[email]`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  * Parameter: `compte[email]`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/login](https://api.app.eva.beta.gouv.fr/pro/admin/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Parameter: `code_postal`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher](https://api.app.eva.beta.gouv.fr/pro/structures?code_postal=ZAP&commit=chercher)
  
  
  * Method: `GET`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://api.app.eva.beta.gouv.fr/pro/admin/password](https://api.app.eva.beta.gouv.fr/pro/admin/password)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
Instances: 9
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://api.app.eva.beta.gouv.fr/pro/admin/login</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>commit=Se connecter</p><p></p><p>The user-controlled value was:</p><p>se connecter</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

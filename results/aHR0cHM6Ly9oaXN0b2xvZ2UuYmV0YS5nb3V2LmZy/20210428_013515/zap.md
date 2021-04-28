
# ZAP Scanning Report

Generated on Wed, 28 Apr 2021 01:28:53


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 11 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 3 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 5 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 2 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Cookie Without SameSite Attribute | Low | 2 | 
| Cookie Without Secure Flag | Low | 2 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 2 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 5 | 
| Information Disclosure - Suspicious Comments | Informational | 7 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 184 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/dev_qg](https://histologe.beta.gouv.fr/dev_qg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Chiffres](https://histologe.beta.gouv.fr/Chiffres)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/sitemap.xml](https://histologe.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new">Agence Nationale de la Cohésion des Territoires</a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new"><img src="images/logo_ANCT_header.svg"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Chiffres](https://histologe.beta.gouv.fr/Chiffres)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new"><img src="images/logo_ANCT_header.svg"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new"><img src="images/logo_ANCT_header.svg"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.interconnectes.com/" target="_new"><img src="images/Logo_label_2021.png"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.interconnectes.com/" target="_new"><img src="images/Logo_label_2021.png"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/CGU](https://histologe.beta.gouv.fr/CGU)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.cnil.fr/fr/modele/courrier/exercer-son-droit-dacces" target="_blank" rel="noopener">https://www.cnil.fr/fr/modele/courrier/exercer-son-droit-dacces</a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new"><img src="images/logo_ANCT_header.svg"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Plan-du-site](https://histologe.beta.gouv.fr/Plan-du-site)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new"><img src="images/logo_ANCT_header.svg"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://agence-cohesion-territoires.gouv.fr/" target="_new"><img src="images/logo_ANCT_header.svg"></a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.interconnectes.com/" target="_new"><img src="images/Logo_label_2021.png"></a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.js"></script>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/js/all.min.js](https://histologe.beta.gouv.fr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.js"></script>`
  
  
  
  
Instances: 3
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/CGU](https://histologe.beta.gouv.fr/CGU)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Chiffres](https://histologe.beta.gouv.fr/Chiffres)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Plan-du-site](https://histologe.beta.gouv.fr/Plan-du-site)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline mt-2 mt-md-0" action="ident_new.php" method="post">`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect.php](https://histologe.beta.gouv.fr/connect.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline mt-2 mt-md-0" action="ident.php" method="post">`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="Message" name="contact" id="contact">`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-register" action="signFinish2.php" enctype="multipart/form-data" method="post" name="signale" id="signale">`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/initUser.php](https://histologe.beta.gouv.fr/initUser.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline mt-2 mt-md-0" action="first_ident.php" method="post">`
  
  
  
  
Instances: 5
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "id_user" "pws" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/initUser.php](https://histologe.beta.gouv.fr/initUser.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect.php](https://histologe.beta.gouv.fr/connect.php)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 8 [main.php].</p><p>Predicted response size: 308.</p><p>Response Body Length: 6,665.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Parameter: `PHPSESSID`
  
  
  * Evidence: `Set-Cookie: PHPSESSID`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `PHPSESSID`
  
  
  * Evidence: `Set-Cookie: PHPSESSID`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `PHPSESSID`
  
  
  * Evidence: `Set-Cookie: PHPSESSID`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Parameter: `PHPSESSID`
  
  
  * Evidence: `Set-Cookie: PHPSESSID`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Parameter: `PHPSESSID`
  
  
  * Evidence: `Set-Cookie: PHPSESSID`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `PHPSESSID`
  
  
  * Evidence: `Set-Cookie: PHPSESSID`
  
  
  
  
Instances: 2
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.js`
  
  
  * Evidence: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.js"></script>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.js`
  
  
  * Evidence: `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.js"></script>`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Chiffres](https://histologe.beta.gouv.fr/Chiffres)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/dev_qg](https://histologe.beta.gouv.fr/dev_qg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/sitemap.xml](https://histologe.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/robots.txt](https://histologe.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/css/all.min.css](https://histologe.beta.gouv.fr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/CGU](https://histologe.beta.gouv.fr/CGU)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Plan-du-site](https://histologe.beta.gouv.fr/Plan-du-site)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/images/logo_ANCT_header.svg](https://histologe.beta.gouv.fr/images/logo_ANCT_header.svg)
  
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm](https://histologe.beta.gouv.fr/_adm)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/robots.txt](https://histologe.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/sitemap.xml](https://histologe.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/dev](https://histologe.beta.gouv.fr/dev)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/dev_qg](https://histologe.beta.gouv.fr/dev_qg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Plan-du-site](https://histologe.beta.gouv.fr/Plan-du-site)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Chiffres](https://histologe.beta.gouv.fr/Chiffres)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/robots.txt](https://histologe.beta.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/css/all.min.css](https://histologe.beta.gouv.fr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `d09GRgABAAAAABVEAAsAAAAALOAAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAADsAAABUIIslek9TLzIAAAFEAAAAQQAAAFZJwk67Y21hcAAAAYgAAAFuAAAFNuKa/PhnbHlmAAAC+AAADhoAAB2IDPM492hlYWQAABEUAAAAMAAAADYblhFQaGhlYQAAEUQAAAAeAAAAJAhwBAhobXR4AAARZAAAABEAAAEcSCAAAGxvY2EAABF4AAAAkAAAAJDonu+SbWF4cAAAEggAAAAfAAAAIAFWAFluYW1lAAASKAAAAR0AAAHyFNvC+HBvc3QAABNIAAAB/AAABJyXrlRreJxjYGRgYOBiMGCwY2BycfMJYeDLSSzJY5BiYGGAAJA8MpsxJzM9kYEDxgPKsYBpDiBmg4gCACY7BUgAeJxjYGSZzziBgZWBgYGf2QNIroDQTA4MVoymQJqBlZkBKwhIc01hcPjI+NGN+cB/AYYc5gMMH4DCjCA5AHlACw0AAAB4nO3T523jQAAF4ZFFy0nOOeecc842a3CRV9D9cg+swOboXRlH4NsBF0zALoFuoFk7qBXQ+KaBx996ttGZb9LfmS/407mmcL4qf37qseFYnxedsau+tqif2KKHXvrq+wZoM8gQw4wwyhjjTDDJFNPMMMsc8yywyBLLrLDKGutssMkW2+ywyx779fsPOeKYE04545wLLrnimhtuueOeBx554pkXXnnjnQ8+KeuPafH/aDs0v/6dla5XdFawK7DNcCdURbimVXe4S6pWYHsC2xvYvsD2h7unGghsO/y6ajCwQ4EdDuxIYEcDOxbY8cBOBHYysFOBnQ7sTGBnAzsX2PnALgR2MbBLgV0O7EpgVwO7Ftj1wG4EdjOwW4HdDuxOYHcDuxfY/cAehH98dRjYo8AeB/YksKeBPQvseWAvAnsZ2KvAXgf2JrC3gb0L7H1gHwL7GNinwD4H9iWwr4F9C+x7YD8C+xnYMih/AaHUtUQAAHicnVkLbFtnFf7Pf53rPO2a+Pq2S+z5sdhxk+Zhx/byclrFuU7XR2jY1tCmWTvdZh1jo6WP0a1QTbSj6pbQscqgske1sKfQtALqeFQwMgkM2nhIpRrVQBVI04TYQBDWYOI7zv/f61fqlJS6vvf3vfc/5zvnP+c7578hAiEfHzBtFHYQO3GTNYRASHbIjhVm0Sy6A/6Af0UsGosKeCmEgzbwirFQHLpwYAG7C+jYiQP7BhOJwX0HtL/nRjPdm7ec3zJy68Az337mr8Gh5uahUXYQxksfgxVslN11e3tHZ/unegYGZowH8UAqSnBFySDZSEiFN4/InUfZhAMOzQLmQJw6ZLwbaIOA34wXRHysydsGXXEIucBugUAo2uX3inZHEXIdCAd3dP34tk+PJ0PHn/hy51D8xddfXttbW+u95Rt375y4+7T7Zqu1Hwai49Ho+GfZIRrs7R3t7X18kRBu4Y967fUOR3/XrbQvMjy4XhhaO6ruGp941OFYterkzvFd6id/YkjBg8rEjPYSQgrrUYN2R3A9ImEpLPkkX8QXqS9nf4AtTLSL3fGy33Z2h/rVdFpNZ8rYeOL+HdsisVhk247LuQGcYQ+n1ezlcpaoJc/yAcIiDOx5+jPEScAWtnkkj81n80RQM7RqF1XtIpzJDVpVbtcLpklhkNiIRFYRUgUOXA6fhy1ODHB5HIIUjrAvPQbviha5bmG4bmWdGd41yw0rx1RVFVYv/Lym0WGxOBprhO4aiyV7n6rCRCbDoJiK5NvJStJYTgN4QEBf2vBbTol2u1CrPRRSy+la+B2dyf5ThdkMt/3jd4Q/0HlSSUgTyFUQQw/Qk1Cb1B7WHk5Crfp1Nj4CxxXtX3Qnw6f7K0WbWGRDjM2hY/ND2pvarAJtV5PaLMST+nMf/1l4n37AZAM6FcxVIMMJujN7lstHmXBG1eaScByOJwnlcg/T0+jhKrYSuAayWTYDnFKpmJyfR8n0dPYYPZK8Oq9AnD2uzzlHX0YsbPVkpsITQEgB+npG0d6AtYp2UT9nYE9GgbU4wt/aG0omb4tEX+C28NnUZZgAe64q0A9xZbEtKL0KAuCJCEFtToHjzE912WcxSApey2M7VrAHIwvNkUFwq9kMswfi5e35Dp0x7AkwTU38CP9m6BE39RsD2PMvbsmGjHHO2eM27OHz6JNMkTaL9swr2iwO8nYzbNweZgzGvODWRpPwqnacRf5ftC04xkQy1rwQJ2xlAH1spifzq0e7s8/SXdo/k8wdSj5GOjgOM394zHAnzBiAdHsx1jcJ0+ihBkLqPTa7iGHuj0A45HAiqq5oL6MNTySsCu87pYUjkpN+mJacCyudUhrTU4UzWlxyOiVh1CllMpITI97gnheQe6aJTHwkgBhQnpQTbitINXsYHeEIaUn22DzCaJpJY3oMBZj1akpwp9TMwhXBLazGm1e4QjdXllY5PWl7dZtNIk0xm41cmoO3lOyHmBi/hLeS2Q94YhTXqSBpX6IWlOXCWCAmY4SW4/syXNh7UZmGBqUsp5dhwvTF5BQ0DC/CF70RfPUxlrABc4ABXS7M+6eVqWnlq1PK41PK9HLBwqVpZRqn4EScbsTb1zHuazgn5VEwZvpoXvn3VeUjDL9X55V5HOHveYXbuR/tHM/xODBCzYWILxKOeFjOso8wmlGdUjaBK56BOW0vrjudV7OfYHFAP8QQeU7bC6fY1+DvYrlOVvk8Uqlw2eaxVYRtvnr8wgTM5eWn6ZgW52GFGtQiHdkEvZDS1eTy5ibUIZBaQmLIrlU59k4JxxaOYOR1KNqYtnUY2tVqFU5Au6JthZcV7be0TZ9/AOdvJ9XEgtHqi0A0dDNWGTMn6s9cpH3WoGXaal34O5PWx35bp/BS9i6V5Gs7m28iVlLP4j0AkrxIzDr4T1Kr2MsmN1vzws6yqyZFxcsWC8q0ZneqhBRsWk0+wbgAJFaDw0U5G25Cx6EePMxlkKLQY4f01Fe1hxR49D16Gukqo13kLjspOdFd7/E7aqGuHuLyg7wPYx2iC2TWXLlZnxWHWLSex3XMnw9ss4NnXmnnVdI3Hj+475uy/M19h7Srxujg8T07tg+sk+V1A9t3/KYw3BO/p6/vniPsEPd2e73dCXYQVvf1vH306Ns9fbnzwpU1rSNbdu/eMtK6pjD6ojEVD6oxFQ+8v7wD7XqY1BEXaULL+jBnRZNuUCCG9MsaSheNxgIWaMOTHBBdNFYRwFZTMAeiLiqLZsCTWfjSAe1v/3ll1Yo71z2VFP6YfD77SnjIKp9483c7Jlsnd97mqWn44DmLNbLeC48Ph+ul+599fdvmz3/0zimHY7PW3bE94RUq1ksPXPrK1qf6n0oueJPP0zvbHxzc8/ydNV2TjTWe23ZOtv71Od/6iNWyLzl857bUxMpVI2tWPPiLw1+8F35OvYntHXoc7Dc1IP/UIQNhVS4OAeBEHRPcmRwPw6yaSqeF8QxLHwyGY5JTq03jv+I4HSci5gmLqrA5EI6EY0j1Nl8TCvSgeLMun55EQSnM5lp6IZ19CWNoLGOtczA1sIdJXLiCVyQnarJbrU6JFPJoHGNKYvUrFI3YPPlSE0DQMSkFrShhjteVK446awY0hN2qVxmrRaIXeOOXs3sc7caMqgdPUcni2WBDSdSvy0GJExl6gXbkBLE8yGQvC+6c3fsRF/OhTG6+xot6ALeArR7rol1sgWKHnuLbgihSEG4KgmqJa7MJ3uUjD7WyLt/E7WdrVYVsJ2P0IZfYwnqaYAfMtii++hJnG74eS6e5mjNcSarY5zqQswwHqoLWNGqC1iLnu7jvi+sU75LL1ikB6TvAWvFy1eiHyLBlKw71s14/zXsJU0k9XEM6b6gisg0Pcvyya7a6FKQyRRD7L+xOCuvN1sGJ3U5L2X6ni8HjW2LJHNHpywky26mcD+ViyimFOtpGRn88OtLWoQ7uP7F/EHugt5ySVssjA2M4dBe7xx66KxRK7B8c3J8I6clmKsLgwUho/18oKngNlHyQR7MEElb6WNGFVg5pSUC8PKppOJUDZtSUjcj5ViM/S/BUsS1JIMUC20giuKy9sQ4egSPrSjs9bTOs2Kh9H4Y3Gr3lJqEFZdox5q+RWlEFNk8VLRYr3KMd0D4ruBcycBgOlIq+qD0Nava7aOJ3YZOxlu+YbsJeWyBm1s/UYy3NfXhxp2PZl/h5Xs3gZ1lzct/SOQfQjuvnT64FKv+S4U9LJtBJlkDsa+TPpv8vfwSjR1pu/gR567TsBPLrKA0e13PcuxST+EVcZfw1AIiyLKC3qyXRVFM9V1VV3ikviTW12o/EaiqKM6IkLt4L9NwQs8gOuxVE7FtYzMWiy+63mxHeXHV1hcigLttTiRmzVDEjirRKhCFuASniRtaHylhfGf9jxDVhv+szak0uOYAxjSe3q2M9L3L+WDah5koLy4lUiKU01oEHMEgzeoLryQ5zmP+nnFIqJWFDXZHX68N4ipBu0s8qT4FluF5njn9aQNLTs5/m7yD51OO+D9iXkVBriqlK6Tpz4wLNqAtX0nqLn72cSlXrF/leMa0/xu1Ic/4KsQexm0hlD6VSMKEurlUdS0WYFMYNMm0TsF2T4+DCts3nFRHrEsWrub+xpn34jg1dlXdXdPb4TS0uhFF2RRGEOlrbs/n2RFDwrQvand7KNX3NTmlDmfqm3NCOFF0Xwy00uhV7ijYQ2YtLFzPghiqeU3K1mPw9neKuyq4Ndwy31zT2BZcbmhn1vHuD5GzuW1PpddqD624RgkO3b+6uJYt6BB8JL2FZDJELZhk7YMlXHxDbaCSMnbJLiJW14d54TLrryRc3dnZ/6TN9qc7OHnaaMi6WBf1RzzPPT42It2xdVaN8bkB7c+wmfjau5vY+qmmrcB9fAwIsn3Fn4kB0QrirTcD+nK0AexeM0Ot9dpcQxb3exOGDBw9/f/VqqzV5NtX3wNeefrKbjk8cPnTwCz9oCVqtw/mLf97S0OC8+YWD+77w8G5wjTyxL067b81OjjY2ulwv4tUjk9qfPvnE3gHojhXtw9j+lbAqnc9lmScTe09yLPuSqu+zMP7TLC+2sajXS1qabcyQ+o1ayWRVEge5CXMUpWFD5rEJnuKOlGchUoI6lf1tiIvk9RGs0FrNCJq2T2UTgjttbPjcjCNY08HeS+02jeP6rkTZuOlnGcNWuKjNsIvCo5eUS/2nNj1072Rff3/f5L1zbBB+BK92hPO/2eChjU8Ya6HLbL+OVHMceaY0G7DfjaGy5KW+a5Sd7gjn+xnerCSOdj6CT7YvArDplNx5NJHvafjz4Y7Ce9fzcIZ5ldV3bP+zCTij5vYhwvvCNH/XTuQioLAIuZ2hTeezR9s7OpRoDgabE0Pfyg0ez2fp/TBbcocPcnnF9cmkFdm3RKOv4JXy2kv2zwUoKmpQnlNQA7ReC2q08MeKInxbFP22sqUcUrXwdwndRz/F/tSKkdhUXC2aGNVimbCAP9BUEWDL6g/E8BKChQuzLOJmoUq01FVW1llEbR7+kWwKhluGe9Y6G8+ynZzk/L2JirWVC+9V1orU9HvXcOOn2iPbGoZbjg4n+nsMf+m6K7DTYv25GbcFcmBZGOjJV773vVd+dX0gdOtj6ccCy0Gj++FV7gfvUn5YA/n3eDEZ/NfqppfOJc+dU157TTl3LlnWC+ncXfxP8j541fBB8/V9UKp/bgkHlIBY2gOlSHQcR4046FpuJDQtCoxyPplJDo9s3Zwcn+xo1zL/I0h+nVz72s7dr69Nbn738IP37VGviRlTHqceMz03FjWL8S7pwyVAL+3O6yP/L0ERSDgAAHicY2BkYGAA4qWOPU/j+W2+MnCzbACKMNx+kpaAoP+Hsqxj7gNyORiYQKIAZQkMY3icY2BkYGA+8F+AgYFlAwMQsKxjYGRABe4AVsMDggAAeJxjYGBgYNkwirFhAB+hMTkAAAAAAAAAAEwAyAEcATQBZAGaAbQByAHgAfoCGgIuAkgCYgKCApYCrgLGAtoDBgNAA1QDpAP+BBgERAR2BJYEtgTgBRAFfAXkBgoGOgZgBoYGugb4BywHfgfACAoINAhkCH4ImAjMCR4JWgm6CfYKTgqcCwoLXgukC8oL+gwkDHAMfgy2DRANTg2UDdAOFA5oDsR4nGNgZGBgcGfwZWBlAAEmIOYCQgaG/2A+AwAXvwGwAHicXY69TsMwFIVP+odoEAIhMZulC1L6M/YB2pkO2dPESVslceS4lSoxM/MUzDwFz8WJeyUqbOn6O+ceXxvAA34QoFsBhr52q4cbqgv3SXfCA/Kj8BAhnoVHVC/CY7xiIhziCW+cEAxu6YyRCfdwj1q4T/9deED+EB5y+qfwiP6X8BgxvoVDTILRPjV1u9HFsUysZ19ibdu9qdU8mnm91rW2idOZ2p5VeyoWzuUqt6ZSK1M7XZZGNdYcdOqinXPNcjrNxY9SU2GPFIZ/brGBRoEjSiSwV/4fxUxY73RaYY4Is6v+mv3aZxI4nhkzW5xZW5w4e0HXIafOmTGoSCt/t0uX3IZO43sHOin9CDt/q8ESU+78Xz7yr1e/MPVTYgAAAHicbVLpetMwEPS0HEmaNE0KtOUsV8tljnKfBQqU11BkufGHbBnZ7vH2WLu247To18xod1YayVvwePW9/699LGAR53AeF3ARHXTRwxL6GGAZQ6xghDFWcQmXcQVrWMcGruIaruMGbuIWNnEbd3AX93AfW9jGAzzEIzzGE/h4imd4jhfYwUu8wmu8wVu8w3t8wEd8wmd8wS6+4hu+Yw8/8BO/sI/fXl9IaYok98NI64boKFFDEQS+jKzUinjHcQd6QivLDRXkcmvNkR+Yo4T4qMWzdoVWIXestXhW2tmM9fU53SmlSzHRtWVrY4UVGx1M5zxZKGtE5blxSp+Zjs/urLalIiVtwFrFhg3jjoEsg0gCYSmVGaO45FTJP1WZgxNzzAlJbTLVjrjHioNLgdIqV+RXY7JwgWoj+Cm6Koj4JRg5bayOc2UToR3juR11wt19B0wYcmHZp/zGz7mckmgESTSCEB2CUBqEfN2G0ZNESWhsLPLIJLQ9J5CjNmUe5EiItFhEmjVCFEGsksLfqVSHHRqlopildlYht1SLE+4jRFdPbZSUwfBHrwnd5m+hsua4M0ZdVoVWZVPuqgnNyMRhlQshOnGmhJVcXGOakBWT3ArJD9QtT8vHYESpHRpdxBw9p9YW2hVxUf2KOcFVLFdC+Svdfou6Xc/7B2RZePg=`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/initUser.php](https://histologe.beta.gouv.fr/initUser.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect.php](https://histologe.beta.gouv.fr/connect.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x0000\x0010�\x0010Q� ��0ӏA\x0014�QU�a��qן�\x0018��Y�����ۯ�\x001c��]�㞻�߿</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/js/all.min.js](https://histologe.beta.gouv.fr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `SELECT`
  
  
  
  
Instances: 7
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: ""use strict";var n=t("base64-js"),a=t("ieee754");r.Buffer=e,r.SlowBuffer=function(t){+t!=t&&(t=0);return e.alloc(+t)},r.INSPECT_", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/CGU](https://histologe.beta.gouv.fr/CGU)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Chiffres](https://histologe.beta.gouv.fr/Chiffres)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Plan-du-site](https://histologe.beta.gouv.fr/Plan-du-site)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/connect_new.php](https://histologe.beta.gouv.fr/connect_new.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/signale](https://histologe.beta.gouv.fr/signale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h">
   
      
        <!-- entete -->
        <header class="rf-header">
            <div class="rf-container">
                <div class="rf-header__body">
                    <div class="rf-header__brand">
                        `
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-logo" href="#" title="République française">
                             <span class="rf-logo__title">République
                            <br>
                             française</span>
                        </a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/dev_qg](https://histologe.beta.gouv.fr/dev_qg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/](https://histologe.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Aide](https://histologe.beta.gouv.fr/Aide)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr](https://histologe.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/sitemap.xml](https://histologe.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/dev](https://histologe.beta.gouv.fr/dev)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm](https://histologe.beta.gouv.fr/_adm)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/robots.txt](https://histologe.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Contact](https://histologe.beta.gouv.fr/Contact)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Qui](https://histologe.beta.gouv.fr/Qui)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/Home](https://histologe.beta.gouv.fr/Home)
  
  
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
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `252645135`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16753920`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `14204888`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13528509`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10410725`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `35975351`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `77275007`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16729344`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16634018`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12357519`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `999999999`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10145074`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11881376`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `17210368`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16775885`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10025880`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10264286`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `12632256`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15794160`
  
  
  
  
* URL: [https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js](https://histologe.beta.gouv.fr/_adm/include/plotly-latest.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16119260`
  
  
  
  
Instances: 184
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>252645135, which evaluates to: 1978-01-03 03:12:15</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

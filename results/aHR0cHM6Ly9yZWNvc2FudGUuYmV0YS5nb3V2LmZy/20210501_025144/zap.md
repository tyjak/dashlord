
# ZAP Scanning Report

Generated on Sat, 1 May 2021 02:36:08


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Content-Type Header Missing | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 8 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/robots.txt](https://recosante.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
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

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/static/663c13484331a79ab24964c7b24a8500/Recosante_Kit.communication.professionnel.de.sante.zip](https://recosante.beta.gouv.fr/static/663c13484331a79ab24964c7b24a8500/Recosante_Kit.communication.professionnel.de.sante.zip)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#oZXFz`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#oZXFz</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://stats.data.gouv.fr"/>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://stats.data.gouv.fr"/>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://stats.data.gouv.fr"/>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://stats.data.gouv.fr"/>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://stats.data.gouv.fr"/>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sport/](https://recosante.beta.gouv.fr/sport/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="Form__Wrapper-sc-11txskx-0 dfPfqE">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sport/](https://recosante.beta.gouv.fr/sport/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/?name=ZAP&patients](https://recosante.beta.gouv.fr/inscription-patients/?name=ZAP&patients)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="Form__Wrapper-sc-11txskx-0 dfPfqE">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sport/](https://recosante.beta.gouv.fr/sport/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form method="post" class="SubscribeForm__Wrapper-sc-1h5x93k-0 janDFD">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "email" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sport/](https://recosante.beta.gouv.fr/sport/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v3/polyfill.min.js?features=IntersectionObserver"></script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/component---src-pages-stats-js-d43d75047ded99d6504a.js](https://recosante.beta.gouv.fr/component---src-pages-stats-js-d43d75047ded99d6504a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/framework-ddff9c6a94258f6c8286.js](https://recosante.beta.gouv.fr/framework-ddff9c6a94258f6c8286.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/app-71c054d69e9ef7a48de5.js](https://recosante.beta.gouv.fr/app-71c054d69e9ef7a48de5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/commons-a1ce566168a3f90c44fc.js](https://recosante.beta.gouv.fr/commons-a1ce566168a3f90c44fc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/robots.txt](https://recosante.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sitemap.xml](https://recosante.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sitemap.xml](https://recosante.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/robots.txt](https://recosante.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sitemap.xml](https://recosante.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sport/](https://recosante.beta.gouv.fr/sport/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Logos__StyledLogo-sc-1y4cuq8-4`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>.�(��ҷ)^t� ��\x001c�\�r��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/manifest.webmanifest](https://recosante.beta.gouv.fr/manifest.webmanifest)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/component---src-pages-inscription-patients-js-00018c5a1c226055717d.js](https://recosante.beta.gouv.fr/component---src-pages-inscription-patients-js-00018c5a1c226055717d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/acd228c973bcc8442de6f392692e9a2f8ed15512-dc8ab09578b434627e38.js](https://recosante.beta.gouv.fr/acd228c973bcc8442de6f392692e9a2f8ed15512-dc8ab09578b434627e38.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/component---src-pages-stats-js-d43d75047ded99d6504a.js](https://recosante.beta.gouv.fr/component---src-pages-stats-js-d43d75047ded99d6504a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/polyfill-39e793ba5020a71d3643.js](https://recosante.beta.gouv.fr/polyfill-39e793ba5020a71d3643.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/commons-a1ce566168a3f90c44fc.js](https://recosante.beta.gouv.fr/commons-a1ce566168a3f90c44fc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/215a364054556408f3c42100732b83abdd2f79b6-2c74c92085e262a07dbc.js](https://recosante.beta.gouv.fr/215a364054556408f3c42100732b83abdd2f79b6-2c74c92085e262a07dbc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/app-71c054d69e9ef7a48de5.js](https://recosante.beta.gouv.fr/app-71c054d69e9ef7a48de5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/framework-ddff9c6a94258f6c8286.js](https://recosante.beta.gouv.fr/framework-ddff9c6a94258f6c8286.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/component---src-pages-professionnelsante-js-47597ab19fd87671d221.js](https://recosante.beta.gouv.fr/component---src-pages-professionnelsante-js-47597ab19fd87671d221.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 9
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "(window.webpackJsonp=window.webpackJsonp||[]).push([[11],{DeS2:function(e,t,n){"use strict";n.d(t,"a",(function(){return i}));va", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/profil/](https://recosante.beta.gouv.fr/profil/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sport/](https://recosante.beta.gouv.fr/sport/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><picture><source srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" /><img loading="lazy" width="99" height="90" srcset="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg 1x,
/static/cc4670285ce6ba76eec48317038efb68/c8888/repufrancaise.jpg 1.5x,
/static/cc4670285ce6ba76eec48317038efb68/ce470/repufrancaise.jpg 2x" src="/static/cc4670285ce6ba76eec48317038efb68/a93c7/repufrancaise.jpg" alt="République Française" style="position:absolute;top:0;left:0;opacity:1;width:100%;height:100%;object-fit:cover;object-position:center"/></picture></noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription/](https://recosante.beta.gouv.fr/inscription/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/robots.txt](https://recosante.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/professionnelsante/](https://recosante.beta.gouv.fr/professionnelsante/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/inscription-patients/](https://recosante.beta.gouv.fr/inscription-patients/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/cookies/](https://recosante.beta.gouv.fr/cookies/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/sitemap.xml](https://recosante.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/pollen/](https://recosante.beta.gouv.fr/pollen/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/asthme/](https://recosante.beta.gouv.fr/asthme/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/mentions-legales/](https://recosante.beta.gouv.fr/mentions-legales/)
  
  
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
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `591716069`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `794921875`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `591716069`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `794921875`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `807395231`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr/](https://recosante.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `821369966`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `821369966`
  
  
  
  
* URL: [https://recosante.beta.gouv.fr](https://recosante.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `807395231`
  
  
  
  
Instances: 8
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>591716069, which evaluates to: 1988-10-01 13:34:29</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Fri, 11 Jun 2021 04:31:11


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 9 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 10 | 
| Sub Resource Integrity Attribute Missing | Medium | 7 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cookie Without SameSite Attribute | Low | 11 | 
| Cookie Without Secure Flag | Low | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Dangerous JS Functions | Low | 2 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 10 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 10 | 
| Timestamp Disclosure - Unix | Informational | 2 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 12 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/tabular/preview/](https://www.data.gouv.fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://www.data.gouv.fr](https://www.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/datasets.csv](https://www.data.gouv.fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/resources.csv](https://www.data.gouv.fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets.csv](https://www.data.gouv.fr/es/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/resources.csv](https://www.data.gouv.fr/en/resources.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr](https://www.data.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://www.data.gouv.fr/](https://www.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="shortcut icon" href="https://static.data.gouv.fr/_themes/gouvfr/img/favicon.png?_=2.6.2">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://static.data.gouv.fr/_themes/gouvfr/theme.3c12239b98e35508354ef88c35d946c9.css" rel="stylesheet">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="author" href="http://www.etalab.gouv.fr/" />`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/home.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://static.data.gouv.fr/static/common.8d0d560b186410ec6260fa773b80edc7.css">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://static.data.gouv.fr/static/home.d21e92be044c9a31cab1b6aad75a4d34.css">`
  
  
  
  
Instances: 7
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/en/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/resources](https://www.data.gouv.fr/resources)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/es/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/en/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/fr/search/">`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="site-search" action="/es/search/">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "search" ].</p>
  
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
  
  
  
* URL: [https://www.data.gouv.fr/es/organizations.csv](https://www.data.gouv.fr/es/organizations.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/reuses.csv](https://www.data.gouv.fr/fr/reuses.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/resources.csv](https://www.data.gouv.fr/es/resources.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/resources.csv](https://www.data.gouv.fr/fr/resources.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/reuses.csv](https://www.data.gouv.fr/en/reuses.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/reuses.csv](https://www.data.gouv.fr/es/reuses.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/organizations.csv](https://www.data.gouv.fr/en/organizations.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/resources.csv](https://www.data.gouv.fr/en/resources.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets.csv](https://www.data.gouv.fr/es/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/organizations.csv](https://www.data.gouv.fr/fr/organizations.csv)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 131 [https://static.data.gouv.fr/resources/catalogue-des-donnees-de-data-gouv-fr/20210610-074952/export-organization-20210610-074952.csv].</p><p>Predicted response size: 431.</p><p>Response Body Length: 469.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.data.gouv.fr/reuses.csv](https://www.data.gouv.fr/reuses.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/datasets.csv](https://www.data.gouv.fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/resources.csv](https://www.data.gouv.fr/fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/resources.csv](https://www.data.gouv.fr/es/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets.csv](https://www.data.gouv.fr/es/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/resources.csv](https://www.data.gouv.fr/en/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/reuses.csv](https://www.data.gouv.fr/en/reuses.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/resources.csv](https://www.data.gouv.fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.data.gouv.fr/es/resources.csv](https://www.data.gouv.fr/es/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets.csv](https://www.data.gouv.fr/es/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/resources.csv](https://www.data.gouv.fr/en/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/resources.csv](https://www.data.gouv.fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/datasets.csv](https://www.data.gouv.fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/reuses.csv](https://www.data.gouv.fr/reuses.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/resources.csv](https://www.data.gouv.fr/fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/reuses.csv](https://www.data.gouv.fr/en/reuses.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/home.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/home.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/tabular/preview/](https://www.data.gouv.fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/tabular/static/csvapi-front/js/chunk-vendors.60de0680.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://static.data.gouv.fr/tabular/static/csvapi-front/js/chunk-vendors.60de0680.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/tabular/preview/](https://www.data.gouv.fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/tabular/static/csvapi-front/js/app.19e51586.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://static.data.gouv.fr/tabular/static/csvapi-front/js/app.19e51586.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/site.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/site.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/site.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/site.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/site.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/site.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js`
  
  
  * Evidence: `<script src="https://static.data.gouv.fr/static/common.5fdb9e5a5c5c0baff356.js"></script>`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/donnees-relatives-aux-resultats-des-tests-virologiques-covid-19/](https://www.data.gouv.fr/fr/datasets/donnees-relatives-aux-resultats-des-tests-virologiques-covid-19/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/donnees-hospitalieres-relatives-a-lepidemie-de-covid-19/](https://www.data.gouv.fr/fr/datasets/donnees-hospitalieres-relatives-a-lepidemie-de-covid-19/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/tabular/preview/](https://www.data.gouv.fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
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
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tags.csv](https://www.data.gouv.fr/en/tags.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tags.csv](https://www.data.gouv.fr/es/tags.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `Pragma`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tags.csv](https://www.data.gouv.fr/es/tags.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/robots.txt](https://www.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Pragma`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/robots.txt](https://www.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tags.csv](https://www.data.gouv.fr/fr/tags.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `Pragma`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Pragma`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tags.csv](https://www.data.gouv.fr/en/tags.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `Pragma`
  
  
  * Evidence: `public`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tags.csv](https://www.data.gouv.fr/fr/tags.csv)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://www.data.gouv.fr/fr/resources.csv](https://www.data.gouv.fr/fr/resources.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/users/](https://www.data.gouv.fr/fr/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/resources.csv](https://www.data.gouv.fr/en/resources.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/users/](https://www.data.gouv.fr/es/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/users/](https://www.data.gouv.fr/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/users/](https://www.data.gouv.fr/en/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets.csv](https://www.data.gouv.fr/es/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/robots.txt](https://www.data.gouv.fr/robots.txt)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.data.gouv.fr/resources.csv](https://www.data.gouv.fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/resources.csv](https://www.data.gouv.fr/en/resources.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiZTE5YmQyMzhjMDk3NDA2ZWQ1NTc3ZDRhYmYzZGI3ZDgxOGMzYmU0ZiJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/reuses.csv](https://www.data.gouv.fr/reuses.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/reuses.csv](https://www.data.gouv.fr/en/reuses.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/datasets.csv](https://www.data.gouv.fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/resources.csv](https://www.data.gouv.fr/es/resources.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets.csv](https://www.data.gouv.fr/es/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/resources.csv](https://www.data.gouv.fr/fr/resources.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJfZnJlc2giOmZhbHNlLCJjc3JmX3Rva2VuIjoiMzEwODUyYzEwOTYwYmQ2NDcwNDVjYTkzMmYwYjkzY2Q1NzAwZDJmMSJ9`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>{"_fresh":false,"csrf_token":"310852c10960bd647045ca932f0b93cd5700d2f1"}</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.data.gouv.fr/resources](https://www.data.gouv.fr/resources)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/frequentation-des-musees-de-france/](https://www.data.gouv.fr/fr/datasets/frequentation-des-musees-de-france/)
  
  
  * Method: `GET`
  
  
  * Evidence: `xxx`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `From`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "<script type="text/javascript"></p><p>  var _paq = _paq || [];</p><p>  _paq.push(['setDocumentTitle', '404/URL = ' +  encodeURIComponent(doc", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.data.gouv.fr/en/tabular/preview/](https://www.data.gouv.fr/en/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Haut de page</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/en/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Back to top</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/tabular/preview/](https://www.data.gouv.fr/fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Haut de page</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Haut de page</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/es/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Volver arriba</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/fr/datasets/r/dc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Haut de page</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/es/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Volver arriba</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/tabular/preview/](https://www.data.gouv.fr/es/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Haut de page</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/tabular/preview/](https://www.data.gouv.fr/tabular/preview/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://static.data.gouv.fr/tabular/static/csvapi-front/js/chunk-vendors.60de0680.js"></script>`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/en/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Back to top</a>`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/fr/datasets/r/09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Haut de page</a>`
  
  
  
  
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
  
  
  
* URL: [https://www.data.gouv.fr](https://www.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/robots.txt](https://www.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/](https://www.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/datasets.csv](https://www.data.gouv.fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr](https://www.data.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/users/](https://www.data.gouv.fr/fr/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/](https://www.data.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/users/](https://www.data.gouv.fr/en/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/users/](https://www.data.gouv.fr/users/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/users/](https://www.data.gouv.fr/es/users/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://www.data.gouv.fr/en/datasets.csv](https://www.data.gouv.fr/en/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210610`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/datasets.csv](https://www.data.gouv.fr/fr/datasets.csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210610`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>20210610, which evaluates to: 1970-08-22 22:03:30</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fresources](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fresources)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2Ftabular%2Fpreview%2F](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2Ftabular%2Fpreview%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fes%2Fdatasets%2Fr%2F09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/es/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fes%2Fdatasets%2Fr%2F09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2Fdatasets%2Fr%2Fdc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2Fdatasets%2Fr%2Fdc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fen%2Fdatasets%2Fr%2F09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/en/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fen%2Fdatasets%2Fr%2F09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fes%2Ftabular%2Fpreview%2F](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fes%2Ftabular%2Fpreview%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/en/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fen%2Fdatasets%2Fr%2Fdc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/en/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fen%2Fdatasets%2Fr%2Fdc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2F](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fen%2Ftabular%2Fpreview%2F](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fen%2Ftabular%2Fpreview%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2Fdatasets%2Fr%2F09f013c5-9531-444b-ab6c-7a0e88efd77d](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2Fdatasets%2Fr%2F09f013c5-9531-444b-ab6c-7a0e88efd77d)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/es/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fes%2Fdatasets%2Fr%2Fdc13282f-3c7a-4fac-b1f3-3939e39d45f6](https://www.data.gouv.fr/es/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fes%2Fdatasets%2Fr%2Fdc13282f-3c7a-4fac-b1f3-3939e39d45f6)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
* URL: [https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2F](https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Ffr%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `next`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.data.gouv.fr/fr/login?next=https%3A%2F%2Fwww.data.gouv.fr%2Fresources</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>next=https://www.data.gouv.fr/resources</p><p></p><p>The user-controlled value was:</p><p>https://www.data.gouv.fr/resources</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

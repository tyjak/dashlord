
# ZAP Scanning Report

Generated on Sat, 29 May 2021 02:15:24


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 7 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 2 | 
| Vulnerable JS Library | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 7 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 2 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Sensitive Information in URL | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 7 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 11 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 11 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="nav-link" href="https://communaute.inclusion.beta.gouv.fr" rel="noopener" target="_blank" aria-label="Accéder au Forum de l'inclusion (nouvel onglet)">Communauté 

<svg
    class="icon"
    width="18"
    height="18"
    fill="none"
    stroke="currentColor"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    style="vertical-align: text-top;"
>
    
    <use xlink:href="/static/icons/feather-sprite.cbef33d25b84.svg#external-link"></use>
</svg>
</a>`
  
  
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/advanced/](https://emplois.inclusion.beta.gouv.fr/stats/advanced/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.inclusion.beta.gouv.fr/app/iframeResizer.js"></script>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://stats.inclusion.beta.gouv.fr/app/iframeResizer.js"></script>`
  
  
  
  
Instances: 2
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 3.4.1 is vulnerable.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v3.4.1`
  
  
  
  
Instances: 1
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p></p>
  
### Reference
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/search/employers/results">`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers/results?city&city_name=ZAP&distance=5](https://emplois.inclusion.beta.gouv.fr/search/prescribers/results?city&city_name=ZAP&distance=5)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="" class="d-block mb-5">`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/search/prescribers/results" class="d-block mb-5">`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/signup/siae/select?siren=ZAP](https://emplois.inclusion.beta.gouv.fr/signup/siae/select?siren=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="" role="form">`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/search/employers/results">`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI](https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="" class="d-block mb-5">`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/signup/siae/select](https://emplois.inclusion.beta.gouv.fr/signup/siae/select)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="" role="form">`
  
  
  
  
Instances: 7
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "id_city" "id_city_name" ].</p>
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.inclusion.beta.gouv.fr/app/iframeResizer.js`
  
  
  * Evidence: `<script src="https://stats.inclusion.beta.gouv.fr/app/iframeResizer.js"></script>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/advanced/](https://emplois.inclusion.beta.gouv.fr/stats/advanced/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.inclusion.beta.gouv.fr/app/iframeResizer.js`
  
  
  * Evidence: `<script src="https://stats.inclusion.beta.gouv.fr/app/iframeResizer.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/tarteaucitron/tarteaucitron.6a98ba4f7937.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/tarteaucitron/tarteaucitron.6a98ba4f7937.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/bootstrap.min.e1d98d47689e.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/bootstrap.min.e1d98d47689e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.525832369e2a.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.525832369e2a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `evAl`
  
  
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.03b4df74a362.css](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.03b4df74a362.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/css/itou.ff73752164b1.css](https://emplois.inclusion.beta.gouv.fr/static/css/itou.ff73752164b1.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/favicon.b48853d646f6.ico](https://emplois.inclusion.beta.gouv.fr/static/favicon.b48853d646f6.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/bootstrap.min.a15c2ac3234a.css](https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/bootstrap.min.a15c2ac3234a.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/tarteaucitron/tarteaucitron.6a98ba4f7937.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/tarteaucitron/tarteaucitron.6a98ba4f7937.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/favicon.b48853d646f6.ico](https://emplois.inclusion.beta.gouv.fr/static/favicon.b48853d646f6.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.525832369e2a.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.525832369e2a.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/js/configure_jobs.3b689087a4c6.js](https://emplois.inclusion.beta.gouv.fr/static/js/configure_jobs.3b689087a4c6.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/popper.min.56456db9d72a.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/popper.min.56456db9d72a.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/js/city_autocomplete_field.6b6cace3f660.js](https://emplois.inclusion.beta.gouv.fr/static/js/city_autocomplete_field.6b6cace3f660.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/bootstrap.min.e1d98d47689e.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/bootstrap-4.3.1/bootstrap.min.e1d98d47689e.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/css/itou.ff73752164b1.css](https://emplois.inclusion.beta.gouv.fr/static/css/itou.ff73752164b1.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/js/logout.7b285c03f082.js](https://emplois.inclusion.beta.gouv.fr/static/js/logout.7b285c03f082.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.03b4df74a362.css](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-ui-1.12.1/jquery-ui.min.03b4df74a362.css)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `aH3V3wVYzHwH3UDpbHmiOgLrDjQ3pIssfVH2tU2xz5IehGvvZAYMZHPmkD6OLj7h`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `LXiu5KmtcGg44SCMkXWo2DsUZUUu4xYnNEKfrJ7IfZUxYNsYR7UdqY8xqUK1khfV`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `bpsd9WjksRgaT9IUra4Kzrm7uhcpT7m7HZfuj4AM8iMN6pcKT9x5SikEk8XvykCL`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>-x�䩭ph8� ��u��;\x0014eE.�\x0016'4B����}�1`�\x0018G�\x001d��1�B��\x0017�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/password/reset/done/?email=foo-bar%40example.com](https://emplois.inclusion.beta.gouv.fr/accounts/password/reset/done/?email=foo-bar%40example.com)
  
  
  * Method: `GET`
  
  
  * Parameter: `email`
  
  
  * Evidence: `foo-bar@example.com`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL contains email address(es).</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script></p><p></p><p>        // Tarteaucitron's language is set according to the browser configuration</p><p>        // but a lot of users don't ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/](https://emplois.inclusion.beta.gouv.fr/accounts/login/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="#" data-toggle="modal" data-target="#no-email-modal">
    
        Je n'ai pas d'adresse e-mail
    
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js](https://emplois.inclusion.beta.gouv.fr/static/vendor/jquery-3.4.1/jquery.min.220afd743d9e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+k+"'></a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" data-toggle="modal" data-target="#no-email-modal">
    
        Je n'ai pas d'adresse e-mail
    
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/js/matomo.68934dd60c07.js](https://emplois.inclusion.beta.gouv.fr/static/js/matomo.68934dd60c07.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="matomo-event" data-matomo-category="MyCategory"
       data-matomo-action="MyAction" data-matomo-option="MyOption" >`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/signup/job_seeker](https://emplois.inclusion.beta.gouv.fr/signup/job_seeker)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="#" data-toggle="modal" data-target="#no-email-modal">
    
        Je n'ai pas d'adresse e-mail
    
</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/js/configure_jobs.3b689087a4c6.js](https://emplois.inclusion.beta.gouv.fr/static/js/configure_jobs.3b689087a4c6.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" role="button" class="js-job-delete">Supprimer</a>`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/signup/job_seeker](https://emplois.inclusion.beta.gouv.fr/signup/job_seeker)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" data-toggle="modal" data-target="#no-email-modal">
    
        Je n'ai pas d'adresse e-mail
    
</a>`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/static/favicon.b48853d646f6.ico](https://emplois.inclusion.beta.gouv.fr/static/favicon.b48853d646f6.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
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
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/sitemap.xml](https://emplois.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/robots.txt](https://emplois.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/signup/](https://emplois.inclusion.beta.gouv.fr/accounts/signup/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/versions/](https://emplois.inclusion.beta.gouv.fr/versions/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers](https://emplois.inclusion.beta.gouv.fr/search/prescribers)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/stats/](https://emplois.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr](https://emplois.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/](https://emplois.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>31449600, which evaluates to: 1970-12-31 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI](https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI)
  
  
  * Method: `GET`
  
  
  * Parameter: `kind`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/](https://emplois.inclusion.beta.gouv.fr/accounts/login/)
  
  
  * Method: `POST`
  
  
  * Parameter: `account_type`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=job_seeker)
  
  
  * Method: `GET`
  
  
  * Parameter: `account_type`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI](https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI)
  
  
  * Method: `GET`
  
  
  * Parameter: `kind`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=siae)
  
  
  * Method: `GET`
  
  
  * Parameter: `account_type`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI](https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI)
  
  
  * Method: `GET`
  
  
  * Parameter: `city_name`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/](https://emplois.inclusion.beta.gouv.fr/accounts/login/)
  
  
  * Method: `POST`
  
  
  * Parameter: `account_type`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber](https://emplois.inclusion.beta.gouv.fr/accounts/login/?account_type=prescriber)
  
  
  * Method: `GET`
  
  
  * Parameter: `account_type`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/](https://emplois.inclusion.beta.gouv.fr/accounts/login/)
  
  
  * Method: `POST`
  
  
  * Parameter: `account_type`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/accounts/login/](https://emplois.inclusion.beta.gouv.fr/accounts/login/)
  
  
  * Method: `POST`
  
  
  * Parameter: `login`
  
  
  
  
* URL: [https://emplois.inclusion.beta.gouv.fr/search/prescribers/results?city&city_name=ZAP&distance=5](https://emplois.inclusion.beta.gouv.fr/search/prescribers/results?city&city_name=ZAP&distance=5)
  
  
  * Method: `GET`
  
  
  * Parameter: `city_name`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://emplois.inclusion.beta.gouv.fr/search/employers/results?city&city_name=ZAP&distance=5&kind=EI</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [option] tag [value] attribute </p><p></p><p>The user input found was:</p><p>kind=EI</p><p></p><p>The user-controlled value was:</p><p>ei</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

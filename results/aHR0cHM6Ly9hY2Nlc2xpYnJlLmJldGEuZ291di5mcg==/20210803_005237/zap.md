
# ZAP Scanning Report

Generated on Tue, 3 Aug 2021 00:42:02


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 0 |
| Low | 5 |
| Informational | 2 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Timestamp Disclosure - Unix | Informational | 5 | 

## Alert Detail


  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?what=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?what=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next=/](https://acceslibre.beta.gouv.fr/compte/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/robots.txt](https://acceslibre.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/register/](https://acceslibre.beta.gouv.fr/compte/register/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="a4a-search-form" id="search-form" action="/recherche/">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "code" "lat" "lon" "what-input" "where-input" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next=/](https://acceslibre.beta.gouv.fr/compte/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/register/](https://acceslibre.beta.gouv.fr/compte/register/)
  
  
  * Method: `POST`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/](https://acceslibre.beta.gouv.fr/compte/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next=/compte/register/](https://acceslibre.beta.gouv.fr/compte/login/?next=/compte/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next=/compte/login/](https://acceslibre.beta.gouv.fr/compte/login/?next=/compte/login/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next=/recherche/](https://acceslibre.beta.gouv.fr/compte/login/?next=/recherche/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/password_reset/](https://acceslibre.beta.gouv.fr/compte/password_reset/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contact/](https://acceslibre.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next](https://acceslibre.beta.gouv.fr/compte/login/?next)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/register/?next=/](https://acceslibre.beta.gouv.fr/compte/register/?next=/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/register/](https://acceslibre.beta.gouv.fr/compte/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `csrftoken`
  
  
  * Evidence: `Set-Cookie: csrftoken`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//unpkg.com/swagger-ui-dist@3/swagger-ui-bundle.js`
  
  
  * Evidence: `<script src="//unpkg.com/swagger-ui-dist@3/swagger-ui-bundle.js"></script>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/register/](https://acceslibre.beta.gouv.fr/compte/register/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/sitemap.xml](https://acceslibre.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contact/](https://acceslibre.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/partenaires](https://acceslibre.beta.gouv.fr/partenaires)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/recherche/?what=centres+de+vaccination](https://acceslibre.beta.gouv.fr/recherche/?what=centres+de+vaccination)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation](https://acceslibre.beta.gouv.fr/conditions-generales-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/](https://acceslibre.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/accessibilite](https://acceslibre.beta.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/communes/](https://acceslibre.beta.gouv.fr/communes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr](https://acceslibre.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/visibilite.ed3fed9e2baa.png](https://acceslibre.beta.gouv.fr/static/img/landing/visibilite.ed3fed9e2baa.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/fiabilite-des-donnees.da83f39dbb8e.png](https://acceslibre.beta.gouv.fr/static/img/landing/fiabilite-des-donnees.da83f39dbb8e.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/favicon.f67248f8d5b7.ico](https://acceslibre.beta.gouv.fr/static/img/favicon.f67248f8d5b7.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.decff39675c5.css](https://acceslibre.beta.gouv.fr/static/dist/main.decff39675c5.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/mctrct.5d6c432de8f2.png](https://acceslibre.beta.gouv.fr/static/img/landing/mctrct.5d6c432de8f2.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/participez-enrichissement-donnees.9a4c019e1212.png](https://acceslibre.beta.gouv.fr/static/img/landing/participez-enrichissement-donnees.9a4c019e1212.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/rassurez-vous.800bd7d0c390.png](https://acceslibre.beta.gouv.fr/static/img/landing/rassurez-vous.800bd7d0c390.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/manifest.4c2dfab4446e.webmanifest](https://acceslibre.beta.gouv.fr/static/manifest.4c2dfab4446e.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/apple-touch-icon.1dbbb71330f3.png](https://acceslibre.beta.gouv.fr/static/img/apple-touch-icon.1dbbb71330f3.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/landing/stopwatch.e7e63e9218f6.png](https://acceslibre.beta.gouv.fr/static/img/landing/stopwatch.e7e63e9218f6.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/img/logo-acceslibre.5aa4e1e45947.svg](https://acceslibre.beta.gouv.fr/static/img/logo-acceslibre.5aa4e1e45947.svg)
  
  
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

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/2b-oletta/a/centre-de-vaccination/erp/centre-vaccination-oletta/](https://acceslibre.beta.gouv.fr/app/2b-oletta/a/centre-de-vaccination/erp/centre-vaccination-oletta/)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/64-arudy/a/centre-de-vaccination/erp/centre-de-vaccination-darudy/](https://acceslibre.beta.gouv.fr/app/64-arudy/a/centre-de-vaccination/erp/centre-de-vaccination-darudy/)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/app/07-lamastre/a/centre-de-vaccination/erp/centre-de-vaccination-de-lamastre-centre-socio-culturel/](https://acceslibre.beta.gouv.fr/app/07-lamastre/a/centre-de-vaccination/erp/centre-de-vaccination-de-lamastre-centre-socio-culturel/)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js](https://acceslibre.beta.gouv.fr/static/dist/main.ec44d16a19f8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bTODO\b and was detected in the element starting with: "<script></p><p>    // TODO: move to component?</p><p>    $(document).ready(function() {</p><p>      $(".btn-vote-no").on("click", function() {</p><p>   ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/contact/](https://acceslibre.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/login/?next=/](https://acceslibre.beta.gouv.fr/compte/login/?next=/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/api/docs/](https://acceslibre.beta.gouv.fr/api/docs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/static/dist/main.decff39675c5.css](https://acceslibre.beta.gouv.fr/static/dist/main.decff39675c5.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `70710678`
  
  
  
  
* URL: [https://acceslibre.beta.gouv.fr/compte/register/](https://acceslibre.beta.gouv.fr/compte/register/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31449600`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>31449600, which evaluates to: 1970-12-31 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

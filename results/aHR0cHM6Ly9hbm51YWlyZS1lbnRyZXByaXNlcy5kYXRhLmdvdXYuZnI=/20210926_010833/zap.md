
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 01:02:13


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 6 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 11 | 
| Incomplete or No Cache-control Header Set | Low | 10 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Content-Type Header Missing | Informational | 8 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Loosely Scoped Cookie | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 7 | 
| Storable and Cacheable Content | Informational | 2 | 
| Storable but Non-Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 5 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="canonical" href="https://annuaire-entreprises.data.gouv.fr/administration}"/>`
  
  
  
  
Instances: 1
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher/carte" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "search-input-input" ].</p>
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  * Parameter: `datadome`
  
  
  * Evidence: `Set-Cookie: datadome`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/resources/favicons/manifest.webmanifest](https://annuaire-entreprises.data.gouv.fr/resources/favicons/manifest.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
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

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `0S6JqLOGeBEK3YeTHj9iKXDkS31aUaizaG3Thsfc-IiUYtvR`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `zj1DM98wwyc-JjHC3Et32wnDdbYRSl3ueZ1n2RcoFoTAeFspRndzZ7_9wAt50J_TxxOS5rsQ1WX-EGa90jPREPrv-iox`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `4552-zX/G2D9C9FDwbuQYfOcWdG3pAvA`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fQ_wV-A-nIc_03tbuHwkK14_BpJxa83L`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f08-ja55Uo/01c0moGiJBJNoKhpEDMI`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `TeUn9z_UFwHcFkHOIUbUbVSiY60-IBv8_ZxbjUM9j227dNwlo42lcB6`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4552-zX/G2D9C9FDwbuQYfOcWdG3pAvA`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `DdMOU5Is3p3NYYlQBe13E_jrW_fUFCmi2oYpDDYD`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  * Evidence: `0U4fd1JBHK9KwcYNRhTIxCKz1U6pHxqGaKSHSQu`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `WbOBZRY73YLYoNuLRerh9zzG5YlG75Pv6D0i1BNix2F0oT`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  * Evidence: `xgTUfwQrR3IPzRmOJ36SK-lAuAG4QJlXBhmfekrWEklqYtQK`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1Xc6uTRSPmJdF5BGLzsmehDqft3tJYdbHiraMY0lrZRd3T54VXYxR_oAjLjn-1TLzGwFe22uKcpXoWfq56qHGTx24b9xqDxiwPRBsGqgI0`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�.����x\x0011</p><p>݇�\x001e?b)p�K}ZQ��hmӆ�����b��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/carte/](https://annuaire-entreprises.data.gouv.fr/carte/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/dirigeants/](https://annuaire-entreprises.data.gouv.fr/dirigeants/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement](https://annuaire-entreprises.data.gouv.fr/etablissement)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: "<script></p><p>    (function addCopyFunction() {</p><p>      const copyList = document.getElementsByClassName('copy-to-clipboard-anchor');</p><p> ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Loosely Scoped Cookie
##### Informational (Low)
  
  
  
  
#### Description
<p>Cookies can be scoped by domain or path. This check is only concerned with domain scope.The domain scope applied to a cookie determines which domains can access it. For example, a cookie can be scoped strictly to a subdomain e.g. www.nottrusted.com, or loosely scoped to a parent domain e.g. nottrusted.com. In the latter case, any subdomain of nottrusted.com can access the cookie. Loosely scoped cookies are common in mega-applications like google.com and live.com. Cookies set from a subdomain like app.foo.bar are transmitted only to that domain by the browser. However, cookies scoped to a parent-level domain may be transmitted to the parent, or any subdomain of the parent.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Always scope cookies to a FQDN (Fully Qualified Domain Name).</p>
  
### Other information
<p>The origin domain used for comparison was: </p><p>annuaire-entreprises.data.gouv.fr</p><p>datadome="MyEIFrayHu6Y2L8wjZt7bOOvNsXs~gXTpsTebbWCXxsXzH1rHRa0w4~6ckS~WbOBZRY73YLYoNuLRerh9zzG5YlG75Pv6D0i1BNix2F0oT";$Path="/";$Domain=".data.gouv.fr"</p><p></p>
  
### Reference
* https://tools.ietf.org/html/rfc6265#section-4.1
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html
* http://code.google.com/p/browsersec/wiki/Part2#Same-origin_policy_for_cookies

  
#### CWE Id : 565
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `501215367`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `400731430`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `628372620`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `695292204`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>501215367, which evaluates to: 1985-11-19 02:29:27</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

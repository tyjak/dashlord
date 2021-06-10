
# ZAP Scanning Report

Generated on Thu, 10 Jun 2021 05:17:22


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 9 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 8 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 1 | 
| Cookie Without SameSite Attribute | Low | 1 | 
| Cookie Without Secure Flag | Low | 1 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Dangerous JS Functions | Low | 8 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 5 | 
| Retrieved from Cache | Informational | 8 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 6 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.notion.so/JeVeuxAider-gouv-fr-pour-les-coles-et-les-universit-s-a9a595aa05a044b3a1944533a48e71d8" class="custom-link btn border-width-0 btn-color-893878 btn-outline btn-icon-left" target="_blank">Consulter le centre d'aide</a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-12 py-2 transition ease-in-out duration-150" data-v-656f1182>
            Centre d'aide
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://gqlg3qh7po-dsn.algolia.net" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://gqlg3qh7po-dsn.algolia.net" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.crisp.chat" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://static.axept.io" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.axept.io" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.crisp.chat" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.axept.io" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://static.axept.io" crossorigin="anonymous">`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/volontaire](https://www.jeveuxaider.gouv.fr/register/volontaire)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.jeveuxaider.gouv.fr/engagement/" method="get">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form mt-4 el-form--label-top">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="#" method="GET" class="w-full flex md:ml-0 mb-0" data-v-60d7911c>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.jeveuxaider.gouv.fr/engagement/" method="get">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="gdpr-privacy-preferences-frm" action="https://www.jeveuxaider.gouv.fr/engagement/wp/wp-admin/admin-post.php">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form aria-labelledby="newsletter-headline" class="sm:flex mt-9" data-v-019604d4>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form mt-4 el-form--label-top">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="gdpr-privacy-preferences-frm" action="https://www.jeveuxaider.gouv.fr/engagement/wp/wp-admin/admin-post.php">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form aria-labelledby="newsletter-headline" class="sm:flex mt-9" data-v-019604d4>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form form-register-steps el-form--label-top" data-v-bf75fa14>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/volontaire](https://www.jeveuxaider.gouv.fr/register/volontaire)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form form-register-steps el-form--label-top" data-v-5945ef07>`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "s" ].</p>
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `uncode_privacy[consent_types]`
  
  
  * Evidence: `Set-Cookie: uncode_privacy[consent_types]`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `uncode_privacy[consent_types]`
  
  
  * Evidence: `Set-Cookie: uncode_privacy[consent_types]`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `uncode_privacy[consent_types]`
  
  
  * Evidence: `Set-Cookie: uncode_privacy[consent_types]`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/610648/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/610648/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-3.4.1.js`
  
  
  * Evidence: `<script src="https://code.jquery.com/jquery-3.4.1.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"65d01f238ec80f12","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.5.2","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"65d01f170e6c0f12","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.5.2","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-3.4.1.js`
  
  
  * Evidence: `<script src="https://code.jquery.com/jquery-3.4.1.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-3.4.1.js`
  
  
  * Evidence: `<script src="https://code.jquery.com/jquery-3.4.1.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"65d01f08cb5c0f12","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.5.2","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/610648/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/610648/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"65d01f4e9de2d2a6","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.5.2","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/610648/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/610648/smarttag.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat/7050/benevolat-secours-catholique-lain-bourg-en-bresse](https://www.jeveuxaider.gouv.fr/missions-benevolat/7050/benevolat-secours-catholique-lain-bourg-en-bresse)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat/8485/benevolat-restos-du-coeur-23-saint-sulpice-le-gueretois](https://www.jeveuxaider.gouv.fr/missions-benevolat/8485/benevolat-restos-du-coeur-23-saint-sulpice-le-gueretois)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat/10713/benevolat-emmaus-defi-paris](https://www.jeveuxaider.gouv.fr/missions-benevolat/10713/benevolat-emmaus-defi-paris)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat/9457/benevolat-beyti-grenoble](https://www.jeveuxaider.gouv.fr/missions-benevolat/9457/benevolat-beyti-grenoble)
  
  
  * Method: `GET`
  
  
  * Evidence: `EVal`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/1d080cd.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/1d080cd.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat/6610/benevolat-kafe-citoyen-plougonvelin](https://www.jeveuxaider.gouv.fr/missions-benevolat/6610/benevolat-kafe-citoyen-plougonvelin)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/robots.txt](https://www.jeveuxaider.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/robots.txt](https://www.jeveuxaider.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/uploads/2021/04/logo-benevolat_0003_Calque-2`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `fbf2-TU2bgQnp8HFdBf4ZfCAbIWr6LxA`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `d63d-XHx55g9bx0wkWs0HAyXqvcjxvCA`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `c9a5-5U/Knd/SrKki7kiKxlv76NvLd+A`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `d10a-uEtBKjgArUfaDmrV74E2p6V/C0s`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `e3eb-I6thOYoGHbg3h8Pi6RnkJp2sTX4`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>r����hi�?�M��N?��(���z�%j���M�	�j��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bDB\b and was detected in the element starting with: "<script>window.__NUXT__=(function(a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u,v,w,x,y,z,A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="S&#039;informer" href="#" data-toggle="dropdown" class="dropdown-toggle" data-type="title">S&#8217;informer<i class="fa fa-angle-down fa-dropdown"></i></a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a tabindex="-1" href="#" class="inactive-link pushed" data-lb-index="0"><div class="t-entry-visual-overlay"><div class="t-entry-visual-overlay-in style-dark-bg" style="opacity: 0.5;"></div></div>
									<div class="t-overlay-wrap">
										<div class="t-overlay-inner">
											<div class="t-overlay-content">
												<div class="t-overlay-text single-block-padding"></div></div></div></div><img src="https://reserve-civique-wp.s3.amazonaws.com/uploads/2021/01/logo_api_engagement_0007_Calque-2.jpg" width="258" height="116" alt="" /></a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="underline hover:no-underline mt-4 text-lg cursor-pointer" data-v-fd29cafa>Page précédente</a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a tabindex="-1" href="#" class="inactive-link pushed" data-lb-index="0"><div class="t-entry-visual-overlay"><div class="t-entry-visual-overlay-in style-dark-bg" style="opacity: 0.5;"></div></div>
									<div class="t-overlay-wrap">
										<div class="t-overlay-inner">
											<div class="t-overlay-content">
												<div class="t-overlay-text single-block-padding"></div></div></div></div><img src="https://reserve-civique-wp.s3.amazonaws.com/uploads/2021/04/logo-benevolat_0003_Calque-2.png" width="1000" height="563" alt="" /></a>`
  
  
  
  
Instances: 5
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/1d080cd.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/1d080cd.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 108`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/d61dbdf.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/d61dbdf.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 109`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/84fa558.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/84fa558.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 108`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/25a371f.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/25a371f.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 108`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/df10e71.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/df10e71.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 109`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 107`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/90c9750.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/90c9750.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 107`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/6672bf1.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/6672bf1.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 108`
  
  
  
  
Instances: 8
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/robots.txt](https://www.jeveuxaider.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `96804923`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/1d080cd.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/1d080cd.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/b933aef.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `35327633`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/6672bf1.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/6672bf1.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `06270029`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>96804923, which evaluates to: 1973-01-25 10:15:23</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=Je%20maintiens%20le%20lien%20avec%20des%20personnes%20fragiles%20isol%C3%A9es](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=Je%20maintiens%20le%20lien%20avec%20des%20personnes%20fragiles%20isol%C3%A9es)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[template_title][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[type][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Pr%C3%A9vention%20et%20protection](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Pr%C3%A9vention%20et%20protection)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[domaines][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27apporte%20une%20aide%20alimentaire%20d%27urgence](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27apporte%20une%20aide%20alimentaire%20d%27urgence)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[template_title][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Pr%C3%A9vention%20et%20protection](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Pr%C3%A9vention%20et%20protection)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[domaines][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20en%20pr%C3%A9sentiel](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20en%20pr%C3%A9sentiel)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[type][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27assure%20une%20mission%20de%20mentorat%20pour%20un%20enfant%20ou%20un%20jeune](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27assure%20une%20mission%20de%20mentorat%20pour%20un%20enfant%20ou%20un%20jeune)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[template_title][0]`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=Je%20maintiens%20le%20lien%20avec%20des%20personnes%20fragiles%20isol%C3%A9es</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>refinementList[template_title][0]=Je maintiens le lien avec des personnes fragiles isolées</p><p></p><p>The user-controlled value was:</p><p>je maintiens le lien avec des personnes fragiles isolées</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

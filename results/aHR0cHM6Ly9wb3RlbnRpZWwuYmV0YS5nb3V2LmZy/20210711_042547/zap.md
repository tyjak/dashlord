
# ZAP Scanning Report

Generated on Sun, 11 Jul 2021 04:11:36


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 2 |
| Informational | 2 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 5 | 
| Absence of Anti-CSRF Tokens | Low | 4 | 
| Incomplete or No Cache-control Header Set | Low | 8 | 
| Information Disclosure - Suspicious Comments | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 1 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/](https://potentiel.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/index.html](https://potentiel.beta.gouv.fr/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr](https://potentiel.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/](https://potentiel.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr](https://potentiel.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/index.html](https://potentiel.beta.gouv.fr/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/robots.txt](https://potentiel.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr](https://potentiel.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/index.html](https://potentiel.beta.gouv.fr/index.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/sitemap.xml](https://potentiel.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/](https://potentiel.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' metabase.potentiel.beta.gouv.fr;connect-src 'self' 'unsafe-inline';img-src 'self' data:;style-src 'self' data: 'unsafe-inline';script-src 'unsafe-inline' 'self' metabase.potentiel.beta.gouv.fr;object-src 'none'`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/login.html](https://potentiel.beta.gouv.fr/login.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/login" method="post" name="form">`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html?success=Si%20l'adresse%20saisie%20correspond%20bien%20%C3%A0%20un%20compte%20Potentiel%2C%20vous%20recevrez%20un%20courrier%20%C3%A9lectronique%20avec%20des%20instructions%20pour%20choisir%20un%20nouveau%20mot%20de%20passe.](https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html?success=Si%20l'adresse%20saisie%20correspond%20bien%20%C3%A0%20un%20compte%20Potentiel%2C%20vous%20recevrez%20un%20courrier%20%C3%A9lectronique%20avec%20des%20instructions%20pour%20choisir%20un%20nouveau%20mot%20de%20passe.)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/retrieve-password" method="post" name="form">`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/login.html?error=Identifiant%20ou%20mot%20de%20passe%20erron%C3%A9.](https://potentiel.beta.gouv.fr/login.html?error=Identifiant%20ou%20mot%20de%20passe%20erron%C3%A9.)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/login" method="post" name="form">`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html](https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/retrieve-password" method="post" name="form">`
  
  
  
  
Instances: 4
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "email" "password" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/](https://potentiel.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/login.html?error=Identifiant%20ou%20mot%20de%20passe%20erron%C3%A9.](https://potentiel.beta.gouv.fr/login.html?error=Identifiant%20ou%20mot%20de%20passe%20erron%C3%A9.)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr](https://potentiel.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html?success=Si%20l'adresse%20saisie%20correspond%20bien%20%C3%A0%20un%20compte%20Potentiel%2C%20vous%20recevrez%20un%20courrier%20%C3%A9lectronique%20avec%20des%20instructions%20pour%20choisir%20un%20nouveau%20mot%20de%20passe.](https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html?success=Si%20l'adresse%20saisie%20correspond%20bien%20%C3%A0%20un%20compte%20Potentiel%2C%20vous%20recevrez%20un%20courrier%20%C3%A9lectronique%20avec%20des%20instructions%20pour%20choisir%20un%20nouveau%20mot%20de%20passe.)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/images/favicons/manifest.json](https://potentiel.beta.gouv.fr/images/favicons/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/index.html](https://potentiel.beta.gouv.fr/index.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/login.html](https://potentiel.beta.gouv.fr/login.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html](https://potentiel.beta.gouv.fr/mot-de-passe-oublie.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 8
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/scripts.js](https://potentiel.beta.gouv.fr/scripts.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "          // Ignore, user is still typing", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://potentiel.beta.gouv.fr/images/favicons/safari-pinned-tab.svg](https://potentiel.beta.gouv.fr/images/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `20010904`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>20010904, which evaluates to: 1970-08-20 14:35:04</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

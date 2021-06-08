
# ZAP Scanning Report

Generated on Tue, 8 Jun 2021 02:22:06


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 8 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 5 | 
| Cookie Without SameSite Attribute | Low | 5 | 
| Dangerous JS Functions | Low | 11 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Charset Mismatch  | Informational | 12 | 
| Content-Type Header Missing | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
| Modern Web Application | Informational | 10 | 
| Storable and Cacheable Content | Informational | 8 | 
| Storable but Non-Cacheable Content | Informational | 3 | 
| Timestamp Disclosure - Unix | Informational | 12 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 15 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-admin/admin-ajax.php](https://eva.beta.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a href="https://app.eva.beta.gouv.fr/" target="_blank" style="color: white" rel="noopener"><button style="background-color:#0053B3; border-radius: 5px; margin-right: 5px"><strong>Accès participant</strong></button></a>`
  
  
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='google-fonts-1-css'  href='https://fonts.googleapis.com/css?family=Quicksand%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto+Slab%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CWork+Sans%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic&#038;display=auto&#038;ver=5.7.2' media='all' />`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="https://gmpg.org/xfn/11">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='google-fonts-1-css'  href='https://fonts.googleapis.com/css?family=Quicksand%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto+Slab%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CWork+Sans%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic&#038;display=auto&#038;ver=5.7.2' media='all' />`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="https://gmpg.org/xfn/11">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='google-fonts-1-css'  href='https://fonts.googleapis.com/css?family=Quicksand%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto+Slab%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CWork+Sans%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic&#038;display=auto&#038;ver=5.7.2' media='all' />`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='google-fonts-1-css'  href='https://fonts.googleapis.com/css?family=Quicksand%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto+Slab%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CWork+Sans%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic&#038;display=auto&#038;ver=5.7.2' media='all' />`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="https://gmpg.org/xfn/11">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="https://gmpg.org/xfn/11">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel='stylesheet' id='google-fonts-1-css'  href='https://fonts.googleapis.com/css?family=Quicksand%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto+Slab%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CWork+Sans%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic%7CRoboto%3A100%2C100italic%2C200%2C200italic%2C300%2C300italic%2C400%2C400italic%2C500%2C500italic%2C600%2C600italic%2C700%2C700italic%2C800%2C800italic%2C900%2C900italic&#038;display=auto&#038;ver=5.7.2' media='all' />`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="profile" href="https://gmpg.org/xfn/11">`
  
  
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `POST`
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-submitted mc4wp-form-error mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-submitted mc4wp-form-error mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-submitted mc4wp-form-error mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form name="loginform" id="loginform" action="https://eva.beta.gouv.fr/wp-login.php" method="post">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form id="mc4wp-form-1" class="mc4wp-form mc4wp-form-705 mc4wp-form-submitted mc4wp-form-error mc4wp-form-basic" method="post" data-id="705" data-name="" >`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "EMAIL" "_mc4wp_honeypot" "_mc4wp_timestamp" "_mc4wp_form_id" "_mc4wp_form_element_id" ].</p>
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?action=lostpassword](https://eva.beta.gouv.fr/wp-login.php?action=lostpassword)
  
  
  * Method: `POST`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?action=lostpassword](https://eva.beta.gouv.fr/wp-login.php?action=lostpassword)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php](https://eva.beta.gouv.fr/wp-login.php)
  
  
  * Method: `POST`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php](https://eva.beta.gouv.fr/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php](https://eva.beta.gouv.fr/wp-login.php)
  
  
  * Method: `POST`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?action=lostpassword](https://eva.beta.gouv.fr/wp-login.php?action=lostpassword)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?action=lostpassword](https://eva.beta.gouv.fr/wp-login.php?action=lostpassword)
  
  
  * Method: `POST`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php](https://eva.beta.gouv.fr/wp-login.php)
  
  
  * Method: `GET`
  
  
  * Parameter: `wordpress_test_cookie`
  
  
  * Evidence: `Set-Cookie: wordpress_test_cookie`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/themes/astra/assets/js/minified/flexibility.min.js?ver=3.5.0](https://eva.beta.gouv.fr/wp-content/themes/astra/assets/js/minified/flexibility.min.js?ver=3.5.0)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/lib/swiper/swiper.min.js?ver=5.3.6](https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/lib/swiper/swiper.min.js?ver=5.3.6)
  
  
  * Method: `GET`
  
  
  * Evidence: `evAl`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery.min.js?ver=3.5.1](https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery.min.js?ver=3.5.1)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/plugins/elementor-pro/assets/js/preloaded-elements-handlers.min.js?ver=3.3.0](https://eva.beta.gouv.fr/wp-content/plugins/elementor-pro/assets/js/preloaded-elements-handlers.min.js?ver=3.3.0)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2](https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/themes/astra/assets/js/minified/flexibility.min.js?ver=3.5.0](https://eva.beta.gouv.fr/wp-content/themes/astra/assets/js/minified/flexibility.min.js?ver=3.5.0)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/themes/astra/assets/js/minified/frontend.min.js?ver=3.5.0](https://eva.beta.gouv.fr/wp-content/themes/astra/assets/js/minified/frontend.min.js?ver=3.5.0)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-admin/admin-ajax.php](https://eva.beta.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery.min.js?ver=3.5.1](https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery.min.js?ver=3.5.1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/themes/astra/assets/css/minified/main.min.css?ver=3.5.0](https://eva.beta.gouv.fr/wp-content/themes/astra/assets/css/minified/main.min.css?ver=3.5.0)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/feed/](https://eva.beta.gouv.fr/feed/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/comments/feed/](https://eva.beta.gouv.fr/comments/feed/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap_index.xml](https://eva.beta.gouv.fr/sitemap_index.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/comments/feed/](https://eva.beta.gouv.fr/comments/feed/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-admin/admin-ajax.php](https://eva.beta.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/feed/](https://eva.beta.gouv.fr/feed/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap_index.xml](https://eva.beta.gouv.fr/sitemap_index.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/comments/feed/](https://eva.beta.gouv.fr/comments/feed/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap_index.xml](https://eva.beta.gouv.fr/sitemap_index.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/themes/astra/assets/css/minified/main.min.css?ver=3.5.0](https://eva.beta.gouv.fr/wp-content/themes/astra/assets/css/minified/main.min.css?ver=3.5.0)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/feed/](https://eva.beta.gouv.fr/feed/)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/Sans-titre-e1622495184485`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fnos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fnos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/Sans-titre-e1622495184485`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `POST`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/Sans-titre-e1622495184485`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/feed/](https://eva.beta.gouv.fr/feed/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/document/d/e/2PACX-1vQ0mYR22VK-y_vX0buYtxTQBb6VuLZbMKfDuU0O7p1pi_y5nsbP1HOhiW5MPysbAhszxNIQ4lIin8s6/pub`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/wp-content/uploads/2021/05/1200px-Republique-francaise-logo`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>~���(�ק����������_���v�Jq�\x0017���b��~��q��{�h�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Charset Mismatch 
##### Informational (Low)
  
  
  
  
#### Description
<p>This check identifies responses where the HTTP Content-Type header declares a charset different from the charset defined by the body of the HTML or XML. When there's a charset mismatch between the HTTP header and content body Web browsers can be forced into an undesirable content-sniffing mode to determine the content's correct character set.</p><p></p><p>An attacker could manipulate content on the page to be interpreted in an encoding of their choice. For example, if an attacker can control content at the beginning of the page, they could inject script using UTF-7 encoded text and manipulate some browsers into interpreting that text.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fen-savoir-plus-sur-les-referentiels-devaluation%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fen-savoir-plus-sur-les-referentiels-devaluation%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fattention_concentration%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fattention_concentration%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fvigilance_controle%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fvigilance_controle%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Ftemoignage-de-fabienne%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Ftemoignage-de-fabienne%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Felementor-page-datterrissage-395%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Felementor-page-datterrissage-395%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fstatistiques%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fstatistiques%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fnos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fnos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fcgu%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fcgu%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fcomparaison_tri%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fcomparaison_tri%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fqui-sommes-nous%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Fqui-sommes-nous%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Forganisation_methode%2F](https://eva.beta.gouv.fr/wp-json/oembed/1.0/embed?format=xml&url=https%3A%2F%2Feva.beta.gouv.fr%2Forganisation_methode%2F)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Force UTF-8 for all text content in both the HTTP header and meta tags in HTML or encoding declarations in XML.</p>
  
### Other information
<p>There was a charset mismatch between the HTTP Header and the XML encoding declaration: [UTF-8] and [null] do not match.</p>
  
### Reference
* http://code.google.com/p/browsersec/wiki/Part2#Character_set_handling_and_detection

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/uploads/fbrfg/site.webmanifest](https://eva.beta.gouv.fr/wp-content/uploads/fbrfg/site.webmanifest)
  
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 9
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected 2 times, the first in the element starting with: "<script id='popup-maker-site-js-extra'></p><p>var pum_vars = {"version":"1.16.1","pm_dir_url":"https:\/\/eva.beta.gouv.fr\/wp-content\", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/wp/v2/categories/1](https://eva.beta.gouv.fr/wp-json/wp/v2/categories/1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type=\"application\/ld+json\" class=\"yoast-schema-graph\">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-includes/js/dist/vendor/wp-polyfill-url.min.js?ver=3.6.4](https://eva.beta.gouv.fr/wp-includes/js/dist/vendor/wp-polyfill-url.min.js?ver=3.6.4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/js/frontend-modules.min.js?ver=3.2.4](https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/js/frontend-modules.min.js?ver=3.2.4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-json/wp/v2/pages/1235](https://eva.beta.gouv.fr/wp-json/wp/v2/pages/1235)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type=\"application\/ld+json\" class=\"yoast-schema-graph\">`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/elementor-page-datterrissage-395/](https://eva.beta.gouv.fr/elementor-page-datterrissage-395/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script data-cfasync='false'>
    window.$crisp=[];
    CRISP_RUNTIME_CONFIG = {
      locale : 'fr'
    };
    CRISP_WEBSITE_ID = '779ed78e-5574-4966-9ac9-dbb340a6ccdc';(function(){
      d=document;s=d.createElement('script');
      s.src='https://client.crisp.chat/l.js';
      s.async=1;d.getElementsByTagName('head')[0].appendChild(s);
    })();</script>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/js/frontend.min.js?ver=3.2.4](https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/js/frontend.min.js?ver=3.2.4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/plugins/elementor-pro/assets/js/frontend.min.js?ver=3.3.0](https://eva.beta.gouv.fr/wp-content/plugins/elementor-pro/assets/js/frontend.min.js?ver=3.3.0)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-includes/js/dist/vendor/wp-polyfill.min.js?ver=7.4.4](https://eva.beta.gouv.fr/wp-includes/js/dist/vendor/wp-polyfill.min.js?ver=7.4.4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/js/preloaded-modules.min.js?ver=3.2.4](https://eva.beta.gouv.fr/wp-content/plugins/elementor/assets/js/preloaded-modules.min.js?ver=3.2.4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery.min.js?ver=3.5.1](https://eva.beta.gouv.fr/wp-includes/js/jquery/jquery.min.js?ver=3.5.1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
Instances: 10
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/temoignage-de-fabienne/](https://eva.beta.gouv.fr/temoignage-de-fabienne/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/](https://eva.beta.gouv.fr/nos-experts-scientifiques-vous-invitent-dans-les-coulisses-deva/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/](https://eva.beta.gouv.fr/en-savoir-plus-sur-les-referentiels-devaluation/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap_index.xml](https://eva.beta.gouv.fr/sitemap_index.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/robots.txt](https://eva.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-admin/](https://eva.beta.gouv.fr/wp-admin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/sitemap.xml](https://eva.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-admin/admin-ajax.php](https://eva.beta.gouv.fr/wp-admin/admin-ajax.php)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623073074`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623074281`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621415716`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1999999999`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1999999999`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621415716`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623118871`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623074281`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623073074`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1623118874`
  
  
  
  
* URL: [https://eva.beta.gouv.fr](https://eva.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621415708`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621415708`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1623073074, which evaluates to: 2021-06-07 13:37:54</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_element_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_element_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_element_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/](https://eva.beta.gouv.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_element_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/qui-sommes-nous/](https://eva.beta.gouv.fr/qui-sommes-nous/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_mc4wp_form_id`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
* URL: [https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F](https://eva.beta.gouv.fr/wp-login.php?reauth=1&redirect_to=https%3A%2F%2Feva.beta.gouv.fr%2Fwp-admin%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect_to`
  
  
  
  
Instances: 15
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://eva.beta.gouv.fr/qui-sommes-nous/</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>_mc4wp_form_id=705</p><p></p><p>The user-controlled value was:</p><p>705</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

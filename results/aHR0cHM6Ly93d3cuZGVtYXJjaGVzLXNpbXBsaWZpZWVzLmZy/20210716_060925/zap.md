
# ZAP Scanning Report

Generated on Fri, 16 Jul 2021 06:02:13


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 5 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Reverse Tabnabbing | Medium | 11 | 
| Application Error Disclosure | Low | 1 | 
| Dangerous JS Functions | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Sensitive Information in URL | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 1 | 
| Non-Storable Content | Informational | 6 | 
| Storable and Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 80 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 6 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/commencer](https://www.demarches-simplifiees.fr/commencer)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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

  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>img-src, frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `img-src 'self' *.openstreetmap.org static.demarches-simplifiees.fr *.cloud.ovh.net stats.data.gouv.fr * data: blob:; script-src 'self' stats.data.gouv.fr *.sendinblue.com *.crisp.chat crisp.chat *.sibautomation.com sibautomation.com cdn.jsdelivr.net maxcdn.bootstrapcdn.com code.jquery.com 'unsafe-eval' 'unsafe-inline' blob:; style-src 'self' *.crisp.chat crisp.chat cdn.jsdelivr.net maxcdn.bootstrapcdn.com 'unsafe-inline'; connect-src 'self' wss://*.crisp.chat *.crisp.chat *.demarches-simplifiees.fr in-automate.sendinblue.com app.franceconnect.gouv.fr sentry.io geo.api.gouv.fr api-adresse.data.gouv.fr openmaptiles.geo.data.gouv.fr openmaptiles.github.io tiles.geo.api.gouv.fr wxs.ign.fr data.education.gouv.fr; default-src 'self' data: blob: 'report-sample' fonts.gstatic.com in-automate.sendinblue.com player.vimeo.com app.franceconnect.gouv.fr sentry.io static.demarches-simplifiees.fr *.crisp.chat crisp.chat *.crisp.help *.sibautomation.com sibautomation.com data`
  
  
  
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Notre newsletter" class="footer-link" target="_blank" rel="noopener" href="https://my.sendinblue.com/users/subscribe/js_id/3s2q1/id/1">Newsletter</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/suivi](https://www.demarches-simplifiees.fr/suivi)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://matomo.org/" target="_blank" rel="noopener">Matomo</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class='btn button primary' href='https://browser-update.org/fr/update.html' rel='noopener' target='_blank'>
Mettre à jour mon navigateur
</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/administration](https://www.demarches-simplifiees.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" class="cta-panel-button-blue" href="https://app.livestorm.co/demarches-simplifiees/presentation-general-de-demarches-simplifieesfr">Inscription à notre webinaire</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/password/new](https://www.demarches-simplifiees.fr/users/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Notre newsletter" class="footer-link" target="_blank" rel="noopener" href="https://my.sendinblue.com/users/subscribe/js_id/3s2q1/id/1">Newsletter</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" class="link" href="https://franceconnect.gouv.fr/">Qu’est-ce que FranceConnect ?</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/commencer/demande-d-inscription-a-demarches-simplifiees](https://www.demarches-simplifiees.fr/commencer/demande-d-inscription-a-demarches-simplifiees)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://faq.demarches-simplifiees.fr"><span class='icon help'></span>
<div class='dropdown-description'>
<span class='help-dropdown-title'>Un problème avec le site ?</span>
<p>Trouvez votre réponse dans l’aide en ligne.</p>
</div>
</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a target="_blank" rel="noopener" class="link" href="https://franceconnect.gouv.fr/">Qu’est-ce que FranceConnect ?</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/stats](https://www.demarches-simplifiees.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Notre newsletter" class="footer-link" target="_blank" rel="noopener" href="https://my.sendinblue.com/users/subscribe/js_id/3s2q1/id/1">Newsletter</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Notre newsletter" class="footer-link" target="_blank" rel="noopener" href="https://my.sendinblue.com/users/subscribe/js_id/3s2q1/id/1">Newsletter</a>`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Notre newsletter" class="footer-link" target="_blank" rel="noopener" href="https://my.sendinblue.com/users/subscribe/js_id/3s2q1/id/1">Newsletter</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Application Error Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `POST`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 1
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/13-2e881985343712b6cded.chunk.js](https://www.demarches-simplifiees.fr/packs/js/13-2e881985343712b6cded.chunk.js)
  
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/robots.txt](https://www.demarches-simplifiees.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/suivi](https://www.demarches-simplifiees.fr/suivi)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/administration](https://www.demarches-simplifiees.fr/administration)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/stats](https://www.demarches-simplifiees.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/password/new](https://www.demarches-simplifiees.fr/users/password/new)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/commencer/demande-d-inscription-a-demarches-simplifiees](https://www.demarches-simplifiees.fr/commencer/demande-d-inscription-a-demarches-simplifiees)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/runtime~application-d193cc0db2885ecda3e1.js](https://www.demarches-simplifiees.fr/packs/js/runtime~application-d193cc0db2885ecda3e1.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/commencer](https://www.demarches-simplifiees.fr/commencer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/suivi](https://www.demarches-simplifiees.fr/suivi)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/administration](https://www.demarches-simplifiees.fr/administration)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/application-c2ab60ccfdc9383a65e9.chunk.js](https://www.demarches-simplifiees.fr/packs/js/application-c2ab60ccfdc9383a65e9.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/runtime~track-56b42adbc64acfab2dd8.js](https://www.demarches-simplifiees.fr/packs/js/runtime~track-56b42adbc64acfab2dd8.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/robots.txt](https://www.demarches-simplifiees.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/favicons/32x32-e102b3b45d814f1c53ec524455833223e7e83899443575994b0ffa455340ac3f.png](https://www.demarches-simplifiees.fr/assets/favicons/32x32-e102b3b45d814f1c53ec524455833223e7e83899443575994b0ffa455340ac3f.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/13-2e881985343712b6cded.chunk.js](https://www.demarches-simplifiees.fr/packs/js/13-2e881985343712b6cded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/favicons/16x16-02811394c05c7c0c941c5a7404bd2939ee9bf04eae047a68a576c098307d416c.png](https://www.demarches-simplifiees.fr/assets/favicons/16x16-02811394c05c7c0c941c5a7404bd2939ee9bf04eae047a68a576c098307d416c.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/application-c2ab60ccfdc9383a65e9.chunk.js](https://www.demarches-simplifiees.fr/packs/js/application-c2ab60ccfdc9383a65e9.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/application-7c6ba35c883f9c0fc1282d7e60cc889efba95787b005b6cc84f015ea8ac31dfa.css](https://www.demarches-simplifiees.fr/assets/application-7c6ba35c883f9c0fc1282d7e60cc889efba95787b005b6cc84f015ea8ac31dfa.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/runtime~application-d193cc0db2885ecda3e1.js](https://www.demarches-simplifiees.fr/packs/js/runtime~application-d193cc0db2885ecda3e1.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/Muli-Bold-d2dc11eebbc84a2ec6433ef027713b0c75c40c51cb522eaf2ab7dfa7be432e30.woff2](https://www.demarches-simplifiees.fr/assets/Muli-Bold-d2dc11eebbc84a2ec6433ef027713b0c75c40c51cb522eaf2ab7dfa7be432e30.woff2)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/favicons/96x96-4d358ff895f149a83a81b7aef960a9d90cdc916223f615c1acaa618dc2b8a254.png](https://www.demarches-simplifiees.fr/assets/favicons/96x96-4d358ff895f149a83a81b7aef960a9d90cdc916223f615c1acaa618dc2b8a254.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/runtime~track-56b42adbc64acfab2dd8.js](https://www.demarches-simplifiees.fr/packs/js/runtime~track-56b42adbc64acfab2dd8.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9.woff2](https://www.demarches-simplifiees.fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9.woff2)
  
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/suivi](https://www.demarches-simplifiees.fr/suivi)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/administration](https://www.demarches-simplifiees.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/application-7c6ba35c883f9c0fc1282d7e60cc889efba95787b005b6cc84f015ea8ac31dfa.css](https://www.demarches-simplifiees.fr/assets/application-7c6ba35c883f9c0fc1282d7e60cc889efba95787b005b6cc84f015ea8ac31dfa.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAQElEQVR42qXKwQkAIAxDUUdxtO6/RBQkQZvSi8I/pL4BoGw/XPkh4XigPmsUgh0626AjRsgxHTkUThsG2T/sIlzdTsp52kSS1wAAAABJRU5ErkJggg==`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/france_connect/particulier](https://www.demarches-simplifiees.fr/france_connect/particulier)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Bu131edcES96PQ13poTEDuYshvFfxQWqQZ`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/landing/hero/dematerialiser-42e628b42a640cfaec60f6fa548d248ed255026d71befea88113e2dc02b432f0.svg](https://www.demarches-simplifiees.fr/assets/landing/hero/dematerialiser-42e628b42a640cfaec60f6fa548d248ed255026d71befea88113e2dc02b432f0.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `7h112m-108-26v32m-7-33h120m0-33H360m115`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/password/new](https://www.demarches-simplifiees.fr/users/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/assets/Muli-Regular-bb62be3d0c815d86838837a026024c5833d2a54e3b457012d5d161a3ece1aaa9`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>~�ڲǭ��.�/�z\x000b�j��o��{wts�ywμ��7�6�M�s�7�ݚ燷o�{�]���zխ�q�Zi�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/password/reset-link-sent?email=foo-bar%40example.com](https://www.demarches-simplifiees.fr/users/password/reset-link-sent?email=foo-bar%40example.com)
  
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/application-c2ab60ccfdc9383a65e9.chunk.js](https://www.demarches-simplifiees.fr/packs/js/application-c2ab60ccfdc9383a65e9.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/administration](https://www.demarches-simplifiees.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/suivi](https://www.demarches-simplifiees.fr/suivi)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/13-2e881985343712b6cded.chunk.js](https://www.demarches-simplifiees.fr/packs/js/13-2e881985343712b6cded.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/password/new](https://www.demarches-simplifiees.fr/users/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/track-733ff033ba3a2f407152.chunk.js](https://www.demarches-simplifiees.fr/packs/js/track-733ff033ba3a2f407152.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script></p><p>//<![CDATA[</p><p>window.gon={};gon.autosave={"debounce_delay":3000,"status_visible_duration":6000};gon.autocomplete={"api_ge", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 1
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/administration](https://www.demarches-simplifiees.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr](https://www.demarches-simplifiees.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/suivi](https://www.demarches-simplifiees.fr/suivi)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/](https://www.demarches-simplifiees.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/contact](https://www.demarches-simplifiees.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/commencer](https://www.demarches-simplifiees.fr/commencer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/sitemap.xml](https://www.demarches-simplifiees.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/robots.txt](https://www.demarches-simplifiees.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/favicons/32x32-e102b3b45d814f1c53ec524455833223e7e83899443575994b0ffa455340ac3f.png](https://www.demarches-simplifiees.fr/assets/favicons/32x32-e102b3b45d814f1c53ec524455833223e7e83899443575994b0ffa455340ac3f.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/assets/favicons/16x16-02811394c05c7c0c941c5a7404bd2939ee9bf04eae047a68a576c098307d416c.png](https://www.demarches-simplifiees.fr/assets/favicons/16x16-02811394c05c7c0c941c5a7404bd2939ee9bf04eae047a68a576c098307d416c.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `145523070`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `680876936`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `271733878`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `643717713`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `373897302`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1926607734`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `530742520`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1990404162`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `701558691`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1473231341`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1069501632`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `155497632`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `606105819`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js](https://www.demarches-simplifiees.fr/packs/js/12-403cfdc475d2bf13e786.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `722521979`
  
  
  
  
Instances: 80
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>67108864, which evaluates to: 1972-02-16 17:21:04</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users](https://www.demarches-simplifiees.fr/users)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[email]`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users](https://www.demarches-simplifiees.fr/users)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users/sign_in](https://www.demarches-simplifiees.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://www.demarches-simplifiees.fr/users](https://www.demarches-simplifiees.fr/users)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[email]`
  
  
  
  
Instances: 6
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.demarches-simplifiees.fr/users/sign_in</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [data-disable-with] attribute </p><p></p><p>The user input found was:</p><p>commit=Se connecter</p><p></p><p>The user-controlled value was:</p><p>se connecter</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

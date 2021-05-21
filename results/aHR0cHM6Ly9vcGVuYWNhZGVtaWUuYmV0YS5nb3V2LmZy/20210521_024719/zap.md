
# ZAP Scanning Report

Generated on Fri, 21 May 2021 02:40:38


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Application Error Disclosure | Medium | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 4 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 4 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 2 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 1 | 
| Retrieved from Cache | Informational | 12 | 
| Storable but Non-Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Application Error Disclosure
##### Medium (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://openacademie.beta.gouv.fr/_next/606fdfa5-77bd-43e7-8f5c-e7e9c1166a43/page/_error.js](https://openacademie.beta.gouv.fr/_next/606fdfa5-77bd-43e7-8f5c-e7e9c1166a43/page/_error.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
Instances: 1
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/sitemap.xml](https://openacademie.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/robots.txt](https://openacademie.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="border-color:#ff7b19" href="https://tube.ac-lyon.fr/video-channels/openacademie_channel/videos" target="_blank" class="jsx-2155082703"><img src="/static/icon-video.png" alt="" class="jsx-2155082703"/>Tutoriels</a>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/trombinosco/](https://openacademie.beta.gouv.fr/trombinosco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="border-color:#a31390" href="https://tube.ac-lyon.fr/video-channels/openacademie_channel/videos" target="_blank" class="jsx-2155082703"><img src="/static/icon-video.png" alt="" class="jsx-2155082703"/>Tutoriels</a>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/cedisco/](https://openacademie.beta.gouv.fr/cedisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="border-color:#c40207" href="https://tube.ac-lyon.fr/video-channels/openacademie_channel/videos" target="_blank" class="jsx-2155082703"><img src="/static/icon-video.png" alt="" class="jsx-2155082703"/>Tutoriels</a>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="border-color:#24b47e" href="http://gestionnaires.actifforum.com/f23-openacademie-et-ses-outils" target="_blank" class="jsx-2155082703"><img src="/static/icon-forum.png" alt="" class="jsx-2155082703"/>Forum</a>`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Quicksand:400,500,700" rel="stylesheet" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Marvel" rel="stylesheet" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,700,800" rel="stylesheet" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Marvel" rel="stylesheet" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/robots.txt](https://openacademie.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Open+Sans:300,400,700,800" rel="stylesheet" class="next-head"/>`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Quicksand:400,500,700" rel="stylesheet" class="next-head"/>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/trombinosco/](https://openacademie.beta.gouv.fr/trombinosco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/votre-projet/](https://openacademie.beta.gouv.fr/votre-projet/)
  
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="jsx-1626402373">`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="jsx-1626402373">`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/trombinosco/](https://openacademie.beta.gouv.fr/trombinosco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="jsx-1626402373">`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/cedisco/](https://openacademie.beta.gouv.fr/cedisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="jsx-1626402373">`
  
  
  
  
Instances: 4
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://openacademie.beta.gouv.fr/_next/4e3a9486d176ee0d1840bacbcce7fb60/app.js](https://openacademie.beta.gouv.fr/_next/4e3a9486d176ee0d1840bacbcce7fb60/app.js)
  
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/robots.txt](https://openacademie.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/sitemap.xml](https://openacademie.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/trombinosco/](https://openacademie.beta.gouv.fr/trombinosco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/votre-projet/](https://openacademie.beta.gouv.fr/votre-projet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/sitemap.xml](https://openacademie.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/robots.txt](https://openacademie.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/votre-projet/](https://openacademie.beta.gouv.fr/votre-projet/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/trombinosco/](https://openacademie.beta.gouv.fr/trombinosco/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/_next/4e3a9486d176ee0d1840bacbcce7fb60/app.js](https://openacademie.beta.gouv.fr/_next/4e3a9486d176ee0d1840bacbcce7fb60/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/files/MobiliSCO_V7-2-1`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0nMjAwJyBoZWlnaHQ9JzIwMCcgZmlsbD0iIzAwMDAwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIiB4PSIwcHgiIHk9IjBweCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDEwMCAxMDA7IiB4bWw6c3BhY2U9InByZXNlcnZlIj48Zz48cG9seWdvbiBwb2ludHM9IjM2LjMsNTcuOSAxMS41LDgxIDg2LjUsODEgNjEuNSw1Ny42IDY0LjIsNTQuNyA5MCw3OC44IDkwLDIzLjIgNDksNjIuNCA4LDIzLjIgOCw3OC44IDMzLjYsNTUgICIvPjxwb2x5Z29uIHBvaW50cz0iODYuNiwyMSAxMS40LDIxIDQ5LDU2LjkgICIvPjwvZz48L3N2Zz4=`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/_next/606fdfa5-77bd-43e7-8f5c-e7e9c1166a43/page/contact.js](https://openacademie.beta.gouv.fr/_next/606fdfa5-77bd-43e7-8f5c-e7e9c1166a43/page/contact.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0nMjAwJyBoZWlnaHQ9JzIwMCcgZmlsbD0iIzAwMDAwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgdmVyc2lvbj0iMS4xIiB4PSIwcHgiIHk9IjBweCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDEwMCAxMDA7IiB4bWw6c3BhY2U9InByZXNlcnZlIj48Zz48cG9seWdvbiBwb2ludHM9IjM2LjMsNTcuOSAxMS41LDgxIDg2LjUsODEgNjEuNSw1Ny42IDY0LjIsNTQuNyA5MCw3OC44IDkwLDIzLjIgNDksNjIuNCA4LDIzLjIgOCw3OC44IDMzLjYsNTUgICIvPjxwb2x5Z29uIHBvaW50cz0iODYuNiwyMSAxMS40LDIxIDQ5LDU2LjkgICIvPjwvZz48L3N2Zz4=`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��Z�'?~)^��(n)bH#�W���</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/trombinosco/](https://openacademie.beta.gouv.fr/trombinosco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/votre-projet/](https://openacademie.beta.gouv.fr/votre-projet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script></p><p>          __NEXT_DATA__ = {"props":{},"pathname":"/","query":{},"buildId":"606fdfa5-77bd-43e7-8f5c-e7e9c1166a43","build", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://openacademie.beta.gouv.fr/_next/4e3a9486d176ee0d1840bacbcce7fb60/app.js](https://openacademie.beta.gouv.fr/_next/4e3a9486d176ee0d1840bacbcce7fb60/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 86475`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 86478`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 1`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 86478`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 1`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 20967`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/sitemap.xml](https://openacademie.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/robots.txt](https://openacademie.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 25417`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://openacademie.beta.gouv.fr](https://openacademie.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/opencartecomptable/](https://openacademie.beta.gouv.fr/opencartecomptable/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/outils/](https://openacademie.beta.gouv.fr/outils/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/sitemap.xml](https://openacademie.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/contact/](https://openacademie.beta.gouv.fr/contact/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/mobilisco/](https://openacademie.beta.gouv.fr/mobilisco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/gemasco/](https://openacademie.beta.gouv.fr/gemasco/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/emaintenance/](https://openacademie.beta.gouv.fr/emaintenance/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/robots.txt](https://openacademie.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/projet/](https://openacademie.beta.gouv.fr/projet/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `686673499`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `511178964`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `701247520`
  
  
  
  
* URL: [https://openacademie.beta.gouv.fr/](https://openacademie.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `663490327`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>686673499, which evaluates to: 1991-10-05 14:38:19</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

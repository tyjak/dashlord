
# ZAP Scanning Report

Generated on Wed, 21 Jul 2021 02:46:47


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 4 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: Wildcard Directive | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 77 | 
| Absence of Anti-CSRF Tokens | Low | 1 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 31 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 1 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 1 | 
| Modern Web Application | Informational | 1 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 4 | 

## Alert Detail


  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, img-src, connects-src, frame-src, frame-ancestors, font-src, media-src, prefetch-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `upgrade-insecure-requests; base-uri 'self'; object-src 'none'; script-src https://communaute.inclusion.beta.gouv.fr/logs/ https://communaute.inclusion.beta.gouv.fr/sidekiq/ https://communaute.inclusion.beta.gouv.fr/mini-profiler-resources/ https://aws1.discourse-cdn.com/standard20/assets/ https://aws1.discourse-cdn.com/standard20/brotli_asset/ https://communaute.inclusion.beta.gouv.fr/extra-locales/ https://dub2.discourse-cdn.com/standard20/highlight-js/ https://dub2.discourse-cdn.com/standard20/javascripts/ https://dub2.discourse-cdn.com/standard20/plugins/ https://dub2.discourse-cdn.com/standard20/theme-javascripts/ https://dub2.discourse-cdn.com/standard20/svg-sprite/ https://stats.data.gouv.fr/matomo.js https://stats.data.gouv.fr/piwik.php https://stats.data.gouv.fr/ http://communaute.inclusion.beta.gouv.fr/matomo.js http://communaute.inclusion.beta.gouv.fr/hotjar.js https://static.hotjar.com/ https://script.hotjar.com/; worker-src 'self' https://aws1.discourse-cdn.com/standard20/assets/ https://aws1.discourse-cdn.com/standard20/brotli_asset/ https://dub2.discourse-cdn.com/standard20/javascripts/ https://dub2.discourse-cdn.com/standard20/plugins/; manifest-src 'self'`
  
  
  
  
Instances: 1
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-chat-integration-9f895dea389d437b4b2ac94b9ff998789c8e9a6381d80ed5679cb5cb65247d82.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/discourse-spoiler-alert_0130a821b3cfb1f3e402b39aa38aa91ed814cf90.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="discourse-spoiler-alert" />`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto&amp;display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/plugins/lazy-yt-4e94ac3522a311236b5b7b0cf0ad4f98ee8632f45a4c686ac5b6676fcabe6f78.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_0130a821b3cfb1f3e402b39aa38aa91ed814cf90.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop" />`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/hosted-site_0130a821b3cfb1f3e402b39aa38aa91ed814cf90.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="hosted-site" />`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/discourse-details_0130a821b3cfb1f3e402b39aa38aa91ed814cf90.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="discourse-details" />`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_36_9a24f190e48a9b487c11ebbe62a20af87ec6f569.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="36"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/locales/fr-186a7655e4719468acf9424af0d08ffac6c76bf9ae00b29ff1c0b966163f1753.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_7_d1d29d46ae46d5c3caaecca2a55d4449afc9cba1.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="7"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/4f6452c43da32a01aec538e2ef5bdcce55ae713f.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/poll-4b9592bd848c2a090591a9b6dda4eba9bf34ad150e4263b26416959ecfde02ad.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_30_a4d4fc4441ebeaf2566c0c433386295dde24515f.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="30"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_12_cab15950f6790025b543a08515f6f06a3cde0040.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="12"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/color_definitions_base__7_7dc78672bf84ea92101c986e63ead91214f7dc57.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" class="light-scheme"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-akismet-b158ed3716457724147fc14a3b6cf4c6234b3b715dcbb2dc830a349d3da3a5db.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/vendor-9297d3b5d396b76cde3e1a19c960cf10c5edf8be99b1f5aeff21012e3ae57a34.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-cakeday-600ed4e8da158bdecffbe690ea83a887981a822344335a239e49500e491d5ded.gz.js"></script>`
  
  
  
  
Instances: 77
  
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
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id='hidden-login-form' method="post" action="/login" style="display: none;">`
  
  
  
  
Instances: 1
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "redirect" "signin-button" "signin_password" "signin_username" ].</p>
  
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
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-details-61554ea83ad59329c2d5c9f0390a0498f3e3665deb58d32dc608aeca24fa0bb9.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-details-61554ea83ad59329c2d5c9f0390a0498f3e3665deb58d32dc608aeca24fa0bb9.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/76a8e5d8a709906947df99a265301999077e3bf8.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/76a8e5d8a709906947df99a265301999077e3bf8.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/hosted-site-e21a70e39bd7e5c8f8a01dd0f404f767fc05ae1a75ae051a24828115f5ec5026.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/hosted-site-e21a70e39bd7e5c8f8a01dd0f404f767fc05ae1a75ae051a24828115f5ec5026.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/95d12c2d452939961609ccaf52169c4ef00a0573.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/95d12c2d452939961609ccaf52169c4ef00a0573.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-adplugin-b24bcfe138ed1d7e300b170177d714f4cd71a3a741e5ab09dfeabfcc1c83127b.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-adplugin-b24bcfe138ed1d7e300b170177d714f4cd71a3a741e5ab09dfeabfcc1c83127b.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/0632bf59c689cc9e3c5b1446fc07c3e1e836e12b.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/0632bf59c689cc9e3c5b1446fc07c3e1e836e12b.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/application-38e7ba8d44d8f6050114fd240f73ac6e4ed6933ec58a0117bc3ca11067780c4b.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/application-38e7ba8d44d8f6050114fd240f73ac6e4ed6933ec58a0117bc3ca11067780c4b.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/0828be4560e695619a7505baa86c3068cf1c6bcb.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/0828be4560e695619a7505baa86c3068cf1c6bcb.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/4f6452c43da32a01aec538e2ef5bdcce55ae713f.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/4f6452c43da32a01aec538e2ef5bdcce55ae713f.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/lazy-yt-4e94ac3522a311236b5b7b0cf0ad4f98ee8632f45a4c686ac5b6676fcabe6f78.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/lazy-yt-4e94ac3522a311236b5b7b0cf0ad4f98ee8632f45a4c686ac5b6676fcabe6f78.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-akismet-b158ed3716457724147fc14a3b6cf4c6234b3b715dcbb2dc830a349d3da3a5db.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-akismet-b158ed3716457724147fc14a3b6cf4c6234b3b715dcbb2dc830a349d3da3a5db.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/poll-4b9592bd848c2a090591a9b6dda4eba9bf34ad150e4263b26416959ecfde02ad.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/poll-4b9592bd848c2a090591a9b6dda4eba9bf34ad150e4263b26416959ecfde02ad.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/2ca7fc2ca3915b958f7d0c41d55a877c8bb93d99.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/2ca7fc2ca3915b958f7d0c41d55a877c8bb93d99.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/ae1fab3e0022ed39b6a49dc7bdb7ac0982a91d10.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/ae1fab3e0022ed39b6a49dc7bdb7ac0982a91d10.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-solved-be68360ae740ad69b2b4d48fbde314ac17a093b4f5256315469a13677501f9e4.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-solved-be68360ae740ad69b2b4d48fbde314ac17a093b4f5256315469a13677501f9e4.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-spoiler-alert-acf6e7cfe0c2032e73507e60b6015e04535b24fa5dbc1835274b53a43e4ae64e.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-spoiler-alert-acf6e7cfe0c2032e73507e60b6015e04535b24fa5dbc1835274b53a43e4ae64e.gz.js"></script>`
  
  
  
  
Instances: 31
  
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
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache, no-store`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/standard20/uploads/communauteinclusion/optimized/1X/a07679729a1e853552e36066838c0f0a9ed767f1_2_32x32`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>r���֧u���O�Z\x001av�ܢi����z)ܖ�"��ئ�7��U�kN������^���g��N��\x001c��\x001a��{���o��\x001d�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script type="application/ld+json">{"@context":"http://schema.org","@type":"WebSite","url":"https://communaute.inclusion.beta.go", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-path="/">
      
  <header class="d-header">
    <div class="wrap">
      <div class="contents clearfix">
        <div class="title">
          <a href="/">
              <img src="https://aws1.discourse-cdn.com/standard20/uploads/communauteinclusion/original/1X/6117f6e747c39c92550d81af891ffb2960858d81.svg" alt="Communauté de l&#39;inclusion" id="site-logo">
          </a>
        </div>
        <div class="panel clearfix">
            <span class='header-buttons'>
                <a href="/signup" class='btn btn-primary btn-small sign-up-button'>S&#39;inscrire</a>
              <a href="/login" class='btn btn-primary btn-small login-button btn-icon-text'><svg class="fa d-icon svg-icon svg-node" aria-hidden="true"><svg id="user" viewBox="0 0 448 512">
    <path d="M224 256c70.7 0 128-57.3 128-128S294.7 0 224 0 96 57.3 96 128s57.3 128 128 128zm89.6 32h-16.7c-22.2 10.2-46.9 16-72.9 16s-50.6-5.8-72.9-16h-16.7C60.2 288 0 348.2 0 422.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-41.6c0-74.2-60.2-134.4-134.4-134.4z"/>
  </svg></svg>
Connexion</a>
            </span>
        </div>
      </div>
    </div>
  </header>

      <div id="main-outlet" class="wrap" role="main">
        <!-- preload-content: -->
        <div itemscope itemtype='http://schema.org/ItemList'>
  <meta itemprop='itemListOrder' content='http://schema.org/ItemListOrderDescending'>
  <table class='category-list'>
    <thead>
      <tr>
        <th class='category'>Catégorie</th>
        <th class='topics'>Sujets</th>
      </tr>
    </thead>
    <tbody>
        <tr>
          <td class='category' style='border-color: #231F20;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='0'>
              <meta itemprop='url' content='/c/actualites/81'>
              <h3>
                <a href='/c/actualites/81'>
                  <span itemprop='name'>Actualités &amp; Informations</span>
                </a>
              </h3>
              <div itemprop='description'>Découvrez toute l’actualité des acteurs de l’inclusion (Evolutions des services de la plateforme, nouveautés, astuces…)</div>
            </div>
          </td>
          <td class='topics'>
            <div title='62 Sujets'>62</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #9C6FF4;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='1'>
              <meta itemprop='url' content='/c/spie/49'>
              <h3>
                <a href='/c/spie/49'>
                  <span itemprop='name'>Service Public de l&#39;Insertion et de l&#39;Emploi</span>
                </a>
              </h3>
              <div itemprop='description'>SPIE = Service Public de l’Insertion et de l’Emploi.</div>
            </div>
          </td>
          <td class='topics'>
            <div title='3 Sujets'>3</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #010738;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='2'>
              <meta itemprop='url' content='/c/se-retrouver-par-communaute-d-acteurs/45'>
              <h3>
                <a href='/c/se-retrouver-par-communaute-d-acteurs/45'>
                  <span itemprop='name'>Echanges par communauté d’acteurs</span>
                </a>
              </h3>
              <div itemprop='description'><strong>Echangez avec des collaborateurs d’une même organisation sur tout le territoire.</strong></div>
            </div>
          </td>
          <td class='topics'>
            <div title='3 Sujets'>3</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #026ADC;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='3'>
              <meta itemprop='url' content='/c/plateforme-de-linclusion/2'>
              <h3>
                <a href='/c/plateforme-de-linclusion/2'>
                  <span itemprop='name'>Les emplois de l&#39;inclusion &amp; vous</span>
                </a>
              </h3>
              <div itemprop='description'>Fonctionnement, actualités et retours utilisateurs</div>
            </div>
          </td>
          <td class='topics'>
            <div title='112 Sujets'>112</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #F25154;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='4'>
              <meta itemprop='url' content='/c/le-marche-de-linclusion-vous/53'>
              <h3>
                <a href='/c/le-marche-de-linclusion-vous/53'>
                  <span itemprop='name'>Le marché de l&#39;inclusion &amp; vous</span>
                </a>
              </h3>
              <div itemprop='description'>Mise en visibilité des offres commerciales des Entreprises Sociales Inclusives (ou Employeurs Solidaires)</div>
            </div>
          </td>
          <td class='topics'>
            <div title='1 Sujets'>1</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #FEAD1D;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='5'>
              <meta itemprop='url' content='/c/le-pilotage-de-linclusion/106'>
              <h3>
                <a href='/c/le-pilotage-de-linclusion/106'>
                  <span itemprop='name'>Le pilotage de l&#39;inclusion &amp; vous</span>
                </a>
              </h3>
              <div itemprop='description'>Proposer des tableaux de bord prêts à l’emploi pour permettre aux acteurs de l’inclusion de prendre des décisions mieux éclairées, tout en réduisant le temps de collecte de données et de production d’indicateurs</div>
            </div>
          </td>
          <td class='topics'>
            <div title='0 Sujets'>0</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #18A47D;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='6'>
              <meta itemprop='url' content='/c/se-retrouver-par-territoire/31'>
              <h3>
                <a href='/c/se-retrouver-par-territoire/31'>
                  <span itemprop='name'>Les Régionales</span>
                </a>
              </h3>
              <div itemprop='description'><strong>Entraide, bonnes pratiques, actualités, événements.</strong></div>
            </div>
          </td>
          <td class='topics'>
            <div title='1 Sujets'>1</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #ED207B;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='7'>
              <meta itemprop='url' content='/c/ressourcerie/46'>
              <h3>
                <a href='/c/ressourcerie/46'>
                  <span itemprop='name'>Outils &amp; Bons plans</span>
                </a>
              </h3>
              <div itemprop='description'><strong>Tous les outils et services publics numériques partagés par la communauté de l’inclusion.</strong></div>
            </div>
          </td>
          <td class='topics'>
            <div title='14 Sujets'>14</div>
          </td>
        </tr>
    </tbody>
  </table>
</div>




        <!-- :preload-content -->
        <footer class="noscript-footer-nav">
          <nav itemscope itemtype='http://schema.org/SiteNavigationElement'>
            <a href='/'>Accueil</a>
            <a href="/categories">Catégories</a>
            <a href="/guidelines">Charte</a>
            <a href="/tos">Conditions générales d&#39;utilisation</a>
            <a href="/privacy">Politique de confidentialité</a>
          </nav>
        </footer>
      </div>

      <footer id='noscript-footer'>
        <p>Optimisé par <a href="https://www.discourse.org">Discourse</a>, le rendu est meilleur quand JavaScript est activé.</p>
      </footer>
    </noscript>`
  
  
  
  
Instances: 1
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://forum.inclusion.beta.gouv.fr/](https://forum.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://forum.inclusion.beta.gouv.fr](https://forum.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://forum.inclusion.beta.gouv.fr/sitemap.xml](https://forum.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://forum.inclusion.beta.gouv.fr/robots.txt](https://forum.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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

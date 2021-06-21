
# ZAP Scanning Report

Generated on Mon, 21 Jun 2021 02:01:15


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
| Sub Resource Integrity Attribute Missing | Medium | 73 | 
| Absence of Anti-CSRF Tokens | Low | 1 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 29 | 
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, img-src, connects-src, frame-src, frame-ancestors, font-src, media-src, manifest-src, prefetch-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'none'; object-src 'none'; script-src https://communaute.inclusion.beta.gouv.fr/logs/ https://communaute.inclusion.beta.gouv.fr/sidekiq/ https://communaute.inclusion.beta.gouv.fr/mini-profiler-resources/ https://aws1.discourse-cdn.com/standard20/assets/ https://aws1.discourse-cdn.com/standard20/brotli_asset/ https://communaute.inclusion.beta.gouv.fr/extra-locales/ https://dub2.discourse-cdn.com/standard20/highlight-js/ https://dub2.discourse-cdn.com/standard20/javascripts/ https://dub2.discourse-cdn.com/standard20/plugins/ https://dub2.discourse-cdn.com/standard20/theme-javascripts/ https://dub2.discourse-cdn.com/standard20/svg-sprite/ https://stats.data.gouv.fr/matomo.js https://stats.data.gouv.fr/piwik.php https://stats.data.gouv.fr/ http://communaute.inclusion.beta.gouv.fr/matomo.js http://communaute.inclusion.beta.gouv.fr/hotjar.js https://static.hotjar.com/ https://script.hotjar.com/; worker-src 'self' https://aws1.discourse-cdn.com/standard20/assets/ https://aws1.discourse-cdn.com/standard20/brotli_asset/ https://dub2.discourse-cdn.com/standard20/javascripts/ https://dub2.discourse-cdn.com/standard20/plugins/`
  
  
  
  
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
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto&amp;display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_b0a8164acc137a940681055d724297cd756e95c1.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop" data-theme-id="7"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/vendor-d0c9e6c505a84fa8f3e94def4d2b21ca24b3da8a8d3d2ae26f90b26f3ea9fa94.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/locales/fr-5433648e022207e1a2e330ed60a8b33f6ed1f870e34f6bf879579b4a2a8deed7.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/discourse-cakeday_b0a8164acc137a940681055d724297cd756e95c1.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="discourse-cakeday" data-theme-id="7"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/lazy-yt-9db193c8caacf2e3b3a24ed4c63699ad497c210f668f467d95380efd00982345.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/4f6452c43da32a01aec538e2ef5bdcce55ae713f.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_25_195cf604c1796d02b4e288ef79d4b09939a89711.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="25"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-chat-integration-fa17daf77bf2a81735aed513146a082aa2486d1fc37f77b4b6439477c7608520.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/poll-05bb4e6a91c9f4511c5c98fe452a74c9bc1fac76f374e9f7623ad639fd8e7690.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/discourse-chat-integration_b0a8164acc137a940681055d724297cd756e95c1.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="discourse-chat-integration" data-theme-id="7"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/vendor-d0c9e6c505a84fa8f3e94def4d2b21ca24b3da8a8d3d2ae26f90b26f3ea9fa94.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-narrative-bot-0b1e40d099d739cee23bbad45c2fb5eac1dcaaba028fdc9fa21b9e32930ec40b.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-adplugin-b96fb7611234546f6be4f2ef6176222fea7c538e6e14af69ab4520482e5d64a0.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-akismet-fd0f01327e978fcb6a168b08adc65cffa8021a5fdd2e186dee94a711b5225b75.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preload" href="https://aws1.discourse-cdn.com/standard20/assets/browser-detect-115ab5953de1b5bb122bfb26b757f5391dd8d1d2aef2b81baf7b59aee99d9f34.gz.js" as="script">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/browser-detect-115ab5953de1b5bb122bfb26b757f5391dd8d1d2aef2b81baf7b59aee99d9f34.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/hosted-site-8a1feb14846dbc2670cd6a67a5567395f532c015a7d849e61a6f461b2d77d79c.gz.js"></script>`
  
  
  
  
Instances: 73
  
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
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/application-f7789e702ef7ef572dd76361fda3dcaf312aca19c10212e726e7d0954e04549e.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/application-f7789e702ef7ef572dd76361fda3dcaf312aca19c10212e726e7d0954e04549e.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/hosted-site-8a1feb14846dbc2670cd6a67a5567395f532c015a7d849e61a6f461b2d77d79c.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/hosted-site-8a1feb14846dbc2670cd6a67a5567395f532c015a7d849e61a6f461b2d77d79c.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-cakeday-4a048c366290fa5def00e5becaa720dcca5212082db42efac4889bd9256133bc.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-cakeday-4a048c366290fa5def00e5becaa720dcca5212082db42efac4889bd9256133bc.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/lazy-yt-9db193c8caacf2e3b3a24ed4c63699ad497c210f668f467d95380efd00982345.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/lazy-yt-9db193c8caacf2e3b3a24ed4c63699ad497c210f668f467d95380efd00982345.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/locales/fr-5433648e022207e1a2e330ed60a8b33f6ed1f870e34f6bf879579b4a2a8deed7.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/locales/fr-5433648e022207e1a2e330ed60a8b33f6ed1f870e34f6bf879579b4a2a8deed7.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/0632bf59c689cc9e3c5b1446fc07c3e1e836e12b.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/0632bf59c689cc9e3c5b1446fc07c3e1e836e12b.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-solved-a620eb3e2f6fc280f3e88e6e34c25dd283620a7d47b166914ff07b22179eef5e.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-solved-a620eb3e2f6fc280f3e88e6e34c25dd283620a7d47b166914ff07b22179eef5e.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/439467e32046c35cf61da5f23dacfc0c9bd80a2e.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src='https://dub2.discourse-cdn.com/standard20/theme-javascripts/439467e32046c35cf61da5f23dacfc0c9bd80a2e.js?__ws=communaute.inclusion.beta.gouv.fr'></script>`
  
  
  
  
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
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/vendor-d0c9e6c505a84fa8f3e94def4d2b21ca24b3da8a8d3d2ae26f90b26f3ea9fa94.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/vendor-d0c9e6c505a84fa8f3e94def4d2b21ca24b3da8a8d3d2ae26f90b26f3ea9fa94.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-details-9be9806ef2338ede8e5c567dfd5b521aaad27d01694f01c604516118466d2120.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-details-9be9806ef2338ede8e5c567dfd5b521aaad27d01694f01c604516118466d2120.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-akismet-fd0f01327e978fcb6a168b08adc65cffa8021a5fdd2e186dee94a711b5225b75.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-akismet-fd0f01327e978fcb6a168b08adc65cffa8021a5fdd2e186dee94a711b5225b75.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-local-dates-cfd10a0543a7fca73f7386759c3978d5d9a5e6117f19819c2ef3e4389200c61b.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-local-dates-cfd10a0543a7fca73f7386759c3978d5d9a5e6117f19819c2ef3e4389200c61b.gz.js"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/2ca7fc2ca3915b958f7d0c41d55a877c8bb93d99.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/2ca7fc2ca3915b958f7d0c41d55a877c8bb93d99.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-spoiler-alert-265785c5c99c237ac058e9297da2c398a80805d63e1e9b9caaa99e3251154864.gz.js`
  
  
  * Evidence: `<script src="https://aws1.discourse-cdn.com/standard20/assets/plugins/discourse-spoiler-alert-265785c5c99c237ac058e9297da2c398a80805d63e1e9b9caaa99e3251154864.gz.js"></script>`
  
  
  
  
Instances: 29
  
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
            <div title='54 Sujets'>54</div>
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
            <div title='5 Sujets'>5</div>
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
            <div title='103 Sujets'>103</div>
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
            <div title='2 Sujets'>2</div>
          </td>
        </tr>
        <tr>
          <td class='category' style='border-color: #FBA900;'>
            <div itemprop='itemListElement' itemscope itemtype='http://schema.org/ListItem'>
              <meta itemprop='position' content='5'>
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
              <meta itemprop='position' content='6'>
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
            <div title='12 Sujets'>12</div>
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
        <p>Propulsé par <a href="https://www.discourse.org">Discourse</a>, le rendu est meilleur quand JavaScript est activé.</p>
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

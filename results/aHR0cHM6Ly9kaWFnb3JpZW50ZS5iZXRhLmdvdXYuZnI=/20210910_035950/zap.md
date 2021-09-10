
# ZAP Scanning Report

Generated on Fri, 10 Sep 2021 03:51:30


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 4 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: Wildcard Directive | Medium | 8 | 
| Reverse Tabnabbing | Medium | 8 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| Absence of Anti-CSRF Tokens | Low | 8 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 8 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 10 | 

## Alert Detail


  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>script-src, style-src, img-src, connects-src, frame-src, font-src, media-src, object-src, manifest-src, worker-src, prefetch-src, form-action</p><p></p><p>The directive(s): form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `frame-ancestors  https://diagoriente.beta.gouv.fr/ app.diagoriente.beta.gouv.fr diagoriente.beta.gouv.fr professionnels.diagoriente.beta.gouv.fr https://test.mathislorthios.dev test.mathislorthios.dev https://metis.afpa.fr https://metis.afpa.fr/;`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://beta.gouv.fr/" target="_blank"><img style="width:100%;height:100%;margin-bottom:0" class="image2" src="/static/db2acdbfe5631303c513cc3611c90843/m.svg" alt="logo"/></a>`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://sibforms.com/forms/end-form/build/sib-styles.css">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://sibforms.com/forms/end-form/build/sib-styles.css">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://sibforms.com/forms/end-form/build/sib-styles.css">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://sibforms.com/forms/end-form/build/sib-styles.css">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://sibforms.com/forms/end-form/build/sib-styles.css">`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="sib-form" style="padding:0px" method="POST"
                    action="https://b54ca439.sibforms.com/serve/MUIEAOHL5-dvwPku0FEpat7THy2EZsEXhqs-p2phrL71trvz3W8FNGSHQQxXftCLHFIvZM_sG6pv5zd20QvVgJUvA30UUytioTT1S2p59YTrUiuL9mrvnAprcXFpNE0GbpnHhlLRiPryi4H4ychrC0GuznrfVb_034Qpj-9kKheghO8umISR1tvk0Sq8Hdg8bgiWuh_L4R4W7Q8Q"
                    data-type="subscription">`
  
  
  
  
Instances: 8
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "EMAIL" "email_address_check" "locale" ].</p>
  
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
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://sibforms.com/forms/end-form/build/main.js`
  
  
  * Evidence: `<script src="https://sibforms.com/forms/end-form/build/main.js">
    </script>`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/page-data/sq/d/3715776872.json](https://diagoriente.beta.gouv.fr/page-data/sq/d/3715776872.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/page-data/sq/d/1947816842.json](https://diagoriente.beta.gouv.fr/page-data/sq/d/1947816842.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/page-data/index/page-data.json](https://diagoriente.beta.gouv.fr/page-data/index/page-data.json)
  
  
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

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/framework-93cd612b3d643a08ad6d.js](https://diagoriente.beta.gouv.fr/framework-93cd612b3d643a08ad6d.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/webpack-runtime-e9082057ace1f6b26b6a.js](https://diagoriente.beta.gouv.fr/webpack-runtime-e9082057ace1f6b26b6a.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/styles-89fd2ae28bdf06750a71.js](https://diagoriente.beta.gouv.fr/styles-89fd2ae28bdf06750a71.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/4c1c676572c521914252e8b5391e12a5a8171883-d4a682656e8574deee17.js](https://diagoriente.beta.gouv.fr/4c1c676572c521914252e8b5391e12a5a8171883-d4a682656e8574deee17.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UCfh-72vbjMaa-ZFzKIAF1Dw`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/0b7b90cd-1678aede3a96c066fcac.js](https://diagoriente.beta.gouv.fr/0b7b90cd-1678aede3a96c066fcac.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/app-8a21aad41e6ed296f4ca.js](https://diagoriente.beta.gouv.fr/app-8a21aad41e6ed296f4ca.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `/campus2023/components/demarcheCampus/demarche/`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `/static/odile-Regular-93680edbdd52f22d0fe76981257aeb59`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��Z�'?�إ{�^��Z��w��\x001eu�]�g���\x001f{���]���</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/component---src-pages-index-tsx-3a95a5d615bc20bd1c94.js](https://diagoriente.beta.gouv.fr/component---src-pages-index-tsx-3a95a5d615bc20bd1c94.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/4c1c676572c521914252e8b5391e12a5a8171883-d4a682656e8574deee17.js](https://diagoriente.beta.gouv.fr/4c1c676572c521914252e8b5391e12a5a8171883-d4a682656e8574deee17.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/2d4594b7-8e97825caa24f86f4506.js](https://diagoriente.beta.gouv.fr/2d4594b7-8e97825caa24f86f4506.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `dB`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/app-8a21aad41e6ed296f4ca.js](https://diagoriente.beta.gouv.fr/app-8a21aad41e6ed296f4ca.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/component---src-pages-home-page-home-page-tsx-a35898d01c35c94dfa40.js](https://diagoriente.beta.gouv.fr/component---src-pages-home-page-home-page-tsx-a35898d01c35c94dfa40.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/323797f025cf413a17fde46afddc588921e8fb37-5a8aefbea75c2fa0bec5.js](https://diagoriente.beta.gouv.fr/323797f025cf413a17fde46afddc588921e8fb37-5a8aefbea75c2fa0bec5.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/component---src-pages-cgu-cgu-tsx-cfc85a2a652fb97277f1.js](https://diagoriente.beta.gouv.fr/component---src-pages-cgu-cgu-tsx-cfc85a2a652fb97277f1.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Username`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/0b7b90cd-1678aede3a96c066fcac.js](https://diagoriente.beta.gouv.fr/0b7b90cd-1678aede3a96c066fcac.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `SELECT`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/framework-93cd612b3d643a08ad6d.js](https://diagoriente.beta.gouv.fr/framework-93cd612b3d643a08ad6d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/component---src-pages-education-education-tsx-28ac1e5759ab01d696fe.js](https://diagoriente.beta.gouv.fr/component---src-pages-education-education-tsx-28ac1e5759ab01d696fe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/polyfill-40d5b9705d0e5c94fc9f.js](https://diagoriente.beta.gouv.fr/polyfill-40d5b9705d0e5c94fc9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/a79515f9-c7b83fbbdc210e296681.js](https://diagoriente.beta.gouv.fr/a79515f9-c7b83fbbdc210e296681.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `SELECT`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(window.webpackJsonp=window.webpackJsonp||[]).push([[29,20,21,22,24,26,32,33],{"+3zt":function(e,t,a){e.exports={essaiContainer:", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/framework-93cd612b3d643a08ad6d.js](https://diagoriente.beta.gouv.fr/framework-93cd612b3d643a08ad6d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/polyfill-40d5b9705d0e5c94fc9f.js](https://diagoriente.beta.gouv.fr/polyfill-40d5b9705d0e5c94fc9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/4c1c676572c521914252e8b5391e12a5a8171883-d4a682656e8574deee17.js](https://diagoriente.beta.gouv.fr/4c1c676572c521914252e8b5391e12a5a8171883-d4a682656e8574deee17.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-T5SXVD3" height="0" width="0" style="display: none; visibility: hidden" aria-hidden="true"></iframe></noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/mentions-legales](https://diagoriente.beta.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/statistiques](https://diagoriente.beta.gouv.fr/statistiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/cgu](https://diagoriente.beta.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/icons/icon-48x48.png?v=72d8827a7ff40f1b8f3eae272a482423](https://diagoriente.beta.gouv.fr/icons/icon-48x48.png?v=72d8827a7ff40f1b8f3eae272a482423)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/favicon-32x32.png?v=72d8827a7ff40f1b8f3eae272a482423](https://diagoriente.beta.gouv.fr/favicon-32x32.png?v=72d8827a7ff40f1b8f3eae272a482423)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/manifest.webmanifest](https://diagoriente.beta.gouv.fr/manifest.webmanifest)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
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
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `63159454`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `63159454`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `1947816842`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1947816842`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr](https://diagoriente.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `63159454`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/](https://diagoriente.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `63159454`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1947816842`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/documentation](https://diagoriente.beta.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `1947816842`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/robots.txt](https://diagoriente.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `63159454`
  
  
  
  
* URL: [https://diagoriente.beta.gouv.fr/sitemap.xml](https://diagoriente.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1947816842`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>63159454, which evaluates to: 1972-01-02 00:17:34</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

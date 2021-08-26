
# ZAP Scanning Report

Generated on Thu, 26 Aug 2021 05:28:33


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 8 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Reverse Tabnabbing | Medium | 5 | 
| X-Frame-Options Header Not Set | Medium | 7 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| CSP: Notices | Low | 3 | 
| Dangerous JS Functions | Low | 6 | 
| Incomplete or No Cache-control Header Set | Low | 8 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec) | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 8 | 
| Storable and Cacheable Content | Informational | 3 | 
| Timestamp Disclosure - Unix | Informational | 5 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-b2242b6c-49a1-4122-b720-95d1b01d688d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-7b5edb34-b535-4afb-a20f-b294eb556181' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-403101d3-2e5a-4ba8-98b5-dcc37eff4591' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
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
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-b2242b6c-49a1-4122-b720-95d1b01d688d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-7b5edb34-b535-4afb-a20f-b294eb556181' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-403101d3-2e5a-4ba8-98b5-dcc37eff4591' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>img-src, frame-src, frame-ancestors, media-src, object-src</p><p></p><p>The directive(s): frame-ancestors are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-403101d3-2e5a-4ba8-98b5-dcc37eff4591' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-b2242b6c-49a1-4122-b720-95d1b01d688d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-7b5edb34-b535-4afb-a20f-b294eb556181' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
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
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://community.hedgedoc.org" target="_blank"><i class="fa fa-users fa-fw"></i> Join the community</a>`
  
  
  
  
* URL: [https://pad.incubateur.net/yaml-metadata](https://pad.incubateur.net/yaml-metadata)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://community.hedgedoc.org" target="_blank"><i class="fa fa-users fa-fw"></i> Join the community</a>`
  
  
  
  
* URL: [https://pad.incubateur.net/slide-example](https://pad.incubateur.net/slide-example)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://community.hedgedoc.org" target="_blank"><i class="fa fa-users fa-fw"></i> Join the community</a>`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/hedgedoc" target="_blank" rel="noopener">Source Code</a>`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/hedgedoc" target="_blank" rel="noopener">Source Code</a>`
  
  
  
  
Instances: 5
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/yaml-metadata](https://pad.incubateur.net/yaml-metadata)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/slide-example](https://pad.incubateur.net/slide-example)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 7
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline">`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline">`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>Duplicate source-expression *</p><p></p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-b2242b6c-49a1-4122-b720-95d1b01d688d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-403101d3-2e5a-4ba8-98b5-dcc37eff4591' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none';base-uri 'self';connect-src 'self';font-src 'self';manifest-src 'self';frame-src 'self' https://player.vimeo.com https://www.slideshare.net/slideshow/embed_code/key/ https://www.youtube.com *;img-src *;script-src https://pad.incubateur.net/build/ https://pad.incubateur.net/js/ https://pad.incubateur.net/config https://gist.github.com/ https://vimeo.com/api/oembed.json https://www.slideshare.net/api/oembed/2 'unsafe-inline' 'nonce-7b5edb34-b535-4afb-a20f-b294eb556181' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM=';style-src https://pad.incubateur.net/build/ https://pad.incubateur.net/css/ 'unsafe-inline' https://github.githubassets.com;object-src * *;form-action 'self';media-src *;upgrade-insecure-requests`
  
  
  
  
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

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js](https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js](https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~index~index-pack~pretty~pretty-pack~slide~slide-pack.8092a5d86578aedd8625.js](https://pad.incubateur.net/build/vendors~index~index-pack~pretty~pretty-pack~slide~slide-pack.8092a5d86578aedd8625.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/pretty-pack.b21dd2f79ece6ba8677f.js](https://pad.incubateur.net/build/pretty-pack.b21dd2f79ece6ba8677f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/index-pack.2c5918216c59b64772c4.js](https://pad.incubateur.net/build/index-pack.2c5918216c59b64772c4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://pad.incubateur.net/slide-example](https://pad.incubateur.net/slide-example)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/site.webmanifest](https://pad.incubateur.net/icons/site.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/yaml-metadata](https://pad.incubateur.net/yaml-metadata)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js](https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/config](https://pad.incubateur.net/config)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack~index~index-pack~pretty~pretty-pack~slide~slide-pack.9f63351fd96366e9e752.js](https://pad.incubateur.net/build/vendors~cover~cover-pack~index~index-pack~pretty~pretty-pack~slide~slide-pack.9f63351fd96366e9e752.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js](https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/build/common.1c773fb6375f6e4c11cf.js](https://pad.incubateur.net/build/common.1c773fb6375f6e4c11cf.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
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
  
  
  
* URL: [https://pad.incubateur.net/new](https://pad.incubateur.net/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/me/delete/](https://pad.incubateur.net/me/delete/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/robots.txt](https://pad.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/sitemap.xml](https://pad.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/logout](https://pad.incubateur.net/logout)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://pad.incubateur.net/me/export](https://pad.incubateur.net/me/export)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec)
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) headers were found, a response with multiple HSTS header entries is not compliant with the specification (RFC 6797) and only the first HSTS header will be processed others will be ignored by user agents or the HSTS policy may be incorrectly applied.</p><p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL).</p>
  
  
  
* URL: [https://pad.incubateur.net/logout](https://pad.incubateur.net/logout)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/me/export](https://pad.incubateur.net/me/export)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/sitemap.xml](https://pad.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/robots.txt](https://pad.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/new](https://pad.incubateur.net/new)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/me/delete/](https://pad.incubateur.net/me/delete/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that only one component in your stack: code, web server, application server, load balancer, etc. is configured to set or add a HTTP Strict-Transport-Security (HSTS) header.</p>
  
### Reference
* http://tools.ietf.org/html/rfc6797#section-8.1

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/site.webmanifest](https://pad.incubateur.net/icons/site.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/favicon-32x32.png](https://pad.incubateur.net/icons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/apple-touch-icon.png](https://pad.incubateur.net/icons/apple-touch-icon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/favicon.ico](https://pad.incubateur.net/icons/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/safari-pinned-tab.svg](https://pad.incubateur.net/icons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/favicon-16x16.png](https://pad.incubateur.net/icons/favicon-16x16.png)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `3b75-Q1jK3et25H+doCfldiwS+sSG7vg`
  
  
  
  
* URL: [https://pad.incubateur.net/me/export](https://pad.incubateur.net/me/export)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWQ3SRqXfAGwx4O0aAqLT07i92QMnzs-Q`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `3a7e-uAP1WecOIivF100oF9HC7++QfMc`
  
  
  
  
* URL: [https://pad.incubateur.net/logout](https://pad.incubateur.net/logout)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWQ3SRqXfAGwx4O0aAqLT07i92QMnzs-Q`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `9dca-tGMHyBJV6np6mx+sk8J/ITyBJGU`
  
  
  
  
* URL: [https://pad.incubateur.net/sitemap.xml](https://pad.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWQ3SRqXfAGwx4O0aAqLT07i92QMnzs-Q`
  
  
  
  
* URL: [https://pad.incubateur.net/me/delete/](https://pad.incubateur.net/me/delete/)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWQ3SRqXfAGwx4O0aAqLT07i92QMnzs-Q`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Evidence: `fcf5-5sIxJCaUj9WNO6jmtu/Y5oZdwsY`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `3a7e-uAP1WecOIivF100oF9HC7++QfMc`
  
  
  
  
* URL: [https://pad.incubateur.net/new](https://pad.incubateur.net/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWQ3SRqXfAGwx4O0aAqLT07i92QMnzs-Q`
  
  
  
  
* URL: [https://pad.incubateur.net/robots.txt](https://pad.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWQ3SRqXfAGwx4O0aAqLT07i92QMnzs-Q`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Evidence: `15ea-sJonn05i7ecczozHKV37i9nNGXY`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>ݾ��
c+w�ۑ�v���ذK�\x0012\x001b��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<!-- delete user modal -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js](https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack~index~index-pack~pretty~pretty-pack~slide~slide-pack.9f63351fd96366e9e752.js](https://pad.incubateur.net/build/vendors~cover~cover-pack~index~index-pack~pretty~pretty-pack~slide~slide-pack.9f63351fd96366e9e752.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js](https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js](https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js](https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
Instances: 10
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "var t=d.defineLocale("da",{months:"januar_februar_marts_april_maj_juni_juli_august_september_oktober_november_december".split("_", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js](https://pad.incubateur.net/build/cover-pack.9162a6d0589f02e83c1b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">
            <div class="item">
              <div class="ui-history-pin fa fa-thumb-tack fa-fw"></div>
              <div class="ui-history-close fa fa-close fa-fw" data-toggle="modal" data-target=".delete-history-modal"></div>
              <div class="content">
                <h4 class="text"></h4>
                <p>
                  <i><i class="fa fa-clock-o"></i> visited </i><i class="fromNow"></i>
                  <br>
                  <i class="timestamp" style="display:none;"></i>
                  <i class="time"></i>
                </p>
                <p class="tags"></p>
              </div>
            </div>
          </a>`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="ui-edit" title="Edit this note"><i class="fa fa-fw fa-pencil"></i></a>`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack~index~index-pack~pretty~pretty-pack~slide~slide-pack.9f63351fd96366e9e752.js](https://pad.incubateur.net/build/vendors~cover~cover-pack~index~index-pack~pretty~pretty-pack~slide~slide-pack.9f63351fd96366e9e752.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js](https://pad.incubateur.net/build/vendors~cover~cover-pack.46c3a7f3928401ea3af9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class='page' href='#'></a>`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Intro</a>`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="ui-edit" title="Edit this note"><i class="fa fa-fw fa-pencil"></i></a>`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#">Intro</a>`
  
  
  
  
* URL: [https://pad.incubateur.net/yaml-metadata](https://pad.incubateur.net/yaml-metadata)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="ui-short-status" data-toggle="dropdown"><span class="label label-danger"><i class="fa fa-plug"></i> </span>
            </a>`
  
  
  
  
* URL: [https://pad.incubateur.net/slide-example](https://pad.incubateur.net/slide-example)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="ui-short-status" data-toggle="dropdown"><span class="label label-danger"><i class="fa fa-plug"></i> </span>
            </a>`
  
  
  
  
* URL: [https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js](https://pad.incubateur.net/build/vendors~common.5e1034cb4e0fcfb8b567.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+Fe+"'></a>`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="ui-short-status" data-toggle="dropdown"><span class="label label-danger"><i class="fa fa-plug"></i> </span>
            </a>`
  
  
  
  
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
  
  
  
* URL: [https://pad.incubateur.net/me/export](https://pad.incubateur.net/me/export)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/robots.txt](https://pad.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/new](https://pad.incubateur.net/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://pad.incubateur.net/logout](https://pad.incubateur.net/logout)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://pad.incubateur.net/sitemap.xml](https://pad.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://pad.incubateur.net/me/delete/](https://pad.incubateur.net/me/delete/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://pad.incubateur.net/build/3.b67314821de89ccff48b.css](https://pad.incubateur.net/build/3.b67314821de89ccff48b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000000`
  
  
  
  
* URL: [https://pad.incubateur.net/build/3.b67314821de89ccff48b.css](https://pad.incubateur.net/build/3.b67314821de89ccff48b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `80000000`
  
  
  
  
* URL: [https://pad.incubateur.net/build/3.b67314821de89ccff48b.css](https://pad.incubateur.net/build/3.b67314821de89ccff48b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `66666667`
  
  
  
  
* URL: [https://pad.incubateur.net/build/3.b67314821de89ccff48b.css](https://pad.incubateur.net/build/3.b67314821de89ccff48b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `42857143`
  
  
  
  
* URL: [https://pad.incubateur.net/build/3.b67314821de89ccff48b.css](https://pad.incubateur.net/build/3.b67314821de89ccff48b.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `33333333`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>00000000, which evaluates to: 1970-01-01 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

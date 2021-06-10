
# ZAP Scanning Report

Generated on Thu, 10 Jun 2021 03:01:30


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 6 |
| Low | 8 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 2 | 
| CSP: style-src unsafe-inline | Medium | 4 | 
| CSP: Wildcard Directive | Medium | 4 | 
| Reverse Tabnabbing | Medium | 5 | 
| Source Code Disclosure - SQL | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 7 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| CSP: Notices | Low | 4 | 
| Dangerous JS Functions | Low | 5 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec) | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| CSP: X-Content-Security-Policy | Informational | 1 | 
| CSP: X-WebKit-CSP | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 8 | 
| Storable and Cacheable Content | Informational | 3 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://pad.incubateur.net/build/pretty-pack.eff46802d40e9014e27a.js](https://pad.incubateur.net/build/pretty-pack.eff46802d40e9014e27a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4426950407214463`
  
  
  
  
* URL: [https://pad.incubateur.net/build/index-pack.8ee15b21a281c9bb0f2f.js](https://pad.incubateur.net/build/index-pack.8ee15b21a281c9bb0f2f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4426950407214463`
  
  
  
  
Instances: 2
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Visa</p><p>Bank Identification Number: 442695</p><p>Brand: VISA</p><p>Category: CLASSIC</p><p>Issuer: GlanDALE AREA SCHOOLS F.C.U.</p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-9518b569-1201-4968-8f89-26df1ac2c9b1' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-d6c1ddab-cf91-4de3-8c30-cd25ac5e01fd' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-0caf76c9-3a7f-422d-9cb0-ca0e94de9d64' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-f76775fc-b991-40fc-b30e-96ce536d997d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>img-src, connect-src, frame-src, frame-ancestors, media-src, object-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-9518b569-1201-4968-8f89-26df1ac2c9b1' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-d6c1ddab-cf91-4de3-8c30-cd25ac5e01fd' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-f76775fc-b991-40fc-b30e-96ce536d997d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-0caf76c9-3a7f-422d-9cb0-ca0e94de9d64' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 16
  
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

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://pad.incubateur.net/build/pretty-pack.eff46802d40e9014e27a.js](https://pad.incubateur.net/build/pretty-pack.eff46802d40e9014e27a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select set skip startsas stop title update waitsas where window x systask add and alter as cascade check create delete describe distinct drop foreign from group having index insert into in key like message modify msgtype not null on or order primary references reset restrict select set table unique update validate view where`
  
  
  
  
* URL: [https://pad.incubateur.net/build/index-pack.8ee15b21a281c9bb0f2f.js](https://pad.incubateur.net/build/index-pack.8ee15b21a281c9bb0f2f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select set skip startsas stop title update waitsas where window x systask add and alter as cascade check create delete describe distinct drop foreign from group having index insert into in key like message modify msgtype not null on or order primary references reset restrict select set table unique update validate view where`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>select set skip startsas stop title update waitsas where window x systask add and alter as cascade check create delete describe distinct drop foreign from group having index insert into in key like message modify msgtype not null on or order primary references reset restrict select set table unique update validate view where</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/config/Safe.js](https://pad.incubateur.net/build/MathJax/config/Safe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script
 *    src="http://cdn.jsdelivr.net/npm/mathjax@2/MathJax.js?config=TeX-AMS_HTML,Safe">
 *  </script>`
  
  
  
  
Instances: 1
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline">`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-inline">`
  
  
  
  
Instances: 2
  
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

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>1:539: The child-src directive is deprecated as of CSP level 3. Authors who wish to regulate nested browsing contexts and workers SHOULD use the frame-src and worker-src directives, respectively.</p><p></p>
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-d6c1ddab-cf91-4de3-8c30-cd25ac5e01fd' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-0caf76c9-3a7f-422d-9cb0-ca0e94de9d64' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-9518b569-1201-4968-8f89-26df1ac2c9b1' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-f76775fc-b991-40fc-b30e-96ce536d997d' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://pad.incubateur.net/build/index-pack.8ee15b21a281c9bb0f2f.js](https://pad.incubateur.net/build/index-pack.8ee15b21a281c9bb0f2f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `$Eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js](https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/pretty-pack.eff46802d40e9014e27a.js](https://pad.incubateur.net/build/pretty-pack.eff46802d40e9014e27a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `$Eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js](https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js](https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js](https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/slide-example](https://pad.incubateur.net/slide-example)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/yaml-metadata](https://pad.incubateur.net/yaml-metadata)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/js/mathjax-config-extra.js](https://pad.incubateur.net/js/mathjax-config-extra.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pad.incubateur.net/config](https://pad.incubateur.net/config)
  
  
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
  
  
  
* URL: [https://pad.incubateur.net/build/cover.9d2bc807d9062ac0ef97.css](https://pad.incubateur.net/build/cover.9d2bc807d9062ac0ef97.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css](https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/site.webmanifest](https://pad.incubateur.net/icons/site.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://pad.incubateur.net/icons/safari-pinned-tab.svg](https://pad.incubateur.net/icons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net/banner/banner_vertical_color.svg](https://pad.incubateur.net/banner/banner_vertical_color.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net/build/font-pack.8b60ca65f33929a11b34.css](https://pad.incubateur.net/build/font-pack.8b60ca65f33929a11b34.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=86400`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
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

  
#### CWE Id : 16
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Evidence: `13db-/Bd8X2Z4YaHVtQjSbbs8TchmArY`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `9b68-0MVNzocgG0H+oUQzpgg6Hflj2W4`
  
  
  
  
* URL: [https://pad.incubateur.net/new](https://pad.incubateur.net/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWnp4HYPDNbn5rvyVSnxn7oMvVhwbhHHl`
  
  
  
  
* URL: [https://pad.incubateur.net/sitemap.xml](https://pad.incubateur.net/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWnp4HYPDNbn5rvyVSnxn7oMvVhwbhHHl`
  
  
  
  
* URL: [https://pad.incubateur.net/logout](https://pad.incubateur.net/logout)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWnp4HYPDNbn5rvyVSnxn7oMvVhwbhHHl`
  
  
  
  
* URL: [https://pad.incubateur.net/s/release-notes](https://pad.incubateur.net/s/release-notes)
  
  
  * Method: `GET`
  
  
  * Evidence: `e274-4t67ZKQtFtCsYinPi4Jm2mpwlOA`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `4114-TFdcDPZVUQPos7kyMXtqMYPKwy8`
  
  
  
  
* URL: [https://pad.incubateur.net/me/export](https://pad.incubateur.net/me/export)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWnp4HYPDNbn5rvyVSnxn7oMvVhwbhHHl`
  
  
  
  
* URL: [https://pad.incubateur.net/robots.txt](https://pad.incubateur.net/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWnp4HYPDNbn5rvyVSnxn7oMvVhwbhHHl`
  
  
  
  
* URL: [https://pad.incubateur.net](https://pad.incubateur.net)
  
  
  * Method: `GET`
  
  
  * Evidence: `401d-eana/gjmGvkk1uEHFXMzzjmJubs`
  
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Evidence: `401d-eana/gjmGvkk1uEHFXMzzjmJubs`
  
  
  
  
* URL: [https://pad.incubateur.net/me/delete/](https://pad.incubateur.net/me/delete/)
  
  
  * Method: `GET`
  
  
  * Evidence: `3AWnp4HYPDNbn5rvyVSnxn7oMvVhwbhHHl`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�w[��]�}�ᆇV�#I���7!�</p><p>�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### CSP: X-Content-Security-Policy
##### Informational (Medium)
  
  
  
  
#### Description
<p>The header X-Content-Security-Policy was found on this response. While it is a good sign that CSP is implemented to some degree the policy specified in this header has not been analyzed by ZAP. To ensure full support by modern browsers ensure that the Content-Security-Policy header is defined and attached to responses.</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-0caf76c9-3a7f-422d-9cb0-ca0e94de9d64' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: X-WebKit-CSP
##### Informational (Medium)
  
  
  
  
#### Description
<p>The header X-WebKit-CSP was found on this response. While it is a good sign that CSP is implemented to some degree the policy specified in this header has not been analyzed by ZAP. To ensure full support by modern browsers ensure that the Content-Security-Policy header is defined and attached to responses.</p>
  
  
  
* URL: [https://pad.incubateur.net/](https://pad.incubateur.net/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-WebKit-CSP`
  
  
  * Evidence: `default-src 'self'; script-src 'self' vimeo.com https://gist.github.com www.slideshare.net https://query.yahooapis.com 'unsafe-eval' https://disqus.com https://*.disqus.com https://*.disquscdn.com https://www.google-analytics.com 'nonce-0caf76c9-3a7f-422d-9cb0-ca0e94de9d64' 'sha256-81acLZNZISnyGYZrSuoYhpzwDTTxi7vC1YM4uNxqWaM='; img-src *; style-src 'self' 'unsafe-inline' https://github.githubassets.com https://*.disquscdn.com; font-src 'self' data: https://public.slidesharecdn.com https://*.disquscdn.com; object-src *; media-src *; child-src *; connect-src *`
  
  
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
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
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js](https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `where`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `FIXME`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js](https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `later`
  
  
  
  
* URL: [https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js](https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js](https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js](https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 10
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected 5 times, the first in the element starting with: "!function(e){var t={};function n(r){if(t[r])return t[r].exports;var i=t[r]={i:r,l:!1,exports:{}};return e[r].call(i.exports,i,i.", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/MathJax.js](https://pad.incubateur.net/build/MathJax/MathJax.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js](https://pad.incubateur.net/build/common.116b96cba39b7131b98f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+x+"'></a>`
  
  
  
  
* URL: [https://pad.incubateur.net/s/terms-of-use](https://pad.incubateur.net/s/terms-of-use)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="ui-edit" title="Edit this note"><i class="fa fa-fw fa-pencil"></i></a>`
  
  
  
  
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
  
  
  
  
* URL: [https://pad.incubateur.net/build/MathJax/config/Safe.js](https://pad.incubateur.net/build/MathJax/config/Safe.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script
 *    src="http://cdn.jsdelivr.net/npm/mathjax@2/MathJax.js?config=TeX-AMS_HTML,Safe">
 *  </script>`
  
  
  
  
* URL: [https://pad.incubateur.net/features](https://pad.incubateur.net/features)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="ui-short-status" data-toggle="dropdown"><span class="label label-danger"><i class="fa fa-plug"></i> </span>
            </a>`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js](https://pad.incubateur.net/build/cover-pack.192514c666b866e66682.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
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
  
  
  
* URL: [https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css](https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000000`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css](https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `33333333`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css](https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `80000000`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css](https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `42857143`
  
  
  
  
* URL: [https://pad.incubateur.net/new](https://pad.incubateur.net/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `79816759`
  
  
  
  
* URL: [https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css](https://pad.incubateur.net/build/cover-styles-pack.b807addb6d3e44422f27.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `66666667`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>00000000, which evaluates to: 1970-01-01 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

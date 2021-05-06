
# ZAP Scanning Report

Generated on Thu, 6 May 2021 00:32:46


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
| CSP: script-src unsafe-inline | Medium | 5 | 
| CSP: style-src unsafe-inline | Medium | 5 | 
| Reverse Tabnabbing | Medium | 3 | 
| Cookie Without Secure Flag | Low | 1 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 7 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Base64 Disclosure | Informational | 6 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 4 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 2 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/robots.txt](https://aplus.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/sitemap.xml](https://aplus.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/robots.txt](https://aplus.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/sitemap.xml](https://aplus.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `connect-src 'self'; base-uri 'none'; img-src 'self' data: stats.data.gouv.fr; form-action 'self'; frame-src 'self' https://www.dailymotion.com; style-src 'self' 'unsafe-inline' stats.data.gouv.fr; object-src 'none'; script-src 'self' 'unsafe-inline' stats.data.gouv.fr; default-src 'none'; font-src 'self'; frame-ancestors 'self'`
  
  
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="mdl-navigation__link aplus-color-text--black" href="https://docs.aplus.beta.gouv.fr/faq" target="_blank" rel="noopener"
                        >FAQ
                            <i class="material-icons">
                                open_in_new
                            </i></a
                        >`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="mdl-navigation__link aplus-color-text--black" href="https://docs.aplus.beta.gouv.fr/faq" target="_blank" rel="noopener"
                        >FAQ
                            <i class="material-icons">
                                open_in_new
                            </i></a
                        >`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="mdl-navigation__link aplus-color-text--black" href="https://docs.aplus.beta.gouv.fr/faq" target="_blank" rel="noopener"
                        >FAQ
                            <i class="material-icons">
                                open_in_new
                            </i></a
                        >`
  
  
  
  
Instances: 3
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `POST`
  
  
  * Parameter: `PLAY_FLASH`
  
  
  * Evidence: `Set-Cookie: PLAY_FLASH`
  
  
  
  
Instances: 1
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js](https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js)
  
  
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
  
  
  
* URL: [https://aplus.beta.gouv.fr/sitemap.xml](https://aplus.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/javascripts/00e6a5edf00321c7670836b9eb62c11a-main-page-bottom.js](https://aplus.beta.gouv.fr/assets/javascripts/00e6a5edf00321c7670836b9eb62c11a-main-page-bottom.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/robots.txt](https://aplus.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js](https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/material-design-lite/1.3.0/material.min.css](https://aplus.beta.gouv.fr/webjars/material-design-lite/1.3.0/material.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=3600`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/images/dae756ffe40acb0a9fb5429d5bd3275d-logo-marianne.svg](https://aplus.beta.gouv.fr/assets/images/dae756ffe40acb0a9fb5429d5bd3275d-logo-marianne.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000, immutable`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/roboto-fontface/0.10.0/css/roboto/roboto-fontface.css](https://aplus.beta.gouv.fr/webjars/roboto-fontface/0.10.0/css/roboto/roboto-fontface.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=3600`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/images/adf103d2a2763dc99455dce877c09c7c-pointbetagouvfr.svg](https://aplus.beta.gouv.fr/assets/images/adf103d2a2763dc99455dce877c09c7c-pointbetagouvfr.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000, immutable`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/stylesheets/517bbf2184aafd33b2616383ad2b9f36-home.css](https://aplus.beta.gouv.fr/assets/stylesheets/517bbf2184aafd33b2616383ad2b9f36-home.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000, immutable`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/material-design-icons/4.0.0/material-icons.css](https://aplus.beta.gouv.fr/webjars/material-design-icons/4.0.0/material-icons.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=3600`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/stylesheets/2657e81ade3f64e6a03e14b4d2ade850-mdl-extensions.css](https://aplus.beta.gouv.fr/assets/stylesheets/2657e81ade3f64e6a03e14b4d2ade850-mdl-extensions.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000, immutable`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/00b17e99d3b1b82d64e3b352f610d891-index.css](https://aplus.beta.gouv.fr/assets/generated-js/00b17e99d3b1b82d64e3b352f610d891-index.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000, immutable`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/stylesheets/79a46a707d26ff8dec1d6d5cea6abcd0-main.css](https://aplus.beta.gouv.fr/assets/stylesheets/79a46a707d26ff8dec1d6d5cea6abcd0-main.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=31536000, immutable`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/material-design-lite/1.3.0/material.min.css](https://aplus.beta.gouv.fr/webjars/material-design-lite/1.3.0/material.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `mdl-color-text--deep-purple-A100`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJkYXRhIjp7ImNzcmZUb2tlbiI6IjlkODliYjdmOWE0MjhiNDYxNzgwNmEyYjhjMjJlMjJlZjNmNzgyMjYtMTYyMDI2MTE1Mjc1OC0xMDZkYmY2NWVhMzUzYzkwNTc0ZTkxM2MifSwiZXhwIjoxNjIyODUzMTUyLCJuYmYiOjE2MjAyNjExNTIsImlhdCI6MTYyMDI2MTE1Mn0`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `POST`
  
  
  * Evidence: `eyJkYXRhIjp7ImVycm9yIjoiQXVjdW4gY29tcHRlIGFjdGlmIG7igJllc3QgYXNzb2Npw6kgw6AgY2V0dGUgYWRyZXNzZSBlLW1haWwuXG5NZXJjaSBkZSB2w6lyaWZpZXIgcXXigJlpbCBz4oCZYWdpdCBiaWVuIGRlIHZvdHJlIGFkcmVzc2UgcHJvZmVzc2lvbm5lbGxlIGV0IG5vbWluYXRpdmUuIiwiZW1haWwtdmFsdWUiOiJmb28tYmFyQGV4YW1wbGUuY29tIn0sIm5iZiI6MTYyMDI2MTE1NSwiaWF0IjoxNjIwMjYxMTU1fQ`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `/assets/images/home/cf2f205f4433b43d68faaed7c05ade80-Aplus-qu-est-ce-que-cest-mobile`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/assets/images/home/cf2f205f4433b43d68faaed7c05ade80-Aplus-qu-est-ce-que-cest-mobile`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJkYXRhIjp7ImNzcmZUb2tlbiI6IjcyYWQ4ZGE5ZGY4ZDc1NzYyZTE5NGI4YTlmMDIyMzkwZWJiNzBiZDQtMTYyMDI2MTE0OTkxMC1mY2JlODUxOTkxZjU3OGM0NjdlMGIyOTgifSwiZXhwIjoxNjIyODUzMTQ5LCJuYmYiOjE2MjAyNjExNDksImlhdCI6MTYyMDI2MTE0OX0`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��~r�h��^�߾u�����W�\x0003]4</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/javascripts/00e6a5edf00321c7670836b9eb62c11a-main-page-bottom.js](https://aplus.beta.gouv.fr/assets/javascripts/00e6a5edf00321c7670836b9eb62c11a-main-page-bottom.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js](https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/javascripts/00e6a5edf00321c7670836b9eb62c11a-main-page-bottom.js](https://aplus.beta.gouv.fr/assets/javascripts/00e6a5edf00321c7670836b9eb62c11a-main-page-bottom.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 10 times, the first in the element starting with: "// Area Change Select", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js](https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/login](https://aplus.beta.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><p><img src="//stats.data.gouv.fr/piwik.php?idsite=42" style="border: 0;" alt="" /></p></noscript>`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><p><img src="//stats.data.gouv.fr/piwik.php?idsite=42" style="border: 0;" alt="" /></p></noscript>`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript><p><img src="//stats.data.gouv.fr/piwik.php?idsite=42" style="border: 0;" alt="" /></p></noscript>`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/stylesheets/517bbf2184aafd33b2616383ad2b9f36-home.css](https://aplus.beta.gouv.fr/assets/stylesheets/517bbf2184aafd33b2616383ad2b9f36-home.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/stylesheets/2657e81ade3f64e6a03e14b4d2ade850-mdl-extensions.css](https://aplus.beta.gouv.fr/assets/stylesheets/2657e81ade3f64e6a03e14b4d2ade850-mdl-extensions.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/stylesheets/79a46a707d26ff8dec1d6d5cea6abcd0-main.css](https://aplus.beta.gouv.fr/assets/stylesheets/79a46a707d26ff8dec1d6d5cea6abcd0-main.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/sitemap.xml](https://aplus.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/material-design-lite/1.3.0/material.min.css](https://aplus.beta.gouv.fr/webjars/material-design-lite/1.3.0/material.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/material-design-icons/4.0.0/material-icons.css](https://aplus.beta.gouv.fr/webjars/material-design-icons/4.0.0/material-icons.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/](https://aplus.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/robots.txt](https://aplus.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr](https://aplus.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/images/bb24f2cd5ff2ee1dbcb59efcd02c83a8-favicon.png](https://aplus.beta.gouv.fr/assets/images/bb24f2cd5ff2ee1dbcb59efcd02c83a8-favicon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/webjars/roboto-fontface/0.10.0/css/roboto/roboto-fontface.css](https://aplus.beta.gouv.fr/webjars/roboto-fontface/0.10.0/css/roboto/roboto-fontface.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=3600`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js](https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `94906265`
  
  
  
  
* URL: [https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js](https://aplus.beta.gouv.fr/assets/generated-js/79fd3e8e7ae85113b2d86b51672342d0-index.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62425156`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>94906265, which evaluates to: 1973-01-03 10:51:05</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

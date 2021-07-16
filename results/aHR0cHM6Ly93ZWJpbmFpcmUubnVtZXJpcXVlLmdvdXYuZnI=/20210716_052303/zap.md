
# ZAP Scanning Report

Generated on Fri, 16 Jul 2021 05:18:21


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 1 | 
| Cookie without SameSite Attribute | Low | 3 | 
| Cookie Without Secure Flag | Low | 3 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 6 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 7 | 
| Timestamp Disclosure - Unix | Informational | 1 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.cnil.fr/vos-droits/vos-traces/les-cookies/" target="_blank" rel="noopener">http://www.cnil.fr/vos-droits/vos-traces/les-cookies/</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf_link" href="https://visio-agents.education.fr" target="_blank" rel="noopener">https://visio-agents.education.fr</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
Instances: 1
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 274 [https://authent.webinaire.numerique.gouv.fr/auth/realms/master/protocol/openid-connect/auth?client_id=BBB-Visio&response_type=code&scope=openid+email+profile&redirect_uri=https%3A%2F%2Fwebinaire.numerique.gouv.fr%2Foidc_callback&state=aOXmHgtlMarbAwkY&nonce=E1aBvP5mzkwchHkr].</p><p>Predicted response size: 574.</p><p>Response Body Length: 795.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 3
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2dl-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2dl-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-adm-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-adm-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/](https://webinaire.numerique.gouv.fr/static/misc/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/toc.css](https://webinaire.numerique.gouv.fr/static/css/toc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/images/favicon.png](https://webinaire.numerique.gouv.fr/static/images/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/global.css](https://webinaire.numerique.gouv.fr/static/css/global.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/nico3333fr/van11y-accessible-modal-window-aria/blob/master/LICENSE`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiOGQwYzBmYjU3MmZmNGRiNjlhMzBmYTVlMzQ0YWNlMTgwOTQzOTg1YyJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `eJwVjMFugzAQBf_F54iIGhPCrZUq5VIlx_aEFntNLLBN12uQWvXfa47vjWZ-hU5kB44zBtGLZrSmu6r68tIqaVF2YBvQIDt9NRdUCmvZNm0nxUnoTISBh5Xi5gxSsQ1ayAsXaDCxC8AuHtUn85r683nHsZyOsArZI7nvjNUU81ZZKmzR0WNxLcHkjzIGHQ2agTCtMSQUvYUl4UmEGHRZ4r2Gt-2h_M-86-dtpiInBj4Q3D_9beLlA2h83ecv8fcPAnZQcw`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Evidence: `eJwljt9LwzAQx_-VcM-j2-y6dX2RKcJeRJ9EUSnX5NKFpkm9pB1u7H83xafjvr_4XKHWFsOJAlSfVxAxHSBmz7X1rXGwgEc_MhuywrgJrVGUicNEFzH5MYjGkBMRh69xtaJ90iKToB6NFffibU4MfpzT_J-gEPCXOIPv2_cCZGBdR9-Rgwo2jVblvljv7rZFrikvUW9QYl7KvdpRUdA63262ZZ6QZCIiF-uB_ZSAOLUVaRxtTKaiEI3DaPy8eopxCNVyeaYmiYYpc2NPbH5GytqElmlOnpW-p9TVjG0_L5OTXpGqmcLgXSCoNNpAC3DeyfTB0xofpteiv3RneTp2nMohYpwtfHnvj220z8jN4dx9wO0PCGF7ng`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiNGJmZDg5NTE3MjY1M2ZlMzhhZjRhY2EzOGM5ZDdlNTVlMTM2NDY4MyJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `Creer_une_reunion_Improvisee_V5`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x0000\x0010�\x0010Q� ��0ӏA\x0014�QU�a��qן�\x0018��Y�����ۯ�\x001c��]�㞻�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "          // we remove content from its source to avoid id duplicates, etc.", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found with a target of '_self' - this is often used by modern frameworks to force a full page reload.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr](https://webinaire.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/](https://webinaire.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>23000091, which evaluates to: 1970-09-24 04:54:51</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

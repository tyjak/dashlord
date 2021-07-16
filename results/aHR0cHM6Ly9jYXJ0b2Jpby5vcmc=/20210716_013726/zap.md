
# ZAP Scanning Report

Generated on Fri, 16 Jul 2021 01:33:07


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 5 |
| Low | 8 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 10 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 3 | 
| Reverse Tabnabbing | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cookie without SameSite Attribute | Low | 12 | 
| Cookie Without Secure Flag | Low | 12 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Secure Pages Include Mixed Content | Low | 1 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 4 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Storable and Cacheable Content | Informational | 7 | 
| Storable but Non-Cacheable Content | Informational | 4 | 
| Timestamp Disclosure - Unix | Informational | 21 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4037315389283467`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4041066118585037`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4033867674246892`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4050288979639434`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4024736819860613`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4031626073178425`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4052802305431247`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4044814639477656`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4035738820163737`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `4020961302475083`
  
  
  
  
Instances: 10
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Visa</p><p>Bank Identification Number: 403731</p><p>Brand: VISA</p><p>Category: </p><p>Issuer: CITIBANK</p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://cartobio.org/api](https://cartobio.org/api)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/s/index.php?action=index&date=previous30&idSite=109&module=CoreHome&period=range](https://cartobio.org/s/index.php?action=index&date=previous30&idSite=109&module=CoreHome&period=range)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/api/notifications/](https://cartobio.org/api/notifications/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/](https://cartobio.org/geoserver/gwc/service/tms/)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://cartobio.org/api/notifications](https://cartobio.org/api/notifications)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif](https://cartobio.org/api/espacecollaboratif)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="m-social__link external-link" href="https://www.facebook.com/ignfr" target="_blank" title="Facebook IGN">
                                <span class="m-social__icon icon-facebook" aria-hidden="true"></span>
                                <p class="m-social__text">
                                    <span class="sr-only">Facebook IGN : </span>
                                    <span class="m-social__nb" id="facebook-followers">61K</span>
                                    abonnés
                                </p>
                                <span class="icon-external-link" aria-hidden="true"></span>
                            </a>`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://cartobio.org/georem/](https://cartobio.org/georem/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/georem-stats/](https://cartobio.org/georem-stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/georem/add](https://cartobio.org/georem/add)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/data/about](https://cartobio.org/data/about)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/api](https://cartobio.org/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/api/doc/georem](https://cartobio.org/api/doc/georem)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://cartobio.org/georem-api-clients](https://cartobio.org/georem-api-clients)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Material+Icons&display=swap" rel="stylesheet">`
  
  
  
  
Instances: 11
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/georem/](https://cartobio.org/georem/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/georem/add](https://cartobio.org/georem/add)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/georem-stats/](https://cartobio.org/georem-stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/georem-api-clients](https://cartobio.org/georem-api-clients)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/api](https://cartobio.org/api)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://cartobio.org/data/about](https://cartobio.org/data/about)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0](https://cartobio.org/geoserver/gwc/service/tms/1.0.0)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/](https://cartobio.org/geoserver/gwc/service/tms/)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/](https://cartobio.org/geoserver/gwc/service/tms/rest/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/](https://cartobio.org/geoserver/gwc/service/tms/rest/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/](https://cartobio.org/geoserver/gwc/service/tms/)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Parameter: `BIGipServerPOOL-IP-185-113-40-76.INFRA.CEGEDIM.ORG-HTTP`
  
  
  * Evidence: `Set-Cookie: BIGipServerPOOL-IP-185-113-40-76.INFRA.CEGEDIM.ORG-HTTP`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0](https://cartobio.org/geoserver/gwc/service/tms/1.0.0)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/](https://cartobio.org/geoserver/gwc/service/tms/rest/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/tms/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css](https://cartobio.org/geoserver/gwc/service/tms/rest/web/gwc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/rest/web/geowebcache_logo.png](https://cartobio.org/geoserver/gwc/service/rest/web/geowebcache_logo.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpgbio_)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/](https://cartobio.org/geoserver/gwc/service/tms/)
  
  
  * Method: `GET`
  
  
  * Parameter: `GS_FLOW_CONTROL`
  
  
  * Evidence: `Set-Cookie: GS_FLOW_CONTROL`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/](https://cartobio.org/geoserver/gwc/service/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:rpgbio_points_2019@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/api](https://cartobio.org/api)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0](https://cartobio.org/geoserver/gwc/service/tms/1.0.0)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/data/about](https://cartobio.org/data/about)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/](https://cartobio.org/geoserver/gwc/service/tms/1.0.0/cartobio:anon_rpg_2020@EPSG:900913@pbf/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0`
  
  
  
  
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
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/map~operator~prototypes.c193620f.js](https://cartobio.org/js/map~operator~prototypes.c193620f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-vendors.b9b448fd.js](https://cartobio.org/js/chunk-vendors.b9b448fd.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/operator.b1ebda6a.js](https://cartobio.org/js/operator.b1ebda6a.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/map.e001e650.js](https://cartobio.org/js/map.e001e650.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/app.efe4a7eb.js](https://cartobio.org/js/app.efe4a7eb.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/js/map~prototypes.77f17541.js](https://cartobio.org/js/map~prototypes.77f17541.js)
  
  
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

  
  
  
  
### Secure Pages Include Mixed Content
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes mixed content, that is content accessed via HTTP instead of HTTPS.</p>
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `http://piwik.ign.fr/piwik/piwik.php?idsite=36`
  
  
  
  
Instances: 1
  
### Solution
<p>A page that is available over SSL/TLS must be comprised completely of content which is transmitted over SSL/TLS.</p><p>The page must not contain any content that is transmitted over unencrypted HTTP.</p><p> This includes content from third party sites.</p>
  
### Other information
<p>tag=img src=http://piwik.ign.fr/piwik/piwik.php?idsite=36</p><p>tag=img src=http://piwik.ign.fr/piwik/piwik.php?idsite=36</p><p></p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Protection_Cheat_Sheet.html

  
#### CWE Id : 311
  
#### WASC Id : 4
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://cartobio.org/favicon-16x16.png](https://cartobio.org/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/favicon-32x32.png](https://cartobio.org/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/css/map~prototypes.8f485d92.css](https://cartobio.org/css/map~prototypes.8f485d92.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/css/prototypes.0c4c07ce.css](https://cartobio.org/css/prototypes.0c4c07ce.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/css/map.033a7d73.css](https://cartobio.org/css/map.033a7d73.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/css/operator.6fd4650a.css](https://cartobio.org/css/operator.6fd4650a.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://cartobio.org/apple-touch-icon.png](https://cartobio.org/apple-touch-icon.png)
  
  
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

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://cartobio.org/css/operator.6fd4650a.css](https://cartobio.org/css/operator.6fd4650a.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/css/map.033a7d73.css](https://cartobio.org/css/map.033a7d73.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/apple-touch-icon.png](https://cartobio.org/apple-touch-icon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/favicon-16x16.png](https://cartobio.org/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/css/prototypes.0c4c07ce.css](https://cartobio.org/css/prototypes.0c4c07ce.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/css/map~prototypes.8f485d92.css](https://cartobio.org/css/map~prototypes.8f485d92.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://cartobio.org/favicon-32x32.png](https://cartobio.org/favicon-32x32.png)
  
  
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
  
  
  
* URL: [https://cartobio.org/js/app.efe4a7eb.js](https://cartobio.org/js/app.efe4a7eb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/blog/2020/02/21/Nouvelles_ressources_RPG`
  
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `BIGipServerPOOL-IP-185-113-40-76`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `UklGRh4AAABXRUJQVlA4TBEAAAAvAQAAAAfQ//73v/+BiOh/AAA=`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `org/officeDocument/2006/docPropsVTypes`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>~�ۖ�?�M��M��_͢�ޖW�������q�?D�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://cartobio.org/js/app.efe4a7eb.js](https://cartobio.org/js/app.efe4a7eb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Admin`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-vendors.b9b448fd.js](https://cartobio.org/js/chunk-vendors.b9b448fd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-vendors.b9b448fd.js](https://cartobio.org/js/chunk-vendors.b9b448fd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-vendors.b9b448fd.js](https://cartobio.org/js/chunk-vendors.b9b448fd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://cartobio.org/js/prototypes.9ae631b9.js](https://cartobio.org/js/prototypes.9ae631b9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://cartobio.org/js/operator.b1ebda6a.js](https://cartobio.org/js/operator.b1ebda6a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-vendors.b9b448fd.js](https://cartobio.org/js/chunk-vendors.b9b448fd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `SELECT`
  
  
  
  
* URL: [https://cartobio.org/js/map.e001e650.js](https://cartobio.org/js/map.e001e650.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script type="text/javascript"></p><p>            /* web-application */</p><p>            if (!window.wapp) wapp = {};</p><p>                     ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://cartobio.org/api](https://cartobio.org/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/api/espacecollaboratif/](https://cartobio.org/api/espacecollaboratif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>
        <p>
            <img src="http://piwik.ign.fr/piwik/piwik.php?idsite=36" style="border:0;" alt="" />
        </p>
    </noscript>`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-vendors.b9b448fd.js](https://cartobio.org/js/chunk-vendors.b9b448fd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/georem/add](https://cartobio.org/georem/add)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/georem/](https://cartobio.org/georem/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/data/about](https://cartobio.org/data/about)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://cartobio.org/georem-api-clients](https://cartobio.org/georem-api-clients)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
    _paq.push(['setDomains', ['cartobio.org', 'www.cartobio.org']]);
    _paq.push(['enableLinkTracking']);
    _paq.push(['enableHeartBeatTimer', 15]);
    (function() {
      _paq.push(['setTrackerUrl', 'https://cartobio.org/s/']);
      _paq.push(['setSiteId', '116']);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.defer=true; g.src='omotam.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://cartobio.org/css/map.033a7d73.css](https://cartobio.org/css/map.033a7d73.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cartobio.org/favicon-32x32.png](https://cartobio.org/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://cartobio.org/css/map~prototypes.8f485d92.css](https://cartobio.org/css/map~prototypes.8f485d92.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cartobio.org/apple-touch-icon.png](https://cartobio.org/apple-touch-icon.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
* URL: [https://cartobio.org/css/prototypes.0c4c07ce.css](https://cartobio.org/css/prototypes.0c4c07ce.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cartobio.org/css/operator.6fd4650a.css](https://cartobio.org/css/operator.6fd4650a.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://cartobio.org/favicon-16x16.png](https://cartobio.org/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=2592000`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://cartobio.org/](https://cartobio.org/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/sitemap.xml](https://cartobio.org/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org](https://cartobio.org)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://cartobio.org/robots.txt](https://cartobio.org/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `252645135`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `461845907`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `77275007`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16711935`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `015873016`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `858993459`
  
  
  
  
* URL: [https://cartobio.org/css/operator.6fd4650a.css](https://cartobio.org/css/operator.6fd4650a.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `60788791`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777216`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `34094679`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `29549936`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `25002273`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1431655765`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435455`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777215`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `40075017`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `80029008`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1540483477`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `38636864`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `86367051`
  
  
  
  
* URL: [https://cartobio.org/js/chunk-2d22497b.38f4de6c.js](https://cartobio.org/js/chunk-2d22497b.38f4de6c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `81822308`
  
  
  
  
Instances: 21
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>252645135, which evaluates to: 1978-01-03 03:12:15</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

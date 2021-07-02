
# ZAP Scanning Report

Generated on Fri, 2 Jul 2021 02:17:45


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 3 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: Wildcard Directive | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 18 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 6 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 1 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 1 | 
| Non-Storable Content | Informational | 1 | 
| Storable and Cacheable Content | Informational | 4 | 

## Alert Detail


  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, img-src, connects-src, frame-src, frame-ancestors, font-src, media-src, prefetch-src, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `upgrade-insecure-requests; base-uri 'none'; object-src 'none'; script-src https://communaute.inclusion.beta.gouv.fr/logs/ https://communaute.inclusion.beta.gouv.fr/sidekiq/ https://communaute.inclusion.beta.gouv.fr/mini-profiler-resources/ https://aws1.discourse-cdn.com/standard20/assets/ https://aws1.discourse-cdn.com/standard20/brotli_asset/ https://communaute.inclusion.beta.gouv.fr/extra-locales/ https://dub2.discourse-cdn.com/standard20/highlight-js/ https://dub2.discourse-cdn.com/standard20/javascripts/ https://dub2.discourse-cdn.com/standard20/plugins/ https://dub2.discourse-cdn.com/standard20/theme-javascripts/ https://dub2.discourse-cdn.com/standard20/svg-sprite/ https://stats.data.gouv.fr/matomo.js https://stats.data.gouv.fr/piwik.php https://stats.data.gouv.fr/ http://communaute.inclusion.beta.gouv.fr/matomo.js http://communaute.inclusion.beta.gouv.fr/hotjar.js https://static.hotjar.com/ https://script.hotjar.com/; worker-src 'self' https://aws1.discourse-cdn.com/standard20/assets/ https://aws1.discourse-cdn.com/standard20/brotli_asset/ https://dub2.discourse-cdn.com/standard20/javascripts/ https://dub2.discourse-cdn.com/standard20/plugins/; manifest-src 'self'`
  
  
  
  
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
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_7_c20c5316b8cf86703b3a7b10c2b2861d7da8094b.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="7"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css2?family=Roboto&amp;display=swap" rel="stylesheet">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/ae1fab3e0022ed39b6a49dc7bdb7ac0982a91d10.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="apple-touch-icon" type="image/png" href="https://aws1.discourse-cdn.com/standard20/uploads/communauteinclusion/optimized/1X/a07679729a1e853552e36066838c0f0a9ed767f1_2_180x180.svg">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_12_b3c8a5b09738ff16426516722bf8f859f541085c.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="12"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_25_999cc67125edc13062a7521ad79ffb554d48109c.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="25"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_c6dbd7d34550956b881264118d2a20d87869906c.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop" data-theme-id="7"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_32_6e52529052f84781c39641cc22f0de07cc3617d2.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="32"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/0828be4560e695619a7505baa86c3068cf1c6bcb.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="preconnect" href="https://fonts.gstatic.com">`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_36_b7efedfc97f5746f0832c2854f543e78d002d75b.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="36"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_30_9915a97542877f90906770fff3e77b83edbfc846.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="30"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/2ca7fc2ca3915b958f7d0c41d55a877c8bb93d99.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/95d12c2d452939961609ccaf52169c4ef00a0573.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://dub2.discourse-cdn.com/standard20/stylesheets/desktop_theme_11_13bdbef6d2dd443e0c68ba27712d17ad242525b4.css?__ws=communaute.inclusion.beta.gouv.fr" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="11"/>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="icon" type="image/png" href="https://aws1.discourse-cdn.com/standard20/uploads/communauteinclusion/optimized/1X/a07679729a1e853552e36066838c0f0a9ed767f1_2_32x32.svg">`
  
  
  
  
Instances: 18
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/0828be4560e695619a7505baa86c3068cf1c6bcb.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/0828be4560e695619a7505baa86c3068cf1c6bcb.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/723ec67d0fa7134fc9afd3ff6fcbb434351336bc.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
* URL: [https://communaute.inclusion.beta.gouv.fr/](https://communaute.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/fe4db7dc8b8a38f2d064f967d5f307889c6b4a86.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
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
  
  
  * Parameter: `https://dub2.discourse-cdn.com/standard20/theme-javascripts/95d12c2d452939961609ccaf52169c4ef00a0573.js?__ws=communaute.inclusion.beta.gouv.fr`
  
  
  * Evidence: `<script src="https://dub2.discourse-cdn.com/standard20/theme-javascripts/95d12c2d452939961609ccaf52169c4ef00a0573.js?__ws=communaute.inclusion.beta.gouv.fr"></script>`
  
  
  
  
Instances: 6
  
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

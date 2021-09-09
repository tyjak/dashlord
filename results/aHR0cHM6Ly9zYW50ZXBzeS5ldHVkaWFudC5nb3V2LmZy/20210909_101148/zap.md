
# ZAP Scanning Report

Generated on Thu, 9 Sep 2021 09:55:06


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 1 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Permissions Policy Header Not Set | Low | 6 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 3 | 
| Non-Storable Content | Informational | 3 | 
| Storable but Non-Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 10 | 

## Alert Detail


  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ https://*.tile.openstreetmap.org/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/ 'sha256-4sJsjD6jok0r8RIemFeNZ1nEQfYv6qdzYIaUCTrSIhs=';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests;frame-src https://stats.santepsyetudiant.beta.gouv.fr;connect-src 'self' https://nominatim.openstreetmap.org https://stats.data.gouv.fr/`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/psychologue/login](https://santepsy.etudiant.gouv.fr/psychologue/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ https://*.tile.openstreetmap.org/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/ 'sha256-4sJsjD6jok0r8RIemFeNZ1nEQfYv6qdzYIaUCTrSIhs=';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests;frame-src https://stats.santepsyetudiant.beta.gouv.fr;connect-src 'self' https://nominatim.openstreetmap.org https://stats.data.gouv.fr/`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ https://*.tile.openstreetmap.org/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/ 'sha256-4sJsjD6jok0r8RIemFeNZ1nEQfYv6qdzYIaUCTrSIhs=';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests;frame-src https://stats.santepsyetudiant.beta.gouv.fr;connect-src 'self' https://nominatim.openstreetmap.org https://stats.data.gouv.fr/`
  
  
  
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, font-src, form-action</p><p></p><p>The directive(s): form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/psychologue/login](https://santepsy.etudiant.gouv.fr/psychologue/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ https://*.tile.openstreetmap.org/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/ 'sha256-4sJsjD6jok0r8RIemFeNZ1nEQfYv6qdzYIaUCTrSIhs=';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests;frame-src https://stats.santepsyetudiant.beta.gouv.fr;connect-src 'self' https://nominatim.openstreetmap.org https://stats.data.gouv.fr/`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ https://*.tile.openstreetmap.org/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/ 'sha256-4sJsjD6jok0r8RIemFeNZ1nEQfYv6qdzYIaUCTrSIhs=';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests;frame-src https://stats.santepsyetudiant.beta.gouv.fr;connect-src 'self' https://nominatim.openstreetmap.org https://stats.data.gouv.fr/`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ https://*.tile.openstreetmap.org/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/ 'sha256-4sJsjD6jok0r8RIemFeNZ1nEQfYv6qdzYIaUCTrSIhs=';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests;frame-src https://stats.santepsyetudiant.beta.gouv.fr;connect-src 'self' https://nominatim.openstreetmap.org https://stats.data.gouv.fr/`
  
  
  
  
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

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/psychologue/login](https://santepsy.etudiant.gouv.fr/psychologue/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.12af88c92ec34f862c84.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.12af88c92ec34f862c84.bundle.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.64f742ab032c99ac6d39.bundle.js](https://santepsy.etudiant.gouv.fr/main.64f742ab032c99ac6d39.bundle.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs=`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>GIF89a\x0001\x0000\x0001\x0000\x0000�\x0000,\x0000\x0000\x0000\x0000\x0001\x0000\x0001\x0000\x0000\x0002\x0000;</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.64f742ab032c99ac6d39.bundle.js](https://santepsy.etudiant.gouv.fr/main.64f742ab032c99ac6d39.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `User`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.c8eb1d5a3769a1b84206.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.c8eb1d5a3769a1b84206.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "!function(t,i){"object"==typeof exports&&"undefined"!=typeof module?i(exports):"function"==typeof define&&define.amd?define(["ex", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/psychologue/login](https://santepsy.etudiant.gouv.fr/psychologue/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    (function() {
      var u="https://stats.data.gouv.fr/";
      _paq.push(['setTrackerUrl', u+'matomo.php']);
      _paq.push(['setSiteId', 160]);
      _paq.push(['setCookieSameSite', 'None']);
      _paq.push(['setSecureCookie', true]);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.src=u+'matomo.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    (function() {
      var u="https://stats.data.gouv.fr/";
      _paq.push(['setTrackerUrl', u+'matomo.php']);
      _paq.push(['setSiteId', 160]);
      _paq.push(['setCookieSameSite', 'None']);
      _paq.push(['setSecureCookie', true]);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.src=u+'matomo.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>var _paq = window._paq || [];
    (function() {
      var u="https://stats.data.gouv.fr/";
      _paq.push(['setTrackerUrl', u+'matomo.php']);
      _paq.push(['setSiteId', 160]);
      _paq.push(['setCookieSameSite', 'None']);
      _paq.push(['setSecureCookie', true]);
      var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
      g.type='text/javascript'; g.async=true; g.src=u+'matomo.js'; s.parentNode.insertBefore(g,s);
    })();</script>`
  
  
  
  
Instances: 3
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/psychologue/login](https://santepsy.etudiant.gouv.fr/psychologue/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.css](https://santepsy.etudiant.gouv.fr/leaflet.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/favicon.ico](https://santepsy.etudiant.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.12af88c92ec34f862c84.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.12af88c92ec34f862c84.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.64f742ab032c99ac6d39.bundle.js](https://santepsy.etudiant.gouv.fr/main.64f742ab032c99ac6d39.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.css](https://santepsy.etudiant.gouv.fr/leaflet.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `70710678`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0511287798`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `314245179`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1631181422`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `40075017`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `18764656`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23592600`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15496570`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/leaflet.js](https://santepsy.etudiant.gouv.fr/leaflet.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `20037508`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `22503768`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>70710678, which evaluates to: 1972-03-29 09:51:18</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

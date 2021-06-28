
# ZAP Scanning Report

Generated on Mon, 28 Jun 2021 06:52:13


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 2 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 5 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 5 | 
| Storable and Cacheable Content | Informational | 6 | 
| Storable but Non-Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
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

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/main-93a70a8412f1441e111a.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/main-93a70a8412f1441e111a.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.7ccf6535708d32e9b4e3.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.7ccf6535708d32e9b4e3.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/14168061e2e69b09a39ac54666219dedbfc929ec.43f1a3cc959bba78ec33.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/14168061e2e69b09a39ac54666219dedbfc929ec.43f1a3cc959bba78ec33.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-2011279d6b235450b6a4.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-2011279d6b235450b6a4.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/48ee0394bfdc1ae6fe280bb9317f16cc73df2953.605a2bf360896cb01fcf.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/48ee0394bfdc1ae6fe280bb9317f16cc73df2953.605a2bf360896cb01fcf.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/ad7c8ed99411093b9ac9e15f715c4427ece2bd82.484002ccc937304fa9eb.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/ad7c8ed99411093b9ac9e15f715c4427ece2bd82.484002ccc937304fa9eb.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/29107295.ec38b7381592e291b989.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/29107295.ec38b7381592e291b989.js)
  
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/e07c76b2c0f68885c22b3ff40a89e9a22fa43b64.cbfb59e0d3943aa0dd4a.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/e07c76b2c0f68885c22b3ff40a89e9a22fa43b64.cbfb59e0d3943aa0dd4a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `f54-gEXM2+eQH4hplxfWoGYEzLlq3vU`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `150b-nt3PaavKrf2PC3TgVDkagdsurGc`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/eb7db5a47c9d27a5f4bdebd4be993084e9a7598f.8d7cfcd17cd941f69cf9.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/eb7db5a47c9d27a5f4bdebd4be993084e9a7598f.8d7cfcd17cd941f69cf9.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16h8v2H8zm0-4h8v2H8zm6-10H6c-1`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `150b-nt3PaavKrf2PC3TgVDkagdsurGc`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�x~����k��~o�hzW�v��z�l</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/14168061e2e69b09a39ac54666219dedbfc929ec.43f1a3cc959bba78ec33.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/14168061e2e69b09a39ac54666219dedbfc929ec.43f1a3cc959bba78ec33.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/main-93a70a8412f1441e111a.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/main-93a70a8412f1441e111a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/ad7c8ed99411093b9ac9e15f715c4427ece2bd82.484002ccc937304fa9eb.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/ad7c8ed99411093b9ac9e15f715c4427ece2bd82.484002ccc937304fa9eb.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/48ee0394bfdc1ae6fe280bb9317f16cc73df2953.605a2bf360896cb01fcf.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/48ee0394bfdc1ae6fe280bb9317f16cc73df2953.605a2bf360896cb01fcf.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/025009ad1d3c027e76559a2e365f000f911909d0.29b5fe0ba5b2715c3dc3.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/025009ad1d3c027e76559a2e365f000f911909d0.29b5fe0ba5b2715c3dc3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/6053359b2e69b9482ae72f9b165816c12fa82411.6f6530588627de8cbf55.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/6053359b2e69b9482ae72f9b165816c12fa82411.6f6530588627de8cbf55.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.7ccf6535708d32e9b4e3.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.7ccf6535708d32e9b4e3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/404","query":{},"buildId":"2yXvHijxRGaY0mb", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/404","query":{},"buildId":"2yXvHijxRGaY0mbmRGPqs","runtimeConfig":{"API_URL":"https://api.stargate.igloo.fabnum.fr/api"},"isFallback":false,"customServer":true,"appGip":true}</script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"2yXvHijxRGaY0mbmRGPqs","runtimeConfig":{"API_URL":"https://api.stargate.igloo.fabnum.fr/api"},"isFallback":false,"customServer":true,"appGip":true}</script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/404","query":{},"buildId":"2yXvHijxRGaY0mbmRGPqs","runtimeConfig":{"API_URL":"https://api.stargate.igloo.fabnum.fr/api"},"isFallback":false,"customServer":true,"appGip":true}</script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/polyfills-806d69b60a648b7a73e7.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/polyfills-806d69b60a648b7a73e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/main-93a70a8412f1441e111a.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/main-93a70a8412f1441e111a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/css/6ff37306c670ca78ffc0.css](https://stargate.igloo.fabnum.fr/_next/static/css/6ff37306c670ca78ffc0.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-2011279d6b235450b6a4.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-2011279d6b235450b6a4.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
Instances: 6
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/global.css](https://stargate.igloo.fabnum.fr/fonts/global.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff](https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff](https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff2](https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff2)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff2](https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff2)
  
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>29107295, which evaluates to: 1970-12-03 21:21:35</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

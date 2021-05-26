
# ZAP Scanning Report

Generated on Wed, 26 May 2021 03:48:00


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 6 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: style-src unsafe-inline | Medium | 4 | 
| CSP: Wildcard Directive | Medium | 4 | 
| CSP: Notices | Low | 4 | 
| Feature Policy Header Not Set | Low | 6 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 4 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 7 | 
| Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec) | Low | 7 | 
| X-Content-Type-Options Header Missing | Low | 7 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 4 | 
| Storable but Non-Cacheable Content | Informational | 7 | 
| Timestamp Disclosure - Unix | Informational | 15 | 

## Alert Detail


  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>form-action</p><p></p><p>The directive(s): form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
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

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>1:36: The block-all-mixed-content directive is an experimental directive that will be likely added to the CSP specification.</p><p>1:288: The upgrade-insecure-requests directive is an experimental directive that will be likely added to the CSP specification.</p><p></p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self';base-uri 'self';block-all-mixed-content;font-src 'self' https: data:;frame-ancestors 'self';img-src 'self' https://stats.data.gouv.fr/ data:;object-src 'none';script-src 'self' https://stats.data.gouv.fr/;script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests`
  
  
  
  
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

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js](https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/favicon.ico](https://santepsy.etudiant.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js](https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js](https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/favicon.ico](https://santepsy.etudiant.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/favicon.ico](https://santepsy.etudiant.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js](https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 7
  
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

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js](https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bXXX\b and was detected in the element starting with: "(self.webpackChunkreact_starter=self.webpackChunkreact_starter||[]).push([[216],{2122:(e,t,r)=>{"use strict";function n(){return", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="defer" src="/manifest.c87220ab61ee5d46a359.bundle.js"></script>`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="defer" src="/manifest.c87220ab61ee5d46a359.bundle.js"></script>`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="defer" src="/manifest.c87220ab61ee5d46a359.bundle.js"></script>`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="defer" src="/manifest.c87220ab61ee5d46a359.bundle.js"></script>`
  
  
  
  
Instances: 4
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/favicon.ico](https://santepsy.etudiant.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js](https://santepsy.etudiant.gouv.fr/manifest.c87220ab61ee5d46a359.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js](https://santepsy.etudiant.gouv.fr/main.e973f9d2b7ea55c3d04f.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/](https://santepsy.etudiant.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr](https://santepsy.etudiant.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741825`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741824`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `805306368`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/sitemap.xml](https://santepsy.etudiant.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1622001103`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/robots.txt](https://santepsy.etudiant.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1622001068`
  
  
  
  
* URL: [https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js](https://santepsy.etudiant.gouv.fr/vendors.15aff07c386d7ce05763.bundle.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
Instances: 15
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0123456789, which evaluates to: 1973-11-29 21:33:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Mon, 14 Jun 2021 04:36:39


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 5 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| CSP: script-src unsafe-inline | Medium | 2 | 
| CSP: style-src unsafe-inline | Medium | 2 | 
| CSP: Wildcard Directive | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 7 | 
| Cookie Without SameSite Attribute | Low | 10 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| CSP: Notices | Informational | 2 | 
| Information Disclosure - Suspicious Comments | Informational | 1 | 
| Modern Web Application | Informational | 5 | 
| Non-Storable Content | Informational | 6 | 
| Storable and Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 12 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/favicon.ico](https://www.rdv-solidarites.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/omniauth/franceconnect](https://www.rdv-solidarites.fr/omniauth/franceconnect)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users](https://www.rdv-solidarites.fr/users)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_up](https://www.rdv-solidarites.fr/users/sign_up)
  
  
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

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/stats](https://www.rdv-solidarites.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `POST`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/agents/sign_in](https://www.rdv-solidarites.fr/agents/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/mds](https://www.rdv-solidarites.fr/mds)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/organisations/new](https://www.rdv-solidarites.fr/organisations/new)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_lapin_session`
  
  
  * Evidence: `Set-Cookie: _lapin_session`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js](https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/mds](https://www.rdv-solidarites.fr/mds)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/omniauth/franceconnect](https://www.rdv-solidarites.fr/omniauth/franceconnect)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/stats](https://www.rdv-solidarites.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/agents/sign_in](https://www.rdv-solidarites.fr/agents/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js](https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/organisations/new](https://www.rdv-solidarites.fr/organisations/new)
  
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/css/application-05ce0c89.css](https://www.rdv-solidarites.fr/packs/css/application-05ce0c89.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/robots.txt](https://www.rdv-solidarites.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/mds](https://www.rdv-solidarites.fr/mds)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/welcome/location-06907703397aa504d21ad0f6bd8d1daa.svg](https://www.rdv-solidarites.fr/packs/media/images/welcome/location-06907703397aa504d21ad0f6bd8d1daa.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/stats](https://www.rdv-solidarites.fr/stats)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/logos/logo-f5be109ad11920d0bb655368a542296b.svg](https://www.rdv-solidarites.fr/packs/media/images/logos/logo-f5be109ad11920d0bb655368a542296b.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/welcome/location-06907703397aa504d21ad0f6bd8d1daa.svg](https://www.rdv-solidarites.fr/packs/media/images/welcome/location-06907703397aa504d21ad0f6bd8d1daa.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js](https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-16x16-764f9dc6cee7d41d0e7e4f762b2c9c7d.png](https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-16x16-764f9dc6cee7d41d0e7e4f762b2c9c7d.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-93a56fb828635ea14e7b9a7771f59f27.ico](https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-93a56fb828635ea14e7b9a7771f59f27.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-32x32-c752017713fef76c08c49481fb078516.png](https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-32x32-c752017713fef76c08c49481fb078516.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/css/application-05ce0c89.css](https://www.rdv-solidarites.fr/packs/css/application-05ce0c89.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/welcome/service-efb33e620a53f582c6ac3aa9854bce25.svg](https://www.rdv-solidarites.fr/packs/media/images/welcome/service-efb33e620a53f582c6ac3aa9854bce25.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/robots.txt](https://www.rdv-solidarites.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/welcome/motif-41619024745244c70dd39f0b86632aae.svg](https://www.rdv-solidarites.fr/packs/media/images/welcome/motif-41619024745244c70dd39f0b86632aae.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/welcome/creneau-3ee22592805cf19808328546b1baa129.svg](https://www.rdv-solidarites.fr/packs/media/images/welcome/creneau-3ee22592805cf19808328546b1baa129.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/logos/logo-f5be109ad11920d0bb655368a542296b.svg](https://www.rdv-solidarites.fr/packs/media/images/logos/logo-f5be109ad11920d0bb655368a542296b.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/apple-touch-icon-c4d0d633e092edb358ce3fc357105bc9.png](https://www.rdv-solidarites.fr/packs/media/images/favicon/apple-touch-icon-c4d0d633e092edb358ce3fc357105bc9.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/mds](https://www.rdv-solidarites.fr/mds)
  
  
  * Method: `GET`
  
  
  * Evidence: `iTQDD5vaBVxQfsdwlC5TOo3VDcH8xjdSJELChc4j4n7JtO6sttKcRqS1adN0ASmz5wAr96CTYokQQQ1kSyjp2eSg9GW1Q0yMsR3vpWbGabTf9vVnRwPwUWz4`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FOQGeWrzf36i4jLWNqavRW7QmL6wIG2kjH7jynMmrCtyzY1uvn`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BkFFQtrptnnHUxeUMPbjvIigmtR0zfQ5oh`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js](https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/css/application-05ce0c89.css](https://www.rdv-solidarites.fr/packs/css/application-05ce0c89.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAAGQAAAAeCAYAAADaW7vzAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6Q0NBRjI1NjM0M0UwMTFFNDk4NkFGMzJFQkQzQjEwRUIiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6Q0NBRjI1NjQ0M0UwMTFFNDk4NkFGMzJFQkQzQjEwRUIiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDpDQ0FGMjU2MTQzRTAxMUU0OTg2QUYzMkVCRDNCMTBFQiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDpDQ0FGMjU2MjQzRTAxMUU0OTg2QUYzMkVCRDNCMTBFQiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PoNEP54AAAIOSURBVHja7Jq9TsMwEMcxrZD4WpBYeKUCe+kTMCACHZh4BFfHO/AAIHZGFhYkBBsSEqxsLCAgXKhbXYOTxh9pfJVP+qutnZ5s/5Lz2Y5I03QhWji2GIcgAokWgfCxNvcOCCGKqiSqhUp0laHOne05vdEyGMfkdxJDVjgwDlEQgYQBgx+ULJaWSXXS6r/ER5FBVR8VfGftTKcITNs+a1XpcFoExREIDF14AVIFxgQUS+h520cdud6wNkC0UBw6BCO/HoCYwBhD8QCkQ/x1mwDyD4plh4D6DDV0TAGyo4HcawLIBBSLDkHeH0Mg2yVP3l4TQMZQDDsEOl/MgHQqhMNuE0D+oBh0CIr8MAKyazBH9WyBuKxDWgbXfjNf32TZ1KWm/Ap1oSk/R53UtQ5xTh3LUlMmT8gt6g51Q9p+SobxgJQ/qmsfZhWywGFSl0yBjCLJCMgXail3b7+rumdVJ2YRss4cN+r6qAHDkPWjPjdJCF4n9RmAD/V9A/Wp4NQassDjwlB6XBiCxcJQWmZZb8THFilfy/lfrTvLghq2TqTHrRMTKNJ0sIhdo15RT+RpyWwFdY96UZ/LdQKBGjcXpcc1AlSFEfLmouD+1knuxBDUVrvOBmoOC/rEcN7OQxKVeJTCiAdUzUJhA2Oez9QTkp72OTVcxDcXY8iKNkxGAJXmJCOQwOa6dhyXsOa6XwEGAKdeb5ET3rQdAAAAAElFTkSuQmCC`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `2B9IFg3IrkqU07KZIHZVx0a73LVb7qP`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `h4AO18UtaBgq5CyzbhCvrKXhFiCZuTYt`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FShM5Op8LA7NMb3f2GJApteZioExlmhH3SFLkZaK71LlK0FRs8ZwMtv18soP36CxYq5VTNABeemaNVzPYe0esE9yk9u`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/stats](https://www.rdv-solidarites.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FrZ5mJ7fp1l78MEG97ZcJekqy9uh5L3Mdz8CMvXhuWapR47SPfRjQRhSlAAgiCfmMebykWHmPiQiLkc2Hv8On534vOUna`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BZpFONQ5BUcDg3kWYfAPrwSgC3F6BV`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `POST`
  
  
  * Evidence: `2F0aIN9djn6cDR1HuaOZ5RQTKjFiQmFfoBSuKA1`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `bYbHoiFy8lyAawiwtdDffP86GaRgZMSyT3GlEQFG`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�4\x0003\x000f��\x0005\P~�p�.S:��
���7R$B�#�~ɴҜF��i�t\x0001)��\x0000+���b�\x0010A
dK(����e�CL��\x001d�f�i����gG\x0003�Ql�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Informational (Medium)
  
  
  
  
#### Description
<p>Info Items:</p><p>1:509: A draft of the next version of CSP deprecates report-uri in favour of a new report-to directive.</p><p></p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'self'; font-src 'self' data: github.com; img-src 'self' data: stats.data.gouv.fr voxusagers.numerique.gouv.fr; object-src 'none'; style-src 'self' 'unsafe-inline' *.bootstrapcdn.com cdnjs.cloudflare.com api.mapbox.com; script-src 'self' 'unsafe-inline' stats.data.gouv.fr api-adresse.data.gouv.fr data1.ollapges.com fidoapi.com data1.gryplex.com lb.apicit.net tags.clickintext.net api.mapbox.com blob:; connect-src 'self' api-adresse.data.gouv.fr sentry.io cdnjs.cloudflare.com etalab-tiles.fr; report-uri https://o320280.ingest.sentry.io/api/1811205/security/?sentry_key=9483c31bc6f442ba8aa0ed3869608da0`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Other information
<p>The response contained multiple CSP headers, one or more of them contained a report-uri directive and therefore they could not be merged. The first identified header/policy was analyzed.</p>
  
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
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js](https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bBUG\b and was detected in the element starting with: "!function(t){var e={};function n(r){if(e[r])return e[r].exports;var o=e[r]={i:r,l:!1,exports:{}};return t[r].call(o.exports,o,o.", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/agents/sign_in](https://www.rdv-solidarites.fr/agents/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a class="close" data-dismiss="alert" href="#"><i class="fa fa-times"></i></a>`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js](https://www.rdv-solidarites.fr/packs/js/application-8cc4da9fc9e1bc6a9a7a.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+b+"'></a>`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/organisations/new](https://www.rdv-solidarites.fr/organisations/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="close" data-dismiss="alert" href="#"><i class="fa fa-times"></i></a>`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/agents/sign_in](https://www.rdv-solidarites.fr/agents/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="close" data-dismiss="alert" href="#"><i class="fa fa-times"></i></a>`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a class="close" data-dismiss="alert" href="#"><i class="fa fa-times"></i></a>`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/mds](https://www.rdv-solidarites.fr/mds)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/sitemap.xml](https://www.rdv-solidarites.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/apple-touch-icon-c4d0d633e092edb358ce3fc357105bc9.png](https://www.rdv-solidarites.fr/packs/media/images/favicon/apple-touch-icon-c4d0d633e092edb358ce3fc357105bc9.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-16x16-764f9dc6cee7d41d0e7e4f762b2c9c7d.png](https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-16x16-764f9dc6cee7d41d0e7e4f762b2c9c7d.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-32x32-c752017713fef76c08c49481fb078516.png](https://www.rdv-solidarites.fr/packs/media/images/favicon/favicon-32x32-c752017713fef76c08c49481fb078516.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/robots.txt](https://www.rdv-solidarites.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0296608686`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0134253030`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0322718080`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0329803234`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr](https://www.rdv-solidarites.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `2106102022`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0806000092`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0164147777`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/](https://www.rdv-solidarites.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2106102022`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/users/sign_in](https://www.rdv-solidarites.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `2106102022`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/accueil_mds](https://www.rdv-solidarites.fr/accueil_mds)
  
  
  * Method: `GET`
  
  
  * Evidence: `2106102022`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `0559693411`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/contact](https://www.rdv-solidarites.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `2106102022`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0296608686, which evaluates to: 1979-05-26 23:18:06</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `support_ticket[city]`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `support_ticket[email]`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `support_ticket[first_name]`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `support_ticket[last_name]`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `support_ticket[departement]`
  
  
  
  
* URL: [https://www.rdv-solidarites.fr/support_tickets](https://www.rdv-solidarites.fr/support_tickets)
  
  
  * Method: `POST`
  
  
  * Parameter: `support_ticket[subject]`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.rdv-solidarites.fr/support_tickets</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>support_ticket[city]=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

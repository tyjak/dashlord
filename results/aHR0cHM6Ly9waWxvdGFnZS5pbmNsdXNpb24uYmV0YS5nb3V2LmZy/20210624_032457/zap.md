
# ZAP Scanning Report

Generated on Thu, 24 Jun 2021 03:20:58


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 4 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: script-src unsafe-inline | Medium | 4 | 
| CSP: Wildcard Directive | Medium | 4 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| CSP: Notices | Low | 4 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 17 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-Iz1AcUlLZ7q5baHtHtoUfA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-ki6S0/hPWvfmhqEvgN+69Q' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-2ptQtnC1khuii1AQABacnA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-bYep3dGb8qj7kt4/thx/OQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, img-src, connects-src, frame-src, font-src, media-src, manifest-src, prefetch-src, form-action</p><p></p><p>The directive(s): form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-bYep3dGb8qj7kt4/thx/OQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-2ptQtnC1khuii1AQABacnA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-Iz1AcUlLZ7q5baHtHtoUfA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-ki6S0/hPWvfmhqEvgN+69Q' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb52](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb52)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb54](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb54)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Finclusion.beta.gouv.fr&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNFZVSeBPwerNSN1fBx4rasnnX0HCw" target="_blank">La plateforme de l&#39;inclusion</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="XqQF9c" href="https://www.google.com/url?q=https%3A%2F%2Fforum.inclusion.beta.gouv.fr%2Fc%2Fse-retrouver-par-territoire%2Fseine-saint-denis-93%2F54&amp;sa=D&amp;sntz=1&amp;usg=AFQjCNGLB_cb36r-eCOolkYAoEGcvie06Q" target="_blank">ici</a>`
  
  
  
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="2ptQtnC1khuii1AQABacnA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://www.gstatic.com/_/atari/_/ss/k=atari.vw.C7hxTR4DjR0.L.W.O/d=1/rs=AGEqA5kRg3nL0A1UsdO9SxLAawZTmsFbBA" nonce="NtIiS/hDhNGxDly2SRn6rA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Arvo%3A400%2C700%7CLato%3A400%2C700&display=swap" rel="stylesheet" nonce="Zd2qPWmuf2TeDLklsKIC7g">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Arvo%3A400%2C700%7CLato%3A400%2C700&display=swap" rel="stylesheet" nonce="NtIiS/hDhNGxDly2SRn6rA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="2ptQtnC1khuii1AQABacnA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="icon" href="https://lh4.googleusercontent.com/S4-u3UrnYgr8BDV1IXP3GBN5wtCHiETwz4y3PsiIf4ul6XfN6hu_q7-r1GZr5-QRWM4Yys2-Wn9xmnCDz1nIaQQJrU4pgq2quFwQOpj7B_tK8Q">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="icon" href="https://lh4.googleusercontent.com/S4-u3UrnYgr8BDV1IXP3GBN5wtCHiETwz4y3PsiIf4ul6XfN6hu_q7-r1GZr5-QRWM4Yys2-Wn9xmnCDz1nIaQQJrU4pgq2quFwQOpj7B_tK8Q">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="Iz1AcUlLZ7q5baHtHtoUfA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Google+Sans:400,500|Roboto:300,400,500,700|Source+Code+Pro:400,700&display=swap" rel="stylesheet" nonce="NtIiS/hDhNGxDly2SRn6rA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Google+Sans:400,500|Roboto:300,400,500,700|Source+Code+Pro:400,700&display=swap" rel="stylesheet" nonce="Zd2qPWmuf2TeDLklsKIC7g">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://www.gstatic.com/_/atari/_/ss/k=atari.vw.B1U9f3yUaRk.L.F4.O/d=1/rs=AGEqA5mUw3qgqDCoDO7xRzY8crNAabNojQ" nonce="Zd2qPWmuf2TeDLklsKIC7g">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="Iz1AcUlLZ7q5baHtHtoUfA"></script>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="ki6S0/hPWvfmhqEvgN+69Q"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="2ptQtnC1khuii1AQABacnA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="bYep3dGb8qj7kt4/thx/OQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="dmIETXzVX/G2WzCh8xfxaQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="Iz1AcUlLZ7q5baHtHtoUfA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="dmIETXzVX/G2WzCh8xfxaQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="aQNQ/rzpiICFyTJci++/xw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="ki6S0/hPWvfmhqEvgN+69Q"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="bYep3dGb8qj7kt4/thx/OQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="2ptQtnC1khuii1AQABacnA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.JhFF570cUkM.O/d=1/rs=AGEqA5lW8sbPCEax-o8MCVRJjWiZz904Tw/m=view" id="base-js" nonce="aQNQ/rzpiICFyTJci++/xw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="Iz1AcUlLZ7q5baHtHtoUfA"></script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>The report-uri directive has ben deprecated in favor of the new report-to directive</p><p></p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-Iz1AcUlLZ7q5baHtHtoUfA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-2ptQtnC1khuii1AQABacnA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-bYep3dGb8qj7kt4/thx/OQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-ki6S0/hPWvfmhqEvgN+69Q' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL1sB9LEmKO8HYhl5lUxf6OCT82vx_0cj2uY8mY1zGT5xP2P8Br3BflWo1FcS6H9GCx5nHTa`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0F1vU-e7xJOLwjyFLF2p8cT5Oe5ExLyo5pu0AXehaa3dmPuEiWZlgp2D4hgbUad5yyeNU-`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL1Xg98fkLYiEnWWrHRA4376OPpuiywYZDaMkgWtt78Ole83SxYt0b48qe3tjUaYka7Qj9QB`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL3a_ASzYhVtIITl7u30L6Vjy5aPEVLIDBjUOzjVd-5ZhjLZWcRzuEkmQqQepKNM2iNtfAqP`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL1xcr3YXFQFIFlhwv_AM4YkS79CloGC9DQ9chVpPNfMj-itpnjlAmAxqCrzZBFmowjX0SXc`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL2q_y-qz--TiceD3VjggKQpAcjGGZ3jVqb8Xz2nPUo1-eC-EsjfCW84IFDBQ-QS9BwIbFaS`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL2d7VVwgnVaErmBE7Kzg4FvfOlpsSvk1P8Oyaw6pTgGCQBNd5Bi4R3ZE0LPsPTCTN4t4n0r`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0-8Fpe6kulKG3qM1Ob1VNGsKgOMcnWQ46BeZj8GKoh_lUFHNy7HVZgzo7JQWtp7PW-jpD4`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0OKHHsDIRbL7Tcc3usHi3tWdJtkeYhgpjU5XmkV5rJjWRHNOHeHhcclnIFBeuVnsNEtrti`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL39y3YLpoRbS6FRf9I9wtzJt6sqMjpDqKANW5hDZDMclSRiisSxJwbqqAUhQYNE3AtJwDMQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0dUR5FSDPeMjNwzWZEQ8W5Dt2dYu8D0WvN3RGf5Mtp1tFDJ9XzpgOY905geTFDVN3nNNJW`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL2tpknPOI5v3eUCqVV_vESz9jMRni9Y7RDAakIa7SZLJ9Sw5aB-ZTOSl-nq8dxIyybA-rSf`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x0000r���l\x0007�Ę��\x001d�e�U1��Oͯ��\x001c�k��f5�d�����\x001a�\x0005�V�Q\K��\x0018,y�t�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="aJHbb dk90Ob jgXgSe HlqNPb" jsname="QwLHlb" role="link" tabindex="0" aria-expanded="false" aria-haspopup="true" title="More" jsaction="keydown:mPuKz; click:vHQTA;" data-level="1">More</a>`
  
  
  
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 11
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000009411`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000004706`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `380239050`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101462`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101530`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101502`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `150000006`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1174377224`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1915097782`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14100834`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `687544355`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101046`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000002353`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101534`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101550`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1000000015`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101510`
  
  
  
  
Instances: 17
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0000009411, which evaluates to: 1970-01-01 02:36:51</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

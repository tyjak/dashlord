
# ZAP Scanning Report

Generated on Sat, 15 May 2021 02:39:26


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 4 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: Wildcard Directive | Medium | 6 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| CSP: Notices | Low | 6 | 
| Feature Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 17 | 

## Alert Detail


  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>style-src, style-src-elem, style-src-attr, img-src, connect-src, frame-src, font-src, media-src, manifest-src, prefetch-src, form-action</p><p></p><p>The directive(s): form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-NY5sUwebjGxyGjs/Ru3Hfw' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-WTXgC2TOlTPiYb+j++/bJQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-UOeHJK+93OA3gCrMb+SyqA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-f0FXdfThVEDM0JIRmMiHaw' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-S+qq6BhFvsowXgcAAzQdZQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-3v1aR1xHLA/7+BpCDm6jzw' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
Instances: 6
  
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
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="3v1aR1xHLA/7+BpCDm6jzw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Google+Sans:400,500|Roboto:300,400,500,700|Source+Code+Pro:400,700&display=swap" rel="stylesheet" nonce="WuE1PzXjHKQ4EX35ccs06A">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="icon" href="https://lh4.googleusercontent.com/aq6lQ-Sdw7A6_xL27DmgiDmofKGgTYHrA2AnhtmOCzE2k5FJeRfiMSyxqDW7m7LQxm51yYeesHD1NH-3ioZiQ2uyq67WnmdmlxEFDSWGFPacyA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Arvo%3A400%2C700%7CLato%3A400%2C700&display=swap" rel="stylesheet" nonce="WuE1PzXjHKQ4EX35ccs06A">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Arvo%3A400%2C700%7CLato%3A400%2C700&display=swap" rel="stylesheet" nonce="bg3jgqxthWNkajGrDzxpdA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="WTXgC2TOlTPiYb+j++/bJQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="icon" href="https://lh4.googleusercontent.com/aq6lQ-Sdw7A6_xL27DmgiDmofKGgTYHrA2AnhtmOCzE2k5FJeRfiMSyxqDW7m7LQxm51yYeesHD1NH-3ioZiQ2uyq67WnmdmlxEFDSWGFPacyA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://www.gstatic.com/_/atari/_/ss/k=atari.vw.ld0B4kLqRG8.L.W.O/d=1/rs=AGEqA5l49BPmmKO1lK2QxDs5OY65zkw-3Q" nonce="bg3jgqxthWNkajGrDzxpdA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="3v1aR1xHLA/7+BpCDm6jzw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" href="https://www.gstatic.com/_/atari/_/ss/k=atari.vw.JaYIY8cU64g.L.F4.O/d=1/rs=AGEqA5mTMWlaCH5rW7SSOr48WkoGl8LxfA" nonce="WuE1PzXjHKQ4EX35ccs06A">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://fonts.googleapis.com/css?family=Google+Sans:400,500|Roboto:300,400,500,700|Source+Code+Pro:400,700&display=swap" rel="stylesheet" nonce="bg3jgqxthWNkajGrDzxpdA">`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="WTXgC2TOlTPiYb+j++/bJQ"></script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="f0FXdfThVEDM0JIRmMiHaw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="NY5sUwebjGxyGjs/Ru3Hfw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="NY5sUwebjGxyGjs/Ru3Hfw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="f0FXdfThVEDM0JIRmMiHaw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="S+qq6BhFvsowXgcAAzQdZQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="UOeHJK+93OA3gCrMb+SyqA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="WTXgC2TOlTPiYb+j++/bJQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="UOeHJK+93OA3gCrMb+SyqA"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://apis.google.com/js/client.js?onload=gapiLoaded`
  
  
  * Evidence: `<script src="https://apis.google.com/js/client.js?onload=gapiLoaded" nonce="3v1aR1xHLA/7+BpCDm6jzw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="3v1aR1xHLA/7+BpCDm6jzw"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="S+qq6BhFvsowXgcAAzQdZQ"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view`
  
  
  * Evidence: `<script src="https://www.gstatic.com/_/atari/_/js/k=atari.vw.en_US.UdNwq5nKlzQ.O/d=1/rs=AGEqA5km3GEOx8LYKQVaSaSIHUiChaasVg/m=view" id="base-js" nonce="WTXgC2TOlTPiYb+j++/bJQ"></script>`
  
  
  
  
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
<p>Warnings:</p><p>1:75: Invalid base64-value (should be multiple of 4 bytes: 22).</p><p>Info Items:</p><p>1:35: A draft of the next version of CSP deprecates report-uri in favour of a new report-to directive.</p><p>1:106: The "'unsafe-inline'" keyword-source has no effect in source lists that contain hash-source or nonce-source in CSP2 and later. Ensure that this pattern is only used for backwards compatibility with older CSP implementations and is not an oversight.</p><p></p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-f0FXdfThVEDM0JIRmMiHaw' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-S+qq6BhFvsowXgcAAzQdZQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-WTXgC2TOlTPiYb+j++/bJQ' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-UOeHJK+93OA3gCrMb+SyqA' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-3v1aR1xHLA/7+BpCDm6jzw' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `base-uri 'self';object-src 'none';report-uri /_/view/cspreport;script-src 'nonce-NY5sUwebjGxyGjs/Ru3Hfw' 'unsafe-inline' 'unsafe-eval';worker-src 'self';frame-ancestors https://google-admin.corp.google.com/`
  
  
  
  
Instances: 6
  
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

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL3Q7BW--pLN9C68VpRHCqkFS8D_gVMe-uSIhcu-kyAhkyRlyB1BsWD6nehY5VlxK67qxbxK`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0Zvkeaix_ZYuIFqHoAlIm-prbzDRNfEtY6djOMnktOHqmQdGAOaPF9fm8qjB5x35qEXHO3`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation](https://pilotage.inclusion.beta.gouv.fr/exp%C3%A9rimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0kY2zq_HaEi_V4mrsAlsUiBzf4Uo6S5Q_ZZsq35hY223IOhv-bJhbSfyPB9Gxj3XmH3mU9`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL1agao5qLFEnnslWP6nK2aQl5h01hQzKmF3PEoO1iXzJYAVj_cTgSOescBkmFGVDakN1EoJ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/accueil](https://pilotage.inclusion.beta.gouv.fr/accueil)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0FMelMIv7D4iBrhIOfxmeh29NABQhI_6BpLBNKsvYQmwfelaHX2-jAdMQMsVHj5uotYfQm`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sabonner](https://pilotage.inclusion.beta.gouv.fr/sabonner)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL0_Yn59s76BWaWGomw2ufgRv9CkBj4akpjK_MMeeZs5sNzGdUgJUw9qAEHzRbpOhMSz9E9m`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL12b5G9tGB9RBRVY-kSyTh84whp0f9rXEqpVCjUX-ob7cts3jTF3FK8uSGvx5Re5scJ1tH-`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL2M88C3HW1oNHvS5-pfZQ2EL-hwDQdSeXYBvskyUTRITO3-0rSequO79vqC36sCTI5IZLm_`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb32)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL209OAow-fo1CEZdHGyxNnEF5UgMeMTgtOjEp1z8djjJt2Cq5LGx0oAmbZ5KdGDu1vHxE4W`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL2H7L9TMhJXVZqRRwSVFxq9O38AqnDar7ORFNcu0E_tMotFhbY4EeShUrJZnNXm2gUo_693`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL2VnjU6yNnglrkzRW1KfI4qpbNUhnETErQAENBKnIDWAOEZB0_cnZKtQRCIF_iL74eBiI70`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/tb90)
  
  
  * Method: `GET`
  
  
  * Evidence: `AHKXmL3fNZBl5QEVAZUzPR0aARzhuGUVFMwzM8EWsqq-AXk9PRkq6n5Umk_bmf9gYENqyOq_uKrY`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>\x0000r�����\x0015�����.�V�G</p><p>�\x0005K���S\x001e�䈅˾� !�$e�\x001dA�`���X�Yq+��żJ</p>
  
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
  
  
  * Evidence: `14101462`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14101530`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `840527803`
  
  
  
  
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
  
  
  * Evidence: `351512120`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `14100834`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `372432901`
  
  
  
  
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

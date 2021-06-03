
# ZAP Scanning Report

Generated on Thu, 3 Jun 2021 03:43:32


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 2 |
| Low | 4 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Hash Disclosure - Mac OSX salted SHA-1 | High | 3 | 
| Content Security Policy (CSP) Header Not Set | Medium | 5 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 8 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 7 | 
| Base64 Disclosure | Informational | 7 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 6 | 
| Retrieved from Cache | Informational | 12 | 
| Storable but Non-Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Hash Disclosure - Mac OSX salted SHA-1
##### High (Medium)
  
  
  
  
#### Description
<p>A hash was disclosed by the web server. - Mac OSX salted SHA-1</p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012121212121212121212121212121212121212121212121`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012323232323232323232123232312121212121212121212`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `012323232323232323232123232323232323232323232323`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that hashes that are used to protect credentials or other resources are not leaked by the web server or database. There is typically no requirement for password hashes to be accessible to the web browser.      </p>
  
### Other information
<p>012121212121212121212121212121212121212121212121</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage
* http://openwall.info/wiki/john/sample-hashes

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/beta](https://app.passculture.beta.gouv.fr/beta)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-analytics.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async defer="defer" crossorigin="anonymous" src="https://connect.facebook.net/fr_FR/sdk.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-firestore.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async defer="defer" crossorigin="anonymous" src="https://connect.facebook.net/fr_FR/sdk.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-firestore.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-analytics.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://connect.facebook.net/fr_FR/sdk.js`
  
  
  * Evidence: `<script async defer="defer" crossorigin="anonymous" src="https://connect.facebook.net/fr_FR/sdk.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-analytics.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-analytics.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=AW-706346995`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.googletagmanager.com/gtag/js?id=AW-706346995`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-analytics.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-analytics.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://connect.facebook.net/fr_FR/sdk.js`
  
  
  * Evidence: `<script async defer="defer" crossorigin="anonymous" src="https://connect.facebook.net/fr_FR/sdk.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-firestore.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-firestore.js"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://www.gstatic.com/firebasejs/8.0.0/firebase-firestore.js`
  
  
  * Evidence: `<script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-firestore.js"></script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
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
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/beta](https://app.passculture.beta.gouv.fr/beta)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/runtime.3bf49e49.js](https://app.passculture.beta.gouv.fr/static/js/runtime.3bf49e49.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/main.43ae5b95.js](https://app.passculture.beta.gouv.fr/static/js/main.43ae5b95.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/beta](https://app.passculture.beta.gouv.fr/beta)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/0.css](https://app.passculture.beta.gouv.fr/0.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest.json](https://app.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `/iosSplashscreens/iphone5_splash`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/main.43ae5b95.js](https://app.passculture.beta.gouv.fr/static/js/main.43ae5b95.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `ICKjBVVL7kE1q4JGo0h4l6t8yG7Drioexj/D5DUnbXM=`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/iosSplashscreens/iphone5_splash`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `/iosSplashscreens/iphone5_splash`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `/iosSplashscreens/iphone5_splash`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhEQARAIAAAODn7P///yH5BAEHAAEALAAAAAARABEAAAIqBIKpab3v3EMyVHWtWZluf0za0XFNKDJfCq5i5JpomdUxqKLQVmInqyoAADs=`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/beta](https://app.passculture.beta.gouv.fr/beta)
  
  
  * Method: `GET`
  
  
  * Evidence: `/iosSplashscreens/iphone5_splash`
  
  
  
  
Instances: 7
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�*,J�Z�\x001b\x001c�秳�������)��!</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/main.43ae5b95.js](https://app.passculture.beta.gouv.fr/static/js/main.43ae5b95.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `fixme`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFIXME\b and was detected in the element starting with: "(window.webpackJsonp=window.webpackJsonp||[]).push([[0],{128:function(e,t,r){e.exports={black:"#151515",primary:"#eb0055",tertia", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/beta](https://app.passculture.beta.gouv.fr/beta)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js](https://app.passculture.beta.gouv.fr/static/js/vendors~main.ec0715c2.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script async src="https://www.googletagmanager.com/gtag/js?id=AW-706346995"></script>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone@3x.png](https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone@3x.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 53679`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphonex_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphonex_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 45196`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone.png](https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 41754`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphoneplus_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphoneplus_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 45196`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone5_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone5_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 41755`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 2`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 2`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone6_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone6_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest.json](https://app.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 53680`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone5_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone5_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone6_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphone6_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest.json](https://app.passculture.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone@3x.png](https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone@3x.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone.png](https://app.passculture.beta.gouv.fr/manifest-icons/app-icon-iphone.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphoneplus_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphoneplus_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/sitemap.xml](https://app.passculture.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/iosSplashscreens/iphonex_splash.png](https://app.passculture.beta.gouv.fr/iosSplashscreens/iphonex_splash.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/robots.txt](https://app.passculture.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `706346995`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr](https://app.passculture.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `706346995`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `706346995`
  
  
  
  
* URL: [https://app.passculture.beta.gouv.fr/](https://app.passculture.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `80095874`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>706346995, which evaluates to: 1992-05-20 07:29:55</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

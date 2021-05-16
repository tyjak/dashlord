
# ZAP Scanning Report

Generated on Sun, 16 May 2021 01:05:55


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 12 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 6 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 1 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 8 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 6 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 1 | 
| Modern Web Application | Informational | 11 | 
| Retrieved from Cache | Informational | 12 | 
| Storable but Non-Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 15 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/sitemap.xml](https://blog.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2019/04/12/gestion-publique-101-engager-et-depenser/](https://blog.beta.gouv.fr/dinsic/2019/04/12/gestion-publique-101-engager-et-depenser/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://palya.fr/" target="_blank" rel="noopener">
                <p>Tout faire pour les usagers</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2019/06/11/embauche-beta-gouv-fr-devient-mon-entreprise-fr/](https://blog.beta.gouv.fr/dinsic/2019/06/11/embauche-beta-gouv-fr-devient-mon-entreprise-fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://johangirod.com" target="_blank" rel="noopener">
                

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/general/2021/05/05/letaxi-service-public/](https://blog.beta.gouv.fr/general/2021/05/05/letaxi-service-public/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/olmaffre" target="_blank" rel="noopener">
                

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2020/04/23/11-initiatives-covid19-accompagnees-par-beta-gouv-fr/](https://blog.beta.gouv.fr/dinsic/2020/04/23/11-initiatives-covid19-accompagnees-par-beta-gouv-fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/beta.gouv.fr/edit/master/content/_authors/florian.delezenne.md" target="_blank" rel="noopener">
                <p>[Cliquez ici pour améliorer cette bio]</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2020/01/14/lapproche-beta-gouv-fr-essaime-dans-les-territoires/](https://blog.beta.gouv.fr/dinsic/2020/01/14/lapproche-beta-gouv-fr-essaime-dans-les-territoires/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/hijazi_i" target="_blank" rel="noopener">
                

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2018/09/24/simuler-impact-loi/](https://blog.beta.gouv.fr/dinsic/2018/09/24/simuler-impact-loi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.linkedin.com/in/sandra-chakroun" target="_blank" rel="noopener">
                

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2020/01/22/coder-la-legislation-au-benefice-des-citoyens/](https://blog.beta.gouv.fr/dinsic/2020/01/22/coder-la-legislation-au-benefice-des-citoyens/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.linkedin.com/in/maukoquiroga/" target="_blank" rel="noopener">
                <p>Engagé dans la construction d’une action publique au XXI<sup>e</sup> siècle.</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2019/03/18/le-standup-histoire-dun-rituel/](https://blog.beta.gouv.fr/dinsic/2019/03/18/le-standup-histoire-dun-rituel/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://pezziardi.net" target="_blank" rel="noopener">
                <p>Débureaucratisation et Rock &amp; Roll</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2018/08/04/amiens-plante-et-moi/](https://blog.beta.gouv.fr/dinsic/2018/08/04/amiens-plante-et-moi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/jdauphant" target="_blank" rel="noopener">
                <p>Chercheur de simplicité</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2020/11/10/nous-recrutons-une-brigade-numerique/](https://blog.beta.gouv.fr/dinsic/2020/11/10/nous-recrutons-une-brigade-numerique/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/beta.gouv.fr/edit/master/content/_authors/florian.delezenne.md" target="_blank" rel="noopener">
                <p>[Cliquez ici pour améliorer cette bio]</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2018/02/12/mes-aides-nos-voeux/](https://blog.beta.gouv.fr/dinsic/2018/02/12/mes-aides-nos-voeux/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://palya.fr/" target="_blank" rel="noopener">
                <p>Tout faire pour les usagers</p>

              </a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2020/05/25/retex-rituels-de-sprint-de-lequipe-e-controle-titre-provisoire/](https://blog.beta.gouv.fr/dinsic/2020/05/25/retex-rituels-de-sprint-de-lequipe-e-controle-titre-provisoire/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/lazybird" target="_blank" rel="noopener">
                

              </a>`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/img/posts/2020-02-06-mes-aides-experts.jpg](https://blog.beta.gouv.fr/img/posts/2020-02-06-mes-aides-experts.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#6Lrh`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#6Lrh</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/sgmas](https://blog.beta.gouv.fr/categorie/sgmas)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general/beta.gouv.fr](https://blog.beta.gouv.fr/categorie/general/beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2021/04/19/1-120-000-euros-pour-les-laureats-du-fast-7-postulez-des-maintenant-a-la-8eme-edition/fast@beta.gouv.fr](https://blog.beta.gouv.fr/dinsic/2021/04/19/1-120-000-euros-pour-les-laureats-du-fast-7-postulez-des-maintenant-a-la-8eme-edition/fast@beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/sitemap.xml](https://blog.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/FAST_2400x448-nom-du-fonds.jpg](https://blog.beta.gouv.fr/categorie/dinsic/FAST_2400x448-nom-du-fonds.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href='https://fonts.googleapis.com/css?family=Roboto:400,700&subset=latin,latin-ext' rel='stylesheet' type='text/css'>`
  
  
  
  
Instances: 6
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general/](https://blog.beta.gouv.fr/categorie/general/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/presse/](https://blog.beta.gouv.fr/categorie/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/newsletter/](https://blog.beta.gouv.fr/newsletter/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="https://app.mailjet.com/widget/iframe/1O2v/9ud" id="newsletter">`
  
  
  
  
Instances: 1
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "subscribe-email" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef](https://blog.beta.gouv.fr/categorie/fabnumdef)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi](https://blog.beta.gouv.fr/categorie/pole-emploi)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2020/11/26/retour-experience-FAST/](https://blog.beta.gouv.fr/dinsic/2020/11/26/retour-experience-FAST/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic](https://blog.beta.gouv.fr/categorie/dinsic)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes](https://blog.beta.gouv.fr/categorie/mtes)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general](https://blog.beta.gouv.fr/categorie/general)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/presse](https://blog.beta.gouv.fr/categorie/presse)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/general/2016/06/09/FenS/](https://blog.beta.gouv.fr/general/2016/06/09/FenS/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 21 [/categorie/fabnumdef/].</p><p>Predicted response size: 321.</p><p>Response Body Length: 25,263.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/sitemap.xml](https://blog.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general/](https://blog.beta.gouv.fr/categorie/general/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/presse/](https://blog.beta.gouv.fr/categorie/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0, must-revalidate`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/sgmas](https://blog.beta.gouv.fr/categorie/sgmas)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general/beta.gouv.fr](https://blog.beta.gouv.fr/categorie/general/beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2021/04/19/1-120-000-euros-pour-les-laureats-du-fast-7-postulez-des-maintenant-a-la-8eme-edition/fast@beta.gouv.fr](https://blog.beta.gouv.fr/dinsic/2021/04/19/1-120-000-euros-pour-les-laureats-du-fast-7-postulez-des-maintenant-a-la-8eme-edition/fast@beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/sitemap.xml](https://blog.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/FAST_2400x448-nom-du-fonds.jpg](https://blog.beta.gouv.fr/categorie/dinsic/FAST_2400x448-nom-du-fonds.jpg)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/presse/](https://blog.beta.gouv.fr/categorie/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general/](https://blog.beta.gouv.fr/categorie/general/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/fabnumdef/2021/04/02/au-bout-de-l-agile/](https://blog.beta.gouv.fr/fabnumdef/2021/04/02/au-bout-de-l-agile/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dinsic/2020/11/26/retour-experience-FAST/`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef](https://blog.beta.gouv.fr/categorie/fabnumdef)
  
  
  * Method: `GET`
  
  
  * Evidence: `MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic](https://blog.beta.gouv.fr/categorie/dinsic)
  
  
  * Method: `GET`
  
  
  * Evidence: `/dinsic/2020/11/26/retour-experience-FAST/`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/general/2021/05/05/letaxi-service-public/](https://blog.beta.gouv.fr/general/2021/05/05/letaxi-service-public/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/codes/article_lc/LEGIARTI000039784232/2020-12-27`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2021/05/11/bilan-gamma-1/](https://blog.beta.gouv.fr/dinsic/2021/05/11/bilan-gamma-1/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/5Vca3nP1xxOqvX4nNfr-IBWbSaegZQXo3ceE5vF7059zpEoNOREZdH_DpYR0n1Mh8coxZStOt8kEITg48gXjI8gI89xdMSmGleFfRrsbEmnYRWwEDRDo-GJ4ecqiD8Q1MaHowYRQ`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2021/04/19/1-120-000-euros-pour-les-laureats-du-fast-7-postulez-des-maintenant-a-la-8eme-edition/](https://blog.beta.gouv.fr/dinsic/2021/04/19/1-120-000-euros-pour-les-laureats-du-fast-7-postulez-des-maintenant-a-la-8eme-edition/)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/img/posts/FAST_2400x448-nom-du-fonds`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Evidence: `MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>1|1207|0|0|photo-page||||en|0|||</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/dinsic/2019/04/12/gestion-publique-101-engager-et-depenser/](https://blog.beta.gouv.fr/dinsic/2019/04/12/gestion-publique-101-engager-et-depenser/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: "<script type="text/javascript"></p><p>var dimensions = {</p><p>  height: 130,</p><p>  width: 800,</p><p>  margin: {</p><p>    top: 50,</p><p>    bottom: 110,</p><p>    le", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/general/](https://blog.beta.gouv.fr/categorie/general/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/presse/](https://blog.beta.gouv.fr/categorie/presse/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a  href="">Articles</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 172884`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 4`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 1`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 3`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 2`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/sitemap.xml](https://blog.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
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
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/fabnumdef/](https://blog.beta.gouv.fr/categorie/fabnumdef/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/](https://blog.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/sitemap.xml](https://blog.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/innolab-62/](https://blog.beta.gouv.fr/categorie/innolab-62/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/dinsic/](https://blog.beta.gouv.fr/categorie/dinsic/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr](https://blog.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/lab-mi/](https://blog.beta.gouv.fr/categorie/lab-mi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/](https://blog.beta.gouv.fr/categorie/incubateur-des-affaires-sociales/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/pole-emploi/](https://blog.beta.gouv.fr/categorie/pole-emploi/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/categorie/mtes/](https://blog.beta.gouv.fr/categorie/mtes/)
  
  
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
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `84187871`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `09370803`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `43294953`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `25388719`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `84199531`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `74611281`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `55809517`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `56693769`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `56693751`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `74611298`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `25388736`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `43294936`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `91930485`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `23531459`
  
  
  
  
* URL: [https://blog.beta.gouv.fr/robots.txt](https://blog.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `24208544`
  
  
  
  
Instances: 15
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>84187871, which evaluates to: 1972-09-01 09:31:11</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

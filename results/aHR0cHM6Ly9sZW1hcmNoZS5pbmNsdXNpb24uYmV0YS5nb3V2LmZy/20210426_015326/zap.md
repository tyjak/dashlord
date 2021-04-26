
# ZAP Scanning Report

Generated on Mon, 26 Apr 2021 01:37:48


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 4 |
| Low | 13 |
| Informational | 9 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 12 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Application Error Disclosure | Low | 3 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Cookie Without SameSite Attribute | Low | 4 | 
| Cookie Without Secure Flag | Low | 4 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 6 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Information Disclosure - Debug Error Messages | Low | 3 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Sensitive Information in URL | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 9 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 43 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 15 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2533/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2533/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50870892200044`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1436879464/voir](https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1436879464/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `50777322400013`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/5763/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/5763/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50065213600010`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=3](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=4](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=4)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/4631/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/4631/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `30582109200031`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=1](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=2](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/1649/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/1649/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50005187500044`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=5](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=5)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/4593/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/4593/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `30582109200031`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/184/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/184/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38848971800022`
  
  
  
  
Instances: 12
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 508708</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="h_sl" class="btn btn-outline-primary" href="https://itou.typeform.com/to/nxG0HlYx" target="_blank" style="margin-top:18px;">
                                Faire une demande
                                <i class="icon-right-small"></i>
                            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_medium/uploads/listings/images/b38e983edc851ae7f85b58cc8af05a93fb8dd2fd.png](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_medium/uploads/listings/images/b38e983edc851ae7f85b58cc8af05a93fb8dd2fd.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=I\x001b\x001cOåþîÑv·õ7ó{øÃï­\x0016K÷O[ß~ûë+www>¼û`JÁO?¿µ?MÎÏÏÜÞ^yzz´ZyñâÆb>·y~ö¯ÿöGBkÍwßýÆëkw÷÷z\x00177/Ã`8Xk\x001f?~´?ì}ÿýwnooí÷{ÍÆétTUJQ¥ª« \x0000Uzïè Ð{W\x0008\x0014U]éR¥úR)UT/D\x0012i¥%ªJõNTNJÚ \x0010H\x0008¥@Kè¦µH($4\x0014½Pz÷¦ª«c3\x001bºa\x001cd\-ÖùJ\x001bæd \x0011PJ$\x0012R\x0005R½PH\x0002Z"
*tZkfã( @
DU¡Tu½w\x0014¢
Hª®tNÇ\x0003Êi,æ+Ã0z7M©ÞËlvR\x0015ÏÏ6ý`hÑ\x001a	\x0005 \x0000\x0000\x0015Qè\x0012U@AR\x0012\x0005 P( \x0004\x0001(ªPeüéw.ÏÏ­×k½ÞËv³5õI\x0012CkÖëÙlFq6ê5Ùí÷zùba¿ßÙî¶ÖëÅre¿ß\x001bÂñxt<uãÉáX§'\x0017\x0017Z\x001b<<>Hb\x0018\x0006««ÁõÕ¥Ýv´ÙPUN§W¯n<Ü?ùù§]_ûáwß¦÷ï?yx|ò×ÿòWíÎt*½7_¾<êýh½Z:??\x0016}:\x001a2¶p~yn6y~Úè½ùøé³õêàß}¯ãa¯N'Ç©»¼º2\x001b\x0006üó<>nÌç£åúÚétpwç°ZûõÝ\x0007ÏÏ[»ÝÎÇ\x000fôâööÖn·õððÅb6sy¾¶\Î,Wk÷wOapv¾6ÎF\x000fOÇëKçgg®®®<o÷>ß=¦ÉÙÙKÅ|n>yzzt÷ÅõÍ\x000b_½~ãýû·Þ½ÿÕ4\x001dµ\x0016U\x0011¥WGD\x0004B&) ªTu¨\x000c\x001aJ©*\x0014ER\x0014UEAIPHIÈÐ¨ h4$Z\x0002(´*IHÐUÑZ\x0006\x0014Ò\x0014Õ
\x001dê2ÆùVf#ÃØÔ0×f3Ã8J\x000bJK¤EU§&­
!R\x0005\x0012¦ª\x0012D\x001b"¢µAÒTÑª*¡Ïç &	HQ\x0001(U\x001d¥*(U\x0005\x0012 *R\x001c\x000fÓtp8,\x0016sã08õÉi\x001aLS7Mf¾ÍF³qfhM\x0002]é(Ñ\x0014\x0014\x0000 (\x0002(\x0000$¥\x0004º¤T¢+\x0005J\x0002\x0014T\x0001¡@©tckí~g¹[Ì\x00176Ú\x001fvªOæ³Ñííal\x000eYkÍöÙf»7£a\x001c³Ñ|>ªâÅÍµççgËåÂv»sw÷ mÐÁnwp:~QÍvg&ËåR)ñÙz9×ZÌç\x000bëõÊóóùÜßÿýß¹ûòÙn·µÛî¬W+OO\x000f~yûÞáxòÍ7ß\x0018ÇÑáp°ÙlMûrv~®÷n¿ßûüøàâbíööÖãóÖ_ÿú³³õi¨r}uåo¾òòöÒiÜ}9ÒËf³5\x000eÍùå¥/_:\x001dßÚîvóÓqï¯ýIUwxxx\x0012TñÍ·ßùÃ\x001fþÆÏ?ÿdµZÚíöZÙ|a½:wØ÷ïßyùòÖ|±°ÿøÙé4Y,\x0016æ³ýþ µ¦µøóÿl66\x0017gkÇÃÎ84Oû\x001füIUóæÍ×NÇwï~v:\x001e\x000cã zIQU$Ò$TR\x0002JT\x001a$\x0012\x0014\x0014\x0015i´\x000c"º*R\x0000hÒ\x000b"Bu$@$H"´¨*i\x000c­ªÒZ´DUQT*=e\x0018¢Íg2vc+\x0019\x0006]Ó\x001aãÐ´Ö´0´ÖL½¨2\x000eÍ0\x000cR¨D\x0012PUJi-Z$a&¢÷\x0012]tÃ0
Ö\x001a\x001a"\x0001zQJ\x0012\x0014\x0015U]\x0012Õ'\x0000t\x0011©¨Î)
¥÷	¥¦4TkªºÖh-Ö\x000c­I\x0008ª:é\x0004EUI
\x0000\x0000\x0000@\x0012	\x0004¥ªB©*	B¢\x0010\x0000)\x0014\x0018¯¯Î©ÒZs:\x001dD\x0019f±ZX,Ö«¥ÞËép´ïÍfc¿ßKkÆÙÜóóÆÙÙÚÍ\x0017¶ãñèìlíl½rv¶6´Áþp²ßï¬×+ýNõîüüÌlY-¶»>\x001dm6Of³ÓéäphzÜßÝ{yûÂo~óûû\x0007?ÝB9\x001eO./®ÜÞÜZ,\x0007ªûðñÙxëþáÁÇÌÇªîêêÚb¹öå~k¿l?:??3\x000cÍ0ãì|áxÚûøñ£d°^­]\^x~~öñógçççÞ|ó/_¾¦qlf³¹\x001fÿúq¾tssíêúÒiê\x000eû=u2_4Ã6f¿?xùò¥Ãng¹[­V6ë\x0017þú×\x001f]]^yýò¥ÕzåþáÞóóÆÐ\x0006OÏO½¸ºôøø(­¦ÉápòåîÞj}f±Xzýú\x001fßëý¤·¢\x0017EÖ\x0006	U%E¡ P\x0005\x0008¨*II\x0004è\x0005¥Ð\x0012\x0011ªèzÐ§If£a\x0018\x0011­Ek\x0011MÐCU0(t­EKSU\x0014U]ï\x001d\x000ci2kÕD)ÑÖ\x0006±\x0019Ú \x0018AÁqª2\x001bFÃÐDT$ ªº2I"¡µfhM4t­Ç¤$]B\x0012\x0010\x0008UD@I\x0000\x0005P$\x0014R\x0018DIQ)IW}Ò§£2\x0001EB/0$¡I#(\x0004\x0001t@\x0002\x0000T\x0001U\x0005\x0000@ \x0014%hD\x0015\x0014B"U JUQeüúÍKÏO\x001bíÞ4Mfã`¹;??·^/ív;OfR6½ÓédhN§½Ífc½\Z.æóË«3}:Iâõë[\x000cîï¾/ç¦é\x001c13WW×Zøôù^Ýáp0õù|¦÷ÉÙÙívç_þõn®¯\\\Øïï$\]]y}8y~Üúôþ½ß|÷µ§GÛç­iQ>|øèññÙb±ðúõ+5ÌüË¿þó+ÿÍ?ü_~þÙýý\x0017óóµ*~ýõÊ_~ü«ËËKÃ08\x001eöZX¬V\x001e\x001e|úôÙjµ¶^-MÓÑ0\x000eÖçg6­Þ»Ývçñyãó/®¯.\]_z÷îÃáàp8ÏfÎ®/Ìçs/o_øå×wÒFgçg~÷ûßúþï\^N'O³sßþæ;ÇÃÑ89¦iÒ{y|z¶ÛÿèþîÎüÿè÷¿ÿõúÌÛ·?Ûl6(\x0015 ª«bê*ã\x0010Mô"\x0000U"Ji¢:¦Tº(\x0015Z¢µ\x0008TÐU:J\x0015ÕªºÍlÖÖÖ@ª\x0006`\x001c\x001a	&I3´\x0001QUªJÕÉXÑ+\x0006¤:¦rf6ÎÃ\x000c\x000cã ibR\x0018Ak
T\x0004¨¦4¥TºÖ¢µ¦¡µ¦ª®e¤\x0010(BtU$\x0011¨\x0002Q
P\x0004H	 ÷®×¤L¤£T\x0015\x0012´Fk@¨ )\x0014\x0000ª\x0000\x0005¤Ñ{\x0001¨* B\x000f)\x0000z¨¤©@!A\x0015A*(q6»}¹æÓ'­5çgg.¯.¬VKÇÓÁf;yzzT\x0015ÕJkq8\x001c\x001dN'­
ZcN6­Å|épØÙnât:9ì\x000ffãÌz½v}s©µæ4uU%ÖÊ8\x000cªºý~çx<Úï\x000fÎÖç¾ùú\x001båÜÔ»÷ï>ùù§wn^l
#z¼yóµ³µÇ»\x0007\x000fO>~ZØl6îpÜ¦I\x0012Ã8\x001ags\x001fÞr8NVË¹««\x000b«ÕïýOÿßÿç§¯^Y-Zõjíý\x000ff³ÝvëúêÊêìÂv·óøøøÍw¿ñéã{³ùÜ÷?|ç_ÿåa´^Y«©¼{ûÁÙúÌ«/=?o<>>ùõ×¼zýÒl¹ººõ»\x001f~çÿõÿþÿ8îfÃÌ8\x000cÞøàÛo¾ñÛß~çÓ\x0007_¿yãþógoß½÷ío¾±Z­­Ïí\x000f'··/Pöû½Û·¾\x001d\x0006ÏOTMJ\x0001Påt::\x001e\x000e\x0016åba6\x000cT©*	  -TQ´\x0016Ð'zH¢µ¦%JTAÐô*Õ» &fc³aÐÒ\x0010\x0011Ò©"´6H\x00062h´F\x0005\x0004e4VWHHêq:N*Ñ\x0012ã87\x000esB&Ö\x001ah-&\x0002D\x0015A)QZH\x001bÐ´Dë\x0003¢ª¨RÕÑ$A¡¨\x0004\x0010iMõN\x0011\x0008U$P@\x0000JUW½HB \x0010D\x0002Ñ«Ò@\x0010B\x0004ô^ÚP $ª
\x0004@ÒTu\x0011\x0004B\x0000\x0001I£:\x0000@(Æ\x001füÙÍÍ\x000bã8×{·Ï\ëºÝþ¤ª8õ2öÉ|>3Í\x001cOGçgóÅÜ0Äæyk6Î\x001cÝçÏ{U\x001cöG³ÙàáñÞÍkgë3ûÝF2¦Éétr:<=ml\x000f{ËùÜÙúÌ~·óùó'¯^ÝZ.nooüòË¯ýýßÿ­Å|îxìfÃÜÙÙÚÔ'»ýÁáxRÕíö\x0007óùÜoó\x001bÂÐb}óÊúìwîï¿øù¯V«®Ï\x0017¦ir§÷òõ×_¹¸<sÿ`êåpê(¿ûá{C\x001b¼{ûÞýÃÃiòpÿèÍ×öû£Ï\x001e\]]º½¹T§ãéäã§zô^¾ýök?ýø£þçõõ×ßøñÇ½þê\x001bÏgóÙ\K¼ÿÞé´·ÛnÝÜÜØï>¼}ïüüÂãó·oq}qíêâÒi:Y.FççNûçG\x001aóùÜr9sØMª\x0002U~ÜØo\x000c¹0®\x0016Æ1ªJïEHJkÑZ\x0013(ôHk"ú\x0010U%)I4¥¨`ªÉÔ»!ÚÉ8\x001fÍ\x0016\x000b-D4#®tQÀ0JT4Ö$\x0011!TuCu-EJJULÊD¢µA\x001b"iZJTJKD´\x0004\x0010\x0000=4è¢HCHhM2¨êzïIB\x0013Õ\x0006Õ	4A	C^T©ê\x0002\x0000UA\x0010ÐHê !\x0004®TuIRJD¡ª$\x0000UÐ@U\x0004)J\x0011 $(¥\x0012ª@G*Q`øÝ÷ßýcÂl6zzz²Ým
C\x001c\x000e{ÏgÇÃIõRHb¹\sU¥ª´\x0016óÙL¯n·Ý\x0019ÇÙlÔZåj¡÷îp<Jb»ÝÍf\x000eÃñHÝþ`<©*³q´Z¯N'ç­ÓÔõ^\x000e4VË¥««+ÃÉîpÔ§õzi>\x001bm7[ç\x0017\x0017NÓÉwß}ãï¿³Ûm¼xqãòòÒÝÝ½·¿¾óðpòü¼ñ¼ÙØï\x000f¶ÛÝ~ïÅ\x001b¿ÿß9\x0014ÃÐìv[ëÕÚ|¾0õë«+\x0017çç6g§SÍæÇ/_>yýêµÓéh{Øûñ§}úøÙj½6õîÔÙn\x000e¦©<>>û/ÿüO6Ûg¿ûýoýíßþÎÇ\x001fÜÝß{÷îívoµ^)Ýáx²ÛíQÖgg§É\x000f\x001fìv[Óéd±\:M'ÇÃÁáx0\x000cD7\x001bc\x00188\x001d\x000fv»Ùlpqqf6i-Æqlfã`\x001c\x0006³q4´AkÍ04ã0\x001aÇf\x0018b\x0018b5ã8\x0018f\x00186Ä8\x000cÖd¡5Äl¾²Z®\x000cC3´fhÖ\x0006­5CkZkZ\x001b
Ã 
Ö\x0006­
qÐA&­ÑÖahZÖÖ\x0006D¯Ik1\x001bGÃÐ´\x0016I\x0016-MÖ\x0000H£5Ò¤ *A©Þ'½ºa\x001c´\x0016IH¤\x0005ôÞ%´Ö\x0014 PT\x0001	IH@\x0012]L§£ç§G»ýÞr¹2ÍLÓI¯ÒBU\x001c\x000eGÍÖ~´\Ì-çÒ\x0006ÕfdT¢ª@kMk\x0004T\x0015Hr8\x001cì\x000f{S?)e\x0018\x0006ë³sçësã8DBï]Mª\x0002 A¤JBÚ 
£±µÑr¹2\x000cÍÅùÚv÷äáñÁb67&§ÓÉr±d8êÕÁ|9WÊn·SÕõ¢&»ãÎ0ÎÖkóÅÌá\x0014ùÌ4MN§n\x001cfád8èU6ù|n\x001cGÃñh:N\x000eíd>_èÇÇ{Ò28??3MG¿üòO>Ùí\x000e§n:\x001d¼º½öúõ+ßÿ/w\x000fÚ8º½ya³y¶\Î­×küó_üó?ýÅléûï¿µZÏLÓÉÃÃ³ÞËñ´7ÍüéOrv¾òß|kµ\ûõ×_}þüä?ý§ÿäÍ¯¬W+-¼ùê¤üé?yñâÆ\x001fþ»ÿÖ_þü\x0017\x000fO^¼¸qÿôl6{~zÖ{9\x001cîîîhQÕ]ß¼°X­|øôÉófcµ^¸¼¾ôîý\x0007ªÙlz5ß~û­û·?Ù\x001f\x000ev»­/_9ªøùw\x001eÎ\x001fí\x000eG777...¬WgæóVÝnÓE×«\x0012ûaD\x0013cb66Ñ0H"h*zÐÚ\x0000hJ©DC*ºR\x0015MSºÒT/Õ©bl£aIJtÑÄ(AR -*$A´\x0016ITQºVAPTi\x0005QUZ*ÒH"PE$\x0014\x0012\x0000 Ö\x0014TI"A!D)RU 	Jé&UêÿO\x0010~-Y¥iÝú·ê¡F\x0007KV¼Q\x0016@@\x0004x9<Û\x0000\x00022\x0017¸ÀôÌTu±ÌÈ\x0008gæÆí0Õýa-QU \x0001\x0000

 \x0010¥\x0004PÞ»yô>IB\x0011¨ÐÖÖF­¤$!!\x0000\x0001U@B\x0015\x0014
\x0000tUA©*\x0005
\x0000@
\x0000\x0001¡¢P1j¥ZY-.¶[/Ãé(\x0015«åRµætìm©g>+$ZkË5xyyq8N^v{/»õféòâR\x0015ÇÃd:¼¼ìÌ}Ò{$1\x000eÅ¸ HºÃáäééÉóó³åjíe¿·9n½º¾Ðûd¿?iÃhg»Ý¯wú<ibµZûæo)\x0016ÃàË\x001b=ÕréþþÉÏ_½<¿øî\x000fßúÍß¹»ÿêêúÂz½Ö;m\x0018,\x0016£i:º¹¹qwo1®Ãèõë7\x000es­
\x000eÇO>Z.F¿ûÝo}øõ_~þÅ÷?¼õ»ßýÖ×¯÷öË3ëåÂW×ªÊr¹p}yé4O¾yûÎÛ·ï¦îøü?|øðÉ_þò«Â4uÍVðéÓ'××\x0017Î.Ï¤Êñpôò²7ÍÕõµ_?|ôéóÞ»ËËKÃ0¨jÎ¶\x0017æÃÞ<í¤\x000cé¤kU¤TaX\x0018ÖJ)
¨ª\x001eAUi­$ô$Z(´").\x0006i1OLÓ¬Ui­iÒ\x0014T£hPTºRREQ\x0005¥*¤Q$T\x0015P¡ª@UT\x0015\x0005¥ª¨\x0008ªJ!	¨¢\x0012PEQUBA5PÕU5UE5ÕªAUQ¥¦ÑHª\x0002\x0012
	¢\x0010E(%\x0015A¯èéæy2÷	QÕN\x0012\x0014Z+Õ\x001a\x0013CHR\x0004¨*URÕôÞ\x0001$PU  BPª*é\x0001 RªÄøæÕÕzm\x0018\x0006\x0017ë­ÓÅ¥ýÎ<Ï$ÆåÒÎAëô~¢wã88\x001cÊ<w­5½w½G\x0012Ó4{~y1MGïÞ½uu}e»í\x0016ãD©[¯W6ëµÓé¤ª,£ÝÂv3Kïî\x001eîÕ0j5z||±^­Å¤g\x0006ðÍ7oË¥\x001f?ùõãgûÃÉr¹òã?¨Ä_?¹¸<³^oHÓ;ãb¡D|ûÝ÷àÓÇÏ§£oÞ½÷øø¤jãÝ7oý×ÿéöô¼Óçxýúµï¿ÿÞ¯¿þlN\x000eiîÎ¯®¼yûÚOþ³û·¼zuåììÜ_þò³Å8X­Vë¥ûûG_o¿zÙí\x001cO'o^¿±\ÚXzõzëÿñgËåÂr¹2÷ÉÓÓ£Ç;ß¼{í°?xÙí|ûî\x001bãØ¬VKÓÔN³x~ÞÙï\x000fªÊãã£÷ïß{÷þ;ÃÀãÃy:ª\x0016Z£a\x0018,\x0016\x000b¥¨R
)PJ
UhEZ!\x0012JTºªHêE
hæÞQ.½¨\x001aP
¥I¡
TQÕTP**H¢ª\x0002
=ª¨")RªJU©Ö\x0004ê¨P¥*J4¨¢\x0015ÒEI\x0002ÐT\x001bÃ\x0002@)Uj$\x0000^H( 
% ¢¡\x000bæ>¦I;\x0002R\x0004Ph­´¡iC#\x0008\x0005U 
\x0000¥TQ\x0005ô\x000e¥R $\x0008\x0002ª\x0000R\x0005\x0008* !a|÷î­^ÅþèjsæÝëW>=Þùz{ç4D´6zz~1´Å88\x001cN\x0016Ñv»ÑZóò²s8\x001cTÞãñéÅ}&»ÝÁ÷S·\x0018\x0006C+åÒ¼XJºy$ÝËËóva'Ó49¿8â8Mzº\x0017?OVëÑv»\x0005Q^]_[.NÇ¯w\x000fw{¿~øàÍëkç[íom6kI÷ñãg××WÆÅ¨°ß\x001f¼}÷ÎúÙíí½ËsI¼¼<;ì÷Þ¿ïÛï¾÷éÓ\x0017··÷½^[­6=<>[®¶v»7o¯oýô§½<ïüæ·ßëiU
_\x001dOçÝÁntw{ï¿þOÿ\x000b¸¼¾òæíµËóK§ÃÁt\^^Ù\x001fv./Ï]]\Z\x000bã0hÊÝý½k\x0017..Îåig\x001c\x0017ª-¼ìö>}úäíÛ×ªÊóó³\x001füÑj½2ýiòôø\x0005é\x001d]\x0015ÃÐ¤ (Ri\x0012(*R¥)e\x0006M£HºRR´
U ª¨"\x0015½O\x0004J\x0015U¨Ò@¡TE¡*ªj
@\x0012U%ªB©Hu½R¢´jª\x0006­J\x0015ª¨"h\x001dRUªhUª
BQ((@QôD\x0004MU©*I@+&\x0002"@H+I\x0011TIB¨ 
$ÑçYú\x000cªJ\x0015\x0005J«2\x000cÅØ\x000cC©FU©jh¢P ªP(4ªHÒÓAUCPU(\x0004\x001dQ\x001a
PZ#\x0001ª ¨\x0008
áÿð¿ÿÏÿ·³õÖëÍÖ\x000fW\x0017Þ÷½ó7ï´a4´&b>MNÇ£Þ»q\x001cT5ËÅ¨
¥÷Ùét2M³q\x001cÁáp°ß\x001f\x001dGCk¶Û­i:ç	ôtûýÞÃÃ§çg§Ó¤§¼ìv\x000eÇ£Þã4ÍV«qhæéh¹\\x0018ªÙ\x001f\x000e¦i¶Ùl]]^\x001aK64¯®.
\x0015­ñêÕ+ÏÏ;\x001f?~Ö3y÷ö­ËK\x0017\x0016ãh³9óëî\x001e\x001e=?=Û¬W^½ºvssëöö^kÍ·ß½÷þý;éåééÑt\x000cÃ`½^ë·o®ýæ·?H?þñÏVëµ\x000b\x0017ç\x0017Vëµi
ÃàÕ«+ËåÒ4Gzìv{Zùöý[ÿýÿö\x001fmî\x001f\x001eÜ|ý*q\x001ccóíwï\x0005_¾|öêÕ+w÷\x000f¦éd»Ý\x0018æe·\x0017³qh6µóÍÖÕåÝÞËËÞj½qq~ît:Ú½¼Ø¿ì¼<?Y,G××¯,W\x001b­\x0015EkM)PÕTT©*ÕJUQT\x0015UT©¢U©*¥PªPLól&ã8Zo6qÐªT+­ª¦ª´VªJ«ÒªÑ\x0006U¥µ¢¨*M©*ÕJk¥ª©jªÊ<w}P\x0016¥a\x0018Ô@UÓj J\x0003¡¢ª¦ZQ*ÕJ \x0000
\x0005¤ëÓäpØX­VqTJ5´F\x0015\x0005¤"\x0012¥hMU¡4¥ª@ªÌS÷pwçååÉÙöÂf{&yî$hjhæÄétr8\x001e­l×+ÃbE[P\x0000(U¥µ¦µF+=$\x0010IL§£Ãaof0£íöÌv{n±XP¥ªÐõÞ\x0001P(U%¡ª\x0019Ú 
ñßÿýþÓßÿ½Ëw.\x001a«åõ¹¤o·>~þh¿Û[.\x0016æÞµ6X.\x0007­
¶½{ÞíLs\x0007½Çn·3Í'B\x000fÏ/ÎÎv..ÎCSÅ4w­5ËÕÊz³år¡U<>>\x001aÇÑf}îüüÜr¹ðòò¬ªÙn6Öë£¯ww>}þìâüÌïó£³­§GÛÍÖ§¯7ÆÛ[¿\x001bîï\x001f\x001d\x000e'ÃÀýÃó³\x000bççgÖëµãé`\x0018íÙÆþôgëÍÒõõ\x001fó\x001bÏOÏl¶KZë6w¯_ùýïÿàæËW?ÿüõfí\x001f~ð_þËAO_Øï÷ÖãDgçççÒ»Öoßk»ZyuqfÑ?ýô³Öa\x0018ìw{÷÷÷îï\x001eÜßÝIÊãó­ªr~¾ñø|¯0fÃAO7\x001f?é½ûî»o\]¿s{{§Ï1Ï³$ªVMUWUÊ 
^\x0001BRJSUzïTPZ"HJ¤)³*ªhUZ£µRUªRR \x0014\x0002\x0015@\x0014J\x0014P\x0005ÐhVj\x0006\x0008\x0000@¨Ò4\x0014\x001a\x0010($QÕ\x0008©H\x0002zïÒgÕRZ
´HQJBª@)@¨¢¨j(sõÞRU
BÐZim4\x000e£ª.U(\x0004!$P%H\x0001ª¤\x0014.	H\x0004
¥\x0000\x0000DU\x0001H\x0002º\x0002%Æýþèt<Y-\x001c÷2Ï¤[­VÞ¼yk\.LSw<Nºn\x001c\x0007ËÅBOl6[ãr¡$¦Óäplú©[®VZ\x001b<?ï|þüÙ4\x001d½zue±\hù8[­Öë­Åb4Ï'Ã>ÆáRz,\x000b«åÂ4Çb±r:\x001d=¿¼Øl6Î¶[\x000f\x000f~ùå\x0017¿\x0019÷ß¼q}}é?ýÅ¿ýñ/Þ½~å»i2÷£û;ûýÑ7ïßx÷vi16½O>|üä|»6´²üë?xýúÚÇ\x001f]øý\x001f~k·{öË/¿ê½LÓäîþÎ8._;\x001c\x000f¶g\x001bIüË?ÿÿü_þ³ÿþ¿ü£?þéO^\x001e¦t§¹»½½3\x000eÍj³6oÞ½µY¯¼yu­ÿõþa±²\­]\_y¸²Ûí<=\x001d½zueµ\¹¸¸rw÷`÷r°Z,m6\x001b77_¬VKß¾ÿÖÝíÃñhêÝþpÐZ³\\x000e½ÿößþÕõÕ¹×oÞ¹½ù"­PZ±\x0018\x001aTÁ B+\x0000D%º\x0006 ª(!\x0011HIHºJTèºêªVM\x0015 J%B)\x0001ô
"
(J!\x0012 ¡@DD\x0012\x0002\x0011¡(T5\x0005 @\x0015\x0002\x0005\x0012Q è¢±ÖJU B@ HH\x0008ÒE	
ª\x0011(U]tÉ¬÷Þ'I\x0017\x0001=Q:
RUªJ)$"REH\x0011@\x0000	 $¨RUH  \x0014\x0000J\x0012U\x0005 ªT\x0011\x0008ãwß~ël{f14''Ò©\x0018\x0017£W¯^Kè½ûå×Í}\x0012\x001dÑ3©q\x001cÐØn6¦ÓÉ8Ç£Ã~/m6k§ÓÉÜ»Å¸´Zn}ýúÕÝÝõfe\x0018\x0006ûýÞr¹¤º»¯¤¬7[û\x0017§ÓÉb1Øív...lÏÎ}¾¹â¯Æßj­ùæík\x000f÷ïìwG//;ÕhwØ£9Û9\x000en¿ÞX,..Î-+///~üñ\x0007_on<??«j~þù/\x000e\x000f\x001f>[,\x001emÏ·Ö\x000bw·wþôÇ=>ì,\x000bóÄ<u§ÃÉét4NZkjRñòôìþáÁ»×¯½yõJ
Å¸ðòøh>\x001dì÷qwÿèéå³ÝÁþ°7Ï'ÕÖoûíöÌ_?Z-×ÎÎ.lÏ.{ÏOÏ¦ÓÉ84ëÕÊb±°Ýn
Ãàe·³Ýnl¶k/Ï;UM4¿ÿýßØí}øô+U¡\x0019\x0017
BI\x0011@¡B\x0012Õ @BKi\x0015DBBB%\x0012Ò©VzïzïJPQ¨(\x0004j¥ÐC%\x0008A*U¥ª\x0001Þ£ªT+zªRE\x0015VJÓª@U\x0001 Pª
\x0004A)ÒCOD\x0007UBT\x0010@B\x0015\x0004\x0011tDOPT¡£D\x0008BÒ¥ÏzDDÒ)F\x0002\x0012ªh­TQ\x0005"¨H¢
 J\x0012I$Ñ{$\x0005\x0000\x0008¨*I@\x0012\x0000 \x0010	ãùÅÕjeNú<É<Iï¢T¡ñêÕ+sï¦ùäöîVï]'ÇÃA\x000fÓt4M'§i²X,,W\x000b\x0012ó4és·Ù¬]\æîø²·ZM./¯õ\x001e77_©²X­T
N§;ç\x0017k/»\x0017»çwoùt2N\x0016Áét2÷îâêÚ±sûðäç_?¸¼8óúÕkÿù\x001fÿÁOþÅÍÍ\x0017ßþð­\x001füÞýíåbTÕ\x001cGsb¹Z9&ûýÁÏ_ìv;U£¯ÆqÄËËÎñøèz¾òîí[×W>~üøæÝ[§ãÉ4M\x0016ãàËÏîîn­W[oß½µÙ¬->|r¶9³Ý¬-ÇÁóaï×_~u:ì\x000c-N§µÛ[]s}}å*ç~ýõõzíÛo¿3O'w·w./¯DlÏ/Y,¤wg­Ï77v\x0003iì÷{t\x0018\x0017KÃÁr¹4\x000bãä\x001f~ïßþõßdÚ«jª5¥$\x0005ªè(\x0014Fu\x0005(\x0014ª
\x0010R¢B©¢D\x0012I´¢
\x0014U4ZJ¡Z©*­Ó«\x0010 jª\x001aªBI\x0002¦ãH&ã8\x001aQµ¨*j V4MU*\x0012hè\x0008JB\x0002RE¥Kºy-FªJ\x0015(\x0014H\x0002B$Ñ{§OªJ)*\x0012
%\x0008	!s×çDµR\x0005ô\x001eªK\x0002
C5­5Õ\x0000 \x0004\x0012\x0004H\x0001"\x0000\x0000\x0001Q(UP(\x0000U\x0002\x0004("¢\x001bÇ½Ó|´?\x000c6}&\x0001Q\x0002ah£W¯^#¿üìññÁépðøôd·Ûyy~6Ï3\x0018Ázµôøø¬Usv~îúêÊz³r:\x001cG½w=±Þ,]l¦ÉtÌóI\x0015gW\x0017çæSw&ÛÍZÛn\\^§ÙãÃ¹ÇÕùÖ×ãÎÓÓ³Þ»¯·wÞ¾~í¯þð[Ï»ÇÇ\x0017«ÅÂûoßººº²{Ù\x0019ÿò«ûóGÿøÿ¨ÏüúëGÍÊñxrsóÕoû£ívíúúÚv»5ÝóÕjíÛoÿ;_>ôõë'çgV«¥Ï_¾úúõÆÍÍÍfg»=óøøàt:z÷öµWWn¾Þøzsãññ>N\x0007ÿ\x000fçØãßÿø÷ïÞyu}i:\x001c\]_{yyòë¯¿Xo7è\x0014÷÷·^]_\x0019ÇÑØô(Aì\x000f\x0007sãñä°ß\x0013æ¹[¾º6.\x0006\x001f?~´^­üþ÷ëñî³V\x0003A+P \x0006
\x0002bÐ
	B\x0015¨\x0002	4ª®\x0014)Ðª\x0019Û µF\x001a¨FRÒªT\x0015¢÷\x0019T5Qª5@©*$X,FÂ8.,\x0016\x000bªKAS­iÕ4E(%\x0015\x0012¤\x0010A)*:¤T
%=úÜ¥wPU\x0000\x0000¤KJUIº$\x0008!U
\x0000\x0012t.ézïz'¡@@\x0012I\x0004³VÔÀ04Ckzo 
JuT$\x0001\x0000DGGèT©*\x0000\x0001¥ª´V\x0000 

$¡¨*ñééÑËîÊ¼ZJ \x0008º¤T±^¿~K\x000f\x001f~ñôøè4Mv»VÍv³5K­5OÓ$éÎÎÎýðýw\x0016²ßïµ6X.\x0017NÓÉ<l6\x001boß½q<ìí^îo\x001f%q8ì¼~}ål}æóÍ§§ÕbéÕõ`ÊÉáp°X.\x000cm×+Sx>\x001c\x001dö{Ï>Ý|ñÝ·?¨\x001aÌóÁ«ËKUÝí×;_¾Þ:\x001e'ßÿ£óó\x000b77·æyvqqnØûÏÿù¿óã?úróÙÓÓÙ|Ak¼º¾t:íýó?ý³O¿úÍo~ãoþæo¬VK\x0012m\x0018lÏ¶ö»O>ImÖ®/_ùËÏõyöÝ·ß8;¿ðáÃ'ËÅÊþùÅ¿ýë¿Z.Fã¸tyumh§§gÅÊi>yóæÇ§g»ý¯_-WKOOª6\x000cæÓìl{æååÉÐÊn÷âp8º¸¼°ßï\__;\x001eOþúoÿÁ×/\x001eî?IV¨PH5Bª\x0000:¢\x0002DW\x0015\x001aJ:½ª¦\x001eJ3\x000c£q±ÔZ£:5¨\x001a¨RUJiU
\x0012\x0001]\x0012	©¦µB¡T\x0015H¢÷Y\x001b\x0006mèªJk%mT¨BRJ!@¡\x0010 $T\x0004I(\x0012>wÓ4{\x0017\x0001PJ!¤¤$]ÒIG£¨*\x0000
\x0012$Ì¹Ï ZÓªa"	"Õ5Mk¥µ¦:¥D \x0002\x0014
$HH$!H( \x0001ª
(Z
Zkzï ¡\x0004\x0010$ÆÍöÜz}f9®'=¥÷èa¨BIuÁÐ\x0016®¯®\x001d÷;Óáh¿\x0018m,\x0016Kó\¦i¶?ì\x0019Êrµ°^/oôiòôüd·?¦Y2\x0013ÕjiÐ<?î]ëéN§Û¯\x000f6ë×¯_9\x001eöÒãååY\x0012gç\x001bÅèy·×{\x000cÑñ0)Íñ8¹ÿõ}w~v¡2\x0019ª\x0011çç\x0017gg\x0017aðéÓgwww^½º6.Wö\x000f\x000f~ÿ»7înoýë¿ü»§\x0007\x0017W\x0017ÎV[«ÕÂÅùÆóóûû[5VÓÜÝÞÞ»¿¿w<N\x0016\x000b>}úèüüÌ0Û»;§ÓìÍw~øá\x0007ÛõÒw¯ãÒýÿY\x001b\x0006ã0{|½{TU¦\x001eß÷­³³KÃ0èóìùùÙÙv«ëþòá\x0017W\x0017WTs~va±\x001a¦Ót4\x000bïÞ½ññÃG_nn½ìvv/;gÛ3ËÕÊ¸\¸¸zåpz1Kaê\x000eº(\x001dÑ
(ê¥t\x0011tA:)ª\x0015\x0013U\x0003-j(qe\¬ÕPÔ¬4ePUª\x0002\x0014¨D4\x0012PB©j(À¬TIQ­Ó¨* JèB!\x0001\x0015$ @$Q)
R\x0012æÞÍódÎ,\x0015tP){t (T"T4UÑQ T:2Íegª\x001bÛÂÔ
eÎAR\x0012\x0004P* %é$Ò¡¢
T> $¥\x0000\x0014JPÕCÓ{Ìs$\x001d%	\x0002H"ÊxvvæÕÕ¥õØÔñYÒ%D\x0005\x0005AIX,\x0016ÎÏÎ¼oM§-\x0016³ýar<í19?;3\x000e#Ê¯¦i2Ï'/»ý~o1¥Õê(q\x0018[®VÇ£¹wÂóÓo¯¿³\x0018\x0007\x000f÷\x000föÞ»iÍ=Öëýaïp<çÙéxtqvn¹¼Ö§Y?\x001d¬×+§\x0013ûýj^½ºVU~úé'///Ç£ï¾û^\x001e\x001e=><øüùççg_>¶9?3\x000e£ÝÎn·÷õæÖ8\x000bçgçÞ¼}ëòüÜnwp8\x001cUÅrÔ{÷òòâÍ·zï.//yyÙ\x0019\x0017oIù·ÿø£»ÇGï¿ùÆ&qwwëââÂïÿ{ã0:\x0016Áãã£ó³\x000b»ýìßÿãüðã÷æ©{yÞy÷îÕjåp|±ßï´j\x0016ãÂ8^¿yc·?xyÙI8\x001dO´ÉÍ×¯Ö«Ñ7ß¨~4\x0014
AWh\x0014ÍLèPEJ\x0010\x0004Ðgzï¨*mlJ)´VÆqPC¡$\x0002ª)\x0000$EQ(U\x0005¨*	\x0000"Ñ\x0013A\x0001
\x0014$\x0002 !\x0002\x0012é1Ï]OD\x0012 @\x0017\x0011I'¡\x0002RT\x0013\x0010D\x0002\x0004D\x0017sbgSõD)Ã8\x0018ÇQ«#!õ $\x0005$z:éª" $D\x0012é\x001d%UR¥B\x0012½GÒE¤#\x000cÃh³\x0019%q8\x001c\x0000\x0000\x0008\x0014ãñ°7\x000eÚòL
MUiU
©\x0010 	ºªRC³^­\^^éáx¸wØ?¦$¦¹¦Y\x0012I\x0010ÃÞ4wmXX®"\x001e\x001e\x001e\x000cÃàüüÜv»ñúõ+ÏÇ£Þc:\x001d\x0007ýA\x0012///aa\x001cGÇÃÑzµ¶Z­\x001cO'p~vf\x001cGõÆùÙÖùå^÷vûd¢±?\x001eì^^\^^Z¬VÚ0ÚnÏ\]^æåjá\x001fþÓ?¸¼ºò²{qwçùqçúò7o^¹¸<óó/?ûúå³&þòó¯\x001e¼{÷Ö8.¬×+OOÏ÷¦yv{ûàöîÖt:yóö/7_ÝÝ?X®V\x0016«¥õfíöîÖr¹ "f=³ósû\x001b©zw8\x001c¬\x0016\x000bã8:;Û:\x001c\x000eÇ£Ãþ¨\x000cóÁétÔ{w:M}øðAïÝÙù¹q1x~Þ\x0019ÇsÛÕÚP]«êdP\x0008Ò\x001bE\x0019Q\x001a¡ D\x0017jQ}\x001e½E\x001b\x001a¢÷®§¢VP@P\x0010\x0004MUI\x0000 \x0010U$\x0010@TDÒ%QEB\x0001\x0000(%E\x0012\x0004¤HH >Ïæy\x0016\x0010!\x0000\x0011!PT\x0012R \x0000$\x0004\x001dsbgÓ<K+Ã0\x0018ÑÐÊIB)Q\x0014ª"\x0015I\x0014H"Jª$¡\x0003D\x000fI$ÑCOÔÜÍódgIT1÷HX,FÛíVïÝñxREUI¢ª"1n·[ÇãÑnlÆ6¨6
ª5ªI"¡'Jªf\x0018GgÛs=e<>=9\x001cæ\x001e\x000c(TÖ\x0006ËåÚ<ïÕ@ÂÓËãngµZiÃ`\x0018ÃáàêòÜñx4KI×{¬VKÃ0è½£¹¾¾Ò{÷øø £ÍzíñáÁåëW¶­y]]{ýæÒÓóÞ[\x000f\x000f÷6g\x001bsï\x000eÇoÞ¿w}}m¿Û\x001bÚÂîeg»Ýº¾ºöúÍ[÷w>}úäöî«íÙ³­jåòòêÎ¶[½w»ýÞëW¯ÜÜ|u{{g±\x0018­×+ß~ûÞÏ?ÿìááÞv{a·?yy~q~õZÇj½¶Yo|üðÁñtòøøèý»oÌS÷?ý/ÿ?÷·ç»÷ß{yÞÛIk¾ÿþ½õråùéQkô~²Ù¬ôLöûçç\x0017ã0x~~¶X®¦ívãééÉ0\x000cæyöþÛo=Ü=øåç\x000fþú¯~k\x0018Ge\x0006R
½ÐJPA\x0018\x0015!\x0015*T#DzW¦é\x0015¦ª$ô¹#ºnÐ\x0008ª\x0000(\x0008\x0002ª
 ª
T\x0015\x0006\x0008HB\x0000\x0000U
\x0001\x0000\x0000H\x0000$T\x0001@P ÷®Ï³ô¨*$ 	¢*ªJ\x0012\x0014U¢\x0000B\x0000\x0000I$D(]EÐÑ0NaPEæY×@U	 P¢\x0010\x0004DÒ¥^M¥$ WIkªyõÞ%ìö{ûýÁf³µXzïæ>[\x001a-\x0016\x000bëõÚ<Ïz%\x0000@±µæùeçÇ\x0007õúÊj\x0018$(\x0004s¢'R\x00051.\x0016./_Q9³ÝÁÃÃÅr´Z.´6¨j§#PEïÒ»$fåeäþÁr¹4Ï³ãñèt:Úl6Ö5½\x001bf8z÷î\x001b§ÓÑÐ\x0006ëõÊ4\x001dLÓlµY[Ízí\x001f¾5´ÁÓóÝþàÍëWJùéÏÝáp²^¬=ÏÏÌq{«Ö
ã°vÿä_>ûðñ3½ÿÖùÙÆ/w\x001f=<Ü\x001bÍÙvëîîÑÙÙÖÊýã£³ó\x000bûÃÁÜùù_}÷ý76g+ýËìpØy÷Í[OîîîiÍùÙ9éVË5	U\x001e_üæ·[oß¾õøüd·ßY.WÖëÃ´÷ùóëËKOO\x000fX.¶Û­a\x001c\x000cãè§?ýìææ«ívíÍÛ·Þ¼yCºÞgëõ\x001a1N63Y®¥ªRE)!Z\x0014 \x0012RRQ"E*\x0015ZT#³¦T¡
@\x0012U\x0005B$PªH \x0000(U$AT\x0015¤H\x0002@hP¤($\x0000\x0010\x0000@IB\x0007\x0011	Élî¤« \x0004\x0005\x0014\x0002¨R ¨R"B\x0005\x0001(\x0004ô ª¦jPmTmÐQ\x001bFNz\x0011U¦jÐj@	@R
H\x0000T\x0015Ö\x0006åÊ°ß;væyöôüäñéÑz½ÖÚqlN§É8\x000cË¥Õzmf»ÝdVU\x0000
ãùù¹³íþp'Ã@5Ð{GP"z®z\x0010]ª³³3oÞ¼±ß\x001f	pfãbi\x0018\x0007ó|"Ýóó\x000b½\x001bÇýþ¨µAï1fÇÃÁ4_^X®\x0016ZHãáÁn÷l¹XØí´\x0016Wv/{ËÅRÖkûÝ³>OÎ¶[>vûõNR^^
ÃàtÚ;ìæi6Ï³Íríl»qo¹ZúôùÇ§\x0017sçx<ùñÇïüá\x000f¿÷üül¿?èÝ~çåeç?¸<¿ð7ûWnovóõVkÍ¸XÚïvþÇÿÏÿ×Û·o´6z~ÙyzÙ\x0019\x0017\x000b»ÝÎv»u}yåþþÖîåÙo~ó[ÿé?ýo¼<¿øòå³³³sOOî\x001fnãÒz»¶G7_î|üøÙÃÃ««KÇÓl<\x001c\x0007»ÝÎv»qØíGûýÁ8¾Þ|1\x000cÍ·ß¾WUZkv/;×W×q¡ªk­;E\x0010\x0010BB¨.	$\x0008\x0015I$A\x0014Z+­
ª ª\x0000H¨*\x0004@\x0002A\x0000T\x0005\x0000\x0010\x0001D\x0012I$¨B	z¢\x0004E\x0015\x0004ª\x0002DR\x0008U¢K\x001eæy6&ó<ª¦\x0010\x0001I\x0008ªRA\x0015URE§\x0010AP
 H$Ñª´6h\x0006-ÍÐFÃ8\x001aQj2÷ÙÜ'½wUÖ\x0006C
D\x0012Õ
\x0000\x0000$\x0001ÂÐ\x0006«åÊz½q:\x001d\x001d\x000e{\x000fÆai\x001c\x0017q´mktÃQkÍ0\x000c6µ¹O\x0003\x0002\x0000Æ«Ëkßû<]i/Ïæ ]g½7)"HÊlÌ\x0002¤«b½\{ûæ±5/»gûÝAU\x000c#Wsmh^wÆÖ<¿ì\x001d\x000f'Ã0X­\x0016V«*vûôYt··wz­\x0016+at~~îáþÞjµ\x0006÷\x000fÎÎÎÁÃãõjíëíåò\x0017øýRkçþàééÑÃÃiêTY®FÕâêê\)ÍÖ<Oîoÿú÷63­W¯_©*üãOöû½ívm14Çytn¾XmVÞ¾ym½Zx~Þy~~qºíöÌ4uÓ|²X.==½è»½a\x0018Ãàp8xzzòôôè\x000fø×¯^)üé§ÏÎ6\x001bWöËåÂj½ÒçõzíÃOa°^­´j\x001cG§ãÉ86ÏóÉñt4OÓ4çîO?ýäx:yu}åòò
]tÅ:¡cVB)A
 \x0012T\x0001 \x0008\x0002ªJ>Oæ¹K\x001a¨BA\x0008\x0000U%	º\x0004$\x0000 \x0008\x0000zf=]\x0014U \x0000\x0000 \x0000\x0004$\x0000 %Bºy¦É<Ïº.B
=":E\x0005U(JÐE@\x0002!D$DtÕÊP¦TQ­ã`±\x0018æØgó<é½¨B+
¢*\x0004­DtÑ\x0012\x0000U\x0005`\x001cGÛÍÖt:9\x001eNv»~c\\x0016Ëq\x0018¬×+óÜ\x001d\x000e\x0007ëÕÊ8¶3éÝét\x0000cæn5.d\x0018Í"õÌú<2«*]WÊhÕMóLHº$X£««KëõÊ}»'Ý0ÎÏ¶ÚÐôi¶\®ìO³ãñ¤µ²X\x000eÖÌÓÉ4Tk\x000eûÓéd\x0018\x0007Ïö¡ãéäþáÉ0\x000c\x0016«9åùñÉÓã£wïÞ\x0019Ç¥Ç§\x0017¿Ü¸½»u8\x001eôÄnwÐ{wv¾AHU5«õÊùÅùoÿêÕÕ+øýïl6KéÝÓóÎ¿ÿÇÝß?z÷î­ÅØì-+WWç´Áátp?üî7atJüúë¯Þ¼þ­³íÖùÙöìÌû÷ïýË¿ý«6«ËK\x0017\x0017g^^%üôç¿ø|óÕÓÓ³ï¿ûÞj¹ôñÓG»Ý³¿ÿÛ¿1Ï³¤¼zõÊííªBìw/"^^væy¶?ìì\x000f;OOW¯^ÛnÖ¦Ó³³\x000bÏÏ;ÇýÞwß~k¹\x001cõ>y|z²\\x000c6«¦jP&D¡B\x0002¤"!E!\x0002\x0002*\x0012"zbg}î¦iÒ{Ô@D	B!\x0004H\x0002\x0000 ª\x0000¥  zfÑ%!Tk"\x0002QU$\x0000\x0000H"¤®÷nêÓt2Ï³¤KfÉ\x0002\x0000\x0001*(DO\x0017%" T K\x0011%hE¨b\x0018Å8ZC>wó<K\x0002""\x0018@!PèV\x0005\x0000¨*ÅÂf³µß\x001fì÷\x0007ÏÏ/>þb\x001c\x0017\x0016ãR\x001b\x0006ËÅhf§v´l\x001båÊºOæyÒ{\x0017À¸^¯ãÂ±Ïúa§\x0016£¾Xçn'©&\x0015¡b;"\x0002A@UY®W.ragé]\x0012I,W\x000bÛ³)qØ\x001fív{ÁrÑ-ÎVaÐçÙÓÓ³åbáoß9&ÓtrJWÊ4ÍN§ÉÙùîp<\x0018ÇÑáp°Z¯\^\êáÓç\x001bûýÑÅÅ¥iµÖ¬KqáíwqôðøàùåÙ·¯_éS÷Ë¯\x001f\x0014¦i²Ùn­W+ËÇÇ{«õÆr¹²Ûï½yû»Û\x001bçû½Þ»Õfc½Zim´\m\x001cöGåÊùùèòòBÓLÓÉv»õ»ßÿÎ×oü¯ÿôÏþô§?©Ö_Øl¶\x001e\x001f¤Ïvû£ÍzëååÅ<Çjµr:¼~ý\x001aÝv³µ?\x001c}úüÅ~¿³ßïõ^~L÷êêÜétôæÍkÅèîö«Ýnçõ·¾~½õüòâõ«këõq\x001cÌ§\x001dI\x0010A(é¨\x0012\x0011¡\x0008J\x0000\x0008sNÞ»Þ;B"¡

\x0001	\x0004\x0000\x0000T$\x0000 	è=\x0012ÒI"	!	P\x0000\x0014ª\x0002I\x0000@\x0012½GÒÍól&Ó|ÒÓ	\x0002\x0001UPª\x001aP%!H\x000fP
\x0010H\x0000\x0008U\x0000\x0005$¨*­5­5Ã8Z,ÆÅIÕNïÑ{P
ªRA\x0015	J)¥\x0000\x0000TÞ»$a°^¯;\x001e\x000f=??»¹¹±Z¯,\x0016£v~¦ÆÁá4ÑNË¥Õje&ûý\x000etãÅå ÷nOZBûät:ª\x001a¤J\x0017M\x0013Ý<ÏÒC\x0003@\x0016\x0011½wãbéâêÒ|:\x0019F±X.l·\x001b=1Ï]íKºÃáè4MæyvØï\x001dGÛí¡ÚjdÕµVæS·Zoã"X,ÖgKëÍÆé4{x|r8\x001eµqaê\x0007/û½\x0012ÛÍÚÕÕÕbpyyf½9óË/¿¸½ýj\x001c\x0017®®®=><úó±^/½~ýÚb¹Rû£õzi½^;?ßºººò\x001fÿñ\x001fö»½_~þÙ<uó<k5º¹ù"áõWZkV«Å8¸ùôÙÓã£åbi½^Y.\x0016àÝÛwÞ¿ïááÑÝí½.nïî½¼ì¼zõÊzµÒÑýý\x001f?¸»{0£$Ço¿ýÖÃÃyUãqv<NN§\x0007ûýÞ86Uô>yxØyxxòáã'W×Ç¥\x0015J\x001bÚØN'%ªº$\x0012:hªº¤¡K(\x0004\x0004I@\x0012ó<;N ÷HHBJïTE:PU\x0012\x0000¨*\x0000U%$\x0000zï\x0012zÒ;é\x0011!QU(\x0014\x0000¨*\x0000IT$ 	 Hº>Ï¦iÖ{WhU(D))\x0014\x0014($¨ @\x0002T\x0000\x0000H"¡§çY *ª©a0\x000c£a±´XMV«ç§\x0017I*\x0004A!@¢*ªP\x0002U \x0000Æq´ÝnN'óÜ\x001dGÏÏÏ¾Þ|µZ®\x000cæ¬m
\x0006ÇãÑ0q\x0018­×\x001b½ÏÇ#\x0018[.ãÈj+ãBÄ<\x001d\x001d\x0007­T\x0012e6§\x0013P
\x0005\x001eÞ;Øl6j³ÑçÙa¿§ÓZ\x0019Z\x0019åb°Z­­7+ÃÁn¿s<\x001e]]ØnÏ\x001c\x000eGUÍb9\x0018Ú`\-ì÷\x0007ÃÐ\x001c\x000e{\x000f.//,K§ÓÑ8.ÝÝ½øôå³\x001a\x0006ÕÂrµtq¶ñöõkWW\x0017Æ¡¹¸ÜZ.×¾ýî\x001b>òÇ?þÙ_ÿÕ_yÿþ[­»»;·w\x000fqåõë·\x0016_¿~µ\®|½½us{k¿?Z­W¶Û3//;77_Ýß?Z­VÞ¼~ãÍ+ÛíÖÕõ¥_~þÕÍÍWói6
>Ï>~üàx<¸8?³X\x000cÞ¼yeµ^óó3¿ÿÝoÝÝÝùòù³û×qqyé\x001fþá\x001f<<Üç*«ÕÊ~¿÷õæÆùù¹Åbr:\x001dõiòüôìx<úzsk8¦¯_ýúë¯h..ÖÆq´ßô>R£T'Ð)
Ñ	
)\x0004\x0000H¢÷.=zè}D\x0012\x0012 \x0005\x0000 T\x0015$ 	H\x0002H ´\x001a´j\x0004\x0002 	¨*\x0000IT\x0015H\x0002ªJ\x0012\x0000U\x0010½wó<ëó¬÷\x0000P]«\x0010E\x0015@¤H\x001a\x0005E\x0015T$RE ôÞM§Ói2÷.è\x0002¢\x0018\x0006Ã¸°\­­×GËÕ*ªR\x0015\x0012 E\x0005Q\x0015) ª\x0000Bô\x001eUe±X:;;7Ï]==çÙãÓ£åÍÂb1\x001aÚh½Z3ÏÇa5\x001aÇõz#Þ»ñùùÅÙv£6[CJ-\x0006ú¬ÏÓtRºÖ
%ÕÌô~R	\x0002Dï]\x0012P¡ZÓR5¨-Ázµr\Ã`½Y\x001bÇÑíýÞÜgÃ0ÚIâîîÞ<wËÕèÍWÎÏÎí÷\x0007ÓtruuéùåÉr1ºº8÷ÿb\x0018N¡çY«rvvæòüÜùvãúÕÝó³ãñäÕë7\x000eÇ7¯/ýýßýµÿùù'þó\x001f]_ÿ£³³\x000bÿö\x001f?9?ïÎ/öîúêÍëkíÊýÃ£ùàþþÑz¹öæõkm(«ÕB\x0012ÇãÑ4Mvû³óï]__9\x001eONÇd6\x000bÇÇ'»ÝÎ4|÷í{ÃÐÜ|ýìüìÜï~÷[ßÿðívåþ®îêêÒû÷ß\x0018f³YN·oÞøËÿìãÇ\x000fNÓdY2\x001bÚàoÿú\x000fN/_ï\x001c¹sw÷`µZJg·;Øl·Ë¥§§g7_nüðã÷ÎÏV¦c×û¬\x0002T@Q\x0008I'%		$\x0010HºiN'½Ï\x0006\x0004\x0000PUª
\x0000\x0000½wI@\x0002\x0001ÖaXhí$UV\x0005\x0000\x0000\x0000H$H\x0002 HJï1M³yîz\x000f¨BQ
T
D¤B
\x0004I¨"$\x0001I\x0004Ð\x0013sïöÇ£ýþà4Íz\x0004 PZkÆqa±XY-×ä$:	"J\x0002@\x0012\x0004QBQUªJU¡$@´Ö,Kgggæy¶Û½8\x001dOîïï,\x0016Kãb©µÑÊàx<i\x0006«ÕÊr¹Ä~¿3nÏÎ\x000cã6êÃ\x0012Ø={Ì}Ö@	z5É,=J@A\x0015J\x0015DUé½ª²Þnd^:\x001e\x000fJ\x0019®¹w½wÏ/;ûýAÕàúêÊjµr<<=¿8\x001eOÖ¥õzi³^\x001bÄ86ï¿ùF«\x0002o^¿±?\x001c­V+5Ãáàòü\j¬\x000bûæááÙ¯Ö«Á/_|óþ­Åò?ûóOvØ\x001f]]{÷îÚtÝßÝz|¼÷Ûß~o¹\ùãOÑ{|ÿÝ\x000f.ÎÏ\_»ùúÙ4\x001f¼yûÝáàáþÞñxðßþÛ¿øù/?»¸¸´\.­7+W×¯M§ÙjµòòòdhÍÝýÓ4yÿþ\x001bã8xýúÚÍ/þë/¿X.~øö{ûÃÞ¿þë¿fµ^¦³íÚ0§çgûû\x0007CkÑblno_¼ì^\^¾ruyéùùYáòòÊj½öpïl»qyyi¹XN'½¯´aÔçª\x0010\x0012T \x0012DH¤wDÒõt)\x0014ó<9Næ>\x0019ÒT/ª¨\x0012\x0014 ¡
\x0000$è½ª\x0002\x0014ªhã 
BABA\x0003D\x0012\x0000\x0004$P¤K$æ¹¦Éé4If= JURA\x0001Ò¢\x0000 è\x0000$æyv8\x001eí\x0007Ó<H\x000f"\x001d)QªÊ0ÆÅ(Ó¢(\x0014 \x0001T¡HQ\x0005(U¥µ¦µH.\x0001a°^¯Módîý~o·ß»»»µZ­,\x0017\x000bÃù9ýá¨Z³Z-­VkI7n7[ÑTEZ\x0014¢I5BD\x000f\x001d2k¡j ]tIPª

\x0005¨*IÀ0\x000cÚ8ªVÒ»60MÝón§'Î6[°]¯
ÃàTåzcîôÎ<wÃÞ0\x000cv»½\x000f¿~p¶=·Ùnì÷GËåÚñt2Í³år¡Ï³·¯_yzzòüøìññÉb¹ðþÛw\x000e»VkU£/·q´Þûøñívë\x000f¿ý­?ýé'ÃÁ·ß~ïp<ùËÏ¿Ú®·þþïþAkì^^üôç¿x~zVÅíÍW¯®­×kåÒ\x001f~ÿ[?ÿüÑ?ÿË\x001f}óþ³ó­ûû\x0017Wç¶Ûµ¡5Ãbáç_>8\x001eÒ»«ë\x000b?ßØ¿ì_º¾ºpv¶öðto»Ùz~>º¿{ðwÿ×T÷üòl»Ý:ì÷v»\x0019\x0017>|úäùéÉ¸XÙï÷æùäíW¹8?÷á×_=½¼øö»ï¥Ïî\x001e\x001e<<<zûæõje:MIÐE\x0005J¥TH"	¢\x000bºô.®KèÊ©LóÄL%¤Q¡
\x0000$\x0002IG$D\x0002´ÖP\x0000ª¨VÚ0hUZB\x0002(I\x0000$\x0001\x0004\x0005ªdF\x0010HbgÓ|t\x000eJôNWh(\x0002(U\x0006YO\x0004	\x0014 $J\x0011æ¹;&§y6õû,=¢$tPÕDéE@©jª
P(¥¡¡\x0014ªJÂ aÞ»\x0004H\x0002a°^¯¦É<ÍN§\x0017_¿~µ\.ãh³^\x000b\x000e§a(ÅÂz½5Bgsïæ¹k­I\x0010\x0000\x0012\x0010@$"$ ¨j ¡tf1\x000b«õÃÞ4\x001fUÍfíêòRz×çÙ<LÓIa¹\bÄíÝ½V««+y´?ììö;°Ýní÷\x0007Ó<és·^­U³³3ËÅÂnwðòòìõ7¾ýî;÷÷wÆqt<Üß?X.Wþò==?ùÃ\x001f~g\x001cvûýñäÿñ\x0017ãØüÕ_ý>Ïþòç½ÿ­>óæõ7¦ùàîî«íÙÍzãîöÖr\x001cý_ÿ/ÿgÿÃÿýÿiX\x000cVË¥§\x0007%8Nþð×m±\ûùÏ6\x000cååyçåig¹\Z,\x0007ÃØüòñ\x0017÷÷\x000fÞ¿ÿÞj}òéÓÞz½²\-<>ýd³]Ùn×\x0016O/~ùðÅËËÎÕå¹ËËsÛí/_nÌól{væ×_u:\x001eN'»û»;ó<ÛlÖ-\x0016Ko~ÿ£Ý®ì÷\x000f £R R³¤KHB\x0002®÷çÙ<wó\x001csïæ\x001eé¡J
\x0015\x0000¨\x0002\x0012 é 	¨*UMU\x0003I$AT\x0015Hè¡	\x001a  	\x0000\x0008\x0008)tD\x0012D»yMÓd&C\x0015¨*U¥\x0014\x0015ªB¡PEQ]	UHº¤«"!¢÷®Ï]\x0002¥÷ç.Ê4wó<IHæÙáxé$ª¢BQH©*\x0000\x0005¢ÐZÓZÄ04½wD\x0012U¥ª,Æõzm&½Ç4Í\x001e\x001f\x001f-\x0016\x000bÅRkÍjµt:ìje¹X\x0018[£ªô\x001e½ÏªH¢ªP(UHN¢ D\x0012P\x0005\x0004¥U¡ô\x001eZ3.Wa°X,-ÆÑ4wãb!\x001d\x000fGûÝ\x001eÝÔT³\x001cW^ìv{óÜ\x001d'¯_]Ùl¶aÄ4Ma «¥a\x0018\x0014$ÖëµËË\x000bó<¹¿»·\,MÓÑ~··ZoN\x000fZãwoýüó_\__yûî­§gw·w\x001aô~òáÃ¯^½zíÍ7ÎÏÏýÝßýÞb¹tûõÎép´Z,­-\x0017³O>xõúÿÓÿñçáéÑ~·Sýät<"\x001eýÿïÿ«ËK\x0017çÞ¼~íìlãpÜ{~Þ¹¿¿óñã\x0007Û³­øû¿s}ýÚ¿üË¿zõêÚ×Û;»ÝårcµZè8«Ñ»ÞüÓ?ý³±×¯®,KIWÅb±puuåßïîüÇ\x001fÿèúêÊ4M¬Ök\x0017ÖëÇG/Éùù+§éät|&]% º¤\x000bR\x0005*\x0011@RzyMÓdfz\x0014Òé-$J(ª\x0006\x0000D\x0012\x0000U\x0005ª
\x0003\x0002ªHº¤\x0003èéºhU\x0004E\x0012¥(\x0012\x0002P\x000eTÐ\x001egý4ëS×\x0016\x0003\x0002Òh\x0014(@$RJ)© $\x0012$z"¡UÓªIÊÔ#éæÞõDDÄé4Ù\x001fOjô@Q­T\x001a\x001d\x0005D\x0012PTÖ$Zk¡é=æyÖ{WUÚÐ¬V+é]f»ýÞñxrwo¹\Y,\x0016Zkj1:C3´fLïj\x0018\x000cC4UE$Z\x0011\x0011B\x0011¢¨RP
\x0000T$ \x0015PJOÒÑv±°X,ìö{A»¤KºÖØï\x000f²ÓaçxLs÷õõöÖïó£7o^[¯×Ç£§ÇGmµR58N ÷®ªÌs7Ï\x001dåp8¦û\x0007ËýQkãaïoÞyýê
>\x0007¯_½¶\®µÖ|ÿÃ{ÃP6¦£ËËs·wwàòêÊr1Úm\]Û½\x001cmÖ+?üð/_nüôÓ_ôósÃ0X-W¶»»;¯®®}÷í{/ÏO2Ìód¿ß\x0019Áj½v}ýÆýý³ý~r<\x001eÑ<>>û÷ÿw¿ýíï\x001c³s«Õh±<\x0018ÆÁõë+gç[ÍÆr¹ôõëWÓ4\x0019\x0017\x000b§Ód¿?ªëf'Ó<9_ª5××ÖãéhWÎÎ^ÛÕèpxÒû¤*"(IDÒ\x0005\x0000	I7M³é4N'óÜ%t!(BDU\x0001 ¦ª\x0000A¡\x0010I\x0010\x0000;s§5I$Q\x0004D\x0004\x0011\x0005(DD\x0012D\x0012½w£ÏÑçÎØ(\x0004¡T©*@\x0000A¡T5UÑ3K:\x0002"\x0008B«ÁÐ\x0006Þ#jÉÜCa\RM\x0010D)M5z\x0007ª
$!QU(­5I´Ö\x000cÃ U\x0015HB\x0018Û`µZ¶³S\x001dGûÃÁíí­åri\x001cGíü\x000cÍþpÔÑDï³Ö\x0006ÅB\x0002( 'T\x0011\x0008	\x0000¢HP(\x0004\x0004]T(¢\x0017\x0011Ue\x0018\x0006§é¤R`:M¦Ód&½Ïæy2÷n;âe·÷áãgm\x0018\x001cGUe\.¼<¿\x0010^^^<==9;?W­ÙívÇ£õzåíÛ×V«¥þü³¤¹¾¾t{ûÕ÷ßÿà4M~ùù/ÚÐ\Ûí\x000f\x0016Á¯¿~ðpÿàý7oýæ·?º»{ôËÏ­×\x001bÇÓÉþôi¼ÿæ½ª8\x001cnn¿¸»{pûõÞölëí·n¿~u<_8N>}þb¿ß¦nî1ÍGãbðþý{?üøþø\x0017?ýôg¿ùÍ\x000fö£OoôÎjµÄt\x001cNG_o¾JºÍfííÛ7æÓdgÛíFïÜ~½uwwk³ÙZ,FéÝr\x001cÐ}þüÉû÷ïmív\x0007Ï//./.\]¯Ü~åÐ\x001fTMHºh(	\x0011\x001eççn&Ót2O³>w*@$A\x0000@\x0002A\x0001 \x0010DB\x0012DÂ<wó<çÙP\x0005¨*D
\x0001\x0014\x0002\x0005¤# W3õtsõ>ë¢#º$@5U\x0012T\x0015º$\x0000 )IIH\x0002 	Hè½ë½k­\x0019ÇªÌ(BU#¥÷ç®år&½\x0008¥¤JB\x0015	\x0011Aõ¨¢RªÖa\x0018$´\x0016IÌó\x000c ahVëiÌ½;\x001d}ýzc¹\\x0018ÇÁz½\x0016¥v\x0007c»J)¥µ¦ª\x0002P\x0002\x0012 \x0014%(AQôDÒ\x0011\x0014\x0005P@\x000f¢WCTJ«2£>wÃ8¢\x001c'ó4Y¯V¡yz~6M\x001d\x000cÃ Çç_ýäÕë\x000b­5U¬ûl'}î\x000eÇ£ýáàññÑÙÙ\x0019Uîî¾ºº:·Ýn½}ûÆÝíÓiòõîÎ¯¾\x0018ÆÑaðúúJª<<>¸ýÓÅbéw¿ûQÂ<Í
×××=¿<K¡
\x001eõyru}i»¹°Ýù<ÝúøáÃþ`&ó\x001cïÞãË/nîîÍÓ¬ÕàÇ\x001fÔ3ë}¶Ýûzsç×\x000f\x001fl7k¯^¿²Þ¬=>>;\x001c\x000f¶çkgÛÇûG»ýìååÅn·÷ñãgßûÞv»1\x001f&\x0012»ÝÎf»µ\.\x0019f»Y\x001bÑ¯\x001f?¦£ßÿö7^TÓ´¶Ýlµi:HÞzft"t\x0012éÑ{×ç®Ï3¢Ð3û,ªJ!¨"*\x0008\x0000\x0000H\x0002 !!¡ÏÝ<Mjh\x0008¢÷®ªDª\x0008 A!\x0012z"\x0008H¢÷è½ë¹wÓ<ç.éB\x0014U\x0004 \x0010@\x0008\x0012@\x0001 ¡K¢§çÉ4Í6X,Zk(@i5Å<³ß\x001fÍSWJï\x0011%\x0002R"\x0014Q$\x0004= Z\x0000¥ª\x0019H\x0006IôÞA\x0012PUÆq´Z­MÓÉ<Oæiòøøh¹\Z.Æq¡µÁát2jM×U/U¥ª(R\x0014(\x0000\x0004ª¤\x001aJU\x0011JPªJPB\x0015\x0015@T\x0015f\x0014\x0008a0\x000ci:Ùï\x000f:Ë¥Ö\x0006ËÕFp<ÌSWÕ,\x0016\x000bI×{÷ôòl{¶ôîÝ\x001b}íw{sµ6¨*\x0012ã0X.\x0017ÎÎ¶ÎÎ6^,\x0016\x000bUÍÃÃÇ§gÓ$­8NÆÅ¨'n¾ÞØ\x001föV«¥¿ùë¿u}}Éb¹ ñðpçîî^\x001b\x0006ÃÐ¼zua³ÝØ=¿ØívÎÏÏMs¬×[ËåÂi\x001d§Ç'gç¾ûö\x0007÷\x000f÷>ühµn\x000e§½ÍzåÝ»÷ÎÏÏ=><Z-\x0017^¿~åáþÑ¿ýÛ\x001f\x001dG¯^_yx¸óüôhº§ççgC¡>wËÅè0MæÓäüâÜj½±\.ýéÏ?y~~tõÝ{7·w¾|¹õøüèñÕW×Wª\x001f?¸¹ùêÇ\x001f0,\x0016\x001c×j\x001e
­dîbüÿ	Â¯fÉÒ3=°\ïÞ®
\x001d:\x0013	\x0014P\x0002 /ÚFÍMÿõ1¶ÙÌ4ÙTÕDU\x0001J!>î¾¿÷µ
MG\x0012\x0012ABRjÌëIM-\x0006L(\x0000It·R¢TA$\x0008\x0000H\x0000\x0000\x0018®\x0000HPQH($\x0000$
\x0004)\x0012BN\x001b\x0019\x001eÆhs"(BA©B\x001a¡
D$ j\x0004PN[ÆÐÕfc·ÛZ­W¦iÒ\x001dUTªFì\x000f\x0007wwwÖS{|±Q\x0015\x0005\x0001RP(4)DBÒRªÊ4\x0015&óL\x0012I1$\x00010Õd»Ùèq¢ÇðÐ\x000f\x000e\x000f\x001f>Øl¶ÖëG\x001eYÍ³Õ4Ïº$º£* B
\x0012\x0000UE\x0015Uª¨Ä¤Pª\x0014PE\x0008 \x0008¨
)QÊd&óÄz½q²;1O³Ãáàx\,Ç\x0005±;Ùj"¥j¥»-}ðð°w<.&©&ëíÚv»µYo\x0014ÖëµG\x0017NOvNv;ýÞíí½ÍvëÃå·ï>xüø±i\\Y¯×ÆX\x001c÷ãgOÙí¶^¼|âþîÎéÙ©wï.ýå¯ßøîÛïl6kýAMååóç*<yòXwì÷\x0007ªÄpqq¡Ûû;'»\x0013ïÞ¾sqvæßýö\x001fý~âæöÎaÿàóÏ>òé§¯|xÿÞééÖçæÍë·Þ\x001cÞ{ýæ­Ýnë£NÏN\]ÞÈ´RÓÚÙé¹Ï?ûÌùÙ©i\x001c\x001b=âx\,cè\x001e¶ëëk·/ÌÓÆñØVóÆéÙ·ï?¸¸8·ß\x001füõ¯ßÙív¾úê+7·\x000f.¯®Ìæyc9¶h ­\x0013	ItZw\x00136«ÙzUT(ª.\x0001\x0000(¤T\x0005% ª&L\x0008\x0002 ªÔ<1M¢tSE)$\x0004¡ 
$
"¤I"\x001dItÑÃ2e\x000cë^B 
\x0004PU(I@Rh\x0011\x0000Q iA1X­×6»­õjm&UÑÝ(ÓTV«Ùj5{Øß[Ï§¦*\x0004\x0001"\x0001
Ði\x0012\x0006Ue&0My%D\x0012ÄT¥æÙn»Ó£õýþÁÃÃ÷ïßÙn7Öë³³s«i*Ó´²,-i	\x0012\x0010\x0001	U@*$"" \x0001\x0008B\x0008J	ºCíîÄ¼Z;\x001e®®¯ÜÞ¾uÿ »Z­Ö\x000eÅX\x0006UNOÏLÓìêòFX­Öæùè¸\x001c\_HÚ2Û[w÷÷^<îúúÎ7ß:==s8\x001cêqT<yñÒû\x000fï½ÿÁn{Âzvw·×}tuõÎ²ðÝ÷?yx¸óþòÚåõÕT\x001e=:÷ìéSO>5Ï³»ýÁýí¥Ï>ùØjµòç?ýÉqiö¹ó³s?¿þÙèÅíý­ívãO>öóë·\x001e\x001eîtÇõÕ­ï¿ÿÉãGO¬W[j2Í³/¿üÂåå\x0007Ï¿ÄîÕ§Oùó_þâáîÜW_|îÅg\x001e\x001eî¼÷ÎñxôòùK5O¾ýî;	ëõVÕìúêÎ4=Øn7_<µY¯ýøÃäcçç=y<tÇ~¿·Y¯Í«÷×vÍzRi\x0012	ItÚH\x001bYt\x001féXÕÊ\³RJ\x0008"J\x0001\x0008
DR\x0008H¨\x0002\x0000\x0000J)BwtGUÌó$!)B \x0004H"¡;DÒº[w\x001bÝËp\m\x001aE
¢ (2HB\x0008¢\x0010ID\x0012A\x0012It·å¸è1¬v;ÍÆjµ2M\x0013Ý A&ëÕÊÙé©ó³S«\x0019@$\x0011	\x0010$\x0008Ò\x0011L5ª\x0002ULSçY\x0012It·$\x0000V«ívk¡»\x001d\x000e{·77Þ½{k³ÙçµUiË2\x001a¡\x0000P@"­D	$ @I¨

¨\x0002 *\x0002\x0004Ñ
Ój¶YÍÖL\x001c#5YÅf½²Z­¬æÙñp´ß\x001f]9=Ù¹¹¹vyye·;ñøñýþ¨Ü\x0019MÍì÷\x0007WWW`5¯ÝÝ?¸½»sv~j·Ûa\x001cÛíõ­å\x0010ûû£ÝvçÑsÂ\x0018\x0007×7·>þø\x0013cÄ7ß|ãýåµÕzíùç¾úò3/=3¯&ÇexýþÒ_ÿö7ç'[ö\x000bï.¯½yóÆÓÇ=züØj»¶ôâOú^±4f=ØlN<zôÔýÃÞwßý`xðâÅ\x000bëõìíÛ·Öë­gO9=ßØïoõ8£~úÎÓ§\x0017^¼xîêê\x0012åx8V³ínëþ~ïêúÚj^Ù¬7ÎÏO­7³««K77×..ÎLÓd½^yôøÂáppïääÄ§}æo¿us}éå³\x000bÆ1\x000eBéDwë1\x001ez\x000cU-	$\x0012TH@\x0002\x0014T\x0001\x0002\x0000I$$\x0001I$$­ÇÑXª&	$\x0012T!@\x0004A¡Ð¤%$­{XF\x001b#ã0F£0	ª
¥@\x0004A\x0012\x0010\x0011@BB\x0012It\x0002"ènË²\x0018ÝV«õjm&U¥ªTM\x0006ójr~vêÉÓ'zyPè4\x0012@©\x0000I\x0004ID¤"ÚT³ª\x0002Ó4!I÷\x0004H¢ªÀz³±í¶aaY./¯¬×\x001bëõÆªGj2O\x0013UVU
B\x0002 ªRP\x0002\x0012\x0000
 DIQU\x0000 EQ\x0014j*5ÓÓSUåÑãÇ\x001eîî\x001d\x000f\x0007Ä$¦Bî£û\x0007ËX\x001c{q¿?Ø®×æÕÚz½±,Gû½ãáà§òôÉ\x0013\x0017ç;ëÍÚ'ÝÜ\çÇg~üñÝæÔÙé¹§O\x001eûèÕ3«ÕÆíõÃáÁz5ûõo¾öæÍ[ï>\¹¸8óÑGÏívkË8øpyãòêÖ÷?¾vzzî¸´~~íÕ«WæÍÖ÷ß~çêòÒÿíÿþu¿¿÷Ý·ßùëßþf½^ûíoçÕ«\x0017J\\;;Ûùþû\x001f|ûÝ°\x001c\x0017gg§v»­_ÿúï¼~ýÖííµëxÿþ³ÓS§§çÒí¯ýÎ£G¢ì\x000f\x0007-û£å°xxxpssãüüÜqY¬×k¿üå×Þ¼yëêêÒÅÅ#O>vs}åpX,ËÊ7ß|ãÕ«6ÍzkzôÄgO]xëp\Ä\x0010DéDwëÑ:­,Æ8\x001a=t·
P$QfD\x0012UF)$\x0004 H\x0018c±\x001c÷½yµ\x0016\x0004I(\x0000*A)$$\x0008I$-iI$ma,Ã²\x000cc´1Z\x0007\x0015\x0011\x0014
E\x0006	U\x0000(\x000e@\x0004\x0001@B\x0012Ýíx<ê1L[Ï \x0000\x0000\x0000IDATódgS\x0015Uª
 MU¶ÛÝÉÆþþ\x000cII"\x0001RJ\x0000\x00044¢j2M\x0013 Ti@\x0012Ý­»Á4M6µel\x001eú¾\x001d\x000eG\x001f>|°Þl¬Æ²¨*Ó\¦*©É4	%*LE"ÝT!\x0014B\x0005\x0002\x0008\x0015\x0010Pª
H\x0010

EHAÐ\x0000ìv;çggöÛ««+ÇãÁèAµª¸½»q}\x0013£c³;±Z¯í\x000f\x000bÊnYlv\x001b«yíôdëììÄÕÍ­³Ó3Ï<5Æb·ÝÚ¬:\x001cÖ­W\x001f¿TfÝ{éVááþÖ\x0017Ï\x001c\x000fùý¿úÍo~í·¿ýýqo·Ýº8?õþý[ggçno\x001e¼{÷Þ³'={þÌÕÕ×ïÞÙívNv[ç\x0017çÞ¾{ëòêÒ¸¿½SÓÚ»\x000fWÞ¾}ã_åpØ{ýú'××7Çáã?r{së§~2¯V>ÿìS}úãrôæÍ\x0007?ýôO>~äx<xúôªÙþü?=~t¡{¸88ÝîÜÝÞyxx°?<Ø\x001c7ªÊá¸w8ì}òñÇÞ¼~íoû«õz6Ft¿û»_¹¾þà/ý«ó\x000bíG\x0017\x0017¿øØzµöã\x000f\x0007Çã­$\x0012º\x0019K\x0011Ý-5\x001caY\x0016ÝÃÜE\x0015U\x0008U\x0000  T B$\x0001IqtØ?8.\x0007ÛDD´(\x0015
ªH)¡JR$ènÝ
ènÝmaYÚ²\x000cËh£[÷´$@ D£\x0005@$\x0001I@B\x0012I$$$1\x001c£1ª2M&I$\x0001DD\x0012=\x0016Y\x0016Ëá`Y\x0016\x0011Q\x0018\x0010h\x0000R
I$1F¤Ú4\x0015\x001aÀ4MV+$¨*Ý
æi¶Ýít·±\x000cûÞ»¿¿÷þÃ[«ÑÃ4f4Ó¤¦RUT\x0001\x0013%\x0008U  ¤J 
\x0000\x0010*\x0002\x0000\x0015(\x0005 T \x0002ª2O³yl·[§ggýaïx88äh¿?º¿{°9Ù:=ÝZM3UËÁÕÍ"9qq~æüüÌ¹²Ù¸¾¹³XÍ+oÞ¼õôéS\x0017úùçmw\x001bO=v~¾ux8ÚlN©)\x001e=>S5ùîû\x001f|ùåç¾üüS«ÕÆ÷ßëa¿§6nï\x001eZÍo¿ùÖqYúðáÒÍ\\x001e?}êæöÆ\x001fÿøG_ùý~ïþpôâåK\x001f=vssëòò½~úÙ?þìêúÎËW/\\{x889ìv\x001bgg'nï?zîÉ£SËr°gÏ\x001eùðáÚÓ§O¼|ùÒýý\x001dáöþÞ<¯{õê7¯ß\x0018cñøÑ#÷÷·6ÛW\x001f}ì\x001fòÇ?þÉ¯ó\x001bÇÃ°,yÞXMm®Éfµ´wïÞ[¯Ö6ÛSÇã=BÈÒÆhc\x000cK\x000feXÆQ!\x001dI\x0014T¡\x0000-(
@$\x0010\x0011\x0000I\x0010Ä\x0018Ã2\x0016ÝCÒ¤É\x0004@BD\x0014\x0002Ñ $ºcÖ\x001dc\x000cÇeH\x0004!¤BI")\x0012I\x0010	\x0004@Ò$ÆhËqèÕ4«@D\x0012I#e\x001cÝ?Ü»½½õpo\x0019g\x0012(A'P¥ HQ)\x0004@\x0002´AÃ¤ªTª2My$\x0008H"	UV«Ùv»µ,îáx8º½¹³êft¡0Õ¬\x0014BQ(EA¨\x0012\x0004A@©T\x0001@$@V*TP(\x0008$T)¥`´i^9=¿qê°PÅ¶ZÚ¦Y­fÍìd»±?\x001c=<<èe2Ïe»ÛYF«*»ÝÖÕõ÷\x001f.=}òTÍ+w\x000f\x000fv§gV«µívëÃû\x000fn®o|ñÅNO¶¶'[\x001fÞ¿w{së/>÷×¿}ã?þ§ÿêé£'>þä#òão½{wëâÑW¯úëÿêîîÁ«W¯¬V³ãXÌëífãóO>ñþÃ¥7\x001f.mv'æÕìßÿî\x001f|ýÕWt´Õ¼rÿppswt\7oß\x001acxþì)\x0016ÿöoÿêìôÂ¿ÿÝ?Úßßûÿüÿ¶§§~~óÖíÍ½Ó\x0013õ¨©ÜßÝéi}þé\x0017¦õjòèâÂýÃ?ÿéÏ¦yíùWÞ¼yíááÁ4MÞ½g\x001cÛgOãÑÏ?ÿd¤íNv~õõ/^¦,2å¸w8ì\x001d\x000eGe8.!M ¢\x0000\x0005\x0005­L(\x0004%	\x0000\x0000J\x0015Ý%ÕÔYL\x0010(©"\x0001I\x0010\x0014! EÑ1:ºca\x0019Ã\x0018QT&"AP¢\x000b\x0000@@\x0012\x0004\x0004$nc\x000cÃÐ©fSJÖié\x0018ãaqÿppwX¨Ô$&j\x0002@\x0012\x0014\x0000\x0010¢´defUTQU¦i2ÏA$$1ºUbRV«Ýn§Ç0º\x001da5ME\x0018cQ¢j\x0000¥Dª\x0012\x0001\x0010!\x0005*B\x0008 \x0011*PU\x0000*\x0000¥\x0010\x0005$\x0014nªtJª@UWkëy¦8.CØm¶NÏNl\x001d\x000fëë{¬ÌóÊjÞ:\x001cëë;ëõÊjµ²Ûnt·ÕjlçrqqâôôÄrÜº½¹õáÃ{gg'¶õzí§~¶Ýî<yòÄ»wñv¼ñôÙ¯ñ¥»Û[\x000fw\x0007\x001f½xa½Z©i¶=Ù1MºÕ<Ó±Z­¬æÓÅ×ol6\x001bgg§ÃâáþÞv³öÑG/¸¹½÷öí¥~üÉógO<~|áÝ»7^¿ùÑógÏ|öù§öû;5óGÞ_^»¹;XÆÑýý­×¯_{öìÓ³3U¬×kO>s}}åôlk·Ûº¼ºòáÃÛÛ{U¯¾úÊj5ù×ýO>ùØ'OÍÛÉãÇl·;ÿé?ÿ\x0017¿ÿßûò«/|üê#çç\x0017ºÃÃ\x0015adXÆÑá¸·ßï±8,C*¥B\x0001 @D)\x0014 \x0010Q@¨") *jÐ\x001dÝ­¦¢\x0000!\x0010:A$ÑÝ\x0012\x0008AH"Ý1,cXa\x0019-
%P@\x0012 H\x0007$$@\x0012\x0000	A\x0012IK·e\x0019öËÑè\x0006$Bî¶?,no\x000f\x000eÇr~va6*³J)QU¤T ¨*\x0012ªJÒ\x0012NKç	¥ªLÓ$ÂD\x0012¨*ó<Ûl6Æh£[ò`5M\x0013¢»\x0019LÓ\x0000U% $\x0001B @Q\x0000P\x0010*IT\x0015!¢ A$¨¢
Dt`1t§²Ýl<:d³ÚfNOvÒñæîûû½yµ¶Úì¬×[IyØ\x001fÕ4Y­ãd·urzf·Ý¹½½u²;±^­Ìgg.¯.­Wk_ýëë[ïÞ½S5Ùï®®®]]ï¿üüÇ¿÷?üÁ¿üÛ\x001f}õÕçþþïåÇ\x001f~¦ÛÏ?½6:Öû{SØ¬6\x001e=ºðþý{Â4ÍÆ²xsyéîöÔãGüúï¾¦\x0017ÝGçç;Ï>òèbg¿ßøôÓOüê¿ðîí[ûë7ÞüüÖ<Í~úù\x0007Ï/|ýË¯mN¶þëû?{öô7?ûäWNON¼ÿÞÍÍ
&W×\x001f<yòØ³gÏ<zôØ\x0018l6;'''^¾|æñ£sËqxóó[/_¾ôìù\x0013¯ß½öÙg_øòË¯üíoßÐ¡e,îï\x001fô2f\x0019m\x0019­»-c8\x001e\x000eÇ!¢RJI\x0001 A¡\x0004U\x0005\x0014RJD@BR\x0008	¡Ó\x0008\x001a\x0001\x0011BP PîD\x0012IH¢»1\x001eÆX,Ëâ¸\x000c="\x0002\x0012 !H\x0002¤%1ÆÐÝHH\x0010H¢ÅÒÃápp\x001cC§EF$\x0011P:q8.î÷{ÝÈ¬BQ¡\x0014A\x0008$\x0004\x0005"M`"\x0010mè¦ªP¦©LÓ\x0004çY\x0012I\x0004U¬V+»ÝVÒÆ\x0018VÓT¨"HH \x0014\x0002$ª\x0010\x0004EU©B"$\x0000(\x0000\x0000D)\x00101)Ut¨Bh­j\x0002AÒJI\x001atªÙùù³³3Éb£ËK777åÈ\x0014ÉÎ²\x001c¬×k«ÕZUé\x0011U%=ÜÝÝ*è¸¾ºÑ\x0019áþno»=1Ï+ÆàþáÞá8T­ÜÝÝeðúÍ{··÷~÷ÛpñèÜ¿þÛ\x001f\x001c\x000eÃ¼ZÛï\x000fv»­yµr~~fY\x0016·wwÎNOM\x0013¿ûÝ?ª*¯_¿öí7ßøßþC[¯'O\x001e?òñÇ\x001fkrq~áÍwþõß~ïòò­çOûèÕGeÑÚýÃÑzuðý÷?xûáÍfíÕËW^½zåÑãs«ÕZw¦Ér<úþûï¬V\x001b¿|æùóW¾ûî\x001bççç¶Ûµª2Æb½ÙøÝoçÿù¿û/ÿõ¿xþü©¯ñ¥ínëË¯¾òÙÿ/þüçÿéþ£O>þÔñ¸qD7éÂiEµd¥»\x0000A\x0008(\x0002T\x0001	\x0000)(	D\x0005"Nô\x0018Ò-i\x0014\x0000	\x0008\x0012ª
\x0004-NHZ÷0zXÆ0Æ0F[z1ºEQ\x0013UR%¢ª\x0004\x0012\x0004\x0004t7Z\x0012I$DwKGº-c8\x001c\x000eÇ£î\x0016\x0011!-	@DQeôððpO·Ç§³d H"\x0000$\x0001\x0002\x0001I\x0001H îÄ<OÂJ\x0015Ó4énPUj$MSXÏ+½ÙZ¶G«yÑª¨\x0010
J\x0014\x0010\x0000\x0012¦©\x0004I*5M(\x0000B\x0015¨* \x0010ª bRU\x0012TL"iQ(D\x0015U%	U¦i2Õ,=\x0019ËÑ\x0018­Ív6Me3OªbôÑÉfëädçþþÞñx\x0000«ÕÊápPÝnîî\x001dÆ0Æbf77·º\x001b\__º»¿·;9ñp8zØ\x001flÖkI\x001c\x000e\x0007w5éL^¼zî/ß|ëæö½UÊv·5Mûû;'»­Ý'Ï¾ôÃ?øé§\x001føÍ¯íììÔñpôîÃ\x0007§'[ÃÞj5;=;³ZÏ<}âòêÊÝíÁj¾qq\x0011'';\x001f>\zñâõzíOþFMåË/>÷w¿ü¥ªÉz3Ùï÷þö·¿:;;óâÅ\x000bß|û½ý~ïúêÚz5ûùç×~øá\x0007ËX<öÌj\x001cG/_~äï~ý+¦øöûo½|ñÜG\x001fÅÍÍµ\x0017Ï©ßÿËïýë¿þÁ×_}é£WOiºCMæye³9³^X­Ntè\x001eR³\x0002\x0008\x0014$\x0008J\x0015A\x0012 \x0005HB"¨*Ó4a$R\x0002\x0012ÐiIëBº¥Û\x0018maÅ2e\x001cõ²\x0018=¤Z\x0015Ó4)\x0014\x0004\x0000
@\x0012	I¡%D\x0012ItZ'z\x000cËáèx8J·
I(¦*IiÑ¡LÖ«ÍzåááÞr¸7Æh1\x0001\x0005\x0005$ \x0001ª\x0000\x0002ªÊ4Ñ\x001d@K\x0018\x001dªT·ªRUæy\x0004¤È\x0008"¡ªlVkc·³ª¤J¦IªRJU)%B\x0000
H4:¨\x0002UB\x0004\x0005(\x0000\x0010AU¨\x0012H\x0008\x0000@\x0012TIÐÂ$	SÄdªÉf½õèâNYß­\x001dö{5\x0011\x0014z´ãñh¿?º¼¼´,§O¦Iõvc3Íå`'áööÆv»Ó¡Ó\x000eÇÅÃþÁ·^½òw¿úÊË\x0017OÝ\ß{ÿö­1\x000e^½xéx»Û;ÃA÷ââìÔùù¹\x000bÇ¥%³Õ¼ñöí;ÿýáUMTélw'Vëµ«ëk··7ÎÎO\<ºðpôæÍÏ^¾zæììÂ\x000fwî\x001fö\x001e?~jô°×Ç£ï¾ýÆÓ§Ï\ßÜxöìÇ/T­l6;§§§q,>|xï\x0017¿øï¿ÿÞ·ß~ëüìÜf½ñäÉcÛÝÆ<W¯^y÷î½õjãÑ£G\x001e\x001eöîîî<}úÜÿãÿùÿò\x001fþßÿÁßþúíÊÉne£ÑGa½ÚJHJènI\x0010I)\x0013$ 
HH\x0004\x0014
\x0000À4M¦y6YU¡$%	 	@Ö\x0010Jt"1e\x000c£[aY\x0016Çå¨{QZU© @D\x0012	IKH\x0002HH"¤%-$z´ýáèáá`t$\x0000I$DÕjíüôÜÙé±ìEt`B©¢
M'`J\x0012\x0000\x0000\x0000ÓT"(It1\x0008ó<£T1M\x0013H¢;H¢¦²Ýl­¦i\x0010¥ªTAÐJ
(\x0008A¡$H¨*U\x0008\x0004M\x0015U(	ªHLª\x0014(@\x0015\x0005H"Bè\x001e(5ONÎNMëÝÉÎû÷\x001fì\x001f\x001eìv;gg\x0017¶Û­ûû\x0007÷÷÷¦ir8\x001c¼~ý\x0006åüüÔÉÉ)EU9\x001c\x000eöÛÛ;£c·ÝØn¶ÎÏ¶¦iòã?ùùõ\x001bO\x001ezùâÃþ'ùëß\|¸ðéÇ\x001fûìýüæë«+½,6ëµ'O\x001e9Ùí¼ÿpé«/>óóÏk÷\x000f÷®nïì\x001f\x001e¬æµÃ±½}÷ÁãGg^¿yg½Y\x001b£Ú?<Øï\x0017W×îï\x001f<~ôÈjÅénç°?:9=±Ù¬ív[#\x001cÓ\x0007ó¼quu-¹·]o¬×³û\x0007¥¬7kÛÍÆ¿ÿÝ¿szvJy}x÷\x0016³gOû§üýáÖ\x001fÿøG¯^~ìâìLª}õÅWÖÿëÿê?ý§ÿèa´Z±,åx´,CBjÂ¤G$Dé H\x0002\x0000¤@\x0012&$\x0002¨\x0000AÒ j*©\x0016\x0011­ªb*Ñ(R\x00122HBhÑî´\x001em,íx\ì÷GûýbV\x0013sAIJ\x0007$è$F$A\x0010\x0004maÿð`x4\x0015\x0000	Ý$!M3O³Ó\x0013Ï<vwmfT0©\x0014\x0015ó<IRU\x0000\x0000 2Õ,NKZ[\x0010PU(I@ÕdÂ\x0014It7¦Éª¦É¤iºK)ª\x0000\x0011Ð( E¥\x0014æi&
(\x0000$QBÆ\x000c
$%¡
\x0008(\x0005($\x0001Q\x001a´R ©©ir²=1¯Ö¦ir{sCb½Z©©\ßÜXG''§»»{77×®®v>yììì*\x000f\x000f\x000fjí÷GIY­ÖînïÍ>~õÊÍõ?ýéO\x001e]{üèÂ\x0008¦rs{ëÃÕ\x0013O\x001e?r~vêýÛ7¦âþîÎX§O\x001eùùõkï/ß[­6¶«µªÉTX<ìïÕzmg÷÷{Ïw;¯^½4F[¯ËÍÍ­Ç{Ï?õÃ?yóö­ôd½ÚØlvÎÏ/ì\x001fîmÖk÷û{\x001f.¯½yýÖíí­/yüäûû½ãqqssC\x000f»ÍÆn»sssãd·#åÃ\x000f½X{þü\x000f\x001fâ¿}k\x001cÛÅ¯ÿÎÍå¥÷g?ûüËOíÿÎíõ{ûkËeÄr\x001c\x001eö\x000fj^YzènéèFE2IJ	U !¨\x0006\x0008H\x001a$4ZP:­³z¦&A\x0005hTè\x0004!\x0016KÇ\x0018­a,ÃqYì÷Ã~?tS5¦¢HP\x0015I\x0010D\x0012@$$$Dw$´¤u·eY<\x001c\x000eÇ\x0005¤H`B\x0013\x0012º#$Vëó³SÕGsM U\x0015JTE´R¤P\x0000\x0008)Ý!$-Mw¨\x0006ºÔ4¡T\x0001Ue&Zu©*c\x000cÄªæÙ\x0004\x0019R¤0ME¤$D¡¨PÁDURJ)\x0005\x0000J	
ªh
ª @U\x0001EP\x0000\x0001 ª@A\x0001 Hhe
ª¬çÇ\x0017ìN<Üßx¸¿\x000cÓj¢¸¿{po\x0019q·?ÈåÑqzvb^­\x0008\x0017\x0017g\x000eÇÅýþàôü«ëKW×W<~bYâêæF^½òë_}íç×¯]^^¹8ØlVÎÏN½úøc}\¼yûÎf½öáröúí[\x0015fqÜï=Üï=äéóg./?8;=ññ'\x001f\x0019Ëâ°ß{xØÛl6¾üâs¯=õîÝ;×××6»\x0013ûæ{=\x0002ÎÎO¨òãO?»»½5Ï\x0017/^¹¾¾q}sm»ÝxôøÂ\x0017/¼~ýÚÃÃW/_zýúgßÿðe´ûû;ÃÁ¼½»|g{²³Ýn}ýõ/¥'ùëÿÄ'Ïýðã\x001bæ¤­V\x001bvgÖSËòÖaÙ»¿¿³t»8?q<>´$¤(¢1	
\x0014¨j\x0000A@\x0010I$!¥CÍÓÊT³¤t·®É¤QdF\x0011:´$H¢\x001e1ºu¢»\x001d\x000fÃáà¸,R5S$\x0004\x0000H\x0002(´$î´$ºcXvØ/Ë JIB\x0012\x0011Ý­Ó(\x0011ª¬æÙj5SÑiªT1¨I\x0012)ªL\x0000\x0000H"\x001aÑÝ"1"ÓBªÉ4M¦i2UÉT®(\x0003mtÊ¤¦É4ÍjTRJ©*\x0005J)\x0005)RUf¥\x0000* ª\x0000¥\x0014H2)\x0013J\x0002T\x0015\x0005\x0004\x0010Dî$
\x0005PTBÑ\x0018\x001dILÓl·Û:?;7M1\x0016ÛÍÆf³v8<¸¹¹vusã8\x0016K·±´»û\x0007·wwªÊ¼:¿8£Ê¼^[¯·F\x000fÛÝÆ£3§§§\x001eö\x0007·7×>ÿìS\x001f½|a¿ß{Ø?xx¸÷öÝ;ózíÕ':?¿ÐÝîï÷¶S\x001f=ñèüÜÉvãã_©³ÓßýÓ?8=;qçéÓ'¾øü3»Ý?ÿå¯^ÿø£õTÎNOÜÜÜù·?üÙÕõ­ÃÑõí­~~­\x0013\x0017\x0017,KçµíÉ©$NNv^<j³YçÉÅÅ#ÓTe±Ýî,ÝÞ¼yk»ÙøùÍ\x001búËmv;IÓíââÜßÿÃ¯]\<ò_þÛ?ûæÛ¿yxxðæÍ\x001bÐ)1{ôø©Õjíx<Úïï½ÿðÎû\x000fï,ãHZ% $¢\x0001\x0000D\x0012IH\x0008IDtZÐ\x0015\x0014UÊ¤L\x0012º£\x0013	BDÒ:D\x0012ÝÑÝÒCwë\x0011c\x000cË²8\x001c\x000eÇ£±\x000cH"Ý´$\x0000H"!!	"$HZ\x0012I$1º\x001d\x0007\x000f\x000f\x000fÆ\x0018ªÊ4Mj*AD§uZ\x00124iÑ¢u·îF@BÕ¤jRUªÊ4M¦iRUªJU©*R\x0000 
H3F\x001bc\x0018c\x0018c\x0018c\x0018cèJ©U¡è\x001e¦R¤¨É4M¦©TA$PJ)RPQ\x0000*@JU©*\x0014*\x0000$P$\x0004H$A$\x0000Q¢BI)P ¢\x0013&¬V+»\x0013»\x0013ójvØ\x001fÜßß[Æ¢¦RÓ¤ª\x0004ÝÑ#t\x001bË°\x001c\x000fno®­Ö³\x0017/Ûm·eñüùs/_¾tuuåúúÊ\x0017_~á«/?7cÂX»Û;ój¶Ýnív[év{}íìôÔ£ÇO<ñÜ³çO\^¾ñý÷ßº¿¿³,Ã·ß|ç°?zòä±íÖv½ñã?\x001bá¸\x000cÇ\x0011?þô³³ó3ójåx<:\x001e\x000eîïî¬×³y\x0005ýÞj=yüÈ«Ïîì÷\x0007Ë2ìv;ÓT\x001e?~L×ïÞZm·?îå«WÖ«û\x0007WW\x001f|øðÎÉéÆßÿýo<~üÄ?ý`½^9;=3£ûû{cÄj½óòå'VóÖ²,\x000e\x000f\x000f\x000e½î¦ \x0008\x0000"\x0012(I$D\x0012D:ÒQAÂî6ÆÐÝ\x0012
\x0010\x0011$¤£»u·înIK"$º£{\x0018£ÑÆr°e9\x001a½F$@\x0010I$Ñ\x001dIK"îH"îDwëîv8\x001eÜï\x001feQ¡ª\x0014$NtG\x0012\x0011It\x000fÝ-\x0004	H\x001a&$º[wK"îDwK"\x0001\x0000 ;Æhc\x000cË21\x001e:\x0000Hè1L¥*©¨"\x0000¢*¦¢\x0012(\x0011Ñ	PT\x0015¨*\x0000UB$¨*D\x0016DU&\x0003­*ªJM¡ZU(ª¢4Ú$ª©PU\x0014ÑÑbWv»3Ûíª2Mõze³YÙm×ÎNOØnÖyTØ?ìéa»^Ñm
\x0019Ãñp4M³á«/>óäÉ\x0013ÿüþ\x000f¯ß¼ñêå3¿øâ3}òÝfçÍë7Þ¼ycµm7kUÛ®Úv³r\\x00165¯\x001dGó4Ûï\x000f®®o-K»ººõúõ[=â°ß{õò¥ÝéË;]³Û{Iì¶['ÛÓÝÖßýêk}úåpðøÑ¹ýÃ½ï¿ûÆ§}úÉÇ>ýø#\x0017çg=|óÝw¶Û­gÏzüøO>úÈ³gÏ}¸¼r{sçt{JøpùÁ´}xÿÞ?ÿ·ÿ.øû¿ÿ{ÇÃð?~ÿ/\x000e\x000f\x000fÃÑ\x000f?|ï»ï¿ó°ß{ôøÏ>ýÊjÞXD\x0004A\x0010\x0012I\x0010% îH"$\x0012:&!\x001dÉ^ôX^$Ê$¡C\x0012Ý-iIKZÒ:C[tZ\x0012c´1Ñí8å¸XÅèFjVU
Ð\x001dI$´¤u\x000fÝCÒºÛ\x0018Ñ\x001dIt·tënciãp8\x001cu£&eBè´înI$´$H\x0007P(A\x000eABDwënIt·1î6ÆDw\x0000\x0005ª
Ñ\x001dÝm¡{XÆbYÆ8ê\x001e !Í\x0018m\x0005UE(T\x0014PU$"\x0008U@Ñ\x0005\x0004¤\x0000\x0000\x0002\x0000\x0008¨*\x0000)\x0002\x0014\x0000@A£@ **\x0004PLE\x0000 \x0010J¦Ùv»óäé\x0013éáþþÎõÍRVëÓy%\x0003Ìóäx<Øï\x000fVëµívcµõ\x0018ºãììÔáp íã?vs{ëûï¾wq~æÙ§>{¡»\x001d~ØÛ?<\x000c}<8Û­<¹xá°ÜYzåÑãÇºÛÇ\x001f}ªëëk»S\x001fúË«KgïNHl·\x001b»G={îîþÞýýõjåòÃ\x0007Ï=õÿð÷?{l9\x001eúê«¯üí¿ùöÛo¥\x0017=\x0016?þø³ós'Û\x0013ó¼r<.öûÓÓS\x001f}üÊW/½yóÖ_þügó4{õê¥ã8¸¾¹ñâù3oÞ¼7¯ï|ýõ/¬×kÿý¿ÿ7ÿá?üoÎ/ÎnUåêúÚvZùä£Ïüã?üÎåÕµãþ`E§\x0005¥H\x0004DP"i´\x0004F)$HZ÷´$¤¤1\x0015&D\x0004$AH¤c6F\x001bc\x0018cq<\x000eÃp8\x000c£Y×dfU\x0013 PE\x0012I$Dwën		ÝÑÝF·t\x001bcØ?\x001c<<\x001ct©f5Í(ÝÑÝ2¢;z´ÑÑÝÒm6:Æ\x0004H\x0008@\x0015\x0002\x0012 ª\x0000$\x0004PhI\x0010U%	"î\x0006Fi\x0008It·²J¢&jP*\x0014)\x0000\x0011
JB\x0002\x0011U\x0000\x0000\x0010\x0001	\x0008\x0001\x0013i(4Ú4M\x0012@
¢\x001a¡HJ¡B@	ÕjíÉö±Séáõë·.¯nì\x0007m8Ùn¬æJyØïÝ=<Ø?\x001cÔá`ïìNì¶[§§;I»¸¹¾vssëâìÜ<OÞ½û`³ÙyñròâÅ3ñ¹Û»\x001b?þô¹
Ý}{tva³^ûë_ÿæìüÄíí½o¾ùÎG\x001f½ôégº¿»óý\x000f?Høå×_{ÿö­ýÃ½Ñ§Ùj½6W|üñ+c9úæÛo}öÙçÞ½çÝ»·ÎN¶Nw\x001bÉâÃÕÕzçÙÓ§>ÿäcïÞ¿óã?ùäO\x001e?}n=Ï®®n\]ßXgO^\x0018Çá¸,>ùô\x0013û½ÝÊï~û\x001bg§'þ÷ÿø¸¹}ðÉ§\x001f;;;u¸¿ssuít³ñ÷÷\x001b2|÷ý_\x001d\x000e\x0007K·NT¨*\x0012	
ZÒ"\x0002!	)(\x0012I$$tÇ²,F\x000fë ´J\x0016HI"!!)II¢»u\x000fc,ãâxlÇc,£u7¡î\x0018½è\x001eª&Ð\x001dI$D\x0012ÝÑ$H¢\x0013#1\x0012¶£û{w÷÷ªLJB:Ò¥3IJD:º£G\x001bÝF·Ñ-Ý¤\x0002\x0008Uª&I@\x0012Ó4©*ÝÑÝ(\x0004\x0005(\x0014Z\x0012D2IÒ£%1º%-a½ÞX\x001dÍz£LR\x0011\x0008ªR"\x0010
\x0001PÊ¤\x0014U¦©\x0000\x0000U\x0013A\x0004TR(%\x0002\x0011((\x0012 P\x0002I¨\x0010(\x0005)D\x0001$`ªÉjztqæÑù¹×oß{÷áÃa¯DÅqtyuíæî\x001e\x0011±Ø®ï¼|ñÜÉn§'\x001fKøþ»ï<{öÜ\x0017_~é\x001f~p8\x001cüðã~~ýÚçÏ¬æÙ\³\x0012W{«õÎjsâîîÞþò«Ë[ÛËµËËk«ÕÚz³%åääTÂË+û±ØlýßÿÞÍíÞ4Ïj\x0014'g'½ó³\x0013÷w¿t}}ëúêÒTl·[çg§Æh·w\x000föûï¾ÿÖåå'O\x001eæÙå\x000fv»­ôðèÑ_|õÿúÏÿÃ_þúWgÿô÷~ý´Û­½{ûÞþaïêÃ\x0007«íÊ«W/ýûÿïüþ÷¿÷üçÿêé'~õÕ\x001e»¿¹2\x0019þé7¿ñâÙc5µ\x000c"R
@\x0015H\x0002t@w\x0010j"!HènÆ\x0018z´1ZwënUN ¥¡$\x0001	I$ÑÝÆ\x0018ãÑ²\x001c\x001d£ãñè°,Ñº[\x0015
îènÓÔ(ItG\x0012ÝÑÝº[ÖÝÆhc´ÎÐÝÒ1Fì÷G7·wîï÷\x0004L\x0015´îaÖ\x001déè´îè\x0011c´î6ºn#1\x0003\x0014¥(ª¨¤&	ÓDw«*DU@wK"	\x0000H\x0000¨*c\x000cc´ÑÃèÄj^W³Õ~k&5­D©"¤ÁT\x0013F\x0012\x0000U¥PU(\x0000$ª&s­Ô4\x0019iIT* 
¨ (¡\x0000\x0002\x0014ªª\x0002IT\x0001BU)\x000e&(I@\x0000%\x0008b=O>yd»Ý8?ÛúpuãêêÚÍõµ««\x001bûýâþa¯SRB:nïî­V³d8995Mi5kíêêÊÃþàþîÎýýx÷öõ4«âç×ïmOÏ=Þn¼¿|ãîîÎîdggëÍÖ4Mnîîy÷Îr88;=±^­üÛ¿þ«_ýê\x0017ÎÎ/¼}eY\x0016gg§ÞßÞºzÇv]¾øü3I;\x001eî­VÝnç°?¸»Û»¼ºru}ãúöÁf½vwwëñGvwc5»»[\x000fûÝÉ¹Gg~~ýßÿË¿8=ÙùÅ×_¹¾¹ñîõ\x001b»ÝÚa98?{ìÕËWö_úpuãü³í¼ò«/?3MåþæÚtvæ\x001f\x0019=¬j"\x0011\x0014(t\x0007@\x0012\x0010\x0011AKBHÑÑm&!î¨\x001a\x0008!!	¤11,ËÑ\x0018Ã²,öûýýáà¸\x000cÝ¡Ê4ªR
¤@wt·¤uGwënÝm¡»u\x000fÝmôÐ\x001dcû£«Û{\x000fERjÔT$z´îaYe\x000cÝ­»ÑmtëîÖÝº[*ª"ZU$ª\x0000¦	$\x0001U%i*ÓTÆ\x0008H¢»%\x0001Ó4çYwK8.ãrÔÝªÊ4MæLV·7¦i¶Þç\x0015HèP\x0005B\x0008PUªJU$\x0010\x0001(ªJ)ójefÉ¢{ ª
¨HP¨B\x0000@U\x0001\x0001ª&\x0000*¥"\x0004  \x00105\x0015\x0010 Ý¤­W+ÎOm×³y^¹¼¼òþòÊÕÕ-5kã\x0018VÓd³Ýærwÿ b³^Y¯7ªÊÅÅ¹i\ß^#6Û\x0013O>ñþý\x0007ïß¿×«Éf³±=ÝY²8\x001c\x000f>úèÕzöp·¸¹¹s<\x000e'§kÛÍÎõõ«KóG¯¼xþÜ~ÿàúòÊ<M~õõ/ÜßÝ¹½½6\x0017'»i­V+§§§Öë\x001f~íç^{üè±«ë[je³=uu}mýxíâÑý^\x0012éaµºSÅÕõ­/¿:õ«¯a9\x001cüôÓOþ÷ÿø¼ÿðÁÅù¹Û»;oÞ¼ñÕW_yÿþG\x0017>ÿìSË1N·'ÊäîîN&mo®Ùj³&eêIÕ¤\x0005($$\x0000F$\x0004t·¤%-)U \x0013¥¥\x0001\x0010\x0012H¨¢»u·eY,Ë°ô°ôpXö£Ãáh9\x000eRJU©©T\x0015$HZw$ÑÝº[wënÝ­»õX¤ÛXÚñ8ÜßïÝÞÞ[FSER:md\x0018cè\x001eF·îÖ\x001d£cYå¸\x0018cèîè\x0000\x0012*Ò¡jR)D\x0004@UI¢ªLÓd'I\x0011DwK¢ªÌól&PUtt·iHÀêæúilw§¦i6ÂèÄªR))
L\x0014U$A)\x0005HB\x0001i*U%)I¨*
d\x0002P(\x0012*\x0000)ª\x0010\x0012 
¨\x0002\x0004	U$:t·î¡R¦í¶kg';§§'ÎÏÏ\x001d\x000eÃýÃbfe¶Z­$íæöÖÃþÁãG\x0017NO\x0016«y6Ï³ãþ`»Ýúø£\x000eËËkÇãÑ<Ýnk¨*_|ñ¹«÷~þùµW¯^ùô½{wíæöVMT1±,ÖëÙT\__¢l6çÞ¾}çx<úßüÆùÅ/¼}÷Þj½²ØûÃ\x001fÿäììÌa¿·Ý:.m^ol6\x001bW×ÖëiýüúÏ>ýÄz³õþÝ[ëõÚ«?%íÉÓg.\x001e]ï\x001eüöþÑÉvç§ò?üÉW_}áóO?v<<¸¹¹õäñcw7·nïß¦ø§ßþ½Ó3½ðîõ\x000fj,ÆXÜßßÛôp\\x000e$NOOÕ<I\x0001DÒZ\x0004$\x0001\x0002¡\x0003$^±\x000cÝ-\x0008º£*P!%!\x0004HÚ\x0018eY1,cXÃrX\x001c\x000eGûÃÑqY¤£ªLUèn¡zB$DÒº#î6Æ0Æ0ºõ\x0018º±\x000cciãÑÝÝ½»Û{cÄTLU2\x0018c\x0018cXÆ°,C\x00181bXá¸\x000c£[\x0012DkS\x0002*$ÖH ª
$\x0001U¥ªP(É0Æ\x0004TªRU\x0000ª¨*U\x0005F·ZÕíý
f¬LÓd½9D(R\x0014RE)U\x0005\x0008\x0002H"iB¢*Ô\x0004Ò$@U!\x0012(\x0010E¡¨* ¢B\x0001ªB(DI\x0018Ý:-\x0019*1U9Ù­}úÑK\x0017gg~úùï¾ÿÉÍí½©b£ý½it·îÉá¸¸¼¼¶Ý¬=º¸°½Ø:\x001e\x000enontâápïðzoÊÇ\x0017æyãÃåµýa¯v¿w}yc·[«jÿøO¿ñ?þÙõõ­Õjo½^{õâ§O\x001f»üpåÝû\x000frñø©?üá~~ûÆ´zéòúJw;\x001c\x000e2âêúVº½x¹òÙç¹ºº2Ï³õzöæí\x001bõÆë7·¾ûþGgg'6µ×o^Û®W>ûôS¸½¹qrræë¯¿vrzâ\x001fòîÝ\x0007_|þ©¯¾úÚ~¿÷öÝ;ÛÍÖÝýýñàôìÜ\x0017êö=5­tMÑ\x000eÇ;IæYFd°9ÙV+Ó\TD$Q!	H  \x0013é\x00061ba\x0019GU\x0013!î\x0006
&B\x0012I$t·eiË\x0018c±,mYÃaq<.e1:nIK"iÝ-îÖî6ÆÐÝºÛèÖ\x001d£[6Æ0Æâpxp{wëp8¨DM&U¥»¥\x0011cD6Æ0R±8\x001e\x000fËb,­; ¤¥¢´@G'b\x0012\x0000$\x0004\x0000TiLS#H\x0002 îÖ\x001d¥LÓdg\x0010Ñ£\x001dûhµ,ÃõÝ¥TæÙYw4Ó¨Ð \x0012\x0000\x0000(\x0000	U­5$\x0011-)@)E\x0001UP"JPR\x0000APQ	\x0005\x0008\x0005H¢ª\x0000E\x0000ªBë´N\x001bJ\x000b]V«É³§<¾8w²ÝÙ?ÜÙï\x001fTm,£±\x0018y^9;;³^¯<Ü?XGÝnëñãG\x001eî÷îï\x001fìN]ßÜ«P\x000eÑÃIL6Ûe´wï>øðá_?ºð\x000fÿwþçþâû\x001f~ôìÙ3÷û\x001fòpÿà°,¾ÿñG¯^¼òÛßþ\x001e\x00075Í®.¯}¸¼ôâùs¯^¾ôìé\x0013\x001f>|p\\x0016'';'';W××\x000eËÁÕÕµ¯^úú¿ðÝwß»ûùÆ/õµGÎ}ÿí÷æirrr&¹TÓÊýÝÓós¿ûÝoùÃ¿þ¿üõ\x001bÇãÑj5\x001bËâýòAÂ4Ï¶Û£Õ<9=ÛQ<<Üª*-ËÑv\x001c\x000fG·×·\x000eËÑ´ZÙn­7³$ 	@\x0002º#1±\x001cÍ«ÙÈ0e*\x0008!\x001d$ ÑÃq,Ëb9\x000eËqq8\x001cíÃq±,C2U!º1ÖZºu¢Gë´îÖc1Æ02t·1ÚXÚ\x0018Ã²,\x000eÅíí[ã¢&jÒ\x001dË\x0018ËÁ²\x000cË2¤£ãñh<:\x001e\x000fåhôÐ\x001dIt\x001aT	\x0008	Õ:Q¨\x0002(I$QUªJU\x0001\x0008\x0006IénI¤#i¬æÄ2\x0016c\x000c°¢±¸½»²^o­Wk½\x001cIT J©*\x0015\x0014I\x0001"¢2¡T\x0015\x0000è\x0010M\x000f*PP\x0000\x0014"ª
\x0005*@\x0012R\x0002¢ \x0008*\x0014R $ª
$­¦¨NtLU¦Õl»mÖåätcµ>1<ì÷\x001e\x000e\x0007\x0012S±'c=ìöË¥i¢¦ÙTeYÕvgfÛÝVwï?x÷þ=ÓìöîÎf½²WvÛÇ\x001f¹¹¾ñøÑ_|ù»û{÷÷\x000f¦©Ü\_[£ýÍzãæêÊ£ó3K&ïß_Ê´Ö)0ÆÑn·Är<Ú®·\x001eö{=¢\x0007»Ý[ÿð_8ì\x000fþø?¸½½ñé'¯|ù÷\x001f>Xm6öû>\x001e'áÓ?r{ãêîÚÿù/ÿj³^û÷¿ý­ýÞ_þò\x0017O=õôÙS××W¦°ZÏîno«\x001cGÓ\6«±\x001cÕ¡ÔhI«igZM \x0013Ðª\x0012!$DwtGwëBJ¥ub\x0016I\x000bH\x0014N,#%ãp<.ÇÅÃa±?,Ç¶,­»\x0011¥\x0014FÚèXFÌ\x001a­;:­Ç0º-c\x0018cXF\x001bc\x0018Ë0Æ0Æâ¸,\x001e\x000eG·÷\x000fnïî\x001d¦¨i*SM\x0012ËÑá¸·ß\x001feDLFÇr\\x001cGËr4º\x001díplëu¤btSÑ¡ª%\x0004TBJ\x0002\x0000$ÑÝ L&1$\x0000tt·¤­jé2G··\x001flÖkcP)\x0014 PªH¢ª(\x0008\x0008$\x0004L\x0004\x0015$(\x0000¡PU@Q
\x0002\x0011	ªT\x0015¨\x0002T@¥
 P ª\x0000($ÒÑ\x0004\x0015\x0012	=e9Z­Ê³'ÌÓìáaïîþÁqY\x0014æ©L«É²\x001fÆ±­V³«ë;\x0017çg¦õìxØ\x001bËb,+77wnïîì\x000fÃñÁzµ²Ýl\\yõâ§Oúþû\x001f¼{÷Þ'~ê£\x0017ÏÝÝÝW\x001b··wF\x001feÁª,K{ÿþ½³Ó\x0013ïß}ððpðâÕ+}ò±wïÞøë7ßº¹¹\x001e:íÝ»7ÇÅn·óå»¿»³Ûl|ñé§.?\º¹¹óáÃ¥O>zåäôDº­æÙ~\x0019Ç½Ï>ûØ~¿g\x001a½xæáÇ£iÞxûæ\x001f~úÙãGl·;·7·þüç¿X¯V^<}æôüÌX\x0016w776»\x0013)Ñ¶ÛY0a69ì¦UÙmU\x0015	 ÒD$H¢;H¨Pº©®H4PTé±,e±,ãqq8\x000cÇãÑñpt\\x0016Ç¥uZ)Tt¢NT\x000fÄ\x0018­»-Ëba\x0019Ã²\x000cc\x0019F·1\x0016Ë²8\x001eýþèîîÎíý½¥[U©ÌÓ\x0004ÆqÑY<ì÷öû\x0003T­ã2,Ça,m,íaps{G±Þ "!\x00152P\x0012hPJ\x0002\x0000$ÑÝ@\x0000JwKD\x0012It·1$\x0012ºcUJUéÄñpïîîRM\x001bDUIH\x0000¢\x0004¡
\x0000T\x0015\x0005%HC¤(T* @UIÆ\x0004ª
T¨*@(\x0004PTEB)$JH"!\x001d\x0011L&$Dë^èa5Íz¥DM\x001cGéHb½ì6+IÙlv6óÊTe5Oö£hc,no\x001fÜÞ?89=ód½v²ÝØngñ©ífã¸\x000cO\x001e?òí÷?¸|ÿÞ<J#6­»Û;ççç={*i«Õìââ\x001c¤n<{üÈ³§U\x000fWÒíp8úùç-ËâÝ»·>úè#¿øÅ/ãÁn»öäñ#\x000fÇ£\x001f~üÁ·ßo9.¾üòK\x000f\x000f\x000fz´ÓÓS¿ýõ¯>þä\x0013ëÕl½ìNlO¼ëøÏÿù¿xúä©/¾üÒÉnëûï¿õÜþ\x0017~ôgÎ%Ü^_Y­×v''JçÙ<ÏeXAÅÃ][­gëÍ
$A\x0004:\x0002	¡;º[\x0012ÝCº¥#Sn!S$Ñi´\x0012ª\x0004iXÆÑ\x0018\x0007Çå`YöÇ½ýÞáxt8\x000ec´t(\x0014
H"ÝZI"¡»11,cXÆ0Æ°,Ã\x0018Ã\x0018GÇåèpXÜ?Ü»¹»óð°DÕdªR&Ýíp8\x001aËÁa¿·\x001c\x000753îXÅq9ZF,#îî\x000fÞ~¸t\x001cÃãÇ³ÝÉ\x0016\x0001I¤©\x0002º[´*º\x000b\x0000$DwënIT&I@\x0012D\x0012I@U\x0001BbU\x00150Ué\x000c\x000fû;ÓÔF·\x0008\x0002\x0008Eº\x0010PB©\x0010¤(J&\x0001@("(@\x0011\x0008¨* ­ªP*(\x0004P\x0000¦©$TPE¤@P¡»u·Ñ¦ $H/2\x000ej=ÛnfÓ¼1Ïåx8þÿ	ÂeÛì@°\x001bÓØê«@\x0004DeV&ZìÑ\x001f\x000f£\x0019\x001bld»¬¢!\x0010xâ¾+Új-w\x001cÃuYE¦Ãak;ï2X×êùéÁ¼m¦Ù\x0010áåxr>Lãh(áÍ«;¯_ßÚïwö»­O~óõáÑëWo½¾¿w½^<\x001eO_^\x001cnîm7\x001b÷w7vÛ­»»\x001b_¿~v¾4k½õêÕ½Z«»½i\x0008»ÍlzûÆÃóQïér]´Z=??Ûn·æyTuã\x0018\x001e\x001e¿Ò«ßýø£\x001fó¿üêééh³,×«W÷÷þñ¿ÿw¿üò«ÿñ?þï¿ÿÞv··ßo|óáç§G?½<ûúø¬üõg·w7vy\x001a<?=*­"et×ËÑ4qÔ[µÝÎJµ¦Är½º\x0006ÓpC2SJ\x0012È$Lz¦MïMïUmUÉTZ%i-½\x0013D¤\x0014\x0012ÙS­Õº.åjY®Z]«ëõêz]¬kÕZ\x0019"L©÷®µ¦µ*³È¤÷®õ¦Öªµ¦¶¦µªÕ®Ö¦ÖÕZWu]]®«ÓÅóËÉu©$@èÖµ:/ÚºXÖEK¢\x0014]kÝºVµUµw­Ó®«Z«ÖÝî`»\x0005RÊLd¦Ì\x0012\x0000ÙSJ)3õÞõÞõÞõÞAf\x0008Ì\x00002\x0013D\x0012¡bH\x0011ô\x000ca]\x001b®ÖÖeo"Ò" \x0000\x0000 ev\x0002\x0002\x00102»D \x0012]f\x0000\x0000(\x0002)\x0001\x0004"\x0002È:\x0008\x0011!\x0013R&ID¤D\x0008)¥©õ¦ô\x0000QLzO){ÓzÕ5%a`³\x0019¥\x0018Ê`\x0019FÃXl§Y]«çóÉãóÛû;ß¼ßÛï¶2É$\x0014Ër%ºa\x001c==¿xy>ù?ýÙùr%&7½âéùì²vN'»íÖýÝ­yüúë/®×o¾ýÖ/\x000fÆqôùó'ÃÖ<ðøø`©ÝËy±®ÕñåÙn·UÊ`]W_¾|ñùógëÙõ²(1øû¿ÿ{ë«{¿þüÑù·Ï>|xãææ`­Í¿þû¿ûßþá¿¸®«O>ûýï\x000f^Ýßp_ôÞµ\x001e\x001e|úòÅe½úoÿû?ø¿ý£Ï¿þêr|6o6Z_,ËÙñiµz¶^w¶»;Ó¸hkX.Wm·S¦\x00022Sf\x0002È¤÷Ô{zv­7ëºªu\x0011e B)MDH)¢\x0010\x0003è=õÞÕZ]¯\x0017×ëârY,k³\\x0017×eµ®M]W½uPdº6Ë²XRq\x001cZëZëÖVµÖ´ÖÔZÕÚ¬µYÖÅz]-Ëâtºx~zñòrVk#j«ç³q,ÚZµÖÅ0\x0018ÆAé©µ®µªµ¦÷.3ôLk]Ó¢Ö.3¥ \x0013È$¥dÈ¤gzïZk2Sk]ï])!"d\x0012\x00112SDÈ\x0014\x0011"B)\x0005DOc S)¡·ÐZ×úbíMHQE\x0006\x0004\x0008\x0000$BDA\x0000H]&\x0000)\x0005\x00002\x0013\x0010\x0002\x0002Bf\x0002@f"D$\x0008"LdJ)Ì\x0014\x0011$$B Ñ{Wk\x0013Q\x0004\x0006A\x0000½§ÖºÖºÖRïMïUÏ@\x0008aFÓ8jS{³Ôj­«\x000c\x000c£ëuõòòâõ«W^½º3of»íNfê¨=ýå§_ôÆµ2möçº®(¦yãí»\x000f\x001e\x001cGÃÎíí­/_¾º¿ízYýúë¯>|ó­ÚÒ¯\x001f?¹»¹ÕË²úíó\x0017_¿|1\x000eÅwo|÷ÝwÎ§£ùÿ¥µîåxrs¸qw³ssØ{ûîãéè_þ×¿ûúðäw¿û½û¿üåÏÎ³ßÿþoüó?ÿOÿñ\x001f2MýaïpØùÝï~4Í\x001fµVµÞ<?½øí·O¢wz3\x000cÍ¼±v²wçÓÉrM×óÑ~¿xõæíá GZëbYVa2»Ì\x0004©'Ìzïjmj­j­DÓ{*e\x0010QD!\x0014\x0011h\x0008­u½wµVëºZ®WëÒ\®Ëe±\ªu­jí:\x0008Ì°®Íå|5
\x0017%\x00062	zëjëj«j«ZmÖuUk³.ÍeY,×Åå|ñôòâééÙõº¡\x00042HÖµz~zÑÖªµ°Ùìl¶a\x001c\x0006ÙÉÖµZK­7)\x0010zÒzêIDÊL\x001dD
d"ÉLZozk2Sï)³#e\x0012\x0011\x0000J	Ì\x0019("Bï]kMëÝ\x0018
Ñ%¢¬©·¦÷0D\x0001D\x0010\x0001"C
\x0004\x0002!%èd!\x0008"\x0005\x0008\x0000\x0002\x0019)\x0012\x0001d¦@ê\x0002\x0002\x0002d&\x0000:\x0010@ \x0013\x0010È\x00042eoZkÆ¢w\x00042µzïZK­wµUµ®"BDAÈèB(^¥NÝ~o¶N§O¿\x0008ïß¿w{8ççç£§gûÛ4N³ÇãÛ[ÛíÖ/_|<LÓl\x001c'Ó4ÓÓétr¹ì÷ßø¯ÿõ\x001f|ùòèãÇßÜß¿²,«Û»Wæ!üç_þ¢âõÛ÷Ö\x001e¾|ýªõ&"DZj]ìi¿ßº¹»ñåëW\x001fæ÷þñ¿ÿWOO\x001e\x001f¾|zp³ÝúÇÿö_e¤ÿø÷×³¡øë_ñáÃ[?þþG½s8ìôÖ}ùúèáñEæÏ~üð\x000cËu1³q;ê­)¥Bàr9{zz\x0014Óh&"´µiã ¢Ë^e¦,¡÷dèÙõN¯]«U­Õ²4]\x0019ª\x0010e4\x000eQ@èh½iµi­º^\x0017ËÕe©NçÅñxr¾\]EmUÏD\x0010@mÍõr1\x000eAJ¥\x000czïÖµY[UëªÕfYVëZ]×êr]'§ÓÙóËÑétÕj\x0013Qd"ºÌ°\«ÇÇ\x0017ÇãÉÚqÜß R&µumíZ]µº\x0018\x0008²ÓzjJozO\x0010H@d 3õÞd&Rê\x0004\x0011ÈD\x0008\x0011dI\x0004\x0008 ¢÷®D\x0018# \x0008]\x0008\x0011©÷\x0014"("B\x0002ºD @ "\x00042Sf
\x0001H\x0000)"@D H\x0012$ÈL\x0000¤\x0014BÈL\x0000\x0011!3\x0001\x0000D	\x0000\x0000!Df×³H)2Sï]k]f×{ÓZ3Q$ªÞ»ÞºÞ:\x0018¢\x0018§Ù~;\x0008ÍãóÕu]\x001dOG½§ãñèt>ûúðèñùÙápc³Ýê½;O2»Dë©ô¤w¯îïf]\x0017\x000f\x000f\x000fîî^Ùl¶v»O¾xzzòÍwß9¼}åñáZW¯ß¼uw{ëf°ÝÌ"¿þô÷ïÞ{ýö½~úÙdR×j]\x0017/Çîú\x0017üã\x001fý×ÿò¿ùóöåËg»ûÿÝ8M¾~ýâr½ú?ü\x0014Þ¿c3M>]¾Ønw>üðAké·OÜ\x001eöö»½¯O_]Ïge;ÛL³(t]£\x0012Óù(¿pÿúµiÞ\x0010¡õ.³ëD§Ó3édÞ»Þ»ÞÖZ«u½j½	0\x000c:Ì±\x0019Ê 3ÔÖôj«j­.Åùru¾.NÇóÅù²XUï)\x0004AT"Éf¹è"Â8L2»e©ÖÚ,ëb]\x0016Ë²º,Ëuu:]N'ÇãÙé|u¹®R\x0018A$	i]ç#ÑÕÆ<oD\x000cD±NÌt¹^]®g×åª®Í0PJIfYuE"\x0004\x0002 %\x00192SfÊNÏ$S 5¥\x000czO­7)2©÷®Õ&{7F\x0004\x0008A\x0010"\x0008!3õ$2\x00142C¢e*(\x0011èd
\x0004 3ev\x0011\x000c\x0002\x0000\x0000\x0000.\x0000	)3Rd¦ 3e¦\x0000\x0004 e¦\x0012EfÊ\x0004zO½§ì©é"B\x0004Ð{W[ÓzÓ{×;´HÔeV­5­u½uÐÛªD\x0011½ÆImÝñt\x0011ÙMód»ÜßÝøòðäù9Õºº½½õôô$³\x001bÇÉ4Î\x000eûÃng\x001c·oïì÷{\x001fûÍÿüÝîðùó\x0017µ®>ùlGûýZ¯¾|ù"bð»ßýh·Ýùåç\®ß>}r<_\.W÷¯l¶[ó<úïÿøß<?\x001dýòëoîïî=ß\x001fýòë/záÿùÿúûöÛ\x000fÆ(ö\x0003^ÝßYÅ?ÿóÿt:]¼~óÚßüþ÷þð7¿ÓzStM]Wu½Z£aè\x000cA\x0019DoÎÏÏ²77ww¶\x001b=\x0007­w)\x00022$;½w­5µVµVëºZ×«µVb\x0018»qLc\x001b-\x0011zOµ6uíÖµº.«ÓõêrY\¯W§Ëâ|Z\¯«ÚÞÉL	èJé2WKQD\x0019\x000ccÓ[ZÖêº,.×«åzq¹\/Óåât¾º\®.«umz\x0012\x0011"BJÐAmMË.;aq<ôLc)2S]«Ëõâ²\e\x000b\x000cJ)@ïô.\x000b	D2Sï]f×{Ó[Ó[×zÓ{×[D\x0008©÷&\x0013\x0012\x0000ôôT¢\x001b#Bf"\x0000\x0000!\x0014zR\x0002\x0010);:Y\x0002D\x0010\x0002\x0000\x0012\x0011	\x0000\x0000\x0000d\x0002 D\x0000	 3EÌ\x0004½w\x0010\x0011"\x0002d¦\x0000"BB\x0004Ùe¦ì©÷Ô{\x0017\x0019"@ÞS«M­Uk©õ®µT"É$RÏ¦÷U­Mfj­ËÞe¿ªµ«µ«9¨­©ëb\x001cGï\x000e\x0007ÛyÔ:gÇçGÃ0ÚLÝÞÓó³í~¶ÙldoZ¯vó^)a\x0018u©>}úd³9úá\x001f}óí\x0007ã8é>þâÍ«;¤çç£7oÞØ\x001fv\x001e¾~Uku{{§µf]W¤ôÃ\x000fßÉ¾úôÛoÞ½ûàññÅ/¿|´ßí}óíw>~úìÓÇßÔÚ}÷Í\x0007oï_¹^Ï´îÍÛ·-Ëe¹Ê\}øðFëÍ4ª£VWÑS¯«º\x0016QÒ8Î¢&¥\x000cÊPÔåêåéÑ²¬nÕ¼ß\x0019¦A$dÊzÖÖªZWëºZÅ²¬Z«dHET¢,Zg­Í²®¥Z®ÍuY\ÕõºZëj¹Vkmjëz'\x0010DH\x0011!Ì°¶®Îj/"&µ¦ë²¸\¯.³åzu¹\]®Ëu±¬ÕRV;\x0008%(è\x0008¡(Ã \x0010²%Y¬KÕúQ 3õÖ´ºª½\x001ceBÈìµZ¯U\x0019G=!e ;Ì.3u]ö¦÷®·¦gÓ{×{LH\x0012\x0001@Ï½#DPJ\x0018J\x0018ÇPÊ`\x001cgã8j­d\x0002\x0008!\x0004Rï]\x0004\x0004\x0004@R\x0008"dO!R\x0004\x0000\x0010\x00112\x0013 \x000bÑ\x0001\x0000d&\x0008\x0000\x0008\x0012 D\x0000 C"Dê­k½)Zëj\x000b\x0011 
\x0011!{ZkS×®·ÔkªkSJ\x0002ÈìZëjkzïz¦Öº¶6ëºZjS\x001bQ0Í³Ívg¼¿·Ýlí÷;½§ÞÓÓãq\x001cm7\x001bw··îïî,×Åõz2\x000eW÷w"Â?~g³=>>SØî·J\x0014o^¿v¹\|þüÞ»ÝnëññQ­ÕÛ·¯½zuëz]ÔZõ^mw;·77j]ýøýw~ýågÿöøoÖ>þúÉíý¿ýãßÈìóU\x0019&¾<¸¹½ñþÝ\x001b\x000f_¾øòõ«ÝvçæöÆç/}úôI)ÅõrÑÖp~z°,Z\x001ba(R7	eØ\x0018"ÐE\x0014Ó¼q]«ãËu½Ï\x00077w·6»d©·®uz¯Öºº.WËÙårv½.ZkZ\x000f­¥Ìèµ6ËZ-Ëj]«eijmÖÖZõìjë 3\x0010B\x0010ÈDèëµ)±º,«nQÊUÏ°.Õ²®uq].Ö¥ZfmM­]vz&B\x0004\x0001\x0008)J\x0008!"\x000cC1Ô\x000b2E!¤ÌIf\x0010"\x0002dvË²8ÎvÛ³iE@\x0012½Kd¦ÌD)J*\x0002¥\x00142d&IfÊL\x0019©µ&3\x0001\x000cC1O£y\x001cã¨£Í¼1n¶[ýtÒz\x0003\x0004\x0008ÌT2e&H@ 2E\x0000)\x000c$\x0000 "d&ÈL\x0000@\x0000\x0000\x0000@\x0002P$H\x00012S\x0004	2Hµ7Ù»ÌP[34J	\x0019D\x0010ZcYVËRõNë´ÖõÞÔ³Ëz§µ®õªujëÖuµ,«ë²Z×ªõNi-×j\x001a6Þ½{ã}0MOÎçÓél³Ùè½\x001bÇÁá°·\/¦iv9=ôæõëWôôÍ7\x001fDÇçgëºªµ:ì¶~ÿ»ß©ëÕO¿ü"J±®«Ã~çí{µv?ÿò«ÇÇ\x0007ÇãÑwßëoÿø{çãÙÇ¿Ùî\x000e\®Æ)¼yûÊ/\x001fõúÍÿò÷ðúîÞu©Ç£Gww·Þ}øà?ÿü\x0017\x000c~øá\x0007Óo£ÿïÿùùþËï¾ûÞ~;é«a,1XÛblUj²M\x0019D\x0014½7i2³íþÖéåÉùåèt^ôÞÝ;ãfºÞÞèz¯2a\x0008»ýÖë|cÚl/\x0017§ãUm«ë²Zj³,«ë²ZÅº®êÚÕFOz§édÊ\x0010\x0000H\x0011!3\®Õ¯OÊ0¸®UïP´jmjkjozvÙºÌB*"("\x0002\x0000@ \x0008"B\x0010%H\x0011Å0\x000eaPJ ´Z­ëªÔ.{ZWµ5_\x001fB&ûÝÖf3ÆÁ4\x000eÊP\x0018\x0000
(H­5rRïÙµZKÙÞVÓZÖ;Éf\x001aMe\x0010S\x0018J1A)aÜîöj«jo¢§.2H)3¥\x0004"0\x0008\x0005\x0019\x00012S\x0002B \x0000\x0000\x0000\x0000@\x0006Ì\x000e\x0008"\x0002$BÔ\x0011@¦ÌDÊ$%\x0000R×²k=ôÖõV  Q[ZÅZ¯z¦ÖZ\x000bR×Zê=eïzïZojkÖµ»\\x0017ëÅr]ÕÚ¬­©-
eðôttw{ïûï¿%ö¦q\x0004\x000f\x000fZc'zs¹ÂíÍí<;¾¼¸^\x0017­5ëZíw{­v÷?¼q:|ýüÙÇ_5£ÝfööõkÍF\x0014>}þìíÛwöûÏÃñxò§?ýÙûw¯í·\x0007ÿò?ÿ·oßøþû\x001f\×«Ý4
~ùå\x0017ß÷ï¾ûàÓ\x0007ûýÆÿúÿâË×Ïþá\x001fþÞáæàþþµåzµÛì´C³¬«oÞ¿sg~Ó.\x0017uM½\x0017c\x0019dKËr5o¶¦iQ´ÙÌäÁsë®ËêùéÅ¸Ü{\x0019bFó0§Ùv··?Ü\x0018Ç­ZÓËñÅãÓçç\x0017ÇãÉËñÅétr¹^Ôu±.«Ëuq<]ÎWËÒ´Úµ^ev²XUmWz\x000f\x0011\x0005árm>}=!µLAì)2d$\x0011d\x0011Q\x0012D H"ÈL\x0011!3e¦\x0000\x0004\x0002!\x0013É\x0010Å4\x000cÆq4N£q\x001a\x0008µVËuR{×Zª­é-­µ{zz±,ÕÍaçæfçöæ`»¹µÝnE)DID,ëªÖ³ZÌÔzê­«­jµ[kªuU[Õj³¶¦ÖF¦i\x0018\÷[ûÝlÞLæy²ÙÌÆÍfk­«Z«Ö\x0012H\x0011D2\x0001\x0008 PH@@\x0000R ¥\x0012\x0000\x0000DÌ\x0004$ d"\x0008!%\x0019"\x0010d¦DdH	I(\x0008  É\x0004ÙI2SÏÔ3õ"R)\x0005IÖºëuq]¯BÑjSÑ¤i­]­Uf×{Ó[³®Õ²4ËuuY¯ÖµÉ\x001eZ¦ÔZÕÖý¯ûWO_½~ýÊßçÕë;ã\x0010N§qÝÜì¬ëb;í½ºe·Û¹¿»\x0013Ãäó×\x0007ÇçgÃ0xÿá\x001bã0ÇÉñåÅ§Ïl7³ï¿ûÆ?þh\x001cGþË_<\x001fÞ¿ÿà\x000fï½ÿÁÿñü|úüÙ?ÿÏÿå»o¾µÙl=|}4£aCñ·ü£_~ýÕ¯¿~ôÍ7ßº»Ùûúå«Ý~ïx<ú×ýwïÞzÿþ\x001b?}r>¼~õÊu]ýôóO®§\x0017e]4E,2§ÉÚV½V1N":"í~'£ðü¢ez~>¶[oÞ¼·»¹7o\x000f¶óÎv³³ß\x001fìon\x000cÓÆùzõòòâÍñ¨ÖªµjY®j]æi°Ûnôì~úé\x0017ÿü/ÿê·ß>[«ZWPÊèåøâôüHtkkN§ËeÕ["]Ö\x0014R)E"JQ
¡ "d\x0012\x0011"\x0000 \x0011\x00002\x0013d& DR
 E@J]è`\x0018\x0012£±ZR[U[×Z\x0017×b]ªËåªõÕ²^ôì¶Û½Ý~$ÞÉ¤gê­y9=?=º.Wµu½u­u­5­UkïzëjkZí2Sï]oM)áée¶ÝL¦i°ÙvÙXJ±ß\x001f´ÖÔÚÕÖôL¤=ôL­u¥\x000c\x0002A	) \x0000\x0000)L"ÈL\x0000)3E\x0004ÈL\x0011\x001e"\x000c	$Éì\x0012²\x0008\x0011ôl"
\x0000$\x0002È¤gÊL½w½w=è\x0000j]®gË²*etY\x0016µÖ»µ6Ë²Z×*Ñ{×Zµ,Õºvµ5­¥I&\x0001!"Àùrõ\x001fú³ß>}½KÝíÍÁa¿Ó[³ßï´6;¾\x001c\x001d/.ÅçÏ_lv\x0007)NgËrõÝwç'"ÄP¬­Íî_¿öõëWÇãÑãã£ï¾ÿÞv³ñòòìææÎ?þãóýÿ?>}òsÿÕßÿýß·³?ÿôWïÞ}ðý\x000f?Ú\x001fv>úì|¹huñêþ­ß~û(3Ýßß»\\x0016ÿú¯ÿîùùÅ÷ßãÇßÿàt¼øø×}úíã»×6%½<?(%¡(IPAéÍå|r9\x001f
ã`³ÝÊ¹\x0019ÆÙ~7Ü{9-ÅËãÙ7ßÞxóáwq6HQBÓ-õ*ru]®Z;\x001bÇ4Ï³(;%îãh»Ý»½¹óúõa\x000cÿùÿivþü¿Z×Þ«RÂ8N®³ãË£RXëêÓo_}þüÕùrÑ3õÞ­kÓ["J\x0008!¢Ì."D\x0004 e¦L"\x0002@fÊL$BD\x0000"èÙ´ÞeKt\x0019iìE)2L\x0002ã8ëZ¦y\x001e­ËjY\x0016k½z9\x0010¦i¯÷ADh­«½é=µV===y||°¬Uï©g)3õÞd¦LzO½'B&­¯zoÎ¡\x0014ãXÌÉ~»1^.W»ÝÖn··,ÕZÒ*ºÌ$\x0011d&\x0010Hz¦\x0012A\x0012ADH\x0000\x0010 3e&\x0000\x0000ÈL\x0000\x0000!{\x0008)Ì \x0013¢\x0000@f\x0007 HI\x000f$Dö®µ¦·\x0010(2»¥..e©ÓùTkµ¬ÍuYµÚdRí]¯©7ºD d\x0010@ïIO\x0014//\x0017ýéW\x0011|øðÖ÷ß¼³´îÓ§Ï2\x0011LóÆO?ýìó/q¶ßî¬ëjY®2Ó4O¾>|õøøìË×\x0007ÇãÙv·\x0013º/>Ûïwö»y<<<ø÷ÿ\x000fÿå¿üWoß½õåáÉç/æ¿üÕßÿÝ\x001f\x000cãä×ß>¹¹½s¹\x001cG¯îïmæÉv3ûñ\x001fm·{ËêãÇÏ29Ï~ýø«y3¡÷®K½6zr9=ÛÍ\x001bC)\x0010\x0011Zkzo.ç³lÕ8Mzë¶=´)M0m6¦µÊuuyyöøåWwonµ\x0018,ËUkÍ8Ìn\x000e7¶»½PôlR×zW²+ãh\x001c'ÛM±»RV½5ÙÎ\x000eûÁû÷wz=È¤\x000cÅ4ÎZ[Ï¯\x0003½wo^}õõÝ£óå¢gÓ{w¹\½<\x001cGëª¶ \x0008!b@\x0008\x0000\x0011	!"d&ÈL@ EÙõ\x000cYÂÐSêú²Zb\x001cÒ8¤\x0012a\x0018\x0006ÓPL1ÈiÔ7\x001b½U×õêº,R8/Z{ÐZ³,µU½w­5×ëÕ²,²§Lz\x0002\x0012BfÈìz\x000f2$R!ÚºÚº¥r]eéÿÇÿýÿöOûýÁ0N2CkM««Ö»ÞSï	J)aP"´L\x0010A Bm«eYÔuÕz\x0007¡2SfÊL	\x0000 3AD\x00012SD\x0000\x0010\x0010!\x0002\x0000¤Ì\x0000);)RÏ\x0014Ò4\x0014C!DöÔZw<\x001dýüó/>}~P\x001b­6×ËÕéru¾,®Kµ¬M­i­]­]&)d\x0016\x0011\x0005@\x0000\x0000	H¬µy~~v>]!,Ëêx¾zxzör<¹\\x0017ëêt¾h½\x001bKÑZõúõ+¯^¿Ò[SJ±Ýì\x001d_N\x0012D\x0014C\x0019ív;øÃßØï÷zï>~üÍårv/ÆÑérñüü,"ÜÞÞ:¾\x001cÏgïß¿³,ÌîÛï¾Éº®Þ½/ðòrtØ\x001f\x001cn\x000eÎç³¯_¾h­Ùn7þøûßY/'/_?ëëÕ\x0012RR(ÆqÙµZe'2PD\x0014­w-»ÖºÖº¡ÐE_«eY]¯UkÝ4Íö»½ífg\x001aGÖªV«º.êzÖÚÙº\x001cO\x000f\x001e\x001f~óÛÇ_|ùüÖªÍ<ÛÌÍf6OyMÃ 4Íh»Ù¦ÉápðöÍkïß½öáÃ\x001bß|xíý»{¯î÷vÛI)©gê½\x000b)
\x0001B\x0004\x0011ED\x0008\x0010\x0001¡\x0002"B)!"D\x0010\x0011¢"\x0014ôNï©µ½ë­iµËL\x0011¡PJ\x0018b&Íd»ÙØl6a°,«óùâ|9»\.®×«eY¬ëJ\x0006\x0006¢È\x000c\x0004\x0001\x0010\x0008$@Ò³ÉLP\x00102I\x000cÿð·?üÓáæÆ¼Ù)eRkM«Mk]G 0\x0008\x001d\x0011©\x0004%\x0008êZ-Ëb]W­V\x0010H	"\x0002\x0000d&\x0000\x0000	\x0000\x0000	\x0008"D\x0004L$\x0002RÊI&@	Æ!\x000c%H2Sfªuõôüè§_>zxx±VÖÚ]jY»ÚRïd/zLD È\x0010\x0001\x0008"\x0000\x0000\x0000$\®«Óéìùåh]WûýÞ~¿·Ùl<??9N\x000eûq(Æi\x0010Ááæ {÷Ë/¿(Qüðý÷ÆiôõáÁùrv½.^Ýß\x001bp\x0007Æa0Ï³_~ýh\x001cGß~÷­2\x000cDq>_ÜÝÞº¿»óùóg»ÝVïÝÇ\x001fí÷\x0007ËÕ¿ÿû8\x001cöö½¯_LãèíÛ·v»\x0003X«»»?üî\x0007?ÿçøúñ£1\x0019JÆADA¦Ñ4ÍJ\x0014=Sk
Iv\x0019ÈÔjSÁ².d\x0017Ioiwö77æyT¢kíêr~ôøôÉËóe9ªõ¢·«u9¹].'§ÓÕñxr>]´Æ4ÎqRJ:\x0008½7½/¡\x0018§q\x001cm·\x001b·7{÷w{w·;ww×¯v^¿¹õæõ»Û\x001bíÆ0\x000c\x0004]f	"B\x0004\x0000\x0000\x0011!"D\x0014\x0010\x0011"\x0008!D\x0008\x0008d²§ÞSï]fÊL]&Q\x00180MÍ<ÇA	¢\x00141\x0014¥\x0014¥\x0014\x001d\x00042Sf
\x00002\x0013	DIO\x0011\x0005\x0000\x0011aøöÃý?Ã`·Ûça\x001cÉÔjµÖ¦g2R\x0006\x0004\x0012\x0012J\x0014\x0011¡µfYWëºj­P@f\x0000Ð{\x0007	\x0008I\x0002" @J$\x0000H\x0010 @\x0008)2;	A"
A`,a(EDH¡gZÅãã£¿}ör¼j=´ÚµFf H\x0001 
	D \x0012!\x0012DBJD@È\x0004z¦Ëåê|>k½ÙÌ³ý~¯÷îr>Ûn&ó<Ùî6§óé$2=??[®W»ÍìÃ÷uñøøèøò\x0002nïn\.\x0017¿ýöÑ×¯æyc­«Þ»Ývc³Ù\x0018Ñårµ.Õþ°ÓÚêr¹Øï÷®×«ÝnK/¿j­zýêÞáöàr9¦É4MÎç½ßÿø½h«?ÿÛ¿©i\x0018\x000cq,"Bb&\x0011E\x0004 »ì\x001d)u){'èåjTÕv\x0015Ñõ¾º\ÇG//\x000fÇ'ËRãd\x001a']­VW\x0011è"R.U«Z¯zVÙSö¦D5Mi3§Ñ<
6b3\x0017ó¦q1Ív;ÚmgûýÎáæàææÖn»5Ï£Ýf6O\x0013IoMÏ\x000e"\x0002\x0010\x0011\x0008@ \x0000"	"\x0010!\x0004\x0019 gêzïzïZkjmZëzozo"Â8\x000cÊ@\x0019Â86ól&ã0ÆÉfR@d$2ÉL	2Sf'S\x0002"0|ÿÍº.WÓ<Ùíoì¶{Ã8ê­YkU{\x0003e\x0018RD\x0014\x0010\x0012¡P¢hµº.u]õÞe&\x0002)$d\x0008!£ÈL\x0010A\x0004\x0011\x0014\x00002\x0000\x0010\x0001\x0008\x0010H$È\x0004\x0008\x0004\x0011HE\x001a\x0006\x0012!ÞÒu¹z|~òððh]Ì\x0019\x0008\x0011\x0001$\x0011!"D\x0010"(¥\x0010\x0002D\x0004@R\x0000\x0011\x0008\x0004Ikét>ùúðèááQkÕÍá`·ÛÚngk]].\x0017ÃÞÛ·oì÷;ÃXÌÙýý½ï¾ûäË×¯ÖVe¦ëåìËçO2¸9\x001clæÉf|}xÐÚêõëWJ¾><:^îïo}x÷Î8
J	ûýA­Ío¾1Ï³O>ùðá[OOÏ\x001e\x001e¾àééÁ\x0010éÍíÏ?ÿäóÇ_Lc	Ó\x0010J(¡\x0010Af7\x000cÅ0\x0016%BKz\x0011R¨kÓêbgQ\x0006¥\x0014C\x0019\Ï/Öu5m¶ÆiR¡2\x001b§ýþÎ4ïdvëzÕ[UJ(dEyÕû^	¢Æ2\x001a4
Í4vóÄ<§ylÆ¡\x001aÊj(ÕPV%ÏäÔzÓ³¦Ù~wp{{ëÍë{\x001f>¼õîÝk77{ã4ÊL­7½'BD\x0010\x0000\x0010\x0001dBBB\x0014\x0010@ \x0012E
©k½éÞ»^ÞIÈ`0\x000eÅ\x0018a\x001c\x0007ÛíÆÍ~oÞLÊ\x0010RR\x0008){Êì2S&\x0000\x0011!³ËL\x0000\x0010\x0011ßÿþ»º.Wkm¶ÛýíÍv£\x000cE«ÍÚªÌ&"a 
\x0019\x0004\x0011\x0012"B­Õ².ÖÚôÖd\x0000I\x0000\x0000Ì\x0008dG\x0000È\x0010\x0002!2\x0000\x0000\x0012\x0008A\x0004\x0002);L \x0013d`\x001cÂ\x0010DÐz×ju9_<==:\x001e2SD\x0000	\x0008"\x0008\x0011!J\x0008)J\x0010@@\x0010\x0001D\x0010\x0011"BD\x0008\x0010\x0011"B\x0004% 3\ÕÓó³§§gó<{óö­a\x0018\x001c_m7³ÃaïææàþþÎáp0O¿}r¹\}xÿÁårõùëW§ãYkÍýý½i,ëâéùIëÝº¬®×«W¯^¹¿¿óôüätºÆÙ«»;oÞ¾ÕZ7MÇ§g?ñêÕ+>öððh\x0018\x0006\x0011\x000cÃàº\­ËÅ~3{øüÉåôb\x0008¦!e\x0010Èì ·&{SÆA\x0019F1BQkÓZRÔ^]«\x0008¦q2\x000e³i]¯ËõjÞîÝ\x001cîl6[ã¸\x00111¢²WËrRëUf*Q\x0008\x0011E)Ef'»q\x0018
¥(\x0011":\x0016Ã°§4MÝP°Ê¶UdÕÛ¢®ÝºR+kM¡\x000c\x001byãæpðúÕ7¯_yûöµ·ïÞzûæµÛÛ\x001by\x0012ÞºÖ\x001bÙ\x0001!"Aï\x001d)\x0010"B$\x0011\x0000\x0010":¡gêzO­5µ6­uµ5½u½w]\x0019Âv7Ûí6æi°\x0006»íÆf3ÙÌÝvc\x0018.eï²wD\x0004È$\x0010\x0001D\x0004á\x000fóÝ?õL×ëU&7½ÃÍÞfÐZU×d\x0018\x0006QB&¤\x0012RDZ«e]¬µªµÉL\x0011\x0005\x0000!\x0003R\x0008\x0004È "\x0014@ \x0000 \x0000\x0000@\x0004\x0002\x0010B&LzO\x0000¤Ô5\x0011i(a(dªuµ\¯§£\x0007çóEb(\x0003AB\x0004\x0011!"D@ \x0008"@\x0004\x0008\x0011!"DPJ\x0011\x0011J\x0014\x0011!JA(¥(eÐÖ:Èz«înoep¹\x0015ÜÞ\x001c\x001cö{ófãåtô§?ýÉ0Þ½{ïr¹úúðäz]l6[ûýÁÓÓ£ççgûýÞáæà·OE)îîo===:\x001eÏ¾|~ðüôìÃ÷¾~ýâx<ùæoýüóÏ"ÂårñÛo¿ÙïwæyÖ{wssðúþÎõôâéË\x0017ÝXB\x0014Bê½é½é½L¢qRbPAmUë«R,áº®.ç³\x0012i\x001c\x0007Ó¼Õ³;\x001edïöû½ÃÍA\x0019\x0006-\x001b:\x0011d½\x0019Á4ÍJ)J\x0019\x000ce\x0014AÏª÷&{j½ªõªµEk\x0017r5D(QôÆ²tËÒÕÊº¤Ë¥9_¹.ë\x0012Z\x000fCÙ§yÞæÙ<¦y²gýÁíÝ­û»[÷÷·îîníö[ã8JÝÚÞ\x001b\x0000\x0000"\x0002\x0000@D b\x0010\x0011\x0004\x0011D\x0002A´ÖµÖÕÖÔÚ´V­µéJ)¡\x0008¡ÆÑf3Ùmg¯^ßûðþ­Ýn'3Dè2C&½w2\x0001¤DG\x001aþðûïÿ©\x0008½5×ËÅ8Ývg3Î$µV½w%(2\x0011\x0008¥\x0014\x0011¡ÖjYWëºê­"3\x0001!@\x0008\x0001\x0004\x0010B\x0010\x0001"BD\x0008$B\x0010@f*\x0011DH\x0001 \x0004R"\x001eôì: HP\x000ce0Ð³ºO^GÏÇ£ç\x0017e\x0011¥(ePA)!
\x0011!"D\x0004AP"D)"B)E)ÅP\x0006\x0011¡PJQJQÊ D1b"¢¢"¢\x000cR\x0006%
Â8zOÏ/Ï\x0002wwwæÝFDñéÓoàææÆù|¶Öêp¸ñéÓ\x0017ÍÆÝí­§§gëâ|¹hÙ¡h½¦Ñ÷ß}g¿¿q<¾8\x001e\x001d\x000e7\x001e¿>ûõ×ß.\x0017­5ËÅÃÃW¯^i­ùòð ®Ííí­ý~g­Õñx´ÛÌ¾}÷ÆóçO®Ç\x0017ó8(\x0005H\x0019\x0008Ù»ìMPÁ0ÊXôìÖº8_NÖV
ÓNæ Õ®gYc1Móù¤ÖÕííWoÞ7\x001b¥\x0014ó´1³y\x001aMÓ D!RöªÕUë]ïM«ÖV½7µ®Öµj­ÉL­¦VÃ²\x0014óóëR,KX°Ô°ÖAm¡g\x0011e2É0dÈL){HÃ\x00106Û\x001b¯_¿ööí\x001bww÷¶Ûa(2Sï)3 ¢B\x0000 "\x0000\x0011!0\x0008@\x0010A©õ¤Ó:!DÌ2\x0001Á8noo½zuo'=Ó4M¦i2a\x0008\x0011d6²\x0012i(i\x001aÂf\x001eíwáóÃ?\x0004Ó8¦É8\x0016ÛÍl»Û\x0019§	d«z¦\x0010z\x0006(Á0\x000c"BkÕu]­uÕ[G\x0002\x0002D\x0000\x0004BD\x0001¤\x0002\x0012\x0002\x0010A\x0010\x0011DH@@\x0000@Z&2\x0011$ \x0014c)æ1\x000cC×ëÕËóËé¤\x0000µV½'Ab\x001c\x0007Ó8\x0018ÇA) ¢(%R\x000cC\x0011QRR\x00122(e\x0010%\x000cÃ`(E)ÅPR2\x000cJ	\x0011E)E)ÅX\x0006\x0011¡¢""Zo®×«ÖºÍfët9{|z&Âr],×«ÃÍÍfãååÅ²Tã8i­¹^/Z¯J)Æa½;ì\x000fÆqôéó'ùË_ýðÃ^¿~íáñÉùrÕZóêÕ+»ýÎ/_,ËâùùÅét"SÏf0£ÃnVO/ÎO_\x000cÙ\x0015!¢(%DP"Rdï²wQBPÆÁ0\x000ezïRw½^Ïg©7;½ÓújYN`¿»\x0015ev|>ÚnwÞ¼}o³Ù"UÄª·«ËõÅ²¬ËÅr½jµÔ³Ë¤gQ+=\x0007ú¨·A­e
kem¡æ zÞCí¡VZ/Æa2N³,ZOÐÖºZ»ìD	ã<Ûívîîî¼yõÚ»·o½zýÚÍÍ­yÞ(¥ÈL=Ô\x000c\x0011\x0001 "@\x0010\x0011\x0004%AD("BD\x0008¢ dì´zkZkÖ¥ªµZkÕ{SJ±7æiT×Õ\x0010ÜÜìÝßÝ8ì·\x000e»ÛÃÖ«ÛWw{o_ÝøöÃ\x001b¿ûþ½ßÿø?üø­QLÄàÝï½ÿö\x001b_\x001fü~ÜÞÜº¿¿\x0015Ù¼¼\x001c]×."ô "\x0004\x0012!\x0000\x0011\x0000\x0010\x0000"Bö\x0012\x0008zÙ H\x0000DÌ\x0004"A\x0002\x0002$ \x0000D\x0014\x0005\x001dt!"e¦AÚN³Ãn4
U58\x0005m\x00087½·w·\x000eÛß>?8_\x0017\x0018
9Ã<§eiµª­	\x0001RR\x0004 Af)\x0004\x0010A\x0004ÈL\x0011!@*%\x0010\x0004\x0011Ð;\x000fO/\x001e^|÷]sØ\x001fÏgúÏ¿xsçíÛ7ÎçeY]®gËÒôÎ4ODZÖUf\x001aÑõºøçÿù/öû­o¿ýÎ8l\/«ï¾ÿà÷øÑ¿ýÛz~yñóÏ?ûî»oLãèùùÙõ|UÆb­ë¹¸Ýï|xÿÞëÛ½Ï?ýI½\x0011b\x001côD\x000cBÙéMD²§Þºõ²\x00182\x0018ÙvwpYe97;[ÇSszyöÔ\x001emæyw0MÅÓÃW\x000f\x000f_ÅXd6­¯Ä*TëZ\x001dW½wÃ8` 5­\x000c"\x0004!sÈ,"zoZo(ä`(2\x0014U/UÖUÏf\x001aFÛÝÆf;\x000b\x0005¤T"R '=SHQ(\x0008¡Øï»ûW^¿}ïÃû\x0017OOÏ_\x001dÏ\x001e\x001e¿úòùãËëRõÖE\x0004\x0002)J "R(\x0008\x0011\x0001 3 HRÓ¥µu]+]öÁ<\x000fb,ÆHÚÕz	!\x001c^\x001fLÓÆPV«Z«"B$ãPl6íf¶ÙLÆi2\x00062\x0018ÁÛwßøáÇ?úù?ýû¿ÿ§iM¿ìv[ww÷RÈãÉuY))¢\x0008\x0010QD\x0012!LH\x00082D\x0006 S\x0004\x00052D\x0004\x0011D \x0001)\x0000\x0010dÊD\x0000@\x0008È."P\x0004$y*^ßlÜ\x001eFÓ0Y7Òºãq´Ûmm¶\x001b7ûÙf\x001cüúåÁé²èBD\x0018ÊÁ25et½V½7\x0008È$\x0010!\x0012	\x0000H\x0000%B@\x0010A\x0014dJd½{9ÜÝÝùæ[>ý¦÷îááIâr]¤DZ®ìÍ×oµÞ´^N'ó4Ú£÷ïÞúðá­ï¾ÿÁÿü\x0017ÿö¯ÿFçöæFßí\x0008_¾|us³\x0017Á0zk\x0008ww\x0007ïÞ¾U¢ûúñ¯.\x000f_EkÊ8É"R\x0006¥tzê­hLìM««uYóFD±Ù\x001eÜÇìùåÉù|t?»»«µîéËGíWwC±ÛmÎ/>þô'Í`{Ø\x000bD\x000czïz+ä(¤0*eB\x0011F%\x0006¡ë²U¦AëIRJyµÖ«Ì"Ê`Fã8è}ÐËhf³PJ1O£R\x0006\x0011!J\x0008\x0011!J\x0018QD¨uE\x0018ÇQ"3A)(mKÛíÁÝý½ÞÓ0e¹úòå«¿~ôë¯\x001f}þüÙËË³u]e&\x0019H\x0011B\x0012D\x0012\x0001J\x0010A\x000cÅPa(00NÅ46ód3Ï6Ód»l7í<¦É4¦q0
£RD¤¡\x0014¥\x0012Å8\x0014ã8\x0018ÇÑ4
J\x0019)E¦±\x0014Ûíd·Û)eòéÓ'%Òf}ÿÃ÷6û½[¡õÔZ³ÔU*dÈ !\x0004 	$\x0012)	$$\x000c\x0002HIBD\x0010:\x0002È\x0010\x0001\x0004RHH % À8\x000e¶ÛÁí~4
´Íd3^^6Öº§b¾¿5My¿óñÓWO/G­u\x0011ÅPÒ0LÆi2Õr½Z×&{JD\x0010Af \x0014\x0011\x0012\x0000I\x0012ADÈL\x0011\x0001\x0000RzO\x0004Âõºúù_}ÿí\x0007ïß¿s9WëZí\x000e;K]Ét{{cS«Óél\x001c7_õÞ¼~ý¿ûß\x001bÁãÃ£isµ,\x0017ýë¯Þ½{ç\x001fþî\x000f6­ç§gýé¯ÜÜ\x001cÜß\x001f,Å8\x0015¢{zz`½ØçU?½¤a #\x0003\x0005\x0011¢Ö;2»Ú«¡ÐÛ¤·aRbts³7m\x000f^¾Z¯\x0017÷ï¾UÆÙñåÉóóqÚØíoÌóÖÓ×\x0007/¯\x001fm÷7ÆaÖu=G-W\x0019VS
Ó4\x0018Ù8ÎJÔ{§Lz\x000cz­$\x0019¡õÐ3(E\x0019\x0018¦0Lh\x0003e\x0014¥\x0018P\x000c\x0008e\x0018a\x0010\x0011B\x0018¦\x0008j^0Î[e($¥\x0014ÃPa\x0010.3¡\x0018ÇQ\x0008Ë²:\x001d\x001e\x001e¾úõã/þú×¿úù|ùüÙåz\x0016J¡\x000cÆ¡\x0018Á0\x000e¦q4Ïy\x0018c1N£yLÓl\x001cFã\x0010¦a0M£y\x001eLãd\x001aGãP\x000c%
CQÊ D\x0018J\x0008D¦R\x0008¤RR\x0006e(a4\x000ea(J\x00192Ù].G§ÓëõdYV?ÿô«yÓà»ï¿³ÛmÕz£µ®²§B\x0000RB\x0004D" \x0004RÊL ÈD \x0008²#É.\x0013\x00122CH ¥$\x0002\x0000\x0000A\x0002Zo®ËU]ÓfLÑ<\x0014Ûirº\Ô¶R7Ûíîà°ÝúËÏ¿úòô¢õ.;¥0M(£RRÄj­Uk]&Q$\x0002Bf\x0008"\x0002\x0000D\x0004Ì\x00042e$\x0008\x0005!umåYd÷Ã\x000fß¦AT{s¾½~ýÚÓó³y.jO\x000f\x000fýíßþí~ë¯ù/_\x001eÜìöè\x0012×ëâåxvÿÊ<vÛÉ0\x0015Ýäöö õ.³ë¹:ÜmµºjËbÞ§låô¨×³q\x001céÕ0Njv=S)]b\x0018\x0007½7=ô®¶¦¯«HR½6³\x000fï?8=¿hËÙííÞïÿð·¾üú³óñÙ8\x000c\x000eéåùÅÍñjÞNÎKw^ªëÒ´J\x0018Le2Ådw¦q&é­©uµ´Eí\x0008ó4Ë^evÓ<\x0019§I\x0019\x0007ã4\x001aI«©\x000ci\x0018\x0006Ã8\x001aA\x0004½w"Ê "D\x0014Ó4©Ön\x0018GÛÝ^ö$çÙ4Na4M\x001bÓ4¦Q)Å0\x000c2S­«e¹Z×\x001fýÃò_<=?ùøëGùËüòóz~zÐÖÅ Íc§Ñ<6ól3ÏÆq0\x000cÅ8\x0016ã8Êd\x0018\x0006\x0011¡b(¡PJ\x0018J!Þ "N\x0012\x0008\x0011\x0001(¢\x00141\x000cb(¢RÀ\x0008%ÈôôøÅÏ?\x001eD\x000cj«þúÓOæÍdgïÞ½·ß\x001fôZv×ËE\x0004\x0011!\x0002B@\x0006\x0019"B\x000c)\x0013\x0019R\x0017A\x0008)e\x0012\x0008"D"Cf\x0012\x0012\x0008HR"EÌ\x0014\x0011\x0004]\x00022Sf×{\x0007Ù»Së\x001e]Í9+¹wØïLãh\x001cFófvm«e]­Ëj¿|óú\x0015=E\x0019}yzQ×*A\x001aÊh»(âZ¬kÕ{'Ì\x0014\x0011"Bf\x0000	\x00002SD\x0008@\x0001R`\x0018FÐ{:\x001eÏ>}þâoÞÚßÜXÖ'\x000fæi¶g=S]\x0016zêµysÿÚÃG§óÅ/¿~´ÛÍNçÞÓ4n\x001c\x000e·^^\x001eô_VûÃÁºV¯^½v¼\Eï^^\x001eMcÚN[wû\x001b1®/.Ï
R*\x0011ÂH\x000cÊ01¤Þ»Ê0hL½³ÖÕ<JÞ»ÞV×KU6\x0007ÛÝÖËé²zûöí¼ññ¿x9ÍóÆíá _.?6ßs\x000bZcÁn·³ÛmmæÉ8NRWëb]®uqYÖÓf»ÕÇ.3Mó¤2Ê0\x0018Á0Læy\x0014¥(¡\x0018Q)¡Öj]+J\x00192\x0018ÇÉ4M2SD1o7\x000e\x001b\x0010\x0011vÛ­iÃh\x001cFÓ4çÉ0\x000c\x0008½7ëzq>_ÔÚR|øð­?þáïü÷ÿþ¾~ùìËçß<?~v9}Ò'ê\x001e\x0018ã¨""\x0008Q(@\x0012	BÐ\x001b\x0012T"HR
!\x0004R\x0008\x0014\x0011A\x0010\x0011Rê=5Mn$¥ÏÏ"Òõr\x0016\x0018Ê`]ª?ÿç_Ã¬ÄàÍ7\x000eÝXj&\x0011\x0004¢\x0008E\x0004\x0010\x00112é=AH\x0002È\x0014A)¤\x0003@&\x0000)\x0002è=%Zï \x0010\x0012)µj­ÖuÑZ\x0018Ùä<!NZën\x000e{yc\x001egC/Jõzµ^O"ÓÛû[Ã0ÙÎ\x001b×åj\x001cGÇÓÙËùªÄh3J\x0019]Êª®UkUfÊ$"@DÈL\x0000\x0011!3\x0001\x0000DÌ\x0014\x0011\x0000 "ã¨µ¦ÁuY}ýòh7>¼'\x0012óùêf\x0018m7\x001bq[ÔÚ==>Úïo¼yýÆÿòg§ËU)!;mí¶AÏæt>[®WçËªÁ÷ß¿1³ãñäáëW·7~ÿýwvÇ_ÿÓùóG\x0013Æq\x0016Þº\x0011AèRR2\x000c2SöN¦ÞS\x0017¢Ò8\x000eÖZÏ'ó4\x0019âøòl\x0018f··¯Dù/?;]®vÙ\x0018áôøY+³ùö­Ín£g7\x0015¶ó(JÈX-u½k½ëb\x001cL1*Ö»óõb\x0018yD\x0019D)B1\x000c³ívoÞlRÔµé½ÞRïdRÊ`\x001c'ã8Ûn7æy\x0016\x0011z?Øî¶öûR(a¢\x000c\x0008zkèÆ±\x0018âr¹º^/"¦IDQk\x0013Áíí­·oßøîûïOgÇç\x0007§ç.Ç~u~zr9]­µÉB ³K\x000c\x0014¥\x0014 \x0008\x0005\x0000\x0011A SA"³\x0008\x00110\x0010AÒ[£®G
aøÃï¿û' ³k­[®V+\x0012E­Õñø"3í÷{ûýÞ<Ï(DH,Ëj]VumZï \x00022SD #EBBH\x0011	2$\x00142B¢')u)³k­9Î^^®Ú\x0016-»lM«U«Õ²\\x001dG///.ºV»íèö°!»e]dvÃ8ÇÑP\x0006EÊÞ­uÑZ5\x000eÝvãþfïÛ\x000f¯ýðí{ÍÆùrv¾\À8¢\x000c\x0012)e\x0002	\x0000\x0000 "DR
\x0000\x0010\x0011"\x0002!"H=Sk]kÝP\x0006ï?¼±ÛÍj­¦q½ ýnk·ÛÙl7êºj­ÉHµVC)\x0004ó4\x001aÇb]V)\x000cÃ´®ívc'×ËÙ~\x001b>¼¾uþòÙ/úW±^ÍÃ$"$¢\x0014\x0019¡GèBFÑ{"ÞéI"SÆ (z=é\x001di\x0018\x0007\x0011a½^ÕëU)ýáÎn¿#S¯q(Zo2«ÃÁÍí½Ýnc3\x0017ã\x0010è¢tQR¢A\x0019'ea0\x000cEïU­«RqÚ\x0018§Ù8LÆq¶w¦y£'­wuYÕe±®«u]I¦q²7¶Û­ý~çp¸q8\x001cì÷;»ÝÁf3¦Á4M²7çóI­«ÞeYÔº\x0008½w§ÓÑËËÔ
ã¨D E0ME)i\x0018\x0018ÇÍæ`¿ßØïÂaÏÍÍh»ó(\x0002z6¤DD\x0011\x0011"\x0012"BD\x0008\x0011ED(\x0011¢(E1\x0012"B\x0004¥\x000cJ\x0019\x0010A\x0008!\x0004BLÃ\x001fÿæûJAÒ3µVÕV¥$,¢µ®^^àææÆáp0Ï³\x0012a­«ëe±,u­ZïR\x0008\x0004\x0000RÊL)2LÈBB\x0012B"\x0013ät>ùõ×~ýøÉñxÔ{Ó{W[ÕZUkUkµ®«ëåâr½juq»ßxu»3EÏ®¶¦÷n\x001c\x0006ó4¦Ñ<OÆi4E)è\x000eûÉ»7wÞ¾yåöö ÁuY\U&ÃXC\x0018"dÒ{D \x0010\x0011"BD\x0000\x0010\x0011 "\x0010"Bfê½ õIêîî\x000e¾ýîi,d
LóäÍëW\x0004¯îïô^}þòÙû÷ïìv\x0007OOÏRì÷;··\x0007çÓÑñx\x0014C1og77{óÞ}÷í{ßûÚÓ<üòWç¯êåÅ(\x0018	èDÊH]2èBkMÏf(EdHjoz\x0006eTÊ "dïJ\x0014)$\x0008½6uYÔµÊ\x000cÛÍÖÍíÁ4b\x001cE\x0019´åEöªbÞnÄ82\x001aÆÉ0NJb\x0018)"J1i\x0012zOÛíÞíÝÝvo\x001agã´1M\x001b2ÎgÓYë«(a&ó<Ûï÷\x000eýaï°ßÛívæy2£yMÓ Õêt:Zº.®×ºVQ\x0012(2Sf\x0008QB	B¢+CÆ"VÞ\x0013¡è<\x000bÆáh»cØº¹=8Üìl¶³q\x001c\x0002E&\x0011E\x0008\x0012E\x0008A¤\x0008J\x0014¥A¢\x0010\x0011¢\x0014e\x0018\x0012J)"¡\x0014c)R\x000c\x0011Ê\x0010?þÍ÷ÿIF\x0008¤$\x0002)\x0010\x0014"Â²T///¢p{{c»Ýe¹º^.®Ëb­«Öº ¥L\x0002B`\x001cGÛíN)£ÖÈ\x0010Ì¤wIvÙS&©©gzxxô¿þÕ/\x000fjm\x0008ôZO­w­w¢(1h­é½»¿Ù{}w0¢wµj½)ã`'Íl3Oæy4*tC	%íft{s°Ýn¥p½^­u5\x000c£q\x0018 \x0014AF\x0011\x0010A	\x0019\x0001\x0002\x0011\x0001 "\x0000\x0000@DÈ¤÷I¢öF²Ûll6a(Zë>}þjgµUçÓY­Õ/_½~óÆýý+§ãI)a'ïß¿3¯ÖVRÌÞ»±°\x0019åÅÇ?ÿçÏY\x0016%RD\x0011%D\x00141$Ñ$¢L2\x0006këD¨­\x0019¢Ö õ.Lb(Æi²ÔU&QB\x0004c\x0019d¦ÞªZWÙªìU\x0019Íî`·»1\x001b×ËÙz=Y®'1NÆí2nÄ0\x0011#\x0006eØ\x001aÆqÌãd7æy#QÁÍÍýþÆ4Í\x0004Ã0æI\x0019¤\x0004ÛÍìîæÆÍíÃÁa¿·ÝlÌÓd\x001cG%Â²^Ôu\x0011\x0011J	½u×ËÙõz1L£Ývk³ÙÆÑ4\x000ca\x0012\x0011R#\x0018A\x0019(ÑA ¥ÞªÖ\x0016­\x001eõåI»þ¦^õAj,Ìe0oFûÁÍíÖáö`ØÚnF¥\x000cDê@1\x0008((""¥\x0018"(!"¡\x0018¢(\x0011\x0012R%D	Q(C\x0018þø7?þ @\x0008 JPD\x0018üÿ	ÂÏ¥Û¶í0¬k½¹Â\x0017v:é^Ä\x0005@Â¢h±,»Ê~?=Ú*( Ò'íôµÖsôîÖ¶mõüü$óùdßw//\x0017·ÛÍ¶mö}Ws*Ð&Ð\x0000`YÞ<¼õöí{"¼^^íÛ4çnßwûæÜmûnÓ>§}ªÊ¾OO_}üôÅS\x0018D\x0002Hn\x001a!DLÞ<ÜyÿæÞq\x000c´FuÛöÝ¬)2\x001dÅñpp<\x001c-K\x001aK`Û6¯/¯ÖÛêt<úðî­·oÞè^.¯n[iCfLîRZ\x0004\x0004Ýº\x001bÐ \x0004îÖÝ »\x0001­»UîÖÝº[U»\o^^^\x001cG\x001fÞ¿·®»ý·ß»ÞVïÞ¾×\x0008UmÛvwç;_¿~u<uóúòâîîlV¨ÙÞ½}ëÝÛ·Þ½{ãoßyþø?ÿË÷úõI6º\x0008\x0011!G\x001a\x0019*JkCç°Î]Ç¢#Te\x0019"è.ªt\x0017\x0011*è\x0008Ëáäxº3\x000e\x0007ûªËX\x0016\x0011aßwsßìûÕº]mÛæx8¸»»SÒºífµ\x0016îïßz|÷­ãÝ£±\x001c\x001dgww÷îÏwNç³±,\x001a³¦9wÇãÑÃÃe\x000cÐÑ\x000eÅùtr<\x001cO'\x000fÞ¾yãññÑápÐ]º[D íûêz½¨¹\x0008Ý&B.\x0007ÇãÙétçx<\x0019\x000b´\x0016\x001a]¥º\x0008"BjQMÞnöõýöyýI]ÿl¿ý¬öÏª^tOÝ\x0003DÉ,Ëaq:-î\x001f\x000f\x001eÞÝyóöÁýã½óiK\x0012e	K\x000eL#B\x000e2Â\x0018)3%-9F¦\x001ciÉ2äHH¡uîÖÝBÐ \x0010"\x0008éõõêþé½^.#¸»»\x0017"hÑ©A@#¨º[M2[\x0008\x0019¡u[í·\x0015­ÙmÛ7U\x0005ºCw@x÷æ­óùÎ¾íæ>­ë9ÅDÊ\x0008]¥k\x0008ÇãQ7×uw:¤¦[4]¼¾Þôübn»·î\x001eîÎ\x000f2Ó2\x0017×ëêõz³n7oÞøÍGKüãiñoþÕÇÏ¯ªÊr\x0018Ä ·Í¬\x0012nº\x001b\x0004hÐÝº[DèÖ

º[Dèn
\x0011¶múùçONÇwoÞ8\x001c\x0016\x000f÷\x000f>~r÷ÉÃã½Ûmõøæ­××W×Ëãñàr]U·õúêx:øío¿÷ùó\x0017ïß½ñøprw:ÈýêóÏöüù«l:BEÝF®i«\x0016{X(æ¾é\x0018:JwHû¾;a¡º-1tëjYáñþ\x001dä«e¤ÃÖËEºê½Ô\í·UmSV¦Çwâpçòú¢nõë'wý·î¿ùÞ¶ïº¦\x000cÔ´ï»9§ãÎç³»óÉ2\x000e\x0004\x0011áp88\x001eÆ\x0018"BUë*év»ùòåãñèññÑ\x0018iÎÝ¶­îïï=>>\x0002Bf:\x001c\x0016¡æ´o«ª	b\x000c¢)j\x0017Ý¢[ÕnÎ«ªW=_u]èÕÐ2B%1î\x0004ºZä"2°(åÁÈEõÅ\x0018ÓÈaîírÝ<}Ý¼¼ì®×Í×/íWK¤\x0010Z\x00119dÈ\x0014\x0011\x0000tÈ\x0008\x0002BBñ÷û7ÿ\x000bD´\x0010\x0011\x0008\x0010" \x0000m,\x0007\x001f¾ýNDøãþàþé]®«÷\x001fÞ\x001b#Í}Wsª¦»\x0008\x0019¡ªmûn]WÛºsµm7¯WÏ/Ïn·«e¤Ãáàx:\x0012áv»ÙöÝÜwÛ¶Ù¶mÛìûj$w÷÷\x001e\x001eï°­«®\x00129ÄH\x0011¡»Õ,UE·ÈAhc¤e\x00192B\x0008)"ÔÖuU³\x001cå Ç\x0019ÆHc\x00192Ò6wÛ¾\x0019ÁãÃÉ·ß¼óîñQ×æõõÕ¾Mc\x000c#SC\x0005Mwh \x0000D\x0004\x0008\x0011D\x0008"BD\x0008\x0011\x00108\x0016ß|xçt<¸m»ëõfÎÝÝýYàùéÉ7o<<Ü9\x001cN.«uÝ\//p>¦ûsýf¿<ùùO¿÷õ×_ô"Bf$A\x0004Ý-r9Ôl³1ÌY"C""\x0004¢ZDÈ\x001c:¸ÜVÛ,\x0007ÇÓ½óý£·ï¿ñðønYÞ®æm5÷*)Ð\x001a³\Ü=¾5ÆÐûMÏÕùáÁã»w"Òºí¶mSû¦»u02OGo\x001e=<>¸¿pw>;NÇ£Ãáàp88\x001eOÆXlÛæåõUwËLp8\x001cN'Ër°,Gçó½\x0007ÃQD"-#\x001d\x0007Ë2D¦ÌtXN\x000eÃ\x0018Xz\x0012óÜ\x0016õ3ógQ?K,ùâ´óñàx:9\x001e±\x001c\x001dN\x000fNwoNg§óâ|>8Nw»óÙýÃ[ÇÓQ÷Möª»l³­Ûp[ÏòðÁûoþÚ\x0018GÛzQ2É1D.\x0008c	)3\x0010Ð
"h\x0011d\x0016ADÐ¡»5 È@\x0010tÓ==<ÜûÏÿùòõé«\x001fþÉ_~úE£meÐ
e±ä°¯7ëzu¹\lëÍ¬)"\!sÈ1\x001cÅéx4Åa9ÈÛÍåòjîS\x0005Á81,Ëâî|§Ëõjßw/ÏÏ¶}Êm\x0013\x0011¢[f\x0008\x0019!"u×ë&®©úÓÑ\x0018\x000c!#6g{½\EÙå|>YÆÑÝÝÁñtïáaõòzqy½¨ÚíÝý½oþão}ÿÍ£\x000fÿô\x0007ÿøÏôåëUG8\x001eS
ë6u\x0017\x0008\x0019\x0000\x0010\x0002\x0000\x0011\x0001 »\x0001D\x0006&Çp»m~úù\x0017¿ýÍ÷Þ¾¹GéY²§óý½õvõåÓ¯Kº¿ôáý[\x001fº}ú\x0014Øé°¤º|õüå£õrs»\D1RU£ êFëÚõL\x0011C\x00065[rî´¤ZD\x000c\x0002öÙnÛÍX®¶Û«~û \x0016üòãÅ~qÉÂ¼M5§\x0008¶­¸ìÄªkWÝÞ¼}¯³]¿øøçqw>:=|ChÃaC\x000eF¹È\x000cU
"Ò¬Rs\x001ac±\x001c\x000e2SuÛ÷²\x001c\x000eÞ¼yôíwßH)´Dè¢ºe\x0008\x000eÇ£ãéÎÈÔ=Õ¼éZÕþÌúÅ^Oºq\x0011y½é¤»ÈI&\x001c'1Ê)ÉdiDQW½?éýjÆ¦º=?\x001dÝnÃËky}M/ò|	ë:ì\x001dîîn¾ÿnÈqtÿæËÓ¦öÝD£iZé\x000eÈÐZ$)E\x0004\x0001D%¢E\x0012Bw\x0003ZkÕ!cH¡µ©=¾yô·û÷~þågÃª°îÓ>\x000bD \x0008ðððÆ7\x001fÞ¹]^ýòËN§áv;¸]WÕ-"À)¹íºÊÜwû¾\x001b1GË!½{÷Ö·ß}k\x0019Ã%\x000c_¾~uùñGsN³Z\x00175Ë¾m(Ëáà°,b\x000cPÚek/ªÊ|ûÆû£<\x0004BDÈ\x000c­Ý¶WUíþîÎéxp>Üß=>Ü¹^¯jf­öíâtZüÝ¿ÿÞÛ÷o¼{÷èû?þÅ_~þ¬vNÇ!3Ü9§ª\x0002\x0010\x0011\x0008Ý-"@w\x0008Ð\x0008D\x0004hh4ªðô|±þÛ\x001f­·\x000f\x001fÞz÷æNÍéx<¹;ìë×õv5Æb½½¸;ýÃü®Ía99´~þ×ÛEÝ.R3R\x0014s7p\x0018!ªtÐZWéA×MäAH*d\x000eÙS6£Ý\x001aÑ!3\°¨¹Û×u}õòåëë«q8øæßZ_EíÆù&Ïæmenj_íu5#¬UöY2Òãã[§»i}òúóïÅÞþöï,wä0BEw»^¯Öus<\x001eÍY¶ms:Ý9\x001eÏàx8\x001aãèpX,ËÑÝÝ\x001bÃâp8\x0010èÖÝªJuÑ!G\x001a\x00192C&\x0019D_ÕvSÛWµ}²oÍõÚ¿ªºp\x0010\x0006.Ñ%¥!a9ã¢7s~VëW³ËÄ¾_mÛnßN.ëÉë5=_Êòõëêr)·ÙâpçþîàîHäjÛ>êý*e9Z·IL©\x0010º\x0003"\x000042À\x0012ÐA´\x0004ÐÝº(b\x0011n\x0011,KZF\x0008joªE\x0007\x001d\x0002¡	ÎÇ£ß|ÿ\x001b#Ãoÿê7\x001eß<ê\x0019¾|ýêÓçO¾~ýêúúj»ÝlÛjÛ7Û¶\x0013­óé,sxx8ùÍo¿÷Ûßü æôùógëÍm»úúõÉóÓ«¹\x0017¨.û,ÕSu\x000ba\x0005t\x0011A\x000bÛl__nªèº÷öñÎ)CfhÐU¶ms	"n\x0011G§û£ûóÁãÃYíåz½øúüÅíúj9\x000cß¼{ð_þÓß¹¿»ó¿ÿ·ñ/¿ÿÉå¶[\x000eÈ£Ûm³m»î\x0012¦5\x0000\x0000ht·n\x0000 ªÑºn"\oÓ\x001fþø£¿üø£Óéà°\x001cüæûoäþnñáýw.Ú¼}¸3Æpw<9ÞjÃ2\x0016çL½ÝDýÅº^Íj\x001d©bX02µÞ2î¶WI;{°´LF\x000c\x0011Ðt©\x000e\x0011\x00149q\x0010±ª9]_^­·Íá|öáÛ\x001fÜ?Ü{sÿ\x0006%ºDM£¹»¼<ûòåõòl»^ÙÚ8Xgyóxï´\x001c½~úèöúêí7ßyóÝ\x000f.×«mîî'c\x001cìÛôôôbßÛãGËáìx:¹»;[ÆBaYn\x000cZÙ·]U#\x0010Iæ\x0011¢wµ]­Û¹}Vûgæ7µ_t]tmºW{MCæYÆQ\x0004\x0019íp:\x0018KZ¬F½Êí£4ì·\x0017Ûg³§½îmûË½õäåròùËîéy5{ºn9ËÃã£7÷÷§\x0013Ýj{¶Í6çQ\x0017û2\x000f2oØ\x00161hZ	!2@\x0004®ÖA :t·% BHÐ\x001aÐÝZË \x0011Ãz»ùé§?ùüùY«Ì\x0010FÐ\x0011*RÄ\x0014Ý®¯ÏÖõÕwï\x001f¾ñßü;ÇÃÉËó\x001fõñÓG_¿|öõó'OÏOn·\x0006@Í2k×n./~ýµ¬·«_ùè×/O~ùøÕçOOæ>L³§6µ¡æ´u#d¦ÌÐ
Iêò|]u·jÞç½±\x001cD\x000e!TÑÛ®»Deî\x0013íÍãÁéx\x0010G\x000e\x0014Ù¾>}õôôäxÛ\x001cÆÉø÷?x{ïþîÎû§ß{¹®2\x0016\x001c°m®\x0006Ý\x0006´&´@#@D0\x0008\x00101d\x000c#[D\x0008Ióòü¤÷«Ó1õ~ï|z´áîþA.\x0007³Bu8b\x001cäá\x0007\x001fÃñäé×?»]®Jª
V\x001d"\x000e"Z\x000b³1ÈÊ.ÑE®1\x0010MD:\x001c\x000fÎu´ä Ù×WÛz\x0011UÖË³\\x000e\x001cÎ§£Úéxöþ7íÃoÿ/~öúôÅíru}}¶îÓï-\x001f>xëË³O\x001fýöwÿ`?\x001c|ùò¢;½y{rÿøÆºOûÜÏG§óe,q00 Ã¾íö9uÓcLÃ\x0012\x0011ºK×4çÕº½ë\x0017ûöÉÜÕþÌ|½\x0018:R\x0017a\x0011D\x0012L9BÚ\x001dFûþÛï­ûW_?ÿ\x001fr[uÜ1\x001e\·Ëå[×íÞu}ðñëôñËÅ>¹^].7c9x||ãÝÛ·Nç\x000fß|0ðëÏ¿x}yµ\x000cîÎwryÔÑz}5ÅX\x00165w:éÒ
´ÐR\x0004î\x0012 T\x0010Ý¢ÓÒA\x0006:t5D\x0008ºén)m»ùóÿäååY7Cw«.$V"¦ÛíÅù7·×b\x000cµ=»¿¿³­«ívqÈÓ¡,\x000b¢´F\x0008°ÏÍåò´lb\x0000\x0000w\x0002IDATjÛn~þù'´eÛËm
/¯«}h¹¤¹Oºõ,ºÕ,Ý%¢äxp^Î"B÷D1d´ÛÖ~ýzQBä°<,ºK÷´m;®j¶}ßms5÷·ïÞ8\x001f\x0017\x001déx:;ÞvÏ¯¯^^."n\x000e£ï?ÜûÿÇ¿s^Â?þë\x001f|zº"e\x000ec°¯ÓE\x001c-"d¤9,1XÆ0FZF\x001aeX\x0006iä\x0010\x00112Ú\x0018a\x0019ÃEf {Wsnç#÷÷w\x000eÇÌÆád,G\x0011ÈÅx|ãñÝ\x0007\x000fï}ùËï=¿~Q3,1to¦¢Cw«.\x0001ÍÐZté*m7Æ\x0010]2ZÐ]Bè2Ú²\x000cçÃ*sßÌâåéõv\x0015eq>v\x0018í°\x001cäñÎñt'³»oîÖÕz}õåëW_?}4çôý7ß8Þ¸\.Ö×g§ó£ãá¤»µ°\x001cO¾ûî;¢\x001cÅápt\\x000eN§óýÑùî¬ªýòó'ëÓ\x0005Sw1é*êbÖ«¹¾êõÕ¯öùlîÏjÞ$RÐg³RÅ²ÄÉÈ4ÆÙÂEäEÕ³Óâ\x0007Ç»ßøõç?x}ÙÜæ[¯ë§ËÁí:ÜÝ«\x001cýá§õéógÎÇ»ûG÷÷\x000fÎç\x0013¸Þ®^_^¼}óhß¦ðpÿàîtt<,:Oúôhtëj_W©ÒÝH\x0011è©#\x0004h4\x0002!2¶DÐZ\x0008\x0011\x0001BhÕ%î\x0016hëzóõËgÛ¾én¢UªÒ $2èB·ízõ\x001cÓº­>}üY\x0004sn\x000eËp<m{»\\®/®×]Æ°,ªr½n.Ý¶í¶}£ZÆPÒlºéj\x001d\x001c\x000e\x0007}f.\x0002U»ªÖ\x001dÒpww\x0016\x0011Jë\x00081Bã¶·O¯ZHo\x001fï1t±­SõjVÙçnßvûÎã³Hæ¾Ëåèþ~±­Óº^].¯Æzóöþì¿ü\x000fëÝÛ\x0007ÿò\x001fýúéÉº5j¶¹O1Êé´8\x001e\x000eËÑápp8,\x000e#%ad\x001a#H9BF "hjN­@ ÍjÕÓ­Ã,QÌÅrXä c:áx\x001aN\x000foD~pÿðè|ÿÆáÏÿäùëgªu
Ñ­çTZ5!d´®©º¨2zX\x0007©\x000c­j\x0012IÐMQ¶}¥ZWs7¯¥12Ý\x000e7Ë\x0018ÎK[\n¾Æ\\x000eN\x000fo,cXÎî/_¿¸ýú³ðáý\x0007§¯¿úñÿì7û?úîß8,Ãéx4Å\x0018iä9NgwwwNwge¨*×gìj¾¨ý¦êªöWsÖóUÔªkeÞtL]¥"\x000e"\x000eãY,!ºÅ|±Ä\x0017\x0019\x0017ÙSÎf9Ëë<ú×??ùðáo|~þÏ~ÿÇ¼¬<¿¶ëíÕÛw\x001f|ûWßéÞ¿{ãxHoÞ¼u8Ì9uOÝeázy¥Ë»·\x000fÞ¼¹·Þ\x0016Ë\x0008sî./7§ãÑé´ëjté\x0004ÝÒ\x001dD\x00084t£\x0010B¶@\x0008ÖÝ 3*-D´}ß|úôIf #tî\x0012hzê.U-"0¤E(so³Ú>K\x0015\x0011¥«è\x0012Ýtk­»u}î¶¹Û«T5M\x000b³Ú:7sî\x001a%Ó1\x000f®vÚí\x0015B\x0018ÑlíÒW=iÜße¦î6;d\x001clU>?½Æ;K\x001eP½Û÷2çê°\x000c=[ÕÛ¾9\x001c\x0011aDZÆÁññÁr;øúôÑåòjßw§ãÙßÿÍo|ÿí7~úù>\x0013L]e,Î'çãÉa9\x0018c\x0018 \x0011!ÑjÕÓìÖÝºJW©
Ý¥´êÐbê#D¤TF¶\x001c!³dìt«\x0019nÛUo\x0017\x0019Óéñ½ÓÛ\x000f¾=Ý¹ûÞÏøG_þ=['ë¾³oÌICs\x0012@O*»ÖjÔ:C&s_\x000eËbî®\x0008¡6«l½Ë­1ôÓÂÛ6u\x000ec¤åñ­ãÃ[÷ÛîéëG·×¯^ÐÛYS\x001eÏþî?ý\x0017oß¿w\\x000er,Æ8\x0008Ým$¦ÛËgÏ·¯^_~õùÓ¾~´­7Ý»ª«îW]W£Ë\x0012CÆ°×TÝj¶®ÖZfÉ\x001cÆÒNw'§ó{Ña»üÑvù®/¶j³\x000e¶zpÛ\x001f½\¾¾.ÖÙ¾ÿáÕåúà_^Ét<Þ\x001bKx÷áÇÇ{_>ööÍ[çÓ\x0019lÛÍëåU\x0006ïß½u>Ø\x001eÎZùúå\x0017ëºêYÖæÖöµÜÏ\x0011¶ÛWÛvÕ=¥¢S7\x0011\x0001º[7ÐÕ ¢E\x0015dXD \x0004@\x0000\x0004ÝD iºy}}±HCfªª'A\x0004ÐÕö}
 R\x0010"\x000eØ\x0016I!î B\x0005Õ­ªU\x0012\x0008ÑÌ*sfµîÔ=Å¾ºÇ1¦îÍÓ\x000c\x0013\x0012±Y®×F\x0004÷äÐ å\x0008:í5}~¾Í,Þ>Þ\x0019\x0019"\x0006ÝªÊ¶îz¡­Xp>,NÇáxhF:\x001e\x0016÷ç{fÙ¶Í¾¯Nç³oß½ñþÍ½/_ßx}y±¯7Ým,áp<8\x001c2Dèn¥DµlºÛÒJtÑ­»Ð"ZäªCuh»ìÔ\x00112\x0012Bæ0F(\x0011,¶bÛVõõu]-ç\x0007çûw¾ûÝöøþ;¿üá½Ï?þÁúúÊz³¯an\x001bÕ"\x000e\x0011!s\x0008Ù%j7{ÒLD§\x001cÃeDJ­ºF\x0008Sè""tíjnf\x0019\x0007µ®Ö}jáë§nëêÝ7ß9\x001f\x000f7z_ÍuuùúY\x001dj[õÜ­'ÿñ?ÿßüð×Gõz³í¯öõ«}ýj®OöËG××n×O¶íF\x000cG9Nq4·ôÔµµÙçnÎ)a\x000c\x000eKZFÉÃÍáxt8\x001eDÞë.ëÕåex¹¤Ëzï²Þ»ìw/íë×'Õ/®õÅÃã½ûÇ÷Þ¼yðÃ·ß{yyV½ûúôÉóë§¯ö}\x001a1Ðä°¤Ún>¿>Û¶hÛ­d¦4·rÝ¯Új½Ý»?-¢Õ~Ó³´&\x0008nª¡\x0001D Bk\x001dA·¥\x0005Ñ\x0012­4"è\x0006"\x0008]¥»éPÕD\x00080kª*jsNûÜD\x000eeb¢é\x0000:¨Ò]\x0002\x0011)\x0010Zè¦!\x0008ÕaÖÔ\x00152Â,fÑEw«nÛz¡w\x000fÑÖÚ½6³\x001dd\x0018*¸]¯¾(ÝåññÑá°è*Ì¡#lûîËóUWszópr<\x000e\x0011)´î²íj\x000e\x001dÚ¢kSs\x0013\x000e"	át8ÈGëÅåvq»^Esw÷àÛ÷Î\x000b?®Öu§è\x0019*R\x000cD\x0008A´ÐhÕÖ"\x0002Ñ"\x000eÝ¡ÈEZÌÙ:é\x0008!#Á\x0008D	d\x001cì±\x0010a»¾º]¯z/÷ßÿÖ\x000f¿û\x0007ßüÕßøéÿèÇùß¼üô\x0007[=BÏ¢[d\x0008¡0uM]ÐR5K\x001eÌ}SX\x000eT\x001b\x0011r\x000c{m¶©÷¢É\x001cæ¶ÞU\x000c{2·²\x000bÝe]_­ûf\x000cÜÝ;-Gß|øàËç._¿êóYÎÍ}µ½|uyúâoþáWËádßnFÜ,ùÌüdnOfÝtoÔ.ê\x0005\x0018NÇ;Ë8ê.ûÜí¦2¥)s·vXÒ\x0018d0¨¡ö¶miÆÑì¿âüÚ]oÏ~~þêëÓ«¶\x0011i9\x001c\x001c!cJÓ\x000fß|ë°°ÝÍýêåùÉO¿5Í½¤!#hµ¯®ûª»e\x001c©µ}ßíÛTûT5å\x0008{¶=Ê0õª¦@Ä\x0010I5\x001ah\x0010\x0011\x0008@î¶D\x0010M\x0007\x0011\x0001@\x0007Ñ@\x0010#u7\x0015JË¥\x0010H{µ½
è6«TMÝ­»µÖZ££\x0010Di­\x001bB"Ð"È`tH¤¦[ÍF#Ñ4U¥zê.ë¶{Ù¯ÇtÒ\x000e\x001d¶\x0019:(EL#¨l·ÛÕ¯¥º½}óÆ8,ª	!3aÖôt¹jmVyûxç|\x001c2B	°Í]u©>éz¶®2+N\x0018éGËñä¸¾q¹<Ù×«v>=ÜÔ|çË×'Û~U
h\x0004\x001d-:¤¡ÖÐ@\x0008¡u7\x0011RÈ\x000c-t·e\x000cÝè&ÚÈ!2Ù"nºI´6´ïÓ×/àáÍ\x001bßüÕßxxÿ÷ß|ë/ÿø¿úùßþ»Ûóº­æ¾\x0011M\x0011Zh\x0019)ºU·î&Bç´ïS\x000b\x0019¡#,9t\x0006Eå´m«}¶ö½Ô¾É(µ·­[Ç°\x000b\x001dCw\x0011íõé«y½¸?ßûæo|óþ_×\x0017ëë³17±¯zî~¿ÿW?ýø'\x0002\x0015\x001e\x001fï|øæäÃÅy9¼·ÕÅÈ«\ZU*i\x0017V5o¶íIÕjäÉ2R.»ÑSFLå`­½îU?ªõ­¾ÞÙ;\x001cGïßÿÆoþêÎ§Uüê\x001fuOÓAF.zº½<H·.ûr\x000cCU\x00191\x001c\x000e\x000bÕºwªd¦1BD\x0012aî»}îº[\x0017c,± hK¶9oºK5­¨ÐÈ¦£D\x0004BwÖ
!\x0002\x0002,\x0019!:\x0000Ð"Bd ´\x0012\x0011\x0000º\x001bÌZ\x0019Ks·í9§}ß­ÛÍº­¶my¢!Ð"Bd\x000eî\x0010h\x0011D\x0004 \x00112\x0010\x001a\x0011!#	º'f+¶é\x0010Sæb\x0011\x0012[£[tënÑ­mÛ½¼¼È\x0008ñøèx<Ð!\x001cC7m/__nªÃû³óah¡Ì*óvµÇp<,f±ÎW÷urw>9,1\x000eÇtZÒõúd]Wûms<½ÿðÎùîÎç/OÖí&¢EN\x0011°H\x0010BdênªIB¨JÑ¥5Ý"R\x0008¡EÒ\x0011º®"\x0018#e&\x0002\x0006¢
\x0013e¯\x0012\x000eFu¿ùüù£Ó_þèááÁÃùÞñ·ÿÑñðèx÷ÁÏÿú_½~úY\ÂÜ§Ê\x0016Ñ"\x0016\x001d¡´ª©;Åhf«:SæZU	ME#ÚÜw\x0019edÐ¥gë(sb\x001cÈÐû´^®jÛe××\x0017ß¼güð[¿þùOöË³Û\x001cfmns:ÜV!]×éãñè_þÝo¾q·\x001c,ã$zs8ÞÜ\x0018SXéÕÜKäPu£®2KôÁÈa9<X÷áº-¶z°ÎÛÖ}ØvôWU»Ó!Ü^?ùr>yy¹èyñpw0+PUj\x0016=Ñh\x001dat\x0018i9\x001fp\x0014Ð¥ö]Õ¦zj­»Ñ"RÅñp\x0014ªË67snöY:Ò\x0018\x0011Ì\x0015Õ¢¦£UÓÝ"\x0013-"\x0010º\x0000\x0000\x0004K@ÐZ\x0008\x0004\x0011\x0002\x0004\x0008ÐQ ªEp>\x001dm\x001b×W>öúòâë×/.·ÕºnÞ½yôÝ7ïi"R4¤\x0010të¢²Ð"h\x0004\x001a%"D¤@w\x0013AÐè¦ÑÕªÊÞíÚmÙÊÃaXÔ:¨\x000eÙ¡+T\x0014\x0008û>½¼¼ªnîÎg\x0010Z\x0004-­[ûò|³míÍýÉýéà0BDÓ¥ÛÜ¬ÛætZ\x000cýÊÜyóxïx\,K:\x001eïÜÝ-.í¶ê*ex÷öÑùîÑÓóëõY÷\x0014\x0011\x0002Ö 3uCS¡î\x0012\x00112j¨Y:¨Ð9D\x0010\x0011\x0000hÝM·\x000c"ZEËnÕm\x0011z0k÷é\x001f¥éÛ\x001f~ãxºw|xôíßþ'ËÝ£§\x001fÿàÓÿÕëÅ¾QTn\x0004\x0011!#´@«Y"1SWÙç¦ªÌdîMµ\x0010"(©,¢.Ý-ªÌ9åá ¥¹·eIUÓåòâr>y|óNÎé×?ÿÞz}5÷Í¾®öuwwÿAmÓu^áç__Ù®Òý8º;1òÁÝ·a\x001c¦E»oEüàòüÅeÝRíoÇ7^Öö|Ù½^§§ç«Ûí¦fi!3-\x0011^³}ùøVº\x0002)\x0004\x000102,ã G \x0016U¢WQ!GXÅÝÝi[§1mß|ùúÕ¶ïªË¾Oû6íû´îÓ¬\x0012ÃÑñ°h©öM­«¨]ôÔ\x0011\x0012-´ \x001bD\x0008 \x0002Z7U%2,\x0010\x0001\x0010\x0011@\x0003\x0011\x0001 "d¦îFj\x000fwgëax~z¶Ý6\x001fýäóÓgÛ6íûô\x001f¾ñ7ÿî¯\x0010B E\x0010\x0002\x0016Bf@\x0004Ý\x0000tk­AF\x0004îÖÕªJEØ:½\x0016\x0019\x0002£[ \x0003\x001dZÓÔ\x000e5ËõrÕMD¸¿;éN"VUfMëªé.­=Þ\x001d
Ð"BdØ¶Õ^;q6òèvªU·oïÝÝßÑ'ç»ÛåêõõÅz»8F;O\x000e§·.¯'ÏO¯æÜÑt\x0008\x0000"BDª(Ýn\x0011!\x0012\x0011º\x0008024 ºt\x0003\x0010h¡«\x00042Bwà e}õÓOôùëGoß½÷öí;ãpòÝïþÁßýÃöòñÏþõÿüÿøé_ÿ»ëÏ¬W!\x0016"ÂTæl]edªª\x000cUe7ÍJ\x0011è\x0010ÝD[04ÑºKbh³6*ÁIÐ®×\x0017#ÛÝÛwÞÏòË°^^\x001do7ûmÕ{Û
·Úe\x000cÏ9tÝ,Ûj\x0006u:\x0018cj÷ÞüðF\x001e¶íÁþr§]/wn·Íåº¹miöÛ¶©.sNëu1%EH4:Ef@´\x0016\x00112Z*\x0011M´îbN³vÝ»D\x000e¹/\x0004çÓ\x001d#Ó\x001e\x0007õ³¯__ísÚ÷©@ æ´¯W×º¹ÝÝ(Ø-Ñ:B\x0008m"ÔA
Ý
"\x0012\x0016\x0011 ±\x0004\x0002"\x0008 3u\x0007Ý\x0004@ \x0001\x0010"Úñx°,ÃÜ¦O/_üå§_|þò\x0019a¯r>\x001fÕ," [\x0008\x0011(\x0002DÌ@\x0003B\x0004Fwk-\x0010\x0011ºKÏVÕfMsßu2Ü*¼\x0016Ç(¡d§nZ«&»\x0001MÈ\x0004ëºz~z¢Ûýý½Ãa!Zõ¦jêj« ¦Y¥º=Þ\x001d\x001cÆ@£	hë:-¹;Ömúåã'¯×«\x001f¾ÿÆÛ·÷F¦ÃHÃðôõÉz»êÞ,Ç{o\x001c{/ÏO.×gÝM\x0000Ý­»u£QSÏMW	\x0010Zë\x000eÑM\x0007\x0008MÌ$hèÖ\x0002IÐ\x0000\x00121B7¡tPÂv½ø|Û\¿<;?Üyx÷ÎÝ¿õWýÿôïÿþ?ù·ÿö¿ú?ÿ×ÿ·_ÿøoÖË«Ú§è"JE!EÈ0çnVÉN{ÙSu«\x0008Õ%±D8dX24ö½E0FÊ*=w­E\x000fQSTêmsë){§Ãùí\x0007ï«}úËï]//b¾±¨<¸nõºz}¾s:\x001ejªùl.ÔëyýÁîï¹{pÝÂº?ÛëÅÓVSuÉ
Õ\x0003a\x001cÂñN;$\x0011BK-4B\x0004´FaRSuYfMÕSwk\x0004Z*\x0003A}+×/ª>ÛçÔ\x0011ªÊåõjÛ'ÕJ©.ë¶Ú·Ú¯jnÂ´D{8\x001dóA\x001cBg\x000c!"IF\x0004\x001d*\x0018hè\x0006\x0004\x0001è¶@\x0004-Ð"èn\x0004\x0011"\x0000 Ð "t§\x0014Bê.C7s ¨¢@ Ð¢[G\x0011)\x0008\x0004\x0000\x0011\x0001\x001aU¥ºUÐ¦jÚgÙgéº&ÍÞÃu\x0018-¢fWJI©»UÐ"B&Ûí¦ªt··oßZ\x0007:èU(5§ëdÎ6g¨noï¤«h\x0008!mûÔnôõé¢ê\x0013Þ¾9Y\x000e!s1òäõùÅõöbëÕáxp:\x001fD>hÓåòª»DîÖÝªJWë*]M7B5\x0011´6\x0008¢\x0006¢L\x0019¡#@7 #Ð\x0008\x0011Ú\x0019ºZ\x000bÕìûÍÓÓæùåÉíõê¯þýï|÷ýwþáú½ûæ¿üáßüå\x000fÿæÿúÏ?þ¢÷Õ2Æ"ÆÐQZ\x0008Ù­;Uµi7È!cÐTÓZDªjÝ-Ð]ºÙ¶T2¸iÇ\x001aöàêÕ<ãã£\x000fÿîw~ýñG¯fÿÅ¸{CÌõây»º\x001dNÞO\x000eËÑíö*.?Ùjw{û[o¿µwÐ¶,ÃHh#RÆ\x0010BD\x0013%Öhª©V5uíª¦îÝ¬©«t·®©L"µ@j¡v¶½íµÛ¶Íz»Ún«mÛÍÚu4Õt¡ÂÔ]ºÊÀ!\x0018§t\ÎNËâxXä\x0018D©¢¦è#¥\x0014¹ D\x0014¨n\x0010\x0008Ñ)\x0002Ý\x0008\x001a\x0004\x0001\x0001\x0000\x0000D\x0004è&"d´
"Ó\x0018Cæ\x0010\x0011"RDÓTµ\x000eD \x0010"R\x001bD\x0008 ¢\x0011\x0008¡ÑªKÕD#tO­T·SUÕºCDèf-`d\x0018ÁÞmVÌ\x0014\x0011"\x000eU-¢e&Ø¶ÍÓÓ\x0013xûö­Óéh9\x000c]«Ú7ÝmeÞ®æçÍ¶¼¹;;,CÕÔµ\x000bI´}²®N'ÃÁëëÍ\x001fÿô£õ»÷>¼°d:\x001dï\x000f^.w^^ÕÜe°\x000cÞ>Þàåõ¢jÓN]¡jMw\x0008)\x0016\x0008!\x00042È\x0000\x0010Af\x0010©\x0016H@\x0008\x0008\x0008D\x00041¤ \x000baoÖj{MÕéëçöýj_¿úßýÎoÿýß»ÿßþÝÿà¿ùgÿçÿïÿë×?þº½(Mª)\x000cê]×N¤ÖºÒ\x0018C\x0006ìªÛÜ\x001bt·ÙÌbV+Ð*Øµm\x000cµCVÛ'Õ\x001cïîåù\x000fÿîÞl~ùåÏrûêx8\x001b2Sï7¯}´Ü=È\x001e^×ÕíöânIÇ{\x0007!»¤\x0011º[2¦PºKÏ]ÕT³¨]×¦9Ë¬]u\x0005\x000bM\x0008!!3´0gs·ï»}ÛíÛn]oöýfÎ©jê¢[`$!d¦\x0010Æ8
%£¤\x0010F\x000e9Ò2\x0016Ë\x0008cIc\x000c³¦¹¯ºJhidÊh\x0019¡Ö\x00024 £è\x0010\x0016\x0011 @4\x001aD\x0004 uC\x0010\x0010"Z\x0007Ð2C\x0010
¡}¶\x0000\x0011\x0001\x00141D\x0010AD\x000b­;tÓZU³UµªF(ûæ,UÓ»}/U­\x0010Í6F¡«í5\x0005F\x000e4Zê¦»E0çôôô¤»½{÷Îù|yÒÝjnº¦ÞÛeß¬ëÍåzõöáÞqÐs7«T\x001deÑÝnëæþîì|:¹Ü6üÓO®×w¾ûö»Ó""Ü=ÜÉe¸Ý®t\x001b#õ8ñÎX>ÛÖ]t\x000e .!$\x0011F\x000e\x0011D$"\x001a@f\x0008-E¦ÌEFH¥U\x0017Ý"Cf\x0012a¡ªÔMv[ª¬³mûnöêòtõçßß\x000eÃï~÷;ß|xïÍ»wóÙñþÑOø[?ÿù®/_Ìí¦{\x001a¹\x001bc\x00152ïïN¶\x0019~ùõÕz+sºJwS¥ºÌj[±wØ\x0010ºÚ¬r»Ýdîz¦1WÖÕ¶\x000f§{çÇ\x0007\x001dáô\x000fÿ£q¾÷ã~ïryq\x001c\x0011,Áº\x000e/ûjNeqwwï|J\x0007¯ª¦îivÙkª*U¥»t·eîSwén!D"pÒ\x000etss3÷ÍÜ7sîæ\Í¹étÑ¥»,X\x0006½Ì£Ì4¤)FH\x0019i´\x001c\x000e2mÛ°\x000b4FÈ\x0008\x0019) `\x0016[§
\x001a\x0001]ºÚ4\x0005d@§\x0010\x001a]SKa\x0008\x0010Ñ\x0004@\x0008\x0001h\x0011¡\x0006!F\x0008E4È\x000cI¦\x00102Úu]E1T@\x0008©E´BÆ\x0010\x0008PÍÌ=Ô\x000cs¶î©»íûnßwsNU¥ªTµî@h4ªK4a¦#tµSf\x001c¢\x001b¡»E\x0004ªòüü¬ª¼ÿÞýÝ1Næ>ÕÜuïz¶®\x0017×\x0017\x000fçóñà8JÏr8ÌÔÝ_^lëôøð ùì¶n¾ÿöÇÇ{z3rº;\x000f×ëªf;îÁr\x0018ôõË³õºêÙht¤è\x0010r¤Ìt@@\x0010-" Ì°,)s\x0010©ÑÝZén\x0011!s\x0018#EêVnUa©¶/lënÝw¯O7ÿø¿¿xþòßýÝô»ÿð\x001f<¾¹÷ñÓ'?üí?xóýßx~ú*ææxà|¾ÉüªæTs¡Ó>yûeõåóÅåõf}½Ø×Ú.Öõfn«ÙuÝìU\x000eÇ\x0011ìÝTS»%§½¸Î`\x001cÄ^ãÙéîÞátçxÿÆßýÿä¸üñ÷ÿd½½8DÉ\x000cs\x000f[í^æÁéáÁãý{û>=þYÍRÑfÑ\x001d\x001aÕèÐP\x0014nÐ(ºUê*17=§ª©ªt·vH£å!1DCÉ\x001cÄÐ\x00112ÓÈÅÈ!GÊ\x001c"BD\x0018c8\x001e\x000fªÊõzÕ½é*ºE\x0000è@lÝ)3Uh\x0004
M\x0004\x001d\x00014¡\x0001­\x0008ªÚ\x0012\x0011\x0004¢e\x0004\x001dº\x0001ZD\x0008¦\x0011A\x0019-"u\x0017d\x0014B7\x0011áv]}üøÙå·ß;\x001c\x000f\x0008\x0001ºî\x0016Á2Â\x0018aVÝ¶}ºm»mNÛÖu3ç\x0014Ñæ¶m\x0014Qt\x0003hi*\x0010.0\x0008ª§*"\x0016¢\x0008\x0010\x0011"Bfên¯¯/ªZ½ãñáÎñxçZí6ÕÜÑro·ëÍËëÅ{oîKªnÃ\x0010\x0011¢ÓuÞèöðx/søüõÅºí¾ûö\x001b\x001fÞÞÉ1Ô,Ã°®ËõÅñxôp^Ïïï\x001e|ùòäåë\x0017½\x0016½\x0008\x0019r\x0010\x0011Bê\x0006 "D\x0006\x00024"h!\x0012BT9K\x0004!±XPÝ\x0008­uMUÃ<\x000cÛ^.·Íõúâÿé¿ùøËO¾~ô÷ÿðõýoüùú£ÓÃbí³ýv\x0014<\x000fÛþêùõ«§çWÛ¶XÈ{ùøÞñ¸\x0019\x000f7snj®NÛÍ~{q}ùª>ÿj^^\x000cSÏÖc¡Ck5Ù«T%\x0015ìWóTOo\x001eßº{xt8ýÝßÿ½ï¿yç_ÿñ¿úøËÝö¶\x001bjßì\x0013\x000f÷ÆÃ{7¾®Ö]º©nÕtè¦&]Ú\x0014]BÓBd`\x0008\x0011\x000ccI$2\x0008\x0019\x0010"Bf\x0008\x0016"\x0006\x0011b,å ªÒ¦©'5wÑ\x001b5u5Zw \x0011"R RT!\x0004J	)\x0010ADj\x0010tkÐ\x0004¢u·PÆÿðùÛÿ\x0005\x0000@\x0008\x0011D\x0006@\x0008ÐZ74¨æùùâùån:Ì}·ïeYÈ°Ï©µî¶Ïi]7sªp[wëêåróòòêééÙ×¯O^_].\x0017·ëÕz»¹Ý®¶mUÕ"BDè¢ºh\x0010Ú\x0012\x0008ÝÌ\x00082\x00112C\x0004§ÓÉ², "@fÊL\x0011\x0001h5Ë¶m"Âé|c±ï»}ßì³Ôl³ÚºOÛ,s6BF Ì\x0014Á>§mßåHãÑmÛ¼¼¼X<Ü?8\x001c\x000e(lÛêzyvXÒXÆñàîþÎáxR\x001dæ¾Ì42D\x000c2Sæ\x0010\x0008)sÈHad\x0018KAfÊ\x000cc\x000cËH9Â\x0018CF\x0012d¦BLc98\x001cr¤È\x00109å`,\x001c¡»½¼<ûñ§\®\x0017oß¾±Þnö9¶n\x0017×Ûmo³N^®íùõ¦¡ª¬ûjÝ®¦\x0000"Óáx´\x001cOb9 ôÜD\x0016Ý"BwÛg\x0011ÄÐØ×ËËWÛõ9íëÕö»¿ú+?|xo»]}~úª´Ãùäá÷¾ù÷¿óøá{Õeß.öíbn\x0017½_Ø¯²nXe_\x000c«%6ÜÆt>p>¦Óq8óqq:º;\x001eÜOÎ§£Óéèx88\x001e\x0016Ãâp8\x0018Ëâp8\x0018ccXE!3e¤Ìc\x0018#ÕömSû®kê.5w]Ó»®©»\x0001!Ð\x0010äXf¹ïª&\x0008\x0011!"\x0011D\x000cÝDC \x0003\x00112Ò"\x0019ºH \x0000"P\x0010 \x0014t«J´9DÐ\x0010¡\x001fúÕm]}÷Ý\x0007÷Þ½yðæÍ#ÂóË\x0013Êñxt»m_}}~õôôâz½¹®»mj¶®V]ºKD\x0018Ù2\x00182SFªT£\x0015:@ ¡0Æ¢»Ñ2Ù¶2Æ\x0010\x0011"\x0002@F\x0000ÁºÝ|þòÑ¬éíÛ·\x001eÞ¾\x0017ÏéryQÛ®ºEukO½©\x000e
\x0016}h\x001c\x000b\x0011¶}÷òòª;ÜÝÝûîÏ?}´íåïÞ;,'½íÆ`\x001fáó×gWÓÑé|òîÝ£û»{~9xúúIÍh\x0011@\x0013-#E¤\x0008"C \x0011\x0004\x0004M4Ñ2CD\x0010m\x0019T]ª¦\x00149\x0008"Bæ\x0000\x0011m6\x0008Ë¸s:.^^\x0017/ÿþÿÕ×/,Ë½­\x0016Çó·oùòåËååp'£eìæ¶Zo»«}ß¬ÛÕ^;³ÌnÕÌj\x0007ãá\x0019C­\x0017=oºW\x0007\x001d!»ÔÜe\x000e!tËëÓù|g¿<y\x001båû÷ïü¿þçÿ»Ç7÷>¿<ûðý÷Þ÷ó7ÆØeOmYBæ\x00111d¦H*JH)iD@6Z\x000bÝ-:4R hZknn\x001aÐnÑRµÙ÷]í; \x001bÈL]¥\x00014B\x0007 \x0010©;ÐMGè »u\x0011C\x0004PB\x0017\x0002RH­D7BDX "@\x0000@\x0008\x0002!ÈPÕ #t6ED\x0008¡"d\x0008\x0004:´Wùåã\x0017¾|µ,éþîä»o¾qwwïó¯.\x0017Ë\x0018ºÛ^åvÛ\¯«}/Õ­B µF«lÃH"BfÒ%¢5"\x000c¢é& D\x0013\x0011àv[Í¹Û÷r:N'@#D\x0010D\x0010mß§/_¾³}ûí{oß#ÇâòôdßWÝÌÂÞ.·M×N\x001d=ÜÑÍrhc\x000cÃ>ÛóËUWº»;©~üùWËÅwß¾s:,ÄÑá°\x0018KÚ·Íz»R»q\x0017ÎÇ;ßýð½ãiñôõ}Ýd\x0011A\x0012\x0019\x00021BD\x0010¤ hÖ]ª\x001a-\x0003Â \x000e\x0015!"Ðº¦Ù-\x0010ËÍÐ=RX××þø\x00071\x000eÓ½»7ïÎ\x000fÎ§;·ëÍ¶¾ØgÛn\x0017Ï/_\¯\x0017µOÝmß§mßÕ¤9Û^mVéYj®d\x001flå.§\x0011SÆ42,Mdéq4Æ"r±w«ÛÕ¬íêSp\/¾ûá[ÿÿò?ùe]åùä|:;K\x0013CJ#CD\x0012D$Jën\x0010RkÝSWS­+´VÝº'ÐDÔÕ\x0000:\x0002MPÕ"\x0002\x0003aÖ\x0014]ZûN·Ðªé"2©ÖM# Zu\x0008\x0019CDjtC
´@ @D D·n\x0010@\x0013ÚBFjÐD\x0008-\x0000 \x0011!&\x0010!*¤PQ\x001a\x0011D&n\x0014\x0008\x000c5Ûu®×g×ëôøæëåâùåUW»;\x001f½{ÿFÄbÛ(s6{én­Aw\x0016$ºCL\x001a\x0011a\x0014AkÝ\x0004\x0008\x0004\x0008û¾»Ý¦9§9§Ì2Ch\x001a\x0002\x0004AÕôôôEwùþ»o½÷%\x000f>Ù÷U£µu/UtoªÓÃ\x001d§.½\x001cÄX´éùõÙ¶ß<ÜßL\x001f¿|±î7¿ùá{o\x001fßÓ«x8Ûör»\­·UF8\x001co¿çÍÛ\x0007~}òúòLì2É\x001c\x001a\x0011\x0010\x0011D\x0008\x0011
"¨jº@uè*%Æ BD\x0013iÔ
hZëF4\x001d2f¨\x00109\N']¬Ûê²­ngËá,ò`]w·m÷ñãW¿üúÑËëuÛÕ,U¥gUª\x000bt\x0017A
\x0001\x001a!º,cÑ!¢ÍmÚ·¶ïípà\x0018©½
LSïæõvóryv÷qz÷áoß¼µÞÃ\x00085ZwSÐZk¨©Fwh\x0012\x0011ºZUéj]­5èF@\x0013\x0008ê¦[D D\x000cªKHc\x001c,ËQ\x0017ëzUµiÖ\x001ah\x0008º\x0006îIw©.#\x00171\x0006"è&"\x0014\x001dd
©Ñ\x0008@w\x000b­\x0015AD\x0008Ýe\x000c!Ö\x001a:@h
\x0008\x0011d¦î&LQ-\x0004Ý"\x0008\x0002\x0000\x0006\x0008îé¶n<¿¨YºBU;ïüýßýêòoÿö\x0007//7ë¶»Î«ª\x0002­\x0000\x0010È\x000cc\x000cs)±í
\x0019!:Ð
\x0004\x001d 5ZD ÐU®×«Æ8Ñ\x0008\x0000\x0001ÑºËóóîòÃwß{÷î\x001báËOæ¾ ±\x0017Û®»Ty\x001aÅñÈ\x0012A\x000cÛºêYÎç1\x0016O/\x0017ýÓ/Äðáí£e\x0019ÚîpLq²ÞVëzq¿\x001c\x001dOgoß¼ww÷àÇ\x001föòòY+9RDèZîÐ
D\x0000ÐMDé\x000e©ìÔQt`Vén\x0004BU«.U)bÈH"U'\x000edËÁñ\x0014b,¶}³mëv#ëV>yñÇ?þÅ¯\x001f?Ùö\x001diD\x001acXÆp^±,%,#F¦1B\x0004\x0011\x000e#\x001dF\x001bÊ¾N××¯_¾¸ÜV\x0019iYÈ\x0008\x001aÝ*Ó¬¶öæº¾º¾¬µÛMüö\x0007µ,®-îÖD\x0018:\x001c"Bw\x0010 BwS\x0014ª[ n\x0004ªéV\x0001­LzÊ V\x0010%sq<Þ9N¶íf[\x001bD§lfÒ2S\x0006´FCAvÑ\x001ai\x000f2Z\x00084è Gh\x0008"Cu\x0010\x0011"hD´Fk#C`L	tR-ÐD@\x0004\x0008"B+\x0019t¢ZD\x0018\x00152ÒT\x0000"\x0002t·HÝív[é B »»óùä_~u¹lB\x0008\x0011¡»\x0000\x0011!"Dî\x0006#ÌTUDhT·\x0010B¨h4\x0011©£D¦ªr»Ý1d¦ãá \x0000 [D DÆËó\x001f«ýðý÷Þ¾ûÆX>}úÕÜnrhª¦ëVú²Õî*è\x0010Bv³\x001cÖ}7_¦óÝÙ²\x001c<?_üaû£í\x001f|ûÍ\x001bçãâphçy7¼¾\]^_-#»·ï\x000er|ãçy~új\x0014¢©fO\x001dA£iÐ\x00002@\x0010Cä®#µ1D\x00061Ð\x0015\x001aÝ¥Ð"[æb0EÄ\x0010y°®Õr(ge]¯n·9ËÃX¸ýÁ·ïÎºÊÈaä°\x001c\x0016Ë2dÌ\x0010ÑF\x0010)#@æ Û¶¯ÖuuyÝì5µlýì²îzÓF\x0010BvÉyeM·>øxãz]eÓÛ\x000fF\x0006y9\x001crãÀXD$¹\x001c"BÔ$\x0008\x0010MW\x0008#Ô t£[Ï6÷I\x0014ÝZ)S+©LËñàxºccÞ©\x0002ªíÛ\x000eÚ4k§KDØ'sß±ii­;\x0000¥+\x0010@Ð"\x00189t¢è.ÑA7\x0004¡\x0011\x0008]!",:i"CH\x0015-´\x0000­#Ð\x0008\x0011\x0010ÐZd\x000eÝD\x0002@\x0000\x0000º[Dè¦
JD\x0010áõõÕþô'ïÞ¿s»ÝÜn7û^ª
D\x0004èn\x0010\x0011DÖ"BD\x0008Ál¥tÐI£\x0011\x0000Bh!#t\x0004X×Õår\x00118\x001d"\x0000 \x0010B\x0007­¼^^ýå§|ÿÝ·>|øÆñxôË/?Ú¶UdèfïRk\x0011SuÐ¤Ã0äÂ0«½¾^\x001dO\x0007§ãÁí¶ùÃþäùõÑ\x000fß¾õÛï?8?,Êîp\x001a¾|*_l]Þ¾}ëáþ ¿çñáÞÇ}ýüÅ\7ºTLU-º B\x0004ÐMd\x0008Aî\x00141\x0018CwZÆb\x001c\x000eÆ\x0008\x0003À\x0010AG\x0008@\x0008c	1BG\x0011`d:\x001dO\x000eãÅºmºÛãÝÉ7o\x001fìÛ®k§! ¨h\x0011I\x0017 »AU{¹\o__]®7×ë´W;Þ-#ÌÛÅz½Ø·²D:dXr¸jÏç{7ï,\x000foÕûwîø­ó·¿5N\x000fr\x001ctÐMÇ" \x0010\x0011\x0006D ¡CDÖ"\x0014Bæ9VJ7\x0019I\x0004=r\x001cR\x001b\x0019NÇÃrPM7¡TM¡tMû¶éYn×\x0017¯¯Ï2Ãùtç°\x0014*Ns¶m·ÏÕ}»Øn«}ßÌ¹µèØE@÷$Zuë.ºdî\x0016\x0011B\x0008´¦ÛBë\x000e@fèn\x0016"BF\x000e\x0011\x0000¡5¦@kD \x0008 \x0001\x0000\x0000BD\x0003d]7ÿò¯¿wþËO®·ÍuÝè\x0000\x0000\x0010\x0011 ÐR\x000e¢¥\x0010h
ZÑD\x000ec\x000c1RfHD4$\x0002\x0000Ø¶Í%BF:\x001cSD\x0008\x0010@æÐ¸Ý®~üé'ÕíÛo¿õýoþÊ/?ÿd½^E$Ýö*ê\x00001\x00069\x001cí\x0014c\x0011\x0011ª¸^WsîîNf\x001fúÕåõbÎð×¿ýÞÃÃYÉºÃõu:¦û»ðþ»ßúþ¯þÆ¿üÓ¿øñ/v»\ô^º'È\x0018@\x0010h=!\x0014Ñ"IGEÖ0{I.\x0008Bh@k¥ªT2í³í³tÐ­a\x0019¶tX\x0006Z×ªªT3ç®«µT]ªZWª¦«U¹ïnÛîvÛÜnu2ÓýýÉ2ýºÚÖäáÎv½¹¼^t~xçÝ·ßúðÃ\x000f¾ýí_ûðÝo=>¼u8ÄéH.¢SF«h³ÙgÑ-2,¦\x0016U\x0004î\x0006¢u\x0011H\x0015!"¤aÄÿ <i,K³\x0003»µ¿sUõ=3ó&<ºl\x0002\x0008\x00148 ÿÿ¸JRÅ\x0001\x0005 	Dïáá=U½gs­\x000b-¶6f.ìx>Îng¢Õ½íóD­DQDÂdl³C·l¨ÇýÎãru;Þ¹Þ^\n7Çõ*Çuè>§ûãîþöÙÛýÍçO=§§ÇónOç¹=\x000fçy×ÇÓ>O{ºê¡Ni\x001dQB \x0010@«*\x0019$¨\x0018IQ\x001a1	*¢Ð\x0012@!Ø¨­ Ï\x001f>~jhIi\x0001\x0000Hb$´Ò*ZXk	Ò§Ý§5ãv»:.\x0017Ý[m\x0014H$D\x0012I´õ|<|òÉV·Ûj+"A"báq¿ûÃ\x001fþàñxøÍoþÎo~ó[úÃï}üéGmÄx<OÉHÏO2z<\x001d}\\x001cÇÅdiy»ßµ§×wï­ãÕ·ßýèãÛÿÏ>ùÇßþÊW_^Ý®/Þ½ÞLn¾ýî/þòí·¾üâ\x000b·\x000f\x0017_~ý÷?¿zÿõ×~÷ßÿÅ·øì	\x001d»$\x0019IUÅ\x0000\x0008\x0012S÷,Û]k\x000ef!Úíì¶÷öÜ§6ÎÆsoç.­5qYA]e-¤\x0012\x0012º·ªfÛ»62cÍÈÞ©öp\x001bñ´ÕËÕ»ãæc\x001c3&sÇ§Ïoq{ýÂíåËí½×÷Þõµw_|åöòêr½I´:xÈ>M·næ<³§í4¶Øö>\x0005{oí\x0006í\x0016\x0014-ZYãX±ËiédÙ»Ï§ó|:û¤§îê®ª	&4\x0000DÂdÌZ&ã1kdÆ:®ær³Ëõêr¹XÇaÖxyùàz{/s1+ãâryq¹\$q§Çãáùx¸ßßÜßÞÜïo»£J+\x0019ED \x0005"@Q¥ÕV\x000bc&fD[ÐF@DAÁ\x0006-\x0000\x0004A\x0004\x0014A\x0001$ÑV[\x000444´©\x0011Ç±L«OöfïZ\x0013ËÅy½·L\x0004\x0012I$\x0001Ðòx>x¸\.\x0000@7óùôç?ÿÙÞõÛ¿ÿ­ßüö\x001fýá÷¿ó·ïþso\x001fOçÞöyzÞ\x000e·ër9·Ë®Ëq±f\x0010÷çiÿôÑëë«××÷~úø£ÿüÿý¯þö·¿ùþÍ?úåÏ¿ðr­¾øâæþxõ?ïÑ_þjdo¿üæ/ßÿ[ÿ§?ÿéÏb\x0018\x0015d\x000c\x0010\x0001mÁq,@M¶LÌÄxZÆÌØbî8\x001b\x0015²LÆ
»Oçù\x0010Û©51]ÎýÔÝºZb¬Å:be¬uh·ª\x000cZçYÏçv{ÖóyÚ%³Ìqu¹\]®/æxÇåwËÍº¼8®7³.}n=Oo?~´÷\x0013\x000fkÕ*tÖùÜû¤[{°\x0006ÐªÚÝ E©(¨Ù£û\x0010QuóxnÝu§óùÐnRA\x0010LÈ\x000cN]Z$ì\x0010Î²C[{V\x0005\x00101s¹9¬5fÆÌXë0³d\x0016\x0019f\®\x0017ÇåæryñòòÞíõÕíåæöróá/\x001dÇÅäµ$qH\x0000(UId\x0016 (Èì:³eÈ¦
D\x0010$\x0010BT\x0001\x0010IhQI@\x0002D[Ð@\x0010ÉÈDDÂà\x0004±[÷û]E\x00123£$ÚSB\x0012\x0000I\x0008\x0012ÏçÓ§OÁõ¸È$@i-cs×_þògç¹ýã?þøÇÄ·ý\x000bÆ½ë~>ØÛÆ£ÜvÜöC7×Ë58»}úüÉõrñúòÞ§?úý\x001fúìÿòïÿ­ßüúgÖzl\x001fÞ¿÷|òûßý~ü¯¿üÒL­#~ó÷_YSßÿí'=· "\x001aªjI*d\E"a-m²4±2fÆî8wí]£Ò­{{>kæ4CTU\x001b³Æ:^¬Ä5ÖZf\x000eÁdk·só<Çã\x0019Ï3:ËõÅíõ½uya.dÅ\x001c"º·v{|úèy>=\x001eo÷»ý<éir:V\x001daML\x0008\x0012¨so\x0015I%[\x001b\x0015;Ì0ª\x0001¨ \x0002¤´dÌ:<ÅÙ-\x0013çyªm­nQTÕØ¨ª	\x0012IH$´\x0001\x0006³»4¨¢­}>uNñL$$#\x0006uîmÄ:\x000e·wÎsu±®W±$cÖ2ë`µ\x000eÇõâH\x0002\x0000\x0000 	(R\x0002$JÈ\x001dmÈ\x0004\x0001\x0000U
PI´\x0005\x0000-\x0000\x0010!´\x0005\x0000\x0005U\x0004\x0000ì}:[\x0015dF&Úz>ãp\x001cqîÓyl03\x0019I$q§Ï?s«Ûõ&	(¨¨d¬\x0015çÓ·ßþÅù|ú§þ'¿ýí?JÆ¿ýÇ³ÖÏ§çÞ\x001eÏÓy;äeÌd;:ãÐ,½=o.ÓËë{ë¸úöÛ\x001fü¿þ·ÿìÇÿìïó3·+9ß¼9äoüðã'úó·¾øâjf»ÌøßüÌßÞ½úöÛï¼=b@ºUH\x00043ËÌØ»X3fbfdF°÷io²È\x000cSJö\x0016\x001b[÷Öó´Ï»íÄnÇ1Ër¬8nË:¬ãb¦dÄdd¢ÝÚF»X7ÇõÅu½ã&×YËÞÛÛçÏî\x001fßÏ§ó|:Ï§ó<õÜÚÒÒítÚ­É¸¬Ãq\x001ds3Éa·¢&E­\x0019ëÍyÞ%ËdìsÛÝ\x0012%¶´\x000c	U\x0010!£9$ó\x001c½Eèör=tªû\x0014HiQ»[B\x0001T\x0010\x001ai0Tµ§BI \x0002¶ÉÈ\x000cbcR»\x000f?~ÿ£ÇóéX\x0017Çq1yá<<ïwë¸Xëô|ç©q¶5Ë\x0001\x0004\x0000´\x0004\x0004I@Ä4\x0004É\x000ch(Rh\x000b -\x0000A\x0003\x0000 (\x0000\x0000\x0014$¶Ú­\x001d&Ö1f"³dÆ¬Ã±\x000eÇqHbïÓ>Q\x0000öÞh+¶fÆyÞî\x000f3Ëår1\x0013\x00140Ú"cÙ{ûþû¿ù¯ÿå¿øçú'ÿ÷¿%ñÇ?ýÑ~nÇXîÏíÜOç£ºÇ¬\x000cû¤U2Øowçyzy¹ùòë¯}ÿÃOþßÿÛö§¿üÂ¿ý7çg_\½»\x001eÿìk?üø£\x001fþöÉëëÍí:Vê\x0017¿øÒ»\x000f¯þðÇ¿øé§Oö¹-53\x0008a\x0012XÇ\x0000ª­IìnUTÅ\x0008e÷ÔÒníé|>Ï§½ÄZË±\/ãr©ã`fvÛ;¶¥\x0019ÉÅÌÁºéñb]^¬u#Ën=îw¿ÿÁçO<î=ß>ë>Ù\x001b4Lb&RºÚÊ:¼\nf\x0018ËÞ!£
af\x0004ÝÛq\Ý^^½½ñÅ\x0017ï<\x001e§·ÏoìÓÞ§\x0018ÁÌ¶@	f"³È\x001cÞÞ\x001ej\x001cÇ²Ï§X×åù8Ï'H¨ÐM\x0015\x0005-T\x001aÄ.M¤\x0001¡uî ÎsÛçVµÖ2³t§îR^n/®«u\¬µìóa-f6}lË`[\x0013Àv$Ñ\x0016$\x0001\x0000m%\x0011D\x0012D'²Grj+\x00133\x0008\x0012Ð\x0002A\x0012Ð\x0016$\x0001J\x0015@\x0012m\x0001D[\x0000@i\x0005I$\x0001I$1kYkYÌ¡çé<Om=OçãÉDD\x0012\x0000D\x0012ÄÞÛç·Ïàz=L%\x0002&%,¬,gêÇ\x001fô_þÛñ\x000fÿðþî7¿?üág]%âÜõÖÊýi}^¼F'ö}Ëº[e2àyº?ïÞ½¾úú\x000f~øñGÿí¿ýïøÿø\x001fþ­úí/]ç´\x001fw¿øæKÏç\x0017>}ú¬êúz5¯¾úàv»ùã\x001fÿâû¿}ï|>Í0¡`DB\x0012\x0015mIµ'%mïbw\x0014{oçyÚçö|ÞÏS÷&ÑYö>=OÅóY,3\x0017ÉÕÌÍº¾Z·÷æxuÅrÛýñôøøÉýí£Çý£ÇÛGÏûSwÍÄL\x001cGL\x000eDÔÞ§î­¶frÉárÝm ¬0SkÅZ5£»f-çÖ×wf=|ü|·.79z>E´%´´¡c&ÖZ.×9^üøñÍó¬\x0019Îç÷Å±\x0006Ëy 0¤\x0005-T[-U;U¬.¥â<·çó¡=\x0011k
\x0013çãiïm&1\x0019ï?¼J"Ì¢ÕÄZK\x0013Ïç)¨h\x000bznÝ\x0005\x0007$\x0004@\x0012m\x0001lµ\x0004A""\x0012 !ª\x0008¶h\x000b`ï-¶\x0002Ú¢Â.h\x000b\x0004\x0002\x0004H\x0002ZZ »h·ö	ª\x0016­½·ãX2\x0003Ú\x0002h+¶Hbïúüö\x00197·ëM\x0002\x0004\x0015)°V0>}úäÿü?ÿO¿ýíßûÍo~ãz½ùÝï~g§EËãÉOO}Yn\x0007cê\x000c\x0002Î]?þôw/7_|ñ^V|ûí\x000fþËýï¾þú\x001bÿæ~mßôù§ï½^âÝ»\x000f¾ÿñ\x0007?üô\x000fïÞ;\x000e^_.~ý«o\x001ck|÷Ý÷Îç\x0003µf$°%\x0019É\x0011uOÝ0­ö>µËî¸?\x001eÏ§ó¹ÝïwçÖ]Y¬Ë8ÜÜWõÎº¾:\x0017¹¼³æ\x0002Ý\x001e\x001fÏÏ»ìóÜzìJ·k9!QLbf\x0014öS÷¶»uo0C2.ÉÝ\x0011²bïìeö2³doµÈØ;tãt\x000f·ÛÅ±"¸\¯\x001ewºOIH\x00184fÆÞÛÛÛÃÑ«ÙÚ\x0007j%ºëñ8õ8¬uÁè>\x0015-»ÕÒVË>OmÁ¶mµ²¥§îtÓPÖ\x001aëú"$ÉÈ\x000cBv«È®sÎ½ÍZÖZìÒ¢(8h«­$\x0000\x0000\x0000" \x0010$Z\x0012f\x0008ÈM\x0012m\x0001@\x0012mDÐ\x0016@\x0015Ñ Hh\x0015Q\x0010\x0001mµÐÖÞÛ¶uÓ½Uµ@@(ÅÆ\x0002\x0000@\x0012mÁÌ$öÞÞÞîq½\$£J+!\x0002¨µB\x000eûýu§_ýê×à÷ÿãwÎóé2LíÍãQ\x001fû´ÏÓ¾-/×pnçYI$c\x0012Ïn?|üèqÞ½¼sY\x0017ýö;ÿËÿúÿðýÿíÿî?üûãåýøôãÅÃ\x000fï}ÿý\x000fþø§¿øâý;_~øàXñòrñòzóécõ|a­eï-\x0004a«ÝmOÏ³ÚØª¶vé^Î.Ïçéù|zÛóÜÎ,ËÕõrs¹¾º¼¾º\_¬ãfÖEÇYçç7ÏçOz>õ|ê~8wï^ä8|~ûl·:eGKºíóÔn[HTÍ2	+`2fâ\x0018fÆ1¬\x0015§xZNÙ}ÚY$\x0008ÙîoÝß>ÛÏ»nr½:.Ëãqj+%3\x0006	É¶ÏÚÏow×/ÕÅçßYa­q6Þî§çsË<Ö¬e·ÏS[=·î\x0000	X9$1F²Õ¶d¤KAd
´bÛª¥"\x001dI$£{ÛçIëÜ\x0005×ËaÛ¹+\x0001\x000eE\x0011""´
¥H\x0000B\x0003\x0011U	D2AAJ\x0004´\x0005\x0000P\x0008\x0005\x0010-\x0000
Z
PÕV[\x0000I\x0000ì]mµ\x0005TED
Ð½õ¬¦h\x000b\x0000\x0000ÚJ¢­$·û\x001d\/¬5ª ¡eMärñx<ýë¿ü«ûÛÝ¯~õk¿úõ¯üñOô8OÇ\x001a+çé­§Z¨q»FÍNQüôã'çýôáÃ;_¼ÿàÏýÿåýúö/ßù¿þÇv;^¤w}|ör9|\ü÷ÿþ;}yçË¯¾R\¯Ëä½ûãaí&£âyÚó<=ÏÓó¹í²R\x000bK6q9.ëãf]_].¯.ÇÕÌEqO÷Ç'{ÿ¨Å®:E%¬9]ÖòîõÅÞõùó'zêù´wuW÷F­aE\x001b	Áq\Ì}	kÆq9Ì`oÇÄ

B¶¨¦à\x0004~úhïíù<µì·íååæz¹x»¿Ù{³kf$µ÷¶Û\x0016Ûvßu\ßåqÞ\x001dkÌñx>y>¤\x0015±ÖHbµ\x0015\x0012v\x001d+f\x0016&\x0004Å®
N=+s\x000ch·$b$\x0019Ñso{C(»[[°2ªöãa'ëÅníç)å\x0008L@DÐDJSTD\x0012\x0014\x0010D\x0012I\x00040\x0019É\x0000­´ ¶\x0000\x0000 Z\x0000 	­"h"­
\x0005\x0004H¢-H"\x0014EU\x0004\x0011\x0012D[@A[\x0000I´\x0004@[$ÚºßïÌÅ$\x0012Z\x0002ëåð|þø?z>O?ÿå/üò¿ò¿üÙ>OY\x000b%Ç\x0019yDÅeÕôavÍ:¤KÑ]?}úä¹>|xï¿üµ¿}÷½ÿýÿÿøóÿèßÿôË¿}÷|¾iÇåzõ§¿üÕ·ûèË¯æz½²Nuñö6îo\x001f\x001dyjëynç~êÞçioz\x0006#\x0013\x00123æ`¬µn2/ÌÒ,ÛØ»Þ\x001eoìÏö>µÛ¤fXY2\x0014Ý]µ±=Ï§¾ÿãzuYQK'Z\x0008h7ÝÚ-Ø-­5\x000b\x001cëp¬1©$cÚÝ\x0004JØØ&ÌPºO?}¶\x000bìVpîír\x001c\x001e§½OéØè®´&yJOzzw9Ø#ÏÏ.+^ßßì^ôÜ²·½·½«­I\x001ckìÍóñ4e65Ú(¶l$â)	É°Æ\x0008¨(Rb$ìÍ©&#3ÒMk\x0012kF÷òòrsÿô¦ÏÓ!\x0011\x0000E\x0004B7		\x0014\x0001\x0000mA\x0000\x0011H  \x0001Ú\x0002H\x0002ÚJ¢­\x0008J\x0001¨R\x0002
ª\x0008 ­$dÄH¨ÝS\x001b	\x0000I@[\x0000\x0004\x0008\x0004$\x0001ÐV\x0012I\x0000Öãñáz½H\x0002¨¶\x0000`&Öq8Ï§oÿògÇÝÏþsß|ós?|ÿ½½·ð<\x0019s\x000e8Ö!N{oÙ\x0008ÂÆÇÏo\x001eÏ§/Þ¿÷õW_ùt}ñ§?~ëíãø_ùÙW¯^^\x000eÝ\x000fë8|øðÞß¾¿ûÃ\x001f¾óîÝ×CsàÕ¬q?jvé\x000e$&ä\x0018ÉÒÎ\x0005\x0017Í!ÇM«ö°Å~n»\x000f»§Ø&58\x0012& tÛ­î­{$Çã¡­¢¥-*\x0008*Ö:\x0004éiïJÆ.k××W·ëÅù¼;Ï;¶ÝÍªh£Ý8U³Ù´[ÏSw\x0015\x0019Á~<Ý\x000f#1«³Å*Ë)s:\x000e\x000b\x001e\x001eÏ<Ë9.ë0³±7Ïçv>K«Ýtë¹m[YÌ("Ö,\x0006	%È>íÒ"lä=C¢\x0019fYk\x0019±±Ìr9.Úz¼}ö¸¿é>Íây^oWóÂç~rd¢{\x000b\x0004è®\x0011@D\x0002\x0004H\x0004\x0000 \x0002(\x0000\x0000ÚJ¢­$P\x0004h+ª¶P"Új\x000b¨$\x0000\x0012Z\x0012ZZh\x000b\x0000\x0000\x0000\x0018#\x0000\x0000\x0000h+	h·IH´u¿?P×ëÕÌ \x0000\x0004hEf9Û÷ûÎy~ñË_úâË/}üøQ\x0012k\x0006UÕg£çbÛmIï\x001e÷b\x0010;ìÖyßöù÷çöáË\x000f^^n¾ÿî;ÿÇýW¿þÕW~ñó/½\ëz,//ïÔáíqúñ\x001füøãxýðäp=\x000e·Û\x0017âáã§\x000e£
©\x0013[C]í^$É8wy<pÒ*\x0006+ÔJ$uO=«	 $ÖÄ\x001c$$]vë~¿k«Ýö®¶D\x0012I$Ë¬¸ÌY²®Ö±|x÷Þõrøüé']í"µ\x001bZ{\x0017\x0008m\x0011±ÁÌD[Q³bfP)ºMN\x0003JIb·4&´§>N=Oslçóa\x000fºí½íýtÎi&½Ù'ç®]Òª\x0001D\x0012Ð\x000c3bTu/YËÌ2Ça]®Öåj.\x0017k]d-³âyf-×Ëã8ì]Ïûg?þä<ï\x0019É8K&ë.÷»#\x0005" 	EhK"\x0000h\x000b$º+d@[\x0000\x0000\x0000I@\x0012\x0000I@[ (\x0000Ð\x0016@\x0012D\x0012\x0000mÍD\x0012mA[\x0000Ð\x0016$Ñ\x0016\x0000Ñ¢\x0000@\x0012m%\x0001m\x0001Ñ\x0010\x0001Ýõx<%q½\Ì\x000c¡»\x0002*H8.C~øÑÞõÍ7?óúújïmfì½íl[µç2Ãõ¸èºÚÏ»Ì\x0012hÝ\x001fOÏ\x001f¾÷Ø\x000fß|õµ_üò\x0017¾ûî[¿ûÃ}~ûì«/.~þõÏ¼Þ\x000c//î?üþ¯>~>}õõÏôÜY^_Þ¹nî?y<Î.gæ*½hFg\%)»ö\x000cÆ$&Aíg\x0019ØeÍA"YÖZÖ­v·îÚ{ÛÝ
\x0014ÈÄ1\x0019IDÉ\x0008 ahëÓ§>þôtÿüI÷	\x0002\x0008$ILjBZ\x0013\x0006ZJvIdoV[-0C[-X¨ÑnmÝr\x0002-ål#dik°µY¬C2e}n5ËÕq¹ZÇÅZ¶vÆ:\x000e³\x000e³Y#kY%F\x0013\x0005umí]8a¸\x001c\x001f\x001c/¯ô´&blìÖóqãâH ÚJ"	\x0000IL¢J$Ò\x0012ÈDBDK\x0002\x0000\x0000\x0000\x0000´\x0005D[I@[ÄÞ\x001b´0\x0019B[313\x0000\x0000\x0000\x0000$\x0000 
b&\x0012\x0000 -$\x0000$ åñxJãv»¦\x0014-**µ\x0016?ýdïíg?ûËå*Æq\x001cö~êf­Yx¼=½\Þ±8ïRÕl=ã§\x001f?rnß|ý_üâ\x0017~üá\x0007ýö\x0007çó»§5ËËëò÷±{cnÎýY³=Ï¸^¿rî\x0017¼ñ¤gU´LêrÄ\x001aÎó))%b2\x000c3ÑÌY®ÇÅq\ìsëYÂyÖÙ­»L¬Il±VR\x0011Öi\x000b*\x0006ÓmïÓO\x0019ÏÄd»Øf±&´J\x0018$5è¦ÝP\x0014 Z@Q(hQZöISm5U\x0005»\x001bÌ,Yd,±®\x0017ÇõfÖEfÉ\¬ËÕ¬eÖÁ,\x0012\x0015D[vebÖ2ë\x0019%	"\x00193!£j\x0008¨h\x000b@jBRí¦[±32\x0017u8[\x0011EÃq;|õÍÕ\x0001D\x0012	I@[m%$D\x0012IaW²%\x0011¤\x000531\x0013ÉHC¶¶\x0000\x0000 ¶\x0000\x0000\x0000\x0000fF[ \x0008IÌÉÐV[I\x0000´\x0005I@[I$\x0001D\x0002¡#$ª\x0000HB"!"$\x0000lÏÓZOëEftW\x0000
À9øôùó/ÛW_~éz¹yÿá¿û»¿w>îf8»	?ÿÙÏüá÷¿÷ã÷ß«ít>&L*\x000bbïúøéM÷w¾ùÙ×¾ùú\x001b·ëÍ_¿ûûýÏ¾þê½/Ëw/.S×¬\x0017÷{ýßýÉçÛøÅ/~i-ÌÅõzñ§}ÓVÂå¸XsØ­CfhÍZÚÅÉ(&#³d.æ¸8ûýÍ¹OÁÑj\x000b¨	Á\x000eM$1I$\x0004$DLâTZÇd$\x0011¥nIQDZUB"\x0010JS»\x00120¶ÒÍ>Q-D\x0013-22#d¬cãb«\n.×«ã¸Ê:dee\x0012\x0015ÍD[ÅnuD[miA[Q\x0010)D\x001a{\x0000U
A\x0012\x0014(UÄdØ\x001b¥FCvA\x0015µ\x001c-\x0004ÕV[I$\x0004\x0000\x0010\x0012\x0015	ÝÕ\x0016Ö4´¶\x0000h+	$Ú\x0002h\x000bÚ¶\x0000\x0000h«-ª-hkï­¥»v·½7H¢-¶ ¶öÞÑV\x0012ÐÒ\x000e!¡-¶´* \x0005\x0012@bw{Oïo\x001fÀÛÛBH£»(a\x0012ÇZîootûøýìkëX~úqûòÃ\x0007·\x0017?|ÿ½óqúægßx¹Ý\¯~øÎOßÿÕ~ÞçÃ>·\x0011AË§ÏwúË_=§o~öÛíâ/ýÖ_¿ûÁù<}þø/?¼z}y1ùäv»øå/¾ñ/ÿý÷¬¾ùù;×ÛÍýñ`×Z75.«ËíFÌ\x0010ã0ëE2vÙçÞZÖåp\x001cWãÐryÓ>µLB"b&fÆd$\x0008I,A\x0019fÆjP0!	\x0014\x0011\x0011@[U\x0010DD°»5@ (QíÖnZ°;\x0006 µ»5cÖa\x001du\¬ãê¸\x001cf\x000eYYf-2 \x0013RÑ!b\x0017-h"	K\x00101\x0013mµE\x0011iµ\x0016´õ<O{Úª
@"]\x0004hX5t*¥¥V@µq$´ÕV\x0002$±÷\x0006\x0004´\x001b#(H¢­"\x0019I\x0014\x0001\x0000@[\x0000mµ\x0005\x0000m\x0001$ÑV[\x0000mµ\x0005\x0000I$ÑV\x0012Um\x0001@\x0012m\x0001\x0000@\x0012\x0014EP²%\x0011\x0003\x0000\x0000´\x0006¶ ¨}n///.çãa?OØeC½O///þÓúOþãü\x000fÞÝ^Üwüã\x001f}þüæ\x0017¿øµ_þò¾ÿá£o¿ûÎ$2c]n~þË¿óÍ7¿ðxûìù¼ûøñ£ûÛgk¢=íóôÜõ×ï?9-ßüìK¿üõßûë_¿óãçÓqûàÓóÅ~\x001b·ÛÅÊÛ¯ýÝ?ýÜÛs{Ë\x0007YW3ÛqlÇ»9\x001cë"ë¢3`Í\x000c,ûÜÝÚj\x001dã8\x000e	÷ÇÝ~>é %HH±«=U%µefhõÜö\x0019\x0012I´ìDD& Ý$L(D\x001a\x0015\x0015)2S\x001b @D\x0003DHdu,k]d-ëXeÖÈ,³dQ­v92ÝìêD\x001d- Q¥5\x00034\x0001É¶; `Í8ÃZKÄÌ8Ö õx<ÜïwUÝ§Ý­¶Újk\x0017¶´¶Ú\x0002¤´\x0016P\x000e \x0012H\x0002\x0000 ­$`ïm­HH\x0002"¶"bdF ¡Ñnm%\x0001mA\x0012\x0000\x0000D[mµ\x0005\x0000m\x0001\x0014\x0000D\x0002@\x0012mµ\x0005\x0000\x0000mA\x0012@ÉV\x0001\x0010\x0001\x0000@iµ%$\x0001T\x0012m}ÿý÷®·«ûãîÈ\x0008ªîuøú«¯ý»ÿéßùOÿév>î~ÿ»ÿáí~'ñúúÞïÿ\x0007ýî;?}6shë~¿{üít½\x001cÖÄ8¬ËÕ¯¿n×Ëár½ØçÓÞ[÷¶ÖÈõæÝë{ï¿úgçYk\x001dÖ\x001a+\x00159®¶x[^\x0013mXëp´ZÚ8\x0013óYÝÛxfÛçÓãq·÷C\x0012Äå8\ÃLe?´5a\x001dîÒ-*%"$\x0002\x0015\x000bÓÒjiªH\x0004\x0015\x0001Jv%¥´[\x0013v4\x001bEÈ¨H1\x000eÉÈdLF&:YuÌµdÉ\x00082#ÝR¨¤b$±TK\x001c$Z \x0000
¶Ðhk>O
\x0014IÌý)\x0013\x00113cÍ¸]\x000f×ÛÍqÜ´J-	Ø-è®¶ÚSwíV÷Vì½)B[ûÜÎçvîMë$\x0000Ú\x0002\x0000H\x0002\x0000h«-\x0010¶¨\x0000º7¢-h\x000b\x0000Ú¶h\x000b\x0000 ¶Ú\x0002\x0000Ðj«­$ Ú¶\x0000Ú$ ­$ -©\x001a-mµÕ\x0016D@[D\x0012ÅVÔ\x0008(Ò\x001a13~úéG?þTv]×Ååz\x000c >|øàï~ýwþþ·ÿà«¯¿öûßýÁ~>$üôñ××÷^^^çOÏ§ëõ¢ÈÄu_ÁZµÆe­qÌ²fÌ1.×«Ëåâ%$F¬µ¼Ü^ÌZÎ}zOQ=\x001fî»Î½9OQmµ!' 4±&màQçùtî§Q×ã8H¬Ä²éFHÌ¨Ýj¶¶¤(F&\x0013»\x0010Ì\x000cHF2\x0010"\x0012
\x0019225b1³Ì,Yf\x000cA#b2\x000c
-\x0015vµ§î-\x0013\x0012 
\x0019	HF[ë¸X3ÞÞîH"B\x0000h\x000b¶(¶P¶ ­îz>\x001f\x001eåóÛ\x001b?|@$$±µ$fÆZËÌ \x0007eïhkï\x0013Ðò|>=×ÓìjëH¢­¶\x0000\x0012Ñn	I\x0000$ÑV\x0012I\x0000\x0004\x0019\x00126\x0002\x0000$Ñ\x0016´D\x0012\x0000Ð\x0016@[\x0016Q\x0005Ån\x0001\x0000\x0000\x0000I´\x0005\x0010¡T\x0006\x0001ZmA[mA\x0012I\x0000\x0000Q\x0014	
@KË±ÆõvqÌr½Þ\¯7YW¿ùÍoüü\x0017¿p{yq{óùí\x000f¯/n×«u¹å¸\x001c.×½«JB"D,Ç\x001a3132!qî\x0008ÖDË¹Îót¿¿aËÄår±Ö¡âù|:ÏÍ®ìÐ»ö\x0004Å$f\x000eÛv»,x>\x001ffoµÆe	Æ\x00081+½·vk·$A\x0010É 2!a\x0019V$ÄdÌÄ:\x000e	IÌ,3#\x0019Ö$2!K²dA\x00141\x0010ªb$Á¨\x0008R¶ÚJÙSM´[\x000b\x0014\x0019tl´!Cê8\x0016bÖ		
H¶Ú\x0002ji+3\x0002h+¶FX´±wíM[ÐÖÞ<ÎM	\x0015ÉHÖd\x0000%Ñ½í]mÉ².#âH¢$\x0008H\x0002$¶$Z(ÈÄL\x0000I\x0000\x0000@\x0012\x0000\x0000\x0000\x0000I´\x0005
Z\x0000A\x0004\x0000$\x0001\x0000\x0000m%\x0001 U\x0002\x001a\x001am´ÕV\x0004HD¢\x0005R)vDQh-ñÍÏ¾ñÿÜíz³ëõÅõzõòúêõý{Éx{»{>\x001f®×ëíâýûWÇýðö8].W{×ãñ´[)I\x0008\x0019H$\x0004-»íé\x00013$(¡û´÷ér9\®W/×+x\x001csoûÜowçóiO}>ì½%ã\x0016uÚ®×«\x0011-Twm\x000fíYv"3Zö\x0019ZD
scYë°Öa\x001dã8Ì:Ì±Ì5KÖÈI$\x000cL$@@Ð\x0014Ô`JØE\x0011 \x0010D\x000cY@)bkKI+»Q[\x0001Z-QÐV»õµÆ¹ º7!\x0016\x0000-\x0010Új«E«\x0000P¨\x0016hi+!©¶´  \x00148Ï
Î:%¡\x0000\x0010		ÐFBöVq\x0010	m@KBÐ\x0014PD\x0002$E´\x0005@¤5H(\x0012ZÚJ\x0002\x0000\x0000\x0000\x0000\x0000h\x000b\x0002\x0000"	 (AI¢-H\x0002@\x0000\x0005\x0004ª¨ÐhCH\x0006Ñ\x0012aBÉ\x0010\x0010Ð QA\x001dëp9\x000e-ÇõÅíÝ;×ËÅW×ë³ñx>íóéÜÛ~nçYk\x000ekNãAO
µD&&d"SD\x0012\x0011n	inÁt\x001bTdoº]Öx¹^½»]]¯\x0007áz»È\x000c¸¿½y|þìq¿xÞïÏ§¶½·¨§m\x001e±Ïmw£`:Ö\x0011+£+²\x0016ë0k¬uXkYÇa.u\x001cÖ:ddYk¬µÌ%\x0013\x0012I$C\x0002" H\x0008\x0014ªj\x0007(0©$2\x0011Q\x001bA(ÐV\x000bU(Ta"\x0000U
\x0015\x0005ÝUuî­E¶åñx\x0002\x0019ABK\x0012\x0000P\x0004\x0004T\x0015\x0001¡Õ\x0016´\x0005mA\x000bµ7\x0000É6\x0013D2ÚÒ­­¶(* ¤"\x0003 	\x0000¨
\x0000¨ h¢Jh7¢-h\x000b\x0000\x0000 ­¶\x0000\x0000H\x0002´
E)tkk&Ú\x0000ª\x00026´\x0008)¢S\x0002\x0014mDÉ\x0006M41ÆÆ$¨\x0014jÏî®×»¯¾¾8Öá²×ëÅîÓýíîÜÛJmB\x000f\x001føÁ¹·îÓy>I\x001c±dÆ
\x0013&\x0011!5Ù´¢&\x0015¥U\x0015b×)´&qYËåîÓýíÌ8®7ËÕq\\//\x001e×WçÃy>ç©{ë®ó|:\x000fÝ§Ýe%f-su\\®Wë8¬ã°eÖr\x001cYËÌÈ,IdBF\x001a	\x0012¢\x0005"\x0002­$2\x0011´Eµ\x001bCCH`HF\x0012mI$ÄÐÈDwì½iµÑnÐ\x0016@[IT\x0015 \x0001@H\x0011\x0010¥Õ2h9[[mµ[\x0012\x0011B\x0012IH$\x0014A\x0012ÉÐjF] \x0001m%\x0001ÐV\x0012-3A\x0000DKBKK[P¥@\x0012\x0004\x0005D\x0014\x0015\x001c	m\x0001$\x0000\x0010\x0000\x0003\x0018t#\x0004\x0005@%ÌD\x0000m\x0001´\x0005\x0000I@[m%ÑBPmµ\x0004@D\x0015$%\x0000D\x0004\x001b\x0000\x0000\x0011\x0010\x0002AUi¤ì	%­$Òª 6gÈV¡Ì\x000415ËZµÖxÿzøêÃÍ¯ñµ¯>\É¶öÃÛÇ¿¹?ïÎ}e«Y©Ûýãµ\x000c£±Âm\x0012dLª=iDiuW»µ¥´[[mm$1×«5£­ûý
Lç³vCr8n¹mVB2Øöói§î
1\x00133Ã$$2cf$ÑÄÎØl\x0012IÍÄ\x0008ÂD'$"$\x0012\x0008h+$hiÙ{K\x0010\x0002¢­dK\x0002FLÑr[w	\x0011[µ\x0005mA[\x0004@ \x0001I\x0000´d¢Aª "hkf´D&H"H¢­´\x0004$Ñ\x0010Ñ½=Om\x0001´U´¥\x0005-D[T\x0002ÀL0dD\x0015\x0010mµ]\x0015\x0015DT\x0012Ç:ó~"(F2(Ý¨$$ÚjI\x0000\x0000´\x0005ÐV\x0012m\x0001$Ñ\x0016@[mA[D[ \x0000$\x0001I\x0000\x0000\x0000@¤@(¢¨ÚêÜ[jÈ ZSGã\x0018·c¹Ý\x000e×ëáåvñr½¸\x001eÛu¹\x001eu½ÛõâõåÅõòÆý²nv\x000foo§ö´Éaímå0IMJje$Lb¦¦b¶¢û´[-\x0005¥\x0004ÔZ\x0017Çå"3ÎsÛ¶Éhâô0Çére]±\x0012&FÌ\x001a³ÆdPZÂnµ[÷ÖÍ¶ís¶ÚPL\x0008\x0004bÍ!\x0001\x001a-Ð\x00161\x0013mµÕ2\x0013D²$°í½)E\x0002ì½\x0011\x0011ÛÔÌXë°Ö8Ï­{\x0018R{o\x0000I( D\x0012\x0000I\x0010\x0000\x0012U\x0002\x0000´\x0005`Æ@"	\x0010"`f@\x0012)I@\x0012\x0012	aF[{o\x0004\x0014ÐV»uÓÒnIÌD[ñúîU\x0012ÇC[3ãñx8OÝµ7»$L:^_oÏýÜ*¨¶\x0008Ð¢¢­ÌÐ¶\x0000\x0008 ÚJ¢-$\x0000 ­$Új\x000b\x0000\x0000h«-\x0000 ª\x0000ÚÒ h\x000b\x0000$
n¶Ú­Êp¬±ËÁëËÅëËÕËíp»Ûuy½]½Þ®^.W/·åv[.ÇrYã\x0010p¢&\x0011§½ÒÖÚwÖ\x0007¶]Q5ãX\x0019!S\x0013&0\x0001ìjh«­¢­î
öÞÚ\x00131¢EbÖáxyËMgÈXk9ÃZYËåzq\b\x001dCÆ$f"	\x0019ÉXk\x0019\x0004µwµe×Þ[»µÕ½Ð\x0014\x0011J" \x0008\x0000¥Ji*	Ø{$blD\x0012@0´¤öÞ\x0012\x0008ª¶zÖÞ[f$\x0010Ð\x0016Ì¶ÚJBB\x0000­$\x0000Z¨¨\x0002\x0000Új+¡¥­$&\x000c­}n\x0006Ø{k\x000bÒj\x0001\x0006-eï­-\x0019IlD[m\x0011D2f
fÆõzõ|>í½u\x0010\x0011§óyÚçF´PDfY\x0013Çûwï|þøÙÛù\x0010$´ \x0001;\x0015¥´\x0016´E\x0000\x0001É\x0004\x0000$ ¶ ¶ 	¶\x0000ÚJ¢­¶@K\x0008\x0012Ø\x001b\x0006´\x0014mµ\x0005@¬Ä1ã8Æí\x001a×Ëx}¹úò\x000fÞ¿»y÷zõáÝÕû×ÛÅå\x0018Çb
ke\x0019H*-{Ó-Ðj7ª\x001b­´ìýI2äfgLjæ0ëâz\x001cËÅ¬É \x0012\x0014ªØP\x0000
F'vcfXeÌ\x001aåúru{}oYËÌXkÌºHLDì}r¾aìÔÌ2³\x001e@5\x0002\x0019Ç\x0010X´U´ÕV[{Új*ª\x0018\x0019ÐÖÞ[[D¤$´"f
 "*Ø»¨di¶$¶Ú²K	\x0000H\x0002\x0006ª-¥Ê&h$Ú*\x0004\x0000\x0000h«\x0005Újkf¬5ö¹µ[O¶öÞ Ý\x0008(\x0004%h\x000b`ï
\x0004$`\x00121a&`ïíñx½·Ï>I"¶ÎsÛ» ­\x0002ZÎsëæøòý\x0007\x001føÉãñ´[-\x0019ª¦"\x0004Ð\x0019\x001bm\x0001PÔ\x000cRUJ[I´P\x0005@UBD[Ð\x0016PT\x0002D@K;Î½íÍÞ%¥ÅFMj\x001dãë/?¸^}>¼{¹zÿîÅ\x0017\x001f^¼½y¹-ï^®n·Ûey¹^\x001ckY«&¤±Ë¶¥OÓ-Ý"iÙ[²µ[Ê½7}ÚÝÚÄ\x0008©\x001al//W{®¶!ËZ\x0017Çåp\\x000e\x0019\x001aÝUT5
B"\x0013I\x0004+1\x0019É0Ã1k,3c\x001dËårXÇ¡D TlÌ.ØNÎ'HH"YfÌa­e­eÖ5ËÌHBH\x0002Z\x0014­¶½«­©ã8$Ñ\x0016u§}V\x001b°wQPlÓ\x0010¦ËdPÉHAQ\x0016´@\x0010\x0000mµ\x0005I@[{o[EPI$\x0001\x0000DP\x0005Ð\x0016´D[
Uçi­eïm[[\x0000m%\x0004\x0008
V\x0012\x0000MD@B2\x0008AH8Ï\x0013ìV
UÑV[Z\x0004LJ\x0000*ãÃ\x000f>|øÑ§·7oow\x0002Ñ \x0005nÉ\x0002QTV\x000b´hLF\x0002$\x0001RZ\x0000
\x0000\x0001VRM«ÝtKX\x0013kÆëíðõ\x00177ï_oÞÝ®ÖDzZ+®×Ã¯~ñ3¯·Å~x½]Ý®7cÄS{J±\x0012±V$%£óy×çÃRÇZÒØ*NÝ§­vNJÏÊYí¦[DÖuH¬ãõõúë;§ûc;Ö²nYdÌ:¬Y\x0008	\x0019I0$\x000c\x0012D\x0002\x0011#32ÄÌYÖZÖ\x00113K:ªÚjkïMkr\x0002Ðn0sJÆ§=Ëó\x0018YcfLÆÌH\x00183ÄÌHHH"	âX\x0001°V¬cY\x0013B[{o-\x001amû´÷¦µ[mQÊÞÛV0SI$\x0011\x0010h«EK
\x0002\x0001¶`ï
D2ª"$\x0004h\x000b\x0000\x0014\x0000h«­¶@«¥jï­­\x0011mµ\x0005k-3£­d$ÀVmµ%\x0000$\x0011\x0001\x00121 -¢Ò8\x0015'hK¶Ú\x0002´¨ Ý&#3××W\x001f>|á\x001fr¿?ìVZ@¤A4±[E0Ý\x0002 @H\x0008&\x0011¶Ú­9\x0005
h(;UU\x0015$1\x0013c\x001cÇárëe¹½\x001cÞ¿^}xÿêÃ»«/_/Þ¿¾øðáÕËípqÌ`«JÔÉ25µl22ËÌµ\åz\¬5[{ª²¹zz{ÔÞO+![Z»EÀî(d¸åX\x0017s\¬ÛÍõå½ËíÅq{q¹½Z«¹¼ËÍý¾}z{³Kf$#\x0019³¡\x0014It\x0017@\x0011\x0010Df$1Ycfµ!\x0015A\x0000@[mí½µ[\x000b´µw´µ÷Fµ5­ì0Lb\x0012efÄ0#\x0019I$äÿ_\x0010\x001c.K\x001dÜYÌg¿U§{fôa\x0002\x001cø\x000fApÿgdiÔ}j/2sssTêØæ\x0003î>W\x001eãóJÁÌì¾Ü;ÝÙæÞëÞk{gm¶\x0001¨T¶9ç\x00186¶\x000b*\x0015\x0000Ø\x0006*À`Y1m\x0000`mÀæn\x0000l\x000cïïoG\x0014°Ùfm¶s\x000eøÜëóý\x0001\x0001H\x00016*s¢rNrlSa&0@e8e\x001b\x0005¶ÑÌÜûñúúzûÇ_øëÏþõïùõû\x001b\x0000±(Ê°
8³±ff²±Íºn×õ1Ùf®9*5\x0007çÉs×ëñãýx=~~½üõç?ÿøá\x001fþá¯?ß~þxûãÇ?~üðóÇ÷ëñ|lWØ.ãÁs8å<Çç\x001cãåx\x000e§ã\x0000rióñ-û\ö±Í.\x0019'÷>>{t^<zy^_s|ó|y½ß÷[_o¯÷çëËóþò¼8ï\x001f:Ç)\x0007äõþò×ýýË?ÿù¿üç?¿}F¦{5*§#G''ê¨d*\x0015¥8ç¨TÎ9*pÎ\x0001\x0004*ÛT*Âf\x001eÆ6pïuï\x0005°Á0ÁuG»v:¶ãJåCÇîqï£¨£ò¹Iïo*ssNÎIqÎñ<\x000fëcØgî{¯Ïçc\x001bCl³ÍÆö\x0001\x0000°M\x0005*\x0000\x0015Á!Ñ¸\x0019\x0000Øí\x001a\x0000\x000cf\x0008Q¡
À÷÷·
À9Gå^î\x001d`\x0000 3uAp?Àé8ç8¥\x0002\x001c3\x0010îfml¶Q*P©×9ùãÏ?ü×ýÃ?ÿùOßo3	¬\x0010ÉTî\x000e-!£G}9Þ^g¾¾ÞNó¼\x001f¯Ç\x001f?øùóËÏ_þúãËüð?úë/?¾Þ~¼\x001f__¯×ñ~cÃæ Mc.Ñ9æéåUNy§\x0008.¦2lØ]vÝûqw}o~{ì¼ì<vâ¼t\x001eûùÓóó\x001f^÷\x001f×\x001f÷Ûóþò¼ßz^ÎóÖóÒyt\x000eE)VNRÂkû¨ë¿þñ÷ëñÿýóùõë·äC©ãô8çQ)Îy\x0014\x0003cÀ9©T\x0000*\x0000P
@!Ü{UÎ9 \x0002\x0000P8cGèätT:9ef}Àö±%Çd\x0011\x0014£RlT*çyT*ç¡\x0002B0\x0000°Í6m6 ²
Tî½ \x0002P©Ì$
\x0018\x0000bm`wl@±Am m\x0006\x0000Ø\x0006àóùF8Í\x000603À\x0000\Tmî\x0006QNQ^Ïùõë·{¯»Ù`B¥\x0002¯âý~ùÇ?þò×_ø×þí÷÷ÇE;p¢\x0001[æý\x001c§<çå9WÿÍûüßÎÉÿþßþòõâëëøùþòÇ×O__/ï÷ãýä9Ó9\x0012(ÎæÄS\x000e¶ë ¦}Ã1/s:<=ê0Ük÷}¸cË6w\x001f\x0017\x0013¾ôz¹¯/çýçÇ\x000fçýåýõÃóþÉssç­çz$\x001e\x0016[V&\x0017\x0007Ç\x001c(ç<r$û|t¿þüòãëñïÿíóh\x0007I\x0003rÀm6\x0018l\x000cQ©T¶
\x0000ÃØ(À\x0001\x0015 Lå£²
9\x000fç\x0004 °£BL¦AÄöÁl\x000c6¤"\x000c\x000eï\x0002Ns#ÝÙ®{gÆ\x0018\x001a°\x0001ÛT¶©T¶©\x0000T
cÌ\TqÎ1lsï\x0005
\x0000\x001b\x0000(l\x0000`\x001b\x0000\x0000\x0000ØÆk.¥bÃ\x000c\x001b \x000c.0\x0014ç¤\x000eÈXfmÄ9ù|¦k»\x0000¶m¶Ùæ<ÏñÇø¯ÿí¿üÏþÓ÷÷ßsòt<'ï×ËsRó:Çs8\x000fÏÃûõøz¿ýùÇ\x001f~þøòÿüíï_ÿÝyî7¾mIàà\x001cNÉõÌsòz\mN1\x0013ã^lfÉe!ùÜmìbè±\x001bKOÎëåy}yýüËëë/¯x~üð¼:Ïç¨c]Ö\x0000Mf¨\x0000\x001c\x0014¤¢R\x00079FÔ1ÊîåÉ¯üôë×·+\x001c\x0001,ëÐ1.3ÌÆ6 Ù\x0006Î9*ÛT*\x0000PÌ\x0008RÉ\x0018:êÚ8\x001dç0ç\x001cÅ\x000c\x0014
1`\x001b0\x0006ØE\x0003¬$Æ|0¤\x0000¢\x0007) ¦\x000e¸\x00010Àd\x001bc\x001bØ¦R\x0001aJbhÁ(`3lSqÇF\x000c$@ P\x0000T`\x0000\x0000m\x0000\x0000l\x000e{\x0019\x0015\x0006\x0008\x0007\x0000\x0000Ø\x000c\x000cÌÜ;w×5°
a
´\x0019`\x001bxm\x001f»×ëä¿þúËÿøïÿ§ÿûoï÷Û×/ïçñõ~ûz\x001eóíóùÅýØý¦9å9y¿ßþüë/ï×Ûÿê:÷ÛýþæóÛ1÷^EñÄë\x001cÏÉ)GÎÂÔÇñqG#Çvõ\x0001\x001e¬c\x0011s¹s1±£X\x000fÏKÏÛyÿðõþ©×\x000fï?¼þáüøé|ýÔóå·
{¯Åp
\x0011¤¡Ô@¥\x00029êèLT\x000cqÊ
3ÜÑç:=^¯{ùý=:j\x0002\x000cL \x0003\x0019
`¶©\x0000T¶©l\x0003\x0015Ø0
X\x0017\x0001J¥ÂtrN0 X`\x0006`Ê6Ì6\x001bÉÄí*1\x0010c\x0003 é`W\x001d\x001b0©kXT(ÀÅ\x0008\x0002\x0016FÃ±Í½#*Ie£Éî\x0005+u\x0004a¡\x0018\x0000P1\x0000\x0000\x0004\x00183a\x0010Ã6\x0000Ø\x000cG:I¶¹\x0006ÁØf\x0010G\x0018¨lÃ\x0004BÊ66P,v/\x0000xíûo÷û·ûýÛýñøoþ\x000fÏ9¾~¼½¿Þ¶¸×ý|ûõëßþþ_ÿËç{8*E÷úþû?Ö/ûý\x001foßÖo=W\x001b]áÄ)O\x001f\x0006³RÃÇý@xÙ>¶ÏØFó .=Ñ×Ñyëõå<ÇëëËóõ×Þ_z~üÔûí¼^êqË;îf÷Úf\x001bØ¦ I\x0005\x0008\x0008 E'Ò\x001e\x0001\x0006\x0004\x0011\x0019 pï|>\x001fç<:Ù®Ï÷·NÎØuFç \x0002r
\x0001\x0003\x0008³
@\x0005àÞ1mtUÂF\x0001\x0015fCÌ\x0005ÊÆví¢±\x0011Û\x0001\x0003\x0000\x001a\x0000Øf
c!03ÓH¶\x0000)`1)¶@a\x0019*5 ànì²ÌX`Æ¨l@\x0018<\x000fÉ\x001dÛ
0À\x0010\x0000*`Ì\x0010Ø`dÆd\x001b
$a\x0000`,Û@÷Zs#Ê6@*s{?È5rÎqïµÍ6¯³_4;ó~\x001d_ï/¯çñ<Ï÷·ûýíóýÛï_ÿqÿÖ®WÓã]>\x001f÷û_4g¿½î7÷}t§\x0010I\x0005à\x000eÈÌì^\x0006Ñ¥c½óÒyô¼×ó¼ô\x001cÏûíy9¯/çýÃóõÃy½×Ëóz9Ï[çQ[îæÛ¸ãa0ÛÜ;Ì6°QlT\x0000*°Må\x0000\x0010
3cT\x0018\x001eÆFQ!d»¾¿?Î\x0019Ýë÷ïß:Î9N!Ïó8'ÎQIê\x0000è\x0004²
pl³Í6ÛÜ{UÀf(\x0014Û\x000c>Sl||$\x00026
\x0006\x0004cpT Sæ\x0001m ²`T\x0018Ð\x0010Æ \x0003q\x0007
Ø\x0000ERa\x0014\x0000Ma00±\x0001\x0018\x0000àó¹*\x0000ÆvÙ(C\x0008\x0017"ì\x000e	`@\x000146ÛÀÆõÑfp\x000ehÓ
Í!Î9*Û@Qpm³±]÷Î@l\x0000`×ýþË~üç÷¿ý=Gú|´ëîcß¿ì÷ogÓÈ·]Ïáà~®Ïýh\x001fîl	9 i\x0011\x0013\x001dG²8OÎëå¼Þ<oÏûí¼¿<¯\x001f^_?çíy}9¯=Çy½çE\x0013=N\x0007ls7°;ÛµÁl\x0013l¶aî®
\x0006H\x0005
Ê6P
a6\x0018HÎ9*Ì\x0006\x0000bQ¶¹<Ïñ¼\x001e¿~ýöù|\x0013ç\x001cÇñÇyó<:GlSNkm`Ý¹÷{¯Ê6Û\x0014\x0000\x0001¸w pJaÃ±
T é\x001c
@¥ Ì6\x0004\x0000¶\x0001\x0003 `\x0000¶a\x0008pY\x0000¶1Ä \x000c³¥ \x0008RÀ6!C\x0008bÃl0\x0004\x0012¦\x0002\x0019\x0006c\x0000Hl\x0002J\x0000ClCÊ\x0000Æ5\x001bçRTÎóØØ¨)à£R9ç\x0000(66`c\x001bÂl\x0003\x0000×ßÿßÿt¤qÏÁq\x000eÏË3»kÙ'vPÎëèÄØ¹ÚK8\x001d@çõÒ9Äy\x001eç<ÎórÎËy^Îëíy½÷[¯Çy\x001eçyq\x001e:,N`\x0000àÚg>>}®m@1ldfØfm\x0000 \x0000\x0000Ø\x0006\x0000 B£`\x0000*m2
Ø\x000c\!`çäÏ\x001f_^ÏË?ÿõ/ÿùÏ/Å9SórÇó<Îy.ãÄîÀ6Ã66[`\x001b\x0000m6ÎÉ6\x0015Ø\x0010`\x000cl£Rá¨©TÎ	\x0001BäØrï0PÙ\x0006\x0000À°À\x000c\x0000Ã\x0010\x001b\x00103-C\x0006t\x0000\x0000³]Â\x0012`Kl¨Ø(PÇÌ\x0000Å\x0006S#\x00002$`Ã\x000c6d°\x0001\x0000\x0000\x0000¨0¹¦´yãëëíãÞÙ¨Ù\x0006`\x001b¨\x0000lCó8ç±Mem¶¹÷R^ýÍÉpÎ£çm\x000e{fÏc=×ëå9Çëýö¼ÞÎs'
ÎQyó<óx^oÎ¡9ç8\x001d:ê¨t\x001e+\x0003I«Ë`l©\x000c6×T66l\x0002\x000c\x0004f¶1f\x0000\x0000\x0000\x0000¶©@\x0005\x0000`#C\x0004T`»@\x0004 ÀÌ@ \x000cSÇ\x001f/óÓ½ß~ÿþ¸÷ºïÏ·ç3ç\Ïs½_çõÒrÍÝ0\x001bÛ\x0000\x0003@\x0001{¯J\x0001\x0005Ô\x0001À,ÖQ\x0013s: è\x000c	\x00044\x0015²asù\x0000(lC\x0008a\x000c]`\x0001"\x0000qH\x001c0C`!ÌF\x0019\x0000ì²\x000c-0#À\x0004t@8X(\x0000ç\x001c¥\x0000°À6°
l\x0003\x000em\x001a\x0006\x0001QÇ9a¶«Jem*Ûl\x0003°Í6\x0015ts¨À6{éØ®×¯_\x001f¯¯/½\x001e^o_?þp^oÏëñúñÃûývÎ£\x001b'^ÏËóz;¯\x0017\x0005®Óq\x001a%Y©c\x001d\x0000\x0006È0\x0003C\x0001Ø\x000cc×\x0000\x0006¹\x000bl\x00196`P6\x0018PÜÙÆ©\x0000À60\x0000¬Ø@\x0005¶	\x0000\x0015Øb\x0000\x0003
-°Ù½üñóKþá_ÿþÏ\x001d2É\x0011:Ê\x0006³Í6Ì6¥B6
\x0003Pa*£\x0000\x0002\F¢"©s0\x0000\x0000°\x000cÀ\x0014@6
@eC0 ò\x0008\x000e61\x0014\x0019\x0000 0\x0018w\x0014$(\x0000Àl0a&@`\x0017RÙÈp\x0008('8Ä9\x0007T`0lmm¶Ù¦¢À6»×Á\x0000Æ½\x001fÿý±Í\x0006\x0014\x0000PÙfm¶±±(äsÔQÀ6Lxýøßþ\x000f_þáýã§?ÿðõã§ó~y½\x001fÏë¥óÂ\x000c+á\x0014Ø ×\x001caMa\x0018\x0017.ÂFl\x0017Ø\x0001\x001a\x0001\x001b\x0010f ¶\x0001\x0003í\x0002£¹®°
\x0003\x0013÷b6`\x0006\x0000*ÛÀ6\x0000bcJ¥\x0002J¨!\x0000\x0000Å\x0006\x0003\x0015Øb\x001b\x000c-÷^¯?~þ4ùÏ~\x001b6,çðz?çÙ\x0000R×P´t\x000e¨\x0000)\x0008©0\x001aTê(¶¹÷¢Â\x0004\x0000Ø\x0006\x0018cÊvA\x0005
\x0006æ
\x00036\x0018
\x0000\x0004LE\x00082\x0004`\x0000ÀPÂ6\x0000\x0003\x0000Ôlh\x0006c\x0006\x0018\x0004r`Ô\x0005wÉaHvzTB%©\x0008Øæn&ÛlÜÑ\x0002L¥²ñ\x0019\x001ba\x001bØ¸w`\x0019\x001bfs
lsïµÏes7!ÔqNÎ9Ê9!¯ÿþÿü¿Þ_o¯×Ûëýö¼Þ:9çíº÷\x001a20ì²
£\x0003`\x0001±1±\x0001\x0001\x0010\x0006³\x0001\x0000\x0000ÌÐ\x00002Ãl\x0000ØØ\x00053m\x0018m

\x0000\x0000\x0004\x001bç\x0000\x0008`£@¥\x0002PÙ\x0006@±\x0001Û\x0000T66l\x0000î.Ë÷÷uÎñ>/ßçãûó±Íç¼<\x001dG  \x000b\x001d\x0000\x001c.bB´\x0010A\x0000P\x0002
È\x00016Ê\x0006C¹÷\x0002\x000e¨a*\x00000cÙf\x0003\x0018\x0006\x0012¢\x0010`4\x0004m\x0012\x0000\x0000\x00002\x0000À\x0010\x0000ÌFA\x0000\x0018\x0000\x0008\x0015¨\x0000
\x0003\x001bÛp\x0015{/¨sT\x0001\x0000HffCd*ð<Ç9\x0003÷²ÍÝØµQyJ'çT\x0000àÞëóýqïÇç^°Í6Iâ²a8ä\x0010¯¯¿þáyçyçåG'°ûqïu7\x0003l\x0003	\x0001\x0000\x0003\x0001\x000cØF×î@\x0001a£\x0000\x0000Ø\x0006`\x0000Øf\x001b¨l\x0003Ì\x0006À6Û\x00000Û\x0000@\x0005\x0000¶!\x0005(\x0000\x0010\x0018²M¥\x0002P\x0001¨lSm\x0000\x0000
±ÌØ\x0000lsïlß¶y½Ò9Èë¼<ÏKEl\x0000À\x0004\x0008\x0001\x001d\x00001`N 0Û@\x0005\x0000 B*	\x0000@\x0005\x0008@\x001d\x000c\x0000$lÃ\x0010(`\x0008k£8²\x0001\x000c\x0000\x0001\x0014\x0000\x00006\x0003\x0000\x0000´YI`£ P
\x0000\x0000\x0000\x0014ÙÆÆ
\x0000£ä\x0000h³Í ,\x0016Ês:`{ù|>îe\x001bqÎqÊó<^¯Ê÷÷·{¯Êó<Îy|>×¹\x0017×½×6°
¸,4·+y=Ïñ<×óx£Ø®{¯{¯»aÈÌ½#\x0010`\x0012
Cca\x0004\x0013`\x001bÂ¥À\x0006a\x0000`\x001bØ0\x0015m`\x001bØ\x0006àÞ\x000b0ÛT\x0000,\x001a\x0000(\x00080\x0000\x0000\x0000\x0000\x0000\x0000\x0000P\x0001¨À6\x0000ÆÄ\x0002\x0006\x0000Ôð±\x0001ïWÞ½uãc\x001b1À\x0016Ø. °a\x0011\x0010T£Á%\x0018b£\x0000\x0000\x0002£ \x000c![
Ù\x0006*÷\x000elÃl\x0003PÙfd\x0006È5\x0001\x0008\x0014P!la*6
m*\x00006Í@\x0008\x0003\x0000\x0015\x0000Ø\x0006 \x0002w£Ëíªä°\x0019¸M`
;nSz\x001e'ê {æõ\x001có\x0012Äçs}>ß¾?ßî½*ÏÇ½W¥rïl³]Ì°M\x0001×h`øÜ«òz=×9Î	sïõù|Ü;\x001bC¨¹w\x0013\x0000ÛT`\x0008\x000cC¶\x0008\x001b\x0000\x0000f\x0003
Ø\x0006`\x001bm\x0018m\x0000¶m`m ÇPS@a!A±%\x0019jÀ\x0010Û\x0014\x0000°M¥RÙ¦\x0002@Hff \x0003,\x0000\x0015Ø&\x0001\x0010M±\x000b¶Cãp\x0000\x001cÆ\x0006Ù\x0006HH\x0010à\x0001`\x0008\x00005¤\x0000\x0010'\x0008\x0010 \x0005a Ø8'\x0004Î	Ù®í\x0002\x0000¨0Û\x00001&3\x0019(\x0008\x0000\x0000a ,\x0019K\x0005¶\x0001\x00080\x0010\x0002\x001b5\x0004\x0000\x0000\x0000`\x001b\x0000\x0001±\x0019a¶	\x0003³Mas÷±Ýyãõz9ç¨ô\x001cÊó\x001cã~®ïïoßßß¾?×½×½×6÷^÷^Û|>×½\x001fa\x001bÆ\x000cE2sïÀëy\x001euÏ½>»ÙØm\x0000\x0000\x0016C0Ö\x0018:\x0006\x0008Âf°)\x0018Ø¦²a3\x0000l\x0003\x000c\x0001`¶Ù\x0006\x0000¶1\x0006£\x0000@\x0018¤"\x0018à\x0008\x0010\x0014 6@\x0005\x0000\x0000*ÆEI`»¶\x0019\x000e\x0012e\x0001 Â
\x000c\x001bvTp±°aJ\x0005\x0012\x000b\x0018ÊH
(\x0013ÉÍ6\À\x0002m*\x0000À\x0010\x001aB6\x0018 P!°
l\x0003BE
0\x00000±\x0000aÆm\x00006\x0000`Ala\x0000¶\x0001¨À6
\x0000\x0006\x0000\x0006»»\x0001.2\x0001\x0018°ÌµÍvl×9Çó<Î9Î9Â\x0019çäùzûñ~ù¾sï|îÇçs}¾¿ýþþöùþö}?î÷·Ïçc÷c»6¶q)à~®Ïý¶ñª\x0014]ÏÇ½×Æ0´!\x0000\x0019L6 \x0008®\x0000\x001b\x0000\x0019²
0°\x001d`#v\x0019`\x0018\x0002\x001bÛ
\x0000\x000c\x0006%\x0010\x0000"\x0018\x0006!0´C#\x0000J\x0008
X\x0000,Â©ÏçÃ^£b\x0003@A\x0000BÌNÎ¡s\x0004²Íp\x0000J°\x0019H\x0008`áP\x0001\x0002'<\x000c\x0016rwíf£FS\x0001Ø¦\x0002\x000036Å\x0016Ø\x0000`
fm\x0000¶Ù\x0006à\x000cÌe\x0007(`×\x001d¤\x0000Ta\x001a0
\x00012\x0013,
!\x0000\x0015Ø\x0006 \x0002\x0005\x0001\x0000Ø\x0006°£Áa`£2\x00036÷ÎöQùþ¦çy|?sÒÉSóð<½Ïsòë~Üæs?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=I\x001b\x001cOåþîÑv·õ7ó{øÃï­\x0016K÷O[ß~ûë+www>¼û`JÁO?¿µ?MÎÏÏÜÞ^yzz´ZyñâÆb>·y~ö¯ÿöGBkÍwßýÆëkw÷÷z\x00177/Ã`8Xk\x001f?~´?ì}ÿýwnooí÷{ÍÆétTUJQ¥ª« \x0000Uzïè Ð{W\x0008\x0014U]éR¥úR)UT/D\x0012i¥%ªJõNTNJÚ \x0010H\x0008¥@Kè¦µH($4\x0014½Pz÷¦ª«c3\x001bºa\x001cd\-ÖùJ\x001bæd \x0011PJ$\x0012R\x0005R½PH\x0002Z"</p><p>*tZkfã( @</p><p>DU¡Tu½w\x0014¢</p><p>Hª®tNÇ\x0003Êi,æ+Ã0z7M©ÞËlvR\x0015ÏÏ6ý`hÑ\x001a	\x0005 \x0000\x0000\x0015Qè\x0012U@AR\x0012\x0005 P( \x0004\x0001(ªPeüéw.ÏÏ­×k½ÞËv³5õI\x0012CkÖëÙlFq6ê5Ùí÷zùba¿ßÙî¶ÖëÅre¿ß\x001bÂñxt<uãÉáX§'\x0017\x0017Z\x001b<<>Hb\x0018\x0006««ÁõÕ¥Ýv´ÙPUN§W¯n<Ü?ùù§]_ûáwß¦÷ï?yx|ò×ÿòWíÎt*½7_¾<êýh½Z:??\x0016}:\x001a2¶p~yn6y~Úè½ùøé³õêàß}¯ãa¯N'Ç©»¼º2\x001b\x0006üó<>nÌç£åúÚétpwç°ZûõÝ\x0007ÏÏ[»ÝÎÇ\x000fôâööÖn·õððÅb6sy¾¶\Î,Wk÷wOapv¾6ÎF\x000fOÇëKçgg®®®<o÷>ß=¦ÉÙÙKÅ|n>yzzt÷ÅõÍ\x000b_½~ãýû·Þ½ÿÕ4\x001dµ\x0016U\x0011¥WGD\x0004B&) ªTu¨\x000c\x001aJ©*\x0014ER\x0014UEAIPHIÈÐ¨ h4$Z\x0002(´*IHÐUÑZ\x0006\x0014Ò\x0014Õ</p><p>\x001dê2ÆùVf#ÃØÔ0×f3Ã8J\x000bJK¤EU§&­
!R\x0005\x0012¦ª\x0012D\x001b"¢µAÒTÑª*¡Ïç &	HQ\x0001(U\x001d¥*(U\x0005\x0012 *R\x001c\x000fÓtp8,\x0016sã08õÉi\x001aLS7Mf¾ÍF³qfhM\x0002]é(Ñ\x0014\x0014\x0000 (\x0002(\x0000$¥\x0004º¤T¢+\x0005J\x0002\x0014T\x0001¡@©tckí~g¹[Ì\x00176Ú\x001fvªOæ³Ñííal\x000eYkÍöÙf»7£a\x001c³Ñ|>ªâÅÍµççgËåÂv»sw÷ mÐÁnwp:~QÍvg&ËåR)ñÙz9×ZÌç\x000bëõÊóóùÜßÿýß¹ûòÙn·µÛî¬W+OO\x000f~yûÞáxòÍ7ß\x0018ÇÑáp°ÙlMûrv~®÷n¿ßûüøàâbíööÖãóÖ_ÿú³³õi¨r}uåo¾òòöÒiÜ}9ÒËf³5\x000eÍùå¥/_:\x001dßÚîvóÓqï¯ýIUwxxx\x0012TñÍ·ßùÃ\x001fþÆÏ?ÿdµZÚíöZÙ|a½:wØ÷ïßyùòÖ|±°ÿøÙé4Y,\x0016æ³ýþ µ¦µøóÿl66\x0017gkÇÃÎ84Oû\x001füIUóæÍ×NÇwï~v:\x001e\x000cã zIQU$Ò$TR\x0002JT\x001a$\x0012\x0014\x0014\x0015i´\x000c"º*R\x0000hÒ\x000b"Bu$@$H"´¨*i\x000c­ªÒZ´DUQT*=e\x0018¢Íg2vc+\x0019\x0006]Ó\x001aãÐ´Ö´0´ÖL½¨2\x000eÍ0\x000cR¨D\x0012PUJi-Z$a&¢÷\x0012]tÃ0
Ö\x001a\x001a"\x0001zQJ\x0012\x0014\x0015U]\x0012Õ'\x0000t\x0011©¨Î)
¥÷	¥¦4TkªºÖh-Ö\x000c­I\x0008ª:é\x0004EUI</p><p>\x0000\x0000\x0000@\x0012	\x0004¥ªB©*	B¢\x0010\x0000)\x0014\x0018¯¯Î©ÒZs:\x001dD\x0019f±ZX,Ö«¥ÞËép´ïÍfc¿ßKkÆÙÜóóÆÙÙÚÍ\x0017¶ãñèìlíl½rv¶6´Áþp²ßï¬×+ýNõîüüÌlY-¶»>\x001dm6Of³ÓéäphzÜßÝ{yûÂo~óûû\x0007?ÝB9\x001eO./®ÜÞÜZ,\x0007ªûðñÙxëþáÁÇÌÇªîêêÚb¹öå~k¿l?:??3\x000cÍ0ãì|áxÚûøñ£d°^­]\^x~~öñógçççÞ|ó/_¾¦qlf³¹\x001fÿúq¾tssíêúÒiê\x000eû=u2_4Ã6f¿?xùò¥Ãng¹[­V6ë\x0017þú×\x001f]]^yýò¥ÕzåþáÞóóÆÐ\x0006OÏO½¸ºôøø(­¦ÉápòåîÞj}f±Xzýú\x001fßëý¤·¢\x0017EÖ\x0006	U%E¡ P\x0005\x0008¨*II\x0004è\x0005¥Ð\x0012\x0011ªèzÐ§If£a\x0018\x0011­Ek\x0011MÐCU0(t­EKSU\x0014U]ï\x001d\x000ci2kÕD)ÑÖ\x0006±\x0019Ú \x0018AÁqª2\x001bFÃÐDT$ ªº2I"¡µfhM4t­Ç¤$]B\x0012\x0010\x0008UD@I\x0000\x0005P$\x0014R\x0018DIQ)IW}Ò§£2\x0001EB/0$¡I#(\x0004\x0001t@\x0002\x0000T\x0001U\x0005\x0000@ \x0014%hD\x0015\x0014B"U JUQeüúÍKÏO\x001bíÞ4Mfã`¹;??·^/ív;OfR6½ÓédhN§½Ífc½\Z.æóË«3}:Iâõë[\x000cîï¾/ç¦é\x001c13WW×Zøôù^Ýáp0õù|¦÷ÉÙÙívç_þõn®¯\\\Øïï$\]]y}8y~Üúôþ½ß|÷µ§GÛç­iQ>|øèññÙb±ðúõ+5ÌüË¿þó+ÿÍ?ü_~þÙýý\x0017óóµ*~ýõÊ_~ü«ËËKÃ08\x001eöZX¬V\x001e\x001e|úôÙjµ¶^-MÓÑ0\x000eÖçg6­Þ»Ývçñyãó/®¯.\]_z÷îÃáàp8ÏfÎ®/Ìçs/o_øå×wÒFgçg~÷ûßúþï\^N'O³sßþæ;ÇÃÑ89¦iÒ{y|z¶ÛÿèþîÎüÿè÷¿ÿõúÌÛ·?Ûl6(\x0015 ª«bê*ã\x0010Mô"\x0000U"Ji¢:¦Tº(\x0015Z¢µ\x0008TÐU:J\x0015ÕªºÍlÖÖÖ@ª\x0006`\x001c\x001a	&I3´\x0001QUªJÕÉXÑ+\x0006¤:¦rf6ÎÃ\x000c\x000cã ibR\x0018Ak
T\x0004¨¦4¥TºÖ¢µ¦¡µ¦ª®e¤\x0010(BtU$\x0011¨\x0002Q</p><p>P\x0004H	 ÷®×¤L¤£T\x0015\x0012´Fk@¨ )\x0014\x0000ª\x0000\x0005¤Ñ{\x0001¨* B\x000f)\x0000z¨¤©@!A\x0015A*(q6»}¹æÓ'­5çgg.¯.¬VKÇÓÁf;yzzT\x0015ÕJkq8\x001c\x001dN'­
ZcN6­Å|épØÙnât:9ì\x000ffãÌz½v}s©µæ4uU%ÖÊ8\x000cªºý~çx<Úï\x000fÎÖç¾ùú\x001båÜÔ»÷ï>ùù§wn^l
#z¼yóµ³µÇ»\x0007\x000fO>~ZØl6îpÜ¦I\x0012Ã8\x001ags\x001fÞr8NVË¹««\x000b«ÕïýOÿßÿç§¯^Y-Zõjíý\x000ff³ÝvëúêÊêìÂv·óøøøÍw¿ñéã{³ùÜ÷?|ç_ÿåa´^Y«©¼{ûÁÙúÌ«/=?o<>>ùõ×¼zýÒl¹ººõ»\x001f~çÿõÿþÿ8îfÃÌ8\x000cÞøàÛo¾ñÛß~çÓ\x0007_¿yãþógoß½÷ío¾±Z­­Ïí\x000f'··/Pöû½Û·¾\x001d\x0006ÏOTMJ\x0001Påt::\x001e\x000e\x0016åba6\x000cT©*	  -TQ´\x0016Ð'zH¢µ¦%JTAÐô*Õ» &fc³aÐÒ\x0010\x0011Ò©"´6H\x00062h´F\x0005\x0004e4VWHHêq:N*Ñ\x0012ã87\x000esB&Ö\x001ah-&\x0002D\x0015A)QZH\x001bÐ´Dë\x0003¢ª¨RÕÑ$A¡¨\x0004\x0010iMõN\x0011\x0008U$P@\x0000JUW½HB \x0010D\x0002Ñ«Ò@\x0010B\x0004ô^ÚP $ª</p><p>\x0004@ÒTu\x0011\x0004B\x0000\x0001I£:\x0000@(Æ\x001füÙÍÍ\x000bã8×{·Ï\ëºÝþ¤ª8õ2öÉ|>3Í\x001cOGçgóÅÜ0Äæyk6Î\x001cÝçÏ{U\x001cöG³ÙàáñÞÍkgë3ûÝF2¦Éétr:<=ml\x000f{ËùÜÙúÌ~·óùó'¯^ÝZ.nooüòË¯ýýßÿ­Å|îxìfÃÜÙÙÚÔ'»ýÁáxRÕíö\x0007óùÜoó\x001bÂÐb}óÊúìwîï¿øù¯V«®Ï\x0017¦ir§÷òõ×_¹¸<sÿ`êåpê(¿ûá{C\x001b¼{ûÞýÃÃiòpÿèÍ×öû£Ï\x001e\]]º½¹T§ãéäã§zô^¾ýök?ýø£þçõõ×ßøñÇ½þê\x001bÏgóÙ\K¼ÿÞé´·ÛnÝÜÜØï>¼}ïüüÂãó·oq}qíêâÒi:Y.FççNûçG\x001aóùÜr9sØMª\x0002U~ÜØo\x000c¹0®\x0016Æ1ªJïEHJkÑZ\x0013(ôHk"ú\x0010U%)I4¥¨`ªÉÔ»!ÚÉ8\x001fÍ\x0016\x000b-D4#®tQÀ0JT4Ö$\x0011!TuCu-EJJULÊD¢µA\x001b"iZJTJKD´\x0004\x0010\x0000=4è¢HCHhM2¨êzïIB\x0013Õ\x0006Õ	4A	C^T©ê\x0002\x0000UA\x0010ÐHê !\x0004®TuIRJD¡ª$\x0000UÐ@U\x0004)J\x0011 $(¥\x0012ª@G*Q`øÝ÷ßýcÂl6zzz²Ým
C\x001c\x000e{ÏgÇÃIõRHb¹\sU¥ª´\x0016óÙL¯n·Ý\x0019ÇÙlÔZåj¡÷îp<Jb»ÝÍf\x000eÃñHÝþ`<©*³q´Z¯N'ç­ÓÔõ^\x000e4VË¥««+ÃÉîpÔ§õzi>\x001bm7[ç\x0017\x0017NÓÉwß}ãï¿³Ûm¼xqãòòÒÝÝ½·¿¾óðpòü¼ñ¼ÙØï\x000f¶ÛÝ~ïÅ\x001b¿ÿß9\x0014ÃÐìv[ëÕÚ|¾0õë«+\x0017çç6g§SÍæÇ/_>yýêµÓéh{Øûñ§}úøÙj½6õîÔÙn\x000e¦©<>>û/ÿüO6Ûg¿ûýoýíßþÎÇ\x001fÜÝß{÷îívoµ^)Ýáx²ÛíQÖgg§É\x000f\x001fìv[Óéd±\:M'ÇÃÁáx0\x000cD7\x001bc\x00188\x001d\x000fv»Ùlpqqf6i-Æqlfã`\x001c\x0006³q4´AkÍ04ã0\x001aÇf\x0018b\x0018b5ã8\x0018f\x00186Ä8\x000cÖd¡5Äl¾²Z®\x000cC3´fhÖ\x0006­5CkZkZ\x001b
Ã 
Ö\x0006­
qÐA&­ÑÖahZÖÖ\x0006D¯Ik1\x001bGÃÐ´\x0016I\x0016-MÖ\x0000H£5Ò¤ *A©Þ'½ºa\x001c´\x0016IH¤\x0005ôÞ%´Ö\x0014 PT\x0001	IH@\x0012]L§£ç§G»ýÞr¹2ÍLÓI¯ÒBU\x001c\x000eGÍÖ~´\Ì-çÒ\x0006ÕfdT¢ª@kMk\x0004T\x0015Hr8\x001cì\x000f{S?)e\x0018\x0006ë³sçësã8DBï]Mª\x0002 A¤JBÚ 
£±µÑr¹2\x000cÍÅùÚv÷äáñÁb67&§ÓÉr±d8êÕÁ|9WÊn·SÕõ¢&»ãÎ0ÎÖkóÅÌá\x0014ùÌ4MN§n\x001cfád8èU6ù|n\x001cGÃñh:N\x000eíd>_èÇÇ{Ò28??3MG¿üòO>Ùí\x000e§n:\x001d¼º½öúõ+ßÿ/w\x000fÚ8º½ya³y¶\Î­×küó_üó?ýÅléûï¿µZÏLÓÉÃÃ³ÞËñ´7ÍüéOrv¾òß|kµ\ûõ×_}þüä?ý§ÿäÍ¯¬W+-¼ùê¤üé?yñâÆ\x001fþ»ÿÖ_þü\x0017\x000fO^¼¸qÿôl6{~zÖ{9\x001cîîîhQÕ]ß¼°X­|øôÉófcµ^¸¼¾ôîý\x0007ªÙlz5ß~û­û·?Ù\x001f\x000ev»­/_9ªøùw\x001eÎ\x001fí\x000eG777...¬WgæóVÝnÓE×«\x0012ûaD\x0013cb66Ñ0H"h*zÐÚ\x0000hJ©DC*ºR\x0015MSºÒT/Õ©bl£aIJtÑÄ(AR -*$A´\x0016ITQºVAPTi\x0005QUZ*ÒH"PE$\x0014\x0012\x0000 Ö\x0014TI"A!D)RU 	Jé&UêÿO\x0010~-Y¥iÝú·ê¡F\x0007KV¼Q\x0016@@\x0004x9<Û\x0000\x00022\x0017¸ÀôÌTu±ÌÈ\x0008gæÆí0Õýa-QU \x0001\x0000</p><p></p><p> \x0010¥\x0004PÞ»yô>IB\x0011¨ÐÖÖF­¤$!!\x0000\x0001U@B\x0015\x0014</p><p>\x0000tUA©*\x0005</p><p>\x0000@</p><p>\x0000\x0001¡¢P1j¥ZY-.¶[/Ãé(\x0015«åRµætìm©g>+$ZkË5xyyq8N^v{/»õféòâR\x0015ÇÃd:¼¼ìÌ}Ò{$1\x000eÅ¸ HºÃáäééÉóó³åjíe¿·9n½º¾Ðûd¿?iÃhg»Ý¯wú<ibµZûæo)\x0016ÃàË\x001b=ÕréþþÉÏ_½<¿øî\x000fßúÍß¹»ÿêêúÂz½Ö;m\x0018,\x0016£i:º¹¹qwo1®Ãèõë7\x000es­
\x000eÇO>Z.F¿ûÝo}øõ_~þÅ÷?¼õ»ßýÖ×¯÷öË3ëåÂW×ªÊr¹p}yé4O¾yûÎÛ·ï¦îøü?|øðÉ_þò«Â4uÍVðéÓ'××\x0017Î.Ï¤Êñpôò²7ÍÕõµ_?|ôéóÞ»ËËKÃ0¨jÎ¶\x0017æÃÞ<í¤\x000cé¤kU¤TaX\x0018ÖJ)</p><p>¨ª\x001eAUi­$ô$Z(´").\x0006i1OLÓ¬Ui­iÒ\x0014T£hPTºRREQ\x0005¥*¤Q$T\x0015P¡ª@UT\x0015\x0005¥ª¨\x0008ªJ!	¨¢\x0012PEQUBA5PÕU5UE5ÕªAUQ¥¦ÑHª\x0002\x0012</p><p>	¢\x0010E(%\x0015A¯èéæy2÷	QÕN\x0012\x0014Z+Õ\x001a\x0013CHR\x0004¨*URÕôÞ\x0001$PU  BPª*é\x0001 RªÄøæÕÕzm\x0018\x0006\x0017ë­ÓÅ¥ýÎ<Ï$ÆåÒÎAëô~¢wã88\x001cÊ<w­5½w½G\x0012Ó4{~y1MGïÞ½uu}e»í\x0016ãD©[¯W6ëµÓé¤ª,£ÝÂv3Kïî\x001eîÕ0j5z||±^­Å¤g\x0006ðÍ7oË¥\x001f?ùõãgûÃÉr¹òã?¨Ä_?¹¸<³^oHÓ;ãb¡D|ûÝ÷àÓÇÏ§£oÞ½÷øø¤jãÝ7oý×ÿéöô¼Óçxýúµï¿ÿÞ¯¿þlN\x000eiîÎ¯®¼yûÚOþ³û·¼zuåììÜ_þò³Å8X­Vë¥ûûG_o¿zÙí\x001cO'o^¿±\ÚXzõzëÿñgËåÂr¹2÷ÉÓÓ£Ç;ß¼{í°?xÙí|ûî\x001bãØ¬VKÓÔN³x~ÞÙï\x000fªÊãã£÷ïß{÷þ;ÃÀãÃy:ª\x0016Z£a\x0018,\x0016\x000b¥¨R</p><p>)PJ</p><p>UhEZ!\x0012JTºªHêE
hæÞQ.½¨\x001aP</p><p>¥I¡</p><p>TQÕTP**H¢ª\x0002</p><p>=ª¨")RªJU©Ö\x0004ê¨P¥*J4¨¢\x0015ÒEI\x0002ÐT\x001bÃ\x0002@)Uj$\x0000^H( </p><p>% ¢¡\x000bæ>¦I;\x0002R\x0004Ph­´¡iC#\x0008\x0005U </p><p>\x0000¥TQ\x0005ô\x000e¥R $\x0008\x0002ª\x0000R\x0005\x0008* !a|÷î­^ÅþèjsæÝëW>=Þùz{ç4D´6zz~1´Å88\x001cN\x0016Ñv»ÑZóò²s8\x001cTÞãñéÅ}&»ÝÁ÷S·\x0018\x0006C+åÒ¼XJºy$ÝËËóva'Ó49¿8â8Mzº\x0017?OVëÑv»\x0005Q^]_[.NÇ¯w\x000fw{¿~øàÍëkç[íom6kI÷ñãg××WÆÅ¨°ß\x001f¼}÷ÎúÙíí½ËsI¼¼<;ì÷Þ¿ïÛï¾÷éÓ\x0017··÷½^[­6=<>[®¶v»7o¯oýô§½<ïüæ·ßëiU
_\x001dOçÝÁntw{ï¿þOÿ\x000b¸¼¾òæíµËóK§ÃÁt\^^Ù\x001fv./Ï]]\Z\x000bã0hÊÝý½k\x0017..Îåig\x001c\x0017ª-¼ìö>}úäíÛ×ªÊóó³\x001füÑj½2ýiòôø\x0005é\x001d]\x0015ÃÐ¤ (Ri\x0012(*R¥)e\x0006M£HºRR´</p><p>U ª¨"\x0015½O\x0004J\x0015U¨Ò@¡TE¡*ªj
@\x0012U%ªB©Hu½R¢´jª\x0006­J\x0015ª¨"h\x001dRUªhUª</p><p>BQ((@QôD\x0004MU©*I@+&\x0002"@H+I\x0011TIB¨ </p><p>$ÑçYú\x000cªJ\x0015\x0005J«2\x000cÅØ\x000cC©FU©jh¢P ªP(4ªHÒÓAUCPU(\x0004\x001dQ\x001a</p><p>PZ#\x0001ª ¨\x0008</p><p>áÿð¿ÿÏÿ·³õÖëÍÖ\x000fW\x0017Þ÷½ó7ï´a4´&b>MNÇ£Þ»q\x001cT5ËÅ¨
¥÷Ùét2M³q\x001cÁáp°ß\x001f\x001dGCk¶Û­i:ç	ôtûýÞÃÃ§çg§Ó¤§¼ìv\x000eÇ£Þã4ÍV«qhæéh¹\\x0018ªÙ\x001f\x000e¦i¶Ùl]]^\x001aK64¯®.
\x0015­ñêÕ+ÏÏ;\x001f?~Ö3y÷ö­ËK\x0017\x0016ãh³9óëî\x001e\x001e=?=Û¬W^½ºvssëöö^kÍ·ß½÷þý;éåééÑt\x000cÃ`½^ë·o®ýæ·?H?þñÏVëµ\x000b\x0017ç\x0017Vëµi
ÃàÕ«+ËåÒ4Gzìv{Zùöý[ÿýÿö\x001fmî\x001f\x001eÜ|ý*q\x001ccóíwï\x0005_¾|öêÕ+w÷\x000f¦éd»Ý\x0018æe·\x0017³qh6µóÍÖÕåÝÞËËÞj½qq~ît:Ú½¼Ø¿ì¼<?Y,G××¯,W\x001b­\x0015EkM)PÕTT©*ÕJUQT\x0015UT©¢U©*¥PªPLól&ã8Zo6qÐªT+­ª¦ª´VªJ«ÒªÑ\x0006U¥µ¢¨*M©*ÕJk¥ª©jªÊ<w}P\x0016¥a\x0018Ô@UÓj J\x0003¡¢ª¦ZQ*ÕJ \x0000</p><p>\x0005¤ëÓäpØX­VqTJ5´F\x0015\x0005¤"\x0012¥hMU¡4¥ª@ªÌS÷pwçååÉÙöÂf{&yî$hjhæÄétr8\x001e­l×+ÃbE[P\x0000(U¥µ¦µF+=$\x0010IL§£Ãaof0£íöÌv{n±XP¥ªÐõÞ\x0001P(U%¡ª\x0019Ú 
ñßÿýþÓßÿ½Ëw.\x001a«åõ¹¤o·>~þh¿Û[.\x0016æÞµ6X.\x0007­
¶½{ÞíLs\x0007½Çn·3Í'B\x000fÏ/ÎÎv..ÎCSÅ4w­5ËÕÊz³år¡U<>>\x001aÇÑf}îüüÜr¹ðòò¬ªÙn6Öë£¯ww>}þìâüÌïó£³­§GÛÍÖ§¯7ÆÛ[¿\x001bîï\x001f\x001d\x000e'ÃÀýÃó³\x000bççgÖëµãé`\x0018íÙÆþôgëÍÒõõ\x001fó\x001bÏOÏl¶KZë6w¯_ùýïÿàæËW?ÿüõfí\x001f~ð_þËAO_Øï÷ÖãDgçççÒ»Öoßk»ZyuqfÑ?ýô³Öa\x0018ìw{÷÷÷îï\x001eÜßÝIÊãó­ªr~¾ñø|¯0fÃAO7\x001f?é½ûî»o\]¿s{{§Ï1Ï³$ªVMUWUÊ 
^\x0001BRJSUzïTPZ"HJ¤)³*ªhUZ£µRUªRR \x0014\x0002\x0015@\x0014J\x0014P\x0005ÐhVj\x0006\x0008\x0000@¨Ò4\x0014\x001a\x0010($QÕ\x0008©H\x0002zïÒgÕRZ
´HQJBª@)@¨¢¨j(sõÞRU</p><p>BÐZim4\x000e£ª.U(\x0004!$P%H\x0001ª¤\x0014.	H\x0004</p><p>¥\x0000\x0000DU\x0001H\x0002º\x0002%Æýþèt<Y-\x001c÷2Ï¤[­VÞ¼yk\.LSw<Nºn\x001c\x0007ËÅBOl6[ãr¡$¦Óäplú©[®VZ\x001b<?ï|þüÙ4\x001d½zue±\hù8[­Öë­Åb4Ï'Ã>ÆáRz,\x000b«åÂ4Çb±r:\x001d=¿¼Øl6Î¶[\x000f\x000f~ùå\x0017¿\x0019÷ß¼q}}é?ýÅ¿ýñ/Þ½~å»i2÷£û;ûýÑ7ïßx÷vi16½O>|üä|»6´²üë?xýúÚÇ\x001f]øý\x001f~k·{öË/¿ê½LÓäîþÎ8._;\x001c\x000f¶g\x001bIüË?ÿÿü_þ³ÿþ¿ü£?þéO^\x001e¦t§¹»½½3\x000eÍj³6oÞ½µY¯¼yu­ÿõþa±²\­]\_y¸²Ûí<=\x001d½zueµ\¹¸¸rw÷`÷r°Z,m6\x001b77_¬VKß¾ÿÖÝíÃñhêÝþpÐZ³\\x000e½ÿößþÕõÕ¹×oÞ¹½ù"­PZ±\x0018\x001aTÁ B+\x0000D%º\x0006 ª(!\x0011HIHºJTèºêªVM\x0015 J%B)\x0001ô</p><p>"</p><p>(J!\x0012 ¡@DD\x0012\x0002\x0011¡(T5\x0005 @\x0015\x0002\x0005\x0012Q è¢±ÖJU B@ HH\x0008ÒE	</p><p>ª\x0011(U]tÉ¬÷Þ'I\x0017\x0001=Q:</p><p>RUªJ)$"REH\x0011@\x0000	 $¨RUH  \x0014\x0000J\x0012U\x0005 ªT\x0011\x0008ãwß~ël{f14''Ò©\x0018\x0017£W¯^Kè½ûå×Í}\x0012\x001dÑ3©q\x001cÐØn6¦ÓÉ8Ç£Ã~/m6k§ÓÉÜ»Å¸´Zn}ýúÕÝÝõfe\x0018\x0006ûýÞr¹¤º»¯¤¬7[û\x0017§ÓÉb1Øív...lÏÎ}¾¹â¯Æßj­ùæík\x000f÷ïìwG//;ÕhwØ£9Û9\x000en¿ÞX,..Î-+///~üñ\x0007_on<??«j~þù/\x000e\x000f\x001f>[,\x001emÏ·Ö\x000bw·wþôÇ=>ì,\x000bóÄ<u§ÃÉét4NZkjRñòôìþáÁ»×¯½yõJ
Å¸ðòøh>\x001dì÷qwÿèéå³ÝÁþ°7Ï'ÕÖoûíöÌ_?Z-×ÎÎ.lÏ.{ÏOÏ¦ÓÉ84ëÕÊb±°Ýn
Ãàe·³Ýnl¶k/Ï;UM4¿ÿýßØí}øô+U¡\x0019\x0017
BI\x0011@¡B\x0012Õ @BKi\x0015DBBB%\x0012Ò©VzïzïJPQ¨(\x0004j¥ÐC%\x0008A*U¥ª\x0001Þ£ªT+zªRE\x0015VJÓª@U\x0001 Pª</p><p>\x0004A)ÒCOD\x0007UBT\x0010@B\x0015\x0004\x0011tDOPT¡£D\x0008BÒ¥ÏzDDÒ)F\x0002\x0012ªh­TQ\x0005"¨H¢</p><p> J\x0012I$Ñ{$\x0005\x0000\x0008¨*I@\x0012\x0000 \x0010	ãùÅÕjeNú<É<Iï¢T¡ñêÕ+sï¦ùäöîVï]'ÇÃA\x000fÓt4M'§i²X,,W\x000b\x0012ó4és·Ù¬]\æîø²·ZM./¯õ\x001e77_©²X­T
N§;ç\x0017k/»\x0017»çwoùt2N\x0016Áét2÷îâêÚ±sûðäç_?¸¼8óúÕkÿù\x001fÿÁOþÅÍÍ\x0017ßþð­\x001füÞýíåbTÕ\x001cGsb¹Z9&ûýÁÏ_ìv;U£¯ÆqÄËËÎñøèz¾òîí[×W>~üøæÝ[§ãÉ4M\x0016ãàËÏîîn­W[oß½µÙ¬->|r¶9³Ý¬-ÇÁóaï×_~u:ì\x000c-N§µÛ[]s}}å*ç~ýõõzíÛo¿3O'w·w./¯DlÏ/Y,¤wg­Ï77v\x0003iì÷{t\x0018\x0017KÃÁr¹4\x000bãä\x001f~ïßþõßdÚ«jª5¥$\x0005ªè(\x0014Fu\x0005(\x0014ª</p><p>\x0010R¢B©¢D\x0012I´¢</p><p>\x0014U4ZJ¡Z©*­Ó«\x0010 jª\x001aªBI\x0002¦ãH&ã8\x001aQµ¨*j V4MU*\x0012hè\x0008JB\x0002RE¥Kºy-FªJ\x0015(\x0014H\x0002B$Ñ{§OªJ)*\x0012</p><p>%\x0008	!s×çDµR\x0005ô\x001eªK\x0002</p><p>C5­5Õ\x0000 \x0004\x0012\x0004H\x0001"\x0000\x0000\x0001Q(UP(\x0000U\x0002\x0004("¢\x001bÇ½Ó|´?\x000c6}&\x0001Q\x0002ah£W¯^#¿üìññÁépðøôd·Ûyy~6Ï3\x0018Ázµôøø¬Usv~îúêÊz³r:\x001cG½w=±Þ,]l¦ÉtÌóI\x0015gW\x0017çæSw&ÛÍZÛn\\^§ÙãÃ¹ÇÕùÖ×ãÎÓÓ³Þ»¯·wÞ¾~í¯þð[Ï»ÇÇ\x0017«ÅÂûoßººº²{Ù\x0019ÿò«ûóGÿøÿ¨ÏüúëGÍÊñxrsóÕoû£ívíúúÚv»5ÝóÕjíÛoÿ;_>ôõë'çgV«¥Ï_¾úúõÆÍÍÍfg»=óøøàt:z÷öµWWn¾Þøzsãññ>N\x0007ÿ\x000fçØãßÿø÷ïÞyu}i:\x001c\]_{yyòë¯¿Xo7è\x0014÷÷·^]_\x0019ÇÑØô(Aì\x000f\x0007sãñä°ß\x0013æ¹[¾º6.\x0006\x001f?~´^­üþ÷ëñî³V\x0003A+P \x0006
\x0002bÐ</p><p>	B\x0015¨\x0002	4ª®\x0014)Ðª\x0019Û µF\x001a¨FRÒªT\x0015¢÷\x0019T5Qª5@©*$X,FÂ8.,\x0016\x000bªKAS­iÕ4E(%\x0015\x0012¤\x0010A)*:¤T</p><p>%=úÜ¥wPU\x0000\x0000¤KJUIº$\x0008!U</p><p>\x0000\x0012t.ézïz'¡@@\x0012I\x0004³VÔÀ04Ckzo </p><p>JuT$\x0001\x0000DGGèT©*\x0000\x0001¥ª´V\x0000 </p><p></p><p>$¡¨*ñééÑËîÊ¼ZJ \x0008º¤T±^¿~K\x000f\x001f~ñôøè4Mv»VÍv³5K­5OÓ$éÎÎÎýðýw\x0016²ßïµ6X.\x0017NÓÉ<l6\x001boß½q<ìí^îo\x001f%q8ì¼~}ål}æóÍ§§ÕbéÕõ`ÊÉáp°X.\x000cm×+Sx>\x001c\x001dö{Ï>Ý|ñÝ·?¨\x001aÌóÁ«ËKUÝí×;_¾Þ:\x001e'ßÿ£óó\x000b77·æyvqqnØûÏÿù¿óã?úróÙÓÓÙ|Ak¼º¾t:íýó?ý³O¿úÍo~ãoþæo¬VK\x0012m\x0018lÏ¶ö»O>ImÖ®/_ùËÏõyöÝ·ß8;¿ðáÃ'ËÅÊþùÅ¿ýë¿Z.Fã¸tyumh§§gÅÊi>yóæÇ§g»ý¯_-WKOOª6\x000cæÓìl{æååÉÐÊn÷âp8º¸¼°ßï\__;\x001eOþúoÿÁ×/\x001eî?IV¨PH5Bª\x0000:¢\x0002DW\x0015\x001aJ:½ª¦\x001eJ3\x000c£q±ÔZ£:5¨\x001a¨RUJiU</p><p>\x0012\x0001]\x0012	©¦µB¡T\x0015H¢÷Y\x001b\x0006mèªJk%mT¨BRJ!@¡\x0010 $T\x0004I(\x0012>wÓ4{\x0017\x0001PJ!¤¤$]ÒIG£¨*\x0000</p><p>\x0012$Ì¹Ï ZÓªa"	"Õ5Mk¥µ¦:¥D \x0002\x0014</p><p>$HH$!H( \x0001ª</p><p>(Z
Zkzï ¡\x0004\x0010$ÆÍöÜz}f9®'=¥÷èa¨BIuÁÐ\x0016®¯®\x001d÷;Óáh¿\x0018m,\x0016Kó\¦i¶?ì\x0019Êrµ°^/oôiòôüd·?¦Y2\x0013ÕjiÐ<?î]ëéN§Û¯\x000f6ë×¯_9\x001eöÒãååY\x0012gç\x001bÅèy·×{\x000cÑñ0)Íñ8¹ÿõ}w~v¡2\x0019ª\x0011çç\x0017gg\x0017aðéÓgwww^½º6.Wö\x000f\x000f~ÿ»7înoýë¿ü»§\x0007\x0017W\x0017ÎV[«ÕÂÅùÆóóûû[5VÓÜÝÞÞ»¿¿w<N\x0016\x000b>}úèüüÌ0Û»;§ÓìÍw~øá\x0007ÛõÒw¯ãÒýÿY\x001b\x0006ã0{|½{TU¦\x001eß÷­³³KÃ0èóìùùÙÙv«ëþòá\x0017W\x0017WTs~va±\x001a¦Ót4\x000bïÞ½ññÃG_nn½ìvv/;gÛ3ËÕÊ¸\¸¸zåpz1Kaê\x000eº(\x001dÑ
(ê¥t\x0011tA:)ª\x0015\x0013U\x0003-j(qe\¬ÕPÔ¬4ePUª\x0002\x0014¨D4\x0012PB©j(À¬TIQ­Ó¨* JèB!\x0001\x0015$ @$Q)</p><p>R\x0012æÞÍódÎ,\x0015tP){t (T"T4UÑQ T:2Íegª\x001bÛÂÔ</p><p>eÎAR\x0012\x0004P* %é$Ò¡¢</p><p>T> $¥\x0000\x0014JPÕCÓ{Ìs$\x001d%	\x0002H"ÊxvvæÕÕ¥õØÔñYÒ%D\x0005\x0005AIX,\x0016ÎÏÎ¼oM§-\x0016³ýar<í19?;3\x000e#Ê¯¦i2Ï'/»ý~o1¥Õê(q\x0018[®VÇ£¹wÂóÓo¯¿³\x0018\x0007\x000f÷\x000föÞ»iÍ=Öëýaïp<çÙéxtqvn¹¼Ö§Y?\x001d¬×+§\x0013ûýj^½ºVU~úé'///Ç£ï¾û^\x001e\x001e=><øüùççg_>¶9?3\x000e£ÝÎn·÷õæÖ8\x000bçgçÞ¼}ëòüÜnwp8\x001cUÅrÔ{÷òòâÍ·zï.//yyÙ\x0019\x0017oIù·ÿø£»ÇGï¿ùÆ&qwwëââÂïÿ{ã0:\x0016Áãã£ó³\x000b»ýìßÿãüðã÷æ©{yÞy÷îÕjåp|±ßï´j\x0016ãÂ8^¿yc·?xyÙI8\x001dO´ÉÍ×¯Ö«Ñ7ß¨~4\x0014</p><p>AWh\x0014ÍLèPEJ\x0010\x0004Ðgzï¨*mlJ)´VÆqPC¡$\x0002ª)\x0000$EQ(U\x0005¨*	\x0000"Ñ\x0013A\x0001</p><p>\x0014$\x0002 !\x0002\x0012é1Ï]OD\x0012 @\x0017\x0011I'¡\x0002RT\x0013\x0010D\x0002\x0004D\x0017sbgSõD)Ã8\x0018ÇQ«#!õ $\x0005$z:éª" $D\x0012é\x001d%UR¥B\x0012½GÒE¤#\x000cÃh³\x0019%q8\x001c\x0000\x0000\x0008\x0014ãñ°7\x000eÚòL
MUiU</p><p>©\x0010 	ºªRC³^­\^^éáx¸wØ?¦$¦¹¦Y\x0012I\x0010ÃÞ4wmXX®"\x001e\x001e\x001e\x000cÃàüüÜv»ñúõ+ÏÇ£Þc:\x001d\x0007ýA\x0012///aa\x001cGÇÃÑzµ¶Z­\x001cO'p~vf\x001cGõÆùÙÖùå^÷vûd¢±?\x001eì^^\^^Z¬VÚ0ÚnÏ\]^æåjá\x001fþÓ?¸¼ºò²{qwçùqçúò7o^¹¸<óó/?ûúå³&þòó¯\x001e¼{÷Ö8.¬×+OOÏ÷¦yv{ûàöîÖt:yóö/7_ÝÝ?X®V\x0016«¥õfíöîÖr¹ "f=³ósû\x001b©zw8\x001c¬\x0016\x000bã8:;Û:\x001c\x000eÇ£Ãþ¨\x000cóÁétÔ{w:M}øðAïÝÙù¹q1x~Þ\x0019ÇsÛÕÚP]«êdP\x0008Ò\x001bE\x0019Q\x001a¡ D\x0017jQ}\x001e½E\x001b\x001a¢÷®§¢VP@P\x0010\x0004MUI\x0000 \x0010U$\x0010@TDÒ%QEB\x0001\x0000(%E\x0012\x0004¤HH >Ïæy\x0016\x0010!\x0000\x0011!PT\x0012R \x0000$\x0004\x001dsbgÓ<K+Ã0\x0018ÑÐÊIB)Q\x0014ª"\x0015I\x0014H"Jª$¡\x0003D\x000fI$ÑCOÔÜÍódgIT1÷HX,FÛíVïÝñxREUI¢ª"1n·[ÇãÑnlÆ6¨6</p><p>ª5ªI"¡'Jªf\x0018GgÛs=e<>=9\x001cæ\x001e\x000c(TÖ\x0006ËåÚ<ïÕ@ÂÓËãngµZiÃ`\x0018ÃáàêòÜñx4KI×{¬VKÃ0è½£¹¾¾Ò{÷øø £ÍzíñáÁåëW¶­y]]{ýæÒÓóÞ[\x000f\x000f÷6g\x001bsï\x000eÇoÞ¿w}}m¿Û\x001bÚÂîeg»Ýº¾ºöúÍ[÷w>}úäöî«íÙ³­jåòòêÎ¶[½w»ýÞëW¯ÜÜ|u{{g±\x0018­×+ß~ûÞÏ?ÿìááÞv{a·?yy~q~õZÇj½¶Yo|üðÁñtòøøèý»oÌS÷?ý/ÿ?÷·ç»÷ß{yÞÛIk¾ÿþ½õråùéQkô~²Ù¬ôLöûçç\x0017ã0x~~¶X®¦ívãééÉ0\x000cæyöþÛo=Ü=øåç\x000fþú¯~k\x0018Ge\x0006R</p><p>½ÐJPA\x0018\x0015!\x0015*T#DzW¦é\x0015¦ª$ô¹#ºnÐ\x0008ª\x0000(\x0008\x0002ª</p><p> ª</p><p>T\x0015\x0006\x0008HB\x0000\x0000U</p><p>\x0001\x0000\x0000H\x0000$T\x0001@P ÷®Ï³ô¨*$ 	¢*ªJ\x0012\x0014U¢\x0000B\x0000\x0000I$D(]EÐÑ0NaPEæY×@U	 P¢\x0010\x0004DÒ¥^M¥$ WIkªyõÞ%ìö{ûýÁf³µXzïæ>[\x001a-\x0016\x000bëõÚ<Ïz%\x0000@±µæùeçÇ\x0007õúÊj\x0018$(\x0004s¢'R\x00051.\x0016./_Q9³ÝÁÃÃÅr´Z.´6¨j§#PEïÒ»$fåeäþÁr¹4Ï³ãñèt:Úl6Ö5½\x001bf8z÷î\x001b§ÓÑÐ\x0006ëõÊ4\x001dLÓlµY[Ízí\x001f¾5´ÁÓóÝþàÍëWJùéÏÝáp²^¬=ÏÏÌq{«Ö</p><p>ã°vÿä_>ûðñ3½ÿÖùÙÆ/w\x001f=<Ü\x001bÍÙvëîîÑÙÙÖÊýã£³ó\x000bûÃÁÜùù_}÷ý76g+ýËìpØy÷Í[OîîîiÍùÙ9éVË5	U\x001e_üæ·[oß¾õøüd·ßY.WÖëÃ´÷ùóëËKOO\x000fX.¶Û­a\x001c\x000cãè§?ýìææ«ívíÍÛ·Þ¼yCºÞgëõ\x001a1N63Y®¥ªRE)!Z\x0014 \x0012RRQ"E*\x0015ZT#³¦T¡</p><p>@\x0012U\x0005B$PªH \x0000(U$AT\x0015¤H\x0002@hP¤($\x0000\x0010\x0000@IB\x0007\x0011	Élî¤« \x0004\x0005\x0014\x0002¨R ¨R"B\x0005\x0001(\x0004ô ª¦jPmTmÐQ\x001bFNz\x0011U¦jÐj@	@R</p><p>H\x0000T\x0015Ö\x0006åÊ°ß;væyöôüäñéÑz½ÖÚqlN§É8\x000cË¥Õzmf»ÝdVU\x0000</p><p>ãùù¹³íþp'Ã@5Ð{GP"z®z\x0010]ª³³3oÞ¼±ß\x001f	pfãbi\x0018\x0007ó|"Ýóó\x000b½\x001bÇýþ¨µAï1fÇÃÁ4_^X®\x0016ZHãáÁn÷l¹XØí´\x0016Wv/{ËÅRÖkûÝ³>OÎ¶[>vûõNR^^
ÃàtÚ;ìæi6Ï³Íríl»qo¹ZúôùÇ§\x0017sçx<ùñÇïüá\x000f¿÷üül¿?èÝ~çåeç?¸<¿ð7ûWnovóõVkÍ¸XÚïvþÇÿÏÿ×Û·o´6z~ÙyzÙ\x0019\x0017\x000b»ÝÎv»u}yåþþÖîåÙo~ó[ÿé?ýo¼<¿øòå³³³sOOî\x001fnãÒz»¶G7_î|üøÙÃÃ««KÇÓl<\x001c\x0007»ÝÎv»qØíGûýÁ8¾Þ|1\x000cÍ·ß¾WUZkv/;×W×q¡ªk­;E\x0010\x0010BB¨.	$\x0008\x0015I$A\x0014Z+­
ª ª\x0000H¨*\x0004@\x0002A\x0000T\x0005\x0000\x0010\x0001D\x0012I$¨B	z¢\x0004E\x0015\x0004ª\x0002DR\x0008U¢K\x001eæy6&ó<ª¦\x0010\x0001I\x0008ªRA\x0015URE§\x0010AP</p><p> H$Ñª´6h\x0006-ÍÐFÃ8\x001aQj2÷ÙÜ'½wUÖ\x0006C
D\x0012Õ</p><p>\x0000\x0000$\x0001ÂÐ\x0006«åÊz½q:\x001d\x001d\x000e{\x000fÆai\x001c\x0017q´mktÃQkÍ0\x000c6µ¹O\x0003\x0002\x0000Æ«Ëkßû<]i/Ïæ ]g½7)"HÊlÌ\x0002¤«b½\{ûæ±5/»gûÝAU\x000c#Wsmh^wÆÖ<¿ì\x001d\x000f'Ã0X­\x0016V«*vûôYt··wz­\x0016+at~~îáþÞjµ\x0006÷\x000fÎÎÎÁÃãõjíëíåò\x0017øýRkçþàééÑÃÃiêTY®FÕâêê\)ÍÖ<Oîoÿú÷63­W¯_©*üãOöû½ívm14Çytn¾XmVÞ¾ym½Zx~Þy~~qºíöÌ4uÓ|²X.==½è»½a\x0018Ãàp8xzzòôôè\x000fø×¯^)üé§ÏÎ6\x001bWöËåÂj½ÒçõzíÃOa°^­´j\x001cG§ãÉ86ÏóÉñt4OÓ4çîO?ýäx:yu}åòò</p><p>]tÅ:¡cVB)A</p><p> \x0012T\x0001 \x0008\x0002ªJ>Oæ¹K\x001a¨BA\x0008\x0000U%	º\x0004$\x0000 \x0008\x0000zf=]\x0014U \x0000\x0000 \x0000\x0004$\x0000 %Bºy¦É<Ïº.B</p><p>=":E\x0005U(JÐE@\x0002!D$DtÕÊP¦TQ­ã`±\x0018æØgó<é½¨B+</p><p>¢*\x0004­DtÑ\x0012\x0000U\x0005`\x001cGÛÍÖt:9\x001eNv»~c\\x0016Ëq\x0018¬×+óÜ\x001d\x000e\x0007ëÕÊ8¶3éÝét\x0000cæn5.d\x0018Í"õÌú<2«*]WÊhÕMóLHº$X£««KëõÊ}»'Ý0ÎÏ¶ÚÐôi¶\®ìO³ãñ¤µ²X\x000eÖÌÓÉ4Tk\x000eûÓéd\x0018\x0007Ïö¡ãéäþáÉ0\x000c\x0016«9åùñÉÓã£wïÞ\x0019Ç¥Ç§\x0017¿Ü¸½»u8\x001eôÄnwÐ{wv¾AHU5«õÊùÅùoÿêÕÕ+øýïl6KéÝÓóÎ¿ÿÇÝß?z÷î­ÅØì-+WWç´Áátp?üî7atJüúë¯Þ¼þ­³íÖùÙöìÌû÷ïýË¿ý«6«ËK\x0017\x0017g^^%üôç¿ø|óÕÓÓ³ï¿ûÞj¹ôñÓG»Ý³¿ÿÛ¿1Ï³¤¼zõÊííªBìw/"^^væy¶?ìì\x000f;OOW¯^ÛnÖ¦Ó³³\x000bÏÏ;ÇýÞwß~k¹\x001cõ>y|z²\\x000c6«¦jP&D¡B\x0002¤"!E!\x0002\x0002*\x0012"zbg}î¦iÒ{Ô@D	B!\x0004H\x0002\x0000 ª\x0000¥  zfÑ%!Tk"\x0002QU$\x0000\x0000H"¤®÷nêÓt2Ï³¤KfÉ\x0002\x0000\x0001*(DO\x0017%" T K\x0011%hE¨b\x0018Å8ZC>wó<K\x0002""\x0018@!PèV\x0005\x0000¨*ÅÂf³µß\x001fì÷\x0007ÏÏ/>þb\x001c\x0017\x0016ãR\x001b\x0006ËÅhf§v´l\x001båÊºOæyÒ{\x0017À¸^¯ãÂ±Ïúa§\x0016£¾Xçn'©&\x0015¡b;"\x0002A@UY®W.ragé]\x0012I,W\x000bÛ³)qØ\x001fív{ÁrÑ-ÎVaÐçÙÓÓ³åbáoß9&ÓtrJWÊ4ÍN§ÉÙùîp<\x0018ÇÑáp°Z¯\^\êáÓç\x001bûýÑÅÅ¥iµÖ¬KqáíwqôðøàùåÙ·¯_éS÷Ë¯\x001f\x0014¦i²Ùn­W+ËÇÇ{«õÆr¹²Ûï½yû»Û\x001bçû½Þ»Õfc½Zim´\m\x001cöGåÊùùèòòBÓLÓÉv»õ»ßÿÎ×oü¯ÿôÏþô§?©Ö_Øl¶\x001e\x001f¤Ïvû£ÍzëååÅ<Çjµr:¼~ý\x001aÝv³µ?\x001c}úüÅ~¿³ßïõ^~L÷êêÜétôæÍkÅèîö«Ýnçõ·¾~½õüòâõ«këõq\x001cÌ§\x001dI\x0010A(é¨\x0012\x0011¡\x0008J\x0000\x0008sNÞ»Þ;B"¡</p><p></p><p>\x0001	\x0004\x0000\x0000T$\x0000 	è=\x0012ÒI"	!	P\x0000\x0014ª\x0002I\x0000@\x0012½GÒÍól&Ó|ÒÓ	\x0002\x0001UPª\x001aP%!H\x000fP
\x0010H\x0000\x0008U\x0000\x0005$¨*­5­5Ã8Z,ÆÅIÕNïÑ{P</p><p>ªRA\x0015	J)¥\x0000\x0000TÞ»$a°^¯;\x001e\x000f=??»¹¹±Z¯,\x0016£v~¦ÆÁá4ÑNË¥Õje&ûý\x000etãÅå ÷nOZBûät:ª\x001a¤J\x0017M\x0013Ý<ÏÒC\x0003@\x0016\x0011½wãbéâêÒ|:\x0019F±X.l·\x001b=1Ï]íKºÃáè4MæyvØï\x001dGÛí¡ÚjdÕµVæS·Zoã"X,ÖgKëÍÆé4{x|r8\x001eµqaê\x0007/û½\x0012ÛÍÚÕÕÕbpyyf½9óË/¿¸½ýj\x001c\x0017®®®=><úó±^/½~ýÚb¹Rû£õzi½^;?ßºººò\x001fÿñ\x001fö»½_~þÙ<uó<k5º¹ù"áõWZkV«Å8¸ùôÙÓã£åbi½^Y.\x0016àÝÛwÞ¿ïááÑÝí½.nïî½¼ì¼zõÊzµÒÑýý\x001f?¸»{0£$Ço¿ýÖÃÃyUãqv<NN§\x0007ûýÞ86Uô>yxØyxxòáã'W×Ç¥\x0015J\x001bÚØN'%ªº$\x0012:hªº¤¡K(\x0004\x0004I@\x0012ó<;N ÷HHBJïTE:PU\x0012\x0000¨*\x0000U%$\x0000zï\x0012zÒ;é\x0011!QU(\x0014\x0000¨*\x0000IT$ 	 Hº>Ï¦iÖ{WhU(D))\x0014\x0014($¨ @\x0002T\x0000\x0000H"¡§çY *ª©a0\x000c£a±´XMV«ç§\x0017I*\x0004A!@¢*ªP\x0002U \x0000Æq´ÝnN'óÜ\x001dGÏÏÏ¾Þ|µZ®\x000cæ¬m
\x0006ÇãÑ0q\x0018­×\x001b½ÏÇ#\x0018[.ãÈj+ãBÄ<\x001d\x001d\x0007­T\x0012e6§\x0013P
\x0005\x001eÞ;Øl6j³ÑçÙa¿§ÓZ\x0019Z\x0019åb°Z­­7+ÃÁn¿s<\x001e]]ØnÏ\x001c\x000eGUÍb9\x0018Ú`\-ì÷\x0007ÃÐ\x001c\x000e{\x000f.//,K§ÓÑ8.ÝÝ½øôå³\x001a\x0006ÕÂrµtq¶ñöõkWW\x0017Æ¡¹¸ÜZ.×¾ýî\x001b>òÇ?þÙ_ÿÕ_yÿþ[­»»;·w\x000fqåõë·\x0016_¿~µ\®|½½us{k¿?Z­W¶Û3//;77_Ýß?Z­VÞ¼~ãÍ+ÛíÖÕõ¥_~þÕÍÍWói6
>Ï>~üàx<¸8?³X\x000cÞ¼yeµ^óó3¿ÿÝoÝÝÝùòù³û×qqyé\x001fþá\x001f<<Üç*«ÕÊ~¿÷õæÆùù¹Åbr:\x001dõiòüôìx<úzsk8¦¯_ýúë¯h..ÖÆq´ßô>R£T'Ð)</p><p>Ñ	</p><p>)\x0004\x0000H¢÷.=zè}D\x0012\x0012 \x0005\x0000 T\x0015$ 	H\x0002H ´\x001a´j\x0004\x0002 	¨*\x0000IT\x0015H\x0002ªJ\x0012\x0000U\x0010½wó<ëó¬÷\x0000P]«\x0010E\x0015@¤H\x001a\x0005E\x0015T$RE ôÞM§Ói2÷.è\x0002¢\x0018\x0006Ã¸°\­­×GËÕ*ªR\x0015\x0012 E\x0005Q\x0015) ª\x0000Bô\x001eUe±X:;;7Ï]==çÙãÓ£åÍÂb1\x001aÚh½Z3ÏÇa5\x001aÇõz#Þ»ñùùÅÙv£6[CJ-\x0006ú¬ÏÓtRºÖ</p><p>%ÕÌô~R	\x0002Dï]\x0012P¡ZÓR5¨-Ázµr\Ã`½Y\x001bÇÑíýÞÜgÃ0ÚIâîîÞ<wËÕèÍWÎÏÎí÷\x0007ÓtruuéùåÉr1ºº8÷ÿb\x0018N¡çY«rvvæòüÜùvãúÕÝó³ãñäÕë7\x000eÇ7¯/ýýßýµÿùù'þó\x001f]_ÿ£³³\x000bÿö\x001f?9?ïÎ/öîúêÍëkíÊýÃ£ùàþþÑz¹öæõkm(«ÕB\x0012ÇãÑ4Mvû³óï]__9\x001eONÇd6\x000bÇÇ'»ÝÎ4|÷í{ÃÐÜ|ýìüìÜï~÷[ßÿðívåþ®îêêÒû÷ß\x0018f³YN·oÞøËÿìãÇ\x000fNÓdY2\x001bÚàoÿú\x000fN/_ï\x001c¹sw÷`µZJg·;Øl·Ë¥§§g7_nüðã÷ÎÏV¦c×û¬\x0002T@Q\x0008I'%		$\x0010HºiN'½Ï\x0006\x0004\x0000PUª</p><p>\x0000\x0000½wI@\x0002\x0001ÖaXhí$UV\x0005\x0000\x0000\x0000H$H\x0002 HJï1M³yîz\x000f¨BQ</p><p>T</p><p>D¤B
\x0004I¨"$\x0001I\x0004Ð\x0013sïöÇ£ýþà4Íz\x0004 PZkÆqa±XY-×ä$:	"J\x0002@\x0012\x0004QBQUªJU¡$@´Ö,Kgggæy¶Û½8\x001dOîïï,\x0016Kãb©µÑÊàx<i\x0006«ÕÊr¹Ä~¿3nÏÎ\x000cã6êÃ\x0012Ø={Ì}Ö@	z5É,=J@A\x0015J\x0015DUé½ª²Þnd^:\x001e\x000fJ\x0019®¹w½wÏ/;ûýAÕàúêÊjµr<<=¿8\x001eOÖ¥õzi³^\x001bÄ86ï¿ùF«\x0002o^¿±?\x001c­V+5Ãáàòü\j¬\x000bûæááÙ¯Ö«Á/_|óþ­Åò?ûóOvØ\x001f]]{÷îÚtÝßÝz|¼÷Ûß~o¹\ùãOÑ{|ÿÝ\x000f.ÎÏ\_»ùúÙ4\x001f¼yûÝáàáþÞñxðßþÛ¿øù/?»¸¸´\.­7+W×¯M§ÙjµòòòdhÍÝýÓ4yÿþ\x001bã8xýúÚÍ/þë/¿X.~øö{ûÃÞ¿þë¿fµ^¦³íÚ0§çgûû\x0007CkÑblno_¼ì^\^¾ruyéùùYáòòÊj½öpïl»qyyi¹XN'½¯´aÔçª\x0010\x0012T \x0012DH¤wDÒõt)\x0014ó<9Næ>\x0019ÒT/ª¨\x0012\x0014 ¡</p><p>\x0000$è½ª\x0002\x0014ªhã 
BABA\x0003D\x0012\x0000\x0004$P¤K$æ¹¦Éé4If= JURA\x0001Ò¢\x0000 è\x0000$æyv8\x001eí\x0007Ó<H\x000f"\x001d)QªÊ0ÆÅ(Ó¢(\x0014 \x0001T¡HQ\x0005(U¥µ¦µH.\x0001a°^¯Módîý~o·ß»»»µZ­,\x0017\x000bÃù9ýá¨Z³Z-­VkI7n7[ÑTEZ\x0014¢I5BD\x000f\x001d2k¡j ]tIPª</p><p>
\x0005¨*IÀ0\x000cÚ8ªVÒ»60MÝón§'Î6[°]¯
ÃàTåzcîôÎ<wÃÞ0\x000cv»½\x000f¿~p¶=·Ùnì÷GËåÚñt2Í³år¡Ï³·¯_yzzòüøìññÉb¹ðþÛw\x000e»VkU£/·q´Þûøñívë\x000f¿ý­?ýé'ÃÁ·ß~ïp<ùËÏ¿Ú®·þþïþAkì^^üôç¿x~zVÅíÍW¯®­×kåÒ\x001f~ÿ[?ÿüÑ?ÿË\x001f}óþ³ó­ûû\x0017Wç¶Ûµ¡5Ãbáç_>8\x001eÒ»«ë\x000b?ßØ¿ì_º¾ºpv¶öðto»Ùz~>º¿{ðwÿ×T÷üòl»Ý:ì÷v»\x0019\x0017>|úäùéÉ¸XÙï÷æùäíW¹8?÷á×_=½¼øö»ï¥Ïî\x001e\x001e<<<zûæõje:MIÐE\x0005J¥TH"	¢\x000bºô.®KèÊ©LóÄL%¤Q¡</p><p>\x0000$\x0002IG$D\x0002´ÖP\x0000ª¨VÚ0hUZB\x0002(I\x0000$\x0001\x0004\x0005ªdF\x0010HbgÓ|t\x000eJôNWh(\x0002(U\x0006YO\x0004	\x0014 $J\x0011æ¹;&§y6õû,=¢$tPÕDéE@©jª</p><p>P(¥¡¡\x0014ªJÂ aÞ»\x0004H\x0002a°^¯¦É<ÍN§\x0017_¿~µ\.ãh³^\x000b\x000e§a(ÅÂz½5Bgsïæ¹k­I\x0010\x0000\x0012\x0010@$"$ ¨j ¡tf1\x000b«õÃÞ4\x001fUÍfíêòRz×çÙ<LÓIa¹\bÄíÝ½V««+y´?ììö;°Ýní÷\x0007Ó<és·^­U³³3ËÅÂnwðòòìõ7¾ýî;÷÷wÆqt<Üß?X.Wþò==?ùÃ\x001f~g\x001cvûýñäÿñ\x0017ãØüÕ_ý>Ïþòç½ÿ­>óæõ7¦ùàîî«íÙÍzãîöÖr\x001cý_ÿ/ÿgÿÃÿýÿiX\x000cVË¥§\x0007%8Nþð×m±\ûùÏ6\x000cååyçåig¹\Z,\x0007ÃØüòñ\x0017÷÷\x000fÞ¿ÿÞj}òéÓÞz½²\-<>ýd³]Ùn×\x0016O/~ùðÅËËÎÕå¹ËËsÛí/_nÌól{væ×_u:\x001eN'»û»;ó<ÛlÖ-\x0016Ko~ÿ£Ý®ì÷\x000f £R R³¤KHB\x0002®÷çÙ<wó\x001csïæ\x001eé¡J</p><p>\x0015\x0000¨\x0002\x0012 é 	¨*UMU\x0003I$AT\x0015Hè¡	\x001a  	\x0000\x0008\x0008)tD\x0012D»yMÓd&C\x0015¨*U¥\x0014\x0015ªB¡PEQ]	UHº¤«"!¢÷®Ï]\x0002¥÷ç.Ê4wó<IHæÙáxé$ª¢BQH©*\x0000\x0005¢ÐZÓZÄ04½wD\x0012U¥ª,Æõzm&½Ç4Í\x001e\x001f\x001f-\x0016\x000bÅRkÍjµt:ìje¹X\x0018[£ªô\x001e½ÏªH¢ªP(UHN¢ D\x0012P\x0005\x0004¥U¡ô\x001eZ3.Wa°X,-ÆÑ4wãb!\x001d\x000fGûÝ\x001eÝÔT³\x001cW^ìv{óÜ\x001d'¯_]Ùl¶aÄ4Ma «¥a\x0018\x0014$ÖëµËË\x000bó<¹¿»·\,MÓÑ~··ZoN\x000fZãwoýüó_\__yûî­§gw·w\x001aô~òáÃ¯^½zíÍ7ÎÏÏýÝßýÞb¹tûõÎép´Z,­-\x0017³O>xõúÿÓÿñçáéÑ~·Sýät<"\x001eýÿïÿ«ËK\x0017çÞ¼~íìlãpÜ{~Þ¹¿¿óñã\x0007Û³­øû¿s}ýÚ¿üË¿zõêÚ×Û;»ÝårcµZè8«Ñ»ÞüÓ?ý³±×¯®,KIWÅb±puuåßïîüÇ\x001fÿèúêÊ4M¬Ök\x0017ÖëÇG/Éùù+§éät|&]% º¤\x000bR\x0005*\x0011@RzyMÓdfz\x0014Òé-$J(ª\x0006\x0000D\x0012\x0000U\x0005ª</p><p>\x0003\x0002ªHº¤\x0003èéºhU\x0004E\x0012¥(\x0012\x0002P\x000eTÐ\x001egý4ëS×\x0016\x0003\x0002Òh\x0014(@$RJ)© $\x0012$z"¡UÓªIÊÔ#éæÞõDDÄé4Ù\x001fOjô@Q­T\x001a\x001d\x0005D\x0012PTÖ$Zk¡é=æyÖ{WUÚÐ¬V+é]f»ýÞñxrwo¹\Y,\x0016Zkj1:C3´fLïj\x0018\x000cC4UE$Z\x0011\x0011B\x0011¢¨RP
\x0000T$ \x0015PJOÒÑv±°X,ìö{A»¤KºÖØï\x000f²ÓaçxLs÷õõöÖïó£7o^[¯×Ç£§ÇGmµR58N ÷®ªÌs7Ï\x001dåp8¦û\x0007ËýQkãaïoÞyýê</p><p>>\x0007¯_½¶\®µÖ|ÿÃ{ÃP6¦£ËËs·wwàòêÊr1Úm\]Û½\x001cmÖ+?üð/_nüôÓ_ôósÃ0X-W¶»»;¯®®}÷í{/ÏO2Ìód¿ß\x0019Áj½v}ýÆýý³ý~r<\x001eÑ<>>û÷ÿw¿ýíï\x001c³s«Õh±<\x0018ÆÁõë+gç[ÍÆr¹ôõëWÓ4\x0019\x0017\x000b§Ód¿?ªëf'Ó<9_ª5××ÖãéhWÎÎ^ÛÕèpxÒû¤*"(IDÒ\x0005\x0000	I7M³é4N'óÜ%t!(BDU\x0001 ¦ª\x0000A¡\x0010I\x0010\x0000;s§5I$Q\x0004D\x0004\x0011\x0005(DD\x0012D\x0012½w£ÏÑçÎØ(\x0004¡T©*@\x0000A¡T5UÑ3K:\x0002"\x0008B«ÁÐ\x0006Þ#jÉÜCa\RM\x0010D)M5z\x0007ª</p><p>$!QU(­5I´Ö\x000cÃ U\x0015HB\x0018Û`µZ¶³S\x001dGûÃÁíí­åri\x001cGíü\x000cÍþpÔÑDï³Ö\x0006ÅB\x0002( 'T\x0011\x0008	\x0000¢HP(\x0004\x0004]T(¢\x0017\x0011Ue\x0018\x0006§é¤R`:M¦Ód&½Ïæy2÷n;âe·÷áãgm\x0018\x001cGUe\.¼<¿\x0010^^^<==9;?W­ÙívÇ£õzåíÛ×V«¥þü³¤¹¾¾t{ûÕ÷ßÿà4M~ùù/ÚÐ\Ûí\x000f\x0016Á¯¿~ðpÿàý7oýæ·?º»{ôËÏ­×\x001bÇÓÉþôi¼ÿæ½ª8\x001cnn¿¸»{pûõÞölëí·n¿~u<_8N>}þb¿ß¦nî1ÍGãbðþý{?üøþø\x0017?ýôg¿ùÍ\x000fö£OoôÎjµÄt\x001cNG_o¾JºÍfííÛ7æÓdgÛíFïÜ~½uwwk³ÙZ,FéÝr\x001cÐ}þüÉû÷ïmív\x0007Ï//./.\]¯Ü~åÐ\x001fTMHºh(	\x0011\x001eççn&Ót2O³>w*@$A\x0000@\x0002A\x0001 \x0010DB\x0012DÂ<wó<çÙP\x0005¨*D</p><p>\x0001\x0014\x0002\x0005¤# W3õtsõ>ë¢#º$@5U\x0012T\x0015º$\x0000 )IIH\x0002 	Hè½ë½k­\x0019ÇªÌ(BU#¥÷ç®år&½\x0008¥¤JB\x0015	\x0011Aõ¨¢RªÖa\x0018$´\x0016IÌó\x000c ahVëiÌ½;\x001d}ýzc¹\\x0018ÇÁz½\x0016¥v\x0007c»J)¥µ¦ª\x0002P\x0002\x0012 \x0014%(AQôDÒ\x0011\x0014\x0005P@\x000f¢WCTJ«2£>wÃ8¢\x001c'ó4Y¯V¡yz~6M\x001d\x000cÃ Çç_ýäÕë\x000b­5U¬ûl'}î\x000eÇ£ýáàññÑÙÙ\x0019Uîî¾ºº:·Ýn½}ûÆÝíÓiòõîÎ¯¾\x0018ÆÑaðúúJª<<>¸ýÓÅbéw¿ûQÂ<Í</p><p>×××=¿<K¡
\x001eõyru}i»¹°Ýù<ÝúøáÃþ`&ó\x001cïÞãË/nîîÍÓ¬ÕàÇ\x001fÔ3ë}¶Ýûzsç×\x000f\x001fl7k¯^¿²Þ¬=>>;\x001c\x000f¶çkgÛÇûG»ýìååÅn·÷ñãgßûÞv»1\x001f&\x0012»ÝÎf»µ\.\x0019f»Y\x001bÑ¯\x001f?¦£ßÿö7^TÓ´¶Ýlµi:HÞzft"t\x0012éÑ{×ç®Ï3¢Ð3û,ªJ!¨"*\x0008\x0000\x0000H\x0002 !!¡ÏÝ<Mjh\x0008¢÷®ªDª\x0008 A!\x0012z"\x0008H¢÷è½ë¹wÓ<ç.éB\x0014U\x0004 \x0010@\x0008\x0012@\x0001 ¡K¢§çÉ4Í6X,Zk(@i5Å<³ß\x001fÍSWJï\x0011%\x0002R"\x0014Q$\x0004= Z\x0000¥ª\x0019H\x0006IôÞA\x0012PUÆq´Z­MÓÉ<Oæiòøøh¹\Z.Æq¡µÁát2jM×U/U¥ª(R\x0014(\x0000\x0004ª¤\x001aJU\x0011JPªJPB\x0015\x0015@T\x0015f\x0014\x0008a0\x000ci:Ùï\x000f:Ë¥Ö\x0006ËÕFp<ÌSWÕ,\x0016\x000bI×{÷ôòl{¶ôîÝ\x001b}íw{sµ6¨*\x0012ã0X.\x0017ÎÎ¶ÎÎ6^,\x0016\x000bUÍÃÃÇ§gÓ$­8NÆÅ¨'n¾ÞØ\x001föV«¥¿ùë¿u}}Éb¹ ñðpçîî^\x001b\x0006ÃÐ¼zua³ÝØ=¿ØívÎÏÏMs¬×[ËåÂi\x001d§Ç'gç¾ûö\x0007÷\x000f÷>ühµn\x000e§½ÍzåÝ»÷ÎÏÏ=><Z-\x0017^¿~åáþÑ¿ýÛ\x001f\x001dG¯^_yx¸óüôhº§ççgC¡>wËÅè0MæÓäüâÜj½±\.ýéÏ?y~~tõÝ{7·w¾|¹õøüèñÕW×Wª\x001f?¸¹ùêÇ\x001f0,\x0016\x001c×j\x001e
­dîbüÿ	Â¯fÉÒ3=°\ïÞ®</p><p>\x001d:\x0013	\x0014P\x0002 /ÚFÍMÿõ1¶ÙÌ4ÙTÕDU\x0001J!>î¾¿÷µ</p><p>MG\x0012\x0012ABRjÌëIM-\x0006L(\x0000It·R¢TA$\x0008\x0000H\x0000\x0000\x0018®\x0000HPQH($\x0000$
\x0004)\x0012BN\x001b\x0019\x001eÆhs"(BA©B\x001a¡</p><p>D$ j\x0004PN[ÆÐÕfc·ÛZ­W¦iÒ\x001dUTªFì\x000f\x0007wwwÖS{|±Q\x0015\x0005\x0001RP(4)DBÒRªÊ4\x0015&óL\x0012I1$\x00010Õd»Ùèq¢ÇðÐ\x000f\x000e\x000f\x001f>Øl¶ÖëG\x001eYÍ³Õ4Ïº$º£* B</p><p>\x0012\x0000UE\x0015Uª¨Ä¤Pª\x0014PE\x0008 \x0008¨</p><p>)QÊd&óÄz½q²;1O³Ãáàx\,Ç\x0005±;Ùj"¥j¥»-}ðð°w<.&©&ëíÚv»µYo\x0014ÖëµG\x0017NOvNv;ýÞíí½ÍvëÃå·ï>xüø±i\\Y¯×ÆX\x001c÷ãgOÙí¶^¼|âþîÎéÙ©wï.ýå¯ßøîÛïl6kýAMååóç*<yòXwì÷\x0007ªÄpqq¡Ûû;'»\x0013ïÞ¾sqvæßýö\x001fý~âæöÎaÿàóÏ>òé§¯|xÿÞééÖçæÍë·Þ\x001cÞ{ýæ­Ýnë£NÏN\]ÞÈ´RÓÚÙé¹Ï?ûÌùÙ©i\x001c\x001b=âx\,cè\x001e¶ëëk·/ÌÓÆñØVóÆéÙ·ï?¸¸8·ß\x001füõ¯ßÙív¾úê+7·\x000f.¯®Ìæyc9¶h ­\x0013	ItZw\x00136«ÙzUT(ª.\x0001\x0000(¤T\x0005% ª&L\x0008\x0002 ªÔ<1M¢tSE)$\x0004¡ </p><p>$
"¤I"\x001dItÑÃ2e\x000cë^B </p><p>\x0004PU(I@Rh\x0011\x0000Q iA1X­×6»­õjm&UÑÝ(ÓTV«Ùj5{Øß[Ï§¦*\x0004\x0001"\x0001</p><p>Ði\x0012\x0006Ue&0My%D\x0012ÄT¥æÙn»Ó£õýþÁÃÃ÷ïßÙn7Öë³³s«i*Ó´²,-i	\x0012\x0010\x0001	U@*$"" \x0001\x0008B\x0008J	ºCíîÄ¼Z;\x001e®®¯ÜÞ¾uÿ »Z­Ö\x000eÅX\x0006UNOÏLÓìêòFX­Öæùè¸\x001c\_HÚ2Û[w÷÷^<îúúÎ7ß:==s8\x001cêqT<yñÒû\x000fï½ÿÁn{Âzvw·×}tuõÎ²ðÝ÷?yx¸óþòÚåõÕT\x001e=:÷ìéSO>5Ï³»ýÁýí¥Ï>ùØjµòç?ýÉqiö¹ó³s?¿þÙèÅíý­ívãO>öóë·\x001e\x001eîtÇõÕ­ï¿ÿÉãGO¬W[j2Í³/¿üÂåå\x0007Ï¿ÄîÕ§Oùó_þâáîÜW_|îÅg\x001e\x001eî¼÷ÎñxôòùK5O¾ýî;	ëõVÕìúêÎ4=Øn7_<µY¯ýøÃäcçç=y<tÇ~¿·Y¯Í«÷×vÍzRi\x0012	ItÚH\x001bYt\x001féXÕÊ\³RJ\x0008"J\x0001\x0008</p><p>DR\x0008H¨\x0002\x0000\x0000J)BwtGUÌó$!)B \x0004H"¡;DÒº[w\x001bÝËp\m\x001aE</p><p>¢ (2HB\x0008¢\x0010ID\x0012A\x0012It·å¸è1¬v;ÍÆjµ2M\x0013Ý A&ëÕÊÙé©ó³S«\x0019@$\x0011	\x0010$\x0008Ò\x0011L5ª\x0002ULSçY\x0012It·$\x0000V«ívk¡»\x001d\x000e{·77Þ½{k³ÙçµUiË2\x001a¡\x0000P@"­D	$ @I¨</p><p></p><p>¨\x0002 *\x0002\x0004Ñ</p><p>Ój¶YÍÖL\x001c#5YÅf½²Z­¬æÙñp´ß\x001f]9=Ù¹¹¹vyye·;ñøñýþ¨Ü\x0019MÍì÷\x0007WWW`5¯ÝÝ?¸½»sv~j·Ûa\x001cÛíõ­å\x0010ûû£ÝvçÑsÂ\x0018\x0007×7·>þø\x0013cÄ7ß|ãýåµÕzíùç¾úò3/=3¯&ÇexýþÒ_ÿö7ç'[ö\x000bï.¯½yóÆÓÇ=züØj»¶ôâOú^±4f=ØlN<zôÔýÃÞwßý`xðâÅ\x000bëõìíÛ·Öë­gO9=ßØïoõ8£~úÎÓ§\x0017^¼xîêê\x0012åx8V³ínëþ~ïêúÚj^Ù¬7ÎÏO­7³««K77×..ÎLÓd½^yôøÂáppïääÄ§}æo¿us}éå³\x000bÆ1\x000eBéDwë1\x001ez\x000cU-	$\x0012TH@\x0002\x0014T\x0001\x0002\x0000I$$\x0001I$$­ÇÑXª&	$\x0012T!@\x0004A¡Ð¤%$­{XF\x001b#ã0F£0	ª</p><p>¥@\x0004A\x0012\x0010\x0011@BB\x0012It\x0002"ènË²\x0018ÝV«õjm&U¥ªTM\x0006ójr~vêÉÓ'zyPè4\x0012@©\x0000I\x0004ID¤"ÚT³ª\x0002Ó4!I÷\x0004H¢ªÀz³±í¶aaY./¯¬×\x001bëõÆªGj2O\x0013UVU</p><p>B\x0002 ªRP\x0002\x0012\x0000</p><p> DIQU\x0000 EQ\x0014j*5ÓÓSUåÑãÇ\x001eîî\x001d\x000f\x0007Ä$¦Bî£û\x0007ËX\x001c{q¿?Ø®×æÕÚz½±,Gû½ãáà§òôÉ\x0013\x0017ç;ëÍÚ'ÝÜ\çÇg~üñÝæÔÙé¹§O\x001eûèÕ3«ÕÆíõÃáÁz5ûõo¾öæÍ[ï>\¹¸8óÑGÏívkË8øpyãòêÖ÷?¾vzzî¸´~~íÕ«WæÍÖ÷ß~çêòÒÿíÿþu¿¿÷Ý·ßùëßþf½^ûíoçÕ«\x0017J\\;;Ûùþû\x001f|ûÝ°\x001c\x0017gg§v»­_ÿúï¼~ýÖííµëxÿþ³ÓS§§çÒí¯ýÎ£G¢ì\x000f\x0007-û£å°xxxpssãüüÜqY¬×k¿üå×Þ¼yëêêÒÅÅ#O>vs}åpX,ËÊ7ß|ãÕ«6ÍzkzôÄgO]xëp\Ä\x0010DéDwëÑ:­,Æ8\x001a=t·</p><p>P$QfD\x0012UF)$\x0004 H\x0018c±\x001c÷½yµ\x0016\x0004I(\x0000*A)$$\x0008I$-iI$ma,Ã²\x000cc´1Z\x0007\x0015\x0011\x0014</p><p>E\x0006	U\x0000(\x000e@\x0004\x0001@B\x0012Ýíx<ê1L[Ï \x0000\x0000\x0000IDATódgS\x0015Uª</p><p> MU¶ÛÝÉÆþþ\x000cII"\x0001RJ\x0000\x00044¢j2M\x0013 Ti@\x0012Ý­»Á4M6µel\x001eú¾\x001d\x000eG\x001f>|°Þl¬Æ²¨*Ó\¦*©É4	%*LE"ÝT!\x0014B\x0005\x0002\x0008\x0015\x0010Pª</p><p>H\x0010</p><p></p><p>EHAÐ\x0000ìv;çggöÛ««+ÇãÁèAµª¸½»q}\x0013£c³;±Z¯í\x000f\x000bÊnYlv\x001b«yíôdëììÄÕÍ­³Ó3Ï<5Æb·ÝÚ¬:\x001cÖ­W\x001f¿TfÝ{éVááþÖ\x0017Ï\x001c\x000fùý¿úÍo~í·¿ýýqo·Ýº8?õþý[ggçno\x001e¼{÷Þ³'={þÌÕÕ×ïÞÙívNv[ç\x0017çÞ¾{ëòêÒ¸¿½SÓÚ»\x000fWÞ¾}ã_åpØ{ýú'××7Çáã?r{së§~2¯V>ÿìS}úãrôæÍ\x0007?ýôO>~äx<xúôªÙþü?=~t¡{¸88ÝîÜÝÞyxx°?<Ø\x001c7ªÊá¸w8ì}òñÇÞ¼~íoû«õz6Ft¿û»_¹¾þà/ý«ó\x000bíG\x0017\x0017¿øØzµöã\x000f\x0007Çã­$\x0012º\x0019K\x0011Ý-5\x001caY\x0016ÝÃÜE\x0015U\x0008U\x0000  T B$\x0001IqtØ?8.\x0007ÛDD´(\x0015</p><p>ªH)¡JR$ènÝ
ènÝmaYÚ²\x000cËh£[÷´$@ D£\x0005@$\x0001I@B\x0012I$$$1\x001c£1ª2M&I$\x0001DD\x0012=\x0016Y\x0016Ëá`Y\x0016\x0011Q\x0018\x0010h\x0000R</p><p>I$1F¤Ú4\x0015\x001aÀ4MV+$¨*Ý
æi¶Ýít·±\x000cûÞ»¿¿÷þÃ[«ÑÃ4f4Ó¤¦RUT\x0001\x0013%\x0008U  ¤J </p><p>\x0000\x0010*\x0002\x0000\x0015(\x0005 T \x0002ª2O³yl·[§ggýaïx88äh¿?º¿{°9Ù:=ÝZM3UËÁÕÍ"9qq~æüüÌ¹²Ù¸¾¹³XÍ+oÞ¼õôéS\x0017úùçmw\x001bO=v~¾ux8ÚlN©)\x001e=>S5ùîû\x001f|ùåç¾üüS«ÕÆ÷ßëa¿§6nï\x001eZÍo¿ùÖqYúðáÒÍ\\x001e?}êæöÆ\x001fÿøG_ùý~ïþpôâåK\x001f=vssëòò½~úÙ?þìêúÎËW/\\{x889ìv\x001bgg'nï?zîÉ£SËr°gÏ\x001eùðáÚÓ§O¼|ùÒýý\x001dáöþÞ<¯{õê7¯ß\x0018cñøÑ#÷÷·6ÛW\x001f}ì\x001fòÇ?þÉ¯ó\x001bÇÃ°,yÞXMm®Éfµ´wïÞ[¯Ö6ÛSÇã=BÈÒÆhc\x000cK\x000feXÆQ!\x001dI\x0014T¡\x0000-(</p><p>@$\x0010\x0011\x0000I\x0010Ä\x0018Ã2\x0016ÝCÒ¤É\x0004@BD\x0014\x0002Ñ $ºcÖ\x001dc\x000cÇeH\x0004!¤BI")\x0012I\x0010	\x0004@Ò$ÆhËqèÕ4«@D\x0012I#e\x001cÝ?Ü»½½õpo\x0019g\x0012(A'P¥ HQ)\x0004@\x0002´AÃ¤ªTª2My$\x0008H"	UV«Ùv»µ,îáx8º½¹³êft¡0Õ¬\x0014BQ(EA¨\x0012\x0004A@©T\x0001@$@V*TP(\x0008$T)¥`´i^9=¿qê°PÅ¶ZÚ¦Y­fÍìd»±?\x001c=<<èe2Ïe»ÛYF«*»ÝÖÕõ÷\x001f.=}òTÍ+w\x000f\x000fv§gV«µívëÃû\x000fn®o|ñÅNO¶¶'[\x001fÞ¿w{së/>÷×¿}ã?þ§ÿêé£'>þä#òão½{wëâÑW¯úëÿêîîÁ«W¯¬V³ãXÌëífãóO>ñþÃ¥7\x001f.mv'æÕìßÿî\x001f|ýÕWt´Õ¼rÿppswt\7oß\x001acxþì)\x0016ÿöoÿêìôÂ¿ÿÝ?Úßßûÿüÿ¶§§~~óÖíÍ½Ó\x0013õ¨©ÜßÝéi}þé\x0017¦õjòèâÂýÃ?ÿéÏ¦yíùWÞ¼yíááÁ4MÞ½g\x001cÛgOãÑÏ?ÿd¤íNv~õõ/^¦,2å¸w8ì\x001d\x000eGe8.!M ¢\x0000\x0005\x0005­L(\x0004%	\x0000\x0000J\x0015Ý%ÕÔYL\x0010(©"\x0001I\x0010\x0014! EÑ1:ºca\x0019Ã\x0018QT&"AP¢\x000b\x0000@@\x0012\x0004\x0004$nc\x000cÃÐ©fSJÖié\x0018ãaqÿppwX¨Ô$&j\x0002@\x0012\x0014\x0000\x0010¢´defUTQU¦i2ÏA$$1ºUbRV«Ýn§Ç0º\x001da5ME\x0018cQ¢j\x0000¥Dª\x0012\x0001\x0010!\x0005*B\x0008 \x0011*PU\x0000*\x0000¥\x0010\x0005$\x0014nªtJª@UWkëy¦8.CØm¶NÏNl\x001d\x000fëë{¬ÌóÊjÞ:\x001cëë;ëõÊjµ²Ûnt·ÕjlçrqqâôôÄrÜº½¹õáÃ{gg'¶õzí§~¶Ýî<yòÄ»wñv¼ñôÙ¯ñ¥»Û[\x000fw\x0007\x001f½xa½Z©i¶=Ù1MºÕ<Ó±Z­¬æÓÅ×ol6\x001bgg§ÃâáþÞv³öÑG/¸¹½÷öí¥~üÉógO<~|áÝ»7^¿ùÑógÏ|öù§öû;5óGÞ_^»¹;XÆÑýý­×¯_{öìÓ³3U¬×kO>s}}åôlk·Ûº¼ºòáÃÛÛ{U¯¾úÊj5ù×ýO>ùØ'OÍÛÉãÇl·;ÿé?ÿ\x0017¿ÿßûò«/|üê#çç\x0017ºÃÃ\x0015adXÆÑá¸·ßï±8,C*¥B\x0001 @D)\x0014 \x0010Q@¨") *jÐ\x001dÝ­¦¢\x0000!\x0010:A$ÑÝ\x0012\x0008AH"Ý1,cXa\x0019-
%P@\x0012 H\x0007$$@\x0012\x0000	A\x0012IK·e\x0019öËÑè\x0006$Bî¶?,no\x000f\x000eÇr~va6*³J)QU¤T ¨*\x0012ªJÒ\x0012NKç	¥ªLÓ$ÂD\x0012¨*ó<Ûl6Æh£[ò`5M\x0013¢»\x0019LÓ\x0000U% $\x0001B @Q\x0000P\x0010*IT\x0015!¢ A$¨¢</p><p>Dt`1t§²Ýl<:d³ÚfNOvÒñæîûû½yµ¶Úì¬×[IyØ\x001fÕ4Y­ãd·urzf·Ý¹½½u²;±^­Ìgg.¯.­Wk_ýëë[ïÞ½S5Ùï®®®]]ï¿üüÇ¿÷?üÁ¿üÛ\x001f}õÕçþþïåÇ\x001f~¦ÛÏ?½6:Öû{SØ¬6\x001e=ºðþý{Â4ÍÆ²xsyéîöÔãGüúï¾¦\x0017ÝGçç;Ï>òèbg¿ßøôÓOüê¿ðîí[ûë7ÞüüÖ<Í~úù\x0007Ï/|ýË¯mN¶þëû?{öô7?ûäWNON¼ÿÞÍÍ
&W×\x001f<yòØ³gÏ<zôØ\x0018l6;'''^¾|æñ£sËqxóó[/_¾ôìù\x0013¯ß½öÙg_øòË¯üíoßÐ¡e,îï\x001fô2f\x0019m\x0019­»-c8\x001e\x000eÇ!¢RJI\x0001 A¡\x0004U\x0005\x0014RJD@BR\x0008	¡Ó\x0008\x001a\x0001\x0011BP PîD\x0012IH¢»1\x001eÆX,Ëâ¸\x000c="\x0002\x0012 !H\x0002¤%1ÆÐÝHH\x0010H¢ÅÒÃápp\x001cC§EF$\x0011P:q8.î÷{ÝÈ¬BQ¡\x0014A\x0008$\x0004\x0005"M`"\x0010mè¦ªP¦©LÓ\x0004çY\x0012I\x0004U¬V+»ÝVÒÆ\x0018VÓT¨"HH \x0014\x0002$ª\x0010\x0004EU©B"$\x0000(\x0000\x0000D)\x00101)Ut¨Bh­j\x0002AÒJI\x001atªÙùù³³3Éb£ËK777åÈ\x0014ÉÎ²\x001c¬×k«ÕZUé\x0011U%=ÜÝÝ*è¸¾ºÑ\x0019áþno»=1Ï+ÆàþáÞá8T­ÜÝÝeðúÍ{··÷~÷ÛpñèÜ¿þÛ\x001f\x001c\x000eÃ¼ZÛï\x000fv»­yµr~~fY\x0016·wwÎNOM\x0013¿ûÝ?ª*¯_¿öí7ßøßþC[¯'O\x001e?òñÇ\x001fkrq~áÍwþõß~ïòò­çOûèÕGeÑÚýÃÑzuðý÷?xûáÍfíÕËW^½zåÑãs«ÕZw¦Ér<úþûï¬V\x001b¿|æùóW¾ûî\x001bççç¶Ûµª2Æb½ÙøÝoçÿù¿û/ÿõ¿xþü©¯ñ¥ínëË¯¾òÙÿ/þüçÿéþ£O>þÔñ¸qD7éÂiEµd¥»\x0000A\x0008(\x0002T\x0001	\x0000)(	D\x0005"Nô\x0018Ò-i\x0014\x0000	\x0008\x0012ª</p><p>\x0004-NHZ÷0zXÆ0Æ0F[z1ºEQ\x0013UR%¢ª\x0004\x0012\x0004\x0004t7Z\x0012I$DwKGº-c8\x001c\x000eÇ£î\x0016\x0011!-	@DQeôððpO·Ç§³d H"\x0000$\x0001\x0002\x0001I\x0001H îÄ<OÂJ\x0015Ó4énPUj$MSXÏ+½ÙZ¶G«yÑª¨\x0010</p><p>J\x0014\x0010\x0000\x0012¦©\x0004I*5M(\x0000B\x0015¨* \x0010ª bRU\x0012TL"iQ(D\x0015U%	U¦i2Õ,=\x0019ËÑ\x0018­Ív6Me3OªbôÑÉfëädçþþÞñx\x0000«ÕÊápPÝnîî\x001dÆ0Æbf77·º\x001b\__º»¿·;9ñp8zØ\x001flÖkI\x001c\x000e\x0007w5éL^¼zî/ß|ëæö½UÊv·5Mûû;'»­Ý'Ï¾ôÃ?øé§\x001føÍ¯íììÔñpôîÃ\x0007§'[ÃÞj5;=;³ZÏ<}âòêÊÝíÁj¾qq\x0011'';\x001f>\zñâõzíOþFMåË/>÷w¿ü¥ªÉz3Ùï÷þö·¿:;;óâÅ\x000bß|û½ý~ïúêÚz5ûùç×~øá\x0007ËX<öÌj\x001cG/_~äï~ý+¦øöûo½|ñÜG\x001fÅÍÍµ\x0017Ï©ßÿËïýë¿þÁ×_}é£WOiºCMæye³9³^X­Ntè\x001eR³\x0002\x0008\x0014$\x0008J\x0015A\x0012 \x0005HB"¨*Ó4a$R\x0002\x0012ÐiIëBº¥Û\x0018maÅ2e\x001cõ²\x0018=¤Z\x0015Ó4)\x0014\x0004\x0000</p><p>@\x0012	I¡%D\x0012ItZ'z\x000cËáèx8J·</p><p>I(¦*IiÑ¡LÖ«ÍzåááÞr¸7Æh1\x0001\x0005\x0005$ \x0001ª\x0000\x0002ªÊ4Ñ\x001d@K\x0018\x001dªT·ªRUæy\x0004¤È\x0008"¡ªlVkc·³ª¤J¦IªRJU)%B\x0000</p><p>H4:¨\x0002UB\x0004\x0005(\x0000\x0010AU¨\x0012H\x0008\x0000@\x0012TIÐÂ$	SÄdªÉf½õèâNYß­\x001dö{5\x0011\x0014z´ãñh¿?º¼¼´,§O¦Iõvc3Íå`'áööÆv»Ó¡Ó\x000eÇÅÃþÁ·^½òw¿úÊË\x0017OÝ\ß{ÿö­1\x000e^½xéx»Û;ÃA÷ââìÔùù¹\x000bÇ¥%³Õ¼ñöí;ÿýáUMTélw'Vëµ«ëk··7ÎÎO\<ºðpôæÍÏ^¾zæììÂ\x000fwî\x001fö\x001e?~jô°×Ç£ï¾ýÆÓ§Ï\ßÜxöìÇ/T­l6;§§§q,>|xï\x0017¿øï¿ÿÞ·ß~ëüìÜf½ñäÉcÛÝÆ<W¯^y÷î½õjãÑ£G\x001e\x001eöîîî<}úÜÿãÿùÿò\x001fþßÿÁßþúíÊÉne£ÑGa½ÚJHJènI\x0010I)\x0013$ </p><p>HH\x0004\x0014</p><p>\x0000À4M¦y6YU¡$%	 	@Ö\x0010Jt"1e\x000c£[aY\x0016Çå¨{QZU© @D\x0012	IKH\x0002HH"¤%-$z´ýáèáá`t$\x0000I$DÕjíüôÜÙé±ìEt`B©¢</p><p>M'`J\x0012\x0000\x0000\x0000ÓT"(It1\x0008ó<£T1M\x0013H¢;H¢¦²Ýl­¦i\x0010¥ªTAÐJ</p><p>(\x0008A¡$H¨*U\x0008\x0004M\x0015U(	ªHLª\x0014(@\x0015\x0005H"Bè\x001e(5ONÎNMëÝÉÎû÷\x001fì\x001f\x001eìv;gg\x0017¶Û­ûû\x0007÷÷÷¦ir8\x001c¼~ý\x0006åüüÔÉÉ)EU9\x001c\x000eöÛÛ;£c·ÝØn¶ÎÏ¶¦iòã?ùùõ\x001bO\x001ezùâÃþ'ùëß\|¸ðéÇ\x001fûìýüæë«+½,6ëµ'O\x001e9Ùí¼ÿpé«/>óóÏk÷\x000f÷®nïì\x001f\x001e¬æµÃ±½}÷ÁãGg^¿yg½Y\x001b£Ú?<Øï\x0017W×îï\x001f<~ôÈjÅénç°?:9=±Ù¬ív[#\x001cÓ\x0007ó¼quu-¹·]o¬×³û\x0007¥¬7kÛÍÆ¿ÿÝ¿szvJy}x÷\x0016³gOû§üýáÖ\x001fÿøG¯^~ìâìLª}õÅWÖÿëÿê?ý§ÿèa´Z±,åx´,CBjÂ¤G$Dé H\x0002\x0000¤@\x0012&$\x0002¨\x0000AÒ j*©\x0016\x0011­ªb*Ñ(R\x00122HBhÑî´\x001em,íx\ì÷GûýbV\x0013sAIJ\x0007$è$F$A\x0010\x0004maÿð`x4\x0015\x0000	Ý$!M3O³Ó\x0013Ï<vwmfT0©\x0014\x0015ó<IRU\x0000\x0000 2Õ,NKZ[\x0010PU(I@ÕdÂ\x0014It7¦Éª¦É¤iºK)ª\x0000\x0011Ð( E¥\x0014æi&
(\x0000$QBÆ\x000c</p><p>$%¡</p><p>\x0008(\x0005($\x0001Q\x001a´R ©©ir²=1¯Ö¦ir{sCb½Z©©\ßÜXG''§»»{77×®®v>yììì*\x000f\x000f\x000fjí÷GIY­ÖînïÍ>~õÊÍõ?ýéO\x001e]{üèÂ\x0008¦rs{ëÃÕ\x0013O\x001e?r~vêýÛ7¦âþîÎX§O\x001eùùõkï/ß[­6¶«µªÉTX<ìïÕzmg÷÷{Ïw;¯^½4F[¯ËÍÍ­Ç{Ï?õÃ?yóö­ôd½ÚØlvÎÏ/ì\x001fîmÖk÷û{\x001f.¯½yýÖíí­/yüäûû½ãqqssC\x000f»ÍÆn»sssãd·#åÃ\x000f½X{þü\x000f\x001fâ¿}k\x001cÛÅ¯ÿÎÍå¥÷g?ûüËOíÿÎíõ{ûkËeÄr\x001c\x001eö\x000fj^YzènéèFE2IJ	U !¨\x0006\x0008H\x001a$4ZP:­³z¦&A\x0005hTè\x0004!\x0016KÇ\x0018­a,ÃqYì÷Ã~?tS5¦¢HP\x0015I\x0010D\x0012@$$$Dw$´¤u·eY<\x001c\x000eÇ\x0005¤H`B\x0013\x0012º#$Vëó³SÕGsM U\x0015JTE´R¤P\x0000\x0008)Ý!$-Mw¨\x0006ºÔ4¡T\x0001Ue&Zu©*c\x000cÄªæÙ\x0004\x0019R¤0ME¤$D¡¨PÁDURJ)\x0005\x0000J	</p><p>ªh</p><p>ª @U\x0001EP\x0000\x0001 ª@A\x0001 Hhe</p><p>ª¬çÇ\x0017ìN<Üßx¸¿\x000cÓj¢¸¿{po\x0019q·?ÈåÑqzvb^­\x0008\x0017\x0017g\x000eÇÅýþàôü«ëKW×W<~bYâêæF^½òë_}íç×¯]^^¹8ØlVÎÏN½úøc}\¼yûÎf½öáröúí[\x0015fqÜï=Üï=äéóg./?8;=ññ'\x001f\x0019Ëâ°ß{xØÛl6¾üâs¯=õîÝ;×××6»\x0013ûæ{=\x0002ÎÎO¨òãO?»»½5Ï\x0017/^¹¾¾q}sm»ÝxôøÂ\x0017/¼~ýÚÃÃW/_zýúgßÿðe´ûû;ÃÁ¼½»|g{²³Ýn}ýõ/¥'ùëÿÄ'Ïýðã\x001bæ¤­V\x001bvgÖSËòÖaÙ»¿¿³t»8?q<>´$¤(¢1	</p><p>\x0014¨j\x0000A@\x0010I$!¥CÍÓÊT³¤t·®É¤QdF\x0011:´$H¢\x001e1ºu¢»\x001d\x000fÃáà¸,R5S$\x0004\x0000H\x0002(´$î´$ºcXvØ/Ë JIB\x0012\x0011Ý­Ó(\x0011ª¬æÙj5SÑiªT1¨I\x0012)ªL\x0000\x0000H"\x001aÑÝ"1"ÓBªÉ4M¦i2UÉT®(\x0003mtÊ¤¦É4ÍjTRJ©*\x0005J)\x0005)RUf¥\x0000* ª\x0000¥\x0014H2)\x0013J\x0002T\x0015\x0005\x0004\x0010Dî$</p><p>\x0005PTBÑ\x0018\x001dILÓl·Û:?;7M1\x0016ÛÍÆf³v8<¸¹¹vusã8\x0016K·±´»û\x0007·wwªÊ¼:¿8£Ê¼^[¯·F\x000fÛÝÆ£3§§§\x001eö\x0007·7×>ÿìS\x001f½|a¿ß{Ø?xx¸÷öÝ;ózíÕ':?¿ÐÝîï÷¶S\x001f=ñèüÜÉvãã_©³ÓßýÓ?8=;qçéÓ'¾øü3»Ý?ÿå¯^ÿø£õTÎNOÜÜÜù·?üÙÕõ­ÃÑõí­~~­\x0013\x0017\x0017,KçµíÉ©$NNv^<j³YçÉÅÅ#ÓTe±Ýî,ÝÞ¼yk»ÙøùÍ\x001búËmv;IÓíââÜßÿÃ¯]\<ò_þÛ?ûæÛ¿yxxðæÍ\x001bÐ)1{ôø©Õjíx<Úïï½ÿðÎû\x000fï,ãHZ% $¢\x0001\x0000D\x0012IH\x0008IDtZÐ\x0015\x0014UÊ¤L\x0012º£\x0013	BDÒ:D\x0012ÝÑÝÒCwë\x0011c\x000cË²8\x001c\x000eÇ£±\x000cH"Ý´$\x0000H"!!	"$HZ\x0012I$1º\x001d\x0007\x000f\x000f\x000fÆ\x0018ªÊ4Mj*AD§uZ\x00124iÑ¢u·îF@BÕ¤jRUªÊ4M¦iRUªJU©*R\x0000 </p><p>H3F\x001bc\x0018c\x0018c\x0018c\x0018cèJ©U¡è\x001e¦R¤¨É4M¦©TA$PJ)RPQ\x0000*@JU©*\x0014*\x0000$P$\x0004H$A$\x0000Q¢BI)P ¢\x0013&¬V+»\x0013»\x0013ójvØ\x001fÜßß[Æ¢¦RÓ¤ª\x0004ÝÑ#t\x001bË°\x001c\x000fno®­Ö³\x0017/Ûm·eñüùs/_¾tuuåúúÊ\x0017_~á«/?7cÂX»Û;ój¶Ýnív[év{}íìôÔ£ÇO<ñÜ³çO\^¾ñý÷ßº¿¿³,Ã·ß|ç°?zòä±íÖv½ñã?\x001bá¸\x000cÇ\x0011?þô³³ó3ójåx<:\x001e\x000eîïî¬×³y\x0005ýÞj=yüÈ«Ïîì÷\x0007Ë2ìv;ÓT\x001e?~L×ïÞZm·?îå«WÖ«û\x0007WW\x001f|øðÎÉéÆßÿýo<~üÄ?ý`½^9;=3£ûû{cÄj½óòå'VóÖ²,\x000e\x000f\x000f\x000e½î¦ \x0008\x0000"\x0012(I$D\x0012D:ÒQAÂî6ÆÐÝ\x0012</p><p>\x0010\x0011$¤£»u·înIK"$º£{\x0018£ÑÆr°e9\x001a½F$@\x0010I$Ñ\x001dIK"îH"îDwëîv8\x001eÜï\x001feQ¡ª\x0014$NtG\x0012\x0011It\x000fÝ-\x0004	H\x001a&$º[wK"îDwK"\x0001\x0000 ;Æhc\x000cË21\x001e:\x0000Hè1L¥*©¨"\x0000¢*¦¢\x0012(\x0011Ñ	PT\x0015¨*\x0000UB$¨*D\x0016DU&\x0003­*ªJM¡ZU(ª¢4Ú$ª©PU\x0014ÑÑbWv»3Ûíª2Mõze³YÙm×ÎNOØnÖyTØ?ìéa»^Ñm</p><p>\x0019Ãñp4M³á«/>óäÉ\x0013ÿüþ\x000f¯ß¼ñêå3¿øâ3}òÝfçÍë7Þ¼ycµm7kUÛ®Úv³r\\x00165¯\x001dGó4Ûï\x000f®®o-K»ººõúõ[=â°ß{õò¥ÝéË;]³Û{Iì¶['ÛÓÝÖßýêk}úåpðøÑ¹ýÃ½ï¿ûÆ§}úÉÇ>ýø#\x0017çg=|óÝw¶Û­gÏzüøO>úÈ³gÏ}¸¼r{sçt{JøpùÁ´}xÿÞ?ÿ·ÿ.øû¿ÿ{ÇÃð?~ÿ/\x000e\x000f\x000fÃÑ\x000f?|ï»ï¿ó°ß{ôøÏ>ýÊjÞXD\x0004A\x0010\x0012I\x0010% îH"$\x0012:&!\x001dÉ^ôX^$Ê$¡C\x0012Ý-iIKZÒ:C[tZ\x0012c´1Ñí8å¸XÅèFjVU</p><p>Ð\x001dI$´¤u\x000fÝCÒºÛ\x0018Ñ\x001dIt·tënciãp8\x001cu£&eBè´înI$´$H\x0007P(A\x000eABDwënIt·1î6ÆDw\x0000\x0005ª</p><p>Ñ\x001dÝm¡{XÆbYÆ8ê\x001e !Í\x0018m\x0005UE(T\x0014PU$"\x0008U@Ñ\x0005\x0004¤\x0000\x0000\x0002\x0000\x0008¨*\x0000)\x0002\x0014\x0000@A£@ **\x0004PLE\x0000 \x0010J¦Ùv»óäé\x0013éáþþÎõÍRVëÓy%\x0003Ìóäx<Øï\x000fVëµívcµõ\x0018ºãììÔáp íã?vs{ëûï¾wq~æÙ§>{¡»\x001d~ØÛ?<\x000c}<8Û­<¹xá°ÜYzåÑãÇºÛÇ\x001f}ªëëk»S\x001fúË«KgïNHl·\x001b»G={îîþÞýýõjåòÃ\x0007Ï=õÿð÷?{l9\x001eúê«¯üí¿ùöÛo¥\x0017=\x0016?þø³ós'Û\x0013ó¼r<.öûÓÓS\x001f}üÊW/½yóÖ_þügó4{õê¥ã8¸¾¹ñâù3oÞ¼7¯ï|ýõ/¬×kÿý¿ÿ7ÿá?üoÎ/ÎnUåêúÚvZùä£Ïüã?üÎåÕµãþ`E§\x0005¥H\x0004DP"i´\x0004F)$HZ÷´$¤¤1\x0015&D\x0004$AH¤c6F\x001bc\x0018cq<\x000eÃp8\x000c£Y×dfU\x0013 PE\x0012I$Dwën		ÝÑÝF·t\x001bcØ?\x001c<<\x001ct©f5Í(ÝÑÝ2¢;z´ÑÑÝÒm6:Æ\x0004H\x0008@\x0015\x0002\x0012 ª\x0000$\x0004PhI\x0010U%	"î\x0006Fi\x0008It·²J¢&jP*\x0014)\x0000\x0011</p><p>JB\x0002\x0011U\x0000\x0000\x0010\x0001	\x0008\x0001\x0013i(4Ú4M\x0012@</p><p>¢\x001a¡HJ¡B@	ÕjíÉö±Séáõë·.¯nì\x0007m8Ùn¬æJyØïÝ=<Ø?\x001cÔá`ïìNì¶[§§;I»¸¹¾vssëâìÜ<OÞ½û`³ÙyñròâÅ3ñ¹Û»\x001b?þô¹</p><p>Ý}{tva³^ûë_ÿæìüÄíí½o¾ùÎG\x001f½ôégº¿»óý\x000f?Høå×_{ÿö­ýÃ½Ñ§Ùj½6W|üñ+c9úæÛo}öÙçÞ½çÝ»·ÎN¶Nw\x001bÉâÃÕÕzçÙÓ§>ÿäcïÞ¿óã?ùäO\x001e?}n=Ï®®n\]ßXgO^\x0018Çá¸,>ùô\x0013û½ÝÊï~û\x001bg§'þ÷ÿø¸¹}ðÉ§\x001f;;;u¸¿ssuít³ñ÷÷\x001b2|÷ý_\x001d\x000e\x0007K·NT¨*\x0012	</p><p>ZÒ"\x0002!	)(\x0012I$$tÇ²,F\x000fë ´J\x0016HI"!!)II¢»u\x000fc,ãâxlÇc,£u7¡î\x0018½è\x001eª&Ð\x001dI$D\x0012ÝÑ$H¢\x0013#1\x0012¶£û{w÷÷ªLJB:Ò¥3IJD:º£G\x001bÝF·Ñ-Ý¤\x0002\x0008Uª&I@\x0012Ó4©*ÝÑÝ(\x0004\x0005(\x0014Z\x0012D2IÒ£%1º%-a½ÞX\x001dÍz£LR\x0011\x0008ªR"\x0010</p><p>\x0001PÊ¤\x0014U¦©\x0000\x0000U\x0013A\x0004TR(%\x0002\x0011((\x0012 P\x0002I¨\x0010(\x0005)D\x0001$`ªÉjztqæÑù¹×oß{÷áÃa¯DÅqtyuíæî\x001e\x0011±Ø®ï¼|ñÜÉn§'\x001fKøþ»ï<{öÜ\x0017_~é\x001f~p8\x001cüðã~~ýÚçÏ¬æÙ\³\x0012W{«õÎjsâîîÞþò«Ë[ÛËµËËk«ÕÚz³%åääTÂË+û±ØlýßÿÞÍíÞ4Ïj\x0014'g'½ó³\x0013÷w¿t}}ëúêÒTl·[çg§Æh·w\x000föûï¾ÿÖåå'O\x001eæÙå\x000fv»­ôðèÑ_|õÿúÏÿÃ_þúWgÿô÷~ý´Û­½{ûÞþaïêÃ\x0007«íÊ«W/ýûÿïüþ÷¿÷üçÿêé'~õÕ\x001e»¿¹2\x0019þé7¿ñâÙc5µ\x000c"R
@\x0015H\x0002t@w\x0010j"!HènÆ\x0018z´1ZwënUN ¥¡$\x0001	I$ÑÝÆ\x0018ãÑ²\x001c\x001d£ãñè°,Ñº[\x0015</p><p>îènÓÔ(ItG\x0012ÝÑÝº[ÖÝÆhc´ÎÐÝÒ1Fì÷G7·wîï÷\x0004L\x0015´îaÖ\x001déè´îè\x0011c´î6ºn#1\x0003\x0014¥(ª¨¤&	ÓDw«*DU@wK"	\x0000H\x0000¨*c\x000cc´ÑÃèÄj^W³Õ~k&5­D©"¤ÁT\x0013F\x0012\x0000U¥PU(\x0000$ª&s­Ô4\x0019iIT* </p><p>¨ (¡\x0000\x0002\x0014ªª\x0002IT\x0001BU)\x000e&(I@\x0000%\x0008b=O>yd»Ý8?ÛúpuãêêÚÍõµ««\x001bûýâþa¯SRB:nïî­V³d8995Mi5kíêêÊÃþàþîÎýýx÷öõ4«âç×ïmOÏ=Þn¼¿|ãîîÎîdggëÍÖ4Mnîîy÷Îr88;=±^­üÛ¿þ«_ýê\x0017ÎÎ/¼}eY\x0016gg§ÞßÞºzÇv]¾øü3I;\x001eî­VÝnç°?¸»Û»¼ºru}ãúöÁf½vwwëñGvwc5»»[\x000fûÝÉ¹Gg~~ýßÿË¿8=ÙùÅ×_¹¾¹ñîõ\x001b»ÝÚa98?{ìÕËWö_úpuãü³í¼ò«/?3MåþæÚtvæ\x001f\x0019=¬j"\x0011\x0014(t\x0007@\x0012\x0010\x0011AKBHÑÑm&!î¨\x001a\x0008!!	¤11,ËÑ\x0018Ã²,öûýýáà¸\x000cÝ¡Ê4ªR</p><p>¤@wt·¤uGwënÝm¡»u\x000fÝmôÐ\x001dcû£«Û{\x000fERjÔT$z´îaYe\x000cÝ­»ÑmtëîÖÝº[*ª"ZU$ª\x0000¦	$\x0001U%i*ÓTÆ\x0008H¢»%\x0001Ó4çYwK8.ãrÔÝªÊ4MæLV·7¦i¶Þç\x0015HèP\x0005B\x0008PUªJU$\x0010\x0001(ªJ)ójefÉ¢{ ª</p><p>¨HP¨B\x0000@U\x0001\x0001ª&\x0000*¥"\x0004  \x00105\x0015\x0010 Ý¤­W+ÎOm×³y^¹¼¼òþòÊÕÕ-5kã\x0018VÓd³Ýærwÿ b³^Y¯7ªÊÅÅ¹i\ß^#6Û\x0013O>ñþý\x0007ïß¿×«Éf³±=ÝY²8\x001c\x000f>úèÕzöp·¸¹¹s<\x000e'§kÛÍÎõõ«KóG¯¼xþÜ~ÿàúòÊ<M~õõ/ÜßÝ¹½½6\x0017'»i­V+§§§Öë\x001f~íç^{üè±«ë[je³=uu}mýxíâÑý^\x0012éaµºSÅÕõ­/¿:õ«¯a9\x001cüôÓOþ÷ÿø¼ÿðÁÅù¹Û»;oÞ¼ñÕW_yÿþG\x0017>ÿìSË1N·'ÊäîîN&mo®Ùj³&eêIÕ¤\x0005($$\x0000F$\x0004t·¤%-)U \x0013¥¥\x0001\x0010\x0012H¨¢»u·eY,Ë°ô°ôpXö£Ãáh9\x000eRJU©©T\x0015$HZw$ÑÝº[wënÝ­»õX¤ÛXÚñ8ÜßïÝÞÞ[FSER:md\x0018cè\x001eF·îÖ\x001d£cYå¸\x0018cèîè\x0000\x0012*Ò¡jR)D\x0004@UI¢ªLÓd'I\x0011DwK¢ªÌól&PUtt·iHÀêæúilw§¦i6ÂèÄªR))</p><p>L\x0014U$A)\x0005HB\x0001i*U%)I¨*</p><p>d\x0002P(\x0012*\x0000)ª\x0010\x0012 </p><p>¨\x0002\x0004	U$:t·î¡R¦í¶kg';§§'ÎÏÏ\x001d\x000eÃýÃbfe¶Z­$íæöÖÃþÁãG\x0017NO\x0016«y6Ï³ãþ`»Ýúø£\x000eËËkÇãÑ<Ýnk¨*_|ñ¹«÷~þùµW¯^ùô½{wíæöVMT1±,ÖëÙT\__¢l6çÞ¾}çx<úßüÆùÅ/¼}÷Þj½²ØûÃ\x001fÿäììÌa¿·Ý:.m^ol6\x001bW×ÖëiýüúÏ>ýÄz³õþÝ[ëõÚ«?%íÉÓg.\x001e]ï\x001eüöþÑÉvç§ò?üÉW_}áóO?v<<¸¹¹õäñcw7·nïß¦ø§ßþ½Ó3½ðîõ\x000fj,ÆXÜßßÛôp\\x000e$NOOÕ<I\x0001DÒZ\x0004$\x0001\x0002¡\x0003$^±\x000cÝ-\x0008º£*P!%!\x0004HÚ\x0018eY1,cXÃrX\x001c\x000eGûÃÑqY¤£ªLUèn¡zB$DÒº#î6Æ0Æ0ºõ\x0018º±\x000cciãÑÝÝ½»Û{cÄTLU2\x0018c\x0018cXÆ°,C\x00181bXá¸\x000c£[\x0012DkS\x0002*$ÖH ª</p><p>$\x0001U¥ªP(É0Æ\x0004TªRU\x0000ª¨*U\x0005F·ZÕíý
f¬LÓd½9D(R\x0014RE)U\x0005\x0008\x0002H"iB¢*Ô\x0004Ò$@U!\x0012(\x0010E¡¨* ¢B\x0001ªB(DI\x0018Ý:-\x0019*1U9Ù­}úÑK\x0017gg~úùï¾ÿÉÍí½©b£ý½it·îÉá¸¸¼¼¶Ý¬=º¸°½Ø:\x001e\x000enontâápïðzoÊÇ\x0017æyãÃåµýa¯v¿w}yc·[«jÿøO¿ñ?þÙõõ­Õjo½^{õâ§O\x001f»üpåÝû\x000frñø©?üá~~ûÆ´zéòúJw;\x001c\x000e2âêúVº½x¹òÙç¹ºº2Ï³õzöæí\x001bõÆë7·¾ûþGgg'6µ×o^Û®W>ûôS¸½¹qrræë¯¿vrzâ\x001fòîÝ\x0007_|þ©¯¾úÚ~¿÷öÝ;ÛÍÖÝýýñàôìÜ\x0017êö=5­tMÑ\x000eÇ;IæYFd°9ÙV+Ó\TD$Q!	H  \x0013é\x00061ba\x0019GU\x0013!î\x0006</p><p>&B\x0012I$t·eiË\x0018c±,mYÃaq<.e1:nIK"iÝ-îÖî6ÆÐÝºÛèÖ\x001d£[6Æ0Æâpxp{wëp8¨DM&U¥»¥\x0011cD6Æ0R±8\x001e\x000fËb,­; ¤¥¢´@G'b\x0012\x0000$\x0004\x0000TiLS#H\x0002 îÖ\x001d¥LÓdg\x0010Ñ£\x001dûhµ,ÃõÝ¥TæÙYw4Ó¨Ð \x0012\x0000\x0000(\x0000	U­5$\x0011-)@)E\x0001UP"JPR\x0000APQ	\x0005\x0008\x0005H¢ª\x0000E\x0000ªBë´N\x001bJ\x000b]V«É³§<¾8w²ÝÙ?ÜÙï\x001fTm,£±\x0018y^9;;³^¯<Ü?XGÝnëñãG\x001eî÷îï\x001fìN]ßÜ«P\x000eÑÃIL6Ûe´wï>øðá_?ºð\x000fÿwþçþâû\x001f~ôìÙ3÷û\x001fòpÿà°,¾ÿñG¯^¼òÛßþ\x001e\x00075Í®.¯}¸¼ôâùs¯^¾ôìé\x0013\x001f>|p\\x0016'';'';W××\x000eËÁÕÕµ¯^úú¿ðÝwß»ûùÆ/õµGÎ}ÿí÷æirrr&¹TÓÊýÝÓós¿ûÝoùÃ¿þ¿üõ\x001bÇãÑj5\x001bËâýòAÂ4Ï¶Û£Õ<9=ÛQ<<Üª*-ËÑv\x001c\x000fG·×·\x000eËÑ´ZÙn­7³$ 	@\x0002º#1±\x001cÍ«ÙÈ0e*\x0008!\x001d$ ÑÃq,Ëb9\x000eËqq8\x001cíÃq±,C2U!º1ÖZºu¢Gë´îÖc1Æ02t·1ÚXÚ\x0018Ã²,\x000eÅíí[ã¢&jÒ\x001dË\x0018ËÁ²\x000cË2¤£ãñh<:\x001e\x000fåhôÐ\x001dIt\x001aT	\x0008	Õ:Q¨\x0002(I$QUªJU\x0001\x0008\x0006IénI¤#i¬æÄ2\x0016c\x000c°¢±¸½»²^o­Wk½\x001cIT J©*\x0015\x0014I\x0001"¢2¡T\x0015\x0000è\x0010M\x000f*PP\x0000\x0014"ª</p><p>\x0005*@\x0012R\x0002¢ \x0008*\x0014R $ª</p><p>$­¦¨NtLU¦Õl»mÖåätcµ>1<ì÷\x001e\x000e\x0007\x0012S±'c=ìöË¥i¢¦ÙTeYÕvgfÛÝVwï?x÷þ=ÓìöîÎf½²WvÛÇ\x001f¹¹¾ñøÑ_|ù»û{÷÷\x000f¦©Ü\_[£ýÍzãæêÊ£ó3K&ïß_Ê´Ö)0ÆÑn·Är<Ú®·\x001eö{=¢\x0007»Ý[ÿð_8ì\x000fþø?¸½½ñé'¯|ù÷\x001f>Xm6öû>\x001e'áÓ?r{ãêîÚÿù/ÿj³^û÷¿ý­ýÞ_þò\x0017O=õôÙS××W¦°ZÏîno«\x001cGÓ\6«±\x001cÕ¡ÔhI«igZM \x0013Ðª\x0012!$DwtGwëBJ¥ub\x0016I\x000bH\x0014N,#%ãp<.ÇÅÃa±?,Ç¶,­»\x0011¥\x0014FÚèXFÌ\x001a­;:­Ç0º-c\x0018cXF\x001bc\x0018Ë0Æ0Æâ¸,\x001e\x000eG·÷\x000fnïî\x001d¦¨i*SM\x0012ËÑá¸·ß\x001feDLFÇr\\x001cGËr4º\x001díplëu¤btSÑ¡ª%\x0004TBJ\x0002\x0000$ÑÝ L&1$\x0000tt·¤­jé2G··\x001flÖkcP)\x0014 PªH¢ª(\x0008\x0008$\x0004L\x0004\x0015$(\x0000¡PU@Q</p><p>\x0002\x0011	ªT\x0015¨\x0002T@¥</p><p> P ª\x0000($ÒÑ\x0004\x0015\x0012	=e9Z­Ê³'ÌÓìáaïîþÁqY\x0014æ©L«É²\x001fÆ±­V³«ë;\x0017çg¦õìxØ\x001bËb,+77wnïîì\x000fÃñÁzµ²Ýl\\yõâ§Oúþû\x001f¼{÷Þ'~ê£\x0017ÏÝÝÝW\x001b··wF\x001feÁª,K{ÿþ½³Ó\x0013ïß}ððpðâÕ+}ò±wïÞøë7ßº¹¹\x001e:íÝ»7ÇÅn·óå»¿»³Ûl|ñé§.?\º¹¹óáÃ¥O>zåäôDº­æÙ~\x0019Ç½Ï>ûØ~¿g\x001a½xæáÇ£iÞxûæ\x001f~úÙãGl·;·7·þüç¿X¯V^<}æôüÌX\x0016w776»\x0013)Ñ¶ÛY0a69ì¦UÙmU\x0015	 ÒD$H¢;H¨Pº©®H4PTé±,e±,ãqq8\x000cÇãÑñpt\\x0016Ç¥uZ)Tt¢NT\x000fÄ\x0018­»-Ëba\x0019Ã²\x000cc\x0019F·1\x0016Ë²8\x001eýþèîîÎíý½¥[U©ÌÓ\x0004ÆqÑY<ì÷öû\x0003T­ã2,Ça,m,íaps{G±Þ "!\x00152P\x0012hPJ\x0002\x0000$ÑÝ@\x0000JwKD\x0012It·1$\x0012ºcUJUéÄñpïîîRM\x001bDUIH\x0000¢\x0004¡</p><p>\x0000T\x0015\x0005%HC¤(T* @UIÆ\x0004ª</p><p>T¨*@(\x0004PTEB)$JH"!\x001d\x0011L&$Dë^èa5Íz¥DM\x001cGéHb½ì6+IÙlv6óÊTe5Oö£hc,no\x001fÜÞ?89=ód½v²ÝØngñ©ífã¸\x000cO\x001e?òí÷?¸|ÿÞ<J#6­»Û;ççç={*i«Õìââ\x001c¤n<{üÈ³§U\x000fWÒíp8úùç-ËâÝ»·>úè#¿øÅ/ãÁn»öäñ#\x000fÇ£\x001f~üÁ·ßo9.¾üòK\x000f\x000f\x000fz´ÓÓS¿ýõ¯>þä\x0013ëÕl½ìNlO¼ëøÏÿù¿xúä©/¾üÒÉnëûï¿õÜþ\x0017~ôgÎ%Ü^_Y­×v''JçÙ<ÏeXAÅÃ][­gëÍ</p><p>$A\x0004:\x0002	¡;º[\x0012ÝCº¥#Sn!S$Ñi´\x0012ª\x0004iXÆÑ\x0018\x0007Çå`YöÇ½ýÞáxt8\x000ec´t(\x0014</p><p>H"ÝZI"¡»11,cXÆ0Æ°,Ã\x0018Ã\x0018GÇåèpXÜ?Ü»¹»óð°DÕdªR&Ýíp8\x001aËÁa¿·\x001c\x000753îXÅq9ZF,#îî\x000fÞ~¸t\x001cÃãÇ³ÝÉ\x0016\x0001I¤©\x0002º[´*º\x000b\x0000$DwënIT&I@\x0012D\x0012I@U\x0001BbU\x00150Ué\x000c\x000fû;ÓÔF·\x0008\x0002\x0008Eº\x0010PB©\x0010¤(J&\x0001@("(@\x0011\x0008¨* ­ªP*(\x0004P\x0000¦©$TPE¤@P¡»u·Ñ¦ $H/2\x000ej=ÛnfÓ¼1Ïåx8þÿ	ÂeÛì@°\x001bÓØê«@\x0004DeV&ZìÑ\x001f\x000f£\x0019\x001bld»¬¢!\x0010xâ¾+Új-w\x001cÃuYE¦Ãak;ï2X×êùéÁ¼m¦Ù\x0010áåxr>Lãh(áÍ«;¯_ßÚïwö»­O~óõáÑëWo½¾¿w½^<\x001eO_^\x001cnîm7\x001b÷w7vÛ­»»\x001b_¿~v¾4k½õêÕ½Z«»½i\x0008»ÍlzûÆÃóQïér]´Z=??Ûn·æyTuã\x0018\x001e\x001e¿Ò«ßýø£\x001fó¿üêééh³,×«W÷÷þñ¿ÿw¿üò«ÿñ?þï¿ÿÞv··ßo|óáç§G?½<ûúø¬üõg·w7vy\x001a<?=*­"et×ËÑ4qÔ[µÝÎJµ¦Är½º\x0006ÓpC2SJ\x0012È$Lz¦MïMïUmUÉTZ%i-½\x0013D¤\x0014\x0012ÙS­Õº.åjY®Z]«ëõêz]¬kÕZ\x0019"L©÷®µ¦µ*³È¤÷®õ¦Öªµ¦¶¦µªÕ®Ö¦ÖÕZWu]]®«ÓÅóËÉu©$@èÖµ:/ÚºXÖEK¢\x0014]kÝºVµUµw­Ó®«Z«ÖÝî`»\x0005RÊLd¦Ì\x0012\x0000ÙSJ)3õÞõÞõÞõÞAf\x0008Ì\x00002\x0013D\x0012¡bH\x0011ô\x000ca]\x001b®ÖÖeo"Ò" \x0000\x0000 ev\x0002\x0002\x00102»D \x0012]f\x0000\x0000(\x0002)\x0001\x0004"\x0002È:\x0008\x0011!\x0013R&ID¤D\x0008)¥©õ¦ô\x0000QLzO){ÓzÕ5%a`³\x0019¥\x0018Ê`\x0019FÃXl§Y]«çóÉãóÛû;ß¼ßÛï¶2É$\x0014Ër%ºa\x001c==¿xy>ù?ýÙùr%&7½âéùì²vN'»íÖýÝ­yüúë/®×o¾ýÖ/\x000fÆqôùó'ÃÖ<ðøø`©ÝËy±®ÕñåÙn·UÊ`]W_¾|ñùógëÙõ²(1øû¿ÿ{ë«{¿þüÑù·Ï>|xãææ`­Í¿þû¿ûßþá¿¸®«O>ûýï\x000f^Ýßp_ôÞµ\x001e\x001e|úòÅe½úoÿû?ø¿ý£Ï¿þêr|6o6Z_,ËÙñiµz¶^w¶»;Ó¸hkX.Wm·S¦\x00022Sf\x0002È¤÷Ô{zv­7ëºªu\x0011e B)MDH)¢\x0010\x0003è=õÞÕZ]¯\x0017×ëârY,k³\\x0017×eµ®M]W½uPdº6Ë²XRq\x001cZëZëÖVµÖ´ÖÔZÕÚ¬µYÖÅz]-Ëâtºx~zñòrVk#j«ç³q,ÚZµÖÅ0\x0018ÆAé©µ®µªµ¦÷.3ôLk]Ó¢Ö.3¥ \x0013È$¥dÈ¤gzïZk2Sk]ï])!"d\x0012\x00112SDÈ\x0014\x0011"B)\x0005DOc S)¡·ÐZ×úbíMHQE\x0006\x0004\x0008\x0000$BDA\x0000H]&\x0000)\x0005\x00002\x0013\x0010\x0002\x0002Bf\x0002@f"D$\x0008"LdJ)Ì\x0014\x0011$$B Ñ{Wk\x0013Q\x0004\x0006A\x0000½§ÖºÖºÖRïMïUÏ@\x0008aFÓ8jS{³Ôj­«\x000c\x000c£ëuõòòâõ«W^½º3of»íNfê¨=ýå§_ôÆµ2möçº®(¦yãí»\x000f\x001e\x001cGÃÎíí­/_¾º¿ízYýúë¯>|ó­ÚÒ¯\x001f?¹»¹ÕË²úíó\x0017_¿|1\x000eÅwo|÷ÝwÎ§£ùÿ¥µîåxrs¸qw³ssØ{ûîãéè_þ×¿ûúðäw¿û½û¿üåÏÎ³ßÿþoüó?ÿOÿñ\x001f2MýaïpØùÝï~4Í\x001fµVµÞ<?½øí·O¢wz3\x000cÍ¼±v²wçÓÉrM×óÑ~¿xõæíá GZëbYVa2»Ì\x0004©'Ìzïjmj­j­DÓ{*e\x0010QD!\x0014\x0011h\x0008­u½wµVëºZ®WëÒ\®Ëe±\ªu­jí:\x0008Ì°®Íå|5
\x0017%\x00062	zëjëj«j«ZmÖuUk³.ÍeY,×Åå|ñôòâééÙõº¡\x00042HÖµz~zÑÖªµ°Ùìl¶a\x001c\x0006ÙÉÖµZK­7)\x0010zÒzêIDÊL\x001dD</p><p>d"ÉLZozk2Sï)³#e\x0012\x0011\x0000J	Ì\x0019("Bï]kMëÝ\x0018</p><p>Ñ%¢¬©·¦÷0D\x0001D\x0010\x0001"C</p><p>\x0004\x0002!%èd!\x0008"\x0005\x0008\x0000\x0002\x0019)\x0012\x0001d¦@ê\x0002\x0002\x0002d&\x0000:\x0010@ \x0013\x0010È\x00042eoZkÆ¢w\x00042µzïZK­wµUµ®"BDAÈèB(^¥NÝ~o¶N§O¿\x0008ïß¿w{8ççç£§gûÛ4N³ÇãÛ[ÛíÖ/_|<LÓl\x001c'Ó4ÓÓétr¹ì÷ßø¯ÿõ\x001f|ùòèãÇßÜß¿²,«Û»Wæ!üç_þ¢âõÛ÷Ö\x001e¾|ýªõ&"DZj]ìi¿ßº¹»ñåëW\x001fæ÷þñ¿ÿWOO\x001e\x001f¾|zp³ÝúÇÿö_e¤ÿø÷×³¡øë_ñáÃ[?þþG½s8ìôÖ}ùúèáñEæÏ~üð\x000cËu1³q;ê­)¥Bàr9{zz\x0014Óh&"´µiã ¢Ë^e¦,¡÷dèÙõN¯]«U­Õ²4]\x0019ª\x0010e4\x000eQ@èh½iµi­º^\x0017ËÕe©NçÅñxr¾\]EmUÏD\x0010@mÍõr1\x000eAJ¥\x000czïÖµY[UëªÕfYVëZ]×êr]'§ÓÙóËÑétÕj\x0013Qd"ºÌ°\«ÇÇ\x0017ÇãÉÚqÜß R&µumíZ]µº\x0018\x0008²ÓzjJozO\x0010H@d 3õÞd&Rê\x0004\x0011ÈD\x0008\x0011dI\x0004\x0008 ¢÷®D\x0018# \x0008]\x0008\x0011©÷\x0014"("B\x0002ºD @ "\x00042Sf</p><p>\x0001H\x0000)"@D H\x0012$ÈL\x0000¤\x0014BÈL\x0000\x0011!3\x0001\x0000D	\x0000\x0000!Df×³H)2Sï]k]f×{ÓZ3Q$ªÞ»ÞºÞ:\x0018¢\x0018§Ù~;\x0008ÍãóÕu]\x001dOG½§ãñèt>ûúðèñùÙápc³Ýê½;O2»Dë©ô¤w¯îïf]\x0017\x000f\x000f\x000fîî^Ùl¶v»O¾xzzòÍwß9¼}åñáZW¯ß¼uw{ëf°ÝÌ"¿þô÷ïÞ{ýö½~úÙdR×j]\x0017/Çîú\x0017üã\x001fý×ÿò¿ùóöåËg»ûÿÝ8M¾~ýâr½ú?ü\x0014Þ¿c3M>]¾Ønw>üðAké·OÜ\x001eöö»½¯O_]Ïge;ÛL³(t]£\x0012Óù(¿pÿúµiÞ\x0010¡õ.³ëD§Ó3édÞ»Þ»ÞÖZ«u½j½	0\x000c:Ì±\x0019Ê 3ÔÖôj«j­.Åùru¾.NÇóÅù²XUï)\x0004AT"Éf¹è"Â8L2»e©ÖÚ,ëb]\x0016Ë²º,Ëuu:]N'ÇãÙé|u¹®R\x0018A$	i]ç#ÑÕÆ<oD\x000cD±NÌt¹^]®g×åª®Í0PJIfYuE"\x0004\x0002 %\x00192SfÊNÏ$S 5¥\x000czO­7)2©÷®Õ&{7F\x0004\x0008A\x0010"\x0008!3õ$2\x00142C¢e*(\x0011èd</p><p>\x0004 3ev\x0011\x000c\x0002\x0000\x0000\x0000.\x0000	)3Rd¦ 3e¦\x0000\x0004 e¦\x0012EfÊ\x0004zO½§ì©é"B\x0004Ð{W[ÓzÓ{×;´HÔeV­5­u½uÐÛªD\x0011½ÆImÝñt\x0011ÙMód»ÜßÝøòðäù9Õºº½½õôô$³\x001bÇÉ4Î\x000eûÃng\x001c·oïì÷{\x001fûÍÿüÝîðùó\x0017µ®>ùlGûýZ¯¾|ù"bð»ßýh·Ýùåç\®ß>}r<_\.W÷¯l¶[ó<úïÿøß<?\x001dýòëoîïî=ß\x001fýòë/záÿùÿúûöÛ\x000fÆ(ö\x0003^ÝßYÅ?ÿóÿt:]¼~óÚßüþ÷þð7¿ÓzStM]Wu½Z£aè\x000cA\x0019DoÎÏÏ²77ww¶\x001b=\x0007­w)\x00022$;½w­5µVµVëºZ×«µVb\x0018»qLc\x001b-\x0011zOµ6uíÖµº.«ÓõêrY\¯W§Ëâ|Z\¯«ÚÞÉL	èJé2WKQD\x0019\x000ccÓ[ZÖêº,.×«åzq¹\/Óåât¾º\®.«umz\x0012\x0011"BJÐAmMË.;aq<ôLc)2S]«Ëõâ²\e\x000b\x000cJ)@ïô.\x000b	D2Sï]f×{Ó[Ó[×zÓ{×[D\x0008©÷&\x0013\x0012\x0000ôôT¢\x001b#Bf"\x0000\x0000!\x0014zR\x0002\x0010);:Y\x0002D\x0010\x0002\x0000\x0012\x0011	\x0000\x0000\x0000d\x0002 D\x0000	 3EÌ\x0004½w\x0010\x0011"\x0002d¦\x0000"BB\x0004Ùe¦ì©÷Ô{\x0017\x0019"@ÞS«M­Uk©õ®µT"É$RÏ¦÷U­Mfj­ËÞe¿ªµ«µ«9¨­©ëb\x001cGï\x000e\x0007ÛyÔ:gÇçGÃ0ÚLÝÞÓó³í~¶ÙldoZ¯vó^)a\x0018u©>}úd³9úá\x001f}óí\x0007ã8é>þâÍ«;¤çç£7oÞØ\x001fv\x001e¾~Uku{{§µf]W¤ôÃ\x000fßÉ¾úôÛoÞ½ûàññÅ/¿|´ßí}óíw>~úìÓÇßÔÚ}÷Í\x0007oï_¹^Ï´îÍÛ·-Ëe¹Ê\}øðFëÍ4ª£VWÑS¯«º\x0016QÒ8Î¢&¥\x000cÊPÔåêåéÑ²¬nÕ¼ß\x0019¦A$dÊzÖÖªZWëºZÅ²¬Z«dHET¢,Zg­Í²®¥Z®ÍuY\ÕõºZëj¹Vkmjëz'\x0010DH\x0011!Ì°¶®Îj/"&µ¦ë²¸\¯.³åzu¹\]®Ëu±¬ÕRV;\x0008%(è\x0008¡(Ã \x0010²%Y¬KÕúQ 3õÖ´ºª½\x001ceBÈìµZ¯U\x0019G=!e ;Ì.3u]ö¦÷®·¦gÓ{×{LH\x0012\x0001@Ï½#DPJ\x0018J\x0018ÇPÊ`\x001cgã8j­d\x0002\x0008!\x0004Rï]\x0004\x0004\x0004@R\x0008"dO!R\x0004\x0000\x0010\x00112\x0013 \x000bÑ\x0001\x0000d&\x0008\x0000\x0008\x0012 D\x0000 C"Dê­k½)Zëj\x000b\x0011 </p><p>\x0011!{ZkS×®·ÔkªkSJ\x0002ÈìZëjkzïz¦Öº¶6ëºZjS\x001bQ0Í³Ívg¼¿·Ýlí÷;½§ÞÓÓãq\x001cm7\x001bw··îïî,×Åõz2\x000eW÷w"Â?~g³=>>SØî·J\x0014o^¿v¹\|þüÞ»ÝnëññQ­ÕÛ·¯½zuëz]ÔZõ^mw;·77j]ýøýw~ýågÿöøoÖ>þúÉíý¿ýãßÈìóU\x0019&¾<¸¹½ñþÝ\x001b\x000f_¾øòõ«ÝvçæöÆç/}úôI)ÅõrÑÖp~z°,Z\x001ba(R7	eØ\x0018"ÐE\x0014Ó¼q]«ãËu½Ï\x00077w·6»d©·®uz¯Öºº.WËÙårv½.ZkZ\x000f­¥Ìèµ6ËZ-Ëj]«eijmÖÖZõìjë 3\x0010B\x0010ÈDèëµ)±º,«nQÊUÏ°.Õ²®uq].Ö¥ZfmM­]vz&B\x0004\x0001\x0008)J\x0008!"\x000cC1Ô\x000b2E!¤ÌIf\x0010"\x0002dvË²8ÎvÛ³iE@\x0012½Kd¦ÌD)J*\x0002¥\x00142d&IfÊL\x0019©µ&3\x0001\x000cC1O£y\x001cã¨£Í¼1n¶[ýtÒz\x0003\x0004\x0008ÌT2e&H@ 2E\x0000)\x000c$\x0000 "d&ÈL\x0000@\x0000\x0000\x0000@\x0002P$H\x00012S\x0004	2Hµ7Ù»ÌP[34J	\x0019D\x0010ZcYVËRõNë´ÖõÞÔ³Ëz§µ®õªujëÖuµ,«ë²Z×ªõNi-×j\x001a6Þ½{ã}0MOÎçÓél³Ùè½\x001bÇÁá°·\/¦iv9=ôæõëWôôÍ7\x001fDÇçgëºªµ:ì¶~ÿ»ß©ëÕO¿ü"J±®«Ã~çí{µv?ÿò«ÇÇ\x0007ÇãÑwßëoÿø{çãÙÇ¿Ùî\x000e\®Æ)¼yûÊ/\x001fõúÍÿò÷ðúîÞu©Ç£Gww·Þ}øà?ÿü\x0017\x000c~øá\x0007Óo£ÿïÿùùþËï¾ûÞ~;é«a,1XÛblUj²M\x0019D\x0014½7i2³íþÖéåÉùåèt^ôÞÝ;ãfºÞÞèz¯2a\x0008»ýÖë|cÚl/\x0017§ãUm«ë²Zj³,«ë²ZÅº®êÚÕFOz§édÊ\x0010\x0000H\x0011!3\®Õ¯OÊ0¸®UïP´jmjkjozvÙºÌB*"("\x0002\x0000@ \x0008"B\x0010%H\x0011Å0\x000eaPJ ´Z­ëªÔ.{ZWµ5_\x001fB&ûÝÖf3ÆÁ4\x000eÊP\x0018\x0000</p><p>(H­5rRïÙµZKÙÞVÓZÖ;Éf\x001aMe\x0010S\x0018J1A)aÜîöj«jo¢§.2H)3¥\x0004"0\x0008\x0005\x0019\x00012S\x0002B \x0000\x0000\x0000\x0000@\x0006Ì\x000e\x0008"\x0002$BÔ\x0011@¦ÌDÊ$%\x0000R×²k=ôÖõV  Q[ZÅZ¯z¦ÖZ\x000bR×Zê=eïzïZojkÖµ»\\x0017ëÅr]ÕÚ¬­©-
eðôttw{ïûï¿%ö¦q\x0004\x000f\x000fZc'zs¹ÂíÍí<;¾¼¸^\x0017­5ëZíw{­v÷?¼q:|ýüÙÇ_5£ÝfööõkÍF\x0014>}þìíÛwöûÏÃñxò§?ýÙûw¯í·\x0007ÿò?ÿ·oßøþû\x001f\×«Ý4
~ùå\x0017ß÷ï¾ûàÓ\x0007ûýÆÿúÿâË×Ïþá\x001fþÞáæàþþµåzµÛì´C³¬«oÞ¿sg~Ó.\x0017uM½\x0017c\x0019dKËr5o¶¦iQ´ÙÌäÁsë®ËêùéÅ¸Ü{\x0019bFó0§Ùv··?Ü\x0018Ç­ZÓËñÅãÓçç\x0017ÇãÉËñÅétr¹^Ôu±.«Ëuq<]ÎWËÒ´Úµ^ev²XUmWz\x000f\x0011\x0005árm>}=!µLAì)2d$\x0011d\x0011Q\x0012D H"ÈL\x0011!3e¦\x0000\x0004\x0002!\x0013É\x0010Å4\x000cÆq4N£q\x001a\x0008µVËuR{×Zª­é-­µ{zz±,ÕÍaçæfçöæ`»¹µÝnE)DID,ëªÖ³ZÌÔzê­«­jµ[kªuU[Õj³¶¦ÖF¦i\x0018\÷[ûÝlÞLæy²ÙÌÆÍfk­«Z«Ö\x0012H\x0011D2\x0001\x0008 PH@@\x0000R ¥\x0012\x0000\x0000DÌ\x0004$ d"\x0008!%\x0019"\x0010d¦DdH	I(\x0008  É\x0004ÙI2SÏÔ3õ"R)\x0005IÖºëuq]¯BÑjSÑ¤i­]­Uf×{Ó[³®Õ²4ËuuY¯ÖµÉ\x001eZ¦ÔZÕÖý¯ûWO_½~ýÊßçÕë;ã\x0010N§qÝÜì¬ëb;í½ºe·Û¹¿»\x0013Ãäó×\x0007ÇçgÃ0xÿá\x001bã0ÇÉñåÅ§Ïl7³ï¿ûÆ?þh\x001cGþË_<\x001fÞ¿ÿà\x000fï½ÿÁÿñü|úüÙ?ÿÏÿå»o¾µÙl=|}4£aCñ·ü£_~ýÕ¯¿~ôÍ7ßº»Ùûúå«Ý~ïx<ú×ýwïÞzÿþ\x001b?}r>¼~õÊu]ýôóO®§\x0017e]4E,2§ÉÚV½V1N":"í~'£ðü¢ez~>¶[oÞ¼·»¹7o\x000f¶óÎv³³ß\x001fìon\x000cÓÆùzõòòâÍñ¨ÖªµjY®j]æi°Ûnôì~úé\x0017ÿü/ÿê·ß>[«ZWPÊèåøâôüHtkkN§ËeÕ["]Ö\x0014R)E"JQ</p><p>¡ "d\x0012\x0011"\x0000 \x0011\x00002\x0013d& DR</p><p> E@J]è`\x0018\x0012£±ZR[U[×Z\x0017×b]ªËåªõÕ²^ôì¶Û½Ý~$ÞÉ¤gê­y9=?=º.Wµu½u­u­5­UkïzëjkZí2Sï]oM)áée¶ÝL¦i°ÙvÙXJ±ß\x001f´ÖÔÚÕÖôL¤=ôL­u¥\x000c\x0002A	) \x0000\x0000)L"ÈL\x0000)3E\x0004ÈL\x0011\x001e"\x000c	$Éì\x0012²\x0008\x0011ôl"</p><p>\x0000$\x0002È¤gÊL½w½w=è\x0000j]®gË²*etY\x0016µÖ»µ6Ë²Z×*Ñ{×Zµ,Õºvµ5­¥I&\x0001!"Àùrõ\x001fú³ß>}½KÝíÍÁa¿Ó[³ßï´6;¾\x001c\x001d/.ÅçÏ_lv\x0007)NgËrõÝwç'"ÄP¬­Íî_¿öõëWÇãÑãã£ï¾ÿÞv³ñòòìææÎ?þãóýÿ?>}òsÿÕßÿýß·³?ÿôWïÞ}ðý\x000f?Ú\x001fv>úì|¹huñêþ­ß~û(3Ýßß»\\x0016ÿú¯ÿîùùÅ÷ßãÇßÿàt¼øø×}úíã»×6%½<?(%¡(IPAéÍå|r9\x001f
ã`³ÝÊ¹\x0019ÆÙ~7Ü{9-ÅËãÙ7ßÞxóáwq6HQBÓ-õ*ru]®Z;\x001bÇ4Ï³(;%îãh»Ý»½¹óúõa\x000cÿùÿivþü¿Z×Þ«RÂ8N®³ãË£RXëêÓo_}þüÕùrÑ3õÞ­kÓ["J\x0008!¢Ì."D\x0004 e¦L"\x0002@fÊL$BD\x0000"èÙ´ÞeKt\x0019iìE)2L\x0002ã8ëZ¦y\x001e­ËjY\x0016k½z9\x0010¦i¯÷ADh­«½é=µV===y||°¬Uï©g)3õÞd¦LzO½'B&­¯zoÎ¡\x0014ãXÌÉ~»1^.W»ÝÖn··,ÕZÒ*ºÌ$\x0011d&\x0010Hz¦\x0012A\x0012ADH\x0000\x0010 3e&\x0000\x0000ÈL\x0000\x0000!{\x0008)Ì \x0013¢\x0000@f\x0007 HI\x000f$Dö®µ¦·\x0010(2»¥..e©ÓùTkµ¬ÍuYµÚdRí]¯©7ºD d\x0010@ïIO\x0014//\x0017ýéW\x0011|øðÖ÷ß¼³´îÓ§Ï2\x0011LóÆO?ýìó/q¶ßî¬ëjY®2Ó4O¾>|õøøìË×\x0007ÇãÙv·\x0013º/>Ûïwö»y<<<ø÷ÿ\x000fÿå¿üWoß½õåáÉç/æ¿üÕßÿÝ\x001f\x000cãä×ß>¹¹½s¹\x001cG¯îïmæÉv3ûñ\x001fm·{ËêãÇÏ29Ï~ýø«y3¡÷®K½6zr9=ÛÍ\x001bC)\x0010\x0011Zkzo.ç³lÕ8Mzë¶=´)M0m6¦µÊuuyyöøåWwonµ\x0018,ËUkÍ8Ìn\x000e7¶»½PôlR×zW²+ãh\x001c'ÛM±»RV½5ÙÎ\x000eûÁû÷wz=È¤\x000cÅ4ÎZ[Ï¯\x0003½wo^}õõÝ£óå¢gÓ{w¹\½<\x001cGëª¶ \x0008!b@\x0008\x0000\x0011	!"d&ÈL@ EÙõ\x000cYÂÐSêú²Zb\x001cÒ8¤\x0012a\x0018\x0006ÓPL1ÈiÔ7\x001b½U×õêº,R8/Z{ÐZ³,µU½w­5×ëÕ²,²§Lz\x0002\x0012BfÈìz\x000f2$R!ÚºÚº¥r]eéÿÇÿýÿöOûýÁ0N2CkM««Ö»ÞSï	J)aP"´L\x0010A Bm«eYÔuÕz\x0007¡2SfÊL	\x0000 3AD\x00012SD\x0000\x0010\x0010!\x0002\x0000¤Ì\x0000);)RÏ\x0014Ò4\x0014C!DöÔZw<\x001dýüó/>}~P\x001b­6×ËÕéru¾,®Kµ¬M­i­]­]&)d\x0016\x0011\x0005@\x0000\x0000	H¬µy~~v>]!,Ëêx¾zxzör<¹\\x0017ëêt¾h½\x001bKÑZõúõ+¯^¿Ò[SJ±Ýì\x001d_N\x0012D\x0014C\x0019ív;øÃßØï÷zï>~üÍårv/ÆÑérñüü,"ÜÞÞ:¾\x001cÏgïß¿³,ÌîÛï¾Éº®Þ½/ðòrtØ\x001f\x001cn\x000eÎç³¯_¾h­Ùn7þøûßY/'/_?ëëÕ\x0012RR(ÆqÙµZe'2PD\x0014­w-»ÖºÖº¡ÐE_«eY]¯UkÝ4Íö»½ífg\x001aGÖªV«º.êzÖÚÙº\x001cO\x000f\x001e\x001f~óÛÇ_|ùüÖªÍ<ÛÌÍf6OyMÃ 4Íh»Ù¦ÉápðöÍkïß½öáÃ\x001bß|xíý»{¯î÷vÛI)©gê½\x000b)</p><p>\x0001B\x0004\x0011ED\x0008\x0010\x0001¡\x0002"B)!"D\x0010\x0011¢"\x0014ôNï©µ½ë­iµËL\x0011¡PJ\x0018b&Íd»ÙØl6a°,«óùâ|9»\.®×«eY¬ëJ\x0006\x0006¢È\x000c\x0004\x0001\x0010\x0008$@Ò³ÉLP\x00102I\x000cÿð·?üÓáæÆ¼Ù)eRkM«Mk]G 0\x0008\x001d\x0011©\x0004%\x0008êZ-Ëb]W­V\x0010H	"\x0002\x0000d&\x0000\x0000	\x0000\x0000	\x0008"D\x0004L$\x0002RÊI&@	Æ!\x000c%H2Sfªuõôüè§_>zxx±VÖÚ]jY»ÚRïd/zLD È\x0010\x0001\x0008"\x0000\x0000\x0000$\®«Óéìùåh]WûýÞ~¿·Ùl<??9N\x000eûq(Æi\x0010Ááæ {÷Ë/¿(Qüðý÷ÆiôõáÁùrv½.^Ýß\x001bp\x0007Æa0Ï³_~ýh\x001cGß~÷­2\x000cDq>_ÜÝÞº¿»óùóg»ÝVïÝÇ\x001fí÷\x0007ËÕ¿ÿû8\x001cöö½¯_LãèíÛ·v»\x0003X«»»?üî\x0007?ÿçøúñ£1\x0019JÆADA¦Ñ4ÍJ\x0014=Sk
Iv\x0019ÈÔjSÁ².d\x0017Ioiwö77æyT¢kíêr~ôøôÉËóe9ªõ¢·«u9¹].'§ÓÕñxr>]´Æ4ÎqRJ:\x0008½7½/¡\x0018§q\x001cm·\x001b·7{÷w{w·;ww×¯v^¿¹õæõ»Û\x001bíÆ0\x000c\x0004]f	"B\x0004\x0000\x0000\x0011!"D\x0014\x0010\x0011"\x0008!D\x0008\x0008d²§ÞSï]fÊL]&Q\x00180MÍ<ÇA	¢\x00141\x0014¥\x0014¥\x0014\x001d\x00042Sf</p><p>\x00002\x0013	DIO\x0011\x0005\x0000\x0011aøöÃý?Ã`·Ûça\x001cÉÔjµÖ¦g2R\x0006\x0004\x0012\x0012J\x0014\x0011¡µfYWëºj­P@f\x0000Ð{\x0007	\x0008I\x0002" @J$\x0000H\x0010 @\x0008)2;	A"</p><p>A`,a(EDH¡gZÅãã£¿}ör¼j=´ÚµFf H\x0001 </p><p>	D \x0012!\x0012DBJD@È\x0004z¦Ëåê|>k½ÙÌ³ý~¯÷îr>Ûn&ó<Ùî6§óé$2=??[®W»ÍìÃ÷uñøøèøò\x0002nïn\.\x0017¿ýöÑ×¯æyc­«Þ»Ývc³Ù\x0018Ñårµ.Õþ°ÓÚêr¹Øï÷®×«ÝnK/¿j­zýêÞáöàr9¦É4MÎç½ßÿø½h«?ÿÛ¿©i\x0018\x000cq,"Bb&\x0011E\x0004 »ì\x001d)u){'èåjTÕv\x0015Ñõ¾º\ÇG//\x000fÇ'ËRãd\x001a']­VW\x0011è"R.U«Z¯zVÙSö¦D5Mi3§Ñ<
6b3\x0017ó¦q1Ív;ÚmgûýÎáæàææÖn»5Ï£Ýf6O\x0013IoMÏ\x000e"\x0002\x0010\x0011\x0008@ \x0000"	"\x0010!\x0004\x0019 gêzïzïZkjmZëzozo"Â8\x000cÊ@\x0019Â86ól&ã0ÆÉfR@d$2ÉL	2Sf'S\x0002"0|ÿÍº.WÓ<Ùíoì¶{Ã8ê­YkU{\x0003e\x0018RD\x0014\x0010\x0012¡P¢hµº.u]õÞe&\x0002)$d\x0008!£ÈL\x0010A\x0004\x0011\x0014\x00002\x0000\x0010\x0001\x0008\x0010H$È\x0004\x0008\x0004\x0011HE\x001a\x0006\x0012!ÞÒu¹z|~òððh]Ì\x0019\x0008\x0011\x0001$\x0011!"D\x0010"(¥\x0010\x0002D\x0004@R\x0000\x0011\x0008\x0004Ikét>ùúðèááQkÕÍá`·ÛÚngk]].\x0017ÃÞÛ·oì÷;ÃXÌÙýý½ï¾ûäË×¯ÖVe¦ëåìËçO2¸9\x001clæÉf|}xÐÚêõëWJ¾><:^îïo}x÷Î8
J	ûýA­Ío¾1Ï³O>ùðá[OOÏ\x001e\x001e¾àééÁ\x0010éÍíÏ?ÿäóÇ_Lc	Ó\x0010J(¡\x0010Af7\x000cÅ0\x0016%BKz\x0011R¨kÓêbgQ\x0006¥\x0014C\x0019\Ï/Öu5m¶ÆiR¡2\x001b§ýþÎ4ïdvëzÕ[UJ(dEyÕû^	¢Æ2\x001a4
Í4vóÄ<§ylÆ¡\x001aÊj(ÕPV%ÏäÔzÓ³¦Ù~wp{{ëÍë{\x001f>¼õîÝk77{ã4ÊL­7½'BD\x0010\x0000\x0010\x0001dBBB\x0014\x0010@ \x0012E</p><p>©k½éÞ»^ÞIÈ`0\x000eÅ\x0018a\x001c\x0007ÛíÆÍ~oÞLÊ\x0010RR\x0008){Êì2S&\x0000\x0011!³ËL\x0000\x0010\x0011ßÿþ»º.Wkm¶ÛýíÍv£\x000cE«ÍÚªÌ&"a </p><p>\x0019\x0004\x0011\x0012"B­Õ².ÖÚôÖd\x0000I\x0000\x0000Ì\x0008dG\x0000È\x0010\x0002!2\x0000\x0000\x0012\x0008A\x0004\x0002);L \x0013d`\x001cÂ\x0010DÐz×ju9_<==:\x001e2SD\x0000	\x0008"\x0008\x0011!J\x0008)J\x0010@@\x0010\x0001D\x0010\x0011"BD\x0008\x0010\x0011"B\x0004% 3\ÕÓó³§§gó<{óö­a\x0018\x001c_m7³ÃaïææàþþÎáp0O¿}r¹\}xÿÁårõùëW§ãYkÍýý½i,ëâéùIëÝº¬®×«W¯^¹¿¿óôüätºÆÙ«»;oÞ¾ÕZ7MÇ§g?ñêÕ+>öððh\x0018\x0006\x0011\x000cÃàº\­ËÅ~3{øüÉåôb\x0008¦!e\x0010Èì ·&{SÆA\x0019F1BQkÓZRÔ^]«\x0008¦q2\x000e³i]¯ËõjÞîÝ\x001cîl6[ã¸\x00111¢²WËrRëUf*Q\x0008\x0011E)Ef'»q\x0018
¥(\x0011":\x0016Ã°§4MÝP°Ê¶UdÕÛ¢®ÝºR+kM¡\x000c\x001byãæpðúÕ7¯_yûöµ·ïÞzûæµÛÛ\x001by\x0012ÞºÖ\x001bÙ\x0001!"Aï\x001d)\x0010"B$\x0011\x0000\x0010":¡gêzO­5µ6­uµ5½u½w]\x0019Âv7Ûí6æi°\x0006»íÆf3ÙÌÝvc\x0018.eï²wD\x0004È$\x0010\x0001D\x0004á\x000fóÝ?õL×ëU&7½ÃÍÞfÐZU×d\x0018\x0006QB&¤\x0012RDZ«e]¬µªµÉL\x0011\x0005\x0000!\x0003R\x0008\x0004È "\x0014@ \x0000 \x0000\x0000@\x0004\x0002\x0010B&LzO\x0000¤Ô5\x0011i(a(dªuµ\¯§£\x0007çóEb(\x0003AB\x0004\x0011!"D@ \x0008"@\x0004\x0008\x0011!"DPJ\x0011\x0011J\x0014\x0011!JA(¥(eÐÖ:Èz«înoep¹\x0015ÜÞ\x001c\x001cö{ófãåtô§?ýÉ0Þ½{ïr¹úúðäz]l6[ûýÁÓÓ£ççgûýÞáæà·OE)îîo===:\x001eÏ¾|~ðüôìÃ÷¾~ýâx<ùæoýüóÏ"ÂårñÛo¿ÙïwæyÖ{wssðúþÎõôâéË\x0017ÝXB\x0014Bê½é½é½L¢qRbPAmUë«R,áº®.ç³\x0012i\x001c\x0007Ó¼Õ³;\x001edïöû½ÃÍA\x0019\x0006-\x001b:\x0011d½\x0019Á4ÍJ)J\x0019\x000ce\x0014AÏª÷&{j½ªõªµEk\x0017r5D(QôÆ²tËÒÕÊº¤Ë¥9_¹.ë\x0012Z\x000fCÙ§yÞæÙ<¦y²gýÁíÝ­û»[÷÷·îîníö[ã8JÝÚÞ\x001b\x0000\x0000"\x0002\x0000@D b\x0010\x0011\x0004\x0011D\x0002A´ÖµÖÕÖÔÚ´V­µéJ)¡\x0008¡ÆÑf3Ùmg¯^ßûðþ­Ýn'3Dè2C&½w2\x0001¤DG\x001aþðûïÿ©\x0008½5×ËÅ8Ývg3Î$µV½w%(2\x0011\x0008¥\x0014\x0011¡ÖjYWëºê­"3\x0001!@\x0008\x0001\x0004\x0010B\x0010\x0001"BD\x0008$B\x0010@f*\x0011DH\x0001 \x0004R"\x001eôì: HP\x000ce0Ð³ºO^GÏÇ£ç\x0017e\x0011¥(ePA)!</p><p>\x0011!"D\x0004AP"D)"B)E)ÅP\x0006\x0011¡PJQJQÊ D1b"¢¢"¢\x000cR\x0006%</p><p>Â8zOÏ/Ï\x0002wwwæÝFDñéÓoàææÆù|¶Öêp¸ñéÓ\x0017ÍÆÝí­§§gëâ|¹hÙ¡h½¦Ñ÷ß}g¿¿q<¾8\x001e\x001d\x000e7\x001e¿>ûõ×ß.\x0017­5ËÅÃÃW¯^i­ùòð ®Ííí­ý~g­Õñx´ÛÌ¾}÷ÆóçO®Ç\x0017ó8(\x0005H\x0019\x0008Ù»ìMPÁ0ÊXôìÖº8_NÖV
ÓNæ Õ®gYc1Móù¤ÖÕííWoÞ7\x001b¥\x0014ó´1³y\x001aMÓ D!RöªÕUë]ïM«ÖV½7µ®Öµj­ÉL­¦VÃ²\x0014óóëR,KX°Ô°ÖAm¡g\x0011e2É0dÈL){HÃ\x00106Û\x001b¯_¿ööí\x001bww÷¶Ûa(2Sï)3 ¢B\x0000 "\x0000\x0011!0\x0008@\x0010A©õ¤Ó:!DÌ2\x0001Á8noo½zuo'=Ó4M¦i2a\x0008\x0011d6²\x0012i(i\x001aÂf\x001eíwáóÃ?\x0004Ó8¦É8\x0016ÛÍl»Û\x0019§	d«z¦\x0010z\x0006(Á0\x000c"BkÕu]­uÕ[G\x0002\x0002D\x0000\x0004BD\x0001¤\x0002\x0012\x0002\x0010A\x0010\x0011DH@@\x0000@Z&2\x0011$ \x0014c)æ1\x000cC×ëÕËóËé¤\x0000µV½'Ab\x001c\x0007Ó8\x0018ÇA) ¢(%R\x000cC\x0011QRR\x00122(e\x0010%\x000cÃ`(E)ÅPR2\x000cJ	\x0011E)E)ÅX\x0006\x0011¡¢""Zo®×«ÖºÍfët9{|z&Âr],×«ÃÍÍfãååÅ²Tã8i­¹^/Z¯J)Æa½;ì\x000fÆqôéó'ùË_ýðÃ^¿~íáñÉùrÕZóêÕ+»ýÎ/_,ËâùùÅét"SÏf0£ÃnVO/ÎO_\x000cÙ\x0015!¢(%DP"Rdï²wQBPÆÁ0\x000ezïRw½^Ïg©7;½ÓújYN`¿»\x0015ev|>ÚnwÞ¼}o³Ù"UÄª·«ËõÅ²¬ËÅr½jµÔ³Ë¤gQ+=\x0007ú¨·A­e
kem¡æ zÞCí¡VZ/Æa2N³,ZOÐÖºZ»ìD	ã<Ûívîîî¼yõÚ»·o½zýÚÍÍ­yÞ(¥ÈL=Ô\x000c\x0011\x0001 "@\x0010\x0011\x0004%AD("BD\x0008¢ dì´zkZkÖ¥ªµZkÕ{SJ±7æiT×Õ\x0010ÜÜìÝßÝ8ì·\x000e»ÛÃÖ«ÛWw{o_ÝøöÃ\x001b¿ûþ½ßÿø?üø­QLÄàÝï½ÿö\x001b_\x001fü~ÜÞÜº¿¿\x0015Ù¼¼\x001c]×."ô "\x0004\x0012!\x0000\x0011\x0000\x0010\x0000"Bö\x0012\x0008zÙ H\x0000DÌ\x0004"A\x0002\x0002$ \x0000D\x0014\x0005\x001dt!"e¦AÚN³Ãn4
U58\x0005m\x00087½·w·\x000eÛß>?8_\x0017\x0018</p><p>9Ã<§eiµª­	\x0001RR\x0004 Af)\x0004\x0010A\x0004ÈL\x0011!@*%\x0010\x0004\x0011Ð;\x000fO/\x001e^|÷]sØ\x001fÏgúÏ¿xsçíÛ7ÎçeY]®gËÒôÎ4ODZÖUf\x001aÑõºøçÿù/öû­o¿ýÎ8l\/«ï¾ÿà÷øÑ¿ýÛz~yñóÏ?ûî»oLãèùùÙõ|UÆb­ë¹¸Ýï|xÿÞëÛ½Ï?ýI½\x0011b\x001côD\x000cBÙéMD²§Þºõ²\x00182\x0018ÙvwpYe97;[ÇSszyöÔ\x001emæyw0MÅÓÃW\x000f\x000f_ÅXd6­¯Ä*TëZ\x001dW½wÃ8` 5­\x000c"\x0004!sÈ,"zoZo(ä`(2\x0014U/UÖUÏf\x001aFÛÝÆf;\x000b\x0005¤T"R '=SHQ(\x0008¡Øï»ûW^¿}ïÃû\x0017OOÏ_\x001dÏ\x001e\x001e¿úòùãËëRõÖE\x0004\x0002)J "R(\x0008\x0011\x0001 3 HRÓ¥µu]+]öÁ<\x000fb,ÆHÚÕz	!\x001c^\x001fLÓÆPV«Z«"B$ãPl6íf¶ÙLÆi2\x00062\x0018ÁÛwßøáÇ?úù?ýû¿ÿ§iM¿ìv[ww÷RÈãÉuY))¢\x0008\x0010QD\x0012!LH\x00082D\x0006 S\x0004\x00052D\x0004\x0011D \x0001)\x0000\x0010dÊD\x0000@\x0008È."P\x0004$y*^ßlÜ\x001eFÓ0Y7Òºãq´Ûmm¶\x001b7ûÙf\x001cüúåÁé²èBD\x0018ÊÁ25et½V½7\x0008È$\x0010!\x0012	\x0000H\x0000%B@\x0010A\x0014dJd½{9ÜÝÝùæ[>ý¦÷îááIâr]¤DZ®ìÍ×oµÞ´^N'ó4Ú£÷ïÞúðá­ï¾ÿÁÿü\x0017ÿö¯ÿFçöæFßí\x0008_¾|us³\x0017Á0zk\x0008ww\x0007ïÞ¾U¢ûúñ¯.\x000f_EkÊ8É"R\x0006¥tzê­hLìM««uYóFD±Ù\x001eÜÇìùåÉù|t?»»«µîéËGíWwC±ÛmÎ/>þô'Í`{Ø\x000bD\x000czïz+ä(¤0*eB\x0011F%\x0006¡ë²U¦AëIRJyµÖ«Ì"Ê`Fã8è}ÐËhf³PJ1O£R\x0006\x0011!J\x0008\x0011!J\x0018QD¨uE\x0018ÇQ"3A)(mKÛíÁÝý½ÞÓ0e¹úòå«¿~ôë¯\x001f}þüÙËË³u]e&\x0019H\x0011B\x0012D\x0012\x0001J\x0010A\x000cÅPa(00NÅ46ód3Ï6Ód»l7í<¦É4¦q0
£RD¤¡\x0014¥\x0012Å8\x0014ã8\x0018ÇÑ4
J\x0019)E¦±\x0014Ûíd·Û)eòéÓ'%Òf}ÿÃ÷6û½[¡õÔZ³ÔU*dÈ !\x0004 	$\x0012)	$$\x000c\x0002HIBD\x0010:\x0002È\x0010\x0001\x0004RHH % À8\x000e¶ÛÁí~4
´Íd3^^6Öº§b¾¿5My¿óñÓWO/G­u\x0011ÅPÒ0LÆi2Õr½Z×&{JD\x0010Af \x0014\x0011\x0012\x0000I\x0012ADÈL\x0011\x0001\x0000RzO\x0004Âõºúù_}ÿí\x0007ïß¿s9WëZí\x000e;K]Ét{{cS«Óél\x001c7_õÞ¼~ý¿ûß\x001bÁãÃ£isµ,\x0017ýë¯Þ½{ç\x001fþî\x000f6­ç§gýé¯ÜÜ\x001cÜß\x001f,Å8\x0015¢{zz`½ØçU?½¤a #\x0003\x0005\x0011¢Ö;2»Ú«¡ÐÛ¤·aRbts³7m\x000f^¾Z¯\x0017÷ï¾UÆÙñåÉóóqÚØíoÌóÖÓ×\x0007/¯\x001fm÷7ÆaÖu=G-W\x0019VS</p><p>Ó4\x0018Ù8ÎJÔ{§Lz\x000cz­$\x0019¡õÐ3(E\x0019\x0018¦0Lh\x0003e\x0014¥\x0018P\x000c\x0008e\x0018a\x0010\x0011B\x0018¦\x0008j^0Î[e($¥\x0014ÃPa\x0010.3¡\x0018ÇQ\x0008Ë²:\x001d\x001e\x001e¾úõã/þú×¿úù|ùüÙåz\x0016J¡\x000cÆ¡\x0018Á0\x000e¦q4Ïy\x0018c1N£yLÓl\x001cFã\x0010¦a0M£y\x001eLãd\x001aGãP\x000c%
CQÊ D\x0018J\x0008D¦R\x0008¤RR\x0006e(a4\x000ea(J\x00192Ù].G§ÓëõdYV?ÿô«yÓà»ï¿³ÛmÕz£µ®²§B\x0000RB\x0004D" \x0004RÊL ÈD \x0008²#É.\x0013\x00122CH ¥$\x0002\x0000\x0000A\x0002Zo®ËU]ÓfLÑ<\x0014Ûirº\Ô¶R7Ûíîà°ÝúËÏ¿úòô¢õ.;¥0M(£RRÄj­Uk]&Q$\x0002Bf\x0008"\x0002\x0000D\x0004Ì\x00042e$\x0008\x0005!umåYd÷Ã\x000fß¦AT{s¾½~ýÚÓó³y.jO\x000f\x000fýíßþí~ë¯ù/_\x001eÜìöè\x0012×ëâåxvÿÊ<vÛÉ0\x0015Ýäöö õ.³ë¹:ÜmµºjËbÞ§låô¨×³q\x001céÕ0Njv=S)]b\x0018\x0007½7=ô®¶¦¯«HR½6³\x000fï?8=¿hËÙííÞïÿð·¾üú³óñÙ8\x000c\x000eéåùÅÍñjÞNÎKw^ªëÒ´J\x0018Le2Ådw¦q&é­©uµ´Eí\x0008ó4Ë^evÓ<\x0019§I\x0019\x0007ã4\x001aI«©\x000ci\x0018\x0006Ã8\x001aA\x0004½w"Ê "D\x0014Ó4©Ön\x0018GÛÝ^ö$çÙ4Na4M\x001bÓ4¦Q)Å0\x000c2S­«e¹Z×\x001fýÃò_<=?ùøëGùËüòóz~zÐÖÅ Íc§Ñ<6ól3ÏÆq0\x000cÅ8\x0016ã8Êd\x0018\x0006\x0011¡b(¡PJ\x0018J!Þ "N\x0012\x0008\x0011\x0001(¢\x00141\x000cb(¢RÀ\x0008%ÈôôøÅÏ?\x001eD\x000cj«þúÓOæÍdgïÞ½·ß\x001fôZv×ËE\x0004\x0011!\x0002B@\x0006\x0019"B\x000c)\x0013\x0019R\x0017A\x0008)e\x0012\x0008"D"Cf\x0012\x0012\x0008HR"EÌ\x0014\x0011\x0004]\x00022Sf×{\x0007Ù»Së\x001e]Í9+¹wØïLãh\x001cFófvm«e]­Ëj¿|óú\x0015=E\x0019}yzQ×*A\x001aÊh»(âZ¬kÕ{'Ì\x0014\x0011"Bf\x0000	\x00002SD\x0008@\x0001R`\x0018FÐ{:\x001eÏ>}þâoÞÚßÜXÖ'\x000fæi¶g=S]\x0016zêµysÿÚÃG§óÅ/¿~´ÛÍNçÞÓ4n\x001c\x000e·^^\x001eô_VûÃÁºV¯^½v¼\Eï^^\x001eMcÚN[wû\x001b1®/.Ï</p><p>R*\x0011ÂH\x000cÊ01¤Þ»Ê0hL½³ÖÕ<JÞ»ÞV×KU6\x0007ÛÝÖËé²zûöí¼ññ¿x9ÍóÆíá _.?6ßs\x000bZcÁn·³ÛmmæÉ8NRWëb]®uqYÖÓf»ÕÇ.3Mó¤2Ê0\x0018Á0Læy\x0014¥(¡\x0018Q)¡Öj]+J\x00192\x0018ÇÉ4M2SD1o7\x000e\x001b\x0010\x0011vÛ­iÃh\x001cFÓ4çÉ0\x000c\x0008½7ëzq>_ÔÚR|øð­?þáïü÷ÿþ¾~ùìËçß<?~v9}Ò'ê\x001e\x0018ã¨""\x0008Q(@\x0012	BÐ\x001b\x0012T"HR</p><p>!\x0004R\x0008\x0014\x0011A\x0010\x0011Rê=5Mn$¥ÏÏ"Òõr\x0016\x0018Ê`]ª?ÿç_Ã¬ÄàÍ7\x000eÝXj&\x0011\x0004¢\x0008E\x0004\x0010\x00112é=AH\x0002È\x0014A)¤\x0003@&\x0000)\x0002è=%Zï \x0010\x0012)µj­ÖuÑZ\x0018Ùä<!NZën\x000e{yc\x001egC/Jõzµ^O"ÓÛû[Ã0ÙÎ\x001b×åj\x001cGÇÓÙËùªÄh3J\x0019]Êª®UkUfÊ$"@DÈL\x0000\x0011!3\x0001\x0000DÌ\x0014\x0011\x0000 "ã¨µ¦ÁuY}ýòh7>¼'\x0012óùêf\x0018m7\x001bq[ÔÚ==>Úïo¼yýÆÿòg§ËU)!;mí¶AÏæt>[®WçËªÁ÷ß¿1³ãñäáëW·7~ÿýwvÇ_ÿÓùóG\x0013Æq\x0016Þº\x0011AèRR2\x000c2SöN¦ÞS\x0017¢Ò8\x000eÖZÏ'ó4\x0019âøòl\x0018f··¯Dù/?;]®vÙ\x0018áôøY+³ùö­Ín£g7\x0015¶ó(JÈX-u½k½ëb\x001cL1*Ö»óõb\x0018yD\x0019D)B1\x000c³ívoÞlRÔµé½ÞRïdRÊ`\x001c'ã8Ûn7æy\x0016\x0011z?Øî¶öûR(a¢\x000c\x0008zkèÆ±\x0018âr¹º^/"¦IDQk\x0013Áíí­·oßøîûïOgÇç\x0007§ç.Ç~u~zr9]­µÉB ³K\x000c\x0014¥\x0014 \x0008\x0005\x0000\x0011A SA"³\x0008\x00110\x0010AÒ[£®G</p><p>aøÃï¿û' ³k­[®V+\x0012E­Õñø"3í÷{ûýÞ<Ï(DH,Ëj]VumZï \x00022SD #EBBH\x0011	2$\x00142B¢')u)³k­9Î^^®Ú\x0016-»lM«U«Õ²\\x001dG///.ºV»íèö°!»e]dvÃ8ÇÑP\x0006EÊÞ­uÑZ5\x000eÝvãþfïÛ\x000f¯ýðí{ÍÆùrv¾\À8¢\x000c\x0012)e\x0002	\x0000\x0000 "DR</p><p>\x0000\x0010\x0011"\x0002!"H=Sk]kÝP\x0006ï?¼±ÛÍj­¦q½ ýnk·ÛÙl7êºj­ÉHµVC)\x0004ó4\x001aÇb]V)\x000cÃ´®ívc'×ËÙ~\x001b>¼¾uþòÙ/úW±^ÍÃ$"$¢\x0014\x0019¡GèBFÑ{"ÞéI"SÆ (z=é\x001di\x0018\x0007\x0011a½^ÕëU)ýáÎn¿#S¯q(Zo2«ÃÁÍí½Ýnc3\x0017ã\x0010è¢tQR¢A\x0019'ea0\x000cEïU­«RqÚ\x0018§Ù8LÆq¶w¦y£'­wuYÕe±®«u]I¦q²7¶Û­ý~çp¸q8\x001cì÷;»ÝÁf3¦Á4M²7çóI­«ÞeYÔº\x0008½w§ÓÑËËÔ
ã¨D E0ME)i\x0018\x0018ÇÍæ`¿ßØïÂaÏÍÍh»ó(\x0002z6¤DD\x0011\x0011"\x0012"BD\x0008\x0011ED(\x0011¢(E1\x0012"B\x0004¥\x000cJ\x0019\x0010A\x0008!\x0004BLÃ\x001fÿæûJAÒ3µVÕV¥$,¢µ®^^àææÆáp0Ï³\x0012a­«ëe±,u­ZïR\x0008\x0004\x0000RÊL)2LÈBB\x0012B"\x0013ät>ùõ×~ýøÉñxÔ{Ó{W[ÕZUkUkµ®«ëåâr½juq»ßxu»3EÏ®¶¦÷n\x001c\x0006ó4¦Ñ<OÆi4E)è\x000eûÉ»7wÞ¾yåöö ÁuY\U&ÃXC\x0018"dÒ{D \x0010\x0011"BD\x0000\x0010\x0011 "\x0010"Bfê½ õIêîî\x000e¾ýîi,d</p><p>LóäÍëW\x0004¯îïô^}þòÙû÷ïìv\x0007OOÏRì÷;··\x0007çÓÑñx\x0014C1og77{óÞ}÷í{ßûÚÓ<üòWç¯êåÅ(\x0018	èDÊH]2èBkMÏf(EdHjoz\x0006eTÊ "dïJ\x0014)$\x0008½6uYÔµÊ\x000cÛÍÖÍíÁ4b\x001cE\x0019´åEöªbÞnÄ82\x001aÆÉ0NJb\x0018)"J1i\x0012zOÛíÞíÝÝvo\x001agã´1M\x001b2ÎgÓYë«(a&ó<Ûï÷\x000eýaï°ßÛívæy2£yMÓ Õêt:Zº.®×ºVQ\x0012(2Sf\x0008QB	B¢+CÆ"VÞ\x0013¡è<\x000bÆáh»cØº¹=8Üìl¶³q\x001c\x0002E&\x0011E\x0008\x0012E\x0008A¤\x0008J\x0014¥A¢\x0010\x0011¢\x0014e\x0018\x0012J)"¡\x0014c)R\x000c\x0011Ê\x0010?þÍ÷ÿIF\x0008¤$\x0002)\x0010\x0014"Â²T///¢p{{c»Ýe¹º^.®Ëb­«Öº ¥L\x0002B`\x001cGÛíN)£ÖÈ\x0010Ì¤wIvÙS&©©gzxxô¿þÕ/\x000fjm\x0008ôZO­w­w¢(1h­é½»¿Ù{}w0¢wµj½)ã`'Íl3Oæy4*tC	%íft{s°Ýn¥p½^­u5\x000c£q\x0018 \x0014AF\x0011\x0010A	\x0019\x0001\x0002\x0011\x0001 "\x0000\x0000@DÈ¤÷I¢öF²Ûll6a(Zë>}þjgµUçÓY­Õ/_½~óÆýý+§ãI)a'ïß¿3¯ÖVRÌÞ»±°\x0019åÅÇ?ÿçÏY\x0016%RD\x0011%D\x00141$Ñ$¢L2\x0006këD¨­\x0019¢Ö õ.Lb(Æi²ÔU&QB\x0004c\x0019d¦ÞªZWÙªìU\x0019Íî`·»1\x001b×ËÙz=Y®'1NÆí2nÄ0\x0011#\x0006eØ\x001aÆqÌãd7æy#QÁÍÍýþÆ4Í\x0004Ã0æI\x0019¤\x0004ÛÍìîæÆÍíÃÁa¿·ÝlÌÓd\x001cG%Â²^Ôu\x0011\x0011J	½u×ËÙõz1L£Ývk³ÙÆÑ4\x000ca\x0012\x0011R#\x0018A\x0019(ÑA ¥ÞªÖ\x0016­\x001eõåI»þ¦^õAj,Ìe0oFûÁÍíÖáö`ØÚnF¥\x000cDê@1\x0008((""¥\x0018"(!"¡\x0018¢(\x0011\x0012R%D	Q(C\x0018þø7?þ @\x0008 JPD\x0018üÿ	ÂÏ¥Û¶í0¬k½¹Â\x0017v:é^Ä\x0005@Â¢h±,»Ê~?=Ú*( Ò'íôµÖsôîÖ¶mõüü$óùdßw//\x0017·ÛÍ¶mö}Ws*Ð&Ð\x0000`YÞ<¼õöí{"¼^^íÛ4çnßwûæÜmûnÓ>§}ªÊ¾OO_}üôÅS\x0018D\x0002Hn\x001a!DLÞ<ÜyÿæÞq\x000c´FuÛöÝ¬)2\x001dÅñpp<\x001c-K\x001aK`Û6¯/¯ÖÛêt<úðî­·oÞè^.¯n[iCfLîRZ\x0004\x0004Ýº\x001bÐ \x0004îÖÝ »\x0001­»UîÖÝº[U»\o^^^\x001cG\x001fÞ¿·®»ý·ß»ÞVïÞ¾×\x0008UmÛvwç;_¿~u<uóúòâîîlV¨ÙÞ½}ëÝÛ·Þ½{ãoßyþø?ÿË÷úõI6º\x0008\x0011!G\x001a\x0019*JkCç°Î]Ç¢#Te\x0019"è.ªt\x0017\x0011*è\x0008Ëáäxº3\x000e\x0007ûªËX\x0016\x0011aßwsßìûÕº]mÛæx8¸»»SÒºífµ\x0016îïßz|÷­ãÝ£±\x001c\x001dgww÷îÏwNç³±,\x001a³¦9wÇãÑÃÃe\x000cÐÑ\x000eÅùtr<\x001cO'\x000fÞ¾yãññÑápÐ]º[D íûêz½¨¹\x0008Ý&B.\x0007ÇãÙétçx<\x0019\x000b´\x0016\x001a]¥º\x0008"BjQMÞnöõýöyýI]ÿl¿ý¬öÏª^tOÝ\x0003DÉ,Ëaq:-î\x001f\x000f\x001eÞÝyóöÁýã½óiK\x0012e	K\x000eL#B\x000e2Â\x0018)3%-9F¦\x001ciÉ2äHH¡uîÖÝBÐ \x0010"\x0008éõõêþé½^.#¸»»\x0017"hÑ©A@#¨º[M2[\x0008\x0019¡u[í·\x0015­ÙmÛ7U\x0005ºCw@x÷æ­óùÎ¾íæ>­ë9ÅDÊ\x0008]¥k\x0008ÇãQ7×uw:¤¦[4]¼¾Þôübn»·î\x001eîÎ\x000f2Ó2\x0017×ëêõz³n7oÞøÍGKüãiñoþÕÇÏ¯ªÊr\x0018Ä ·Í¬\x0012nº\x001b\x0004hÐÝº[DèÖ

º[Dèn
\x0011¶múùçONÇwoÞ8\x001c\x0016\x000f÷\x000f>~r÷ÉÃã½Ûmõøæ­××W×Ëãñàr]U·õúêx:øío¿÷ùó\x0017ïß½ñøprw:ÈýêóÏöüù«l:BEÝF®i«\x0016{X(æ¾é\x0018:JwHû¾;a¡º-1tëjYáñþ\x001dä«e¤ÃÖËEºê½Ô\í·UmSV¦Çwâpçòú¢nõë'wý·î¿ùÞ¶ïº¦\x000cÔ´ï»9§ãÎç³»óÉ2\x000e\x0004\x0011áp88\x001eÆ\x0018"BUë*év»ùòåãñèññÑ\x0018iÎÝ¶­îïï=>>\x0002Bf:\x001c\x0016¡æ´o«ª	b\x000c¢)j\x0017Ý¢[ÕnÎ«ªW=_u]èÕÐ2B%1î\x0004ºZä"2°(åÁÈEõÅ\x0018ÓÈaîírÝ<}Ý¼¼ì®×Í×/íWK¤\x0010Z\x00119dÈ\x0014\x0011\x0000tÈ\x0008\x0002BBñ÷û7ÿ\x000bD´\x0010\x0011\x0008\x0010" \x0000m,\x0007\x001f¾ýNDøãþàþé]®«÷\x001fÞ\x001b#Í}Wsª¦»\x0008\x0019¡ªmûn]WÛºsµm7¯WÏ/Ïn·«e¤Ãáàx:\x0012áv»ÙöÝÜwÛ¶Ù¶mÛìûj$w÷÷\x001e\x001eï°­«®\x00129ÄH\x0011¡»Õ,UE·ÈAhc¤e\x00192B\x0008)"ÔÖuU³\x001cå Ç\x0019ÆHc\x00192Ò6wÛ¾\x0019ÁãÃÉ·ß¼óîñQ×æõõÕ¾Mc\x000c#SC\x0005Mwh \x0000D\x0004\x0008\x0011D\x0008"BD\x0008\x0011\x00108\x0016ß|xçt<¸m»ëõfÎÝÝýYàùéÉ7o<<Ü9\x001cN.«uÝ\//p>¦ûsýf¿<ùùO¿÷õ×_ô"Bf$A\x0004Ý-r9Ôl³1ÌY"C""\x0004¢ZDÈ\x001c:¸ÜVÛ,\x0007ÇÓ½óý£·ï¿ñðønYÞ®æm5÷*)Ð\x001a³\Ü=¾5ÆÐûMÏÕùáÁã»w"Òºí¶mSû¦»u02OGo\x001e=<>¸¿pw>;NÇ£Ãáàp88\x001eOÆXlÛæåõUwËLp8\x001cN'Ër°,Gçó½\x0007ÃQD"-#\x001d\x0007Ë2D¦ÌtXN\x000eÃ\x0018Xz\x0012óÜ\x0016õ3ógQ?K,ùâ´óñàx:9\x001e±\x001c\x001dN\x000fNwoNg§óâ|>8Nw»óÙýÃ[ÇÓQ÷Möª»l³­Ûp[ÏòðÁûoþÚ\x0018GÛzQ2É1D.\x0008c	)3\x0010Ð
"h\x0011d\x0016ADÐ¡»5 È@\x0010tÓ==<ÜûÏÿùòõé«\x001fþÉ_~úE£meÐ</p><p>e±ä°¯7ëzu¹\lëÍ¬)"\!sÈ1\x001cÅéx4Åa9ÈÛÍåòjîS\x0005Á81,Ëâî|§Ëõjßw/ÏÏ¶}Êm\x0013\x0011¢[f\x0008\x0019!"u×ë&®©úÓÑ\x0018\x000c!#6g{½\EÙå|>YÆÑÝÝÁñtïáaõòzqy½¨ÚíÝý½oþão}ÿÍ£\x000fÿô\x0007ÿøÏôåëUG8\x001eS</p><p>ë6u\x0017\x0008\x0019\x0000\x0010\x0002\x0000\x0011\x0001 »\x0001D\x0006&Çp»m~úù\x0017¿ýÍ÷Þ¾¹GéY²§óý½õvõåÓ¯Kº¿ôáý[\x001fº}ú\x0014Øé°¤º|õüå£õrs»\D1RU£ êFëÚõL\x0011C\x00065[rî´¤ZD\x000c\x0002öÙnÛÍX®¶Û«~û \x0016üòãÅ~qÉÂ¼M5§\x0008¶­¸ìÄªkWÝÞ¼}¯³]¿øøçqw>:=|ChÃaC\x000eF¹È\x000cU
"Ò¬Rs\x001ac±\x001c\x000e2SuÛ÷²\x001c\x000eÞ¼yôíwßH)´Dè¢ºe\x0008\x000eÇ£ãéÎÈÔ=Õ¼éZÕþÌúÅ^Oºq\x0011y½é¤»ÈI&\x001c'1Ê)ÉdiDQW½?éýjÆ¦º=?\x001dÝnÃËky}M/ò|	ë:ì\x001dîîn¾ÿnÈqtÿæËÓ¦öÝD£iZé\x000eÈÐZ$)E\x0004\x0001D%¢E\x0012Bw\x0003ZkÕ!cH¡µ©=¾yô·û÷~þågÃª°îÓ>\x000bD \x0008ðððÆ7\x001fÞ¹]^ýòËN§áv;¸]WÕ-"À)¹íºÊÜwû¾\x001b1GË!½{÷Ö·ß}k\x0019Ã%\x000c_¾~uùñGsN³Z\x00175Ë¾m(Ëáà°,b\x000cPÚek/ªÊ|ûÆû£<\x0004BDÈ\x000c­Ý¶WUíþîÎéxp>Üß=>Ü¹^¯jf­öíâtZüÝ¿ÿÞÛ÷o¼{÷èû?þÅ_~þ¬vNÇ!3Ü9§ª\x0002\x0010\x0011\x0008Ý-"@w\x0008Ð\x0008D\x0004hh4ªðô|±þÛ\x001f­·\x000f\x001fÞz÷æNÍéx<¹;ìë×õv5Æb½½¸;ýÃü®Ía99´~þ×ÛEÝ.R3R\x0014s7p\x0018!ªtÐZWéA×MäAH*d\x000eÙS6£Ý\x001aÑ!3\°¨¹Û×u}õòåëë«q8øæßZ_EíÆù&Ïæmenj_íu5#¬UöY2Òãã[§»i}òúóïÅÞþöï,wä0BEw»^¯Öus<\x001eÍY¶ms:Ý9\x001eÏàx8\x001aãèpX,ËÑÝÝ\x001bÃâp8\x0010èÖÝªJuÑ!G\x001a\x00192C&\x0019D_ÕvSÛWµ}²oÍõÚ¿ªºp\x0010\x0006.Ñ%¥!a9ã¢7s~VëW³ËÄ¾_mÛnßN.ëÉë5=_Êòõëêr)·ÙâpçþîàîHäjÛ>êý*e9Z·IL©\x0010º\x0003"\x000042À\x0012ÐA´\x0004ÐÝº(b\x0011n\x0011,KZF\x0008joªE\x0007\x001d\x0002¡	ÎÇ£ß|ÿ\x001b#Ãoÿê7\x001eß<ê\x0019¾|ýêÓçO¾~ýêúúj»ÝlÛjÛ7Û¶\x0013­óé,sxx8ùÍo¿÷Ûßü æôùógëÍm»úúõÉóÓ«¹\x0017¨.û,ÕSu\x000ba\x0005t\x0011A\x000bÛl__nªèº÷öñÎ)CfhÐU¶ms	"n\x0011G§û£ûóÁãÃYíåz½øúüÅíúj9\x000cß¼{ð_þÓß¹¿»ó¿ÿ·ñ/¿ÿÉå¶[\x000eÈ£Ûm³m»î\x0012¦5\x0000\x0000ht·n\x0000 ªÑºn"\oÓ\x001fþø£¿üø£Óéà°\x001cüæûoäþnñáýw.Ú¼}¸3Æpw<9ÞjÃ2\x0016çL½ÝDýÅº^Íj\x001d©bX02µÞ2î¶WI;{°´LF\x000c\x0011Ðt©\x000e\x0011\x00149q\x0010±ª9]_^­·Íá|öáÛ\x001fÜ?Ü{sÿ\x0006%ºDM£¹»¼<ûòåõòl»^ÙÚ8Xgyóxï´\x001c½~úèöúêí7ßyóÝ\x000f.×«mîî'c\x001cìÛôôôbßÛãGËáìx:¹»;[ÆBaYn\x000cZÙ·]U#\x0010Iæ\x0011¢wµ]­Û¹}Vûgæ7µ_t]tmºW{MCæYÆQ\x0004\x0019íp:\x0018KZ¬F½Êí£4ì·\x0017Ûg³§½îmûË½õäåròùËîéy5{ºn9ËÃã£7÷÷§\x0013Ýj{¶Í6çQ\x0017û2\x000f2oØ\x00161hZ	!2@\x0004®ÖA :t·% BHÐ\x001aÐÝZË \x0011Ãz»ùé§?ùüùY«Ì\x0010FÐ\x0011*RÄ\x0014Ý®¯ÏÖõÕwï\x001f¾ñßü;ÇÃÉËó\x001fõñÓG_¿|öõó'OÏOn·\x0006@Í2k×n./~ýµ¬·«_ùè×/O~ùøÕçOOæ>L³§6µ¡æ´u#d¦ÌÐ
Iêò|]u·jÞç½±\x001cD\x000e!TÑÛ®»Deî\x0013íÍãÁéx\x0010G\x000e\x0014Ù¾>}õôôäxÛ\x001cÆÉø÷?x{ïþîÎû§ß{¹®2\x0016\x001c°m®\x0006Ý\x0006´&´@#@D0\x0008\x00101d\x000c#[D\x0008Ióòü¤÷«Ó1õ~ï|z´áîþA.\x0007³Bu8b\x001cäá\x0007\x001fÃñäé×?»]®Jª</p><p>V\x001d"\x000e"Z\x000b³1ÈÊ.ÑE®1\x0010MD:\x001c\x000fÎu´ä Ù×WÛz\x0011UÖË³\\x000e\x001cÎ§£Úéxöþ7íÃoÿ/~öúôÅíru}}¶îÓï-\x001f>xëË³O\x001fýöwÿ`?\x001c|ùò¢;½y{rÿøÆºOûÜÏG§óe,q00 Ã¾íö9uÓcLÃ\x0012\x0011ºK×4çÕº½ë\x0017ûöÉÜÕþÌ|½\x0018:R\x0017a\x0011D\x0012L9BÚ\x001dFûþÛï­ûW_?ÿ\x001fr[uÜ1\x001e\·Ëå[×íÞu}ðñëôñËÅ>¹^].7c9x||ãÝÛ·Nç\x000fß|0ðëÏ¿x}yµ\x000cîÎwryÔÑz}5ÅX\x00165w:éÒ
´ÐR\x0004î\x0012 T\x0010Ý¢ÓÒA\x0006:t5D\x0008ºén)m»ùóÿäååY7Cw«.$V"¦ÛíÅù7·×b\x000cµ=»¿¿³­«ívqÈÓ¡,\x000b¢´F\x0008°ÏÍåò´lb\x0000\x0000w\x0002IDATjÛn~þù'´eÛËm
/¯«}h¹¤¹Oºõ,ºÕ,Ý%¢äxp^Î"B÷D1d´ÛÖ~ýzQBä°<,ºK÷´m;®j¶}ßms5÷·ïÞ8\x001f\x0017\x001déx:;ÞvÏ¯¯^^."n\x000e£ï?ÜûÿÇ¿s^Â?þë\x001f|zº"e\x000ec°¯ÓE\x001c-"d¤9,1XÆ0FZF\x001aeX\x0006iä\x0010\x00112Ú\x0018a\x0019ÃEf {Wsnç#÷÷w\x000eÇÌÆád,G\x0011ÈÅx|ãñÝ\x0007\x000fï}ùËï=¿~Q3,1to¦¢Cw«.\x0001ÍÐZté*m7Æ\x0010]2ZÐ]Bè2Ú²\x000cçÃ*sßÌâåéõv\x0015eq>v\x0018í°\x001cäñÎñt'³»oîÖÕz}õåëW_?}4çôý7ß8Þ¸\.Ö×g§ó£ãá¤»µ°\x001cO¾ûî;¢\x001cÅápt\\x000eN§óýÑùî¬ªýòó'ëÓ\x0005Sw1é*êbÖ«¹¾êõÕ¯öùlîÏjÞ$RÐg³RÅ²ÄÉÈ4ÆÙÂEäEÕ³Óâ\x0007Ç»ßøõç?x}ÙÜæ[¯ë§ËÁí:ÜÝ«\x001cýá§õéógÎÇ»ûG÷÷\x000fÎç\x0013¸Þ®^_^¼}óhß¦ðpÿàîtt<,:Oúôhtëj_W©ÒÝH\x0011è©#\x0004h4\x0002!2¶DÐZ\x0008\x0011\x0001BhÕ%î\x0016hëzóõËgÛ¾én¢UªÒ $2èB·ízõ\x001cÓº­>}üY\x0004sn\x000eËp<m{»\\®/®×]Æ°,ªr½n.Ý¶í¶}£ZÆPÒlºéj\x001d\x001c\x000e\x0007}f.\x0002U»ªÖ\x001dÒpww\x0016\x0011Jë\x00081Bã¶·O¯ZHo\x001fï1t±­SõjVÙçnßvûÎã³Hæ¾Ëåèþ~±­Óº^].¯Æzóöþì¿ü\x000fëÝÛ\x0007ÿò\x001fýúéÉº5j¶¹O1Êé´8\x001e\x000eËÑápp8,\x000e#%ad\x001a#H9BF "hjN­@ ÍjÕÓ­Ã,QÌÅrXä c:áx\x001aN\x000foD~pÿðè|ÿÆáÏÿäùëgªu
Ñ­çTZ5!d´®©º¨2zX\x0007©\x000c­j\x0012IÐMQ¶}¥ZWs7¯¥12Ý\x000e7Ë\x0018ÎK[\n¾Æ\\x000eN\x000fo,cXÎî/_¿¸ýú³ðáý\x0007§¯¿úñÿì7û?úîß8,Ãéx4Å\x0018iä9NgwwwNwge¨*×gìj¾¨ý¦êªöWsÖóUÔªkeÞtL]¥"\x000e"\x000eãY,!ºÅ|±Ä\x0017\x0019\x0017ÙSÎf9Ëë<ú×??ùðáo|~þÏ~ÿÇ¼¬<¿¶ëíÕÛw\x001f|ûWßéÞ¿{ãxHoÞ¼u8Ì9uOÝeázy¥Ë»·\x000fÞ¼¹·Þ\x0016Ë\x0008sî./7§ãÑé´ëjté\x0004ÝÒ\x001dD\x00084t£\x0010B¶@\x0008ÖÝ 3*-D´}ß|úôIf #tî\x0012hzê.U-"0¤E(so³Ú>K\x0015\x0011¥«è\x0012Ýtk­»u}î¶¹Û«T5M\x000b³Ú:7sî\x001a%Ó1\x000f®vÚí\x0015B\x0018ÑlíÒW=iÜße¦î6;d\x001clU>?½Æ;K\x001eP½Û÷2çê°\x000c=[ÕÛ¾9\x001c\x0011aDZÆÁññÁr;øúôÑåòjßw§ãÙßÿÍo|ÿí7~úù>\x0013L]e,Î'çãÉa9\x0018c\x0018 \x0011!ÑjÕÓìÖÝºJW©</p><p>Ý¥´êÐbê#D¤TF¶\x001c!³dìt«\x0019nÛUo\x0017\x0019Óéñ½ÓÛ\x000f¾=Ý¹ûÞÏøG_þ=['ë¾³oÌICs\x0012@O*»ÖjÔ:C&s_\x000eËbî®\x0008¡6«l½Ë­1ôÓÂÛ6u\x000ec¤åñ­ãÃ[÷ÛîéëG·×¯^ÐÛYS\x001eÏþî?ý\x0017oß¿w\\x000er,Æ8\x0008Ým$¦ÛËgÏ·¯^_~õùÓ¾~´­7Ý»ª«îW]W£Ë\x0012CÆ°×TÝj¶®ÖZfÉ\x001cÆÒNw'§ó{Ña»üÑvù®/¶j³\x000e¶zpÛ\x001f½\¾¾.ÖÙ¾ÿáÕåúà_^Ét<Þ\x001bKx÷áÇÇ{_>ööÍ[çÓ\x0019lÛÍëåU\x0006ïß½u>Ø\x001eÎZùúå\x0017ëºêYÖæÖöµÜÏ\x0011¶ÛWÛvÕ=¥¢S7\x0011\x0001º[7ÐÕ ¢E\x0015dXD \x0004@\x0000\x0004ÝD iºy}}±HCfªª'A\x0004ÐÕö}</p><p> R\x0010"\x000eØ\x0016I!î B\x0005Õ­ªU\x0012\x0008ÑÌ*sfµîÔ=Å¾ºÇ1¦îÍÓ\x000c\x0013\x0012±Y®×F\x0004÷äÐ å\x0008:í5}~¾Í,Þ>Þ\x0019\x0019"\x0006ÝªÊ¶îz¡­Xp>,NÇáxhF:\x001e\x0016÷ç{fÙ¶Í¾¯Nç³oß½ñþÍ½/_ßx}y±¯7Ým,áp<8\x001c2Dèn¥DµlºÛÒJtÑ­»Ð"ZäªCuh»ìÔ\x00112\x0012Bæ0F(\x0011,¶bÛVõõu]-ç\x0007çûw¾ûÝöøþ;¿üá½Ï?þÁúúÊz³¯an\x001bÕ"\x000e\x0011!s\x0008Ù%j7{ÒLD§\x001cÃeDJ­ºF\x0008Sè""tíjnf\x0019\x0007µ®Ö}jáë§nëêÝ7ß9\x001f\x000f7z_ÍuuùúY\x001dj[õÜ­'ÿñ?ÿßüð×Gõz³í¯öõ«}ýj®OöËG××n×O¶íF\x000cG9Nq4·ôÔµµÙçnÎ)a\x000c\x000eKZFÉÃÍáxt8\x001eDÞë.ëÕåex¹¤Ëzï²Þ»ìw/íë×'Õ/®õÅÃã½ûÇ÷Þ¼yðÃ·ß{yyV½ûúôÉóë§¯ö}\x001a1Ðä°¤Ún>¿>Û¶hÛ­d¦4·rÝ¯Új½Ý»?-¢Õ~Ó³´&\x0008nª¡\x0001D Bk\x001dA·¥\x0005Ñ\x0012­4"è\x0006"\x0008]¥»éPÕD\x00080kª*jsNûÜD\x000eeb¢é\x0000:¨Ò]\x0002\x0011)\x0010Zè¦!\x0008ÕaÖÔ\x00152Â,fÑEw«nÛz¡w\x000fÑÖÚ½6³\x001dd\x0018*¸]¯¾(ÝåññÑá°è*Ì¡#lûîËóUWszópr<\x000e\x0011)´î²íj\x000e\x001dÚ¢kSs\x0013\x000e"	át8ÈGëÅåvq»^Esw÷àÛ÷Î\x000b?®Öu§è\x0019*R\x000cD\x0008A´ÐhÕÖ"\x0002Ñ"\x000eÝ¡ÈEZÌÙ:é\x0008!#Á\x0008D	d\x001cì±\x0010a»¾º]¯z/÷ßÿÖ\x000f¿û\x0007ßüÕßøéÿèÇùß¼üô\x0007[=BÏ¢[d\x0008¡0uM]ÐR5K\x001eÌ}SX\x000eT\x001b\x0011r\x000c{m¶©÷¢É\x001cæ¶ÞU\x000c{2·²\x000bÝe]_­ûf\x000cÜÝ;-Gß|øàËç._¿êóYÎÍ}µ½|uyúâoþáWËádßnFÜ,ùÌüdnOfÝtoÔ.ê\x0005\x0018NÇ;Ë8ê.ûÜí¦2¥)s·vXÒ\x0018d0¨¡ö¶miÆÑì¿âüÚ]oÏ~~þêëÓ«¶\x0011i9\x001c\x001c!cJÓ\x000fß|ë°°ÝÍýêåùÉO¿5Í½¤!#hµ¯®ûª»e\x001c©µ}ßíÛTûT5å\x0008{¶=Ê0õª¦@Ä\x0010I5\x001ah\x0010\x0011\x0008@î¶D\x0010M\x0007\x0011\x0001@\x0007Ñ@\x0010#u7\x0015JË¥\x0010H{µ½</p><p>è6«TMÝ­»µÖZ££\x0010Di­\x001bB"Ð"È`tH¤¦[ÍF#Ñ4U¥zê.ë¶{Ù¯ÇtÒ\x000e\x001d¶\x0019:(EL#¨l·ÛÕ¯¥º½}óÆ8,ª	!3aÖôt¹jmVyûxç|\x001c2B	°Í]u©>éz¶®2+N\x0018éGËñä¸¾q¹<Ù×«v>=ÜÔ|çË×'Û~U</p><p>h\x0004\x001d-:¤¡ÖÐ@\x0008¡u7\x0011RÈ\x000c-t·e\x000cÝè&ÚÈ!2Ù"nºI´6´ïÓ×/àáÍ\x001bßüÕßxxÿ÷ß|ë/ÿø¿úùßþ»Ûóº­æ¾\x0011M\x0011Zh\x0019)ºU·î&Bç´ïS\x000b\x0019¡#,9t\x0006Eå´m«}¶ö½Ô¾É(µ·­[Ç°\x000b\x001dCw\x0011íõé«y½¸?ßûæo|óþ_×\x0017ëë³17±¯zî~¿ÿW?ýø'\x0002\x0015\x001e\x001fï|øæäÃÅy9¼·ÕÅÈ«\ZU*i\x0017V5o¶íIÕjäÉ2R.»ÑSFLå`­½îU?ªõ­¾ÞÙ;\x001cGïßÿÆoþêÎ§Uüê\x001fuOÓAF.zº½<H·.ûr\x000cCU\x00191\x001c\x000e\x000bÕºwªd¦1BD\x0012aî»}îº[\x0017c,± hK¶9oºK5­¨ÐÈ¦£D\x0004BwÖ
!\x0002\x0002,\x0019!:\x0000Ð"Bd ´\x0012\x0011\x0000º\x001bÌZ\x0019Ks·í9§}ß­ÛÍº­¶my¢!Ð"Bd\x000eî\x0010h\x0011D\x0004 \x00112\x0010\x001a\x0011!#	º'f+¶é\x0010Sæb\x0011\x0012[£[tënÑ­mÛ½¼¼È\x0008ñøèx<Ð!\x001cC7m/__nªÃû³óah¡Ì*óvµÇp<,f±ÎW÷urw>9,1\x000eÇtZÒõúd]Wûms<½ÿðÎùîÎç/OÖí&¢EN\x0011°H\x0010BdênªIB¨JÑ¥5Ý"R\x0008¡EÒ\x0011º®"\x0018#e&\x0002\x0006¢
\x0013e¯\x0012\x000eFu¿ùüù£Ó_þèááÁÃùÞñ·ÿÑñðèx÷ÁÏÿú_½~úY\ÂÜ§Ê\x0016Ñ"\x0016\x001d¡´ª©;Åhf«:SæZU	ME#ÚÜw\x0019edÐ¥gë(sb\x001cÈÐû´^®jÛe××\x0017ß¼güð[¿þùOöË³Û\x001cfmns:ÜV!]×éãñè_þÝo¾q·\x001c,ã$zs8ÞÜ\x0018SXéÕÜKäPu£®2KôÁÈa9<X÷áº-¶z°ÎÛÖ}ØvôWU»Ó!Ü^?ùr>yy¹èyñpw0+PUj\x0016=Ñh\x001dat\x0018i9\x001fp\x0014Ð¥ö]Õ¦zj­»Ñ"RÅñp\x0014ªË67snöY:Ò\x0018\x0011Ì\x0015Õ¢¦£UÓÝ"\x0013-"\x0010º\x0000\x0000\x0004K@ÐZ\x0008\x0004\x0011\x0002\x0004\x0008ÐQ ªEp>\x001dm\x001b×W>öúòâë×/.·ÕºnÞ½yôÝ7ïi"R4¤\x0010të¢²Ð"h\x0004\x001a%"D¤@w\x0013AÐè¦ÑÕªÊÞíÚmÙÊÃaXÔ:¨\x000eÙ¡+T\x0014\x0008û>½¼¼ªnîÎg\x0010Z\x0004-­[ûò|³míÍýÉýéà0BDÓ¥ÛÜ¬ÛætZ\x000cýÊÜyóxïx\,K:\x001eïÜÝ-.í¶ê*ex÷öÑùîÑÓóëõY÷\x0014\x0011\x0002Ö 3uCS¡î\x0012\x00112j¨Y:¨Ð9D\x0010\x0011\x0000hÝM·\x000c"ZEËnÕm\x0011z0k÷é\x001f¥éÛ\x001f~ãxºw|xôíßþ'ËÝ£§\x001fÿàÓÿÕëÅ¾QTn\x0004\x0011!#´@«Y"1SWÙç¦ªÌdîMµ\x0010"(©,¢.Ý-ªÌ9åá ¥¹·eIUÓåòâr>y|óNÎé×?ÿÞz}5÷Í¾®öuwwÿAmÓu^áç__Ù®Òý8º;1òÁÝ·a\x001c¦E»oEüàòüÅeÝRíoÇ7^Öö|Ù½^§§ç«Ûí¦fi!3-\x0011^³}ùøVº\x0002)\x0004\x000102,ã G \x0016U¢WQ!GXÅÝÝi[§1mß|ùúÕ¶ïªË¾Oû6íû´îÓ¬\x0012ÃÑñ°h©öM­«¨]ôÔ\x0011\x0012-´ \x001bD\x0008 \x0002Z7U%2,\x0010\x0001\x0010\x0011@\x0003\x0011\x0001 "d¦îFj\x000fwgëax~z¶Ý6\x001fýäóÓgÛ6íûô\x001f¾ñ7ÿî¯\x0010B E\x0010\x0002\x0016Bf@\x0004Ý\x0000tk­AF\x0004îÖÕªJEØ:½\x0016\x0019\x0002£[ \x0003\x001dZÓÔ\x000e5ËõrÕMD¸¿;éN"VUfMëªé.­=Þ\x001d
Ð"BdØ¶Õ^;q6òèvªU·oïÝÝßÑ'ç»ÛåêõõÅz»8F;O\x000e§·.¯'ÏO¯æÜÑt\x0008\x0000"BDª(Ýn\x0011!\x0012\x0011º\x0008024 ºt\x0003\x0010h¡«\x00042Bwà e}õÓOôùëGoß½÷öí;ãpòÝïþÁßýÃöòñÏþõÿüÿøé_ÿ»ëÏ¬W!\x0016"ÂTæl]edªª\x000cUe7ÍJ\x0011è\x0010ÝD[04ÑºKbh³6*ÁIÐ®×\x0017#ÛÝÛwÞÏòË°^^\x001do7ûmÕ{Û
·Úe\x000cÏ9tÝ,Ûj\x0006u:\x0018cj÷ÞüðF\x001e¶íÁþr§]/wn·Íåº¹miöÛ¶©.sNëu1%EH4:Ef@´\x0016\x00112Z*\x0011M´îbN³vÝ»D\x000e¹/\x0004çÓ\x001d#Ó\x001e\x0007õ³¯__ísÚ÷©@ æ´¯W×º¹ÝÝ(Ø-Ñ:B\x0008m"ÔA</p><p>Ý
"\x0012\x0016\x0011 ±\x0004\x0002"\x0008 3u\x0007Ý\x0004@ \x0001\x0010"Úñx°,ÃÜ¦O/_üå§_|þò\x0019a¯r>\x001fÕ," [\x0008\x0011(\x0002DÌ@\x0003B\x0004Fwk-\x0010\x0011ºKÏVÕfMsßu2Ü*¼\x0016Ç(¡d§nZ«&»\x0001MÈ\x0004ëºz~z¢Ûýý½Ãa!Zõ¦jêj« ¦Y¥º=Þ\x001d\x001cÆ@£	hë:-¹;Ömúåã'¯×«\x001f¾ÿÆÛ·÷F¦ÃHÃðôõÉz»êÞ,Ç{o\x001c{/ÏO.×gÝM\x0000Ý­»u£QSÏMW	\x0010Zë\x000eÑM\x0007\x0008MÌ$hèÖ\x0002IÐ\x0000\x00121B7¡tPÂv½ø|Û\¿<;?Üyx÷ÎÝ¿õWýÿôïÿþ?ù·ÿö¿ú?ÿ×ÿ·_ÿøoÖË«Ú§è"JE!EÈ0çnVÉN{ÙSu«\x0008Õ%±D8dX24ö½E0FÊ*=w­E\x000fQSTêmsë){§Ãùí\x0007ï«}úËï]//b¾±¨<¸nõºz}¾s:\x001ejªùl.ÔëyýÁîï¹{pÝÂº?ÛëÅÓVSuÉ</p><p>Õ\x0003a\x001cÂñN;$\x0011BK-4B\x0004´FaRSuYfMÕSwk\x0004Z*\x0003A}+×/ª>ÛçÔ\x0011ªÊåõjÛ'ÕJ©.ë¶Ú·Ú¯jnÂ´D{8\x001dóA\x001cBg\x000c!"IF\x0004\x001d*\x0018hè\x0006\x0004\x0001è¶@\x0004-Ð"èn\x0004\x0011"\x0000 Ð "t§\x0014Bê.C7s ¨¢@ Ð¢[G\x0011)\x0008\x0004\x0000\x0011\x0001\x001aU¥ºUÐ¦jÚgÙgéº&ÍÞÃu\x0018-¢fWJI©»UÐ"B&Ûí¦ªt··oßZ\x0007:èU(5§ëdÎ6g¨noï¤«h\x0008!mûÔnôõé¢ê\x0013Þ¾9Y\x000e!s1òäõùÅõöbëÕáxp:\x001fD>hÓåòª»DîÖÝªJWë*]M7B5\x0011´6\x0008¢\x0006¢L\x0019¡#@7 #Ð\x0008\x0011Ú\x0019ºZ\x000bÕìûÍÓÓæùåÉíõê¯þýï|÷ýwþáú½ûæ¿üáßüå\x000fÿæÿúÏ?þ¢÷Õ2Æ"ÆÐQZ\x0008Ù­;Uµi7È!cÐTÓZDªjÝ-Ð]ºÙ¶T2¸iÇ\x001aöàêÕ<ãã£\x000fÿîw~ýñG¯fÿÅ¸{CÌõây»º\x001dNÞO\x000eËÑíö*.?Ùjw{û[o¿µwÐ¶,ÃHh#RÆ\x0010BD\x0013%Öhª©V5uíª¦îÝ¬©«t·®©L"µ@j¡v¶½íµÛ¶Íz»Ún«mÛÍÚu4Õt¡ÂÔ]ºÊÀ!\x0018§t\ÎNËâxXä\x0018D©¢¦è#¥\x0014¹ D\x0014¨n\x0010\x0008Ñ)\x0002Ý\x0008\x001a\x0004\x0001\x0001\x0000\x0000D\x0004è&"d´</p><p>"Ó\x0018Cæ\x0010\x0011"RDÓTµ\x000eD \x0010"R\x001bD\x0008 ¢\x0011\x0008¡ÑªKÕD#tO­T·SUÕºCDèf-`d\x0018ÁÞmVÌ\x0014\x0011"\x000eU-¢e&Ø¶ÍÓÓ\x0013xûö­Óéh9\x000c]«Ú7ÝmeÞ®æçÍ¶¼¹;;,CÕÔµ\x000bI´}²®N'ÃÁëëÍ\x001fÿô£õ»÷>¼°d:\x001dï\x000f^.w^^ÕÜe°\x000cÞ>Þàåõ¢jÓN]¡jMw\x0008)\x0016\x0008!\x00042È\x0000\x0010Af\x0010©\x0016H@\x0008\x0008\x0008D\x00041¤ \x000baoÖj{MÕéëçöýj_¿úßýÎoÿýß»ÿßþÝÿà¿ùgÿçÿïÿë×?þº½(Mª)\x000cê]×N¤ÖºÒ\x0018C\x0006ìªÛÜ\x001bt·ÙÌbV+Ð*Øµm\x000cµCVÛ'Õ\x001cïîåù\x000fÿîÞl~ùåÏrûêx8\x001b2Sï7¯}´Ü=È\x001e^×ÕíöânIÇ{\x0007!»¤\x0011º[2¦PºKÏ]ÕT³¨]×¦9Ë¬]u\x0005\x000bM\x0008!!3´0gs·ï»}ÛíÛn]oöýfÎ©jê¢[`$!d¦\x0010Æ8</p><p>%£¤\x0010F\x000e9Ò2\x0016Ë\x0008cIc\x000c³¦¹¯ºJhidÊh\x0019¡Ö\x00024 £è\x0010\x0016\x0011 @4\x001aD\x0004 uC\x0010\x0010"Z\x0007Ð2C\x0010</p><p>¡}¶\x0000\x0011\x0001\x00141D\x0010AD\x000b­;tÓZU³UµªF(ûæ,UÓ»}/U­\x0010Í6F¡«í5\x0005F\x000e4Zê¦»E0çôôô¤»½{÷Îù|yÒÝjnº¦ÞÛeß¬ëÍåzõöáÞqÐs7«T\x001deÑÝnëæþîì|:¹Ü6üÓO®×w¾ûö»Ó""Ü=ÜÉe¸Ý®t\x001b#õ8ñÎX>ÛÖ]t\x000e .!$\x0011F\x000e\x0011D$"\x001a@f\x0008-E¦ÌEFH¥U\x0017Ý"Cf\x0012a¡ªÔMv[ª¬³mûnöêòtõçßß\x000eÃï~÷;ß|xïÍ»wóÙñþÑOø[?ÿù®/_Ìí¦{\x001a¹\x001bc\x00152ïïN¶\x0019~ùõÕz+sºJwS¥ºÌj[±wØ\x0010ºÚ¬r»Ýdîz¦1WÖÕ¶\x000f§{çÇ\x0007\x001dáô\x000fÿ£q¾÷ã~ïryq\x001c\x0011,Áº\x000e/ûjNeqwwï|J\x0007¯ª¦îivÙkª*U¥»t·eîSwén!D"pÒ\x000etss3÷ÍÜ7sîæ\Í¹étÑ¥»,X\x0006½Ì£Ì4¤)FH\x0019i´\x001c\x000e2mÛ°\x000b4FÈ\x0008\x0019) `\x0016[§</p><p>\x001a\x0001]ºÚ4\x0005d@§\x0010\x001a]SKa\x0008\x0010Ñ\x0004@\x0008\x0001h\x0011¡\x0006!F\x0008E4È\x000cI¦\x00102Úu]E1T@\x0008©E´BÆ\x0010\x0008PÍÌ=Ô\x000cs¶î©»íûnßwsNU¥ªTµî@h4ªK4a¦#tµSf\x001c¢\x001b¡»E\x0004ªòüü¬ª¼ÿÞýÝ1Næ>ÕÜuïz¶®\x0017×\x0017\x000fçóñà8JÏr8ÌÔÝ_^lëôøð ùì¶n¾ÿöÇÇ{z3rº;\x000f×ëªf;îÁr\x0018ôõË³õºêÙht¤è\x0010r¤Ìt@@\x0010-" Ì°,)s\x0010©ÑÝZén\x0011!s\x0018#EêVnUa©¶/lënÝw¯O7ÿø¿¿xþòßýÝô»ÿð\x001f<¾¹÷ñÓ'?üí?xóýßx~ú*ææxà|¾ÉüªæTs¡Ó>yûeõåóÅåõf}½Ø×Ú.Öõfn«ÙuÝìU\x000eÇ\x0011ìÝTS»%§½¸Î`\x001cÄ^ãÙéîÞátçxÿÆßýÿä¸üñ÷ÿd½½8DÉ\x000cs\x000f[í^æÁéáÁãý{û>=þYÍRÑfÑ\x001d\x001aÕèÐP\x0014nÐ(ºUê*17=§ª©ªt·vH£å!1DCÉ\x001cÄÐ\x00112ÓÈÅÈ!GÊ\x001c"BD\x0018c8\x001e\x000fªÊõzÕ½é*ºE\x0000è@lÝ)3Uh\x0004
M\x0004\x001d\x00014¡\x0001­\x0008ªÚ\x0012\x0011\x0004¢e\x0004\x001dº\x0001ZD\x0008¦\x0011A\x0019-"u\x0017d\x0014B7\x0011áv]}üøÙå·ß;\x001c\x000f\x0008\x0001ºî\x0016Á2Â\x0018aVÝ¶}ºm»mNÛÖu3ç\x0014Ñæ¶m\x0014Qt\x0003hi*\x0010.0\x0008ª§*"\x0016¢\x0008\x0010\x0011"Bfên¯¯/ªZ½ãñáÎñxçZí6ÕÜÑro·ëÍËëÅ{oîKªnÃ\x0010\x0011¢ÓuÞèöðx/søüõÅºí¾ûö\x001b\x001fÞÞÉ1Ô,Ã°®ËõÅñxôp^Ïïï\x001e|ùòäåë\x0017½\x0016½\x0008\x0019r\x0010\x0011Bê\x0006 "D\x0006\x00024"h!\x0012BT9K\x0004!±XPÝ\x0008­uMUÃ<\x000cÛ^.·Íõúâÿé¿ùøËO¾~ô÷ÿðõýoüùú£ÓÃbí³ýv\x0014<\x000fÛþêùõ«§çWÛ¶XÈ{ùøÞñ¸\x0019\x000f7snj®NÛÍ~{q}ùª>ÿj^^\x000cSÏÖc¡Ck5Ù«T%\x0015ìWóTOo\x001eßº{xt8ýÝßÿ½ï¿yç_ÿñ¿úøËÝö¶\x001bjßì\x0013\x000f÷ÆÃ{7¾®Ö]º©nÕtè¦&]Ú\x0014]BÓBd`\x0008\x0011\x000ccI$2\x0008\x0019\x0010"Bf\x0008\x0016"\x0006\x0011b,å ªÒ¦©'5wÑ\x001b5u5Zw \x0011"R RT!\x0004J	)\x0010ADj\x0010tkÐ\x0004¢u·PÆÿðùÛÿ\x0005\x0000@\x0008\x0011D\x0006@\x0008ÐZ74¨æùùâùån:Ì}·ïeYÈ°Ï©µî¶Ïi]7sªp[wëêåróòòêééÙ×¯O^_].\x0017·ëÕz»¹Ý®¶mUÕ"BDè¢ºh\x0010Ú\x0012\x0008ÝÌ\x00082\x00112C\x0004§ÓÉ², "@fÊL\x0011\x0001h5Ë¶m"Âé|c±ï»}ßì³Ôl³ÚºOÛ,s6BF Ì\x0014Á>§mßåHãÑmÛ¼¼¼X<Ü?8\x001c\x000e(lÛêzyvXÒXÆñàîþÎáxR\x001dæ¾Ì42D\x000c2Sæ\x0010\x0008)sÈHad\x0018KAfÊ\x000cc\x000cËH9Â\x0018CF\x0012d¦BLc98\x001cr¤È\x00109å`,\x001c¡»½¼<ûñ§\®\x0017oß¾±Þnö9¶n\x0017×Ûmo³N^®íùõ¦¡ª¬ûjÝ®¦\x0000"Óáx´\x001cOb9 ôÜD\x0016Ý"BwÛg\x0011ÄÐØ×ËËWÛõ9íëÕö»¿ú+?|xo»]}~úª´Ãùäá÷¾ù÷¿óøá{Õeß.öíbn\x0017½_Ø¯²nXe_\x000c«%6ÜÆt>p>¦Óq8óqq:º;\x001eÜOÎ§£Óéèx88\x001e\x0016Ãâp8\x0018Ëâp8\x0018ccXE!3e¤Ìc\x0018#ÕömSû®kê.5w]Ó»®©»\x0001!Ð\x0010äXf¹ïª&\x0008\x0011!"\x0011D\x000cÝDC \x0003\x00112Ò"\x0019ºH \x0000"P\x0010 \x0014t«J´9DÐ\x0010¡\x001fúÕm]}÷Ý\x0007÷Þ½yðæÍ#ÂóË\x0013Êñxt»m_}}~õôôâz½¹®»mj¶®V]ºKD\x0018Ù2\x00182SFªT£\x0015:@ ¡0Æ¢»Ñ2Ù¶2Æ\x0010\x0011"\x0002@F\x0000ÁºÝ|þòÑ¬éíÛ·\x001eÞ¾\x0017ÏéryQÛ®ºEukO½©\x000e
\x0016}h\x001c\x000b\x0011¶}÷òòª;ÜÝÝûîÏ?}´íåïÞ;,'½íÆ`\x001fáó×gWÓÑé|òîÝ£û»{~9xúúIÍh\x0011@\x0013-#E¤\x0008"C \x0011\x0004\x0004M4Ñ2CD\x0010m\x0019T]ª¦\x00149\x0008"Bæ\x0000\x0011m6\x0008Ë¸s:.^^\x0017/ÿþÿÕ×/,Ë½­\x0016Çó·oùòåËååp'£eìæ¶Zo»«}ß¬ÛÕ^;³ÌnÕÌj\x0007ãá\x0019C­\x0017=oºW\x0007\x001d!»ÔÜe\x000e!tËëÓù|g¿<y\x001båû÷ïü¿þçÿ»Ç7÷>¿<ûðý÷Þ÷ó7ÆØeOmYBæ\x00111d¦H*JH)iD@6Z\x000bÝ-:4R hZknn\x001aÐnÑRµÙ÷]í; \x001bÈL]¥\x00014B\x0007 \x0010©;ÐMGè »u\x0011C\x0004PB\x0017\x0002RH­D7BDX "@\x0000@\x0008\x0002!ÈPÕ #t6ED\x0008¡"d\x0008\x0004:´Wùåã\x0017¾|µ,éþîä»o¾qwwïó¯.\x0017Ë\x0018ºÛ^åvÛ\¯«}/Õ­B µF«lÃH"BfÒ%¢5"\x000c¢é& D\x0013\x0011àv[Í¹Û÷r:N'@#D\x0010D\x0010mß§/_¾³}ûí{oß#ÇâòôdßWÝÌÂÞ.·M×N\x001d=ÜÑÍrhc\x000cÃ>ÛóËUWº»;©~üùWËÅwß¾s:,ÄÑá°\x0018KÚ·Íz»R»q\x0017ÎÇ;ßýð½ãiñôõ}Ýd\x0011A\x0012\x0019\x00021BD\x0010¤ hÖ]ª\x001a-\x0003Â \x000e\x0015!"Ðº¦Ù-\x0010ËÍÐ=RX××þø\x00071\x000eÓ½»7ïÎ\x000fÎ§;·ëÍ¶¾ØgÛn\x0017Ï/_\¯\x0017µOÝmß§mßÕ¤9Û^mVéYj®d\x001flå.§\x0011SÆ42,Mdéq4Æ"r±w«ÛÕ¬íêSp\/¾ûá[ÿÿò?ùe]åùä|:;K\x0013CJ#CD\x0012D$Jën\x0010RkÝSWS­+´VÝº'ÐDÔÕ\x0000:\x0002MPÕ"\x0002\x0003aÖ\x0014]ZûN·Ðªé"2©ÖM# Zu\x0008\x0019CDjtC</p><p>´@ @D D·n\x0010@\x0013ÚBFjÐD\x0008-\x0000 \x0011!&\x0010!*¤PQ\x001a\x0011D&n\x0014\x0008\x000c5Ûu®×g×ëôøæëåâùåUW»;\x001f½{ÿFÄbÛ(s6{én­Aw\x0016$ºCL\x001a\x0011a\x0014AkÝ\x0004\x0008\x0004\x0008û¾»Ý¦9§9§Ì2Ch\x001a\x0002\x0004AÕôôôEwùþ»o½÷%\x000f>Ù÷U£µu/UtoªÓÃ\x001d§.½\x001cÄX´éùõÙ¶ß<ÜßL\x001f¿|±î7¿ùá{o\x001fßÓ«x8Ûör»\­·UF8\x001co¿çÍÛ\x0007~}òúòLì2É\x001c\x001a\x0011\x0010\x0011D\x0008\x0011
"¨jº@uè*%Æ BD\x0013iÔ
hZëF4\x001d2f¨\x00109\N']¬Ûê²­ngËá,ò`]w·m÷ñãW¿üúÑËëuÛÕ,U¥gUª\x000bt\x0017A</p><p>\x0001\x001a!º,cÑ!¢ÍmÚ·¶ïípà\x0018©½</p><p>LSïæõvóryv÷qz÷áoß¼µÞÃ\x00085ZwSÐZk¨©Fwh\x0012\x0011ºZUéj]­5èF@\x0013\x0008ê¦[D D\x000cªKHc\x001c,ËQ\x0017ëzUµiÖ\x001ah\x0008º\x0006îIw©.#\x00171\x0006"è&"\x0014\x001dd</p><p>©Ñ\x0008@w\x000b­\x0015AD\x0008Ýe\x000c!Ö\x001a:@h
\x0008\x0011d¦î&LQ-\x0004Ý"\x0008\x0002\x0000\x0006\x0008îé¶n<¿¨YºBU;ïüýßýêòoÿö\x0007//7ë¶»Î«ª\x0002­\x0000\x0010È\x000cc\x000cs)±í</p><p>\x0019!:Ð</p><p>\x0004\x001d 5ZD ÐU®×«Æ8Ñ\x0008\x0000\x0001ÑºËóóîòÃwß{÷î\x001báËOæ¾ ±\x0017Û®»Ty\x001aÅñÈ\x0012A\x000cÛºêYÎç1\x0016O/\x0017ýÓ/Äðáí£e\x0019ÚîpLq²ÞVëzq¿\x001c\x001dOgoß¼ww÷àÇ\x001föòòY+9RDèZîÐ
D\x0000ÐMDé\x000e©ìÔQt`Vén\x0004BU«.U)bÈH"U'\x000edËÁñ\x0014b,¶}³mëv#ëV>yñÇ?þÅ¯\x001f?Ùö\x001diD\x001acXÆp^±,%,#F¦1B\x0004\x0011\x000e#\x001dF\x001bÊ¾N××¯_¾¸ÜV\x0019iYÈ\x0008\x001aÝ*Ó¬¶öæº¾º¾¬µÛMüö\x0007µ,®-îÖD\x0018:\x001c"Bw\x0010 BwS\x0014ª[ n\x0004ªéV\x0001­LzÊ V\x0010%sq<Þ9N¶íf[\x001bD§lfÒ2S\x0006´FCAvÑ\x001ai\x000f2Z\x00084è Gh\x0008"Cu\x0010\x0011"hD´Fk#C`L	tR-ÐD@\x0004\x0008"B+\x0019t¢ZD\x0018\x00152ÒT\x0000"\x0002t·HÝív[é B »»óùä_~u¹lB\x0008\x0011¡»\x0000\x0011!"Dî\x0006#ÌTUDhT·\x0010B¨h4\x0011©£D¦ªr»Ý1d¦ãá \x0000 [D DÆËó\x001f«ýðý÷Þ¾ûÆX>}úÕÜnrhª¦ëVú²Õî*è\x0010Bv³\x001cÖ}7_¦óÝÙ²\x001c<?_üaû£í\x001f|ûÍ\x001bçãâphçy7¼¾\]^_-#»·ï\x000er|ãçy~új\x0014¢©fO\x001dA£iÐ\x00002@\x0010Cä®#µ1D\x00061Ð\x0015\x001aÝ¥Ð"[æb0EÄ\x0010y°®Õr(ge]¯n·9ËÃX¸ýÁ·ïÎºÊÈaä°\x001c\x0016Ë2dÌ\x0010ÑF\x0010)#@æ Û¶¯ÖuuyÝì5µlýì²îzÓF\x0010BvÉyeM·>øxãz]eÓÛ\x000fF\x0006y9\x001crãÀXD$¹\x001c"BÔ$\x0008\x0010MW\x0008#Ô t£[Ï6÷I\x0014ÝZ)S+©LËñàxºccÞ©\x0002ªíÛ\x000eÚ4k§KDØ'sß±ii­;\x0000¥+\x0010@Ð"\x00189t¢è.ÑA7\x0004¡\x0011\x0008]!",:i"CH\x0015-´\x0000­#Ð\x0008\x0011\x0010ÐZd\x000eÝD\x0002@\x0000\x0000º[Dè¦</p><p>JD\x0010áõõÕþô'ïÞ¿s»ÝÜn7û^ª</p><p>D\x0004èn\x0010\x0011DÖ"BD\x0008Ál¥tÐI£\x0011\x0000Bh!#t\x0004X×Õår\x00118\x001d"\x0000 \x0010B\x0007­¼^^ýå§|ÿÝ·>|øÆñxôË/?Ú¶UdèfïRk\x0011SuÐ¤Ã0äÂ0«½¾^\x001dO\x0007§ãÁí¶ùÃþäùõÑ\x000fß¾õÛï?8?,Êîp\x001a¾|*_l]Þ¾}ëáþ ¿çñáÞÇ}ýüÅ\7ºTLU-º B\x0004ÐMd\x0008Aî\x00141\x0018CwZÆb\x001c\x000eÆ\x0008\x0003À\x0010AG\x0008@\x0008c	1BG\x0011`d:\x001dO\x000eãÅºmºÛãÝÉ7o\x001fìÛ®k§! ¨h\x0011I\x0017 »AU{¹\o__]®7×ë´W;Þ-#ÌÛÅz½Ø·²D:dXr¸jÏç{7ï,\x000foÕûwîø­ó·¿5N\x000fr\x001ctÐMÇ" \x0010\x0011\x0006D ¡CDÖ"\x0014Bæ9VJ7\x0019I\x0004=r\x001cR\x001b\x0019NÇÃrPM7¡TM¡tMû¶éYn×\x0017¯¯Ï2Ãùtç°\x0014*Ns¶m·ÏÕ}»Øn«}ßÌ¹µèØE@÷$Zuë.ºdî\x0016\x0011B\x0008´¦ÛBë\x000e@fèn\x0016"BF\x000e\x0011\x0000¡5¦@kD \x0008 \x0001\x0000\x0000BD\x0003d]7ÿò¯¿wþËO®·ÍuÝè\x0000\x0000\x0010\x0011 ÐR\x000e¢¥\x0010h
ZÑD\x000ec\x000c1RfHD4$\x0002\x0000Ø¶Í%BF:\x001cSD\x0008\x0010@æÐ¸Ý®~üé'ÕíÛo¿õýoþÊ/?ÿd½^E$Ýö*ê\x00001\x00069\x001cí\x0014c\x0011\x0011ª¸^WsîîNf\x001fúÕåõbÎð×¿ýÞÃÃYÉºÃõu:¦û»ðþ»ßúþ¯þÆ¿üÓ¿øñ/v»\ô^º'È\x0018@\x0010h=!\x0014Ñ"IGEÖ0{I.\x0008Bh@k¥ªT2í³í³tÐ­a\x0019¶tX\x0006Z×ªªT3ç®«µT]ªZWª¦«U¹ïnÛîvÛÜnu2ÓýýÉ2ýºÚÖäáÎv½¹¼^t~xçÝ·ßúðÃ\x000f¾ýí_ûðÝo=>¼u8ÄéH.¢SF«h³ÙgÑ-2,¦\x0016U\x0004î\x0006¢u\x0011H\x0015!"¤aÄÿ <i,K³\x0003»µ¿sUõ=3ó&<ºl\x0002\x0008\x00148 ÿÿ¸JRÅ\x0001\x0005 	Dïáá=U½gs­\x000b-¶6f.ìx>Îng¢Õ½íóD­DQDÂdl³C·l¨ÇýÎãru;Þ¹Þ^\n7Çõ*Çuè>§ûãîþöÙÛýÍçO=§§ÇónOç¹=\x000fçy×ÇÓ>O{ºê¡Ni\x001dQB \x0010@«*\x0019$¨\x0018IQ\x001a1	*¢Ð\x0012@!Ø¨­ Ï\x001f>~jhIi\x0001\x0000Hb$´Ò*ZXk	Ò§Ý§5ãv»:.\x0017Ý[m\x0014H$D\x0012I´õ|<|òÉV·Ûj+"A"báq¿ûÃ\x001fþàñxøÍoþÎo~ó[úÃï}üéGmÄx<OÉHÏO2z<\x001d}\\x001cÇÅdiy»ßµ§×wï­ãÕ·ßýèãÛÿÏ>ùÇßþÊW_^Ý®/Þ½ÞLn¾ýî/þòí·¾üâ\x000b·\x000f\x0017_~ý÷?¿zÿõ×~÷ßÿÅ·øì	\x001d»$\x0019IUÅ\x0000\x0008\x0012S÷,Û]k\x000ef!Úíì¶÷öÜ§6ÎÆsoç.­5qYA]e-¤\x0012\x0012º·ªfÛ»62cÍÈÞ©öp\x001bñ´ÕËÕ»ãæc\x001c3&sÇ§Ïoq{ýÂíåËí½×÷Þõµw_|åöòêr½I´:xÈ>M·næ<³§í4¶Øö>\x0005{oí\x0006í\x0016\x0014-ZYãX±ËiédÙ»Ï§ó|:û¤§îê®ª	&4\x0000DÂdÌZ&ã1kdÆ:®ær³Ëõêr¹XÇaÖxyùàz{/s1+ãâryq¹\$q§Çãáùx¸ßßÜßÞÜïo»£J+\x0019ED \x0005"@Q¥ÕV\x000bc&fD[ÐF@DAÁ\x0006-\x0000\x0004A\x0004\x0014A\x0001$ÑV[\x000444´©\x0011Ç±L«OöfïZ\x0013ËÅy½·L\x0004\x0012I$\x0001Ðòx>x¸\.\x0000@7óùôç?ÿÙÞõÛ¿ÿ­ßüö\x001fýá÷¿ó·ïþso\x001fOçÞöyzÞ\x000e·ër9·Ë®Ëq±f\x0010÷çiÿôÑëë«××÷~úø£ÿüÿý¯þö·¿ùþÍ?úåÏ¿ðr­¾øâæþxõ?ïÑ_þjdo¿üæ/ßÿ[ÿ§?ÿéÏb\x0018\x0015d\x000c\x0010\x0001mÁq,@M¶LÌÄxZÆÌØbî8\x001b\x0015²LÆ</p><p>»Oçù\x0010Û©51]ÎýÔÝºZb¬Å:be¬uh·ª\x000cZçYÏçv{ÖóyÚ%³Ìqu¹\]®/æxÇåwËÍº¼8®7³.}n=Oo?~´÷\x0013\x000fkÕ*tÖùÜû¤[{°\x0006ÐªÚÝ E©(¨Ù£û\x0010QuóxnÝu§óùÐnRA\x0010LÈ\x000cN]Z$ì\x0010Î²C[{V\x0005\x00101s¹9¬5fÆÌXë0³d\x0016\x0019f\®\x0017ÇåæryñòòÞíõÕíåæöróá/\x001dÇÅäµ$qH\x0000(UId\x0016 (Èì:³eÈ¦
D\x0010$\x0010BT\x0001\x0010IhQI@\x0002D[Ð@\x0010ÉÈDDÂà\x0004±[÷û]E\x00123£$ÚSB\x0012\x0000I\x0008\x0012ÏçÓ§OÁõ¸È$@i-cs×_þògç¹ýã?þøÇÄ·ý\x000bÆ½ë~>ØÛÆ£ÜvÜöC7×Ë58»}úüÉõrñúòÞ§?úý\x001fúìÿòïÿ­ßüúgÖzl\x001fÞ¿÷|òûßý~ü¯¿üÒL­#~ó÷_YSßÿí'=· "\x001aªjI*d\E"a-m²4±2fÆî8wí]£Ò­{{>kæ4CTU\x001b³Æ:^¬Ä5ÖZf\x000eÁdk·só<Çã\x0019Ï3:ËõÅíõ½uya.dÅ\x001c"º·v{|úèy>=\x001eo÷»ý<éir:V\x001daML\x0008\x0012¨so\x0015I%[\x001b\x0015;Ì0ª\x0001¨ \x0002¤´dÌ:<ÅÙ-\x0013çyªm­nQTÕØ¨ª	\x0012IH$´\x0001\x0006³»4¨¢­}>uNñL$$#\x0006uîmÄ:\x000e·wÎsu±®W±$cÖ2ë`µ\x000eÇõâH\x0002\x0000\x0000 	(R\x0002$JÈ\x001dmÈ\x0004\x0001\x0000U</p><p>PI´\x0005\x0000-\x0000\x0010!´\x0005\x0000\x0005U\x0004\x0000ì}:[\x0015dF&Úz>ãp\x001cqîÓyl03\x0019I$q§Ï?s«Ûõ&	(¨¨d¬\x0015çÓ·ßþÅù|ú§þ'¿ýí?JÆ¿ýÇ³ÖÏ§çÞ\x001eÏÓy;äeÌd;:ãÐ,½=o.ÓËë{ë¸úöÛ\x001fü¿þ·ÿìÇÿìïó3·+9ß¼9äoüðã'úó·¾øâjf»ÌøßüÌßÞ½úöÛï¼=b@ºUH\x00043ËÌØ»X3fbfdF°÷io²È\x000cSJö\x0016\x001b[÷Öó´Ï»íÄnÇ1Ër¬8nË:¬ãb¦dÄdd¢ÝÚF»X7ÇõÅu½ã&×YËÞÛÛçÏî\x001fßÏ§ó|:Ï§ó<õÜÚÒÒítÚ­É¸¬Ãq\x001ds3Éa·¢&E­\x0019ëÍyÞ%ËdìsÛÝ\x0012%¶´\x000c	U\x0010!£9$ó\x001c½Eèör=tªû\x0014HiQ»[B\x0001T\x0010\x001ai0Tµ§BI \x0002¶ÉÈ\x000cbcR»\x000f?~ÿ£ÇóéX\x0017Çq1yá<<ïwë¸Xëô|ç©q¶5Ë\x0001\x0004\x0000´\x0004\x0004I@Ä4\x0004É\x000ch(Rh\x000b -\x0000A\x0003\x0000 (\x0000\x0000\x0014$¶Ú­\x001d&Ö1f"³dÆ¬Ã±\x000eÇqHbïÓ>Q\x0000öÞh+¶fÆyÞî\x000f3Ëår1\x0013\x00140Ú"cÙ{ûþû¿ù¯ÿå¿øçú'ÿ÷¿%ñÇ?ýÑ~nÇXîÏíÜOç£ºÇ¬\x000cû¤U2Øowçyzy¹ùòë¯}ÿÃOþßÿÛö§¿üÂ¿ý7çg_\½»\x001eÿìk?üø£\x001fþöÉëëÍí:Vê\x0017¿øÒ»\x000f¯þðÇ¿øé§Oö¹-53\x0008a\x0012XÇ\x0000ª­IìnUTÅ\x0008e÷ÔÒníé|>Ï§½ÄZË±\/ãr©ã`fvÛ;¶¥\x0019ÉÅÌÁºéñb]^¬u#Ën=îw¿ÿÁçO<î=ß>ë>Ù\x001b4Lb&RºÚÊ:¼\nf\x0018ËÞ!£
af\x0004ÝÛq\Ý^^½½ñÅ\x0017ï<\x001e§·ÏoìÓÞ§\x0018ÁÌ¶@	f"³È\x001cÞÞ\x001ej\x001cÇ²Ï§X×åù8Ï'H¨ÐM\x0015\x0005-T\x001aÄ.M¤\x0001¡uî ÎsÛçVµÖ2³t§îR^n/®«u\¬µìóa-f6}lË`[\x0013Àv$Ñ\x0016$\x0001\x0000m%\x0011D\x0012D'²Grj+\x00133\x0008\x0012Ð\x0002A\x0012Ð\x0016$\x0001J\x0015@\x0012m\x0001D[\x0000@i\x0005I$\x0001I$1kYkYÌ¡çé<Om=OçãÉDD\x0012\x0000D\x0012ÄÞÛç·Ïàz=L%\x0002&%,¬,gêÇ\x001fô_þÛñ\x000fÿðþî7¿?üág]%âÜõÖÊýi}^¼F'ö}Ëº[e2àyº?ïÞ½¾úú\x000f~øñGÿí¿ýïøÿø\x001fþ­úí/]ç´\x001fw¿øæKÏç\x0017>}ú¬êúz5¯¾úàv»ùã\x001fÿâû¿}ï|>Í0¡`DB\x0012\x0015mIµ'%mïbw\x0014{oçyÚçö|ÞÏS÷&ÑYö>=OÅóY,3\x0017ÉÕÌÍº¾Z·÷æxuÅrÛýñôøøÉýí£Çý£ÇÛGÏûSwÍÄL\x001cGL\x000eDÔÞ§î­¶frÉárÝm ¬0SkÅZ5£»f-çÖ×wf=|ü|·.79z>E´%´´¡c&ÖZ.×9^üøñÍó¬\x0019Îç÷Å±\x0006Ëy 0¤\x0005-T[-U;U¬.¥â<·çó¡=\x0011k
\x0013çãiïm&1\x0019ï?¼J"Ì¢ÕÄZK\x0013Ïç)¨h\x000bznÝ\x0005\x0007$\x0004@\x0012m\x0001lµ\x0004A""\x0012 !ª\x0008¶h\x000b`ï-¶\x0002Ú¢Â.h\x000b\x0004\x0002\x0004H\x0002ZZ »h·ö	ª\x0016­½·ãX2\x0003Ú\x0002h+¶Hbïúüö\x00197·ëM\x0002\x0004\x0015)°V0>}úäÿü?ÿO¿ýíßûÍo~ãz½ùÝï~g§EËãÉOO}Yn\x0007cê\x000c\x0002Î]?þôw/7_|ñ^V|ûí\x000fþËýï¾þú\x001bÿæ~mßôù§ï½^âÝ»\x000f¾ÿñ\x0007?üô\x000fïÞ;\x000e^_.~ý«o\x001ck|÷Ý÷Îç\x0003µf$°%\x0019É\x0011uOÝ0­ö>µËî¸?\x001eÏ§ó¹ÝïwçÖ]Y¬Ë8ÜÜWõÎº¾:\x0017¹¼³æ\x0002Ý\x001e\x001fÏÏ»ìóÜzìJ·k9!QLbf\x0014öS÷¶»uo0C2.ÉÝ\x0011²bïìeö2³doµÈØ;tãt\x000f·ÛÅ±"¸\¯\x001ewºOIH\x00184fÆÞÛÛÛÃÑ«ÙÚ\x0007j%ºëñ8õ8¬uÁè>\x0015-»ÕÒVË>OmÁ¶mµ²¥§îtÓPÖ\x001aëú"$ÉÈ\x000cBv«È®sÎ½ÍZÖZìÒ¢(8h«­$\x0000\x0000\x0000" \x0010$Z\x0012f\x0008ÈM\x0012m\x0001@\x0012mDÐ\x0016@\x0015Ñ Hh\x0015Q\x0010\x0001mµÐÖÞÛ¶uÓ½Uµ@@(ÅÆ\x0002\x0000@\x0012mÁÌ$öÞÞÞîq½\$£J+!\x0002¨µB\x000eûýu§_ýê×à÷ÿãwÎóé2LíÍãQ\x001fû´ÏÓ¾-/×pnçYI$c\x0012Ïn?|üèqÞ½¼sY\x0017ýö;ÿËÿúÿðýÿíÿî?üûãåýøôãÅÃ\x000fï}ÿý\x000fþø§¿øâý;_~øàXñòrñòzóécõ|a­eï-\x0004a«ÝmOÏ³ÚØª¶vé^Î.Ïçéù|zÛóÜÎ,ËÕõrs¹¾º¼¾º\_¬ãfÖEÇYçç7ÏçOz>õ|ê~8wï^ä8|~ûl·:eGKºíóÔn[HTÍ2	+`2fâ\x0018fÆ1¬\x0015§xZNÙ}ÚY$\x0008ÙîoÝß>ÛÏ»nr½:.Ëãqj+%3\x0006	É¶ÏÚÏow×/ÕÅçßYa­q6Þî§çsË<Ö¬e·ÏS[=·î\x0000	X9$1F²Õ¶d¤KAd</p><p>´bÛª¥"\x001dI$£{ÛçIëÜ\x0005×ËaÛ¹+\x0001\x000eE\x0011""´</p><p>¥H\x0000B\x0003\x0011U	D2AAJ\x0004´\x0005\x0000P\x0008\x0005\x0010-\x0000
Z
PÕV[\x0000I\x0000ì]mµ\x0005TED</p><p>Ð½õ¬¦h\x000b\x0000\x0000ÚJ¢­$·û\x001d\/¬5ª ¡eMärñx<ýë¿ü«ûÛÝ¯~õk¿úõ¯üñOô8OÇ\x001a+çé­§Z¨q»FÍNQüôã'çýôáÃ;_¼ÿàÏýÿåýúö/ßù¿þÇv;^¤w}|ör9|\ü÷ÿþ;}yçË¯¾R\¯Ëä½ûãaí&£âyÚó<=ÏÓó¹í²R\x000bK6q9.ëãf]_].¯.ÇÕÌEqO÷Ç'{ÿ¨Å®:E%¬9]ÖòîõÅÞõùó'zêù´wuW÷F­aE\x001b	Áq\Ì}	kÆq9Ì`oÇÄ</p><p>
B¶¨¦à\x0004~úhïíù<µì·íååæz¹x»¿Ù{³kf$µ÷¶Û\x0016Ûvßu\ßåqÞ\x001dkÌñx>y>¤\x0015±ÖHbµ\x0015\x0012v\x001d+f\x0016&\x0004Å®</p><p>N=+s\x000ch·$b$\x0019Ñso{C(»[[°2ªöãa'ëÅníç)å\x0008L@DÐDJSTD\x0012\x0014\x0010D\x0012I\x00040\x0019É\x0000­´ ¶\x0000\x0000 Z\x0000 	­"h"­</p><p>\x0005\x0004H¢-H"\x0014EU\x0004\x0011\x0012D[@A[\x0000I´\x0004@[$ÚºßïÌÅ$\x0012Z\x0002ëåð|þø?z>O?ÿå/üò¿ò¿üÙ>OY\x000b%Ç\x0019yDÅeÕôavÍ:¤KÑ]?}úä¹>|xï¿üµ¿}÷½ÿýÿÿøóÿèßÿôË¿}÷|¾iÇåzõ§¿üÕ·ûèË¯æz½²Nuñö6îo\x001f\x001dyjëynç~êÞçioz\x0006#\x0013\x00123æ`¬µn2/ÌÒ,ÛØ»Þ\x001eoìÏö>µÛ¤fXY2\x0014Ý]µ±=Ï§¾ÿãzuYQK'Z\x0008h7ÝÚ-Ø-­5\x000b\x001cëp¬1©$cÚÝ\x0004JØØ&ÌPºO?}¶\x000bìVpîír\x001c\x001e§½OéØè®´&yJOzzw9Ø#ÏÏ.+^ßßì^ôÜ²·½·½«­I\x001ckìÍóñ4e65Ú(¶l$â)	É°Æ\x0008¨(Rb$ìÍ©&#3ÒMk\x0012kF÷òòrsÿô¦ÏÓ!\x0011\x0000E\x0004B7		\x0014\x0001\x0000mA\x0000\x0011H  \x0001Ú\x0002H\x0002ÚJ¢­\x0008J\x0001¨R\x0002
ª\x0008 ­$dÄH¨ÝS\x001b	\x0000I@[\x0000\x0004\x0008\x0004$\x0001ÐV\x0012I\x0000Öãñáz½H\x0002¨¶\x0000`&Öq8Ï§oÿògÇÝÏþsß|ós?|ÿ½½·ð<\x0019s\x000e8Ö!N{oÙ\x0008ÂÆÇÏo\x001eÏ§/Þ¿÷õW_ùt}ñ§?~ëíãø_ùÙW¯^^\x000eÝ\x000fë8|øðÞß¾¿ûÃ\x001f¾óîÝ×CsàÕ¬q?jvé\x000e$&ä\x0018ÉÒÎ\x0005\x0017Í!ÇM«ö°Å~n»\x000f»§Ø&58\x0012& tÛ­î­{$Çã¡­¢¥-*\x0008*Ö:\x0004éiïJÆ.k××W·ëÅù¼;Ï;¶ÝÍªh£Ý8U³Ù´[ÏSw\x0015\x0019Á~<Ý\x000f#1«³Å*Ë)s:\x000e\x000b\x001e\x001eÏ<Ë9.ë0³±7Ïçv>K«Ýtë¹m[YÌ("Ö,\x0006	%È>íÒ"lä=C¢\x0019fYk\x0019±±Ìr9.Úz¼}ö¸¿é>Íây^oWóÂç~rd¢{\x000b\x0004è®\x0011@D\x0002\x0004H\x0004\x0000 \x0002(\x0000\x0000ÚJ¢­$P\x0004h+ª¶P"Új\x000b¨$\x0000\x0012Z\x0012ZZh\x000b\x0000\x0000\x0000\x0018#\x0000\x0000\x0000h+	h·IH´u¿?P×ëÕÌ \x0000\x0004hEf9Û÷ûÎy~ñË_úâË/}üøQ\x0012k\x0006UÕg£çbÛmIï\x001e÷b\x0010;ìÖyßöù÷çöáË\x000f^^n¾ÿî;ÿÇýW¿þÕW~ñó/½\ëz,//ïÔáíqúñ\x001füøãxýðäp=\x000e·Û\x0017âáã§\x000e£
©\x0013[C]í^$É8wy<pÒ*\x0006+ÔJ$uO=«	 $ÖÄ\x001c$$]vë~¿k«Ýö®¶D\x0012I$Ë¬¸ÌY²®Ö±|x÷Þõrøüé']í"µ\x001bZ{\x0017\x0008m\x0011±ÁÌD[Q³bfP)ºMN\x0003JIb·4&´§>N=Oslçóa\x000fºí½íýtÎi&½Ù'ç®]Òª\x0001D\x0012Ð\x000c3bTu/YËÌ2Ça]®Öåj.\x0017k]d-³âyf-×Ëã8ì]Ïûg?þä<ï\x0019É8K&ë.÷»#\x0005" 	EhK"\x0000h\x000b$º+d@[\x0000\x0000\x0000I@\x0012\x0000I@[ (\x0000Ð\x0016@\x0012D\x0012\x0000mÍD\x0012mA[\x0000Ð\x0016$Ñ\x0016\x0000Ñ¢\x0000@\x0012m%\x0001m\x0001Ñ\x0010\x0001Ýõx<%q½\Ì\x000c¡»\x0002*H8.C~øÑÞõÍ7?óúújïmfì½íl[µç2Ãõ¸èºÚÏ»Ì\x0012hÝ\x001fOÏ\x001f¾÷Ø\x000fß|õµ_üò\x0017¾ûî[¿ûÃ}~ûì«/.~þõÏ¼Þ\x000c//î?üþ¯>~>}õõÏôÜY^_Þ¹nî?y<Î.gæ*½hFg\%)»ö\x000cÆ$&Aíg\x0019ØeÍA"YÖZÖ­v·îÚ{ÛÝ</p><p>\x0014ÈÄ1\x0019IDÉ\x0008 ahëÓ§>þôtÿüI÷	\x0002\x0008$ILjBZ\x0013\x0006ZJvIdoV[-0C[-X¨ÑnmÝr\x0002-ål#dik°µY¬C2e}n5ËÕq¹ZÇÅZ¶vÆ:\x000e³\x000e³Y#kY%F\x0013\x0005umí]8a¸\x001c\x001f\x001c/¯ô´&blìÖóqãâH ÚJ"	\x0000IL¢J$Ò\x0012ÈDBDK\x0002\x0000\x0000\x0000\x0000´\x0005D[I@[ÄÞ\x001b´0\x0019B[313\x0000\x0000\x0000\x0000$\x0000 
b&\x0012\x0000 -$\x0000$ åñxJãv»¦\x0014-**µ\x0016?ýdïíg?ûËå*Æq\x001cö~êf­Yx¼=½\Þ±8ïRÕl=ã§\x001f?rnß|ý_üâ\x0017~üá\x0007ýö\x0007çó»§5ËËëò÷±{cnÎýY³=Ï¸^¿rî\x0017¼ñ¤gU´LêrÄ\x001aÎó))%b2\x000c3ÑÌY®ÇÅq\ìsëYÂyÖÙ­»L¬Il±VR\x0011Öi\x000b*\x0006ÓmïÓO\x0019ÏÄd»Øf±&´J\x0018$5è¦ÝP\x0014 Z@Q(hQZöISm5U\x0005»\x001bÌ,Yd,±®\x0017ÇõfÖEfÉ\¬ËÕ¬eÖÁ,\x0012\x0015D[vebÖ2ë\x0019%	"\x00193!£j\x0008¨h\x000b@jBRí¦[±32\x0017u8[\x0011EÃq;|õÍÕ\x0001D\x0012	I@[m%$D\x0012IaW²%\x0011¤\x000531\x0013ÉHC¶¶\x0000\x0000 ¶\x0000\x0000\x0000\x0000fF[ \x0008IÌÉÐV[I\x0000´\x0005I@[I$\x0001D\x0002¡#$ª\x0000HB"!"$\x0000lÏÓZOëEftW\x0000</p><p>À9øôùó/ÛW_~éz¹yÿá¿û»¿w>îf8»	?ÿÙÏüá÷¿÷ã÷ß«ít>&L*\x000bbïúøéM÷w¾ùÙ×¾ùú\x001b·ëÍ_¿ûûýÏ¾þê½/Ëw/.S×¬\x0017÷{ýßýÉçÛøÅ/~i-ÌÅõzñ§}ÓVÂå¸XsØ­CfhÍZÚÅÉ(&#³d.æ¸8ûýÍ¹OÁÑj\x000b¨	Á\x000eM$1I$\x0004$DLâTZÇd$\x0011¥nIQDZUB"\x0010JS»\x00120¶ÒÍ>Q-D\x0013-22#d¬cãb«\n.×«ã¸Ê:dee\x0012\x0015ÍD[ÅnuD[miA[Q\x0010)D\x001a{\x0000U
A\x0012\x0014(UÄdØ\x001b¥FCvA\x0015µ\x001c-\x0004ÕV[I$\x0004\x0000\x0010\x0012\x0015	ÝÕ\x0016Ö4´¶\x0000h+	$Ú\x0002h\x000bÚ¶\x0000\x0000h«-ª-hkï­¥»v·½7H¢-¶ ¶öÞÑV\x0012ÐÒ\x000e!¡-¶´* \x0005\x0012@bw{Oïo\x001fÀÛÛBH£»(a\x0012ÇZîootûøýìkëX~úqûòÃ\x0007·\x0017?|ÿ½óqúægßx¹Ý\¯~øÎOßÿÕ~ÞçÃ>·\x0011AË§ÏwúË_=§o~öÛíâ/ýÖ_¿ûÁù<}þø/?¼z}y1ùäv»øå/¾ñ/ÿý÷¬¾ùù;×ÛÍýñ`×Z75.«ËíFÌ\x0010ã0ëE2vÙçÞZÖåp\x001cWãÐryÓ>µLB"b&fÆd$\x0008I,A\x0019fÆjP0!	\x0014\x0011\x0011@[U\x0010DD°»5@ (QíÖnZ°;\x0006 µ»5cÖa\x001du\¬ãê¸\x001cf\x000eYYf-2 \x0013RÑ!b\x0017-h"	K\x00101\x0013mµE\x0011iµ\x0016´õ<O{Úª</p><p>@"]\x0004hX5t*¥¥V@µq$´ÕV\x0002$±÷\x0006\x0004´\x001b#(H¢­"\x0019I\x0014\x0001\x0000@[\x0000mµ\x0005\x0000m\x0001$ÑV[\x0000mµ\x0005\x0000I$ÑV\x0012Um\x0001@\x0012m\x0001\x0000@\x0012\x0014EP²%\x0011\x0003\x0000\x0000´\x0006¶ ¨}n///.çãa?OØeC½O///þÓúOþãü\x000fÞÝ^Üwüã\x001f}þüæ\x0017¿øµ_þò¾ÿá£o¿ûÎ$2c]n~þË¿óÍ7¿ðxûìù¼ûøñ£ûÛgk¢=íóôÜõ×ï?9-ßüìK¿üõßûë_¿óãçÓqûàÓóÅ~\x001b·ÛÅÊÛ¯ýÝ?ýÜÛs{Ë\x0007YW3ÛqlÇ»9\x001cë"ë¢3`Í\x000c,ûÜÝÚj\x001dã8\x000e	÷ÇÝ~>é %HH±«=U%µefhõÜö\x0019\x0012I´ìDD& Ý$L(D\x001a\x0015\x0015)2S\x001b @D\x0003DHdu,k]d-ëXeÖÈ,³dQ­v92ÝìêD\x001d- Q¥5\x00034\x0001É¶; `Í8ÃZKÄÌ8Ö õx<ÜïwUÝ§Ý­¶Újk\x0017¶´¶Ú\x0002¤´\x0016P\x000e \x0012H\x0002\x0000 ­$`ïm­HH\x0002"¶"bdF ¡Ñnm%\x0001mA\x0012\x0000\x0000D[mµ\x0005\x0000m\x0001\x0014\x0000D\x0002@\x0012mµ\x0005\x0000\x0000mA\x0012@ÉV\x0001\x0010\x0001\x0000@iµ%$\x0001T\x0012m}ÿý÷®·«ûãîÈ\x0008ªîuøú«¯ý»ÿéßùOÿév>î~ÿ»ÿáí~'ñúúÞïÿ\x0007ýî;?}6shë~¿{üít½\x001cÖÄ8¬ËÕ¯¿n×Ëár½ØçÓÞ[÷¶ÖÈõæÝë{ï¿úgçYk\x001dÖ\x001a+\x00159®¶x[^\x0013mXëp´ZÚ8\x0013óYÝÛxfÛçÓãq·÷C\x0012Äå8\ÃLe?´5a\x001dîÒ-*%"$\x0002\x0015\x000bÓÒjiªH\x0004\x0015\x0001Jv%¥´[\x0013v4\x001bEÈ¨H1\x000eÉÈdLF&:YuÌµdÉ\x00082#ÝR¨¤b$±TK\x001c$Z \x0000</p><p>¶Ðhk>O</p><p>\x0014IÌý)\x0013\x00113cÍ¸]\x000f×ÛÍqÜ´J-	Ø-è®¶ÚSwíV÷Vì½)B[ûÜÎçvîMë$\x0000Ú\x0002\x0000H\x0002\x0000h«-\x0010¶¨\x0000º7¢-h\x000b\x0000Ú¶h\x000b\x0000 ¶Ú\x0002\x0000Ðj«­$ Ú¶\x0000Ú$ ­$ -©\x001a-mµÕ\x0016D@[D\x0012ÅVÔ\x0008(Ò\x001a13~úéG?þTv]×Ååz\x000c >|øàï~ýwþþ·ÿà«¯¿öûßýÁ~>$üôñ××÷^^^çOÏ§ëõ¢ÈÄu_ÁZµÆe­qÌ²fÌ1.×«Ëåâ%$F¬µ¼Ü^ÌZÎ}zOQ=\x001fî»Î½9OQmµ!' 4±&màQçùtî§Q×ã8H¬Ä²éFHÌ¨Ýj¶¶¤(F&\x0013»\x0010Ì\x000cHF2\x0010"\x0012</p><p>\x0019225b1³Ì,Yf\x000cA#b2\x000c
-\x0015vµ§î-\x0013\x0012 </p><p>\x0019	HF[ë¸X3ÞÞîH"B\x0000h\x000b¶(¶P¶ ­îz>\x001f\x001eåóÛ\x001b?|@$$±µ$fÆZËÌ \x0007eïhkï\x0013Ðò|>=×ÓìjëH¢­¶\x0000\x0012Ñn	I\x0000$ÑV\x0012I\x0000\x0004\x0019\x00126\x0002\x0000$Ñ\x0016´D\x0012\x0000Ð\x0016@[\x0016Q\x0005Ån\x0001\x0000\x0000\x0000I´\x0005\x0010¡T\x0006\x0001ZmA[mA\x0012I\x0000\x0000Q\x0014	</p><p>@KË±ÆõvqÌr½Þ\¯7YW¿ùÍoüü\x0017¿p{yq{óùí\x000f¯/n×«u¹å¸\x001c.×½«JB"D,Ç\x001a3132!qî\x0008ÖDË¹Îót¿¿aËÄår±Ö¡âù|:ÏÍ®ìÐ»ö\x0004Å$f\x000eÛv»,x>\x001ffoµÆe	Æ\x00081+½·vk·$A\x0010É 2!a\x0019V$ÄdÌÄ:\x000e	IÌ,3#\x0019Ö$2!K²dA\x00141\x0010ªb$Á¨\x0008R¶ÚJÙSM´[\x000b\x0014\x0019tl´!Cê8\x0016bÖ		
H¶Ú\x0002ji+3\x0002h+¶FX´±wíM[ÐÖÞ<ÎM	\x0015ÉHÖd\x0000%Ñ½í]mÉ².#âH¢$\x0008H\x0002$¶$Z(ÈÄL\x0000I\x0000\x0000@\x0012\x0000\x0000\x0000\x0000I´\x0005
Z\x0000A\x0004\x0000$\x0001\x0000\x0000m%\x0001 U\x0002\x001a\x001am´ÕV\x0004HD¢\x0005R)vDQh-ñÍÏ¾ñÿÜíz³ëõÅõzõòúêõý{Éx{»{>\x001f®×ëíâýûWÇýðö8].W{×ãñ´[)I\x0008\x0019H$\x0004-»íé\x00013$(¡û´÷ér9\®W/×+x\x001csoûÜowçóiO}>ì½%ã\x0016uÚ®×«\x0011-Twm\x000fíYv"3Zö\x0019ZD
scYë°Öa\x001dã8Ì:Ì±Ì5KÖÈI$\x000cL$@@Ð\x0014Ô`JØE\x0011 \x0010D\x000cY@)bkKI+»Q[\x0001Z-QÐV»õµÆ¹ º7!\x0016\x0000-\x0010Új«E«\x0000P¨\x0016hi+!©¶´  \x00148Ï
Î:%¡\x0000\x0010		ÐFBöVq\x0010	m@KBÐ\x0014PD\x0002$E´\x0005@¤5H(\x0012ZÚJ\x0002\x0000\x0000\x0000\x0000\x0000h\x000b\x0002\x0000"	 (AI¢-H\x0002@\x0000\x0005\x0004ª¨ÐhCH\x0006Ñ\x0012aBÉ\x0010\x0010Ð QA\x001dëp9\x000e-ÇõÅíÝ;×ËÅW×ë³ñx>íóéÜÛ~nçYk\x000ekNãAO</p><p>µD&&d"SD\x0012\x0011n	inÁt\x001bTdoº]Öx¹^½»]]¯\x0007áz»È\x000c¸¿½y|þìq¿xÞïÏ§¶½·¨§m\x001e±Ïmw£`:Ö\x0011+£+²\x0016ë0k¬uXkYÇa.u\x001cÖ:ddYk¬µÌ%\x0013\x0012I$C\x0002" H\x0008\x0014ªj\x0007(0©$2\x0011Q\x001bA(ÐV\x000bU(Ta"\x0000U</p><p>\x0015\x0005ÝUuî­E¶åñx\x0002\x0019ABK\x0012\x0000P\x0004\x0004T\x0015\x0001¡Õ\x0016´\x0005mA\x000bµ7\x0000É6\x0013D2ÚÒ­­¶(* ¤"\x0003 	\x0000¨</p><p>\x0000¨ h¢Jh7¢-h\x000b\x0000\x0000 ­¶\x0000\x0000H\x0002´</p><p>E)tkk&Ú\x0000ª\x00026´\x0008)¢S\x0002\x0014mDÉ\x0006M41ÆÆ$¨\x0014jÏî®×»¯¾¾8Öá²×ëÅîÓýíîÜÛJmB\x000f\x001føÁ¹·îÓy>I\x001c±dÆ</p><p>\x0013&\x0011!5Ù´¢&\x0015¥U\x0015b×)´&qYËåîÓýíÌ8®7ËÕq\\//\x001e×WçÃy>ç©{ë®ó|:\x000fÝ§Ýe%f-su\\®Wë8¬ã°eÖr\x001cYËÌÈ,IdBF\x001a	\x0012¢\x0005"\x0002­$2\x0011´Eµ\x001bCCH`HF\x0012mI$ÄÐÈDwì½iµÑnÐ\x0016@[IT\x0015 \x0001@H\x0011\x0010¥Õ2h9[[mµ[\x0012\x0011B\x0012IH$\x0014A\x0012ÉÐjF] \x0001m%\x0001ÐV\x0012-3A\x0000DKBKK[P¥@\x0012\x0004\x0005D\x0014\x0015\x001c	m\x0001$\x0000\x0010\x0000\x0003\x0018t#\x0004\x0005@%ÌD\x0000m\x0001´\x0005\x0000I@[m%ÑBPmµ\x0004@D\x0015$%\x0000D\x0004\x001b\x0000\x0000\x0011\x0010\x0002AUi¤ì	%­$Òª 6gÈV¡Ì\x000415ËZµÖxÿzøêÃÍ¯ñµ¯>\É¶öÃÛÇ¿¹?ïÎ}e«Y©Ûýãµ\x000c£±Âm\x0012dLª=iDiuW»µ¥´[[mm$1×«5£­ûý
Lç³vCr8n¹mVB2Øöói§î
1\x00133Ã$$2cf$ÑÄÎØl\x0012IÍÄ\x0008ÂD'$"$\x0012\x0008h+$hiÙ{K\x0010\x0002¢­dK\x0002FLÑr[w	\x0011[µ\x0005mA[\x0004@ \x0001I\x0000´d¢Aª "hkf´D&H"H¢­´\x0004$Ñ\x0010Ñ½=Om\x0001´U´¥\x0005-D[T\x0002ÀL0dD\x0015\x0010mµ]\x0015\x0015DT\x0012Ç:ó~"(F2(Ý¨$$ÚjI\x0000\x0000´\x0005ÐV\x0012m\x0001$Ñ\x0016@[mA[D[ \x0000$\x0001I\x0000\x0000\x0000@¤@(¢¨ÚêÜ[jÈ ZSGã\x0018·c¹Ý\x000e×ëáåvñr½¸\x001eÛu¹\x001eu½ÛõâõåÅõòÆý²nv\x000foo§ö´Éaímå0IMJje$Lb¦¦b¶¢û´[-\x0005¥\x0004ÔZ\x0017Çå"3ÎsÛ¶Éhâô0Çére]±\x0012&FÌ\x001a³ÆdPZÂnµ[÷ÖÍ¶ís¶ÚPL\x0008\x0004bÍ!\x0001\x001a-Ð\x00161\x0013mµÕ2\x0013D²$°í½)E\x0002ì½\x0011\x0011ÛÔÌXë°Ö8Ï­{\x0018R{o\x0000I( D\x0012\x0000I\x0010\x0000\x0012U\x0002\x0000´\x0005`Æ@"	\x0010"`f@\x0012)I@\x0012\x0012	aF[{o\x0004\x0014ÐV»uÓÒnIÌD[ñúîU\x0012ÇC[3ãñx8OÝµ7»$L:^_oÏýÜ*¨¶\x0008Ð¢¢­ÌÐ¶\x0000\x0008 ÚJ¢-$\x0000 ­$Új\x000b\x0000\x0000h«-\x0000 ª\x0000ÚÒ h\x000b\x0000$</p><p>n¶Ú­Êp¬±ËÁëËÅëËÕËíp»Ûuy½]½Þ®^.W/·åv[.ÇrYã\x0010p¢&\x0011§½ÒÖÚwÖ\x0007¶]Q5ãX\x0019!S\x0013&0\x0001ìjh«­¢­î</p><p>öÞÚ\x00131¢EbÖáxyËMgÈXk9ÃZYËåzq\b\x001dCÆ$f"	\x0019ÉXk\x0019\x0004µwµe×Þ[»µÕ½Ð\x0014\x0011J" \x0008\x0000¥Ji*	Ø{$blD\x0012@0´¤öÞ\x0012\x0008ª¶zÖÞ[f$\x0010Ð\x0016Ì¶ÚJBB\x0000­$\x0000Z¨¨\x0002\x0000Új+¡¥­$&\x000c­}n\x0006Ø{k\x000bÒj\x0001\x0006-eï­-\x0019IlD[m\x0011D2f</p><p>fÆõzõ|>í½u\x0010\x0011§óyÚçF´PDfY\x0013Çûwï|þøÙÛù\x0010$´ \x0001;\x0015¥´\x0016´E\x0000\x0001É\x0004\x0000$ ¶ ¶ 	¶\x0000ÚJ¢­¶@K\x0008\x0012Ø\x001b\x0006´\x0014mµ\x0005@¬Ä1ã8Æí\x001a×Ëx}¹úò\x000fÞ¿»y÷zõáÝÕû×ÛÅå\x0018Çb
ke\x0019H*-{Ó-Ðj7ª\x001b­´ìýI2äfgLjæ0ëâz\x001cËÅ¬É \x0012\x0014ªØP\x0000</p><p>F'vcfXeÌ\x001aåúru{}oYËÌXkÌºHLDì}r¾aìÔÌ2³\x001e@5\x0002\x0019Ç\x0010X´U´ÕV[{Új*ª\x0018\x0019ÐÖÞ[[D¤$´"f
 "*Ø»¨di¶$¶Ú²K	\x0000H\x0002\x0006ª-¥Ê&h$Ú*\x0004\x0000\x0000h«\x0005Újkf¬5ö¹µ[O¶öÞ Ý\x0008(\x0004%h\x000b`ï
\x0004$`\x00121a&`ïíñx½·Ï>I"¶ÎsÛ» ­\x0002ZÎsëæøòý\x0007\x001føÉãñ´[-\x0019ª¦"\x0004Ð\x0019\x001bm\x0001PÔ\x000cRUJ[I´P\x0005@UBD[Ð\x0016PT\x0002D@K;Î½íÍÞ%¥ÅFMj\x001dãë/?¸^}>¼{¹zÿîÅ\x0017\x001f^¼½y¹-ï^®n·Ûey¹^\x001ckY«&¤±Ë¶¥OÓ-Ý"iÙ[²µ[Ê½7}ÚÝÚÄ\x0008©\x001al//W{®¶!ËZ\x0017Çåp\\x000e\x0019\x001aÝUT5</p><p>B"\x0013I\x0004+1\x0019É0Ã1k,3c\x001dËårXÇ¡D TlÌ.ØNÎ'HH"YfÌa­e­eÖ5ËÌHBH\x0002Z\x0014­¶½«­©ã8$Ñ\x0016u§}V\x001b°wQPlÓ\x0010¦ËdPÉHAQ\x0016´@\x0010\x0000mµ\x0005I@[{o[EPI$\x0001\x0000DP\x0005Ð\x0016´D[</p><p>Uçi­eïm[[\x0000m%\x0004\x0008</p><p>V\x0012\x0000MD@B2\x0008AH8Ï\x0013ìV</p><p>UÑV[Z\x0004LJ\x0000*ãÃ\x000f>|øÑ§·7oow\x0002Ñ \x0005nÉ\x0002QTV\x000b´hLF\x0002$\x0001RZ\x0000</p><p>\x0000\x0001VRM«ÝtKX\x0013kÆëíðõ\x00177ï_oÞÝ®ÖDzZ+®×Ã¯~ñ3¯·Å~x½]Ý®7cÄS{J±\x0012±V$%£óy×çÃRÇZÒØ*NÝ§­vNJÏÊYí¦[DÖuH¬ãõõúë;§ûc;Ö²nYdÌ:¬Y\x0008	\x0019I0$\x000c\x0012D\x0002\x0011#32ÄÌYÖZÖ\x00113K:ªÚjkïMkr\x0002Ðn0sJÆ§=Ëó\x0018YcfLÆÌH\x00183ÄÌHHH"	âX\x0001°V¬cY\x0013B[{o-\x001amû´÷¦µ[mQÊÞÛV0SI$\x0011\x0010h«EK</p><p>\x0002\x0001¶`ï
D2ª"$\x0004h\x000b\x0000\x0014\x0000h«­¶@«¥jï­­\x0011mµ\x0005k-3£­d$ÀVmµ%\x0000$\x0011\x0001\x00121 -¢Ò8\x0015'hK¶Ú\x0002´¨ Ý&#3××W\x001f>|á\x001fr¿?ìVZ@¤A4±[E0Ý\x0002 @H\x0008&\x0011¶Ú­9\x0005</p><p>h(;UU\x0015$1\x0013c\x001cÇárëe¹½\x001cÞ¿^}xÿêÃ»«/_/Þ¿¾øðáÕËípqÌ`«JÔÉ25µl22ËÌµ\åz\¬5[{ª²¹zz{ÔÞO+![Z»EÀî(d¸åX\x0017s\¬ÛÍõå½ËíÅq{q¹½Z«¹¼ËÍý¾}z{³Kf$#\x0019³¡\x0014It\x0017@\x0011\x0010Df$1Ycfµ!\x0015A\x0000@[mí½µ[\x000b´µw´µ÷Fµ5­ì0Lb\x0012efÄ0#\x0019I$äÿ_\x0010\x001c.K\x001dÜYÌg¿U§{fôa\x0002\x001cø\x000fApÿgdiÔ}j/2sssTêØæ\x0003î>W\x001eãóJÁÌì¾Ü;ÝÙæÞëÞk{gm¶\x0001¨T¶9ç\x00186¶\x000b*\x0015\x0000Ø\x0006*À`Y1m\x0000`mÀæn\x0000l\x000cïïoG\x0014°Ùfm¶s\x000eøÜëóý\x0001\x0001H\x00016*s¢rNrlSa&0@e8e\x001b\x0005¶ÑÌÜûñúúzûÇ_øëÏþõïùõû\x001b\x0000±(Ê°
8³±ff²±Íºn×õ1Ùf®9*5\x0007çÉs×ëñãýx=~~½üõç?ÿøá\x001fþá¯?ß~þxûãÇ?~üðóÇ÷ëñ|lWØ.ãÁs8å<Çç\x001cãåx\x000e§ã\x0000rióñ-û\ö±Í.\x0019'÷>>{t^<zy^_s|ó|y½ß÷[_o¯÷çëËóþò¼8ï\x001f:Ç)\x0007äõþò×ýýË?ÿù¿üç?¿}F¦{5*§#G''ê¨d*\x0015¥8ç¨TÎ9*pÎ\x0001\x0004*ÛT*Âf\x001eÆ6pïuï\x0005°Á0ÁuG»v:¶ãJåCÇîqï£¨£ò¹Iïo*ssNÎIqÎñ<\x000fëcØgî{¯Ïçc\x001bCl³ÍÆö\x0001\x0000°M\x0005*\x0000\x0015Á!Ñ¸\x0019\x0000Øí\x001a\x0000\x000cf\x0008Q¡
À÷÷·</p><p>À9Gå^î\x001d`\x0000 3uAp?Àé8ç8¥\x0002\x001c3\x0010îfml¶Q*P©×9ùãÏ?ü×ýÃ?ÿùOßo3	¬\x0010ÉTî\x000e-!£G}9Þ^g¾¾ÞNó¼\x001f¯Ç\x001f?øùóËÏ_þúãËüð?úë/?¾Þ~¼\x001f__¯×ñ~cÃæ Mc.Ñ9æéåUNy§\x0008.¦2lØ]vÝûqw}o~{ì¼ì<vâ¼t\x001eûùÓóó\x001f^÷\x001f×\x001f÷Ûóþò¼ßz^ÎóÖóÒyt\x000eE)VNRÂkû¨ë¿þñ÷ëñÿýóùõë·äC©ãô8çQ)Îy\x0014\x0003cÀ9©T\x0000*\x0000P</p><p>@!Ü{UÎ9 \x0002\x0000P8cGèätT:9ef}Àö±%Çd\x0011\x0014£RlT*çyT*ç¡\x0002B0\x0000°Í6m6 ²
Tî½ \x0002P©Ì$</p><p>\x0018\x0000bm`wl@±Am m\x0006\x0000Ø\x0006àóùF8Í\x000603À\x0000\Tmî\x0006QNQ^Ïùõë·{¯»Ù`B¥\x0002¯âý~ùÇ?þò×_ø×þí÷÷ÇE;p¢\x0001[æý\x001c§<çå9WÿÍûüßÎÉÿþßþòõâëëøùþòÇ×O__/ï÷ãýä9Ó9\x0012(ÎæÄS\x000e¶ë ¦}Ã1/s:<=ê0Ük÷}¸cË6w\x001f\x0017\x0013¾ôz¹¯/çýçÇ\x000fçýåýõÃóþÉssç­çz$\x001e\x0016[V&\x0017\x0007Ç\x001c(ç<r$û|t¿þüòãëñïÿíóh\x0007I\x0003rÀm6\x0018l\x000cQ©T¶</p><p>\x0000ÃØ(À\x0001\x0015 Lå£²
9\x000fç\x0004 °£BL¦AÄöÁl\x000c6¤"\x000c\x000eï\x0002Ns#ÝÙ®{gÆ\x0018\x001a°\x0001ÛT¶©T¶©\x0000T</p><p>cÌ\TqÎ1lsï\x0005
\x0000\x001b\x0000(l\x0000`\x001b\x0000\x0000\x0000ØÆk.¥bÃ\x000c\x001b \x000c.0\x0014ç¤\x000eÈXfmÄ9ù|¦k»\x0000¶m¶Ùæ<ÏñÇø¯ÿí¿üÏþÓ÷÷ßsòt<'ï×ËsRó:Çs8\x000fÏÃûõøz¿ýùÇ\x001f~þøòÿüíï_ÿÝyî7¾mIàà\x001cNÉõÌsòz\mN1\x0013ã^lfÉe!ùÜmìbè±\x001bKOÎëåy}yýüËëë/¯x~üð¼:Ïç¨c]Ö\x0000Mf¨\x0000\x001c\x0014¤¢R\x00079FÔ1ÊîåÉ¯üôë×·+\x001c\x0001,ëÐ1.3ÌÆ6 Ù\x0006Î9*ÛT*\x0000PÌ\x0008RÉ\x0018:êÚ8\x001dç0ç\x001cÅ\x000c\x0014</p><p>1`\x001b0\x0006ØE\x0003¬$Æ|0¤\x0000¢\x0007) ¦\x000e¸\x00010Àd\x001bc\x001bØ¦R\x0001aJbhÁ(`3lSqÇF\x000c$@ P\x0000T`\x0000\x0000m\x0000\x0000l\x000e{\x0019\x0015\x0006\x0008\x0007\x0000\x0000Ø\x000c\x000cÌÜ;w×5°
a</p><p>´\x0019`\x001bxm\x001f»×ëä¿þúËÿøïÿ§ÿûoï÷Û×/ïçñõ~ûz\x001eóíóùÅýØý¦9å9y¿ßþüë/ï×Ûÿê:÷ÛýþæóÛ1÷^EñÄë\x001cÏÉ)GÎÂÔÇñqG#Çvõ\x0001\x001e¬c\x0011s¹s1±£X\x000fÏKÏÛyÿðõþ©×\x000fï?¼þáüøé|ýÔóå·
{¯Åp</p><p>\x0011¤¡Ô@¥\x00029êèLT\x000cqÊ</p><p>3ÜÑç:=^¯{ùý=:j\x0002\x000cL \x0003\x0019
`¶©\x0000T¶©l\x0003\x0015Ø0</p><p>X\x0017\x0001J¥ÂtrN0 X`\x0006`Ê6Ì6\x001bÉÄí*1\x0010c\x0003 é`W\x001d\x001b0©kXT(ÀÅ\x0008\x0002\x0016FÃ±Í½#*Ie£Éî\x0005+u\x0004a¡\x0018\x0000P1\x0000\x0000\x0004\x00183a\x0010Ã6\x0000Ø\x000cG:I¶¹\x0006ÁØf\x0010G\x0018¨lÃ\x0004BÊ66P,v/\x0000xíûo÷û·ûýÛýñøoþ\x000fÏ9¾~¼½¿Þ¶¸×ý|ûõëßþþ_ÿËç{8*E÷úþû?Ö/ûý\x001foßÖo=W\x001b]áÄ)O\x001f\x0006³RÃÇý@xÙ>¶ÏØFó .=Ñ×Ñyëõå<ÇëëËóõ×Þ_z~üÔûí¼^êqË;îf÷Úf\x001bØ¦ I\x0005\x0008\x0008 E'Ò\x001e\x0001\x0006\x0004\x0011\x0019 pï|>\x001fç<:Ù®Ï÷·NÎØuFç \x0002r</p><p>\x0001\x0003\x0008³
@\x0005àÞ1mtUÂF\x0001\x0015fCÌ\x0005ÊÆví¢±\x0011Û\x0001\x0003\x0000\x001a\x0000Øf</p><p>c!03ÓH¶\x0000)`1)¶@a\x0019*5 ànì²ÌX`Æ¨l@\x0018<\x000fÉ\x001dÛ
0À\x0010\x0000*`Ì\x0010Ø`dÆd\x001b
$a\x0000`,Û@÷Zs#Ê6@*s{?È5rÎqïµÍ6¯³_4;ó~\x001d_ï/¯çñ<Ï÷·ûýíóýÛï_ÿqÿÖ®WÓã]>\x001f÷û_4g¿½î7÷}t§\x0010I\x0005à\x000eÈÌì^\x0006Ñ¥c½óÒyô¼×ó¼ô\x001cÏûíy9¯/çýÃóõÃy½×Ëóz9Ï[çQ[îæÛ¸ãa0ÛÜ;Ì6°QlT\x0000*°Må\x0000\x0010
3cT\x0018\x001eÆFQ!d»¾¿?Î\x0019Ýë÷ïß:Î9N!Ïó8'ÎQIê\x0000è\x0004²
pl³Í6ÛÜ{UÀf(\x0014Û\x000c>Sl||$\x00026
\x0006\x0004cpT Sæ\x0001m ²`T\x0018Ð\x0010Æ \x0003q\x0007
Ø\x0000ERa\x0014\x0000Ma00±\x0001\x0018\x0000àó¹*\x0000ÆvÙ(C\x0008\x0017"ì\x000e	`@\x000146ÛÀÆõÑfp\x000ehÓ
Í!Î9*Û@Qpm³±]÷Î@l\x0000`×ýþË~üç÷¿ý=Gú|´ëîcß¿ì÷ogÓÈ·]Ïáà~®Ïýh\x001fîl	9 i\x0011\x0013\x001dG²8OÎëå¼Þ<oÏûí¼¿<¯\x001f^_?çíy}9¯=Çy½çE\x0013=N\x0007ls7°;ÛµÁl\x0013l¶aî®
\x0006H\x0005</p><p>Ê6P</p><p>a6\x0018HÎ9*Ì\x0006\x0000bQ¶¹<Ïñ¼\x001e¿~ýöù|\x0013ç\x001cÇñÇyó<:GlSNkm`Ý¹÷{¯Ê6Û\x0014\x0000\x0001¸w pJaÃ±
T é\x001c</p><p>@¥ Ì6\x0004\x0000¶\x0001\x0003 `\x0000¶a\x0008pY\x0000¶1Ä \x000c³¥ \x0008RÀ6!C\x0008bÃl0\x0004\x0012¦\x0002\x0019\x0006c\x0000Hl\x0002J\x0000ClCÊ\x0000Æ5\x001bçRTÎóØØ¨)à£R9ç\x0000(66`c\x001bÂl\x0003\x0000×ßÿßÿt¤qÏÁq\x000eÏË3»kÙ'vPÎëèÄØ¹ÚK8\x001d@çõÒ9Äy\x001eç<ÎórÎËy^Îëíy½÷[¯Çy\x001eçyq\x001e:,N`\x0000àÚg>>}®m@1ldfØfm\x0000 \x0000\x0000Ø\x0006\x0000 B£`\x0000*m2</p><p>Ø\x000c\!`çäÏ\x001f_^ÏË?ÿõ/ÿùÏ/Å9SórÇó<Îy.ãÄîÀ6Ã66[`\x001b\x0000m6ÎÉ6\x0015Ø\x0010`\x000cl£Rá¨©TÎ	\x0001BäØrï0PÙ\x0006\x0000À°À\x000c\x0000Ã\x0010\x001b\x00103-C\x0006t\x0000\x0000³]Â\x0012`Kl¨Ø(PÇÌ\x0000Å\x0006S#\x00002$`Ã\x000c6d°\x0001\x0000\x0000\x0000¨0¹¦´yãëëíãÞÙ¨Ù\x0006`\x001b¨\x0000lCó8ç±Mem¶¹÷R^ýÍÉpÎ£çm\x000e{fÏc=×ëå9Çëýö¼ÞÎs'</p><p>ÎQyó<óx^oÎ¡9ç8\x001d:ê¨t\x001e+\x0003I«Ë`l©\x000c6×T66l\x0002\x000c\x0004f¶1f\x0000\x0000\x0000\x0000¶©@\x0005\x0000`#C\x0004T`»@\x0004 ÀÌ@ \x000cSÇ\x001f/óÓ½ß~ÿþ¸÷ºïÏ·ç3ç\Ïs½_çõÒrÍÝ0\x001bÛ\x0000\x0003@\x0001{¯J\x0001\x0005Ô\x0001À,ÖQ\x0013s: è\x000c	\x00044\x0015²asù\x0000(lC\x0008a\x000c]`\x0001"\x0000qH\x001c0C`!ÌF\x0019\x0000ì²\x000c-0#À\x0004t@8X(\x0000ç\x001c¥\x0000°À6°
l\x0003\x000em\x001a\x0006\x0001QÇ9a¶«Jem*Ûl\x0003°Í6\x0015ts¨À6{éØ®×¯_\x001f¯¯/½\x001e^o_?þp^oÏëñúñÃûývÎ£\x001b'^ÏËóz;¯\x0017\x0005®Óq\x001a%Y©c\x001d\x0000\x0006È0\x0003C\x0001Ø\x000cc×\x0000\x0006¹\x000bl\x00196`P6\x0018PÜÙÆ©\x0000À60\x0000¬Ø@\x0005¶	\x0000\x0015Øb\x0000\x0003</p><p>-°Ù½üñóKþá_ÿþÏ\x001d2É\x0011:Ê\x0006³Í6Ì6¥B6</p><p>\x0003Pa*£\x0000\x0002\F¢"©s0\x0000\x0000°\x000cÀ\x0014@6</p><p>@eC0 ò\x0008\x000e61\x0014\x0019\x0000 0\x0018w\x0014$(\x0000Àl0a&@`\x0017RÙÈp\x0008('8Ä9\x0007T`0lmm¶Ù¦¢À6»×Á\x0000Æ½\x001fÿý±Í\x0006\x0014\x0000PÙfm¶±±(äsÔQÀ6Lxýøßþ\x000f_þáýã§?ÿðõã§ó~y½\x001fÏë¥óÂ\x000c+á\x0014Ø ×\x001caMa\x0018\x0017.ÂFl\x0017Ø\x0001\x001a\x0001\x001b\x0010f ¶\x0001\x0003í\x0002£¹®°
\x0003\x0013÷b6`\x0006\x0000*ÛÀ6\x0000bcJ¥\x0002J¨!\x0000\x0000Å\x0006\x0003\x0015Øb\x001b\x000c-÷^¯?~þ4ùÏ~\x001b6,çðz?çÙ\x0000R×P´t\x000e¨\x0000)\x0008©0\x001aTê(¶¹÷¢Â\x0004\x0000Ø\x0006\x0018cÊvA\x0005</p><p>\x0006æ
\x00036\x0018
\x0000\x0004LE\x00082\x0004`\x0000ÀPÂ6\x0000\x0003\x0000Ôlh\x0006c\x0006\x0018\x0004r`Ô\x0005wÉaHvzTB%©\x0008Øæn&ÛlÜÑ\x0002L¥²ñ\x0019\x001ba\x001bØ¸w`\x0019\x001bfs</p><p>lsïµÏes7!ÔqNÎ9Ê9!¯ÿþÿü¿Þ_o¯×Ûëýö¼Þ:9çíº÷\x001a20ì²
£\x0003`\x0001±1±\x0001\x0001\x0010\x0006³\x0001\x0000\x0000ÌÐ\x00002Ãl\x0000ØØ\x00053m\x0018m
</p><p>\x0000\x0000\x0004\x001bç\x0000\x0008`£@¥\x0002PÙ\x0006@±\x0001Û\x0000T66l\x0000î.Ë÷÷uÎñ>/ßçãûó±Íç¼<\x001dG  \x000b\x001d\x0000\x001c.bB´\x0010A\x0000P\x0002</p><p>È\x00016Ê\x0006C¹÷\x0002\x000e¨a*\x00000cÙf\x0003\x0018\x0006\x0012¢\x0010`4\x0004m\x0012\x0000\x0000\x00002\x0000À\x0010\x0000ÌFA\x0000\x0018\x0000\x0008\x0015¨\x0000</p><p>\x0003\x001bÛp\x0015{/¨sT\x0001\x0000HffCd*ð<Ç9\x0003÷²ÍÝØµQyJ'çT\x0000àÞëóýqïÇç^°Í6Iâ²a8ä\x0010¯¯¿þáyçyçåG'°ûqïu7\x0003l\x0003	\x0001\x0000\x0003\x0001\x000cØF×î@\x0001a£\x0000\x0000Ø\x0006`\x0000Øf\x001b¨l\x0003Ì\x0006À6Û\x00000Û\x0000@\x0005\x0000¶!\x0005(\x0000\x0010\x0018²M¥\x0002P\x0001¨lSm\x0000\x0000
±ÌØ\x0000lsïlß¶y½Ò9Èë¼<ÏKEl\x0000À\x0004\x0008\x0001\x001d\x00001`N 0Û@\x0005\x0000 B*	\x0000@\x0005\x0008@\x001d\x000c\x0000$lÃ\x0010(`\x0008k£8²\x0001\x000c\x0000\x0001\x0014\x0000\x00006\x0003\x0000\x0000´YI`£ P</p><p>\x0000\x0000\x0000\x0014ÙÆÆ
\x0000£ä\x0000h³Í ,\x0016Ês:`{ù|>îe\x001bqÎqÊó<^¯Ê÷÷·{¯Êó<Îy|>×¹\x0017×½×6°
¸,4·+y=Ïñ<×óx£Ø®{¯{¯»aÈÌ½#\x0010`\x0012
Cca\x0004\x0013`\x001bÂ¥À\x0006a\x0000`\x001bØ0\x0015m`\x001bØ\x0006àÞ\x000b0ÛT\x0000,\x001a\x0000(\x00080\x0000\x0000\x0000\x0000\x0000\x0000\x0000P\x0001¨À6\x0000ÆÄ\x0002\x0006\x0000Ôð±\x0001ïWÞ½uãc\x001b1À\x0016Ø. °a\x0011\x0010T£Á%\x0018b£\x0000\x0000\x0002£ \x000c![</p><p>Ù\x0006*÷\x000elÃl\x0003PÙfd\x0006È5\x0001\x0008\x0014P!la*6
m*\x00006Í@\x0008\x0003\x0000\x0015\x0000Ø\x0006 \x0002w£Ëíªä°\x0019¸M`</p><p>;nSz\x001e'ê {æõ\x001có\x0012Äçs}>ß¾?ßî½*ÏÇ½W¥rïl³]Ì°M\x0001×h`øÜ«òz=×9Î	sïõù|Ü;\x001bC¨¹w\x0013\x0000ÛT`\x0008\x000cC¶\x0008\x001b\x0000\x0000f\x0003</p><p>Ø\x0006`\x001bm\x0018m\x0000¶m`m ÇPS@a!A±%\x0019jÀ\x0010Û\x0014\x0000°M¥RÙ¦\x0002@Hff \x0003,\x0000\x0015Ø&\x0001\x0010M±\x000b¶Cãp\x0000\x001cÆ\x0006Ù\x0006HH\x0010à\x0001`\x0008\x00005¤\x0000\x0010'\x0008\x0010 \x0005a Ø8'\x0004Î	Ù®í\x0002\x0000¨0Û\x00001&3\x0019(\x0008\x0000\x0000a ,\x0019K\x0005¶\x0001\x00080\x0010\x0002\x001b5\x0004\x0000\x0000\x0000`\x001b\x0000\x0001±\x0019a¶	\x0003³Mas÷±Ýyãõz9ç¨ô\x001cÊó\x001cã~®ïïoßßß¾?×½×½×6÷^÷^Û|>×½\x001fa\x001bÆ\x000cE2sïÀëy\x001euÏ½>»ÙØm\x0000\x0000\x0016C0Ö\x0018:\x0006\x0008Âf°)\x0018Ø¦²a3\x0000l\x0003\x000c\x0001`¶Ù\x0006\x0000¶1\x0006£\x0000@\x0018¤"\x0018à\x0008\x0010\x0014 6@\x0005\x0000\x0000*ÆEI`»¶\x0019\x000e\x0012e\x0001 Â</p><p>\x000c\x001bvTp±°aJ\x0005\x0012\x000b\x0018ÊH</p><p>(\x0013ÉÍ6\À\x0002m*\x0000À\x0010\x001aB6\x0018 P!°
l\x0003BE
0\x00000±\x0000aÆm\x00006\x0000`Ala\x0000¶\x0001¨À6
\x0000\x0006\x0000\x0006»»\x0001.2\x0001\x0018°ÌµÍvl×9Çó<Î9Î9Â\x0019çäùzûñ~ù¾sï|îÇçs}¾¿ýþþöùþö}?î÷·Ïçc÷c»6¶q)à~®Ïý¶ñª\x0014]ÏÇ½×Æ0´!\x0000\x0019L6 \x0008®\x0000\x001b\x0000\x0019²
0°\x001d`#v\x0019`\x0018\x0002\x001bÛ
\x0000\x000c\x0006%\x0010\x0000"\x0018\x0006!0´C#\x0000J\x0008</p><p>X\x0000,Â©ÏçÃ^£b\x0003@A\x0000BÌNÎ¡s\x0004²Íp\x0000J°\x0019H\x0008`áP\x0001\x0002'<\x000c\x0016rwíf£FS\x0001Ø¦\x0002\x000036Å\x0016Ø\x0000`</p><p>fm\x0000¶Ù\x0006à\x000cÌe\x0007(`×\x001d¤\x0000Ta\x001a0
\x00012\x0013,</p><p>!\x0000\x0015Ø\x0006 \x0002\x0005\x0001\x0000Ø\x0006°£Áa`£2\x00036÷ÎöQùþ¦çy|?sÒÉSóð<½Ïsòë~Üæs?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/cest-quoi-linclusion](https://lemarche.inclusion.beta.gouv.fr/fr/page/cest-quoi-linclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/faq](https://lemarche.inclusion.beta.gouv.fr/fr/page/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1241158796/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1241158796/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/cafe-signes-sensibilisation-surdite-840865018/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/cafe-signes-sensibilisation-surdite-840865018/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/840865018/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1241158796/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1241158796/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1241158796/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/strategie-de-communication-731075650/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/strategie-de-communication-731075650/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/731075650/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/annonce/resultat-recherche" class="form-category alt col-xs-12">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/video-motion-design-1415815731/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/video-motion-design-1415815731/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1415815731/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/contact/creer">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/transport-de-marchandises-1717064659/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/transport-de-marchandises-1717064659/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1717064659/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/les-teams-building-322626612/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/les-teams-building-322626612/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/322626612/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/identification-verification"
                          method="POST">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae/export/csv?page=1">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/inscription" method="POST" autocomplete="off">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Application Error Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 3
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1241158796/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1241158796/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/322626612/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/322626612/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/731075650/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/731075650/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1415815731/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1415815731/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors&structureType=1&withAntenna=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors&structureType=1&withAntenna=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/251202856/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/251202856/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors=9&structureType=1&withAntenna=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors=9&structureType=1&withAntenna=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/840865018/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/840865018/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1717064659/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1717064659/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 57 [https://lemarche.inclusion.beta.gouv.fr/fr/identification].</p><p>Predicted response size: 357.</p><p>Response Body Length: 474.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
Instances: 4
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/les-teams-building-322626612/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/les-teams-building-322626612/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1241158796/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1241158796/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/strategie-de-communication-731075650/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/strategie-de-communication-731075650/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-402587701/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-402587701/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/transport-de-marchandises-1717064659/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/transport-de-marchandises-1717064659/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/cafe-signes-sensibilisation-surdite-840865018/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/cafe-signes-sensibilisation-surdite-840865018/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/campagne-de-sensibilisation-251202856/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/campagne-de-sensibilisation-251202856/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/video-motion-design-1415815731/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/video-motion-design-1415815731/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/help-desk-909148577/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/help-desk-909148577/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/common.9038d883.js](https://lemarche.inclusion.beta.gouv.fr/assets/common.9038d883.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/accessibilite-numerique-452681361/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/accessibilite-numerique-452681361/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js](https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/test-recette-applicative-informatique-882556899/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/test-recette-applicative-informatique-882556899/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/creation-de-sites-web-digitalisation-numerique-636822883/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/creation-de-sites-web-digitalisation-numerique-636822883/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/css/ie.css](https://lemarche.inclusion.beta.gouv.fr/css/ie.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=86400`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/faq](https://lemarche.inclusion.beta.gouv.fr/fr/page/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/cest-quoi-linclusion](https://lemarche.inclusion.beta.gouv.fr/fr/page/cest-quoi-linclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Debug Error Messages
##### Low (Medium)
  
  
  
  
#### Description
<p>The response appeared to contain common error messages returned by platforms such as ASP.NET, and Web-servers such as IIS and Apache. You can configure the list of common debug messages.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
Instances: 3
  
### Solution
<p>Disable debugging messages before pushing to production.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/faq](https://lemarche.inclusion.beta.gouv.fr/fr/page/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/css/ie.css](https://lemarche.inclusion.beta.gouv.fr/css/ie.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/favicon.ico](https://lemarche.inclusion.beta.gouv.fr/favicon.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/cest-quoi-linclusion](https://lemarche.inclusion.beta.gouv.fr/fr/page/cest-quoi-linclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�ǫ�����kjب��^��'O*^�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-verification-email?username=ZAP](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-verification-email?username=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `username`
  
  
  * Evidence: `username`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL contains potentially sensitive information. The following string was found via the pattern: user</p><p>username</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected 2 times, the first in the element starting with: "<!-- allow a user to go to the main content of the page -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 6
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script></p><p>var ORDER = 1;</p><p>var SESSION_ID = "";</p><p>var VERSION = 1;</p><p></p><p>//export function track(page, action, meta={}) {</p><p>async function t", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="slider-prev">Previous Slide</a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1684993419`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `666863243`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1738243216`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `382825700`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `809282018`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `750730664`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1287361925`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1016728672`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1979597865`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `731075650`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1050870750`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2016967485`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1661271550`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `840865018`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `402587701`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1642303161`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1849703834`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1421469314`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `322626612`
  
  
  
  
Instances: 43
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1684993419, which evaluates to: 2023-05-25 05:43:39</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[start]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `sort_by`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[nb_days]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `time_range[nb_minutes]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
Instances: 15
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=01%3A31%3A27</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [option] tag [value] attribute </p><p></p><p>The user input found was:</p><p>characteristics[5]=12</p><p></p><p>The user-controlled value was:</p><p>127</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Fri, 28 May 2021 02:40:08


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 4 |
| Low | 13 |
| Informational | 10 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 12 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Application Error Disclosure | Low | 5 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Cookie Without SameSite Attribute | Low | 4 | 
| Cookie Without Secure Flag | Low | 4 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 2 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Information Disclosure - Debug Error Messages | Low | 5 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Content-Type Header Missing | Informational | 3 | 
| Information Disclosure - Sensitive Information in URL | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/119/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/119/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38768261000234`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2533/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2533/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50870892200044`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/5763/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/5763/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50065213600010`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=3](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=1](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2784/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2784/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38469683700044`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=2](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/55/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/55/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38745382200067`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/213/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/213/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38784620700026`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3013/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3013/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50930450700023`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/184/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/184/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38848971800022`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3664/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3664/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38173482100030`
  
  
  
  
Instances: 12
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: DinersClub</p><p>Bank Identification Number: 387682</p><p>Brand: DISCOVER</p><p>Category: BUSINESS CARD</p><p>Issuer: </p>
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xxmedium/uploads/listings/images/8c446bae2b2d42cff7ef40b51623b4feb8891ab2.png](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xxmedium/uploads/listings/images/8c446bae2b2d42cff7ef40b51623b4feb8891ab2.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=%í¬\x0011EBÓ\x0008¾öúUÖ.¿ÂÃ£1þÁCî\x001eMÑR\x0019OR¤\x0000À9G\x0008\x0010\x0002Zk´Ö\x001c\x001d\x001dR×,Ë(\x0002c\x000c\x0000RJªªF\x0003\x0000\x0000\x0000\x0000\x0000\x0000¤i
ÀÝ»w¹|ù2gÏe0\x0018`\x0001!H]ÜlÎ¯¼vrY)ÅÚ`À«WwØ<¡|«6²Ñ^"\x001b]FÓ\x0019«+\x0003¼ð(\x0008!0\x0018\x000c¸|ù2·nÝ¢,K¤\x0010\x0010B  @\x0018#É\x00044M±ÖòÒK/ñk¿ö«|ï{ßc¹\ ¥BJI\x0010#xï	! @k<Ï\x0011Jâ\x0016KBµ\x0004º\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000D@\x0000Î{NOOùøã1Æ`AJ÷\x0001ç<Þ{\x0000\x0019Ç\x0008!(ªª\x0008!\x0010cD\x0008Á;wØÙÙ¡ª*¢ ®k\x0000s\x0010\x0008!`Á\x0018Ãt:e8\x001cb´¡ªk¦Ó1i! Ñh\x0010BÀ;ÇÓÓ%t[O$\x000f>c{kîÎ\x0016/¯Y~üþ-îî¹\x001a?!O\x000cãÑ\x0018\x000eH\x001b9~öÑqaYmHTÖb¥;`6/)\x0002ç\x001cÞ{1\x000c\x0006\x0003Úí6Y\x0013#\x0010°Öa&µ\x0016­\x0015\x001a\x0000\x0000\x0000\x0000\x0000\x0000À9Ë|6ÃZK»Ýf0\x00180\x001a
é÷\x0007\x001c\x001d\x001d2:\x001drþÊ
º[g(«ù|\x000c\x0017._çÚEO¹(XÛÜ¦»ºÍ§?·à\x0007<æ»?xf#§Ñh\x0010| È\x00103gÎ$	wîÜa<\x001e#@JRv»M¯×£Óé$	\x0000+++¼üòËÄ\x0018yúô)\x0000Æ$\x0008!R"\x0004À9\x0007<Ï1ÚÑlò5®.\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000 F `÷`Èÿ÷\x000fþWâ²nN§C$$A\x0008I\x0011ï=BÀÁÁ\x0001'''\x0018£±Öá½Ç{\x000f\x0000@UU|òÉ'4M¢À{O\x0008\x0010\x0002u]# ªjÉðÞ±XLxò¸B*\x0001RQ,G(Òh&äYJ\x0008YíXê&2ørÄù­\x0001R+²°Dú\x0005ßï\x00105Ú':ËÊÚU²¤Íéþ\x001eÓSê\x0000J	´¤í¼Õ¥ß+qårÉÆÆ\x0006½^\x000fc\x000c[äyÆññ	Þ;¬õÄ\x0018\x0019\x000c\x0006Ä\x0018Ñ\x0000\x0000\x0000\x0000\x0000\x0000\x0000Å,ÏqÎá½gN§C#Ï!\x0006BÒ:s\\x000bÊº¤
\x0012"XËxxJi\x001dþ
RF¶Ïeyç)§§C>üðC^|ñEZ­\x0016"\x0008Rxï\x0019\x000c\x0006Ü¸qÑhD\x0011ï=Fn·Ö\x001aç\x001cUU¡µæÅ\x0017_äñãÇ<xðÅbI\x0008\x0001­
RJÑ\x0008!QJ\x0012cD)E#o$	Î;eÉøè!'osö~\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0018#åbÆÓþÿé_üÏ\x001fñ[×Î²øÌ\x001b¬êS¤IR
)%B\x0008\x0004\x0002!\x0005.]âã?Æ9s\x000eç\x001c!\x0004bÄ\x00181òèÑ#.^¼Èr¹$Æµv»Ít:%ÆH\x0019\x001aMIsÙ%M\x0013´\x0011\x0008!	\x0002¦Ã\x0019¾®°.R%vs\x001b}~í«ùõ×¶ðû\x0015;ÛgÐRà½åë¯]æ/ò1íµm\x000e?¾KáÆ\x001cM\x001fóÝg¼ýpYYÒV¬Ù&ëmr:\x001esrrõ5íVn·Ö££#:\x000eEQ²XÌ1à½§,\x000b&	&I1¢\x0001\x0000\x0000\x0000\x0000\x0000\x0000¤\x000cú\x0003\x0011 ÛjÓi·	. Öº¼s2ä¶=åÂIÅ*a%ï°\x001drt°GUX\x000e&?{/~¶`ã¨Á»\x001fßÅYËññ1o¾ù&\x0017.\`ss\x0013c\x000cUU±X,PJqùòe\x00108çðÞ\x0013BÀZK\x0008\x0010\x0002\x001b\x001b\x001blnnòî»ïRU5Þ;¤H©H\x0004c4B\x0008B\x0008ÔµE\x0008A\x001eë,Îyl½ \x0018?#1^o\x0000\x0000@\x0011[×Ì&#öv÷xøà\x001eîÞÄ\x000c\x001fs­Ð)|éÓ\x0017X-kV³þÎ\x0019._¸\x0000\x0002Æã	ÞYZí6Ýnýý}þâ/þù|NUU\x0000\x0010\x00001\x0002pttD¯×'\x0000µ5kkk´Ûm\x000e\x000f\x000fÑ:GÑ M¦´\x001a
fó9u½¤ÓË¸z~õ~Îö\x0015:«-¶v:¼úÊU¿º¶ g
¤\x0005;_²:þË¯A·OWkÆÏFüäæ-þãÝ\x0007<ô\x001b\x0019ývN²uR4(Ë#¬­°Îe\x0019Ífáp÷,ËN'\x0008!É²\x0017^x\x0001c\x0012¾ÿýïC¬qÖ¢\x0001\x0000\x0000\x0000"\x0000 ÅbÁábDhjö}Içì6»Ó	\x001fÏ<L\x0016<Î<nº`÷ò*Ó[\?]°°KéLkA&o¯ÐÈ¶y¶8àÖÓ'xï\x0010BS%\x000f\x001e<`<\x001e³²²B§Ó¡Óí\x0018÷\x0010\x00021FbÄ\x0018\x0011B ¥$I\x0012Ö×ÖØÛÛc4\x001aa­ÅZK$dY1\x001a!\x0004R*\x00108W\x0003 Ä\x0018Ã²X\x0012BI\x001a¤Ý\x0015¤6C¾ý§ÂÛ\x001fÓ>%\x001esûÑ\x0013
\x0017¤\x0012¾ò©s¬û\x0005þÖç^¢\x001f¦Tw±öüËlîì¤)B@¯×åðð\x0010ç\x001c\x0000¯½ö\x001aNñxµ\x0016)%1F\x0000bÄ\x0018ñÞsttH§ÓA\x0008IUÕ(¥8{ö,F@)P«(\x0007_þõ-»zÍ.×.÷Ø½U â¹Ï_£¿	6ÌIdsÊY Ê9óéÓgÇNîqþÏÑ\x001c¬ppû>?=\x0019³·¬é§~\x0017_å¯ü
?üÁ[<}ü\x0018¦$"ÄZR^¯\x0010Á`@UÕL§\x0013\x0000úý>ÎY¼s$A\x0003\x0000\x0000\x0000\x0010aV,øñÍwø·ÿéyóÎ»\x000cÎ_àÆ/#qOq²dfJÒ4Ã%
\x000ef\x0015Q\x000e\x0019ú9óG3\x0016Ë9ëi$§D\x0005ý^\x000béGÜ:ä-ÖÒ4MéõzlllÐn·ÑZã½'ÆH\x0008\x0010\x0002\x0000B\x0008\x0010\x0008!PJ¡BJIeÌçs\x0010\x0000Ìf3¶¶¶0F#¥\x0004@\x0008RR×\x0016)%R
|ÜHäbÂxxÊ¹_ãää\x0018[<~ë;ÜþÉ[\î§üÚ«iû\x0006W\x0007	\x001b[Û¼òÂU\x0006\x001eA&4}É\x0001ï\x001exî»\¿ú\x001cY!¥¤ªj¤\x0006 Ùlç9UU!\x0000 Æ\x0008@\x0018#\x0000Ãá\x0010c\x0012´VTUI\x0008ããc$á¹ç®qrz·
®\xÄoÿ75þÍ°÷¬ÁË¯}îú
ûw<÷ÞyÂ+¿tÒÏHò9ÏK\x0016\x0006ÉrÎhï7oóètûÑq½w\x000eÇ<\x001e\x000fiëf"(ÒS§Îüíßú[¬®\x000eøÎw¿­kNOO1Æ µÆ\x0018M§Ó%ÆÈéé)ý~v»C]W,K$!Æ\x0006\x00001r8\x001bñ\x001fßÿð¿ÿo¼õ×?`\x001e\x001dW>÷\x0005.ý\x0017¿ÎýÃ§d!±¶\¸x\x0019i2zU&kÛ\x001cÝ¹Kza÷o\x001f\x000cYÙÙf£­8Î,u\x0003he¤WùÆ7®PU\x0015\x0010\x0001\x0008!\x0010BÀ9\x0007@\x0011\x0000)%1F´Ö(¥\x0008!à#\x0000@m-UU¡´f>¦)Æ\x0018\x0010(¥\x0010B\x0000\x0010B ®k÷ÔÖÒL\x0013âbÄþÝ÷ÉºÛ¬n\x0018I\x001a
~íë_áó\x001b<ip®×ccû\x001c¡Ðê÷H\x001a-\x0016ádÊ\x000føÎ\x0007Çüü?|Ì/}é&ÿÏöOéÆ.Þ{z½.IP×5Î9$a±Xç9\x00001F\x0000b\x0010RR%Ëå$I¨ëº®qÎ!¥$Ë2\õÈ×~¹ÉáãÀÞçhw3ª¨éiðäö£=Ïã\x0007\x0013VÎP\x0005Ñ\x0017	é3DÚd|pÀñî1÷\x001fìÑØ^ÒY}½éGÓSÚÝ\x000e­fAá$ÙÚ5
\x0017\x0019
Üs~¿G»Õb2 À{1f³E&h­étÚ\x001c\x001d\x001dqÿþ=¬u,\x0016\x000bRTU1R8Ë¿þÑ·ù÷?ýK~~ë&ågÚqþ«_æÕßþ\x0006ËjÉõ\x001b/e9Í$GHÁ¬XÐë\x000f¨·Ïððß¿ÃT\x0018òÏ_çøÙ!÷ÇSÎ^8Ã§\x0006k¬¯åNe±8²L¡µÂZs\x000e\x0018#B\x0008\x0010\x0002!\x0004\x0000B\x0008R\x0008!\x0008!\x0010cD\x0008\x0001\x0000\x00001Òl5M§\x0018c°¶\x0006"Zk¤h­R¢µ&ÆH\x0004¬õ¸ºdïÉ}öO¦¼úµßD+
1â´¿ÉÖÚ\x0019´j6\x001a°\x0008¨X©6^f\x001cÏ\x000fø«Û»üÁÏNÔ
¥5?ÿø)·\x001f<äóy÷Þýe¹dg{\x000f\x001f3ÏXYY!I\x0012b\x0000Ä\x00181\x0012B@\x0008A\x0018\x0003eY\x0002P×\x0010\x0002­VÁ
+««L\x0017\x0005\x0017Î¥ä­üð?ìP×ëX'qÆ@Óè¶YÌ<»\x0018ÒÖ\x0001&1\x0008ÕEFI\)I^¸FÛö¸^@³7¡¿þ\x0001Ãµ\x000føb{@gp÷?|D=ÏYÔ\x0016\x0011-³é¿úþ_qõêUÚí6£Ñ\x0018#J)s\x001c¡µ¡ßïÓï÷É²·ß~\x001b!\x0004Ëå\x0012c\x000c\x0000êo~ã¿ønÍöøüÙ\x001fóþ;ï QeÉR®|ù\x0017SÓÎ[¬¯¯ã¢§MQÞÓH2²¬Éâôêñ\x001eóÉ\x0018³a\x0007Möw÷ð\x0014Ï9Ì<\x000f¤Bû\x00061@UU\x0014EAUUeI]UXk!F\x0000\x0008!\x0010B\x0010c\x0004À{\x000f@\x0010\x0002½n,M988Ä9\x0007@¿ß'Ë21¤iJ¦h­¹té\x0012\x001bë\x001bH%)Æ»<¸ùS\x0006ç^äÌçD"\x0010C¤´é½\x000f¨êÈ'O\x001eqxxL5Ú%o=<å_ÿxi­ñeJ3¬w<¼wW^¼ÆæÆ:{OùäácF£!³Ùº®ùøã±Ö"@\x0008\x0001\x0012!\x00041F@\x0010BÀ\x0018C]×(¥h6$iÂóç(5ÿìg\x0005\x000f\x001f]#Ë2\x0016ó9W¯oqþRÙ\x0008ÆC\x0000\x0003qÎF
ªQ=\x0016õCÚkkô×n°±sÎú
óÅOéWÈÅ	g.6\x0019l]&æ\x0005O\x000ej\½rÕÕ5¾úÕ¯²··Ç'|B³Ùdeeº®ñÞS×5RJÊ²¢ÕjbL\x00100NÉ²ÉdþÙÏÞæcÙÜYãÉM½ó\x0010Âæs7hnõYv§ÏîGL\x001f<CT\x001eüOÿÖß!Ïrn¼þ\x0019{í3Ì'cïßãéýwøÜ\x000b¤ÿÇÍUö\\x0013Q\x001fñwW-Õá\x001a³ñ\x0006óÅªª¨ª¢(°u\x000f\x0001ç=RJ\x0010Ä\x0018\x0011B\x0000 @\x0008\x0001@\x0011ë,½¬G¯×åôô
ò<GkR
c\x000cBH\x0000lmñ\x0011D¬\x0019î2skg®ã½Gi\x0005÷\x000eÒ\x000e£¼ÇÑ'\x000fY\x001cÐ6å£
\x0005Õ²àýáSö%Jjóè$pþÒKTºËÿíþ#.í´épJ³·FâcdccV«Åb±@J\x0010\x0002!\x0004\x00001F¤\x00008ç(\x0002$IÈ²n·ËÁÁ\x0001©Dr÷kd¦Ár¾`>·\x001cÍP*ceGóä\x0001øªàx7eóÚ1iv\x0019\x001f-È²ú\x0010©J\x0017j®\x0012V·ÎáÆï³8ÝåÜå\x000e×ßbVì3<mpíÚUVWWé÷û\x0000H)QJRU%u]ç9\x0000eYâ}`mmº®Y.Ä\x0018©ª
\x0010èüä§Ï7yíÕOqðá\x0019>þË\x000fHVût¿F\x0015 $<½ó.üé\x000fX9V|á\x000b)×~á\x0011§uêì×ILÂ².Ézm.}î³¬^¿Èùý?`»7¦ÛÌùáþ*ï~ì¨ü\x001e_ûUÇwßm \x0010H)ÑZ\x0013B ª*Ã!I ¥D\x0008\x0001\x0000\x0012ï=\x0000ibÁûÀh4¢Óée\x0019R*IPJ"¥Ä\x0018M&8gi5s\x000fnqº÷3^'Isj[£BJIUUè4Em^E>~Æöú*õtÎf³É±Õüû·\x001fqëé\x0010O$\x0004¡$yÞ¦Ó[E¦-î>=ä{OÈ\x0012ÅÆ à¹3=»¸I£Ñ Ûíptt\x0010\x0002\x0000!\x0004!\x0004b\x0000\x0008!\x0010BPU\x0015Æ\x0018Ò4CJÅññ	Ýn/|nP§,\x0017}Ê²¦ª*²äôdF\x001dÛ´ûmZ]Íôx-4õ¼IÝ=À$\x0006¬0|Àz¯áù³\x0005Y²M³½Áàì\x0016¾ÜGÇSFó\x0006¯Þ»O¶°ÖÒívÉ²\x000c­
Zkªª¦®-1F¼÷h­R"¤ÑhâCJI\x0008\x0001¥\x0014BþøÖm¶Ï\gtô	Ï]Ü`þü\x0015|¯EÈ$åî3îÿõ;'üÍ\x0017¿÷?<ÇW\x0010õe~8}ÆwË)Ö4¨¼¥5°1bZ+Ìú¯2yô³7>á7Îe\x001c¼²Õ®huJ<\x0005141"@)E\x0011)%Þ{êº&I\x0012\x0010\x0000Ä\x0018ñÞ\x0013cD)E³Ùd>_Ðh4X__g4\x001aS%k«kä\x0006ycæÅç/ðÅO_äñí',»Ì\x000e\x001e buã,óùªª(\x0018#itý\x001cfû*f²K'ÍW\x000b~üàwö\x0003Õb\x000ei\x000e¢¢ÙÞ »ºÍÉ¬¦:=¤¬-Á\x0005&³%ûGcn?:æ³óÈßùÚ«lllpûö\x001d´ÖH)	!\x0010c\x0004\x0000 Æ\x0008÷\x001e­5\x001bh­9::\x0002\x0004ÍVd±èâ¢¢®Å\x0012ç\x001cGGS\ÝC§
Z\x0006QÎ|Pº$½=zz\x0013!SðÒ>Æ4sj
ZÉu ¦µ²ÍrtÂâpÈúöU¦UöN*Ë\x0002!`8\x001c²XÌ\x00011¢µ&MSB\x0008Ä\x0018\x0001h4rúý\x001eÓÙ\x0014)%Î9¼÷\x0000èÁÊf]óèñSv\x000fÆ¸\x0017:x\x001fxú³¿¦zrH·öüö\x0017þÏüÍ_½ÊWw1¢÷S¶Í}Äâ¹ßB\x0004K¥4J) R÷^ ·ù>·Ýâ\x0017ïñ¥³×ùÜ«ë\x0004°·»\x0002\x0012\x0019%!\x0004¤\x0008!pÎQ%Þ{\x0010\x00101âC\x0008Rªª\x0010B°½½Í£GPJ²ººÊoüæo¦)ÖZb[aç¦UåÜïÏÙûdÕç¾Äáñ1£á)UUc!x\x000f1V»ÍÍã\x0005Ë{O9kj\x001c\x001cñW')Ãñ)1\x0014´ò\x001e­­K¬l_"o÷¨ê\x0000hPKt\x001e¡\x0004\x000eÉßÄùíu®]»Á\x000fþêxï\x0001\x0010B ¥$Æ\x0008\x0000@\x0011!\x0004Þ\x0007®_¿Neìîîbë
\x0011%ïµ8<<!ú².Ùß=fYöÉ6iÞ!Ë;ÙÄÓ	è\x001d,È\x0001ù!­µ\x0015òÅqN\x00144]#k	¦£Õµäñ
O\x000e\x0018ÏÞc¹\0<=e<Ï1\x0002 "ÆHQ\x0014(%ét:dY­+B8ç©ë\x001ak\x001dú¿ûïþì¦§\x001c=ý1Ñ\x0001ÓÑ\x0010\x001cÕã\x0019¯ì8.ý
_ýò«\¿ô\x0000Ä\x0003<ç\x00104iHÈþ·?ÚdrZP\x001c\x001e£¤¢wù"[7.óÂ¹\x00179k\x0014ûG?åk¿0 ~ûv)\x0001âºªÐF¦)u]S%eY"¥¤®kbÄ\x0018	!à½\x0007@JIelnnòéO¿Î·¿ýmÎ;÷7ß|4M)Ë\x000bçÏðÏ¯PLw1bB§ãÈ&éä_cýì9Ö×ÖðÞ¦)\x0000F\x001bj[C»û\x001dþø?¥\x0014lla¦\x001dÒÙ8C÷ÜXç9=x8xFiÖÂ ê!Y
J' \x000cÐ¿~ï\x001e»ÔBi\x0005\x0000@\x0018#1F\x0000\x0000¤H)1\x0002\x0011k-EQ&	\x000fîu°SEd,\x0016SN.Ç\x001c\x001ctÍ'Ð18å
V»}²ª Y´!$ á\x000c~©Ñ ÕÑi$,\x0004¦Ý§¡Ï]¢ÝG§çQñ³¾ÃOÞü\x0011uå°>Ðhd\x0008!\x0010B F\x0008<oÒnwh4r@ ¥À{s\x0010\x0002ú­þ\x0014a$¦\x0015vHÃ\x0014LfkÛßüÍ_¤>ø\x0002\x001b«Xí\x001f\x0012b$2$òñAÁ»?=æÛÏ8|ø\x000c?[\x0010¤\x000f>BØ/ópõK¬ol\x001eäÜÞ}BçÒK®R×{U	\x0008\x0010H©ÐZ£bgg\x0007ï=Þ{¬µ8çpÎ\x0011BÀ9µårÉë¯¿Îh4f<\x001esæÌYË\x0005\x001f?&MS$á7íu\x000cst4´Áú¹\x001dÎþB \x000c\x0015Z\x0019¬¬0Æ \x0002\x0000\x0001J)b\x0008üÖßø\x001aïÝ¼Ë£G0õÝ\x000fht×ÉVÎ3\x001dâÚgg>è#í£ %îS=þ\x001eÉô\x0003²V\x0007¤$\x0015ñlÁéØ¢\x0002!PJ\x0011c$\x0000\x0000\x0000\x0000\x0010\x0002ï\x001dÃáf³E»Õ¡Û\x0019P\x0017-\x0010ýã}f#º ²ñ¢d<\x001dÑÎ\x0004ä\x001c«+-úç^ ÛÖ¨\x001aü\àc\x0000\x0015Iã\x0002woF¢%+2Â´B.W0ó\x0017h%Gr\x0008Î\x0004>z´Ët^÷\x0008)	! µF)E\x0008\x001e<oç9ÖÖÜ¹sñxB&\x0010¨ª\x0012\x0000m­%¶MPBRZÍZ³Åõ\x001bWXñ\x0003uf@¯ÿ!R4(ã)\x000bq{û«ü/onðlu\x0016ì¼ÐF5³½=\x0016sËÝ÷>"Ñû;=þîÙ¹B¢A¸H\x000cªªÉ²\x000c¥\x0014Å\x001c¥\x0014I`Á9G\x0011ï=ÖZêºÆZs\x000e)%/¿ü2×®]ã_üÁ\x0007\x001f|@«Õâ3ù\x000c\x001e=¢X.Ù8³Å³+è\x0018\x0008Yq)\x001b«Ô:UU@\x0010\x0002J)\x0000êºÆ{sóç6ùå/|ùÁT²EÒYCæk\x0014²þ¥ÿ
¹þ\x0012Næh,Æ\x0017´,\x0014ùeb£Oõ#\x001cÿ´»F\x0015\x00041zÞþù'\x0010\x0002\x0004 ¤DH\x0001\x0011\x0000\x0000\x0000\x0000¤TÔµ¥×I6rùìEdÔ<Ýß¥®K$2§´3f§§Øãk¬ÇÙÞ\öPÚ\x0011¤!Z\x0016\x0019\x0004ëÆ¸ù|ed°Éòè\x0019ÇGßçäð\x0019e©pU,íòâ`ÀgÎ­ó¸[ðÉ³}|ÔuÖ\x001a­5ie\x0019UU1Y.\x0017TUEQ,\x0011\x0002B\x0008\x0008!¨ë\x001a$	 ¸÷Ð¯2*f|éÂ:çWÎPLÎsvÇ±µ9ÅÅ\x0006BäÔqÉ7?:âþ^à\x001cI\x0011
ÕIÙÙþ\x0014y\x001dsëí\x000f¨ëk<Ð\x000bþæ+¿ÌÒN\x0019Î\x001e#È\x0019ô\x0007D"!\x0004$!\x0010\x0002B\x0008\x0000¤\x0008!ÐZ³¶¶ÆóÏ?Ï¹sç8<<ä÷ÿ÷yçwxã7ø'ÿä\x001f³±±Éïÿþï3ÎiV¨Ðr\x0017%ÉÙÁ\x0010Û?ÅwÏ!¥\x0004"Þ{\x0000sxï©ë\x0010\x0002µ\x000e­fJÖÛÀ9Ca\x0006èÏýCÊö6±¨P)\x0018\x0016!%5
¿`+8ÿ\x0015ã[¨Å\x0010b\x0017ï\x0012êØ Ë2æ\x0005&3diFQ\x0016\x0010\x0000\x0000\x0000\x0010B@L&SRréÂ%20<:&O%YÖ¤ð¸(\x0018¤5_}íe®¦e`7²I¹PzRà5à\x0008õùþ!ÃgOØ¾~û\x001fÞÄôrýâ\x0015ÞzpÌ_¼¿Ç²\x0014uN\x001d£cûü\x000e½Å\x0014[ì
BF£I«Õ¤®jf³)Y³¾¾Îúú:N7oâÇ{s\x0010\x0002:Ïs$a}mM·I\x000c°}iLì\x001c"+Åù37É³%53r®ZÉþl\x001fë,\x001bk´Ú-TbÈó\x0006Fh\x0002ÐþrNX,\x0019f|âJ§ïK4ÖîÂÇ\x0002"1\x0004D\x0014H!DTh©ð!\x0012%M3._¾Ì\x001b7è÷û<xð?ú£?â£>b>ó«¿ú«üÞïý\x001eËå\x001fþðÔugÏ\x000eyöÁ{\x000cÎ_çdÊä½¿F*\x000eîÜe¸¹àùßx($1F\x0010H)ÑZ\x0013BÀû\x0014¢¤5
ÝÅ\x000e. _û»ÔóP,B\x0000\x0010½C' \x0005Î[ÄrOs\vzñ>Ò4hDvV©ë\x001a)%Î;¤\x0008!\x0000\x00001\x0002\x00108kéwúdåtA³Ý¢´\x0015eQ"bä\x0017nìð;¿ö
n¼ð\x001c4Ô¥ÅÎÆøºb±r÷Þ-\x0006\x001b=\x0016ó\x000eÁYé\x001aæ£c\x001e\x001f¯akÇ\x000f¿û\x0003º¿Tsóg»¼õÑ1N\x0008êÚf\x0015Qi\x001aÙCÊÚR\x0015^£ÍhQRU\x0015(X_ßdmm<Ï1Æç9I°\\x0016Ä\x0018\x0001\x00016Æà½§ª+T(mH\x0013I»;g<{Hgå6Ä\x0014!*fá	?:8ÃÅkWhngKYF§ß¥ÕìÐK;H-1"À¹Àh4æâÏx\x0001®~º>"o·É;-&¦"s×W¶Á.Hê\x0019ÃIX;ËÖÅëÌ&cîÞ»Ç£G¨ªÁ`ÀïþîïråÊ\x0015^~ùe~þóóá\x001frîÜ9´Ö\x0008`åÂ<IC½÷>é[8¿Ê{ªÉ»ëÏÑî\x0018^ORB\x0004ç\x001dÞ{\x0000RÄ\x0018qÎ!àøhH):\x0017~xýPÑÓ\x00085D$ÑÔN"ÉPv÷\x0015ÊÕ\x0004o*ÇÛà,2É\x00081"[\x001bäË11\x0002D\x0000\x0000¤\x0000\x0000H)\x0001HMJUVL\x0013ª¢ÂhI\x0008\x0011ë=í,ãï|ã«¼þÒy\\x0015°Ó
·\âí½gxóç\x001frçpOé2£É	kgöi
>È\x0004÷îþ\x001bë\x0017¹Öé°wç6/}Þrù7·\x0008qNÚï1¾÷\x0011÷ni:ç"òM(«%¹\x0017l\x000cÖèonÑh6HtBb\x0012\x0014H)QJ\x0011b@\x0008	D\x0000\x0010\x0018cÐEQ\x0000P%\x0008A«ÙÅ$5Ñ\x00061îb´c*¦4cÎÁò?}×q<o\x0012\x000cVz\x000czm\x001ay\x0002L¢h\x0006RHbTÒÎ:\x001c/¾ÈÛ¬ó%z¯et®eVÏ8¼{æâK2#ä\x0002+\x0002ÍÌ±\x0015?úËo3W|ýë_çë_ÿ:ív4Í1\x0012cà»ßý3~üã\x001f³¶ºÊíÛ·±Öæ
®>Ñø'·>¢³v?\¾Á'UNj\x001aG§ôïÍøµÖðÎáCÀZ÷\x001e!\x0004Ij(\x0007#¨Î¼Z
¼ Ã¥¦goìØ/30M(Jâh \x001c>\x0008°KBQÌð6b\x0005I³	Q"Ó\x000e+\x001b;Äzó\x001eï=Ö:Bð\x0000(¥Rb´AFÉî]z½.R\x0008æË\x0005I\x0010@GG_+,vb©ë\x0019ËÉ£Oîð>àÎ8Ð_¿ÊBßâÒè
÷\A%óâÖù$)/¾ÖE54ËÑ)ÙÖ&÷ª#\x000e>rñú\x001cñÝ\x0006%)gW»\x000cÖÖ ÑÂd\x0019\x0002\x0008!è\x0004¥\x0014ÖZ¼÷\x0008\x0001Æ\x0018²,\x0008! \x000e0IÂt2\x0005\x0011ILÎÎ\x0002\x0017Î1:ÍÍ\x000e	1s<oádµ\x0016B\x000bò4a4\x001d1_l¬\x000cÐ\x0004bô¸\x00180Ê \x0004H%è·®"8ZÖ´ãý½wx¶÷l\x001b/±¿XÒ-NðÎ29ÜãÍÿôlÞà·ÿÁ?âS/¿\x000c@$â£X\x0016|çÛßæ;ßù.íNª®1\x0012½çüå«ôÛ
nß{Ûwv¹yö+ìwÚtòH\x0015\x000c\x0007ÑòÿÞ;O\x0017ü£¯Ç\x0018Ið\x0001¥\x0014\x0008IÊ÷&ÜßþmhØé\x0014QVÄ~Ì\x0005V\x0004#Ër2ù\x0004%<½ãØ5ðÖ\x0012ª\x0012x/ ÔàA*l"$Èz\x0004B\x0000 µÂ{1âCkM\x0008\x0001\x0015\x0005^~¿Ïh4Ä.="x@²Mp³\x0005ËÙ\x001c7Z0\x0019?coöc>\x0018pkÒ£Ûï`1FA¿ßEå;fO8ÿfòø\x0007¬\Z²ríe¬[â+M½b¬¥¹¾T§´òÈÚZÆd\x0012|
ÂC\x0008¸Ê¢FkM\x0001W9¤H)	Á3Ï±Ö#Â9Î\x001b
úý\x001eJJ"0/q\x0016¤i2<1¼ùÓÀ¾0bÂ'ãÈþáFÓÒé¶©¢ Õé1\x0018¬gMlô\x0010\x0002Fid\x0004­
J	\x0016E09UÏ3|¿bc½Ç¯¾ô\x000b\ÎW\x0018>}Â¿ûþÿôð>×v¶8Ìöwhnce0 ÆH¨\x0016T³!óð£¿~?û³¿ v²,)$MÉ²^~ñé>\x0007\x0007cæ% ,\x000bÆ>Eö6(GCþßÿù\x0003vÌ?øÆK(	ã¢æç\x0007ï?Ôüå^Æ,QÈ
i+rå¸Ú-è,±Îa\x001aÔÁ ¢À¹£ÇË\x001a\x0015k¨¦`g\x0004ÑÈ$[ýqM\x0014\x0006oÚÔÕ3´V\x0008!1\x0002 @\x0008A\x0008\x0001\x0010ôº}²4ÇYOU{´I°ÃÅ@=>d¼û®Ü~ð'ã7ÙüÜmT½M3]'	ózÉ6èod\x0015×¼\x0001É 26ÅÖ#D\x0008$YBHÜbJgk\x001dÒ\x000f%Ä¨Xï$tû9d]¢6(	Á;jïJ!\x0004D@úså²Àû­kDèÉdÌúú\x001aYÓl6Ï\x001ec]ÄÙ\x0005EÝá½\x000fl^Ê¥³9ãeäèdHõ¤Ä\x0018M§Û¥Óé°¹9fãÌ&kuT\x001a@\x000b\x0010\x0011­\x0015R*¤ª	Þá2OcmÀßzí\x000b,Tà[ò§\x001c½{Ñ(°t\x001b\x0014Õ:¦w\x000eàõ\x0017^ Ûé\x0010l\x0005årrÌÌ%\x0008_påü:\x001f?xµ¢ªRrõÆKtZ\x0019\x000f\x001eq:®H¬8Ì_cº$mC½,ñÓ\x0005¾óGß~Ï^ia³>ÿê}ÉO3
'Q¾DÈ@)\x0000EéøèDÐUMjÝ¦P\x001eé¦x[ \x0010x\x0010ë\x0005a1!FEH6\x0002\x001a
ÃéhLY+ÒDáAg
êåv»
kk1\x0000H©hä
I\x0008!P-k¼sX[S¸º\ÒYxðà>·?yÌÿç?cûS\x0013þáß\x00084R2\x0003Á\x0015h$Z4I\x000e¨\x0016N¬]nST\x000b¼\x0007[8ªÙf»GPmL³\x001f®nÓìögÌ\x0016y¥î8×ÜB+ð>B\x0004$\x0018A\x0008\x0010B Æw5Z8\x0004\x0018#úÑ£GÜ¿,Ë¹zõ
\x0017/^fcKòlÿ³g_Àä
¼ù² ,\x0007H µg¾,\x0018Íæ´\x001b#NGc\x000e¹té\x0012Ï] \x0003²¼\x001a\x001f\x0002Îyfåªò\~é*\x000fÌçüo~\x000b/¿Ì£?\x0007·îÒë\x000fÍf9sk® Â\x0013´w´²V\x0008}í\x0006?\x0005\x001fÜyHÅbN«Õæ^À/ö\x001eïácB9\x001bÑyö&Ìu¼­)mNõô\x0011b<Do\ç`¾äÿõí{\x001cõ_áIj&$¹à«\x0012\x0019\x0003$9"o3\x00130^Ló)b>\x0004çñ(P	ÌO\x00081¤
¤N ØEa9<µÔbÒ\x0006!8Ð4md°\x0008!év»eI\x0008\x001e\x0010h­QJQÛ\x001aÂ;sùbÁ¢.)9¹üoßû9·¦\x000böç\x0005ó¥\x001c)\x00041\x0008p\x001a¢Ñê7[4Ò
\x0002P\x0008\x0007:!,f\x0008"Î{¢·h-°1 ò>åò¬Ù¼°Æñ½\x0005Å\x000c²ª\x0019\x000fO\x0019¬®¤)BKB\x0008H!\x0010B\x0000 ¤\x0004\x0004µóTA!ÇGÐo¼ñ\x0006RJ.]ºDQ\x0014\x001c\x001fe\x001aÓØçøá)^²\x0007¤UÆÉÌå)­FÊt0N\x0019ÍfL\x0017s£!ÃÓ1eÁKWHW5ÖV\x0018\x0010g^¬µV0*\x0012CKIÌ\x0014áJÍ/³±yYÒ=3XéòDMÁAÖt¥§·XàG§,G'Üúù;L'sz½\x000eóÙÍH®=÷<ä½\x0007GÌæ\x001e%\x0005fqt\x0005U\x0011Óg²Ä½JÌÀÏùó£-d0èL£\x0019B\x0008|e\x0011*!\x0012¯Jd9A,Äj÷\x0010£\x0010ó\x0003ât
*\x0005õÄl\x000b\x000epö\x0018¥\x0002$\x0000à\x001d6(Úí6F\x0003ç\x001cJI¼wàAÑ\x0006ï<.X|\x0008T¶f<0.±x²ì\x00173d*I\x001aöÄÑhg´Cg°Ê`­4\x0019å|\x000fÅ\x001e¸#ðØZa$,çÈ¼$¦]DÞ¡²q6çÇß±,&´á x!
*b5\x001bh¥P"ä\x0019I¦^\x001a9ÁgÐi6Xë·ÑÁo}ëÛìííÑh6\x0019ôWiä\x0019ÝnÎ\x0013ï©ã!±<\x001cÎ¨ÅY\x0000bt:m\x0010¨©bQ\x0015Ìf3³)»{{ü¼ù\x0016«+käÝ6ý~\x001f¥%&O\x0018öOéw\x0007ôZ=:i
#\x0014Qe¿ø\x0002?|ú3>ÿ¯Ñ)\x000cÿîÑ7ÙR'<¿}\x0005ÂNÓð	§»O»Ô
ç\x001c³Ùùt\x001cR\x0014s6³ù\x0018DÙ9½ú©k£±¨Í-âlw5éê\x0006Ëæ*A)2èDcà\x00021Fdt\x0008W\x0010\x0016CÜèèk\x0010	H\x0003U\x001d\x0013ê@Ô9²ÙAêX\x0008?\x0003;FHIt\x000eo+N @Ô\x0006ïçÀ\x0018Ãr¹$MS\x0000ï#!8j[âCÀZ\x0001pÔ~IÞ\x0008Û\¿róvFU(Î^lÑ]»ÈÙK/aÇ\x0017p1dMy\x0017[?¢ö5J§ \x001b8;Æ+K=\x0014\x0015äYD(Òæ
Ëñ>ÝÕ³|ð\x0004ªÂ´2Jé¶ü_¾B¯ ¤Gi¦Â\x0007-Js=f<H¶°Á\x0012ñè[·nqöì\x0019¶·wh6\x001bÄ(9=: kY\x0002^ÃÒjµ\x0019Møð\x000c\x0011Û8\x0017	uI#OIAÏ5óÅº.uÍñ²äèðB¤)k\x001b+9»Í²ª8\x001eÐhæ4\x001bM:\x001e«í>+l³X.ùë\x000fß"{©Ëkò\x001a_ÚøEþjù\x0011«åà@8V!Ë'{\x001cÕM^záyRÜºuýý}nt¯páÒK|ë{oñäñc\1e0¾Å0û\x001cyr¦]p{.\x0008y\x0014\x0015:ÓD\x0012\x0004ï<ÄH¬\x0016à
âr,'HW\x0012\x0000BÅ\x0018æ#bÔÄ¤0\x0019\x0012I$\x0010«\x0012\x0007$²¦Ùi1\x0017Ôó\x0019ÑÖ¼KÈr\x0012Y`­E)E£Ñ Æ÷\x001eHD\x001ed\x0004­\x0015±r\x000cz]ºÝÏÿÂ

õ\x0011ÚÜ1]Ö¶r¾ôµ_£¿Ù¦­ÐhµAÁ|¾ ªn2\x0006I\x0007%"e5"I¡*\x001c³¥7dXçÁt\x0018Ï-í\x0015O$uPGLÒ 5pý\B¯\x001d\x0010Ù\x000e¾û\x001cÖF]ptçÔÕLp\x0007¦¥¢(-KëÐív~¿Rº¶ØÚQõ­)ÖÈ¥£e\x001a¬õ»Y9äý»
Æå:\x0001²
dä­&BÂ|.(ªZH\x0012#\x0011B\x0012g2ÒÈrÒ$!Is²`ºX0n,pÑsÞ­P.K.¼ò\x001c§nÊ8æßä¥ËÌ}E*\x0013î
\x001fÑ7\x0011W\x0019Ò
ÖÖV1&¡Ùlò³·ßæÝÞG17^ý
¿üË¿Â'\x001eóá\x0007ï\x0011G\x001fÃúKÄtfq\x0017mS¼nSÆ6Ij¨t4	n¾$V%br\x000cÕXÏqÖ\x0002FD\x000b1Ø(S¢i!"z§F\x0005b÷Ó·±Æ3\x0019V\x0004¡0:A\x000ca\x0012<`\x000cI\x0004"1F¤T(¥HÓ\x0014ï#":¬·Dáiu\x001a\={óç8»¹àÎ»\x001fS/\x0015*öxã+ÏqõÆK\x00049A\x0019N\x0005Ú¤S&ÓS\x0006\x0011¤Ê0*C\x0004u\x0013ÒFÆÂ`¤í6N\x0018l¹¤¡\x0007T\x000er·àÌù\x000e\x001fß,Ò\x0010T¤\x000c\x0015ãéiô{LkÁbV¢lE¬\x0004±¨èifIå\x0000B£ó<g:\x0012B@)såÌ±Ò¯IÚGT®Ä\x00125É§¯Þâ'\x001f/9o\x0010ÆyÖ	f\x0013fdó%³bAUÕ¨\x0018A@a+N#ÒFF§éI9i®Ð\x0004FÇÇLýYÒ øÜ¹ùX<aägTÅ\x000bã\x0015¶fì\x0015'ÔÁñpæ,©v? D¸pá<(­Ù=8%O
¥|Áú\x0005²TòÂK¯r~6e¼`/lóÑ^À\x001bp5d\x0019"ÔP\x0005Bµ$,Æ0\x0010ª\x0002I¨k|\x0018=ÒÍvA°
²\x000eDèâ\x00141yH\x001c~\x0008ó}D\x000c8!QIN\x001b$­\x000e:m!\x0010":ÉÈt$FðÞ£\x0002\x0004Æ\x00186ÖzH\x0013ÅÚöYÖ6WÉ\x0012Ã­{\x000føøö!/^ºÊ°|Ê\x001b_»Ìóú%Ú-EE
\x0011\x0005®
H¡YL\x000b$\x0006@\x0012CE\x0014¨«%­ YF`«J.HÅìÏ~î"ïÿì²,ÉD+jô$âÆ»¤Ë]ülÂtY`\x0017KBUá¬£ÕÒ£\x0011HôÉÉ	'''Ä\x0018Y]]¥Û\x001dP×F\x00169sñÇ'¬³ÖÚbÕÐ0{4ó§|ïýÈÉd\x0013¼ 8Ö	*1´º\x001dÒ<¥\V,\x00163¼õ\x0018X,LÆS1T®FjÁéÑ	kj@iJòFr¸äè\x0004v\x0015âÈqX\x001c3jÌ\x0008\x0011f³\x0005³ù££cB\x0008L§S\x001e?~LÏ~áWè\x000fzl®ui´\x0012æà~#ç¥8go6g6õ¤k	µs\x0008W­p5\x0008[\x0011gSBmÑÂ\x0011'X\x000f¾F\x0004\x000fÞãd\x0003ò\x001c©
rv\x000c£;á\x001düä!¡!´\x0002¥\x0010*\x0001­\x0002bØb\x0001B¤M\\x0000tF«©(«
c\x000cZk\x0000²¬ÁÖÖ:\x001fß¾ÅÖÖ\x000e³ÅùCv÷1L¹t~ßû½ÈÚºb}sI\x0005µ+02 ¤"Dw\x0005y#£*,Á×(-Hô&U}DTÓ,\x0014T¾ÂGA³,%E9¥,;ì>!âE^ze§<æøôL+4'J)\x0017K°¬ñEM]Yb\x000cäF0h
9\x0008\x0004º×ëÑh4\x0010BpþÜ9Ö7¶ú&2$\»>á{?lð`²ËµÎ&\x0017M\x0006[].®ÐÌò'?*\x0018ÏÏ\x0010Áú\x0012çj(­i·[dº¬)\x0005QDæÓ\x0019&1h­)\x0005I²ÝZ%I\x0014³é;Ë\x0007LÚ3ög»<\x001ej¼\x000f<¨\x0010k(\x0005·\x001fÒ\x0014ù|\x0010\x0002k-Óé<Ëùú¯|í-rÁl|L9;¦i*öiOOè°Â´ÕfY;R$Þâ\x0015¢\x0004g\x0011u\x0008\x001e\x0017,T%ÂÕ\x0010$ÑdD BÈ§ïÂÁÏñ³=\x0008(sDÚD%
dj \x0002@ô\x000eoKbÐ @*
BPE1	\x0008µ\x0016)\x0014R
¶v¶\x0018ôr\x0016ó\x0019·ïÜ¥Ùl2\x0019±Ö±³½ÍÖæ\x0016Jôév\x000cy(#ZEÊ©kðÁá@\x001bCµÌxv_Ñh­1]æ³\x000f/p´óä¾Ä&Uh\x0011Ê³ì\x001f\x000cjR³Æû»¬nµi73é\x0005\x001e=ÌON(*[B¹¨)kG]ÖÔ¥Å9K$\x0002\x0002I¤ß2\x000cÇ\x0015\x0015 Ë%!\x0004¤Ü»û\x000f\x001eqñÚ\x0012ï\x0015\x001b+5ªÃX\x00111  5yårãÑ\x001eo}P0\^"ú\x0006Þ:"°,
\x0004\x0002c46n\x000bg-²d:ç
LP\x000bd2aÛÔ2ò¤ù\x000c§KæcÏð$Å·\x0004ÃÁ´ÈÜÞåÞ_¾Ëõ\x000bW¨ªº®Rbm1ÑÁ#D}Ìt>¦X.\x0010BÑêöÙ\x0012FÛ³¿ÿ\x001fd>"P\x0004_à¦3Ä\x0010~ö%Þ:b\x0014\x0004B"A-\x000e`ï-âÑ{øÅ) !\x0001©!TÄª&`Ê "z\x0002¡\x0015BH¼³8[ \x0006£IAn§àqÎáCàÆó/±µÞ£Z\x0014(©h6\x001bdYJ³Ù¤Ñl°¶2àÑÝÀäÀP»@\x000e­\x0014F%ÔÕ\x0012\x0017\x0005QJØb÷~8gem\x001d©\x0015ËYG\x000fÖLRvÎR¹\x001e¢Ü \x0008Ø}t³;MÊ¥Ä\x00165ÎÖ¨<ãÂ¥Ë8»IÀQ\x00155¥uTE-jl]\x0011|\x0008\x0011ðD\x0016ô:)£IÞßßÇ{O$xï	\x001e\x001a\x0003Iå!K4««Óa ¹R¢µ¦é;(!ÙéwxùjAUróþ]\x000efW±Aå\x001dÎ[¼
Äe@(A"
(Ií<~>Ç{©\x0013.øu\x0013ÖC&
Ë¾9SX9l3/g<öÇ¤Ý n\x001esvm\x000f\x001f\x0011B`>SU\x0015u]³±6`9?BÈ&³ÅÙ¢F&Ýþ\x001a[\x0017®ðÊÆ&¯.J·-ßºµ@,§bóè\x0002:xï>\x0010eN4
ð\x0015jþ\x0014yø>ñàçøj4\x001a¡D\x0014"D"\x0001D\x0002Þ\x0012ª\x00196XT£ò\x0014i\x001a(c\x0008Þ!\x0010( \x0006\x0016Udì¦\x0010\x0003!\x0004Ö7¶ùÌ+Ïø!Á´M	­VN§ÃÖæ&óÅn»w)ÕBR;­\x0001!PÑøà\x0011@5HAð $\x0006\x000f1 e³5ÎWX"ËjI\x0016\x0014ínb\x0011X.kêª¤®gØ
¼ö\x0000Fk¢µÔXêÒâJ­\x001dÁy\x0002@\x0002Ä\x0008Hzí\x0004[:ôÊÊ
1F\x0000Ò4E¢è÷\x0002.î#$q[<=l^rd'l<¤4´åÂzÓs\x0015	âã\x000f8(®\x0012Ô
"Föø ðÖR9O\x0014\x0001\x0013\x0002Q&ÌãVá¹ÞÙ NR\x000eâ!Ãù	[eAÙ`¿ØãIkÂ¹]ùð'o}ÌéhR\x0010\x0002ív^¯µ4Õ\x001c\x0016¬ê\x000eysþZ<o"¥\x0000 ,*Öú\x0003þ/+8\x001aüõ­\x0005Òz¯\x0008®Æ D%±FO>'oáï\x0010\J\x0012bÞ\x0001)\x0011\x0011p\x000e\x0002kAi\x0010\x0011#ø`\x0005!8TâI@%\x0006ïKìlAwÐ\x0006A" ¥ä\x000b_ýeÎ÷rÇ\x0005oß~Âêú6JiÄg9Å²DDp¶D«\x0006\x0001\x0011\x0010\x0008l,Q\x0008p\x001014H%Y.ÇäÍ\x000eÞÕ\x0008\x0019°õ\x0018-±t¸Z\x00115äMEÞ)Ñ\x0007½úÞÖ\x0001\x0007gñ~\x0010"A\x0006lpÔµÃº¬p¾&\x0002H\x0002O$F\x0008D\x0005Vz\x0006\x001dB@)E\x0011ç,ZIð`EM¤¯²8ì1<eg5gê'hÝÁ(Ãz7çâN@@2ãæÝ[<]'È5´ÈèJâ¼%X\x0016F\x0005Å\x000bÍsôt²,y6{Âä\x0000rÍú²­\x000bº\x0003ò½\x001aýÐ\x0012«Èáñ\x0011ûûûH)È²\x000c!$+++\x0000\x0008¡9ñ%Ö760Æ$\x0006!$ÖÖxïñÞ³XÌéeÿáË=\x001aõ	§§é¬f^z|¢Ý1ËÓ]&\x000fßÃ>\x0000_\x00009*kc\x0000\x0004Ñ\x0007D\x0008óÿ'\x0008¿.M\x000fÃÎïÿ7|¾s¾üuîéî=\x0000\x0006\x0018`@\x0008D HT¢L®´^y©µ]å²¥RË¾/öÂ®½ñ^èÆ[e®TÔJ+KZR²	QD 0\x0018`\x0006;§/§ÏàßÏ»
Tw\x00164 "Àâª\x0012l\x0017\x001eÇZKÄ 
År	ÞS·=à¸uç\x000ew^¾N5zÂ½ý	ï}öõÍ-  \x0008\x0002µ\x0014ó9B
â$àÊ\x0010%`¹ôdKKmj¬µ\x0004Ä\x0012OT0U\x001709\x001b±¾¥i¬ô\x000eÚOi5wé­D¬ìÌ¸pù3Ö/\x000cÐ]ÒÉ9µ(\x0008ÚÝg	¦ÚFH\x0005ÞQ%\x0011\x0015uSU5Î8<\x001eÀa\x0011³`­EjA\x0014\x000bÄoüÆoø­­-nß¾DðÎ»¿ (O¸ùù\x0019íFÉÉ\x001dö\x000fGÄë\x001f°Òµô\x0016¹/ÁzjoÉjËdå5E*.#¦õ\x0006:Hh5t»]\x0002\x001d`½Ãã9ÜÛ#-yûòç¹¼u\x0011¼Ç­*²ØM´Ç?zy9çó·^'\x000cb²"g: µÆ9G\x001cÇ<~üÓÓSÂ0äâÅüÎoÿ\x000ef$I\x0008Ã\x0010!\x0004eY¦)UU\x0011!F\x0013­$EYRT¬¬H³%£³\x0013ê"çì|Æd4C© Ô\x0008­â\x0004!%\x0002I\x0014F\x0018c(Ê4]âjÔí\x000b;Ú2]LIÂw?#I\x00126.\b¶X²¶¶A£ÝA	÷\x0016M\x000e&ãÕ7ÞäÂúÃý'|òéCÒrç×QJa­ÅZR
¥\x0015ÍæË_¾L£á°Va¥¶\x0015ÎY¤ô8,B8¤\x0014H	ZGÌÎ4Z12Ì(Ë\x0011³3Î\x000fJ¢(¢3tt\x0006«DÍ.ããSNÏ¨e×\x0019ÏôÀoã\x0001!\x000cW[9¯°Á\x0001Îy¬³xgñ\x001eð ´¦Ùl\x0013F\x0001Þ{ôÑñ\x0011\x001b\x001b\x001b¼üòË(¥øþ\x000fÀû¿zÀ/~\x000eA8¡Õ:Á\x0018C\x00154\x001bMªê^¯GQ\x0014DQL¿ß'M\x0004f{{\x0017C\x0010$	kk«loï`MM]\x001bÒ,å{\x000fÆ<Ú;Æ\x000c¦ô:×1¦f%êÄMÄ í¥üä/¿GYV\½v\x001d)%\x001eO#i°ºº
\x0008@óýïüä§´ZM^}õ\x0015ÎGçèY@\x0018\x0006Xk)Ë4M\x0001ã(h4\x001a(­qÖ\x0002\x001e¥4(¢³s\x0011)\x0015¯½\x001a"µÄ\x0019
!\x0005A i·Ú(­	Ã(É²ÑhÌt:E\x0000ßøÖ·ØßÝe2pã\x001büÉü)»»Ïyë­/\x0012E\x0011ÞynÞ¼I\x0018\x0008!9;?ãôôN»M´AW^»C»ÝæKo½E\x001cE8ç\x0000\x000f\x0000÷à½§ª\x0004BTH\x0002\x0000\x0000\x0002)\x0015R
@°¾!ÐZ£¤Ä·`}ÅsãD\x0000 \x0010\x0002\x0010°Òk×!Ë\x000b¦£	×.[\x0010\x001eç\x001cÎy<\x0000\x0000\x0000\x001eï=Îy¼w8ç±ÖÒH\x0012¶¶¶Â\x0010\x0004h)\x0015RI\x0000¤\x00144M:í6Z+¤H¥\x0010B$;o¼Î|>gss[·n±¶¶F¯×ãää\x0018­\x0003ÞÿWxïhµÛtÚm6·6¹pñ\x0002Æ\x0018\x0016\x0005æÄaðæúåMn]_%$nP\x0004'F#z½>YQ×5\x0017.ì\x0010\x0004\x0011»»ÏR²³³ªª°Öç\x0005««k\x0004AH¦,\x0016\x000b¢ ®+¢(&I\x0012´Ö(¥¨ª\x0000\x0008t÷\x000eï\x001cB)FV»M\x001c\x0006º$ËrÒ,£ÈK\x0010e\x0005++}êº"Ësâ(fee\x0005¥\x0015Ö\x0018äEA\x0010|ðÁôz=>ùäSþôOÿ\x0003W®\áÕW_¡ªk¤RHéRb¡¬*Ö7Zt»\x001dò<G\x0000uU¡¥\x0004À\x000b@\x0000\x001e¼\x0000!\x0010\x0012¤\x0010\x0000x\x0000< @\x0000ð\x0000\x0008\x0001\x0000àñx<\x0000\x001e¼Ã\x0001R\x0008@ < \x0004B5\x0015³É\x0019Yb½Ã{O³Ù&\x0012"'"´Ö\x0000xç\x0011\x0002\x00148ëñÞ\x0001\x000e\x0004\x0000h)@
÷\x001e!$½^+W®pçõ×X][Ç\x0018ÃG\x001f}Ä'|ÂÕ«W\x0008£\x0010)\x0004o¾ù&Q\x001c¥\x0019ççç¤iÊ2] ¤BJ	ÞszzF\x00104
ÄQÈ\x001b¯Üà¿þÛ_g{5¦Õ)ÐI\x0003¥\x0005ÖÖ\x0018
Ò¥!\x000cCªª"M\x0017\x0000h6\x000cC¢ ×ë\x0011\x0004\x0001Þ;â8"\x00084e³XÌ)\x0002!\x0004Q\x0014\x0011Ç1Zk\x0010Xc\x0011JB]#0\x0018nl³ºs­Õ!n\x001b¥\x0015ueXf\x0005£Óc>~Àb1Ç9Ët:¥Ñh\x0010E\x0011ËzI\x001cÇô{=Z­6:Ð8ï¨ªwß}7ß|(
yþü\x0019/Þ¼ÉÖÖ6EQ ¥¤Õj\x0011Ç1Þ{1t:\x001d¤Aç \x0004x\x000f\x001e\x0010 \x0010\x0007\x0004\x001e\x0014\x0002!\x0004B\x0008\x0000À\x0003\x0002\x0000\x0000!\x0005B\x0010\x0002\x0000\x0000\x0000\x00018\x0000¨ª
ç\x001cYq~~N·Ó¢ÛíñäñCþôßþKv?û\x0010o\x001dA\x0012\x0013Æ\x0011Í\¾vª*HZ}zý>ZÂÊê*½þ*\x0000\x0000BH@\x0000\x0000 µ\x000e°¦Æ{\x000f@\x0018\x0006ÔuÍgwï³r|B\x0017L§\x0013$áôì@\x0007ÄqÌþþ>Ueèõ:\x000cCsüà\x0007?`mm8R¦)yÓjµ\x0008¥äÆÅuÞ|ñ7¨³SªrFUÔ\x000e´R\x000087e½¥yñÊüüãS´\x000eètº4-\x0006\x0001Q\x0014QU\x0015F\x0003k-RJF£1Zk²,#\x0013Z­&EQà½ÇZ\x000b\x0010\x0012é\x001cB)\x00040Øy­[o°Ò
¹Ø×¦ÝSËY&Y	ssÁµm=ÒÃ{,)³ù$Nh4\x001aTes\x0001Ýn\x0017ï<Æ\x0018ò<g8Y]]%MSª²äW¿ú\x0015UUñõ¯\x001d \x0008\x0000¨ª
­\x0015q\x001c"@JI^\x0014Q\x0014\x0012\x0001À{\x0010B\x0000\x0002!\x0004B\x0000\x001e\x0010\x0002\x0000ð\x0000!\x0000\x0010\x0000\x001e!$B\x0008ð\x0000²ªÈóÙtÊ½»qrtÄñî]tüè?áñÃ\x0007\x000cº-\x0004J"äþ\x0003>|çG\x0018S£\x0004!57oßæK_ÿuz½!\x0008\x0012)\x0005B\x0008\x0000\x0000´1\x0006c-\x001e\x0010\x0002!\x0004UUñôé\x0013>úhf³I»ÝaoápH»Ý&" $c¼sTU$I¢\x0008­5F\x0003­5UUÑ
<ë\x0006NZ2#´ÆZA¾H	\x0002A\x0010jêª\x0002oøöWoQåd8à\x000b_x\x0013¥4Ï?#Ï\x000b\x0000F£\x0011eY\x00020\x000c\x0011B uÀÊÊ
óù¢(hµZäyµ\x0015J)\x0012h\x001d\x0010E\x0011­Á6ÁÎ«<YjúMÇ47üh×ðÙÈp÷¼"¯\x001dq 9É<ø\x0002¿¹¢èÚIóår1n·Â\x0013!yóós¦Ó\x0019?øÁ\x000f(Ë(ÙÝÝÅZÇç>÷\x0006ÖZð\x0010\x0011J)Ê²ÂÔ\x0006­\x0003RdYÆ\x001fýÑ\x001f±½½Í/¼ÈÅ\x0017éõºH¥\x0000\x0012\x0010\x0000 @\x0000\x0000\x0000 \x0010\x0000\x0000\x0000\x0008@\x0000\x0000\x0000P\x0014%'ü»ý/ø«ïý9³Å.û»{Ìæ\x0019RÀx"¥$Ôv+!-+\x0004^³2P\x0019Ç|:áäøíKKÍ&\x0000\x0002\x0001\x0000\x0000®ë
k
\x0002\x0001@]ÕXk\x0011B\x0012E\x0011B\x0008Ò4EkÍ`°B«ÕâÚµëÜ¼y4MÙÛÛ£,K¦Ó)Ià½Ç9Rf³I£Ù`½\x0017³½\x0012c«%ebG¸8lb`69E

)\x001dqØä_»M®wÍfL'\x0013\x0010\x0012cjvwO\x0001H\x0006Ýnë×¯S×5J)´Öt:\x001df³\x0019eY1\x0018¬PU\x0015Þ{¢0D\x0008EY\x001bt÷\x001a\x001fN5\x0006Ã[!GKÇ½³gKe\x0014¼Ñl6\x001c\x001f>2Ûéò[ÍU6Ô\x0001h1ããcVWW\x0011Àx<F\x0008(Ë\x0002ð8gét:Ü¾}\x001dªªbuu\x0015ï=åªª°Öb­%/
XkÏçüùÿ9ÞÃíÛ·øÚ¯ý\x001a_xóM67·PJà\x0001\x0001\x0000\x0008!ðÞ\x0003à\x0011\x0008\x0000@ ð\x0008\x0004\x0000\x001e\x0000\x000fÎÏùÿËÿ?ýÿ»}FWô×VYì\x001dpv>G\x0000B)dåÐÒÐM(<8Ç,-)kÇ`Ec¼`<òËý¨5àÎ7R"¤D\x0008\x0001\x0000N\x001aMÖ(%1ÆprzBçC)R\x001aç\x001cRJ:\x000eA\x0010 $Çc\x0000\x0000xïã\x0018ï=ÖZ±ÊÑ\x0017\x000b"ë(sKm3«)³\x001cgs­H\x001aMl»ËÉá\x0001±()¡¡è·;\x0014ó\x0011ßÿÑ'Ìf\x000b©	F£A\x0014E8çX[[c<\x001e³\.ét:\x000c\x0003Â0¢Ûí2Î8==cgg\x001bk-UU/6^d\x0014®\x0003\x0004Oe,ÏÆÇSÇ¯\x001dÍD\x0013ZÅÙ´$ÎçøÅOöº¬t\x001c¿9ÐøbI][¬­Ïç8gY.,)''§(¥xûí¯òÊ+¯pëÖ-¤\x0008!ðÞóÑG\x001fñìÙ3R¼ñÆ\x001b4\x001a
ò<Ç{\x0007@\x0018QDºX²»»ËÏÞy\x0007çk_ý\x001aÕ\x0001ÂK\x0010 \x0000\x0004B\x0000\x0000Þ\x0003 \x0000@\x0000\x0000\x0008pÞ³÷ô\x0011ÿö_ü¿ù\x0017ÿü8:â\x0004x\x0004,%Ë
8TH!°Æ" Í+\x000eéÅ\x0011×ºXëñRP\x001a¨­Å Ùß}Æ­[·i6\x0008\x0001\x0000\x0000\x0000z{k0\x0008\x0011B¢bssÃÃCË% ¨ëº®Íf¼óÎ;aHe\x0005S\x001b¬5ìíí3NñÞ³¿¿O¥\x0004:Ä9xóæ&­+=â+/ptZ²ûä.
\x000e4\x001e¢®	^¿C³Û&\x000eÔuõ^ÛãÊ\x0019Ïï"@kµ\x0016)\x0015FB\x0010\x0004ìïï\x0013\x0004\x00017nÜÀZK¿ß§ÑhÐï÷Èó<ÏÑZSW\x0015¶9ähõ-Þ;´ô¢ôä\x000f\x000fzüÁ
vbØmÇ-+d^Ðªf`slz\x0000M(Ë\x001a_8ç©ª
ï¡ÈKÒ4£(
ÒüÎïü\x000e_}û«è@#¥àôô÷ßétÊ£GX,\x0016¬­®ñòË/\x00030NIÓ££#1ô{=\x0001kkkXcùå/~I¯Ûã­·Þ¢Ùl\x0002\x0002\x0000ðxï\x0001ð\x0000<\x0002!@\x0000\x0000R(Þ{÷çüwÿ·ÿ+\x001eÜÃ$ÖÌó\x001a%\x0005eVPV5qH%iG \x0010¬´cúíN«\x001bM®l
ét\x001aà%£EÅ£IAêk$Â;\x0007\x0010\x0002\x0000\x0000\x0000m­C\x0008\x0012ç\x001cR
Â0¢Ó(¥HÓ\x000c¥\x0014Ýn0\x000c\x0000ÁÏßyÅbIUx\x000fÞ;¤\x00148çñÞ\x0003\x0002 K»Äzñî\x001e(Øéw1õÚ\x0019æyÆd:g<É\x0017%íNN§
\x0013¶V{t××è®msãò&ù³\x0000
!\x0004Q\x0014aÁZCf\x0008\x0001\x0000um8==¥ÛíÒëõéõúÔuÍd2fjc~2érþá¿Ù\x0001T\x0001ó\x0017¾ÈÃî\x00056¥ä{Mó/?-ù«iJ#	<£"#\x001eq?hñ­¾ -J0¤ÕjÑh$,Ó%¦®PJò7ÿÆßàÂ\x001däyµÏ>ûï~÷»,)ý~(Ígüûÿï	Ã·ßþ*''ÇPU\x0015B\x0008.]ºÄ7¿ùMRÜ»wñx5\x0006\x0000ïAàñ\x0008\x0000<÷\x0000 <x\x0017\x0002ï=Â{~ùóòÁ\x001f±Lk¼\x0017\x0004JàñàaQÖX<Æ{ó\x0008$@0lk®oµXí$\\ë°½Þ§Û]!#d xCh\x001e9[\x001b\x0004A\x0000Þ#@\x0008\x0001\x0000ÞÛÛ¥×ë! ®k>üðC¦Ó\x0019a\x0018  Ibâ8Â9Ë|\x0013Ç	ãñÑhµ\x0016¥\x0014\x0000B\x0008R\x0018c±Ö\x0010\x0018q+W®!ª+\x0014gÏ\x0018\x001dÝc.XV2/ÈòeáÙ?;f±,é*Ï[ÖQvh¿ÕæÎ\x001b7yåòñý'\x0018\x0007FÖ\x001a­%ÎIÀ\x00178çPJâ½g:\x0012!N\x001bk-Q\x0018²8Ë1¿úç¼\x0016OÉÒ{Ï°"àÉüßÿÍ\x0016×®^ãµ7>Ï¹NJD}Æ³l	&c»!èJPZÓn·ñ@\x0018´Z-¬µ\x0018k\x0019\x000eW¹|å2Zk¬1A@f\x000cyã½§®k\x0010H)©ë'O°XÌ©Ê\x0012\x001d\x0004¼ðÂ\x000bºfooõõuÃ!q\x001c³½½MUUH%ñÞ#Ç#\x0000\x0007\x0004à\x0000\x000fxÀ{¬säyÁógOyþô!a\x0018`Ó¼¶¸Ò³ºÖg>[ \x00104µBÆDC¿©¹ÔKØ\x001e6Ym¬vcz­&íFLÒLh´HÐU1Ãí5üÆËä^á\x0001\x0000\x0000\x0000\x0000=Í±Ö ¥Ä9Çh4b>\x0013Ç1a\x0018Q×v»Åææ\x0016,\x000bÞ{ï}±e1V«EÒHÂªª°Vág±ÌpÂrã¥\x0010"a¼8¡?Ø ,\x001dÚÎG\x0016QDÖ\x0011$	/®¶ÈSËìàôW\x001fqñó_â\x000fÿË¿Î¿ú\x001frÿÑ\x0001Zk< usªªh6h­	²,±Öç9Î9RÄqÂFÇ\x0011\x0008Ç¥KY±9»ÐçÝ§#Ò<åúêUå¸ÿg?cÆ\x000cVï`6^¥-º¡â¾ÆÙ@ÅèF¢¬Èó\x001c)%Þ{êº¦Ñh µÆ;\x0010\x0012­5RJâ8&I\x0012Ë%um(Ë\x0019Å²,iµÚ<|ôV«ÍW¿ú6F_}ð\x0001Q\x0014áÃ9G³Ùdmm
­\x0014Þ{¼÷ \x0004\x0002\x0010\x0000\x0000\x0010\x0000ÚXiÊ§\x001f}Ä\x001fÿ¿þ{î}ö1óE1\x000eCÇ1/Ý¼Â;ï~©j@Ò%ZÀ \x0019±Ò
é6\x0003Z¦\x0013GDZ«ÀUxßBë\x0004\x0011&Í\x0004\x0011\x0007´ZC¦Ó9B\x0008\x0010\x0000\x0000èßüÍïpéÒ%úý>Î9^{í5\x0006\x0001F\x0003!\x0004ãñãã\x0013¼÷4
\x000eãn·C\x0007\x0018ch·Ú \x0004Î9666©ëédÆîÁÝÓ1/æè@ôV\x0011QD7+(Ë%JÁ¥\x001dGm,gÓñ2g­09RÔ5v<ç£÷ÁÛ·ùÖ_fký2\x001e=¥òN¯ËÁÁ\x0001Y\x0011!ÆZò<G\x0008R
ï=u]ã½#Ísz­Ï¿ö\x0012~~Àí­\x0006ý¤Ï_`of¸ýÂutñ#þê\x001fòûÿ³\x0007ÿµ«_"~ñ«4£&M1'ð\x0015e]£$B¼÷äyN¦(¥\x0010B CM]×¸Ú\x0011hM\x0012'äyÎt:åìì²,) \x0008ØÙÙÁ9GQä\x0014EI¯×GJI]\x001bÒ4EJ5 ÐH)ñ\x001e¼÷\x0008ïñ\x0002ðà\x0001¼\x0003\x0004Î9NOOùô£_ñöï8|v,/É*KQ\x001b¬\x001bWV)ò²*\x0011ÞSÖª¬ô\x0012Ö:\x0011+vÌF¯EC+5TUE\Ø¦¡²%¡hàG\x0019ÉJLÔ\x0007\x0000\x0000@ÿÁ\x001fü\x0001A\x0010  ÓéðOþÉ?auu4Mét:ìííQ×5\x001fü1O<A\x0008RÁ`Àd2!bÍ\x0006Æ\x0018vww©ª~¿OÒj`eÀÏî\x001fqíÒ9\x00177¶ðÎ2Ì8?:d÷à¨\x0019³¹µJ Vç4\x0002uÁ°C,CN«z:áèÙ\x0013úÃì\\x00190Z.QRÑl5)Ë\x0012­5Zk\x0004\x0000  \x000c#\x001a\x0006\x0000Þ{ª²B\x0000D#\x000bè6"t\x001crûÊÜêíà³GwiE\x0001WV{'Käù³»F~r\x000fõõ¿Éç_ÝÁù\x001a¥\x0014Zk¤RDQµº®	Ã\x0010¥\x0014A\x0010`ê\x001a¥4Þ{â$Æ{O¦Ìçss\x0008!(§O\x0012E\x0011ÍfããcÂ0$Ër²,Å\x0018µ\x0016ë,Î9¤\x0008áñ\x001e¼\x0007\x00018g1µ¡ªk¼÷x\x0007O\x001e<àçÿé_±ÿè>gSÎg\x0005EåJ#\x0005\¿¸Î\x001f=@\x0000R
¼\x0017\x0004\x0012zvB¯\x0019\x0012E
á=Ö¯
eUc¬Ãz\x0001Ö¡¬C{ðÞc0\x000cqÎ!\x0000\x0000@çyNYeÖ8±Öâ½#Ï\x000bË%J):í\x000e/_áW^áìì4ÍùäIÓ\x0014ï=Þ{¶·wè÷û§®k¼÷Ü{rÌ½§lF»\x001f½Çû¿|Æà\x0002\x000föÇ|íËo²¾¾ÁÑóTy·PDs¶È)"òb1!LÆc¤T\x0004a@\x0018´Z-¦Ó\x0019J)¤TÄqÖ
!$Z)ðà\x0011xïX,\x0016,)¯l¯\x0011µ\x0003Ú\x0006uUÒô\x0015e6áþÃû<=9GXGn\x000cA \x0019´%Ëô»ßÿ\x000cü×X}ë
â8Æ{\x000fs\x000ec\x000cA\x0010\x0010Ç\x0011A\x0010"\x0004¤YFç(­¹sç
þÛÿö\x001aÿôþS~ñ_ `eeårIeÔuÍb±à{ßû\x001e·o¿áp\x0015­5B\x0008s8çñÞã\x0007\x0000\x000fRI¬±äyÁb¹¤®+Òù{\x001fþ\x0015gÇ\x001c\x001cO8ääµ\x0001À;Ëêp$8,p\x0014\x0012%\x0005Bx\x0002éh\x00058\x000c\x0008À8C¢b8ÀIuà=x\x0004Ö;¤\x0010H\x001c¦Êq\x001b¡\x0014à\x0001\x0000ÐB\x0008¢("\x000cC1TU³v»M¯×çÑ£G\x0008!â\x0008;6t:]Ã!Y±º:äûßÿ>Ï?ÇZR
cjÆã1Yá½gÿ¥\x0014w®0\I\x0018noqñÚçùÂW¾ÎÆjr~6¢(k¤ÐÄZs2^p-Ùè
Q\x0014
k
\x0007\x0007\x001c\x001dY_\x001f\x0012E!yqp°÷\x000b;\x0017	Ã\x0008!\x0000\x0000!@D \x0004uE(\x001d/_Û!\x0016%Ò\x000bÒÙº~\x000eÞ\x0012\x0008Ëlºà,3,jñN;a%i«\x001eÝÛE:Áßz(PJQ×5y^ µ&\x0012ò<#Ïs´\x000eØÜê\x0013Ç1J)¢`}}0\x000cY__ç\x001bßøu&	\x001f}ô1UUqzzÆ'|Â|>çÎ;¬¯¯\x0011!Æ\x0018&	eYÒëõPRRÕ5F8¨kó0\x000cyöè#v?þ!\x001füô\x0017<z¼ËÑéÚz¤T\x0008i±\x000eV×ûDquP+b-éÆnÄz§A3ÒH\x0005Î\x000b\x0016µcïx­!aCÓ@¡u\x0001^x\x0014 \x0010R \x0000\x0010\x0000\x0000èf³µ\x0016k-RJÂ0$i6\x0008´&\x000cCÊ²`2ÉL&\x0014E÷\x001ek- ¢ýý}NNNèv»\x0008!\x0018F\x0014EÖ\x001ac\x000cé2åûï¾Ç²,ø¿üÃ?àÍæÚ\x000e½/0yô1GÏNçx­\x0008\x0002\x0000\x001a¡¢ë\x0014uiPÊ¡Û\x0001½NÄ`Ða4Y`¬et>f2¡¦\x0004üõoÝ&/\x001d\x001fvDU{¤\x0008!\x0001±\x000e[Õ¼y}^SbJÍÝc:qÌ2M)²\x001c¬¡\x0017Â³iîXmÇx­YYéò­¿þ·p"b>_Wlmm±¾¾N\x001cÇ¼ÿþûXk©ê
ç\x001cÃá \x0008\x0010B\x0000\x0000 `ee^¯Ç;wøÖ·¾Me$I<Ïyøð!ï¿ÿ\x001eãñÕÕU¢(Bk²,±ÖRU\x0015E³··ÏÚÚ\x001aý~\x001fï=¦®XÌFì?|Ý§¹{ÿ1ãyÉ¼´\x0018ç	Ú[jëY\x001föÎSsh©\x0000\x000f\x001ezb«\x001b\x0011'
/\x0004EÅÇ»\x000bÆYM\x001cGüüÁ\x0019Qã9_~ý\x0016o¿ù\x0006½$BÊ\x0000!\x0014RJ´\x000epÎ\x0001\x0000\x0000 Rh­\x0001Öv§M·Û\x0001/pÎ²¾¾5ápÈl6\x0003<ÖZªªÂ{Ï7¿ù
R<{ö^¯ËÙÙ9\x0017.\de¥ÏÝÏîòá\x001fb§±ºÎ`}
5;áÑ»?am6#¨\x0017ÔU
\x0003\x0008!±Þ\x0003¤\x0015¢\x001a
¤ÒÄí.\x0017.pãhÎù¨EÿÂ-p5Gxï¨ª×n\x0005l\x000e\x001bÜ¾Ñá{?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=%í¬\x0011EBÓ\x0008¾öúUÖ.¿ÂÃ£1þÁCî\x001eMÑR\x0019OR¤\x0000À9G\x0008\x0010\x0002Zk´Ö\x001c\x001d\x001dR×,Ë(\x0002c\x000c\x0000RJªªF\x0003\x0000\x0000\x0000\x0000\x0000\x0000¤i</p><p>ÀÝ»w¹|ù2gÏe0\x0018`\x0001!H]ÜlÎ¯¼vrY)ÅÚ`À«WwØ<¡|«6²Ñ^"\x001b]FÓ\x0019«+\x0003¼ð(\x0008!0\x0018\x000c¸|ù2·nÝ¢,K¤\x0010\x0010B  @\x0018#É\x00044M±ÖòÒK/ñk¿ö«|ï{ßc¹\ ¥BJI\x0010#xï	! @k<Ï\x0011Jâ\x0016KBµ\x0004º\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000D@\x0000Î{NOOùøã1Æ`AJ÷\x0001ç<Þ{\x0000\x0019Ç\x0008!(ªª\x0008!\x0010cD\x0008Á;wØÙÙ¡ª*¢ ®k\x0000s\x0010\x0008!`Á\x0018Ãt:e8\x001cb´¡ªk¦Ó1i! Ñh\x0010BÀ;ÇÓÓ%t[O$\x000f>c{kîÎ\x0016/¯Y~üþ-îî¹\x001a?!O\x000cãÑ\x0018\x000eH\x001b9~öÑqaYmHTÖb¥;`6/)\x0002ç\x001cÞ{1\x000c\x0006\x0003Úí6Y\x0013#\x0010°Öa&µ\x0016­\x0015\x001a\x0000\x0000\x0000\x0000\x0000\x0000À9Ë|6ÃZK»Ýf0\x00180\x001a
é÷\x0007\x001c\x001d\x001d2:\x001drþÊ
º[g(«ù|\x000c\x0017._çÚEO¹(XÛÜ¦»ºÍ§?·à\x0007<æ»?xf#§Ñh\x0010| È\x00103gÎ$	wîÜa<\x001e#@JRv»M¯×£Óé$	\x0000+++¼üòËÄ\x0018yúô)\x0000Æ$\x0008!R"\x0004À9\x0007<Ï1ÚÑlò5®.\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000 F `÷`Èÿ÷\x000fþWâ²nN§C$$A\x0008I\x0011ï=BÀÁÁ\x0001'''\x0018£±Öá½Ç{\x000f\x0000@UU|òÉ'4M¢À{O\x0008\x0010\x0002u]# ªjÉðÞ±XLxò¸B*\x0001RQ,G(Òh&äYJ\x0008YíXê&2ørÄù­\x0001R+²°Dú\x0005ßï\x00105Ú':ËÊÚU²¤Íéþ\x001eÓSê\x0000J	´¤í¼Õ¥ß+qårÉÆÆ\x0006½^\x000fc\x000c[äyÆññ	Þ;¬õÄ\x0018\x0019\x000c\x0006Ä\x0018Ñ\x0000\x0000\x0000\x0000\x0000\x0000\x0000Å,ÏqÎá½gN§C#Ï!\x0006BÒ:s\\x000bÊº¤</p><p>\x0012"XËxxJi\x001dþ</p><p>RF¶Ïeyç)§§C>üðC^|ñEZ­\x0016"\x0008Rxï\x0019\x000c\x0006Ü¸qÑhD\x0011ï=Fn·Ö\x001aç\x001cUU¡µæÅ\x0017_äñãÇ<xðÅbI\x0008\x0001­
RJÑ\x0008!QJ\x0012cD)E#o$	Î;eÉøè!'osö~\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0018#åbÆÓþÿé_üÏ\x001fñ[×Î²øÌ\x001b¬êS¤IR</p><p>)%B\x0008\x0004\x0002!\x0005.]âã?Æ9s\x000eç\x001c!\x0004bÄ\x00181òèÑ#.^¼Èr¹$Æµv»Ít:%ÆH\x0019\x001aMIsÙ%M\x0013´\x0011\x0008!	\x0002¦Ã\x0019¾®°.R%vs\x001b}~í«ùõ×¶ðû\x0015;ÛgÐRà½åë¯]æ/ò1íµm\x000e?¾KáÆ\x001cM\x001fóÝg¼ýpYYÒV¬Ù&ëmr:\x001esrrõ5íVn·Ö££#:\x000eEQ²XÌ1à½§,\x000b&	&I1¢\x0001\x0000\x0000\x0000\x0000\x0000\x0000¤\x000cú\x0003\x0011 ÛjÓi·	. Öº¼s2ä¶=åÂIÅ*a%ï°\x001drt°GUX\x000e&?{/~¶`ã¨Á»\x001fßÅYËññ1o¾ù&\x0017.\`ss\x0013c\x000cUU±X,PJqùòe\x00108çðÞ\x0013BÀZK\x0008\x0010\x0002\x001b\x001b\x001blnnòî»ïRU5Þ;¤H©H\x0004c4B\x0008B\x0008ÔµE\x0008A\x001eë,Îyl½ \x0018?#1^o\x0000\x0000@\x0011[×Ì&#öv÷xøà\x001eîÞÄ\x000c\x001fs­Ð)|éÓ\x0017X-kV³þÎ\x0019._¸\x0000\x0002Æã	ÞYZí6Ýnýý}þâ/þù|NUU\x0000\x0010\x00001\x0002pttD¯×'\x0000µ5kkk´Ûm\x000e\x000f\x000fÑ:GÑ M¦´\x001a
fó9u½¤ÓË¸z~õ~Îö\x0015:«-¶v:¼úÊU¿º¶ g
¤\x0005;_²:þË¯A·OWkÆÏFüäæ-þãÝ\x0007<ô\x001b\x0019ývN²uR4(Ë#¬­°Îe\x0019Ífáp÷,ËN'\x0008!É²\x0017^x\x0001c\x0012¾ÿýïC¬qÖ¢\x0001\x0000\x0000\x0000"\x0000 ÅbÁábDhjö}Içì6»Ó	\x001fÏ<L\x0016<Î<nº`÷ò*Ó[\?]°°KéLkA&o¯ÐÈ¶y¶8àÖÓ'xï\x0010BS%\x000f\x001e<`<\x001e³²²B§Ó¡Óí\x0018÷\x0010\x00021FbÄ\x0018\x0011B ¥$I\x0012Ö×ÖØÛÛc4\x001aa­ÅZK$dY1\x001a!\x0004R*\x00108W\x0003 Ä\x0018Ã²X\x0012BI\x001a¤Ý\x0015¤6C¾ý§ÂÛ\x001fÓ>%\x001esûÑ\x0013
\x0017¤\x0012¾ò©s¬û\x0005þÖç^¢\x001f¦Tw±öüËlîì¤)B@¯×åðð\x0010ç\x001c\x0000¯½ö\x001aNñxµ\x0016)%1F\x0000bÄ\x0018ñÞsttH§ÓA\x0008IUÕ(¥8{ö,F@)P«(\x0007_þõ-»zÍ.×.÷Ø½U â¹Ï_£¿	6ÌIdsÊY Ê9óéÓgÇNîqþÏÑ\x001c¬ppû>?=\x0019³·¬é§~\x0017_å¯ü</p><p>?üÁ[<}ü\x0018¦$"ÄZR^¯\x0010Á`@UÕL§\x0013\x0000úý>ÎY¼s$A\x0003\x0000\x0000\x0000\x0010aV,øñÍwø·ÿéyóÎ»\x000cÎ_àÆ/#qOq²dfJÒ4Ã%
\x000ef\x0015Q\x000e\x0019ú9óG3\x0016Ë9ëi$§D\x0005ý^\x000béGÜ:ä-ÖÒ4MéõzlllÐn·ÑZã½'ÆH\x0008\x0010\x0002\x0000B\x0008\x0010\x0008!PJ¡BJIeÌçs\x0010\x0000Ìf3¶¶¶0F#¥\x0004@\x0008RR×\x0016)%R</p><p>|ÜHäbÂxxÊ¹_ãää\x0018[<~ë;ÜþÉ[\î§üÚ«iû\x0006W\x0007	\x001b[Û¼òÂU\x0006\x001eA&4}É\x0001ï\x001exî»\¿ú\x001cY!¥¤ªj¤\x0006 Ùlç9UU!\x0000 Æ\x0008@\x0018#\x0000Ãá\x0010c\x0012´VTUI\x0008ããc$á¹ç®qrz·
®\xÄoÿ75þÍ°÷¬ÁË¯}îú</p><p>ûw<÷ÞyÂ+¿tÒÏHò9ÏK\x0016\x0006ÉrÎhï7oóètûÑq½w\x000eÇ<\x001e\x000fiëf"(ÒS§Îüíßú[¬®\x000eøÎw¿­kNOO1Æ µÆ\x0018M§Ó%ÆÈéé)ý~v»C]W,K$!Æ\x0006\x00001r8\x001bñ\x001fßÿð¿ÿo¼õ×?`\x001e\x001dW>÷\x0005.ý\x0017¿ÎýÃ§d!±¶\¸x\x0019i2zU&kÛ\x001cÝ¹Kza÷o\x001f\x000cYÙÙf£­8Î,u\x0003he¤WùÆ7®PU\x0015\x0010\x0001\x0008!\x0010BÀ9\x0007@\x0011\x0000)%1F´Ö(¥\x0008!à#\x0000@m-UU¡´f>¦)Æ\x0018\x0010(¥\x0010B\x0000\x0010B ®k÷ÔÖÒL\x0013âbÄþÝ÷ÉºÛ¬n\x0018I\x001a
~íë_áó\x001b<ip®×ccû\x001c¡Ðê÷H\x001a-\x0016ádÊ\x000føÎ\x0007Çüü?|Ì/}é&ÿÏöOéÆ.Þ{z½.IP×5Î9$a±Xç9\x00001F\x0000b\x0010RR%Ëå$I¨ëº®qÎ!¥$Ë2\õÈ×~¹ÉáãÀÞçhw3ª¨éiðäö£=Ïã\x0007\x0013VÎP\x0005Ñ\x0017	é3DÚd|pÀñî1÷\x001fìÑØ^ÒY}½éGÓSÚÝ\x000e­fAá$ÙÚ5</p><p>\x0017\x0019
Üs~¿G»Õb2 À{1f³E&h­étÚ\x001c\x001d\x001dqÿþ=¬u,\x0016\x000bRTU1R8Ë¿þÑ·ù÷?ýK~~ë&ågÚqþ«_æÕßþ\x0006ËjÉõ\x001b/e9Í$GHÁ¬XÐë\x000f¨·Ïððß¿ÃT\x0018òÏ_çøÙ!÷ÇSÎ^8Ã§\x0006k¬¯åNe±8²L¡µÂZs\x000e\x0018#B\x0008\x0010\x0002!\x0004\x0000B\x0008R\x0008!\x0008!\x0010cD\x0008\x0001\x0000\x00001Òl5M§\x0018c°¶\x0006"Zk¤h­R¢µ&ÆH\x0004¬õ¸ºdïÉ}öO¦¼úµßD+
1â´¿ÉÖÚ\x0019´j6\x001a°\x0008¨X©6^f\x001cÏ\x000fø«Û»üÁÏNÔ</p><p>¥5?ÿø)·\x001f<äóy÷Þýe¹dg{\x000f\x001f3ÏXYY!I\x0012b\x0000Ä\x00181\x0012B@\x0008A\x0018\x0003eY\x0002P×\x0010\x0002­VÁ</p><p>+««L\x0017\x0005\x0017Î¥ä­üð?ìP×ëX'qÆ@Óè¶YÌ<»\x0018ÒÖ\x0001&1\x0008ÕEFI\)I^¸FÛö¸^@³7¡¿þ\x0001Ãµ\x000føb{@gp÷?|D=ÏYÔ\x0016\x0011-³é¿úþ_qõêUÚí6£Ñ\x0018#J)s\x001c¡µ¡ßïÓï÷É²·ß~\x001b!\x0004Ëå\x0012c\x000c\x0000êo~ã¿ønÍöøüÙ\x001fóþ;ï QeÉR®|ù\x0017SÓÎ[¬¯¯ã¢§MQÞÓH2²¬Éâôêñ\x001eóÉ\x0018³a\x0007Möw÷ð\x0014Ï9Ì<\x000f¤Bû\x00061@UU\x0014EAUUeI]UXk!F\x0000\x0008!\x0010B\x0010c\x0004À{\x000f@\x0010\x0002½n,M988Ä9\x0007@¿ß'Ë21¤iJ¦h­¹té\x0012\x001bë\x001bH%)Æ»<¸ùS\x0006ç^äÌçD"\x0010C¤´é½\x000f¨êÈ'O\x001eqxxL5Ú%o=<å_ÿxi­ñeJ3¬w<¼wW^¼ÆæÆ:{OùäácF£!³Ùº®ùøã±Ö"@\x0008\x0001\x0012!\x00041F@\x0010BÀ\x0018C]×(¥h6$iÂóç(5ÿìg\x0005\x000f\x001f]#Ë2\x0016ó9W¯oqþRÙ\x0008ÆC\x0000\x0003qÎF
ªQ=\x0016õCÚkkô×n°±sÎú</p><p>óÅOéWÈÅ	g.6\x0019l]&æ\x0005O\x000ej\½rÕÕ5¾úÕ¯²··Ç'|B³Ùdeeº®ñÞS×5RJÊ²¢ÕjbL\x00100NÉ²ÉdþÙÏÞæcÙÜYãÉM½ó\x0010Âæs7hnõYv§ÏîGL\x001f<CT\x001eüOÿÖß!Ïrn¼þ\x0019{í3Ì'cïßãéýwøÜ\x000b¤ÿÇÍUö\\x0013Q\x001fñwW-Õá\x001a³ñ\x0006óÅªª¨ª¢(°u\x000f\x0001ç=RJ\x0010Ä\x0018\x0011B\x0000 @\x0008\x0001@\x0011ë,½¬G¯×åôô
ò<GkR</p><p>c\x000cBH\x0000lmñ\x0011D¬\x0019î2skg®ã½Gi\x0005÷\x000eÒ\x000e£¼ÇÑ'\x000fY\x001cÐ6å£</p><p>\x0005Õ²àýáSö%Jjóè$pþÒKTºËÿíþ#.í´épJ³·FâcdccV«Åb±@J\x0010\x0002!\x0004\x00001F¤\x00008ç(\x0002$IÈ²n·ËÁÁ\x0001©Dr÷kd¦Ár¾`>·\x001cÍP*ceGóä\x0001øªàx7eóÚ1iv\x0019\x001f-È²ú\x0010©J\x0017j®\x0012V·ÎáÆï³8ÝåÜå\x000e×ßbVì3<mpíÚUVWWé÷û\x0000H)QJRU%u]ç9\x0000eYâ}`mmº®Y.Ä\x0018©ª</p><p>\x0010èüä§Ï7yíÕOqðá\x0019>þË\x000fHVût¿F\x0015 $<½ó.üé\x000fX9V|á\x000b)×~á\x0011§uêì×ILÂ².Ézm.}î³¬^¿Èùý?`»7¦ÛÌùáþ*ï~ì¨ü\x001e_ûUÇwßm \x0010H)ÑZ\x0013B ª*Ã!I ¥D\x0008\x0001\x0000\x0012ï=\x0000ibÁûÀh4¢Óée\x0019R*IPJ"¥Ä\x0018M&8gi5s\x000fnqº÷3^'Isj[£BJIUUè4Em^E>~Æöú*õtÎf³É±Õüû·\x001fqëé\x0010O$\x0004¡$yÞ¦Ó[E¦-î>=ä{OÈ\x0012ÅÆ à¹3=»¸I£Ñ Ûíptt\x0010\x0002\x0000!\x0004!\x0004b\x0000\x0008!\x0010BPU\x0015Æ\x0018Ò4CJÅññ	Ýn/|nP§,\x0017}Ê²¦ª*²äôdF\x001dÛ´ûmZ]Íôx-4õ¼IÝ=À$\x0006¬0|Àz¯áù³\x0005Y²M³½Áàì\x0016¾ÜGÇSFó\x0006¯Þ»O¶°ÖÒívÉ²\x000c­
Zkªª¦®-1F¼÷h­R"¤ÑhâCJI\x0008\x0001¥\x0014BþøÖm¶Ï\gtô	Ï]Ü`þü\x0015|¯EÈ$åî3îÿõ;'üÍ\x0017¿÷?<ÇW\x0010õe~8}ÆwË)Ö4¨¼¥5°1bZ+Ìú¯2yô³7>á7Îe\x001c¼²Õ®huJ<\x0005141"@)E\x0011)%Þ{êº&I\x0012\x0010\x0000Ä\x0018ñÞ\x0013cD)E³Ùd>_Ðh4X__g4\x001aS%k«kä\x0006ycæÅç/ðÅO_äñí',»Ì\x000e\x001e buã,óùªª(\x0018#itý\x001cfû*f²K'ÍW\x000b~üàwö\x0003Õb\x000ei\x000e¢¢ÙÞ »ºÍÉ¬¦:=¤¬-Á\x0005&³%ûGcn?:æ³óÈßùÚ«lllpûö\x001d´ÖH)	!\x0010c\x0004\x0000 Æ\x0008÷\x001e­5\x001bh­9::\x0002\x0004ÍVd±èâ¢¢®Å\x0012ç\x001cGGS\ÝC§
Z\x0006QÎ|Pº$½=zz\x0013!SðÒ>Æ4sj</p><p>ZÉu ¦µ²ÍrtÂâpÈúöU¦UöN*Ë\x0002!`8\x001c²XÌ\x00011¢µ&MSB\x0008Ä\x0018\x0001h4rúý\x001eÓÙ\x0014)%Î9¼÷\x0000èÁÊf]óèñSv\x000fÆ¸\x0017:x\x001fxú³¿¦zrH·öüö\x0017þÏüÍ_½ÊWw1¢÷S¶Í}Äâ¹ßB\x0004K¥4J) R÷^ ·ù>·Ýâ\x0017ïñ¥³×ùÜ«ë\x0004°·»\x0002\x0012\x0019%!\x0004¤\x0008!pÎQ%Þ{\x0010\x00101âC\x0008Rªª\x0010B°½½Í£GPJ²ººÊoüæo¦)ÖZb[aç¦UåÜïÏÙûdÕç¾Äáñ1£á)UUc!x\x000f1V»ÍÍã\x0005Ë{O9kj\x001c\x001cñW')Ãñ)1\x0014´ò\x001e­­K¬l_"o÷¨ê\x0000hPKt\x001e¡\x0004\x000eÉßÄùíu®]»Á\x000fþêxï\x0001\x0010B ¥$Æ\x0008\x0000@\x0011!\x0004Þ\x0007®_¿Neìîîbë</p><p>\x0011%ïµ8<<!ú².Ùß=fYöÉ6iÞ!Ë;ÙÄÓ	è\x001d,È\x0001ù!­µ\x0015òÅqN\x00144]#k	¦£Õµäñ</p><p>O\x000e\x0018ÏÞc¹\0<=e<Ï1\x0002 "ÆHQ\x0014(%ét:dY­+B8ç©ë\x001ak\x001dú¿ûïþì¦§\x001c=ý1Ñ\x0001ÓÑ\x0010\x001cÕã\x0019¯ì8.ý</p><p>_ýò«\¿ô\x0000Ä\x0003<ç\x00104iHÈþ·?ÚdrZP\x001c\x001e£¤¢wù"[7.óÂ¹\x00179k\x0014ûG?åk¿0 ~ûv)\x0001âºªÐF¦)u]S%eY"¥¤®kbÄ\x0018	!à½\x0007@JIelnnòéO¿Î·¿ýmÎ;÷7ß|4M)Ë\x000bçÏðÏ¯PLw1bB§ãÈ&éä_cýì9Ö×ÖðÞ¦)\x0000F\x001bj[C»û\x001dþø?¥\x0014lla¦\x001dÒÙ8C÷ÜXç9=x8xFiÖÂ ê!Y</p><p>J' \x000cÐ¿~ï\x001e»ÔBi\x0005\x0000@\x0018#1F\x0000\x0000¤H)1\x0002\x0011k-EQ&	\x000fîu°SEd,\x0016SN.Ç\x001c\x001ctÍ'Ð18å
V»}²ª Y´!$ á\x000c~©Ñ ÕÑi$,\x0004¦Ý§¡Ï]¢ÝG§çQñ³¾ÃOÞü\x0011uå°>Ðhd\x0008!\x0010B F\x0008<oÒnwh4r@ ¥À{s\x0010\x0002ú­þ\x0014a$¦\x0015vHÃ\x0014LfkÛßüÍ_¤>ø\x0002\x001b«Xí\x001f\x0012b$2$òñAÁ»?=æÛÏ8|ø\x000c?[\x0010¤\x000f>BØ/ópõK¬ol\x001eäÜÞ}BçÒK®R×{U	\x0008\x0010H©ÐZ£bgg\x0007ï=Þ{¬µ8çpÎ\x0011BÀ9µårÉë¯¿Îh4f<\x001esæÌYË\x0005\x001f?&MS$á7íu\x000cst4´Áú¹\x001dÎþB \x000c\x0015Z\x0019¬¬0Æ \x0002\x0000\x0001J)b\x0008üÖßø\x001aïÝ¼Ë£G0õÝ\x000fht×ÉVÎ3\x001dâÚgg>è#í£ %îS=þ\x001eÉô\x0003²V\x0007¤$\x0015ñlÁéØ¢\x0002!PJ\x0011c$\x0000\x0000\x0000\x0000\x0010\x0002ï\x001dÃáf³E»Õ¡Û\x0019P\x0017-\x0010ýã}f#º ²ñ¢d<\x001dÑÎ\x0004ä\x001c«+-úç^ ÛÖ¨\x001aü\àc\x0000\x0015Iã\x0002woF¢%+2Â´B.W0ó\x0017h%Gr\x0008Î\x0004>z´Ët^÷\x0008)	! µF)E\x0008\x001e<oç9ÖÖÜ¹sñxB&\x0010¨ª\x0012\x0000m­%¶MPBRZÍZ³Åõ\x001bWXñ\x0003uf@¯ÿ!R4(ã)\x000bq{û«ü/onðlu\x0016ì¼ÐF5³½=\x0016sËÝ÷>"Ñû;=þîÙ¹B¢A¸H\x000cªªÉ²\x000c¥\x0014Å\x001c¥\x0014I`Á9G\x0011ï=ÖZêºÆZs\x000e)%/¿ü2×®]ã_üÁ\x0007\x001f|@«Õâ3ù\x000c\x001e=¢X.Ù8³Å³+è\x0018\x0008Yq)\x001b«Ô:UU@\x0010\x0002J)\x0000êºÆ{sóç6ùå/|ùÁT²EÒYCæk\x0014²þ¥ÿ</p><p>¹þ\x0012Næh,Æ\x0017´,\x0014ùeb£Oõ#\x001cÿ´»F\x0015\x00041zÞþù'\x0010\x0002\x0004 ¤DH\x0001\x0011\x0000\x0000\x0000\x0000¤TÔµ¥×I6rùìEdÔ<Ýß¥®K$2§´3f§§Øãk¬ÇÙÞ\öPÚ\x0011¤!Z\x0016\x0019\x0004ëÆ¸ù|ed°Éòè\x0019ÇGßçäð\x0019e©pU,íòâ`ÀgÎ­ó¸[ðÉ³}|ÔuÖ\x001a­5ie\x0019UU1Y.\x0017TUEQ,\x0011\x0002B\x0008\x0008!¨ë\x001a$	 ¸÷Ð¯2*f|éÂ:çWÎPLÎsvÇ±µ9ÅÅ\x0006BäÔqÉ7?:âþ^à\x001cI\x0011</p><p>ÕIÙÙþ\x0014y\x001dsëí\x000f¨ëk<Ð\x000bþæ+¿ÌÒN\x0019Î\x001e#È\x0019ô\x0007D"!\x0004$!\x0010\x0002B\x0008\x0000¤\x0008!ÐZ³¶¶ÆóÏ?Ï¹sç8<<ä÷ÿ÷yçwxã7ø'ÿä\x001f³±±Éïÿþï3ÎiV¨Ðr\x0017%ÉÙÁ\x0010Û?ÅwÏ!¥\x0004"Þ{\x0000sxï©ë\x0010\x0002µ\x000e­fJÖÛÀ9Ca\x0006èÏýCÊö6±¨P)\x0018\x0016!%5
¿`+8ÿ\x0015ã[¨Å\x0010b\x0017ï\x0012êØ Ë2æ\x0005&3diFQ\x0016\x0010\x0000\x0000\x0000\x0010B@L&SRréÂ%20<:&O%YÖ¤ð¸(\x0018¤5_}íe®¦e`7²I¹PzRà5à\x0008õùþ!ÃgOØ¾~û\x001fÞÄôrýâ\x0015ÞzpÌ_¼¿Ç²\x0014uN\x001d£cûü\x000e½Å\x0014[ì</p><p>BF£I«Õ¤®jf³)Y³¾¾Îúú:N7oâÇ{s\x0010\x0002:Ïs$a}mM·I\x000c°}iLì\x001c"+Åù37É³%53r®ZÉþl\x001fë,\x001bk´Ú-TbÈó\x0006Fh\x0002ÐþrNX,\x0019f|âJ§ïK4ÖîÂÇ\x0002"1\x0004D\x0014H!DTh©ð!\x0012%M3._¾Ì\x001b7è÷û<xð?ú£?â£>b>ó«¿ú«üÞïý\x001eËå\x001fþðÔugÏ\x000eyöÁ{\x000cÎ_çdÊä½¿F*\x000eîÜe¸¹àùßx($1F\x0010H)ÑZ\x0013BÀû\x0014¢¤5</p><p>ÝÅ\x000e. _û»ÔóP,B\x0000\x0010½C' \x0005Î[ÄrOs\vzñ>Ò4hDvV©ë\x001a)%Î;¤\x0008!\x0000\x00001\x0002\x00108kéwúdåtA³Ý¢´\x0015eQ"bä\x0017nìð;¿ö
n¼ð\x001c4Ô¥ÅÎÆøºb±r÷Þ-\x0006\x001b=\x0016ó\x000eÁYé\x001aæ£c\x001e\x001f¯akÇ\x000f¿û\x0003º¿Tsóg»¼õÑ1N\x0008êÚf\x0015Qi\x001aÙCÊÚR\x0015^£ÍhQRU\x0015(X_ßdmm<Ï1Æç9I°\\x0016Ä\x0018\x0001\x00016Æà½§ª+T(mH\x0013I»;g<{Hgå6Ä\x0014!*fá	?:8ÃÅkWhngKYF§ß¥ÕìÐK;H-1"À¹Àh4æâÏx\x0001®~º>"o·É;-&¦"s×W¶Á.Hê\x0019ÃIX;ËÖÅëÌ&cîÞ»Ç£G¨ªÁ`ÀïþîïråÊ\x0015^~ùe~þóóá\x001frîÜ9´Ö\x0008`åÂ<IC½÷>é[8¿Ê{ªÉ»ëÏÑî\x0018^ORB\x0004ç\x001dÞ{\x0000RÄ\x0018qÎ!àøhH):\x0017~xýPÑÓ\x00085D$ÑÔN"ÉPv÷\x0015ÊÕ\x0004o*ÇÛà,2É\x00081"[\x001bäË11\x0002D\x0000\x0000¤\x0000\x0000H)\x0001HMJUVL\x0013ª¢ÂhI\x0008\x0011ë=í,ãï|ã«¼þÒy\\x0015°Ó</p><p>·\âí½gxóç\x001frçpOé2£É	kgöi
>È\x0004÷îþ\x001bë\x0017¹Öé°wç6/}Þrù7·\x0008qNÚï1¾÷\x0011÷ni:ç"òM(«%¹\x0017l\x000cÖèonÑh6HtBb\x0012\x0014H)QJ\x0011b@\x0008	D\x0000\x0010\x0018cÐEQ\x0000P%\x0008A«ÙÅ$5Ñ\x00061îb´c*¦4cÎÁò?}×q<o\x0012\x000cVz\x000czm\x001ay\x0002L¢h\x0006RHbTÒÎ:\x001c/¾ÈÛ¬ó%z¯et®eVÏ8¼{æâK2#ä\x0002+\x0002ÍÌ±\x0015?úËo3W|ýë_çë_ÿ:ív4Í1\x0012cà»ßý3~üã\x001f³¶ºÊíÛ·±Öæ
®>Ñø'·>¢³v?\¾Á'UNj\x001aG§ôïÍøµÖðÎáCÀZ÷\x001e!\x0004Ij(\x0007#¨Î¼Z
¼ Ã¥¦goìØ/30M(Jâh \x001c>\x0008°KBQÌð6b\x0005I³	Q"Ó\x000e+\x001b;Äzó\x001eï=Ö:Bð\x0000(¥Rb´AFÉî]z½.R\x0008æË\x0005I\x0010@GG_+,vb©ë\x0019ËÉ£Oîð>àÎ8Ð_¿ÊBßâÒè
÷\A%óâÖù$)/¾ÖE54ËÑ)ÙÖ&÷ª#\x000e>rñú\x001cñÝ\x0006%)gW»\x000cÖÖ ÑÂd\x0019\x0002\x0008!è\x0004¥\x0014ÖZ¼÷\x0008\x0001Æ\x0018²,\x0008! \x000e0IÂt2\x0005\x0011ILÎÎ\x0002\x0017Î1:ÍÍ\x000e	1s<oádµ\x0016B\x000bò4a4\x001d1_l¬\x000cÐ\x0004bô¸\x00180Ê \x0004H%è·®"8ZÖ´ãý½wx¶÷l\x001b/±¿XÒ-NðÎ29ÜãÍÿôlÞà·ÿÁ?âS/¿\x000c@$â£X\x0016|çÛßæ;ßù.íNª®1\x0012½çüå«ôÛ
nß{Ûwv¹yö+ìwÚtòH\x0015\x000c\x0007ÑòÿÞ;O\x0017ü£¯Ç\x0018Ið\x0001¥\x0014\x0008IÊ÷&ÜßþmhØé\x0014QVÄ~Ì\x0005V\x0004#Ër2ù\x0004%<½ãØ5ðÖ\x0012ª\x0012x/ ÔàA*l"$Èz\x0004B\x0000 µÂ{1âCkM\x0008\x0001\x0015\x0005^~¿Ïh4Ä.="x@²Mp³\x0005ËÙ\x001c7Z0\x0019?coöc>\x0018pkÒ£Ûï`1FA¿ßEå;fO8ÿfòø\x0007¬\Z²ríe¬[â+M½b¬¥¹¾T§´òÈÚZÆd\x0012|
ÂC\x0008¸Ê¢FkM\x0001W9¤H)	Á3Ï±Ö#Â9Î\x001b
úý\x001eJJ"0/q\x0016¤i2<1¼ùÓÀ¾0bÂ'ãÈþáFÓÒé¶©¢ Õé1\x0018¬gMlô\x0010\x0002Fid\x0004­
J	\x0016E09UÏ3|¿bc½Ç¯¾ô\x000b\ÎW\x0018>}Â¿ûþÿôð>×v¶8Ìöwhnce0 ÆH¨\x0016T³!óð£¿~?û³¿ v²,)$MÉ²^~ñé>\x0007\x0007cæ% ,\x000bÆ>Eö6(GCþßÿù\x0003vÌ?øÆK(	ã¢æç\x0007ï?Ôüå^Æ,QÈ</p><p>i+rå¸Ú-è,±Îa\x001aÔÁ ¢À¹£ÇË\x001a\x0015k¨¦`g\x0004ÑÈ$[ýqM\x0014\x0006oÚÔÕ3´V\x0008!1\x0002 @\x0008A\x0008\x0001\x0010ôº}²4ÇYOU{´I°ÃÅ@=>d¼û®Ü~ð'ã7ÙüÜmT½M3]'	ózÉ6èod\x0015×¼\x0001É 26ÅÖ#D\x0008$YBHÜbJgk\x001dÒ\x000f%Ä¨Xï$tû9d]¢6(	Á;jïJ!\x0004D@úså²Àû­kDèÉdÌúú\x001aYÓl6Ï\x001ec]ÄÙ\x0005EÝá½\x000fl^Ê¥³9ãeäèdHõ¤Ä\x0018M§Û¥Óé°¹9fãÌ&kuT\x001a@\x000b\x0010\x0011­\x0015R*¤ª	Þá2OcmÀßzí\x000b,Tà[ò§\x001c½{Ñ(°t\x001b\x0014Õ:¦w\x000eàõ\x0017^ Ûé\x0010l\x0005årrÌÌ%\x0008_påü:\x001f?xµ¢ªRrõÆKtZ\x0019\x000f\x001eq:®H¬8Ì_cº$mC½,ñÓ\x0005¾óGß~Ï^ia³>ÿê}ÉO3</p><p>'Q¾DÈ@)\x0000EéøèDÐUMjÝ¦P\x001eé¦x[ \x0010x\x0010ë\x0005a1!FEH6\x0002\x001a
ÃéhLY+ÒDáAg
êåv»</p><p>kk1\x0000H©hä
I\x0008!P-k¼sX[S¸º\ÒYxðà>·?yÌÿç?cûS\x0013þáß\x00084R2\x0003Á\x0015h$Z4I\x000e¨\x0016N¬]nST\x000b¼\x0007[8ªÙf»GPmL³\x001f®nÓìögÌ\x0016y¥î8×ÜB+ð>B\x0004$\x0018A\x0008\x0010B Æw5Z8\x0004\x0018#úÑ£GÜ¿,Ë¹zõ</p><p>\x0017/^fcKòlÿ³g_Àä
¼ù² ,\x0007H µg¾,\x0018Íæ´\x001b#NGc\x000e¹té\x0012Ï] \x0003²¼\x001a\x001f\x0002Îyfåªò\~é*\x000fÌçüo~\x000b/¿Ì£?\x0007·îÒë\x000fÍf9sk® Â\x0013´w´²V\x0008}í\x0006?\x0005\x001fÜyHÅbN«Õæ^À/ö\x001eïácB9\x001bÑyö&Ìu¼­)mNõô\x0011b<Do\ç`¾äÿõí{\x001cõ_áIj&$¹à«\x0012\x0019\x0003$9"o3\x00130^Ló)b>\x0004çñ(P	ÌO\x00081¤
¤N ØEa9<µÔbÒ\x0006!8Ð4md°\x0008!év»eI\x0008\x001e\x0010h­QJQÛ\x001aÂ;sùbÁ¢.)9¹üoßû9·¦\x000böç\x0005ó¥\x001c)\x00041\x0008p\x001a¢Ñê7[4Ò
\x0002P\x0008\x0007:!,f\x0008"Î{¢·h-°1 ò>åò¬Ù¼°Æñ½\x0005Å\x000c²ª\x0019\x000fO\x0019¬®¤)BKB\x0008H!\x0010B\x0000 ¤\x0004\x0004µóTA!ÇGÐo¼ñ\x0006RJ.]ºDQ\x0014\x001c\x001fe\x001aÓØçøá)^²\x0007¤UÆÉÌå)­FÊt0N\x0019ÍfL\x0017s£!ÃÓ1eÁKWHW5ÖV\x0018\x0010g^¬µV0*\x0012CKIÌ\x0014áJÍ/³±yYÒ=3XéòDMÁAÖt¥§·XàG§,G'Üúù;L'sz½\x000eóÙÍH®=÷<ä½\x0007GÌæ\x001e%\x0005fqt\x0005U\x0011Óg²Ä½JÌÀÏùó£-d0èL£\x0019B\x0008|e\x0011*!\x0012¯Jd9A,Äj÷\x0010£\x0010ó\x0003ât</p><p>*\x0005õÄl\x000b\x000epö\x0018¥\x0002$\x0000à\x001d6(Úí6F\x0003ç\x001cJI¼wàAÑ\x0006ï<.X|\x0008T¶f<0.±x²ì\x00173d*I\x001aöÄÑhg´Cg°Ê`­4\x0019å|\x000fÅ\x001e¸#ðØZa$,çÈ¼$¦]DÞ¡²q6çÇß±,&´á x!
*b5\x001bh¥P"ä\x0019I¦^\x001a9ÁgÐi6Xë·ÑÁo}ëÛìííÑh6\x0019ôWiä\x0019ÝnÎ\x0013ï©ã!±<\x001cÎ¨ÅY\x0000bt:m\x0010¨©bQ\x0015Ìf3³)»{{ü¼ù\x0016«+käÝ6ý~\x001f¥%&O\x0018öOéw\x0007ôZ=:i</p><p>#\x0014Qe¿ø\x0002?|ú3>ÿ¯Ñ)\x000cÿîÑ7ÙR'<¿}\x0005ÂNÓð	§»O»Ô</p><p>ç\x001c³Ùùt\x001cR\x0014s6³ù\x0018DÙ9½ú©k£±¨Í-âlw5éê\x0006Ëæ*A)2èDcà\x00021Fdt\x0008W\x0010\x0016CÜèèk\x0010	H\x0003U\x001d\x0013ê@Ô9²ÙAêX\x0008?\x0003;FHIt\x000eo+N @Ô\x0006ïçÀ\x0018Ãr¹$MS\x0000ï#!8j[âCÀZ\x0001pÔ~IÞ\x0008Û\¿róvFU(Î^lÑ]»ÈÙK/aÇ\x0017p1dMy\x0017[?¢ö5J§ \x001b8;Æ+K=\x0014\x0015äYD(Òæ</p><p>Ëñ>ÝÕ³|ð\x0004ªÂ´2Jé¶ü_¾B¯ ¤Gi¦Â\x0007-Js=f<H¶°Á\x0012ñè[·nqöì\x0019¶·wh6\x001bÄ(9=: kY\x0002^ÃÒjµ\x0019Møð\x000c\x0011Û8\x0017	uI#OIAÏ5óÅº.uÍñ²äèðB¤)k\x001b+9»Í²ª8\x001eÐhæ4\x001bM:\x001e«í>+l³X.ùë\x000fß"{©Ëkò\x001a_ÚøEþjù\x0011«åà@8V!Ë'{\x001cÕM^záyRÜºuýý}nt¯páÒK|ë{oñäñc\1e0¾Å0û\x001cyr¦]p{.\x0008y\x0014\x0015:ÓD\x0012\x0004ï<ÄH¬\x0016à</p><p>âr,'HW\x0012\x0000BÅ\x0018æ#bÔÄ¤0\x0019\x0012I$\x0010«\x0012\x0007$²¦Ùi1\x0017Ôó\x0019ÑÖ¼KÈr\x0012Y`­E)E£Ñ Æ÷\x001eHD\x001ed\x0004­\x0015±r\x000cz]ºÝÏÿÂ</p><p>
õ\x0011ÚÜ1]Ö¶r¾ôµ_£¿Ù¦­ÐhµAÁ|¾ ªn2\x0006I\x0007%"e5"I¡*\x001c³¥7dXçÁt\x0018Ï-í\x0015O$uPGLÒ 5pý\B¯\x001d\x0010Ù\x000e¾û\x001cÖF]ptçÔÕLp\x0007¦¥¢(-KëÐív~¿Rº¶ØÚQõ­)ÖÈ¥£e\x001a¬õ»Y9äý»
Æå:\x0001²</p><p>dä­&BÂ|.(ªZH\x0012#\x0011B\x0012g2ÒÈrÒ$!Is²`ºX0n,pÑsÞ­P.K.¼ò\x001c§nÊ8æßä¥ËÌ}E*\x0013î
\x001fÑ7\x0011W\x0019Ò
ÖÖV1&¡Ùlò³·ßæÝÞG17^ý</p><p>¿üË¿Â'\x001eóá\x0007ï\x0011G\x001fÃúKÄtfq\x0017mS¼nSÆ6Ij¨t4	n¾$V%br\x000cÕXÏqÖ\x0002FD\x000b1Ø(S¢i!"z§F\x0005b÷Ó·±Æ3\x0019V\x0004¡0:A\x000ca\x0012<`\x000cI\x0004"1F¤T(¥HÓ\x0014ï#":¬·Dáiu\x001a\={óç8»¹àÎ»\x001fS/\x0015*öxã+ÏqõÆK\x00049A\x0019N\x0005Ú¤S&ÓS\x0006\x0011¤Ê0*C\x0004u\x0013ÒFÆÂ`¤í6N\x0018l¹¤¡\x0007T\x000er·àÌù\x000e\x001fß,Ò\x0010T¤\x000c\x0015ãéiô{LkÁbV¢lE¬\x0004±¨èifIå\x0000B£ó<g:\x0012B@)såÌ±Ò¯IÚGT®Ä\x00125É§¯Þâ'\x001f/9o\x0010ÆyÖ	f\x0013fdó%³bAUÕ¨\x0018A@a+N#ÒFF§éI9i®Ð\x0004FÇÇLýYÒ øÜ¹ùX<aägTÅ\x000bã\x0015¶fì\x0015'ÔÁñpæ,©v? D¸pá<(­Ù=8%O
¥|Áú\x0005²TòÂK¯r~6e¼`/lóÑ^À\x001bp5d\x0019"ÔP\x0005Bµ$,Æ0\x0010ª\x0002I¨k|\x0018=ÒÍvA°</p><p>²\x000eDèâ\x00141yH\x001c~\x0008ó}D\x000c8!QIN\x001b$­\x000e:m!\x0010":ÉÈt$FðÞ£\x0002\x0004Æ\x00186ÖzH\x0013ÅÚöYÖ6WÉ\x0012Ã­{\x000føøö!/^ºÊ°|Ê\x001b_»Ìóú%Ú-EE</p><p>\x0011\x0005®</p><p>H¡YL\x000b$\x0006@\x0012CE\x0014¨«%­ YF`«J.HÅìÏ~î"ïÿì²,ÉD+jô$âÆ»¤Ë]ülÂtY`\x0017KBUá¬£ÕÒ£\x0011HôÉÉ	'''Ä\x0018Y]]¥Û\x001dP×F\x00169sñÇ'¬³ÖÚbÕÐ0{4ó§|ïýÈÉd\x0013¼ 8Ö	*1´º\x001dÒ<¥\V,\x00163¼õ\x0018X,LÆS1T®FjÁéÑ	kj@iJòFr¸äè\x0004v\x0015âÈqX\x001c3jÌ\x0008\x0011f³\x0005³ù££cB\x0008L§S\x001e?~LÏ~áWè\x000fzl®ui´\x0012æà~#ç¥8go6g6õ¤k	µs\x0008W­p5\x0008[\x0011gSBmÑÂ\x0011'X\x000f¾F\x0004\x000fÞãd\x0003ò\x001c©
rv\x000c£;á\x001düä!¡!´\x0002¥\x0010*\x0001­\x0002bØb\x0001B¤M\\x0000tF«©(«</p><p>c\x000cZk\x0000²¬ÁÖÖ:\x001fß¾ÅÖÖ\x000e³ÅùCv÷1L¹t~ßû½ÈÚºb}sI\x0005µ+02 ¤"Dw\x0005y#£*,Á×(-Hô&U}DTÓ,\x0014T¾ÂGA³,%E9¥,;ì>!âE^ze§<æøôL+4'J)\x0017K°¬ñEM]Yb\x000cäF0h</p><p>9\x0008\x0004º×ëÑh4\x0010BpþÜ9Ö7¶ú&2$\»>á{?lð`²ËµÎ&\x0017M\x0006[].®ÐÌò'?*\x0018ÏÏ\x0010Áú\x0012çj(­i·[dº¬)\x0005QDæÓ\x0019&1h­)\x0005I²ÝZ%I\x0014³é;Ë\x0007LÚ3ög»<\x001ej¼\x000f<¨\x0010k(\x0005·\x001fÒ\x0014ù|\x0010\x0002k-Óé<Ëùú¯|í-rÁl|L9;¦i*öiOOè°Â´ÕfY;R$Þâ\x0015¢\x0004g\x0011u\x0008\x001e\x0017,T%ÂÕ\x0010$ÑdD BÈ§ïÂÁÏñ³=\x0008(sDÚD%
dj \x0002@ô\x000eoKbÐ @*
BPE1	\x0008µ\x0016)\x0014R</p><p>¶v¶\x0018ôr\x0016ó\x0019·ïÜ¥Ùl2\x0019±Ö±³½ÍÖæ\x0016Jôév\x000cy(#ZEÊ©kðÁá@\x001bCµÌxv_Ñh­1]æ³\x000f/p´óä¾Ä&Uh\x0011Ê³ì\x001f\x000cjR³Æû»¬nµi73é\x0005\x001e=ÌON(*[B¹¨)kG]ÖÔ¥Å9K$\x0002\x0002I¤ß2\x000cÇ\x0015\x0015 Ë%!\x0004¤Ü»û\x000f\x001eqñÚ\x0012ï\x0015\x001b+5ªÃX\x00111  5yårãÑ\x001eo}P0\^"ú\x0006Þ:"°,</p><p>\x0004\x0002c46n\x000bg-²d:ç
LP\x000bd2aÛÔ2ò¤ù\x000c§KæcÏð$Å·\x0004ÃÁ´ÈÜÞåÞ_¾Ëõ\x000bW¨ªº®Rbm1ÑÁ#D}Ìt>¦X.\x0010BÑêöÙ\x0012FÛ³¿ÿ\x001fd>"P\x0004_à¦3Ä\x0010~ö%Þ:b\x0014\x0004B"A-\x000e`ï-âÑ{øÅ) !\x0001©!TÄª&`Ê "z\x0002¡\x0015BH¼³8[ \x0006£IAn§àqÎáCàÆó/±µÞ£Z\x0014(©h6\x001bdYJ³Ù¤Ñl°¶2àÑÝÀäÀP»@\x000e­\x0014F%ÔÕ\x0012\x0017\x0005QJØb÷~8gem\x001d©\x0015ËYG\x000fÖLRvÎR¹\x001e¢Ü \x0008Ø}t³;MÊ¥Ä\x00165ÎÖ¨<ãÂ¥Ë8»IÀQ\x00155¥uTE-jl]\x0011|\x0008\x0011ðD\x0016ô:)£IÞßßÇ{O$xï	\x001e\x001a\x0003Iå!K4««Óa ¹R¢µ¦é;(!ÙéwxùjAUróþ]\x000efW±Aå\x001dÎ[¼
Äe@(A"
(Ií<~>Ç{©\x0013.øu\x0013ÖC&
Ë¾9SX9l3/g<öÇ¤Ý n\x001esvm\x000f\x001f\x0011B`>SU\x0015u]³±6`9?BÈ&³ÅÙ¢F&Ýþ\x001a[\x0017®ðÊÆ&¯.J·-ßºµ@,§bóè\x0002:xï>\x0010eN4
ð\x0015jþ\x0014yø>ñàçøj4\x001a¡D\x0014"D"\x0001D\x0002Þ\x0012ª\x00196XT£ò\x0014i\x001a(c\x0008Þ!\x0010( \x0006\x0016Udì¦\x0010\x0003!\x0004Ö7¶ùÌ+Ïø!Á´M	­VN§ÃÖæ&óÅn»w)ÕBR;­\x0001!PÑøà\x0011@5HAð $\x0006\x000f1 e³5ÎWX"ËjI\x0016\x0014ínb\x0011X.kêª¤®gØ</p><p>¼ö\x0000Fk¢µÔXêÒâJ­\x001dÁy\x0002@\x0002Ä\x0008Hzí\x0004[:ôÊÊ</p><p>1F\x0000Ò4E¢è÷\x0002.î#$q[<=l^rd'l<¤4´åÂzÓs\x0015	âã\x000f8(®\x0012Ô</p><p>"Föø ðÖR9O\x0014\x0001\x0013\x0002Q&ÌãVá¹ÞÙ NR\x000eâ!Ãù	[eAÙ`¿ØãIkÂ¹]ùð'o}ÌéhR\x0010\x0002ív^¯µ4Õ\x001c\x0016¬ê\x000eysþZ<o"¥\x0000 ,*Öú\x0003þ/+8\x001aüõ­\x0005Òz¯\x0008®Æ D%±FO>'oáï\x0010\J\x0012bÞ\x0001)\x0011\x0011p\x000e\x0002kAi\x0010\x0011#ø`\x0005!8TâI@%\x0006ïKìlAwÐ\x0006A" ¥ä\x000b_ýeÎ÷rÇ\x0005oß~Âêú6JiÄg9Å²DDp¶D«\x0006\x0001\x0011\x0010\x0008l,Q\x0008p\x001014H%Y.ÇäÍ\x000eÞÕ\x0008\x0019°õ\x0018-±t¸Z\x00115äMEÞ)Ñ\x0007½úÞÖ\x0001\x0007gñ~\x0010"A\x0006lpÔµÃº¬p¾&\x0002H\x0002O$F\x0008D\x0005Vz\x0006\x001dB@)E\x0011ç,ZIð`EM¤¯²8ì1<eg5gê'hÝÁ(Ãz7çâN@@2ãæÝ[<]'È5´ÈèJâ¼%X\x0016F\x0005Å\x000bÍsôt²,y6{Âä\x0000rÍú²­\x000bº\x0003ò½\x001aýÐ\x0012«Èáñ\x0011ûûûH)È²\x000c!$+++\x0000\x0008¡9ñ%Ö760Æ$\x0006!$ÖÖxïñÞ³XÌéeÿáË=\x001aõ	§§é¬f^z|¢Ý1ËÓ]&\x000fßÃ>\x0000_\x00009*kc\x0000\x0004Ñ\x0007D\x0008óÿ'\x0008¿.M\x000fÃÎïÿ7|¾s¾üuîéî=\x0000\x0006\x0018`@\x0008D HT¢L®´^y©µ]å²¥RË¾/öÂ®½ñ^èÆ[e®TÔJ+KZR²	QD 0\x0018`\x0006;§/§ÏàßÏ»</p><p>Tw\x00164 "Àâª\x0012l\x0017\x001eÇZKÄ 
År	ÞS·=à¸uç\x000ew^¾N5zÂ½ý	ï}öõÍ-  \x0008\x0002µ\x0014ó9B</p><p>â$àÊ\x0010%`¹ôdKKmj¬µ\x0004Ä\x0012OT0U\x001709\x001b±¾¥i¬ô\x000eÚOi5wé­D¬ìÌ¸pù3Ö/\x000cÐ]ÒÉ9µ(\x0008ÚÝg	¦ÚFH\x0005ÞQ%\x0011\x0015uSU5Î8<\x001eÀa\x0011³`­EjA\x0014\x000bÄoüÆoø­­-nß¾DðÎ»¿ (O¸ùù\x0019íFÉÉ\x001dö\x000fGÄë\x001f°Òµô\x0016¹/ÁzjoÉjËdå5E*.#¦õ\x0006:Hh5t»]\x0002\x001d`½Ãã9ÜÛ#-yûòç¹¼u\x0011¼Ç­*²ØM´Ç?zy9çó·^'\x000cb²"g: µÆ9G\x001cÇ<~üÓÓSÂ0äâÅüÎoÿ\x000ef$I\x0008Ã\x0010!\x0004eY¦)UU\x0011!F\x0013­$EYRT¬¬H³%£³\x0013ê"çì|Æd4C© Ô\x0008­â\x0004!%\x0002I\x0014F\x0018c(Ê4]âjÔí\x000b;Ú2]LIÂw?#I\x00126.\b¶X²¶¶A£ÝA	÷\x0016M\x000e&ãÕ7ÞäÂúÃý'|òéCÒrç×QJa­ÅZR</p><p>¥\x0015ÍæË_¾L£á°Va¥¶\x0015ÎY¤ô8,B8¤\x0014H	ZGÌÎ4Z12Ì(Ë\x0011³3Î\x000fJ¢(¢3tt\x0006«DÍ.ããSNÏ¨e×\x0019ÏôÀoã\x0001!\x000cW[9¯°Á\x0001Îy¬³xgñ\x001eð ´¦Ùl\x0013F\x0001Þ{ôÑñ\x0011\x001b\x001b\x001b¼üòË(¥øþ\x000fÀû¿zÀ/~\x000eA8¡Õ:Á\x0018C\x00154\x001bMªê^¯GQ\x0014DQL¿ß'M\x0004f{{\x0017C\x0010$	kk«loï`MM]\x001bÒ,å{\x000fÆ<Ú;Æ\x000c¦ô:×1¦f%êÄMÄ í¥üä/¿GYV\½v\x001d)%\x001eO#i°ºº</p><p>\x0008@óýïüä§´ZM^}õ\x0015ÎGçèY@\x0018\x0006Xk)Ë4M\x0001ã(h4\x001a(­qÖ\x0002\x001e¥4(¢³s\x0011)\x0015¯½\x001a"µÄ\x0019</p><p>!\x0005A i·Ú(­	Ã(É²ÑhÌt:E\x0000ßøÖ·ØßÝe2pã\x001büÉü)»»Ïyë­/\x0012E\x0011ÞynÞ¼I\x0018\x0008!9;?ãôôN»M´AW^»C»ÝæKo½E\x001cE8ç\x0000\x000f\x0000÷à½§ª\x0004BTH\x0002\x0000\x0000\x0002)\x0015R</p><p>@°¾!ÐZ£¤Ä·`}ÅsãD\x0000 \x0010\x0002\x0010°Òk×!Ë\x000b¦£	×.[\x0010\x001eç\x001cÎy<\x0000\x0000\x0000\x001eï=Îy¼w8ç±ÖÒH\x0012¶¶¶Â\x0010\x0004h)\x0015RI\x0000¤\x00144M:í6Z+¤H¥\x0010B$;o¼Î|>gss[·n±¶¶F¯×ãää\x0018­\x0003ÞÿWxïhµÛtÚm6·6¹pñ\x0002Æ\x0018\x0016\x0005æÄaðæúåMn]_%$nP\x0004'F#z½>YQ×5\x0017.ì\x0010\x0004\x0011»»ÏR²³³ªª°Öç\x0005««k\x0004AH¦,\x0016\x000b¢ ®+¢(&I\x0012´Ö(¥¨ª\x0000\x0008t÷\x000eï\x001cB)FV»M\x001c\x0006º$ËrÒ,£ÈK\x0010e\x0005++}êº"Ësâ(fee\x0005¥\x0015Ö\x0018äEA\x0010|ðÁôz=>ùäSþôOÿ\x0003W®\áÕW_¡ªk¤RHéRb¡¬*Ö7Zt»\x001dò<G\x0000uU¡¥\x0004À\x000b@\x0000\x001e¼\x0000!\x0010\x0012¤\x0010\x0000x\x0000< @\x0000ð\x0000\x0008\x0001\x0000àñx<\x0000\x001e¼Ã\x0001R\x0008@ < \x0004B5\x0015³É\x0019Yb½Ã{O³Ù&\x0012"'"´Ö\x0000xç\x0011\x0002\x00148ëñÞ\x0001\x000e\x0004\x0000h)@</p><p>÷\x001e!$½^+W®pçõ×X][Ç\x0018ÃG\x001f}Ä'|ÂÕ«W\x0008£\x0010)\x0004o¾ù&Q\x001c¥\x0019ççç¤iÊ2] ¤BJ	ÞszzF\x00104
ÄQÈ\x001b¯Üà¿þÛ_g{5¦Õ)ÐI\x0003¥\x0005ÖÖ\x0018</p><p>Ò¥!\x000cCªª"M\x0017\x0000h6\x000cC¢ ×ë\x0011\x0004\x0001Þ;â8"\x00084e³XÌ)\x0002!\x0004Q\x0014\x0011Ç1Zk\x0010Xc\x0011JB]#0\x0018nl³ºs­Õ!n\x001b¥\x0015ueXf\x0005£Óc>~Àb1Ç9Ët:¥Ñh\x0010E\x0011ËzI\x001cÇô{=Z­6:Ð8ï¨ªwß}7ß|(</p><p>yþü\x0019/Þ¼ÉÖÖ6EQ ¥¤Õj\x0011Ç1Þ{1t:\x001d¤Aç \x0004x\x000f\x001e\x0010 \x0010\x0007\x0004\x001e\x0014\x0002!\x0004B\x0008\x0000À\x0003\x0002\x0000\x0000!\x0005B\x0010\x0002\x0000\x0000\x0000\x00018\x0000¨ª</p><p>ç\x001cYq~~N·Ó¢ÛíñäñCþôßþKv?û\x0010o\x001dA\x0012\x0013Æ\x0011Í\¾vª*HZ}zý>ZÂÊê*½þ*\x0000\x0000BH@\x0000\x0000 µ\x000e°¦Æ{\x000f@\x0018\x0006ÔuÍgwï³r|B\x0017L§\x0013$áôì@\x0007ÄqÌþþ>Ueèõ:\x000cCsüà\x0007?`mm8R¦)yÓjµ\x0008¥äÆÅuÞ|ñ7¨³SªrFUÔ\x000e´R\x000087e½¥yñÊüüãS´\x000eètº4-\x0006\x0001Q\x0014QU\x0015F\x0003k-RJF£1Zk²,#\x0013Z­&EQà½ÇZ\x000b\x0010\x0012é\x001cB)\x00040Øy­[o°Ò</p><p>¹Ø×¦ÝSËY&Y	ssÁµm=ÒÃ{,)³ù$Nh4\x001aTes\x0001Ýn\x0017ï<Æ\x0018ò<g8Y]]%MSª²äW¿ú\x0015UUñõ¯\x001d \x0008\x0000¨ª</p><p>­\x0015q\x001c"@JI^\x0014Q\x0014\x0012\x0001À{\x0010B\x0000\x0002!\x0004B\x0000\x001e\x0010\x0002\x0000ð\x0000!\x0000\x0010\x0000\x001e!$B\x0008ð\x0000²ªÈóÙtÊ½»qrtÄñî]tüè?áñÃ\x0007\x000cº-\x0004J"äþ\x0003>|çG\x0018S£\x0004!57oßæK_ÿuz½!\x0008\x0012)\x0005B\x0008\x0000\x0000´1\x0006c-\x001e\x0010\x0002!\x0004UUñôé\x0013>úhf³I»ÝaoápH»Ý&" $c¼sTU$I¢\x0008­5F\x0003­5UUÑ</p><p><ë\x0006NZ2#´ÆZA¾H	\x0002A\x0010jêª\x0002oøöWoQåd8à\x000b_x\x0013¥4Ï?#Ï\x000b\x0000F£\x0011eY\x00020\x000c\x0011B uÀÊÊ</p><p>óù¢(hµZäyµ\x0015J)\x0012h\x001d\x0010E\x0011­Á6ÁÎ«<YjúMÇ47üh×ðÙÈp÷¼"¯\x001dq 9É<ø\x0002¿¹¢èÚIóår1n·Â\x0013!yóós¦Ó\x0019?øÁ\x000f(Ë(ÙÝÝÅZÇç>÷\x0006ÖZð\x0010\x0011J)Ê²ÂÔ\x0006­\x0003RdYÆ\x001fýÑ\x001f±½½Í/¼ÈÅ\x0017éõºH¥\x0000\x0012\x0010\x0000 @\x0000\x0000\x0000 \x0010\x0000\x0000\x0000\x0008@\x0000\x0000\x0000P\x0014%'ü»ý/ø«ïý9³Å.û»{Ìæ\x0019RÀx"¥$Ôv+!-+\x0004^³2P\x0019Ç|:áäøíKKÍ&\x0000\x0002\x0001\x0000\x0000®ë</p><p>k
\x0002\x0001@]ÕXk\x0011B\x0012E\x0011B\x0008Ò4EkÍ`°B«ÕâÚµëÜ¼y4MÙÛÛ£,K¦Ó)Ià½Ç9Rf³I£Ù`½\x0017³½\x0012c«%ebG¸8lb`69E</p><p></p><p>)\x001dqØä_»M®wÍfL'\x0013\x0010\x0012cjvwO\x0001H\x0006Ýnë×¯S×5J)´Öt:\x001df³\x0019eY1\x0018¬PU\x0015Þ{¢0D\x0008EY\x001bt÷\x001a\x001fN5\x0006Ã[!GKÇ½³gKe\x0014¼Ñl6\x001c\x001f>2Ûéò[ÍU6Ô\x0001h1ããcVWW\x0011Àx<F\x0008(Ë\x0002ð8gét:Ü¾}\x001dªªbuu\x0015ï=åªª°Öb­%/</p><p>XkÏçüùÿ9ÞÃíÛ·øÚ¯ý\x001a_xóM67·PJà\x0001\x0001\x0000\x0008!ðÞ\x0003à\x0011\x0008\x0000@ ð\x0008\x0004\x0000\x001e\x0000\x000fÎÏùÿËÿ?ýÿ»}FWô×VYì\x001dpv>G\x0000B)dåÐÒÐM(<8Ç,-)kÇ`Ec¼`<òËý¨5àÎ7R"¤D\x0008\x0001\x0000N\x001aMÖ(%1ÆprzBçC)R\x001aç\x001cRJ:\x000eA\x0010 $Çc\x0000\x0000xïã\x0018ï=ÖZ±ÊÑ\x0017\x000b"ë(sKm3«)³\x001cgs­H\x001aMl»ËÉá\x0001±()¡¡è·;\x0014ó\x0011ßÿÑ'Ìf\x000b©	F£A\x0014E8çX[[c<\x001e³\.ét:\x000c\x0003Â0¢Ûí2Î8==cgg\x001bk-UU/6^d\x0014®\x0003\x0004Oe,ÏÆÇSÇ¯\x001dÍD\x0013ZÅÙ´$ÎçøÅOöº¬t\x001c¿9ÐøbI][¬­Ïç8gY.,)''§(¥xûí¯òÊ+¯pëÖ-¤\x0008!ðÞóÑG\x001fñìÙ3R¼ñÆ\x001b4\x001a
ò<Ç{\x0007@\x0018QDºX²»»ËÏÞy\x0007çk_ý\x001aÕ\x0001ÂK\x0010 \x0000\x0004B\x0000\x0000Þ\x0003 \x0000@\x0000\x0000\x0008pÞ³÷ô\x0011ÿö_ü¿ù\x0017ÿü8:â\x0004x\x0004,%Ë</p><p>8TH!°Æ" Í+\x000eéÅ\x0011×ºXëñRP\x001a¨­Å Ùß}Æ­[·i6\x0008\x0001\x0000\x0000\x0000z{k0\x0008\x0011B¢bssÃÃCË% ¨ëº®Íf¼óÎ;aHe\x0005S\x001b¬5ìíí3NñÞ³¿¿O¥\x0004:Ä9xóæ&­+=â+/ptZ²ûä.</p><p>\x000e4\x001e¢®	^¿C³Û&\x000eÔuõ^ÛãÊ\x0019Ïï"@kµ\x0016)\x0015FB\x0010\x0004ìïï\x0013\x0004\x00017nÜÀZK¿ß§ÑhÐï÷Èó<ÏÑZSW\x0015¶9ähõ-Þ;´ô¢ôä\x000f\x000fzüÁ
vbØmÇ-+d^Ðªf`slz\x0000M(Ë\x001a_8ç©ª</p><p>ï¡ÈKÒ4£(</p><p>ÒüÎïü\x000e_}û«è@#¥àôô÷ßétÊ£GX,\x0016¬­®ñòË/\x00030NIÓ££#1ô{=\x0001kkkXcùå/~I¯Ûã­·Þ¢Ùl\x0002\x0002\x0000ðxï\x0001ð\x0000<\x0002!@\x0000\x0000R(Þ{÷çüwÿ·ÿ+\x001eÜÃ$ÖÌó\x001a%\x0005eVPV5qH%iG \x0010¬´cúíN«\x001bM®l
ét\x001aà%£EÅ£IAêk$Â;\x0007\x0010\x0002\x0000\x0000\x0000m­C\x0008\x0012ç\x001cR</p><p>Â0¢Ó(¥HÓ\x000c¥\x0014Ýn0\x000c\x0000ÁÏßyÅbIUx\x000fÞ;¤\x00148çñÞ\x0003\x0002 K»Äzñî\x001e(Øéw1õÚ\x0019æyÆd:g<É\x0017%íNN§</p><p>\x0013¶V{t××è®msãò&ù³\x0000</p><p>!\x0004Q\x0014aÁZCf\x0008\x0001\x0000um8==¥ÛíÒëõéõúÔuÍd2fjc~2érþá¿Ù\x0001T\x0001ó\x0017¾ÈÃî\x00056¥ä{Mó/?-ù«iJ#	<£"#\x001eq?hñ­¾ -J0¤ÕjÑh$,Ó%¦®PJò7ÿÆßàÂ\x001däyµÏ>ûï~÷»,)ý~(Ígüûÿï	Ã·ßþ*''ÇPU\x0015B\x0008.]ºÄ7¿ùMRÜ»wñx5\x0006\x0000ïAàñ\x0008\x0000<÷\x0000 <x\x0017\x0002ï=Â{~ùóòÁ\x001f±Lk¼\x0017\x0004JàñàaQÖX<Æ{ó\x0008$@0lk®oµXí$\\ë°½Þ§Û]!#d xCh\x001e9[\x001b\x0004A\x0000Þ#@\x0008\x0001\x0000ÞÛÛ¥×ë! ®k>üðC¦Ó\x0019a\x0018  Ibâ8Â9Ë|\x0013Ç	ãñÑhµ\x0016¥\x0014\x0000B\x0008R\x0018c±Ö\x0010\x0018q+W®!ª+\x0014gÏ\x0018\x001dÝc.XV2/ÈòeáÙ?;f±,é*Ï[ÖQvh¿ÕæÎ\x001b7yåòñý'\x0018\x0007FÖ\x001a­%ÎIÀ\x00178çPJâ½g:\x0012!N\x001bk-Q\x0018²8Ë1¿úç¼\x0016OÉÒ{Ï°"àÉüßÿÍ\x0016×®^ãµ7>Ï¹NJD}Æ³l	&c»!èJPZÓn·ñ@\x0018´Z-¬µ\x0018k\x0019\x000eW¹|å2Zk¬1A@f\x000cyã½§®k\x0010H)©ë'O°XÌ©Ê\x0012\x001d\x0004¼ðÂ\x000bºfooõõuÃ!q\x001c³½½MUUH%ñÞ#Ç#\x0000\x0007\x0004à\x0000\x000fxÀ{¬säyÁógOyþô!a\x0018`Ó¼¶¸Ò³ºÖg>[ \x00104µBÆDC¿©¹ÔKØ\x001e6Ym¬vcz­&íFLÒLh´HÐU1Ãí5üÆËä^á\x0001\x0000\x0000\x0000\x0000=Í±Ö ¥Ä9Çh4b>\x0013Ç1a\x0018Q×v»Åææ\x0016,\x000bÞ{ï}±e1V«EÒHÂªª°Vág±ÌpÂrã¥\x0010"a¼8¡?Ø ,\x001dÚÎG\x0016QDÖ\x0011$	/®¶ÈSËìàôW\x001fqñó_â\x000fÿË¿Î¿ú\x001frÿÑ\x0001Zk< usªªh6h­	²,±Öç9Î9RÄqÂFÇ\x0011\x0008Ç¥KY±9»ÐçÝ§#Ò<åúêUå¸ÿg?cÆ\x000cVï`6^¥-º¡â¾ÆÙ@ÅèF¢¬Èó\x001c)%Þ{êº¦Ñh µÆ;\x0010\x0012­5RJâ8&I\x0012Ë%um(Ë\x0019Å²,iµÚ<|ôV«ÍW¿ú6F_}ð\x0001Q\x0014áÃ9G³Ùdmm
­\x0014Þ{¼÷ \x0004\x0002\x0010\x0000\x0000\x0010\x0000ÚXiÊ§\x001f}Ä\x001fÿ¿þ{î}ö1óE1\x000eCÇ1/Ý¼Â;ï~©j@Ò%ZÀ \x0019±Ò</p><p>é6\x0003Z¦\x0013GDZ«ÀUxßBë\x0004\x0011&Í\x0004\x0011\x0007´ZC¦Ó9B\x0008\x0010\x0000\x0000èßüÍïpéÒ%úý>Î9^{í5\x0006\x0001F\x0003!\x0004ãñãã\x0013¼÷4
\x000eãn·C\x0007\x0018ch·Ú \x0004Î9666©ëédÆîÁÝÓ1/æè@ôV\x0011QD7+(Ë%JÁ¥\x001dGm,gÓñ2g­09RÔ5v<ç£÷ÁÛ·ùÖ_fký2\x001e=¥òN¯ËÁÁ\x0001Y\x0011!ÆZò<G\x0008R</p><p>ï=u]ã½#Ísz­Ï¿ö\x0012~~Àí­\x0006ý¤Ï_`of¸ýÂutñ#þê\x001fòûÿ³\x0007ÿµ«_"~ñ«4£&M1'ð\x0015e]£$B¼÷äyN¦(¥\x0010B CM]×¸Ú\x0011hM\x0012'äyÎt:åìì²,) \x0008ØÙÙÁ9GQä\x0014EI¯×GJI]\x001bÒ4EJ5 ÐH)ñ\x001e¼÷\x0008ïñ\x0002ðà\x0001¼\x0003\x0004Î9NOOùô£_ñöï8|v,/É*KQ\x001b¬\x001bWV)ò²*\x0011ÞSÖª¬ô\x0012Ö:\x0011+vÌF¯EC+5TUE\Ø¦¡²%¡hàG\x0019ÉJLÔ\x0007\x0000\x0000@ÿÁ\x001fü\x0001A\x0010  ÓéðOþÉ?auu4Mét:ìííQ×5\x001fü1O<A\x0008RÁ`Àd2!bÍ\x0006Æ\x0018vww©ª~¿OÒj`eÀÏî\x001fqíÒ9\x00177¶ðÎ2Ì8?:d÷à¨\x0019³¹µJ Vç4\x0002uÁ°C,CN«z:áèÙ\x0013úÃì\\x00190Z.QRÑl5)Ë\x0012­5Zk\x0004\x0000  \x000c#\x001a\x0006\x0000Þ{ª²B\x0000D#\x000bè6"t\x001crûÊÜêíà³GwiE\x0001WV{'Käù³»F~r\x000fõõ¿Éç_ÝÁù\x001a¥\x0014Zk¤RDQµº®	Ã\x0010¥\x0014A\x0010`ê\x001a¥4Þ{â$Æ{O¦Ìçss\x0008!(§O\x0012E\x0011ÍfããcÂ0$Ër²,Å\x0018µ\x0016ë,Î9¤\x0008áñ\x001e¼\x0007\x00018g1µ¡ªk¼÷x\x0007O\x001e<àçÿé_±ÿè>gSÎg\x0005EåJ#\x0005\¿¸Î\x001f=@\x0000R</p><p>¼\x0017\x0004\x0012zvB¯\x0019\x0012E</p><p>á=Ö¯
eUc¬Ãz\x0001Ö¡¬C{ðÞc0\x000cqÎ!\x0000\x0000@çyNYeÖ8±Öâ½#Ï\x000bË%J):í\x000e/_áW^áìì4ÍùäIÓ\x0014ï=Þ{¶·wè÷û§®k¼÷Ü{rÌ½§lF»\x001f½Çû¿|Æà\x0002\x000föÇ|íËo²¾¾ÁÑóTy·PDs¶È)"òb1!LÆc¤T\x0004a@\x0018´Z-¦Ó\x0019J)¤TÄqÖ</p><p>!$Z)ðà\x0011xïX,\x0016,)¯l¯\x0011µ\x0003Ú\x0006uUÒô\x0015e6áþÃû<=9GXGn\x000cA \x0019´%Ëô»ßÿ\x000cü×X}ë
â8Æ{\x000fs\x000ec\x000cA\x0010\x0010Ç\x0011A\x0010"\x0004¤YFç(­¹sç
þÛÿö\x001aÿôþS~ñ_ `eeårIeÔuÍb±à{ßû\x001e·o¿áp\x0015­5B\x0008s8çñÞã\x0007\x0000\x000fRI¬±äyÁb¹¤®+Òù{\x001fþ\x0015gÇ\x001c\x001cO8ääµ\x0001À;Ëêp$8,p\x0014\x0012%\x0005Bx\x0002éh\x00058\x000c\x0008À8C¢b8ÀIuà=x\x0004Ö;¤\x0010H\x001c¦Êq\x001b¡\x0014à\x0001\x0000ÐB\x0008¢("\x000cC1TU³v»M¯×çÑ£G\x0008!â\x0008;6t:]Ã!Y±º:äûßÿ>Ï?ÇZR</p><p>cjÆã1Yá½gÿ¥\x0014w®0\I\x0018noqñÚçùÂW¾ÎÆjr~6¢(k¤ÐÄZs2^p-Ùè
Q\x0014</p><p>k
\x0007\x0007\x001c\x001dY_\x001f\x0012E!yqp°÷\x000b;\x0017	Ã\x0008!\x0000\x0000!@D \x0004uE(\x001d/_Û!\x0016%Ò\x000bÒÙº~\x000eÞ\x0012\x0008Ëlºà,3,jñN;a%i«\x001eÝÛE:Áßz(PJQ×5y^ µ&\x0012ò<#Ïs´\x000eØÜê\x0013Ç1J)¢`}}0\x000cY__ç\x001bßøu&	\x001f}ô1UUqzzÆ'|Â|>çÎ;¬¯¯\x0011!Æ\x0018&	eYÒëõPRRÕ5F8¨kó0\x000cyöè#v?þ!\x001füô\x0017<z¼ËÑéÚz¤T\x0008i±\x000eV×ûDquP+b-éÆnÄz§A3ÒH\x0005Î\x000b\x0016µcïx­!aCÓ@¡u\x0001^x\x0014 \x0010R \x0000\x0010\x0000\x0000èf³µ\x0016k-RJÂ0$i6\x0008´&\x000cCÊ²`2ÉL&\x0014E÷\x001ek- ¢ýý}NNNèv»\x0008!\x0018F\x0014EÖ\x001ac\x000cé2åûï¾Ç²,ø¿üÃ?àÍæÚ\x000e½/0yô1GÏNçx­\x0008\x0002\x0000\x001a¡¢ë\x0014uiPÊ¡Û\x0001½NÄ`Ða4Y`¬et>f2¡¦\x0004üõoÝ&/\x001d\x001fvDU{¤\x0008!\x0001±\x000e[Õ¼y}^SbJÍÝc:qÌ2M)²\x001c¬¡\x0017Â³iîXmÇx­YYéò­¿þ·p"b>_Wlmm±¾¾N\x001cÇ¼ÿþûXk©ê</p><p>ç\x001cÃá \x0008\x0010B\x0000\x0000 `ee^¯Ç;wøÖ·¾Me$I<Ïyøð!ï¿ÿ\x001eãñÕÕU¢(Bk²,±ÖRU\x0015E³··ÏÚÚ\x001aý~\x001fï=¦®XÌFì?|Ý§¹{ÿ1ãyÉ¼´\x0018ç	Ú[jëY\x001föÎSsh©\x0000\x000f\x001ezb«\x001b\x0011'</p><p>/\x0004EÅÇ»\x000bÆYM\x001cGüüÁ\x0019Qã9_~ý\x0016o¿ù\x0006½$BÊ\x0000!\x0014RJ´\x000epÎ\x0001\x0000\x0000 Rh­\x0001Öv§M·Û\x0001/pÎ²¾¾5ápÈl6\x0003<ÖZªªÂ{Ï7¿ù
R<{ö^¯ËÙÙ9\x0017.\de¥ÏÝÏîòá\x001fb§±ºÎ`}
5;áÑ»?am6#¨\x0017ÔU</p><p>\x0003\x0008!±Þ\x0003¤\x0015¢\x001a
¤ÒÄí.\x0017.pãhÎù¨EÿÂ-p5Gxï¨ª×n\x0005l\x000e\x001bÜ¾Ñá{?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/filiere/recyclage](https://lemarche.inclusion.beta.gouv.fr/fr/filiere/recyclage)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae/export/csv?page=1">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/annonce/resultat-recherche" class="form-category alt col-xs-12">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/contact/creer">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/conditionnement-de-produit-121599016/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/conditionnement-de-produit-121599016/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/121599016/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-et-transformation-en-nouveaux-produits-1261414131/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-et-transformation-en-nouveaux-produits-1261414131/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1261414131/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agent-dentretien-des-locaux-1622061097/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agent-dentretien-des-locaux-1622061097/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1622061097/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1138015681/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1138015681/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1138015681/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/identification-verification"
                          method="POST">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/inscription" method="POST" autocomplete="off">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agence-dinterim-dinsertion-generaliste-1142590615/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agence-dinterim-dinsertion-generaliste-1142590615/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1142590615/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/besoin-ponctuel-de-main-doeuvre-811161776/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/besoin-ponctuel-de-main-doeuvre-811161776/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/811161776/flash" id="quote-form" class="date-selection">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 2: "lat" "lng" "country" "area" "department" "city" "region" "postalCode" "zip" "addressType" "serialSectors" ].</p>
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxlarge/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxlarge/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxmedium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxmedium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1261414131/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1261414131/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=121%7C138%7C86%7C87%7C88%7C89&structureType=0&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=121%7C138%7C86%7C87%7C88%7C89&structureType=0&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors&structureType=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors&structureType=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/121599016/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/121599016/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1138015681/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1138015681/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1622061097/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1622061097/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1142590615/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1142590615/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors=9&structureType=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors=9&structureType=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/811161776/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/811161776/new?budget&communication&prestaStartDate)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1138015681/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1138015681/voir)
  
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/besoin-ponctuel-de-main-doeuvre-811161776/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/besoin-ponctuel-de-main-doeuvre-811161776/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agent-dentretien-des-locaux-1622061097/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agent-dentretien-des-locaux-1622061097/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1535866043/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1535866043/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-et-transformation-en-nouveaux-produits-1261414131/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-et-transformation-en-nouveaux-produits-1261414131/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/conciergerie-dentreprise-de-quartier-483504808/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/conciergerie-dentreprise-de-quartier-483504808/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/conditionnement-de-produit-121599016/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/conditionnement-de-produit-121599016/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="//maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agence-dinterim-dinsertion-generaliste-1142590615/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/agence-dinterim-dinsertion-generaliste-1142590615/voir)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js](https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/common.18f25e76.js](https://lemarche.inclusion.beta.gouv.fr/assets/common.18f25e76.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 2
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxlarge/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxlarge/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxmedium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xxmedium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xsmall/uploads/listings/images/ad9b37724d9a82342002cfc9f33a89424a771496.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xsmall/uploads/listings/images/ad9b37724d9a82342002cfc9f33a89424a771496.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/72ecdc109ccd80c11218e37e31da2a5824f65cad.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/72ecdc109ccd80c11218e37e31da2a5824f65cad.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/user_profile/uploads/listings/images/ad9b37724d9a82342002cfc9f33a89424a771496.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/user_profile/uploads/listings/images/ad9b37724d9a82342002cfc9f33a89424a771496.jfif)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 4
  
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
  
  
  
  
Instances: 5
  
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
  
  
  * Evidence: `811161776`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1743023743`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1123563716`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1138015681`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1542050529`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2069819949`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1622061097`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1169396135`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `147785318`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2027611725`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1142590615`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `434947866`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `297038754`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `36881736`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1011653028`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1905883262`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `896762127`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `399349292`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1053082609`
  
  
  
  
Instances: 43
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>811161776, which evaluates to: 1995-09-15 10:42:56</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[start]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `time_range[nb_minutes]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `sort_by`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[nb_days]`
  
  
  
  
Instances: 15
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A34%3A21</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [option] tag [value] attribute </p><p></p><p>The user input found was:</p><p>characteristics[5]=12</p><p></p><p>The user-controlled value was:</p><p>124</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

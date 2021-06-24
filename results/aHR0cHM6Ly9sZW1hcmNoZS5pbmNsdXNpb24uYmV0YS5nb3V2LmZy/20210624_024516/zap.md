
# ZAP Scanning Report

Generated on Thu, 24 Jun 2021 02:24:37


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 5 |
| Low | 13 |
| Informational | 10 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 9 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - PHP | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Application Error Disclosure | Low | 6 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Cookie without SameSite Attribute | Low | 4 | 
| Cookie Without Secure Flag | Low | 4 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 3 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Information Disclosure - Debug Error Messages | Low | 6 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Content-Type Header Missing | Informational | 6 | 
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/119/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/119/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38768261000234`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2533/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2533/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50870892200044`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1448622627/voir](https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1448622627/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `30470797900098`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=1](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=France&location%5BaddressType%5D=country%2Cpolitical&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D&location%5Blat%5D=46.2276380&location%5Blng%5D=2.2137490&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2841.31433%2C%20-5.5591%29%2C%20%2851.1241999%2C%209.6624999%29%29&location%5Bzip%5D&page=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/55/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/55/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38745382200067`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1726404730/voir](https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1726404730/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `38073003600049`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=Oise%2C%20France&location%5BaddressType%5D=administrative_area_level_2%2Cpolitical&location%5Barea%5D=Hauts-de-France&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D=Oise&location%5Blat%5D=49.4214568&location%5Blng%5D=2.4146396&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2849.060525%2C%201.6888659%29%2C%20%2849.7639221%2C%203.166125%29%29&location%5Bzip%5D&page=1](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?location%5Baddress%5D=Oise%2C%20France&location%5BaddressType%5D=administrative_area_level_2%2Cpolitical&location%5Barea%5D=Hauts-de-France&location%5Bcity%5D&location%5Bcountry%5D=FR&location%5Bdepartment%5D=Oise&location%5Blat%5D=49.4214568&location%5Blng%5D=2.4146396&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D=%28%2849.060525%2C%201.6888659%29%2C%20%2849.7639221%2C%203.166125%29%29&location%5Bzip%5D&page=1)
  
  
  * Method: `GET`
  
  
  * Evidence: `584001221343`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1746572229/voir](https://lemarche.inclusion.beta.gouv.fr/fr/profil-utilisateur/1746572229/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `5079667290083`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3664/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3664/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38173482100030`
  
  
  
  
Instances: 9
  
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

  
#### CWE Id : 693
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_medium/uploads/listings/images/301e3986d65b0eff2166fe511498e042a1888cfd.png](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_medium/uploads/listings/images/301e3986d65b0eff2166fe511498e042a1888cfd.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹~ü`/oÏ~r\x0001"@HH\x0000C P¬²Z*"¬R\x0014!Q*\x0015¨\x0014EB\x0010\x0011¨$\x0002*$\x00042Ã`f\x0004	"\x0002\x0000@¨\x0014P©T*\x0005!\x000cQ\x0000\x0000\x0002\x0000@%T\x0014\x0005¨T²\x0000\x0008\x0012\x0000`Ù\x0000 ÖZ´¥YX*\x0008\x0005\x0008\x0000\x0000@¥\x0002\x0000\x0002\x0005(\x0000P9	0@\x0018\x0000	 \x0014!YÇR©L\x0004A\x0000¨T\x0000\x0004B\x0001\x0001\x0000¢R´hK¥"\x0008\x0008¨\x0000bF\x0012Âûc9ÊÂ\x000c\x001aT\x0014¢"$\x0001\x0002l¨\x0011¶ÉDH\x000eì3^ßÜøÉg¯}3ãÅùä»Óæázu\x001c}Û<Èyß]Cr\x0018¶ÝóÓ£Ë~xÚOÎ·\x001f?ù/o~ìWo¿óÛþ¿úá÷æÍ<;ßüÅW?øÿæÏýÁÃ°==ü`ÛÎ^ùÛÖó£ççG[Ê T\x0006\x0003 E%Ô²ÖR	
)HQcI\x0001 ¤Ò\x0004J\x0005 ©ÌBÌ1¶\x0019P©Ì\x000c3¤¨\x0000\x0008\x0008#P\x0001Xe+J-Ù\x0002\x0000*0\x0000\x0000\x0010\x0000\x0000a \x0012\x0000H¦A4\x0000 \x0002fÀ\x0000\x0014\x0003$k-(À0Â\x0018\x0000T\x0000 \x0002\x0000\x0000\x0002\x0014 \x001a\x0008l\x0006\x0003Ì0 \x0000\x0000f\x0018 ²ÖT*V*IR©
	\x0002\x0018B\x0000 R\x0000J-J!*¤\x0002\x0000\x0015P\x0002y^Ë·OWK\x0006§\x0019\x0015\x00182QYå(«\x001c¥R\x0014P\x0019ÆpÚ6¿õê»ÓÉ5Ù(k\x001dVËµ<ÎfqÓr\x001eöÓa\x001dçò|º¸»¹¸{üäo>ÿ_üø\x000f¼zøÖ?½ùÚÿø'w^½¾ñÕ§G\x001f¾ýÖ§÷\x001f]¯OÞýæ+Û~ãúôìáñÑÃã³\x001f3\x00061fÆÌ\x0019\x000c\x0000`\x0004P\x0014Q)V)\x0008@\x0002\x0000@V\x0000\x0008¡¨T*\x0000\x0000!Ì\x0019\x0000\x0000`$)È`\x0006\x0000\x0013E\x0001@\x0001\x0015R!\x0015\x0000\x0000J¥R\x0001"*\x0000PI R\x0001\x0008\x0000\x0002@\x0014 \x0000\x0014k\x001d\x0014!Ê*µÔRK\x0005 \x0002\x0000\x0000\x0000I\x0005 \x0000\x0000\x0004`\x0003"	I\x0001B\x0011\x0013c-¢JÅJ¥R©h©$@ \x0004\x0000\x0019\x0000$©$B*\x0002 RJPàáÈûër]\x001ck!\x001c¥¢Ì\x0000\x0003"¨\x001c\x0005H\x0008Eh\x0019×·\x0017÷ëðþý'÷þ£ÇÓ¶Yë°ã(cÛí²·fÜÏÞ==«emËËW¾¼»ñòùÉ_ö»ÞúÖë¾w{söÓßùÂOûo>~òÕ×_ûêïþÖùÅ[×ëG¿þåòwÿù?ø»o¾ñÝóaf3Ã\x000c3cfÀ\x000c\x0000¢\x0002\x000bIH\x00040HR\x0014U*\x0005\x0004\x0005\x0012\x0013\x0008"I*J\x0005 RY+03\x0000 RY\x0001J%Ì\x0001) P©@Q\x0014
\x0000\x0000T*\x0000 (\x0000 ¢@\x0005\x0000\x0002@ \x0001\x0014¨ Z\x0000F\x0004(b\x0002*k-\x0000\x0000\x0010\x0000\x000c\x0000\x0015 \x0000 @\x0000\x0000\x0008\x0000H\x0018\x0000ke­T@	`\x0019Ð$©\x0010P@$¢\x0002P
\x0008¨$P	B©\x0000@\x0005\x0014wO÷ÏkãÑrjlÛ\x0008¢T\x0000\x0006	T\x000eÁ>\x0003bq9|Þá_ÿÏÿ÷o>óð/ÿÿú'_ëaÃeÛ¬øh¼Ú6çµ<Û¼<|º^íÛf3Ö~òæ³ÏýüñÙû/¿ðo?|ïï\x001f\x001e­ÓåÖÛßúÒ¿ûËÿèãwïüêÛïü£9»9óþï9üúÕ'7fÆ\x0018\x00003\x00034@EY\x0000\x000c\x0000\x00080\x0012B
\x0011Ê
¢$\x001ak-µTVÙ\x0000\x0000JeÍ\x0018
\x0000\x0010T*\x0010
\x0003@¨\x0000Ì\x000cX+d­eÛv\x0000\x000003*\x0015\x0018Ã\x0000\x0002 \x0019\x0014\x0000¢ P1\x0004Å\x000c A$3\x0000\x0000\x0000\x0011Û\x000c\x0000C¥aÛ\x00190\x0000\x0002\x0000\x0015\x0000(\x0006\x0000\x0010\x0008\x0003\x0000\x000c\x0000'\x0000\x0000\x0000\x0002\x0000	\x0004@A@À\x0000,¢¢\x0000("\x0001\x0000\x0000\x0008 T²Ô¨\x0004%I\x0000\x0015\x0003¿{¼út\x001cãI¾{~²oËÍ\x0000p1Ûx^V\x0002\x000cV1£±\x000f\x0010\x0018p\x00136ãóÏßúüóW¾ýðàÏó|ñ¹/Oc­Ãét\x0012®ñ8ûÉy-Ç¶¹1k9íf3··~üÅçþôzõ×ÛÏ}º¸®åætvÞ/>||p<nNòÿò×¾øì¥Û\x0017\x0017\x000f÷¯ýæ8±c\x0006$\x0000\x0001\x0001*
(\x0000\x0001\x0006ÂP	\x0000\x0000PDQT*A1\x0003*\x0004!(3£\x0002\x0003(
\x0000\x0000\x0001`fT`Û6E¬Ú\x0001ÀÌ¨@ef@\x0002@DÒJû\x0018\x0000(DÃ \x0012Ñ6\x0000\x0002©1C\x0018@ÅÀ¶ó¾J±ÖRË~\x00023cfìÛ¦\x0000¨\x0000@ \x0019A!\x000c$0QÌpªÌ\x000c	 \x0000\x0000$\x0011
¡°0Tf\x0006T*\x0000À\x0000Q\x0001\x0000\x0000Ê*3hQ*µT\x0014F \x0005\x00143<¬å?~|ò¸Çµ¼?\x000e:<<=ùÂk7§\x0013PVáv?Ùæðt½º®À\x0002\x000c\x00063c\x0000\x0000\x0000\x000b«\n.þø_ý\x000bÿðÕw>ì»¿ýðÉ\x0017o_\x0015qÞXk<oóZ\x0006_Ü^Ü¯«¯íÊ¶óýßúÑgvi\x001bÏÇr¹¸}ýÆéròêæÖo^ysç|ËÇÓ_\o<nÜì\x0014\x0001*\x0010*À(\x0012@\x0000\x0010 ¡4(0HH\x0008IE\x0011\x0004 R©\x0000\x0014µ4£\x0002PQ1c¤\x0002\x0004`@\x0000mÛÌp\x001c#\x0019Ã°m\x0001\x0000\x00001\x000c\x0000±0e\x000c\x0002a \x0018\x0018¡b\x0018\x0003I\x00180*3\x0003\x0000\x00063cb-\x000c03fÆ\x000c\x0001$\x0003Â\x0000\x00001B\x0002\x0000\x0002\x0000Hq\x0002\x0000 \x001a\x000c¡@\x0000¨$,\x0015\x0016\x0006\x0000\x0018\x0004ÔR\x0011"¤B 23fF\x0005¨TZ
(Z²0j\x0010FÅ >\x001cùöÈu-×«ã°,O-ÿþ\x0007?{óÆÞrt¸®e?\x000ew77nO'\x001f}º^\x001d+°Ï0\x0003c\x0000\x0000ÅÝøÉW¾üá_Æ»ëÕûcy¹µÓ¶Ûg\x001c-eqîpl»¿}xô|Y.§Í`öÓÝ\x0017/ï]§u0¼|ûÆöbó¸\x000esbö«¹¹÷ëýïÝyË¤²ÊV ²¶MQ©ÊQ`Ä\x0000\x000cH¶	©\x0001\x0002B(RYe+\x0015Æ\x0018f\x0010\x0000\x0000\x00193T\x0000*3\x0003*a¢\x0002\x0000@0\x0008P\x0001\x0013\x0006\x0019Ì\x000cQ\x0001J\x0005 \x0011\x0000\x0000 h\x0014Di\x0000\x0018\x0000T\x000c\x00000\x0002\x0012fÆZ§§ÃÌ(àXËõ8\x000c¶\x0019aßv\x0004@\x0001\x0008@\x0002TÆ\x0000\x0002
\x0012\x0018p
\x0008¥Á
0`@\x0000¦ÁP\x0002ÌPÀ\x0018	(\x0011¢\x0004\x0004\x0000¨@\x0005ÔQ©%IB(\x0008
\x0014f|<ÇÙ<áùzõ|\x001c\x001e-wûÉw>>=yy¾H*«åñéÙÃó×÷÷ÞÜÜ¸;|¸^=\\x000fGÙ\x0002\x000ca`Ø0Æ*wç³?~ýÒßûÇòíÓÕéöìÝ`äÀuÛ\ÖÕy²¶ÝãÊý¶Ù±ðÝÊ÷Æãõ0ÆËW¯½z}o=>XûíæâÓå¯6"YXeU6)IHVY¥\x0002"H*\x0002Ê\x000c\x0000
!R)*\x0006Ã6c\x000c\x0000\x0000Øgóúå+Çm\x0006T\x0000 Ò\x0004\x0006@ @\x0005\x0000 "\x000cÂ` k-3£23*k-3\x0003\x0000\x0000@\x0000$5\x000cE\x0008\x0013\x0006A@\x0001\x0015\x0000\x0000\x0019Ê\x000cÇZcÙf¤r\x001cKeÛ\x0006¬@@Â \x0000@\x0002\x0000@\x0001\x0000'\x0000 0%	\x0000\x0000`0
\x0000ÌPa0 B*A1\x0003
\x0000\x0000@R¤R\x0011EE!\x001a\x0010 b\x0010\x001f\x001c3Ö¶»®åá¸ú´®Öfßw¿zÿÁýÛ³\x0000«ÀÃó÷ß>x}wïõý½77\x0017·§åÃõêáz8ÊÙØ°
'@Æ>c\x0000?}yçí7ßùø|õýó³}ÜÎ²ð¼°Ï¸qZË}óíóÕêÆi\x001b{Yëðþ8|Øn=\\x0017¸½}áí·Î^ßß:Îw~ñ¸{\Ùv\x0018\x000cQ´bK\x0008Í¨T@QV\x0019$¢\x0012\x0000*&$\x000c*\x0019PI*3Tj!\x0000çóÙé´\x0003\x0000¨Ì¶yýê3Ï×«u\x001c*\x0000\x0003(Ä6\x0003\x0000\x0008\x0000\x0000T\x0000*3\x0018\x0000B\x0005 RYkÙ÷
\x0003\x0000\x0000\x0000\x0002\x0018\x0006\x0001 \x001130 L1\x0003D23\x0004\x0008\x0003\x0004Pãp\x000c3£\x0002k-¤\x0006L\x0003\x0000\x0000\x0002\x0004\x0010\x0006\x0000A\x0018\x00000*3ã\x0004\x0000\x0001\x0000fH\x0000 \x000cÆP\x0014F\x0002\x0000@Ì¦ÐB \x0004\x0000*\x0000\x0015HT²Ô¦\x0002$	!@A4Â#\x0007¶ÓIx¾>{Z÷×¼8_<\x001cyÿôäÕÍ13fÆi?y:\x001eýí»oýÝû\x001f|vïó»{oÎgwûÉ\x000fÏWOkÙÊeF\x001bkg\x000cûËÙïßÝø÷OÏ>\\x000fwÏöòVNFeßÆÓâ\x0011Ór;ùôôäùîÎ¾í¦ÃóõêÀóvòñ8ËÍw¯ÜÆíÍÿÒ\x000bß\x001dÙ\x0000\x0008 @\x0000¥RY-U*J3$É\x0018@AX2\x000cF\x0014¨TVI\x0012"¶ÙÜß¿p>íf\x0006\x0000\x0000Ì¶Ù¶Íq½ªÌ\x000c\x0008JÌ\x0000\x0000\x000c\x0000\x0000\x0002\x0014`\x00100\x0006@efTj©Í\x000c\x0000\x0000Â\x0010\x0006\x0010\x0000\x0010 \x0002fL!	T\x000cd\x000c\x00103£²+3Æd­hÌd³\x0019\x0003 \x0000\x0000\x0008¢a\x0000"T LØ '\x0000\x0000\x0001\x0005@\x0012a\x0008\x0011\x0008\x000003,µ"\x0000 \x0004\x0000\x0000\x0000P R4Q*\x0015¡\x0004A  \x000f+`ßlç³ç§ë³Ç\x000e_}|ïn?»Ùwÿør¶a±f÷ÝË[§}óÝã_|û¿~÷­W7·ÞÜÞyq¾qÞ7Åk}\x0006\x001c±\x000fÛÁï¾¸ó¿úÖÃõð°o¶ë!¼Ø67ûØÚ,¼?\x000e39ááùÉ»çg·Ûx*Û¶Y6ñþz\x0010çËÅëW¯mï>ù°ßùÕÃ	cf33\x00180(\x0000P©ÔRY-µ\x0019B
É\x0018\x000cf\x0018@Q©\x0014Å\x0014\x0010	Ì6.Ó¾c\x0000@¬µTÌ\x0000\x0000\x0000R\x0018fÆ\x0000 \x0002\x0000\x0000\x0000\x0010ZafÌ6 \x0002\x0000ÇZN'\x0000\x0000*3\x0003\x0000\x0000
B*3\x0003\x0000\x0004@C\x0005\x0000 \x0012L\x0006ãX¶\x0019\x0001 ÃØg,YÛÉ 	\x0000A\x0010
\x00083\x0002\x0004\x0008§
\x0001b\x0005J!\x0004l3 \x0010\x00023£\x0002P	"Q*
@\x0005*3\x0003\x0000\x000cB²$\x0004*\x0000%Pd\x001cåý±LaÜÞÜÚ÷\x000f\x001f<·dùêÃ;ÇÓ¾xáåí}Æv:YeÛ6Û¶¹ì'/¯Ï~xzôÍ§þáã\x0007Û¶{y¹øñÍûÓ~r±ÏØg\x000c¦4Ë¶o>¿¿ó²¯½zööròt\x001c°ía3³a9¯\x001e÷1Û8O~õé\x001fOÆíåÆl¯¯Þ_\x000f«N'¯ß¼ññáX·eÛÆÌa6f \x000c\x0003$µ´¢¥¢\x0000	\x0001\x0000Ê6Ã13*!T\x0008\x0001Q$\x0000c\x000cÈ\x0018f¬µ"\x0019\x0003\x0000 \x000cHÆ\x0018\x0004P\x0000 \x0001\x0012\x000c\x0006¨\x00013\x0003`f@E\x0001Â\x0000\x0000\x0000ÂÄAa Ëùìr>»\x001eWOÏ!\x0001 Ì0ÛØ¶ÍZm3\x0000XÍZKû23@\x0010\x0000\x0000\x00010\x0000\x0000IÆà4Fb\x0000\x0008\x0004\x0000Æ \x0006Ãl£2\x001dØ	Û¨\x0000\x0000´RQ*\x0001\x0018\x0002\x0015\x0000¨\x0008HjYmK¥¨@¥Ò\x000cP H®åß½ûÞ~\ÞÞÞ:NîoïÌÃ\x0007_|¯uuÙ6ï>ýà¯¾úö»?sÞwf\x001ce}ßíûî|¾xu{ç·Öòx\}¸>{Zw¼~òòrvw:¹ì'7ûnß6§aÁîþîÆO^ÜøG×»[Íx<ZÖÚ\x001cåYË\x00036×ûîÓq¸â²\x000fxuÚ½~öîz8Ê¶íî^½ñÍ7÷¾ýÈÌ\x00193Í\x00183\x0003\x0008IÈ4LjQ*²dC¥L#(T4\x000c\x0000$&\x0006%2\x0006 @A
\x0019\x0000\x0000P\x000c\x0006P\x0001\x0003\x0002\x0005\x0004\x0001a0Ã\x001803\x0000 \x0000\x0000\x0001\x0000\x00000!\x0008$c\x00000.çÓiS\x0019*\x0000\x0019H\x0018l3ö\x0019ÏÏ¶\x0019aPË*mÆõ8Ï\x0017³
 \x0002\x0012\x0000\x0018\x0004\x0010 \x0019À `\x0000'\x0018(\x0000 \x0000$(clÛ¬²YÆÐÆÊÌ
©\x0010\x0018	\x0004\x0012\x0000
\x0010J%P! \x0000T\x0000V9¶Í_|÷µoÞ}ïÍéäo>þàz<{|zðq\x001döòï\x001fé÷>ûÌg¯^3cf,ÀyßU\x0016*÷å3¬ëÕóq536(ÇÊ>¹b0ÃåtòÏ~ö;^¿ÿèclÃµ82e­å4Z¦qÞÆÝéäæº<®åÕùdN~üâÎû\x001f>úþz8V.ûæüâ¯;{j\x001931\x0000\x0002\x0005\x0011&D\x001b¡\x0010\x0000\x0005`\x0010`PÉH0\x0003\x0004"(\x0004\x0014ÉÀ\x000c\x0000\x0000\x0008\x0010\x0006\x0000\x0000PÌ\x0000\x0000P\x0001\x0000\x0008\x0003\x0000 \x000c\x0018ÃP\x0001¨Ì\x0002\x0000\x0000\x0000\x0000@\x0018		00¸OfX+lömsuÊÌ(Âh±mããÇ*3\x0003\x0000*fT¾üìsÛ¶\x0011Ð `\x0000!\x0000Â\x0000\x0002Jef\x00143\x0001(\x0000\x0000\x00000Ù8m;Hj1cB\x001b3\x0012\x0019­(J¥\x0000HD\x0005\x0000\x0000\x0012HB¥\x0016¥ ¤P\x001a \x0000¨ìøòrö\x0007o?scüê«ßøþ«¯<|ó5¶ë³:\x001c-ïNÿoNþÛùßØædfl3\x0006ÛU5©ÀjÜ7Ï\x00060 Ê¾Á\x0006òêöÆ?¿½ñ´òîñÉ/~øèy-Åeßìå\x001aGÜì»+[¹Î¸ß7Çåì²ñÝóáz,·§§ó½_?
a¨Ì$ID%\x0014ÉD`ÑP Xå8\x000ek6­\x0000\x0000\x0001\x0001\x0000P	\x0001\x0008@2Ô!a\x0000À`\x000003\x0000\x0000\x0000 af\x0000\x000c\x0000\x0006a\x0010@ÁÌ0L¬µQ\x0019Ç:1\x0003\x0018\x0000\x0008\x0000\x0010\x0006@\x0000\x0008\x00030N'3\x0003`f\x000c\x0002\x0000\x0001(\x001a\x000673²Ö²!\x0004mÛ½yõÂ¾\x0004\x0008h\x00040\x0000\x0011\x0006\x0002J\x0000 Å	 0\x0000\x0000\x0008\x0000cìûÎ\x0000\x000b#[Ë\x000cÓ`\x0004¨(\x0015A L$P©\x0000TD\x0002J¥\x0016E!1\x0008\x0008Øðzx{sqÿåýñ\x0017_úøGäã§OÖõj­ÃÓóÕûO¾úôÞ/>}ô\x0007ß}ç§ÿ\x0019µRKUÂ6c!®kiØg\x001ce7¶mì1pÙÆ\x0017·7¾þøÉ/\x001f\x001f]öÝÓ¶±âáz¸Ý773.Øìå²\x000eß<=yZË69_<¯¬YcÛ6\x0015\x00166DQ\x000c\x0003\x0000AJ-ÏÏO\x00177ÙÆ6cÂ\x0004 !$C$É`D\x0001bB\x0018Ûór\x001c\x0007HÆ\x00000\x0014`0cfÀ\x000c\x0015\x0006$\x001903 \x00001c\x0002\x0000Â\x0000Û\x0010ZYk\x0019P\x0011§}\x0007 \x0001\x0000\x0000\x000003*ÊÌ\x0000\x00000\x0012*3\x0003\x0000*3\x0003àþîÖ>#Ë¾mf`\x0003mÆýý½·o^\x0002AH\x0006\x0000\x0008\x0010\x00000B\x0000\x0000\x0013\x0000\x0000a@¨À\x0000`&§}3Æ*\x0006Æ\x001aF6ÆØ\x0000©($\x0010\x0008P\x0001\x0000DIJ¥ ¢BÂ\x0016\x0004\x0014(\x0006§3Nûæ´í^^.¼z\x001c+ß=>Z\x000f\x001f½y|ëôþÿÍ;?zõÚíå¬\x0019\x001bë:¬2F²ÍØÁ*û`Æ6£(\x0018kØÊB\x0018Ù\x001fÝ^üïÞù0W¯ÎËÍûmSyZËi¸Ù7#·òé8|x|p\üæ\x0013®\x00073înnìÛh\x001d(¶m¬cYÃ²oJ¥"¶mh\x0003k\x001d>=<Z×g/oo÷[§óÙZËõ¸:\x0002\x0018cA\x0002B(
ÀíùÆËû{Çºúðñ\x0013\x0010\x0006\x00080af\x000c`\x0006`À\x000cÁÌ\x0000\x0018\x0010\x0018#1\x00080\x0000c\x0006Æ\x000c,OO\x0008Ìýt\x000203\x0018\x000c\x0002\x0000\x0000\x0003\x0001\x0000 \x000c
Ì\x0000\x0000P\x0001\x0000ÊÂýÝ?ùùï[ëp:öÝl\x001bÆ¶möms>_¼¸¿\x0007	h\x0000\x000c\x001a@\x0000\x0008\x0000\x0010\x0000\x0000\x0000'\x00080`\x0000À\x0000 q{sv:m§\x0003\x00040\x001c\x0018l-c³Je$\x0010\x0001\x0000P\x0001\x0008BQ*$ILK3\x0010\x0000iãê|>Ë²0¸®åù8ÔòùåÆÓÅofó¯¾ò¯¿ñ~ëÇ¶	£Élc[¬²Mö\x0019±â(Ó£\x0001ûFP\x0016\x0016¬lÃ\x001dÝ^¼<íþê÷>^.\x0006/·\x001bgËó±¬µ¼¼mòx\}ûñ_}xof<[>]¯àærázõðþ½m6³mfÆ6ãtrNö}÷¼ïÎçÓ¾«À¶óÅõrãùüìr>ùÑëW~ôÙ[w·÷±Öòðøèz,m!JFYÌ¶!k-VUÖÊ¶\x0005¶\x0019·7\x0017·7\x0017×ëxØ\x001eT\x0000\x0000À\x00183Ì\x000c\x0000af\x0004\x0000\x0000\x00190\x0003\x0003\x0008\x000cf\x0018À\x000c\x0019Û6*ÀRÙ¶}Û1\x0019\x0000\x0000`fÌ0\x0000\x0019\x0000°
T (\x0000Å\x000c\x0000ÂPÙ÷üä§`\x0019
Â\x00181
@\x0000F\x0000E\x0000@\x0018\x0000\x0000\x0001\x00008\x0001@PÌ\x0000\x0011@1À¶mnn.Îûæ±+\x0006$\x00005l¢(¡"@@T*\x0000\x0000AI*J%L\x0000\x0011\x0000Á§O\x000fçgË\x0019Æh\x0006ìÛf=?ùðôèèê|{ñ\x0017_í'¯_zóâ^ÆÌ\x0018ÌÅ²\x0004ö\x0019ÀÂfQ\Wf`\x000c\x0002·ÝÏ_¿ô7\x001e¼½¹qw:{|¾z^ÏÖrmùt½øóÙãÙ?|ÿÎo>}°fóæîÎÇçgp{së¿úãûðá½ÁÀ\x0019ÛmÛÌmÛ¡ÀÌ8íg§óÉÍåÆë¯¼}óÆårkÛ6OÏÏjayz>äÿ'\x0008O~vÝ÷\x0003/ïúþîûyÞw5{íîc\x001f[JPMT()&Dj !\x0006\x000c\x0010\x000c\x0010Iþ¨\x000c"1\x0004&0"R\x0004C\x0002¥J\x0006\x0011\x0015\x0004S¶c»íÓxï³»µ÷ZëmûþäºY\x000b#Ìµm
è<\x000cöm·¶ÍÚ6c¬µlk¹ì»Ë¾YkYks½\\x001cÇa­e­,5ãÄ1ÃÌaf¬5`flk©±Ö23\x0006f\x0000lÛr'\x0000\x0019Û¶ÀaÆYË¶í\x0008©Ì,3\x0003\x0000\x0008\x0000\x0000Ì\x000cÂ\x0000\x0000\x0000\x00008Ï\x0013\x0000@\x0000\x0000\x0000 À\x0010\x0015a¢\x0011\x0008iÆ\x0004	\x0003\x0018\x0014`\x0002\x0000`(A@\x0011@
Ø\x0001 \x0002I\x0002\x0010@!3cß6kb\x0004 \x0018\x0004sÚ:å\x0004JC`\x0000\x0000H*$©SEQ
b¨\x0000 \x0019OÏOÞ?ç¥±m\x0017ûæávóîéÉwÏþúá¶\x0017ÛæÇ¯^ùÕÃ?úå¯ü+¿÷»Öu\x00003Ô82¸lcpbf	Ç\x0019rÆu_\x0006ËXÃ\x0018á(¿ñòÞï¿~Å¶»®ñáÃ§\x000f\x001e:=§_¼ã\x000f\x001f¼Úo\x001f>øá8=â7NÞ>=\x000b×ËÅßû»ÏZ\x0001\x000c\x0002\x0004\x0018\x0004\x0000`fÌµ6ýb¿\¬Yó°ÖØ÷åÕ{çyÊ\x0018Ã\x000c`\x0000\x000cf1\x000c\x000cØÖfß7Û¶\x0019ö}3Ã`mË\x0000\x0006Sì\x001br\x001cËZËZË1+°ï;0¬5\x0018Û¶9ÏS1ÃZ\x0005\x0000fØ¶¥²Ö2C\x0001\x0000\x0005\x0000\x0000\x0010\x0006\x0001\x0000\x0000\x0000¨\x0000\x0000\x0000Ô©23 \x0002\x0001\x0005\x0000Ò0`@\x0000	\x0002\x001a\x0006	#0C\x0001`H\x0018\x0010\x0002\x0008\x0003ì\x000003Â\x0000\x0008(\x0001Â\x0000 \x0002\x0003\x0006a$\x0000IÁi\x0000\x0010\x0002ÊÌ¨\x0008\x0010P©(E R\x0001¨\x0000ÁurÞÍZ¦lÃÛÇ\x0007ÿ¿ï¾õöùÑuß½¾Üùüî\x0005ÆæÉ¯\x001eÞûã/ßú½Ï>õãO?e5cpb\x0004Bq5cÍ`
ÌP\Ö\x0019KÎ3pànÛýæý?÷`9yzôÝãwÇÍóyz÷OOÞ\/nxwrwwï½ñÝã³Î¬µ¼zõÊýÝ=\x0006\x0000T\x000c\x0002\x0000\x0008\x0003\x0000fÆÌ\x0019\x0015p¹º\.H\x0005´A\x00003c$T\x0018\x0010ÆXk\x0019À`_ËÊ6cÖ2HæÌ\x001aó43fÆZcfLì³0`bÛ\x0006	ÌZS\x0005\x0000fFe-\x0018&\x0005\x0000Ìe\x0002\x00000\x0000\x0001\x0000\x0000\x0000\x0000Çyz||r\x000fÎóT\x0001\x0000\x0000\x0008`\x0006\x0008C \x0000\x0003\x0010\x0006ÆH\x00020\x0000\x0018\x0014\x0006\x0000\x0000H\x0000\x0008\x0003`\x0007\x0002\x0015¢!\x0000\x0000`\x000c\x0000F"`À fT PH%4\x0001\x0004 \x0002\x0000Pä,dH\x0012 \x0005	\x0000»ÅíéÁ»ã\x0010î_½ò\x0017?¼õ³\x001fÞz}¹øñåêóû\x0017.k÷t\x001cþê«/}pºûÑOüá\x0017_ù×î_xñò\x00053ÌØ\x0010ÆÅy&QNÖbf,ã8i gÀ\x000cÅlËo½~éÏß¾õx»q{ötóôp»ùpfÝmneÍòáäËÕ±Æ·ÏÏNkÆ\x0011Û¶+f\x0000¨Ì\x000c(\x0008\x0000\x0000a
¬µÀ\x000c&\x0002\x0018cTH\x0005f¡NÎ\x0014k\x00163fNçy8af\x00043\x0006&b\x0006³Laf13\x0012Æ2\x0000ÂL\x0018³"\x000c\x0004\x0000\x0000f 3\x0003\x0019\x0000\x0008\x000b\x0014\x0000\x000003f\x0001\x0000\x0000\x0000\x0000 ²Ö8ÏÓÃÓ\x0007wwW³\x0013@ef\x0000\x00143\x0000a\x000cH\x0006\x0000\x0004\x00001\x0013\x0000\x0000¥\x0019\x0013`\x0000\x0001a"\x0001\x0002@\x0018d\x0007\x0000\x0002!\x0004\x0000\x0004 \x0002!L¡aP\x0012\x0000\x00030 \x0010\x0000\x0000\x0000	Q*¤BB!H\x0001D0Àäã}óöùæË\x001f¾6\x001fÞùøøÜÏ?|ðp»¹ßw¿~xðåÃ\x0007?}ñÚ¯¿ëË\x000f>ùü3¯×Å_üÉø|ãïüÁ\x001fØ.\x0017Û¶\x0019tKe­q9b\x0004ÏÓÌX1k(Oçi
3,C¬\x0019G¼¸ì>ZãûÛ³­ìkYçÈHÎÓÛ#ÿâÝ¿p·üE§m.Þ>ß\x001cçi¥\x000e\x0015(\x0000 \x0002\x0000\x0000\x0000\x0008\x0000aP\x0000`P\x0002\x0008£RéÌq\x001e*kmÖÚÁq\x001eº¡DQÌ\x0010Ä@\x0012Æ`\x00061(\x0000\x0000C\x0018`\x0004\x0000\x0001\x0001ÅL\x0008\x0000\x0019\x0005@\x0018@\x0000\x0008\x0003`fT\x0000 Xk¹Ý\x000eï>¼³Í¦\x0002\x0000@\x0001\x0000\x0004X*03\x0000\x0003ÈD\x0010\x0001\x0002a\x0000	`\x0000"\x0008\x0000U)Q\x0000\x0000@\x0008\x0000	©$IhH(I (\x0000@B¥\x0002¤\x0002P©T\x0014AHNu"P\x0010NÊOîûýê»g¾yÿÁ_½}ëÇ\x0007÷·g¿øá­³|ÿôä/ßýàÕ×^ß¿p÷kùÃ/¾ôÍ»wÎóp§`-Û,3#4T\x0014±ÍrYËeÛlkÙÖ&\f¬\x0019áVË
Öò;o^Û;¬\x0019û\x001aûÚ\·Ý«ýâ²6§ñ«ç\x000fmÛ´6ß>\x001fnGÖZ\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0008\x0000h\x0004\x0000 pvz~~òøøàééÑíöì8nãpÜnãæùvóüüì8\x000fg§ÎC\x0005À\x0000\x0015å<\x000eçyH\x0002\x0011Á@A\x0000\x0000\x0000\x0008\x0011\x0015\x0001$\x0010\x0002\x0000\x0000\x000000
\x0010 \x0004\x0000\x0000f °­ÍóóÍí8
\x0000\x0001¨\x0000\x0008
BH\x0000B 	\x0000\x0018\x0012\x0000\x0004h\x0000\x0010\x0000²Ã\x000c\x0000 \x0001\x0000À\x0000D%LLi\x0001f$Ó I\x0005\x0000P\x0000\x0001\x0000\x0010 *JE\x0014"\x0000ê\x0004\x0005!5>ÞÇ¿ùÙ\x001b_>Þ;}èæÓ\x0017wî¶ÝW\x001fÞ¹n\x0017?¹åO¿þJk\x001ckó\x001cçéÕìéÝ{ÿÓÏþÂ¿ñ·þEû,fl3öm9\x001bg§Õ¸9\x001dçiëZöµ(\x0006Í¸5Ã°\x000c8q¾yã»\x001f¾÷å\x000fï\×æý¶µ°XcÖòÕ\Üf÷éåêz¹x>z<n^¯\x000b¥N3\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000T\x0000\x0008 \x0004\x0010\x0006\x0004*·Û³§§G\x0003`ì\x0017Z8ÇZÃ:\x0015P\x0019K¥Nuzzzr»=;Ãív
ã<O3cÍX³\x0004b\x0006
\x0010\x0006@\x0005
Ã \x000c
\x0005\x00000\x0000\x0003Ô\x0001 \x0019\x0003\x0000f\x0006@1\x0003±­A\x0018\x0000\x0019\x0000\x0000Â\x0000F\x0002\x0004\x0018@Æ X\x0003\x0002\x0014\x0000\x0001@\x0008\x0001\x0000@\x0000v\x0000\x0006\x0000P\x0001!\x0000HEf(\x0001fF2R\x0019\x0003 THE\x0001¨@@ÈtRrJ\x0008!\x0015\x0000\x0005@1ñ\x000fôÊÿóç_ñãøêí×~öÃw^~ü©û×^­åíÃ\x000fOO~òÑk¶ÝyÎµüäã7~õôàÏ¿ùÊï~ý#¿óã\x001f³ÆlmÍ¨ì+OÇa°­q35ã»\x0019kX²Í"fåw>ýÔWïÞùþùæñ<­µÙ×æ²ï.×;ö\x0017×«O_¼ðÉ¾éáæáù\x0011*\x0000\x0000\x0000\x0000\x0000\x0015\x0000\x0000\x0000H\x0002\x0010\x0008@\x0004T\x0000`fìûÅÌçç'ÇqYËqÜ·ÃZ9Ãyfm.{9=?<úðá­ï¿ÿÖÃã\x0007clû\x000b¯^î\x0014²f³¶å²mmÛ¬µÌ\x000c\x0000Â¨Ì\x000c
\x0000!\x000c\x0001T\x0000 \x0002\x0000\x0000\x0000@Á`\x0000!\x000c\x0019@`\x0006\x0000a\x0000\x0000\x0000\x0005A2\x00000\x00141\x0000Ä\x0018	\x0006\x0001BA	\x0000@²\x0003C\x0018\x0000@\x0000\x0010\x000230ÀDd $a\x0006\x0010*3\x0003HSRI\x0008¤R\x0000@\x0000*É_Þù\x0007¿ÿ7|9»ó1çáééÉO®÷óôõû÷~úÑ\x001b¿ñÑÇÞ=?{>\x000e¿|å\x000fï\_¿òáÌ\x001fþõ\x0017>ÿè#¯×r`
ÛZf\x0006ÃÊ\x0005Çyz>N·óTmÆZËà\x0018¶Ó\x0018ãÁ6ãÓW¯ýèõ+¿üò+//\x0017×ËÅ¾_í«ËåêrÙ]¶Ý¾\x0016ÆÚÆÛaf\x000cÎ²\x0001\x0000\x0000*\x0000\x0000\x0000\x0000\x0000 \x0004\x0008B hÌ\x0000	ÀÌ¸\.ö}WYÛæ<NÛ¶[kÃé<NdÖ2Få<O3ãùöÁ»÷_{x|ë<No>þMlnçÍÖn$£8Î!ÖZ\x0000\x0000
¡R\x0001  @1\x0003\x0000 0\x0008\x0003*\x0000\x0000\x0000#\x0004\x0008\x0000a\x0019`f\x0000\x0018\x0000\x0000\x0008\x0003\x000c\x0000@\x00013TÆ\x0010\x0006ÂH \x0010F\x0018!\x0000\x0005\x0004\x0010\x0004D\x0003À\x000e
0\x0006 \x0000\x0000PÀZ\x00140\x0018\x00004T \x00100\x0002@@JE	 JE)\x0004\x0010 \x0005)@\x0001CrÙw[ËÇ¯_{õúµã8<\x001d7·O?1ksËÅy\x001e¾y~ôzßÝï\x001fù~]|ñÕ×þù¯¿ò·ë¢Á f-\x0010ö5Ö,ÜTÏÌyºlËcã~-Û!f\x0018cÍøÝO>õ³·?¸î\x0017×ËÅºÜ¹\.î®\x0017/¯Wm·fìkÙ\=Ün`ft\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0019
$\x000c¨\x0010¨ÀÌ\x00000cÍb\x001bk-3ã²]Ù/`fTnÇÍ²lûæ£×yqÿÚíöììtÙï==?yx|vw½Ú·ÍÌ\x00193KefYk\x0014
\x0000\x0000!@ Tf\x0006\x0000TÌÊ\x000cP!3cfT\x00000H\x0001\x00190\x0000C\x0000À\x000c\x0000\x0000\x0001\x0006\x0004\x0000\x0000\x0000@@\x0000@\x0002\x0003ÀP \x0019À\x000e\x0001\x0006a"\x0004¨\x0000a°Ö&\x00191*0\x0006FR\x0001Ì\x0010\x0000@\x0000\x0000\x0002\x0000Q:C\x0012B\x0002\x000cR\x0000	 \x0004¹§rµsÆ¾_lå,·N÷ûæýíôjÛ½X»Nq|ô?úõ×~òæ#¾ù\x0019cl\x0019kÆe[\x0018çë¹<\x001f§Ûqx<\x000eg9ÎÔé	×}YÃfq\x0018Óé£\x0017/ýö'øîñÉÝåêz½º^®.ÝeÛ­µÜ¯e_Ëeî<§03Î\x0012\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000 4\x0008\x0000\x0013
\x0000\x0019\x0000P§ã8çiö±­aYË`¤\x0019»ÆZËÍ¶]Ü]À¬
Ëåbßv3\x00140\x0000\x0010`\x0000\x0014\x0015\x0008\x0001TH\x0006\x0000TfF\x0005\x0018@
Â\x0000\x0000\x0000\x0002\x0004Ì\x00001\x00103\x0000!\x000c$\x0003`0¡Â\x0000(fHÆ\x0000\x0000\x0000@\x0001\x0005\x0006
\x0000À"d\x0006\x0000P\x0006\x0000\x0010\x0000B%9E\x0000@\x0005\x0014\x0001Á\x0000f\x0000\x0014E¥\x0002@\x0013\x0010*JE\x0011B!\x0000ISÌ23î·Í«ËÅ>c3\x0006³TÂÝ¶yy¹¸nûµùhß}þú\x000fkùã/¾t{zr\x001eÛq:ÎÃyNOÇé8O#×µ¼¸^¼¸¿zuwµ¯ÍY¶\x0019Oçé8s³\x0014a­Íårõû|ânß]÷Ý}wÝ7msYc±Í¸\x000eÇZ¾¿\x001d*k:\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0010\x0002\x0000\x0000\x0004\x000c@Ì\x0008\x0000 êt\x0007\x0012\x0008!\x0001\x0004Á\x00190`0\x0000\x000c\x0004\x0008\x0001\x0000\x0000 \x0000¤¢@\x0008\x0000
\x0010\x0000\x0000\x0000B\x0000*\x0005\x0000\x0000\x0000ÀÁ JÈ\x0000\x0003\x0000$\x0000\x0013B$\x0004D\x0002\x0000$\x0001\x0000 ©(\x0002\x0012 \x0000` 	\x0000\x0001Ø\x0001*#\x0000 \x0008\x0000Aó@"\x0000fF\x0005*¡$\x0000\x0010\x0000¨¢NP©T\x0012\x0000A0\x0014$\x0011\x0019gÜÊ\x0019§£ÁÌ¸Ûwg9Î¼?nf²Ö²}-û¾ûèõ+ñí·~ëÛïüî>×ZÎsi\x000eZfx.am-Û\x001aû¶yy\x001dO·\x0001;nçiÅZ±Ý\ß}ïåÓ;/ofùa¿¸l»YËÌXÆ6c±÷ÇÍyf­åvÜ\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000$@\x0008	
\x0000!\x0006¡ÌÊÌ\x00008ÏÓy\x001e:c\x0001\x0019:Æ\x00024ÊÓóçç}ß\x0000A\x0000\x0008\x0000TH\x0002\x0000P!\x0010\x0014(\x0000*03*3@\x0019\x0018@
ÀÌ\x0000\x0000\x0018\x0000\x0018\x0004\x0001\x0005\x0000Æ\x0002Ö@\x0006\x0006\x0005D2\x0003\x0000Â\x0000¡\x0001\x0000\x0000\x0000\x0000 \x0001\x0000\x0000Ø\x0001À@2\x000c
\x0000\x0000\x0006"fFAÎ91Æ\x0018\x0001EE	@BA*\x0000\x0015\x0011RIHT\x0014\x0010\x0010H\x0000F¾¹åÉ2Nçyµ\x000c.kiÒ£ä´£ÙÌJ§33W÷/ü°¿÷?ÿÏ_½ðfûÈ¹Æf\x0001Øf\x001cx:N\x001d}µm-û¾qf
ËÌâÃ;÷¥ùøÞo>~ëúüÞãÃ£WûüßïÿYc112¸N?§ã<mk·\x0000\x0000\x0000\x0000\x0000\x0010\x0002L\x0000BRÌ\x0000\x0000\x0000P\x0001¨Ì
ÀÌHNÙ \x000cÂP§ó<¬5\x0004\x0018\x0006pvzxøàéëÝÕÖ²Í@
\x0002\x0000\x0015\x0019 H\x00010\x0008\x0003%\x0000	d\x000cF\x0005*(af\x0000\x0000\x0000\x0000\x0000\x0010\x0006\x0000\x0011\x000c\x0002f@2
Â\x0000Â\x0000\x0000\x0000\x0000\x0000
\x0005\x0018@\x0018*\x0019\x0002\x0000\x0008\x0005\x0000@\x0018`\x0007\x0000\x0000\x0000\x0000\x0008\x0000\x000c¨\x0013É \x0000§¡\x0000@\x0008(P@¥23 $PQ*¤H\x0000D\x0004*oò_ýóoüðæ\x0013ooãvs~øàØ7/îïÌ¶YÆû§'-î.WY&k²ãÞnMn¼ñÅ/~éýüþWÿÂëºc[Ö°f\x000cöafs§ÛyºÝn®ÛfÅ0k³\x001eÝýùÿìï¾ý¹ã§ùÑë{Ý¿r<m®»ýá?{|ëçÏÓÚÐ8åÁ9yçãpÙ.*A\x0018\x0000P\x0001\x0003\x0011`\x0000\x0002\x000c\x0002¤¨\x0000T\x0000 \x0002\x0000P\x0019û~±ÖfÛ6Ðd\x000c Ûífßd\x0006A\x0014Çqè\x001c\x0002\x0002\x0000ÌP\x0014\x0015\x0000(BÂ\x0000\x0006\x0008\x0003"\x000c\x0000\x0019\x0000\x0001\x0000\x0000\x0000\x0001A\x0010F\x0000P1\x0000 \x0003\x0006\x0018B\x0000\x0000¨Ì\x000c\x0000a\x0002Â\x0000\x0000 \x000c\x0000`\x0008\x0000\x0002\x001a\x00060\x0000`p\x0002DQ*\x0010DN,\x001aA1\x0001P©SE\x0010H\x0000@
©T:J¥\x0012H  À­ñ_ùÎÿãëïýK~êÖòÕwï¼ñ7~ô#·NÇáO¿ùÆz~öêåK³=!³[À>\x001c3î·ååýë'\x001fù_ÿÚo|úßþÑçN\f3³¬\x0019§±-ÖlfádC\x0018cûåÏüæ\x001fý¿üýýÑßþßsÿòµl;cïýoÞÿÊ±Ý{w¹¸l»µïfÆ¾Æw·G¿êæù8­\x0019Je\x0006 \x0005\x0000\x0010
\x0003\x0000\x0000\x0010\x0010\x0000P\x0001\x0000\x0000¨ÀÌ\x0000\x0008k-k-\x000cÂ &,c¬µ\x0000AÀ\x000c39;Á\x000c\x0000\x0000\x0015(\x0008\x0000T\x0008$ @\x0003\x0008B \x0000\x0011&"\x000c\x0000\x0012\x0011 \x0012Q)\x0008c\x0006\x0000(À@\x0004aÁ 0\x0002\x0000\x0010\x0006a\x00143\x0000\x0000\x0018\x0000\x000c\x0002\x0000\x0000\x0004\x0000\x0010\x0000BÂ\x0018\x0000;\x0010\x0000P!\x0000\x0000 T
\x0013\x0018\x0003\x0013#CK\x0005\x0000Ä \x0001(\x0000*$¢T\x0012B\x0002!
@AÂà/ó>þÆoÿTÛæÃ\x0007_ãoþÆmÆ/Þ?Xw\x0017?ýøÇãôÅ»·>|ïÍÇo<Ü\x000e}-&ÛòÙëüâwþ¿¿úk¼~åõ\x0017q¬ìk9¥X3fFÃ`ÿö+/ÿø¿÷û¿ügþþïü
¿õ[Óå²q\x001cfÙ7Û\\x0019Äß}÷Þÿâý\x0017þÑÝgöËÅ~löµÙ·Í>¹âñx»5àì4\x0016Ð0!\x0002\x0008\x0000\x0000¨@%©\x0000\x0000\x0000@%\x0000Tf\x0006(\x0000DQÌdÖr¹\ÁÌAqwwït33\x0000\x0008\x0000\x0000\x0001 \x000c \x0015(\x0000\x0000 (\x0001#\x0018\x0004@\x0013cfÊÌPÌ¨Ì\x000c\x0000ÊÌ\x0000\x0018\x0003 \x0001`d\x001a\x0000\x0004À\x000c\x0002A\x0001\x0001\x0019¡ \x000c\x0001\x0000\x0000\x0000\x0000\x0000\x0001*°\x00030
a\x0000\x0000\x0000\x0010\x0012"2\x000cÊ\x0018\x0013k\x0000@\x0002$ TfF\x0010!\x0001A*B©\x0014\x0008\x0008ðxæ¿y{xóêÏï®¾x|ðÏ\x001fÞûO>rÙëZ~ýð`:ýÖ\x0017î×fÊÝõûë½)\x0015ÒäÃùèéxöt>s9½øä/¿úÚ\x001fÿê\x0017þÞïümXx>Owûf0\x0003ãÃ÷ß;ÿøð;úOüÞÓwþÎ\x001fü¾Ï?ÿ\x001c§Îe&s:Çlåj/ÄÿîÃ[ú|ï¯Ökg§Û:íçMòbÛ|ßÍçgcÌ:±(\x0004\x0019Q\x0001\x0010\x0000\x0000\x0000\x0015
)\x0000\x0000ÊÌJ\x0000\x0000 \x000c`\x0019fm\x0014\x0000ÊÌrw÷R\x001e­5\x0000
¨\x0000\x0000@1\x0013\x0002\x0000\x000402\x0008\x0000Y\x0014\x0001\x0000\x0000@\x0000\x0000\x0000\x0008\x0003\x0000\x0000\x0000A\x0001¡\x00010\x0018@Q\x0019P\x0019\x0000\x0000a@\x0000\x0000\x0000\x0000\x0000À\x0000\x0004`\x0007 \x0000 1\x0000\x0000P*0 ¢\x0019DÌ\x0010 RTH	\x0000I\x0000\x0000PÉ\x0000:2Æ\x001f=äg·ñû«oüÕûw~ãþÞï¿|é~-\x001fnÏ\x001eg^¯}
òb[\x001eÏÜd&Ëa9Ým»Úqxq=½¿üàOùs¿õÉg>}óÆeg­¸l·oßúó?þýÑÿøOl_ÿÊ¿õßýüs6\x000f\x001f>âîÎ¾å¼e
³6öÝfdùÝóçé[ÿÙyï½ÍÓqóx{öp\x001e®Ûòæº{|~±f©\x00131Ñ(@\x0005\x0000\x0000\x0000\x0000\x0000\x0000H\x0001\x0001
T`f(a\x0000a\x0006Â \x000c \x0000\x0000\x0000°Ö²­\x0005\x0000\x0000 \x0002¢\x0000a\x0000¨@2\x0006hT\x0008\x0004\x0005\x0018\x0015\x0000\x0000(81\x0000\x0000\x0000\x0008\x0003\x0000*3013f(LXj\x00180\x00034\x000cJ\x0010\x0006\x0002\x0000P1Ca\x0010 \x0001\x0008T`\x000c\x0003@\x0000\x0000\x001d\x0000\x0008\x0000\x0000)\x0012%@\x0002"1Ì\x000c\x0013\x0006T ¢\x0008\x0000\x0001B\x0008¨T` (\x0015¥\x0010P©T\x0014Å\x0000\x0019äÝÉ?y\^îËÛ³½ûÁÇ«?xõÚuwÏÏÞÝT>Ün>»»ó|\x001cn.kùp{Ö0¸§5}Ø×æ0î®/¼zó¹·ïý³¿ú¹õ_ziÃû«÷ï?øÃ?üCôÿþï}ùë_êºxùÂÿÕééñðñÛïÜí\x001b\x001d»\x0017¶Yæ8Y§µvöp9OÿÊùÁÏ¾ñ_Î+\x001fÎÛwÇ³Öò¿~õ¹­SefgHA\x0000\x0000\x0000\x0000\x0000\x0000\x0000*\x0000\x0000@ 23\x0000\x0000b\x0008"Ì0\x0000\x0018$Q\x0001\x0001À@\x0004\x0000\x0000\x0008	\x0013	@\x0005\x000cA\x0018 (\x000c%Q\x0000a\x0000d$c\x0000\x0000\x0000\x0000\x00143\x0000\x0000\x000c4L\x000c\x0003\x0008\x0003\x0000\x0008\x0010\x0006\x0000\x0002\x000c\x0000@\x0000\x0000 \x0000\x0000\x0018\x0000Ä\x0004\x0000À^\x0019\x0000 \x0000\x0001`\x0000\x0018DqÊ\x0018#4\x0018
J\x0012\x0000 \x0014@\x0012\x0002\x0000	\x0000\x0004\x0000!$\x0001P\x0008üå3?{<søòáÁG«ß{õÚuÆ·\x000f\x001eÃs§§óðÑõÎÈÃíYe\x0019\x0019ö\x0019§<\x001e§ÁQ\x000c
k-\x001f¿¸÷ôé\x001b?ÿî[¿õë_û¿ùSùgæþãì\x0017ÿügÎ}Ì«æÅóðmã¿|\x000f_½÷\x001fXþ@Ì2³³6³2ÇaÛ6ë²»Ì2Æëò¿ÿÞ\x001f=þñm§óp;ýí_Ûä,³Æq\x0018df\x0000T\x0000\x0000\x0000\x0000 \x0002\x0000\x0019\x0000\x0000f\x0006\x0000\x0000\x0000\x0010\x0008\x0002!\x000c\x0000\x0010\x0019 \x0002\x0010
\x0008@D\x0005\x0000\x0008$\x0000\x0015\x0000\x0002\x0010 BÂ 	\x0013¨1\x0002f(\x0006A0*P\x0019\x0000\x0000\x0000\x00000\x0008\x0000\x0000ÀL\x0018\x0000\x0001Â\x0004\x00180\x0000Â\x0000\x0000\x0000\x0002\x0000#\x000c00\x0010}fTf\x0006!\x000c$\x0000À\x0004áD
\x0006\x0019\x0002\x0002\x0000\x0001(\x0008$ \x0014B*\x0002\x0012\x0005D"*
ÅÿçûG?ÿì£ëÕÝ¾ûí¯\f|ýøàÝíÉe6ÏçénÛ½Þw_?>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_medium/uploads/listings/images/60d0929e718d7522619d9a2f58235061bac39b8d.png](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_medium/uploads/listings/images/60d0929e718d7522619d9a2f58235061bac39b8d.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¦n\x001bå|¶n\x001bª\x0002U\x0005ªJU©*PUZkÆh\x001a¶*\x0012£X¶a\x0011Ó²nO«·ï?øá»?øýï~ïËo¾t}óRÒ=?={óãþóßÿ½ÿò÷ÿÅíÇ[UE*@\x0001\x0000@\x0000\x0010\x0000I(ªH¢õ¦ÆÙrz¦8ì&Í0ªÌS³m^e75OçÍÓiõÅålßÞ£÷ÝÔ×ÆÔÌ-Î5Ì½i-.®.\^í±¸¼Ø¿þ¥/¾úÆg×WUÛÍÚÄh¶Û¹¸º4Ï;é{i{ÑEI]ºzqíúf¯@)TQJU©*\x0005P\x0000\x0012¡°;\x001c\\\[Õ45£5£ÏMª"ôýÞåë×._}nq°ßO^ÜÜXwq<\x001d===ÝÚjs±¿ÖôÞµÞ¨D\x0012\x0001¨\x0001\x0014\x0000\x0000\x0000°át>\x001açgÎ'¦t>ÉÕKÛé¥Óùh7ã"ªÇÅÅì\x0017ß|ãoþõ¿õÏß½õðü[ÛóIMr|¸sûá­Çû_ºÙÇÐGQO|8çóPUv½»9ì¼ØåÑ¼>ÈvF)¤OöûÃå¥y·Þ$ 1ª¬Ûf[W§e\x0011´\x0006@¡$zºÞJZW¢B\x001aÓ\x001c»]sØwµm=zzzp:T\x0015$J\x0008TQ$D  À´ë¾üú3¿øæ+W\x0017\x0017Zëö»\x000b¹yil\x00074­ï´\x0016U\x0004PU ª@\x0015\x0004\x0000\x0008iÑZ3Ïyjjlu±®\x001b\x0000¨*\x0000PU\x0000`Û6U¥¤ë­\x0011ÖQNivNç³oÿø'ÿð÷ÿèÃ\x000f>ûê+Ó´3¶òøôìû7ßûÏû\x001fýîþÑùx\x0002\x0005\x0004(T\x0011\x0000¨\x0002
!¡ªôÞO'©aÍÕ~'£Ø8ìvgRZ>=IËÝdjMQCU[ô ÅyY­ë°ºÚ6=ÍåÅ~Ø9ìwÖuuØ\x001flJÐû¤õYµ.}¯ïoLóÖ:\x001a%è»K»Ãµù°w>\x0007@\x0015UT¡¢ \x0000\x0000\x0001\x0005$vû½\x00177ÙÆfY­Ê¢LiF¨\x0016\x0017W¾þåùæ\x0017¿ryyChÓäðâ3m9{<>[ÎÛb?]jÞ»Ö\x001a Ò$( 
PT)\x0002Ä¨²®«±nT0Fë2\x001dØ]YMî\x001eî\x001dÆpØu«\x000b»+¿ù¿ô«ßüK|óÁùü:¢<?>`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=¹~ü`/oÏ~r\x0001"@HH\x0000C P¬²Z*"¬R\x0014!Q*\x0015¨\x0014EB\x0010\x0011¨$\x0002*$\x00042Ã`f\x0004	"\x0002\x0000@¨\x0014P©T*\x0005!\x000cQ\x0000\x0000\x0002\x0000@%T\x0014\x0005¨T²\x0000\x0008\x0012\x0000`Ù\x0000 ÖZ´¥YX*\x0008\x0005\x0008\x0000\x0000@¥\x0002\x0000\x0002\x0005(\x0000P9	0@\x0018\x0000	 \x0014!YÇR©L\x0004A\x0000¨T\x0000\x0004B\x0001\x0001\x0000¢R´hK¥"\x0008\x0008¨\x0000bF\x0012Âûc9ÊÂ\x000c\x001aT\x0014¢"$\x0001\x0002l¨\x0011¶ÉDH\x000eì3^ßÜøÉg¯}3ãÅùä»Óæázu\x001c}Û<Èyß]Cr\x0018¶ÝóÓ£Ë~xÚOÎ·\x001f?ù/o~ìWo¿óÛþ¿úá÷æÍ<;ßüÅW?øÿæÏýÁÃ°==ü`ÛÎ^ùÛÖó£ççG[Ê T\x0006\x0003 E%Ô²ÖR	</p><p>)HQcI\x0001 ¤Ò\x0004J\x0005 ©ÌBÌ1¶\x0019P©Ì\x000c3¤¨\x0000\x0008\x0008#P\x0001Xe+J-Ù\x0002\x0000*0\x0000\x0000\x0010\x0000\x0000a \x0012\x0000H¦A4\x0000 \x0002fÀ\x0000\x0014\x0003$k-(À0Â\x0018\x0000T\x0000 \x0002\x0000\x0000\x0002\x0014 \x001a\x0008l\x0006\x0003Ì0 \x0000\x0000f\x0018 ²ÖT*V*IR©</p><p>	\x0002\x0018B\x0000 R\x0000J-J!*¤\x0002\x0000\x0015P\x0002y^Ë·OWK\x0006§\x0019\x0015\x00182QYå(«\x001c¥R\x0014P\x0019ÆpÚ6¿õê»ÓÉ5Ù(k\x001dVËµ<ÎfqÓr\x001eöÓa\x001dçò|º¸»¹¸{üäo>ÿ_üø\x000f¼zøÖ?½ùÚÿø'w^½¾ñÕ§G\x001f¾ýÖ§÷\x001f]¯OÞýæ+Û~ãúôìáñÑÃã³\x001f3\x00061fÆÌ\x0019\x000c\x0000`\x0004P\x0014Q)V)\x0008@\x0002\x0000@V\x0000\x0008¡¨T*\x0000\x0000!Ì\x0019\x0000\x0000`$)È`\x0006\x0000\x0013E\x0001@\x0001\x0015R!\x0015\x0000\x0000J¥R\x0001"*\x0000PI R\x0001\x0008\x0000\x0002@\x0014 \x0000\x0014k\x001d\x0014!Ê*µÔRK\x0005 \x0002\x0000\x0000\x0000I\x0005 \x0000\x0000\x0004`\x0003"	I\x0001B\x0011\x0013c-¢JÅJ¥R©h©$@ \x0004\x0000\x0019\x0000$©$B*\x0002 RJPàáÈûër]\x001ck!\x001c¥¢Ì\x0000\x0003"¨\x001c\x0005H\x0008Eh\x0019×·\x0017÷ëðþý'÷þ£ÇÓ¶Yë°ã(cÛí²·fÜÏÞ==«emËËW¾¼»ñòùÉ_ö»ÞúÖë¾w{söÓßùÂOûo>~òÕ×_ûêïþÖùÅ[×ëG¿þåòwÿù?ø»o¾ñÝóaf3Ã\x000c3cfÀ\x000c\x0000¢\x0002\x000bIH\x00040HR\x0014U*\x0005\x0004\x0005\x0012\x0013\x0008"I*J\x0005 RY+03\x0000 RY\x0001J%Ì\x0001) P©@Q\x0014</p><p>\x0000\x0000T*\x0000 (\x0000 ¢@\x0005\x0000\x0002@ \x0001\x0014¨ Z\x0000F\x0004(b\x0002*k-\x0000\x0000\x0010\x0000\x000c\x0000\x0015 \x0000 @\x0000\x0000\x0008\x0000H\x0018\x0000ke­T@	`\x0019Ð$©\x0010P@$¢\x0002P</p><p>\x0008¨$P	B©\x0000@\x0005\x0014wO÷ÏkãÑrjlÛ\x0008¢T\x0000\x0006	T\x000eÁ>\x0003bq9|Þá_ÿÏÿ÷o>óð/ÿÿú'_ëaÃeÛ¬øh¼Ú6çµ<Û¼<|º^íÛf3Ö~òæ³ÏýüñÙû/¿ðo?|ïï\x001f\x001e­ÓåÖÛßúÒ¿ûËÿèãwïüêÛïü£9»9óþï9üúÕ'7fÆ\x0018\x00003\x00034@EY\x0000\x000c\x0000\x00080\x0012B</p><p>\x0011Ê</p><p>¢$\x001ak-µTVÙ\x0000\x0000JeÍ\x0018</p><p>\x0000\x0010T*\x0010</p><p>\x0003@¨\x0000Ì\x000cX+d­eÛv\x0000\x000003*\x0015\x0018Ã\x0000\x0002 \x0019\x0014\x0000¢ P1\x0004Å\x000c A$3\x0000\x0000\x0000\x0011Û\x000c\x0000C¥aÛ\x00190\x0000\x0002\x0000\x0015\x0000(\x0006\x0000\x0010\x0008\x0003\x0000\x000c\x0000'\x0000\x0000\x0000\x0002\x0000	\x0004@A@À\x0000,¢¢\x0000("\x0001\x0000\x0000\x0008 T²Ô¨\x0004%I\x0000\x0015\x0003¿{¼út\x001cãI¾{~²oËÍ\x0000p1Ûx^V\x0002\x000cV1£±\x000f\x0010\x0018p\x00136ãóÏßúüóW¾ýðàÏó|ñ¹/Oc­Ãét\x0012®ñ8ûÉy-Ç¶¹1k9íf3··~üÅçþôzõ×ÛÏ}º¸®åætvÞ/>||p<nNòÿò×¾øì¥Û\x0017\x0017\x000f÷¯ýæ8±c\x0006$\x0000\x0001\x0001*</p><p>(\x0000\x0001\x0006ÂP	\x0000\x0000PDQT*A1\x0003*\x0004!(3£\x0002\x0003(</p><p>\x0000\x0000\x0001`fT`Û6E¬Ú\x0001ÀÌ¨@ef@\x0002@DÒJû\x0018\x0000(DÃ \x0012Ñ6\x0000\x0002©1C\x0018@ÅÀ¶ó¾J±ÖRË~\x00023cfìÛ¦\x0000¨\x0000@ \x0019A!\x000c$0QÌpªÌ\x000c	 \x0000\x0000$\x0011</p><p>¡°0Tf\x0006T*\x0000À\x0000Q\x0001\x0000\x0000Ê*3hQ*µT\x0014F \x0005\x00143<¬å?~|ò¸Çµ¼?\x000e:<<=ùÂk7§\x0013PVáv?Ùæðt½º®À\x0002\x000c\x00063c\x0000\x0000\x0000\x000b«\n.þø_ý\x000bÿðÕw>ì»¿ýðÉ\x0017o_\x0015qÞXk<oóZ\x0006_Ü^Ü¯«¯íÊ¶óýßúÑgvi\x001bÏÇr¹¸}ýÆéròêæÖo^ysç|ËÇÓ_\o<nÜì\x0014\x0001*\x0010*À(\x0012@\x0000\x0010 ¡4(0HH\x0008IE\x0011\x0004 R©\x0000\x0014µ4£\x0002PQ1c¤\x0002\x0004`@\x0000mÛÌp\x001c#\x0019Ã°m\x0001\x0000\x00001\x000c\x0000±0e\x000c\x0002a \x0018\x0018¡b\x0018\x0003I\x00180*3\x0003\x0000\x00063cb-\x000c03fÆ\x000c\x0001$\x0003Â\x0000\x00001B\x0002\x0000\x0002\x0000Hq\x0002\x0000 \x001a\x000c¡@\x0000¨$,\x0015\x0016\x0006\x0000\x0018\x0004ÔR\x0011"¤B 23fF\x0005¨TZ</p><p>(Z²0j\x0010FÅ >\x001cùöÈu-×«ã°,O-ÿþ\x0007?{óÆÞrt¸®e?\x000ew77nO'\x001f}º^\x001d+°Ï0\x0003c\x0000\x0000ÅÝøÉW¾üá_Æ»ëÕûcy¹µÓ¶Ûg\x001c-eqîpl»¿}xô|Y.§Í`öÓÝ\x0017/ï]§u0¼|ûÆöbó¸\x000esbö«¹¹÷ëýïÝyË¤²ÊV ²¶MQ©ÊQ`Ä\x0000\x000cH¶	©\x0001\x0002B(RYe+\x0015Æ\x0018f\x0010\x0000\x0000\x00193T\x0000*3\x0003*a¢\x0002\x0000@0\x0008P\x0001\x0013\x0006\x0019Ì\x000cQ\x0001J\x0005 \x0011\x0000\x0000 h\x0014Di\x0000\x0018\x0000T\x000c\x00000\x0002\x0012fÆZ§§ÃÌ(àXËõ8\x000c¶\x0019aßv\x0004@\x0001\x0008@\x0002TÆ\x0000\x0002</p><p>\x0012\x0018p</p><p>\x0008¥Á</p><p>0`@\x0000¦ÁP\x0002ÌPÀ\x0018	(\x0011¢\x0004\x0004\x0000¨@\x0005ÔQ©%IB(\x0008</p><p>\x0014f|<ÇÙ<áùzõ|\x001c\x001e-wûÉw>>=yy¾H*«åñéÙÃó×÷÷ÞÜÜ¸;|¸^=\\x000fGÙ\x0002\x000ca`Ø0Æ*wç³?~ýÒßûÇòíÓÕéöìÝ`äÀuÛ\ÖÕy²¶ÝãÊý¶Ù±ðÝÊ÷Æãõ0ÆËW¯½z}o=>XûíæâÓå¯6"YXeU6)IHVY¥\x0002"H*\x0002Ê\x000c\x0000</p><p>!R)*\x0006Ã6c\x000c\x0000\x0000Øgóúå+Çm\x0006T\x0000 Ò\x0004\x0006@ @\x0005\x0000 "\x000cÂ` k-3£23*k-3\x0003\x0000\x0000@\x0000$5\x000cE\x0008\x0013\x0006A@\x0001\x0015\x0000\x0000\x0019Ê\x000cÇZcÙf¤r\x001cKeÛ\x0006¬@@Â \x0000@\x0002\x0000@\x0001\x0000'\x0000 0%	\x0000\x0000`0</p><p>\x0000ÌPa0 B*A1\x0003</p><p>\x0000\x0000@R¤R\x0011EE!\x001a\x0010 b\x0010\x001f\x001c3Ö¶»®åá¸ú´®Öfßw¿zÿÁýÛ³\x0000«ÀÃó÷ß>x}wïõý½77\x0017·§åÃõêáz8ÊÙØ°
'@Æ>c\x0000?}yçí7ßùø|õýó³}ÜÎ²ð¼°Ï¸qZË}óíóÕêÆi\x001b{Yëðþ8|Øn=\\x0017¸½}áí·Î^ßß:Îw~ñ¸{\Ùv\x0018\x000cQ´bK\x0008Í¨T@QV\x0019$¢\x0012\x0000*&$\x000c*\x0019PI*3Tj!\x0000çóÙé´\x0003\x0000¨Ì¶yýê3Ï×«u\x001c*\x0000\x0003(Ä6\x0003\x0000\x0008\x0000\x0000T\x0000*3\x0018\x0000B\x0005 RYkÙ÷
\x0003\x0000\x0000\x0000\x0002\x0018\x0006\x0001 \x001130 L1\x0003D23\x0004\x0008\x0003\x0004Pãp\x000c3£\x0002k-¤\x0006L\x0003\x0000\x0000\x0002\x0004\x0010\x0006\x0000A\x0018\x00000*3ã\x0004\x0000\x0001\x0000fH\x0000 \x000cÆP\x0014F\x0002\x0000@Ì¦ÐB \x0004\x0000*\x0000\x0015HT²Ô¦\x0002$	!@A4Â#\x0007¶ÓIx¾>{Z÷×¼8_<\x001cyÿôäÕÍ13fÆi?y:\x001eýí»oýÝû\x001f|vïó»{oÎgwûÉ\x000fÏWOkÙÊeF\x001bkg\x000cûËÙïßÝø÷OÏ>\\x000fwÏöòVNFeßÆÓâ\x0011Ór;ùôôäùîÎ¾í¦ÃóõêÀóvòñ8ËÍw¯ÜÆíÍÿÒ\x000bß\x001dÙ\x0000\x0008 @\x0000¥RY-U*J3$É\x0018@AX2\x000cF\x0014¨TVI\x0012"¶ÙÜß¿p>íf\x0006\x0000\x0000Ì¶Ù¶Íq½ªÌ\x000c\x0008JÌ\x0000\x0000\x000c\x0000\x0000\x0002\x0014`\x00100\x0006@efTj©Í\x000c\x0000\x0000Â\x0010\x0006\x0010\x0000\x0010 \x0002fL!	T\x000cd\x000c\x00103£²+3Æd­hÌd³\x0019\x0003 \x0000\x0000\x0008¢a\x0000"T LØ '\x0000\x0000\x0001\x0005@\x0012a\x0008\x0011\x0008\x000003,µ"\x0000 \x0004\x0000\x0000\x0000P R4Q*\x0015¡\x0004A  \x000f+`ßlç³ç§ë³Ç\x000e_}|ïn?»Ùwÿør¶a±f÷ÝË[§}óÝã_|û¿~÷­W7·ÞÜÞyq¾qÞ7Åk}\x0006\x001c±\x000fÛÁï¾¸ó¿úÖÃõð°o¶ë!¼Ø67ûØÚ,¼?\x000e39ááùÉ»çg·Ûx*Û¶Y6ñþz\x0010çËÅëW¯mï>ù°ßùÕÃ	cf33\x00180(\x0000P©ÔRY-µ\x0019B</p><p>É\x0018\x000cf\x0018@Q©\x0014Å\x0014\x0010	Ì6.Ó¾c\x0000@¬µTÌ\x0000\x0000\x0000R\x0018fÆ\x0000 \x0002\x0000\x0000\x0000\x0010ZafÌ6 \x0002\x0000ÇZN'\x0000\x0000*3\x0003\x0000\x0000</p><p>B*3\x0003\x0000\x0004@C\x0005\x0000 \x0012L\x0006ãX¶\x0019\x0001 ÃØg,YÛÉ 	\x0000A\x0010
\x00083\x0002\x0004\x0008§</p><p>\x0001b\x0005J!\x0004l3 \x0010\x00023£\x0002P	"Q*</p><p>@\x0005*3\x0003\x0000\x000cB²$\x0004*\x0000%Pd\x001cåý±LaÜÞÜÚ÷\x000f\x001f<·dùêÃ;ÇÓ¾xáåí}Æv:YeÛ6Û¶¹ì'/¯Ï~xzôÍ§þáã\x0007Û¶{y¹øñÍûÓ~r±ÏØg\x000c¦4Ë¶o>¿¿ó²¯½zööròt\x001c°ía3³a9¯\x001e÷1Û8O~õé\x001fOÆíåÆl¯¯Þ_\x000f«N'¯ß¼ññáX·eÛÆÌa6f \x000c\x0003$µ´¢¥¢\x0000	\x0001\x0000Ê6Ã13*!T\x0008\x0001Q$\x0000c\x000cÈ\x0018f¬µ"\x0019\x0003\x0000 \x000cHÆ\x0018\x0004P\x0000 \x0001\x0012\x000c\x0006¨\x00013\x0003`f@E\x0001Â\x0000\x0000\x0000ÂÄAa Ëùìr>»\x001eWOÏ!\x0001 Ì0ÛØ¶ÍZm3\x0000XÍZKû23@\x0010\x0000\x0000\x00010\x0000\x0000IÆà4Fb\x0000\x0008\x0004\x0000Æ \x0006Ãl£2\x001dØ	Û¨\x0000\x0000´RQ*\x0001\x0018\x0002\x0015\x0000¨\x0008HjYmK¥¨@¥Ò\x000cP H®åß½ûÞ~\ÞÞÞ:NîoïÌÃ\x0007_|¯uuÙ6ï>ýà¯¾úö»?sÞwf\x001ce}ßíûî|¾xu{ç·Öòx\}¸>{Zw¼~òòrvw:¹ì'7ûnß6§aÁîþîÆO^ÜøG×»[Íx<ZÖÚ\x001cåYË\x00036×ûîÓq¸â²\x000fxuÚ½~öîz8Ê¶íî^½ñÍ7÷¾ýÈÌ\x00193Í\x00183\x0003\x0008IÈ4LjQ*²dC¥L#(T4\x000c\x0000$&\x0006%2\x0006 @A</p><p>\x0019\x0000\x0000P\x000c\x0006P\x0001\x0003\x0002\x0005\x0004\x0001a0Ã\x001803\x0000 \x0000\x0000\x0001\x0000\x00000!\x0008$c\x00000.çÓiS\x0019*\x0000\x0019H\x0018l3ö\x0019ÏÏ¶\x0019aPË*mÆõ8Ï\x0017³
 \x0002\x0012\x0000\x0018\x0004\x0010 \x0019À `\x0000'\x0018(\x0000 \x0000$(clÛ¬²YÆÐÆÊÌ</p><p>©\x0010\x0018	\x0004\x0012\x0000</p><p>\x0010J%P! \x0000T\x0000V9¶Í_|÷µoÞ}ïÍéäo>þàz<{|zðq\x001döòï\x001fé÷>ûÌg¯^3cf,ÀyßU\x0016*÷å3¬ëÕóq536(ÇÊ>¹b0ÃåtòÏ~ö;^¿ÿèclÃµ82e­å4Z¦qÞÆÝéäæº<®åÕùdN~üâÎû\x001f>úþz8V.ûæüâ¯;{j\x001931\x0000\x0002\x0005\x0011&D\x001b¡\x0010\x0000\x0005`\x0010`PÉH0\x0003\x0004"(\x0004\x0014ÉÀ\x000c\x0000\x0000\x0008\x0010\x0006\x0000\x0000PÌ\x0000\x0000P\x0001\x0000\x0008\x0003\x0000 \x000c\x0018ÃP\x0001¨Ì\x0002\x0000\x0000\x0000\x0000@\x0018		00¸OfX+lömsuÊÌ(Âh±mããÇ*3\x0003\x0000*fT¾üìsÛ¶\x0011Ð `\x0000!\x0000Â\x0000\x0002Jef\x00143\x0001(\x0000\x0000\x00000Ù8m;Hj1cB\x001b3\x0012\x0019­(J¥\x0000HD\x0005\x0000\x0000\x0012HB¥\x0016¥ ¤P\x001a \x0000¨ìøòrö\x0007o?scüê«ßøþ«¯<|ó5¶ë³:\x001c-ïNÿoNþÛùßØædfl3\x0006ÛU5©ÀjÜ7Ï\x00060 Ê¾Á\x0006òêöÆ?¿½ñ´òîñÉ/~øèy-Åeßìå\x001aGÜì»+[¹Î¸ß7Çåì²ñÝóáz,·§§ó½_?
a¨Ì$ID%\x0014ÉD`ÑP Xå8\x000ek6­\x0000\x0000\x0001\x0001\x0000P	\x0001\x0008@2Ô!a\x0000À`\x000003\x0000\x0000\x0000 af\x0000\x000c\x0000\x0006a\x0010@ÁÌ0L¬µQ\x0019Ç:1\x0003\x0018\x0000\x0008\x0000\x0010\x0006@\x0000\x0008\x00030N'3\x0003`f\x000c\x0002\x0000\x0001(\x001a\x000673²Ö²!\x0004mÛ½yõÂ¾\x0004\x0008h\x00040\x0000\x0011\x0006\x0002J\x0000 Å	 0\x0000\x0000\x0008\x0000cìûÎ\x0000\x000b#[Ë\x000cÓ`\x0004¨(\x0015A L$P©\x0000TD\x0002J¥\x0016E!1\x0008\x0008Øðzx{sqÿåýñ\x0017_úøGäã§OÖõj­ÃÓóÕûO¾úôÞ/>}ô\x0007ß}ç§ÿ\x0019µRKUÂ6c!®kiØg\x001ce7¶mì1pÙÆ\x0017·7¾þøÉ/\x001f\x001f]öÝÓ¶±âáz¸Ý773.Øìå²\x000eß<=yZË69_<¯¬YcÛ6\x0015\x00166DQ\x000c\x0003\x0000AJ-ÏÏO\x00177ÙÆ6cÂ\x0004 !$C$É`D\x0001bB\x0018Ûór\x001c\x0007HÆ\x00000\x0014`0cfÀ\x000c\x0015\x0006$\x001903 \x00001c\x0002\x0000Â\x0000Û\x0010ZYk\x0019P\x0011§}\x0007 \x0001\x0000\x0000\x000003*ÊÌ\x0000\x00000\x0012*3\x0003\x0000*3\x0003àþîÖ>#Ë¾mf`\x0003mÆýý½·o^\x0002AH\x0006\x0000\x0008\x0010\x00000B\x0000\x0000\x0013\x0000\x0000a@¨À\x0000`&§}3Æ*\x0006Æ\x001aF6ÆØ\x0000©($\x0010\x0008P\x0001\x0000DIJ¥ ¢BÂ\x0016\x0004\x0014(\x0006§3Nûæ´í^^.¼z\x001c+ß=>Z\x000f\x001f½y|ëôþÿÍ;?zõÚíå¬\x0019\x001bë:¬2F²ÍØÁ*û`Æ6£(\x0018kØÊB\x0018Ù\x001fÝ^üïÞù0W¯ÎËÍûmSyZËi¸Ù7#·òé8|x|p\üæ\x0013®\x00073înnìÛh\x001d(¶m¬cYÃ²oJ¥"¶mh\x0003k\x001d>=<Z×g/oo÷[§óÙZËõ¸:\x0002\x0018cA\x0002B(</p><p>ÀíùÆËû{Çºúðñ\x0013\x0010\x0006\x00080af\x000c`\x0006`À\x000cÁÌ\x0000\x0018\x0010\x0018#1\x00080\x0000c\x0006Æ\x000c,OO\x0008Ìýt\x000203\x0018\x000c\x0002\x0000\x0000\x0003\x0001\x0000 \x000c</p><p>Ì\x0000\x0000P\x0001\x0000ÊÂýÝ?ùùï[ëp:öÝl\x001bÆ¶möms>_¼¸¿\x0007	h\x0000\x000c\x001a@\x0000\x0008\x0000\x0010\x0000\x0000\x0000'\x00080`\x0000À\x0000 q{sv:m§\x0003\x00040\x001c\x0018l-c³Je$\x0010\x0001\x0000P\x0001\x0008BQ*$ILK3\x0010\x0000iãê|>Ë²0¸®åù8ÔòùåÆÓÅofó¯¾ò¯¿ñ~ëÇ¶	£Élc[¬²Mö\x0019±â(Ó£\x0001ûFP\x0016\x0016¬lÃ\x001dÝ^¼<íþê÷>^.\x0006/·\x001bgËó±¬µ¼¼mòx\}ûñ_}xof<[>]¯àærázõðþ½m6³mfÆ6ãtrNö}÷¼ïÎçÓ¾«À¶óÅõrãùüìr>ùÑëW~ôÙ[w·÷±Öòðøèz,m!JFYÌ¶!k-VUÖÊ¶\x0005¶\x0019·7\x0017·7\x0017×ëxØ\x001eT\x0000\x0000À\x00183Ì\x000c\x0000af\x0004\x0000\x0000\x00190\x0003\x0003\x0008\x000cf\x0018À\x000c\x0019Û6*ÀRÙ¶}Û1\x0019\x0000\x0000`fÌ0\x0000\x0019\x0000°</p><p>T (\x0000Å\x000c\x0000ÂPÙ÷üä§`\x0019</p><p>Â\x00181</p><p>@\x0000F\x0000E\x0000@\x0018\x0000\x0000\x0001\x00008\x0001@PÌ\x0000\x0011@1À¶mnn.Îûæ±+\x0006$\x00005l¢(¡"@@T*\x0000\x0000AI*J%L\x0000\x0011\x0000Á§O\x000fçgË\x0019Æh\x0006ìÛf=?ùðôèèê|{ñ\x0017_í'¯_zóâ^ÆÌ\x0018ÌÅ²\x0004ö\x0019ÀÂfQ\Wf`\x000c\x0002·ÝÏ_¿ô7\x001e¼½¹qw:{|¾z^ÏÖrmùt½øóÙãÙ?|ÿÎo>}°fóæîÎÇçgp{së¿úãûðá½ÁÀ\x0019ÛmÛÌmÛ¡ÀÌ8íg§óÉÍåÆë¯¼}óÆårkÛ6OÏÏjayz>äÿ'\x0008O~vÝ÷\x0003/ïúþîûyÞw5{íîc\x001f[JPMT()&Dj !\x0006\x000c\x0010\x000c\x0010Iþ¨\x000c"1\x0004&0"R\x0004C\x0002¥J\x0006\x0011\x0015\x0004S¶c»íÓxï³»µ÷ZëmûþäºY\x000b#Ìµm
è<\x000cöm·¶ÍÚ6c¬µlk¹ì»Ë¾YkYks½\\x001cÇa­e­,5ãÄ1ÃÌaf¬5`flk©±Ö23\x0006f\x0000lÛr'\x0000\x0019Û¶ÀaÆYË¶í\x0008©Ì,3\x0003\x0000\x0008\x0000\x0000Ì\x000cÂ\x0000\x0000\x0000\x00008Ï\x0013\x0000@\x0000\x0000\x0000 À\x0010\x0015a¢\x0011\x0008iÆ\x0004	\x0003\x0018\x0014`\x0002\x0000`(A@\x0011@</p><p>Ø\x0001 \x0002I\x0002\x0010@!3cß6kb\x0004 \x0018\x0004sÚ:å\x0004JC`\x0000\x0000H*$©SEQ</p><p>b¨\x0000 \x0019OÏOÞ?ç¥±m\x0017ûæávóîéÉwÏþúá¶\x0017ÛæÇ¯^ùÕÃ?úå¯ü+¿÷»Öu\x00003Ô82¸lcpbf	Ç\x0019rÆu_\x0006ËXÃ\x0018á(¿ñòÞï¿~Å¶»®ñáÃ§\x000f\x001e:=§_¼ã\x000f\x001f¼Úo\x001f>øá8=â7NÞ>=\x000b×ËÅßû»ÏZ\x0001\x000c\x0002\x0004\x0018\x0004\x0000`fÌµ6ýb¿\¬Yó°ÖØ÷åÕ{çyÊ\x0018Ã\x000c`\x0000\x000cf1\x000c\x000cØÖfß7Û¶\x0019ö}3Ã`mË\x0000\x0006Sì\x001br\x001cËZËZË1+°ï;0¬5\x0018Û¶9ÏS1ÃZ\x0005\x0000fØ¶¥²Ö2C\x0001\x0000\x0005\x0000\x0000\x0010\x0006\x0001\x0000\x0000\x0000¨\x0000\x0000\x0000Ô©23 \x0002\x0001\x0005\x0000Ò0`@\x0000	\x0002\x001a\x0006	#0C\x0001`H\x0018\x0010\x0002\x0008\x0003ì\x000003Â\x0000\x0008(\x0001Â\x0000 \x0002\x0003\x0006a$\x0000IÁi\x0000\x0010\x0002ÊÌ¨\x0008\x0010P©(E R\x0001¨\x0000ÁurÞÍZ¦lÃÛÇ\x0007ÿ¿ï¾õöùÑuß½¾Üùüî\x0005ÆæÉ¯\x001eÞûã/ßú½Ï>õãO?e5cpb\x0004Bq5cÍ`</p><p>ÌP\Ö\x0019KÎ3pànÛýæý?÷`9yzôÝãwÇÍóyz÷OOÞ\/nxwrwwï½ñÝã³Î¬µ¼zõÊýÝ=\x0006\x0000T\x000c\x0002\x0000\x0008\x0003\x0000fÆÌ\x0019\x0015p¹º\.H\x0005´A\x00003c$T\x0018\x0010ÆXk\x0019À`_ËÊ6cÖ2HæÌ\x001aó43fÆZcfLì³0`bÛ\x0006	ÌZS\x0005\x0000fFe-\x0018&\x0005\x0000Ìe\x0002\x00000\x0000\x0001\x0000\x0000\x0000\x0000Çyz||r\x000fÎóT\x0001\x0000\x0000\x0008`\x0006\x0008C \x0000\x0003\x0010\x0006ÆH\x00020\x0000\x0018\x0014\x0006\x0000\x0000H\x0000\x0008\x0003`\x0007\x0002\x0015¢!\x0000\x0000`\x000c\x0000F"`À fT PH%4\x0001\x0004 \x0002\x0000Pä,dH\x0012 \x0005	\x0000»ÅíéÁ»ã\x0010î_½ò\x0017?¼õ³\x001fÞz}¹øñåêóû\x0017.k÷t\x001cþê«/}pºûÑOüá\x0017_ù×î_xñò\x00053ÌØ\x0010ÆÅy&QNÖbf,ã8i gÀ\x000cÅlËo½~éÏß¾õx»q{ötóôp»ùpfÝmneÍòáäËÕ±Æ·ÏÏNkÆ\x0011Û¶+f\x0000¨Ì\x000c(\x0008\x0000\x0000a</p><p>¬µÀ\x000c&\x0002\x0018cTH\x0005f¡NÎ\x0014k\x00163fNçy8af\x00043\x0006&b\x0006³Laf13\x0012Æ2\x0000ÂL\x0018³"\x000c\x0004\x0000\x0000f 3\x0003\x0019\x0000\x0008\x000b\x0014\x0000\x000003f\x0001\x0000\x0000\x0000\x0000 ²Ö8ÏÓÃÓ\x0007wwW³\x0013@ef\x0000\x00143\x0000a\x000cH\x0006\x0000\x0004\x00001\x0013\x0000\x0000¥\x0019\x0013`\x0000\x0001a"\x0001\x0002@\x0018d\x0007\x0000\x0002!\x0004\x0000\x0004 \x0002!L¡aP\x0012\x0000\x00030 \x0010\x0000\x0000\x0000	Q*¤BB!H\x0001D0Àäã}óöùæË\x001f¾6\x001fÞùøøÜÏ?|ðp»¹ßw¿~xðåÃ\x0007?}ñÚ¯¿ëË\x000f>ùü3¯×Å_üÉø|ãïüÁ\x001fØ.\x0017Û¶\x0019tKe­q9b\x0004ÏÓÌX1k(Oçi
3,C¬\x0019G¼¸ì>ZãûÛ³­ìkYçÈHÎÓÛ#ÿâÝ¿p·üE§m.Þ>ß\x001cçi¥\x000e\x0015(\x0000 \x0002\x0000\x0000\x0000\x0008\x0000aP\x0000`P\x0002\x0008£RéÌq\x001e*kmÖÚÁq\x001eº¡DQÌ\x0010Ä@\x0012Æ`\x00061(\x0000\x0000C\x0018`\x0004\x0000\x0001\x0001ÅL\x0008\x0000\x0019\x0005@\x0018@\x0000\x0008\x0003`fT\x0000 Xk¹Ý\x000eï>¼³Í¦\x0002\x0000@\x0001\x0000\x0004X*03\x0000\x0003ÈD\x0010\x0001\x0002a\x0000	`\x0000"\x0008\x0000U)Q\x0000\x0000@\x0008\x0000	©$IhH(I (\x0000@B¥\x0002¤\x0002P©T\x0014AHNu"P\x0010NÊOîûýê»g¾yÿÁ_½}ëÇ\x0007÷·g¿øá­³|ÿôä/ßýàÕ×^ß¿p÷kùÃ/¾ôÍ»wÎóp§`-Û,3#4T\x0014±ÍrYËeÛlkÙÖ&\f¬\x0019áVË
Öò;o^Û;¬\x0019û\x001aûÚ\·Ý«ýâ²6§ñ«ç\x000fmÛ´6ß>\x001fnGÖZ\x0002\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0008\x0000h\x0004\x0000 pvz~~òøøàééÑíöì8nãpÜnãæùvóüüì8\x000fg§ÎC\x0005À\x0000\x0015å<\x000eçyH\x0002\x0011Á@A\x0000\x0000\x0000\x0008\x0011\x0015\x0001$\x0010\x0002\x0000\x0000\x000000</p><p>\x0010 \x0004\x0000\x0000f °­ÍóóÍí8</p><p>\x0000\x0001¨\x0000\x0008</p><p>BH\x0000B 	\x0000\x0018\x0012\x0000\x0004h\x0000\x0010\x0000²Ã\x000c\x0000 \x0001\x0000À\x0000D%LLi\x0001f$Ó I\x0005\x0000P\x0000\x0001\x0000\x0010 *JE\x0014"\x0000ê\x0004\x0005!5>ÞÇ¿ùÙ\x001b_>Þ;}èæÓ\x0017wî¶ÝW\x001fÞ¹n\x0017?¹åO¿þJk\x001ckó\x001cçéÕìéÝ{ÿÓÏþÂ¿ñ·þEû,fl3öm9\x001bg§Õ¸9\x001dçiëZöµ(\x0006Í¸5Ã°\x000c8q¾yã»\x001f¾÷å\x000fï\×æý¶µ°XcÖòÕ\Üf÷éåêz¹x>z<n^¯\x000b¥N3\x000b\x0000\x0000\x0000\x0000\x0000\x0000\x0000T\x0000\x0008 \x0004\x0010\x0006\x0004*·Û³§§G\x0003`ì\x0017Z8ÇZÃ:\x0015P\x0019K¥Nuzzzr»=;Ãív
ã<O3cÍX³\x0004b\x0006</p><p>\x0010\x0006@\x0005</p><p>Ã \x000c</p><p>\x0005\x00000\x0000\x0003Ô\x0001 \x0019\x0003\x0000f\x0006@1\x0003±­A\x0018\x0000\x0019\x0000\x0000Â\x0000F\x0002\x0004\x0018@Æ X\x0003\x0002\x0014\x0000\x0001@\x0008\x0001\x0000@\x0000v\x0000\x0006\x0000P\x0001!\x0000HEf(\x0001fF2R\x0019\x0003 THE\x0001¨@@ÈtRrJ\x0008!\x0015\x0000\x0005@1ñ\x000fôÊÿóç_ñãøêí×~öÃw^~ü©û×^­åíÃ\x000fOO~òÑk¶ÝyÎµüäã7~õôàÏ¿ùÊï~ý#¿óã\x001f³ÆlmÍ¨ì+OÇa°­q35ã»\x0019kX²Í"fåw>ýÔWïÞùþùæñ<­µÙ×æ²ï.×;ö\x0017×«O_¼ðÉ¾éáæáù\x0011*\x0000\x0000\x0000\x0000\x0000\x0015\x0000\x0000\x0000H\x0002\x0010\x0008@\x0004T\x0000`fìûÅÌçç'ÇqYËqÜ·ÃZ9Ãyfm.{9=?<úðá­ï¿ÿÖÃã\x0007clû\x000b¯^î\x0014²f³¶å²mmÛ¬µÌ\x000c\x0000Â¨Ì\x000c</p><p>\x0000!\x000c\x0001T\x0000 \x0002\x0000\x0000\x0000@Á`\x0000!\x000c\x0019@`\x0006\x0000a\x0000\x0000\x0000\x0005A2\x00000\x00141\x0000Ä\x0018	\x0006\x0001BA	\x0000@²\x0003C\x0018\x0000@\x0000\x0010\x000230ÀDd $a\x0006\x0010*3\x0003HSRI\x0008¤R\x0000@\x0000*É_Þù\x0007¿ÿ7|9»ó1çáééÉO®÷óôõû÷~úÑ\x001b¿ñÑÇÞ=?{>\x000e¿|å\x000fï\_¿òáÌ\x001fþõ\x0017>ÿè#¯×r`
ÛZf\x0006ÃÊ\x0005Çyz>N·óTmÆZËà\x0018¶Ó\x0018ãÁ6ãÓW¯ýèõ+¿üò+//\x0017×ËÅ¾_í«ËåêrÙ]¶Ý¾\x0016ÆÚÆÛaf\x000cÎ²\x0001\x0000\x0000*\x0000\x0000\x0000\x0000\x0000 \x0004\x0008B hÌ\x0000	ÀÌ¸\.ö}WYÛæ<NÛ¶[kÃé<NdÖ2Få<O3ãùöÁ»÷_{x|ë<No>þMlnçÍÖn$£8Î!ÖZ\x0000\x0000</p><p>¡R\x0001  @1\x0003\x0000 0\x0008\x0003*\x0000\x0000\x0000#\x0004\x0008\x0000a\x0019`f\x0000\x0018\x0000\x0000\x0008\x0003\x000c\x0000@\x00013TÆ\x0010\x0006ÂH \x0010F\x0018!\x0000\x0005\x0004\x0010\x0004D\x0003À\x000e</p><p>0\x0006 \x0000\x0000PÀZ\x00140\x0018\x00004T \x00100\x0002@@JE	 JE)\x0004\x0010 \x0005)@\x0001CrÙw[ËÇ¯_{õúµã8<\x001d7·O?1ksËÅy\x001e¾y~ôzßÝï\x001fù~]|ñÕ×þù¯¿ò·ë¢Á f-\x0010ö5Ö,ÜTÏÌyºlËcã~-Û!f\x0018cÍøÝO>õ³·?¸î\x0017×ËÅºÜ¹\.î®\x0017/¯Wm·fìkÙ\=Ün`ft\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0019</p><p>$\x000c¨\x0010¨ÀÌ\x00000cÍb\x001bk-3ã²]Ù/`fTnÇÍ²lûæ£×yqÿÚíöììtÙï==?yx|vw½Ú·ÍÌ\x00193KefYk\x0014</p><p>\x0000\x0000!@ Tf\x0006\x0000TÌÊ\x000cP!3cfT\x00000H\x0001\x00190\x0000C\x0000À\x000c\x0000\x0000\x0001\x0006\x0004\x0000\x0000\x0000@@\x0000@\x0002\x0003ÀP \x0019À\x000e\x0001\x0006a"\x0004¨\x0000a°Ö&\x00191*0\x0006FR\x0001Ì\x0010\x0000@\x0000\x0000\x0002\x0000Q:C\x0012B\x0002\x000cR\x0000	 \x0004¹§rµsÆ¾_lå,·N÷ûæýíôjÛ½X»Nq|ô?úõ×~òæ#¾ù\x0019cl\x0019kÆe[\x0018çë¹<\x001f§Ûqx<\x000eg9ÎÔé	×}YÃfq\x0018Óé£\x0017/ýö'øîñÉÝåêz½º^®.ÝeÛ­µÜ¯e_Ëeî<§03Î\x0012\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000 4\x0008\x0000\x0013
\x0000\x0019\x0000P§ã8çiö±­aYË`¤\x0019»ÆZËÍ¶]Ü]À¬
Ëåbßv3\x00140\x0000\x0010`\x0000\x0014\x0015\x0008\x0001TH\x0006\x0000TfF\x0005\x0018@</p><p>Â\x0000\x0000\x0000\x0002\x0004Ì\x00001\x00103\x0000!\x000c$\x0003`0¡Â\x0000(fHÆ\x0000\x0000\x0000@\x0001\x0005\x0006</p><p>\x0000À"d\x0006\x0000P\x0006\x0000\x0010\x0000B%9E\x0000@\x0005\x0014\x0001Á\x0000f\x0000\x0014E¥\x0002@\x0013\x0010*JE\x0011B!\x0000ISÌ23î·Í«ËÅ>c3\x0006³TÂÝ¶yy¹¸nûµùhß}þú\x000fkùã/¾t{zr\x001eÛq:ÎÃyNOÇé8O#×µ¼¸^¼¸¿zuwµ¯ÍY¶\x0019Oçé8s³\x0014a­Íårõû|ânß]÷Ý}wÝ7msYc±Í¸\x000eÇZ¾¿\x001d*k:\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0010\x0002\x0000\x0000\x0004\x000c@Ì\x0008\x0000 êt\x0007\x0012\x0008!\x0001\x0004Á\x00190`0\x0000\x000c\x0004\x0008\x0001\x0000\x0000 \x0000¤¢@\x0008\x0000</p><p>\x0010\x0000\x0000\x0000B\x0000*\x0005\x0000\x0000\x0000ÀÁ JÈ\x0000\x0003\x0000$\x0000\x0013B$\x0004D\x0002\x0000$\x0001\x0000 ©(\x0002\x0012 \x0000` 	\x0000\x0001Ø\x0001*#\x0000 \x0008\x0000Aó@"\x0000fF\x0005*¡$\x0000\x0010\x0000¨¢NP©T\x0012\x0000A0\x0014$\x0011\x0019gÜÊ\x0019§£ÁÌ¸Ûwg9Î¼?nf²Ö²}-û¾ûèõ+ñí·~ëÛïüî>×ZÎsi\x000eZfx.am-Û\x001aû¶yy\x001dO·\x0001;nçiÅZ±Ý\ß}ïåÓ;/ofùa¿¸l»YËÌXÆ6c±÷ÇÍyf­åvÜ\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000$@\x0008	</p><p>\x0000!\x0006¡ÌÊÌ\x00008ÏÓy\x001e:c\x0001\x0019:Æ\x00024ÊÓóçç}ß\x0000A\x0000\x0008\x0000TH\x0002\x0000P!\x0010\x0014(\x0000*03*3@\x0019\x0018@</p><p>ÀÌ\x0000\x0000\x0018\x0000\x0018\x0004\x0001\x0005\x0000Æ\x0002Ö@\x0006\x0006\x0005D2\x0003\x0000Â\x0000¡\x0001\x0000\x0000\x0000\x0000 \x0001\x0000\x0000Ø\x0001À@2\x000c
\x0000\x0000\x0006"fFAÎ91Æ\x0018\x0001EE	@BA*\x0000\x0015\x0011RIHT\x0014\x0010\x0010H\x0000F¾¹åÉ2Nçyµ\x000c.kiÒ£ä´£ÙÌJ§33W÷/ü°¿÷?ÿÏ_½ðfûÈ¹Æf\x0001Øf\x001cx:N\x001d}µm-û¾qf</p><p>ËÌâÃ;÷¥ùøÞo>~ëúüÞãÃ£WûüßïÿYc112¸N?§ã<mk·\x0000\x0000\x0000\x0000\x0000\x0010\x0002L\x0000BRÌ\x0000\x0000\x0000P\x0001¨Ì</p><p>ÀÌHNÙ \x000cÂP§ó<¬5\x0004\x0018\x0006pvzxøàéëÝÕÖ²Í@</p><p>\x0002\x0000\x0015\x0019 H\x00010\x0008\x0003%\x0000	d\x000cF\x0005*(af\x0000\x0000\x0000\x0000\x0000\x0010\x0006\x0000\x0011\x000c\x0002f@2
Â\x0000Â\x0000\x0000\x0000\x0000\x0000
\x0005\x0018@\x0018*\x0019\x0002\x0000\x0008\x0005\x0000@\x0018`\x0007\x0000\x0000\x0000\x0000\x0008\x0000\x000c¨\x0013É \x0000§¡\x0000@\x0008(P@¥23 $PQ*¤H\x0000D\x0004*oò_ýóoüðæ\x0013ooãvs~øàØ7/îïÌ¶YÆû§'-î.WY&k²ãÞnMn¼ñÅ/~éýüþWÿÂëºc[Ö°f\x000cöafs§ÛyºÝn®ÛfÅ0k³\x001eÝýùÿìï¾ý¹ã§ùÑë{Ý¿r<m®»ýá?{|ëçÏÓÚÐ8åÁ9yçãpÙ.*A\x0018\x0000P\x0001\x0003\x0011`\x0000\x0002\x000c\x0002¤¨\x0000T\x0000 \x0002\x0000P\x0019û~±ÖfÛ6Ðd\x000c Ûífßd\x0006A\x0014Çqè\x001c\x0002\x0002\x0000ÌP\x0014\x0015\x0000(BÂ\x0000\x0006\x0008\x0003"\x000c\x0000\x0019\x0000\x0001\x0000\x0000\x0000\x0001A\x0010F\x0000P1\x0000 \x0003\x0006\x0018B\x0000\x0000¨Ì\x000c\x0000a\x0002Â\x0000\x0000 \x000c\x0000`\x0008\x0000\x0002\x001a\x00060\x0000`p\x0002DQ*\x0010DN,\x001aA1\x0001P©SE\x0010H\x0000@</p><p>©T:J¥\x0012H  À­ñ_ùÎÿãëïýK~êÖòÕwï¼ñ7~ô#·NÇáO¿ùÆz~öêåK³=!³[À>\x001c3î·ååýë'\x001fù_ÿÚo|úßþÑçN\f3³¬\x0019§±-ÖlfádC\x0018cûåÏüæ\x001fý¿üýýÑßþßsÿòµl;cïýoÞÿÊ±Ý{w¹¸l»µïfÆ¾Æw·G¿êæù8­\x0019Je\x0006 \x0005\x0000\x0010
\x0003\x0000\x0000\x0010\x0010\x0000P\x0001\x0000\x0000¨ÀÌ\x0000\x0008k-k-\x000cÂ &,c¬µ\x0000AÀ\x000c39;Á\x000c\x0000\x0000\x0015(\x0008\x0000T\x0008$ @\x0003\x0008B \x0000\x0011&"\x000c\x0000\x0012\x0011 \x0012Q)\x0008c\x0006\x0000(À@\x0004aÁ 0\x0002\x0000\x0010\x0006a\x00143\x0000\x0000\x0018\x0000\x000c\x0002\x0000\x0000\x0004\x0000\x0010\x0000BÂ\x0018\x0000;\x0010\x0000P!\x0000\x0000 T</p><p>\x0013\x0018\x0003\x0013#CK\x0005\x0000Ä \x0001(\x0000*$¢T\x0012B\x0002!</p><p>@AÂà/ó>þÆoÿTÛæÃ\x0007_ãoþÆmÆ/Þ?Xw\x0017?ýøÇãôÅ»·>|ïÍÇo<Ü\x000e}-&ÛòÙëüâwþ¿¿úk¼~åõ\x0017q¬ìk9¥X3fFÃ`ÿö+/ÿø¿÷û¿ügþþïü
¿õ[Óå²q\x001cfÙ7Û\\x0019Äß}÷Þÿâý\x0017þÑÝgöËÅ~löµÙ·Í>¹âñx»5àì4\x0016Ð0!\x0002\x0008\x0000\x0000¨@%©\x0000\x0000\x0000@%\x0000Tf\x0006(\x0000DQÌdÖr¹\ÁÌAqwwït33\x0000\x0008\x0000\x0000\x0001 \x000c \x0015(\x0000\x0000 (\x0001#\x0018\x0004@\x0013cfÊÌPÌ¨Ì\x000c\x0000ÊÌ\x0000\x0018\x0003 \x0001`d\x001a\x0000\x0004À\x000c\x0002A\x0001\x0001\x0019¡ \x000c\x0001\x0000\x0000\x0000\x0000\x0000\x0001*°\x00030</p><p>a\x0000\x0000\x0000\x0010\x0012"2\x000cÊ\x0018\x0013k\x0000@\x0002$ TfF\x0010!\x0001A*B©\x0014\x0008\x0008ðxæ¿y{xóêÏï®¾x|ðÏ\x001fÞûO>rÙëZ~ýð`:ýÖ\x0017î×fÊÝõûë½)\x0015ÒäÃùèéxöt>s9½øä/¿úÚ\x001fÿê\x0017þÞïümXx>Owûf0\x0003ãÃ÷ß;ÿøð;úOüÞÓwþÎ\x001fü¾Ï?ÿ\x001c§Îe&s:Çlåj/ÄÿîÃ[ú|ï¯Ökg§Û:íçMòbÛ|ßÍçgcÌ:±(\x0004\x0019Q\x0001\x0010\x0000\x0000\x0000\x0015</p><p>)\x0000\x0000ÊÌJ\x0000\x0000 \x000c`\x0019fm\x0014\x0000ÊÌrw÷R\x001e­5\x0000</p><p>¨\x0000\x0000@1\x0013\x0002\x0000\x000402\x0008\x0000Y\x0014\x0001\x0000\x0000@\x0000\x0000\x0000\x0008\x0003\x0000\x0000\x0000A\x0001¡\x00010\x0018@Q\x0019P\x0019\x0000\x0000a@\x0000\x0000\x0000\x0000\x0000À\x0000\x0004`\x0007 \x0000 1\x0000\x0000P*0 ¢\x0019DÌ\x0010 RTH	\x0000I\x0000\x0000PÉ\x0000:2Æ\x001f=äg·ñû«oüÕûw~ãþÞï¿|é~-\x001fnÏ\x001eg^¯}
òb[\x001eÏÜd&Ëa9Ým»Úqxq=½¿üàOùs¿õÉg>}óÆeg­¸l·oßúó?þýÑÿøOl_ÿÊ¿õßýüs6\x000f\x001f>âîÎ¾å¼e
³6öÝfdùÝóçé[ÿÙyï½ÍÓqóx{öp\x001e®Ûòæº{|~±f©\x00131Ñ(@\x0005\x0000\x0000\x0000\x0000\x0000\x0000H\x0001\x0001</p><p>T`f(a\x0000a\x0006Â \x000c \x0000\x0000\x0000°Ö²­\x0005\x0000\x0000 \x0002¢\x0000a\x0000¨@2\x0006hT\x0008\x0004\x0005\x0018\x0015\x0000\x0000(81\x0000\x0000\x0000\x0008\x0003\x0000*3013f(LXj\x00180\x00034\x000cJ\x0010\x0006\x0002\x0000P1Ca\x0010 \x0001\x0008T`\x000c\x0003@\x0000\x0000\x001d\x0000\x0008\x0000\x0000)\x0012%@\x0002"1Ì\x000c\x0013\x0006T ¢\x0008\x0000\x0001B\x0008¨T` (\x0015¥\x0010P©T\x0014Å\x0000\x0019äÝÉ?y\^îËÛ³½ûÁÇ«?xõÚuwÏÏÞÝT>Ün>»»ó|\x001cn.kùp{Ö0¸§5}Ø×æ0î®/¼zó¹·ïý³¿ú¹õ_ziÃû«÷ï?øÃ?üCôÿþï}ùë_êºxùÂÿÕééñðñÛïÜí\x001b\x001d»\x0017¶Yæ8Y§µvöp9OÿÊùÁÏ¾ñ_Î+\x001fÎÛwÇ³Öò¿~õ¹­SefgHA\x0000\x0000\x0000\x0000\x0000\x0000\x0000*\x0000\x0000@ 23\x0000\x0000b\x0008"Ì0\x0000\x0018$Q\x0001\x0001À@\x0004\x0000\x0000\x0008	\x0013	@\x0005\x000cA\x0018 (\x000c%Q\x0000a\x0000d$c\x0000\x0000\x0000\x0000\x00143\x0000\x0000\x000c4L\x000c\x0003\x0008\x0003\x0000\x0008\x0010\x0006\x0000\x0002\x000c\x0000@\x0000\x0000 \x0000\x0000\x0018\x0000Ä\x0004\x0000À^\x0019\x0000 \x0000\x0001`\x0000\x0018DqÊ\x0018#4\x0018
J\x0012\x0000 \x0014@\x0012\x0002\x0000	\x0000\x0004\x0000!$\x0001P\x0008üå3?{<søòáÁG«ß{õÚuÆ·\x000f\x001eÃs§§óðÑõÎÈÃíYe\x0019\x0019ö\x0019§<\x001e§ÁQ\x000c
k-\x001f¿¸÷ôé\x001b?ÿî[¿õë_û¿ùSùgæþãì\x0017ÿügÎ}Ì«æÅóðmã¿|\x000f_½÷\x001fXþ@Ì2³³6³2ÇaÛ6ë²»Ì2Æëò¿ÿÞ\x001f=þñm§óp;ýí_Ûä,³Æq\x0018df\x0000T\x0000\x0000\x0000\x0000 \x0002\x0000\x0019\x0000\x0000f\x0006\x0000\x0000\x0000\x0010\x0008\x0002!\x000c\x0000\x0010\x0019 \x0002\x0010</p><p>\x0008@D\x0005\x0000\x0008$\x0000\x0015\x0000\x0002\x0010 BÂ 	\x0013¨1\x0002f(\x0006A0*P\x0019\x0000\x0000\x0000\x00000\x0008\x0000\x0000ÀL\x0018\x0000\x0001Â\x0004\x00180\x0000Â\x0000\x0000\x0000\x0002\x0000#\x000c00\x0010}fTf\x0006!\x000c$\x0000À\x0004áD</p><p>\x0006\x0019\x0002\x0002\x0000\x0001(\x0008$ \x0014B*\x0002\x0012\x0005D"*
ÅÿçûG?ÿì£ëÕÝ¾ûí¯\f|ýøàÝíÉe6ÏçénÛ½Þw_?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1432852191/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1432852191/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-cartons-papiers-plastiques-1746663385/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-cartons-papiers-plastiques-1746663385/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-du-personnel-1886111767/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-du-personnel-1886111767/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/tp-btp-espaces-verts-peinture-industrie-1730535705/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/tp-btp-espaces-verts-peinture-industrie-1730535705/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/masques-chirurgicaux-type-ii-980159291/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/masques-chirurgicaux-type-ii-980159291/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/prestataire-de-service-dans-la-gestion-des-deee-2019969519/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/prestataire-de-service-dans-la-gestion-des-deee-2019969519/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/travaux-de-maconnerie-1106306838/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/travaux-de-maconnerie-1106306838/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-861514076/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-861514076/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
Instances: 11
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion](https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/contact/creer">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae/export/csv?page=1">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/masques-chirurgicaux-type-ii-980159291/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/masques-chirurgicaux-type-ii-980159291/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/980159291/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-861514076/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-861514076/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/861514076/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/annonce/resultat-recherche" class="form-category alt col-xs-12">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-du-personnel-1886111767/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-du-personnel-1886111767/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1886111767/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/prestataire-de-service-dans-la-gestion-des-deee-2019969519/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/prestataire-de-service-dans-la-gestion-des-deee-2019969519/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/2019969519/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-cartons-papiers-plastiques-1746663385/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-cartons-papiers-plastiques-1746663385/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1746663385/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/identification-verification"
                          method="POST">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/tp-btp-espaces-verts-peinture-industrie-1730535705/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/tp-btp-espaces-verts-peinture-industrie-1730535705/voir)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/quote/1730535705/flash" id="quote-form" class="date-selection">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/inscription" method="POST" autocomplete="off">`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "_token" "email" "firstName" "lastName" "phone" "subject" ].</p>
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_small/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_small/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/760186ee95ad5f17ca2a6334e7c0f674ccb4c012.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/760186ee95ad5f17ca2a6334e7c0f674ccb4c012.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=121%7C138%7C86%7C87%7C88%7C89&structureType=0&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=121%7C138%7C86%7C87%7C88%7C89&structureType=0&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors&structureType=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors&structureType=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/760186ee95ad5f17ca2a6334e7c0f674ccb4c012.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/760186ee95ad5f17ca2a6334e7c0f674ccb4c012.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1730535705/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1730535705/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/c2629827e496c28d0d70e9d1fabfa719f777936b.png](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/c2629827e496c28d0d70e9d1fabfa719f777936b.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/c2629827e496c28d0d70e9d1fabfa719f777936b.png](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/c2629827e496c28d0d70e9d1fabfa719f777936b.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/quote/1746663385/new?budget&communication&prestaStartDate](https://lemarche.inclusion.beta.gouv.fr/fr/quote/1746663385/new?budget&communication&prestaStartDate)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors=9&structureType=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=ods&lat&lng&page=1&postalCode&prestaType=2&region&sector%5B%5D=9&serialSectors=9&structureType=1&zip)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 130 [https://lemarche.inclusion.beta.gouv.fr/media/cache/user_profile/uploads/users/images/760186ee95ad5f17ca2a6334e7c0f674ccb4c012.jpg].</p><p>Predicted response size: 430.</p><p>Response Body Length: 766.</p>
  
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

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
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
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-861514076/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/sous-traitance-industrielle-861514076/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/masques-chirurgicaux-type-ii-980159291/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/masques-chirurgicaux-type-ii-980159291/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/prestataire-de-service-dans-la-gestion-des-deee-2019969519/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/prestataire-de-service-dans-la-gestion-des-deee-2019969519/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-cartons-papiers-plastiques-1746663385/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/recyclage-cartons-papiers-plastiques-1746663385/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/travaux-de-maconnerie-1106306838/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/travaux-de-maconnerie-1106306838/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/tp-btp-espaces-verts-peinture-industrie-1730535705/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/tp-btp-espaces-verts-peinture-industrie-1730535705/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-du-personnel-1886111767/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-du-personnel-1886111767/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1432852191/voir](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/mise-a-disposition-de-personnel-1432852191/voir)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/common.48bd8f41.js](https://lemarche.inclusion.beta.gouv.fr/assets/common.48bd8f41.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/bs4_common.6032a86d.js](https://lemarche.inclusion.beta.gouv.fr/assets/bs4_common.6032a86d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js](https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 3
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/manifest.json](https://lemarche.inclusion.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion](https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion)
  
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_contact/uploads/users/images/0b50158f6d017b0be6f67a26d97b16f30cb09290.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_medium/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_small/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_small/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
Instances: 6
  
### Solution
<p>Disable debugging messages before pushing to production.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
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

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion](https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
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

  
#### CWE Id : 693
  
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
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/16fcfef5b9a1a0282799571f173411296d394e5a.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/16fcfef5b9a1a0282799571f173411296d394e5a.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/07ef92fa6a327b34354a7982a98df11e1404e970.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/07ef92fa6a327b34354a7982a98df11e1404e970.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/0ca5b2d46926dd9a6c189103ed072a6bab17adb1.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/0ca5b2d46926dd9a6c189103ed072a6bab17adb1.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/5d0ea98a96273fd6f2bb600d04502056d1a6f6bd.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/5d0ea98a96273fd6f2bb600d04502056d1a6f6bd.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/7f0547b8815dfb7c2045f709bdd8833412321101.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/7f0547b8815dfb7c2045f709bdd8833412321101.jfif)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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
  
  
  * Evidence: `1432852191`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `284407453`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2042235137`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1199510057`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621873101`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1345576341`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `349167192`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2019969519`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1530435789`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1730535705`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1196448685`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1230430571`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `387377491`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `328540996`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1397769748`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1071504434`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `859151117`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1551055594`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1432858399`
  
  
  
  
Instances: 43
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1432852191, which evaluates to: 2015-05-28 22:29:51</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[nb_days]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `time_range[nb_minutes]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[start]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `sort_by`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
Instances: 15
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=02%3A20%3A11</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [meta] tag [content] attribute </p><p></p><p>The user input found was:</p><p>date_range[nb_days]=1</p><p></p><p>The user-controlled value was:</p><p>1</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

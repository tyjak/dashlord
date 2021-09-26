
# ZAP Scanning Report

Generated on Sun, 26 Sep 2021 09:19:33


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 4 |
| Low | 8 |
| Informational | 8 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - PHP | Medium | 3 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 12 | 
| Cookie without SameSite Attribute | Low | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 12 | 
| X-Content-Type-Options Header Missing | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Sensitive Information in URL | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 9 | 
| Storable and Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 521 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 13 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `574574574574`
  
  
  
  
Instances: 1
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: Maestro</p><p>Bank Identification Number: 574574</p><p>Brand: MAESTRO</p><p>Category: </p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/statistiques](https://www.monstagedetroisieme.fr/statistiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/statistiques](https://www.monstagedetroisieme.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" href="https://beta.gouv.fr/"><img alt="Logo beta gouv" class="mt-3 d-print-none footer-logo-img" aria-hidden="true" src="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/beta-gouv-logo-4db47f99e37c7b7f888f315b993f3376.png" /></a>`
  
  
  
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/CarnetStagePro_USEA_WEB-2.pdf](https://www.monstagedetroisieme.fr/documents_utiles/CarnetStagePro_USEA_WEB-2.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=T(#%J636lS.2E9gGp-S'@'5];hno_
IunL6Gh-Q-C45eD@!)4u5WUmP9E[]ncs$&\Nga01?mou9"[A*(HBopV5sM088tZE+
8(5lH52)AcG'7<<gf#p8bV.eos/=$;C`$=qD(WDrjfA]lRYim,RqrACdejgO/AF>(
/:tg]_t>sDIL8P<ndm?OOg2bg,-Em:1jeEn-[97]R[[bI(P]d%f!I;eeb'o)qeJ7,
B.cOqT*d(nYRO5hkDtb5$C0au"Tu@Gd5re*4LT0a7a1s2(FCIYl*Hscd?$6a1aIjm
`#s0m!>?_.0o<c)d:14=0]UGQjn;]0qKM`<7PPUaM-O)AhPTW$':M2&0_hHReg`^d
7R:TK-mVk@qM%4_RD&Zoj*$-:O\,P7G8CNp$hFmd47K<8U_e8pRSKd[0+J5ELBKfW
9L7',Oq*H#neRo8?p<q%gkY'iJ^MpD;p9Z&0HV^R_Q8>,=2iEcr<Rg<bF`7PF$4(]
7=;9#?7M7#FSgN'HKh'jS#/aY66j[4MXrY:L>ZOF;(Wn!kIE`M_?jL64MdEt,m)Yc
q)k2_XWMBFeot(QWg#\eAS8p.1#t0Oh:R&-2fIWY4$4OTG4i"eHMFCbG%eAR>[fpD
DUAgu&;"Vg$-7)+o:(\%WDg[DHaj=nPCQTMYbl%pT"7k`gGf;5csf#*;r&)CH+o&S
,iC5aJQd)D_edC]SdIK.>-h`N(pX2/]qhur8]&$Vfr@,nVo+@bQqo[;hEa5/e+dSU
r+qq.!4%H/QLeg@]Q7`s:MnoKRc*j44?N\<_*jGI1b!)b'6*q4!7^H/3W~>
endstream
endobj
363 0 obj
<</BitsPerComponent 8/ColorSpace 243 0 R/Filter[/ASCII85Decode/FlateDecode]/Height 74/Length 898/Width 104>>stream
8;Yht=gir*%*^G4G5iM&4&7"b7LWDdH.UM[.3p1*%.=!D[e*/GoW!24mC6KLF/o$H
p3`V+%Q2YE''\'1:9K9-l24&s/bZuO5L@E$h>/oJ-qd@`=`@5g9LpcuIZsmteEn[l
MR"c_mp'jPLS$@Lp;?48*kW^2g7J!48]XJC'=-./.-<F:16<p$QJk-biV8T01k(,X
6&m@BfR?>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÓSkåúòúN¿ðºaòkXzçóö0¼¦i¶EZS\x00147<_úÌûQRmèfè*ÀÃp\x001f®í!¾\x0005)Uvú®	ôíÁpã} ¤ðÒ<ïÓ\x0013öÜ{\x0013¥"9;\x0017,ÀÈí4Óùêt-OÂN:JÈ²Ò¹cáWé8d¬\x0001äZ\x001b\x0004S\x0014y\x001e\x0004\x001ayeÂ\x0001ò]2õï8pRWªÊ3z£qµ\x001bgÒµ\x0006¨mTð\x0001­rN\x001fÉÑ[³|³óÌ^\x0019+\x0019h\x00049Þêý8Àñ6Öïé\x0012=}Ð\x00154ð'!+ãc}²\x0008Ñ\x0017\x0000ìNÓU<\x0008\x0014 Ã5á7Xpp~\x0003(\x000cXïl\x0000ÜZv7OU0Ë\x0011´m\x000cùwÎ\x0017C-«6\x001díðà\x000f\ y	ÚsÒ~Ô\x0015}«cfdj¯\x0013á\x000bHõ\x0002\x0008\x0019
Ù×\x0003µJjDl\x0006
\x0018|B\x0016ªYð<\x0003ZR\x0007²>4\x0017ï¸ô\x0000öë<ò\x0019\x0010=	-páÛ92äw@Qu^EåJÄC'%Ø\x0008¥î±àº\x0016¯U}ìÁ\x0015ðD!
b5_\x0000õj\x0004¹GÇ©æñ\x0012Ëeiv\x0010)Å'LpZZ"6J×"s\x0011ø\x000cÃ6A]\x0006ïÃyRãñ3?\x0001³»xw?5ð´ªÌ/Ä¥Â%B(«üØåh~:OîÇ\x000eÏ\x0017¶rêY\x0012í\x0018ò\x001aGðC`·'ð½bpÍ\4å&R\x0018Èg.»²®+{Ùg7öOD\x001emj_â\x0010­Ð\x0018\x0017¢¹@5\x0001[\x0016ûMÏD¤5p÷Û\x0017·´® 43ômi\x000ey\x0012ûÀØ8\x000fjÆ²pà\x0011ZÃýÏÎØ\x001bN#×entÒSà\x0017`\x001câê5K¤+®¾gø¤8ÂkÐ ~¹\x001eOÓ ÄÏÀf¹´¬U\x000b9\x0002òð_#± pypËsAb¦:VÏ\x001c -+Îù%î\x0010ÂºÐÂ²'N\x0015jà28r\x0010>;ÑoæØB,H\x001eJO\x0004'¢2þ\x0004Ö`ÇÝßÏLÐ%Ý·m\x0003K\x0014S¿fM#;4Í\x000c«
³\x001f\x00143\x0003±òX9ØîùÄ`Ä[âï8ü\x000b3¾\x0018\x000cb½(½)öÐNîOxÎ\x0004ÐQê(|üY#\x0014\x0011EÂ\x0013ãÔÆ(r\x0010Ç&ðÞtó\x0017»¯xH¤(Uî¦
¿"@	/d\x0007\x000fXB$ÐÑM4	0òPô¾æ¬£3(d®ì÷U+rì\x0014U%ß·ÁCÈ>\x0004wIvjoÜ¯\x0002´å~4:¿6:ýê\x000b·\x0019º2Ø\x0007©ü"êð\x001a\x0001)Ã5:WÍK°[Åã¡Ç@¼EüÉ^ö¼Vg¯¡bÞñlq)\x0001\x0016Y+g0'	dOß·Ñ(´ôW»ct¯ÚÎ1\x0019q,Ô\x000e:W6¿äå\x0019¤(÷¼è;Ð{w­ÀxÈ\x0008\x0013\x0015
¶êúÌ@gLÑi@EÉàå\x0014\x000f\x0008­E\x0000Íy*u\x0007×ã®v¤.ºi ëÓÖ¯±:²·r4gj_êìg=ÄN«IÎ3:×pæÐ®éÁXÓ+Í±ÄÌ]9¢\x000bÿ\x0015rª éø\x0017Ý:Ó\µ%¯'º°:ô\x0017#¢¬ôÅo\x0002\x0004¦\x0011@H\x0014ÚÁ³}^ÉûVp¦Ã÷&¢n¦09Dâp!Ò\x0012ç¬«ÒM±x2¹\x0003B¶²\x001bd*°
× ËôÀ´£Èeqì°å
tRj\x0018ó\x001c«\x0019´WD\x0012\x0007ï\x000ciÚ(h\x0015GËÍÔY \x00162nYégí±\x0014ªH»²\x00077\x0002n\x00053ò4ÑM\x0011@\x000b\x000fhA±\x0014þd"Dl|GºK;äû%*W|Â·ßÌ]¬àF>]Ä\x0000:\x0006
ú¼\x0015\x001a5\x0011l»­o(0jÒ"&ÌØEINÔ±£Ñ\x0014"\x0006\x0018 b
!\x00101­\\x00004ßP\x0019z\x0008\x0005Ð·ìíUä\x0001¤ÏØE\x001at\x00047\x001aôü@³ù<\x0014ý\x0008J\x0014N[º4à\x0007µg+Ûçhg3\x0012è»Î¤õÄYW¶m{©BjF£îúÐï¯çÉÝû84 âËc\x0015ALq$Ã@ã\x0008rG\x0004\x000c'£\x0017Ü¶"ÊÔ[qKFl;|ÃI\x0015sSRoÈ
¬xð\x0006­Óq{ÞlIzz\x0006eÒåõ¢Ûkñ\tõ<Ó\x0017·\x0005\x0004×¢Q(¨ºCA­tâ±Ë0\x000e0" \x000c,_=\x0012\x0017gÎ~ÊôLA\x0011g¥\x0015%ôy=µ[Rù®¨I\x0018EFI¢b_\x0014(Å]\x001a\x001ew©ß\x0014n³)2\x0013Y\x0015´ÔK+X\x0002QL\x0012\x0006NFÅ~Zfå
±\x0004­{Õæåê+Åê÷Q\x00143Ú+äÒn\x00149°ºVîY\x0003Ø&7Ù\x0011Þ¼X1`\x0018\x0003¯3æÒ\x0010íêÊ4d%Ø\HYq<¬Ó×Å}J<³fd(acGiº\x000bË¤#`ÇmòÀOwa5è\x0013 	Î\x0015\x0002å\x0017o£
\x001e"½§l×øÕô¤B¿xbd;Õ(!=¢Ûuä\x0012ZÜ\x000bÑ5îÝC¦.Ì!ö=rrû$FM"KlÌ0nî?éÁ\x00033T¢e:-wZÏæËQàYQ±KL\x001fÊn\x0002h2$Õj8\x001c\x0004Ï0+z \x0014w-w[Ëa°x¡¹qr\x000f¤\x0017]²©gHÌå~(3Í"ïGÑÃgÂ\x001eé¶¸ú'\x0016á6K§²É£Ë=®óS\x0003P\x000fRfï\x000fC:ÁFg\x0006<Ö­bî\x0004\x0012Lõ´\x001d\x0016÷¿\x0003Í8ýveFã`E\x0011vW.ÏBOÍºCNÉÝF\x0001Ü¨*CJº'¡¸,1åm\x00071»hÉé\x0016\x0001 Ö¡e4á!í9º÷\x0002DM\x0018ÓW¶­ÐÛÓø³Êå4¤m8FÂaØ\x0016k¼à3`ç$F»((êTô\x0006B&Ò£\x0002½§\x0015\x0019å¢v
÷dº×p Ó]\x001e@UjÜÛ\x0019\x001e\x0006\x0006^øE^`ðxwû­ý\x0001F9ª0ýwdEÖ´nÈ =¹¿KüÙ,2mUBÖXÆ¨\x00192®Iã¦\x001c Z@;«\x0011kZkÈ³êâûRÆ'hDL7¥´½\x0008Ñ\x0013,ßñ\x0002ùc7Æ 9«K\x001du?\x00059-÷Ñ\x0005M\x001drÞ8h×3àAWBÉÝ\x0007W÷BåbÄN/YñËº\x0002ª¤èé$\x0003¹K~³»Øæ¡\x0010wØ\x0015\x0018l,S6&	0*\x001d¦ð\x0013Ô«\x0016L¡m¤Ì ò*Ý.ò6LÏ¸\x0018¡N\x0007çUa[",\x0014¹\x000f\x001f§õFZî{­\x0007ø7#U¯6\x000ct\x00108¢ñÀ\x0008iti-?kEîuàÍä7º£6\x0015qÍÀÌXxP¥°«p¬3ò	\x0007Vù3|>\x001a\x0018¡Þ%®ÒÁ\x000ecøu9T¢ã³KFØYt\x001bèÃ±ZÑ\x0003:°æB\x001f½t±\x0003m_¢\x0003ÝLÿq¤ó.§Àö<à¨x--S8\x0003^º5ZþÍéý\x0000é\5 !s/
)¿ÄJY¼R£ç.ùìÏØ*\x0013I:ÌcãçmÖèNÍÁ\x0007¹ÎÄ.ßE÷L'û]_I\x001e\x00044\x0011é¶½\x0013=\x001bÒL¶he}BÇÙ³ÓåüÒ¶x)\x001a\x000c»^öOú½H'Ä7ªû/Nò\x0008.»1Æ¦ ³M}\x0012RoÓ¢¥¢å¢õøB\x0019rªæF^xC¦B\x0017C$)\x0012\x0008w}ï\x0017uþó~V!$è[¯QÀ]ÃJmôË\x0012¤oNv\x001eèPÕ\x0015©¨"Qù©óÐ·\x000c~°#áÎPn\x001e9¤\x0011Y=ë\x000ebIò³[§|\Dð\0ãEÐ6­-¼{Ój\x0015TÔÈiúè\x0011\x001be>À/(\ØN-F'üøE¸ýâÅ/­ÿ\x0010"óæÿ<¾¹ýÛ÷_üá{ÉrÊí}ë+ýj\x0008¤\x0000Ü \x0008·Ûûo^¼\x000cñÕûÿõÅ\x000fÞ·²"#X8ù?t¢6½ÒìU\x0019OÈh4\x0013³É\x0002iè\x0016Á\x001f&BÑ\x0019Ï\x001bpñö\x001f\x0001¨\x0000+ó'å@?yÉºé¡2Áþ8.h³0¹\x0011x6<>yÎÓÎé"Õ?íÊ¯\x001c\x0013§qã\x001a\x000c¸<$!*ô,3sP\x0012Ô@2|î3Âq\x001bæÊ­lÀ¿·òéÌÁ·qX\x0019\x0011'dÑ+\x0019ì\x0011^è©Á\x0012\x0011\x0001$\Òi!Îk¤CÐDã<A±íú:\x000bÏ\x000b¸»D\x0005\x0003ç\x0013 \x000cÃ%\x0013	$\x000e	\x0004ÉÝ2\x0014\x0008G\x001b1ùÈÃ\x000e^@¥P\x0013QöÇ\x0011È >Z¥[pb\x0001H\x0000¤/½q×º¯4ú\x000få]\x0010A5\x001f\x000có\x001cú4E¬JÏ+	\x000c\x0007Âp¬A¿={ß4\x000e¯+çI9Y¡i1&Hv\x0015[3à¤\x001bøø\x0011Û5ó´sÚ hù´ë¾rØ\x001e.5øª&\x001e»<¨x\x0006ÊÉ\x0004P\x0007l\x000cöf²\x0010Ø\x0008´44Û¥Ê
õ¼rPDò¡ª\x0008öbÖ;Dfáf?èwéÎ#ÚÚ»^ÆÅ
]:\x001d+Ë\x0012öë\x000eV6ºõ¢\x0011ï¦xâ\x0012ÆM_Îø\x0006
Ìj9IQþ*%ÓH§Ø\x001a|/!ÀB®dÙ9Fr]ä\x0007<Óws\x0013\x0007¹Uð¬+1[þð=+ç\x0017ÛNóÿ\x0001±óUãendstream
endobj
223 0 obj
27281
endobj
231 0 obj
<</Length 232 0 R/Filter /FlateDecode>>
stream
xÍ}Ýr%Ç\x001e.¬Ø]ïü\x0002í«=Ph»þ»uãÐRD\x0005EKÄ]Úá1\x0018.\x001c\x0007!!cù\x0018|ªÕ[(öJ¼ñ\x001fÀùåOeõ\x0001gHxä0W±\x001cd®¬¬Ì¬ª¬¯««>æ}füOÿ½¸>ýO\x001f·é³»Óy?ÇÆ¿ºN·¦%Õ}ÎS×²Oë\x0014ZÉûyj©û°Ò#§/¨ð\x001aQúó)Ôö¸îç%Ni©$-M)Ä²U*)M?yú;«·W³P5óÒ«	ó\x001c÷µ\x001eUC·yëÖ°îs¡j#UÛ¦¥}Í\x001eþ8Ý°>9ïsdìGVê°ÂªP\x0016¶*Å<9\x0004ÔÕU
K$ë<T©}ªôxa¸oTf®y\x001fÊ¨\x000f~`\x000bÓKÙ·É\x000bÁb2uÊ:!×}KþSj¡IÔÈ>Y÷k¡gI0k
êÞé\x001f>ñà³\x000b\x0012`±éÙSq ¶Å}B\x001b#ÉXéÙõé§»ßßLßuÛîð\x0017ú»\x0010êºûâ\x0012üµ¬!ì¦«»Û«ûéFËZãnzqNWçwôÿ·gO"\x0019ÞÝ_ñ3Ë\x0012\x0017*ø\x001cDSÉ»é³¶çºäÝË{2Ö7ü\x000bµ1îîÏÿÇáêîN·ÚîËX×²»¹ÿÉÙ<ïãÖÝtößý\x0017²5l4=ûðôÙ?Ý}þZD¤\x001aE¿ÛKoÜôÏ¤uOÁWI
ýµUÞ,6\x000bqZ Ì8\x0019¿<Ý=}ù/_M_\}vu8¿¹þãtö÷°mç
5(¦Ìûì9\x0017J\x0011¥>Ý}pÎÂ>.¹­»W¯ïj\x000bõüööêËÛéó×_¿¾H»º¤²æÝ7¿|qéÁ±e)»ó×xx	miawwyEe#\x0005xË»çR~Ê»\x0003	e²-%.úSXò¼ì¾8«ûuNô×Ë;pç5´»8Ýï ,ÍaN;)NÝ¦î^à'\x0016Öj»Ë\x001büMÆuwûÍùáêþ\x001bÖ¡¸C\x0014 XK\x001a¬á°Äh6DÕ\x0014Ö~bv{²Ò8B¦Åj¬âÚê¢\x0001baq}ys¿¾&Ã}5\x001dHÛ«çW\x0017ç÷W/oî¦;bVÖ\x001dù~~õòõ-=G\x001dæ"àp:O$êþrú©\x0005\x0010õ\x000fö!«ðáé.ì·¾]`­5o?Ýýì,ï×¶§^Ol~\x0011*öÈ6\x0014{wÐè'ÓÝ7Ë\x000büy\x0003u¿\x0016ÏþÙ´9ªþÕc¶ØÅýÙ³ÿ9(R\x0011¨¡+B6Ç\x0000N½òÙY^ö5²{I\x0011öçéùíY ^\x0012ZÚ½¼º¿ü	)wEZ}E&º\x001dtýé\x0018\x0011k<ÿÊÐ ¿ÌÔ)_#Ä/§óWp U\x0012àÙóÿu¬±)Ô5NoÓx7½7¨!\x000fRÏå\x0007sÚç\x0014ª5í½ËûI¬E
\x001e.q\x001b
:'²üõËmx\x001cëXf\x001aë\x0008ÛåÇêH\x001fê¸;ùñÉÓ?üúäÃN>9ùGþû'?:ù\x001dýû	ýûñÉ³\x000fN>ú\x001füêä\x0017ôûGD?=ù\x00042ßÆ#}âÉºÇ2}IÃùB³\x0014Ùfbú/i÷ñ/OC¡Yt®4ÿf\x001a¯ât}\x001aëR÷KêÃéÓÓø\x001b§¢3BÂ/Ã°dfhB®æ(ÁxFøøòæùåWOd¸¨
qq'f¹
\x000fþ\x001eµcÀÞÔN­ÜSC·µùåg4s·@\x0001¹'/ßÝvùüòþölÅ 2\x0007
í»+\x001cJàbÿâvTí¯f\x0014r¼ªE\\x0011ê©ô¤W¤Ôôüë3\x001aäHÓ¶;¿¸x}yu \x001eNqoö\x000by®l¿?O=1¶]¼¼~uqf¶ußhÒÓ(ðdÆ\x0003âû/¦\x001d6ÿßë¤ÎÚRÏçu±óÁ"¢\x0004ÏaÍ4ÄßË\x001cÜv·ãt×Û\x000e\x000fÔ¬ÒvÜSÜBYÉSOh~ ¹ LO $ªåÞà}àSjã²Ò¤´£ \x0017ö¨\x0013|À}Bÿ#U)=ØýÝ½å^ó+<JîÍl\x001dî.\x001füáä¸ô¯éG\x0008¶ÌÁ\x0005» îsÿ¸á|ÀOKµÿá\x000c#BiêúÛ³±ÂZ/\x0019\x0002¹üIjä3Jx©qa¿ê\þáËÛ;\x001eí¿Iùò\x0007bË$®C\x0016R¸PâÁqQ)\x0013Ýó\x0000v{yC3Æg7ßLwçìîuÍ\x0013/9uÁù'<6»/o^Þ_½Ð©n\x001aø2FSê3¯Æh$
ý·?\x000f_üo¤Y÷³\x001a©×Òþòæ³\x0003³>`jø¯rð>Ë¼ÇêpòÒºPL|[Ü$äØkÑüûÈn,|\x0002¦»í©Ã¶9!íìÓýSÎ<)
¡äð\x0000WJù)ÏàZs
+.\x0012$ÊïKÙ]É\x0013±¢	ø{Áó»\x001b\x000fôË¯Î0r,ëÎ$H^M4
~
qs@6øÍÿ^C
»¿x_HGª©´QÆWx~ãO\x000fìáá\x000b\x0011=\x0012;nA«­òÓmÆ\x0012iÇ>^(]¤\x0014éÕë¡iß-ñÊ½kéîÜHÌW.ýÛ\x0015·!|ãô\x0019\x000b2v8\x000c~yï½<FÛ;\x0019pôÀ¯¸+ñ\x0000­ÙÜ)<­ÒttP'¿ö±\x0007%5¹&#Ç]WqæôÞÌéÖO.¶÷\x0005Î3ò\x0015ùU\x0003FkT\x001e7àóË;ÿq¨óÇø)ZUP O½|=Ô£¹\x0016\x0019g%_ææÆáaô	µÌ\x000c\x0003\x000euMª¡þÈ´-)¡\x0011ìGûoøoO]ä1\x001aA¨Û¨©ÔÎwW=ÕôäIòp]4qÂ4´Ðò­|[-d\x0018T\x0017Ç\x000cZÈ¤é	-#Å
\x0011WÑC$>P_x¿5Ô8\x0002­í\x0016Óô½.ËîA\x0010æB)D[ÍñïßÜ^~F~Bâ\ÿú%\x0017¦h¤.þ|\x0010tõk\x000f­QÂ{u!OJ>ÂpÉ¿-è
´F8\x000e3ÊÉI½ÊWüt]h¹Ö¤\x001dÚXoZ.wL\x001f?dÅèJ&JXï¿xqu¸ê
r4ÉsÓã¨\x0008ÈuRó\x0019õî¥å:À\¾x¥Ä\x0017æ¥ìDt,ûôk])ß¥DVÌ\x0014CAË.J)×¢\x0010Ø/Xû7Î,Ãº$E¨ÀÚöµLLG\x0003\x0015eÄ¡É8\x0011¦\x000cx¬M\x001ahúw\x0001]ö ["#²¶`3\x0015¤è \x001dhQ³L1Ä\x0005
Ó	tY \x0004JTªª&ö6Q
Y¹D¢e\x0007I
\x0012àÀ4ÍÃ\G¦Ú(ñ%\x000eÍcH\x001e\x0003ÕAu¦9BÙPØ<$±ÂÒ(QhZ#þ¥\x0007\x001arCUÈeñx\x0002îÇaC\x0000=WñÀÒ¸ÂH\x0019ô\x000c*Æ5À^(Ã¾4R¦¶BOÏðoLUJdô\x001b\x0001m£\x0002	ËTj5-ø÷°c¬°#[\x0007Vn%²	¬\x0004tm\x001dÓ>ÁìG\x0012iÎ¥\x000eI45ÚJ®[á: ;Ò\x0013Ã\x0014¨\x0000g&ö\x00129r\x00152V\x000f8\x000f\x0012È(LÎ\x000cK!¢"ÌÄ\x0001\x00043D\x0000bq\x0008¨mÄ]bÔæ\x001ct\ö\x001a\x0015PqBNÀiRä\x00161-æÏ\x0011Æ$NfãÕ>BM#wF`T\x0005\x0019+{W6N¥¼¢Á\kdE+\x0005F9)0\x0010ñ\x0015^CE
Ó:7¸§
l\x0014$>"èbN~%¿C%ê3¤4I`Çp\x0004e<AFªEúT\x001f-ÈQ¨j
Yb\x0008þ£Ð¢\x000eD¤7"pD\x00142É×ô<Ç?Eõ
ä/Îi/0S@\x0007\x0000Hg¹D],"\x0004æÀ:¥ÚØLA6\x0001&ÃÏd®*1f6Ó2úÐEiø7[\x000b\x0000J!(COpÔ%Ö~]\x0013¢c\x000c0\x0004:ª\x0015°ñÚ¢ÆL\x0000\x000cI¾ÄdþO®Y%Ê8fh`¨¬þ\x0003ý?HYÑ	)º\x0012õÿÆq<£K¡\x001d\x0014ë\x000bâ£\x0005ðDn×!Â¶1¸üö¥\x001fM\x000335n\òDAI\x0003¸-
»XòíB_±\x0017@·´\x001e¤HM¯O)_Øcú5N¦\x0000ªd©
;äuÊ\x0001Ø"h\x001cL
ÝK|\x001a1H~¢¥e\x0000¾á®:QÚäVÂ\x0014»\x0001~Fë*\x0000\x0000\x0004y2¹b!\x001fÔB\x0001Ai ¢\x0015@\x0001z\x0003\x001a#¢Y`¦b½\x0011M^¥ÀÉ\x0011KX*i(Ï°g"CS\x0018Ð"·B`¢I àÎ¦L!\x0010õB¨\x001a0^r£)Ti¸ª\x0015mÐ­$äÅiE%e\x0000£Çb_ÓRo/&·
\x001a.6\x0012f4u:7N+{´Ö\x0000ôDsO&E\x001bÕ[À#Lalä\x0019l4J²`¤T¯uñÄ\x0019FÏÜ¹¦xîf´ûA&#.¨ R\x000fâ¦g¼\x0006\x0010rÚ×\x0005Q\x000b ÅËÌ
dt¤8\x0019h¡¾Ð\x001fïaD©
\x0006	\x000b³JA \x000f­\x0007zà1= P\x0015ð*êÆ2ô¸é\x0001ÔÒRhÞ){À[çä\x0002\x0015#Tà\x001e#2\x0018"áÀ= 1NT¼gA\x000f ÅÄT\x0016*\x0010\x0002÷\x0000ÊÖ^\x0016\x000eÿ($é
ý%ÏcFË\x0019\x0016È¾QßF'VÜ9,\x000f£ÁÌ\x0012\x001aùdå\x000ePÈ«4É/ð\x001d:@ÃXL³zHJáùEVi3\x0012Oãw0×U;À6×\x000cÀtÂP\x001dÐ\x001aÙ\x0006f$%¥\x0003°NÊA\x000fX¼|E&Ç\x001a\x001a/Ib£yâºÓ\x000bÕK¬x_Ö´\x0007Pü\x0012f\x0014êç¬\x001bj'{#VyÁ&}`-lY»xÔÃ@ãz
\x0008úÚPCà_¦$¸§WLð\\x0003F\x0018´\x0016\x0013Êè,{Ó¦nM3[á¹\x0004wü%¨\x000e4óN7Wié%z4Õ
·\x001enâÐp<×G÷B\x0013I¡q¦_î	é¸'àµ\x0018æ/ï	Æ±@f1ç}æÐÄ>½'Ìhfð\x0010Ú'zO@Z²¡3DêsõÎDuÉÞ\x0019ùæ±/`ä]«÷\x0005$Û­x_@:\x0019òÐ\x0017\x0002\x0005Ø½/ÌkËz\x0018Ñ$1|è\x000bs¨Èø­/äue+t3	é}Á8Ö\x0017´|ì^Cý@\x0006®ÉûBÄ½\x0004\x00168%}!!³é]A¨Þ\x0004~<=\x0001\x000b¦\x0016¼'tZ\x001c×å÷ÈäÙ¼'D«W÷tgo´'Ô\x0016\x0007´'\x0008½x\s±#ÄÈSP§ñZ~Í^ \x0007u\x00046ë\x0008\x0016Gáú¸åNÄ B+¤ SB~Ð\x0011¼Ï\x001e:rzGH_¦ªy2bm\x0019§\x000b{Ê:BæW\x001c>%dNô½\x001fäJ¡|RÈ\x0015ÓóÚû\x0001ý^4Jµ#d\x000cÀO
9Ñ´ÒûAÆº`\x001dæ\x0004Ò @¢õ\x0003\x0010+\x001cfA3^
Ý\x001aUèön*Û \x001bIÈ¡\x001b(G»· î\x0015XÔgÎ¾|F \x0013(²\x0017¨´ÈIã@ISFg×n`do\x0002\x0017\x0018g\x00042[\x0006ÞcýÀiñ[¯Áâ>SryÌi ÌîèÚfs´\x001fä×>#\x0008í3\x0018g\V:±¸÷\x0019Á©w\x0004¶Þ\x00114\x001aÂW­óôåi~sôÊèã_Rl#âIÑÓ\x0014Q×SVÒ¤Èë·Îãee\x001bJ²oc|rC\x001eKý©ÜHzHú\x0014-jØxwR\x000e¯\x0008ÉîòÂoi\x0015¥\x0005ÿßmq_^Æ®±\x0007\x0005V¡ñ|&ïó¶oÎ°.)ïîÏÈ´ \x000c»óWSxËË´´ (ô½±3]X¦\x0019\x000cx¸[\x0006À!=MnÄ^@\x0001ø³[\x0006lÙNDËYÞù"%iô¦ÿÛÇE·Ët´]L_bÑ\x0008Ña_æ%h©r\x000eàTÎ¾c;8­Na¤W¼aå¥\x0011sÈb\x0019Óaäp¾É»yhYÖ0]Q<\x0012°5ú¢kfÃ)ÉêeÆ`Ñe\x000e4×Ê2c\x001dF\x000eën2­mÇöà¶àglfâl¥â
^èCçPµØC"­\x0003(úì´äeCL\x0019F¬\x0006´´Õ­IGáòÐ?\x001cõ\x000fq\x0018Nèmà`ÞF§Õ?Æqÿ\x000c\x001c±¥Êì¶ÖZxþ¡¹.ðÄý(\x0017Y©\x0007^*¶/OÙ<ÕOéo¤	½5or\x0012\x0006Yl6\x0000°I
½\x001eÅ0ç\x0000NàU»ræe\x0016÷l\x0018Ëiª\x0018íRX+\x0008ã\x0014\x0015Á"»½µÒÁGªØà#Z4\x0000yó2Xµ\x000c"ä:Y\x0002\x0018ªÕa Uk\x0011ç­ÚZQà
|\x0016ÛQSìCç3DM)å\x0017<v/ãØÝh\x000e§X}\x0005´\x0016ïßá*Þ\x0010\x0018FW)gprºk\x0012\x0000ô<ÒE2ÎÁvÃ¯j­ü\x000e¨Ë¬\x0018÷ÜWF»¯ã¾ò2bû.RI©Ó}¥j\x001d\x0006ê­òz»¶¶\x0018ü:ÑYÊqgUlmÝ8Ë9Ö2£S	\x001d\x001a¢(Ær²
È5Õ¨Wc~ëþv'à\x0019¯-FÁÌ8\x0008c.Ct\x0006þÃ4ÖL\x0005\x001bS2hRn72_Ô\x000bØ@B\x0012ø t\x0003Øß&¦Ù\x000e\x0019ï¤nGf\x0011!TÐr¢ñn¢2RÉ¤5é±±Ìáæ/<põ2çu\x00175JÚTºÌâ0SèÜ\x0006µe`µ¡¬\x0015´í¨´ð×Á8+pÁxn[§%07\x0013¨¿Âáv0²\ñZ§JËäs$DlÚ¯+\x0019\x000bo;Zæà\x0008´`Iõã­M\x0002kH\x0000H®G9Ì9Za¤¬ä¦PFº
N³MZò¤¥þ?HZêÑ¤ÇIQ5;\x001cÖ½OÚ¶c{XÒÂ\x001b·ã8#*çû'-\x0018¶*¬$Ë,Ø¼PÏ¢Wdào\x001ad)ê0ø­9j^ïrc\x0003dì5Î²¦Tz$³`ÉÆi3ôQçà¥úd"Fzlu*yÑÕRÆAzO\x001d
ÐÒçO×éhG8¦Õaä°Ú*±·êÈ\x0012<ÄfÎÄiè¡°
ÐËÖ9Î¡g1\x0015\x0017QR=÷
ñ±¡\x0005#¿IpÇt1æ´òÊ½· ­¼°\x0006:i~QÎà\x0017ç\x001dU¤Yªt·¨RîÜªäfò|FãsÚÜ¢Á-Îh\x0012\x001el[;p+V\x000c^[r\x000b\x0006·(ÇÜ¢E¶náÄ¨>Ö/©ñKûÁ/,§AJ5<C4¿·&:iQÎà\x0018ç%U¤\x0019ZëtÏ¨ZîD\x0016h^\x0000ÃÚ\x0006GwÚ<£Á3Îx\x0012\x001en[Kp3P×à\x0018ya;øE\x0018æ\x0016y¾{¥$¼k¢Ç\x0017v\x001eÊãÕré\x001c\x0008\x000bOÊ!¿©ü~¶4ï\x0000@»:§â
ø \x0001¯
§¡&o\x000b]¦¹N*YÆd+RD ìt¯´sT­.AÕÞ´\x0014\x0008M)5^7 `´©\x001aÖÂa:*ÍI&ï\x001d\x0006½"aÕÄÃ^!M\x0016ø\x0019\x0000b\x0006º±b^b\x0011\x001c\x0011Ù\x000fHÎ\x001c\x000b^|¶<Ò+/:üiìÀA`~a¶ª}ñ\x001e\x001c©l§)/¼+]y:\x001dø=7{c\x00181VÀÛÇ±\x00027ÈKÑÛ U\x001aº1V\x0016\x0019ªX'Uo+ -cEg¥õ\x0007ñP\x001bÍEÏ0ÒYp½Ø\x001anÿN«zl\x000b\x00166¹é}\x0010FÜ´lQZË7¶¹è¨\x0006¥\x001c<±ãc±u¢$g.3°KÆÃÞ8\x000fé\x001bí\x0015\x001b¸Sv9ÂÁh\x001b¢$\x0008Â!zFÏ
4'¥^L\x0002ÌÀ\x0016KüÑÐkL\x001e\x0011¯5´F£/ºVÆª(!7æ8Èì4W
\x0019Â1½\x000e\x0003Ç\x0014\x0017Þ®­-¸%\x0010\x0008\x001c\x000cëÐÊjÍsèm.UfÍ Iq^ôt´Ì)mÑ=ã8ºg\x001cKz\x000b¶·\x000cè\x001e¾@Û¢{\x0015/Yò:$ÊÄÉØ\x0008Ðï\x0018yMÔÓs¥/\x0006\+ê6+GzãHÈ\x001ch®Õ\x0013eÓì0rò\x001eYÛí¡2Ë\x0016:2Îa\x0000°¯([¢ìä\x0016Ý3]\x000cÝ\x000bØ¸d\x001ff¾q!ãþ\x0019ä¤-º×Û H]o£Óeî¹\x0006Ø²#jë)þÐüc8Ýã\äà\x0014u)3>n2À(à³Î°~\x0007bDIxÛ{ÆqÄÈ8þ\x0010½àÖ;\x0000Fî"ç9;^¨æîbwQÇÚº:\x001age\x0014¬3F¡Z\x001d6­E·jk	Çè´\x0005÷3àEQ6æ
xQç¼\x0005Ü+!\x0001Ük36[ïò\x0015¶ÍnÐ=ã\x000c¾RN÷MÀ+Î<ÐR±;«,Ø¥:ø\x0018+òé.wî+£ÝWÆq_y\x0019±}\x0017idÓµ«Ðªûªk­âz«¶\x0018|\x0015¨ïm°=ã¸¯
^Rm|å\x0001Û+Ø5;b{Æpl7@l°=ç¼\x0019Û+ØI=b{ÆplÏ8í1=`{D·
¶Gõæ-¶Ç\x0002\x0006l5k\x001dÚ#²m¡=â,\x0003´W°Y\x001b£·uM©C[»=\x0004Úó2\x0002í¹HöÆJ\x0005ÚëZ	²çJ\x000b²gÍrdO[îÈÞ`\x001aFö\x0006Ó¹e\x001dÙ+3V\x0008#²g\x001cGö¨V\x0006Ù\x001dÙsÎ\x0011²\x0007})íz$²7¯ü®üz\x0013å-nO.Ó\x000fÖ`$¹â\x001f^¾b\x001dF\x000eTï"µeÇÖ0\oæ]#®§ã¹0mÓ±û*\x001e}ñ@0\x001fëáü\x0003] u9³¼Õï¸r:\x0017"/ô\x0007kv`¯F\x0015Ã\x0000ì\x0011'ò)\x000e&V\x0014.X­J;´g\x001cÇö¼\x0002u]f§¹Ö\x0001ÜSÍ\x000e#Gt7Ö¶#{\x000cè^ÀÆ»8¢{Ê9\x000c\x001cÞÕ1\x0000|ÎÙb|sa[î¤.Æ|d\x0018µÃ@=k§Óæ#ã¸#ö4fo­Ô]dz¹\x000c³"\x0006ÚH§ÍEÆq\x00179GÃKeöðÛZc@úÜEô¹:§»¨:rá}ó¡\î#ÃûÜI÷YK\x000cà³:mN2;É9bQi\x0016·ZÝK¦{É\x0010ºîX\x0005ðºã;m^2{É9\x001a`*³\x0007àÖ\x001eú¹\x0014õs\x001f\x0019£»È¸\x000c\x0011Ã7bi\x001d±?å\x000cØr:²\x0017*1\x0003d«çÀÉ<É»Qk¨éA
f\x000cØ_/¢È^\x0017Ùé^iç¨Z]ª½ié\x0006û\x000bøÚ¤Ør:ö\x0017ÌüýnËýU\x001cæ³\x0001û#Nâ
{N\x0017Cºo\x0006ý\x0011Õ\x0010h\x0006ý
4ãPþ°\x0002y\x0001o8Ûü<K¢d4¾ä*\x000eý
:+ôç­\x0012èÏ[½±Ë\x0006ú\x001bl¥Ð_/¥Ð_jí\x001cl¥0Í6Í­´Í±?m¾Cn\x001eþ\x0006Z\x001bëöRkõ;­Þé\x0005ô\x0013nqQ{@þ¼a\x001aÔ\x001a¾1Í\x0003ä\x000fÍ-ù±È_H¼\x000fñzSô©!Ê1¨\x000f
biÔÉE>lê7à\x001f\x0006\x0006"åò\x0016þ\x0016Âk\x0014úbÐJ8üy\x0019EñºÌNgù Ó9¢×aä¨â&ÓÚµµÅü\x0005Ùö2 ¡oé\x001cri\x0018¿ÎxñÈÓEpâÒxtSßóHêµGíýJIÿ³k<\x001d\x0017ùZúOÏÎðå\x001cÚîg¿}ÿ\x000cA²²¢\x001esÃÖ_þ&÷M\x000f¿m§¤e¿vþÆqðÒ8ý\x0010µ5âCãûq-×¨ès\x0012#¶¶\x0016ÀÇêXÔÛZÀh_\x000b\x0018Ç×\x0002Æ±¼Þd:-µúZ@\x0015;Y>E\x0012Ö²ckèZ\x001eç\x0012}-`\x001c_\x000bà|\x0008yùÆEÜBªJG.i§7î£zà\x001c\x0017cÎ1±7AQÈÞD§Å9Æpç8G
©"»¡µÒ\x001fs\x000c|¬Ô\x0003\x0017) ÖÄ[B\x0014\x000c[WÙáüv0
é.Aî1äÊ8l\x0011-;M®6g	G¬å;9ÛSe½cGÃv4Ì8y\x0019F·\¤RgÃL­ÃÀP½E·kk\x000bÃcd\x0014ü2Ãa´Ôè 7B\x0019\x001fPðª·ð$¾@}»·¨P¶\x000c¤a{Ë8Ýò³àQNr½³\x0000mÅ0Úà¬Âó¶;KéÁYÊ\x0019ÕËwºH#ÓÆY¦Öa`Ú*®·jk	÷U#c`î+ã\x000c¾Â§¦[_uÎ\x0000]Òêµ`î\x0008£1\x001cºL+¦°\x0001¹ì7\x0003	Û\x0016$­éb£íæ\x0014àÒ8\x0006\¦U1\x0003.^ê\&¼Ð\x000f=ùÎI8kîÈeÂÙ¡Ë=\x0003s\x0018 Kæ¬Å K"u¿ook1H¿7¶ØË
.½@.R Ë±R.]-Á.]mÁ.­a]Zã\x001d¼\x001cÌÃàå`>·®ÄY4sRðÒ8\x000e^&|ê¥ï&\x0004¼tÎ\x0016¼¤¥|Ø\x001faí/\x001flæi²\x0000uìÒ8]\x001a§'\x001fm]Ç|E+>ÎWÚwæ+ñ(_\x000f¦Äø`Jß1%¶aJTÅ|J4Í»HmÙ±54_¡òi;\x001f\x001açx>\x000cÛ|%<À.óoÊ\x0006rI­|\x0007vI¥hÊ\x0018 Ke8r©\x000c\x0003!l\x000c´;ÍÕ:pÓ£,7ïAq\x0013OçÜK£\x001d¸4\x0003^F@HÙé&ßawjv\x00189¢»ÉÔ¦mmá°e^\x0012\x0010Z*ÃAKª\x0015\x0007,
 ¥s6 å#½£0{§KQç(¼h-Pô±7ÐisqÜ9Î\x0011CH3´Vé¾1¥Ü7.ö">vNoã¾qÆÊ´°ÛXÂñJ÷î\x001bc¸o¬Ì±o\x0014­|¤s\x0014sç(lèÞQ\ÑÚ °co¢Óæ\x001dã¸w#¦4fj«ÓÝcj¹{\x0014Vt
ìè\x001eï´¹Ç8î\x001eçhd©L\x000b¼-:PéÞ\x0011XÒ£´ûF\x000b\x000c®QðÖ6\x0015ß}:Li\x001c)c $Ñß+:­g:§Í¹Æ)y\x001dM\x000fWêj\x0008ÃaJ/" ¤4Ú+í\x001cUË$Ú0e^rßCP5Àc0%Ó²\x0001n\x0016¡LK,"¬
¾\x0011g×?FSXù\x000eE\x001cÅÜÑ;þ5)tÇ0å@\x00034\x001b\x0016\ThöR¹ªy3/I\x0006O	\x001aJt¥\x0005§\x001cÅ8åÐìaFr4à^JpJj-\x001d¥¦0Í:­÷\x0012ÍÞ,Á¥ý\x000eTº\x0004¨\x001chmí`1µ:ÀHó\x0015\x0010\x000fv Òôv rhÙÒ-:éØ6Ç@%·\x0017ÿ>
¨¤R\x0001Hêõ(9\x000eT\x001aGqGV äz;PqÂÊZ\x001c¨d+å:¹<²b¼B&/\x0006á(e/ £Ëë´\x001e\x0014â\x001cÑé0rTi\x0013imÚÚÁAJ\x000f9ÁC!Iã\x001c\x0006\x000e¹3,\x0003Jé¿6L3Z]¾'L¾\x000fò\x0018ðÖ¼È£r\x0006äQ9Ãõ
|ÀÎ@ëq\x0019Ó(;T\x0007Nµ,'º O[*o´§òÆñTÞ8\x001dªR\x0003\x001duªqT³ÃÈaÝ»LmÛ±=\x000c{Ô*\x0006lK9Ë§&EÍå<Â\x001eU\x0017\x0003\x001fñMãú]\x000b-w1÷tìÑ`X£5ÑiuOçt÷\x000c\x001c1¥É4S[­?8÷tôñQ\x001eê¥d°a#&\x0015Ïª¹ìównÅKØ\&ç1¸\x0018æ\x000cè£r:Ú\x0017"|vA§«¦(Æasù~à\x00065fp«Õd¹\x000c-ìe\x0004Lì"ä:\x001d}Tµ\x000e\x0003CõVy½][[\x000cècH¼/g@\x001fã¸£
sÞ>&â8û&W*ÞÜ¥LÃ\x0018ø´ëQLÑOæÍ²Êé\x0018	ÃH/úy¿q°²Úz\x000b\x0007ÃÞÊà\x000fÞRzðr\x0006oõ2bü.ÒÈ¶õªu\x0018\x0018ª·ÊëíÚÚbðV|\x0012äà-å\x000cÞÂ*së­Î\x0019ñÇ\x0006\x000f@¡2\x0006ü1Èé\x0003\x0000Ù9oA \x0003æñÜ¤+xÅ\x001fÑáGyuø1\x0010_-¯ðcXyOáG¼iÅáGè\x0016\x001fñRTÁc\x001fñ~:Ö\x000e?\ê44µXrÚZ,íSø±Qø±Tøq¨TáÇ®Â]m\x001fµa\x0003ü¨\x001fàG7ÀÝzÝ´\x0003ø\x0018pË=
c\x001e\x0003N¾ª#ôØ9[è1áN\x0007+û(ìJÅ}\x001a Ge8ò¨zTZ
]$yÞ¦+ñÿKº\x0012ÇùP5;$gÕ©LiÚ-,Y©8\x000cn	ñýS\x0015ÅîRÅiÆÜ1If}Mêbæ¾ûABã\x0018Ht×¤NûñKèÔ*\x001fez\x00189|Ja\x0017ÙÈ#ËÚqG£\x001dw4ã^F0DÙé {#\x001dFhn"­eGÖpà8Eaa\x0005\x001aãÐcjeÑÕê
ôø8\x000f)Þ6x¨K1\x0007)PØ¡@bo¦Óê c¸#Æ4fl­Óýcj¹\x0014'ìE\x0014Gì"6ÿ\x0018§ûÇ\x0019\x001aY*²GÞÖ\x0016\x000e>\x000eþQ°qðqÜ?VêØ?
?>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-eleves.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-eleves.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=+*ìnskGÃðÏ¨ÖyCÄÊ÷;\x0005Å 8\x0005î»}¶ynnÿ	BsÐñ±ÐÏ?D(í%2m¾\x001c>ú\x0010±(ÌóJûXìÇ\x001f"4Ðî\x0011©üó
¥\x001brØ\x0014ý¬¡
(18\x001f	ýìb9Oéq¨>HèT¶¹>Öô¯\x001f$\x0014\x001b\x000f\x0014\x0007?³O)§êcóßT:É-Ú#©_|Pº	\x0001Ö#U_|Ô\·oÔ\x00079nC`ùz$ô\x000f\x0012ZéÔÏíÓÖàÇ~ÐìG§\x0003Ãc\x001fü6ò'Ô\x000f
SÂ7¼-¡>LhÆz,ô\x001f$\x0014I\x001aÇÇ±gMÏÈ7KlÔH?ðÁ\x0015:Hòçø³n¹Ê§õ¶tF$\x0014Yæñ'\x001d¤\x0016)ËeáWZj°r¿ä?ûW¿à9DË4cñÇD\x001eYH[	\x0001#É$[dr70e~Á2U7Ú½Gü)ÿk
)fúý3mò£îÈ\x0012VÜmEÛAJ§¢¾\x000b\x001bª\x0001ï\x001e.¿½Ýÿ´\x001bÕ]?¶\x0010Ãtn¥Æ©ÅãË\x0006"dÚ\x0014­·¨O>ûô\x000ey×´ð\x000e7Ã?t\x0019UÂ2\x0013&\ëRénNt;"âvB
Ûÿ4\ÓögÃ¯nÐ&Ñé8Bí\x0012¡Hð0¡\x0016ÌA\x0006C8Ò¹äopýÂGn&Â"ét!|%,r\x000bVµ\x001e¾±\x001fXñD\x0007é®4.ÓTé\x001c\x001fy\x000e1*\x0000Q©\x0017Ú\x0019®üSèH#ÝØm^\x001aoé6Î\x0001ä*\x0007ôLp8è ëåÀ­r\x001e\x000bñCðo\x001cT&ýt\x0000T{Uzg)ç\x0000NäÁ©\x001cÐªL§¥W!\x001cÕìÐsXw©¶\x001dûl\x0001\x0013Áp3ß\x0013¢\x0003ÈÙ\x0018\x0007eÐ` +\x0007kã\x001cJ4xGÓí±¦O\x0008||º\x0012½HBü\x0008uRZÀA9àF`7H¸\x0019ét\x000br<@ÎiÎ\x0014æëÖçß^| ÙD¨ðSâ£m\x001eÇ'Ì\x0004îNt!,Ã}\x0016Ý» {ý¿+Bc¡Ãâ\x0013aã
¨U9Â¡\x001e\x0003Ï+Ê\x0001]P\x0017PO#ßMp:
R¯>DÊÑ\x0010Lñ7Ëà^ÞfÊ!W|XÖÚL#Mª]ö\x0018	G5;ô\x001cÑ½É4ÛüA¶D>Ô\x0016"SF¾ñ§q$&3Û+­óªóìB+En±1J\\x0001L:r\x001b×	§\x000fp<\x00003O¨NKG\x001e©bï1/]@Àáb&³bÆ/\x0005Di\x000fr< ÖF«2.r/×Ý/õ\x0001iº[@mGþè\x0003²$º'Ó\x0007D8\x001e\x0010ôäÎµ2\x000e\x001bÐ,?Ò\x0011\x0010r÷4»A-S[`Oõ\x0013g	\x001dùõ[\x0007É
\x0016G\x0015\x001c,e¡´TN¡$9\x0008](ô\x0004
Ó¸®í\x000b=2ñ½K1\x000fJ±6Ô`\x0010V®d¦'>y.ÏÑÀ\x001e\x0006è¹Æaâ\x0007\x0006¦¨­DîÌT¢Øð(&´«	Â)0òßÙÂn¸6t »² E²È"OB1{©Ã)Ë\x0004©\x001eWå¼JóØÚË,#Ð©\ÅïøÆ!©sáÃJôìL\x0014ÃR¥)Ù9\x001d²´\x000fu¤z8Q\x0019TéÆa¤\x0012`ÑC£DÿzY¢\x001c/Kc%Æ\x0018¸ÿæ¸,Iÿ\x000fÊôeO5;ô\x001cÖÝd6Ûýáe	8ï¶ì)ãIe	.ÉSôä\x0018þ¥È¢BÕß\x0011#Ê\H¶{&9:CNÆ)ôä\x0015\x001fËüÈIGsÏ<Ë
'À)ÆOÆy0ôPZ\x0007ëµÑ;×¬q\x000em\x0014Í]\x001b:3w2^YpfÓto2Í¶µ?Øj¨1#ÌrÿvdÆÁ\x0019T\x0008bJ:X\x0013c´\x0008e>ðüÔ\x0008Ñ
ÁYd\x0011r9\x001a!:°QkVÐ2\x001f\x0017·Òir<BÆiÞTêmíÕ#¤yòÂÒ¼
¼\x001bC'Sir<BÎiº7fÛÚ\x001fl\x000b\x0018ô\x0010eT\x0014síB¤\x000c\x000f¶9Q
üÜe\x001f#ß\x001f"Ì84\x001bv!r1\x001a¢\x0014Ú9fF
t«ÂÍtZC¤\x001c\x000fq;U¦º[{õ\x0010©f\x001e":\x0013r×\x0006cÊL¥-DÊñ\x00109§éÞdmk°-v´\x001e"l¬»ø0åÁÑ«»à\x0014:ÓCUðX\x0017úDÄÊ\x0000ZãP»È°)\x0007t;¬2óª\x001dÕ2F¢uÖ\x0005ðÉ¢Á»\x0010z×©!\x001cê\x001eÄ
]¹ø6Fk§ÆhZ©\x0000Õzmé+æ:ÇQ0$Ù '§É8 ùac¦é\x0014\x0011ÑL¡C\x000bJÉ\x001dU­Z2U
õÈOív4\x0014\x001aº\x0006|wE\x0004:\x0000\x000fN¡¥§ði¯ØÓÊß¾Eåãìuè!w
«ø)J¥
\x0017£gÊ!oazWÙÌ¸a7HnøÊ5â.To|\x000eÏÝú&°#u\x0012¡Þe\d!Wn:k\x0003±Dj\x001f$>¥s
=ý0÷´Ù»nÜ¹÷lÁ±\x0006£\x001f\x0017oWUû ±ôv%Y·ÍìWv¶.¥ Rèá\x0006:dÏgkåßw-J°náVüÊV¯ÒQ>;)\x001cÐ3U£Ò÷ÔÓÜ-Íâ^åIêÉtI>Ä4(]6bç:5\x000e	óòÞ\x0000>,s'Ðhîe\x0008§©uè9Mñ&Ó\x000c[{dÀí<2§Q\x001erÅ5¸+çà\x001cæÈÛ?meWO|L¨;#6¯nÝòóÌÔ;uYÛ]r¤\x0016ß$ÿëKº-=¡n>úodÏK)!¼\x0007UPTÃ9(:cöDÝÍ)£×dÂVéùävM\x0018§¶·«\x0012½õ`öèÉ°°¼\x0015]|zfOI\x0007§Ç2	\x0019Vè*ÿ@\x001e¨´ç3ÛÚ¸ðÆH^(V?\x0012]-t«Z÷0BùþIÝ\x0014Þ÷Í=ÍOß¼Lô"\x0001Ær:ÎLye8-ÝsbÜ¾wQï]#ûl";zRHI8ªØ¡ç°ê*íZyÀw-\x0012ì»\x0016eØ®\x0005=fÁ\x0018\x000c5Î\x001aLUM\x001a:Óû\x0002 úû7-"ê8ªhÎhp³n\x0011QG¤ãû\x001a.«ÞUàöo("
>%"\x0006¹>à]<EUÃæfz$`ù!ô\x0014\x0018E¹êÅ\x0004Ýz	°¦\x001c\x0005Þ
=L\x0016cO')\x0014c/õP\x001d»±:Tg¡iP]\x0017\x0006u¡i°¦Án*ÓiêÔº¦Ö¡gÞM¢Ùuä\x000b\x0007ê
\x001d?Oµ\x0003êÓ\x0001u\x001cÜ\x0003uÆqä´àGT0\x001aDwÒË\x001a7-ü^U(\x001a§\x000bEãë\x000b\x001dó=\x001d\x001b Õ\x0018\x000bÒ ô868E7\x000b\x001d©w\x001c[ir<\x0016ÖF=«2NòàqD±CÏ\x0010ÍU¤Zvä.\x0018¥pÁÜ\x0005£q<\x0018èÎåuÁpÎ\x001a5Å\x000e\x0014rp³1\x001c5edCM|/j\x0004±(ªàjQ\x0014ÔT9¢ë±%	£¦L·ÉNPSA[:Ô\x0014J»=MY»j¨)\x0003\x001aS\x000f²?Ã¦ ðÕZ¡wj­z\x0003N] C§}J\x0002ºÆ6\x001c;U«\x001d;u¿\x0008vê~[ûÚ±S´Ð\x001ciØ©r\x001c;åÐöS:gb\x0002Nüf§`§hÄ·t®:)Ìèîè6U\x0012aâ»B\x001dÍý\x001eW\x001fÿ\x0016ÅG·Ò©ZÓng5Í°c_t·séíPãÔÝ.l£õ.?ª@òp¢\x0013~îi¸é\x0014æY$Q9ÂqÜT9¦CÝNJÇ\x000eNô²X;Ø\x0014\x001c~=¤\x0017S-É`S¥\x001d6UÃ¦ÞF Pit{Î8M³CÇiª7fÙÚ\x001bBB²Gh\x0016ÉFá8n:Ñ«Ú\x001d]id5núÄ\x00085°É±\x00085Óìh\x0018¨i¤EH9\x001e!ç7U¤z[;õ\x0008©b\x001e¡\x0006qz\x001b@]¦Ñ\x001a!åxÓTo"Í²µ7\x001c5íBÔPÒ.DÊñ\x0010i«ã\x00185è±ÑÆM»\x0010\x0018\x000bQÃ8ÍªFZã!r¸SEª»µS\x000f*æ!j\x0010§·\x0011\x0008Ôe\x001a­!RÈ8Mõ&Ò,[{ÃQÓ.D\x0004vñaÒ£×wÁQ4qØZOK*ÇqSå(,:ÑYÒyîéEñ\å$)»LBâWÂy\x001fBï:=ãÀ©·\x0011\Ôe*í½\x001a§é¥\x0012Tïµ­=r5%éR.È©r\x00149\x0005-¨PCN\x0016T¨á}SÌsC\x001aT
ÎB~pº\x0004.>¬E± I\x000eÅÂÈb§\x001dÍØißB\x0010?è1ëù\x0013ÁJÁ©ôÐeG\x0017ê­ka×¶1ÛªìÌöwzð´÷\x0018t_®\x0015ã§.TõnÕ\x001dªÑMqk1ëá\x0012uzÑ\x0003*\x0014&HÕA vt3¶sXs\x0006Ai
¶0*:æ¡æÞ¶$\x000b®¾rN¡ÍE¬5Á§ô²RúW©÷Á¨h\x0015)9®z9Ìq$U9²ã.ÛÒ\x0001©pÃØî!;_%à"Ü¶NK»1ív£^qOo#¸¨Ë4{u,µ)vè\x0019Ms\x0015©­½áP*çI:(U9«âÆÚJ9?7J/\x001cCüPjt(õ-XfüÀAKaç¼\x0015Ê\èYjz
ÛÛòn¬AùÇBÚ§í*á»
åè\x0016!ÓnVdw¦\x001aÈIXc·©(	0UÛT\x000etJL\x0001ÔFú¦B9¾©PaaM¤ÓÜ§o*T­CÏ!½U¢uì	ßSdÞ\x001f\x0014ßS(Ãö\x0014ß-Ö£ÎY£ªNC5\x0003½8uú¡-\x0007ÇÅht\x001a\x0016iV4¨Rt²\x0005ÇðN
3'\x001bXªV(õo,8
V>%8\x0006>
 S\x0004\x000b!\x0008
¢\x00113[y7æ,@RW\õrã°r\x0014#Ëô¢èîx¢öÜáj\x001e\x001fe±!/ÓÊÙ
«u\x0001j\x0008W\x0017 Y\x001aF¦2¶\x0000	Cõ:ôÜ\x000e\x001f²H³ìÈ\x001b\x000e«åöþiÕÓÁjòr¾\x001eV3cª½èñ¡7qLqY£^/QVáh.\x001ccî§2±¦Î
¢TÎBoúÍ]<À©
(\x0013\x000b­e\x0016Fz4\x001aÃ¡
Ô±*ÏéÒî*§iuè9¢·T»|Ñ\x0005#U~Õw\x0017Æñ`dzxè1Nç¬1ÎLO,ÅÐaÊq3Óaä\x0003á~N¾\x0017å\x001c¢I¶(
Ê©\x001cE9f8CPÎLo_/Kr¢\x000c\x0005*S\x0013vp[`NVOaO\x000cÐAëQÁ9ÁÛ
çÌôÒÀ1\x000e½I\x0011\x000f±7)ø#8§7â\x0002\x0019çì{\x0014Óu\x0012 Óu\x0016 S­r¤S-w¤Ó}#H§ûníoG:ÁÑLiH§r\x001céDÏUá A:³B:K¤Ýàü4¤\x0013\x0012!\x0016W\x0014ft7Y\x001bÇ*\x000czJìÉ"\x0018Àª&	=Òùÿ«(	=Ô©\x001dz\x000ein"aÇ¾èîµF*á»O\x0019OªJ\x0004,,´cZt\x0016*ìSèNå8Ò©\x001c-\x000bm\x000eJOrÇt\x0016ºñ_¦\x000eé,ô¸¡Ý\x001dd:ÈF¬uÚhG:ãH§·\x0011ÔÒe*\x001dõ(¿rf#ª7fÙÚ\x001bt(¯Ow¤S9t2J2wH§3ÖHç\x0013#Ô°½.B.G#Ô`I³£Áj¦\x001a!åxÓ¼©"ÕÛÚ©GH\x0015ó\x00085XÒÛ\x0008jé2¶\x0008)Ç#ä\x001cQ½4ËÖÞp¤³\x000bQÃ5»\x0010)ÇC¤­cÔÐÂ>F?\x001aéìBäb4D
4C\x001al©v:©!RÈ8Í*RÝ­zT1\x000fQ%½ .Si\x000br<DÎ\x0011ÕH³lí
G:»\x0010\x0011´ÙÅI\x000f^ß\x0005GÑ¿Bw¹C:ãH§r\x0014ÇÄú?¶\x0003 Jóç$\x001cé,ôÞ²àHg¡Ê8ÅÁû\x0010z×é!\x001cG:½à.ÓhëÕ8M/ z¯míÎÂ\x0010ôÔ!ÊQ¤é\x0012
é,\x0004b¹C:9jèNN¥ZN­0Ò\x0016Y^\x0004§H'Ç¨$C:;A·¾\x0000sà9tHg¡ÏbðÛså¨¿¶pÍ\x0005éìlc¤³³}å\x001eéì=&H§·b¤Ó6c»n;L1£âÚBLs¤SÍw¤Ó\x001d$HgGÏmôºÃÄ\x001d\x0016\x0004£[¬Å(ï4§7Í\x001déìlK²é+ç\x001c#,©®Î\x001f>0Vü	«^No!),©\x001c-Y\x0003ÙnïÙ6NÂÒT;¤]E.TäÊäH§Òt*ÇNo#°¥Ë4:nk\x0007tª^Ó4o"Í²µ7\x001céä<É=Ò©\x001cG:9ª\x0012Cmeããü-¦Èø\x0013=N\x000fµÍü\x0015\x000eb\x0014>A\x0013A\x0000í)nZ&ª\x001bÂX\x0010F-X\x0013<¦+ÞáÅ»r´\x0012gÉsOÎòÌA\x000e\Í]ñ\x000eN!°Ç0Jú UÎZ¼+éÅ»r¼xW!PMdGs§^¼«bC«H5ìØ\x0017^¼'úüÏÒ\x0015ïÊ°â\x001dÝ¶ó1\x0006C\x001ag
)ª:zP¦\x001fØYyp:!
ô\x0008þg64xPMtrÖ§²\x001aÄhÁé8âÉ\x0006Qª£\x0015Ãü[\x000bÂO	Á#0\x0010¿x69d5Ã5yzgQØp\x001btÈ_ºêä\x0008Ç1,å(\x001eèSsêéhû\x0011A¬ØYµÇ°ØÙ1,vw\x0007b5ºC±\x001a§±´bR*ÓéÔ\x001eOh\x001cÕìÐsD÷&Ól;òãXÊ!)é\x001aj¥\x000eÇê¢Ôp¬.JæÙL/Kö\x0008Ñ^½£GÎS¦÷æö ¢rº4\x0005 gþ´ÓÒ\x0007$Íã¨\x0007\x0000#÷ÎTæ<Jy®½6Ú\x0003¢\x001c\x000fµQçªL§¹×. M³. ª»ÊTÛüÑ\x0005$\x0017>aÐ\x0005¤q< _²Rº8g
,&(©w<\x0004þS\x0003)Ë\x001aÕE'ß\x000b,"M,*¹Z$\x0005XT\x0002LO\x000e,^ä5ø
,¢óÒ\x0003H\x001ftÕEV/9°è±ìØ\x0003\x001fív`éêÀ¢Ò;³wQ,SEo À¢\x000bd`±ïQE×IE×YEµÊEµÜE÷\x0000î»µ¿\x001dXD$5S\x001a°¨\x001c\x0007\x0016\x0013!\x0007©\x0007\x0016³\x0002\x0016óÔ¥Î=\x0005XÌc®¢I\x0011Fw³³q¬Ð\x0018ðuîhé÷¸8©ÿ\x0016ÅIío©5Åº[jMuÙL;öFwÃs¤m{÷Î\x0015e<©:\x0011t.?pÚ\x0003Wó;\x0003Ô°44Ê=Ü¿c2Â §ö\x001c¹ÒU!½Æ	_<è9Y&3ÐÇõèp2Ú¡Eå8´èm\x0004&tF'ù¼qfÓto2Í¶µ?\x000c[Ìü¤hê°Eå8¶é
í¥\x000eÒÈ\x0018klñi!j`Z\x0017"\x0017
(c\x001cÐÌh8¡é´H9\x001e"ç;U¦º[{õ\x0010©f\x001e¢\x0006\x0004z\x001bÁ	]¦Ñ\x001a"åxÓto2Í¶µ?\x001c\ìbÔ Ä.FÊñ\x0018i«ã 5®\x000fR\x0003\x0017ß\x001d£¦u1r)Ùð2\x0006\x0002Í\x0006\x0014Nkã1røSeª¿µWjæ1jH ·\x0011 Ðe\x001a­1RÇÈ9M÷&Ól[ûÃÑÅ.F\x0004'v\x0001bÒ££×wÑQÄ-\x0007z\x0016eêÐEå8º¨\x001cÅ\x000eAóñ²\x0014~5NÝúóç\x001e¾_®YÎÎ»\x0012³<\x0011ÕpAk °¡3Òú3NÓÈÚ7×Vö¸b\x001eéÛP¹Ã\x0015£¸"èÀÇP\x0004ábr²¢°"z7m+(\x0004'Ëô\x0016n'Ê­ÅB\x0007ú\x001dVÌôF\x0016yÒ$ÉDf«o!(\x0018ô(íIåù&££¶°\x0016¦¹Àn\x001a£å+ßô¨bï/A\x0015½\x0015£&³ÚuÚaj\x0019ÝÔ¶\x0016Eì07ã\x001dTt÷\x0008¨ØÑbjï.qÀè\x0016"kQ´\x001en.o;¨è¦%Y½Íðk1E68Õ'b\x0018ÇK{ïa#¡è t¿ôtT4°qèCåí&Æù$¿-Å\x0010E¥\x001dQT#ÞFàAitÕW«4NÓìÐsîM¦¶ò\x0003#ò¾\x0006\x001f*Ç\x0001Eô[ü´q~¶£t¨\x001e=Ã7Ê7»ÎFþ\x001e¤¼«½½7\x001d%ÐC{ozÅ\x0016}ÌíÅés,òât~×z6ÃG\x001füü³}ÎÇ+éÎ\x0013}=ææºBG2/~¢Ø\x0017Ï?ùâó&õ§¾¥~ýy&ZÊèÆ(}·h©ò\x001eTù\x0003½«U>Îò}Ú´Ï9\0g+Øþ¯©ü¤\x0006{\x0013ìÛU£Ïýjüå\x0008ïV?ÚÒHú\x0004\x0001«ã¦}/âçq\x0013áÊným¹©©F;WSíØMíK7¬!};Ø¿±ºïÝ\x0014èoôõxúRb%h"Ð»Öè\x001bï\x0013è\x0005\x0005ô6¾iO\x001f\x0018/tJ\x0012dç \x0002½³\x0011\x0003-±ÕfÔy\x000b\x0003ÎDu¥Óp\x0011\x0015oì \x0003UØ3Å@^h\x0016\x0008>@%âtdX¡o!Gú® UMÁ\x000c\x0006Õ§¬\x0006Í÷ì½ÊïÁ\x0003ÍQ§3«£- ´d.µÀaØÃiºs²t-¦(pZ GÚk4wñ\x0004ØÎ½¿èIÑÎ+ó¢\x0013È-A^\x0017hæCÊ	ôé¶ ÖfòÇBó-è,\Èrï\x0019Ê|\x000eübEoA¯\x0016Õg~_Ìg\x0017fZ9;\x0007å¥JÔa#?\x000b£-Èa#}ULü\x0007#Õ]z=¹»ÌÑt¦þ°úÓ×uÍªDß!ê­^ùE|%{¯>a±[z\x000f\x0007þî\x0007> [ú¥×'Ïs±i*âï±F·µ\x0016\x000c$WÏPÂÆØÑt¼8¬2ÞqEzbzc°\x0018Lé\x0005\x000eÝ¤prxÄYn¨-äx7
ëD,½é+ç´ïö%Áýü5\x001eÁ$·F.\x0000º÷LOrG-¼óë_ü½¿pôÝ\x000c
n ÿ\x0014ùúeðÏýýâ\x0005\x0014ÿê\x000eý_K¡J[endstream
endobj
257 0 obj
10248
endobj
272 0 obj
<</Length 273 0 R/Filter /FlateDecode>>
stream
x½ËÎ%I¤·Ï§8ÜE\x0012]ÿ¸]ü6;\x0012
Ñ\x001b\x0005n¦¹ª\x000e .Ù\x0011Eò5ú	g9ÅWàfTDUTí\x0019n\x0006
tY\x001c÷ßÝÌÜ>S\x0011»üëc{k
ÿ\x0017ÿýðå÷¿¿þøe{ÛúÉÙûñý¯¿´½½ãÑ&ÿ³\x001fûýÖïÇ±õ·±Û\x000f>þò_þõÆ=â?\x001f¾<þç?ÿò'»ÅãÏ\x001fìÆ{Ç¿üù/¿ø\x001fk~Ú¿án×õÖýêË/í­\x001d?ÿ_¿üÇwÿÇ¯½¿íw¿Þ}ûùýããÃû¯¿}úíýÏ?ìÿ§Ç\x001f_\x001f?~¾ÿëÇ_í\x0006Û6¯ëÝãýãïHÙsóÝOüïyqã_>|øXÉßúïÎý¼Þ1ÿ\x001eíïþáñùýã÷ï¿¶óíº¶ûÝ·\x000fÿRÿøþÓ×uÕãï?ßÿ¾Üò±ÜæÇO»Ï¯Ú­\x0000¯ó~÷øõÿüóÿòKë?ÿã/\x001b^ìÏÿã|÷ãÓ_¿úüö\x0011õÃ·¯[n÷õç§o_ß~ýÓ¼í\x000f\x001eÝÃþ×u{ÜÍJrì\x00137Æ=ÿ1nÃq_Ïã·o~>þ_\x0014à÷_~ÿüéãããÏ\x0007þþß?>`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=T(#%J636lS.2E9gGp-S'@'5];hno_</p><p>IunL6Gh-Q-C45eD@!)4u5WUmP9E[]ncs$&\Nga01?mou9"[A*(HBopV5sM088tZE+</p><p>8(5lH52)AcG'7<<gf#p8bV.eos/=$;C`$=qD(WDrjfA]lRYim,RqrACdejgO/AF>(</p><p>/:tg]_t>sDIL8P<ndm?OOg2bg,-Em:1jeEn-[97]R[[bI(P]d%f!I;eeb'o)qeJ7,</p><p>B.cOqT*d(nYRO5hkDtb5$C0au"Tu@Gd5re*4LT0a7a1s2(FCIYl*Hscd?$6a1aIjm</p><p>`#s0m!>?_.0o<c)d:14=0]UGQjn;]0qKM`<7PPUaM-O)AhPTW$':M2&0_hHReg`^d</p><p>7R:TK-mVk@qM%4_RD&Zoj*$-:O\,P7G8CNp$hFmd47K<8U_e8pRSKd[0+J5ELBKfW</p><p>9L7',Oq*H#neRo8?p<q%gkY'iJ^MpD;p9Z&0HV^R_Q8>,=2iEcr<Rg<bF`7PF$4(]</p><p>7=;9#?7M7#FSgN'HKh'jS#/aY66j[4MXrY:L>ZOF;(Wn!kIE`M_?jL64MdEt,m)Yc</p><p>q)k2_XWMBFeot(QWg#\eAS8p.1#t0Oh:R&-2fIWY4$4OTG4i"eHMFCbG%eAR>[fpD</p><p>DUAgu&;"Vg$-7)+o:(\%WDg[DHaj=nPCQTMYbl%pT"7k`gGf;5csf#*;r&)CH+o&S</p><p>,iC5aJQd)D_edC]SdIK.>-h`N(pX2/]qhur8]&$Vfr@,nVo+@bQqo[;hEa5/e+dSU</p><p>r+qq.!4%H/QLeg@]Q7`s:MnoKRc*j44?N\<_*jGI1b!)b'6*q4!7^H/3W~>
endstream
endobj
363 0 obj
<</BitsPerComponent 8/ColorSpace 243 0 R/Filter[/ASCII85Decode/FlateDecode]/Height 74/Length 898/Width 104>>stream</p><p>8;Yht=gir*%*^G4G5iM&4&7"b7LWDdH.UM[.3p1*%.=!D[e*/GoW!24mC6KLF/o$H</p><p>p3`V+%Q2YE''\'1:9K9-l24&s/bZuO5L@E$h>/oJ-qd@`=`@5g9LpcuIZsmteEn[l</p><p>MR"c_mp'jPLS$@Lp;?48*kW^2g7J!48]XJC'=-./.-<F:16<p$QJk-biV8T01k(,X</p><p>6&m@BfR?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://d2uvddcac8vf0w.cloudfront.net/packs/css/application-5eb3e6a7.css" data-turbolinks-track="reload" />`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://d2uvddcac8vf0w.cloudfront.net/packs/css/application-5eb3e6a7.css" data-turbolinks-track="reload" />`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="shortcut icon" type="image/x-icon" href="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/favicon-d21ba7166343077ed001c60d663a06e1.png" />`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="shortcut icon" type="image/x-icon" href="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/favicon-d21ba7166343077ed001c60d663a06e1.png" />`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="all" href="https://d2uvddcac8vf0w.cloudfront.net/packs/css/application-5eb3e6a7.css" data-turbolinks-track="reload" />`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="shortcut icon" type="image/x-icon" href="https://d2uvddcac8vf0w.cloudfront.net/packs/media/images/favicon-d21ba7166343077ed001c60d663a06e1.png" />`
  
  
  
  
Instances: 9
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search?school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers/search?school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" id="mobile_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?page=8&school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?page=8&school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="" id="mobile_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="home_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?page=2&school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?page=2&school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?page=2](https://www.monstagedetroisieme.fr/internship_offers?page=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="home_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?page=3&school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?page=3&school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers](https://www.monstagedetroisieme.fr/internship_offers)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="d-none d-md-block rounded-6" id="desktop_internship_offers_index_search_form" action="/internship_offers" accept-charset="UTF-8" method="get">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "checkbox_144" "checkbox_145" "checkbox_146" "checkbox_147" "checkbox_148" "checkbox_149" "checkbox_150" "checkbox_151" "checkbox_152" "checkbox_153" "checkbox_154" "checkbox_155" "checkbox_156" "checkbox_157" "checkbox_158" "checkbox_159" "checkbox_160" "checkbox_161" "checkbox_162" "checkbox_163" "checkbox_164" "checkbox_165" "checkbox_166" "checkbox_167" "checkbox_168" "checkbox_169" "checkbox_170" "checkbox_171" "checkbox_172" "checkbox_173" "checkbox_174" "checkbox_175" "checkbox_176" "checkbox_177" "checkbox_178" "checkbox_179" "input-search-by-week" "test-mobile-submit-search" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19543](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19543)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19542](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19542)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19541](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19541)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19540](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19540)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users?as=Student](https://www.monstagedetroisieme.fr/users?as=Student)
  
  
  * Method: `POST`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19544](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19544)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19539](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19539)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19538](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19538)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student](https://www.monstagedetroisieme.fr/users/sign_up?as=Student)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19537](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19537)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19536](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19536)
  
  
  * Method: `GET`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users?as=Employer](https://www.monstagedetroisieme.fr/users?as=Employer)
  
  
  * Method: `POST`
  
  
  * Parameter: `split`
  
  
  * Evidence: `Set-Cookie: split`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up](https://www.monstagedetroisieme.fr/users/sign_up)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  * Parameter: `_monstage_session`
  
  
  * Evidence: `Set-Cookie: _monstage_session`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/statistiques](https://www.monstagedetroisieme.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js`
  
  
  * Evidence: `<script src="https://d2uvddcac8vf0w.cloudfront.net/packs/js/application-4402f01c6dcdae88c9a5.js" data-turbolinks-track="reload" defer="defer"></script>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/robots.txt](https://www.monstagedetroisieme.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/statistiques](https://www.monstagedetroisieme.fr/statistiques)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/USEA-Cherchez-la-chercheuse.pdf](https://www.monstagedetroisieme.fr/documents_utiles/USEA-Cherchez-la-chercheuse.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/versLinfini.pdf](https://www.monstagedetroisieme.fr/documents_utiles/versLinfini.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-eleves.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-eleves.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/USEA-Carnet-Stage-Education.pdf](https://www.monstagedetroisieme.fr/documents_utiles/USEA-Carnet-Stage-Education.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-entreprises.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-entreprises.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-referents-departementaux.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-referents-departementaux.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/MS3_Programme-a-remplir.pdf](https://www.monstagedetroisieme.fr/documents_utiles/MS3_Programme-a-remplir.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/CarnetStagePro_USEA_WEB-2.pdf](https://www.monstagedetroisieme.fr/documents_utiles/CarnetStagePro_USEA_WEB-2.pdf)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/robots.txt](https://www.monstagedetroisieme.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/RienNeSertDeCourirPageBD.pdf](https://www.monstagedetroisieme.fr/documents_utiles/RienNeSertDeCourirPageBD.pdf)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-membres-pedagogique.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/USEA-Carnet-Stage-Education.pdf](https://www.monstagedetroisieme.fr/documents_utiles/USEA-Carnet-Stage-Education.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-eleves.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-eleves.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/versLinfini.pdf](https://www.monstagedetroisieme.fr/documents_utiles/versLinfini.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-entreprises.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-entreprises.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/USEA-Cherchez-la-chercheuse.pdf](https://www.monstagedetroisieme.fr/documents_utiles/USEA-Cherchez-la-chercheuse.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/CarnetStagePro_USEA_WEB-2.pdf](https://www.monstagedetroisieme.fr/documents_utiles/CarnetStagePro_USEA_WEB-2.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/robots.txt](https://www.monstagedetroisieme.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/RienNeSertDeCourirPageBD.pdf](https://www.monstagedetroisieme.fr/documents_utiles/RienNeSertDeCourirPageBD.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents_utiles/MS3_Programme-a-remplir.pdf](https://www.monstagedetroisieme.fr/documents_utiles/MS3_Programme-a-remplir.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-referents-departementaux.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Mode-d-emploi-referents-departementaux.pdf)
  
  
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

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up](https://www.monstagedetroisieme.fr/users/sign_up)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FDAK7FthxNtK9oEzXCcWwjNuHU0Y5iipoZMDOTnjw`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Bv0ocvC5GPHxfGRV50TDfL5OhYfSZpj0oZBEUIAd7CBYxZ1pnAtofyuziE2Cc44`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `yHQr1Nq/4tdVeNP2iub93DBhEZ3sEx8PyKByHkyA01b8AqUeDU3fvu7ggnLM2s5uYPkRL4fR78CFzGtlP4AYsw==`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Bilyt8i9XSr45S0gVws0ZVbZshpUO8dd7sc68G6ikMXK9kCNFQ0xUFzq6ljHRcpHcZk`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `2F5RVl0MySz57jusX8fxs2YsaXlZMe00a0fdjUtJYgB3OLOtokHw9Llc6aUWrqHAViHBzYY5`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `GlR9nvDvcUkw+417XniVUX/nrXgUYkeddb0rQApUKMcuIvNUJx1MIItj3P8YRKbjL3+tyn+gt1I40TI7eVTjIg==`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FPURYZL1x63gDBRpukWPsj3eOzRf6JQH5EFKykOisxcJazTPLekY7okhqDnJjigoK`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FzpGyUXeYrlQFMql4rgFYqB81UbYEXPh6pmym44a8UFHg`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Mp91DmJUbcA418HQ4AJRjjBXhssqL1b`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FavSF8w1GyFrpFwBdKBOnTRJOOm8SJX1bqma818Vs2mvsqyzNDN3SLpcP6cQTLCxubtRx9KyWUzmlX`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `dI0zSlSJyhcFxNCouCekOSLbl5NNcO8PFJJhsYGTvwaWMKnCeycNt5BINykDP0A7AXtiVdirkSPPcY0Mi5OeA7GOJPpHYRQCmZxw`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BLkd4aT4jvnivE1s4VjTlnmgorugG1DAG4pM4Y`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�P�+�m�\x0013m+�\x0004�p�[\x0008͸u4c����L\x000c��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19544](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19544)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19542](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19542)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19543](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19543)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19540](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19540)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19541](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19541)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19540](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19540)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19541](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19541)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19542](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19542)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19543](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19543)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19544](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19544)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19539](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19539)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19539](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19539)
  
  
  * Method: `GET`
  
  
  * Parameter: `user[targeted_offer_id]`
  
  
  * Evidence: `user[targeted_offer_id]`
  
  
  
  
Instances: 12
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL contains potentially sensitive information. The following string was found via the pattern: user</p><p>user[targeted_offer_id]</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student](https://www.monstagedetroisieme.fr/users/sign_up?as=Student)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users?as=SchoolManagement](https://www.monstagedetroisieme.fr/users?as=SchoolManagement)
  
  
  * Method: `POST`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19543](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19543)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19544](https://www.monstagedetroisieme.fr/users/sign_in?user%5Btargeted_offer_id%5D=19544)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19544](https://www.monstagedetroisieme.fr/users/sign_up?as=Student&user%5Btargeted_offer_id%5D=19544)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up?as=SchoolManagement](https://www.monstagedetroisieme.fr/users/sign_up?as=SchoolManagement)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users?as=Student](https://www.monstagedetroisieme.fr/users?as=Student)
  
  
  * Method: `POST`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/password/new](https://www.monstagedetroisieme.fr/users/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/confirmation/new.user](https://www.monstagedetroisieme.fr/users/confirmation/new.user)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected 2 times, the first in the element starting with: "<script type="application/json" class="js-react-on-rails-component" data-component-name="SearchSchool" data-dom-id="SearchSchool", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/politique-de-confidentialite](https://www.monstagedetroisieme.fr/politique-de-confidentialite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/contact](https://www.monstagedetroisieme.fr/contact)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/statistiques](https://www.monstagedetroisieme.fr/statistiques)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a name="top" id="top"></a>`
  
  
  
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/mentions-legales](https://www.monstagedetroisieme.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_up](https://www.monstagedetroisieme.fr/users/sign_up)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/documents-utiles](https://www.monstagedetroisieme.fr/documents-utiles)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search](https://www.monstagedetroisieme.fr/internship_offers/search)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/](https://www.monstagedetroisieme.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/accessibilite](https://www.monstagedetroisieme.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr](https://www.monstagedetroisieme.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/conditions-d-utilisation](https://www.monstagedetroisieme.fr/conditions-d-utilisation)
  
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/sitemap.xml](https://www.monstagedetroisieme.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/robots.txt](https://www.monstagedetroisieme.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=315360000`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001074435`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000924738`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001076488`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001043361`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001064335`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001074092`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001195319`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000693014`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001344148`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001309288`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000874010`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001049338`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001153321`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000086243`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001045039`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000104304`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001072499`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001067408`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000889530`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf](https://www.monstagedetroisieme.fr/modes_d_emploi/MS3_Guide-stage-a-distance-2020.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000967196`
  
  
  
  
Instances: 521
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0001074435, which evaluates to: 1970-01-13 10:27:15</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Parameter: `school_track`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[channel]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search?school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers/search?school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Parameter: `week_ids[]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers/search?school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers/search?school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Parameter: `school_track`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Parameter: `week_ids[]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[channel]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[channel]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Parameter: `school_track`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144](https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144)
  
  
  * Method: `GET`
  
  
  * Parameter: `week_ids[]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[channel]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[email]`
  
  
  
  
* URL: [https://www.monstagedetroisieme.fr/users/sign_in](https://www.monstagedetroisieme.fr/users/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
Instances: 13
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.monstagedetroisieme.fr/internship_offers?commit=Afficher+les+r%C3%A9sultats&school_track=troisieme_generale&week_ids%5B%5D=144</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [option] tag [value] attribute </p><p></p><p>The user input found was:</p><p>school_track=troisieme_generale</p><p></p><p>The user-controlled value was:</p><p>troisieme_generale</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Tue, 11 May 2021 03:23:11


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 6 |
| Low | 5 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 10 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 10 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 11 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
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

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/tutoriels/Guide_entretien_Place_des_entreprises.pdf](https://place-des-entreprises.beta.gouv.fr/tutoriels/Guide_entretien_Place_des_entreprises.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#dRC4`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#dRC4</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=@¥gyCãÌÝEHP\x0003e¼[\x0015+bI6\x0008®\x0019MÓÚPwµ"P (Ð)×ÒÅ­lWÌÁÕ(øðWÓam\x0004?z6±\x000b~e.3R)\x00073ÕÇ\x0006Jrô\x0010ÞLåÄVêÏ7ÖNnÕq\x0004M| 'ä°ó@9ü\x0001ÊÊ>ôc-aêQzÆqî·\x0008ê¥Ü\x0014Q\x0016\x0010Ð<ÓYø½Ä7f¡{ñÂ4ÀêÇÓµÎëO4Fé\x0001øú*e\x0012\x0005³C[­\x0011\x0018×BÀ\x0018 W¢ïey\5GiáK
·Êmxý]§z\x000chNgÛõSîÑ=o\x000f3\x0006ãØ,ñXë£&_?õ` þñMÕ/!äV ¬ij.>ÚxÁôÕ%\x001bÉj\x0016s@Ña¾\x0014T^7Y_UÎ\x0010Æx2Û>\x0019_Bû¬\x0007?úÌ\x0001ÓÜô¿\x000eàÍ¹ü|ó[¢\x0011ý\x001aùPÀ\x0015\x0011vàZA¢2Ï\x000fS#\x001f÷º)ù°9ôþÉoÈØ/ýS§v±\x001bÅ½ÁQ/3\x000f|C\x000b¼ãx\x000bBåÏT½"\x0008g/Úhh\x0013Íu¯M'üëDìOÈxÌ_\x001a\x000c±|ü\x00058×Hû»Å«þÒv¦m%\x001cááõê¶:4«¯NÃ:Þë%l\x0008^¬ #xà¢OURÇåªñ\x0017Méa´HQè¸7ús-þ8jè×ÃêH\x0019i°s&âêñP\x0003¢Æ]\x0000fã$Ñ¡\x0006Wðl\x000eÍ\x0017Và6	61&g\x0010-±Ò@\x001e¸¼,;\x0010N{6X0Ye\x001fÍ\x0011¬\x001bÛ ³"zÃa«\x0015µµ¶Æ\x0013Ak)æÔæ\x001bó\©%ÕoDçs(eãC-Ë15ën¸l¬\x000cb\x001a0ß:\x0017yf¾h£¾'\x0004¶,X1¤Áå£²Ï¼pf7¯ïÆ\x0013Û<ä¢øÍK ¶`Ö\x0000"´S7¯y°\x0010GxSOÁ¦×\x001bWÚ¤ú\x0002<V{ÒòÚ\x001f`ÍouÚåÄê NS\x0012FÔ$Ga²Gxï\x001f§¼[HÂóRUÂqþòû\x0016íxhÑ²\x0000äñl\x000c\x0016½êÐÓ \\x001c¾Ø\HQww7­åÅ¿ü\x0002,\x0018\x001e@ÐC\x001bj%\x0011NÉ\x0004î\x0017À\x0002ïßØiâtõ`ÅéH+.47¾_Ævâï8´IV}½MÐÆÀ?"/î-¥Â\x0013¸¹¢)íöþ<¦
îÑ\x001dâo
\x001eÉïÔÍ*iR\x0002ÝAT¹\x0008Ý­ñxü·ÿ0t<uÃ]\x0007h M\x0014N|ÉúBtI¥;\CD
\x0005E¿\x0000h¶1\x000eFjê)]²w{Üê\x0000¨°i·s\x0015Eö8êq\x0006üu/²\x0001)1úß9û\x0018\x001dû¡/}<åEÚ÷OI iáN^C\x0003éýHÚ<\x0004¿c¦fø4\x0005÷§úù
|ÃAõ-£"ãæ\x001f¬\x001cL¦»\x0013Ãþ@å+isªc\x00102ßÕ\x0019È=¿ïõ§\x0018\x0019;æ\x000fc<GÝ2âÙ¥q9\x0017Ê³Üë36õ6ÔTß?Ø¯ÿ¹hç³ù8pj´F=[³RIxcå¢\x0015aOñ\x000fi¡ÛbN1ÎIÔ·Î\x00028MQ\x001c¾_+oÉòð×{Ñþ}\x0001øXóøræ\x0006\x0015Ö¸c=\x0018\x0008 ÛÎÌÃ\x001f:§\x0003|Èv5=±[{\x0004l¬l(1å¸ÕrÝ«ø\x001e\x0002\x001a¥26Án»¯"ó\x0008\x0003¨\x001b|ÄA¯çU¹/Ó\x0017Z3\x0016=X
oÌDÚ\x0010'¼W\pÀ\x0013E\x0014QçXa»h-ºór\x0012­¿Þ$C\x00167Fïé6\x0002ü|5#ëªôN=oEY7;\x0005ÛÈWò7;@{sZ|[Uµ\x001d=]/¹\x001c.6ö½·-÷5\x0007/ø!\x0019q¯ûí¯®\x000cß
½\x001fªÃ\x001dj÷\x000eW¬G¼¼äÆ&`³84-µ*Ñ\x000fPéÖ\x000c6=¤Ø°t\x0012º3ß­¡é\x00193°Ïc£\x0006­þ\x0011Ú£2ÍôÐÝÅ¬\x0018\x001fD´!á`ZC GòúßGzíÑÄý%µ\x000cjMÏQ\x0011C-\Î+qt?\x001fÕD\x001c\x0017¤\x001b8ÌÐ`ÈÊE[¾­Ls¿pMÿ±\x0005.Û8Ñt»\p_RoÍ9²øÄ\x0016Ú
{]æÜÛvjZYW¢³°Ô1³¯4K¸\x000eæ×(éîú\x0006¿ÎÕ\x0004Ù¸è
*úGøt­é¾X¤\x001dy¹\x000f79¶Cwà·¨ûFò/j¼Ã¡´­\x0008\x001cÛ\x0011Åú=¿ÆwYcÇ.sÙ(B\x00004¢n±¹*BÔôªåûp³?|ø¦íë3\x0001B½\x001cUêxSsø8Öº¯ÿò!6KCKË%Õ»\x0001+~¤a­à×¹ô÷\x0008Lå¬õ4Úéd¥ñ\x000ctæ«¿.1'(\x001c9UÑ¦ð{!g
3äºþÇ\x0018ãïÓºkg\WÂ=D¯*W< \x0006ù±¾ÛYÂã§\x0014¹tâói\x000c\x0017%×?Õ\x00141C5ú¸\x0014ZPå»:µëc°ÅlzT\x0003èÎPÈù|_×êyåö\x0004ÁÖd¦p&Â\x0014X=¡Çá\x0015C\x0012}"',]\x0005B}ÞlÞ<Wq²G¸õò}ý÷FUWéáóºÝ·®<\x000fLöÒx\x001cô¨M0tòFþâÞÉ_ñ£½3\x0019ô\x0003vY\x0002yìNb®ä\x0015Ðpv¡\®4Ô\x0016\©õ1õ¹ºó\öZ=oì	gûUYº&þ\x0001%Ùî\x0003Ø¡ åhîØt\x000cj`ômpB\x0015íÐ0¾\x0019q§[Í$£~\x0012Ï&'ù¯¢´Ó2N$\x0010¹øºÀv{¨õÆÜ°z(«Ïc\x0002Ùo?û±v·«U/V'ÅÛèª8ì?f«û°ýæÝí¼ñ*ÚK¤¥ñ>\x0014)\x0008á4a«¹ó[q¥wàö3=\x0003±\x001còÙºöëíìÛ©í^ÿòóÑ"²¬5Ú\x000cY¬Â×¬\x00192ý\ß 7&KW»»eÍY]è\x0006á¹³\x0003µ_·z¦Á\x0014ÑÜáaÊ`^­Mµ¸[§õÎWÝòlSÍMTx\x000b'd¡f\Gr[wJ£+\x001ae7B\x001d\x0006èë)üáû@mýW\ÝM6\x0013ß\x001cØ{ÇyüªÞ_\x001e2-#4ü,dÿ®6Þ	5ÔqZ|çØ\x001f|ªüïÜ}]§)Cæ)qX1(ÝÍÔ@bÝÝ#Ý=J)[jô<u\x001ap\x001c¢£T9úËÀ(dyW(¼ùø\x000cºF¶9ºr\x0016	!5ÞÉ\x0013Ô\x000e°É>Ìe:jÉ\x0015£uÿ¨ùG¯\x0019\x0002m!Ç.\x001077Ãßy\x0014\x0013_û\x0006yä\x0008 cºûhm\x0018å¿ä"½¾\x001bØ\x000b¬ç­;aàWàûØÉ#:/¸©F¨ÔÉ²Á<6Ã6þéïQI¤Úv§³>I$
\x001dÎK\x0016áIÜ¡¢öF:Î³\x0017/Î.AÅ~lö\x0006\x0011\x00126\x001bgÚà/\x0001¿È\x000c|Ó±î.ìóI\x0019ì%\x0019\x0005Ù>×êú 'û\Óíªù\x0008¥\x0019è\x0018èÛT»ùÙ$A\x001c}Ïf#>°*¸©9ôjw_Ý®­Ùd&GkC\x001aÊï.7à´¾é<¬wå¿\x001fö¨ÛõKæÄ/áöb©LÆÆ°4yv\x0015y$2|\x001c3XÝ²¹¥Þ<Jò¾ÂO2Ôä¡É%&K{#L;h#(vl\ÓÞÁgøaÌÚG\x0001~à,.·#_äo¥å1åy?åøëD\x0013¥¹?êÉEDÅè2èÁË;>W\x001a¹tcs¯wx%\x0011þ>)3=Ûç\x001bwÇóX©x-Âd\x001d¢À\x0007\x0015:IK\x0001wèg;ÌoÛB¯­Ò\x0017¹DÙßü®wgÐËz°¢º4\x0006¦Hj\x0004I÷@®Á_î¯µã\x0004_\x001c\x001f¬¬v\\x001cs¶UÓÆpÕ<\x001fAè¢e\x001bØR¾\x0000"V¬\x0013|a¡~M2Ñ$ós\x0003?VSH¿ãµê\x001aûÉÑä(\x000bz_Tn[e¥Ôæû\x001dhþL¤©H
\x001eü\x001b>¬¤JÕÇú=Íô~r%_Ö^\x0000\\x000cNÈ[¶zv\x0010A«wÔ\x001e\x001a©n8TäCÄ^l°­ù\x00029Ö¤\å;\x0017\x001e.!G"<~>w\x0017²K@Í&qÎØ´©­Ú¢pîO\x0011öu¯PU^ØÍsNIIÍQ²o7^\x001b\x000bT»<\x0003]Vü\x001eêøü5||\A¦\x000eèf¢ñQóÍ»ù?çòdÔRR6Ö9{¾kGú!PY)¥Ïíq­\x0018dº\x000b)\x001f'7{º¿Áv$ï« ¢1².|\x0001~Ö\x0018p\x000fùëýV\x0008è\x0002þ+\x0012ÝëÔC1=\x0019&ýHï=\x0003\x0003ç*ÒW7NËc±éæzÅ^.Ë57Í\x0017[ÜwøÈ\x0012'¿W#ÜÀ\x000f®\x000cgóÑÔþÏæÑ	\x001f8\x001cäaz7L¤k=ª#óêK6Wtó1\x0012mQÎ_M®DÂûëñUKüÙ¬!Â§3å7\x000fwk\x0013¶ÑGUOnõPÛÜë\x001dã¼\x0017E_Ô×aÅ
¨ï\x000cM²ü\«÷&e-\x0011\x0019»=E
\x0001\x0003Fý\x000b ºÔC{¶DGY«ÒóSPoZá÷Q*ãô©ó°ù\x0012'¸3A?Í®¡@÷¡\x000ej\x0018\x0004¶qÎ\x001016Kª@ve\x0011\x0014\x000c8cb6â\x001f^ËÏþK?h_É|Ècª£\x0015\x0017ø­³»j¤H\x0012_3ùH·Ikv9KglÓ	ÝË¯ÚàRÐû	*©Ö4~Q\x0019x?uv¹@@ý£Ò\x0006¨¨ä¹ïÑCÍÉoÄ\x0006a8T²>Ê\x0012VU *\x0019K»äÄ¢L¥ì
eV°TÛ°\x000fõ\x0005XÔ\x001fÉ«i_tÜÏ9n³Ñ\x001e9\x000fkvï\x0005y.ü-ûa3.³^8CJ5U¶þ50ö\x0014qÌïÝý¢%´Ì×^\x0018s"ÁW?I6©%µçðÌ\x001e8\x0019ÉÉ<ÊèMv¼Õ\x0011©×5ü»î\x001a=¨ÚmZP
d¢MË7ç2xâÕéÑ¨Ø\x000cË)a­f[ÑG*X9QQã&M
G°\x0013\x0013:mls\x0014<]\x0005\x0014VFû§ùÇ¼Tý~!ÔwÙµûw6K¸z|\x0016'~÷&{\x000fT¢¸~ÁÐ
BsC.\x0017:?Ð­tôS£\x0003¥\x0003¸\x0012m¾ÕvA\x0019ìã¶N)óCÞÀx\x001aØwg>í;\x0011\x0006OI³@µ\Ì©¸\x001dÒ\x0018\x0007c]3Ó¯?REµC6ùTÚuµ05gEÌ&éHlûE`ö\x00191Ö­ÎÇ\x0018NÓ]\x0011K|¦\x0014~D9õXü\x001a³§l.[ÁÍÓ©þçà\x0012íÁØþ1H­ÐI\x0016Ñô)|î§:^ì\x001bkÍÎfÉø|{-Íy¦g{Gr\x0004O\x001eh\x0013ø\x001aR|ÑãÜ@Ö{O¹\x000cv©~rÀîc¹êaÙðWeùP·1°ì¬O]Ë!\x0004=®Z×ýC­\x0018Cu¬ê
Ü³=ïëÒSAµÏí\x000e¦Þ\ó"5­\x0013ÑþFGK[W\x001b«\x001c¾ûÓYùÊSM\x0010¶8ðKXo¦q2'[[A Ï¥.î2\x001dÏ¸Ðò#I\x0010áÔ\x0002§9®\x0016\x0017z\x0006.,÷\x001bòNêCu%ôÞ\x0007òaé6"}"\x0018*êëöÀûVi¡Y¢7C@2\x0002{%\x000bæ\x0005KÊ>,¾;¦:/÷Æq\x0007y«@y\x0005\x0015I°ó\x0001OþÉY¶\oÿ\x001b¦¡ÞÖæ\x0014ú'O"xª^VwìnlFÐ{/æ\`((k5´X¶t4Ê%C7tÊÄ*¼\x0013müÅ3ÿxA=ÚÙL+º»Õ>}«\x0004c½ÜÙE}
f¡8ÒÒÆá0zæZ\x0012âÙ(h¤Ô"cQà·è¤}O§£ÚB`\x000fO
Põ|\x0014º#ûp»%ÀË¡ÿ\x0018n¶@É·}\x0019d_t\x001dQÄ³AX.Ô\x0012áp4Ól(çr$Ë"2\x0008YÜFÖ«[W¡/Ý0LiXð}r ùìæe×\x0004É\x001bVåëÀ'ÍÚS¬\x0015q"r
uÉ\x0017à\x0014c,n\x0004Ç\x0018pèìÀn¦ÛÛÚ!}¹µ$\x0017ëCtäRLü@Ó¦ß\x001bo+Ò0\x001c\D6\x001c2¿3å]§Þ¤¬§ÿ+ßÂ\x001cCP¦½\x001aÒ\x0015\x0017.ÔRRJ\x0002ÛÆÞ#åGÖ¬­?ÈÙ37ÒÐwõ\x000f:Ë*õwgÞ¨ª´gèd~ 'ÂÂ!8÷>Ôoÿ¾&vÓf®8fHÙ2\x0002¹ý8u/ÁAÌ@a\x0008³ö-rL'ÜÖËO\x0008ÖåsöÀ«2~Î\x0017þ!ÙËzÞ\x0000÷§Õ³^k¨v[Á¡Äps&¥É\{Çc5Uc\x0002]a\x0015
ÆîíÌ\x0017@·ÈÀi"^wT`\x0017¾?\x0014¼Ôéó;ÿPÆsÒyà²9ÔOÃÿV°2î\x0005H¨\x0005lø/ôîÖ¿±\x0012þDìñÃ®|>H¤6Pµ+gãùÃMS½Ôú\x0001Æô¥óMHm-\x0003)"\x000fÙ­N\x0010þúß¢@X¤ù\x0015HÌJ{ok~ÔU=¤`R«@µGziÙqsJ\x001dKÓcïùizË\x001dHàÝ/üa{Ï\x0014ÔbóÚ-®¤&>HÆ@\x0006L)·ëj]8xc±¼\x0003EBÅYµ?UpN88º×¸é¥QA]Ðäõïv­fx±léÜXÙ
È«#úâ\x0000GØý\x0000\x00063i9ÏL¦.\x0002øs
üY\x0002ôN¹]½Ì\x0005!r,©v¨(!0Nòîáº)VÛxn\x001cYÑ¥l¸zíXü\x0005M\x001bãd®åõ8OaÝ\x0003MX\x0012\x0013ªvíÞy±»ûæ\x000e\x0012©ÃùÚþ:\x0013ë4ÉÕÔkFsW»ôÅÇï\x000cFì:² ¢\x001f1X°ôïwZË¥\x001eÍ¿p\x0002\x0008ÂvÛHIn_\x0015VH5VÔß\x0015}\x0014\x0003àwÞÊÓÙ¦\x0008 êýH#Û{ñ¤`.Ó(}(ßü]-áÚNF}x?¯ë\x001aNe\x001cjÎn.<¬µ«.ùÓÞßÍhò{e\²Tû5@¸{?\x001f6Í%n¿ÝÝ3=É\x001cxSy\x0010@Hâè \x001es[°¾ø-C\x0014ZËeÖZZX;êM(oj$*úMITþ«}YÒ]VøaÇóÇ ±²ßñMIåT®ÀP3n\x00111÷=Ö­ÛÏt(¯°\x0000ô£-J
Pµ\x001e\k
\x0006ÏÍ¸\x0010«Æ(\x0012d¨\x0006K8y\x0019\x0012J¦dê¶wÁô\x0005´O;ûò|ØÑX/übßs¯VµÑÝóþ¥\x0012 ¬èD\x001bÂ\x0008\x0010ÿØx\x0014pfa£¬\x001e!3e×ô`R½7úi A)Å\x0008Eg{­¶LðIñ\x00058{\x001eUÖ´WÂP;ã\x0001}»òõu)#\x0000\x0019\x001eýúY³.\x0017"®¿Ç`W°9ùó\x0000ÆÞÙ\x0019M\x000câ]Âló,R©X&«2õ?é\L2es\x001dÜ1+\x0011ÃÐ+ÿ´Æþ¡àæ\ÈNK­¸$0¾\x001c«	.ü'§Ñ½\x0008rt¨]\x0019ãlb(É\x0011\x0019Ïç¹Þªö2
]-iª§ÔY19;T29³K òï"H\x000bF  àÝ\x0013\x0006|Öcî|\x0001¦\x0013\x001d\x0017|T&æ\x001a9»Y\x0005ÿ.:Ü{	-£ë·Ml¸ý[þÝÓ×Ò¤z\x0000\x001c	·°¶{bOÑö&·­\x001bÛ@Kù-]\x001cÌ/îêø¦6ûê\x000b`\x0011ÄG§7íìßÒ"½_>×\¸ÞËªÜ´qbæìÊ:ÏSD-\x0004X¥w¶u0RnÎþñ^nMEZ0^6WWËm0]Î\x0006ÕÜ?ì´P.\x0003¯ÃÒ\x0015Æ JâZE¶]}>\x0008,\x0006ñ
ªfÛU|\x0001üu\x000cnn°r\x0013tAµ+SOñË\x001b\\x0004QE$Â¨áázZ«´TPIRdÉuô5êe\x001da\x001b\x000f?Ý\x000f|Bî\x001bÐ\x000f9{\x000bLdì\J
«Æ\x000bY\x000f½\x0005\x0019´\x0006|;Ï0@=\x0011WfÐQò±W\x0001\x0012î®«ë\x001b\x001cÚ)âXbÙ§\x0003Ì\x001aî6\x0008w¹\x0016)tÂÆ\x0014ÈÅ®¾X\x000b~\x0018çòssg¢L¹6¤§¿Ç\x0007k¥îk×üô
\x001eo$\x001bFÐ\x001aëÜ?èâ\x001a~eÐÉA¦0d8ì¿\x0015Wcl 
ëoîýuüíÒ\x0000\x0017éÁ\x001d^î/;^À(ÿ\x000bõO©ýòÒ\x0017\x0008\x0017s`¹é]6£Úèó]\x00196Æ{dÄãbk[\÷É&°5Çé\x001bò~1ìÁGÀÇ°ëß^\x0006¶x×Ê|o1`ZJåè6Û\x001bßCÇ\x0013TdÞãûø}dÓ\x0015bPFÒT(Á\x000eZ&\x0011£Â^$ìWt¤GÔíÚ?\x0012¼àÆ%õ:HG
:év%íG><¹Ä7"|º÷Ù[øyã+qo}bJö'È?D?[í*
Kú-u¸+\x00181Ëñ\x00106¾\x0017'Êï|Ø\x0015[kJÇï¢v¼\x0018\x0011Gp³\x0010'\x0006Mç\x001d
[ÿý¨¾ø\x0019\x00076¯9óÌß½
¨ªóª"à ,Ë	ü+nBÙ=o::ßÆó­Âö\x0015ù^\x0006g±§Ùu²´?õ\x0012\x000e2y\x0004\x001fUæùýd©ùM©hÁÞ:dï¸ç{\T`^d×¢4\x001e|Íé¯\x001füÚ.Iÿ	Ñx»«rË;\x0002¼\x0016¤ù)`?GQv9¤\x0006¢i!§Ì«±õ|ö)kCÛl''ÓÝß	l\x0002í#\\x0007Ææ	Yû¹Ï¿ITïö\x00108Þb±< â»,ÑíÂÓ;ô]F÷·ª¬q\x0019ÊZòÆõ66ð'ÐÀª¬À Â
3ÓÝ?5È)\x0016H¥*é8¹·\x001bZË»`QÕ\x000cßNKúÝ\x0005\x0002\x0018j\x0016Ý2Q³Ð¯÷ãê\x0018D%:¶Ý=á3RÅ,\x00113#îq9\x000b².X\x0015Ø[B\x0019R\x0006/$wK\x000c£h\x000e\x0005\x0013®º	ÜÍÚ5fú\x001b=\x0007ËÈ®s\x001dÞg\x0001=Õ%³µ×ä­¸×õöµ»÷ÈwÎ-È¯F«µ\x0018¦ó4üê\x0004HÒÕ¤ð3 9êI\x0016	çFþ§÷1\x000c2n}bOá<³ë\x0011-±x»¬$æ!ÔÚAÿ<\x0005è°(ñÈEµ\x001f¶nã\x0007e¸¼\x000f4jGÕò_½Õ¡FÃ
Fò$6ßïKUÊq«Ý\x0016¦Í¡éq\x000e]øà\x001eÍ[YºyÖ8Ð\x0005ëÉ`òkÌ\x001cû¨L\x001f½ Õ¿¬î:Ô(z7úWâ°\x000f:zz\x0016ÿß9X"\x0012®Å#v¡_$ñf(¢ä1\x001e*[H§í\x0000L»	\x001bëEë
,]"cpPµZK¦ÍùÆê/lIë¾ööwé
ÝóTåª-Âû!îòØ£¨\x001f§}ÃT\x0008Ø©Æ5½ÚL\x0017iæ¯4¥#\x0011£Z?ÐT\x001ej¾£;¶§\x001cíyïëixÁwIºÅ¯ÔLq=\x001d(<¥`\x001bó\x0007H8¬
ÿôà-sMn\x0002×ÿv\x001faýß>y9§i)5l´ñ¹
ñt\x0014#7ÔZ'	Û\x0012k\B1Ç\x001f¢Þ\x0016Æl=|f $cA~\x0002Ï\x0003§ÝõÃ®/Ñ\x0018ÂUÍ\x000ceâ\x001f2íVÆ¸\x001cf\x0011âÒ¼¸j}\x0003=§È8Yòü?%ÎD7Ü<¦úù\x0016×NÿhçÍ\x000fnRpù·¦â\x0011ös\x001bº\x001b(Õ­láè[\x0007.a/KRÑëz+T¸W\x0016)\x0007töµ\\x0000X©eÎ´.âæ:Ë\x001c¤	Ñâíì«oÇ\x0007^ßAFK×Ô7É	¼àÔcò~µ×\T?3á\x0008¹k`×ÍdÑù§=tÃô,¯'xy­¾EÁ2@Ì:ò/4zPU4\x001fÝã³Ð£Pd­ljÆ3Y9R\x000f®öo+
^ RwU°CÍZËÑ/S<÷YúZ}1ýg2áMYµ\x000f¼Ã®Ü(x\x000b\x0011äû\x00114Zfw£ÇñÌ>ÐÀ4ÁÐU¸æ
NÈ»Ý\x0006Y®É\x001e3·R¹eTâçøé¿¬8\x0007
Ä#n(ìÁ\x0003­o\x0008r\x000eßQ\x0008m}~E(\x00052ÔÎ7¯K?ø´'¤Ã\x0013ç$ÖÇù|\x0003\x0003\x0018\x0018Z\x000b&èkÔÒS¾\x0003
:Û â'{\x0015\x0019Äæö{:ÞæÑzsÚºjY$è[\JÆ¾Çpò2`ËK\x000bo\x0016'ÞðøZº\x0003\x000eéEH\Ùu@ÔØY=OH\x0004
Í¬÷"å¯jz?æg	\x001c8Þ´­TÒ¼\x000báÝr÷Ke\x0011Ä;\x0001¶*ä}#pBÛû¡õKQUºS>SX0)òM£ØS¼p¹\x0018¨Ôöµ[\x0017üË:\x001c*zÍªñ£ç¡ü\x001f¿\x001b\x001f>¨A-ß9GÍã0ã?ög]\x001eª;ª*=*uÏ\x0006¥;\x0012/ñ\x001aÞbÝØ+4ÁÐ\x000c·à\x0016eÜT\x0019;g¼É¸C^h³PÁuª#ô®¢Ä	Q \x0013\x0006?ÇÆuh<\x0017+\x001bDtéòzÄV³Ë¶úãçn¸®vÖ\x001eÒ\x001b=¹á8[áÆ·ý\x0004Ðÿ-¨ë\x000b/í³g«=§î#ööPÄÆ\tß°\x0000\x0014»|ÚÎùÐ~XYÖÔ R\x000bÉræ8-~\x0019{\x000f\x0004Js\x0003S
Öv¬w\x0014r\x001b->s\x0013¦ãæÀà¦õ¤\x000b¸jØ1NËAÕæ\x0005
Ì5yb/ü_+1-GW\x000c \x000bvÚ.\x0019\x001fòNõCu}0¿qnÕZ5;§ÿóæÄ6ÀwÎ\x0006rk
rnå\x000c±w®B\\x0007®\x000e%"oÊÌÒèF@EÛJ©@@^úÉAµ&!\x0003EhèúM¢D/#Uû¢}\x00102ðU1zò^·ý; ÔÛõO¯¬GÍ­¾~\x000bhT$gY\x0000ýOdJ\x0000)]íÐ9E$KI°6©\x000fTù¾¡?v)´¹(\x0011¹Ì!=/ùN\x0018XvbÑ¡yhÞ\x0002Oe&sey¸\x0007oöÕìE£ÑW¢cd?ÂbÄí\x0001\x000c¼«9Ïc6oN&Õ9f\x0013Úç¡·Ù?T¿+Î\x001e¿\x00155Ëj	µf*J¿B0Ý\x001fÿ!v6
æ±GEuåß\x0017Xúh\òJµ<Úò¾3'ÕÚÒ÷4áù*c*Ë0þ«§8u\x0017Æ5çM+-\x0010*¥¦rÆüÄõ§9\x001eB"¹O\Òè\x001a·\x000f%Ö2k1ñÖ%o(á}/kØ0·áÖEðp­"Q.U\x0003op0|\x0010Ç-6ô8?#T°\x001bGÔ=á®³s¯#Ê/ÔÆYZ5\x0008­yÓ\x000fÏzýËÞ\x000eÒ÷ý5¦bä<§\x0002cmE\x0002²¥tHE_RÔ2éþ.\x0015LÒðX\x0003ïÇ\x0019ËUú¶È#}¨ÌÏw\x001bçþºxé:¾4/\x0015_Gjî1$:'iz&È¿Ä[1>«Ë7Å£ÊRüa\x0005<R9Oø³ã«Y·¹ÂÍå$ A\x0008Ã@(CÜÛµNn\x0004Oîëë·¤qbsh}I.\x0019¹ÇU;	\x001cáU\x0011\x0014¤cüÝ\x0010=ÉÝU{éE@±ú/º\x000f\x0008x¾¾¢\x001f?»]û5ÔZç\x0000ÀHgÅÞ	\x000b\x0015Á¿É·{\x0017Gàô»f ?ÈwF3»«J
 \x0011­+7¨\x0010ð²±qG2~\x000b¿ý$Gè§ª\x001d*ìåè~Zlßå\x001eó\x0005þ3¡Õ^6ÔçD!ö\x0015Ìd¶<Êj>3òAQºöËC^¯\x0006i®Ô5\x001aÜþ\x0003Ä\x000f\x001a<\x001fhÄ.Ã25v÷¶|ÃE"J[Ù¼¨l%è.	éÈO^d¶z JìJW3yzgi\x0012\x0016)e;Ê¹KJ3\x0006YdyÙvC6´òRf\x001f{\¶¢
í+òNW»ÂöÎ4oÅ3\x00046HÀO%^U)²éßvzÔíâõ\x0001ÌT\x0013»#n§K\x0005 \x0019+ÜÐVO,qÊkeÏÔ®\x0004·÷J¦+\x0004E¨Vù×¥!;×¤Ç"ï÷8,Ê\\x0007ª\x001däç²_Æý\x0013®p ÷zÝX'\x0014a¦Å.\x0005Z-\x000cPIø\x0007AÛr«J:µ³D¯ªØ1`<Íx\x0006B_RHè¶Zí\x0017`\x0008ä£5§ò÷Nc3³/éÄÊUkrpÏpKLÖ·ôÏOo
òç2pßÁÜØ³Ûû:!êfÄM\x0003ÏI|¶\E£ì÷³\x001eq-·ñ^IàTØVik\x001c\x0001Àb<¿PK	á¯}ñ\x0017 ÑÏççÛ£Ù?÷¢¦Ú¿5¬«'$\x0017Æ`7çÙÎ|\x0004ÕÜý£G\x0014eU)äPmð\x0014Q(êáãþ#(vÓJéO\x0002\x000fî\x0004zù¦¦)¶_ÈB `F\x0015±½ýåÈÕÈ´Ûy~ÇïS\x0000lÖ\x0007\x001a?¿ýøcïÕ~ÍÞásqõYH£Ó«¦r\x0001|¨\x0005éç»t^OÅöÜ®5\x0008ú¯Îô*«À\x0001ü\x001f¿¬9LüX¦¯g\x0003è©zæaï|báÉS;>£\x0016Þ\x001a´þònÚZGj)ÁWE\x0018tÛjâZ%Ûã©-JÙÚ¼ÜÃ\x0004\x001f\x0011\x0000ã\x000eòÃ²Ç¹»xítRÎH\%ô"Ðeâ¾g\x0010¤×\x000bú\x001eg«'[èÉý\x0017f!Ïg}$û°m\x0003·Mþb¹(\x000c5²Ù/wRÉ]2X|lËôoútÓâ¼yT%{*WÏîÔ¾IÕÕúh!ÞvÄç¨l.å©6J	ÿHp©¯¿@H[Òh­ÒÀ\x0016¶\i&ÃHØíÄÆ?9*ú2jÄ,Ä\x000fÃËôxz©W\x0000þÅ\x001aÌæö\x000f1M\x0016\x0018\x0015mÜI\x000cm#]4ä ßÉvGÝ!ÈYòR\x0016%¦.EL5h°G7Å´¡Â\x0017h÷ø¹Ë2È\x001a\x0007õK >¹á}ôT£xÑû\x000b \x0018löQ6s_aÙÓª\x0017?\x0016hNCt³ã6\x001bÄxûP4¦Íhî\x001d¥`WôQl=YêÂb1\x0008ÉÇJº¶c\x0001
L×·c\x001b¤\x001ftrq@úÙ=bÄ&¡ÖE\x0000¦z:éµ(?Í\x000eö«ÞTø¾°¹*={ûNÁ\x0012Ä®_[ÀQÛðmnÏw(©«8A\x0014:Ì@¢.æè®uÑ*\x000e=q\x000fªnAíÊ=\x001e[Eúâ
\x0001ê\x0012Êöñ ×\x001d\x0004=ûÎI½ô:æ¬tGùSR«ÑT&¡¡êj»v\x000chö
I\x0002÷\x001fYõ'ù¼Ó\x0003­i\x000c»qM9MÆ¤ÞäL\x0007Õq¢íÍ\x001a\x0000ÊÜ\x0013qÜµ¦¡ò\x0011,O´Â@p²é?'\x0003Qìu\x000fè\x0017À,\x0016æ6~ä\([h^ckh:\x000cJÒp	\x0015F¤O\x001fÚS\x001csà\x001bÃÜa \x001cÀÃ?as\x000bÏ¦}:©³ö¼N¹DVÄ\x0018\x000fØáûPP~Ó\x0018£¥1í
\x001eáû°½¬qÑ\x0015°!\x001a­ÿ£ç
çTàecoê­#\x001cÃxK¤(ÔÖ)t\x0010\x001bÜ;\x0018\x0003ªÕÝ4°ÑB°!> {<.ó³l|È9í\x000eÏ\x0013ÕIù±^ oöGA\x0013)\x001a¥I`\\x0012
±ûxûuA¬Ñ.C/aª«pI¯,\x0004S.RV\x0013P\x0013&,äkV\x0004®µ}H¬\x0012µ\x001c8U	EÆMd:Bö w\x0007ù\x0014gï±âî¨$\x0010µ\x0004;zë$÷ñ\x0012\x0010kæ3è\x001f0µÐ` 0­mä¤÷ËCôH_\x000fÛëÙÜoKLMfü`Â\x0016å\x0006ÿ5¢	m\x000eV¬JV
TÁw7ÊF\x0011­%ÀÁEðÍé(f¶¥ï	Ô æÆ=\x0010LÑê2OZ&®¬ìôÌ\x000e¸\x0002EóÝ´§O[Y9´Ø\x0011,&mÇ ]
º\x001eÀ8*ª\x0004»	?L\x000fuÞ¸´ôô¸ébÉÏK\x001dQÍ÷\x000b 
,¤Yh
<\x001cU="áÕ·wý-éêMtí¦\x0015èY\x0011z\x0004\x000b}\x0001@fé5KÏ÷æ5E)ÂQëï:pp!Ûë=öF§ËËÎ²f)æ¿\£(GµìÍ¡"ûmn¹ÇWÇtÞÉÍ{Ñ?Æ\x0010ÑéÈØî\x0013Ð\x0014óªtED½ÌØ\x000eíË°#\x000enÛ\x0004ÂÎc¶n\x0016;\x001cP%-awu~\x0001×÷Ï\x001c'\x0004¶}föÉ89GR¾iÈÅ5ÌTO»h©©{gë\x0011èi\Âð½OÏe
dòö¢T\x0012|\x001bÂ\x0002aÌR¤îû«èË4RÆ©Ð¥C\x0002ÿí$°Á(\x001dK¸Ù´\x0012eqÇ]õiNqaN{¥>à\x001dpão\x0016\x000c¤\x0018ëö¸7¶E®\x001d
ÉßS\x000f¢\x0013ô\x0001ys}\x0002ÜA¿HåQõè=!Ú=\x0005ü|µT;\x001d*ÃÙe¾áH#ãß¾hru\x0017$\x0019
\x0018\x0001\x001d\x0004Â{¶\x001dÚ\x0014¯yv\x0019<Ç©Æ\x0006s4"ü\x0010ZæM-)xqºë¡gZÎÑ\x0008øÓ.ÚÙ¾2ü/®\x0006sÁDë\x0012Ö`ÌÆÐ&ý$\x0004×Ou\x0016[0\x001fÖ0¿\x0004í`Ñhé¼ãÚ¸\x000eµÌ{h\x001aØM÷\x000fPz[EzqîE//ówÿ¡Ü\x001cÚm©9\x001edZIGW\x0012ßÎÉ/~%+8Q\x0017r~h;Í:A5Å\x0018#ÇïHz0Ï\x0004Uý\x001ex¨ë²=æÀ+³`\x0001t\x0019ï#sùÄ~Lm©e3àü3âh\x0006G\x001bèñ4Í\x0008Î\x000eÈÏ\x0011èe[ßÝlÀ!}¡lknÂt\x0012Øá¹[A\x0010\x000eûÄ)=ô/÷\x0018ú|èø\x0002/Uç>Þ
46«äy9ÁdD6(\x0010ÿv\x0003Ö\x001f*\x0019\x0017¿©ü<ªôÖ7´7\x0004Ûõ\x0000\x0004"\x0007àssUËýÉÕ8Ln®8ó\x001dÏýÞÝs­nár0&Þ7_Ô:aÂ²
\x0006Ú÷Ç44nÜ²?ÇÜ«Ð("\x0019Z\x0015Øú©1\x0003"WXû[Ãó\¸z-o	Z\x0005¯ÓÛíj\x0013\x0004Ü:xö¿«Hòoê½éée=oè3$\x0001¬\x0015\x0005éÓG~ÙP×üÛ¢J\x000bkIÆv[&Àq¼5og\x001dI<,þ~Oêr"xj\x001ao¢B*\x0006\x0000\x0000\x0016çõgx«uLTã\x0005#@#\x001baX
ÔÎ\x001f\x001f9­s\x0018ª3?ÁÅÇ\x0005/"´Û¤<à\x0007\x000fÇºLU
Vû#ECª&yc[0Ù7áïÒÇç3,¥j\x000f8`pé*>äÎZ×\x0017\x0000wÅ³6 çOó\x0017à\x0002$ìlÑÔ¦
Ë\x0013á«\x000c ±6FS­Ë_bÍµ¸\x000br/IÒn'cFòp\x001by
Q\x0014F,ük³kªb_aÁÜUk¢ÕÒõ±U\\x0008kþ»oi.CÐjå\x0007uW·ðP£×#N*\x0017Bî®é­ï¬(\x001cá¬¤ñtU\x0002üµDå[C[ê­.^0ãu\x0007r\x0019á5`\x0008Øe¤4\x001e¤p¦
OÈ=.57Ø\x0018t\x001dmpr¦êsæÂDU"\x0018õÛYzJ[\x001bH®ú-YÕÇ.tl\x001axÈwL0\x0012`s\x0015ÂtøÆíÅ&ÝTeür;j\x0008Wg$"¨`í­«sí^V \x0012\x0003d^\x0011\x0012+\x001f[I~yì¯¥ß£+ÊÖßKå½7Ãø¸ß Ë\x0011x;ÐRØ0à;etø«7Å»AÑwL~`Å{9WUÀ¶a÷±¯ÃD½ÒEÜ9¢E\x0011À\x0003G ô±r`\x0000#{NE\x001cyÉVc:P\x0001PÙ\x0014Ù§ÙàÊqjô¿å\x0010Jo[ÊPñc
Æà°É9¸
B\x001c\x0007²§jI\x0018ÑÆ)Ùt¡ÿ(\x0011°ô"ó6S\x000cö\x0010êC,w¦nMg*Ô6¥Îæ^¥eìË=(\x0018\x0001ÑD×^XÃT¶cäý¶6³\x0011^&v[¾ý]z³ÑÛ(}¹SÓ¦Âùñé.¢ü@<ïèh¥\x0005ggá: ò\x0008~¨ÆØÐ¦Õ4
Y9vÆç}|ªxJÎ¶3Y\x001bñ, [Û÷£ÇÁ®cøÝ\x0003NeÄ,*N¾C6]½\x0019!fÈr+\x0004À¸Oøã·àÙ>Ìõ$áOö*Á\x000eæbïº~JBî0`çFâæ\x0018´ê¦$Õ76¡s«$Ûî\x001ddî\G
Ié
Ç4%Ìq3E\x0012­$ï\x0007A\x0006+\x0015j§IMÚÀ®ù+f³øÆÑ\x0004©=´ò]\x0000µ©tÒ¥Y09Ä
\x0001ûÑw iÖL¯nKäÓ¿f$Á_¶j!_t¾0
ÐÃ¶(g&1.5Õ>Ä\x001bhÏ\x0019`ÂB±ûÅ\x0013dÏV\x0013\x000e\x0006ÆÈ
mI¾ï#¸Üi©h^árø%v4È¯Kx"!l\x0019nÅW#zNgÍ:&ÒZÑÜ
P¸³¼\x0010H(\x001bz¶'÷\x0003k=c³¥
T\x000e"5\x0000j\x0019û Åv~éZ¸É\x0001´´¥LpÐOåÈÈß¶ á¥éõíN;FWÇÂ Ø\x0003ðçßc5BéRÅ¹àæv=Ñ\x0014?%k½ \x0008/qpºÝÙ²Ë\x001e©¸¸KéXW¢nÏâJàÃÜ6¨\x0013aîK<*·[\x0012\x0000x4z]]	æ×¦>¯n #N±7¾ë AZN,íqøÈqqs±ñqñî\x0016èeÏ½$AeCøÌ,;Ë|b]¢rÀVÅcÜ·ü\x001b\x000c~¨\x00191Ó\x001b¾¯ñ+½'BýY&Ôn\x0010éMÖ\x0004\x0005\x001c\x0017K#oëpnUa\x0010ã&Ð"ã\x000bÅû£\x000f\x0010©)3î\x0016ã\x0006V;æª\x0018s>0!äÿ½,SèuÇÊõ}üo%.Oì:t	d\x0000Ä­\û7G%Ù\x000fz«DÍ?E\x0019ry56XFýÌ=yN·*\x0015*Ömo$ÈÒi]½\x001c§\x0001à:Þþ²!®ñÍ?[ëæt\x0014À°¸t°\x0004ÁSeÍÕðºB;\x000bë¨\x001aÓÈï¢ô\x0016Áê¡Æß¤$íøR¥òrÅ­!¦|Ö¸/\x0000=¬ÉöZV·(9 XE6ùóRsÑá¯UH©ºj\x00133\x001fWP2N÷JZ[gº&\x0004þ~`Ó?¬\x0017Mÿå:¯=»jË»Ò6\x0015:Ñ¾ÁS-Çò"<$'ºu³e[¬ô@IúÚªÑ×#áGY1\x000b\x0011üûÚ`=Fx]N^GXÔ\x000b4Çt£\x000bÏgÖ÷¿l¬I=i\x001d!{«hQ¬/}VWO\x0004ÿ¹\x0003'wé\x001b1ÝÑÆæ7â\x0014Üñ}ÛÛù\x0002Ù?]\x0006H´cP#¬ÿæ¬|èdO~ÿr#Ý+ísV Oðyþ\x0002P¶=þà:	®\x001bga?Õ\x0019v2ØT$z·ý¨¢\x0007\x0008l¶_L)°#áY´èÔ:Ôòè\x0007¢n\x0015\x0013Ç´^lÓáM\x0005¢_N\x000b*hÆ¨Ä½Ä¨{
ÛüuÜö<ÀÜfô¾èýðm/uaUSL\x0013	1:Rù`Kp¹Éõr\x0004oì\x001b·´2BWV
\x0010=CÑ·©¨¦ Â§C¡	¦kàücï\x000f^mè'í~z®a
RÇå\x000b[: ¢èH¥9öìð\x0014¶ÊgýÖäàÂ×ó8g+ø^D3*¼\x0003á\x001cd\x0004BH¨20]¤º»\x00147ç±h#øñlõV|_ÖÜ\x00197ÖiCÙ\x001a\x0011²ÁíÓþZ\x000bñ\x0005äLêüÈ\x001ehèyPôþñ#	­\x000f\x0012â\x0015ÑV¢BÆ7¡Ó%FUÁ@ß¸Dq\x0001®¼£\x0016ë\x000bÐ\x0004*\x000fÙëèíjWU£\x0000BÍR\x0006·?\x001d\x000buC³\´EÂ·=&K\x001db
£4?gºmæh\x0016Ú6±2fqH$!\x0018Ý\x0016Û÷c@.%6·kì3Gì½¿ð2ýÍþ9³&\x0005í\x00009¸ú	|ÃoÁ\x0015>\x0006u\x0000àd\x0017PÀeÆ·ÇÂÿjËÕ {¤òð\x001b\x0006,*&.ÿ¸\x0017X*êP>3Ï\x0005\x000ci\x0015EÂ\x0004ù\x001b\x0013*"\x0018\x000cxÓG0uÄI&	Õò}FP\x0003\x000bßbbõ\x0011q_ã*\x000fs`,áj&\x0011\x0004Ç^àHó$´þ>òhSÙ9ÎkáMÐÎÜ¶Ê\x0000Õ\x0002ªçô\x0010ì´ÍsåÒì=¹V³\x000fNE\x0016ø)8)¼º?\x0004¡þx\x0016L\x0000OlÑi9ØÖ1®ùsßelXy2Q\x001c'Hï\x0013»e3\x0019µ±[ºòÙ6òÚØÐ7ÊXuË¶ûKEmz­ã_>Q¸34\x0015
c^f\x0012ÎCË\x0000±É3Kaáý((á\x0008Ù\x001aLÊ\x0008«YTÈâ\x0003´2Qá¬ße}\x000eiÑ±Æ0ÉùÄ2öÁYççGUòºãÚl}y5ø÷\x0005F¥xOpÊ?ùøFVH`Ý¦\x0015$j\x0019T2´ûYY/XÓO&îö*rã}!'ûóäøáÈÎU¬[=\x000fw:ía	´x?[8$Ç\°äâÌ®Í]æ{Ì7Ì/©`¢q.<¿g0ã¹\x001c6]ÿ¸Yß,º+»\x0016eÎï¨\x000c
ø½ªª\x0003ïØ\x0003§[4a\x001br¨ì¼B
§²²\x0007ª\x0016ÄÓèà2%ªé¢ÕáÙÏÅDk¡ÂfnCü):j
\x0010\x000cÌ¬>¦Ö¢Æ7\x000bF±ÚäíèF°G¿R#°$éú°ÎÛ«
!¤cTdëâj\x001f\x0003VÖ:é¤,^i<,\x0006\x001bö'5:\x000e\x001c¿u{\x0008<V\x0018÷ \x0006\x0014È©r]Qçø\x001fjbõØúC¥S\x0004\x000e¯\x0002¤/óø\ÓòaL{"«©4\x001b¥Hº\x0013Y^tva~£<\t{Öä\x0014¹Uphiék÷hìWûõÝ\x000c".\x0017\x0008\x001dâþx\x001b1©ïP\x001e¤®øe÷7h/+&ÈIá±óÛ«e\x0018\x0015¾Î¥øR\x0014g\x000fw!\îv0\x0013åÕ7ãuCùÇ¬2nÄ\x0004Z
ûùEÝ\x0005\x0012\x001eN¯ßä_­[\x001e3O\x0004ã·\x0001+ô¼XÇì<¹obßÅ	\x000e¥g\x001cÛO|ö
-\x0018ÕR±û¸!\x0006sÓúçbò¼ªcJ
©^JP\x0005ÇI\x001d_Þmùï\x001c\x001d556²>Ö¡ÆáÊÿ-\x0014@\x001b³ñ#É
\x001dBÝj_¼»5#jù\x0001ï±N¿\x001f\x0016¶ð|TaÖç+ç=-A\x0001 þØ@\x0005¼W\x0007^L #Vb2*¶k8nGÕqf0¥yÉY
ÍMË¼Àë%ø}ØæÕ\x0014}áÙý\x0002ª°JâñµÒ×#\x001a¡cÍÜEêk\x0011¹ËHÍN£Î«*ÁA	{læ\x0006«Niæas©\x001b°²afì.ç	2¯K6]-\x0008øæt\x000e;!qÈ·\x0006È\\x0007\x0014Bg\6ÒÊ+$­¿ê+vjb,ÙBZ[7
²<ç¨U£\x0004êVíÖ¿ªj|,áÊÛtýÖGËÍÿ6&ÂLÖ`X\x001dIªmàþW#ÿ\x0012%YÄB?\x000f´=à8b\x0011ÿÆh,/ú\x0002<Îe\x000e$ùßt{%Å}¶hBÂÜï\x000e¼\x000f2t )ù2ý¾\x0012S\x0013fÞM\x0011ì¨\x001cº\x0019÷\x001bí¸îÆ¯Ô-zªH¬ÿü-¢@\úÓx6×ï?ô\x0006éßÎ±Çà ààb\x000eA×öWø/5«û#Jûzkãâä<\x0002\hº.ÚË¨´ÉõZ$ÓôÕQ¨"Ä¤eT\x0017\x0006\x001bè\x0012¶ÑÒ\x0003·\ùÏºÛzK?&þP;«ßAÌ\x0014ÍÈ{Tàîî\x0006\x0013@@ÜcCCèÎ83Su5¤F*ªD«ü;jßfêU?À\x0000­_©n÷\x0011Ë\x0014üø±ÉñwV
ÙùÈÒ\x0007¯È­ýûü\yWl@É1\x0002Ðøo{\\x0016	\x000fñ~ÐH¥~N\x0010\x0015Õ\å\x000eFÒÇ½ö³æR¶¿°->\x00059C\x0016>\x000b/TB`·zk¸Ì\x0007È¹ô®M\x001a
3P¾úO!Ê­\x000eµ^e÷\x0018U\x000c¿©i¬Ëî$pÁs¦á¹f(9ù¸7Íèî
Ì³\x0016&Ô¾X)\x0018i½a÷+¢Éáp2¾ªvLmªD]~n-ãM
Q\x0004ña\x0010±eí\x001aþþO.tdï¹þÙ;Ûú=hT;;f\x0000c²ª3--bDÑ¾ªzáåÍ9:¶\x0014âÈèØD®Ø\x0014éÓ¶8¢å>\x0012\x0015yÍRæFa\x0000ì¯Ëa$¾ùÍ¯ÜÛ#|
3\x0019­?\x0005\x0005~o/UNí\x00058ZÎ¬Ç\x0005þ\x001d©þ`×Lz,DÒ^\x0019[¨í½>ÄQ"]P+ß4Ø0¬Ä\x0007Æ\x0005ØZoÝ»~Gz¼CmA¹V\x000e-\x001d/R¢Çº\x0013ÎùÚ:\x0002ÈXþTë]Li(9úr´\x0016ê?ÖüK©=|À\x001f/5/Ë6\x0008ô	Ð Â\x0005\x0005¶üòg.½L{!³Sf+Hä,¶>cz6ÿû\x0012×ÃÂ kËt!G@Õ
 SÊeQVt)_\-M8[\x001cÀ\x0002W\x001e\x0010\x0016»XþH$\x001f\x001c\x0018ë7;_y}Sn\x0005+Åø¨lîx6°®Õ2Ûm&á.R Pé¸\x0016\x0013¿Å\x000cödëu!6c9m6h»\x001b÷Kn\x001b¶Þ\x0001·@è@hé\x0012ãW
5\x0002óÎðÑÛñ\x0017õDªÔ\x0013Ø t	\x0003\x0007+¢§\x0011\x001f¢åe\x001e\x0001¶ÿÊH`ºãÈ\x001eB\x0003cªb Ø©F6Rz\4P{ß\x0012+·Û\x0004á\x0002­\x0007D­\x0019¯\x0011\x0007GsÍÂ\x000bø\x0002ðµ\x0007âû6\x0019\x0018ØXäÍ1Õü1J]&.¸)Vlàr\x0005s|Ç®¿ ×\x0014ÎJ:þ'\x000fÜX*«´@-d\x001c\x001fáL=^{S\x0004\x0008\x0010:V,-q!¸&WùH(w·z¯Ø¾øFL
\x001aÂ\x001f-lyÄËJCF
Ü/Ó¬5MÂ\x0011C;õ/¼ægÐ.\x0011H÷ô~\x0019\x0011\x0010¥\®5\x001cÌ²}J\x0002Äóö¡i7©âÍ\x001fiÛ³f6\x0004(h\x0012T\x001a¥×\x001dE\x001dE/ÿ-n·:´D.jÄÞ\x00004ÎÄ·3\x00158¹­xÎ[ÝZ,/ªÕ©¿$>ýW¼\x0006­¥\x0011µBÊzñíÈ\x0008$÷çêÅ^Æ¼±:M®
\x0013TIqÉíãÚfõÆ«d\x0013$Õü~>ÍO÷Ü%qCY»·	Á;éáÏÜ#Z)Â\x0014¨*bþã~\x001fvbÀ¨qÉÑ8\x0000ZÅ¥Ä¶òHs®F¦èÆìÃìo
ÁWC1ìQj×1»×ü
\x0017\x0019G/,C6ÏXa¢§1[v·èu4§2ÞíÝí\x0003Zd L-\x000cG\x0016_Î±g¶½ÌµÜKµêÔìB	ª\x000ee_»KN {¦2k}H( q°ï_¡
.Ë®¬\x0019¥¬±WçÓ¹X
\x000c¡UgI¥WËÔKÌÔ\x000b\x0005ñù(\x0010.iÉ\x001f÷<\x0001ðû)\x0012ëÌk¶Z\x0014Dp
\x0010\x0001»\x0018~øáU«ÐÛpwÕõ^	G÷íhZ\x0010ñ?
>aj:ò¸68Xô¯\x000e\x0007òXÍ}âðKw­ä¾¶Dt\x000b§:âSÈÐ\x0010ç/æ¹TSO\x001d$I\x0011ÿLÂ±´\x000fØtùL6ÒaÉV\x001e=Õò\x001eÏö\x0005¨m³A09L½g\x000eè K××\x001bÎ
\x001eW`P¢ÛðÞã0\x0012oñÂ\x0014ì´¬ËKÊËüSêMÙùsÈmSø×àû	âÇ`=ß2\x001aJ®\x0017\x001b\x000c?(·O\x001c\x0002ÕÇ!\x000fpö\x000eÆ`©4Y9ºlú\x0004èJì|~Zp¿U¶±!áàÃè\x0008tûcWfÿôIföÜ+\x001bÍÕß0oóý(F²;c ¥M6B?ö»Ù©P2Óa.7iÀÕ åx\x0014½¨gß~BX]]³¯\x0007hP·°#Â¿;+ñ?kÕ0áøBº
E2å>~QÂ³FµÂ52\x0008\x0003Ë§¦ò'<7°\x001c½I¢IÊ\x0012êØ>¿Æ{æðUSOcSÖëIsÚy,BÅ¶\x001a\x0008ÍV¤ùÝ2\x0005B\x0011
1ÅJ\x000b\x0011\x0019ç¢8ÌLA:/!Ó\x001a\x0003xÈÂÉ¾,6ð%N\x000còíðsp\x0011L¶p»gûÌs©anÜÜÞÑå6ðÇ«â\x0013q[Aà\x001b©uÿ\x0001ú\x000bi{-íÚÖm\x00114ß h\x000e@\x0019\x0012>²\x0006ÔRÛUH0a¸f\x001cr(¬Ô¡~ÄaM\x0012QN+¿Hx\x001aõ\x001fK@b\x001ar¯\x0006t¬z¼Â?íìuMB¡¥x_ù\x0002#_
®\x0012çÎ	½5%Zå\x0013¸ñ"!Ë'°oÔ"\x000fdÅ]ñ[9¯äóeÌ±ÃqÌéqÌMR2\x001av\x0018E\x000f\x0002XÑo¾Å@u^®ÓkáÇõ½×Øq\x0003vî!S(XÜË÷µ4l-Ü\x0005½?ýS<Ajj#ÃÆÁ\]¿ïÔÙg½\x001b"Ô\x001bø6¤)õNAÌÈbóËmÅç¤GÈ4AöSæº&ÛÆk\x0014B\x0018Wtåá¹,G¦µï$¬|Uå YÒeÂ,Uµ¦Áµ&¼M\x001fuqÚf_9L.A¦L.ü>ÐºoîrÊZ¯q PäLÎ\x001dÿô´à³Å]Rw#\x0007µCJå \x0012¹ð\x000e4û\x0005\x0008ù`@Riêét×£c¤ñ$\x0014ï:'×ìßeÔ	ÃÃTTPÍ¤¼ÿ¾e±æÓ÷º0¶Q\x0012Õ\x0004Ðh,{óGoÈï`j\x0013\x001aÈrö\x0011\x0014&\x001cZ¤^µb~"&íqSn#ZY\¢H\x0019ÔÃ2T¤²Qo¨%ø%\x0008?\x0003ßbÒBF©ÃT³üSaE\x0006Áÿ8yæ\x0018ÜãÁ®À¹Ö\x001cËQ_³*5³¨3$ð\x000cZ§
Ýg8³\x0005þR\x0012U·æó%ÿv\x001eÞpØ=Îoñ	üÙ\x001cOXÕðÒè=úðºèwÈm¬7\x001a×\x0004Ã M*\x001eÕ_8B*éPÈ\x0003ÈëÚ\x0015\x0013QyóZ-e³T]y+\x0007Â-ÇÜ3i\x001d.:Þ ½>ïÄyÕf¥ ±?Hô¿÷ÕBé\x001atöl!\x0000§¨pÏ¼§lHú
mè&ÝÖR·jDc<yN¥é\x001eY/è\¤ZèJ $]Yï\x0015HèÞ\x0002Å/×É rµìveàýÒ\x0005nÊS\x0013u÷LöDDk\x0006U\x001dº³¼_~\x0004þçÅu\x0018 ¼K \x000cá«´xZtÏ\x001f\x0018Ç±¼¶?\x0002(½5÷§4¢`%]W\x0010\x0001`áÐ\x0018÷[ª¨´\x001f°;zÿ\¶qBH7Õ\x0013år\x001d\x001b²ø¶\x0013Óñ\x001fÕ\x001e\x0004\x0012Al°¶xfêétôèP7ÃOÿ¹\x000cX4\x001eÎüË.%ÜÝ°	/f4(
­\x001dûÄ¨-~f\x0013\x0015¶ªzÅíÚOêÓ\x0008¼Ô	Þ489å¹ã]
Í¨
?¨N.d\x0004ù\x001fx/C¤QÚ¿\x001b>y$É4®Ù,ìÎ¶.\x0002Päw½Èª^\x0017'äN)c.\x0014£³2ÈXRÞ>$ÓSí
}pW\x000f2øµWF''õ¨ÚyÎÁÅ¬§²|óIó»Úá\x0011XW\x0002]+æHþÇãÊìRÇ\x0016\x0002\x0002ÎBÖ\8ìBµàBq\x0017¹\x0018o]ye(VY\x0018\x001eDeºà
\x0015ÅßÁÜZé}O¦Â¬z)®BF=¦\x001bûî\x001b_\x0000øóÓD_j»R6·[vIÈï(µ
[z
\x001fEÌ;qÄB*½+q¤Aé.]c\x001b«:@q¥|¿KÅãé\x000eôfy\x001c\x001c×]öÜ\x0014©s-eÓD iä	úô;·\x0011¿7³ÇZ\x001aO*æ,ùÔ8ÖÑ§\x0019ß\x001cñlþ)C"\x00023ö>$XrXg6ì¼mV¦ºG\x0007¡«}¥yÕ]µ@jí1RËýgIÅë:\x001e¡E£t\x0001ÝFÐ\x0010ÑN¶2ùh~Ö· ×TÓ\x001cÓ\x001c¿6\x0007^º¹F\x0008dzÿA+\ù\}oóã·ù±Öh3­$¼lö¼÷Û\x001b©R\x001b»ïîRN.\x0001v6¥ ·êP®Ûñ"\x0011ÖÙ ú0Í[\x0007ó-È¹ñ\x001cS÷tg¿ÿ\x0014AÌQKN%-Ð@ÏÞó\x0000n­ª:có]Ä
.!²t¾ÛëÉ{0"³#öèeÛøi}¤
G\x0003)&ª¥ôOktr\x0011ÂÀ\x0002
0ÁØ1éâËHj!#y-ÝV,Ñc*\x000c½bï\x0018pýûS\x00039â
N?d·
\x0003\x0019"ãHÞR\x000b%
8È:Ù\x0015üaKÅþÌ¸{oª³ ç©CV\x001eÒôjî+
ü$ä0aQ]­H%.ð\x0014NûÆ@G>-áê-1\x001f÷l)ÚRÓì?4¿¹£ëFRTKp\x000cU\x000cZ?üôØQVrØ2×`\x0001Â»ú(­u$­²\x001f
9\x001fY\x001aRwÂ¸lèÈ^!¢gÌ!àÝÖfeÊcgåã±O`ÁmÉÐ_Ý1Ç\x0008
s^{cý\x0001»§Ú³6<îÙ«C½)-É÷\x0008\x0003Q;I¾¼yÖÓè÷Þ×\x000b²\x0018ã;þ¤í\x000fß]ÿ\x001f\x0007¤®ê¶\x000cU~þ¬ë~\x0001©×\x0005§ú­½\x0018jÎRã\x0014y¾*\x0018Yi{¿°AÖä$tçÒt«PÃÒHrKq*¢â"åaý{9ó-\x0002È\x000f%åÛpçå7;L\x0008T\x000c<3@b-f4Ê6hGÜ\x0003*<X %Ë4\x001b\x001b\x0004ðýmv°hÕÞ\x0018Ô\x0010¥¿³C8¶ø°ëQÖÉoªðin\x000f?^ORùòQy¿Y\x0012;8b)L÷pXt­¢"$*Ø\x000fÑj>é÷x)-Å\x000e[Ì¾Ú-÷í[{\x0012Câu~PßÁb\x000e»\x0003És5º³z¨[ß¯POSv\x0011Iwuõ\x0004¶ÉÁ\x0018BW\x0012Ätø«ÆJcÊùØ}¾@­z®EÃ:ÏÎ¼)÷^s#b\x0003\x0018±zT²Ýl¹ò\x00005\x0018Ka9ÙÄ»P4B}=InÍ£cKnÓ$Kÿvæ6°;\x0010GOÓØq\x0014ùºAì0AæÝ\x0006ìÂÎ#is¦ëÄ[n]\x001c£¯\x001a"\x0002ø\x000bg\x000b_\x0008ßWn\x001ag\x0010"Á­\x000c'³÷öfNy\x0002úÆ\x0000+¯\x000b§ÿ¼À\x0019U©mVK§â_èæCW5Nù[\x0015¡PÉ#M\x001bÎ
_\x001a._Ow(ÄKC\x0006\x001c¢ôÎ~¡Ðã\x0014ì¥BÜ¦ôý¶U\x0006IR\ÒúþmMë(/dW\x0001ñ\x0019WgDz\x0016\x001e\x0007q\x001c"òÏ"°\x0003ªá¹VYÂ\x0001®\x00089*({8+³ãLÎí%{»q©Ä\x0000¢Y\x001cmt*T¡ËUôÀ,_Ê\x0001ærFû\x000b\x0000§ÔØÄQø\x0006'Z-Án$C²Ì9áó\x0006V\x001cº×nºÔ¤àz\x0003¸Å\x00047µé\x0017Ôq
æu§ê\x000fq\x0011ã){	JR¤¹­Ê½]¿3oq!DÓò$Ó¸~0¨·bqFLÉ.C\x0007+XêK<W·¹BlÌ\x000c\x0014|*7Crj¶rôhÌy\x0013ò\x001fGFa}Sìì\åéÖ©·É|OBg§TòÝ^cD\x0019Rrd4e\x0002¹©å\x0019\x0003ÅS`y6\x0013èÈ=¿yæ\x0001dÃßm\x0012\x0002ºTgQ®/õÆduA}úM
øýpuå8¨íM_\x0000k(÷\x001böÌHäï\x001d.)|K\x0016]\x0001'J\x0002\x001a\x0013\x001d\x0007oü¬\x0013\x0012DÀ²ù/ÀYeK&>\x0007$Ø,õÂ\x0002+«.TÊ\x0007Ò\x0017 ëcDóï_æ¾9ÐÞîùPØ#0¿¬ëRX¾qþ?y²#&µ¼ëTYùÓ]	Ýv!ïÓøüóX{~jÉÔ@=-T$8óOý².ú\x0001~ð\x000b \x0010¯^¸)@Ëp\x0005ç¤
ç\x0018`2lw·÷\x0005XG\x0007ò~Ðü"Û?Õl¹¤Gkü\x0002Ø\x0013iñfSôýL
\x0016ù<\x00150kx\x001aV\x0013ÉÆâF\x0016jÆ\x0010©d\x0004\x001cÏ5»Ï;;^\x000e÷fPY\x000eüâ!NxÌ\x0017Ef\x0010W\x000chãäJ¢2,Þ
!Îno×hÂH \x001au¹
JW´Ñ\x0015LªLP\x0014oÀ7+P{]ú\x0002d®ò:
\x0000\x0002[«$Í3\x0005~\x0006a´§Ùï¡
Q\x0010d\x0005ZÌÛ!\x001d~äNÑ§©&på[	G\x0018}Óþ5"	ýý\x001aÊý, \x0001¼¯á§y,ÁÚ<t'Æ¢|à\x001cÄ®÷\x0008b0Þ5{kÈ°GùÓ!T^0#¢Úò¹Õj\x001d+\x000b
¤ªFé1l\x001eö´\x0014ÔN±süüñ9£\x0019½8ç6X\x000cOú\x0018M\x0003£²¢tYÖè6,\x000bç+Ir\x0016.=;};\x0017LôOÕ´ F\x0016]öz.Ñ\x0016 ï÷WN\x0002`i\x0005\x001cb¦Dé\x0004³8vu:¾¦'¸NÊ¹e·¹j©`MF³%
'¢µÚý¸Y\x0008$ïôabh)$0=Ó\x001fÙÞ8YkÒL+»r\x001bg]¿+\x000fÑ#¥º¹Ø"ëNÀMSÂ®î V_Ïõ6¿×!G-B\x0011 ã¡·N\x0015H
"\x0014ÇPË_\x000c\x001ca=\x0006'\x0004¨PY9óìoh|ðB\x0019Hì¤ªnéåÅg®\x0001f|;\x000f.¡5äLs]úKuÍÒk\x0014»róßcÀ]¦Unzìuª\x0001vHªö´	;ÓNZ®oÚA\x00085åcâSÖ[yÃ¿: íÊøñ{¦£\x0006·HRÕêÙ£)\x0014¦¥¦exHû\x0002l
ÜÄ\x0008%³ïºù\x0016\x0001è~ns×Ð¦ëâm\x0012)<Ïø¿Ä\µS\x0017\x0002qâ÷O-³×83<\x0008ú$ñ^\x0017§}£õçÖôwnïÂbÔ&¥V\x0016B\x0012\x000e®r\x0003[ãbr¸|ÆÈË2ÉºÀhìÅ4«äæÛùõwúß\x0005¹\x0001¶\x001f±\x0003Ù &EaW*\x0019\x000eVÐtêà\x0016]p[vLzTÕ\x000fßÞåY?-+²*5Ë\x0005\x00083-c¾V¦\x0011"¬ÛZ\x0007Ô\x00113\x000c\x0002¾@òbª=³Tµm\ÌìZÛT\x001c{Â¶ìþ¡¾´\x000c/ÕAêöV+3\x001bªy8cgóCü¼ª2é~MÅ \x0010ÚçÕãñÌIW3É³\x000cæÃKús&Ùªúâp§ÿ±Ígê{¢Ë¿%^|®"ÛÙª?¿*¸Éÿ£Äjä\x0019ü¨§)Õ%÷J÷ê¥H1C®		:|Ô?û\x000bîEÕ¸Yù.`\x001c×±,\x0004\x001dHI^ eÃ^y\RH\x0008É½ªÊ¦\x0002¾© 7iKã·î\x0014ËVÆ¡RE¶MíO\x0012a¾ùÎ- =ºÌÀH\x0017A¢b`ù\x0003'´ò\x001d6bcR1Ì\x001a\x001b °Zö\x000f\x0002<BîUJÙõÅÐÖ;´±m¨»a'ñ20óÆ¥ÙÂ\x0015à\x0013j®$1P?àìBO\x0014à¼áj³aéY\x0001)T10\x0014\x000cqª£\x001a=ÛåF=x¶y\x0016g÷ã'%öÿY\x001c\x00105´Äsû1¬Ã\x0000ÚÂ\x0004k\x0012v¹\x0004BøÑ£8µØ¦ÁÈ*ï\x0015eÇ!îÕÂÔßkMC/6Ø¥\x000e\x0010ÂQ\x000fHy_5rò´$o>»*µ¥l¨48,¶Ö`ç?\x0004íÂ¢×¸6jF··TEßOy7Û¹g6òÝ\x001ek^\x001c\x001fO\x001eÆ8\x000c\x0006\x0012\CÐe\x000e	ðã£ðá þ5Âø¤ÔA\x0001sÕ©qúï\x001a»-æ\x0005\x0005?e»\x001b¶Õ©Ía"\x0014}5*Ô\x0004ÔÌ\x0012iZôbXsMKCqyÄ[Ñä}5ããÈ
È¡ËïÊÄIa¸î&\x0015ºWwÝ\x000fuiÖ_þÚÅèSk9JAßcçÃ\x001b¸\x0008;ÑI?ÚAj\x0007éþXæ\x001cÍ¡|õ\x0014*\x001d\x000c\x0012Xx\x0013f{I>Q»\x000bGí¨uS\x0016¬&ö.ÖD& ú\x0002\x0004Â\x0008Oà\x0010g/<ÓE$\x0015ÖN!¢ e\x0016»¯ä\x0005¶¨áïÕÈ\x0012Ê@ÐÃ¾M¢\x0005¢ØÇ­~f¢ N\x000bÐBRñ×³fÜV\x001a]¬¯q3õ¿ôª
Ë\x0015o4´Zh'nÌÏsê
;\x001cÙ`HËìY|Jv¯\x0018­oOÅ
wÁmÒ$¤å),`þY\x0016| 3¶î\x0016¨¦1\x0015ßÃ1\x001f¼¼}[±f=3u²ùæöO«Ä
gù:\x0011$×C\x0012/Và\x001f`«q$f\x0013ïèA[eÕfÀ|¥
Ï\x001b\x0012½ó\x0005h´­¤\x001föÀ\x0019iÌä\x0001&IÙ»\x0007Ø.\x001dÑñtGû<$\x0005ÅÓvAý`/¢l²Jtplæ=Ã8Õ2ÁwJ²e\x001b\x0001Í¢¨Äp¾@J¸ûâ\x0016Á¬9tê·ïÎy\x000f*/þä\x0017'Ê\x001eé/0\x000eKÓK\x0003$p	\x001a\x0002,\x0004ã\x00172é¢±nY&.US\x0012xOõÖ\x001c\x000e\x0002éç#Ò×«l[Ï3-ï\x0016ü¾\x0000Fâ3 Sü¶ö\x000c¤²mÊ\x0012±òg¦2µÌLÇ©Ö¡´!GÐ]É¡\x0001õì #Ñé+éÓ`á¦¼<\x0004ÖãgcäzKÍdçÞNù|Ö¾÷JL=yÙÕódUÿ}×à>û/\x0000_$kÄÚð¶3\x0007êå¯÷dF\x001c¶\x0015"R\x0012\x0007SßKîÛ¢Õ¹¦auîlrX¹.«,m!ì^0,\x001c6`M_u._\x0019
þ(
ÕFö^\x00112322&©N°¢\x0010UFJ_­ï\x0000ÑöPAµ
Øk\x0012j\x001dZÅü7
Äê9¾®M?öÊ=\x0017Isu°?<Ë%úz bÜaJpÐ\x000cG×#8¸4ÕÑBí
2³p\x0014½0p&zÖ¢ùX\x0015\x000cl)¶àÈøq¡|z\x000fþ\x0013ìvòD\x000f*bö\x000b|WáX¦À'âÆ¿¢Öm±¿Ù\x0010£
\x0014?_yÅPèR;LÂQÚUeOíøå_³.
l=«\x001dªEb8Õ¢\x0016£rd)hËM¢û\x0019EÚ«Yñy	Ã³è\x0005Yïr%\x0018éHµÁ3e4#\x001bù$@åÐ¡ks\x0006,Õ\x001f+\x001a _U:.8WZü5<$Ð{$Û×ð'Ý²W[¿`\x0016Dä?Àø`°Ó¨O}\x0013RgÅÆ¤0ì8&\x000eÝÉ>\x0004ÝwÌæíøÜ\x0013K\x000bâ«Þ¨QûLQeÒGý\x000b\x0019#]¨Qcãýy#ªÚ}GÀßé\x001bÄgm$H¯Ý\x001b÷
ñ~Viïê¦\x0014)ãà¹·ù4\x001aEïòé]:ý\x0005È\x0001XÕ\x0002×:<ùI®\x000cG7$!7$Y\x0005Ä\x001b>o8
Ï\x0004:ºø³\x001eÖ»íù<\x000c§ù+k\x001bmÿÌÿRn\x001bw¤\x0012_úö ´XbáªÛ0½A£;i¼T:á?¤é¾\x001f·©â¦Ü0%G{°Àì5áÀ§\x0004Õ(\x001dE?XÁ¹^\x000cÞ\x0003ñ_zâi¶\x00194\x000euûL¬Í¾<Ô¢Ç´n\x0019¬Øbèk;²µ¨#GÍÜ$o\x000b²ÊTGLÏËÚ\x001dÕÇÕû¨¨WÐÇ%\x001bëpÜ\x0002+ôh¤Û\x000f.y²ìt\x0003xäl;ÃÖ^T¥¶Ê6¹ò\x0015\x0018\x0019¶h03\x00154Ñ=ìs¦jÒ?Ó5g\x0017ä|\x0001ÈõRôÚ\x001d\x0004 éÚøÕ}ÇÃE±.9Àu]9Ö±ÑÉØÔf\x001d_.z]\x0014\x0014Ãßõ^dÚ\x000bOç]áû\x0002ÐÛ¹°åÅÔl*h;ÒÃ)XKoÑ)\x0013`·@ú)ÃþÞ¬"\x0008	ÖOìöR¨\x0018c°\x0011:	PXZ¨µ\x0010\x0018º7ë28`\x0002\x0004´2\x0004#ï|½¹1\x001eTL\x001eåú|FÍz\x000c(9\x001c>	ßùþ\x0019ýÐO~W\x0005qæ-\x0003ç"ÖfÎÖ$)e¥g%G±oBàJ£Û\x0015ÿí]\x0011â2 %RdÄÐR]K¢Ê;³ðïjä\x0019Ã¹«ÊÏd©\x0019,ì\x0017àçs­\x0010ÿþQlçk\x0000ý[;\x0003\x0007ÉòUû`¼8Ó¦¦*Ïù©4g1ÎV\x001fUt£¿;	ÑéÌ©·³4àV\x0015\x0006\x001dáLXÖsß²\x0006[ÀAa*9D4.,R\x0013nCÅ%=ô~-/\x0000õó\x000bÐ\x001dÎ²W\x0003£a±ÛèÃOEôCtð\x001b_Í¤RSIãBä\x001br:ø\x00143ÈÖ<7OÆ\x0005n«=5s;±;êuYcwßÁðó\x000ciÌ\\x0012÷p~å%¸ LBBVÿ®C%/yê¬¾Ûéð¿á4;¸\x0001ÈÉUøí~H\x0001.ÎÞÙ÷
:ìu\x0001ÜøqØ>Uv2%àµ\x0001þÅü\x000bàYØ«å Åðý-r\x0000«Ùêíw>ÒR\x0016¬,mß©\x001a-5}ÊlKÙöDAÖ_Q*"G
A*£[\x001ct\x0019\x0010\x001cþ\x0008ßëÂï\Gk;.\x001b@ÌÝÔû9Rr¦ùÃ\x0017Àüí\x000b\x0010a2¹XWrÆªÝÁ\x0017å^]Kmôr°½m$[\gj£/\x001fG\x0015)ú\x0007!j3Ù¬\x000ed÷7,>+·\x0002M7kÆ¶©Ä\x0006/{j§­9±\x000c©+`\x0005\)<W¸äù\x000bo\x0019ÁÉ\x0006KáAã\x000b øä­¹-¥"°nÙ\x0003Ìb\x001dðûþoq
N¤ù¯Cw³®Ö\x0017@=àø\x000b\x0000q©vN¸\x001fïðÇ\x0012Vs'ä0ágO>uKN¥pw\x001aÄ\x000cÍöiBK21-ëØÓQãCìË#ï#s°%#àA\x0003Xø^mËIµãE¿a¢oü\x001dØZu`&<\x0010Ãw¼Õ¶\x0018 á¶Vô\x0005\x000eß0#+,Çþ¦ê6%öÈð8õ\x0003ÜJ\x001fôø;â±´\x0010
\x001bBÊ_5QÖ\x0018\x000eDrúR;
AááøÏÕ«òC\x000c³\x0010ÅÐt«\x0010ÇÈaÐW¶óÂyúÀ¦Í4{Ti¶câ/FÒx°Ø±!e\x0018òp"\x0010ï\x0013pÒ3+¢ÉÊü$\x0013jf\x001ay\x0002ºrAyµPBJú":ÓÿGoùíç"üJd\x0011¬T2!MH3µ¶íjX}R é9hèE-WE\x0005*\x000c\x0011é
\x0016?\x0005MP~\x0019	¢¢ën *Þõ[\x001d\x0000\x0011@@µ£¹c~;ú[\x001am\x0004åBìr*«)m§iÀ6ÄÉU,9âÊ¦µÎYÉÜ\x0000E¡
ÿ¢¤ÿÉiÈ Õjª;~2F
Áé¥DA béBâN}[º#'xe :Ö¿vS]¯¤\x0008J×H¤Gw[ÿ\x0002ÔÒºQ2vP\x0004¿°æÎ\x0019I@×0³sØ"Å²h\x0003Ð\x0004ÑÌÄe°\x0006'Ö[¤\x000f;÷Ou7	ZÌ\x0008?ÙI\x001eÆa%÷¤ö§¬×&ò&µ<\x000f\x0018ïØ¼\x0005

\x0013&*Ãß"\x0010ÔÿÛ·&Þ#ìñ² [ÛÅ·wéûÃ\x001e*^:Jq+¾¶±©k¸FþÓ@\x000f.=W ½W\x0001
³(à0\x00134òÍ}\x000f[\x0018?Çh¢Cx\x0018%\x001fçr\x00124Pñ\x001eoLàN+ß×M³ùq4
kEÃÇ\x0000/EHLåSÂh\x000eÖÿ
MtVõµµ¶@¶\x001eXk\x0006Û\x000cSºJ#\x0013Ýv¬#ú&j\x0002_\x0000==µ£q\x0005\x001e.[Þ½\x0004o\x001da ¬`=&n#õ´£ÔR\x0003Ü\x000c\x000f¼\x00071Ñ\x001f!u\x0019] \x001848P|\x0001~´\x000b:\x001c\\x0008o
8æÆñ\x001b\x0007^gT\x001c¦ña{ü:[Té¤Ô´,M\x000c}\x0003éêÉUL¢÷­d¸²\x0011Í[U\x0002ï®c\x001eòØåZæ.Ö¦Éëh\x0016\x0013+\x0005§\ÿàÞæÕhÆ6v÷\x0000\x0012ÂL\x001d\x0001DÄ\x0007¾_\x0000Ý=2\x001cøËP\x001b\x0000k\x000bíJpPS\x0017L¼Ý¤å*w´¿Sqy2<aý\x0019\Ä³í}u%3ó\x0015ÊáE<ã\x000f3\áS\x0010¡UÜÊ\x0016¯%³\x000cÍ¹j\x000eC©¤\x001brM£>\x000e¸6j\¥aÑ[ý}î]\x0001m2æÌTü$U¿7Ü¡¶`:_ZG%>\x0003F`Ù\x000c§\x00150\x0006ðU!NZL\x0014Ä{¬Õüh
à%»_ìÍg¨·înÙî*\x0017ðÓB¾ÒÏ\x0010Ôcz]ü?r./h3t©ddk\x001eÓc\x0003\x0006±Xæó^\x000f\x0003\x0000ª1ÇòsyØ`\x001bIRÈÌðQ\x0012ýäaàwâ9\x001aè\x0018@\x0012\x001dJ,-Tx¸YîBá\x0015'&**\x000föÁùIÀ9.\x0015ª[_9«2l ÙVæ$ßwb×\x0000
\x001eª|:l(Hýwö¹H
8A\x001b>W[<þ®[uéÃ\x0004\x0005|:Ýdô\x000eèBXxèÔ"sF6!#'ÝS\x0007\x0013­!$ã'µêµn\x001fËøPdºãsCÎ
C]!äV(É3¤å	Q wéÆuÆ_Ö?º\x0019\x0007É>ÏÃ
FoOì\x0008\x0013Õ´4ë(Ý;\x0012ö8Ñ\xd\x001aÂÇùàÈÉ¹1\x0004\x0006K\x001aôU©3·W5¸$ ìô\x001e\x001c¼Ûáhi0Iß¬I{«×Ôn\x0002\x0001\x000bì­k\x0007ðá5LG»	õã z\x0002ÛÔ³ñj\x0014j=äÃ¶Y~ÒÀ`¤OiYx®µnkÒá\x0017úX×Gã\x0017`"f8\x000cC\x0001«L\x0016Ï?jö¿,Y®sÝÛá/B·éQ°Õ[gÚáµë£PÂïJÎ+Õ(Ý2\x0014\x0018AO¤Ò»½Ç\x001a\x0000\x001bÙ.8a\x0015Ê3\x0017³½I8ö\x00055ûfág·æ\x001djC÷\x0002\x001bRD¢C¶\x000bê·\x001cñ¨Å¥=\x00083:`>âZ·\x0002ö¯ña%\x000c
\x0005¹±´\x001b\x0004©C\x000c/ÅLL~9öZÅFnm¤®\x0003
n«	\x0015\x0016\x0011bSDF`¨Ç\x0011L%ô-\x0005Á¤YÂ\x001f¶½»\x0013j,í¦,Á!]ÄV=Ba­¥¼æ¡VßhõGWÖÄÙu\x001c^ÎlC¦pEäAñ\x001eªIÄbE\x0001Òg-®32\x000e®sîb½íÒ&InùÂ²±Ù´'ÎEG@!³@d\x0018Æ¹«ïy\x001a½Ñë$¶a.eS=ÏCh\x0002m ¦¸¿Õ4ò¬§2]8ø¹Õ6zÒÔúøcÈ¼G-Í°ß~?Óù0²·\x0017.÷£\x0014ì*ÓàÄ¦ù*\x0004dëÌ¼*×¨\x0007ñ'9JG}7
üV;¡"AàDÞö±k
\x001c\x0014]\x001fqÈ¦àD<
ÎðÏ\x0010·ÿ\x0013#£ÌóX\x0015[.;\x0013\\x000eØÏ§3È(6p*\x001b\x0015öA{õ	\x001aivUBæârãÀøæÒáÆ{ µ½ÚpóàV¦¨Ë÷\x0003×ø\x0012&ÑÕw^¦+yJªÚàÄÉ\x0011Þ\x0001ad\x0015®*×8æoóm@×Îí_\x001aO,ý/ÀùÒãTzËaC[{\x001c\x001bVrr^Ô\x0006\x0012
åÚÒØ,¸Gý¶
X§[LSi«7á\x0017O¯×NµM:Ò\x000fõ\x0007Å%h\x0000®°¶\3	ü{ãþy\x0013H\x0016ýßHZ´CVÙí\x0017\x0016}ùBiqì©ÉR\x001de"ÕSÒì
*3ºA¶ÆL´§Ò¼å³\x0014lR²8M¥À8U0y\x0018Þ\x0011\x0014º¾µÁeØ¤9þ¿	ùáÊÐÁ*ò¨"G1=¼££¦{iø(~j¦ÞP¤GMMÙäpGy\x0005\x000b\x001bØKö÷\x0012¡»@GNrBé}\x001bóµ^Õ\x0000\x00186É\x0012KÍ\x0011o\x0012\x0005ýPÖçWú\x001bº	2éâý\x000f[\x001b-[hÃÐTã\x001f)0Y\x0006Fæ1«§\x000fÇKmEºº¼\x000f3D/Õß\x000b®ÌÈ\x0014íP\x0019Q	Tú/\x0003=ìll¯#×CFéX¡ÉEjÊÍ´³\x001bì0 ¾\x0000X\x000cø\x0006àq8Zá7ç\x0017.\x000f\x001d¬ìbVkRò\x001c"oVGjê¤zmjØº\x0011Ý92D\x0004Y&
*Ç\x0012\x001fCãûïºëË?ÿªM¸ÖÊxà\x000ce²2²§\x000eô·	ZáwG!NF4å¢
ä¸¸9o\x0007Ú4$°)	çQ!B±s«B\x001cÕÒF³Û\ÎÍFsåM$)Ý× uYµ¤(ÞÀÁ­uÐeH+v!g\x0017\x0005uY¨5û¦é¯$â¼¯m\x001dW¾Í0ñ=çj­\x0004rÂjä?JÇÝ5 "½\x0015*î«tàfYp\x0015Ý3\Q(H\x0002~-,+`»¬\x000f5àHâHÙFS³á$PÁÇ°àx\x00034ÞütH"¥öU7§T¥'r1í*n´Ñ×
xÉ\x0002{É>|§³\x0007\x0005\x0000(Ö§ÀÖßûÌCÿK=D`1äãa¸[Ù! \x000f	~0øï\x000e\x000e	@ æoS'\¨-(o 7úû.	²Mâ?x²w
½&j®ZQÁP\x0005"Q6Ø\x0018Ñ¨
A¹\x001fx\x0000y¨zjzäEâ\x0003B\x0005<¬\x0001\x0016=\x0002Á¦¹MqUôX\x000fM÷\x001fîd#ã\x000e=ËxOty\x000cA:c¶¶¥oNègèÒHiYüÅµÂ¼8«§Ëmqm\0x\x000c«üÂ®õMæ'ÈûÏXçÚ\x0004è\x0006ÝñÑÿ&¡Õ¢\x0006rú%]L\x001d+ëË\x001cN\x0010\x0008jã¼WõTókÈEï¯R$§O;»÷\x0015ºPô*í!\x0004ÏÏ1ÞÝ%\x0016
ïëò\x001a³ñiL90Û¿§\x0006âè*\x000cÁ\x0004lå/æÞÁ8¤H\x0015\×²	\x0013Vô k1\x000f7ö(Õ76Ç66ÉÎ¯ÎÕ HÄ¿X$¿\x001eæ@µ\x0015}àØÇ\x000ew[Jr\x0017ËO
IU\x0002c\x0003\x0010ïEàT\x001eË\x001b\x000blaYéþî¸Ä\x0000,gléE\x0006Ih\x000bQ\x0011åü»o_ÔÄ2W®ú nË~­¬\x0010³¹­¨ãò_»ú©ißf{òÌe¾PÁ\x0010Ð\x0014\x0016«\x0018lPÆO*\x0018IgàÜ-#+gÔ$j`Ô\x0010EÌ\x000b^\x0011Û¥cGÐz\x0018â\x0012h»g´®lâ\x0010\x000e²Û±Ý²U,\x0018o_~fÆ\x0005\x0012\x0005ÓqÁMü¨K¾Éõè#wyýto½u\x0016ÈP®Þ¼ò&\x0013i1\x000fñ2£âò[üNÐ()5Uà\x0012\x001c¥¼*0'Ó))lÆÆOÎCºUòª\x0019XZ&ä·y¨yYõ\x000b>®¶7¾i\x0002úBqs¿¾ÿÓq¬%¢ÃëÞAì [t%P#áÇ\x0010¾\x0019C~I°ð/l*þ$VSÙÐ!+ÅôÚ(+ûgÝ.x&¹: :Ò¶A\x0007\x0003d\x000fNûP\x0003\x001c´ë\x0011\x00195ù^\x0019BÁagÑk-÷\x000b»VU~ò\ó·Ã¹Mü\x0003Hç\x0012¶ÚÄ²há¹+\x0011ÖÊ\x0017ô/\x0000\x0006éZÙKÆ\x0015e\x0019NË§#|e==\x0007~ÅÓsÙª^+÷XÊÔâ¯ÔjôOÌ§KDZSi7Â²ËÎè{Å
Í)§}0\x0012dZ%â\x0014ø#RS§éV|=hñ?\x0015ÆÙàl#aP£\x0016°æÚñÕ\x0012þtÔ/úiZÆ\x0008\x001eÄq\x0013ÀFÖ \x000e¢7Z½ÄD®ZÄ\x001aró+.3ëH}\x0001ª\x0015TVòaã{\x000f\x0002¥uY7\x0019Öa:ðý;ðù\x0003N4-VÁ®;7lN\x0006Dc\x0006ô
ñ+:=³{­Üñã¸¤¤óõ\x0008!\x0000Ó»é@dÁªÆÓÃ}åqp(ýM? á=Æ\x000c\x0006:iXæLÜá?ò\x000fL×üÁ5ªPû¸ÞÆ1º/=o/â\x0000Gõ\x0005ð^ù\x0002\x0004¬Ì´\x0007ªÇGè·\x0002 \x0004æþ¢r3\x0018°j?Õz	C­åÙãâKñ\x0000Ì \x000b7¬ÜhG¡"H\x0017Þ:R¶¦\x000eÓxµÓ\x001cT\x0015Bë{V«
5ÛåâE¯-cÙÖyC\x0005â.û'XþÓ]¶åÑÌþQNC¼d\nóÛ7e6Á6·[ü2ÌÇVj)ln	ì	ô¥WC\x001d1\x001c¹¸\x001bJþ{U¹=ç0ê\x001dîô%æw\x0003\x0005qÆ\x000b»¢Äª|·\x0006pän3\x001c^%Óh\x001cWï³\x0010º
½yÂ\x0004å0\x0004\x0004ØCìcÓì²ìjÐ£åÐÇ-\x0000I¼ü´\x0012â")bõXü£L8ªüf]ôal#\x0000æ?\x001cÖ\x0001Z9\x0000FÀ\x0019ÙÂ\x0005üeýâ:ä÷HU*ÔþÏo¿[Z<UxSï¾ë\x0017è®\x001fQQ\x0013C\x0019=S\x0014ÈqL!DÔ!¤Dåê½\x0002çÿÝù\x0002hg	BÄÍ\x0003õú}o\x0012\x0015\x001a\x001a>Ó"yMIóèR»^$î\x001a\x0015§WË-/ÏÂã~¬\x0008J1zÔ;KòÓÄä\x0018âÝc¬êáç\x00126§\x0013àâ\x000f22LÏoö(Èppã\x0013Ä±¼\x0012©\x0006|\x0001Îx^³5!\x0015òCÓ¼cpN=\x0012w0r\x001eàì(\x0005ª´ª\x0012W\x00160Y)\x000bãê
­!û`ó![À\x0012×ºÚ°\x0015QÔ¬=B+î{\x0012¸BþütAg\x0006®P¾´Ú?Ë$\L\x000clhzÓ\x0018Æ"jRÕLÓ¨\x0008\x001e0\±\x001cW/ÀÌyúlÊ¥\x001emBx¼Ó	Iñ{
0Õ+gÏp#ñD\x001f\x0007¯\x0012§\x0006Yñ¶ÊµÖ¦.íÄ%\x0019í(ï Ç¥\x0001©zÂ\x001ezÖÇ<¼«Kþç¿êË²
ù"#7Òðä¸Oì\x000b
\x001e]Xê\x0004*I¸kÀUô]ºCÿOÇkÔA<IªPu}·ÈKe\x0003£õõ
êÚ[7^\x001e'òC­3%'l;ÓÅ¬¿§©S¼®¥ZÅ^³Å\x000f\x001dor¡õµs,\x001b¯ÿ\x001c§E\x00044¾Éÿ¾v\x0017­0Atè´ÆYñÿ-Pà;Ø±p	Ôü^±\x0016Üã²ò\x001eAXÚd»¢8¾SO\x001aÃç\x001cÄ×·ð@¢O\x000b2J¬æµw[1mòíAñÔÍ°X\x0004a^\x001aXÝkA]J\x0012IÕ\x0001ßïõT ÛÝù\x001e\x0005íâ-br±	þ¹\x001a\x0017';Õ|ëøm9_ÇF\x0015\x0015ä\x0013 ø«°£ÖëµYY$p±þ\x000b@XëýjûÀýä`Ü\x0019)=sË«Åx¿ßãÆ71G´É»&äF)¹.-T¼¾ !iê"È¦÷Æ3bx$\öþ\x0005 /òó´ÊrØç\x0011\x001fÛ\x0007ùþi
xª\x001eÓòæµ êe[úX*e°¾9\x0011-Ç512&¦ÝK±0\x001e
ÆO%^ÂM­AjÖt{Ù\x0003ý[\x000f¢!\x0010ZÄðM§v'\x0001*ª\x0016X+¤~S¹«v\x0019D\x0013OHOÝkö³[ÇÛ'ª\x0013&;7(D´Ê\x0012sx\x0003}>I\x0019MjÅÖ\x0010Kn\x0013\x001eÉÙ@÷j =¼W\x0015üÌéG²bf×\x001e­áé^yµla²ºG\x000f\x001521¢=2TÂ.ôÍ Þ+ù! >¬LDA_!=C\x0016/
Ë"]\x0006í\x0012\x001c»Ð%z:Æl¸J\x0019ý})\x001f\x000b\x001bFÐfWÑÕ\x001a\x00000+Å!7¤-Dc0ùV£½ö2u,F\x001c°ÿCÒR½ÁcÊûø\x0004Z×æfaìRF\x0005\x0008@\êèw!9\x0011ø\x0008,éïÀXK\x0016Á;û²ð\O!5\x0010\x0011I\x0003<Ê-\x0012¥£ý8É©\x0010ú{õ÷B	\x0012þKµÔ/ÀREv¿£¥Z>d\x0003Y\x0006½µq,\x001dîi§¹ENás	+²j\^âÖup¬u)77Üp©î\x001bSG¿ûÈ´¢P­öå%¥0r-¬\x001bø\x0003"ÿæÛ$Ç(~ÂUYU@\x0002WjtRÈ`öÉ\x0012\x0015TÆ3¢ð@d3\x0000jV9I¨µÁ|0<í\x000bÐ9ñ¿ëÎxÓBÞ\x000c\x000fv¾\x0000²U5Üll!Ó^ÆêEiÈï;¨ë6+?PSJ¤&¢sqÒ\x0010USÄÞ!èùEe4d¥6NbÎ¨,.S(¡";W§!\x0012Á\x0006¨\x000e¢é%\x0019TæøbØ)ÂdJ¶E¸¿\)ò\x00110\x0019æ\x0004\x000cvîCcè_ÿü%×*lCjÞØN\x000bh¢½Z}.¹òèHµÛCQÜì7\x0010S\x0014îüô\x0000¡Å{(ä\x0004ýÝì"£yGe¡ðó.»óhÉ­\x0008\x001cõ3÷µª;6ø\x0013±ûhõ­
£AKÄ\x0014L\²h2KNc3OvÚ3åH$ù#\x0016/r>û\x0008ºi^ÏÃùÖ\x001aí*I­I`\x0011¤t¿Vcû¤BÂ»£\x000e!Âè2K6¹L´+w_n\x0008¿zOÜÛé²©×\x0014ÄúÀ1p¬ÃùKÅø©+T%ºã§\x0019Ñ\x001dM@é<\x001aô8qºã;æº>;M\x0006¨Aióá\x000b ¼ÔÄÑQçPëf{7Ì\x001c\x0014Ñ.¬2×tÔðÛªJW"Î8&\x001d\x0014|}ô0%§Ój"xæót½¨\x000cP÷­À_×\x001fö@Ü\x0007.Ïë¸dË\x001e(Á\x001b{Õ0\x0019àÙR\x0005sh±æîvbÌuj\x000ccï?mÎ¬u¹Õ\x001bãÐÉ\x0010fÖà7O|\x0003]^nø\x0011Ú^§\x000e»§\x000e4lÔ\x001cø×'%Î\x0016\x0014íØz5õª\x0016\x001a	&ò·ßä¦(\x001déÆ1ïx¦>ûêÔ²¦ À\x0004æjU9ÞþXÇc
\x001bqòyjB\x0004\x001d4&@aJ?\x0008~\x0001t§]\x001a1\x0017ª-¸Ó¹\x001e¡Í\x000f\x0012e/kê «ÝGkÉiéz|@HDmq\x000eÓÂý9kÇ)\x0014üíÓ¬
®µð@zIøÇ\x001a9½¹}èÙ¶\x001c¿\x001boì\x0016
°8æ±¼¶eÊÆN\x0000²mÅ|\x0017\x0005þuö\x0011\x001f
¬ñ'Ùgge7$Ï¹ÁØæ71Ö\x0003gO£\x0016\x001dÍ\U\x0016³h
ä¹\t3w/Ø\x0002°¨\x0008Æe!íC¥gH¢¬ -D{y\x0004d\x0004Á¥$×,TÃ¥\x0004\x0014iY\x000b¡¬se.ôÏ
\x0002
E4iWAÖ¸@ª±¿\x0014á)\x001eñ?[rÊNWz¡\x0001å.\x0004Ó³üdnº÷\x0011lÚØÇyÅd¥®ý\x001b«Õ\x0008äîjMG}Ó¬Á\x0012ò\x001acd|\x0001\x000brÈ	Ã	\x0008¯AUÚ K£Nð2´Ë«f	|\x0012ü\x0018\x0012¶­ zrA\x0019½öî¶'->q ÇQ\x001e2\x001bÈÒ¼¾Oý\x0000MÖ]Óv\x000erÏê©ï=ñe/:\x00012¢\x0000­y?À)\x0010Î;Þq¨ØC¿Àÿá^\x001aÏ9dL\x001f
?\x001fØb\x0002äYïÝ¸ñyuSìÂ\x001cÃBôE]ä\x0011í"®å;&ø6ÕaáPø8p¯t\x000f~	@e\x0017X}ÖéÀJ\x001c(IØ"5+0S\x0018¨ÃW²
{?3uuü¯r\x0012z%R\x0013»æòvC¤ïÌ¦\x0015R\x001f3MÓ+ôãøoÐYB]e\x001c<\x0014ÂÐK\x0003RÊyö¿\x0000v5O.®_\x0000îIU\x0016_J:r³OÎÓ*õzÞiøS0çÑ/Í§Êt3\x0000cÐdSÅE\x0004SÜõ£â³è¶K!CóMY\x0007n©#ã#yò¦È\x0000¿\x001c:>i0é$ßíC­Þ\x0004L´1²ÿÐü¼Dû Os2\x00053ÐC ÜþÃwÿT\x0016ÒW²ÜÊM¦éçP_ \x0015wùòvOÏp³çó/k\x001få\x0003 ü´Ã¿ 0ñ©EÍ¯Ù÷JWIÃïOF]h½ºëËþ¨¶Ë¯Àá£ÉÐ¨Â ÷§O
P-\x001b	¤uK\x001e\x000bÇ±{\x0003\x0017xÇUd7! ZüíÛ¢:[m´2ûµ¾TD\x000b\x0001G\x0010\x0006ÝuÛ|\x0002JÓ]êÿ\x001e\x0003ºâ´ë`tùf09ëÈs­£®ôks£¢Gád?ºX\x0003¾\x0010"µ¯ª\^ÛQaª\x0004\x001c?H£½ý±ûaÇ vÒ
B»Ò\x001evÅ;H¼\x0013\x001cv\x0000{6\x0002¡\x0006ëTôYk¯&$Õ~ËÑnuéÍóXÌk?ûF:B³u\x0005ÑµÔ~RÏTÂ\x00017\x0002èß¹aõùòq\x001d³þåA\x0008\x001fBéëbÕ®\x0004ßðÙx©µÑ¥ì	3¶Ì\x000e±Í~Å]_¿¨5´6eêU\x000c}^íÀ¯Ïí
ÏßP¦pÓ¼pÿ-Í"ìë\x0003Û Ïjü³
Ä[¹Aæü\x001büâs5~\x000e
îÊ#çñÝV«^ÄvcÑau	H{ÒÅ6Óê»Hâ\x0000»\x0014ùóh¦ÆñøÂé\x000ekht¶\x0016ÝðØ8±\x0018Åì8ð®\x000cÛÙ¹,\x0013>Ìà\x0015Gea\x0010]?Ô2çµ\x0017¨âÜË&xTõ¤8Ù@,·Ìn6´Y «+\x0008\x0008f\x0006í»`Æ[N\x0007½ø\x0018ëE-\x0004¿¬\x000e8û: Õ\x0003 £iáÅ"Îo\x000c´u¶Súàì±é#m\x0006 ïb£¦)ÃÊ$`\x000e@\x0002\x0010¯ì#\x0001^fZTï\x0005ò·/Ëå9r?\x0001Y:ËRø+«ûpE\x001fÂ²ç\x0003ÃíÁ"3ú\x00181\x0011DÒUX®\x0000
\x0011á\x0001E[#º@b÷·ß5T¶<Èpª8PÿBfTµ5KÐ«Ò]µÝ\x0012>èÎCYXêyfJ¿a,ý íeÁþI\x000e\x000fÙ	\x0003\x0005u\x000c÷:KÇ\x0008\x000f}ðC\x0019*5yp.K{X"ïë}cº¬ôv¡Ö\x000c\x0011m\x001c3Ñ¶ü¯òS\x0017\x0015\x0001Ú§T\x00149JÈ$,&õ\x0019°Ïú\x0005Ø\x0016K\x001a¡gféwn?æ¤PisÙ	[pQi²äbUÀHö 	`?U
IL&Èß\x0003~Û\x0010ZÚ\x0017Úx(c@SDe\x001cÒ<æØACTäF­\x001e\x0011þpQûZx¨Üú£ÿ8\x0012:\x001bà2ö=ìRß³äVÏVe¦\x0005
\x0018¥¼â5lZð¼>Cz'â k@²zå!u±ôÎÜé¨7\x0005vÚL)	M,hä·§ñ(G<Ù¢Qs§éÀå\x0016<[a\x0000Ç/V(RÈÀKQ8kÞW\x0000C\Á0a1\x0004I®f=3¼z¼ÿ\x0012Ô|\x0002=nÓ­eÕðÊÃ\x0000\x0018#±OU\Ü_®(sõ8\mâÛnê\x0015îØÍ\x0017 º®ßU\x0015\x0017K·Ô¢+\x00172@êY©ýÝÍ\x0000Ò\x001bóÎ(ûî	gæYÔí%{jéqÍÇL \x0000ÿ6ùECbÑÆûzó­~ëþ¹Ã\x000cç\x0019®ÍÚ0b\x001aCéómÁjÕÃÇmÔº·\x0013p*\x0000úÄôeòÌ±>\x000cè\x000b°â »ð#ùc|\x0005Ú¬ü±âáCõY±;#%=9qªë\x0008\x0015My«EAÿ»éCÃ¦Í=T\x001eTåx+b=¨Zh
A³S==Íxÿp¦]°gX¹@µ@¿É\x001b×:¢ß¿ÄÑS÷­ê\x001dn¦âOK¨ywdüa\x0016	ê\x0016\x000f}\x0000<0fÜÛ[Áoð(\x0000õÏÄÈwê~C>]ûÝ[¯Õÿmfþ\x0015ààÃÌt\x0010 ¤èJ¬höº"8:Së»I½¹ÿ
\x000f®9©8UWðr1<¤(âRÑÇ\x001em6BF9<\x0004aá1Ç¯°¾fiæ)Ø?\x0006õ0@ªMe]Þ.ÇHðïxm#ruåþ¹~dü¾·ÆY~Ön\¥p/©"~:\x0015¨Þ²Ø\x0011mBÑï´,s¢-t/)Ï»ä¿=àýìuJé\x000e¦µß3CE\x001d\x0017ÒgA µO\x00102U´9ãqÝs/ècÕ+8º¼Ã µõÚößÇ®åFß\x000bx©Ò´@ÙIh\x0007àÑÇÉAP\x0001KÎ´å\x000f3Z6,Â1Ni\x0007\x0000CÙv©XéO¸ÄcËðí\x0018ÂpëÂß<õ¼¿½¦\x001dú¤¤
è\x000eBûÆ/Ýå#B¥M°¶C
¡|êCª\x00023ý\x0007HÃ$ÓRG-ël-#§I$ìCkÜ¼#óg%·¯\x0017û$Õc;yÌ[&÷\x0012<ö{µÃX\x001d
rÔU\x0015ã\x001a?Ò¢¶¥´<ßÊX>Óæ2\x0005i\x0001}Å<\x0002*ÁRPÿç,#¯ªèµ\x0002Á4«¬+.@N\x0018J\x0002àºÔé®E\x0018ÖÒ\x001eéçþ¢=Ö5á	äí;ýßÁå9\x0005®ï=\x001féef\x0002!\x001c=ô ß¸lWU\x0010\x0010ïn¸[Þ\x000b¿eçÌãxíYÎs\x0004ü41âã:d8&(û©f/}¨ ¿9«¥C"Ì1©vX¾{i,b\x0013W¼ø0º¥¾ òÍþ%ß\x000cÃØ¿J(ù¤9W)`.\x001dk	jü}@ÇP'ü¼¨\x001b+9÷\x0014¼æP¿ÞG\x0010ÿ¾Êj®Z|\x0006+¬ëí¬\x0007\x0015GìF~\x0014ÌÀ\x0015[ò<ïÐpAön#ÜÀá\x0016gSL²ú\x0005\x0018©VKîÜ.eÞ_÷Æ?Ñõ\x0014Q&DMðv`cÿ\x0002@ù\x001fß3\x0015C|\x0001ÈG]®Ç/s«;t3Nª\x0005"¢Í:\x0010òÖßo\x0019¢\x001fÿö¤yûý8þ¤NÞÿììý·Ø\x0014ÚÀ1\x0006f\x001cø-mTª
î1¸ü\x000b\x0000ÿôÓûsL÷¿I$þrWêùÈûoi\x0010vS1®¬\x0004¸I[ôåî_5åÓ6B1ïÏ«ÒÜqtXýÕ=\x0013AÑPBèçEãHY+·6ö\x000fù×âØ\x0017ºÎ\x0006gôlº``?Ñäÿ
üF\x0003¹Í\x001c¨\x000co\x000bÙÛ©\x0011ÞÝ¡8çjgùT¤A\x001aàë\x0017ç\x0019Ág'ù\x0010
j+û0úG\x000bÃ4Y\x0001<?`dIEö ÀgÌ\x001eqÄqL\x001eE7ìdPïRaÙL¹\x001f^¥4ë\x001býÑÏ-ãþ k\x0002=>\x001b+9\x0019^i79\©Ú½¿2?*4
NOÄ|:~¹qh³¾Ø\x0010d\x0019-Î?Z©m§^\ÿ\x0000©Ø÷Âð*´óÍq!yäy[\x001bC;\x0012p;d×±ø~(NdÑ"ð#\x0016\x0019äëùÓ\x0011å7\x001aeÕ¸Äñ2×"+Ç¨nÁâ;¡ËÅì¼¾ÝGoCì76P\)YbV\x0004w®#Ä~\x00161#ÍhÇ²gÂì2¥§mçÛ_~ñ>Yc<$d`ç#ÝÇ¸¨î<!n	2\x0017\x001eßþºÎÐ5\x0003TOâ\x0000¤ÿ\x0000~2rGõ\x001eùõ5ëÐ¼7VñÏ\x0003¬J¡ÑáéNÂ<kAlªË\x0005Üm¹&W ý?\x000fÖ¦Òu\x000b/¶¬:Ä.°ÉòJÑ¹Q\x0019'ýjÇÔc\x001dÇ¥zV¥£ÚÞÆUã\x0001½q^oâ-\x0016M9Ø°Ü |Þ¥_f3¯»ðF%Ï\x000c·B?ùæ¯ý\x000ejêøOEH\x001b[ùpOÚ\x0018\x0011úÔ>\x0005Ô¡áÄI\x000eé¬ßÈbO%z©ü¸ü+¡lç¹§d\x0007\x0015®é\x0016:|\x0002[\x001bib;Â±i·>ºl¹\x0003\x0015­â5i4ù\x0001»»pG5ÏiÒr\x0008®jÈë Î¦ÞB1Ï\x0015}[p\x0018èk*Ûk(­\x0018{Á\x001aHãüafm5KmN1ò¸\x0011¿Õy\x001fãð­Ô`d$t'#ñ«zÎ5=.kSÃ°Ê\x001fF\x001cý+#Lw:}«H0þJîÏ®+¶®¬rUVw4ãlJ
Y~¹ª üÀÕÐI\x0018\x0007ZØÄ­2X\x000e9§¸N\x0003\x000fÊºOâ|S\x0002\x0001Ì?:vÏzK}ß¼N½ñUrÃø\x0000[+Å58Àüê%Ü{ÎÔó@\x0007>ÔRóÚ\x0000´\x0010\x001d09\x0018ÁÆ)ÞX ä9\x0000u\x0018üºÓÌHyÇ\x0007Þà*\x000c\x000cüÛÎEdXÄ\G9ÏøÒ*²v\x000exÚHÏéSªá\x0015q»\x001dK6iJsòwãû\x001ab Ù\x0008
\x000eG\x0000ñÿ\x0000 Ñ°\x0018ÝÎìäçõ\x001fÒ§*Ý	$\x0011OZ\x0014\x0012:¶\x0007|Ð\x0004IËóñì½¸©\x0011SvF0¼¸þà\x000ez6sìsO\x001c\x0013sØÐ2!\x0012®Ð\x00161Ï¨#òÅ;ìÁmÇ+à\x0003R3.y~{sÖ9^7~\x0008@ªù\x0007\x000czü\x001a6ò0\x0006\x0008ç'#òÍM´g¹÷&§x=Í\x0000Ba,\x0007Ìp=1þ5)\x0012ñóg\x001ccõ§`|ß¥/=:þ\x0014\x0000Å.ÜuÏ\x001csR\x0011.Ñ´g'À¦³²+;îÚ9ÂzO¿¶Ô­~ÑnÎSqB\x001e2¬¤u\x0004\x001e\\x000b
\x0018ã ñÞ´\x0001_§j7`v?\x0003Ó­0+\@0}0\x001dX)¯,ñ|ò^xXU\x001d°'\x001dûô÷&½^GPû\x0018©?{nFH¯)ðäÚ^3G\çaëÔÿ\x0000%`¹gÄ\x001a\x001fØ4+\x0019SväûÄ©\x001fxWOà\x001dCÏÒ\x0016ÂB\x0003G¹à$ýäÏÌ¿Ucù0­MnÃíÖ\x0012ÂSï\x000e9è{Wé3h÷þ[·¶PÊíÈA\x0018ÿ\x0000²A*Þ úM=u\x0003ÖÆwcr*´Ñü¤0-Éä{ÿ\x0000Z]>ýoítR	Y#'&7î§qÜ\x0010EX;!'\x0003\x0000õäPÁ\x001egâÍ\x000cÛKçF>Wê:`úý*ïÃý|ÛÉýxÛcwýÉ'î9þ\x0013ìÇ§¹÷®î\x001b9á?Ýæ\³awo8ç\x0004ûã½yÎ§c.¨îòÄ¨8ee!e^ãÛÿ\x0000ÔE(°höR	\x001dë\x000fÄV)s¦\+ÄlAÆy\x00035GÃ~)µ¹·X/.`£ËN\x001aOUsýñÿ\x0000u\x001exË[·±Òg·Yãk»Ê*£d¨<glÓhW0~\x0017È~Ñ¨Dßuã÷\x0005¿Æ»»·xá-\x001f 
ÂX·oÃ­q_\x000e-e\x001b\x0016D\x0000OL\x0000{zf»ì~ò\x00100\x000f\x0003æÊÑù±mþøÁùx9\x0015ÁÚ\x0013\x001bìn
µÖøê¥£:c0B>|*g9ÏWìFzW/p\x0002ê\x0001p\x0001qOëXÕZ\x001bÑvfåÁQZðJN\x0008ïX\x0016asøV½³\x001e@\x0019®]ÔÕÍ5|MÂÎi\x001cÊ¬¬ºå*b\x0013*U%H*p~­iÎÌÂp¹VãAw\x0004Ùj÷1`ã\x000c¨Ãù\x0003Q.©¢O\x0010Ë»ýVµãy\x0006âÒ\x0002	È,@À¤/q³&D^y\x0001wdcð5×sÆtz\x001dÀ\x001f¿×¯\ôÊ¤j?ô\x0013S®\x0008@[Q¿sýï5W?Ö´¾Y;q\x000eO¯ÓÚ\x001f\x0014 \x001c£úQqX­\x001e\x000f8º¾<u3ü,^Ãk+õ\x00120'ñ«ÊUk}Tb¾`\x0008o¡\x0002\x0018Sh\x0008_÷:¥ü#Ór·ó_ëP¿ä#kPÏ®Äoè+¡Þ»	\x000e[§­5âÜÛ|ÒTõÎ
'pG04
@®½sÙ·¢ºF7ÉÇ½\x0014j3/jt\x000bÓëH
Ç^ÜÓ\x0004\x00100~´»HíÏµ\x0000\x001bÈá?R)Tè?AC\x0002O R\x0006ÚNS8ú@Az\x0012KgXÑãaó\x0007mªy©£\x000eÊ¼\x000c²8§¥y`ÿ\x0000\x000e)ÛT\x0003è:Pj(7î\x0007Ú\x0007RE*ª\x0011
p\x0003\x0018ÚqLCr¤1íO\x0019ÏJf1'
¸õ¦ÞHd2íÝ³98õ>\x0000JX}\x001eµ\x001eò¸b¥S|Ó.$¸T&(Ãc¹p¡qëÔ*ùS©EåA\x0003\x0019â\x0018f\x0019á[èA Oç\x0007ZöÞAÿ\x0000\x001e¸!±çm\x0007\x00074ø!åie]§Ç>Ù\x0003õ¥}Gbràr¡»ò:TV°µ´r*Í#ïrÃ8'Ò¬ykrÃ\x0003\x001dx¥ã×õ§a\x0000¶òF}}i\x000cÈCÉ×écÆ\x001cåN=±RycËÚ\x0018qßhj\x0000­vá]\x0018ã-\x0019\x001d\x001aóo\x0002\x0011\x0017ãº\x0007Ô\x000fþµzdà0eV*W\x001càãÇò¯+»\x0013èþ,3F¹xæóT\x0001÷½Gâ3BÜ\x000fXqAïúW\x0011âÝ\x0019ûlqÆ$^¹\x0015ÙYbx\x0012çí\x001bãC \x0018Æ\x000f#¥-Í²Î¬AR0F(a±ç¾\x0014ÖäÓï<·>\x0017\x0018êfs·Ý×¾£+ÜW¥+$Ñ\x0006FGE\x000c§\x0004d\x0011^Yâ]"]:çÎñ±·£\x000e\x0008ÁÏé]GÃíY¯l'³{fÜ«þÃ\x001eØ6\x0002)Þácrâ\x0006Iã\x0013¦ü)Uazý?ýUGVÓ"½´dºüÎJÆáéÓÿ\x0000¯[*Î&\x000b·x|ê8\x0003ßÐÔ	Àù?Ò¦Ã¹ä·zMÖtÒDÆ.Ä¹\x001bëÛ\x0015\x0016¡Üê\x0017cpÈ',Qvõ£c\x001bÇ²tY\x0007«\x001fþµ>\x000bX \x001f¹WýÓOQhRÒ´å°³HP\x00058\x0019ã<zU£k
ä¢l\x0001¿©\x0002¦E6F*2[°¦ãwå@\x0014o-ØÛºÄí\x0019a \x0003\x0007Ö¹
^ßÈÔ\x0010ñóÆ\x000b`c$q]Î\x001dNîÝ2½*;=*\x000bKÛØÄÌ3å+\x000fR;þ5\x00126Æ\º=ÍÚ\x000cE»·\x000bùÿ\x0000t¶ú+ªþöt\x001eÊ¹þu¤\x0000;\x0001À\x001d*Q#B+qÊ¼ÅhôÛdã\x000eßVÇò©
¹\x0018ØGÑN\x000e)rsZrG±;îS6\x001b\x0002¹Gb9üê9\x0010\x001e\x001d9\x001d8Æ?:ÑÍ!;\x0008ÏÖ\x0005ÌÔ\x0001rw<ÏN*¹PÇ\x001b\x00030\x001dTíÏãÚ´äÀÚ\x0014Ô\x000c\x0018Á=?Î)4\x0017\x0005Mª\x0007O\Òð1ÏÐô¤VÀÃuöæäg%OÓ\x0000q\x001c\x0007\x00189¥Ê23¾ãÈ^½ù¦(\x0003'<îâ,äz*\x001dÌß4S\x0011Åÿ\x0000Âm¤í8äàt\x0011/øÔÑxÃJX.K\x001eÛ\x0014cõ¯;³¶ð@8==Mn[XyXÜUA\x001dIçéXÊV)#­\x001e+°-òÙ\ø\x0002ëHþ(²LfÖç\x0007¯Ý\x001fÖ¹Ï³\x0000\x0008R8ôª×@å¤ðI©U\x001b*ÇTÞ-²VÂZNã©ÎÑýiÆ\x0016{°7,sÎJë\Ya4þ61ÈP:±£Ç]ÿ\x0000	}¡\	É=\x0002ºümh$	ýzÎ{o\x0019Írfä7¦å\x0019\x0006Ò\x0000\x0000\x001fÒçÿ\x0000¦à\x0016A8ëÍ/i"NÒO\x0012åHÉ\x00146îOÐv¬Û[øâ×%½=÷/ÇÎ\x0001H\x0003 _P\x0007r}k*kÃ¹­ÑBîPç#§S¨U¤#2d&7Ç#<c¯½f§S¸îtcÅF7y\x001eÉ¥n3\x0004ÈÏLcÜÓí<ngR#Ñäeì<áÏ°â¹ç·[Õ»ã\x001d@Û953É\x001b\x0013\x0002n@F6¢äúgÐÕ{Vk?\x0013ÍÚÚ\È \x001dÊÓ\x000fð¤O\x001fE½Ul\x001dTñ0Àý+\x000fÌhàeEÞ\x0014m\x001989î\x000f®9¬»¸|ÙÃÄ£À\x000c\x0001ùUÆ¥Àîäñt±Í\x000cÊ\\x0006\x001c}qõ¨dñ» BtðÁÁ92r¾â¹K{©§Mà#ô\x000cç>?\x00068Ñ÷rw\x000eT·^isIhÀéá<}åF\x001eyÿ\x0000Ö©Ç\x0012lÜúh\x0000ð\x0000õé\b 7\x000eìC\x0003Î:óO\x0017\x0011Ë(.£\x001fZ´ÛcLì\x0014\x000c
5²G?¾\x001fá\Þ¹~u;Ä»·ìÒFr¤>[#¡üë:f6ì¾g\x001bÏ\x001fJz0ÎqéV=\x000eJñOdþ\\x0005Ó\x0018ø0HOÌWþ±çýHô­!ãÛM6r	\x001cuà×\x00107Át·Vò¼3¡ÈxÛ\x0007ó§Í{\x001cÈLö(f#ýd\x000fåîS\x0004~X\x0015OQltZ·ôýJÜÆl.\x0015Éà³¯\x001fäW?ámXhÚÉ¹h^XÌO\x001b `	î?¬ß6ëÌ_-H#)ÐÅåXåSK`=\x0004xöÓ\x001bNºSÓåOó¥O\x001fÙ6L7j3Æ\x0019\x000e~¾õÀMjZ@o6#îX]\x0012OvAÅ9> é­÷­.Ôôè§ú×äçDûÍõ¦\x0016G¥\x001fhäað\x001fúâ?øªpñ¾p	º_ûwÿ\x0000ë×úðzñÍH\x0007z\x0000ôÛ/\x0013éúôvvBé¤¡1m
1IÏ\x0018®\x0017GR\x0013øF+Ï|\x0003d\x000cwú\x0004´AaOø\x0017/ú\x0005®çL\®þIl¯åW\x001eä¾Åäþ:ÖmÆ§ad\x000fÚnâR\x0000ùsúV%÷m!%--&¸#»6Åþ¦\x0011ÖÒábñ>¿~Ð´ût_]¬ß© U/§S´Å\x0018ÿ\x0000d ÿ\x0000\x001a\x0002çgÎj)î ·\x001f½\x0013ýæ\x0002¸ÆÓ<Upqq|Ê§®%Àü\x0015,\x001e\x000fRwÝÌÎÞ«LW7dñ\x000e\x0013áïc.N\x0002¡ÜJIuF·¸¸Û6ËuÝ 	ÎÞäsÈ®wPðèÓ@º·%âÈ\x000c\x001bø=ýÅQÖ®¦µÒ¼µpÞ^\x0017´\x000cÊ-.	»ØÛ>1ÑÀäÝòx\x001eOÿ\x0000^þ3Ò\x0001\x0000­Ø>¾Pÿ\x0000\x001aàÎ
ÒHSnçb\x0017$çÓÃr£¸\x001e8ÒÝCG
é\x0007^yúÔw\x001e9°7"Öì3(þµÁ§Ík\x0019ÏaÒ¢Ô%\x0002Ïowaùu¦¸¬;añ\x001fM\x0003þ<oò\x001føÑ^dM\x0015v$éá%\x00171ðäí_öG·½YX~`9\x001dÚ%\x0012Ç\x0013¯\x001b³ÁõÏÿ\x0000ª§d$\x0005Ç×5Ã&îh1ón]ÞàÖV·pð^Gäìm©¹zÖÂmï\õÁSBIFr:ÿ\x0000\x0008éúV´É.Ç¨»¡Ù\x000eÕ\x001d\x000brMFó±\x001dÉ`	\x0005OAøQóÈ¸à\x0000qÀàS|¶U\x0007ràdÜ§kq\x0016EÈ]ÈPv#­I\x001cÞd®ÀÛíÞ¢´D\x0016\x001dNz
XGBfG$í=øÑd\x0006ÊJ7Þ$É98\x001d\x0005Aæ¬K mÉ¼\x000bdúê6,\x001c\x0003\x0019;N8?Ö£º\x0012:áT.OÊ\x000fn*\x0014uÔ\x000bP1eó·¸bÄ
½;Õ¥ùl\x0014\x0010IcÉú~Uc$LgwÊNâO­^JFsÎN>£f\x0005ò\x0008¼¸ðÀÙ?äÓ"\x000f\x001d¹\x00042\x000cwì}j;xÌM¶Wl®\x0008\x0018ïëøTS\ÁiC»g¦z~4%Ñ
j0]<RK28=\x000f­j\x000bky*±Þ\x0010\x001c9\x0019ç¨ÅsÒ\yAHÔáqWti
$mÄ|»°¸ÿ\x0000\x001a©ÃKÄw¢[i\x0015ÆÆ\x0007æõ\x0014Ë7\x0007i_vÜÕí\+qÐäîÏùéYXÜFáÀýjàï\x001b6i^i\x000crÄþ\x0003ØU9È¶±ÿ\x0000Vç×ÐûTe\x0014£9\x0000(éùÕËí#ÆÆ9\x0014\x000e\x000ei\x0011C\x001e{óV¢S¨iàn"à1þ1èjr\x0010@Í2\x000ci\x0003$Ô1'9ã#¥5L¹\x0004íKÉÆh\x00187µ3\x001c\x001aSÔ£¡Áê(\x00023èE$|úÓºDá\x001d(\x0001BõÅH\x000e1ô¤\x0003å4á÷G<R\x0011Ù|>Ô|u;it[\x0016p	Ç?tË\x001f;WñLR\x001buhã8\x0001TáTzûþ5¢Êh\x001a¨7;K\x001aqé?©¬ÂLLd#q^\x0000=*ÓÐ¹ÓÚè×w¥\x0007Ø\x0004÷­í+Â\x0011${×2\x0011ü=ªM\x0013RK}2ÒGä<c5·o¬YKÇ\x0007±¡\x0008³\x0014\x0011Fc@ª\x000608©UzqK\x001cJ¹F\x0004{\x001a~ÕÎj®\x0016\x001a»»âóÅ)éÅ R:Ó\x0001FFÉ"F\x00042ú^uâÛsk5½»\x0012Æ=ÛIþ$ÀÁúö5é
Ò¹_\x001bX\x001b­1n¢LÉhIoxÏ_Èàþu2ÚÃ[ÜóöaòçZf\x001eA9ú~\x0014®Ã\x0000Ôs!'+Þ±[½Ú7Èq\x0019\x001cqTµY\x0001¸\x0011?SVmØ\x0011·n+)É#;uc´\x0013\x0014Q¥\x0015D\x001d\x00042¹N\x0003`\x0001éS\x0007\x0001@'+>ÌKq4p[Äï,µ\x0011z]l>\x000c\x000fg'öÑ\x0012º¢\x0016á\x000f×ø¿JäP¹¥Î\x001fRÕ³[Ù\x0010\x0017£8ê}c\x0016Ú¹\x001fwÑø"\x001b\x000b_2å~Ø{²±À\x001eËéùÖ't8¡¶{Dòö²\x000fºGCôÿ\x0000õÖÉ¤ùHz19 \x0015ÇN)vr	>ô¬årSO\x0018Ï­7\x00104!/Ã}à:j±\x001c1¢åPç±Æ\x000fáUàÆ«P@ÈúG¾$\x0000cïÈÏ"³i¶\x0005Øc,\x0007ÈWæù9©Z\x0011#\x0012È>\\x0006û§8Îj\x001by]l÷Fd,ë÷çi©CË&Kªüª ³¦W9\x001d~ÜÖn÷\x0019_ËÛ)Ú6ÁÉÏ Tó1ùqÆãÖ¨Ú\x0017mÁd¸8À\x0000ö¦FN\x001c\x0007vv9 \x001f½ïíO]Ø\x000fÝåÄ\x000b\x000c¶9\x0000ò	íúVMá+3&H\x001c\x00123ÔÖã2ì\x0000ü¸ g\x001d\x0007qüë\x001bSUûQÚpqøURÜ¨nS,»°T\x0011ëtlËÆqÁæ¢Ç\x0000þx§)ÇqÞº\x001a.ýÍIÕ'²´1x0ã\x0018\x0002¡ ß3ÛÏJ2êª\x000bs)îÙV °öÏ\x0015	XÆ[ÌÅ<\x000e¸ªù«1Ú\L»¡F\x00078Àëô¨
àà\x0008ã\x0007­4"þ)·pÎ;f©Eö{÷\x0003\x001b[\x000c1ïÍ%É\x0011njùq\x001b`\x0003o\x001e¨¹H¬[$6ÚMÙÁéjØÒ¨ïé@\x000fÇ\x0000æ¦·¶ém¡R«¹.p=j\x0012Ù\x0018©¡KxÊã2	RA PÆV#æ\x0018¥æ,}ép\x000e1K\x000e\x0007ÇéB\x0001@\x001cÒg()Ü\x0013ÇOzP¿)8äP\x0005:ôÚHÉ&ZÞAµÓ=}þ¼Vµå¤PJ¯÷f\x0003\x001eþ°6d`Ô±^]Ç\x0017\x001dÄ<cfr)¦&®w\x0017[k-mç\x0003\x0013´k×¸\x001f­tQhc\x0018AZà|\x001eâK&<È¢d'Õx?¡Ïá]íË\x0004;grv\x0002}*âK,Ìyp'ÍØ
r½ñä"îjÔ\x0006&PË}jl\x0003Ò¨¬sL§\x0012(ü*ÂK»­;`&ËQÍ\x0000)9Ze*Ê\x0008#\x0004\x001eTpqG\x000c3@Ï\x001e×,³u«@\x0008HØóÝ\x000f+þ\x001fPYÀE\x0003sð\x0007Ö½\x0017Ç:)¼ÓÖþÝs=¢À\x000c¸úÏç^q1Ì\x0005½Ö±jÌÖ÷D7\x0008ÐØ:°*è6\x000fCVf\x000e\x0000\x0000}+Fs?\x001cb½y=jæ¥<L.n£ùº¢\x0013{wö¦/R(´ Ñ)õbr>dþïµ\x0015µì~¼*yXô\x001d'L°Ó-UaDÀÃK»,ÿ\x0000SßéV¡¼âIc?6ÃTpE@m"\x000bò \x0000\x000c,\x0018\x001cTÑC\x00140mp9lHîz×*çþµ\x001d·!\x001b@#¶=k×ìÕ#»R£-ØÚz~9®\x0014m¸*IÎ;þ½q_\x0010¯ÖÞ×ì6Ò\x0003-À\x0001\x001cN¤ôÏ\x0003ó­íÌ1_¾3VUY£\x0005C\x000c\x001c\x0012;ÔR\x0003¼|ÇÒ¡°£p\x0007¡Ry5³\x0011>D1\x0012=½êKXãGL÷9äUS\x0014Î¤Û\x0006¤\x0003É*Ê~ïëRÖnZ[\x0008®\x0000\x001c`ãwÔÕÈ<[\x0008VÁ<\x00039à_¥b.¢_åB\x0013#\x0018­(î
 À\x0018 pF1þ5Í(µ¸ÑCTr=¶\x0011°xluÇ|zÕ[m@¢í*\x0006\x0017\x001b¥K{\x0004ÍpÄ+\x0012Ç\x0003>A¡';\x001b~òÖÐI«\x0012i. ìû¢\x0018b0>×"\º\x001er}*Rñe\x001bñÚÌ7.ýÄ à{úÓPì;¼\x0010FTÉ÷ß¨\x001dB\x0012Ü¿\x0012\x0019êHéô¨Ø±9$àtÿ\x0000ëÓ\x0014sÏaÔö«+Yb§\x0018\x0008\x0000ã½[Ñ-Òîä´ÅLQ\x0000Ì	ûÞUJ\x000c
£ñ\x0019«VÑÉ|¨]\x0001ëÇ·jRVDõ7^xÝöÂë¼dáOÝÈçéPÞiâö4,\x0007\x0017\x001b×úgÖ[(,%V\x0019r:\x0015\x0005XmfÝ\x000f\x0012\x0000êab\x000fâ\x000fô¬Ô_CD´ÔÇN¹¶É"¨:+U\x0006%Ç\x0015ÙÏåÌ2®¬\x0000\x000c@þ%=Åq÷0ÉkpðÊ¥\x001d\x001b\x0004\x001fÒ©;(ØãsqN'\x0007>µ\x001a¶ç ¶\x0006\x0008$ô\x0015§.¹w!`V\x0016\x000f\x0008·D\x000eå\x0000ôëUv"ÛqDb\x0014d2\x0000õ>.ÃäE$¿êðBÐài[Sº(­"Eåí\x0004àqWtá-»ÛÌú[^£+lI#fBAçø\x0003ð©cCµ{«Å´æÑ#\x001bJ$ó>RGqÁçÿ\x0000FÔ4ØÄ×û#¾WF\x000c3\x001fcùSDÆán
N`Efx làuã=\x0007\x0002ª¹Þ\x0001\x0014HÑ+eT¶@÷ýM\x0008\x0006\x0017ÉäS²ÛI¡\x0011¤u\x0008Äð\x0000\x0019ÍM,\x0013ÚNÐ\ÄðÈ\x0000%$R\x0008\x0007§\x0015@DNáÇ¥5@\x001dÍ=ºg\x001cûS\x0005\x0000^Ò.ÿ\x0000³õK{¼ñ\x001båÇª\x000fèkÔnV[£0aäw¯#\x0018Ýþ5è~\x0008×cþÎû\x001dÓs\x0001Ú\x001býßáøUEÑ¤y\x0001ÜûÔ´Ô\x0019\x0012!\x0007½^á0ñe=Ç4¥"^p3Z\x0010=_pÈ¦»ê@¨MÔ*qæ\x000cúQæZIË0'Þ{Çñ
Ý/UaVU-_¨h6u\x0011­\x0017\x0011\x0002^\x00068 þUæ^+ÐæÓµ\x0013\x001d²fÚé[ãø}Túc?zºÆ8\x0000~\x0015ã\x0008\x0016o\x000fÌà|Ð²È\x0008ê9Áý\x000f52Ø¤ìyöb¶è¯y\x0000\x0019nB@\x0008ýjá\x0005r\x0002¤ç§ó¨­¾Øíìõc+V\x000bUë!ó\x001bÓøk\x001b6Ê2g(®c`£\x0018\x001eØ¢«è¡)"áþëçõ¥òF#3\x0004?+¡ÁÏ¸úW7o|!bvÂ\x0001À<)ö\x0015FëÆ")g\x0006Gh,BîõÇRzzV1jEXìn¦Ö#5Äâ1²\x0010\x0000ÿ\x0000>æ>$\x000b¬\\_Zî\x001bÈHê£cõÅ\x00177jNÓ9Qå er\x0018\x0012y\x0004ó»?çÔ%n,
ä|HªÊàp\x00187}zU»¥qòÏåÄÁN\õnõP\x0002¬AëëZº²Og>@\x001b$ädwôªóÄ¦øÎG¨ì}+Dô¹\x0004²\x0011<
Ã¸üVéòç\x0018Å:Ê\\x0013\x0003ôcòCK±Eæ\x001c=©l\x0005ëXcâ\x000f\x0018ÜÃ#×ëZ\x00025§o	vÎvÖq	ãgRÛ\x0008=:¶°	¤r¤\x0007\x0000\x0001\x0007\x001dÇåXM6\x0006+
¢#\x0018t\Ô\x0011JÍÔ,>Ò¦[xÈ;^<ð{\x000c\x001aÞâ3\x000b,ÀI#ð\x001dG_ð§Éq²Dw&=ªIÛ2*#Í\x00163;¼Ã
L#Ú\x0006Täô÷®ßÂ\x001e\x0019ïQK¸¨¹×;)úúWc©xvÖöÅl¡\x000b+pÙf\x0015
ô^09ïÍu6+\x001ecáÝ\x000bûVS<ÒyvÈáI\x0003%ÏR\x0007°\x001dMfÝC\x001d¾©s
!1Å+¦ß`ÇúW­Ûh\x0016úm¢Ãcp¤"à,\y9õ5Ç^ø\x001bX½¾º¹B$ÌøP	Éí¿g\x0019IÉ§·@±Æª£HÉ¸GqÀ«ú\x001ciçÏ#\x0013¢$\x001f|Q¬h:z »¶egå\r¬=CU½)\x0012Î	¡¹&E|Á\x000fÝôÁ­$ô\x001cQ¡1YZ0\x0017\x0008P×æ\x000bü°?\x001a©we=Æ^ÌÏ¹x \x001c öì\x0007õ¥Ã\x00046÷	 Lr®B±\ä6\x000fR;j¼Ò2Û
\x001b»>Ðc$ãóÁ\x0007Ú¢RåW5,ØÙM\x001aF.0Ì\x0010\x0006\x0001ü+\x0013ÄlÏ&Â=H\x001d3Z){\x0015¼\x001fÎÔá¶üª*äæÞò4\x0017vÖå\x0014|Là\x001föºÍNIÞA%súXídµL\x0008;\x0000õÇ'ßµT\x0011ã<ãúWE«¥Y6,â, "\x00101·=:V8´Ì BC¦\x0000ãÜVÑjæMXX,]®Q\x001c\x0011þ`î\x000e6úñÍi®£s¦Ç\x001aÚI"Rz¬LeÏ\x0004V6Êû\x0013sRêA
\x0015O§=N\x0007ÒOÕî­,ÌK!hÕÃ¤l2»±ß=±×±©zê\x0008«%ÝÁÎÎ<ÉÔ!GÍ|ÖÎihÑ,WÆ%i´W00&2z\x0002; ç¥WÓ^Ùôë¨ä6QJQö¢Ü\x0008\x0003;AìrN?
£¦ù7\x0012®\x001cÆ2Nå\x0019 \x0001È\x001eüÐõZ\x000cäµîQ­P®cT¼9ëÀ=;Õ­A<í.ÊùÍÓK!1O1p¿Täð3µu\x001aÛ¿¤ª¤G\x000c3Á\x001f­\x0019ÅÃi,²_\x0015Ü!Ôä7Ã=(°\x0019Ç8ÆF\x000fZi\x001cu©gòC'eÛ´\x0016ó1ÞØíMã\x0019\x0003 \x0010\x0012\x0007ÌF=jþv,u(åcû¹?w ÿ\x0000d÷ü\x000f5C8<1)Æ6)ÁaéL\x000fWÓäk\x001b\x0002\x0001ËHÅº:fªÜ^ÝÌÛ-ÐÍ!8ÉáWükR\x000bM<Á\x001fs¸D\x000bc\x001b@\x0018Ç~çÕ4«C±\x0014·û«¿#3\x0011tbãæä\x000cÿ\x0000
*x<3xòfâüÇ\x0018\x001fÁÔ×K\x0005Ô\x0013D²ÄÀ¡ô©C«c\x001cÓ²\x0003\x00014ýFÍ±æ¨BÜ0\x0015v9¦N¾VáëÅ&\x0017ØÐ\x0016 c Ã®)ÒÆFÑÈ»ãpU÷\x0006¥ÂûR2äw¦\x0007\x0001wnö7òZÈIØ~Vþòö5nÙA\x0003\x0015·®i/zÍ\x0008\x0006h¸ÇMÊ{~\x0007Î±àÊA\x001dsI eÀ\x001d¨§\x00058¢¨F\x000e§r¶¾S¼{ý}s,Lì$}®Ç!É$õíR\x0008íZV2\x0019º¶ã~äxíÃ±Ü²Î}rÇÜ:	mmÊI$³\x0015ÉÎÜ\x0012p@ãñþT\x0017Vv­¤\x0004T\x0003pêOqÅgÇu9¸m°³\x0010]\x0017\x0001³Õp³\x0017ó§%vìõ«Jú2e#¤M2û]f\x000b[\x0012\x0002¸ô_L÷8¦Í£A§\x0006K¬äò\x0004y#\x001fN­¢Y®m\x0013+¸E\x0005\x0006KdUÖ?0Ämà926qíÇ$Ôë²Ø\x0014nq\x0017\x0016,»NW¨#¸õ\x0014_væÁb0Mt3ÛZÎòA3\x001bVuá£%Aô%H®mV[yµÈ)"\x0002F2=jÄ5b}ÇºÓ\x001b\x001d3W\x0012Õ«\x0004Îv\x001ejà\x00126ÀõR¸þu.@\x001c[©\x0004\x001aé4¨-nU\"¼Nö=G§¥cÍ\x000cË\x000bÎ¶2/!\x0010:ò[Ô\x000fN+wÃ\x0016\x0013Z[4Ó8/páU{\x000fòhI=G\x0015©Ôxjö8¯$µa.ÕýT\x0013ü¹ü+ \x0001óóÇ¿\x001d\x0017\x0015ÅÛ9´ÕþÙpñ¢Dç`fÆA\x0018#=¸é]EÆ­\x0000´\x0013³ÚHó\x0014õ\x001eÿ\x0000Ê¬h¼ñî\x0001WÔU\x001b\x0012ß¿Eÿ\x0000r\x00101Ú¤ûSy¬±Dï!\x0003ä^{±§ØZÉ\x0000ÌAwbÍ_JÝÜFG"GðÓI3\x0005h¤GS·w$à}	ü«Ï ³y®$
éä	\x0003<çÐ{×qã«¶Ù\x00052Å\x0019Ïìøç²\x001fÒ¸¸.§tcQ$d$>é\x0004äoñÁªÐihW\x0000cyY#\x0011)\x001a}Ñõ8«v-í\x0016èíPÒ*W\x0019Á#>£4º¤i\x001c\x0001[ýJóß=?§Ü\\x000bÝ\x001cÛùçÄT¦\x0006ÒØ#\x001eÜT=ØÖÊÞódÏÕgr$\x001cÑ=Ò-Ó[ÛÚ"Æ\x0007;Ø±côÎ\x0007ÿ\x0000\UWÍ\x0004R9)#\x000c¶£ù\x000f¡¥¶1Euç1k1´m\x0001Tc¾N¥'k\x000eåË>Ú[[e\x0005°¬\x0014àç\x0019úV"YÜ­È¢t\x0019Ï\x0015«o)Y$w\x0001òr­Éük?P\x000c¹\x001fpsß?ýzTÛØÊ`¾àÍ¿\x0004ã¦1íM.\x0000B~NÇ[?Ê®Ú])­fdÏ*\x00101ëÍBöæÞý"h\x000bA\x0008NÒÀô­I$Õ|ðÊ
~ò1\x0000\x0010½º÷ª*È²`2¶@nOøU»»`³H«\x0000C\x001bçÊ\x000e\x000f\x0004ôã¯áP]Ï
Äí,\x0016©l§\x001clHÏ¨ÏJq\x0002]ÒM,B\x0016ùäÂ( \x0000=³Û\x0015\x001c°Mo;Eu\x0013$ªFCúãÞÒyabSÊ¶[\x001e§~TÖY\x001fs³1Æ\x0001cÎ(°ÉXá9Å\x0019%r\x000eG¦*<¶rH\x0003\x0018Á¥\x0018Î7qL	£8ù\x0000ûÒùY6`A\x0000¸4Ì\x0000¸#ó§Gò¹'\x001d8 \x000eò	¤ÕÎ±;çå\x0003,§¸5§¦øeùú!\x001fv>Àû×\x0017àË»_\x0013C\x001d¼Ç3þô\x0003P\x0002r}1þz×wu¬´·gO°Ä·#\x0001Çhóëþ\x0014ÒD²ì[Y\x00022¦qO¯µ9\x001aúq¢\x0010!þ9	ú/_Ï\x0014Û[Hlq5Ì¾eÇy_\x001eÊ:(ú~µeoîz¢EÄ\x001b¦>ùkù\x000e3S-¸ÿ\x0000\x0011®Oó©#rÃ$RÉ,q¦é\x0019T\x000eäâ\x00115\x0004|¡ú£úT
ow\x0011&\x000b¥q»2ìËäiÿ\x0000Ú\x0010?ú¥ox¢,?<bö©1ÿ\x0000\x001e7Xÿ\x0000t1\x0014W\x0016Ó,Z\x000flXádûñ¹öaßØOº·bnb ûØþãMúÊåÍä\x0013F²®1q	T`Ý3PAi>åbs%¿ðç\x000fCLOAÂ\x0003ÔU±\x00128ÜíSÐzQ@Ï\x001f·ól/\x001a7¸FX?{'\x001eÕ\x0015ÍçfLðÄp={Ô­¨§åcWð\x000eÞ:2ñY×\x0011Ï4»YCFNVEùõ?ýjçßsg.ÄÖÒ a"UÖLõ"¦76×W\x0001¥UXå ÊëÝëY«o$\x0004pîÆ}êÕÃæ~¤uÛFzûÐÒÝ\x0012µ:ÿ\x0000Ò{¹b}èÈ$RØ\x0008\x0018}ß¨ªy+Ý¡µ0\x0005U
¢IÄdg?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=@¥gyCãÌÝEHP\x0003e¼[\x0015+bI6\x0008®\x0019MÓÚPwµ"P (Ð)×ÒÅ­lWÌÁÕ(øðWÓam\x0004?z6±\x000b~e.3R)\x00073ÕÇ\x0006Jrô\x0010ÞLåÄVêÏ7ÖNnÕq\x0004M| 'ä°ó@9ü\x0001ÊÊ>ôc-aêQzÆqî·\x0008ê¥Ü\x0014Q\x0016\x0010Ð<ÓYø½Ä7f¡{ñÂ4ÀêÇÓµÎëO4Fé\x0001øú*e\x0012\x0005³C[­\x0011\x0018×BÀ\x0018 W¢ïey\5GiáK
·Êmxý]§z\x000chNgÛõSîÑ=o\x000f3\x0006ãØ,ñXë£&_?õ` þñMÕ/!äV ¬ij.>ÚxÁôÕ%\x001bÉj\x0016s@Ña¾\x0014T^7Y_UÎ\x0010Æx2Û>\x0019_Bû¬\x0007?úÌ\x0001ÓÜô¿\x000eàÍ¹ü|ó[¢\x0011ý\x001aùPÀ\x0015\x0011vàZA¢2Ï\x000fS#\x001f÷º)ù°9ôþÉoÈØ/ýS§v±\x001bÅ½ÁQ/3\x000f|C\x000b¼ãx\x000bBåÏT½"\x0008g/Úhh\x0013Íu¯M'üëDìOÈxÌ_\x001a\x000c±|ü\x00058×Hû»Å«þÒv¦m%\x001cááõê¶:4«¯NÃ:Þë%l\x0008^¬ #xà¢OURÇåªñ\x0017Méa´HQè¸7ús-þ8jè×ÃêH\x0019i°s&âêñP\x0003¢Æ]\x0000fã$Ñ¡\x0006Wðl\x000eÍ\x0017Và6	61&g\x0010-±Ò@\x001e¸¼,;\x0010N{6X0Ye\x001fÍ\x0011¬\x001bÛ ³"zÃa«\x0015µµ¶Æ\x0013Ak)æÔæ\x001bó\©%ÕoDçs(eãC-Ë15ën¸l¬\x000cb\x001a0ß:\x0017yf¾h£¾'\x0004¶,X1¤Áå£²Ï¼pf7¯ïÆ\x0013Û<ä¢øÍK ¶`Ö\x0000"´S7¯y°\x0010GxSOÁ¦×\x001bWÚ¤ú\x0002<V{ÒòÚ\x001f`ÍouÚåÄê NS\x0012FÔ$Ga²Gxï\x001f§¼[HÂóRUÂqþòû\x0016íxhÑ²\x0000äñl\x000c\x0016½êÐÓ \\x001c¾Ø\HQww7­åÅ¿ü\x0002,\x0018\x001e@ÐC\x001bj%\x0011NÉ\x0004î\x0017À\x0002ïßØiâtõ`ÅéH+.47¾_Ævâï8´IV}½MÐÆÀ?"/î-¥Â\x0013¸¹¢)íöþ<¦</p><p>îÑ\x001dâo</p><p>\x001eÉïÔÍ*iR\x0002ÝAT¹\x0008Ý­ñxü·ÿ0t<uÃ]\x0007h M\x0014N|ÉúBtI¥;\CD
\x0005E¿\x0000h¶1\x000eFjê)]²w{Üê\x0000¨°i·s\x0015Eö8êq\x0006üu/²\x0001)1úß9û\x0018\x001dû¡/}<åEÚ÷OI iáN^C\x0003éýHÚ<\x0004¿c¦fø4\x0005÷§úù
|ÃAõ-£"ãæ\x001f¬\x001cL¦»\x0013Ãþ@å+isªc\x00102ßÕ\x0019È=¿ïõ§\x0018\x0019;æ\x000fc<GÝ2âÙ¥q9\x0017Ê³Üë36õ6ÔTß?Ø¯ÿ¹hç³ù8pj´F=[³RIxcå¢\x0015aOñ\x000fi¡ÛbN1ÎIÔ·Î\x00028MQ\x001c¾_+oÉòð×{Ñþ}\x0001øXóøræ\x0006\x0015Ö¸c=\x0018\x0008 ÛÎÌÃ\x001f:§\x0003|Èv5=±[{\x0004l¬l(1å¸ÕrÝ«ø\x001e\x0002\x001a¥26Án»¯"ó\x0008\x0003¨\x001b|ÄA¯çU¹/Ó\x0017Z3\x0016=X</p><p>oÌDÚ\x0010'¼W\pÀ\x0013E\x0014QçXa»h-ºór\x0012­¿Þ$C\x00167Fïé6\x0002ü|5#ëªôN=oEY7;\x0005ÛÈWò7;@{sZ|[Uµ\x001d=]/¹\x001c.6ö½·-÷5\x0007/ø!\x0019q¯ûí¯®\x000cß
½\x001fªÃ\x001dj÷\x000eW¬G¼¼äÆ&`³84-µ*Ñ\x000fPéÖ\x000c6=¤Ø°t\x0012º3ß­¡é\x00193°Ïc£\x0006­þ\x0011Ú£2ÍôÐÝÅ¬\x0018\x001fD´!á`ZC GòúßGzíÑÄý%µ\x000cjMÏQ\x0011C-\Î+qt?\x001fÕD\x001c\x0017¤\x001b8ÌÐ`ÈÊE[¾­Ls¿pMÿ±\x0005.Û8Ñt»\p_RoÍ9²øÄ\x0016Ú</p><p>{]æÜÛvjZYW¢³°Ô1³¯4K¸\x000eæ×(éîú\x0006¿ÎÕ\x0004Ù¸è
*úGøt­é¾X¤\x001dy¹\x000f79¶Cwà·¨ûFò/j¼Ã¡´­\x0008\x001cÛ\x0011Åú=¿ÆwYcÇ.sÙ(B\x00004¢n±¹*BÔôªåûp³?|ø¦íë3\x0001B½\x001cUêxSsø8Öº¯ÿò!6KCKË%Õ»\x0001+~¤a­à×¹ô÷\x0008Lå¬õ4Úéd¥ñ\x000ctæ«¿.1'(\x001c9UÑ¦ð{!g</p><p>3äºþÇ\x0018ãïÓºkg\WÂ=D¯*W< \x0006ù±¾ÛYÂã§\x0014¹tâói\x000c\x0017%×?Õ\x00141C5ú¸\x0014ZPå»:µëc°ÅlzT\x0003èÎPÈù|_×êyåö\x0004ÁÖd¦p&Â\x0014X=¡Çá\x0015C\x0012}"',]\x0005B}ÞlÞ<Wq²G¸õò}ý÷FUWéáóºÝ·®<\x000fLöÒx\x001cô¨M0tòFþâÞÉ_ñ£½3\x0019ô\x0003vY\x0002yìNb®ä\x0015Ðpv¡\®4Ô\x0016\©õ1õ¹ºó\öZ=oì	gûUYº&þ\x0001%Ùî\x0003Ø¡ åhîØt\x000cj`ômpB\x0015íÐ0¾\x0019q§[Í$£~\x0012Ï&'ù¯¢´Ó2N$\x0010¹øºÀv{¨õÆÜ°z(«Ïc\x0002Ùo?û±v·«U/V'ÅÛèª8ì?f«û°ýæÝí¼ñ*ÚK¤¥ñ>\x0014)\x0008á4a«¹ó[q¥wàö3=\x0003±\x001còÙºöëíìÛ©í^ÿòóÑ"²¬5Ú\x000cY¬Â×¬\x00192ý\ß 7&KW»»eÍY]è\x0006á¹³\x0003µ_·z¦Á\x0014ÑÜáaÊ`^­Mµ¸[§õÎWÝòlSÍMTx\x000b'd¡f\Gr[wJ£+\x001ae7B\x001d\x0006èë)üáû@mýW\ÝM6\x0013ß\x001cØ{ÇyüªÞ_\x001e2-#4ü,dÿ®6Þ	5ÔqZ|çØ\x001f|ªüïÜ}]§)Cæ)qX1(ÝÍÔ@bÝÝ#Ý=J)[jô<u\x001ap\x001c¢£T9úËÀ(dyW(¼ùø\x000cºF¶9ºr\x0016	!5ÞÉ\x0013Ô\x000e°É>Ìe:jÉ\x0015£uÿ¨ùG¯\x0019\x0002m!Ç.\x001077Ãßy\x0014\x0013_û\x0006yä\x0008 cºûhm\x0018å¿ä"½¾\x001bØ\x000b¬ç­;aàWàûØÉ#:/¸©F¨ÔÉ²Á<6Ã6þéïQI¤Úv§³>I$
\x001dÎK\x0016áIÜ¡¢öF:Î³\x0017/Î.AÅ~lö\x0006\x0011\x00126\x001bgÚà/\x0001¿È\x000c|Ó±î.ìóI\x0019ì%\x0019\x0005Ù>×êú 'û\Óíªù\x0008¥\x0019è\x0018èÛT»ùÙ$A\x001c}Ïf#>°*¸©9ôjw_Ý®­Ùd&GkC\x001aÊï.7à´¾é<¬wå¿\x001fö¨ÛõKæÄ/áöb©LÆÆ°4yv\x0015y$2|\x001c3XÝ²¹¥Þ<Jò¾ÂO2Ôä¡É%&K{#L;h#(vl\ÓÞÁgøaÌÚG\x0001~à,.·#_äo¥å1åy?åøëD\x0013¥¹?êÉEDÅè2èÁË;>W\x001a¹tcs¯wx%\x0011þ>)3=Ûç\x001bwÇóX©x-Âd\x001d¢À\x0007\x0015:IK\x0001wèg;ÌoÛB¯­Ò\x0017¹DÙßü®wgÐËz°¢º4\x0006¦Hj\x0004I÷@®Á_î¯µã\x0004_\x001c\x001f¬¬v\\x001cs¶UÓÆpÕ<\x001fAè¢e\x001bØR¾\x0000"V¬\x0013|a¡~M2Ñ$ós\x0003?VSH¿ãµê\x001aûÉÑä(\x000bz_Tn[e¥Ôæû\x001dhþL¤©H</p><p>\x001eü\x001b>¬¤JÕÇú=Íô~r%_Ö^\x0000\\x000cNÈ[¶zv\x0010A«wÔ\x001e\x001a©n8TäCÄ^l°­ù\x00029Ö¤\å;\x0017\x001e.!G"<~>w\x0017²K@Í&qÎØ´©­Ú¢pîO\x0011öu¯PU^ØÍsNIIÍQ²o7^\x001b\x000bT»<\x0003]Vü\x001eêøü5||\A¦\x000eèf¢ñQóÍ»ù?çòdÔRR6Ö9{¾kGú!PY)¥Ïíq­\x0018dº\x000b)\x001f'7{º¿Áv$ï« ¢1².|\x0001~Ö\x0018p\x000fùëýV\x0008è\x0002þ+\x0012ÝëÔC1=\x0019&ýHï=\x0003\x0003ç*ÒW7NËc±éæzÅ^.Ë57Í\x0017[ÜwøÈ\x0012'¿W#ÜÀ\x000f®\x000cgóÑÔþÏæÑ	\x001f8\x001cäaz7L¤k=ª#óêK6Wtó1\x0012mQÎ_M®DÂûëñUKüÙ¬!Â§3å7\x000fwk\x0013¶ÑGUOnõPÛÜë\x001dã¼\x0017E_Ô×aÅ</p><p>¨ï\x000cM²ü\«÷&e-\x0011\x0019»=E</p><p>\x0001\x0003Fý\x000b ºÔC{¶DGY«ÒóSPoZá÷Q*ãô©ó°ù\x0012'¸3A?Í®¡@÷¡\x000ej\x0018\x0004¶qÎ\x001016Kª@ve\x0011\x0014\x000c8cb6â\x001f^ËÏþK?h_É|Ècª£\x0015\x0017ø­³»j¤H\x0012_3ùH·Ikv9KglÓ	ÝË¯ÚàRÐû	*©Ö4~Q\x0019x?uv¹@@ý£Ò\x0006¨¨ä¹ïÑCÍÉoÄ\x0006a8T²>Ê\x0012VU *\x0019K»äÄ¢L¥ì</p><p>eV°TÛ°\x000fõ\x0005XÔ\x001fÉ«i_tÜÏ9n³Ñ\x001e9\x000fkvï\x0005y.ü-ûa3.³^8CJ5U¶þ50ö\x0014qÌïÝý¢%´Ì×^\x0018s"ÁW?I6©%µçðÌ\x001e8\x0019ÉÉ<ÊèMv¼Õ\x0011©×5ü»î\x001a=¨ÚmZP</p><p>d¢MË7ç2xâÕéÑ¨Ø\x000cË)a­f[ÑG*X9QQã&M
G°\x0013\x0013:mls\x0014<]\x0005\x0014VFû§ùÇ¼Tý~!ÔwÙµûw6K¸z|\x0016'~÷&{\x000fT¢¸~ÁÐ</p><p>BsC.\x0017:?Ð­tôS£\x0003¥\x0003¸\x0012m¾ÕvA\x0019ìã¶N)óCÞÀx\x001aØwg>í;\x0011\x0006OI³@µ\Ì©¸\x001dÒ\x0018\x0007c]3Ó¯?REµC6ùTÚuµ05gEÌ&éHlûE`ö\x00191Ö­ÎÇ\x0018NÓ]\x0011K|¦\x0014~D9õXü\x001a³§l.[ÁÍÓ©þçà\x0012íÁØþ1H­ÐI\x0016Ñô)|î§:^ì\x001bkÍÎfÉø|{-Íy¦g{Gr\x0004O\x001eh\x0013ø\x001aR|ÑãÜ@Ö{O¹\x000cv©~rÀîc¹êaÙðWeùP·1°ì¬O]Ë!\x0004=®Z×ýC­\x0018Cu¬ê</p><p>Ü³=ïëÒSAµÏí\x000e¦Þ\ó"5­\x0013ÑþFGK[W\x001b«\x001c¾ûÓYùÊSM\x0010¶8ðKXo¦q2'[[A Ï¥.î2\x001dÏ¸Ðò#I\x0010áÔ\x0002§9®\x0016\x0017z\x0006.,÷\x001bòNêCu%ôÞ\x0007òaé6"}"\x0018*êëöÀûVi¡Y¢7C@2\x0002{%\x000bæ\x0005KÊ>,¾;¦:/÷Æq\x0007y«@y\x0005\x0015I°ó\x0001OþÉY¶\oÿ\x001b¦¡ÞÖæ\x0014ú'O"xª^VwìnlFÐ{/æ\`((k5´X¶t4Ê%C7tÊÄ*¼\x0013müÅ3ÿxA=ÚÙL+º»Õ>}«\x0004c½ÜÙE}
f¡8ÒÒÆá0zæZ\x0012âÙ(h¤Ô"cQà·è¤}O§£ÚB`\x000fO
Põ|\x0014º#ûp»%ÀË¡ÿ\x0018n¶@É·}\x0019d_t\x001dQÄ³AX.Ô\x0012áp4Ól(çr$Ë"2\x0008YÜFÖ«[W¡/Ý0LiXð}r ùìæe×\x0004É\x001bVåëÀ'ÍÚS¬\x0015q"r</p><p>uÉ\x0017à\x0014c,n\x0004Ç\x0018pèìÀn¦ÛÛÚ!}¹µ$\x0017ëCtäRLü@Ó¦ß\x001bo+Ò0\x001c\D6\x001c2¿3å]§Þ¤¬§ÿ+ßÂ\x001cCP¦½\x001aÒ\x0015\x0017.ÔRRJ\x0002ÛÆÞ#åGÖ¬­?ÈÙ37ÒÐwõ\x000f:Ë*õwgÞ¨ª´gèd~ 'ÂÂ!8÷>Ôoÿ¾&vÓf®8fHÙ2\x0002¹ý8u/ÁAÌ@a\x0008³ö-rL'ÜÖËO\x0008ÖåsöÀ«2~Î\x0017þ!ÙËzÞ\x0000÷§Õ³^k¨v[Á¡Äps&¥É\{Çc5Uc\x0002]a\x0015</p><p>ÆîíÌ\x0017@·ÈÀi"^wT`\x0017¾?\x0014¼Ôéó;ÿPÆsÒyà²9ÔOÃÿV°2î\x0005H¨\x0005lø/ôîÖ¿±\x0012þDìñÃ®|>H¤6Pµ+gãùÃMS½Ôú\x0001Æô¥óMHm-\x0003)"\x000fÙ­N\x0010þúß¢@X¤ù\x0015HÌJ{ok~ÔU=¤`R«@µGziÙqsJ\x001dKÓcïùizË\x001dHàÝ/üa{Ï\x0014ÔbóÚ-®¤&>HÆ@\x0006L)·ëj]8xc±¼\x0003EBÅYµ?UpN88º×¸é¥QA]Ðäõïv­fx±léÜXÙ</p><p>È«#úâ\x0000GØý\x0000\x00063i9ÏL¦.\x0002øs</p><p>üY\x0002ôN¹]½Ì\x0005!r,©v¨(!0Nòîáº)VÛxn\x001cYÑ¥l¸zíXü\x0005M\x001bãd®åõ8OaÝ\x0003MX\x0012\x0013ªvíÞy±»ûæ\x000e\x0012©ÃùÚþ:\x0013ë4ÉÕÔkFsW»ôÅÇï\x000cFì:² ¢\x001f1X°ôïwZË¥\x001eÍ¿p\x0002\x0008ÂvÛHIn_\x0015VH5VÔß\x0015}\x0014\x0003àwÞÊÓÙ¦\x0008 êýH#Û{ñ¤`.Ó(}(ßü]-áÚNF}x?¯ë\x001aNe\x001cjÎn.<¬µ«.ùÓÞßÍhò{e\²Tû5@¸{?\x001f6Í%n¿ÝÝ3=É\x001cxSy\x0010@Hâè \x001es[°¾ø-C\x0014ZËeÖZZX;êM(oj$*úMITþ«}YÒ]VøaÇóÇ ±²ßñMIåT®ÀP3n\x00111÷=Ö­ÛÏt(¯°\x0000ô£-J
Pµ\x001e\k</p><p>\x0006ÏÍ¸\x0010«Æ(\x0012d¨\x0006K8y\x0019\x0012J¦dê¶wÁô\x0005´O;ûò|ØÑX/übßs¯VµÑÝóþ¥\x0012 ¬èD\x001bÂ\x0008\x0010ÿØx\x0014pfa£¬\x001e!3e×ô`R½7úi A)Å\x0008Eg{­¶LðIñ\x00058{\x001eUÖ´WÂP;ã\x0001}»òõu)#\x0000\x0019\x001eýúY³.\x0017"®¿Ç`W°9ùó\x0000ÆÞÙ\x0019M\x000câ]Âló,R©X&«2õ?é\L2es\x001dÜ1+\x0011ÃÐ+ÿ´Æþ¡àæ\ÈNK­¸$0¾\x001c«	.ü'§Ñ½\x0008rt¨]\x0019ãlb(É\x0011\x0019Ïç¹Þªö2</p><p>]-iª§ÔY19;T29³K òï"H\x000bF  àÝ\x0013\x0006|Öcî|\x0001¦\x0013\x001d\x0017|T&æ\x001a9»Y\x0005ÿ.:Ü{	-£ë·Ml¸ý[þÝÓ×Ò¤z\x0000\x001c	·°¶{bOÑö&·­\x001bÛ@Kù-]\x001cÌ/îêø¦6ûê\x000b`\x0011ÄG§7íìßÒ"½_>×\¸ÞËªÜ´qbæìÊ:ÏSD-\x0004X¥w¶u0RnÎþñ^nMEZ0^6WWËm0]Î\x0006ÕÜ?ì´P.\x0003¯ÃÒ\x0015Æ JâZE¶]}>\x0008,\x0006ñ
ªfÛU|\x0001üu\x000cnn°r\x0013tAµ+SOñË\x001b\\x0004QE$Â¨áázZ«´TPIRdÉuô5êe\x001da\x001b\x000f?Ý\x000f|Bî\x001bÐ\x000f9{\x000bLdì\J
«Æ\x000bY\x000f½\x0005\x0019´\x0006|;Ï0@=\x0011WfÐQò±W\x0001\x0012î®«ë\x001b\x001cÚ)âXbÙ§\x0003Ì\x001aî6\x0008w¹\x0016)tÂÆ\x0014ÈÅ®¾X\x000b~\x0018çòssg¢L¹6¤§¿Ç\x0007k¥îk×üô</p><p>\x001eo$\x001bFÐ\x001aëÜ?èâ\x001a~eÐÉA¦0d8ì¿\x0015Wcl </p><p>ëoîýuüíÒ\x0000\x0017éÁ\x001d^î/;^À(ÿ\x000bõO©ýòÒ\x0017\x0008\x0017s`¹é]6£Úèó]\x00196Æ{dÄãbk[\÷É&°5Çé\x001bò~1ìÁGÀÇ°ëß^\x0006¶x×Ê|o1`ZJåè6Û\x001bßCÇ\x0013TdÞãûø}dÓ\x0015bPFÒT(Á\x000eZ&\x0011£Â^$ìWt¤GÔíÚ?\x0012¼àÆ%õ:HG</p><p>:év%íG><¹Ä7"|º÷Ù[øyã+qo}bJö'È?D?[í*
Kú-u¸+\x00181Ëñ\x00106¾\x0017'Êï|Ø\x0015[kJÇï¢v¼\x0018\x0011Gp³\x0010'\x0006Mç\x001d
[ÿý¨¾ø\x0019\x00076¯9óÌß½</p><p>¨ªóª"à ,Ë	ü+nBÙ=o::ßÆó­Âö\x0015ù^\x0006g±§Ùu²´?õ\x0012\x000e2y\x0004\x001fUæùýd©ùM©hÁÞ:dï¸ç{\T`^d×¢4\x001e|Íé¯\x001füÚ.Iÿ	Ñx»«rË;\x0002¼\x0016¤ù)`?GQv9¤\x0006¢i!§Ì«±õ|ö)kCÛl''ÓÝß	l\x0002í#\\x0007Ææ	Yû¹Ï¿ITïö\x00108Þb±< â»,ÑíÂÓ;ô]F÷·ª¬q\x0019ÊZòÆõ66ð'ÐÀª¬À Â</p><p>3ÓÝ?5È)\x0016H¥*é8¹·\x001bZË»`QÕ\x000cßNKúÝ\x0005\x0002\x0018j\x0016Ý2Q³Ð¯÷ãê\x0018D%:¶Ý=á3RÅ,\x00113#îq9\x000b².X\x0015Ø[B\x0019R\x0006/$wK\x000c£h\x000e\x0005\x0013®º	ÜÍÚ5fú\x001b=\x0007ËÈ®s\x001dÞg\x0001=Õ%³µ×ä­¸×õöµ»÷ÈwÎ-È¯F«µ\x0018¦ó4üê\x0004HÒÕ¤ð3 9êI\x0016	çFþ§÷1\x000c2n}bOá<³ë\x0011-±x»¬$æ!ÔÚAÿ<\x0005è°(ñÈEµ\x001f¶nã\x0007e¸¼\x000f4jGÕò_½Õ¡FÃ
Fò$6ßïKUÊq«Ý\x0016¦Í¡éq\x000e]øà\x001eÍ[YºyÖ8Ð\x0005ëÉ`òkÌ\x001cû¨L\x001f½ Õ¿¬î:Ô(z7úWâ°\x000f:zz\x0016ÿß9X"\x0012®Å#v¡_$ñf(¢ä1\x001e*[H§í\x0000L»	\x001bëEë
,]"cpPµZK¦ÍùÆê/lIë¾ööwé</p><p>ÝóTåª-Âû!îòØ£¨\x001f§}ÃT\x0008Ø©Æ5½ÚL\x0017iæ¯4¥#\x0011£Z?ÐT\x001ej¾£;¶§\x001cíyïëixÁwIºÅ¯ÔLq=\x001d(<¥`\x001bó\x0007H8¬</p><p>ÿôà-sMn\x0002×ÿv\x001faýß>y9§i)5l´ñ¹
ñt\x0014#7ÔZ'	Û\x0012k\B1Ç\x001f¢Þ\x0016Æl=|f $cA~\x0002Ï\x0003§ÝõÃ®/Ñ\x0018ÂUÍ\x000ceâ\x001f2íVÆ¸\x001cf\x0011âÒ¼¸j}\x0003=§È8Yòü?%ÎD7Ü<¦úù\x0016×NÿhçÍ\x000fnRpù·¦â\x0011ös\x001bº\x001b(Õ­láè[\x0007.a/KRÑëz+T¸W\x0016)\x0007töµ\\x0000X©eÎ´.âæ:Ë\x001c¤	Ñâíì«oÇ\x0007^ßAFK×Ô7É	¼àÔcò~µ×\T?3á\x0008¹k`×ÍdÑù§=tÃô,¯'xy­¾EÁ2@Ì:ò/4zPU4\x001fÝã³Ð£Pd­ljÆ3Y9R\x000f®öo+
^ RwU°CÍZËÑ/S<÷YúZ}1ýg2áMYµ\x000f¼Ã®Ü(x\x000b\x0011äû\x00114Zfw£ÇñÌ>ÐÀ4ÁÐU¸æ</p><p>NÈ»Ý\x0006Y®É\x001e3·R¹eTâçøé¿¬8\x0007
Ä#n(ìÁ\x0003­o\x0008r\x000eßQ\x0008m}~E(\x00052ÔÎ7¯K?ø´'¤Ã\x0013ç$ÖÇù|\x0003\x0003\x0018\x0018Z\x000b&èkÔÒS¾\x0003
:Û â'{\x0015\x0019Äæö{:ÞæÑzsÚºjY$è[\JÆ¾Çpò2`ËK\x000bo\x0016'ÞðøZº\x0003\x000eéEH\Ùu@ÔØY=OH\x0004
Í¬÷"å¯jz?æg	\x001c8Þ´­TÒ¼\x000báÝr÷Ke\x0011Ä;\x0001¶*ä}#pBÛû¡õKQUºS>SX0)òM£ØS¼p¹\x0018¨Ôöµ[\x0017üË:\x001c*zÍªñ£ç¡ü\x001f¿\x001b\x001f>¨A-ß9GÍã0ã?ög]\x001eª;ª*=*uÏ\x0006¥;\x0012/ñ\x001aÞbÝØ+4ÁÐ\x000c·à\x0016eÜT\x0019;g¼É¸C^h³PÁuª#ô®¢Ä	Q \x0013\x0006?ÇÆuh<\x0017+\x001bDtéòzÄV³Ë¶úãçn¸®vÖ\x001eÒ\x001b=¹á8[áÆ·ý\x0004Ðÿ-¨ë\x000b/í³g«=§î#ööPÄÆ\tß°\x0000\x0014»|ÚÎùÐ~XYÖÔ R\x000bÉræ8-~\x0019{\x000f\x0004Js\x0003S
Öv¬w\x0014r\x001b->s\x0013¦ãæÀà¦õ¤\x000b¸jØ1NËAÕæ\x0005</p><p>Ì5yb/ü_+1-GW\x000c \x000bvÚ.\x0019\x001fòNõCu}0¿qnÕZ5;§ÿóæÄ6ÀwÎ\x0006rk
rnå\x000c±w®B\\x0007®\x000e%"oÊÌÒèF@EÛJ©@@^úÉAµ&!\x0003EhèúM¢D/#Uû¢}\x00102ðU1zò^·ý; ÔÛõO¯¬GÍ­¾~\x000bhT$gY\x0000ýOdJ\x0000)]íÐ9E$KI°6©\x000fTù¾¡?v)´¹(\x0011¹Ì!=/ùN\x0018XvbÑ¡yhÞ\x0002Oe&sey¸\x0007oöÕìE£ÑW¢cd?ÂbÄí\x0001\x000c¼«9Ïc6oN&Õ9f\x0013Úç¡·Ù?T¿+Î\x001e¿\x00155Ëj	µf*J¿B0Ý\x001fÿ!v6</p><p>æ±GEuåß\x0017Xúh\òJµ<Úò¾3'ÕÚÒ÷4áù*c*Ë0þ«§8u\x0017Æ5çM+-\x0010*¥¦rÆüÄõ§9\x001eB"¹O\Òè\x001a·\x000f%Ö2k1ñÖ%o(á}/kØ0·áÖEðp­"Q.U\x0003op0|\x0010Ç-6ô8?#T°\x001bGÔ=á®³s¯#Ê/ÔÆYZ5\x0008­yÓ\x000fÏzýËÞ\x000eÒ÷ý5¦bä<§\x0002cmE\x0002²¥tHE_RÔ2éþ.\x0015LÒðX\x0003ïÇ\x0019ËUú¶È#}¨ÌÏw\x001bçþºxé:¾4/\x0015_Gjî1$:'iz&È¿Ä[1>«Ë7Å£ÊRüa\x0005<R9Oø³ã«Y·¹ÂÍå$ A\x0008Ã@(CÜÛµNn\x0004Oîëë·¤qbsh}I.\x0019¹ÇU;	\x001cáU\x0011\x0014¤cüÝ\x0010=ÉÝU{éE@±ú/º\x000f\x0008x¾¾¢\x001f?»]û5ÔZç\x0000ÀHgÅÞ	\x000b\x0015Á¿É·{\x0017Gàô»f ?ÈwF3»«J
 \x0011­+7¨\x0010ð²±qG2~\x000b¿ý$Gè§ª\x001d*ìåè~Zlßå\x001eó\x0005þ3¡Õ^6ÔçD!ö\x0015Ìd¶<Êj>3òAQºöËC^¯\x0006i®Ô5\x001aÜþ\x0003Ä\x000f\x001a<\x001fhÄ.Ã25v÷¶|ÃE"J[Ù¼¨l%è.	éÈO^d¶z JìJW3yzgi\x0012\x0016)e;Ê¹KJ3\x0006YdyÙvC6´òRf\x001f{\¶¢
í+òNW»ÂöÎ4oÅ3\x00046HÀO%^U)²éßvzÔíâõ\x0001ÌT\x0013»#n§K\x0005 \x0019+ÜÐVO,qÊkeÏÔ®\x0004·÷J¦+\x0004E¨Vù×¥!;×¤Ç"ï÷8,Ê\\x0007ª\x001däç²_Æý\x0013®p ÷zÝX'\x0014a¦Å.\x0005Z-\x000cPIø\x0007AÛr«J:µ³D¯ªØ1`<Íx\x0006B_RHè¶Zí\x0017`\x0008ä£5§ò÷Nc3³/éÄÊUkrpÏpKLÖ·ôÏOo</p><p>òç2pßÁÜØ³Ûû:!êfÄM\x0003ÏI|¶\E£ì÷³\x001eq-·ñ^IàTØVik\x001c\x0001Àb<¿PK	á¯}ñ\x0017 ÑÏççÛ£Ù?÷¢¦Ú¿5¬«'$\x0017Æ`7çÙÎ|\x0004ÕÜý£G\x0014eU)äPmð\x0014Q(êáãþ#(vÓJéO\x0002\x000fî\x0004zù¦¦)¶_ÈB `F\x0015±½ýåÈÕÈ´Ûy~ÇïS\x0000lÖ\x0007\x001a?¿ýøcïÕ~ÍÞásqõYH£Ó«¦r\x0001|¨\x0005éç»t^OÅöÜ®5\x0008ú¯Îô*«À\x0001ü\x001f¿¬9LüX¦¯g\x0003è©zæaï|báÉS;>£\x0016Þ\x001a´þònÚZGj)ÁWE\x0018tÛjâZ%Ûã©-JÙÚ¼ÜÃ\x0004\x001f\x0011\x0000ã\x000eòÃ²Ç¹»xítRÎH\%ô"Ðeâ¾g\x0010¤×\x000bú\x001eg«'[èÉý\x0017f!Ïg}$û°m\x0003·Mþb¹(\x000c5²Ù/wRÉ]2X|lËôoútÓâ¼yT%{*WÏîÔ¾IÕÕúh!ÞvÄç¨l.å©6J	ÿHp©¯¿@H[Òh­ÒÀ\x0016¶\i&ÃHØíÄÆ?9*ú2jÄ,Ä\x000fÃËôxz©W\x0000þÅ\x001aÌæö\x000f1M\x0016\x0018\x0015mÜI\x000cm#]4ä ßÉvGÝ!ÈYòR\x0016%¦.EL5h°G7Å´¡Â\x0017h÷ø¹Ë2È\x001a\x0007õK >¹á}ôT£xÑû\x000b \x0018löQ6s_aÙÓª\x0017?\x0016hNCt³ã6\x001bÄxûP4¦Íhî\x001d¥`WôQl=YêÂb1\x0008ÉÇJº¶c\x0001
L×·c\x001b¤\x001ftrq@úÙ=bÄ&¡ÖE\x0000¦z:éµ(?Í\x000eö«ÞTø¾°¹*={ûNÁ\x0012Ä®_[ÀQÛðmnÏw(©«8A\x0014:Ì@¢.æè®uÑ*\x000e=q\x000fªnAíÊ=\x001e[Eúâ</p><p>\x0001ê\x0012Êöñ ×\x001d\x0004=ûÎI½ô:æ¬tGùSR«ÑT&¡¡êj»v\x000chö
I\x0002÷\x001fYõ'ù¼Ó\x0003­i\x000c»qM9MÆ¤ÞäL\x0007Õq¢íÍ\x001a\x0000ÊÜ\x0013qÜµ¦¡ò\x0011,O´Â@p²é?'\x0003Qìu\x000fè\x0017À,\x0016æ6~ä\([h^ckh:\x000cJÒp	\x0015F¤O\x001fÚS\x001csà\x001bÃÜa \x001cÀÃ?as\x000bÏ¦}:©³ö¼N¹DVÄ\x0018\x000fØáûPP~Ó\x0018£¥1í</p><p>\x001eáû°½¬qÑ\x0015°!\x001a­ÿ£ç</p><p>çTàecoê­#\x001cÃxK¤(ÔÖ)t\x0010\x001bÜ;\x0018\x0003ªÕÝ4°ÑB°!> {<.ó³l|È9í\x000eÏ\x0013ÕIù±^ oöGA\x0013)\x001a¥I`\\x0012
±ûxûuA¬Ñ.C/aª«pI¯,\x0004S.RV\x0013P\x0013&,äkV\x0004®µ}H¬\x0012µ\x001c8U	EÆMd:Bö w\x0007ù\x0014gï±âî¨$\x0010µ\x0004;zë$÷ñ\x0012\x0010kæ3è\x001f0µÐ` 0­mä¤÷ËCôH_\x000fÛëÙÜoKLMfü`Â\x0016å\x0006ÿ5¢	m\x000eV¬JV</p><p>TÁw7ÊF\x0011­%ÀÁEðÍé(f¶¥ï	Ô æÆ=\x0010LÑê2OZ&®¬ìôÌ\x000e¸\x0002EóÝ´§O[Y9´Ø\x0011,&mÇ ]</p><p>º\x001eÀ8*ª\x0004»	?L\x000fuÞ¸´ôô¸ébÉÏK\x001dQÍ÷\x000b </p><p>,¤Yh</p><p><\x001cU="áÕ·wý-éêMtí¦\x0015èY\x0011z\x0004\x000b}\x0001@fé5KÏ÷æ5E)ÂQëï:pp!Ûë=öF§ËËÎ²f)æ¿\£(GµìÍ¡"ûmn¹ÇWÇtÞÉÍ{Ñ?Æ\x0010ÑéÈØî\x0013Ð\x0014óªtED½ÌØ\x000eíË°#\x000enÛ\x0004ÂÎc¶n\x0016;\x001cP%-awu~\x0001×÷Ï\x001c'\x0004¶}föÉ89GR¾iÈÅ5ÌTO»h©©{gë\x0011èi\Âð½OÏe
dòö¢T\x0012|\x001bÂ\x0002aÌR¤îû«èË4RÆ©Ð¥C\x0002ÿí$°Á(\x001dK¸Ù´\x0012eqÇ]õiNqaN{¥>à\x001dpão\x0016\x000c¤\x0018ëö¸7¶E®\x001d
ÉßS\x000f¢\x0013ô\x0001ys}\x0002ÜA¿HåQõè=!Ú=\x0005ü|µT;\x001d*ÃÙe¾áH#ãß¾hru\x0017$\x0019</p><p>\x0018\x0001\x001d\x0004Â{¶\x001dÚ\x0014¯yv\x0019<Ç©Æ\x0006s4"ü\x0010ZæM-)xqºë¡gZÎÑ\x0008øÓ.ÚÙ¾2ü/®\x0006sÁDë\x0012Ö`ÌÆÐ&ý$\x0004×Ou\x0016[0\x001fÖ0¿\x0004í`Ñhé¼ãÚ¸\x000eµÌ{h\x001aØM÷\x000fPz[EzqîE//ówÿ¡Ü\x001cÚm©9\x001edZIGW\x0012ßÎÉ/~%+8Q\x0017r~h;Í:A5Å\x0018#ÇïHz0Ï\x0004Uý\x001ex¨ë²=æÀ+³`\x0001t\x0019ï#sùÄ~Lm©e3àü3âh\x0006G\x001bèñ4Í\x0008Î\x000eÈÏ\x0011èe[ßÝlÀ!}¡lknÂt\x0012Øá¹[A\x0010\x000eûÄ)=ô/÷\x0018ú|èø\x0002/Uç>Þ</p><p>46«äy9ÁdD6(\x0010ÿv\x0003Ö\x001f*\x0019\x0017¿©ü<ªôÖ7´7\x0004Ûõ\x0000\x0004"\x0007àssUËýÉÕ8Ln®8ó\x001dÏýÞÝs­nár0&Þ7_Ô:aÂ²</p><p>\x0006Ú÷Ç44nÜ²?ÇÜ«Ð("\x0019Z\x0015Øú©1\x0003"WXû[Ãó\¸z-o	Z\x0005¯ÓÛíj\x0013\x0004Ü:xö¿«Hòoê½éée=oè3$\x0001¬\x0015\x0005éÓG~ÙP×üÛ¢J\x000bkIÆv[&Àq¼5og\x001dI<,þ~Oêr"xj\x001ao¢B*\x0006\x0000\x0000\x0016çõgx«uLTã\x0005#@#\x001baX</p><p>ÔÎ\x001f\x001f9­s\x0018ª3?ÁÅÇ\x0005/"´Û¤<à\x0007\x000fÇºLU</p><p>Vû#ECª&yc[0Ù7áïÒÇç3,¥j\x000f8`pé*>äÎZ×\x0017\x0000wÅ³6 çOó\x0017à\x0002$ìlÑÔ¦</p><p>Ë\x0013á«\x000c ±6FS­Ë_bÍµ¸\x000br/IÒn'cFòp\x001by</p><p>Q\x0014F,ük³kªb_aÁÜUk¢ÕÒõ±U\\x0008kþ»oi.CÐjå\x0007uW·ðP£×#N*\x0017Bî®é­ï¬(\x001cá¬¤ñtU\x0002üµDå[C[ê­.^0ãu\x0007r\x0019á5`\x0008Øe¤4\x001e¤p¦</p><p>OÈ=.57Ø\x0018t\x001dmpr¦êsæÂDU"\x0018õÛYzJ[\x001bH®ú-YÕÇ.tl\x001axÈwL0\x0012`s\x0015ÂtøÆíÅ&ÝTeür;j\x0008Wg$"¨`í­«sí^V \x0012\x0003d^\x0011\x0012+\x001f[I~yì¯¥ß£+ÊÖßKå½7Ãø¸ß Ë\x0011x;ÐRØ0à;etø«7Å»AÑwL~`Å{9WUÀ¶a÷±¯ÃD½ÒEÜ9¢E\x0011À\x0003G ô±r`\x0000#{NE\x001cyÉVc:P\x0001PÙ\x0014Ù§ÙàÊqjô¿å\x0010Jo[ÊPñc</p><p>Æà°É9¸</p><p>B\x001c\x0007²§jI\x0018ÑÆ)Ùt¡ÿ(\x0011°ô"ó6S\x000cö\x0010êC,w¦nMg*Ô6¥Îæ^¥eìË=(\x0018\x0001ÑD×^XÃT¶cäý¶6³\x0011^&v[¾ý]z³ÑÛ(}¹SÓ¦Âùñé.¢ü@<ïèh¥\x0005ggá: ò\x0008~¨ÆØÐ¦Õ4
Y9vÆç}|ªxJÎ¶3Y\x001bñ, [Û÷£ÇÁ®cøÝ\x0003NeÄ,*N¾C6]½\x0019!fÈr+\x0004À¸Oøã·àÙ>Ìõ$áOö*Á\x000eæbïº~JBî0`çFâæ\x0018´ê¦$Õ76¡s«$Ûî\x001ddî\G</p><p>Ié</p><p>Ç4%Ìq3E\x0012­$ï\x0007A\x0006+\x0015j§IMÚÀ®ù+f³øÆÑ\x0004©=´ò]\x0000µ©tÒ¥Y09Ä</p><p>\x0001ûÑw iÖL¯nKäÓ¿f$Á_¶j!_t¾0
ÐÃ¶(g&1.5Õ>Ä\x001bhÏ\x0019`ÂB±ûÅ\x0013dÏV\x0013\x000e\x0006ÆÈ</p><p>mI¾ï#¸Üi©h^árø%v4È¯Kx"!l\x0019nÅW#zNgÍ:&ÒZÑÜ</p><p>P¸³¼\x0010H(\x001bz¶'÷\x0003k=c³¥
T\x000e"5\x0000j\x0019û Åv~éZ¸É\x0001´´¥LpÐOåÈÈß¶ á¥éõíN;FWÇÂ Ø\x0003ðçßc5BéRÅ¹àæv=Ñ\x0014?%k½ \x0008/qpºÝÙ²Ë\x001e©¸¸KéXW¢nÏâJàÃÜ6¨\x0013aîK<*·[\x0012\x0000x4z]]	æ×¦>¯n #N±7¾ë AZN,íqøÈqqs±ñqñî\x0016èeÏ½$AeCøÌ,;Ë|b]¢rÀVÅcÜ·ü\x001b\x000c~¨\x00191Ó\x001b¾¯ñ+½'BýY&Ôn\x0010éMÖ\x0004\x0005\x001c\x0017K#oëpnUa\x0010ã&Ð"ã\x000bÅû£\x000f\x0010©)3î\x0016ã\x0006V;æª\x0018s>0!äÿ½,SèuÇÊõ}üo%.Oì:t	d\x0000Ä­\û7G%Ù\x000fz«DÍ?E\x0019ry56XFýÌ=yN·*\x0015*Ömo$ÈÒi]½\x001c§\x0001à:Þþ²!®ñÍ?[ëæt\x0014À°¸t°\x0004ÁSeÍÕðºB;\x000bë¨\x001aÓÈï¢ô\x0016Áê¡Æß¤$íøR¥òrÅ­!¦|Ö¸/\x0000=¬ÉöZV·(9 XE6ùóRsÑá¯UH©ºj\x00133\x001fWP2N÷JZ[gº&\x0004þ~`Ó?¬\x0017Mÿå:¯=»jË»Ò6\x0015:Ñ¾ÁS-Çò"<$'ºu³e[¬ô@IúÚªÑ×#áGY1\x000b\x0011üûÚ`=Fx]N^GXÔ\x000b4Çt£\x000bÏgÖ÷¿l¬I=i\x001d!{«hQ¬/}VWO\x0004ÿ¹\x0003'wé\x001b1ÝÑÆæ7â\x0014Üñ}ÛÛù\x0002Ù?]\x0006H´cP#¬ÿæ¬|èdO~ÿr#Ý+ísV Oðyþ\x0002P¶=þà:	®\x001bga?Õ\x0019v2ØT$z·ý¨¢\x0007\x0008l¶_L)°#áY´èÔ:Ôòè\x0007¢n\x0015\x0013Ç´^lÓáM\x0005¢_N\x000b*hÆ¨Ä½Ä¨{
ÛüuÜö<ÀÜfô¾èýðm/uaUSL\x0013	1:Rù`Kp¹Éõr\x0004oì\x001b·´2BWV
\x0010=CÑ·©¨¦ Â§C¡	¦kàücï\x000f^mè'í~z®a</p><p>RÇå\x000b[: ¢èH¥9öìð\x0014¶ÊgýÖäàÂ×ó8g+ø^D3*¼\x0003á\x001cd\x0004BH¨20]¤º»\x00147ç±h#øñlõV|_ÖÜ\x00197ÖiCÙ\x001a\x0011²ÁíÓþZ\x000bñ\x0005äLêüÈ\x001ehèyPôþñ#	­\x000f\x0012â\x0015ÑV¢BÆ7¡Ó%FUÁ@ß¸Dq\x0001®¼£\x0016ë\x000bÐ\x0004*\x000fÙëèíjWU£\x0000BÍR\x0006·?\x001d\x000buC³\´EÂ·=&K\x001db</p><p>£4?gºmæh\x0016Ú6±2fqH$!\x0018Ý\x0016Û÷c@.%6·kì3Gì½¿ð2ýÍþ9³&\x0005í\x00009¸ú	|ÃoÁ\x0015>\x0006u\x0000àd\x0017PÀeÆ·ÇÂÿjËÕ {¤òð\x001b\x0006,*&.ÿ¸\x0017X*êP>3Ï\x0005\x000ci\x0015EÂ\x0004ù\x001b\x0013*"\x0018\x000cxÓG0uÄI&	Õò}FP\x0003\x000bßbbõ\x0011q_ã*\x000fs`,áj&\x0011\x0004Ç^àHó$´þ>òhSÙ9ÎkáMÐÎÜ¶Ê\x0000Õ\x0002ªçô\x0010ì´ÍsåÒì=¹V³\x000fNE\x0016ø)8)¼º?\x0004¡þx\x0016L\x0000OlÑi9ØÖ1®ùsßelXy2Q\x001c'Hï\x0013»e3\x0019µ±[ºòÙ6òÚØÐ7ÊXuË¶ûKEmz­ã_>Q¸34\x0015
c^f\x0012ÎCË\x0000±É3Kaáý((á\x0008Ù\x001aLÊ\x0008«YTÈâ\x0003´2Qá¬ße}\x000eiÑ±Æ0ÉùÄ2öÁYççGUòºãÚl}y5ø÷\x0005F¥xOpÊ?ùøFVH`Ý¦\x0015$j\x0019T2´ûYY/XÓO&îö*rã}!'ûóäøáÈÎU¬[=\x000fw:ía	´x?[8$Ç\°äâÌ®Í]æ{Ì7Ì/©`¢q.<¿g0ã¹\x001c6]ÿ¸Yß,º+»\x0016eÎï¨\x000c
ø½ªª\x0003ïØ\x0003§[4a\x001br¨ì¼B
§²²\x0007ª\x0016ÄÓèà2%ªé¢ÕáÙÏÅDk¡ÂfnCü):j</p><p>\x0010\x000cÌ¬>¦Ö¢Æ7\x000bF±ÚäíèF°G¿R#°$éú°ÎÛ«
!¤cTdëâj\x001f\x0003VÖ:é¤,^i<,\x0006\x001bö'5:\x000e\x001c¿u{\x0008<V\x0018÷ \x0006\x0014È©r]Qçø\x001fjbõØúC¥S\x0004\x000e¯\x0002¤/óø\ÓòaL{"«©4\x001b¥Hº\x0013Y^tva~£<\t{Öä\x0014¹Uphiék÷hìWûõÝ\x000c".\x0017\x0008\x001dâþx\x001b1©ïP\x001e¤®øe÷7h/+&ÈIá±óÛ«e\x0018\x0015¾Î¥øR\x0014g\x000fw!\îv0\x0013åÕ7ãuCùÇ¬2nÄ\x0004Z
ûùEÝ\x0005\x0012\x001eN¯ßä_­[\x001e3O\x0004ã·\x0001+ô¼XÇì<¹obßÅ	\x000e¥g\x001cÛO|ö</p><p>-\x0018ÕR±û¸!\x0006sÓúçbò¼ªcJ
©^JP\x0005ÇI\x001d_Þmùï\x001c\x001d556²>Ö¡ÆáÊÿ-\x0014@\x001b³ñ#É
\x001dBÝj_¼»5#jù\x0001ï±N¿\x001f\x0016¶ð|TaÖç+ç=-A\x0001 þØ@\x0005¼W\x0007^L #Vb2*¶k8nGÕqf0¥yÉY</p><p>ÍMË¼Àë%ø}ØæÕ\x0014}áÙý\x0002ª°JâñµÒ×#\x001a¡cÍÜEêk\x0011¹ËHÍN£Î«*ÁA	{læ\x0006«Niæas©\x001b°²afì.ç	2¯K6]-\x0008øæt\x000e;!qÈ·\x0006È\\x0007\x0014Bg\6ÒÊ+$­¿ê+vjb,ÙBZ[7</p><p>²<ç¨U£\x0004êVíÖ¿ªj|,áÊÛtýÖGËÍÿ6&ÂLÖ`X\x001dIªmàþW#ÿ\x0012%YÄB?\x000f´=à8b\x0011ÿÆh,/ú\x0002<Îe\x000e$ùßt{%Å}¶hBÂÜï\x000e¼\x000f2t )ù2ý¾\x0012S\x0013fÞM\x0011ì¨\x001cº\x0019÷\x001bí¸îÆ¯Ô-zªH¬ÿü-¢@\úÓx6×ï?ô\x0006éßÎ±Çà ààb\x000eA×öWø/5«û#Jûzkãâä<\x0002\hº.ÚË¨´ÉõZ$ÓôÕQ¨"Ä¤eT\x0017\x0006\x001bè\x0012¶ÑÒ\x0003·\ùÏºÛzK?&þP;«ßAÌ\x0014ÍÈ{Tàîî\x0006\x0013@@ÜcCCèÎ83Su5¤F*ªD«ü;jßfêU?À\x0000­_©n÷\x0011Ë\x0014üø±ÉñwV</p><p>ÙùÈÒ\x0007¯È­ýûü\yWl@É1\x0002Ðøo{\\x0016	\x000fñ~ÐH¥~N\x0010\x0015Õ\å\x000eFÒÇ½ö³æR¶¿°->\x00059C\x0016>\x000b/TB`·zk¸Ì\x0007È¹ô®M\x001a</p><p>3P¾úO!Ê­\x000eµ^e÷\x0018U\x000c¿©i¬Ëî$pÁs¦á¹f(9ù¸7Íèî
Ì³\x0016&Ô¾X)\x0018i½a÷+¢Éáp2¾ªvLmªD]~n-ãM
Q\x0004ña\x0010±eí\x001aþþO.tdï¹þÙ;Ûú=hT;;f\x0000c²ª3--bDÑ¾ªzáåÍ9:¶\x0014âÈèØD®Ø\x0014éÓ¶8¢å>\x0012\x0015yÍRæFa\x0000ì¯Ëa$¾ùÍ¯ÜÛ#|
3\x0019­?\x0005\x0005~o/UNí\x00058ZÎ¬Ç\x0005þ\x001d©þ`×Lz,DÒ^\x0019[¨í½>ÄQ"]P+ß4Ø0¬Ä\x0007Æ\x0005ØZoÝ»~Gz¼CmA¹V\x000e-\x001d/R¢Çº\x0013ÎùÚ:\x0002ÈXþTë]Li(9úr´\x0016ê?ÖüK©=|À\x001f/5/Ë6\x0008ô	Ð Â\x0005\x0005¶üòg.½L{!³Sf+Hä,¶>cz6ÿû\x0012×ÃÂ kËt!G@Õ</p><p> SÊeQVt)_\-M8[\x001cÀ\x0002W\x001e\x0010\x0016»XþH$\x001f\x001c\x0018ë7;_y}Sn\x0005+Åø¨lîx6°®Õ2Ûm&á.R Pé¸\x0016\x0013¿Å\x000cödëu!6c9m6h»\x001b÷Kn\x001b¶Þ\x0001·@è@hé\x0012ãW
5\x0002óÎðÑÛñ\x0017õDªÔ\x0013Ø t	\x0003\x0007+¢§\x0011\x001f¢åe\x001e\x0001¶ÿÊH`ºãÈ\x001eB\x0003cªb Ø©F6Rz\4P{ß\x0012+·Û\x0004á\x0002­\x0007D­\x0019¯\x0011\x0007GsÍÂ\x000bø\x0002ðµ\x0007âû6\x0019\x0018ØXäÍ1Õü1J]&.¸)Vlàr\x0005s|Ç®¿ ×\x0014ÎJ:þ'\x000fÜX*«´@-d\x001c\x001fáL=^{S\x0004\x0008\x0010:V,-q!¸&WùH(w·z¯Ø¾øFL</p><p>\x001aÂ\x001f-lyÄËJCF</p><p>Ü/Ó¬5MÂ\x0011C;õ/¼ægÐ.\x0011H÷ô~\x0019\x0011\x0010¥\®5\x001cÌ²}J\x0002Äóö¡i7©âÍ\x001fiÛ³f6\x0004(h\x0012T\x001a¥×\x001dE\x001dE/ÿ-n·:´D.jÄÞ\x00004ÎÄ·3\x00158¹­xÎ[ÝZ,/ªÕ©¿$>ýW¼\x0006­¥\x0011µBÊzñíÈ\x0008$÷çêÅ^Æ¼±:M®
\x0013TIqÉíãÚfõÆ«d\x0013$Õü~>ÍO÷Ü%qCY»·	Á;éáÏÜ#Z)Â\x0014¨*bþã~\x001fvbÀ¨qÉÑ8\x0000ZÅ¥Ä¶òHs®F¦èÆìÃìo</p><p>ÁWC1ìQj×1»×ü</p><p>\x0017\x0019G/,C6ÏXa¢§1[v·èu4§2ÞíÝí\x0003Zd L-\x000cG\x0016_Î±g¶½ÌµÜKµêÔìB	ª\x000ee_»KN {¦2k}H( q°ï_¡
.Ë®¬\x0019¥¬±WçÓ¹X</p><p>\x000c¡UgI¥WËÔKÌÔ\x000b\x0005ñù(\x0010.iÉ\x001f÷<\x0001ðû)\x0012ëÌk¶Z\x0014Dp
\x0010\x0001»\x0018~øáU«ÐÛpwÕõ^	G÷íhZ\x0010ñ?</p><p>>aj:ò¸68Xô¯\x000e\x0007òXÍ}âðKw­ä¾¶Dt\x000b§:âSÈÐ\x0010ç/æ¹TSO\x001d$I\x0011ÿLÂ±´\x000fØtùL6ÒaÉV\x001e=Õò\x001eÏö\x0005¨m³A09L½g\x000eè K××\x001bÎ</p><p>\x001eW`P¢ÛðÞã0\x0012oñÂ\x0014ì´¬ËKÊËüSêMÙùsÈmSø×àû	âÇ`=ß2\x001aJ®\x0017\x001b\x000c?(·O\x001c\x0002ÕÇ!\x000fpö\x000eÆ`©4Y9ºlú\x0004èJì|~Zp¿U¶±!áàÃè\x0008tûcWfÿôIföÜ+\x001bÍÕß0oóý(F²;c ¥M6B?ö»Ù©P2Óa.7iÀÕ åx\x0014½¨gß~BX]]³¯\x0007hP·°#Â¿;+ñ?kÕ0áøBº</p><p>E2å>~QÂ³FµÂ52\x0008\x0003Ë§¦ò'<7°\x001c½I¢IÊ\x0012êØ>¿Æ{æðUSOcSÖëIsÚy,BÅ¶\x001a\x0008ÍV¤ùÝ2\x0005B\x0011
1ÅJ\x000b\x0011\x0019ç¢8ÌLA:/!Ó\x001a\x0003xÈÂÉ¾,6ð%N\x000còíðsp\x0011L¶p»gûÌs©anÜÜÞÑå6ðÇ«â\x0013q[Aà\x001b©uÿ\x0001ú\x000bi{-íÚÖm\x00114ß h\x000e@\x0019\x0012>²\x0006ÔRÛUH0a¸f\x001cr(¬Ô¡~ÄaM\x0012QN+¿Hx\x001aõ\x001fK@b\x001ar¯\x0006t¬z¼Â?íìuMB¡¥x_ù\x0002#_</p><p>®\x0012çÎ	½5%Zå\x0013¸ñ"!Ë'°oÔ"\x000fdÅ]ñ[9¯äóeÌ±ÃqÌéqÌMR2\x001av\x0018E\x000f\x0002XÑo¾Å@u^®ÓkáÇõ½×Øq\x0003vî!S(XÜË÷µ4l-Ü\x0005½?ýS<Ajj#ÃÆÁ\]¿ïÔÙg½\x001b"Ô\x001bø6¤)õNAÌÈbóËmÅç¤GÈ4AöSæº&ÛÆk\x0014B\x0018Wtåá¹,G¦µï$¬|Uå YÒeÂ,Uµ¦Áµ&¼M\x001fuqÚf_9L.A¦L.ü>ÐºoîrÊZ¯q PäLÎ\x001dÿô´à³Å]Rw#\x0007µCJå \x0012¹ð\x000e4û\x0005\x0008ù`@Riêét×£c¤ñ$\x0014ï:'×ìßeÔ	ÃÃTTPÍ¤¼ÿ¾e±æÓ÷º0¶Q\x0012Õ\x0004Ðh,{óGoÈï`j\x0013\x001aÈrö\x0011\x0014&\x001cZ¤^µb~"&íqSn#ZY\¢H\x0019ÔÃ2T¤²Qo¨%ø%\x0008?\x0003ßbÒBF©ÃT³üSaE\x0006Áÿ8yæ\x0018ÜãÁ®À¹Ö\x001cËQ_³*5³¨3$ð\x000cZ§</p><p>Ýg8³\x0005þR\x0012U·æó%ÿv\x001eÞpØ=Îoñ	üÙ\x001cOXÕðÒè=úðºèwÈm¬7\x001a×\x0004Ã M*\x001eÕ_8B*éPÈ\x0003ÈëÚ\x0015\x0013QyóZ-e³T]y+\x0007Â-ÇÜ3i\x001d.:Þ ½>ïÄyÕf¥ ±?Hô¿÷ÕBé\x001atöl!\x0000§¨pÏ¼§lHú</p><p>mè&ÝÖR·jDc<yN¥é\x001eY/è\¤ZèJ $]Yï\x0015HèÞ\x0002Å/×É rµìveàýÒ\x0005nÊS\x0013u÷LöDDk\x0006U\x001dº³¼_~\x0004þçÅu\x0018 ¼K \x000cá«´xZtÏ\x001f\x0018Ç±¼¶?\x0002(½5÷§4¢`%]W\x0010\x0001`áÐ\x0018÷[ª¨´\x001f°;zÿ\¶qBH7Õ\x0013år\x001d\x001b²ø¶\x0013Óñ\x001fÕ\x001e\x0004\x0012Al°¶xfêétôèP7ÃOÿ¹\x000cX4\x001eÎüË.%ÜÝ°	/f4(</p><p>­\x001dûÄ¨-~f\x0013\x0015¶ªzÅíÚOêÓ\x0008¼Ô	Þ489å¹ã]</p><p>Í¨
?¨N.d\x0004ù\x001fx/C¤QÚ¿\x001b>y$É4®Ù,ìÎ¶.\x0002Päw½Èª^\x0017'äN)c.\x0014£³2ÈXRÞ>$ÓSí
}pW\x000f2øµWF''õ¨ÚyÎÁÅ¬§²|óIó»Úá\x0011XW\x0002]+æHþÇãÊìRÇ\x0016\x0002\x0002ÎBÖ\8ìBµàBq\x0017¹\x0018o]ye(VY\x0018\x001eDeºà
\x0015ÅßÁÜZé}O¦Â¬z)®BF=¦\x001bûî\x001b_\x0000øóÓD_j»R6·[vIÈï(µ</p><p>[z
\x001fEÌ;qÄB*½+q¤Aé.]c\x001b«:@q¥|¿KÅãé\x000eôfy\x001c\x001c×]öÜ\x0014©s-eÓD iä	úô;·\x0011¿7³ÇZ\x001aO*æ,ùÔ8ÖÑ§\x0019ß\x001cñlþ)C"\x00023ö>$XrXg6ì¼mV¦ºG\x0007¡«}¥yÕ]µ@jí1RËýgIÅë:\x001e¡E£t\x0001ÝFÐ\x0010ÑN¶2ùh~Ö· ×TÓ\x001cÓ\x001c¿6\x0007^º¹F\x0008dzÿA+\ù\}oóã·ù±Öh3­$¼lö¼÷Û\x001b©R\x001b»ïîRN.\x0001v6¥ ·êP®Ûñ"\x0011ÖÙ ú0Í[\x0007ó-È¹ñ\x001cS÷tg¿ÿ\x0014AÌQKN%-Ð@ÏÞó\x0000n­ª:có]Ä</p><p>.!²t¾ÛëÉ{0"³#öèeÛøi}¤</p><p>G\x0003)&ª¥ôOktr\x0011ÂÀ\x0002</p><p>0ÁØ1éâËHj!#y-ÝV,Ñc*\x000c½bï\x0018pýûS\x00039â</p><p>N?d·
\x0003\x0019"ãHÞR\x000b%</p><p>8È:Ù\x0015üaKÅþÌ¸{oª³ ç©CV\x001eÒôjî+
ü$ä0aQ]­H%.ð\x0014NûÆ@G>-áê-1\x001f÷l)ÚRÓì?4¿¹£ëFRTKp\x000cU\x000cZ?üôØQVrØ2×`\x0001Â»ú(­u$­²\x001f
9\x001fY\x001aRwÂ¸lèÈ^!¢gÌ!àÝÖfeÊcgåã±O`ÁmÉÐ_Ý1Ç\x0008
s^{cý\x0001»§Ú³6<îÙ«C½)-É÷\x0008\x0003Q;I¾¼yÖÓè÷Þ×\x000b²\x0018ã;þ¤í\x000fß]ÿ\x001f\x0007¤®ê¶\x000cU~þ¬ë~\x0001©×\x0005§ú­½\x0018jÎRã\x0014y¾*\x0018Yi{¿°AÖä$tçÒt«PÃÒHrKq*¢â"åaý{9ó-\x0002È\x000f%åÛpçå7;L\x0008T\x000c<3@b-f4Ê6hGÜ\x0003*<X %Ë4\x001b\x001b\x0004ðýmv°hÕÞ\x0018Ô\x0010¥¿³C8¶ø°ëQÖÉoªðin\x000f?^ORùòQy¿Y\x0012;8b)L÷pXt­¢"$*Ø\x000fÑj>é÷x)-Å\x000e[Ì¾Ú-÷í[{\x0012Câu~PßÁb\x000e»\x0003És5º³z¨[ß¯POSv\x0011Iwuõ\x0004¶ÉÁ\x0018BW\x0012Ätø«ÆJcÊùØ}¾@­z®EÃ:ÏÎ¼)÷^s#b\x0003\x0018±zT²Ýl¹ò\x00005\x0018Ka9ÙÄ»P4B}=InÍ£cKnÓ$Kÿvæ6°;\x0010GOÓØq\x0014ùºAì0AæÝ\x0006ìÂÎ#is¦ëÄ[n]\x001c£¯\x001a"\x0002ø\x000bg\x000b_\x0008ßWn\x001ag\x0010"Á­\x000c'³÷öfNy\x0002úÆ\x0000+¯\x000b§ÿ¼À\x0019U©mVK§â_èæCW5Nù[\x0015¡PÉ#M\x001bÎ
_\x001a._Ow(ÄKC\x0006\x001c¢ôÎ~¡Ðã\x0014ì¥BÜ¦ôý¶U\x0006IR\ÒúþmMë(/dW\x0001ñ\x0019WgDz\x0016\x001e\x0007q\x001c"òÏ"°\x0003ªá¹VYÂ\x0001®\x00089*({8+³ãLÎí%{»q©Ä\x0000¢Y\x001cmt*T¡ËUôÀ,_Ê\x0001ærFû\x000b\x0000§ÔØÄQø\x0006'Z-Án$C²Ì9áó\x0006V\x001cº×nºÔ¤àz\x0003¸Å\x00047µé\x0017Ôq</p><p>æu§ê\x000fq\x0011ã){	JR¤¹­Ê½]¿3oq!DÓò$Ó¸~0¨·bqFLÉ.C\x0007+XêK<W·¹BlÌ\x000c\x0014|*7Crj¶rôhÌy\x0013ò\x001fGFa}Sìì\åéÖ©·É|OBg§TòÝ^cD\x0019Rrd4e\x0002¹©å\x0019\x0003ÅS`y6\x0013èÈ=¿yæ\x0001dÃßm\x0012\x0002ºTgQ®/õÆduA}úM
øýpuå8¨íM_\x0000k(÷\x001böÌHäï\x001d.)|K\x0016]\x0001'J\x0002\x001a\x0013\x001d\x0007oü¬\x0013\x0012DÀ²ù/ÀYeK&>\x0007$Ø,õÂ\x0002+«.TÊ\x0007Ò\x0017 ëcDóï_æ¾9ÐÞîùPØ#0¿¬ëRX¾qþ?y²#&µ¼ëTYùÓ]	Ýv!ïÓøüóX{~jÉÔ@=-T$8óOý².ú\x0001~ð\x000b \x0010¯^¸)@Ëp\x0005ç¤</p><p>ç\x0018`2lw·÷\x0005XG\x0007ò~Ðü"Û?Õl¹¤Gkü\x0002Ø\x0013iñfSôýL
\x0016ù<\x00150kx\x001aV\x0013ÉÆâF\x0016jÆ\x0010©d\x0004\x001cÏ5»Ï;;^\x000e÷fPY\x000eüâ!NxÌ\x0017Ef\x0010W\x000chãäJ¢2,Þ</p><p>!Îno×hÂH \x001au¹</p><p>JW´Ñ\x0015LªLP\x0014oÀ7+P{]ú\x0002d®ò:
\x0000\x0002[«$Í3\x0005~\x0006a´§Ùï¡</p><p>Q\x0010d\x0005ZÌÛ!\x001d~äNÑ§©&på[	G\x0018}Óþ5"	ýý\x001aÊý, \x0001¼¯á§y,ÁÚ<t'Æ¢|à\x001cÄ®÷\x0008b0Þ5{kÈ°GùÓ!T^0#¢Úò¹Õj\x001d+\x000b
¤ªFé1l\x001eö´\x0014ÔN±süüñ9£\x0019½8ç6X\x000cOú\x0018M\x0003£²¢tYÖè6,\x000bç+Ir\x0016.=;};\x0017LôOÕ´ F\x0016]öz.Ñ\x0016 ï÷WN\x0002`i\x0005\x001cb¦Dé\x0004³8vu:¾¦'¸NÊ¹e·¹j©`MF³%
'¢µÚý¸Y\x0008$ïôabh)$0=Ó\x001fÙÞ8YkÒL+»r\x001bg]¿+\x000fÑ#¥º¹Ø"ëNÀMSÂ®î V_Ïõ6¿×!G-B\x0011 ã¡·N\x0015H</p><p>"\x0014ÇPË_\x000c\x001ca=\x0006'\x0004¨PY9óìoh|ðB\x0019Hì¤ªnéåÅg®\x0001f|;\x000f.¡5äLs]úKuÍÒk\x0014»róßcÀ]¦Unzìuª\x0001vHªö´	;ÓNZ®oÚA\x00085åcâSÖ[yÃ¿: íÊøñ{¦£\x0006·HRÕêÙ£)\x0014¦¥¦exHû\x0002l
ÜÄ\x0008%³ïºù\x0016\x0001è~ns×Ð¦ëâm\x0012)<Ïø¿Ä\µS\x0017\x0002qâ÷O-³×83<\x0008ú$ñ^\x0017§}£õçÖôwnïÂbÔ&¥V\x0016B\x0012\x000e®r\x0003[ãbr¸|ÆÈË2ÉºÀhìÅ4«äæÛùõwúß\x0005¹\x0001¶\x001f±\x0003Ù &EaW*\x0019\x000eVÐtêà\x0016]p[vLzTÕ\x000fßÞåY?-+²*5Ë\x0005\x00083-c¾V¦\x0011"¬ÛZ\x0007Ô\x00113\x000c\x0002¾@òbª=³Tµm\ÌìZÛT\x001c{Â¶ìþ¡¾´\x000c/ÕAêöV+3\x001bªy8cgóCü¼ª2é~MÅ \x0010ÚçÕãñÌIW3É³\x000cæÃKús&Ùªúâp§ÿ±Ígê{¢Ë¿%^|®"ÛÙª?¿*¸Éÿ£Äjä\x0019ü¨§)Õ%÷J÷ê¥H1C®		:|Ô?û\x000bîEÕ¸Yù.`\x001c×±,\x0004\x001dHI^ eÃ^y\RH\x0008É½ªÊ¦\x0002¾© 7iKã·î\x0014ËVÆ¡RE¶MíO\x0012a¾ùÎ- =ºÌÀH\x0017A¢b`ù\x0003'´ò\x001d6bcR1Ì\x001a\x001b °Zö\x000f\x0002<BîUJÙõÅÐÖ;´±m¨»a'ñ20óÆ¥ÙÂ\x0015à\x0013j®$1P?àìBO\x0014à¼áj³aéY\x0001)T10\x0014\x000cqª£\x001a=ÛåF=x¶y\x0016g÷ã'%öÿY\x001c\x00105´Äsû1¬Ã\x0000ÚÂ\x0004k\x0012v¹\x0004BøÑ£8µØ¦ÁÈ*ï\x0015eÇ!îÕÂÔßkMC/6Ø¥\x000e\x0010ÂQ\x000fHy_5rò´$o>»*µ¥l¨48,¶Ö`ç?\x0004íÂ¢×¸6jF··TEßOy7Û¹g6òÝ\x001ek^\x001c\x001fO\x001eÆ8\x000c\x0006\x0012\CÐe\x000e	ðã£ðá þ5Âø¤ÔA\x0001sÕ©qúï\x001a»-æ\x0005\x0005?e»\x001b¶Õ©Ía"\x0014}5*Ô\x0004ÔÌ\x0012iZôbXsMKCqyÄ[Ñä}5ããÈ
È¡ËïÊÄIa¸î&\x0015ºWwÝ\x000fuiÖ_þÚÅèSk9JAßcçÃ\x001b¸\x0008;ÑI?ÚAj\x0007éþXæ\x001cÍ¡|õ\x0014*\x001d\x000c\x0012Xx\x0013f{I>Q»\x000bGí¨uS\x0016¬&ö.ÖD& ú\x0002\x0004Â\x0008Oà\x0010g/<ÓE$\x0015ÖN!¢ e\x0016»¯ä\x0005¶¨áïÕÈ\x0012Ê@ÐÃ¾M¢\x0005¢ØÇ­~f¢ N\x000bÐBRñ×³fÜV\x001a]¬¯q3õ¿ôª
Ë\x0015o4´Zh'nÌÏsê
;\x001cÙ`HËìY|Jv¯\x0018­oOÅ
wÁmÒ$¤å),`þY\x0016| 3¶î\x0016¨¦1\x0015ßÃ1\x001f¼¼}[±f=3u²ùæöO«Ä
gù:\x0011$×C\x0012/Và\x001f`«q$f\x0013ïèA[eÕfÀ|¥</p><p>Ï\x001b\x0012½ó\x0005h´­¤\x001föÀ\x0019iÌä\x0001&IÙ»\x0007Ø.\x001dÑñtGû<$\x0005ÅÓvAý`/¢l²Jtplæ=Ã8Õ2ÁwJ²e\x001b\x0001Í¢¨Äp¾@J¸ûâ\x0016Á¬9tê·ïÎy\x000f*/þä\x0017'Ê\x001eé/0\x000eKÓK\x0003$p	\x001a\x0002,\x0004ã\x00172é¢±nY&.US\x0012xOõÖ\x001c\x000e\x0002éç#Ò×«l[Ï3-ï\x0016ü¾\x0000Fâ3 Sü¶ö\x000c¤²mÊ\x0012±òg¦2µÌLÇ©Ö¡´!GÐ]É¡\x0001õì #Ñé+éÓ`á¦¼<\x0004ÖãgcäzKÍdçÞNù|Ö¾÷JL=yÙÕódUÿ}×à>û/\x0000_$kÄÚð¶3\x0007êå¯÷dF\x001c¶\x0015"R\x0012\x0007SßKîÛ¢Õ¹¦auîlrX¹.«,m!ì^0,\x001c6`M_u._\x0019</p><p>þ(
ÕFö^\x00112322&©N°¢\x0010UFJ_­ï\x0000ÑöPAµ
Øk\x0012j\x001dZÅü7</p><p>Äê9¾®M?öÊ=\x0017Isu°?<Ë%úz bÜaJpÐ\x000cG×#8¸4ÕÑBí
2³p\x0014½0p&zÖ¢ùX\x0015\x000cl)¶àÈøq¡|z\x000fþ\x0013ìvòD\x000f*bö\x000b|WáX¦À'âÆ¿¢Öm±¿Ù\x0010£</p><p>\x0014?_yÅPèR;LÂQÚUeOíøå_³.
l=«\x001dªEb8Õ¢\x0016£rd)hËM¢û\x0019EÚ«Yñy	Ã³è\x0005Yïr%\x0018éHµÁ3e4#\x001bù$@åÐ¡ks\x0006,Õ\x001f+\x001a _U:.8WZü5<$Ð{$Û×ð'Ý²W[¿`\x0016Dä?Àø`°Ó¨O}\x0013RgÅÆ¤0ì8&\x000eÝÉ>\x0004ÝwÌæíøÜ\x0013K\x000bâ«Þ¨QûLQeÒGý\x000b\x0019#]¨Qcãýy#ªÚ}GÀßé\x001bÄgm$H¯Ý\x001b÷</p><p>ñ~Viïê¦\x0014)ãà¹·ù4\x001aEïòé]:ý\x0005È\x0001XÕ\x0002×:<ùI®\x000cG7$!7$Y\x0005Ä\x001b>o8
Ï\x0004:ºø³\x001eÖ»íù<\x000c§ù+k\x001bmÿÌÿRn\x001bw¤\x0012_úö ´XbáªÛ0½A£;i¼T:á?¤é¾\x001f·©â¦Ü0%G{°Àì5áÀ§\x0004Õ(\x001dE?XÁ¹^\x000cÞ\x0003ñ_zâi¶\x00194\x000euûL¬Í¾<Ô¢Ç´n\x0019¬Øbèk;²µ¨#GÍÜ$o\x000b²ÊTGLÏËÚ\x001dÕÇÕû¨¨WÐÇ%\x001bëpÜ\x0002+ôh¤Û\x000f.y²ìt\x0003xäl;ÃÖ^T¥¶Ê6¹ò\x0015\x0018\x0019¶h03\x00154Ñ=ìs¦jÒ?Ó5g\x0017ä|\x0001ÈõRôÚ\x001d\x0004 éÚøÕ}ÇÃE±.9Àu]9Ö±ÑÉØÔf\x001d_.z]\x0014\x0014Ãßõ^dÚ\x000bOç]áû\x0002ÐÛ¹°åÅÔl*h;ÒÃ)XKoÑ)\x0013`·@ú)ÃþÞ¬"\x0008	ÖOìöR¨\x0018c°\x0011:	PXZ¨µ\x0010\x0018º7ë28`\x0002\x0004´2\x0004#ï|½¹1\x001eTL\x001eåú|FÍz\x000c(9\x001c>	ßùþ\x0019ýÐO~W\x0005qæ-\x0003ç"ÖfÎÖ$)e¥g%G±oBàJ£Û\x0015ÿí]\x0011â2 %RdÄÐR]K¢Ê;³ðïjä\x0019Ã¹«ÊÏd©\x0019,ì\x0017àçs­\x0010ÿþQlçk\x0000ý[;\x0003\x0007ÉòUû`¼8Ó¦¦*Ïù©4g1ÎV\x001fUt£¿;	ÑéÌ©·³4àV\x0015\x0006\x001dáLXÖsß²\x0006[ÀAa*9D4.,R\x0013nCÅ%=ô~-/\x0000õó\x000bÐ\x001dÎ²W\x0003£a±ÛèÃOEôCtð\x001b_Í¤RSIãBä\x001br:ø\x00143ÈÖ<7OÆ\x0005n«=5s;±;êuYcwßÁðó\x000ciÌ\\x0012÷p~å%¸ LBBVÿ®C%/yê¬¾Ûéð¿á4;¸\x0001ÈÉUøí~H\x0001.ÎÞÙ÷</p><p>:ìu\x0001ÜøqØ>Uv2%àµ\x0001þÅü\x000bàYØ«å Åðý-r\x0000«Ùêíw>ÒR\x0016¬,mß©\x001a-5}ÊlKÙöDAÖ_Q*"G</p><p>A*£[\x001ct\x0019\x0010\x001cþ\x0008ßëÂï\Gk;.\x001b@ÌÝÔû9Rr¦ùÃ\x0017Àüí\x000b\x0010a2¹XWrÆªÝÁ\x0017å^]Kmôr°½m$[\gj£/\x001fG\x0015)ú\x0007!j3Ù¬\x000ed÷7,>+·\x0002M7kÆ¶©Ä\x0006/{j§­9±\x000c©+`\x0005\)<W¸äù\x000bo\x0019ÁÉ\x0006KáAã\x000b øä­¹-¥"°nÙ\x0003Ìb\x001dðûþoq</p><p>N¤ù¯Cw³®Ö\x0017@=àø\x000b\x0000q©vN¸\x001fïðÇ\x0012Vs'ä0ágO>uKN¥pw\x001aÄ\x000cÍöiBK21-ëØÓQãCìË#ï#s°%#àA\x0003Xø^mËIµãE¿a¢oü\x001dØZu`&<\x0010Ãw¼Õ¶\x0018 á¶Vô\x0005\x000eß0#+,Çþ¦ê6%öÈð8õ\x0003ÜJ\x001fôø;â±´\x0010</p><p>\x001bBÊ_5QÖ\x0018\x000eDrúR;</p><p>AááøÏÕ«òC\x000c³\x0010ÅÐt«\x0010ÇÈaÐW¶óÂyúÀ¦Í4{Ti¶câ/FÒx°Ø±!e\x0018òp"\x0010ï\x0013pÒ3+¢ÉÊü$\x0013jf\x001ay\x0002ºrAyµPBJú":ÓÿGoùíç"üJd\x0011¬T2!MH3µ¶íjX}R é9hèE-WE\x0005*\x000c\x0011é
\x0016?\x0005MP~\x0019	¢¢ën *Þõ[\x001d\x0000\x0011@@µ£¹c~;ú[\x001am\x0004åBìr*«)m§iÀ6ÄÉU,9âÊ¦µÎYÉÜ\x0000E¡</p><p>ÿ¢¤ÿÉiÈ Õjª;~2F
Áé¥DA béBâN}[º#'xe :Ö¿vS]¯¤\x0008J×H¤Gw[ÿ\x0002ÔÒºQ2vP\x0004¿°æÎ\x0019I@×0³sØ"Å²h\x0003Ð\x0004ÑÌÄe°\x0006'Ö[¤\x000f;÷Ou7	ZÌ\x0008?ÙI\x001eÆa%÷¤ö§¬×&ò&µ<\x000f\x0018ïØ¼\x0005</p><p>
\x0013&*Ãß"\x0010ÔÿÛ·&Þ#ìñ² [ÛÅ·wéûÃ\x001e*^:Jq+¾¶±©k¸FþÓ@\x000f.=W ½W\x0001
³(à0\x00134òÍ}\x000f[\x0018?Çh¢Cx\x0018%\x001fçr\x00124Pñ\x001eoLàN+ß×M³ùq4
kEÃÇ\x0000/EHLåSÂh\x000eÖÿ</p><p>MtVõµµ¶@¶\x001eXk\x0006Û\x000cSºJ#\x0013Ýv¬#ú&j\x0002_\x0000==µ£q\x0005\x001e.[Þ½\x0004o\x001da ¬`=&n#õ´£ÔR\x0003Ü\x000c\x000f¼\x00071Ñ\x001f!u\x0019] \x001848P|\x0001~´\x000b:\x001c\\x0008o</p><p>8æÆñ\x001b\x0007^gT\x001c¦ña{ü:[Té¤Ô´,M\x000c}\x0003éêÉUL¢÷­d¸²\x0011Í[U\x0002ï®c\x001eòØåZæ.Ö¦Éëh\x0016\x0013+\x0005§\ÿàÞæÕhÆ6v÷\x0000\x0012ÂL\x001d\x0001DÄ\x0007¾_\x0000Ý=2\x001cøËP\x001b\x0000k\x000bíJpPS\x0017L¼Ý¤å*w´¿Sqy2<aý\x0019\Ä³í}u%3ó\x0015ÊáE<ã\x000f3\áS\x0010¡UÜÊ\x0016¯%³\x000cÍ¹j\x000eC©¤\x001brM£>\x000e¸6j\¥aÑ[ý}î]\x0001m2æÌTü$U¿7Ü¡¶`:_ZG%>\x0003F`Ù\x000c§\x00150\x0006ðU!NZL\x0014Ä{¬Õüh</p><p>à%»_ìÍg¨·înÙî*\x0017ðÓB¾ÒÏ\x0010Ôcz]ü?r./h3t©ddk\x001eÓc\x0003\x0006±Xæó^\x000f\x0003\x0000ª1ÇòsyØ`\x001bIRÈÌðQ\x0012ýäaàwâ9\x001aè\x0018@\x0012\x001dJ,-Tx¸YîBá\x0015'&**\x000föÁùIÀ9.\x0015ª[_9«2l ÙVæ$ßwb×\x0000</p><p>\x001eª|:l(Hýwö¹H</p><p>8A\x001b>W[<þ®[uéÃ\x0004\x0005|:Ýdô\x000eèBXxèÔ"sF6!#'ÝS\x0007\x0013­!$ã'µêµn\x001fËøPdºãsCÎ
C]!äV(É3¤å	Q wéÆuÆ_Ö?º\x0019\x0007É>ÏÃ</p><p>FoOì\x0008\x0013Õ´4ë(Ý;\x0012ö8Ñ\xd\x001aÂÇùàÈÉ¹1\x0004\x0006K\x001aôU©3·W5¸$ ìô\x001e\x001c¼Ûáhi0Iß¬I{«×Ôn\x0002\x0001\x000bì­k\x0007ðá5LG»	õã z\x0002ÛÔ³ñj\x0014j=äÃ¶Y~ÒÀ`¤OiYx®µnkÒá\x0017úX×Gã\x0017`"f8\x000cC\x0001«L\x0016Ï?jö¿,Y®sÝÛá/B·éQ°Õ[gÚáµë£PÂïJÎ+Õ(Ý2\x0014\x0018AO¤Ò»½Ç\x001a\x0000\x001bÙ.8a\x0015Ê3\x0017³½I8ö\x00055ûfág·æ\x001djC÷\x0002\x001bRD¢C¶\x000bê·\x001cñ¨Å¥=\x00083:`>âZ·\x0002ö¯ña%\x000c</p><p>\x0005¹±´\x001b\x0004©C\x000c/ÅLL~9öZÅFnm¤®\x0003</p><p>n«	\x0015\x0016\x0011bSDF`¨Ç\x0011L%ô-\x0005Á¤YÂ\x001f¶½»\x0013j,í¦,Á!]ÄV=Ba­¥¼æ¡VßhõGWÖÄÙu\x001c^ÎlC¦pEäAñ\x001eªIÄbE\x0001Òg-®32\x000e®sîb½íÒ&InùÂ²±Ù´'ÎEG@!³@d\x0018Æ¹«ïy\x001a½Ñë$¶a.eS=ÏCh\x0002m ¦¸¿Õ4ò¬§2]8ø¹Õ6zÒÔúøcÈ¼G-Í°ß~?Óù0²·\x0017.÷£\x0014ì*ÓàÄ¦ù*\x0004dëÌ¼*×¨\x0007ñ'9JG}7
üV;¡"AàDÞö±k
\x001c\x0014]\x001fqÈ¦àD<
ÎðÏ\x0010·ÿ\x0013#£ÌóX\x0015[.;\x0013\\x000eØÏ§3È(6p*\x001b\x0015öA{õ	\x001aivUBæârãÀøæÒáÆ{ µ½ÚpóàV¦¨Ë÷\x0003×ø\x0012&ÑÕw^¦+yJªÚàÄÉ\x0011Þ\x0001ad\x0015®*×8æoóm@×Îí_\x001aO,ý/ÀùÒãTzËaC[{\x001c\x001bVrr^Ô\x0006\x0012</p><p>åÚÒØ,¸Gý¶
X§[LSi«7á\x0017O¯×NµM:Ò\x000fõ\x0007Å%h\x0000®°¶\3	ü{ãþy\x0013H\x0016ýßHZ´CVÙí\x0017\x0016}ùBiqì©ÉR\x001de"ÕSÒì</p><p>*3ºA¶ÆL´§Ò¼å³\x0014lR²8M¥À8U0y\x0018Þ\x0011\x0014º¾µÁeØ¤9þ¿	ùáÊÐÁ*ò¨"G1=¼££¦{iø(~j¦ÞP¤GMMÙäpGy\x0005\x000b\x001bØKö÷\x0012¡»@GNrBé}\x001bóµ^Õ\x0000\x00186É\x0012KÍ\x0011o\x0012\x0005ýPÖçWú\x001bº	2éâý\x000f[\x001b-[hÃÐTã\x001f)0Y\x0006Fæ1«§\x000fÇKmEºº¼\x000f3D/Õß\x000b®ÌÈ\x0014íP\x0019Q	Tú/\x0003=ìll¯#×CFéX¡ÉEjÊÍ´³\x001bì0 ¾\x0000X\x000cø\x0006àq8Zá7ç\x0017.\x000f\x001d¬ìbVkRò\x001c"oVGjê¤zmjØº\x0011Ý92D\x0004Y&</p><p>*Ç\x0012\x001fCãûïºëË?ÿªM¸ÖÊxà\x000ce²2²§\x000eô·	ZáwG!NF4å¢
ä¸¸9o\x0007Ú4$°)	çQ!B±s«B\x001cÕÒF³Û\ÎÍFsåM$)Ý× uYµ¤(ÞÀÁ­uÐeH+v!g\x0017\x0005uY¨5û¦é¯$â¼¯m\x001dW¾Í0ñ=çj­\x0004rÂjä?JÇÝ5 "½\x0015*î«tàfYp\x0015Ý3\Q(H\x0002~-,+`»¬\x000f5àHâHÙFS³á$PÁÇ°àx\x00034ÞütH"¥öU7§T¥'r1í*n´Ñ×
xÉ\x0002{É>|§³\x0007\x0005\x0000(Ö§ÀÖßûÌCÿK=D`1äãa¸[Ù! \x000f	~0øï\x000e\x000e	@ æoS'\¨-(o 7úû.	²Mâ?x²w
½&j®ZQÁP\x0005"Q6Ø\x0018Ñ¨</p><p>A¹\x001fx\x0000y¨zjzäEâ\x0003B\x0005<¬\x0001\x0016=\x0002Á¦¹MqUôX\x000fM÷\x001fîd#ã\x000e=ËxOty\x000cA:c¶¶¥oNègèÒHiYüÅµÂ¼8«§Ëmqm\0x\x000c«üÂ®õMæ'ÈûÏXçÚ\x0004è\x0006ÝñÑÿ&¡Õ¢\x0006rú%]L\x001d+ëË\x001cN\x0010\x0008jã¼WõTókÈEï¯R$§O;»÷\x0015ºPô*í!\x0004ÏÏ1ÞÝ%\x0016</p><p>ïëò\x001a³ñiL90Û¿§\x0006âè*\x000cÁ\x0004lå/æÞÁ8¤H\x0015\×²	\x0013Vô k1\x000f7ö(Õ76Ç66ÉÎ¯ÎÕ HÄ¿X$¿\x001eæ@µ\x0015}àØÇ\x000ew[Jr\x0017ËO</p><p>IU\x0002c\x0003\x0010ïEàT\x001eË\x001b\x000blaYéþî¸Ä\x0000,gléE\x0006Ih\x000bQ\x0011åü»o_ÔÄ2W®ú nË~­¬\x0010³¹­¨ãò_»ú©ißf{òÌe¾PÁ\x0010Ð\x0014\x0016«\x0018lPÆO*\x0018IgàÜ-#+gÔ$j`Ô\x0010EÌ\x000b^\x0011Û¥cGÐz\x0018â\x0012h»g´®lâ\x0010\x000e²Û±Ý²U,\x0018o_~fÆ\x0005\x0012\x0005ÓqÁMü¨K¾Éõè#wyýto½u\x0016ÈP®Þ¼ò&\x0013i1\x000fñ2£âò[üNÐ()5Uà\x0012\x001c¥¼*0'Ó))lÆÆOÎCºUòª\x0019XZ&ä·y¨yYõ\x000b>®¶7¾i\x0002úBqs¿¾ÿÓq¬%¢ÃëÞAì [t%P#áÇ\x0010¾\x0019C~I°ð/l*þ$VSÙÐ!+ÅôÚ(+ûgÝ.x&¹: :Ò¶A\x0007\x0003d\x000fNûP\x0003\x001c´ë\x0011\x00195ù^\x0019BÁagÑk-÷\x000b»VU~ò\ó·Ã¹Mü\x0003Hç\x0012¶ÚÄ²há¹+\x0011ÖÊ\x0017ô/\x0000\x0006éZÙKÆ\x0015e\x0019NË§#|e==\x0007~ÅÓsÙª^+÷XÊÔâ¯ÔjôOÌ§KDZSi7Â²ËÎè{Å
Í)§}0\x0012dZ%â\x0014ø#RS§éV|=hñ?\x0015ÆÙàl#aP£\x0016°æÚñÕ\x0012þtÔ/úiZÆ\x0008\x001eÄq\x0013ÀFÖ \x000e¢7Z½ÄD®ZÄ\x001aró+.3ëH}\x0001ª\x0015TVòaã{\x000f\x0002¥uY7\x0019Öa:ðý;ðù\x0003N4-VÁ®;7lN\x0006Dc\x0006ô</p><p>ñ+:=³{­Üñã¸¤¤óõ\x0008!\x0000Ó»é@dÁªÆÓÃ}åqp(ýM? á=Æ\x000c\x0006:iXæLÜá?ò\x000fL×üÁ5ªPû¸ÞÆ1º/=o/â\x0000Gõ\x0005ð^ù\x0002\x0004¬Ì´\x0007ªÇGè·\x0002 \x0004æþ¢r3\x0018°j?Õz	C­åÙãâKñ\x0000Ì \x000b7¬ÜhG¡"H\x0017Þ:R¶¦\x000eÓxµÓ\x001cT\x0015Bë{V«
5ÛåâE¯-cÙÖyC\x0005â.û'XþÓ]¶åÑÌþQNC¼d\nóÛ7e6Á6·[ü2ÌÇVj)ln	ì	ô¥WC\x001d1\x001c¹¸\x001bJþ{U¹=ç0ê\x001dîô%æw\x0003\x0005qÆ\x000b»¢Äª|·\x0006pän3\x001c^%Óh\x001cWï³\x0010º</p><p>½yÂ\x0004å0\x0004\x0004ØCìcÓì²ìjÐ£åÐÇ-\x0000I¼ü´\x0012â")bõXü£L8ªüf]ôal#\x0000æ?\x001cÖ\x0001Z9\x0000FÀ\x0019ÙÂ\x0005üeýâ:ä÷HU*ÔþÏo¿[Z<UxSï¾ë\x0017è®\x001fQQ\x0013C\x0019=S\x0014ÈqL!DÔ!¤Dåê½\x0002çÿÝù\x0002hg	BÄÍ\x0003õú}o\x0012\x0015\x001a\x001a>Ó"yMIóèR»^$î\x001a\x0015§WË-/ÏÂã~¬\x0008J1zÔ;KòÓÄä\x0018âÝc¬êáç\x00126§\x0013àâ\x000f22LÏoö(Èppã\x0013Ä±¼\x0012©\x0006|\x0001Îx^³5!\x0015òCÓ¼cpN=\x0012w0r\x001eàì(\x0005ª´ª\x0012W\x00160Y)\x000bãê</p><p>­!û`ó![À\x0012×ºÚ°\x0015QÔ¬=B+î{\x0012¸BþütAg\x0006®P¾´Ú?Ë$\L\x000clhzÓ\x0018Æ"jRÕLÓ¨\x0008\x001e0\±\x001cW/ÀÌyúlÊ¥\x001emBx¼Ó	Iñ{
0Õ+gÏp#ñD\x001f\x0007¯\x0012§\x0006Yñ¶ÊµÖ¦.íÄ%\x0019í(ï Ç¥\x0001©zÂ\x001ezÖÇ<¼«Kþç¿êË²
ù"#7Òðä¸Oì\x000b</p><p>\x001e]Xê\x0004*I¸kÀUô]ºCÿOÇkÔA<IªPu}·ÈKe\x0003£õõ
êÚ[7^\x001e'òC­3%'l;ÓÅ¬¿§©S¼®¥ZÅ^³Å\x000f\x001dor¡õµs,\x001b¯ÿ\x001c§E\x00044¾Éÿ¾v\x0017­0Atè´ÆYñÿ-Pà;Ø±p	Ôü^±\x0016Üã²ò\x001eAXÚd»¢8¾SO\x001aÃç\x001cÄ×·ð@¢O\x000b2J¬æµw[1mòíAñÔÍ°X\x0004a^\x001aXÝkA]J\x0012IÕ\x0001ßïõT ÛÝù\x001e\x0005íâ-br±	þ¹\x001a\x0017';Õ|ëøm9_ÇF\x0015\x0015ä\x0013 ø«°£ÖëµYY$p±þ\x000b@XëýjûÀýä`Ü\x0019)=sË«Åx¿ßãÆ71G´É»&äF)¹.-T¼¾ !iê"È¦÷Æ3bx$\öþ\x0005 /òó´ÊrØç\x0011\x001fÛ\x0007ùþi</p><p>xª\x001eÓòæµ êe[úX*e°¾9\x0011-Ç512&¦ÝK±0\x001e</p><p>ÆO%^ÂM­AjÖt{Ù\x0003ý[\x000f¢!\x0010ZÄðM§v'\x0001*ª\x0016X+¤~S¹«v\x0019D\x0013OHOÝkö³[ÇÛ'ª\x0013&;7(D´Ê\x0012sx\x0003}>I\x0019MjÅÖ\x0010Kn\x0013\x001eÉÙ@÷j =¼W\x0015üÌéG²bf×\x001e­áé^yµla²ºG\x000f\x001521¢=2TÂ.ôÍ Þ+ù! >¬LDA_!=C\x0016/
Ë"]\x0006í\x0012\x001c»Ð%z:Æl¸J\x0019ý})\x001f\x000b\x001bFÐfWÑÕ\x001a\x00000+Å!7¤-Dc0ùV£½ö2u,F\x001c°ÿCÒR½ÁcÊûø\x0004Z×æfaìRF\x0005\x0008@\êèw!9\x0011ø\x0008,éïÀXK\x0016Á;û²ð\O!5\x0010\x0011I\x0003<Ê-\x0012¥£ý8É©\x0010ú{õ÷B	\x0012þKµÔ/ÀREv¿£¥Z>d\x0003Y\x0006½µq,\x001dîi§¹ENás	+²j\^âÖup¬u)77Üp©î\x001bSG¿ûÈ´¢P­öå%¥0r-¬\x001bø\x0003"ÿæÛ$Ç(~ÂUYU@\x0002WjtRÈ`öÉ\x0012\x0015TÆ3¢ð@d3\x0000jV9I¨µÁ|0<í\x000bÐ9ñ¿ëÎxÓBÞ\x000c\x000fv¾\x0000²U5Üll!Ó^ÆêEiÈï;¨ë6+?PSJ¤&¢sqÒ\x0010USÄÞ!èùEe4d¥6NbÎ¨,.S(¡";W§!\x0012Á\x0006¨\x000e¢é%\x0019TæøbØ)ÂdJ¶E¸¿\)ò\x00110\x0019æ\x0004\x000cvîCcè_ÿü%×*lCjÞØN\x000bh¢½Z}.¹òèHµÛCQÜì7\x0010S\x0014îüô\x0000¡Å{(ä\x0004ýÝì"£yGe¡ðó.»óhÉ­\x0008\x001cõ3÷µª;6ø\x0013±ûhõ­
£AKÄ\x0014L\²h2KNc3OvÚ3åH$ù#\x0016/r>û\x0008ºi^ÏÃùÖ\x001aí*I­I`\x0011¤t¿Vcû¤BÂ»£\x000e!Âè2K6¹L´+w_n\x0008¿zOÜÛé²©×\x0014ÄúÀ1p¬ÃùKÅø©+T%ºã§\x0019Ñ\x001dM@é<\x001aô8qºã;æº>;M\x0006¨Aióá\x000b ¼ÔÄÑQçPëf{7Ì\x001c\x0014Ñ.¬2×tÔðÛªJW"Î8&\x001d\x0014|}ô0%§Ój"xæót½¨\x000cP÷­À_×\x001fö@Ü\x0007.Ïë¸dË\x001e(Á\x001b{Õ0\x0019àÙR\x0005sh±æîvbÌuj\x000ccï?mÎ¬u¹Õ\x001bãÐÉ\x0010fÖà7O|\x0003]^nø\x0011Ú^§\x000e»§\x000e4lÔ\x001cø×'%Î\x0016\x0014íØz5õª\x0016\x001a	&ò·ßä¦(\x001déÆ1ïx¦>ûêÔ²¦ À\x0004æjU9ÞþXÇc</p><p>\x001bqòyjB\x0004\x001d4&@aJ?\x0008~\x0001t§]\x001a1\x0017ª-¸Ó¹\x001e¡Í\x000f\x0012e/kê «ÝGkÉiéz|@HDmq\x000eÓÂý9kÇ)\x0014üíÓ¬</p><p>®µð@zIøÇ\x001a9½¹}èÙ¶\x001c¿\x001boì\x0016</p><p>°8æ±¼¶eÊÆN\x0000²mÅ|\x0017\x0005þuö\x0011\x001f
¬ñ'Ùgge7$Ï¹ÁØæ71Ö\x0003gO£\x0016\x001dÍ\U\x0016³h</p><p>ä¹\t3w/Ø\x0002°¨\x0008Æe!íC¥gH¢¬ -D{y\x0004d\x0004Á¥$×,TÃ¥\x0004\x0014iY\x000b¡¬se.ôÏ</p><p>\x0002</p><p>E4iWAÖ¸@ª±¿\x0014á)\x001eñ?[rÊNWz¡\x0001å.\x0004Ó³üdnº÷\x0011lÚØÇyÅd¥®ý\x001b«Õ\x0008äîjMG}Ó¬Á\x0012ò\x001acd|\x0001\x000brÈ	Ã	\x0008¯AUÚ K£Nð2´Ë«f	|\x0012ü\x0018\x0012¶­ zrA\x0019½öî¶'->q ÇQ\x001e2\x001bÈÒ¼¾Oý\x0000MÖ]Óv\x000erÏê©ï=ñe/:\x00012¢\x0000­y?À)\x0010Î;Þq¨ØC¿Àÿá^\x001aÏ9dL\x001f</p><p>?\x001fØb\x0002äYïÝ¸ñyuSìÂ\x001cÃBôE]ä\x0011í"®å;&ø6ÕaáPø8p¯t\x000f~	@e\x0017X}ÖéÀJ\x001c(IØ"5+0S\x0018¨ÃW²</p><p>{?3uuü¯r\x0012z%R\x0013»æòvC¤ïÌ¦\x0015R\x001f3MÓ+ôãøoÐYB]e\x001c<\x0014ÂÐK\x0003RÊyö¿\x0000v5O.®_\x0000îIU\x0016_J:r³OÎÓ*õzÞiøS0çÑ/Í§Êt3\x0000cÐdSÅE\x0004SÜõ£â³è¶K!CóMY\x0007n©#ã#yò¦È\x0000¿\x001c:>i0é$ßíC­Þ\x0004L´1²ÿÐü¼Dû Os2\x00053ÐC ÜþÃwÿT\x0016ÒW²ÜÊM¦éçP_ \x0015wùòvOÏp³çó/k\x001få\x0003 ü´Ã¿ 0ñ©EÍ¯Ù÷JWIÃïOF]h½ºëËþ¨¶Ë¯Àá£ÉÐ¨Â ÷§O
P-\x001b	¤uK\x001e\x000bÇ±{\x0003\x0017xÇUd7! ZüíÛ¢:[m´2ûµ¾TD\x000b\x0001G\x0010\x0006ÝuÛ|\x0002JÓ]êÿ\x001e\x0003ºâ´ë`tùf09ëÈs­£®ôks£¢Gád?ºX\x0003¾\x0010"µ¯ª\^ÛQaª\x0004\x001c?H£½ý±ûaÇ vÒ</p><p>B»Ò\x001evÅ;H¼\x0013\x001cv\x0000{6\x0002¡\x0006ëTôYk¯&$Õ~ËÑnuéÍóXÌk?ûF:B³u\x0005ÑµÔ~RÏTÂ\x00017\x0002èß¹aõùòq\x001d³þåA\x0008\x001fBéëbÕ®\x0004ßðÙx©µÑ¥ì	3¶Ì\x000e±Í~Å]_¿¨5´6eêU\x000c}^íÀ¯Ïí</p><p>ÏßP¦pÓ¼pÿ-Í"ìë\x0003Û Ïjü³
Ä[¹Aæü\x001büâs5~\x000e
îÊ#çñÝV«^ÄvcÑau	H{ÒÅ6Óê»Hâ\x0000»\x0014ùóh¦ÆñøÂé\x000ekht¶\x0016ÝðØ8±\x0018Åì8ð®\x000cÛÙ¹,\x0013>Ìà\x0015Gea\x0010]?Ô2çµ\x0017¨âÜË&xTõ¤8Ù@,·Ìn6´Y «+\x0008\x0008f\x0006í»`Æ[N\x0007½ø\x0018ëE-\x0004¿¬\x000e8û: Õ\x0003 £iáÅ"Îo\x000c´u¶Súàì±é#m\x0006 ïb£¦)ÃÊ$`\x000e@\x0002\x0010¯ì#\x0001^fZTï\x0005ò·/Ëå9r?\x0001Y:ËRø+«ûpE\x001fÂ²ç\x0003ÃíÁ"3ú\x00181\x0011DÒUX®\x0000
\x0011á\x0001E[#º@b÷·ß5T¶<Èpª8PÿBfTµ5KÐ«Ò]µÝ\x0012>èÎCYXêyfJ¿a,ý íeÁþI\x000e\x000fÙ	\x0003\x0005u\x000c÷:KÇ\x0008\x000f}ðC\x0019*5yp.K{X"ïë}cº¬ôv¡Ö\x000c\x0011m\x001c3Ñ¶ü¯òS\x0017\x0015\x0001Ú§T\x00149JÈ$,&õ\x0019°Ïú\x0005Ø\x0016K\x001a¡gféwn?æ¤PisÙ	[pQi²äbUÀHö 	`?U</p><p>IL&Èß\x0003~Û\x0010ZÚ\x0017Úx(c@SDe\x001cÒ<æØACTäF­\x001e\x0011þpQûZx¨Üú£ÿ8\x0012:\x001bà2ö=ìRß³äVÏVe¦\x0005</p><p>\x0018¥¼â5lZð¼>Cz'â k@²zå!u±ôÎÜé¨7\x0005vÚL)	M,hä·§ñ(G<Ù¢Qs§éÀå\x0016<[a\x0000Ç/V(RÈÀKQ8kÞW\x0000C\Á0a1\x0004I®f=3¼z¼ÿ\x0012Ô|\x0002=nÓ­eÕðÊÃ\x0000\x0018#±OU\Ü_®(sõ8\mâÛnê\x0015îØÍ\x0017 º®ßU\x0015\x0017K·Ô¢+\x00172@êY©ýÝÍ\x0000Ò\x001bóÎ(ûî	gæYÔí%{jéqÍÇL \x0000ÿ6ùECbÑÆûzó­~ëþ¹Ã\x000cç\x0019®ÍÚ0b\x001aCéómÁjÕÃÇmÔº·\x0013p*\x0000úÄôeòÌ±>\x000cè\x000b°â »ð#ùc|\x0005Ú¬ü±âáCõY±;#%=9qªë\x0008\x0015My«EAÿ»éCÃ¦Í=T\x001eTåx+b=¨Zh</p><p>A³S==Íxÿp¦]°gX¹@µ@¿É\x001b×:¢ß¿ÄÑS÷­ê\x001dn¦âOK¨ywdüa\x0016	ê\x0016\x000f}\x0000<0fÜÛ[Áoð(\x0000õÏÄÈwê~C>]ûÝ[¯Õÿmfþ\x0015ààÃÌt\x0010 ¤èJ¬höº"8:Së»I½¹ÿ
\x000f®9©8UWðr1<¤(âRÑÇ\x001em6BF9<\x0004aá1Ç¯°¾fiæ)Ø?\x0006õ0@ªMe]Þ.ÇHðïxm#ruåþ¹~dü¾·ÆY~Ön\¥p/©"~:\x0015¨Þ²Ø\x0011mBÑï´,s¢-t/)Ï»ä¿=àýìuJé\x000e¦µß3CE\x001d\x0017ÒgA µO\x00102U´9ãqÝs/ècÕ+8º¼Ã µõÚößÇ®åFß\x000bx©Ò´@ÙIh\x0007àÑÇÉAP\x0001KÎ´å\x000f3Z6,Â1Ni\x0007\x0000CÙv©XéO¸ÄcËðí\x0018ÂpëÂß<õ¼¿½¦\x001dú¤¤
è\x000eBûÆ/Ýå#B¥M°¶C
¡|êCª\x00023ý\x0007HÃ$ÓRG-ël-#§I$ìCkÜ¼#óg%·¯\x0017û$Õc;yÌ[&÷\x0012<ö{µÃX\x001d
rÔU\x0015ã\x001a?Ò¢¶¥´<ßÊX>Óæ2\x0005i\x0001}Å<\x0002*ÁRPÿç,#¯ªèµ\x0002Á4«¬+.@N\x0018J\x0002àºÔé®E\x0018ÖÒ\x001eéçþ¢=Ö5á	äí;ýßÁå9\x0005®ï=\x001féef\x0002!\x001c=ô ß¸lWU\x0010\x0010ïn¸[Þ\x000b¿eçÌãxíYÎs\x0004ü41âã:d8&(û©f/}¨ ¿9«¥C"Ì1©vX¾{i,b\x0013W¼ø0º¥¾ òÍþ%ß\x000cÃØ¿J(ù¤9W)`.\x001dk	jü}@ÇP'ü¼¨\x001b+9÷\x0014¼æP¿ÞG\x0010ÿ¾Êj®Z|\x0006+¬ëí¬\x0007\x0015GìF~\x0014ÌÀ\x0015[ò<ïÐpAön#ÜÀá\x0016gSL²ú\x0005\x0018©VKîÜ.eÞ_÷Æ?Ñõ\x0014Q&DMðv`cÿ\x0002@ù\x001fß3\x0015C|\x0001ÈG]®Ç/s«;t3Nª\x0005"¢Í:\x0010òÖßo\x0019¢\x001fÿö¤yûý8þ¤NÞÿììý·Ø\x0014ÚÀ1\x0006f\x001cø-mTª
î1¸ü\x000b\x0000ÿôÓûsL÷¿I$þrWêùÈûoi\x0010vS1®¬\x0004¸I[ôåî_5åÓ6B1ïÏ«ÒÜqtXýÕ=\x0013AÑPBèçEãHY+·6ö\x000fù×âØ\x0017ºÎ\x0006gôlº``?Ñäÿ</p><p>üF\x0003¹Í\x001c¨\x000co\x000bÙÛ©\x0011ÞÝ¡8çjgùT¤A\x001aàë\x0017ç\x0019Ág'ù\x0010
j+û0úG\x000bÃ4Y\x0001<?`dIEö ÀgÌ\x001eqÄqL\x001eE7ìdPïRaÙL¹\x001f^¥4ë\x001býÑÏ-ãþ k\x0002=>\x001b+9\x0019^i79\©Ú½¿2?*4
NOÄ|:~¹qh³¾Ø\x0010d\x0019-Î?Z©m§^\ÿ\x0000©Ø÷Âð*´óÍq!yäy[\x001bC;\x0012p;d×±ø~(NdÑ"ð#\x0016\x0019äëùÓ\x0011å7\x001aeÕ¸Äñ2×"+Ç¨nÁâ;¡ËÅì¼¾ÝGoCì76P\)YbV\x0004w®#Ä~\x00161#ÍhÇ²gÂì2¥§mçÛ_~ñ>Yc<$d`ç#ÝÇ¸¨î<!n	2\x0017\x001eßþºÎÐ5\x0003TOâ\x0000¤ÿ\x0000~2rGõ\x001eùõ5ëÐ¼7VñÏ\x0003¬J¡ÑáéNÂ<kAlªË\x0005Üm¹&W ý?\x000fÖ¦Òu\x000b/¶¬:Ä.°ÉòJÑ¹Q\x0019'ýjÇÔc\x001dÇ¥zV¥£ÚÞÆUã\x0001½q^oâ-\x0016M9Ø°Ü |Þ¥_f3¯»ðF%Ï\x000c·B?ùæ¯ý\x000ejêøOEH\x001b[ùpOÚ\x0018\x0011úÔ>\x0005Ô¡áÄI\x000eé¬ßÈbO%z©ü¸ü+¡lç¹§d\x0007\x0015®é\x0016:|\x0002[\x001bib;Â±i·>ºl¹\x0003\x0015­â5i4ù\x0001»»pG5ÏiÒr\x0008®jÈë Î¦ÞB1Ï\x0015}[p\x0018èk*Ûk(­\x0018{Á\x001aHãüafm5KmN1ò¸\x0011¿Õy\x001fãð­Ô`d$t'#ñ«zÎ5=.kSÃ°Ê\x001fF\x001cý+#Lw:}«H0þJîÏ®+¶®¬rUVw4ãlJ
Y~¹ª üÀÕÐI\x0018\x0007ZØÄ­2X\x000e9§¸N\x0003\x000fÊºOâ|S\x0002\x0001Ì?:vÏzK}ß¼N½ñUrÃø\x0000[+Å58Àüê%Ü{ÎÔó@\x0007>ÔRóÚ\x0000´\x0010\x001d09\x0018ÁÆ)ÞX ä9\x0000u\x0018üºÓÌHyÇ\x0007Þà*\x000c\x000cüÛÎEdXÄ\G9ÏøÒ*²v\x000exÚHÏéSªá\x0015q»\x001dK6iJsòwãû\x001ab Ù\x0008</p><p>\x000eG\x0000ñÿ\x0000 Ñ°\x0018ÝÎìäçõ\x001fÒ§*Ý	$\x0011OZ\x0014\x0012:¶\x0007|Ð\x0004IËóñì½¸©\x0011SvF0¼¸þà\x000ez6sìsO\x001c\x0013sØÐ2!\x0012®Ð\x00161Ï¨#òÅ;ìÁmÇ+à\x0003R3.y~{sÖ9^7~\x0008@ªù\x0007\x000czü\x001a6ò0\x0006\x0008ç'#òÍM´g¹÷&§x=Í\x0000Ba,\x0007Ìp=1þ5)\x0012ñóg\x001ccõ§`|ß¥/=:þ\x0014\x0000Å.ÜuÏ\x001csR\x0011.Ñ´g'À¦³²+;îÚ9ÂzO¿¶Ô­~ÑnÎSqB\x001e2¬¤u\x0004\x001e\\x000b</p><p>\x0018ã ñÞ´\x0001_§j7`v?\x0003Ó­0+\@0}0\x001dX)¯,ñ|ò^xXU\x001d°'\x001dûô÷&½^GPû\x0018©?{nFH¯)ðäÚ^3G\çaëÔÿ\x0000%`¹gÄ\x001a\x001fØ4+\x0019SväûÄ©\x001fxWOà\x001dCÏÒ\x0016ÂB\x0003G¹à$ýäÏÌ¿Ucù0­MnÃíÖ\x0012ÂSï\x000e9è{Wé3h÷þ[·¶PÊíÈA\x0018ÿ\x0000²A*Þ úM=u\x0003ÖÆwcr*´Ñü¤0-Éä{ÿ\x0000Z]>ýoítR	Y#'&7î§qÜ\x0010EX;!'\x0003\x0000õäPÁ\x001egâÍ\x000cÛKçF>Wê:`úý*ïÃý|ÛÉýxÛcwýÉ'î9þ\x0013ìÇ§¹÷®î\x001b9á?Ýæ\³awo8ç\x0004ûã½yÎ§c.¨îòÄ¨8ee!e^ãÛÿ\x0000ÔE(°höR	\x001dë\x000fÄV)s¦\+ÄlAÆy\x00035GÃ~)µ¹·X/.`£ËN\x001aOUsýñÿ\x0000u\x001exË[·±Òg·Yãk»Ê*£d¨<glÓhW0~\x0017È~Ñ¨Dßuã÷\x0005¿Æ»»·xá-\x001f </p><p>ÂX·oÃ­q_\x000e-e\x001b\x0016D\x0000OL\x0000{zf»ì~ò\x00100\x000f\x0003æÊÑù±mþøÁùx9\x0015ÁÚ\x0013\x001bìn</p><p>µÖøê¥£:c0B>|*g9ÏWìFzW/p\x0002ê\x0001p\x0001qOëXÕZ\x001bÑvfåÁQZðJN\x0008ïX\x0016asøV½³\x001e@\x0019®]ÔÕÍ5|MÂÎi\x001cÊ¬¬ºå*b\x0013*U%H*p~­iÎÌÂp¹VãAw\x0004Ùj÷1`ã\x000c¨Ãù\x0003Q.©¢O\x0010Ë»ýVµãy\x0006âÒ\x0002	È,@À¤/q³&D^y\x0001wdcð5×sÆtz\x001dÀ\x001f¿×¯\ôÊ¤j?ô\x0013S®\x0008@[Q¿sýï5W?Ö´¾Y;q\x000eO¯ÓÚ\x001f\x0014 \x001c£úQqX­\x001e\x000f8º¾<u3ü,^Ãk+õ\x00120'ñ«ÊUk}Tb¾`\x0008o¡\x0002\x0018Sh\x0008_÷:¥ü#Ór·ó_ëP¿ä#kPÏ®Äoè+¡Þ»	\x000e[§­5âÜÛ|ÒTõÎ
'pG04
@®½sÙ·¢ºF7ÉÇ½\x0014j3/jt\x000bÓëH</p><p>Ç^ÜÓ\x0004\x00100~´»HíÏµ\x0000\x001bÈá?R)Tè?AC\x0002O R\x0006ÚNS8ú@Az\x0012KgXÑãaó\x0007mªy©£\x000eÊ¼\x000c²8§¥y`ÿ\x0000\x000e)ÛT\x0003è:Pj(7î\x0007Ú\x0007RE*ª\x0011</p><p>p\x0003\x0018ÚqLCr¤1íO\x0019ÏJf1'</p><p>¸õ¦ÞHd2íÝ³98õ>\x0000JX}\x001eµ\x001eò¸b¥S|Ó.$¸T&(Ãc¹p¡qëÔ*ùS©EåA\x0003\x0019â\x0018f\x0019á[èA Oç\x0007ZöÞAÿ\x0000\x001e¸!±çm\x0007\x00074ø!åie]§Ç>Ù\x0003õ¥}Gbràr¡»ò:TV°µ´r*Í#ïrÃ8'Ò¬ykrÃ\x0003\x001dx¥ã×õ§a\x0000¶òF}}i\x000cÈCÉ×écÆ\x001cåN=±RycËÚ\x0018qßhj\x0000­vá]\x0018ã-\x0019\x001d\x001aóo\x0002\x0011\x0017ãº\x0007Ô\x000fþµzdà0eV*W\x001càãÇò¯+»\x0013èþ,3F¹xæóT\x0001÷½Gâ3BÜ\x000fXqAïúW\x0011âÝ\x0019ûlqÆ$^¹\x0015ÙYbx\x0012çí\x001bãC \x0018Æ\x000f#¥-Í²Î¬AR0F(a±ç¾\x0014ÖäÓï<·>\x0017\x0018êfs·Ý×¾£+ÜW¥+$Ñ\x0006FGE\x000c§\x0004d\x0011^Yâ]"]:çÎñ±·£\x000e\x0008ÁÏé]GÃíY¯l'³{fÜ«þÃ\x001eØ6\x0002)Þácrâ\x0006Iã\x0013¦ü)Uazý?ýUGVÓ"½´dºüÎJÆáéÓÿ\x0000¯[*Î&\x000b·x|ê8\x0003ßÐÔ	Àù?Ò¦Ã¹ä·zMÖtÒDÆ.Ä¹\x001bëÛ\x0015\x0016¡Üê\x0017cpÈ',Qvõ£c\x001bÇ²tY\x0007«\x001fþµ>\x000bX \x001f¹WýÓOQhRÒ´å°³HP\x00058\x0019ã<zU£k</p><p>ä¢l\x0001¿©\x0002¦E6F*2[°¦ãwå@\x0014o-ØÛºÄí\x0019a \x0003\x0007Ö¹
^ßÈÔ\x0010ñóÆ\x000b`c$q]Î\x001dNîÝ2½*;=*\x000bKÛØÄÌ3å+\x000fR;þ5\x00126Æ\º=ÍÚ\x000cE»·\x000bùÿ\x0000t¶ú+ªþöt\x001eÊ¹þu¤\x0000;\x0001À\x001d*Q#B+qÊ¼ÅhôÛdã\x000eßVÇò©
¹\x0018ØGÑN\x000e)rsZrG±;îS6\x001b\x0002¹Gb9üê9\x0010\x001e\x001d9\x001d8Æ?:ÑÍ!;\x0008ÏÖ\x0005ÌÔ\x0001rw<ÏN*¹PÇ\x001b\x00030\x001dTíÏãÚ´äÀÚ\x0014Ô\x000c\x0018Á=?Î)4\x0017\x0005Mª\x0007O\Òð1ÏÐô¤VÀÃuöæäg%OÓ\x0000q\x001c\x0007\x00189¥Ê23¾ãÈ^½ù¦(\x0003'<îâ,äz*\x001dÌß4S\x0011Åÿ\x0000Âm¤í8äàt\x0011/øÔÑxÃJX.K\x001eÛ\x0014cõ¯;³¶ð@8==Mn[XyXÜUA\x001dIçéXÊV)#­\x001e+°-òÙ\ø\x0002ëHþ(²LfÖç\x0007¯Ý\x001fÖ¹Ï³\x0000\x0008R8ôª×@å¤ðI©U\x001b*ÇTÞ-²VÂZNã©ÎÑýiÆ\x0016{°7,sÎJë\Ya4þ61ÈP:±£Ç]ÿ\x0000	}¡\	É=\x0002ºümh$	ýzÎ{o\x0019Írfä7¦å\x0019\x0006Ò\x0000\x0000\x001fÒçÿ\x0000¦à\x0016A8ëÍ/i"NÒO\x0012åHÉ\x00146îOÐv¬Û[øâ×%½=÷/ÇÎ\x0001H\x0003 _P\x0007r}k*kÃ¹­ÑBîPç#§S¨U¤#2d&7Ç#<c¯½f§S¸îtcÅF7y\x001eÉ¥n3\x0004ÈÏLcÜÓí<ngR#Ñäeì<áÏ°â¹ç·[Õ»ã\x001d@Û953É\x001b\x0013\x0002n@F6¢äúgÐÕ{Vk?\x0013ÍÚÚ\È \x001dÊÓ\x000fð¤O\x001fE½Ul\x001dTñ0Àý+\x000fÌhàeEÞ\x0014m\x001989î\x000f®9¬»¸|ÙÃÄ£À\x000c\x0001ùUÆ¥Àîäñt±Í\x000cÊ\\x0006\x001c}qõ¨dñ» BtðÁÁ92r¾â¹K{©§Mà#ô\x000cç>?\x00068Ñ÷rw\x000eT·^isIhÀéá<}åF\x001eyÿ\x0000Ö©Ç\x0012lÜúh\x0000ð\x0000õé\b 7\x000eìC\x0003Î:óO\x0017\x0011Ë(.£\x001fZ´ÛcLì\x0014\x000c
5²G?¾\x001fá\Þ¹~u;Ä»·ìÒFr¤>[#¡üë:f6ì¾g\x001bÏ\x001fJz0ÎqéV=\x000eJñOdþ\\x0005Ó\x0018ø0HOÌWþ±çýHô­!ãÛM6r	\x001cuà×\x00107Át·Vò¼3¡ÈxÛ\x0007ó§Í{\x001cÈLö(f#ýd\x000fåîS\x0004~X\x0015OQltZ·ôýJÜÆl.\x0015Éà³¯\x001fäW?ámXhÚÉ¹h^XÌO\x001b `	î?¬ß6ëÌ_-H#)ÐÅåXåSK`=\x0004xöÓ\x001bNºSÓåOó¥O\x001fÙ6L7j3Æ\x0019\x000e~¾õÀMjZ@o6#îX]\x0012OvAÅ9> é­÷­.Ôôè§ú×äçDûÍõ¦\x0016G¥\x001fhäað\x001fúâ?øªpñ¾p	º_ûwÿ\x0000ë×úðzñÍH\x0007z\x0000ôÛ/\x0013éúôvvBé¤¡1m</p><p>1IÏ\x0018®\x0017GR\x0013øF+Ï|\x0003d\x000cwú\x0004´AaOø\x0017/ú\x0005®çL\®þIl¯åW\x001eä¾Åäþ:ÖmÆ§ad\x000fÚnâR\x0000ùsúV%÷m!%--&¸#»6Åþ¦\x0011ÖÒábñ>¿~Ð´ût_]¬ß© U/§S´Å\x0018ÿ\x0000d ÿ\x0000\x001a\x0002çgÎj)î ·\x001f½\x0013ýæ\x0002¸ÆÓ<Upqq|Ê§®%Àü\x0015,\x001e\x000fRwÝÌÎÞ«LW7dñ\x000e\x0013áïc.N\x0002¡ÜJIuF·¸¸Û6ËuÝ 	ÎÞäsÈ®wPðèÓ@º·%âÈ\x000c\x001bø=ýÅQÖ®¦µÒ¼µpÞ^\x0017´\x000cÊ-.	»ØÛ>1ÑÀäÝòx\x001eOÿ\x0000^þ3Ò\x0001\x0000­Ø>¾Pÿ\x0000\x001aàÎ</p><p>ÒHSnçb\x0017$çÓÃr£¸\x001e8ÒÝCG
é\x0007^yúÔw\x001e9°7"Öì3(þµÁ§Ík\x0019ÏaÒ¢Ô%\x0002Ïowaùu¦¸¬;añ\x001fM\x0003þ<oò\x001føÑ^dM\x0015v$éá%\x00171ðäí_öG·½YX~`9\x001dÚ%\x0012Ç\x0013¯\x001b³ÁõÏÿ\x0000ª§d$\x0005Ç×5Ã&îh1ón]ÞàÖV·pð^Gäìm©¹zÖÂmï\õÁSBIFr:ÿ\x0000\x0008éúV´É.Ç¨»¡Ù\x000eÕ\x001d\x000brMFó±\x001dÉ`	\x0005OAøQóÈ¸à\x0000qÀàS|¶U\x0007ràdÜ§kq\x0016EÈ]ÈPv#­I\x001cÞd®ÀÛíÞ¢´D\x0016\x001dNz</p><p>XGBfG$í=øÑd\x0006ÊJ7Þ$É98\x001d\x0005Aæ¬K mÉ¼\x000bdúê6,\x001c\x0003\x0019;N8?Ö£º\x0012:áT.OÊ\x000fn*\x0014uÔ\x000bP1eó·¸bÄ
½;Õ¥ùl\x0014\x0010IcÉú~Uc$LgwÊNâO­^JFsÎN>£f\x0005ò\x0008¼¸ðÀÙ?äÓ"\x000f\x001d¹\x00042\x000cwì}j;xÌM¶Wl®\x0008\x0018ïëøTS\ÁiC»g¦z~4%Ñ
j0]<RK28=\x000f­j\x000bky*±Þ\x0010\x001c9\x0019ç¨ÅsÒ\yAHÔáqWti</p><p>$mÄ|»°¸ÿ\x0000\x001a©ÃKÄw¢[i\x0015ÆÆ\x0007æõ\x0014Ë7\x0007i_vÜÕí\+qÐäîÏùéYXÜFáÀýjàï\x001b6i^i\x000crÄþ\x0003ØU9È¶±ÿ\x0000Vç×ÐûTe\x0014£9\x0000(éùÕËí#ÆÆ9\x0014\x000e\x000ei\x0011C\x001e{óV¢S¨iàn"à1þ1èjr\x0010@Í2\x000ci\x0003$Ô1'9ã#¥5L¹\x0004íKÉÆh\x00187µ3\x001c\x001aSÔ£¡Áê(\x00023èE$|úÓºDá\x001d(\x0001BõÅH\x000e1ô¤\x0003å4á÷G<R\x0011Ù|>Ô|u;it[\x0016p	Ç?tË\x001f;WñLR\x001buhã8\x0001TáTzûþ5¢Êh\x001a¨7;K\x001aqé?©¬ÂLLd#q^\x0000=*ÓÐ¹ÓÚè×w¥\x0007Ø\x0004÷­í+Â\x0011${×2\x0011ü=ªM\x0013RK}2ÒGä<c5·o¬YKÇ\x0007±¡\x0008³\x0014\x0011Fc@ª\x000608©UzqK\x001cJ¹F\x0004{\x001a~ÕÎj®\x0016\x001a»»âóÅ)éÅ R:Ó\x0001FFÉ"F\x00042ú^uâÛsk5½»\x0012Æ=ÛIþ$ÀÁúö5é
Ò¹_\x001bX\x001b­1n¢LÉhIoxÏ_Èàþu2ÚÃ[ÜóöaòçZf\x001eA9ú~\x0014®Ã\x0000Ôs!'+Þ±[½Ú7Èq\x0019\x001cqTµY\x0001¸\x0011?SVmØ\x0011·n+)É#;uc´\x0013\x0014Q¥\x0015D\x001d\x00042¹N\x0003`\x0001éS\x0007\x0001@'+>ÌKq4p[Äï,µ\x0011z]l>\x000c\x000fg'öÑ\x0012º¢\x0016á\x000f×ø¿JäP¹¥Î\x001fRÕ³[Ù\x0010\x0017£8ê}c\x0016Ú¹\x001fwÑø"\x001b\x000b_2å~Ø{²±À\x001eËéùÖ't8¡¶{Dòö²\x000fºGCôÿ\x0000õÖÉ¤ùHz19 \x0015ÇN)vr	>ô¬årSO\x0018Ï­7\x00104!/Ã}à:j±\x001c1¢åPç±Æ\x000fáUàÆ«P@ÈúG¾$\x0000cïÈÏ"³i¶\x0005Øc,\x0007ÈWæù9©Z\x0011#\x0012È>\\x0006û§8Îj\x001by]l÷Fd,ë÷çi©CË&Kªüª ³¦W9\x001d~ÜÖn÷\x0019_ËÛ)Ú6ÁÉÏ Tó1ùqÆãÖ¨Ú\x0017mÁd¸8À\x0000ö¦FN\x001c\x0007vv9 \x001f½ïíO]Ø\x000fÝåÄ\x000b\x000c¶9\x0000ò	íúVMá+3&H\x001c\x00123ÔÖã2ì\x0000ü¸ g\x001d\x0007qüë\x001bSUûQÚpqøURÜ¨nS,»°T\x0011ëtlËÆqÁæ¢Ç\x0000þx§)ÇqÞº\x001a.ýÍIÕ'²´1x0ã\x0018\x0002¡ ß3ÛÏJ2êª\x000bs)îÙV °öÏ\x0015	XÆ[ÌÅ<\x000e¸ªù«1Ú\L»¡F\x00078Àëô¨</p><p>àà\x0008ã\x0007­4"þ)·pÎ;f©Eö{÷\x0003\x001b[\x000c1ïÍ%É\x0011njùq\x001b`\x0003o\x001e¨¹H¬[$6ÚMÙÁéjØÒ¨ïé@\x000fÇ\x0000æ¦·¶ém¡R«¹.p=j\x0012Ù\x0018©¡KxÊã2	RA PÆV#æ\x0018¥æ,}ép\x000e1K\x000e\x0007ÇéB\x0001@\x001cÒg()Ü\x0013ÇOzP¿)8äP\x0005:ôÚHÉ&ZÞAµÓ=}þ¼Vµå¤PJ¯÷f\x0003\x001eþ°6d`Ô±^]Ç\x0017\x001dÄ<cfr)¦&®w\x0017[k-mç\x0003\x0013´k×¸\x001f­tQhc\x0018AZà|\x001eâK&<È¢d'Õx?¡Ïá]íË\x0004;grv\x0002}*âK,Ìyp'ÍØ</p><p>r½ñä"îjÔ\x0006&PË}jl\x0003Ò¨¬sL§\x0012(ü*ÂK»­;`&ËQÍ\x0000)9Ze*Ê\x0008#\x0004\x001eTpqG\x000c3@Ï\x001e×,³u«@\x0008HØóÝ\x000f+þ\x001fPYÀE\x0003sð\x0007Ö½\x0017Ç:)¼ÓÖþÝs=¢À\x000c¸úÏç^q1Ì\x0005½Ö±jÌÖ÷D7\x0008ÐØ:°*è6\x000fCVf\x000e\x0000\x0000}+Fs?\x001cb½y=jæ¥<L.n£ùº¢\x0013{wö¦/R(´ Ñ)õbr>dþïµ\x0015µì~¼*yXô\x001d'L°Ó-UaDÀÃK»,ÿ\x0000SßéV¡¼âIc?6ÃTpE@m"\x000bò \x0000\x000c,\x0018\x001cTÑC\x00140mp9lHîz×*çþµ\x001d·!\x001b@#¶=k×ìÕ#»R£-ØÚz~9®\x0014m¸*IÎ;þ½q_\x0010¯ÖÞ×ì6Ò\x0003-À\x0001\x001cN¤ôÏ\x0003ó­íÌ1_¾3VUY£\x0005C\x000c\x001c\x0012;ÔR\x0003¼|ÇÒ¡°£p\x0007¡Ry5³\x0011>D1\x0012=½êKXãGL÷9äUS\x0014Î¤Û\x0006¤\x0003É*Ê~ïëRÖnZ[\x0008®\x0000\x001c`ãwÔÕÈ<[\x0008VÁ<\x00039à_¥b.¢_åB\x0013#\x0018­(î</p><p> À\x0018 pF1þ5Í(µ¸ÑCTr=¶\x0011°xluÇ|zÕ[m@¢í*\x0006\x0017\x001b¥K{\x0004ÍpÄ+\x0012Ç\x0003>A¡';\x001b~òÖÐI«\x0012i. ìû¢\x0018b0>×"\º\x001er}*Rñe\x001bñÚÌ7.ýÄ à{úÓPì;¼\x0010FTÉ÷ß¨\x001dB\x0012Ü¿\x0012\x0019êHéô¨Ø±9$àtÿ\x0000ëÓ\x0014sÏaÔö«+Yb§\x0018\x0008\x0000ã½[Ñ-Òîä´ÅLQ\x0000Ì	ûÞUJ\x000c
£ñ\x0019«VÑÉ|¨]\x0001ëÇ·jRVDõ7^xÝöÂë¼dáOÝÈçéPÞiâö4,\x0007\x0017\x001b×úgÖ[(,%V\x0019r:\x0015\x0005XmfÝ\x000f\x0012\x0000êab\x000fâ\x000fô¬Ô_CD´ÔÇN¹¶É"¨:+U\x0006%Ç\x0015ÙÏåÌ2®¬\x0000\x000c@þ%=Åq÷0ÉkpðÊ¥\x001d\x001b\x0004\x001fÒ©;(ØãsqN'\x0007>µ\x001a¶ç ¶\x0006\x0008$ô\x0015§.¹w!`V\x0016\x000f\x0008·D\x000eå\x0000ôëUv"ÛqDb\x0014d2\x0000õ>.ÃäE$¿êðBÐài[Sº(­"Eåí\x0004àqWtá-»ÛÌú[^£+lI#fBAçø\x0003ð©cCµ{«Å´æÑ#\x001bJ$ó>RGqÁçÿ\x0000FÔ4ØÄ×û#¾WF\x000c3\x001fcùSDÆán</p><p>N`Efx làuã=\x0007\x0002ª¹Þ\x0001\x0014HÑ+eT¶@÷ýM\x0008\x0006\x0017ÉäS²ÛI¡\x0011¤u\x0008Äð\x0000\x0019ÍM,\x0013ÚNÐ\ÄðÈ\x0000%$R\x0008\x0007§\x0015@DNáÇ¥5@\x001dÍ=ºg\x001cûS\x0005\x0000^Ò.ÿ\x0000³õK{¼ñ\x001båÇª\x000fèkÔnV[£0aäw¯#\x0018Ýþ5è~\x0008×cþÎû\x001dÓs\x0001Ú\x001býßáøUEÑ¤y\x0001ÜûÔ´Ô\x0019\x0012!\x0007½^á0ñe=Ç4¥"^p3Z\x0010=_pÈ¦»ê@¨MÔ*qæ\x000cúQæZIË0'Þ{Çñ</p><p>Ý/UaVU-_¨h6u\x0011­\x0017\x0011\x0002^\x00068 þUæ^+ÐæÓµ\x0013\x001d²fÚé[ãø}Túc?zºÆ8\x0000~\x0015ã\x0008\x0016o\x000fÌà|Ð²È\x0008ê9Áý\x000f52Ø¤ìyöb¶è¯y\x0000\x0019nB@\x0008ýjá\x0005r\x0002¤ç§ó¨­¾Øíìõc+V\x000bUë!ó\x001bÓøk\x001b6Ê2g(®c`£\x0018\x001eØ¢«è¡)"áþëçõ¥òF#3\x0004?+¡ÁÏ¸úW7o|!bvÂ\x0001À<)ö\x0015FëÆ")g\x0006Gh,BîõÇRzzV1jEXìn¦Ö#5Äâ1²\x0010\x0000ÿ\x0000>æ>$\x000b¬\\_Zî\x001bÈHê£cõÅ\x00177jNÓ9Qå er\x0018\x0012y\x0004ó»?çÔ%n,
ä|HªÊàp\x00187}zU»¥qòÏåÄÁN\õnõP\x0002¬AëëZº²Og>@\x001b$ädwôªóÄ¦øÎG¨ì}+Dô¹\x0004²\x0011<</p><p>Ã¸üVéòç\x0018Å:Ê\\x0013\x0003ôcòCK±Eæ\x001c=©l\x0005ëXcâ\x000f\x0018ÜÃ#×ëZ\x00025§o	vÎvÖq	ãgRÛ\x0008=:¶°	¤r¤\x0007\x0000\x0001\x0007\x001dÇåXM6\x0006+
¢#\x0018t\Ô\x0011JÍÔ,>Ò¦[xÈ;^<ð{\x000c\x001aÞâ3\x000b,ÀI#ð\x001dG_ð§Éq²Dw&=ªIÛ2*#Í\x00163;¼Ã
L#Ú\x0006Täô÷®ßÂ\x001e\x0019ïQK¸¨¹×;)úúWc©xvÖöÅl¡\x000b+pÙf\x0015
ô^09ïÍu6+\x001ecáÝ\x000bûVS<ÒyvÈáI\x0003%ÏR\x0007°\x001dMfÝC\x001d¾©s</p><p>!1Å+¦ß`ÇúW­Ûh\x0016úm¢Ãcp¤"à,\y9õ5Ç^ø\x001bX½¾º¹B$ÌøP	Éí¿g\x0019IÉ§·@±Æª£HÉ¸GqÀ«ú\x001ciçÏ#\x0013¢$\x001f|Q¬h:z »¶egå\r¬=CU½)\x0012Î	¡¹&E|Á\x000fÝôÁ­$ô\x001cQ¡1YZ0\x0017\x0008P×æ\x000bü°?\x001a©we=Æ^ÌÏ¹x \x001c öì\x0007õ¥Ã\x00046÷	 Lr®B±\ä6\x000fR;j¼Ò2Û
\x001b»>Ðc$ãóÁ\x0007Ú¢RåW5,ØÙM\x001aF.0Ì\x0010\x0006\x0001ü+\x0013ÄlÏ&Â=H\x001d3Z){\x0015¼\x001fÎÔá¶üª*äæÞò4\x0017vÖå\x0014|Là\x001föºÍNIÞA%súXídµL\x0008;\x0000õÇ'ßµT\x0011ã<ãúWE«¥Y6,â, "\x00101·=:V8´Ì BC¦\x0000ãÜVÑjæMXX,]®Q\x001c\x0011þ`î\x000e6úñÍi®£s¦Ç\x001aÚI"Rz¬LeÏ\x0004V6Êû\x0013sRêA</p><p>\x0015O§=N\x0007ÒOÕî­,ÌK!hÕÃ¤l2»±ß=±×±©zê\x0008«%ÝÁÎÎ<ÉÔ!GÍ|ÖÎihÑ,WÆ%i´W00&2z\x0002; ç¥WÓ^Ùôë¨ä6QJQö¢Ü\x0008\x0003;AìrN?</p><p>£¦ù7\x0012®\x001cÆ2Nå\x0019 \x0001È\x001eüÐõZ\x000cäµîQ­P®cT¼9ëÀ=;Õ­A<í.ÊùÍÓK!1O1p¿Täð3µu\x001aÛ¿¤ª¤G\x000c3Á\x001f­\x0019ÅÃi,²_\x0015Ü!Ôä7Ã=(°\x0019Ç8ÆF\x000fZi\x001cu©gòC'eÛ´\x0016ó1ÞØíMã\x0019\x0003 \x0010\x0012\x0007ÌF=jþv,u(åcû¹?w ÿ\x0000d÷ü\x000f5C8<1)Æ6)ÁaéL\x000fWÓäk\x001b\x0002\x0001ËHÅº:fªÜ^ÝÌÛ-ÐÍ!8ÉáWükR\x000bM<Á\x001fs¸D\x000bc\x001b@\x0018Ç~çÕ4«C±\x0014·û«¿#3\x0011tbãæä\x000cÿ\x0000</p><p>*x<3xòfâüÇ\x0018\x001fÁÔ×K\x0005Ô\x0013D²ÄÀ¡ô©C«c\x001cÓ²\x0003\x00014ýFÍ±æ¨BÜ0\x0015v9¦N¾VáëÅ&\x0017ØÐ\x0016 c Ã®)ÒÆFÑÈ»ãpU÷\x0006¥ÂûR2äw¦\x0007\x0001wnö7òZÈIØ~Vþòö5nÙA\x0003\x0015·®i/zÍ\x0008\x0006h¸ÇMÊ{~\x0007Î±àÊA\x001dsI eÀ\x001d¨§\x00058¢¨F\x000e§r¶¾S¼{ý}s,Lì$}®Ç!É$õíR\x0008íZV2\x0019º¶ã~äxíÃ±Ü²Î}rÇÜ:	mmÊI$³\x0015ÉÎÜ\x0012p@ãñþT\x0017Vv­¤\x0004T\x0003pêOqÅgÇu9¸m°³\x0010]\x0017\x0001³Õp³\x0017ó§%vìõ«Jú2e#¤M2û]f\x000b[\x0012\x0002¸ô_L÷8¦Í£A§\x0006K¬äò\x0004y#\x001fN­¢Y®m\x0013+¸E\x0005\x0006KdUÖ?0Ämà926qíÇ$Ôë²Ø\x0014nq\x0017\x0016,»NW¨#¸õ\x0014_væÁb0Mt3ÛZÎòA3\x001bVuá£%Aô%H®mV[yµÈ)"\x0002F2=jÄ5b}ÇºÓ\x001b\x001d3W\x0012Õ«\x0004Îv\x001ejà\x00126ÀõR¸þu.@\x001c[©\x0004\x001aé4¨-nU\"¼Nö=G§¥cÍ\x000cË\x000bÎ¶2/!\x0010:ò[Ô\x000fN+wÃ\x0016\x0013Z[4Ó8/páU{\x000fòhI=G\x0015©Ôxjö8¯$µa.ÕýT\x0013ü¹ü+ \x0001óóÇ¿\x001d\x0017\x0015ÅÛ9´ÕþÙpñ¢Dç`fÆA\x0018#=¸é]EÆ­\x0000´\x0013³ÚHó\x0014õ\x001eÿ\x0000Ê¬h¼ñî\x0001WÔU\x001b\x0012ß¿Eÿ\x0000r\x00101Ú¤ûSy¬±Dï!\x0003ä^{±§ØZÉ\x0000ÌAwbÍ_JÝÜFG"GðÓI3\x0005h¤GS·w$à}	ü«Ï ³y®$</p><p>éä	\x0003<çÐ{×qã«¶Ù\x00052Å\x0019Ïìøç²\x001fÒ¸¸.§tcQ$d$>é\x0004äoñÁªÐihW\x0000cyY#\x0011)\x001a}Ñõ8«v-í\x0016èíPÒ*W\x0019Á#>£4º¤i\x001c\x0001[ýJóß=?§Ü\\x000bÝ\x001cÛùçÄT¦\x0006ÒØ#\x001eÜT=ØÖÊÞódÏÕgr$\x001cÑ=Ò-Ó[ÛÚ"Æ\x0007;Ø±côÎ\x0007ÿ\x0000\UWÍ\x0004R9)#\x000c¶£ù\x000f¡¥¶1Euç1k1´m\x0001Tc¾N¥'k\x000eåË>Ú[[e\x0005°¬\x0014àç\x0019úV"YÜ­È¢t\x0019Ï\x0015«o)Y$w\x0001òr­Éük?P\x000c¹\x001fpsß?ýzTÛØÊ`¾àÍ¿\x0004ã¦1íM.\x0000B~NÇ[?Ê®Ú])­fdÏ*\x00101ëÍBöæÞý"h\x000bA\x0008NÒÀô­I$Õ|ðÊ</p><p>~ò1\x0000\x0010½º÷ª*È²`2¶@nOøU»»`³H«\x0000C\x001bçÊ\x000e\x000f\x0004ôã¯áP]Ï
Äí,\x0016©l§\x001clHÏ¨ÏJq\x0002]ÒM,B\x0016ùäÂ( \x0000=³Û\x0015\x001c°Mo;Eu\x0013$ªFCúãÞÒyabSÊ¶[\x001e§~TÖY\x001fs³1Æ\x0001cÎ(°ÉXá9Å\x0019%r\x000eG¦*<¶rH\x0003\x0018Á¥\x0018Î7qL	£8ù\x0000ûÒùY6`A\x0000¸4Ì\x0000¸#ó§Gò¹'\x001d8 \x000eò	¤ÕÎ±;çå\x0003,§¸5§¦øeùú!\x001fv>Àû×\x0017àË»_\x0013C\x001d¼Ç3þô\x0003P\x0002r}1þz×wu¬´·gO°Ä·#\x0001Çhóëþ\x0014ÒD²ì[Y\x00022¦qO¯µ9\x001aúq¢\x0010!þ9	ú/_Ï\x0014Û[Hlq5Ì¾eÇy_\x001eÊ:(ú~µeoîz¢EÄ\x001b¦>ùkù\x000e3S-¸ÿ\x0000\x0011®Oó©#rÃ$RÉ,q¦é\x0019T\x000eäâ\x00115\x0004|¡ú£úT
ow\x0011&\x000b¥q»2ìËäiÿ\x0000Ú\x0010?ú¥ox¢,?<bö©1ÿ\x0000\x001e7Xÿ\x0000t1\x0014W\x0016Ó,Z\x000flXádûñ¹öaßØOº·bnb ûØþãMúÊåÍä\x0013F²®1q	T`Ý3PAi>åbs%¿ðç\x000fCLOAÂ\x0003ÔU±\x00128ÜíSÐzQ@Ï\x001f·ól/\x001a7¸FX?{'\x001eÕ\x0015ÍçfLðÄp={Ô­¨§åcWð\x000eÞ:2ñY×\x0011Ï4»YCFNVEùõ?ýjçßsg.ÄÖÒ a"UÖLõ"¦76×W\x0001¥UXå ÊëÝëY«o$\x0004pîÆ}êÕÃæ~¤uÛFzûÐÒÝ\x0012µ:ÿ\x0000Ò{¹b}èÈ$RØ\x0008\x0018}ß¨ªy+Ý¡µ0\x0005U</p><p>¢IÄdg?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js](https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select blank values from multiselect`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>select blank values from multiselect</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
Instances: 11
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-05-11&start_date=2020-11-01&territory=63](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-05-11&start_date=2020-11-01&territory=63)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/stats" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats](https://place-des-entreprises.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/stats" accept-charset="UTF-8" method="get">`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "start_date" "end_date" "commit" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js`
  
  
  * Evidence: `<script src='https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@20210329/tarteaucitron.min.js' type='text/javascript'></script>`
  
  
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/packs/js/pages-44ff17db39b6d5c584bc.js](https://place-des-entreprises.beta.gouv.fr/packs/js/pages-44ff17db39b6d5c584bc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/packs/js/application-a012f70aa4e8cca02365.js](https://place-des-entreprises.beta.gouv.fr/packs/js/application-a012f70aa4e8cca02365.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js](https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/highcharts-567e2edbd9da97346811f4298b2a010868618d927a37a541af75d3ea043b86e3.js](https://place-des-entreprises.beta.gouv.fr/assets/highcharts-567e2edbd9da97346811f4298b2a010868618d927a37a541af75d3ea043b86e3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/robots.txt](https://place-des-entreprises.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, s-maxage=31536000, max-age=15552000`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Bkuhvsb7ofpaKdm1xZpKr9eip3mpG5lWr`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FOQjBwcOsiD6jwGq4hMZavuhbIHWjlE4IqPzu22FGJ09ZYO0gTD`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2ki6W2pgZi6uo2VJAVmwSIgnt7c1n3NA`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `A7gaVCVfCa3fO0SWV6Kf0vgHnBWVsoW57scaKWMxHtvhZOYvMuZtUkEVd5ZZ0lw72Wxm0zGDNCv4guJ`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BFF8d1qpcStGcOq1kHqP9KBEziLVDESppK8MwwcYwI`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BgDkTCqF225sAUyj2cUJ7lEoHw1Jd4`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FeeN671Zk93ihdnJbU1xRPaz8nTrHuetjSrs5jKZjLQeVSl3cQk9wVAUJ0uPaqWN7gr0mmRgqqNKF0xJmZm0UVXGU7OA925uaAb3hJP15r`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `2By3TAqs3tKIc5Ctxlu2rSfBpjyDo20dvpKL7YQv6ltMv0Jl8BXNaOQbFE1Kk972NHX4uAn9x7lq0cSLdc84G0WAIgGpSwTnrzkuVVmAArGhdDG9BFHtGjha`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FCKXjvu79GJ6s03xgoDPAP0Aa0lgglwBLhRIq`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BItN686cQdq7L6Jd1FGTgHgOaGTM334DtMGAepR19nkssjT97BabW5CIWFag3DE3V0F1CKh7mjuBfoJIlh3FunqSJ`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `Lh1rEvPXawaYR0U2xqghVdIEMYwD270eGPegwd2LQirmbiyNwh0A3T1HqXK1KSNk58H8fqJTIWeIZKPt2rki0qaUQ3`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `VTunSUCEZtJ253UjHu2VMmRb2rzZFsBiQ2QIHBcHdrLXVOgCq918yh9h`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�\x0019.��\x001b��h�f�\x0016i*�^���neZ</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script></p><p>  tarteaucitron.init({</p><p>    "privacyUrl": "",</p><p>    "hashtag": "#consentement",</p><p>    "cookieName": "tarteaucitron",</p><p>    "bo", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="tarteaucitron.userInterface.openPanel();return false" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/robots.txt](https://place-des-entreprises.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `s-maxage=31536000`
  
  
  
  
Instances: 1
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `798054765`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `798054765`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `798054765`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `798054765`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `798054765`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>20210329, which evaluates to: 1970-08-22 21:58:49</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[email]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[full_name]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[phone_number]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_options_slugs][]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_slug]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[email]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_options_slugs][]`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [data-disable-with] attribute </p><p></p><p>The user input found was:</p><p>commit=Connexion</p><p></p><p>The user-controlled value was:</p><p>connexion</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3


# ZAP Scanning Report

Generated on Thu, 22 Apr 2021 09:29:18


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 4 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| Dangerous JS Functions | Low | 4 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 3 | 
| Non-Storable Content | Informational | 10 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 576 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 11 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
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
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
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
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
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

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-04-22&start_date=2020-10-01&territory=63](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-04-22&start_date=2020-10-01&territory=63)
  
  
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

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/highcharts-567e2edbd9da97346811f4298b2a010868618d927a37a541af75d3ea043b86e3.js](https://place-des-entreprises.beta.gouv.fr/assets/highcharts-567e2edbd9da97346811f4298b2a010868618d927a37a541af75d3ea043b86e3.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/packs/js/application-47cec7361a3c7e110904.js](https://place-des-entreprises.beta.gouv.fr/packs/js/application-47cec7361a3c7e110904.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/packs/js/pages-711e95e411c04ee7d6bd.js](https://place-des-entreprises.beta.gouv.fr/packs/js/pages-711e95e411c04ee7d6bd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eVal`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js](https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/robots.txt](https://place-des-entreprises.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, s-maxage=31536000, max-age=15552000`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `2B0yD3JEhZtWmbpiRmR5GQxNvXoFhhqB1wKorvg8LRTbr5cOpiNzKqVlx6FTsMU3nGTGd0EgJ0NTgJKAwtRKr2WFK9W5vxglLCleiWazwTAIgOL62w1wX4y6S5baLE9VGYZhhfVpeM2VamOyO3yroC0S4aUKRFlaQzekW08qd1mY8l9TIaGzfrpnGluGyK1ebyOXT16gYpfa2bbYAgOvc9NVQZNnpzpqtKf3QiAkTymz`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `XIbyhN0U9fD3FHWCGB30GZordIOFIvFbRKFxMg8Y386XxuGmoVho0TckTa4f4X0ldrMMpAxovb5eegeuPC9zko`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `2B9dSuRxuPaYaxdE5HJp1qUCus4e1q3EqnzCoG`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FDBYprKFRM2Pp4TC3i2LzDeuK9yKz`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `2F83fAFvTVsgeVSTu18nlz2hbhTQ0iJIVP`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `2F2bgspEgb7UakB4EC5DuGxUA9Gr64UI5lGjLGCI4WY`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5fd0ht7ciANcgkJdMW1FcE8m8SRCq0bEnhX`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FXTuFNBdXBrTcItcxeOnc7r6siRJwESmaMUNQqGI1cfrTFeT3Zfr6XjBiqWj8cACnYa`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `bYvdEkb4cdmVbwyJA0z9xiU67Yhp1kLuynXDDKJj7pg1IHUCLMBH1arPEIYNA9qR82kRdaROTv0JCb5QoJOBxrwMeRtiokQLy97bLJfnBXDj`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FJIvXQHUWJgqZb3UWwDdJGXdAKRID9R3TrYVdqhP9yWyiuKH1lDGj0s0NJoifjYfOC9qgfwX36gSVExLwFltKNg5jUTIX4MJpOnsKf5T12bzOYMhyHmr81nBazpj3NdOJCVPAaIv19ppE2G3QbkpOPyO6kpy27CU6LsntWBhaKhweG`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FOawLZHDK73NRXU3P1PasrFrxh3oSA`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Blhp1e4cTR8OOO1IanKqHcuZQz9rsgQ498cXhn75c76DP6edRo2fGP4W7C87LuBwaOQm8vc5Al4YgIkDajBGPBuvNLkHkrxf1DQlqHs2Ce62e4`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�\x001d2\x000frD��V��bFdy\x0019\x000cM�z\x0005�\x001a��\x0002���<-\x0014ۯ�\x000e�#s*�eǡS��7�d�wA 'CS�����J�e�+չ�\x0018%,)^�f��0\x0008����
p_��K��,OU\x0019�a��ix͕jc�;|��-\x0012�</p><p>DYZC7�[O*wY��_S!��~�g\x001a[�ȭ^o#�O^�b��ٶ�\x0002\x0003�s�UA�g�:j���B $O)�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "<script></p><p>  var _paq = _paq || [];</p><p>  // Configure Matomo analytics</p><p>  _paq.push(['trackPageView']);</p><p>  _paq.push(['enableLinkTracki", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js](https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a />").addClass(F.label).attr("data-"+R.value,r).html(j.label(r,n,k.preserveHTML,k.className)),a=k.onLabelCreate.call(a,r,n),A.has.label(t)?A.debug("User selection already exists, skipping",r):(k.label.variation&&a.addClass(k.label.variation),!0===i?(A.debug("Animating in label",a),a.addClass(F.hidden).insertBefore(o).transition({animation:k.label.transition,debug:k.debug,verbose:k.verbose,duration:k.label.duration})):(A.debug("Adding selection label",a),a.insertBefore(o)))},message:function(t){var n=Q.children(P.message),i=k.templates.message(A.add.variables(t));n.length>0?n.html(i):n=e("<div/>").html(i).addClass(F.message).appendTo(Q)},optionValue:function(t){var n=A.escape.value(t);Y.find('option[value="'+A.escape.string(n)+'"]').length>0||(A.disconnect.selectObserver(),A.is.single()&&(A.verbose("Removing previous user addition"),Y.find("option."+F.addition).remove()),e("<option/>").prop("value",n).addClass(F.addition).html(t).appendTo(Y),A.verbose("Adding user addition as an <option>",t),A.observe.select())},userSuggestion:function(e){var t,n=Q.children(P.addition),i=A.get.item(e),a=i&&i.not(P.addition).length,o=n.length>0;k.useLabels&&A.has.maxSelections()||(""===e||a?n.remove():(o?(n.data(R.value,e).data(R.text,e).attr("data-"+R.value,e).attr("data-"+R.text,e).removeClass(F.filtered),k.hideAdditions||(t=k.templates.addition(A.add.variables(O.addResult,e)),n.html(t)),A.verbose("Replacing user suggestion with new value",n)):((n=A.create.userChoice(e)).prependTo(Q),A.verbose("Adding item choice to menu corresponding with user choice addition",n)),k.hideAdditions&&!A.is.allFiltered()||n.addClass(F.selected).siblings().removeClass(F.selected),A.refreshItems()))},variables:function(e,t){var n,i,a=-1!==e.search("{count}"),o=-1!==e.search("{maxCount}"),r=-1!==e.search("{term}");return A.verbose("Adding templated variables to message",e),a&&(n=A.get.selectionCount(),e=e.replace("{count}",n)),o&&(n=A.get.selectionCount(),e=e.replace("{maxCount}",k.maxSelections)),r&&(i=t||A.get.query(),e=e.replace("{term}",i)),e},value:function(e,t,n){var i,a=A.get.values();A.has.value(e)?A.debug("Value already selected"):""!==e?(Array.isArray(a)?(i=a.concat([e]),i=A.get.uniqueArray(i)):i=[e],A.has.selectInput()?A.can.extendSelect()&&(A.debug("Adding value to select",e,i,Y),A.add.optionValue(e)):(i=i.join(k.delimiter),A.debug("Setting hidden input to delimited value",i,Y)),!1===k.fireOnInit&&A.is.initialLoad()?A.verbose("Skipping onadd callback on initial load",k.onAdd):k.onAdd.call(ne,e,t,n),A.set.value(i,t,n),A.check.maxSelections()):A.debug("Cannot select blank values from multiselect")}},remove:{active:function(){z.removeClass(F.active)},activeLabel:function(){z.find(P.label).removeClass(F.active)},empty:function(){z.removeClass(F.empty)},loading:function(){z.removeClass(F.loading)},initialLoad:function(){b=!1},upward:function(e){(e||z).removeClass(F.upward)},leftward:function(e){(e||Q).removeClass(F.leftward)},visible:function(){z.removeClass(F.visible)},activeItem:function(){X.removeClass(F.active)},filteredItem:function(){k.useLabels&&A.has.maxSelections()||(k.useLabels&&A.is.multiple()?X.not("."+F.active).removeClass(F.filtered):X.removeClass(F.filtered),k.hideDividers&&J.removeClass(F.hidden),A.remove.empty())},optionValue:function(e){var t=A.escape.value(e),n=Y.find('option[value="'+A.escape.string(t)+'"]');n.length>0&&n.hasClass(F.addition)&&(T&&(T.disconnect(),A.verbose("Temporarily disconnecting mutation observer")),n.remove(),A.verbose("Removing user addition as an <option>",t),T&&T.observe(Y[0],{childList:!0,subtree:!0}))},message:function(){Q.children(P.message).remove()},searchWidth:function(){W.css("width","")},searchTerm:function(){A.verbose("Cleared search term"),W.val(""),A.set.filtered()},userAddition:function(){X.filter(P.addition).remove()},selected:function(t,n){if(!(n=k.allowAdditions?n||A.get.itemWithAdditions(t):n||A.get.item(t)))return!1;n.each(function(){var t=e(this),n=A.get.choiceText(t),i=A.get.choiceValue(t,n);A.is.multiple()?k.useLabels?(A.remove.value(i,n,t),A.remove.label(i)):(A.remove.value(i,n,t),0===A.get.selectionCount()?A.set.placeholderText():A.set.text(A.add.variables(O.count))):A.remove.value(i,n,t),t.removeClass(F.filtered).removeClass(F.active),k.useLabels&&t.removeClass(F.selected)})},selectedItem:function(){X.removeClass(F.selected)},value:function(e,t,n){var i,a=A.get.values();e=A.escape.htmlEntities(e),A.has.selectInput()?(A.verbose("Input is <select> removing selected option",e),i=A.remove.arrayValue(e,a),A.remove.optionValue(e)):(A.verbose("Removing from delimited values",e),i=(i=A.remove.arrayValue(e,a)).join(k.delimiter)),!1===k.fireOnInit&&A.is.initialLoad()?A.verbose("No callback on initial load",k.onRemove):k.onRemove.call(ne,e,t,n),A.set.value(i,t,n),A.check.maxSelections()},arrayValue:function(t,n){return Array.isArray(n)||(n=[n]),n=e.grep(n,function(e){return t!=e}),A.verbose("Removed value from delimited string",t,n),n},label:function(e){var t=z.find(P.label).filter("[data-"+R.value+'="'+A.escape.string(k.ignoreCase?e.toLowerCase():e)+'"]');A.verbose("Removing label",t),t.remove()},activeLabels:function(e){e=e||z.find(P.label).filter("."+F.active),A.verbose("Removing active label selections",e),A.remove.labels(e)},labels:function(t){t=t||z.find(P.label),A.verbose("Removing labels",t),t.each(function(){var t=e(this),n=t.data(R.value),a=n!==i?String(n):n,o=A.is.userValue(a);!1!==k.onLabelRemove.call(t,n)?(A.remove.message(),o?(A.remove.value(a),A.remove.label(a)):A.remove.selected(a)):A.debug("Label remove callback cancelled removal")})},tabbable:function(){A.is.searchSelection()?(A.debug("Searchable dropdown initialized"),W.removeAttr("tabindex"),Q.removeAttr("tabindex")):(A.debug("Simple selection dropdown initialized"),z.removeAttr("tabindex"),Q.removeAttr("tabindex"))},diacritics:function(e){return k.ignoreDiacritics?e.normalize("NFD").replace(/[\u0300-\u036f]/g,""):e}},has:{menuSearch:function(){return A.has.search()&&W.closest(Q).length>0},clearItem:function(){return G.length>0},search:function(){return W.length>0},sizer:function(){return B.length>0},selectInput:function(){return Y.is("select")},minCharacters:function(e){return k.minCharacters&&!te?(e=e!==i?String(e):String(A.get.query())).length>=k.minCharacters:(te=!1,!0)},firstLetter:function(e,t){var n;return!(!e||0===e.length||"string"!=typeof t)&&(n=A.get.choiceText(e,!1),(t=t.toLowerCase())==String(n).charAt(0).toLowerCase())},input:function(){return Y.length>0},items:function(){return X.length>0},menu:function(){return Q.length>0},message:function(){return 0!==Q.children(P.message).length},label:function(e){var t=A.escape.value(e),n=z.find(P.label);return k.ignoreCase&&(t=t.toLowerCase()),n.filter("[data-"+R.value+'="'+A.escape.string(t)+'"]').length>0},maxSelections:function(){return k.maxSelections&&A.get.selectionCount()>=k.maxSelections},allResultsFiltered:function(){var e=X.not(P.addition);return e.filter(P.unselectable).length===e.length},userSuggestion:function(){return Q.children(P.addition).length>0},query:function(){return""!==A.get.query()},value:function(e){return k.ignoreCase?A.has.valueIgnoringCase(e):A.has.valueMatchingCase(e)},valueMatchingCase:function(t){var n=A.get.values();return!!(Array.isArray(n)?n&&-1!==e.inArray(t,n):n==t)},valueIgnoringCase:function(t){var n=A.get.values(),i=!1;return Array.isArray(n)||(n=[n]),e.each(n,function(e,n){if(String(t).toLowerCase()==String(n).toLowerCase())return i=!0,!1}),i}},is:{active:function(){return z.hasClass(F.active)},animatingInward:function(){return Q.transition("is inward")},animatingOutward:function(){return Q.transition("is outward")},bubbledLabelClick:function(t){return e(t.target).is("select, input")&&z.closest("label").length>0},bubbledIconClick:function(t){return e(t.target).closest(K).length>0},alreadySetup:function(){return z.is("select")&&z.parent(P.dropdown).data(H)!==i&&0===z.prev().length},animating:function(e){return e?e.transition&&e.transition("is animating"):Q.transition&&Q.transition("is animating")},leftward:function(e){return(e||Q).hasClass(F.leftward)},clearable:function(){return z.hasClass(F.clearable)||k.clearable},disabled:function(){return z.hasClass(F.disabled)},focused:function(){return n.activeElement===z[0]},focusedOnSearch:function(){return n.activeElement===W[0]},allFiltered:function(){return(A.is.multiple()||A.has.search())&&!(0==k.hideAdditions&&A.has.userSuggestion())&&!A.has.message()&&A.has.allResultsFiltered()},hidden:function(e){return!A.is.visible(e)},initialLoad:function(){return b},inObject:function(t,n){var i=!1;return e.each(n,function(e,n){if(n==t)return i=!0,!0}),i},multiple:function(){return z.hasClass(F.multiple)},remote:function(){return k.apiSettings&&A.can.useAPI()},single:function(){return!A.is.multiple()},selectMutation:function(t){var n=!1;return e.each(t,function(t,i){if(e(i.target).is("select")||e(i.addedNodes).is("select"))return n=!0,!1}),n},search:function(){return z.hasClass(F.search)},searchSelection:function(){return A.has.search()&&1===W.parent(P.dropdown).length},selection:function(){return z.hasClass(F.selection)},userValue:function(t){return-1!==e.inArray(t,A.get.userValues())},upward:function(e){return(e||z).hasClass(F.upward)},visible:function(e){return e?e.hasClass(F.visible):Q.hasClass(F.visible)},verticallyScrollableContext:function(){var e=V.get(0)!==t&&V.css("overflow-y");return"auto"==e||"scroll"==e},horizontallyScrollableContext:function(){var e=V.get(0)!==t&&V.css("overflow-X");return"auto"==e||"scroll"==e}},can:{activate:function(e){return!!k.useLabels||(!A.has.maxSelections()||!(!A.has.maxSelections()||!e.hasClass(F.active)))},openDownward:function(e){var n,i=e||Q,a=!0,o={};return i.addClass(F.loading),n={context:{offset:V.get(0)===t?{top:0,left:0}:V.offset(),scrollTop:V.scrollTop(),height:V.outerHeight()},menu:{offset:i.offset(),height:i.outerHeight()}},A.is.verticallyScrollableContext()&&(n.menu.offset.top+=n.context.scrollTop),(o={above:n.context.scrollTop<=n.menu.offset.top-n.context.offset.top-n.menu.height,below:n.context.scrollTop+n.context.height>=n.menu.offset.top-n.context.offset.top+n.menu.height}).below?(A.verbose("Dropdown can fit in context downward",o),a=!0):o.below||o.above?(A.verbose("Dropdown cannot fit below, opening upward",o),a=!1):(A.verbose("Dropdown cannot fit in either direction, favoring downward",o),a=!0),i.removeClass(F.loading),a},openRightward:function(e){var n,i=e||Q,a=!0,o=!1;return i.addClass(F.loading),n={context:{offset:V.get(0)===t?{top:0,left:0}:V.offset(),scrollLeft:V.scrollLeft(),width:V.outerWidth()},menu:{offset:i.offset(),width:i.outerWidth()}},A.is.horizontallyScrollableContext()&&(n.menu.offset.left+=n.context.scrollLeft),(o=n.menu.offset.left-n.context.offset.left+n.menu.width>=n.context.scrollLeft+n.context.width)&&(A.verbose("Dropdown cannot fit in context rightward",o),a=!1),i.removeClass(F.loading),a},click:function(){return c||"click"==k.on},extendSelect:function(){return k.allowAdditions||k.apiSettings},show:function(){return!A.is.disabled()&&(A.has.items()||A.has.message())},useAPI:function(){return e.fn.api!==i}},animate:{show:function(t,n){var a,o=n||Q,r=n?function(){}:function(){A.hideSubMenus(),A.hideOthers(),A.set.active()};if(t=e.isFunction(t)?t:function(){},A.verbose("Doing menu show animation",o),A.set.direction(n),a=A.get.transition(n),A.is.selection()&&A.set.scrollPosition(A.get.selectedItem(),!0),A.is.hidden(o)||A.is.animating(o)){var s=!!z.hasClass("column")&&"flex";"none"==a?(r(),o.transition({displayType:s}).transition("show"),t.call(ne)):e.fn.transition!==i&&z.transition("is supported")?o.transition({animation:a+" in",debug:k.debug,verbose:k.verbose,duration:k.duration,queue:!0,onStart:r,displayType:s,onComplete:function(){t.call(ne)}}):A.error(q.noTransition,a)}},hide:function(t,n){var a=n||Q,o=n?function(){}:function(){A.can.click()&&A.unbind.intent(),A.remove.active()},r=A.get.transition(n);t=e.isFunction(t)?t:function(){},(A.is.visible(a)||A.is.animating(a))&&(A.verbose("Doing menu hide animation",a),"none"==r?(o(),a.transition("hide"),t.call(ne)):e.fn.transition!==i&&z.transition("is supported")?a.transition({animation:r+" out",duration:k.duration,debug:k.debug,verbose:k.verbose,queue:!1,onStart:o,onComplete:function(){t.call(ne)}}):A.error(q.transition))}},hideAndClear:function(){A.remove.searchTerm(),A.has.maxSelections()||(A.has.search()?A.hide(function(){A.remove.filteredItem()}):A.hide())},delay:{show:function(){A.verbose("Delaying show event to ensure user intent"),clearTimeout(A.timer),A.timer=setTimeout(A.show,k.delay.show)},hide:function(){A.verbose("Delaying hide event to ensure user intent"),clearTimeout(A.timer),A.timer=setTimeout(A.hide,k.delay.hide)}},escape:{value:function(t){var n=Array.isArray(t),i="string"==typeof t,a=!i&&!n,o=i&&-1!==t.search(I.quote),r=[];return a||!o?t:(A.debug("Encoding quote values for use in select",t),n?(e.each(t,function(e,t){r.push(t.replace(I.quote,"&quot;"))}),r):t.replace(I.quote,"&quot;"))},string:function(e){return(e=String(e)).replace(I.escape,"\\$&")},htmlEntities:function(e){var t=/[<>"'`]/g,n={"<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#x27;","`":"&#x60;"},i=function(e){return n[e]};return/[&<>"'`]/.test(e)?(e=e.replace(/&(?![a-z0-9#]{1,6};)/,"&amp;")).replace(t,i):e}},setting:function(t,n){if(A.debug("Changing setting",t,n),e.isPlainObject(t))e.extend(!0,k,t);else{if(n===i)return k[t];e.isPlainObject(k[t])?e.extend(!0,k[t],n):k[t]=n}},internal:function(t,n){if(e.isPlainObject(t))e.extend(!0,A,t);else{if(n===i)return A[t];A[t]=n}},debug:function(){!k.silent&&k.debug&&(k.performance?A.performance.log(arguments):(A.debug=Function.prototype.bind.call(console.info,console,k.name+":"),A.debug.apply(console,arguments)))},verbose:function(){!k.silent&&k.verbose&&k.debug&&(k.performance?A.performance.log(arguments):(A.verbose=Function.prototype.bind.call(console.info,console,k.name+":"),A.verbose.apply(console,arguments)))},error:function(){k.silent||(A.error=Function.prototype.bind.call(console.error,console,k.name+":"),A.error.apply(console,arguments))},performance:{log:function(e){var t,n;k.performance&&(n=(t=(new Date).getTime())-(d||t),d=t,f.push({Name:e[0],Arguments:[].slice.call(e,1)||"",Element:ne,"Execution Time":n})),clearTimeout(A.performance.timer),A.performance.timer=setTimeout(A.performance.display,500)},display:function(){var t=k.name+":",n=0;d=!1,clearTimeout(A.performance.timer),e.each(f,function(e,t){n+=t["Execution Time"]}),t+=" "+n+"ms",l&&(t+=" '"+l+"'"),(console.group!==i||console.table!==i)&&f.length>0&&(console.groupCollapsed(t),console.table?console.table(f):e.each(f,function(e,t){console.log(t.Name+": "+t["Execution Time"]+"ms")}),console.groupEnd()),f=[]}},invoke:function(t,n,a){var r,s,l,c=ie;return n=n||g,a=ne||a,"string"==typeof t&&c!==i&&(t=t.split(/[\. ]/),r=t.length-1,e.each(t,function(n,a){var o=n!=r?a+t[n+1].charAt(0).toUpperCase()+t[n+1].slice(1):t;if(e.isPlainObject(c[o])&&n!=r)c=c[o];else{if(c[o]!==i)return s=c[o],!1;if(!e.isPlainObject(c[a])||n==r)return c[a]!==i?(s=c[a],!1):(A.error(q.method,t),!1);c=c[a]}})),e.isFunction(s)?l=s.apply(a,n):s!==i&&(l=s),Array.isArray(o)?o.push(l):o!==i?o=[o,l]:l!==i&&(o=l),s}},p?(ie===i&&A.initialize(),A.invoke(m)):(ie!==i&&ie.invoke("destroy"),A.initialize())}),o!==i?o:r},e.fn.dropdown.settings={silent:!1,debug:!1,verbose:!1,performance:!0,on:"click",action:"activate",values:!1,clearable:!1,apiSettings:!1,selectOnKeydown:!0,minCharacters:0,filterRemoteData:!1,saveRemoteData:!0,throttle:200,context:t,direction:"auto",keepOnScreen:!0,match:"both",fullTextSearch:!1,ignoreDiacritics:!1,hideDividers:!1,placeholder:"auto",preserveHTML:!0,sortSelect:!1,forceSelection:!0,allowAdditions:!1,ignoreCase:!1,ignoreSearchCase:!0,hideAdditions:!0,maxSelections:!1,useLabels:!0,delimiter:",",showOnFocus:!0,allowReselection:!1,allowTab:!0,allowCategorySelection:!1,fireOnInit:!1,transition:"auto",duration:200,glyphWidth:1.037,headerDivider:!0,label:{transition:"scale",duration:200,variation:!1},delay:{hide:300,show:200,search:20,touch:50},onChange:function(){},onAdd:function(){},onRemove:function(){},onLabelSelect:function(){},onLabelCreate:function(){return e(this)},onLabelRemove:function(){return!0},onNoResults:function(){return!0},onShow:function(){},onHide:function(){},name:"Dropdown",namespace:"dropdown",message:{addResult:"Add <b>{term}</b>",count:"{count} selected",maxSelections:"Max {maxCount} selections",noResults:"No results found.",serverError:"There was an error contacting the server"},error:{action:"You called a dropdown action that was not defined",alreadySetup:"Once a select has been initialized behaviors must be called on the created ui dropdown",labels:"Allowing user additions currently requires the use of labels.",missingMultiple:"<select> requires multiple property to be set to correctly preserve multiple values",method:"The method you called is not defined.",noAPI:"The API module is required to load resources remotely",noStorage:"Saving remote data requires session storage",noTransition:"This module requires ui transitions <https://github.com/Semantic-Org/UI-Transition>",noNormalize:'"ignoreDiacritics" setting will be ignored. Browser does not support String().normalize(). You may consider including <https://cdn.jsdelivr.net/npm/unorm@1.4.1/lib/unorm.min.js> as a polyfill.'},regExp:{escape:/[-[\]{}()*+?.,\\^$|#\s:=@]/g,quote:/"/g},metadata:{defaultText:"defaultText",defaultValue:"defaultValue",placeholderText:"placeholder",text:"text",value:"value"},fields:{remoteValues:"results",values:"values",disabled:"disabled",name:"name",value:"value",text:"text",type:"type",image:"image",imageClass:"imageClass",icon:"icon",iconClass:"iconClass","class":"class",divider:"divider"},keys:{backspace:8,delimiter:188,
deleteKey:46,enter:13,escape:27,pageUp:33,pageDown:34,leftArrow:37,upArrow:38,rightArrow:39,downArrow:40},selector:{addition:".addition",divider:".divider, .header",dropdown:".ui.dropdown",hidden:".hidden",icon:"> .dropdown.icon",input:'> input[type="hidden"], > select',item:".item",label:"> .label",remove:"> .label > .delete.icon",siblingLabel:".label",menu:".menu",message:".message",menuIcon:".dropdown.icon",search:"input.search, .menu > .search > input, .menu input.search",sizer:"> span.sizer",text:"> .text:not(.icon)",unselectable:".disabled, .filtered",clearIcon:"> .remove.icon"},className:{active:"active",addition:"addition",animating:"animating",disabled:"disabled",empty:"empty",dropdown:"ui dropdown",filtered:"filtered",hidden:"hidden transition",icon:"icon",image:"image",item:"item",label:"ui label",loading:"loading",menu:"menu",message:"message",multiple:"multiple",placeholder:"default",sizer:"sizer",search:"search",selected:"selected",selection:"selection",upward:"upward",leftward:"left",visible:"visible",clearable:"clearable",noselection:"noselection","delete":"delete",header:"header",divider:"divider",groupIcon:"",unfilterable:"unfilterable"}},e.fn.dropdown.settings.templates={deQuote:function(e){return String(e).replace(/"/g,"")},escape:function(e,t){if(t)return e;var n=/[<>"'`]/g,i={"<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#x27;","`":"&#x60;"},a=function(e){return i[e]};return/[&<>"'`]/.test(e)?(e=e.replace(/&(?![a-z0-9#]{1,6};)/,"&amp;")).replace(n,a):e},dropdown:function(t,n,i,a){var o=t.placeholder||!1,r="",s=e.fn.dropdown.settings.templates.escape;return r+='<i class="dropdown icon"></i>',r+=o?'<div class="default text">'+s(o,i)+"</div>":'<div class="text"></div>',r+='<div class="'+a.menu+'">',r+=e.fn.dropdown.settings.templates.menu(t,n,i,a),r+="</div>"},menu:function(t,n,i,a){var o=t[n.values]||[],r="",s=e.fn.dropdown.settings.templates.escape,l=e.fn.dropdown.settings.templates.deQuote;return e.each(o,function(e,t){var o=t[n.type]?t[n.type]:"item";if("item"===o){var c=t[n.text]?' data-text="'+l(t[n.text])+'"':"",u=t[n.disabled]?a.disabled+" ":"";r+='<div class="'+u+(t[n["class"]]?l(t[n["class"]]):a.item)+'" data-value="'+l(t[n.value])+'"'+c+">",t[n.image]&&(r+='<img class="'+(t[n.imageClass]?l(t[n.imageClass]):a.image)+'" src="'+l(t[n.image])+'">'),t[n.icon]&&(r+='<i class="'+l(t[n.icon])+" "+(t[n.iconClass]?l(t[n.iconClass]):a.icon)+'"></i>'),r+=s(t[n.name]||"",i),r+="</div>"}else if("header"===o){var d=s(t[n.name]||"",i),f=t[n.icon]?l(t[n.icon]):a.groupIcon;""===d&&""===f||(r+='<div class="'+(t[n["class"]]?l(t[n["class"]]):a.header)+'">',""!==f&&(r+='<i class="'+f+" "+(t[n.iconClass]?l(t[n.iconClass]):a.icon)+'"></i>'),r+=d,r+="</div>"),t[n.divider]&&(r+='<div class="'+a.divider+'"></div>')}}),r},label:function(t,n,i,a){return(0,e.fn.dropdown.settings.templates.escape)(n,i)+'<i class="'+a["delete"]+' icon"></i>'},message:function(e){return e},addition:function(e){return e}}}(jQuery,window,document),function(e,t,n,i){"use strict";e.isFunction=e.isFunction||function(e){return"function"==typeof e&&"number"!=typeof e.nodeType},t=void 0!==t&&t.Math==Math?t:"undefined"!=typeof self&&self.Math==Math?self:Function("return this")(),e.fn.calendar=function(a){var o,r=e(this),s=r.selector||"",l=(new Date).getTime(),c=[],u=arguments[0],d="string"==typeof u,f=[].slice.call(arguments,1),m={5:{row:4,column:3},10:{row:3,column:2},15:{row:2,column:2},20:{row:3,column:1},30:{row:2,column:1}},p=["","one","two","three","four","five","six","seven","eight"];return r.each(function(){var r,g,h,v=e.isPlainObject(a)?e.extend(!0,{},e.fn.calendar.settings,a):e.extend({},e.fn.calendar.settings),b=v.className,y=v.namespace,w=v.selector,C=v.formatter,x=v.parser,T=v.metadata,D=m[v.minTimeGap],S=v.error,A="."+y,k="module-"+y,F=e(this),O=F.find(w.input),M=F.find(w.popup),E=F.find(w.activator),R=this,L=F.data(k),I=!1,P=F.hasClass(b.inverted),q=!1,j=!1;h={initialize:function(){h.debug("Initializing calendar for",R,F),r=h.get.isTouch(),h.setup.config(),h.setup.popup(),h.setup.inline(),h.setup.input(),h.setup.date(),h.create.calendar(),h.bind.events(),h.observeChanges(),h.instantiate()},instantiate:function(){h.verbose("Storing instance of calendar"),L=h,F.data(k,L)},destroy:function(){h.verbose("Destroying previous calendar for",R),F.removeData(k),h.unbind.events(),h.disconnect.classObserver()},setup:{config:function(){null!==h.get.minDate()&&h.set.minDate(F.data(T.minDate)),null!==h.get.maxDate()&&h.set.maxDate(F.data(T.maxDate)),h.setting("type",h.get.type()),h.setting("on",v.on||(O.length?"focus":"click"))},popup:function(){if(!v.inline&&(E.length||(E=F.children().first()).length))if(e.fn.popup!==i){if(!M.length){var t=E.parent(),n=0!==t.closest(w.append).length?"appendTo":"prependTo";M=e("<div/>").addClass(b.popup)[n](t)}M.addClass(b.calendar),P&&M.addClass(b.inverted);var a=function(){return h.refreshTooltips(),v.onVisible.apply(M,arguments)},o=v.onHidden;O.length||(M.attr("tabindex","0"),a=function(){return h.refreshTooltips(),h.focus(),v.onVisible.apply(M,arguments)},o=function(){return h.blur(),v.onHidden.apply(M,arguments)});var r=function(){return h.set.focusDate(h.get.date()),h.set.mode(h.get.validatedMode(v.startMode)),v.onShow.apply(M,arguments)},s=h.setting("on"),l=e.extend({},v.popupOptions,{popup:M,on:s,hoverable:"hover"===s,closable:"click"===s,onShow:r,onVisible:a,onHide:v.onHide,onHidden:o});h.popup(l)}else h.error(S.popup)},inline:function(){E.length&&!v.inline||(v.inline=!0,M=e("<div/>").addClass(b.calendar).appendTo(F),O.length||M.attr("tabindex","0"))},input:function(){v.touchReadonly&&O.length&&r&&O.prop("readonly",!0),h.check.disabled()},date:function(){var e;v.initialDate?e=x.date(v.initialDate,v):F.data(T.date)!==i?e=x.date(F.data(T.date),v):O.length&&(e=x.date(O.val(),v)),h.set.date(e,v.formatInput,!1),h.set.mode(h.get.mode(),!1)}},trigger:{change:function(){var e=O[0];if(e){var t=n.createEvent("HTMLEvents");h.verbose("Triggering native change event"),t.initEvent("change",!0,!1),e.dispatchEvent(t)}}},create:{calendar:function(){var t,n,a,o,r,s,l,c=h.get.mode(),u=new Date,d=h.get.date(),f=h.get.focusDate(),m=h.helper.dateInRange(f||d||v.initialDate||u);f||(f=m,h.set.focusDate(f,!1,!1));var g="year"===c,y="month"===c,w="day"===c,x="hour"===c,S="minute"===c,A="time"===v.type,k=Math.max(v.multiMonth,1),F=w?h.get.monthOffset():0,O=m.getMinutes(),E=m.getHours(),R=m.getDate(),L=m.getMonth()+F,I=m.getFullYear(),q=w?v.showWeekNumbers?8:7:x?4:D.column,j=w||x?6:D.row,N=w?k:1,H=M,z=H.hasClass("left")?"right center":"left center";for(H.empty(),N>1&&(l=e("<div/>").addClass(b.grid).appendTo(H)),o=0;o<N;o++){if(N>1)H=e("<div/>").addClass(b.column).appendTo(l);var V=L+o,U=(new Date(I,V,1).getDay()-v.firstDayOfWeek%7+7)%7;if(!v.constantHeight&&w){var W=new Date(I,V+1,0).getDate()+U;j=Math.ceil(W/7)}var B=g?10:y?1:0,Y=w?1:0,K=x||S?1:0,G=x||S?R:1,$=new Date(I-B,V-Y,G-K,E),Q=new Date(I+B,V+Y,G+K,E),X=g?new Date(10*Math.ceil(I/10)-9,0,0):y?new Date(I,0,0):w?new Date(I,V,0):new Date(I,V,R,-1),J=g?new Date(10*Math.ceil(I/10)+1,0,1):y?new Date(I+1,0,1):w?new Date(I,V+1,1):new Date(I,V,R+1),Z=c;w&&v.showWeekNumbers&&(Z+=" andweek");var _=e("<table/>").addClass(b.table).addClass(Z).addClass(p[q]+" column").appendTo(H);P&&_.addClass(b.inverted);var ee=q;if(!A){var te=e("<thead/>").appendTo(_);r=e("<tr/>").appendTo(te),s=e("<th/>").attr("colspan",""+q).appendTo(r);var ne=g||y?new Date(I,0,1):w?new Date(I,V,1):new Date(I,V,R,E,O),ie=e("<span/>").addClass(b.link).appendTo(s);ie.text(C.header(ne,c,v));var ae=y?v.disableYear?"day":"year":w?v.disableMonth?"year":"month":"day";if(ie.data(T.mode,ae),0===o){var oe=e("<span/>").addClass(b.prev).appendTo(s);oe.data(T.focusDate,$),oe.toggleClass(b.disabledCell,!h.helper.isDateInRange(X,c)),e("<i/>").addClass(b.prevIcon).appendTo(oe)}if(o===N-1){var re=e("<span/>").addClass(b.next).appendTo(s);re.data(T.focusDate,Q),re.toggleClass(b.disabledCell,!h.helper.isDateInRange(J,c)),e("<i/>").addClass(b.nextIcon).appendTo(re)}if(w)for(r=e("<tr/>").appendTo(te),v.showWeekNumbers&&((s=e("<th/>").appendTo(r)).text(v.text.weekNo),s.addClass(b.weekCell),ee--),t=0;t<ee;t++)(s=e("<th/>").appendTo(r)).text(C.dayColumnHeader((t+v.firstDayOfWeek)%7,v))}var se=e("<tbody/>").appendTo(_);for(t=g?10*Math.ceil(I/10)-9:w?1-U:0,n=0;n<j;n++)for(r=e("<tr/>").appendTo(se),w&&v.showWeekNumbers&&((s=e("<th/>").appendTo(r)).text(h.get.weekOfYear(I,V,t+1-v.firstDayOfWeek)),s.addClass(b.weekCell)),a=0;a<ee;a++,t++){var le=g?new Date(t,V,1,E,O):y?new Date(I,t,1,E,O):w?new Date(I,V,t,E,O):x?new Date(I,V,R,t):new Date(I,V,R,E,t*v.minTimeGap),ce=g?t:y?v.text.monthsShort[t]:w?le.getDate():C.time(le,v,!0);(s=e("<td/>").addClass(b.cell).appendTo(r)).text(ce),s.data(T.date,le);var ue=w&&le.getMonth()!==(V+12)%12,de=!v.selectAdjacentDays&&ue||!h.helper.isDateInRange(le,c)||v.isDisabled(le,c)||h.helper.isDisabled(le,c)||!h.helper.isEnabled(le,c);if(de){var fe=h.helper.findDayAsObject(le,c,v.disabledDates);null!==fe&&fe[T.message]&&(s.attr("data-tooltip",fe[T.message]),s.attr("data-position",fe[T.position]||z),(fe[T.inverted]||P&&fe[T.inverted]===i)&&s.attr("data-inverted",""),fe[T.variation]&&s.attr("data-variation",fe[T.variation]))}else{var me=h.helper.findDayAsObject(le,c,v.eventDates);null!==me&&(s.addClass(me[T["class"]]||v.eventClass),me[T.message]&&(s.attr("data-tooltip",me[T.message]),s.attr("data-position",me[T.position]||z),(me[T.inverted]||P&&me[T.inverted]===i)&&s.attr("data-inverted",""),me[T.variation]&&s.attr("data-variation",me[T.variation])))}var pe=h.helper.dateEqual(le,d,c),ge=h.helper.dateEqual(le,u,c);s.toggleClass(b.adjacentCell,ue),s.toggleClass(b.disabledCell,de),s.toggleClass(b.activeCell,pe&&!ue),x||S||s.toggleClass(b.todayCell,!ue&&ge);var he={mode:c,adjacent:ue,disabled:de,active:pe,today:ge};C.cell(s,le,he),h.helper.dateEqual(le,f,c)&&h.set.focusDate(le,!1,!1)}if(v.today){var ve=e("<tr/>").appendTo(se),be=e("<td/>").attr("colspan",""+q).addClass(b.today).appendTo(ve);be.text(C.today(v)),be.data(T.date,u)}h.update.focus(!1,_),v.inline&&h.refreshTooltips()}}},update:{focus:function(t,n){n=n||M;var i=h.get.mode(),a=h.get.date(),o=h.get.focusDate(),s=h.get.startDate(),l=h.get.endDate(),c=(t?o:null)||a||(r?null:o);n.find("td").each(function(){var t=e(this),n=t.data(T.date);if(n){var a=t.hasClass(b.disabledCell),u=t.hasClass(b.activeCell),d=t.hasClass(b.adjacentCell),f=h.helper.dateEqual(n,o,i),m=!!c&&(!!s&&h.helper.isDateInRange(n,i,s,c)||!!l&&h.helper.isDateInRange(n,i,c,l));t.toggleClass(b.focusCell,f&&(!r||I)&&(!d||v.selectAdjacentDays&&d)&&!a),h.helper.isTodayButton(t)||t.toggleClass(b.rangeCell,m&&!u&&!a)}})}},refresh:function(){h.create.calendar()},refreshTooltips:function(){var n=e(t).width();M.find("td[data-position]").each(function(){var i=e(this),a=t.getComputedStyle(i[0],":after").width.replace(/[^0-9\.]/g,""),o=i.attr("data-position"),r=n-i.width()-(parseInt(a,10)||250)>i.offset().left?"right":"left";-1===o.indexOf(r)&&i.attr("data-position",o.replace(/(left|right)/,r))})},bind:{events:function(){h.debug("Binding events"),M.on("mousedown"+A,h.event.mousedown),M.on("touchstart"+A,h.event.mousedown),M.on("mouseup"+A,h.event.mouseup),M.on("touchend"+A,h.event.mouseup),M.on("mouseover"+A,h.event.mouseover),O.length?(O.on("input"+A,h.event.inputChange),O.on("focus"+A,h.event.inputFocus),O.on("blur"+A,h.event.inputBlur),O.on("keydown"+A,h.event.keydown)):M.on("keydown"+A,h.event.keydown)}},unbind:{events:function(){h.debug("Unbinding events"),M.off(A),O.length&&O.off(A)}},event:{mouseover:function(t){var n=e(t.target).data(T.date),i=1===t.buttons;n&&h.set.focusDate(n,!1,!0,i)},mousedown:function(t){O.length&&t.preventDefault(),I=t.type.indexOf("touch")>=0;var n=e(t.target).data(T.date);n&&h.set.focusDate(n,!1,!0,!0)},mouseup:function(t){h.focus(),t.preventDefault(),t.stopPropagation(),I=!1;var n=e(t.target);if(!n.hasClass("disabled")){var i=n.parent();(i.data(T.date)||i.data(T.focusDate)||i.data(T.mode))&&(n=i);var a=n.data(T.date),o=n.data(T.focusDate),r=n.data(T.mode);if(a&&!1!==v.onSelect.call(R,a,h.get.mode())){var s=n.hasClass(b.today);h.selectDate(a,s)}else o?h.set.focusDate(o):r&&h.set.mode(r)}},keydown:function(e){var t=e.which;if(27!==t&&9!==t||h.popup("hide"),h.popup("is visible"))if(37===t||38===t||39===t||40===t){var n="day"===(d=h.get.mode())?7:"hour"===d?4:"minute"===d?D.column:3,i=37===t?-1:38===t?-n:39==t?1:n;i*="minute"===d?v.minTimeGap:1;var a=h.get.focusDate()||h.get.date()||new Date,o=a.getFullYear()+("year"===d?i:0),r=a.getMonth()+("month"===d?i:0),s=a.getDate()+("day"===d?i:0),l=a.getHours()+("hour"===d?i:0),c=a.getMinutes()+("minute"===d?i:0),u=new Date(o,r,s,l,c);"time"===v.type&&(u=h.helper.mergeDateTime(a,u)),h.helper.isDateInRange(u,d)&&h.set.focusDate(u)}else if(13===t){var d=h.get.mode(),f=h.get.focusDate();f&&!v.isDisabled(f,d)&&!h.helper.isDisabled(f,d)&&h.helper.isEnabled(f,d)&&h.selectDate(f),e.preventDefault(),e.stopPropagation()}38!==t&&40!==t||(e.preventDefault(),h.popup("show"))},inputChange:function(){var e=O.val(),t=x.date(e,v);h.set.date(t,!1)},inputFocus:function(){M.addClass(b.active)},inputBlur:function(){if(M.removeClass(b.active),v.formatInput){var e=h.get.date(),t=C.datetime(e,v);O.val(t)}j&&(h.trigger.change(),j=!1)},"class":{mutation:function(e){e.forEach(function(e){"class"===e.attributeName&&h.check.disabled()})}}},observeChanges:function(){"MutationObserver"in t&&(g=new MutationObserver(h.event["class"].mutation),h.debug("Setting up mutation observer",g),h.observe["class"]())},disconnect:{classObserver:function(){O.length&&g&&g.disconnect()}},observe:{"class":function(){O.length&&g&&g.observe(F[0],{attributes:!0})}},is:{disabled:function(){return F.hasClass(b.disabled)}},check:{disabled:function(){O.attr("tabindex",h.is.disabled()?-1:0)}},get:{weekOfYear:function(e,t,n){var i,a,o,r=864e5,s=7*r;return i=Date.UTC(e,t,n+3)/r,a=Math.floor(i/7),o=new Date(a*s).getUTCFullYear(),a-Math.floor(Date.UTC(o,0,7)/s)+1},date:function(){return h.helper.sanitiseDate(F.data(T.date))||null},inputDate:function(){return O.val()},focusDate:function(){return F.data(T.focusDate)||null},startDate:function(){var e=h.get.calendarModule(v.startCalendar);return(e?e.get.date():F.data(T.startDate))||null},endDate:function(){var e=h.get.calendarModule(v.endCalendar);return(e?e.get.date():F.data(T.endDate))||null},minDate:function(){return F.data(T.minDate)||null},maxDate:function(){return F.data(T.maxDate)||null},monthOffset:function(){return F.data(T.monthOffset)||0},mode:function(){var e=F.data(T.mode)||v.startMode;return h.get.validatedMode(e)},validatedMode:function(t){var n=h.get.validModes();return e.inArray(t,n)>=0?t:"time"===v.type?"hour":"month"===v.type?"month":"year"===v.type?"year":"day"},type:function(){return F.data(T.type)||v.type},validModes:function(){var e=[];return"time"!==v.type&&(v.disableYear&&"year"!==v.type||e.push("year"),(!v.disableMonth&&"year"!==v.type||"month"===v.type)&&e.push("month"),v.type.indexOf("date")>=0&&e.push("day")),v.type.indexOf("time")>=0&&(e.push("hour"),v.disableMinute||e.push("minute")),e},isTouch:function(){try{return n.createEvent("TouchEvent"),!0}catch(e){return!1}},calendarModule:function(t){return t?(t instanceof e||(t=e(t).first()),t.data(k)):null}},set:{date:function(e,t,n){t=!1!==t,n=!1!==n,e=h.helper.sanitiseDate(e),e=h.helper.dateInRange(e);var a=h.get.mode(),o=C.datetime(e,v);if(n&&!1===v.onBeforeChange.call(R,e,o,a))return!1;if(h.set.focusDate(e),v.isDisabled(e,a))return!1;var r=h.get.endDate();r&&e&&e>r&&h.set.endDate(i),h.set.dataKeyValue(T.date,e),t&&O.length&&O.val(o),n&&v.onChange.call(R,e,o,a)},startDate:function(e,t){e=h.helper.sanitiseDate(e);var n=h.get.calendarModule(v.startCalendar);n&&n.set.date(e),h.set.dataKeyValue(T.startDate,e,t)},endDate:function(e,t){e=h.helper.sanitiseDate(e);var n=h.get.calendarModule(v.endCalendar);n&&n.set.date(e),h.set.dataKeyValue(T.endDate,e,t)},focusDate:function(e,t,n,i){e=h.helper.sanitiseDate(e),e=h.helper.dateInRange(e);var a="day"===h.get.mode(),o=h.get.focusDate();if(a&&e&&o){var r=12*(e.getFullYear()-o.getFullYear())+e.getMonth()-o.getMonth();if(r){var s=h.get.monthOffset()-r;h.set.monthOffset(s,!1)}}var l=h.set.dataKeyValue(T.focusDate,e,!!e&&t);n=!1!==n&&l&&!1===t||q!=i,q=i,n&&h.update.focus(i)},minDate:function(e){e=h.helper.sanitiseDate(e),null!==v.maxDate&&v.maxDate<=e?h.verbose("Unable to set minDate variable bigger that maxDate variable",e,v.maxDate):(h.setting("minDate",e),h.set.dataKeyValue(T.minDate,e))},maxDate:function(e){e=h.helper.sanitiseDate(e),null!==v.minDate&&v.minDate>=e?h.verbose("Unable to set maxDate variable lower that minDate variable",e,v.minDate):(h.setting("maxDate",e),h.set.dataKeyValue(T.maxDate,e))},monthOffset:function(e,t){var n=Math.max(v.multiMonth,1);e=Math.max(1-n,Math.min(0,e)),h.set.dataKeyValue(T.monthOffset,e,t)},mode:function(e,t){h.set.dataKeyValue(T.mode,e,t)},dataKeyValue:function(e,t,n){var i=F.data(e),a=i===t||i<=t&&i>=t;return t?F.data(e,t):F.removeData(e),(n=!1!==n&&!a)&&h.refresh(),!a}},selectDate:function(e,t){h.verbose("New date selection",e);var n=h.get.mode();if(t||"minute"===n||v.disableMinute&&"hour"===n||"date"===v.type&&"day"===n||"month"===v.type&&"month"===n||"year"===v.type&&"year"===n){if(!(!1===h.set.date(e))&&(j=!0,v.closable)){h.popup("hide");var i=h.get.calendarModule(v.endCalendar);i&&("focus"!==i.setting("on")&&i.popup("show"),i.focus())}}else{var a="year"===n?v.disableMonth?"day":"month":"month"===n?"day":"day"===n?"hour":"minute";h.set.mode(a),"hour"===n||"day"===n&&h.get.date()?h.set.date(e,!0,!1):h.set.focusDate(e)}},changeDate:function(e){h.set.date(e)},clear:function(){h.set.date(i)},popup:function(){return E.popup.apply(E,arguments)},focus:function(){O.length?O.focus():M.focus()},blur:function(){O.length?O.blur():M.blur()},helper:{isDisabled:function(e,t){return("day"===t||"month"===t||"year"===t)&&(-1!==v.disabledDaysOfWeek.indexOf(e.getDay())||v.disabledDates.some(function(n){if("string"==typeof n&&(n=h.helper.sanitiseDate(n)),n instanceof Date)return h.helper.dateEqual(e,n,t);if(null!==n&&"object"==typeof n)if(n[T.year]){if("number"==typeof n[T.year])return e.getFullYear()==n[T.year];if(Array.isArray(n[T.year]))return n[T.year].indexOf(e.getFullYear())>-1}else if(n[T.month]){if("number"==typeof n[T.month])return e.getMonth()==n[T.month];if(Array.isArray(n[T.month]))return n[T.month].indexOf(e.getMonth())>-1;if(n[T.month]instanceof Date){var i=h.helper.sanitiseDate(n[T.month]);return e.getMonth()==i.getMonth()&&e.getFullYear()==i.getFullYear()}}else if(n[T.date]&&"day"===t){if(n[T.date]instanceof Date)return h.helper.dateEqual(e,h.helper.sanitiseDate(n[T.date]),t);if(Array.isArray(n[T.date]))return n[T.date].some(function(n){return h.helper.dateEqual(e,n,t)})}}))},isEnabled:function(e,t){return"day"!==t||(0===v.enabledDates.length||v.enabledDates.some(function(n){return"string"==typeof n&&(n=h.helper.sanitiseDate(n)),n instanceof Date?h.helper.dateEqual(e,n,t):null!==n&&"object"==typeof n&&n[T.date]?h.helper.dateEqual(e,h.helper.sanitiseDate(n[T.date]),t):void 0}))},findDayAsObject:function(e,t,n){if("day"===t||"month"===t||"year"===t)for(var i,a=0;a<n.length;a++){if("string"==typeof(i=n[a])&&(i=h.helper.sanitiseDate(i)),i instanceof Date&&h.helper.dateEqual(e,i,t)){var o={};return o[T.date]=i,o}if(null!==i&&"object"==typeof i)if(i[T.year]){if("number"==typeof i[T.year]&&e.getFullYear()==i[T.year])return i;if(Array.isArray(i[T.year])&&i[T.year].indexOf(e.getFullYear())>-1)return i}else if(i[T.month]){if("number"==typeof i[T.month]&&e.getMonth()==i[T.month])return i;if(Array.isArray(i[T.month])){if(i[T.month].indexOf(e.getMonth())>-1)return i}else if(i[T.month]instanceof Date){var r=h.helper.sanitiseDate(i[T.month]);if(e.getMonth()==r.getMonth()&&e.getFullYear()==r.getFullYear())return i}}else if(i[T.date]&&"day"===t){if(i[T.date]instanceof Date&&h.helper.dateEqual(e,h.helper.sanitiseDate(i[T.date]),t))return i;if(Array.isArray(i[T.date])&&i[T.date].some(function(n){return h.helper.dateEqual(e,n,t)}))return i}}return null},sanitiseDate:function(e){return e?(e instanceof Date||(e=x.date(""+e,v)),!e||null===e||isNaN(e.getTime())?i:e):i},dateDiff:function(e,t,n){n=n||"day";var i="time"===v.type,a="year"===n,o=a||"month"===n,r="minute"===n,s=r||"hour"===n;return e=new Date(i?2e3:e.getFullYear(),i?0:a?0:e.getMonth(),i?1:o?1:e.getDate(),s?e.getHours():0,r?v.minTimeGap*Math.floor(e.getMinutes()/v.minTimeGap):0),(t=new Date(i?2e3:t.getFullYear(),i?0:a?0:t.getMonth(),i?1:o?1:t.getDate(),s?t.getHours():0,r?v.minTimeGap*Math.floor(t.getMinutes()/v.minTimeGap):0)).getTime()-e.getTime()},dateEqual:function(e,t,n){return!!e&&!!t&&0===h.helper.dateDiff(e,t,n)},isDateInRange:function(e,t,n,i){if(!n&&!i){var a=h.get.startDate();n=a&&v.minDate?new Date(Math.max(a,v.minDate)):a||v.minDate,i=v.maxDate}return n=n&&new Date(n.getFullYear(),n.getMonth(),n.getDate(),n.getHours(),v.minTimeGap*Math.ceil(n.getMinutes()/v.minTimeGap)),!(!e||n&&h.helper.dateDiff(e,n,t)>0||i&&h.helper.dateDiff(i,e,t)>0)},dateInRange:function(e,t,n){if(!t&&!n){var i=h.get.startDate();t=i&&v.minDate?new Date(Math.max(i,v.minDate)):i||v.minDate,n=v.maxDate}t=t&&new Date(t.getFullYear(),t.getMonth(),t.getDate(),t.getHours(),v.minTimeGap*Math.ceil(t.getMinutes()/v.minTimeGap));var a="time"===v.type;return e?t&&h.helper.dateDiff(e,t,"minute")>0?a?h.helper.mergeDateTime(e,t):t:n&&h.helper.dateDiff(n,e,"minute")>0?a?h.helper.mergeDateTime(e,n):n:e:e},mergeDateTime:function(e,t){return e&&t?new Date(e.getFullYear(),e.getMonth(),e.getDate(),t.getHours(),t.getMinutes()):t},isTodayButton:function(e){return e.text()===v.text.today}},setting:function(t,n){if(h.debug("Changing setting",t,n),e.isPlainObject(t))e.extend(!0,v,t);else{if(n===i)return v[t];e.isPlainObject(v[t])?e.extend(!0,v[t],n):v[t]=n}},internal:function(t,n){if(e.isPlainObject(t))e.extend(!0,h,t);else{if(n===i)return h[t];h[t]=n}},debug:function(){!v.silent&&v.debug&&(v.performance?h.performance.log(arguments):(h.debug=Function.prototype.bind.call(console.info,console,v.name+":"),h.debug.apply(console,arguments)))},verbose:function(){!v.silent&&v.verbose&&v.debug&&(v.performance?h.performance.log(arguments):(h.verbose=Function.prototype.bind.call(console.info,console,v.name+":"),h.verbose.apply(console,arguments)))},error:function(){v.silent||(h.error=Function.prototype.bind.call(console.error,console,v.name+":"),h.error.apply(console,arguments))},performance:{log:function(e){var t,n;v.performance&&(n=(t=(new Date).getTime())-(l||t),l=t,c.push({Name:e[0],Arguments:[].slice.call(e,1)||"",Element:R,"Execution Time":n})),clearTimeout(h.performance.timer),h.performance.timer=setTimeout(h.performance.display,500)},display:function(){var t=v.name+":",n=0;l=!1,clearTimeout(h.performance.timer),e.each(c,function(e,t){n+=t["Execution Time"]}),t+=" "+n+"ms",s&&(t+=" '"+s+"'"),(console.group!==i||console.table!==i)&&c.length>0&&(console.groupCollapsed(t),console.table?console.table(c):e.each(c,function(e,t){console.log(t.Name+": "+t["Execution Time"]+"ms")}),console.groupEnd()),c=[]}},invoke:function(t,n,a){var r,s,l,c=L;return n=n||f,a=R||a,"string"==typeof t&&c!==i&&(t=t.split(/[\. ]/),r=t.length-1,e.each(t,function(n,a){var o=n!=r?a+t[n+1].charAt(0).toUpperCase()+t[n+1].slice(1):t;if(e.isPlainObject(c[o])&&n!=r)c=c[o];else{if(c[o]!==i)return s=c[o],!1;if(!e.isPlainObject(c[a])||n==r)return c[a]!==i?(s=c[a],!1):(h.error(S.method,t),!1);c=c[a]}})),e.isFunction(s)?l=s.apply(a,n):s!==i&&(l=s),Array.isArray(o)?o.push(l):o!==i?o=[o,l]:l!==i&&(o=l),s}},d?(L===i&&h.initialize(),h.invoke(u)):(L!==i&&L.invoke("destroy"),h.initialize())}),o!==i?o:this},e.fn.calendar.settings={name:"Calendar",namespace:"calendar",silent:!1,debug:!1,verbose:!1,performance:!1,type:"datetime",firstDayOfWeek:0,constantHeight:!0,today:!1,closable:!0,monthFirst:!0,touchReadonly:!0,inline:!1,on:null,initialDate:null,startMode:!1,minDate:null,maxDate:null,ampm:!0,disableYear:!1,disableMonth:!1,disableMinute:!1,formatInput:!0,startCalendar:null,endCalendar:null,multiMonth:1,minTimeGap:5,showWeekNumbers:null,disabledDates:[],disabledDaysOfWeek:[],enabledDates:[],eventDates:[],centuryBreak:60,currentCentury:2e3,selectAdjacentDays:!1,popupOptions:{position:"bottom left",lastResort:"bottom left",prefer:"opposite",hideOnScroll:!1},text:{days:["S","M","T","W","T","F","S"],months:["January","February","March","April","May","June","July","August","September","October","November","December"],monthsShort:["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"],today:"Today",now:"Now",am:"AM",pm:"PM",weekNo:"Week"},formatter:{header:function(e,t,n){return"year"===t?n.formatter.yearHeader(e,n):"month"===t?n.formatter.monthHeader(e,n):"day"===t?n.formatter.dayHeader(e,n):"hour"===t?n.formatter.hourHeader(e,n):n.formatter.minuteHeader(e,n)},yearHeader:function(e){var t=10*Math.ceil(e.getFullYear()/10);return t-9+" - "+(t+2)},monthHeader:function(e){return e.getFullYear()},dayHeader:function(e,t){return t.text.months[e.getMonth()]+" "+e.getFullYear()},hourHeader:function(e,t){return t.formatter.date(e,t)},minuteHeader:function(e,t){return t.formatter.date(e,t)},dayColumnHeader:function(e,t){return t.text.days[e]},datetime:function(e,t){if(!e)return"";var n="time"===t.type?"":t.formatter.date(e,t),i=t.type.indexOf("time")<0?"":t.formatter.time(e,t,!1);return n+("datetime"===t.type?" ":"")+i},date:function(e,t){if(!e)return"";var n=e.getDate(),i=t.text.months[e.getMonth()],a=e.getFullYear();return"year"===t.type?a:"month"===t.type?i+" "+a:(t.monthFirst?i+" "+n:n+" "+i)+", "+a},time:function(e,t){if(!e)return"";var n=e.getHours(),i=e.getMinutes(),a="";return t.ampm&&(a=" "+(n<12?t.text.am:t.text.pm),n=0===n?12:n>12?n-12:n),n+":"+(i<10?"0":"")+i+a},today:function(e){return"date"===e.type?e.text.today:e.text.now},cell:function(){}},parser:{date:function(t,n){if(t instanceof Date)return t;if(!t)return null;if(0===(t=String(t).trim()).length)return null;t.match(/^[0-9]{4}[\/\-\.][0-9]{2}[\/\-\.][0-9]{2}$/)&&(t=t.replace(/[\/\-\.]/g,"/")+" 00:00:00"),t=n.monthFirst||!t.match(/^[0-9]{2}[\/\-\.]/)?t:t.replace(/[\/\-\.]/g,"/").replace(/([0-9]+)\/([0-9]+)/,"$2/$1");var a,o,r,s=new Date(t);if(!(null!==t.match(/^[0-9]+$/))&&!isNaN(s.getDate()))return s;t=t.toLowerCase();var l,c,u,d=-1,f=-1,m=-1,p=-1,g=-1,h=i,v="time"===n.type,b=n.type.indexOf("time")<0,y=t.split(n.regExp.dateWords),w=t.split(n.regExp.dateNumbers);if(!b)for(h=e.inArray(n.text.am.toLowerCase(),y)>=0||!(e.inArray(n.text.pm.toLowerCase(),y)>=0)&&i,a=0;a<w.length;a++)if((c=w[a]).indexOf(":")>=0){if(f<0||d<0)for(u=c.split(":"),r=0;r<Math.min(2,u.length);r++)o=parseInt(u[r]),isNaN(o)&&(o=0),0===r?f=o%24:d=o%60;w.splice(a,1)}if(!v){for(a=0;a<y.length;a++)if(!((l=y[a]).length<=0)){for(o=0;o<n.text.months.length;o++)if(n.text.months[o].substring(0,l.length).toLowerCase()===l){p=o+1;break}if(p>=0)break}for(a=0;a<w.length;a++)if(o=parseInt(w[a]),!isNaN(o)&&o>=n.centuryBreak&&a===w.length-1){o<=99&&(o+=n.currentCentury-100),g=o,w.splice(a,1);break}if(p<0)for(a=0;a<w.length;a++)if(r=a>1||n.monthFirst?a:1===a?0:1,o=parseInt(w[r]),!isNaN(o)&&1<=o&&o<=12){p=o,w.splice(r,1);break}for(a=0;a<w.length;a++)if(o=parseInt(w[a]),!isNaN(o)&&1<=o&&o<=31){m=o,w.splice(a,1);break}if(g<0)for(a=w.length-1;a>=0;a--)if(o=parseInt(w[a]),!isNaN(o)){o<=99&&(o+=n.currentCentury),g=o,w.splice(a,1);break}}if(!b){if(f<0)for(a=0;a<w.length;a++)if(o=parseInt(w[a]),!isNaN(o)&&0<=o&&o<=23){f=o,w.splice(a,1);break}if(d<0)for(a=0;a<w.length;a++)if(o=parseInt(w[a]),!isNaN(o)&&0<=o&&o<=59){d=o,w.splice(a,1);break}}if(d<0&&f<0&&m<0&&p<0&&g<0)return null;d<0&&(d=0),f<0&&(f=0),m<0&&(m=1),p<0&&(p=1),g<0&&(g=(new Date).getFullYear()),h!==i&&(h?12===f&&(f=0):f<12&&(f+=12));var C=new Date(g,p-1,m,f,d);return C.getMonth()===p-1&&C.getFullYear()===g||(C=new Date(g,p,0,f,d)),isNaN(C.getTime())?null:C}},onBeforeChange:function(){return!0},onChange:function(){},onShow:function(){},onVisible:function(){},onHide:function(){},onHidden:function(){},onSelect:function(){},isDisabled:function(){return!1},selector:{popup:".ui.popup",input:"input",activator:"input",append:".inline.field,.inline.fields"},regExp:{dateWords:/[^A-Za-z\u00C0-\u024F]+/g,dateNumbers:/[^\d:]+/g},error:{popup:"UI Popup, a required component is not included in this page",method:"The method you called is not defined."},className:{calendar:"calendar",active:"active",popup:"ui popup",grid:"ui equal width grid",column:"column",table:"ui celled center aligned unstackable table",inverted:"inverted",prev:"prev link",next:"next link",prevIcon:"chevron left icon",nextIcon:"chevron right icon",link:"link",cell:"link",disabledCell:"disabled",weekCell:"disabled",adjacentCell:"adjacent",activeCell:"active",rangeCell:"range",focusCell:"focus",todayCell:"today",today:"today link",disabled:"disabled"},metadata:{date:"date",focusDate:"focusDate",startDate:"startDate",endDate:"endDate",minDate:"minDate",maxDate:"maxDate",mode:"mode",type:"type",monthOffset:"monthOffset",message:"message","class":"class",inverted:"inverted",variation:"variation",position:"position",month:"month",year:"year"},eventClass:"blue"}}(jQuery,window,document),function(e,t,n,i){"use strict";e.isFunction=e.isFunction||function(e){return"function"==typeof e&&"number"!=typeof e.nodeType},t=void 0!==t&&t.Math==Math?t:"undefined"!=typeof self&&self.Math==Math?self:Function("return this")(),e.fn.accordion=function(n){var a,o=e(this),r=(new Date).getTime(),s=[],l=arguments[0],c="string"==typeof l,u=[].slice.call(arguments,1);return o.each(function(){var d,f,m=e.isPlainObject(n)?e.extend(!0,{},e.fn.accordion.settings,n):e.extend({},e.fn.accordion.settings),p=m.className,g=m.namespace,h=m.selector,v=m.error,b="."+g,y="module-"+g,w=o.selector||"",C=e(this),x=C.find(h.title),T=C.find(h.content),D=this,S=C.data(y);f={initialize:function(){f.debug("Initializing",C),f.bind.events(),m.observeChanges&&f.observeChanges(),f.instantiate()},instantiate:function(){S=f,C.data(y,f)},destroy:function(){f.debug("Destroying previous instance",C),C.off(b).removeData(y)},refresh:function(){x=C.find(h.title),T=C.find(h.content)},observeChanges:function(){"MutationObserver"in t&&((d=new MutationObserver(function(){f.debug("DOM tree modified, updating selector cache"),f.refresh()})).observe(D,{childList:!0,subtree:!0}),f.debug("Setting up mutation observer",d))},bind:{events:function(){f.debug("Binding delegated events"),C.on(m.on+b,h.trigger,f.event.click)}},event:{click:function(){f.toggle.call(this)}},toggle:function(t){var n=t!==i?"number"==typeof t?x.eq(t):e(t).closest(h.title):e(this).closest(h.title),a=n.next(T),o=a.hasClass(p.animating),r=a.hasClass(p.active),s=r&&!o,l=!r&&o;f.debug("Toggling visibility of content",n),s||l?m.collapsible?f.close.call(n):f.debug("Cannot close accordion content collapsing is disabled"):f.open.call(n)},open:function(t){var n=t!==i?"number"==typeof t?x.eq(t):e(t).closest(h.title):e(this).closest(h.title),a=n.next(T),o=a.hasClass(p.animating);a.hasClass(p.active)||o?f.debug("Accordion already open, skipping",a):(f.debug("Opening accordion content",n),m.onOpening.call(a),m.onChanging.call(a),m.exclusive&&f.closeOthers.call(n),n.addClass(p.active),a.stop(!0,!0).addClass(p.animating),m.animateChildren&&(e.fn.transition!==i&&C.transition("is supported")?a.children().transition({animation:"fade in",queue:!1,useFailSafe:!0,debug:m.debug,verbose:m.verbose,duration:m.duration,skipInlineHidden:!0,onComplete:function(){a.children().removeClass(p.transition)}}):a.children().stop(!0,!0).animate({opacity:1},m.duration,f.resetOpacity)),a.slideDown(m.duration,m.easing,function(){a.removeClass(p.animating).addClass(p.active),f.reset.display.call(this),m.onOpen.call(this),m.onChange.call(this)}))},close:function(t){var n=t!==i?"number"==typeof t?x.eq(t):e(t).closest(h.title):e(this).closest(h.title),a=n.next(T),o=a.hasClass(p.animating),r=a.hasClass(p.active);!r&&!(!r&&o)||r&&o||(f.debug("Closing accordion content",a),m.onClosing.call(a),m.onChanging.call(a),n.removeClass(p.active),a.stop(!0,!0).addClass(p.animating),m.animateChildren&&(e.fn.transition!==i&&C.transition("is supported")?a.children().transition({animation:"fade out",queue:!1,useFailSafe:!0,debug:m.debug,verbose:m.verbose,duration:m.duration,skipInlineHidden:!0}):a.children().stop(!0,!0).animate({opacity:0},m.duration,f.resetOpacity)),a.slideUp(m.duration,m.easing,function(){a.removeClass(p.animating).removeClass(p.active),f.reset.display.call(this),m.onClose.call(this),m.onChange.call(this)}))},closeOthers:function(t){var n,a,o,r=t!==i?x.eq(t):e(this).closest(h.title),s=r.parents(h.content).prev(h.title),l=r.closest(h.accordion),c=h.title+"."+p.active+":visible",u=h.content+"."+p.active+":visible";m.closeNested?o=(n=l.find(c).not(s)).next(T):(n=l.find(c).not(s),a=l.find(u).find(c).not(s),
o=(n=n.not(a)).next(T)),n.length>0&&(f.debug("Exclusive enabled, closing other content",n),n.removeClass(p.active),o.removeClass(p.animating).stop(!0,!0),m.animateChildren&&(e.fn.transition!==i&&C.transition("is supported")?o.children().transition({animation:"fade out",useFailSafe:!0,debug:m.debug,verbose:m.verbose,duration:m.duration,skipInlineHidden:!0}):o.children().stop(!0,!0).animate({opacity:0},m.duration,f.resetOpacity)),o.slideUp(m.duration,m.easing,function(){e(this).removeClass(p.active),f.reset.display.call(this)}))},reset:{display:function(){f.verbose("Removing inline display from element",this),e(this).css("display",""),""===e(this).attr("style")&&e(this).attr("style","").removeAttr("style")},opacity:function(){f.verbose("Removing inline opacity from element",this),e(this).css("opacity",""),""===e(this).attr("style")&&e(this).attr("style","").removeAttr("style")}},setting:function(t,n){if(f.debug("Changing setting",t,n),e.isPlainObject(t))e.extend(!0,m,t);else{if(n===i)return m[t];e.isPlainObject(m[t])?e.extend(!0,m[t],n):m[t]=n}},internal:function(t,n){if(f.debug("Changing internal",t,n),n===i)return f[t];e.isPlainObject(t)?e.extend(!0,f,t):f[t]=n},debug:function(){!m.silent&&m.debug&&(m.performance?f.performance.log(arguments):(f.debug=Function.prototype.bind.call(console.info,console,m.name+":"),f.debug.apply(console,arguments)))},verbose:function(){!m.silent&&m.verbose&&m.debug&&(m.performance?f.performance.log(arguments):(f.verbose=Function.prototype.bind.call(console.info,console,m.name+":"),f.verbose.apply(console,arguments)))},error:function(){m.silent||(f.error=Function.prototype.bind.call(console.error,console,m.name+":"),f.error.apply(console,arguments))},performance:{log:function(e){var t,n;m.performance&&(n=(t=(new Date).getTime())-(r||t),r=t,s.push({Name:e[0],Arguments:[].slice.call(e,1)||"",Element:D,"Execution Time":n})),clearTimeout(f.performance.timer),f.performance.timer=setTimeout(f.performance.display,500)},display:function(){var t=m.name+":",n=0;r=!1,clearTimeout(f.performance.timer),e.each(s,function(e,t){n+=t["Execution Time"]}),t+=" "+n+"ms",w&&(t+=" '"+w+"'"),(console.group!==i||console.table!==i)&&s.length>0&&(console.groupCollapsed(t),console.table?console.table(s):e.each(s,function(e,t){console.log(t.Name+": "+t["Execution Time"]+"ms")}),console.groupEnd()),s=[]}},invoke:function(t,n,o){var r,s,l,c=S;return n=n||u,o=D||o,"string"==typeof t&&c!==i&&(t=t.split(/[\. ]/),r=t.length-1,e.each(t,function(n,a){var o=n!=r?a+t[n+1].charAt(0).toUpperCase()+t[n+1].slice(1):t;if(e.isPlainObject(c[o])&&n!=r)c=c[o];else{if(c[o]!==i)return s=c[o],!1;if(!e.isPlainObject(c[a])||n==r)return c[a]!==i?(s=c[a],!1):(f.error(v.method,t),!1);c=c[a]}})),e.isFunction(s)?l=s.apply(o,n):s!==i&&(l=s),Array.isArray(a)?a.push(l):a!==i?a=[a,l]:l!==i&&(a=l),s}},c?(S===i&&f.initialize(),f.invoke(l)):(S!==i&&S.invoke("destroy"),f.initialize())}),a!==i?a:this},e.fn.accordion.settings={name:"Accordion",namespace:"accordion",silent:!1,debug:!1,verbose:!1,performance:!0,on:"click",observeChanges:!0,exclusive:!0,collapsible:!0,closeNested:!1,animateChildren:!0,duration:350,easing:"easeOutQuad",onOpening:function(){},onClosing:function(){},onChanging:function(){},onOpen:function(){},onClose:function(){},onChange:function(){},error:{method:"The method you called is not defined"},className:{active:"active",animating:"animating",transition:"transition"},selector:{accordion:".accordion",title:".title",trigger:".title",content:".content"}},e.extend(e.easing,{easeOutQuad:function(e,t,n,i,a){return-i*(t/=a)*(t-2)+n}})}(jQuery,window,document),function(e,t,n,i){"use strict";e.isFunction=e.isFunction||function(e){return"function"==typeof e&&"number"!=typeof e.nodeType},t=void 0!==t&&t.Math==Math?t:"undefined"!=typeof self&&self.Math==Math?self:Function("return this")(),e.fn.modal=function(a){var o,r=e(this),s=e(t),l=e(n),c=e("body"),u=r.selector||"",d=(new Date).getTime(),f=[],m=arguments[0],p="string"==typeof m,g=[].slice.call(arguments,1),h=t.requestAnimationFrame||t.mozRequestAnimationFrame||t.webkitRequestAnimationFrame||t.msRequestAnimationFrame||function(e){setTimeout(e,0)};return r.each(function(){var r,v,b,y,w,C,x,T,D,S,A,k=e.isPlainObject(a)?e.extend(!0,{},e.fn.modal.settings,a):e.extend({},e.fn.modal.settings),F=k.selector,O=k.className,M=k.namespace,E=k.error,R="."+M,L="module-"+M,I=e(this),P=e(k.context),q=I.find(F.close),j=this,N=I.data(L),H=!1,z="",V="";A={initialize:function(){A.cache={},A.verbose("Initializing dimmer",P),A.create.id(),A.create.dimmer(),k.allowMultiple&&A.create.innerDimmer(),k.centered||I.addClass("top aligned"),A.refreshModals(),A.bind.events(),k.observeChanges&&A.observeChanges(),A.instantiate()},instantiate:function(){A.verbose("Storing instance of modal"),N=A,I.data(L,N)},create:{dimmer:function(){var t={debug:k.debug,dimmerName:"modals"},n=e.extend(!0,t,k.dimmerSettings);e.fn.dimmer!==i?(A.debug("Creating dimmer"),y=P.dimmer(n),k.detachable?(A.verbose("Modal is detachable, moving content into dimmer"),y.dimmer("add content",I)):A.set.undetached(),w=y.dimmer("get dimmer")):A.error(E.dimmer)},id:function(){D=(Math.random().toString(16)+"000000000").substr(2,8),T="."+D,A.verbose("Creating unique id for element",D)},innerDimmer:function(){0==I.find(F.dimmer).length&&I.prepend('<div class="ui inverted dimmer"></div>')}},destroy:function(){S&&S.disconnect(),A.verbose("Destroying previous modal"),I.removeData(L).off(R),s.off(T),w.off(T),q.off(R),P.dimmer("destroy")},observeChanges:function(){"MutationObserver"in t&&((S=new MutationObserver(function(){A.debug("DOM tree modified, refreshing"),A.refresh()})).observe(j,{childList:!0,subtree:!0}),A.debug("Setting up mutation observer",S))},refresh:function(){A.remove.scrolling(),A.cacheSizes(),A.can.useFlex()||A.set.modalOffset(),A.set.screenHeight(),A.set.type()},refreshModals:function(){v=I.siblings(F.modal),r=v.add(I)},attachEvents:function(t,n){var i=e(t);n=e.isFunction(A[n])?A[n]:A.toggle,i.length>0?(A.debug("Attaching modal events to element",t,n),i.off(R).on("click"+R,n)):A.error(E.notFound,t)},bind:{events:function(){A.verbose("Attaching events"),I.on("click"+R,F.close,A.event.close).on("click"+R,F.approve,A.event.approve).on("click"+R,F.deny,A.event.deny),s.on("resize"+T,A.event.resize)},scrollLock:function(){y.get(0).addEventListener("touchmove",A.event.preventScroll,{passive:!1})}},unbind:{scrollLock:function(){y.get(0).removeEventListener("touchmove",A.event.preventScroll,{passive:!1})}},get:{id:function(){return(Math.random().toString(16)+"000000000").substr(2,8)}},event:{approve:function(){H||!1===k.onApprove.call(j,e(this))?A.verbose("Approve callback returned false cancelling hide"):(H=!0,A.hide(function(){H=!1}))},preventScroll:function(e){-1!==e.target.className.indexOf("dimmer")&&e.preventDefault()},deny:function(){H||!1===k.onDeny.call(j,e(this))?A.verbose("Deny callback returned false cancelling hide"):(H=!0,A.hide(function(){H=!1}))},close:function(){A.hide()},mousedown:function(n){var i=e(n.target),a=A.is.rtl();(C=i.closest(F.modal).length>0)&&A.verbose("Mouse down event registered inside the modal"),(x=A.is.scrolling()&&(!a&&e(t).outerWidth()-k.scrollbarWidth<=n.clientX||a&&k.scrollbarWidth>=n.clientX))&&A.verbose("Mouse down event registered inside the scrollbar")},mouseup:function(t){if(k.closable)if(C)A.debug("Dimmer clicked but mouse down was initially registered inside the modal");else if(x)A.debug("Dimmer clicked but mouse down was initially registered inside the scrollbar");else{var i=e(t.target).closest(F.modal).length>0,a=e.contains(n.documentElement,t.target);if(!i&&a&&A.is.active()&&I.hasClass(O.front)){if(A.debug("Dimmer clicked, hiding all modals"),k.allowMultiple){if(!A.hideAll())return}else if(!A.hide())return;A.remove.clickaway()}}else A.verbose("Dimmer clicked but closable setting is disabled")},debounce:function(e,t){clearTimeout(A.timer),A.timer=setTimeout(e,t)},keyboard:function(e){e.which==27&&(k.closable?(A.debug("Escape key pressed hiding modal"),I.hasClass(O.front)&&A.hide()):A.debug("Escape key pressed, but closable is set to false"),e.preventDefault())},resize:function(){y.dimmer("is active")&&(A.is.animating()||A.is.active())&&h(A.refresh)}},toggle:function(){A.is.active()||A.is.animating()?A.hide():A.show()},show:function(t){t=e.isFunction(t)?t:function(){},A.refreshModals(),A.set.dimmerSettings(),A.set.dimmerStyles(),A.showModal(t)},hide:function(t){return t=e.isFunction(t)?t:function(){},A.refreshModals(),A.hideModal(t)},showModal:function(t){t=e.isFunction(t)?t:function(){},A.is.animating()||!A.is.active()?(A.showDimmer(),A.cacheSizes(),A.set.bodyMargin(),A.can.useFlex()?A.remove.legacy():(A.set.legacy(),A.set.modalOffset(),A.debug("Using non-flex legacy modal positioning.")),A.set.screenHeight(),A.set.type(),A.set.clickaway(),!k.allowMultiple&&A.others.active()?A.hideOthers(A.showModal):(H=!1,k.allowMultiple&&(A.others.active()&&v.filter("."+O.active).find(F.dimmer).addClass("active"),k.detachable&&I.detach().appendTo(w)),k.onShow.call(j),k.transition&&e.fn.transition!==i&&I.transition("is supported")?(A.debug("Showing modal with css animations"),I.transition({debug:k.debug,animation:k.transition+" in",queue:k.queue,duration:k.duration,useFailSafe:!0,onComplete:function(){k.onVisible.apply(j),k.keyboardShortcuts&&A.add.keyboardShortcuts(),A.save.focus(),A.set.active(),k.autofocus&&A.set.autofocus(),t()}})):A.error(E.noTransition))):A.debug("Modal is already visible")},hideModal:function(t,n,a){var o=v.filter("."+O.active).last();if(t=e.isFunction(t)?t:function(){},A.debug("Hiding modal"),!1===k.onHide.call(j,e(this)))return A.verbose("Hide callback returned false cancelling hide"),H=!1,!1;(A.is.animating()||A.is.active())&&(k.transition&&e.fn.transition!==i&&I.transition("is supported")?(A.remove.active(),I.transition({debug:k.debug,animation:k.transition+" out",queue:k.queue,duration:k.duration,useFailSafe:!0,onStart:function(){A.others.active()||A.others.animating()||n||A.hideDimmer(),k.keyboardShortcuts&&!A.others.active()&&A.remove.keyboardShortcuts()},onComplete:function(){A.unbind.scrollLock(),k.allowMultiple&&(o.addClass(O.front),I.removeClass(O.front),a?r.find(F.dimmer).removeClass("active"):o.find(F.dimmer).removeClass("active")),k.onHidden.call(j),A.remove.dimmerStyles(),A.restore.focus(),t()}})):A.error(E.noTransition))},showDimmer:function(){y.dimmer("is animating")||!y.dimmer("is active")?(A.save.bodyMargin(),A.debug("Showing dimmer"),y.dimmer("show")):A.debug("Dimmer already visible")},hideDimmer:function(){y.dimmer("is animating")||y.dimmer("is active")?(A.unbind.scrollLock(),y.dimmer("hide",function(){A.restore.bodyMargin(),A.remove.clickaway(),A.remove.screenHeight()})):A.debug("Dimmer is not visible cannot hide")},hideAll:function(t){var n=r.filter("."+O.active+", ."+O.animating);if(t=e.isFunction(t)?t:function(){},n.length>0){A.debug("Hiding all visible modals");var i=!0;return e(n.get().reverse()).each(function(n,a){i&&(i=e(a).modal("hide modal",t,!1,!0))}),i&&A.hideDimmer(),i}},hideOthers:function(t){var n=v.filter("."+O.active+", ."+O.animating);t=e.isFunction(t)?t:function(){},n.length>0&&(A.debug("Hiding other modals",v),n.modal("hide modal",t,!0))},others:{active:function(){return v.filter("."+O.active).length>0},animating:function(){return v.filter("."+O.animating).length>0}},add:{keyboardShortcuts:function(){A.verbose("Adding keyboard shortcuts"),l.on("keyup"+R,A.event.keyboard)}},save:{focus:function(){e(n.activeElement).closest(I).length>0||(b=e(n.activeElement).blur())},bodyMargin:function(){z=c.css("margin-"+(A.can.leftBodyScrollbar()?"left":"right"));var e=parseInt(z.replace(/[^\d.]/g,"")),i=t.innerWidth-n.documentElement.clientWidth;V=e+i}},restore:{focus:function(){b&&b.length>0&&k.restoreFocus&&b.focus()},bodyMargin:function(){var e=A.can.leftBodyScrollbar()?"left":"right";c.css("margin-"+e,z),c.find(F.bodyFixed.replace("right",e)).css("padding-"+e,z)}},remove:{active:function(){I.removeClass(O.active)},legacy:function(){I.removeClass(O.legacy)},clickaway:function(){k.detachable||I.off("mousedown"+T),w.off("mousedown"+T),w.off("mouseup"+T)},dimmerStyles:function(){w.removeClass(O.inverted),y.removeClass(O.blurring)},bodyStyle:function(){""===c.attr("style")&&(A.verbose("Removing style attribute"),c.removeAttr("style"))},screenHeight:function(){A.debug("Removing page height"),c.css("height","")},keyboardShortcuts:function(){A.verbose("Removing keyboard shortcuts"),l.off("keyup"+R)},scrolling:function(){y.removeClass(O.scrolling),I.removeClass(O.scrolling)}},cacheSizes:function(){I.addClass(O.loading);var a=I.prop("scrollHeight"),o=I.outerWidth(),r=I.outerHeight();A.cache.pageHeight!==i&&0===r||(e.extend(A.cache,{pageHeight:e(n).outerHeight(),width:o,height:r+k.offset,scrollHeight:a+k.offset,contextHeight:"body"==k.context?e(t).height():y.height()}),A.cache.topOffset=-A.cache.height/2),I.removeClass(O.loading),A.debug("Caching modal and container sizes",A.cache)},can:{leftBodyScrollbar:function(){return A.cache.leftBodyScrollbar===i&&(A.cache.leftBodyScrollbar=A.is.rtl()&&(A.is.iframe&&!A.is.firefox()||A.is.safari()||A.is.edge()||A.is.ie())),A.cache.leftBodyScrollbar},useFlex:function(){return"auto"===k.useFlex?k.detachable&&!A.is.ie():(k.useFlex&&A.is.ie()?A.debug("useFlex true is not supported in IE"):k.useFlex&&!k.detachable&&A.debug("useFlex true in combination with detachable false is not supported"),k.useFlex)},fit:function(){var e=A.cache.contextHeight,t=A.cache.contextHeight/2,n=A.cache.topOffset,i=A.cache.scrollHeight,a=A.cache.height,o=k.padding;return i>a?t+n+i+o<e:a+2*o<e}},is:{active:function(){return I.hasClass(O.active)},ie:function(){if(A.cache.isIE===i){var e=!t.ActiveXObject&&"ActiveXObject"in t,n="ActiveXObject"in t;A.cache.isIE=e||n}return A.cache.isIE},animating:function(){return I.transition("is supported")?I.transition("is animating"):I.is(":visible")},scrolling:function(){return y.hasClass(O.scrolling)},modernBrowser:function(){return!(t.ActiveXObject||"ActiveXObject"in t)},rtl:function(){return A.cache.isRTL===i&&(A.cache.isRTL="rtl"===c.attr("dir")||"rtl"===c.css("direction")),A.cache.isRTL},safari:function(){return A.cache.isSafari===i&&(A.cache.isSafari=/constructor/i.test(t.HTMLElement)||!!t.ApplePaySession),A.cache.isSafari},edge:function(){return A.cache.isEdge===i&&(A.cache.isEdge=!!t.setImmediate&&!A.is.ie()),A.cache.isEdge},firefox:function(){return A.cache.isFirefox===i&&(A.cache.isFirefox=!!t.InstallTrigger),A.cache.isFirefox},iframe:function(){return!(self===top)}},set:{autofocus:function(){var t=I.find("[tabindex], :input").filter(":visible").filter(function(){return 0===e(this).closest(".disabled").length}),n=t.filter("[autofocus]"),i=n.length>0?n.first():t.first();i.length>0&&i.focus()},bodyMargin:function(){var e=A.can.leftBodyScrollbar()?"left":"right";(k.detachable||A.can.fit())&&c.css("margin-"+e,V+"px"),c.find(F.bodyFixed.replace("right",e)).css("padding-"+e,V+"px")},clickaway:function(){k.detachable||I.on("mousedown"+T,A.event.mousedown),w.on("mousedown"+T,A.event.mousedown),w.on("mouseup"+T,A.event.mouseup)},dimmerSettings:function(){if(e.fn.dimmer!==i){var t={debug:k.debug,dimmerName:"modals",closable:"auto",useFlex:A.can.useFlex(),duration:{show:k.duration,hide:k.duration}},n=e.extend(!0,t,k.dimmerSettings);k.inverted&&(n.variation=n.variation!==i?n.variation+" inverted":"inverted"),P.dimmer("setting",n)}else A.error(E.dimmer)},dimmerStyles:function(){k.inverted?w.addClass(O.inverted):w.removeClass(O.inverted),k.blurring?y.addClass(O.blurring):y.removeClass(O.blurring)},modalOffset:function(){if(k.detachable)I.css({marginTop:!I.hasClass("aligned")&&A.can.fit()?-A.cache.height/2:k.padding/2,marginLeft:-A.cache.width/2});else{var t=A.can.fit();I.css({top:!I.hasClass("aligned")&&t?e(n).scrollTop()+(A.cache.contextHeight-A.cache.height)/2:!t||I.hasClass("top")?e(n).scrollTop()+k.padding:e(n).scrollTop()+(A.cache.contextHeight-A.cache.height-k.padding),marginLeft:-A.cache.width/2})}A.verbose("Setting modal offset for legacy mode")},screenHeight:function(){A.can.fit()?c.css("height",""):I.hasClass("bottom")||(A.debug("Modal is taller than page content, resizing page height"),c.css("height",A.cache.height+2*k.padding))},active:function(){I.addClass(O.active+" "+O.front),v.filter("."+O.active).removeClass(O.front)},scrolling:function(){y.addClass(O.scrolling),I.addClass(O.scrolling),A.unbind.scrollLock()},legacy:function(){I.addClass(O.legacy)},type:function(){A.can.fit()?(A.verbose("Modal fits on screen"),A.others.active()||A.others.animating()||(A.remove.scrolling(),A.bind.scrollLock())):I.hasClass("bottom")?A.verbose("Bottom aligned modal not fitting on screen is unsupported for scrolling"):(A.verbose("Modal cannot fit on screen setting to scrolling"),A.set.scrolling())},undetached:function(){y.addClass(O.undetached)}},setting:function(t,n){if(A.debug("Changing setting",t,n),e.isPlainObject(t))e.extend(!0,k,t);else{if(n===i)return k[t];e.isPlainObject(k[t])?e.extend(!0,k[t],n):k[t]=n}},internal:function(t,n){if(e.isPlainObject(t))e.extend(!0,A,t);else{if(n===i)return A[t];A[t]=n}},debug:function(){!k.silent&&k.debug&&(k.performance?A.performance.log(arguments):(A.debug=Function.prototype.bind.call(console.info,console,k.name+":"),A.debug.apply(console,arguments)))},verbose:function(){!k.silent&&k.verbose&&k.debug&&(k.performance?A.performance.log(arguments):(A.verbose=Function.prototype.bind.call(console.info,console,k.name+":"),A.verbose.apply(console,arguments)))},error:function(){k.silent||(A.error=Function.prototype.bind.call(console.error,console,k.name+":"),A.error.apply(console,arguments))},performance:{log:function(e){var t,n;k.performance&&(n=(t=(new Date).getTime())-(d||t),d=t,f.push({Name:e[0],Arguments:[].slice.call(e,1)||"",Element:j,"Execution Time":n})),clearTimeout(A.performance.timer),A.performance.timer=setTimeout(A.performance.display,500)},display:function(){var t=k.name+":",n=0;d=!1,clearTimeout(A.performance.timer),e.each(f,function(e,t){n+=t["Execution Time"]}),t+=" "+n+"ms",u&&(t+=" '"+u+"'"),(console.group!==i||console.table!==i)&&f.length>0&&(console.groupCollapsed(t),console.table?console.table(f):e.each(f,function(e,t){console.log(t.Name+": "+t["Execution Time"]+"ms")}),console.groupEnd()),f=[]}},invoke:function(t,n,a){var r,s,l,c=N;return n=n||g,a=j||a,"string"==typeof t&&c!==i&&(t=t.split(/[\. ]/),r=t.length-1,e.each(t,function(n,a){var o=n!=r?a+t[n+1].charAt(0).toUpperCase()+t[n+1].slice(1):t;if(e.isPlainObject(c[o])&&n!=r)c=c[o];else{if(c[o]!==i)return s=c[o],!1;if(!e.isPlainObject(c[a])||n==r)return c[a]!==i&&(s=c[a],!1);c=c[a]}})),e.isFunction(s)?l=s.apply(a,n):s!==i&&(l=s),Array.isArray(o)?o.push(l):o!==i?o=[o,l]:l!==i&&(o=l),s}},p?(N===i&&A.initialize(),A.invoke(m)):(N!==i&&N.invoke("destroy"),A.initialize())}),o!==i?o:this},e.fn.modal.settings={name:"Modal",namespace:"modal",useFlex:"auto",offset:0,silent:!1,debug:!1,verbose:!1,performance:!0,observeChanges:!1,allowMultiple:!1,detachable:!0,closable:!0,autofocus:!0,restoreFocus:!0,inverted:!1,blurring:!1,centered:!0,dimmerSettings:{closable:!1,useCSS:!0},keyboardShortcuts:!0,context:"body",queue:!1,duration:500,transition:"scale",padding:50,scrollbarWidth:10,onShow:function(){},onVisible:function(){},onHide:function(){return!0},onHidden:function(){},onApprove:function(){return!0},onDeny:function(){return!0},selector:{close:"> .close",approve:".actions .positive, .actions .approve, .actions .ok",deny:".actions .negative, .actions .deny, .actions .cancel",modal:".ui.modal",dimmer:"> .ui.dimmer",bodyFixed:"> .ui.fixed.menu, > .ui.right.toast-container, > .ui.right.sidebar"},error:{dimmer:"UI Dimmer, a required component is not included in this page",method:"The method you called is not defined.",notFound:"The element you specified could not be found"},className:{active:"active",animating:"animating",blurring:"blurring",inverted:"inverted",legacy:"legacy",loading:"loading",scrolling:"scrolling",undetached:"undetached",front:"front"}}}(jQuery,window,document),function(e,t,n,i){"use strict";e.isFunction=e.isFunction||function(e){return"function"==typeof e&&"number"!=typeof e.nodeType},t=void 0!==t&&t.Math==Math?t:"undefined"!=typeof self&&self.Math==Math?self:Function("return this")(),e.fn.dimmer=function(t){var a,o=e(this),r=(new Date).getTime(),s=[],l=arguments[0],c="string"==typeof l,u=[].slice.call(arguments,1);return o.each(function(){var d,f,m,p=e.isPlainObject(t)?e.extend(!0,{},e.fn.dimmer.settings,t):e.extend({},e.fn.dimmer.settings),g=p.selector,h=p.namespace,v=p.className,b=p.error,y="."+h,w="module-"+h,C=o.selector||"",x="ontouchstart"in n.documentElement?"touchstart":"click",T=e(this),D=this,S=T.data(w);(m={preinitialize:function(){m.is.dimmer()?(f=T.parent(),d=T):(f=T,d=m.has.dimmer()?p.dimmerName?f.find(g.dimmer).filter("."+p.dimmerName):f.find(g.dimmer):m.create())},initialize:function(){m.debug("Initializing dimmer",p),m.bind.events(),m.set.dimmable(),m.instantiate()},instantiate:function(){m.verbose("Storing instance of module",m),S=m,T.data(w,S)},destroy:function(){m.verbose("Destroying previous module",d),m.unbind.events(),m.remove.variation(),f.off(y)},bind:{events:function(){"hover"==p.on?f.on("mouseenter"+y,m.show).on("mouseleave"+y,m.hide):"click"==p.on&&f.on(x+y,m.toggle),m.is.page()&&(m.debug("Setting as a page dimmer",f),m.set.pageDimmer()),m.is.closable()&&(m.verbose("Adding dimmer close event",d),f.on(x+y,g.dimmer,m.event.click))}},unbind:{events:function(){T.removeData(w),f.off(y)}},event:{click:function(t){m.verbose("Determining if event occured on dimmer",t),(0===d.find(t.target).length||e(t.target).is(g.content))&&(m.hide(),t.stopImmediatePropagation())}},addContent:function(t){var n=e(t);m.debug("Add content to dimmer",n),n.parent()[0]!==d[0]&&n.detach().appendTo(d)},create:function(){var t=e(p.template.dimmer(p));return p.dimmerName&&(m.debug("Creating named dimmer",p.dimmerName),t.addClass(p.dimmerName)),t.appendTo(f),t},show:function(t){t=e.isFunction(t)?t:function(){},m.debug("Showing dimmer",d,p),m.set.variation(),m.is.dimmed()&&!m.is.animating()||!m.is.enabled()?m.debug("Dimmer is already shown or disabled"):(m.animate.show(t),p.onShow.call(D),p.onChange.call(D))},hide:function(t){t=e.isFunction(t)?t:function(){},m.is.dimmed()||m.is.animating()?(m.debug("Hiding dimmer",d),m.animate.hide(t),p.onHide.call(D),p.onChange.call(D)):m.debug("Dimmer is not visible")},toggle:function(){m.verbose("Toggling dimmer visibility",d),m.is.dimmed()?m.is.closable()&&m.hide():m.show()},animate:{show:function(t){t=e.isFunction(t)?t:function(){},p.useCSS&&e.fn.transition!==i&&d.transition("is supported")?(p.useFlex?(m.debug("Using flex dimmer"),m.remove.legacy()):(m.debug("Using legacy non-flex dimmer"),m.set.legacy()),"auto"!==p.opacity&&m.set.opacity(),d.transition({displayType:p.useFlex?"flex":"block",animation:p.transition+" in",queue:!1,duration:m.get.duration(),useFailSafe:!0,onStart:function(){m.set.dimmed()},onComplete:function(){m.set.active(),t()}})):(m.verbose("Showing dimmer animation with javascript"),m.set.dimmed(),"auto"==p.opacity&&(p.opacity=.8),d.stop().css({opacity:0,width:"100%",height:"100%"}).fadeTo(m.get.duration(),p.opacity,function(){d.removeAttr("style"),m.set.active(),t()}))},hide:function(t){t=e.isFunction(t)?t:function(){},p.useCSS&&e.fn.transition!==i&&d.transition("is supported")?(m.verbose("Hiding dimmer with css"),d.transition({displayType:p.useFlex?"flex":"block",animation:p.transition+" out",queue:!1,duration:m.get.duration(),useFailSafe:!0,onComplete:function(){m.remove.dimmed(),m.remove.variation(),m.remove.active(),t()}})):(m.verbose("Hiding dimmer with javascript"),d.stop().fadeOut(m.get.duration(),function(){m.remove.dimmed(),m.remove.active(),d.removeAttr("style"),t()}))}},get:{dimmer:function(){return d},duration:function(){return"object"==typeof p.duration?m.is.active()?p.duration.hide:p.duration.show:p.duration}},has:{dimmer:function(){return p.dimmerName?T.find(g.dimmer).filter("."+p.dimmerName).length>0:T.find(g.dimmer).length>0}},is:{active:function(){return d.hasClass(v.active)},animating:function(){return d.is(":animated")||d.hasClass(v.animating)},closable:function(){return"auto"==p.closable?"hover"!=p.on:p.closable},dimmer:function(){return T.hasClass(v.dimmer)},dimmable:function(){return T.hasClass(v.dimmable)},dimmed:function(){return f.hasClass(v.dimmed)},disabled:function(){return f.hasClass(v.disabled)},enabled:function(){return!m.is.disabled()},page:function(){return f.is("body")},pageDimmer:function(){return d.hasClass(v.pageDimmer)}},can:{show:function(){return!d.hasClass(v.disabled)}},set:{opacity:function(e){var t=d.css("background-color"),n=t.split(","),i=n&&n.length>=3;e=0===p.opacity?0:p.opacity||e,i?(n[2]=n[2].replace(")",""),n[3]=e+")",t=n.join(",")):t="rgba(0, 0, 0, "+e+")",m.debug("Setting opacity to",e),d.css("background-color",t)},legacy:function(){d.addClass(v.legacy)},active:function(){d.addClass(v.active)},dimmable:function(){f.addClass(v.dimmable)},dimmed:function(){f.addClass(v.dimmed)},pageDimmer:function(){d.addClass(v.pageDimmer)},disabled:function(){d.addClass(v.disabled)},variation:function(e){(e=e||p.variation)&&d.addClass(e)}},remove:{active:function(){d.removeClass(v.active)},legacy:function(){d.removeClass(v.legacy)},dimmed:function(){f.removeClass(v.dimmed)},disabled:function(){d.removeClass(v.disabled)},variation:function(e){(e=e||p.variation)&&d.removeClass(e)}},setting:function(t,n){if(m.debug("Changing setting",t,n),e.isPlainObject(t))e.extend(!0,p,t);else{if(n===i)return p[t];e.isPlainObject(p[t])?e.extend(!0,p[t],n):p[t]=n}},internal:function(t,n){if(e.isPlainObject(t))e.extend(!0,m,t);else{if(n===i)return m[t];m[t]=n}},debug:function(){!p.silent&&p.debug&&(p.performance?m.performance.log(arguments):(m.debug=Function.prototype.bind.call(console.info,console,p.name+":"),m.debug.apply(console,arguments)))},verbose:function(){!p.silent&&p.verbose&&p.debug&&(p.performance?m.performance.log(arguments):(m.verbose=Function.prototype.bind.call(console.info,console,p.name+":"),m.verbose.apply(console,arguments)))},error:function(){p.silent||(m.error=Function.prototype.bind.call(console.error,console,p.name+":"),m.error.apply(console,arguments))},performance:{log:function(e){var t,n;p.performance&&(n=(t=(new Date).getTime())-(r||t),r=t,s.push({Name:e[0],Arguments:[].slice.call(e,1)||"",Element:D,"Execution Time":n})),clearTimeout(m.performance.timer),m.performance.timer=setTimeout(m.performance.display,500)},display:function(){var t=p.name+":",n=0;r=!1,clearTimeout(m.performance.timer),e.each(s,function(e,t){n+=t["Execution Time"]}),t+=" "+n+"ms",C&&(t+=" '"+C+"'"),o.length>1&&(t+=" ("+o.length+")"),(console.group!==i||console.table!==i)&&s.length>0&&(console.groupCollapsed(t),console.table?console.table(s):e.each(s,function(e,t){console.log(t.Name+": "+t["Execution Time"]+"ms")}),console.groupEnd()),s=[]}},invoke:function(t,n,o){var r,s,l,c=S;return n=n||u,o=D||o,"string"==typeof t&&c!==i&&(t=t.split(/[\. ]/),r=t.length-1,e.each(t,function(n,a){var o=n!=r?a+t[n+1].charAt(0).toUpperCase()+t[n+1].slice(1):t;if(e.isPlainObject(c[o])&&n!=r)c=c[o];else{if(c[o]!==i)return s=c[o],!1;if(!e.isPlainObject(c[a])||n==r)return c[a]!==i?(s=c[a],!1):(m.error(b.method,t),!1);c=c[a]}})),e.isFunction(s)?l=s.apply(o,n):s!==i&&(l=s),Array.isArray(a)?a.push(l):a!==i?a=[a,l]:l!==i&&(a=l),s}}).preinitialize(),c?(S===i&&m.initialize(),m.invoke(l)):(S!==i&&S.invoke("destroy"),m.initialize())}),a!==i?a:this},e.fn.dimmer.settings={name:"Dimmer",namespace:"dimmer",silent:!1,debug:!1,verbose:!1,performance:!0,useFlex:!0,dimmerName:!1,variation:!1,closable:"auto",useCSS:!0,transition:"fade",on:!1,opacity:"auto",duration:{show:500,hide:500},displayLoader:!1,loaderText:!1,loaderVariation:"",onChange:function(){},onShow:function(){},onHide:function(){},error:{method:"The method you called is not defined."},className:{active:"active",animating:"animating",dimmable:"dimmable",dimmed:"dimmed",dimmer:"dimmer",disabled:"disabled",hide:"hide",legacy:"legacy",pageDimmer:"page",show:"show",loader:"ui loader"},selector:{dimmer:"> .ui.dimmer",content:".ui.dimmer > .content, .ui.dimmer > .content > .center"},template:{dimmer:function(t){var n,i=e("<div/>").addClass("ui dimmer");return t.displayLoader&&(n=e("<div/>").addClass(t.className.loader).addClass(t.loaderVariation),t.loaderText&&(n.text(t.loaderText),n.addClass("text")),i.append(n)),i}}}}(jQuery,window,document),function(e,t,n,i){"use strict";e.isFunction=e.isFunction||function(e){return"function"==typeof e&&"number"!=typeof e.nodeType},t=void 0!==t&&t.Math==Math?t:"undefined"!=typeof self&&self.Math==Math?self:Function("return this")(),e.fn.search=function(a){var o,r=e(this),s=r.selector||"",l=(new Date).getTime(),c=[],u=arguments[0],d="string"==typeof u,f=[].slice.call(arguments,1);return e(this).each(function(){var m,p=e.isPlainObject(a)?e.extend(!0,{},e.fn.search.settings,a):e.extend({},e.fn.search.settings),g=p.className,h=p.metadata,v=p.regExp,b=p.fields,y=p.selector,w=p.error,C=p.namespace,x="."+C,T=C+"-module",D=e(this),S=D.find(y.prompt),A=D.find(y.searchButton),k=D.find(y.results),F=D.find(y.result),O=(D.find(y.category),this),M=D.data(T),E=!1,R=!1;m={initialize:function(){m.verbose("Initializing module"),m.get.settings(),m.determine.searchFields(),m.bind.events(),m.set.type(),m.create.results(),m.instantiate()},instantiate:function(){m.verbose("Storing instance of module",m),M=m,D.data(T,m)},destroy:function(){m.verbose("Destroying instance"),D.off(x).removeData(T)},refresh:function(){m.debug("Refreshing selector cache"),S=D.find(y.prompt),A=D.find(y.searchButton),D.find(y.category),k=D.find(y.results),F=D.find(y.result)},refreshResults:function(){k=D.find(y.results),F=D.find(y.result)},bind:{events:function(){m.verbose("Binding events to search"),p.automatic&&(D.on(m.get.inputEvent()+x,y.prompt,m.event.input),S.attr("autocomplete","off")),D.on("focus"+x,y.prompt,m.event.focus).on("blur"+x,y.prompt,m.event.blur).on("keydown"+x,y.prompt,m.handleKeyboard).on("click"+x,y.searchButton,m.query).on("mousedown"+x,y.results,m.event.result.mousedown).on("mouseup"+x,y.results,m.event.result.mouseup).on("click"+x,y.result,m.event.result.click)}},determine:{searchFields:function(){a&&a.searchFields!==i&&(p.searchFields=a.searchFields)}},event:{input:function(){p.searchDelay?(clearTimeout(m.timer),m.timer=setTimeout(function(){m.is.focused()&&m.query()},p.searchDelay)):m.query()},focus:function(){m.set.focus(),p.searchOnFocus&&m.has.minimumCharacters()&&m.query(function(){m.can.show()&&m.showResults()})},blur:function(){var e=n.activeElement===this,t=function(){m.cancel.query(),m.remove.focus(),m.timer=setTimeout(m.hideResults,p.hideDelay)};e||(R=!1,m.resultsClicked?(m.debug("Determining if user action caused search to close"),D.one("click.close"+x,y.results,function(e){m.is.inMessage(e)||E?S.focus():(E=!1,m.is.animating()||m.is.hidden()||t())})):(m.debug("Input blurred without user action, closing results"),t()))},result:{mousedown:function(){m.resultsClicked=!0},mouseup:function(){m.resultsClicked=!1},click:function(n){m.debug("Search result selected");var i=e(this),a=i.find(y.title).eq(0),o=i.is("a[href]")?i:i.find("a[href]").eq(0),r=o.attr("href")||!1,s=o.attr("target")||!1,l=a.length>0&&a.text(),c=m.get.results(),u=i.data(h.result)||m.get.result(l,c);if(l&&m.set.value(l),e.isFunction(p.onSelect)&&!1===p.onSelect.call(O,u,c))return m.debug("Custom onSelect callback cancelled default select action"),void(E=!0);m.hideResults(),r&&(n.preventDefault(),m.verbose("Opening search link found in result",o),"_blank"==s||n.ctrlKey?t.open(r):t.location.href=r)}}},ensureVisible:function(e){var t,n,i,a;n=(t=e.position().top)+e.outerHeight(!0),i=k.scrollTop(),a=k.height(),parseInt(k.css("paddingTop"),0),parseInt(k.css("paddingBottom"),0),t<0?k.scrollTop(i+t):a<n&&k.scrollTop(i+(n-a))},handleKeyboard:function(e){var t,n=D.find(y.result),i=D.find(y.category),a=n.filter("."+g.active),o=n.index(a),r=n.length,s=a.length>0,l=e.which,c={backspace:8,enter:13,escape:27,upArrow:38,downArrow:40};if(l==c.escape&&(m.verbose("Escape key pressed, blurring search field"),m.hideResults(),R=!0),m.is.visible())if(l==c.enter){if(m.verbose("Enter key pressed, selecting active result"),n.filter("."+g.active).length>0)return m.event.result.click.call(n.filter("."+g.active),e),e.preventDefault(),!1}else l==c.upArrow&&s?(m.verbose("Up key pressed, changing active result"),t=o-1<0?o:o-1,i.removeClass(g.active),n.removeClass(g.active).eq(t).addClass(g.active).closest(i).addClass(g.active),m.ensureVisible(n.eq(t)),e.preventDefault()):l==c.downArrow&&(m.verbose("Down key pressed, changing active result"),t=o+1>=r?o:o+1,i.removeClass(g.active),
n.removeClass(g.active).eq(t).addClass(g.active).closest(i).addClass(g.active),m.ensureVisible(n.eq(t)),e.preventDefault());else l==c.enter&&(m.verbose("Enter key pressed, executing query"),m.query(),m.set.buttonPressed(),S.one("keyup",m.remove.buttonFocus))},setup:{api:function(t,n){var i={debug:p.debug,on:!1,cache:p.cache,action:"search",urlData:{query:t},onSuccess:function(e){m.parse.response.call(O,e,t),n()},onFailure:function(){m.displayMessage(w.serverError),n()},onAbort:function(){},onError:m.error};e.extend(!0,i,p.apiSettings),m.verbose("Setting up API request",i),D.api(i)}},can:{useAPI:function(){return e.fn.api!==i},show:function(){return m.is.focused()&&!m.is.visible()&&!m.is.empty()},transition:function(){return p.transition&&e.fn.transition!==i&&D.transition("is supported")}},is:{animating:function(){return k.hasClass(g.animating)},hidden:function(){return k.hasClass(g.hidden)},inMessage:function(t){if(t.target){var i=e(t.target);return e.contains(n.documentElement,t.target)&&i.closest(y.message).length>0}},empty:function(){return""===k.html()},visible:function(){return k.filter(":visible").length>0},focused:function(){return S.filter(":focus").length>0}},get:{settings:function(){e.isPlainObject(a)&&a.searchFullText&&(p.fullTextSearch=a.searchFullText,m.error(p.error.oldSearchSyntax,O)),p.ignoreDiacritics&&!String.prototype.normalize&&(p.ignoreDiacritics=!1,m.error(w.noNormalize,O))},inputEvent:function(){var e=S[0];return e!==i&&e.oninput!==i?"input":e!==i&&e.onpropertychange!==i?"propertychange":"keyup"},value:function(){return S.val()},results:function(){return D.data(h.results)},result:function(t,n){var a=!1;return t=t!==i?t:m.get.value(),n=n!==i?n:m.get.results(),"category"===p.type?(m.debug("Finding result that matches",t),e.each(n,function(e,n){if(Array.isArray(n.results)&&(a=m.search.object(t,n.results)[0]))return!1})):(m.debug("Finding result in results object",t),a=m.search.object(t,n)[0]),a||!1}},select:{firstResult:function(){m.verbose("Selecting first result"),F.first().addClass(g.active)}},set:{focus:function(){D.addClass(g.focus)},loading:function(){D.addClass(g.loading)},value:function(e){m.verbose("Setting search input value",e),S.val(e)},type:function(e){e=e||p.type,"category"==p.type&&D.addClass(p.type)},buttonPressed:function(){A.addClass(g.pressed)}},remove:{loading:function(){D.removeClass(g.loading)},focus:function(){D.removeClass(g.focus)},buttonPressed:function(){A.removeClass(g.pressed)},diacritics:function(e){return p.ignoreDiacritics?e.normalize("NFD").replace(/[\u0300-\u036f]/g,""):e}},query:function(t){t=e.isFunction(t)?t:function(){};var n=m.get.value(),i=m.read.cache(n);t=t||function(){},m.has.minimumCharacters()?(i?(m.debug("Reading result from cache",n),m.save.results(i.results),m.addResults(i.html),m.inject.id(i.results),t()):(m.debug("Querying for",n),e.isPlainObject(p.source)||Array.isArray(p.source)?(m.search.local(n),t()):m.can.useAPI()?m.search.remote(n,t):(m.error(w.source),t())),p.onSearchQuery.call(O,n)):m.hideResults()},search:{local:function(e){var t,n=m.search.object(e,p.source);m.set.loading(),m.save.results(n),m.debug("Returned full local search results",n),p.maxResults>0&&(m.debug("Using specified max results",n),n=n.slice(0,p.maxResults)),"category"==p.type&&(n=m.create.categoryResults(n)),t=m.generateResults({results:n}),m.remove.loading(),m.addResults(t),m.inject.id(n),m.write.cache(e,{html:t,results:n})},remote:function(t,n){n=e.isFunction(n)?n:function(){},D.api("is loading")&&D.api("abort"),m.setup.api(t,n),D.api("query")},object:function(t,n,a){t=m.remove.diacritics(String(t));var o=[],r=[],s=[],l=t.replace(v.escape,"\\$&"),c=new RegExp(v.beginsWith+l,"i"),u=function(t,n){var i=-1==e.inArray(n,o),a=-1==e.inArray(n,s),l=-1==e.inArray(n,r);i&&a&&l&&t.push(n)};return n=n||p.source,a=a!==i?a:p.searchFields,Array.isArray(a)||(a=[a]),n===i||!1===n?(m.error(w.source),[]):(e.each(a,function(i,a){e.each(n,function(e,n){var i;"string"!=typeof n[a]&&"number"!=typeof n[a]||(-1!==(i="string"==typeof n[a]?m.remove.diacritics(n[a]):n[a].toString()).search(c)?u(o,n):"exact"===p.fullTextSearch&&m.exactSearch(t,i)?u(r,n):1==p.fullTextSearch&&m.fuzzySearch(t,i)&&u(s,n))})}),e.merge(r,s),e.merge(o,r),o)}},exactSearch:function(e,t){return e=e.toLowerCase(),(t=t.toLowerCase()).indexOf(e)>-1},fuzzySearch:function(e,t){var n=t.length,i=e.length;if("string"!=typeof e)return!1;if(e=e.toLowerCase(),t=t.toLowerCase(),i>n)return!1;if(i===n)return e===t;e:for(var a=0,o=0;a<i;a++){for(var r=e.charCodeAt(a);o<n;)if(t.charCodeAt(o++)===r)continue e;return!1}return!0},parse:{response:function(e,t){if(Array.isArray(e)){var n={};n[b.results]=e,e=n}var a=m.generateResults(e);m.verbose("Parsing server response",e),e!==i&&t!==i&&e[b.results]!==i&&(m.addResults(a),m.inject.id(e[b.results]),m.write.cache(t,{html:a,results:e[b.results]}),m.save.results(e[b.results]))}},cancel:{query:function(){m.can.useAPI()&&D.api("abort")}},has:{minimumCharacters:function(){return m.get.value().length>=p.minCharacters},results:function(){return 0!==k.length&&""!=k.html()}},clear:{cache:function(e){var t=D.data(h.cache);e?e&&t&&t[e]&&(m.debug("Removing value from cache",e),delete t[e],D.data(h.cache,t)):(m.debug("Clearing cache",e),D.removeData(h.cache))}},read:{cache:function(e){var t=D.data(h.cache);return!!p.cache&&(m.verbose("Checking cache for generated html for query",e),"object"==typeof t&&t[e]!==i&&t[e])}},create:{categoryResults:function(t){var n={};return e.each(t,function(e,t){t.category&&(n[t.category]===i?(m.verbose("Creating new category of results",t.category),n[t.category]={name:t.category,results:[t]}):n[t.category].results.push(t))}),n},id:function(e,t){var n,a=e+1;return t!==i?(n=String.fromCharCode(97+t)+a,m.verbose("Creating category result id",n)):(n=a,m.verbose("Creating result id",n)),n},results:function(){0===k.length&&(k=e("<div />").addClass(g.results).appendTo(D))}},inject:{result:function(e,t,n){m.verbose("Injecting result into results");var a=n!==i?k.children().eq(n).children(y.results).first().children(y.result).eq(t):k.children(y.result).eq(t);m.verbose("Injecting results metadata",a),a.data(h.result,e)},id:function(t){m.debug("Injecting unique ids into results");var n=0,a=0;return"category"===p.type?e.each(t,function(t,o){o.results.length>0&&(a=0,e.each(o.results,function(e,t){t.id===i&&(t.id=m.create.id(a,n)),m.inject.result(t,a,n),a++}),n++)}):e.each(t,function(e,t){t.id===i&&(t.id=m.create.id(a)),m.inject.result(t,a),a++}),t}},save:{results:function(e){m.verbose("Saving current search results to metadata",e),D.data(h.results,e)}},write:{cache:function(e,t){var n=D.data(h.cache)!==i?D.data(h.cache):{};p.cache&&(m.verbose("Writing generated html to cache",e,t),n[e]=t,D.data(h.cache,n))}},addResults:function(t){if(e.isFunction(p.onResultsAdd)&&!1===p.onResultsAdd.call(k,t))return m.debug("onResultsAdd callback cancelled default action"),!1;t?(k.html(t),m.refreshResults(),p.selectFirstResult&&m.select.firstResult(),m.showResults()):m.hideResults(function(){k.empty()})},showResults:function(t){t=e.isFunction(t)?t:function(){},R||!m.is.visible()&&m.has.results()&&(m.can.transition()?(m.debug("Showing results with css animations"),k.transition({animation:p.transition+" in",debug:p.debug,verbose:p.verbose,duration:p.duration,onShow:function(){var e=D.find(y.result).eq(0);e.length>0&&m.ensureVisible(e)},onComplete:function(){t()},queue:!0})):(m.debug("Showing results with javascript"),k.stop().fadeIn(p.duration,p.easing)),p.onResultsOpen.call(k))},hideResults:function(t){t=e.isFunction(t)?t:function(){},m.is.visible()&&(m.can.transition()?(m.debug("Hiding results with css animations"),k.transition({animation:p.transition+" out",debug:p.debug,verbose:p.verbose,duration:p.duration,onComplete:function(){t()},queue:!0})):(m.debug("Hiding results with javascript"),k.stop().fadeOut(p.duration,p.easing)),p.onResultsClose.call(k))},generateResults:function(t){m.debug("Generating html from response",t);var n=p.templates[p.type],i=e.isPlainObject(t[b.results])&&!e.isEmptyObject(t[b.results]),a=Array.isArray(t[b.results])&&t[b.results].length>0,o="";return i||a?(p.maxResults>0&&(i?"standard"==p.type&&m.error(w.maxResults):t[b.results]=t[b.results].slice(0,p.maxResults)),e.isFunction(n)?o=n(t,b,p.preserveHTML):m.error(w.noTemplate,!1)):p.showNoResults&&(o=m.displayMessage(w.noResults,"empty",w.noResultsHeader)),p.onResults.call(O,t),o},displayMessage:function(e,t,n){return t=t||"standard",m.debug("Displaying message",e,t,n),m.addResults(p.templates.message(e,t,n)),p.templates.message(e,t,n)},setting:function(t,n){if(e.isPlainObject(t))e.extend(!0,p,t);else{if(n===i)return p[t];p[t]=n}},internal:function(t,n){if(e.isPlainObject(t))e.extend(!0,m,t);else{if(n===i)return m[t];m[t]=n}},debug:function(){!p.silent&&p.debug&&(p.performance?m.performance.log(arguments):(m.debug=Function.prototype.bind.call(console.info,console,p.name+":"),m.debug.apply(console,arguments)))},verbose:function(){!p.silent&&p.verbose&&p.debug&&(p.performance?m.performance.log(arguments):(m.verbose=Function.prototype.bind.call(console.info,console,p.name+":"),m.verbose.apply(console,arguments)))},error:function(){p.silent||(m.error=Function.prototype.bind.call(console.error,console,p.name+":"),m.error.apply(console,arguments))},performance:{log:function(e){var t,n;p.performance&&(n=(t=(new Date).getTime())-(l||t),l=t,c.push({Name:e[0],Arguments:[].slice.call(e,1)||"",Element:O,"Execution Time":n})),clearTimeout(m.performance.timer),m.performance.timer=setTimeout(m.performance.display,500)},display:function(){var t=p.name+":",n=0;l=!1,clearTimeout(m.performance.timer),e.each(c,function(e,t){n+=t["Execution Time"]}),t+=" "+n+"ms",s&&(t+=" '"+s+"'"),r.length>1&&(t+=" ("+r.length+")"),(console.group!==i||console.table!==i)&&c.length>0&&(console.groupCollapsed(t),console.table?console.table(c):e.each(c,function(e,t){console.log(t.Name+": "+t["Execution Time"]+"ms")}),console.groupEnd()),c=[]}},invoke:function(t,n,a){var r,s,l,c=M;return n=n||f,a=O||a,"string"==typeof t&&c!==i&&(t=t.split(/[\. ]/),r=t.length-1,e.each(t,function(n,a){var o=n!=r?a+t[n+1].charAt(0).toUpperCase()+t[n+1].slice(1):t;if(e.isPlainObject(c[o])&&n!=r)c=c[o];else{if(c[o]!==i)return s=c[o],!1;if(!e.isPlainObject(c[a])||n==r)return c[a]!==i&&(s=c[a],!1);c=c[a]}})),e.isFunction(s)?l=s.apply(a,n):s!==i&&(l=s),Array.isArray(o)?o.push(l):o!==i?o=[o,l]:l!==i&&(o=l),s}},d?(M===i&&m.initialize(),m.invoke(u)):(M!==i&&M.invoke("destroy"),m.initialize())}),o!==i?o:this},e.fn.search.settings={name:"Search",namespace:"search",silent:!1,debug:!1,verbose:!1,performance:!0,type:"standard",minCharacters:1,selectFirstResult:!1,apiSettings:!1,source:!1,searchOnFocus:!0,searchFields:["id","title","description"],displayField:"",fullTextSearch:"exact",ignoreDiacritics:!1,automatic:!0,hideDelay:0,searchDelay:200,maxResults:7,cache:!0,showNoResults:!0,preserveHTML:!0,transition:"scale",duration:200,easing:"easeOutExpo",onSelect:!1,onResultsAdd:!1,onSearchQuery:function(){},onResults:function(){},onResultsOpen:function(){},onResultsClose:function(){},className:{animating:"animating",active:"active",empty:"empty",focus:"focus",hidden:"hidden",loading:"loading",results:"results",pressed:"down"},error:{source:"Cannot search. No source used, and Semantic API module was not included",noResultsHeader:"No Results",noResults:"Your search returned no results",logging:"Error in debug logging, exiting.",noEndpoint:"No search endpoint was specified",noTemplate:"A valid template name was not specified.",oldSearchSyntax:"searchFullText setting has been renamed fullTextSearch for consistency, please adjust your settings.",serverError:"There was an issue querying the server.",maxResults:"Results must be an array to use maxResults setting",method:"The method you called is not defined.",noNormalize:'"ignoreDiacritics" setting will be ignored. Browser does not support String().normalize(). You may consider including <https://cdn.jsdelivr.net/npm/unorm@1.4.1/lib/unorm.min.js> as a polyfill.'},metadata:{cache:"cache",results:"results",result:"result"},regExp:{escape:/[\-\[\]\/\{\}\(\)\*\+\?\.\\\^\$\|]/g,beginsWith:"(?:s|^)"},fields:{categories:"results",categoryName:"name",categoryResults:"results",description:"description",image:"image",price:"price",results:"results",title:"title",url:"url",action:"action",actionText:"text",actionURL:"url"},selector:{prompt:".prompt",searchButton:".search.button",results:".results",message:".results > .message",category:".category",result:".result",title:".title, .name"},templates:{escape:function(e,t){if(t)return e;var n=/[<>"'`]/g,i={"<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#x27;","`":"&#x60;"},a=function(e){return i[e]};return/[&<>"'`]/.test(e)?(e=e.replace(/&(?![a-z0-9#]{1,6};)/,"&amp;")).replace(n,a):e},message:function(e,t,n){var a="";return e!==i&&t!==i&&(a+='<div class="message '+t+'">',n&&(a+='<div class="header">'+n+"</div>"),a+=' <div class="description">'+e+"</div>",a+="</div>"),a},category:function(t,n,a){var o="",r=e.fn.search.settings.templates.escape;return t[n.categoryResults]!==i&&(e.each(t[n.categoryResults],function(t,s){s[n.results]!==i&&s.results.length>0&&(o+='<div class="category">',s[n.categoryName]!==i&&(o+='<div class="name">'+r(s[n.categoryName],a)+"</div>"),o+='<div class="results">',e.each(s.results,function(e,t){t[n.url]?o+='<a class="result" href="'+t[n.url].replace(/"/g,"")+'">':o+='`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/packs/js/application-47cec7361a3c7e110904.js](https://place-des-entreprises.beta.gouv.fr/packs/js/application-47cec7361a3c7e110904.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/packs/js/pages-711e95e411c04ee7d6bd.js](https://place-des-entreprises.beta.gouv.fr/packs/js/pages-711e95e411c04ee7d6bd.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 3
  
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
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000749074`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000755041`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001329013`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000289528`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001211674`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000560400`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000378`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001381134`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000090`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000423025`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000210`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000927851`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000469`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000375529`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000771854`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000702336`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000482081`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001368099`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001371911`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000456`
  
  
  
  
Instances: 576
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0000749074, which evaluates to: 1970-01-09 16:04:34</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[full_name]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[email]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[phone_number]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[email]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_options_slugs][]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_slug]`
  
  
  
  
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
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>solicitation[full_name]=ZAP</p><p></p><p>The user-controlled value was:</p><p>zap</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

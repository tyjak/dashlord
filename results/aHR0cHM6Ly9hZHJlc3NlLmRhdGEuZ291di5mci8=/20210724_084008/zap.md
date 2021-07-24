
# ZAP Scanning Report

Generated on Sat, 24 Jul 2021 08:32:18


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 8 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| Directory Browsing - Apache 2 | Medium | 8 | 
| Reverse Tabnabbing | Medium | 3 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 9 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf](https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf](https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Directory Browsing - Apache 2
##### Medium (Medium)
  
  
  
  
#### Description
<p>It is possible to view a listing of the directory contents. Directory listings may reveal hidden scripts, include files , backup source files, etc., which be accessed to reveal sensitive information. - Apache 2</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/addok/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/housenumber-id-ign/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/](https://adresse.data.gouv.fr/data/ban/adresses/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/csv/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/ban/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/group-id-ign/</title>`
  
  
  
  
Instances: 8
  
### Solution
<p>Configure the web server to disable directory browsing. </p>
  
### Other information
<p><title>Index of /data/ban/adresses/latest/addok/</title></p>
  
### Reference
* https://cwe.mitre.org/data/definitions/548.html

  
#### CWE Id : 548
  
#### WASC Id : 16
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/de-la-commune-au-d%C3%A9partement-la-collaboration-sur-les-adresses-dans-le-gers-c0d83fb20950" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/de-la-commune-au-d%C3%A9partement-la-collaboration-sur-les-adresses-dans-le-gers-c0d83fb20950" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#ni4M</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?={\x001c\x000b\x0011Ý/[9\x0008:ä9xêÁ/\è"/\x0005X\x0001~æ£¹\x0008\x001fOçà,êÕ»|$;Á×\x0016§Â\x001ah\x000f\V\x001e5¼\x001aBs9r\x0002ÿàcA[ð97?»ë¿yÊ±JU[²7·6W¹Õa\x000bN\x001a5x°ªÁ%ã{ï.Y©Ë
¸\ã\x0006¸<x\x0007ÑæÇ\x0007µ7gÇ¯^bÃG\x00185¦d¤>HÁ|sÖÖûÃìb\x0005µj­ð&äÐÓËÞÂo!d\x0000ï*ýtAºè²Ë\x000f°Øòõ\x001e6#ï_øè
?ÞÜ|úq\x0011¤Á¶é§\x0013\x0012lm4\x0019Ræ>æi\x0007S-|\x0008v=H<ÒÍÔ¿\x0005)óAZ§rÂ\x0004ë\x0008­\x0008BÇõ ñÙ*ýôAZa0$ù\x0003r\x00102_ÍÖÄ½ÞîgÍ$¶3Ë»ÛÂ\x001dÊe;\x0002þ\x0014ï\x001cgýj¸\x001f¿I?½;Ò»¶.òÑí©0no·xã8ýÛ:Râø7»Á¦óËO¯¸)l\x000bÓÂ¦NÒ\x0018ì?\x0017¥²tPJ.\x0012Õßôp0çüøõÛ¹\x001bìc¤¨\x0019wCN3Q=_­	ùñ\x000fYÉ¡vé\x0001k9ê?®þñ·\x000fý3*ü¿[môû··\x001bøÛ7÷{|//'\x001a\x001fVsHGiÍq'p$õã»_.o±Æ\x0017 \x0017\x0007oÏ\x0000òè¢Áø·pÿ£ý\x0005M7.L9](
xñ~óa}Ôr\x0014$üsÊfDÛã-=¹	\x0017áÀ4,zh6\x000f.\x001d=\x000cQc¤ ýô \x0002\x0000_ó$|[ìÙ6¹1ô\x000eN¬_¨ïÿñÓÍ¿Rh\x000cN¢>îÀ5ø1K¸7'\x0011®Nùe\x0010þÉ°ß\x0018¤D\x000f\\x0004\x0012\x001f¼{ù\x0002ÅÛ\x001fA|ðñòQD¼ÓYzC«ÉO«p¨\x0011¢OzøË\x0010úxù×_ÿAY=9§RN|usÚ]5g\x0011sd²\x000bæ\x0010Á
ÊÝ\x0012IQk×¬´\x0012_^`RÏÃp÷ò'\x001b6Õu¥¨ôß\x001f|w»ùçÝÝÕ>¶¯ÄèFÚ@\x0006ÛQ\x0017i}ÃdmþïÎþt~þòq¼|méÄ\x000b¹³4âé§e>+Z\x000fS:ùP3Y\x001bâ3\x0014mV¼ð5ù`Ùù^>¥èQ\x0008ølº\x0003&>vvÕf5¾l ;ù¨ö\x001dù<¥\x0008O\x0006\x000fðìZtÙôâ\x0019Aoç\x001aã:fDÛíáW\x0003Ôß¤ê >@Ø\x0014IÌ\x0005\x0001aÈX"lÙ\x001fqµõ+Yõ\x0002ê\x0005W_>*p©¤s%8L.éÝ½Ø.UÊDma\x0010I2 Zmw$ËÑ»}u\x0008Yt\x0001\x0001Sai\x0002ôn}\x0006s~×\x0002¿Iõî_|\x000fÏï{\x0000h!FÀÀûC¯ö1¡{÷¯"8Zé@A\x0012ø\x000f+Ã|rµ\x0003F£yëÝ\x001eFÉb?ÀÁ
ù\x0000Ä:>\x0002Äç¨µ\x0000áoÒ½[Ä ,PæS¾L .;$'®­Ãèn¾{
ç/owØ?40`\\x000f\x0010vîÝ!(u\x001cr¸AÁj4yh¸u\x0012 
ä®\x0004¹\x0013¦{`·fúÄBÓÓäa=<Ø\x001d¦{`²iÆÑ¡þPÆ3\x0001åzxÓ\x0007èù\x0015\x000c\x001b³Ñ;²diel°oÆ\x0001ßÿýÞß|¨<ü7×\x000fS\x001e®ö¦\x0014{Lêd/F\x000bþÂ¹}>\x0005Uc¼99zÎùÄé
¬N\Aâãì\x0000¤I7à\x0004\x0019Ùð=\x000em±h|ç1È|\x0019\x0019ÔäÐ\x0018K±C)¶îVÓa\x001dÄXñ\x0000¤ÎÅnèu)>\x0012(.¡\õkç[S/# #l\x001a\x0014Ç(øÞä1fº\x001e$üe®\x001f2h¶}Ø¦\x0019Ùù
X|¼\x001ec¾Þõ2FY\x0002Õ6àý=ðÞ\x000e¢q\x001f\x0011\x0001HUL\x000cE<0«üµUã\x001cÌ\x0017ÑNH%ø\x0014 ©ðB¦ \á\x0000úËåU\x0008.ÅãðÕOÔ­Þ0bxôëæÓ=A{R¯\x0008XHï@àzg{m¢H²!,ð\x0016þ¦*U \x0008\x001c\x001c½;zý|\x0006¡GBßM(\x000cåUI\x000f·{ÃÃ6\x0017®\x0002 \x0006\x000f×\x0001Ä¼õôÓ	h
¼$
ÈÈ\x001cÀ6g0µf\x0010\x0003áé§\x0017P¤</\x0004ôS\x001bà.Cu,"õäZ\x0010\x000eøÓIh¨¼\x0013³TDÎ5\x0006BA5\x0005\x0011þ\x001bz%BTÅL?½shÉRËà}!"¡¢ÈuI³c
Bü\x001d1@è)\x0017
ÎðÜÅ*\x0011:C%ìJ_Yá~zwr à\x000c\x0000½\x001dïÏ4Öù\x0008K\½PEu`ñ+ËCOCmøGºµNÃ¤\x0005~:	Cyã	Øú6Ðk\x0019¥·Dì×»\x0012!F
ÒO'!êA\x0013 §û\x0015\\x0013(Õ\x001d\x0000­[\x0005\x0010Ö6¼ôÛEè±cMvh¥\x000fné
¨\x0005ðz,¹úæÍæÓÇÉSã\x0000 O½ËÐcOMª]ÒÆ¥öÌ\x0000hT`@¡\x0015\x0000m\x0002´ÝXÄÀ|6:)Î)
óa=Ã³Û«7÷\x001f.û\x0001ö²\x0006Íü[\x0000ã;Ùíþoª\x001cù>\x0000VDRåsT1Ðqí\x0002uõW}Éø\x001c_ËÎö¼zW:QênJ¬³Èe\x0018Y¹ÂF\x0019*|õéy~\x0019ä/Âü\x0018omó`&ÞÃó¿n>]¾Oå¡{ò[°ëhGX
OP~ÏÞEQßÂÕ\x0003ß\x001f½>~¶§à´P:¬\x000fÈ¿}©&;]÷­\x0013%s9°íÍRÊÛ¿\x0019ùÏ))\x0017)ý\x000eä=ìÆ½7\x0002#À×¦Ô×èR÷¯TèLÖ%DÑÀkÊo^·kÆ\x00192½Ä¥>H£²"\\x0006¨(\x0000o5§ç¦¤ÇûíãÇ\x001bWM|ôó}Í\x0012cw9\\x0002\x0006%zá-¿¼.§:ª®TE4úùi+Mw\x000bÅ\x000fSs©Ð5ÌWfªË\x0014{\x0008bÚV¶®Ì]T9Ñ¯c®r\x0018\x0004©ÀdW\x0006æÊÒ\Yí\x001aÑ>*
qöÌ"*Í©\x000b1pè\x0010Ök#NÓEI\x0006^vP	Î
ÐøêI¹¯Aò\¥úãÅTÇ5ÊÛ,ð
%³Út\x0017u\x0015tã-¶*-N):&KGºk¥xÒd¹HU\x001bU#fÙ\x000cAe\x0007\x001eÿsE±ê*\x0003càÀCñìåXø¤¹Xà¼
ÎÁÞ¥)z
\x0015\x0016<>¯|~f\x000e\í á\x000b7\x000eTG)j\x0005uû°Ð¿Ô~>\x0012e¶<´e<DôVÀÂµ¥;Ö/YCp×Ä\x0006*å¥.¦*Õ\x000e\x001dKK*¢rÛ¥EåReWÀRXþ~:\x000eÓ@ç\x0003>°}±\x0011}+©\x000f\x000b«·Dß§Ì\x0002«ì!?\x0007ñ'­Ø{\x001f\x0014¸¥=
 TN§\x0012Ñ«ÀX­t\x001e¬déÓÏL,\x0011³;ãÐ\x0018;£<-«.´\x000f\x0016YtA¡Sú\x000bå¶\x0015\x000b`\x0019i]Á²¢O\x00180o9\x0017Æm¿I?s¿¡àVí¢ÎÚ\x00180_p\x0011!.ÌË\+ WÏÚ\x0012¹bÚym\x0019ærr
.|jI?³\x0017g\x0017\x0010+)Ë|)z\x0006\x000b>¬Âe°Ãt[pÏ
Äel)r´\x0015C*ß^\x0001\x000b§«çÇ i¦ÂZ@C\x00161¡ÒéU°¸hîW\x000c:ÙAä²®<¸J®(Â*ÓIõég.\x0017ê¾\x0010\x0017\x0018Erlâ\x0004Õ"ë\x000fÕÌÀRa³	òÏBc\x0016Á7ù·\®_l~Ù\x0017êQ*×ÔX	ÑR^\x0016)ídGxª\¨_\x001c½y\x0014	wsþ\x0014\x000eI¥\x000b\x001cfÁDT\x0001¦EÊ3YD¤\x0013O¤9uÈhs\x0001Hr\x001a²Ç\x0017!Ùdç#yÛ´#RH\x0012º¨.#r[\x0005DÂ©EH>!ùÙH\x0011zÑ,Á.D1\x0007D²Z\x0012A×¶\x001fÉ~|ÿÓ_nª<²åN6÷{«:`GT[¼¨òKwlåÌ=wrtÑ*Øb}q~\x000bóã\x0002_ësâ5r15á±ËÄ\x001c,©Ò3íáR)±"9î[.§ÙëÓù¢s¸\x001c¾§¹\Xï#½x&°pR&,F\x001e§ØßÁ«ËÛ\x0007¢¨óÐ0\x0008õMúæP5>+X\x0008ï_\x0003h6JªdÞ»5Ðàj6Ï\x0006ç$i¸aúïa~MÂ^`¬¨_5\x000fÞÞÜßÂü8Lf\x0013YÇBó¨M%iÀgN±g@óì2K£]\x0003ÍD2':&-¦J¥ÚØù-X`v-¡¹UÐ|zöðVÎFÃwKÖI©ü\x0006\x001c¨¾sï©H¿²ã{ÂMÂåg7\x0000s\x0000Î*Íõ\x001eÝ®~ÜÜwB]÷Ê£(Ekm'&ûlóó{ü\x000b÷=XÆÂ_Ê9W¥ 6K-¢6ÞæÇÏ\x000f=ù\x001d½zvtñí#t2\x0015ãçß\x000e<\x001füa~¿\x0012à×ç(jpô9\x0015ft¯C\x0017&D83è<ù÷Ö£l*á@¯k.\x001dl÷æörsÿÛ0Ê\x0019\x0007ÓÇñ0É æÙ0YG	ß¬
ÁE|ö§_®C±ø^GúÙâ]þ|s}}³§\x0016ÒFO/ÑB\x001b\x0003(p´\x0014R·ójóéòÁ{üêôää´U
Éx2ÇÉåä)úq>'aÒrt\x0000Î6Ó!Pù/\x001a\x0002LÕâ\x000fIÿu\x0013\x0006<1óo\x000faT;¡á
L\x001aVÖ2\x001fhÞ]]ÞÿÆ©\x000b\x00081¯"ÿv\x0011Â)lPph\x001f\x001coÉé³ñ·ôò'loLõ\x0019S¤#÷UÚ\x001b~¬Òq´\x0005Ü\x0000ºwjåS@èýÏ??¸\x001aO\x000eÎNÛ²PR¥D;5Í´{2\x0006\x0012\x0018V\x000e_ßH¶GkJ\x0011©,\x001e!¿Û`ß%!\x0015H¦ß®yô19\x0003Õ#¤\x0001¡HÁ5ÚT~ófs»¹»Û|\x0018ÇS)\x0011BMÓ!fàáv¦<Ep³$ªæ/\x001f\x000f_
\x000eÐéD×ùy¥áÐ»t\x0012ì°=m,É¼\x00180_\x000f\x0005Éòo\x000fÀ8dN^Ã\x0010 ËtàDTu`kð9´ÝëäÞ\x0008¤Íª¼ð$C\x001f¢Â<Þ\x0015à|Jjò¢séá½'öÁÇM×ÒäÀ9²)óo\x0015¾TZ:ÍÔ±ø¦­á¼É\x000e=~[e9É\x0018s=ÖÀÃüÛ·smný\x0006|.ëÓgáwE|è(¬°óo\x0017^´$Ë	Ó§²¢?\x001e-åþê*x\x0018fÌ¿=xX¬\x000bañlÞPÒ?ÈB¾lçþãóµK}n0* ìÎÆ=¼'B8Ê1ª¼\x000fy-IÍÖb;µoÎ16pðìæöc#£\x000eõnöwG(¬©Y õaUs\x0011"¡>ïe`¥gn¸¡û$[74¬ð#½¿\x000eê·î.SÞ\x0001ã?÷¶IÀÓ$evàÃ¤ð¹\x0018\x000eäáSÞó\x001bêLÝçÀø§v»Bh4>ÕhÑChðìpÙ¨òÅD»\x0015ùÙM*èxûå¸\x0003\x000flªYxJW­­³9KF`sR~}\x0013Ñ¬'=¶pÈ¿\x001d|pOÈ­9§`¢/þ*Æµ×ùÀÒ§<\x0010_%ÌAT>r"@a¨ü¤; ÆÕ\x0008\x001f¸;ÍDz\x0003g5Â?æ'
±0É.D¼\x0014ïíªL/Í»Íõ\x001d\x001eg{cÍøéJ56ÁFÍõ|¢UaZÎwG'çÇggM5£B(UJ'÷XF	e"ä\ãr*é;Ã½Ù¥§D\x000c¸-á3\x001eÏ\x0019/z§0\x0004Ê¤T\x0001<\x0007\x0012mÏBðrè	\x0016®%ïo\x001e´*s\x0019ÃàVþíüÎáPR\x0017\x001eØ¡ÄöÙ=´;\x001bÑ'\x0017ÂO\YÖ\x001e\x000b\x0011}y%Ò¥Ï®
éíeïbÄÞ\x001c®(²\x0013àF¯J5lÊõS\x0006,½È¿]FjÊ¡\x0000_!°FÒ\µ)kê¨õSF¤\dì¥Tbü©i£ Æ^Æs5Ñr5J­\x001eÄ7çPb{\x0001K;\x0007%£èiÉå\x0017^®}{{	\x0007äÍ\x0001ÎÙ\x001e£!ù·\x000b\x0011\x001cm`uR~\x0003 Fz0x3¥»Õý¤YÌlÂ|þë/ÿ¼©
²ÏîÙ}>§\x001d\x000e%ÔJVÃ§¤m¦LÄÿëôvóùæjò6wÁîìóýîì07KëF\x000cdý´Ù*o©ÀÂ3N«\x0015\x0011Sô¡\x001b\x0011î}$\x0006aà²ê¹ª²\x001fà
\x001ak­Îq*LëC>U£Qn'©\x0003È\x00188Ò¥l¤u\x00101©\x0016ÿÕh
#âs\x0019éã(c\x0019Ñ§\x0014âu\x0010ñ½
ÿÕ¨\x001cõ]Ñ\x0016w\x000e9<RÃ\x0004WBLáûôÓ»\x0018Ez¬HÙ\x0012/Ù&]¯0cåÿõ	§\x0011O\x0007»ýÒUvÖþg\x000b¿sêñY+8¦.t\x000fæy]pÒ«7\x0007'§¯_<·³\x0010çáI®\x0017ÇCóö<÷ÖAaõàò\x0000\x001füMÎwò	êPu^$	 àK;>ßÿîÇÃ´\x001aÐ\x0017°.7_[`ä7x"\x0000.¸°\x001a\x001d\x0006éAª.Ä(£\x0002­=çyîh\x0008~wÓI\x000cé¦.<§Y\x000c'ÀiHer@i«\x0001â;Ô¾T\x0004SR]Ñ0ÑÈµ\x0000Q ,ýt\x0001*Æ¦\x000fL¯P6º²\x0000ÕZ»·\x0012¤è\x0001%ú\x0015°U(\x0001\x0006[?·\x0016`ê~º\x0000áò x¯¯UE\x001e¯+ñ\x0015ç^¾|_Öx¢BD§¸Dr®W\x0002Ä¨Rúé;c\x000c\x001b`ï"1nÇì×úÀI­-ýôÙß5Þ\x0018¶¿?pò\x000fð½¿þÉ½×éFý¥²þî\x000e0 ©&{¼\x0017c(ÃR¡X»õä§R\x0018¹Ãæ\x0003ý3ßùÁóÓ·ÇG\x0017ÿÏct[swà	EÚt
+ÒÅ¶g|³}s/^\x0012É0¶\x000fÏP±\x0002/#5GÑ(l³ïu7\x001e÷.§0Ý&OQ þ?;³ÚÜ¹$F\x0010ºà¼§gFØñýfN:Æ\x0014vgîN<Å1d\x001f^8¤/\x000b\x001f¤ü°ý_¦\x000b©×ÂJtxê®§"\x0011\x0007À+w7|`<\x001fáýòé/W?½DÓïìI¹ËìÙ\x001aøLk(ÕÝpGøÀU/\x0018ykDÓéVtpzvôöôe[	\x0001+A·>B¢d|\x0015(ÝQé\x0018X %¡ÜO¸#ë#Ü\x0016¦áeÝQXK*ÅÒ¹\x0010wvðlD/YU»@5îRY\x0016\x0018´&®ö12ýô~gÇ\x000f;àD§\x0004ô\x0014ç\ïÌZ³X\x0000w"\x0016X,É÷\x0010y\x0012£{$\x00123\x0010[¥NB)ê\x0012jÒhDí/.¡\x0016k}gÚ.é§\x001fÊ\x0012Q?¦ Z\x0016pj¥IÔ\x0018H?}©Q\x0000}æ ¹6CªÈÑ_ÛÔôxÿÛ_Äg"«hòd\x001dÌ*õ{\x0000uH1iê\x001aG[E
VâÄýG\x0007oÿtvzqþ8áN,k&¡UÔ\x0014S;l)Kv¹\x0004Ð½GC°?Ú6p'\4PÉô\x0002úÅ\x0015ay\x0011¨Ê\x0005\x0008\x001a\x0008Ý\x0012ÿ*éF&1Ë+é\x0000ë½%)mÈÔ\x0017±Q!4~«s½øqóµÝûòºÙ4|«SÍªÙ\x0001Æ]ã7Q\x0006Ã\x000e\x00046å\x0006HVP»mØ6f5Æ$÷~ú\x0018¥p°\x0014AÇtkN§¼ãµ\x0018Ó¡Ó}êH\x0013\x000e©\x0010ÙÄ­"5#Æ¤j·\x001abªí°ÝÓ¨(Ù\x001a£Iu\x001ei\x001a¹\x001bRLåZ¥-t\x001f£/ý\x000e\x0008ì-
ÍÊ\x001dÑ®ÉgúécD<ÕÀñ¬Ä\x0001a\x001dÃz\x0018¬V±{5jUâý\x0016FÊ¼Æx¡VK\x0011üû¿ýíîÁGä¹³ÿYQäoÒÞ}\x001c\x0016ØÑQ2
ÙÛÓV_Ü-U*\x0015¸\x001f%?Ë\x0017_ödË©°\x00069È\x001e*¬ÊB¥ù­½Pù¸J¦\x001eÂ²k²¢dý-¸Êqo&\x00161©ßÎ\x0018ÕutMz«)\x001016¿^ÞÞå°\x0002ü\x001bÔmWMjáé9\x0004W\x0014×sÚÈY(Ê>, þöìèÝñÙy\x000e+À¿yý¼>Q\x0011¦\x0012À~BIÕÍ\x0012Õ6
iæZÎÞÔµg\x0015D.s½Ø± oQð\x000f$)\x0015)¸°¬¯iè_ âóéETÙ\x0017$Þ¬-Õ¡*-Y\x0000[ê°Þ¶0¶\x0016=ÔÁ1\x0012©ÿ\x0016 ¢\x001dWD\x0013\x001dÿÕÈöVâ;b0<T'!ÝÃ*âCtWê$tÜe-O¢"Âüö°¾ô\x0010 Ãjè\x0011@Ë:çºì\x0015©X£ÛZ¹\x001e"Ö ~Ä@FDâK%\x0019ñ\x0012EIsg%D¼/øþÏ/t="Óù3«`Jö`Xm%J,;N?ÚÁ_ZñÁ­l)\x0008´
±ó¹úÏ¿ýýûËß«fM'éî_X,,,*U¤ÿ \x001a×\x0017\x0008dø\x0010¬R 1&\ùt\x0008­ÂÈ§\x0011pæÀ_vtð\x0002Q¾9I/rÿëøäøí7W>Ü|útYþa\x0007¥®GãJÏHH\x0003Ö#\x0015\x0002MDÍ¯D£1ú0ÍÍÇÍÝçÛ/hþq)ïÿr?\x0018f¸ØoRåj\x0013&¢§±HA
Z¼\x001fªh\x001dVß\x0000\x000e}\x001a\x0006>ÑñÙ\x0019Jm7'ql\x0016K3ÈçüI RQäüN ÂúÊL$Í\x001e¢Ö\x0004]Þø;eª	zwùéóe.µ~\x0004>öée\x0012H9ðzI>'\x0019ñ¨Ù¼;~ýö\x0018ª[³rÿ/ùÛæo;\x001féû|Ö\x0010\x0007\x0017O\x001c"cPa)¯\x0017-máðnw½\x001f|©fíïóù§\x001f¯cªÂØ"
gXx¿o>0ìåÒ|\x0008ªÇù\x0010(Õ_Æ\x0019»»'ûbûQø\x001fv10ïýô3\x0003CF:gÀEÁ\x001a
\x0013Ê±\x0010Ã&ùÊ\x0001\x000cmqæß9Ó\x0011DZ\x0013È¦×äéðpðe ú¦\x0003·\x000b­í\x001f|Ã×¡{ü¿ýéãAîß½ËåÞ'È\x0015r¼<-[¼§Ï\x001d:+®tï¸ÀóúÛÜµ{»p\x0008í½Rzö\x000cþ ¡]ýzùS)¯~¾lolï+$.gTM>TÞ¥\x0000\x000bp¹\x0010§ëøìå»ã·=ùòÕñ\x000eý³ÙüzýÛÕ~âÖæ÷µÁ\x001d\x001cþXNd,ûÍû«ëëËô\x0005ðÙ\x0013
ArqU\x001b*O\x0013óK«s:u÷üÿ¨{·ä:rd]s*@Ñp¿(i¥e\x0014ÉM²®zI[(%3)RIÊËÓF¿öS×8j&=\x0003îX ×\x0000"'Î>¦Ä[û\x000b\x0004àp8Üöêâð(¬­7g«ÜÛü\x000237R\x0017¯¶,¸\x000ejjà×jlª¤\x000b¨Úñ\x0014H\x000b£i¹L¨BAañ\¨Iù¬\x00155ªI¨ðÇ\x00186Ð#H!jTì\x000b5õ kEeÉ\x0001\x0004Ôà£òÊ}º	`gDM
ÔZQ1|
\x0013 B£\Z\x0018U¥qP5Ü¹ÏDJ]½GU&¯\x000bdã¨2M£:\x0015Õÿq÷\x000b/7T0éVcõðéòf'ç,IF+ÈêKGÑÀçX
\x0003\x001aílÙ¥<?8<~³·ºxµ:\x001e\x0005û\x0002Á°ÙÄòÀPoqy`©\x0019ç\x0002Áñ[ XêºY	\x0014
\x0001\x000c.ßÕ°\x001fÀ\x0016ÓÁ61ùeX,_gK$câ§wW÷`Ìà·¥ðýqïïèí\x0000x\x000ftwûþòþþ*\x001eñ¶Ãà4ßbªgoáhö~
×Øð
èìäÅêüüpë¯Ã·±·ËäÛ¬Õ\x0005ñý®ÖúoÝÏé\x001d!¾½ºÿºkêy¸!$YYîÆ\x0003Må)&8~\x0010\x0006/ñÂ)íô\x0008ß\x001e¿Ù>ù
¸´Ë/\x0014.Í¼Â¥Ý~¡piÇ_(\ÚÃ	GûØè®øø'/Ã\x0005ëwë\x0018Yyýßÿ\ÿ÷?Å°ívS'¥HùÎ\x001e:óÒÆ)4u\x0010êîÑ½8x~p\x001c£+¯WG«o
'wà0@° 8ÿËÃ
ÿ^À\x0007ÀûðìùÝúóíÃýýÎ\x000fj¬4±vL1\x0007-ÀcxÙ*RJ-\x0008µ.Ôó³×'\x0017çç;\\x0012æ\x0013À|Z\x0004\x000b\x0019\x0019\x000e0|!0
`ÔB`8Ì\x0019þ¿sÎ|c¿]]Ý\x0017vèõúêþöæ~ïøòá[¼	Ø¾Êc\x0003ÿaÕ#ÅPeÌÂ,q^\x001f\x001c\x001cï\x001d¯.Þn½\x0010è0%ó³,¦äÁ,)9.ËbJþÊ²RpbYLé¬³\x0000¦?\x001eìûß¿t\x0010tï´ã@Í}ìâ\x000c\x0007j+SCç°×óÔ5*\x001c¨5H­õÜ¤]wOú'knÌÍÇG7ëW7;Ýà±A'¹ä°)DlÉa3â1É\x001fÃÑ¾¼Ìî±Ü~þü×·\x000fÅÂ{õõõN\x0014.LÌ
,QÝÍ$\x0016')r\x00143O\x001f³üûàh+»5îÏÝÊ«;ø¿»Ó\x001bIlG\x0002ãâYJË\x0001Énlølæ\x0011Ë«3øÛöq)`²ï?
F°tñ\x0016&¯H0û©b\x0014/
à\x0006·\x0016Fýñ{Ø\x0007»\x0013&êî¹JÛxñ\x0007ßÈ¨TÔ\x0008rá©\x000c*¸úâù\x0012Õ¶@3âj2ýàYOOxøè¡ñfÍ¤º\x0018\x0013\x0016É_,&BBt÷É##Ê\x0012QV#\x0006Ëcd¾ühqÙ\x001bÐ\x001a¨JDU(A\x0012GÑÚTk\x001e\x0010ùÆNê~8¨\x001eQº\x000eÑy\x0013@\x00181¡SPù3\x001c\x00109T7LD4%¢©\x001eEè´»\x0015ûé;KÏ5
â\x000c¶$´õßYÄ
	 46ÉTÂwNª*\x0001Q÷7Ä\x0006DW"ºjD¹YÐ&
ÕÃ ÚF\x000cn:¡/	}=!Ù¥@¨QX% \x001aN&G³Éu¬"«fÄV}q\x0014uÌ»\x0001FmtþÐÍ"ïZîjÓ-9;l\x001cGØ\x0002£¤ë{®¦OF.:¢Q¸$±\x0012\x0019\x001aV¼\x00027\x0018}ÿ\x000e¤±³½ðêýEH¿µLÏà\x001dHCKFÎ0\x001f;ûK_y}\x000c£úÌÑ¦
(`t´fäô
w6\x0018^¹Ã\x0004Fæ÷Uv·Ð\x0010,{\x0012BO6ß¼³Áðê\x001d\x0006Rù¼ËÃ¨¯,°O\x001b\x000c£ÎØÙbxõ\x001e\x0003wãË\x0013#wyÉ>ÑTÆÎ\x001eÃ«7\x0019î£ªDüÔ(\x000c\x0018À¼ÈzºGÆ;\x000c¯Þe¸K
â0º¨e\x000e dÁcÅé4FÑÙeDõ.Ã­¥ãR<¡$Ë\x0013\x000eÕÑL¶¢³Ëê]\x0007×VæaDç\x001b+Aâ(úÉ\x001dû-jíw8\x0014ÈýxÌSÂó¤tg¼d©Çµ±al\x001aEÇ4jÓÈ2öñÇ¥¦¶\x0010/ðxaM^Ó¢cwD­Ýù;QvÌ·¬6ß\x000c²\x0000\x0015\x0017ÒÂà\x0005\x0012g#ý$OýÓº÷±×Õ©jüÚ\x000cR{Ïóu`z¼í\x001dûÃd,
×?\_>Ü]í>
jMÖ\x0011ÓUc}_õ	S¶4\:þp´º8;\x001c&\x0014%¡¨'´F© dâÐÑéï0õ²\x0004õ<\x0016$©Øª+\x0015,ÃÚS\x000cÐ©éc¨JDU\x0008M<ùEÒ	cÈ\x0005í/Q[j"¢.\x0011uý(*Jìú@\x001a?3ev3-û\x001bL=¢)\x0011M=¢ß<oã(J:\x001f¨\x0019\x0016-\x0011mËrF?DöµÂe?ºØ\x0000èJ@·ÈÏìKD¿DDÞµÚ
fûo`ì,h¾¬\x0015\x001d\x001c¥îÞ\x0002ÊÒúæ\x0011áx\x0010:¼\x0007&2í~F9áxß¿ÞÞÔj^`\~\x0010Qj¦D4µ\x0001'
äÁuÑô¡\x0003!"ºØña"¢+\x0011]5¢QtuÀI\x000cæ"ãt7ÖO¬ªGÜ\x001a\x0001³ê/
ÅéjHú¼GkEYÂ\x0006
²(8\x0019yg½ðú\x0005£4íÒÂ¦Þ
ÀÈ¬¤+¶éÃ¨;zÃØYÓ¼zQ[\x0010PK^­\x0006C	;\x001aE­¦\x000f£í Úú/mÐÙ'ý4@ä4Q×y"¢ï ú%~iÑ±;¢Þî\x0018\x0013}Y`\x0012ïêµtª½åz2#ï0òE#×eÙqúA·vLAð¸ãÖ)\x0001UBw.*Mõ[ëý(Ù`\x0010Q¢\x0016QB!
%B°¤8\x0003r\x0015<'Bl¯\x001d(KD¹ÈQT%¢ª\x001fENå<³T\x000f¹-B¡3\x0010êP/r\x0010Mh\x00169\x0015]èª\x0011Ã¶GßYX¼8Æp4¬­ZX\Oëä3.o\x0018y×..Ò0òaäË²Løîþ\x0012~\x0000ûËéõú}Ò\x0016z¹þ<É5£((Ü]ºT¢-^àp`zçÓ£\x0017IQèåÁë\x001d\x0019Nt¢N¥þ\x0001îØSa§ý£x|5,ñd%\x001eJ\x0001OñÔ!3àY\x001c<ÏûõÕtª¤SKû´º¤ÓK£3%Y\x001a-éìbèt/ç\x0013\x0004þ0øzýpw\x0015\x0018O/¿Þ¿ÿy 49øþ\x001a}!òÂuªWÝSå«¯\x000f.Î\x000e\x0003èéêÍy°Ã¢Ä\x0014
%®t\x0018Õ¸óHzë¸¿¨Æ%¦lÁù\x0012FS	Äô2æ\x0013ñ÷jLUbª\x0016L\x00135\x0013q4\x0005Êy)óhÎ@©KJÝ@éX¼ÀÀÁLq@iéÈçô\x0013áãjLSb\x0006Lå¢\x0000>\x000e¦§5N¶tßDiKJÛ2&\x001f¤¼\x0003è\x0004gf?DÛéJL×éó\x0002>\x00021\x001dù\x0011±÷dL_bú\x0005¤é:\x0015j\x000b4®sÏ	Ó©~¢`\x0003f\x0011OÖ"«bTqzM700(\x0014>Ywû(yµ³»	5ìBÁ».7ÎN"\x001b$§f0ï¼cÞy}\x0017ÌÒ\x00108eÚ¼Ì\x0011G7Ã"â\x001dóÎ[ìûßóÙ;\x00067Xx\x0010L%Ó)¨CAs\x001aÎ§tQª9;\x0016·ø¿g<;67\x0018ùp¸¡D\x0014	M\x0008ÐÈÃ5ë;&ï\x0018yÞbåÿñìXyÞ`æýÉôq<\x001d&ö(o4\x0015k\x0005gd:§èy±X3/:f^´y%ö7÷\x000cHiIØÊû~I`\x0013e÷¨ÑrÖø{F³³\x0019Í(\x001c.=rJ­çæFÄÎ`<Eg3\x0012ÝDg3\x0012-vÄ Ã<\x00158>K¯°Giâ-ÍH4lF\x0002\x0014P\x0013¦¶xÜÐ±³uÂí­'cvö"Ñ²\x0017YÄa8=fèjFEáÜ5ÃV$:[XìV$:[hÙ¬ÃÜ\x0010©)¤ahi8çÈ-\x0016Þìhç7
Å_4;\x001f¥··pvã4-¶\x0013*i<5Ö­hó\x0019¶"Ù±I²Å&yµoi8=\x0016Íi¦Tæã);]6,v¸\x0011¥ËùTB\x0007:¤9\x000eí²³dÃ\x001aÌe¥>£±t.üÙ&ñiî\x001c3½X'3=¥ëõÍN	\x0007Èðâû¤\x000e`0ËA\x0019'(Ì©D/TH\x0006\x001f\x001c\x001f\x001c
Ó©N-Îtf1t¦Ô~O?è¨-_\x0006¼¯?_Þ]
\x0008Â2m´É>òÙ<ª'vÅ(\x0004º
o~\\x001dî\x0010\x0003Í ¢\x0004\x0015- PÓ8­Ý§½;\HñQ)KLÙ	Ú.g\x0005ÑxRMZð60<õªäT\x001dN]bê\x0016ÌpÀr%èyíñFMØÜçÀ´%¦]ìhú\x0012Ó/\x0015³\x0011MbåìÚÎ&ãù·pvÖ:oZì<w(\x0000\x001f\x0018Å©ÏîÐ#õ&ÒÎrçMëýo\x0019ÑÎzçM\x000b\x001eî+Ó£Ã\x000f'ÐGÅM \x0015Ï|À¸\x001f9\x001b»éFR\x0012â`º4Îb\x0012MÉ¥FJT F\x0003\x001cò>\x0015*® U½Úð¾&Õ«õ@Ò/(!\x000e'7è°+·	g\x001d%ç¯\x000ev¦%«~ùù´u|\mâÃ&õÑ\x0005\x0019:Í)\x0004·K§h\x001c ,\x0001e\x0003 ñ1L\x0007>Ó\x0011v\x001fãS%ªäây8\x000b¥ßWØë@9£D;ä#Æ\x0001ê\x0012P×\x0002z	tÕ({ÅÝ}¿K= )\x0001Mõ\x0012)âWjxÇó\x0015Å.Yq®\x0004tu°ÉPT\x000c²¶ÞçÝpò\x001cô% ¯\x0005tTV`\x000eÚto´ËJ¿Côg\x0014`á¤)öHj	CÈ»vºÒPuÂHÕBJN©:Z|Iê:°c©ûúS#\x00085ÊtJiQ_Ei-òÁ»_*T\x000fØ±Ô}ñ©A@P\x000bô)\x0005\x0002n"lôÆTXÞd«\x001f\x0017ËV\x0013vlu_zjÐyÒ\x0004¬VYÌb\x001aÑ8À­îëN
\x000fa\x00187TK\x0012]Ì°-Ô=Êqª&ì\x0018ë¾ìÔð\x0010BØQæuÖZ3ÒäKÝq§\x0011Ú\x000e¡­$TÅþ40£ÜbhîQ(·\x001a°³ô\x0015§\x0006\x0001-dççeÜ\x0012Z¢b¯ß©®\x001e°³ôõ¦GPøp|¥B\x0002¯|\x001eÁ]\x0002?£\x0000Eg;éM
\x0002\x001ao(I¨¼E	öòQ\x0016S5ag;éKM
\x000f!\x000bÎ4r­F]Hé¹Ï9fª×%ºív\x0002Ò\x0006
§¡ò(ã«à
1\x0007§NCÑÙOúbXðÃti\x0019\x000eN9ò\x000eH5^g3\x0011µ	(:²Õ2Ûj!i\x0018;Õ§\x0011Ý¤/Õ5HÈ%ÄÌx\x000eWÑ§pÇä}ÇwÈ`#ìì&¢v7Ñ*÷\x0014ÁUi\x000cW|¶ó±è\x0018kQk¬Ã\x000fIeQ2\x0011W\x000c\x0010*G_ÙïRY\x001cE(;ÆPÖ\x001aCeü¾Äyè=\x0018XnÍæý£n{Õ\x001dS#kMÎÈp\x001dVôFæ \x0003úeg-ËÚµ\x001c+\x001bC§âa*kÏ ²w«	;+¥¯\x00177Dh­dÔßV\x0013TJÌ\x0018íáäS²í\x0001;±Ø(°.Ü\x0013äÞç\x001c£
v\x0013O\x001cm\x0010}LQÉÃt  b?]öÝEö$ã ;¡¸DOwW_.ï¾]]\x000e`jÔ\x000b\x0003¦\x000fûµK\x0001k<ô=:QÑ0´Ý]®ÎÞB\x0013ù!VW8;\x0015þÚDkE®\x001dr@*\x000crRÔ#âiÜõÝûË/OD]/\x001ekÜ¦]äýÞéÿs
Qãz6è^TºìPAm7ì£Mû"U³® `¼« 
\x0001E	(ê\x0001Ã\x0005[`p\x0001é\x0010íÊªãÓ%^\x001e-ùìòø|Éç\x0017Ä§e/\x001a\x000baÕN?ÐË¯WÁFþp{óu=x½¢9ÕCKoQËI\x0015ÂúQ°dÓ\x0015tõæ0XË\x001fNß\x001cì¾cIÈeê«Ì©¯
ÌaD\x0015Kf)\x0016\x000fllC¶\x001ddÛ¬\ìæ\x0012ÙÑ1Ì»\x001c»ÕOåñµ1I2'\x001d60\x000bOw2a·g\x000e97\x000cRO%V"sÙ3¦á\x0007`L\x000f?Yßß\x0013õ××±ýËËûûÝ\x000bÏø|Öð\x0010%Gý4±5£¹ïm¦¯O\x000fÎÏ	ýÅ\x0007G±¡}Xç\x0017;Ö!¡«\x0012]MB·*j´DtªâÐZÛïnJt3	=¸Óî­Á5	äè\x0013h-å¬è®DwÓ&Á/pgÂ\x0007ð¨ê\x0018^í)Ó\x0017^öùpñåÿ öÎ:å\x0016ªe9láá\x001e!é¶iÏ²ÓÛ·/»Ùv'	¼³Jù´e
ý\x0003"¸dÐ½¨iÐõ£Àiã 3Ãû&ï\x001d1Ö{g·ï¾üº»MBlÎôI±^hIÛê÷\x000b)\ö½³ð×7»$¾	U¨rÑ¨ªDU-¨Mþ\x0014µ¤b³©o?\x0008Õ \x0012Õ,zTmj\x0017êJT·hT_¢ú%£i¼#\x0013¶@Öaå¶¬¼c®x½úÛX;ö/Ô`©^Sð\x00033ýóöþòËÏ{¯×_¾º|ØÉéÂ	T`[UM·¨JIû\x0015<ºæ
§¤¯NÜ{}ðæÇÃÕÅ0¤,!åB!U	©j!£ôI¾¬\x0012*vULÊI\x0014°}áë\x0016H]Bê¤)!MõH2Ïðà®¤ÂN¿Êæ¶ìq*`\x0003£+\x0019]=£Í	aôèZÕÒEG\x0014O\x0004q*!Ët6k\x000ej(¹¹ÑáùJ\x0019om\x001eÊ\x0019(»&h¡6¨Lk³)­­Ò\x0001ÄH£R\x000c»ã(CJöTOZÊ\x0011âÕV(`jêþ¨¥B-­\îþø(££²cøBÍ\x0010ï!^mêF\x0014$ò¢9£&4ü©ÌýZHÛ´\x000b\x001dÊµäÕæ\x0012ÒÝrk)hè\x0016\x000f\x0008y!ep¦Sú\x000e¥¯§¢zlÞ$¨1Døö²ä\x001fç(ÔSQ\x0017ÕF\x001dä)V© \x001f\x0008¥Ù4\x0008|êÊ£²cÔÅBºè\x0018uQoÔ\x001dcû8PÒ©Uþà\=%ÐX\x000bÙñ~ÅBÝ_ÑÙyDýÎcí¦¿û<í<Òç¾âQßá\x0006Ê¹\x0014\x000b5us?â2É\x001fµV\x0013ÇÓ{*³WnÓVü©~|Õ;ù¦õ"îåëjÇÈpJ"UÂQq\x0011ó¸ë÷¹oÒ)öÞÜÞÝ&ÅõõÕû\x0001M
¯rc>ðÝS¸ÛÜ+?Ê¥I×oNÎÎ@âèèðÅ®ó¸í\x0007»-ß¤UTb
,ÝWX/è(sÝ>Êäkâ%§là\x000c|À\x000e\x0003Z$ÜY²³`ª\x0012S5
§§D\x0006%\QÙ¶t×¿ØkãÔ%§n\x0019Ns¨`8S=æ>;îO·ß¬\x00065%¨i\x0019ÐpÂ\x0010*[P\x0005­aHi½?%BS\x000fjKPÛ2¢EG\x0013G\x0014+o³ùi<]éZ\x000c\x0013Ë\x0019,

-P,G»\x000c*g\x0019O_úñ¹½·²îÈ ,?þ¸~¯\x0005w,(o1¡2,tG}b-ö'Ò9Fwl\x0013o1NÉXY\x0013A}V\x001b3,\x000féS²SãI5ë\x0015_\x001ftÒS\x001eöÞ®¯÷>@îäýû»Ë«\x001d¸ÐSÛE\x001f\x0019óàS³	NDnïà·Ý\x001c_ì½=8Ú{¹·:q¶:<\x001eFV%²,ãÅ&V	Qûê\x0017ÏûZEíÄ¦$6µÜ\x0010sB6ó!3\x001dg°*Týµéß!\x001eÝÞ|º\\x001aH³bÒ¬ÑE´\x0016·\x0003ñHª¹sÑqtrüjuðjwZX5¾5ý[Ä°^P¯±Ô¶W9F²y\x0012þ4\x0007­g%­ïß#£å<IÑ!-ª`;ò]$ëNÛ`yÙA\x0000.=u#­ÙçÖr»\x001a
\x001aKµ#\x000b¼¶T\x0017\x000f´¼¦1\x0016e\x0010V$1Ø©&ãj9ÏàÊîàÊÆÁU
|,\x0014íáÄµ$h&eÿ¾¡\x0011×vl\x0002üµ	7\x001cb\x0014âÊBg>ãÎ5ºNtp]ÿ\x0012|\x001c®`)]\x0011pÃeõ\x001eNØ	×öC½m¸¢Tð\x000fÇCÎ\x001bq\x0005¹
Ö$\x0016q)G4\x001c\x0016g±¹Bv¬\x0018üµ	WHÒ*µÖ`©ò(>o¤ß¦\x0017XK«»´m+M@\x000fV´.Ï\x0005cÈ0ø¾OÖ+»vL6Ú1áR+\x0014H¡~#\x001c\x000fØ¼\x0005J¶g¡í\x000e®l\x001c\É\x0014\x00057\°ºtØÉ[Û:ýUâê.®nÄ\x0015"V*\x0002®´Ôø3ìg\x0006ÃYhmÇ,À_h\x0001\x0011\x0007WI,\x000fÔ\x001cëh!v8\x000f­ëX\x0005øk\x0013mØÑ0à¤@+ÝÌcëº3Á5Î\x0004Í¢o\x001bÇÖíëtøå*\x000f®îW\x000c¶á*Öqsá¯M¸pÉ¶)q£`'¥P(Ý\x0017\x0005o¤U©\x0000m¡ºV6,§rL-\x0018	b*»3\x0011µ\x0002·{ài<ñ(¦cØ+â:*I\x001aZÛWÒjdµÝ¡µCU<\x001c\x0014Á`\x000c,X
¤uóÎLÙS%|>ÞO]Ô´5¢c\x0013à¯K¦uÝ±uË\x001e[ßqkà¯\x000b¦µÝ`=\x0013¬êÒªÓÚ.í¢ç-¤KZ¿hÚ²\x0016>ÐökáÇÒN*¯Á5]\Óèà~÷Áå}½t.;e@÷Piõå\x0012¨v\x0006/FÐ¸ä~§#¯\x0014,ëômu\x0017Ï¡À
"û;»Òò¾\x00129e÷úñ î&hêb>Ð0Ê\x0003m=UÚ\x0012Ô6B© 	ÜPY¬\x0012ÎeÅ\x000eµ-PÅéKNßøå¥ß|yM_ÞÏúå@\x0012VñãGÔØ².\x0006:DXPY#o\x0016ÒÎ\x001cå-ÔIJÍnÁ¯ø¦BòmQû*ÒÎ$å-³T]Úh
ÊùëyÆÔuH]\x000b)¬'joehás£t{J\x0015igAñ\x0015¥Ãy\x001bïñ£æ)²¬J.ú	FM¤¢³¢DËÒRæ\x001eßZf+·\x0019Ó~RL\x001big{\x0012-ûfÞ1\x001cË6ZÐ´\x001cÚ(MÒ4P*¥c"LpP\x0018-Fqnáì,{Ñ²ì!qc[]Ç¢è#zNÛ}¿·{\x001bhgÕU\x001fü¹¨x\x001bGÔ£.ª,Z&¸­.T\x0015igÕU\x000fý­Èæ{à2ø+>Î±ê\x001b\x000epõXË²tK\x0010õ\T\x0016"\x0015Y5ÚÏ²dÇ>É\x0016û\x0004Ý+ñ\x0016j¿Úg\x0013±7\x001d]ç¹Å:IpJÓìã§g$6ÃçYN²ãÈ&ïù;»ùá öSO^Få¤Ò½\x0017wW÷_\x0003ÑzwFIð9ö\x001d:zRà¢7Âjjú­jÇ\x0006ÝºÎ\x000eÏß\x001f\x001eìH%!DY"ÊZD(d \x0019!É\x0017ø:­!ûH»\x001eÑ®\x001açªDOÊPÿ¥²=z*´p\x0013ßYWèàÑ~=\x00146¨ô¡¥\x000f-\x001e¯×0êþ\ÔÅ\<½ºü\x0000¿?¿½ÚµfÂ8:FùMZ²¨*\x0005Z¹í<=\½ß\x001cî\2	Sj±¦Ä4Åt%¦[*f)M¤s½ì\x00029;k/v\x0011ñÎ"â]E¼³øb\x0011ï,#Þ°¤óÔ]CYLü\x00019t\x0012\x0000ÖýôÅ\x0016LÑYF¢a\x0019A÷0Oì'¬§\x0014ÖG©MÝh±«HtVXà*b±ïï¦Æ
\x000e\x0002ÝóÅË«ë«O7ïwûÃ^Üñ\x0000áE¾¢ß\x0018¤ð_\x001e\x001e\x001d¾Z\x001d¿(\x001dâ>¢,\x0011å"\x0011U¨\x0016hJD³HDW"ºE!2%º0\x0014m¬Ï«»õÍÁ.ÊÁF\x001aMa\x0003m\x000cv¯\x000c£fÞ\?%/\x0010\x0016ó«³ãUoÁ\x0000¤¬\x000cç2Ôs×\ï«\x0018Ûó¹jòé
§
Rj¡#©KH½PHSBBÚ\x0012Ò.\x0014Ò¾\x001e2X\x001fUVã5 \x0016\x000e³zúÂ)wDVÞYÚPò
â
Fèo¡ì¬o¾Ð\x0005Î;k/mñ\x0008ÖkF\x001b~PTëxÞåíÝ×«]i\x001e	O9JËÔ\x001cÝH¦(Ð¦ê5²y«³7;\x0012<D¿ R¤ÈÅ\x0001Ê\x0012P.\x0010Pj¦\x00044\x000b\x0004t% [\x0010 ¦\x001fé5eÕ«ðÛÛðüúu§\x0017\x001e05£

\x0005òð\x0018ÖT4Îì¶N\x0012«ÓÃãðÛÛð|óf÷%éß@Í©Ä\x0005¡\x0000þ®¢m[8E-.ÆoÀU%®jÄ\x0015úbC­n ü½àeÌ«K\ÝËÃèb2\x0016åÂ#ódÐsM\x0006[âÚÅãº\x0012×5â*C7æJQÏSÃÃ\x001c!ð¤ÒI\x0003­/iýr\x0007×öãZV­^_Þ¯o>
^ñº}u5:KhJEò\x001c ¡ÿ4çëÕùÁñ«1²\x0004\x000b\x0004Ô% ^  -\x0001í\x0000\x0019öûØ¤+ü9hds}ûðn¨\x000cÑD\x000c4â\x0011X5isQ¾EÄ\x0008\x001aØ\x001c\<ßÙ[­ßnK\x0016í¶Æ\x0002²\x0012ö®ß(ZEí4\x0004¦\x0002\x0012ÐT\x0003zÚ×\x0005\x0017§£Ho\x0004.¤S\x0001m	hk\x0001ñ¶\x0004è\x00083Ìm[OËª\x0000]	èª\x0001y\x0014 \x0000@æö¥À\x0011T¹%]?)§\x001eÐ¾\x0016P\x000b
Ur¸%£\x0011D=2\x001d\x0006pê\x001c,ô±õMå\x0010J%â6·vb^Ó7~ÚY«\x0001ä\x001d@^=¹\x0003*7,VçÂ\x0010rE«Dö+õë	EPT\x000f¡Þ·8Z£8N\x0018BCC(¶¨zU\x0010vL5¯¶ÕZ_Ã
uâihi\x000c'ÏBÕ\x0001TÕNdÁ7ÄÄÊ\x0000(°µ_ØUÖª ìl&¼z7Ñ©\x00159\x0010*¿©ºw>ò£&²Õ\x001dcÍ«­µN\x0016\x0010\x0008ÃÖg±ÒsZ(|òvÂ;ÖWë¿á+wÌ5¯¶×ÁÂx	¥#cCO¦2Ô\x0000ÎJ\x0016Õ+9PdÚ\x0019´Ck(ð¢­QSíµè,\x0014Q½P|øÈ	\x0010\x0018qÇËM¿­S¡è¬\x0013Q»N@Ô\x0012\x001bV3øÆ¼[±§-ëWÕ\x0013vf¡¨ß3ÙÏ«Ïú¹w¾¾y¿»¡LØù|¼Ã\x000ebR
\x000bZå¬ýØNñ#àîÃÊ]=e\x0008XÀ}E¥ÑÀÆS2*\x0007I;\=Öå}pWii\x0015¯.yû5ÑK\x001c`S\x0002÷û\x000b-\x0011ØÀýÊè%\x0002»\x0012¸/ó±D`_\x0002÷E_\x0016\x0008\äÚUë«,¸kÿ\x000f0Ä¼c\x001f5x["qGù\x001eg\x0006üd±àLö®¬¡$,Ìoá¿Ú{y\x001b \x001fîöþùp}uy³\x0017	×\x000f\x0004ït¾ô\x0014ñ½áÂÅÞ\x0001æàíê\x0018üÀzq¶÷Ï£ÃÕñ^ü\x000f\x000e.^À\x0017%¾Ï¥PBy\x0000Àç$ÍL?\x00165\x0019_ørêèK5Ð@cãoë[ÃÑbf|Uâ«£\x000f"\x00179\x0004òÐØGÎË|Óï#7\x0019_øzâè3»ÓpGc\x0005Ý\x0002hòôÍ&ã\x0012ßL\x001c}å(ö ­¥¾nÎqÔê\x0017ßøn"¾V$S'ó­ZÀÏ%ÓÂÎ=y|ï§Îý¤ÖE¿¨wì)ÏýqeúTú2¢Ë¢\x00173mòøMý¿ÆÊ0yhîó¹'\x000fïn[\x0013÷-\x001e¦EY\x0000«Qä\x0010ZXæÉ¯ÔÌü}OÝ¸ k()%¦C(§9Çø¹g?ïl\|âÎÅM®áÈlß	º\x0013\x0017}ÕäÉü\x001dÓÏ'Ú~hÍ\x0007á6Æãü»5ÿJÌÌß±ý|ªñ¹_@h-)8Ë«L¿B~2¿íðÛ©ÖÓÝ\x0003Ô]ùlè\x001aÖÏí¸ñÎæÅ§î^R`N°:l:µ¨^t¬¿jýEV¬¬7øDèÇ'ów¬¿jýëÃ\x0015Î~\x001b/\x0002£õ4Äoú÷ù»§©ÖÙÓq\x0014³SÖ|Îfý¢cýÅTë¯tÎQpÅî%rqgÿöu2Çú©Ö_1\x0010¶°è=å+æ?\x001dë)¦ZOèãÖ_çîN:\x001aÉç\x001eÿï,¦:ÏRQÏ\x0005¡M^¿ÒP¯\x001báfæ\x001dû#§Ú\x001fÅÖ\x0005ôÛ¥ñ§éÓop1¾\x001btºz±¿vÌÑ²¨\x000f\x0012èy\x001eý¾XÕdþÎêSW¯PÔ'O@Ç\x000elß"²õafæs»ì¬^9uõ
ò,\x0010}Cz}}\x0002=Ùsµ+§®]aÈóá$Ó\x001d\x0006_\x001aÚºúµ¦â«ÎÒUS.g¤Äë ¨­Ø$Í¼xï´X¡\x0007øÁ´è\x0003£¬\x000eélÞÀ\\x0016GSýöÏío¡}/ê\x001c<óð\x0011ÞÞ^¥ÄÕXÏ\x0015e¨>Ù½ê©d½jTlc\x0003}b\x0015Õ9ËGmùÞ\x001c¦ôÕXÓ\x0015¨^îÊaEXQÂ&X\x000b\x001a³\x0002a³B¢âb\x0003kç%¬\øÈª\x0012V-\x001cV°zá°¦5m°ÂQ§0\x00136ÉÔV%°Ò\x0015¶ï´ÂÚ\x0012Ö¶Á\x001a\x001ecî\x0000\x001bü)\x000c¿k®,Áö\x001b>´Âº\x0012Ö-|\x001aø\x0012Ö7¬ÈU\x00020²\x001aGVûGw7¥î
Üõ.NÃ\x000fzª1Ç·^ÞíVé`VÓm\x000eC\x0012PÖQ_\x001d!·ö8<ß;>ù×êl\x0004¢(\x0011Å"\x0011e(\x0017¨JDµHD]"êE"\x0012Ñ,\x0012ÑvQLõ\x0013Ì\x0015&ß>|iÿópùçÝz7¢e9ÁA8A=áµö.GJúõT'\x0017obÚçÿ\¬þuv0LXto
Ð¼©PÅ¡ÂZNÂZäæhÌ=ªïî\x0013¾_XÇðiB^=`\x000c¡%v\x001d¢äÊ6 \x001d8©ôò~¸©\x001aw\x0011y5b\x0018:lþ¬\
\x0001"E$
\x0017Ôj\x0011\x00100 Æ$ó*Äà¯Q\x00057b"ç\x001bpnûùÇÕª¨j\x0011!\x0018	\x001d\x000f¦ïÌôÄÏl@\x0010|"\x0004Õ-gÏí1ZÎpaëª\x0016Ëúîýåíßø§uÿ+¯kÇÐQt\x0010d\x00104v¸Û¬GÂ¼\x0006'|Ö>¤ªtz\x000cÇo
\x001e§Î§Áeì×ÝÔÅÞ÷\x000cãûz³#t4ØÑN(~\x0006Æ\x000f=Æ\x000f\x000bc\x000có¥÷µÃ\x000c¯ýÚÊç,?¸m%Ûèó\x001c2<»!u\x0018Ê.$ü¤~N}:'6\x0015\x000cÅ9IÍ?8cN¾ë}ïwKûÞ¬ÿ½Yý÷ç\x0008i%J¬C+È¼Óô¯G+(­í3­³àáç/ëûûË½óõÕÍ×Ý¾ÿyç¡\x0015ÔmíFÎ¥\x0006\x0005>×ý²ºÃ×§\x0007çç«½óÃã7{g'/~\x001c\x0014%¤X(¤*!ÕB!m	ië!­ØWißÖPE\x0019÷í@N%\x0002ê)'Cú\x0012ÒWCªpV@\x0007M+\x0014ZPÜDVMfäÝu³ÐSäº\x0001¥\&%³¡81á\x0007µ¬S­>\x0008ÉJ\x000e±¬¯`]*tÏ\)ß¯Gyq{óa\x001dþºûÎqCõtÀq¶åÎÎÉ/N_\x001e¿îº©BVY²ö{º.U¬ýzÀ±µ_
8\x0015ú»àùÇ8<\(\x000bz\x0017[\x0012oZa]	Û¯ª\x001b\x0005ë<R·Æ0²ÂSÙ£¢åFXÞ]]MËËy[7Vï+µµ¤¼\x0003\x0006f\x0016ZÑ¡íz\x001f[¬]`iah%§IëäL°\x001dcÀm
¹\x000cX,zÖvl\x0017_¶ñ*²\x0001¶_\x0017<rhYnD	C+ÒÐjEÈ­Þ*i;Ö·/ç4B@\x001dKIvá¬iû²\x0015­´¾CÛ¯\x0008^ÖD\x0010\x001d[û¨\x0019õÂ`;¦V´Z¸_å\x0008+UÌ{ûU±I÷ëkÔ´Òvl­X¶­\x0015\x001d[+Úl­5*WÆ=×î'{ MNåãýËVØ©\x0015Ë6µ¢ã'&G±ìM- %eIJ3´ùÖîÄ´\x001dS+ÚL­qº¿
h¬ý©Mn[(v¶{¯ íZ±lS[4,X_wa¤õ
°BåTkô\x0014ÌC+ûww­´\x001d[+Ûlíß6\x0011dÇ|É6óõýiE?| úáóË»»Ë½×^ÞíZxÏ\x000cº\x0011V\x001aOJ\x0005|{\x000fø½óÕÙÙjïõê_«³\x0011°ºÕ\x000b
¸\x0017	ÿv¿ÓîåÍå·«1Y\x00106Q¢\x0002Õ$Íå,Ó[P!óju¼z{¸;\x0011÷4ÚT4\x001auØ¼÷\x0018ª\x000cÝÚ~³\x0011U¨ý¶ÀãP¡Â\x0008Eí >39]S ³j­CU%ªjBeòï¸§Øv\x0018SM2¶×ªKÔ~\x000fãq¨8%g\x000cJ\x001fCâþ¶ãL\x001d¦)1û½àÇ`:ïx\x0016'u£¡\x001d<¡òyæ©+QûMÖÇ¡s,VC\x0019À1eäf¹`´f!õ%i¿Éú8ÒMúIÔ\x001dIßpQû!ù6ÔBg\x0001,j¿Íú8V\ÖÈÊ¨>/ì§Td¢ûµ\x0003¬]ëßbþq\x001cWmP\x0005ViKµÀ\x000e\x0012qç`íØÞ²\x0001\x0004VI[v$ú &ÝdÕÔmDíØÞ²\x0001@)	\x000cpÐ\x0019Ç\x001cì*û>¨\x001dkÅÌU8mQÏN(Mó.n³DìÄåû®7es7??ü¹3#\x0000N,ò}¤t¸ó\x001b®$Å0ÂÚêe\x0004 îý\x001f/þµ3\x001fÀ÷½\x0013ßé ³\x00088YÂÉJ8\x001b­C©m#\x001fÿéîn\x0015pªSK\x00199®ú;¤*º¿øyý×@û1ðà\x0018
ühêQ\x0002\x0017\x0013\x0014GT(H\x001dê<ø÷Îþh)w¹\x0008öC5ÂÆu×¾á¨ñn}ÿõêòfw$x\x001aLm\x00060EI<eF\x0001~ú\x0000®~ÏWÏ\x000fÎß\x001c®aM\x0007Ö4Âb£e«}H­õõ\x0002j9Ã\x0001¶Ð\x0002¶\x0007zU_^\x001bØElRUÁ\x0014WN>¦Wýðð\x0007êVu¾:z»óxÙ¬\x0005D±HDY"ÊE"ª\x0012Q-\x000c±ßZP°2Å\x000cãùúËÕÍP\x0015¤0å*5ÅíTý\=Jì\x0000\x0003y~pzx¼Ã@\x0012¤(!ÅB!M	i\x0016
éJH·0H&ûUÜÒwÛ]þp·¾ºÛÙÉ/¸ß\gÍ>Ð}\x0011¨¸Q]ëëUnzùýpvpx¶«\x001f!\x0012QT#já¼%gÖû,+¨\x001fåÖ#Ê\x0012QÖbn¸+\x001dõ.	£hI´Tn\x0011r¯AÔ%¢^ä¶%¢­F\x000cçVK\x0002"ÊAEåZêÈÔ.?5¾DôÕÁ%s(²\x0018v\x0019Â\x0000Áã¦dkõtã¸\x001aDÞ]ÑõKZIÊla$\x0011TÇm\x001eÆ§[Ô0v4_ä.[Õø²UÍ\x0018;×¯ê¿ã[\x000e£Yä8v,\x000f¯7=Ç8ò®jL\ÛðZT¾1ä6Ö§D\x0013äÈ«¾"D
ªwýÀ+ç c³w|{µó²\x000cú*JhEgEAìTäA5®N±Èø\x001cköO\x000ew^!¤(!ÅB!e	)\x0017
©JHµPH]BêB\x0012Ò,\x0014Òv¡®t\x000bô%¤¯d6'ÏsIÑR\x0016lx¾þxº·ê8HÑ7æÂQúëÏ»Óz®-©BÓHS÷rxëµ­úË×;;Ó¾	\x0017®Ñ@\x000bÛ %E³p¸F¹v\x0005W\x001fÝqW¢É\x0012MÖÛCÈxÕÇQË÷öéîr£Ñt¦\x0017fJ4S÷Aõ¾Æ\x0005Ëý>ª\x0010*G\x0017¬O7P\x001d
æJ0· 0_ù%}ÌâÞ\\x001dgÿ÷\x000f\x001aï´Jö½WçO\x001f»ëóc
\x001dÄ\x000c1Å)º»§ôãÇ=Æ±½ãª\x001bÀ~\x001e~rËÖ¿¤»÷*\x00187\x0011ÛPF±Mk\x0018\x001a­Kþ(\x0003âàõé^lW¸kÊp¢\x0013\x000b%\\x0018*áÔ2àÀ´õÜ\x000fæK÷ãÅúÃÃûËÝëÁyo¨±¶Ò\x000c»pÃ¸$ñ\x0012¶Í\x0003yqðòâÅjçeýð4ó¥\x00132\x0006Ðÿ¥}-ò¥r\x0000ôTWüHT´\x001eP²a\x0004\x001d\x0016>CÍ;&[L\x00064\l³wã\x0001U	¨\x001aFP Ê\x0006¤68\x001aAÊ¬\x0015ýµz@]\x0002êj@¹oHlÊSÄÅ8MKD=Ý·\x0006Ð¦\x0016P\x0018L¢2NDËó\x001aÛ\x0012BÆóÙÏVó)j®\Ú}# E×/ÿd`\x0004à»ðr½MÆ|ôç·w\x001f /äìáêþþrý°Û\x0008\x0006\x0017EØ|ÀË\x0011\x0007\x001dcpßí}àç'g/!3äìâðü|up±áësÉK.K\z9\¶ä²Ëáò%_\x000c\x0017ïÎûÿý\x0013?Ì,ðI¸Ù\x001c\x001e4ä\x0017õkÖ\x000fíöLÑ\x0011,\x0005êÒkrL´µý~TR£ï,¶à½ca\x0018»"ßúa/ûPGëÝ ÎÀ\x000e\x001b9áOÒba\x001b3tÍß\x000fÈ\x0013èÅ^ö¥\x000eFÑvn\x0010"qÙß´
:8{Ø*ÑrF6GZ÷Û5ÕS~¨é\x0014´<ì½¾}¸\x000ez~½¾y¿ÖjC´P)n¥6¹\x0017ë6%½×'\x0017GáOÏ\x000e_\x000c³U´±Â\x0011\x000eç­áy>l\x000eÚmÉÀ¯U%¬Z8¬)aÍBa\x0005ëz\x0013ðòÌrvû~\x001dvugTÕ$¥OåpH9°¦¯ßCîÎÙÉøÃaBQ\x0012zBCa\x0006)\x0005º´é
«ûuW
ªDTµstj¥Jy!±}nn×ïfÙ\x0000¨K@]\x000fèHAZ\x0005a9Aò,M\x001fCS"jD¡)H.F\Ã|î«ãô£U\x0005¢-\x0011m5b~x<ál ðQü!|¥é®DtÕ7NÙ]\x0002·Ê$YìÉ[*D_"úzDGil_\x0015NÎÔ&"ü«\x00117áàh\x0014Y5£V±h&æXø(`\x0011\x000f§\x0012\x0017x¿Åb\x0005#ëgè²^î¸
\x0001Á©Ê\x000bÄ¬ÒN0d¸aV>°9¢H@ôæ
ÖÛ[\x0000"ë_\x00182º0\x000c\x000cñS?¿[¾}¸¿\x001fÈ}õPwj°^RP3b\x001f,O.{¼ªÃ\x001fãç~~v\x0010vëóóÝé¯¬Èè\x0006±ÕS\x0015\x001e¼b©\Q½yÂ7Áª\x0012V-\x001cÖ°f©°±x@WUòÜ\x0018§$ðùÝÀQSKê­À\x001dJò´V,3n·æT½8yý|ç%<Å²çÏä\x0013pÆÄö?Q\x0014c4éÀÆ\x0007ôÕr»\x0018:Qv\x000eHZ\x001e1GÃæfÀ\x0010\x0015Wxv'O\x001dü¸Ý\x001a\x001f»ÇTÛ¤ÛÍ\x000fÅ¿?;½^¿¦ôôöîkØvRJÌÎ	\x0005Ç9S¤Gãû&êôèàE´£§'goÂ´=(Ù¯U{µjG`â¯a\x0018_^Þß?ì^=Æqì(cEjr Iý5\x000cgÏÔ\x0013Lü\x0011\x000cbX@ç\x0017ú=ýaCØM\x0005z\x000e
e¶¸9\x001a\x000e ù¡#mò=ª\x0008ç±'\x0010¡*Ã\x0006h®Dsuhf±T%¥Ù'\x001fµØ\x0018æâwÍJSÏÃ\x000f¢ÒÔéÝÿ³wº¾»¼ùm÷	ÖæòHÍ\x0018 )F%!ÜÈÞ±æôlµwzp¶:þ­Xð\x0019c`¾Ø\x000bí3ß­Ç~¾¾»¹úïÿ{7t[¤ü~<¹J	17Ê\x0011$&\x000e±ü-ë6\x0018ì³ãÃÕÙ:\x001atñxÑð:àÁ_ÅglÏØñ¹îø¹¥ë[Øø)Ö\x0019?øë²øtO/oÍe÷lu\x0010~\x0000Ç\x001f¯?ïÕd\x001ap·O\x0006,w\x0018\x0017Ôà?ÒOøñèõ^/Ù ÅgNtbit²¤K£S%Z\x0018]NMóÎ-\x000cOt\x0006O,môdgÕÊe,[õÓåï¿Z\x0011?o\x00181øuôÿý¯ÿûàæÃÝíCÔ¸s\x0008¤\x001d­\x0001÷\x000b\x001c>ÿqyó·ëëOë\x000fÿýÏçõ\x001d\x0010j¡=O(wÜ§f2\x001ct&¢Ís<\x0018=päáXñãÁ)\x001c/ÿ±:þÇÛ£W\x0007\x0017/W¯\x000fÎ\x001dí\x001d\x001c¿<;¹8\x000e®ßíçÏ\x0000¿?¢\x0005\x0016~M¡eI¢;\x0001\x0017opeÂµ,êMÂÕ·ú\x0006m6Xêpîx~ûp÷©T+ïbï-îÃæê¶DØVRÖ\x000b§¦Ø\x0017|\x0017èjïùÉÅÙ«aÌ`¯E;&¦ç\x0004NmXà¸qâÔ~h@GsH6sS	èFEN\x0011\x0003§°é®\x001d8ãyn\x0016Î°T;§LÇÎ4\x00169MêÞ
}ágûìú\x0019\»4bB8Y!¦U¹wÂñ³\x000f-ûÑá\x001f2ÍÅRæÈÉ÷\x0011SZZEé}\x0016ÌàqÛfL© K;.vb
Ú£\x0000¦
3ìànÊä¤Å®d¾lRL\x0007\x00053¼¯oÆ´*¯õ`;¹O«l;ç²I\x0010ë_­«\x0008¯ª\x0003¨Ôû¸ÖuþìÏeÀMàí{³é²5p
vÍ\x0000í\x0001\x001dt\x0012k~Â\x001bó	»ßÈÉÈÈK¼+t0Ugûðá\x001fâÍ»æ<v%P\x0016|Àã\x0004\x001a[kÎ\x0002J\x001e^\x001b¨0`4ë¾\x000c_[Ñ\x000cMmTgá\x000c¦7ïG\x001aT\x0017#¨ópín\x0008JÙ\x0006P6Ûö\x000e5ø¼yCÒ +¶¤¹\x0018@µ'?¹¹6N(\x001dàÍ[6>¯yfó§÷Î!(ç³­ù0×yó¦¤Ã\x0002RdíÍ¾	Tú\x001cå»\x001buÿ¡ëÏ¿;ã¯U
âwÆ¤G\x0004×³\x00069YÒæÛÍù\x0002.ß\x000cf¾\x0005T	¾³£µ\x000fg;ä´nØ4åÌ\x001e}\x001b§·Ü\x0001t\x0017\x000fù\x001a7%æÜ°±\x001f\x000b]ú6P\x001eH5\x0016@*Ð2/æ\x001bÒìÕ7r
\x0007\x0003©\x0014©Sh \x0015\x000e=<ÎÌ°u\x001aKýú&Ò03e:È[¡ð|\x001c,uD:bg\x001aK]û¦uï$\x001c,õ\x0013\x000c\x000bßi\x0002\x0015ó
ivî@¡väXÅ³òpJvþúùþ¼ÉÓ°Ûó¾hùúó»Ûx-[\x0011Ñ	ÿiÊ²ã\x000e:½ÇÄ&îÃP§)\x001bìÖÐøväw\x000f^½à|ß\x0003_x»ßÊ¤"\x000bü%øm8\x0010 ¿\x00182cãùõ/?_ëkÈ-Z|lR\x000b\x0002&$¬ïêærÎ¦á°³¹\x001e=\x0005®|>\x0016\x0006§{`ÞlÒ\x000fÂ\x0001I'\x0007g[ç|¯ßÿuUiÊOpb*Æß@;§dò l¥ a©¿ãF©\x0001CRÿ	äË\x000cCë\x0016É&\x0007[ü	\x0010©[H
¼6ö\x001cÜöòËÕõ/å§[Jrùí¿ÿi\x0019+dw.Ób\x0014ÖRÐX©±3\x0006ªMVoWÛ¢±\x001bz¸\x001cxÔªÞ\x0004o#JCÄ;u©
\x0003O\x000e\x00127~È1n\x000f6ìQë§¶¡g)÷<¸áüÁ5
½ ú¡\x001d¾\x001e.>d?éªiè±·\x001eÃ÷2I=ÂbÕÂ÷CÇ¼Ñô÷ïØ'}WÆx:ô§Y,¬\x0006ß¸øÞó|ù Ç\x001a ?E=±!~ð×]¿\x0011W\x001b¿óIÙ>ð3MÇ
Ç\x001a6pÖªx/°±z\x0005\x000ep¾kè!å\x0007Ro>TZMáDÊNâNBw\x0016\x0013_!¼\x0001~\x0003çÆ[ÍÓ³\x001e}üré,^!,*oæy\x0005ÉT<Á+8\x0013}Kx\x0005ÅÐ\x0000ù\x001dÞÇÀ\x0007ë%TÊ¢\x0004·éto\x0004¾\x000eºÅá;Ìù!>û_ý­8Ã\x0017¯pöpusYGÏ\x0004Ä\x0019ÓBPÁû=~¸±"·á?\x0018»C5çñj\x0004y:,O$ÐG#¹;
ÊT"\x000c#LÉ±»×hrME\x0017lß"¹Æ\x000b´(è¼*=g%Qè\x0019È\x0015yÈp_\x001a\x0003\x0000\x0001]ICè|¼¿\x0013ýþã\x000fYº;\x0001îåÿóíj]i'}çi´\x0014)BÍgcp}Z©\x0007fxøÿz¹z{x0H
\x001eüj%
6\\x0002ê!Áb\x0000ÊýÐ©u,¨
\x0016	~5\x000fij\x0007\x0017]¯thCJ&/8/C\x0011Õ±¤a~\x0006¿ÅrèÛ}úöÜs\x0008	Ì\x0004
á*=aHe, ¶Âðÿèð2îf!
3TO¥ZG\x0019Äxh\x0008^T:5È\x001fèît7©þËÿòù¾Øâ~¸}¸»MYu¨^Ðæf@îV¥eZO6üÎ\x0006\x0016þ\x000f'\x0017a/\ÆmúM=è?º\x0011õWW·ï.ïn.ÿ¬bõB¸û*Á¹Ô±ÁÌ>\ô&ÃªØpöÑjïÕáÉóÕÙñê_[pûxùñª¼£*[\x0011<`í]Õ1F¤0\x0019$OÇpÉgw9\x0014\x0010.{\x0015\Äê¼Ax¼\x000e\x000eÏcR?ÀsMf\x000c
\x0008\x0011>&\x001fÏ
\x000fñ6?\x001d^\x0013J»\x0005ç¢Û©\x001dY6a\x00076â\x0006v\x0010Pf\x001ev2!\x001c/ºÝ±ã~`ÿh\x000f\x0013Qº9f¤à2ó.¥Ä)Oq\x0007øÓ<ð_ÿøåç®y¹\x0015Iõ\x0003®R¿\x0001nUØ]dÚ\x0007µ"ÍFäÇz¥1¬tg×Æ
&%Ô¬2Ò0G2\x0018Y¨!¥[»ÖQ5©/Z²\x001fïH¨ÃI\x001aãYéâ®uTSm\x0015°*¡í0¬y\x0006ðáËåñ¬tu×8®\x001eþo\x000e"¡jL\x001cd~Ð¿¨ ¥«»ÆQå©(\x0019FÕ²Ô"\x0019\x000c\x0019ÞÂd\x001d¼
\x001fÏJw­¬,	þÃ\x000c0©-J`µ\x00190|)6îï\x001aY\x0005Ïãª³Õ^bl	3#+eè5²BÆ£Î+Ë\x000bºvQ4®Ã·÷£Y7Yzí\x0003ëp\x0012°\x0011PÖ8÷¸¶¢=5¬9S¯aÖ*ÎéH\x0014|\x0007¬nFÖ¬×>®É´²¶8v[\x000c¤P2:\x001bjÎ×kGMq3+ÑÐvÕ\x000e¾k`sÎ^;¬¶\x0008Ëã}O9®f8\x0017n<jNÛkE\x0015Q\.îZ2ï°pnO°Ã	Ú\x0003¬òþã»ß>\x0002+ÈàÁ¯³Û¯$ yÿ~ý¡z§U.ÎU\x0008À[¿ïú~¡\x001bÚ\x0012ÎN.ÞÄæùÃìÂú,>¦Âpf/\x0001\x0010ÉîJëy10\x001bØ!\x000c\x0019\x001fÓÙ-]^\x000e9Ö\x001cp/\x0007Îú
è
B×ð®<K*¬pïäñêO\x0000ÞÙØ\x0001÷¬\x001e\x001eÅÇäq,ö²W0µM\x000c]À¸\x001b,ò\x0012L±UZO\x001f|X8yÎ0ã­\x000e)`a j.í2\x0013\x0005\x0007\x000eG£é¿°??^ß\x0017ö\x0004\x001f;\x0010³*½Æ\x0007§(5æ\x000b/9zuaèµÈø#§Î^ñß\x000c¾\x0000Lz5Ï\x000bX½\x0016­Í8üaFI<\·Uü 
¿¦òk°\x0002\x0014ðÒ\x001akÒ\x000bèÍü\x0011#gÕ\x000bÀµ\x0005üá\x0005°\x000b=^?%÷5|F/ ùÈ\x0005Pó\x0002ûâ\x0019Þ \x001c½0l\x0007Ê\x001d>Ý·JJgÚ~)Äá\x0006%>fx\x0001Çè\x0006Pç iTÏÄ70C±»¦73T|L\x0003\x001eÎ\x0015xå­FÒ(ç\x000ce\x000e×^\x0000Â+ñ1Ç\x000bPU"\x000cìPX\x0010<ÛÑïñ	 ×J|Ìñ\x0006\x001e£QÁ\x0010	Ü¡Q"­c;p^jyxÝ\x0013\x001f3¼@8ô\x000bÀ¦v\x0017Üh¦,}¡\x001bÐ¦7\x0000ë\x0016\x001f3¼
.3nfpß\x000cæ¢¡«Ñ¦7Øx|Ìð\x0006ÁéÇb\x0004ÍEJ\x000fo \x000cÙR£¾-\x0015\x001a\x001f3¼\x0001i±ÁfàöeZ\x0006Pf+i¾Ç,\x0002\x0007=>fx\x0003ìÄ\x001asÖs\x0012vÖ\x001c
+·½\x0001È'X?Ç\x001bxÄX8ÎÐ,ò©fßa\x001dH4ÄÇ\x000co\x0010¯Ú|\x0003tÌ&\x0011JÚïà\x0014Éû-Ù,o\x0010V²¢(ÊÃ\x001bäsAj2û\x000bÀíÅ¥\x0010*gój÷ð	¨é!1¶7I$çDÊb -\x0018Ó|¶ö4dLù÷X\x0006`¡å\x001c³ð\x0006FPJ/dÕá\x000b\x0018Oöú{L"ÂI3Ï*°.cn]ÚMöÔ÷8Å+Êøé\x0005È\x00109L\x0006	/ óf0	Ûö\x0006\x0010^1ól\x0006Þ fI4D\x0002Ó\x001bÁ\x001d¥oð\x001d\
\x0005GK5ÏùRjtÐÓÙ@%ÇÔZïsb>KÄoÔ\x0015§>\x0002EëìkP5úzy}uyW\x00196\x0012e$2^ù\x0018=àV\x000e\x001e\x000cPPwïàÍêèpu6LîÕ§[
,B\x0013xÊ°0¨\x001e\x0014ÈÕPl«<Ý]Ï1æl\x001f+ñESÙ\x0015\x0007Zrºmn5y°\x0003c*¢¶¹F\x000ejÑAnT°9Ð%\x0012äI`\x0011È\x0005M\x00171DTOiÔÉ\x0011ÐÃ1Þeá±<_ø¬E§ª«éè.\x000fºÆäu¸ü¦é"ì0üáóï_~\x0015eªbîs\x0017KS/o>\Þ|­­÷Ñ*ÚT\x0015Ãm÷.Ô\x000c/V¦®_®ßl\x000bÿoÞ\x0000\oÅçy\x0003¥)þ/à^7Mz\x000e¢è8þC\x0015{¯\x0000&^Íô\x00118oÃ4OP ùYåW\x0018µlkßËçx0ó9n±LE_\x0001Þ@É\eð]Þ\x0000<L#çy\x0003a©ðG0»Å\x0007r,ÿ.ëêÞfx\x0001î\x001d]ÃÀ'H5W\x001e²\x0019è
Æ\x0019ÿÊWà\x0010È9ÞÁiJü\x000egCZ\x0008ñ\x0006¾Â(O­ö\x001dDt\x001dÄ<ï`y.\x0002e\x000cÃo¼	ó¡wøÀåÛO=ÇíÅuà¹¼^\x0003°©}~wy]ïwJ,ú\x0017²eÃ\x001eMiàz\x0007ôâhõzu\x000cM	ö\x000e^?_\x001d
¿AJïé
R\x0013\x001f,! Ô)Ã
\x0010\x000c.4½BéÈM\x0007hü_A³¨9\x0014óh\x0004}á{É¦w@\x0015ÙyÞ\x0001V\x0003ªGðÔ\7\x001e`²zÄàÑ·å\x0015R\x0010n¶WpU\x0003¬°ª[[%é\x001d"(-¯\x0000¡=5ç+\x0018,X3
ïöàHC¯`äí­þ\x001dÂôTv¶ÕàcQk|\x0007ZzQ¢S¼1ö{|\x0007Pº×³­èp´Ä,'\x000eÝxÊ±<¿ÃPVoÛ;MS«Ù¾£h
·\x0004yï0T"Ôö
áÛêùQ X\x0016irR¥ÍeN8²U¿\x0003¤\x001a1Ûg°1³2¾\x0003OMõbHþ\x000cßc5@¼m\x000egOæ²Ì
s'J_aH¡§é\x0015 \x0015ÆÎæ(AîÂ²ÕTÁ\x0015_ÁäRàïñ\x0006á\x001fµó­\x0005±/È]å©\x000bZ¬Ê%Âæ{8\x0019RèfÛ\x001aLU®IµS°ÑeÙ1ÁÆúw@áyÞA8TâNçO\ÏÐ8Þá{Ø$ÒÍauYjsZ\x000c¹¨Ú¸í\x0015\x0014¤QÎ8èôÆéÎµ3dH[Þ³X3\x0001\x0017\x001exæQU5ÅÞu\x0004|WtF6aåty/Ü§­AÑ\x001b	KV¿BV]ç\x0015T¬3U:\x0015ÄÓ\x001bÄä\x000eZÓ;àj¶\x0015
Íêp9@:\x0005~\x0007C5\x0005Vï°;p8QÅÇl§\x001f\x0014¤\x0013çÚ$Kz\x001dV\x000fi¡V¼ÄgóóÝý¢^µ¸^X}º¾º¯\x0015¤\x0013j#'`b
3À3Eû³\x00183âõÂêÕÑáù¶[×;U.Nå\x0012|ô°Ü
*:È\x0006ÁZËZì\Q0[ÒçÜRñÊ¯Á"Jl\x0008ÊJ1\x001d\x0018jÃ­H·MY%3ÆE\x001dÇC\x0011v3Ìo\x0001"æYRTéM7ÜÚ\x000ffwTrç*·ÜÁº£\x0000\x0014³T`´h\x0019u°úsßý~õÛ7[¨5Ü÷_þû»u0ìá¨Â(°¨¢û
¡)®8TXºA??]\x001d\x0004«8Lÿ(¯`
=VèqÃ7=ª²:Ì Êb\x0003>ÎÂï²ºÉ£o\x0018é\x0013BwÚÙùA0G¸Yø
WùØ\x001e\x000eNc\x0004#Ó>æÐ[\x000fç75\x0017~Nl\x0005ñ.<²\x001b\x0012¸4NÌ?ù²9­øREi8ú6ÝÇ\x001aO£oóO~èY9\x000f¾\x0012tTý×Q\x001dX»\x001cn\x0018o6GóÁÉ³Çm²
\x0004¹\x0007®d,Wó¯]H×÷~¦á'¹¯÷5þæzu´S6ÇÍ<kW)CúÆ6G\x0018\x000c³äÉñÎðÀ\x000b¼ÿíÓ/*6©òQ·qäc\x000bÊõÃçË½ÓË?ïn\x001fj\x001d\x0007\x000eú`©ÐY;ÔctÞQÆ\x001bÔ%ÇWM-\x000f.^¯öNWÿ:;¹ØêAä7\x0001\x0011ßgñ1Ó«\x0004³\x001cïà]ÎïÂI£V»­oz\x0015UÅ6ùU@z:­kÉ<njÎK\x000b\x001b\x000e1ßë]ÀÛÙÞeÓÄ\x0013ãÓð.BåU"ÇÙØúw\x0011u\x001f\x001fs­\x0016ÇóÙÝ	ºmbôY¬\x001bãm\x0015¸ª\x0011FÌ÷*VÅ\x000eµ1\x000caR)Ax\x0013F\x0019fHµýU`ó\x0016v¾\x000f-,\x001dîe8/cÀ3Ï9>&¢Òô.2Ê«±\x0019ß\x0005G%¾£\x000b\x0010¯÷\x001d\x001fs7Þø.P¨Âæ[-\x0010£CaZ\x0011N\x00191ÂiÝûÛ{ËH1³ó½	ôQ$?ËìK|\x0013i)ð(Ç%äµ¼\x000b¬y9ãÂ\x0017Ö¡N¢(E\x0012Ì9«M
l´¿\x000bèSùöI\x00018Á\x0004V\x0013yAÂîÁ\x001e\x000fI}µ¿
¤QÇÇL¯\x0002Rï\x0002ô
¢Ü$+´&¼\x000bÔØÙùJÉ\x001c\x0015Ú	Ëò»H³fP\x0004¥õ]\x0014¬\x00145ãr\x0001Í(Ê%ãJz\x0017IÍo¬\x001cRhk\x0015¨\x0003¹^ÅSö2µ6\x000bo¢r7õQW@m¯\x0002m2ãc¦WQ,WÃÉ\x0011sf¤ÙÔó|/R³Åf|\x0015O-Ñx8E
¯Û+Ii|\x0015PIqTEþh5m-Òdu7²ø¤å]à\x0002Í·µ¨ÍÍ\x000cð\x0018\x001a
V4À$ÿnï\x00027âñ1Ó»h¸òÂ}\x0012\x000eÉxùËrQú~ï\x0002
9âc®ï",\x0019±àöcÌEfYm;ØI²ýUà\x001e[«ù¶|¥4Õ±Bì\x0017k$\x0014ËúæÃ\x001a7Íï\x0002»V|Ìö.&ÉÅ´dI¹¤*ÇÂÌ÷ó*5ì+zÎÍÅIòö¹öñ¾\x001bÞEç\x001bï¶OBMÃ³øëU¼D-\°¾´\¡\x0004"c¿'fX¼fo£Ô<Ë7p)á\x0014ó6§+,Êly\x0017¸/ñh\x000cb>T\x0010¢<?+o­ôÈ{w\x0001måøë]@Ì^åª
cÖÒ\x001cScJ\x0012\x001aß\x0005ù|Þ¾f¹÷\x0013\x000c\x000bPË¡ò;¾Woéí=W(HK\x0015
Á¶QÍúnf\x000c®/\x0019Cûsj»\x000bªd¾\x000b­|ùÝ6JPM}ff\x000cíC\x0006£n2>ÊE_,¡f2í¯\x0002A}3cd_sGI'<xeNA¦¯2·
»ùãöòþÝc-Óÿþçëú®2\x0011A}¶¢^Ô:kJö1iJ;D®Þ\x001cmMÁÛ@Cr¢°S©¥¦VêÊ
TU0FduÍ±R\x0016c©Áâ)?{ÊëWÁ=ä(\x001eE¢3Ü\x000fòWRC½1©m,e\x0001jP@tH
«øÜÐ6lÊMf.Õ¡¥AÑCOI\x0001Þò©»ù\x0018mÔ ²WPã´ÖÎ\x000f~Tx
uð{g+µB=|§@¶\x0017%2-I%x7Ni`45ØS[ë\x000cqÔV$\x001aR{E²ýFQ¿¿d?ü¥(¥~s·þvywßË»¸}¨\x001có`?\x0014)T\x000bl¬\x0005¢¤Àej©ß\x001d¼]©\x0017'\x0017/AmIæz`»Q\x0016\x001bl\x0008\x001fÞBROÚÁ°_ã[ ,Ñ\oÁÉ\x0003.\x001a½Èò¤C3©í- û\x0001~Íõ\x00166\x000bÝ³LòÃ[xr\x0004ôÐMeã[\x00133ß·9\x0005\x0018ô\x0019±m­f·p3¾Q÷rýëëâ|}uóuïtýP]d£³èV¹²]³\Ý1_àüàðøÍÞéÁÅ6Ûô1Ò\x0017K?x\x000e\x0005\x0012Ø%ëùúþ\x001fGW\x000fÔð«à\x000cpâWp\x001bÒÿ:\x001bê¡l<èòüà|ïèpuñ
\x0007CQK=
,\x0017\x000ewwÉ=\x0013"·0czçE·¬D·l\x001a:Ëw\x000ea
¥V\x001d\x0006Äó^z£ÉE\L"wÞPÞ;´ZH¢ \x0001=S\x000fåEÕûÎD÷Ófºsù®Z\x000bÔ\x000cw¹··\x001bò0Ç;\x0006D\x001eVRê?{võqïÃC°4_ªL5V£\x000c$\x000f¤d}a³¸D\x001fÒ^<Zí\x001dþ°÷ò"ØÓ!rQiäF£ö¢\x0007ÕNä$ÚiìP¢r\x0015¸,ÁåDpý\ $´¸\x0000&ÑC§ì*rU«iäÚb\x0012f ×IÓ \x001bl|\x0018È\x0007ª×ë\O$×xßçU7\x0002'ö4ÍÕp{É
rS³ÅÆ\x0013k$gI¢9NóL>\x0014´¬"·%¹8æ\x0012\x0010½Ò©K\x001cs:\x00189¤Ô_EîJr7yÌS®74æV¨pÉÅOìÛ\x001fîËï¥^ä/?_ÝD³wW×Ý.Å"ö\x0019¿^_ýuu
\x0012JabR7\BäK>\x000b^®\x0017xØ°ÒJDÜÖÞ^^Ý\x000cº\x001f\x001d\x001cþûðèÙ\x001fW¯\x000f£ÙÁóÕáÑ¶~Ä%'õ¯æÔ&u~fÎq\x000f¥ïS+ätÏÉ\x0019[ã£\x001aÔÉd¡)ðV\x0004õÌ!¨y{éäo¦¬:*)ßÿ¼¾û°\x0013RKÆc©\x0002H\x000bÕÇ\x00112,+
cé_ÛÂ\x0019&ïÙËAÌM\x001b¡JNí9F8y,Æ\x0014Ó¢k\x00118×Ó9¿9c>ÿ\ÔsgÊ-±O|ufÃ\x001c,\x0007Dtüê\x0010áL_\x001dnÏÞÆË»\x000f7ï{\x0012u@!¶d%iÏ\x0006XJú\x000068\x001c§(·8E4õ\x0019`ÿøvµ¾ý³TR-¿ÿÃ»Ë»O\x0003«)üOL\x000c\x0006ó\x0014|K\x0011'ªOùôÁ8	\x001fWh0½·7Û>ýÅóÕÙ«­KiH*`Õ
;¸\x0006D\x001eµ-!Nài0­Pz6Fí^70ò¤\x0000 Xé\x0013£Ê\x0003ÉÁ\x0003\x0006ùåóÝÃïOMÌ½\x00177_/oÖÁàí¶JÎà=1Â;ÃUÂ »5\x000bZía}r­_ì½X\x001d¿Y\x001d\x001f\x001c=}ßU\x001a¸ºS
 \x0016.´}\x0002\x0005Ýd>=O*8\x00014\x0016bÌ\x0007JzV
#ê±¸¼\x00138¢\x00169%s@cad|Ôh<Ðp¨Í2*M\x001e\x001aMÏH
)ñQO\x001aÖxó\x0007R\x0003ÁÁHÊL&e|:©~ÿÕ__UéÅùð~÷¶©¤Ã,\x0005!Xì\x0003á¥\x0012£g¸>\}z\x0008»ÅV?äåÅmë}CHÛu\x0002Ë
\x0005¤M\x000b©çq LÍGøi\x001f&k>"d´t¨| \x0014ÎÏF¸%ªAòj:ÓdÂÑ\x001fÍ×*\x001dy1<\x0005\x00104Qâ£j\x000cÄ\x0016Y"\x0016äbÆ¯Ì\x0019®\x0015ïø\Q¤(>ª\x0000Çk/¡¥A÷\x0002NúÉ¿´"6?Å|~y×ôsúMD xä;|ÿ\ßÜþ	ï½s³\x0011ÔÝ\x0003®Ói³\x0008O\x001cDÁa³ÍÿÔÓÿ<8>ù×êl=TSÂ!7\x0019p%\x00188íÒ\x001aÜjb s6J\x001f\x0016³gõ\x000e.i9¥\x0005ðÂ¡\x0014Íòu\x0013)¿ýqåî¶~ñ»\x000fW7»5ëYê\x0014ÜsËÑzC«\x0000tÖÂ0Ê=\x0007Ò³ÇÃ \x0010æ\x0014²\x001eÔ¤ÿ\x0004çØ3êÓ\x001b@£®ätÐõíû
Î\x001e6ø(H_Ç\x0003ÏÐ©SßÐàIDÉm@,¥ìZ\x001dl%ú\x0017ù{ôu<ïlõ7¨\x0016z\x0017[Wj­ÁìbæÅÇ\x000b\x001cT´å§ÞÞýòð!6( 6Ñ\x001bWèt}½HÖN?(ø\x0018é®\x001d¤¥A×2úA:us±?|4¿Ø;=8:h× $*4TB\x001aJ\x0019¡Sò¾N^Ã½6¼32ö­ÒHÆ`RS^n¸ÁÈu ¡ÛTÈ¿üo_®Àtn:Á\x0016óò|ýéf÷¬´\x000czgÀR÷°~DZ?Ð%B*ëÐ\x001b¢ëé9y~ðêxë,\x0018A¾g9Ç0r\x0004\x0002$Óû)D¨Y
\x0016\x0003£x¥>ü~](èm>upa\x001eö®cÀxçò\x000e§N,}dPÙ%ãòvR¦\x000by«ÿZ
??ý¹ß\x001d\ì¥\x0010ñ +Iå7Àj¹¬¦\x000ck\êÄÊÑ\x0014	p·æ$Ý¨4 ­2I/@u÷¾ÅaÅ0\x000cÔÍ»Y`ç?ßÅ\x0000\x001c8×ª\x001b[ï½½Z__~ýºû\x000c)½\x0001o\x001dÜN\x0006ñw<[`3 à3)9æl\x0001öÞ\x001e\x001e\x001c­Þ¼ÙvÜÐ>\x0014§u\x0016÷N\x0001Mèé¡\x0015ZQkÆ\x001cÕFÀ~~÷ñãÏ7¥\x0017zøùËú>åðPpjgËúT^\x0008QX\x0006÷1Z(\x0004yNpq´Ý!9|}zp2u /ËËã- \x001f¿²¬tñ
Ðlôþöz÷ Â\x0015ÊS\x0010\x000c:\x0006¤Aµ\x001cb¡Èn\x001fÕôhoõâdK£ÅTo\x000f¿êI¹ÂÆ\x0012\x0002%Æà9ùÌy7\x0003©»\x000fóè!+Ð°HOÞÿ<8UxëÆcÂkbõ@§\x0010î¶\x0004g: 'aÚn§\x001bTjNÕjtÔV8ý:â¶oÑË7\{1'*%\x0014· *ºå\x00015Ê\x001c'W¡\x0001úYQÃÊ·ª
\x0015²0èÝ>:|Bbà[9'i\x0014&TÒ¸äÁrA\x0018"ÝÁyÜ\x0004xl^=#+5Àjae\x001eýhéÂá\x001eCfªÙ\x0016m\x0002Lãøh\x0002\x0015àæ§Aõ;\x001eÏ\x0013@ÙyYÁþËÇ\x001bÀ8V\x0015±\j \x0014¢åQf*è_¿Þüù\x00053\x001bc>ãó~ïtà¯mð¢5®&i²9\x0015Ì)Ã£y¾wºýh¿\x0001|¼?\x0002TØ>KÈ`Ç¨ \x0000cØ\Í\p·®\x0012Ð(f¹Lî\x0008ØM\x001a¾XU4îóÍõ­s¼&à¥Ñ|\x0008^î·Ë¯»c
\x0002ÜÌ9å¡ê":L\x000e¯]ÂÆ®]öÎÖ\x001f×_\x0004¼\x0008¾òÛÕ-êãíú?:ú¨Ô©úU'¥æ	^PA\x0005\x00039ÚtÑ\x0002\x0012\x0018xPR:åç\x0006'6xs.KºÜúÕÖÔ
\x0019]ª&	ú	,%¹\x0003©p2Y¨`zµ¾»\x000b\x001f¢{ZÃU4\x0018=d \x0019g\x001b\x000bÞ\x0003&ó8ZY¸tcÀ\x0004\\x001eÅÇø\x0011\x0003B<ôúxNC¦(ü&eÊ2¦ÀgÑh ¥v\x000c&¼ÇÓÓN#\x001a%·[\x000e5lÐ=ëY|fR`ú\x001b<Ê¾\x0001\x001bvf\x0008h6y³{/®o¿6c9¸\x001cs5Ó,ú«i\x0001\x0008è_\x0018©¬ £6-ÖïÃíK#VÜÏÒs,\x0017¸÷é¤Â@Õ\x0013nsÂ\x0015¦«À$\x001cçi7\x0008ÉÏ_î÷no>Ý·\x0012zH8KÏñ^ÅâdÈÃ\x0008GXF\x0008]ª¹Â<XN2\x001b¡m\x001e}Å\x000bÇ9rE\x0003aX´&\x00012î)vü\x0019\x0000elèU\x0016\x0001M5@È,]:PÂâ\x0004Â_~ýôû¯QY2 ,øh^ï\ Ü ¢iX âft\x0003\x000bDí^ G°v±îÎ¾ûtÿ5º°E\x0014x\x000f{¯o¿~ýs§KâµO\x0019Åë°´I\x0008n1ªg$T\x0016îÚ¾.ö^¼yó¯!ºxû\x001c\x001f\x0015tBzp\x0010SE¿ØCõHçÛZSG\x0017èâ£.ìü©¹#\x000f\x001e7t¼`RÛyèÀ!1¾rì oXøØ8Ò)!\x0005\x0016Ï@g!\x0011 >jèÂ¼Ãì.)$%\x0003xçÉW¼§®^ëØ7Eu#g°´,Þ\x000bÇüÐE#'ø<\x000et³ÅG
\¾ÄR.6µLXt?$6¹ºàÀÇ\x0000SòºÏº9\x0019Æ¡IJ\x001c:)éúJí©Äu\x001a®Ó³\x0002P£DS\x000c_;º¨\x000cË"­zW"O\x001d¡\x0001o =+	-Æ7i2<ÞÈÙ\x0008á"(=+	1ZÍ¡û¢!BÌîp\íVW\x0012ªH¨j	M:\x0005@\x0007Ji\x0018NÁ!tÏ÷cë²ø¬\x0001Ô\x001a¯y\x00054ù²\x0018ðAmðH¸ã\x001a¥0æÛÇg
¡aØnVòÆØ\x0019ö
¿I6ß\x0018¸PLåB¤í\x0017\x0008
úU60\x0013á|Ó0\x001a\x001bSkl­Ö8\x000f <VK\x0001\x0015ãÔ|\x001f\x0019Ò!Ò³\x00060lo\x000c\x0001uL,Úa0×\x0019L_ÐÆ¬F[¹Ýié±lZTÁ!\x000c?Æ¤A6§\x0006+ùt,ÒX\x001b\x0014`\x0017"8h\x00104[\x001a«ø\x0004\x0014^>KÏª/Lµ¡B\x0005/Ð¢)tZ\x000b
`ðt¼¾ª§ã\x001en~{_Fl£lÊCª[?äÅo¿=ì\x000c\x001b\x0016F2E^ 3n²ÙN
\x001cH\x001dNÃÛB\x0017\x00114ÖÎ\x001d\àíâÛÕÿ\l\x0017ØX2	;E?  æD\x0008´A\x001aãö³@Û¿¾ê¿~ù©×\x0018\x000eÿûÿ|
Ð\x0003÷¶\x001cÛ0A3
pâ<À\x001edÖh³sÃÉ¬o\x0002ë \x001fÝ×\x0000BÉur{ N²³bvc\x0002\x0004¢\x0000aR=*BÅð0\x001a\x001c³¸9FB'\x0005Ò]nY\x001d\x001f\x0005
§*ù :ÊâÕ¼¦ZðeUvËf\x0003ô)ÚU	\x0018N¤\x001c\x0007ÐÇã_\x0004dtuè8Û;PK\x0008Y¬^Ö\x0012Ê}FC¯á
ãÙ³Õb>B\x0008{]I(ÑJ\x0006À(j\x001a\x0001QG\x0007\x0000ýl1ò#³Þ÷èYHAàiP-M³\x0010ÓÄ Üp¶i(cÄ0÷\x001d½MþÈÁ\x0014züÈgÏVÍ¶¡Á3\x0015	GdgÐç1Ü\x0000]®÷\x0018ÀÛwZ~se}\x001eÊAbÕÀ=¡ÖádÏÐñ62ÿò26;ÊPÖ\x000c\x0002Ûï	\x000b:,\x0010¯ SÎ¢rJ ³¡dP¾\x001cþ0¸DÆó	Ìfp$_X ¸ULNëR½\x001cEHfÀãQ¬Ðî\x001dÅ'Hp,¬¤d\x0003\x0005(þ6\x0013`.$ª\x0001c:´8ª\x0016Ó>/\x000f#ÍlP\x0008\x0010\x001f5ÌäiXÉ¸>´\x0013´\x000cÚ!¾¿þüñ÷\x000f?õ»I\x0007ór{ssùuýn(O}Q0£òáÞP­\x0018¢-ÌÉññêÍÁóíé\x0012vM]O)éX0+òÙ/|Ê\x001c³§pWM©¼Jpq,
\x0005ÂÁOÐXÚ\x0011^M\x0005e©O9Ò9Z4,ØlLÛ5.Cê\x0011[ÊhÈM\x0002J%¥e\x0018·\x0004î$E\x0010l#%ÁÙ¨×5òõ·\x000f_8~²1ø\x0013\x0007>éöe:ðAñ|J^\x000c³µÔÉÝzä\x001bh\x0000^ò¡\x0003\x001d×¸ÒÄ\x0005<Zt¥§±VUC\x0006ÈL Î¤U= ÃF\x0016LY\x00072J\x0011Pq:4K1Û\x0010öDÇ\x0012ZQ'h\x0011Q\x001d'¤`ð³\x0011RP%aXÄÉËaP\x0007êq\x000c\x0019e÷Èùf!¼ª¯akæ\x0006\x0001-ä\x0001 ÷N\x0011 Ù\x001dÏ\x0019O\x0018Õ#\x0006d\x0013ÙæÏqÉ\x0003\x0001QÍ5Á A¾mýg\x000eþÅ(\x0014f°BÓl¬cq©Ú¢þöëo<Ë½\x001fÖwë\x000f;-!ÈÜè|á o*©Eq¯)ÃFÓíücy#¤ûáàìàâå\x0010\x001bWQö@ÕÀYº.\x0015G\x001fÌ3O
Q6\x0006¢·\x0016Tá	¸ü\x0011û\x0018<¨£H
V&ÃT{ìÁ<$®ÈÙø +>*øHâ<ð\x0019ÇÏäªcHò\x000b\x000f»«\x001b>¾O\x0002K\x001aÏ(.5ÞÒ\x001e?Û×,&ýTN
;F2,é
|\x0018u\x0001zWÑv\x001d\x001f8Áñ1/ø}©LàcTeêc_Ä\x0007â sñ
¾pFÆÜ=\x001d¶b*J\x001eó~Àº:~ûë/·~xä\x0005Þï½Z?|½\x001a\x000eUùIæÉÿ}ªå\x0014­pLIÉ?_Þ¬¯\x001fÃï½:¸xs¸C8øâ§\x0010\x001b/k$apøPyÎÃ)9ºy!QÊ/\x0016j'ãÿ¹)ä\x001c\x001fuÃ\x00082A:\x0006hq\x0018\x0005f@·óAÆ\x001bëø¨0¦I\x0010K\x0005
v\x0013$ÈÏÇ\x0008Ñ\x001aÉ«ç#©eI`\x000cÛ£í\x000e\x000bÂ@é_ûêýúõ×R\x0008\x0018¯/cRe*1¸Ý\x0019Ø4\x0010o\x0015xx\x000eO+ò¸¬M·¥±G\x001aþztrü*\x0015\x001blQO/a¡\x001dlÕ<ÃÆ»RLS7¦îR\x0018vVXªv«µ\x0006t^ó)q]Y\x0014÷Òi77,9Å)ü^C+\x0004%0
õ®éÚ4Þ&Z";sÒ
8I\x000b:N×ÐÊpN\x0017á¿ÒhìÙxð¤%0+-lÂ4Ì\x0004\x0001e\x001f\x0016êßRN\x0007lóTö¡æZb¿º_¯å¯ý-ôaïôöfwÔÉê Ñ\x0002¤ÞâáUr\x001aPÌþkóÓãmÁÑ
\x0016·\x0004«àr\x001c\x0015ª+ÉQr0p¡\x001f§v\x001f\x0008Grå\x001a£q\Áx^ÛÉ\x0017æ¸Öö@4b\x001c\x0016\x0007\x001dø\x0018Í\x0005\x001d"\x0004äÁ0T¯`1K9bSÁraíx0N²\x001aâd\x001cUQÉóYFlq?\x0016\x000b\x0018\x000b#\x0016\x0013\x001e"¥è¡b©(e*X÷À<rÄ\x0014íÌ\x0014GÓoÜ\x001cr#83\x001a,\x000c\x0013Ãb1«¤à\x0014oj(Åf\x0014\x0018>\x001coÄ@Ö*' FÈp9K\x0001.a·W$ÖÛÖ80\x000b\x0006ÿãwt<Ç´æ°¬\x00022½ª1­ÞÆö\x001bÀ%©¾Ý	Eu&a¦M\x0000S¿^?Ü~ob\x001aäÆ¶F¥¾]d6Øc		N=Õ¢³ºséþ\x0006ÿ©Ç\ç«³­Ê\x001b0opçÆ\x0019\x001f<då¸N´ÌjÎX½3¼6\x0012MÀu©¦\x0006-\x001c}ª\sa}¦d-¯\x0004Äd­h1yRÖ}NÅÓ¥!s\x0010\x0002ôø9!Õ\x0016kÖ´\x0019
\x001d¥sñ~¦âZ\x0010ø\x0011DÇ°üÀ+#²µNÁÞ«¯¡\x0003ùb\x0014¯f\x001e$ÌÓØQ5ëèÀ/Ss6sRB´a¡*Z¨ª\x0011£ªÉ<t±#§ª\x001a;¦Iø;
\x000f¥\x0013¸*\x0011ípÈj,\x001d\¥«â>}Ä
[§Ü
Î;fI\x001eÚbÏD\x0007Aÿø\x0018Ogl:\x000f@°®Ð½t\x0014"hGë°Ë<ü¹nçÊÄU\x0016Ø`5\x0013HZ\x001aô=\x0002¢o
ýL£\x0006R£ñ1N	\x0014¸\x000bßÔîã åù\x00067mó°AnÒ3-ªF\x000evRÔÞÒ\x000e¯Ö¼ät5dÌðýÁX:ÂhS±V!C-vìáyè¢4t
\x0012â¦Î·XUJ«FsñMß\x0008)À¤\x000b5¯
ä\»CÌ2U~TME8·Ïé¶BÞ&®­yà`Y\x0019«*à¬K-#\x001dð{®%©Ïêáû¾tÅ\x001eÂ\x0015[jWºo6\x0007.$ýÃÆÖÃW²\x0010ÕtÂC»×\x0014à¶>ÓMü²¿ýú\x0010ñYÄ»¾Í5øzïÍíÃî\x0006%à {:Ì+õq´Zá,¿ûä\x0010Å\x0006ß\lSCÝÀùõ¦\x0006.^Ðc(\x000b\x0012Á\x000c^Ð[Atz \x00042\x000eúÖ>\x001a<\x0010Äceûiè8)\Ã\x0019uw¸a<\x001dã£Î\x0005WDa"\x0010*\x000fp.iäØ}°\x001fÏ\x0006é5¼Ì±\x0019Ã\x0016ËlòW-v Ô\x0013l¦M»Ûßÿ¼»\x0019}p$Ï9ÎùÈ´ûJj£\x001cÂ%Þzæ$e7ð\x0011÷ßç{oW;$¡3\x001fIÖ\x0000\x001e\x0002\x0002
Z³\x001eé3¼Y\x0007i·z#\x0001
©C\x0019¤ë¢E&@æ\x0013\x001cÆ\x0003âë\x0000
êÁ¥\x0011Ä\x00019E¸ùøx,²V²\x000e0ø\x0006G\x0010äUqÇµ\x0006s0¬â{ÚxB¸	áFU\x0011\x0006§=Ý¤!ÄU"ê4cPÀ\x0001*>*\x0008cS`üÈÐf¡\x0014Bg\x0005 Ý!ñxp¥,Ê{å1\x0003è5E ,Ë:ßÂÓÁÌÆ\x0004¹¹\x0006\x0010¶6!+\x00070ø+ÌåI)haÐ\x0000Jê Ü4ü§ëõÃõçØó\x0004î¸âãàÛå
\x0010B\x0006ßçww\x000f BÌ?KEÐêìösT}ô*`è%HÏ<ZÆ0\x001d¯\x0016W³T9èÿ\x0008\x0012D\x0007oWÇ\x0000¶·zýüìâiÍá\x000e2\x001dMX \x0011\x0013<eÀr)¢\x0012°Â\x001fSIcð\x0012bÁ{\x001b\x00168+ðhÁÒ\x001a¤¦J§ôG Ò©j>\x000cV\x0014Úm£¢>-T6\x0019dÀr"¶!\x0007,¿a¬åkÃ"\x0013x´`y\x0011Ëu`j1Zrè¡\x0011KÇv®ã±þº¾¾þJÍR#ü9dñ?DòJA\x0007Q\x0008!Jçuz¡aB¤$âc-,È³\x0011\x0003\x000e)ûÃ8Pª]\x0003J4.f\x000c\x0002\x000ea¸­0â§wW÷0>ð[Ý\x0010ñØk&A¹<D:y0D`U[©¾^Þ\x0001\x0015üVGÅb)U¢W¦JÙüá®¢ºÿó·/\x001fØóè:öË½º¹¼[_íÆâ6Ìi\x0013± ø6öçÞgJ¦´NAõ]*µÑ=<^\x001d\x001c ëO«*:\x0019¾@Ç|TÛtér\x0012ðäã	V\x0007qf<\x0016;\x0013F<\x00155{\x0002H\x0011@\x0017ï.¦ÑÀ5Ò\x0019Îp\x0015Îq÷\x0001ºTÞ\x0005xbò·íöå¨\x001c<\x0017}³ÇðÃ&ç6°	í'²ñ(èÚ<v
mHÜ\x0000dx"e$\x0001{¼X+ñ çOX\x0017,M<h\x000b¥hây\x001a¾§\x000co%_\x00140o\x001d>ò³#_²Æqø\x0004­	0\x000fü2Ùüy}l	|\x0016ûÃø)2{1\x000e4¯ßI²nübÔ<\x001fC	|ÖÉü}§.Ý¨\x0016Ôï§R³<@\x0016øÂ!PÐòp\x001aùjùàpË[
³I,éûJt\x0001ÂøÉ<~§_¿\x0003|ÝðÅ<4|<Öø¤åAæ%\x001aÖi|1\x001d¢ÏúÍçõñ\x000eø§åÁ¦¿~·¾ºÏ«£\x0012KLÑBôéóâ	FZ/§N?Jml\x001c?\x001dÓoãøX&\x0010Ç/åHÀø	3\x000f\x0004bZ·\x000fhthqü¤\x0001làÓ\x0016Ís°ùÀ'mÞ>ìfùj\x0007\x0017&iüèëN6~Z0VÑ\x0019\x0015.k"+¡6£Ç&Ï¾~_Ð:>\x0003·\x000fzÉàèi³\x000fZòMåPRóæ¡SÞU\x001c¿$J\x0005|RÑê5Ó¿/d\5o\x001e8Ã§bR]Ä3ç&ïm @"7\x000f\x0015køãèÉ\x000bx((
£ç&\x001eÞ!6âÉhPâð¥T1à\x0013"\x000fß\x0013§ïJ¾(´ÞÊ'£¨@\x001a?\x001eÍ\x000cð±º\x000cãg'ây#^\x0012ª¦Ùä­Óà±©~=\x0008\x000eËæC(ô\x000ftÜÅ§@ÇQÝ\x0017\x0006\x000fr¢§ñõÚ'Öñ9\x001eÎ#3yq°©Zû4òÉì¸0\x0015ûüE>tKmÔ&íÜÚðXêè\x0017ð x`qø¬¥é§ÔT¿\x0000\x001a\x001aÈæµËRYmä1;\x001cø(ø\x0019øÄT¿\x0019º©Öå¡}j&\x000c|Nmø8ÙÉ§J¸CT­«CS\x001bF\7\x0011\x0002£\x0001Oµ.Ové\x001cÏ\x0007ÝÎ"^p\x0000­D<A«#^'NÃ¶õ­«CC0\x0019g_8ôæá#:6uíÆ¤ØÖµ\x0001sèD¼9\x0006:¥imðÉ>=\x0008Äêæµ\x0011ä&í»à\x0000ÒÖ¡8M¾]</ü\x0003ºyq8¹kC(Ú\x001cñ\x0004~^\x0003µñ\x0013ñP	°\x0011ÏÆs8ð\x0005\x0017ÁÓç%ÓlbI_\x0003ß¯q÷ÇO\x000cbC½\x001fn\x0003Û\x001bØ0ýÀ+õÁ±±Óâ>çacKÃçR¼®Ä\x000b`¯O÷~8	hÛnÊ6h½Óx\x0015\x0005A)(¦\x00006.bVÊ~ì(\x000etõ'±uÏjula}F©¦À\x0006º:¤@iìmÖNÖ=fÔ	\x0016û`\x0000Xzñæseðò\x0000\x001a:	h=/¯\x000eMä\x0007²-Í§\x000f\x001a6Al>hÏÃ«d\x000b\x0004&}PðV¸Ml¨L\x0012ØtÿÆª
\x0004YMó¸ÙhØâ7û\x0012
/
,èL@#ò&4-)Skè\x00143%ß\x0017.Ð\x001cÆOaëzulEg\x0004ØN'ÚÀ¦\x0015Ù\x000fn'±A±he\x000e\x0008¸\x0014\x000cKÚ0T<Û\x000fÎõ\x0014¶®»YÉ*×\x0012z0nÞd67Åº²|\x0013\x001bô¸¤ù¦,.\x0005oÑ³a3ôI»^pí'åÙã"KÓ
FÀ¸IhP\x0006Ój@ òi
®R):IElq3lgëzçÃæS¹0Í¶´ay\x0017©4l]×¼~²qÑ§Ùf­Ù]ÅÖsË+ÙÂì÷d@È9\x0012o[ÿXSÇÂ´Ml\x0010ß\x0004©s`\x000bÞ+ApfpÜvS6¬Þq¡rÜ¼@q)èX\x001a\x0003ãF7°\x0014ø\x00146\x0014þl\x001f·´LêciÜ0ÄiSãv¶î9¦
t?\x0014Z·¤n\x0001lBÐ|ÓfÊ\x0005g\ÝjÞÂ\x0004©»8nP²kÁ§\x0006\x000faÜX?ºYÇZëmlÐq\x000bç)!CÔ_Ñ|ä¼Qã¸\x0006\x0015Æ;ôÇÃ¸a\x001a \x00084»	lÜý´'ÓuãÑÔªX\x0005\x0003SN0ÜëÃv@+Õ)\x001ey {\x0017éÞ5Ò\x0019Ryà\x0004(Óm]ÀÓÙóUj!	xï#ÞûÖÁ³1}":J_:Ñ8z\x001f"ÞV<"Â`cçHçèH#üSj »t­A\x0011\x0016Õ\x0008âaP¡±ã±\x0007\x0016F\x001e&yçÁÂ\x0010¬qaØpL\x0011ÏÄ\x0018\x0010\x0018Q&\x0007F&\x0006m`e\x0004¼¶\x0011ñèlãyÊ®x´SØ)V%Ð½tm\x000b#Ð©tË\x000eëa\x0016} ã´n¥b\x0003Þ×¶0\x0002\x001eÅãÀ­ã\x0008'hâA3Ip\x0011®m]X¦6ç°1È©<vbâÄû\x0018ñ>6â°Ov×\x0011ÎHÃ$ÓØ>E¶O­l"Çp g\x0003.
Cå\x0008 91
ïç÷sëMÿ\x0011ÏÇ\x0016ñË\x000b\x0005\x0007µIq\x001c°xaCl´x1»\x0019$ácHBçSbì(=\x0005ï]Äk´x{¹\x001a&SæI\x000c4å£ÿ¤U\x001bèÞGºF\x0007-îLl²dðRôiu?í©îC¤k4x©; Å«½Gº¼É~ZLe.N<Ñ<ñl*D\x0004<á(,ì¹¥#\x0013S\x001c÷.âµN<è\x0007m\x0017µ
N(¢j"SèþÖÞo9#ÇÓ¾\x0015\x001eî\x001e\x000c#ÿ"3£(¶å(
%:¶¿	¢mÍÈ<í9ÚÛØ+î{Ø3ßÉ^É\x0007T\x0002õVV½\x0012+êé_w·ÉÊ\x0004HàN¹ñÚ,Øæá\x001eü<\x000c#ÞPÞÚM\x001bÏ©7^¶sv\x0007/Þ\x0013OÍCQJµ
Íû¢\x000fª7¡XG²Ñ\x000cÈC\x000eèhøþôSþ©¼þÏIÔ*GW\x001aáôæö§[êZýò«¦\x000bT\x00043Õá§àê\x001f\x000cC\x001dk\x0014ÄàSØ¾jÒè¦oÎ¿=¿zòô33hx0©Ä(ùL®S=ÏÄ"}\x0002)óÝ1¸ö\x0017ý|$Å\x0012´|)\x001eørMz\x0012\x001fg\x0016/l\x000bböðý;®üO?\x001f/Eø¶N\x001eÈÈINÑ±ñäÔ¦J¢4Ç\x0001¶eûÚ?}¶oò×n~\x000bïõ»èöýíÝÝÔËüÕòh<êeFJp	Y/PvÛ;I¢Ýç\x0017\x0017m`^`­\x001aÝvcÑ=±Jâfè j!VÜÖÃö`­ZÈvc¡Ù¨}¯FôL\x0005\x0011ÑÏ/Kf6QSmº³vcQ¡Á\x0014$á-ÂñÎÞG¾\x0016¼~UêãZ·ìå¢©y5	GºL×~âÊr\x001ftÛò\x000e¬M;Ân,RÔ¯X\x0019\x000cW3Ç`åí!À¶íôA®psþGÿw÷×?ýôöîöÝÍ\x0003.\x0017wÃB.Ë\Áù¹Ã\x0004Öi`´\x000fß]}ûíó§\x000fc­:wb\x0019Êê×"¥\x000bWëG>Mma#PU¦\x001bÊzþìê}\x0014ÿ®lxô
íÚvIî]ªà\x0016íS\x0004\x001b«déqIiÿèãÚ´GîåBcÅupjDsýn.Q&ç8Àµi;ÜË\x0005ëËR*Ü\x0012mÒZ8R¿ÕµéæÛý\x0019-éT®:túsÅ9\x001ciUêàÚ´Éíå²\x0016ªÀ\x0005!ÈEíèR¼­ÇëàÚ´íå2¶º\x001f®Ï¯î§Hê4YOMµmêÚGE1iç¤ÂTÖKË;RüÙÁµi÷ÙËåt3@öâ\x0014sàød+¶\x001d\F\$0R¸XÖ»Iá\x0006¹R\x0002.Ô#Ñé~¬mÅ^,yÏ\x0010iÊL¥r²»´Äw@ñn¨T¬ôrS¢»úÄ\x00081ÏTfdomû)ö.å
bZr\I\x001ay"¬«\x0003º¸Vål\x001dëE3¥Ðy\x001a]5q9Ã\x0011\x001d	mVåb\x001d\6a¼7×çê°)³\x0018·½;\x001d\Òú\$c\x0003µ¡ ÞÊ"Çï8bQÃ¤I¬¡ò¦>>ÑW>¬ÈoOÓ`­\x0011»U¦±rH×uTt@\G\x001f'UâÉF\x0014#ÀÚ!K_¦'ÅrÈsöÅzÕ Uý=\x0015\x0011V4¿Îý÷¢ÝLh7:{Ï¦\x000b&'s/ÅýñH;{\x0017Ø	ì\x0002j\x0013¬ c=	ÄqI#\x001bÍ{úÞk>g»q¦
É\x001a\x0018¦ù\x000b9Höz"S\x001cL¢S¼hè½#,ê'1\x000eyoOû\x000cÉ4û^Ôk¼CjµUØ\x0001]¹\x00112w¤Á¯ÇWN3j>gJIZ#\x0003Þ¸cõJ>ùl(ºH\x0013YÒ¹Z@\x000e\x0000¸)\x0012ÑøÁ»¾gvZÒì´DBælléA=°/÷b8b\x0019\µ	M±ÕRÈ¢Ñ1Íç0Ã\x0018AÛ\x0014æô%+&G ñ\x0003\x0010f\x0011¯S\x0005']u¥4t\x0008Ìä<5¾Ó[ê	æË\x001b~ÙjmÑÄ:ÉY("³?þþ_¯ï·bXÏÞúðáö_¾ÿôÛ\x0017¡l¤ji¹2\x0015	\x0015n{,ü<1Ç*,{öüêåK\x001a wõâ3L÷ûô©¾\x001fBd\x0013\¿x{ó//Þßýùßï¿Àw!x¾RfôµøÖÐx£ú\x0015£³Gò(/<¦1B.¿ [gÃöÙÌê9Ù#$Ç\x0019.E&³GÎd\x000fØZrm?\x0016ÇìÊ	,rJ\x000cO¤ÙÞv;È¶¹ºÝhSafk
$Iwc´Ç²O=d\x001b±«ýdÆVµ[û\x001a£u\x001c\x0000EkäyzÈ6:H»Él&	\x0010M³ÎK,\x0012\x0016)N\x001bAÛ¾¬íF3àXÿ-O\x0005A\x0015-Ëã\x000c:øuH'ÚF?e?\x001aò°93Ô÷P5\x0004ð\x0012\x0019ÍÆ¡C°ÍùìGóN^K\x000b\x0019-±0N Þ\x0008Ú6ï³\x0017Í\x0016o§N\x001fBó¹
\x0018\x001b´üNÐâ§\x001e´Me7\x001aÅ´5\x00132x¾\x0008«YÑR\x001e2\x001d«6®\x001e²\x0014%]0Ò\x0010\x0015Ä`9w\x001d0NÛf4:Ð"ÚÚ¨²·6¹<å\x000c\x0010
\x0016%
\x001a¼^Ñ5ôµ]5=`$\x000eÅ\¤ü%Ês|«\x000bdÞÈÚ¾.2­_.(,¯à\x001c§\x000f\x0002~Îm&¨\x0007­m
éA%sDk\x001d\x001eÚÌæthGÐ\x00007\x0019è6Z(åh\x0006\x0008\x001a®+\x000b>\x001eQ¥è!Ã]\x0006º\x0016\x0004ÛÉ{sêª¢\x0002Þyøt\x001eQ\x0000í\x0000KÓ Ý×\x0004\x0011×Äf¥h\x0006÷_7ÚPÈAO\x001aI·f±DÎÒ\x0000\x00141\x001bÎùxÂØªñôsÍñtÜÍh4\x00015
½BÑs\x0004Ê3³Îyr|¨\x001e
·Ú\x001a"?àùB@:üCÇ.ÒÙëÐrâçUê\x0012{Å{-Ù#ªß=\x0015®\x000f+ôýw\x0016\x001f&eh¿DGWØbØ±®_Ü\x0003øæÞ¿surù}Y$_~|ûóÝíõ§¿\x001fÁÚô'i+#5¥È5³/ÆxZ»÷\x001f|wq~võ¿öPÝ\x0010Õ*D.Åow*=í\x001cxg\x000cÂAÏôÞhB½\x0011#T´u\x0011\x0015\x0017¶e×õ»=T·Du«¡ª½D£ty\x0014ÉPåíÕ®ê'¢úI³«lÍ\x0015ñ~Ëið·u\x0019û\x0003Tÿþ¿\_'*ªYY\x001fßÞÝÜ>4\x0019Àûüt4-¤f¤¬åÈÂX»5ª?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun
Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T
T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001c0îÉQ¯U4G=7<Ä­\x0007Îù¥\x0016º¼¾º¼þxöæöæò@$$¡\x0006\x000cÝÞRøDçOz\x0000"\x0014ó­ÚO\x0018kÂØ¿Ad)\x0014IY³bRB\x0008i!\x0001ÙGjÂÔMhåý\x0012	tÜã\x0005Q\x0008Id}\x001báîe\x0008åek=¢s¥ÈLÂõä]e|³Kã\x0007ú\x0008uC¨»	½tß#¡ 2èRF;¼F¹Ö²\x001búÕr­y>ûáî·»¿\x001d6`ú_³4¦«CVn)Ð0¯?ËWÛ³\x001fÎßÿñ8¯Ù|\x001f6\[>±IÉW;aÒÅÂíÕl±f]l$C&JUh¤YÓÕ±§iÏ}u-ÛîX\x0010Ûî:½\x000e\x000e¯ÒJà@ª0¶Et^ï»\x0012NÏæÑ\x001f¦D(\x0007<äæ\x001eE;Tåò³\x000b`àçI ë×µ\x0017ï\x0012ìw»>\x0014éèÙ¼®	Ïöâ!Íïx\x000e¸ä\x0005­rL·Û¼µ|\x0018\x001fÎÆ±)Û.\x001fe!¾=\x001e\x0011º!\x0005\x001e7L!q¹v\x0010¤dC½HÑ
 %!>^ï\x0017)¶&´½Ó\§Üï\x0015yÎ°ò\x0008mÒ\d®\x001fÐÕ®\x001bÐ'\x0019¤8ÉçØÀÊQ¼¹Îû;û	}Mè»	§*LhåveB\x0010@¿y	C
\x0018º\x0001­®èädv¶P\x0000ÝÜþõ\x0002îJä	p2]\x0010-wË%ª\x0013În×H÷7~ó7ÖÍAÖÝ'\x0019H'?÷q&]u\x0006Ê"ºy>¬\x001fÑ4¦\x001f\x0008	£¼	9öæRi?_³\x000bu÷6ê$k^KÈ
\x0007Þ¼¨ÉéFÆ\x0018B·5Ä;f9ÊP\x001eñUéÖ5/º»\x0011¸`¶×º\x001bÑAßèõxÎV¾ô¿\x000e/"þ§nóø÷|÷ü.ÆÇ<1|#%-~\x0004Ò\x0018ùK\x0007[ê_z~{E×á\x0015p®s}ph\x0008-p¥¼\x0005n!©½\x0002Îéù\x001f½\x001bósÿøôëÔ\x0000Iù/kÊPsÒF\x0007Ç3´÷\cÃ¢PøÅõÍ\x000fS\x000f$å\x0016Þ\x001d\x0008»\x0004\x0014jP\x0018\x00025Ç\x0005\x001aü¼róIñ\x0010ªðÂfÔ\x000cZÑ.¡þkNÓ·tI-´ÓÖvÓiV2\x001aeÎ5=e1çbQ?©«IÝ\x0018©å\x001bÑjò-Y¦à\x0005¯Nòé}
êÇ>}b1LCí^¯Ì6ÀÒPË~ÒP±%
WÆ%U\x0012£\x0005Íz@6,Ö1öÆ4­©nKESä8i±PjI&ª4Õ¤ilM=\x000f\x0012Â¯¯«lê¥\x0017¸nÒj®Æ	uZS/fdG¥\x00023rã»fP\x0000µuPc\x001eÊÉ4\x0006C
ê<Ù#åû/Î;èFm\\x001eôQÓ`°	ÕÊ\x001e\x001fyrõ~©÷¼\x001fµñQzÌIÑ¸N>U¾Ú«ÁÉ\x0006¬jã¦ôBûÄµqJ'ñSGYoç×É1ÒÆMéA?å9}ehÐ-æßû%ÅÃ~ÔÆQé1Oe$H\x0012eµ8­
K­3ý¨§Òc®Ê
%úþÊJ<\x0005e\x0003´ñTzÌUáeÇõRúÍrå}t²UÕÒ«M?jãªô¯¢A(¿¿£ùûËtkêÌ?\x0001*4¾
Æ|\x0015ØW¼¨nwü\x0003k\x0000[¼Yâ\x0002í\x0015eÌþÓ\x000b}&ÍÓ"sÁ{Y\x001f6F~¦\x001dä¼Ðÿ\x001fï~þ×ç	ôþó$6\x001e÷üpg@+VÃÈØ6ê¥°ÿ\x001fÏßüóíDyquÐ×¾0Z+4:E\x001e\x0019 c\x0010\x001fÕRGZ\x001fa¬	c7a(ïvSóEþÒÑË\x0004_DÝJXEyHX\x001e?×#z\x0017{+Ý\x0017ÑF	â|J\x001f"4Ð\x0008¦Üðv¬<rËmÉ-­BÔ*ÎßSbI<ÜÜýüpdF³\x0002\x001bev\x001fþÏéö9%\x000fTZP\x001aç%ÛÍùËCc¤Õ\DHíDVQ\x0019+j*g7
¤\x001a\x0008ºù³g\x000fU¨©BÏZiÑÃ$#Ö\x0014¥àcQD~-U¬©b\x0007\x0015$Q¶WÔ\x001ex­DrÃ¥ö£µT©¦J=_Pó\x0013¢%\x0019¡B%EË>b%Uõ,R)\x0007­[¬2Ù:©¹Ì\x000cÄÉb`»`ÏÖRéJ÷PEnM¶S<-Û]\x0017ª%øµXiÐ=¶A{\x0019AjcüD¸ýè\x001cï¬øªÄoÖa)\x0019AE\x00159|¥\x0003'}%nqXëZ¬Ædé\x001e¥ì\x000e\x000bä¦QÔ	kª1YºÇfÑ8±ì{hD°Ø¬2\ú\x0001Ç±\x001a¥;ÆXÛ\x0008R\x0004ÎtIò	)ç9J\x0005Í9s¨á4vÙ"(UJ4\x0004¦JYkÚ7\x000cü\x0003½aþüûßïÏ.ýý?¿Ü]ýþ÷o¿ÿç_ªþ9~H£ÑÎü:\x0000\x0006x\x001c5aþ\z~uuqqvqûÃÅ»³«\x0017?­`55«\x0019e¥[fÖRcBAßgP]êFQñhä\x000f¨Jf[­94~þ5Ä\x001ajÖ0Èª\x0011o´A\x0017	\\N+ë:/»\x001abM5k\x001aeE"ÅÛ¤ÔX\x000e\x000code]7 ¦\x0018ÚG7üÃ\x001fJ¿ËÔÑtÿóïV'ÚP®\x0010Ôkøm5\x0005¹Z,ñä¦7?^\x001c¬PL~ö7Ì÷w_¿Ý??\x001d±JÞËË4}{¶àJü
J[z\ýðñâöæ8\x0016ÔXÐEUÃXZZ'µ<T\x0012×Âª­ær5ëâö\x001b[¨è"çÕ`Àj._sù\x001e.¼iñ@\x001b\x0015#Kj\x001dd»W¾c¨¹B×z\x0001·;#¡q:J\x0019§KK¯9«¹bÍ\x0015»ÖKË[\x0015¦|ãÄåw·­Kój¬Tc¥.,/C2\x000f¬p±\lâRî{-×.\x001b2Y	Õ\x0003f \x000eÎ\x001fj/b}h·µæ«Ë~(#\x0005\x0013ñi\x0004³r\x000fK×Õ`\x0001Ó]\x0016zËt¹£rl¬­à\x001duÃÜ½^M`¦\x000bLQ;IîÛ\x0000©\x0001ÑNñ?6°Ý[Õ\x0004f{À °¶ít}ÎÃ\x000cHñPö\x0018IU56_w\x0019}ãS©'Æ	ÌJS¨³K=«Á\x001a£¯»¬¾ Øª2ì\x0012ÁÊ­Ð.{®\x0006k¬¾î2û$\x0010²»®zæ\x000f	Kzm«±\x001a£¯»¬¾.=Uj\x0002°@&|½ì_ÃE3¿\x0018þð\x0007]w)þtÿD¡â±H¬$µ\x000cBd@ÆKÏ§5íz\x0014º¸¡@ñ8¢©\x0011M7"u¢I|Ýb\x0008+õ´Ê\x0018
/ú\x001eú\x0019mÍhû1'¦Þ\x000c*Kf»kc\x0014:¿\x0016\x000c0ºÑõ3j\x0011\x0018·&´ ãFO\x001döÕî\x0018÷hÙë¶+h\x0002ôý\x001f:9në´ô\x001cË5¤>Î\x001f¦'l]ÄX3Æ¡Eiµ.\x0017d2F²óþÃ~ÆJE^»¦D~íBâ%\x0007wãégwL91óÄÝÊ/­¢íÍ\x000fÿ@VGZbß>~ùöÏw\x000f_\x001f\x000e#âq¡Lâ\x0007$£z\x000b÷\x000bI;ìÛëw\x001fß__~¸<`µÓÔf;·'NÏú%4ò&È\x000bö<×8éjL7øè@Bs\x0019#sZ~Õ¤\x001bí	8}Íé>»a½æ\\x0011 ]0Óü=\x0019kÌ8\x0019¹ý\x0014Óò[Ägl\x0017ç±W\x001f'Ì:\x0015éß®æ¼ûöíî0¡5å¡= 
JQd\x000e)Á\x0013ö\x0010üx~mwk#6²A=pÖpJww2ÔÔìà`\x0013\³pºså¢<ÄNzm¬49h3ûöà*8hV\x000eúVÎi/ò\x001b!X~Â£\x0012EÒéEóøJ8;/°¹x¢j¢¼øËÃ»ç_\x001eÊh\x0005À­\x0011V¥ÀU`4{\x0017çõÞ\x0016¬\x000fg\x0017ï/ßß~w]\x0017ËÌ\x0018«¹ã\>1\x0002.\x001d¼\x001d¨I¡Üæ\x0005
ËÙ
Î	¡!!B¼cRä\x0010ò½\x0000(
«úÞfÀ\x0003\x0000³\x0001`øÚ£\x0010á?ß=ýöðùóQÉ
Ä2¦ômp\x00179"\x000f¿o3\x0012â\x001fÏoÞ^^]\x001dRÙ0
Z7MZõÌ·7÷Oh­ï}í`J	ÞyGF/ÕÛfX\x001bR^Ü ­¾¸Y\x0001ikHÛ\x000f©iD4m¨2\x0015IêÌüz:ÂèjF7°\x0018¹²üÅméÖ0/Ú?\x0007\x0018CÍ\x0018FÖÑæ\x00174V¦Kñc9QîüÖAjÊ4B)IU3]¼\x000cS¦Ò¢3ï|é¡ÚÎâpüVÁ¼z|~ oó\x0017Ãe\h²#IuSWüÔ\x001duÐ¢í\x0006]]ß^Ã¹D{t ÒL\x0010¡Fÿ¶F´ÿ­\x0010Uõ¶á\x001fê\x001cJÖÑ}ºÿvTA\x0010¸ÐËá¿¤9æ\x001c¿·/²cµþÁùÍÍÅÇCjIv\x0016Ðâ\x001fäeäüËû³ïî¾üü/\x0011iT\x001cç\x0015Ë£ (~Wu~Q6çüÝ»³ïoÎß½ù§CG:µ\x0005ÿë\x001fôN{ãÃãçû#ßÚÎ¹y\x0006÷ÒÊ\x0012_ÜWE|ãÃõÕÅåÕ\x001f~¾ûåîë·§ûò\x000fs:¨é \x000eÄÿ\x0001^Xy^'ÉÅKað<%ÛKgj:ÓGg4×VO5Á97\x0006Aqê\x001fá¶¡Ù\x001aÍv.\ò2?\x0008È¼\x000fÒK\x0017õ0±Î×t¾wáÊH(ªãár\x0013B©¦v>d=]¬éb'\x001dÄ]%µg=\x0010\x0008r¢áåÛ6]­\x001aµUxV2Û§8	\x0006Á+Í§Võâ5\x001bOwî<ã}	®)\x001bãà½\x0018\x0014e·í<Ýì<Ý»õ\x0002\x001a7i×'>´Aú¡¢^\x000e²Öã5[O÷î½`¤QJ:c`<~\x001cCsì÷\x00085\x001dÁÓ c[}N\x0012øâìOàßÑ0Z³ÆÃ\x0003Á:z@\x0015x¬6\x0014ö
'øi\x0012úûpÏÔ|¦/\x0016>'M\x0010÷P/jHjÏÕ|¶æ³½|1ÉX\x0002gx®\x0011.¬[z`ì¢s5ë¤ÓJÔ§\x0004<>Íj\x0011PñK½\x000f]x¾ÆóÝ\x001fWå;\x0003cÈBçÅsB·OÀu5]ªéRïây+tP\MÚµÛW¿Äf¨Öê£ëyh.¡\x0014\x001e]Ñ1}ócV\x0003ê\x0006P÷. :³(+¨¸(\x001b\x0006\x0001Ü×X>Ýkú´êb=\x0014Ir8Ê\x0007}ÃmV\x00036¦O÷Ú>ó'Ðv\x001ekeh\x001aé$n\x0004llî5~TÆ\x001f\x001f\x001cù6+Á²\x0001:'ºø\x001aë§{Í\x001fç!\x0018ú\x0016,KP_\x0014ÊèâkÌîµ¤{\x0012ó\x0005~ZÄë±;\x0018em\x0004\x000c
`è]@\x0004d>åen»K^\x000c´Þ7úp5_c¡u¯\x0006odäÒ²~x\x0015
¸WÏÿ\x0018\x001fM
hk|ð\x000f­<Ø×³7O_¿\x001eIMSâRj´Ut¯ø
G\x001aSÐ¨ytºËf¼¹¹þðá¢Iû?ýë§¿üú$©\x0016§®2ÊßòjiQü\x001f¾»ÿrÿLÉóøüû~ý7¾ûòí\x001eÿ%þÿnJñò}\x0012¯AvR<¡:\x0006\x0013r	\x0003~xn=|wqK©ñ¸ºøð\x000fo~<÷ñ\x0002ÿÕ\x001f®2Ý\x001f÷§þ\x001aP<¸n\x0018ÔÅ,Í &Q}Í\x0004ê 
(7\x0014´\x001f%¥t¯qÔ%zÉ!R«ó´4$
H=	)îÅ0¼¦èY¦òqÜÉº#BÌÊ¶HØ§#Å\x001f\x001d\x0007I1¼6¹Rnë®ODJÚôÔÉåó$¤hÒ(iÂ{(dPª\x0000ÖyImN»ÑÇ?á6¥XþsæeÒ`\x0003^AÔ$ãø@9ÇZ7'!EëFÿ9¸¦T²Ìgÿ!/ªÎÏó¸¨Ñ\x0010\x0015\x0001úÏ1T2¢j~Ð1\x000f¦U¬²N]«Ó\x001d)4ô¨¢§`*\x0014P¢V@Bu!ð\x0006À¸ãtg|¦\x001e5Tæ³
ÙfÑ\x0006P&×Õã^Õ\z\x0012T´RzØR\x0014IádZÕ\x0018Ù¦\x001a<ïU\x001fâ	W\x0015·½\x001e6UÔ\x00118õ¥\x0014\x0013PÎd\x0001qb\x0001ÜVGå>}ùß~æü\x0014e¥®îè5ÿÓÝ©\x000ft%)ÐÀÌ©ß.\x0000Ì´¨äS;hUÏéqÿ5½½¬!Å\x0003jGIñZ*zº¶\x0011hR)	h8\x0018Oõr2\x0004jh
¤Ï¤FQÖ\x001eI½â\x0002<$\x0015Q®²ï\x001f#¥ÖÀ\x000có\x001b\x0013¨ó¼KÑá\x001eÜ¥] Å£\x000eZÅ­\x0019ÿ8Ù~4øNÔÃAÛßG*njÔá=)G~ÓÙJùë\x0003	qeT\x0007\x0007
ê
Ôÿóÿëß1s¡ÿÝo\x001e~é\x0008Pc\x0008ùÅ¼)°ãw\x001f\x000f{ü§·¯¯o¾[ÃÍÓ\x0008#5ìe7êâT`\x0019\x0004'hgOÄ/z#\x001fÑÒ\x0013cF4Q\x000c}<\x0019b¾â ÒÄ×\x001c8\x0005z:dF%1K§BÌ7¦\x0001DÍNùºäãQ\x0010CëR:xYîaÌ7¡eä2[b¤ÌÂÄhxà+1Ú\x0013­£ôCGÆDz¾w\x001az\x0016\x0012äX[­6Aþòé¯ûk¬L\x000fÅGoï>ßýüç»çï0j:,d%\x000bì#O&GÈÎºpìÞñöüê\x001cÿrû?öÂ~ù·ûòë¿Î`@¬ow\x000f\x001d¬
Ïpî¡ /?¥´§+r	=l:lÒ\x0011:þ?_®båpn58q?èt,Ýí¦ÈÓYÉ:Ù£ñ|\x000f+\x0007tc¬oð¼®$]YcØÓxl\x0013ô°îrd#{DoòEÙé@ù²éÄgß\x001cÍæ\x001c\x0005ýÿõéÏ.Ô\x000eóñù¯\x000fS{ÏZF§S~¯ÂV·¥åô,\x0003´°>ýëÛ.÷¶$5ù«÷\x0003Ò`\x001b\x0017\x0011ãu«îÅàØ\x0013\x00198xê;\x0008sü>@\x0018ó$íÎ©hsZBóñ`Ð>\x001dôCë\x0001sØ>ðA½âOl\x000cõNçoKã\x0010PÅC;ñ\x0018àûõ_¾úÊb¾¾¿{þüpÿÜChYÁ%hÊØy\x0011£f\x000bT4É\x0011__ß^]^Ü®aÌ\x0007eQáFtå1¤ÀC"£Tb÷\x0013\x000eæ<"*ÑËÏù\x000fSeÆãó·I½åíãû¯ßº>ýô  4?(×\x0004#IúQÜÍõíÇIÔåíõ»\x000f\x001f\x000fí\x0002ïjx·\x0015ÞåÂ?~\x000c1òÆPð\x000f«\x0011z_Óû­ôT¶\x0018eéiùÏ3\x0008§Õ?d¸FøCÍ\x001f6ó;ÉGÑ\x0013OÆä\x000b¾9ä\x0019Fðc\x001f·á«¤T\x0016°Ê×lR,·óSü\x0015\x000eå)FðS¶â{]Xb£m\x0001BI²ëCæf\x000b_*|Ùò\x0003\x0002¿RS6ÓpìcÝ½gø\x0013^®\x0011~½õ\x0003Pý'¿\x001bâeXóþWJ6P8è5\x0017~ÀBKtE\x000f
=l¤÷¸ú1\x001fÞHs¸-?|¼·±'>½\µ"?Ànü\x0001\x000e/¥!Çù\x001a&þ`<Ü¤C¦îÅo\x000c¿Þhù\x0015®®Xþ\x0018\x00125KL!k­Czá'^üÆòë¦º¸ð\x000b\x001fu\x0007¾·hIþ\x001aÅéø\x001bÓ¯·Ú~«bÙý	äÙÏË·'\x001dÙÓþÆøë­Ö$\x0017#§ßh²ã· ¹å:×»ÿ÷ýO
$vÏxM#è¦¼ÇÙû§ßÿÎ²W\x000fTÓC\x0019ò\x0017 Y6çjª`¸
mßí÷ìý\x0008
^]~¼ÙØ.?\x0000ê\x001f\x0000\x001b\x0000(\x0013øå\x0018¨\x00018?qMÅ?\x001e\x000cGøMÍo6\x0000y\x000cìnT9+céFuðb?ò\x0003\ý\x0003Üæ\x000f ¼\x0004@)&jû~@´ò\x0003üA#4ò\x0003Bý\x0003Âæ\x001f@}ã|\x0004Ò¤¢2ý$µ\x0007!ÃÅ\ý? Õ? mÿ\x0001\x0013ìø1\x0014e²ò\x000fr\x0006?ñ\x0016Ò­\x0011ÚjôÅò\x0015\x0006"eé\x0014«hä\x0014»\x0013ï!Ý\x001c\x0002½ý\x0014p¹;þ\x0000¯ø\x0012ã¼Kü\x0003¢9R¼¶ú\x0007 ýt\x001f ?ÔÒ<È?ô¶àå©+Bù\x0001ÒlM\x00058üØN\x000fàìè+Cù\x0001Pÿ\x0000Øþ\x0003tyO¤ÖÙ^ÉË
.aCø¦Æ7ñ£¢\x0017y²Í9\x0014gµ)/¶ðÐ\x000fpõ\x000fpbEC\x0012HX%Vôp 4ô\x0003Bý\x0003ÂÖ\x001f@Ï£¡¥\x0012L\x001f,\x0019ú\x0005©þ\x0005iû'°RæI+(È#¦äá¢?\x0014\x000bü\x0002ÝZ¡­f\x0008XszD°×r8ø CH§;ÈAÍ\x000ciÔ­ß¾ûYT¸ßÞ=d
îµß\x0000<PmÎfM²*t%ó:ÈsbL\x000eòû«ó7â\x0007Þ_îWç®ø¡æ­üTÝ
??b4WÒqêÐ\x0007\x0018á75¿ÙÈÿ+\x0012Nûè¨
fZÿ°{È?XóºÀ¿'!\x0011ê\x0019¿\x000co7o\x001eûÀ)5EÕyó¸R\x0005}°ngdñ}Íï·òôS¡\x000eH~Â7Iz
üÁÔ.|ï}P­~þP¹$Ë¯S\x0015¢ã\x000e\x0004\x0017AøS:
-ÊúG¼
¿¯ùýF~³»\x0007ñ¤\x00157UQF¹\x0007à??Öüq+?îyëF¦aGK\x0016µ¬p\x0007SéýüU*\x001dTÕC:ø\x0003§\x000c \x001dÜnáÁ\x001b)cµ_\x0006~@s\x0000ôÖ\x0013\x0017­,V@? ¾rù\x000bèäå\x000b`L}\x001f÷°Øx_¼E)ãùxÿôÿíÝãÃÓ}Oc\x000eµ»8Ç¹]½^(©x8õáìãÅÍ
þ·w×7{õÌ*x¨áa#<º+w?]ã;Ä!\x001d \x0007èMMo¶Óç\x001c\x0004ÐMé¥0àxý~'}¨éÃFz¥åàB¥üO¢6§DXîdô©¦OÛèCâa\x0000\x0001\x000cL£j&z~¿vêxïT\x001f¼nÏìÆC\x001bHf2{]¬d¯\x0000ífÆ7\x001a\x000egp×âãgNL#¥o,ù¿\x001eî¿uQ¢6zÉw\x0016\x000c9«ãáúVîX®,ï¿¿¾¹øxü7@ý\x001b`ûoÀÐÓ\x000f¤½/¿ÖÇru4+KG~©9Ág\x0008¹ßgj&Ì_¡tä\x0006sè\x0008ý\x0004Wÿ\x0004·ù'`¨\x0005G¨\x0012eø>U¢ØRGsð-xì'ú'í_\x0001\x0003O©QöZjH¹«\x0000#þ0?}jÅ§í?#eíIü\x0019ÁJÛ4µ|òÏéÁ§ý\x0019wíÏ¸ûÿ×Ï°ó|ÍÓÂäu\x0007×ñ\x000bÀçQJ\x0008ÿ(û\x0002ßl\EbúÈ\x0003ëîOGùMÍo¶ò#¥¼Ð\x001b-5@(ünUuJ\x0007¿­ùíF~G£Â¦þ\x0017\x001b³\x001c.\x0006\x001dî\x001f\x001eaw5»Ûºöx[µ
\x001dií}´]WÚÔÁïk~¿ßS±-gÔ\x001dM§å§\x0005É¨SoýPãø\x0012êk#¦IØ´ü\x0011$\x0015êüÁTâ\x0008ªùÓV~\x0007J\x000cÞÓNø½\x0015üoJ\x0003øU6ÂÎ
ûFøS\x0016ÌÐôð£*DRZ\x0006öÄÇW·¦«í·>½\x0002¶ýÔiÏ\x001f \x001cß N||uc~ôVûcE0\x0018\x0013~\x0002#ç7\x001clj\x001eáoö¿Þz\x0000&£)m¤Í?X(]¤qUeîz~hö\x000flÝ?´êNÞTä$ \x0006WD%VÕwü&v­ÁC\x0004-1ô\x0003Ø\x0003û\x0000ú91s\x0000`ë\x0001 ³£\x001c\x0017\x0015xIiÑÈ\x0003±@\x0007U=\x0016~ÀÇ\x0018¦oÜ\x0017lõ_TËæ³49ãw\x0015\x0011\x0007ÛÒGV¿9¾°õøFï8±\x001fÂ¨I¥¸\x0012z\x001dØÁÕ7Íá5[\x000f/
ãÍèNÖÞJ?\x000c
À9ÕÒ§ù¥%\x0011Ç¿<½¿ÿöðíì}gI%ëúQI¥âK\x0017%z²Ãa\x001båÐoÏÞ_|¼üHEAÇÑ¡F-èx\x001cmÖE9h#èÞ\x0018É \x001fÖáèg75»Ù¶ìÑe÷A
²2»=Ø­ßÏîjv·mÝµ*5\x0018ês
hª\x0010\x000enôP£mèÊ4dNüO_ ³Ë\x0005=\x001cìú|¾ÇÄ¤y|Êèãá%e««IÑ)\x0017MîÖü°uì]sÝZM&\x0006\x000fgà¦õië$>§Z
ÿÃáJ~øf¯ëÝ)®ñ·#×øZ·¨\x000fß\x000b»áÝ®7nw/} £?Áû\x0002o\x000f6À®Ýïqå®L¸¿ÿùÏ÷g¯ï\x0010ño]ûÝðó¢NF\x001e×q¿x%m\x000fFó4«öâÍ\x0017g¯ÏñüÇ\x0003«îç¯,Þ5iÀ\x001f\x001eþzÿô\x001fw=yL\x0012bá\x0016Ç\x0014{ËI¥Ô¯\x000b$¸üéâæ\x001fJbúùÊû¼òèµÔ ×xe¹¶ÖXYz\x001aGsRzSÓô1ÊÛèT].ôJlMX×d´>Ôôa\x001b=þãó
Q³d\x0006Æb\íðßcÕ%|=}ªéÓFzÇ"¿ìFn.uTI%O»°*\x0010^M¯ÛS»ñØ\x0006¼vh~Ú%£Ïø\x000bz\x001cA\x001døZÍÂxüÃ®óÃÝÃog?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¿zùâðâìÍÛJQ\x0006EXÒ\x0008 Â:°S\x0004 ï³¹y\x0015;ü,¹<7Q±÷Àe!\x0002ã2³Ø\	Ôr©¼d=
ôÁRóéB¨R\x00085,tÔhna¢\x000fÉ\x0010"w®£K\x0008_
áG©C(~¤Jâ$½ÉNë¥q\x000c*¥é\x0017
Õð'yç.,þ~usÿáú§©2õ\x0008Xï\x0013p\x0014Ýgå\x001bÆO\x000f¯Î._~³
}á\x0002èÂ
a×
³;q\x001eÎ\x0018C\x0019A¡ª)ûnìËöHÀ®ô\x0010vñáÒ"\x0011\x001a£Ð\x0006ºúæÎnìÆ¬±\x001b3ÝÚü\x00040³ó´lW\x0008»Õ±Ö\x0005Ü\x0017
ãÇ\x0014Æf¾\x0005h<ÆôàHØlo\x001a&±¯\x001c\x001fÀÎs\x0013ÄÎ\x000bÜ\x0000>E^°)Ûgð+»À\x0012ü,¶XÎ)\x000cjª¯\x0012w\x0017äbÈFz\x0018d %Á*ôVdð0Ì:\x0013¼-ÁÛ1µñH\x0014\x0019\x0017þáðå\x0014äº\x001a°w,È.¾\x0002ð¾\x0004ï¿&ðªT\x001b5¤6P\x0003§{X2.¬¥>	Î7Gº°ëÒRê!KéY\x001ep\x0019$>È\x001bFeÕ%ë\x0006oË·c\x0007Ï%ÍËÃÁK4ó2¯ävê\x001båÊûêîë?
<316_¬Ã\x001fr1íÓû»\x001f{²k\x0010DGÞú;©(5¥dµ­3çu^¾¼ºª%u\x0012øÕp4e¹\x0017¼\x0012§Ö,0ìã\x0008½\x0015\x0012\x0019FV6åeÁû\x0012üàÉëTê\x000c¢Ö=#
'ìm\x0015æFìfÅ\x0015°²ÖÙ=¨¼HÙ4å\x001cuÕ\x0002ú\x0004©H3x»bÂ20W FÀ[\x001b ¦l\x0014t»ã\x0013Eõq\x001e^°¶%ê­àJD\x0004_V"ºO^\x0012G=0ìÑ}ÕNy\x0004ßÂ\x000eÜ} "vc\x000e^RÿõÐÔ\x00134diLuX³\x001búB\x001e¡[1\x0004\x001dFg¥Æ\x0012ñÄü«óMÜÆÍØ*Ý©±c×ÄT\x001fta9\x001c{Úû\x000eá_Ë\x0016¹\x0016ð©dh\x0016}0W¤ÞÝ¶çV0ø\x0008/«`ñ\x0002ê"'4¸¹%oüôåù6î¥<\x000e¸!	·\x001bw0+É!\x0008ªwTZ\x00057ËjÊÒ/i1\x0016)¯ä\x0000ìà\x000bøZâVcfR:iñ\x001a_kk\x0006®Òèå1
xR¾¥Ïïîo?´k¸d"·uB`mJy.¨¶£Û\x0018®¿¼<±	|\x001dì)
öv#\x000f\x000fi*ÎZ\x0019¼UðÄpI\x0005N­ÐW{*\x0001z±§²\x001bºp\x0016§Ø-ì©LTØÁªPMù¶F6è\x0017Ð\x001dß\x000f]yo8¦à­Ê~\x001e{)É"6½¢Ðu	]\x000fAçDÔ`¥\x0005§JzÔuçl\x000b\x0019v\x0003tF\x0001]_#u{sß±>D¢2qJÇe@\x0008t»\x0016Í"¯s0eä¯ÎÏ.«{è\x0013t±ì`\x0004èBù!ìÐy|Fci15¸,F\x001aMoh#x½\x00140\x0001¼\x0016z\x0004|@M\x0019`¦hÿ
ï\x0010ÚuÝD Þ\x0001Þàí\x0010xEci¿b\x0004¯5NÂiYMí\x0006oÊ7C'\x000fô\x001eÈ\x001a\x001e}àò:2SN>ÊÉ±\x0002\x000f¿¶É\x001d\x0010á#øè7:.8¾Máµm2ðí:¿æO%½_¯àÛ§úF.ªÚcùäó\x00172\,]\x0012F.Ê.Åw\x001d©
È\x000e8<|S\x001bÔÞ6­È¸:|óæÙ&ì[ ä\x001fÜ\x001eØsE\x000cÀ
%\x000foÑ\x0013kcßßB-\x0003¹4ü?<)6L¼¿>\üþw?ÿþ_÷=\x0014ÙÒHi)¤ä\x0008Þ±*Ý\x001e\x0015µ/N\x000f\x0017gÁ\x0019¾¬å\x0004Ú­%Ðn\\x0002¢«u2>
ÄçYgÞÄgß.ZÀ ²vT\x0002Á2\x000f\x0015ò\x0001R\x0006ÓD¿Uò\x001d@°µÑAE*Ö~~5ºt,HÐ§\x0019\x0004òJyR)>]§X\x0012dÞðÊ¯âY\x0010áéýõw?·
 |øÿ4Hª¤Å%!@WD$ÂkþC\x000ejA§§/Â\x001f¶$Xõ^\x0004±÷rH\x0004\x001d\x000eÞ¢2iô\x001c\x0012¶kR\x0007lí\x0015ë\x0013A¦\x0002É²7VBÄ¬¾ÂÃáâî/\x001dY\x0005\x00170"ÿVÜ_îñ\x0003\x0008Ô ¯k\x000còþÍáâåwµ¬B\x0002.\x0016*\x0017\x0000\x000e¿î\x0006\x000e\x000c\x0006Ø¨¥H±Am,q¹x9\x0011÷Bå\x0017qs>pà!\x001a§ïà:¤ÊR\x0011ã\x000foIã´\x0002_È¬"p!\x0006Ã63Imö	µ\x0015D
ÅkÛà{QÛò¸íÀqCs·UØ_Ï04\x000cjB´P²Ö^ß[.\x0017\x001b~ÝÚL!M/0%£¢ÏçíÌ¼óËðwÄ­ÔÀyÃè4ÒpA\x001e'áVÄ\x001c\x0011â\x0019çÍ#nµðùqè~ók'óÙÝýÇÛ\x000fÍ®±ö\x0002\x001b÷¬ôjK%\x0004Õ´ÅìÙËË«ó\x0017[¸Ýò\x0004\x0001n·nÿïÅm¤ù\x000b9hàÔ¸\x000b7´Å\x0003h\x0002ÎY	<þ¾\x001f¹fiÞÈø´\x000e4\x00027Øò\x000fF½Å\x0007k\x0005nýÀ
ôjûÜ\x001a¬{\x0018Ã8VlâØÅ<äî\x0008¹\x001b8rCüg\x0006zæq*ÐÂpEBÎÄo!×évÚJ\x000cn§]\x0013»\\x0005|ùÐNí"¤\x0011°[0æ³á\x001f)=©0ÅÇl' _å»\x00175r\x0004>øÐkððë\x0000ø8Z'±äDKÖXr²lÉh·ç«é\x0004ú$ÅÐÑCQÛbvUãd ÕÒ-ÙÕ\x0016\x001a£Vôèá÷!ô\x0012Ñb\x0017"ô¨óá\x001eéVôb5`\x0017;%Õ}ýèáÕ\x0014XÆq´\x0003OSÄÍ¶7c_ºP\x0012öu\x001bÊg¤7ÊqlC±ZxLlÇ`r\x001ezéJôÒ
¡\x000f0ÛÃ	Fä]Vs#u¦\x001aÖu£_ù2\x0011}éÌô½PÙ±ËÙsêCi¡i6Á´ÿùÇc[ÿãàeÉ^àÔ¤ 4¨=
#[&&}Ä}ÿúkÀ/í\x0011\x0013\x0019°d\x0000\x0013Ùù/¿^üH¥ç×·÷·=¤´&¯uv4¦\x0005û\x000bWËn?uzuEy¥ç§ççµFÀÛµ\x0004\x0010
I\x0010.'T\x0013\x0012sx;ñJúÌ¼W«~wIp<ey°â4\x0012h=yrq÷éð>¸hïï>îk]å@YÆ1\x0008´\x0002W+kg÷WÝµ¯\x000f\x0017ÁY»xyÕØÂE\x0011kQÄ\x0004QÙ"l<\x0007FôAÜÒ[s\x0006$kIä\x0014I,;á´\x001e¤v-ÇÞËÚpÚ$j-#æôM8<vQ\x0014®òæË\x001aGÈ(z-#¤ÒJ\x0008x\x0013»_ÓEÑµõ@\x0003µ$f$>SÝ\x0003ë=\x00118g7u­¬; ]bç/\x001c4\x000eÖÅH2_ôQàò?$n-û
%ÕaÅ\x0002'eý&þ÷üçÙ_Þß~ìy\x0014
­¥veÖbF\x001cÂÔØêÖâáì»ó«\x0006\x0001ÄZ\x0000ñ\x0015
 ×\x0002È¯P\x0000µ\x0016@}}\x0002¬h2ub8\x001aÀkªÖ\x0004Øä®iLZÖ±K\x0000e¾@øÃuÛòáÕû»O×÷?µûå!$UØ*\x001eÞ\x0006Ó\x0005Ht\x0001Q]m®c©4¾
&éôòMè«~T\x000bëG°Ã$?µ¹\x000bLd\x0008;ôó5Jé~èËjJnÍ\x0010t#(\x0014\x000c=Óä%ÏÐê
¼ØÕjh\x00124\x0006FFvçÜ)\x001c\x0014¶\ù\x0013Õ!\x0000ÒT\x001f¨
\x001eö_6°FðZ\x000c7\x000cim«Í1oj\x0018n\x0019q¦ÊjÔ]D\x001e\x000e½T§Ã\x001fèuuúæãáÛ»à5¼û¹½¿CoX"p¶\x0010õ é$\x00178\x000eäEäßjhÙÿöåà2?Ôúô\x00123ÍÂ
\x0004ûýÖL|Ww\x001f>ÁÿL\x0008­Ó\x0010¯Åf£@\x001eÌ\x0006PO³jJã½zùâ5üÏôçw×?]ütÿ¡¯²\x0012eÝ½W\x000ceq OhA­oAG1#æª>ÜN)|) \x00054\x0010
c\x0015\x000c7\x0001
G½ñM\x001b\x001cº¤\x0010\x000bA"H!Ö\x0004;¥0Q!\ã¸ÂY²¨¾ ¦O\x000c%\x000b1\x001c\x0017\x0003cø1¤ÍY&Ëò{\%ªÙ'ÆÂÎ\x001aÅX³³î\x0015C\x0008t¬p>ÁÉÌ:3_©$+J²	J%$ì\x0005å\x0006fO\x0004.æ\x001aÅð¶©ÈÖ))Å0ãbH\x0007]\x00143¬¶i¹\x000c3¶ðçwáda¨\x001c7TRÇ{\x001d§¾ÂÓü\x000eå\x001dO¤j!Uì\x0012\x000b_Üøû\x001cÊ\x0007ãJ,1y¤\x000fPùÝðF´\x0010é6Ë\x0001¸e\x001c\x001eØ\x001bX9£qÿû?Ú}\x0010\x001f¼m\x0006>åÖj¼\x0016Á\x0017´J8ÛÖôý
:ì¿\x0004ü\x001awç¬àà·!XûåæÃ*\x0007ópxöóïÿõÛýÍÃ¿Ý<Ü¾o×*ÎÂåÀ<\x0011¶;OËBuÍR\x00157àM½½<{óíÙóÊ7É¢µhb¾hBã~\x0012 ÌÆ}`&BÑT­·zP4¹\x0016MÎ\x0017S	Þi 7äÈGw\x001cêÖìl¿hj-/\x001a¹¨üÙp¥ÓRÓg«Ý®AÙôZ6=[6\x0006ëgÒ\x001aeC>G§¸È²µ:úe3kÙÌ£È\x001d9\x001a
ýXRTâd²ÆM2([ËææËfb«¡M¨È
æ©\x001aÂ´¨TÿÇdãå\x00030ý\x0005`ÐömQ8©'2Ê8\x0012ÎÖ¢ÑAá'O\x0003"-ÎÃ\x0019H9â*Ê\x001bk$\x001c{SÇO·úÃÓ}qýéo\x0007Þ1ãú\x0004s¬>/Ç6¹\x001c'ÙÆ3}~uuöü,xL\x0017§¯ÿ\x0014þs7±5v1\x001d\x0018ü±è\x000eàCò\x001c¥3øz±§\x001b¼\càU0Ù¸|ç\x0001?-\x000cõ=T\x0017Sî\x0001¯ÖàÕ\x0018øpÜ|\x0001ï,æiE\x0014µ>Ã>ðüXåùgU^tgäã@È \x0008<íh¦F~ü\x0007ðb\x001b¼XÿÎw\x000fjã5\x0017\x0014:káHçM­×m\x000fx¹\x0006ÿ9ï\x0001ïòÂ9\x0000Ï\x0011¼\x0015\x0005^­ÁNç;À[Fd½s4\x0013ª5í~ô5òfìþÏò·ÿ¤°¨sTÊ¹¼ûxóëÝ/¿ÜÞÜ\x0007Ä\x0002S¯>ãþø	°B¯µ¦éa	l(úIXÞã¨çÀôýÿQwvIvÝH~ßJm`*ïà\x0013]­æ_Q$\x0015yQ\x0014©r\x001e6Ù.\x001d3óämøÕOîuh'^@&îÁ¹¼u\x000f#tX\x001a]væ8øH$2ÿy}ùj\x0011¿~þòêÅó§O\x001f_]`/\x0019)¬ß¾\x001clgôRÒOñQkQÔ}À7¹ù3i#µq1í\x000fÚTÆä¯dF\x0007m¹¸\x000fc|¹cæÈ8KN~
Y\x0003§ *Iù¶n§O¶\x0007Ñ\x000e!:U,u®\Ìµë\x0002@s­aLk0º±O
rÍÀ43ÓSÆQúr\x00006úã@\x0005Ëùoßð@\x0002õ\x0010Êû!Iª ÿm\x00002-çò^\x00190ÝSÊ\x0006)â<ìHI\x0016ùo#ã\x0008ü\x0014\x0010s¿2Vf¤²û¬l \x0019µü·\x0011HMá2Ú
d¨âU;m?i\x001fKvlm§\x0019É9Æé &\x0017¤@j.,QÁì´¶)òÿ6\x0002éä6ÊÓu9Cj	_Sÿ¦} Ié=ÿm\x000c£ºà\x0002]ïËHÊ¡­Úvãôfý\x0000GwIÃ½ÅO\x001f¨ÉO\x0014©\x0005Ê)ß\x0007
îóß\x0006 5Hû	À¬çw  ué7ì\x0002IÏQ\x000fòß\x0006 )mºìÔ#/­<X^8Ô{\x001fHC¯F
BÆªêí¥s\x0005Òö¸Ïç6ôgÜØ¤WçòÆ\x0016\x001cÕ,¯]ÂE@û8»i\x001bÿé¦ìæ7Kec\x0010,õ1çíÜÈvnvrxmüémvËß\x000eúåÜ5üòÀ+¼¶âKw\\x000cëzS¶ô7Û%'a lZVU°û¬\x001f\x001aÎ7y80Óp²£\x0011\x0003µ	á[Ô]º½&g\x001aÍ·e4¾º~Ìy4ANHpu4÷ò5|^Dsl\x0011å¶`ÓQ¯\x0015æ­=¸®;é«ÿ¿úÏ_\x001d\x000fH\x0005ùìõn»ßÜ¼ÉCùÛÎMó?þíÝûçôå´üðýûÛÚÁàæ}ú/'ÄÛ{\x0019cð"REí\x0011ËîNZR\x001aýê?|òäª¶+xøäù³gOK:-)é\x001c§¿¾qÊtHÐ_ß6%ùÓô×·MIúÙô×·HùÉ¨ûÊ½-Ó-¼üýIIÀýËm<IçlÐ¢?\x0003\x0008|á	1p3K²®èüÚ\x001f®N'¸Ä>ül?¾kmÓ·¥¿l\x001d0§ÐÕ\x0000µ1ô4\x0007,:©\x00066ëb;N7wooÿv\x001aÛé¯\x001e ZÂ\x0006r2\x0010§Ñ$ \x0000a\x0002.¡\x0007ÈÆ´	s}UrY©¬$\x000399}®\x001bèæÓ\x00070Ï#¶6ú+\x0001½úxW%öN\x000f\x0010¥A¢dü[\x001a+â¡S£L"ôj=\x001e^¼z~]$ôNÍ!Å\x0005jO[þà\x0001}÷×ä®'ïÞßÜ;ÃmL÷x.¥5h)\x001fà\x0000e\x00150¬Ãð²þ^^<yüäá©\x0014ò\x0003 7Õd@mz\x0001!ké\x0016M?K{E\x0006\x0004ØÔK\x000c\x0000\x001a\\x0002\x001aì\x0005Ä(ÍVÍùÔ\x0019Ð¢ä&¶uÕ#º\x0001ÔÝØIÒ¡1Hu\x0003üEw>®½EÌ\x0014[ê\x0002¤q¾Â\x001bÑ\x0001èßjX_z\x0001}ó}ÿ'¶â\x001aïÉqÎ3Ì£Æu\x0004±\x001b°\x0019Aß?¶
_\x0006K
üÊ\x0008DÖf\x001206«8ö¯âúJEê->Ê*\x0011ÔjnnöÁ\x001cÏî\x001bBoè\x001as¸@±\x0017\x001fÔEm|\x0011Bß\x0012vd*\x0010`­Güü\x00137ò$´Í2¡½c¨E|Þêt\x0011F\x0019CYÈAÅIBÛ\x0012Úî1t¶ÊeZ\x0006ôâmê`æv\x001aê¬½\x0004ôýâ,¢9G·\x0012¡¸wÚãðGÖ!;\x000cÓD\x0007Æ¡.®þòþæÃçw\x001fÎ8Å$$âYy:ätðì_YQbÊÎ{XúÞ½¤"×Ï^=~v²ðì@É*òÐ§r+¥Íbz,¤K*iìÖ·{4k·tÒº%¥uýÇû"¥XY>YD

ÝÚW\x001d¡ô
¥ï§´WN\x001e>_9@\x001a\x001b¤ï\x001d§\x0019}3+}÷¬´ieHªöY\x001e¦¸aõ{·½#(³p~ö\x000f¥V»\x001a=¿ó\x001dÆ"oÓ®¥t\x0003.H¦FMy:²jûCpÓK\x001cm1m?fôÒÄ+ñZ\x001cGðNOcúv4}÷hRñe\x0010]u¨\x001b¦\x0011×\x0002\x0015Ì¦oGÓf¬ÙN6ë\x001aÑ\x0014'\x0012Áø	LÕerëÖré~¹ùËû¯÷¤'ÆY©FY*ä,\x0018Ù1OG®Ó½úÑ\x001fþðìt´H0\x0017~FÂ´v\x0000S×nÀSõZÉ\x001d\x0008;zw2v½Ó%§3\x0003É«d	\x000bÃ§±vÕ&úyÈÅÞ ½\x001e\x0019Ì QB\x001cKy.WÒí\x0002£\x001fLPÍ`ÒÏÉ©Äë0AÉCoT"$¯ïy×ß\x000eª]\x0003ªÝØ\x0006V2§>\x001c2¢N@­\x0007Eh¾<ýì\x0007\x0005Ñ[7|ñöT![­AF×ìHù&ß?QÞz©üY\x0006³ª{\x001a\x0007'_ý:@]\x000b:òÕÓôähÓÝÍ\x0004*
2Ì=	­ÛA\x0017'&z5\x0002ûlHÊ\x0002*ÍÌ=¯ÒA¥lAuÛ±õÓKSÇà$\x001f\x0002~<êdÒÖvJh¾;ý\x001c\x0018N/ÏÒ$º,É\x0008hxµ[uúr;(6ß]ãÐw\x000f²ºäÅKnä\x0013\x0008Ê<§nv¥Üô|d!fº]:>ÝÁJ³1\x0008;¶^\x001erC\x0012©R\x0011äÃó\x000ejÛ,­\x0017¢Ü\x0010\x000bÜF4ñ,Hf¡p\x001e\x000508CË\x0019F8­x"\x001eã¥â\x0003^Ë¹iÂ# ¾9èç·	jÚ3É\x000cI.J.vº\x0013]:®\x000e°rÈ;s:É£\x00034¶ ëVS\x001bÏ$¿¦ÿGa\x001bÎÙ6}${9\x000b*²QróP#¨\x000f¼Ò§¯Þ<V¸{R6c:Õ,%ú90C$êF\x001bê7Zzg»\x001dz×\x001eJnèP²õ}*úÜXAÓÏcRNí\x0002~öc*\x0011\x0017¡d\x001aÄg¢¾Pó ¦Ùë\x0019Øë]tJA©\x0010ók³­Vå`³uBÃ\x0013ê\àC>9<üÌ©%¤\x0018í:
6\x0000\x001aÛ\x0005\x001fG\x0016¼#·\x001e
h@©¥\x000b¬©\x0016£óó÷¤Ø.¤8²\x001cJÇGÊ\x001dÔ§«2ú0?C£n¶¦\x001c\x0019è\x0006MK©ôùÆY"ÞÞ[ùð÷Ô&nç\x000cÍJ¢Ýéð,2/\x0011\x0011ø½Í{¬}½î)¿ÙÊY{\x0006Õ°\x0008\x000c\x000c(u/!Ðé\x001fy¯w^Î\x0015âô\x0007Ê\x0015jHÃ;b¢¤kG4xWÛ\x0015(£¦w'\x0000ÕÒï~Òä8	)Uûà
.¾ÃüÁ\x0004 üÔ\x000fz\x001aÙóº·A*Âv\x0000Ð¶ 8p[2t[*ÓT§k\x000c©õ\x0002\x001aæ#Nlõñqèã[\x000e9EÊ\x0014|%_úÐn¥ùw?)õ,)¾ºô\x000fC\x001aç\x000fQX¾%eP7òñ¥\ÔÚÖoïDº,ÒIPÓºOùw7hº¸Rb\x0000ÏW²}|Zd¼ðY'
)·±Y\x000eêÍÀÜþ%Òã\x0017:\x001eV\x0016\x0017àvU¾vD^îTôgý"\x0019Ù¬¬Íª
\x001eùù£*}÷#`\x000b#ÀÚÇMËD¸tÅ\x000b0
­ÞáÄJÓáóÑtø<°È°N\x0007\x000cR chT\x000fôdØ7G°o¾¹¹«\x001d½æÀaKH\x001f
r·/\x0007Eú·\x001fßKÀ¶Ò`I§ë\x0014Ì\x0007¬ý\x0000\x0011¾ù@ªó?9\x000fØ\x0000R¾z? ¿\x0007à\x0013 \x0001Êm«ÖÏ·ÌwpË|­|\x0010¤ù³Ü§­$[y÷ëäÄ>@\¼3$@Ìò´]t³ç$m;´\x0004(uj Û	¨m\x0003¨m7 ¬5Jï"\x000ey^X	EuóQù~vñYj\x0018\x0015¸½·ñ´½Ô\x0006I"×a\x0012pb\x0000\x000f9V\x001b\x0001\x0003(I¸ñéÐ	eäNf%Z\x001b×Yî¡9\x0017ªo\x0004ýA)Ïf½í<õ3|=e+Y<rÑ£>¸n>-ÁYç$Cô\x001e\x00040~=y¥c\x0000\x0017î\x0010\x000fáM'còÛ¸Á9¬2U\x0007'ÞSË\x0018ß¬\x0019ß|3\x00131ÚH%í°Y§KKúµÌ}E\x0002_ÞI§ò¶f}QÅÙ
µ8'P.Ð\x0014ÙW¤^øúÉ}yJ\x0005ÓÄ%&\x0017
vbªYt¤
fM\x0000:
Î\x000c`úf4ýÀh
¢\x0019Ô¡\x001c~ÚËsAÎEÆ4
¦\x0019À\x0004{È$5©L\x0019|ÄÓÙù)C3ad0¡*fh#wÈiä¯£\\x0003\x0011\x0011\x0006ffÔü&¬IQÇÒ©J¹.jì§\x0004ðÍ2\x0007?23\x001diH\x0006·ç\x0019\x000e	½'	6c.2©\x0008.J#\x000b\x001fZ5íL¿¹ªjzj.kG2çÈp&×µÒº¡\x0007­Ì\x0019Eó
Í\x000e8\x000cq:;Ài-]\x0011J~'PÔ8¼¶¡Åém\x0013\ûÙÝÈg·i\x0017ÒõRLi¥\x0008B®YÛé¥N?û1éFÈÅ*w*±fÇÄ\x0016\x0013G0uM\x000eP1-ÖE´~\x000b\x001eál\x0017\x001fYDÎÊ\x0006O\x000b\x0015Ý&´à¦9Ch8©ëR7gr>dvF\x0011\x001c
ÆA­~9]±Øá|,\ââ~Ü\x000c¸I\x001bB\x0005M*wÝ$©ju´­\x000bTé\x000eíHË\x001f<ð\x0007¡O\x0017\x000fßÞ¼}wMÃèÅE¢Á,YÒÁÕÄ\x000f4úä`>|ôðÑã{«²
â¢;!"ô3r}ªòÞ\x0000më¬ã~ÀE\x00112µÐýZÜaîÒ\x0008£®ùðëì~FÛ0Ú~Æt.ò^©sãÜ\x0008}Gå$ýX\x0015%=©!D)æÖrÏM²°\x0012c{\x0018±,EZ¬~\x0000BG¿ÜÜý\x0016õ\x0019F%Ã¨\x0011'e\x001eÎZVêH\x001eýùáõSZÔ\x001b\x0018qÉ\x0003Ua\x001bcg%\x0005öTMN\x000f¤^Bê¡ä«Yt\x0014Þà­ñ(ÿdÑ,\x0019M7#ÄÈ©\x0012$dÁå8i ­\x000c¤^o#v	iû\x0007\x0012«&dÚ\x0014eLÞ@=Q(Ö\x0003én`$ìHTGR$@\x0001ÖÕÓ#~	éûGÒ¢LI/e#æ!ìµÄ\x0008bX"¡\x0019Éï!ñ0Rn\\x00135µ=q	\x0019ûÇ1-htJBúCæë Ö\x0000ä"ÖF\x001b¹\x001aØ\x0016CiX\x0001
¬\x000cå\x001eíqÓÞ¤\x000b¶ÈsÐX2eòÏÌcÙ\x001c80pâ +sæW0Q\x0016}<Q ÜCÙ8Ðäè",^\x000eoêèVÆ2H\x001c\x001d\x001cì@Ù9Ðè¤ëàa,\x001c:Vûª¼ÎÓ\x0019¡l\x000e\x001dè?u4\x0017\x0006i\x000cU?ÌÐ\x001c9Ðæhë9á)¹\x0018u\x001bòJb`Üß\x001eÊæÌþCG\x001bÇ	/A§óÇZ\x0019KqzÕ:1BÙ\x001c;Ðîh§/YfêÒ²6´°;8BÐ\x001c;ÐîÐPF\x001eÊä®Õ¡÷\x001dÜaá`sì`ÿ±C#i$Ø¯Y±=
e<ÔõÏC¶\x0017þý<Cò\x0002O·E%KGF\x0012Â)Y\x001eÊf§ÄþR{¼\x000c\x001c\x0008òZ\x0002V\x001eEñ\x0006×r2#Í.\x0003»P4\x0012VÌH\x0012\x001b@?¿\x000ba³¾q`}\x001b[w¡ü\x0004EÝ¥ê{Ä\x000c$¨Çþ\x0011Ö9öøøåíT\x000cÜ¢çì!ýcimo®®\x0008*®³¥?<ýèÞWÜÂ¹X= òêéåÔFóC³'ÏÈ²ÓfX6/\x0006þ\x000e¦á\'[nâD\x000e\x0014dNÍÝt;ÉàÏs.Þ¡\x0012çQAÿ\x0016ÎZF8C
RzvÕó¾ÔåÔÄyTºÓKiGSuè`/¨ÖWñ\x0011ÎÅËIâôëÂîMÏ oãA»\x0013Î{sÿ¶rês]¼e½+Åà\x001e½\x0016?ÓñÄÓ­\x0005:8ïîG¾;åù:Èë(Êzßg<cóÝãÀw7Q\x001d
'©x>Jr5­£p_6í6N~\x000elôNzJÐ\x001dñ=¿ìä#ÝW¿S·#\x0013\x0014äF7P\x000e\x0019y-\x0007\x0012\x001cåÞêffÁÐnP\x0003\x001c$ô¨Ï2¨\x000br"¹{S7ö7#G|ºý² 0D/qaª¤\x0016Ðu¼c\x0004Ô\x0006Ô®K?6Fnjö£ {}úsYK÷W¤n\x0004õÍ\x0019O?\x0007@\x001dG<Ø\x001a2¬ãëw\x0001Lê-Ö¸"CK>9 åOKQ\x0012=ÝÑo\x0017î-üØ\x0004
Ô¡¤Yóa]+ÿÒn¿Èw,ûýþ©>`¤	EãÝ\x0003gr¤i}E\x001aÛH[TÚJûY©DÉ°3jD:³Âº\x001c¢÷m\x001fÖÕ°Þ\x000c£cT®ð":MÇè\x000enµM\x0015MqIjh¶z¥ºz¥¥Ò£õJçOÓä¶À\x000fÍW
ÜÖÛS\x0018\x001d\x0014Ç\x001djid÷ðOt;\x0005hº\x000eÌ\x0001J/ä£ßººÿ\x0007->\x001f¬Cb£z³\x001aÕ~T-\x0012§éû«úôoCõN×y=}¤ÎýÔ>cRFÎa[ýrñâöó»Ï\x0017/Þß|¸D=Ð7Ýò8^\x001bd_¥\x000e|'©×\x0017/®^=~uñâÉÃggA­j@Õ\x0000)	¡qI¢|\x0002¤;½Ö\x0019¸Å\x001f!E×ÒÏ\x0001ÔtBi~åJ»ª×ZàêêT\x000fªö
ªöc¨µM¤\x000e\x0014n.¤ Ñ[<Uê×Cj\x0016Zê$\x0017´ì
ºÔ¦£ÊC%emÖhk\x001e'jÓÖêZT7F\x001eAt@	EET\x0015õB\x0017ªoQý\x0010*eÄrnMÚ±¸öáð\x000e²Ö´\x001e\x0003õ-¨\x001fÙ¨¨	\x000b' :Ç!¸ÐyjCíC-j\x001cA-â	òäÉ\x0017éàëò·ëèó\x0010jh?\x0018ùü¿Ó¨\x0006Ý¢ê!T'
y:*¹M \x000f\x0019½{ÚtèL¥`¾¢È§T^\x001fô©d\x001fj»ªÂØª\x0010\x0005%îKP²VÁ¤ÝÿûßE\x001a~,*¬²ÂÔN£x©ÁI~\x001dÚS1\x001eÔ¥ZZvTP©ï\x0014\x001c\x0018£¢ACÕòý»P¡uþ`hª:¸n\x0001T°3©®·Öì°ÿÛÅc\x0004._#:HsrjI÷\x0015©§ä¨Ö¦CîÒl\x0017ê"UPC\x0018A\x0005${©®æ\yïE\x0010ã\x001eËßÇæªÊ§Õò®Úá\x0004(ipF<I¼\x0000\x0011j?j¦3è¯.îUì±Þ\x000c¸¬ZÕìù`9Ó6*+½\x0004#¸Ó\x0012W´´m
Ð¦}Y
'(Þò^P_¢Í©èÿ6ØtÈÏ}õMðNÂë_>ç2ÝG·ÿñ¿þãîÝÍçû8-å\x0014qöÕôHB{)ðÐîØ¾F?ý*Wê>ºú½º~üðÕ9ÌE·\x001dÂÌÝvz9)I]òÕ\x0013\x0005o¢ÜîëÔ~Nï\x001aNÊ\x000eéæL;«\x0008·\x0017i¥Ìi$÷_ãºµ}?§vÍxæÃºd»EiA9ÎçðÞ-\x001aÆ¬³N\x00068]Ë90i{MªÒ1qÖj~8Í!0MÎ#ìÅtØ\x001cwaiÏ j+£#Õ~ÌÃOÆÌMc:1}Ú\x0004ÓÕÑ\x000cNÕ=t\x001dM\x001dà<\¥3']¥»95Èì$ªÒÉÏXã\x0013Z¯Óú9}ûÙýÀg÷à8UO§u¯x8«o\x0016Ñ4åÁÝÏäî÷&Ö`ôRF³\x001eFGÍ$ú9Ó\x000e·ä¤ÝAz+Õò\x001eéc,qTëâÍnNX¤oå=>g|v:4Q:aA¹Z[ÓÙa]\x00159\x0000ê|\x000bêú¿¼CºÜ8ÐO£à\x0000¥<¬Õýfèá5BæèþIµj%'êp¨wÒõKßÐÁùÓÛõÑù¶³·ÔÑjeyÑLL¬\x000béªP^£þ<\x0012=!Ô"\x001eâ©µ Î\x001fLz©&¨ý\x0013À¡â§³|)õeõ{«$/ò¨ÑÑØ\}»«ý\x0013à÷ØP	õfzóM¢ê¥Ä£L~TRu\x0016\x0017\x001f¤v?Mêëùõ\x0005¯\x0007UAî\x000f¸¨÷Lë"m~é&÷ö.vn?|>×\x0011R$j#\x0007ºVÃgA%aºÅ=º¢KÝ£«g¯îé._ñÌ\x0012Ï|;x¡¤\x0015\x001fbA=hÄXè}ôåÇ/woÏ(bz"©èE\x0016ÞÅù9/*ß¦÷ÑÏ__?:¹È.
%»´\x001b3±99á­(
§+\x0008FêÈ\x0001\x001dÀtzéô\x0008¦\x0008NêçÕ­%&¢Z¨ö`B.5\x0007\Ü;¨bMê0¾\üñæËß~y÷á×Ü\x001fb\x0008¾'ÇÃð\x0003O\x0017bÆ\x001dùò¯óüãÃ×/þüø>áK\x0006ô- ï\x0005¤"}¾\x00159ªcb-ÑC\x0013ufv' ¶#Ý#H\x000c2]¬=ë¬sÑêõ\x0003èf<RÞh\x000b'½Ê2\x000f¿\¼¸ûòáÝíÝ[P¨ï\x0000¤®A\x0012NÖG<\x000b__¼¸~ýìñÕõYÄEZfBÔ¶\x001bQ\x001dÂ2\x0011ë¶SÚ;ØhQ4ý£¨$±\x001a(²b^BB?}J°¨\x0003Ñ7¾\x0017ÑEuÉ=¥bé
T:zßê\x0007
`\x001c\x0019CÑçTÒ\x0006Æ°v#\?lu#.z'ÄekóÚH±¡Îd|ÏÅrBIi\x000bbÌ}2\x0017\x001a0\x0011²\x0006LÍbútñÃÝÍ,ªsû·¿iän4¢á\x0018¢ø\x0013û¸Wë»&3½¼øáúá³,®sõâÅ½\x0005KÌì\x001af7Ê\x001c(K´\x001aª\x0015ÙI¨MâÉÄÆnäE\x00066Õn©qä \x000b?#'.æÀ|*g°Ù4ÌfÙHêx\x0008è¤hQIÛ¹®ýÈ¶A¶\x0013Ã\§2?x+Ô^¦òÉ¾!ÝÀ¶\x0017v|^h|\x0010¼$é*ÑÙK.ê©zndß±\x001f\x001fãäj\x0019fÍ¥Êëºal»Ø\x001cã\x00129ÆadW¥)ÂAÀG\x0005ñô½:Y×Ë¼¬°ªéNóAzÝ\x0005Ã\x0001@dîÜé>ÆÝÐºÎôs\x0010:ÝF$=2x-ó\x0019´\\x0004Hët/hÛ´\x001d\x001eé±nÎ^\x001at\x0006pµ«`0{\x001d(àZh7\x000em\x0014§vS×6©¦n>YÃÙ
\x001d­\x0003ÂðÞ\x0011©`¦0»C×xeÙusGÑaf½\x0014¥N¸~Ù)ï.Y0/ Hrª®!«tµÝkvP/æ\x001c\x001cuë\x001cÒ9»}Ð¬8j$Ùx²ÍG7s{®á%\x000bµ­#M\x0014©­±Vò\x0015­?ÙO©Ù©f¿sjt¿sÔýGzOS¥Ô/jÕÉÖè\x0003ÐK	Í}3Ì}èJ¶<RÈ\x0011n¿×¤&î7kî7ÃÜZ\x0004\x001di¿J¥uUî?Ùº\x0003Û\x00159Eº ÊÊ$\x0007õÅ§_îÎ	9Ï\x001aä\x0002ÝÀâ¯ÈÙ\x0002$¡}RAùéëëó|\x0010\x001a>\x0008ZY©±6AU­\x0002ÅÊgÔÝä¤8ä&@ÊÞ]\x0000f®\x0011¤l R»dT\x0010@-ÏZi\x0007^"m\x00079³j©E\x000fÆÉJ\x000eØÆ\x0013BGÑÁÉ`¹R
º6}½çÈ`Yys÷ööo'õR1s\x0006\x001dð9ÜH>\x001d´Ì\x000bô¶y÷Ì\x0018ë¥\x0002}B0ÐXM9\x001a\x0018\x001aeÇò§{-öBr\x0012%vC\x001cVrñ kû	@\x0019§BuCc3
Og\x000crÁªVb£\x0004¯üQ>Á8³mfÇÚßéZJÚ.Ó½ë20Jf¸ÛìX
ÂÓ1ï¡Ó@qA*4(î/îð^È,}Bj|«^:Âj\x0003\x0003\x00055(´\x001fs;7&v\x000eBèÜIeÊÃ\;	;gvØî°Ô.4¸TÓ¼^wïÞ}:\x0017:\x000e^Iÿ³´ï ò!¼Bù°'BÇ®®\x001f¿¼?v\ £]BFÛ\x000fi²s¥`Ãp\x0004ÖÖ"¸£n²Ý \x001aHúÙM©¥¢8S²o®\x000eJaîÓA¹¨~$J
ýà%\x0000OIºÜú'?HöÎ©µííXê±Tò¹±ä¹ûX{°£_G\x001aº\x0008³+¶ÔÏÄ¬)®âÖöi\x0018C>\x0000¨\DÚ[\x0008ÜU\x001d5_¾o\x0015)±¡Ä\x0011J¼äÎÖÎÕö¶P{puBö\x0008¤k Ý\x0000¤ác)}Zär¬Dij\x0007æ\x0013ÝJ: \x0017\x0001Ç\x0004©U7¤ò\x0006\x0014IÊ3ÉL(ª®\x0004¹Î$\x001b¡Ô
¥î\x001fJe¹\Öq\x0019GEüµ×µ¢\x0003.,\x0011]è\x001fH'\x0011[J¾b\x0006C3\x0007rý\x00041@¹¨\x0012NÞ÷S\x0006)\x0011 ÌKÞË½ñÒ
VMOIX¼¨Ò\x0016´l«±\x0015\x0012ÄÑ ³ERûÃPj­Ñi¡\x0004Ó?É÷a\x0005Í	µ\x001cÈhY:æÔÅºk/;Bç%~3²[bÝ,¯\x001f:§âumé-'Ú~Ît«åú**ª&EÍ²\x0017iYèpªûXß¾Y
èoq@½o\x0007Ôû\x0001¥J\x001bS\x0017\x0012Jj¬;îq\x0004\x001dÒy@ß~[\x0003jÖ\x001eæ(ÓãO\x001f¿üåö\$MÑK\qÑûzi\x0013?\x0018Ì:\x001beqÿùÓó×?\Ý\x001fL+\x0019*åÁ\x0001Ì ¬Ni\x0017Áñ>ªª*ú¤8e\x0007f4KÌhú1\x0001ü©	¦ôê\x000cU»ûhû\x001cà\ºì\x0006V\x001a[AÓÉÎYáÊL±R\x0007\x0006ní!p.\x0019\x0013§õ\x0003"R\x0006Öro ±Hð÷¼½n¦-e\x001c ¤\x00175)R¤"Z®\x0007Òªv\x0015=UúÝ\x0001ªùìô³\x001fTk	å
+\x0006\x0015\x0011â\x0008÷Â6.Ò\x001cò®¤G@Um©k'2+b{Æ\x00164\x000eZSGÊ¤MUÒY·o\x001cá\d\x0014\x0011ç*¥h#§ªSÔ\x0000'À\x0006*\x0003\x0001]7³\x0019\x0001íy\x0014\x0007\x000e$Aú@QÌC,¤pâÑùþ5Ð·7?ß|¢z¯jÕ¨V##Jeè¡Ö¨:éò&k	<»\x0011Õº¢¹X§\x0017JüÔåjÿ\x000cê°ÖP~gØÌiZN3Ä\x0019$
\x001eõøYÔ9è>8¿jÛLQm\x0007¦¨öU=Ç\x0018¼\x0014eçªH\x0016öà\x000c®á\x000cn3MKÍáC]Å\x0008IëWs÷¤ãu¬ùn×«þvhÙók\x0018É\x0012KkÌ*Gà×í;Ç\x000e¦[ÏGÓÛÓ\x001e%?ÂPÒ4
RU:áÎWç°¾Y\x000fë¡a­M«rf\x001aW[wÓ\x001dÆ5±¾]³\x000ekT¼oHI÷©Z½¶.¦\x001f\x0001?¯gÀÏßè\x000ch¤~u`\x0006\x0018i´GºäÒáÊúºYíâð-îõLz36ªuPY;;
ª«:u'qæ§¶ÖÉ\x0019©uº½íQM¢a2UËÕb!\x001aS\x0015ÉÖO\x0002M2DSãSã\x0000'õ\x0015âÝ?¬Õ(=ÊÒw'bõ]ì|jgÇÆSZa\x001b%â¡µ¸_/ü\x0011Î¥\x0016y\x0010Õ\x0000'H#t\x0005µ\x0012)É=¤Já\x000e¯×Zöp\x0002úf~¢ï\x00075T¥Å\x00134ÖÎ(!\x0014¡\x0007m´]MÑví\x001eÑni×±\x0019º\x0014ôÊsôf`¢\x0008æÕ`^£rÍÓÊ~ý¹¦óÛ/6|þúo\x0006>Ú<uýü(ªnr/I~Ý\x0013ëÛ5ëÛo5æEÍZø½­IÞ(u\x000b1ËÀå­äñú°îµh-6¥·%¡6ÝÔ{ <ÛP¶\x0013'íE)\x0015
i-M\x0012Ú¸$´±\x0010$SQºÈâ1$ÅÜIÂØl¤Ò~BÙß#	sÃ3£¤c)i:Ï"º\x0006Ñu#b®Â,QªØL½y#±^Df­ät¾NFzå*Î²OºÒIED°jr\x0014a\x000f\x0011m?¢\x0015DÊ\x0007ä¾ÎFâ!áHú®\x001bqq\x0013"ú~DéÆ\x0015Ó7 \x0018\x000f#;\x001báH±1´¡Ñ"ëµDPºçq\x000cë"´^Æ¦~Dúomï¦\x0012·KJ*axûí,\x001aP«Fvé\x000f\x001bÙ½úx÷öÛûõeHM,§ÜkzÙä\x0000r\x0000élqúzF\x000f¯_§ß×W'Ø\x000b¥C·¤t¸î_¸	SÀñN*Ç-ÒÑÌâ½=8*é!u\x0011\x001bØ¸n^¹\x0011ÖI'\x001eKù³a¥\x0016$¹§B	=°>æûu\x0017®M° Ü%èü­´aÑ÷v´Ûº¨
!ÔÐ¼·£:Ã/¯Cdý]\x0003Ò7JµÌÐ\x0018khU\x0008Cë
ÒÎ\x0014K5¶Fâ´ÆJ\x0013­Ö7Ë!Ø\x0008~	\x001b²Çí@òA\x0015\x000f¾´\x0008ü¹\x0007«·
ëQ§Èm¬ÉãÞº¨«ä=\x000bkK.{ò]¶\x0003\x0016H;`\x0001\x000fÐj%ª¹w\x0004À¨l­Ðª/_=´ÐNü{¶*Þz(Õè9ZëEÈë¸Mù\x0018­-­\x001dÚ\x000e´+G\x0017¤õ%ÎI§«-úPÃ
õ¨áÝ6Ô´]\x0005n¼\x000c®¶CBÒ\x0004÷õë ]
ÉWâ£®gÛ }à.m #cré¥4hµ\x00033vä¢[

\x0016\x000fáfäÔ¥M¬Ì\x0008KùDeò¢æV\x001dÁ\x0002ì2#À\x001fqZn£c\;HÒ_$¹]ÒWô(}ôü]Êy\x0013øÍÐ\x0011,iØ^\x001fôK\x000c\x00189õ\x001e\x00139óÞ¬yG&\x0005$×{MR\x0001\x000eD\x001bðâÞh?Ç|ûuhßæÐ~\x0015yÜ\x001a6Ó\x001d@­ñ¸¨4í\x000còRN-\x001c¾.ô¸-Äg×¡}Cûß&ç2´oshÿälBû¶\x0004\x0005¾5Pëj«ÛËÄÕír}zswþÞÝÞ»yV¤)ô\x0018M¥\x000eEè3ªpxyñôáõõóg¤uvßõau\x0003«Ç`c­¶TÑ£¨­&§ê\x001c:Y]ÃêÆX\x000fÅÎ\x0014\x000f4RÎ*eê(ål\x001066°q\x00186\x001eä^¹Å\x000cF~)O³`]0<\x0006kY`\x0007göR\x000cJ°\x001c^ÅzÀÆÓ±¢\x001eÖbNb
vW\x0017ÉÇqÝª"ì®NGzXc3®qt\£H»pCdi\x001fiß\x001a´×XáÐÆX³\x000774c½<ó­wF"Ø ¨Ø}\x000fÚÐÒAÚ(éûÉOcµ\x001eÿtÑ`\x001fìB?`\x0011Ç`­â:Ì\x0004«åôÂ(©v°8h3­\x001f\x001cÚÚ"\x0015¢å,?º3¬[÷GîuyÁÂ{I°«êûä\x0010ÜOI
Ò\x001dß\x0016Ó?ò«7Òs^\x001dmZË\x0002öä
'\\x0008ÛRø\x000cz	â
(|èÚe\x000cä>î\x0003÷hFl!l<+þà]\x0016#çsyD'\x001a!°:db5³¾\x0019Dð½£h©`\x0003\x000b¢?dh~@¥.Îßy¶\x0010×iû[\x0010#Gu\x001aOîÔ\x0017uÔ\x0012\x0019¼Gîjëw^¦r/}Ó	©r\x0013Á2\x001b\x0003×\x0006\x0007â°Õ}
&[)ß®)ß~?¯)î¤4wHOVÍsRùÚìþ\x001eáÚÍ·kÊÛoq,ß¬)ß|CVÿÔj¨'\x0007Y/\x0014
>]<ùøåï·?\x0015\x0006\x0011R\x0000ë¹Ã¥Oç7×9EsB¢<1>yþúÇ«W¯î}P-¾áô#QR¨#O>F8<Vô\x001fá\4âMÁ÷s\x00064$99©_$«\x0018ij\x0018Ýé{çvÎØpÆ\x0011NRK)5·\x0010Qr¥má<*$èãt¥÷É"Þ¾Xã´½øø×¿õØ´2Ô| W_\x001enÆ"\x0002\x0015Né>¤%ôüéÓsþZ¦\¤M¤Û*kb\x0013&F+%B¬Ï\x0011 )Ù*¬N\x00070AÆ ùÃ£©¥·\x0008\x0002,¹CÉwU't|º(]CéF(=åß\x000b%¿BiQ~SÞôÒ7SÚÒP«}ØbLWgê
Ø­[C\x000f`:µÄtj\x0000\x0013åÑ<
fî¤1k«\x0016å×²cýË»dÂ\ß%·qÚ\\x0003^ÓI@ÁEQsWî\x0006@\x000f§k9G>{âäFqùvn³^x×²µ\x0003®\x001dO72¦µ`jçz\x0017k·££ÆQ#íxºñt¡\x0006\x0010Òíïi^ÅÚw\x0011Në[9)óf¹Á«\x001d>\x000bqtNK7Xâ¯!ÚÓÍÐ|wïN\x0012\x0015u<Q\x0012z¼söÓß\x001dÑ4hF8
jðC³b§ºqupêfûD=°RßBîí\x0002T\x0012,r\x0018éSêX\x001d\x000b\x001fÂ4~`\x0019Eà×ï\x0019¹U×¨¡^ßÛ\x00068\x0017u¶ÄiaS\x0011\æ\x000cN\x001c%¯£\x001cGv-\x00020À\x0019Ûe\x0014G\x0011j	\x0019£\x0012áò\x0001eûô§¯EÛ9]Ë9°}\x001aeD8-ÃKàíÓ:
'ªX:8µj\x001dO5r\x001cQû+]9ùºAâTÕÞ>56Ë]ã»ä­¼Ä!J·\x0013OÙ¥2Ó\x001e²n½\x0010=æ\x0004i¬ÚK`NÖz\x000cóßÜ5[|Þ=¾Å±t«ÛÆÈXþ\x000e¾~dfBV\x000b-Ë}ÃÔ+æÌAdãO­,§\x000f Ñ
}úë?Þÿúþó\\x0012gAc#G\x0002z)øÕêDÀë§WO®þõ¾L\x001bFt
¢\x001b@\x000cµÖV\x0013½@xâym3¡n\x0006Q\x000f\x000c¢E9#Ó5Í®U\zBþp3¢Á%¢Á~D\x0013D"ÇàA\x0014KÆ2¸¢WÂ\x0013º÷\x0019\x000f\x0016J.ôêæ\x0003\x0015ø*\x0018kÀhÜÒÒY{JVyÛ\x0010RÓÏQ÷3\x0002Ty\x000c¯¤[\x0007iC¤a-âÒÍ\x0018[Æ8ÀèëzvQ¢:ºÊxªìx#âj9\x000f¬çtçkBTR\x0015 $.|O\x0019ïFD×ÎF÷mÍÆóå\x0016\x0017Üt\x000c,Ta?]¼ürw{óåßï\x000f®HÇ9\x0007¥6B\x0005.\x001d0'Ï¿¯¯¯\x001e¾þ¯gñ|ç»ù\x001c©ópû´j\x000c÷DF¹|\x001b{ª'òfÆEKdb¶\x0001Ì&HgåF®\x000fÄ!SÒ£	ë\x001a¥\x0001HÓBþ´"?îl¨\x001diµH¹Ó\x0019\x0010\x0019CË8ðµsFí\x001bFíû\x0019ë\x0019m±êSð·\x001dJûw;¤ig¤éiÙp¬`Ë@¢\x0019\x0019Oév@B\x000b	ýZ\x000bXªEÃõHÚuJù\x0000¤m!í\x0008d^ÓÚ¤® Í	\x000eÈEÐ \x001dvCRþ nªØ(\x001b\x000f"adüé4·¨\x001aHTý\x000e$Ø?oumÛuG¯~FhÖ
ýìfDñzóÚê\x001b\x000b³Gb¢Z\x0008(ýQ/«&Âê¹\x001aX­°ª\x0001Åò{ð#Ó§[W@=úøåï\x001fïw/¢\x0016q½üË\x001d%H­Àé~¬Y8ùùë\x001f\x0006\x0012ú);Q_L¬\x0015A\x0018%3SÝ_Ú²
ÒÚ%¤]W@nNôu ]\x001a8§$G|8~z²
èvJçn]K¸R\x0007Éº¦¡äh´BôûåÒa£\x000fj`0\x0004O[©ËíF"ûæd\x0017·-&äâ\x0008§«qsuxró÷ïîoÃbJZ ËJóÈ\x001d£¼M×.b$¥ù\x0013É$¯\x0013âÏ\x001fß×\x0001±\x0001Ä\x0001@/À½¨Ãn\x0010ÀB_[\x0001]\x0003èz\x0001Qó'ÎPu(\x0003TøÚ\x0008¸h\x0001\x0000Û\x0016PFP\x001eDHX#¹ÔrIòp"Û\x000cØ4\x0005\x000faNm9\x0007Ò\x0017áûÃZñ°.Qzq÷ë?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=z\x0008O®¾\x001a\x0011jDèG\x0014\x0007\x000buR\x0007ìK\x000eÅÓ	:\x0011±FÄ\x0011DiM¤\x0012\\x001eI²NCïªçï$45¡é'\x0014läõuiï×jWô´\x0013ÑÖ¶\x001bÑ¶~\x0015AïjåJ\x0017ìP®FtÝÎrH_ÆWë²îAí¬ãèDô5¢ïF¤!r\x001bDQ¯"W\x0012â\x000e½Þ\x0018jÄÐh\x000bá¨\x001f@*'=çjçTNÄX#ÆnDZÑÆ×%én.ØQ\x000e\x000bâ.ëØXÕ¿Méû~FWÚ÷¢\x0000¶mµ«o¿\x0013°5-ý¶Å):Y+jqÞTÄÒ
·kþQ'cc[t¿qqZêiç\x000co\x0012SÑý]qNÆÆ¸è~ëâÊ4!
%A«¢+\x0006pü0¾'\x000fÎ¢(Æg9¹Tã÷wnÿzwûôX\x001c2CuTë9¤ÄM×z\x0014¿?»8=zþãÙéÅw\x001fn~ºùüåa\x000fÞ»¶\x0001ê"ÔAb
ÉØsñ-\x0019=';Ü
pþ\x001bëí\x0011º\x0019q÷ñþáîé×.*	$D\x001ehä\x0001$_8\x0017=¤Ñ³óË«³§ñ Æ^<ª
\x0002(õ±Ô\x0006Éc!ÌÕXw bÝ\x0012ô¦$]CQ6>H(Æ¹N\x000eDS#n)æ©\x0014ÙK\x000cÒ5Í-\KhkBûM
ÑÕ®[Ò8ëµ\x000c)Pº!Ã\©J\x0007¯ù|7\x001fÊO e\x0013Õ¥*5Î
ôí \x000c5aè%L6­¼üËÍÅ^qSE\x0013æªh:\x0010c\x0018»Î Ë94ÜäUº¤ÈXIX·º¶\x00034JÑn\x0017¥Èª\x0013\x0014÷LøYÈØ\x001an«T)	å,òmÑåCGØ3`!bcXt·e1é- ¤_åv>=Åæ9Ê»gêØRÄÆ°ènËbì¦ÐÜIkª¦iÍOðv06Ew\x0016\x0013¸«l*6Ì]âÉG*Ý%~{ÓØ\x0016Ým[3%ë\x001cÐ
K1õ\x0018¬ellî6.4\x0002kM¨Àó9\x001a$\x001fíöÌ¥}ÑÝ\x0006Æ\x0004(¥T\x000féø[oã\Î©±Qßº[¨å8:ÍAE­<nnõê\x001b\x0003nnÝhµ)MnIñä\x0011ìþù_Z-Fh4\x000ftk\x001e\x001bK\x0010ËQË\x001aªÉ_Í¨BMÜ\x0001Kå<FÉz\x0014l®
§ÇV·mØ½®ú°BÕÛ´Y>\x0017]	ëµ¤mT\x0018 \x0005cx\x0018ëä¢ñSoDU¹\x0002Ò% \x0010·ó\x0006q7 nöô¦¾yüüù\x001f²}Z\x0018Ã'Pâð	FlÎí\x000e¥C\x0013ÔÉ~×'×¯_îkfg`¨a\x0018¢L\x000c^\x001ea\x0018eÛWú5f)½ÄX\x0013ã¸eÌ\x0011¢q\x0012\x0017§²|&ù\x0014M/±©ÍCÁc:Ñm¦µE®~7hvUÁ\x0011ÛØ\x000e\x0013'\x0017ÞèB¬øT\x0004Ià$âÉØÕÄnJ8s?=YÄ gÂîÚ(0Æëk^?Ìk\x000cíÇäZA6\x0013he\x0018>îÜP:F\x001cjâ0~&ø\x0008£s\x0016g5Ñ®?Á\x0008¶UÄHýQBûêîö\x0003%ÿïÓ 6zYÃ¥i\x001dh^Û\x0010|\x0019:/ÙWg§Ï)áü¿\x0017pBÍ	C({\x0006e=\x0003ÁÉv\x001emæSS= Xâ\x0008¨7²6[ëiâÙ\x0004jd|³]cúAM
jF@DµÉ-ÌÝ\x0006$Q\x0004\x0001ÝUcÐ\x000fjkP;\x0000ê\x0014ò`ª
â#\x001aJEïxæ÷sºÓ
\x001dÑ(©IV\x00167\x0004iOGtÖéáô5§\x001f'çþtzaÉ\x000fF8Ý®Úèå äroUm]?\x001f=»¼ûøñþÓç§YÝ¦~\x0003ÙGH[$}µÏIwy}v~~yñúi\WãºA\ãOOVò\x0015'\+Û\x0005´ÞµQy\x0008××¸~\x00107AI\x0001R9¬B»©¥$AïÌl
á\x001a7\x001e\x0006,¹LÅó%è0 .¸n¬qã .­Æá±R1äöýisdÙç3Ø}´u8Z}·)\x0006èÄM\x0012\(Å\x001fª\x0014\x0005ìJ>\x000cáê\x0006Wãòòô\x000f*\x000b\x0015Ê¬äyuÛÉ\x000b
/\x000còÇîdÄd£¤-nÁ®\x0001ôCg×¾ûÐjÞ\x000f\x0002VTÙÍ\x0004ïÀÄüùò\x000c\x0002-WF\x0019[eF_üãïþñ÷ä}¿¸yüøqÁ?z)p2M?å4©´{X¾8½8½:9''üÅÉõùù>\x001bg¶\x0006BwëÐ©GÛkÀÈ´(¡0ïö$\\x0006ÈCM\x001eÖ§ãÁBwÔ	ì\CÒ~@òJÛ\x0019['ßÆÐÝq\x000eäÒ0©\x000brZ`Ï¼í\x0001rÝëUä\x0016,ñ:J°*äHàÖ\x0001ðfOo\x001d\x001avX'õRP
ÆaAQKëÕ\x0007=ëU\x0012Øq¥ÜÃ±YîÆHK±\ÎnÀ¥7#ìíö¿

ÓG'l\x000fõ¸ù×_n~ZðZ¡eëÙ
yS61£,\x001aÐ{2\x0004¯ß|¿\x0000\x000fj<èÅ³NF]jyõ\x0019yü²WPÏÎ<[\x000e5 ö\x0002:~$ób®TËî|ôÁ\x001aÎôÂÑÊeöè]Ì$Ó\x0012VñüÜîÝÅº\x0001Ô½ÉsÐ£¦1ÍÜã Êò\x0010·g\x0012ùBBÛ\x0010Ú^B[ªóÓuÎß8ùieØª\x001dl³Ð5®Ð(r
$à ®¸ê³íBË	}Cè{	³Ã	±øº¦C77\x0001x9ah\x0008C/¡Mï\x0014¦ÇÙ¦\x0005ÃÍMÚY\x0000\x0018Õª¨éôdxsûðp{óø×Ew\x000bß
ø2öW\x0003ëB£f÷
¤\x0007ÃÓ««Óë{\x001a\x0014jP\x0018\x0002EY\x0006kÈódj%\x0011°\x0004:w©»@±\x0006Å\x0011P;]	4=r¹ÜN Û*g\x0017kö\x001aÔ\x000cº$FÇ\x001eÕ±æX\x0007löªÎÍ¬ê\x0003µ5¨\x001d\x0000µydÉ\x0004j\zÛrF\x0001çLb\x0017¨«AÝ\x0010häi\x000b	4\x001e\x0003szÙü	nÎ2vqúÓp&¸À\x0002
:ïSáeu³\x0003«ú@C
\x001aF¨*+\x0000i­&fO2Ä²£tö­×Å\x0019kÎ8"ÐPÆæSÙ\x001brxÞñ\x0003Ã\x0018-éï\x0001­ÑQmÑ}\x0012õ<>¹»ù%D\x0002Ø¼=ÌUÒ­]\x001a1LNiÑNÖÀ±ç4Z5[Ù\x0005ÚØ%=bÒQd½?fw½Ü¬9Ä×YÒ#v¾<§el49!?}z\x0001]ÑGÚ¨{=¤ïÿEêÉ\x001e#6M?
°&÷#ðwêQGDàiúAT~\x0013QÔ~	(tá&GÔòB]åJJÞ(ñ¢üìÛ¼Ïª\x000c'?êfÀB	®&GJ\x001d\x0007éxôâG©¹\x001e¤>Uµ-Z­\x0007e\x001bõ·¨Y_9q¦b«vî\x0012ì×´c°>L#âS\x0005îl.Ëu
ì*ëàÕ~ëBÏ=Q\x0006TsqóávAäË9\x000c²ZÙ\x0004®â¢IrÅk\x0019
s.Nî\x000fy1*Ö¨8
%Ùi(\x001dÇ/]Hg»úHMMjÆªùijbÈKKÉõ\x000fâ©ºùÓÚEjkR;BJÑN®ß$T+\x0017K\x0012ÈÆÏMéDu5ª\x001b\x0012ªV°¤\¡Dî)¨³Í-}¨¾FõCR]a\x0007ºPC\x001aP}àÁÚ	59\x0006N^U¢YÃì.à.Ô:#ï+çºÕ Õ6N¬R¥iÂÜPÈ^Ôº½\x0019¡EÙ\x001ehcîþ¤Æ1U$;ÿjYaË\x0008`hÀ\x000fw\x001fo¾<>,(Î¤i¿±\x00029üXXílGòÄúÃÙùÉë½v\x0019\x0016jX\x0018¥j¬\x00080\x0019Û¨Jí«Ý\ß	5,ÁÒ7Ç§@Ëz\x0005X´ÖìöËNXSÃAÉNååÓ1 ±v -NáÜ¸^X[ÃÚÁ3\x000bRLdAÉH;ª/û5\x001bCïu5¬\x001b<\x0006Õ\x0013\x001fJ´\x001aÁHÝ\x0010Ù	ëkX?(Y»¬/\x0017¬\x00086ÎÇúXcÍ\x001a\x0007Yc±_èd_\x001d\x001aiI/Ã\x001cYÝªÙA=k@²**çåàIç¢Ä]æ£\x0004g¶yÉLçvóé>ºÞ£Ë;BÒÑuåè\x001eèéªLk2e\x001fÆxuQb®L\x000fC\x001d$ö`¼ï[Þ÷ß:ïMË{óòªí}«
ëôÛÉ§\x000fw·>\x001f=¿ÿíýÍ/7¾<]»\x0017\x001dRt°¢ÓtI¸¢Þ\x0013@8¹x~vzñúèùåËg'oÞ\¼ÙWÃ§¶°*¬srcôN\x001e\x0014
¢d½tP²uvqì0>Öø¸\x0012_{\x001e@ðô5j'ÁQev([oj|³Vú^´¶"sÃ\x0015\x000f\x0001dË¬y\x000eâÛ\x001aß®Ä§6\x0001\x001e\x0010ç@\x0006Ä¥£Ïá\x0008å÷åvð]ï\x000epsyx2EG\x0007##øæË@GñC\x001fÖK_óÕ¥h¶lþu Ò?´æ©Új³	v_K;r¡4
¾\x000ci<0}£7õZÅ\x001e	°ßX\x0014g«\x001bfk\x0013Gù\x001bÍ£×ª\x001eÊËÊäÄ ´:j9=³Ëù»«×^^4\x0012³M¨Ç\x0003á\x0011¢ôP\x001cXsêæîêÕ×øµÆc^\x001e7-
ææÂêëyæ{ryTþëè\x000bý¾$ï\x0010ëó¬¾»AºÈ©ÓMîn0úN9,swaõÝÇ\x000fm;é\x001bK·\x000fWöâÃv:\x0008|5âÚ´ûóÑÛ%\x00032£5e#(¥s3¼ûÔ\x0007>×çrM­Ú/_\x001d½8½zb§ßò\x00132\x000c#;<¦ kX8)_S»²\x0018ÄX\x0013ã¸A¶\x0018{<\x000eV\x0002\x0001eÕú\x0001eljb3LìËÞå$m	
U+×wåâ\x0007mMl*\x0003ÛldíXfÊí46Hìjb7L\x001cdhw"Þ\x00089Ø¼§¯\x0017Ù×È~\x0018vÊ0±¢.ê\x001c\x001dÚl8ßå\x000f\x00128\x001fäP¢,6¹w
\x000e\x001d$5q\x001c±ã\x0012ÍDìÊ´\x000fØlj
ó³Èº5"ãVÄ©2 Î@edË®\x0011·kK/3n
ýNÖ¡Ùç\x000f÷w=ººüeA\x0017V²t.*Ã\x0013­4­\x001cad\x001db\]ýÛÑÕåõ½Á¸­ù\x001f\x000c£ÈN9\x0019í\x0019rÒ\x0001d¯Ox"'Ú52\x000eK98éê$\x0005
¬6+rç+¸»Ml¥\x000c\x001b§³gFi°eºÝÜvÏ\x0001b[\x0013ÛUç¢(\x000cëøXlP½µ\x0012]Ä®&vÄ4H½ý<tsB\x0006\x0005¶è8µ7QÚ¬¬²7²ÿ:Ou\x0016³)~òÜªº\x001eb\x0007[\x001aV×MÀ\x001f?Þ\x001eß<¾øÛÊØ\x0019/ñcCn\x001c×Î(\x0015I3áãós"½~võ§§	¡&nBc_\x001ae\x000c·½i+i<5Tè!ô5¡ï&LFÇ\x0018\x0019\x000cyæ=UÊI\x001cÒèñK\x0010Ñlu\x001c¡QõÜûûO_è|¾¼ÿx÷é÷»Û'fúÎ<Ò\x0006\x000f&Aßà¸KÊi÷\x000c=¼¼xCôååùÙÅÛ³Ó«§Á±\x0006ÇUàXÀ³\x000bÁe8¾õw+¿½ðÉkø«Ï\x001f\x0017ø8Þ8ÍÓbÀ¡¢\x0017hely\x0004¦ósk5_¼>ßïÙøíMJ^\â%\x000beÀ++U=\x0011ÊæGcgªçÄ\x0003»u^ÁÖçõÅ#íãxüðëíÃýÛ$¨co¾)7ßÉ ³sO´^_ÓNëç?^]Îox¯uKûLëöüæèt@ohñÅÍã_¾¿ùíöÉ¸M\x001fUJý!D\x001e\\x0012¼ÛLéÜÕ@Ït:Oh	ÆÉõ¿\x001d}òòt>¤³A®òøM?\x0018%WÜ\x0002ä\x0015dnÙÍ\x0002;ëþû°iñ÷¶C\x001eå\|\x001cc¶\x000cë\x0004\x000e1b¦F¶\ çÚ<wÕ(òÜ½3wè>Þ\x0011;
q¡¿Îo?\x001f½x¸ý}bô*3ºÄøéöËgb\x000b\x0011Ñ§²9Úýh]\x001ek\x0008*Üãg
(~]¾yýÝùéë£\x0017W§okF~
E²%ô×Ó\x0014!ú)­4Q$UqW²27QhwRìþ­,ÞÝLÒ¸Y"\x000e\x001drà@X\x0016!\x0017å(`·(æ ÞÿÇãýo£âS,üüöèíÝÇ7c¶ &×+P×\x0015åË§¼ÛTsI;¸'\x0008´`\x001bI\x001c½=;??Iî×Ü©Ø@Ð&gúk\x0001\x0004rÎi ÂÉ\x0017\x0005X4qÌô×\x0012
\x001b½Ë\x001427Qp[g¢@n=\x001e Hr0\x000be¡pÊ~\x0012ER>>Ë6¿1cÏ³J¨ý2
G{ïíDAm¹Ów ü\x0007ä³¸.­\x000eñü\x0003Ñs¯ûrôòö·ßîöT3mcOD6\x0017K\x0007ÕiÇDÛë'"Rg¯"{sôòôåË³¹çBÅ\x00055\x0017ôp¹ih\x0006Ããü½B\x0008Q¸x\x000fÇ \x0017Ö\ØÃ¥§[ù\x0013Zî\x0001M\x000eNðò	5®\x000135é\x0004\x000b¶Ü±Æ<O$qÙUX¶Æ²\x001dXäôów¤Ç_îíE\x001eÎ°\x001cW\x001d\x000cr¹Ëõ+Ùp­3Q\x00184ÈUtv\x0015¯Á|À\¤Y5\x0013÷9#ô¥3"±\x0010a
X¨ÁB'\x0018fsâ\x0002ïÔÀäJÊB³A°XÅ\x001e°ôR\x000b|%cÌ¡	\x0006nWq®à2\x0016Ñ­ªÌçKIëÙ\x0015
X\x001d\x001d×\x001c2Ýjý\x001eµz\x0002É%ÊêÂE+¾\x000c1\x0018$kô¾îQü¨\x0003û²É_H\x0016É0YÎï¿`Ý\x001a²Fóë\x001eÕ\x000fÉ¿õLFG\x000e2\x0019Å¬2á5±dÕ=J\x0016(ÃoØ»°Zr¼|M\x0017V}ÍFËê\x001e5\x000b\x001e¦?"³!G&Ì0?ö\x000cí\x001a²FÍê\x001e=Þ\x0004ÇYÿ{Ú§\x001d\x000cË\x0015ð	Ì5nÔ¬îÑ³é4ÍS>f<æ©p­\x0013X£euÕ\x0001\x000b\x0017-ÏÍ`Vþ7aúFËB\x0005\x0007ÇL`ú8ðé·â\x0006A²FËBÕÉ³\x0000>ýÑq\x0003núZtY\'³Ö»îÑ² ô±\x00159R\x001eÌ0\x0016Å5Ç\x000c\x001a-\x000b=ZVk%Z6=ÚsÊ(ÉLûòvÆU_³q°¡ÇÃÖ´ßßé­\x0014,f2¥V5ú\x001f:ô¿"ç"¿n=\x0015O\x0013\x0001BP|ÎüJ5ú\x001fzô¿\x001cþ¾¦Î©$3#\x001e9®dþ\x001eý¼'@dQ)î8G\x0008V¾f4«È\x001aE\x000b=V©i~&\x000byMT"c9µêåÅ\x001e=þ»Ç|12c7vÔÀÔ\x001ae2Ã\x001eeÌÚÔ'H\x0002ÓgÞÐæ\x0019¶åN¯:dØ¨\x000cìP\x0019\x0016\x0010	\x0019Õ\x0018d0.JJ`¨ÖxØh\x000cìÑ\x0018!ÉåéÙF¦ÈÒMçéÂªÓÍ½Ä{©Ò¿¦Áz¤ËTÞ\x0004´«C´«ãa_¦èhåØ\x001dí\x000bµùi§Ù.9»êÅ¾À\x000e}¡<
¡cí\x000fç@D±K^«5/&Óh\x000cÓ¡1hÐx9eÉÉfï¦w³ÌÜ*»d\x001aÏÌtxfé§®ÈÌèà%ÈâaÕ#Ó4îépþÙ¦Ü4*Ãô¨\x000c7
¾À¬Í£\x0012\x0018çUÐ¯Ãj<\x000cÓáa¨ ­¥O{ÎË¡RVtl\õ3Â0=
ò³Úó½|\x0018DëåSê5<Û\KÛs-½vÇ¬aOH|Äè\x000b\¥/´-©âM,Cz¾\x00173üÔi7½\x0004§l\x0010³i\X\x0003Xå²KÂ¤&ÓrvÏ\x0017ÉÉ	\x0012	\x0013÷^©<ÈÉ]xFCy©tëÕÃ?þþùè§ÿþÏÿ:ýtôìf.ñ\x0019µ¥¦Öl£¦éz\x0013\x0017í\x0016Î\àuån¼º:}}ôýÑéÅÑ³ùLð¶7\7=`¹ñÀ¬aåT)d\x000eçÈæ?gS«P·g~¸ÿ8%Ú)#ÁY\x0003í4
·$ã¶] ê9}~y¾'[\ °ÂÅPÖ£Äe\x001díP7\x0019ÊhÉâ\x0018=Îdj&³ÉiR\x0012\x0013SÇ 0ùm¿¿ÉÕLn9SRõVbþ(i¸èï^!(_CùåP4sJÞÉ;$z]R7Û^E\x000fT¨¡Âb(üiþz4©<°R\x0000ÚiãL±f4ºiÚ\x001b=%C6ØÆâ\x0008?~ª\ÙäjH6Dpp\x0013\x0014lÄBíDM\x000fT« k¨ !åbr¡ó\x0011Ì®C\x0012ÒÁñk§\x001bý¤+(ÚT#i\x0013x\x001e\x001b\x0006¯%i·=­\x001eªFCéå*Êè©\x0012+g\x0018\¼°IKú5gªQQz¹Bë¦©»S\x00103oåmQ1¬ jt^®¤ÐçEÍ\x0013\x0017ÊWÙN-÷@5JJ\x0003Z
\x001a-\x0005Ëµ\x0014)½1\x0011¥Ó\x0005%ÓÍ\x001fÏê\x0015î\x00014J\x0001:\x0002¹ë\x001c\x001776OH\x0007Ý\x0006ùx_ez¨lCe;¾âpMzÖ\x001fkàÀ³$\x001e­Û.
èÂæ\x0003âò\x000fH©*²%²k¨O»Æ½ÃFQárE¥Ó«AbôÁ\x001e;ÜÑûí\Ð"*W÷å\x001f´ýeç¿>Þ¥\x0017Ga9ã£\x001b3­ªt<§\x000fLºRæÜWG
nÏ¼>{sµgle\x00055 v\x0003z©+t$;\x0006,¾q¯¼«^>Só\x0011>~O8Ìí\x0017Ä'F\x0008=¬\x0016 ­\x0001m/ ÅØJR\x0015sÈ\x0016A\x001cy¿Z®\x0006t½.Ní6ì?ç\x001a\x001eZ±)Úm»Þ¯Ï×|¾Ï"Ï5Gï\x0011Å \x000bk\x0001C
\x0018z\x0001*~\x0010È\x0003ÄèàÏ¨¿z\x0015õ\x0002Æ\x001a0ö\x0002Òþ5\x0006Dà>
J8oÚµ\x0012¬Þ%®Ú¹Ð«\x0008=IÆD\x0008ÝvåQ?¡n\x0008u÷G\x000eEé¬\x0007c(\x0015HÛÙ~ÂFQënM\x001d­/ú\x0000¼\x0013:#JaÍ×\x000eA/a£ªu¯®¦B<\x0017Ø»ãNõDXtµUÛ%©ý®ÖÝÊdXDÈºzj.©µÆD7ºZ÷*kXDh¤j\x0019E¸¦è'l´µîU×^Çi\x001a÷Ô\x0019b¹¼%}d(å-ë/J£®u¯¾¦­:²;è9\x0003e GLÒXAØèkÝ«°©úÒÃê8 	Þ\x0017í·kÊ»\x0001¡Ñ×Ð­¯½;vöO\x001f9d\x0004G8½Ãî\x0007lÔ5ôªkªÅT+&\\x001e­DßØÔrµ\x0006\x0005\x001au
½êú_AØ¨kèU×AO³´r¡¤ÑÒ[Xnß.Ôï'lÔ5ôªkÖÊQëóH\x0004\x0018E\x0019z0«\x001d¯Ð¤Ò&ï°\x001dï¼ÈÿrR\x000bj¿³(¾
|ý&^L\x0019¶1A1Ôpÿæ×ü¿ßo?Ý}\x000fmð´^ÖÖ\x001cX4AÌ	lù]ÔbÿæÇÓ·§\x0017gsmÀ\x0015©±L\x000f-\x001ekp }\x0005ÁÇ(q\x0004ô+¸lÍe{¸¥b¾´&\x0016N\1K»\x0006+ÔX¡\x0007Ë[éÙ\x0012\x001f\x001aèc\x000fã\o\x001fJÎá\x0000\x0006\x000czÀnc\x000b\x001bÉYFérb§­¤Q'W£42\x001bk¥×RIÔ%hC¦6Ö]n\x0015üõò}\x0006DÔ|ôå|´Ó$!fûa£Ò¶*R\x0016ÒzÆTþA5å§Ç£\x001fî\x001f\x001föÜM(ÉÉ`¥~-D©_Ãh¾Öeß_\x001fýpy=7½\x0018`»Ï\x0013ªÅ¿4©ëÓ»/ó!mê:eØyÞ3¡¼)¬ý:øHC¹.Þ\½y\x001aÌÔ`¦\x000bLKµkvL\x001a¶xÁv
W¥4 NT.\x0001³J28FZ½ÃïdÿT/Ý.§(£4¦ó5ó\x0017\x000f7rïI£Ü¼å;æO(Á
m¾¶\x0002Ù¦¿¸:¹ ØýGÎn\x001f9«ª9?\x001dÔÍ]SÉZq
lz7Èßq#z@ý6¨¯@¼yü2]Û§ºÆ=ÍzßX(ï\x001d­ÅJ¯µñ'×o¦û+-äóeG*aZ%ÿ×ïQ@rú{jiv÷¹TE}ÚCi%UV*¢Ì\x0014³áÐo¦.\x001c=»<{]Ê¢.f;Üí»÷ïyøõ'>t\x001c¸}ømúÊ/î~¹º\x0004æ±ß$ÿö·xyóð¿øõæ#±\x0005åÌîHoWgù¨0õkÐðô\x000f°¿t~þ§£D÷òäê4Ýóï~8½z9}ó\x0017g/Ng'»Ô2\x0019a\x0018\x00132fà
{ÂÌ*:aJíó\x00010ÓïK
abàq>\x001e\x001cÇ©T01\x0007ti\x0019\x0004·¨­ÇäR=.Ð\x001b<²2}z~¥\x0011lùòaÝ\x000f?ýõá¯®¿|\x000fK/\x001fá¢\x001c¤ïÍÍÉ]àiÁÛl4we*$þÊ=H\x0010xÌ~z\x001eÜLä\x0015$¾;¡Þ+¬ç\Ù¤f°Ì¹¢)<¤ªßOYÊ§ }\x000c¹w31F
6\x0013bRèõÌ7%[H\x0013xHm?Í]V¬P³Â\x0018+µ×å[aªÎ÷ÖñD¹à=Ï\x0013\M5-\x000eJV³\eZ#	G+äoìÖ?Ý¨®Fuå¤F\x000f¹7Ñ2«\x0019©«Y}Íê\x0007Å
Gý¦c0© ?M%Èb5Ü7¸\x001a5Ô¨aôn©,SË5±$S`ÔÕXÆQ¡æFi\x0012*\x0005D2¬Ñ¹UÓ¨¾ÃÐ²³.:K
ÖN$[À"#Ùòê§@]ÕÁmUì¨¥1|d'ú&éÊÂÈ`¥¯b5n£eõ %}\x0010mîæ$ÕÅû=a¾«i\x001b-«GÕ,&/4Ó&\x001d½$[Þ\x001c\x001aì$k\x001aV3j\x0012rà`½Î95\x0012­\x0018\x0005Ô»½½nZÛÐÚQskx+\x001c¡çf8rHË±uî@\x0007¡±azÐ%^ÜÓ\x0000êXpyÓi°Á\x001eH)4fL\x000fÚ1o\x001d¯éö$èiÐHÂIÁÚ\x0003iÜÆéASFSï\x0010³pµÉ[\x000c\x0012­\x0017GÑÊNéµ¸Ð\x0018\x0008\x00184\x0010ÉûwU\x0002£6|toýh«q[¿vÔ±µ\x0007ë{\x001ana\x0018Ñ¥f\x000e$ÜFÁ \x0016ó(«Ð§\x001b³\x0013\x0006±¨\ËÉ°õ\x0012Ý.\x000f\x0007Iõ\x001f`C'!\x0004ÒÂù\x0000³Çþt ëf·«½~\x0006ÔúqÈEÊ\x000fi\x000ft?¦§$ýÏ½ýíîSW áæ\x0010F>Æ^TqhÊ9Þ-äç?¾<»X\x0010"(¼PóÂ(¯±´*D´øeç\x0014'ñâîÜÏ5/\x000eñ¦Ã uÞ\x0000ü\x001b'/\x0008¼I&\x0000¸¸é\x0010í×º©r\x0010¯nþ¶L²ÒåÓI\x0008Ús\x0010SÑ@]v\x001d¢ÚóúùUÿi\x0001¥©)Í\x0000¥WOH\x001a Ï\x0014J\x0004Ê\¬§´5¥\x001d ÄéægÊ(Æa*\x001dbJ7\x001fJXLékJ?@é'å\x001aè²_ë
!îñe\x0016\x00130ô\x0012\x0006z{NÓð\x0008\x0012y`ôâpE\x000bófk1e¬)ã\x0008¥JÆÒéIQ²+Äyu¿°~:]¶\x001cyX.æyÊ{U.wðóöbÌF\x0005én\x001d\x0014ÔÔï
ÍtççøKÌ3×R6*Hwë ôSGð\x0014·¦v6rQ&J£\x0004\x0013Ô\x0001Ùè Ý­\x00083\x000f¹$LTÇ)£cJ)Ý_Eé\x001aJ7@Üþ<Æ?$ç9\x0017$LÇ\x00162*t\x0007Àl\x0014\x001eÐDFQå;VS·\x001ea\x0006Çÿ%L)îY	Í={®\x0004&MÒÍ\x0017(`\x001e\x00070ý\x0007õbÌÖÕ\x0018¸ç:=¤ó>àéÇìk\x0004Çû£¸þ¢CsÑaà¢k3\x0017FÅÜB\x0018£cQj­\x000eÀØÜ\x001f\x0018¸?`tÞØ\x0013lÒE\x001cðIn=ßr\x001dý\x001a\x000b©ÝVÖ.üwßq}Ab]æ´§'g\x0004Zÿ\x000cùs\x001b¡\x0005ífj¹Î ¡>\x00085"ô#º\x0003¨Pç9ÝÐ\x0007\x0010ÄXI\x000f"ÖØHnáE¶tÏ©\x0002,;CÀÞºÝ¡È\x001eFS3n1ÒÈ«À_ÚªcÕ¤\x0005)5 zÕ¶f´ýÄ°\x001cÑæÍwô'¯÷~&ñÜÁèjF×Ïô¸e9&Ûí²a*iSÜ­Ç{\x0018}Íèû\x0019½,(®S»Nø]^Ã\x0018jÆÐÏh
7\x0012#\x001cg\x001dn£\¹yåô Æ\x001a1\x000e\k/¶;ü\x000eó%A.MÑ+\x0010«÷Ãä°
|j[®uÒBÊð§\x0016
î­ßm\x000b{ [#ÓkeèãQ&·	Ò\x001bG´ÞÝ¦°\x0007²13ºßÎ$
Éi{r}¹\x0016Ë;\x0014ýHáîµÑ\x0003vÖä$R!OGNÄ Wë\x001eÝØ\x0019ÝkhèÖØi¶â$GÌmZ1åc¯flìî54é¦\x0000ïù¢,b^@¤(\x0015#v\x0006Ö»=º±3º×ÐükäØØ\x0019ÝkhHãø©Ru*uñ\x0012M\x000b&Êy\x0003\ÆÐè^KC\x001aGÖÑ\x0017$_Ûk'h×íÆÔè~[\x0014¶¤\x0004#\x0015ße\x001du(µc«=\x001fhl
ôÚôG-5úÚ\Øä}ùØ¸Ú\x001eBcj ßÔPm WDê-ÓüêR"ÇPy\x000fcû éµ4¤}4»¹ISÀ*«\x001f#_ËØX\x001aè·4à\x0002otö\x0014ØÏ.EAq¦\x0016¤\x0007²15Ðojh\x0010\x0012ÆRoiKLE\x0004iÖ36j\x001cúÕ¸¦X\x001f§J©ÓU¤÷bkT\ÿµ\x001b\x0015	ý*RGGMqùÖ¸cQ>ÅÓU3Ó=Î¸nR¹S´~Ð\x001b
Pü]\x0012°°*p\x0000\x000c+¡­Áù\x0007ÁGÏï\x001f¾Ü}:úþþaéñ,1sTK¼uäÔ~zÏ<\x0015¥7æòê
e\x001a/¯\x00160CÍ\x000cãÌ´K"Ëö½H²èÏdöfñº±fÆqf\x001bK'ª\x0012\x0001öZâéÊÌVõ2Ù3Ó\x0014\x0008Î§Ðüv>\x001bVÂ\x0008Q6.\x001eÙÖÌvc\à±èÚÈáÌ\x0010CØ\x001btí\x0002v5°\x001b\x0007\x0006Ô\x0000mÁAJã¾*Ü^`_\x0003ûqà(»½\x00038%5\x001fQ{ÉXú\x0003Þ¾P3qfeù
\x00104íøÊ'ÙK4>¸§­9ÖÌqÍIÔ\x0016õ]Ã\x000c¢åötjt2\x0010ÏÖè×nh²wÈ¥\x000bÔ\x0005££Þ»\x0013¼=Ø
Ô­	\a\x0003-r\x001diºyª¸?N^±ÑèÃA7öD¯0(({á§"\x0011C\x000784õº\x001e\x000cºQÎzv¦\x0005
¬ìÈ :É²\x000ea&¨Ñ\x0001ý>Ù­²¹bìæ·?\x001f]Ý?þ²ÌsFqy´J\x0012&4p£¼ÒæjÛN^¾:ºº¼m\x001c­ ±Ä\x0001Hl\x0010¥F)Í\x00001ÑÎÏ\x0014wA\x001aÒHÒN}êÓûÂPwÿ$J/Ýë\x0019ÑEéjJ÷Q¦÷Ïß\x000eaòÛÏ~ûóÍçÏyÖèÛÛ_n\x001fUÒv$®Ï FÒÈù¼\x00121aFi½|uòúuCúöôêÅéÕjQ\x0008[^0ä!0ÃÔ`òwÊ§\x0014k¨\x0000Ò\x0010²­í
d£§9#çîáj¼<¡wz!­§~¯\x0010·ë0±øúßÿù_\x000f¿-|ZÅO	xcµÇç^[v~tyõrßecN¬9q\x0013J²¥ÝÄ Ò!?\x0004«©YÍ(+LsÕYi0¼ÀSÓO÷¾ß²ÚÕ±zòÐ¹kÖh±\è­(²0c¹:Y}Íê¿mÖX³Æo5yü[Ï÷ôlnséøãÑùÍï÷w\x000fË`%xò\x0011¸ø\x0015Q'Ï1Ë¥ã×Gç'o/ÏæFtÉÖÏF®ÁFÑþ«ü-Ñ³µ\x0019ë¤/ÐXCã
èÚÿ2\x0013©ý¯Ý\x000em\x00174è­øYúÁ°q \x0012ølÎ¨xûÔ\x001a ã\x0012Eö$+Ö¬+\x000c\x0004´<#\x001bÂªö\x0007 ²uPÌê\\x001e\x0004O\x0006\x0002\x000bëÞÍRT[£\x000eÚ\x0007çý±çp\x0012Y\x0000\x001d6¥\x000e{û\x000b²úuÐ>8;M½Î¬@£|&­\x0010äÊÌL,½5Ö¬ö\x0014\x0018p\x00127ù·A\x0014¸3h×VÜÖ\x0002¨¶Zu\x0016z´0­°ãV\x001d.@·¶\x0004è=QôùúiLSc\x0011L³±`Ás\x0005º
¾\x00048fJú0miG01Ð
-	ÄxiÖ³~º\x0002}\x0001¦¯1ý\x0008fºôy\ÎÔ±#m&`å«£=ÄW\x000f5gèæÌM;.¦\x001dm¤iÇ¦'KåæÜ\x0004<\x0001g\x0007(æ}_5Å@\x00174Å,\x0000mn»î¿î\x0007iYÀÙ\wÝß¹1\x00069\x0015éó*­Æ'Ê\x00166\x0017^÷ßx\x0002
<j¬mÀÖ\x0005®át#Ô\x001c\x0013Ks\x000c÷ xg\x0005\x0014Ý\x0001\x0004
­=\x001a9¡£ïè]^q¡¦¿aÊ ìÉ\@ÙO\x00189:¤	0N«É§Äb
\x001aµ\x001a\x00075ï¼ùðÓOÿÁ®39Ì4?ðæËÍÃO\x0015ÙÀÑlÁKS$\x001d§1\x001684A3K',kÛV\x001a\x001e8
\x0011<ysrõýÌëÎ¼ûõ··ÿÎi)¹Â\x0003ä\x001e^Ý~¹ûrôìöæñÃ¯·_ S¢%Ýq\x000ex'³¢ÇRv6½UímøxÜõÑ«Ó7go\§wéÜüMóÎ}øbJ]DÕÍ?Ý|úéèÅí§/w\x0012$êij\x0013	fÌä\x001eæd\x0017óèYmiÌÈW¨ü^NÄ\x0017'\x0017ß\x001f½8½x3;Ö¼³þË_?}áDÐþ9¿9:¼û|ÿåËí\x001f:ÊCI¹é6Ê[Ó!´\x0013
ò>9:¿>{}ùæÍgiÞ½WP7êwÏ¦¢­$z\x001eçi	Fö\x0004}Þ\x0006$è\x0004\x0003ì8'G%½sMÿÉ¬ô
(Ô 0\x0000
´Éo$\x0015\x000cæG\x0011BÞ¸¢Ö`\x000fÁikN;À©\x0003¢\x0004£ÏGÆse¦¯ÿõü\x001at÷â
Ô× ~\x0008TZ\x0007
uÈä\x001cj\x0002\x0015-\x0014]\x0002ú¤DC
\x001aF¾|\x001eÎ7}zëÙ¿éêð-JæÆ\x001f\x00024Ö q\x0004\x0014%²d5"5yL £N[õµâ\x001c\x0000õï>´\x001fÿÃ\x0000«¶üJ·Ip°1\x0002rsS²¦jí}â=ÚåFÝÉ\x0015}¾RÉAr|\x0000\x001cÏ\x0000±²unµXjÅúÓXã´².Uò8Ø ÑÆQ\x0011«Z£¦C­\x001a½O?ø®]²Ð4\x0001Ð|\x00006u\x001f\x0011,;ívHµÚG!&êIT¬Qq\x0008UÜ+¢\x000eå¬²PÁh}\x0010T[£Ú1TéL^)tL¨Í\x0014l%óQ}êÇP\x0015×´'ßÄ\x0014mZ|\x001d\x0006u4Ö¤qTÅBÞí9ëH\x001båðkK5Ê!\x0006¹Ujô¬æ¡²ÝQXùíîÀÃaX[
0¦\x0002h^Õô|·&é­Èz\x0015x¢¨3*|m\x0003FX\x001b\x0015 \x0007ub\x001b0yÒE\x0007pb\éÃ\x001c×MAyÑ®[+~\x0016\x0013{9µ:ðBìÉ\x0014*ØJô\x0012¿O×*lKV´\x000c=C?ç\x0017ßç\x001bûü\x0014©.%ÆYÃÍÇ´ä=Á)9öõôu~ë½Î\x0019±¹J\x001a´ò\x0005&Ô~V0æn!ãâ\x0018^\x0004SXã®'ÕbÖdU#TúÄÂó^O_îï>-°¯yó\x001d9X`yþmrZ\x000c_.egV^\x0013prñæòìbÏy\x0015PWº\x0011PËû	# \x0004\x0014ânÕ	êkP?\x0002J\x0003"QST\x0000uï³Da÷ê\x0004
5h\x0018¨ã.'CÔÀ7ß8\x0001Ua·kÕ	\x001akÐøíJtcW±²«Ý"õEjËPHmÇjøúÚ\x000fBC
C÷ÞrªÖèLy¼è\x000f"Rl@q\x0004Ô\x0006®1^\x0012Qá
{ÌÖn¯º´Ñ¤zLzöS\x000c­èN*AÞñ 2µ
©ýeÚ(}=¤õÓÕ·ÙÒÄk-1\x0015ætú\x0010ÆI7:_\x000f)}ë¹Óx\x001f¸Ä7IT@w½§\x0007@\x001b¯>õ³æOO;0\x0002?§<J \x0015Ã!H¡Ñ¥0¤Kõ\x0014HÖ×Z(,S\x001fà\x0010º\x0014\x000f#\x0017?I\x001fþÆQ«#rDÓÛµZ£¤Í1±cú/R¦õë\x0015ª<Oº
jä¸¿1ä\x0005djä¸Æ\x001daêåÀÉç\x000f[	
ºcS³Q÷KrQÔ!½hç\x0015à\x001dQA*_|òR¿vNÓ¿s\x0016êro\x000eJ u\x000b9Bé¸íÒ¹ää®ö ñIow<ù·\x0019çâýÓ´øM¬úy§yBIó dy@²<³±¾¯\x0012\x0012[©¨\x0002èk@ß\x000bØd#¢èù&\x001b1¸Õ_dJÑ¹Tß<>Ü|úðô­}i0u¾5\x0008yMâtkv½>¹fôüäúêäâù\Z\x000fÞ=<ºÿóÓgF%À·÷w·G\x0017·¿\x0013\x0019°\x001f
\x0013ÙÝíÃç?|¾üüW\x000f7?Þ}"Âdoâ4ùßyoÐû<\x0014)¹É<NC9,\x0019ï³Ó«×G¯/¯ÓÓøêäõùÙÅwo/ÏN.N¯ßÎÝë0ý¢fn\x0008mzzB^l!¯\x0001SÎ»!B¥¢»ü¯\x0006\x0004.!E5U5%AjÍ[×£1)a³ûákÌ'§\x0002TXcnOÔXéyæY"\x0005n(K¨6Ç\x0013ª+-zëPMº=Wc\x0011ª\x0006O3\x0002'Tyh\x000e¤·g®\x001c¡ml¥\x0005r\x001dª­Q·'9-D\x001chJ¨VåàhBÕyí_B%·\x000eÕÕ¨Û@¡ºugBª5(x\x0003béÂ+;ã{8CÍ¹=\x000cä\x001bâ5çöÈ¤E@cò2oö-'#'|ÓEs\x000b%,\x0019õ«1}ËXÏ¥DI¦Tâ4¡&s/¨\x0008óÚ´\x0007U7¨Û\x0013¾-±6ÿ«}ËXIQeío´§-ï\mÓjÂAn¿nÔÿW³û¾-¹6úÿ«\x0019~ËX¥BæÅ³V\x0005ÍJ\x0015iþjÔ²ÝWô?ýý`yêW.\x0007\x001dI°\x001d\x0015\x001d\x0016ÁîvíkØw?ûó\x0008o©K áz¤péF\x001bÃJãÚ<E`û)òñæè{êÈ¢\x0015:Ï\x001eîî¿|^ê\x0013FçóTBoÀ@ö«ÁÐà®£WcÙ\x000fÔ EKu]]¾KóT¿
Ô¿
üþU°þUðÿs÷nÉÜØÁîTö\x0004û%ôÄ*Q\x0012;X¤~VQaûEAIÄvl³mÉOßþÇãqôL<³\x0016°\x00166°¹@fù´#XÙíÒ\x0007$°nX­B\x0005\x001f¬£¥X\x00122èy!¸f)¶^Ýd)Zäb`\x001cé²{©·\x000eiõ¼\x001c[;¼+®\x001eÚô¼{{ûüáÃãýâ%¸èOÈ\x001e\x0005¹äó
ð¦³cçç¥Ñ¾DôíéÍÛ·è¾H®jrµÜË\x00132ûp {¾\x0011F
ÇF¿w¥FÈuM®×\x0007Eì±hMæDmeÔ¤Z¥ó7`\x0004ÝÖèv
:×ãË«MÎD\x00027Û\x001aÏrhSp_ûUà6î\x0005¨KÁ4\x000c\x000fð9Wb³Ób\x000eo¨iµÙ\x001f\x001f¾ÿùîiqd#\x0015lQÈ ×&y©¤*ø<ú^Èüùê\x0012Ö1Û/§BW5ºZ.l~fÁ;JSì@> *yôÛÛÜ®!\x000fN(\x0002W,\x00163¤nÁ8^"ØûÜ¯"×\x00145FôÓZ\x0001]«\x0012\x000c1Ûnz¬Ñã\x001aô4:\x001cy3²á\x0006\x0011Ù?bÆ\x000fËö®º¤(\x0017u(\x0001R£I.\x0006õrt\x0004]7èz\x0015ºóåâ,¼¬H­)Þ\x0013|MÙ[*W]S/hì\x00138'ÞðÁ\x0008°\x001dj¿È,^À®\x000e*'p=>\x0004øÿùÏÿ:}zº{ÿþn©BÒRx6\x0002dÜâ«Q³EoÍ¼_u}uó\x000eàw§××g\x0017\x0017³c>Ó\x001eC}\x0014H\x001f\x0001-mûåãbwPE,-£\x001edN\x0005\x001e¢çã"Ê\x0017À¥]¿¼:î\x0016C\x001eH¦kéÆä\x00024\x0004\x000fE\x0019y¹\x0019øÿèÙÿ^ïsj\x0005\x001cu0\x0003d0¾l»=\x0012ï¡wöà¼8ÎK>èw»o\x001ezºûmñ
Uæ\x001e<,Øºl¦\x0007v\x0011Gz>æg»o®n¾¼>«`H;\x001c\x000fyl¦Ù~Ø}sÿÓÃòë©Í5³\x0018ö°øZa\x000f-ù´è\x0018_6\x0018±á×ùÇïg<4ºb3Ö¶\x001b\I>æÆ©\x0012\x000b£J1\x0000\x000fGL\x0001pS\x0015àø
Ê²\x001cCú9¯ÊÛG^q\x001fÔä©R÷úéöþ°×Ç"pgi¨×Xò²4õ*ç\x0008¬Í\x0017,¯¯OÏ'»~ÌbSº³Ú>Ë
\x001c\x000fy\x000eEzÓ
ÜØyY~H~ä¤ØÃb¢pàÅ\x0017s\Òâð:¶¸èEÚì{\x001f9-(\x000f«×ßé\x0017týmü·àß\x000c\x0016Ø\x000füÉEÐXûüt÷S®Í&Ckzâ¿{øÓ»§G¸\x0007\x0011\x0004FÎ³ç\x000cNui@æÒ+0m«\x0011Îg»w×Wp©\x0000\x001aë¯Ï¾¯ÓÖß~üëwýá×\x0008ÍÔuÚo\x001eß§¢çãà¡ç\x0010\x0005\x0016Da\x001fç\x0013\x001dS0"!\x001aUÍ\x001e9D\x0004çøÍÕÍÅlÉ³þV<ºïÿC×Øµ}:äÓ¯äù9\x0002öÏçòq%¼©Ru÷pÕÎÍ}Ü\x001fT?Ö;wq·|Ï°\x001cËÐÜ\x000b\x0000öÌFÃ{VµWÛcaW¼[sT?¿ÿùÇç§D\x0005\x0001þ¼\x001b7åÕó\x000f÷@ð"Ân9iÊu\x0004£[æ±áÚ[jÂ¬öb
.]\x0015¸\x0018¯nÞ¾=ßÌ2µnþE\x001bìxõt÷ÃãÃ\x000f·9wì\x0005^\x000bþjÎ\x001e^ÓSNý\x0016rc\x0005\x001c¨0Á»·ã_]}~uùùé|\x000eY\x0005­kh=\x000emc&ÆÞÜ1\x0013\x001bCW\x0006{®lGlkb;N\x001c$e½G\x0010üÙÏ\x0006hoéÌ
5u\x0006]ÍìÆAØçÄbØhÍH
Ö<o´ßp£}
íÇ¡czãMÐ!\x001035W8iNoÇ\x001cjæ°9R;q8\x001c>Wm!tä³QeF®e­Ü\x0018\x0017\x001cÆKc¢ò$3K!ù\x0016\x001a±Ý¦<\x0000VãÐZQé\x0018¤Í©@\x001açºñV;¹Ý´ãâÎ\x001bGãc#ö¶K½GtÐ4\x001e\x0011|Y5\x001a_Mm\x001aj3¾×v¿×èØ¼×©EðSÖ× u#óä¸ÐsÎÑ(Ê\x0018Ï!" 9º\x0005^Øò26\x0002DK\x0010À¥Æ¢i\x0000RÊ\x0015ÕA@·Qn'ô¨l\x0018g\x0006K)\x0004DìÞ\x000fµRe£MÜîP«Fê©q©\x0017à*lÞáÐR\x0005Ñ6\x001aæv\x0002D5\x0002D\x000b§ñ%jlX%3µ´×j¬³\x0001uc2©q	\x0014KªÄ4ÚÄ\x0015¹¦Qáa;ÓT5ö\x001a7@"\x0016Ó	\x0013n³yjµ!«I\x000b¹ØS±¡ãÔÆçÒap[DÌE$@í-¹ÊZm¨Îus\x001bõøm^\x00104\x0016êf
ãá¤µòµF=R°S¼¶@·CÀv*¬ÂÍG­ÐèÓ[lx,Ë½ÌÆÈ²¨CËw\x000f?Ü=ÿíén÷áùi÷êöéÃËðZbË¡\x001cWQ(º³ºáQ2pT¤%´|vùùÙÍ7×g»·7×»W§×o\x0017¬A5kP«× ÝI¾¦JaÁG^\x0002uMÂ ¼¦«`%ÕK°.wÒ5\x0018ê¤\x0006k°.­ÑnRï¯¡äcÒ\x001ar>æªU(©È´u&wYÂ\x0007DÁ%îþ\x000cÓáÜz	\x0014Î­\x0017q»r\x00151R:lIÓÒ@\x0016áKKE3þÐØ·hzÒç_PÖÈþ¡ëõÏ·Ï¿.ñò]ÖW8RÐ°ä\x00073Zº9%»ÝzýÕéÍ?½L\x001bjÚ0H\x001by,bÔVçè9Ð\x0006\x001ecã±\x001a{q+)K«n^]¤WÆÜD\x0008ÝdK#>1]q#Þæ0ÈÁÓmBsCí¨\x0002Å\x0001¯¢®µ6õ§¡N§Ì¿¨ãÿóÿuöÓûû%wÎ«ÀíßeÊÓ,ÒX\x0017¾þ^îÎ¾¼8?~ËÜá-s\x0007\x001f\x0016\x001aEs\x001b£Óö$\x001b*`¿Rwe\x000c¡lAjjR3F\x001a¸\x00058ì)M×AFÐ±\x0004²\x0002ÕÖ¨v\x000cÕzvÕ\x001d°qTú\x0002i[ºÔ
\x0006\x0019hØRtVrôWGI×*JqÌ×]\x001ajÔ0j4\x0007ªµ9å\x0001\EnU\x000f¨ú»\x00185Ö¨q\x000cU\x0019jw\x0014¹\x0004\x0011w5Wq\x000bTÙJª1Q\x0015\x0000\x001e-0ÂD¢Ê`#³*},D³µ¹Vrì^\x0005g\x0001\x0001ªÍÝd5ö\x0016áÃªÔ±`ÁbÔæ^É±\x0015AZ\x0005U¤\x0015\x00056À\x00034,\x0003&_ÛºY}ÃêÇX¥ÃÀ\x001c\x001fWK.¶Ò|\x0004dØä\x000847K]-ìÌÄÕWAëµ)\x0002k«¥«¥®\x00168QÄ\x0005ÌÌê¼u\x000b= Z3`È\x000eÐB\5\x001dÀò¹
\x0001X©å]\x000cK´ÀíÓ÷w Ôff³
Í¿§Çû_w¾»}Ø}~ÿÃýÝÓËg@Ew%\x00122×¢kóuÈ\x0014Ó\x000eòM6\x0002¯¯Îÿi÷ç³ÓËÝççÍ2«ÈUM®VTÈ
rR\x001b< ·4\x0013Îöl,k\×äz
¹\x0006\x0019¡òYÆV>£{A½\¢Á.é[¢\x001aÝ¬ÛtÇ¯Åx^,\x0017°ÌÊyÙv×mnWíº\x0016xJÒ®[P\x000e»Nå¡°ë~Ö<\x001bCw5º[¯°ù¬K8õ1ozÐd­}±í%
5yXwÔ
[ïÒ	r4à¨KÍîç¼·!ôÚ×ìÏ²ã@ÒÎ÷R19¨÷mÈµ8éX­Mçy÷æöãS®Æzñ©^³d±$""«\x001d©f-ÝSø¿gË¯*LUcª~L\x001b\x0003Çv¬±1UÁ[`\x001aÓ\x000c`ú¬\x0015­"À2ÓÇÇÙ#Û\x0003hk@;\x0000hsIO\x0000u!r¹ Pjj°\x0019½·Ý:(]Mé\x0006(¥*ÑÂù¤ô\x0000a\x001cÙ\x0017Øêj\x0003L_cú\x0001L\x001cL\x000f¥q\x0003x`eÓ¡ôfþ©\x00033Öq\x0000SÓüÖh¤0\x001f#ÏÉöj2Óµ²\x0012¡õà¶.LÇG3·H)¼æÍõ,;([q9 /­â\x000eåÑ(»Eh\x001c+ÉGóH\x000c¤³rD`\x0002ÊÂ\x0008OIþêÏ¦UD=À#\x0012Sh¶j´©³
`:\x001c½}t`6bSÈMIÏ \x0012\x000c©lD/Ë3È\x0016ÊG6RS\x000eM\x0013âÉ:¤fïÓÁç¶¹BÔ\x0003bÓD{0LMiÒñ³ÏÑíÀl¤¦\x001c\x0010&R\x000fÀôO¦-¯I~û£\x001a©©\x0006¤&ø\x001fl*c¥QÎ\x0015(SÜ"6"Ù\x0000³\x0011j@lâ7§4E
\x0016½ÑüÑË7ßb7[+s@j\x001aã9ã]á`l¾P®\x0010\x001bÜô*w\x000b9õÈMwåéP§6ôi;y\x0000Qtz>\x000eÛÁÙHw5 Ý±2ð±m\x0011m§¡F\x0011\x001bænÙHw5 ÝwÂ_b-öþLÛ©4\x001fÏMºj\x0004¼\x001a\x0010ð:::¥Ö¢\x000cÆ0¬ßd?\x001b	¯F$<x\x0019´
sîsÐ$DOûiã|zo\x0007gh8ÃÀ~æðÓ\x0012Üñ4\x001b>Zç6pÚT£Ô*\x0002«#xâô¨ãÓ~j>ÖÏ§¦/çÔ2Ò\x0003Ê\x0008gö\x0010&æ\x000cRðCí´víÔ2Ò\x0003Ê\x0008Û*Ð«\x0000vô6t,}\x0003©\x001be¤\x0007ò²NLH£\x0000±\x001c«6v\x0003!¯\x001be¤\x0007\x0006w¥\x0015\x001còòe7í\x0016\x000fÝè"= þ¶³QFz@\x0019imø-0M\x0017Ê§ÓãÃ\x0004qn)Õ|ßKÊj\x000f­4¹\x0001ç´ä	\x0018ðä\x0010;ÃÔwF¿ýîà~×On°/¤H­ÙnáÅÅÃ6²±&ZzbÓ^S¤\x000eÜ\x000fÁ\x0016³[\x0008)]¥;æ½\x001dØØH[qB\x0017¥z¸YecíìÛå\x0012TuXP§l"øawñøü7\x001cÖ¶\x0000Ö£LV\x001a\x000e*ë9Þ\x0010Â&ÍIlow\x0017W7ßàÄ¶\x0005Ä±&ÃÄ!0±5¹\x0001&]\x0005:\x0008AMgÁ\x0010WA<e?kò\x001aû½ÎÎ\x0018­§qÓÀ¬h(^\x000cr®\x0012fY5Ìj\x0019ó°È(°.ñ\x00124Ödf=§Æ\x0006MÃl])í²Açi4:\x0018Ëqrð´¶c¶
³\x001dfÆÄts (g;	f¶s¾Á\x0000³kÝ0sPd×ÇÊ%
ÆÌ¹'à\x0001bß\x0010ûQâÃT	9FRvàm+\x001aÓÙÿ#Èª¹jô\x0002j\x0001ÙS¾ðü\x0000à\x001c;9\x0001§Õ¯fÖõüö>oîßßß-É6gÀ@\x0003oÜW\x0016¹LÇ)K­jóæüâüìhB´>ì mÝë´\x0007W;Í¯U8c+bø§<³\x0016Ëß'_zGp}ë\x0007q<É§Á\x001bV{ÞE.ðKçn\x001bÚPÓAZ8¼J¶lÊãÊ®¯å³ '#3\x0003¸õC[ÖÑc»k07o¯å\x000c./dÙ^=õt9ÂÛ\59x×þ×NT­ýñ7#Ô
ó#©\x000f\x0002xTÁätiì±P>Ì¤õ\x0015â)1¥&Æß\x000c\x0011\x001bESã¢\x0007½a·yÒ[\x000e,\x000fÛÓÈÔæë÷·ßw§¡:¥¹DÜz~ø\x0008\x001bí#§Nð×\x0017§¯\x0017'w\x001eê
tÅ .àu)NdZ¶z¦ï\x0000­®iõ(­)Q\x001b]j
¸¶$£ºÉ½\x0001\Sã\x0015Ëg\x0001_\x0014-W&Ù²»S6å\x0000®­qí(.hbJfr2âF'ÜE\x001fÂdúì\x0000®«qÝ(®UüØd}ä¤é+^Æn\x001bÀõ5®\x001fÅ\x0005c]p=U Ì ¨5\x0000æýoD\x001bjÚ°â,pª\x0013ø\x0016\x0014ã<Áê)ç¢\x001f·ÎqÌvÃ\x0018¯ç9â\x0011ë-}¤ÝÕ,\x0018¦ôð\x0000m«#Då¦\x0019Õ¹\x0008Ég½\x0001ÚFEÈQ\x001dáuêùåCk\x00169j2éÿüö¨òÀ£\x0012×Õ\x0014ÙY\x000b,Âá ðÛè\x0007Ù\x0008\9*q½¬Ï°\x001aÔÒ90¦Ô\x0002M6%\x0018àm$®\x001c\x0015¹\x001e[*Ò¹U.OO\x0004^gÙ¸	q­0¶©Z\x0005~Ø}ýøðqQ^®âÚ59æÔ"0Ø"¾\x0014Y½Ý}}u9;^¥T5¤êô¥\x001dSÅ\x0008ëÊÅ:Òâ!ç;\x0007CÃËTý\x000bC\x001a¹/XvÜ°AÈ°¯\x0003/«Z¼¦4Ý\x0018uÎí =WqÄý%ªªÐÖ¶\x001bÊc2\x0003¦å±c²µ2¤OZ\x000eéjH×¿NîÎaû¥´UZÍÉ#ý­\x0016Cú\x001aÒ|ëÒ\x0012\x001fM\x0008ÒpI¢?RB½üfûk{·íþà\\x000e"Óø±\XE\x0018Ãßqu\x0008¿ã¼JÕ! ÏpTðîõíÓÓ²¾P
<
4\x0012Aç\x000cvD\x000cb:\x0010g
ï^ã<\x0017ùJ:YâC?²\x000fÇMäDa
)\;9oøÄªYÀGðàJÃ´UOWO÷wï{:©h\x0019r"LÄP9§\x0011zrú\x0015frMª\x001bî¤òêúüìbQ\x0017\x0015B5z\.Áp6Ô\x0004FÆÜ\x0013Ó[Ã=´Q×iÜ4äf3tË¦ÀN}xfÚ¦ÎÏ§ªÑÌ9xsûÓÃíÃÇ\x00056¿(\x001e±ý?\x0011\x001d×;\x00189ù(Æ¼oN¿¼<½'dö°ôÊz\x0007\x000eÃúîñã¢j1g,§¿[©ÙÐEùÙ>véÑ\x0003'`½ºzw¼RÌ\x001e`Ù¦!P\x0017®Ö4¿==sTÍq!8!3æÞRÜïÈr/Ôìg1w\x0001Or
»0!ÛîìaGl/\x000ba,(LB\x000e}\x0014òZÁ@ ×
¼ÖI\x000bf»§\x001eL\x0007ÿÑû\x0017\x000f¶û`DOG#'N¨¢Ì(Í%áóé&\x0015GÓK?÷Û¹q\x0004\x001ajÐ0\x0008
\x0012\x0012\x0014\x00058±rú=\x001fãéb	Ô¶µb$Ù<ijÚõ½dks¦\x0016ön¬lN\x001c=\x0002!r\x000b.8£y|Xê\x0005ÈëHå$Ë£^O?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=YV÷jÀv~0G¦Âx\x0010«:RÙq®]\x00181`Â\x00050`\x0014-¨Ñq¨]@§\x001fÊv\x0005D	04ù\x0004$æäDã`»\x0000\x000f\x0003,\x001eÓ`zu×ôzV\x001eçB
,Þê2gc òÒìÇ7Û`&w±~0]ËL \x0004`jE§Ä\x0006#¶\x000b\x0005±À´Â\x0011S(Ú\x000fg7U\x0006	\x0019ÁÚ`L?\x0019TRÑ\zÔD	fWÖCî£d¤uÄ#Óõ=ÌëjÄD­¦[Y\x0013\x0007`IìÁ\x000e \x00184 Âþj^ÇÍ~{\x001dg)TøKd"\x0004ÐðÈ¬Ú`ýí]^iï¸@@1ÙÙºÔ¼ÝÒÎÆû\x0016sî\x001b{â\x001dÈ@XÝ>Ú¤f\x0003>]øô
>á<VQ¨
nOâøÉ5\x0003VÃ}\x0011\x0014]"A¶ªß
lI¹5ÑµµúhÓÂês´úÜðêûÃÿnoÿÞ\x001aºÜ`&¹¶/>Ý~¼¼»ZJò#]\x000fØ*ÈÚf,ÝR\x001dh-¼Ú\x0017¯_=?9?}"mêÝÃÏ7:áh\x000f÷nß8ÛWé~yóîòîòóbÎ\x0010\x0006ó8¼³¾Kn}:X4\x001aôµOÓ-óÅ×'ç'o_Eøð÷Ë ò3Ü\x0001êòîîòú®dv¼¹úù'$T¢
\x001e%5	½x)kÎ¢mó[NÎÏOÎÎKBÇÓß½xR<¥¢IpòÇæ y+ºjp ÊÌ¦jÇiÓ^\x0004VÃå\x0005ø0áTN\x0007Êp\x0016íF3Tiãp:/}Í¹m1Á9S¤\x0014àì0r90ÇVFÎì¢¢ÀiWÓ\Bó\x000e¾\x0016NCòEþ0ábíkgÞÆ\x0000W.ÁÚ®Ö\x001bÿþ÷³	«ºÆûúÑùÃÝåÍÑ«#+nê\x001eúæM*á5«ÄWÓ}\x001f\x0013w~hõ8:{~ò¢ü'\x000fÂX
G7L\x0000Y|ZZå\x0002úv\x0015ëªÑËòû§O¿º\x001fxAMDISöuú7á/éÀ¸Ú\x001e?Ú¢à\x001d¶uMîÉIóõõëW¯àï\x000eCQ`A¥w-Ä½ þXp.*T§Q«>ÿéÍhf[¦\x0017×7KD\x000eô¾1r\x0007%bRªþ¼3I:þ}öâ¤\x0008	­á\x0010A`ª{\x0011Zê)¯\x0018ªÖæg®\x0010Íæ·58\x0010\x001a°\x001c\x001ckkw\x0015c¨\x0017Q\x0010\x0014FÑÐñ`=\x0003­#\x000eÇÚÔ¢%ì\x0017\x0010Tm#p\x0000\x001fÇCò5\x0007'Ä:Y2b\x000ex0¡ÎU\x0013&çÓì'Ë\x001d+\x001e\x001e¬åKYì\x001aá<54\x001dK\x0019\x0012ã#'
MÏê\x0012\x000c4\x000eóµ¾'\x000e¬\x001dHUp¬½\x001e\x000c\x001dÿÒYT°ðð\x0008F\x0003Ôdðq)t3:RR\x0000	¨qcy:R\x0013æÒüî\x001e~ü»nNg?¿ût½|JÄHöØÖ
Ê\x0010\x0014¦Ého]{¬¿üúõÙòB1ïÜ;ÕDw\x0017Ë®&\x0016®HÐÂø@9\x0007Þiêú\x001f{\x001e_\x0007^ô5±¨\x001aòDó\x0008\x0015ÙeIû¨Ñçð\x000eª¬\x0010±ò\x0011üíÛ\x001f tn·?/.¾~JÖ/\x0008é1UP\x0005\x001d°\x0012#ý=\x001dõ²}}J _\x0017]¿÷\x001f.ï?ß]Õ?Ð[ØýÕO>5ad\x0000x¸»ÉõJk9ÒEÎ&¿zp)l*dl²\x0001áí9ø]\x0010%fÜ\x0001ûCå \x0002V%¤
ÍM¢hö7òàº0´:\x0006\x000b\x000cJ}CgP*Pj]A&\x0006F]»0Áêm+ _H	\x0003çÚáÖN	9Y]\x0014\x0010\x001a·"ín|Ô
OH¼e¹\x0016\x0003ã\x001f}\x0018\x0001\x001f-Å8\x0003æwYi\x001b\x0005\x0019&\x0005&àuQ@ãm\\x0019\x001a·\x0004)5ah½zbî]ß`HÌ\x0005±_&\x0016§°«\x00110å®\x0007AÜ2+#$7NÅI\x0012tVÊµkò¹ú BQ±ÙÑF\x0006ò S5o(À3Ç³w÷\x0017­P\x0019\x001c2Ï/ï>,e]d=Jk±¾Ac)jT
¢mO¥¨p¸<?9ÿf9ó¢©\x0016LqÀàMÉa<Là|A~\x0003\x0005ÄbsÕ^\x0001¦[0Í\x0001³ò\x0018³\x0003á\x001c\x001bh¨HOJmIÈ
.Ór\x0019\x000e\x000c\x0010ÎÌ\Ú\x0016ç.M$åïCvë\x0008m¹l?±À´v\x0018§<>x{,JÁ\x0000s-ãZd¨È+*\x0011iÀüÔ
Ë·\Ãå\x001dÕhpQ%#R²Ú$és\x0005XhÁ\x0002k&%åOç\x00122`U¾ÃÌèf1°b\x0015Y\x000bßÐ\x001b/<÷¢é £\x0005fÃcM~0)&¶U0mXCR	ª67J¨\x0011²©ÕgýdR\x0015}\x001dIUK[7å
lbö%ËîV,-2ERòi#Ð£\x0011aMì¾d\x0019þ@%ÀÐ\x000e\x0014+Ø\x0012\x0019\x0015\x0003Y©G,¬X~É2ýicF|¶¨7@O{M«Kõ
²í\x000cãî ª&\x001f)KjqY\x0006\x000b\x000b(g4u\x0018d\x0013ã/\x0019Ö?¶"2U^fÒÞ\x000côàf\x0019Ú\x0013ó/\x0019ö?Ù³X\x001f´¤'8e]%QqbMì¿d\x001c\x0000\x0001\x001cgMVÇ\x000egBü°\x0003ÖÙä\x00083ÀçÞQ\x0019\x00025¨$££1ó#djr\x0006(Ö\x0019\x0000Ñì2dÎbl=y\x0014s3mwÏ\x0015`#@ñ\x0000G	H@FFCÕÃ)6ÁÛ\x0015dSÏ{\x0004hz
7X3\x000c-\x0010NWM\x0000Å:\x0002¢ÄR_mPÄ \x0019ÚZ`-ýó¯&Gâ\x001d\x0001»ì\x001eèjýÒ	0bÍÔä\x0004P¬\x0013 §%Þy\x0013\x0018\x0015ºY;dÍÔÄÎ*\x0005w\x0016m\x0006ôyÇeVýFëÎ&=±\x0019ç7B\´2èâKù\x000ck\x0004kb14ËbHE\x0015âiù¼ 2¡ÊbÌHÓöùÉ"ó¬E&LJÅÑQiJ~²Ú2?½Ê±îrÉÿ1®\x0016\x001e$\x001eéH;-ËÙ\x0017\x0017¢\x0013ªÈ¢²õ\x001c7e{\x0016¬Ú¼bN#·\x000fKNMäØ¢ä_õlh°èaÜÆ'oKOQ)3='
/Dfè=ÚHvBUwL?y!y\x001a+N±X×^íPOC§9Tûñ1«ÔÚ¥¥l{(ëA¤½%Ye©à{®¥@÷VTnJæxÞkÕæ\x0005\x0002QnçðÜ,ß;XG@¯CÝÅ:fòIÃúä\éÊ\x000f¬ïôn.ñº+va³\x001ejêè\x0004§cªü\x0004¤\x000c×\x001fÉ;ôO{âÒ{g6ïÐv2p¡\x0011¯ ZR§¢dì\x0007\x001c\x001d=µ`gÁb©\x0018p-ÐÕ·U"ÊM©§VL³¬\x0018\x0008íb\x001f\x0014*a\x001f%]Ec2¨òä		ü9\x0013¡µ±]a2\x0014\x0002K\x0017£ÝÖ0}Ò±¥ûñþ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9Y??=ÿû\x0004¾TvTÃ§\x000cºOb\x0012_âÓT}"XÔ\x0002|\x0001S\x000bm\x0005Hí=\x0013\x001f\x0016\x001eËÌ'4Ï_ØKJªáK=½ÒGù\x000f¬ð®ÎúöÀ\x000fLRP)¹\x001eð¼U:õ»Ä´\x0017üOÃw¶yüc,éÑQK¡èuÄ:)IQË¢iÑCv¶¾øÏq¨­je\x0001\x0015ö«ä
\x001dôbÑ¢#SíÇ\x0007K±¢Ë\x0012,')5zn)r\x0015Ü¥Âîùz
©¶í	¦SiTP§\x001a¶íz\x0014®\u2ó°\x000cFïÓG\x0001Vð¦	Ã[ª>\x0003v}Ïá{¹WN_åÈ\x0015bym\x000fRSx\x00175g\x0015`¨\x001eöMèB,Tx{>J°DÈ:\x000f\x0005\x000fiÆ\x0012$Àe»ò2,KxÓg\x0001\x000eTÝ%Æ\x0017Gþ\x0015\x001b	áè÷¤\x001c
±M½©lÑNÔ:Ë\x0010Ë`OØ\x001c wü#Ûuî\x0014b¥7Jþ,ÀÂ¤b3j`×a
`Îº ¼?\x0007vò<¬$§?\x000b°àÌÊ\x0000R`/ÔÒÙ{=´û(ä²éõ>K¸áÞ\x000fpLNõ|\x000e\x000bª¸~¿\x0002+ú\x0012y´wÒÇ»Û«ÍêÅí/7×\x0015\x000cì¬O{±ZÁÜ¸\x0017Ûvy.\x0006pa\x0017íÝéÑzõâôõëÃãuú7òmk¬¿S>ü§¤ïO|ýøÅÿ<\x0000Xí±'1}\x000b+ðùõåÍÏ#yèÝ\x0016,Ùì²`\x0014\x0017\x001b9,\x0012\x001eOa)>?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=-m¸¡æm¸ÍnÞ	<5#h¥ýdÏ\x001alUc«m°x\x00014ìC¼'bçîø\x0003ô0·®¹õ6Ü s)\x0001}qmIÜì'Éhá5Ô¦¦6\x001bI[æQÃy´"jÉÔfÒ\x0001¼\x0006ÛÖØv#aü¨ØgÐ\x0006Áax00.nWs»ÄM«+óè\æ\x0016ÅÍ)Ø`'C
×pûÛoÃ-é\x0005\x0006=·Ô/åÍ3Óã2ÔÜa³sÂÇÛ¼\x000f/\x0013vä\x0019>'Õte´9b\x001bpl­
e¤L\x000ewìÒã õaðÖXnd-e(\x0012we¸P(ñrðÚ\x000e7ÖRnc.E\x0010X¸Àc´O¸\x001e
\x000b\\x000eKÙK¹½Ä5ö|RÒâæ\x0004îË4§\~>\x0006ÞØK¹Á\x0014\x001er¿#siw<\x001e¡M\x001a·=²1r#)4ÂäXk£Ä\x0005Q\x0012fØ!ÑÛXÍ\x0018Ì±J\x0011÷\x001f(JhàÀ75\x000cÞXM¹Ù\x0014"ïÀAððÂ°2,Õ`ü7VSnc6E^|çX)cå¡\x0008|:/}
xc6å6v3\x0006\x0000Iáº$3¶\x0018¶Ð\x0018\x001fØÆø\x0008\x001cóïÊ\x0001gy\x001b¿Ýù6RÛÈö8ÈK\x0001q&,Ö^L0Ì-Ú1]):®+\x0002M]FóDoÈ9ÔeØþt2çªm¯7Ã£3ÚRÇ¾-\x00179\x0006Ø\x0000\x001f¦ø°ô=úµIús!\x0005@ô²A¼,ËæËrxêÍ\x0003ø©ÅÕ¬Î%¦&þ#WùøÜø3*ý	>l/Õ.ÉÛ\x0006J@ÇÞã\x0001üé_n÷>\x0000ým\x001f\x0011^Ë.\x0014kP\x0006\x0007iGÔ½&æ\IÌ=ýåïÿ÷\x0008ÝËlpS®¯Rô4\x0006ÚHÚÏeånNÎ~8}\x001f\x0007\x001a\x0018¶\x00006¬%¥7¸51\x0001[Þå\x0016\x0005>£ä;U
¬6\x0000ÆR\x0007òÏ±|(\x0007\x00168?%ìgE\x0007°®õ\x0006À8\x0018\x0014y\x0008ø¶¬ò¤u~\x000c\x0011s¡g\x0007°©Í\x0016\x0012Ö¹Ý\x0003%¬xAq¡FhFyt\x0000»\x001aØ\x0003\x0007¥9í=4ä\x0016ZN)Ç`YÍ(ë%À
&ZBÕÅß?¥í>­u\x0019=\x0013ªt¥ñ\x0008iÖe \x00015Æi=ÞïoÒÏ7oN9Pesñ\x0000/¾ä¸üãÄÛ'\x0007ò·0È«j^5.ßÀ#\x0002N§¡RGÁ|§û	{yuÍ«Çå«v©Æ Lñ>ÅºÃîk\x001e^Sóq^pE¾ñ¾g­y\x000f µ3i\x000f®«qÝ\x0006¸æ\x0005Ê+´ÜÃm\x0018;½¾Æõã¸Fä±òXljxü¥\x0001~´Zî\x001b¸\x001eÞPó
x5w0º\xU9½àn[½&\x0010J"{\x0004ØbI,@¦\°ái[\x00118ì»<=À­¹\x0018·\x0017^;^hé¬çÕ7\x0006$ë_éN°lìÜÀ`Äsà¨õÀ\x0015sÉ\x00198\x000ci\x0008Ù\x0018\x000c9n1pÈ\x001dí»sÊÓlÉ#q¹WBì{\x0010=ÀÅã&\x0003ý\x0006p\x000c¯iI-S\x001fLØ\x0016èáµ
¯\x001dçÕ&\x0007¤×\x0018NN[¶ÈvP¼	ßé\x0010s"cä\x001c\x0007Á%,ÎxÞ¹k¡Á\x0015cb[nÂ\x001dCOÚ,¾&\x001ce9\x0015z?
í1!ûÜ[`;ë¸'\x0015ÃRAZòào'ÕJq\x000b?ñã£ÑÞEû/?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ª$QÓ\x0013L3Éâ\x001cX1ü\x0008RÁmªA±e\Ë\x0014HQ¹\x0019ë}\x0002[<\x001d~\x0002
Û\x00059=\x000eEòåLxw¶\x001e0»\x001eÕVã_B\x001cnB_\x0002\x0006(f¦^	Pz¡ø\x001aÌø×\x0000*#¸\x00024
$ÍW6²VpÜ÷\x000cº|\x0006½¼ã¹WGgI}¾þ}ØÒºf£_Âf¯sð£<yuµysqßÙþ¯Í´\x0016b\x001f;\x0006YÖG¨¨½¿:>xvøúusû\x0017âË9¾\x001cÆ7\x0017Û$"ªY«W¾¢eÖù\x0000vþ\x0000vø\x0001&¹ð\x0000ìo2ÿvÇ \x0017ü|ü\x0001r©k8Æ¡ý4}\x0003Y¿¤¢\x0014Ô÷\x0000³öGXAjø\x0001Ü¾Â%$$Eï6R\x001dþ5;{x\x0013;ÿ\x0006àöêaC\x0000ÿßÿñï®.ïãwË\x0005Å
\x000fb;ì\x0012\x000b\x0015q!rß;|~|töÕC58\x0006XÁ`
©±}\x0013+Ê\x000côÂÞÜr\x000b¯,xå\x0008¯2û4jBäI¿J.iÝÌp\x001fç¡\x0012«)XÍ\x0008«µ¤\x0000\x001eV,6Ú;¥\x001c©\x001e-ÕÆ/±ÊÂ®rÈ®á á$5çÉÿ²\x0013l4\x0017\x001aÖ,^29ô\x00197©¡iLÆTyªÚ÷l;\x001bß\x0002½AzÈ¶.\x000b\x0018À(¼´h-
\x0016a¿\x001bÇfU×ðJ=gP'c¬Ï\x0013íÐ\\x0003î¬s6àfi¾-!7óÿ£F)«_dÅënÆ-V®\x001eZ¹©3Ñ	H¦Õ@Ò©n©\x0007©\x0001wV\x000euE~pÃEZIÓ£]\x00167~I²Ö\x0015[®\x001bÚr51\x0012KTv0y.í
KÝ-´mÝm!Ò%ãúl\Ò«Vl©Ð¿Ë/C\x0013S\x000eÿ¾««\x000b¼xusq{ÙÞÎ\x001d\x001dháð¢\x0016*M½
Ô\x0012·ñ\x001e\x001c\x001f\x001f\x001eâ½Ä«×§Gµ±NÈ®çìz\x001d\x0005At\x000el5§r-%*\x001a\x0001=ð®*À8Ä\x0000½
®CË+·OóMÖ3áº\x001ez],\x001b=¶n\x0002ç>Þg%2EB«ªv¸
¹ÇR\x0006.J\x0019L÷qßß\ß_\¯\x0003Ë&UVJGÎHÚPXMõcºûþäåëÃõçX¼5o\x0017áÚE^¿¿Ù¼iã\x000eq\x0007ä¢"¸áÌáck<UÊy_\x0019ê>U;¿þáäàÙ"õì\x001aÑsºFì¢\x0016
3hZ ÜPôïÚÕï:VQÏ¼ç@Þs\x001fuìÒ\x0002jæÅ>BS[E\x0008\x0003ZÊâ|².\x000fÆÙøZ>ß´Þ2+&D°²¹£¡î6\x001e9\x0011Ã
5ÆÆòùÁií´q;	\x000c\x0005o\x0004\x0004æÜ«k\x0012%{°ÔÇm©&Ñæ^NQé:£ÿõ~|\x000b¾(ðÅ0¾¢y"l/87XØ\®Å+\x001e}üªàW£üb/¬÷Kü¹ÈW:T»øea9le\x0000@.\x0008×#¹ ±amæç,¾¶Sq\x000b\x000c\x000cá%þÍå³T:;®ÅT0û+Uçsö\x0017\x0007G\x000bGi¼m\x000eþG\x001a;=/nY³åp®q¿á8ß1ü\x0013\x0014°Çùá-E-õýã(¿Áuað\x0017ÛûÖ«L«*-t°\x0018g÷M´v\x0008Ñ\x0004
\x0003µÙÙÜ/\x000eN_\x001f\x001e×lí\x001f\x001d£!¬\x001f£s5©u\x000f Cp¬p8%Xë/½'~&×©-=
g):s~MÔ>Ê7:\x0017w{/.?ÜÜmZçkzãò}²ä\x0014¬È¹û|sx¶÷âèÅÉÙAm8hd
ðpi?\x0004¯2<óð	çªÅ°ü*zæ]\ú³¦?÷¤$;Þü~syÛ¶CfåÊàÖPÚjiÜ"®ã\x001fON\x0017±¹cs7À\x001dW\x001aý\x0003N$ZÜ©\R\<¼Û¹G®s)\x0017¿ùðqT\x0001NS\x0015ó\x001cnB\x0002\x001ci;^Ó=xñj½{t§\x000f	`»g	+víz\x001e\x0017T|ìg:YKr¬\x0011EÆî)LÅÝ«ûËût\x0017uyÑº©9NZ[pÌ*ëM\x0000%\x001aÛ~\x0002\x001c¾>zn¡\x000eOËDs\x0002åSák\x0004?÷¢\x0006_X
G\x0003*P+¾Aú×ìWnZCÈ3¿©ÿïÿøÏû»»ÖÀ)\x001c£Òì\x00101MHÕÆP\x0015­
½Ê[ãÞÁùëó³³jð$\x001e9\x0005°Å\x00073ÿãö\x001e]ëëö\x0016\x0017¸wJ\x001bºa¹¸@ä¬Öôø?N_£\x000bóòåá7·»ûà@Ñ_<\x0006Vs`Õ\x000b¬ræ\x000b&%ªT\x0012\\x0017<´ª\x0014®\x0004Ös`Ý\x000b\x001cr*°44ÄDÔ§í+#\x0017JÞôÂý\x0005Ö¦\x0013gZ\x000eáûäWS¹ðÓÙý\x001er6\x001fú0ð\x001eo|@^\x0015%<\x001diøÈÚ#L^:ævá¯Ï^ïáß·ýKà\Å¤ô¬[=áés9»ßÜ_ÞÄ^Ý·÷]ë\x0017\x0003
Û ñ.\x0015\x00168²lx¬Â?{}ðúè$þôê$¼ÉÏ·¯­MðÂ·÷\x0000²	Pú{qwùöâ:|cÏÞo®.îïf!ÉÕ\x0016|mrs`NBfµ\x0007'!Õê\x0014îáÙÑw/Ã÷õìãÃ×g³ ¥öÂä\x0012ó\x0012;}(\x000eÞ3Ó\x001fJÕ[\x0017\x001eê«oU~"9"ù/ò5©ùC©2ó2ÿ"\x000feç\x000feÿE\x001eÊÍ\x001fÊý<?ÿ×x¨çN\x0014û\x0017yªòèý\x00179{yqöòÝ\x001e¾ÿÿ=Uqþò\x0003\x0017\x00070ÿ\x00179¹.Jÿ½êgæxá¨?~½°Y\x001c_ìýxyu\x0015\x0002¾hÊry
­\x000c5Ú[¥¨$P\x000f÷~<:>\x000eñEc\x0010E\x000faÌü!`ÀÐøS(¬\CG_*´å4\x001cWT
m·>ÆW]q|\x0006ÎË/ïâ«\x0010\x001aDè©\x0007jí¬T9'¼ë§åSÈ\x001d<EÃ!&ßTM\x0003Ó\x0008ñ»ØÙW\x0001àÅ\x001e\x0015Âùc=¯74àpe%Í!\x0014¹C\©Ê\x0005ò_.Ó¦.~>"w\x0005ù_tÖk2HRæyY*'ä­jBàÅÍ¥Úrs¹Ü*RoLÓ\x0008=+¯Ô\x0016®C\x0017¼@\x001f\x0007\x000bÃ4«æ&\x001b\x0018K«ÅU\x000fWÏÄ§ü/êSkÉÚÇKcírÙP.§.+\x0019íuèr6¶= Ç!xcèÆo\x001a;\x0015Â«©rxWVÑÔst;.\x001cËÞ\x0003dèÑê.\«$Ö¢Û\x0012ý±tÖjt¥XÚhª¨\x0015\x001aa
\è\x000eÿÌ\x0014¤eÖMx
µ÷ðãôûÅÞÓ«Íuó\x0015\x00084[ \x001a
ÛK:Î³(éöèàüÇÃ½§Ç\x0007/Í/ØOæá}ú\x0015=±xÍñ°¹½¿¼¸ÕkÐ\x0016Ã2Û»Ûÿõôö"^ßDEI\x000e*°m0n$Ç:u\x000e>\x0000Y\x0018þ:Oö>?<ý_Oë\x0008\x00171ÿ8?8}}txºP®Q }_üMPÃ7-ÿ&¨aù¨¿	jð,ô·úñß~÷ïf¯ÕMÎßn®ß]Ü\7Zcð}\x0019\x001c\x0002]7iñfÈxëä6Ò\x0017\x00071\x0012{~zðòùáÉË\x0016ÐôR}« úòý\x0017ñ\x001bïé	üy\x0001ÕÙ\x0017Ùúq5\x0014j£\x0000:\x00162à2oÒak<ÓÛa¡4ûðq{óáÃCøOãÿ>æåPæ\x0011?Fy N\x0001õp\x000c\x0002q)f>N¬X\x000f\x0011\x001bºXÖO$v©\x0017\x0008\x000badq\x001a?\x0006HEÎqT94ÕÃ¾\x0010ÓI	\x0015ª\x0012ÃÈ\x0010dÄ\x0001äð²©´¡Ó#U/\x0005+'oÝ8ïÕ.²bÚø1,tjN\x0001drªì\x0004â].\x000b!
\x0000!à\x0014\x0006%`M»\x0005OÊ°\x0000\W
\x0013+0±\x001a41ÞìH,Y\x0007\x0016,ëØyëw°[8öÇµùð5Ç1°|¸¹~Û\x0008«2\x0018RKX\x001aé­¸\x0019Û\x0006\x000fãð\x0000þÝöÓxÆúÈs\Ç
Û0\x0014\x000b\x0006Vë%ê2¯$®\x0005ÅÌ¶µÐ\x0005ûÈËYiØ°X¡u4Àª\x0010S\x001a4¬æø¦1]\x000bôÁÞñwN;¨L\x0006íôyzóp%^×oCtÓÆ+5tbê^¬Õ¤í÷Ñ\x0018»9ïéÉùëXÜõò»\x0010àl[±Û;ûñ«+öêbïUÃbî2©\x0002Í!\x001fw]\x0001ãwc¶	qÊ¨ÁPÛ6±É<Ü{\x0015¢±­%º\x0005îãpç[Ä½ÿS~¹ß\x0014\x001eï?ÇÞ¹ÅÊ¬M\x001dh ê£1×\x0017<\x0007ß}©ÖZúÿ<zºµY®à"\x0007÷àúãáJýªfö:^½Ëó}Ð¸Å\x0001Cá\ÒÉ'tVmõVf{{\x0003]²Ú·JbÖÕt&Î\x0003HÞ)ÇÙ!°¼Ó­!@\x0003Þû?äï\x0017úk\x001bMØ\x001a¿ø³1NµÆ\x001aOÜÀµCÔð
+<muïmØ\x0019<üçvÔK¦þ¼þeKúçûÍÏ·\x001eÚp-ÌH¥®!\x0006\x000c1JªÄ!\áÉ¦\x000e\x001a'Ãêï\x000f\x001eýã¼	ù¯i o\x0013ùÁ]øxûSXU,8vé\x0013OÉTdysÙF¬8Ç\x0011a/7±î\x001f8¥H#4ÁË3ÛÖ\x0004\x001e©¢òähÛ)9c\x0015Uô³º8R!¡jDgÔmïØzT\x0015QU7*ô·
d50P1²*Yí¶ÐÈzûþËÕç7_{ÑÎ.no/>^\x0004¿îºíP2ÆàÀ k¿/UJ`yé\x0000ÎìâÆpvxzzøê0øv/·Q3èG¯Ú7\x000c-?ë?\x0007ëÆM7¼û±	\x00086]/\x0018å-$O«Ö8½Í\x0007.ÉÊN;ÃÊ'ê7µy/nõíÌZOo\x001fZOQ.õá­ñÐ9\x0018OQ.x
ÝÂ_ÉbhÊ\x001cëééyå\x0000A%[}KPÁö>×pY®á\x0003uû2e¸KQyà²lÛ\x0016Sçºp×¿¼ýmö
>¿½ü°yxÛöZÂ;¡â\x0011h\x001dCOHø\x000c/;mçTÏO^\x001c×Âî@¾\x0011®O\x001f½×[ü\x0010W]6~£F}üB¹T¨²\x000c\x001a\x001fé\x000b
¥]¯A¦ä8ü
Û¿]{ýó§Åûy]S
\x000e\x000eÌ5ÐÉ\x000b÷00%\x0019Q\x000bÌh\x0006'|û»pXi*¸è\x0015ý&¸Ì»?U§oÞonÛV
Kuù\x0014îÁ\x000cèôF§*Å{\lÍA\x001c=ûáàtû²%}+`ïåo7ÌÏKè[¾¹¿¿hÌ/xh¡Uéd×\x001cç$³SªßÛ­Á\x0014´*¼~}¸=¯ðð»¹ÿC|=ks·÷,:Y?ÚPµõi>	\x0014\x0010\x0008\x0018ð\x0019Ý|\x0014\x0003	\x001eßVïy	9Û{vòâÅùËóÛJýç¯«Wó×\x0016ïù\x001b¾kn|¨ûI\x001b\x001b\x000b[¿ëtÁß\x0000ïì7\x0000uyýñáûr[åt\x0002ä¹À1Px¬²Ôþg¬×ÛÚüzqg\x0001ò°ëÀâÑ`×æçÜ¦
0\x0010\x001c´-®NÆ~û}ú<ßãn\x001e~ÿ¯ÿÛWð2îp5ÇÒ^bdª"1oz)°¹\x0004NúEìs§:u©KÇ÷}!cíbÊ\\x001aKó´êsÎ)oùõ°\x000ciN\x0004\x0002Ç9\x0011}ÄBPW%bãÓM¸ñQÔ»ý"|-±(E7±aI>\x0019l¡E Æ\x0001x[ªn%²/ìû,èÚ3 £¦Pð\x001aP8 +µ£uáK+û~+sÔ\x001b\x0001ÙnYrtÊÈÛuÈ=z÷ú­Ìý>ÇÏ\x0008\x00109OVÎ+ïf)G»Eÿv!\x0004Ç2\x0014\x0001\x0012\x0016SV7\x0010s¾mÏ]I¬Jb5@¬`Døwr²"ìðå³Î"ä§i¾xúÅãùâÏÞtÇÝýýß\x001b7Ãlh£DÑõ\x0010dcÅ+u
¾Æ\x001d;F^¼:<{}øã5{L-Jj1Fí\x0018Áâ\x001a\x0006§¥äôL\x0013µÚæ/¬ÂV¥±Õ ±\x001dÓä¶2¨F lôþ\x0003öÖª5Ø4\x0008±ã\x0004¢!ìp²°Tµ\x0004ã/yòÂâFk?´\x0003lÍ
kk6fm\x0013^EL\x0006º\x0010N$âÁ_Ã»+\x0013\]`ÂÚ1ä\x001dÂ6.´6ç(rÎ­¦EbìN^IÃ\x000blÃ\x0007±9\x0008r\x001bÄV(yÅÀK®àîº|#Íà\x001bi¸Qû
\x001d¶?Ì2:T7\x0006c«¥}»	»\#ft\x0004BJÂ§ÛHm#c«mAÜ:j[RÛQjG·µP»\x0006ðqçò\x00121»x\x001fÏ[PûA[\x0007Ï¶\x0011®lÊqqç¥ÍídaûÒÖ~ÐÖ\x0002JpakN{¶g¨ågÝBíXakøq:ÄÉUe"l"1¯cEÔKØf1iÂÖÅ.âôà."aìlZØBJ<×\x0005S¬ív±8W\x001aÛ
\x001a[ÂÀ¬äDpæØ½eÚpNn½ZmKìÁ
BºxÐÀÈvL×[nÚ-3-Ô¾<hüèA\x00033\x0006±\6\x0019´D8÷hlëw²x%Jì1GÛ@\x0003$\x0019[\x0010Ò$lÁ\x000c­ì­ÖuØªÄV£Ø\x001a¤+é\x0014hmßG¹mÏÒc1<`bt\x000475NÓ£æ20ï#lk\x0019ø:nñ{txO\x001b\x0002\x0004¼äãÊSÀø\x000ev\x0012\x000eºþ\x0005·\x001b´·	Ýäüi}\x00057´L`\x0012å\x000e°y\x0014EAl\x001dè Â\x0016Ê
\x00056B\x0000zäF\x000cF¿\x0002$qÕÌ\x0019\x0008àHå²u×ª·\x001e«\x001eÂæÞHxÝ·z#¹,~±-;\x00125+5ëE6>,i^E\x000fS§ðÞ\x001aõ\x0008\x0003r9sl\x0000YÈº\x001fY³4q*î§´{8CÝEo-\x0014_lKdÛ\x001c\x001cjã\x0010ã¤,°.W±­!z+2QÞyZËá\x0017O¼.¦®ºÊ\x000e]¬ÂV¨·j|Ø3¨
ñmÈ³!£\x000bÙÉÈÌeÁ\x000c?vC\x000b«Yh-÷
ÞfxU\x0018\x001eÆÝ@æ\x0003\x0016&Î4Ð\x0016KGàBÃK*æÛÚH°\x0012Z\x0002Z\x0001hiÑó\x0008Ðô£«®°émsÖBë\x0012Z\x000f@3¹ÐÆ§\x0003\x0005.5°¦)vuíÙÌ¶9à\x0013³M=<YÌJ=ßC&ùOÀmúÅrn¯\x001b3\x0002};á@Il¸HöT7&\x0017+~S\x0001Ù\x0002¬ÃÚNXíi\x0003X\x001eÜØ\ä&·­U°²°¬ì5mxçAZ*\x0003­Lg5ÐnõãVÑêr\x001dôÒr}ÖÂµx¤å)¿\x000b´~±ºÖ\x0015´®V9JÂô(º²`8"4Ðº,[^¾cõâBCG\\x0001\x0003_"njµ\x0000ZÝàh6ÐÚ¶ó5SÚP\x0001ÔIbIq\x0017:åÚhyi[Þk[-°±/.$f\x0016hS®\x001ch·æÊWá\x0012Wôâ*dÊ¥ Ïk¡Á_Æ-÷0Þ»Å\x001e\x0016q-ârå2î.^4á\x000b\á;qUÐÉ\x0014pe\x0014Qì<\x0004äDë[\x001c÷EZY®\x0005Ù»\x0016`h§mÁC\x0005f¼·y_ð;Ù\x0017¤°%nç¾ B`î\x0002®¥JLk\x000c½i¾%ø\Æ5¥uM¯uaÆÌ'Z\x001aõÈ¬Ì\x000bw\x0017¬¶dµ¬Ü+ªò£F:³\x000cÝF8}wáÙÈò5½¯\x0019·>Ö}úV
\x0013\x0001×ìÂµQå\x0011¡z\x0008¸Nu¥F\x0001\x0017+\x0005\x0000Wìb1(Á\x000b\Á;q5Î\x0002\:\x0019Ì©É½\x001c»pÅT¹©Þ]C\x0007\x000fà\x0010ò¤	AÌhFk×ìäUSªÄU½¸gG×pLÂ3C=\x0001w«âÆ*ÜrgPÝ;\x0003\x0013015â&O\x0007pa\x0016\x0013âê­­Îkpõ£h²×Ó
û+ÕÈy2\x000b\x0001W\x000b
#ÔNG]º7º×½aÀÖ\x0006\x000b-æù\x0004Vb\x0017îåÚ\x0003.üØ«ôx7*`^QÊ¥BA4ârØ#qÃS?òu;ß5\x00052IóH =y\x000c&ìi\x0014¦1î\x0006µÔó2»ñ\x0012*\x0016OSòVê\x0018f {J\x0015ÿ\x0002ã`åYÖÇµVOà\x001cNÊ&\x000bÜºàÖ\x0003ÜÚ;\x0010\x001d~°c`û\x001f×Ô¨`ó{ÍÔª°¶\x001a²6cÌR\x001bC,²H9\x0012¼	Ü[++:¸\x000bk«\x0011k°°An\x000bÇ_Z%Ê"·ÝZê´Û\x0014Üf;\x0018\x0019±\x0015ß\x0002ssÄöz1¥Úmeb\x0010Ñ#\x0002ni¡½$r«\x0014y\x0000÷Ö«Å\x0015Ü\º\x001bºzí#1Ó/nï[KË,5°\x0010Öã\x0014<î\x001cÖñ\x0004@ÂéÉÓÃÓ×KÜ®àvCÜ\x000eÇm\x0002·§¬°ó\x001a/Ààß\x00117g¬à?÷[¡b÷\x0011hnp\x00069B\x0015UM°T+¼[5´Vã@âÏ\x0004\x0003\x000béûëû¯6oÞ_4
ÂÝ\x0000
)q¸®Q1^L+¼(5vÙ1ýþäåë§Ç\x0007Ï~8<]\x0017³ý\x0000\x001fe÷\x0006à\x0005sû©òC\x001cÃ\x0006>D~kÇm\x000fº-ì.ìÝ!\x000bÔ/Ý]ê±R(oÉî[k;à¥+ì.Ý Ý=ÅÁE\x0002å\x0000/IT²RrÛÁnxÁ\x000e?\x001a\x001e×\x000c\x0012\x001eÁð$¤Üò»Ú\x0004ï\x0001^ÍB\x0006\x0018Y\x000c G{ÓØæ«ep½Ñæ\x000eTrRb)lðx*¬XÏAöäüß\x0016g\x0005¡¬Y7²!½,\x000eBx6Å9Î°pËqN#rieÝoeå °/!»}ÌäZfxkGÛZb[\x0012ÛnbM­P=Ni&\x0019Ç@¼µQ}-±/}?±À¾ÿ@l w)\x0011kZ\x0016~kÜJdÃ\x000bdÃûéæ/ {J=Bí$!oí±Z,KdÙlÐ
.Ä=¼|L\x0013òn\x0016\x0006çå\x0016Çyÿ\x001e§9N\x0016\x000e1*´rXj|§¶]½UOi%³~ÄÜ¿cèàxPÔ°ß%fK
v¹Ò¬Y«Y«~f¯AU & \x0002¾B9¡êÝ^\x0001Õì\x001eE\x00070Oýqt°BÞÞ{\x0010{J
Áç3éæÝÓåpÌi,û×QÝ¾
Ìy\x0001Ìy714ÁJ\x0014äg\x001cn¶#±Á:\x000chãhQ_k@V%²êGÖ\x000eëÛaR=ªX\x000b'ñÛ\x0016YlJdÓìH\x0015kGZDpw%!/Wd´!Ï*H\x0000¹(!Y,Lcq\x0000Ù§v5ÁÍFÞ\x0005/\x0005ï\x0007\x000eá&\x001b3\x0014¹\x0013c÷¾Ió°\x0001YÈª\x001fÙà\x0003äàx¦tj\x0010MF\x0016»±òüN> wò«¡·?E%Zç\x0010\x0019
$ÞUùê©þWOcv,\x0010\x0007\x001b[¤b7p;ÚÞt¹uÿ:ÖÁG\x001fNA\x001a2-
Å\x0019.
gô0\x001bË\x001dY÷ïÈ^Ç$
æN6\x000e1$¦Z®k#.Wî_\x0015[Ê).Ñ\x001b
o2	;ÕÃkA.×é^\x0017;«\x0008FØc.B° ³wlKdÛ,sÒNÁS'¢ç¼µ7j\x001d²)ý!Óï\x000fà\¤\x000bð(K¬1EÊQ¥ÂÃ\x0018ÓÝ ËÂÊFö[\x0019\x0006îá\x0000 \x0010A¥ÐÊeä­Ò+­ÈáHú©lnPæQÙÜ*ym#\x0018ÍG\x0008ë\x001a½NPaÁn(a­õ°ªÈ3q)@.Dë\x0014ÁÙOÄ:8ù©\x0012Æ\x001a\x00121[Nâ6\x0011\x000bV\x0018Y°n#[-cé	 +Õ\x0006B[­r|¹8±Ä¼8`¢Ò.Ô{T]7Ô·ÏcåÅ.U±,ê_\x0016pÁÄ\x000c\x000eÁHLW´.\x001cá\x001e\\x001b±-lûß=êKÄLà-§ÐLbS3çËU mÄ¾$öýÄNÆB	\x0014ÍKi|¡²0Bðñ\x0017³ZMÈR\x0014Ë\x0002~ìE¶>f;\x0001ÙrLÄAy\x000fMÖñË©6äÒÊrÀÊ>ÎØH3kx\x001eyÀP\x0018Ö1±µI-²-í\x00082K\x0002Ò\x001b\x0014Æ\x000cÈ<#ïèíSå¦¬ú7e\x0003uâHÌ°À=,eúF-5?Ä¶$\x001e02\x0019"@\x000e\x0006G'Îë¼\x001cóµ!o\x001ayû°ØÇ©Ìk5½z|kR3/Ô	\x0005#Û\x000boèøæÃÏ­\x0002ÃÆ\x001b]\x000f\x001cfáúäÀ9Oú!Xö9O^<\x0005¥á*ñüØ\x000bÄå±·\x0006Ùr#¡¹3"\x000f/´5
½C\x001ej9qÑB¬|A\x000c?v\x0012GÝtc\x0014µH\x0005²N(¢»U\x0010m\x001d²\x0011Å²0¢w]XÍ\x0014ÝKP&{êkÑ
Õ\x001aMÄ²0²ÝFÖ,¶Qz(\x000fKm\x001dÕ~ûx×uÈÎ\x0014ÈÎt#\x001bhHëBZFµ\x00196î@i|êÖê©µÈºDî^\x0017PèÊptÅ©a[IÄ
uSMÄ¶4²í72Ä{hd\x0013»#"²P\x0019¹!DmAöåì»7ekÂb@ÑmÉ\x001cÞþÂX]ª­Ø:Ëb\x0015rQâÅùã\x0012¯uÌ$T¬w	¡TÚâ,^ñxóV\x0015ÂÈò\x0011rÿ\x0001ÈJ`iÁD\`&\x0001°Wïäõãü\x00113\x001f`ùºi\x0003M<v¶\x0006ÓZZÛ]1ëGÌýËÙÇÂÈÌ\x000cíÌ\x000b\\x001bZ-×Ïµ1ëGvÖ\x0003væûi5­\x0008[ÄãAd±uÈÇ:dáJ3\x000b7`fOK#8AXJ43³R;z\x0005Õ£]Cõï\x001a\x0016®Eðóù\x0015t\x000e¥Â\x001eºUJ¢Ù(èÂ¦:°'\x0000øÕÕæMJxþ÷üçý¿ï®.ï{Ü
Ç¿a/+Ð\x0011ZÈ­ÙðWÇ\x0007Ï\x0012ôÞáóã£³¯h)!®ã!\máF2ájHQqè!msBmMx¶ãÊ9®\x001c³.yÌrA\x0007ÐªCÖÝ¾hÇÕs\=k,¶asó4ðÜÑ\x0016±µ\x001e§\x001d×Îqí\x0018np9ÖRÓw3\x0004Úmï[;­Óú!Ú`Q7\x0019×àÐp\x0012æÙÀÛb½f\^n\x000cc;\x0003èëÌëp10å3ï°yyñªñ¡w
îl¼Ê¼IDMí\x0004bëîÛ[¼j|è]NÒÄ¡h^Äu4Æ'àns$Úyw\x000f½l âÉ}æM]&!\x0018F[ocÒÎ[¼m|èu\x0010G[¯Ïu²ÓòÝ~3ÝÌ+×M\x000c½n\x0012&å&\Åsùf>×¶·ÖµÓ\x0016/\x0018{ÙÂêÅ½à`ñRQ½0[KzÛqM½l>\x000b´\x0003¯Cëúìå­qs;oñ²±-g(\x001air¬tVHy·åÚyMm\x0015¢}Éq\x001048ð\x000el\x000eÞEÆY9¬{bçi»½ç\x000f×ï6×o\x001bç½i\x000b	Ã)f±K
äÜë¥ðâlïùùÑËç\x0007/Ã_n/ää¾$÷cä!Ê@í7Ï55qáH\x001eó¥ £ÜÍÊA\x0002¹ôK¸&Mmð\x001cïÑA9ÚàÅbz~\x0005º,Ñå\x0018:\x0008\x0014©,8EßÂhÒSZ,;]A®Jr5F.\x001c¶\x0005\x0008¯YÂé$,^á¬àÖ%·\x001eä\x0016è\x001e\x0005nL
Ù8Rá[¬xZAnJr3F\x001e\x0002=Ò1Ó2¾(½µÜävI\x0012R\x0000Ý_4¹È«Å,*Â¬ wÅ¦èÜÐ¦¨ÊzgÒ\x0002a'´´+ê­¡à\x001aôpþa\x0000\x001cÈ¼ us}yuusÝFn ^\x0013¤Ï¬·xÒËå\x001bÀ³½W'/_\x001f\x001d\x001f¼\"\x0005¹\x001c&wè\x0003zòø@NñÖ²®Ø
r]ëAò<\x001cÉZ½/\x0005+"··k+ÈMAnÉQ3Ú¬\x0019È)L°[')¬'uÇuÎÐYp³\2Ì&pëTÎå7´\äb\Â5w$%î±¹úVÅþÅ\x0015èªDWcè0u(Å\x0011PãÃñ\x001dµ$
!\x0016ë\x0000WÏJ\x000cÜ³!rCË\x0005Ð¦F\x001fn\x0015-t®íîl.Ê.\x0006\x0017ºs\x0018\x001a\x001b)ñæ"aV/¯ /\x0017º\x0018]è.0 ®?
Õ
è\x0014Åq¹X\x0006¶\x0006Ýèvô\x001dÅu\x001e^Q»5dt¹XÙ¸Ü\x0014\x000b]±\x001e\\x0017\x000e#m9ÖöskP-ÇÃp¡KýÈ\x0001\x0018;ÀIL)6PÖG\x0015+\x0007·ã	Ý.VF· ã§R\x0010
D3JË\x000fÆ*1©\x001dÞ\x000bPéKyxÁ©\x001b]5ô=?=zqp¾ý.\x0001Ï{íG\x001dÇk\x001dKk;ð:jKà\x000e»w\x0003ðrëU\x0013ð\i&\x0000J3«¡yI§HC¿
6·	lVv¹8³XèbM\x0008Ý½(´æiÓ\x0016\x000c²¯©¹ÍKZ\x0013l«þJ`_\x0002û~`g(Êqª\x000e;?$Íèn¹%¨	YòbUHÞ½*\x000c£ÛÅ¬0©)!+K¸ûØ	²)M?²¢áN\x001c4]=\x0016ùsÌB0¹}H÷:äy&ìn¦{a\x0017
Ç\x0003s\x0007\x0010ia\x0018ìK\x0008nH\x000fÞ\x0001²-·\x000bÛ¿]¸4,\x0004!6@+M\x0002UX¸XÌi.!si\x001fGî6Eî\x000fÔ(öêæ®QÿK
f\x0008\x001d\x0006\x000f¥ký|wÇ·N\x000f<=§>±W'g5Õ2û8v´)vìãµt×h@
\x001c¯½'oÚn3YÅë
^×Ïë±g\x001e$sizq¼.Fï{Íà:^[ðÚ\x0001^¸\x00126\x0010×\x0010îvIFÜ8)Í»'Ôb\x0004æºf+\x000eñÔOª¹°ÔUÃ'¤.ö"Däé\x0006Ç±u\x0003Ì±Ú.1CÝGB¶Ô¢âÇ¾µ\x0011«ÂÈjÀÊ\x0012¦\x0013'`Eã#µ¦Éál»¶ÔZd]\x0018Y\x000f\x001898?.õ¨¨u\x0017:O\x0005dÐý±#ær-\x000fY\x0019P/Ov\x000e^\x001c®\x000cci1»	ímÌ¦°³\x0019°³fñvæ80\x001cfÑjÞ®\x0015¿¹°³\x0019°3(ÿ¡C\x0008¶ÙÎ-~Û]Áì\x0006ÃÁçRc
®\ÊôÂRÏÝÕFÇ\x001fmt#;O\x0015ó\x0000\x001dÜ¡Ô¥\x0019\x000e\x0016leÛËH×2ÂÎ1MÚÉì8:\x0010À,<N\x0013\x0010F9ZÐºa
ê\x00024S"ÞaLr\x0008ãe©ø\x000b\x0003Eo®\x001bÏm\x0005-y
)Å\x0008¢ïè(ÛíÜ3¹_\x0018%zò²"â gR\x0010á?X~[\x000fMBBA\x0018Ø\x000e\x0003?k·æ\x0017;°mm°i²\x0000
tu\x0001[*FÖmÕ³\Ïí5âFÖ\x0008ø\x001d8xBAB*m	«Ã\x0011÷V_t57\x0017\x00057\x0017CàÜcÚ\x0008W¥^PÃ>=\x0007:È;ã\x0016%·\x0018á\x0016,¯o­1\x000b\x001dI$
ÈÍâ¼ÎvpU«Ap¥\x0011Üüi\x0000'eÀ­Ql\x0007·)¹Í w*\x0005\x0015\x001c\x0014Û¡´dp±<Õµ\x0019\+\
­p\x0011ððÕ¤þ½ÀM{Nn\x001dÔ¸[Üz[
\x001aÔ\x0007í\x0017¸¥pFÃ]Ýö²õà¶\x0004·CàÊRÕf8J\x0017Ò3V¸ÞØí\x0000%¸\x001c²¸qM\x00047ÐÛ\x0017Á¹ñ\x0008nvøng=\x001f:ì-´¨Å=è\x0007$pjiwÛ\x0005~:Àm	>rÜC$ÉP&KLá@&\x0013øò\x0000ãVðÙ-(\x000b1dq;Í¸\x000eÇK¥·ÜüÔ½Ër\x001d9çý*ÜÍªiãnZQJVÊt3f*­¦7iÄÊÒ|*©jªkÕ¯ÑÛYu=G¾I?É\x0007\x0007ÜqÂ\x000f+N \x0002Á\x001cqlFdååç\x0008\\x001c\x000e÷¿[*IÍÆöÖ§ãT\x000b
\x000eþ7iW}üØÝ¾;d©>LÝB¡»NrvùÞ@úU/N4Ã©äF1òìÆz"\x0007G5yqRãBÇå¡Ü	r7DîR `»Â«\x001aPG\x001ck\x001bù¬¯²Ü\x000br?F\x001e#goa÷MJÖÆÒ-Í÷¶Ý@\x0004y\x001a#÷ò+°\x0018§y\x0013+5[{ë£\x0005:¶Bkù\x0015ycGÅ\x0012'\x0012½J¬B×êèÑ&ùÏÿý\x001fÿùòï>v®Í|ê$n\x0013\x0008\x0014©Ò`\x0014çáúÄ³ÿúòÅ\x0012*\x0008TØZ\x0005(+ji¿WQ[~9¾4\x000e³z1¬~ë°ZßZÂyÃ½ øî{]¬b\ýÖqE\x0005\x0012f\x0005z=ÊN_C]êÐj\x0005ªÝjH¦ ¶\x0012\x0003g\x001aëÂ{m\x0007ëT4<ÿåT4|\x001dl\x0015Ý®)î±jÿhCwA/I÷Ê=@oÝ\x0004\x0002j°·v_G\x0015ëotI[¢ÕJV»UÇs\x001aToQ5µ°úÖ4Ö-Uöô°:Éê¶²\x001a{hj\x001aI*NØÚ\x0007£FÑ\x0000¬5?Kõõ|¥êë+cxØÉ£\x000e.äSC¦
È©Ï;Å¢*Ã²K_ 'å\x0001\x0008-$ÖB[¾û¡\x0016»¦x¢Ò
åíö\x0006\x0010#
00Ò\x0013½Á@ëþ\x000fJú´,RÜ\x000bí$ôÀHç9ÁÐVµP)xkàî¶\x0013´Ð~\x0004:P1\x0000¾\x0001Dâæ¡ø
°{ÒÉ$s\x001aa6ÌÍO\x001d­CP\x001cîèAÒ\x0007m6fd\x001d&ê+\x00006Ï\x000e
\x001e¡î\x001dE\x0004Ô^#m­XÖìxk\x0016ÜvZij¬Òümc-´Ðn\x0004ZåÓ.µ@t\x000b\x001a%=[»\x0016:Iè4\x0002í1ôÐXF.E\x0015¹ù\x0006©\x0016µ ú§\x001d\x00062³ì0°9Ïã*\x0003\x001e\x0002
9Ön\x0013Ü¦&ÿÅN\x001b³Ã
ÍR ] =·}A_jYÕrwç>f¯\x0004³W\x0003Ì­'	`	NÉñ(\x0003Mw<\x0011¡ÖÇoâÚÒ¡¯gÏ¯ÿþþÍÍ>çÎ¦HÚò~¬¹&\x0011\x000b)Ip1C÷õÙó}úøòÇÓÈfªÈf\x001f¿\x0012\x00190EÄ@ýX"ÇÄóia+­$¶Û£¥ÎV*\x001cNïà8³\x0011Ò¬PÂJä Ãvä|G
¡U\x001fÖ|%\x0015èðFd³põïF\x0006\x000cóÑ§¹`²I\x0017\x0005mX\x0017*-\x0000º­D¶Û\x0001+õ\x0018ÔðÒªSw!\x0016úqØ§|û¼\x0000ÝØBbi3ÔYfâ%5ÄndÈÛçvM/,#×\x0006åÊ\x0007hób©ç`/²Üâìö-NÇØJhRäÃ­ÕìK÷:^'yÝv^¨ "¤´ã@·
ná´î$ö =l'Ö\x0006¡0e°6FPV7Y¶öÇÞKd¿\x0015Ù¦ ¸\x0013yÀ:ÈØÔ¯\x0015ïB\x001c¤s\x00116;\x00176\x0001ë×äi(QW\x0019Åí¸ÌRIò2±Iòå\x0006\x001dDqg}uûþ¯×½\x0002
Ù=Æ{I\x0011c´\x0014ï.
\x0017\x0005\x0017+¬^]=ýéâD#òNu×l\x0005Æà,µDÀ\x0014ùÀ	¤M\x001bµZîÅÕ\x0001¬½\x0004Ö~;±eaö|ib5]­)áËÇ`\x0002\x001dÄ0I®CâòóFb¥(\x000fF¡h
=A:\x0016\x0011Óvù&Ò\x0003<UÒE`©¤»j\x0016GÇ\x0005¯>\x0002>ÔGÓÀG´Zzaê"¶ÓN@x-­V\x0010[U½ìA l\x0006Bâ\x001e~>cg%q8"\x000e
ºñ8ªªÂæ\x001cåýrÛÓÄù ýYÔy`«æü÷üçåÇ/·7oÿ|Ý{ÙËSÙU§ÞÄêX\x001dñDr|Ë\x001a9»|ñãÕe¾¦ÎîÉD\x001e\x0004y\x0018#7Þ²N¢³ÞÓ±Ï<ÇÙ9½|ÉE^î\x0016r\x0019ýµüÜR[LÎòá*-g\x0014/k_
w'm£|\x0010m£¾ýôþæëßÎ&}3\x001d\x0005IäÏÙ@405G>ÅÅ[ÕOO/_ÿñ¬ü-gåo9mÂ\x000c\x0013w0Ã§HÍ	\x0015Ö\x000c%Mñ$\x0016\x0001Ð³%CÛ­\x0008Ò°\x0015´¯\x0014Vä$\x000eôfY}¬5c"f$µ\x0019Ù\x0019¤}(ï¤õM
X:MW\x001b`µ0Àê=\x000cH\x0012#ò¡b©Ê\x0008ßÜ\x0003ç%-©\x001d¬7ÃEaÍ\x001ek\x001bV×ÆjMM±2]·Ä°\x0005Oa½\x0019^~
¿Ã×ÀÔpÊ\x0012CÅ×ÄfpÍWrKýF6\x0001Ò\x000cØÃ\x000cÍ\x001a+&jV
Ç¿&3ì\x0017´Á\x000c+Í°ûA×Ô|_"\x000f\x001fÿ:±\x0019KÉXëÍ\x0008rR]&UéÆ\Í\x0000j\x0001_\x0003Ø%±
fÈ%¾Ïñ\x001dYoÜx×^»-W$'cw_\x001bòÄ°{\x0018¸Ä
M*G\x001dÈÐ"þ\x0018°ôf¿Á
ù1Ò\x001e\x001fÃ¨sU÷[cí9=\x001eZn\x0007ãz+pJ|
§öø\x0014ùÐ ¡9cTfñ}wÛù­
f¹lù\x0017"íæóÙóO_:\x00158mJ®mÊ\x001bÏ{Ot0Ë
\Ï_þxB|\x0004vÛó\x0007Sìðyì$B\x0011´DG[1K\x000e_'°#ì70¦ßÖÛ\x0002vt\x0014£T\x001c-1
ºx§bx÷H\x000co
oö?icÁÔ	EÀÐÔÁRo\x000f°\x0011\x0003\x000cfó\x0000\x0003µIÊWxGÝq1kÇµð²Y\x0007ï´9næ\x0015ÍqWñFÏ%6y£\x0003JuT ¹]q\x000cö\x0000vbF\x001cÆ­\x00016\x001d|ëå$ñû²ÔýY\x0011uÀ^\x0002ûÍÀ\x0010(ß\x0011s¨w\x001dV¦Ñ\x0014Þ\x00056Êé\x00107O\x0007

6(LÄ+°Õ\x001b\x0015,=Æu\x0002'9ºiëè¤)1SaoghH|c]lÕÅ;}¡E'Mm\x001dàýê#ñ&7i\x0012¯·Å>¢}Àr°7\x0010\x0015¦\x0017\x0014àÔ2îòÉÀ÷N`¹\x0003ÛÍ;p©½£
"Y®DÖv³×µË<I\x0010,Àv3°7´hÜd&l<ÂË\x001dûå\x0016l7oÁ¥û	¹Rl\x0019Ü\x001bËb\x000cx\x0017`éõØÍ^O¨\x001bm\x001dáDýéJ75\x0002/í\x0004VNÿ,¥\x0017®Ò\x000bíýâÃõÙwúË¼0Y­.»|\x001aSÎ^\x001b=Äyµô\x0000^ª¼¾{yªÆ«@Oò¨\x0010ÚØ\x0001èÚe±¼\x001e\x001e¶J1s}=tËz½Ð ¡a3ô$ÅNGÈÐÆ2ôâ×	=i\Ð²qýJhðÔò;\x001fÎ³s\x0013p3Å\x0019Ý\x000bm$´\x0019Vçµmg\x001fÖ\x0014\x00134,«JöA{	í\x0007 öü27bRÊÉ"Ë¼]lò³È¬MÉÎòÇ#æW\x001f2b'tò£cXüO
!<(NÂ´]#ýêYþ\x001b\x0016°5Slüq+vQ=§¼ªl\x0004'xàè`1f)\x0004³\x0002ÛIìí£±\x0013+cÆìá+j¨ÐZ\x0010\x001b³Ø­¥\x0013[»i\x001ay¤e\x000e÷JnT®®ù?ÚkîÔ÷@WPf)TÔÏíäö\x0003ãÏU
ako,ùü\x001a\x001bþ\x0012wG"w/w<\x001aï84Þ\x0016CDÛ¶ÂÒèX\x00088ï/;Mo=I/Ü2o~57\x0015Ëk¨\x001e¨P¨¬¥°õ\x0011¶\x001eÁ¶\x001a%C
7½\x0012qs­\x0010î1{qË½»ü¼Û\x0005ª×¨þY\x001ft¸µ].\x0008éä\x000eVw8vþVq'Mmuh­«u2DOò_îµpÄ\x001d\x0006¸\x00013ÈªÖ5ö\x000b«ÔÖÐìÎ.UÏ\x0001ßC\x001dARÇãûÁ*jÝGß­«2ùH£
n¹¸³ûhÄY\x0002`è\x0019UÇd0¯¬p7)<ídº¹ý\x0011·\x001fá6íÐIZð¼N\\x000eEí{a§#ì4ÍùAyù\x0005Þ\x0004Sâ3ÞÀrár'wRr\x0013LÇ÷uÓÄQ§`º\x0006TIÄmSg{¹¦I\x001a&ÖÕøÞU"·'8ÔÅàt'uþw
êòóvj×4\x0004°uE"lÍGÕËeµ½ÜÆIîã»Ù:nî'
xw\x0008¹	Ûíµ(Á\x001eaß¹\x0007¯ÁÆ\x001aq\x0012C±Ù£"¡[\x001dyQ¸Ëä.2È°j>nWðÜgP\x0007§é)#ï+<»µëQ»í&wÜ\x0003¶
!pO5FycÑìRÍÇx6[\x0001nÇÀ5wêÍä@1\x0013Ü¢Ø©r³Î÷\x0016ò ÈÃ\x0018y¢\x0018D,É}\x001bóÙ\x0012Å
äN¹\x001b\x001bsT¦±ÀCh³|¶.f\x0003x\x0014àq\x000c\x001c\x0015ái}¶\x000eD\x0018GçC$h/x\x0012ài\x000c\x001ckÈC»òT¼§våQûÌ4>½Ó«GáøJÿüS§`¹Ë÷\x000e*uVÉrG\x0014¯\x001cÇèãüRa~þòÆz!SÏJ=ÇÕ
bªÄ¡=£HÄ¾Ë?é ¶bïÜ\x0018Ö\x0010G®ÁUÒ\x0002îl\x0017½Y|~ì$rãÀ\x0018'*Áÿ©¯l¢[¬ÁíDNZ '½\x001dâÅ&¥\x0014=§Ù¸DñâèæÛ¬D\x00061/Òñ
x\x00052\x0006ã\x001d!'¬¨*ÈÁ\x0007F^½êE\x0013#
L\x000c
%@È×DÈ¤\x001b£sK:\x0003}ÈZêQùy#³Ê7\x0003HÙ°\x0014Z^Úéì²vM\x0017³6Y\x001f;ØÝÌ6{G%ÄÌØJÉSÒX`fÓ\x0015@ë`¶GÌÇ¯\x0008+³£¡k¿û5	ÀhÞçÜbv'³;sùy#3¶\x001a­Ó9f\x0007ìð¹½"Û0ß`«\x0013Y?¦µj'¼'å¸þú·>æL¤å­\x0006ÛÔ\x0013\x0010TjOLòb?=yùüùë\x0017\x0017¯ÿx{"\x0003ÜG\x001d¤×ãã©&p ú¼	r­¶Y\x001cì~n#¹Í\x00087¶u\x0007GÜ\x001a÷\x0012rEÁ\x0017~ðÀ\x001bÀá:Ý¨\x0003\x001f0Zs;`³¼ó­\x0000#îF<Dó\x0015på±jMÓí9R-çðõG	\x001eÀó\x001eHA!\x001d$Ç¢£\>\x0003oíýàIN44U¬¥{Wã,ÿ\x0017bhs¹çu'ø$µ\x001aÁR«×;ç\x0001×-/Êq¾½Ñ\x001d¹´½ÜZ\x000c8è¡\x0001Ç"& )îHx¼\x0016ð\x0014ßmmBàq\x0004\x001cu+h¦\x0004îÚáSòm7Ô³úú«Á'^\x0008nÌ\x00108îÝ4Åó¥¦J\x0000$­ÚÒ\ô¶û¹å¡\x0001Ï7\x0017jïRr3Jü,;)!ò\x0014÷¹\x0019\x001dà\x001aJïëiFh\x0010êÃ7g¯®o¿d¼>¯;{NÔSL%eè>¦Që¨SÒÉÅÕù9\x000c\x0012\x0019¶#ãèRÍmÊÿ\x0016äÍ³Ö£5Ë¯L]¼\x0013ËÒhÔmæÍS1T°$ª³\x0019uëì¸W'²¦ºGNÊß¬@öyÏà(Fý·útê#ïêõò\x001d¡\x00139Hä°\x001d9òó#¦5hJD¼ßyX,8êEN\x00129mFÎ×ª¨}=ERÏ\x0019EßürP¯Ø[1/¼Ý>/P1¡¾ê|¨$Ê?³twLÞÎ¶ÉéEV±\x00089M|\x001eÝ	ùb#þçÝZ8§±qãç]Å)\0û\x0002&\x0003¾ØÆb\x0001z\x001dQjh\x001a\x0013¡\x001a<'e\x00175\x0001J<GXMí\x0004µ\x001b¡¶æ¼>
 ¹¦¡NDqw\x001d­ðú ½öCÐ\x0001Ýºt\x0016(R­1 ÃIga?j1«ýè´N:\x0010u`m{nw¢\x000eb¬ÃÐX[JÛÇÄ5RæÔ$;\x0017°ÙrõÐb¨ÃÈP\x001bM¢­\x0019:\x001ee`g°qäZz;\x0019g,½\x0015fè/>¾ë-ª¸nòâÃP0GpÒ~HaI³àò,ÿâùË\x0017ß-@OõøáX\x001d4G\x0010sÞýb}ã¢jµ|K_ÎXí$Ã\x000c#Ãl\x000cÙQ
H&ß¸0;q\x001ff£\x0005³Ñ\x0003ÌèðS/oì/Qß7Tf Ü²×Ñ	\x001dÄÔ0aûÔÀ&ZzL\x0007ÍR)q®òz±\¿\x0013zRÍ¨«\x0019WB{lCsè@NíR´!':jµ×"´r¤íÀHãí;Ôéá\x0000h\x0015fhV;Ñ.-&:õA\x0007# \x0019Î7,W·à=gzê éIÃ%EÔ~è ¡Ã\x0000´-.\x001eB\x0007uN³#\x0018z¢3qI«¨¹ÈØM7ð¨ì\x001d_o>|`æÔÂV¬\x0005ò\x001d«¶y|Äðå\x001bæk __>{ÆÐå7§A0Ã\x00003>a$bö(õ[í\x0001y'b+í\x00001\x0006§k\x0000,yÇ9{Q±cýì\x0012ìeÖ\x0000Ò³Ã&ØÒ³['F¡
\x0017Ç\x0017\x001e\x0012£hU`n6Õúà%-VêVd\x0010È0\x001cùÕ\x0005IQ\x0005R\ï\x000eµ9a\x0003Ãl\x0014\x0008b`:l
W\x0017Ã¼¾ÙZäi(	r®Vêªp»¼y6M6\x0003\x001c\x0016\x0005?»\x0002W3\x0007Á\x001c\x0006CS]ÏÎ?%/\x0019Ã"æË\x0019bÀI\x0000§íÀNóê,D`\x000eB¿\x0018ÎÝ\x0005Y+1ñÇíÜ²pý±\x0004\x0013pm?Ì×Ö­Ö\x0012Z\x000f\x000c´¥¦
_´|}ª5ö°\x0002;dû A¬@
\x0003K\x00103¿	ZAÛ5\ká1_}¹\x0016ÚHh3\x0000íBW>Ã©Ô\x0015\x001b|q³\x00063{OY\x000bmå¶#sZT±\x0002mÉÙÈsCýø£ÐVÉ{7\x0002Ë{÷Õû·¾¾}×\x0017ÞHÖ·
Ùy®
\x0007Ybè¸\x000f^=}òû«ï\x0016£$ÛÅ´¥:Êsxcbm1LDÞ\x0005ÙÈA6\x0007¹xÎ|
jG\x0015Õñ¼ø\x001aÛ<y¶Bdñlµ\x000eÙ\x001cZÒdúX9\x001d6é´üÒE<Õ\x000fÂç<ØN¸à¯\x000er¹Ò@\x0006yQ#¯\x0013Ùy!+tV!ç5|\x0015ÙR2Qí9\x0013ÔN«o*\x0000Ú>ÊØÃª
\x0011bÄ
\x000c\x0013ç\x000bsV\x0002\x001b	l¶\x0003£Z\x0017õmÈÞ\x0011Ð´h-Ø±Íò>ÈV"ÛíÈÞ¢ØQm5Áj\x0006³·\x0008Y/û-!+ãåv!·ÏØõî}_ö3Zº>bÌ\x0013äe¥=9¸´ø.ÿ\x0003ö¼{:²AÀN\x0002»­À´##p\x0002VPÇ{6\x0003÷ät\x0000\x0007	\x001c¶\x0003'
6ç.q\x0017UZwÁ/uÐé¤Mr>¤Íó\x00018Ï?bó\x001fæ\x0007N?
Xú´\x000f°\x001cÞ´yx1M\x0013Ý\x000e4y|YÌ­\x0003x*Íùâj3°)J\x0013\x0015¸\x0014ÀÕ\x0011æ	ìÍbZI'pÀa3°ÁÄ¿\x0002ºn4¦-ÂÛÅ³®\x000bØ[1½Ý<QY¬\x0016~hoÎë]/H\x0003\x001c\x000bÃ{xµ\x00021#ÊÏ\x001bS(i­å	
0¯«\x0010{
\\x0004Løß8\x001c\x0011o\x0013ØÆÓ\x000bq<±:mG>k\x000fq:"N\x0001/£ëîñ\x0015VÓl¬¥ØFücÚ3<Æ±QF¾}Óùmm¾2Q\x0016E½Ú68¾M£üûCñì\x0002¹¯^xÈ.èqòàÑã±´Î:t,Ë#±\x0017ÀÇZüaËC\x0017\x0019Ñ£eÔ®u\x0014èåçíì&zz)Ènb¬2Ø\x0014.ª±Kðe\x001c¢Ìå_\x001cGæV¾@ä)B·½=kL ±\x0010+vÒ\ÎyX|52öR¨í\x00085µ#ÎP;RHQ33Ìf¦­gvÙ
0ciØüÔc\x000fÉÎ\x001dÕÈ}ÔNR»\x0011j¯Xø6ÚNP¯'Ð\x0006{¶cû
ìãxâxÆ?ßüåýÇ3jËýæúkßFbeÄ\x0002ä>¹&7\x0019ê'¿¿|þôÅ\x0019µå~|ñú4t4\x0002\x001aÜ
ÿ]t\x0013Ô±n%,ÐD\x000cÌêzwCç\x0019b\x001a!p(ó2¾úôöÏ7oºÅ,=*÷RòC\x0004Ê\x000fø\x000eAy\x0004ÙïÛû\x000eÜW/ó_?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=JC\x001f\x001eDTCDÕ(\x000f-õ_Dkr2"ç/ý´§¾\x0007Q\x000f\x0011u3",£zDa)ë¸´H,\x0017¢\x001d\x0012ÚvÂ@f©Ç­ôT\x001f£|F¤Âr!º!¢kFÔG°È\x001aþ9QöL¼×\x001eD?DôíRÔ<\x001d\x000e{þÎ\x000bñÓ°H\x000fb\x001c"Æ§y[Fº1Ýa)Þ\x0013¸4jjÊ*7ìs¿Ç)o7w÷\x001f¯SÅã<c,AùÔ[+Tu¹6FÝ­8òíäìòåñÑùÃj©:0ñ0Ò¤z\x0011YkåyÙ4æÛ©ºG<ÓÐ¹à¹ÒK;nB1r\x0012xíÃ4CLÓ#MÏ¹¡$M\x0012f|TYÚ!¤íäï
>\x000cÍØ\x00074Bt~ws{\x001b¢\x001f"úÏm9\x0002øssBKÏÌ´o\x000cCÈÐ\x0001é\x0014G\x0002Áj¤\x0004Òo8|îÇ8q\x0019{>·áªMò&LCS¹\x0001Óìîl¯Ä´vjLÚ\Ä¼£¹ý¡y·XLEÖ\x0006÷çnÒS\x0002îÔ¤iðÕÉW½íû'ó2®\x001aâª^Ühy{Ë$x \x0005Íl\x0002ÜIº\x001bW\x000fqu·t\x0005ÝªË3#\x001c]þGÄµC\Û~#\OC}´44\x0013pã#áú!®ïÅU1m¦O¸'ÅHVZ\x001bÌ£àÊñUë¾k29è7Py¹\x0006}A§AN\x001aæpgbÏÄ::¸²ûä
¼y\x001cmx½\x0004O;Â>ÎQ££ {Ï\x0003Å@¦4\x000eDÌòZ\x000c'dÖé±Ù\x001dÌ\x001bG¼±7\x0014ù:OE¬À\x001b\x000b¯vôÉWÎ®ê>»ÂóÒ[ãUÑ#yÔug÷!ñªÑñUÝÇwpÕ\¤Ù±\x001a\x0017	³x§\x001bX{yGWuk^\x0019Ëz\x001c§\x000fi\x0016¢¥¤8ÇúqhGMõ+^ËS6Àâ:äIHª\x0008÷îèª©Þ«^h\x0016¹±Ê4áUã)Xr§íåÕ£«¦»¯<rØwSÆa1í¤¼¤vlá,1q\x0014\\=B\x000f\x0005Oi\x0006^¹ô\x0011S{WÚÁè\x0015)\x000fNï~¿úøfsu c*.Ï®.°ÛjË
Ó\v\x000f¢ÀßâìG/\x001fåßâAV5dU¬¦t\x0012¡CA°²D{ÝDp\x000f«\x001e²ê>Ö<@ËkbÎÀ\x001b7SÔÍj¬¦U\x001fÏó\x0005U(ºz\x001cV;dµ}¬*ªÎ²FA:oKõôîY3í°n\x0008ëú`eª;M°AsÕ³¥pØûóTÚaý\x0010ÖwÂJ2\x0010R¥\x0013ÕÌm'þ;«vD4{`Ã\x00106tÁ¸mÆÀÌªKfÊÉG:\x0005qÈ\x001a;YÍ¶ÒÇS÷qñxA®;Æõ°\x000e«2ì¶*£\x0011\x0016§P}\x000bÜ/\x0016\x0001KV=ãÇ«ïõBÃ«àLª\x0013/µ£ºäèù}ï\x0017ºa|\x0010àÙ¥²\x001c\x001bËIÀ3ñ(´£\x0007Lö½`¸Ò{ÒÁ\x0000§\x001e>ëi`ýV\x000fíè	}oÑ®tzÍ-Ö©¢\x0011vÌ.ì¢\x001d=b²ï\x0015ÃÀb KFiîM°¶4i+ùH'aôÉ¾gÌë¨\ImZ*ëÔÜ\x001aèw\x000eEê¡\x001d=c²ï\x001dÓÑsq¶\_fe9¶Ó\x0015XÝ°£gLv¾c`!\x0018Ê"b[²h9ß)v\x00150ôÐ\x001e2ÙùH.ÓKFí"V\x0015\x0003ü´­\x001a½dªó%\x0003XZå\x001c½=\x0014a¹ÊÆùÇqmÔè%S}/ö±\x001848\x0013ÊRW`éå\x0016öuÓ\x001d±¾LGMÇ6I£*0+\x0006Øã\x0018¶jô©¾\x000c¹\x001bÝSp\x0006
\x001d®øsæq|15zÈTßC¦Ã¶Ù\x00101G\x0007¡ìàð»põÐ\x001e2Õ÷á&ò"ZÃFÙ¶i;÷HÇvô©¾\x000c7\x0000\x001a\x001e\x0018¹=Ùx[ü±]3zhG\x000fê|È´-ÚÖÌè°U`cÒ¨ÑK¦ú^2m,
Û\x0003_WQ ÉØR¥ïw\x000fÍm\x001d=dªï!ÓÒ>u_\2\x0003ÞnÑ_s\x0010ôè%Ó}/V²z ZS\x000eB¬}\x001c[Q^\x0006Ýù2\x0008[^à¸[Ãl§ëìê<è%Û\0T¸\x001a\x0003\x001fÂ\x0011\x0001ÒÓ`M8
¥QXú:\x0001Ïd!Å4X+¶ÁÚÔ2ñr}ý	þ«Ï÷vNà8\x001eO\x00138©=Ï\x000b¼\x0012)H»«À\x0010\x001b'^®/ÎNO^¿ÞÛ?1
Ôm ¶SC\x000ew( (E=Ü17×\x0017ÓÄ©úéÊÓ\x000c9M<uéÔt§×Éí0\x001d'\x001f\x0005Ô\x000eAm\x0017¨?Ô¾´\x001dÑþ?YfYy¿+*×\x000eê ®\x000bÔ\x001dR¬ Z\x0000³¯¹£L?Ê	õCNßùåsÂ\x0003>¶ãU½²y\x0008Rìªm\x0006
CÐÐ)Ð¼éÐíÃ¦Òòl¹Ã1lçCÎød¯¼\x001c]yÙuçGÅ\x0002*X ÜÁ\x0007¤Ë®¶_H1\x0018ûP¿ÿò¯ÿ½¿/í¢1ëh)"yñnZbÆV&Îï8Úßj8í¾"\x0017É5\x0011¢uGã§ñì¸[ÛüîÑ¤-zH¨	-àLI\x001a×è¨LÇÚéê\x000eB7$tÍÖò\x0016à$mwÀM³¥¡ê«|v3a\x0018\x0012fB¥8uÖ\x0003Ð|WÍæ¼
jZ!ÐN8lÖGÆu3¤;tÛ£hhî¤áÌõ_Õ75@ÊéuÃ{b>\x001dàªèýjÜNyøK\x001a\x001d*Kºrºó
á»b.òþAF5dT\x001dÛ\x0018¤æÕ\x0019\x0003Íè0,½\x0018R\x000f!u;$NØ\x000e¥²l¸ëEq·\x001bÔ\x0004i¦\x0003Ò\x0015¿\x0007Þ\x0018C\x000cÛÏívG í\x0010Òv@F\ÒÇ=Ô³$K[ÕWãÉº Ý\x0010ÒµCâ6²H¶\x001aËmbo×â¬fH?ô­ \x000e}étM
µ\x001dÄ;\x0017Xl\x000cCÈÐ!I·¤9dA©¢â1>MA\x000eùrÌ¯$\x000e[\x0015Dýi¢\x0019ÔqùÅ#e.;´9¼\z¤\x0003%i\x0014¸\x000b¥Nj&\x0011ÚD9R²CSFYd)5íRÊ\x0014J\x0019w'¾(GR6«J%-NËM²ùõ.-²z¦0ªq¤(e¦\x000ca;DuÛÈ«c:5\x0013Ón¢\x001ciJÙ®*õ,I)ÀÆÈÏ·esÒGù\x0008\x0017|¤d»\x001aúw@ª\x0016RÍZHáÄ2\x00162ðÖ-¥³»"\x0003­#³W5Û½J9\x001a}\x000c\x0004#=\x000bÒóú
\x001fÝîB&Æ±ÙÛ¬)ÿ-#«W5½ÿ\x0016Æ.WÍº<5Áó2,Ô¦×Ûm\x0007ºÍ\x0014¸5Qô¤jÖè\x0016\x001eJ§©ÌUi¡¶C\x001f¦È\x0011Gj6Õtº¶S\x0003¼§×&°þ\x0011fù×Ö#ý£Ûõ\x000f\x0018Aú\x001aJFXvGI·Ü\x0011Ó£»­;î¶Re\x0000Øj9/­¬*O÷®xt+äèâèö£À]äèþ6¯c-/ÑñÓ)]££Û/r,ñ\x0002þR[VBLig\x0012M£»£ÛïÊ&¼ðû¡(ÃvÅõÛ ÕØ©Å¿m¿<¥í\x0006÷ÔÑ±4q»?o¦^µ	s¬D0qé2ayIÕÜ\x0012àýrOGÍ5Õe¯©²\x0019Ghº?1ÃòçQM\x000c¶\x000eMá¬lÊ9aÙ\¶Ð­á5\x0007Á.¿æjb±ulÂÊ²t\x001b'ØÓ2Ô\x0013¬å\x0002%Aßd\x0000¯Û-`U*¤ÝZÀ¶4\x001eÁ/\x0013q\x000c\x001a9q[Ì6öK`p~T\x0019¼k|Qsìw\´!i*YsLP\x0014'R)\x001e½k&¸zºÂÜk\x001cMF\x0004¥\x0018p\x0017¨áEâ(Ó<Jb\x0018\x0006Æ\x0008Â2P3\x00055} Û±¯Jó7Ìï±DÃRÚ)¨í\x0000\x0005]oi\x0018»\x0011ü_2B4Ç¬¯\x0008\x0010>\x0004:Ü#@Ë\x001eÉë$\x0001oxà·Â\x0008üéw
²j\x0002
S®O\x000ff¼àÝQ\x0012'ä¿Ý_ý°½4Ç9]-)ýpÄßwëÍÝ§OW{·^:,çr2ÉMi>j~¿+Gqt³bÏ..ön¾$<5ÄSxÚnË÷%÷q\x0004Q,$±³¤\x0005Ï\x000cñL+ËXÉbW<j×\x0016}![\x0018²F6eJ\x0014\x001d\x0007«çÊa\x001fËÒ\x0000»Ë¸¬ÃSjrðÐ<Øâ­>_Ý\_=°\x0008\x001c+ZxF'\x0005«£ìå\x0013»º\x0000oõúèäøhï¾mÂÓC<Ý§
º\x00105;cGV\x001aX»×ã!iÄÛý\x000bÂó\x001au±m\x0014j÷Ç­Ç³C<Û.=NÅÇ@·\x001f×ÆÝûçëéüÎ·Óq½E(µ?@Ç5+!.\x0015^\x0018âV<±M\x0004ö°)*Yíªõj¡CºØHg$o×ÂR\x0010*I\x0012LÛ°ôäÉ±ZiÖ+ë£±
Ä±^áJé&âj¼7ÓºØçT\x0017ûbý+Ö¨|»Þ¼¿ß«\x0015vLåÐI2³²Éâ
Ï7ÄN\x0011ÛÕ+,OùvuþÝåþ\x001dÓz¢qÞ¸Èçåúzs½¿$N¨Òù/EY\x001f®
;RÓâ½aýÌËÕñùñÞÊ==1\x0006\x0000Q5#J[Ú
4ï¿PØ\x0000ÎÆ¯CªEÔCDÝ\x0018§âl\x001c.Î5\x001fÃ;1\x001d«Ó\x000eh¶\x00190ñpø8è$Ë0P§åtNQ\x0003¢Ö )9X\x0018÷úv\x001f£Â\x001e-Ï\x0011'\x001e­¥¼lXy»{êb\x0004àãÓ
H34í¸\»v\x0015\x0007rÊ´R\x001f¦·¹Q©\x0011#þm+¥
¼\x0018ÉKUöy;ÁÝ-AL:	Û0åÔ\x0012jP\x0017\x0017ð<\x000bcìÞ[
Ê\x001báÁÈ×«â8\x0017#wzH\x0001Ocþ?È§|ªOC-KuB rvSV¦É\x0001»\x0016>3ä3Í|ÛÖVÉ­­pWJ×Ý®ö6>;ä³­|XkJ}+åÚdà§Ý=þ¦Ï
ù\+R¥P\x0018N\x0016H[\x0016ÏJ±ø\x0000!`h\x0006\x001c\x0008Û}x×\x001aß\x0017Ò
k¡Ô°\x0016ªöþF~òlà9¾ài\x0002ëÝ½Ê-£û+\x001b/0\x001cµb6à\x0000OK©Ô²®\x000eLë¥7DN l<JÆÀÓ¬<¸v¹ß[ÈE·Æì.\x0015m!\x001c\x001dAÙx\x0006RrKhyü¾UÜuf¦këÛ	Õè\x0018ªÆc¨\x0014.iD(¨Í\x00103E»\x0013\x0001-ãw¤õ\x001cbW?ÉÐa\x0001\x00195\x000c¨gZx\x0007s@ºÆãeºÊå\x0013¸,bú\x001c\x000b5nü~}s³ß\x0005P)Zæ¾²ÞN$s-Fß¯NNö×Ó°Pã¾Ç\x0007á0ØQÒæRÚ½ÕX-pf\x0008gÚ$'uà\x0003WÅ°\x0019ãÊä©ehvf\x001bå¦Ê\x001c7\pÊ}Neé\x0015\x000báÜ\x0010ÎµÉ
ç¾Ç"7ÎÝ\x0012ÁwbWÄ£\x0001Î\x000fá|ä¼Ý®_\x000f\x001cîb»9Îu0VÂ!\hÛî·6m)\x0011uY8º3ÐV\x0005\x0017§\x00118ð;NÖ¿ß]ï\x001b\x000f'N\x001fR\x0014+(V\x001a\x001cJnúî®Õ?Ï÷
Ê'.5äR-\^Ò((°E%ïg\x0011 êJX|ç#V\x000b¦`ºI`#ÎølÄ46î.Ê¯\x0005³C0Û\x0002\x0016K¿R\x0008Û*-J¬yW@²\x001eÌ
Á\Ä\x0004+5üKî¬\x0011l1Ù°»¢\x0012,Æ!XMlÛ\x0012éÓ\x0018ÕLÆýa÷ÀêÃ?¨HÇÝ¦Êr9\GÒû\x0001¯{ÐÖXj"\x0006
+´6±Sá\x001f÷ëÍçë«ÍÁÙÍ¿îSg:HÃ\x0005\x0006§p¤¼\x0001Xæ\x0017W	üËÕùëã£ó³\x001f^¾WgÎèì\x0012:\x0015¿¦[\x0002§Æ¢S­²ÃU¤4a\x001asï2·¼b²é®\x000eÇ,M^\x0002e«®>\x001d<¿»ÿôÛýÕçýë¦¼ã-ô\x0016þPc(ZNôn	]\x001c<?»¼øÇåÑë½©éì\x000feGqÑZJ\x0015x\x0013¼\x0013*ÀUTeù¨ q"Ôtì²Ã-NFh$AÀn¼\x001eRMGöIÒ\x000c1M\x0007fàI\x0005ÎºPÖÉ½ãzb\x0000ôQº!¥{ªaH\x0019zNe\x0019ÃË¤ÉBV¥ºIëÅ]MèÞ.98·í\x0002f»t*àüÂ\-ÈõêÚé¨}Í
¦áÔWi¸çwwûmfðÒ(u\x001e£/­öªÔED=?\x000càùÙù7{uå4	§¾JÂ=\x000c¨¶ëÂqmâ6{ÎÍÈåz\x0008¨[\x0001\x0005Ã=-dL²,ç\x0016{FRT\x0002! i ¡ú\x0003\x0000\x0007\x0016ºì`z>IX	h¶ù\x000c- !\x0005	ÆòÅ|µ\x0012Ð
\x0001]³\x0004EÙ\x0005g*8´R'Á0\x0004\x000cÍ\x0012ôEe	;¾ÞÌ÷Õ\x0012®V¾AÌ\x001eµèP3%¸­Q¥Ùd2Iª\x0005PN}`9ô/>¯÷£YðNxÎaä¢:_æ´î\ózypñzU\x0003eP¦\x0001ÊX^¡\x0019£"gNº­_>ã3Ub¹!kÀÂ:0J\x000bAq\x000céJ£\x000b\x000eÜ[\x0015X¡\x0001\x000b«Æy\x0000X /\x000e°ÊÔÒ¸;\x0014ÿ\x0010V\x001789¬(Õ\x0007/î7\x000fà@#â½Ã=YµùÈK¥T4»ëà¿}y¾·\x0008ÇM«
\x001cõ=	8;³O\x000cÎ
áÜÓÓ£3§Ø¡Ó£C§Ø©Ó£\x000f«ÌÕÓòyíGúÊ>­,\x000f\x0012TçÞ¹ZÓù\x0015Û"ê\x001a?¢ÕCZýtis@k{k´Èyû»ûÏW\x0007\x0017ëë[øÓ»»oö/	øü6;À\x001eK²#µ¡q1¬ùª¸åìòõÑÁÅêø\x0014þôâìäìåó½\x000f]Ú*aÔ£puû¯ÿûGéM6W°<\x0006êà4V*¯.³-UöG§û^"3C2ÓFY>"ÛvqEn \x000faWÏQ\x0003\x001b¢¹&4,B$ûXá\x000em*Tl `f\x0013*ÙÂ-´±\x0010tã¬\x00157N°«^©M\x000fâ\x0018@§½iÂÃr±Îå\x001e+¢Û1­\x0006ÏMGV:1È©}{·yµ¹»Ý{â¤ÄF\x0013Gy@­)ýxjw©Ü·gçß\x001d>\x000c§pº	\x000e+s\x0005\x0019¥`+Sj
mhN­íN-TÀit7¤èîñÇ_×>5Ô^\x0008[\x0016ð9\<NÛÆ¡£§ãäZ\x001c¿|µº¸¨¯¿\x0008ÓàiHÁÓ'\x000bê ®\x0013ÔÛ\x000cêÅ¡fN.f\x0011\x0013ÿh7çL¼/LA¼\x000cêéSMg½*1L?Ü\x0003Íf³¾ÿ¼·t\á
iAµÄÖq>ß\x0007.n\x0007Í³;ýp	¿p~¾º|½¿v\Lckb\x0018ÙRv\x0008i!5æ6¹ÍVÒÆ'\rËo7\x0000éîJÒ\x000f!}$áV\x001b´lå¤\x0000\x001bANÒÿ]a\x0008\x0019¨$ÇÍÿéã/´²
îWöR:N@xÍ\x001eaÚ¹u.AB7|
jº@Ñ\x001fÔ\x0011ÙNóe>RT\x000fËtÓLÕ¥!¯àæ¦!ÄªxM1Îo¢áòBñ<büÕ©½qrR\x0017d]O^¬héEIÉgÈ\x0017w÷\x001f÷· %!q³ç\x00114<\x0002¼Ä|Æ|qvù²\x0002Ó\x000f1};¦\x0014Ü"â5¦L2¦Æ6 \x0019&m}}a\x0019:¤©K8V2¢N\x0011Ëõnq:¤²8Õù«\x000eLÆ\x0019&Lï\x000e\x0005a\x001a\x0010§Ëwrî¼;ëéþ\x0015èo\x0014à"ÒÁ´¼øJiGÖº\x0003ÃM-e´#FÛÃèJ %\x0006,Ü#HÒAqº1»\x001d²\x0014Å'H,ZW\x001coÍÄmÄìÃt\x0014nusýi¿¶t¥6>u´¶Ü\x000e¢s\x0019½£ïN/*\x0008õP·\x0013ùR@\x0018¹¸\x001bZÚ¬fO«\x0011í\x0010Ñ¶#XÖõÀW°Ê¯ Îå\x001d\x001fB\ç½PªL^\åõnp _^o®~_ß\x001c¼CØÛïá	ßw0-<!?à\x000eÀ© ðö\x0015§)Y{y|~ôÏÕÉÁ7\x0007G§\x0007ßÃSþìíúÝúÓçÍUù)v\x001ccÇ\x0005ØÆÓ 'ï´à\x0012(%\x0015Ú©iî´\x000b[#¶tº`ã\x001c\x0000Üõ÷Ïë\x001b¸õð\x0017o\x0001~¿äP»ç\x000b6\x0007zµ\x0008¼Ã¨I.õÇ'pááÿ.^\x0000/ØGs|oòÖ\x0006ÜáyÚo\x0002ûì\x001b°Ý\x0000,é&dÝ_[eØ¼'w¢+\x000cPÏù\x0006L7@K	i\x001fDTeÄeBÄ¿mBL
´yÆÇúgy\x001e±ýÚ¤Ìª+àÈàß>Kññïïß\mö\x001dEuÅ7\x000chô°ªÒÚ¢4§­	).~ðýåó£ó¹Ãç~ü=¾µ¿%\x001dQ\x0007üãèãõ
ZìÊ\x000eÜ³WWo?ÀÚ,pê\x001a\x0008H\x0006Ö Ãà\x0002~Eð\x0001þi\x0014Ñ«£\x0017ß?;zù|ur1û;o>[ÿûéwÏ¬\x000fNÖ÷^ÍüÞZ¨4~\x0014o­ò:8é*×Çù cjÂN¿w:Ùÿ5÷Aàw_Xÿ|G\x0019>a ítÛÞÏýöà±§ªVìeG+m\x0017v E¤ÿé.íBÎ¿ýQ:\x000f«ïª\x0000à"©\x001a\x0000\x0017°T5ýïÇ²\x0004\x0001B.K\x0000\x0000\x0013\\x001f\x0000pë*4È"\x0001\x0004\x001aÐ\x0000>\x0000øçª\x000f\x0000^%¡\x0013`Lú\x0000\x0014\x0001\x0008Ûù	@ÛÊ3nh\x0002yb\x001a<\\x0016\x0001R\x0000¢\x0003\x0000¾«\x0002ðØ1\x0001t\x001eô\x0000\x000f¡0²\x000f\x0000®¯\x0001\x0008p	
\x0001¨¬à\x0012<8\x0004\x0001Rt£\x0003\x0000P\x0001\x0000~`ÚD®¡Fm\x0000N:¾\x0005yÞP\x0007\x0000	±\x0006\x0000'Í(\x00020y\x000b\x0016\x0000\x0005D=Ð÷\x0005°¬\x000bÿx\x0018\x0000¼M\x000f!æ`Ry=|("ò}\x0000¨\x0008k4¡¶þ0A\|\x000cüý5\x000b t~\x0001toe&Ô[=\x0000\x0016o^\x0011 \x0010øN=~¬S\x0011Mó;hs\x0007\x0001j"ïø\x001dìÓ\x0003è<Ë\x001aU¨m2¢\x0008ÀW1>\x0002)"\x0018]\x0000ðéd*4"o-Oß¦.»àX
üëøý\x0001[ÖhB°R­\x0008þþ&½Ìé÷×õ@´\x0000n¬Q\x0016ì\x0011kè\x001eè\¼=V	rÎ½\x0000ô ¬Ó\x001fä\x0008J\x001edø[Í§ÀuÊ\x0000>¬Qx
\x0014`p¤y"0îÖ}\x0017\x0011\x0018«\x001a]dµI¡$\x0002Ø\x0017\x0002À÷]\x0004løW5Ê\x0008	4ÝDãX\x0019\x0005\x0011ËG}V\x0011ªF\x0019Y\G
\x0019\x0007Nç\x0017©ÜÔyØñÛÃÑQ5ªÈêÔ\x001fÇ÷ _Ä ]\x001cbç\x0017Û£jTÅQ«¶¨"áé\x000b\x00179è¾k\x001e³ªQF\x0016U°*¾%\x0019P:>É®ó\x000c"RUÊ\x0008\x001bÂMq\x000eè\x0010ªb\x0017ÚNç\x0004g*«\x001a]d+©\x000fy\x0018\x001a\x0012X~\x0011ò¬\x000e\x0002ø×T.²Ú\x0015÷ÄR\x0008\x000f¢)¾©ê#À0®±Ìlp`ÿ$xåY\x0015t¾I8øVW©CpP$»h>×Z\x0001-WÁtºhX\x0005««Ô!C-#ÅoR0±|\x0005Û§\x000eð%ÑUê07	c\x0014\x0008Â\x0016 S\x0004ðítB9DÆ!_\x0005¾½§\x0010T¡®Q`\x0007\x0017U\x0000fª¤'1nob§q&¥®Q\x000eCætAqc\x001a½	L\x001f\x0001:·¦æ\x001e8©qÌp&0¹\x0014	|!ð}¯"F=MÕ=\x0000ûT"$»ÁÛâ¥É¾{\x0015¦ê\x001eÀÿp>\x0007 ÉO\x000b´#\x0003uè$ÍÔ=\x001dEl©áWÑ\x0015'¥\x0017\x0000^DSõ*æùûY\x0004:×(:4UU9Ç\x0000þ5Só,*8ÿ>\x0002èZqÔ	di<S\x0015®°l\x0015CIN¢`Uhe_¬\x0002ãà¶*T{¢È?À³\x0014³5ü\x001cÙN\x0017	U¸­¹Æ\x0008vÔ£3l\x001bºÈF¡\x0002ü×lÍ541­ùÎ· rÈÎ[_ü\x0003Õw\x000bÐ°UaÓëêÓ- hQ	Ø7Æoà\x0015N/A.pÆÐigÓÉúàâj³IùËô;Ïå\x000f|¯$\x0003f[²RÎ®¢\x001bÈ«£óó¬L¿°;Q<yp\x0007çxÁ½X}yuprw\x000bKL}~8G(öÜ¬¡»é­\x000eå©^ýðÝåÑÁÉÙå)üùA\x001e#<Û¨áÑ¸!óÝKèL\x0017\x001eåU3O*,Ð~Ëca×ûõÇ_©¨à[ú<'"%ÒDÙ¤¾<F~úRßQéÊ\x0005~±zùÊ\x0008¾\x0005®ùS¦²B!UúûZ.0êÓª[àòð\x0015e¾ÖZ[Î\x0005¹í¥jàÊÃ\x0007ìK!\x0017üwî¾»A¬õõý¬p:½ø`~XJÐ:Öä\x0004Àì«Ëÿqv¡¯.gÂæ¿?ÿþ+õ1KõúzsR\x0000\x0002\x0000ln®>ýÇÕçÿx\x0001ÿêÕÍUÊ\x0017
\x001aòiÒÒÑ¤SQ~}T\x0014©??9ºø£×ÿñbuñúèäèõ³×Ççg³\x0003¹FP9sU\x000f%pÎJ÷_k0\x0012M\x0002/\x0003M	ó\x0006^lµ\x0014*g³Z ¤IkÑ\x0001
L"üË\x0004%è4Å\x0005P9ÃÕ\x0002\x00052ø,)ð£Rå\x0001ZäÑ\x001bP^r)TÎzµ@aY\x000c	Êç:-LPÔ\x001b\x0004\x0015õR¦\x0008ka\x0012"áðÛû|íÀÚ	¹¼\x001a \x0014\x0005\x001e\x0016@åäX\x0003\x0014*\x0000©\x0008Jg»\x0007´|¤TX|ÎsÂ¬\x0005JÙ4\x0007\x0000¡à\x001e:¢Ý~\x0008e\x0016kDkú|yÇdTÈ\x0013<ðóyþ|ZøPYk¢
¬§°F:ë©\x0010£.*A-=TnkRTÉÎT:¿C*Ç\x001fPS|i\x0001\x0015åà\x001a\x001e\x001a½6YS¥\x000eÓ¬©fM%£]ª\x00158/×"+\\x0005Ê²R¹\x000f³>\x0014Y->%Úô\x0002V>:2yÍ8@9Q\x000e»_ªÔ¥L\x0005÷x´ðÏ-ê\x0001gPn\x0015i~\x0005%\x000eÐáØwäÕgõæÃÍ¸ÔæÕÍz]\x0007\x0015\x001d\x001dyðbTNv{¬\x0005ÊVÆÖÝTX\x0008u²ZÕ`\x0002§UÊrj±$<Å©\x0003m>Ð`2kxE\x0017\x0011ëé\x0017CR'%+,t­Âê©tZgMÂÊS\x0000\x0001+Î¢ÕX\x0012KëÓ&.m(¯\x000by><&¶,}Eíg4×C\úý/?ÇÉEDÏ¦ê3:a(¬®Î+Ê1¶Ê»vr\x000f\x0016º;5\Ûø´¸¶W±\x000bks\x0014q\x00020Ë·Q»9Ã¦\x0005l{\x001d«Áln¶H\4\x0010\x0016££Ö0\x0017¹Îí\Ê_Ýü28`¯6ëwi<ÅÃ§Þ¼2\x0017´ò&\x0017´\x0004!\x001dYÌ\x001aþßÌu|u¾úæhPg:\x000fOW\x000b\x000e\x0014=\x0004u\x0015\x000eMfÊíäô¤êò÷k@²Qä¯\x0007¶V¶i¢£O§3û*>\ö¿\x0010Pö½\x001aô\x0008¦á'É\x001e
XYÄÍûÅ')û^OHJÙïz:@ìsµ|7é»\x0005g6\x0000\x0015åMµQqFW6vnZ ÀH°*C¹l¹ÄHYDm¤Qá\x000f õ»\x000fïß\x000f\x0014åÅÝýæÍu¥¡n¼bÃE£A<\x001b4¿,RÍØy\x0017gçÏ÷Øê\x0003°¬,ÛÀ b,PÖ.W\x001fàzáÈ1+'\x001f\x0001,¿Åm`1PëÆ.\x0002>dp\x000c¥8e\x0011XÖåM`V\x0005\x000eÒªÀq¢\x0000\x0017.®#]ÄÃ|m\Z¤\x001eÜÄ¥r\x001er9Í\s®D\x000bX~kÚÀ¨ë
ÁÀ86ùì;\x001f9,Å#H,¿9m`V¤U:hVIjûG°@f;\x001aËÁò»Ó¨-4e 5fc%mQ>¥5½òÏß7~ûy Æ^®ï7W×Uf¨Ä\x0014MGL9%óÖe\x001fMy¦Ýl,äåêòüèxÞ\x000c\x001d`e%ÖmõUÄ\x0015±T¨ô¦h Ê\x001a¬UXd\x001d;¥ò¢&\x0014/²ZNÕW¬¸!H9^w²¢Ô¶vÆ-ÿY{µ	ËQr\x0010°h\x000f
+òÉ²sv{\x0003VÖ]mÒâÜrX\x0018CqR.\x0005ó"Ìh\x0006¬¬¹Ú°Ü!}Ã\x0010s\x001bqú\x0004\x0015\x001f\x0001*k­6(Ë°\x0013Ut¹
©øÀ{ñ\x0008×0ÛÌMX2­´D,/l^\x0003ë£ö±¤ì<Yá§\x001bç\x000eÏÝÝ^\x001d¬6¯?­o×7W\x0007Ï¯6Wj£URö	çpî\x0010ìÖlUè´Ît'æ\x001e\x001d`\x0007óÅêt\x0005þþó£ó£ùÁ\x0003léÑàÇ\x001fÀ£Ð\x0012Ø0n³ëV\x001c\x0013\x0011ÝÌg_\x0000O\x0017þX,qM\x0012úkÏ8
\x000b¸±G\x0003,ãvX\x0015¸ááK=Ù!½\x0005[ÚóÜÏG/ýXÄ­\x0004U\x0019ãP\ºÜÔõ ¥ó4\x0016co\x0016þX\x0004\x0013DÓAQÑÎ#\x0000÷Â\x0003ïD=ÒÕ4ëÖ_þ\x0018F{×\x0007çW·ï*­F#8Õh±Ë(;&`*f××ÀË%¬\x000eÎNgç\x0019À(ÜûôÀ(ÞûôÀ(ÞÛ\x0004¦\x001duÊi\x001b|^\x001b\x0008`z\x0002ÁÁöÁ¨º	L©\x0002\x0006\x0006')ªw3ÆÍÕÝ´Qgu\x001b¥Î>=Ù5ÁIÇ`f.5Ô\x0000F\x001d×M`>mÉgº¯Ñã\x001c­	³±û\x00060êÄný¹Î\x0017ÎX¤\x001c_°úQáÍ&­\x001e\x0002ûEoÞÞù¡\x001eÃñ×_6w÷ø»×IÍbý}rÍÏ\x0007ÌeK¸¼h.ãñbõÃùÙ%þM\x0005`I_5\x0002\x0006}(l\x0006ÄùW:\x0003FËÞÍ\x0018á­%Õ\x0008\x0018#ßTÌ±i
9N\x0019íËà6ñtV«\x0000#«0§E\x0002tØ²ÃIÀù\n\x0013`\x0019\x0014Ñ\x0006h¥ \x0006AmpMæS?°³k[ùÊ\x001cF>\x0011i¨Æ«¬)@ªB\x0001«W«\x0002´Æ«zp_]}¾~[°ôy2w`aÛ{\x000b3â*Î¦\x0006^\x001fwº'c9\x0000£L\\x0013\x0018z©T0ã¨'DQªyÔ^iáÊ'®\x000b[ÿ¸ÐÏr,2:_\x0012\x0004aæam\x0001£\x001cX\x0013\x0018§£\x0004\x0001è\i\x001bÓ\x001cîösñî\x00160Ê=9X\x000bB\x000e 2÷s¡È¸8Y¹¹ÙBFµÍd"\x00162\x001bL\x0015²\x0019W¦Sv­ÇOa+	´\x0019g{¼KÛ5QIb£&3¬0¤ðQÀ¾ Vdvæ\x0019¨\x0007h3§\x001fOîÉ\x0017 ´Þ¿Nhï¿Ú±iyr³~³¾­}6á-÷Ô9`¹s 8ÚÛ\Ü\x0007Í\x0013ìý8Ýój\x000eðaÙ\x0007:ÖR¹©¹ù\x0010³x\x001f(?çoÄ+fe£ôò\x001a^2{µ%éÑ@73_¨ÑW¬Ê6<S\x001e+ð_¸Ë¹R.ïçÌ\x001a¼ß¾_7?
Î^ZS[ä\x0002'^$$ËuIj±\x000c{,-ÉÙS0 ÊG®
ûÞ)Á¡ÐNËÑG.ásn\x000ccU\x0008+Ë'­´¦o(\x0000#Si\x0004\x0004¬à¥D£M¼4|Ãì
´Qåõ¾å\x001cFA2\x0016¼h\x001cè±\x0014+G>Z°\x001cºðÚÚsØ4Ï\x000eE¬¹ìz\x0003V6hÚÑb«±\x000bã|¾+\x0006.ðbi©å\x001fÑå>\x0003Çù?	¡}üòN~y?~Ï©\x0019¹Æ\x0005v\\x0016\x001bmd\x001e0wü<Ny¦,v¾IyDµ-o®¦\x001a¦µñ\x0012ÿè0qd#Î}Ê\x0006¬mus½°båBj4r*Å\x000b¸Y$Ì\x0019e
XÛÚæZ,\x000c¤Yz²óÖ\x0015
¤=fÄRmÀ*! \x0006¬À½VH:A³êàlÍõM6`ÈO=wÅ<#\x001f4ÇEã#\x001eù2W´álQe*\x0008ËP´,,¥öÔÍWRa£
\x0017ÑÑø_\x0010Îó\ð"rJ@î«¯¤*\x0013Hÿ~ªßßþvó«\x0019Fìx:ýó»û*ûY\x001a-¹f	ß£ü!#®\ï"ÅKÉê]Î[Ð\x0003D*ìoFTÂ2\x0013+s6\x0016§t\x0018®È«8n\x0005Ì\x001aö	\x0003Rôóé\x0002R\x0018ôé\x0002RãDû5\x001e\x0007e£äj5o
\x0017ÑÉ¹dc3"µR´ËPnk"æN9+hð·vv.QÛHAåv)ªT¥¥(è-\x0003)rÉM\x0011´\x0012Rt¹]*Òk\x000b\x00071ÕM&!*¡çÐJXÂÌ\x001dB´æSÅ¥\ÊHsqfF\x000e8·Ñh®Xr6òX\x0013«)\x0019¤3\x00199ôÜ!ÇF^cÈ\x001bÿPV±\x001cçÒÍ\x001cnfÔB²£ï\x000cU~ùèDào=Ómf¤ÖOÙà±×\x001dç\x0011´
\x0015f·BÀq\\x0011êæ{\x0004«\x0010^¿ùÃ
ÃëOë7W×7\x001f*\x000b3àðÈ\x0008\>É-9\x001cÄ4bî3Ã_¬\x001f\x001d|¿§fd\x000bGÑÂF8\x001dËm0&@\x0015SÅz3Nd\x001b[6¾ZÙçÎ\x001c\x0014\x001c;GV\x0016W2Î¼ymp\x0014ÏlãË\x000b~®a\x001fÉ\x001a®¶\x00113îd\x001b\x001aÅ4[¿i(s7à£Z.\x0013[dæk£Ðf+à2%\x0013]ÞÙ¥p¢x¼s½0mp\x0014àlÃ¡\x001b\x0014ê\x0001Ó
Ã+\x0008gxZ£3\x0003ÛÐ(ÈÙ(7Å)8ô2eäz8.;s­ìmlÙ´zJß4ê÷?ßÈqDñb}s]\x0017éT^à¢Ôd\x000bv@þ¢ð4Ð
må\K+¸ç\x0017«ãùPç\x0000¬\x0004\x0015\x001bÀà{fc\x0019WS
\XÜ¹Ô\\x0013]\x000bW*6pÁ·ô\x0004\x0006\x0006¨!0Ep:\x0015\x0014.\x0006+qÅ\x0016Y\x001aò$f%K,\x0016ÍGðªÁJd±Eb\x001aÂÓ#¦b\x0011Ør¬\x0012YlÁrÔ	°È°¤0\x0000k®¦«\x0016\x001b¸g7Ñ\x0004WÄe83b¥\x0003V¢
`2pC\x0003®Jt\x0004&¹\x0013\x0003·×/\x0007+\x0001Æ'\x0001ö§Ñ×··X\x0018É»ôãÅzóÓÝý¦\x0002ÍÆ3ö
i~\ºÐp	Gg7×½òbuþíÙåy
\x001a®\x000fI?
Ú½öö·áôÿþçÿºüt}[÷\bû(7PKZc¹Z:;WÕppyq|:ÿV\x000eÀèIj\x00033§p*\x0011h`[ð«A¤½õ`ô&5CBÆ¢éÎs'Î´Z\x000cEïQ3\x0014\x001d°\x0001U|D*z©¬PÉG)´?\x001a±l\x0019ðÞK"\x000b\¿.ý\ì­\x0001
#1²ùp\x0005°x\x0014Oly:8Jçé¥ÂÍæà\x001e@\x0013¿ü®ú4éÿºn0¬­ÑôV&\x000fØP"Îñ\x0004«O{Îñ\x0003õ\x0000oÛ\x0005Ö»=8{©Ø)qQ\x0012=Ë\x0013¶ám{ÁÚ¤\x0017Jq[\x000cy1\x0015Þ\x0006[¤ç÷´ê4àm;Âð´¡aÕ\x001a\x000b\x001f\x0018\x000fu,9³¥mxÛ¾°6é\x0019ªàÅ9W\x0006ºX1f\x001bNÚè¶ÍamÂ\x0013<f15Nðt\x0014É.çlºnÛ!ö\x0014é¶mbmt U\x0008ÎSØ\x0019\x0007ËpXm¶¥
,Ýc'L9wüP\x000cTÞÜ 6<NÑ4óÅFõÆùw\
TZ9õìÏ6>^\x0005ÚÌ§©L\x000f]<2{q)#\x001f½¹¡»x¼(´\x0003\x0003làÕp)*GïQÞ³É\x0004ÞfHTÇ\x0019R¡Åuh¬õl	S\x0005¥ÿùÍÇÍ°òüî-­[øný\x000e0«\x0010cÚ%.!î\x001eå®*ðäT=§aÎÏ^Ð&ïVß\x0000k
g¶\x000eú8á
¦ø[Ä©\x000cy¶ä©\x000cðÿ=óÁ{8³ÐÇk\x0013óô\x0018,G%d)\x0001nÎé\x0001Í\x0006C\x001f(n\x0000ÏV0%-#_!\x001c(ñx Ùtè\x0002
\x0002Zà{SÖLP\x0012B¹p\x000fg6":\x0005\x001a¨qUE§é¶@9\x001e\x0015g+ù{@³=Ñyå{8W~þéû8iô¾»ßlÖsm­ Ñ\x001a\x001aóc\x001e\x001f_zøÜÜáÄ\x001eÖ³ËóóÕ|«Ð\x0000nÛäý\x0004á¶
Þ-p¸JîdKog³\x0002K\x001f\x0003nÛÝÝ(¹¾ÁzmpÛÎî'(¹m[w+Ü¶éÜ¨¯á\x001e­áÛ¾ªæ~C\x0003Fw$Á² e¶\x001cª\x0002.ÜÞ|\x0010#+gýóº²äÄ\x001a\x001añHªÁ\x000cÁCå\x001cç«ÿ±/ã\x0018\x0010=SM¤­¦­ò¸(?\x0011%Ø§½+µ¯F"Ó¥\x001e	×[e"\x0019iØSd\x0004h¯æÚöªÈD©\x0006R5à÷\x000e8\x000e>WáPê\{mÊú$yñ r8C& ÞZ:\x0017ºNÒ;ÿÓ\x0007õæÇ<ÏúYúñûõæóõÕ&/({»¹»ÿ£
Qà> ­DCöðà³4·Næ\x001f8êè<?ì/ÎÏ.ÿóa`@þñ
^Ç7½Ä\x000b¬nâ·Hüöÿ?ÄöÇ5Ôuÿ©ÀÐ\x001b­\x0000xrT ¹¬F¸¹\x0010M\x000bñ\x0017ýStRî\x000fKïðÇÑ§·ðÜÝßÖõ	\x001b]éÒ\x0007\x001a¥3\x001b$+Æ0\x0017\x000c9ºÀ\x0017äìòtßÜ·O··7¿'@\x000cÖàÕæê¶\x000e
.'m2jê\x0007á¨¸Ri=§"WçG§\x0017³û\x0000ÝÚþ|·\x0019¼º-£ç¬\x000b´¡]	ð2i{[4ä%ÑH<jîA¬í\x0014È\x00160\x000fª2ËJ¼.zN Òh\x0011æ¦4ñÇ''1\x001eãØ\x0004æ=eÿPV5S)æR\x000bõXeJcÓpCÍ\x001dóJ¸´[5uér»4ÀÅC\x0018Û.òx(\x0019(Ó"É`àzÏÕ;=\x0004výáÃ\x00177®Ülþõ¿7uNµ·7§¥
;Z]¨¹®\x000eL¿¹NØÕ9=Ì%ÑÊH?ÈÑ8¾?çöOòzU\x001c}0[ð·\x001fìÝýÝæãÓQUô[W}K)ØÔJÐ\x0000x,¸ 	Õw\x001cø¯\x001fÆÃÅÔÁ¶óÉXJØ0 hr±w\Â¦öôz¶ðìBü$\L\x001fnGW4\x001cÛ
.Í³ðRa~úÑÌ\x0007(÷\x001ayç"àägÍ<a6­Û\x0004ÿô£\x0019\x0010î\x0003	\x0010§çf¯\x001a§ss{­\x001a\x0001Ñ¼¡\x0003Ðrq§Ã·æêkÁ
2F>Æ\x0001\x0004\x000b0\x001d|
=#ò±¡QCÑDÏ>¶ëÉk\x0003Ô©7F7\x0003\x0008Ö¤æN-öoñ_`Çm¾v±\x0001\x000f}+iMüò\x0006tñÁ¥\x001b\x001cx¼½µûBõ¸=ýhW1Çck\x0011-°ÃBln-Ú;oó\x0001Àû÷V|~*\x0010ÇD8ª:®\V\x001aâzY-SH\x0016MT­O8?w;\x000ep\x0015Æ\x001cÕï\x0016\x001b=*gip¹@'Ç6\x0015Û\x0019üZò4\x0005açG\x0007g7ëA¬m´ Í\x0017<÷\x0013,Ul9É¾àvGâ¬.y\x0000ìúÝ¯qóóÈe8Yÿzõ¹Î«\x000eAóª(¬" EÆwÅÁµ-^yuôzêî\x000faÉæ@ú¯-k\x001bißÌ\x000eM7eûæÜ\x001aÜ£´¶ña¨íËZ*\x0011Á\x001c¡0\x001cRFáé4ue\x0011ÔpÇe¬\x0004V&,§i½\x0010È<>xíç7îÅútûîýýAä÷åÝýõÍÍú\x001a\\x0005\x000c¼øpõñú¶ò§5 e\x0015÷p\x001aÅ=ÏÖÎ!/Ï.ONVÇà6` äÅ÷G/O\x001f\x0006\x0006ï\x0001þX\x001cMipR%ð2pdÖÄ¹¢®6hãnÞ¿\x001d\x000eCÉ@e{®®ÖQRÐ1¸¸]×>·f8ÿR
\x0014õ¹7@)ÃsµµTùUHèxÆ Ý=W
ÅãRë¡0&»Í-ñl\x000fë9Ebf÷\x0018ÖBá®\x0001¥Û¨¬å\x0012_8X\D\x0013tiùYË\x0004_ÅFI\x0005\x0004{eË\x00165Wz5ÍüÀÏJ*\7£Û¨\x000c×\x0013Ku[©13\ÆÏECª¡À\x001dfe\x001bTQ\x0011iæ"×}X\x001aÎÙ?õT`YÓF\x0015ä6SY¶ºÙR¯\x0001/úBªT~´+\x0010\x0016Oí¶\x0012?fjIÐÛñs½\x0012ÕX8U5ýh³Ô\x0016¯­\x000f\x001c]¶¾\x0014²Î%7w?ßü:!qõeÏz]5»ÄúÉL&#>@96#¹0\x000c÷0Îýp/ûé¼ýñÏ¿½\x001f¦¬nÑÁa	PöØ#\x0015²c/NÙé6÷§Öü
 l,Ö\x0003Å\x0014	\x00087\x000cÓ3­¤fÄTËó§
\x0002Jéì°¡ãÙDtsJµ0ÙDx"09èØ0´Ep,\x0005~\x0011¸ùm3c\x0017ÔòP\x001a§~Q¤\x0002à´Ú®NÊ \x001e3£'ky²Ò \x001fÃ}±N¥ÍY@ÌBùä:îz\x001ep,"\x0005çÀw¥:\x0000¥ËçZ&\x001eV
Ój\x001c\x000fwÂéS\x0014­¶-rçæÂZ"ªÔ®'ÂÝR@áikxøf\x001ao¼\x0008j³ë\x001c8Ë¤ÁåÊcä£µ%êfÞØZ \x001aÓ0ÑÅð\x0014$§y¶et¢Ü1±ìLó<z x¿,_2Oû/¢åÍíB¬\x0005¢á7õ@ÞñxY\x0004¢fx\x001f\x000bOÏó\x0015¯B¼¹\x001b÷«½¸»ÿXÙ=\x001a]+Ð£Í\x0012&r #ÎY'+¬'{9ox¼gÄç_x\x000e¿À»ë?ÀKÿtðíÝýæíÊ$hBRSµç\x00108\x000bÐÎæIõüìø?ÁG¿8À6apÔçK\x0018
¸\x001a«Eà÷Ø(´BscV\x000cÂqTDÌyïèz®\x0017¡[Éì¸@ÝÒ>\x000e\x001aÙþâ>t3D7K\x000bU\x001bÍëË\x0001æÇjã÷tbö Û!º]kÊHUÍã\x0003¢¡d\x0011s\x0006]'¹\x001b»eBtÒ¦vt\x000cr,Ííi£ë!÷Cr¿Hæ`\x0019RþE£ø©<¤¤P+=ìD\x000fCô°ø¤;:éßÞÁIwq~ó^\x000fz\x001c¢Ç¥ª1~\x0001+¯AxzOJô 3\x0010=Gb©Ø5I'O¡Ô#ë=]=èãtñSêèÄà \x0006\x001a\x001aKÌÛ?î£ÇT.zMu\x000c8Xõº¥Ó®¹F\x0018ôúã\x001eÑk*\x0017=§Ú\x001bUÙ#\x0019xAé}Înïd\x001f=§rÙ{ªeyOq´-évÏ	j3_\x0004ÓyU\O.ëzá·ô4iÏùu8çE?;|¿\x0011?L
ß\x000cßWw·\x000fÞÝ\x001f|{µÙ\_mêR~¥5Xù2ì1*ËæsnÕ«³Ó×\x0007ß\\x001e|{t~~|tþ0®\x001aâª^Ü@)y\x0015à2$åøC87®·\x0015W\x000fqu'.øòÔm\x0000jûPe»\Û\x0008®Ð\\x0000½\x0015×\x000cqM'®K3t1mî¸à!ÓÂÿ¹\x0000v+­\x001dÒÚNZÊ³2TÀö ®ç\x0008E\x000br5Óº!­ë¤\x0015ã§a{\x0014Àç¡\x0016æóN¸B±^À_\x0018í\x00088\x0001¿½2©¨\x0010@Y Sk¸Zòáùì'à¼?ª¨ª\x0007UF\x0003	3j\x0019i6.gTÿàpì:T=DÕ]¨!òµ6°n¸ÀÎ9w±Ô\x000cIM\x001f©âiÞ\x0016[¶©ÚÓ±èÄ\ÅB#ª\x001d¢Ú.T¯9ôn}¤Ì)8²eNÿ£pº!§ëâÔëV@¸Ô
gpâ8IT>\x000e©\x001fú.R°×iì\x0001¢zFµåãÏ
nD
CÔÐª\x000cgìTéÁf+Õ¹Åµm¨q\x001a»P¦²\x0003eq©§æêK"svy\x001biq?³ò\x0017}¨ñw6D\x000e±m.BÎ=6¢ß©®
kZ©µÅFSE2«*£èçz%\x001bYG\x000fì|©,
VNmKèCÉ`èY\x000b uôRÉ¾§êß%×Ñ[%»\x001e+4V4åT)#\x0008uÀlØ¾U\x0007üøf¬\x0005Þt)×PlXÚÆ
ï³«Y+SK»\x001eÓ®»¬/Ç\x0000\x000bG,DpMû¼]EûFj;qeñ÷À®¨¿¦*Ëõ§Ê-eËè}å(\x001aÀÒæ ;GúbõòU*®\]Ì\x000fA) j\x0008ª:@]H\x0015 ¹C©à\x0006n\x0007Ì¶pµpê!§îá\x0004_P@/\x0018ÜNF"P3\x00045= Zòp3c\x001d¯«ð\x000bWÃ\\x0013a\x001b§\x001drÚ§Ëéþ	rªiðJQðjó9¯xYyûá®ª²:MR-®Å:\x0017ÞàÈ°Xb:çT¿Îk^V?¼øþìôa`5\x0004VÝÀ¼z@[3W4\x000bÅøÌìÖôf`=\x0004Ö½ÀÁóFQ¬·W\Ê-\x0001ÆÌé«v`3\x00046ÝÀ\x0016çÃ0p1\x0016Ênu3_ÝÌk¼¶7PÌ-ñ
¼)¤*\x0002
cµ\x0002»!°ë\x0005ö \x001fh©v<LÒ2àw6¡Ö\x000eìÀ¾\x0017\x0018+"XÂ\x0011óT[ç¶q¶\x0003!pè°æ%ì åÂ6\x0014%¡ã£\x0001Ç!pì° J(ÍËîãÙ$¸wø\x0007éUEþm\x00171¼l<\x0011Uë²ãÊ)ùèjB_ºî§\x000ecL9\x0014\x000f,3fçv°´\x0012Ë0Rlø·ÈºÌÚ¶HÜ9Å\x0017ÏÌ\x001d"
w\x001di\x000büÎÃáyÊ5pFÇg£èåo´Ò\x0013+\x0008~!MD»z8#¨\x0015½sI\x0013!@mðÞ\x0008mÊ"ò\x0019\x0011\x001f½À¤ÂK
ô0§\x001arª\x000eNxÐÊÜux¡iDr\x0019k.ævË·aê!¦î\x0011'®7"LçØz\x0000ç'l¹ÆÌ6P3\x00045]ß]³c\x001cQr\x0003\x001a\x0018ëÁh¶ë{\x001a ¤­àÒ>øæåYPrnÐo\x0013¨\x001cÞý|ð\x0017:d\x001a±*+ß¥È*\x0016ÇÔñ)Û§VÉk&Á\x000eømÞ\x001e×W÷\x001ai¥©TBc¿|Ñ\x0007lÐåÎÈ¹\x0002öMÄ5ã©çèAX5U}°2âË\x0004+d²Å¨#mé\x0002Ø¹ÆVX=Õ]°Ês
p,í8À¦Jëåh5CXÓ\x0007\x001b\x0004·¡ó\x0005ÓVr¬Í}6²Ú!«í<²<y1±ÒhQ\x001dÙ3Svn
}-¬p*µã\x0017V`ì2æv¹õûû«|º®]Åë"\x0016Ææ\x001aYÞÅ\x0011]\x0019bÄ¬t~8_}wy¨OW³ÕõþGùÆÜ®ñçw÷Ù`yõ¯ÿ³¹º¾¹¿ùÿó\x001dÝ\x001e|¹µÈÜþYù'\x0012®Ñ.o\x0004S é2®ME·éÀ¿Qj4ON]fcåà£Óï\x0013îÝÇ÷·Wüç¯ayú{/¬Á\x0004HbÕ2\x001c¢dqty\x0003ÿ|äåeÊ\x0003à»åª\|¬XÃ\x0011²\	\x0004\x001b\x001e\x0011ÀwÃÂ\x0013M2I°
]$Y\x0013¢\x0008ËÃ\x001f\x0001\x0007ÁwÃ8±K
aÈûëA²4.\x001d\x0003ûh°<
¾\x001bÖÄÔ\x000f°Ö.¥E\x000b.ÃjÁÕ\x001b\x0000Ë\x0013á{aq©=æÅd\x000bl\x0010Ö\x0015É>.È½ý°8*\x0011ñ\x0012,­\x0001Ã
\x001cÄÅ3ËírXîËë¦Õ þÓÜçt\x000eâa,åÆñ\x0014èÊàç?äo_Þ~õ"Ü¬\x000fÎ×o-o0Ûó
D\x000cÒ¦W\x0000lnéé\x0015\x0008¤­d0;)î(Y=\x0007(Ü\ö ×Pù×sù\x00145D.m³Á^'VùrÇUoÃ\x001a*új,kSB#Uçt,î|P%ËÐ³~®¡N¯çÊ
ú©|\x001e¹~¼Ï8TßÕ\¸ß0sa5$m¸Ôç¥
k¨¨«±tÎþ¦Ï\x0008Î\x0006)gí\x0015kºkÃ\x001aªäj,Ð½!´ò@\x0001´\x001c¤diÉÅÒÊáXàÛ­t\x0017ÉyLk1×ðQ¨åRipMþ.\x000báÑò9ìââbén,n\x0014oä\x0002\x001aïI^:Çã±Wðw\x000cvÒo\x0003\x001b½KÕ`6²i3¦¤Ì`4\x00089i¯Å`Ô7Þ\x0008æSæ-K,U=%0'Ê+´X­rÿx#åIz¼f\x001bNù¹ýXÔEÞåìöÕ¶4	YÁ±²E^Á¨¼\x0011\x000c{,-i°ÜR:/X¯º¸øJâ äf¯lZNÂWÒ[ú!>
K^u+.²
Àä!qI½}vØ²M\
ôj×a8TOÀÖ¼É\x000c
0¨fU!ÆÐJ¾6O\x0008\x0008Ê[¥\x000e[ú%QäªùNÂë-h¬+BßÚ\x0014'Z÷Á¹WÍg_²°¬õ\x0015»Í@\x0013\x0016[ü)áÜ«æ³/1
\x001cÄ4ILi_$¶T[à¾\x0007Ý|ø¥Ñ©\x0002 i1Zäk{\x00149¿Ô>\x000bþL·\x001f~\x0015Ò\\x001c\x0000\x0013|È\x0016¢\x000bÀÄN×·
\x000cþ\x0003ºýð\x001bsÏ¾\x0000×Ñ¥\x0014Ô«p~©a\x0019ºýìröá[bÑAÖ\x0016|)áä.½8%E·ë}\ÏÔÂe\x0019^p;¦"x%¡ïKÊ?¯LL£å1² ÓÖ,äÙK#L¥æxàA[È\x001cRqÊS,X\x001a?Vª	b®jo\x0004Áçüa\x0008ì#\x0004\x0011h\x0002\x001e¢b6;Û\x000b®¾®\x0004hHvX½eä`¯Ïo 0ÄMðÜ@çö)så\x0019\x001dÿ¨aPiPb>\x0011\x0002Ã\x0000aùÑ(U[­\x0010\x0006ã\x001b¦òXæÍwt,c¶vü1L°}\x0010èN8[-	ë$'Ip\x0004$¡;!0tQw$\x0004z\x001f²\x001cKEÇRÇr,]ì@Åìë´\x0004J"È"	¾\x001bÞ9\x0012×C`´¤î`*VÊ]ª\x0002\x001bÌ®Ø¥_ÃÃ¥Â?j\x0004\x0011üÖ¢Òy¨4¾*E\x0010Þt^\x000eXJMå\x0003Ö¡å¯a8Ïä¶EgwJ\x0002_PyCÿ:\x0008ZÜò÷BÐv¿õràPöPw9þ*IXÀxö,ÿü[?N{ñ4.Æ«ú&:5O%­\x00198úì|(Z3vjMm\x0012ù{8þûO\x001bÿàÚ ó¹¿:¸X_ß~>ø'ü£W·û2RJª4ñ
h,è²§-æM¼\x0011ç íË£Õñéë\x001e¾8:ËD
¨(ãÓDe\x0015=³\x0016ÏÈ\x001b=0A©pÑ2(Ê÷4AñccÑ\x0014É\¡D\x0018\x0001²r©¤(ÙÓ&)Cip\x0019\x0002I¢ )±R=m¢µhC§ªy y¤ ÊÊ¨Téi¦ú\x0006N},+úÓÂv(Êó4A4"EE'])]$e\x0016BQ§íû9ÊS[7;åï'ÊO+Ú©(ÇÓ&ªÈ\x0017°¤[ATUµ\x000b\x000fUÉð4QHÑdÀ²dâ\x000eHÃXÎ-ÄâüNÛaw¦\x0008KÑ\x0017Ô®+»ð\äN\x000b\x0015\x0006ª4Ã²ªI:W¾áÒOÈ&Y9\x0006CMN±öÑÅ¶%ÊÉ
\x00021¸õÉ·yéÉâ¼N´ò¶AVªÌ\x0006iÙ­ÊZJÅY¶Å5"Và:\x001aå×Y¥S:m·Ðo?¡Û>Ïee¢_U2:MX>ÍÀÎX\x001e{\x0001ò',XV,VÉç4a\x0005\x0006Ë&,Z\x0001Xnk6È/tÉæ´\x001dø\x0014e\x001bËåg|(6V×ÿõíúÛaµÖñÇ_×>]aãÁÅz³Yï­|ÃäWáJ·H\x0001R.|\x0013z\x001c¥=~ùjuqq\x0006\x0017«óóU\x0005T6ÜÛ Dà\x0012Ra\næÃT\x001cÔ\x000b¡²áÞ\x0006%å6îo¹¬Í9\x001c#¦\x0016ReË½
¤Qv\x001c¿\x001fûÂK¦²q!U¶ÜÛ¨|ØÊJäårié(Aå\x001e«l¹·QYK\x0017ð×dâ$¤")¹)\x001bîmLT#\x0015¨x¶+\x0012Aÿ-ýxÙloDò\\x0013-t £\x000f¨<gÞ´^*¨l¶·QIÅé@ÖÀ$(c)d^fõ2±ÕÞ\x0002¥£ã\x001e\x0002L\x0005\x000ce\x0002ÁG]¨\x0012Ø<n£²)-ÉXTèFÁ3V\x000fÕ{ûùý&ï\x001fÄ\x0012æ×w·_ö\x0010ÁÓÓ \x0011\x001804$ÍùÀZª\x000cÉÈHyË \x0016-¿>;ýáaüÆÔóxÐ\x0004|ñ-c­iÏ\x0012JÈ/ÁÉ¯KxlH\x0013S\x000e^ò2Uç¸N±ÙÙÊß\x0006\x001epª\x0002.ìÞÈâ\x0011,\x001d#\x0016áä\x0007¥E<iTY\x0016¡%ÑYn%\x0010\x0013®'«í\x0006\x001eÜóMæIt\x0018M<Ô<z	NV-8\x0012c\x0019ÇSW\x001bà(¾î0Y#\x000fÇ
\x001apô4\x0004áëtØ\x0002Å%@ä·\x00004\x0016j\h©
üj\x0001²v	\x0010ù¿
@Ûæ\x0018¹!íT('Úµ\x001f¡Ôûß®ÿØå\x0008¤\x001a\x000b\x001c$¾?\x000f*ó°$&Á¥@ØoÈ¥@Êî|8R\x0015É\x0005\x000e
+!\x0019°MüZ6¬d¤3\x0005ê@£RRæ`Gí6Ø&nAµÜ42ÒyçÚ®R-B|\x0004¶sPÍæSËk[`\x0013ÅÇ­îÔÀ61ÆkÙòØ\â¥Ù£
²\Ë\x0019'¡	mb\x0000×¢©nÄ\x0018\x0002WCc\x001e>én\x0013¸\x0005í+³Mr}/9Êã:Z\x0011Cï'ýEø\x0014~O%5ð=ñ«ÛÏw÷·ëww÷û´\x0017\x0018hÉ5\x0014Ü\x0016}äLu\x001cö\x001c¾>»<]}sv9\x001c°Àÿ\x001cü£\x0005\x0007hP{uyÎ\x0007.9\x0017\x0004£ÇõÏm,\x0018YÆ?jY\zÿ¸#ZÕsæâ\x0002Á au=\x000c(u©J\x001bqÖ\x0005ZÐ*\x0000ø7ÆºÅÁ-Ã?ª\x0005çü§f¼4?&\x000bQäØsªa¹ÿéú>³ð¸»Ï×p±>\x0002\x0011Þ¬o\x0001kÇKª\x0003ÂÞ±T[z¨Q\x000eôäìõ1\«@÷ê[Àó\x0006dùõk's¥¬\x0019C+fJõÃ¸É¦\x000f-?~íhöjç\x001dM\x0013D²Ò½hÆ¦U\x001fZ~ûÑÐ¡\x000fjS
fb£M\x001dÀ6	nö±eo¦
÷Z\x00127ã®¦\x0014ßé±Þý'øG3\x001b\x000e[Õå\x0006ª\x0016¥GÉ\x0013Y;áÊ-¥Û´\x001f8ÅÆ<æt k\x001a¶µ¬\x000fÕ\x0007é$\x000e/~&qfq+ ÜÆ4`3\x0016êlrýÔ½Yr\G.¼\x0015l i1\x000fÆ§\x0004EAAÖu_d	"\x0005B\x0005\x0002$\x0006IäÓÝÆÝAÿë¨Üüî\x0011î'\x001298'ë\x0016»Í*¢EåG\x0008ýs~¬"Ô­þÃ\x0000*ñëuªÙ\\x000f¸{
³zEz
\x0017
Éj»¦ë\x0003ðc\x0002øqÀ\x0005\¨;­X©©ä+k\x000fg\x0018@-ý-µ³ÿ6\x0000 GTùõ\x001a\x0013uÑq_¹Ûï\x001aþëL\Ë\x0015a\x001cÓè¾_Í¶)>G\x0019\\x0015q ~	=#öe­t_>÷Ýt²V¿tðÕ¡\\x0003>0g9üEZ\x0000æñÆ3<±ÒñoWGs
ðÒà9ÃÃÉÞMqu¨Ù
¯\x000eè\x001aàÑÎOGÀp²±­®µ«#º\x0006p2â*b÷\x0016µ¬:JôÊ¸ä\x000e\x000cWGuýáazUì´Ì;Pp\x0016\x0012¿2j¿\x000b|Ë¡]\x0003@¯)õª¢<¨Á\oü¿\x0007ñEt^î9\x0011ìÏ6®¥¤éóTè\x0017*·E\x0004\x0019JÿAeÑ
ÓÈþä|ëÉï´7\x0018k\x0012;Zê¿sØ\x0007DýwûïêòT#ü*ûKÆS¬i158ÿQ2¥¹ÆÖm,`²oÙ\x001b\x0012TuÍýtLQ\x0006¤:×Ó\x0008&¿¹\x001fäÎä$yÉhbNJ
cÜ\x0003\x0015]é®S#Àðkï%7\x0019a+F©\x0018	M¬©	\x001aÑP¾¾¿l\x0002U3¬\x0014\x001e\x001b6sGr9(çG\a.`¶ ÔÚ\x0007eª\x00074ÜR¤ëiÿF0T9è
F\x0007LÙðµ\x0011Ô²#MipRcÐP7_4æ-\x000f*rãxÑ4b\x000c\x0016*a´¨\x001aIª&H\x001aÇ@UÃrÆ¹4Ôº×\x001bSæYô¿©µjqNvÄóÆhÍÿ0ÖRª\x0014*\¦3À.ÀaYËåËa1v\x0001\x0001\x0016<ÂÓ\x000c¦\x0015¼Ù	{-\x000bÈõWyµk#ÿú6\x000b¡ÛWÀlaSS¡\e£ 4R8¾ÊËåÜ&1¨­ëY\x0000g¥l\x0013 M>E&ÔÔ\x0004\x001e:\x0006£ð\x0010ãC\x0003\x001ev¸¶&ñ\x0011Od\x0001­q+ú\x0002`\x000fõ\x0007$4·F\x0007ZJ\x000e\x000cZi¥ÜêûÜ\x0017\x0010üuTüqN\x0019'~\x0014<Èd\x0016Ô¿\x001bÏØ«/I>ð§ñ×ÁÃËçùÞôéãËã¦\x0002ZîOHÉ\x001b/Êá\x00053±J\x001d^\x001eO÷¦ç\x0007g\x001bæç
\x001a\x0003'¿ZÐ8EplÎR'8Ô+éÄR·M#\x001cp\x0005ñWo86Ñ¦ \x001c\x0017M\x001eoÂn\x0012²¥ ºÍµ\x0015\x000eüaüÕ\x001b±Ô5­½ÄòLîÜàöV'jòF4\x001eÎÉ7¥£ò¹­5\x001dUA£Æ\x001c;ì\x001bï1ñzé	\x000b·#»¥½^X½þz;ËùïýÆ]ô¿ÜÞÜc\x0016ccÚ\x0002i\x0015¨þ\x000bn;±µ8m@ÕÔl-G½_\x000eß`î¢\x0007\x0018Nè	FvØ\E¤¹\x0004å\x00023W*\x001fca
X[À1\x001b²dÒ \x000bÁp¨\x001bW»`
c÷Z0X$Å_}OÉYjWE¶7î`/:J{3\0Ø¬¿~Cñ×yº¿óÞ¢ñì\x0005je}éX²È¦ÎI·^_?¥kó©·x´xCß²Ç]°åÚØV4z~wõÜ­+àôJî9é\x0005H\x0014n÷´ïÇ\x001f
¯+ö8¾;N\x0016÷y¥ëÞÁµñnÀK\x0007¼Mr­Ã±õ~4ªÅwTiÙ`U)\x0010\x000e\x000fÙh\9ïSô\<U¢pD9\x001b
Ëãë\x0019ÅV\Iï\x0006y!=ÚÞZ\x000fÓ:z*9»W\x0013n­¸\x0016³Þ
¸¬çZ®Â\x000eE3#¥G,ÑN\x000cÀµ\x0018÷nÀ\x0005j¡,tX­Ïª\ûõp¡\x0015×bâ»å5Zî\x001cÇ~'Ëõ\x001fv\x0003\x001b-®ÅÈwË1)7¼öNÑ\x0014\x001fójô®\x0011VwººåÚ¹\x0008ìê#\x000e&\x001b<?ÇèÇ^ûî(sËýoØE}ñä>¸sKÄ\x0003pÙ\x000bÇ\x0011È	LêëTñ`Ìë\x0019Ê%\kòY\x000b`ÝQØ¯\x0004Ç)\x001dFLç\x0017<È[%¶\x0015\x0019{{­GÙuúÝªrú^04\x0003#×ïÇ\x0013YÇ\x0011l\x001a²ä¹×þ`ñÛüÁ!à:^a£ä´fnÅ´µ´l\x0008eÅJØæ]¬\x0001w£´ýøÔQÿG¹x=ßÜñÍl4Îä¦9Æáv\x0013\x001cõ¯Õ\®^¬
p\x0016(J´Õ\x000fÆ>k\x0007
B/ý­Xæ\x001f\x0008\x0004ÿ
.6È8U\x0015fLF¾Ü\x001d³\x0006Ç:ß½+_oHnzBáÓ#£Qê\x0010K\x000f¤·j(Eæ¿\x001f\x0014\\x001fÊlÆ\x001evY3²û5×¤TæI*óþRaînl0s,\x0015î>#Ì\x0012¾B	r\x0008DRúæÇ\x0001¹N@®ûDðx\x00047}ÀüïJ;Ûåþ/ýõYt\x0002ÎÅ|Tùn^y³¥b\x0014Ã6,L \x001bpÃóÒ0?òë&\x0012K.9-½Y_@
7ßîî¯×°(<¼ÜÍ6êc\x001coÍêX\x0017>ÏPH8¶vÚýôòh²\x001dÒkº­ò"ïÉÈ7\x0014­²)Ê¯_é\x0008£DkZ!\x0005¢\x000b\x0001Hp\x00179$Öbý°tÂ´Ædu@ïg]#¨ ØÎãN-Ë¼Y-µ³Ò@Å«ßÄÍíÊy·§½ãûçÍ×\x001db\ 5ÚiZª!áî\x0007®¸­aåï\x001d\¬»ä\x001dTËÓd=PyÐ\x0010ÊeTÆ)È÷QasÚ\x0010TÁÜÝØû×z¢o\x001aÜzG±\x000f§q­\x0008_"
'ÝPåÃ·\x0002«\x0006Ì{ççç»åqÞ&RläA-·Ô©6\x0008Y5kÞ\x0017\x0019Â¡§\x0018Í\x0017\x000cNÉvº8\x001eX5tÞ[dàÎÒlG`©ª!\`-U «æÏ{#sóÕ.o8ÌCè¡ÔÅì*Î6d9EÕ\x000csgi¾fNóF,»ÄHØ\x001fÙÝ¼ÿ¼\\x000eÚ>ÿ 8F\x0007UÆ\x001f¼eJ¡hKA4Î²Æ	_ èÔ¶£ÐóÂb\x0011];S¦0Ìr
½/N	h+\x000c\x001c¤\x000868H\x0015(\x0001ÎO/ñó4À@üø«4<}«©ir½5·eÇW¥\x0019õ(xÈè_1XÔ\x0000§zNo0w.\x001có<½Áñª^\x001aÐé\x000f\x0003¯¶íy5\x0014~\x0019\x0019 í\x001c9ÿ¥?Æ¡ÂÀ\x001eqÛ÷fXö5\x0000|Söw¡W?í(0¯äû¢p4z	 \x0002ïßL-ù±º¹±\x0001EwNªï\x0015åé2O
ÝxE9#kÅjíÕ\x000bI\x0019úW\x000cAõGÒ\x001dnûW\x000c´5Éä*ÉäªLàë	FGj¼ìÌ
}2 I$ý\x000e\x0007©2r%ïrÈ\x0012ñ?H\x000c\x0005\x0002\x0012%ô;\x001bÜ]EKM\x0005è2âE÷\x001b/Y.£7Hä*I¤ïÑ\x0008á\x0014 wªÀ#.ëuÂÑ÷\x0001s4j¾Læ±÷!\x001eªIºóÿ\x0019ÁmHÔÓËÍ½YY(?Ý>Þn)ü­ÜÒÇ\x0005¥¢ääÛÒÆ1>\x001c\x001d®s\x0010;«Ñ} 
i¨*÷¶ì\x0000]SÊéh¹Þ»\x001dÈ
\x0019/»°Á\x0017IõGJi¹¦Ú\x0007d6>ÄD³NGvVlXS¿é©KWÝ\x001b\x0014îÀb>\x0002ë3(µ\x0000µ¦\x0000Ñ\x0017T\x0016º?(ÎO$PgçÊÓ·~MM¼/¨\x000eýroP®³oH¶\x0019Y$eì+õ4ûr{õ²:]ùáqþtõíùÿ½1l\x0004/WÒó³àÔP	Ì-<ökóq\x001fÎ¦çû¿®
\x001cÿ|ß?V\x001bÄ_ún7ÇeT<Ii¦@ÝÝÞ\x0018N3×=\x0004e£ùÚ.Ë\x0005¢òìHÆÒoî1¶ÍÝËûß\x0017xµ\x0002ê4\x0018õ\x0007$¹ZÐI\x0017Xq©Z\x0010uy?D\x001eBìLçb\x000cöTGÊ
zFd^+©\x0016@¢¾dIVBD!é\x0016)&Vúum¹\x0005PÇ¸ô\x0004\x0004qVî¼ØJó2\x0018ÈÚieWtµ ê´\x0011õD\x0004J2Ð¥Í¬IBÙ»«¥ý\x0000½üþÇÏó_Ñ[Â%êüzOK±)\x0015p,i"m\ùó1p¤c¯=¥³wé?¸ZõÇ+÷ý*ùk´Eñäÿ}³-·Ç>#\x000eñF¢\x0007ô@×T]éû
=Ô\x000b\x0000Øë¿z\x0000±\x0015½"é8íYXÚê\x0019Ì¾\x0008Ð	õ@©:S²vÊS®º\x0010Ù:\x001b±\x0019Á\«ç/ÏÝBQ*Äl_øYº\x001a"wªxQ*±öQS\x0001æ¤\x0017\x0008*\x000cõ\x0000\~Ax0\x0003§T¬ç¹·aøMÜþ¦BÇ\x0010~¸}ï\x001d¤+;»ÛÚÙZ\x0012\x0000¦\x001aÕâZJU\x0015?\x001cM\x000e¦{\x0007§ÇÇ'£µüs\x000bDD\x0002ÐÈ0×æ5\x0004HîÀ\x000e;þ1\x0008 \x0001\x0010N\x0012R¥\x000cq\x0001@\x0008\x0011K¤^Ý×\x000fÑË_AÜ'¾þzîyÿðòx³ÑÓ;ë4·`±®0TûÚo9î½?½<{¿Èôòÿ \x0018ßoõ·ûßR&
\x001e\x0010þ°óÃí|3; Â hPëÔ\x000fm\x001d³ß)/\x0013z\x001f\x000e§\x0007Óµ0îþüýóo0v}\x001eÍûÐå+ÁIV\x001còäènAØ\x0019ür\x0013\x000c³Oo\x00054º/\x0010\x001dhö_#Y>*\x0013ð Z\x001bqDûr#R\x0005/óÈzåa3)7¼fR°:$\x001a¦_©ü]÷\x0004eÅrº\x001eÅ\x0015üuR¾Hæïûu\x001fç\x0004\x0015O\x001bxÊâsp\x0007¸Ò;_øçë|ü\x0012ËÈ:¥ÇÐt\x0005M7AÃ\x0008\x001aÂÁ\x0000ë£\x000b%6î³_\x000fm]õ¡YÑfE\x00134ã
°JC\x0011Ô´ËYÈ%g·Qj\x0010Lt¡ù\x0016hðÝo\x0018$\x000eü¼²ÍCÖD´­Èb,6	ÍI\x000c1\x001dqÒ\x00134'ÊyÖ¦£\x0011«nû\x001e\x0001x\x000e]hªí¦\x0019ÎGáMSn\x001a÷­ÃMc 
ùqÎ3TÏ34=O<O§Ëy\x0006f}\<O;\x0006¿^-iÜ«\x001fæj\x0000wû´¤uñ'
\x0007« \x0017«[æ\x0017FX\x0013S¶Ko¶$½Y\x000b8-¸o\x0005ÅgË´\x0017r]\x000cBçtB·x«p0\x001eÿÛüñsJö½½\mâtWQ\x0002Ñ*ýRr\x0003%ÎÅV÷îoÓ³ãë{6¹Üÿûvpº\x0002§Àè\x0017àä\x001b}i-çg\x001a(ûvù28óVßýÛ'"Ã¿Ý\x0018zâ\x001a1
+lÌ}Á\x0010ü\x0006Åa¨·í\x001e\x0013\x0015þáÂÐ\x0017@Ö\x0013'\x0000\x0003\x0002±/³\x0003ìý4û<m"(N\x0017L/\x0004><_ÍÝÊ6ÚµóÕ{?M§Ë
¾[\x0006iD\x0017ä2i@\x001fð\x0008H×A«Õ\x0000RrÙ
­\x001e
RV e;H\x0013x&\x000cBÅL7\x0002Ünè\x001e\x0007T\x0015H5\x0000¤Å¬e!°L4PÚ»\x0014ó\x0000¾:îeÞ> qÑ$:{¤ñå¸ëZÐ ÕÃY¦#è\x00052°gàqt²iBs×£\x001cqÜRð\x0002>\x0002	?Èt?Ë\x001dåýÜVaûc^¹Ú\x0003·Ú.¸Iªg^÷c*´7f[a¶Ã1{Ï9*£q\x001d$å¶Ei\x000fVa5ùV;fWavcäÌJÞ`^Í0g\x000f§¿¥_CØÙWý\x00089»HÏ
\x000cz¤aV\x0001À³WóxµC\x0015ä8\x0002²Õ3W\x0019<Íwýd8ðVc6cÖ¢9Ñ\x0013
Å\x001cy_\x0003ø&4\x0017 æµ¹Ê­a\x0003k\x001cT\x0017rb0\x001azöªKÁÐø5üG)[\x000e7ÃÇì(I[0»·5äD´Ö\x0003­tv±y§fAòºä(Í(×zCÕ]¨z\x0018TSV¾KÃÁPL¤£XCU×\x0008Õt¡P
Ý\x0001ë"4-åUëçkï@\x001bTÛj\x0007Bµ8$/¥\x0015®çó;\x0011jè"
"#&Gïxá¸´©Qõ\x001aîÄF¨±\x000b5\x000e\x0014ª U®jdrP\x000e©vtU¥èBb\x0018VåË]5L\x0017¹u
gr#VYa±\x0012T©ÊdÞÞ£_Ã¹Ú\x0008µÒ«r bUö6&²ÚLß\x0000b
Ì+ïvµR¬r fÕaÁj¨º\x0014.a]ë\x0019´a­4«\x001cªZ5[\x0001lÉóUkÁ\x001avò´*Õ*\x0007êV\x001cð û
>®¦6*-ZÚ­¡\x000fmÄê*¬n # rM]\x0006Ä­Ì½þ\x0000U¯ænê«§å=-ÔþÌYë55óÁK(v`
Ev_¨JÕ\x0015*lÈC\x001dx6»\x0002\x0017°Gkua\x0016Á\x0015*\x0008ÆKg_]¡:ìß×#Ä%hª¦Z ¥Ñ\x0001fÒoxÁ02¿ÔüÔLWÈt\x00132!Ð j=O\x001db~c\x000c.Sá2m¸ba7\x000bÂSlæÉ$W×3Z¡Ù
mæ¹#\x0005{ì=·8ðYÊ1¸\Ë5áJ:ßÿTBË"+·Ì¯ùÖÃ\x000cù.j\x0004v%¡¬ëMnÐLuÏLÓ=Ãõ³¦DæÅ\x000eó²(QAæªkæ®òÛ$pg(mn	ç\x0003bÝÖ¬ºh®é¢!õ>\x001fáf\x001eæ	Ò~1º0æ¦ùÊ\x0006ø&\x001b\x000e`XÌxD&â)&Zy¾z\x0004¾é\x0011(\x000cO¹\x000e;ª§Ô/W¶B\x000b\x0015´Ð\x0004
ü$ITÝ;\x0010fhzÔÊ>&û¸x]n¹kÖ¹Å¢ú1È*Í\x0011Ú4§°H\x000b\x0017x¨SÛ©\x0018ó>C¥9BæÐ\x0011´¿ ©\x0019aÊÆ\x0003ßj\x0014´Ju6\x001b«²¨·C\x001afòRrû(\x001f-Tï34½Oì""ÂÙ\x0014ñÞ\x000e6ì²vÆ u\x000b²\x0008-\x0017d\x001b4È2ñiJ³\x0015e\x0013¸íÊÃüzõò-ÜÜä$\x0016¿ÒG®a\x001fÍ®\x001e^ò$¤Ä²yûav{÷éÿý\x0004_d=Ä×DÈ¦\x000c&Ó{pt%®}D\x0014ÐHé('G?MÏ©}4Ù?½Ä)Õõë
\x0011öçâGDX2Ô\x0019Q0¹¦pXBäÌ\x0000D¿ßÚgã©øJ.ïïæßæÏÏ\x001b°h\x001f\x0013Y\x0006`±1Òü±H° O©ì`y4ýûùôâb=oOßþt(\x0018ì¾I\x001fG·ó½w·ÏØ
\x000bhî\x001eîo^6`R\x0010\x0004ç±\x0019/.oÏ1
Kj	ÿDö©	ÓÑáôrïÝá\x0005vÅ\x0002²£Ó÷=ð)Ü\x000c>ZñaÖ.uW!_^¢/\x0007|Z\x0004Aøt.¦\x000e÷ç'§ï±WU44\x0006\x001fùÕáÖÙË×DÆµ\x000eYÀ\x0019øtRH^ÑÑà0
^,z|\x0004,¿9\x001cË:»üÏËµ|\\x0015&Üö\x001f-ÍÅ0P\x0003!%é\x0013¨4ò@y¯F¢Â­?øÑJØ<æ\x0003¨¬Îe{\
bH+hÇ}G òÊ·¡B¦÷Q9{°±P$\x0002	Í¤\x001f#Paç1~4 ò>\x0013´2g\x0000\x0001UZôe]\x0011¨%\x0006?ZP!\x0013}\x0006e$rf#(\x001f,\x001f #\x000f\x0010{ÓG\x000b¨4*4ëí\x0004iìÂé¼ôÑ\x0002	wekl!ùùyÜè@©(ýHP8r\x001f-\x0017\x001d¿ÛgP:æd=*¤#u\x0002¶Þ¦\x001f
\x0014ª\x0004Û¦\x0012°u'uÅcl}Îàð&:ÉøÿNQ¨1M\x001f
¨¢yÄ\x0008¯ºË½: Ô­|ÕÃ8Y)l\x000cH\x001f-\x0007È¹_8@05>«Ï¨4)*\x0015Æ]uÞôÑ$*p\x0011HTàl	²N²¨\x001e+*ô÷týs ªOÂ»\x001erÞ\x0012®\x000f¬\x0016´\x001f§«Òlúh²ÊîMdKCa\x0017ZeW¬²\x0019çÁ(4ÈªÕ*ëÌ12i\x0005çØ±n¤¤PwªV\x0005ùpò_Ê
()QPw\x001d§jÔ é®ÿ\x0012UyN2ª FÞuìM\x001fM^UÈ{\x0015A:
îv$µÀ\x001bH£Â4}´¼ÀàqÓnzp.«P\x0017%¿@\x001bGÞ+L¼¦¦\x0008Bä
\x0010 XÄV!\x0004\x0012j¥\x0013\x0014a\x0007ª0"L\x001fM·=^H'¨:Ñ/ÖOp¤_¬0Û>Z<+NGâ	ºÜD\x000fP)§Æ¢Â7\x0018\x001a½\x0018g(H¨\x0002½AÉÆÞu\x000cnÓÇ\x000fåÄ`z/}4êu%\x0015"\x0011-Á­Â,+"\x001b
­Mh´6ÿÚ\x0018\x001e3;oÓGS\x000cOD&¨\x0015d^\x00001<{\x000bZ8;V&ö2ôe-\x0017ËÐ4¸ì2ñ§eø¶Ë±ÁÑñÎè6\yrUnGd\x0008\x0005]xíòl`+°ù£øúý\x001f\x0008L$ö%Ì®ÍöÎæ__nçOt$Î,b°JUÉ7]TùªéùÞÙô?/\x000f§ç=` )N\x001fý`\x0018¤&ÈÁ(¶A,\x0017´Å\x00191Ã`\x000eÁÆ¾HlæéJ\x0002Q&·`\x0019
?$\x0012¡cÁ
Yúèy8ð¼T6$Òê7Åëe(ZË5PV+w (ìNJ\x001fý 8¡ØWÂMrZ¦\x000eÅRy%MbÁÓÛôÑ\x000f\x000bZ2/é²EæòNpY¢\x001f\x0005\x0013;é£çu1\x0001ÝÙ$\x0017pru~@Ö(Æ\x0012âàG£üoÓG?,\x0011Gz³ÒÃ\x0011÷ìwÀÿ\x0014¥ÖzmXx5}ô\x000bhÝÀráú\x0006ÏÃ°\Ìp,øTÿgäð`"=i\x001bkáîÊò
#tbµ\x000c8µÛóUC´O\x000e>®\x0011sVïùúZ7BÛ%»d\x0013\x0015kÏ\x001bW²\x0005\x0008o\x0014]`rì!&ç¡ÂeáôEU¹¨\x0008È£\x00058,#"Ã1ëtÞ:8îêwiq\x001f®B\x00177}TùçÙõüqCaÇzP8~Àè,aòÆrö=ºúÀºéñäÝt-±ùU|»¹Ý%\x0005ÚÝlïýìîöþv#¶¼¡°\x0014\x0002\x0019+\x0003[NYÖ\x0005ÜÑdïýäèðä°\x001fºÂ
Þ
/Ú<&Læ6\x0003\x0017ø<ASê]À\x0003À_­ð ¦°6\x00115åjÁ]²\x0004/Ú5»6x\x001d§lÀéRÐ&ËKmÓéú¢ÒÇÃSÈF>~Lx¥_
Þ¿ôt¿<~ûýã
M)¤ÙýÇùÝ\x0006=\x0002ÿnîîR\x0006õHÆã¬æJ°ª«k±°?=Z\x000bàÓ\x00177ûÇ·êØÝ=íÌ_~[\x000f\x0001T©ÈL
¾+¾II\x0000DF)/0\x0006ÝÔÄþäè|ïdzù·µ ¾Ï\x001f?ºïxJ\x0008"}\x001cÍöögÏ6)z°v4\x000e¯$8\x000byNÖ8Ð\x0017I1\x0008B®îÎä|orvñÓ\x0006Eï®oUrV0Å÷·÷ó«Ç·DY0ÂÆQ!,æÍ|¸f!r¸\x001f+
úþðdº¶éfüõÝýö8K7\x0017\x001d8ü8}Ä¡ççMG#
7¤®È­p6"²ª¬
G4ç|qºþh®¿ýùâè§£Ù\x001e^ÒkÚ\x0007¸V"ºu°³[eª\x0002r²H\x0004mkGr²WõÝmÑ\x001d4
GÒGO4N;ìIh\Ì¼²x½&4Á¹V4¿Ï¬üèr Ãør9½\Û U°Ö]~0^.7¶¢R	Ìvuá¦hÉå»uÄ\x0017\x001dD

búè\x00080}Î*\x0018Öt!"eÉ\x0007\x0018jÚ\x0010©¹R7IFÈ>\x0016
\x0018ùô^\x001egw[Ò\x001d´U\x0018Î;7Ä§Äæjð^\x0004³R\x0001#§ÞåÙÅähCÎ£\x000f
øÑO£Çä	\x001f¯À9gç\x0008_\ã<µâËë\x0011ÒfÃV\x0011:"ÂU2MÛhºmÊd\x00107¬v ú@¼þÇoó¯ßi$,
\x001d¡e}|]mÔ`Ù\x0005ÆºIW\x0005©$
Üü¢«\x000bõ|\x001cxûÔf\x0001V¬§\x00064Ð ÷Éh"\x0007¾V1hP4¾E6ê
eJ¬!\x0008ÀhS\x0012H#°`û\x000217öÆ\x0012\x000b\x0018«\x0018-`ä\x00084ØöE\x001bYú¡±ý4`\x0015©\x0011\x0006Ð\x0018>'çí`4
©
ÓG?4"UAòAá~Õ\x001cÈ<oh´ÃoB>ôÑW6¸â5\x0007¾¸V91öÂmÖÔp)ÐcîMNW{·ô\x0002\x0004f¼\x0011pd¾9\x001e©2ùæ4Kçc¸þÓ!\x000fªD>:<=Ï\x001e^6àÁà²ä<£\x001b\x0001\x0005kè¸¢[mK\x000e&\x0017ÓË>°\x000b\x0007?Z0k\x000fÍa· &LW´fef ?&´l.´ao"x\x0011ô,¦RÂtºmô\x001bzp\x0011,\x0001b\x0015\x0014e¾\x001dÑùôõá:yp\x0018ý\x0018
<\x000e\x001eî¯ÁÓ¾½Ø)Å~|¹ÎÛËÐ-1üðÅrèqpzò\x000eÜíÃÓõáG\x0007Qñ)\x0010D
{\x0003ý÷ËÈ§Ï÷³¤ð\x001eù¼\x0001pöô|»1\x0008\x001fÓT´BÝLlp¹K\x0004§d¬ÕÑþäüâpS\x000c°À²(ËôÃ¢TÞNXD\x001e{6È?\x001c	Ë+ÃÑ\x001f\x000b.8x«úËÅO¨\x0011\x0003\x0007ÝP¨¦0±X£\x001b¡|»Q~»KnkÚÑwïÏ>nLlpÅ\\x001a¤¯IÆË9ìþL(À«SÚ\x0000ã`;\x0002%Ò~Fñÿ\x001cÁ×÷Üe\x0004\x0018ÁãÇäóÕíüînÓI\x0019Î\$ÃMUÔ|e-µiãxLÕ\x001269Þ?\x001e\x001dmx.\x000b\x001cØ>úàP(7\x0015®¢
\x0003Üt?akÂñéö»»ÿê\x000b¨ÚðãèÿþïÿóÓì
ôÿõ|ïçÙÇ«MY}\x0017ÉñSÑÓ\x0014\x001c<$MF\x0018\x0017+«´÷Ód\x001fLÀ»éÞÏÓýí¸\x0014²f§&\\x0001'nhbCs\x0015É\x0000è¼L5äÒ\x001bÖÿ\x0014LâØ¤%\x001aXû¸Ïu{·éÜ4.ô¤â\x000e8¤MÙ9ö¹_.]LÁé:<Zt×â/ñm´\x001cFUAÕiÔãÇ-é\x0017léÍ>ÂÙ\x0003Ðän§å^V'z|y¶1\x000bÓÅ\x000bEªÿÍðþüì¾t÷Í\x001f=$uüy~ÿLûÀÞ\x0004. Y\x00027\x0013x¬!åv\x000fnk°²®~&Õ|<=¹ MàS÷Â7/ü`ø>ÚßÿqFªðÖ©êê\x001d|Ý<ÞÞoÀ\x0016gdl\x001aaæ$¤T÷¾îxZø?MÞ\x001d¬EuõòÇ7û°\x001c¾ÃëÜàçáÂVòb±[$åÌ²¡=yº¶\x0011£"f6f[X\x001ao\x0001\x001c\x0001o~Â\x0011¸íT\x0016ãX'ÙoîûÃ×_\x0017Ë2hWtN&!sîGó¬:­âF¦ª\x001d6DoibÞþùNê\x0000­LÐYqîÏ\x001e¯æô¦4¸°=d'\x0008ôf:\x0000.Ø	Jf¥7÷'gûÓ
jó>Ü\x0016s¢´HD\x0016è9ÿr{s¿©ª¡.-Å^jj3Á9.ðÈÚ3<ßûåðýÉ.\x000el4\x0000$W=¡TËÈó­\x00143 \x000f©¬!Óã*,}dw\x0016°Ìúb¡¥¢\x0019\x000b)éà¹{Xªº\x001bd;ëh?]ÿÙ¹·û ôæ÷|D­5­PÚÕÈ\x001ecÁÏoG,\x0015¿@ÍMO6xÏæê>yè´\x000bê1ûð8{ÞÜÿa0En«QwÒZcÐe·jé¶~8\¬E¸ýö½ûu±gmö|³±ø\x0006â¦¨!u
åâ\x001b8t+6TeÀ÷\x001bÎâÏÇ/_R¿ÅÖ¸ôÑµáû\x000f×\x000bµF\x0005¢VÒ9~6xb\pRb]¡vÿôìÝÆ:íwñi~¦ëUj3{ûö\x000c>°]ó\x0018î.òtN¾ßn(Û×.r&L\x0007dâ\x001a\x0001%T°\x001d­í\x000c>°có\x0018.ñ»½Éÿ:\_ÁµRß¦K,ñ?>ºå\x000fó'lÙ\x0014ý	Gs\x0015ØOõ&\x0007¢
7@æg¥W§ úù0=Ç®µÐ>ùxL{àRõ½[|ßGUõ´1\x001aÃ)+
\x0004 é¹{¯©)\x000e´±_YVÙ`Õ\x000e^Ü:mØEµØjÜ\x0002\x000c¢\ëµ\x0006sw&#\x0013tñ¥\x000fa#°µ®Îß\x001f\x001fS!%e¡©\x0019à\x0019×ølxVáÊ\x001aÉ.\x000c\x0017l\x0004\x0007\x0002\x001a]i$,èà\x001eõoQ««Y@Tv¥ÐùñqSýPã6°ZÕ&JÌmdÅè(\x000e¦ÎËcð|vö÷µ´\x000c\x001d\x0010þmÚ8Ó\x0003Dj\x000fRY;\x0007ÎïC]VBªÚ\x0017m\x0000\x0001g[·K\x0002á,Iû
\x0013\x0005ªààÄ àÏÙØ\x000bJ[¥\x0012\x0006ø_!\x001bKlX$\x000cj©³7\x0006'£ßi °t\x001a²*p¢V\x000eÄ\x0000ÎÉ~\x0018Å\x001eÁ\x0007Ê®\x001b-b`\x0010u¡½\x0001\x0004ü¹Ô\x0007ØïZæá_í\à\x001b½¶\x0004B¡ m½@èL;\x0003 ,Q£!\x0008KöZD1ôJÍIv§\x000f¤¡\x0012\x0008íØ·Õ\x0008\x001bp«\\x0018\x0008\x0002öSUÈç\x001cóq`êÓS«C¤±õLï3\x000c\x0004HÐõUUÚÞÀO²y].JB:z¡Q
\x0004ü9×OUIð\x001d\x0003]Lðáè^"zü´\x0005\x0003h)×OSAÝ\x001a¬éZz\x001a¿Ã­hf\x0018\x0006ô=5\x0015ÜÅÝ3¸\x0008\x0004? \x0006Ú.\x000c¤}OM5·,\x0007/iS8\\x0008n!CÒ¡\x0000-å{j*\x0003¾
)*ó\x001e|\x00161\x000e|\x0018Øúà{ê)#É\x001fÕ¸ÿÄ\x0012 ù,ZÏ²°²Ï}ä­§;,\x0006ñ¼\x0018
\x0001Äç{*)Më´A??¥#à·©Í@Ãù_ßSI¹\x001c²	\x0016ÜËüVp\x001d|\x001c*	øs¾§+£,õÊ%Ï2;:\x0004VfàÄ9áÐO?(¤1È\x0008BäÔ\x0011¹m\x0000!\x000c|¼
¹\x000f\x0004Ãá-`ðTÂ­ÝìÑ¡ï\x0002sª¡zÀfhò*q¬'¯Rðu0b \x001fyºÐO? Q#ÉÁ\x001bÌ§¦ëà\x0014cÐb ÍÂÖÐO?(p ò¼\x000b¸×·QcQ¡\x0000C\x0013l?\x0010Ø\x0012A0
\x0006àáKÄ¡ àE~j
\x000c5%+áJr-\x000f|\x001c~(\x0008PQ¡RàÙG:\x000e¤iÉé\x0015c
KBë¡\x000ft±k¹Ïq8z\x001cÞ\x0012\x0013\x0004\x001e\x0007?P­\x0006ú×È\x0010zêÊ@\x0003ÞXväÇaÜ"ì\x001bz%ðÏÅÊÓP\x0000\x0001î>\x0019p¸¢¬-åÐ+\x0005ÞØójC'ðB%Ç}Fäù{\x0004\x0011\x0007ª	Å=_¨v¬ªÉMKXVdM58êC/,ö|ÊR9\x0018\x000eSVÖSê¡rÛ\x001c{º\x0011:\x0012E\x0003ò2\x0010M\x0011ú2ì_\x001b3ði û\x0011{Æ\x0019§\x0002!þµ¸ü/7¸ðW\x000e·\x0001êmúèåä\x000b¢õÐV)ì6IÇ¡%\x001b\x000e?PI(\Ô>z\«sQçuªx\x001eJsÌ\x000eEEZÓÓ`
í¬µ5\x0019Q\x0017äH­­°ªLÏp\x0003ÙØØ×÷ÔOw³d$ì°\x0007¢ðÏ¥^÷ÂP¾¶\x0010ü\x0019ÕºQçyw
É3ÒGÏè/Ð\x0013Q:/jK¡\x0017ËÂµ)Gë]¶Æl]úØxùøiÓ¼eÊwe¼+ó<ì)Â¶Ng\x001fü4í\x0000mNúØÀIÉã¦ê{A3¨¦\x0000¶|û³Ö<§æT6RÄNp0»º}|ØTVN9\x001ezIédMóJÚ\x0003sª©ªï\x001dLö\x000fÏNÎ×¢yúíç{d7¦\x0011\x000e\x001e\x001f^þÚP\x001e\x0012àZzê)ÇKÊÝÿ¥§\ÕùÉÞÁÙéå­E1ûòp;Ý\x001e\x001d&»¶Á?f.¤è\x000cOú%\x0004©£¤\x0007\x0000êxÙ\x000e@+òh\x000c¶Ø\x0013CTävhã¢\x001e\x0006\x0000s}\x0000à\x001agb\x0013Â¤:1gÄh¹©K×3Fý\x0011PoÙv\x0004Jñ¸\x0004\x0005§ le¢?\x0018\x0004@b)!}ô 
%éºÒMêÎ\x0018BÃ0àEt½®bÔi¬"O¨7v\x0019B\x000cr\x0018\x0004ì«s½.cT>ïPÀjIåGtl=\x000fy¸\x0006\x0008ÿqýéæÏÔJAdsõ~~\x000fÿÚ~|}\x0010¹úíDBd½\x000fÔK
¯c)-ó~z2y·ýéëüóÜðA\x0017âf¶©¤.ÑDå¨/k(sl¹½\:-3y?9Úþí9ûmßÛ³WÌ#9«\x0016Q
ù~¼y\x0006zó÷\x000bÏ\x0013¶8½JFù9d¼\x001còýx\x0015êñý \x0007ÈÊ°/+ä¿¿^\x001a6îùýØ·îá¶ïºÇàï¯\x000eTCàó÷K`=¿\x001fÛ(éñýVå\x0015\x0013ð÷GH3¼Î·¤\x001bz~?v\x0014
Ûçü\x001dçø:\x000b;\x000e¸ó®\x001fN0	ßGü`
=?\x0017\x0011ãõ'\x001a2H\x0006=?V\x0012=¿\x0008Ií¤ï7åú+)¨P°ÄØûûq`!µam}þsHîLÉP¥5½\x0018"~i²öÚá52»\x0013QS\x0012zþ~-ÜþÌCÑCûà²>CÚO:j"ãåûí\x0010ñ#
vúØþ÷÷Ô\x0001\x0007ß¯Ë¼ºñåû¦R{~?j\x001fÙCûàñKº~*\x0012Ç\x001b\x001c?·(3Hûà¡¥­ß¯u9áP\x001c»ùûU\x0018òüÐj§­ßo$·\x0013\x0005gò<ùª§·{~?ª\x001fÙCý`ÜN\x0001;	¸nÌ®ZZêùý¨~d\x001fï\x0003+Èú(AÍÜX·\x000eEý
zÿ¨~d\x001fõ£\x0002îpàó×¤þ\x001c\x0013Ø)\x0015|?vé¥ínf×¸hFqNO±ú\x0015~÷moRõÑ?à\x0006SO÷fñ÷çy}\x0019Ã÷63}l×?"tøûË+1L{	añ\x0010ýýiéc»ù\\x000fôÁQû-ÄsKé0ï\x0013s\x0014éc»ù
\x0014\x0000hßiµcb¡¤\x001c¢qÚ]ª>ÞO°Ü\|å¾_0m\x0014\x0006&C¾\x001fõê¡ÿ2]{6?âaYF(ÒªÝ\x0001ßÚOõq¾\äÛ\x0017ð!\x0004öýYûA\x001fêã{yMË\x0010ï\x0017èëK\x00072bòE-}lw½-÷Ê$ß\oÏ\x0019%~ó¾ß¯Qùé\x001eÊ\x000f)1\x000c)_\x0013øyäI¹A¶\x0007\x001dôñoúz|úºÏÓ×5NðPáYRÍWâî¸!O\x001fWË¥íß/ØôG\jDOóÓ×Ë)ÉßO_÷yúÙÞ°ë\x0013éöE»p}|=¾}ÝçígJáü×ìùP#\x0008þíÝ\x0010ÃMâécë×\x0017¾|\x001d!î¢¸G¢Ó¿ß\x000eQü\x00187½M\x001fÛ\x001d\x000fVÇåUØi
Iû\x000c
¼°OýmúØîx\x0008Vü)ÓEY'®4}ýç³o¿¥B&h([áéyã(\x0014öÚs¹³ÜÀø¨Ìÿj\x0014êàôübº¾6P(ÌÅ*×\x001b+­´XëWÔëî\)³×­´Û|||ùü×sºèáÇñì#|éÝlc.Ê\HX¨$É*ê®D'\x0007ð¿&}P$R+Ý\x0007
ØaN\x0019¹\x0018È'Ò©ß2ÕHÔV\x0014Á>»ßÓ'*\x0007ü8~¸½ÜÝÎ7$g!ôaH­16$>^\x001a¬\x0014Ñ»*68>=¹\â ÊZ$_oÿxùý¡S4)_¸©QËÓÀ^r(A¤m(>Re¦øÛ!àåÆ_=0RæûÃùÔ,fJf«$A\x0008Hî¿úA3¹®öp)¢ç\x000e\x0012¨+;\x000c\x0003@Ç_½0\x0008nÀÀ¢ªã.\x0012+Øb`ûÝ\x0006.£#\x0008¶T¸¥/\x0018ªlu\x0003\x0006óýÄ\x00001³f1HY4¬iª\x001b àÈ¢é'\x0006\x0013¸íß«RèW9ð¥u\x0003\x0002.\x0011þê#\x0006ð\x001a¨]\x000e\x0017\x001dRâ\{\x0013Y\x000eÃn¤Â¼]úè¥\x001d\x0002W\x000f0F!¶±äOªÖâþ °u%}ô.IL\x0000QIm	£ª-\x0000Û@ ÏèoÈ\x0012¾`oÚ>\x0003oSòÈ¥e[ãxQ\x0016ýh[å\x0011hü½\x0007\x0002^ñÚc)$\x001d	¢+©!c\x0004Ñ\x000fCÀ\x000b]{¬	<Q)&
M@àx¯ý\x0011ðòÖ^K ,¯×4è\x000e&#ð\x001aÒ ?\x0002^ÔÚ\x0003\x0001W³¬\x00007BóÒ5ÞU/ué\x000fw²öØÄªÞÌêûñ\x0004­qá^ÖÖº?\x0000^¿º\x001du´\x0008i\x0003i\x000bg­`\x0007\x0001(«V·\x0003(
i\x0016CLC»h¥ãK ª¸¶?\x0002Þ¬ÚC\x0004©\x001fbp¼8Æ\x0007b\x0017¸nn\x0010\x0002^£ÚgÉ,UÕ\x000c·Iz\x0008¼£Eªj\x0019S\x0000¼2õß\x0006×£öØ^i¥Å¥Q\x0003ü~\x00178¸\x0007­4ä\x0008\x0016P·[\x0004Ü÷FÚPú71ÇTB\x0017U hÅÒÓ\x001e&)Ðä½º0ò'ËÀ!g°ØpÚ\x0003-Ä0*Í½d£HÅ%iê&Àþ\x0008xi
¦¬{U28TÎë^éÅæÒ\x001e%5un[Ì÷I2\x0008\x0010]³I\x001a¢\x000e\x0017KJ·\x0003\x0000HE\x0002½Äkna\x0010¸\x0005¤=L¢zÃ\x000bËmÊ\x0016Q2=P½´?\x0000^>ºý\x001aêXL"n\x0008¢g\x0010Ü KP\x0016öX¸hyû×~GÉÝÉ\x0011)P\x0007 (KE·?\x0004l­¡Í\x0006!2ÐÈÈ&I
\x0002ÀûC·\x001f2¸Â'\x001d_,P³ºT1\x000cRÈeWh\x000fÄ\x0003& U¦ 
ïxjÐS,{A·#P9#\x0012ÉP;°v|\x00086\x000cºe\x0007h\x000f\x0017Ýk`ËJ»È±3 °ÃdÀ\x001b?·_Ä¨:ÀX¸ä\x001a	î7\x0018z\x0006¼Ûs»\x0004,3I\x0018¤¼#ÿ8ÄÈé1\x000eRGeg iÂÌ*)hYtä\x0003¸\£ÅÒÎ^\x0001{§\x0002\x001dÕì\x0017²\x0002]´x&Ín¾¿t\x0007³ÿóeöø|;DZ¥>#,Ø,°\x001cÄÝ\x0017<%îªA·ÿ¼]\x001cNÏS),Ì\x001e?Î¿äOÂs\x0017á»\x0011O³YÎ\x001e^nfß\x001eg\x001b¸\x0006ÓÃÔÄ\x001e\x000b\x0001\NA;K¹\x0004\x0001aDµ\x001d·ð\x0002^¾üýlr²	SÅ¶	a?
0éÜ®\x000c¤gDuX\x001fD·³Ù×ø§:U#3ßëS,\x0017\/vgÁd©o\x000e\x0012Cbáä5+\x0008\x000eÍ4eù\x0007û¼?j\x0015DÅ5ßËûT×Cr\x001ewtf/\x001bT\x0017ñÛ\x0006\x0017yílpª\x000b)U-\x0012\x0017×t/oT]O\x000eI\x0008A¸\x001d(êVàæ*7 ô4Ã\x0018¼à%1ÁT¶w\x0008DWAtí\x0010£gd\x0015í¯\x000f¸\x0010ê8V±B\x0018\x0007³¦©\x0001\x000bFj!pÎ¼Þ\x001b\x000c\x001e\x0005\x0011«n\x001d©í­\x0019£cWßj\x0006È\x001c¡\x001eìo\x0002¨]¡*\x00001;s0ûä®\x001fæß\x001e7)|df2a+x×§1°ônÁúuÕìÁä\x0003rº~þýl\x0003E'ÁRRwaáoûâ2\x0011\x0015lö\x0005@Ãf:=g%µÈ<\x00018\x0010\x0015,,¦÷\x0015\x00178¨E\ÖQNÛËÅz	SQ±õÆ\x0015~ÍÌ\x0005WH\x001c\x0007³ÇÙËÕìé?¶]0ÜZM¾Ø­DÜLp\x0003Ö¡"\x001b:M.÷'ç=.Xf+h¶
¤r>@Ó4ÅÛ\x0019ÙÈÁ³F\x0016 »#Y\x000f»}YjÄ8
7¶bmìÍÆdÒ\x0017Ï\x0012páoß¾\x0003¯\x0007¬éÃËÓó&{\x0014M®FxzÈåÈÓ7\x00157â;ðxÀ ^_LÖ\x0013I\x0016X¦eúÃÂ\x0005\x000b¹¾¦àX1\x0005g VÒ\x0010â\x0008\¶Æe\x001bp\x001a³:^ã,i+£\x0015]!Vå~°fB¤.X\\x0013øÁ[ümÞ¡ø\x000bøi\x001bæ*q9 M[\x0003\x0001U #TìÍûzz&mQü\x0005<´ÿZ/(i gAaÞ\x001dûöÃËï\x000fwÿñ\x001eÅëM\x0011÷e8Ý9^b\x0018m¡E«,åËOöÞønÃÙII|vXfvÙ\x001eO\x0010neì0wùZWZ­veÙí\x000fPÅ.ªØ*r8\x000ea\x0017	ÊzQ6b©\x0015Ô·}QE]¡ÒÿnXÒú@/Ï\x000fÓèøÛ·ç³ÛûçÿØ¿Ýnb×{,©ù\x0000izÊ¤Ô°\x0005f¨\x000bë|rxr±·49Ü@«O¨6]TøÛ¾¨  é=+àÞS\x0011\øRñsUÿxOT.íÊôÅ#ÄNü-³²ÏÑx7ÿcv¿)Î\x0016ÈÃ|VéÑðd.ò\x0018ÝY/wU%ö):\x0013ï¦¿LN68\x0013\x0019!²v\x0010ª<pÑ0*~À\x0015y¼b[\x0018Þ E\x001dì¶ ´I¯.B\x0013,ÞáoAÝ?? ¼³ùíÝÝ&{Eu\x001eZ\x000f´ðPaë ÍÈÖÃA\x001f.O.N\x0011ÛÙôðèh=Ñ=cÓ¶Â)ØþØ4æòòk\x0000W\x0000\x0008ÞìçlÕ>Ø\x001b\x0019\ºTeZø\x0014p¦©\x0005~ÿáö	]Ì\x001e7.(W¦ì-RÆæüÇ¶Z2HNÕÔ\x0007ç\x0008ìbrv±áE0®Pã
ýqa»§Åé­·×
GµD\x0008Ñ\x000f¶ÉsíFö­¢Ð\x0008Çý\x0006\x0006h"õ×YìçÉÅ!\x0007oËSÕåG7\x001f\x0014ÇÉzægB£«Ð é¿\x0005\x000e\x0004vÉãZ(	\x0010¶ÊC¡O{ç\x000f/wé§ã;~¸?}¹ÛÄÌÌ\x0019
.z£]\x0002ÿÚUÐõ´ÂùÞùéåQºñé,OO¦ç\x001fÖ\x001fçLèìñqNà\x0007oñ·oß'¢öãÙõFöx\x0000£Ù×w ÃÜ\x0000â
·õÂ-«ÚÞ'öãÉ»éÙú+¸^é\x00159â}Ã\x001aðþÃËíÇOÛ3\x0003Ú
ÞÔ\x0001§ÉD=ér¥Ðq\x000cåðà§\x0017Ø+T¸B\x000b.ex\x001d\x001fèW"§ô\x001bvà¯lãâïÌ¸°dÝ\x001f\x0017¶×åÄ_ÌdCd^gTÉV`²\x0002&[iÍëeý¢\x0019ÖkÎò\x0008SeÊZ©
j\x0001f=\x0017ºÁ\x0011ã><_¶8=âi]áÒ-¸£ùRã¢dÎM_V\x0008]U[Ù
m\x0001æ\x0015µËáÆ1Z%n|àî\x0008øK¹û®ÐMº"8&A\x0011ËZ\x0010EWÈ\x0011°*U¡T\x0005ÖíXW8j#\x0000XÑ\x0014]1\x0006X¬Å&`¼`"\x0001Ë\x0017?H®h:,iÄe*UaZTÃ\x001c´¤6Xl
Ê\x0015`=o\x0005V©
Ó¢*\x0018Èo°=6±²CÔ´q­À*]at-äD.(l+Î:L\x0016s4æî\x001bS\x00013MæÈqèvû®°Ln¼n\x0003ÉäTcg+ûgÄF×£û½\x000föHl4ÍU%#° c#§yp\x001b+Ê]oìôäýÞÉú¦gFãk4¾\x001f\x001a/<OYÁ[¥^³Dç«\x0006 Q\x000b=hT«ÛÆb\x000cqÌÌPÜ\x0018¸ÉÀÄp;\x001aw-d>\x001cFïÇóûÙ·½_p¢èf\x0013Ýú!¥\x001b/´\x000buãÅñôdò÷½_p¬èý\x0006Ïqù\x001aoÀå<\x0015à%r3Ö!'\x0000W½g²\x0011W¨q\x0006\¸iÄ\x0011.M9hm\x0004ïqf¸b
+öÛ©ø\x0018µ º\x000cÐªt\x0007Tû~ÛpEQáÂ9Â¾¸@0¨ÈScjV,ZKT¥F\²Æ%\x001bpá`o>Fc#·aÇ\x0011ãªÈspáp|\x0007Wï\x000bÞ]nRiYE%\x001dÑ2"«ë`T^U¨Pîý\x001f£¡è\x0015]¤|\x0017<FÁëu?¸LË4à2\x0006UAy	_µv\x000cË\x0011°|
«Aw)£©\x001e$±NK£\x0006J\x000b¾ô!\x000cU\x0012\x0016\x001c.®ôûþ·^Krýà52©6\x00067¬Ùû\x0000³¿^=ÿÃÏ¯~]ðMNþß¿¤åu\x0007³/·Ï³ÛûùÞÅÃËãýíÓS\x001ao¥¿\x0005toç	\ðÎ¦\x001eÔ\x0000gBæ{sJx\x001eN0¬*\x000f§gço'¿LO.Ó\x0016»ÉÃÉáÉtïâôòìäðü|òöãÃçÏ/÷sþçk¨\x0003p0TÃø­Ë\x0019©ã\x0010ÍHríw41váP½ \x00114\x0013ÁûH«\x0004\x0000kà¦ºÄç¿3¬8ecu\x0016óÂI¬ =Aå
Ú\x0013ëÈN ¦ç\x0011buDe«ù²_ËË9\x0011¤µß¡X©\x0015n(Ö Ø#÷\x0008\x001d\x001c\x0012Ùñø\x000c»+ï\x0016\x001c5\x0012 $CÐ¹l
X\x0015UV$Q_ì\x0004ib\x00184%L3P¸¶IÇ#ÐÈ3,z2Å&æáÏÊ£i¤n&­s~\x001c j^(©ä\x000e¡b·ñðgåg¤*\x0003k+ixHO	"ÿØ	V\x0019þ¬ Ôå`\x000eWõª¬® * {%yzc\x0017X1Á ?+p,i9Á4Õå*=å­w\x0015·\x001dxXÊñuµ^d X?¥äI\x0000{¯G¼+ÍZ
¶øòeu\¥fBG¥G<,­ÎÒXÜ\x0015â\x0008+gI¥¶»Ó¬&Õ#\x001eqèÊ#V#³¤¯\x0002ÏÉ@Y­]`Å\x0016f¸{å­ F\x0005ë¢\x0004a¼c^0KîN°ÂÕ7#\x0000N`g¥CÄ7X\x0012láî|\x0016L\x0011JÀ{\x001aR5È\x0001¤#aåÑïÐgA·ÒÐ\x0003Áò\x001dÐ:[\x0001UH?¢;\x0004JÌ4CFK¼nØíóÎßJê¶Òîðüáýá:\x0000~,1ÊÜ-\x0002¿qÌÀ\x0017\x000f;ÃÊL7±\x0006*¢C\x001bH\x0010ª§¾ÆàåîÄÊl4C¡bm8«DîOX\x000b«l°»»¬Ì\x00183\x0018ªG?%A#,ÅÑ \x0008<(¿\x0013¬´\x0003|(V$LÓ%¯O\x0011\x0016²hR\x000b¢Û¡+È[ºbÅi$^6B´öUùÒ.¹;Å´Bu\x000b¨y9GjØ`Á\x0013ÛXyÕõ`¬¥3DHi\x0003]ZÕGXÝ\x000eÅ
¯ÊxYÞ\x0016Ç\x0010óÜ\x0001@µÜíô\x000e}l^Y=\x0014k\x0010ä\x000bê¬\x000cÕ)ngT;Ô­¼Tz0TK±«\x0006£\x0019\x0011k¤Â§\x0013;L^ðâçX£ä2xÎµ2½®5;T­¼y0R\x000e\x00064>1-	©+MçqwA\x0016vùá\x000f+âÔ4Ñ}Á
ÐÙdá\x00043a;\x000c\x0008yÍòP¬Ê\x0014~õ¨)mÊv
³ÃP@Æ_¯nR
\x0013ÿ983XR\x0018^¸¼(\x000c?³\x0012Ë²f7Ñv\x000c.è\x0008ÈàVÑÖ=ceÌ­\x0010\x0000Ù{N\x0010ìPyi\x0012²\x001e%dï\x001c·à'ÃVlÖ\x00142ì\x0014òóü1AÆ\x000el9R4Ø5*	òbXÓï0[ ³!²\x001d#åPj2ÚzÖ\x0013gDt»l	²\x001d\x000592å«Ñ*\x0016oÜ(Wí0p ÇgG=¾`<§\x0011qA\x0006¬\x000b³×;L"Yz|vÔãC\x0006ÌÝiÀÅãàLSÙ\x0018 \x000b·»²¢\x00192è¢\x0011#é\x0017|ÌÓ&hØêZç_gÉ>Ï\x0006Ãõ\x0006YYs~¦HØ\x0004ÞédeÜEÈ\x0012\x000e£¬\x001e.\x0001#V\x0018¤â¶Tj&"\x0012\x001bF"¶¿ÿå\x001e¿þºØ¹\x001aç{g\x001f¿l.Ø\x0012mÕ\¯--Ôeiã2¶8Ý;;ø°\x001dN¦nc\x0003V\x000c\x0013\x001eÈIVÌ cÖåúâÁºF\x000b\x001eÜë\x0019aLã:\x001dJa\x0010 'ôj\x001dÔ\x0017\x0010\VÓ$ ¯Þ\x0010ñ¡>X`çÎ_\x0013Ýj\x0017ª/åþíx<qÚÀ\x0005òØ«èÌ½eÐ|( å.­\x0002ï¼\x0003YÌ¥r~nV®±s=\x0001½næØ(è%GØ\x000cÁÂ¨;\x0016¢5½2_h¢\x0000QÌüX£uT¢·jM²«/¢Äß\x00089-ÍÚ*G&0áBõbµì(q\x001d7É\x0008\x0019\x0015I3bÇ8{þ²È(;µW6[\x0010\x0005ÜäÄ¶¨\x00037\x0001X%YY\x00073JY§ÅnMß#
1(dêÁÜ1Gÿq( W
>ÛE\x0014i1wbÄô,"®åÙ0Ê|¤ÕoMÚ(\x0015ìd¹EôöÁÂÆrÆ!zÕW´UD.2«\x0004\x0004\x0016¹\x0017Dä%+ì(FÝkhÈl¬Ü\x0015qà2Y¢\#³ÆiîèU?Ó6\x0019I\x0011(ðHDÓ1_#Ç\x0007ÈÈ²!èT©&\x000b\x000cÙÄ°ðCÆ6k
}\x0011½ê¤Ú*#\x0005Ö8­ÉÔc #Ã§N¬éJì\x0008'46fDùñbÕ´+2²v:zÝÃµUF[úAFp¥²\x001cóóu\x001e1\x0019­\x00146úø\x0000ÉÈ-oãSiyÆ`(¢W½c[Eä5­HN"9é"y;îâ\x001fèUØ6D*SÈfß³õY\x000eÜ_O@8¬¬[ôc@\x000f:\x001b}÷Fç;dya\x0010X´5%¾p^u¥m)´\x0010Ï¿±Y\x0015ùÂ{Þÿ(D \x0018ur\x000cHÅ\x001f_³º¶Ú\x0002\x0019Qwèu7ÜV\x0019ÅÂ\x0015ë*È3
6IÇ«w"?­[c\x00108ôDV_°\x001fb\x0017ö#¬©\x0017õ\x0005ôª\x000fo\x001b dÕôðç¤oàíÀÒé\x0017\x001bþ´nQ`õ5Sà	c¸iÍÉ\x00129F1Êê¿îÿÛ*#£\x000b±uÌ\x0002K\x000fN¯)ðô\x0003\x0007®[Ù ½ ñtd1»Ñpg§Óã.õ«Ã­\(üó¸k>XÄÆý\x000cÈ¬)(õDôº³p\x001b"\x0003\x0007sFEÒ\x001cò«h^÷\x000fn¿CÜ:n%üOêmBñ5
ãÔ5Æ¦I]\x001b¥yKtä8ê´)D¤FyE¯Û\x0016·_£È\x0014µ <\x001c®\x0011Ýk/Æ)G\x001c\x00087MÚZ\x0007QB}aË5bPpe×$åû"zÕ.¹\x001dQ Ö\x00088µxnG&\x0005\x0015ÅRª}k-8â7Ñ§$OF,Ò4z\\x000eBaÅ\x0002þk³\x0016PHÛå
¨@ù5mJÔoFfü~½J ®~ó¢)ÝxÒ\x0004Í©c9.\x0015aè\x0008Më\x0011\x001aÅ5v\x00167{UÐÒâÒ\x00110×
\x000cëÒ¼!bhì\x000cçµgVLÜº\=\x0007`uõ|+0\x001bKþ6ÈÒ\x0010fÃª±y.Ørá«OBZèbè4\x001f8N.é5Ã?}«\x0001Tò\®xn/
\x0008êK+£¬[õ³r\¦R;Ô\x0012àn6h	ð7Õ\x001br\x0015²ÝMÉ\x0018Æ¥\x0006\x0001ÓUÂÔ $\x0002\x0018»\x0012¸\x0000
EY\x001d-Ô@ÑÍÒ7+YDÏá\x0002¨|ò=K\x001cìô¾çÞ\x0015õX4^-p559Ã%*Õh
°0¤jõgYPJïn¶'çó½Éãçù|ïo³ûLbºÞ\x0012i"\x0015³\x0001]S\x001a\x001cä\x0015Qj)dzG=9=îMÎ§Ó½¿MN\x000e\x0012©éV¨\Ì\x001c\x0006\x0015I/f,a<R	ª\x0010;íÃ¡Òå\x0005p1æ
t8ÚRÖy+w\x0007K²Ã "U¡*tw\ê\x000b2\x0011K½\x0007£b;ã` \x0001¢\x0002\x001bu_y_VÊ\x0019³;¨\U\x001e&Ó¨Þ0û(H5\x000fâ)»Ôa7
)O\x001c.T°ÇÕt(
Í%\x000fUvÔí\x0002ê¢2>ð\x0002\x0010q5y×
Ö7ØWz)1=
(6ÉÈÁ@£Yp)Ã)k¤«æal¡vµ\x0014÷	\x0015·¯Ðà8®IÜÑ\x001e
Ö\x001dÊµýÉÕÉ¢\x0001ò\x0000q«áZ©jw\x001a`Ñ\x00100\x000c«\x0014THISî<.\x0014ØÑUÂìN\x0007,Z\x0005a
eç\x0003ÃJN¹ñ¢ÜÝÙÕE\x000fÁ0¨VpüàÀZ9®OÙ"Vívµ´\x0017\x000cÁ\x001a\x0012À6ÎH®¥YÉÑ¡Javµt\x001e\x000c|ZÛ\x0010 ìá
)÷b©[y\x0014ÔÒ0L¬fñ²pÏ6\x0015s-`/kÑ¬0ðe)ÚP\x000fbÕòÉ/\x000bO;µ\x00046aruÓ?ÎÊ¼Ã\x001dû>bëî®À¢¿a\x0018Ta
'¦òcÑa&½\x0016ivçµ,ú\x000caÕ\x000e{\x000cY\x000b°X
\x0007Ìj\x0001¤Ù\x0005É³\x000b\x0003Áü-ÛYJ\x0018+\x000bÚ¡6XÎ
\x000e¬5o=G»@8Ll\x0017vèÇ¦dÌÉflá!w@5\x0017£}Ñ·vLÊóÈç\x0019èÐ:Z&¤KÂýæB¤\x001fq\x001bàÍÉ\x0017ésÉòjn¨U¼ÿ|8ä«ëg)]§£\x001e×\x001aì?¼Ü]ÍïïçOë°E¡ \x0006v+±óÀ3î ÊKU\x000c7\x0019ì^\x001eíOON¦çkÀ|R×Ø\x000eýkÌL\x001dÏîP|G³çç¼åböôt{sÿmýI[\úÃëª]¦d\x001b\x001a8\x001däTÅÉ±ÿ\x000e\x0013UÇ£,À¼åbr~~øþäïÛáæÜÕ`¸FF^oi¶ázÇõÝà«ìÑpótÀ\x0008é
Ú¹f¥ÔDÑ\x0004Òå]®f\x0014\x001b
7ç°K7*î¹Ac³së¸\x0019\x000c.pØ%ÜÉ\x0018\x000e·Ì[¥dÞaâ0ÅUZ³C°"\x0018\x0016)isß\x0016x\x0000èÑ&´Y\x001fÂ.Ë¡÷p¼u*àÄ)!\x0003O\x0013KìÒÝ%^
iãÕ\x001cÑÞ\x0017Ùf\x0001Höfö»Ô\x000c\x001c*+¸|M=¹"\x000cx\x0005ï5q§×b°áxàÚ	Üm5/¥\x000c3»Ë¡Í`¸:F\x001aÇµ\x001aTYÎ\x001bH´\x001f7T\x0005÷Ñx©[z8Þà¹±K\x001d\x00162ãU|\x001bbEå6\x001a.5.\x000f[µè6à\x0014Còg¥s¦WíR¼«¼¹\x00167B\x0007;+·*È¼[\x0001u0\x0010UÄªà*8\x001bV=#%¼cÔÍrÜ­¥ÓÔ S\x0013Â\x0008ØEÃ©Èto2\x0008î\x0010
"îò\x00084ÑF¸k<á\x0005'â?¸Ë¥§Iû"8A\x000cñ:\x0017ÁU^~4wÊøÝúk\x0018WF\x0008+G¸lò
5¯+I±á\x00149n\x0019
÷Óõ÷§?ÿì\x001e\x001cÍö\x000efÌîæ·ëCH4êyåwBQÀi\x001c¦Á¿Ñ={\x0008\x001e\x000f&¿L¦gë"ÆÙÇëï\x001d¿ü`ö}v7[\x001b*b
AòÂ¯ÈM°Àú	\²n¸p0ù_£Éº\x0018ñÆ?]]_u\x0003ÖùÞÁ§Ùýõü./$_Ó¨\x001e\x0002õ<çò°¢FuîÂV±jT?î\x001dü49y7=^¬\x0001â®ÜÝÃ\x000eOóÏ·÷\x0014è\x001f?¼ÜÏ¾¾l\x0008î¦\x0001g05¥¸æ\x001d{ù!®cwðÓôøðâûãÓËÉ^®;¡\x000e²\x001c¶"\x0003^åÛ¬m.úz®£¡Ç4\x001e\x0016]VXçU
äK(d\x0007ÊÐ¢\x000eãå\x001eVd\x0001ndqn4hf-\x0007\x0015¬ÇCË]\x0007­Ð"¦e²Ð\x0004ó\x001e$>Â,3YQ\x000cD\x0003ÞfdñMö\x000c1Ä±\x001e$\x001b¥hüxqtÛ\x0008MëÀn ÃBäTa¬+^-Ø\x001e?ðÛÝJ­ñaþíqþånvÿ<»ÞÄÄÅL9bqÂ$hn@[ä#EòØ>Lÿ~6ýp49¹¼ënYsôE\x0007÷?O\x0002:ø7\x0004O\x0018\x001a-Á\x0018võ©¶¡ã\x000efx&\x0018ªbØ¨Â\x001b¶Õär*ííêçÐ\x0007Þ×/÷IU¥R÷Þß=y~~Þ\x0000	\x001cFò\x001dÒvX#P\x0013ÏÇª\x0005\x001e®Øû£S0Ï\x0017\x0017ë|ÿæ>º®<üü\x0005\\x0018ôeÐVÞ®·Õ\x000ek&9`1¯B4È\x000cÐ8Q³J\x001c\x001e\x0000¿\x0005\x001ds4k3»\x000bHùb5AâÎ®õ\x0006S R\x0012\x0005 õH×\x0000H9\x001dÚ\x0002É\x001aªÝ"\x00115Q#Ó³!H±R«}!éÛ»?â¬[¬+^\x0010ÒÝÃýÍ$ÀU&"bsÁùrkËÉ\x0001\x0011«
GAu pÛº\x000bõÇÌÅó\x000bu4ûô\x0000×\x0006ßÏÄ@Sø\x0006~G~\x000ce\x0015§\%§£ÉO§à{­\x0013S\x0007N}zÀÁ	n*X!¯$Åw¼Â\x000b£\x0000ÕW©\x0007 ï}\x0003·
J¥[65u¶·\x001dOîTmÀ\x0013¨W;\x001d_N§MÚcðdÏ¯åÀ\x001cwIØÈ½Rp`±\x0000ò«ôQ@Ù«j\x0001¤ßðy\x0005NÀ\x0005Å;¤n\x0004\x0008_ú6}´\x001c$
è\x0002®\x0010ïLIÙÌfHÏÝÿé~[iDö>Ü~ÜP´ÄÑ{=Ä¹gÉÝõ«µõÞÃíX­Çf,ð§®@Ð®p7\x0008Ò>ÊúÕ\x001a±'e»±\x0005òDØ\x000béÎIÌ\x0012KB+ú¥o\x0005c5­£s"^9Gýgà§1Xr\x0014Õ\x001f¤6\x0018¸1\x000c¼rp¯ùÊØUJg3ømöY®¾¾g·Ìïç/l\x0000°1?Ò0©äiíKýØ¯1ð{g¿LO¦¿¬³¥\x001d`¯îr\x000f`à
½a\\x0006µ6+¯^®y]Ûp=øÜÞÌ»L	\x000cììá\x0005ì
:H1
4R\x000e¢Ëù:\x001dØY'ViÅ³ÓKð¯ß^®SB\x001dP43ýc¢ü½Îùû\x001f\x0000üsþý»ì(§£ÙýõÃËããzÞFä\x0016yY:z÷¤\x0004îÖ¦RÅîó èÝéåÙÙ:Æë<|îV»fOÏa~w·ÉIì×L(\x000c(JJùjO­D*ÔäqGs$\x001e\x001d­µ`þÓç»+QÅc.Ý\x00149\x00059o´wÑ+jÄ\x0010ZÑ\x0010¹Vu?J©ÒõX\x0007A~ë}\x0010ä>\x0010\x0017q­xþv\x0013²\x0003¯ÓA_Ïaë×ke\x0017\x0002¤`æÆ\x0019 ü0\x0008Ù>õ ¸ßE\x0013wEhG\x00032¸þ¡\x0005ÂÝÍ§ßµïö\x0016\x001fÁûÜ+vH\x000f«¹«L%Oh gÕýzxksÄ¾}_¿wÿú·ó½w·Ï{Ç³ÇçùÝúö*«-­?uèçâµ¼°K\x000bY\x0015\x0015\x000e§{ï\x000e/ö'g\x0017Ó£íp²î\x000f\x0007ßÊp¼$v\x001e\x000b!/]\x000bQ\x0005ýÐÇ·îë|ÉñÆ\x0008×ban:çá²§`#*\x0019]R\x0011{Ç\x001bZ÷IÄo;_\x000f>Êìññáe­\x0014¤É\x0003(\x0005¸DNæ<ì$)È:/\x0008ÞÉä\x000cTöÚ·ñ\x000cÝ¿ÿ»ÙÇ\pzo\x00038\x0001ÈHcÜ\x000f\x0001>ùÚüÜ\x001d G\d:\x001eO×J¤\x0003(««\x0006@·Ê\x0000 \x001e\x0015\x0010Î(\x0006TÑ´\x0003Ê
¬\x0001è5'hã.?aa)I
w¦z>íxòsnÀ\x0003ïÙ\x0012 ¹\x0010\x0010ª2\x0002T{Ú\x0001åÀºE@\x001aÃû\x0004ÈX²O\x000c±î@V±Û\x0001e
Ó\x0000H9â¸Ir\x0010×¦\x0002hÜ\x0015Ê~Ë\x0005
K\x0000áÔð\x000b	q,Ïf¶<2G5Ì\x0004(SÔ,
h\x0014\ÅicU%\x001fIo|XO\x0018\x0003ü-"%Ó\x0012¢L®k\x0015âN$ÄÕ¤\x0016=ub\x0018î\x0014¬\5Èß\x0006&ÐÐdLÄÑÎL-vT²xü¨\x000bÍ½
¼!ÖñåH"b\x001a[Ñ8D4üØ\x001b\x0017¸¯.5¸Âdä$_!§\x0006Ü¡xó\x0012¾>u}Ð\x000f\x000f÷Ï©Ëd¾èÓTÜèÞßßO\x001d·ãlþt{=¿ÿ+\x001fÇðÛ×ç÷ºÖS7uáúd×CzY«Î¦çï¦'\x0007¹ø19;ø	º\x0015Yö?ZAÈ¤)9\x0015ù\|´¤\x001f\x0001ß\x0001²ì´"s\x001d)^\x0011j]à&iYuU\x000c}VhH±c¯vÓ1²Êo\x001b\x0008,û&ÍÀ\x0014¥%\x0000ãÅÖ0O\x0017a\x00072Ë^J#4¬l\x0013µ´ÒÑ	&q÷ªÚJ×\x0002í\x0011â°k³òuöÌ	1Ú@C¥7\x0015À»SµzõöÑé\x0000\~
½\x0001bY ç1zÉ	Np%Õ'Û
pùAô\x0007X¢Ý·Ð\x0004IÇieìn\x0000ft\x0000@pM#IÐj
Ç
ö!\x0015«U]+Àì¢\x000e\x0000ÛeI`¶\x0014\x00014Äq£¬òÔÃ\x0001f§u\x0000À`)`uItÄÌk q\x0013Ó.\x0000²\x0013Û0¢«@CVI¹©ÛDåùÈª¦\x0015áÇÏ}éö!ýóÿcwó½g×©±\x0006µáÕã\x0006I:¤É\x0006$Ï'íÀ\x0012SÂPÕ\x000cm\x001dÓ½'gïR{
*Åý³>XÉ/ø\x001fÔãÿ\x0008¬¤)ÿG`%oâ\x0004Vr/~\¬ß\x001fÔ·\\x001b
d¬\x0010jI=GNC¨M¥ð¥lã_\x0011e= ­
\x0007¶C³ËÊÔ5fé	ÚÊ­ Ú]ïÛö¶*\x001eØ\x000eÍñ¶M§¸HghÛ$}5<\x0010Ùªp`;2\x001cØÊB3\x0010
çx\x0013®\x001c1¾)\x001fõ\x000e ­
\x0008¶BÃUªÙëv\x0006×VÓkp+k¼Æ&d«âíÈ\x0014<N®]òR'\x0001¾­âÚeUÍ\x001d\x0008mÙYì\x0007
\x0000\x0018\x0012æVfø·©y\x0012 Åõ¡Êfh×Â=ý#¬<Ï»\x0005´zNÑÖ\x0017Pt¶¼\x0007\x000eYPÑ­Ót\x0005åv]÷ðÇ·?f]¯ìh¶wvûûÃÝ&Î\x0008¥¹c\x0018~ñz,\x001d¨ò¼bU!n²wvøóéÑºLÐüáëççYWß>¼<§ÔÔþü~vó²©Bî¬£Y\x001emUä>\x0019\x0011©_(UÑA^^¤Ü\x00148÷kÅÒDz¶\x0005Îe\x0016\;yø\x001b\x0010ÑÅ\x0017ZEDJ¬\x0005\x0011/¬ÕN;W"ðr{-«¹\x0001HE4@`(7\x0013\x0001$A`$\x0019RU­\x001b\x0000TC\x000b$MËµÁÅ4\x000cú\x001côb¤(rl;8ER7Gk @J´iXªd×\x000e©bm×[\x0013&09DÀ\x0002ÿ:aR1\x0013\x0013'ñNÑØ¬\x0006\x0015Étlàr±\x0016¨ºu\x0006@"f»&H\x0016©b2<\x000cG§i¼ÒjäÑQÖ¼\x0005\x0013òeÕdæ]\x0007ÂRú\x0010nxEðÜ)ÕZ0I¦QÓ6^¡®K!­\x001f§\x0008¬	`ådpaã\x001dÆT¯\x0016éI\x0007ë>×v.Í1<=Í7
ºTÿMÚ)\x0002>"I\x0005CK6Èª\x00030¥1óóéúÙÑ\x000e(rÛ[@	i¢\x000cJ/
æ{Ods\x001b\x0000Ü¨\x0006P\x0001\x0002D\x0014&¨÷[ppr¬¤*ÛÒ\x000f·D`\x0013=nÒ!I!¥e\x0006¥ä§·\x001dÔ\x0017ýñÏO]®ð³tÉïþïÿþ?Ó§çÙýÍ¦Ò°åÚ\x0010F\:f"ï\x0013\x000e±Zuv.ùÑÞôübrò~; ºO-Ä\x0019ÃÓ~o\x0000$
 1pÈmjcÕ\x0000ã¾@ØXÐÔ\x0011i+\x001eºÙmâ!~~#\x00141N"\x000efâf\x0014 râ\x001a\x0000\x0019n=\x0003\x0013§KËU &u8¸®³\x0019\x0010=³\x0016@p\x0019\x00132ÉÀ«sbM#ß\x000c\x001c¸\x0016@æ\x001b@BGcd ?\x0000
£\x0018¥ú[\x0000	"\x0005Ïc¼\x0019gR58±1o¬¸Mh|]\x0012W"Âá\x000b´\x0014\x0005´Â¡æ\x00168ÚQ
$\x001ddDº\x0008È¹AÅ·mCäI\x000b)»\x000e	\x0011¨bcj\x0006Dý)M\x000csÔ G'5ThÅ£¨½ÈVDÔÒ\x0008\x000f½zÃ\\x001a\x0012äÂ¯~)ân\x0005Dte-[Ð2(\x001cj \x0019>35ê\x0012q4Ò"!Ã^\x0006I\x0004¹£V£\x0018Ò$¤\x0012éÑ\x0004\x0001âr2h±g\x000e´F\x0011ñµÖ²8\x001fEDj\x0004\x001cúhS¶\x001b­(ôÇeE, 5êR3Y\x0013"ËV
f\x0008)ÊZÒDÊZ\x0010	C%\x0003¸Õ.\x0013+H©u!?ÑíîÇìãÓ·¿w4Àsüpÿ4¿½¹¿<"¶ÙË&b\x001d\x0007\x0002Óm\x0003H\x001a\x0018ÁBÒà,-µãÓóéáûéå\x0019<\®gÙé@\ø­\x0010e¤ny\x0013Lñ r#ÙéøÊ\x0011\x0018\x0008qáU¶BÄæg¨=·ùq, kV¿\x0011\x0000\x0017N]+@äh¡cVºÂ1å«ö~ùA\x000c!²!'õ i*hM£C FfyÒ¯<Ð\x0016]=ûûnîþâa3uàèåy.$2Ëd±4óÁ\x001f\x0008uqº:æËµúcþ±úzÊùìöþù?~Ïî×çx\x0004\x0006¿YYÇÃ¾RKZ\x0019¨PÁ\x0000aO\x000eO.ö~NN¶Âáì\o<R&¦Í\SÜd«\x0003µú+Q\x0013\x0016öÃóôÙÜ}íÎó`¯ï?ÿ{c³/\x0018\x001bCýâJó\x0008èR\x001e9pÝÙÜãÛùþø÷}NFüÛ¾¿Üÿ·\x0000fOÑûnëMn»ï]¼<>®\x001fp\x000b\x0016\x001cù7DªdM¦­µ1e=ò\x000cì\x0012M\x001e\x000f¸\x001dM÷..ÏÎÖÎ¸	'¾Ü|ë\Êó§T\x001eýeþíñvCbÖX\\x0011Éßµ"Ú\x001b\x001b´ ù\x0001\x0011B5?p~zyÊ¡¿Lÿ~v¸6/[ë	Îâ\x0007\x0008lrwHéç×{Î	"x²V\x0007êì\x0013÷Ðª\x0014ö\x0015T££DB?}·!¯W0é.&ÝÕ¬µÈ\x0010DM\x000bæ>¨B6L¶É¶`²Ä4cmP\x0003L\x001a)àfèá ÒÜy\x0005,­\x0019èÍ0½¦Å1c>Cnò\x0010¶¢Òë
=ª?X\,0ÞÇ³ß\x001fÒ\x0010øz}ìµ¹\x000fÀ\x000blÐÌúÛn\É\x000c\x000böñäçÓ4	¾
îBÓ­Ð4ùß^âªcOÐÈÔ&VÝDíàl\x0017m\x0005g¨\x000càqò!\x0006\x0006G³Â\x001cÐVÇ:kÃ'xþÁ\x000bx«äÞ\x001aæÖ:×\x0017®
ßUïêGÃ÷±Æ÷ñGÃw]ã»þÑðÍk|ó\x001f
ßo5¾ß~4|75¾\x001f
ß§\x001aß§\x001f
ßmïöÇÂ§jý¬\x001aõ³Æô$ã\x00168ã$U\x0002À¸ù×\x001eT\x000f|\x0002bïÊ)À\x001f$§ÖNçÜ×\x0004<áMa0H\x0004u4¸<9O\x0013µU\x000f#oÆô×\x0004\áµ\x0001CA§ºèT#:\x0007ßµÎÊ â}Î"ºj¾\x001dîÂÓÍÂS¼Áè\x0010y\x0015a\x0006=\x0011Á\x001f\x001c\x0005ÏváÙvx\x0013K:\x0001W£t·´¹¹\x0015ïÂóÍðáeÝÚ\x000b®\x001bAËëñpWm=ï\x000f/váÅvx\x001a{\x0019\x0012<çà\x000eàr÷j¯´\x0015¬\x001fnóËÅaaCA¬s\x001càëH.½Àþ1ðª§!ß\x0000m»át\x0003WÓt ¹\\x0001joÔÛÕÛÍCDÍKÍµ4\x0003øXñÙ0îx«Ç!_\x0008\x0002oÀgx_\x000eÒ3¾¥\x001d¦­øª×!È;r\x0012>\x0013©h¢½ãÛgâ¨ãUÕëPí¯ÃEÞZ®±\x000cGÇkùöi=J·¨êu¨ö×Ë©³îS"P÷«ÔvOa·ð(Ã¦ª×¡Z_G2¼tû0$§ºb¢0Û4Gá«^j}\x001d.ÛS\x0006FåÎÏÝ4ågFi?å×Ç\x0008g­ö\x0003G
²~6ÒqÂÅ²\x000e\x0018a
Æ
\x0010µx»øÁ[-*\x0011Îp\x000ev\x000b=:ÎP{\x0001\x00188GÄ\x001a!R[¸ók¿	NÁn$JÆÖî)þ vOÿ6ÿ\x000c\x00187m7±`ârß:®æÄ*\x001e0ò"L¤
\x000b+\x0001þmz\x000cøÖ'û\x0018é3à\x0002'B\x001a¹|¾ÑA3!VkÀ¾àl\x0017m\x0003Üà4	,*²EÊE·Zÿõ\x0005çºà\£ä°UããÍÊ/jÚ\x0013¨¼Ò«ï]_p¾\x000bÎ7³t*
n(ófõðF;´Ð\x0016\x001a¡iÞPçÒ*SZ\x0015\x0015\x000fÖâvp±\x000b.¶\x001fj\x001bÏ]bÏ\x0014\x0003;\x0006\x0014"\x0011è Ró$:tL|Ýû2{iWÛ¾èj5×ªç´&ö1ûQ<o\x0011³ü ]í
ôE§*tªU(j!r\x001aéEhiª.cÈau\x0014Ù\x0017®ÀéFp!0%ºÆv\x0019\x0006'"££\x0014¬Ll´\x0011Æ¨òbQéetÞ\x0017ÙÕÒíè*\x001b![áeT\x000eC "½ó<©\x0006²[\x001fè®2\x0012²ÑJL°µ\x001dWù$èçÀ²ÓãdWY	Ùh& Î¦ì\x0000l@_>¡ï\x0017£l¬\x000cl´\x0014\x0018òH_à©q\x0014ê¢îÆ)ÊRÈFS¡g\x0016%'pu±£Ìª,j´\x0014ÿjÑ¹JÝ¹Fuçl nsôIh\x001c¾³\x0004
·\x001bSÆÝò7)äTÿny¹.Rê\x0007\x000f\x0015vN\x0016E¨Í(ÏXW M;HeØp\x0018æO²z)Ä\x0002bÔ1\x000bù
c3D\x000bc(üÉÛ6Ke¸s\x0006¤;Ð¶ù¥F\x0015øÁRlöpû×7\x00173¥èÛ¸²ÙYÑ\x000b\x0016K£q\x001d`§ÿµ
êRýAáÊñ¼Í\x001b\x0019Ã+\x0017Z$/ûªWa¶Ò]Pº?(C\x0019\x0000\x000bßä}`_y8È5)Ú>L\x0017i8»À\x0013óFúÈÓ_à¾sæIÈ5³\x0007(×\x0005å\x001a@aºÎ\x000e,B$IÙ\x00108Ý´î¦÷\x0000å» |ÃÙiÅ)Dìª¤\x000clÀ8&2ëbÁ\x001e B\x0017ThT!-ÖðÂaðÁéø¼_ç÷\x0000\x0015» b¤°ã6ß)u0
L\x0015\x000f:{µÎÍÝ\x000eª\x0013÷¡\x0012
¨"KnÀ*r¸\n\x0012\x001d|©d­:\x001bt'N§ÓUÇÞaÃ+­\¸¸.`éªÒ²Ay¢	\x0014$«Òz\x0008²*wÝá'X©*Ù «Ô\mD,ÁA¸r¯ÖÔWû ²\x0015*Û*òTN{\x001c)·\x0016¹2ãÔ`­.+\x0005*\x001b4(\x000e®hºUÙ\x0003x«|«cªô§lP _Ö$(9.©4ª Úè_õJÊ\x0006
jà~\x0006\x0015¸
2\x0006msvMøÑ\x0003U¥Ae
µhl2§\x0006öKS½*jÎÅ[·&Ü\x000eJU\x001aTµhP\\x0004B @WQ\x001b8Q+\x0010ª4¨jÐ V;ä²rä#P©z°JPµëÙ >­pÈZPéHL\x001f8\x0005Me°C¬*ßS58\x0016\x001cÌÙ¯³<\x0018\x001d\x0017Éì\x0008³¬*¥®\x001aºYQ¢ìÁDYnº\x001fn\x0000U¥ÔURÇáäÔ\x0001ÄfHW\x0005E~\x0015ÄÃ\x001f`¥ÕUV·ÊPL£#5(ïT\x0015L|(ªJª\x0006
j± O0»G+zAWQ¤e\x001e¬Auõ\x0006uË\x001b4<\x0015\x0000'\x00189 Ö\x0013\x001cî,è:þkxØ3À\x0006'¦)*åq\x0000¬±ðöª\x0014Cöør\x000c[SÿÆR|\x00138¯ï£,ñÍ`%Ý+h®
\x001aò%?ã
Ñ^?ÃÍWK\x000cõ­àçKàð'ý=\x0008Oy\x0019\x0000\x0017J`([*Ð2Æ\x0003ölf
þ²¥ì \x0001¯\x001byÖ³¿¬Ùµ±fÃUæ\x0000\x0018ØUCÐãhLßà\x001eDö¹\x000c½9;<¾Wrù®©W©¶Í\x0003gNHqDÏ{qk
+Y1ÜLÊå»\x0006àZîõ\x0011\x0007b²\x0005(c|¸­½XáW
¤M`k3µ¿J¯ßdïÐù`8i³¦Ã¯\x001f´¯/³eÑ½¥õ\x0006\x0014Y¤á@P\x0002\x000b
\x0000pxü\x0001\x0000_¡kD\x0003Ç	¶\x0004Ü¼\x0019T\x00041Üá\x0017qù\c£ò-mÍ"\x0019â ¸uÓË5­ý°-É-¶éÞ3IØ+=\x0010¡5MU y·\x000e\x001ftÓá/{ïç÷óÇÙÝÞÑüãÝüqý¾åÔg@]¥¸Þ\x0010IËú¤YÝ\x0005q¹÷~z2=\x001cí\x001dM\x000f¦gëV/\x0017¨ª\x000bU
ØIr\x000b]Äþ\x0003²þT8+ó=Í8M\x0017§\x0019\x0013Á%7X\x0003NÍ\x0012ua'H]\x0017©\x001b\x0014y\x0008ò»HôFP©[M\x0011ÜÉÙ.Ò0P¦R\x0000©àÊÌ,dìÊÀ¾\x0015ê"w^\x0018«\x000cR2r±çÇ¥YÙÚ\x000cµzQrèòo£×\x001fÞ8~SÑ\x0014ÂUJ½/V%dÝS?è(ªÃG\x0000:ß;x|Ø´\x000b\x001a\x000cOD²2²âH,½Âí?<\x0003Ó½³ÓµCÊ\x000cNuÁ©FpÈL±¹âX\x001bÅäIÂ®jpkÀ¦»Øt#6\x001d8$A\x0003Éý¼f!¸\x0015O¦\x0001éb3Ød¤e\x0000Mq£,@£'Üª^Ô\x0006p¶\x000bÎ¶\x001f*õº\x001b[:*àT¹\x0011Úø\x0015\x001a¼\x0001ës­3L\x0005a<¦Ð³àd\x0011Üª©\x0001ïbó­\x000b´û\x0000\x0004gØ÷7*ròÀ¬ê£h\x0000\x0017ºàB#8»¤Ä\x0006Ä(´u\x0017kZ,97îTc\x0017\l\x0005'ÊÈÄñl\x0014íO\x0005p«"ôþàaË\x001aX´¢³\4A±õ5BðXÙÖÞ®¶\x000f\x0006*mü"Ñ(P\x0019Ä(%,+\x0003![-\x0004,q¢\x0019$,9YbUH×\x0000®²\x0010²ÑDÌFRÞ\x0004Nò&Vá\x001aÐU6B6\x001a	\x0011³Õ`K¯ç<É¢^ºÜ®2\x0012²ÑJà¼\x001bõ\x0010à£ böTÁÄG±ÂÏk@WY	Ùh&pÚM\x0011:ì
tN1º°Ê³k@WÙ	Ùh(\x0004\x0008}:x\x0014ñT9ÙUÅ\x0006t.ÊXx<ó\x0019]()pçX¡øQBUºX5êb,ïù`­PL=¯]9×q\x001e§ªT±jUÅ\x0017\x0008À­Óhn©xÀèü(SUÊNµ*;gßØÅÄ4Ç
87J\x0015«JÙ©VeçÊø¬\x0015¥ÍF[]\x000ev\x0015s@\x0003ºJÙ©Veg\x0015m>Jè\x0002=XmuA7Ê\x0003P:Q­êD*â°28BUGÅã(ð«jì
è*u¢ÚÔà\x0010'\x0004ü(HÄ!\x0001B§ÆyÅºz²ºíÉþëÑUÞnóÀ¯ôorÊÏb\x000b/\x001d¬eÿDUi\x0006pu|Ý¦PÒ¼\x0005\x0004ÂDN.Ð\x0013u¥PtBq\x0011 og!¤ \x0006\x0001U*¹ÒóOt¥PtBq15\x0013ºÙû<\x000f\x001d)¤+Ù\x0002\x001aÐUÞnó\tJó\x0006mÂS*\x0014tã¼']\x0005²º-{Çã¨\x0006;îÙVÉÈàü(ÑÊ?1mþ	Ó\'²àÚ\x0015pÌß-m\x001cvêVO)Ø©\x0015õÉl,y
°\x0017'ÝKÄ¨V%¾[<¼eàåµÄ6\x0002\x0016$\x0016RÉä:¹ðôÆ\Ñ)l1ÈNe«·«ÌW\x0011\x0002]½\x001d[^\x0011V
\x001fµx|¯$©Û%i\x001ds~£ËÌÌ$\x00177°ª)©%ü
dûT¡d§@ùÈ:ã\x0014µãôá«g£ß
øì§_¶¡î<$ \x001f\x0007ñÕYëæ³\x0006Í­£j\x0005©mËj[qjÛ¼Bh\x0006	Q]v¶ÍKäDb»¬ÆÕ3ü2Hß~\x001b¥ÁbP¾;LTå6®j\x0019ïQÚºr?¨+×?Ï_ð\x001fÇ³Ûõ\x000cÍ:jÁúq}
Â'f\x0015ÀÀ+V?#QóåÞñäp\x001dEsÁ§ºøT3>~³\x0019¡DÉ\x00001á\x0015¶v4@Ý\x0005¨Û\x0005(8g
«§e­Âq\x001aAÉzò ¦\x000bÑ´ËPY&&\x000e"Pâ\x0014B1²p5W%\x0013Ú Ú.DÛ.E\x0019R
¤¨(£MkD W\x000fì4At]®]Ó
 E&p}j\x0011â*³ÒÐw\x0011úv!ªH5hëe <ªpm\x0003!aè"\x000cí2tÖ,ùÈÁ(î\x00036º~Î±0\x000eÐ¸óA×Û;Þ\x0003«¤ó«:ÛZ .*HIev)\x0006ná\x00001*òp\x0004îf1®*Ó´a¬ÍÊ\x0000»âA['.Fªs	/#_EkW·î4@¬,l7-¸p\x0016Ùyë)u\x000eöùíX9
Ô±2.ruÜCn]à\x001d#\x0002GHfå\x001cq\x0013ÆÊºÈvóûÉh3·&s:\x0008«\x0016+©D VÖE¶\x0017\\x0011L§ 4¥¤«ð¼pNa{ÎXyíö\x0005g
QRÆ\x001f®`10b´#!+\x0003#Û-\x000c(p^y´q2\x0018ä0&Å\x0018+\x0013#Ûm\x000c¶6±\x00154:á!èóq%q\\x0013ÄÊÆÈv#ã<AÐí\x0014Á\x0014;-GAUÙ\x0018Õnc¬äIò%rC£p&,|Ñ\x0018+\x001b£Úm\x000fm5>ðÜ¬,¢\x000f¤y°z,Æ:|i72ÖqÓB2ùQ{nA;8ZQí6Æ#ÝlV<\x000e;{²­ÁñÞ(¿rà¦	cecT»Áe/í`>gÏËÔA{¯\x001cWj\x0002XY\x0018ÕnaÕDY\x0005çÌ\x0001\x000c6ÌÖc
µª,j·0¸ÐÇSf\x0003­5\x0017AÞ\x0019«\x001aUeaT»\x00014èå F\x001b5gï|\x0019Ç§$TeaT»q^Ëh\x0015QÂã °ä2\x0016cebT»	Ø§J\x000b¥°Ïï#\x0013m;öÍèÊÆèv\x001bã|¤¶Z£ º\x0008\x0017ÖI¹©¹	cect»	©|­]PÁÃ£a\x001bcV\x000eR7a¬ln·1pØT±` 9¿\x0013là\x0014\x001cíÝê:KÖnd\x0002²\x000c\x0018\x0005úI±Ø\x0018=:{¢+\x001b£Ûm3y\x000e7\x001c[æu\x0010àU=ºRáz
æ¯\x0001ãb'/y21:\x001eÔzÔíêÑ\x000b[0êÈ¹¼\x0010)\x0014£M¡©TiW=AZ*\x0012¥=r¼\x0019V\x0015õèÔX×ÑTÏÚ´?ë ,Í\x0014Y¬ÿ\x001a6º¨ð\x001cÝM\x0018ëÌrûÁÕ°.»=XÞ§~f8²óntÐjª7cÚß\x000cNãÅÖÈ¦°èe¢6Õ1ío&@\x001cHëÞ!á®uáYM\x0016ÐÑVoÆ\x000ex3 ¸Ù¥p¦¸f\x0013\x0014 9Æ¾k[½\x0019;àÍ8_MvFÐªâÀ©Q°\x0012c\x0013\x0014¶.u\x000c\x0008\x0015^µá¡\x0014¬\x0012ÆËoÚRÌÍUdµÂÔØ0FpLÛgSc#B©ñ^\x0005À¼ZyÕ\x000c\x00137¸S¢\x0002ûÈs¢B\x0007\x000e\x0018^ÉÆÛ\x0008óë\x0012Ì¯#söq£ÎÙNä_`>7K\x0013wZSNÜHâç\x0017fáG1¾´Ð­ªSy¡;£Þ»Â\x0010j\x0016"n÷RÌ$\x000cñöøäý+ z\x0008P',
ùá]\ 6\x0005ËÔ¬d³nK>¿ê@EÒòL\x000b\x000eÇï¸hÙZÆñU\x001bÿ
©\x001f$Tä2uØÑ²³^r\x0019ãÏßwÛº\x0008j° 7TËõ\x0011L\x0017ä>>0I±¹£kÛÈÐ²$Õ0èüÔrçºd6ðYq3ÃJúF¨\x0015½\x0007£]â÷hè¾à,u	:Í\x0017«\x0017µ5â}
v\x0000R\x0013i\x0015ºõà×S:\x0013~|Q9.YüØnñÿõe	@yµ²Ùà{\x001bK\x0016SIZû ¢%ë\x001fÆºóâµ\x001aôXZLyø¶xP2\x000e<\x0000é×4ð1áü8\x0017rÅÚxÆÛQÿãá¾Â:\x0004¨-[à±ÄGR_*qÕXYcÝ§~NJµ?'«Å"Mlí\x0010ÂNjDE½?\x001eåÕ\x0012Êæç´5³^	ÁiÕX²5ãQ~\BùqH\x0019Í\x000f\x0013g\F3ÅÛÛ\x0001Êç%ÍÞ3Î_xÊ|¢È%-\x0007>¾YCé¥{©Ûï%Æ\x001fäã\x0003:Jiã¶ßÀõ¾l0¯`¶ëy [%ó¾\x000b\x0011\x0003¯@@¾óÑeÉ%i\x0001¯\x001c¥I?MÝ¹6ÉIc\x0011×ð¾4¡¼ZBÙ,Lô%	Ó)ÖEA:¾jt©\x0005`~]Ù\x001c%­á'\x00165ÌÿÏÜ»%Ýq$\x0007[ÁãÌ\x000b,Âãnýô¦P\x0006\x0014@úEö.¡
Eª@@6ê§y%Ì\x0016f\x001b½^I»g¸ÇÉÈqNxæ_-J&+Ô©\x0002ígø%<ü"/½\x0017
Ú«Öb~Ù`ªõRïòb×$&*ØÌÓ!\x0008þ±?A4éM\x001aDYæt\x0018\x000cEÅj~ÞÆIpèÚæW¢§,\x001cÉàÅ¼Ãî\x0018FÝ«F/O\x000f\x0018Nk³ÝtQ
´Úðwüê»Óï7z»I}Xl\Ñ¸fÎ^òËR­Bt	â\x0010¢x.ì/¦¤\x0016Å.§¾:\x000e'ø"Qq6·¦\x0018\x0007¦\x0015~ï\x000e0ÕUoI\x000fÝÞ\x0001ïoãw4¤P\x001d»\x000bÐr§¯\x001b{÷£wwJ²yJ©Õ\x001dµ7ý] JÞ+Ø#¤x1âè3Õ&ïÔËa\x0005·;[W·¾=\x0002åÈ\x0011\x0008·®D{=ê\x0011EÒÌv0ð>¨CÿÖ5\x001cÑ\x000fýæ¨OÏ~|¼=¤ØñÕÝã%M^4SæÙíuÕ­Ã?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ê>o¥¼}ÿl&io\x0017È±\x0019\x0006ÇÆåT"æbö\x001a¥ Ñ(p££Ø\x0013sH?.;\x0005\x0015[¨{]ê\x0004g r(½§	%\x000bkÿ´c¥\x0004äZV6å\x0007v¸É\x0007ò`ã*I½Ç\x0019JYhµ¨Øj\x001f¹¤Àqú\x0019\x000cdw8\x0006êQ'Ìi Ie\x0015Í4©¶àÜ÷Ô\x0011¬¥\x001e³z_\x0005^\x0000àhñZ5«ùÂ¤Q¬\¸WÉê¥á$3\x0015,¶ÙÌé ¾\x001eÎ·XS$ÏNaÕY\i­Ä\x0001£\x001aZ\x0003Nõ×îcÅ[¹°\x00060·&£HYà\x0007\x001bNd·û2*Æ°r9`-«1Y²*\x00174Ú|GÄ\x001e\x0001\x0003KäÆÀ"¿jK è	B\x001bY*6\x0013ýSoÔ|'\x0001F§Ôc\x000b<hZ±\x0006K\x001bØÄJ_2|gY0\x0003j)P%ßTcGÃ@µq®¬Ù}á1°ð¯RSl\x0001¶¨»
FyxÚ\x0016Ø=oþ£`aE©	Ç¬Çl
2\°×¨¾[\x001aÍUfÌÊ(XøW©	G-8¨ \x0008´¹]\x001eÎl\x0011ºÓÁ/IM0]Þ¤ælùH\x0008¹¨ÂV\`\x0003ó=\x001b,
³ê	~\x0001öF 2Ye9ÅJJÇ%ZÎÈe A`)*\x0015\x000cö°N°¢(D3ßaÙ\x0003zÇíñeÄ\x0011¬ \x001b¶Ä³aÅ|Æ\x0000kTõ\x0014Ë¥\~ÖÔ×<³Êâ\x001dÎh\x000bPZOðb¼\x0011ô,)(YX¢ "Oì|n7j7ê)VÖÚn\x0005×h¸lY÷âbïHO1²p"xSV¢*\x001ac\x001c¯\x0019].ÖÕS¬s®jFtQ\x0005ÝìÞÜë\x0011°Ø\x000cÐL1²!UçU ñ½&ÅÊP\x000c×|K\x0016m àÌbõ8ß¾à·`Ýîªèæ[³pà<3\x0013YïÕîH°tMe°³²{ÂÙ£`ÁÂIþa,.ðô¼\x000f\x001bL²\x0017#ç\x0005\x0013k¦Y\x000c\x001a´°ü$í\x000evÆU\x0000\x0016ÖL±²!\x0014V©P<D\x001c\x0018uÏk×\x0018VÞ\x0006¦°¦Õ¼½$Gb¤\x000fEm_Ç\x0018X°\x0003v-\x0008"r­¸r\x0017\x00016# Ø=ãq°0n;Á\x0016 ª!X\x001d¸ÀE)®Ä°VÏ¸\x000cÀ`Û	¾lªÀ\x0008E·.Rõ§;Ýºùn4§g'ø²AjzÑÒ"A²\x000eJD>lõG\x0002v­´S\x000c.\x0015Ì©-\x000cYÙòXÿÀ|°`°í\x0014KkJfe`Y]·øÝv~ë\x0018Tì0è¦Ä\	N«æ÷yWfu6³ôÝÓGõÅ|)Z°¸\x001cÈny.æ´vOAø(Z´S^<à~(H\x001bÖÜõ,\x000f\x001cØäÀ,¾ÊÐëÜî\x000fð.Wo®\x001e~Ú^c'Û·ÛÛÑÕ*ÒÓÆ\x00003ÅfDvô\x0010¹vsuñbu­)Ö«uOí&ú
ap\x0018ë-±]aáÃåíåèë¯ÈmQQ0Ïµ\x001dK,,ù©=/ö\x0017«¬¾\x0006ÿh}Ô-QøU_MæãÏ\x0018k û,¢påJÜkÇóë&¿þøåãõ#yý¬>\^ÁçÛ±\x001d\x000eî $ÿé5_ñ¶åÚlzÏ\x001b_½<M¼:\\x000f@WMt5\x0015]ò\x0013¶rµv\x00015ß®E·Mt;
ÝÃ
JÆ\x0012Y\x00114íÞ5Ó¯ð7Ý5ÙÝDv«\x000e,­w8©J8õJ¬ï\x0017Â\x001dÉ.ukµëðDRxÀ\x0011»T»ÀKï\x000býXöÖS\x0017Õ¹	Q~\x0006/\x0013_î^ý¯IcÙ}ÝOdwº,\x001a°3.¨ðWØ\x0019\x0019[ðñ«W-û®&\x001aøÿexÝ²ðz¢Çw\x0008ÎRñ¬Nêe»öúg£ØKÃF6ñ9rÒµ|éÀ\x0018
Biî\x0000\x001bv&#o\x001f­6­©}7;6WÛãë>\x001d\x001cz\x0007¨\x000bg9wì¥ñýÏíÜÇ;{7Ç«³Õèæ@ôl\x0003¬ú[áý%¡u\x0003±ÍØy\x0006Â]íQKÔd¸¢«äÃ\x001eo¿f ²õÈ¾\x0012'r»l¼8Ê!Y8Çù~-æ#úïÊûûû\x0007\x0014Å~½½\x001d­®©\x0005w¥@)l+UFÐ¯\x001büû\x000b¬	y½Z÷Èi\x0016xÕW_\x0019¼mÂÛÉð%Ó\x0016V\x0012¿¦c.+g«ô\x0007ÆÒËÖÔËés¯,+\x001c\x0012}YÃ\x0005ÖÉol`ü­ÏÆ\x0014ò)ý¨ÊÒé\x000f§
§\x0017R]wI¯	~»¹&\x0003
Ã7Ur¿%QÓïä~ùD Ä½X-OÈ\x0002a\x0013ñe&.\x000fÆèæ`k4ØÞè¸é
Ö\x001fp\x0014hïÅfÜh¤xtVKQb)\x000f³ÛíÝÝÍå89*p\x0002\x0006jÁÙ\x0006q'z¿÷\x000bA9öõêüüôh½\x0017]Ë\x0016ºÊnÔ\x00019\x0018QË%Yb¿A\x001aBÿ\x0006.­ìyºe>{¢O?á\x0012úv{{»¹~7ò0Öá@åþÔMØPÆ*\x0017bî)YAá§\x0017øß®ÖëåÉ7{ñ}hâc}ÿD~\x000c¨¸\i#Åq8ýï½_àHôÓø²\óìãíx"|	Ô·£ ®áJX\x001dûÕ¡\x0007\x0000á\x001fÙT)[6õûÍÛ_\x001f°IÈÍÃÝÝv32\x000f-b×«Pq@±ä\x000ffõûåá?.°=ÈéÅùùjÙ\x0017VÏ#R¢9"%æ\x001bRØY¥¨ÊÝÁ*6L±¿¸³fHÂ=>ø\x001c~IËOÛë\x001c¬Î*d#k©¬	|n\x001bGoÌ"\x0004®Ru¦¿\x000fÁòõê$\x0007«³\x0016YCº\x0005Þ¾I;ºIOeSR\x000f´v\x0007,\x0014ê`\x0010|ÿUt\x0010||\x001c_©=
×õGÑ\Ë9à&r\x000e8ûJÖö\x001eÌM}FºÈÞwáL1LØ\x0018$K(=ßþô\x0000Óþ\x001cý¢Ç:An8eB)\x0012\x000eÍ÷{K±¯^\À>Çæ>=øäNìðáLÆö¯7WeÅüù_#\x000e]ë\ãæX$:N­1±?|txzÜ\/ûà½jÂc\x0011ê4zL\x001b'_Èþ4EÂÉþ·ÉðÁ7á±Ûü4x³ë-F:%±¨ÇïIÀ\x001a\x0007a\x0003>ù\x0017¤\x0003Þcoï\x0006&ô?Ï\x000cÆWÉÌ\x0007QðaÁOÏ^Þ<\¥®ÇE\x0011z´¹\x000c\x001eÇ`ë¦bl.
k÷õG}_^\x001cç?eYèýãÀÌÆ8ðÇ\x0019\x0006
I		Ö\x000fç\x0017h'¨þ·¿KSÅ8\x001a§W\x001aG>½¦\x000f$¸ò\x0008Ô=Éæ(IÌ&É³ÙF²°¨ºPFy\x001cÈÙ%ø§ÛÅÛ±§\x0001ljKðdTKCR©|Ö`öýñlÔ²]¯\x0016/Ö§ýG¶ñSÐ-çþ¬·osÛº7#8ZY?Ø\x0008ÜÝY3\x0000ËÇ³rÚ­´^\x001dæëñspÝÆ7?üüî×«7¿\x001bñlw©\x0004òÍõ}ÊNQä©ÇÔwÿvöpyÀ.I3§z,i=v³Ä@/>yçTK¸\x0010/
tÏ\x0017g\x0017G¯Îù.	¼ËW	)æ\x0007m7þá1+øÉßß\ÿú\x001a·wqÐAÆM\x001dötÂ5>·8\x0011Fú/äDZ¸ðÓ÷§'ÿ¸@Û®\x000e'æ7áG³½ú¸º1\x0017Óg\x0003Ó\x000b¾Aô×E?7Â|oÙæÝ°Ñ¢Í=dþÖ´¿Ü\ßoß7æöðò>/\x000f·¨½8»ÚÜo®G,
\x0007¶;©ÉÔã3Ý\x0000[å\x00170À_X\x000cÆ><zWÅË5j`/Î¯'=k£Ágû«åçRé¯w\x0000T?ýÕ\x000eË¿Þ\x0001{¿¾Þ\x0001P9ó×;\x0000ØÀêëÛÄW7ê!4\x001b°ÍÝâð=F\x0010\x001en£cxÌ^\x000bÔ\x001d\x0016\x0018sï1ªù)£xÍùâð;\x000c\x001e\¬\x0007QgY¯:X_\x001buõùÚ¨so¼¯ú³~øý³ÿò6ñòæú\x0001\x001b\x000e·!Ö\x001e	\x0011:E	É\x001a`AÜ\x0017iî\x0012/OO.°	è\x0010Ò¼\x0003ÿ¶¤o\x001en?ü¢\x001as«\x0008p!¼ØÜn~\x001acM<\x00086»åØ²ÛeXê\x000b´²Ë+Ï\x0003øóåzù¢Ç ~øùjûã\x0013´ÕÝÛÍ\x0015õ¥\x0019ºjUÖÁé¥55íÃUëV}\x0011x|E[\x001f.SK.Ük½WéNÉ¢O»¸?Ü{`«}$	ÅS,©Ñ tÀ\x0013Ôa%O±r±ë\x001a¼øÃå\x0007öÚY\x0012Pì\x0002ÿt»}÷«|bÏn¶÷#ÖGMCÔ\x0007-gËÐQNW¯zÖ\x0003ÜÌ¯üð\x0004çáçc.ìNQö<L¥q"½
Á\x0017öTsÕKzøÏ³¾Ëú&\x0006ïÞ6H[%F\x0003)½Êz?@	Öä°\x000b9Ý
(MgXaoaQð	5½áIG\x0015çQá#z&¤¶I0_4¬#¤®ã	±Ø@Qð@,æu\x001fNÓ¾\x0017_$\x001bÕ\x0011>¡H7<¼·\x000cjy¨\x0012Ý´gâ\x0017UOÊÐ
Cç0© íjgy\x001dúX¶õ\x0017ª8u¸Q*w
\x0018\x001b\x000e\x0011¹@9^(\x0014Ç\x000b¿H©C|J\x001foà$ªÔ<!:'gB4¶Ð3!¢hýãáaèsHº:ëoÑÅÓ\x0011¿x®­C|J¹oèvÎBxH(ØÞx\x0019y7!ÓU\x0007ø\ß@@\x001b9\x0014_³ Â\x0010Ù+Ò_TÖ!¢h~ÁñDeeÒer\x00191(Ã_³xÑQGøà@Bi²(º\x0011$\x0017É5Ö\x0016?b\x0003E5\x0016G*öÔa:-yf"x>gØÌíf£\x0011áB% dêXí²Q´ÁF\x000e|Ñ^i\x0004dÎ\x0006+ï&geØoo\x001en\x0017þ\x001ftx\x001f~\x001fn~´ÈKÒZ,ÇÌËÒ\x0007úÒC§KöíéÅz¼Üßñ&Nñüñáîú¾éæÜ,\x000eáØ^=Ã\x000cÑ\x000c&\x0008ìû»ûÛÞÿÛÕößÿùß< ÚÀÑ"c\x0000ÇZK\x0004¸-ÀV\x0007àÙ|qX\x001e¼Z|\x0001|«W\x000b¿ç«ÿ¸xv|º8\¿Z\x001dwø-<òqÆãYMP8R
*àãj"4ÑÍCH>ÎxBl\x0003kÐ\x0018	\x0018\x001cÌ½Êa\x0016ÀâãüÝæðçßÄöç_·
Bßn\x0002bÒh\x0012ÿ\x0007@Ø
Ô\x001bL"f\x0002\x0000 *7ey\x001ap±ÏÃå\x0010>Ú$£ù¢D/\x0016ñ¢ÌGðn<ÑéyàHJ{4\x001cª\x000c9¢ÓF\x0001t'OgaÉ|´ÇóåV0ÏR\x0002/|¹(ù¬6ðx>.¢È§\x0002©ä\x0002±Ä'cÏ\x0006\x001eÎWöïøÝ\x0011\x000fÈH#`n\x0018²\x0000ö\x0018é}7þ÷Í§öî}qµ½¼\x001b\x0003èw2à\x001a\x001ayH×\x000bøâxut>°ìß±.e¾3¡%Béc!ìý\x0013æp
aê\x0005\x0008±É¥"BÞ$RÎ4`\x000bl\x001d H\x000eW\x0002ôt8ý´3¡Èáºé¤Ó?Ð²\x000c%Wå\x0002¡äeHq¯éÅÒCsÀÇ\x001c\x0002Àwl\x0014\x001fsf¦/\x0019\ßX\x0005òæ\x0019PDÔÖB@\x0017"o\x0013¡záò7whnð/5\x0016G¥PlÚÏþ\x000ed¥Ën	S8µ}óÛ¿4ÏäÅùÃÛÍÕûÔeøTP=ëy.ÙjkÓët_\x001c.¿[u½v´(s=R§¹L\x0019©Ã+=Sö_\x0000ÆP\x0016\x0007»2ËÕ"¥TåR1"Qö;°{)??<|üåM;\ÿû}ll\x0000½0\x0017=y9AkB\x000cÚ?H\x001dWbÅO¼\x0012(þ[â5âJ#ùÆèz¾'\x000bRÇ\x000cLglM}ºl«I×h÷0vöLÒ\x001c\x0002:\x001b\x0015\x001d|8{ø°Ç×\x000c|»ÒøÙsøL'áìáTæës\x001d\x0006ò='$Ó.Ò
9'\x0010cL¾ÜP?y¿û_}wÕv®±
xñúr{õ~ðy'
&6;ÁHR/A;!ù\x0006¯{\x000c`®ú]¼>Z\x001d×}êmµú,7Ofà6
::6\x0015Ö%WLRûOôt\x001c;\x0012ºûXÙåµî)VÞ1·zãMÀÆ\x0002Ù4Í>FJuF\x000f¨CTÝ³<úÝ/¿Ý~\x000cmê?ÿÄÏoo\x001e~zØÞßß\x000cf¶XáîJ\x0008/·ÀÛ«ã¥ae÷ú]"ïóõéÅÕ«W§\x001dñPñûå÷o\x001dÕb¦
LØbØnÄ\x0012VM¨
|KXÂÃdZõx\x001a«\x0005¶¥[î\x0005|d\x0005Æ!bY«Ë.wÜ/\x0007ì\x0014­ZØz®×\x0014ô#¾	ñí§f\x000e*|ç¯.?^]\x000e^ `rÂ \x0010JO-ó4ÖiÐI$\O(`¹xutv|Ô\x0015õÆz«\µDeù\x000fR¾øæ\x00163\x001cÁMÇúç\x0011ß¹È%ø£t?-c"}çª'6z¸\cf#xëXöÜm·
µjR«zjMmÒJÕå°§k$@Çn_d4´nBë	Ð±D¡­÷ÔL1`C2ÕÝQ¶ÑÔ¦Im¾©\x000eMè0\x0001Ú\x0005¾ÙÙÌ \x0005{ª'4\x001cZÊGZÊ²¨ÿüo Æ3îþõ«»·7ÃmÀ\x00025ÇW)Vx«³-\x0017¾\x001e\x000bRèñ Ã±Óã\x0001CðÍ!ø\x0019`Îs¾³\x0006R\x0008r`ù8`«{ÌtÝ\x0010bs\x0008ñ+\x001bdÓ¥gïîªÊ\x001bMÞ¤hªð
ï®\x0002E·­A?i GZØU]}]ì¦Én¾.v×dw_\x0017»o²ûiìàºê¯\x0005\x001eså^`{læ8vóx¯G{uÔ³ ¦gA¹{IÍ\x001fóûîcª\x0001Ýã-"mÉ ÚÝ\x001dl40¶\x001d	tùR9W\x0010O&Å³\x001czlâ0`¥ÿêÞ%»®\x001bé\x0012
UäÂû±ÔºùÙô"%%%¹Q\x001d­+¶é¤%'%:nÕ4j\x0008ß?IäG\x0000\x0008\x001càH\x0017ç\x0015×%6Òiß´{ã\x0000\x0011@Ä9\x0011²2')\x0007}ò?n¯O\x001e_ÿyÿ?\x0017\x0004\x0004üÔä+Fe\x001c\x0017b\x0017¬¢ðI¯º<¥¤ñ×Ã·V<\x001cH\x0012OÞÝ<ÙßÜ}]\x0017\x0010®üTç¤¨ Þ\x001c%Zt
»'»ó«g\x0017=¤²ÙÍQ¸G Ï¡ç~öÖ\x0010ÁdÀ³' õP2¯=*¿=9wØt\x0004Ï¡¿þð¶x%y¸\x0019pX!·û\x0018Vô·'o÷ïß~½¬R%¡$î.?åÙ°½S\x0018¶8îÚ½\x0008ëúüÅÉãÝÓ'd\x0000"hé
h\x0017Ûê\x0002èK\x0018Èþáöc
l\x0017\x0000çqT\x0015,³\x0002\x001b­\x0012pnò\x0010¦Jx\x0001mÈ\x0017\x0017Ï.^¤à¶\x0007>k\x0017ª\x0002\x001e¶³à_~¸¿»»þ4\x001buø»â\x001aÃrsç³ÀÓ,ÇãFtì\\x0000ýòÙ«««³Shù`ç\x0012ÚhçVáUøZnôXs¥ã|nÀ+A¨s\x001b`©r%*\x0002*Ö¤~·ÿõz\x000f1ëãë·³·ç6'\x001fÃZ¢>µ6_\x0019Ôüð-í»ÝåÙî\x0015ªÏ\x000e\x001c\x0001dÍ;Úc\x0018håb\x0007ÏÍûÔ\x0005±bcìP\x000c·\x0002$,´\x0002õÇ´1:ÏÁÏ/ \x0017Ëðf¬w\x0016\x0016\x0003x\x001dD\x0007t\x000bb
\x0001¯péØc¥1\x001cã$qø\x0008\x000e¿Nb¬Æ
ZWae±A\x0002°T~â9è	«é\ßg58¦\x0017ÁBgØ\x00161¯³¼ßgñ«y".j²qc1
T0ãKê8àËYÞï;²Wâõí¿ÌÝÏÿh\x0013ÿ?\Ã¥1©)#XÁ^|¸¿ù\x0008hïïö?H`¥Ün4m!lã)ð\x000cârH¤\x000c«\x0002g¯Î_\x0000Úç»«ÝwÏbÞÿ³xU<npò³¯\x001cg)`ù\x001aqþúVüóö÷\x0014\x0016¿þ1g¢DQíû,^\x0005¨îçÂÖ^XvÏ½×ÇØ9)¥;\x000eÀÖÖW\x0006ø3ØYMûÕIÖ®ß\x000f=×üùç;óã¨Û\x00132\x001c»7w×÷¿'ñÔY°
Ü@De*
Ió\\x0018\x000cquÔ>
qñÉîñÕÙ«\x001f\x000eË¦×æ_þ§þU\x0001~òóõ¯QÏ	¢·÷ûÛëO©Éo\x0016h\x0005å)#©Dt\kÁ\x0010³æN\x001eÆüä»³Ë\¼ýd÷twqöòp¿x}wÇþø×OõÙ»®Åf.²R¹\x0012&\x0004\x0010>5È\x0010Ú{\x0017Ù¨ÎÞHÚG=-!ñÚÞ¾ÿ%u\x0014T#ðìý­)àè¯ªb\x0018B(¡Õ)Ojò\x0003ºÒõÎÝYXÍËçg\x001cxýö·?ÿq\x001f[SËÙýðñg£tÂåWàðwfín)4Ôæ\x0003ÌpâéòÑ\x000f"\x0015F~üõ\x001fíCZØ§\x001fÞ¿ÛM»dJßªÀ¬%}\x0019®ÎgSfD\x000f+ìÐgO¿ÙízPll@Û¾ª­Â+$ÏQºr\x0000L¯SÖf¼Vw\x000eÖL¼ÿüó\x000fûsÚªà%¸Øßÿ¹`\x000f\x001b[z\x0002VÐ§\x0011û`\x000fØt\x0007RNóÑº\x0007ÕWÿëð÷ÿÇ¿ÔÇO¿¾¢Ïïöïnng/§aÇþtp	áþcU:ö"7\x001d\x0004À\9_í¾9¿8¼¿üi?üñÇ¡\x000eÚ4Üm^L!¡C=nRÖÔ1Ñ[Ì©>\x0006d.¼]\x0001RFUé\x0004R¤ë:$\x0018y÷ -ÁXÌübFçúe\x0005rwQÑ\x001eÆä
ë\x0010³Ú¾_\x00002×®\x0000)d6JKtEa: 
\x0015È/öûÎýÜ._\x0000\x0014TÕÄÙrÑpæ\x0018Ð2Ó5DKP~©¡v¦¹ô"g¼I=y-EÎ!)+]÷|/Aù¥ÚkÝ\x0001ÊðÅcßN@)s«²}\x001f´\x0004äVç.e\x0019\x0005Ö¤âQXJ#¤¨íBR-©VnK(+Ì(½M]<\x0012Â%Di«2´m(uø\x0017é
GÜg[iRÊ8\x001eq´CLQmK\x0013ÖÑ¬\K¡r¹p8;\x001cc
_bbÇ<ÛùâôâùG<õ\x001d©\x0010­¥7`ØÌá¾dÛP²v Dú¡Åy¾jª\x000bâpÝH¥
ôÏcò2^7rxä}o\x0003\x000cÚ8ÏwQõðå¨\x00175xñÀÀË\x001a¼|`àU
^=0ð¦\x0006o\x001e\x0018xWw\x000f\x000b<gµa\x000f\x000c}cnø±7y¾Å\x001e:y\x0006\x0005©ÿº»^pY7L|	\x000e·Ë\x0010×é\x0004Üä}H8vò5("õ_Wgõ(+Ðª\x0006­¾vÐÜ}j$RÆ&þý\x001eâ÷\x000b\x0002¿pµK¾æY>\x0000\x0002¿Ü¥¬W½,)Jüû+\x0006N\x0003\x00175pñË\x001a¸|@ÀU
\= à¦\x0006n\x001e\x0010pW\x0003w[\x0007³í\\x0001ÎÍè¾\x0003Àkßé£ïÜ°äªF®2òoµ 0O¼1+|]\x0011Êæg{\x0015®Â©[Lrg4n\x0016P¬¡@.ØÈ 
VûLuòÃõûO\x000b2òLâË\x0011àö9Ù)\x0015Þç¤¶Óþ'ü¿=}Ùs@¬`µ×\\x000e[eíx°y£H=$\x001eH`§z¥ÚÙ»\x001aöÙÛ\x000f·?J\x0016Oké¸·¹ëI9©ô4ê³'Ï.úÎ\x001eeC\x001fâDF¨«:	Ð\x0017\x001cG~T\x0000\VYé\x001c
Ú\x0001åT'\x0001ô4RQ#\x0015«
~ª2Pß? ¤Âí zY\x0005HuT¯]SSfF¤>¸¦ÉU¶Ø[\x0000ÕÖPí:¨Å\x0004XId\x0012 \x001a´iÚv¬ñ\x0002¨¾ê×Aµe§:}êx6¶ãñæ#åíZw¨\x0004ÖÝ\x0006Ó¥ò«\x0008ìUÄjuÇ\x0008,À*\x001b¬r\x001dVåS\x0014LwOÅ\x0010\x0001+ºck:Vv\x0016T36\x0000¦\x0012ë~~óÓuøûo®\x0017o8 V\x0016x
ÈÃ}ÊIå\x001blÊ1¼:y~þíÙ³§OÏÏ\x000e\x0017p°<¾¾¼ê
ú%Wn\x000eYéÙøëW\x001cû¤\x0015\x0014ILb~2qÕ\x001e§ö®Æ#¥hUV}íhMÖ|íh]Ö}åh«+\x0006Ké¹¯\x001bnc\x0014ø×n\x0015xsÎø×~ÐxsÐø×{Ò8Nu\x0018~8üü×ß ø÷äûý¯¿.¨F\x000b·Iº­í\x0010ãb+ziÙóËçPù{òýîòò ¢PYÔÅÃÀ,kÌr=æ\x0010ó¨\j\x0001¥u\x0019Kk,ï\x0004\x0010K1û\x001a³ßYÂ\x000bÅ\x0007Ì\x001ecJÑ»\x000eÏ\x0006Ý´F¥\x001fê
àÍÇ%ñ\x001ag\x0006WÛX\x000eù¶x\x000e%^1}/mÀÓQ<1\x0011°ÉÑÖf²ÞÚ_9ú<º2&lRîf*"r#\x0004\x001cÔ!õ#ñ&Êýd6brL\x0005^ÔàÅFð²\øTV\x0007y+y+1ùn2\x0013<Sã]¯Úz'×·\x000bµÃ\x0015%ç*4(GIpC±¹BÛïkOÎ.zuÚ\x0005·¨q-¸ÊA\x001d\x0005ña0Ãv=\x0013³\x001c¶ªa«\x0007\x0003ÛÔ°Í\x0016ØÁ_*Ü&\x0012Ò\x0011¶â¥VVwê\x0012\x0017\x0000çãmÂU{6ËlØù5Þ¥Éò|2­Æ$g· ræxØ¸Àv|.m}.ÂÅO·7\x001f\x0017`×%è\R¿\x000cÐ=vÚXÛ«OÆ5\x0007yo/Îë>«CØE]lÄ\x001e âº³!±zéÊ:Ù1ç\xY\x001bÁMãsÐåY©É,qk{5×óWþ
\x0013¢jÿ\x00170R]äö8H=ÕLÜ-8¨\x0002ÔtÒº\x001b­°E*×Ýwúqxzª¸êô\x0008¼a2ºP¡
nÉ¢®á÷×û÷á.8¡ÚKBìyÖ/Òa®æÝîïÏvOaàÃAI®6n\x0011á\x0007´a;X(ãH=Þ\x000bîj<)\x0010+n=&×YXyÓ=é¿S{÷$dÉjÈÐbº\x00122ôwgÈQý,\x0005®48u÷ó2È¼Ì×C/M]~|
³Ç	e']Y4ÅZÌ,	\x001e¦t¯Hmô\x0001³Ð\x000e1÷(aV¦Æ\x000c:È+1\x001b\x0003^1u\x0018êS\x0003\x0012§\x000eÃÎcÅBÌÍ	T«O`ÔeI&ÃrÃíº+ÒÉN¸½\x000c³n ^}\x0004aDBj@
·\x0001\x000fce\x0015c½:ÿm\x0003Ù®\^ÜLØÙ&ogm\x001eÞ
²#hd\x0019ÚGÖ\x001eA~jñÅ%KÃÖ°h-ë\x0005ªs1×Â!\x0011s\x0012\x000eAÌÏ¯?ÝÌÎ\x0018P
÷©êNÃ \x001c\ëÜ¨­ñ3¶óó³\x0007\x0015Z*Ì¦ÁlÖc¶Ù<k#ô)Bù>àX¯Pc!dÛ@¶ë!ëÜ@«uØÎ:÷ûA3b¾|ñ\x0019Öy\x001efÍkÌ¯Æ,Y®ú
ËÌp;3)\x0015®3ïÑs1Çú#YEsþ\x0011XÐç×o.×®\x000b\x0002è\x0000ì4\x001b°OR:[\x0018Ùln{ûùìÉwåÒÕÓ(¸u[oÁíDòZØ\x001cø\x000b}«Ö÷6õ|Ü*¾3ë!ê\x0008î\x001bîÏ!Ò\x0007Øß\ÿ¾¿`ä«1.ß³½3h£AÄø0æ«xQùæìÝAÑ/\x0000¬åè¢e¾¦¼¸¾K É1(\x0010»Ä­Q_
,;á¢'kðâì*áN2\x000ca\x001bÖ\
\x001fCCÌº\x00177I÷âäìãìkh\x0013-ø®\jEÖ	WnÃ0H_Gé³-\x0015lSÃ6\x001b`­Ka©~ìh¬CäM¥Æôªºâ\x0016¬Æ-ØõV(\x001a\x0018Ö[}Ö\x001bäeò÷ÒªKËfÁå\x00157Ú¢¢\x0004¬¸JY'^ÊªL­\x0002¶\x0019¸\x00125p%¶\x0000·."aÛÈ\x001c@ôo\x001c!\x0004®\x001aàj\x000bpÏ±<Z8ÕaÜ¹r6ipÇb&3xp\x001ep_ß]ÿíÙýõ\x0002à!L--Âäw`Ò5>\x001d0×ñð5òg¯¦±7F<`Ïê	ëÑC\x0008JRüÔÇ\x0012\x0002%)ºê\x00043Ñó×ïìÛ[|ÀZPI0x÷Ó\x0007@\x0003D9¢Ýßß]ÿ~wý·ÛýßìßÜÁcZ\x0004\x0002j«Ã¢z\x0018©-Â§ô)\x001fb¼½3òEQ\x0005@ý\x0012(®Î\x0002ô' ¢su\x000en=Ê\x0005ï®¾}vèm²Au\x001f¶¡å	j¸©ÔH"¤Yüaëº+E\x0002+a#Zª¨ f
ÍPó\x0016\x0008'p\x000c5\x0005z\x0004P³ÒÖ&¨&½\x0002T+R&,ÜÇ=3\x0019­ç\x0008m´
mÔcLhU\x0012ß\x0003´Î!ZéÐæ!wÛÐÚSk«\x0007´¦¬­¢Ú	y¬ÓV´Þ&´N¦ÇC@kÓx§³Î
\x0001Ú¬`²
-;Í'\x000c·¼m\x0008V\x0010-J&[×Öå}\x000b9ò²\x0013<ÂU\x0008.x°Í.ÌðøÎ\x0003palÌ«\x000b}±	®%Ú¸P0È7û°`\x0015ÂJ¦ÕÕé\x0007V\x0017J\x0012\Iµº(\x0018³
®AG\x0006Iñ¨F
p\x0015n\x0006nL\x0004pQeëêê
[×!Zn9\x0011Ú°§øvË¢¶s^\\x0017×Y4\x000c(ø*£ê6F_1	\x001eÑ
/"0îpq=\x0011Ü¢f·Ù¡a¼è\XãÐ#ÂÊ¨½m««ãí\x0007VW0´\x000b\x001e®&iu©Ì\x0002ÎÚÖáâZÎK0îU0D¡
ÍF\x000c´,3X:{\x0002Z§L2ª3
·#îQ°	-\x001fl\x0002	g\x001a±9$wi(WD«R9\x0014 -ÛV0ª\x0010|Øì\x001fòpñ\x0018,øô\x0007\x001b\x0017Z°
3Dî\x000c^gÄf\x0007\x0011ÂEtg<©ËÁâ\x0016ÿ'\x0013\x0013 
\x001fIlw\x0010\x000e÷\x0002,.(BD¸eiç`Ýß½½þ­\x00034Äâbs<îuÔ\x0012ëe9\x0003P	ÅyÓ\x00121(T=YØ\x0005*_v`8«ýl\x001bp¢m\x0000E*r³'s¶Ü{½HS0·¬Ä	T9%¨O]\x0019ÌäÃuÇ#Ü\x0012+¢ÛÄÒf_\x0016î8xÈ\^
pUÉ*x¢\x001c\x0008¼{ÊíÞÌË¤õ°\x0013\a\x0011.U\x0014\x0006ñÜìÎ yY\x0010\x0019&\x001f\x001f>\x0013\CuÔÂ¦Ý\x0019(1%iL\x0014´j/\x0004O&7{³d
0!&r+¬.	1ª\x0016\ÜìÎÂ^\x0010¸\x0017xjY\x0006¸ºl]*'\x0011>ÜîÓT¬¸Ë×\x0011ó²\vlnQ%Ýº\x0013Ä\x00157ñähQÁ}\x001bZ\x0013\x0001"\Êe`iË1sh'À¥ÚìÐ¼©íøö`Ðä\x000e¯\x000fThåVÛýÏñ\x0005ÊÂ]Z\p­'2
µTÛ\x001dDl=Lpe¹E\x0004W\x0013]  Ý®¶\?¬.+!¹,þÌ\x0012\x001d4(ìÒÛS¹Q>\x000cJòôW½ó¿üòéæÓè¡ww÷ÏûëÅPe?\x000f©;bbI0(Døxjï]ÒwWu°ÿ´\x0002\x001a\x001b*$\x001e±ÕPM¬t\x0001¨*
÷0y@{k~ñ
É~ºÿý]=CéòC\x0011çç¼¼Û=ðñÓõíâ=à¸3Â?åd\x0019®<ãuFv¬×å³ðS¢óòj\x0017¶Ãg\x0017\x0007W¹ÂÞ§iðK\x0015Ç\x0015À\x001e6<e\x001d\x0003þ8>.îaÛqmkñ§`\x001aü!H\x001fÒ,Ã\x001fÒ·õ\x0017ÁOíôÎJÜ#;$~\x001e Guä¸sx'¼\»òé-\x0004¿\x00171$K\x000f\x001ad.â\x0007ô¼öÆ\x001dvðïÍ/Æþ^\Ét\x0012@ÝÜÅùFËÀ\x0010Ïü\x0011n"É\x001b­q×;yØÌàX¦WðãùÕÁYG
ðvÔzàyÌ_Z)àÁ\x001e[¡¨Vðc\x0015òdl(\a¥c.IVÁ{û½óÀ±
yª!@î\x0004>0;\x001c6\x001d\x001b|±5\\x001cNa¬B\x000c$\x0001ò\x0010¡äÝâ Ó&ïsÅwRÄ»%Í\x0010 ç6WL8ë`%\x0000×®,¹=ìUWáN};n\x000e¢é\x0016îÒ<\x00027
­ºg32«§b\x001a\x0002äFâ^	7[|.
1lf­èÔÿ¬B\x0011Á^Q%g\x0017ì\x001fÖ0\x001auVF«ÃaÀ\x001aäXeC\x0001ÝÅÞð¸Ï-sS\x0012!áo¡ÝèXqCá\x0004V`Y¯!Ç\x001b¡örÎ­"VßP\x0018tY6\x000cÏ\x0002tÏ?F\x0010»¬Ä¡°è%pq0\x000f {Q%Ñ0æ&\x0017:èy\x0013i4
\x0001Kêt\x0001Ó\x0001c\x0008)@ÿb¨^á\x000e\x000eÓ8Q!°ìÅ9Ä\x0003n¯sÈe 5XZD\x0000\x001d:ÇÓ³h##r¥\x0004Æ[â#\x001aì9'±éàGóÃË¢\x001fÍÅ;¶ó¸\x00069ðP g¸]<WXÇ£u\x0001Þy²üú|ú÷êNÔH6ý~s
ÃE\x0016c×2í\x0016\x001dbõ\x001cæzk1UÈ:¯3pÓ\x000fçg0bd\x000eøa*ðvðÁ\x001e:Äï «\x0011ñCIxÆo\x000f^kñ§;\x0006
þ\x0010YÄoÒÓ£\x0005CÆ\x0011¿¦Çâu\x001aüÚãÆ×ð\x0002Á3~qÑ©RX?E¿Dø\x0011<O5\x000b6þû\x0013vÞIã­ÄQ$\x0011x·k\x001dî\x001d*Ã/\x0011TôZø9\x001c#:»%ªC/\x001fP¬ø;­\x0012k	äÈÈrê`\x0007\x0002\x000e$\x0012\x0001oÅ
ÿEøÝ\x001fï|[¿
.Òû÷ÒÀßI¼\x0010þf/\x000br\x000b)\x0007©\x0014æOíï\x0014g6Ò³WO_ÂÜß\x0019psGÍ\x0006¸à;³á,&¦{Ã=\x000fWÙéÞã[÷Ë:Tüµýç/?~xóÅ\ãó[\x0018\x0001¾x
\x001aIá\x001f!2ï\x0016&=fË"dçEc\x0007_À0ðË\Á\x001eg\x001a¿fØüùN³»º;0ìËýÝO÷×Ë÷2W2\x0002»à:?{÷JÿÃÞ¸Ü]}ûêìðÖ¨À\x000e[y5X¦1§hU\x001eá`â\ëÇÚÉöàP·æ|a#o2\x0017>8öBéìe4æ¶ì=1ÇhTØÛ|â\x0003ÀþÞ_»÷¿Ách¬G©#úñûÛëOÐU¼\x0014·W\dÏ"T®´Q$éå\x0015êÊìN\x001e?{uqö\x0012ú\x000fv\x0014\x000býó;ÅëìÐÅõ+§c»cF«\x0014Mi«1£ezågåâs\x0008¬üU}úGZ_(þ?<Ùßíº¿¹ýyù9t6x\x00147q#eª°\x000e{Á¨äQ¼4½+òîj÷í«óï\x000e
\x0004ò×¿]ßÿúÏD¼PN\x0019ë)AtôÃýÝ§ýòm\x001c6jÝ\x001e\x0000\x0007kÊ¼\x0002`Ëe¼¥z\x001dÃñäÙ««»ÃÙÛë?ßþ\x0004áõTªðßÿóÿ½ýù?ÿ½\x0014qØ\x0013,Ñ\x0005\x000bí©³\¼Â¢_%ñÃY8}9Ù3\x0002úï\x001fÿõ£ù3.-ÔRf
\x0010ÉúéúÓ§å'MÂ¤ìxÐ@²3\x0016"Æ\x00054Ö+ýÜE¥¬oÏ^¾<|Ð\x0014»³\x001fÿ\x001d\x000b%`ïÂ\x001f.?¼ÿôËÅ`m\x0013U\x0012Nfñ\+¤ÈE^áïtÃ_>{úòûg\x0007u"ùë_Ô»ß>ü«r\x001e»ûË`ÂnÞ/Æ	ÏÜ*::î9H!\x0001ÎàÿÝõF°Ãº{ur\x0019Ì×ùÓi RÄRp±\x0005*\x0004Ã:C
Î"v@[á|®åðÆwZYf`ýQÝù7\x0011+XØ'\x0004bA·û5°sÖ\x0002Vx8\x0010\x0006#á¼®ÚuÞ.@/èbw~Ø\x0006TXÁÅ.¡õX¡ð,®«°F\x0007\x001f°Ô ËÁò½[Æ\x0002¬P¤\x001c{nÖc
Þ©ÕæÊTË­\x0013&cíÕüÎÊÄÛFc"\x0000ýÏßþç¿º»YìjAZ¦N8Y2%Ô¥e9aÇ­éï³³o¯Î\x000f¢½sÿ¸ùí×æª¹ö6¡eé\x00029p¹\x0003Þ;Ìm^ç\x0019^#\x000e\x0001ýÃÜýr\x001fíj,Si\x0007\íß,/?³ÆÄ\x0006\x001b@ÊM\x0008+´Wù\x0005nÇ=¨W»ÇgÅ[n¤º{ÿ{D
A2)Î¼\x0008±Öûå.@0V$\x001b\x0010,V,b±à\x000fòç÷¾×Ö¸;y\x0011"­§}Àû?ºã\x0001$ä\x0000â\x001f^ìooÇXÊ9\x000e_<øª°%\x0015¶skÓè$\x0019^ì..:ÑÕÇû7¿ß]GÐ¹\x0004ØTÌ'°\x0013HÞV*i\x0002%fd/\x001dR\x00152\x001dB{ÿ/ÿéÃíú\x0001Æþ´"á\x0014<T~}
Ë\x0006Ô9_¦=ëE'?À4Óo\x000füwþÆk¤û(Ã½&7\x0016fiR±¸3Ù©|¢îÔîN¢\x00107dÄR\x000c\x0018ÿø9Ê>XRy[¬)\x000c¨Ë/«ÂcK ï^³æ¡ÌFËZ²A=B2ì\x0008kf^Ëî2k
mYK¯O¹*
\x0013<xÉ1\x0019ê:Nt.Ê,'´\x0005%Ôuå})D\x001aÇ\x001cPbßê©ÌE¥n¶ K?*Ý°\x0014é}ÉKWç Ïþâ¯ßÀ7³y9\x0019vF\x0004w·&Ãç+KpÌÕë=\x0000Ýo\x0003Ú£\x0012Ðá¤»Ò\x0012ÑEº@ÿùüMýÑDÍO~ÞºÞßÜBêjeHª|\x0004
!©Î]Õ1|Æè¹WÂ·{y\x0016n&1õBÓÏQ»ÿvw§Õ7\x001f~ÍO"ëoÓ ágrÞ1È	ÅëtjS
·éÎcæ7Ï.óÈp§îâÆë?\x0005né%´rÄ4\x000eV'Ü\x000cqw\x001e1çá~Ãl=¸¿~\x001c~\x0003R@«÷r\x001fk³\x001fïo\x0014ë-ì\x000e¼j\x000bïÚxÓ>;êõ^îbIöãÝ/g[\x00106oa\x0013àaW\x0018v	&rfVÄ¡\x0017Ûv\x0016|\x0019p×\x0000w\x0004ÀÏ¯á\x0006¦OeÀE®ÅöV\x001c>Kß¬Ã_nn$ÏÆ:Då
s\x001d\x000e÷®s:Aw-tUWaogÃÂÈOSB8ûåp\x0008´\x0008ºh6:üåö\x0013ªYn$
·<\x0015Ã
/B^w|ù2èª®¶C\x000f7_h¯I	'¦é\x0004/d1ÝDtF!\x0012©O)\x0004%©\x0014p6Ó1u¸êÜz<¦\x001bW]¹ûo>6-\x0007Éé¿gõo\x0013NH¨M%·ÌÀÃ7x¢\x001cOy%{µ{Éï\x0003ï)Ã\x001bÅç¾¨@\x001f^'ÀÃ;\x0005K\x000f+!Îàá"¡çÃÙèßÐ\x0008Ýú²g\x0004U^ðÄòýþîÝÍû@$\x0001~|ýþÃÍò6O\x000es¤\N³©,u\x0015nÚ%ËÖ\x0017\x000c×÷»«oÎ¾\x0000:Iü÷ñÙÓgõ\x0010Ñ\x000bbb\x0005.¼f\x0015ÿ`x\x0014LH4\x0018IõºçzÄ\x000e=\x0016b~DúÁe.0&°ç9\x0006­übSÄ\x0010%\x0012\x0012v¤Ä$j1Jxf5\x0018¾­òN·\x0017\x001fñâÔ¼T~#
\x0001\x0003Ç£²ØHÍMOk\x000b11"&ÉÒã)\Ñ¹P¥G\x0002pCLIbbvZ²\x001d\x0002ÅF/_L¹ãØ*²IÄ\x00145±"&\x001b¢ÍÄ\±\x001d¢þß@Lijb0\x0005 Û\x000eòÎª\x0008Ä\x0004£x¤­hFÄ\x000c91´ø­9ìål·P²#JÂô©ä\x000c7¡.­áÜèNjr\x000b±QÈ!¨C\x000e]Äc\x000fV¥\x0002\x001f4\x001bËÛ&b£CP\x001c\x001e\x000c}N%\x0007bîÈ^B\x000eI\x001drh\x0017\x0007©gCïsU%÷ÅùãlE99$uÌ\x0001ZC6\x0013³ðæaX¯;=b\x000eI\x001dsÖ</Ño~/\x0000-\x001a´óÇq`r\x0014rHêÃð8³.ò²§\#/UßãØ\x000e9
9$uÈa\x0004¼è7\x001bE!m~tÄF!¤\x000e9¬BÙ4a\x001c¬ÅvÈ#\x001cr\x0014rHêÃÖg\x0018Æ»¶uù`êH´Fa¤\x000e;@AÒeZÃ÷R¬\x0004õGº_ÊQØ!©Ã\x000e[s(\x0010\x0010\x0015[\x001cZ£ CR\x0007\x001dÖÛ¥/
ZaÃ#ïé\x001el!¦FA¢\x000e:¬AÑ:pa\x00031<`º#-´Ø(èPÔAG0Y<\x0010|X\x0016\x000fÔJÀ¾'$¹Ø(èPÔAG8V\x001aM½ÁD6ØÎÂeOCy\x000b±QÔ¡¨£\x000e¯sí*\x0013c\x0013:ÆRÒ\x001d'R£CQ\x001c Ø\x000eLcúF\x001b]¢úÎÈ&b£CQ\x001cÞâ,3áYf5\ÂDj\x0014n(êpÃû8k5!UâåK¢þHy\x000e5
8\x0014uÀªÉ¹\x001cp!Ùv\x001cÇ¬Fñ"7\x0004ãÐ>Ì|°ô\x001aæ?fZ½­-¼F\x0001"\x000e8Ä ù#K#.ØpSé)\x000bo ¦G\x0001&\x000e8DøJ2ßÀï¥Ëó;Î÷Ò£pC\x0013\x001bi\x001c\x0015 yE\x0015håqâ(=
74q¸!Bð$rC8ìÕ\x0016\x0015¿¸ëÍ\x001aÙBl\x0014nhâpC°Ø \x0017IY¹ùu\x001dy§MÄF\x0011&8\x0004d6ò\x0017 Â+X·Ya\x000b±QÄ¡#\x000eèwuÙ9Â%ö»\x0016\x001f&{s»¶\x0010\x001bE\x001d8ê\x0010éå!Å¬¤´T%ø=NÔ¡GQ&:\x0004cÈ1{¼Ì½9\x0012¯QÔ¡©£\x000e®sSLß`F»¼\x001d+{£GQ¦:¸)\x001b1\3óÙ³\x000c`Çqbf\x0014t\x0018ê #ð%øÅ|¶g%Jìh³nâ5:\x000cuÔ\x0001\x0018%JÇª!\x000bÙã¤¥Ì(ê0ÔQ(³Ò!{\x0018µGÕhntk6£¨ÃPG\x001dbxZ	~\x001aO)ï\x000fÇ	¦Ì(æ0Ô1\x0008Ö"gÛ¸\x001d6"\x0008sÛ\x001b]»Ø(æ0Ô1(óàbEb2\x001dø¹ì\x001eøÌ(à0Ô\x0001°@%±²(¡eX	8ÜÒ\x001cf\x0014p\x0018êCøRÎ!\x0005ö¿\x001as¤8´A\x001fØ(â0Ô\x0011GØ|>\x0017\x0007Xù\x0000STóTÌaF\x0001¡\x000e8)\x0001¢-ÚLáÈº\x0010Ò\x001fç{ÙQÄa©#\x000eásP|-ÄÊU¥×ù¶×(â°Ô\x0011d¥cx5Ìº#ôv\x0014qXêCb\x0007@,+Ê
\x000f\x0003ÖS{ÞDl\x0014qXê#\x0010sÃ,~1>¼ð\x001d)\x001d`G1¥9äP\x0008æý)òRåIöH)m;
9,uÈ!-^ÂbõM6õÜ\x000cÕ7G²\x001d£¨ÃRG\x001dr¸­p5õ&\x0004\x001b%ú=\x000e¯QÐa©\x000eÅqÖ¦ä©©\x0012\x0006\x000bð\x0012û\x001eÕ(â°Ô\x0011G`5$´ñcÉÂÜ\x001eé\x0001ÂB\x000eê\x001e#\x0001ÚÕªDô&\x000fS\x0010öµ½!¹\x001bx¹QÄá¨#\x000eP)ËÙQ\x0010å´¸
ÑÎ#µâ¸QÈá¨C\x000eU\x0014.8Ö8|°\x0012K\x001d©\x001aÑB\x000eG\x001dr¨²®\-Ð÷HæÐ\x0002\x000eG\x001dp(ªKÈòù¬$GùqrRn\x0014o8êxC3\x0014Ö¤oWmd±\x001c ³x\x0014b£ÃQ\x0007\x001cZ\x000eY_\x0005Ê<)éQ~\x001cSïF\x0001£\x000e8´Æª=hÄÁibp÷Â\x0002í#\x0011\x001bE\x001c:âÐî
U\x000f¹ÃÈ(^Ñ\x0014Ó»QÐá¨@¬´Ny\x001c\\x0013\x0004éê,Ý(êpÔQax½Y£É(Y²ÙGJÓûQÌá©c\x000e\x0018ÄKÚ\x0017³Rª¸æ.Ç&b£ÃSW¦Ñä\x0005K)].å\x0012n~\x0014sxêêQx¹ôC0»IM¹\Ê#yg?:<uõ(4lçè×ã\x0013º*þHýõ~\x0014sxêêQÉ±¿\x001ehåC¹ò\x000e&t[ñ£Ã÷È24ôp[ÉE*Ê\x000fãxf?
9<y¬;U9ú5&	 @?iáuÞ\x0002\x000eO]>ªí)Þ-eyåe\x0017\x001e©SÛÂ
OÝ­b4fnÀA\x000eS7âHï`~\x0014nxò~\x0015Y\x0004Gt£re	8øQZI\x0005cMÀ\x0011ÿX ¦´«\x0008]ômµ.m\x0002ü(ñ¡¨\x0015ä\x00121ê\x0003&ØfC\x000fÛØÿ ñÖ|ä¨\x00009×\x0018yý¨,·f-Ê^f~=\x0001\x0002°-/ê,\x0007\x0017\x0018oè(î*ÀJ!3?JÚWîUË¼ci\x0000$r°Ù\x0000w¦\x0008l"¦GÄÈ+9ü)Ë}Sª(ú\x000c/²ì(n\x0002æê´¼ðªg½B¦\x0014Ó£¼¨°£R\x0002\x0006y·Ä¨\x001cÆâs\x000e\x000e£h\x0016ëÌØDÌQ'9ÈzmÑv0Lr\x0014i\x000e~Ë¥1à-1ò$Ãâ6àsªuqbâ(×0\x0001ó\x001d\x001bb:Ï\x0011Â)¡Ê5\x000cSõ¦\x0014
w\x001cïÌGa\x0007§~[±ºlEÇñ¨I»Ó"6\x0010\x001b\x001d:ì°C\x0002Çób<L¹8«ÎlàMÄFq\x0007§;+m+¡6C\x0013>R (Fg^qÏ\x000e\x000c¯,ª\x0014\x0007Ø£H=\x0008&FG\qO2\x0018Íµ<Ë9Uú:óµ7\x0011\x001b\x001d1zÅ=\x000e_	k-5¦¦ÐØ\x001féÑ\x0001#×Ûe6tlB^å\x001d#Õ\x0001±Û\x0016¹Ú\x001eËÓéùxA{¦u7\x0008\x0008qFÄÈ3¼\x0010Ó\x0002ë\x001eÇ\x001b&8ã\x0010\x001b\x0005öGPÛ+u`Ú"/,>\x0017ì(õ\x001cð.0âE.¹gó d\x0019DZÉPCðc°QXO¯¸Ç°\x0019ÔêQ\x0003ë\x001e`$Óqx¢zzÁ=^\x000cb%8Â\x0019~0qî)oZbô{y\x001b:UR¿\x001c;\x0005Äq\x001eÂà¡tÄê\x0008j{

ÃQ?>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?={\x001c\x000b\x0011Ý/[9\x0008:ä9xêÁ/\è"/\x0005X\x0001~æ£¹\x0008\x001fOçà,êÕ»|$;Á×\x0016§Â\x001ah\x000f\V\x001e5¼\x001aBs9r\x0002ÿàcA[ð97?»ë¿yÊ±JU[²7·6W¹Õa\x000bN\x001a5x°ªÁ%ã{ï.Y©Ë</p><p>¸\ã\x0006¸<x\x0007ÑæÇ\x0007µ7gÇ¯^bÃG\x00185¦d¤>HÁ|sÖÖûÃìb\x0005µj­ð&äÐÓËÞÂo!d\x0000ï*ýtAºè²Ë\x000f°Øòõ\x001e6#ï_øè
?ÞÜ|úq\x0011¤Á¶é§\x0013\x0012lm4\x0019Ræ>æi\x0007S-|\x0008v=H<ÒÍÔ¿\x0005)óAZ§rÂ\x0004ë\x0008­\x0008BÇõ ñÙ*ýôAZa0$ù\x0003r\x00102_ÍÖÄ½ÞîgÍ$¶3Ë»ÛÂ\x001dÊe;\x0002þ\x0014ï\x001cgýj¸\x001f¿I?½;Ò»¶.òÑí©0no·xã8ýÛ:Râø7»Á¦óËO¯¸)l\x000bÓÂ¦NÒ\x0018ì?\x0017¥²tPJ.\x0012Õßôp0çüøõÛ¹\x001bìc¤¨\x0019wCN3Q=_­	ùñ\x000fYÉ¡vé\x0001k9ê?®þñ·\x000fý3*ü¿[môû··\x001bøÛ7÷{|//'\x001a\x001fVsHGiÍq'p$õã»_.o±Æ\x0017 \x0017\x0007oÏ\x0000òè¢Áø·pÿ£ý\x0005M7.L9](</p><p>xñ~óa}Ôr\x0014$üsÊfDÛã-=¹	\x0017áÀ4,zh6\x000f.\x001d=\x000cQc¤ ýô \x0002\x0000_ó$|[ìÙ6¹1ô\x000eN¬_¨ïÿñÓÍ¿Rh\x000cN¢>îÀ5ø1K¸7'\x0011®Nùe\x0010þÉ°ß\x0018¤D\x000f\\x0004\x0012\x001f¼{ù\x0002ÅÛ\x001fA|ðñòQD¼ÓYzC«ÉO«p¨\x0011¢OzøË\x0010úxù×_ÿAY=9§RN|usÚ]5g\x0011sd²\x000bæ\x0010Á
ÊÝ\x0012IQk×¬´\x0012_^`RÏÃp÷ò'\x001b6Õu¥¨ôß\x001f|w»ùçÝÝÕ>¶¯ÄèFÚ@\x0006ÛQ\x0017i}ÃdmþïÎþt~þòq¼|méÄ\x000b¹³4âé§e>+Z\x000fS:ùP3Y\x001bâ3\x0014mV¼ð5ù`Ùù^>¥èQ\x0008ølº\x0003&>vvÕf5¾l ;ù¨ö\x001dù<¥\x0008O\x0006\x000fðìZtÙôâ\x0019Aoç\x001aã:fDÛíáW\x0003Ôß¤ê >@Ø\x0014IÌ\x0005\x0001aÈX"lÙ\x001fqµõ+Yõ\x0002ê\x0005W_>*p©¤s%8L.éÝ½Ø.UÊDma\x0010I2 Zmw$ËÑ»}u\x0008Yt\x0001\x0001Sai\x0002ôn}\x0006s~×\x0002¿Iõî_|\x000fÏï{\x0000h!FÀÀûC¯ö1¡{÷¯"8Zé@A\x0012ø\x000f+Ã|rµ\x0003F£yëÝ\x001eFÉb?ÀÁ</p><p>ù\x0000Ä:>\x0002Äç¨µ\x0000áoÒ½[Ä ,PæS¾L .;$'®­Ãèn¾{
ç/owØ?40`\\x000f\x0010vîÝ!(u\x001cr¸AÁj4yh¸u\x0012 </p><p>ä®\x0004¹\x0013¦{`·fúÄBÓÓäa=<Ø\x001d¦{`²iÆÑ¡þPÆ3\x0001åzxÓ\x0007èù\x0015\x000c\x001b³Ñ;²diel°oÆ\x0001ßÿýÞß|¨<ü7×\x000fS\x001e®ö¦\x0014{Lêd/F\x000bþÂ¹}>\x0005Uc¼99zÎùÄé
¬N\Aâãì\x0000¤I7à\x0004\x0019Ùð=\x000em±h|ç1È|\x0019\x0019ÔäÐ\x0018K±C)¶îVÓa\x001dÄXñ\x0000¤ÎÅnèu)>\x0012(.¡\õkç[S/# #l\x001a\x0014Ç(øÞä1fº\x001e$üe®\x001f2h¶}Ø¦\x0019Ùù</p><p>X|¼\x001ec¾Þõ2FY\x0002Õ6àý=ðÞ\x000e¢q\x001f\x0011\x0001HUL\x000cE<0«üµUã\x001cÌ\x0017ÑNH%ø\x0014 ©ðB¦ \á\x0000úËåU\x0008.ÅãðÕOÔ­Þ0bxôëæÓ=A{R¯\x0008XHï@àzg{m¢H²!,ð\x0016þ¦*U \x0008\x001c\x001c½;zý|\x0006¡GBßM(\x000cåUI\x000f·{ÃÃ6\x0017®\x0002 \x0006\x000f×\x0001Ä¼õôÓ	h
¼$</p><p>ÈÈ\x001cÀ6g0µf\x0010\x0003áé§\x0017P¤</\x0004ôS\x001bà.Cu,"õäZ\x0010\x000eøÓIh¨¼\x0013³TDÎ5\x0006BA5\x0005\x0011þ\x001bz%BTÅL?½shÉRËà}!"¡¢ÈuI³c
Bü\x001d1@è)\x0017
ÎðÜÅ*\x0011:C%ìJ_Yá~zwr à\x000c\x0000½\x001dïÏ4Öù\x0008K\½PEu`ñ+ËCOCmøGºµNÃ¤\x0005~:	Cyã	Øú6Ðk\x0019¥·Dì×»\x0012!F</p><p>ÒO'!êA\x0013 §û\x0015\\x0013(Õ\x001d\x0000­[\x0005\x0010Ö6¼ôÛEè±cMvh¥\x000fné</p><p>¨\x0005ðz,¹úæÍæÓÇÉSã\x0000 O½ËÐcOMª]ÒÆ¥öÌ\x0000hT`@¡\x0015\x0000m\x0002´ÝXÄÀ|6:)Î)
óa=Ã³Û«7÷\x001f.û\x0001ö²\x0006Íü[\x0000ã;Ùíþoª\x001cù>\x0000VDRåsT1Ðqí\x0002uõW}Éø\x001c_ËÎö¼zW:QênJ¬³Èe\x0018Y¹ÂF\x0019*|õéy~\x0019ä/Âü\x0018omó`&ÞÃó¿n>]¾Oå¡{ò[°ëhGX
OP~ÏÞEQßÂÕ\x0003ß\x001f½>~¶§à´P:¬\x000fÈ¿}©&;]÷­\x0013%s9°íÍRÊÛ¿\x0019ùÏ))\x0017)ý\x000eä=ìÆ½7\x0002#À×¦Ô×èR÷¯TèLÖ%DÑÀkÊo^·kÆ\x00192½Ä¥>H£²"\\x0006¨(\x0000o5§ç¦¤ÇûíãÇ\x001bWM|ôó}Í\x0012cw9\\x0002\x0006%zá-¿¼.§:ª®TE4úùi+Mw\x000bÅ\x000fSs©Ð5ÌWfªË\x0014{\x0008bÚV¶®Ì]T9Ñ¯c®r\x0018\x0004©ÀdW\x0006æÊÒ\Yí\x001aÑ>*</p><p>qöÌ"*Í©\x000b1pè\x0010Ök#NÓEI\x0006^vP	Î</p><p>ÐøêI¹¯Aò\¥úãÅTÇ5ÊÛ,ð
%³Út\x0017u\x0015tã-¶*-N):&KGºk¥xÒd¹HU\x001bU#fÙ\x000cAe\x0007\x001eÿsE±ê*\x0003càÀCñìåXø¤¹Xà¼
ÎÁÞ¥)z</p><p>\x0015\x0016<>¯|~f\x000e\í á\x000b7\x000eTG)j\x0005uû°Ð¿Ô~>\x0012e¶<´e<DôVÀÂµ¥;Ö/YCp×Ä\x0006*å¥.¦*Õ\x000e\x001dKK*¢rÛ¥EåReWÀRXþ~:\x000eÓ@ç\x0003>°}±\x0011}+©\x000f\x000b«·Dß§Ì\x0002«ì!?\x0007ñ'­Ø{\x001f\x0014¸¥=</p><p> TN§\x0012Ñ«ÀX­t\x001e¬déÓÏL,\x0011³;ãÐ\x0018;£<-«.´\x000f\x0016YtA¡Sú\x000bå¶\x0015\x000b`\x0019i]Á²¢O\x00180o9\x0017Æm¿I?s¿¡àVí¢ÎÚ\x00180_p\x0011!.ÌË\+ WÏÚ\x0012¹bÚym\x0019ærr
.|jI?³\x0017g\x0017\x0010+)Ë|)z\x0006\x000b>¬Âe°Ãt[pÏ
Äel)r´\x0015C*ß^\x0001\x000b§«çÇ i¦ÂZ@C\x00161¡ÒéU°¸hîW\x000c:ÙAä²®<¸J®(Â*ÓIõég.\x0017ê¾\x0010\x0017\x0018Erlâ\x0004Õ"ë\x000fÕÌÀRa³	òÏBc\x0016Á7ù·\®_l~Ù\x0017êQ*×ÔX	ÑR^\x0016)ídGxª\¨_\x001c½y\x0014	wsþ\x0014\x000eI¥\x000b\x001cfÁDT\x0001¦EÊ3YD¤\x0013O¤9uÈhs\x0001Hr\x001a²Ç\x0017!Ùdç#yÛ´#RH\x0012º¨.#r[\x0005DÂ©EH>!ùÙH\x0011zÑ,Á.D1\x0007D²Z\x0012A×¶\x001fÉ~|ÿÓ_nª<²åN6÷{«:`GT[¼¨òKwlåÌ=wrtÑ*Øb}q~\x000bóã\x0002_ësâ5r15á±ËÄ\x001c,©Ò3íáR)±"9î[.§ÙëÓù¢s¸\x001c¾§¹\Xï#½x&°pR&,F\x001e§ØßÁ«ËÛ\x0007¢¨óÐ0\x0008õMúæP5>+X\x0008ï_\x0003h6JªdÞ»5Ðàj6Ï\x0006ç$i¸aúïa~MÂ^`¬¨_5\x000fÞÞÜßÂü8Lf\x0013YÇBó¨M%iÀgN±g@óì2K£]\x0003ÍD2':&-¦J¥ÚØù-X`v-¡¹UÐ|zöðVÎFÃwKÖI©ü\x0006\x001c¨¾sï©H¿²ã{ÂMÂåg7\x0000s\x0000Î*Íõ\x001eÝ®~ÜÜwB]÷Ê£(Ekm'&ûlóó{ü\x000b÷=XÆÂ_Ê9W¥ 6K-¢6ÞæÇÏ\x000f=ù\x001d½zvtñí#t2\x0015ãçß\x000e<\x001füa~¿\x0012à×ç(jpô9\x0015ft¯C\x0017&D83è<ù÷Ö£l*á@¯k.\x001dl÷æörsÿÛ0Ê\x0019\x0007ÓÇñ0É æÙ0YG	ß¬</p><p>ÁE|ö§_®C±ø^GúÙâ]þ|s}}³§\x0016ÒFO/ÑB\x001b\x0003(p´\x0014R·ójóéòÁ{üêôää´U
Éx2ÇÉåä)úq>'aÒrt\x0000Î6Ó!Pù/\x001a\x0002LÕâ\x000fIÿu\x0013\x0006<1óo\x000faT;¡á</p><p>L\x001aVÖ2\x001fhÞ]]ÞÿÆ©\x000b\x00081¯"ÿv\x0011Â)lPph\x001f\x001coÉé³ñ·ôò'loLõ\x0019S¤#÷UÚ\x001b~¬Òq´\x0005Ü\x0000ºwjåS@èýÏ??¸\x001aO\x000eÎNÛ²PR¥D;5Í´{2\x0006\x0012\x0018V\x000e_ßH¶GkJ\x0011©,\x001e!¿Û`ß%!\x0015H¦ß®yô19\x0003Õ#¤\x0001¡HÁ5ÚT~ófs»¹»Û|\x0018ÇS)\x0011BMÓ!fàáv¦<Ep³$ªæ/\x001f\x000f_</p><p>\x000eÐéD×ùy¥áÐ»t\x0012ì°=m,É¼\x00180_\x000f\x0005Éòo\x000fÀ8dN^Ã\x0010 ËtàDTu`kð9´ÝëäÞ\x0008¤Íª¼ð$C\x001f¢Â<Þ\x0015à|Jjò¢séá½'öÁÇM×ÒäÀ9²)óo\x0015¾TZ:ÍÔ±ø¦­á¼É\x000e=~[e9É\x0018s=ÖÀÃüÛ·smný\x0006|.ëÓgáwE|è(¬°óo\x0017^´$Ë	Ó§²¢?\x001e-åþê*x\x0018fÌ¿=xX¬\x000bañlÞPÒ?ÈB¾lçþãóµK}n0* ìÎÆ=¼'B8Ê1ª¼\x000fy-IÍÖb;µoÎ16pðìæöc#£\x000eõnöwG(¬©Y õaUs\x0011"¡>ïe`¥gn¸¡û$[74¬ð#½¿\x000eê·î.SÞ\x0001ã?÷¶IÀÓ$evàÃ¤ð¹\x0018\x000eäáSÞó\x001bêLÝçÀø§v»Bh4>ÕhÑChðìpÙ¨òÅD»\x0015ùÙM*èxûå¸\x0003\x000flªYxJW­­³9KF`sR~}\x0013Ñ¬'=¶pÈ¿\x001d|pOÈ­9§`¢/þ*Æµ×ùÀÒ§<\x0010_%ÌAT>r"@a¨ü¤; ÆÕ\x0008\x001f¸;ÍDz\x0003g5Â?æ'</p><p>±0É.D¼\x0014ïíªL/Í»Íõ\x001d\x001eg{cÍøéJ56ÁFÍõ|¢UaZÎwG'çÇggM5£B(UJ'÷XF	e"ä\ãr*é;Ã½Ù¥§D\x000c¸-á3\x001eÏ\x0019/z§0\x0004Ê¤T\x0001<\x0007\x0012mÏBðrè	\x0016®%ïo\x001e´*s\x0019ÃàVþíüÎáPR\x0017\x001eØ¡ÄöÙ=´;\x001bÑ'\x0017ÂO\YÖ\x001e\x000b\x0011}y%Ò¥Ï®</p><p>éíeïbÄÞ\x001c®(²\x0013àF¯J5lÊõS\x0006,½È¿]FjÊ¡\x0000_!°FÒ\µ)kê¨õSF¤\dì¥Tbü©i£ Æ^Æs5Ñr5J­\x001eÄ7çPb{\x0001K;\x0007%£èiÉå\x0017^®}{{	\x0007äÍ\x0001ÎÙ\x001e£!ù·\x000b\x0011\x001cm`uR~\x0003 Fz0x3¥»Õý¤YÌlÂ|þë/ÿ¼©</p><p>²ÏîÙ}>§\x001d\x000e%ÔJVÃ§¤m¦LÄÿëôvóùæjò6wÁîìóýîì07KëF\x000cdý´Ù*o©ÀÂ3N«\x0015\x0011Sô¡\x001b\x0011î}$\x0006aà²ê¹ª²\x001fà</p><p>\x001ak­Îq*LëC>U£Qn'©\x0003È\x00188Ò¥l¤u\x00101©\x0016ÿÕh
#âs\x0019éã(c\x0019Ñ§\x0014âu\x0010ñ½
ÿÕ¨\x001cõ]Ñ\x0016w\x000e9<RÃ\x0004WBLáûôÓ»\x0018Ez¬HÙ\x0012/Ù&]¯0cåÿõ	§\x0011O\x0007»ýÒUvÖþg\x000b¿sêñY+8¦.t\x000fæy]pÒ«7\x0007'§¯_<·³\x0010çáI®\x0017ÇCóö<÷ÖAaõàò\x0000\x001füMÎwò	êPu^$	 àK;>ßÿîÇÃ´\x001aÐ\x0017°.7_[`ä7x"\x0000.¸°\x001a\x001d\x0006éAª.Ä(£\x0002­=çyîh\x0008~wÓI\x000cé¦.<§Y\x000c'ÀiHer@i«\x0001â;Ô¾T\x0004SR]Ñ0ÑÈµ\x0000Q ,ýt\x0001*Æ¦\x000fL¯P6º²\x0000ÕZ»·\x0012¤è\x0001%ú\x0015°U(\x0001\x0006[?·\x0016`ê~º\x0000áò x¯¯UE\x001e¯+ñ\x0015ç^¾|_Öx¢BD§¸Dr®W\x0002Ä¨Rúé;c\x000c\x001b`ï"1nÇì×úÀI­-ýôÙß5Þ\x0018¶¿?pò\x000fð½¿þÉ½×éFý¥²þî\x000e0 ©&{¼\x0017c(ÃR¡X»õä§R\x0018¹Ãæ\x0003ý3ßùÁóÓ·ÇG\x0017ÿÏct[swà	EÚt</p><p>+ÒÅ¶g|³}s/^\x0012É0¶\x000fÏP±\x0002/#5GÑ(l³ïu7\x001e÷.§0Ý&OQ þ?;³ÚÜ¹$F\x0010ºà¼§gFØñýfN:Æ\x0014vgîN<Å1d\x001f^8¤/\x000b\x001f¤ü°ý_¦\x000b©×ÂJtxê®§"\x0011\x0007À+w7|`<\x001fáýòé/W?½DÓïìI¹ËìÙ\x001aøLk(ÕÝpGøÀU/\x0018ykDÓéVtpzvôöôe[	\x0001+A·>B¢d|\x0015(ÝQé\x0018X %¡ÜO¸#ë#Ü\x0016¦áeÝQXK*ÅÒ¹\x0010wvðlD/YU»@5îRY\x0016\x0018´&®ö12ýô~gÇ\x000f;àD§\x0004ô\x0014ç\ïÌZ³X\x0000w"\x0016X,É÷\x0010y\x0012£{$\x00123\x0010[¥NB)ê\x0012jÒhDí/.¡\x0016k}gÚ.é§\x001fÊ\x0012Q?¦ Z\x0016pj¥IÔ\x0018H?}©Q\x0000}æ ¹6CªÈÑ_ÛÔôxÿÛ_Äg"«hòd\x001dÌ*õ{\x0000uH1iê\x001aG[E</p><p>VâÄýG\x0007oÿtvzqþ8áN,k&¡UÔ\x0014S;l)Kv¹\x0004Ð½GC°?Ú6p'\4PÉô\x0002úÅ\x0015ay\x0011¨Ê\x0005\x0008\x001a\x0008Ý\x0012ÿ*éF&1Ë+é\x0000ë½%)mÈÔ\x0017±Q!4~«s½øqóµÝûòºÙ4|«SÍªÙ\x0001Æ]ã7Q\x0006Ã\x000e\x00046å\x0006HVP»mØ6f5Æ$÷~ú\x0018¥p°\x0014AÇtkN§¼ãµ\x0018Ó¡Ó}êH\x0013\x000e©\x0010ÙÄ­"5#Æ¤j·\x001abªí°ÝÓ¨(Ù\x001a£Iu\x001ei\x001a¹\x001bRLåZ¥-t\x001f£/ý\x000e\x0008ì-</p><p>ÍÊ\x001dÑ®ÉgúécD<ÕÀñ¬Ä\x0001a\x001dÃz\x0018¬V±{5jUâý\x0016FÊ¼Æx¡VK\x0011üû¿ýíîÁGä¹³ÿYQäoÒÞ}\x001c\x0016ØÑQ2</p><p>ÙÛÓV_Ü-U*\x0015¸\x001f%?Ë\x0017_ödË©°\x00069È\x001e*¬ÊB¥ù­½Pù¸J¦\x001eÂ²k²¢dý-¸Êqo&\x00161©ßÎ\x0018ÕutMz«)\x001016¿^ÞÞå°\x0002ü\x001bÔmWMjáé9\x0004W\x0014×sÚÈY(Ê>, þöìèÝñÙy\x000e+À¿yý¼>Q\x0011¦\x0012À~BIÕÍ\x0012Õ6
iæZÎÞÔµg\x0015D.s½Ø± oQð\x000f$)\x0015)¸°¬¯iè_ âóéETÙ\x0017$Þ¬-Õ¡*-Y\x0000[ê°Þ¶0¶\x0016=ÔÁ1\x0012©ÿ\x0016 ¢\x001dWD\x0013\x001dÿÕÈöVâ;b0<T'!ÝÃ*âCtWê$tÜe-O¢"Âüö°¾ô\x0010 Ãjè\x0011@Ë:çºì\x0015©X£ÛZ¹\x001e"Ö ~Ä@FDâK%\x0019ñ\x0012EIsg%D¼/øþÏ/t="Óù3«`Jö`Xm%J,;N?ÚÁ_ZñÁ­l)\x0008´
±ó¹úÏ¿ýýûËß«fM'éî_X,,,*U¤ÿ \x001a×\x0017\x0008dø\x0010¬R 1&\ùt\x0008­ÂÈ§\x0011pæÀ_vtð\x0002Q¾9I/rÿëøäøí7W>Ü|útYþa\x0007¥®GãJÏHH\x0003Ö#\x0015\x0002MDÍ¯D£1ú0ÍÍÇÍÝçÛ/hþq)ïÿr?\x0018f¸ØoRåj\x0013&¢§±HA
Z¼\x001fªh\x001dVß\x0000\x000e}\x001a\x0006>ÑñÙ\x0019Jm7'ql\x0016K3ÈçüI RQäüN ÂúÊL$Í\x001e¢Ö\x0004]Þø;eª	zwùéóe.µ~\x0004>öée\x0012H9ðzI>'\x0019ñ¨Ù¼;~ýö\x0018ª[³rÿ/ùÛæo;\x001féû|Ö\x0010\x0007\x0017O\x001c"cPa)¯\x0017-máðnw½\x001f|©fíïóù§\x001f¯cªÂØ"
gXx¿o>0ìåÒ|\x0008ªÇù\x0010(Õ_Æ\x0019»»'ûbûQø\x001fv10ïýô3\x0003CF:gÀEÁ\x001a</p><p>\x0013Ê±\x0010Ã&ùÊ\x0001\x000cmqæß9Ó\x0011DZ\x0013È¦×äéðpðe ú¦\x0003·\x000b­í\x001f|Ã×¡{ü¿ýéãAîß½ËåÞ'È\x0015r¼<-[¼§Ï\x001d:+®tï¸ÀóúÛÜµ{»p\x0008í½Rzö\x000cþ ¡]ýzùS)¯~¾lolï+$.gTM>TÞ¥\x0000\x000bp¹\x0010§ëøìå»ã·=ùòÕñ\x000eý³ÙüzýÛÕ~âÖæ÷µÁ\x001d\x001cþXNd,ûÍû«ëëËô\x0005ðÙ\x0013
ArqU\x001b*O\x0013óK«s:u÷üÿ¨{·ä:rd]s*@Ñp¿(i¥e\x0014ÉM²®zI[(%3)RIÊËÓF¿öS×8j&=\x0003îX ×\x0000"'Î>¦Ä[û\x000b\x0004àp8Üöêâð(¬­7g«ÜÛü\x000237R\x0017¯¶,¸\x000ejjà×jlª¤\x000b¨Úñ\x0014H\x000b£i¹L¨BAañ\¨Iù¬\x00155ªI¨ðÇ\x00186Ð#H!jTì\x000b5õ kEeÉ\x0001\x0004Ôà£òÊ}º	`gDM
ÔZQ1|</p><p>\x0013 B£\Z\x0018U¥qP5Ü¹ÏDJ]½GU&¯\x000bdã¨2M£:\x0015Õÿq÷\x000b/7T0éVcõðéòf'ç,IF+ÈêKGÑÀçX</p><p>\x0003\x001aílÙ¥<?8<~³·ºxµ:\x001e\x0005û\x0002Á°ÙÄòÀPoqy`©\x0019ç\x0002Áñ[ XêºY	\x0014
\x0001\x000c.ßÕ°\x001fÀ\x0016ÓÁ61ùeX,_gK$câ§wW÷`Ìà·¥ðýqïïèí\x0000x\x000ftwûþòþþ*\x001eñ¶Ãà4ßbªgoáhö~
×Øð</p><p>èìäÅêüüpë¯Ã·±·ËäÛ¬Õ\x0005ñý®ÖúoÝÏé\x001d!¾½ºÿºkêy¸!$YYîÆ\x0003Må)&8~\x0010\x0006/ñÂ)íô\x0008ß\x001e¿Ù>ù</p><p>¸´Ë/\x0014.Í¼Â¥Ý~¡piÇ_(\ÚÃ	GûØè®øø'/Ã\x0005ëwë\x0018Yyýßÿ\ÿ÷?Å°ívS'¥HùÎ\x001e:óÒÆ)4u\x0010êîÑ½8x~p\x001c£+¯WG«o
'wà0@° 8ÿËÃ
ÿ^À\x0007ÀûðìùÝúóíÃýýÎ\x000fj¬4±vL1\x0007-ÀcxÙ*RJ-\x0008µ.Ôó³×'\x0017çç;\\x0012æ\x0013À|Z\x0004\x000b\x0019\x0019\x000e0|!0</p><p>`ÔB`8Ì\x0019þ¿sÎ|c¿]]Ý\x0017vèõúêþöæ~ïøòá[¼	Ø¾Êc\x0003ÿaÕ#ÅPeÌÂ,q^\x001f\x001c\x001cï\x001d¯.Þn½\x0010è0%ó³,¦äÁ,)9.ËbJþÊ²RpbYLé¬³\x0000¦?\x001eìûß¿t\x0010tï´ã@Í}ìâ\x000c\x0007j+SCç°×óÔ5*\x001c¨5H­õÜ¤]wOú'knÌÍÇG7ëW7;Ýà±A'¹ä°)DlÉa3â1É\x001fÃÑ¾¼Ìî±Ü~þü×·\x000fÅÂ{õõõN\x0014.LÌ
,QÝÍ$\x0016')r\x00143O\x001f³üûàh+»5îÏÝÊ«;ø¿»Ó\x001bIlG\x0002ãâYJË\x0001Énlølæ\x0011Ë«3øÛöq)`²ï?</p><p>F°tñ\x0016&¯H0û©b\x0014/
à\x0006·\x0016Fýñ{Ø\x0007»\x0013&êî¹JÛxñ\x0007ßÈ¨TÔ\x0008rá©\x000c*¸úâù\x0012Õ¶@3âj2ýàYOOxøè¡ñfÍ¤º\x0018\x0013\x0016É_,&BBt÷É##Ê\x0012QV#\x0006Ëcd¾ühqÙ\x001bÐ\x001a¨JDU(A\x0012GÑÚTk\x001e\x0010ùÆNê~8¨\x001eQº\x000eÑy\x0013@\x00181¡SPù3\x001c\x00109T7LD4%¢©\x001eEè´»\x0015ûé;KÏ5
â\x000c¶$´õßYÄ</p><p>	 46ÉTÂwNª*\x0001Q÷7Ä\x0006DW"ºjD¹YÐ&</p><p>ÕÃ ÚF\x000cn:¡/	}=!Ù¥@¨QX% \x001aN&G³Éu¬"«fÄV}q\x0014uÌ»\x0001FmtþÐÍ"ïZîjÓ-9;l\x001cGØ\x0002£¤ë{®¦OF.:¢Q¸$±\x0012\x0019\x001aV¼\x00027\x0018}ÿ\x000e¤±³½ðêýEH¿µLÏà\x001dHCKFÎ0\x001f;ûK_y}\x000c£úÌÑ¦</p><p>(`t´fäô
w6\x0018^¹Ã\x0004Fæ÷Uv·Ð\x0010,{\x0012BO6ß¼³Áðê\x001d\x0006Rù¼ËÃ¨¯,°O\x001b\x000c£ÎØÙbxõ\x001e\x0003wãË\x0013#wyÉ>ÑTÆÎ\x001eÃ«7\x0019î£ªDüÔ(\x000c\x0018À¼ÈzºGÆ;\x000c¯Þe¸K
â0º¨e\x000e dÁcÅé4FÑÙeDõ.Ã­¥ãR<¡$Ë\x0013\x000eÕÑL¶¢³Ëê]\x0007×VæaDç\x001b+Aâ(úÉ\x001dû-jíw8\x0014ÈýxÌSÂó¤tg¼d©Çµ±al\x001aEÇ4jÓÈ2öñÇ¥¦¶\x0010/ðxaM^Ó¢cwD­Ýù;QvÌ·¬6ß\x000c²\x0000\x0015\x0017ÒÂà\x0005\x0012g#ý$OýÓº÷±×Õ©jüÚ\x000cR{Ïóu`z¼í\x001dûÃd,
×?\_>Ü]í>
jMÖ\x0011ÓUc}_õ	S¶4\:þp´º8;\x001c&\x0014%¡¨'´F© dâÐÑéï0õ²\x0004õ<\x0016$©Øª+\x0015,ÃÚS\x000cÐ©éc¨JDU\x0008M<ùEÒ	cÈ\x0005í/Q[j"¢.\x0011uý(*Jìú@\x001a?3ev3-û\x001bL=¢)\x0011M=¢ß<oã(J:\x001f¨\x0019\x0016-\x0011mËrF?DöµÂe?ºØ\x0000èJ@·ÈÏìKD¿DDÞµÚ
fûo`ì,h¾¬\x0015\x001d\x001c¥îÞ\x0002ÊÒúæ\x0011áx\x0010:¼\x0007&2í~F9áxß¿ÞÞÔj^`\~\x0010Qj¦D4µ\x0001'</p><p>äÁuÑô¡\x0003!"ºØña"¢+\x0011]5¢QtuÀI\x000cæ"ãt7ÖO¬ªGÜ\x001a\x0001³ê/
ÅéjHú¼GkEYÂ\x0006
²(8\x0019yg½ðú\x0005£4íÒÂ¦Þ</p><p>ÀÈ¬¤+¶éÃ¨;zÃØYÓ¼zQ[\x0010PK^­\x0006C	;\x001aE­¦\x000f£í Úú/mÐÙ'ý4@ä4Q×y"¢ï ú%~iÑ±;¢Þî\x0018\x0013}Y`\x0012ïêµtª½åz2#ï0òE#×eÙqúA·vLAð¸ãÖ)\x0001UBw.*Mõ[ëý(Ù`\x0010Q¢\x0016QB!</p><p>%B°¤8\x0003r\x0015<'Bl¯\x001d(KD¹ÈQT%¢ª\x001fENå<³T\x000f¹-B¡3\x0010êP/r\x0010Mh\x00169\x0015]èª\x0011Ã¶GßYX¼8Æp4¬­ZX\Oëä3.o\x0018y×..Ò0òaäË²Løîþ\x0012~\x0000ûËéõú}Ò\x0016z¹þ<É5£((Ü]ºT¢-^àp`zçÓ£\x0017IQèåÁë\x001d\x0019Nt¢N¥þ\x0001îØSa§ý£x|5,ñd%\x001eJ\x0001OñÔ!3àY\x001c<ÏûõÕtª¤SKû´º¤ÓK£3%Y\x001a-éìbèt/ç\x0013\x0004þ0øzýpw\x0015\x0018O/¿Þ¿ÿy 49øþ\x001a}!òÂuªWÝSå«¯\x000f.Î\x000e\x0003èéêÍy°Ã¢Ä\x0014
%®t\x0018Õ¸óHzë¸¿¨Æ%¦lÁù\x0012FS	Äô2æ\x0013ñ÷jLUbª\x0016L\x00135\x0013q4\x0005Êy)óhÎ@©KJÝ@éX¼ÀÀÁLq@iéÈçô\x0013áãjLSb\x0006Lå¢\x0000>\x000e¦§5N¶tßDiKJÛ2&\x001f¤¼\x0003è\x0004gf?DÛéJL×éó\x0002>\x00021\x001dù\x0011±÷dL_bú\x0005¤é:\x0015j\x000b4®sÏ	Ó©~¢`\x0003f\x0011OÖ"«bTqzM700(\x0014>Ywû(yµ³»	5ìBÁ».7ÎN"\x001b$§f0ï¼cÞy}\x0017ÌÒ\x00108eÚ¼Ì\x0011G7Ã"â\x001dóÎ[ìûßóÙ;\x00067Xx\x0010L%Ó)¨CAs\x001aÎ§tQª9;\x0016·ø¿g<;67\x0018ùp¸¡D\x0014	M\x0008ÐÈÃ5ë;&ï\x0018yÞbåÿñìXyÞ`æýÉôq<\x001d&ö(o4\x0015k\x0005gd:§èy±X3/:f^´y%ö7÷\x000cHiIØÊû~I`\x0013e÷¨ÑrÖø{F³³\x0019Í(\x001c.=rJ­çæFÄÎ`<Eg3\x0012ÝDg3\x0012-vÄ Ã<\x00158>K¯°Giâ-ÍH4lF\x0002\x0014P\x0013¦¶xÜÐ±³uÂí­'cvö"Ñ²\x0017YÄa8=fèjFEáÜ5ÃV$:[XìV$:[hÙ¬ÃÜ\x0010©)¤ahi8çÈ-\x0016Þìhç7
Å_4;\x001f¥··pvã4-¶\x0013*i<5Ö­hó\x0019¶"Ù±I²Å&yµoi8=\x0016Íi¦Tæã);]6,v¸\x0011¥ËùTB\x0007:¤9\x000eí²³dÃ\x001aÌe¥>£±t.üÙ&ñiî\x001c3½X'3=¥ëõÍN	\x0007Èðâû¤\x000e`0ËA\x0019'(Ì©D/TH\x0006\x001f\x001c\x001f\x001c
Ó©N-Îtf1t¦Ô~O?è¨-_\x0006¼¯?_Þ]
\x0008Â2m´É>òÙ<ª'vÅ(\x0004º</p><p>o~\\x001dî\x0010\x0003Í ¢\x0004\x0015- PÓ8­Ý§½;\HñQ)KLÙ	Ú.g\x0005ÑxRMZð60<õªäT\x001dN]bê\x0016ÌpÀr%èyíñFMØÜçÀ´%¦]ìhú\x0012Ó/\x0015³\x0011MbåìÚÎ&ãù·pvÖ:oZì<w(\x0000\x001f\x0018Å©ÏîÐ#õ&ÒÎrçMëýo\x0019ÑÎzçM\x000b\x001eî+Ó£Ã\x000f'ÐGÅM \x0015Ï|À¸\x001f9\x001b»éFR\x0012â`º4Îb\x0012MÉ¥FJT F\x0003\x001cò>\x0015*® U½Úð¾&Õ«õ@Ò/(!\x000e'7è°+·	g\x001d%ç¯\x000ev¦%«~ùù´u|\mâÃ&õÑ\x0005\x0019:Í)\x0004·K§h\x001c ,\x0001e\x0003 ñ1L\x0007>Ó\x0011v\x001fãS%ªäây8\x000b¥ßWØë@9£D;ä#Æ\x0001ê\x0012P×\x0002z	tÕ({ÅÝ}¿K= )\x0001Mõ\x0012)âWjxÇó\x0015Å.Yq®\x0004tu°ÉPT\x000c²¶ÞçÝpò\x001cô% ¯\x0005tTV`\x000eÚto´ËJ¿Côg\x0014`á¤)öHj	CÈ»vºÒPuÂHÕBJN©:Z|Iê:°c©ûúS#\x00085ÊtJiQ_Ei-òÁ»_*T\x000fØ±Ô}ñ©A@P\x000bô)\x0005\x0002n"lôÆTXÞd«\x001f\x0017ËV\x0013vlu_zjÐyÒ\x0004¬VYÌb\x001aÑ8À­îëN
\x000fa\x00187TK\x0012]Ì°-Ô=Êqª&ì\x0018ë¾ìÔð\x0010BØQæuÖZ3ÒäKÝq§\x0011Ú\x000e¡­$TÅþ40£ÜbhîQ(·\x001a°³ô\x0015§\x0006\x0001-dççeÜ\x0012Z¢b¯ß©®\x001e°³ôõ¦GPøp|¥B\x0002¯|\x001eÁ]\x0002?£\x0000Eg;éM
\x0002\x001ao(I¨¼E	öòQ\x0016S5ag;éKM
\x000f!\x000bÎ4r­F]Hé¹Ï9fª×%ºív\x0002Ò\x0006</p><p>§¡ò(ã«à</p><p>1\x0007§NCÑÙOúbXðÃti\x0019\x000eN9ò\x000eH5^g3\x0011µ	(:²Õ2Ûj!i\x0018;Õ§\x0011Ý¤/Õ5HÈ%ÄÌx\x000eWÑ§pÇä}ÇwÈ`#ìì&¢v7Ñ*÷\x0014ÁUi\x000cW|¶ó±è\x0018kQk¬Ã\x000fIeQ2\x0011W\x000c\x0010*G_ÙïRY\x001cE(;ÆPÖ\x001aCeü¾Äyè=\x0018XnÍæý£n{Õ\x001dS#kMÎÈp\x001dVôFæ \x0003úeg-ËÚµ\x001c+\x001bC§âa*kÏ ²w«	;+¥¯\x00177Dh­dÔßV\x0013TJÌ\x0018íáäS²í\x0001;±Ø(°.Ü\x0013äÞç\x001c£
v\x0013O\x001cm\x0010}LQÉÃt  b?]öÝEö$ã ;¡¸DOwW_.ï¾]]\x000e`jÔ\x000b\x0003¦\x000fûµK\x0001k<ô=:QÑ0´Ý]®ÎÞB\x0013ù!VW8;\x0015þÚDkE®\x001dr@*\x000crRÔ#âiÜõÝûË/OD]/\x001ekÜ¦]äýÞéÿs
Qãz6è^TºìPAm7ì£Mû"U³® `¼« 
\x0001E	(ê\x0001Ã\x0005[`p\x0001é\x0010íÊªãÓ%^\x001e-ùìòø|Éç\x0017Ä§e/\x001a\x000baÕN?ÐË¯WÁFþp{óu=x½¢9ÕCKoQËI\x0015ÂúQ°dÓ\x0015tõæ0XË\x001fNß\x001cì¾cIÈeê«Ì©¯
ÌaD\x0015Kf)\x0016\x000fllC¶\x001ddÛ¬\ìæ\x0012ÙÑ1Ì»\x001c»ÕOåñµ1I2'\x001d60\x000bOw2a·g\x000e97\x000cRO%V"sÙ3¦á\x0007`L\x000f?Yßß\x0013õ××±ýËËûûÝ\x000bÏø|Öð\x0010%Gý4±5£¹ïm¦¯O\x000fÎÏ	ýÅ\x0007G±¡}Xç\x0017;Ö!¡«\x0012]MB·*j´DtªâÐZÛïnJt3	=¸Óî­Á5	äè\x0013h-å¬è®DwÓ&Á/pgÂ\x0007ð¨ê\x0018^í)Ó\x0017^öùpñåÿ öÎ:å\x0016ªe9láá\x001e!é¶iÏ²ÓÛ·/»Ùv'	¼³Jù´e</p><p>ý\x0003"¸dÐ½¨iÐõ£Àiã 3Ãû&ï\x001d1Ö{g·ï¾üº»MBlÎôI±^hIÛê÷\x000b)\ö½³ð×7»$¾	U¨rÑ¨ªDU-¨Mþ\x0014µ¤b³©o?\x0008Õ \x0012Õ,zTmj\x0017êJT·hT_¢ú%£i¼#\x0013¶@Öaå¶¬¼c®x½úÛX;ö/Ô`©^Sð\x00033ýóöþòËÏ{¯×_¾º|ØÉéÂ	T`[UM·¨JIû\x0015<ºæ
§¤¯NÜ{}ðæÇÃÕÅ0¤,!åB!U	©j!£ôI¾¬\x0012*vULÊI\x0014°}áë\x0016H]Bê¤)!MõH2Ïðà®¤ÂN¿Êæ¶ìq*`\x0003£+\x0019]=£Í	aôèZÕÒEG\x0014O\x0004q*!Ët6k\x000ej(¹¹ÑáùJ\x0019om\x001eÊ\x0019(»&h¡6¨Lk³)­­Ò\x0001ÄH£R\x000c»ã(CJöTOZÊ\x0011âÕV(`jêþ¨¥B-­\îþø(££²cøBÍ\x0010ï!^mêF\x0014$ò¢9£&4ü©ÌýZHÛ´\x000b\x001dÊµäÕæ\x0012ÒÝrk)hè\x0016\x000f\x0008y!ep¦Sú\x000e¥¯§¢zlÞ$¨1Døö²ä\x001fç(ÔSQ\x0017ÕF\x001dä)V© \x001f\x0008¥Ù4\x0008|êÊ£²cÔÅBºè\x0018uQoÔ\x001dcû8PÒ©Uþà\=%ÐX\x000bÙñ~ÅBÝ_ÑÙyDýÎcí¦¿û<í<Òç¾âQßá\x0006Ê¹\x0014\x000b5us?â2É\x001fµV\x0013ÇÓ{*³WnÓVü©~|Õ;ù¦õ"îåëjÇÈpJ"UÂQq\x0011ó¸ë÷¹oÒ)öÞÜÞÝ&ÅõõÕû\x0001M</p><p>¯rc>ðÝS¸ÛÜ+?Ê¥I×oNÎÎ@âèèðÅ®ó¸í\x0007»-ß¤UTb</p><p>,ÝWX/è(sÝ>Êäkâ%§là\x000c|À\x000e\x0003Z$ÜY²³`ª\x0012S5
§§D\x0006%\QÙ¶t×¿ØkãÔ%§n\x0019Ns¨`8S=æ>;îO·ß¬\x00065%¨i\x0019ÐpÂ\x0010*[P\x0005­aHi½?%BS\x000fjKPÛ2¢EG\x0013G\x0014+o³ùi<]éZ\x000c\x0013Ë\x0019,</p><p></p><p>-P,G»\x000c*g\x0019O_úñ¹½·²îÈ ,?þ¸~¯\x0005w,(o1¡2,tG}b-ö'Ò9Fwl\x0013o1NÉXY\x0013A}V\x001b3,\x000féS²SãI5ë\x0015_\x001ftÒS\x001eöÞ®¯÷>@îäýû»Ë«\x001d¸ÐSÛE\x001f\x0019óàS³	NDnïà·Ý\x001c_ì½=8Ú{¹·:q¶:<\x001eFV%²,ãÅ&V	Qûê\x0017ÏûZEíÄ¦$6µÜ\x0010sB6ó!3\x001dg°*Týµéß!\x001eÝÞ|º\\x001aH³bÒ¬ÑE´\x0016·\x0003ñHª¹sÑqtrüjuðjwZX5¾5ý[Ä°^P¯±Ô¶W9F²y\x0012þ4\x0007­g%­ïß#£å<IÑ!-ª`;ò]$ëNÛ`yÙA\x0000.=u#­ÙçÖr»\x001a
\x001aKµ#\x000b¼¶T\x0017\x000f´¼¦1\x0016e\x0010V$1Ø©&ãj9ÏàÊîàÊÆÁU</p><p>|,\x0014íáÄµ$h&eÿ¾¡\x0011×vl\x0002üµ	7\x001cb\x0014âÊBg>ãÎ5ºNtp]ÿ\x0012|\x001c®`)]\x0011pÃeõ\x001eNØ	×öC½m¸¢Tð\x000fÇCÎ\x001bq\x0005¹
Ö$\x0016q)G4\x001c\x0016g±¹Bv¬\x0018üµ	WHÒ*µÖ`©ò(>o¤ß¦\x0017XK«»´m+M@\x000fV´.Ï\x0005cÈ0ø¾OÖ+»vL6Ú1áR+\x0014H¡~#\x001c\x000fØ¼\x0005J¶g¡í\x000e®l\x001c\É\x0014\x00057\°ºtØÉ[Û:ýUâê.®nÄ\x0015"V*\x0002®´Ôø3ìg\x0006ÃYhmÇ,À_h\x0001\x0011\x0007WI,\x000fÔ\x001cëh!v8\x000f­ëX\x0005øk\x0013mØÑ0à¤@+ÝÌcëº3Á5Î\x0004Í¢o\x001bÇÖíëtøå*\x000f®îW\x000c¶á*Öqsá¯M¸pÉ¶)q£`'¥P(Ý\x0017\x0005o¤U©\x0000m¡ºV6,§rL-\x0018	b*»3\x0011µ\x0002·{ài<ñ(¦cØ+â:*I\x001aZÛWÒjdµÝ¡µCU<\x001c\x0014Á`\x000c,X</p><p>¤uóÎLÙS%|>ÞO]Ô´5¢c\x0013à¯K¦uÝ±uË\x001e[ßqkà¯\x000b¦µÝ`=\x0013¬êÒªÓÚ.í¢ç-¤KZ¿hÚ²\x0016>ÐökáÇÒN*¯Á5]\Óèà~÷Áå}½t.;e@÷Piõå\x0012¨v\x0006/FÐ¸ä~§#¯\x0014,ëômu\x0017Ï¡À</p><p>"û;»Òò¾\x00129e÷úñ î&hêb>Ð0Ê\x0003m=UÚ\x0012Ô6B© 	ÜPY¬\x0012ÎeÅ\x000eµ-PÅéKNßøå¥ß|yM_ÞÏúå@\x0012VñãGÔØ².\x0006:DXPY#o\x0016ÒÎ\x001cå-ÔIJÍnÁ¯ø¦BòmQû*ÒÎ$å-³T]Úh</p><p>ÊùëyÆÔuH]\x000b)¬'joehás£t{J\x0015igAñ\x0015¥Ãy\x001bïñ£æ)²¬J.ú	FM¤¢³¢DËÒRæ\x001eßZf+·\x0019Ó~RL\x001big{\x0012-ûfÞ1\x001cË6ZÐ´\x001cÚ(MÒ4P*¥c"LpP\x0018-Fqnáì,{Ñ²ì!qc[]Ç¢è#zNÛ}¿·{\x001bhgÕU\x001fü¹¨x\x001bGÔ£.ª,Z&¸­.T\x0015igÕU\x000fý­Èæ{à2ø+>Î±ê\x001b\x000epõXË²tK\x0010õ\T\x0016"\x0015Y5ÚÏ²dÇ>É\x0016û\x0004Ý+ñ\x0016j¿Úg\x0013±7\x001d]ç¹Å:IpJÓìã§g$6ÃçYN²ãÈ&ïù;»ùá öSO^Få¤Ò½\x0017wW÷_\x0003ÑzwFIð9ö\x001d:zRà¢7Âjjú­jÇ\x0006ÝºÎ\x000eÏß\x001f\x001eìH%!DY"ÊZD(d \x0019!É\x0017ø:­!ûH»\x001eÑ®\x001açªDOÊPÿ¥²=z*´p\x0013ßYWèàÑ~=\x00146¨ô¡¥\x000f-\x001e¯×0êþ\ÔÅ\<½ºü\x0000¿?¿½ÚµfÂ8:FùMZ²¨*\x0005Z¹í<=\½ß\x001cî\2	Sj±¦Ä4Åt%¦[*f)M¤s½ì\x00029;k/v\x0011ñÎ"â]E¼³øb\x0011ï,#Þ°¤óÔ]CYLü\x00019t\x0012\x0000ÖýôÅ\x0016LÑYF¢a\x0019A÷0Oì'¬§\x0014ÖG©MÝh±«HtVXà*b±ïï¦Æ</p><p>\x000e\x0002ÝóÅË«ë«O7ïwûÃ^Üñ\x0000áE¾¢ß\x0018¤ð_\x001e\x001e\x001d¾Z\x001d¿(\x001dâ>¢,\x0011å"\x0011U¨\x0016hJD³HDW"ºE!2%º0\x0014m¬Ï«»õÍÁ.ÊÁF\x001aMa\x0003m\x000cv¯\x000c£fÞ\?%/\x0010\x0016ó«³ãUoÁ\x0000¤¬\x000cç2Ôs×\ï«\x0018Ûó¹jòé
§</p><p>Rj¡#©KH½PHSBBÚ\x0012Ò.\x0014Ò¾\x001e2X\x001fUVã5 \x0016\x000e³zúÂ)wDVÞYÚPò
â
Fèo¡ì¬o¾Ð\x0005Î;k/mñ\x0008ÖkF\x001b~PTëxÞåíÝ×«]i\x001e	O9JËÔ\x001cÝH¦(Ð¦ê5²y«³7;\x0012<D¿ R¤ÈÅ\x0001Ê\x0012P.\x0010Pj¦\x00044\x000b\x0004t% [\x0010 ¦\x001fé5eÕ«ðÛÛðüúu§\x0017\x001e05£</p><p></p><p>\x0005òð\x0018ÖT4Îì¶N\x0012«ÓÃãðÛÛð|óf÷%éß@Í©Ä\x0005¡\x0000þ®¢m[8E-.ÆoÀU%®jÄ\x0015úbC­n ü½àeÌ«K\ÝËÃèb2\x0016åÂ#ódÐsM\x0006[âÚÅãº\x0012×5â*C7æJQÏSÃÃ\x001c!ð¤ÒI\x0003­/iýr\x0007×öãZV­^_Þ¯o>
^ñº}u5:KhJEò\x001c ¡ÿ4çëÕùÁñ«1²\x0004\x000b\x0004Ô% ^  -\x0001í\x0000\x0019öûØ¤+ü9hds}ûðn¨\x000cÑD\x000c4â\x0011X5isQ¾EÄ\x0008\x001aØ\x001c\<ßÙ[­ßnK\x0016í¶Æ\x0002²\x0012ö®ß(ZEí4\x0004¦\x0002\x0012ÐT\x0003zÚ×\x0005\x0017§£Ho\x0004.¤S\x0001m	hk\x0001ñ¶\x0004è\x00083Ìm[OËª\x0000]	èª\x0001y\x0014 \x0000@æö¥À\x0011T¹%]?)§\x001eÐ¾\x0016P\x000b</p><p>Ur¸%£\x0011D=2\x001d\x0006pê\x001c,ô±õMå\x0010J%â6·vb^Ó7~ÚY«\x0001ä\x001d@^=¹\x0003*7,VçÂ\x0010rE«Dö+õë	EPT\x000f¡Þ·8Z£8N\x0018BCC(¶¨zU\x0010vL5¯¶ÕZ_Ã
uâihi\x000c'ÏBÕ\x0001TÕNdÁ7ÄÄÊ\x0000(°µ_ØUÖª ìl&¼z7Ñ©\x00159\x0010*¿©ºw>ò£&²Õ\x001dcÍ«­µN\x0016\x0010\x0008ÃÖg±ÒsZ(|òvÂ;ÖWë¿á+wÌ5¯¶×ÁÂx	¥#cCO¦2Ô\x0000ÎJ\x0016Õ+9PdÚ\x0019´Ck(ð¢­QSíµè,\x0014Q½P|øÈ	\x0010\x0018qÇËM¿­S¡è¬\x0013Q»N@Ô\x0012\x001bV3øÆ¼[±§-ëWÕ\x0013vf¡¨ß3ÙÏ«Ïú¹w¾¾y¿»¡LØù|¼Ã\x000ebR
\x000bZå¬ýØNñ#àîÃÊ]=e\x0008XÀ}E¥ÑÀÆS2*\x0007I;\=Öå}pWii\x0015¯.yû5ÑK\x001c`S\x0002÷û\x000b-\x0011ØÀýÊè%\x0002»\x0012¸/ó±D`_\x0002÷E_\x0016\x0008\äÚUë«,¸kÿ\x000f0Ä¼c\x001f5x["qGù\x001eg\x0006üd±àLö®¬¡$,Ìoá¿Ú{y\x001b \x001fîöþùp}uy³\x0017	×\x000f\x0004ït¾ô\x0014ñ½áÂÅÞ\x0001æàíê\x0018üÀzq¶÷Ï£ÃÕñ^ü\x000f\x000e.^À\x0017%¾Ï¥PBy\x0000Àç$ÍL?\x00165\x0019_ørêèK5Ð@cãoë[ÃÑbf|Uâ«£\x000f"\x00179\x0004òÐØGÎË|Óï#7\x0019_øzâè3»ÓpGc\x0005Ý\x0002hòôÍ&ã\x0012ßL\x001c}å(ö ­¥¾nÎqÔê\x0017ßøn"¾V$S'ó­ZÀÏ%ÓÂÎ=y|ï§Îý¤ÖE¿¨wì)ÏýqeúTú2¢Ë¢\x00173mòøMý¿ÆÊ0yhîó¹'\x000fïn[\x0013÷-\x001e¦EY\x0000«Qä\x0010ZXæÉ¯ÔÌü}OÝ¸ k()%¦C(§9Çø¹g?ïl\|âÎÅM®áÈlß	º\x0013\x0017}ÕäÉü\x001dÓÏ'Ú~hÍ\x0007á6Æãü»5ÿJÌÌß±ý|ªñ¹_@h-)8Ë«L¿B~2¿íðÛ©ÖÓÝ\x0003Ô]ùlè\x001aÖÏí¸ñÎæÅ§î^R`N°:l:µ¨^t¬¿jýEV¬¬7øDèÇ'ów¬¿jýëÃ\x0015Î~\x001b/\x0002£õ4Äoú÷ù»§©ÖÙÓq\x0014³SÖ|Îfý¢cýÅTë¯tÎQpÅî%rqgÿöu2Çú©Ö_1\x0010¶°è=å+æ?\x001dë)¦ZOèãÖ_çîN:\x001aÉç\x001eÿï,¦:ÏRQÏ\x0005¡M^¿ÒP¯\x001báfæ\x001dû#§Ú\x001fÅÖ\x0005ôÛ¥ñ§éÓop1¾\x001btºz±¿vÌÑ²¨\x000f\x0012èy\x001eý¾XÕdþÎêSW¯PÔ'O@Ç\x000elß"²õafæs»ì¬^9uõ</p><p>ò,\x0010}Cz}}\x0002=Ùsµ+§®]aÈóá$Ó\x001d\x0006_\x001aÚºúµ¦â«ÎÒUS.g¤Äë ¨­Ø$Í¼xï´X¡\x0007øÁ´è\x0003£¬\x000eélÞÀ\\x0016GSýöÏío¡}/ê\x001c<óð\x0011ÞÞ^¥ÄÕXÏ\x0015e¨>Ù½ê©d½jTlc\x0003}b\x0015Õ9ËGmùÞ\x001c¦ôÕXÓ\x0015¨^îÊaEXQÂ&X\x000b\x001a³\x0002a³B¢âb\x0003kç%¬\øÈª\x0012V-\x001cV°zá°¦5m°ÂQ§0\x00136ÉÔV%°Ò\x0015¶ï´ÂÚ\x0012Ö¶Á\x001a\x001ecî\x0000\x001bü)\x000c¿k®,Áö\x001b>´Âº\x0012Ö-|\x001aø\x0012Ö7¬ÈU\x00020²\x001aGVûGw7¥î</p><p>Üõ.NÃ\x000fzª1Ç·^ÞíVé`VÓm\x000eC\x0012PÖQ_\x001d!·ö8<ß;>ù×êl\x0004¢(\x0011Å"\x0011e(\x0017¨JDµHD]"êE"\x0012Ñ,\x0012ÑvQLõ\x0013Ì\x0015&ß>|iÿópùçÝz7¢e9ÁA8A=áµö.GJúõT'\x0017obÚçÿ\¬þuv0LXto</p><p>Ð¼©PÅ¡ÂZNÂZäæhÌ=ªïî\x0013¾_XÇðiB^=`\x000c¡%v\x001d¢äÊ6 \x001d8©ôò~¸©\x001aw\x0011y5b\x0018:lþ¬\</p><p>\x0001"E$
\x0017Ôj\x0011\x00100 Æ$ó*Äà¯Q\x00057b"ç\x001bpnûùÇÕª¨j\x0011!\x0018	\x001d\x000f¦ïÌôÄÏl@\x0010|"\x0004Õ-gÏí1ZÎpaëª\x0016Ëúîýåíßø§uÿ+¯kÇÐQt\x0010d\x00104v¸Û¬GÂ¼\x0006'|Ö>¤ªtz\x000cÇo</p><p>\x001e§Î§Áeì×ÝÔÅÞ÷\x000cãûz³#t4ØÑN(~\x0006Æ\x000f=Æ\x000f\x000bc\x000có¥÷µÃ\x000c¯ýÚÊç,?¸m%Ûèó\x001c2<»!u\x0018Ê.$ü¤~N}:'6\x0015\x000cÅ9IÍ?8cN¾ë}ïwKûÞ¬ÿ½Yý÷ç\x0008i%J¬C+È¼Óô¯G+(­í3­³àáç/ëûûË½óõÕÍ×Ý¾ÿyç¡\x0015ÔmíFÎ¥\x0006\x0005>×ý²ºÃ×§\x0007çç«½óÃã7{g'/~\x001c\x0014%¤X(¤*!ÕB!m	ië!­ØWißÖPE\x0019÷í@N%\x0002ê)'Cú\x0012ÒWCªpV@\x0007M+\x0014ZPÜDVMfäÝu³ÐSäº\x0001¥\&%³¡81á\x0007µ¬S­>\x0008ÉJ\x000e±¬¯`]*tÏ\)ß¯Gyq{óa\x001dþºûÎqCõtÀq¶åÎÎÉ/N_\x001e¿îº©BVY²ö{º.U¬ýzÀ±µ_</p><p>8\x0015ú»àùÇ8<\(\x000bz\x0017[\x0012oZa]	Û¯ª\x001b\x0005ë<R·Æ0²ÂSÙ£¢åFXÞ]]MËËy[7Vï+µµ¤¼\x0003\x0006f\x0016ZÑ¡íz\x001f[¬]`iah%§IëäL°\x001dcÀm</p><p>¹\x000cX,zÖvl\x0017_¶ñ*²\x0001¶_\x0017<rhYnD	C+ÒÐjEÈ­Þ*i;Ö·/ç4B@\x001dKIvá¬iû²\x0015­´¾CÛ¯\x0008^ÖD\x0010\x001d[û¨\x0019õÂ`;¦V´Z¸_å\x0008+UÌ{ûU±I÷ëkÔ´Òvl­X¶­\x0015\x001d[+Úl­5*WÆ=×î'{ MNåãýËVØ©\x0015Ë6µ¢ã'&G±ìM- %eIJ3´ùÖîÄ´\x001dS+ÚL­qº¿</p><p>h¬ý©Mn[(v¶{¯ íZ±lS[4,X_wa¤õ</p><p>°BåTkô\x0014ÌC+ûww­´\x001d[+Ûlíß6\x0011dÇ|É6óõýiE?| úáóË»»Ë½×^ÞíZxÏ\x000cº\x0011V\x001aOJ\x0005|{\x000fø½óÕÙÙjïõê_«³\x0011°ºÕ\x000b
¸\x0017	ÿv¿ÓîåÍå·«1Y\x00106Q¢\x0002Õ$Íå,Ó[P!óju¼z{¸;\x0011÷4ÚT4\x001auØ¼÷\x0018ª\x000cÝÚ~³\x0011U¨ý¶ÀãP¡Â\x0008Eí >39]S ³j­CU%ªjBeòï¸§Øv\x0018SM2¶×ªKÔ~\x000fãq¨8%g\x000cJ\x001fCâþ¶ãL\x001d¦)1û½àÇ`:ïx\x0016'u£¡\x001d<¡òyæ©+QûMÖÇ¡s,VC\x0019À1eäf¹`´f!õ%i¿Éú8ÒMúIÔ\x001dIßpQû!ù6ÔBg\x0001,j¿Íú8V\ÖÈÊ¨>/ì§Td¢ûµ\x0003¬]ëßbþq\x001cWmP\x0005ViKµÀ\x000e\x0012qç`íØÞ²\x0001\x0004VI[v$ú &ÝdÕÔmDíØÞ²\x0001@)	\x000cpÐ\x0019Ç\x001cì*û>¨\x001dkÅÌU8mQÏN(Mó.n³DìÄåû®7es7??ü¹3#\x0000N,ò}¤t¸ó\x001b®$Å0ÂÚêe\x0004 îý\x001f/þµ3\x001fÀ÷½\x0013ßé ³\x00088YÂÉJ8\x001b­C©m#\x001fÿéîn\x0015pªSK\x00199®ú;¤*º¿øyý×@û1ðà\x0018</p><p>ühêQ\x0002\x0017\x0013\x0014GT(H\x001dê<ø÷Îþh)w¹\x0008öC5ÂÆu×¾á¨ñn}ÿõêòfw$x\x001aLm\x00060EI<eF\x0001~ú\x0000®~ÏWÏ\x000fÎß\x001c®aM\x0007Ö4Âb£e«}H­õõ\x0002j9Ã\x0001¶Ð\x0002¶\x0007zU_^\x001bØElRUÁ\x0014WN>¦Wýðð\x0007êVu¾:z»óxÙ¬\x0005D±HDY"ÊE"ª\x0012Q-\x000c±ßZP°2Å\x000cãùúËÕÍP\x0015¤0å*5ÅíTý\=Jì\x0000\x0003y~pzx¼Ã@\x0012¤(!ÅB!M	i\x0016</p><p>éJH·0H&ûUÜÒwÛ]þp·¾ºÛÙÉ/¸ß\gÍ>Ð}\x0011¨¸Q]ëëUnzùýpvpx¶«\x001f!\x0012QT#já¼%gÖû,+¨\x001fåÖ#Ê\x0012QÖbn¸+\x001dõ.	£hI´Tn\x0011r¯AÔ%¢^ä¶%¢­F\x000cçVK\x0002"ÊAEåZêÈÔ.?5¾DôÕÁ%s(²\x0018v\x0019Â\x0000Áã¦dkõtã¸\x001aDÞ]ÑõKZIÊla$\x0011TÇm\x001eÆ§[Ô0v4_ä.[Õø²UÍ\x0018;×¯ê¿ã[\x000e£Yä8v,\x000f¯7=Ç8ò®jL\ÛðZT¾1ä6Ö§D\x0013äÈ«¾"D
ªwýÀ+ç c³w|{µó²\x000cú*JhEgEAìTäA5®N±Èø\x001cköO\x000ew^!¤(!ÅB!e	)\x0017</p><p>©JHµPH]BêB\x0012Ò,\x0014Òv¡®t\x000bô%¤¯d6'ÏsIÑR\x0016lx¾þxº·ê8HÑ7æÂQúëÏ»Óz®-©BÓHS÷rxëµ­úË×;;Ó¾	\x0017®Ñ@\x000bÛ %E³p¸F¹v\x0005W\x001fÝqW¢É\x0012MÖÛCÈxÕÇQË÷öéîr£Ñt¦\x0017fJ4S÷Aõ¾Æ\x0005Ëý>ª\x0010*G\x0017¬O7P\x001d
æJ0· 0_ù%}ÌâÞ\\x001dgÿ÷\x000f\x001aï´Jö½WçO\x001f»ëóc
\x001dÄ\x000c1Å)º»§ôãÇ=Æ±½ãª\x001bÀ~\x001e~rËÖ¿¤»÷*\x00187\x0011ÛPF±Mk\x0018\x001a­Kþ(\x0003âàõé^lW¸kÊp¢\x0013\x000b%\\x0018*áÔ2àÀ´õÜ\x000fæK÷ãÅúÃÃûËÝëÁyo¨±¶Ò\x000c»pÃ¸$ñ\x0012¶Í\x0003yqðòâÅjçeýð4ó¥\x00132\x0006Ðÿ¥}-ò¥r\x0000ôTWüHT´\x001eP²a\x0004\x001d\x0016>CÍ;&[L\x00064\l³wã\x0001U	¨\x001aFP Ê\x0006¤68\x001aAÊ¬\x0015ýµz@]\x0002êj@¹oHlÊSÄÅ8MKD=Ý·\x0006Ð¦\x0016P\x0018L¢2NDËó\x001aÛ\x0012BÆóÙÏVó)j®\Ú}# E×/ÿd`\x0004à»ðr½MÆ|ôç·w\x001f /äìáêþþrý°Û\x0008\x0006\x0017EØ|ÀË\x0011\x0007\x001dcpßí}àç'g/!3äìâðü|up±áësÉK.K\z9\¶ä²Ëáò%_\x000c\x0017ïÎûÿý\x0013?Ì,ðI¸Ù\x001c\x001e4ä\x0017õkÖ\x000fíöLÑ\x0011,\x0005êÒkrL´µý~TR£ï,¶à½ca\x0018»"ßúa/ûPGëÝ ÎÀ\x000e\x001b9áOÒba\x001b3tÍß\x000fÈ\x0013èÅ^ö¥\x000eFÑvn\x0010"qÙß´</p><p>:8{Ø*ÑrF6GZ÷Û5ÕS~¨é\x0014´<ì½¾}¸\x000ez~½¾y¿ÖjC´P)n¥6¹\x0017ë6%½×'\x0017GáOÏ\x000e_\x000c³U´±Â\x0011\x000eç­áy>l\x000eÚmÉÀ¯U%¬Z8¬)aÍBa\x0005ëz\x0013ðòÌrvû~\x001dvugTÕ$¥OåpH9°¦¯ßCîÎÙÉøÃaBQ\x0012zBCa\x0006)\x0005º´é</p><p>«ûuW
ªDTµstj¥Jy!±}nn×ïfÙ\x0000¨K@]\x000fèHAZ\x0005a9Aò,M\x001fCS"jD¡)H.F\Ã|î«ãô£U\x0005¢-\x0011m5b~x<ál ðQü!|¥é®DtÕ7NÙ]\x0002·Ê$YìÉ[*D_"úzDGil_\x0015NÎÔ&"ü«\x00117áàh\x0014Y5£V±h&æXø(`\x0011\x000f§\x0012\x0017x¿Åb\x0005#ëgè²^î¸</p><p>\x0001Á©Ê\x000bÄ¬ÒN0d¸aV>°9¢H@ôæ</p><p>ÖÛ[\x0000"ë_\x00182º0\x000c\x000cñS?¿[¾}¸¿\x001fÈ}õPwj°^RP3b\x001f,O.{¼ªÃ\x001fãç~~v\x0010vëóóÝé¯¬Èè\x0006±ÕS\x0015\x001e¼b©\Q½yÂ7Áª\x0012V-\x001cÖ°f©°±x@WUòÜ\x0018§$ðùÝÀQSKê­À\x001dJò´V,3n·æT½8yý|ç%<Å²çÏä\x0013pÆÄö?Q\x0014c4éÀÆ\x0007ôÕr»\x0018:Qv\x000eHZ\x001e1GÃæfÀ\x0010\x0015Wxv'O\x001dü¸Ý\x001a\x001f»ÇTÛ¤ÛÍ\x000fÅ¿?;½^¿¦ôôöîkØvRJÌÎ	\x0005Ç9S¤Gãû&êôèàE´£§'goÂ´=(Ù¯U{µjG`â¯a\x0018_^Þß?ì^=Æqì(cEjr Iý5\x000cgÏÔ\x0013Lü\x0011\x000cbX@ç\x0017ú=ýaCØM\x0005z\x000e</p><p>e¶¸9\x001a\x000e ù¡#mò=ª\x0008ç±'\x0010¡*Ã\x0006h®Dsuhf±T%¥Ù'\x001fµØ\x0018æâwÍJSÏÃ\x000f¢ÒÔéÝÿ³wº¾»¼ùm÷	ÖæòHÍ\x0018 )F%!ÜÈÞ±æôlµwzp¶:þ­Xð\x0019c`¾Ø\x000bí3ß­Ç~¾¾»¹úïÿ{7t[¤ü~<¹J	17Ê\x0011$&\x000e±ü-ë6\x0018ì³ãÃÕÙ:\x001atñxÑð:àÁ_ÅglÏØñ¹îø¹¥ë[Øø)Ö\x0019?øë²øtO/oÍe÷lu\x0010~\x0000Ç\x001f¯?ïÕd\x001ap·O\x0006,w\x0018\x0017Ôà?ÒOøñèõ^/Ù ÅgNtbit²¤K£S%Z\x0018]NMóÎ-\x000cOt\x0006O,môdgÕÊe,[õÓåï¿Z\x0011?o\x00181øuôÿý¯ÿûàæÃÝíCÔ¸s\x0008¤\x001d­\x0001÷\x000b\x001c>ÿqyó·ëëOë\x000fÿýÏçõ\x001d\x0010j¡=O(wÜ§f2\x001ct&¢Ís<\x0018=päáXñãÁ)\x001c/ÿ±:þÇÛ£W\x0007\x0017/W¯\x000fÎ\x001dí\x001d\x001c¿<;¹8\x000e®ßíçÏ\x0000¿?¢\x0005\x0016~M¡eI¢;\x0001\x0017opeÂµ,êMÂÕ·ú\x0006m6Xêpîx~ûp÷©T+ïbï-îÃæê¶DØVRÖ\x000b§¦Ø\x0017|\x0017èjïùÉÅÙ«aÌ`¯E;&¦ç\x0004NmXà¸qâÔ~h@GsH6sS	èFEN\x0011\x0003§°é®\x001d8ãyn\x0016Î°T;§LÇÎ4\x00169MêÞ</p><p>}ágûìú\x0019\»4bB8Y!¦U¹wÂñ³\x000f-ûÑá\x001f2ÍÅRæÈÉ÷\x0011SZZEé}\x0016ÌàqÛfL© K;.vb
Ú£\x0000¦
3ìànÊä¤Å®d¾lRL\x0007\x00053¼¯oÆ´*¯õ`;¹O«l;ç²I\x0010ë_­«\x0008¯ª\x0003¨Ôû¸ÖuþìÏeÀMàí{³é²5p</p><p>vÍ\x0000í\x0001\x001dt\x0012k~Â\x001bó	»ßÈÉÈÈK¼+t0Ugûðá\x001fâÍ»æ<v%P\x0016|Àã\x0004\x001a[kÎ\x0002J\x001e^\x001b¨0`4ë¾\x000c_[Ñ\x000cMmTgá\x000c¦7ïG\x001aT\x0017#¨ópín\x0008JÙ\x0006P6Ûö\x000e5ø¼yCÒ +¶¤¹\x0018@µ'?¹¹6N(\x001dàÍ[6>¯yfó§÷Î!(ç³­ù0×yó¦¤Ã\x0002RdíÍ¾	Tú\x001cå»\x001buÿ¡ëÏ¿;ã¯U</p><p>âwÆ¤G\x0004×³\x00069YÒæÛÍù\x0002.ß\x000cf¾\x0005T	¾³£µ\x000fg;ä´nØ4åÌ\x001e}\x001b§·Ü\x0001t\x0017\x000fù\x001a7%æÜ°±\x001f\x000b]ú6P\x001eH5\x0016@*Ð2/æ\x001bÒìÕ7r</p><p>\x0007\x0003©\x0014©Sh \x0015\x000e=<ÎÌ°u\x001aKýú&Ò03e:È[¡ð|\x001c,uD:bg\x001aK]û¦uï$\x001c,õ\x0013\x000c\x000bßi\x0002\x0015ó
ivî@¡väXÅ³òpJvþúùþ¼ÉÓ°Ûó¾hùúó»Ûx-[\x0011Ñ	ÿiÊ²ã\x000e:½ÇÄ&îÃP§)\x001bìÖÐøväw\x000f^½à|ß\x0003_x»ßÊ¤"\x000bü%øm8\x0010 ¿\x00182cãùõ/?_ëkÈ-Z|lR\x000b\x0002&$¬ïêærÎ¦á°³¹\x001e=\x0005®|>\x0016\x0006§{`ÞlÒ\x000fÂ\x0001I'\x0007g[ç|¯ßÿuUiÊOpb*Æß@;§dò l¥ a©¿ãF©\x0001CRÿ	äË\x000cCë\x0016É&\x0007[ü	\x0010©[H</p><p>¼6ö\x001cÜöòËÕõ/å§[Jrùí¿ÿi\x0019+dw.Ób\x0014ÖRÐX©±3\x0006ªMVoWÛ¢±\x001bz¸\x001cxÔªÞ\x0004o#JCÄ;u©</p><p>\x0003O\x000e\x00127~È1n\x000f6ìQë§¶¡g)÷<¸áüÁ5
½ ú¡\x001d¾\x001e.>d?éªiè±·\x001eÃ÷2I=ÂbÕÂ÷CÇ¼Ñô÷ïØ'}WÆx:ô§Y,¬\x0006ß¸øÞó|ù Ç\x001a ?E=±!~ð×]¿\x0011W\x001b¿óIÙ>ð3MÇ</p><p>Ç\x001a6pÖªx/°±z\x0005\x000ep¾kè!å\x0007Ro>TZMáDÊNâNBw\x0016\x0013_!¼\x0001~\x0003çÆ[ÍÓ³\x001e}üré,^!,*oæy\x0005ÉT<Á+8\x0013}Kx\x0005ÅÐ\x0000ù\x001dÞÇÀ\x0007ë%TÊ¢\x0004·éto\x0004¾\x000eºÅá;Ìù!>û_ý­8Ã\x0017¯pöpusYGÏ\x0004Ä\x0019ÓBPÁû=~¸±"·á?\x0018»C5çñj\x0004y:,O$ÐG#¹;</p><p>ÊT"\x000c#LÉ±»×hrME\x0017lß"¹Æ\x000b´(è¼*=g%Qè\x0019È\x0015yÈp_\x001a\x0003\x0000\x0001]ICè|¼¿\x0013ýþã\x000fYº;\x0001îåÿóíj]i'}çi´\x0014)BÍgcp}Z©\x0007fxøÿz¹z{x0H</p><p>\x001eüj%
6\\x0002ê!Áb\x0000ÊýÐ©u,¨</p><p>\x0016	~5\x000fij\x0007\x0017]¯thCJ&/8/C\x0011Õ±¤a~\x0006¿ÅrèÛ}úöÜs\x0008	Ì\x0004</p><p>á*=aHe, ¶Âðÿèð2îf!
3TO¥ZG\x0019Äxh\x0008^T:5È\x001fèît7©þËÿòù¾Øâ~¸}¸»MYu¨^Ðæf@îV¥eZO6üÎ\x0006\x0016þ\x000f'\x0017a/\ÆmúM=è?º\x0011õWW·ï.ïn.ÿ¬bõB¸û*Á¹Ô±ÁÌ>\ô&ÃªØpöÑjïÕáÉóÕÙñê_[pûxùñª¼£*[\x0011<`í]Õ1F¤0\x0019$OÇpÉgw9\x0014\x0010.{\x0015\Äê¼Ax¼\x000e\x000eÏcR?ÀsMf\x000c</p><p>\x0008\x0011>&\x001fÏ
\x000fñ6?\x001d^\x0013J»\x0005ç¢Û©\x001dY6a\x00076â\x0006v\x0010Pf\x001ev2!\x001c/ºÝ±ã~`ÿh\x000f\x0013Qº9f¤à2ó.¥Ä)Oq\x0007øÓ<ð_ÿøåç®y¹\x0015Iõ\x0003®R¿\x0001nUØ]dÚ\x0007µ"ÍFäÇz¥1¬tg×Æ</p><p>&%Ô¬2Ò0G2\x0018Y¨!¥[»ÖQ5©/Z²\x001fïH¨ÃI\x001aãYéâ®uTSm\x0015°*¡í0¬y\x0006ðáËåñ¬tu×8®\x001eþo\x000e"¡jL\x001cd~Ð¿¨ ¥«»ÆQå©(\x0019FÕ²Ô"\x0019\x000c\x0019ÞÂd\x001d¼</p><p>\x001fÏJw­¬,	þÃ\x000c0©-J`µ\x00190|)6îï\x001aY\x0005Ïãª³Õ^bl	3#+eè5²BÆ£Î+Ë\x000bºvQ4®Ã·÷£Y7Yzí\x0003ëp\x0012°\x0011PÖ8÷¸¶¢=5¬9S¯aÖ*ÎéH\x0014|\x0007¬nFÖ¬×>®É´²¶8v[\x000c¤P2:\x001bjÎ×kGMq3+ÑÐvÕ\x000e¾k`sÎ^;¬¶\x0008Ëã}O9®f8\x0017n<jNÛkE\x0015Q\.îZ2ï°pnO°Ã	Ú\x0003¬òþã»ß>\x0002+ÈàÁ¯³Û¯$ yÿ~ý¡z§U.ÎU\x0008À[¿ïú~¡\x001bÚ\x0012ÎN.ÞÄæùÃìÂú,>¦Âpf/\x0001\x0010ÉîJëy10\x001bØ!\x000c\x0019\x001fÓÙ-]^\x000e9Ö\x001cp/\x0007Îú
è</p><p>B×ð®<K*¬pïäñêO\x0000ÞÙØ\x0001÷¬\x001e\x001eÅÇäq,ö²W0µM\x000c]À¸\x001b,ò\x0012L±UZO\x001f|X8yÎ0ã­\x000e)`a j.í2\x0013\x0005\x0007\x000eG£é¿°??^ß\x0017ö\x0004\x001f;\x0010³*½Æ\x0007§(5æ\x000b/9zuaèµÈø#§Î^ñß\x000c¾\x0000Lz5Ï\x000bX½\x0016­Í8üaFI<\·Uü </p><p>¿¦òk°\x0002\x0014ðÒ\x001akÒ\x000bèÍü\x0011#gÕ\x000bÀµ\x0005üá\x0005°\x000b=^?%÷5|F/ ùÈ\x0005Pó\x0002ûâ\x0019Þ \x001c½0l\x0007Ê\x001d>Ý·JJgÚ~)Äá\x0006%>fx\x0001Çè\x0006Pç iTÏÄ70C±»¦73T|L\x0003\x001eÎ\x0015xå­FÒ(ç\x000ce\x000e×^\x0000Â+ñ1Ç\x000bPU"\x000cìPX\x0010<ÛÑïñ	 ×J|Ìñ\x0006\x001e£QÁ\x0010	Ü¡Q"­c;p^jyxÝ\x0013\x001f3¼@8ô\x000bÀ¦v\x0017Üh¦,}¡\x001bÐ¦7\x0000ë\x0016\x001f3¼</p><p>.3nfpß\x000cæ¢¡«Ñ¦7Øx|Ìð\x0006ÁéÇb\x0004ÍEJ\x000fo \x000cÙR£¾-\x0015\x001a\x001f3¼\x0001i±ÁfàöeZ\x0006Pf+i¾Ç,\x0002\x0007=>fx\x0003ìÄ\x001asÖs\x0012vÖ\x001c</p><p>+·½\x0001È'X?Ç\x001bxÄX8ÎÐ,ò©fßa\x001dH4ÄÇ\x000co\x0010¯Ú|\x0003tÌ&\x0011JÚïà\x0014Éû-Ù,o\x0010V²¢(ÊÃ\x001bäsAj2û\x000bÀíÅ¥\x0010*gój÷ð	¨é!1¶7I$çDÊb -\x0018Ó|¶ö4dLù÷X\x0006`¡å\x001c³ð\x0006FPJ/dÕá\x000b\x0018Oöú{L"ÂI3Ï*°.cn]ÚMöÔ÷8Å+Êøé\x0005È\x00109L\x0006	/ óf0	Ûö\x0006\x0010^1ól\x0006Þ fI4D\x0002Ó\x001bÁ\x001d¥oð\x001d\</p><p>\x0005GK5ÏùRjtÐÓÙ@%ÇÔZïsb>KÄoÔ\x0015§>\x0002EëìkP5úzy}uyW\x00196\x0012e$2^ù\x0018=àV\x000e\x001e\x000cPPwïàÍêèpu6LîÕ§[</p><p>,B\x0013xÊ°0¨\x001e\x0014ÈÕPl«<Ý]Ï1æl\x001f+ñESÙ\x0015\x0007Zrºmn5y°\x0003c*¢¶¹F\x000ejÑAnT°9Ð%\x0012äI`\x0011È\x0005M\x00171DTOiÔÉ\x0011ÐÃ1Þeá±<_ø¬E§ª«éè.\x000fºÆäu¸ü¦é"ì0üáóï_~\x0015eªbîs\x0017KS/o>\Þ|­­÷Ñ*ÚT\x0015Ãm÷.Ô\x000c/V¦®_®ßl\x000bÿoÞ\x0000\oÅçy\x0003¥)þ/à^7Mz\x000e¢è8þC\x0015{¯\x0000&^Íô\x00118oÃ4OP ùYåW\x0018µlkßËçx0ó9n±LE_\x0001Þ@É\eð]Þ\x0000<L#çy\x0003a©ðG0»Å\x0007r,ÿ.ëêÞfx\x0001î\x001d]ÃÀ'H5W\x001e²\x0019è
Æ\x0019ÿÊWà\x0010È9ÞÁiJü\x000egCZ\x0008ñ\x0006¾Â(O­ö\x001dDt\x001dÄ<ï`y.\x0002e\x000cÃo¼	ó¡wøÀåÛO=ÇíÅuà¹¼^\x0003°©}~wy]ïwJ,ú\x0017²eÃ\x001eMiàz\x0007ôâhõzu\x000cM	ö\x000e^?_\x001d
¿AJïé
R\x0013\x001f,! Ô)Ã
\x0010\x000c.4½BéÈM\x0007hü_A³¨9\x0014óh\x0004}á{É¦w@\x0015ÙyÞ\x0001V\x0003ªGðÔ\7\x001e`²zÄàÑ·å\x0015R\x0010n¶WpU\x0003¬°ª[[%é\x001d"(-¯\x0000¡=5ç+\x0018,X3</p><p>ïöàHC¯`äí­þ\x001dÂôTv¶ÕàcQk|\x0007ZzQ¢S¼1ö{|\x0007Pº×³­èp´Ä,'\x000eÝxÊ±<¿ÃPVoÛ;MS«Ù¾£h</p><p>·\x0004yï0T"Ôö</p><p>áÛêùQ X\x0016irR¥ÍeN8²U¿\x0003¤\x001a1Ûg°1³2¾\x0003OMõbHþ\x000cßc5@¼m\x000egOæ²Ì
s'J_aH¡§é\x0015 \x0015ÆÎæ(AîÂ²ÕTÁ\x0015_ÁäRàïñ\x0006á\x001fµó­\x0005±/È]å©\x000bZ¬Ê%Âæ{8\x0019RèfÛ\x001aLU®IµS°ÑeÙ1ÁÆúw@áyÞA8TâNçO\ÏÐ8Þá{Ø$ÒÍauYjsZ\x000c¹¨Ú¸í\x0015\x0014¤QÎ8èôÆéÎµ3dH[Þ³X3\x0001\x0017\x001exæQU5ÅÞu\x0004|WtF6aåty/Ü§­AÑ\x001b	KV¿BV]ç\x0015T¬3U:\x0015ÄÓ\x001bÄä\x000eZÓ;àj¶\x0015
Íêp9@:\x0005~\x0007C5\x0005Vï°;p8QÅÇl§\x001f\x0014¤\x0013çÚ$Kz\x001dV\x000fi¡V¼ÄgóóÝý¢^µ¸^X}º¾º¯\x0015¤\x0013j#'`b
3À3Eû³\x00183âõÂêÕÑáù¶[×;U.Nå\x0012|ô°Ü</p><p>*:È\x0006ÁZËZì\Q0[ÒçÜRñÊ¯Á"Jl\x0008ÊJ1\x001d\x0018jÃ­H·MY%3ÆE\x001dÇC\x0011v3Ìo\x0001"æYRTéM7ÜÚ\x000ffwTrç*·ÜÁº£\x0000\x0014³T`´h\x0019u°úsßý~õÛ7[¨5Ü÷_þû»u0ìá¨Â(°¨¢û</p><p>¡)®8TXºA??]\x001d\x0004«8Lÿ(¯`</p><p>=VèqÃ7=ª²:Ì Êb\x0003>ÎÂï²ºÉ£o\x0018é\x0013BwÚÙùA0G¸Yø
WùØ\x001e\x000eNc\x0004#Ó>æÐ[\x000fç75\x0017~Nl\x0005ñ.<²\x001b\x0012¸4NÌ?ù²9­øREi8ú6ÝÇ\x001aO£oóO~èY9\x000f¾\x0012tTý×Q\x001dX»\x001cn\x0018o6GóÁÉ³Çm²
\x0004¹\x0007®d,Wó¯]H×÷~¦á'¹¯÷5þæzu´S6ÇÍ<kW)CúÆ6G\x0018\x000c³äÉñÎðÀ\x000b¼ÿíÓ/*6©òQ·qäc\x000bÊõÃçË½ÓË?ïn\x001fj\x001d\x0007\x000eú`©ÐY;ÔctÞQÆ\x001bÔ%ÇWM-\x000f.^¯öNWÿ:;¹ØêAä7\x0001\x0011ßgñ1Ó«\x0004³\x001cïà]ÎïÂI£V»­oz\x0015UÅ6ùU@z:­kÉ<njÎK\x000b\x001b\x000e1ßë]ÀÛÙÞeÓÄ\x0013ãÓð.BåU"ÇÙØúw\x0011u\x001f\x001fs­\x0016ÇóÙÝ	ºmbôY¬\x001bãm\x0015¸ª\x0011FÌ÷*VÅ\x000eµ1\x000caR)Ax\x0013F\x0019fHµýU`ó\x0016v¾\x000f-,\x001dîe8/cÀ3Ï9>&¢Òô.2Ê«±\x0019ß\x0005G%¾£\x000b\x0010¯÷\x001d\x001fs7Þø.P¨Âæ[-\x0010£CaZ\x0011N\x00191ÂiÝûÛ{ËH1³ó½	ôQ$?ËìK|\x0013i)ð(Ç%äµ¼\x000b¬y9ãÂ\x0017Ö¡N¢(E\x0012Ì9«M</p><p>l´¿\x000bèSùöI\x00018Á\x0004V\x0013yAÂîÁ\x001e\x000fI}µ¿</p><p>¤QÇÇL¯\x0002Rï\x0002ô
¢Ü$+´&¼\x000bÔØÙùJÉ\x001c\x0015Ú	Ëò»H³fP\x0004¥õ]\x0014¬\x00145ãr\x0001Í(Ê%ãJz\x0017IÍo¬\x001cRhk\x0015¨\x0003¹^ÅSö2µ6\x000bo¢r7õQW@m¯\x0002m2ãc¦WQ,WÃÉ\x0011sf¤ÙÔó|/R³Åf|\x0015O-Ñx8E</p><p>¯Û+Ii|\x0015PIqTEþh5m-Òdu7²ø¤å]à\x0002Í·µ¨ÍÍ\x000cð\x0018\x001a</p><p>V4À$ÿnï\x00027âñ1Ó»h¸òÂ}\x0012\x000eÉxùËrQú~ï\x0002
9âc®ï",\x0019±àöcÌEfYm;ØI²ýUà\x001e[«ù¶|¥4Õ±Bì\x0017k$\x0014ËúæÃ\x001a7Íï\x0002»V|Ìö.&ÉÅ´dI¹¤*ÇÂÌ÷ó*5ì+zÎÍÅIòö¹öñ¾\x001bÞEç\x001bï¶OBMÃ³øëU¼D-\°¾´\¡\x0004"c¿'fX¼fo£Ô<Ë7p)á\x0014ó6§+,Êly\x0017¸/ñh\x000cb>T\x0010¢<?+o­ôÈ{w\x0001måøë]@Ì^åª</p><p>cÖÒ\x001cScJ\x0012\x001aß\x0005ù|Þ¾f¹÷\x0013\x000c\x000bPË¡ò;¾Woéí=W(HK\x0015</p><p>Á¶QÍúnf\x000c®/\x0019Cûsj»\x000bªd¾\x000b­|ùÝ6JPM}ff\x000cíC\x0006£n2>ÊE_,¡f2í¯\x0002A}3cd_sGI'<xeNA¦¯2·
»ùãöòþÝc-Óÿþçëú®2\x0011A}¶¢^Ô:kJö1iJ;D®Þ\x001cmMÁÛ@Cr¢°S©¥¦VêÊ</p><p>TU0FduÍ±R\x0016c©Áâ)?{ÊëWÁ=ä(\x001eE¢3Ü\x000fòWRC½1©m,e\x0001jP@tH
«øÜÐ6lÊMf.Õ¡¥AÑCOI\x0001Þò©»ù\x0018mÔ ²WPã´ÖÎ\x000f~Tx
uð{g+µB=|§@¶\x0017%2-I%x7Ni`45ØS[ë\x000cqÔV$\x001aR{E²ýFQ¿¿d?ü¥(¥~s·þvywßË»¸}¨\x001có`?\x0014)T\x000bl¬\x0005¢¤Àej©ß\x001d¼]©\x0017'\x0017/AmIæz`»Q\x0016\x001bl\x0008\x001fÞBROÚÁ°_ã[ ,Ñ\oÁÉ\x0003.\x001a½Èò¤C3©í- û\x0001~Íõ\x00166\x000bÝ³LòÃ[xr\x0004ôÐMeã[\x00133ß·9\x0005\x0018ô\x0019±m­f·p3¾Q÷rýëëâ|}uóuïtýP]d£³èV¹²]³\Ý1_àüàðøÍÞéÁÅ6Ûô1Ò\x0017K?x\x000e\x0005\x0012Ø%ëùúþ\x001fGW\x000fÔð«à\x000cpâWp\x001bÒÿ:\x001bê¡l<èòüà|ïèpuñ
\x0007CQK=
,\x0017\x000ewwÉ=\x0013"·0czçE·¬D·l\x001a:Ëw\x000ea</p><p>¥V\x001d\x0006Äó^z£ÉE\L"wÞPÞ;´ZH¢ \x0001=S\x000fåEÕûÎD÷Ófºsù®Z\x000bÔ\x000cw¹··\x001bò0Ç;\x0006D\x001eVRê?{võqïÃC°4_ªL5V£\x000c$\x000f¤d}a³¸D\x001fÒ^<Zí\x001dþ°÷ò"ØÓ!rQiäF£ö¢\x0007ÕNä$ÚiìP¢r\x0015¸,ÁåDpý\ $´¸\x0000&ÑC§ì*rU«iäÚb\x0012f ×IÓ \x001bl|\x0018È\x0007ª×ë\O$×xßçU7\x0002'ö4ÍÕp{É</p><p>rS³ÅÆ\x0013k$gI¢9NóL>\x0014´¬"·%¹8æ\x0012\x0010½Ò©K\x001cs:\x00189¤Ô_EîJr7yÌS®74æV¨pÉÅOìÛ\x001fîËï¥^ä/?_ÝD³wW×Ý.Å"ö\x0019¿^_ýuu
\x0012JabR7\BäK>\x000b^®\x0017xØ°ÒJDÜÖÞ^^Ý\x000cº\x001f\x001d\x001cþûðèÙ\x001fW¯\x000f£ÙÁóÕáÑ¶~Ä%'õ¯æÔ&u~fÎq\x000f¥ïS+ätÏÉ\x0019[ã£\x001aÔÉd¡)ðV\x0004õÌ!¨y{éäo¦¬:*)ßÿ¼¾û°\x0013RKÆc©\x0002H\x000bÕÇ\x00112,+
cé_ÛÂ\x0019&ïÙËAÌM\x001b¡JNí9F8y,Æ\x0014Ó¢k\x00118×Ó9¿9c>ÿ\ÔsgÊ-±O|ufÃ\x001c,\x0007Dtüê\x0010áL_\x001dnÏÞÆË»\x000f7ï{\x0012u@!¶d%iÏ\x0006XJú\x000068\x001c§(·8E4õ\x0019`ÿøvµ¾ý³TR-¿ÿÃ»Ë»O\x0003«)üOL\x000c\x0006ó\x0014|K\x0011'ªOùôÁ8	\x001fWh0½·7Û>ýÅóÕÙ«­KiH*`Õ</p><p>;¸\x0006D\x001eµ-!Nài0­Pz6Fí^70ò¤\x0000 Xé\x0013£Ê\x0003ÉÁ\x0003\x0006ùåóÝÃïOMÌ½\x00177_/oÖÁàí¶JÎà=1Â;ÃUÂ »5\x000bZía}r­_ì½X\x001d¿Y\x001d\x001f\x001c=}ßU\x001a¸ºS
 \x0016.´}\x0002\x0005Ýd>=O*8\x00014\x0016bÌ\x0007JzV
#ê±¸¼\x00138¢\x00169%s@cad|Ôh<Ðp¨Í2*M\x001e\x001aMÏH</p><p>)ñQO\x001aÖxó\x0007R\x0003ÁÁHÊL&e|:©~ÿÕ__UéÅùð~÷¶©¤Ã,\x0005!Xì\x0003á¥\x0012£g¸>\}z\x0008»ÅV?äåÅmë}CHÛu\x0002Ë</p><p>\x0005¤M\x000b©çq LÍGøi\x001f&k>"d´t¨| \x0014ÎÏF¸%ªAòj:ÓdÂÑ\x001fÍ×*\x001dy1<\x0005\x00104Qâ£j\x000cÄ\x0016Y"\x0016äbÆ¯Ì\x0019®\x0015ïø\Q¤(>ª\x0000Çk/¡¥A÷\x0002NúÉ¿´"6?Å|~y×ôsúMD xä;|ÿ\ßÜþ	ï½s³\x0011ÔÝ\x0003®Ói³\x0008O\x001cDÁa³ÍÿÔÓÿ<8>ù×êl=TSÂ!7\x0019p%\x00188íÒ\x001aÜjb s6J\x001f\x0016³gõ\x000e.i9¥\x0005ðÂ¡\x0014Íòu\x0013)¿ýqåî¶~ñ»\x000fW7»5ëYê\x0014ÜsËÑzC«\x0000tÖÂ0Ê=\x0007Ò³ÇÃ \x0010æ\x0014²\x001eÔ¤ÿ\x0004çØ3êÓ\x001b@£®ätÐõíû</p><p>Î\x001e6ø(H_Ç\x0003ÏÐ©SßÐàIDÉm@,¥ìZ\x001dl%ú\x0017ù{ôu<ïlõ7¨\x0016z\x0017[Wj­ÁìbæÅÇ\x000b\x001cT´å§ÞÞýòð!6( 6Ñ\x001bWèt}½HÖN?(ø\x0018é®\x001d¤¥A×2úA:us±?|4¿Ø;=8:h× $*4TB\x001aJ\x0019¡Sò¾N^Ã½6¼32ö­ÒHÆ`RS^n¸ÁÈu ¡ÛTÈ¿üo_®Àtn:Á\x0016óò|ýéf÷¬´\x000czgÀR÷°~DZ?Ð%B*ëÐ\x001b¢ëé9y~ðêxë,\x0018A¾g9Ç0r\x0004\x0002$Óû)D¨Y</p><p>\x0016\x0003£x¥>ü~](èm>upa\x001eö®cÀxçò\x000e§N,}dPÙ%ãòvR¦\x000by«ÿZ</p><p>??ý¹ß\x001d\ì¥\x0010ñ +Iå7Àj¹¬¦\x000ck\êÄÊÑ\x0014	p·æ$Ý¨4 ­2I/@u÷¾ÅaÅ0\x000cÔÍ»Y`ç?ßÅ\x0000\x001c8×ª\x001b[ï½½Z__~ýºû\x000c)½\x0001o\x001dÜN\x0006ñw<[`3 à3)9æl\x0001öÞ\x001e\x001e\x001c­Þ¼ÙvÜÐ>\x0014§u\x0016÷N\x0001Mèé¡\x0015ZQkÆ\x001cÕFÀ~~÷ñãÏ7¥\x0017zøùËú>åðPpjgËúT^\x0008QX\x0006÷1Z(\x0004yNpq´Ý!9|}zp2u /ËËã- \x001f¿²¬tñ</p><p>Ðlôþöz÷ Â\x0015ÊS\x0010\x000c:\x0006¤Aµ\x001cb¡Èn\x001fÕôhoõâdK£ÅTo\x000f¿êI¹ÂÆ\x0012\x0002%Æà9ùÌy7\x0003©»\x000fóè!+Ð°HOÞÿ<8UxëÆcÂkbõ@§\x0010î¶\x0004g: 'aÚn§\x001bTjNÕjtÔV8ý:â¶oÑË7\{1'*%\x0014· *ºå\x00015Ê\x001c'W¡\x0001úYQÃÊ·ª
\x0015²0èÝ>:|Bbà[9'i\x0014&TÒ¸äÁrA\x0018"ÝÁyÜ\x0004xl^=#+5Àjae\x001eýhéÂá\x001eCfªÙ\x0016m\x0002Lãøh\x0002\x0015àæ§Aõ;\x001eÏ\x0013@ÙyYÁþËÇ\x001bÀ8V\x0015±\j \x0014¢åQf*è_¿Þüù\x00053\x001bc>ãó~ïtà¯mð¢5®&i²9\x0015Ì)Ã£y¾wºýh¿\x0001|¼?\x0002TØ>KÈ`Ç¨ \x0000cØ\Í\p·®\x0012Ð(f¹Lî\x0008ØM\x001a¾XU4îóÍõ­s¼&à¥Ñ|\x0008^î·Ë¯»c
\x0002ÜÌ9å¡ê":L\x000e¯]ÂÆ®]öÎÖ\x001f×_\x0004¼\x0008¾òÛÕ-êãíú?:ú¨Ô©úU'¥æ	^PA\x0005\x00039ÚtÑ\x0002\x0012\x0018xPR:åç\x0006'6xs.KºÜúÕÖÔ
\x0019]ª&	ú	,%¹\x0003©p2Y¨`zµ¾»\x000b\x001f¢{ZÃU4\x0018=d \x0019g\x001b\x000bÞ\x0003&ó8ZY¸tcÀ\x0004\\x001eÅÇø\x0011\x0003B<ôúxNC¦(ü&eÊ2¦ÀgÑh ¥v\x000c&¼ÇÓÓN#\x001a%·[\x000e5lÐ=ëY|fR`ú\x001b<Ê¾\x0001\x001bvf\x0008h6y³{/®o¿6c9¸\x001cs5Ó,ú«i\x0001\x0008è_\x0018©¬ £6-ÖïÃíK#VÜÏÒs,\x0017¸÷é¤Â@Õ\x0013nsÂ\x0015¦«À$\x001cçi7\x0008ÉÏ_î÷no>Ý·\x0012zH8KÏñ^ÅâdÈÃ\x0008GXF\x0008]ª¹Â<XN2\x001b¡m\x001e}Å\x000bÇ9rE\x0003aX´&\x00012î)vü\x0019\x0000elèU\x0016\x0001M5@È,]:PÂâ\x0004Â_~ýôû¯QY2 ,øh^ï\ Ü ¢iX âft\x0003\x000bDí^ G°v±îÎ¾ûtÿ5º°E\x0014x\x000f{¯o¿~ýs§KâµO\x0019Åë°´I\x0008n1ªg$T\x0016îÚ¾.ö^¼yó¯!ºxû\x001c\x001f\x0015tBzp\x0010SE¿ØCõHçÛZSG\x0017èâ£.ìü©¹#\x000f\x001e7t¼`RÛyèÀ!1¾rì oXøØ8Ò)!\x0005\x0016Ï@g!\x0011 >jèÂ¼Ãì.)$%\x0003xçÉW¼§®^ëØ7Eu#g°´,Þ\x000bÇüÐE#'ø<\x000et³ÅG
\¾ÄR.6µLXt?$6¹ºàÀÇ\x0000SòºÏº9\x0019Æ¡IJ\x001c:)éúJí©Äu\x001a®Ó³\x0002P£DS\x000c_;º¨\x000cË"­zW"O\x001d¡\x0001o =+	-Æ7i2<ÞÈÙ\x0008á"(=+	1ZÍ¡û¢!BÌîp\íVW\x0012ªH¨j	M:\x0005@\x0007Ji\x0018NÁ!tÏ÷cë²ø¬\x0001Ô\x001a¯y\x00054ù²\x0018ðAmðH¸ã\x001a¥0æÛÇg
¡aØnVòÆØ\x0019ö</p><p>¿I6ß\x0018¸PLåB¤í\x0017\x0008
úU60\x0013á|Ó0\x001a\x001bSkl­Ö8\x000f <VK\x0001\x0015ãÔ|\x001f\x0019Ò!Ò³\x00060lo\x000c\x0001uL,Úa0×\x0019L_ÐÆ¬F[¹Ýié±lZTÁ!\x000c?Æ¤A6§\x0006+ùt,ÒX\x001b\x0014`\x0017"8h\x00104[\x001a«ø\x0004\x0014^>KÏª/Lµ¡B\x0005/Ð¢)tZ\x000b
`ðt¼¾ª§ã\x001en~{_Fl£lÊCª[?äÅo¿=ì\x000c\x001b\x0016F2E^ 3n²ÙN</p><p>\x001cH\x001dNÃÛB\x0017\x00114ÖÎ\x001d\àíâÛÕÿ\l\x0017ØX2	;E?  æD\x0008´A\x001aãö³@Û¿¾ê¿~ù©×\x0018\x000eÿûÿ|
Ð\x0003÷¶\x001cÛ0A3</p><p>pâ<À\x001edÖh³sÃÉ¬o\x0002ë \x001fÝ×\x0000BÉur{ N²³bvc\x0002\x0004¢\x0000aR=*BÅð0\x001a\x001c³¸9FB'\x0005Ò]nY\x001d\x001f\x0005</p><p>§*ù :ÊâÕ¼¦ZðeUvËf\x0003ô)ÚU	\x0018N¤\x001c\x0007ÐÇã_\x0004dtuè8Û;PK\x0008Y¬^Ö\x0012Ê}FC¯á
ãÙ³Õb>B\x0008{]I(ÑJ\x0006À(j\x001a\x0001QG\x0007\x0000ýl1ò#³Þ÷èYHAàiP-M³\x0010ÓÄ Üp¶i(cÄ0÷\x001d½MþÈÁ\x0014züÈgÏVÍ¶¡Á3\x0015	GdgÐç1Ü\x0000]®÷\x0018ÀÛwZ~se}\x001eÊAbÕÀ=¡ÖádÏÐñ62ÿò26;ÊPÖ\x000c\x0002Ûï	\x000b:,\x0010¯ SÎ¢rJ ³¡dP¾\x001cþ0¸DÆó	Ìfp$_X ¸ULNëR½\x001cEHfÀãQ¬Ðî\x001dÅ'Hp,¬¤d\x0003\x0005(þ6\x0013`.$ª\x0001c:´8ª\x0016Ó>/\x000f#ÍlP\x0008\x0010\x001f5ÌäiXÉ¸>´\x0013´\x000cÚ!¾¿þüñ÷\x000f?õ»I\x0007ór{ssùuýn(O}Q0£òáÞP­\x0018¢-ÌÉññêÍÁóíé\x0012vM]O)éX0+òÙ/|Ê\x001c³§pWM©¼Jpq,
\x0005ÂÁOÐXÚ\x0011^M\x0005e©O9Ò9Z4,ØlLÛ5.Cê\x0011[ÊhÈM\x0002J%¥e\x0018·\x0004î$E\x0010l#%ÁÙ¨×5òõ·\x000f_8~²1ø\x0013\x0007>éöe:ðAñ|J^\x000c³µÔÉÝzä\x001bh\x0000^ò¡\x0003\x001d×¸ÒÄ\x0005<Zt¥§±VUC\x0006ÈL Î¤U= ÃF\x0016LY\x00072J\x0011Pq:4K1Û\x0010öDÇ\x0012ZQ'h\x0011Q\x001d'¤`ð³\x0011RP%aXÄÉËaP\x0007êq\x000c\x0019e÷Èùf!¼ª¯akæ\x0006\x0001-ä\x0001 ÷N\x0011 Ù\x001dÏ\x0019O\x0018Õ#\x0006d\x0013ÙæÏqÉ\x0003\x0001QÍ5Á A¾mýg\x000eþÅ(\x0014f°BÓl¬cq©Ú¢þöëo<Ë½\x001fÖwë\x000f;-!ÈÜè|á o*©Eq¯)ÃFÓíücy#¤ûáàìàâå\x0010\x001bWQö@ÕÀYº.\x0015G\x001fÌ3O</p><p>Q6\x0006¢·\x0016Tá	¸ü\x0011û\x0018<¨£H</p><p>V&ÃT{ìÁ<$®ÈÙø +>*øHâ<ð\x0019ÇÏäªcHò\x000b\x000f»«\x001b>¾O\x0002K\x001aÏ(.5ÞÒ\x001e?Û×,&ýTN</p><p>;F2,é</p><p>|\x0018u\x0001zWÑv\x001d\x001f8Áñ1/ø}©LàcTeêc_Ä\x0007â sñ</p><p>¾pFÆÜ=\x001d¶b*J\x001eó~Àº:~ûë/·~xä\x0005Þï½Z?|½\x001a\x000eUùIæÉÿ}ªå\x0014­pLIÉ?_Þ¬¯\x001fÃï½:¸xs¸C8øâ§\x0010\x001b/k$apøPyÎÃ)9ºy!QÊ/\x0016j'ãÿ¹)ä\x001c\x001fuÃ\x00082A:\x0006hq\x0018\x0005f@·óAÆ\x001bëø¨0¦I\x0010K\x0005</p><p>v\x0013$ÈÏÇ\x0008Ñ\x001aÉ«ç#©eI`\x000cÛ£í\x000e\x000bÂ@é_ûêýúõ×R\x0008\x0018¯/cRe*1¸Ý\x0019Ø4\x0010o\x0015xx\x000eO+ò¸¬M·¥±G\x001aþztrü*\x0015\x001blQO/a¡\x001dlÕ<ÃÆ»RLS7¦îR\x0018vVXªv«µ\x0006t^ó)q]Y\x0014÷Òi77,9Å)ü^C+\x0004%0
õ®éÚ4Þ&Z";sÒ</p><p>8I\x000b:N×ÐÊpN\x0017á¿ÒhìÙxð¤%0+-lÂ4Ì\x0004\x0001e\x001f\x0016êßRN\x0007lóTö¡æZb¿º_¯å¯ý-ôaïôöfwÔÉê Ñ\x0002¤ÞâáUr\x001aPÌþkóÓãmÁÑ
\x0016·\x0004«àr\x001c\x0015ª+ÉQr0p¡\x001f§v\x001f\x0008Grå\x001a£q\Áx^ÛÉ\x0017æ¸Öö@4b\x001c\x0016\x0007\x001dø\x0018Í\x0005\x001d"\x0004äÁ0T¯`1K9bSÁraíx0N²\x001aâd\x001cUQÉóYFlq?\x0016\x000b\x0018\x000b#\x0016\x0013\x001e"¥è¡b©(e*X÷À<rÄ\x0014íÌ\x0014GÓoÜ\x001cr#83\x001a,\x000c\x0013Ãb1«¤à\x0014oj(Åf\x0014\x0018>\x001coÄ@Ö*' FÈp9K\x0001.a·W$ÖÛÖ80\x000b\x0006ÿãwt<Ç´æ°¬\x00022½ª1­ÞÆö\x001bÀ%©¾Ý	Eu&a¦M\x0000S¿^?Ü~ob\x001aäÆ¶F¥¾]d6Øc		N=Õ¢³ºséþ\x0006ÿ©Ç\ç«³­Ê\x001b0opçÆ\x0019\x001f<då¸N´ÌjÎX½3¼6\x0012MÀu©¦\x0006-\x001c}ª\sa}¦d-¯\x0004Äd­h1yRÖ}NÅÓ¥!s\x0010\x0002ôø9!Õ\x0016kÖ´\x0019</p><p>\x001d¥sñ~¦âZ\x0010ø\x0011DÇ°üÀ+#²µNÁÞ«¯¡\x0003ùb\x0014¯f\x001e$ÌÓØQ5ëèÀ/Ss6sRB´a¡*Z¨ª\x0011£ªÉ<t±#§ª\x001a;¦Iø;</p><p>\x000f¥\x0013¸*\x0011ípÈj,\x001d\¥«â>}Ä
[§Ü
Î;fI\x001eÚbÏD\x0007Aÿø\x0018Ogl:\x000f@°®Ð½t\x0014"hGë°Ë<ü¹nçÊÄU\x0016Ø`5\x0013HZ\x001aô=\x0002¢o</p><p>ýL£\x0006R£ñ1N	\x0014¸\x000bßÔîã åù\x00067mó°AnÒ3-ªF\x000evRÔÞÒ\x000e¯Ö¼ät5dÌðýÁX:ÂhS±V!C-vìáyè¢4t</p><p>\x0012â¦Î·XUJ«FsñMß\x0008)À¤\x000b5¯
ä\»CÌ2U~TME8·Ïé¶BÞ&®­yà`Y\x0019«*à¬K-#\x001dð{®%©Ïêáû¾tÅ\x001eÂ\x0015[jWºo6\x0007.$ýÃÆÖÃW²\x0010ÕtÂC»×\x0014à¶>ÓMü²¿ýú\x0010ñYÄ»¾Í5øzïÍíÃî\x0006%à {:Ì+õq´Zá,¿ûä\x0010Å\x0006ß\lSCÝÀùõ¦\x0006.^Ðc(\x000b\x0012Á\x000c^Ð[Atz \x00042\x000eúÖ>\x001a<\x0010Äceûiè8)\Ã\x0019uw¸a<\x001dã£Î\x0005WDa"\x0010*\x000fp.iäØ}°\x001fÏ\x0006é5¼Ì±\x0019Ã\x0016ËlòW-v Ô\x0013l¦M»Ûßÿ¼»\x0019}p$Ï9ÎùÈ´ûJj£\x001cÂ%Þzæ$e7ð\x0011÷ßç{oW;$¡3\x001fIÖ\x0000\x001e\x0002\x0002</p><p>Z³\x001eé3¼Y\x0007i·z#\x0001
©C\x0019¤ë¢E&@æ\x0013\x001cÆ\x0003âë\x0000
êÁ¥\x0011Ä\x00019E¸ùøx,²V²\x000e0ø\x0006G\x0010äUqÇµ\x0006s0¬â{ÚxB¸	áFU\x0011\x0006§=Ý¤!ÄU"ê4cPÀ\x0001*>*\x0008cS`üÈÐf¡\x0014Bg\x0005 Ý!ñxp¥,Ê{å1\x0003è5E ,Ë:ßÂÓÁÌÆ\x0004¹¹\x0006\x0010¶6!+\x00070ø+ÌåI)haÐ\x0000Jê Ü4ü§ëõÃõçØó\x0004î¸âãàÛå
\x0010B\x0006ßçww\x000f BÌ?KEÐêìösT}ô*`è%HÏ<ZÆ0\x001d¯\x0016W³T9èÿ\x0008\x0012D\x0007oWÇ\x0000¶·zýüìâiÍá\x000e2\x001dMX \x0011\x0013<eÀr)¢\x0012°Â\x001fSIcð\x0012bÁ{\x001b\x00168+ðhÁÒ\x001a¤¦J§ôG Ò©j>\x000cV\x0014Úm£¢>-T6\x0019dÀr"¶!\x0007,¿a¬åkÃ"\x0013x´`y\x0011Ëu`j1Zrè¡\x0011KÇv®ã±þº¾¾þJÍR#ü9dñ?DòJA\x0007Q\x0008!Jçuz¡aB¤$âc-,È³\x0011\x0003\x000e)ûÃ8Pª]\x0003J4.f\x000c\x0002\x000ea¸­0â§wW÷0>ð[Ý\x0010ñØk&A¹<D:y0D`U[©¾^Þ\x0001\x0015üVGÅb)U¢W¦JÙüá®¢ºÿó·/\x001fØóè:öË½º¹¼[_íÆâ6Ìi\x0013± ø6öçÞgJ¦´NAõ]*µÑ=<^\x001d\x001c ëO«*:\x0019¾@Ç|TÛtér\x0012ðäã	V\x0007qf<\x0016;\x0013F<\x00155{\x0002H\x0011@\x0017ï.¦ÑÀ5Ò\x0019Îp\x0015Îq÷\x0001ºTÞ\x0005xbò·íöå¨\x001c<\x0017}³ÇðÃ&ç6°	í'²ñ(èÚ<v</p><p>mHÜ\x0000dx"e$\x0001{¼X+ñ çOX\x0017,M<h\x000b¥hây\x001a¾§\x000co%_\x00140o\x001d>ò³#_²Æqø\x0004­	0\x000fü2Ùüy}l	|\x0016ûÃø)2{1\x000e4¯ßI²nübÔ<\x001fC	|ÖÉü}§.Ý¨\x0016Ôï§R³<@\x0016øÂ!PÐòp\x001aùjùàpË[
³I,éûJt\x0001ÂøÉ<~§_¿\x0003|ÝðÅ<4|<Öø¤åAæ%\x001aÖi|1\x001d¢ÏúÍçõñ\x000eø§åÁ¦¿~·¾ºÏ«£\x0012KLÑBôéóâ	FZ/§N?Jml\x001c?\x001dÓoãøX&\x0010Ç/åHÀø	3\x000f\x0004bZ·\x000fhthqü¤\x0001làÓ\x0016Ís°ùÀ'mÞ>ìfùj\x0007\x0017&iüèëN6~Z0VÑ\x0019\x0015.k"+¡6£Ç&Ï¾~_Ð:>\x0003·\x000fzÉàèi³\x000fZòMåPRóæ¡SÞU\x001c¿$J\x0005|RÑê5Ó¿/d\5o\x001e8Ã§bR]Ä3ç&ïm @"7\x000f\x0015køãèÉ\x000bx((
£ç&\x001eÞ!6âÉhPâð¥T1à\x0013"\x000fß\x0013§ïJ¾(´ÞÊ'£¨@\x001a?\x001eÍ\x000cð±º\x000cãg'ây#^\x0012ª¦Ùä­Óà±©~=\x0008\x000eËæC(ô\x000ftÜÅ§@ÇQÝ\x0017\x0006\x000fr¢§ñõÚ'Öñ9\x001eÎ#3yq°©Zû4òÉì¸0\x0015ûüE>tKmÔ&íÜÚðXêè\x0017ð x`qø¬¥é§ÔT¿\x0000\x001a\x001aÈæµËRYmä1;\x001cø(ø\x0019øÄT¿\x0019º©Öå¡}j&\x000c|Nmø8ÙÉ§J¸CT­«CS\x001bF\7\x0011\x0002£\x0001Oµ.Ové\x001cÏ\x0007ÝÎ"^p\x0000­D<A«#^'NÃ¶õ­«CC0\x0019g_8ôæá#:6uíÆ¤ØÖµ\x0001sèD¼9\x0006:¥imðÉ>=\x0008Äêæµ\x0011ä&í»à\x0000ÒÖ¡8M¾]</ü\x0003ºyq8¹kC(Ú\x001cñ\x0004~^\x0003µñ\x0013ñP	°\x0011ÏÆs8ð\x0005\x0017ÁÓç%ÓlbI_\x0003ß¯q÷ÇO\x000cbC½\x001fn\x0003Û\x001bØ0ýÀ+õÁ±±Óâ>çacKÃçR¼®Ä\x000b`¯O÷~8	hÛnÊ6h½Óx\x0015\x0005A)(¦\x00006.bVÊ~ì(\x000etõ'±uÏjula}F©¦À\x0006º:¤@iìmÖNÖ=fÔ	\x0016û`\x0000Xzñæseðò\x0000\x001a:	h=/¯\x000eMä\x0007²-Í§\x000f\x001a6Al>hÏÃ«d\x000b\x0004&}PðV¸Ml¨L\x0012ØtÿÆª
\x0004YMó¸ÙhØâ7û\x0012
/
,èL@#ò&4-)Skè\x00143%ß\x0017.Ð\x001cÆOaëzulEg\x0004ØN'ÚÀ¦\x0015Ù\x000fn'±A±he\x000e\x0008¸\x0014\x000cKÚ0T<Û\x000fÎõ\x0014¶®»YÉ*×\x0012z0nÞd67Åº²|\x0013\x001bô¸¤ù¦,.\x0005oÑ³a3ôI»^pí'åÙã"KÓ
FÀ¸IhP\x0006Ój@ òi
®R):IElq3lgëzçÃæS¹0Í¶´ay\x0017©4l]×¼~²qÑ§Ùf­Ù]ÅÖsË+ÙÂì÷d@È9\x0012o[ÿXSÇÂ´Ml\x0010ß\x0004©s`\x000bÞ+ApfpÜvS6¬Þq¡rÜ¼@q)èX\x001a\x0003ãF7°\x0014ø\x00146\x0014þl\x001f·´LêciÜ0ÄiSãv¶î9¦
t?\x0014Z·¤n\x0001lBÐ|ÓfÊ\x0005g\ÝjÞÂ\x0004©»8nP²kÁ§\x0006\x000faÜX?ºYÇZëmlÐq\x000bç)!CÔ_Ñ|ä¼Qã¸\x0006\x0015Æ;ôÇÃ¸a\x001a \x00084»	lÜý´'ÓuãÑÔªX\x0005\x0003SN0ÜëÃv@+Õ)\x001ey {\x0017éÞ5Ò\x0019Ryà\x0004(Óm]ÀÓÙóUj!	xï#ÞûÖÁ³1}":J_:Ñ8z\x001f"ÞV<"Â`cçHçèH#üSj »t­A\x0011\x0016Õ\x0008âaP¡±ã±\x0007\x0016F\x001e&yçÁÂ\x0010¬qaØpL\x0011ÏÄ\x0018\x0010\x0018Q&\x0007F&\x0006m`e\x0004¼¶\x0011ñèlãyÊ®x´SØ)V%Ð½tm\x000b#Ð©tË\x000eëa\x0016} ã´n¥b\x0003Þ×¶0\x0002\x001eÅãÀ­ã\x0008'hâA3Ip\x0011®m]X¦6ç°1È©<vbâÄû\x0018ñ>6â°Ov×\x0011ÎHÃ$ÓØ>E¶O­l"Çp g\x0003.</p><p>Cå\x0008 91
ïç÷sëMÿ\x0011ÏÇ\x0016ñË\x000b\x0005\x0007µIq\x001c°xaCl´x1»\x0019$ácHBçSbì(=\x0005ï]Äk´x{¹\x001a&SæI\x000c4å£ÿ¤U\x001bèÞGºF\x0007-îLl²dðRôiu?í©îC¤k4x©; Å«½Gº¼É~ZLe.N<Ñ<ñl*D\x0004<á(,ì¹¥#\x0013S\x001c÷.âµN<è\x0007m\x0017µ</p><p>N(¢j"SèþÖÞo9#ÇÓ¾\x0015\x001eî\x001e\x000c#ÿ"3£(¶å(
%:¶¿	¢mÍÈ<í9ÚÛØ+î{Ø3ßÉ^É\x0007T\x0002õVV½\x0012+êé_w·ÉÊ\x0004HàN¹ñÚ,Øæá\x001eü<\x000c#ÞPÞÚM\x001bÏ©7^¶sv\x0007/Þ\x0013OÍCQJµ</p><p>Íû¢\x000fª7¡XG²Ñ\x000cÈC\x000eèhøþôSþ©¼þÏIÔ*GW\x001aáôæö§[êZýò«¦\x000bT\x00043Õá§àê\x001f\x000cC\x001dk\x0014ÄàSØ¾jÒè¦oÎ¿=¿zòô33hx0©Ä(ùL®S=ÏÄ"}\x0002)óÝ1¸ö\x0017ý|$Å\x0012´|)\x001eørMz\x0012\x001fg\x0016/l\x000bböðý;®üO?\x001f/Eø¶N\x001eÈÈINÑ±ñäÔ¦J¢4Ç\x0001¶eûÚ?}¶oò×n~\x000bïõ»èöýíÝÝÔËüÕòh<êeFJp	Y/PvÛ;I¢Ýç\x0017\x0017m`^`­\x001aÝvcÑ=±Jâfè j!VÜÖÃö`­ZÈvc¡Ù¨}¯FôL\x0005\x0011ÑÏ/Kf6QSmº³vcQ¡Á\x0014$á-ÂñÎÞG¾\x0016¼~UêãZ·ìå¢©y5	GºL×~âÊr\x001ftÛò\x000e¬M;Ân,RÔ¯X\x0019\x000cW3Ç`åí!À¶íôA®psþGÿw÷×?ýôöîöÝÍ\x0003.\x0017wÃB.Ë\Áù¹Ã\x0004Öi`´\x000fß]}ûíó§\x000fc­:wb\x0019Êê×"¥\x000bWëG>Mma#PU¦\x001bÊzþìê}\x0014ÿ®lxô</p><p>íÚvIî]ªà\x0016íS\x0004\x001b«déqIiÿèãÚ´GîåBcÅupjDsýn.Q&ç8Àµi;ÜË\x0005ëËR*Ü\x0012mÒZ8R¿ÕµéæÛý\x0019-éT®:túsÅ9\x001ciUêàÚ´Éíå²\x0016ªÀ\x0005!ÈEíèR¼­ÇëàÚ´íå2¶º\x001f®Ï¯î§Hê4YOMµmêÚGE1iç¤ÂTÖKË;RüÙÁµi÷ÙËåt3@öâ\x0014sàød+¶\x001d\F\$0R¸XÖ»Iá\x0006¹R\x0002.Ô#Ñé~¬mÅ^,yÏ\x0010iÊL¥r²»´Äw@ñn¨T¬ôrS¢»úÄ\x00081ÏTfdomû)ö.å
bZr\I\x001ay"¬«\x0003º¸Vål\x001dëE3¥Ðy\x001a]5q9Ã\x0011\x001d	mVåb\x001d\6a¼7×çê°)³\x0018·½;\x001d\Òú\$c\x0003µ¡ ÞÊ"Çï8bQÃ¤I¬¡ò¦>>ÑW>¬ÈoOÓ`­\x0011»U¦±rH×uTt@\G\x001f'UâÉF\x0014#ÀÚ!K_¦'ÅrÈsöÅzÕ Uý=\x0015\x0011V4¿Îý÷¢ÝLh7:{Ï¦\x000b&'s/ÅýñH;{\x0017Ø	ì\x0002j\x0013¬ c=	ÄqI#\x001bÍ{úÞk>g»q¦</p><p>É\x001a\x0018¦ù\x000b9Höz"S\x001cL¢S¼hè½#,ê'1\x000eyoOû\x000cÉ4û^Ôk¼CjµUØ\x0001]¹\x00112w¤Á¯ÇWN3j>gJIZ#\x0003Þ¸cõJ>ùl(ºH\x0013YÒ¹Z@\x000e\x0000¸)\x0012ÑøÁ»¾gvZÒì´DBælléA=°/÷b8b\x0019\µ	M±ÕRÈ¢Ñ1Íç0Ã\x0018AÛ\x0014æô%+&G ñ\x0003\x0010f\x0011¯S\x0005']u¥4t\x0008Ìä<5¾Ó[ê	æË\x001b~ÙjmÑÄ:ÉY("³?þþ_¯ï·bXÏÞúðáö_¾ÿôÛ\x0017¡l¤ji¹2\x0015	\x0015n{,ü<1Ç*,{öüêåK\x001a wõâ3L÷ûô©¾\x001fBd\x0013\¿x{ó//Þßýùßï¿Àw!x¾RfôµøÖÐx£ú\x0015£³Gò(/<¦1B.¿ [gÃöÙÌê9Ù#$Ç\x0019.E&³GÎd\x000fØZrm?\x0016ÇìÊ	,rJ\x000cO¤ÙÞv;È¶¹ºÝhSafk
$Iwc´Ç²O=d\x001b±«ýdÆVµ[û\x001a£u\x001c\x0000EkäyzÈ6:H»Él&	\x0010M³ÎK,\x0012\x0016)N\x001bAÛ¾¬íF3àXÿ-O\x0005A\x0015-Ëã\x000c:øuH'ÚF?e?\x001aò°93Ô÷P5\x0004ð\x0012\x0019ÍÆ¡C°ÍùìGóN^K\x000b\x0019-±0N Þ\x0008Ú6ï³\x0017Í\x0016o§N\x001fBó¹</p><p>\x0018\x001b´üNÐâ§\x001e´Me7\x001aÅ´5\x00132x¾\x0008«YÑR\x001e2\x001d«6®\x001e²\x0014%]0Ò\x0010\x0015Ä`9w\x001d0NÛf4:Ð"ÚÚ¨²·6¹<å\x000c\x0010
\x0016%
\x001a¼^Ñ5ôµ]5=`$\x000eÅ\¤ü%Ês|«\x000bdÞÈÚ¾.2­_.(,¯à\x001c§\x000f\x0002~Îm&¨\x0007­m
éA%sDk\x001d\x001eÚÌæthGÐ\x00007\x0019è6Z(åh\x0006\x0008\x001a®+\x000b>\x001eQ¥è!Ã]\x0006º\x0016\x0004ÛÉ{sêª¢\x0002Þyøt\x001eQ\x0000í\x0000KÓ Ý×\x0004\x0011×Äf¥h\x0006÷_7ÚPÈAO\x001aI·f±DÎÒ\x0000\x00141\x001bÎùxÂØªñôsÍñtÜÍh4\x00015
½BÑs\x0004Ê3³Îyr|¨\x001e</p><p>·Ú\x001a"?àùB@:üCÇ.ÒÙëÐrâçUê\x0012{Å{-Ù#ªß=\x0015®\x000f+ôýw\x0016\x001f&eh¿DGWØbØ±®_Ü\x0003øæÞ¿surù}Y$_~|ûóÝíõ§¿\x001fÁÚô'i+#5¥È5³/ÆxZ»÷\x001f|wq~võ¿öPÝ\x0010Õ*D.Åow*=í\x001cxg\x000cÂAÏôÞhB½\x0011#T´u\x0011\x0015\x0017¶e×õ»=T·Du«¡ª½D£ty\x0014ÉPåíÕ®ê'¢úI³«lÍ\x0015ñ~Ëið·u\x0019û\x0003Tÿþ¿\_'*ªYY\x001fßÞÝÜ>4\x0019Àûüt4-¤f¤¬åÈÂX»5ª?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
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

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-MEJs95Z/omxn3TXvSLWyK5wtscM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `8f3c-gfG+P67yFyIFmwt7DJcFE37xcQc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-MEJs95Z/omxn3TXvSLWyK5wtscM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8105-2RoW8oHR+2wMO/pWUtvrTE3i1m8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-bqOfxlX6Z3R5FCK8Jng0x6UaoD0`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-ebdq7wY3Xcn1wH754ARs29ueaEo`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-KtJk4IeM7iemyszqJCGYUuf9nck`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-fp7mACB6YwkvUbxVTPtMSTkYQAI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-RNjp9qhpApQVLInQSFmngEonNM4`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-lSMIckl4Xohky11p57bEWwets/Y`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��y��	��Y����t׽"�Ȯp��\x000c</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{},"isSafariBrowser":false,"__N_SSP":true},"page":"/bas", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `366405469`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1611761132`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `273111588`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1439655420`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1919628686`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `912784966`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1838188997`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `831362559`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1745640841`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>366405469, which evaluates to: 1981-08-11 19:17:49</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

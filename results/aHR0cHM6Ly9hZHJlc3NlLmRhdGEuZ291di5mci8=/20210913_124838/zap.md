
# ZAP Scanning Report

Generated on Mon, 13 Sep 2021 12:41:57


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
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/azay-sur-cher-des-adresses-d%C3%A9taill%C3%A9es-hameau-par-hameau-et-rue-par-rue-6ba16cd18738" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/azay-sur-cher-des-adresses-d%C3%A9taill%C3%A9es-hameau-par-hameau-et-rue-par-rue-6ba16cd18738" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-22.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-22.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=:\x001b6NÔáM\x0006t;Q5VìÈMeTµS?Å6ãH\x001d^eo´)sÛ¦\x0012/¯Ø¦´º¬~À\x001fÞe\x000f¶)kMÐ¿\x001a{#÷¶¨Hìò.ÍÛæð.\x0003:lÖ`ÛèÚÓú]Ë\x0001}}þá«oýÕáYþÇ»7o§\x0012¯ÍMóú(Ñª\x0003Pµnq>\x0005?ªTõé\x000fGÓ\x001cU¶á=ÓfüÈ$«C½Ê´\x0013Õ\x0001ðhàZgó\x0000îjy[¨1\x001e\x0014­\x000eIFC·$cW\x0002¹÷ºÝ¨ÁTîÐÂòÁg=7¥\x0001»ÎYZ=Í×^PÐ\x0017¾0ÉÂ\x000f:@·b|t\x0015]â\x0010óÁm¸ËåÒ+»Öq@·ryTâ\x0017¨9+_\x0000UnUrÑgq}ç\x0001Ýú+ä_¦¢s¦!Q\x0001K¹Üy¢Ã\x0010\x0017ÛG>\x0003y{\x000bÅ0ä³úÐ*\x001fÕZºæUØJ*Låø´\x000e¡\x001fKÿæ¿zýz	\x0015äBº»½~óâ_¯ÞÜ^
~i=½¿~ú¼\x001c\x001aò_|øÇV!\x0017[µ¬¾ZsÎz}þ\x001bJ\øÐåÚ³::×^F%9yOì\x0017òÄc¾C\x0000¿C\x0017s0â¸qr8	"÷8µ·\x001dð\x0000\x000eêðú Â|HXÔ/ç¬¼ï:à\x0001<ÛÊU.<ÓÊY\x001d>Fr
dåã\x0018®n
ô|dsM|±:<K\x0011
øH
ÀAz¾z\x0014ïaÑk\x0016×ZàuåÛ\x001a®¡/ÒóÉ\x0003zf\x0016Óäi°WÁÃ.}\x0004à </!Ã/Zx¨O×\x0018wèçÑÊ¬Ng©+nFîË)ÅÚ6ôà\x0008\x0003:ìÆdC¦séáIò\x0005ý\x0002\x001eweV\x0000·Ý\x0018
Y\x0005=yéK)ç\x0005}PÔ\x001c¼l@í\x0018AÈz\âLdBXO©ß\x000e÷\x0003:ìGåùÃ\x001dÓ¹h¦oÂ\x0002Þw©/\x0003\x000f°\x001d]°ö/ý¦i\x001c1zÚe¾\x0000Ü¶cÇ,²Õiø>E·\qª-o\x0018+÷91\x0005ÐÙ5Ìê±¯è[ú.@/p\x0015ëWôÄF)&Þ0³PyþE­ÚçT\x000f\x0017íýr7¦TØèq#\x0016Ú®¿u¿|¿>óß¯-k·ï^ü\x000e>Ã\x0010*&ó`ð\x000b¹N%áKàÙ)·ÈÐ\x000b¬y¯Í\x001cÌºÏ¦IA±Z;t:
o\x0004\x000f{k
\x0012ÃnT\x0005ÀAH^Y«4\x001eé\x00017.üfñ/v|\x0000\x000e:òµbç¨j>³êmë4Ñ{j»A1\x0000\x0007\x0019ymÉøT
xNw#Ý¿zÙÝÉ*MÎC6­ÒéSÝ\x0013lè8æ\x001aÆ**)XU§&¿'K ¸¥\x0006\x0002t\x0018·ÄTÇ|IC#\x0017~B
Ð0l©)KùZzÉàq±¸ÛöP\x00016ÎZ&è¡\x001a±0O{5O\x0003YY£¸Ýã\x000eè0l\x0019\x001dH\x0011Ên\x001ci\x000bú2±ï&Mäúº\x0003:O[B,¬·\x000eI@vùâ<±_Ã\x0017\x0008Ð\x000bY&Ó'uN$nòIkØuQ\x0001x%ÃrÞ 2XvzHüQÛtLÎÏ¨GzGçH{×ø\x0002p×\x001eú¶
ÐA¡Þ7ê¿nýpøêêi+ùeàPk)Q\x0006B¼p¾\x0018åþá¥Ë­±Ë\x0000:\x001dR \x001dR¾¢eÊµ\x0015nDréà÷\x0000:SqÃ\x0003]\	ÚìµU>JyßC\x0005à\x0011î]\x0007ÜØ^£¶Àß´y^út6\x000fN\x0015 'ZzÇäI_v{%Âyü'ïÐù9µ¼ÁIRÔ@{]iåÌõü\x0002ë\x001a¹Â1-¬\x000e¡[ÝóA5CN	Ðá%Í	gväùaµfãØ\x0007¨uKç
èpL#9ÊAJë1
ï¯î¶)+@Ç´\x0014º\x001ds¥\x0016Sè^ü¹ñ\x001eZË\x000c\x001cô\x0000÷¥Wâ¯Ð'¶º£°ë,\x0003l|îP\x000cZ\x000e)÷ÎècÊMqÎï5â\x0000\x001dvºsÐß2Î\x00113\x00174®]¨°VJ\x000f¼CÎ~\x001dQ\x0003\x0015\x001eùSÊ\í\x0012Î\x000c^ó
\x0003ÄCúòG¸\x0003$\x0012çEqìØ2ór<\x0010\x000f\x0019:\x0010\x000f©\x0013\x000fo®¿} úà£>\x0010\x000f\x0001zíèð\x0012X\x001f
mÊd³OÝó
¼C5y \x001eW\x000céa)\x001d\x000532ù\x0011Ï\x001ex\x0000\x001d>jp }>\x0006àx
UgVøNîâó
¼CUsîÈäZÐ»ã»w6R\x001e\x0018
\x001d\x0018KÏt?Ö¾4¢9\x001e\x001eÐûñß7\x001c½\x0000\x000eÑ±\x0015v\x0004øbÏüÞµÁº|àè\x0005l0KD¡±ðø.ñèT!+ç{½À^×Ø\x001b\x0003Ö8òD¸\x001d\x00177£IrnôÂ{=wÝJ½â\x0017£çcçÏOwßÞÇµyõ=úÿz}{{-1í»OÎ\x000fÛ
ªÜS9µæ\x0003¨=Þµ/!ØÏ9×mv]ÆÔ>3	Tâhº\x0000s4ò\x000b«¸¬a3¥\x0006ØÖ)]#\x000cúµR\x0010Væ^êO\x0003°#¬;ÃÕ\x0014Îæ.\x000b'÷§ºw\x0010\x0000nMØêAÖè/Õ@¹öv\x0002\x0000·	\x0018
î-I1\x0018Hý \x0014:"Õ¼\x001bR\x0003lëÙ¯=XPi\x000cÛ¨÷\x0002v_¦0{Ýuß\x0002¸
ÀkàrØ¸6£S"³q3t[o=\x0000·\x0000¶ièPÉh\x0017«\x0014þ®íT#\x0001ÜÆ_\x001aKJ¹<x¶y!í0í\x000eSj\x001aª5<C3¡dê³ªn[à\x0000ì\x0000fé\x0010ü\x000c\x0015ô°¥\x001dµ©k¥\x0000ô\x0004_4ã¼*fçå²Ísßq\x0003x\x0001£\x0007 -Ô\x001eÖe¬\x0004fVRõ]¤\x000fè°_Ô«\x0007ôE7,t×âlÔÃKs\x001fo¿ùêÀ4?zLïîogcËõý_?ý+#k[2£ìj	E{UNÆñÌÈ\x0007ûièiT~fÓ¡(xj4É©\x001aà\x001c\x001d<P\x0007cÌ½6öæ\x0001ð\x0008\x000b\x0016#9~;¥eáÜ1£­µg\x0006°\x0013,<;!/\x0018g«\x0005;»% s»QhÀÎ­³a@Jì+Íû\x0014WÙ²{f\x0000Ü¤^$`¦IU\x00133¯¼-Ù$·£\x000b\x0001ð
+÷àCY\x00023{-\x000f-qêß\x001fÀMHF'D!Ý3Hy¯´Â1GO;\x0000ï´\x00111S¥Ýilø}/Nlè É¤¤=P9Q:JÖ×ÉÎ³oÝêë\x0004Ð=íE\x0008Æ$¦àò¬g5½¸K¶\x0003:"\x0015¤\x0007ôºÌ\x0014ëVçfú%t8 gÚ\x0011ÐKgÉ\x0014A¯K:\x0015GÏ÷£ýè|Wù\x001d¤²ÆcuS\x0006tØ3®dW)¢À\x0017\x000c·	zÞ²Á\x001bº¥}eÏ4\x0010\x0015ôð7d_2Öâã\x001d^ÉÛ¯ÞüújO?x÷îúöÝß7ñ\x000f¤\x001c;òÈJºÈØ\x000bðnÅ\x0016¾\x0014ÚÝ{ §=\x0007RçH@½µ¶ø¤¹z q	´ÇLÞú@\x0002¶=òü¡Wk ¡\x0007
ÓY£¾÷¼y\x001f\x0001ÛN¶6)gÀÖ;\x0017\x001eyÝ>ìT¡\x0001ÛÞG\x0015©·R±É¢gí\x0017
\x00155Ên\x0008\x0012ÀíÒ³ø¸Ä±nÍ)ZfÌú<\x0002´=Úï\x000f\x0004´#5Jwiëe5ÊN\x0015\x001aÀí:\x0015Xõ£V¸\x0002¯iÌkÜ\x000fëë\x0008Øö:&q<\x0018\ûåè2êTiu÷]\x000c\x0006ØvÑ
þudäegægyè\x0017£¤²Á\x000c\x001d\x001eGûAû¡ÒÇÛ0\x0005Þ*¡mKÜîaíÐåÂ©¼v¿®}¤ä\x000e1\x001e \x0007Ø\x0001\x0007íÛ*ÛîU	?iÝÊ!\x0002º\x001d¢XÍ«©Ý\x000bwÉSÏ2
\x000eA\x001e \x0017°L\x001dúÛèªBÙ2Ýç°È!È\x0003tÛª \x0001ä\x000c
¥ÞÁ =Q>ãö°6\x001fãµ\x0008zeñ¡¬õ/\x0018ìÝwª\x001am\x001fÞÇ¯¿ý^ÂíûxwóËÿr÷îÝÕýëOÿJºÐØóH\eL
`F¼ÜSüßÇRè4Ãø¡Gr\x001a\x001fÉe·en\x001e`¥àÄû>\x0004ð@à
_2§ò(\0¨W\x0012°­­
µ[lµû\x000b9ïÚ\x0001<\x0001xç]\x0016¾hW*§ôëÆÖg\x0012À­-\x001c¶àhç	%·\\x000c°ÅÐ,[/\x000fÀ¶*ª2âÂÅ/!}g§s\x0011ü9wO\x0019`[\x0015%{ÇuºÈ¡\x0005\x0016\x001aPçÝscèÐQur¸<»\x001b\x001bÀí{¦\x0005Ã"_z\x0012¨»µew_\x0003¶<IüÄ1/ßòòF]ä\x0010üæçw?ídçýáþ÷ÿx\x001eÌP1µ,\x001f7¹Ç\x001eL\x001d	³Æ¼ª-áí\x0006öS`\x0007aK¾\x00064ªz7Ä,<\x0012Ã`\x000f§ÔË\x0008ÀÉ9\x000b¸G2gegb2çy\x001eøk\x000c<ÙÊUw\x0010ÀÅ¯.T_ô\x001dùtåÃ9\x0019¸1Eg%´6^á¬ü¬Ì[
ÐÊBíüæ2\x0002lãDÖAr»0ªÁw²ü»Äì|Ýq\x0000¸¨\x0001
®¦´6\x001bJÌÀÌÜ¡íG\x0001\x001ch¨½''7\2\x0003{Í\x0012Ûöª3t»êNN×Ó'sw\x001d\x00018\x0012Q£f´lÅJ6Ý¨Ø¢[qC.ÿõÍíwoVJÓáýÓï¿}suû\x000cs©Y^\x0000ºâ«Oþ¢\x000b¤\x0014 \x001b#Ô_\x0002iq=D¡xÚ}/´ò!ë|S^È{	»ù&\x0000\x0012Ù\x0007\x001eJ®r4\x0004	»JÛEÌ\x0000^
ÜuL­\x0004mo¥¹\\x001a¯¼+i=|\x0000~9|.ÖBu¨\x001cY+21yFý`°Ó°-ìà¦ÐÂKâ°S®\x0015®·úýè\x0014Ã¬À+Ý\x001aY~\x0006/ÛÉ)\x00001¾ÐÈ*J¬¼-eËÙôtt\x000c\x001d\x0006a\x001f	¿\x000bzc6Ce\x0010çµÇ¸Í&\x0003:\x000còyÊéy&ÃT·T¢ãÌâït\x0018Ê\x000bjünQÛ\x0018:[x\x001e«{HouËU;Õs,ÐY\x0001«&Î¹\x0014·á8 Û\x0018Ot\x000eS	Q®5>¥ò\x0014ðWÍ{Ú Cá© Ñ\x001cÔ£zÁl÷uG¼í"\x0006tåÓÔV\x0005ô%
"÷9+ñ¸R¶£Yn;2HJÙ-vo!ñÚë.<¿\x0007Ý\x0003r÷<²Ä\x0007OSv\#·hÊÿ[&e³\x001cÎjJbì	!ô<\x001b\x0014ÏOS²Ó$·üKx	\x001fÆ\x0012\x0001ËJk5~¾ÝÓáFõ\x001fÁó\x0011ô%_=s\x000bU_Gkx:¿ÚS\x0007tV©.\x001c\ÙçÂ.@-ç\x0014=;C\x001div\x0017\x0006\x0011%8¦ÞÊ\x001aÊhö=t?\x0002z0t\x0015q´Û=«V&ô¥'%Ì-Ï·{NNs9òLE&«Õ\x0017\x0002ÏãaÊç;&Îîv\x0000÷yÙ2!\x0004*
	Ô¶s\x0013Ð¡«\x0008»\x0007³gÖÓÍJ0·3ûùÌ°!ÇÆ±\x001cëËÅê¬Ä\x0017¦\x0010S>ßÙöãè\x0004°ôÂ×oK\x0016Z>ÂóK¦xCWýx{:rkË~Ô]Dèãn?ô\x0002¸mGU\x0019\x0004µQ\x000eö\x0004¾¸Iqó\x001b¬DCÏ\x0015J9¹\x0017f(Ìrt;¯|\x0014ÆËù^/	î¬Õ7\x000eùBà5Ñ\x0015#\x001fa\x000cCïÆb»QµVí|Xyç«7Îq¥rþ\fà>`ö¼Æ-RÊ\x001a@w@\x0003½ß_Õî¯Ú\x0013.]i?\x0019<q­H\x000e~Ñznjv)Úï\x000fÕÐSZ\x001c÷¥4õhÎ
SÍ0E¶:\x0010â«øú*/vmg\x0019\x0001óZW\x00007ÉY]AÞn-Tò0nwcñÜÝlw8°¦`\ DØJUJ]»)¯\x001d~V»Ò\x0013ø	ð5ªñàÉóA±ÞÚtØÃ\x0014c?\x000f\x0008\x0012\x001f?\x001d\{òü\x000fä~ù\x0003²õ{Ã\x001b!w&ÆÎÇ¯\x001cÔW7oÏc¾ü¯0ÊcPéÐ[õ9ór]øÚ§Þ¥êo\x0014\x000fC¯äAÍÛ±\x0003"{·ñÅ\x0016í\x001bß}-¡þª|ýâ®ß~suó\x000c\x0003óò\x000cqïFé9Ç¾M­' Ýt#	8E\x001eèÝÆ\zèc+ Ô¦?k
Ê9¹d/ê®\x001eÀ­\x00038hßÚáäð°'§\x0014Ç\x0004^ÛÑí\x0000¸uÑG\x0007êYÑ)×\x0013aË¨¯¥ºË\x0004\x0003¶5\x0017k¸@\x0007q¢:\x001c{N»Ô\x0019Ï­N"[\x0013}TQ\x0000\x001c9õÿD­vmÖ¼Ö×\x0007À­sY\x0019
\s ÜO&ï$\x000bÕ\x0016v\x001c\x0005\x0000n]ô1g¸º¦2Èä\x0012\x0006óÂ»ßQ\x0014\x0000¶5E~yèz)ñ÷läÃÚý¶ÇÂÐ¡Ï]<cè¢\x000f]ñÐ\x000b³o77øD\x000fÉ.@CÔ\x001d~Qï\x0016½¤A\x001fJ(î{,\x0000=ÀFo0.¢ÚàìÆÅ¸Ð·Ù#|Hw\x0001:\x001c#­.î¾÷|\x0001¬\x0019Æé\x001eÒ]n\x0007IÙã\x0000ÝÅÈÏ@Lû°ö2SFç'	\x0004Y¢\x0012Y ôPx¹<sÕ\x001d	»l\x0017\x0017ØìÔ|"Ñ5MVênguÖfgæùv\x0019\x0000õRPKF¾BfÃ$fl×Pa2tP\x0006\x0019¼ªðR=\x000c\x001c\x0001º_D$â\x0014ð:ÿ¨ Ý´hÏ³QÐ}é«pÒ¿oæÎ\x0001Ü¾iÒL1<Hr;È
-¹úá\x001f\x001e&Ï\x0001Ý>êxÂÃá	§÷\x0011\x0008<\x0008ç÷£M{-GzxK\x00137\x0014ÉwXÒhÐ>\x000c\x0003¸íT+Ì\x0011\x000f\x0011/Ú0Þ×Å.ã-=Ì\x00038ìx&òÏÚ®rË½ÿ¾\x0019<7tÒ4¡*Ü9«ØK[DÊ\x0018hç·o\x0004\x001dU7\x001dS27ë­³\x000cqÃ`; È6hÃf\x0007ÕÑ~tyñ\x0018'WA<¿}#ìHtè5,ÏµóDÓ&ÑV\x001c;ç\x0007\x0015\x0005Y
(Å2Ë,`tn¹\x0006æ q<?©\x0011å°¢ñ\x001dêHiâwI\x0019Ê8ËÛ|\x0000\x0007\x0005Zhéò·¸9O'\x0004Ø0#ù\x001aÏ\x000fj\x0004=¬Ö±ÖàµËèu\x0019\x0007\x000cãY:Lü\x0003:\x0008\x0004uJ^l\x000cS*WaüSçG5l\x001dù½A\x0003\x0016!Ku) íÓõ\x0006@ùQ<]xQU\x0017\x0004Ä\x0015æ\x0004¦Ëût= ³:#§ÔË^4\x000e9oìêèç<¤ë\x0001\x001d\x0014\x0014ÅL°ö²\x0014aB[:"W}ÈÖ\x00036\x001c>(ì=&\x0015T/W\x001eé\x0006¨Í\x001f²õnT~%¥,Ò\x0012'÷Z\x0018}\x0016xI\x001dt~-i!oE\x0006E]Õ©#J'q!\x0013\x000f=59\x0012Û¤\x000bzyð\x0007ä[b÷µü?×?àYqK¢1=PíêØà/Wà\x0003×Áùø\x0003â2û´ºÀµg»¿;ïy\x0007ËopÛè\x0017Y\x0010¹\x0010\x0018¿¸c3íÛoÓ7Cÿ}ñç«û·/tåÅ~suûõûëÛ»÷Woþô\[õJé*\x0017\x0015öD\x001d\x0015xHÉ4½ô.\x000eD\x001auî§t¬h¥ÁX~Ã'ë9sX³\x0018r9.ßpù/Ñ½\x0000Ú\x0010°÷öãZâæ@Ù\x0010-ÓæôøAh\x0004àÁgOðÝ\x0011vFÞ	Ý-ãÚª\x0007\x0011À­3Ý°säÑ»Z\x0003ú\x0000\x0002\x0007µo=¨\x0000|¥6T\x001a<í\x0013Ë`\x00086¢ø	¿>Ô\x0000_Èð\x0005,³2{Ö\x001a©#oÊ'ÖN\x0007·?<½eÞî\x0003}½v\x0001ýRj%&#\x0016í¡$´t­Ô i\x0004Iõr0tSéh£P\x000c½U¾\x0012kI8óuB÷x§øë\x001f}\x000bÛþ°;9"7Ï [ fÁ©,¡_xlÍ/ÜáÂ$fúì9Ð\,âr Ó\x0003-*èh\x001d\*þÇôü¥PMXgUýn\x0019À³Ç
9PÙ\x0014YJ&Ñh\x0001q×\x001e\x0006àÕÀ	6ªg-{\x0001§=æ4Ý³i\x000f\x0003ðnàr\x0011eX¹Ê9D\x0002/WÒ6«eèÕ*ãÂnd\x0017"Ýß..=o¥z\x0001Ý¬®³ÒÞ\x001bºÜÀ\x001d6üe²ò.3\x0004àÅÀÕ+Î\x0000\x001e(XNEkz·JÞ\x000c=%H\x0016ÍÏy2»XÍÞ¦¯vþQmf·¨¹ºô):vûèäÈ¢8À\Ð\x0008²È~È§Ä-ÂòQû\x0008\x0012Ðíj\x0015ØÀ¢e,^ºG\x001f\\x0007S&óÞA:ÈÀ£·
sr\x0015F \x0004·"ñïêÇ^î\x0016Ð/x©ÎAÿCQé Gk_ÑµÇ¸Ë\x0001z\x0006t,94e\x0010Üó}î¶Rºm½æ
QþÀ&¹\x0012H]ÑGâÔ\x0002tÛìõ¡Cñ\x0011]3\x0004ÙæefÎ·å2!áÊ%ªZVÞÏYCæ\x0006Ðm¿(SÍ;
\x0000©BL¥+F¸´Ë­\x0000º}ÑÁÁ\x000b»±:Ê\x000b¥ÂÓbÞcÞ¥\x0010\x0000Ý.\x0001-ÎÂfTm%ºz5
à\x000fª+ ßÀ\x0013\x0018Fû8/àÙ-4¶ÅS¨¦CXwïüÁ³8¼(I u\x0015\x0017«»^xéyô\x0011\x001dâp@7»t\x001aÚ.êôG:¥.\x0017ºabÝ¸l¿þøÝ«nVíí~u÷FþÇ3GÉWrÓè.éà\x0014®\x0017TïÔõÿrBÀ<¦=>\x001c\x0002N\x0013/! í:\x000btr.DCPS¦]\x001dSÎÛ\x0000\x0010À-\x0000\x001c)\x001a\x0000W²9L.IÌÉ\x0017\x001f#lc@·\x0018PùÉ \x0014QutÊ/Uy¨\x0013ÖÞ¶1 À[\x000cXc²\x0019ä\x000eM5Ó\x0014ÓÔ¶
\x0001\x0001ÝB@\x0015k¬hø5\x0004TSwÓôë\x0007øj¶Ñ\x0006ÐH¶IdÊ¶!& [©\x0001©\x0003:ßW²øÂèi\x0006\x0010\x0013Ð-Äl: Ö\x0008&OªÊLóâGhq1
\x001ebÌæ5>êæPM#X¹\x000c&úù2)È6$i`Ss×iÏ\x0019~Ýó#K^\x000f\x0011\x0000À\x0007X||	èÞS\d-ã\x001fÀÏw¼I56%¿$$Õ2Ü9ípò¼ö8*\x0010\x0000à\x000bìÉhR÷
_¹ãT6e^Îk8Î¢~_çpE}ñæý·ÿþÏ_¿¹y{ýìéÂ\hòZFË\x001bÍ²îÃOLr>9ÿ¿ý±ðµlñ×­7mLIW\x0001¢¤¦<\x0003]«ç^L\x000fwÊzp.ðSëbºåXVRv\x001afßç\x000b\x0001\x001dò²Z¸nSqÌ\x0019Wå?áã¼²V×\x0013à3ÀwLu*\x0001\x000fç­*U÷\x0015>¥ím\x000eðvë³Ü:Á7Î\x0017\x0012ÿÚhÝ.Û\x000b\x0017àíÂÕ¦øR\x0001¾rÃI­w|	áp.¿yÿ·Û[ñß¼½zñ_îoÄ{\x0006ê^	²©\x0013®¹ 1ÛpKä¹MìK\x0004ÖÆ\x000cÍçÏ¹í3öë\x0011Öä[ô\x0019\x001b\x000eªÝF|§ºØÃ\x000f^§õt\x00036¸§\x000eeFÍ
\x00109·\x0017êÀ\x0016ðqþÖÓ\x0007àF¡í\x0005ÆÂ'\x000bï|úªÓò,mÓw\x0008à	À±9¬BåW×#	õ´\x0013ZE\x00007:\x000c_ÁûI§`©,­Ð¼òèw´\x0000nä\x000cºGù{\x001cÝ\x0006ÏÞ@\x00007B\x000c¥µ\x0004mÒ·'ðÖ\x0005LV^ú®7ÐÐ\x0010#çQÁ.âPõÕId\x0011\x0008=ã ÷·ßÝÝä
\x001f«¾åïïï~x9nñ\x000e´ôÈ,!o\x001a"jwÐøUÿÒp£	j½4òZ\x0008ö|è^¿\x0014\x000e\x0010:hTr\x000bK´\x0004yÌÆÚf5+¯lÂé\x0004b6æW3\x000ffkÃ3È¯Â\x0005ø
Øt\x0004¿s![ÊøMË¯mð\x0019+¼8ð&tUÐû4ñ×û»×á¨ýæêÅ®¾º¿ùñý3ìe¥ßb¾~¡$XÓ\x00188Ãmü?H+{ß?Wj\x0006vKí&æ7*ê;ÚÃû°cI\x0001p\x001b\x0015_\x0014îK½ìøHM]·
7o\x0014'\x0002GÝÒÖ¹GÀ©3K¾dÜ1\x001b\x0002¸ÜÖÐ D\x000bF<¬ò;WwL
\x0000nóëÕ×\x000b\x001f².<P~HU¬X²µ\x001d¿<@Ûðº
_äFënl\x0014îãu×\x001d\x001f\x00147\x0000O6U*\x000b×Ñ\x001aÂ\x000eÄ^Ô"\x001f`wZ¸q×ëÿÃTÇTh½ÛS\x001b\x001a:\x0008èªB½RýÒn+fa=Te½9¸ºïßß¾:&Tÿtuÿ×«××ï´©ÑeTó {\x001f¿)+O\x0001ÜàÊûþ\x000fòÆ§1ù6ÒÆ	ì-\x001eãâ`*Þ8õåã6Þ8`_¼qeâ§Qô^¸ôÕä]vÞ8G[¸oPç\x0017"§\x0017âÄ7\x000eàÉV.1Ê%\x0003¢Ä\x0008\x0005"ã8B³¨;)
\x0000Ï¶r½£\x0013l#Ç
Bµ÷e\x000fÎöÙ\x0003ÑªW[yÎ\x0016\x0005Ï¬Lß´\x0011ÁG\x0013ý
ÕÀ;|P¤g\x000fê\x00089ÖÅ&~ËämÐ6H3,^Á(\x000f</éá\x0012ôtL«½ºIß÷ÓÖ¹»ÿúúÅ¯ß¾ùû}öÛtÚèö{\]Ñ\x0007\x0006\x001f§\x0018FM`$&rÖ	$\x0013oV]÷TãÌÃ"éÒ¸,üS]\x0019m4QèÊö¤+£å\x00122jÆkÃ\x0005J\x001b\x0016õpp#Ä\x0014v¤Ï\x001d\x0000;\x0011¶ç\x0018[±©Ûö1y»^\x0019\x0000\x001e
\§ì5Í­R§ SfXµ£ÝÎ9\x0002ðKÚ9\x0001~Ó¹ÎJtßy0x­«ÿ\x0002à\x0005Àõè\£+CÁÉgTÆÜ¸¹2\x0000¼\x0012ø%!3nV\x001aWpºìfaÇ!\x0007àÍÀÅID+¥Ü\x0002N11Ö­t\x0001w\x0000ÏÖÒ"à®\x000fÅ`\x0000\x000fW\x001eGLupa\x000cÝJ,YSÅ	ÐU¬%1zZìÒýîÂ\x0003t\x000fèÞ\x001e^¹\x0015z¢ÆãÎ4¤­\x00061 Û9ÊÊº\x0001k\x0017ÿ7ðn\x000cÑGmë08\x0008à\x0011\x000e\x0002{Jå\x0017iPk³t¿çÉ\x0002t8H*N\x000eÛÑe-ò¸úMÓ®9\x000c°3m\x0018oØÊ\x000bèxå¬ô¦C[Í\x0005@·TtØÎ®X#½ar¿4r×cð÷Ðaeè\x0001·ãö\x0019yú
ÚuX\x0001:\êê¯{[»x<È4%k\x001eýõèóà®8´X\x0001:Ü¼\x0001TB\x001fC	üdd2»O}Ûa\x0005àxóFS¥c=GïôÆV#&=´@\x00014Þ»ÍJÄCÈkôò1
~Zåün\x000cöKýâjå±ó}´´\x001cFï\x000c=:xíÜK\x0000×/À¦ÁU\x0000l;x\x0007Ø¸[º1½êdP'ÿXÀ\x0003\x0000E×ÝVó\x0015Ð\x0013ì\x0016o"AW²BÞÔ·.k¦â0_\x0006è\x0005ÐyÈª6â_.\x001b½ñFwÓÃ8ÿ¤\x0011>i/aåªúÌ»1Ð4Itm\x0004%¾\x001e	6ðA
Ù6)ÑM\x000e>\x0012QýE\x001bCfOý
\x0017\x000fã\x001cãZY\V\x0015MÍGñ¡ãÁ\x001d¿|ûóûcþO÷W·¿ÿw7ou4æYTXR ¶À\x0014B%-PÃqZ/ê_BB±[\x0013?ìO.	Em$ûi{\_í±c\x0007hc7 \x000bºzR\x0004PÉ+yv°R¬ë£\x0000à«Ì\x0011É
Ê>RÁV¼o\x001a&O½spËUª/hºÑ²ò-)ùDî¸×]\x0004\x000fà«Ô\x0015ÓnsJyå±.à\x001bO\x001f S\x0016Õ´\x0005º2)Còª\x0004º»7>`\x0003¥lÀM°µ	±sã¯éÓÎÑ\x0007pKU&6\x0004ìJú¿z(\x001dïÂñ­n>@[¦RKù°OâÂà\x0016Õ\x0014\x001e\x0018<ÖgÒÀ!QRÆÓ\x0013ù
u\x0007ºè\x0004¼n¹p\x0001é+ «\x0002g«4ÞânD\x0007'\x001fÐít*å¾Éh;å\x0005¨d\x0018OØæ.l½|@\x001eÐ0Áq£Ó<°|½\x000fàv<ål\x0003; /)T"ë\x0012ôºe\x0007\x0001ô\x000cè0W'è\x001d\x0008A/k	\x000f\x0014çG\x0014ÉpÅßh\x00033i:×>ÂC\x0010\x0001è\x0015Ð\x000b]\x0000>q#@R\x0016;^{Ù
\x0002:á¶Õ
e\x001dàc\x001a\x001d§åÃ\x0018I:L\x00008³Jw0»JCÒG 
ScØÅ?\x001eà :h¨Ô¥§åö
,ú,\x001btä\x001f\x000fñ\x000f \x0003kuJ~TÏª\x001eêÚ/Û}ø\x0007V\x0016@*{$Ã©õ°!ù\x001aHi;¿\x0002à@[]ãKx£ã¢R¨!Ïr=Î1ó
\x001cÁ:Qa;Ö¾\x0010nÈ\x0005Åêò\x0005Ðµº:h»#¼ôV\x0000_Ñü|Þ\x0000\x001dÞÒÄRNÙ\x0018\x001a¯Ý/\x000fG\x001eØ\x0007Ê\x0017@ZPCÎùÜ8¬=\x0006Þ\x0012cíbC@ç´yÚíâ\x0016ðõë[`Ë¹ÛÏOjZ¨öçkcî7];¿\x001ci¨\x001e"OCpRå
«ÞW»ûBDé!Sq=\x0001\x001dNjÐ´ã´ýo0.pè#¸\x001bí\x0001l8Jê!Án×B1?z+Ü²Ûãn´\x0007ÐñYò \x0000)èKå_\x001e½²¥¶e6\x0001tðî¶\x0017î\x0001­ü°'|Yvû¿oØA\x000c\x001cÈ¼5Çïµ6"ònäû«ÄÖal\x0008°!\x000ep\x000eXåÊ÷,<xtK«?ÎÞ|wÿíû¯\x000fzo%Þüý·×¿ÿvóê9jÅÌ¢Ss)½Y\Àæ)_§|\x0011Åâ}óô#fs)\x0016ë$;0t)É5^\x001b£ti«÷	àP-îÁÃ¸¼ÑØ\x0014ð¸+ý\x0000x\x0004ð\x0000ÒDQsùKÑ®\x0004þ~Wú\x0001p«\x0016ËÅ®fcAL\x000bº¬êËHÈ\x001c¸m\x000c<ÃÊ\x000bn#õ×³Ú}õ\x0003·aC±¸w"þ.ì
êÂÈ)·v<y÷?Æ·×qwò®ßÞ>\x0007U«DU]\x001c|Óó2\x0011üáZ=$®Z\x001bQéç?uûÞÇ\x000cõ0å'\x0008\x0014\x0013JQÃAdvÍÑÛn{\x0001xþ\x0003Ú«X&W) MÀ¹ÖÛð{\x000f"Ô\x0006^	Ü[:´)Ý\x0002N\x000e\x0012ûleË
»\x0003v4Æ0ØÔmmx\x001475\x001d\x001b\x001eû\x000fîëöv×0ð/W_ÝÜÞüþ\x001f÷ÏÑ¾ë9©\x0010ë¨Æ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-27.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-27.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Å®bóAA¹),ëxÀë°K¤J§\x0016©F	
oÅonÞ½;Ýõ:¼Å+´yP\x001fK>\x000bÄÔy\x000cE\x001a!\x0005\x001e¥à\x000c´\x0003ª?Ý=~a1¯7x<<å2½ý¹m©Ç0ÑYÛ\x0018é\x0004:Ú È9Â[½~½+m©ÂK£éÇ\x000b>ªá\x0019\x001bÔ\x0017J&<Ä\x0014)\x0018Å:Úèà²åûéRW\x0008 ³Æ@±K¤S´KÔC{Ù\x00075·uãÉUÍg-ÄãÖ`dx2Ã b\x0013\x001eÔWÊ~<\x0006º%7V@æG\x001c=\x0014/\x000b±æ\x000eËN÷/½¨	F\x000fb±&m\%\x001dÁ\x0004*3|VjÂ±7ª\x001b/ì\x0001\x000c\x0003Â\x0008pñ\x001c4\x001aoopØ,ÁZ\x001bgûGÏh4{6ÊB§µ\x0017Î\x000f´+JnMxÐ$Õ÷ãé\x0000áð|\x0013Qª\x001aÔóÂöt&óa|¡\x0005Ãcü­ÏøÔÐ\x0011ìQøD\x0018Ö¡C»ç¥^bø8t­¿õ\x0016mA²*\x001e\x001b"^Ê£i±\x001cÇÏ§Ö\x0003|ÿö×»\x0007f\x000bßë¼Óá-4hçêt¦A
%íÜÑÎÈ\x000eË.´?o~ùõ/·ÅË_Ì\x001d~~ü¼ÀÝVÂ8t·-T«\x0018\x001c`Á\x001aÒ&ñS&æååÍÕë9 )q\x0014Ðü\x0000\x000c\x0005'0ó\x00114&P­§ÎáÙ éåì( RÄr\x0000Õ±0r´ÙzÊÙÍ	ªÐ\x001d	T\x001d/\x0005\x0012ãBÌj|àSë\x0005S\x000f\x0007'çÇûTë\x0015HA'Ð'Pg\x0011TÑKd\x0003(ÈªÀ¯crTÒ\x0002(\x0008¦ÉDª}Òp±t£\x001f\x00146Óv\x0013÷ü2(6b1É 	AÕqIº}ó8\x0002ªdÚ¡\x0013d\x000cd\x0004\x0018\x0010à(°
¢Cqp\x001e¹<Î\x001e\x0002ÓzJ¦_r:ä¢QE\x001e;Æ\x0002ö¼\x000ec\x0018Ê@ñ\x0008 z´Ö\x0003(\x001f=\x001fD½·ö1Ê%FÝøÛ9d1?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-28.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-28.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;?9?ýnuñî8¾*ñU'¾ËÞ"¦`DnÍ30ÔÒôº¤×ôX<C)0óG\x001cl9çÀì5\x0016çÒÞtÒk~êW!w\x0007qK@-íÓK3ée}ð{O¾5¹Õ}nµá¬ÈÍÔ÷\x0016=îÁß7"h_I´\x0004üIß*,7~År Èý!òø½9#\x001fáý¸\x000eè9Õ\x0001ß¼\x0001\x001fãË	3N\x0003·zèì5cQð \x0014\x0015ÙÓ°{}høooÀ¹xwÂÿãqf]2ëùÌØu\x0015\x0014wt:¿tî/:ÝfÞÙZ/\x0003Û\x0012ØÎ\x0006\x0006YÂ\x0001\x0000k5iÔh´¶ù©s|¾ËpÝX/¹b.Mó©F7tÎÈZ;ª¹V:\x0014so+ãÀ»wÅ\x0004YàS\x0002UtlwY/Y(zw¤×ïTt7ÌàÒd\x0006î\x0012ðtrõôáÓ4óEÄ r&©Å\x001a7\x001a¡¥¹_ÛìÁ\x001d\x0002®O®®±\x0002õPÄBÎÒýòâÓ¯ÿûËÍúi¢Cg40¦½vùDÇG½#³ì{ñíêÝéêú8³*Õlf,µçý1\x000fXñ1g[î¯\x0000ig6%³Ïl\x001dj÷á2ê/Ã\x0006;I.ÅlKfÛ±Ï6GUp:\x001cms.ÁÒÇ-«ãÈv|­.ZÜ
3â~ý÷av.E@q¶\x0000ÄF¡{»ÓM\x001c
Û;T^ïìF9*÷GÚØ0\x001dÙ&;A\x0014¼
\\x000eé6á·½Søvül?µ\x000e4©A\x0019¤Am.ö\x001fOkøÃ-½h,l¸\x0018·CMmùÀò¦Î`ï}\x001fÁD±ÿ¸^½»:¥v4z£ÏÕÖ(¦]ã¨ÐÛ4öêæÃÝú¶¡\x000b{ð ¦SÑ8´iPí.\x0004ò8õþÇ\x0012øí\x0015\x001c4{öêôÅùêïÀ×c|½\x0003¿5ÿ*\x0018}r\x00083Û\x0001~8,Î
j@
\x0012eïÛYI_$bÕèæ{ñéïý+?ò\x000e·òöËp ¿Yÿ\x001aç(8
®\x0005P¾%I`=§÷~ºÃL\¡\x0004MyÇ^®it\x001c¶Ã¹~súÇ\x0017gï\x0006ÀoV>Ð\x001c§"JC$[d:¢
í¸ä¤#RÊÿ\x0002¤hu'\x0012ü}Ý\x0004ÿâ¡*	p\x0013)!cJ¸7ÎËXÜA\x0004lÚÜ3£\x0012Q4©\x0001ø»yr\x0007:@\x000eØ&$P,W\x0002\x000bäÒwúÇ\x0003I;ÀGumH\x0014Ð\x0004$åS5\x0019 aGåd»w	\x000c\x0018ß¤H\x0018\x00001¯> ¥¾¨Øã7µ§î \x00156"ýÌÉDÄ\x000f¼H¤(Õow\x0000Áßm@"MJ\x0003  òm³\x000eR\x0010½Hè:\x000cîÃt&°N|:I\x0016|´a\x000e2¥:	`R¶ó»aG¶n\x0011òéÆIL::fÒ§\x001b\x000b©eð*EX	[A»Äd\x0018IôÊnLlmÂ[R>1 YÂðÓ	KÁuÊ%,mâ[Æôz\x000bLÚ£$OL)ûÃà\x001c\x000bÙÉ³ÃÛä7N@\x000e$¿}ßÀÂÂRôî\x0013\x000e
o\x0014à\x0016Ýó¤æÐÐ#\x0001\x001eÉ\x0016ðZ÷'¸¶²Mc\x0005\x0000©^\x001c\x0004Oâ)x\x0016RwZ\x0003Ø4O¶Ép0Ý"í\x00138°tÄ£Ðl2¹^$¸²M\x001bª±Ð°¤zydÒÙ²L
$¸jâ*&ç\x001e¯I\x0001	<NY\x001487ëÚ=¹üü»ïq\x0008\x001e\x001arj¨æ9ùöáé\x001f\x0007`R¤wÕÔ\x0017®$ñ
RIVj\x000e<o/¯ÿs
E\x0008;	ÂÙá]\x0000\x0019²ª\x0005+Ä\x0012ðý:A¬'PX\x0010=C\x0015¢RÃo\x0013\x00068}1l\x000bÆß\x001e>~\x0011þ{ì\x000c5(Uü\x0015þ¯î\x001e¾ÜÞ<\x001e8!V\x001aÊ{\x0004gtª\x0014K1`9¦ú²:y}}~Ù?ûGÉÛ2\x0010­ÿ¯"=Ý®õ§Ï\x0018HEA3ü\x0002ÿÖWw\x000f¹'Û\x001e\x001cø¤:\x0015îÂ½v\x001aÓlÑ=\x000b4`\x0005Å
#Wçû®U8\x0011qâd\x001c\x001c££È5\x0013659\x0017*HWÚ9Óòeø¥\x0001'$La&}¢ÔÍ0úÖ/ëÂ¹ß$x Ô{sóóíýá#¤\x0015\x001bC¢"\x0018\x00165ÇÄùkÍÒïÍé³§éîN|úQ\x000e\x0007\
Ç[
\x001bö§§÷·G6Ìz¯È\x001f`í§\x000chøM&sn¼cº~~vxÇJïß\x0013Ðû©DhV\x000fí¡\x0008ÃNÃf\x0019°\x0018É«Øô>LF
T\x0014Ã\x00109;ãgûþ7ò¬g=ÇÈô\x0018\x001fÍ§á¨\x0002¯>#ÕæÆ$"ùáÓ¿¹âã+`
$ï;Ö!¸!£@a1\x0002xÙ°
´\x000ccµ1Ä'\x0010¤\x0000Ñÿ=\x0002\x001d\x001c_3D¸ÜÉ¿Q\x0006_\x0012m \x0001\x0018Rz\x0016ÃP63ü2e\x001fâ\x0010\x000bÇµgöÁ¦:^ÜÚÖ;ÆðwõaýQ\x0015gauwwb¯¯nîo|¶}\x0012\x0018û4±Ç S^½ÀQ\x0017=Z=­ÎÏOStõÕéÅéÞ¤µ)E4Û(\x0012ä\x0008Q®\x0017'\x001dÖ\x0016\x001cm³G,Dê\x0019,pN\x000c{UÆô2¥xf\x0013b³\x0002æÒ!¶2;Ä&ø^¦\x0014Ðla²\x001b&lRDFó&ÙÚÍCâ-D m5W¤IYß\x0000¥søÐºØ\x000b"-P"\x0019(è¾9ËÛäí%J\x0011Í&"ÿ,Ð6)JL@(\x001dsx¥ûÖ¥¨f\x000bT9¾¢Ù!V6(\x0016\x0005¾÷<qX³\x0011Ê+
G\x000b×!TþÊÞ{ÇÍ&ªR©J¦\x0006á@\x00153½P\x0014FlÂg<:éÖ¤j\x0011\x0013sX³ÄbóË?þ¹þë\x000ffÉi\x0000\x0001\x001b¤Èhì!\x0017\x001e,ú@Æ¡\x0014i\x0014.8Ï4°\x0015g\x0003Jãå7ÿÝÐÒ?}
ÚÏG9æ¿\x001dBÿ¹{ò©°i.wus¿¾ýüy}ÿáogmèÞ\x0000îµu¤\x000c¥JUcà]Z~mZÉ]^¬ÎÞ¾]]¼ØoÔ\x0016téÓ¶ÒIñ§­8×$Áv
t²÷³é
ÑL'i\x0014Ò\x0005~\x0004KB\x0011RËà%s¢\x0019\x000f$¡ÈIä¨¨
7Ï\x0008=î_w·O\x001aÜr)0ó7ý\x0011ÇcQ\x0002
?\x001aÌe\x0019áh§\x000e'è6p\x0004Yk1vz__\x0002Óa\x0007*\x0003IÌXH¿N\x0006\x0012ôä&c\x001cSà9P\x0014\x0005ÿF3Ð:üòóÇø=ÆØñ1\x0002ë5fF\x001c\x000eX(°ÒÑ\x0018$ð\x0014ó\x0002\x001dLåÄØ\x0007±Â!L±;f\x0003}\x0019ð\x00191ÈÊl\x000bb ioT\x0004ü\x0000\x0018ÝØ\x000bo#2\x0003Näa[\x0010Ï\x001a·°1Uã\x001b/¢\x0018G¾&\x0010OúÇû¿`z\x0017Æ\x0004-\x0005\x0006_|Zÿ´¦t}gÈ{~ÿ\x0007	`SNp|Lj¡e¼¥a\x0007%Ï·+\x0010ðU2Î\x0018ç¯áï¿à\x0019h,\x000f¿7Z¤Çí
y\x0019râð81,½°õNr]¨Q\ð4çÀícùòË¿\x001eþñáéáiÞ§_à@$Ò\x0004W8?Î¢:Ä	È%þZ"ÚíÝ¹þ"oû\x001eýÃýßÿ>0Ù)]²W·G\x000f\x0001Ó\x001c§à\x0007R´±i	iu°òìêØùùñ\x001fþåïvÇÞD$ÈÂd K9L'AÙs[lI \x000cr\x000f\x0002h\x001f_þá\x0014|	\x001d~Ãs³G\x000e\x001e\x001eøq(öPjè{ä³£>\x0017&`ÏÜÑÙ¹Âé"\x000eOÁâÅMfq,xà3ÙÔ£\x0007[NQH9àûv\x0007L@0\x0015\x0006\x00043=ê)Ó\x0002
ì=ïñz\x001cèi\x0008\x0013§Âh0M¯FÆ=ãÈ¿âÀWãà[\x0003\x000bz\x0018Ã/\x0013¿RðX¬:|%ëÓØ\x0014øJÎÑ\x000bV¾\x0019FX¶L?¨£aï@,?Þ\x001ea$\x0007Oiª\x0019Ã0\x0006'Ø¸Çiy\x0007¢ùêl¿×éTI§\x001aé\x000c]4\x0016rÐÇXòmØç\x0012OÓ%nÃÇ\x0004çé
¦-=»\x0001\Ø\x0013j\x000cgJ8Ó\x0008\x0007û¥\x000e,6þ®Rówõ½t¶¤³t2rj\x0012¾=ÑÞ	\x0013yïêw°\x0019t®¤st}\x0002\x001d\x000eÏNçÎD!yïdï¹ó%oÂÓ8Âñ§Õ´yC\x0007O¢³½W6t¡Î§*+Ü<æ'"\x001eÅû¬Ó{\x0002FébI\x0017\x001bé²7\x000ft\x0011·q sô\x0012vOäo*¬¥q8\x001eø<áù4z\x0006ñØ°.ÎÅ\x0003o¶V\x0016ð:\x001eòj}ð\x0018L\x0001,J~FJèq§¯À6¾ò«ÕáL¥J*Õ@¥pàeº\x000c\x0011Çý¦4"í-½Æb^h\x000f.ÁtÓvÑ8=\x0000Ó!\x00020MéÎ^=¡i\¦ä2-\Q
5²%°)ðå4SÉ®í²%mÁÂ\x000c5Ú.¯Ó,\x0012!\x0015§y¥kC¤\x0015Ì`®\x0005\x000ccÍ&G>`6DÇ\x001d\x000b]\x001fÒ`¾\x0005\x000c4|L:4ÆO¯¼`0köD&§\x0012,´¹¼\x001a±]§ÏAIÃÎ;Àb	\x0016[À¤ \x001dÃRqüª)\x001c)ø9ßó)©üE«h!³f\x0007ß¤âMØ1ÉÒ\x0015þê\x0001«e~Ð\x0017âò!5ÿýÒO\x000f='LVB_¶H}Y$,acp
,;Þ/\x00024\x0017¬\x0012ú²Eê\x000bpîÙ-\x0005TJ`Ò[Î|ÁN\x0007Y%öeÜ\x0007õøSr\x0004eH¥\x000c«£\x0018z.¥¬\x0004¿lüÂR_$ ó¿¥t9jß\x0003Ë4°JðË\x0016É\x000fò\x001e;1ð·L.\x0014nc0ÑcóÈJòË\x0016Ñ£+-	² Ù\x001aE?Îêè!«D¿lýØf*a)lE\x000e?\x000b~Àê\x0012cêû/C	)3ð'
*Óç}3a£2%)\x0000-º4[²
\x0010³/5\x001d9mRÈU*jT®»{®lî\x0003þ¤éJ¸ãJØE®Ðc@ÝÆ!bAV$\x0018üà\x0018\x0003K9)ú¬Èñ\x0007v\x00070X®¦ØYÂ1©²i\x0014:ùFû×ø}ÆÈö/¤þÈÇ²\x0018\x001b÷h¯­óg\x001aÏ_à\x001a¤!±TÑ÷\x0005è²y¥Ú\x0002T\x001b¨\ò®\x0006\x0001CòÅñ+E§|\x0011[û×¸}J\x0018..ÚRl\x0006åÀ\x0016Âu}_¹µ}²ñûzåÙO1²|étOõøþêÆû«sYuä\x00082àx\x0003eËõýûÚézß\x0016o\x0008äØ[ùÌ²×Å§R}¢/|¿®ÙÖmbÅËìªFö¡9H£¬e\x0018¸ªéHúAÑtäãÓÉùíÍ¡Wàè$ù\x0011\x0002§õ(·åb`ks}ÓÞçüìt_7\x0002L`ª\x0005L³¥\x0002\x0016§·+\x001d8z\x001fê§òV,]bé\x0016,Ô_°dÚ,\x0013\x0018ÊÕOÔ­T¦¤2M_1PHËr|àR\x0019KöPÙÊN§2 9uÒ{ÏgËÓ\x001bÚ\x001aw¹\x0012Ì5\x0005Ö\x0002pï(Ý.Í'&°è{À|	æ[ÀtVO\x0016=AÉoVsh|×\x0001%Xl\x0001ëB-²@\x000f[WDÙÃµ\x001b
âK´eéÅáµ{\x0000óA1õ)Áª\x0005+ÚU`M
§W÷\x001fnoîOÞ=®úûú\x0007.¨ò\x00199XWÌ\x000eG#¥àF¸:¼ÅØbzuñâìôâäÝÕêõÿ»úóqbU\x0012«ùÄ 
R	Ä:\jzá\x001c\x0017U:\x0013w^Þ9È¦D6óUÎ¢Åf&dÀÞRhß¡Ä^\x0008ÙÈ¶\x0003Ùs\x0002¦±Ì«xCý\x0014×Ã\x001bKÞ8×eóÔ
Á\x0001\x000e/©ZÇû5\x001fÙXñý\x000fÕ¹°â?ÌåÖ\x0018¡}íþÍÉ0¶ûþi1\x0018\x0018îß´½|ùðáËÍÓãÉë!Ùô\x0000«Å*];ËAg9Ë±ð-Kñúäååw§×W'¯/¤ÓãªÄT30
ØØ¯C£iK½Ô>G\x001a¶#!3@u	ªçì§µlè8V\x0018,¿CJ\x001få\x0012 ¦\x00045s@õÐq;ùVYäÂ\x001fÔ\x0007\x001c\x0019 ¶\x0004µ³v4R\x0005aðC®ÃÀÉi¬ÒíÈiéJL7\x0007\x0013\x001cT~ÆYæé¬ue4ÛO\x00113@}	êç:Ë9\x0019Ág¼\x000f¨ÙáóÏà\x000c%gõÝ\x0015[!|@mþð;^PfpÆ3ÎÚÏHU\x0017"\x0019^9çzp¹Ì=ÚX­¤\x0017³64á\x0005ë¨b
6r\x000fáËëípÔ\x000cÒZ'ÍRJA²;\x001e@?\x0011hÔ,\x001e\x0017á¬£°]1m(ÖÅÑMÒ¼*.!d¥ä,¥\x00145¥Nú`ÙØV9ígØQy3\x0003´ÒIrRò
sQÒ¼£¯¼\¥J%É9:	kNL\x0012ö\x001e'?Q_5Î\x0019<Ë\x0005@+¥$gi¥à8kæN\x000f ëéÛ!Ô\x0019¤VsÔ\x001314Ä-À\x00155õ\x0019õàq/!ïe¥ä\x001cÅ\x0004îó3ê à-çúÊ¨¸tÄÚE,¼êq$ÙÍ9¸ßd:ûÈú>
j¡5`\ÂE6VTÏÅ7\x0007ûx£Èv`õcí(e2L}×a)CùâÓ\x001ak>>Ý\x001fzÙáÑ«¸§«TMÔyOw\x0005ÿ©¢éåõÅq:UÒ©F:où\x0006üÉr\x0002Çå¨ß\x000cÙ§K<Ý\x0017c\x001aa\x000e$½*Z\x0010P¼y;ó\x0016ZðLgZ¿­ãÒÂ\x0010s\x001aù¾x³ëÕ®\x0005Ïx¶
OÃ\x0011\x001eî\x001eõÏ´JFÞ=·-~Úð\çZ?n`1\x001eÀÖÐ?.ã\x0012Ògàù\x0012Ï7î\x000c\k\x0010eÎËÂøBÞ½Þ«\x0011J¼Ðúq\x0015·Á\x001a@ê\x000cf¥ÎÑ)-x±ÄxÊå|\x000f)9kØ\x001a³IKï¼\x001a\x001b7gÊ¢õëúg&ïá«øìù°+]¦\x0005¯V\x001aZC\x0005Òwj}v\x0018v'\x0005¶ðUjC6ê
ü¼dÕâþ)â3Ùåîß¿JoÈFÅ¡AqÐóK\x0000\x0005LÆ¬3T)ñ½ ¯R\x001c²QsÀ\x0007fïeØ?:ÜW\x0003¶¯\x0017¯R\x001c²Qs\x0018¬éc³Àr3hç¹æYú^Í!+Í!\x001bU6TñÝ\x000fønH·ØÙ«ôlT\x001cøBE©(Á\x000bJ5r3µ@ÊìJEiÁ«ôlU\x001c&pßÍlÓ´}hï´He¥8d£æ0Ú=#Êq
éb¾\x001a¦S­©Jo¨V½a-ç¥H³ÊqÒº]JëªJo¨F½ï`\x001c\x000e\x000b»Ý{­òÅ\x0006³ªÝV½þº£íóü8c£Þ\x0008^¾Jo¨F½s\x0014\x0014Çé\x0014[U^å¸Òî4Ð\x0016¾Jo¨V½Yú¾¹%¾S'GíçgðUCµ*\x000e<tÔÙ$R{Q9ôÄOxp?:ñ*½¡ZõFôùA\x0003g¯+2\x000b²Ãæz¿n¥9T«æ\x0008jL\x0003§¤u½å\x001cF)|ïå¨4jÔ\x001c\x0006kY±\x0019vw3üum¯U +Ù¬\x001be³\x0001K*\x0015óèùôYÑyút%u«p\x000e:ÞÍÃ´ãØ:\x0016\x0016tâU²Y7ÊfT¼dÎ¥[9EZÊ^T×¡ VÑ\x001c%6\x0003â\x001eN?ð9>\x001dm/_%u£h6i¸cÚ>E\x001d>AudÑ,c§Yª+Ñ¬\x001bE³Å\x0001÷#%¤©LCB¼\x0008;\x0013¸[ð*Ñ¬\x001bE³q:SêÐ\á
§ÂH){·¯ÍºQ6\x0003!\x0006ÄÓþåG ¹²Kì,³oÁ«d³nÍsÌàCZ6\x000c<7´öRìxgjã«¬zÝhÕ[°¦¨~ÅoîÁÆâ7\x001b½#TßÄg*ÝaZuGÌõ5Þç\x001eð¥óç\x0015ÒÅTºÃ4ê\x000e|?¦Æª^FFSi¹+ÚÎú®\x0016¾JyFåa1Ç1)7\x000e&å6H>\x0002{\x0003õñÕúFélå\x0019w`åq<2\x0018\x000e6ã]éä«Äi\x0014\x000cÆo?.G4\x0004ÜN¸J¸Fá©ÕZ(ê¬z£ æa.\x001dï-|ð/¨Þ9B«ô³!M\x0019EÝëx W6gÖtÆ\°OZ\x0001ÿµñz\x0004nú\x0004\x0016\x0001Çûàs\x001aÚY°ß\x0002\x0018jÀæ\x001dÜº\x0008?ÍY.fë¯[ý¯Ô¤\x001a´×Øpê\x001c>¨\x0007¾Æ&?ý÷¾\x0019i±)1\x0002OÊ#M,²!£wäQ4>Ì\x0011c3¡Öõ	fÉR¢µ!·éµgêCz\x0004iÆÄ3s,\x0015'¢9<^vFÛÌÖ×63¾6¾ý²i­¸{\x000f\x001f+º£åJ1jßK°°)1zxë×´Ö/{Þ¢ÔíÆËiü³Àü\x001c\x0003\x0019Í
\x0013`ÝÔKRuÝHÈO\x00016;*²¸ß½rk\x001fMû>Z|à$L;Î[ÄööÎzì¦·ÿz\x001f]ã6ª¨7©'\x001dR+D\x000eeöúËðÛ÷ü1²ÝO%*?bÜ\x0000Å:ó;º_aÍ÷\x001fF\x001f\x001a\x0011-?\x0014ãkN¤wv99 Ü\x001b\x000fÞ\x0012=¶ýRûHe.sç\x0008äçX¹³LN,rÊN,
È'î¥§¦ðAoÆÖç0ÛEpjHéÐ\x0003¼ù|ûñæþÃÍÉnÖ÷'¯\x001fîn\x000f\x0011bÛ~\x001a°ì0Bl¹MJ®*\x001c¾={yzñâôäO§«××çg\x00130U©Ú1\x0015¶\T.j¹Y\x0005¶Ê¢2V½\x0004¥.)u;¥ æq\x000e®6!²=î¢\x0018ÕÌC4%¢ñ½±á8}ï\x000b\x001b4ÝÆ°Èç¶%¥±Þ`\x0013ûTëê8\x0019\x0004þ\®\x000e\x001eù\x000eó0]éfl&ø5ôðí¼ä¹¶*PÕwt#ûg\x001e¥/)ýÍÔ<Ò¹\x000bÈsw8Ç\x0018JÆ0c'\x0015W[
q\x0015ê¦\x0012HéÀQ5j\x0001ÌXbÆ9\x0017ü5?\x0006)4Î¨ùX`+
qEIh­{U+t*µÉs¬eI¤G¡yµæ¥z\x000cÇ°:È*î ÷Óø\x00058+Õ#gè\x001elEþS?:íå¸¿å<ÆJñÈ\x0019gD¤\x001f]®VVQñ5w~o^i\x001f9Cý\x0008PÞdÎ&Qäµ!\x0016ë²R?rþNrp
ls_"Oxñz«^é\x001f9C\x0001	ãf\x0015è\x0002\x0012¹wL\x001c¥\x001fÌã¬4¡dd;Ø¦æÃvn¤»Klg¥ä\x000c-$0\x0000ÈV¦ÏM
#Oè\x000cA.`\x001dÉJ\x000bÉ\x0019jHn\x001f©Ð{,±TKHNUi"5C\x0013
\x0003ù\x001a)Î¼\x0003z¥Ò\x0012&Rs4\x0011^wð ­y\x001fHù\x0005®ª 9HG\x001eX]spÈy?­]ÀàT6R³´gÓá$ÉÈ­\x0019ù|§­Íã¬î»sß± ,cLNb^\x001aVGÁ,!tuô{\x0004ûINºÅ­
ôÝsë2³Äw×ÕùÔsÎ§ÍÀÖäê9\x0019³³a\x0016pueèYFHà*&|Äå1\Å\x0004×H-ñÙ+í®çh÷h¹\x001d=^wC\x0006²±ùº»\x0005Ô®®ã¼åÊ\x0017ËF¼Ï³ðl\`/MuÌ\x001c§Hç<M£=©e¢\x0010Ù@^@Âê\x0006\x00197HnÁ±õ\x0008%hådÖ\x000b`ÖA¤9Q$¯93
\x0015;EÚµá©¼Á\x0005N¦©n\x0013 Qbç\x0011*ÊÒÜ¢\x001díø\x0005ü
SÝ 3ã\x0006)6âa3É_ç¸aðr\x0001Ùn«\x000bdg\ \x001c?\x0014¹a\x001f·»5EÑ\x0012ñ8[]\x001f;+LSþÐÑ 4#8¤°£a«ûcgÜ\x001f\x001c5E¹96æ²x\x001d³\x0001/Ì\x0012Õý±sîO°<ÞÃÁ÷§8¬ÎÃÓã8½}\x001eguì\x001c
ä\x000cË#µR´
¨å\x0002®ºDn\x00162´'c¨¹¤ÔReÃx\x0001ÌXmg%þ\x001b^[b\x001d\x0013M¶p²
³8w]µ¦_tâTÒ]\x0017³dçÇëUÕ1<=\x000f
¯ª¿IØ0
¿]X³\x0005k~Û´Å»5Ñ\x000e\x000f×­´Ömh\x0015^\x0019½ãÐex8°Õ\x000b¶Gk7å\x0018¾^?=Þ\x0002èÕú»ýÊYÏõ9\x001e\x001f6Ólpg¸´Sìè'÷zu}u\x0006W«ïNÏã©\x0012Oµâbmx\x0002!àå
	µ]~Õ§K<Ýg\x001c7\x001b2¬UÂÓ\»&ÔöhF<SâV<\x0013\x0015\x000f¨À'\x0018.Ï\x0011Û
\x001f\x001añlg\x001bñ0(Cå\x001b\`&quÎ áúð\çZñ\x0014w	òçß\x0000\x001eåæáKïÕð%oÄSnS} ¨\x001d\x0005XX_¢ê={¡Ä\x000b­x»=\x0007F\x0006:ài~CõÛx±ÄxàçPo~\x0017UJ\x0008\x0006O"»~»ÑT:\x0019GR\x0019Ãc@÷ðôeÈ{zýpÿå×xø²\x001fÏ\x0008ç9NÝ3i.,ØhÐ\x0018Fm)/¯ß
O¯//Þ¾¸|wO|ª/l*Ã´%Í­Ô9yL;×É§K>ÝÊcÃ©®Óå¹ºXîÉe§¡Ï|¦\x000fÆ¸Kä\x0005p(\x001dï\x001a\x00192í|¶ä³­û>5\x001e\x0004\x0012.Ên:¤é¨:ù\ÉçZ÷Ïçw\x001co#½)/rvw÷õð%oþ¼>Ü\x0007ê"
_×s\x001a­\x0016½§/x¡\x0015/æ\x0014\x001e\x0007\x0007¥qç>\x000f&\x001b²úøbÉ\x0017[ù@¤h®ÊV\x00144\x0001kFñé\x001bgÐÎØ¿Ò!I{8ø#­Ûèvì¢[l\x0017ÍÒÌ 4¹\x0006Ú{6\x0002Á°æ¤ó0[RÛñløAÑÅþÕãÃç\x0017nî
b¢<Eì\x000f@¯\x001fZçnfG»¾ëWWoO^|{zq`Þ\x001dOËF<Õgõ3µQÃ4Ir}»\x001c¿ÍlÑ}X\þò¸NtºÎå\x0001y¸yT@-\x0010óæíj«ß²y¦Ä3x8¥ð|nd©¢Û´
ÚÕa¹\x0005Ïx¶õÛú¬ã`÷¨ñAåÝÛníÑçJ<×\x0007î\x0007w5ò\x0007*än}vG¡U\x001b/ñ|ëÇu¹\x001d¹sÜtIÜëÐì(ïlÃ\x000b%^hÄS6×NæÇ\x0016p|óÅÝÙ,½.t±õÛ\x0016\x00177ð«
	½M\x000eì E#t<ÅÀèÜÇºÎo+kÑª4lnáýÈX*çú\x001a³cðk\x001b^¥3d«Ò\x0010>Ë½ßÐ\x0015¹£ØÕbº¯Ò\x001a²UmH\x001e»=ô\x000c¢¾\x000fÊå_vÇ\x0000õ6¾JmÈV½!d\x0016-¡ÈÚ|=vô#kÃ«ÔlÕ\x001bvËÙò£²Ü6c,ÝÇWé
Ù¨8Dë\x0014pÌ\x0019}ÞM¿4gz_¥8d«æ\x0010r\x0002¸qôÔ\x0008fs>~»Æ\x0004´àUC6j\x000ep9¸×a4yh©Ì-w\x000c¥m£«\x0014lÔ\x001c"ÜO\x000b;ÑÇÕ~ZYUC5j\x000e\x0001Ú\x001bBÅÈ\x0015d<Ø»¼¯Ò\x001cªQsàÝà¡4:\x001f=ÃVvG½u\x001b^ím4j\x000e9¾âVJî!¤;ÍµáUCµ*\x000e\x0010ÌÜÁ\x0017*Ë9K¾\x001dàm|âPCØ\ô\x0016±³\x0016>Ïx;jEÛè*½¡\x001aõ\x0006
\x0016Ï}@-¤\G¾d§XVÚP­jÃØ<\x0001KdO\ºÌ·«j\x001b_¥6T£Ú\x0010à\x0004é¢Í&\x001d>ásûèÞí«ÔjU\x001bà®E®TÜ\x0001\x0019¾n\x001e {O_¥8T«âp"Gì£ÎÚÅ$¶í§Ê6>]i\x000eÝª9Ä¦û¶ÊÝË¥ÈÞ±S´èJqèVÅasP1\x0018PúmÒ\x001d½óÛø*Í¡Û4Ñææïèú&³Elb-Qw^\x000f]Gª\x001aU0æï8c÷oÓ\x0013¡7\x0016¤+Õ¡ÛTÁä¡ë*rv³ÈwGß6ºJuèVÕ©n\x001b³*­M\x000béÞ¯[é\x000eÝ¦;Tt\x001drÅNª\x0004OÍTãÊýv¼JuèVÕ¡íf.ÎfU0½ÛWé\x000eÝ¦;T\x0004áB#\x001aÁ²O\x0018ÍS\w5lã«tnÕ\x001dÊ±å\x0012ËUh:\x001eô®ózJw6Ý¡¢q¹#1ì\x0014Á¡ãñ²¢×´2p6­Â\x0019û]
r"ÍX¿I|²÷~J8Vá\x000c\x0006\x000bµ´\x0018:z¥Ï+ód ;u©\x0011Ze³Êñ*\x001c)\x0016HºÍôà#ÛZø*élZ¥3.¼{\x001bîÍCzß\x0011L%M«p Ïèv`qÌÀ'bT,å>m|t6mÒy0]\x0002÷Ëó¶EÌ}ØÑ/©¯Î¦Q:ãÐ\x0006¶L½ \x0006D¾½zG\x000bó6¾J:6é\x000c¦K®\x0015JpÿEóþíh\x0013ÙÄg+él\x001b¥3N«¥§\x0008[Iyt HxÿÌÎ-|ioÛL{Ø?£\x0006Jq\x001bßaª*Ù~½áz[i\x000fÛ¨=\x0002\x001aÔ\x0016\x0012KrR®Z
¤ý³½¦½­´mÓ\x001e eCP©r'Záu\x001e­zùêgÞ6ñ\x000cÆ©Ìm5¥æqïo¿gn+ùl\x001bå³rÕp\x0004?ì8L|zWÿ6¾J>ÛVù\x000cûÇòE\x000bú<(î¹×W?Û*þ@§ñõÕl¼bp{¯vstq­ÒÅÍîå÷\x0004î/Ò\x001bÏuÕÍu­7Wç,É¨Âódúì·õJ\x0016WÝ\×zsu\x001e\x001e~\x0011=T
.öB¿¨óæºêf¸Ö!6
{-O&\x0002#cjð7:o®«®k¼\x001a8Î\x0013ì`C\x000f|Ng¾Ø¹¾º\x001b¾ñn` º\x001dDÌâ$ÃÊçQÁ;\x0006cµáU×Ã7^\x000f\x000c3S\x001abtz\x0003¡\x0007§¯×°÷Õõð×\x0003ÓØ°ÂÙ:	Osþ¡¿ÓW'\x00085Þ\x000eL\x000bb¯Ük
Z¡ÊQ
­;íR_Ý\x000eßz;¬È·#(JÓÀè$»fÇø&¾PÝÐz;@:[7\x001a\x000f|üÒ«ºÓÓBu;Bëíøÿ{»\x001c;\x001cßs+±ö~
IQj(¥¼¡T^Ô¼\x0014"N\x0001*©[\x001f
Ô<ÝmÜ·Á¼\x000cz\x001dµ»1ºæfÇ=n§ªÕ\x001fòT¶ú\x0007s3F#ÿ,±@ZÂúùÚaRé\x001c%¬\x001f-3ètù-¿\x0019¢¾óÕÍJê´D"&«´!M¯tÀâ2»à{eî*rR¶þÚóíW\x001b}1/¿ þ¦tÃ¹¾\x000cb}6¸¼Í\x000c?K¯¾4\x001eøÒ4Ï¡^ãXJ\x00149ryôîÍ)¥7ZÊb´QädÄhc5:ö[\x0015Åß¢l5À§Ï­ÛeãI6JyÊ1¦Úâo#¾\x0007,÷9å	r\x0003*Ä6cÍD.u§\x001fÙ:õG¦¯q\x0017w\x001aQm£Àf0î2¸:0êóÒ×¶Bc[Û>Z<\x001eû\x000f\x001dµ;Ú§Ð/¢TÅm4îè¶Æö­\x000b6zuÏ>¾ýòðõÓÜæ}÷ðáþëûß?éôÆHu¬Ó\x0007_ ¨yEÔ]¶CÙg¯þrûænn÷¾»}yóæÅ³Wg:¾\x0005\x001b[l<Mceæ}ZÚ\x001a\x0001%~7	1oE9Nm[j;²ØU\x0003føHB\x000cLn'db»\x0016Û
,6ÔyCÞøºGbÕÆM«p\x0014Û·Ø~`µCM\x0012ø\x0012\x0008À|ÉMTÂÍtfëqò(vh±Ã\x0000v6×,½`-`\x001a\x0002)ªjÖ_rÄ:\x000eP;¬úÁ\Ûy±c\x0008"·µí}b§\x0016;
`Sõ\x0004kÃða~ÿ7	ëÜá{:·Ôy\x001amÕº@·i±¦°1Jä0öÒ1ù\x001a3bÿ\x0008\x0013ªá\KSN¤\x0013Õ\x001ewÉM\x0002½\x001cp!¥ë ]VÒQ!Ër§ÍâÛ£Ø\x0001'\x0019C\x001d±ì½»ösÈ\x001e«ÔXòÕ#G¹;w\x0003\x0003þ&Ò ³E\x0015oN\x001fÄÄE\x0007ewÃ%»s70ào\x0002E}¼I"_6MpuäKº\x001bèÜ
ø\x001b Ê¶Ä^\x0003Ûm¨2-5G©;w\x0003\x0003þFEp\x0012'«=ç\x0015ñÑ\x000c\x000c¥ ó70âp0J\x0007»é\x000eU>scn÷qîÎãÀË	0u\x0011Ïë¯M`Ý\x0011\x0010M\x0019\x0017\oì\\x000e¸\x001cXÀ\£a¢­Ë.x(±ó88àqÈÍÈPbVæÙ-d
e6Û|>ÊÝ_ËF\Á*«\x001b»Iæ§ºJ¿\x0014<ÊÝ]Ìpàfæc\x0007»\x0010¤g¹\x0004)u8R¹ø\»s8à*C\x0010ýe\x001aáeÙ
mÒ\x0005­	v>\x0007\x0007|Nðµeäª:ZxlÁ\x0018wg½qÀzOö¬
U®\x000b.hC¡½ ·´\x0015´\x0003V$·Ä[:\x0019\x0016bb½OERÇ¸;sb\x0007Ì	]%\x0011MÍ0ñ9TîK\x0013Û\x001dK;p,=55°5Â¢b½eYv\x0019Ê£ØÝ±´\x0003ÇÒ'ûY\x0014+Xàf«\x0016;ÂI
d®7»yÿþááêÙÃç/>þíþ2s­ù¦¶"U¦¢íËjo^¼¸%e×¿Ü½úóÍYõ,%¡,ÔG\x0012ªÁêÀY´ý
ªÉlKfUdÞpWöÒ\x00024ú@^=À\\x000bæt`UÊÀG\x001eÔh¾Eó:´\+´¼´eâ"w¶j¡F\x000b-ZP¡\x0005i»`(+]ü}òG
\x0015[¨¨[/\x0006~*{ªÒÔç£^ZEZ´¤;±\x000c\x001bÉÏ's©Ø9f2ì©uÔÍ>|`+üõÃÇùÅë\x0011´s½\x0012ÚÌV\x0002£îè¿ç¯·/Ùð¾yùêùëo³aË:6\x0012ð1N\x001d0uEI
)õÍ«z8ÛÂY\x0015\4^­§!³Ú\x001aiÖt¢\x001ds-Ó­L\x0013£±Þ³Â±A^Õb_ÿ§'ó-×-\x001bú
\x0005R\x0016K\x001akKÒ{ð\x0016.(­*øx$·1Á¹:Ö.ô£Æõp±ÊórK,\x0011\=©Ik\x0013ÚÁÏZ¸¤4#f1#2^ìä¹ëD\x0012_\x000f[¸¬[94"¯Q\x000e¥_SÆ\x0000â\x0010[óFáfÙ(ÕÊ9¹\x001dyÈ<\x000cV7øY¡÷\x000e:÷\x0010©5.\x001a.w \x001a\x001c±rÆ\x000c®]ç\x001f@ç ¢1u\x001ca´P3õ\x0016Â\x0018Zç\x001d@é\x001e\x0016a\x0003W.½s.ªøy\x0019\\x0013ã Î=Î?órbK¤µ\x0014±Å
£\x00193tÐ¹\x0008Pú\x0008¤õÎ;8ËÔ\x0002$ÎãÅ\x0013\x0019:=]ç#@ç$¢Éüdá°¼&3Éc\x000e:\x0017\x0001J\x001fá¦\x0002ÁÙìY>¼ÄÀâ#¢\x001d5&\x0000(q³4Dâ\x0017XJ\x0016º\x0006Iç$@é%èö<çM
éu°|µ\x00019±\x0000c»\x000e;7:7AO	\ÕåènÏ'V&[Æ\x0014Ç\x000e,v^\x0002^ÂÕ«ª¥Â\¾ßXîÅ
}«­¿C(}\x0004ÕÞ:6ÄÈ]äÓ=L\x000c±\x001b»á`ç&Pé&¨Wnª*\x0017«ÕC1u{®ó\x0012¨ô\x0012h%¨sôì&KÇò\x001eåz\x001f¶ó\x0012¨ô\x0012Ô;4ß÷qªZÎ\x000b+qÀûÇÎI ÒIÌj2³\x000br\x0007\x0003#t\x0005~ÌM`ç&Pé&hÄ#/·\=UÙ#\x0004ã\x0007?lç&Pé&¨"\x0013ãäÄ\x0002õ³ÎkçÌàíÜ\x0004*ÝDñ\Ü\x0019AÓô\x0012»Ø:üËÁµ³°J7Q\x0008¯ÍÀ%e(E\x0011óµ°J/\x0011#yUb²|Ó$c¨¨D}®ó\x0013Vé'¬L°]\x0004ßI®EÜ\x001cÛu¶O6)ýÄ?|í:GaÂz©¿´!\£\x0004ìE&\x000c®]g­Ò\x0016Ó¸>¦+>\x0003$.kWnàcW1ÛY;«´v\x000ek\x0000`$k]ýÿ\x0018ëÓ\x001a(%|¶îbLP*=¥\x001b3'®;°N{`³4\x000f`Ë]Gê9ót}\x0002Vy$\Õ$Ejkï*`q,`wÝpÊ#á¼\x000cÁr×\x0001;ob\x0001aìèº#áG¢Ü!øÞWSlåá=8Fç»Sá§Â\x0003UOtÎÈ«\x0004Èr(ì±óÝ©ðÊSAOÒ³\x001bCzà/ë¤ìÖÇAGá»Sá§Â×\x0017\x001d4Q\x0006$çÇóàÃàí\x000eW\x001eè¥ó\x001a¨ecö(×\x001do\x0006'¾kãå£_TåûÎ6fIDàØÃ`BÖÀ)$¨\x0019Á_K7\x0006ðBJóÈ[@:z÷ñ\x000eú÷Nª!/\x000eòé\x001f\x000f}÷Fû¼¿ä>?\ýüîáÓ§s}rÉÈ°.Ê©ØGê_×þxûÓó4á§üD½r¯o¯~~~{ww¶¡\x000fú'PÂÅÃ¸8Wõ¨ÊsM&.ZÉñÚ×\x001eä$<<ëóÐ´ÔhÅ\x00012oèÅ\x0005Gx]Ëë®/\x0002?¯MÛAbØl.¿\x001f|Ëë®o\x0016\x0015\x0015ÆÕàÌËÈ\x0000þRÀ¡\x0005\x000eG\x00178E~¬\x0001ªç
Q\x0019R0éRÀ±\x0005Gé9n^à:)´\¹\x001cÈ\x0002§íÔò¦¼\x0019e\x0018=	ÛÊËD3Yp tÓ\x0000ç\x00168\x001f]àrÏN|ä¨vv\x0014\x0018D\x00007¾.l\x0000\x0018zqÔgDH\x001c\x000299\x0000.\x0010HuOä\x0011wV\x0018áâl¹*
b\x00161£²Æõ\x001dr\x0017³Ã¡ï®'SA?\x001cÜ\x001b±º¹Å°@òkÊöb;ÙB»\x0001hoXÐ¹ø< eL
~t±¡ w1\x0010ýP{ð\x001f®~}øôááë»3C|­Í2Á
h +Ó\x000b)\x001f;n]}{õëíÝËÛ7Ï\x001fá[Ñ°EC
\x001agÌ·\x0017\x001a¬tmg\x0019r[eñ#¿1z»E{ln`E³-U¡îüm±¸/V§¨³SÝV²fÍ\\x000bætk&s³\x0000çù®\x0013çB´èqÝ\x0015 !ó-W\x0005)
\x0002ô±ó\x0006Öè\x001a´Ð¢\x0005\x0015Zö×ÑRf
:uV\x001bÂ\x001bB-ZT¡Q|O^²:{ÞÃàÙL-WÒpy\¹\x0007Ö\x001aÑúOFäà}Hëv\x0008
ZnÑ²î\x0008\x0018\x001e3Q¾&ò³
®>+G`CñPV\x000b¼fckTË\x0016\x001dÏ=\x0003z  \x0005	#\x0003n¨\x001djØzG ò\x0004.\x001b.Ë\x0007¬å"ÅtÌ&\x0005<Cl'\x0000+ðÅ\x0015À\x001c~;3I©NëVxÝìÆV
[ç
@ç\x000bèî5\x001fQ;\x000f`­´3x·!­®aë¼\x0001¨ÜO§6uË¢\x000bÜ\x000bÛ¥×°uF\x0017TV×Ó\x0004í\x0019
\x0008ú§,\x0013\x001e;ïÝ¿Ö\x00197ÐY·DNØa\x0015MM¢F\x001füFË«\x0002
;\x000b*\x000b\x0012è}\x0016´ÀJà$¯\x001dmcB­³ ¨² jæ¨ÈRÿ\x0016ï6öVak®¬$Uö#åÚ:´.\x001bÅCØÐÑÔ°uö\x0003UöÃ\x0007+gÔÒqU±H\x00017¦\x0000kØ:û*ûQB É9eNgj?Âº­'Q\x0015PúXýÍ28ùT]\x0002¡uA\x001bª¢6\x001fkvË røIÊB
Ûº­³m¨²mÅäKÖ"%V¢Ì^4GOçÕl]äªÐÍ\x0006\x0012\x001fSv-n^lÛÐ!W ÙÎîZÝ
\x001fI\x0002%6»In/4\x0011v\x0008­3»Vgv³©´¸\x0004v¤©:«±ïi;³kuf7H§'x\x0000nö.«&M¨Ñ¹\x0004Ûßàuf¦ÀKð20ªøø ¦m\x000c­³ºVgu£çAjà±ÎÏY¦ûF7t·²Ñµ*£\x001bhNÏüE©6Iøa%jÛ±Õ uñ¤UÅS×\x0011¯Z±q»@f@\x0014G:dtmç\x0010¬Ê!0Ð<\x001b\x001c¹{6º$~>/[Þ\x0010Ò°u\x000eÁª\x001cBÌ=@\x0012nÒWßbÞ\x0010\x001cÑ°u\x000eÁª\x001cBùd4rQæ.A¶²nÑå³\gvÊì\x0006[ã67iÕNh¢|WÐò\x0018ZgÛÊ¶ç«Uv5jó\ù\x00197G1jÐ:\x0003ât\x0006$x®À\x0007Ê!q!Î!Ù¶!wåºSêt§4¦ê®¨bÙ²ÜûJÜ6tJ]w\x0012î$¤úÂëé5»QAÆ8\x0016îúî$xÝIÈE	ÁÓçåÖ\x0000)
1å)}w\x0014¼î(d\x001bX\x001cÁÒÅ+õc9\x0006ß§ÃU\x0007!"Ò
y\x0002Ëfiò<dÆ.ò¾;\x0008^u\x0010"Ô¸-k_M®¦É\x000fm6ì\x0013ÏôÀ\x001a\x0002§£'+.(£qcÖâY¨ÑVÏz¯:¨¢¬\x000c¤\x0019$}2P7ÜÀÊ/4oâ\x001bªnùN÷Üe<Çþô
è6¤èTï
§IIH²ÁÖ\x0004äÉsÍ;ø¡E,;®ÿÆ´\x00055\x001fyt\x000f~ûA÷t\x0005A¹Î ¼iuãr
\x0012\x000fó\x0013¥Ý\x0018\x0006®z×=%D-a²õA°ÄÄ\x0000NrúÞlè8ê\x0008¿<|ê	é\x0007Mf_æ©OO_©8F\x0018N×0hÏ©Y	käÎ\x0003å\x0000Ë\x000b¡\x001b»ó}x² \Ã0
Ã\x000er	[2ç\x000fåM)¤
%ÚïþÓÛ_Uk`:Q)?HiÁ³÷÷ÿþðéáýûsµ\x0019eóKiA¹ R»*W=ÈXª´õe_Üü|{wûâÅB\x0012A³-U¡yäAÖ`¨´`N\x0007{©éÖl½¬*Ð\æThÔ*h+ZJ¨Ì!¨	ê\x001a2ßy\x0015YqºYÈ¬DîÓkª,Ú\x0010YhÉÌ'\x00187Ï);Ín\x001d\x0000\x0005YlÉ¢Ì9'ös²5:\x00135o\x000cvÒ ¥\x0016-é>'ÊeÇ X\x0000Q¦¥
-Q\x0005Ù"ÑBdò¿sÕ WËaï:\x0010B\x0014!¶¸õ¢º-Ùn«%«ÜlµmYqgåNVçµ®>n¶\x001fâ°ö\x0010{m«qKbAòbÜÆ\x000e*\x0002¢\x0016\x0010SAr|^ÑV#·ÖÙAXÂ¾]¡ü ¥z?ß}OÚqoÿ¸ÿðp¶Zd\x0000eÒYºOòèEåh§t?ß¼yAúqO¼yyû¸Ë¯Ø\x0002¢\x0016°Üÿ-mÂÌ2ÀPeR#Ç\x0002Ú\x0016Ðj\x0001#^\x001b^ÁP#¦`Ü"¤8ÊçZ>§åk&i,ù±\x0000¹NT\_½µ¾\x0005ôjÀPÕ;ç(jvµò\x0002a=ðV\x000b\x0018ZÀ \x0005Ì(\x0002_9×\x0007Î`¡\x0002áO\x001c[À¨\x0004t`$h7®¾r\x0006/+haíB´©\x0005LZ@SËÄË·â¾àê\x0019kMl-`n\x0001³z\x0005ARïÆC-Zö¾\x001aéµ\x0018³\x0012p\x0011&;m´hà*ÊÀô°xâìVq°÷$ZWâÀ²:Ôäè,dd\x0017®k´'\x0001­+q¤ÛÊ\x001f9Ë|
ê
ì×oZÂÎÖPÝ`k%Ü:0\x000cäÎVÖXÓ6t¼
£áÆóB\x0018$ÞZ?hh\x0001;S\x0008j[È)p\x001a1Ë¡tä@Ù\x0001£®\x000e:3\x0003j;ImMq%b©£ôËX¿\x001e,«$Äî\x0014£ú\x0014ÛZûAÄÉ\x001aJñõë2\x0006-awHP}H¬\x0013B0õQ-Hy
£v&agg\x0012ª
]\x000e	)p1 YÉ¨éïMsX(×\x0012W¶¢oé¡R¼r¨²éë¹­êÐúÓê9m2Ô«#Àë	ÒÈëê\x0015õ\x0015å\x0014\x0013\x000f`f\x0010uÄì\x0016÷²¤\x00007Æª÷)gY\x0003ß=I\x001fIQ¬¤A¸Ö­Óä{9óIû\x0018ýÐKÿòÇßþúðéþl?I\x0010\x0006NÌ\x0013k ô\x001c9\x001eÑÀøåÇ?ÿt{ws®Ë_\x0010±ED5"d)È,ÆQzBBbâ'\x001f\x0011ÂP Ú\x0016Ñª\x0011iHÑ¼\x0016ëkD´î\x0011å?\x0005kñ\x001a/Ô7(fÖM*\x001fYÂEç\x001eÓuT ú\x0016Ñk\x0011y"ìÜ1È\x0012æGDv\x0014¡%\x000cêE\x0005ËI±µ5É²\x0018F9)î\x0011½\x000e\x0005bl\x0011£z\x00111,mz¯!\x0019Éyó>¶\x00021µI½&1Nå&íäÝPü \x000b(\x0008sKÕF4¡\x001cáë ºZ8L¸ÜO³9\x0019ßgnEË*j´=kÈU|LlTÁØû\x0015½c)w~e/Ë8b×'Ë\x001eàQ v~\x0005ÔÅ£r6´\x0012óq©ÀiØæ@çW@íXB\x001dà\x0007¤ÇÇÒ\x0015\x0006¥.6\x00187l¹¡s. ö.4_:p«³,h\x0003	¤ÇßÔÇ\x001ebì¼\x000b¨ÝK4µ\x0016ÕF\x0016úvu\x0011aÜrCç\@í]¨f±ú¿,\x0011mª\x001fÚ¨;\x001cbì¼\x000b¨ÝKþë"&	#hÆWm}L/MÁØ¹\x0017Pû\x0017?·§Ï.Pªß Õô§§8£\x0001µYÃ¤à jÌri
ö±á$û\x0019±s1¨v1T\x000b*"	Á×uô|òj¨+\x0018;\x0017j\x0017\x0013S­Fä÷4ú³4jù4|d°¿ºè]\x000c§\x0018KÐP\x001bx#T	Ç\x0006\x000b)\x0000;\x0007j\x0007fÍr(\x0016¦ÊöÔÒßGÅ£\x0015|sA½sÉsIG|BÊµ±\x001d\x001f\x0013\x0007W0vÎ\x0005ÕÎ%}¤ s£\x0003b\x000cÒ_öè\x000c\x000e\x0005cç_Pí_B9!\x0012HÐp]n+°R6ê]\x0018gìü\x000bªýK¶KUuq5óÓ\x0015R\x0012×Ñ?¦´ª`ìü\x000bªýK°2X
,@]Ge\x001dýx@AµÉ)Ê·¦fÖy;:\x001bL2MÛh;÷bÕîD¸ÂÕ"È\x0003VqDw!<6\x0018FÁØ¹\x0017«¿Áüã/¶s/Ví^¢±TÙ:+¹dÊ4ÎmK\x0019÷¶3àVmÀC±Ú\x001cë¸p¤¢^ÞË}zL\x0001XØÙF«¶\x0011\x0017\x0011\x0008|\x000f¤\x0001\x0012HÀø*vfÇªÍ\x000eÍ*\x0010³ëÀ\x0012âJ£°\x001d¿ñ»îL;õ9Éu=¹:OA®\x0007Þ
j×\x001d\x0018§>0	'q¹\x0005\x00168+hDï%<:ÌKÁØ'kÕ'&Qs3·éÚ$BòÖH¾;ÄÇ&ð)\x0018»#ãÔG&e¨½Þð{\x0016bgü8cwfúÌdË­ Nhk¢±¬áðöÝñê\x0003ä+¡Ê|\x0006S[yÂð"úîÀxõÉjäÍHJkó:º8$\x000bÝ:\x0006í::S\x0018]Ú\x0004gFïSg8$\x000b],\x0011¾ÇX"t_:h¿t15u7&lçÝåÄ$ºZ\x000f3v¦1hM£\x0003¨5Ò\x0001´»ûr\x001dþ¼K\x0004<íÃ/\x0007=½nú¾ \x0002dSÚât¸u5TýËñ\x00177ô§ è\x000f3g)èÖÅ3\x001aÊe[Úôýx¦§\x0017ÍµYJy\Ïjicûái[Ü±·êÕ¢\x001e!-~[Y\x0003Jöôò\x0014Æ-»ÉùÒ?t}ùþR¼ï!ïÕqÏã\x0012'eCsÃ(\x0017n;îºnCþèôr9iÂnª/^·gÈòÑqüQÎÿåíÉCÈÛ\x0003/!ï:¾t©"\x0017y\x000b±feAÍC\x0014\x0012ð\x001c/°&Ôî¨Ú'ìÇRÐ«/\x000f\x0007>=M à{¸7ýhàH
Æ®ÿôèÔ>{.?w\x0006ÉöB¶é)ý°úôáÀ§wÆf©êó	jÔ$£Ì\x0005Üg\Yúx`NIËÅ}bZ'-Ç¿=¬POG¹ì:úÞ\x0012{±«uÞÁ:þ&_¶éo'Ûô7í6±ÌIâ\x0011ÈP#'Ìã\x0015i¹§ÌjH\x001fª¸¢5VºõKzq[ão¡«¨	M>Tõ\x0019$m­*¶(¥\x0018y¼æ\x0006V;\x0014ìPÚb©O\x001blU(Ã /£æ\x0002¥\x0004y\x001c&[\x0015pK°Çº[Q\x0014\x001aÂøk}¹üÇ×û\x0013ïT¬
ÿøÝeaÁö¡^ùRÚX/DMø­/''INxlJ±jU×KzÄá\x0003õGÎ¥CÀøÅá¥tè8*VöÂ2\x0018âÉû_ÎÆ »üMöÃ$\x0001	kË'/^ýòm\x0012lIp\x001fI¹ª'\x0006ñR[UE\x0010U½û>\x0014Û¢Ø}(ÎÉ¬ºi\¢\x001agY\x0017·V\x0018Ø\x0007ãZ\x0018·ó\x000bEn3%­-Iæ\x0002¬õúö¡ø\x0016ÅïCÉÒ*h"=k²@­[6Ö\x001e\ÐÂ}0VÔPÊGJ·r¹$ÙèÝ\x0007\x0013[¸se¢ô\x0017ì¥ï%ÊÄ¨s<\x0008Z´\x000fÆ#ËvÏ$bc\x0010Q:Õ\x000cÝ\x000fÁä\x0016&ï)w.\x0016ë0$ÅMìÉðg*+³j¼ØÅ²ÄB3á[+C
ëlí`zóK²åÆM-ÇhzÓ»Ïö´ßì\x0013LUµ)y'×Â\x0017û`:ë\x000b;Íok¡\x0011b¬b]ül\x001aXpí£é\x000c0ì³À\x001a÷y×D+#wDæ8ä¸Ö³Ú\x0007Ó\x0019`Øi©±Ïñu×T«gVúûX:£\x0007;­^Î³¤!ÈÈ)É¸íÖbû`:;\x0003û\x000c§"h¦¡)å\¯fÙ5\x0015\x001a<ö°;Ü¸ïp{'¯òÆ|l\x0012!Ô°nÛÇÒÇ2ûN/7çÊ&¼|&,{\x0008¦Û¿¸oÿúàøe¡\x0004tËÌèå3Åc{\x0006»
û60É_Ñ\x000bue²(&µ ìÎ½\Ðùhÿ¶ï<9®\x0002Íèáy.©âäõ<!p{kN2ï\x001bL¶|¤Ä^:Í9,7w3~=Óh§Å9e°\x0017Ê6Ç~!\x001a\x001e\x000cI\x0004·Ëw[7Îîýr÷'_î~×KH:îó3µG/T\x0014W\x001c³=}[ì|iØ¹F¤öÍj)±\!8q\x0012­¼}\x001b·î ?ÏTNK³+?,#ÿ>_ýëý§ßß}øL·Ð\x001fî?¿/(ç¤F\x0006U\x0018Úb³¹F¸4¶ÜµÖB\x001aÏn__ýëÍÝ³ç/_Óeô×ô}\x001b\x0018[`<
ìE4ÒØyFïôz+37CØ\x0012Í=Æk[^{\x0014\x0004fÜY\x0006=ÔÅ5ëøé(¬kaÝáÅõ\x001cIÐcÉ|÷Ç\x0012òÒnèæ\x001cÅõ-®?k\x0018Eª\SÑ\x001e¹=,´vïGyCË\x001b\x000e/oäå¥)³°#zÑÙ\x000fÁmu8Æ\x001b[Þx\x0017\x001a^®!+!\x0015VÞíÔò¦£¼\x0001D:\x000b#Ô\x0005\x0016¹Ö\x0012[lË\x001d\x0003Î-p\x001e8o\x001c\x0012b±¾N¬¬0Kíån<¹\x000bsx¥x¦pZ\x000eÕÊ\x0012óp^\x001d!î\x001dÜa\x000f\x0017E Å \x0015\x001eô\x001bTÏ[\x0003\x0011w\x001e\x000eº8©ýÞÆFêt\x0003æº+¶¦Ë\x001e#î|\x001c\x001cvrIÚÚË\x001a'yºöRÉYÖøb\x0018:G\x0007G=\x001d\M\x0005ÙâÌk,»bRU¹\x0010qçëà°³£[>¯±r ,çMNY'Z\x0012wÞ\x000eº;0ÕºQ\x000b[·\x0000,\B"T\x0017#îü\x001d\x001cux\x0000N¢a\x0010gb]ÖxK3ý\x0018qçñà¨Ëúdh\x000c/×·]á%\x0006²«+ØQâÎåÁQGrù\x001dcq ²Äà\x000c°Öü:\x0008ËÃÃ./Fî(+ñ¦á9aÅðÓwë\x000bÜQàÎãáQ\x0007h#ÌQÈK%N®F\x0015ÚÅØßéF.uü¸FOËØEñxyk\x0016Û1âÎãáQG"²5NÉRÔÐøRA\x0005vî\x0003º\x000f\x0000[
\x001aîl%¨\x0010÷á·d«\x0011wÆ\x0018\x000f\x001bcì>"\x0017?\x0007´b(âÖLöcÀeÃÃÍDV+)¶ØÕ=!-Þ\x001aÄxØvÂ\x001e¶\x0014Æ²p±¾NÌ+&¸6¸m³}6åð¹3ÒJ2å«¸½w"¬\x0013×G»g\x000f\x001f<#\x0015¨ñ¸Ý \x0000°[\x0003:\x0001wçÎ\x001e\x000fX]Éà å=!]!ºt±\x0015îÎ=|&\x0007ÍÞ#8ñw^ê¨ÈP\ØuçÎ\x001d¾\x0006Ñ^2T¢æ¥×¨nb\x0018\x0006¶xtµØ$]¯}üzÿõ¯\x001f?\x00071\óg7¢\x0004Fc49î7GÞ>{õææÍO¯^Ia\x000bká\x000e.&j/à¬¯oÓ5×ÝVà«\x000b-\PÁ"¬\x001cTÑâbù\x0003g4[s\x0014p©Kº+÷]Î \x0007°µIæË\x0014¸µ~»
nI5\x0011ÜjÚ¹é¬xýà¼h\x0018Å(qJö\x0003vÐ;­sÍ»ÉÕÓ?î?}ùôp®`\x000f½¨ìêpNÔûpC·½°=ýñæî»ÛsÅzî´.Í5/\x000e{Ñø\x001e\x000b\x000bÏu2&\x0015a+\x0001£ s-S\x0005H9Û gÁy)ÃÇ­ëÌ·d^·f<ÊäYð¿¦\x000cÁ¸u\x000eö,h×ÌÉFsRêâ¼<\x001aâPÅ,êÖÌÖÙ
t·# \x001fÓn]-\x0015d©%KÚ5ã\x001cd±\x0011Òãå¼\x0005"Ú±EË-ZV/\x0008"×Ê¥²Óäsº­0{?ZS÷æ:»sÙ@Æ¡øjÓêL/´[ù\x0018\x0005[onög\x0005rý¢®\x000e\x001aÙ\x001el¿\x001f
;4Ô-4\x0019O\x001aÅM9/ºa¸?V°u®\x0000¾À\x0014Iùd8³uÌF	·­s\x0006 ó\x0006>Kd²nb@üV¬®`ëÜ\x0001èü+Qªû
x¿ÙT÷ÛV-­s\x0008 ó\x00084+S&² 7_ÐØñúMÇÐ:\x0000:à¢ôü\x0017K´l7ù¢Ñ\x000f¹\x0004è\\x0002è|\x0002Ý\x000ceÐ«.>ÖY^fðv>\x0001tNÁYz`­ÎØ©ÂÌ\x0001ÁÎ' Î'\x001fë6Ò:O t\x0019dd\x0003ù+ì|\x0002ê|KÒÝEÇïÝæê'\x001dr
Ø9\x0005T9\x0005*I2l¥\x001a7\x000fu`ÝÊ
+Ø:§:§0Ï§×­ö¯,~¾°\x000fùyì\x000c/*\x0003q[iHÕ8#ß\x0014·z
¶Îð¢ÊðR\x0019ò7M\x001fØÀ[u+ÿ3ÄÖY^ÔY^*
åoêkÝ¬\x000br±°.TU±u¦\x0017U¦·ÀU¶\57}m«°\x001eÆÎigzQgzËá´ËG	Bâ2ðesðôn6ÛÙ^«²½4bW¦rey\x0006_µ\x0015¬\x001f\x000b,mgß¬Î¾Y/MÀ·Ìæ¡~Óu¥¶­Ïèì[Ì"ô@>+ý©VlÈV:p?ZgÞ¬Î¼ÑÀDþ¤4{£ä/dÞlgB¬Îd¹(fMÁ®^ØìºdZÅÖ\x001dS«;¦Ån\x0000Ò\x001cdXËÕ¼y;\x0014¸.\x000cqª0Ä$Rëä\x0016Øz¨ó¦]\x0018Úo®;
Nu\x0014h­]L/§\x001b<¢­¦w­;\x000bNu\x0016,ä\x001a"åÄb£­Îÿõ~è,¸î,8ÕY°$\x0000ÎRF\x0006ä,Pï°­;tTlÝYpª³Pâ^q§å¿®\x0005­zÍ²÷ýh¾Ûn^·Ý¬©hX/2¾æQOäÔÔh}W·Ûl\x001dÎ\x00014ºO\x000b²liìþç»Ýæu»4©xR1%@
VNi\x001c\x000b,}·Û¼n·\x0015\x0002Oê®9æ­3\x001aH¥u\x0004-t7è\x000c/\x0015 s\x000câ Þ±² å±lCè\x000eBÐ\x001d\x0004Ê6°ý(á¸tÓáõ\x001cÌ\x0018íÛÇæðMÚö®\x001eÖI¹ªcø´Ì³\O¥Õ¥¸\x0016)Nr½ý~²\­ÚÝÄÿ¢L\x000f\x0006\x001eÌí'6N«Ö÷¢±Ïæôó¢Ñ~^SE¨·á
Ò®¨\x0004`ìIË÷×ë¾®s(á\x001cJ+³P'¯\x000f¹×²÷~?Ù{¿G{Ï7Í¨ÓÒýv05íÍup«½\x0007£çöËÉÚ©F\x000c×2©¹\x0000<&n\x000fÌÌó¿<à=|G6÷§"kO\x0005?#%±ÇKA\x001b{©)&¥\x0011*bB¿|?9MH§V¯ü¿ÐY=Ú}\x001f \Þh²vÚCáÏ§>k
3½âsÐbë"8Éa,\x0003àW×.bJ2#ÇDjûHhÔnV,iNðo''XeÿþáÆùKoUÖ\x000fãµÞM\x0014õ\x0002*Ö\x0018Ú~6®>nTÜ(ú·&×í¤/ÆÙµ¬òëÞ|Ýûïèëæ~ïeÝÖ+þ\x0016øQØ\\x001b±ÐÇF7f\ìÊ¸Xµq¡^m>¹È]Ûd¡CMáý¸÷Þ>üû
Ïj9\x001bÚj¹÷ÿçýïÛ{ÿîóÃ¹¥3Fµ\x0013¥'0Ë­¢\x00116\x001f\x0000^\ÝþðâùëÛÇ\x0017NÈ°%C\x001d\x0019M0s\x0016&9+eL6Ê$+ÀÍýp¶³Z8éÂO¶V\x0019Ú(ö\x00046«\x0015l®esZ¶ÌyÏ²pYf.Y)\x001e-\x000b·Õªó-×ÂÙËå£Î·\x001f\x001bäö\x0003f­¢b\x000b-[P²\x0015ÿÊZ\x0005Éáõ¬\x0005Qà@Ö
ÇNClÙ¢ÍKtT\x0017Î<:µ¶¡
.µpI¿pV\x0015±¸ò\x0017U32vRsËµl }k	jÍ¡õU,3oæ\x0017wÃ5Ô¡+ìÛIW\x0005Ó\x00126UÞ\x0001J,0´ç ÷
Jç@Ó\x0002<o:ã®\x0019Î±\x0018F4i3Ù¾\x001f®³À 5ÁÅð2\ôIäÝ°ª-¹­Îe\x0005\gAkc2ô´Ì½³NÄçæ­Ðu6\x0018´F\x0018d¸¡ÎHe$\x0006àÄÁM×\x0019aÐZáè¤\x000b2AU§³N\x000eìïÎ\x0006Ö\x0008\x001b\x0010ÏJ39Cé%­ ±=×\x0019aÐZá`ë3ÒS\x000cô´-nK\x001bHA×aPÚaÒàã\x001arÇD+--'êäZ:ìì0jí0Éþ°&jf×/ß5ÅÁØÇÁÚ@x~zuå\½0\x0015v0ûáºÓÚÓÚÈ\x001c \x000fÙD\x001fßø-±\x0019\x0005]w$P{$þ±Kg»=gµ{\x000e\+\x0017X/VXÞ²M[	ãýtÝ®³Ê]GZ&"¦mkq\x0018:îí4:j®ó¯Vé_
e³ç\x000bXù¢LzòbMî_¶;\x0013Vy&L}ÁÔ^gý\x000c(WÆ*Ü¹\x0016OVÑugÂ*ÏD¹a}\x000b¬Ñ;Æ\x0004Hn3\x0015¶\x001bÎugÂ)ÏYÞB1Éó¼IX»27ßïöÃuGÂiå9ôS;+'$À{igµc÷C×m:§ÝtPODU\x0019&:[>ÍØ¦sÝ¦sÚMgDbÑSZg>®Ü\x000c)\x0019bßm:¯ÝtÆÊð©¶?B\x0015AJi3õº®Ûu^·ë0g/KW+«\x0000SáâØyõÝ®óº]e\x0013<µ¨ÍvÎdù¨Á\x000fÅê¾Ûq^·ã
\x0019Î3F÷õc¤?"$?v=\x000cÝ\x000bº\x001dÔ&;ÎY	7MâëaHnì°nÇ\x0005í KgÔtÈQSHv³\x0016v?\çùÎóãÔlËt\x0014ÝÍçÁ8Ã[Ú\x0017¤DìçÄDìßH\x001b¹	¸Lr¢]Ê\x0001\x0016t"ë\x000c+¤1âkÓPÖ®\x000eÈ\x0001²T\x000b\x001d\x0007ðQòcX¾}½^}í¸úÚQÿµû´\mÛ´ÀÐ\x001d(à)d@-$æPç®Ðü:¾¨Ñd\x00049ÕcO\x0016v\x0005iÕj¡¹õ4bâ(´Ò!@upG ïËîÊnè
}øüî÷\x000fog'\x001f?ÿÇ×/çGWeIYJØN²0F¦y`w·¯?»}ùôvÒyòêõÿxsûËã\x000f\x0015\x0013[L<Y\x000c\x0010+:XjøäázÒj\x0011?Ñ\x0005>\x0008j[P{\x0004ÔÕ÷Ç\x0012ÂÊ¤)\x0019Ä*m'=o\x0007A]\x000bêb\x0016]\x001c$çÂsð:8¼\x0008§o9ý¡/i8å¬zg¥\x0001(§ªLk/\x0019ZÌph9cUN om9VýÃt\x0014[Îxh9ÌJÁ\x0010äZe\x00129ia¦K¦\x00164\x001d\x0002åÉfR&ásª,*¤W\x000fræ3\x001f<ð?¼7òV3ÈA2'b3Ç@ë³ÜléÍ¡\x0015õ2c\x000f]\x001d\x000ek¢Ä¾\x001c\x001e$í}Ò!§äÝµç5-çõà(©Ã¤Ø¢Ð9%8æ
\x001cë|\x0017çY7©¨út2é içà[*Q»'pü~4ICºÿÎ-Á!¿TÖT@k#Y±OQ@/\x0012@çàc¢ç©\x0019j\x0002GN=;m*;ÈÙ9&8äÈ@ñ±§\x00163^ÑlÝEA;Ï\x0004\\x0013	Î§	Rä÷r\x0013ïÝ%"\x0012è<\x0013\x001crMh$5I»âë8û©Sÿ\x0002¤oCÎÉ{z7H³\x0013\x001di#Í\x0019å?¾\x0017ÅÎ9á!çä¬<XB¹¼óÜÕ£º4bô§	ï]m¡k\x000be|îÃÕû¯oÏ]æHa\x0011kc_âqXµw.õY${{õäöæÍÓ3\x0017NAÃ\x0016
uh4hNºäyª3\x0004S»HCßÀ¯g³-U±¹*[=­L÷õµK>õc@õp®s:8cy,(åÇ¥?hºüpÛaÖÃù\x0016ÎëàPæÿ\x0002`m­ZÖm{Rû~´Ð¢\x0005\x001dZ¬³Ù§Uí*Ú4QØbË\x0016ulV\x001eÉ^óW-KCZrcã÷³¥-©Ø(ÅËË¼(m$SÛF\\x001aü¦¹eËÊuK|?\x000e*ç&CJµsyì(,+\x000b5\x000bWn,V*Î«^O*\x000b*+gÇ¾*ôAç\x001ahÔ1ÓA	\x000edâ-\x0017G®ó
 s\x000e¾fJ'½
\x0019b»x.Æ\x000c0tÞ\x0001tî\x00063/ú.2I6Wm­àÆ\\x0017tÞ\x0001tîÁ7\x001dJ¡¾ó¦\ííköõt{\x0000(ÿ]Uðr\x0016zþ¨Ú8k×y\x0008Ð¹`B\x0004	 k¡¶wavct\x0000ð\x0011ªÞ\*
¦µ[ô¼\x0019³ÄÐy	Ð¹	JÎ²)¦ymÓÝ®ú0\x001côaÐù	Ð9
mÝwÉð­¢,ûÎù±P\x0018;O:O\x0011ÜÒîe\x0019äXa4c§\x0002;O:OAòçm±äaÊ'J¼éÌ§Àþ\x0016¡ó\x0014!ÄªÌä\x001c\x000f·
nå÷cÖ\x000e;G:GAO@¢RFV¾ôPÝX\x0018³'Øy
Ôy
*\x0016åÀ\x000eLJ\x0003\x001bDg ã \ç(Pç(HÕ¯`&ÔÀ9Â¢¸5¸ë:G:G\x0011TfNb®sÜ ó\x001d#¦8x`;G:GQ.ª­0id\x0013kÍ ±ë\x001c\x0005ê\x001cE2¹bãd6fñ\x0014U\x0005\x0001\x0007lç(Pç(B` q[<8f	V76\x0004g;Klu¸øz)\x0008Îå
;\x0005!ÆÈ~\x0002c\x001e\x0000lg­Î\x0014S÷TCÇ\x0006\x0005Q®\x0014\x0018ÓØµ}JGgSÒÓ³¨¢ª¿l\x0007®3ÅVg\x0007¨çÉ\x001eÓÒy\x0012.tÛ®³ÅVgs	yb\x0017)~ËÒaæî\x0019czºÎ\x0016[-NäY¥õ<É\#¬g"\x000cÞ(lg­Î\x0014ø·\x0015À¥µÑ&\x0011@Ä0\x0018<ÙÎ\x0014[¥)ÎF\x001e\x0003©VGZ©ìÂà\x0006w]g­Ê\x0012;ÓÀYRWi2.\x001fv,\x0007àºÝéBöLÕÔP?,ïºâY±~Ø±mç:GáTâ°v£p:G)U'BROhCu\x0014$·=D×§×u¶8û°Ìn©£Wé$Å`\x0012ÀtZ\x0016sÒ~Ð$ï\x001cO´$¹¡:*ÜX.\x001bà\x0014\x0011@ÉøÏØ
ïÂ{m\x0006).¡ÊL\x001e9hcµÍ\x001e\x0006/@xºÚ/\x001dí¢\x0004k¼ÔT\x0008h\x0019\x0006ßðb¿Q·®D.I2ð®I3r$C9øTvºN}ZÀ.OYú7Ê-I®á!\x001d<.Î»¿tO´Jjúû«\x001f>Ý(úÓÇ\x000f_îß}8[xUé´\nY\x0006\x0006PRÞ¿å¸»yYþô§W/¹yþr\x0007«mYíAVYà Ö­SJw
\x00166Ûu\x000eàº\x0016×\x001dÄµUeßØåTGÍ¡WGp}ë®®mÀ=akO\x000f\x001fùà¶Û>\x000fÐ6\x001c¥Íä¢×ßÚº©â^j/Ä\x00167\x001eÂÅD%¤³Á
N$ÉM¹\x001drÐì¦jï\x0011ÜÔâ¦£«\x000b2ÈÅÑ\@î)4\x0012£ínÌ\x0003´¹¥ÍÇ\x00167SµÖL\x001b@f;ìD÷(¹ÐAÎÁ1;öOä5äï|ØÞ\x001eÛ\x000fN\x0006ý`Xsz,X¶ôfÃ\x0002¸Äm½O+?O{òðéÃý§ß¯|üúéý»Y3óÑÉ(ÑUµI\x000cL\x0002éqv«~Ó'·w/oî]=yõæîÅóÛ»oCb\x000bzÈ\x0014eêtG<Ì¦ÖI#vZpÒCÚ\x0016Òê!mS£ñ"*BÓ^¥Ñ~-d£t-¤ÓCF'Õº^\x0013¸µI»¦\x0003Ã¾eô\x0007\x0016ÒÈÉXVD^H/j\x000ff­#«\x000c-dÐCzÃ\x0001R SçÄM=êÃ±ezF¬ê
åDÕh\x0013¤qµGl=áW\x000fZÈtàkgn¡%F\x000e¢0ºK"æ\x00161ë\x0011s\x0017ý¬\x0012òÏí
¦V\x0017È¸êÿTC65LiQGÓP:k:z\x001eªA:ÌÒZiÝÊåè!{o£w7©oîi.òx
\x0012P\x0017Èµ´\x001e²ó6 w7)%àFñ\x0019}mRÝ\x0018Æ®ì¼
èÝMJUÃ*zdaÍB)úóÆºq+	»\x0001½¿IÑ×¥,áá£cs\x0015=ZK½ë);\x0003zHs[Ö2òË©µXp!;\x0003zC7"ùà*Û&F¹¾\x0019¿\x0003Õ3v¶\x001côÆ<Ñ\x0000:>ÞeFÞà¤	=¬\x0007pé);s\x000ez{ÞRFäêg¢ÌuS;\x001dìì9êí9)Ò÷NR\x0008m²\x0011\x0001XÒ$\x001a§ì\x000c:\x001e0è\x0016x\x001cÜD9¿&\x0014sýâk\x0019B=e8`ÑI@L4a\x001d½N¾)Ç½Øt<`ÒÑÈ5'fî7)Ôm\x0019×ÃËõEÇ\x0003\x0016Ý¸E\x0015ÄV&Weì²\x001f÷ØYt<`Ñ\x0001«@q|ðzxb\x001e7ØtÔôrJ\x0016íÓÈ
,¤-âØt\x001a¦ìn\x0011¨¿F$RdµL\Y¾¸L|,À\x0017øâëA½ëÉUJ\x001bjÂ\x0010\Õ]\x000bgé);×\x0007\1×åÐIcOÌ\x0006(sÜ¦ÛÎóX½ç¡ð"²HµC~Z-µ\x000bÄl¶s<Vïxb6\x001d2×Ï\x000e
d	2Ç¸í\x001cÕ;\x001e«dQä3·å[ÜÊ`ýF ì\x0013Wz¿\x0013cêëéIÇº\x001eñóm;¿cõ~'Ú*Bª+ée¬ö¤ß7LÙù\x001d«÷;1à2QÀÈÑµ\x001eßÆ);nõ\x0016=b
-S
e\x0014µRØ£Ï¸@;ªiÎLË¤&U
E¡%¤Xó¾4GjN©Æ\x000b$^L7³iNb\x001a*jú××ù¾%\x0011{äÌ\x0005ò/ù\x0015ò\x0011Øde8,Ù¢zâõ\x0014Øµã¬ÿ),\x001eZØ$ã;'\x0001[é¡×W¿@ò\x001fV\x000b{Ô
Y5äªóDK1¯ç(\x001fÈf¢\x001eÛ\x0002©ÊsE´5©ésÍ²§\x000bX*sÊÚ(Û©<T®³wÍ\x001cÎ\x001béX\x0006{41\x001a-<d´þ\x0019ûµQÅù¤û#¹XYA5A ; Þ>ÖªÚûAÑ<ý\x001fê`£¯WOÿxøë»\x000fW¿>|úrÖQqµµá'²W¸ÒhÖoêo®þxûÓóW¿ÞÞýòm8ÛÂY%'_?õbû9µé«ûBÆYJ>×ò9íâÑ\x001c\x001aÃ´'%ôÜõ¥äó-×®[T5Ë½3	¾Ê¬³Ç\x0001C\x000b\x0018â\x001eÖ\x0003Â\x0017ß\x0000b"ÁlTø(\x0001c\x000b\x0018µ+XbbÏâ¸JÝ¸K<Ç"?¬Åq©\x0005LÚ\x0015Äå4òÌ4B­â®\x001bTu|Ë³\x0019ñÕ¡B»\x0001M\x0008ägç'Rãc\x001d,°1AZ	Ø\x0019@ÐZ@ªwÈ²\x0007'½i\x000f&\x0019\x0011^ôè'ÎÊÖÌ\x0019\x0004ÇAúÔ¨0-!\x000f£gØ\x000c6În>Ç÷ÊE,·p4d\x0015«½$4âÑE\x0004\x001aKÛÖáÐ\x000fRókù\x001f>!³ÖÁ2H-2¯\x001d`qEöëóOo_î@Â\x0016	÷#:UhîP¢­\x0017íõP¼ÝH¶E²»|N\x0004z\x0005KsÙ¯ÀÆme7oün¢°|·è¤Éßçzöë¿ÝHí]·ÄÌÿÍ;ª½Ö3DÈ{¾¢ËQ\x0005µç¯(¥Ó\x001b#¡¾\x0005fJ´Õ>úANßÓ÷÷_¸zöðÛ×Ïÿv.\x0010&Å\x0006j\x0010¹î¸\x0004ì27 ­çÞ=}qóæ\x0019Õì=yóúõ¿Í-\x001fjùHXÜ<°Y9"±RZ­\x0016Ð¶V\x000bX¾,¿òû\³\x0019Dÿ3å°ÊÓh\x0001]\x000bèÊÉù^N3y3§Ý±NÕX{Q- o\x0001½v\x0005±N"
Æ³XII¤\x0014³Ykk\x0001C\x000b\x0018´+H³æØË\x0003H¹I2²\x0007³Y°Ð\x0002Æ\x00160\x001e8$Ü_\x001aÊ\x001f\x001d?Zx\x001eÕG+'¡\x0005L-`Ò® É)&æ0.&+Ë·ÑÚ ¥Ë-]V\x0010/\x0013{ª..=¤ÉþÃõe[É×Dêd£\x0016Ðfé½\x000eUC¬\x0004í2C%#Ú\x0018è½ÖPGHu
ÙÈÄªÔq\x0001Ö\x0012v~\x0004´f.pFT1ù½9Ú,ìºDYKØ9\x0012Ðz8çóW®X1Öä\x0019®Gmh	;O\x0002ZW\x0012io$}Ì¥$TÅ\x001b\x0003K´+\x0001­/):}Ú\x0010¸ë«êKÜº[BKØù\x0012Ð:\x0013õÆÆ&ÄëìøN\x001bÅTûõ­[\x000bØù\x0012Ð:Uz=$\x0011W´u	×m~ZÀÎÖÐ<:Ñt\6MO\x000eu2ÝzÆµ\x0016°s' õ'4¹T"\x0006ËÁ¾)§¾0­K[Ø9\x0014Ô:\x0010¼zÏûq\x00022X*Çá%ÄÎ ÚTG¼Ï\x001dx\x0013sgÏ´ý½DëOhÝòòÔÁÕ,å K[Îzü\x0016°s'¨v'ÆI4Æ O\x001cT±T+=°s'¨v')Õª^!C^BÉmPP2\x0008Øy\x0013Ôz©áJæJy\x001e;S\x000e²©»p]Ò»ð¾\ºÛû
Ý¢èüý¿ªÈ÷×«>~}ÿîÃÕßÿ«_Ï'\x0018èÉUT=p N7	Õ\x0001<&Hÿæê§Wo^<yusõë¹CEÆ\x0016\x0019#ÛèÜC\x000cÎp;V\x0006ÃÉ]g\x001e\x0015QW\x0003Û\x0016Ø\x001e\x0007Î%Lu²<º\x0010Ç\x0011»Ø\x001d'¶UPY\x0007¶xð$È'íd\x0003È¾Eö#Í§DÛÄÈ]§läGgj¨C\x001c¯²÷"È\x0006®ª#
×P\x0013Ç8\x001e_d¬
¼@\x0005e¼È©\x001e¾Ç½\x0001âÔ\x0012§ãk\¢\x0000+"\x001eAt è!CD<.F[â||Ë-\x0015S!Æ¹
\x001a®xg/vôÚ)F~Î.\x001c\äYlkRJ\x0001v"XR\x001e\x001d\x000b¦FîÝÞq¿G\x0017¾ù!\x001d\x0010xS$Ù\x0014¤ûv)àÎéÁ×#UÄÅX}s¸XKídèü\x001e\x001cw|±ª£sÜ3DÉZ±\x0016Ù_l;Ç\x0007Ç=\x001f!ç%\x001eÂ\5\nkt\x000f»>ªód«\þ\x0015CC°dkdxl¹s}pÜ÷QS°ã(.@\x001dØ$ãÏ'mçÎùÁqï\x0017¨åqfFëÂ{Ã$\x0003^l;÷\x0007Çý\x001fu\x000c#û¿(\x0005M$\x0000+gð´{x¹spÜ\x0003¨\x0006\x000bÃ@ÊuoÐæÝ£C²´ÌØ¹@<î\x0002©é\x00199f9Ò<ålºÝÀþ\x001euÜ¥$|.¶ÎðûT9w¢µçÀ^*\x0000ÅÎ>ã}¦vÙÏÀïÎX"~	óO«Z\x0007;[\x0003¶®q<{\x0001¨­Ú:ç.u\x0006±³\x001b8`7¼ÉA¹÷Q#èÄ\x000cõrâ/fëlw\x0006íÀ\x0019,¶÷3Lfo¶uÒHâ¿Ô~¶Ý\x0019´ÇÏ =Ñ\x0001ÇH¸ÌËRfåâÅ®­¶;và\x000câ\x0012lHP\x0017S
êðbÀÝ\x0001´\x0003\x0007\x0010²¨$ÒTØÈ\x001cä\x0000zs1£a»\x0003h\x0007\x000e ©3ÐókE	÷y\x0002_A~tìª\x0016ÙuçÏ\\x0003Ätèq\x0019Â)ñ¾7x)¿íºóç\x0006®UQö²\x0014	!uKÉ^¾Ô½Õõ¹Ì\x001cÍâ{+J\x00018N
3rztÀ±¹;~n Ï\x0015dÊu¹k"Öid/\x0015\x001b¹îø¹¼Q°Uü5Ûf´Ü\x0003ËåõBÌ¾;~àüùÌ\x001a\x001dSæH&¡&_cPw©óç»óç\x0007Î75Î\x0008Eÿ²Ô.k ½Ø2wGÐ\x000f\x001cA\x001aÂÙ®\x00109Û\x0005å-!(^,óÝ\x0011ô\x0003GÐ8:\x00074sFÆÕ+Õå®Û¾;~à\x0008\x001aCEUsÆKf3@6±f¼Ò¥Ö9tG0\x001c?T\x000b\x001bk¶ËuSä­Íáb\x0011h+\x001e-\x0011ÝTò|4¨\x000b×Ö±/g_R\x001c\x0013ÇãÅ.°æ\x0014\x001dÍ\x0010z¨>&³Ê\x0010\x000cTÊ\x00173"\x0016W«Cès^tvQÆÞZòA³ª\x0006Ñ÷'µå\x0007©uüñáýÃ\x0007ê||ûÇ¹ÆGKMú"%E
\x0008'\x0001¹\x0010=áêÑýÇÛ\x0017·/o©ïñéçÚ\x001e\x0019p)á"@)áÚMH3z¸*¦ºD\x001eB\x001d3!9\x0018#\ê\x0016Pê\x0016ö\x0013;5«
Æ\x001b\x000fÀ iÅ¬j?´Ý\x001a¢z
-H±c6u|E	40åU\x0005pQZ!BQZÙOXoÙcI:í\x0010ÒZUK\x0008\x001d!h	ip*å\x000cõ¤TåK\x001a0<J\x001d!jÏr¶µ?.y®%,æ'J#N\}+	]GèÔ¤µÀ\x00036\x0000ëcô³<|Rí\x0008­°8<ød4õ%<×!9ëR=-`glÖØD¬}®¹êdÑ\x001b§L×\x0000\x0018%ìU\x0015f¯"MWû9\x0015åbr,â¼ë<äâX\x000eêâúN'°S­Ôó¿þûýçÏ¢PþôáÓ»Ï÷ïÎ\x000e|ÉY2¸X.Y<:ÏG0<¤\x000eòùO?ß¼~-úäOoï¿¾y~F\@±\x0005Å\x0003 P¬6Ï\x000cEÊ\x0014\x0004\x0001´í+4Ú\x0016Ô\x001e\x0001¥b*âç\\x0006Y\x0016\x0014/Âé[N36 znPÀ\x0010|K/w\x00144¶ ñ\x0008hYöô§Y\x001e£áÒÜr¡îsYG9sËpÆÌ}Å\x0000&JÁaÈr\x0013-1¿\x0000(ôgþÈ¡\x0014P¼F^Ò\x0001
î\x0012 å^Ñ\x0018ÑyÒ\x000f\x0007\x00166pÜ1½Nó8¥Pe´ÊàzwbK½óÿRc£·_>~"\x001d÷ï>þß3Å[ji 9gË\x0008Ò7ãË§¿¼º#\x0015\x0017Ï_ý_ß\x0006Ä\x0016\x0010Õ`0$ik¥1¢ð³ÖuÓ\x0002Ú\x0016Ðj\x0001Ë5]z\x0004@O¦¶Kåñõs-ÓâÀMäX­­ZnN^¨PgÏ·|^ËçÌR:\x000e×µ!®âáÆíAÇ\x0017Z¾ æóÒ¶L©\x0001Ë7Tõ\x000f\+k\x0001c\x000b\x0018µÑÎ%\x001fæ¹§Õ×\x001d¸î
Ö\x0002¦\x00160i\x0001=tÄò/F\x0019{3I\x0018ã[2'\x0013h´%¢\x0010\x001bè\x0016¡\x0014D?\x0005at\x0005¡7Òj+\x001dª,\x001f=Ý$¶Ò9I»\x001f=$Ð\x0019iP[éè«\x00189ºÚÜoi'[×C\x001dag¥Am¦3:~qjf­©ÓwÖBWZÂÎPÚR§Ú\x001b\x001cI+ÓÑI_k^7§k	;S
Z[MÓÔYJ^t§×þï¸Î¡%ì5h­5éz³\x0008FXÄÇ]mOnø$wÆ\x001a´ÖîÎÒï(ªãµc4\x000c»\x0012è,5hMu9\x000e¢\x0010\x0001¤M*%SUÿÂFÆVG;Â¬%¤ª\x00006¯ý4POúçýð\x0007ÆÎ Ö$\x0019\x000c\x0003¹êKd¬Áª\x001d5ÔØy\x0012Ôzä3ÔVÍ\x0002\x0004\x0005P&¥mÑ\x0012öñ¾Ö¤r©bd<×QzÞÙHÖê\x0000;OZO"Vý\x0001ÊÈ\x0015#Vpcü°ó$¨õ$©\x0004ª¢ÃR`Y%\x00125³aÂÎ Úd+éä ¢ÅºHÓ-\x000cÎ ÚPõ0ïÂ¹c>'õ^LÝ­Fµ­¦\x001aV\x000ehÊ\x001dÅË6\x000cb«íZdBIh;ShÕ¦0×a\x0006ÁV½¢\x001ckÈkák-agk¬ÖÖdãEB< Ë]	«« M\x001e=(¶ÛV»\x000fó2¨dÒ|â¯ª¢ÒZç\\x000bØmC«ÞÙÊè\x001cPT	6_\x000bö\x0011F{¢Z~ \x000bü2ûåÇO½ÿðû¹4\x001cý$k¼\x001fÏXH<ë%Ø'bÜ/_ÝýtóòÙ¹$ ¦\x00161i\x0011c®³¬
5îr"\x001a|zd|ý~ÄåLtIV2F'wP\x000bQäÑ\x0012TF×7ù\x001fbÄ\x0011µHã\x0015è<C&±à8¯#H?Pq5}.ä\x0010£ë\x0018z\x001dibà\x001c>XºOñ]>Ôh°vx;Bwb@}dþ)ëØ\x001d\x0019Ð\x00194b»\x0011«@¬c\x0015\x0002øáýÝAõùg¬#vg\x0006¿Ë3ÓO§M$ý µ@(y:ë²\x0008E'\x0004I8ÑRW\x0002ºiê
úfnöO_ÿöðéÜ¼ìóµ¶'ùªé½ÇZä ¶Äk¡èé±çÉÝ?ßÞí Ã\x000et)I±\x0013Ñù9ÊÖÑÎ\x0005ïqÞ»ñlguxf¢³üfùã<ì\x000c­·çÖÙ\x0011%kñ\x0012ÏLãf<\x00196R>®LïNn=Kç[<¯ÄÃ ³P\\x000e×f~ÄµQÔ_·dòut¡¥\x000búok\x0012ÓM9Dþ¶|WIv]£Ä-^Tâ9+Bi®Db¿m¼fÂ¼VÿÖá¥\x0016/)ñ¬aµ\x001aã\x0012Ö­\x0017å¦ÖªªJºÜÒe%]©çøßÅpÍÊ
N¥\x0016¸µNn	\'l´ßv7ù<OX+ÿr½»Ê _ï2>#$)W7âðX¨£\MÖ#=tË\x0000¥ÏÈ\x0001äÕÄù >ÃÉðÂ·¡¯ãë2h­r´¢ëfMgå\x0002\x001fc\x001aåëì\x001eh
_2rirÎKofù£ð%;ês»ùTsX %û#\x0003/¯4=/p§|	\x000cÖIu5d3h\x0014Éõÿ~Èb\x0017úÐÏÅ©F¢Ó¯W?<|xøtÿX¸ÿúþý9N*äz\x0010)½åAÊ<MN÷7W?Ü¾¼½»yAØ?Ü¼yñb\x00072¶Èx\x0014¹þJ¤9³sìàët\x000eÜ¼\x0001\x001c"¶-±=L\VV¦>Qk\x0001HI·#\x001b·y\x00158ìZdw\x00189@O	Ò<\x0018AV\x0019âå}ì\x000f#ã²ÁóäBD4R	\x000cx9äÐ"£È¹pÊèJÉöNfÂÕ\x0013±®!äØ"ÇÃ«ìêµ6!Já:ºÚÈ\x0003ùrÈ©ENW¹D¤2¢8"
2\åTà!âÜ\x0012çã§\x000f¹uq\x000e;÷\x0001"i32Ù¸%`\x001c9¼ÊTzÆ¥Ð¹lºÊÛÊÐû¾ÃÎoz×\x0013fÛ]æWÛt1\x0001óÃÞb\¾^%_o©çÏ_ÎýAçþà°ÿ.Ô2¡W¦\x00173'5Ûp"`3ÄÜù?8ì\x0000i¬hÉ9Ówåª\x0013Åøx1«\x0001\x0003Ã\x001e0[WÍ&HòÂ\x000c;\x0007ã.0#×[¦\x0010ÅÒ9'\x0005ÓS#Ï¥;\x000f\x0008]`öîZv\x0006VK«?ñ\x0017´\x001a\x0007£.Ð@gæÌóHOu²ÌþrÌ\x000f£NÐ`\x000e´Ì\x0003hQ2¬\x0011ñrç/¶·RÞ\x001cmÆ_	N5¥Ü\x0005 ­s.IS64'\x001dB/Ñn
LdVÛûþÏïïß}8×k2L¼NÍÅ2<e=v¾¤þüâæùË\x001dpØÂ¡
Ê1¼Ô»4Û2iÇ\x000ey£FW\x0007g[8«[9H×0'J¦! ¼rÞ/\x0005Adÿ÷Â¹\x0016Î}g+ç[8¯\¹:^Þgs-\x0017\x001e)\x001aµ
\x000e-´há;[·ØÂEÝº\x0019\x00013>féÇ\x000f:R	iÖ£tp©KºK(1iäæmë£lYÙG²]{ár\x000b\x0015k&®¸>	>EÝ¶ÀmL\x0014ÖÀAou68¥e0\x0015ñ±%\x0001\x0019mJ wÎ\x0013\x0007aL'üùáÓÛ?ÎÖ"Q²j^º\x0012ùòw-_U«?ßÞ=ýq\x0007\x001b¶l¨c³YfnZ\x0000\x0019âQÎ(HaJZõp¶³*8jßàª\x0019DËôr÷\x0011ÿàiDÞ\x0010ká\x000eTá\x0005.\{®0Ã\x0005î±\x000cÎ^8ßÂy\x001d\ë\x00005¡ÊLFkù«z×w÷êÙBË\x0016tl\x001ex\x0016\x0000i2Iót\x001e\x0007~-¶lQÇF\x001ayó\x0015ú·¥a\x0008¤\x000e5Áå\x0016.+\x0017.ð	h"9×>æJð`Ç6\x001cô6Ngä¨e\x0005$´\x0019¤ÂM]NDë{é:C\x0002JKbA\x001ab¡àÌ£ïBàú;ì#©½tÝa\x0005åi%aÔ9dbJ½c\x0005è@µ\x0012ctÝ\x0000å(\x001aN;\x0001Õ.ò­E0ÎãØîLîP\x0004þ9Gt&;ÖF2SLg\x0007÷\x001dv§\x0002u§tBÙàÄõSÎt`6k|÷Óu§\x0002u§" WÂ
híb\x000f(\x0001gñ\x0017q®;\x0015¨;\x0015¾Üÿ§2\x0004ÈÉYN+S­\x000e¯\x001d)Õ\x000c®]¯àõëó\x0015ßLfNR\x0000&È\x0007.á;;\x000c¤aM 
}àY~ÌÄ¿~}ÿðùêO\x000f>F£H$âJ|Ì\x0005XÞd+\x0015NëùgÿúæÅíë«?ÝÞÝ\x0019Ï&hØ¢¡\x0002Í\x0016g ñº£\x0008K$|8SÂ¡B³-ý®VÍµhN\x0006Qf»YÄnZ5Ñã
q£YXæ[4ÿ]­ZhÑ
Æ/K%ç®XJ¶nôWÅ,~WZ´¤BN®ûT¼\x0015¬\x0014æ®Ç-kÈ×ÒÉª\x0019
\x001aë´ÜõÁ°${\x0000[krÝ*\x0011±\x000b
ñä¦_~\x0010ûôýßÿë¯\x000f\x001f¾\Ýü~VFÍS~iÖ©¢ù\x0000¢ä£vcjçíO·/¹ºyvNDMèlKgut®\·æÂ¾²ZÅeË]BªQ|ZëÂèè|Kçt1ó¸N°ÞóhÐåu÷å>ºb\x0018O\)%þ8Áôõê§ûOÿ¯·Ü¿¿zñðö}ñøßÈn(ª)K\x0003Ü¹Ctx}sõÓÍÝíÓ\x001fo^\½¸-ÀwO¿M-)\x001e#
 \x00024ÜHéQT§ß¨B<Âj[V{5'
©3X*&%LÎn£Úù\x0008«kYÝ÷½®¾eõGXKÀ`®#+'äÒ¼]ËAízU
-i8¸ª\x0015iÈÛ5°lpª\x0002\x0000~­y5¶¬ñØªÊÅvkÕôtYä(\Z¿Z\x001dAM-j:v°l³Y|å[mÖ¤S=î£¹åÌÇæUÊ.Ô\x0000Õ®n4\x0014\x001c`mâ\x000er\x0001æ»]Tè}Õ!gåÊÝ§¡MÎ\x000b³Jä\x001b«©Z7\x001a\x001cíÜ\x0015\x001cóW9¡(!\x0005¨#°T7]¿¢\x001faíÜ\x0015\x001còW®üßV\x000bà@Tú½\x000f²°\x0001.\x0003Ûù+8ä°\ùkªf\x0004X~¨@ºc×\x001d{\x0011\x0005\x001bC~ x¬\uV@t;ÑÒ)¬qÝMyµ³­pÈ¸\x0016£¨E´»ÑJâ³\x001c^È\x0011üå¾w\x0005÷ßÙÊîäòT~ \x0010ûç÷÷o\x001f®~½ÿúÛý3lHî?pÑ¹!#Ô*Sû':¾_Ü<½½úõæÍß²-Ý
eMºNµ\x0010~®w\x0006µªÜÀq$×"¹ýH\x0010j	(\x0018ß¥\x0004\x0014ú;\x000eÊ·P~?\x0014ÂRË\x001e¹ü\x001e¼«=\x000e})­)µLI±Pµ ÚFæ^\x0011 AG¼¡úW\x0001\x001dSnò~&zb­¿,}kà%é\x0019Mì\x0013Ú*¨%²NQ|=Ã»²'\x000bÕ7¨èzk°ß\x001c4;*FàDgB®À-\x0006ìøç[¢
\x0015{Êðûk\x000c¹nsy-Æç\x0001¨Î À~aQ"\x000e/#Årû$ðsª³\x0008°ß$ ýÿ\x0006ÞU öDåì²«\x000eoõlº\x000fHÿ¨±èË¤ÔïIOûÆ:¬ØcÅý«\x0014\x0017k>Põ\x0003ýÀ\x0017l<i _vÛ¬ú¬\x001fë$\x0003ð¡püC\x0016Ç|
gUl4«±\x0011*\x001b/4áÀº\x0005+ôS®ðõ|½ÿôpõâëÛw\x000fW7_ût.Ö*A·Ìµ&\x0008Z°5Óêúù8¯ÿÇ\x0012j]½xóôùíU!¼»9\x0017\x0016úÓ$¡ZÄtÍê\x0002f\x0007Y Ñ}l\x0018Ð¶V
X\x001cSài\x001fÙ\x000b/UEìÏÅ!D×":5¢­Öøk=z¨
fþ¤#ç\x0010¢o\x0011½\x001e±ß0#\x0017#&ã}?eè\x0010bh\x0011þCÇk^DÌ,Ö@­Ó2,¥/ò;\x0004\x0018[À¨\x0007\x0004\x0019Q\x000c"WøXÇ¤¡Ã\x0012'E¾æ°Ä¡\ÇÍû÷\x000f\x000fñîóÕr·{÷ñü¤p/éI$r¾à\x0001\x0018wYÐ¾\x0010áÅÛ[úóó×WOÊÝîù«3³ëÑuNÏ×<ð*\\x0010ëÜ53Nè;B¯&,$V\x001a|,¥$'D¨}T¾ww\x0018CÇ\x0018ô^jHØ[\x0001¬´§¹>­1vQÏ\x0018ënt+hÖ0Ú\x000bìÆÔ1&ýnµmµlÌÌsêE\x001cÚ)Ç¿uî\x0018³±ô\Mc\x000båÈØ*yàN\x000f0:Ó2:£gLõÀðwv5\x001fqRË{\x0004\x000f:<Ðãñ+Cý\x0015ÜÌ	%úaÂ\x0008Ç¿rÆ\x0013\x0011¾ï\x001eûåÓ»\x000fï¾üý¿Ê?\x0016Øs´{æ\x0011¤6Ø[\x0016ÁFoj\x001fõV>qjbøåîùËç¿Ð?\x0015èWÏ_\x0018[b<LAt\x0012ÝÓ½¤k«Óy¬×GOl[b{Ø\x0001Åºhä²\x0016¨^\x0012Â#-6z`×\x0002»ãK\x001cëÕNÊ\x001có\x0012ªm±¹=Hì[b¸\x0018SÉH\x00147Ï]}Þ.\x0019¥ÇdéôÄ¡%\x000eÇ\x000f^¬ã~ÊM#Èë£©ê=ÉécK\x001c\x000f\x0013Ç´£t9\x0003{\x0019\x0010[ÎåÅS\x000b»$\x000f¼±\x0004-ÜÛVîêä\x0008áE=qnóñ%Ò2@5æ\lé\x000c4ð|¡¸ÉÝ¢?\x0011»S!IUZd¬]p^Æµ\x001a»ñz¸ó\x001fpÜ¾4/rrò6é;ø;{\x000cÇ
rAæE\x000e1×³\x0017êä­y\x0010è\x001e\x001c?{¡NÓ\x000b³\x0008¿V\x000bòF\x0015À1bì62\x001eßÈ¹vLúê ×eâ¹µÀ>\x0012:¾sÂ@ê@åyÓÁ,ý±ë\x0001!C¡.m:C½únwD¹NÒDjN\x001cx\x000f5'þ|Á\x0000£U\x0004^\x0011P·âS#×\x0004îP\x0004\}â\x0004ýÅÌ]?\x001dt\x0006\x001fXñä¥0\x0006ä\x001czºGqd\x001eÞ\x000fnNßã«ÅÌ¿ÿÿõ¿oÞ?|øûÿ÷ñLz\x001ds1\x001b<mÙ\x0014=×d?²Li´°®NvuóâöåÓWg\x0012ìB-\x0019êÈ¢¿ös\x001d3yi®\x00146Aq,®×o?mÁ¬\x000eÌ\x0002\x000b2Á|myÉlILnÌµdNG\x0006G\x0000]ÚÌÜ­\x0013\x000f\x0013,d\x001b\x0015¶ûÉ|Kæud\x00082+¸/gÙfXâÅ\x0001²Ð\x0005\x0015Ù¤ì\x000eLføêeª@Q±×\x0016}?XlÁ¢òcäô
udò%\x0013,¬CÓýd©%Kº%K(\x0015¹\x0004Í2iL
¹#n\x0015G+lÆR\x00085[{A³Üf\x000bäôät:\x0019;k!ì4h}Äln«Ø	
ßÍÒQÜ«\x0016wÄ|@ë}gÀê}w\x0002z\x0019îT-r\\x0006åú,fCxFóy¿ô÷\x000e\x000eYo¾¬^ä»D\x0003\x000bë±I*¸ßz¸ßtp©zd¸k ,"\x000bk7Æ0|­Ä'-K¡zùg÷¿Ýýë¹\x001bSî\O\x0004ÞMPô\x000cÇ§uKÓåæÉMzs®\x0019(xx¢B\x0005U¬MTÆ\x001a)IòÂñä
,ÛbY\x0005
Õ¶\x0005/oúà¸PÜ0\x001fû±\å\x0014XÅª\x0005ÞöhØä\x0002$/\x0002oq#yµ\x001f+´XAE"\x0010âÖÕJfqëëèq?Vj±\x0006+ðÐ­É§{^­(\x000fS\x0018ÍÀG\\x00129ÓA4
.çDû)[\x0018\x0017;@0ÂuòL¯äê"hÎ¢Í\óSà\x0010¨ìyy@F«Ûó ÙôÅ.ð\x0007º¦Ì¥×\x0000NÞI5k«Ûô Ùõ\x0018%÷á\x0007\x0011\x0000Ò `\x001b±Qk¯Øõm1ï|	1ö­«q6ÊÉÓÇÔÁ6°d§heÙTlF\x001cä´rbÆ`Ñ©t#F\x001fVx:º¨£ì\x0002³\x0019N\x0002³}¶#ÌÞ|Hå¸Ø\x000eòGoF¾,®\x000e».È³f¦©Ø\x0010\x0011G·1NäÛxpêÎaqç¿½zúÇßÿß/\x000f÷_ÏaÈU\x0003:\x0006¾F\x0001	vn>^sOÄÓ\x001fo~¹½yóm0ßy\x001dXë©¬\x000fÒ
Q¥q7^Ð\x0014d±%*2¦Ãdåäjã\x0018k=Âº\C[²¬#24NÖÜ­áR­æ°\x001b£ºö5ó~iûñö %)\x0006-h3¬\x0005M\x001e9ÀÂÈçî\x0004î\x0008Ì.sÉd\x0006%¦\x0005Üì\x0010ÜÖ\x0001Ð\x001de\x0008.µºp¤ær-ÅÚá¤@ë\x000e\x0001èNA®ÃÀ\x0013,\x001c\x0006åÕj³¯údé4gíÏï\x001e>}DÿãëÃûwçkïñÚÕÀ{\x001e
W"£Xý|^yßÞÝMbÉÿãÍíçgné4{ì­Ñ.ax|9®t \x000fØ%N_Ù\x0011=¤m!í!HI\x001d8\x0017\x0015HÉ\x0017aZÏéÒCº\x0016Òé!ÁÕQëÙ Û$_ÛÚuT§gô-£?°À]k@=|Kì)ÑS^¥µô¡e\x000c\x0007ÖÑÖ\x0004y	¢¬å¬¹7·V¼ÑCÆ\x00162ª!! \x0017ªøI\x0004 VÖ8³¾Së\x0019SËô9ÐÄÄHÚ£3bt
ëW#=cn\x0019³ÑK¹ú#§Ât?\x0017\x0012Ö\x0012\x000ejÈ%\x0019Ü\x000cP­¤e¡Ôr\x000fJr´}Üx&ÔCöÎFïm \x0018\x001d¾Vú\x001b'J'µS6Ã¸ÎÝÞß@Õ\x0006ÀzùµNêhmZ\x0017óè);S\x000ez[\x000eÉÔ£c3×ªÒZZ¡\g\x0018õ¡\x0004½¥\x0004~x[ú ¯\x0014ÖóxÃbÜ\x0005¾xgà\x0019*;~#+\x0001Þõ|\x001d(±pÆ?8v'\x001c\x000fð \x0013}x9Ó]~¶bÂ*ÔSö±ÚÃCòüÁÓ4v¶b\x001c®«qôÝáÁ\x0003ÇcµY^kËaÏzsv­\x000b§§ì\x000e\x000f\x001e8<.ÍÂÜ\x00052r\x0019d¬ÛÒ­ëÝôÝÙÁ\x0003gÇ¹íÎdùÚÈ*Ó¦\x000e\x0002ÒU¤\x0005\x0007±\x0018\x001eîÈ*\x0006§#ÓÚ°Î³ª1ï×ñ@à\x000bµq\x001eê}
*ëÛÌ%Ê.õ:G¿S±f¾6Na\x001bG\x001b¤º#qÛøñéÓ°©{#× ÒJ®ÿ1\x001c«o\x0017på}Á×|ë9´¦F#C·r¶©.ª¹@,§¨xlM³\-L4¼¦©\x0016T¥áSRý7¯©¤¹5G?ºú°EÊú2%àtë\x0003&t©4a#z¯wîÒ_6Ù(N\x001fPV¡Ú¨Ã\x001fOE±I\x0016Ýþòp.')/Ì¢äýèY[Rß\x000eÖw×¿ÜËÈÇÓÜPlrCßDÊ&<Q
U\x0004?'TäV&c/mìn$\x0017¤/$Ñ4\x0008®3,\x0011°´7mÜmö"¹\x0016ÉíEY©¡\x0005ã´dë*Ew||äw¯_d\x0018<&±I\x0012µ¸~GÙ\x0014Z¤°{{CIÑÙ°D0Ír¬cúÂúäí%-QÜ½HeK£4ÄFyÞ$cx\x0006\x000e\jÒîE²¾ö¿\x0016CÊ6 %¬½Îùø*å\x0016)ï^¥ù}P#æîâ$-LÙ£HK:&¶éo/\x0013Í\x000bj*¹r¶¬X5\x001bñÆ^¦Þzï6ß9»jl¨¥ÙY\x0004	\x0000Ö¥ï»:ó
ûí7,ï5Þq_\x000cU
\x0013ÆãëÔ\x0019KØm-©^Q^x©£îêÃÛúÝm7Qg+a¯±´¦¸,5N2¸\x0010ª\x001d0öø\x000eï%ì¶9¢\x000cb¥g\x0019>tË3øÆ4ÁÝHµ½æÒ\x001az\x0001Ï¹´\\x0002¸øõ(¼ÝL¹½öÒÿÓj\x0008êrYª¯òf©³°×`ZjJò\x0012×³¬#=ÚÖÎÕã\x0000;{
¦-7±k\x0014-ÇZÅ\x000c6x[^W/ìfê\x000c&î5¶\x0004Òö\x001ds}8)\x00010\x001d-±\x000fw÷ÚKK/a²ÅA	\x0000ª¨ÌÔft©wqwÀû¼\x0016Øn;ÙýÛ©|/À1I\x0010^þíÚ9¼nß\x001d¦ÀRÔ=ß~ÛííL-\x0001\x0008Üå¬\x0018q»¶Ý}{j¯ó±¿Îÿ·~@X\x0006-c\x0012Ídªçà\·©Õ\x001c\x0003ñ/,õù+Þ\x000fËO¨ò^,[Â\qÈ¦Ö¿cX´K×E9ûcÕG\x000cHõKXíhmcÆÅ\x0003÷*\x001b¡OdX*~­Ã\x001e>}¸ÿðûÕÓ?\x001eþóþýûwgçr\x001f\x0006\u\x0000ÙrµFHkåè?ÝÞ½¼yùìêé·¿Þ¼xñüÜ\x000c\x0011ÁÄ\x0016\x0013\x000f`ú\x0012rkóRqL¾ZÏ½:Bi[J{2\x001a\x0011ðô%\x0000»ò %\x000bÖ\x0016î\x0008§k9Ýî­$\x001f|Ù³ä\x0001³Á\x0001°..ÕºÓ\x000e\x001b·tØP«ï\x000f
êç«?=éø¥+Íæ<p`±ÅâökGKÞ\x001atþúê»Âùúêç»Û3­¾î´\x0010Ö5°»\x0011I¹YÚ0³«¥`¥9Îmt(i\x0011}èÕ6ËÛ\x0019¦\x0018\x0015ÈJ2Ý¯\x000bÛÔ±%jÂr2K]gPßs7Z¦µ¹EÌG\x0010¥Æ\x0010P\x0014.A\x0008ýaQ\x0014]».1£» bwX@Zè\x0011"-²þ\x001f\x001aºÓ\x0002úã\x0012C·\x0019¹å\x001bC¬ÃF\x0007ºó\x0002\x0007\x000eLh×Q¿¥÷û"Ýy\x0003\x0007&µËÈi-ÌËnÜ\x0001Ò!bw`P`¨ðW1\x0004V­,WÉs9\x00136\x0014·ÝÁ\x0003'&Õ×0:1¼Ö\p7bwbPb¨3\x0017ÝÈ§ÚJFü"ßº;1¨?1T#\x0016W.ÆÚKîÇîÈ þÈÐ(\x001f8õ1Ts1DÛ\x001d\x0019«>2$¡à¹È\x0005¸ÈÅä(ÈÎ®ß>ô§½j±ñYTcTögYLQ¡h
Ð\x0005bÇST{\x0014RíÛNòÆEÚª\x0012BÒÈðQRX-ê\x0001ÒXÜNnüÄ\x001ds¤ýç*éq\x0019ÒÉ¡üÐO|&öütÿõÃÇ¯çFNÚ(ÜnU¬\x0010Kc¥>\x0010òúM¥\x001dÛóÓÍ¯ÞÇNÞì	\x0016ÁR7÷¾ÎJ¦,1#É×z)`m\x000bkÁ:6öåüEúB\x000bëZVw^gY;1%Kzy\x0013¬Oµ\x001dpC\x0016ä\x0010lhaÃ1X\x000f¢|æFvMU§¶ZÙØÂÆ+këk¯#æs¨\x0005\x001eèÏ\x001dÜ\x000fZØt\x000cÖùº²Ff\x000bÝ+­>ô x\x0001X8Ù³Ó?\x001f;bAFHO\x0001*\x001b¯Xßðüù!yûyÃ	ïÁKóM·Ø/t'a\x000bl<\x0012\x001d4¶m!Ülp«\x0010v\x0003\x001b\x0019TîÇ×È§ÍWæ´\x0011Ç\x001cdnüîÌ\ý®v£Ì0Ë¨-ë\x001cäÐ\x001fñ§°f§Èá0²×V~­Ä\x000b\x0019lmøÜÐH<æ.NÝaæ\x0012Ø#U¾pùúHåÖm\x001aÇá\x00192ÿóâ\x001d8=pô\x0008RÝKf³SM\x0005å¦Ølp?ÓÁô\x0006M«2O
T¿}zøú\x001fß¯\x000euSu$^\x0008UaCíöêÅÕÍ»Û7¿¾z~&K.Ø\x0012¢*Ò842\x0006\x001cB­A´Ö!Ú\x0016Ñ\x001e@Dê\x001eµ6\x000c\x000bI¾6M×\x001dEt-¢;ð£<jfW\x000b¤CU@X\x0017s«?t§u7Ð\x0002ïÈ²9e1C¬Ç}[Û~\x000fið§·0_\x000fÍ\x001f®~|wÿé÷3pè"(°Ê8\x000c)ß¸Î¼¸}õòêÇç7wÏ¾
f[0«\x0001£\x0001ôs¶\x000fç\x00033¹Ú4\x0016×ßW\x0003Ösßó|^fÑÂ!7hxyê\x001f^¸S>«ä¢Þ\x0000Ôô`dÖ¬àE<§\x0005ùèÚkÿÓ÷\x001fß}ùôpË\x001a\x001a-\x0015xÔ^\x0015nI]&ÀÖýùéWÏ¹»ý6\x0018¶`¨\x0001sÊ^'°T«r\x0015!Ô©Tp\x0000Ìµ`N\x0003©\x0019]jX¦\x000ek2qC÷HÁÕ`SV²sÍ@íi\x0008Fbíz0\x001bÅÕ{Ø¢'m\x001ft\x000f8\x0005íçû³C }K°Þp.¤ÄÙÄ\x0010RÚ\x0018SÈ~¾97þY°°ÅB\x0005Ö<àO°¸\x0018NÞ
ÕÖH«oR¹ÓLK¦\x001fÏóÃÃ/ï\x001eÎ~J7G¢sÍ\x000bÊ6\x000bµ\x0000¼\	\x001egòÃíËÛ_ßûî4ÿæéçñìBôuÚ1M\x0016f%«u²pZ×1©\x0011mhõ"\x001d[\x0010Eº .«¸\x0011&k\x0011]èÔ)ÿdçæn½X¥+LÜ¸1é\x0010ÓÒúJ)\x00065dñ^§ë\x001b\x001eÇÈÑZÉºî)Ü
þÄº\x001fØºüý¿æ\x0004ûÓ¿ýÛs¹uk}\x0013
z³Àhk\x001b¶	ý#\x0000\x001fåÛ×WOÿüÃËsyuÃ\x0016\x000ep1I¹\x0010\x0015ò\x0014gM]=ct¶¥³Jº´8Úàd\x0000³q\x0019\x000cct®¥sZº(ù1\x001aäÈOsuÞBÞr\x001d
:ßÒy-çê¿èßpUxÜø¸åA\x0014p¡\x000bÚm¥Õ&LÎyæòa¥óÛ®×·N-ý l\x00073ÌÃÜª\x00189)RÛ\x000fiOïbÖ·¡ñ³o©ìôêö÷¿~üðûÕO\x001f?½ýãã»Ï\x001fÎAã\x0016æ&\x0003gb\x0017\x0019\x001a\x0006\x001alÄWÏ^=¥jÔ«Ûg?½zùìê§WwO|õüõË36Ñ\x0013øòÀÿðõo\x001f\x001eþz¶@Ñ&é&A³RA0ò*v:	@xóç·?+K\x0014(l¡p?\x0014Í×a¦ZR\x001fP¾´wk_¼É¶LVÁ®ç'YK.\x0000¥kÄu³Ö~&×2¹ïc|Ëäw3QÒ\x0005ß(TÎ2XÒZùb?Sh)qµ0X[«pCöq\x001d"ï-TÜ\x000fU.÷¬1hi\x0006¨ÌN²R9¯"¥ýP©JßÉJå\x0016*ïrÈq\x0007LæÊIR/Ò\x0001\x0006lÔÒw;\x0019N³*\x00037þ{sÍ\x0006\x0017ïÎÑ\x0010ò>\x000cÕ[óýæÜ9y¼*K¯Ù"d\x0019\x0015p­;¾\x001fª³æ°ß;zw¼RY´oË\x0006ç¤tXOÜ\x000fÕsØoÏ\x001dUæÏi6ÚôÓÐYÔ3ÃñÎ Ã~îéå|*\x0014Êµý6¬ßö3u\x0006\x001d\x0014\x0016=Z)és8>óí=ËF_7àî§êL:ì·étæ>¥\x0017*ù,vtª³é 0ê³6çü\x0001A\x001a^£\x0013\x0001­²Õ\x0007\x000e`gÔa¿U÷h®-ïõ\x0012E³ì¬¥OS²è0UgÕa¿Y/ÿº$âé\x000br\x001fY\x000cr'*_ð8\x0015vf\x001d÷uO&lÖcí\x0003YvûqSQÇýFÝeq$%íVÏëËÄ~ª>FßoÕKø)"¥Æ\x000fÌ\x000b\x0014)Ò åãTYÇýfÝ£\x0013\x0003\x0012\x0017!¯'\x0015û\x0011ÖO´û¡:«
«n«æ¬£üç\x001cÀ$®¸¡±ª³ë¸ß®Ó\x0007d\x000fè
p*¬|@Ç\x001bqÀ¶³ÐæËß½æJÊS¼HÉ<p¸g¤$>\x0007¢õ6\x00131Gìò<·+>\x000e\myºX¨"\x0002\x000eì­>C2ßá\x0015\viT±èdà¯Ñ\x000fkáFEµb³ªEëC­à×¡ÖÀ¥b\x0005§b³ÉÓÓù\x0016f66[\x001e9\x0004þÍ«ÖÍTítK
]¼nVæoºz¤û6=M\x0018YcÚQNw}¾úÓ»÷ï\x001f¾¾?\x0003X\x000eèÒ{4õ}L\x0012rI<xùÚ\x001bã±_KëõÕ¿xqûæÅ·a±ÅC°ÜÖ3Á<'jcZt7Û>ô°¶µÇV\x0016eYCÝÍbÝºÌ1Rßúc¤ôà#­*®Ö¡\x0004y8s~ëÁç\x0008lhaÃ1X/¥ê\x0005Ö%r¶®¬Û®u©Û°ôp)XgYð\x0012bqÁy_Û6&³\x001cÛ²­¡²æ´ÁFµÄ¦Ú\x0004*¯á-¶öú¥wÔC&a	0l\x0013`h­B®/!WuÀIMxëÝWÁ\x000bÆõ\x0002\x0012ôCóº\x0000Ê9?_Mó#\x001fçÌè9bbÉmh½´Y´QöfúÛo
åô·\x0013\x0011[DÔ#Z#Tâ
.à,µÞ%lL_Õ"º\x0016Ñé\x00113\x001f(Ò\x0016á@\x001cmâ*³!ÎªFô-¢W#:\x0014mÈh\x001d7y¢f\x001a³5LK\x0018ZÂ &´õÖMD)8A\x001b¥ÆÔØÍB0\x001dbl\x0011£~\x0011C}ÐDÃ½åhëÜ¨b1Æ·bj\x0011~\x0015³H£\x0015ºI¥PiÝ0bn\x0011³\x001a±r.w/8ü¾TVÑË{?Û~Í¢ÑiãRþí7\x001d\x0017.\x0018ËyW3ö¦[o»=òKOa´ü$VÖ§n\x0016Æ¸Õ¡cìl7èwÙsÐ\x0004*'æºÄ²å!Çµ°¾ÑvöÈ~ÛbM±Ø\x001c\x0017ud5ÁÂ¸Ù~¡cì\x001c\x000cè=\x0015qr93\x001c²q\x0014F?îa ó0pÀÅx\x0012Ð\x0019«\x0019Ë:\x0012ùÍÙ]¿Q_9¥_e?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-19.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-19.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=»cíÑô\x001d`Ü\x0006~t¾\x0013Q+kLyï¶ã|Ü\x000bvq\x001bÐ\x0005\x000eª0K­«5ÎÐ­×Ñ-\x0013\x0017ýKã«\x0010®'î«®7}ÇqO°ô¤Ýú\x001e ¦¢ÃÕiD­ØgÛ=ÀvÙâ1¥ì
KëÏU~.»v!\x001cU4.Ø\x001eã5lGW~æXPbE^#Ýß&\x001cÒ\x0013\x0017ì\x0010)\x0016ô²Ø
­\x0011>KdNôÑQ¡ã
k$4:{è@Ä°°K#q\x001e%:.Øð\x001e9	K\x000ci\x0014ûl\x0001\x0006\.B'¼\x001bY\x001a´ÌÃNmKCð\x0005ºÂ°­K¸4G\x0014zDÞî¥7NÇ³Û,bè-O\x00068¦4¥\x001b'DÇS\x0012\x001fx<;J"\x001c%Êe"÷9_ËK\x0014ö\qí¥\x0013ÏV`\x0015\x0018¦f
çù\x0015x\x0005öf×ß\x0005\x001b_êQ\x0002Ør\x0002"3«úJn5.×[OÝ	vÂ)Õ
\x0017|,ñ%Î6»8ü[\x000eëÐuAÎ#Pe³±ßCáj\x001c\x001dD\x0007t©ô¾×³\x0019Á÷°WúóØ7¡²ToõÜ"$Ø©7¿|IÐéÙD\x00126ñ\x001fÈmPL,ØM¹$\x0005ò\x0019\x0002y_\x0013¨Óª¤\x0003Ií	¶ãqwÕ|ö%3|IÑÉ¦hÒ=(N_
}ö)3~Ê4ä~Bkb¡\x0019qì\x0003¬V=Ô2Djj\x0004\x001aa\x0004\x0016\x0018\x0011l>¹Shâ\x0011ÇWü¯ø¦ë: ¡BYuqn\x001eVÎ.Ê\x0002\x0017¥ÊºF.\x001c\x0003:¶
qÉµõw´Á¼@ãwt	dÁ°D
Óò¨CßN\x000bÊT®þã\x001fOædm[|¤~X8¿\x0010ÓØ°ALãÃ\x0006¾Ð^\x0007êá/åõ~ûâ¾úæþíW/~{÷êëÛ7·×ª1ÉJbml[/<DLÝ®Sy·o¼U&â\x0008²FB«)\x0019Hw|9\x00183ëÛ\x0013\x0004;$¨ÌØP5\x0018Ö)Ê\C`mù[²V6`ð\x000fLà\x0018¯\x001aÕûu×\x0013rjërát1É/¢.² P-\x0001\x0016OF%\x0015\x001fÒøÂç¢0i¥TS±\x0002;öSìý¼\x0006ÓKÒ\x001dÔöú%ÌE¬xE¨O#ËuÇÆH_x\\x0014æ¬H8mI¾|[Ô0b\x0012cõÑ\x0013Î\x0004#-&ÌE(\x0014E\x0014U¦1tBYÙ-Ls\x001cKASæl\x0012'¿b/\x0006¬¼
sVT/\x0006Åóõ¶\x00084ÓiZÎ¡ñÆV\x0006M%EY*ÐBê7É\x0001=Ë²&lÈ°Sª#yû\x0014¨È á2
z3`[\x00194\x0015f\x0014¥y\x0007Î\M[Ñeå0K6è±Y´ÙÉ5\x001d42¤Q{êgñJëY÷
mÐ°[r~	3­

Ú{ÞßÉ´
mÈ\x0015\x000e¥V²ïÓT´\x0006]¢[·
uhðÇP\x001dL\x0018t\x000e{'\x000bÛw/¢³Í\x0002æLÊö\x001fôÜ\x001aye\x0018ÏÛ»«p­:®£c\x0017TWw\x0002?°fn\x0012\x000f¹·ö,:´ÿØåÌÔ¡Ç&¬\x000ez÷ôº2lè
\x000fº®¡
9\x00012Í\x0016,i:ØyÇÇ$YY\x001cuä\x00023MÆ\x0004Á§V\x0003h¾U¢ëÍçgk\x000e]]-°»Ô+¤°ÅDÊ<èÐ·ÖÎ;Û-âX\x001ftÓ.Ø\x0010\x001cý]HÖß½½\x0016ÃÚs\x001dL®¢°÷¶ëÉ¶§¢ëå¹µ±Ö
(ÇÝïûGÀþZ4^7jhNmr²·¸
¶\x001f²ÇýïgÕ­nºÚçXßÏO
¥¥$ÇÝ¿\x0001Cw»Ä¦\x0001­ãÎ0_(TÕâtZª~Öó*ªe
sQ¨\x0018ªâ·S\x0003¥_ª~
UsE¢êyö4\x001e!tJEYª~V
«&SÃ Ú\r{á1'·Uý\x0014«Êi\x001c©§»°ÞSÀÇìã:Võ³\x0008YµPÖÒ
Ã&×ò\x0001\x0003ÀÐnãíë§hµuåc´\\x000cDV\x000eì\x000f"÷zïb^\x0012fy³ªD
èbh\x00048Y,ÓÃ:¦ôSLµQh~Ë¨§ÿ§\x0011àÓ¢Õ\x0004ð\x0017_Ý|ûøJNkÖ0«>ÅrÑMËêt4\ëÚRLÏ~\x000eê.û\x001b\x001aMêt\x000cªÌ\x000cJLZ3ufn®L=]Üët\x000cª¿\x0002"Ëû!ãb;BåmR×&u:\x0007µ!\x0014w¾gåW\x001b\x000f½ïeÝhR§cPM2\x0015N\x001b2µ¨Ä\x0011\x000f9®U>6dh4\x0010\x001bM¬¡Pþ\§£;4Ôé\x001cÔ<RAä±\x0007eÒõ\x001cÌëv:VZ^¾Û<o³©ó\x0001k×í u:¬ä¥¤ül2\x000bià§\x000fØ5«Ê£Û²cåQ]z¾#©/Þ*·ÖÂÁé\ùíÝ7÷ï®Ö¿fø¼)1InÔûUÿ£7}\x0002ÄíEpe¦SEEÈPÆS>\x0000µ]ÂÁUì«3`0«Ê	oýä
Ùf<ËÚØØÊLg\x0016ÎHà§²â¸	Ü¢¤'ã:¶2Ó¡¢<\x0019\x0003Cv\x001b5MàV¾ØÉ\x0015\x0010ÈL[_\x001e\x000e ÇlT.\x0010\x0014ÎÀ'a7¾\x00037)%Ér\x001fú*bôÝÓ[\x0017Ú½ú8yñ»Ww÷WÚFZäÇÇRI»3¨\x0001\x000e<YÛõM&hu9\x001f3\x001f2eSæ#lYmô*¸Å5µSfá6Û­AÏ =CÃ\x00034×L¦9Å°n`	'\x0006\x001b2ÈVjV\x0002eÛ´o\x000c7?g7%äíyÓ\x0013d\x000bï'\x001fó©uð¥hå\x0006
9Yï+\x0014¤kÑ\x001a2ÉûÂÐ½=þl>ÐöÑÂU£E\x000e¬\x0010*ÿUíº;\x0011G3R0UXÕó&ÍRëEQç\x000cÚ}\x001côñ\x0014³úÞãÏ\x001f~úëÏï¿¹VD\x0007tt\x0005²þ#Ô\x000fdÈ+	¦=À>\x0001càÅ¢ºXñ¶£÷r\x0012GÆÀ9È//ÓH\x0012G\x0016ûÒ\x0004\x0001D\x0015ôê\x001céÆÀ¯çXZËåb¹wh´`Q?\x001dYùñ¤\x0005\x0011ÓíaO6iÆMj"]xJc"IÂ\x0018ù\x0016»È³],÷í\x0010´öãÜ\x001b#\x0011Ù[^þ/KÙÚ
\x001cÐVÍ¨\x000fæd³Í-®öq\x001fì\x001b6ÈÖà\x0007'E}\x000c\x001d\x0015©åK²bÍpa5×±\x001dÎ÷z÷<¹óNóm<Fr\x0012kR/OV\Â¶=-¼h\x001bìØ`vX+h2\x000b¶«ïhá\x0013L»(üâÞlØ\x001e\x0015CBFaE5ñeg$Ga¹6c\x0017::ù\x001eõ_tëD\x00163É~/ø2a·òÌªm°aG4XÓVß\x001dZ}^ØßÊrO-d®\x000b4\x001aÙ\x0005ì"Ec§ô!¯nÍÃ¯\x001a¡\x0003Ü\x0014÷ï5ZT£\x001fÿ|s­¾Ê\x0002^Þ{CziA\x0000àmç ~\x00027ÅB·v\x000f6IMpzu£wxd$}'sÉ°/Æ¡\x0006m
B\x0007¤1È¿\x000e"ÐI\x000b¹\x0004Ü-|\x0016T\x001d\x0018z\x0013Tù\x0014*NJR4@\x001b3{¦[sfã½aã )S\x001a<@\x001esÌê0Å¯ã¹
\x001b¨c\x0012ù\x0000Ãº\x00066LÖq3s':{f\x001cÚ°!\x0013l\x0003­Ev,ÂUYÁ\\x0015½t¸hæëÐÐp²ÀÜ\x001cKÿ\x0005\x001bHþZ?pcÜNf\x0008K\x001eòßÍ«Ävé¯\x001c'\x001b68NV\x0015|\x001aäÅê\x001cë,H<M\x0012\x000eÞ÷\x000cå¢\x0007|Ã\x000e\x001dÐÁi\x001ccSyB°Û=±èËìÐÀn¦ã\x0015¤¶kèÍ'ÐÌ\x000fðÝpwehÙ±qº£Az[ù\x001d¤?wÝ½q¥ª ØÈiW±JÔ\x001dÚ\x0004½í}f^5\x001dwdØïÚæ\x0000\x0002çêÃF-_\x0005¼ÒüWY9xQl>)¿½s÷Ó>Ü^ëV\x000c³d¬	û5aÔ´u;«\x0012Gó3sÝ´Üü·è)ÈT}Áz
9\x000fGQ=\x00028³£òö|\x0004Øv\x0004,\x000eE?Gý?\x0000f\x000b\x0008CE	¸Ø«BÞ¸Mëv±$\x001b6ÈË\x0015õ-£\x0016ï\x0002ËÃÈç­\\x0014v\x001dávhpj\x0003¢-ÁJ
|\x0000¸F\x0003^¹'th\x001cµÌHñ°Ükí¶Â}f\x00127v3lÔM:&DÝ\x00121à*ÙPÑÞ+Á¶õAgÜ¹bWô7gªëZÈ¸¹ãz$T4j}½á\x0013ãý¢ºÂ´éjïyZØ»ul°wC\x000bÇlÔÊ\x0015×uÎ|jI¬ýC\x001b6ô\x000fµIX!*»ý¤ª0Ks²iI³í\x0018PÞ¤Æ\x0016ò\\x000e\x0013Ý4\x0008=µ¯Y×sÎg+\x0004ÛpNÎ©'Ï¸Ös
­
\x0012
AV²}YúÅñÕfJg¶®ZàÛ[\x0002\x0002 Y@\x0016**ZfÓ¸«4÷>\x0005¬c\x0003Û¨dÕ ý+\x0003
KwzÙEiÙsÁ\x0006»*§\x000c9Få\x000f±¡:î\x0010vg^®Lm;6\x0004f\x000b§.Ø\x0012YÐÙZ¦fiÓ
q\x000bU\x000eMª,Ù\x0011´«l\x0013%W0.AW»¡ÎR=¢a£L)/3\x000bÕT<\x0000+\x001bêH<Ùâät¶ã\x0013´k\x0019µ\x0006\x0001ìÈ\x0006±í\x001f ì.	WJ	áÁ#O%`þ¶nD"nó®t¥K®|m;4N·Ü/Ð,£õf\x0012Á©ìÊåôØlÍ2gÃ\x000e8lCZ#î¯\x000c¦¤t] coÈ]hd<MÔ\|dùswÜ&Lq¶+\x000bîÊFL"Ð¦%\x0000®I{ÞmeÈÛ¡=®ÀCÚÁ\x0016iºmâOi9ç±§å\x001dx\x0005º1nAØº­ZzaÊíO/\x001a6Ä÷ê«\x001dlÑO+ÐOÝq>¬Ä)\x001c°\x0003sûâ×÷\x000fÿÇ»/ß\)V\x001dÝ#\x001a]úBj
 T%\x0007±ÉípyÖ&j\x0017É÷Ew¯+\x001cvêS\x0007²¶N3ÌôU¹BÉ\x001aY²\x0016Ò.ÚM;6_Ê^Û¥M\x0004[é¥\x0008Í>öµ¯ËcîsC\x001e¹O¹÷å1\x0018Ý·JUÌªLL\x0013¥à­²q­Ì¼¨Þ^W¿×&¦½Èí2XU1±QC\x001bÿÜÛÐ\x0007þ\x0006ZU\x0008\x00109ÛÁ-×4¹I\x0004Jj;ª½}"ß&\x0002D+\x0001 ¥B$ßkY´º&@lÀ@ª\x0015sýÊ¹G}l3\x0013Õt|ÍªJ\x0013\x0001"\x0007ÈÅ)r$áqü\x0004Ü#º3`Tï Ò(÷_h\x0014\x0019 ÑÃPõÒâT&fEÞ\x0012o;²c»\x0019\x001b©ùG»·ý\x00192¨úÓ¬\x0014jrW±\x0013°¼?\x0017»3hè^U½ÿý­ìR9ãÿññÛ7·w?\i:N
Ä\x0018Æ\x001e-Æp«ÍÆü\x000cVÅIþû=ý´GUÒc(aËÆ\¶pºPÝqnÈ\x0001X;cÈ5Æ{\x0006®q-±½\x0001¼¯)¨×ªÿ=ÄÅ\x0007"]\x001c©\x0007\x001dÇMº!\x0003\x0003Ü:4/³q¼sÄØ\x001b\x001dþ¸K7d\x0014÷µ ÃnÕ\x0003èð1u½êã.ÝAcÛx´/vöý±c³5<îÒ
\x0019vi`TdÕe
ÅÒ1¹°&UnÈàG#×sAd;íÿJo¹lË8\x001dY\x001b2l¯÷âûxM\x0001ïÐ@\x0001ÏÅá'TÍxª\x0003ËÞáA\x001bëÖ\x001d\x001b´ýèQíBP}n7èT9ß,SMÏ}nQÖ¢cq\x000e\x001f
}¶¨Q±Z°Ò8<ÔåÝ
Ïµ<ëº¯p\x0006åxÛ;\x0019.Ð.³Yã&(aI]÷\x0015nÐh¯>ú
\x000598Ê6	2ã<q¶¬-kÇn\x000cW©l%OhÊ\x001bÊL7æôâåÙ¡ÑL\x000b\x0012\x0005æ#0CÝyËó»SÖÙ²vö£G}v\x0007%¶\x000f\x0013.«\x001aDÄTs,\x0012\x0019í=gG58©\x0010ýèO±ÍY\x00189?\x0016}mb2vÅË¾Ü¶ÄËnV{p\x0015¨¯\x0003-@ê¹{qõ2)ðªÝEµß½øÝÝýÛ÷ï¯ÕðQèm§LKÐÓúúG2Y\x0015]RÛ5\x0013júñ\x001bÞØ\x0008-Ñ4]mbÛ¥<ÉG\x001buùËR5½CC:\x0014ûÄ`+@Wî\x001aJ\x000b¹Î\x000e
,'] *l£#+Å"'Naè.|r6ê\x0002£\x000e\x0019-2¤ÄZÝ)\x0011uB%V!¹ÏÿphÅ¨üîæíâð`¸o0G¿7\x000bTyUÃ©\x001elÏÞéòüþf<ÅáM\x001d
M*?ã|aËp\x0012oÀÐ^¦\x001aÎàIç\x0013=Â\x0003\x0013\x0011s>1ºÙp¡\x000fSûWÀN
3¹Ù»\x001br*ë\x0006¤
\x0019leÐôÑ.lnd?Yu\x0004[7bæ)
×ÞQh\x0010Ôr-\x001b¨\x0016îÈ>­Ôf¦wç¯~ú;O«ißÞ¼ÖUvÕ®®8þ²é;Ö¯s§òÏ­½¾nYTælO\x0003·Ä¦¸°år¥ä®¦.W?©[Ï)Ë³yrV[\z
ã¶9`Ã´\x000b¦U`\x0006¶e2¨ëqé¢Ó¡¡~+\x0001#p\x0013JÒ¨
So]2î¤Àß ±À/ñ\x000fÎ¶\x001cµ	ËáNÝ7®tìÅ}×±á¾³! Ú\x001bÇv¨û]=¶ðÖãóKþæÅ¯\x001eîï~Ð\x001dõÛ7÷ß~}µ<}áú£26F>\x0001å§	"=÷vª5/ÚøWþVO6¦ÌEè]×J\x0015^ßuÊ¥\x0007ëLZR8.ÐP\x0001P®/$\x0018eõ°ÜZÍÜ\x0002©¸K:Þ\x0005\x001béx1¿\x001ckÇ¨b=ÑÃ&Ë[M!76ÞÙ°±¸°E¤Û\x0007­Z\x00024lê	\x0017\x0019âïÃö­\x0005é]z\x001d\x0003¦[dÍ0·!#aN]Úph­nÒ®ÙÒ
®mBv,;4\x000c:D`UjØj N-Ir¿×%õä\x0002sí\x0013\x0012o%¤{µÖTxÔÝ÷v%]Û°Qº¶nz&\x0017ìP¨s°NÊÉ²bÜéB}nÆ\x0019	@\x0004Ó\x000c¥f{\\x0013É\x000cGä\x0005Úñd[ÀJ[})½Ö`\x000cÂ\x000b42%ÌÍ0!¦¾V\x0008·õNÊ$î\x0006£^O\x001e\x001ax:F>EÆ %Ê|ÉÈôÒô2ó,s¶\x0019#nFy¼A§ªkÀ«(µ\x001façLLg1ágTÕ1ì\x0014\x0013v­)BQ»ÞW:;W\x0013«²Þ
bG$\x0010)§ÜNÐY9­ìÈ8#\x0005h8µµ\x000b'B¦Ô»Ï±v]Ù3ì3B=ÍgxßÎN3ÒÅ_Ï \x000bB\x000f\x001e¼¶ñ2wßQ\x0007Ï¶Ý`ùlgÜç)½\x001c\x000b$êÃ\x0013ÍôÆ\x0014Ý"ìïíF\x0007Ó¥_ß¼¹ÏE	o
ÙÚ\x0017!Õ!\x0018´aí\x0001ðÏîsqÂ"X8jåæ\x0012\x0008N`Z\x0008v\x0011FÏ!ürÖ×óò/\x000bÛ\x000br\x0005d#\x0005à¥\x0014"?èdùuËG\x000f>®\x001a­[CÏ»\x0017ÿçÃ7WËÑQ\x0017>wvcCÍ\x0017

&uáiaÿóvó´«ÿ\x0010Ó\x001eçßXÎÃª?×H¤©³![¼ª®9Ñ&$Xl·gÐ`\x001b­\x0001J\x0002h¥áB¤)\x0013t :\x0005©ñI\x001aå8%H¡Ö*©RúXûdZè\x0004Û¢£ã÷\x0014\x001cÊJ ³\x0011-
7Æóbµ7lg8·¸X+O¬²ö~8Cö\x001f¼èúìÈù#\x001a\x001b2xj\x0014UO\x001a¶\x0012mÝ\x0004~Õn~bþl¦=Ì´¶¥9^!ÄÓVs2^!=%w¶g M¨È°\x0017î8l
÷eJ¨^×½<\x001b6¤>>pÜG
\x001b|\x001e6Õfø/\üÆ\x0018¸õòíÈP\x0019\x001bçDâeÒ(5qõ-×¿ SwìÒ\x0014	\x0013¶=`I"MóN<û\x0011¿¥ü\x001b\x0015. ÃÄ\x001eYiZ­¿).úw;¶ò[bòvõ-WPöö½\x000bIB"kå¦øþö/\x001fn_ØÚê£W¹ç\x0002ñ=}jåÔK=ÇbI³Rynå:\x0019º²aS]GYgðèÍ"uWsfa]u)Ä©®S'®ú\x0012PÅ(TÃÈ¥«
¯¸¿->
]Ð¹\x001a½åûYY\x001bô½z\x001f]Ñ¸;6Öç2ø%É÷ÌTT2pàµÐ;nÏf\x001bµ\x0002ô\x00069\x0002ºbå\x0014Kj\x000f¯£\x001bØ\x0005\x001a/ÿD£Y±È\x0014ð\x0012Ëmå ÀÐåì}{ÿðº	ú}yóöîZcæ¬ wÁï;J»r@øÄÚÚ\x001e«@ìx,¦¹ÔV<ñÆ³]-<Æ©Í#SoN;VÓÜDj«\x0006UÛ\x000493'JV\x0000'\x001b$|óËzXmUÅH ­cáf\x0012Y{GVÏºæ&V[UqaÐT%\x0018!é\x001dAæ6püºæ&V@aGDm\x0004nÜ¦%°~´íýG\x0002XmÕ¨32Ø\x000c8uûXÐ}ï.?ÒÜDjSãè±¨MwÂ^3:VoJèGê\x0018m­ùÎVëç¤I3w±¹ÐfâHýq\x0013£­7­\x0001²jR[_ >w¹WÊ'¸\x0018mjSêíZCïøýÜ÷Ù2û\x000bF\x0018m­\x001d\x000e\x001a\x0006±Üy\x001d»ÈDç5£ÍM¶¢Ê\x0003 Xî\x000c\x000eæà\x0008zSy=ÛÖã\Ù¨½\x000eT0pÍ´¿rrJ`\x0007ìä9÷¡ß¯ám?x\x000fjÝÁÁr\x001bä¹²HÐÑ\x0008û»'û/¢È©u2*·ì\x000bï\\±@Í\x0004XJÝ<Ü|¥ÁÕô¹-'¦CÜ/²¬$^ø%ê¦ôì¡á¨´\x000b(]Ò\x0004H§µ\x001fÖ{hX'®s`\x0019ýX|Û¢\x000bæ_Ã¶Èüs Ñ\x001dª¾\x001dIÄÇÕIý?4¦_Q8Ã\x0008²²vÜÀyèT\x001cTºcáýßõWÎ\x001d»Â¸SB?\x000b§W2c\x0013rð«¥iQh§É¾xs#ùþúÕÝµ4\x0014Üäþ*kq\x0017eÙ ¢G.MYî\x0013PÚYF\x0004¯JÔ\x0012\x0014Ê&\x0016¶A³\x000eÒ\x0001\x0016¶\x0011ã«¢lK\x0007b±L$þ$mèmXFW\x001b®\x0007\Æ-ÚKÑ-ldSÂÁQàèª¨FZÆïèQ\x0008G3\x001b·\x0014\x0012]mÈãx×B\x0005"kO\x001b";&ä^Ø:CNìðâÈÚ|\x001a	
$<^wölÈ#¼òÞX3WvB/ÎM³\x0011lZFX\x001br!dP×Q\x0011\x000f¼«ÓéÂ´%L\x0011VÌ]Aoÿï:\x0017\x000c¯
ß\x0019¿\x000brL",õ]cP¢@~»©_þ»Nz\x00066hØ\x0012\x0012'XÑe\x0000¼Y\x0015Õ§\x0008kMX\x000cV&µzCënºsô£®#¡
yl¤=d0æL²Å1ÿNgú¤c`C\x001eK:Ù²Ùp\x000cè)"{`á%"Ñõ2bù§W÷oîô|¼âµ¡Á¸jw\x001eºãUå¹Å:×,ÖÀ^û\x000c °\x0017õ¢ñ2Û\x0014ec¸i»n=\x000b]ÀÀY²¬\x000b>¢\x0017u$ÎvÖâ\x0011A7\x0015`»HµÆ\x001e	\x0001´¶® \x0015µ!+à,\x000bG}±õ:Ã\x000e8lðmÒw »](W M7XU;tBèr\x001bê±BLö$Ò`Vê´vQØnÑÐgÚJy­%\x001f¨ÉÅê/TÖ¬.ãà|­îÏ]Û^Gèµc#)sKò\x001biägcR2\x0018þðd;ek!>Ü Ae3\x0019O\x001eª>Ðe
÷fªehXd;¶ElU\x001eN§¾\x0006\x0012ÕÎòâ£Ý\x0014S¿ô\x0016Ê£vÊ\x000c\x0018ö\x0014¡û\x001e\x0018¡on¿½ýñj2g*e
c±Ñb­¼Ý·'h_i;Û>\x0001k§\x0005\x000b(·&kÔýPo ýäÉòÄâÀT\x000bLøË7\x0007\x0005	¨CCz¾*Çª\x000chÃ\x001fXõ\x0018Ú4¥Í%qFå­jAWR g-\x001eGkÞJD¡Aï_Ô¡\x000bÚ@ú*32
:n\x000et2hd×ìßz\x00059±9_aÝ_é'£¶HÈ\x0015$\x0014µmî&-}ÑÄ\x0010ÖÀ\x0005\x001båÈ4\x0019\x0002ØªaÅúXÔmccìZò\x000bÂ_Ç\x0006qíÍóäÆ[p.ØPÂ©êµ»¹Y\x0005ë8§V©±P	\x001c
{aAÞ±\x000bÛâÚÖÌ%Ë¨\x0015âÉÚxq\x001b8ÁFZAU;±\x0002­\x000b\x0014XgfR«LõÊÅ¬cÔ_¾¹¼fï_áönëRÕe\x0002¼\x0010z\x001f?»/Ë¡ÄB2#ÌÌ¢\x000fë¤m»¼\x001a\x0015Dô±ë\x0016=3\x0005©mb\x00061P)ÜÓI¥i;ÕmQÊíÐ¸034Íë\x0019Î\x0018g\x001aòJÝØLêÆE{¹F>'¹n\x000be{­s]}ñ\x0004îØ÷ÓÞ%.ØôþÍ¬o.ÀÝwÑæÓIK\x0011Õºþ\x0012¯#3¡]6[Ó$\µùtl\x000c\x000eü°SÕÆKÎ¬\x001bÆN¥\x001b£`£æ»*´ìÚD!«Nc¥JÛª?ºÈ_ööx\x0008ø\x0017ò\x001f®fø¦ÊxtHËÎ¹´[V\x0001\x0005Ãb-p=»¥Ñ\x0012õ¯\x0001+³õ\x0005ué¶ê\x000e|\x0004å£c&¢ª-!ÿð`WÁÑ\x000e
ºe\x0015yÝÝNÍ\x0012t¤\x000f,\x0011Ïò\x0003»ã\x0007~éz|÷þþñÅ¯\x001fnÞ~u¥¸þk%¼ÀUÕâ Í[	ðzê~
o³ÅWv_¶A~Óeô¾R½W&¢¨Xùwõ³Jt8NtT5Ý\x001aé·61È~I¥ôNj=It8¾Cª
GÀå2SHåÈÌü½¢Y·yoÐ ZäRRL\x000c&kâÄ½U[®ÅÚL1ØuÑþêKÞìV\x000c9\ê(¹2{Êý·øïÊ¼q!%\x0017ORFÉI$}bbHKßÉ\x000b0/\x0005;.0	QåLb%£Ä*\x0013Z1]Õ;.È \x0014A÷¶\x000f\x001aÕ]¡·\x000ey©7vA\x0006%£\x0002$¾þ%ÙAÃR:+¶öìEíà\x000cÂ,µ{\Õæ|?|æ1îø~ÜQ\x001d\x001aaåx\x0007ý¬\x0014\x000c·¿úlï\x001dZUbqEudÈ¢¨2´|¨\x0019\x001f{ûºi6Ú\x0001³¸¡6d(Îªz!d_r5Ö	ZÃ½¥RzµÎ4
÷ÈLS´ÌtfZ¡eß
\x001aÊ¾Õ&äÚ&?{\x001dÇ:Ít3Ì\õz¤©×ã\x0003¿âÂàc\x001f·@\x0016¾0\x000bÛ}a~{ûã»wW\x0013\x001b\x0008¿ºMRnËè\x0008åS¥1¶á'Ð~d\x0017r/µç9@#Ñ ;+i+	¹OÊÓ\x0016oTeVwÍ§3ìUÊj\x0005
J2S§@foB\x0013;\x001fpÅ&íÈ\x0015S\x001eR9\x000e\x000bµcf¨%ÎèîZ±Ióâ²§Âÿ¸yx¸{}5\x000eNdWèÌ *}\x0008î\x000c¯ZF\x0010ydBMú)E»Jy»uòSH\x0012T&R\x0012 µ³\x0014Tº
ø\x0000³ÂÌ°,iÑ =C\x000elAAÙYTÑÎÉP® :k×VönRP)¦TÐf\x0011df\x000eh.1r\²o0µ%§¼{#kR?Úµã(V6)ØÑSÝÎÉùNgÿ\x0004z\x0006\x00169,¦\x001cÌ4¤ôf¼zùºeà±A?J\x001cEzAöll \x001fÙ3rã,,Øl\x001d9"2:
	4\x000bÂ\x0015½
\x0019ºY
-\x0012o\x001d\x001a{(ä^µ0jy·\x0012Éy\x001as'C,Òn\x001d\x0018;(¢Ç7¤:/QþEp\x0015ùg\x0013óï&\x001d\x000c,ÀÄ\x0005í\x0012*%°L«fµV@]èÍã·WÛE¤Ôì£×´Ýö+Ô±l°gäÿ<»\x0017ÜèLð¢ÏÄÚ©¥Ì'\x0010ð5²\x0019FdÝ}\x001fº+õ\x00192µ<\x001b$@kMºcÂÔÒcÝ
\GÆ^¼%G\x0008lDÇ\x0004Èhªâ*\x0011Ü°©ç¹\x0016ØEò1»ú8,\x0004ÃØ~ó\x0016]\x0010¸º·è p\x0015Ù9ÆÓBAÑ\x0014¹8ØxDî\°=#Yð Ï{Ý,MV]N\x001d\x0019»L~
%ÎçJ%ÊRìÊ¬+-);%uçÀ £ªXÑ[\x001euiMN+k\x0010;YÈñ_\x000e¥J'\x0018ñ\x0016¹i²?¶:[ê:vüçÇW_¿»¢\x0002¾#ÿ\x0004­º=v·eÔ?£iüÊç.5­¯é\x0005I¯Nù,ó\x000eBõ*!L¢^6Òê	ò\8!ÊÖ)Á£ie\x0010"S¦,%xÔq[9hA­\x001cöÇ\x0012 Ë³Å©eP[ýsAþ«Sæ(ÉÁ\x0015\x0011¸r\x0016ÆTÖÀ\x0007NZ3e+G¥\_â\x0012Éì-n
¥J´îÖDÙ:¥¤²ÚZ:@®\x0013²Í<\x0019náêúY'!\x000c&ËûëýæõÛ+¹ò¶ä\x000f¢½Ôjåÿ;¨UÚ\x0000Z¹HãåRY\Ï~Q/<ñ#øZýÉ\x001f½jRvÇ3ì77¯¾¾y¼R\x0001¥h\x0007\x00035\x0007Í?¥4iÕnQû§ðô]Ù\x0012¹©VTqÏnÄ\x000búÞÊ/OÕ³%¨WýÃ
\x001bnÖõÌ<9©
½xgtèÈÐ£yU%Q}K¡é5`7¹ÃçV®\x0008ÝÃáx@Å,yØ~É¹,õñÅçòÙõløüîöáZ\x0014·\
ý\¯.îã­Ãð&kâà¹£÷5cEb,L,>\x0018\x0012£²¬­²=ÜÊËI\x0011ÎÎZË^«ô§Ê_\x0002Í× Ï½Sô\x000c¹0²\x0003½²§A³ýÏ>i\x00165lßO>çKáÕY¦HØÛ
ä¥]¦nQ\x0011öû=0;6¼¼ `ÜÔãViGùÒ\x0019\x000bê
7ãé=#_!2fRÌö*Ø±$]°\x000bÏG\x0005ìÒ%¹p>(|/jºp±YÔRÿåöíÃÝßê\x001e»»ºXNeÊ&EY/\x0001>M*WÙ>ÆÏÏäXx\x000cL\x0015T\x0019»m5ý}ìË)SKül¿°óTB-6\x001bL¢\x0006Y¢Ä®WÖ\x001b!W³\x0014\x0000;Vn\x001e_|öF~ø×·\x000fWbp¨`;.5×¨¬\x001b\x0007B.¿Át©ÀMÏ}Â¼V
;S¬&}çÓRµ\x000cðp¨±r··6òi^)6h^ÉÔ\x0014|$\x001begFVî¶½¢èVZ]
\x001b4\x0007µS\x0017®&8KSCdëYgÜäò
ä¥èÈC\=ùpÍË¸'ããÖ\x0016àVÊh
:â°K»1.Ð5ÑãO\x001dx¥ù.$¼ëjØ9Ò°AQDî\x000f[
Í±]\t\x0005¨sý?L»ï^üöÇûw÷ï¯¥"ïEò{
MyãòÒÌã³F£ô(÷Ül¿Ùc`jÛ×l\x001cÙÎ¨ö\x0010ìÇç(8\x0008ÑåõQé§®]9d#x\T
\x0006jÑÈÉØæù©»V\x000fY`÷h
¼å&\x00062Ë­'»Ö\x0017ñS\x0007lKrìV\x001ak\x0012w|YîÝjÖ\x0002#~êI\x00061'AÖ\ó\,ÈiU!s«ÌÛ£\x0016m¿º{{w­#g\x0016°Sk÷Ó(¶{¶¼ÄM7¼úù3û\x000bý)ñVµCZÆ>ñ°s\x000eë¾¹s/êÁõ\x0010\x0016$ä\x0012I<Ák=ÕÂõàÜU\x0013ÎG=ØÉ"\x0004\x0011<­­\x0006\x000ce2§ôb7B_\x0014m§ôX\x0003:³±ôW\Ïk ¨ôLé1	¾Ð©C³¸ÄTTÚ\x0008\x0001'³n#ßG\x001b¹SeÇ1d9&{ä\x0018¹i·/tz*3ÁÉÂ8¿­,tdÄ*ãvÝC¾áVbzNK¨æ×\x0004õDJ§AC£·Í /#©Vþz1Ø\x0014\x000b'Nü»Û×oål¹¼R*¬8ê\x0018¾Y±n
i:÷©\x0019Tßõ¹	ãë\ØÊ!©r\x001d¸ªïqôHâVÌvÅr\eÿØ
ýc-Ì\x0002æcÿ*Ò¥R­[Âv]ÈgÑÑ±Éµ<ÁMg/¬"Q<5\x001dEï»ßÝJA¦NÁy³è\x001eÐÊ[&a±ÄVzÞ§eDç\x0017WÝß!ªã#?ÄÑs¦\x0018!ªë\x0017ß'°2\x0017!B$­\x0004
rIÙO41Ï²âÊ\x0015Y\x0007I~\x000e<¸»\x000br\x000cSõmzS£¡/Öd\x0007F+MgÑá)É\x0014(\x0012õìòué;\¢\x001d\x001aëb¡\x0011ð.1®\x0016ÈÁÙ³Úkôyy\®zâß)«âñ»ë)WÉÎ\x000f|z·îÂ¾»\\x000eàÜ.AûÜçåt¹:/'åÑªª\x0005®-û\x0012;/ä\x001dÏ÷aj¢»«bZ×«.aÔQXË§²êÒX[çúñù»AÃó×BqÇ¦\x000b±CÛÉÞ²èè\x000cÅö¯÷ï®¨"\x0012üô^óñÂÊÉ*7øÿ&nÄ«Oò\x001aæ®\x0008mÍ0ø2if\x0004Wùx\x0008Mæx:¹-¢FÔõVCK%1¦rì\x0017í1xßÁ\x000eOÙ[£R\x001cc!æL\x000e\x0008\x0017aÞç{\x001b.´¥\x0014_íÙ½d`ÆõkGê
\x0016(ïÚÇ\\x0013\x001dü\x0004¼&¦»u3ò¿Ü<¾÷â«ÿú÷ÿøå\x000fWãèqÉ/ ··$ûà\x0007\x000fMÙ´µmÝçÍs6¿ª¿á¹:\x000bªéàá&/ÅjøM)Ï\x0016¿~­Îzj^\x0015É	l\x00037MÈ¿W¦\x0003míÿèfE5\x001d2´cx×)Çø­&ñIÎÇÍj^âÈ\x0004gpæxF&cJY4ñÞÅsu=\x0015=:û#-rÅ­åUÙ\x0012§\x000b2WÃvÉÐtÀÍa7½9Àf»{\x0013ÂIâtÃÆZd$»t#ãFyU­e+ºh\x0004øL®Ü±U{¡ùñÅ¯n®%¥¢M!Ô \x0007ÆÅ­RÖMC\x0017JÞ¨¥·	}\x0002\x0011öÑyãK©/ÐyCïAS¬-ù@Éº¡P8Ò÷\x000bÿª]\x0001[ëª`eÝ\x0015Û\x0007t¡Vó\x0018r3\x000cq\x000bí\x0006í\x001c@+¥\x0010\x001cÉ-\x0015Ç´¿X¨Qþv)-¼ÂB¿D\x0006¶æ|ÍÂô	eÆ¥\x000e*\\x001eK6-ËcÀÎÙËc¿½ùó\x001cF½Cß`$t\x001c©ÚZì³«X£ÊªÄ¤T\x0002r=ú'øñ\x0003t\x0013ÉE¬úo·\x000fwo__ëênySº\x000e\x001eß¢\x0012Í¥KÿüõçãÁ/Óõ\x00057Ð¦ÈgCe­R¸\x0014]ªeÙz°AcÊ)Aó}T@*~¨\x0007;¶ëªÿ«¬>ðãÿyûðÍµ\x0018F%ðÅéÌè\x000fpÕ÷lëý
Ï]1[3qY1s\f
¥ä}B=Ú\RæçàYÅl\x0003¸Ì\x0016ìÏö¾pÛ`ÉÙ\x001a®®n7d¨"lò¥ûë8¼êaÓ}b»\x0016Õ1.ÛG\¦­o`¤£\x0011¥1³äÄ¨~ÝU¶!CB\x001b2qÌC¾bòTS©ëoCN0\x001b\x001e¨½e!ÐlpýË¹uOù\x0005yT\x0012r!ai¨Û<>%åGM{¢®{Ê7hÌÑÀ\x0014&Z#`ìJÉªu;EÀ«¼jY(´&»ßÜ_-è(ib«5*ÿvAE\x001e"Éçg×u\ç¯V¹mÖ\x000eQÿ
"$Ö\x0001K²ÈX«6ÕFK[	7è
Ðò\x0007ß&ªB7w`n¼ÅÝYºßQºÿ\x0003±\x0017a\x0019\\x001aÃ¶ðdb__+õ\x0019\x0013çã½µ{Dx[½ÿÒ8y.¸ìàö=¨êÔ#\x001b\x0014lïäÞ»¼»ÂfA¿4ySp0y§F\x0000E\x0001£a\x000199ËRä­±KÊ.Ø©
\x001cMXµy\x0002\x0008.6qZH%¬é­)QKgc®¬Ø\x0014<UoQ±QªÐÖRòä.;@wKÊä<ÝÌâoÞþùæý"VuÁ\x0018.ÏÙæ\x001fô2í\Ø$¡vÛt?Äº`ÇçF@Æ.\¹\x0004b­\x000co.¹Æ\x0014kb·
Yl\x001d\x001aÙñ5\x000cñdgI6Y¹¬°.U¯Ãß©7ÃWÔ7W\x0007
É½åHÛ\x000cZO´W1<wºbL\]]®®R[Ð3tåÉ²WÍ\,6µò#:¸«K\x001e8%L­®0 \x0003õÿ;%hUÁ'\x0015U	b"4à\x0012å*µJÎý>½÷tÑkÒ¡Iîmù=\\x000b'm\x001d;!¶\x0005#\x000fm\x0000ig\x001c`S´&ØaM1ß á\x0001¨fAC	¬\x0004Õå§\x00191TÚu)ÆbZ\x0005
 
Ø!@÷©v=Òj\x0013èFì5}=/6«\x0006ÿ,[áJ'±d×ÖÞ{£«ò\x0019v\x0014UrÑÜñÏ\x0010¯µÑ|8P7Ø\x0018n\x0012w\rl4e­c{Áö¨}á01®P\x000f<Î&ù]·ÐµvQÞy|ñ;¹i_}}-ÒPrlrT^ôB¸Mµ\x0004PLÕÚVfû\x0004Ò\x0007\x000bñ';Û75~\x0019\x0008\x0010ÊÙl\x001cj¦Ö~¦­z[FéèmÉòÉÀ\x0018N¶~j!É-Á\x001b}a\x0013\x001a!Éaû­\x001cFèrKjõ¤òÅxGÊaÒ¤iV}D\x001d\x0002`Ë¡\x0016Æ¸|à\x0011;$Þ\x0007fóµ]ø67ìh\x0000ÛcoüGK½UÉYmõ=p\x0006\x0000ZânhDÈò&!e³d)aÓ|Ü\x0014úl¶\x0013Ì¶¬\x0013ðÍÊªÂ°)©`\x0001aw¡|6Û\x0019f»H°Æ\x0011cÕj\x0016gDN\x0014Ú{aù\x001e4\x0015DF0Kü«¯ïß^+Eì,ëú\x0014v.r4\x0001ÅìMè­\x001a?ÿ9¿*àÕÙ¨üdôOþòÖz]?\x0012{AYñ{üÝÏ\x001f®\x0016o×DZÏ^B¬È\x001c{\x0001$µ©þ?÷{ùy\x0017êr­\x0012F\x000b'ò\x0010zq0~$öñ\x001a¯\x000bµèÇ\x0017ßþøþæJýu²f«­ks{ö'3ø<Z\x000e-'õ	ÔÙ\x0016ºÕðölôOýðÕþZñd4Nþ×»ïïn¯fg"·'5ÄT[vjsVI£wüs;aþÍAækJ-þÉ_¾R´Y¼W\x001e×)?àõõ\x001ak´Ï\x0012Gc¢uû;7UYTöj\x0011þÃn%ZçÜ¾·`ðÚ»A\x001e"Â\x0013V¸:F^§öØfQ­Ô¼®lsö\x000fÜ#äÃF×èï\x001fnüêjvVÄª\h#[ÏO`\x001e f\x0012­
ò	ì³3T6L¯=\x001bþ?}\x00151BÃÉ®Xû»Û×WóVH >·jÍÑã!ÏùÙ{O¾@\lªm\x0015\x0011d-NÿäO_¥fàÊ¹Äì*ÑÞÄÙo®'Î\x001e¹Ã^}mv©
ÈR£7ûÜqÝºù|5ÌíÊ\x0001\x0005nM6uï¯`íclß\x0002»ðà\x0006
\x0012Ü\x0011ºRää¨\x0013iD«<ë\x000cmS\x000eÕÞ´®%LGªóò¤üÞ\x001aæWÙýé
V!R9´Hb¹oA\	]Fy¡<'\x000b¬n.Ð°6á´]ëD.ìN1gSB\x0012ÜÙ"%¢¹="	 ¸I9<.ûÊê¤!Üïn¿z¸}{-1¯R#E2Î\x001a?
\x0013Êè\x001bÏù\x0012ê³î§\x0017eÅ;©Ìï$5FÙkfÅÔ@Bèòo±É¦ï*mGC°
\x001a\x000cÁºÀ¨xÈVc³±Zè\x0011ì\°§Ix?'ám\x001e+S°aÝÊÊ]®Îeßòl«ÚAkY\x0002Öp1ehíb­£U¯¸´\x0014¼÷*uÔN»`£_5àW>\x0003Ù#\x0019n\x0017Z¯ëû¹A\x0007xÁê-\x001eX\x001fXµ%	Ø7u­¸ªÓèÿ\x0015¡Nc¼\x001fõÃ&ÏÐ
/m·]gS\x001d§\x0017ó¸TeçÐÚ\x0005\x0006vå\x00122Ú\x0015ûlª#\x0011õÐ\x000cFveå\x001eK0\x001e·©mÜ+²HÃ®\x001dl.>¾¤=ULiìà¸È\x001cmÈð\x0015»»ú\x0005¹Z6Ô®ÍeBê:WÚá1CQ¦\x0019¬ñ|ßÓKÅ^Õ­\x001a6ö³&ûr@«î%Ñ-++öº~q¦UÙ´!;\x001eµÅQ3WLGM+DojÀ's"\x001fP0KLå¬eZ}¶ÕM\x0017éã
;Ã¸åzClÛ³É\x0003Ýsd¶{júle'\Ù\x0005¬B\x0004;Gâ)ê¹Jh»ùJ£¶cW<XK+g^°µ\x0007\x0006O(¹høSÖæ~Ï¾eÆÎdé9é§d2å­ÐáÎ ¡\x0004n³Çz±Îì*'¥ãé®«ÊZ<tÞ~sÛÔÿÞ½øåã»w7­ÍôÅ¿ýô¯¾¾ýöz©\x0006R
rÑî}Quàé\x0011z0ù	pöâÊ\x0011;¶C\x001eÌ\x0005Æt{9ù?ÝRÝ*øØ54\x0016Ì¨
F\x001fr\x0017C\x0017N\x001adF%Õ7§µ\x001d='ØL¤AÿN°7@À&Ònhææ\x000e\x001fHn}þøc\x000bOÿëßÿã_dv¯Öò¬LïÈÛxiÆÁ~NÑg×F:yu§Cð¥Ì~\x0003\x0008\x0010NÿäO_|\x0008²½}-?ùÅïd+ß\+ñ!!åc1ç_\x000eú¬tô<xn3´³ÔÓÂü9Ú©¤­Ã\x001fåÛ}øøÓóüÓW$÷äø|÷â7÷o_?^«´ùÈ\x0013y§¥¢Jÿã7xy°¥ç~¢-U\x000e×¦|9ZR\x0010ÈZ\x0016ôIÞÒ\x000b_óÚ'u¸î7l;®û¤Q1<]Õî¦"_Af6V.!ôÐÅÉ*)©þ?\x0014çµéó¥r\x0000·Ðí¨ä·a_`
Í¦½\x000b8'ò\x000f3;©äæ´²Ð·nØ\x0001ô­³\x000f äåÃQ\x0012U\x000f±U)_ï«ÕfRì\x0008¬\x0002õ\x001c.Ç9nÎl;6E@Ú\x0005RáýT\x0008UKK\x0015¹?Aûb,ceLxEÒì\x001bÇ\x0001åÑ1aÌ5ÓHüY1á
1aR7Ð\x0002Ø¹	T\x000chê1±Zz]-TÝÎu- ýÛÍãkåre\x0001\x000bF¡Üø)I«íÏ}º(©äo:^z\x0002\x0011_X²püèq>\x0012\x0019Eã7V\x0005é4#üdé­¯¾Q'W3\x0015KÉ%UQà\x000e"ß\x000e®CªöËCª¶jÂg¿dÊ#_õLán&~xI|yHÕZ\x0013µ=\x0019OÑjÑÄ$!Ûó<\x0004«\x0017è¼NX±\x0014Ãýe&&||6×vëÑ¤O-<XtB¸Õ=\x0010u/Ø 2]chFÌ\x001b¶
cá\x0002IM/s-wö\x001d-xýT9Çñ;¹ÒtéÃ«ã\x000cêÕ5úak¥ýùµz\x0013´iJInqÖ6lg`BTo~¬\x0011#h¦ÕÇ2\x000b\x0016wK
ð\x0005\x001b­Ùµ±éq\x001di\x0016\x0008v[«[sÃÆÙ.CvX°S|Y\x0008ÛyC¨­;î({Æ$¡Ü\x0011ÐÕ.ÿ\x0014)O4
(öK¥\x000b4ä[²­ÐD\x0019¿R<W|ô7k>ölF¼ÅmS[W#¬?Këoªp­åóì$ñP¯\íÀVbrÔäi¶\x0017ïÇNMÞ.·ßÜ6uÀ÷/Þ43±wïnÞ¾¾Vé6°K»ÛO²ÿG°U´q*?3Ïï¬%ÿð\x0019dº¾`¯¸Ñ?õÃWsxÅïóöyÓ^1W{Ä°ùyÌu]l\x0019rúyþwä©ö"³XóüÔH\x000e\x001aO³vq{LÕÈv	üÓëú©±cÃSÃTÌõkë2ÑM¦µG\x001a\x000bÑðMO

i\x000f\x000155¢6Ò¸i\x0005g·òÀmØ\x001eÇm s'+\x0010äÉHín2'eùÒØ é¥!'ðhÍª¹\x0011R,¡euÐ®;6½5Ô»\x0005Þ\x001aÅSÃQ,\x001f\x0004Êw=I@wl|l8ôøÈÙvcÀNü$PýÊu\x0002ºaóc#a\x0002:ÏãÎìvçTþVËðîÛ5¶©îoÇB14+òRÞâ$¸|±gàÅ"¸\x001c[iäåC©äÃ\x001e«£ËÄfß\x001eÓÞ¡{?Ð³AEª \x001aMVu¤\x0018\x0002éÙj¶x§èÑÑð#ÉJJ\x0002É'K;ÈÕÙöÎéÇ·w¯î¾½y£'ÜHÖß?¼\9ôÄUÂÁÿÇðÖ\x001a³sPõË
-\x001bÝáÕª§ª©,âfnõíý·ò?»kÿ\x001f¾wc\x0010ÿ¿NÜé¢åù·ñÇøæÕwKÃç·¯¾Ö\x0016ÛÇC*¹S-æûÇ>}ÿd-êÁA©U©¸QUåý »~í¶®.G\x0014Éöëÿ¾a@óÔ8¶³4ÄeÆ¾@¯K\x0019D¥±¬\x001a(`À,¿=à\x0016r\x0012Ðmw®º _`6t«â!\x0019Ð#õwÊÌ9Kj¿ø²|m^}¿\x00084~õæöÇc\x0013õ}dg\x000b÷È³¼y·!/\x001b4×ÓNV Î\x001cRª\x00039lþ\x000c}¶Zb`|ºå½.[º§|\x0016äpÉ®ÍÎ0¥SìtÑ-©Õ¨	ãþXí\x0015ôBØ\x0018	89îÛ\x0019\Â)x	\x0003\ã¡2ÀÕ!¦"x@FSÚ]HB\x0003ú\x0010\x0016tÕJ¡'Ó23\x0003=Lè©[¦Oº\x001d.c÷Íä.OX¸Wuìø\x0012ôÒ®>ü)zò0í\x0015wVi4íÁ\x0013ºïr.ä3t\x00172 \x0011
zÉÈú\x0013tºX
aÅÖçeÏÐõO\x0017tiGí'öÇ\x0003ô\x0018°­ßÙ[\x0016BÞ´gè¥±\x0012çîK¦ÈEv6Y%)i±Ëwjj(þ\x0014¼ú\x0001îL\x001cD ÖòNÒUDèòÆmÄÂÓ±[\x0003cW¥¢q\x001aklt\x0014	w¢gøÚÌ>ìL.\x0004øA/\x0014x9\x0007ôkÑØ,ãg-\x0016¼3Þ¶%éí|ìðÞîwZî\x000cªhÉÞ\x0005½bÙYÐsß¬3-\x0005Ð\x00071åô\x0010~ò\x0000oðùl»¶?]à³C\x000fR$Ú\x000fë\x001cI\x0018+z\x000fö²=\x001d|¶8x3"UÍr8,ÙÊàñmàdnb'ýÕ3ð²[:ÈÐ-¦9\x0002å\x0002\x0019::PÈÚ¸®%mÖö§\x0001î ¢¥´ au&hÚ½Í\x001d¾ÃW7\x0005¤Ã«®\x000f§\\x001a}ÑT
¯\x001a£OM¸e·h\x0016:úJ\x0013¯äÝ\x0006_Î.¿ö§\x001d>£þ³jJ ¡Ià+¯É°9$ÖóÉ©89>bD6.(eBÒäÐ_ðò>oÚá\x0003j\x0017i\x001bÒôi#EúNK
>­y7Ê\x0011
Óó\x0006ßBãLðH?\x0012xUà£¿÷?\x0004ûÃ7#úûìáæñÏÄÒ\x0007Æ|·xõÅ}ÇêÙ»ô1ËÂd©Çg\x0008ìå»ò\x0000&¿OÑ\x0017(úv:ü'z»Iæ¹£[k?\x001a=Ï×Ô@ÏæcÑ½?E÷þ#ÑçeùUýþM_ìØü»»ÆSuØEËù-U\x00128&òñRj­E/0eÉ55÷ºg}øF%<¦@§\x000fÒ§­åBöëK=UÇØ\x001d¥A²
6P¶Ay\x001d-Ò<EÎá£Ë|¶
ä½j)ñ°ºØc\±j)+Z\x000e¿{Þ¶\x000f»aËX!ÕH\x001fè'êj\x001féÑ#Q]«9ÎÙÁ­q\x001f5'\x0012ßBûòqÐå|Ôå#G}¹\x0001Ú\x0014ô\\x0010\x0005èQ\x0012ý@h7¿Ð\x0006´Ë\x001f\x0007}xÑ\x000fèñ¢ÿ0è|ºmFÕòC ç×%ÿ6¼_0[n_üöñáæ}ós¸Ò[¨KLfß=<\x0008ò>\x0018v\x00055È£Ó¥g>t]#\x0019\x001eRBv^}ÎÐ5ä7«Ü\x001fàMS£ªqàsJ¥ éÇ@\x0008ý:ÐÇ~­¡vh]Ð½o]OûÔVçyjs»åy{®\x001a_@ìXþËº°õøpÃîÜ\x001c\x000cb<\x0007\x0000î\x000b<k(\x0005M\x0008\x0005<&ÞK)Ä9z¡§F/¸ KôhÉ\x0015
¹³iº?1Î7) 
Ñå
à\x000e+g\x001e<§Eq\x000b°GyK°
ò]ª
ÓELM\x0014;
¼{]/Æd\x0011<Ò\x0007ufJ\x001dXT!u.å\x0014\x001bú|ê\x0000z/:\x001e9lò4ãä\x0013¬Ð½/äB\x001cÐBÔô?ì¢¦pJ3î)QæR<\x0014Òí\x0017ßÿðûG\x0003J¡{ûóûÇon|¸?(|Ð²OûR6ÿöK´r\x0001ý³\x001ehÙi\x001aã¿ëD¿LØ\x0017Ø^[
z,þ21Te)\x0011{'MsL6Ðc\x0018è®B6·\°§"©¶"eær×\x0002K@uGO#PÕD\x0001¦\x0015£\.	Ç.k¢­S·2é|¢íèú§\x000bº)y\x0010\x0001\x0004]\x001d_`ì¥\x0014G\x0001e	Q¦¹\x0013øö§
>\x0005kÑ·(ï´\x000f¦ÆtC)çÃ|¨íðú§\x000b¼¤\x0006¯,Ë&Ã°!eíµÄ\x001aj÷6øt6õíO;¼úî4}²\x0011S®\x0002Oy?+×\\x001bçàr g?Ð\x0003xÚëà\x0003* 'm÷²Óà\x001bO"Sø\x0010\x0000^©cn´;¿ààsæ
o|³Mñò¦=oÚÏí°¼,z¹vAÓ)exÍ¼¡-Ëö§\x001d]B\x000eÜRú\x001f\x0011ì\x0015½w\x0014Ã¡¿£qèG	5Á@M6lÅF%')G-2¤~HQ\x000cô¢PñÖryÙR¶§ºÆIKÞ\x0005²¥lk-ö3×\x001eá\x000bÀ¯\x000fã'\x000fòÆÀ;=*=\x001cÊ\x000eÄ\·	§Þ\x0007^ô%·\x001dëc8ý°ú§\x001d>¥ÑX¢ð\x0019\x0013\x0002ï"OÎÖ\x001e\x000f\x0019é\x0001\x001faU\x0006lAk\x0015\x001eh\x0007NÚÈ2\x001d®Ó\x0013\x000f5Ç\x0001?j²p,Ø³\x0015Ó/´.ÉæHàK³üôéðpÛáÓx¸Éª RThÄÓº6Ui\x0001 ö\x000c=17Y.Á\x0002è²L!xMÙ¦B»ºÍM6gçMû\x0013Âl½²ïPXáó\x0004ßÏ|zQµ?íð\x00113ÆòüJD=Ñpkw\x000bîó!²\x001fð1Ñè\x0007û¹hv½\x0012|J\x0014Ãng½/õtrôOãËV\x000cÜ\x000bTqú²6rª÷©ûzÈ
íðµÂº\x000c\x0006'G"p¬ëº\x000cTÊÉ×ó2C|oÚG3	êÙåj7TPÖâ@\x0013Ru§ñSû\x0013\x001eÇcaJ°dP«I¯L\x0011¾/\x0007Q4ûÅ¾son~X=þß½øÍÍãwÇ¾¹\x000fk\óBùÉQ\x0011T
m/Ò|\x0002OÿC\x0015¸O\x00185sÔ¬ÏB;\x0016ÊñBÙGiý´\x000bºäÁ)6rÇ\x0012ÚÏ¬\x001d\x0017\x0001±£ã
³kÎÃµµ[ðå\x0019}yMW\x0018e\x000f&a\x0018¼\x001b9ÎÚè\x0010=ãöÍÑp\x000c\x001e\x0012o\x0000e<G/\x001eý\x0010HWæ¿E§XAÏÑS\x0013;ÿ÷\x000cÝ\x0011áGåöÂ'­\x0011\x0014T\x0004¼0vI=¾?ý¤ú§ÿf¹?¹UZ/Ô|h\x000eôè\x0001=ÎewËèÎ\x0005ë[ÄáÀ\x0007pì¡FÀ#æ,\x0004¼òR·ÝQÞ\x001f2é;º\x001ftA7 Ö¤Í5d`#³^é:±ù`kg¿øñ»ßÿ%Ô7Qéñ§ÿýþöæ±yÓþÓÍã/6¾Û\x00153r8.M\x000b5iÓÇ7©\x0012Týs$j^\x0014@çø¿Ïá\x0017àÔ¥Ã7\x0005ü®ËN5ôÓ;çÂÍ\x000bk»\x0004à\x0001øQ­a\x000bËþ±0£¶sèÃ\x001bÐ\x001c^j¼=hµ+5Uì\x0008Oæ3­*×\x001dÆìá­¾£ÛË[=µ2\x0013$ÚTé
\x0003¸ì²ap	¼'è\x0000¿ 
ê°ÅPû\x0016÷\x0012\x000b«ú®à\x0000¥aSð½*iØãÈÜ,\x0019ç¼\x0018\x0017ÛF^\x000fi¼\x001d¼B\x001aOc\x0000wòC
Nº7´)\x001cÈØ_|õúO·?<,+\x0013*{ÿöõOÿyTFùÀÒDõ\x0014Ç+Mwg«$'ôÈhHLÞîàçÝ¸É.:ü¡üÙæ¬1ï\x0007éS\x0013ðÔ0¥[\x0016ßN\x001e{N\x001b<ZíàPHÜÁ#\x0014&RS-«3)R°7·\x000bçK\x001aà)\x0010øÈ5gS=>Û\x0015<ÐWÖ¥\x0001OÑm\x0004ôïÞ,ÛIò\x001a¢¡§öhÿñ)xºÒéÆÐ\x001bÕ\x000b6ÆókÝ+s÷& ;ÌïËU	à¥G+8éÀSO@ÆCÙy\x0007@;TÒä`°;\x0011[Ã[¥¶Þ\x0018W\x000fÅÐ\x001d¼B5(ZHðËÑ\x001e\x0016hU*\x0010Áå\x001c:Ö,K¼ñß~yÌï¿{ñ=ª\x0013Ø{¯oºIï~¡GÅÍ77Gùß\x000f{ÈÈ\x0002£\x0017¹¾«ì%{d£Ux®ö¬\x0014'	W¶\x001c_CêB«)ç:zh´TX\x0004Ãîhë\x000fUÆ\x001dÝ*ck]\x001aû­:KbIÝªÜ\x0017\x001b
)§yÃíèú§=kîÁM-£Pô0\x0015ãésªXX÷¯ï_w»¼rä9,éîJË({ÃÕ`o/°ò´Wï'È\x001côkÿY¯\x001b¹o\x0016Ïaç«OX£í\x0005¨\\x0011qÉø
85óA9z	\x0006r\x0014ç\x000bgG×?ÄG$þ¬Ëh¬#èÓ\x001a\x0010¬\x001d¬\x0007òÊ@\x001fä¨rqÈ%G/ÍªDçj\x000frëéÄ¸Z\x0001¼Þ½f¤>¥\x0012¿+½\´­ÇütbôOcÙ`¢HÔ×%G7,¹¦Ræ\x000f¤2@±{\x0007î]\x001d²eªªáÚNùÜ\x0019à\x001ek\x000b\x001e'F\x001bä+3åÚû\x0012{û\x0014=\x0002úÈW«üeÌyky1ÆVÄ÷\x0007ûÎ0ç9Ó]#¯Ó¬4\x0015p¢wô0¢hyQ8å¹u×\x000cpR6QðÐMÎÁ#ËÐ£Å\x0018yb$²--\x001f\x000eO>?IâO\x0010®ò=P\x0004"åè*½\x0016å¹±\x0005ô!\x0016+èK*tÑf\ê1\x0014^ê¹	*¤CÛÅFÛ\x001a#aæV]þ2½L÷³³ûº\x0004?ùÕãW¯þaiôÏ7\x000f·7\x0007\x0019ö\x000f|»¨+ö\x0018<ebÝÛ)µÃkÄþQ¾jÛY@Òá°\x0005ún_u\x0015ö[]½>d\x000bYÉ!ê\x0006Ëóã}g;À·jÎ\x0005ÜXm¶Î0\x0004ÆÝ\x001bòPµÛÑm\x0000ÚIMÁjçE×ç0ÔÏ»2õ¡`:Ð3LåÃÞ\_Uü4²v«\x000f½ätbl	Xëj\x001bËàÙOà²u¼Jvt¸JZdP¶¢'|\x001aÉ
Nq6YíÓi÷À¶¬*\x001b\x0000èfbÊÉV\x001cÇ\x001eÙww_½þC\\x0006Ý¾{wÿæJ¬ÆOô\x000eôíéÖ\x0013¢ª^?8©]ðÏÝ&+'÷*\x0012<ÔfûµÐ=&H\x000cs©²\x001a<\x001c3 Ö½z:¿ßwt\x000f$\x001f\x001b<¤=`à\x000b´3§6÷òà\x001c\x0008\x000eðQ|ÌZ\x000e¹¯ªÙ\x0013ð»µotN:1ú§ñe\x0013ÐXÃ hYëªÀ[åñÐ';°GìÙªyrÅéÕ{()ïèq|`(H¥"{Ù\x0012z±<t{ðêk÷þá6¬\b~só}ëö¸ÒæRgaÜëòæÜoÆDÍÊr\x0008ù\x0016°|\x0002ü¼CÃr®\x001b\x0003½\x0003{Ç¨A	-!	k\x001dSlïÄ3ù>L9ªÄµ\x0001"r¹»XÆ@þQnå\x0016ôÔ²æçè\x001eÐ}j\x001dÊûØ#7[+ÉÑ»HÂà¶£»ApSmMâé1K¬pJÐÐ6ÀáLÛÑ#4
hÔCzÌ×\x0004^hèòøÕwP=dÞvì\x001aA<B^U#CAðÐI$\x0014ÖÎ6ë²§OàÛvøj¶ÀKP\x0010>\x001b4Yp¼ièa ÃÉ\x0010ä\x0010\x001b\x0014õ¦KÏSÞP+½\x0017æÚáZm\x001cÎA[LÊGåÌT\x0016Õào¡Úñu{\x0001\x000f\x0010è\x001a±ûGMAÞÎÆÎÝÊzËµ±/ÞZ;üxk5øñÖJÁUdt*<G±J1mðõlÙ´?íðÑB®9\x0005}>#z%Ó(M|· \x001e¢ä\x001d=B|rP>yÈvøÓÁëöÁËæ\x001f¥¿$k/ÚÂ\x0016¸\x001aµ·4|:h#ìð)Àè#v\x001fÈo¡\x001e\x0006¤½'ÿB{¡Û£ôÂ\x000e\x000fÒ\x000bEû¡GäyN=ÉÈ\x0012@nçÞ\x000fÕ\x0001?ª+ê=<2\x0000ÉªÜ@ÄÁ\x0013ÉAþúÊõtYæ:eªà,ð:Uàñ\x0019-ðîÒbv
_àíR'J²º	hê£U/¡Jéð§\x0007BqpÄÁ¥:Ýå"­ªÖZ­~s~XV8,sÂ\x001cC2*,G_6\x0005z\x0003¥à»;=qôOãu8\x0016¥\x001aÔ$zÕÚ\x0018Ûô.úóã¦Âq«.úd\á'¾g\x0002\x0005ãì\x0006lÚnAj>öT\x000fÎõÓèmí¢§ÇôË\x0006ßþ4zÚÀ9=*4\x0000Ì6ÂË¦nÅ­\ÏMûÓ¥\x0000åÕj?,£6\x001eÐè\x000bû±¨KcÈÃ»|/\x0019+sX³ZKT²$Ñ\x000e\x0001ßwlÊûãïüá\x000føX­\x001d~ýpóö«ë!äQbÕ»º÷¯xb¸Ü·I\x000eÜ6ó'Põv\x0007i>_Mö\x0010è£\x0015{@ªfHRî,±¦lþÖau`5ïè	XÍ\x0012´k+©²
=m%J$e\x0019Ù^¶ãá\x0002ßþt\x000f\x0005ÎNÙbÈmÓb\x0016Æ:>¸Vµî@Û±\x001dá}ªzÒÐRùZ,ÆñJ·î±Ô¼wø0öotÞ\x000e:¤jä;¢C¦PP5_à7ôCø=Ðî-Ñ(¾-K\x001c¼¦|xÞÛëÖÆC ¸ÃG(shÉsw¢ÁËÑ	¯ªd®iê½ïl¡tx´íði<Ú¢V«ö\x001b7i
j4IÙïôeU\x0002q>\x001dÒý]¹\x0007½^HNýóÃíïÞÝ½}}=â.)éH|\x0014wbL\x0013\x001c©¶ä]k³ÿ\x0004Ndç=Üç¬%úG\x0002)\x001a\x000bêP\x0012øÄf#OÛd³úG\x0003|²rWà÷¶b\x001eR'Ö3zlÑO:ü\x0003}ü@/!µ^=b¨Ä¢Uæp`\x000cíèy0r\x0008HÒHj¦D¤ã\øAar÷Ð:\x0007ÇÎ?}äè$\x0004CýgÕOÑIM-°:öæíèØç\x0003Ê+iPF[U=¡7·µz ×îà\x0015ÈµÁ\x0018\x0010\x0006c±Po[õ®ðfé*-Gbð\x0005Ý"18¤\x000c\x0012äI®£V[oZ8â´öÈ³®w.,B_Ý?~uûðÝãíu¸®Iâã@e°Ø´î·\x0012Z-/GYÔKL\x0014âs3úí¢èd\x000f\x0002`}¾Zök´Hª¯Þ hWo=2Ã2½\x0011}÷P8ð#\x0006z\x0006ôåä<9¯Y	{\x000cð!\x0014 Ç!æ­\x0005}êÉI[ùcK[ûCjy\x0007÷#µ¬\x0017\x0016ÊsE\x001c¨"\x001dm!ð\x001c\ïi·î\x001eÜh'ªZ\x001bàÞpã¨¯Ì½È®ÂAq\x000f\x0005F\x0001PK×¨ßF\x0002»Ö\x001b¥?¤ùM1ÀÓ`\x0018TSAV³5PÛ¨O$x+\x0017M®K\x001d\x001d$\x000eT<\x001e\x0003Y8°Ä§áPS9*í:õ;zò\x0010È¢*³
oÔ\x0008nC&\x0006Çjþ7¾=9/þõöÍÍÝ»¿Kç=Ùù99\x000ccÜçK&h·¿-òÜ\x0012ÂÁ¿I¿©Ï\x001cë7Å,±?Vf\x0013ÑB;\x001ajk¿Û\x000f©÷\x0001\x000eT\x001b}\x0015aÃa°éí®óÚ7Ùü°\x0018ØÑ°¡7©ù6½¸<fdTÌ³,yü\x0003<"yÊbK¶J\x0016¦fqgíF_\x0007ù©\x0001^"$'\x0019vy\x0006f«Ll½K§=t\x0002îà\x0016:\x0001e¬\x0010«\x0015ùG^Òá05¨^JõB
ÃÈ%
°X$\x0006'Æ<ö¸Å³[©Ú\x0003Ïx [\x0018zÄ¼¸:qª7S\x0003©ÄÌK\x000eÃ@¦ï*¯!ÐÙL1Sÿ[¬£P·
î¡uwG÷£u·eì\x0000\Ë\x0007ÄâÉ\x0017£ïÄ¯C_Þ\x0000\x001f}yÉ\x0004Õ\x0008}\x00141{J\x0013Í^;ö*½þúþ\x0013GÐUî,?Y­oú¥\x0017zÅBÚnk6û\x0013h½<\x001c}²&©;y5ÁêWI%ðÈVF?6·\x0014Ì\0Aê®jMeW5| Ñ875~{ïû0\x0007R;:ÆUfnY"\x0006´B\x0010tÏà]$þ(\x001b7ÀQ6Nû\x001a\x0000<v¢\x001fr¦&éÃ^°9\x0004\x0003ãRW÷¡»Ìjâ=ë}Ó8jÇ\x00018\x0014µ×ëñÉµü|ÜNòq¦`ïA\x001b:ò½LIóØ[gÃ!35ÐQANÂ´Á&k®êHSH²\x0018íZDn \x0003­)\x0017\x0003ý®Y\x0019#Æ\x001e)+èm=\x001euä\x0006z>nî¬7{\x0012=Õ#«ãñ»\x001fÞïy©¿C«eÌ wMé«'ákí°ßNç\x001a;ü[iª\±¦V9*\x0008UÙvÌ/<.Tî1
µi\x0017\x001d{
wtèÊ®Å>´ÛvóèÌË¬;&³ìÜ£\x001d\x001d¸Gò¿º\x001dÍ:\x000b±¥|1Ö\x001c\x000b®éfÇC$²#Gèx\x0000¿M\x0003Ò\x0011\x000eLùU­[1\x001e
\x0003Û!v@QkÕÌÆÓXßWLÝÏáÚÑÓÈH-\x0017ã«X¡\x000fQÈNÐ}j#õ¶:CBås&A\x0007¾¬p\x000cpðPÊAÓ,ªq\x0013q\x001dF~ëk
¯1oO\x0017J¾4+l
¿ k \x0007ï\x0004^9Ã¢Âo~¾öÂvkµ.8å¹\x0016.Sç.î'°.\x001e9 %þø§\x0004ÇÙI{sóâ×7Wê<MÕW¶ °»©·&Ø\x0013r¼²7þÈ°ÏË³OVk\x0019f6\x0010ßËð\x001d+\x001døé¾µÙ·dÔ96è\x001c7FP\x0019S±ÑMñkk^ù
éoíe{\x0017éiÜvqlÛ±\x0013`[XYßúrëLñR&@S¦;Ç.]pÜU+\x000c¥þ\x0004ºÑ9æ@\x001b ëÇN÷ál\x001fàãlq;h¸È2,úÚÀ©[Ün´·ù¤\x0001ðQÑ\x0001ÐR\x0008ÉÌ­èqTÿáñý\x001fß7#6s|.ÿê»\x0017¿¸~Kz1$¨`RÍ\x0017f¸¶xºi<·BùIÖ\x001cmök)\x0018#åæ \x001e¢%ÉV£9Ø*#4:²¸nxV\x00167>Û2«È½;ïÿôåw\x0011¬Ðþõ±½É?¿{}{ÿöíÝíÃ,Âªô K+qÖ\x0002s¤ÏípÒJ|0\x0005h³Å};QN-¼SL¬Óh¹wM^e3Ï\x0000ÜÁC
S/¢ÒÄxb[VêÐG<À\x0013èÉ©?\x000b<T$O%m á+?h^AùOß¦7Z?nåäx{s-Mm\x0013({(ÏÝ2\x001euÔà¡~\x001a\x0004cÞ´Ï\x0017çMù`Z\x0018\x000cÙ©Ø)U-¿7/\x0015\x0014vpPP(U5\x0013\x0006vfÿ íÍâ%dðÞ1\x00150À!\x0015 \x0002ÙA¹IqC%NùÚ¾ú\x000fù\x000eù0IR$ÞÆ¦\x0015êÛu\x0019\x000e÷å\x001eÆ}ÙeÅÓAn±ê1H\x000b.5{8T\x0006º\x0007VårM>µÛ3îtäú§\x001d[f\x001dä\x0008%(!\x001ate][U3kO-s:éiÄVí\x0004Kp,Ø
I|U\x0004æ°­pÔ­¸½õ*ÜÞ^'ûÍÍ÷÷w\x000fW×ªÈ­¤BÀVù©\x0004yP_tï¤H6Ç\x0010}Ú8ñ{¸è«\x001c4T\x0014ßÎÂïÁäÖ¾<¯Ò\x0001\x001eÆ\x0003ÀÄ\x0002hgX\x0019R]\x0017&¨&`pP\x00066¨\x0005Ê3y0Ì´»Ø°Æ¿&ñ]l^¥\x0000^`V\x0002ëé\x0010<\x001aîG/-Ýç§Ë\x0000Ï {­n£*Ôì^
w­9ùgÊ²J¶£Ãi[c\x0019¬GùM\x001d9F\x001e\x0015ÚÃî\x0005påjr§´pät¹¸±\R\x0013\x0018ÐÕ`\x001bEbå\x0005B74èÎ\x0017\x001b\x000bFy?H.\x0015½\x0018Kâ£ÇÅúr\x0007n\x0001\x000fÕR
¼ª÷4VåcU75n¾ó#}G×?íèÈ!ýÕè±²ø*3\x001fNÍ?þéÝýí·ãÔ¼º-IM¬£ ª\x0018$:T<¬Áç\x0016üüL¦£+I§/&WõøüíY¹\x000ctp%ù@ô£qÈÆ!\x001f>¯|@Ï\x001f>çK\x0000½~,úÑ;dGGï\x000fE?_3éã×ÌÑ<\x0004ÐãG£\x001fÞ\x0003Ý}äØç\x0013'¼ÿæf)\x0003õøâóÛÇW__)ó«½¡c,Úb\x0013.ç
\x0012\x000e`2¶«Û~\x0002f*S¬ö\x001e¹öÁE¤²&ì\x0019Lrì["Ê¦þ¼:u\x0006ø ëäÖ\x0006\x0007àr!RZY"=\x0002G
\x0007õ\x0001>\x001cÖ³\x0006#q¡\x0017XÅ\x0015p7u\x001fU»\x0016ÖØÑAX#«èæh«Ö¼*z%&}ò2º\x0012(\x000fÏ÷7á-ÐíÀ+ñ§ÿ%ßïõ»\x0017ò²¸º\x000c±\x0005ô3_²T¥Hh2
gI7_ø41\x000f"\x000f}ÒÚÇ\x001etØ··áËÃ*­\x0012ûÎê\x0014­ðàT²cÛáT"A\x001ff/dÉ;n<U?gD\x000f&uPxA °¤Tã§~ò#©®h|g¬å\x0003\x0013wGÏ\x000e¤kRtëWÎøL·¨j¥íÊS\x000fíG\x0003¼@æÅ\x001ax¹%¯l\x0015J_\x0004î:mÍåÐú¿c\x0017hý¯Ú\x0005\x000bEÅ5<ð_¨\x0007~þ\x000e^\x0007?¿-O½»ÈÊÖ'n\(n³=>¯6øö§\x000b¼M¾eZ6xy¾°bhÌæEÔ±RñÚ}ýê»×¢å¯¾¾ù¦q0®e×\x0014jCsnÚÎ;íå'cì"r@áÐ×g®eGÙKv%H+LoäÉËo/¹4»zÜ)8ÀhÇÐ©\x0010ðy<\x0001çB²g[
ü@ÓÚÁ¡ýÈd$ÓÛ¸?°#^]÷ÜËçãÎ0îAWM}IÙÀºþ[æEÖú\x0019¸þi\x0007×öÜ±bTl9à[ºÌ"¡6ôZà\x0001¶£ðP÷@^«ú\x001fiÊe»3$×­ç\x001c\x001db\x0007oÚ`÷±'rºQiª°\x001aûÁ¯d \x000f¿\x0012íL\x000b¥ªÅ\x0019Í¶2qÄ57î\x000eÜ¸³úä.oìµsôdhf u¤
5gfêJ	=ÿr¸Q\x0006:xA(\x00197\x0002º#Â£ú±±ç}\x000b/ßÿ1¾:ö\?¾øì¾·0üæöî:1U\x001dBæ\x0014ÆåriªLr,à-Syvß@¯õüë\x001c÷9kÏ\x0008Ï}ô\x0010d£×=6>N\-9\x0005[÷r9Ôþvô2jêð\x0006¹6y¢xj|\x0003\x001fÕó×+þÀ\x0019ßÑ+pÆ³÷i\x0004>9'NL<5ÇÐ]P\x000fý¦\x0003ÝÂØuÙ`\x0012Fqì*»Kèµå	ëA,} ñó¡¯R%Øw]<û\x0019ÉþôÇÞâWù«?7Sé[\x001e\x0016ÿ"Ëãöí»»w/~qõf\x001e¦r\x000b£ÇV.ÇgOÀ¼çÍÐ§î\x000bpÍh-1¨"RR\x000cdÇ"\x000få©ßÆ7ºï\x0001îA}ÖâE,/Êö^.1[ZÝú9dß\x0006xD7Á\x0002Ê6%ùÔ\x0012ÅØ\x00133Õ0\x001bÑûPd\x001fàPdW\x0016*´O¨HOFpyd35Âç#AïõWï¾½=Ú¼jæýÝû\x0017ß<\Ï¿Ê\x001aâX	Ç÷6x§\x000c£ñ\x0019|Éõ	,Ñtxîõ9kI³QØq\x0011¯"W(E¹UÉÚ±Ëé\x001eª\x0003\x001d
^Î¤úÈ²¤VÖyj[\x0019?\x001d\x0004\x0000\x001c<ä_\x0019§K\x0011µ\x000e\x000b\x00141õi2uõØ¥q\x0001¯`H$+\x001c\x0004ß$?FÕ¨Fj!Òûá°J¿Ì÷7\x0001ÈD{¶FÅ\¾¹}xýø÷±4Q>;oØr!j\x000f2\x0012KúC"AÆ!sÓ'°\x0005Ã{vEÕ \x0013?k\x000e\x0010Åæä[PÈ'OÀF-u\x0007þðî¯\x001e#\M²\x0012HÿÖYKÆ\x0012Ân¥:o·\x001dÝ\x000faà³ÉòÃµ\x001eÌÓ±\x0007¨
x\x001d,¸½ØMuÊ¢\x0006\x001dA·\x001d}\x000e\x0000}ä@¢Ceà¬ç	Û\x0007\x000c%vÕî%\x001dånïÿôè×Î>½¸÷ÙÍßäìï·ñ¢\x0000ZAÈ*ègðõYjc[w,¯êµ÷æØ\x0004\x0005¤ç}ìÇ\x0015ÜdñÞÝ4ìAo@\x000fU¾ªêÐ&â§U$\x000fYÎM$ßs£å¦ÛÑË¨©ÞÿÈ/VïÉÐVÐ99º¾Èñ<ÀÇ;¹*	\x0014ÿuè\x001e»"¼-Ü.ïMÓ\x000f[ðN6t°H©jJ\x001að%k©/ÐMa´ÛKö 02ÐÀ
øÖ¢J¡ìªD¬Y¥-×'Åþ\x001d}<³ã\x0005ïé¶Ì­AçýX\x001bûáæáÛ\x001f@º÷7×·
MÔ%îl³\x000bÙ®ûèVlyùÜéÄ¿Ñ)´ÏÓÄýY\x000fÿÉ_þSèÀ\x0006§Ð\x000fÃ>:îàä\x0014úaàäÐ\x0000O\x001f
~È

ðò±àGÐ\x001dlB?\x000cüPn\x0018àîc?èñ \x0019àh\x0013úàçÓ\x0012?vZ.¡;8¹~\x0000ø|ýþþ!¿ºûàÿÙÍÝuR\x001aú:$ã\x0017ëÜá\x0013Hè´µñÙ\x001fg²ó~ê³ÄÄþF)\x001c\x0015\\x000cîË\x000f·¨\x0006,?Üv7÷yÉ\x000fp?¢Kë \x001eUñzCeb³Dwe%|\x0002Øãâ¶¦?\x0011.à>q{vHÔÀäºÅ¡\x0003ØãbÕò
¶~\x0007Ëz®Ñ8Jg8%¹Ï\x0007\x001e`à\x0001-P\x0004< »Pg<Màè:\x0007b=\x00021§¶\x00060p®\x0008vµÓ¬43­C¸1À!ÜP\x000eK\x001do´\\x0003	GÛXX#ÃÚ9P§àÐÇÜ\x000cÏ\x000c¶F»Jôy\x0002wÇlçw¿\x000f?øù\x001c¸}ñ?\x001fnõEòp%Õê2ñ­\x001dùÍ¬ò_Ã<<gÍá¥O¢ÑgÞ±}²¦\x0016O¯u¢1úH\x001f¦J@IÇ M)0\x001fô\x0000í\x0000Ú\x000c`N\x0004Ì\x000e\x00016&¿hï\x0004`hïô\x0011Þ6YahÐ>pG®ÑÝzèðùöû÷^øLK8üÙýã¯oÿ>²WÔM[\x001abË¨V0í÷UyöNá\x001cäQr¯OÝ\x0017$¹§µXôs÷ÙÒ\x0007Ï¾TÎäÖvb\x000fáÎ@`ëWQ\x0015R¦GV-¡§Àè!äåcy Ç²6É`Hâ
;ºg\x001f()bUÈ½½gÏg\x0006\\x0003å/ Ø¥ärÖã;1¹òÞ|ÿÍWiÁ
ysóâww\x000f×âho\x0003J)\x0005&íd1u³\x0006ÉR'gÅ'Âi´\x0007!>a\x0000Ö7Ö¿\x0004~Îæ+>~ûÄiÌÝ\x001aòPÖÜ±Ý(kÊä\x0018¸+ó\x001a2À3Ol®=80&wô0\x0018mê!éåÄ#¶,fÖ¢­]Ïòhoq'{\x000b
æsb_\x0011è*AÅ1±ðøÝ÷¯¿·Ë\x0003UëWw·ï~ñ¯7_þôWJ3\x0014ùÉdvöîêT«¡&b-V=wvü¤½z>íú¬ñiÕ1\x0016
¿cB£TJ
¾Öo½4óto\x001aí.¨ÿVh±\x000fHfò×E¨c¡ù»·áÝJ§öÊô4¥U\x0011µÄ6Ý·­4%×Âð;yyþî\x000f\x001d\x000eT¬>aºó\x0015JÅ{­H0Æ©«½Þ<m_4è\x001d]ÿ4¸X\x0001×ò\x0012Á}­¼\x001afzibþÎßÿþ7ïüß¿Ïü_ÿþ\x001f¿|õþîû»÷?ýµÅI·¯¾~ñÛkõôj"Å&iJùÂµàÆR`>
õñI½ö\x001f§¹
¦\x0011t'Çý¿¥l­¼%[¤tpM\x0018à\x001ehËr{\x0000O\x0019%,\x000f
LYt¿ß¥·ß¼\x0002¹{/Û¹éÁÞ¿zñÙ\x001b+}å\3ui««ðÎíÎ\x0011uêÚ|îC<ºâ¦Ïj¯/H\x0006ìlüOþöcñ9Þ¸{ \x0003Âäçò;¯tÄJdD+®ìWi.\x0012®\x000efA?Ã\x0001{òº=HÚö¹Òí0$meü¹½\x0014.? x²ìÖb\x0013%_dÿØå³d ÃE­\x0015È\x000c*\x0004± C¢\x0007×î51\x001fÞ\x0003\x001b\x000eo%\x0007A7¼\x0001]ì¬PZÅ»\x001fÊ[`ýóÃmw¸ÖÝ\°X¦Í4a/õ¸BFÚóÜ\x0012ò«¹D¦/Ø\b=þ'ú_Væ\x0012\x0003\x001cØÝ\x001f\x0008~ð\x0018àà-ñaàGk\x001d\x001c­%>\x0010ü`-1ÀãÇ\x001f%vptø0ð£³Ä\x000eÎ\x0012\x001f\x0006¾p¸ ³Ä ÏgÁÍ\x001fÓÝW\x000f«äÊÈ²\x0012\x0003\x00050FnÑ2Nµ\x0004Òl©ºÒ^:Àrð\x000bì\x0013Ö\x0012îãK\x0014}z\x000fW\x0018y	76óøí%09Ú´4×A³x!²\x001eùH[Bê²Ì*»!_\x000f\x000e¬¢\x001d\x001aÕ\x0019T\x0003\x000f¬r*{¾i\x0008ÀNÎ~L·¿»­÷ß®\x001a\x0017åÈ<þáþîZy¨\x0014*µbiWÙ%°ÒôoÅ<oÇ?ü?$[ú|1@6\x0007DT)¸B¢HòÎaãÚ\x0005EF\x0016;8\x0018Yà\x001ct°¨®9å	ºgOEÍö\x001c«*&¾ýáª<ìÿíþñáÕí/®\x0015ÅwâþÄ*1
ö¹þ\x000cõÖ%ÉëPoíó6\x000b©\x0019lô,Y{\x0010IHÍMZg¹ñ\x000e5Ñ\x0001f\x0010ÆÁK²ù\x001e@Ö1ió/aÆ6:¢\x000cì!Ò&~tâ7§Ìß¹é©5¨\x001enË
éüfé\x0001ãVãHà,Ð¹©Ë\x001d4È\x0007x\x0001ð­Öt\x0001O²g²	
OJ/D\x001c\x00143vpPO×\x001ei$CÇ4Í¸üJ\x0012[ÁÕ\x001dzwtÁòÐD \x0015u¹I\x0017\x000b=(röÇbÁï¿üöñÖ//ú«K¯d®\x000fªíÎÎQöÁ6zÚÆV\x000bÎ6ªéÏNÛ7A²V.\x0018µuå\x000e\x00118\x0019@V}VÑØÂ¿½»ë\x001e
\x0006\x0003}\x0014\x000cªú$Üz±?Ä|LÿÌáýó×zxÿj\x001e¸¦ÐÅlgkÊè\x0010
 4UaÙç.\e\x0008¦ïÐg«éAW¦
]Úaênð»u]Hð\x0014\x001c\x001bJc\x0001¹\x0008\x0001·\©6.2v³	>Ä\x0011\x0003\x001b¸Z´HÚh#\x001d·âI¤\x001fÍ\x001d&¿}mê?®Îw/~w÷ÕÍÕ\x001e\x0005É1­Ö´Rû%r)U¼â5ådB±.,\x001e\x000cÖû|µ°}\x0013Dù\x000f°\x0005Jé6ã;j6p&7ÖÓþ8°ÁëõÃ°\x001d\x001c\x001e\x0005\x0012c{8¡ÝôI¶\x0004þhnóV?GÏ\x001f7ôy}~õð.\x0000[yo\x0011û?~úëë»Û_¼i¯®´P³Ó;Ë»x¹ÒJ\x0005«¼Ê]´F:ô /Øgå\x00056#tëgµxéX2&3Î.ê;×²vp\x0017À?E¢!\x0016'Ïbq*:ÂB4>vîûám<ÐÁÏGk{ÃDO\x0005\x0010èe#\x0011õJ\x001a¿¨e=|ÿx\x001bþ¼¼.¯H\x001dÃÕüg×ý6ò|1£:SUWÉ}\x0012GÝá5Ó'kb¶ë\x001dÌ\býW_ã]Ó:P\x0002\x00078P\x0002µ\x0019)[ibkæ®5\x0003CKÊ±@Ñ[íH\x0012qS\x0013û¬ùþ9u;:uÕô\x0012¦%U4q0 q°OªÛã\x001fÓÝïß\x001cÎºöðn\x0019ºÇ;ýÒÿCÞà¾¹RéGÞJ¬õQìæ\x001c}ÀG =~?yy\x001fRu}ê8U\x0017Õ:u8UW\x000b)
¤T<u)EÓ,C\x000fB`\x0003¼\x0000x(/ÇÛ@ûVÑëT¦uHBnôFkæt\x0007×?íàúÔ\x0000¥\x0010e*9Dw\x001d6ÉÐ\x0003\x001fyGw\x001cZVÖ°¦¡cõo»Ì\x001dªV\x0003|T­¢ÎÄ ÇWkY!ÅÀ\x0006ß3øn¾¾vpýÓ>/ò<Æf|ã°3LæÅ²ÏÄf].B\x0017ô
\x001au\x0006\x0016`´
n2v>~r]ô´ÿø£Ëñõ&¾ô\x0007KÌríJºÕD!^9ïýí¥awöòMêsçÜ×ÎýÖ§õ\x0002K#\x000f~Û¸g
?ÄR\x001aûm^±;º\x0005É±â*vÄª.vÄZëüÞú0Ã!Óµ£éj6#lÉ¶ø¦0Â©^bó]Ö\x001eÁÊ¨pñ¸ÔÒqì\x0015C\x0016­¼wxÿÕ×fÒó_ÿþ\x001f]°\x001en\x001eÿ|µÎvi©Nb{²êúï#\x0016Ù*ë£MÝ\x0014f¬ÿä/?|\x0013÷ð½@àÊå¹\x001a\x000c±\x0007}\x001dÝ\x000cjz°¼eßøý¬¥z¾:û4µ´Ú Ôü'|k\x0013\x001f!;ºÇ\x0002Ý\x0007¢\x001f4\x0011\x0006zõ\x001f>¢\x001e?\x0016ýh\x001c¸£qà\x0007£§sôôÑèÇStGSôÃÐçMëxÿêfÑOò¨2!znqûõ²ï\x0012\x0006\x0016Î@Ç÷º\x0012ÒG_Rõú\x001f­¿NU\x001cj}êæ¤¼þ@¹Qû0u\x001cw|Èoo¹ÓCVmcV­zè%lôÐ¦\x0004àà\x000b°Á\x001d\x0012_\x0001{\x0001ª¯®I¡G6IÑ\x0002Ø1ü:þø]\]Ì×£Ù¦æð#ËMå¯«P½Âøi(wÍgF«©ýL°\x0010×É+\x001e\x000b51ÃX~º_u \x0001vøXìcP·Ãqôà.ÎûjG×?í\x0004(C2ËÃ\x0010û.Õhõ÷RÇ\x0012ã½ùáákH¤ýòÍþÚ«\x0006ÿvóíÝÛwFRØÉÂU»³äß\x0006VNmü¨OUtx5÷©k/ ê§Ò *,ð\x0007ê\x001atÞ´lÂá¬\x001bØ   `£N$sc¸NT\x001c[Ê¸jz	a^N;ºþQ9²A\x0008®6Å-\x0014\x0006-Ü¼ár9Òîë«ügè\x001cúL§þÅ¯o\x001eß\§\x001a+=$Â´~l7fInÿúÜeêcî xßgª]áA·ü\x0001Oþø&×pX>\x0017t\x000fÄ±\x000fD?6¶íèÐØö¡èñ z²£Gÿc?Ø\x0008¿«ñ\x0006Ì$\x0006\x001bêW_ÿô¿å\x0003¿~{ûps%æ[ª*\x001fFé¼÷\x0008ç,{w´;éÓ.À1w ã÷Yk\x0019Y !ÚürH^åÓK¬g\x0013ù§÷\x001eÉC9|`Çÿ¹wY®ìH®\x0005\x0005VóJ÷c(RbÉdd5»J­)
ÌDe¢
L°\x0004¤Ì4Õ'hzGW=îijÜ?¡/iw}v,¢G	î<É±ãéåË\x0011»Háý	;E%ÔÉw¬
ÕbÃRÔÁ;¥(çè¡¸þ)+JQÍÑª^\x0000uÑÚ__ï!Ò\x0002¢ig
®8%jhk\x0010A\x0016 _ÁÓÜÌ/¼\x0012ÞÑ¹o³%fW\x0017¤H´\x000cî&,²Ñ\x0015xÅÕðÎ6åòÉã8¡óO;zÒeü49ô&\x001bl:î|TÌÌ½Ää\x0014ìè!Ê.C\x0003fÎ\x0011©v\x0012¬;6,[áÍï§nG÷ý¦\x0013A¶ÎU¢w8ª0#7¡Ó}Il^An¯¿½d»býI:%f¤y»·YØ¯×¿2­ñ?Éë àl\x0015µI\x001b¬¢\x000fxôã§åHo~2Ð7
B³|e¼C7ÈÙôFS
£B+'#):iÂ=ìò§Î[\x001f¬Èda·yÓÕTG\x001fðèÇÏ5Ï\x000foÞßü8¯ÈÃÅonoþðë//¸¾¼9Ó	a	TTb²ÌDÛ/òd-H\x0016GVÛ\x0008/d=&reµ\yð\x0001~üÜçëõÃÏ?ß-Ntu}uÿ?#ÌË\x001dqu<p_\x0017N\x001a"IÅ¾úÔ«²f¼NÒlmêäÚv¶"§º\x0000eF¬
;\x0008ÿ{Û\x0008¯Së¬\x001d\x001cºïD\x001a[©
°Zu;%\x001f\x0017tÅò§oÝrÁwû¾úÇ_¹=·ú^ ó÷Dæ)%£
j	¬óò©£\x000e\x00070ÞW9)_íÕ\x000fxôãçº²wþÝOkº9«\x0002üúª\x0000)ë\x0006\x000bÌÝßK_¸Àºg£É¯>µ(ÀZ\x0011{*ý	Ó\x0011Å\x0012¸¼\x0002G¯ê³¸f¡è/o\x001fSÈ\x000en½®
rà¾\x001bV±\x0019+Ã´V¶lÓ·Ç#Oß|ûcw\x001fÑÝ7\x001f>vfìñà­ýÈÁOÚ\x001f®¾_'Ñ//¾¾ýpuw}ufëÀpµ >¬Iµk@°,
T&II?ÿ34¥\x0012ÛÄI\x0000ÚÀ;+ÓNÃO*¤ÉÎÖ\x000enjR_S«\x001dÜBg¼Ä½\x001e 1']y\x0019\x0002Ý(C{ÈE\x0003Góþ»û÷«ÜÌýÅW×ßÝÞ_Þ½DÎ\x000eB|u_íY¿\x0007XÜ[ëÎç_îiEÚ¼	¥´÷)ÉÞ"íã8ÀIN,¾©ëµ´è7\x001d<bA\x0015²é½\x001bÝT¬M\x000c»ÙæøögzeVFÿW·\x000f7û1?kª#\x001bÕöÂycº¸\x0015W¨ôì"×}Øá\x001c1Ó¦Nbi½cùÁø\x001fýö¹ðéÍ\x000fßý\x0005}}yn#ßVWUÒnSº©Ò;î=\x0010}b3ÿ@Úbphó$U£½ôl=üG¿\x000fÜTñ´c÷~.OÄ\x001aduìô±ã¶ôÄ\x000enãG×qÏwð?\x0012ÜMí¾wp\x0007í¾\x0008>Utð^1òTð:^ý\x001d¼¦\x0002\x001fo?¾ÉoA«j¯\x0010úüÝå=³\x0017ÏdoÑ\x001fQ±å\x001cÃB¬\x001cßë~3÷·®ú\x0005>p\x0004óD[l\x0013öþÆ\x0017<úõÓRü)}{ùÓ·+3ø3z)ßÜ^-\x0002C¾"zÇ¾\x0018µ\x001aL[J½Å\x0008S,¿Í\x0018çD!ð\x0001~ü´\x0016õç«?üôµWþðÓÅo8||&Ó»'Áx<\x001dä\x0008T\x0014¹Ó¾J}ôô©9D¿4NÙ¦LÇ)>àÑãÆ)Üüñ»Õb¹vÑd-\x000cêê^ÎS2kKvqÌB/B\x0014uêÃ(³õêÃXD\x001cFÏµIV}¹RC#\x0007£õK\x001fO\\x0007ï¹¹Ââ8\x001e*\x0017­Óµø&+fãíµýÃÃÕÍ_þr°Èw\x000fï[4Z\x0014\x0018Ît\x000bf%áª+ÍBMú(ðEÅ;^ø¤)Ó&amµyøÙC*[£¢h
}¹bU#í\x000c§V\x000f\x001dúÔêAf&a¦T
\x00008ÕËÐ±\x00084W;>Ñ\x001b:ê©ßfN8jlÞÌ"â.ÉúMp5ù\x001aº»ï¯¡®àË«óªD¬j\x001bØ·ÛÅ
2rIY@,/ :;wþY\x001aU"ÖãôÛu¯;86×~\x001aøÄ°êàÀ°z"øD=ëà@={"¸j,wtÛk,>½½oý\x001f¯gÿ %Ñoß+dÃú\x0016h=íþP+rÙ\x000b}Ú§\x0017¸X[AÎNe¾ÄÅÜ×ùè\x0003\x001eýøÅJÜüü\x0006´lQ=îáÍÕÝ\x001f®ÎDkÏF	»ÔÃgd:øW)ìë3ôú]/ÅtW´ùÒwÅÁð\x001fûði\x001dìÍªKó:<\ü3y\x0005¯Ôxe~DêU²ö´\x000eÙVPùô/Â\x0001e{,·	Ø#Ë5ËºYèÇã§'eòk_Y\x001d\x001c²\x0014O\x0004wS×Ñ\x001dÜõ®£®È,Y^Æ£´ú³-ñãw×\x000f\l"¦^Üýõ?ï/¾¼}ÿö\nº\x000fzNùÄ\x0015#g9@\x0003éÀµÍz\x001b\x001d^¦þ2g\x0003/p=þG?}n¤þç?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=O¹J&°\x0014ìO\x000c®^\x0006\x001bE¤åæ\x001bqÞß-¯\x0013xÖò¸\x001c~ã2\T®ãeðõýÃTQ\x001e÷Úï8w\x001e&X¸Âò\\x000b\x001cèõfhp+¹÷Á×gçW[êÒ«Oz\x0002\x0017$=+ÀLw]À»Ö\x000fí-9Ò\x000c´\x001d\¯L©\x0002
\x001e+Øõè\x0002ÊÂA\x0001!É¦Ôºòú|g26\x0014c(\x0000¿ç_ï×³\x000f÷\x000f\x000f\x0013ålJYÒ16VXüËd/âôËüÝòlq9ûpv~>UÍEO\x0005¡«'TtÎ²aÂÐ3C8
z£÷$´\x0005¡­%t\x0012\x0012ì\x0006ÝRû|!½b9·m!ô\x0005¡¯%ô¶Ãð-n¼éL¹ôÊL\x0015¡ç9¡çë\x0013\x0004LEx\x0000\x00186ÿä×4òa~ûC\x0011~96N¿ÁéÓ*¸¢\x0012½¤Cøá
<¾¹}^ýº~Nv8×\x000f«ÇÜ\x000ceâ\x000b®"µ©CÙe\x0014lu\2,õVÎ%«·ËùÇÅ2yá\Ï/sS×±]í±¥÷X\x0000=O'x6·¸+Ua\x001d2ûS\x001b®\x0006ù=®Þ\x0014·Pw±zþ÷§Õýä\x0007<\x000c\x0018^i0NÖºÊ3_\x001a©>+?9¾þ÷Wçó³©í\x000fÁº\x001cÖµÁàð.+¬¨=¤5±ÑK¢jTerTeXE/\x001b\x0016Î®\x0014¿5;èHií·\x0000[:ì\x001eX¨qMå|`\x000b`HëEQÑ£p£·Õ´¦\x0008­i\x000bmØ;áV8^Ãðdª=H²6ÓÚ"¶¶1¶\x00165MÒ¸Ó
]ºãb[W\x001dm_å\x001e¿0ÕH+qþ²P"¢H\x001fÏ*º{W\x0007¢-&/×8{Aí)Ñv
Ú-v[\x0015K\x001d-Ï®ì8\x0014ÜÈÆà*µ".w°ÅNÁÅt\x0018h7Óòb$D/Ô¦¥\x0008\\x0019\x001cÈ@¤ÙÖ-ûüie1'DÕ&ZNFtPÁH-Ú4æ\x0007\x0019¸<s`¸¾q(0§óá´Ej\x0016\x001b\x000c âá ÑýA\x000bpá±m5ÓÐ \x0016OÒ\ÑÈÕÌÒÕîË\x0006\x0019ôð\x0003dÐSñÝ\x0005ä\x0008V/\x0013P§.	^s²\x0013\x0011VQ*\x001aji6Êî\x0002Ùéb~÷:È±D
#	¯%\x000eK'\x001cù\x000ehæG*\x0016	kk¯¢\x0019_\x0000¬À^=áe\x0019añ±BÊ£¥r,U\x0013-\x0003ÝKé2
ÔRÏ\x0005Ý'Ô îer,SÅÉAÝ[î°£±%JàÚ±íÒø\x001fv§óäáçµ@\x0011c\x0018b¢\x001bb#\x0005§¯Òi7Ø_jö}KÍùê\x001f«çõì¯«×?=ý0qòt\x0014µ9;8w\x001a*Ïá_²¥§æ|þ×ùr1ûëübqùÝÕûí_\x0016-8Egïö\x0016þðøæ|\x001d\x0015+^ÍÇMRÊyY
WCqÃ®|±l%ç¨RñJB\x000eÁ¤(Ààqg0¾KÏ8%àL\x000cBá(\x0019§]Y
YmA\x0010L¹\x0002\x000c\x001ew\x0006\x000b\x0003+½Óaã>Qr1\x0015®­óU	$üÕ!]¯^\x001efh\x001fw¹nä\x0012Òaùcé@ãÀæ\x0005¿	?fæ~=¿;'Ï¸Ëyß©´Òæ¶RÂ\x0001\x0006û¥ª{ïPåC\x001aÉÆ.¥7I'R\x001cÉW¥\x0008)o)¬¬©-e#éÚ9§\x001cÍÏÎÝM7ÐêV7Ñ*\x001e=jcl\x001dÙ½û0Îq\x0010\x0018?Z\x0000Ù@[\x000c\x0004Þ8\x0012 ­\x000fGBØ\x0011RÂ¸»ö\x0007?ëÐö\x0005(@T\x0004Ã¨å\x0018<ðÐ`Î\x0019åâ0°ÙõO¬m (NM²áÜ{CÏ¡ÀFEáêiU1\x0010TÛ@\x0010áh4.\x0002­\x0006\x0018Z§m\x0017Û1ã¹zZSL	¦mJ¶3\x0018g\x001a-34ùQzZ'rZ'Úh9Í.\x0004\x001a'T¥\x0014b«Æ4#+\x0017\x0006W\x000c\x0003×8\x001f\x0008]\x0010yÖ+©®uÔú´:®|0yµÎ^Ê¦4ÐäÀ´óÝyÂÑ!h-+§Ú¶	A:ç\x000c\x0007÷\x000c\x0016/8Ã*AvÔÁ³\x001a×Óm¿¤r4j!º\x000e5¢,µæ\x0019á\x000fòqæ{\x0018ß0\x000f}j"\x000eû|EÄ\x0002\x00123IÑè\x001d¨\x001d5}g»\x001aâ®\x0010W0_ví\x001f
Û¸Ó¿ÿòüÛO©ÝªLqÚQ>L\x0006\x000cU\x0016Ã±qTäô/×Ëíbñ\x0011Ë\x0012K\x001e
(¹Ä±pË\x001c\x000b+¹Üp¹r|¹ºñ¥\x001d)\x0010kgð~ÒÇ²A\x0002\x001b±4ëÀ¶NxMôåþðGøßcYØ\x0001\x00161Ï5`à[Æ;2´\x0016Õk.3BuAcáW*Þ|þÃf¤\x0018dÃtÁË[ü)\x001d\x0006©@C	õB<¡YoiÓ=èÚÎ/î/æ\x001b¥þrPS\x00078â\x000fÇ9üÃqT£jp¢"%nÍMWªöCë)n\x000ftN¤ÈäDæ}eõÓR\x000c\x0010<×\x00109Ñmc¥Ài	401gh\x001cÛZ\x001c3\x001a$î\x0007v²áh]÷Å®ï¿¾Ò\x0017/\x0005inG5\x00044	3Ú÷\x0015ßr1\x000bå¿Ë³é¾x0û£\x000b$ä-Îèo×Ïß~Z?<M´G+PRF\x0018P#K\x001aÛ>ìúñR>\x00157\x001coß.·ß-Î¯¶É>'(¡
(xÜ
.\x001b\x0014Ö\x000fê$zèáä\x000f4â¨ÝC½\x0012,Ñç&"Q;si&,jÁG5
xõµµJ¹Bé¹À²'ã\x000e>;Ç+âÒ=qºËBQÍª³\x0013oñõÑ;³ÆñµÚ\x001dÍXòz
\x0010I%Ù\x001bGR\x0006\x001b·3»
.`ú4`úô\x000ez+\x0006\x0017áÎKþ%\x001c\x0019\x001fV÷Só5<égXøHçp\x001fJ\x0013{Ñ»pJ<ML\x000f\x0008Õ÷w\x0002P5T¨\x0004)ð\x0003\x0015N« «Yõ)LÒ°{÷ý\x0005ãoà\x0011.âÝ\x0010ê[­\x001f?O\x000epï\x0015\x000ehxqi4á¯K=J
oâ%\x0011*\-.OGtÁ¼v1\x0001Ðë	i÷g.\x001cI­çbõò|?Egà=¦
"\x0005ÊQ,\x0015l:tLz7fKr=\x0017ó»åÙé~bÄ\x00144SÀ\x0014Y\x0016è0e?ç\x0002¦Ì\x0012ÂÇéûm,`úÌ©`wL<
 )eÿ\x0012-A¶x,ûWCÉ³\x000644®Æ\x0014^`2|â.Õ\x0008Áf.\x0019\x001cÁÒ1*9Ç'Â\x0004	îö9$<\x001fá+çR
8U=§NÚ¸úJÇ£;W\x000c¦Iw@\x0016©c9ÔÝ8?q\x0001KìäzÞ\x001fÞÀãó\x0015Èß<ÃD~úÓoÿï·ÉZ\x000e%´Ã
Aè¿Àtë.ªlÙq>\x0007í%Ìæ§ßÍornu÷üù:ÜóSíËuØ\x0018?ÇJ°Ó§OkHNÜÃw}AabÇþè.´#5V×aw¼¥`§Ww°BO%¢%70±÷SQøá
7¥ÖÁâï
1]}Ô¿q$gU\x00141Äª\x001d©Ò~\x000bl-Ç\x0000¢å_N¿\x000b¿Ê\x001dJyU\x001d~ÈìÜ¿_¯\x001eCT\x001f~þt?¹x«´[u:PÑÊNBhùî÷ùeæùÕÅÛ³×\x0001M\x0001h\x000e0³°ó2;:@W¼bWý-¶Ý8íxê\x0004pÂòqø G\x000c¨\x000b¾-Æ=4þòò1\x001c}kÐÎ\x001e[%ê\x00144è|Èâ8o ä"\x0015¹uï\x0018~ï¸8£ÿ\x0004|:£+pI
A\x000e<RË³|+¹ÛÒPq\x0003cøãÝÄ\x0019½Ãt\x0005¦kÀô\x0006Æ`Ä>]ÁI.ÕÛí)­Î)í0á±S0=y'Zé;J5J\x000c´0\x001a9hÚhBÝqJ«Y­ÐîÃ	N¢á¼Ü\x00005RúÒ·½s\x001c4Ø]ÔNmÞ\x001dÓ\x0017_oø~Ï`Â]J\x000f?@\x0006\x001e\x000e±ó/O\x000f¿ü´½[ÿ°zþqªÎÜ'I:Ê*
¥fq\x0016ÜA:Ê
¹»¿»:¿þ\x000e8ßÏ\x001f¦úðÅ \x001b\x0008E=!K\x000e`ðÑ\x001d¶!¥)\x0000¹¨&9¡l¡ä\x0018DsB1DÙ?ð*ÙÈRT\x0013êP×\x0013]®Á>H/Ù
íøZ@^\x0000òzB9Ä8\x000eÐ£\x000b¹ëbøê[Þ\x0019£Ï$ËÅ\x000fåSu\x000c
H¥(Ñ¡"¼fK¯Yòý?\x0015å\x0014#åêx¾ç¿±úúYR_Ï\x001d¥Þ>¬\x001e?Oä¡èR`î\x000cêªFø\x001d\x000bZA~½8qeRoÏç§\x001b\x0007®\x000eKäXâÆbÊÀ9Ð~¯\x001d\x0016}xÌ\x000fVwV'Vp:%?`Ë e\x001cß§±zÂì É*;RÝ½N,\x001fZrù\x0008?\x000cäDÏÃ\x0019ÿiÊªÇxÃ \x0012\x001dðC«0­8x.f\x0008GñÎA&åräÀD\x000e&\x0008Læ`òÀT\x000e¦þx0.Ò<æ2³\x000eñ&\x0016&"Úùú	ìN_>¯^\x001e&®&¬\x000cp.0(\x001býuléÆæ=éÌ¨¥ðùâ
NïNçwç\x0013rÅ\x00113L¬ÀçZNÓµSye<xûihÍÀKi\x0015á±\x0004H¹ÍÕ\x000eæ^fsïòéçÕ\x000c4{¥]gÐÊqÂ³íÀã$äWáçWØDÎ&êØàæ0éËxÎ<\x0008\x001bF65ØJ\x000fBWË&s6YÉ&
Zx.\x0004ÕKÅ °\x0017ÊÙT%R¨z\x0013â&O$¢u¯TIÖM´í«=+u#®BÓ\x0003ÏRÿmÄ³Ý[\x0015å=mäLÎfjG\x001cI0xf 5#\x000e¿U=hQØ\x0011-\x001cèKóRøáMç_ònõó*\x001c çÏV/_&NÚ\x0018T	1ÝçVwþ\x0006%]Jü¾_ÌÃ\x0001r¾|;¿{·}é7ÌM4áØDCçÛÕó*Ù(=MÝjá\x0004\x001cZ£D:9Æ95BòÁM6p/æËyrNºº§ENÅsNÅ\x001b8­&ÉL#u²ë\x0003!RjBàÖ6SïÈi\x001f6%ù\x0018O[Amô×©Ë\x0012ey:äjÆ\x0011,ØPa.\x00104¬FÊ\x0007¡Ñûz~w3yÞtWt\x0019~xÃ7\x001aèoVß\x001e^iHãO:är¬mÒt\x0014¬\x0013\x0002 7óËÛ«óÉft\x00046\x0007\x001b\x001a\x0015;\x001aN:0<,*©­+Ì8\x001açÕ¬Kºí\x001a/
Isª
q8á÷n\x0001h\x0008£\x001d[X½ÕjwPÃsPÃÛ@\x0015n¾,C£\x0008í%½ù­¶5\x0015¶\x0008§m\x000b'4\x001c*Ô÷ã¨ák
åÀLiBÿgWÐb|Ú¶ñé4¶\x001dÚ°ÕîJßÈà+ìj÷í¾\x0008¨o\x000c¨'5\x0012ÃHÄ0Oß\x0011XãíÍYÄÓ7~ï´;³\x000cò28B\x001d§\x0017ÏíÒÎs\x0013gÅ§\x0004M°H,åÒäd:m"¶ST_%lÛ\x0008\x0008Û"#U8¼è$S¼Ú)²SC\x0000ÚÿrRµ!³\x0013©í\x0011Jç\x0018²£Ó\x0016Ýiz-ª½NYbÝ\x0010ÎÙÑÖÎ;â\x000cVÓj´Þ{}®\x0018«ÒµU\x001d\x0005Ò¼oP½ÐjcIõKï\x0017T´3\x001d\\x0015kö;R¨Ä{¬ÄSÂ3HU\x0000£Óá!±urïm1\x001er¼åd ãÃû\x0015ÞÝ¯ð§Õ·oO÷Sæt>U9ù¨ÓW`ÕûN=ÒK\x0003\x0012Âoç··Wg\x0013D§r:UM\x0017v\x001a\x001cI'\x0006¥ MxcB
Ò\x0015B
Ó\x0015\x000faã~ö<Yh)Hf%L\x001c§\x001fÅÈAt èÐÎÃ¦ýl9ñz;B\x0013jB¸×\x0015½®ÇÝ¦@#:9ðÑjc9£¬g²¶¨<\x000b "1\x001d½5}±;£Ê\x0019U\x0003£\x0003+ØÏ!\x000cygéÎ-Ö«×ã¸¥S):\x001aþþ7ðøæOÏß`.¼\ÿø¼þ:u<\x000b[`ÉQ8ë%YÜ\x000c)!t«Ü?-oa\x0012¼\|X.nnÆÊiý`r	?dËÍê×é¹9	iÞ\x000b{2\x00104IÕ#ª»Òcâä7óÓë\ÂÒ>ÇÒ~w.\x0010nbT°M.Ñ\x000f¹Ôæ%Ù.\Ü\x000eáx-mß¢·¼ÿÇýúyÚÄqTàR`·\x0000\ZLp3åÕ\x0008ÚÍlyö×³Åd^¢ã}·1Ðñ¼Ýx\x0007<èOºe
lM¢Sè \x001dNr£)`'º¿	]Þqÿ\x0019ðG&ùÏ«ç¿?<L~¥uâj\x000cQRv´#à[óÇðÎ/æË¿OÍ&\x0004«rØÙä\x0018`9Ó¶èÑ\x001f°G®^^f·?=MÉ\x0017;Ae`A²4VóBu'±)3jr7»ý.w\x0019ï¸½
õ"\x0018ªÐ!|7¿¬\x001f&+9=ié:§4Õ*IMÀ`çSõc!r7×óíQ[1^æç8Ó¯øCi¾~,8Õ£çÒÈ\x0019þò^\x001eHb
^ñ0çÜÜN|;È*»á\x0018Yá±ÖJlßò öÓi\x0014n	=ß\x0019¡\x0007=¹BÓ¢\x0012u\x0019V\x000f³·á¿±ê\x0002\x0004Ã´Tð²#l_é\x001e¹ná¨È0?½½º¼\lk\x0005":ÓéZ:mñB!Ðét ï/)7*Y\x0006p[£ÇS	ê{\x001bEz¥~«_^>ßO]¤eQ­ÔDZ5'F?(?-Ê¾æ×w§gcw¼\x001eE½U_ÆâA+»W\x000b	sÍòþËT±{ò$4_@ÙpÒ3pA\x0019Ñ¸¥Âl?Ù,ÏÞMI\x00172\x0015g^©\x0015ê:%î\x001bÎ_¾<ýzÿy6ü2e¸\x0012ð<©°0q¿\x001fv\x000eØ\x0014§Ø<ß½»úxv:_¾²\I|ºW\x0002>x¬\x0003t¤\x0007Ç7Ü¢\x0006>ª\x0015r³¶¦äÛR¡p®sG\x0005çK¸ÚWû»ÂeF?\x0000×If\x001e\x0007\x001c/áøQÁ\x0012N\x001c\x0013)áÌqÁÉ\x0012N\x001e\x0015*áÔQÁé\x0012N\x001f\x0003Ü§hûÂÃv\x0017áÞåK|îÛèf\x0016Î¿×OÏßV\x000fÓj+p\x0013~^Zö\x0003^\x0012`\x001dvßFW³p
¾¾ZÞÎ§=Àe,uäÌ\x0004577ÿñ\x0002ÂÀ\x0017«¿??=®¶Óiã\x0018ÖÙl*P
ç}r\x001bða#Óÿ\x0003zÀ\x0017ó¿,¯.ç¯õH\x0000\x0006½i»#LÙf%E*\x0015Í1ÇË\x0006ïÊR\x0001ÙváîD¦©ªýNdrC\x000c\x0015v\x0006JLÕ¿}¾ÊM)n\x001c
ÛÇâ\x0006\x0015Và	RAevV\x001cÕÛåÙ
}\x0014\x00032©	\x0000\x00005J:\x0011ö¨ämt×æd\x001d%öà>äUºÝ0SeÒ\x0011~4\x0001¾ÓùãçûõcØ­?ý\x000c9ðÕã·¯³ùIØ _N\x001cÏ\x000cdèUW\x0002¥Ó\R&Wò²äææOaB9=[\mûÕ\x0005dÄç·7³9l3ÁeúÃ\x0010Ýæèv/tÅ\x000c§\x001bzÈ\x0006bõ¼!ï\x001b)£ë¡ÐE.öf÷¨º	â=tÞ4¼ëïÐeíË~ìåì \x000b°×ñ]M\x0005ï4b°ÝUÕÓ\x0001ÉuA®÷ºvT\x0011\x0015³ñJ½}R:vÈ¨\x0017#Fî;bÀò\x001dÙArIbÂ()Í\x0001öcW²cä¾qg´DvKÙ\x0015Xv\x001bs-¦?µÙð/í\x000em\x0001|6ùô¼j\x0008;\x00158§«UwbcA8î<ä@Ï*í´\x0002ël~÷v9?}÷Ô@\x0007UxtÍ U\x001cr\x000c<¾pU±~CeW¶ìýé æGàY|þòãËW7}ÿ¼þú¸~Ú\x0005r\x0003Ê+pË/½B\x001fðHN{\x0006\x0010ä\x001a\x0002Îï>ÜÝ²éûåâærqþ*¤Õ9¤Õ
\x000eG£\x0001\x0005ÃÔG\x0019(±[H0±\x0019ÆjÊÌ43P:ó\x0012\x001ek1µsI\x0014ÈHN¾3{\x0012b\x0003ß6JQRzJK	T\x00136®2÷±\x00006¦\x0000½ßÔ.Ú\x001dS¨Áµ&è*äúù9æPßýöÏÇßþùeZ]ÀÓµ³Ð=\x0008àcI,eÎn\x0017Ë%&P/\x0017ïÎ&à\x000c/'t\x0011KîºËwë_VÏßbJõ0»Ô\x0013á \x001a,\x000e¾î$\x0015nÃV\x0005ç\x001f/Ù¸ÒÅõ|y\x001bSúósø7¼Æj]Î
ýÜÕ¬p<Á\x000e\x0001\x0017"G¬\x0002ÕÙ¤\x0017£)ßJÒÌ¤\x000bH£IW\x0003*|é©I^Z$c\x0002*YÌË0NÇÚ|jaT9,<6À:Ëð¼\x0000*\x0003L·\u×nLß¦\x001eV°º	V[<$\x0006X\x001a¨\x0002,\x0015ÀûZf5kø'\x001f~ø\x0001>ü·O/\x000fë_WÏ_f\x001fÖOÏ?®¿Î®~þåþËÓ¤&\x000frA0Ge\x0004ü\x001bÐÅ}{uw¾ø8_¾}X\-?,nf×W\x0017×gï®î^åå%o+0\x0003=¸ä\x0018d8ui:­©\x0004Uxï\x000eDÜ_O\x00011\O5\x0011sPyN«\x0016\x001asÂæ\x0013×TÁË:vbÞ7ÀÆ\x0018C\x0003l\x001brØZjat'm<Þ\x000bWîG÷A%²lEæ,ÉuêÓÂ³-fÛ\x0014r9.xûÀ\x0008£!Ý^\x001am9\x001eiÐ\x0014d]n\x000fö îi#1{ÚÑ\x001e¶>§êÆ±w\x0007+`éÉymëd\x0001Í\x001e¸\x0003ÓÐ.JGo²P\x0015\x0003Ï=]ùé¹æO\x000fT.ÓldçÖ\x0000;´,9?Ô¨på¨pí£Â ô1¨Ñ-¼	GD\x0016ò@S²(\x0017½(=Ó¶­y\x0012\x000fQV¨Û\x0019\x0016n¦)Êe
ä\x001eÈý9""Ã9¢1Ê(ym\x000c\x0018'\x0019\x000c2eÆ¥.]¬÷ îSH\x0018rHmAÖ\x0002ZD"²6$^\x0016¶\x0019,\x000fE¬Ë\x0018ëÖ\x0018%\x0015Ú\x0011\x001ag¨3ZÛ¤æ@Ë\x001e\x0001\x0017Ä­ß\x001eó\x0016;kM¼£Ã$§ä´ö@ßäÅ\x000c\x0007ÈÃY8"+{"pR´RÝ8\x0010²*Æ\x0005<¶\x000bµûÆ)ç\x0010eAêÖþPë*?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-17.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-17.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001aÝ¢¤7ÄöhVlàiÂ©Ôm!¿¢S4¬\x0006·/pi¹5úNâ÷ê¶Ô\x0012'x\x0017Ñ\x0005·±¥\ÏY\x001eßµÆÜóÔÿËØ\x0017m ´/\x0017h\x000cæ­í\x001fùkÜöCU¸\H¦oÐªrºÐ\x000bÛ¬*\x0018Ó
¹
ÝZÚi.\x0015´¨\»3ï­-
\x0002\x0019\x0005\x0011$Æ£Uá\x0008ZX®ý¸ÒÝÊ
9gÐ¥ã!Ç!¸X,õ¢\x001d5cÖÊ\x0019ä5DÎ¥I¡´Ð\x0016í,9\x001dù`ð·\x0007÷¦Pr«Ró\x001bÈE·ý±¸é£"Áoîß=>}&ÜX±Êî!ßµ¢·k=FY7o-÷ÜÓ-XI\x00165Â`§£f§'.eÞC.©ßA£VeX\x0014ÌGlfÔ\x0008²1¶]ÞH\x0006Fæ½©;½C3þ\x0002x.þÒ¢
ÅºhçS\x0005¡ÑLRlÐ¿\x0010ì\x001fP¾Q\x0004E-ä!@î\x0015Cc\x00115¡ÅD<¼mqL\x0016î®GZ#º.ötÖ\x0005KÚ$É­$³ÔbjymÈGHD¤zæGÓd¡"ËõªÝÞ¯\x0002Î|#j
,õô\x0001/bÕEärC\x00000u§whÆ` e¶ê¬)\x001dNº">õ\x001bíIØ Ù¹n\x0011'F§ø¥mÙê
YDÏÏÑþÍ\x000e6^!t:¸E¥W\x001cÜ2òftüXHî\x0001S	Uå²¼ähr5r$+T_}þöáÇyÒOÔ)Òø¤·Qe}\x0010L
D·*nO4\x001aÒOÆÜ¤\x0008Ü\x0014<Ä£Djá*Í~\x0017¾N®K½~\x0004}¡É\x0014âÁ~Ë4,N(~\x0001J7ª@5Ó®\x001bô1h£]P|ZN\x0011cì<(\x0000V5f>¸ÖÔ\x0017tÔj©eU\x0007!\x001bá8\x00086[s>ä	}öL%:±¥&}óZä\x0010%¢o)Ì\x0015éüõ÷c+Ñ*\x001a&.7{
T1/I¦\x0019X{k/§Ê®ö#\x0016UÅÑ\x0019aZ|¾p²pÈíø©µËQJ´&8gø÷?Üü¸Ü\x000fÿðü8ëjH©ÒFÌP÷î&Ê(\x001d#[äQo¦lý²(¨í Ê2\x0004\x001a0w\x0018Bû¹R?+e\x0010Òç-<]x\x001c#èC°½½\x001e÷HÓL$rÊbp\x000c¢U\x0016«\x0013\x00184ì3\x0014ÙGhæüv\x0014´!\x001fõð^:ê±Ý\x000br\x000eA;\x0012\x001a½\x0019\x0005mÐmGáCÊ"
WûÔF§\x0001wUgF\x001a\x0016\x0017e¦	,Bj¡-Zr\x001e³E\x000e¡êéa^_?= ^x·¯o\x001e\x001f§rCjRÒ>.áÞ¥K|£k\x0001\x000biCÝH$D\x001d¥/\x0018¼\x001eõ\x0005êôã?	ç@6\x001e¸hOú\QÌÏ\x0004³±¤*}É«1Ï¤+{úúXðìxµÍúÓç¶aÓ>|¢Ø@Å¼\x0013åºþ0óR\ê?ì\x0016¾û\x000b\x0003Ú&ªûµm7+Þµë\x0005Ô ¡\x0000Âånw\x0015÷ë\x0006}Ü¯$OÐäÚ5èÔ]\x0015Ô$ÈfiC>îW©GÙNéÓõÉì\x0002yQß>]°\x001bt\x0010Ð¬7´¢F\x000e|á
ä­¾¡\x001dú¸`I­QøcÍBóTÏKÉûÄÑÝ Ó/¾|0¿|¨­»{C>îîT"\x001f@Aê*rªOrtj.ëx¢:nÐA#÷ºh*\x0010åhçGrw_fNÝ y¦2=[uÒ3<Ê\x0017gáº\x001b\x000fVhÆ8¢!:¶Ü¡åª\x001bÚ
[\x00036äÃ^ú4\x0003¸ùÎb4
Í¤1aÌ21ªDüß>|ûùãÇ?ÏLcÊ\x0007eï­\x0007RTB&WBFz#Þç\x000b{\x001fÛæ©f*Æ·+­¨y\x00121\x00049	\x000bÁº\x001ewhÖûØü-ZJ æôr¨Oqhæ\x001e7hÖüØ?\x001bûDbQ~DY?+¾3\x00046äëQ³\x000f\x0012Ñd+hÔ#\x0004ªÙU¹!ó®ÊÀó3©(>}IN´!¢9ksNl;K\x000b²\x001cÿ\x001cõ\x00146\x001f­;l.lÕëñ¯B\x0019\x000cYÑSJ4æØB»UgûýÃûÇ\x000f2Æý·ï&&PÎë-uã;cpÐNÚÒ>ò¿éÒ\x0016JÓÅ\x001e\x000c³<\x0019V^m	È{:M\x001bð!	à©\x0015§}PîrT9>ßè¬±âFË\x0015®CnÏ£<LÎ;ñl%ªvä#Q5ø¼_<\x001aV:xfã\x0017<iÝ1èöj%	\x001dD/D3e$÷hCØlk\x001cH\x0008¥V\x0019¡\x0017Wd\x0012¬æ>W\x000b´Jôq:Øà·Lå\x0018Õ,
rÊN¡ùêçpª6\x000fÿ¿¨úF¥\x0018Ø¥;ìh¸B"ÀÍ¨D¿[Ò¶PÕ¾}\x0016ªQ1È4GÛ ¹E)¡e½;ôQ¡ö¤xÆ\x0001 b\x0011mµ\x000cG[\x0004dJwnÐGÚ'1\x0005'®óÁ9´\x0014\x0006hÁ=º(µ\x001cçCáL¨¸å2è\x000crÕ\x0014Ü9]ZNæ\x00068ý£á&9Â6A¤Îyæ\x0015·²Ýð¼ö\x001drí1\x001bÿ²JáÐBFÕ\x0012ôûû§ÏïÞü¡ý¯ûç·³ÞF
\x0008¸­Ç\x0014ëá>8ÆmþÞHfçòF Ú?íÓ®äßí÷ qWÑ½¢Ôyiü\x001b42wÏÒ
!xMh>àÅ\x0018Ì±X;4\x0017ôHbÕÔÌrÕ2¤\x0011ÌæÙ
9µN´©wâ\u\x000fïJ¯:=a\x001bôáÕVäÚ\x0010¨ÉF8Ì	\x0015t¶U~6hîÕ|mh\x000esÈß\x001ehæk7äü\x000bîä³®N¦k'.éAÍ\x00111%6äÃ]®Þ1\x000e@\x0014ñ*\x0011\x0012\x000e\÷Îïù~¨ÙÔ×\x001ekÐ\x0013+\x0018ú·\x0017ÑÏFçÌÓÿÍ»?7µìT[\x0003<üLäµEåîFÜ\x0017Ýh´ÚÕo74+\x0012!:)Òk\x0016PbÔÐl5
*n¯(2T\x0012Ë
\x0008Ã\x0008èe~Ë¹o"¨X\x001aIá¤2ä,Û=r­òjðÕä\x0007mÀ­Y\x0004\x0012$rXåvD94¦ðMLAÒHT{`ÛAêhj;d`ûfoã\x0006Í\x0014"Ç\x001d\x0016¥ª\x000eÄ\x001aTo£ïÞÓ¹g"¨(\x001d©\x001eÇ\x0006¥b»àEé¸m¼ÑÂJU?76\x00045à§a\x0017Þ7Ù.ø¢ £bjìÐÈv$ð\x0004)Ñ~\x0005§íHV¾Î­²\x0008öÛñ\x0013£Ö#Éüìå*Ñ\x001aÅÚ>§!Ý\x0014ÏZT7^4þ
\x0018gp¯´â¦|\x000bwÙ\x000b+2ñ¤?R!õnÆõ7åµ\x0001oF»Q«5\x0008mæyA\x001e¬c\x0006TÓï¢\x0013ÆþVË'\x0001\x0012zÙ\x000f\x0006OÖó4\x001b\x0011äªÑô¡6hæC9Ï$sH\x0013EÃ(w_c²2;4ó¡h8
[õJQä«\x0016ëä\x0017,'jfzkív\x0007¶êT&eÄ,W\x001dªEwÜ¡8!¬þÚM)G(Eä^§laÙ°\x0019)Üìã½k\x001dï$4ÈýÁ\x0001º#³|·ã]ñHs @å»QëÐGÞ:À6lË\x0007ÛhE:NhE¢=?¨5í¦\x0001émG'pÛ×s¢·Çv²èáùO\x000fÏO\x001f>L$Sµ _
û$(\x0012\x001a,LlõËoáâ|aÎ¨êQ)r W\x0012¢µTÙöm\x001fpC>RF´Y\ð\x0011²4å¶ÓjGôæ\±
M\x000f@J.tSÔ8¥WÙ\x0018Ö¤ó:E¶\x0000R¹Y¶ü6@M¿ñÕ]X°ù\x0014\x0012çxo
MG\x0013µdÙºso\x0007Ã3Ù¿¤Põ§¿À'J'T"]úvWDk+gÏäëv¬'ÓPÍKPw\x000fÅ·\x000fÁ\x0014}BèÕ[05[]é<ÄÏ)[\x0003OCXn¯½ÐQ57(	ö#±C3ÝÇ¶[lHQ\x001fNª8à2ÑéMmÕ
·6$n\x000f¡èù"XÕÔÓÅ8Å\x0017\x001b4ï?àãè\x0017Ée¶z­S,mæM\x0002$?Ç\x0006M5oP\x0008à4l¹\x001d\x0015
}\x0013w2ÏÍ
>¾ùíÓ»ÇI6?#\x0008
q2ªTS¢\x000e\x0002#9Ô"k\x000bÀ
ÜsìGYt{z/34ÁÏ|nznÚUR\x001c\x001b)1(¥&ï2Q19;ô\x0019 V?Ç WR<«Ì»2zmfG±O@º¤YµàÄÎlÁÙ\x000f¾z-¥I\x0005®CÇn\x0019QsîeY¡Yñ²=ÜRîS¬^\x0006Ø\x0011à}´!ÀÚ]áÊDtETxFDî\x0008`$\x000c±ë3ÈÆÚvöß>üËýçIÕ\x000fE)¢¾\x001e¢\x000fç+y\x0019Êx\x0003K"ñ/\x00193ÞöOù!\x0003o`ªÍOäÊàÔH*\x001d"Z
õÕf®ïÛÝ,¨®4U¸ ÑA4gnÐ¬±6Jè\x0016xQ\x0011m.ì$]ØB§\x0017wæµ\x000b9Ü{
rCTg­\x0003sù\x0006Í:k=×øô¥z\x0011|Tý¨Ë½Ós¾A³1§\x0011Y[çá¨ý\x0003\x0003j±Ò7d6åÔ>ô_0\x0017ËKØp\x000fiGê78|æBó/ä¹Ë²Ó¾æ^x6ô\x0001ª*µ\x0006\x0017ùT\x0012ä Ë¶bT\x000e(ÌÉ\x0001Y±ù\VRV>Ì¥$¼\x0013Ñ6@îs\¦ë,Í\x001b$yh6|xô¼ª-»H^V]¦Ës§\x001b63Eàì¶%ADL5\x001a¼d>\x001b\x001b6£\x0010øÂô\x000e=éj\x0016a0-f§Ú/|1²$xÄæ\x0016\x0014,BK>¥b+:»½rÃf$\x0002Q1lR\x0000'/R$íCö²sÿÔ\x0006ÌæëÒDpXÀÞÊ¶h¯6Ä-oôÈj\x000e½#çåPÊ"m&&Q#!`4\x0015VàC¨ÓfX<PHHÜM1«Ewec\x001c\x001d><\x000e\x001fÅ0\x001d>"Fy@¤þSÅÞ }\x0012Ý±\x0019É\x0004#g¤°L{fØ(\x0003ãê»ã£ïì;ÏÂÖÒXHAô\x0000µ{Äî³ä
>¾ùV\x0010@/Çc¶\x001dÊWGXQ ¥gû&ÞLò68Õ¦Ñl¼2¡\x0002Ì\x0014\x0013È©>Y*ñµW8ØmpªM£½\x000cugµ nq\x000ehï¥¤óe0\x001eBõi´Ug\x0016nôR\x0018ÍØV­>ãRw3\x001aáT\x0006\i`«nþj\x000e¸X5UI¬\x001aç\x000eØªE\x0005
:K
v'Ë\x0019§ä=Øpª\x0002û\x0014\x000bYoR0«U/LLcê¦@Òß:H,HmáÄENïuX-÷b>"0RjOr¯\x000erT\x0015½hf½aÅæhX\x000cÛìöÞIÆ\x0010zyµGÞg¼c³c>2¶I7\x001a¡\x0002_\x0010>~f1cf\x0013ÇÚ>°MÚÊ\x0012Z%ß\x001dô	gJíÍGe\x0016 4l5t¯}kùzlØF§RX@Rmauæ\x0015F¡æ}ë3b¹\x0000;pº|ABé\x001dû°\x001a(ÀD»0G% \@6
ÑØ`¹\x0017;6\x001bj\x000bs]:6JhÕ\x0007\x001a:Ñô$§¸C3³)¥½ÚÅZ\x0014Á\x0018Jçz0xò]6èÃwA¤á\x0003ìdë©ª$'?d2+i\x001b20äÄ´\x001arê×,G\x0016uÜ¶èÅ'7*iû3&8\x0007N4z 	2du½êãÝPÆDàã\x001a\x0014\x0001HMíNC\x0001u\x0016ü
Øµ&Ëyl2û\x000bllr¿lùH\x0016«\x0006\x000eJYæmÒÕRþõóý\x0017ÿÈúïïÔìä§¤j¦[Ç3XeÇX¡Ê_½xÛþß<}7\x0018¯¹â]µî=Ó-Lf®÷kÍú\x0006²\x0017+êGIJs¤XEÒ=â^¢\x001e\x000eY«èMÓÆ`<I\x0002É´iÑ%ç!,¤]%6\x0001>ªL\x0012Ô\x0018y\x0014H_¢+/:9\x0019/.\x0014®3\x0001>ªLRÿÈlCh(\x001fóæ'(Ê·IÚ \x0019	$8o÷Äâ
1:ÅAÊV&if$\x0010¹\x0014u\x000b\x0014ß5ªÞ÷ª©yµA3&mÛ\x0001¶×\x000e\x0013UÒ6W<\x0001
ÜJ&mÈ\x0003\x0012	\x001bÛ¢éfk\x0017P\x000bf\x0007úQe| z>¦ÈS¹&K¾ù\x0013bôFÍ©$£ôúëÏ\x001fïçñÂÚoÍEÍÇØÊ®ÀquK;Â-Ü8/¬»¶\x001dTa`¢\x001eú£`ôVrRóå;énÈG< °z{C.jGÛZ\x0005\x001dÍÂë\x0006}¸±$>ZÈEK}Î9JhMbç\x0006}xoQäò©UGô4èªDKâÂÎ5x\x0008û\x0008_\x0016Ï¤\x0006Ò\x001b\x0016WR\x0003V\x0018\x0016!ùõ÷?ÿÇöÿþçOÓ2#$>Ãnø#Ô÷G\x000eK\x0005ÜÔa«//HÐ6êÄ\x0008Ií\x001cÞ$¥Ú¤¯ç³¼\x0008©2`VsVhö\x00067¯úHó¶¿JáB\x0005Cá|eS hf\x0018Øtª\x0016&5÷Ö\x0007Ñ{Øþ)Mh\x001b4Kc#dÛè9¯$+7ÄlfÙ¡àÑ%.ßÎOR
\\x001ee:\x0007\x0016Ùsæ±("f[u`\x0003öÚKG×Kúh[u6yP\x001b4\x001e]àÑ#Õ tdZå^'W¾A³Kóøø¢«ÂÚ=&\x0017
=
8WtVd\x0016;R=\x000eNF9k;¨c½\x000e'8'¾¢x"	òDö\x0019iüQt`i6Ê.E<Û\x0011\x00117L\x000eRMºxå:ÀÒ\iTFVhv°K\x0016\x0007KiéNRå .â£ãÇ²\x0017í4ñ¼\x001c`I³¬º@î«QÀX±YÁó:\x0003Öva9*
ÂC£8ÎIõ¶úÕ~x~~xóO\x000fz¤\x0002Ü6#*¥r_¶ìºCçùê°ò`ná\x0011±å'O\x0019·¶ª¸NÃ\x0002/¡0VöHJ\x0014~é9åÛ6ä£äíÅeE¦öª\x0008é\x0006­JÄ-6Ó+6+Òà\x001f\x0002ÄI_Q¾!qÉAS\x001b4Û\x0010?u\x0014¨ÙR²
²Ì\5¯'\x0019È
úØf9|ZLh\x0017\x001d:d»e\x0016!9veÇ>*÷òÖìbyQlIc?IÌÞÙ¼
û¨±SRIÎ|\x001f²\x0014ûèepkè~þ\x0004áæ\x0005\x0004v\x0008)K&ë³QJQGFÔZÿgÑ	o\x0016ö\x0003Ó¬\x001b"(mâÄ¤ø\x0017\x001dã}£j\x001fsu\x000b÷ÃËÚ\x000bQ\x0000u\x0016\x000b%\x001a© 9\x00101«(>Û!-\x0002ä¨½Q	Úñ\x0014BUD
CZTk5ûìÐ1D7óq "D1¾¡<²iQù??ÅZ\x0005Èùê¹`>
¯äö~HkHÅö1µ\x000c£!Xo
Jf­¨U\x001cÉ¶\x001cÛ\x0011£$@²*)3c:¨Eþ\x0003+IìÄGáÌ\x0013EFZnrÁÔêÝ 9±\x0007XQ¯-:þ$Z´lDò*6ûfÁæì\x001b~S¤\x00056Ô´ûY4\x0002çýTû,0¹
"q\x0007uôPÝFÚº \x001frþc³Úí:ûõÓóÏÿ1i°HÙ&\x001d°6\x0006$ÐÇ-Ü{]µþ\x0016®³êüK\x0018m\x0017UÞ¤\x0002*Ú×\x0011\x001aFÍýÅËvç£`7h6.«ÅÌ\\x001aµ=öÂ®®H\x0015/\x0000gÉ#íÐl\Ö*\x001b»C\x00175«¦5¨hË\x0012<Ø¡Ù´¬$Ú\x0000'jçµ=þ\x0012\x001a{Aí<@\x0000U ×G3\x001eÉ/¤¶\x00165ÀNÍ=E{ÌPù_°Å0ÂÅwÚÄª\x0013@¬ê`é\x0001îØ|` yî¿l4&\x000fmÃf2ÿíR/GÎ¦Ò\x0016ÉuWYTÌZñÍdþÛ\x0015Éâæ¨¼+¢
ö7ë¹;ôñ)IxÿÀJÁ­h¨Òc& ö¶Ëó\x0008»\x001550\x00125Aë\x000cõ\x0017ÉqmgµSíÇDNRÃÂXm\x000fLïV\x0011Î\x0016;Ç/ü(þBtÅGN¶`Ö\x0016ÀËÏù<_\x0001\x001d\x0017y>ü×ÿòØ.Ç7oÿçÿ\x001fÿøc/N¹ùcõ(\x0000¿iâ\x0001ì\x000fÏ7øj¾ßî-×î&í¥Ji6ó`,òfëõ³OúêÆÍ¿C{\x0006\x001dîX²4\x0005\x000b«\x0011¥§Ò\x0002&KwG\x000e\x000cYPn+«ªåmîÐÇM\x0004|ÑEKS·ã!ÍÂ\x0015kÎ\x0018²Èúr\x001a\ÂZ®\x0006k6Ä\x000e}þè`Ä\x000e¦Sw\x001cµ©¨7ÖÒìÚ¡+®}\x0014Æ>Fª["\x0016;^É\x001f:ë¸A³ª"¥a\x000fÞ*æ\x0013\x000faL(/}\¦ò5k-§I¥!PvÑÆ\x001cTbzy¬F§M·u%G6¨!\x001fU
î·-&mzN\x000cÚ3js\x000ejØt¬Na\x0017ËMVtÛµ©ü×ïîßßøôñÍï>N\x0014"ÌR6\x0013BÝ#¿Ê®µ2"¯Ü\x0018ÇË"ÿ¢i·RÇ}Ù.\x0016×iW|;dk\x000cø>\x000eë<zLÓn{ó\x0003\x0013Ît¹ª\x0018:9©~
!ýêEÓn[XP¸Ð¸#GE¶Èi&0P8,uÛ\x0015\x000eÙø	×.L)pX¤X<,¹»³Oè8zÎKôô³#\x0003Ò(ÅÑ!:3ð/ÏÛ\x0016Íg¯\x0006"%Ë®,>\x0005t\x0002KÏlæÍ	K[É\x000ewrÑ9«ý\x0018°0&Æ¾v«MÐâáõ³Í\x001félË.v¶½:Ûe\x0002Ø·ü\x000b¯:â§ÊGJù\;ÿæ¹]\x0006?Îìá§Á:üÙ¤	 ûü^á·ÿYtnáj{¡ÎPÛDy·y\x001a?wt_EDÑØE	áU¾·:
6äCÈÞÌBæE\x0019(µhNTêR[yÜ¡\x0003FFøhRÊ»A\x000b\x0007¶­:z\x001bô1CÁ#R\x0013[`(\x0004©ù´ ÎGî5'ñ\x0006}L:°OÏOÉ_¡Ù8\x0002ªxÈ%P\x000f±ßQ$\x00135\x00111ÝätoØlGba
Ú4«õNî5\x0008JwÍ®®\x001dí\x0008\x001fX\x0011\x001dª\x0012t*2¯hþ­É^¡Ñ]>"§\x0006©\x001d;]Æ\x0006¼¼ï
¿4=ÝûGé-ÒègiNoºÝ6>\x0018ûõýóýóJA$,\x0007rÞ#ÄMj\x0012h#\x001f	Ø\x000br7poF¤Çõ\x0005íãÊ%\x0004ï\x0012/\x0006aP\x001c×êQ\x0001\x0005\x0006íã§i´\x0010yû\x001dú,¼M\x001aQ)[4GSSb>¢sRSd\x001dí\x0012:´¥\x0002\x001aÐd\x000enÐL°Åq?¢\x000fÖ\x0014r\x0015ÕKÙú\x0006L!Ë
ú\x0008Ï»'{¾ÔegÏG\x0005m«MnÐG¾\x001b\x001b\x0018\x000ez¤z¥67q¬«3gBlÐG|N¢ù(aAôý\x001fÙ\x001493d\x0019k4zÆÑRÉí5éÕÉ
N@RFo=i¦\x0003ÞnÜ;y®«\x0018ô\x0013|A©	ô8Z¨OÎNi9)í\x0002RI0\x001b±vhdG¤ð¡3}³Øìv;É\x001dYfíY}ÞzÔ-b`Íø\x001cÐ\x001bP£\x000fÉ\x001ef¹A\x001fF\<6Ûiåv²8#X{°Õæ­§èÒ½Áæ\x0001@ð§£-÷>tÖ¹Õé­Ú¼ÚD.è@Àò\x0000JQw\x001c0,vlv¸!qÒ	}JYÎ éÛÆ§<ç×Wl_'Ãa]Ó(ä~\x0007ÆÚ^ptLe>ÛÝÁÆËô<ÞòAXæ§>$²ìd\x0014J%ÄÞUi-IðÁ¸8I£ë\x000fë\x000f2×6 E\x00160õëÏöÃ³ý rëqI9,¶l'ù¸ÐDýhK<Û\x0012ð\x0017I:QÕ`º @\x001cíxmlFÈ¬ºÛ\x001b)Óq-ú_ÎU\x0014ß (@;wì¤´Ø§/ZOYÈÊpn\x001acuµ\x001eÙè'êÊT6\x0014Ô\x0003áz¨\x0006Qé8êò7PeJ\x001aS#ÓÏIV\x001d±\x0018í!Ts5¢z\x001aû</_éJU\x0013Ã¡\x000b\x0013.¿$v\x0007Õ!c]s\x0003Þé\x000b'iÓ&*\x001fÆ¶VVIlwªl\x0003¯©ª²%W¾#\x0007Ì{Oj³DÎE\x0015\x00079zv>¬zð!¾ü\x0015­¨~N\x000c\x001aÄª[8\x0015Åiu2¢Z³E,ß¡;4úÀ@Ûó$ÉÎµù\x0012ò.j\x001bd%\x000c6èÃ-çÅTT£3+i¹¨¯h
úlØÌÏÔÂ\x0012Ø²å$	&Óºa\x0003[7Oµb¥8â
¥öiy=§s\x0011\x0004Wq\x001a¤ýëf\x000c\x0014ÃþªýÓý¬Uªhñ\x000c$ñºcå\x0012Bt*Ý0\x00191çD¯m\x001fUôJº\x0005Ç\x0007ò\x0015Q}Ôå\x0014\x0015·(:\x00174ýB<÷£úãS¯Ì!VYvpKÝhNÓ\x0003Z \x0004¢	\x000b*ìY\jí3¢1@Ú\x00137öã¿ø4/s¥×\\x000e\x0019ÌÂ¿m\x0016Û¥<oá<ùR\x000c\x0019ÌÓ£Ð6Pu\x001b*©±-ô\x0010ýw$Í ö#fS}Cf]\x0014û3QU¯\x0006Ï¶­ÏMÁJÙ Y×`;õ¬¾Ôîl_M<79ô7á|»®Ø¬¹¦ù|Ch\x0014¯êH\x000c2°+`è\x0016gS(üë§öq¦ùF¤¯CÞ»g\x0011\x0017Nï¶Gai¦½Ã\x001aé¼Dµ8ëîYH¼ÉÌSk§>A*~µs`
¾Ú¡\x001eLæ¾U
\x001c¦Q\x001bRl»:Sùq>z\x00051'æ\x001cùH\x001a]¢¨9ùR	{!'¢©
úhèÃ$\x0005\x000cÖé]ì(±ÃìÌ~¾
ù°^lW4KTÅä\x0018\x0001PÍ\x000cZÈ-­å¬[~1ø¤î%×ì½:ÕÕ4Þ
\x0019/f®Ð\x0018=ÈÄ]çÇHh°\x001bã6èãPp)z\x0008Üi¥l{É\x001eídÒ\x001dØ²+Ï\x0013D§\x001a¬SjÜ\x0019¢9ùê°còU»¸f§1î²7\x000e²º=1\x0002Ê}[Du\x000fï\x0012Ûö\x0016_¢:àN\x001fð^Âún¼üï\x000etb>òèÕìSH²I³s6­px7M)6óÊKå4Ô­þ\x0018RJù66Ú3\x0015­¼\x0005 
´ÓõàÓ\x0018ûÓå\x001bC3\x001b@~Ù\x0000¼ \x0011\x0015èâ^n=\x001a#Í\x001d\x0006·ð«\x000f\x000fïæL£¾}9|.á6\x0002\x0012i®!S\x0001 \x0015v¸\x0011-\x0017ËÐ\x0000,f¦µûXf\x0000sp"SÔÜUoF\x0002NG\x0002m·¸£\x001bèò\x0017Ï
é;\x0008ÁTÌ¦
	vÃÛ¿z\x000bs{Ã$ò2ùæ¬]£c\x000c¤éõ>±ýP¦Ö å ·´Ì\x000f9k×$5\x0004òÕ«>Kv®ØGE\x001a\x000b)­³½v^êâd"$
ì`F®ò	äL²ó7\x000f\x001f~þ÷\x001f\x001fé\Íò:E¢=Ö~m/cÕPüÒ\x001cw\x000bfF:8½·öñä¾É\x0001Ùës$öC\x000eÈvÅlÃÛ Ù»_\x0004g¤\x001e¤P\x000fH%µH,ÿsX%¾ýïî???~GÃvÛNÍúòm½R¶îC¬\x0011[ÁDÈ\x000b%Ànä-ÉbXº¨Û6ªOOÄu@ÊÕI&ï¤çQíËjG>¾|û¼KCRH¢´(h+&Ø¡Bd»øØØæâô0\¬2YG¢Bú
©,ÄÀÊÀÅ©á\x0013Í\x0001Õü¥\x0004wÊÄnÀLâ£½0L\x000b\x001e\x0006VóWj\x0016×~Gfâ
ÉóÌSû\x0017`&&É¯KÁýÔP¾A3è\x0019Ás\x0011Ð¹
ë¥IIf\x0016bÅæªª\x0001Ü°ìÞ*\x0018«¶EU7h\x0010ËfY,ÒjimÙj|Â"P~*^lØ,N	¶6lPªwmÙâñp\x0010ÍbþÍ1)Aø¨×Db¦awã3QnÃæ\x0007»rMÒ#Èugiææ×\x001fá\x0004jÔùï\x001e>=þø8­Ý©ù
²ù\x001a;·\x001c+}\x001fù\x001e(¡oý-Ü¿/Ôgl»§ÝÔ²u4\x000euÞçã)©kÒáéUß ù4rÏù\x001b@\x000e¬ÊÐ~éî99\x001bòQ\x000b£ïØwÐú«çoh
¤ÜÙ@Êb7SBQMr\x0008.[mC;ôÁÜ(4\x0011±Ëh\x0018\x001c¤0TÀAëÍJJ¯]öà³aûËØVWäþ%E±¼Ìù2í?+\x001a\x0015[Ð-ßó\x000b!Ë¿\e¸í=*É¥¤z\x001c\x0003\x001aò­\x0018A6ñEÿùLqp\x00085\x0005ðÕÄ\x001e¿.ý\x0002$=ÏÒ\x00054U\x000eo¤ãÒvÿOZÛEÕ1¥Ú*M*B\x000b¤U-6$©S¿A\x001f}-Yfo}M¼ö\x0002Ä÷È¡\x001aÙ\x00158ÍnþüæWOßÝÿi\x001aA\x0018.?ZÆ äÄ ðùflíÑp§ô\x0007¬ãbBh(+dAûL"Ü¯íä,ã\x0000O\x0017\x0016\x00068··'3)\x000cÈUîµt¡}²5]à4À¾\x0004\x000bÀúHê3þÖ\x0006§\x0001Î!±ö2õ]R$miQ8Ío¦ýàÏ0J\x0015Ü
Äë«ÅÀØ\x000bC.w\x0018î$¡FI\x0005Ãj\x000fTÓå2§bSs«\x0014vöè¹¦\x0008,_óõ÷\x000fï\x001f?ôtÈÛ¡æ0zñvÄóî0RÂìÈe·hôßåÚµÁÜNê£\x0012Åa^íCU\x0015$'Û=Ûã=\x001aH\x0014Q<Æ#\x0007QåéÚ3-ÓÏ¹¦s]\x0018\x0000Òéþüæ\x001fï?¼}¾78ÚÉÆ?\x0017â	'3>µ\x0006¸<Í;Ï<X?ûÑåK³ëÙ4cb¶É^ý"õÛÃjIÈîÈGoiaÔÑ<îIEEöFT@¹Õ¾wq§Ê+.×\x0004ÃãrÖ\x000bu\x0011,¿
6°\x0015\x0017ñ}Q¥ÚáH2uàIÅÛ \x000f¥d¶â¨\x001cáZ½ÌUº\x0018­ð{4áàyiG$ß¸&5uqÁ9ðX¡\x000fý-HÎlV$eänxHI]ÚËÐ>öZôÈöÅ£X|*jñY-ÞÈßgTbë¿~GoÂ&]	©\x0016©VûXò¥c
Ú\x001dÀ|.wJö-Ü\x00086Mîä±´Í\x001eïÚ/s\x0011UMv^
`\x0016çL±
ûx\x0008<1´\x001d(¨\x0011©:I\x0004H¥?97\x000c¬ÐxuÙçkUy¨_=|ø¿îÉÅøÛw\x000fÄÐæ`\x0014Å´ZÄ©\x00173\x0005!\x0005\x0008í5¾b\x001d\x001aëU§çÑ¾Oc\x0012\x000eFQâÜ¾ú	\x001bòác§2Ñ\x0010\x0014BªøÚ²ç\x0011\x0016U§úWðâ+`ý+ÐÔFÛ +.¬ªî¡ iÐ¨VÝÇ\x0019ÓF+6K\x001b5À»ÌS;I¶ZP[´ì¥t¸`\x001b\x001d^d^^û'¬ÜÎ¾ïò/¼jïÏ­\x00167\x0003s\x001dÅf>ïÿ<M7ÚGN¥ºþZÚÍÔ\x0015Äj-¨]'ð\x0016¬Ù\x000e\x0017Îm\x000bQ¶§ææÜevAÑô#©LÕ
\x0011.´¯\x0015ÍÞ(ÛS[E¨=\x001d\x0012È\x0019ðí¿QD×5
ú\x0008Ö7©3m'\x0012I©)Pò9ºØHõk\x001b\Xô\oá»ÛSXN®wÛCq·ß\x0004ü\x0016\x000f\x0006\x0006\x0015¹\x001fU:9Ù0Q^ã
¤\x000cN;R|@dv(=ûd7ÂD-lÈ.±Vü¶è"ÇOC
R`§-Úê¥Þ¡³XôÑ9\x001c\x001cu\x000e{¹h©óB©l»[%ÊJ&a{¦RBýN\x001b¢ö#\x00185w\x001a¿ò?ÿûÿøêóÇy¬\x0016Õü(ky°p)EBìFR%6ñÿü¾\x0016§¹ÔE\x001b­>«Y PÄh¦¶!¶VÁ\x0006Í\x00183.ðA\x000fÔW%S%ÔÔ%¡\x0007\x0003ÊJrbÏÅÊ/\x0011$S@Q2Ð&<oÈ¬\x0004L¾TÎCcÛÉ¦W#»ã]þÅÂúÝãû§Óò;\x0019dphôÁUË¼LN"A7òL¿¬\x000cL{¨_!Þ§ } féAµê\x000eÍø3û¼\x000fIJS¶gY& \x000b&Ågf|DWyjÛ\x0013?J(Q'OÎ\x0015vhÆGDÏËµ\x001e[1JÙËXjµ^
:1è( }ý@\x0018e|C\x0005VëÙ\x000fO¿aØÁ$u{A¢D/ÛãRU9%6èÂ 'éN¹\x001fj®eBNé£
ø øÔ ¨óí? GÖdDyIÆ¾=:ÔS£,Ø°¤µg\x0002ëÙ\x0010ôY÷Ã}~óõSxx÷&Ì|þv^¤ß\x000eãÜî ½
H2zÌ¢\x000f-\x0010Ì7\x0012êÛN¢Ñ¡:ã¨}3Ç¢wRN¬¢z SíÚFÛ@q\x0016§IE\x001as-¥3ÀÓè®Q­q£/ñåÏH«6z1Öe\x001f½\x0018D\x0005çÜBv\x0001"	\x000c5C5N·\x0018ËÀ³\x0018ÐR{\x001ea¬VÎåðæ \x0006õõ@¹À¬x)rJc\x0017H82Dâ±¢Aq·¢4ø²\x0019}´ÚýÊ(*nåñ
íýÞUKEu>ªj4\x0015ÄI¿XR¼Zx SHà­¾»\x001dåê\x0010X3ËI¥êª®Z;´¼Ð\x001d90äÈ§z¸äTÞ«¹\x0015Rü§WÃ\x000eÍÒÄÄbûrËµÑ\x0000iëiß Z{¢l\x0007\x0013/Úã/Y-:B
\x001b2K1¢H\x0010g^l+&\x0005
\x0003åE]Æï\x0013A^ÖB¢\x0014£ÎÞfÂ®Ø*ÅÈÝþû29ªî¬ã3Yuæyâ*n\x0001ÚzËã\x0000ò"ÿ0:!\x0010Ågdì\x0014
ÖLºfuør§çomØYìHb»Ý\x001e¦ÔÈÓ\x0016\x001dî/µa³dq\x0014¾C\x001dº(KT\x0018{¿UÛMRf[éâ\x0018fuKÉCh4Òà"²t\x000eáþÏÏ\x0013Um\x0000hIlæV6AgLh\x0004»zÜË²
´*£Ñ\x001bG\x001d6\x0010é\²bAÞ±¢5uG>"8\x000fÈµ²\x0011ê\x0015C¹Í\x001aª%¸C\x001f\x0011\x001c}\x00088\x001824°R23\x0001\x0005»´ÅBé\x0002¨Ã,/\x0011Ûª³Ô`¢a%\x0012:ú³Î
\x0008ç-\x0000øæéÃýY^(;¦ýiHµö~Óý©*7Ã8·Ï)öÇ7ÏNÈJÒ`\x0002!}Ü6DUlYò§êî\x001d\x0019vâº¤\x001e&ØÊ9}f\x001bá\x0018öÒjÁ\\x0012¡×Ö\x001d\x0014®\x0007Á'­¹\x001dûÜ\x0013MjMbÝ2ÿ\x0012½ÔÞ£Fa#«ck-ã7Ïï\x001aÔ´äXtN=­û\x001eAb{uåöÜÂµ\x000bÒç4î)7Ö¾«\x0018|\x001b½Ô­ÈAÍ\x0012Á\x0010LÝ
wÊåæY0	«\x0014¤\x0012]nQ©Wïµ)[áNù«A\s¹è¢Ý\x000co\x000ev§,\x0013ñò¸U»DÂ&¨\x001cº¾ó¹Ø}Ê\x0005e 
ÖuÞ\x0001·^\x0019\x0014ædæ6h\x000bêÜK\x000e$Á¶}d\x0019ª`qö\x001c°
Û_Ä6x ÷·\x000f÷\x001fÞüæéóó·³:Ls#\x000bÚç¡hgù%\x0001y(Ð~Iè\x0019ú[0_û½1H lÆ"3ßâeB¥m\x0014çÀ\x0018­Q\x001f;4SvÂ(ÄG©(\x0013%´|É0\x0007\x000f¾C\x001fö\x001b Ü1\x001bk1»ðr)^}EgùE;rbÈUTÚª
Ú\x001b´Eê=Ö\x0018
¡°ohðØ§it/SâÞ×^ÈÀÅ2Öxá¸¶dK­³5C\x0007+YÊ\x0018ÐUaOI 
±lél\x001e¡an@LNv]0#£Õo±#{ì8ÿ3¯ÊÊ\x001cZÈåµ¯XÌ$Ð\x0006Í\x001a(\x001c`-Ü\x0018Ä8K: 	äª£i_\x001btü\x0005?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-24.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-24.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=~x÷ççoïÖå8g\x000eZ\x001aôì\x0000K0óhUÕë-ù¢s?Ë.oD\x0002ôÈ\x00197É¬Lº}Å>	}\x0005\x000cfY¥voû£ôý,xøÎE³\x001d\x0017<ÁPAq6µx3±§p²Z\x0005Æ¶F .î¶	H2[t\x0005\x001c+g{bÚæ}O`\x0018ëÓf
È#ÉçÜ)M«mUëNä\x0011\x001bZ\x0006if2ìÌYpëÚãÆ\x0006Ô9¯fj\x0000

«\x0015
§Íl\x0007ÜØEúÉ{â %³3\x0010Câ4Rmì\x001bG~Õ~\x001d\x0000\x000eâ§ù[Ç\x001e3xWÇ\x0003ºäèãWÌâ¹NÍµl.LnIMP AÙû ©\x0014<ØÇt#êÃn\x000b²'tU;4TW£~rùtª\x000bu\x001fÔ%þ°V-ÿäÅ\x0015ãÃg×&Yç\x001c¦Î«\x000eÖ\x00009!ntLSv¥\x0015¿×ì	þ"¶ªóMôqJ8ËÏ¦kÊ+ñØ	\x001dyÕ°×.°ÔcLlMMo\x0019_ÇNhÜk\x000bc\x0001\x0012¾Oªy²ÝôÛ¸\x0012Ð\x0010ì9\x0003ÓÌ6%3éa8e\x0004;SÊàv!§¹Ò
¤¶J\x0003>I`2\x0007»\Ê>
¸£ ¸]\x001eþ\x001blÑ3±°v\x001bÎezÊÝ®H5+\x0010üîáÃ;ºþúX1ÿÏ·Ò\x0010#¼*µÑ\x001bFz±_ÞáQäÉ£ðwD\x0010¥Ä\x0013A\x0014	Ñ·º'2tÖÓÊ\x0013Î5N\x001eb\x000föêáÏÓÃ¯u|\x0003D\x0001ZÖ@Pc"k£,Û<Û<,BðTKÖ%S\x0013kM¤qÕ\x0008)ö>E|tºæÄa¯x\×·	¼IåAËß\x0005´\x0018äêL¦·\x0016\x0012ïW·<R'2\x0014©y\x0004Nxp&­,é'ÀfÛ]&ùË«óêµ»ðòä\x0005H¬IM£\x000e]å)f±+û¶ì2)ShoDÆ¶lMbÌé´ë C¾(\\x001eÐÐv>¡)`ZL}á÷\x0017eÒ¼PdOÔ\x00179RNí)D³ïÊ>¡á\x0016æ\x0002y;}¨T\x0013^sèÛÕ-\x0004÷*à©Ó¨`=7]ö\x0004U'.ÜAñ­ {W¹*m\x0006\x000bÈûËyu\x000bÁ·
\x0015«Úú¢½§E\x0007?-ºÓ&]ÝBhÉ\x0012Û;¸ß²ë\x0011§Ñ¾\x0010ÃEMû@\x001e×0Z¦§\x0010ss¾Î$.CZäê\x001a\x0002­B¶òÚ\x0014FöÓvØ\x000bO3Of´¹>\x000eäÆkCû1©M\x001cöû'ô¸\x0012¿ÇW&N9\x000cÃdïV\x001do!÷¾\x0013\x0008*JwCc¹]ö\x001eMê³Î\x0014\x0008ßªßóù\x001bu\x001dîñÌÌM,­ç½çtDÂB¤7í?~å	î:\x001fèï >cùÑÌô.\x001fÛ1}{é\x0017ëU§Eöã3k_k4<1\x0003¥Ü|æ¹ñ»\x0017ùywâJ\x0017//ò¶\x000b7f-\x0015ï­c|\	ÛÊ\x001bò[]ò?ç\x0013/5\x000c\x000e¥UH['¸\x0003Y¾wÙR¥À\x001e±±©JÓL4L
 \x001eWÚe"P,\x0007t0	ò¬)JY¸êåçî¼Äº\x000cî\x0019ÈG¯æäh+\x0002ë\x001ah\x000bÎv\x000c .\x0013vb\x0015Èkø\x0018¥'½ØÕ­ÃU9¸søê\x0019Þ:\u3\x0005î¨B³^
\äõ.ÖíËw ÃË'\x001e\x0012hÍx±êä4\x0007CÁyõ¥e+vÈíÜÑ#¢lú@À`]rq\Ð¿ÖcðÊ_À¡¹)ù=\\x001aX'Ê\x0018Þ\x001a6ùþZV5§ßýô£ç\x000fïþåñãóÓ»_}ÿéÃýÄIr
e²ªö´È°\x0004q\x0012çúÃ×Eþ´ÚR¦rZ.F\x0008\ [,{ÀÃ<ÅíYjNäñfårÞ¹§VI<¦'k[M;qAA¤\x00113éÐ\x0003Qúù\x001c)6Eîøæ0Õ©Øû»ÇOÏß=¾ûÓÃÇoïsz´\x0003ìÎÕÛsrF3TUÎâ«AµfµMUkyÖ\x000cÛÔDzn¯@\x0010·ºfv\x001bîB/@º+hÐ\x000eãÌ O\x000f¥d+èën
WØ\x0011°U®tX¼Z,Íè:\x0016µhÃì¹õ\x0013^@'ÖéAïScm%1%.ØJ
½9 s\x001eRíÜó·ïþðýÓ§¿ÞË-·:#$ (ç=ó²ßaÜ_¯\x0003coÜËÛ¬O~õ4ex+ééïàq4ï\x0012Ï_©\x000eÉÖg]2\x0015BÆ\x0003*/<=Ì¼íE¨uÖ_òÑ
\x000fH³£þmï8/¤9ª½78e#\x001bF»k_3R|¿Coq<(mV»\ge'ï\x000bùl© ÔS|ÔBØ;è¬W:!Ød(\x001démÊÓ!ö[êÒ:¥#qúú\x0005X3\x0013ü+DYÃØîÕ]Ôl^ Ò.³Vi´ÓÉ¸ µ¯S6ò\x0010³\x0005Ñ\x001c}Ið84\x001dºPöìauÊF
ô!³yBÇÈçÙ0\x0019G\x001b-¿\x0018¤¿]C&TåÂÑ½©Ûi¾W.\x000cht*-_9çÉæ¿ XÒZKúåtg7ÝÈuÐ&ÛûòôáÃÃË\x000fï\x001e¿t¡Ø_?~y~ø÷Ò%ôiFC<ûÁb'\x0016ÉjkzËî+YÂ9>Ò=äøèâw¼º\x0005»OãæOó7ÍVýþáå¯\x000f??|¼ïïØÂª÷¦S\x001cÇ\x000b:IäÍ{pÍj|]¾^|\x0015Ý<ù&\x0019}Tøx^]pì\x0007un+èÐ¨À%Ðr×±\x0006¨a%èt{]·?¸G\x0003ÓªòÂg.AX\x0016;²;Jq9Jÿü'%\x000fVê×\x000f/ßÜër[\x0014KÔ\x000ePn¢xHûDÄ¿º(ÒåÍ\x0017Qy(Ô2{¨d©º+×÷½¡o¢*¶ºÌïÒ]ÕRN©M*GÎt°c£ZôËôÖíazK\x000e\x0007\x0010vGÍ\x00111©ÇN2®eÕ-ð5LÕùéÇ\x000fCø¾ùþñË»Íþ\x0018NOÙÆ>ff@B¢Æò­\x0017ïÄÒA£[7wÐlÇ«[°^n;KÕõü¼\x0014þôòAWõî_\x001f^díw»ä~")u5ÞÎoLÐ\x0001à0Å¿!ñ8?£¾¡[ÈÉoù\x001dX­ndæÄe¢\x0013Í\x0013ÆM§è
\x0019|\x0003ï¼e lÉå\'Y\x0013\x0014\x00074$(Ä0áÔ±oödâLÛ{WØ\x000e±U`
-ùÅx0ýp\x000fÓü\x0015¶Gì ¹£\x001d\x001ajHQ
ÞéÀ5M+ì0ag8¡\x0001ÛqB¶6¬\x0003;"¶\x001c\x0000$\x0014\x001e+c\x0019!î\x001d´WÐ¶\x001b¢5ÝIdFl\x000e\x0013¬ûÖG¿ñ:v¦cR ñ·\x0015\x0006¨þâ9\x000fª3´\x001b«ã&ïôÛwE|Ó§wV"ô;Y\x001a½-d\x0000Û4Ý9bãP jaûíG|1·Zù
Ðmg\x0013=ÆËï`å`\x001bY6\i[w}Ø7dèÃVA_§Tòtî\x0012ä++/þN{ï\x000cí!A£ G&gÎô\x0010n²\x00147d\x0010XÙÕWOÄ&MqC¾Ï\x0004ºÁ\x001d\x0004á$\x0006\x000b\x0013ò«ÿrJ¦ÿ·oþÇËãçw¿ø(ÿãËÓ;ÅdÕP'©¹Å·\x0011°Ûw\x0015dßÐ¾ ³]\x001fBÇd97ª`âÄúÕ)!eyÐ]'6ÉÊ\x001bòHVºCóëÜ j¦ä\x000eõ%gûÚä*oÀ#W©\x000c\x0019ÿÓ$íRÆ%\x001b\x0011\x0015×þæ
x¤*ÊC\x001d+.<¬íå\x001f`dßh\x00177F`\x001eÈÒ%&mYr DL®,ÑÌ.UyC\x001e©J­Fás¤\x001fyàf.ËgÙe\x0014oÈ#£ÈC³F./õ¬»Êt\x0010ÆÚmÚïD´¾£pæ¢\x000fÄá&ê§TK'l»:tÀ_·¿¯^è]§à
\x0019N³ÐÕ ÊSï«7,s,çy?.qÓ!ÎÁ~\x0014O
\x0013®NÈÞm§%nÈãtØh ±Á\x0004On®«Ì'ÊÁ³y"<uôéé0à@Ë¹£\x000fÏ£\x0013l-\x0007',Ðâig`\x001a¨Z,À2YÌ!ß;ïzînÈpèä_\x0018ã¡Fµß\x001dí%6ùTb\x001fÁ¸:t\x000e\x000e£½hYflºÓù_ö]ûýÿgî]võL$ÁW!´î&â~Y¶Tê)HÝ$\x0008³\x00132O¥Î\x000cÌ>LjF\x0002\x0004ô;Ìªw³,=Gb^¤dÜã»yÄGq38Ô¢
Ê\x0014ñÇ\x0017\x0017\x000fws³»#é²EÕa>¢ö\x0008åÖKÛ\x0004j¦æ\x0013ùZ\x001aÊ\x001e¹ò\x0010Nsï¨\x0012\x0018Z"Î@§ºjî8¡¯Ã©z\x0019Lµüy|\x0001© *Oµ¼\x0007þ¶°? /[y}U@ûØ¸íAÕR\x0008Ú
\x0005¶x·ÁãµÁR\x0019a>\x001c/½ÚÌTûA÷´Näk»ÃåT\x000eK`¡\x001d© \x000f%Ð9t _»Ð©"%Ì´¾jq¦k,<h·\x000e§Ú:úùóã\x000bRNõ\x001a0Û\x001es=È	ÊKD¾û`¦½^_kê5®¸zÏÑæÜä f½Bt\x0003ãÑâ 5µ;ä\x0006Èr¯±Ùð hn¨µl½Ñ@¡ýÕåÕ23z]å$ë½Ýe;oÄýÅÊ\x001fØ
VÓvðÞSOØF8-î½iiq2*tH\x001dNö\x001drCÚÈA/ò>#\x000eY\x000be?t\x0017§ÌÀÎ\x001e°\x001dDí©Já\x001aË\x0002\x000böò£Oõ¶úÕ÷\x001f^ôãõHÄÒC¬½-K²/EMr½b\x001a0äÔ?N\x0003bûÅõxQ~B1j{LU9\x0008C\nñú)¦a\[¯\x000fT¹Øì©\x0005¢ÎÄ¸Rg:¡%X®À³²\x001dÒ\x0010t7Ý×<dço^?Å6Ç\x0008Ò`¤{[î(,'·ççO19\x0010Uóu0Íª,k<3¹­\x0018t'2úq\x0003.¨`
§\x0016åtK<æ%%øD\x0006/\x000fyüÕz!·h}H»¬kßÍ©q"\x0002\x00071Í,¡\x0014\x0019òæKz\x0007\x000c*ê5|
9ædàI\x001f¿KÄ³9c,¢çb\x001aÇ\x0014«®x¢j¨)vã\x0012<æ\x0013\x001a\x0005Ò"(Þ$4¶B`èÝ}ìn\x0013¢â¥úê£\x001dßú\x0015\x000b1ô\x001bn¾»wÛ\x0010;óÕ\¶\£<æ3Ù×ëé\x0019zæ'4è¡¦K)]\x0015± ¶ë®¤°e×\x000cÎ7Ú¹|í\x0016åbQ÷|!\x0003Y aéq"£EM\x0003]\zKî¨¾Qñ=åÍUþnå\x0001c<´tµ\x001d¥¤Ò\x0002dXái<¼\x0017÷e4	ß~+óùÛ§÷\x001báâ[ý7/å²ËõM"~ÿ)5¡x
§W¤!~'»N¹5% \x0001é¨âõ¾¶3Å2\x001aæ
»#£MUÄ\x0019Rk\x0003v:b² úI®\x0008'2ø÷ô\x0016¬º\x0011d\x001d\x0012¨©ÇMEvÞ­;0ª\x00177èÖjl\x000f%\x00192ë;Ê\x000b}Åo<áÖ$y¨aËH!D5²uqóyï¶èíÝ¦Rà%\x0019\x0013\x00035qÑ,¹üþ\x000cç@GI]Yâ\x0004­ëä~ôöfk\x0001\x000e®¨\x0001\x0004ßÕD)ßv£ù|Ù ñfë\x0015{]Tm»Jâ
íÛÒAý\x000et(^oè\x0018TKçÍväî[ÚIÐ°å*cdjXª)[ä°¾}¢··OkhOÜL+Tåþ´1_\x0017Oôöò\x0011`èüé²d
LûD`âúò~º|2\x0016<f¶È¶Øµ\x000b~ÁÇÛ^ø¨z|xÿ\x001fþðÃO\x001f\x001c<ª\x001f\x001eÿòüðR-uóZvç=\x0011}°ú\x000c¼fÖâæX¬û\x0006Ò½Ö\x0003)õ\x001fY)2÷zsèÚ§(ªòµÙÂ/²þ¢êx,\x001f\x0014Ñ>(¬Ï{4KrèRbAËíëCwzP(A\x0011fÃÇ·æt$w,u_ÉÜÈ® è××x$ôäx©5·\x00148 ñtÌ\x0015­\x0007£3¸ì·HôniàÑ¨Ì¨«Â\x001côÖüÌi Ð#G¼:À¦ð¹\x0006,\x00076ØÊT_n9-E­NX°ÂS§«r-¸|~µhúß{^$Ð¨è¾Üï;*ÖU\x001d\x0019¼ðR`9Æo«Æ\x001d³-ÕMcxq%\x0017#pØÃ@F21´Ñ¯ÉWéÝ¢_sïWKÙPå ÞM3^Åi­ap"\x0007B.×G\x0007 \x0004\x0004\x0017´ÍeqSÔù¦xóçï_ª_Ó»D«©÷¡\x0010¶å\x0010å:Ã/¶ºù¿¬êJ\x0018}ñ-ª!Ê\x0015	¼.%¨bØÌ¤í4\x0003¾¬3dÑ\x0008+µê;u­)ñ\x0000-£(\x001cÉ]ç±¢Ñ?Ò?rÌe»PÑL;9\x00088.JNà+	_(:æ\x0002rWYFZ\x0015¾×³\x0011\x0013jÚb/¢Y·©ëì8(Çg\'n¢Qü¹[]Ã7á­Ñåij{\x0002Ì»\x0016\x0003'\x000c}f1p	\x0001ûM°h\x0004cT7\x0004ÒM2Õ&¯ç\x000b7·w55]\x001c\x0001yq\x0004¨ùÏÃé\x0005ôRbäòqoî2¾VUK %¤òª\x0019\x0012¾ÄøZ'Ïf\x0014T\x001fèª66o\x001dXôZ\x001eëk2nÌ6\x0002m\x0005¸®©mOá\x0008\x0010\x0012ï­9H;2<Àº\x0007%sW5¡;;Pïv
î&\x0000Í6\x0000­\x0015+£9ÂÄæ\x001dã7UèE0M\x0000\x001a'D^\x0011*.G>Þ\x001c\yÊe{$ÔàM¸\x001cHû´Ê¼RÎ8!¾ðüÔ1`=l8¾ á½ª÷MPmPë\x001aÐ\x001b]õÁd\x000c\x001bËµ7ç	
rÁ]m2ê \x00168êRµùgÞ-eåV»â-§¶?á3\x000f*×Ü]2!dFEWÖmð±¨ðÓ:EE.¶»lB6Á¸Z,]Z®èKVs¢â½<yÖV\x0014'4\x0004äÙá\x000eÌÎ\x0019|çªÈÝDÍÙFÍ»`íÁm*ß­úà"h©È6SáÀOÛeoq+ûÚÉ75»íáxÉ\x0010AÈý¸aÌt\x0019îò]8m\x0006~}É|öºÇ³Çåöå¡EìÕ]#óõêVj¿[y\x0001V^t\x0010êË\\x0017®¶\x0016yÔ9
è»¯\x0018À&k·7¹&Í]	Uí\\x000fé¤»	Aß°êðÔ­¿¥5\x001dÉ¹ÈÁ×$¤\x001d\x0019æC\x001fhHèÉ\x001cbvª[Úã
	iGç«ªùÁ³z£$\j\x001dýréné%Ð«Q^Èr~ÐUàKÝ¸ósõuÑ\x001aCñDm2R©Í\x0011¾jÕw\x0015\x000cöE0ø/\x000f|z!O rJõ»«Q¢©»\x0001´{ø­{ñëÊ\x0016.®Înb@uÆ* :¥\x0002\x0006ÈHÌL]Øo¢Àn¢@yy@²\\x0002&:	B±²aí1±\x0003_{ª×e	m\x0004O\x001cA^¿3Y#ïö~v9¬£Ën¢K5óºÎò¨\[OBî\íu(ì/.Ín¢ËÚ2ö½)ÿ\x0005ï6yiQ@¬å3È|\x001d·MÍ÷`6T\x0014IÙg.7æ5_b\x0007¾îÌñê¾FÜØü]
miÀ5Ý\x0005Ý\x0004­$ GEm\x0003Å´[H-qMpc\x0004¯ÂÀnÂÀZÈpÊëJ¡i.<\x0019òNY:´ÐW\x0018XcÂª ÓVOä©ÚVº°G'w\x0003"*ë¾¨ê\x001bD\x001fQú<MHKÁÓ\x0003\x0019\x0004OKE\x0006¬l\x0004{¹6Þ^>/õïOèk\x0017ÉëÌ5#Úä=C»¢÷¶¡z\x000eÂÞoäüøøðér\x0005ÙdûÕ?l* \x0017\óë ­íç/&\x0017ïÐP\x0015WIß?R\x000cÝÝ¦Òu\x000bN
>\x000f)å\x00037LÖ\x0012\SUÎè2W&\x0017×QÐ[½G(!ÓÑ(\x0007v_^@Éz¼¸ÑÍºªf\x000c5\x0017\x0006Z¢»±Ñ¼öUÚô\x000eãP\x0001î,{Ù\x0019Wî´Ò	\x000c\x0006\x001eÚX|Í&\x000cØùÁ±íHëìF²\x0012z\x0012Hx­tdI
J¦béLu"®B%eóªQ(Ú\x0019ôY³\x001aÒ$\x000eÚ;ÖGÕ¥ò$s\x0015S­Ú×7Pìn*ò0dÌMS|Pø­Zu·ÿPwT¢çH²KÅ¼{¹)
¦IvTÎrh\x000e$³<Rg#\x001dí­]ßmÉ\x001aéè7¼A
G\x000cÑ×Sá§»²\x0014z?¡\x0013\x001a\x001a|K3ÙÔy\x000bnÒ~aõF9Î$6\x0003q\x000eÜ+åôè$$¯«¤ów£»}L\x0006?\x000cã{JxÌ
Ê«\x001aòçW·Ü*\x001fþ¯\x000fú÷\x0017R
Îè\x0006Ëßyº\x0005§âä=ÕQ}­»M_ ð§fî¶ä OeS®mt½ËÒ\x000b+³à\x0013\x0018ò
\x001aG@6,5¥\x00193²[\x0018ÈhcZÁA-ª\x0019¬R\x0007<¢ÆÅÆÊærK¦ÙÐ¦Y2«ðoúVV\x001aä'2¤\x000e÷5~";¾+T%7\x000fî;dö1¹ºÈ´+¿ >.i
»ÑB¼¸ßlö>9\x000f:Q2æFºé2f&]ºî×½dsøêêóv\x00133Z÷âÀâ~³)üä2\x0006\x0011­'NÁi\x000f>\x000f¹ÜðRMá§HF²£ÛÌ\x00022'\x000b¼_K\x0007Ð`d"ñe/èLZÙÓ%¤ÇçRVûD\x0006\x001fTàY¨=²\3êÅIo\x0011æê~³)ü¤ºÚ\x0000í \x0006%<ê-\x001b~·
ÑÈ¤ õ?ôXÙç¦ñ«Pîä¼Îà'ÁOJ\x0007ä=LÆ<;\x001fø~0¢\x0016\x001d\x001aö¡:¹ ëú¦nsAwêæTãÈê@²Õä;\x001e\x001e=4.Luc®íC½aÑ'[\x001eH-£\x001dMÏ\x0002 õÐá	É³ØÝ^ú@\x001e\x001b\x0008{\x0008,\x0016Ò¹ î÷\x0012ëÝVò@ê7rçg²\x000bGQs·õã~­¨k
ÔBB1·V6¾îa(ð,*\x000fÉV\x001eò¥> K§\x001a Ö"x±¬\x0017MÛ;4ìÅ\x0014È3>:\x000eëå­Äº,q]ÒH¶¤¡¶¾À \x001cfô4Ó_¨~c\x0010.r\x001d;4lÅD6gòê2æ+lpª½bã#ÞmÅpmEm]Í°\x0015¬£öÎÌôV\x0002\4îÐ°\x0015s$5ØÍ©W8\x0017 7W^×x­ñdc ¢ììèn\x0010\x001eõÚ¡ð­Xè#»%«z\x000c\x0006?)ÞíÅ\x0008ÆB¡UÊcyD~÷ª¾[Õ\x0011­²
MºbåD5ú:[O¼[|ñZ|êás]\x001dIk¨h2oÅíîZy8ë×Ág\x001f\x0016·O´¼x¢%\x0017Áv¸Õøök&\x0002\x001eZrÑÝãGGøEp!É)·»£ÅØø^\x0008[¿FúÌ\x000fHü\x0003||Q¥\x0014@þ\x0005}é\\x0011èÿõÃÇÇ\x001fþôæ?~óðþÅ¼¬kâ¼VsáÌsj§\x000fä\x0007³jõ¾¤í\x0017³çeÏÇ°Ù\x001fy\x00059ü\x000bÕ&=¶\ÖìùdÙóZ¡%ä`YQ¬& ,áõóÇ²ç#çP\x0016Ý¹ÊnÖÊ·]?R,Ç=:
p¼×Í\x0005Ö¢¿)Ö¤â®FÈ°^4ÕÈÕ\x000cÙßÜÓDrW!¾
+##_³ùÞÝÜÓDr_/òÏn¨Ü\x0012ÝµkãÒX	9gÎ7Uf4yÏß\x0010ÝÓÜJ\x001cúY\x0006Kâ\x0015öA®-ß¨\x0006¥©\x0001U¢¬«/ÐG-w\x0001îÔª½Ï\x0000­Ô	Þ(Êhµö\x001bþK²|ô vq\x0008í\x001eUØYF 7©»\x0015\x0002Á¢ªÂÉ{oø\x0005m<§ë&Z½èè´\x000e¤LÍ&e(Ù!n^ÉK&+\x000c£ùÂ_>~óîáéåü#Sy[jí
x+jzË¢~Eá\ëå\x000bÉ\x0017Ö\x001aÁX<vC\x001a°\x0013:Iv=Öú\x0015;2Ô©Z\x0018»ºKàû(VnøwÃCx±.¹|ªÄ\x0002vGjg2d´ UQë±\x0016¯f2dÅ¡Õos4aÔ¡\x0017WÃÎ[-ÍÜ=ÅO\x000e¹sõÚsCþ&¹x\x00084\x001fË\x0019É³QÙÉßs\x001c8öíù²Jb5ÄZ.ïÏîLS2M\x0001({QÉ³Ìèì¡ãvóÜ-
¸ÔôÐ\x0006-_MÒj÷máÕ<j»«ôG³ôHÙ\x0019× <KÊÉÕ('7\x0017ï^ûÍ¼öµ\x0015\x0011fºdf§èÅCóQëþ¸\x000f8ÂF&×|TeDÑÃ¢\x0013±+O÷æ½ßÌ{_«Øµ>FM"\x0013\x0015^åÉÒn\x001eåÍ<ÊUâ\x0015(Fê0Á\x0012¯\x001b{ê¶_½y9ûw@\x001bgì¸e£\x0003®\x001eÎÍ<eScÃI
F¡F\x0002¨Ì\x001bæNXnÆzih;\x0016¹ã\x001bÕ×\x0019tÙw4²EÓ){±±h·¶Mò^\x001c©È\x0005]t7B'­ '.Å6£\x0011ß6³ßEðÐ,[»ªwìRÐÈbBÃ8ÿ\x0017u;4¼\x00114Ó\x0006G+äíi­@\x000f^îºA\x0003\x0011UL ^Ý&,sA7Ç\x0007H\x0018ù±t÷\x0011\x0013Ä½\x0002ú±>zæÒtÍGí\x0007×"Ý}Ä½ü\x001eª~rìe\x0013oGªzË±7éî3&\x0008åµ*[±³à£p[ÂQJw_1a73È#	°ÉD^£9>téå»!Où-lÄ\x0012¸MZn[>©Û(¿ä»oá\x001b&×Kñ¬]jï<êùî\x0013føz\x0012Á<«\x0000&AÄ¬<>\x0006Éôî\x0013fø¾£WªBSË\
æ\x000e\x0018Û|÷
3ö9Ä·ÎizøÊÓÛq-w3]¥ÕøºU\x001d}vÝ|Ä\x0015)wS]@ÿ¬4 	ùôÈ¬(Kz¼ÅÊÝL\x0017$=9\Ò\x001a¼à6Lä\x0006È+yZu\x001dÿêñùû\x000f}!7§X\x001dï=\x0008\x0019Ê<ªbóªôÁòÑ\x0007ÙCQL½à´­Ì\x0017ume.\x0016¦ig¨$jìY«\x001a|cú¼0M?s×¼\x0011ÄS5\x0019Ogc×Q^,x¶fTË¬\x000eJ	1ÇF)\x0002ù\x000fS
Jók\x0002{2Ò]O@`)çÀÌ6í¼§\x0015/#Y\x0013Ø\x0013[3ª]Gju·\x0018Éô\x0006Ód'Ýð\x0007ÙQÄ\x0019ÄY]\x000f	8²òë×£éíîº\x0012p*Ì{7\x0018qRÖ*êÉtv÷"/ôKr-\x0004\x000f\x00192cÍ¬_ïnd U¯÷úgÏ²RíÎ
@ËßÔh5wsU²z·OrE\x0017	:°äæ°ÂeèQüZÝÂÕÜÂ¥wè\x0018Åg\x0012Ò\x001c:à\x001b¡?ßm|mº\x000cÐè\x0004Êdå\x000b>÷ãê¯æ×\x0015/1ç1³­IR~mé|·Y2l0×²#\x0011\x0015ìÚ«q´\x0004®BjB\x0001
ûP®N\x000bÍ£\x000eC
%ßí\x000c;¦¢¤gÌµñ\x0011\x001d	Z7©¯²\x0008-\x0007tA÷Ák/\x001bÇXý\x000f#\x000fà»­X<¤\x0011\x000f
ÙÖM^ªÛ¢»­\x0008¡T© eQ{>ñ9\]%«æ·_}øôîÅºßôÆ¸\x0012Ó5?\x0001Ù·-ºÐ×.ló] ;¥\x0016ÉÜ>8\x0003ZY%¶÷MûæS2)ÞhòÛ¿_%Ý%cÈH±*Ü¥{S_·Õ%ÛV§7\x0005x.±\x0001cP{,F\x000ek\x0001d\x001bëJî×\x000bp\x0003æYf
:\x0001^«6$ÛW'¡\x00110\x0000Cù.fâ®÷mÝV¦¶:MLá3;#ËßIÎ$ÛU7®4Xq¾¬\x0016\x00189\x000cCÅ1;µÕù\x0004ïÊÐå\x001ev¬&<æp#Ölc]å{]\x000e¡íù
\x0008¦èØò¡«|y7ùr]Ì°MZîÕÖöEB®îF\x00042Ù=M­\x0002SU^\x0001ÄÛÕµÁ$Øí½JÅÛ=9/\ý~õ?ÜÇ«·ËÝ.ñ¼KpÈnÚÙÌ"Ú\x0019°wÛ\x0004
À%ÁSFn2±0·+Éç«7\x001dÉv\x0018ª²\x0004Ðj/o[ã1óÚðñF1hn4hXsÁÙ0î.'Çª*ÑMUB\x0007
[[hù\x0001\x0016i\x000cí¦hÝMÑZ\x000c\x001eú¬´ÿ¶7k\x0014\x000cu¦\x001bVæÔr\x000bõÕ`ú"#\x0005ÃCBé¦\x001eÞM=¼ìZ]\x0007´\x0012`qBôÞ#èº5Þm\x0016¨Ó\x0014u	)Ü*§1<C·±ªWÅ©Q-þjì¥£<\x001euº©¥tSK)d\x0012Uq+ðäT\x000f7µnj)Å\x0013?@&#V_Í ³¬½9úËa\x0011ýýæá\x0017Ó¿[³dÜq·/W¯¨pT¾çºij~]v´\x000bJE\x000eD©P£.è1ôÛ"³5OIâoÞÛ\x001bðùÞÖ\x0019*W¹Vþ¼6Q¢@f:&ümé\x001c³A70êjñ¢ïëäs¹E9³?ÜVp\x0017ç\x000e\x000eqËïúÙ51.·aû\x000cÃVËûza;vuUú)
Û´Ù­ÍÌ]À¯K[E\x001b`\x0007NôÆÐ¹m&có!3 Ï0Û\x000e§$eÖÛ\x0014hJ|«wØ8¿êÍ°õ_\x0000ö	\x001ceêÙ\x0019­#Ó£)Éx³ë¯
¸5Zí¸¬£6xÒ ;µ¥\x000cÆÿêY´Ð¿ùÝÃóñI%¢Ã¿\\x0012{º®ò>í_SbïÆ×~ñ)¦¶ùÖÖ§\x001aFÔl#÷cá)¨ëöö<µ·¯gès»|­eÛ\x001e¸¥{xÔQ­§0\x0013±(óf±z¬¥«®ß?½{x~¡ÕãÑpñhLUÃ,ö(gþÛ×\x0013çI9õÕ\x00055
6sÍJ.ÆJ²ú\x0012,|pìÛ+O³Íàc±2\x0015;\x0017{ómøGOÜÀ\x0011ùÎÜ»æÛ2\x0012±ÂOï\x001e?¾ùýãóE"ý_Õ Ë\x001f'] Ï_aÚºä^-\x000fÚÂhnñö·] Ä)9G=³LXÞ^+ÉnékJç\x0004ÕÎuýèXc0pãÌ¦±\x0013¸Y\x0008²ºÚtB&\x0012mÃ\x0001~uç6z\x0008+²¿LN\x0005¹ðªWI\x0018ÊÂÆrX¼wè\x0002Ó\x0001\x0012nòr3Hq\x001bëcñ\x0014Þ¡Á¸×å«¬'Ð0¢BÝ\x0014\x0016¡\x0013»\x0010ª%0\x0014\x0014äØ¯î-\x0005©Ü¯YÂnÜ{·:|\x0007dð\x000fò#9è\x001bF2~)JÑZ?W7h°gU¥ö
¡uaY£è\x0012e@ÊÀ­	z	z\x0002]¥
zÈ\x0019Ñ;j¤(®¥\x001b^fz\ÇK\x001d[ Utæºr(éÓ&+q·ôð­ÑÝu%ùÁ2¤è\x0003ÊºÝ¯ön\x0004X Úpv!KôÇó\x0011Ù~Ù¥Ñ ¸ èe&èÉùêóu0ùÑù,©è\x000b$Gè¹fÑefÑ	tºdÀôä\x000ez'¦jÉ¥uWÛ\x000e{}ÁõðÙËDï6x¼6xÊíâ
û!Jþç1%ªÃÆ¼û`ûÔ;âÚá1uv@7òÀüBB§£\x000eW\x001f¨?Eþ/èX\x0019zç¹Ý}Át}ÁÆZ~ø)dÜ,ìUU®HïîtÝ-%\x0012 »ÎG.Tä\x0010èñX\ó2ódW¹ë#è\x000eÇÍ\dè¶ÙØßíðtíð\*ÞêCÙÔ
¯ùñ&ÀL7}\x000cÓNGyÅ¨á\x001cz¾/ì©n\x0002-£Î0!­Q\x0011EKã<!\x0018ì¢\x0012ê&O\x0019×ðJ\x000cÅj¬È£Î~v\x0008g\x001a\x001cùðÍ\x001e$¼zøôíÓK=E©»Á´½xdí*è§]ÔåÕ8XE¿õ?zê´·¨+\x0019
äÔ¥zSæ¾íêúªmåD\x0006	)òIÅº´$VG¬=\x0008N`\x0014òP\x0013ÚºFÆTè8ï¥-YX'2èGéÓ
h+=Þ}JÜªÚy"g\x00183êkÈ}d¨Ö©R«ÖÒWd©\x0013ùÊKëB@wðÌâEÌr#rj¬ØR'2­e¸6úG$á²ÄªÕ-ÝQOdP[S/ð\x0008§Ù Jö]Z­\x001dÈ(¶&÷q\x0001ÊJæ\x0015ÇEÉÒÊÒ\x0019õÄõ4âvñFUÓ$R+¼æ|\¶¦Ð¸O<v\x000ehç
SR3væUÉ\x0013\x001avÊ.ðpZéÜ´S\x001a§
´¥hÕ tB':7\x001a\x001bï5\x0015JàQoÎÜÓ{ì\x0006®òð	}2'RaòoIuù\x001c;a¯h.û¸³D\x000eqªËÝ½z3À,\x001f\x0008©¥!ñÅRÜh·fë©zx@\x0007\x000f\x0004éSÝ+|pÐM¬{%¯^c'2¤!\x001dj1Gµ'MÏóÃÐ%j'r 1wXw2h®Óï¼\x0013\x001a%þ2è¤Ìe8æ¨\x001cÕãã\x0016\x001e×=.é(&$\x0019Y
õ\x0015^µðÐ(\x000e\x0012\x0004s,/ë²¯«ä{s6èùß\x001fÞ?¼{©Ì{"WÆºÀ\x0007­÷Ã×yosæôCsoÔY\x0012Kq¶}Éß\x0001c/DCI8e¥\x001a{k®\x000e·ä×Ìðfue©´§SA\x001d4pp7}ÁÏK'øié¼ÿöù//´r7J±è \x0019
±\x001fb\x001cÜîWÓ\x0000\x0019EÿpéÈ|¥\x0013Õ\x0014
8\x000bÅx\x000e:*<hOÊré\x001cÀÐ9¨Â@,Ð§ÑÓàÉmk=È\x0003\x0019ô CÀEYsã®"z\x001e*}7­ä\x000b
~\x001bâ9âÀ²³ÍE<ªÍS¢æ@\x00065È\x0010¯,¯,lG³7"Ê¹.Õ \x000fd6v\x0004]ÍÞØ
:öHì[¼2¥\x000ed°¨	èD\x0017Tº=ó\x00172SþçÀ\x0016ÊPIEYÓ²p+ÓâÐ¦2¼\x0007r'ä\x000c[2\x0018Yæ
ßd\x0004+3)pGöØÙéûÉÒ¦©\x0008$\x0012×äõ¿î¢?aûÅ\x0006½îa\x0010\x001b©W5²}fßmï6 \x0004à£WõZÎðfçàyiøÑ\x0006;×C\x000eèHÐ¸·5gÕ>\x0007\x001dÚº r@£	ª\x0007þvÁ:\x001e´\x0005\x000f[ï¿_\x0008Q³MBTQÿ\x001c\x001eÞ\x0018À·HÑ²®¿ùâIÓÅ³\x0019óýòé?ýýùáÇ§\x000f/ÄL÷òJ¢\x0005\x0010AØ{ì6\x0008®lÄ¯«ôk7Aï Õ\x0007\x0015#}ìFzfP.±iL¿¸Ò|\x0007ypéu{÷ÕÚ\x0002\x001dºqI?îîC?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-18.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-18.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Üë\x000cÍ\x0002²»\x001cÖJ%¡#.m¦Âà>\x0007iá}%z	éð³áæ\x000b1Wr[,\x0019ÓÝ\x0014o£\x0000Ö»dõ#ÊÐ¦°Ø'R	 á]bâÙ`&få¿³ÿOalÍ\x0011ÛÝEsD2l(àR©}ÿ/ö¬¥bM¨¯2Qic¤\x0014ÖÂ\x001fS\Ë&Ås;|B!Û\x001c~þ/ö¬'E(a\x001cÒDìnX\x0019óh#ï!{í­\x001e¹!\x001diÏ\x000f`Ïóæ8\x001aÌyã\x0003V
åÿqÌ ãô\x0007âjº(¬8oþóÃÓûÇ÷+°¤^¸\x0016ONAÅ÷F\x0000\x0004øMþµcïä?'ö\x000esì­\x0010%¨ûõÆ\x0015çl4ãåÈ/ñ[a½+\x0019
Î
h ÒMrÍ GÊ²ñ\x001aæØûËÖ<3O±·fÄ\x0019A\x0007½Ir\x001c.Ýv·\x001cM\x000e6öþR\x001cÍÌ8>ÇÞrIAË1Ç8ØdÎ5gÎ\x0017âT0ØØûK<«wO±w\x000fðJÁ.ÙL²Å²î¿9øn\x001eé|³7|t91æY¥Áwo¥÷W\x001dRÆRsq\x00173¿ò\x0014\x00148Õé\x000bOçÈtÎçõoâX\x0005jCgFr\x001ebUî	®ê5ÃËa\x0019aü		1R³çÈÄÉq \x001d\x0017Úî%uÛ® $=46\x000eR\x000cnÍ¢\x0017,]ìl@äçÀ?Ð~$\x001e{QÕrä0\x001d~¶é«\x0008s¸£\x0006\x0006/¥kt¨éÍ´ÑæAVéòóL/Týò/ª~ß>¾ûËx®îÒæ0¨\x000c½Î\x0002vAºä·\x0002ð×ªégÁOA\x0001?ð¢ÕÆ<Ý\x0000$,U?\x000eÃÐåÈ	/­Ô\x0012÷OåñàÇ!¦\x000bM?~\x0003%ò\x0014%AeÖ=·"·ïBRÌ¢´b\x0002\x0018Ü¤CoÄ-fÐO>®£ûlÑOA\x001dà»JÑ\x0012è>ô°$;,CÿdWlºuÀ·|°\x001cLs½.ÃûlÑOÁ\x0005\x0004Ð¨
)ë\x001a\x0000M]C¨\x000fÃ¨\x0014	\x0001\x0015*\x000f7®}\x0016òåa@@5O¤\x0001rGjRyÀ|Eë'\x0008ò¤Ã£\x0010Aú~Ñ|¿Z/x}ÿæÞ%I®#É\x0016ÜJ\x0008Çý öÿ¼YUÌêd\x0016LÉII	Ä\x0003\x0008\x0000A\x0006"À@\x0004H`TÓ·ÚÁËô"¸ZI«]¿vÔÌ®\x0003\x000ftFx
\x0004¡nWÍLM?Gú\x0001\x0003\x0015Ra¿Ø¯:tðúeÍÞyúk/\x0019 P)\x000b4\x0000\x000fÙ\x0014[h¤\x0017eêáÙX¿\x0001\x0003Ew\x000eæãXß#sz~\x0006=w\x001böØD\x0000M2æG\x000e$Ó²ìJö+Mý½h\x0000
r$=º×´}¥1yëL\x0003¨\x0010$\x0000/Mè\x001cÖ\x0018{\x00175#¨\x0017cýnîïöEÌ¯_ïÞ\x001e\x0011Ë¢¼\x0008±t¾ïM F%q`xx,¯.c?ã9\x001b*²\x0017£/ÈÖ\x0004yæ}W»-Îáä6
L\x0015É#ü>%+QLd]$;k./åä2
U{ò\x0000¥Í`j­#aõÆ{6°Up\x0011×\x001c;FY-ðÃÆÖ\x0007<\x0019'Ó»^\x001b^fî¢sªúqUÎèÝ'\x001e5 gTK8vTqçUãà@«ÐÕ)Ýââu]A7\x0018=ÒúR1W°\x0008m»\x000e=ïòÔ95-é¨ÉHB%ð\x0004ìuÌ¡òlÄ­Iµ=g\x0005\x000fÝà½kBÏY"cåB=i=mquý^4=Ä\x001d?_7cÄn
ªí{L\x0008ÐG«TU¨Üõ\x0015'µêUÃ\x0014E\x001e\x0003\x001a@´²ÜµTtÚ\x001eTÛ³V\x0018î+nþö&ÙvsQj3Úã|[\x0004\x001bâ\x0017ÝòññI#àþìÝå¯@t<\x001aïn"?
@+\x0008ç)øz'QW¼æxF\x0007xWaòi«÷5w\x0003ðpé\x001a\x0010çÖ|À`)nmÈ \x0017+\x000f!JfÛàÃ|Ñ\x0000ÂRä\x0002®8¹®g¢n·ÜXe{Z£ûå\x0004ýå½»Ý=ëü»ÛûëcEã¡#­u\x0015a^¾Äò8\x0019Õ.\x001b·ã¥ÓfË\x001bæ´õ{|N\x001aã\x0008ë\x001eo­ÿà·ó\x001e÷Oö*Úÿ>Ñã&\x0017\x001có¾zóæÍýõîMÄ\x0019êö(\x001bíÄCï²Þ×S%\x0013gÖO¡°®Î/9i|ýcsN*+[±>6[ëßþðÙ0«>ñU#ÝííåoÿûöX¡î!Ò¥[¿æ\x001dy;6àS\x000c\x001f\x0001ûõyõ'ÒWW
I<A;¡Ö¾kÆtq\x001e*¸.õå\x001dó@GSeéÂ:æ©/×¥¾Ê±½1JQlÌ×»Ú!4\x0019§Ó¥¾\x001c×Þ±fÆ­\x0003èZé.¼qZM±_{É\x001eÖ0¢dÎ\x0003TîÆ89=~î\x0005·:\x0000Ý\x001cÑ1ï£LÊh\x0013º*Qi\x001c¥ér_.zyÜ¦+Ê|¦ovÈic¨Uü¢C\x0017DÍv3\x000c®«?Õ(r2ÔªË~2¿ÃbïZIÌ\x0003uG
®K~91ÙÃtÞ"+ª»¼	9\x001b\x0004w®K~J?L"×¯ Ì±Ò/ÄË\x0000 ­KC­è>\x0003°Eìîòj{Ñ[·\x0010ZJ8\x000e©íNÕ\x0012\x001ah­Ï\Ø\x0006\x0016]\x0007.E	g6}Ï°µ\x001b\x000cw®k\x0001¤U\x0007ôÃÉm\x001e¥ØJêz!ôÝº/\x0000ÿ
òìÑ¿4\x001d4\x000fþÂ¿ö3ÒS\x0006lVIeÛ!yâ´n\x0011\x000cnÜÁ`A2Ee¢\«,ù8?í²ÉÃ+ü®:»WWGD`íí*¼«Çë\x0018÷\x000fÐÃ¿ÂN\x001e|\x001e^a­0³î\x001cº¢|î@D~Þ}ûGØ#Ê7ØÈL 22Zbî)\x0000;\x000f°|\x0001>È<²\x001d\x0008$\x0017:	Oÿ\x0008ó¬\x000bà­	dxE&PõFÌkÂK2<ÂÍ·ç®a§ºA\x00056æ
\x0012þ\x0015¦P°ù²\x000c\w?ä.ÒwvN/»\x000cVÅå\x0006ýäwÇº\x0011¸$\x001d/ß ñé\x001fa~Ïap´rR-=_2×ãê	Jÿ\x0008ó£îÑ\x0011iQmm÷éy¾n\x0011
¯0Ù\x001f\x0001¶ñVº~ª¯§.t8[w\x0010^á\x0010Å$j\x0006\x0010¶1Ý·Ú°ÑûW¸°EÁõ^f\x000eÀ-<³6>üÜ¿Â!yd¼¢]íý÷î\x0015V~£\x000f?÷¯0{ì\x000fñÚHßAõàÚG7#\x0008\x001a^aî#\x0008â\x0015\x001e|ÓWxë&\x0002.ß0A£¢¼/*u<
®úi[W\x0011\x001eøÈÜ÷X\x0018wÒ\x0005ìÁiÚÌG\x001fí%'aL\x0001JúIyÕ%å­Þ ]DãàJ:lâ(1H¨ë4Õ\x0010ß/!¾£ÏGÈ
rDÛ¾W¾U&Ä÷h\x0008ÃÈ\x0016!Ç!\x000b¯ÕÉ¬¼)ùþ\x0019©Q\x000c§#%¬Q²»X´ôþLåÕ\x001e)J÷qô¨ÁøëÌRrÕ\x000f\x0013
Ìnm¡Ð-(ç¹h¨»Î1ÚÞÒ´Pn$ pA@ßëPB®m·Tm\x0001q\x001d\x0005)\x001aÓ4ÈàR×\x0013×Ò!\x001fÿÃîòúÓª·WÇËÃÛN½Læ[ÒÂÞ`Éë8éáÓlÙÁmL_\x000bffHiäÔ=\x0010ÁËà!&?íàÞK\x0006\x001a/¸ý,V nlXæ\x000eæ)¸ØôuàBª`Q(býN²ÍP9ð\x0011û!rî[ÁÉ\x0000-ÖLÉâ3Cå\x001cIäW]\x00151è®K'CIå\x0000Iå¿ìÉ±tÞy0\x001d!Cr+\x0019ÝWÛÒ=\=|ÁiN\x001eäsRV\x0017$o¬ÿà·O6Á\x0005±	Kçü\x00117n\x0004ÐÅÖ"Å\x0010"(n1´<<|ãüFJ¿¿\x0008ç¤«Òo6cý>}²\x0005ÅåZûÔvoÞ®iý;ú¨ËëcmDî
zÅU^|_òf`<nªº'	g='}ué\x0004ï\x0004Í\2IpÊ\x001c¥\x000f\x001clÙüU2D2\x0014ãÜ`rÜ3
6FcP^\x0005[±d\x0000B'%±cã+n,&.!aO\x000c3ûZ5K?ÄÇYKÉ*¸\x00051ó3rètM^U.ä\x0012\x000c\x0004F(Û,Ö;Ä¢÷ÓUr\x000b`8y\x0000)Û¸ô=4É41kæ^\x0005C.ýF\x0018G¬­p#C¶2Ìð¶£U_$gX²A®PV\x0010,«¤4%ôÛKÆT\x0011,Ôe½\x0010-»\x0018¼qJXEÃý£\x000b\x0002Å¨Ü\x0013'N\x000c\x0005\x0018Ð3Ë$¬áþ9¥¯Ð1/\x0007ú7rÑª2ënÝ@7Pvuf#\x0008\x000e\x0019/#GJëÒ/:d\x0012VÑÑ3èÓ`l\x001a®]]C"a\x000cw0²k«>¤'á93Rt¦óWÑx£3d?¡£\x0011S2TdÞ\x0019P\x0000Þ²ºyÃ{jÚû;zAô¹$ÇC,óAk¥'Q@çuÖ¹¤nOÃ­\x0018O½-[\x0011ÖS¿µþß>Û4ÛwgOon_\x001c+LQ´]p\x0003È>JàæÆ6FsÎÿáGÝníÂhm*»ÐP\x001bë?ðå³\x0018Ç":êÝ\x0012ä¼;£¸:â\x0018Âd:ã\x001dÔ­Ç3¿
DÄÑÖÙ2§\x001aã\x001cÛCm\x0016.XÖÝ´@/\x0013ÃÆHÒ½ènÖ=d|\x0019\x001b"\x0008=r7j\«e½ºy¾»bmõk(þ§¿ºþ|xöþGáì_v÷w\x000bÈ\þá ÔLP\x0010ÂáàMHSÎã8÷\x0010Ëø1Ý[\x0014¢ÖÍ«ûßs\x0002¾T-XL¥7âêòúìßî/®oî/'!èi%\x0018!¹6÷Z	YU\x0008PUË\x000b£ÁãkÆdxKÿùúìûëÝí£h$(N\x001fF|6gDòìL\x000b¸hÄqOØñ5Ò>µ\x00197÷×Ï/ßîU´å\x0007ñÓÿ}ùöÿÀ_å­eç°yK<ÙÑãÈaÅOÃ£Ò\x0002ÿÀÛ{úwüdQý<\ÃçÄn¹ûU~ù³\x000f¯//å\x0013ñ§Û\x0017tø¯c\x0011xR\x0011:\x000bÆk³\x0007óQãJvÈ¼©\x001e7û{7úÓëÈU×\x0001pÝyI{E=ãâùêðò\x000f~y©Ømá\x0016C¼Ë\x0015ÿ"\x001do\x0010³DÔ.h¿-Ý¯ÒÉ07\x0004\x0004­Ý$\x000cMù0j¹v[j>\x0014,oIw^µµÛØ\x0018\x001diíÞ"³Ì\x001bäµ\x0017Þ^zl·¥kÐ.5µýÚÃV|NE"Ó\x0006­Ýëª¬Eª\x001eú\x001bèG\x0002ð¥Ò'\x0004\x0000Bn¨Àa\x0007ô\x0005~`\x0008%áÏý\x0017¦wÀ>\x0015=Öå
\x0011k ¦LÄÝQ2ª­£!1ÙGTûÃoU³:ÓÕ$÷â]X«´þ\x0008\x0003Û\x000bVce¾=ãy\x0013´-DÊÆ\x000c\x0017 I÷ \x001dúvY;¢c¤§¤fu\x001e¶¥&')\x001b°ü\x0019éåHº\x000fbíªNä¡elIç?Z¥3b'6é\x0004×.Ü
îëcåðì×·ç/^ßÂáüïÿü¯½|wq5¶L|×ÃÓ£ñÛ¨ÞûÜêÔ¬\x001b9a©À\x0004\x001fòpª2*}H÷ºÞ:WE=cÏ}µÎÞk¤õ\x00071¾Ý#½¼aIÍÞØ«\x0003â]í f2ÿ @ h"ù\x0014¿\x000f[üãÛ÷ñ'\x0011\x0000=½½¼\x0019¦ü}Ùþ2IøFß|ý¬öo½^:ò\x0008¢ÝÞBÂßï®U±SÕÑ3\x0006\x0000ÄÕøëèÛ \x0006úÏLD°\x001d;«æ2va{±*oKÏ«t\x0015-\x0018\x0007Íå¯£6{7\x0014Qº:\x0003µ{t­@:Mú\x000fíàt\x000cÕi×(\x0000\x0019NÎÏ\x001f_¾w¯äËõ=éòÝÅîþ×#\x001c\x0015ÃBb°ûAH)ÀLDb
OÕ	Ô{UU|Só\x000cU2`\x001e\x0002c¹\x0014zþZLæåüIe½ÌýËØ¤g·\x001aàêÀ»Ezû\x000bÇ3Éq´Ì±9ÔýÂ³ë_^xqÓÛÿãD¼\°,l¿³zuLt²x»øaÏáa77&Né\x000cIîmU\x0012?îÙ®Ï/7¯ \x001eZ¿1Ø¸HÏ¯VÂ6;SÈDÌ°¹ \x001dÜ\x001enÕMM:Ob@ï68á÷[§
®ÝäÞí\x0001éÍïÏ\ßikgâ\x000f®\x0011ÔÅ·(¬Ü{= ¼y=Ìýá`édØ\x000c,\ÀIu0JïõôôÕ'ÍÁ#W¤÷F\x0019¤ç¦v\x001d[Ï;«]Ú­ªUaZP½=X¥ÛµKÒ­ks]è?ÍéÅ\x001fÌâA)@h«6Ï£Up\x001e}jE*Z:GWÖ\x000b{Z¯_jó<ZÕÎ#ç?\x001d¨\x0011}¸t/¨\x0011H:"}ó<Z\x0005ç+Hpd¸Þ§Ýª$LCéHï\x000e\x001c÷g;P\x0003[©O´ÐôÓ\x0016p;É8?$ÿüw]¨Þ\x0014ß½¿µ¯¯íÓûÛW7ÇJÃ¿"?Ôqqïk¦\x001b´4\x0019nÃ³'\x0011)¦þVMq\x001a=­ÏaL-\x0019`¸\x001f\x000fz{¦\x0017ºYPÓ®?«h½Îõ\x000eÎ\x0006f éÆ#¨ÒG¤\x00052<Ð·¦þ{{\x0006²S[6ãôAëÞ`C\x0017­Ü!\x0017\x001dIw¹6tõö\x000c¤¯N&[°\x0006qæòåcVQH/¸ìþ`:ÿòêÎËù×Ý£9AG§e ¼¶ÕGÍ\x0004\x0001©è¼µê4ÒCª*Ã§¢õóü\x0004àYá°ÁôíJdÁèÉa\x001f\x000eÙ¶pÓÇ\x0000	8\x0000${\x001cæÃZ­\x000c¾O@´m¢ùu\x0002½ÇóXHzD²4^wEÇûþ¶t\x0007\x000bÏ
\x0016JÒmF®-^»'ÂWïÉëÞ"£ÒWÌÇ\x0006¦!ó\x000fD\x0004#'sf¾fv¼î\x0014ñ\x0003;øÔX³é\x0007¸/Á/@\\x000fýÀ$5o~\x0013åÍje§c\x0019}A\x000cLö£0/\x001bÑ[zS\x000e~|¯ã_UÅæm=þdÞkôU\x0003¶\x0000ùñô¢uékg+Ä¥¿\x0000 Ü6«ob#\x000bäÜ¯+¹fõ¥ËÃ\x0003]ªôþ\x0002ôö\\x0005\x0007\x0010«d\x000by\x0018Zf£EôFþT|­}ÿbôöbÑqÃi
SÙáÚµLì;ÖÝè_ý	Ð\x001bÙ1hc\x0004~á±$
"1\x0005\x0002-1Èh¼ýò£Ê±'6ý£Ï%=Hù0Ð½\x0004\x0010\x0017¯àIgb\x0004l<£\x000f\x000f\x000eS\x001eÉ©Â¸Ùx½øñÂèÔ¾\x000cÉ¢\x000bÈ­?ï \x001aS\x001fÜ®\x0001²)Dû&z\x0019­¶M¦NB6¢6
×¹Fp¥\x001dAvãåâñu\x0011£MÏsIå²É=\x001a@Bt\x0006Ñ¹5klî-Gû\x0012Ä&\x000cgØ\x0007H!
×m'I\x001eð\x0019O
ºeuKØÔ
ÿÑj\x0019\x0015@\x0016é§¼Ed¯ç\x0001àB:E\x0003{S1:bnmÈ¼
Q¸¬\x0018+÷ÓÚî×ç.ô¨~¿ôÍÛÉÔrö¦ñ>°t@_\x001f£QÅe\x0014Íæ®ò\x001fÓØÖÎÛ`¼8"Ä§[T§\x001dÇ!ÆiÒ\x001d\Ñ$¤Kâj¾GA\x0008O\x0015<\x001b7/)ÿQ«5$8ÜÃ\x0013QØl\x0019ydJvBÇ>)\x0004Â0.ÊáØ·XVî¤áªczâöi`\x0003\:½n\x0006Q£GL')=WéCÖ¤§&=Ô{¿*FÌ'é.;©:ezû*EÐ¢\x001cw1	cÊ®3Å ëÍ-µºÙ]ãw+1\x0004\x001a§ªyÚ\x0015¿I¦R\x001cX½¹§vmúe\x000b¦!a\x0010Ô2É ;tÒ\x000bcõ¦b¬\x0006\x001bCþuh÷ÔPÀõÈ\x000f\x0012Jç»,ÝlÚ\x0018k\x0014x\x0016Ð\x0003å!M(ajòÄµçÑÚ(\x001e\x000eØT®Ô§4ey\x001csy(Ôß\x0012ÎÔò4Ð×ÎjOréÌ\x0002(Õ\x001ejUyóÈ8\x0007Gq\x0014`|uÄµ'\x0007D¤â\x00123\x000c£Ýé»Û\x001eszµ{~´Æ[+aSk;\x0017ë'Ð2VòÜG¯:ògýÏëÞn\x0015ï'à5ÏS08ÞÍø¬ëtxß\x001fL\x0010¾\x001eÌÈLMí`ºdÑ\x000b³ÁØª\x0012Ñ°>$Æ¯!1-i!S[{
ÂÜÐ'	÷ËºïÈ\x000cÏ^½È¯¯µ<;ßÜÞ¼¹¼9\x0016\x0018b-%âB:Â~\x001fÖ\x001bãñ\x001b8¦\x001f\x0018`3¿»cº©7US%1±V0hý®1ÐúÉ(+L
e1¿½\x0015
½ÙlÒjÒÉ½iÇ\\x0013|¬H¸\x001bÌÌ_ExïpÈEÚ\x001c?^và<úì\x000e÷¤7«t«Ýï\ºsý¥];\x0017p\x000bm+Ç!¥\x0013I\x000f\x0006­¦gáäï®\x0003âôïGCÚ\x001a-Ú×8ýí÷X]úGWïÉ=ñÁsè?øÁ)®\x001aâc\x0013ÛÆ:2ð«cy\x0016\x0012ªÞÐ\x0013%.»÷e¤¹\x0019üV\x0010Þ6"Q@°ØÄÆ\x0019Î¤QYªÕÕ,âà¶ðØóÓ\x0004KçÙp\x00167­³S.«rW\x0007·\x0015¤§&|;¶¥-\x0018\x0015£\x0011ÌuULog@z³3ý:äWËeT»\x0013&ï:lêíL±N¬t±t-stkrl¬òî¥k¨òt\x0003¯ MÙb?\x001f\x0017ýk$>.Áñ\x0000\x0008^Å`ÀÒØ\x0012ÜìÅ\x001b=(\x000fMMù³\x0007ä?{	F>7ÏÄY¢ÜH\x000f\\x0014Ð?\x0006Úíðìåë7ïoèãÛÝýÛq$é\x0017Âzh»ETnVàÕ-cc×=åÁ\x001fmo6ÑAëÏfUQñsZè0_þÁ/\x001ftï¿ö]âÿ;\x0006]\x001e\x000b\x0012lÅ\x001bBß[\x000c\x001cd	\x0004\x001eÜA¦3?Ëú§>QYõT`U§x\µÌUQ4D¿\x0014#Ê
OµN}ü\x0003Â\x001b\x0014!1È9³\x0012x£Ä¤âBbSG¼õ\x0007¤7Ð_aliKg^(0ø\x000c£r×JÅNçþ`6á¹aþx`Jl!sCY\x0001B\x0010ÓV¹g­$\x0014soÔ@xÃ®ñJr`ó6³\zAþ©ZÛÆÕâ ¯ÅsådI\x0010ÖKAM¥ó\x001f5t	\x0010ß²ôØé%Ùnéc¥î<Þ½|ÿUÇ1{}óáH1K\x0006óÔ¢u{ÝÓÃe.2^%D9$ôNTÕSqì\x001b",+±~ÏeF|\x0010½\x0015\x0005\x0011¯m)-!Õ
ÒW/jK;\x00075[¤÷G\x0013¤7¼\x0019§é[1G3\x000e\x0001î¯@!n\x0011ÞL\x0010ÞàfÉc¶\x0007+\x000bÜv2ÇÅ´RÅCëÍA\x0013¾¦ÑIë\x0006\x001a-ÉJ)é#1\x0010jÑ#3OxöþæÝù÷òúóÍcâ>ç «ää¿¯ï\x0014\x0017`±tÙT\x0008Ú\x0006&9Ï\x001fªßª'Þ\x0000\x0005ýOZAìàrJ\x00128eLX¡\x0010î
r®¡íl®-Òû7\x0016¤Ã\x001bk\x0012¤\x0001]iþ\x0017½[Á\x0004\x001c9Ñþ¸\x000fÙ@º\x0013ko\x001e\x0008­Ýb7u.3Q¹ÆlCÖ\x001b¤ã\x0013.¥+Á!Q:Ã\x0004¶¤Î\x00066CÒ\x001b\x0007\x0010î\x001bOn]ºÒB¸\x000bÝÒKÜ£{k\x0003ÒÛCÈ¤¾©§I;qd¢Kw¹2Gn\x001fH£~¿ô>}\x0003Ò¡!çì6é\x000c-Q¢YÎJlà\x0006è"}û@\x001aûû¤\x000fx\x001b{u}ý£4gÙ½;ÓmD\x0019z÷íÌ\x0007sµ"-¼·\x000f\x000cc÷2Áé®Z*\x0011yeþ-Ã\x0004¬øvqî½Y8<\x00070L\x0013î@¸mli\x0017±ÍÒ$Y/ñÌÍ=³ÉØôAîíw7w3*ô/}«ÄÓ\x0019½'{a¢¬ÔÈóéx²ù|`\x0017mDÓ\x0003¬¾*ª¸÷`x¸\x0013¸½&!u½NYFµA§ÒCÂ\x0005¤ç¯>¡-L»k7
ÖNSkÒu*ÑI;,¡±±¼&C\x0016HµkìÄp1fl@eé"ð!ÃS\x001cÀ¡M«	6-ÆÑðà´(¡æ, swk®Ò{\x000cÒµØT
Jq³\x0017.UâÕ~±÷Û°oiKs9O\x0011îMJ¢á?eSíöÚ-¬='\x0000nu$\x001d0×¡^YKªÍwvóÈXÛÌÿ1'ÃØ8õ<¾º¿ýªï»:"*ºkî$\x0015¬ hn\x000fÂ~E;'ðä~w«¢JÇÄZêQÌoÒ¢*\x001d­\x0012!¹îplÖÚ1´Ù4á-ÿÊ\x0005Ôz\x001f$²\x000et£T¬4Fÿòü§;ýNî/iëãñöL°K^\x0015NÄú
\x0011gá&\x000e¿\x000bMþ	lðF«*/úÚXÏðê'\x0010S$]û¦Û_¯l\x0001äÔGü ¼ÕM"4\x0007å$ÙzGLúaÜT=lðýîùÇ«7m\x0017âß2Iåþìr¹á6PÔ.zOtÔ{k¶+µW2Î\x000fãS\x001e«½µÛª*rÍ<H.8X½Æ]· ?;±w6AvsöæÄf\x0011 ì´ëèÓ°Áá×«\x000f?þ$Sv·\x0017Ï__¼½9\x0016·\x0001yÁâ éÒ^µÓ	ö\x0013\x001eñÀ»»Yæè­hÕÄÖo­ÿà·{ð¹¿\x0004Ûß\^ß\\x001f\x000bDc\x0001m9y%{ PvFµ±%ô\x0003¶öÐ>þý\x001a²¦UMÏÖo\x00004mÊttqÁ¢¨=Ó§'¶¡aÞ+å\x000b~\x001bG®sk\x000f3LYlÅO g*ÿÄ¤M@}¼xq÷³|)ÞÞ_Ü\x001e	í\x0015TÖ]l¯}Ø{\x0012Î\x0005èØ¥ÐÂ<9Z\x0019\x001cÑª§âæ¶ô2[:ðÿ£¸dAÅ$SU:V\x0004í=t\x0010ÞÒË6çâÖ®A]ØIPârPW&à=Ýî\x000f7×üÁM+Â{ë\x0003Â[¹©t×\x0007\x0010®Dûb¾
)½ö\x001b\x000fùÇU:`\x0014zioA@(iíNpG\x0005Sé©­éÝ&Ý´\x0004ÙJFaABí1\x000bî
R{\x0019D\x000bìqv¸xèfæ\x0012\x0007ä y& (ÑÛ+Ãi¦¾\x001aü\x001fo?¤äµý×ûßþ¿cÝZú.Ñ¹\x001aÒ:¿Ý[ûduÿ\x0019¾Q\x0018\x0003\x001eÿm4\x0003H¶ª©Nðn§Ë?øå£þþñæý\x001b©ÿº¼¸ûx$õÓz\x0005\x000e/l\x0003ï\x0018(r[ÅÝ§ð0¡^µTüÀ\x001e\x0005l°JòOÓ§Ç,\Ïhk\x000e~(£7é¹aÆØÔRô/naô\x0011J\x000fÑà÷»·wéB8>»'U\x001cÉñä\x0006),Yç¼jÅÈÎ30¬jWàâ¿»z <¬Z*ÍEÐwi-4|³¹Ãè¾½c\x000cÊ\x0015·¦ÃPzjÒ\x001bzeÃ¾DãðèpC®¹vâñÜ?ûáujæ{y¼ì\x0000÷\x001d,\x000fqD½R@ý¦\x0003ùæê4ìç¡©ºê24\x001bë?øíÃ.¼{ó"«\x001bqÅ¾¡¯+\x0004ã»û³?_õd­_\x001ee(%kå>­!|b6Û^û2IéaIÎ¶öBõaFÕXÉo·Î¬õ\x001füö\x0011ºüÞ¼ù¹+¾|ýzww¬=\x0008ç\x0013HO­Åµ`\x00036ûG]OoñÌ\x001e¯*îD\x0003\x0019\x0007ò¤ë\x0019"aéíË#ÅO\x001fðMºoï\x0019ý}±\x001f b\x000cz\x001etv'Lpáýå/\x0017\x0017rÿ¾£0þöùn£$\x001e"´Ox3.P°x³\x000c£?[60EV]-nìL\x001bë?øícÍáÝÅEènÙÓû\x0017ÇzÁ9\x0018´Ú\x000fgb\x0006(¤\x0014pA¡>\x001d°\x0003?VÑS	\x001fk¾þC>lÀî§ç?½{!7à¯7\x001fwGÓ¿ëJ\x0002\x0011X\x0011Ì\x001c\x0003­\x0008¹v0À\x0006ø>ÕQõTìPKul¬ÿà·;póêâ×ûî
\¼¸?\x001an=ÇØ½2ëä\x0002\x001eÎ\x0013°íO­Ö¨>aSÕT^úÖù\x001eÈè\x0000a0\x0017ÝÀëâoï^Âf`\x0006n;\x0010n@¸\x0005\x0003ç¸D)ûÄ\x0005ZùÊ	áèëó\x0017Ï;7b÷æX»]ó\x0006bÜÏ\x001b åG\x0018ÃY8èN\x0000d;ðÿU5
WmÌ:­a\x000bË%·B~»wÅ\x0018øÿ@zCì1»`\x0013®¸=\x0007\x0001\x001cFRMrð@Avó@K\x001fy£ÂÉ6Áx;lßR¦¶y÷G~\x0015m\x0001f}F\x0018#wæXYH2Q*Å¦¿>
±
w\-Û¬@'&\x0004|Òyh¼
'O{Ä__¾øOú®\x000cå9R¢^1-¼5ëÎ8lßr¬ç\x0018\x0006$m 9ªj*\x000fJ#oßXÿÁo/nó\x0000ZoÒÃï>Ä¨\x001f~q\x001f>öÏÕíÝëãõúøÅì!:Qµèx5·A\x000flÔæ½ð\x0003OmÕTÁ52\x0002Æ\x0005¶
7%\x0019_.L\x001aý'¥!X\x000f<µ ¼Õ×h\x0003\x0001í
cÔ°¾Æä(Bz¥Ì}
\x00007\x0006ì< ÞÊ']b¹Û²dGDãùOw/?ä.èº¸½½<Zil¢â\x0004Y,<8©Èlè¡¼ªª¤ú¿³±þß>lÂëðêúæ
6á¿ÿó¿þ\x0016øêH.ÁÙ¼<TooÉÛ¤H=6È0Oxà*É¦¿Ùßª¥ò®7þ|~m
,ßuôùYâbRÌ\x0015ô\x0019ûá\x0008(½
GÈgã´ÂâÀµ\x001f'\x0007\x0016ðë×ç?ýØqÜ}ós!`<vÒµÎ­8\x0011r¡}½°¸ÇHå,ôUUÏ$\x000bý|ù\x0007¿|ì}ùKzó§vgßß_^_Ü\x001eÞ'
ÿe5lOÀð"\x0003>¢Õì8DbC\x000f\x0004³UQ\x0005¨ÓÌÜÆú\x000f}ú\x0018x½\x00063KO/èø¿¿?\x0016JÇ\x0019É2l[ÔÅ=R¸Y1Ói\x001cÿ!t)**$~ÍØXþ\x000f\x001f\x000fÿÇ_¨h*ë÷T$§¼ÓÚ­ãY\x0002OLn­ì6òÞ<ä\x0003C\x0001ù¤iaÀT%±ò]ëó\x0014(ò\x001d9·È³É¢ý×¾ðl\x000e	[\x0010ÞÂi\x001eàL§dÄÛQVðÊ²5t$7á\x00007\x001621Æ!E`NWÙÑ~1nr\x0008Z`5è®É\x0007\x0004A cò»UiY\x0003y\x0014\x0008oï9\x0014p(<áLw\x0012.&³ð\x0012M\x000fÌBMxNUk\x0012Þé;ëà¥ZJ£íà	ð\x0006 ø
8\x001fS\x0019\x0001\x001b$Ür:¿òI\x0019è>@¸\x0001µ\x0004èª3\x000c©\x0013S^(`U[è>\x0006\x0010 \x0008vCï!«CW4b\x001ffi·»°Ã\x000f
ÂMvvÀ¤Zlh,£X\x001cö"ÀuÜPÌÌ©CGÿ*\x001bú¼\x0006\[Ñ	R&f
¯S§\x0013­¾ÚU¶¾Z\x001eSØüzÃ0O-ë;á¥WiÈt
Ò5t\x000f0nù\x0015+ÏÝÊ«ìÍ{¯¡(0UEm;NÃLÿJ^ÏìÒCGp\x000e\x001dÁ\x0014¾\x0000Ü(Iz0^*­ÝÖº\x0005­3\x0001|»ýì£\x001ee*Í)Ú"}{í\x0016l9cxà)r\x0019§9rV^L\x0014&é2Q\x000f(K§QÁ,Ùrÿ\x0013^Ñ\x0005\x0001\x0001ßÿ±úöÜß½yßÍçØG
Çê1LÞ	g-:kö¾R
>µ ÒiÄâCPõÔ	µ\x001füæ±\x0002m³{ÝQJþëýå±Ð\x0005¾\x0003Ú¦ì÷7\x001dé"5>bï¢.Á	Äá\x0003ahÕR©=·îZC47Ï»¤\x000b \x000c¾]6êå:inÄBtÀBêÊ\¿!õ\x0013]È²Çº
«_üc×lU\x0001UGl·²N\x000e¢´>¯¬^\x0010kvþÔÃ¶[}6 ªêª\x0007TÍ×ðÛ]øøëÏ/¯Â\x0000ò8*ÆCkÙé\x001b}^¡üJh/¯·¦ò\x0017À&\x000c!CUUñØXÿÁo\x001f#q\x0017v\x0019!\x0006»³?ß^¾?ÖD>\x0006ýãApÆ¬ú×ä\Ö\x0019¸ûÐ\x0013ùÜçMä«ZzÖOä®ÿà·O'òt¦,¤Y
J\x0018'Ö('\x001b[Z\x0004\x0008y\x0011fë D\x0016Úî{ë\x0016" Á\x0017\x0007á82OÌ\x0002å~XK+;µ\x0014¾´K\x0011ãÄ<'æf\x0007ò9åÒµÓy«t11ÏgpÜ4v\x0012*«8R1%p\x001bGæt80Ìí\x0004#\x001c¹µ_Ìb¾\x0003SKÙéÈ<\x000e\x0007&$ ¡)^DÀ\x000ev&Eé^y7\x001d\x0007Òad\x001eóÔ\x0001Ö\x0019Ijfm7\x0007Ñ©v°­b¤¨z\x000e\x000f#.ßD\x0001è°º2\x0013#ùü]\x001f0Á¢]°r|5\x001d\x0003¡\x001eú½\x00110ò£¿yó¡{²þvq{{q´ù´¡kc¥(xÍ\x001cG:\x000e¢9ºµ'ñ^é¡«ê}r×\x0012Çóå\x001füò±|òêãÇ{(pswÁ\x001f°~ý¦kÑÅ8å6,¨Ô¥=\x001d\x0018¦^\x00165=ë¦âôë>øµ#¶à¹¾¾Kú7×´tn¿<\x001aC[bã"Öbì: \x001bç\x001a\x0005HäÙ¬ù$J'ý»XuUôßæzl¬þàÝ¯5¹ìÁow×/
ÀÒ÷Q6»8mÒZ\x001föä`\x001a+²\x001a\x000fÌ9äTú)Y¬£=À¹oK·uªUûê ^êù¬U.ä\x00122I\x0019\x001bd1,Ç,ÙyU.Ó}zwa\x000c\x0005\x0001o0ÍkyÈ:ÊiNWGgèGÝKnØ:´ê`Í1H JÞ´æâ õå*9³\³GòJlejZÅÙÜ­Ur«\x00050¤£§\x0011LMk
ù÷Ð\x0011½\x000b:b$ÁJ\x000c5ÏÑÉì«)ýÐC7ô^pK½z#j]NùRë&\x000f6u\x0000Q\x001bÝ\x0006\x0012'O®QýKQâ\x0010bTÝi®\x0003¶®	08y%3\x0007\x001d¸h2»dt
 [%ÃEaQèY&èmgv
òÖ5\x0001âH\x001e\x001b ´¥Lwä´,ãáÞº&@\x001aé­LÌó\x000e#×åe\x0003û§xÜ|i&\x000c£a\x001d¶ß]7ÛWÙÖ\x0005ú°\x0017Ägc©¢ Ç¥:\x000elK4Ü@ú~´þÚË\x0019½h]¶¿HÞº@Bé²\x0012Ì.VÎ_ËÜ¥¸XYª·DÃ-$Cá<Ï"\x0011ú\x0012E9Ð\x0003½å^4[:æ«b½@{Ñª;ûÌMñLv¶%ÚÀùÐ:bÓÝª}w¨É¢\x0004êèv¨]\x0010ã\x001dcÄ\x0001F["Ør\x000cD\x0001«é\x0008Ëñ\x0004_¬IlN\x000eQ\x001a\x000fWègãH\x001fÒì¿ \x000fù7`ðjiOÁÄ#¢\x0003û7.ªÜ_\x001d\x000b÷ïSz,½È¬(8í1=t/-=Ëîs¼(ÒUçE9®\x000e#\x0007ê\x000e¦éö Ô¹ö[áÈ\x001bý\x0004¥FbêvÉÜÌÚ\x000bnï[ÚéñÀ\x000bÊ\x0019Rwäg^Ô^p»I6'`yç¶|1®\x001e¼ {R|Üça/ÙdääQ¼jaÉ±;]6Ïü³½d ø\x0011\x0004Æe#¡\x0003^&\x0015éù0Sÿl/9
mx¸Ù±ò6*\x0015øáuØK×Á\x0018¬aï!<\x001ab\x0003.¸éáqØKÎ 9\x0001âÖ\x001c~
ù
\x0003\x001d\x001d´E08hÌøßzÊÅ\x000bïgêØÑAÛ\x001bÈj#N¨è\x0007måEIÚL=´½h¸\x0014"á\x0016R´*pBÁ\x001a×.¾ðÄ~¯ºäOÜêmA-JÒAû$\x0013îã3rà\x0007R÷\x0003_pTÆ'Bã\x0013±²ô\x001d+À¶¾\x0007-Ùæ#k ò)§\x0007NðÙÂªüéA/C*müëáQ\x0012\x0008\x0016Þ\x0010\x0005VÓA\x000f\x0011¶VÂ¥uJ¶=\x00059·q3Þ¿U2\x000eä
f-\x000f<îêàeIÏ\x0006=\x0004Ø\x000c\x0018\x00023k{O¥\x0007\x000c¹B^=>
º\x001a¼Öè\x00029+Yò96º(,ùãË ÈÝG\x0001*£ÀA¼\x000cÑ÷q>\x000cz\x0008ÜM\x0006î¨â&g2êÜ-¹P¯\x000f\x001eB÷d1\x000cæt\x0017\x0011vî°j¦ÁãÃ ØôÀ&ëºØÝv\x0001Iuí'ö[\x000f\x0001¶¯\x0010¬u\x0007M·èÐ1M{2÷¢á8ó\\x0012u²ÝcT®ÛÂi¸º\x0017\x000c.)ôÍH\x001bA¤Rì`¯\x0015µu80¦äl8\x001cÚÈìKRN*Új?üö¢\x0001ú¦½\x0008tyÐM´µòvW\x0002ùék¦g¯Ù\x001e\x0003? å\x000fð(Vø\x0001Qï!õÎv¸ó\x0010¬­Ú`-\x0018\x0007\x0014&lÝÄômF\x0005wñz¹5}AàìÈp~ë¤÷_g?-M?.\x00017¯	lÇ\x001e¸©Ô¾O'¥Uî\x001eÍµ\x001füîiZzÜ\x001eMî\x001em\x001bTu\x001d¥Un\x001aNí\x00057#C.\x0013\x001a]nñÇ\x0010ß*YÃ³©Äøcbb\x0011ÜÞLº~@\x000bÄÜð²{Ëu¨f«+tÌÔTÑà\x001b1ÇÌ\x0001ÂY%ª_´è*zKÏà3\x001bN
6[fä hDÍ»Æv$zÔÔì\x0016ýew{¤y_¤¿ üÈ´¦$xèhc@#\x0005¥ßxüÄ¸\x0003©w\x000f9ð\x0004>§\x001dc ðù]\x0019å6È4\x0004ø)<IÍó¡\x001b"á­|PËdòY$õÎ\x0016ã°\x001bC\x0012ã!e2Ü\x001bÀ7)Lå½ä\x0004Cc3\x000c\x0010\x0013ÈwM
&¡ÃKúé*àSEæ@®ØªìçW(õa§e6Q°(¶\x000e3m\x00077'yñÉÆÌ3ø©Ïàoëwb³N}ÎÚj\x001cOc¢×2ûë¬\x0018¦@zÍmi\x001a\x0012ËÖæ\x0006]6<Bá.\x0008ú,Gï´çSW.\x0018z\x0007¢£4®«v9_Ù·T
ye\x0006\x001fB\x0016Éë\x0017½Q7ÁÎ
KÞº,\x0006.\x000b\x0005õ±éè²Ì*\x0002Ô´«\x00032gyåý>
Gë÷rÌï7\x0013\x001c-:®èñ']K¤ð\x0016K÷ÙMx è¾À\x000b±b^~`óy{{,¬¦²²IFÅ´¦&\x0018»  \x001bÃ\x001e¢K!)W=>0}nûÈ2Ö\x001e½,¥ìûJÞ´ú¿­X¶ª $![ërWò0fZýßK¶ 9õÅG\x001e\x001ccæ»5Ï\x0013¦Ö¸ñMCWô2¬È:ôÕ7MN>9ÁöUÉR,2øç¾;U\x001b;Å\x0015ì%C!'ªáô%/m@¶Ý\x000eÖ©c\x0004júô\x0004÷* 6rÇFz.AÜ0ýKÌV\x0004êÒ6¸r\x0006¡NâBR\x00194\x0006¶¦ON0ïy\x0006Á©¢>Û£ZÖzî(/¢áß¸ä\x0007
Ä<ïaú¼G´\x001e¸Ì
\x0000GÊ²K×úÀ$omz\x0007"Öaí{ÉNB[tè4\x001dbgTLQ^äñlè`ÒÊØn\x0013k²fë\x0016âDJ:Ñ\x0010úÙ¥\x000eV-ËRªVÒ&é\x001aÓ§kbÈO\x001c¬Ú;< ¼1ÈU¨r\x0017ìE·{èJC¾ÆZÛu&AC«6óLé3Ay¸è,Ñ¹ÊnÑ~îªíE'XtF³d­@z%1Ý´h5\x0017ìEg±\x001avÑÉa½´QÚÒçðE4x\x0002mp¨,\x0003\x0019Ä¢¥àq|ë&\x0002EY\x0012­;åPËKÞADèP»©¹\x0017Ýnb²Øb¬ÁJvøz[§Kl¶°jQ\x001aáûâä&Ê·îº®{Ñí*&cñ|\x0018mJ]·­ZÉ\x0002Nï\x0017Z¯-Ñí*Ò!EÏÃnÎ¸v2¶Q>©[¼\x0017Ý®bæ~&Y\x001bÙLmºô¦ª]ýz¶Xo£ðcrbíãL\x000bi¶å+#ä©ïtà\x0007¬ü(Ê´B	VÈÚÈ¼5Ù³\x000cg\x001a<ïÿþÏÿúÓýùåõ«£\x0011~\x0007'*B6§°\x0007=sTQ¬!ÇÂ?0§ÚÆ¨Ï1?:×Ûó×í]Òe\x0000¯n,y\x0018sàí"\x0019É8"V«­\x0006S¸8¤à:d8S\x000f\x0018«ûàVÍSi(\x000b:ä\x0011°:uÊÐ®»³e
Ì\x0008(\$\x0003 [ÿ`ÍÊÊ±>	ÿØæj
Æè{Ü
\x0002Éä[HÉ1K^\x0019\x0004Æ\x000cÊ"\x00192(\x0001Ý6Í\x0001Ï(94»¶7ò½©OUÑÁ\x000ej9ËI8£\x0011¢CÜªÌ¬'ZVfQetª£\x001c\x001eCG\x001e`ãH\x0004¶PctYßû³?ßÞpÿî83ã¸©¬{	^\x0012¿Ü&O¤·ESß9(£úÈo'\x000c¸®\x001c+¢ÝÍveI[ñ[[\x0013 òØ¿XX3\x0004s·ÓIÆÊÍ-@±7I¦ð\x0012c·¢I\x000eY\x001e\x001c¦õû½dhè$W\c¨\x0012»ÖBä)ÈÅõ\x001aïi,·\x0015úâäÃ
úü¾¯ò\x0006Nj\x0011½^Tn uÂ©sIÆÈüFËx³à\'Yå(Bn\x0013UùÄ\x0018é/\x0006£¤ëmg£\x000cÝH´\x0011i\x000ev½dÙúNV¼ÔÖ&èí(Ã+î>\x0015H¶+Â5çc.EÏ³ÕQ@$8i,öru\x0010Ûõ\x0015½<Ý3¬õ<[\x001de\x0012yÊ.Â M\x000eh\x000bI´é\x000eU3/KÏòW»³§7·GÝbwo}Cåaz­æW\ÆCZB\x001eíý9pÀ^\x0005§ ÀÒÈô¦ÌçimæEä\x0001y\x0015\B\x0018:gD5)Å\x000eñ¯\x000bÂuô±\x0006ä\x0015¯\x0018ÑFÌì%B\x0007
òzja\x0007è\x0015×Ð\x0011_ÃÙv\x0014z6¥:ÃrKp\x0010#à%LMS©|;?Å1©\x0001Ç\x0014DªÐÑ\x0013©^òVä]I"L\x000c¬î\x0013ziáTÇ \x0001\x0006)J\x0003«k\x0016R«²½lnP´0\x0014Ü0/Y×$«6L&½<UNôSó\x00187oùÿß^\x001dinnÐd\x0000\x0005ãOU\x0003æ-\x0002Ô£²'1éE\x000f,\x0014ç¤+Þ
à ØXýÁ/_3é8»bêáWWïf;òa\x0015rãä\x0004\x000f\x0018\x001bf¶|àJA\x0018Ë@J#Ë¬¢{!uMµ\x000bUÙh(Ç2öåáÇ5J\x0010[÷n¦vr¬\x0002)\x001cB®Fz"¬EUUûÄF;9j|Lu±VÉ®¹äûv\x000e\x001a\x0008ºÞY\x0004]ÙÈ\x000cqTóHt(ÕÐÃ\x0006Ç©fa%uGLXø\x0014Çî³¡TÃ¸+È´ò¼u-®Cç¦Úõ8\x001aö¡RÃ·\x0005Oøi\x0016ay×~ß\x001c<i\x0001\x001d*5ä¿ÊHÂÉN\x0014%¬v_ôØº'H\x0018èlip3JÉr\x0003kÛêÖ5ÑèO\x0018tB¹\x0006$] Ø§ø7@:Má9Á4SPî\x0014ºD¼÷õ\x0005\x001d±\x0001ûMD\x0010fgôúN^ÚÆ.Ò,µØÉÄív\x0013e¦bW@|XºÛØ©ÜOä<µ
^èïï/8KñÍÍýí^èº"N+]3Ydì¤1)>x³ÜÆþi&%õ\x0019J'*8bN l¶aæä®e"\x0011Ró\x000e¥hâZ°îÚ\x001a\x000fSHö!ÛÇ1¬WÈ¤jèº\x0000xÙÄÄ®ÁÇe&¸FÁ\x0019«áÍÒ¨ÔÄÇxÐÛª»\x001eÈk*@d\x0014ùÙîNP6*ú>
ýëÛËç¯/ÞÐq:Òy·±C$f³¡³+9ÌUO§ë¾\x000bCmÈø&y£JÀ\x0019]ÙPg*cÙdÀ­%\x0001\x001e`®_a&y¼¡<o\x0001ÚK!VNã\x001deô¨ìºÃÔÖó1%¿H&N¾Í©ðôÖ	
h'±/L\x0018$ïî¨5"*÷<èQÈL
&\x0014pt°\x0016ÁÍÁÒä\x0006Aq¿¸\x0018b~Fw¬Ês?hÜü É©¶æðãJ\x0016Ñà­0¥\x001aämØÎ\x0004Ü@Î-ÈE­¦ÅuÝÂ°lÜÈ·yVE\x001c,\x000b·ÿéòH´a99ÑFE^\x000bÁ\x0004LXê¥Þý ¨òÓWHjês[1`ÂÐÃ\x0004¦L7sç Tõ½Zc/J\x0016\x0014¬,ûW:òIÏ÷ÏsH@®% Ó""h³Q\x0015t÷¤Ì×Û@ï1\x001cveúÏ|öc0Ø=µx\x0014yò	9t__í.\x0004#õdGÄ[î½k·¶\x0019h·-ùHON?Í\x000c$ägøâU7õÏ\x0017ð»'é®è¾ÞïªÓ«ß\x001fø¢ênÀop\x001c\x0007üº,\x001d
çÓ`\x001fÖÃ\x0004sÒ\x0017§¼Úü­Õ\x001füòq\x001fÆkpyqöOwgW\x0017g¥ãûìéÍ¨¾}îZµ²kÖKi\x001c· M¬æíñwÂÚ!\ ÑNð\x001f|bõ\x0007¿|bÊÈ\x000fL\x0000_|¤/øv÷îÝÅ-:Ê.°'Æ1z»\x0016\x0002\x0013±¶:d0Ø?\x0014ð0Ëä´UîÃ\x000bÚZýÁ/\x001fw¡¤XÑ\x0008Å&}sq{{þ³ y¼!ÞJî]ØZ3²Âå\x00173>0\x0011ôðÞ\x000eÉ§sÒ\x0013ß5ùÄ«Çª­ãq²Xµ¥/TÿN×²Úö9¢&|Í\x0011ø\x0014a{I9rµæqR|\x001cY#
°	<;O¯.ÅÜS+áÉ¸X>YÖ\x001dï4f¿>9¯Enþ¶ú\x0000Ì³R]NTÔüòFÌ\x000eÓB\x0016Ù\x0016fð¤0wÌBceVT0ç0Èzr})*üjd%~w¶;ûîæXc\x00053\x0017b}Ã<¤¤²ù¡gozvcBÍ¤gÝ´éùê\x000f}øÄù\x0008í\x001dûöæþª6ò^íÎ¾¾½9Z¬G+\x001dczÏ©Ï¤\x0001\x000eÁÿ!'±\x000f~ðìH_%Èé|ñ\x0007?|âÙYYPþ>ììûëÝíã¼e"h1ÅÛq>\x000bä\x0019=ÚtÄlü\x000c±uÃPsÒÔ3\x001e1\x000e0ûùê\x000f~ùä±	þ«±¤ÿÍîýåÅq\x0006¥\x0000ãþ\x0002\x0019i\x001f\x0011`~ãù9î$Ü9ò÷ (ÓBÆ|õ\x0007¿|fìÔ\x0018Ý=½½¼9Vµ\x0004\x0017Y[
JQ\x0015Í´OñÁqë\x001b^Ý0Nl\x0011\x0019²
¥7ÀÁ$\x0008(/\x001cËf+¥UÃ¿Ü\x001e|­\x001ctÙiï=\x0002WI§AP¸YëÓHÆNþ:lðâÌ}»»½;â\x0000#%Ùw¼+ó««WJ~&`dm²¦À¡\x001eÿ9?qÙy\x000bø\x000f>±ú_>Ù\x0002\x0007!Ó_vgßÐí.¯/Îv÷g¾º?R½(%+êÞ¥\x00155\x0012}HC¥½>LQCþÔUÜ®5°µú_>Ù 2jg\x0013ÿì»Ûßþq¤·Æ*	ÿ(°¥\x000b+j\x0019úôIèß\x000eMç¤§\x0012\6\x001b·±úC\x001f>{ià\x0016,ÏÌÓû\x0017\x0017Çj`\x0010¼?#âÖohË½]J~px@ìã¿0f\x0018qIï@9ý0à2Æ\x000cðI\x0006F#'÷é
h÷\x0015iíhàlþU3)4\x000e\x0011g´@rDW»LºWvvùÜ«ç»+Ö×xÜ,«xýuOÞ\x001eb·9ozöçÝùÄÙ\x000ej¶ýþðög¦ñ\@xB¦Úì=½\x0002\x0013n\x0006ÄrB²Úà\x0000\ï>üw÷·ÿãOWWì|~ùIø2å7¯Âû ^§7××\x0017/o®¡\x001fû§>Ù\x000cúáyëõDr\x0015m\x0013ÊlP¬.wJúÑ?cõ£ÔÏíÅýíÍÝÝPú2ý\x0018ÐÖÊïõ
do\x0000­/D!ñôsyùö½¿\x001e2wWW\x0013\x001fþK\x0015ÔB:v\x0016zoLëµª ýÓÑÎSeåÓ¿`Ço^\x0013öõýÕq,PæAqÃ´Z\x0000j\x0007*2c¼NKCÞN4ôíÍÕÑ\x000c4óF{TOÐ~U\x000fE3­ñÈ\x0006Ã²tb
\x001d¡ïnî&¹/µÐFYTÙO´b\x000bm}\x0014o=sØ\x0015\x000bQg®S¿Ùwg}ssûÛÿ;øy_¦&òvZ\x0012\x001fzg]ZÔÄ³ùÚÐ\x0004\x001b¹ÛÑÔCösx\x001bò/RSò=ûn÷v\x0004¿LC*Ç6®\x000fRÒÑ.\x001aR¤¼³^ns\x00157s:\x001aºzãÌùOMC\x001c-ý°»¿z1"O¾ð\x0004á`ïâ*º\x0017ý\x0018R\x0011ê'3û¤nÚås+tg¬¿L5.Ú^\x0010ù:ír\x0005mÚT\x000f\x001bM0ètTóT#	GP\ÆÞýyw{q=¶~¡\x001f\x0014Å#¯rÞ\x001bir\x0019\x0001\x0019Éª« ôÓQS?þøK7ôÿÙÝÞ\x0018/¼YÖ9t\x0012MÖ\x000bfI\x001dk÷
<·.r~z}¯¯nÄùY¦:\x001cõüðL
+ÝÄ½ñ!Ë[â0åNëÏñò\x0017ªÊU³Ûßþq=P|áÝJÁ9y»ÖËð\x001cÌeoW|rROû/ï~y/b°³ï/ßï^\x001dëÕJ©
+\x0001Xá\x0015®ºÉ>5~i
ÁÈ
Ò§å?ËBÓîìûûwï¸êzy{\x001c\x0017@9\x0018q·|aF¯1Q0V\x001e3\x0017{xóc\x001f óú<~ØÝqæHÇÇ¹ª±*ìÓ?'¯»f#Ï;9%Å\¥\x0017úã\x0007ùlýpñ|2Lû\x000bÍ\x0005öN>6Ñ¸¼"w}6å0\x000fª>)í<5Z\x0002\x0019þ~I9û\x001b\x0019æ7Ç:=:ËÝG·ºÌ<«ÅÆv±bmª:%
\x0019%OÏß/_]Ó?¾»Ñ"¡LVâí²ÖÕ÷aR9Ûò?Úü¡¨}{«L¼¹¿¾|~ùv¯³µ\x0010Óÿ2*ãß\x0017mü\x0007ªc\x0015¼d&m­LÝ\x001bwDÉjX\x001d»ã¹\x0003åíÍÛ{úwü_¹6\x001dzºÏ/Ât\x0007,^êxïÓU¾áO×¯.fÉ¿0c¢¸*\x00147½1!wÆ4\x001aaK1ï+QG;\x0007.\x0008kr¸×f¯0ì¶Ùþ*è*þÙùåÇ\x001b\x000fGñ)½uäg\x001fçÅcgÀé/â1ÒûP\a|´ühÿ0u¤]¨º\x0012=Oóo8øñÃ\x0016Ø«×?¿zU¹7GªÈq C¯XBH{{¨©ÈØºznáÿ£bÁ#m@ÕTw
æ_qèû\x001dðïo2õþôæ~\x0000Ói8å3<I1Çö"i\x0018Öe)\x0018\x001aæ\x001fl\x0007HÿöÄ{MÉ\x001d(\x0019àÛgøÊn×r5@\T\x0014\x0010Ê`0³-Û¬²3\x001dbU\x0006Á\x0019îU³ªúCÿîöÝ«÷_!üêí\x0011+0nW
9­\x00159&P]­ãún~¤íýÌ\x000bVu%·wë3\x000ei`Ø7öÃ¯o~M¸Ú½¿üí\x001fËíSÉ¸Jïl\x001f¼kîÖóÐ?*×þÉKfRú$kÜ^Y½èáyÇ	5l\x0012\x001aHnlØ\x0017²Mí°`C²u'Ûk©ÝJ\x001fm·eÛ&Û:\x0008ø=ós&²­ëöÎB¶[eû¨\x001bC'Éæi£\x001edG/"JÍ©¬áhÞÞë`D3À»³¯iÓ&­6_h"ë­£	û\x000eüoZÆë§íVeu\x0006bþ\x0015\x0007>Ø ^§\x001fEnáìëÛûGK¼èl£\x0016Ë(7êúi/·ågUh~Nø\x0015®êêvM·à^ÊÆ_U\x0014 T\x0016
X&\x0005l^íæV\x000fß\x0014Dê²\x001eE\x0003iq\x0011Í³-û-¾Ë?»ÛWòýÓoÿxùÔtÆà²¸ï9«=úþOcâ§þþAe³#mrUX÷
hÚäÜ®¾õ²F\x000e"C¤¬\x0019'7\x000bÙû\\x0000¾iÈ%]
«v#Lü.Ú\x001d[µý³×ooß½LØ\x0019p¬z\x0002ò©|×Ù´7,@ÕÆk\x001dÊ[ð(\x001bì\x000bfäS\x001b\UÕm0#\x0003|{.\x000bö\x001d4
ú¥9õ\x0013X!\x001by:-¡yBLµî²p!¸>ÁØÙ3\x000f²­í`¾ï(D{a}Kã¨Q!º½ò!eô ¸×cms**QNÊ¶y\x001cÐ-dû&[Z\x0005òF\x001a_v-\x0002xíÓdF·\x001dl¥ð®jí\x001b\x001b]ñNRêÖe¨qÜ\x001dç-`il-<º2¹«W\x001f~þ%I¼kã}4(UÚËJ½õk-ÑäÜxÆØ¥¾çèá®,ù¥ä¼Ùk¬\x000bídßFpby\¯,§©M\x0006Ù\x0006dWìÔª"ye9e`¥ì«T¶M4#DÛãiMuçb;FºR!Ûì\x0008¾\x0008o,Æ\x0013V\x0015\x0017X\x001cqv\x0010½ÞXc¸ô\x0003é©àä\x001bî\x0014²\x0004¬?ùé¥Óo%Tî_hË\x0015Æ Ö ^¡ML¡Ú\x0018úéØ¥¡	èÔ|þª¬îÚø*\x0018
Ðùó»\x000f\x0010zýßoÞ2È2üìOÇ²B:ÊªÒi­Ú;\x001d[\x001f\x001d(_y\x001eÅ
9?£¯\x001c¬PQ[o)@°õ^¸6\x0018«Ü¹¥
\%á@v³B´¬'àtêÜÆU1ÒíNexÇ`èf¸cV[¾\x000cRk²L=ä\x0018Gb/!»Y!\x0017j\x001ecuùc¿î\x0014äºÓÌq\x0000ÙÍ\x000c\x0001XiÏ
­§v½#>Îð\x0011¢\x0003ì¤m,jÖ\x0017^b´ùZuy$8ðÏv:¾¸ðÓ«Å\x001anoÞ\x001dËÚÎÕp)í3 ¦p1/yCî_óu±>/ñVÖg·\x0011ûÏ å\x001c~~\x000eâ\x0014ùJûÛ_,Ý.\x0016³û­\x001c
,;v²\x0017¢õd"­\x0010mA´k\È$ùþ½\x0010\x001d´Ü67{Av;üLfëTrÙÕ¸\x0002\x0012þÑ	ÙÁ'Ô½ûååOzë~K;ÿÛ?
°0 ³ \x0002Ì
¨­£â¡+Ü"ó\x0007áEäVÍuÇ\x0019\ÁfcÚäê¢\x0002%\x001dqëÜ,p\x0004Ùíò\x0008-@EºQUõ\x0007Ô;¡t\x0015²Û9õÉ·ù_¼n³ëÌ,j\x0004¹\x000eä¶Áìõ°%©\x0007y¦OðÓ\x000fÛé\x000fº\x000ey_D'FÚà³â¬V\x0003íöÑ¼RsýþqÄª»2W\x0013Ê4ç¥bíSë§çPÝ\x0014ÜÙ	gJª²ºÂ{Î
§\x000bdï<HGf3¢+ ý\x0007Ù¦ÉæÑ¹M´\x001c\x0013½ÉÂ¾E]NOÞA´]E³§\x0000ñJu@ô*\x001bió¹~<ó Û­²yâï:§ØºDqWÀu;«¤ÍW~\x0016.dû&gþÂ3¨\x0002Ò\x0002ÓwÙî=¡ØbâñìÐt\x0012\x0012ä¹_( hm¤Jøç'\x0012\x0010\x001dh\x001eªÁ¿L8\x0015GgÜê»ö5î¢{-»=¾¿<\x001a&4D+4gÚCL¢×¨å§è\x001dÕ\x0016|f´XuÕ=N\x001bqP\x0005Ã.ürqõâã\x000eL&L\x001e«nÇÙ\x0010ÇCa5dÐã>ÍlÇh1jë{j¼Só\x0016ªÚäXm¨ÛWke\x0004ª-ÚøyÔáÄvèÕY°<¾n%\x000f$Í\x0005_@«ìÊ.
ÍMÞÎ¢EÝtcµü\x0016cµ£\x0018eã\x0014=ó\x0013Û	¢][6\x000cK°lÓèÌxÙ&:+­íÄvìæ1ðw@gfo¥o\x0016¬0BÖÐu\x0018=[ûÓ·ãÿ×û÷GÂ*Y\x001dEÅÐÞ¬¶¨Lm}1Úb¦\x001fåè§2/ô~CQY(¡\x0000\x000e@\x00039\x001b!#w	%Oq\x0006¤\x0000Ù(1	aê©<0	£\x0017\x000e-9_³³\x000f²!S¢\x0002\x0002¼U4j¬Èö"\x000e5.æÙá\x0007Ù)±IlmÐº\x001cçI\x001e\x000b?-±ìvøvà8\x0004.Ì%²Cwät=8\x000eMvK8rú UsÃ\x001e÷Ò\x0008/Ø`Æñ
Bte\x001bH\x0007ö­ÈÂ\x0004É3à])Ä¥mÙIÄS¶µ·úe\x0016\x0007ÆSBv6å\x0008æmÙY\x001cÁv¼\x0001át\x0002(\x0018øX¬o7Æ
eï\x0007Y±µuîó"\x0016&L;y³Y<\x001btÜ8\x001aB\x0008×p\x0006\x001d8¯Lë%BÜü ïNö~8%Ãåm<°.\x0006qPD3²¦äëôö	×\x0018\x0010æ¨h;ñ;é\x001a3@²\x0008ß>:Î5\x0014É\x0002¿Ñ	;/Þ\x000eÆ\Ë«äÎ¯^NÞ\x001fÈ¢Þ\x001c\x0007éÄ\x0010\x0001\x0005³óÊóÁ¬_´\x0005¡i>¬\x0014\x0010\x001eåùàçýÓÏGÕZWø ï\x0005r!ÌÎ$+Æ*
\x0016:Öl°>@vÃÙ\x0018NZl\x0018ÉO°áaúH­³x½ÆäsÀ´(60V¢;lVrë¢eD@ö\x001a\x001b¡¨\x0006L¼JHDÊ¿í4ñf\x001cP(dCl<¤_\x0003§çfVÌ>\\x0008§&\x0016\x001e$¯¡!\x0019Õ\x0005ÐB/\x0014ð0{¹ÖäqÖUÓÅ-Ë\VíØRbØi²¨ýSTJ&½\x0007Ùy]·Î\x001aòOEÛ\x0016\x0013\x001f´ºÓvø&|UXIº¢ãÂx\x0004_ )érL\x0006\x0013\x000fÂ[Ê\x001eà\x0006´\x000b¤^ÎÃ\x001dY\x0016N¹DôöÝÑ-eÃs!s³üw+\x0002ý @jtþuOOè]_}La\x001cn}ö÷ûÛ£Q_YL\x0012·6\x0004P¬Ðf\x000c2ÔÎüaÄ\x0017Gò±«Ê:\x001fÛ0\x001e\x0005Àdë\x0013v\x0004ÐÝ\x0012	´äüÌHl¨d\x000b¹¹ý´±Öm\x0011Ðm
z1$DCÍN$\x0000¤\x0018|!D«\x000eb­\x0007Ò_\x0010Ý<l\x001dËä¯\x0015\x0005mN\x0006\x000bD+ù2»·¾ \x001aª1Â	öVÕAÏM¶èÌ\x0014g\x0010&\x0010Ýüëãxà O/H°h×f]Ò¢É2bÍÂM%U!¼½í\x0005Ñ«wMáCÃ\x0017¿\x0003e\x0007-×lËäÒÞôè,\x000e\x0008ÀÅ\x000c\x001dE£å	²c\x0001Ù\x000e¦·	oÞµÎ\x0014u\x0001\x000e_Æ\x0012(\x001fu@9X^ÝÀÁLM\x00005\x000b£¢ðZ¸\x0008&3Úôg¦\x00177·%\x0000ë\x001c¿uÂMÅ\Ò2zûâèõâhÎ;7Ók/êì\x0014åv|\x000c®1õöñÖ¡É¶¢Ò®h\x0003rJ¦âã0Å?3¯ÕÕ]'ã~\x001dÇ=éåý\x001dIÉ,J\x0014æ}ÕÆ\x0003JÌ±'\x0013\x001eËµÖÅþ\x001eÀº×ZgÙsá)Ö
,ýÙ{#k±\x001f¶Î\x001cî\x0011Èné=:GO4¨\x001e(l\x0015qôWÁq6cXìõ\x0018Ï© 3ã²×âæ:ºÊâº8Én¿|gm\x0001Âwçhwöôònwÿââöòh\x001c&ªGlÆaÂ|ç\x0008\x001bp%+zÂùíª¸¾à\x0010,D;1\x001c\x001e3,Ñ{i¬¡¡@v;¦-%W¦U\x0007ì\x0014¤Ù\x0008%Jë=\x0010Ý<\x0010òSKî`EVÄ\x0016\x0014Ú=ÝUðB¹  »¹ )û.Y«þÈç\x000e´¡J½´¿\x0001 :hÅÁ¤è\x0000%Ùò]¤xpì\x0011¼züóØÝ:\x0002a+ö¥ém#B#zæâJ Ád¢¯~¬îÏÃ*UmMrÛÎg^d¢t÷¢Ñ\x001b8Ã\x00006ÑD¦W=¡+¨Ä[i¹Jöi
Ôk²\x0001.\x0014òjò./ÑFºl!q\x0006Ù¦cØ\x00194=øÛk²µTIðÃD.:ôw\x001f~ùQOó\x0011tVyéªÓ3µÂxD±iµ}º¬\x0018ûñ§§N'ó\x00190Õª´\x001eM§lBHÇh\x0011ß c¾»¡qÚß\x0002²Û\x0011%\x0017	\x0019m\x0010=\x0011$ZàrÈæÏj/ \x0019\x0002Cã\x0006ß:&2IKï!\x001a?\x0003ml8üó=x(&¡!ÈÐPÖX\x0001.4o¼h=3øM0Ü*\x0005\x0013âØr\x000eAø[EîÔ¬ò\x0002²!4tµçiÿ¾fÓÅÊÚ·Û×)Â}\x0000\x0007²!£À»¹\x000cÕ\x0011~×0ìsÌ¶FÙPÀ°\x001a3Ã1D¢8­¬ì^s¦\x0012\x001e
\x0018 \x001c»5|)S®wgÙÙ@Ë×Ûx{ß<×oæfìþÃñÚñó2X¾"Ðù\x000eA¼#>û<;VµÖuÛf²cÐÜE.}ÉÜ7
dÙ8mUAv§SÊh#\x001dE2æ°àl§íø ÛÂº5TÙÈËQììä3NáÂÄl\x000cÕaB	§æ$	q²ÒK§ËÏ<L
¡z\x0014 Kk½Ì¼¸ ÛÙ¼O\x0012F ;}õ#yè4Ï:M6$uØËÎèTÞE^vwIÓ¼\x000bÈsâ
¶e/\x0005ë&Û\x0008+ÉöÓ´\x000bÈ½äÙíí-¥­ÄpÙ8'È­uH\x0005È0¤]@6ì%\x001dhì\x0015åÔ¨\x0015Â³¸;!êÑÝ\¿x\x0017w_õÑÂ×¯wwgÿvyöÍÑð`&ç ÷?ÙµÑ$Ç¤\x0000®\x0014zN8õR\x00157Iª'ÈO«Pn\x0004dÕ£\x000c\x001c²Å \x001b\x0001\x0003Ð\x0003b×\x001fid1 ¦iu\x0010d\x001fâ-T}H¶±¸J2¨1L\x0018´	÷?MÒÅ{ÒÿÓ+RðNU\x001d¶HïdT\x001cxTdq|yPN  ?HUmÝÛ\x0015\x00066.Ï\x0010\x0011+ðXqQã3µ<Ó\x001f$ÝlRt\x0011CÐìtIs®²\x0019'#´\x001bÌØô|ÿÒ½ßÝ}ùæâîDtÊE\x001d]ñ5Õ`BÆìTðu&ø	·\x001cV­õU¾dÄ@\x001e\x001fäLÎ³*ð3\x0004>ÈtÎÐ¾äCðx«ì7¡èkÖ\x0017\x0005#Íì4
BêyÔµ\x0008@³1­fç\x0013DCOYlÁ\x000ct>ÑÐql+{\x0002³µ\lh{fµ\x0004Ë¶Ò·ÊZäÆi-S¨\x001bÈÆZ\x0002\x000f\x001c8£OÈ-bÝ)u_cþÞË{Å\x001c>GKXk$³+pÚ+¬?%
êþ¨¹5GºNUYÝubh\x000b¸E¥éJ?TÏ# g×	dC\x0007±@£ç9ËÈ"kU×\x000fE¡ðäFlÈYúá}÷\x0018OØä%ï\x0012\x000f»Ü'\x0010\x000c-\NÁ¦Fa°}UeUè½\x0006\x0010Ü¼\x0006ïE\x0019ßZ\x0011L3¸[>Ó\x0005ÇØ\x0007\x0013 »a;\x0006 ÈPOÑ\x001d\x0016EªÈ\x0018¥Gäêúå»ÆGê£Ö,W?EÄäÒêÕ:CV\x0011"9nO¬j¬»Q\x001bqP\x0005#&èç»×Ý^\¼;ûçç7W\x0017Ç\x001aÙ¡bÇã\x0011y³ôo  \x0018õä±\x0012¿Ù¤I1 \x0010Æ\x0006H*\x0000ê}RÑvøî¦,¹»R-î\x000e¸&\x001bÞtQõNK\x0016\x001f\x001eÒñ\x0017N»=A6<¼Æ\x0003Ñ\x0005\x000f\x0017î\x001fÞ,¡L¹ô½
 &;/¢1ñàîd\x001bi<S\x0005N\x000cP&»e:
Yå\x0004¢ã:µ\x0013]Ô=¢IVÙé4>¡sNV@M\x000e\x001d!.\C¦\x0013ãfFAt\x0019ô¢Èi/³a\x0006Õ\x0006áÈ\x001ecQ+AIðXNÂÇ`|­!µA6ìf\x000cøªpÚÎKè=§íV¶·SÃvò¬98*ô?e «dæ:\x0017Ùf{;
$®FçÀ«,»?\x0018(#d/5íí4¸Z¯eoï¦\x0001\x0012\x000eFõS\x001ceY¢-c0SÞq³½¦m§õ\x0002B\x0010È«\x0014}B*Ëi´-\x0013Íöv¶Öº\x0012vì½\x0004×5Dª \x0013\x0005\x0010¶Ûûi
Æ#7I$oGv
©.|Êµ]{?-ìg²èlÇ${Vw\x0018^²CcîîòÅ¯Ww\x001f\x0007÷æÛË#N\x0013±]ä¬v#\x0005®óäÖæÇBÙÏi¯
ëJ\x0010ü\x0015Hlìåµ5Ö!itg´c \x001a²89Øc\x0005ÂzQ4Ì/$D«\x0019í\x0018¶°jQc\x000cûªxßäªÝ¬þ\x0000¢!?->§¶OZ3¢<\x0012nVI\x0005Ùþ«O\x001cÇmâ\x0006ì(dýµü\x0019r\x001f%68¤\x0017\x0000¢³\x0010
\x0014{ÜC(ê\x000f$[ª$©)¨´	×Ý\x00017É)ë\x000f`Özê\x0006p8'äT@f×\x0011Cók\x0018%ê0\x0012ûÿú.Å?~Õ\x0017<IJjÈAeW8¥$\x0018y\x001fd£x5ÌI\x0014]u^»òÈ(á­öòØ\x0007r¥O3#\x0003²\x00016La·IÂÈ(!»\x0003S'\x0015gY>
eNn\x0014\x0007\x0003¦«ÑiäÜásp³´D
fÆzafL~\x001eù¾3³h\x0003d73392\x0007\x000eÚ,ßÑ¤¶[X8ï×\x0015kYô¥GZ\x0006\x0003µèÛ\x001b/
Æ+ÆÂü·jÚÈ\x0018ÆZ%g¹T!Íùå»\x0003äÙy¹l¦\x0013þ5FÖg½×ÝòÝ.|®®®îû¼ÿÅÙ·t+Þ\x001dfÜäEªÔ¹Ö?o\x0016ú\x0019tºÃc[±Ù\x0006°¶j¬G\x0018Æ\x000cz¤%/
\x000cÕëçjÎ\x000c\x0002È?y0dk:SY¦åö3`-ÈÞ
Cèq2¹ªdÓ8«fðE
\x0005NïleËÿH!w:3\x0000²!Ä¡\x0010µË\x0006åë`dÔ\x001cw\x001fÔ\x000c\x001a	²¡xjj[Öª\x0013#¢aîS\x0002&Ì|\x001aÑ\x0013K°>È¶e%oZ·5øìb5ôpÀ\x000cI:tÒÏË]¬sfÖ\	²!0sþ	¨Äë'N\x0012¹h=\x00034ÁÐ;?¿ý\x0007
ÇÌ\x0011\x0003Ùp)­à*PF"æh#³<$@i@pDUz¨j\x0005Õá\x0013MtXÔÕPuðò@8\KÑd(ã%fNN<$\x001f3Ï= \x001cîªlÉ{á,AoÝm'\x0005ù³l\x000f\x0008\x0003®¸<ÁCh\x00193!Ç2ôhÈöpÌöX\x0000Dc(\x000eKo\x0008C­\x0004m\x001f\x0016Èö\x0014Æ1¸ÙÊä]´rz«Ë)Î²= ¼í§Íd\x0006Jdp0!	Îp?áðNÿ|/Þt}0-3
wWÇªÍ§ ¹ÊR2kéC'ÁãîêÇê¥â®åO¿ÓUc]r Q\x0004Rc]Ù¡³M6\x0013æ\x0018fµD\x0010
°3§\x0011\x000cí8Ä\x0014Ø0íeºÐ¥\x0019Ð\x001adÃùéfPx+\x0018F(Æë`ÆÌ¦\x0005ìæ·gz¦¡NÉÉ_|J\x000f^&M±ãldDÕ\x0000Åc\x000e\x0016'ldÈ\x0012±©Ô\x000cù\x0008¢óN\x001dQ/Îuã·î£ìÒ\x0001Ù\x001b1
ÿ\x00101
É  ÖNæÃS
³W\x001ad'x7\x001cæ\x001c\x0003\x0018²x7$ª.e3#¹\x0001Ù\x0000ã_Ò\x0017|öR7áðRóì
\x000fi
Õ+E')<\x0016lûðTp(ògØ^m»\x001eGRB×Vs&Û7\x0013jC×\x00050d6ÔAöíÝèÓv®>xÛW³=Õ\x000cÓÃ Rë$=ÿÜµ\x0010\x0007£¦pS\x0010\x000eí9"*G9×h\x001a-·gfI\x0010è½òópßVîDEIs*VÞu¾\x0005]h1\x0007?\x0000Ç&<F¡\x0016Ui2×óØU!\Å©\x001f\x0000ÂsS\x000b»äÐ®ä9§s/ï§Ï¥\x001668\x0002Mxs\x0004,7Eâè ¦Nw]¢>ë©\x001f\x0000²Ûaá:\x001bTÞy?Ñ\x0015p\x001dT¯îçÐuõþ­9÷_MÚ\x0015~Ø_\x001d\x0011¬Ç\x0018b¢òëx 7n IT~ÿL(DUô\x0007¶>ã\x0006ýxûá2æ\x0011	±Ìñ.S\x001bH\x001bô)ÇÊ­fï¤5LÑ7cg°ÑÓs]Îï	!¯û©úëq\x0011®\x0002
ö\x0008f¥%ø.;ù¼J{Ö¿\x0007 \x001b§*lie·¬H[Iß\x0011æà,Ý\x001eÜ%\x0001I9M^ ÄQÊÂ.¨4ÞðWï¯n,(\x001e
G§êCÀyÔk\x001bâi\x0004 |Á¿ÖUWòôl}Æ!
#Û~úeäp!ûÊ8³£\x0011\x000e\x001b)\x0019©l2+º¹g3°p:æô7¢ê«ïkÆA\x0015\x000c;¡ÒÅËW;y\x001d~¸¹¿¼¢¿w¤;Á>\x0005ÜËSin©§|Oì¬áDæi_ª±îRl|ÆA\x0015¼.ñêb÷FÜ¿ÓF\\_Ü¿?Æ½`9\x000eIáP0öeÏÒO¦9@2"3ýh.¹\x0017Uc¸\x0017ÛqP\x0005Ã^<U^\x000cèå.¯7oÏ¾½¤%\x001eé©ÐFöÅ¨÷\x0006yÆ\x001aYN??ÚÏ\x001dzN
ë_
º\x0005¿äº\x0002¦\x0011(S\x0014-l½±Jnc%\x0013GÐ\x001c¯²H~è\x0011[JGOà©
Y\x001a>RÒÝåËwgOo.DO\x001a)ô,¯*Ûå &­p~V°\x000btøûÏIeò¶%Ï×«%¥woMq!¶B\x0014\x0002¢ó³êÜ*¹Ñ+:4Ûè\x0015éo6r\x0005V-\x000fØEÉ!è\x0019$hÜ\x0006bp\x0007¥\x0006É\5ÇØ½A;=qRWÉm\x001c\x0006»¨-B É©@*­\x0004Ù\x00053%Ý[%·a\x0018Æä;ÜK¦Pd\x0005§°ä\x0010£Ô¶4®\x001bÝ)\x001bÈVî£JLðÞÉÒÖ\x0012
ôUp\x001b±q¾\x000fÞIªoÜ¸N,­Òémåyìlè\x000e]ñ5¬sì=4×ÒS\x000eiÕ"Ùe¡¨óét/\x001axN\x001cjÍÌg¡ñÔy#G\x000f¬Ç^Â§*fù.ÝÞÜ=ÝÝ^\x001eéYb2gñ,1u\x0018öYAòÖíIÅOØC8'}uu8¨É>$Û=\x001e´\x0011ïÎ¾+¾óÍ±0¥*Hä¹O~\x000fîà9¬8kPÅôhÒÏÞd;\x001faã#\x000e}ÿ¸\x0017ZáXF
_}»»|ws,oMånrc\x0008ëÕDÞ?<Ù=Np^è¾§Û\x000c\x0001\x000f<\x00105ßÍæM³«\ðÕ¼\x0007~9ïyQnG´E\x001eÅ¬
p\x0015ÜæÓ3Í\x000fÖk%ÑJËi\Súå§ÚH{úíÍýÕåõÙÿþÏÿúËëcÁ´\x0000
Y·o\x0002Æèôã\x0011:|îE&­õÙÞé7\x001cüüÉfX¹\x0019ß?N¯ÛÍýÍ¤\x0004rDi£ÖÙà<o£ÕÉèa¨í)Ç\¤¯>)ä< g­sàsÕJ¢pÇéþ\x0019\x001fß*\x0019ø:\x0016^öU=¡¤ Z/5ëÆW®/Pwµ{¾2×þö¿^]]\x001e­s[K2gn©\x0017Ý$È\x0010\x000bN÷q`Ò5µÖc"ÇÜ\x001f\x0005\x001aÝä\x0012%y\x0010Tô³m^%\x0003"2\x0006d
t\x0013|²öÏØ½^%Ë6\x001e¨\x0006n¡OrÏ¤ä<\x000bºVÁÈå\x0010'¸$FÙ.zÊõ$èZ%ãÈe]LV&·ì\x001bf\x0003\x0008WÁ0EGÍÀþqÔ,tád,@Ïï¬Ås\x000c 1&ú\x0000F¬Å\x0010^:\x0019\x0002J@×:L²_:áìÁÝÙw·<'îé?\x001f\x0013¸\x0006Ãäub}A.6õÐa×\x0005²pÒ/b\x001a&\x0012Ì?âÐ÷Ï6\x0002Òÿv¿»½£Ï]'\x0010^¼?J=ó4©k\x0015ð¬}¢*óðeÀ\x00031´+ºD6rû#\x000e*`òiD\x0007À8È§7××\x0017/o®_\x001c)ÞJB"£Y|ñ\x000b¦±¨P\x0018%O·ÖÅàÆá[\x0010¼}AxjgÓ:VÉ0Ð(ò`­ g/n\x000eÞw¨ç0
®[\x0011³)\x001dJ"o`¼²ó\x0007lÜ`\x001e0XrÒ\x0002\x0016£9\x0011$ÒÄg\x0015Üz{,ö\x0008DÉß£y\x0006§\x0014«g\x0008ÁUlÃ\x0007ZN>\x0002×*ËÒQ\x000e®d4ülJÇ*¹µö(\x0019	<Ø3£mcêBmLìS«ä\x0015\x001b¨\x0015¥A1s²Zªé¯\x0008É©ÎIìS«äÜ$Ó\x0013\x000b9_
u\x0004|\x0002	ËN³b\x0004\x001d´
ÃòÍÍÑÀ-äuÈVé¬Öª8·^ã\x0017<SI=Yq¶4º_ÜÙ\x0015ÃA\x001b¤gÖd9QÞQz\x0007fÐU2ÎÙ\x000cb ½î$Ó#ì­Ó\x001c&~qgWËA\x0010%Å\x00121Ý\x0018XZsõ'¯aÆ¦èZñe\x0002Ðd0-\x001dÅsÇ¸3,lÛ\x0010<É4¢I¯´$ÎÊnVX\x0005\x0003OÁä¬Ï]RÇò4d!9êYÐ*9ÂC!<Ø\x001b-ã¤/oRVÖÎF¯­a´¦öýc]I\x0004Ü\x001cÔ)CO-í,ñ1Cg\x0010=@­`Pt!\x0017ì\x0017æ¾\x0014±\x0017\x000cxco»6X\x001adÝ5Øø9Þx\x0015Ýn``&öJj\x000eTQÍN\x001ap_`\x0007¬ñ*\x0018øÄx.\x0008º\x000c^^@¶¼rÍ\x0015R»u\x0003\x0001gÌ\x000e\x0015\x001c
î6ÀÝÑ\x0015\x0014Ãu¬ýF[WP#¡\x0018ÔÉ³¼E gå0xãBUÈÖ\x001d\x00041\x0017 ÷%E#Î³VÄ§TÍ\x0008sWÑ­\x000c\x001bvR\x0017÷Ùç#«)iÍ*º¹\x0013\x0018¼¨h\x0013qÖG±j[%oÝC
÷0VÒêýÉS¦[tRòè©hf°èUt\x0003Esn¹è¨\x0016í´¢O\x000ey1\x001efë*\x001a¸dý[Ú=0:\x001f[Ò­S¢¯®nÅDo]E@[ÓÙvÈ¤Ç8^Y$c¸Ò'½u\x0019M»AV£u\x0018qNÚ<ï/< ¹WÑ\x0016tma¶\x001c­Zr\x001a®E\x0005VíÊ\x0013¾u\x0019M»$NÌÊæ¾B±j/Í\x001e\x001dE=c\x0006ZEÃe$\x0013\x001aáEÉÂd#u+5ÊÖe4í2\x0006ºØ
*ÿÚÉq"^É	ßìé³è­+c90á<ÒÀä`ØWÅì%\x0012TP\x0019\x000fíÖ¹¶í\Gå\x0000ÄÂ\x0017nï&ØI8¸ÂKj·YH\x001a×j\x0019\x001d[+B
Rt.\x001eÝ:\x001f\x0016Æ\x0015Ù\x0008¥ª@.`Ø·QòX'Ú­M´0®ÎZcÎá0A¾^1ÊLbt5­ºµvÝÄ-Çý ÓÏþãÖ&:ÕDGá'Õ\x0017\x000e$·ô	d]ÆL»­mtë6Z®¶$\x0010$cÓÆJÑ®ÞÚF'\x0007¯Å¦\x0010<®ã`49ðÔmm£¹k$«Õ\x001cé­eøQëi±9«è¶vÑµ]äP\x0017\x000eGELí¬\x0012Ãß­J%×ì·vÑ+po2Ê
\¡j+GTY½¶vÑ\x001bðABµ÷AÈ6y<{\x001d\x001f\x000flâ×Ëoí¢wÂQU'R\x0013ïë`)¿µ¾mb\x0001õ´£yx¤°ÕB°-\x0004n~k\x000b}ÛB.Êxô\x0012d'©sÚËË\x0014(\ØÚÂ @t\x0002¯)²WÜ\x0006$Z8¨.\x0014ÖÆ°µ\x0001vÐ#%\x000e\x000f¡\x0017Å\x0013ç$s\x001b\x000f7\x001dËËqët~ØÝ\x001f®ó¾rhVR
Ðï\x0013RïèT'\¹eu©\x000b\x001d=øÜÂD|1MòÝW[îÿèPùaÄ°SØ\x0015«éUC¸S\x0012\x000f\x000eìp\x000fe\x0008£ ;Åh§¿í\x0018Nÿ¼¹¿½¾Ø\x001d\x0005ïÄ 8[*¢Ø/jÃÁg\x001a\x001f'öñË\x0010¤7YØú
ì\x0016ûqöw¦1ä^¸»×Gÿª­¤h*í\x0011+ºð}\x0000\x0000[W#ò(7îó\x0017¡\x0008¡ð\x001f\x0006\x0013)ý\x0004Ù¯Èéf\x0008û)<Ý\x000c5\x0008¦Aí\x00187NÛ$Þ\x0001]i:\x0006Ä\x0019*\x0010\x001bZ?´a3Ø²\x0019
\x0010JN%fÁèBjz$R'y©U.{suó|wÅ;\\x0014\x001esûµwÏÖÌËrvk[Å_oÎG¦
ëg§Ö\x001d¶ )ä\x0016²Dz¿|i
,w¾3´p'Ð+hK¬ÝZºE·\x001f~Ç\x0015wÕµóûæþúòùåÛ½\x0016\x0005\x001fE
üû¢ÿ@\x001d¬2ë\x0007©5.ä\x001eoÛXY\x0011\x001cd¢&Bf\x000fòíÍÛû«BnòÕÿÔie\x0003ë×ñù·³ÛoEÎÔÀ³û\x001fÍ_ïqÏ/Þ0Ä®7¾¿</Ù±ýe\x0007G^\x0018ün
âÓ^aG{·\x0013ÀtqdDû½'à¯\x0007\x0013\x0015|Êdíõ&ß\x000fÅ¸Ì\x0004[æ? ÄÇ+=\x000e\x0013¢×\x000b#]+d\x0005
0ü\x0013zµË´vC?¡{öBß9õNú
º\x001b½À/¼Ü!9\x000fk°¹d\x000byù)ó\x000c»Õ:ò\x0018EW
~\x000f½·Õà
{ëb·\x0005US\PtûÍo8øýÃ\x001e¼²ú£Jr\x000fÞÜ¾8Ö.x
¬JLÅÊ´ºò\x0005tLB«\x000c\x0005«\x0017½Ó¼aUSâm~ÁÁ¯\1m~ì~o^û_.®\x0004>ëÝ»w»qPÇ\x0017^3\x000bl_u\x0019Þíh 8Å8øJ+~*×ÌvÛPU®ýê\x0013ßpðûmH¿¾|óÞÏ¶áxû\x0010ÅSF·ß­æ,}ë¤opS¸òÉìCÕV¿\x000fóo8øýÃ>lc²È¹¼½¼ûí\x001fGr,tlIkZWÑí{§&l-Õ\x0006Í±üdÄì\x001f½\x0019¬.ói«×ã±Ø3&WØ´§?\x0001\x001däTç\x0006Gã·.Ä\x0018\x000bäæThÆ\x00137Á\x000c¨E§B\x0005%ü¬'M ØÂs£\x0002'Étv\x0011KNrÉa2V\x0016$7¯+,kÂ$hú«
\x0002]ÎÊrÍxÝoIömÍ®2Yî×ÌÁ¿Fmè$$§TÔ\x001c¶$¶f&ß3mÍ1\x0008mDm­\x0016kN.N\x001cÛ}\x0012kæ© \x0011×l¥»M~ä8¹
$§¶fþïÛµÎO½Éâº\x0002"É[s\x0013Ì^Ô\x001a\x0019i&"J(Ù¨^×®\x0016ÝÕèÖÄÉh\x0002ÎÛ¯Ùjá#sXó2peë
j¸Ù7×OíÎFòr\x0007}\x0018\x0013 ¹]Á¹m:hÖFà\x0004H¶bÍ	ÖÌy\x000f¹ä /J\x0019®·î v¿{\x000b·.¡nÐ(¨¸ó¢s+ Uç\x001cÅªkeAoÝBÝn!ó¯Ý7´ê\x00043mËª½\x0008¡¼®m\x0019zë\x001aê\x0008FI·²8­:\x0004ìg£$U\x001d«>¶®¡n×\x0019ö}»ü
)ã¢\x0011çBü8â&@4\D\x0003\x00145´èd±\x0003\x0016--G.YÍÖ54
\x0014\x001a\x0018ÖìaækY³P³©\x0014¾fë\x0016\x001a
+&k×Ô¬îì(ÔÊÊe)cHÌÖ-4í\x0016rÕ	6Ðr\x00172n é\x0017\x001d
\x0018Ïl]CcÁøG4þt[Z\x0015®,Ú©Îæ<â\x001a@´\x0017¶c­JÐVY¾ßd<hºN\x0005±u8L;\x001cV¹Ö\x000fÏçNµ2\QIF»bKÃnó5|¶\x0013ok7Q(o¢öV^rWü\x000eÝÏ\x0008@o©M\x0008`Ó§ÍÙ¦WQgLã÷\x0011Åu$Çµ0>ß|¼=\x0007/\x0001JÁü\x0012ä\x0006U®^íürotÞÒÎ \x0019êÌõNº\x0006¯\x001eYg´³é\x000b\x0010,ÙLY\x0012¿Ý]N8¼¾Ôß¶¶÷
M;ò¦°_ig\ExôC/Ú'çTmu\x000e7Ïø\x000bà\x0017ÇÜùF¾öi2Ó\x0000\x0004ãc¯ËHäõà«Æ^/¬L\x0010fëç\x000e·é\x001dî
\x001fÜ®©Ãm\x0006;x|65\x000fj\x001eJöKë5\x0005$ù²øjÒ8º®Ùx±f54a±\ìZ]\x0003Ì¿þöÛë£eÕxe\x000bu
õ=\x0003ÕÚa)¼*\x0010\ÚøI ª¬>¸dÄZÛ\x0004
û\x001b\x0006¶ÚJaèÍ\x0004åd\x0008.mH\x000eÚ^\x001eß!$\x0003&¸Jãø\x000e\x000c-?t-ºä!9¢¸£kÖa¬µd¨ÙÐ5rÁÏ0)\x0005ñW²ìÖ|\x0010ÜÎ:yÄ¨äM^\x000cÍªEr²\x0013ê&\x001a¢\x001e®\x000f¶\x0017Iñ¬6¦Çº[tÙÁIØ³^³­\x0014¥ç\x0017'ÑtVR@ÑÚ	E\x0007_,á$îYD·Óñ\\x001dÇ&\×laL#·ßÕxb\x0015\x001dP\x0006-ØÌãErX%§\x0004bÉ\x000fÇ9\a«üB ¿µ«»¼e@\x000eX¹O»È5M.Sº5¹<çÁ	Á^\x000b_B-ÏØÖ\x00054-5|n\x001d<"´C\x0008N\x000b¾Û#\x000c\x0018D·ýcL>Ø#£áðhðT ±ê\x000f¸ËhHðØÜBõ$\x0008{Ôå¤lÝÂ­£aÚÑàI½ë\x00080:RQ78V!¡ªí2]×¡å"º\x0015\x0018\x0002æâ*¯\x0007~Lã\x0001±1Û	À\x0018D§¶j\x001a>\x0004y]\x0018ÁÚª½\x0008\x0001mílD\x000fäÜ\x0016m!jå¯n,NeÑÐçY\x0016\x001d\x0007n·nU ÚµV/\x0012m£Hh+õ\x0011K\x0001ÈnY;Û¬\x001dC1×ôÏ\x000c£Ç<«Ï"\x001bÊJ;Â¢Ar»<\x0005M>èÊR6Nèâd\x0002+nWÑ\x0018Wà hïEÎË'-\½>»u\x000fm»ÌU²\2\x0016&ÚGå¤M*KÞºÖ7Ñô\x0016Úv¤]6O"Jöâ\x001e2¼¥¢û'\x000bÂ?º\>µFCº|!\x001eck+¯.\x0013Ö!Ú~'×\x0010\x0014ü:Úôe2Þ§¥^ìX#$Cû³ïî/ï
Ñåíí\x0004(ö\x001aN2+ÏX8ÓK¸1jH|·\x001e¡2býgÅiN÷q\x001a\x0019tÌ~«Ôå\x0011Ì»1övê».Áw¥@­eVÈÃT2EC¾\x0015ªÌ\x0019ïë"\x0019|×\x0014H?P&ì£\x000cðÉ\x000fÌS×u\x0011Ü\W¦ð7à\x0014sÖ
óLÊ\x0007±äÕ8u\x000e$Ã»9?%\x0007OØ´0²Hn)YÍóÔ"¬Ù\x000b¯;U:mÄéøl.¡0D1'QD¯¥;(ÏóÂÈ"9aú$ó\x0001dá ôä}\x0011ÆWs9·fçt'\x0008¢±¦óó<D¨±0b\x0013:UQ¤ò4àÓØPØã&ñÁ"·]@Ë}º\x0010.1\x0012ÏéÎ\x001c¹Éåý\x0019
íþ`.ã\x0000'ÆL[Ö2®I³ì\x0000bßÿtuõÛ?Êhñ\x001fnîß_\_\x001eËÆòx>©ð+ªÍ2³¨¨ÐùG\x0000µ¥Â\x0018ói\x001bëûü!Ó§%Ì8¸±\x001eè®,0Îsa¾O\x000fð4>½\x0008Oè,ÙNp[Bß\x0007ñVi¨(ò\x0011¥52­òÈ\x000b\x0005r¡ÄÃ!9Ë7_¬8ËX-ós3HDíóUGÆE%®FðI¹æØ%ØP\x001eDP\x001aä\x001fú@ËÿY	«\x0011\x00015\x0000\x0000¸\x0019^XIo¬ð ¬æh\x001eÿÅdË£1<àÊaTë£\x0016Gl8H^ôTú£VSf¹@&8GÊÛ×÷y°Ü\x0000Øì%­_f\x0010¼çÿÇLW7\x0013¾/ÌxÆ,^uJþcq°é
Ô\x001a"ÇX\x001eÛö\x001b}Èå8\x0006+ÏP¦£´\x0006®ë·">
d,£üv72ôävJ¬å\x0018xö¯8CÎ;\x0011{°s5=Cä\x0016èfü¶äe°´8öb\x0018	@pô
¬µ\x0005§Ùø6	`
ku9 ¹\x0005z´æÖNÃ#Ö­¨ª$6UpÃh\x0017É-ám`ÞÀôDìíÊÈÉÑo\\x00047¿ö£a­H0×ÅåþYö$§~ã"¹e[ø\x001c@²â£R-×\x001cJ±vô\x001b\x0017ÉÍoT8ßÕÚÐ\x0000Î2ûÊ´ÉãXEk\x0005.¶Ü2\x000bNn\x0007'! \x001a\x0012ÀF·$>ëÃD\x000e£k¥h2säË"ÚB\x0012æÌX´H¶§ÔiºÎmÞº+|Q\x0006¬r¢Æ\x0016R§Ù©
ÔË"\x0016ª\x0003A5ÄÏ93EjR+yêLÜ@½,¢ÓR
ÔMÍ\x0014õuºÈAw¢'Ã\x000eA4 ^\x0012)"UÉI!°\x0010Ý>ÞÔ8÷þ÷Æ\x000eÒ,ÌÔ'Ï{pOªSIª¥Ò±¿
ÞÐ^z\x0012¾°k·»¤RXÿ,ü|[ø9¬\x001cjH\x000c¢ÈK\x000f«X8wÌJø\x000c\x0011¹=ýÝB~¬ê&¹È²\x0014 ÍZÌçbj	/\x001e?k\x001fÁ_\x0017ó'5÷!Ã}y-ª¦°ZîuîÂH	TÆõ%÷·Ì\x0004\x001d\x0018Jð¬rn\x00151}VGpÛv2¬\x0015{\x001f¥Ó¬§O\x0019R\x0017tCU{(èïµñ¡µ\x0002"s<oz\x000eêÙ¯\x0019Âu®/Á¢¹yB¨Ùfy¥â´¯»VurjoÏo®¯'C\x001b¾4V·\x0012Ø\x0016Ó-r¶dÏ¼½ÿá~-sH~\x0016R¼\x000fÖ±\x0012S&®kð·ÛäeÖ+yBT\x000fÑºEä
pê1}¢áÈ>ÏýZÝ\x0017ómOcg\x0006óiÖtåëêqM`ª}\x001eÀ°WØÖÌuV%w!à­;¶º¯æ3
\x0012HF\x0002\x0010¢É²À\x0010\x000b3Ï\x0004£Ú§\x0018\x0018Â×z_¢£¸¹Ñjv&k\x0002Q\x0015ÔÓe\x0003£@6\x0018-ÓÃ&vÉÅ\x0010æîç"\x0019ÒäoBU"(`µIöüþÿÌ½Ër]Ir%ú+4nOhñ~\x000cÅ,UJ²¬Ûi¥k5\x001d L\x0010`âÁ$ÓLf=íOÐ´G­û\x001bõ'ý%í\x001eqÎöå\x0011{,c\x0002 $&ÀÅØ\x001e\x0011\x001eþ\^¼Ù\x0008/Z]~°y\x001d^åâh3<°ÊÈªèK§\x000e²C­Aa­Ù\x000cÆË	ÛXcCjõ*(\x001a]3ô×êÍhqÅ¤N4\x0012Öõ\x0013ôªmY\x0019.
ÐP
\x001c
è«Ð+íçUp+Æ´V¶Û³Á\x0010B\x000c\x0016·ÉÕ
·A7)Ð\x0015oí´±6yu\x0013!ÎO¾ªzÒø&ªe''HÚãþâvSÝ·ä´È@óM`\x0002I]©Í\x0010ÒZè¦µ®µXÿûîÍÕÅ©2é\x0016\x000f\x000f¸[âÐÁU=þOÐ\x0019ø·ýB\x001e6RY¯À3\x0019dròº\x0005)a×3}yxØxZ!ú\x0019Õès_*o$+fý]Û\x0003ËÉL<\x0006\x0011\x000c¢±Ý  íCº\x0018kÕà\x0007HuãÅgÜ\x000c"ãt.s?Åª\x0005ÿ\x0003ÖqmUxü~aÏ\x0017ûo*n\x001c\x0013Ä<\x001a&\x001eä ûÛT  p\x000bðzmãäTdùanÉSþ@ÛEÖÓÃ~L\x000fó?\x0015±º&\x0007\x0005ë¬È
9 5d"\x0016Æ12ù2ÎÐÚ#¯×ñú1?ìm\x0000"!;?<ÓA[p%´zºªÑ\x0013b%©=656\x000e\x0006^\x000eeg5;S\x00030ZC	\x0008d´TýF»¬·Ò[ÅVªF\x001f{2Àmê±Ëcçãzß²Ã8îl\x001f³ÙÉAgá÷å´k\x0015¤Sz¸¨ªW¾æêsÃY^¡\x001b\x0006\¹~5\x0005°¸\x001aCÉ¢G®öÚâµòQ;D\x000f]µÑfÆoíØ¡@#ôçÖE±>\x000cXÜÈuËV§\x000fë è²QAjX\x001c³æAFü5\x001cÈ.Z­6ü
½. C\x0018S¾B¹C­*lMîÙótíØ­§6hèæâèiê´\x0012­.éKèç\x0017çXÙAq,±²náã6ò@¨e=(ÒÒÊ¢ËJ©Ö^&\x0010ð6£ÓÚn¹B\x000fqíÛµB°ý\x0001Ä.&\x0012²ª>Jã9Ñ]½Å7y¥\x0011èp×qéEI½éT\x0004÷^GìH§öó½¹ô \x0004cTÜ¤!=¤Þ};âB7(t<zVN&Ò\x00060Ó±>/±¿3à\x0011\x0017n¼ÚQ@ë¶´<ö¯åQ×:FZ&õË\x0019V©8íÖðpH\x0005e@Þù<ÌñìÍ\x0018\x000fâ\x0001+\x001e
 «ÌæTcÒ?Æy~	 Cj¯@\x0015.#gÍvP\x0006»¦\x0010VòofÈ¿\x0015\x001eÌ\x0003gGË)ö:àæ¼V¹iÁû×vww\x000b¡ÅÍÃmÂuýâõîTÖ¹É\x0011¯K$}Ä¼-ËphrCy\x000eýãs*1¹ëß\x0016­\x001c]:ÇM¥°~ú£n_µªú#\x000ektY\x000b2X\x0007ä{AËw
²Ê<Æ§®\x0013¡z,PX²#=ªh«ôO´&m\x0004+ódg)¦5s\x001b²\x001bu-k4qÝÞ\x0003C%×®"Ã@RmXÜRªY\x0011r\¿Q{dH'ð,?élv´dÿ£
Ö
õ½wåu=l >#ÜÐ\x0008ÃWáEv½¡Q/»T_yÿ\x000e¢FpÕ¡$áävÓ.µw¤\x0019£.xxqrÚD>V:no«(à¡ 8\x0017û M<Y¯­
£UR±I·Ä2ñúôö¬\Õ0]ÕÀ¹\x000cþ\x0012Ï#\x001adº^\x000f½Gzh®jZæQÙú:tÅ¼ Û#Ã¢¯\x0007«/ó¼XL\x001d×¢C5©õ¶¬Q£ÁÅû\x0016ä\x0015Ã	æ\x001dJ\x0014SjÐNd8¹ö¢`\x000fE®KX\x000eXìÂ#4Ó\x0013PØ­×Ó®\x0018NN=M¥hÇ1V2\x0005Ëì@*»Sã{_©Mqê\x0005)ÜS%> Iû\x0001P¨ÚÙñä"¯×½îÅ"ãH¦j\x0005¯\x0012.Ùë*}Ú.·a¹Á&ãé\x0019µÂf\x001a\x0015#U%5~1·fÌ¿»½|=
¦þæ\x0008©×\x000f«KXÛä%q>=EtèmNÜë~Ù­õ\x001fýôi\x0013^÷ÈÌ~\x00138eÿ×Þ?þT{`UÕC¨\x0016ÂÔäL!÷Aò<TÂx\x000bÎ90\x000c¡lê\x0018EWBÖâ<ÁUÂøT\x001d \x0003f\x001d¶\x001eÄf\x0008B¸I·Òrý@Ã\x001dm(\x0001Vá\x000fÜqÅ½RY_«ßÚ©nËÜÃ'\x0002Q\x0014.\x001cF\x0000\x001e(\x001bÎá(ÂPk?1ã·\x0010B\{°ÈYûñò§ûûñ¡0\x001b¢V¯EÞ¬ÄãØåÍjK®\x0006Ú¸±ø£_½AÃ;Èlªãl5e\x0016O\x001aA»AÑL(L[i ?3Ç¨J`/^¿*uýyÕó\x001a÷r·jCYÃJL8+=Í)ÊLÅ\«²\x0007
Yª+
Ø!¥ðîÅ.î\x001bÙÏ!\x001eñ/»iLé·\x0012ÿ\x0004õÚ'\x001e+~(0KôTØ6ì¹¼ã±<'±5c\x0019"\x0007ë_pôë×z|@ïgøúæòîÅ7·o>¬½×ê\x001a&®÷Å\x001a\x00170\x00089\x0003ý\x00141ÆÝ»f&\x001a¦õõ\x001fûôµ\x0006Àúr\x000bë/d\x001e^¼x}E«üpª'<qÍÕó\x0012ï
¹b­¨Í@ãy2o³ÐW 2+$;¬r\x0000¬Î<òðU]½G\x0015]\x001d¸éO,7f¬Ä¾(	*+ÂV;S=¿î0Q~ß}Ø=|¼x±£ûv{óæTögÔ¨ÔH\x0004\x000eVVÆ\x0012ãìê3r\x0002Ælø9çÈløúú~ûß8aùð`Â?{m\x0013\È?Ü|Ü]^\x001f.åwç+£&l^Û1|ÇxT´c¦W<\x0017ôÀÏÍ	-/¤ÎsÔÌkÕxµ{ów\x0019ù\x0016ÙdèðûáâÅA<ÿïÅÃ»ÓHÅT'F?K%¸ÃÙû[æ;»À¼¾X*ò¹/ø
ÿsãØ\x0015þîyìÊA§Ðó\x001cÔIðß¥\x001dÞ \x0005{$\x0000£\x001f&¯xopòJ_Ä7Ï\áqúÃÏÞD÷PßÏÏ\x0012Ùjÿô@÷ör÷p¢ÝÎ\x0010MâÝ.­®¥\x000b~$4\x0017"÷cò\x000eü~YW~ü1:\x0008K=G!s8sé,¤µûÐ\x0005òÝ	gÓwï	¨¶±`G'O5a'Û:ö\x0017lªI6É3·B\x000e¼/ª= Óë§sõYcÏìr
:
4Ltå½¬È\x0001GÈAü~\x000eÊ<ó]A'^\x0012î\x0004\x001cLµê®úÕVÂS¶\x000bl¢\x0011[±
VÑ\x0013¶$¦ú\x001e\x0015"pÄ^âÝt¸K\x0016(> \x0006+Ç\x0008Ûá\Þ&<\x001e)p9!ÜCä\x0000Ü\x0005¬+á[W³\x0006÷+#É\x0015¸\x001c\x0012BÛ$c]\x0019\Ð%ð\x0014W*Ó\x0015ørLRëÈÍ\x000bx(ÀMÕ2÷a¥ÑPËA1\x0001BÛ´rSõ¥L)èÇºB)à\x000e6Ôd1@iåLn2OÎªw­¼B§À\x001d¥Oß^ÄRÑ\x000ee±\x0004-0Ù¡þ¬Ø«ÏùV»á»«ÝåÝZéÛô¹u1«Ç+,³_B\x000eµJÞÑ¹É­oïÉõù@\x0018w\x0010\x0014;Þ\x000be\x001cs\x0006I{»QO^¤W»H.?Z!\x001f\x000b\x0001÷ò\$.¼\x000bb\x0013DÉd\x001em\x0012ð¹pl\x00165ôñô\x0000ºû»,î·Ñ½Z{µ{ý5míx6]ÚÏ\x001eð£¶\x0001tÑ6±BÐMhÒ\x0017t_¢Wè¹×QúQÝ\x0000º¼J\x001bGòèqnè£¾\x0001tÑ7Sº\x0002\x001eJ\x001bð+àP"×À}¯\x001dôy\x001b<\x000b8\x000fõ\x0005tc°¢ÐÁéetJÔÐÇ§\x000fÐåé#«[Ê¼\x001dGôÕ³Jæ\x0006ß\x0017&úí«äå*K7RÇóH^ ÚSokü0*bA\x000f¢}µÒPî\x0002×QE\x000ea\x0019Fw)¶°Û<1ÎE8Aª¿\ôÌÝ§ÝçªO{hý\x0018n[ì\x000eÅÎ\x0016¼PµöN-Y{ÐZÆ\x0015=÷éêúê·jÛwW¤õN¢ã]uP6ÈMjT¹í\x0003"\x0017È&y\x0005\x001bv~L\x001d³]K#äQÙt!µêEÙÐWrre\x001dX\x000e\å\x001f\x001e{c3]´mðåäÄaú;¡'Õ¡ê*FnX{Q+8èeÑÂ1ç\x000e\x0007O!ª\x0000N6^zo"'Ca\x001b<ÈÒ­Ás,\x0018eOºsº`öáÛ) \x0018²}\x0003]ù\x0006+¼\x0007±>*a@_03¢EÉãt\x0013Ý\x0005¥â	}/öQ\x000b\x0003z\x0006ô*Ý\x0014.´1<\x0008\x001eº*15\x0012Rr\x0015¶Á>ÀqÙSU\x0005íésØÔæê³^Eì1£{Íc@
ÝÚõ5}rË¨\x0005½¿\x001f}´h\x0000ÝýýèÛw©zQ\x0003LÏ\x001a\x001e0îMúÈt\x000f§n_¦*JÆÒME=\x0010<&Ô\^{¬< ¦5²n\x001ew'>Î·JÆM¶ ­\x0017\x0013ÁÁûÄ\x000c0XÉ\x0015ºÊY÷ºûîà¤=7HÇW\x0016ÏC
6þ½¦\x0019s*þì6]ù\x0016ÄðÕÃ?ß\¶!ç»·'^hupÁ&¿\x0004\x000fnBDEöÏ s\x000cý~èª\x000bj\x000c]%ÿÊÉùä\x001eîßì´«YM\x0015´\eÜüq\\x0019í#wu<íaÙIa{É8^w\x001d"nv¦kTØ\x0010\x0017Pß5UGÜ\x000eÖ°\x0018 CX,C\x0001$"wBöE¯º7·ª\x0000°!.Ð1\x000bÑjç$â@M§ú)ì\x000cëV*20-\x0006$
4\x000f÷8MiÈ\x00146ÝRÐa\x001a¯CcL.¥e2\x0013A(hñ<Ö.åÑÛ¼\x0016Ï\x0013dçYrÇ
Fh\x0014©\x0002o¤²ÜY uîRTàp%¹¢Qaßu
+J"¹v3cûRB°Ðf\x0007ÞX`¿2èg}¸_u¡Àáæ y
GTA|N¬ÞKÓ}àí\x0003\x000eñ<n\x0015@û\x000c®\x001cl\x0012Kc­Bn\x0002îP,ôr¢Ì
J3¸R¹4ÒA·-\x0015\x0007R)\x0004&ÐÖé¸2÷Ê)ììÛ\x001b½-\x0014Ô\x0011³â«vPù«[cZÇ À>ò<ûìôÛ\x0010uîë¢ÿc\x001aØ\x001en\x0010Ê	4\x0014!(I\x001b]{-;EÀ\x0000\x001b6\x0013\x0019«\x0008\x001bÕ\x0005JIï&ÿæ\x0010(pØÍ
]\x0004NfºS\x0012ÏZâ©\x0005Rþìíõ]oTlM\x000f7oO\x0016e
:\x001d<p%\x001fì.æL\x000f\x0010¡×Ó>jlÖ»ÕùPa|û» ZÈG\x000cv²;_Y'«7^§$B\x001cÃ&dÅñ\x0006tÉI´a2\x0012úe.D\x000cý\x001arÌt0,6"5\x001bÆû
èË}M¹ÄW\x0001^°ÌÐ3ù°ôÖ°eÃøL\x0003øòL§ªtUðÒÕð,oH÷g½ôþpQ\x001b\x0000z\x0011t\x0017À\x001b<6X\Ö\x000ebOº1N\x0001Î\x0005=J31/¡IîÔ\x0006\x001d\x0010÷<Þw¼Tõü£7\x001ftéÍÍýîöíÉ8\x001c³èi\x001f¼QÔuo¾\x0006µ¥3}HÃã]*öL×a£­Ô\x0005ÕâU\x0012\x001fHÖ
Û?¯>½òøáU§ùbî!à2*{\x0001/\x0012\x001edã¥\x0002à¶\x0002\x0016t¯_[Ó>!n£[A·\x0016M\x001avS#º©\­7ez4l|L\x0000]\x000f\x001c$ï\x0001=¶[ èÆ{>\x001fMó[¾¾þ(GóG:	\x0017/þpqµûx~{ñââþÅ.Þ|Ø]^ÊSMÊ\x001c¯ÞÊëZFå`mÜ¼¿'×üÃNtM®jÅhsÌã³îµSmi²\x00156ÚV¹Á´éUy!0\x0002®ûÁu\x001e©°ÁWeÆLXvndß`ÿ9
íæQ
Yl\x0011g1ÕG«®ïTÊ °æ«\x0002¶øª¬¿àÎÆªRÙÎñºòÄ·Ñ0£²\x0007lñ'ªw\x000bÉ\x001a$[öÌÚ§îTnl§ðgþöWúþâ\x0005Ý«ëûÓÜ"Çäé¸1¤ß\x000f×(ùhUÂ[\x0013O[°÷»×\x0007æünÕAFÚKKÌr"æ1ïcë^¾;éJÅbÏ%1ªè\x0010Õc?\x0001ð¦\x0005$¹*\x001b'º½uv~\x000cýüïA\x001fOÎÍõÛX>ëá¿=\]ÜJþ¼©]¿±:Âèà«3u)ð<ÛA\x0002*9åp}ÄÄYóÄO
wA
j³|ÀIz\x0011]^\x001dW¡ã\x0014V´0@\x0016vÑc%SâÙ ¨ák\x0018°KZÓ
º2Vik#ìØ8\x0019\x0000Z+áÚÒÄ£¦\x0004dÐ´Ì¬-ú÷ÕëÚ.¹G\x0014´¸÷t;Ö=\x0013Ö÷\x0018­©C=\x0004[Ê+J\x0018°A	g\x0003\x0016wH\¥pÒÞ\x0002\x000eZ	ê\x0001¶D\x000e6Î÷±«±\x0012Ô\x0003h	ê¹
z\x001c\x0017\x0000èHM-U!§Î9:Ú©
a=zÂZYÅ\x001e»ðXÕËV;éÈ)Mk7Àv/öha\x0000¶X\x0018Ì·\x0005\x0016pÙ\x0013{	¶×â&ð\x0011\x0003
\.\x000f\x0016ÓÁÅ%]zbb\x0018VÞ)û·\x000fB'\x0003JÝJ!\x001f\x0013K L)êÓíéóë·Á+Ü	3\x0002¯\Í1 ð RÍäØ\x0015\x0012Y\x0004w\x0016VnÁª+Ü~êÔÂ®;!o|zÞß]¾ÿõ®Ýø¾õeÆ)Ñ)G\x001ctxG-(\x001cïº
öhOÐ¾ß`vWÇ\x0013ßÔÜU\x0001m¬þèOâÿxÿù7oAü\ñ~¾»¿¿<Mño¶2!í¡@2Þ±\x0010º-ÌÆ7´é<\x000bW¬\x000bIÙ\x0000\x001c·Y½´vR÷PÝBßm\x0001\x001fÙËa\x0005?^[\x0001¯u\x0001ç\x0010¿<Lô{U\x0015\x0001å[G{ÓyGF\x001d¿ ó\x0016±G ô"û1©\x00192nT¤#Ò/tôQË\x0003º{ù;zô@4ôñÔ\x0003º\x0007±'\x0019ìLèÁ\x000cèV%ä#mq³½¦B½\x0005Ýy»ÉXV	\x001f\x0006÷ø\x0010uD9ú\x0014ÆfSvñÓ¹»¾Ð¡íÝíÉº¨è_Åç9\x0004àÈ\x0016aIÎsÞ6>ªF«mvÃx¡Ò(ü.">ôiy«¸l~!Oã^1£dïrU\x0017	\x000e\x0011YG\x000cÁÅ'ãÁÜ`!xnnÀÀ³ËºääZg;ß¤+s®«\x001fnÞÏs\x0002¿Q[æª6×\x0017\x001fí¢\x0014l/4î\x001fRNÏÂã®£ºì2j\x001aMÔ¥%ë@t\x000e->âìPúð\x0014þð\x0002ª£\x0000\T\x000e\x0007j\x0010¼8ø\x000f9«Ò`\x001e\x0004ÅÆßT\x001c\x0005à¢q¸\x0001]²ó<0µ¥^\x0016ðâ\x0006'69?Ç_nQ'\^<¼øÃåý\x001f×Xq¾ÑÛÎÖÀ
I<Eié$,Î@³*Í}êÃãÌh#wI±^\x0006gI#¼¬ÞÕ¬MÍ¤èËs\x001f\x000f8ù<\x000e>\x000f\x000f«[ºm\x0019½´,k2\x0003zìèãá\x0004tñzJÈ\x0010­qÜèÎ±Í!\x0006^ó|~®MÝ½ûõåZâ¿ÞîhV¸¾¾µ\x001fU\x0017p5ªøËª§-=v­s¬ùw-\x000f²B6\x0019*\x0010xvQQ\x0004gT²½º\x00168\x0007hpkMU!h«Ø¸ØÓOºÌ¦g\x0005Gå\x0003ØâÖòD·\x0008ab\x0013t@uº\x0010¦¼\x0012³\x0001hÙ\x0004\x001dÝVãÉ9h3ÄÍ\î
\x001b\x0002+Lõ\x0007"©j0\x001fc'\x001d\x0010ò-O1	
Ñ¨j³c©HQÖ"d:âï{\x0018aû@á\x0011ÇR¡n"\x0016ÅbÎàY§UWÝZ\x0002Àa3îïÍåSà1\x000eà~e^¡\x0002íd~jXyÌÃÊÓà¯Ônï§ÍpÄ=&v#©0Qo %3Ù®Å(\x0000\x001cb\x0014VÕªpófAõKÚT\x0004æ8×Ô_?þô\x0016ò\x0003\x0013ðÝç\x0015^o
kÆ3öÀñÂ\x0011\x0005iO3òÔ&øèmò\x001a5\x0019W;C\x001c7\x0007Ý7Ç¼«ú»Í<KaGÀXäÈsÚå0D-IáL»|\x0019\x001fîâ6¿ÿ´»{¸=\x0001nÙ\x001dÄÃæíRÞÐ\x0014½8\x0010ù\x001f³ºa#\Æ\x001bÜÔüüòøÚ~ö$ýÏ\x0017é²¥\x0016Å±ýþv÷ùt¶åy¶h\x000bqÝÒÁ#C¼9lý\x0013lJm¸ãß«Iõw)5#pQý[þäô[v2~w\x000eÊ\x0006äBV¸9¦H\x0004\* \x000bÏ¹TM\x0004¡Zu«r*Sue¢ôgoí¯_?ìdwý~¦ÅúÖ­MªhÌ\x0007ØYú\x000fà¾µ\x0006G-\x001bÚH%O
]F­O:ô\x0003¶\x000fðåÒö}ªÍ>¼ÍÔ¶ÓÞ\x0002:ìmJb·&&àR÷|\x0011«À{¹¼\x000bý\x000eà.ÀÒ\x001dZ®tt²~ÖéÜdnâÈºíÏìùù·O+®í¿ß<ìÞH30»(¾\x000e1\x001d\[rÐ«\x0015¥\Ñ¥irÃTåq» X/çÃþÆ6\x00123ÁÚ½\¤{wé»[É¨ó\x0001;\x000bvuÐ\x0018\x001c9ýe7$Ó ½#ù\x0000\x000c>ºä\x0000^\x0016po°þ#òwÀ`LßF\x0007
àdôÈ\x0005¼HÚ»"%Jh´\x001d\x0012é,Ï\x0015g_ßµ_Bû\x000b\x001dÍ/l\x000cÞ_ÐÇUò\x0013*×d$\x0005Î\x0013GÝª·Úbpf*Qj²jA\x0017©GÝXýÑ/íòß>}þíþåØöýÃÅíÕÅÄù­Å~FwáÕÖØ²/=\x000b±±\x0010@¡{ÌøÖã2ÚÌMNc¹îËd\x000eQ\x000b×PÜfç±\x0019
\x001bJò\x0002\x0018ãÖêp\x0008\x0014º\x0016$®ñ\x001e\x0001.4xqs³¸)\x0006¤S÷Lû¯ýÐjæSsÿáîÍÏ?½Ô\x001c\x0017ow\x000f§+eö\x000e¬®[mlö\x0011G5tÃXÛ[múê¦ñQéjÆ¾ÔÌl,þè¯¤?ÅK\x0008Y÷\x0001÷/þxCÎÖ=ïB£²ý\x001d-íT÷ØfUGÑØÚû[=êþM(¡Wñ>õØ4'EYnlÆ%á3ÚXýÑ/v$§\x000f×ïÕ­ø¼ëÑ\x0019q%¤J,û¸°×\x0018\x000bL¬ K%Ô\x0016\x0013zò\x001dã\x000et9ñ\x000eD)bßXýÑ/và_ýâô\x000eÜÎÃ¿1³ë¢âÈc;ñÀ3RÜ~êÖþ1t¥Cf7²ï\x0012j¶â"{Z¼\x0007®\x000e¦\x001dÒ©W\x0017Êðá­Åzª\x0001pq­*Îr7®YIu\x0004_iGûüõú·¯¸±¤ÚþûíÇSåT\Uu\x0003óYÄÐ\x000e¾Ä¦~r\x0003%zQ«BZrg¤×Ðw\x000fÌE\x00140ÒÏ.ªúòh[L;\x0006\x0010 [A4Ð\x0017§\x000bKÝP³JZ´UªLÇ\x0012ÐE)g\x000e$@·ªâÀ8M,IàsbîË»¯ö½
Ü½øîæîîT\x0001I_«â<ñ5C
~åt\x0010\x001eµ&=\x001a»Zhc\x0011\x001b\x001c\x0004uÎPc©3}©êá¡?wn
7ª\x0005@_ÔBM¤sèûbÔX\x001f\x001fWÎ¯¯¤æ´kùÍ½ùYé{¶VÇT|£j0A×9_\x000eF(S¬C|¦ð$ãç\x0010q¶iT
]NÍæ\x0011Õ°±ú£_>í@øíÜÿùâÅ\x0017\x000f'
JºêUa	±,Ô9y¨²võ¤ÄËß(ùIkvñ´\x0017qÑ«+?úÉÔ¿^¯9ó\x000bp2ÞÌ¬¯_QRh¥z(Ë/É´\x0010èSË¼¦Aø]JíÔÏ¾¾ø£ß=?*_¿¸úQ?*iy -8\x0015©])ÊÞerq·D~Èi·À\x0012ióã6Çoí@\x0018óÉ]P­K{É'o­þèO[à.~þz·{9\x0014F´23Ý\çmBÔ\x0004Ùüâ÷<Õg\x0014æü^ÔªKé4Ñ\x0013© \x000b© YC^\x0011FÚÚ\x0017pîÁÍuÝÞÊ®\x0005\x001cË®mÄFú=l£öt¹\x0015]\x0013ù1½b*»^ÐUÙµbÌ).\x0017EjÃÉê9Ì9¯V]\x0003¸@\x0014 äS8'íF¬åuS`©eµê\x001aÐ¡ê´\x00184\x001c²á¦Ê¢²ÔhéÜ}"^À\x0010IÓ\x0016Hì\x0006:0ªñ8btJncÛçnAÇnò\x0019¼\x001cÆ\x001au\x001cFM$Íü¦s8òa÷áþæ7õ\x001c¾þë½á\x0002\x0013Å]h?tE;Lª!mÆÑY9òÙVúäÚxÊ\x0013u15'K8\x001d7VôË§
¸º6éò3>/ÚPÃ\x0013ÙàÕd\x001dîöi1FËèàFN6>æ[\x0018Zyñïót\x0001\x001dý¾4Í»\x0014V¹\x0015¿ê\x000e¡×ZI\x0001\x001a	â\x0002J%$Ý\x0011gp&|vv­í\x001e°!:Ð\x0001NÎzx£ýòl×(â\x0000[SÄA\x000b"+P\x001d²Ð\x001c\x001bïø/\x0003l¤s*­æòzâ\x0003)ºÒL
Ð@CÅæÀµ\x001f5÷5íäPg\x001añ×¨ \x0001\x001b(âxä\x0013Dp}\x0015ÔNj&
\x001e~¹ÖM*ØH\x0012Ç\x0013p!¶åFÂ2«Ë)Óévûx#\x001bsÃ9	Eõ6\x001a:ÎÞÈµrJ\x0000Gî\x0007Û2ñ\x0007ð\x0012\x0007.Á<òýÕ5\x001a7ÀCX
r?ð$2·#ó\x0017q­T\x0013À5Q!èÛh\x0007Æ2Í#dyá¬|\x0010l\x0018ùÀ4\x001eXÖ»\x0001øpëkX\x001dù\x0000àÐù>(Z²
¢jª7:iUMïª\x001f
\x0018\x0000ö`ÚN¤$³\x0011éÈL*lC'v;\x0000öà=Åò"\x0016¯	Ø×\\x001e¥¶Jê©¼\x0008À¡nÒ\x0006¤sI÷¨
¨\x0019«måESu\x0011Cs=½f\x0007fÎ\x0017\x0015\x0001­#'5Í°Û>Nw×K«\x001eÓ^k*Äô\x0015¢×È­\x0011ó\x0001¸hDf\x0013özæfªz=iªê\x001bGÙ4ú\x0002À¡Ä<9äwàÎ±¡P{HædL´\x0002\x000e´\x000c\x000e\x0017\x0003\x0004Õjp}ÎC+1æj\x00008Ô¯ój\x0007g_©ýôúÅ¯©uGN
\x00174é
^ºCØ¨N\x000b\x001f°Û`g\x0019°±4\x001e\x0017\x001dÕ@
\x0002NZÜ)­\x0015\x0002rP«PÀS\x001d8Tô÷¶Âi\x0006Ã+\x000cP8&\x001fÆ­\x001cÈ:rã¦i\x0000vï¸,<ªá=\x001b¤ôÂ²¸æ\x0000\x001cÊsÂ\x0013N*\x000c³¡ÞrÓ²ÊS\x001b4
u\x0000p`40\x0001­ìuèÝ\x001a=\x0003y\x0001X«Lþ\x001cc·@Á\x001aõL~¯Sà.h¢¶iã(
\x0003\x0010¬fÒ*E±Hè\x0007ÎÙÞ»\x001c¶ïf\x0000ºP6³°bWD\x000fzÄõM*aû\x0007Mí\x0002W(Ó\x000e\x0014u7\x001ewt\x0014V\x0006+l4\x001cdRZ\x0005UT\x0016â0\x0016¬\x0017\x000bMdä­õ\x0015\NU`ÁA¥F2QA\x00024\x001aB\x001ezèºÒæx^ÑV\x0013\x000f$@#a³Ó>a\x0018ÁÜ f}÷¬¶\x000fx\x0000{éÈ£ÉÀë=>>M(qûG4È\x0003ß%¦=U\x0002·Nïe¶lÇí\x0003\x001e±\M\x001f\x0014oõÐ®bt.¸æF62Õo\x00008XûNYû\²¦úr®v8
|ûù\x0011lOl)Ë¯ÖJªïm/Û73\x0006\x0005
Çª]Àõ\x001ba[çaÜ¾\x0011\e&aÓÆ¡²É\x000fÔB±Ê:n_ (\x0017ÈT¯WÞ³Ë²òÑ°ü8n_¡(W\VUÚ5KÉ6\x000cfm\x001b9\x0011·¯P¬jå\x0005ç\x0018\x0016MËNÒÃo_!Ikff è\x0004Ùq¡^y)á{ª\x0013\x0003p\x0018dHº\x0016A\x0002\x0013<ª}vpß\{$Òö)OpÊÉÔ4 ¶\ÒTZYÇ\x0010r£OÛ§<Á)·EùWÞ´~mNIÓçvÊÓö)OXRêÑ¨ÞjÖË\4»iãÉvÛ^§\x0003¯¹ô¢XY<M$)ß­ª\x0006[\x001e2ÖÐ·m}§(¾#zúÜ\x0003\x0017ôû¦9eéÝn.Ð¶AáÀ `\x000eÉ\x0002A¸êôjôì\x0012:óyØL@>ÐÐ5\x0007[\x000e·³TgYa\x0019Ì\x000fwW¿A×ú\x000f\x0017/¾ÛÝÝÝ²¤¢ç¦¥X\x000fµ1{T¥t(¶(âs\x0008ª·Ë¨\x0005ÍeÊÒúâ~÷$ü×Ý/Åíîú-wÄ¶B)øªæ÷øÔl}n{ã\x000b@ÎW§e{ê<æÄ{|NÂj=(RTY\x0015/Hbû\x0003\x001dGúliô>4«`\x001a0¶@/Ú²r©\x000c*I.ëzÈàº¸\x001ad¥3ÍÿZ Óß
=\x001eË\x0005:\x000b4©Ê\x0002\x0002aÂ\x0000ÌÓy\x001d\x0015i%V\x000c=Ú\x0003\x000bt\x0011Y³ç,lÌÇÅ\x0010\x001a2è÷Ó£§É\\x0007è
ÙERÁIOÙ\x0019\x0015l
\)¦ \x000f¹ËQ\x0005ï±\x0010àUv>ñt³)²6ãÅ¨}4âÆés\x001eX´èå1 ä \x0017\x0014ÍAq\x000f{rgVToM\x0001{\x0015ðË««ÝûÖ~óúâîîdTÛ^Ï¤¿aJÌF£\x0018¨~áQÛ(¶\x0018á'ÃãDÕ*y`\x000cBU\x0011;\x000e8\x000eY×ÆÜÂRvêÑX°a\x0008\x0002)ø\x0008Ø.êÄ\x0008=\x001f°Ývèé.\x001d \x000b@[p©­w*a\ò\x0003réÐ£e½@×¿\x000bz>úá@\x0003K¯Qçh ÿ÷áýõ©\x0012ê%©ûa]\x000e%w\x000b¶Ñ¾>.q:æ\x0019P4Ø:ï®­¼\x0005UÒéSRJß8Ó²ún¥ÎxJ@ÏïLª²c»¥@åþËÎã,rÂU1Ï9~ñæýuhvÐö¶=þþöòÓ§S\x0011]ñL\x001f´\x001c4nùTQ¡ðÄ¾G­ÜÜà	2\x000fç$¨ö@ls}íG¿»=(³ÆéØ\x0018Nþ\x0016ìis;mØÿ¶ûôéâÅîá\x000bIçáÓ©jÞfYäøØáÉõ97¢þ\x0019¹ò`Gíð5¬=(SVùDÅwWrÊÌ\x001dqv¨]óô_Tm¨í´ðSRy\x0016³lpp4!AAg\x001b\x0014-¦¡g»aO*ç-Æ\x00193	Aq.L¾q·Tª¼Ð>Rg"ÿY «@óø¿,ÐÙ¨ä¦Ê²\x0008<\x0014¡\x0007LÊl\x000f
Ue®\x0006tKôj²´YõÎRö#ä&»ï-v\x001f\x000fÁ\x000ep\x0006­2\x000cèøª\x0016×°§;§£0RUÊ!\x0011¢ÊÊA\x001f¨ýäÐ
Ì\x001cåc¢àé¹bêµk;TÍßv×ï¯§ª NÑBü/U\x001bk·LÚÕl¨L7¸Õù>ñ}\x001aW\x000cØXûÑï^ó¾µ¦Dïû³ÉÉSP\x0019)ì,ÓÅN~µñÄ?õSh§T\x0005ù?í\x001aH¢"që»$#ÏÄ\x0004v:îûR]}ôÝ-øl§LÅ-]ea\x0011e\x0019	
ùrX¦|­\x000bÖ+@ö\x001b¼ìî]âÅ÷;v·nO4y×\x000f­þþèDaT(Ë)ì:>*öF\x0003á|×HdMÛI$\x000b\x0014 lÉÓ0\x0018}¼£w1­ké=6hiæñãOjº*\x0016\x0011\x001fU\x00003²«Ó¡'-½`æ\x0012"Ir\x0017Nbõ\x001f[¢ã±ÁÓ!ê¦½âÓâstqÿâÇûËû\x0017¹¸=SäóÚcµmÌÍ¡G7J)\x0003Ù\x000b¾=:O­+¦&ÔsXk	XTEa²Éå\x0008ySÛ\x001f\x001duÊÄöºKk&³ªC[)\x0017-\x001ca\x0017Í·¸\x0014B;M5iyÒÆü\x0012û¢_bÞÙ\x0017?ì\x001e>ÞÈ!2Þe|JÉyys\x000càíZ\x000eÛ¥Ç´7ÓfÙö\x0014K\x0008&33¯µ\x0017]®ëUe\x001dwêÌ¼+Ö\x0001\x001cÆ4i\x0006aGË5*\x001bîUm\x001dÃ¯´¿îei+/}c¼y8Ñ&G_\x0014Ë'm\x0018\x000fáÂÄMä®K\x0019°\x001fÕ-âY+Üà+O@»¾õð\x0004Ð_\x000e\x0019¸L\x0010¹yæ×Ýnêt|\x000eÐQ «\x0001Ï%Å¬ç4Å K¨<\x0019\x0011m²ö\x001cgßC\x000boWÒÔi±\x0014Up\x0013+M¯ºÏ÷ãì{h¡íò¤Á¤b(0\x000cãcï
\x0011÷"æ\x0015ÍÑ£\x00034v©G½|\x0000#Öµªâ©À	\x0015\x0016:ðû§ê¤\x0001<nöÆÓÎEKTÙÙ\x0004\x0003j}¤ÇêQ96\x0003x³J\x000bÍr¨¢ÒxíÙÂÚ\x001d\x0012&´ïú»[\x001aÞÎò\x0000;CÊ°\x0015÷RÃ®Lç¤íë^ª6w§æú!	\x001a\x0015ìðäE\x001f²1s[ÜÛR£§zjmf§b¢sUs."XLlYøÃÚ½ÓÞãP¶éy [s\f}¶Ç^Î\x000eÉ%Bg+\x0019\x001bjþ0ËTç²jÚ\x0013HÏ
m\x0004;\x0004`aN5«¡0®T=æ ìÇ2Oå!\x0007h)\x000e%ÚVÖ·¤àTá0-[\x0019â¾ûªgCü°lyÄ#Û\x0008R³ª¯ØùH\x000bYé4ÃÅxsÔ:Â¡ÿÿ\x001e.¯¸×}ÿrz­Úmõ»^øöJ}h\x000c¹\x0002=yÌd*È?§E·Èõ\x0012#ÜZû±Ï^S<\x0019jZçÇËó\x0015Ð\x0001W^½ov_oA¾¡\x0004Ç#Gfó³\x0004¶rq[F(ËÅÝXûÑï^sD5ÉFsDOé¤¸ª¦b¦\x001aüÁ÷L´Blc\x000bÏÆ}\x0006ï¹3N&1µ¤¼çÌ6¬½t\x000bK¾Ú©`!³s´|Ü÷Ù¡å9\x000fÞ´õ\x001eGHâÎÖR\x0015´/i-\x000eÜº,\x000eéÖÝýÃí\x0005§k8\x000eùG\x0012ßîòúd\x0012äZ\x000e3|Ò!-GÖ¯wÊ¶\x0007þú¹©Ã\x001cEß¼_\x001bk?úÝ+7Ìi³ê»\x000f»^üùæáT\x001cÉä)éIDÙ ^VF³$Yò¨&ÕüÃdRZ%¢°\x000fl¬ýèw¯¼.\x0005.B\x0017~Þÿ´»Ú]ÞÛ&\x000e£]K9L)$öØZ|ÔhÌÆK3µô¼ZÐS
Â7Ö~ô»W\x0014Ñ}Èó´å\x001fÙª!¤VýÂ§ÀçGúËÙDÔA\x0002\x001b%Inâù8'Iµ\x0017\x0001H,éc\x00052un\x000bùj§øÚù¯öÇfVr{hQrañP\x0014ÃÑrUs=¦y
+½V{0çK;¶t%F\x0014%--ìÐaG?(ªP\x001fÁV7õ\x0010\x001d°¥(òB¥MÎq'*óßèe¼jyÆÙå}}{y²ZeÏkª£®\x0014¿0ØC\x0003Ýx[\x0003³ª+\x000fh©-*°µ\x001fýî5ó³®)\x0005\x001e­x*ã$¨ùGÑ,ò§\x0007IId ªá\x0010ù30NìÔ§CFb3ÿ¥KgkíG¿{Eþ\x0019åÿþÇþ3-î=þ@_~"ºíª\x0007aØ`d<!y\x0000R­\x0011«ësÎÚ\x0003°³ïKjÏ¢´2hpÌB¥OQt)'©ÿ>\x001bkêÙ9@CÇNñ8ë,V\x0006"ï¢Új¼u+óh_»\x0008¾\x001d×üÓÃù\x0015}ùn\x0016;*\x0005#\x001d»°v[²£\x0004$¹¥ä9XSô9É¨=Z2þ`}éG¿zåa©`ì ÑùË¥uæÚ¡J¹\æîÃE90kôs(´³cMj¹W©Ë.¶rÃÚéK°É¾Z\x0015,r\x0019G'cs\x000b8äï9
)\x0015I4\x0006{>\x001e\x0012Cq+fKz`Ò{Rü¾>ß¨\x0016Ò\x001f\x001aÐ\x000e-N<\x0014&m\x0012ck-}òÛ5µ¬ Ù&EV\x001bk?öÙó\x0017Õ¨äIß·íëÓÔ5zÎº³q	×ÒùIÐ3\||Ü­ª©¹¥Äÿ+à?£?\x000b_-=OQ\x0011:\x001bzmä´±\x000b6áDm½"\x0004·Æëp$]ãfëO\x001b{lt\x001bä¹Iñoà¼\x001ajeìåÐH\x001f^¶uÂ4và\x0013j®ñ¡i;BX/Ô\x0018\'¶>\x000bj$®ââk ®*v ®
úM¤KÑÛYÇ*=¶\x0003ê
nòE©aÒm.Y·U\x0017²bÇ¢#·o\x001f^üøpyª §\x001fH\x000cÉ\x000b_·!\x001f\x001a&\x0001;_Zú©\x0015²ÍB¶Íã\x001füÎÚ~÷ü½ÿ_ÿ×? \x0016\x001c\x001aEÙCötY\x001aNµÐ7W¸.&<jÃY4éo³xHTÅSR\x0001ZÂ½èÈæ\x0010¼&ÍµóÙMÓ¼\x0016héÝÌÙAæ¸d.Ç\x0006K¦(QØ¾´ªi<û-ý\x0001Gk\x0003ã5'©ÑR,\x0011[2\x001bòÔ\x001ep@ö\x0000ÞL¨\x000eå©\x001aY75$òµZý\4Ø¡Y ÎI§Ï\x0015hÝÕÀó\x0006@¦1Ò\x000b¶e{ÒÄ­\x0007E-[QDnnØ³G¸Çö lE\x000cÍS\x000eÔh<W"W&w´ñMä{lgá\x0014lJ,Ka[Í\x001bKnÕv\x0013\x0005ß\x0001\x001bÆ1´é\x000e\x0001ÎvR\x0003êÁäRµrÙ\x0004G¸ùÈÙ«@¾\x0004¯KF[²ô©f¬ßáùfî\x0019t6Ìí$«Æ£±\§­¥\x001fýìµ=[{°Ìhûëÿ>Ù¶UMe¤%!ÁsÄ\x001e1¤äü3pæ\x0006`ÙÙ0¢m}éG?{m/ÒÖ^üñæö¯ÿÿý	ç¨¢Ãè\XúL¸_\x0015Ç\x0005ÏÁìø|h\x001fzmôl¬ýØg¯mCÞÚ}mäw7÷»Ó\x000c-á\x0012ª'Âò\x0010ÙC48$\x000b³pu©©ð'ßpdÆ[!\x001b[k?úÝk{Q6÷âÔÃòZ¯\x0015\x0010^¤% Mï®Eö\x0010ÇýÏàåÑF´®\x0007\x001c·¾ö£ß½R0k\x001bqbò\x0019\x001bU-´\x0011bØæyB±{\x000eöDLuNß~¦gc¥T\x001b'Á²v«\x0006Ñ{¡£èáîöú)ÇÉXlæ	éo#HÅ©ßÁ9ÝuëÉVXÛ^»²½\x000f'ÎäW\x000bávÅ\x000c+¾ÞvüMù\x0019\x0014KN\x0003Hþ\x0006Æ3m,ýèg¯Éß­Êÿ0ãº»Þ'züi`ù§¢Y\x001e©ô®ýçØ©µz'æ!×´\x0015½ÂNr<\x001bk?úÝk[1{%w¼\x0017Ø]¿¿8Õ¬2¦\x0003P¹¾ê\x000f\x0012è\x000e\x000b§t¬Ì\x0001ÿ\x001cÑ\x0013Å9íAo¥\¢\x001e%Ä\x000c\x001em¬<»\x0018û÷¢ñ:m\\\x00110[Ù{léßãî
ñÄcepØYy´ÞÑw´åÆº]u{l í».ØA33KÒ¹UiÝfÿ\x0007ÌUNºÊä\x001a+ÀA'I1_=\x0007;e¢Ë<·½\x001e
*¯.ýèW¯53
ó|Á`?¡#Û\x0006\x000ck¬óbqÑÒä4Q{üþæÃ#ô)ªKT£¯8öÄ9ì\x001a)&
\x001fÝÈPm\x0019<:p\x0011:"æÍ \x0014¬¼Í
ÕÈ¡
´*s=Ú\x001e\x0019êÑ<¸Â½*££\x00154t]Ñú\x001ecQ\x000b·Ú\x0005y\x0019'K?ZMTjõõ`Þæâ\x000bÌVáÆçG\x001e\x0011·~fÜ\x001c2ö-\x0012å`
æRðïÈjW}Mâê»]lÌ¥sdw
3gª
@î¼)j\x0000OSI]Jì=ÃÆ9`Kâ.1D1y\x0010¦p\x001f¢Ùî[=9qíätb/'ÊSq	§:Ä!-\x0015°Ü#åÈ-w
ãÇ;:ÉóQ£\x0004÷â[à¬?ûv¯â¡Þ-ÍíþÜ_§²$6æ_¶3/ç\x0001\x001b\x001bÕRË\x0016\x001drd[ì´\x0003ÓaHÅØ\x00156Á-½{e/ä\x00036·²#¡õz¼M(¦c¯°	vl©­Ì ÁD[s#ê³àó FUjgjÎ\x0003¶\x0010ÎUfp³R{ûª`ëöl\x001bÉJnØ+|\x001d[êÌ+0/\x000b\x000cYâ3\x001cô\x0019îCfÚÏ=´Ð~ÆFÊ$âæNç¤Dª~>\¯\x001eª+Z cÝaRB{wi\x0010´z?B\x001fXH\x0006û\x0016¶\x0017ì¨f¶ñDÊâöÅ
Ï^ôeçNû\x0003¶¤x-·Õ\x0002¶S\x0003³\x001cw\x001a\x000f)^ÓµîÆ\x00112`¿\x0013#Ø\x0010Tõx%£]Û\x0001®\x0019ñn\x000esÙ01¹\x0004ùEÂ®H\x0015O6&ás
¤\x0013ôñáúòÍå§Ý\x0015«µE	ÿ\x0014\x001béÞa´kÓ´É°"\x00145»\x0000¶Å9¾kKOo×:Â\x0011&ýÅyÅ6ÝçÓÍ§\x0007úoü[ÖêUëøÛ­V®´¾\x0010ôçýúá:<¼\x0001;\x001e?ïÞ½»¼Þ­\x0014F¤µ\x0007ÇýÎC6,Â£Q\x000e\x000f\x000e9C^2>°¥nU(îðÙÿHGÃ\x0015Gcè?:C6K\x0007\x0012Ï­3âiÐúé"¡%\x001b\x0018m
úöÊ<»E\x0007\x0001w@öÍ¼$ñ$XEõKà¡¥t\x0007\x001fUG\x0001ß:ó A\¹â2#ìB\x001f\x001a/\x0014örç½µN:O=ç´T«;ië ÀMjÝÃø\x0016\x0005\x0005¼@Þ3Ë\x000fRB»ÈH­Gñ\x000c×þìM~È?PþÝ¿ßÐÍ»\©½ý¦S\x001f\x001ebV²[xfãR¸åÔ;&Ô\x000fåO=Zó©÷ã©ï:SC¹Øj\x0010\x000e6Ï	c5H;pã.~û~Ü\x001fO=/§Þlòjo+YupæIª¸·ÐvÕ^î,¾ûÙ{µ»ßÝÜ¾]Íð|ÓîÇYXR¬Ñ\x001ct­d	-ÔÖ>Ò\x0007
\x0005 O¶»C-ÀAPº\x001aÀr0l)æëëÇÆ\x0011_-vU¶oç'{`äBpáär\x0006[\x0005÷Â©\x0008î\x001dÀçÛûéË»óLø7·ï/Z\x000bói¶ØÑ¡Eó\x0017vè^°\x0007\x0001-[Ì!(ú\x0011¶Ø®
óA\x000e¢:S\x0003Ç¶ôÓçKV¹5Hpuyñðâ\x000f÷m\x0000óÛË»µ,Ã·Y\x0010.+û36=)\x001d×/ÜÔôòxóø\x0016ÄúVL÷¡	ìL
ÛZþÑO¶âö*Ý]F¥ïþ¼û¼{8¡Æ³z®@á<ãa\x000fç®¬åEæÃc¿f«;Fc¥ËI\x0017Ü¬/þègOòÏ_¼\x000f¿j}Ôù\x0019OeCW5J¯U¹ô\x001bx\x001e+fbdOC÷R=üÝøÞw9©!¹[Ë?úéÓ\x000e\|¼¾ÉÃðÝÝíÇ»»Ó½	¡ª=ú\x001b)\x001cÞ\x0004Ç¥³^^6Ï½\x0013ÏB\x0011Ùñ\x001ataé\x0012þ­å\x001fýôi\x001bv_Êõ/Úðú°{øx*³Ëz§lûZ6ëÉá^b>\x001624}lW²ä\x0015Wr\x0018|w\x0010Ó\x001a|gx\x001fÖÏÜ½ÐÖÆ67\x000f\x0004ûtÇÑ¤\x0003l1é¸ÍË\x001d«¾óâ-Ø´ûhÎ:SÛhá4>a\x0002.rlr)Ï"ÁÛc@iÓBP>p­±
Õ\x001bM\x0015\x0000\x0017SÅ1ºt\x001føH¾2U¼u*bkjSK,¡\x0002w\x0002Î\x0001:\x0007à±\x0015\x0002\x0001¸ÑÇ-õq£\x0004à\x001eÄâÔÊ«mN\x001eåªôZåÉâãúzqÿ%¼]1²~¸x»Ißèªª\x0001ê\x001cZÊi\\x001bw\x001f rG¸U±
 nÕ¸Å]Vgj:(­ßK$×ïT$98Õ\x001aFßÞ>ã¸Å\x0000î_¢pÄ\x000f\x000eÖ8ÅEÎs\x0016l^\x0019á©À\x0000Í7\x0005\x0010gËð6Ü}¸ÀwñÅw·7'²JÏ\x0016·Õù¸<c@à~¾þ9ôã¹é2:S3Í·ôÓg\x0017éã\x0007s®Ã?=ÜíN\x001aðªm²°N+ÚßGÛ÷*È\x0006ÿêYX$i¼\x0000]PgjºçÆê~ø´\x0003õáîò·Wôç_v·\x0017×'³Ï³­N-ÚXÓö\x001d!$ÍJ\x001cò°-ðúôÛàÆmèÒjöù²
[Ë?úéÓ>üôÁ]ì¾¾TöùëÝÕåç\x0013\x001açAO\x0006®.D»\gº¿\x000bq,]çØÿøô{àG+¨Kªi#ûòwôÓ§=xç¿º{MÐ¼J£óMÒOVM	.Lót¨bò)d0"<\x0017¨¤g¡ühàv\x00195é/\x0006îÖò~ú$ý×¦ú³cÔÊ;þéòDw3øÊs5Õå"²P~x²«ý@
ñdjhLû¨\x0012Ê/¯ýèg¯ìÕT¦Ìëû\x000b\x000e\x001cÌ"òª¶³¤6cbo-æ\x0008¡>ö±^}\x0006¦´\x001f\x001fs\x0012U»\x0004bzÒû`\x0010Ùl^¥_®Jã
\x000fæÏ\x0018{X\x0013 g¥AÈ~<ø¬ªJê¥~>6{èåØ8æT_b{äxZ\x0015\åÞRTùèVMÎ/ÇÀÒÇOqàv\x0015\x0016~Ûº\x0013ÙsÅx\x0015gI-\x0000¼ÏÌ(>X[úÓ_á8ïEÎÍYöbkñG?|í\x000eC3
ï
Ê4¾ý\x001as¦\Ù4Þ.×ØD\x0018If)Gî7Á[ï×ªrç\x000bÑÝF\x000c	^|ô`Ì\x0019¹¥\x000fW\x0010B«¬\x001a]¦\x0005Y\x001c&#öI´Ü@±Ú\x001aà\x0000ÞH¾Â[°âb3ûD\x0004i[5\x0008óI\x0005|jÌcäyA<³-ÒIE¢àêPÈ­c\x000c3WTeG\x0016UÉA\x0012üð´5¾£ZÆ¦\x0015\x000b®hÊ\x000e,Ò\x001a ´äé\x0016i\x0000ÎºÒÆF¹¢(;²(Jëa"\7ò\x0013\x000bktº;´\x0010Þ\x0018×\\x0000[+\x0015´dVÁE-Yï\x001f½#mfÉ\x0016r\x0015d\x0007§¼d7 ©&}æ¢ë¬\x0018\x001bÐ\x0016ÔIËÓ¥ê8\x001dæ:¦Öy²\x0005-!ÇZôØÑª²XgíKå6\x001frë\x0008ý\x0003áZ\x0019ÿË¸	Ò\x0013îxè\x001aÛxÚ:\x001a	ô6\x0013GÂÑ°IY¿t\x0003Í±¦N:î¦\x0000ë÷/½ þ¤1Ì!Ù\x0006ì\x0000\x0015%5fôémÅ3°»â¤±ILíÙ\x0004×n&¬ÞÐØxÁ:RQÀH_ÎZjR\x0007dQ­öB2¬\,^ Î(\x00072Mmìl\x0014Õ\x0001Z\x0014\x0015\x001f?	]Zë\x0010YiV\x0013]1»l\x001dÌ®ýHðÓ\x0017(&[ÔÝ0\x001e
\x0014¹ÚL>Ù\x0019âcÇ¿×Ë\x000b&eC\x0002kÅ\x0005²ÙZüÑ\x000f_1¹\x000e\x001aì\x001d×ïnh-§*ñ\x0008ÉèÃJ]7q_´ÿ\x000c\x001fóãË­ïÁü\x0000\x0016<\x0008ò\x0000n,þè¯\\x0010õeh<Èôv¿Ý\¬P7\x0007\x0005tqáð\x000e9\x0018|â\x000eüØ®ÇzQ/Bho°gÌZVïÔKÕ»ëx\x000cz«Bß
à\x0014\x00154\x0017Ï©:Ú¬Ò|Î­û%®ß±ÛëSEèÈbRo¤Æ\x001fÏ}W6J>Ê=ö\x001b¹±½+w¬ïÁrÇ|\x001b×Xdõµ*äË\x0003r½Ó·^ÞÙÆÜ\x0003W\x00016	"<·G\x0019\x0015ù+ê![iÈwÃ|	Ù[\x001e¶òo»Û·§òYé²*K %·@~´\x0012¢Ý®ÏC®lB3&\x0018ú\x001b?úá+\x001a4êé\x0012\x001cú~±{ñýÍÛËë\x0015vÏo,Ó2ªÂV¸b<pimô}¬Úó¸bvºb$¬æ_È\x0015+Æ´ë~õÌP¼\x0008®¨\x0000,Ojj\x0004»GiÌ­Ë¡@ùHñÊ\x000fÑ[]êâÑH9\x000cÑÙÓû\íÞ*ÝZU¡\x0018«ç\x00029\x001aK z2{G!^u¨ï\x001cpR~´±ø£\x001f¾ä\x0010ûáhÃtZâûtyï\x0012µ{ïJuò-ÐB\x0010
Od}\x00166{ÃRm¶\x001bk?úÙ+Ê.\x000fæb#/8±¹Hÿ¸rü«³\x0007´tÅpDæù£}\x00156Ý\x0014ò a5e'-F$ö6+æ ìÈ\ÌØxUª\x000e
j\x001aÅÀô\x001d Å¢ð\x0019<ã¾	;£x\x000c)½\x001akApPvû øÿù\x001fÿùßOYso£J)\x0017'þ\x0018W*.\x0014í<¾Ã´îÑ§¿_SÉý9Ij(¸ßXü±ï^¹_vxmnoîþ·àç¿*\x0018\x0015Ñc]|±[8{½ËägaÍM¥Uç¶Ë\x001f\x000b«Ö\x0017ä³WÄïÍËæ\x0013ï\x0002\x001d\x00174ñ¹\x0015æ°
ÖÒÑ±\x0011-9·ÈÜÓoÃÔ\x0004tN\x0002\x001b[Ö\x0017ì»}°²ºíÞéòÅîâZëôamLã$\x0008Ü\x001d°©6å\x001a¤\x00070ÓZéÏE·N{i¸Ãe|kç´\x000b®VýñgßÅOo ã \x0019ÍÖ!Mü×ÿùþñx\x0006]\;öø\x0019$	8x[fÊä¬
Ï?\x0007\x001bLM\x0007íÛÿqG0Ì\x0011èÉmWGð .3Ì±:àd§Õ\x0007\x0003½ôÝYzÛwÛæTømh/Ð6\x0008^iE\x0005\x0010&ì$t	
Ûtöq»	n-\x001bé.=yØQ&\x0012tìÐçVocGX\x0006a3e¸\x0016Ä2\x0018\x000e@ã(ÛàEÀyàv\x0012ðññkÿZ¸où'g6±\x0011l\x000fì]R\x0016^ÞMßf¸íâð¤÷]À\x0003RS²TÂ\x0000\x001eÒ\x001cÀSàrVJ]>v8+.Úá\x001crºÏmï§ýäæJ<XÄÊÊ-'}TR\x000b<æmè,Ð\x00012s¼w\x0019«\x0002\x00137«yuTª-sàKW\x0010m\x000eà"õ>´r[ËÙ\x000b~¶Ï¡/êGX9\x0019ÅUTµÆ#
Ï©§í\x0018ñ B³\x000bW¹ìÄÁ	-ódê\¯Àq;´îï\x000f¢\x00027)\x000e\x00071Ìý(\x0008ð\x0017¼®S§ÀÂMPØÙ¶^°\x001d@*\x0015u³îZw\x001dÎxÎ,¼}\x00103\x001eÄ £\x001eY(\x0016)\x0019è ¦ª\x0015b'(Û\x0012/ ñ\x0018{¸>OIÀ×Û\x0019=_ýº­É«\x0005ð,Cø¬\x0004ej\x0010ø°©­¼n¥X¢ÎF\x0006¯X~Æ÷s\x0010\x000bw6Îs;\x0000]&w°ÐË+\x0007g%c\x0002K9UßP×\x001f¸ÍÛo-Ü~~#¤T¼£ú$¦Y¬Û\x0014ºu t\x0017ÁCKÈ\x000b8L\x000bêK¯Êh[qYT\<w\x001d\x000eºS3eyK^{íWaS¹Ø Ê\|9(µ¨\x000ecày
|ó!²\x0001\x001e"zyf%\x0002÷AnÑ\x0007¦æ1:`Ï®+å\x001a\x000cÓeüÙ\x001f/æRûo´H³õJ[hö\x001dcôä5äDþ\K\x0013ý£¤,µÈÏx|º¤T&'±Ô¹Ò¥^ë2¬ÞÎ@8\x001e\x0001ÓL(\x001b.aT\x0006ç Ï&\x001d\x000fÖÂ£¢\x0014ð¼(ÊÄµq¨ËÂ Ë\x001bVn[
ÐÈÅ\x000bèÂÆKè±JÑ³6ïBÚ\x001ep¦Õ.M©Û R'ãAx\x0019½¶à\x0005=Ú2H½\x001b¦ã³ºËpì¸È

\x0002[_¡Ð#Pu3)¶É8~sK-u(\x0014S0¯ÌCXµYÊ£Vh\x0011:È]élRËºûg\x0008zÈ+ÐlÇ´½î\x0004ë.JM\x001azù">N)Zõòu:97½Ù\x0002.ovò6àÊM(ØÕjÃ´õ\z3\x001a2\x000b¶_ê6	\x000cÆ!u_ñÒ-Òº.\x0015£Ûmt\x000bèëÚë¨æc`²{\x0017ô*v/¹Ì\x0016¥7  9Õàô%JM·ÔmåRA¹\x001c\x00148Ï1-\x0008îµË\x00085×8^Jà\x000c¢'XyItPÑÌ\x001bî)Þ7ð2\x0004\x0002¾\x0010ïæÊ9Þe\x0010|á\x0019ò@é]\x0001J\x0006·¹9¦\Ä»î\x000c '\x0018KK7\x0006[Ø\x0008>\x0005§áKéð[»\x001a´ÃQF1Óâ³Á3CðAiuzSV\x000f#"Â/Ì\x000c,\x001bÈÌ\x0011|,XÅÅðNI\x001bò\x0019ÞOîÒ\x0002ïÅ]"s\x0019\x000en¾Ç¡\x001ed5Fg.\+	çâMø\x000cðdÓ\x0014AçqÞ(\x0012½iÆ;\x0013ðo§$O¥Hî8W¦Ö\x00110oÑ´­ôc4î\x001fâ}©+\x0006Ó·ý¯ëÛ¹Fõ¬¦Ì¶ êH¦é¾« çÀM0Ë&3EÃ«ôÈFSt+Ô»yÔ]ZÍô\x0008`\x001cXáÞ¥ç|4¥a.c³C§ä^Ø\x0005ÜÂ\x000bËÇÄÓ
ø0w¡B¯\x001d=Æ \x00071\x000el\\x001f¡½§\x001cúP
\x001e¡`MwÒÊ¦`8Ðs9
:dm%ÛCÇï¢Ón®Ýy0löìi{ô@\x001aß¢¿ÀÓ©\x0015zîÝ\x001ceÔ;¾\x0007g¦±\x000fBÏªaÐ³ÁãÌ\x0005«¯ø\x0002¯8û6à\x001b\x00072?Ò`)Á8ß]À)\x0016y@o?ZB[À}õlÄ£s\½ò£HJ=}[·¤Þ~t¸ªd®HÝ4û\x0003ª\x0019b¾æ=xE\x0018[i?:®	*¾µ©íG\x000bº
¹\x0013zm\x0005n\x0002\x001f²Wð¾½ã.»Q!\x001fàÛ\x000eðÕIÃ]ñ¡ª	B§\x001f#8ö\x0016,~kííG\x000b8Î'"t.Î+^\x0003hâ\x0001~\x000c¨\x0000|\x0016xÛ]¸\x001e\x001esfS\x0016¼I¾£§Ñ|\x0012ô\x000e&sw\x001bJ\x000cd\x0011=)OÐÓþª\x00067 GA\x000fÕ.<ª	Û¤\x0008>kôÜ¢<+a\x0013]Ô; \x0019Ü9[\x0012<Ìlð}´hÉÛÛa[S/K? óðh<%\x0005î»hªÙÒ\x0005íGh8Ú$ºÀ3ÝGÑT\x0015¼mf±·}s÷VìÂó-¨R°Á)Z*êíc[s2A>¼©o®¯×L\x0010&¥½»¾¹>Mà&»äñ\x00062eð!øD&»tjåjxhÊc MsNéìñ\x0006ti)>ã\x001cù\x0005Y&6q\x0018N\x0007æè)6Êû!g½uÝGTÀ\x0017@\x0002gÒxq­<ù0\x0003#wÊ)täÜ°NÎÿ\x0002n3«WÜ>ol\x0003\x000bxÐ¹\x0010»gH|\x0005\x001c|è\x0003L. Û\x0004n£\x0012M=`ÇÃ/èV¢¡­9É\x000b:?]`÷¹\x0011õÚ{ªe\x001c©¡Ð\x001d \x001bHXÇ½^¡\x0007\x0015â¶!µ¨P\x001c GI´\x0013b\x0005k¾*JÆGNç¡½ÑoÁ·\x001f-×;mÛÄV&\x001a~Ù\x001b¥\x0016hS[ßy	z ·Û'ú;|á¨tÂÅû lbSé7\x001aüä\x000b¼¸ãÜ2\x00198Nð®Oâ\x0012ø¤|BS]ÙÃo!À{÷2fàMEa5)xÛ|ÚÜÙö£ßÑdÇ`C\x001eCAÇ0ÚZ$pÆè\x001e-(B÷Êr%tÓ\x0017_·.lûÀC{9Á{\x0013p\x0008ÞU¯à{Ç5nÁg'ÊÆ(iÀ\x000eQô6
èÍîv9l£\x0007@'}°´\x0013:i\x001bÌìd4*JKvI;õe².\x0017øâ_\x0012Þ¹Tµ\x001a&ø¢àMÙ°\x0014\x0016x°\x0014"{±p*½
Zfõ	¿ìÙ]ýùÍ\x000e8é-üxyÝ\x0016;ÙÈîêj­åã\x001bÓ0¾èÂ \\x000e¬S9\x0019ïò¬µÏôxÌç§\x000f®\x0014	'©\x000bMäÖ`æ%²ÞXaúô:îÛà\x0011Áa2\x0019g«\x0002ë¾:
\x001e\x001bãH\x001e_-\x0001Ïâ¡LÇL\x0018AæY\x000bC|õC\x0019o\x0017	  lÏØ³Ëæ­2f=ýJoz\x001fUÛnÁ)ç8½\x0005¹ÐuSé`tå\x0004!5ÏÖ\x0016\x001a C\x0006Éd\x0015Z×Ý¨®oç¢\x0016%Ú^»µ'\x0003f~ëZ/\x0018Çñ1Ùá®´|x\x0018\x001fDA_Ê%9·æ&;¬Ý\x0018Ã¹µ8ÜÄ\x001eÚ^z¥*|Z¹×épæ¸ÐØ¶ÅB¶ÏºUgÝ¥À,£NçýýâÐLCß<6ÂyL@RÉ\x0004©Uç\x001cý±Î±Ù¹I!/èÎ@äÏ\x0004©\x0015&tC'f·v5s'è\x0018W´\x0019Ê\x0010,\x0017õ©
§à­ºKÙ´Ù-n+
:Æ\x0015ü-u(\x000b^«ÔYqýT%¸ {ÙØ\x0000ÕY¶°\x001e@
\x0016Î°¥Ð:\x0014Ò/YÐäK'YÀÉaÅÚàT²Qá\r1Æ®G{öËÃ×÷\x000f&öKåïÛ8èË¹ÿ\x001b½ZzÜðö±Í°¸µ<E\x0019r?\¥è\x001eù\x001dd	­?Lu[]fgüT¹ÉÇrJM
^G¿Q÷×qÔ\x001fÂ<î´ g(µ¦§¯pÔ@w\x0016¬ª8#ðVþ\x0014ËxÁ\x0004¼=+0 \x0013:Ó@¨:\x001f3ìZ\x000b ÉÔ\À\x000bt.e:p!=¤
ÙbF\20Òó÷ïo?Ûu{íâîn¥Wê\x001b-µè7ßçå*³ïö\x001d¦Ñ?¡ã\x001a©×¨º´tAdâÂP(h/£Ò¢©áe´3o¹\x0002²\x0010:íPÃo¼ªå
i¨¯\x0008+´å
\x0005\x0010\ë«{Q*4ªÜ!íY¹¿\x0015¶\x0007õ\x001d\x000c´î¤u³\x0006\x000eí]\x0002½\x000câæúS4]òðh¼.ÛmÙS,SÀ3Äy¸SÎ8«Ê6\x001flîþ æmd\x0014Ã"k\x000eX\x001bµy°þè¹cðÑ\x000c\x0001ð\x0002R1"4Ì¹áTtð/\x001aeU³}\x0008\x000b\x001cÂdÁ²ä\x000cõ«a?õ	ß´¹\x0017t´¹\x0011Kª6Ì+Ú8Ñ\x0015}ZLëhF-	è	¤^À>#t¯"-\µ¥¥nÚ$6;õA\x0008º\x0005«8[áÏß\x0017-vµ7ðÍ\x0003\x0003õ&kqñÀx²xÔI÷NßýözØm­eAkµ¦s¸F\x001csÅ=yKh8vr\x0001\x0005\x001d\@GgÝÀõ§MÐ%J¦èK\x001aöý£cJÐ¥¬8¹ý\x001cÀ\x0003:y\x000f\x0019Õd^{êÁ¹©þqAwPÿè\x0012×qIEÚyBwEïi\x001aíÙ	oÂ×ÉúÛ\x000fe¹=Ù»ZUÉ\x0015o¤\x000eµp`NY¤þ,â\x001f£ZèÂ:Ã)x¼"4Z½Óq{h@Î}ØàZ=½ Cm\x001ewF\x001f½î`¨ë\x0010\ï2(ãÙ\x0004p9çCÈéa
÷Ø±FÝg\x0019Oz\x0018°åd-
É\x0006\x0017cE&%\x0002OE/¼6\x0017;u\x0018-èV:R\x001bÝ	+/A\x0015ësÏ¡Z:=OMß¸Íí´N¶³ð¯\x0008è	d\x0012×¿9¾¯ÍÝ\x000c¼§6B\x001aÐSfRe\x000e\x0015½¥½gÌZ^Ð½hyÒ´Y££XU§\x0006mÇÓal	T\x001b6O
pbÙ\x0019¯©S>>ÏLvzW{½Ã\x0014ý\x0010t~X¡=«\x001d\x0012©ªÅ»&±S&@À¡ê©°u*j>\x0019\x00150®¾¨Rà[iÛ\x0014\x0004lXx0Ø#A/J
V\x001d=`^Vm]7U\x0000ÿh\x0001w\x000e+ÅÌ%ãMÒ=\x000c<h¡WlcÃY4	
Ô­¾G^µ¥Æî%IS`b\x0001BN\x0002J½ð¬t
®Ë©ÈDhé¸©\x0002\\x0014\x0015@øúêÒÿJ^»F`Ù³·á\x0005ò_?~ÚÝÝµdþëÛ¯¨á¯_¼Þ*øQt~Øi[\x000fN2{ÅÒ\x0005Ë½iÍ\x0003ÌG0\x0018·BU<éµ.¶¡\x00071Ó%Àåïv\x0014×$«ØGcËXk ZÐ±*Ñ'¹kÓ{L¡\x0016¯Åê£[}M\x0004\x001búU\x0004éyº1ÂZõt;.NnºxS"ü£\x0005Ëæ$Êm\x0008\x0002K\x0005rÍZ .w£x{Ñ\x0011\x0016Í3å\x0005?zh\x001c´¨¥Ý[¦§¤,K\x001cµc\x0005ô\°ÿ0s8VOìßöìky÷Î¿ÌJºQÿôÛitÉ\x000c\x0008jßéÌùC,1%äJ\x000fh­%î\x0019ô5ª³ièYç$;f\ÍI¼ÌùÁÏìDÌãæ
¸Ô,F\x001eî ÉÀ5ßº\x00014kÿÛ7­o'­¿ [\x0003K'\x0007ÜA!DíÄê\x0006ô8º\x0011\x0005\x001d»\x0011³Ö#ËQJÕ¥ILE=²s½µ¼1\x0003|ûÑâO!\x00198ÝOR:*NÉo\x001aÀÛc/¸L£BXàsç6Xß²\x0016{x\x001e¨\x001a§ts,\x0013w7âõÙÁ? {tð\x0003ý%/U,\x001cSÑ¦R.\x0017\x0008vÄØ\x0008\x001f_Aµ3:AÏ­Jçf7)Þ·Ð:¤dL\x000bõï/,ÿÑãsn`P|¿éû\x0015i)ð`Z²\x0002°¢\x000erV\x0005>ìÀdÓ\x0014±Oõ'Ø`ý1Z\x0004]CF2¹ML\x0003|çÓO\x000b(ðà\x0002ÆRÅÐá\x0019êFÅ$
Uëz¹¨OG¾ýhO\x0001º2JL\x0015k]ÙSã´úæ\x0005ú¹e\x0012Ôæ\x000578Ìà­÷jõÕuøÉó\x0016xð¼£\x000bÂMÀ3An\x0008¨E¥ØMêýÃdyn
'CØyí
9úø4ì©]°+Ü§\x001cÅ^"xÛ»M\x0005Þ9½ôn//±¥kÚ\x0004¾4óñ\x0000o:¡%À«$¸I­
Ò)$'è\x0010\x000bQl2·]ènjT*ÊÐMo7ªl\x001fù\x0002G>\x0014Ê \x000cnI©:h8;ÌðÕÁÊ\x0005¾
Ý\x000cíj\x0011*Öp¦66z}£úëÊÝÃðÐ|\x001b\x001dt\x0011|Lº¤êÂz.|ûì/©ÞÉzjìßßÞÌ<ÃßfAÅ:ôê%{ðGø]fÀp#kµsOÍS8½Këó#ê	Ü+\x000eq¶(;'\x0019ÝïËÄ&EcÒ<.kH lÜ¥cQ°ÚÛaÁ2øTd"à\x0001À¹S:,¹F\x0012[Ï#©\x001eÝEXZËSõ5 GA\x000f\x0005âé~SµóÐ°\x001a=LÃJíÙýõîÝåÍÊ\x0001}}sy¿Âlømç39]5\x0017s\x0012WJbMµaÂ\x0013³á?ú|&WÖFûLÅ£]X-ø²äÁH:,ÉYõ:Ãk2òcçípS» ;qj\x0003\x0011 ±dÌª\x0016&/Uv8ùMÉM¯Ëîåu	Éa2É\x0011¢z£é}Ð9ôT[U¨u\x0016ô(Ô:î1DJNù+µô¨éoJnY¶4½é\x000bx7WÖrSK¾§â¼63P§ª|#\x0004j\x0017t(ª¥CéU\x00007&Uuu\x0012<w6ÒÙ\x001e\x0011tX{°	9GØ/G[0Ù.­\x000eØ\;ôö\x0004Gï"V\x0014Ò³¹ªdº¹Ò:êöÒ+,Ý¥\x0004Eyä\x0017WZ]ªv0ßv´ÎýT\x0002
ú\x001eð\x0004Ð¤<³ÒgE§Ù³³>³\x000f\x001fn®`	\x0002ùÉÝÝ ü\x0001|\x0019¬/µ.I±kä úî<?¦J³Î¯NÏV\x0013×\x0007\x000b>µÌìaùn0¬JJúËMcc\x00196Á\x000e`´y/]ËLq\x0019\x0014/HIªsß¬h'\x001fhÁ¶è\x0003Ñ©Í\x0005zÊ`S%tÜö\x001bæ÷ÐþüËå»ê$>>k£[¿1êzÐ±,1qï ¾PR­Àóé-6?u]6iµã#[ö\x0005\x000fK\x000c "A@ªdå«Nì}ë
Ú"\x0017p)ÍK)rãÚû¤SW6yíç}3Å¤\x000eè\x000eè|T-¯MÑK\x001frW¦¸Þ4UÌ\x0000:0\x0018®"\x001d\x0002åËU\x001f£:\x0013.ñt@ëu¸~ÿól°Ý½øãÅm\x001bPs\x0013mÒa,G·åÐèPb\x000eÌ²\x001cE*Ï!Å&Â..¶\x001dp¦pòMNçÃA¢»NTÍ½+¥Õ8§;\x0004Ð ïG\x0004\x001eÐÉd\x0003¢EBOÊ\x0018&Û³åÌÓD'
èË!Ú\x0010ýÑ]cðÉt\x0010p1\x001d
G"sw¶EôTÕÒÉ;j\x000eËDY¸ g¡,,ìQÙc-½+A¡[Í=Kfmåh£µ)èÅ	zIrw\x0019½bõ\x0006¡«¥{CÿØJ/QÉ\x001f~Zw×¹æz÷õ4\x000f@æ`\x0012¥sÛÉTBsnql½ªÏ@ÿOG´\x000b¬\x0015Ê\x000b!A	hÞ\x0016.ÇîïìJjù\x0014[Ðjâ\x0010táÈÅ\x0006id$tz,sDÁêæ
®
t=\x0014¹.%DtÃöIÅµ[½vÓ\x001f/?½/¾¼/9î\x0007Ð\x001c\v§X\x00183}gÒ.»ñó!ýõú³KuÍDùñáë»S½\x0000t_¼Z
¹KZ.óG(C\x000c¡kG<£®6*Ï937Ñ.¯Vé(g)\x0004$êàØßñUôíVQ>3÷T/F\x001cÏ¨ KQovLí\x000eÒáÁ.\x0018¯I]þ`éÎÌ®ÌÇ¸»Û­\x0016ôÝüòpqº¦Æl.\x0010Ù\x001eJúrò\x0015«6\x000bS5>²/ã\x001bCÛ¤Æ\x0008GW3F\x0008G&O\x001d\x000bØJX\x0004\x0011MÅÒâ'i|Ð\x0004<	{ÉlµåH'oæ\x0000nAÏ£Eþä\x0010k=\x0017rÃBô¬L,^\x000bz\x0011\x0016/ú\x001fUzÇ\x0004\x0008×\x000c\x001aM\x001få{Ãä6x\x0001pæ3¥ÓùF6h\x0002×\x0005ó[\x0016§ã\x001fÃ/7\x000f\x001fg5÷ðâÏý¯»ÛÏtxN\x0014\x000c#±YZEBâ\x0017\x0000ÉÄc;OOïËO¥Å]`gZ5°1$NqÁÑ§g§puÏ!¸	.\x001d$Þ	q\x0000\x000fºäªù,«i¥~SeG\x001eÛÑCÅ}HØu ügn÷ýEØ³ôÃÉÍ¸XÎ>X°ãHö¹°{Z§·ãæxJ\x0017§d.Ö\x0002fZæ­\x001aègmí}\x000cSÞ\x0014À-G©A%ð\°ÃÁ\x0015àJ{¢\x000b\x0003p\x0007Ú­¢\x0015gé±/J\x0001y\x0015
b\x001aÿV\x0010V'VNAG\x001b\x0011k\x0016R
y\x0017î5\x001f\x000fæ.\x001eÊÃZòîÅ»«ËUë×4Ô!¥\ÌFP\x000cþ±'l\x0018q~´¦»¼ÚÛ.Ö4\x0013²8X~´J·Ñ§+\x0006®ÀüZk\x0002\x0002.ý$L®
µsäEÕe]y\x0002Ï+4w_Ë¯÷]ûËåÕÕÅ§¿þ×îDÜRd¬\x000céSf\x000cºBCÄNY¿\x0004¹»tÍWº1ìÄXÓåÔx\x001c!T¼¾þ£ß>í¹¿}û\x001bÌGòÅ¡\x0005]M³¾y+¸#`ü\x000e[\x0011#ÏSGØ7Sîé\x001f©i¿«Ý3àß·7Ò7S°Ã¸a,ImÆâÔ
-àª\x001b\x001a)¡Úü
Üe®®\x001d\x0007pøÖk½¹ô(Xôªv×1! Gt\¡6Í¶CÞ0AI\x0016<W
æ{\x0018«»Â²C»Û¶.>^Ü\x0015ðòÄ?µ²¨&\x0006]oÓ&¾\x001cªß¢¸2¹°ºs¬,6üùñ)è\x0002;S\x0013Ò¡åa©®³Z[9¡r\x000e©W|NÍ8\x0002\x000eÍ8dã\x001dÄÝ¡Í1\x0013pÅrBb]y	Þ¾¿º}¿²Í<HïvúáöâTÝ	&«Ê_kdt\x00193Hj¦ÚØü´§ßå)CÜå¥\x001b±#ÏwV-\x001f\x001c¹àsøðFP49ó\x0000.­	ÌH$\x000cfì\x0007©:#\x0002WM\x0004,Õ96W/Þ¼1+M/¾»y8ÑCS]RÅ´Ôa&x4§"\x001e9t¼yzöº¨ZpWÒ{ÙÁTyZ?í°ê"\x001bU};uµÜEÐ¡¥#ÅéôMÑÍZ²-½çÓ¨&\x0004=È¡Hi\x0004\x000fÑTõ¸-D\x0017\x000c0\x0005ÞÔÉ\x0014oâ­ÕÄCç2ûó<5ý\x001b
Ç\x0010ö¯Â\x0012òK\x001cvà÷úèãºp\x0013\x0007J\x0017çY\x0003%q\x001c\x0002Ø\x0002Ûl2E¡Ç4ãØf§\x000f\x000bº\x000f\ÆÀqMu FwºÌ Æfí7·þy+û|rÚûì\x0015ù0y3×\x0017¸qd	NûDÛûÈM5\x001b~\x0018	»èâÆú~û\x001c\x0019úüðñÃj¢íiég\x001d{|Yn\x0018ùªè\Î[ú¨%Í¬h§	\x0010ML-ì\x0007Ì\x001fLîÌ\x001fv ñªy }kóT"\x0001Ç©D\x0005g §¹\x0010¢\x001b,vÓjãæ¹\x001b\x000b¸ÌÝH.yèâ±\x001aªh°$7r\x0006µÙASg
þgU\x0003Þ@4^?%7\x001c\x0008¿\x001a
\x0005p ·¨	Ý$\x001eEªHÇqCå§+N\x0001-\x0001\x0017OÛsy£\x001eÀ£\x001fÓ@?\x0011ûðÆi¸`Ãp\x001fç ü¤Õ0Îl\x0006ÎÖ2\x0011á\x0001tÝ´b±1_eVÃwh7>*Ýèg5-à8«Õ
2~%¢dbÞÍÔ8À&S\x0001Àá¨ryå#¸\x001bVÞ:#æñX\x0007t\x000f${Þf%\x0017.jBpMÙï\x000b\x0019Q3Ü§ßÒ§÷¨\x001fI=>¼?\x001d+zz\x0016AXúV\x00168.KN¯\x001e¹"|=å8*°.$Þ[\x0003
ÔÞ\x0001q¿e\x001e¬Ø&ÃF\x0013zÒkÕ'Pn\x0003ùw¶\x0016XT[Ó'6\x0007Û¢O%-¦®r\x000b-èÐz\x0018¹¸Î	:\x000fêTþ\x0015\x000f$Aô\x0014÷\x0003\x00136×\x000efÙÆ®\x001e=\x0010\x000c>Uá\x000b8P8ÓR´§¨XÓÊöaöÞüíù/oÁ{;q\x000fDT\x0011c\x0006\x001dN|àà&\x0014\x000c4Î¨GfLÌÅ¯5AL´ñ]Híä@\x0002©GÑ4ÅÑ\x001c¹6d
Ð÷)$ã~< \x001d@<)^×NI0\x0015\x0003\x0002x\x0000p\x001cÁÕy8\x0005¯\x0007tÓo¹¢©\x0018\x0010Ð¥\x0018?ù\x0016\x0007[1h\x001dSÏ]\x001bØ1f\x0001è\x0019Ð
²¡p`\x0019ù\x0014RHªZÉÚ§îL52.-d	-z´mÔ)¬Ê¹öµz\x0012Ð%3M\x001cû;ætGþ82\x001cÒ`õê	Aê­\x000buô2®ö¯\x0003º$¾yúCJhª,
º¦ØV>j§Éè-Ýs*Ú\x0006¡±ÉIsHÔCKJ«H\x0000\x000e\x001diYÒe¾	ìÏµêÑ\x0014%Æ.1>\x0007èÐÁAKv"&`BÞcºÆúéã!

}û*9èkÉ¦1¥\x001eÞ\x000fò¡pLd\x001cS}\x000e¦Ï¯Ú¾J.+5àaíÕ¼R7É«þiÏâseó\x000fÁk£éæáöý<Jï5viS\x000fºÍgxÆ×ÎÇãFv\x0003Ë5¦±^®É¨ÙLÀ\x0007\x0011
PFµ¡«j\x0006óÈ\x000cØ\x0013¹ãË\x0004ÐB°R\Ë>\\x0014]>\x0012ÜÐ
ÕZÜÆ«
Ø0;Ú¨IæLõ£ø¦³SÖ
]Ç
Ø@ïÁd!¹rº	Ç\x0004£sK¶a÷\x0014°a¼»
Z9:EA\ÌpØ÷¤£) à0AY·qv¼Õýôo\x000f\x000bß¿IÛ\x0012\x0017K 2\x001f\x001d\x001e\x001ayª"\x000e	C×_ï\x001fÚ¸\x0018\x0002d5XdÑ²¦jB\x0015\x001bv'K×£ò\x0002p¡N®C\x001d\x0016OíQR©F;e¥\x000fß\x001bu\x0017gXyÅ3Î#;fé##£ùªs¥¬e]÷\x0003³\x0017ð¢Ç\x001fpíª\x0002·¦Wêl³T«U&\x0006ÓUãÊ]òºÊ«©ôÉ\x0004\x0010l\x0018HÈq)\x001c\x0014MÓ<¸â·Qvnc\x0003ÏöDuû <¥â6^ªÉÀf\x001b\Â1L\x001cpáf\x0018«\x0010ÆÝì\x001cùÛØ0÷¹õ\nE¬ëó ²ú`Ïéý\x0007ð\x0008àQQ0WU÷ÙF­kë"5qzþ\x0001\x001c*d¯æ[+:"6B!¶¯<ýÓÈdÌ@5¤x­Tbéü¶ÁqzÈêÃ|ôQç÷gûC¤Çÿ¯¨\x0013AiÇÔãjÖ\x001b°á\x000f\x0007cTùPLòLà2<\x0012-\x0015·}Ä¡G§Á ½\x0014\x000f§R\x00132i0LáÖR4Ûà8$WÔ\x0018\x0005\x0014Ñ°OÃøØjû§¢3\x0000Ç3\x000e<><ÛÃè\x0017»a\x0015x\x001f¿6Mà\x0001p\x001c\x001cR_i\x000bWñ
¼tZTpû{8ä5½¨×b	&è½käS[`CÛ$Ï=f\x0010zÝ°ãe\x0012µÛ&PM-i×Þ"A¤MI?dk5Þ'UN\x001d\x0000\x000e3\x0016\x000cNóÔcu¢&9«¾wùo?m2.ª|snòWZÅêvö\x001aÚ\x00131ÅÒ\x0004\x001cR\jïæ@ZÀõ²;òöµ/píÉø\x0006SyØÕ£©I¶\x0008»©«©E\x000f°aLIØt`ò±Óô<jÏÉT-\x0008Ø`\x0019ÖÔå|NÔØ\x0002íÚ9FJ\x00038h\x0014ÎBá^\x001aý°¹¡¬\x0006Ó\x0008\x001b¶oÐ$E&:p`Ó¦0\x0019XúöøN¤¿}}
ØÎª÷>ë~{­¶¯B#	§\x0001\x001bÌNWñ¹·»ON´R)¤ÎÚº·of\x0001«\x0014\x0014\x000c7w:8DÐ:ÝUKãzH­\x0001\x001bNgp79Ó£ØÆlR3\x0017éñ©h^À¥h<\x0014\x0011\x0016ÎQ©Í\x000e¬Ó¦\x0016
\x000e\x0001\x001cüd\x000e¦
1=ê+\x0013u3G¥£ÅØÛ³ß¶g.BÌ08úç.íÛYÁS&cG)¯£ì\x0015\x0015a7Þæ\x0008\x0013°ÑSÎÐoÝ_\x001fíá\x000fOjëÞ¾\x0015<e¯ÛÉ\x0016×/ÃÅïCÈ¦¹à\x0000\x000eãtÃûCæÛÀ±ô4ÔÚÍåib\x0001g\x0000\x000fh.óKu9ÉZÓÏOjE»S¶\x0005À\x000bëGß6Í=:È<ôÁoÓ\x0008²\x0005ÝÂLHKÉê
RåÆCª ½yÊ-8ÿ\x001c²MjCGk¢ãÌ?\x0000\x001c6´xL¼ò$\x001d}÷\x0019\åý,¿Í\x001dEîäAâ>éü?õÔNaí´ÌûiabqÉ*½B\x001dV±nÈ#¾©o-dDKB5Çsý:uqÓÇ\x0015Ù)%*è\x0012-)Ié/\x0010Ê \x0014ëð\x000c\x0019»ò¾î
\x000cs¡Ñ\x000fNâC\x0014Ò`"ºÖ\x0004å¶õ¹\x0003òH¶Û,>ýQÑj0Ìr&£¥M[ÞÖ/®ÂÚmo_ã0´$8I¨½Q~ûz\x0013+DãI3j2\x0012íX·ßÜ Ú\x0011ÀÅ=l]\x0000øÐ\x0015ÅÊWbHZ¿ô\x0003¿}M=\x000cè¡g\x0012÷Ôðdqå\x001f8dÚø\x0003¿}M½AG+åÂ\x0006â\x0003%kb0û\x001böv¸ÌÃ Ãdb\x0008ôiGË\x000e¦¢éu#Ûq'q'ß)ì\x001f¬ÍôX1£ý
\x000eÏ5ÿswÄ\x0001=Û)|àÿ¨{\x0016\x0016ÄW.(\x0019ms%¸W0ãðÝ×·7ww'âe
*&Èì)ÒjOV72µsíð#ÎotSM¼þ]Fgj^ÉÆò|÷<¸/¼±7_ :âáöT½SYóûº\x000fdX1¹4$óÈ\Cë3æ\x0019¹]@gjFnô9åkY©y
A'\Mg6¶S0
ÀÅ<%ç\x001bh
-ÏÒ
HE
u÷ô·uF\x0001z\x0002t£Ð\x001e3HèzÔí.µ\x0002R\x0001=b {©ðÝÎÃ(\x0017o÷©h?M§\x0013t±hHcU\x001f§¢\x0007«èäóuÉL\x0003»\x0004],\x001a&\x0003w¶;·.³\x0005=&í+ÙÚæMÛi­ \x0007\x001cd\x0011 ¸cyø\x001d&é3__}[{k\x001añ&àâ¥(BÒ\x0014g\\x0005¤Á{\x0001ÙDx\x000bà085à\x000cF2jÃÊ<ÑIn\x0000O·.§©U¥È\x000c\«
ÈjQÏëÜTv"ü\x0004l0Ý}	âmn*2¡r\x0006Tv9×­Èihß\x0001Ý\x0015(¬[WbÇô_\x0003ßÜQ\x0007¯DæLÐ3D08Ù&VàÉô,ÀæzÈòø\x001f1¯
\x0013~ªyÆ©ä\x0008-¬¹×~J\x0002º=ªA¬äí\x0018JHzá¡ù\x0005~[{yÐ^Á 9EÓ^F)Þ!IÚk&!¹6áçë7ª¢ã;\x001e¦w*ê\x0011Îåé\x0000BZõZ\x001e\x0010Ll[]s]Þä\x0002à]Lc\x0000|}ùG?}ÚËsZÌ»ªOãÔó\x000c½êú
¤ò\x0016*ÎÂ­âÑó`øÈe5Æ®S»©U£Ku\x0003´j\x0014n4©cl}¨ù}f\x0018
\x0016ÛíuS¯\x0006 ÃÜ±Ô)z\x000fèÖ\x000c3ð¬2?h¿[@ßMÍ\x001a\x000eÍ\x001a¥ qã"\x0017É«\x0019x!ht×Ôº5\x0000]\ï,\x0006%xÂ\x001e}Ö¨O'\x0013\x001f÷Døø\x0003ºd:*{Ç04p o"ô¤xå=¢Í\x000bz*\x0000\x001d'\x001bªÂLÆáÜÃx¢é¦¡\x0010\x000e$¨L'@ç\x001c³Uè½Dû¨\x0001\x001dìU!ée¹\x0017=!ÔFO±Kf4*\x0001\x001d&\x001bf\x000bÏ8Ýa\x000c
æ+toZ@ej8\x0001t¸M¾ªQxÖ¾Â&s?ÌÂ¦Ëeû.ÁØíÂÅ¶0ñ±dÕT½>J~ÛÒ©EÀ¡¥èR\x0018¦ùL
Ü;½ôV6å¦f\x0016\x0000\x0001¬T@E:dÃáÁaÍÞ40qÈ\x00038Ì\x0007¬*BÆSt02Y\x0007ÆDR\x0002mÞ±f\x0003ºD<ÈîÂ´\x0004O\x001f¬jG­ÓêÑ¶\x0014¸\x0001\x001dÅÄ\x0004S,T%u3\x000c í|§nJ¦
:$S¹fÒÂI/ZM3<ûM7M\x0014p(
fSã\x0011\x001cî×÷(»V1
\x0017[Ð½{2ÿ\x0012¢{5#\x001f{AÌ¦T¼\x0001©p)\x0002>IuTª¾)ëÖ\x0016>ÑL\x0008ºE~è§ÑÌËðÞfÇû)B#à0Q¶\x0006US\x0016.´«Ñ
½`ÀO\x00157.\x00157Ùî¹¬\x001dí¹§\x0005=ûáEJ+
2\x001f\x001e~ùíýhÝ|:\x0019\x0015ebFxµâª\x0015\x001déo6¦OzzØMsw»¤½\x0004¯Óúú~ûì¤ßì»¯/Krus¢&¥t÷ºïSöQù¤(±áÉ%\x0002óäÏâì.#öGÀ®ñ¦Öá0½*\x0007eª¢þ¹BLV
`UCRCËÀr\x001e\x0006æ¾]âb»c2j\x0000\x001cÏWÙ\x0010æÍV\x0013ÌR\x001cR¹¦9øÓ\x0013(àð\x0004:®yT-Ja\x0016Nôè\x0003ÑRÓ\x000b\x0008àò\x00022ógÂ0&\x0002Uy:\x00106ðub\x0001pÙO2\x00130ë87¢6TWùÕÚÔeÚÞÏ\x0004û*\x00161[pÖûiõº[¡ÅD4\x0003Ø°YÑÖ1OêäöZ	p4±§hÁè\x00100\x0003Íí>*\x0015«
4\x0005Ó£5ÓÜK\x0000¯ \x0008E\x001c\x001aÔù¡¤ÛC­sbê\x0012ð\x000cMËÆa
!UÛ\x0000§04x+óÚ­\x0005[,T\x001eÀ\x0002>\x0007·¤«Z¬+HË´Ð(\x0010ÀÅâhÁ_8*ì¦âÂ§u7Olä
ùÉ`»\x0003+\x0002Ug5K0½ë\x001a¥\x000eàÐÏ3"\x0002W7?'7`7\x0003r[ä\x000eDÎ´ì@Ì\x0017ª\x0014¢çTð>IcSæ\x000ed\x001elnå«^ª«²°i¦ïg\x000f<LÕ~\x000eÕ~§[BjËÃUR%Y¹r¶oÞPWà\x001aE?K"±\!ú\x0001¾yE]\x0001ö\x000c²Û\x0003ê¬ËDBÕ\x0016*ó6¯`ó:\x0018°ckÁ>\x0013§j ÉGÐÑ®\x0007'`\x0006 ±-å\x0004ôRD6×ìIÁô¦\x0007?U \x0000:Nì5já¬ÕL]«¹´ÉrîYùíµÃÄ^~BÁ+p<öR½ i¸¤®9l{,\x0011QQ0Ï\x001d¿ª\x0000eðóLiI~LÊãë\x000fIù
£î¨A8Ù¤\x001f?~´÷È³ü ©§·KËÑ\x001d|\x001cV6=\x0004ñ\x000c\x0008«¦®¶.)¾WÒÕFë7¯àüøCàczxú S7%p\x0000<\x0008xBÚ\x0005Ç9bdKJC\x0010s(3­Ýe¸.@WuJ6» L)Î\x0003/³ß³³r±:ÝcÏ\x001eØ Ð
¤»8©(\x0005Ò´~Hûõõc\x000b
SÄùáÛ[xzI\x0000]^L¯^\x0000t:D_©.\x000f\x0013êz÷^\x0012@\x0017ª¬âI\x0010}U§3\x0007µ{3Úî\x000bº\x000eT¦[|U ÓFG\x000cë9=\x0001Ñº²ÂQ¹8O@¢ýC©ûå4'ç§ªQJ6-y¡À5ãBk¸t×?\x000b\x0007 Kélà\x0001 ùCV´
«Ò·+æZ×£ÍvêJ\x0013péJ\x000b<çVhÅ
OÁÅJrî
\x0003xG\x001f\x001fD@·°thP1\½â´ò¨w-ØV\x001eìGÃ\x0012ÀÇ¤9LN-\x001ds\x001fÜÁ2Ê¥s\x000cóË»#?ã\x001fË\x0017T\x0008®\x001a~r1X\x0010kZ>ye
ÐõÏñãçÏúÉ=ñ\x00048ÝSéj\xFK2xþ­I<Q:\x0016»öÜN1â.%~\x0011%FÌ\x001e6ô×ZÃujü&j#ûº¶$ÑT»
è^Ð
\x0012Z·ár`k\x0012ºU3\x0004y¸\ïi|\x0013AÇÑu³àmXCÂ)¼¨ä\x0012S\x0004µ& ¯%éÂ¬¦=¸Zjs{¦[@ÉrÅ ½%\x0007.¡ÌÓÐÿÎ×²¡O!\x0015AÉr5AßdëÆöJäjÜ\x0012=U=Ë=\x0015Ç\x00038LÜEÆ¡vôROI·L\x0013zseg×DÐ« óÐ\x0005\x0010;\x0019\x0010\x0013&ô0\x000cÅ³­PÍMÅñ.Åñ%Ú\x0000®¬å\x0011$jâÑíõfÅ¶Ï?ýdnoÔ+ËÕ×\x0017'¥[ª¶%¬a¨\jgÄÊávêô,fTØ)"×%Å
\x001f"r=Ø\x0013kI}»¢O°¶_Z;ä\x0000\x001d\x001c[z\x000cÄ.¡;\x001dK$t
ÎØóv÷æþú^¿$ßï®Nçº±:°[\x0000s
UØ\x0014Ê
òü¬3Mu¦]N­ª\x001d¸Péñ^%~K\x0014w@\x0018f#tÆ£©Ê\x0014°!££\x0016\ü\x001fëïÔ \x0019_l#=h\x0005\x001ci\x001dæ`ùZ)&Ôà«NX4i,\x0014@CÈk\x0004Ì« &0gæ6@z|¼\x0001\B\x0016Ç²sè\3ÏêêN¢2\x0015Æ\x0002°ÄZ¹µGOM:è§ÚHµ6L>¸`CDQ\x000f¹`Â	U
\x0017Vò<\x0006ÁÇ\x001bÀ#HÄ+ú
?tÈ:Pz¸Vó2ÕÅ\x0002xBq\x0003õ\x001eýÍ¬FÕsøIÅöÏ6Ì
àPób¸ÙReh/¶eÍ¦Ê\x0011\x0001Ê\x00116«!÷Äü\x0007*=\x0014ã@;\x000bøD¹³ {\x000bKçg\x001bÐI©\x0004QÐC~=]¨~f?\x0001ï\x0010ú	íß>eòutf!¤
¹\x001dw_ÆÐ\x001fj.\x0008ýY´·Aóç ­\x0003®þýë_ë×¨ðÝé,¬Z`m0KCN
Á\x000b_S¦oÖyú)ÔvÎ_6!µ·[îíÆú~{³\x000c&[Ðåâ\x0006ºLK\x0015\x001f¡Û\x001c¹¤ ãn½\x0002ÑÎ9LAãÏÎBµÓc­\d¦éø
½±uµ·pAÇÞBrÃqí$eÝæFF³B\x000f±ÑBù)Ú*è\x0016æJ±ÁáA2UU Ú"¸ö¦ÏBê \x001a¸W1ËKÂ²IÃ¸¨~ÅÍE\x001eõ¦Þ_¼nÕõõ©.\x0016ó\x0012áÝ&m(ìôô_$ùm¹©ãýûÍpú4	¼É©9=õÊ6\ÛMCº×T{.i\x001aQr@÷\x0006³Nõ¶44Õ*ï§\x0013Ì:óíÕ»ÝW\x0018JÖ,îûû\x0000òª[Å¼P
GïpÂ5)¤ç2ôo\x000e]v9éÐeädþ2fÖ?\x0004Õ³\x001fºÉÉÌ=D7^_ëÛÚÞ )eM¿yú\x0007Ê\x001c{ÿð«}£æ\x001fnÞèòVf$\x00159éËËÃ)åU)Ûw\x001e·_rk{§ä{\x0017RË;@m;{92õ/\x000fc¸®Õ«o÷{³m|Y\x0016to¡\x0010ßÜÅ\x001b/\x0004§h°*~(t;÷ÁÚê_²¾½?^~¾¸?U¢s¨õ&ç \x001fn/\x0007¼îBm|TwÙ®\x000eqS;l\x0013ëfiå6 (Åá~uô;33d¨*\x0002.*âp×ÿeîÝvì:²+Ñ_!ün"îÇbUW\x001d\x0018UFuÙ¨FH[dJÉL*ÉD\x0001\x0007ðoøµº¾£þÄ_ÒsÎXkÅ\x0011kí\x0012¨mf\x0007¶S\x001aZ{Æm^Çæa\x0001=\x0002zVâ\x0015\x0002Ñ¤ÀUU#\x0014'<n\x001a(\x0003ðÂ´5ôÉô]\x0015q²µ$,a¦a\x0001¼g0möÐÑâY§Y¥\x0001­.bO\x0004¹;zOa2ÅA¿3}ð\x0019Ë=ÔzÇ6]0k¬wôÂdUÅ>ÝèEí\x001eÕvkR}a.%\x00197%*:zOT\x0014cpWÐ#VÇ«­\x0003z\x0000r\x0015nÿé\x001f§³gQÐGO\x0004Ð»,·t÷|\x0005\x000b\x0006Ç¯²ÑÄ\x0005\x001a\x0005|ôc\x0001¼w
Tfªï|µ\x001fMIÃ§\x0007á²qSÊ\x0002Ð{Û@eAÈ®²Ä\x001d4\x0016·L)&*ôäÛ¢\x001e\x001fÔ³à<(¿ûP½\x0016·§p\x0001\x001dÈ^òt\x0011ß§ojý<\Ä7W·\x0017s£5VG`\x001b47¡°\x001em¯ÄTÎE=	\x0019­ñ2kfâè\x001f©ö¿þì/_BûöíëWÊËùóÝ5ý¸\x000b\x0015 CÒÓ9o\x0005È`#\x000cØyÃïÈ×µþÐ¡Æ1äÎìUÂ`\x001d4ê1í\x0003çôÓ£æ £¥\x0000zâlÞÐ}çlæÌ0ÈÄx7wX÷	Z¢<G+\x0001ôD~ÜÑ;ù1}»ÇWÖ$ä\x0014äUS/\x0015S`Ì5\x0007ÃÌ¾sþ|÷@\x0007÷îRâB\x0014£©äí<.Ñø\x001cÔ
9éX¾²DæÔÊ4\x0016Û¬Ä\x000er\x001f¢\x001dÕ\x000bJÌÇi£ìªj µ\x001c\x001epü3Å\x0002zg*~
((e§8\x0016V´aÁ2²\x001d»óZXºå]Oð\x0014ÜÓ
«äa	;Ä$b\x0006è\x001e¾<öi;.Uq\x001bàÓU;µ¦©L#·Þ£Î]svÇ	úÂïèÙyÏ\x001dget\x001b.RÐ.ØS\x0006¿c'ÀÎ^BÊ|ühu²²²\x000b\x0013N
ú\x0007ïè \x001bc\x0017Ø&ô¨3 8]-´\x0008úT]ëèÅÅ¤ªÔd\x0019U àîE%ë\kãFn\x0001½³¸\x0018lg¦+pËèQ*\x0008´]¶ØN#·\x001d¼ÜFVú)=Òd:F%\x0003FF\x000c
=4¢iæ\x0016Ðárõ\x000e>}ýE
¼\x0019}.tì~L])gþò/êù8|xj2\x0008Ç§´\x001bEòYðÃsÕ\x0014×ÜXÜ/Fzo&¿#Ýc¿U~Ç_N¯\x001fnþþ·\x000by\x001e®h\x0016oN3¬ÝÆÌÓ\x000cCÃF\x0004z¾2#Õ¾z§øR¡x	:_j
ôtñ">ÍøÐo\x000fê*stA4AÉ³ïèÛUFdï}2\x0014M\x0001ÿ\x000f=MVÍd9\x0013m\x0002ð\x000e:tHÐÉÌTÄÈJèY7^\x0002;ñ¥\x0002øvÑá\x0006~~A±«Ì¹\x0004uÑ\x001b.OßD
è¥Û¼ÄçÐ.Êª\x000b\x0016M^UÉEåªµ\x0001¼vprÀ ãLQÕj\x0011
gÛùTÙÀ]¯Å´Ý\x0002\x001dÜàPÕn±CG¤ð{\x001aû\x0000ôí\x001e«ä
=NÈç1»\x001cTlÏD2á¦è{\x0005ç?mû]ÞäÊý\x00130Dû%ª\x000b³C2\x000b>µvôÞ*J12q¿\x001e£¤X¤É0~h\x001fÂìæçMG
³É½ ¦{òSzÿC\x001d:{þíêæý¥¸s2¯ÉÙ­ôEô¾Z$W`²\x0018v<\x001eßÑvS\x0010Õ\x000c%e¤®3íÇÖ\x0007&èI­Ì³tjr\x001eNÉÞLT^;z¶Ø$S¸'\x0018Á&·\x000b
Ê$}ÓÁ»ô
×@¼Ô¬zPY)O\x0005Ö¬û&èã¡\x0005t«ÐM¤DItFW·YQ¢\x00047Z@ï9³ÐzH;ómõ·»l"8\x0005è1cQ@ 9fWX¥AÉµVFO¶5þN)@ï\x0019³À-\x0005ö»W<§{½^ÒÅèã»
è=cÆd3¥\x0002ºb¶!ôT>-Û7ë\x0000zêèËð4ØÝcÞÖ<Ø½Yf|[\x0001}{[Y\x0018ÒÏt\x001aA
®\x000c\x0007©åX'\x001d\x0000ïÇ4¹\x0014]Ì\bpQé}\x001a®(á\x001ct\x0013)\x0007 ÷cè\x0007(\x0011*\x001afè#ô%s~|Nû¤D\x000eKÙº!Ãb\x0017oH½\x001fc»a¦é£\x000eÞ§2?P};f¾oð$eM\x0013XGr|@^¿ýþÆ^é\x0007äßß=Ü_]ßÜ\(ÉÊ&TG:ù\x0014ûÆ	8¢\90~\x0012ÅL7Íª4SÉúZØ¦»7ôùU¹7´5õlxòí6\x001c\x0010\x0000w°53ð>\x0012zT\x001e«¡%Í\x001a}nîþîó\x000f×W\x000fzÉ>7§¥ÐÑD«Ùn&Ü\x001cp\-+Í}íbæþ|ßxg63M)ô\x000cÜzä²\x0007EêY¬î#òíB\x001e.@\x0003Õ¿70KÁ[ÑÚ[f\x0010&¢'oñ¾\x0004ìSÉk\x0002ïjUCz¦WQ}vZrÃÓ°Äî\x0011ÅT`I­vý\x001et_d6qÞ×ß¤ï?Üô]ùW¾n>üýoWÒ¦~\x000e
\x000e<1ÍÀ\x001d3½}Kõ\x0008D:µå+w¤×\x001c÷âûI£\x0019ÃA`Ò\x0010NUß¿?Å\x000cfNe×ÍØ\x0001Ð{s7?·¥'üÕýOÕêñ&r[<\x0011;\x0000ºo÷½=§ÜsÕV\x0015ÉÖ5Ì\x0002«÷Æ¿X,ø%feä´U´ùÄ¥\x0001Ð½k%&»]ôìTËP5^µr\x0012xk¶äÕ\x0000¼7òP
Éõ\x0016$\x00063ß×¤ÚO|\x001d¼÷F\x001eÖDp§Õ§Ö\x0000B÷m·LW\x001d½÷ra·ÏùÊRö­ºXD{±Nòm\x000e³59bj;Vc-Õ©t\x0013¡»öí\x0013\x001f[G¯`Ò#4rëø~WèªBÇô\x0004òé[\x0007\x0007\x0001·P-´¸\x001aTkI¶éÁN|Ó\x000eì+ä\x0004ç¾ÓC\x0019ÈtªMzË8ÓFÃ\x000f)0\x000f²Ù{
7Z¯ç
ª³úÓØ¬\x0001\x001cºs õÓ)Ö´HÕQ½¢ê0©Î»IkmCw\x0005\x0012³¯ô\x001d\x0013X)\x0012§<jT\x0004å\_h¬q\x0015n¯ýãì«#èw«pÇ°\\x001eØÞqÌËÓ
¦ELJ"e^7t\x000fÂ°gR`·gMQNvwaØ-\x0015whw\x000fÊ°©Tu\x000f\x0014¯6dåL°¾ØåÕðSÛWG\x0007MÎ¨¸
F\x0005Ñ³¡K\x0016©%s\x001a;BñÄn\x0007ñ+_ï^utÓ\x001d©úÊèz{~íC}ýí>Íoß]}:]=°SðoW×·ÈQ¸»¹ÓÍ¤Êøº¼úÜ¶rEw+Þ\x0019«4\x0011=~ãÄT\x0002\x0010i¾\x001eîdúzrV¢5ÕÄùâ¸ã\x0018\x0003véØ	ESÄ±Æ£Jèº$7O'zðÓq¢G2~­zÝâ°nsP¾0-ûè/w\x000fNlü¿Ònzûp±¸-ëjJ0µó²xò0!\x0017å\x0017vë¯I\x0004\x0019LÜi}:
ÙVzðYÖ\x00193aàEÇJ\x0000\x0018¡ÐsV÷¦\x00137è^9­Ùc:þ)l&dh=rFþIÙÄÛ q\x000eÏ(éTò«n\x001dÅúí0I\x0019fj\x0011X¡¡A ÒZæ\x0014Á)Å*\x0017\x0007\x0006('L/S¡z2ue@`®L¹Ó-¾6®ßÉÉY¡Nm£D¶.ýà|ÖJ®ÓzrB6hÐÁr\x0006©rù«\x0015%\x0016Ïà\x000f_-Ò£W¹BW\x0014\x0005.£Ö+ÆfÜø;h\x001bJ¯&\x0016l\x000bsMFåûXZN\x0019Ä»QÚPz\x0002¦\x0017vEFÍëEõnÎY\x000bøy]HókKÀÑÆ\x0006á\x0015\x0019}[Í¨Cg§¿:´ñÔ?²B\x0003];+¡@\x0001[Ð\x001dcYêQox.c\x0006²\x000cQÓF\x000eOãU³\x0011«¼iälÂnfoÅö0áÌÙ\x001eTÓvz!É¹×;»ÍÖÍ·+6Î
3Í\x001e`s~Ucë±ïºÔW¦ÌÃ
y\x0007Ëzq\x001dz\x0010º¢8a¸Fªoc ¹Ag\x0005m\x0001;DÍ\x000e\x0018íÀ&i¤;3©¯Ø\x0010Íp[?Çy¼'Ìk8ÒÈ
{ßDL²@£\x0014 ]8ßìèR©1\x000eÜ -\x000cåúVl\x0010ësÌ\x0002\x000c;)ýÕg\x000fÏ·\x0013¾Ô,|ö\x0000½d7è¤¹;cQÙ\x000cÂn4çG¯¯\x0007Ú\x0001&ÖE¶TîÐÄºÊpº§ºôVlÅp¬&ñ\x001d éÌ&ÛDF6·ÍÍÄP	±uÃ\x0015\x0013<\x000f\x000c"þà§°tÅ 	FA§Óò\x001c77ÅÛÚÜ!ËüþDY¿@\x0007 ¬§é9Zý´'}\x00032©®LïOãû+4\x000cï³ó
åqo&2ÍnàHN\x0006\x0008SûÜ
z\x0015>ªÉwþnE{\x001bts/ìì\x001cY$¢Eö}×³~/c\x001f½î\x0011^÷ppof¶/U9\x000e»¼Åq8ðw*HÅ\x0016¾¹Aï!\x001a(ç2­Q´¢'yî
Ú\x0003tA·5°n\x0012|1º>K$tfÅ¹\x0006nAo.ÕZ`\x0018g\4x¬ê\x000fn\x0005_\x0016p{ÉÌ³\x000e\x000c)Ñ\x0016-2thÐ¿ÚØÚ¦°\x0015»\x0002vÀâÞètK\x001eÎK¥µNÙÅ\x0005<eèþXø"Ö²²)ºÞn4W§×¦\x001ar\x0005ïÄGÿ»Î*]Îå9ÎÖØA{gZþàÃ³Ã¶â@¼+#VÛMÕý\x0019©eZ¦a¬\x0015ºb1©"ðl9Ö7\x000cTæfoÝá\x0010cKþ\x001fÜVò
ÜàÌ£KU7kg*ðlÚ\x001f\x001c ùCï+©@\x001dÃêL\x0019?gü\x0015vuæsêÀ[°\x0016\x0001¨é³pb@p4xYR¹S½n\x0003Âñ\x0019|¸Uo<\x000f\x00165v\ÒÄû½ü¡·\x0005$.\x0012Õ\x000eÞ*ÍÕ´e\x001aTXÁû\x0002wû÷L+ÅzÎ*
?v\x001eÕ\x001e'WLöJ=på\x000f[a]ÜÓ\x001e±+Þ Á}ëbÊ9+x\x0006ð\x0010 mÀ\x001dVD¸j¯IôÓ"4\x000eB@ùÃ:cétÂH µJî§H\x0015vi'ß¥/X±4»·fy"2\x0001eë²Þ,9¶ävºÎ\x0017ðÜ{Îe\x001cj\x001b
aðy\x001cJ­'í\±Jª-+x¯µpªµªí¢Q½YØ{Y73eÝ\x001eýõúôðÓ³ß¾ûûÿálî¥roiÅHÖmþK6`)r¼\x001c«'@¾9Õ\x0019ØdºG.ï\x0000ÙgÇr\x0015*^4]Ú\x0016Èí]8F÷°¥Àí#\x0000­½èâóÀ|ßöþÔ¨µ"{(Öù6\x001e=%cÂ\x001e-R#³Fã
¼óQÊ Y­ØÁÝ\x001f:h	ö(l6CØìKÆ\_ï´Í~:(rHG¡­\x0019BÛmxv\x000bK\x0016õ`\x0004Ø$©º;j¼¦\x001cãÑ\x0019åÆ\x0006=\x0011\x0010¬Ð\x001e \x001dÒ	Û&]ÓÍºN\x0017]³°\x0017Ú
6¶\x0012¥ÀwÓ\x0013ÉýÂ\x0003n\x001a;Ì-ÛnÉÜÿøì7×\x0017¢µ¦;_gÔhÿ-}G\x001c \x0002!\x001bwö~íÖ\x0017ãvC;.A«¯@®Ù¨ö[Kþ:nH\x001bN?\x0019I?ílõ\x0006\x000cÍXU)VZ7ÜY6¨ê/U¤LvÔ\\x00019£Ð%/F1QÙ±ìåp\x0004ºçp"§\x0002) 5NçpèWhÞ¾D´{^#ÿ\x000f\x000b=^Ü	\x000fy\x0016æ¾Sm|Ô\x001dZÎÔ]¾b÷ÞòXÅn^:¼ZÙÅx­uUæ¥½«V°\x0003|÷þî>{2vÇæVl\x0018c	
pÓynÖ«¾7]è _¶iîxü?@5æ\x0000LUÏ3\x0002û¬[\x0001[\x0007XâVäÎ\x0011\x0017³x"h?¶\x0002ú\x0001»ñ&ïÕg\x0004\x001b$Ï3·0\x000267\x0002"\x0012ü\x0015¶Mrå`!a¼=2m\x000f\x0017\x0016ÅlÐE\x0013÷{nIc³ó@\x0008´\x0007\x0005{îý§ÊUì[ªULN\x001eÌQc\x0005î|\x001a\x001e\x0008$U\x0013¡Z\x001c|ÃZºÌO,Ã+v\x0002{p6¡7];¢È(3;Ô
;JÀR&ºô\x0005»t²ôH¿áy\x001fé³¬KÚY\x0014Àk\x0019õÐx»ë^þüaÁö,9\x0005\x0012íB¢	ö¦°Zù>®ú¦c&]\x0006.ØÀcA\x001a/Súð¢¦ò¯qï\x0011\x0002 Þ³ñþ\x0003¿e7WÏ^îßî¯/4pJWbqB³¦.2y&<³OB\x0006ÞMõ½Wd.ño{\x001aààëÏýð=§ÈÍN\x0011¯Â\x0005©FíÐ§.¹î\x0001\x0004¸Ë2ï)L!Xò4æà8ãP O½ê[>\x0006]Î¶^Ó!R\x001c¿L¶¦o\x000eÑ_~\x0003\x0007
%Âw::²º~Aø;r\x0016/\x001a/0\x001e´l\x0017w\x000f÷dÜ»\x000b1\x0014ÎHÂÇPp:\x0013¹\x0003¿&×\x001a£¼áO`'ïæ\x0015K{7É\x001a5ÀÌ­FÑÛ)Õ\x0015»tØ0:ª\x001b60G&lU£mÐ¹pvRæ®~Zâ²·Ä¿;ýp±ÆþnE°Ò\x0006Ò6jXHêÉ¯*_7urpÚ)¼¤5(²\x0006½oéàëÏþò5ÈxÌîï®ê\x001düûßîn¯îß\è¨%M2d³°ö.%O\x0016Üº|+y\x0011²YÀRLÂ¶¯ÈdâìC¡yÿëÏþò½¥\x0000\x0002¤?^=k«Ñæ³/³\x0004Ì)¢gyd$l©úñ\x0005D¶þ«»\x0015G,¿£wGKÀ<"\x000e4\x0017ªCË«5¦jðqp§%·E\x0010cÏo\x0007ßÄ3L;¯õÉ°ÖÜ8»-/L1ëtßß}â¤ñ\x001f®/D\x0016*¤	ªÕ7ÖÐãÝ\x0008\x000f³a§rßÁÁ+2ÜwvÙÿús?|^F²´±ÙýþîR
Y\x0014HîL\x0015W±úÌ·!åÕW]=b¨Ú$^ä\x0008ô2\x00157æ@4
\x0003Me,~Ü¸\x000f¦`î\x0011\x0001ËH÷¹I\x0017½SyÒÊÝ
;·\É$Ì°a÷2¯Ë\x0015ûÛbLbô­©H\x0003\x0017÷vvMQäÜÿ=E\x001eö£Tso°¦ ©B9!;üÊÂûòsZé\x0015\x0019@§£PÛ`ÝIb\x0016\x001aô\x000f­À9/ï\x000cU\x0007\x0003\x001d0.
Jõ\x0003©¡ÍKusrWàî<{PÆ'èz2aW}ÐmjÐï¼Bwß\x0015{Á\x0018t«©i©¬ó'd
¿Ûp¹"£dzÎXLó±É£vhÝ;\x001b¬Y(<¥¿¹{}uÃ{gZ|\x0013ùâØþë²ôSv÷=\x0005ß\x000f7w×Ó]jÍÞy0çÏ\x0003÷1$ ëypÉ\x0006\x001dÙ±:=´ò÷¿Ýþç\x000f÷ÿÌ\x001bþW/4N£!\x0011úÿùpEØÏþJÿKÇÒ}\x0019²jP!å©qô\x0008Y\x0010£L»¥Ê64OÿÝý\x000eyÿp{ýúúÃj¯Å\x0010Ã\x0016Íð¿\x0016;üo4ÄÚ~Tô¹ê5fæ­Á\x0006©¦êF	ËÿÃÝ\x0007ú¿]ó?²Y0Ì/¿(GÆ¤¤
ñòÝUðßÿ¤ÓýëáWùâªæy\sñã\x001dyø	úÔ¢õI¿\x0015Züøb´s1ùz\x0003ÿùj-öö6þóÃ_qÖ\x0002ÃÃm^~¾ûæíÕp\x0014ÿDÔõ\x000eáÕ­\x00047\x0007écò¶\x0012,ÜEu#Ï\x0008Ôø\x0018+AÎÙ\x001e¿¬\x001d\x0016¢\x000b[`Å
Ù	\x0008o"m\x001e\x0014\x001bÀ\x001a%\x0003ÊÿFÇ£\x0010|\x001bbþ6\x0003´ß
¼"¸/^·N¹\x001eÐíÆCï\æ]éè\x0016¡KP#ÏÉ6Z\x0010\x000f¡CìÐÒ\x0012\x0006K[òÖRÉà)\x0019½+¢Ç0îý
<¾÷\x000föÍÙ=ÇèåÐæ±tgç \x0012Lèn«]\x001bÀe¾?
S0\x0000¶9\x0018\x0002\x000fAÊX«Éy\x000eFYÝ\x000f\x00167
%lDßØ<ýXá	áô¸\x0017ÉL\x001a½1\x001føúÝýòò»¾\x001f\x0003ª7òJO]Ë~ÌVß:ÞA¦yéÓ7\x001f^ý¬oßßß½½½1¿ðþ·IõÖeÚu}'
Å
=½\x000c-w}K­½Kg:ºÍ\ÃÑårè¿!æÞ\x0014)·¿naúå^øD?ê\x0018ÿå'y\x0017C»Ü·*°=cÄÿ
§ëÜ<>¿0oOï>|£^ú?°ä6\x001bîýõ¶ûÂGÆk¿\x0015©WCù Ý\x0003óÆ?ÆrSä\x001cw>½Õ`ü\x000clzô`\x0014\x0003ã\I_6½fúýL¬¢­b¤§!WR\x0007ßdõèýR->ÒF¿â&Õ0ÁÜ÷2¬èÆÛtC·\x001b;¡TMºx\x001c¡\x0007ÿ\x001c¿£]\x0005nìC»Ø­RçD)u£0'pç;3/£×A¿.ÓÆ¬1>3Þ\x0019\x0016\x0006J,ÓèÃÀN\x000e\x000eÕ\x001e~»·ýÛy0 û
>¸¨_\x0002½v×£°\x001f3;Þ§v\x000e·ý¹\x0013³ûþvpx}®¨gÀã\x0013V}¹rJBJ2\x0015Ëñþå\x0001'°\x0004{k8dðàÌ\x0008.,av| 7ðlû\x0003\x0019-rÐú@V*è9h6Àý-\x0002~¸¢\x0019Vn/Ø\x0008&uªn\x0006¯AÌ\x0014dº&\x000f©\x000bDß\x0017\x000e£\x0007
\x001c\x0017´F=âEà|JóñVÏ°Õ©0\x001c)vÉÎªÚ0©
#ô²qóò§7\x0018¿½¨o×É¢åÛK<üö\x0012áÛéÂê¹?Úøá¹v\x0006õ\x0010c|Q\x0019ÊV½\x0015®øË\x00034!µ/ÏêË÷^ÍáV+`~GÀcRà:gÌ<B>Æ%ÞãÌí´Ú,\x0006íÂY¡Á.2\x001fÑ# 3)FÏ
½ê,\x001dsr1ú±Ù+=Ñ\x0005ÓÙU\x0005Ý{\Óat"E×æ\x0002\x000foZ£:§=ûã9Y<S}\x000bDé´säNsÏÛ:<¸´RÃçs½~Æ\x000bRÚâÜ@¯£­Ø¶¸\x0003g½\x0001Õ7-ÞÀè½úð9ü8HjþE\x0018v¦¾é/sÊªµj¤?V³vpób¹ëÐYðØ9:Þ<Í\/\x0002ÿðWµÀ¼\x0010íýÝwª°ýû»ûÓÔßñ«\x0010£"È\x0008ä	¬ùÀî\x0013\x000c\x00119ºêG\x001aô\x001f×N*ßTÿ¨î¶ÚJUÞøW8Ô»ã_\x0011³²&$\x000bòBÏ\x0017@\x001fCjï!5\x0013_ÈDÿö\x001f\x0000Ñrù\x000f\x0004=(\x001fx¾zÜDÜçæ[}_Ü__].îÕ+\x001aÛÎ2Óoô]\x0014è²y¤]\x0003;¥sí|ÜEÍXR=ßv'\x0002(·yÚé¹«øûµ\x001aR´â-
<\x0001x%ÚSú¢ pucGfé\x0013ôq\x0002z¿X\x001eìÏdn\x0018§û\x0018ð ½\x001f~g\x0002@o¾\x001bíGdÖ
F\x0014.AE×Þaú¸ñ%Ã\x000fï/\x0019ÅC©«gñÞ±Ê¿¢ÿnvuâ£Ðº½?³¦/ßwÃSÜÓ=OZU#-<`x5ÚM«*ÃbÁ\x000fýoë\x000f½g\x001e\x0000Æ\x0001	-ùü¨8ÃÉ>yìä4/¯~úát¯\x001f\x0017÷\x000f§¹O÷Ëê<\x001c­\x0006\x0007GfùþÉ³Q\x0014t£îW;º<ï±÷\x000cA]³<Ã[P\x0017\x00139Î=IîhOâè\x000eÛiCim\x001aÕ\x0014zèè\x0005\x00180Ëà 
óÎê>èºHCL1ÀÞÕb)Ìáø\x000ew{G\;Ý5U$²GÅ\x000cÄÞ\x00143\ä>N\x001d#÷4\x0000qºO³kÐÿ'\x0005n\x0000:ú6xDèL Ö\\x001e\x0012\x0006É\x000c>Z9ÿÿYyB¡{°KÅþ\x0002\x001e\x0002\x0007n\x0003\x0016ÀV¬¦`¦ò>¾\x0019Êð÷·;-)_X·N
W¥$éïV§«\x0002\x0018+¢\x0014DÊÓqqGÙÍÕZ/QvóðWµÀìâ¦\x000fW?*Yg:Ý_ß]b\x0019$¨G\x0011\x0012³õmùÇ\x0010)óÝ\x0013òq§\x0014m³NÑ:Åé\x001c<µL\x0002F|Uë¾FòJË®ÿ°¡ÿà¸ R{\x0018SÅt\x001eÓ@)Ï^M\x0019<cþw\x0003÷±çCnh(dRÁj²*»LÎó\x0006Ê>Ý¨6ÐïN¯o®\x001eÞ\_æ$³úÑ®üö¬\x0003¡\x0008\x001f¢¼/Oæ$Ûñ\x001dkæ×`{Ç~ÅY\x000bL\x000bqûñÊßéÆ?îï?_(È¨E\x000fi÷ä­l\x0017ÕÀ¨WþQ\x000eòAÝ.Ç¡Ùê%òõÓ¯\x0008¶§nèGX	-Uës\x0001z$ÕWà¡3>¢gÝ®<h¦Ð«\x00195ªÍËÏïnÞ¾\x001b4Ð~óöê~î\x0001þÂÛºê§;R·jÉ¦%pF%Iñ\x0011ªu9ìÅc\l¥æêYþ\x0011}êP\|©tã¾«mc§\x001b£±Ý£±/Ä\x001e
Ìa©\x001ddÃ.½\mxJ\x0018^á\x0002\x0003 ²'´NE¢\x0007\\t;ul¬èü§íË-\x0006À¢;ù\cT' }y«1N%#\x0000÷ðö\x0002¿>¿½^eºéí:É\x0017ÍBövÞ3Ý&\x0015 I\x000c§:,*}\x0017kî!;U¤\x0000\x001dê£9\x0003{\x0007½ìF]\x0008©F¯-Ó*»Sx\x0001à°¦Å\x0001«A\x0010!\x001bU\x001eÕ\x0002!þFT7\x0006F\x001dÝõâq \x0000Ê,«ª\x0002ÈPV_"Ö`]\x0000¼\x001fQÎQEHÜf cO×²«±¤RvKÞîàÓ+ôø\x0004nÊ©X.u\x0000o$aîxÃ8Ø01C>2°\x000cbÖEé¬iH\x000b=à1:8äõ1z\x001b¢¤^\x0010Úìljc\x0000tØ¾@P\x0017wª.Â²/z;º6qé¦®°\x000enlô©Ê(nÒ,£¢\x0004Ú2Í0\x0017¯u\x0005Î)Æé´¦i8I>éý?Þ1¾ï\x0018\x001f-ð\x0011Ð§WÕÌ½ÕZ\x0016é¹+¬£÷\x001b%¤1z¹s1:ê-@õñ¢¦ô+
7E\x000f\x001b¸îWÛ9ç»¢[ÈùÒõÐ0ÜVèº\x001euz3Ó}9ùK¯ïÞ__¿\âë$\x0019ZRk\x001aU1óÊ\x0006"7Ïü©SFÛ\x000fn§Þf+ñ
 }m+&|©\x0017·å¯uÿQòíõ\x001eoú
Üöî\OÛ©\x000fbs­×vJsib3CëAÎ©G
ýñ RÁùwdå [Xå!\x0014æÓ? Ïr·ß>¾RÕGåÿt±Vì\x0019î¨ºEW|\x0003Y¸ßèHO)º£ÓÐìÅ«
#\x0010>G ´¢w\x001d\x0018QÅ\x0002Yµ±ð\x0013 {iêy\x0000ô¾¼S×Eæy\x000b\çdt¬0ÏÚ¸ÎÉóý÷¨\x0010zõì/w\x000fW¯ß.ï×\x0002d>¶ÍVÍ\x000eâ¤üQ\x001aî\x000fÊîS0Ñ¬%}y=¯½ÿ#Îþþ9Êý±¼ÿ&ýÓ0ùp{}º¿T\x0013r¶U{ÕúíIæd\x0006D,U§R2»ðÅZ\x0012víá7ä¡\x0003<bUvl"{SKW.z÷1#ÉÜOªCÜ\x0002ÝhØ­\x0015Ý\x001a\x0018ª\x0008V9\x0015ÞôqËÖÄî´?Dÿ OÞVG\x0007o+ bD(Á\x0008\x0015& ëljSpÙq\x00147pp\x0014÷X/eåJà\x0003A¤UØè\x0000t\x0007Ã	äO¨\x000b.µ(©;Éj74µDð¡]|ìvñ\x0001	\x0008Br:9E>®ê\x0004ÌY?;[×7§o®¥»zµ£­üÉ©¨§^¸1v­èÐÿËÎ\x000fµHSö#TK%7Ú:9Db,>Z\x001b->ý\x0008KI§ñLC+fv­5-\x001c»\x0000àtPûÔ§RçJ¢\x0016f\x0008¾íÎ8îÎ\x000e\x001e{:oG4?GdêËõ\x0014|jÜÛÕó\x000eh÷\x0000_A³Ç³À»×ðW6\x0007\x0010®öÃ9ü\x000f_°Wõ,Wøº;8[;çß¿{ýóûou°AÿÊÅM\x000cU% ÉCÚÚÅrô \x001eÀ,b°§\x0012mØ2FòÍZâ=lüÑ¯8k\x0001\x0019\x0018}\x0013@¯¿\x001a½þmG¯æ×¡{èÇXÂ§G×çõÕõÅ<\x001fæÑ\x0014u«ãØ\Q­É\x001b\x001eÅ~\x0014ßg\x0017åñ¢kæâãûE'}áÀ\x001eª\ªÝ\x0000^KFÐã&Ýøã#\x000fà½dÊ«
òÆé8¬«[:\DS\x0008°CÇ.¡§Ê½±¹«	É%Tõ%äÊNÆãêÓí·\x0001\x001a6~Áwº¾¹¹ºP50W£+dÓ­PDD\x001fÎ1MõÓ	dR\x001atÄf<®\x0019`þv÷GýýÓbÄÏ¯ËëWú4ÿñêöÍÅÎrqª¾\x0011JkeÜÖ\x0004Äã~Ú#=\x0008û«PÇÓÖl%/3\x000e¨íý³?Zx2×@C.=Ü·®®o/\x0011Ôs´Âu'\x000cj³t\x0016¶¼\x0004Ø\x0001Í±ÂÄõT.ÔQ#{µÖKÔÈ¦<`e=\x00195ÊÇ:ÓÇÚ´To\x0019\x000f@÷¿\x001e}¼T\x0001½×ÝZ\x0000&»³\x0008îã@&¼Óªö>7ã8Æoia\x001eÞn/uktªÊ*qö¶Èuï³\x000c&Õ$e¦'\x0000·f±¡\x0003¢V³ýlÊ\x001ap«¾Õ??¶Þ±S\x001f¡{§¾\x0017¢Ö\x000c&\x0002IÁ7ª\x000bËq<4-´y~¾Áþ¯ÿøÏß<Ü\ê¢ÈQ×r¬Ô©¤PÀ{ô)ÒÐ\x001d}àf+Éè÷ÂðÁ¯8gy\x0011Þ}~=¸À¿¹ÃÎËå¼`\x0011UÂ¦\x0006Ú\x000ek.Á1_K/Gk£\x000c\x0003?ãæF\x0007¦Lª¢ÝauTä>áqlô`´H=«¶¢è´Ð\x001b¸ï\x000bÍbLÐzjMÕ\x0003L8¢Íkçn¦T¿\x001f>\x000e+ýñãÅH¸¬V$õ9¥e*ö:ÐqoÇÓ9n#kèj+Å\x001bzô#Îþþðãêç7·ïÚÖéþÓ»\x001dµì½NÙ¦-máÒR«ßÉéù£T¶\x000en½\x0008¨YKzt{âwÿGýýÓ2îÞ¾×É£\x0017w\x000f¯ß]¢V¦]Î\x0006³Ñpx
´a{ë£´S<Upf\x001aªnÖzi\x001côö\x001dý³&Öáîþsýñ4zi!.Öbi½n½²u-\x0001Jï\x00134ád\x0000}B^ÀÔ«Ø¬56Äïÿ³\x0006ÖátûáÃM\x001cÏÃýÛKÛKU£+i}þ½O	ã\x0011Ö|}BlÉÃq\x0011Æ5h>×>1é#vsyæ*\x0001ÿ )\x0019LÂX\x0000\x0004ìÞ\x0013\x0012b\x0018á\x001eLç,\x0007\x001d3]µ4\x001cCO\x0008\x0005Ì éw*Ó_²SYÔÀ?Mr´Çà\x0015¾Ü¡ô\x001dwºb¤Y²\x0016`²^©¹ë\x000eÞ»Ð¼w\x0015Åvj\x0006\x0002ÓÖá¡ÂXº¤è:9s\x0000^\x00158P\x0001WT|màNG)°øc{°9O¥førÛUY\x0005<j.Z¦\x000eÚâ1xßä+b\x001b\x0014÷ê\x00195EZµÍ}kÌË·oOßjíûÛä2ÙO¶\x000cr¹~½\x0013ëÅ÷~Qïé§\x0012\x000b«©^¢æ#+:Pó£_á{J\,\x0010ÕL\x0016\x0019g7í\x001f@·\x001dÝW¬,rK#È'²@¤\x001fìkæ%þéúÍO,1¢×¢ZÈV+OJëmoPÍÒÜù(¤s\x00079ºi©Æ,;\x0008÷\x0002\x000bNc{ÉUweøÖð=­0÷lÇôõÐÕ(u¶Îkã:!Û[`\x0001\x001c2øn\x0003÷u>±ÁÖÆ¨Ñs·ÏâLR¿¿»{±t{ÍºÃ:wºTf\x0011è\x0001qHÙHuýë\x000fÇÄ÷DwÆ Ì¥Gc,óâ$2]ð»§\x0019Tø8BîY|\\x0019é\x0015¬Þ\x0007£iÃjA\x001c_Ý
¹td¦ÆÂoÎz\x0012Á+v\x0005úäF£4¥8\x0016ä^Í¾)}ñ¡s¨K1.*mßhø-Fâ7`ß?9VP*ñ\x0019vÅ\x0018ÎÚÁÌBÎ4¦X7è\x0000vvÈDÈ·AÇÛkÚa&+i¬RGÐ½¿þ]dZÉ\x0014[e
­¥\x0008j#:\x0002NðÍÂ`¡²çYm4à\x00161ôè¨nÈ¹¯ 40«jvá±\x0012[w£\x001eí¹
{µX#|±QÞ\x0012Wþä ½.SÒn®`?Å6
 °~¦ë¢2?Ñ\x0019,Ø¶\x0019Øb¢'uQ\7ëó0 \x001f\\x001cÖ`cQñ\x000b_8ôÀ¯fgBaÛ\x001a\x00027l(·³Ç\x000eÇÎ»\x001a\x0006âa\x000fm¼Û
¸AÃAL\x0011ÃB;<(c»\x001cô	oüæà$ò\x001fº±\x00156³xbÕ\x0002"uÈ#í[»;¶b[ÄÎ2%¿­dÒû/Ù o¦vÊç\x0011¦\x0015Ûé\x001bÄÃ\x0006ôQ=ÅtÌõ´qrïÙp\x001d\x0000;ª\x0016±B\x0000ê»Õ
\x0014¡\x0008öÔÁ¸b÷þEyÏÁgkDº¬þlewç\x000bÿ°}ö"Õ³bó®Q7I0z´\x00019»`CþÖ²o¼R¥º°IQc\x0007Þav\x0017ìÐc][<ÐGêFZÚýêÑeZ#\x0011\x0007OGØ	°¹­\x001bøQÒõQØÂ/\x0018Ç\x0000Ï#'Oû{@.G\x001bÁÜ ³ÑdL\x000bñêÔ\x0019´@Gè\x000bªÜKÜ¿þ)ýå¬\x0019á¼ÌÆ£;ÂÅÍ2ÏÅÐõy/F·±\x001d§[Þ±\\x0001Â£E8XÇ¼B*ÃëBDytT\x001cpµj^1$£èÍR)úHoi÷G¸\x001a¸\x001eàÚ÷Ï9Ó°3b{$\x0004£èN¥C\x0012\x001dKebÛÝíÌ¾Áå\x000f½¶!\x0005\x00152»>ØÎ\x0002÷µ)\x001f¬¦ü¡×\x0016\x000bnÂb³îÌç¶l\x0015ìÐÀ÷·¡ü\x0001Á½\x001e]À\x000c8ë ÐÚ\x0016§\x001d<óò\x0007\x00049HÖ6·E\x000fó~¾õÎï_²ò^«´Ð²\x0017ø-V£Qëê6{ÇkPþUÐÞÙÎ·óó¤\x00159m3­´\x0017\x000f3¬$çànß\x0004MËKÿÖhHË<SÙ÷Öä\x000f=÷¨s@b6¤p^ù=ÜÓ)Û$MÄ\x000bx²ðå,×Ý±):Óû;«zUb®mÁØïWlà¾§S
ì°"QÁ³J÷FGkô8\x0000ÏÐgùì&wt_Ù VSõ°§^æ1o~ÿùþÇ\x001a§N\x000f×7\x0017k.(Ö8æhû¬H-î)°LÒ\x0011¶P\x0006\x0015¹ô ³\x0011{ý­z5xojòâ"òÅ\x001b´óÀt\x0012Ò\x000b;\x0016P\x0011U+ÍÑ£5w\x0016|åû\x0007h¼d¹¿ÿípáp/7+ÅÃGxVx\ÛÙ8þéo£+T8J
ofïoÆz©Øû~ÅY\x000bÌÜböýé44xüùt{±©Ù½*cÅè¶qJ[iç\x0000]¯æqèjºxÌ¸\x000eÍZ\x0012Iöð£:\x0007ÇútøµÐ\x0007Y JÔ49:Þs$¥:äOñEWÛÒ8\x0010\x0017émVù¾¼û9(¡ªgÿ~ºÿt\x0011L+jY*zó9-u_)Ðî0·ÛK>ðÉäîÓ\x0018ò4cñ2¤\x0001g¹âÞ@ÂL§*|(Æ¨e Ø¹îr@\x0000x÷­ªC~:Çç@Õ%­U×µÏÂ g'á\x000e\x000eÂ\x0007þÒ\x0005!}.Ï±rh¢\x0007 Óêg\x00029£ÿòpbUá?^ý@¿TóKòNÙÏÆUÑÛÒ²¤ë\x000eÊÔ\x0008ö\x000bY\x001aLÓ\x0016V\x001c
tU÷+K,\x000c\x0007çôÖ!'i?çÛp{Î×ÛäPÚ6äF?Ó¡½Öh'²;Ïº`Ã4«§ÚçE\x0012VMëG¯n5¿Ó¨szoz\x000fThM³èÙÍe{\x0008mJßÕ§h×\x000f{u U@\x001eDÇ\x001fù¥\x000fSs³\x0019g\zsÿÑ¯8kù\x000c7óNå·ËÎ®åU\x001e%PÈ¹9Ö±VT½àôC}\x00141©"|iãjLÊl2éEMpÒ#ßWåÕtÏn(Fr&eÞ\x0017èIúÙ×\x0018µâ\x0008OÿªD:«Ê\x001f1Eï
\x001b}\x0014¼À \x001eÓÁÁµì´\x0002·!ï²Ä¬Ø\x0016¿\x001bæ¡m-á£³þhïwyßWÜðë¿yN4.Ø\x0019¿Ù(ýkSë\x0011AVß¥v^ Ø5\x0001ú~¶ö¹W\x0016Ñ¼nôð5Âët\x0000;&,\x0000# M\x0012GÉ\x001b#nØË\x0016lï`><F\x0010ò&î\x0018B+kÇ B@~Î\x0005.ÐYCCÞÅ¬­\x001du\x00051Ò\x001b',ò\x0007Ð\x0001¿:!9\x0010Ê'½ÿt=.D\x0019È\x000fs9dÁrH)È}L\x001b0é³]Ö]tÖIî?OIô\x0005;C9ÜzìþKA§ÑÕÏ`%g\x001cæ\x0004æeUÚÜ\x001eÎdô*\x0007C6ÑâBy\x0011\x0018½\x001d»W`\x000bs\ôCiÕTrEÛ¤¦¦\x001d:å\x0016ì\x0002)ú ò.ÖEmoòU5%z²mk«
;am5D`·ódTæÖ½7´ÒæÌè\x0002­Ô\x0005¿hä)Ù²`g\x000fâ<$\x0005M5*¡ÊT²6kR­y;Vì\x0004që\x0015Z±½×¼Õ$\x001eÜÚÁJò\x001fzA\x0004µ´]EÒÁ®A\x0015àYØ_É£g¡\x0004\x0014-4ÐÊFáe\x0001xè]v*ûd§°Î¥ì\x0006]¡ý/NBÈ\x0015\x001b\x0002H»0woØ¥óý·i'­'FW`Ï\x0005Ð\x0005;ÿêrÖûZ±AíËF\x000fó½RÕQÉâ¢%Ü|{ÍÔÞ -v¡3\x0003\x00124\x001dq\x0006\x001d\x000f\x000eëp
]ÊMu§å¡CË\x0003sý »á\x001a1&¢\x0019¾»I£ÌD+6>:_vÁÚs\x0003\x0007uHÚÐ°5è²+º-Ü§/w
[°½ùõnàklQRÝ¥â,F£d¥¯\x0003xS»9òª,xU\x001c\x0002¸\øÎg\x0002ÓÓ\x0002­/Üº\x0018z\x0005\x0007ZhO÷Sx\x001cÙA\x0017-|Ð6gÃF
»ðå\x000f\x001b8ù\x0001¾6¢bòÉ\x000f}áÁ5bÕ\x0003;\x0010\x000cÌô\x0005\x0017mIºVÉ\x000f~\x001fÚùô\x0007üá×ns?ñ\x0001®à (ôOà\x0000Ñú"ËoAw\x001cújZ±rb>ÝÀç+ î$=mUJuÝ,Y¿\x0011n¡(ó\x0007N¸üa\x0003ÏØÑH[ÖàÑjò\x0012Ú÷=Åú+6§b¯²ÒWuÃ3­:<÷ñ-Ø½°\x001dÔYåQÆ¾
\x0002×¢¶<Ò ±Ú<XÜÀ\x0003\x0015\x001bìÜ /wª\x000b3éhSºû\x0014\x0016pèS6À^¡Ã_e\x0018¢'íä»¥QáÈ£µàÑÒqCZJz²¶y2Ú3Ì±õ<³\x001f\x0003èåî'<Î&KZ\x0001ú`¯DØ+É&hñ¡gC;B9U\x001dzû¶\x000fÓ<Ü°\x0013L&3G÷¹Ý\x0002Gõs\x000eT×7²0b\x000eöa\x0002\x0007.qú
¾;\x0007Í\x001fcÕ/\hdöiâ9[Á;Ë\x0019û¿êÃj±ÏYÓw¹ÓD}µ"wâ+Eyb\x0016¼Kxa\x0015;\XQäm>:>\x0019OvGn³I\x000eî«þðØ.¬|tÕf\x0014å¦cÜáQ:\x0008;¸Î½ó\x0016oÌ\x000eq?H?là	ÿÄ_Q¯þèêûÔ¸·óÄ
²\x0017\x0000/\x0019z,¼ñFußQ\x0010íµÓlJã\x001d9:ø\x0005\x000e~q\x0019tÏÄýT\x001aßt|\x0006³¸2å`A\x000bÌzpo\x001f\x001eÎ´ÍkÑ\~>µyr)?làµb¦Ð\x000e!\x0010sw\x000cwV,,GÏDg²Ð°Ïfq8;h\x001dÀ]i\x0014l\x0007_ªÊnòâÔVÄ\x0005-Üû¦ÁKQ|Ä
>"G°pöã &h­vnÉ\x0019\x0012×iÀfÅö\x001a\x001bÄ¦yû\x0001\\x001fÐ[¥åÀÿt KBW·(ßsYt%¦a=]k`Ýÿr\x0014Þ¬îÁ,n¹öÃ(hïe&Vè.2!X\x001eA6âmKG`Hª"³vîRZ°{Ò:29\x0000ï]x¥ ÅÐ5Õ\x001cz\x001e¢ÚÔ´÷\x000e®rùCÇ¶8H;Z½ùm\x000bQ\x0012\x0014ÜVs\x0004ÞPY?×©ï6ê»«ª÷\x0011vh\x001f\x001e°#`sFGÌNWü\x0006£4Mr~\x0002\x000eÀ3'Ôz¦\x001d_UüVb\x001cÃÐ²âî Ý$ØÀsQîDP=ÄËÑ7JßâGÒõd\x0016ß%J%Q\x000bôúÒ7¬§21m+Ï~,uÔpí\x0019OÐ"ÿÂ'-Ö\x0001<ý\x0005à¿,©ÏaÃ><ÿ¥ÃYH±3\x0017\x0008É¥Hüæôì¦³À=û7úýñîáÃÊ[ÜWaO^\x000e
µ2_¿f,d¿`LÐè1Aé¸é4þ<;­UÒ(\x000cQ¥{º6Ä
Þéý\x0017hPs*Õà\x001cz´
Wß÷çt9~«Úk\x00022nÐÝ\x0006Æ\x0014
-ÉÑ¼3\x000b&È¹»íò\x0002!ÔlÕ`#ù£DlKçç¯A£Æ\x0012ùTÀ¶º\x0016kT\x0004ü	9]é\x0008;A@@.Aì<\x00081
\x0011&Çð¥Úö\x001c@;øl\x0019\x001b\x0005½ß0\x0003úg~D"k
\x000b6t21X§\x0012 uLÚ$9(7çi¤Ô·7
ad\¦\x0007\x0003ïF\x0007&Ñ<ùÔ\x0015v\x0011=Ø]ÂèØ\x000e'ÂÖ´\x00139ê1\x000bÂëp´\x0003\x0003ìÀÀ
í¸M\x001d=\x0019U\x0014g8m\x0013Étídþ\x001b6dþ\x001d×±úg\x0017®"*aÓ «q2w[¿hJsËýûû«Û7\x001fýùþô¯ª?.¦NIÏú\x001a»\x0012\x000f»¼­ÏÁJNæ©pÃOÃ\x0006¯ÈfrÑô\x001e/áÔö
«PySijüh%\x0010Ef\x001b¶¨Gú\x0003\x0019¢ÆÜ¸ÇÊ´¾\x001dÙ);°`;eá\x0018\x000c\x000f\x001ex³U-Û0ôg\x001aWLÈ#ïcÿp`}dÿ·§b9V7èjëOo%oáo:<Kûv¿\x000e\x0001ÖuÙÑT¡Èyv@^\x0010\x0003B\x000eÇÓÛëÛËì|\x001eP\x001fa:73Y\x0000\x001d#÷\x0013=¾òÁÆôÉV²ñ¡%\x000bÞ}sF\x001bT¤Fo®fþ/2Ú91¬Ð ¶PÁAÚÈeeU£Ö­¡¥"ªwæ
Ýw¦-	\x001bc}"7I)
¤ªoº¦Å³ÏñÍ¡M^¾éè,§\x0007àu¿Ô\x001a7£|{üéßþºOýî<4õþËÝ\x0003-üø\híXßîûÀÅÁþ&C*§ø©ôôNBl+^.SI?Á©\x001e\x0007ºF\x0015%\x0013ý|]42ä=Wh ïây/lq\x0018\5[3â´î8h
º;h\x0004m ;ÍhUÄFÐ:mcÜØ\x001aqn%}¸ìHA\x0018Ò¶Ôm÷ðÄQ·<OHÔÇÏ
\x0014/6Ò)D#s½Ô|^Ñx,&x&àÃ°¤$5VÎlO\x001cõOÔì;2\x0013úö+ÓÕ¢sä¹ªS\x0019\x0004©öÎ

{g©Ôl\x001f\x001dtÚ¹h:\x0006úh·O¹²@÷rÏS!ý	ql\x000eÅútù\x0002Ë\x0003Â\x0006
	²ã+`'ÍuXrQcR!úF0­\x000bvÏVá§ØJ;7yHgwÓúH§û¥a;¸_È	Vå¤Ev)NÕeæà9Øös$Õ }¤¼çyi¶Uò\x0014õ«Ê$ÑÒê9\x0005;\x000bt\x000fv<]åÈ4bø~Á?Ð·´¾Æ\x0003ìP\x0001{÷Ø½1øVó\x001a
:õ¼T¸\x0016¹n¨\x0012«q\x0008¤Zù:Íe\x0005»%$!¼Â.C²Ywkõ¤ó\x0008»·cAÎ\x001eË\x0017®\x001cDeª6·m³ê)\x001dì\x0012þÃf\x0013¤ëi$VÛ0ÊÞV#Öê&I\x0015»½¹W¨¿ÿ¬é\x0015¶÷ÊÞ¦e÷w
µ+v\x0001lä²rL<¢¶wpz\x000bÒ¿,ÄG2Ã¡´]û\*MÐÃ|\x0015êDÖ&çû
\\x0011\x0018GÀ²³ú
V³è\x0018/ý<·_/Ø\x0019¦bÄ1«ÞÜV'×ØD2³p°¹\x000bVfªC{¯/n¯/@ÏJ\x0011\x000c=·\x0007.Ð½=P"ÇNµä\x00127P*l¯ô\x00088½&.ô\ûmØ\x0015¤é\x0000ò9é»;\x0007\x0014¶\x0011v:×Q\x0016l¨£\x0018Ì\x0017.\x0016Õí^ø>Õ©géH·f&\x001d\x0010lkt Ò¾(
½­nBð%7yÄ\x0006\x000e\x0003\x0017\eÄcHI×8î\x000eäTA\x0003?°ü\x0001Ò0Ãªj-\x0014Ûëä	RU'(WlÈ:\x0016îJ\x0011STj¡«^Ï8æÅ}Û»\x001b¸\x0003â\x001cUj0\x0018M3Y\x0004WÐ¸FæÎ¦\x0005\x001c:j´à­ñ£¯\x001eè_S´>Uþ\x0008\x001czaªAaòV\x001e]ØÊ,©y'ôäN±í1î±/|évJKcÕKKä\x0011æ¾_èk]&à\x0011¦Á#Ü\x0011wbòñ)N9}ä@år\x0003ozô9D\x0018}\x0016\x0001eæ¶ùë\x0007*Lø½\x0013åÎi\x001bJ\x0003Êdúc5;÷¬X9àP\x0019\x0018#\x0013¦;á\x0019Â	Wyv®;Ï®6õÚª»\x001eR\x0016í\x001d/Ô\x000cE\x001fO\x000f	¸.\x0004ÝF²úW[]'èÖ¶>»\x0000Ë(]o»cEè\x0015vRG6ïcï¼¦ã(«d^rOº
f'%tÓ çË`Ë zìÎæÆaÅÚ­s5)Æ¼_ªZ¡TÅ×\x000c¤0y\x001dÕÍuT;¯Ì\x0010_¹Êê¿8KUsY±ÚÒ±¶\x0016.
WÃ$\x0001rÑ\x0017/ýÃzóEé]ñó¬QÃö\x0006
llj\Æ¨4bsuI/cËýùp\x001d\x0000»DÜÙ>ê\x0006Ç:¸±fú*`\x0006¢ÛêÜE'åµ\x0003hì\x000eÎ¡âe^uF¦XVàA.0©Ö¯Ð\x0011\x000b¥ªÜ1©2\x0012jª/¨hÄq\x000eåàÌð\x001f:vÖ}
ïbö ìaH/×$t\x0007ß\x001dq$\x0003\x0019PfÓ\x0015ÇRt\x0006ì-CzGg=ZünÔ&l#É&ìÉÔÐ6;>E\x0008íÁG°E9CU7\x0006ÓË#ÐGÖhmîÜF:\x0008\x0016
Ð´u÷2açÅöïw\x000f÷\x0017zïYÀPß\x000c¹Ë´PÜ?!øVÕüú\x000f¾\x0017Ñ¼IbÊ=¹^*íxÏ\x000cÐrË#Æ:3it\x000bu\x0012¦XZæ}h×© }ô8\x0015HX¥n´AW£³|©Q\x0002ºïrÁN \x001b,¾\x0014\x0016¢ª´§f\x0004\x000c¬\x0006,ÙøùUnØ}XüKM2w®­ÐðÙÑ °§8TµÔä\x001aÒðTHo&IlØ\x001eE@<pÈÑ+4*i$Ýq|ØÉV4h*\x001d0¦â¯F=Ùi\x00020òäósÖ©A{H×r0<p5*û5_MHA\x0002Å£\x0005\x001bJÝü\x0012{­\x0002Ü¬»\x0018ûàñ\x000cÃã)\x001b\x000eÝ+St¼B/~óå6MÂ==Yæ`JåoRÕ\x0003\x0013)\x0008v0\x0007Øü
\x000e8Oö\x001dt\x0006uÜåi>8ïü
|L^xÒ.g²NcgéZ\x0008G6	Øòòßxx\x0019½Î\x00184ÅwÊ©=Í\x0007ß\x001dár1aÅ«qøì\x0017ºÇ\x0006ö¼tð2áe¦#fZkØ°S¢\x0019È!x+q\x001e9X°=4\x001e;Å\x000c\x001d?D5\x001e\x000f»¤ÑòÎ½Ø+2\x0018Û*\x0012dnhÒ\x001dÍyøhaÿGÏMçÆ\x001654Ê\x001f­.@:ÝzÔpÀ'°`\x0017Ì©\x001aìl¡½«>5[uè*7IÚ©ß	túeJo°\x0008\x0013q(ì¤c×¶³?Ø}üQµ*v¥{[\x0015½æ@fñ.IïÄS
\x001bêUÜf\x0005ÒM<É¨J\x0011Þ\x000f_-Ù¦´lÐ\x0005f\x00018\x001b\x0004\x0017I)º
®-Ýþä\x001ayÃ¤2½bwi:óXüµ7#ÇÙ£0 >²t\x0019ÿñáõõéöÙ»ÛÛÓÕÃ\x001cDÞiÊQ­a\x0013.cî2\x0018ô°B·ÛW¼Ã§\x001bãÐâF*6«»4$\x0014«ÕL\x0017\x0014W´^®¹"6îyh§`I7°Ìg*V»\x0014ôvK"4\x001d|6ÿ¡Ä­\x001aS©A×$¹\x0004¬ÔrÏóÖ\°akòÉO°¢Åè|\x0019øPBëúe\x0016lM\x0002\x000e{5äÎQîJ\x0019«ËFx\x0001]8Â\x000eàÓòµJvði½öiùGKéÔR¢\x0012\x001aÓhÏ³8Ýò\x0017ÎÙ[°Á\x0013ò?XKÝÛà50¹M\x001cî\x0008¸ ¯®]Ã
ÊØC¢OÂdåæäÝ¯t~ÕôÔ\x000e
kSü Y|jÝ\x001e;Ë\x0002í-@sÅ­\x001fIÃ\x0012\x0019è\x0007å<Ï8©íù6¤íðÜ8LQo§¯t²·6Ú¿wí|ï¾¹°0}¶*×eÉwË¯¥$\x001c×÷®Í~ýÜHÚoN\x0016Â6iÁ®
g=êr8£·àOÁ¾®\x001a×\x0006íæ}o\x0007X³\x0001ËÝ\x0016â Ù))ll\x0017ÁÁw»¬oÃ>I\x0013L\x0018½cG]+2Ô¼·ïí°ïcujÆÅ3<
ÚË w-Çz\x001d\x0000Û(sû­3AµÔo<#;1âÛcÄ£xv\x00173öÎ;Ô°û;\x0014kP\x0010×m2PLí\x0014?ÏQîó½á\x0008ÛtJº=(*AlÇSðÝsbÍ¬\x0006=û\x000bv\x000f÷#ë×@ãËá¹Cè4(S£oÛQ hÐ½í!²Â\x000fÌ¹ðxcÈ­Å}
vnæ^X°³8sqÜ\x0005\x0001'²5+\x0002tã·s\x0015¾AÇ^"ÜÕw3 z$Ðºâæªí\x000e\x000bZÃ\x0006\x0016´Ç¶[fËË¸äe©ÃN·ÃÌÜÎNÊ^Uõ²ä´§
IvmÜywB]Ô­'½§Ïã\x0019ôy\\x000cªhV¹kSñ¥¨ä\´­ÿ$íH0\x0008t\x0002	\x0006¦Dì×W°AO\drwµÒM+"9ý/ØÖ`únônx\x0007¢.Z¨±´R«ùû\x001d]
Áö KÁõ§ÍSj¥\x0014E$\x0011¹û¥ÍªÎçµa÷ëÑeßD\x0016ð­\x001d#7}\x0010-p9°	PP:>T%\x0001¶æ4 )íZ\x0016o\x001c¨\x0007)ØÀÉ\x000c½A$Tg\x00009ëúSbÎiF;ýë\x001c\x001ddÿ\x0010=\x0002¾3ÖÀa.k9]\x0005\x0008ôZ\x000eú%Ö4Õ¢´CL-ØÉèª\×P{\x0007·£$õ\x001c÷Ô¦.wº
s\^í.&\x001bÕ7ÀE9­éÒÏ¶\x001c\x001cyùCß\x0019Õh(|Öeaº|Á}\x000e{î´\x001f6Þ<\Vv=ij,ïÖÁhO1\x0012öÓ$©¯íf!\x001aïÝy[¶6s\x0003,\x0004Kêhû\x0005^8&zúuh9ñ¶íËyç4hÉnÔÒ¢HÈ)QÜÀ&ãÃ~£úî9G\x000fIc&\x0018:G\x0018O\ô¹z¾@G([ÐgB8müX¶Ð)RßxÒv\x0006\x001brBä¼\x0018²4`5¬ËÛoÜ\x0014hA.Ð½¾ø¶+´Ëºñl$¿±Æl¦ÉnÐ@-ÒöÖeªQ=Óã\x0007î\x000e¾·vü£OéõÇg¿;Ý^_=üt¸×ròêsûËYzì[lEº¯Z£µ;§u'îuCÜK>P|¡©éÙjþÅäù{\x0017ä\x0004±AîBÇ\x0015µ)Ó-i»J\x0019ÆÎ\x0014-
Úv\x0016²»Qj\x0015äcëhIÏ²\x0010v\x0013\x001d)6\x0017ìN±\x0019E7úîª\x0002j[ÕÁzÞÞza
ìÏ?^=ûÓéÓÕõýõÅ\x0012r\x0006u^+÷o\x001eæ¦©îùã$Ã\x000fTa¦¹W2Üø½Ç\x000cP:eÎ6ÕdX\x001f2Ò\x000bã&ÒÐ\x0005ÛEââF@Hs\x001a§Û¥«Îø°,P\x0013Ü\x001b{kûwCom4(B(dVEåQ'æ³0/¬4\B%
`-1õNÊfi\x000eÍ-²Y~Fâ¼þ£{4öðI\x0018fô	_Åä-C¹¼O{JaPl¬ZÑ\x0002Æf}\x0000ÝåÑ\x0006OXÊ^+îV_\x0006haÇ²WèÞ¦ÊnB\x0008ðÕEë\x0004W§	\x0005KZÒ\x001f\x000b¶\x000b\x001c5tEèÖÓåÏÆ4\x0017ß\x0017hlZ3Ü³ê\x0012F%ÖY­dîd ifrê\x000b	\HÜ
\x0007öfÕx­ì©êDKsÍÐ¹?=»ù¯ÿøÏÿñöæúã¥&kSÔmV\x0014¦×îâ;é°]\x001e\x0018z`%´}dy2;
l\x0013W\x0006[W\x0002¸2\58¶VC\x0010$ðñu'\x000eçBÙk8B¢'\x001f
8nCTdË%\x00195¬AÈ\x0012èï\x0008D5d\x0010â\°GèÔ\x001fvÖBNÌ),£µ³?Ò +ø´Ü4
sê¡\x0015u 0\x0019(ºø<íèä.ÀðÍ¡ g\x00133eõÍIïx·ÊÏþYËVÂ|\x0016´\x0007lZÓ £)=3ÉL¡ûMö\x000b6¬ÑÃ
¤\x0012¢¦C¤rAG~\x0004{§\x001c×°!
ìZÍÍÒ:æ	£©\x0005xÃXa\x000eÃóµ¨±Uï$kC\x000fØÉí\x0008\x001b:Nè®\x0019>Vúd©aï5\x0002¹½gö\x001e.'¥¤l=t
\x000e-`ç0°Ag\x0008\x0003\x0019\x001fä+xÌ»*èa\x0019½\x000c}Õüêúãáæ~ùJjë&l}êë!jöÙÂäîÃ\x0006ºÇÿBÐÿ\x0005¹«ìÙ»jºªf?\x000c3BM¿óÓõ'úÿÿÏ«ûO§ûÓErò¢(êu£Í¦³\x0016è½H\x000bFþ)Ñyìx\x0007mÞ¾{\x0007ô\x0013
\x0010ºR¡}nïÇSøÙ
¡³;ß°;\x000fx(\x0011§6\x001cE9A°vjlH­\x001b'&íÃ;¨wgÚ÷®§µ\x0004Þªtk°ÑÏÃr/´li«O§«Ëzó¬:ðoLHÕÊ¡\x0015i©Nè\x000e\x0007X°r'õë®\x0016Mp¶zÅ¥E7îJåVI¹ïÆ[zÃî·tÖ\\x0013,¯\x001eÕ\x000e~
].Wºi7ìÞ)É£ì¨\x000bR4aµ\x0003E(±Ì\x0002è½.y¯¹zýý\x0003ÝEÿzýÃÕý\x000bm£ì\x001e-
f»,O¹ÂIKÒÆóTø´Â\x000eÉ¯¼\x000c\x0001H~\x000b/-\x0010/¤a\x0017y§ÕéLS§Û©å¯Ø°\@óD+\x0013\x0019}¡¾Õ¦\x0017jÍÁgË\x001fVË³D(p:­±¯ 3\x0008lÙÐv§³Ô\x000brÏR\x0007®Sø.\x0013·£=«³Ó»\x001b¦ý\x000f×¹aB$K[|·rOáðWó?¡\x001f<·\x00081\x0012¾ö}ÿ3_/î¯?~<]K\x0013{)êá'ÂY/Î¸M\x000b(äbãä}*iy!è\x0002Jüõ¡fgZgº8U?E¨JÛäe|gªÏnØ=×K¦Ã¦çN\x0016cG=×XKk¸\x00016èëMYM\x00061Õw¶v³5\x000b«õ\x0011vþõØ;oIÃ.¿\x001e{ç-iØµc'¼E!\x0002»`[==Ùç3!a~KÞ<<ûíÝ÷Ïþpõpsw±ÖA§Õz|)ym\x001d¤+¼ÂP<¡þ(}&û.É<cq¾m¥\x0013«Â\x0000AP¤¸Ú`;\x001b#->Mn°ÜËsA;´ ½vl[\x0014Ù¯\x0005á{Á6JÝfÃÞwÃ\x0010ï&ÚSê»i%*~7­Ú@\x001cæ|\x001aFn?4úëéKEE6ê»Éìív÷p"g{o-E)}*úÓv'Ûë\x001d/EÏö\x001eý³¿çÈ±zs÷Ïñ§ëÓ\x0004äS\x001dh\x0006¿jËWóu\x0007avlâ\x001dO¥\x0014:q½"cIê±_ó44´éVÅá|X\x001a4u¯\x0016ºA÷´8\x0013\x0017C»+Kw)QÀ\x001atô¸\x0008¦0¥Å·Ï´¸áÁHÈ.±Èµ*ChÌ(ä\x0010)Î)þåB¡¯7
ß'ÇÀ26{\x0014ØÑ\x000f»\x001e?^ý@Ëz¡¬{6â@fÇ»'à`\x0005R(ò:ýýI}Or`ÿ¢µà®C\x000bó_Î\x0018$Ë\x0012m*%ðA;T-êåÅÌd½+8ÐH³"\x0002\x0017´%ó\x0016mÞ°WùÎI¿\x0007	èÙ_î\x001eÞ^¬s54ä½ëÆ\x0008ÄÞ\x0010¤C_â	-ôL\x0017N\x0006\x0013\x0002Ô\x000fÕkàªºB\x001e4£øÒÑî\x001cç
Z\x001dç\x0014é \x0014 P÷ T]µäÉÞ½ãìÆãÌ\x0013'\x000f¯îOi¾áOñ^·]+»½8^I®	¯O|BÉ¬©ÎÓ
\¢¸
üâ8%jÃX\x0019×Ö{\x00061×`R¬4¥Oe°¬\x000c´'óãág¿ü±£û¨jiÅèæSïò°IËÞ .h¹ºþxwûì_O\x000f?\ª\x0010kÝ t¸1\x001c»\x001a<\Ëèßã´6ì_\x0014Ó\x0014à+®p}\x0003x²¸ÿ¬ÀO\x0008\x0003µ\x000fãD§d±ÜìV¬ØàV°¤+èëQèð\;-ªËú{×z\x000eþ\x001b¢Kãu\x001a½úkûJ,ÕC*nUó|2¡Á|Ôä¾î:C\x0007?àìoß\x0013.¢6Lrsz&*$ÏZÜ¡ëz,c\x000b±\x0006ú.9ÍLö8kQbÞ9n3M%YMz%A\x0003þËT\x0018v\x001a6231Ý\x000b\x000c%?Ý\x001få\x0000'K\x00197ï)J1v\x0006E)\x0016\x000e\x0006qÒà\x000fr\x001cÊn©çVÌ\x0005»O!ÄExÅæ\x0016X¥\x001b\tê/y¡4Ë;Ã|
\x001bØÒXÚ7EØ2U]o9%Ý¸bk&Ú)È\x000bvé\x0005yr\x0013v±ïdÀÞ^õ>.DIefu^°!LE5ñ3Qâ\x0006\x001béÐ)\x0018²ùÎx`Wä4³\x0006;³\x0019[S¥êOÂAg·×\x0012Âà\x000eZB\bµ-WÄúWNy`*u¯FµWä\x0013~}w!\x0006\x0008&ªÄõIÆíú\x0000G)Trw\x001fe\x001aù(Ô;¬lËÍõ\x000e+gx&	©ª&±I%«P7²@·P4Í¢Ö\x000bEÓæ5Ø´\x0010À4ìh\x001a½ô\x0006M>¦í1»Vø¦üñ¿SF0fÍÏ[MÚt\x0004YÁAz\x000e^yB>ÜÌíùªhäö.¨ß«µ \x001bTÝ\x0016Âøì;,À\x0016®ýMX\x000b>Ø-\x0019u[\x001a³dï	7å \x0017úþô×ùô\x0008ÎöÞ<\è·¸!¸M¾_|\x0016dØ8âÈ2j±ïÊÍm·d7ñ¨a`o÷\x0017ûí{:rª!üã3Ð»Ô\x001a\x0004Ý\x0011/k¯K(\x0016ÅTÅ²\x0008ûÇmâ	yEæ.Ð¢ÞO¨Ê¥w\x001f½:`b''Ï± ;ÅêJxf¾*5ìYt7½´J\x001bÚ\x0019\x001c¹`TªS-ï1`ÍìM\x0010S2'ª´>f'v¹Wd2©õE>ø
gÿ^e\x000b\x0012ÖRÕ\x0002ÍF6ÃZm¬æv Í­·Ïô\x0001í=ÖÐ|\x0014¶ÓÕpvÊRÕ¤y®s\x0015\x001dü³¿o5ô(ÌïøXÜÓ\x0003t{w¡øWE\x0011ßº\x0012µî{|VK\x0014ÁÑ§³\x0010;-rCõ8ðà'ýõ;ëT½ü½WwZvÿB9»h\x0006ÎÊ¸=@Þ¹\`Á¤çr9\x001dø{v.\x0006½DJ\x0003\x0008*µ\x0008¼L\x0018bÏs\x001c©]4;3i5pÚdÎ\x0014Åhj\x001b©]ãrñ-¿÷æîõÕ
\x001blüÅ\U$Øõ?\x001eêÐ?²ñ@ó;5Ý¾ììPÏ§ö8	­ë\x0014ñåõbñÒÇª«¥0GÚ¼õVøûÿýøÏ<\x0013ü+¶\x0002î!X,õþáöúõõÕZ\x0019ÿ,á-vøßh
U~ãÂÏI\x0017ã\x001d6Ëùì­jK¬Fbµ\x000fw\x001f\x001eèÿvÍÿTÌÛ,Ñü1¿|û\x000fXV[\x0019âåµy÷ê»\x001fô|uÿú"+\x001f¼Q\x000bï(_.âäÞZ\x0014Õycw:
.°ðÿð\x000e\x0008~lÌëùÍR\x001co\x00132ü+àVnÍî
¨Í\x0000ïó<Ý/\x001aúÁÕèî×£ûctßÑ3ä·È¢\x0005Ùr~îQ;Ó»,4ÌÖ^1ÌVwh\x001foáã9\x000båÔÇ§ª>~Ìy\x0013ôÛ\x001f?¼ùy(D?ì&¿ðnª^eÒz7\x0015fðï\x0006br8Õ ¿Æ\x0016µ}EiÒ°\x0012Í\ì.5^vìÙ@^?¿¨EpÜk1s5jè²AsÏ¸M\x001dÚ:l=cfÛ¢Ï?ëküþÚÜz_\}üx}{"Ïp
¿l9ÿ?eðÖufÌNËÊ 2\x0005øõ¹F³ãxÍh½Y\x000fÜÆiM?6ko&åß+äðÝ\x0000\x001e5\x0008É\x0000Qæ\x0000½\x001fï9@·\x001dGv7ç¿\x0016çºÞ +\x001a\x0008&ûhL?Þsîþéü\x0002];\x0001\x001f¯9\x0000ß®9ºePæµÊ< ÜCL<è\x0010ó3\x0005¿F\x000f\x001b:3Lön³Êc\x0002&Ã·\x0017UBg5=)Êx\x001fÑ#½B©s}]AI,ãPg\x00175µE\x001do\x0006@O¿\x001e=\x001f£ç_>^=^~-z°õ\x0008ÿÔ7d#]W\x0015hI\x0008:\x0005µah\x0006O><I!ÃI
\x0015ºjÌ®3C·äÕ	Õ4\x001eÇC³\x000cfaæöèØZõí>(ô¢o·Àøªã5Ð_uÖåqãZ¸¥ì®´2h¿D·\x0004\x001d¿\x001f¾ÁIÌ«g¢KïãiÄþ²Û¾¤¬JB¯¥a$ú\x0014q¨ã¦tñõ¯{/âéº\x000fãéjæâØ*KÑGº2{6S ]ó-\x00105«kõM»:»\x0008À·]äé-\x0007®«\x0012ÖÚÕ0o
Õ5ìñh\x0001v\x0005lT*\x0015"{\x001d\x001bEë¦
ô)~*ß<À\x0006º>=<ûÝõ§g/N77§\x001f\x001e.´8dW	F'´\x0005Í÷á\x000b|ÙÕ\x001dþGÜFi|\x001cÑx56Èç\x001fô\x0002XK7\x00144W´ÑÖE³p|\x001b\x0001<tð\x001cÕ8\x0011O&\x0004D¦\x000cæ\x0015É4¾\x001e\x0001=C«ºgÞJtIÂ Í\x001d5³óùÿáóëï`'ÝÝß]&í\x0011lR ïL-ëît©÷SP­\x0008è1vOÉ9ú\x001d \x0019J¼m	bEijCrHÀK\x0016¨8ÖÂªp\x000bmõè\x0000zêè\x0001Dv	ÝG¤\x0007#ôTèfóB\x0006?^ \x0001Ýô¦MBw¾s9\x0008º~È\x001cýçìL¹­Ñ·\x001b4²hâFM\­cæMüvº=Ú\x001bvA\x001fïP@¯^ûÈ\x000f«"\x001b¤ôfô¤Ñ\x001bý\x0018GtìI°cè<\x0014%xÑ¡%ì¨#FcÒtª>|øþæGÈ/¿8½~wýöö6&SôÜ>ûÿ®\x001e¦yÏ/¼£É]R\x001e[üÎ\x0012Bà\x000cYçwÓ¾Â![®Ó!\ºf7^îÒ\x001dýs\x0006\x0016äszÿñÇÇÅs]Y\x0002º\x0006\x0014×káêÐòõ6\x0019×S\x0004%³Ä7»»OæãKÖL%½6ÛKF\x001eù°27X\x0016Ðz|<Â!m<ã-
à±3e]éàH¥ÉàþWàÖÛÙ\x001dÑ;·{´<ÄÛÇ\x0003sô^®½\x0015=Y)ÀâÑ\x001b;?\x000fß~{õfÈÑÜKæB	ìôØ{5¥¬å\x0011?wÍ§#aÔ&\x001a#¿f¯¨©÷eU¹\x0019L£o9\x0014&ê [öM1\x000fèm~" {@÷@µO+à;+xC7\x001a½ÌÉÜ"àkUjxquuûö4W~¿p\x0013\x0019µ£õn-4ñ\x0018\x0015j¾Ñ6\x0017÷ý©$s}\x001a÷P38½}\x000fyº+:3¶ç.³§¹zÅJA\x000e¶´Ç²ÙÐCOÙ8\x000eÆ@Ð:\x0001\x001a×\x0016§Ã2\x0010²³Þ¿þ^ß\x00159Ý~s÷~\x001e\x0016øÒG_·QçèêzY0x§SNäPJ	åéÜ\x0015ãJ4{ÉyÛVÂØè1.y
nðÍ7*\x0005E¿?H;¶¯ãÐÁku"\x0006Nä\x000bÛÁ¸#yÌ\x0011á§÷\x001c±8íI\x001c\x0002Öªa°Ì
Ó&*ñáã§Û¾~ó\x0016âBÅàS\x001cÅÔj×²UÎÈ§Ç).az*Ncãf*>É=8>ú\x0015g-0çéÂ\x000fï^\x0007uaÿöÝÕýû\x000bùä`©<\x0012íù%I\x0017ª¨"ô·G¢æ>G¼­ó\x0018Á6[ë¾F°¡à{\x0015²®b\x0000¯FÑÉ\x00022Øåó\x0002ìè¹£g\x001ct't×IZyµGe£×øúÛOo\x001fÞ©ÈàÅý\x001dóñ|ºT2Ö\x0005§Ê7Ñ¹5\x0019È÷ZÎ*9£Ry2ËìÆ\x0008­KBæ.åÞIw+	æÍ\x0000t\x001fê¤{!\x0014Jé\x0000ß/Tïsì\x001d_5²V\x0018æz]uª´GÏøÎúñôÊÝégùÏW®o/WL§kG%¼l]\x00151¢åA±ÍFÕ\x0006z¤\x001f'áuPK¯£ÝìÅ\x0005ïM\x001c~E4}£ZÅ\x0003\x001d³ªàm\x00176 :FÞ£LÑ4ï))Np:DO\x000eåR½è¤Lë|[Þ~ÎouæÙýËõL8-½LoM´o±ä¢'Æ·øTOThö«u[ç£_qÖ\x0002ÓJXûêûw7°\x0012ÿõ\x001fÿù×ïþþ/Uçª!)ÍÊbBX\x0003\x001eæX\x0005êÄmæ1\x001a¬V"Oh³zúàWµÀ´\x0012ß\x001f~VâáÛ»ÛÛëÕ\x001c)ÒGo6Íº\x0014Ù\x001eñ#ÇlÄ-x*K\x0011Â\x0003h\x0006cr£f=ü\x0015ç\x000c0­Ä]ýö#g[føBWSPCfÜ¾ú\x001a[Xz~y&Üc<@GÇ¡Ùùf*>\x000e\x001bwÌÑ8÷óç\ð]xûùöøN\x000f,Hx)/ \x000cîÛ2y6 mI««ÄLÂO(%\x001fæt°XO\x0002¤\x000f~ÅY\x000bLëpÿ]N\x001fïu:ìúõÕê"^U®é}ÛmT²¡Ô\x0014Yáï1n£#W,'¡Y¥mª\x001b\x0017QB^¯ÖÀ'-H\x0001eiò³cmC÷[\x000eÛ(\x0003W\x0016Ù¨ÉÀºQÛ7t§ÜBóñõ«÷\x0010[½¸{¸¹º¾Ô\x0013¼Ce\x001b²f
[éÙä+´Õ§ ÑOå¹)Âm¶5îY°_qÖ\x0002Ó*¼ºyõé§oõ9Ûnú²UH.\x0005õ
Á­c.\x001eíám5Ùx\x001f%QKÜ¡XRÿÍTÂ5µ¥þm®PX¨&XÛ§ð¤Y\x0006oy\x0019\x0016ÆcÖ±7)ùhU¸÷&ÓL\x001fsÒWÂ4\x0015k_eÑ	\x0019x\x0000ïÁ\x001a\x001fÚÞcalöê\x000cÇjT¸jYb\x0016@ô.\x0005\x0011-³CÔN·DgÓsÒW\x0011Ú\x0017\x001fº\x0005þ\x000e¾\x001dµ»]X\x0008\x001b«iÓy
Þä1êxsvðMîHæÁ¤À¸\x0003ÝGõz1¸¨ÔñÌ\x0002zîèä\x0016¢]G-iB/HåDèÙ	?±\x001d_Þ
ÿ´V(\x000c\x000fBm!²)^\x0017ÃSÈØ°äm2E\x0002ð)kÚÑ{ÖÔRûìo5±\x0004½Õék\x0015º/¢kÆH\x0006ÀS\x0007§Ë,t³sé\x0006³8\x0004´\x0004.¬3.\x001dn\x0018`ÃÐÕØ\x001eé?åÍþla\x0014÷åÐ(¾@\x0001BÛ%løÅÏ¦G\x001c³{66¶Âp|\x0002"&(G¸ç\x0001¿Û#µ\x0001DúB8¼\Bè\x000b÷¦Ö\x0004Fiã\x001b\x001dÝ\x001a^Gâ\x0004N\x000fÜ§S¬SåûáæÓjY1)%BÏ²ænË\x0008ÑBæoª¦J÷É<ãu|A¹$¯Õ__qÖ\x0002s\x000cÿÿ.¥q!N7w\x0017Z`ò\x0018Yü(®qK¦Â^r[6?åÍxÚ¹ø(Þvð+ÎZ`\x000eáÿô#\x0008.	}8Q\x0010!¿6Ñ\x0017ãv0ÉoI-z]
Ð±×\x001cÝãTñ\x000fZc\x0010/ÆbÇ¤Ï\x001cý³\x0006áêóÃw\x001f½>\x000f¿}ww{u¡*{pQ¥¥ùw­/²+Û{3C.NºÑÌ:ÑClæóÐç+\x000f~Å9\x0003Ì÷ÒÃ÷§ûëa\x001dh\x0019\x001e.5¹V=v×qãÊJ~I24k&ra¥\x0001÷©,«£óÒ¬%ïC¶9ø\x0015g-0×·^4\x0001s¼LRùð\x0003ý\x000b=\x000f¶b~ÓG\x0017¶aXisK\x0003{ØO*¹hÆwºYKÃöN\x001fý³\x0016«\x001e×onVMþÝ\x0003³\x001bñ4ç2\x001fÕaÓs¸µÿXDÔ¥ý\x0008úyUhÊR¸Één\x0006ÉÚÞ¢sð+ÎZ`Z×éÊ©»Æïvº½¾¹¹XÕctÑëÚ\x001dj.¹3ø1ß[x¤V¬£Dã¸\x0014Í`Z"T\x001fµýWÐ)AE:Ï
M*\x0016÷-ÒwS\x0008 ÷\x0016Ba``<UÔñ>E5oC\x0018IùÃã\x001b{?´wÿát{út¹êV4Y\x0005K\x0014Ø®TíäT&lqFú\Ì«ãJ4{É+\x0004sòû¿â¬\x0005ææÇR®~ÑÆ?\¿¹yy¿ð¬9iÞ¾bÝav©·=\x0001à+½¨OÊ\x0011(ã\x0003Ô\x000c%·^¯0îÿ³¿Z\x0001ÿÓÏï¬~þp}uÿæRO6*éìÈßº\x001fÒV\x0015ªÎíj§<æ\x001aÎX3¬Áæíþ³¿}ZüùóÛtÒ+p÷êúµöb³"áË®õ6âô\x0001LÆ&>Çþ1zÊ|±©\x0001¸ÙK7\x0000\x001fý³\x0016c{swûJÇ&ÿru{¹¡
òÜÕ±a\x001bÚ(¬Ø»\x0019s-U\x0006ÉÊëïã,oÖuØåä¡*X1¡¨uÈÉY5ø`?B\x00122+zH[B\x001b÷@ô9WW±Í;g«¨]«ÙãÈùîóçÓõ0óÇ»\x001d/mNj*\x0019Ë×ø¹8È°è\x001fHO¨¯Åq­¤Åh[â£_qÎ\x0000Ó"|ã~¼þ¤]múõóóRéÉÀ\x001blOì\x0015È°²rÔ`ÌBÑÓnöø³\x0013\x001fü³\x0016§~¼7C^ìO\x001cð\*OÌqÊr	mMeT\x0013Ñä¾{­x:\x000b1ºÂÍ\²\x0010½éîàWµÀ|/­z«ÄÝ¥ºÊ3J©¿a\x001b:¥;\x0019úsèû£Ù\x0011È~Ä§ÇX³¬ÂæÑ¯¨"L±­BPüld\x0001Å¹ä«Mmº~ºõ6tk\x0000Ý@Yß³\x0014PUè&+ôRw\x0006½Ýw·7IO\x000füëÃéææR\x0003}¬à_\x0011é+|O\x001bQcd§\x0014óÔÑ\x0005hÖ°³3ö\x001cü³\x0016\x0007î}üö¤\x0013\x0000ÿzw)\x001a\x0014î:ÄãîÏ=ö\x000fFÜº¥¶'
ÜO)èZ"©d\x0011z[åÁ¯8k9îÉéÍöûÏ7,¦p¡eÑi?¥5\x0001M~b\x00021Äº\x0013Oª.V¦ G%­\x0006½wäàWµÀ´\x000céóO¡~«áþt{us¹ø3Ø¨Hþ+è:_C!ÚÂÛ\x0013ò\x0000\x0019W¢ÙKx{çÝþ8ûû§x÷)}óÝ0"4Ó×ü-©\x0015+\x0015EzÞLÚ\x0006¾µØÌcéL»§\x001c]âf.ÑªÚ\â£\x001fqî÷ÏlYW?+§\x000eÄ¿ýýo¯/Ôï\x001dL¬U½P¦÷¡r\x0013ä³\x0017>¦\x001eöT\x0016ÁÈJ%ØV°?ú\x0015g-0-Cµo®¸ÒÇáßïî_¿»»P:&\x0004§TÇ²õ¡ÜBgðtÌ¬Ðþ±úØÓÕì%±úÖÓuô+ÎZ`î¼7wß\x0014H\x0011ÿåá$ª§:Ý_¼Øå\x0014èTò¶%¥U\x0007'
\¯*\x001c\x0015B§²\x001cS¼ì%ª\x001a\x001eþ³¿îcù¡^Ç\x001d\x0006úË/sÃÞ°u}´s	\x00114êrµMõåÉDc7\x0018MÃ÷åàÊä6\x0011ËÂHØÃZÅôS\x0003ã3\x0004Ð±\x001f;¯s¹5I~\x0000¢\x001d©t\x0001Î	·?}wªw\x0007+Í\x001d\x0002<zN\x0011\x0014áÓ_ÍTûe^r ];ëÊ=¢_0®u3ø\x0005¸Ö»?âÜï«Æ&\x0005}	þþþîúRu²d\x001aû·!l¡»Í9\x0002õ¼a\x0019÷Ga\x0005\x000b\x0014êýÛ-¥ï>[\Ð½
\x0019%]=ëîª\x001foEÞ{ìJÛûÔBa$\x0019]ªu-\x000fÀU¸\x0004{\x0017n1m\x0000pÅ®C\x0002ÒùÎH³õ\x0011rïgÌ5Bºb\x0001Jbdã5rÝ»y6ä¨+|rA	\x0001\x0001\x000e\x001aØqñe*÷¯À½\x00197 t]ÄaHÁ&ýÁ2\x00001\x0006N\x001bl\x000f`3K!\x0002FMÿ«ús¹QdÌ\x0012m°\x0005¾\x0016êâôµYÃFÝÞ\x001fÐ£9Æ
·\x0002n\x0019í\x0018zäù%+Dý½¾)\x0015¹g\x0017m¦oÌ°rô\x0003²Z9_\x0019\x0013Ë=èÆ\x0006m\x0001ºà\x0003\x0003\x0016\x0008=\x0015 \x001f\x001d½.·at&ÂòØuÜ=¬þèì\x000c\x000c\x001dAÃ\x0010b\x001b¤\x000eÍú«Ü\x0017\x0013
ë\x0006­	þ\x0002B\x001bÅIìxcÈ7\x001fmf\x000b\x0019u³úæª,mÇ9!ïdNè\x0008\x001a6\x001e]>Ñ¥\x001eÍ05é®§$Öbæ\x0005Ú:á1ñy{Ù¨-Í"K
Ø,È\x0007wu0ÀcAp¡«ÞÓÎ\x0006ýÑ#¦>¸BmÆ+´àM
U·Û:\HmTmê`Û £íA®W«X¾=ÚÜÈI7hÞñj\x0019]zñfrº7¼Ùÿçy a¦3|zvÃ¢×77cËÈNÏÑ\x001dµ\x000eÚ${ê{½VÿHR/ûjDóî\x000c^¿h.\x0014swÕgtÑ}65ê_oâÁeÞ ûeîx\x000eÎög¢Òÿ}Y\x000e§ØnçÛû4_Òû§Ò
\x0014ÞÙ\x0001Ú&{\x0004ÝÍÁ'hã­îb$¡ËÞFu)òüÎÖè oáHÊøÑÃç±Ò1£¿
©%o\x000es\x000c\x0006/yËÊ±?\x000b\x0016þÇ\x000es\x001c\x001dæ\x0014l]¨ÆE«:c-U]\x0016¬Ã²ë1ÇÑc\x000e±Ñ/Èfá3è¤LA5èjels~µãè2s\\x0002\x0013Äü9ÅóP«öbx
x×e£ËÌºõ\x0000û\x0002°"Ù¶t4ò®Ç\x001cG»W\x0002N\x0018zù©T×½!óìºÌqt\x0013Ó÷gX@¤ãCÑ\x000bèwæ8:ÍÌkà½Õ·5
Iî\x0014Ü®ß\x001cG¿;Îqùò2bA[9É°ðÎ\x0018Gÿ'lc¿\x0012\x001d9\x001d¨b\x0011«ÓÍ¾\x001bGÿ\x000c+h¹-Ymº¡ãñ¾\x001bG\x0007©>úuK\x0017\x0015&
¸´µ=Ü¾w\x001bGïÙ-ÜN\x0014\x0005aÌJÆòI\x0003Kä³ãÝÆÑ»¥àæ x]õÇ¡\x0015C\x0000]ôÁïû·qôo\x000fîÔ³÷ñ¾\x001bGÿ\x001fãþú°r5Îcsæ4+d/säGÃY}×õCHÿP2Á]§¤(ð\x0016ä£5ì\x0019%údÞ>óGkä¬E¸
=s¢©}\x0004\x001dá£=^£Æ\x001bÅH\x001f­¶\x0007A[ë>ZC××0\x0004|\x0000\x000c­xö@ å«ÖÐÁ\x001aBMóDÊk&ùQÈÑ4õ\x0003ä.¦F\x0001åÎ*ÊøÍÉ©Î\x001bSèÜò}w´\x0005\x000eb.È\x001bÁ\x0017^]¥º©)/xL3I\x001btTg\x001cÒGäû\x000f×õúÆ³B2P^]<¼¨_¾YÕ£Ë:óõ^JSjE£íåT]<ûêú%\x001faíþ#ÿÀa\x0014Wr|\x001còC:\x0015é\x0017yiÁj/ÍÑÚtÞ#ú\x0005´&\x001e#º XäÙ¶û^Úì\x0000Ùám[\x000cm'¬üX$!4ïù\x0005¸SÓso\x0002pÈp7¯\x00128\x0008e@®9î:i\x000b2Æ\x0016rQÂ\x000cäj©~TúfÑ¯­\x0005¹\x0013­[[!IQè!Jh\x000bÎ¼©=&÷áìð,¸½Üäa,³k¨\x000cV#=ßO\x0015.È]Ò~\x001cºï%#lJº\x0016Ó\x001fÄvp¤j1èH\x0015£\x000cìu\x0016=\x0016·ïD-°}\x001fs£Dïª3¥\x000e#öcãDZrWG\x001b¹;QÎ{PÀ#èèÔ» 7ºv-¡r´»\x001fåU\x000fea©@Ü\x00179¢¡[2ïh/C¨M1\x0010zïbxtv²\x0019y1\x001dxh\x000b2´¨°\x0005h±$O\x001fbÒ\x001fÒA\x0010o >dù"&¾³\x0019¨gR0uß÷[û\x0001t*= ¨ry¹\x0014;,bÙ÷ý\x0016è~R\Ê ÚlDO	ó±ÅêMMqUÞ÷þ\x001at÷þÈkÎÒÈ¼A'¬ð\x0012´/ú\x001cúæí\x001cíj×wuÊmÂx.: ÉäJé­$êØñ,\x0017hØÕµêU\x001cn»¢i\x0016è«EÒ\x001díj×wuæ
\x000bÜ\x001eE7Ïc©£\x0003:æußi] û¶ö\x00149Cµ ñU)eøæ
ê\x00088ý\x001boÇ\x0013^`û>ð=Îú-ûð\x0002
rö,u©G¦ïPô«bÝw\x001btw]ôU}uÑIl³Õ;z\x0015=\x0006É\x0008LÎ«ÚÎ¶Z§q>æÑÆè¼U
ñþg\x001d{´\x001b\x0008ñÈ\x0018¢Íq´]åK¶?Z?\x000fëÇã\x001cðv3Ëúâ\x0014õÇpêÈZ¡\x0003j\x001ae
ø\x0000\x001a|VxBTC;/ì`GÐ}ý8\x0005ÐÕ{¡3Óé|vSÅ:ZÁÐW0Ñ5
+È|TQÝuÇÞ¦"\x0002§¾é\x0006ÝMÍuOHÞ°ö:º9$]
§'M=	H­Ð \x001fissÀäM¸¡\x000e¾AgvâxÜ»¥\x000bAU´WWG&¿R_v9Ëþ8:-\x0001N\x000b­zWbÒ×\x0012íb}ÀÝÎT=}íNØ³\x001b¦ñ¾½\x001c¯\x0008=i(\x001bìMM\x001bg¦X\x0000EÎ>\x000e\x0013[°%¿ \x0001oÆ\x0004<\x000f×÷ýC¾JÞj\x0012Ï,5¢\x0019ï\$³ä¸\x0018­
ýV»$ÜÁýäûÐÎfs*Ï1Ý\x001cÆ¦\x0007[âAêÝ\x000c©w^Iè¨æÙ°ª÷¦\x001c­\x0012|ídH&9£
D%­>ÙGª¤g?õnÔ{æk\x0004ö^ÖeVOÎÖí§ÞÍzÏÁJÛ\x0012\x00148êxpnH½K,³z7Cê=[\x000bUgËåÕ¤¬\x001ct\x0006´õì¤å\x000eD-½V*\x000fåÝÐ`¼Næd\x000fúfE³i\x001d+´ÉÚs§xZÛ9úxt¦\x0015pÓq¹@£ªHm>Èé!§OQÐó\x0002·JP\x001fmtõ+È\x0001ÜKë!­OÛ\x0008\x0019Kéd\x00184vÞF\x0017d8ýüx
ÏUBÁäa\x0011¤ö
\x0006f(\x0018d²-¼À&
\x000c±F«\x0006ÚÔ4wÂÑ\x0005\x001a*`µô&a.4Fi¢Ó¡òØÕ5âÜ£\x0008µ\x0008Ú\x0003ÏÏÐ­\x001a4´òWi)ÌAd× {dÇ.WOÊ-ó§Ø©\x001e::i&ß$X·ó\x0000ÿ7P?\x001aT¯[-9`³¡æQ&
CËÎý\x0017Ø
/pñ\x00067ÁÕÙë8Ê\x0005ï÷_a7¼Â%å.nYùo89OÈÕªMOå~vuA®Qr»!£È2N*Ûå®FR´o÷ßa7¼Ã~>n\x0002+[jò_jæ¸jÿ!vÃC\¼jkôu¤ \x000eê\x0012²=¨»á!.ô@BgýsÕð¤³¶%±wÎ¿\x001b\x001eââU>Ê\x0017«ÛÖ¢ntu¢/¼ó\x000c»á\x0019.\x001eß\x001d\x001fî
$K(	÷a7<Ã=¾z\x0014Që·a$\x0011§»\x001c<ÃnxK0\x001d×§¡ý9ênFNç\x001f¼nx)ùáÑá\x0004zÞémë£Ý{)ÝðRr¦\x0016¼`Ï]j_$âb&ë§Ò
O%µÍl­|á¯®\x0003t8x*ÝðT\x0016z\x0019Àu kA%_6\\x001bÄÇ£§Ò
Oe	SOÑ_­\x000f7ùÂîà©tÃS)Yñ\÷L­â`:Ý|tX,\x001c ¼\x0012æ\x001fQ®yè±\x0007ý\x0000Nçå¡³Øe;X:©ùrkøîè´8<-Aw¢¸qèÖQ¾\x000e\x000f
N7ËWWøê\x0014Æ]­%\x000eLGN\x001b\x0012ò2T8=$Ñ\x0008ÚéXÉ£F\x0006§ÓÍòÕ\x0019V1ÉÖc£YÙO7/Ðx\x0016\x000bv\x0000[VÀ*zï\x0012v?+¼@ÃaeAèÍ¡­¨âh7´\x001bÔ"½ø@å\x0006
ÛBgl
yö:Bñ EÂéÄ°å¤¸\x0000.kU¯rÇVIY\x001eíj\x000f»^Ö
\x0001BL£Ó®¶iÙÐ£]
Ý\x0017äS¢9LvzW{ouçÄ\x000bóG»Úÿz7ìhë)ÎpÛ[¬
÷\x0007\x000eóFU½ädZ÷\x0013Ú\x000bt\x0006í§k\x001dUNª§Ü\x0007Uæ697£]íaWgß\x0001þj;Ü UC\x0017çÝ~®|\¹Éý],§\x001d«S_T\Mh¢\x0017GÐp`(Î\x000bÝ Ejõ\x000e	Ú VÚ;©ø\x0005ºçÉîh\x0010Î8`G)kj4ïfâ1[\x0003\x0018ºBA¶yôG[ÝU4Êí$ù\x0017h\x000b\x001bÄwç>©£Næ¤$\x0005¼ptb\x0002\÷]kP}°ßXÜÄbvÊ\x0007\x000b².=©Í$ûF\x0007[|ï)h/­\x0010áè,\x0006Íßá££n\x000báN´tÊMz\x001b2âz´EÐt79½ª­½&ée9ÚÔ¡Ày*,ÛC)ÊÓ\x001aêF¹\x0014D¹v"I\#´pXÔ«£/n{4,\x001emè\x0000:H¸¹B+wÌGE\x000bo\x0011Ï&\x001eÙ9B
¼h\x000f\x0002~ã\x0010\x0019+s«c\x0018åÃD\x0017±`\x0007kéä¡\x0017IÛCå¶)Êÿ°íÎË»rK¨\x001aåØw\x000fQ\x0012p\x0015t[V\x000eoG±éþ6v©ée\x0017=h¿Ý![TÚÏ!x@ð\x001a¬ºH²STÚÉW«ONÜ?c\x001b¯mC5P\x0012TÎØY}ê\x0015gE²ÃÎ\x001cÿ\x0017\x0019¬ßä²ÎøÛº0ÑüíÞ\x001c\x001eÿoÀH jX¹\x0006¢\x0003öªµÔ\x0013«\x001aîdëöº o®ýáêRÃTÉ»4\x0016îR¿kTg5ö>
×#¶_ª\x001bú Û\x0007Ý\x001f±\x0005áà]øá×\x0007»ª\x001bú m¥ \x001bT©Ø6\x0015QÅ\x001cKGn\x000c;\x000eíIÌ gdõJçZÆ\x0005ÛÏzÙ!ëu°g·Â~zjèWl\x0003Ð>\x001aýHÎiÁ5i,·»\x00072\x0017=AH+ÿvÛ¥6=Iåd·Ñ\x001ds!±ÄîÑÿ\x001ee°Fó(
ü@çB¯rÂÛ¹RÌ¥Þ[ÚôC_zÝç4X{sµ\x0011oµÊ-x+Ó\x00185rL»éé\x0005¹·.pÜékUÞRÒ5béyÙ=J\x000blï+³äò\x001bµYû¥¬Ð¡x¼s°µ ÷~\x0008­
[ê\x00102§ªÄ&§´^{³¤\x0015v_\x001d,ê¢ÉÞïg\x0017Ø\x0002\x001fPë 3"gãµKZòÁ\x0010U¹R\x001emòà\x000e#c\x0007\x0019ei*\x000e®Æ\x001c2Ø\x001eéÑ\x000fVNÿ¹wÛÕëÈ®_ð}:\x001f.[NÜN`\x00078ð­°%1\x0012mìæAq\x001b\x0010×Èí\x0015ç5úMò$ÿUk­\x001a£VÕ@nS´a7ºÙ\x001a¬¯VÕ¬y\x0018sLvc$¬h~ôm,í
ÜmM\x0002ÁV;Ës\x001c\x0013³©ø \x001dû\x001e\x001e\x001eØÀ²V\x0019¢@ñP%hG_1åÐ"Ûìð\x0013º\x0018ºÝ°ì<Z\x0014ÏôØ\x0012nËöó _ä´é+«^¸m-eæ´\x0016ÔW6ãòwÿïýïÿ$víûgß}xÖ¬æ\x0013i\x0006zd«kÛ¹ñ+\x000cØ\x0013	ÏÝo3ÜûVJºÖßFÊµO\x0002_ÂÓKÌ´d«¬\x0006O¿\x001f\x001bùý±:Âmîö\x001d2¢\x0012h&VlÆçZmã \x0002Â\x000c&7×&»~­ÚsH©\x001c¨«^Lë\x0014{ºn§çûW²¯?¼xÿædc)TfÌì©b#]Vß¤	HLü¯Ó6\x001c\x0001\x001dqöTîÐ\x0013e r;¤Î`ß!\x0003YÅ\x0016ô÷RÊB¦pJÈVí49\x0002VÕIP£N\x0002\x001aÆMêF%®}4ù\x0002V^dA\x0011d"\x001c8\x0005´ö\x0005Òä\x000b´öò\x000c'EVdüÆZ¹\x0015jË\x0014,¤J&_À&V²É Æ£\x0014 ¸ÂQG\x0006¢÷Hr{J×T,dSg´\x0010\x0013\x001c
y\x001e,íZ[kå¼IhÞçBl¦\x0003*EÌ7#¡z§6E\x001a>ÎµUmVAÝ\x0001nM0#¤kNtµpãs<zµw\x0007\x001aÉW\x001fw	\x0017%å\x0003\x001aN´È$Îâ\x0018|Cf\x0005DÓ(+1¢\x000e=´lm't(Ü	,\x0017:%@ß\x000fè­þ\x0012P5q|\x001bM\x0013\x0003[\x0014~\x000fh8zÎ"ÉEM¶£Ï\x0018Ë\x0004ííº<Û¡¡<\x000c<Æ\x001d:Ò}Zº\x0004Ú¯k¨\x00074tóa¢ÃW) \x001a\x0004\x0013r\×9\x000fäq@bA¾iv¬tTJÍ
y÷\x0011¡Ì¹y\x001c\x001f}X×%Ã\x000e
%Cq)(¡ix¨ã¼Ñ¡ßÄÍ¢-T±´"yzµ\x001cÙé0]ÅÜÅ\x0016iù\x001dðè¥1\x000bXVíy¾ÐMüBKHí.nvÄBbþÔ\x000e<±Y®cg¾SN\x0017iù\x0003\x0018ÌOøØê-O
\x0008w	÷\x00167Ùó\x001d6*£x,ß+6íu¹Awfèî;BÖ?¡ÑnºãÁb¿ycªõ\x000fÑ³dÌ$\x00133\x001b½PÚù«Øêt\x0012¸5[N[h»YlD\x0007éµ=¹'åO
Iyíg­¸1o»N\x001b³$×)¨,~÷·O%¤¬KºÀîÚ#¸ÁôË{[T+ýä¾æ±½Úg3©\x001aÆ Ô©\x0014¬°ÜW\x0015i\x000eã>ITÀ\x0015\x0011-ÁÒ¶V.Zð\x0006üä¾ê¸l\x001fa×-
ÍH6³bxëó¤eÖÁ¾hï2\x0000íÔ½íz6kÁ\x001aðû39l^NK:{\x0013[ÊÖµDç\x0001\x0012Ë#øØé]\x0013-ýä½æXq½(\x001a"3ôrÜ4ÞÇIÔMN\Dr×Î=n°a{è¼Éª×¡#Cø<6ø'9ØÌ*\x0011VÝP8ýäoç\x0004¸9?6E³lí\x000e»Ký\x0008ÞÐfÄ©m
Ç¥¶?ð»£DH9»v «~\x000f3`h~ lsê~ÉîÈ¡×ªÂÀgjÚ_Äû\x001cï)·ßõÀÿL¹½yÿòÝ»\x0017?í{ú¤8{üt§kN
Z>\x001fE±\zWðç7à¥qá~Q~]6m2àA,	:ãÅübÌst\x0012Rq\x0017ò8AIeà]ÔÊ:Dy\x0010\x001d³_õh]È\x0005ÖpÅ9R\x0013%³2hì¡ül³.`NÂþhËÒ
r\x000c&Ñ¹¬\x0013\x0016LV0ÐÑí
HiåWÛ7«rá §\x0016*-q`ÂTVÌ¶[{VWQü\x0005
ÇB¬w D;hÃíãÍº á\È÷tà°)P\x0002­)py\x0015Ã_À\x000f\x001c:~Ú8\x000b¿î º \x0013AÃC½!sÈz8÷óÃ~!\x0010ç\x001aµIT\x0000âOßp1FM3Ò÷ôñÓO-
,\x0011cJ°W\x001dYâð+öÖn-ÛìÈb	\x0017}êy*#@é6¯-©¶LÔ[+´Ð(És\x0019¹XªÊ¦ÄÙãl(Ç«\x001cX»Ì\x001e\x001fÈþS×¼èÏ\,	äÚÂ©¥\x0014\x0002\x0017fKo:YEdveÅ\x001fsxPäý¡¦à\x0018*WëÃÎëÈ ¤¢¡À`\x0013o\x001d­<5#UÖÍ\x001b\x00074èîpæÀUÖ¾K»3­ueÓcq@Ú©wÚ¯ÅÓ¢jr©,Ù¢l×Z0
\x001a§pIÐ\x0004°Z]&è§næÒò\x001dË\x0000ÿ<!T<Õ~O\x001fsò\x0012#+Ø\x0016ß¸»þ\x0011|ÏøÚV%r\x0010\x0018Na¼OÖE×uüêáÝ»Má©ìcÌ`ôõ\x001aÔ\x0018\x001f &\x0014@ñåHì-b:ÕÀTå:Ã\x0010¦\x0015\x001cËe\x0005¿®S\x001d¸À;M<Ãx\x0016re¾·ë8¿²	s6î½¦Y­Åê|mÆ"6ªS¯=
8êDVL=\x001e\x0015iò^(¿N¦Ñ&Ò\x001ajiÅ9Qdä»²ë"æªË\
*è&\x0013Ø|yã§%Ûuê\x0000\x0006Õ0	9Á\x0007\x0015wvR3¬Äà y\x0011é×Ém.Gÿëµèi<·\x001c^ÝXúuz)d\x001d;~\x001aóQ2W]}'Ã®Bý:9åªB\x0003¢4éÖÏàç­Þiá\x001dÐ@\x0014kñ¦TO~J§´k{¬«D1Ø\x000f-\x001c\x00107ÈGÇ`ÓË_»\x0007Ñ~u\x0001u
ZtâN§ù¶]\x000bajTUR`\x001aMS«D\x0007[ìjT\x00074|Å\x0010iLªÑ°Ú3ÚôâÕ©FU\x0013)ÿjM®b°ÓØÎ£]õâÕ©HõQ\x0016zÕ×á\x001b\x0016¦\x0012DËü÷\x0010¦o(~é¦a®rõ«	·"ÿ!\x001anÈk\x001a\x0012ÔÄ:V­g\x001d\x001adP3¹òs\x0012\x0013Ûä6ía\x001d\x0019J&Ñu4
\x000f;mæoØ®Ëª\x001dªA\x0007 *iÉ$Ñ\x001dÇí3==­pÕ²Ô!
Y: ú.¾¢\x000c\x0014¨\x0018¡ì\x001a\x000bOHH·¶x¿é+êÈ°Ñt~bú¬Ò¤Ýïs\x001b³ê+êÐÀ\x000fU¹KØT&:$8\x0005º±+VE
:Â7¬n°!«ü¥ì\x001fäif«q×WÔ1Ä<DT\x001e\x000e\x0007,ìëc»,òå<¾¡xYðiù^Rÿô,,êRWx\(À5l\x0007
pÆRñ"¥IÝ7d®ËØâ_·êêØ`óÁêycDPjÊd¨ûDuãÌñ%)\x0006­ÁÂnT"1G¬ÐµK£{¿ý_¿\x0007÷©àu\x000fÙ­Åé¨4eè\x0016mK'øÃ\x0000×\x0006røÊZ£³lõ¦g\x0007Ü·{ôoáG<1ªé;~\x0014|hþutßìÑ¿\x0019kO\x0005G3\x0004½ù^,¿\x000bN\¶U^¬ÌÕ]m¯øÄzO×O4ÙújÒð`ãè0Ô\x0002{\x0013ô\x001bP*Òé¯H\x0015NY/\x000bì\x0003\x001dy\x0012(8i¾^ë\x000e\x0003\x0019ä\x000e"{&?\x0019\x001cÇêç¡\x0013®\x0016Úºe'kÆ\x0016¨lû
\x001flrÀk]\x0017\x000fdÐ\x001d\x0012d\x0003ñÁB¬£¥s\x0007ý2¢<Á)U	Òíaòü¤J\x0013{ÛÖ"qU8¤´Úô\x001fP\x0005_hÍÙN®]+å\x001dÈèØ'Ô#È!±\x0014*!qº}\x0019Q\x001e¸,Î®·\x0006\x000f0GØ\x000b&\x000bÑö2EUl\x0014Ä"*zÊKfJA\x001f4¶»%P9ÖîG\x001c\x000büÔÙÊi*­~u8y@cÛ]@\x000f(Ë3\x001d\x0011ZÂ\x0005®\x000f$¿É; =\x001dBî1÷°åyþb«³»($ÐSÑ·RVoàýÈ\x0013ôn¸ã\x0001
ç9;¤\x0014é\x0004FJiº:ÑLýtì\x000e\x001eÝDO\x001cÐdØ<V´vEÝV£¶K-\x0004íêÔjîr\x0012moËÜí5\x000c©=À(GxÚ-GS"X)swdPª°ä\x0012*£3\x0019aâÄú>þf·Õ À¢­÷èÊsÓÜ¦\x001aýfFMG\x0006êIû1§Y%%MÅü#TÝ}D\x000fÊ\x000c>\x0013Q31ýX¬\x0007¿±\x000f\x0014\©
whøÁ\x0013½TËiÕÅOUø>Áu1[§a[­£Ã4\x0012\x001b'¡gÉ"1N\x001d{ó\x0006è\x001f\x000c÷ \x0002ýAâ¼çLHgÚö»¸±{ú\x0007\x0017²*Ö!tâö=y\x0000ùÝêóàd'wØ\\x000c¬
\x0013&=Ã4e»zÿ¥8¼;l4}\x0011Ée*ÙMÊ´®Lëîr×Îl¾¤3o
\x0018Ðj/xi&Ò~íÐe;,÷qQ>I>%+t\x0004YþÌÆ·qäÛÄö°\×ÆÌ~ÂLpvË\x0001Iixò¿ûðZ_qèÈwo
Pçýéy£3Îq=Éö\x0005;ñéæÄWrµYp*)Ôº©jwT%ÄG^\x001b"EæË\x0004cÖ\x0002Ú\x00070
¡\x0015,j·D\x0015]!n%5§ô@F\x001d4"[Ä:ûi\{\x0016d»)§94\x00084î/VsS×`äRÖ"\x0006\x00072JwÖ-¹R`eU<
±ð¹¬E´\x000fd\x0014$$ò@Ô±áÓ¹\x0008RÂº÷ú@FõÎ\x0002¥No¤)Ù.ä)k×(ü\x000b¿!Í±A Ù
º\x0019S8Êµr7â\x001d\x0019M>6\x0013¤ÖÈ¸ºÀ9*\x001f·´4G\x0007ºÏiÌ³~çIeSl: \x001d½íø	5ûE;íÙò®!YE\x0007i\x000e4\x0006»âóô\x00119;\x001azïÙî\x0012¢0¨2¹y£év\x0007îj;7zw	-ëçB;TrFJ\x0011'hßLÒj¢S[¨\x0000\x001ci'õNnCnnö*¢IsDã+ò?¢7S¼\x001bØcõéî\x001e¢0¨+Ø\x0017­ìç\x0001*:©z\x0013,¥9XÒ^<4\x0010¦9²ÞuÝïÝMDaPG#Í£±¢¤i:\x0005«9T\x001d¬A\x0013ºÎº SüïMv\x0017\x0011uAz\x0004©ÖR¦íàÙÖÕ´Ñ\x0005= ÙÇÌ¼rløè±Ö³º\x001dÓ\x0014;*4<ábiv¥B³|s®±»/(\x000bê\x000cdÔ~\x0003ì\x0007s1]çè®ÂÒ4¥z>ÀJ¸Â}Ír>x«S³y:ç\x0001
÷\x0007'T¦ûbIFGÇl$G\x000fèJ[
®Î-ÓWä
9\x0006Fí.\x000cjZbH<»Geë\x0018:7uït¯!Î\x0007êªqÊL|ÇÖ\x0016ºw?Ô\0°\x0016üÔg_½xõìw/ß>\x000f\x001f+O6Åh\q´\x001cb0Uü\x00135¹þë¯\x0010öØ©ÚA2rÏE»	9\x001eÖdüõ9¤u">N\x001cRÄÀ\x0016\x00109Òî\êÒ\x000bt^lÇgQSÌ»\x001d¹·H'©r»¥\x0013rÞ0°òä\x0014ë\x0018óë¢ê\x0003ê«Te£ÙÉìÐÔ\x001a¿<*\x001e³
'OOò`\x0003Tô³<\x0012"°Vr.°"ðäÉ?I:x\x0003&ÍÐ<¹;g»k×É\x0013¡M³\x000e6äà7\x00014µ/I\x0008\x0007.Øc¹\x0019J\x001e\x001bÅ\x0017ô\x001cCòT
kV5¾´±õðì\x000f\x000fï\x001f¾ýá©R\x0004òî²Út
\x0017·³XxüÛh¨ýZò{l\x0014Hü3ºYRÜ:\x0007i&Hó -UÄâ¿\x0010ëÂ£.å¸¥áJó ­"·\x001eÆ\x001e9'ÍL\x0017yòv\x0008ë\x0012bGméÍA\x001c*LãÈµ´5Í\x000c/ëñ\x0013i\x0002åtb\x0010¸\x0001Êo¦¼X.&47>Ë"ÊLÓ¤¦Ý\x0019|ôü®MbG5©º/\x000eE°ÅUN?aÓ^©L£
1á¨&ñ6\x0012ú.q\x0012¬+\x0000±R\x000bf5µ)Ø~lN²$XYXW,}^[Û4
TrÆ;ônMê
\x000ecÕºqMµ=¢_6Î\x001fWÅZ?æ:.¼.Èþç\x001fÿøðîÝi\x001bÿþáíû7¯t\x0006¡çÔm\x001d\x0011Ç\x0013+z¨^\x0015\x001a\x000bó²_Á}sÚ²
wùÂ&1Ó´\x0017»\x0017Î×ëLbZ`2²÷ó¨2Ïq£Mv3.pÎu¦B:<>\x001a¶a\x00128M#tìfLÑëLÍ÷\x0004¦\x0005;.ªg²öéæD§xàR©8\x0005O\x000b:\x0005¨Í_¸\x0019
ºV¦èÜ§2í²Ú¤»ÐEX°¬m\x0008IE¸ñl¨\x0014:m´å|Xê°ªo»\x0017óN}¯_<|ø§º¥¿ºòkÇ.Ñ¨PU\x000f¿I¡Ãºú«ÔC$KßYi4,¦§^[ç7vaº§ªÚDb#ô\x0003e³¦RxKï/²¡aº¦§\x0006
,fóYÇEYòú\x001eÈ s¡ÕB@Îi\x001e(ÈHc\x001b²Èíé¢ªÒJÁ%IÃ3u+º´\x0016i;q )k\x001e2³¬È/¡k\x000bë\x00160U$òAàÚ=e³Mu\x0013- oèJa*Iè$i °ëLb¤Æ:H¹l¤.:4J]XRHsþÓ©ëµäUM"L5Í]ÔNlj\x0012a\x000e u®\x0004F\x000f\x0013í~îIMÎn¼Å\x0003zÜÂ\x0018©ñªÊª±Á3äiÕ¹³$vg\x001aãçÀÈÕNI\x0010\x001e¡ª×v3ëF¥,ë$±\x0002iãÊù`\x0019Æ#|^eÊÃ)×Êh\x0019ÀÉQ;\x0012t<írxi³\x001fú\x0007h<PàÜ§i®gæ£÷\x0019\x0016¾nn¹þÁHe\x0019ìE­¦÷Ò\x0006ÇãÜó	\x000bR\x000e J¦\x0003Q\x0011!G®\x000fÄ¶\x0014z\x0010´ôÌÏKCy\x001bÓ
\x0016*rmÚ°Ðºª9¬Úõ\x0013h\ùg÷ðÓ§ÊJTÆþxñ/Ä!X¡íEå/E.x\x0011Îã\x0008
iÄR¦ÚuMSí:¯CÿYµDw\x00064óZ
;%íT»ëB~§\x0011Âý7Ù\x0011_ÂOlùìV\x00032,³í|öß¿}ùÓË'Òº\x0000©L÷:\x000eæÈ£ÅÅßÍî7\x000b"Ìýý°ÓPXÛ
\x0016U\x0012ÈY§ÄØÐY\x001awgËN£[?\x0016ù~lì4ºU\x001eÇHs7åòÄWì¹ôÙ­wci§\x0019«Î&j\x0017Ôâ\x0017y[)su8\x001es²ï/F¡:'Î&ò]\x00106¾Ì|×7h;MCÝÂGOð:cd§¥Î©Ê3¼y\x0003Ð<ßM}|ÚÂ½°ÓXQç0=¯>Ñ4\x001f+O\x001dP©'¹»r¶ÏmÄ&£04©L¶S3b\x000c®çç7­0\x000eÇÄM±Sz"ñD9\x001dj»ªþþBÏB}÷æÉfpGÃR
¥=J*nÕ³ßÄt\x0005\x0016\x0019¨Ã^9´uòì \x000b@³êäÙLeØÔµ\x0016îzåÔPÐó-%0Ë{êüN-J\\x0004¶\x001fRgbx\x000e×T\x0002é
bJa3~£#q1ÔUeÍ1·l@\x0017&=å\x0014WR\x0017ù)ý//>¼{Õ'ðüãËW¯P6iJIÔj\x0007Ë^êOÚßBt_ó7õ~~Ü,_5ÆHÁp}'Xz\x0014\x0017yÍ©t³Ì|©½Ùìzùºlàð,GN±49{Ìîfeõ\x0016Î82k\x0014Ý¸Y@.lª0\x001d\x0019¹~×,h\x001e²]ü:ÙÖ\x0014\x0019\x0016l\x001d­õAª\x0014Ü\x0010;E'\x0002/°èïØ8¦u}\x000e\x001f;Â÷)(\x000e9Ú÷âÙß>|xÿì÷\x001fä2ýùin7<E]Þ§tÄ4¡\x0006\x0015ñ\x0018fA\x0019Ío"¦»iòì}ã\x001aßFÿàü
Ñ;P]× 
K\x0012ÃÓwpòÚ7\x001aÙmFÏ]\x00076\x001adñ*#)û>	 %Æo´©Ût\x0003úÑ\x0013ª«9JmMà\x001dÉ³nÒÇ\x0013÷ÐÇÅñ± Åüw\x000fÏ\x000eÿWo>üéÃË×/ÿòj\x001c
ãã$,GÇ¿E¥\x000eÃ5)9ûe\x001d#ËÞ|#û¦\x0019+{#¿ABMs\x0011MtÒ\x0007|D-r'¦ëÊ\x0017sòæÎ\x0017t18H'É§}\x000e6Y\x000bVv¶t)»t?ü\x0007t\x0001è\x000có5Ò¦tg«²!v´nUHIsüáÙñöíCÚåªZòÜbq`dÂ|³NLùm\x0018!:Öõ~B\p\x0015ó\x001fá¬ü,\x001aå,÷C6ÞiX¤\x0017;tb½!d\x0015&ÇJ}~\x0012#	\x0012´Ü
÷h0´ZöâýË÷ªìööÃ_¼}*Y·\x0018se6YÓkì¿ÄKü	ãÂ\x0014\x0013\x0007ný¡}¹ÝiÙ5½xe$dµà7$ËäXÉÑ\x0012©W·n3\x0006\x000eì3\x0006l\x001c2îJ§K\x00136gdµB·\x001c\x000c{Óqx§\x001c·o^¿~BGÝfVH²VÃòÃû*]¸ê¤dØÆ~})!äÄP&O=×\\x0003gEý:\x0018äG®¹\x00067É\x0005U­\x0005	ËT¦^\x0011ÃÑ©©eCô\x0011Äs\x0018\x0003\x0011« ñ9\x001a¹uF\x00016ûr+Ü\x0017SFíµêÄöMþÌ«ÎKqÉ8\x001fMMmü|nyr^<û\x0007ùÿïýÍË·?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-15.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-15.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¾úêéÇÿ"ÿðó_\x001fþôt7Wiyúr\x0003æ^ë»ôm©\x0000fÖwßÇà´m^×¿6®æÝ¿½bpk©!.ÔiD"òN÷8ûJWóöïj|:\x000bê0EëYÎÂþª9\x001d\x0007\x000b\x0019hçqb±wó@õ-Ïöò8'¤«y£wõfM \x001808Õ-ÈFdw¸\x000b\x0018zqåí\x0008>*åGÓ<\x0002º¥u×\x0014s!C+îhØù 2äÜå;\x0007@ì¾¿Ü\x0005\x001aÛÀ5éyìW}Z\x0013cn´h
j~\x0016t!ÃÚH\x0001}ü6c\x000búù$lÔÝgé>\x0016ª\x00001Q-a*BËÃ½#cöU\x0012\x0017ôqY`,"L+«ÄF<\x001fa\x000böÏ)Ö\x0005
ëC\x0019\x0006P\x0002¬Ænad¹(5\x000f7îZÐ°@ä\x0005Ð½²»À0ÕË]óÌ4º c¯¶D¡`¹GääBÙî¸3Ñh!'Bê\x001ciéµ3½»F\x000b\x001a\x001aª{@\x00122ÇP­K\x00165½$r-»·è­\x0008D#mË*Ç~ÀÜÌtåK¿Í¬í,¸ ±á¾¢^W.Ój=0e³æâ;Ì-hè/\x0017\x000fp\x0014õÝYiU£©ö]tV`¼@\x0002£ºNr\x0016i/É¡vÝéÇg\x0005
Ýüòð4K\x001fÑ\x0018ÚÊ\x0004¥-Ø¼µø@Ü±Ë©\x001fQ¨\x001ah3Õc£V}ñ\x00162HTt2\x0005S\x0016.	\x0012Ë=Åò]Ûè,\x001b¹ Q¢¢£Í¨æ%\x0006A7f!×¾-ë³åÞ\x0006ÐGjcqò¨W÷\x001cþ­
QueB§ ×6\x0000oýVLÉ	9¯é¬§ø^âw6@\x0019½$Ú{2oÿ
Ú\x001b1àGãGÇÒÁ{Øþ×·o\x001f%¶½×Ë¶TÎÈ2®¡lÿ\x0006ÒM#ì\x001e=/ÑVßÂ§dùúée[s åT-Sâ:­YÁmì§w­Üµ$}®Ñ'ug4£ª[»ÛÑOïÚ"CÜÓ
Gd	&ï]ÛOïZY"ñTyZ%)Ã¨n¼¡=#\x0014ØP\x0012l
>Òå æÉØEeÎ6\x0014§\x0017³ìN`V´í\x0014&Þrã@En^·çs!\x0003;\îÈ\x000c¸òdåÏºÛ\x0002¿Â=\x0013Ü\x0014=©Fe¾)T~Ù­\x0008]¡Ù!Bðv
N³\x001e\x000cím\x00162´$´¢ø]\x001bw¨s ð\x001d´z\Ùëzf®ìEOïº["¸eðy\x0018vË¾Î\x000bs;:q5½ùØ²q6H»Mop®\x0008ÿ\x0019 ï¦^ÓÞ±\x0002ÝÍS1­jOtm·ûöáù\x00079Ó¿¿Wßj5Ó9Â¿«³müÏVT{#=}RáF¦Ì°\x0012´Uýè.¯5¹fÞ
\x0007ÝµéY¸GY4h\x000b(¸½k³v"ÜÂª£¸©Ê\x0016+
ÃÍ¼\x0016K-u¼Å¥Nghx·>çÇVô0,<\x0001®ànÞT ©\x0011.H}·=vÂ;CÂ«rþa¶\¥ýQMÇÝ\x001bòW
\x000bO;TÞ]»%ÚgýÑ¹\x001déÎCË°ðdÌ\x0011õéTi3\x0011ræf°±§wéâ­S"C¨K<NÇ¨1ß\x00105¹@\x001f·EÅ@\x0017:s»\x001aÕ¥á«ê-èLóìr{Øù`kóØýF³\x0005
ë.¢SFWÍQL\x0010J\x000cÃ¡ÄÈÕK¿±¥òxøÓ»§ç;UÆk Å$ÕQ!/øú-î5Û 
ð)Nh2[¶6®ª\x000fP£¦FI)$[Íí§X¸ù×á:a#íå¿\x0007¯Úw"ÑQbf%4öôÃì5\x0012L²¸\x001az:Tã-[J7æXu¸¤<ó\x000b«ä£+ÌßùÑÈ\x0019i¡\x0017f¹å¾µ)\x001cÈ\rKcÞè¦XÈÇ÷«sl7×niËØ\x001eÐÞæÚ\x0004á°ú-Ö|õöûçÿòêëÇç><ÝK\x0019(ÊâaéÅÍÎ\x000eÎF¥¾\x000c7ó\x0013k4ÁÖhÆæë\x000b1Aa\x0007Q\x001c\x0005íÁÊF`K4òíØÏÙ%¼\x001a\x001bØäF\x000e]ò­Ð\x000cõG\x0007®c\x000fÄITd¾ëFM.?s!\x0017@nØ£Ürê¦1ÓkÌá6#\x0004[û\x0019JË8æÈm2%p«¯¼©]\x001b`?Û4Ýý¥ïÇB;3l\x0008§3k!w
X\x0018\x0013Û·É(¼0|má\x0005<\x0001xÒÝ<MÏP1öÏ£ô\x001b¬\x0018[U{* \x0003¯Å\x000cÍ\x0018¬=øN	>\x001f\x000bùØ'ÚNÒp\x001b·iJÞÌ³Ï·±õª¡-½0æ:Í\x0017L¦;Y>quÏÙ`ëUC;U )ÏOÌÔÄ`Ó\x001e£n"\x000f\x000eÇÖ«FPÏûI\x0011'µ\x0019%ý>oµ°a¯¨ÿ\x001dÌ´\x0004\x001d
ÜÒ ûðÝÒ\x0017tÃ.bN¸Éoà5\x001dY/[?|\x0006­
UI8Lðä\x001b\x0005Ä+ºçÝÜ÷Öf°Y\x001aU«¶OXé\x0013æä|Âs-Ø\x0012ÛØ\x0004[`ÈZ\x0006¢½Â¯\x001e·lÛY\x000ey!ã¥\x00122Ï%Ö$n2Ê{<û/è\x000cÐÞPr_QÃdam\x0003u\øoéøBu§Âpv´U\x000eéÀsò:Û2\x0002·Ö]£Ts\x000bðÐÑ,Îôä^Zí0p\x000blÁ\x0016Ø$\x0002AýÔÞ\x0012ù\x0003Eu´¤ùè;\x0007û\\x0005\x000b¶
6Ôp\x000bVFFÝX¬CµÝR°\x0005¥Ï<<Îõ¤`ëIrÒu¨l\¾\x0000öìÄ­Àvë#fèî\x00199'Ûv¡^ëÊOÊm¿\x001bºm(zóôøêw\x000fÿööáNtku\x0005 Ö8êÑªüÐÕûòe\x0004?Q(K¦Ë¤í¢ü¦#üÓb=7ahK2þú$G¦ÛPÔO
EÊä>\x0014¼\x001d`c²2lÞÚs;C·
Ej½z4-'ËÙöÉòÉixÎÝ\x000cýÔR\x0014â_\x001bòçÈ U_h2´ÿÚí(ê¶£(¦\x000e¤¢¡¶\x0004<d¦vÈ±ÛÜÌÝBöÙýî#¥i$+À|ÛBÇ	ÄÔåÉ, Ld¥"7+¿¹p¢HÙQ9÷+÷m
®Å\x001c««¾·AçØÝ\x001fÝÉ~CQ·
EjPytü\x000e5CÛ\x0000Uì¦.(-yù\x001dEÝv\x0014)cöø~\x001aø Ë\x001aZÐlÄ¶y\x001d8\x001dEýÔQT [<{Ç"Çì|©ViÍo(ê¶¡(\x0006ô¤\x001b\x0012¬«Qgïê\x0012o¸Û.`h'\x0002ýk]'Hbëls£\x00047üÆºm%R#\x0000hb#íÂÝ1ì$¶[û\x000fDU\x000eüø|Q¥ÜYÿ¬*²åÝðz!Hå$!Ù(r×Aúe¹\x0018A;~cÝ×®æ¡R4ÔS\x001aÂz§ú» Ã°\x00174(`Ê1\x0001!Ã,Hëò\x0000áÝ\x001dÚôIl\x0017hð\x001bS2ùÑ¢º\x0005k \x001bOD'Ýe±-hØ**Ô	\x0013"ë?#WáKÙ·\x0005YÐÇV{l2ë¬õ/3Í­újY\x000b\x0019\x0014î[Á\x0017vÖ247#°òIl\x000b\x001a\x0014\x000eZ@\x0013Õx¦2E3M»>ËhvA>f\x001b2T)Æ4Ú	gKØo}Ã\x000cÂòù}4³òdÌSØÍÜÎ\x0011öo(aÑ!ëÚÕ\x0008ºÒVd_\x0005µóU\x000bºÑòÀþZ½
x}p­pÖRo\x0011«®ëÚ\x001cµ»ãP5Ú\x0004
\x001dÖrZrÃT/=¼M\x0007\x0017o¾~|óW_Ý«z#1÷sÖíq±ÿ\x0006CºÍ\x001aµ~Ñ¢ñ2]&Òn3\x0012/T"
v¦¼YKß_È`/:I§)W#'Q\x0003SáëÎw:\x001b´»¶2Â´\x001b®ó¨uteÌ7:\x001b´©\x0008N=¹\x0007:ËG\x000b©X\x001bj/äã®ßX~@m\$efèeK;ÅÚ½
ìuÎ±PuÔÉÒx5d7Ô^È`-*'9d\x00167~\x0015ÎF\x001d}»\x00137V¾bm9º\x0001\x001dºF3Å\x0018ÙÕM:_`ÁUtR@¥$g|)	2jöTö"<Þ¿úì§E½ù¯Ï\x001fþíñù^Ä8+§\x0012¶\x001aû^Ùn»ÌòÊB(íe¤®?Í¢H¦\x0015Y\x0008\x0001U0´ÊM±]_üã£[rZÈ×c¥öL­|UËqxo¤ÁçuO[{ÆYþ-\x0007üIÿè÷òN\x0005|\x0010o:uÜÕ7ò1â\x001aMâØï6ZÀ\x0007\x0001BËµ9ÂÛFJ:ll\x0005{
®üÕB>7
\x0005íFU¦\x0006#\x000b¹¼MÍU¿Z¸\x0007ï¦
i\x001d
Vú	nÞi²@\x0007|¸ê\x0017u²Û´|9´«ÕwÈæéþyÓà\x0018dFór¯J¾¢r_ÁÕ±6d÷å¾ ã¯\x001có­e|¼å\x0018Î ÒWGæh3F\x0005în[³q<¡>oÈç·È\x0002>qi\x0011ëÓJ¦CÊ(fOä1F;\x0005ß>üù^Ò\x00193\x00103oåøJº© \x0005qØ®ä/ 4\x001aß\x0005ûO\x000eÑÔ¹Áðôósq\x001bÆ\x0017òA¬OÚï\x0001}2kS\x000eVÓÕ=Ý«`\x0001g\x0018rÇö\x001dã\x001bVÌ«òÐôÙG\x0017d\x0010G×7ë\x0001\x001cØx[­vÀÆ;<s%/À\x000c\x0012ÃQ²xÙ£)ÇÝJÉëSYàDjÖ¿\x0000U°å«RP2J@9lÑSÁ¾N\x000bÓ²?cjÎò¶ôò÷o^ýíóãû÷\x000fo¸Wð\x001b»HÈèúõºUß<§_È¨ä\x0013iÓÙÖ_êÖÆ\x000c\x0015GµæÃô}f;\x0011ù×}£\x0012[~Ñ&:4Ö¢ ÞÔyò"\x001d!¸´él«/U[k¡YÞ\1ïÀT¤´_Ï²¶úrës~t)xgA¶å\x0017\x0019sGÏp}Ge~zýé}Ö[´ÕÚGÁRôÈì^\x000b{;ÌîLÚÚKÕNÏ\x0004¬T9Ó)\x001aqßºjÏ:¶úRµ\x0007\x0003êÐê\x000bÇÈ,1\Bn\x0008mõ¥ªAãá|¨5\x0000-r\x000b¬\x0004\x0016_"É¶D¢m¬Ø­;Ò ©\x001b[eVVÛ.n­f Mo\x000bwìMÁ0\x0017F0v_:ÛCU[P\x0008;e©Rï²\x001cÁ§YÃÎó\x0019;óoN½¿}øîÝïÞÞ«Õ0»»ÔÞ¯\x0017E#¶º<%7zÄ\x0017û<ù2!þã\x000b'{ÊgÝõáGD\x000b\x0018
6*f@Ò\x000c\x00019ó%ZFòM|/ÈùW\x000eù|¾^Á¸C^ð\x001d<\x001a;;\x0014ö*}¸bb\x000b\x0018B-\x000e¡±¶\x001b-lüÚKóSn\x000b¹ÑAÖBÞ±¦\x0003ûDKÏ.\x001ds\x0001C£¡¼W >ÉCºô\x0015wÅtßÈ\x000b\x0019\hJÆæ$g×$äTÌã
³Ý\x001d\x001aT>äß%õùÎîr'ç\x0015ç\x001bÆJ\x0017hö\x0001½Ö8$\x001361²û]¸¸æ\x0012T¿TÐ\x0017s6næuûÔñ\x0005\x0019\x0006ò¨O:·\x0016\x001as½\x0004}ëû¡PÙ\x0019\x0014\x000bX³`dP¹Ö£Â7¢ïëN1\x0006+ÿóûût3Ä\x00007ÃßË<|ÐÜé7\x000f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-26.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-26.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ýåB\x000b²Dp\x0019ît&\x001cQÙÃL
©±X]ë\x001c\x001fÞy@òê^Ú\x000cÍ\x0016.Ï\x0016
þçÛÇïHW~q÷×ÛKÊ»\x0010ðÕÍi\x0017«\x000ckg\x000e¿]±ë£xÐÓøÕ\x0017½¸\x001b\x001a\x0013HÐüññ¾¡gõñðá\x0003}ÿû\x000b
\x000fðnk­£[GuÌ\x0006\x001b¡\x001aWËµMPxù-§Q\x001c/¾éÅýÐ\x0014EåtH=Þs\x000cêáùÃÃ¥\x000e(ø\x00101î&kòvLds%ö®¢Ï>\x001aóTË¢,²+L\x0002Ev\x00119|L¯²Wæ	Å9}Â^o½\x0010w7HêÙyWé
X¤OÜ`x.]\x0001Ü¨½k\x0005+8HéÏ[q¶!O<±XòAÈ¶ªÕû\x001bò¨ÞÏ.Èq\x000e%zHM§\x0018ý´æ¨½\x001dA¶²?|xÿO_=pÕ¯Éð¢\x0003ÿîBº­Ø£Kêv¯\x0007ã<9
<6{Å\x0005öÊä£Éc[}Ñ»¡<\x001dN\x001dü\x0005­çþÿôR)Ø¶ìÊÎ´b
Ïg\x0018Ö	ÝëÖÀñÙO&æÖ:òÓö
EÈÜÂ$©Í0ß)\x0015õ;ÌêÖFH.°­\x0013Ø±\x000fÙ°õ8y~f6
9´ÙiÖN'ì$\x0012ÔJÙ½©1Ág\x000b¡¥;2\x00035lç\x0004UÉi\x0018 ¦©$Ù\x0019|iC¯üadçí³°oõ\x001bôâíkØ³jÝ±Å q.3\x0018ëæî­\x0001æ\x0014\x0006o\x001b\x0013½/«u\x0017±n.\x001aÏái 8\x001e}dV\x0015}`>a\x000böèRh²\x0004\x0005óTRvH ê|#åñuNúíØ¿ØÆpvÂ¶\x0011f7\x00116¦\x0013éËZ¢2.ÖÍ?;(;m,O+0H¦f'ìÔúÅ\x000e³7ì(éÔJ\x00141	[ÒN/\x0011³J\x001cÃìëþv¹ðo¾\x001dðÙ\x0008ñ¡-O@!AKÇr\x000eç;§ ³ïrÿÍ;üÑ\x0007N\x001fp.cq0®$¿Y%$ß/ÅóïÅæTióÐó2	( µuC\x0012Èbõ\x000c/V_»`Á)\x0014%AÞàûXÝ\x0014ïë;qm\x001cúes)rM\x0019T]¶\x000f¨ï×ðï\x0005|\x000cÊLC`s|àcéðß­á¿\x00137'¼\x000fh¾\x0015\x0014§ÐÉi	bq°\x000c.\x000e\x0016\x000bú\x0019\x001d&^\x0014ÿ\x0011Xõö]l
\x001fì{¸7\x0001ÎUqåk3kè~!S|é¿K/T$_zoñÒOw>ô­ùÓzkþ$¶FV/0\x0005d\x0001!}ÕôÞù¾öÛõÚoaíÀ¿­]\x000eMæµ»iñÛS½Ò\x0007´øw )\x0007C<­\x001e\x0007[ñG}@oS?×ÅÎó¹~\x000b\x000f¶Ëð`GÔ\x0007¸õtkb_\x0008,Ã\x000b-©)ßýÞ8h`*	WÖ6]\x0013ÏÃ
&¾X¨á\x000cÃôX
»I
§~ª«;C§ú'¼bÜ\x0017=~î¥\x000bÙ\x0010Xé\x0019\x0002ÿÇ\x001byÔñ\x0005¶Ð3¼éßÁV\x000b>\x001baiÚõÐá\x0017\x0017áo\x0011¾À©/¡º-~±ñ.6\x001b-<Px\x001fÓtc|\x0017¦¬0¥ôT4}
ÀOÀö9×f!ª|\x001fße\x0010Á00øz Íî¼Bäýs#{C~óðñîééö[ò¢9ôóçÇÇK%«bD*HWÍ´aeW·e*\Ct<ÆÈü)oíÆL\x001d"Ë/zi3Ìç\x000eìÎ\x0004íØ\x001dØ	<'ovàp&ðìYîÀñLàÙ\x0015ÙÓÀ³ß·\x0003ç3ç:ç\x001d¸	<êvàz&ð!\x000c~Bæ¯C^É=WöìJøì¹ÂgWÒgÏ>»\x0012?{®ø\x001d\x0008väsåÏ®\x0004Ð+v%ö\	´+\x0011´ç ]É =W\x0006ÝJ\x0006Ý¹2x(îÈçÉ b¤µqòåÍ7·÷÷2P\x001a¥mû\x0012÷\x0019sëª\x0007]*\x001bèù\x001a8k\x0017~EÆæ1\x0018/zq7´#Ê/\x001cÑíãÝÓ\x001d/éB¤ÂØû\x001a$S¿-r\¢¥ÿz\x0015í ÑÆô	m|7­x\x0019âýÎ·Ò1©ÐµQ\x0007Ç)\x0016t\x0003rflg÷¯ÊØJ\x00027ÚdqNH· óàtÆËævËò
ä\1ädªÖj²#\x000bJáê \x0010G§üÊ)Î7C+\x0018Þ\x0005©pµ\x0010ï0¥\x0015ÍIdôÿZ4E\x0011¯\x000bÞVèÂ´fÞæT\x0011¸ñ\x0015)/ØL\x0005ï\x000cÌ]ã\x0015{\x0000ÎXúHKvº\x0011§f¹6x]FO0r\x0015+r\x0016hVÞ¯<¥{\x001d¹ì"lIÓDjgÕ· ¬\x0014M
òß>þp1_\x001c(y m\x001c§\\x001a±IÏý7å\x001aê*£5þ\x0013r¾t>sÃ°	2\x001dïùæ&)\x0003ÙNÓFsÒØËwd1xN~heoK\x0001%r­Ff°\x0003\x000fUCwU C\x0008-\x0004%Î\x000f'.û vµíÈbî\x0011cw¼
H1\x001b\x0013Î^Þ/\x0014M\x0014
ý\x001do\x0018¼ÊÊ\x0011¡Ç+zëµ©\x0013;²gå³\x0008ïy\x000eØ¦
Ïfô]í*ª¦LªÆD'\x0001Ú8W\x000b÷¢¢ÐG\x0010+¦LÆpíK\x0012Ç\x0017eÑ>\x0001O{AÖ¢\x0011¬yÁô¸ûîæþb¥\x00069@Ç!Ù\x0019)\x0002\x0013èÈ)÷õJ¦\x0019Ôv<?­\x000fìLI±ø¢6CU\x0007vf¤x\x001dðQ\x001dØâuÀGm`'ÚÁW\x0002\x001fÕÁ\x0006\x001cÏ\x0004>j\x0003;Ñ\x0019¾\x0012ø¨\x000c6à|&ðQ\x0019lÀåLà£Ý±\x0001×3ØUG\x0016C4_¼={®ì)±«
ù\áSbW\x001bò¹Ò§Ä®6äsÅO]mÈçÊ\x0012»ÚÏ\x0015@%vµ!+JìjC>W\x0004ØÕ|®\x000c*±«ìÎA%vµ!ýþ­dÐ+J¸\x001dù\\x0019t+\x0019tçÊàaXÖ|®\x000cº\x000cºseð0kG>W\x0006ÝJ\x0006Ý¹2èV2èÎÁ\x0003\x001b÷	Ù+~%þ\\x0019ô+\x0019ôg\x001b¡+\x0019ôçÊ _É ?W\x0006ýJ\x0006ý¹2èW2èÏA¿A®\x000cú\x000cúseÐ¯dÐ+Á5'äp®\x000c\x001e¦¢ìÈçÊ`XÉ`8W\x0006ÃJ\x0006ÃÙàJ\x0006Ã¹2xó´#'J4DðqÍÑ_ß<|º<=\x0017Ï¨Ûâc9%\x0000³72d\x001fK~\x001b®"L\x001aûÎ0:¦\x0003?+FéT=l\x0006$7Jl%©0\x001cè¹VQà\x0006\x0010ýÄ×X¢Õó1\x001bð¨)ÈÜYh\x0001\x0019VìÛqÁµi\x000c;² þòQr\x000bÄ[ yxÑÃ¤\x001br\x0014\x001c%Wp¬\x0001êOi=$KhÅÊ{t \x0015£Ý\x0008\x00129¶¸½Ü	X£Ù³Ø
Íé<+&Â\x0001bxi»¬¼F~*êa`QÝ\x001e£}k*\x0002ã\x0008xã\x0016\x0011?Uõd\x001er1½²yÚ
LNåÒ(BµÈªzrp' û\x0014g±fÜæÜHgµÈªzx\x001aàµ¤;Öþ¢q3\x0017½ø©ªY¶åØ\x0003NW\x0001rÂ\x0016\x000bÒÈe\x0011\x001añSYO6V¦Ôèó%\x001f\x0011!O\x0013\x001bJZõlÈ\x0001\x0016-
Wcò8\x0019Ö%L\x0003òdÆElÄOu=CN\èb Ö9b1rq[ãÀ
X éåÞ»B*©p9 >êu÷+\x0019\x0014e=Ù:ÑëHp\x001ch
à\x001aJiÂ­FüTÖÃäåbòv¡5´\x0008h,J(µ×f¯¤PÔõð\x0016¡+\x001caÁ>>RÍü¼_
íá¿yó/\x000fw­cÿë»?_jàTÌ\x0013\x0019kmr·%½ÀHÍêC?ÿ£¹\x0016ú\x0013ÞüL×N3×¸\x0003íS;\x0004\x0019Dz\x0019Þ_¬è¦÷ÈÎÁJÞW#+*gf\x0000~%²¢s°k	J{çOÈÉáëL·9ãuV;ïÈù\dEçÌ¬Å¯Ü
Eå`9ï«µ&D~-ôJ
íÙR¨½ýXÑûzè\x001cZîýÐ\x001e¬é}=ôJ\x0012íÙ¨=ÿXÕûzè,Ú|6ôJ\x0018m9{¯WÒhë¹ÐZv\x0004+{_\x000f½FA\x0016`R#Jr0P8\x001a³Ã¦{Új»È\x0004Ì¼\x001az%*ÀÙ'þe¨FÎ\x0013o\x001cYª~\x001e	\x001eyõW¢èâÙÐ+Qtélè(º|6ôJ\x0014]9\x001bz%#GòZh-I\x00120Iòjè(z!9KÞ\x000e&«\x0004µ=\x0012éã\x0017iiWC¯DÆó \x0015¿Gð2O~Ï¯ýáùþRSÇhõ\x0013·ÊîóX®·3b"­
-JóÙ}\x0015Ïæñ|êTMµø¢\x0017wC7ÆëTô*äãÉ»\x0017BÝ¿½ùîÔût\x0004\x0008§Mvï	ñ®4Zþ5	½Ò5|d¢Ô&æ¾1\x000eCÑ^\x0008×Ø\x0004¶/ªÁÂÆX\x0003j»àõ
=±hFöm¦Ë	9E \x00025âL\x0007¢Õ½\x0003ç'ï`q\x000c/\x001e¡ng;?ÙÙ<\x001bEðúsf\x0006\x0006ÓÐ}\x0005³Ò¹íüdf{ï%\x0005z¥G\x0001\x0017í1\x0016æ6jã\x0003ìüd\x000b\x0007o\x001bÚ¾hÙ\x0015nÁ\x0013´)é°ó!\x001cHZ\x0005·z£¥¬\x0019ÖO\x001c:­äøø:?ÙÁ<tKpx<qîY¼
¶4Ê"Å\x000eîÐÂ\x000eæÜÚ snÃK\x0018ë2h\x001c\x001b;}ÀêÞ	;Øgßâ¢'èpP)Øbk\x001fS²º\x001dÂò£7Rò,å\ÇÂÚdóµqú)ÖÙ<.N°Z\x0011EÞ\x0016\x00131llM\x000fh­NQPNQn5\x00138É­æL;@»jõLt\x000e¢\x0017*\x0016\x0011)µÅx 4%½#±­m<_J*z\x0016*Ï\x0005$£U;àO¥â\x0000wëÊ"\x0017½A\x000b\x0017z@÷\x0004M2î°\x000b\x0017\x001dýqdÀÏ[\x00124ô¾?||óõ\x001diþ\x000f\x0017âÊ©`¾*û¼\x0007xO0ÊÛ:¯Z:úX\x0008¯rþ\x0007>\x0005V6^|Qm±\x001bÓ°õà´iy;°èè.ARÝo\x00076\x00113a>Sy\x000e
Û¤¥=_\x0014õ¹:\x000199øÀÍÁRcì
&b²#\x0005ÌEçÎe¦<\x001esHÓð\a±\x001b)BCL\x0013ñOvVUQ;sH³]É\x0002W\x0012\x001bk×¹è!M74M(²Õ®
ÉÌTã´è\x001a\x0016FË\x001cÒd\x001fHXÂ!Y`4'-<ÑÍÛ\x000b[Ýh\x0019Ò4¡aíÐ\x0006(<cÆÆLï¶\x001eÑt&éJ'd\x0007êHà:É+eah\x001d\x0003¶-r?Äô\x0016\ë4+¯\x000c­c<ÓJ®Yr&Ã-\x0016~é$ôp¦;3A¾x 9/^£ÎÓL¸C8ÓWE\x000fÅH:¨X\x000cæ\x001c³·êË\x0011/ÇW7ïÞð¸Í/¿¿½Ø8
&Æ'3mw\X\x0007!Õ+aY¯9R=¢CdÙ<\x0006\x0013­T¹\x001b$wEÍ
nÈCI¯ÊAe¬\x001c}R\x0007O\x001anáÍ\x001cÔM;\x000eKÿ+F9||qEïtó\x0006*Ã\x001aÎ#«¹³ÀKç·KÍ
ºÞ:Ô"ú\x001bI¬¡à\x0001\x0016£_¼vqzíX\x0017$±d\x001e¶^\x0001ÙâfFSÄÌ/Ú\x0010¿º¿½ûðæ\x000f\x000fô¿î/d)2JÍ'« (£jûúÿ=åÞ=¶!Ò\x0007ù(ië\x0002»Èò\x000c\x000eç\x0000fRÎª|y3Ù|Ådx\x0013È\x0017[ô\x0015é`é/ª|y3\x0019}¹zá{;\x001e.mqØ&\x0006¸RMº|y3\x0019}¹JÇ­\x001dï4ÅsZrcQ>ÇND\x00066²;?Ø\x0004Ñ'ä"N¥5i\x001fåËc+b\x001fÑ:Û({\x000bÀHâÈùT3ï\x001e[\x0011û.q~ó`?Þ\x000cpbShõkG3Õc/"#'9
]|Õ\x0012Ç5\x0007§©\x001e\x0011ùÎEAã|Ê0\x000b+ú¼ô\x0016fªÇnDæ\x0000ØäÚß4\x0004ÅNöv\x0011[óØè9+\x0008\x0001Û\x0018Ðl\x000f\x0001+\x0005yËt3Õc?b×WyÃÏ\x0005lÁiCn¦zìGäEGé\x001fÑaÝdfº\x001eÃT±S=6$2tmÌÑû®Ð¸N÷\x000ce¥ÖVÌTý\x0004Lo¼l5ó>]ÊÍ\x000fUìT
¼Ñ^LãÐRr°ÏiZóªêÎcC"ßiÛB<;t¤¥`f+å\x0010õ`£ÇDNàÛÚ,"¡¢1¡Ï$¦z´ÑcK"ï\x0007Ôë\x0006\x001b1¸ÓÈL\x000eä"Úè±' ³ü³!:S±ã¾z´ÑcS"AoìÐûkXz=ý.)IÏº{ìJ¤;LWÂ»\x0017RkGØ¡£)ÓCÛnu÷ØÈÐ\x0001ÜÜ8yÐÑÎ\x001b\x0012\x0016w}´!ü 
\x001f\x0005H:v¡â Ål7ª_=6&²0b°¢X,5&5Ncó ¼»ÇÆD¶i$é\x0016!Ï\x0017Ä£jÊ¢XìzìL$hf±nÁ¨\x0010Ç#1vÓÆ+at(ÂD|_  :ÜêØ=0:ù,\x001aÙûÂQ2¸{~¢)ç+£çÝ=6'ò[^à\x0014ëT^KïË\x0014Ì²NÏ»{ìNdh²lä1VÞø9æ\x0014ZLÉ»{lOä
Ù¬\x0016UÀU×iC[ô'zìOäËç\x0001éìáò¹ib\x000f\x001aí!¬pûñîc[}!Ç\x00150>I\x0013W¸|:
þcÇ/s¸ìë§ú;\x0018Oà©ôF\x0006}íå8á
Y'x'pë|÷ÅM5ì\x001eÓÜÚu+ñ\x0004nQR\x000eF\x0006ýN\x001eô\t\x0007ã	½8>\x0001°4´\x001c>ÿ[uÒ`Ñ\x0004_S)¸â¯¿\x001ew9Z½ÒØc8\x00130¾\x0015oÑdq\x000eæºñ|/½ÒØã$.BEZ,äUFX³Ó[K¢Ùãäï$²ºaÚI\x0008´æiÆWn´öbÇ\x0019_,ÆóÜgÏ\x000eX\x000f)ùhª]Ð\x0006w\áì$rÉD\x000c\x001fÔ\x0008Í)>àÓÒÙ³C>³¨Q ha\x0001\x0017\x0013BÇì\x0016ÎN[È~\x0015\x0005¶\x001d[ªGèÒ§¸¬DP¶\x0018Ñ
\x0016½x\x0014à\x000c\x001b?íu\Då7è 6Är\x0010ÒÅ\x0005\x001fgÀ¤Ö¦õ\x0016'ë-°ÔJµ\x0005&|Df\x0013\x0003hï\x0017e\x001b´\x0008hÐK Ú\x001e\x000b¿Õ`­\x00049C«\x000e\x000bë-NÖ[&£[8%¥LN\x001a­\x0011äð<_¸°Þ²CEÊÔ\x0005jæ\x000bRWÖ[¬·¦IåCiZ.]êÒ2î\x0017U\x001b´è`b}áÄLU=Þ»I1õ\x0019Y+9Ö\x001bl² ó /ï£´i{
5ë-NÖ[sQ
Ì\x0014  qR§®\x0007jÖ[¬·\x000bÔ¡3"j'äâ#p\x000bë-NÖ[ÊÐ-Æ3\x001e£fl.\x000bz
ZÈyI°×lCû\x001c¶üÄäf\x001f¬Ñç¼4\x0005çÉ[ð\x0010$¼{Ö»¶Õ+aôâ¹­ITW8rAI. Ó\x0004\x0016\x0004\x0013\x001b´\x0010Fc%-}YìSô\x000f\x000b
º r\x0012½þ.6ËL(§Èµ\x000fP[!ËnÂ \x0003ûÓaÑ\x0005\x0014u½Ù{%A"½±Ò0­8®;Ôñv´Ç\©ëÙÉ\x000bU´\x001b\x0019×ìÑz´¡#¯\x00041\x0007Ì\x0004Øç\x0004¹è\x0013\x0018µ:Å¤_\x0011ßt_[+ÉC¸PþÔ¢³K®^-#Ûe\x0001eÚ?»»³´«h4g\x000c·ï)ýFOYN[
¤ßèFë\x0014É\x001b²¨Ì·ÔF²\x0000
$ö\x000c¦\x000c«o\x0011>E|ÓTÆ\x0012
=ÓV 	ÙYÈÓ^mthQ¶\x0011\x001cd#I{áä-\x001b
Bw*j-¸¦\x001a\x0008\x000e\x0016bÓÄ\x000c±\x00129Ã\x001c"_y"¤"\x000b+\x0002æ7¿¿ùöæééîïÿãb]ÆÅÁáÇ`\x0006\x00013\x0017ÄÁÀìØ\x0000¾L'}×'M\x000bò\x0007\x0006æ,ÉR<O\x0008\x0007\x001b>\x0007H\x001bÆàíÂõ\x0019­\x0003\x0018é\x000fAò<æêà\x000cvè<\x00100
\x000fÏ;\x001e\x0003\x000eÜÀ\x0018¢ó+ú¸ ?\x00130[\x0013Eù\x0012nFÃ/{aÞdìg
fë\x00119`ñ\x0003\x0002\x0015ÜªS0ûÔ±¬y.üZ¿\x0012K¶Y'\x0017ñ3\x00053óÓ·ö9ÂäÒÈt\x0003¸\x001bu¡Êf\x000efféÅc\x000f\x000c
_3î3\x0007\x001eu×¿L\x0015yÌÉ\x0004÷¶ftÑÉoBBj:Ô÷_¦<\x0002\x0010G\x00134ä#KVä^Îµ\x0014Y6\x0017¸gF@G4ú
Väq*?.\ô2×Í\x0010Jñ\x0006
¹\x001bò@Â´!aá¢©p®õRÉ½NP)ÆE¥Ó~h­TÍpZ¨ög\x001e±r\x0019­9{®f\x001a\x0013»ö<\x001aæ\x0004ðç×êô|~ÂÄî\x001bÚDÔê\x0007\x0005¼\x001aÝúF¿¿»ÕObu"í
yð§£\x000c\x0019äÕ'`t2Ñµú;:¿LY¥`éhâz\x0000<¿Æ¾t¼§\x001bò`Oã÷B0sÅò°µ£lU­¾!\x000fö4\x001e!½"©ÓÈ\x0016B§8·¬èQ¥o°¢UÍZÒ\x0016Ëd	!O|g2:ªô
yÐ\x0017ò3p'¼\x0004ÎSh;\x001bõ%.{àz[ÀûÛ§7¼#Ñ}¾¿X/Ü4ÉÚ%·7\x0006xú'yX¯õôU¸'z\x0017äQz£l2_\x000bôÂ\x0015\x0007^o²ót¹8]gÇ¹«|séD´ÞÒvªeê*\x000bYSÚq9\x001cëÍ\x001f\x001fïÞÝ<}¼ûp)ÇÔbÍxl]BÛ>d¼3¹Ú­¾ä³|$/ï
{cO^ÿ¢\x0017wCÕÛ\x001b²;\x0017ù¨¹7d.²r[g7ýÈGÍ½!ÇsÊ;Î³Í^|TÞq\x000e-¼\x0012ùhÇ9´ðJä£=¾!×s\x0015{¼C\x000b{üUÐGUV\nÞ|}sÏýÜ\x0017
+äil\x001düt\x0016A\x000cmaµ|\x001d\x0005\x0005îmKÓ¼Õ\x0017½¸\x001bªºIfvÿ_|T7i¸òZä£ºIÓÈ×"\x001fÕMf®¼\x0016ù¨nÒ4tåµÈGu¦©+¯E>ª4]y-²¢nÒ4wåÕÐÇG?MW^
½\x0012C{¶\x0018*4^y5ôJ\x0010íÙ¨Ä£Ó4|åÕÐ+Q´g¢Rí¦ñ+¯^	£=[\x0018jç4
`y-´Rí¦	,¯^I£;[\x001ajç4Í`y5ôJ\x001aÝÙÒ¨ÔË¤i
Ë«¡WÒèÎF¥`&MsX^
½Fw¶4*\x00053iÄòjè4º³¥Q)IÓ,WC¯¤Ñ-JÁL¦±¼\x001az%þliT
fÒ4åÕÐ+iôgK£RÖ¦¹)¯Vµ\x0017Ø·¾¾{¸¿ ý\x0016³\x001e@ÓB´\õÕã¨Î&YSéRoôÿìþÚ'w§)ähmq"±MÞt\x0004e¶\x0016\x0003°±·\x0015(b6\x0011{YËÁÌQ^è¸\x0019_\x0012¯Y\x001d-q+\x001e[!\x0001£\x0016D£Îy\x001c^b'J·ñ_\x00112\x001c2ÁÈUò+pºVÖ&g\x001b V*Ú"°Ê³£ \x00089\x001a\x0019Ûw!\x0003ÍY¶T%äTUD\x000cgA\x0010²(Mæ\x000bia+\x0012¶¥ÒeÖúÉÓÏý·7÷7ï\x001fï.%\x0001ÍXtóÖ§\x0004±kúaK-rnè*
£éBúéÀænJ\x001bB³\x0011_ÅCÙi7ZW¯\x0003»\x000c¯)\x0005øK
N½à¡\x0001V\x0017\x0003å:t¹yÎJ\x0001\x0013Hk^DCëI\x0016pR§ùôXnÄK^H×q<øNig^=\x0005.&½;;\x001dxÑm';!Ó'ÈÔYÌ5ânÄV¸«E\x0016\x000eìåXCV=À©^ÐÙÖp¢E\x0016fª\x001fçh\x0016£ýHØ[Ã,iåþÏ<\\x000e2rTÞ\x001aÍb\x0004\x0017ºÔ¤h×/ú\x000fM¦yÄ\x00177ß^´ÆËú)9;²J\x0013D9<ëÏ+Ð=ü¶×<ë\x001e¦a\x00125ÅÜC	ÅG\x0001¸s"é*}Ä,\x000bWâ[Ùlæ\x0018W¦¤}Õ)Ì6dÉ`\x001fÞ\x0016Q\x000e@ï¤\x0012!;õ%«³YlÈB­ÙÐÚ®NÈÞâ§ÅÊÌ\x001e¤ªµ
8\x0017}ôÅÕü*OiûÐºajmCN°ä*:4ÂÔÞ§ª¦ÖÞ5ËÚÿÛ¯Ä&k¿xþxûæ\x0017ÿÛ7\x001fÈÝÜß¾)±^FÀJ\x0008Ø¸mOãÙã\x0012ÃAd`\x000b·Dk\x00100=__æ£ÿ7ÚH> ²\x001f=\x0019µQòqV:/9à«p\x00078ìFÑêü: «\x0019Ð¾\x0006h[HË\x0011ú\x0013Ø|o½2©+ÇÙùýí\x000fw\x001fÞ¼~óÛÇGR®÷´\x0005mPß¥R]ÈÁKU>¤ûáZ:ñÑg?|¦LS
hÓlxóNò	¥áÛ¦E¥\x00076\x00142Îº3±\x0011·Ðß§c[¡\x0006S´º'oÉ"£\x0014\x001cA4®óEÌ\x0017kæ\x001fNÐ±\x0002Eh±\x0011ÛìÐ>B\x0011&w7ìCý-¢ìô¤w61?\x000e\x0001ëÉ·)
³ö>!`d¤û/{\x0011B7«\x0007´s\x0013tþw\x0010â
:\x0016Q\x0013½¤c%5*p
ReÓl°´º\x001fIÜ\x000fo¥km¹\x0004\x0007úëjõ@Öb[s*Cä\x001fvl\x0013åý`=\x0004åµ@K±O¡QåCÀpÃÎ"`èÈz.c?È¿úíê¡~ÛÇÆ{\x000fñÂ\x0013²\x0017º\x0014\x0004=\x0002yÛ±X\x0002\x001az$H6\x001btm\x0013t\x0012\x0016oÍâu'è©a¨â9Æ®s\x001dZÐõVù
\x0013t¯\x0007\x001eÐ©àðëNúZGæ\x001fvdòÙÂ¸Ô)(\x00019fhG!«½Uv¬n_·ÏÈîNËÎ\x0016Ô´×b'ìÎÊÍ\x0011\x001a¸í\x0015\x0013/)ó\x0017ß­dûa\x000f\x0019zY\x0014mÅ\x0015ÄYÔaáÎöI³l?ìàÌ	;d\ÁçJØ|îïMÑ\x001c\è¯÷cW\x0008{ò\x0012²\x001e\x0011¶ét[I×¶eNT/b^ÛÖ
\x0010ðV¨z¡ÿ\x0017{£øê8]\x001aÝvÌî;è\x000c\x0013Rg¹å\x0011ç\zGo)ÝCBf\x0003\x000fUõÍ/\x0019ôåsëÄ¶¾¹
|\x0006\x001d;
B»2
qéâ¬KRz°)åM\x0010³ç¿c\x000b\x0006"Õ aOÍ¯Á\x0003Ùç§\x000e®ëØö\øÐ
\x001cÆ¡ÒÊÃ\x0004Þi½\x000eÙµ\x0013¸ìFÏIø}dKL|\x0013S{¾7ý\x001d¶tÎ\x000bð(¶%ÉNfzÝ´-\x0006\x0018\x000b<é
×ÁWÛ\x0012Å¶$'Ú8Ld\x0012\x0007`A20\x000cÂsGIËÒçÅ¶ð\x000f;¸\x0014K|\x00170HÄ\x001b!À  ­<\x001fÂ"\x001bx\x0008Yrè\x0018²ßq<±«À*C¿ÏìÌÎÒ\x0013¸ì,å\x001aùmÌÜf\x001b\x0011»Oó±Å,Ôm\x0011ÓpÍ}¸\x001c\x001c\x0012\x000c¸Ó\x0018ÓCð	\x001búxéÖ©ÉÛB\x0013Ë}¬k]f\x0015§ÈÍ\x001eÑ3²B3rp#\x0013²Ë¦K'íå
[ôy;é©Ò-8É¹ÍBo,»æP-Ò±¤Ækýc¿éñDËÍà´\x000cG\x000fuêàº>t\x001dlJÑþAà}|\x0000ÇÂÑºÓ¸µxONã-'\x0003¾x¼{ÿpw±h\x001c)ô\x001a#ûö&\x0005ÙCÞo©Ïî0.gIãMp\x001c\x00173éBk\x001b»\x0001Î\x0011m×\x001a.w`A¦ç¡O;o	Å6#¾)AÆíÈK/XÁMJnhÁ±Yti#Ý¤q-íÈÈj+Àm?\x000e¸\x0005\x0003ö:Ø4rÙ\x001d9\x0002²\x0018ìR:ù\x0000ÆÝäÌ]øv\\x001f?Ü½»ûñæoÓ.\x0013ýòýîæ¯7$\x000bÿtûO¿øûßn\x001f1Òd \x0018¾C\x0000v|^k¡û^\x0006\x0007}áxìèøoyLY\x0011\x0006LÌ¶òÏ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-08.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-08.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x00072ÀúºÀÙ6Z'§\x0007«<mý8ñ\x0000F\x0018>TÅ¾÷`\x0012.eN>q$Q\x001c[Ô\x001dF¹\x001eè\x001c<>]\x001dºi£¸·S\x0011Õ\x001c+¤MäÚæi^­C5:\x000f®íÜÞN/T!F°óÔ^S\x0006¢ò8\x001byzÒÂÝ¾
N\x0017×\x0004q>x\x001c !\x0016èù4z]¢JµÊÏßÿø\x001fÞ}øñ/ÏfL8\x0014÷\x0006ÁT¯ÓËc\x001dø/\x001bV:Õ\x0005\x0015kÚ\x001dÇç<ºEÃa\x000bo¦{\x0011éªUÓ¬f\x001fçC­\x0013Û\x0004N¯ü3y°\x0007¶z'mY¾Âl]ÿ¹\x001cçb,uK,O¹\x0017\x0001¶¬!QþE\x0018Q\þ\x0019µ|òQ£å¢2Tcokæ^~¯ÉÌ¦m¸ÆtÓnf9\x0015âûÊ®ð«bþÀd/qz\x0013Ü=üùÕ?¼{óp÷ö¾¯XèÐÚñP\x0007¥×zmù{óËà*\x0000$Û¤\x001f\x0000\x0004ðQ£µS+¥\}<òµnïéU\x0000è>I\x0019ISn O\x001d\x0003ëvt«æ>HÑaÀÚ#,ºàT\x0016íR êf\x0002	ºÎ^àPð 1þã7\x000fÏU¢ÑÁxrk\x000c7¹\x0004ÙHtò~©Ñ\x001fûpÈî\x0018\x0002c×\x001eÜ^±²$?\x0019ÿÁM\x0007\x0007òYý©âl ±Ð$3ÓÅ\x000b3õ¼òsYIz§ç¥£Ê\x001añÔ\x001a·­IÔ8»\zºÒ±FIïñÍ7Ï¥¤µj\x001fsá\x0014|\x0007>ýà\x0003¿ÈëG{\x0019=YJ¢|ª²\x001bUÉ}cÚu\x001amåWãß± ×Ï­½fTÉv¬Îâ(\x0015^CÅ\x001d\x0019BÅ\x0011 ;ª5Çc¤\x0004¹\½_»
§å÷­þµ\x0010¼ñ¥J¹zU\x0004ªä-½LÏ÷ÇÕ¾\x001dº0g+~òÇÎ{&F\x001f=Î\x000fb¦\x000fo¾¹{ÿÕ3Ùip,\x0012³»9xrIB6´\x0004m\x0010xHý#Ûe¡ÚQMJ\x000bcDI2Ã±Zôez«\x001fÈêØªStÀ\x0017M «A-ÍiéÍæ\x0000Æè¸SÕ@\x001c\x0002.Öê\x00189,$\x0002M\x0002x\x0010Á	¥óx"i6vÛqÊ<`AÆ_eoaÁútb\x0012ç\x001eµüT)î\x0000F>\x0019é¹\x0005Ü ZL4K.nÊA8Ï[
b©RÙWþk^ò6vöjn6³à÷YÝ7à@Ý
Ê\x0014Ê¼\x0019S¸\x0003\x0018)NV\²\x0019òÉª¡²\x0017ÆÁ\x001d\x001a\x0007PêS\x0000\x0015ÓÐy\x0004¼9|'Ì^\x0006ñOL~ü\x001f¿¹÷§o\x001eÞÞ¿úíûwwïM¡ÕsU¢ì°ð¦M\x0017íûE«\x0017wMgGJg\x001fÊÙìnR~yêJ+5Uë>öHk.´n÷qîx^³Î<\x000b²\x0015úy¬¤ÎLÏ­ÎÂßÝ}ýà<Ë9QãÃsU_éxöq²k£\x0012îê/t«ÃÝÐÒ(\x0010\x0019\x001dnfHêÀµqR®·Ö\x000e}¶;+5ü¬ÍFmwÆ\x00022\x0010ð¨H 1²fùr;ôÙñâ\x0005ëÌhË
í_7\x0014}¨\x001c\x0018äÞÓb¾Ü\x0006N]Þ±¢\x001c5+_aCdJ áÿ\x0018\x0000®¯û\x000e\x001d\x0000ºÃ^GU¡Äîa¦Î¢ú\x0018\x0014;\x0003·C'pÛ\x0006ûÅØ¡ðÜ³¶¹g;ò)ÜÑ
Î\
­fªû\x0016mp@èê¬û±Á\x0005_=¾úý»\x000fâà¿óêwb\x000f÷ÏT\x0015R];XÊ-Û¤ÃhÏ²ÐÓ^¨y¡¦¹Éel7ªÅÁsä	\x001d59k\x000bå\x0003\x0019ºi|BÖy¡T\x001b\x0017SB-OÛ\x000c\x000edè¦q\x0011\x0005Ôuü#²2
w¨j®i\x001an\x001eÀg3Mh
Â\x001f£ñ\¥\x00163\x0001x1<¼ÙA\x0003êjGÌC\x0016NêB9ê¡¢7u
í  .=ÌãÉ¹
Z\x0018¢Ï·±°&N¡3\x0010z3ÀØÊ![Ìc¸ëFÒ8vÎÀ\x0008o\x0000¹I­  ¤î3§Ð\x000e\x001aÐ1ËÐ£â(¼Ëg#Ô\x0017¬f&
\x000846fí\x0015nt4\x0012SÀj(qÎªivÒ@Ð¡pp6²ãÉVÅÌnsòÊ\x0004OR¦e)û-n\x000fÍ\x0003(>ó¼
ø^Ù \x000c1Ð<
ª\x0010\x000b&|s3\x0007z\x0013/L1hf.\x001b\x0012±ò\x0000¦¡Í\x0005Ðfºë¼²Bb cÙq°p)L\x0014+(ÊK·\x0018xÞÌ\x0014ÀA{N)ò¢\x000b®TjN\x0004jvAtF©G{ÛñdùÜë\x0008¯\x0002x÷øöá¹\x001cW\x0015_#Ç¼Ä#ÀÑa¤¯GR·úÆ\x000b¼:°öcr¥ÙHp:å\x0001e\x000cÉ:=\x0004ª'fÒ_\x000b	Îl$8ÖM!­¦=b¹º§<oÊFSiâX\x0015\x0014\x001f\x0012ë%ó°\x000b1£2\x0017\x0002ÉFS^\x001bì½KÕ\x0005*"+ácÛó4½»#gØ\x000c!ªw¸\x0015FØ³÷\x0011ê][ÍvØS»I5ô\x0013Â6ÊGkÅ<rQWÎó\x000e\a½~´8Ü7i8øzÉ,y°¸®}f;r=Î04Nypì1s­$âðÓ\x0006\x001dùe\¡\x001aÑ\x0010ðM\¸$Ö[kõïÐ Þä"\x0016W*IÓ¹\x0002PÃ|®Ï\x000cö'/U\x0000~øeD+¹(½nC\x0000Vö\x0007êMN3\x0017`&\x0012vd\x000cÅO\x0016=×8 O©G\x001dF\x001dSZ4Ão(\x000fYuXÈ7íÐ\x0018\x0005ºA\x000b%è\x0006eÄ\¾i®Þ´#	º­fxîÔàXR«æ^ß¼\x0019¯­ÖA3GöÃS_´8c¦O¥l#V\x0008J\x0017\x001aÛÂ¡ÖI6ÌÅôym¢ÔÊ\x0010=\x0018böÔBV;Utj§Ù8ï÷ÜÑ\x0010Ó8j7äÌ.Å@¡õ\x0013ÊÀ\x0006\x001dÀ\x0010[.ÕTÌ°8ùd-Q5E®e²\x0002>ÂïÏ\x001e,Mrmôs5\x0005ÑÅ¾KT\x001dM\x001f\x000eûm»8°þoI\x001dùKÙ$\x000b],ùÉ;yxoÈéç"[Ó¼!líçÜ~\x001eò¤b\x001bè(n\x0005ÛWw~õëwÏÅ\x0006Q/Ç²¸\x0012ÎËËî½ü®^÷/V±µÏÏ²CÖ\x0001®øÉ\x001f;#V\x0018ÖÖ\x001fß}}ÿþÕ{|xûöîñÛçêÇäê±ø6§`\x0008ç\x0007-}¾PûcE©{´ÕZ\x001a¹\T\x0002\x0003¥\x0018\x0002ÇE-´1ðê©ìÀç½¢Õ²³3¸x\x0015$%äÊsÑåyËÀ\x000cÅÚ@\x0003z|Ûªt'r\x0008¼æ>\x0004®~Ê\x000czîJ\x0003Môý2!gS\x0006öu.\x0000²#ãØuGEqÇáÍx_y7ú<ZØ\x000bìF§ÞK1#l\x001aÝ \x001d\x0016\x0017{uRv`¥èf3\x0002%ºo¦ú¹±³®NÊ\x000cª\x0014\x001e¥Jñ5Õ®]ã]}\x001e,ìÀgÁÖW\x001c¾=Êø\¼Î<n*n
ô`aÆm¯\dN¤W.»Á÷¡\x0015lá~:æ8Ü¿úÇ÷Ï$Ã¥}.Ü}DºáD-Ï9ö/ö*L\x0006ª9Þ÷åü½fßÃ¹¾o\x001f¿{xóð§»·úón\x001fâÞ?|ýÝýßýá^GA÷<f§{rnø
S\x0017('È\x0003{LçÙ\x0016ôå\x001211ô¨e¾?½ûÓ£üg\x000fúOEç`ò1[Ï[\x001d¢«þ\x0017ßþ[zÿÐ?³	´ä³<?þåëoï¿û0füïþ÷üÅ÷\x000f2æÙq\x000cO\x001fÇ¦M¼\x00184J\x001cü±sr§
C¹ÆØè8ÒVüuêÂ#éýô£yì\x001e=1\x001bë^§.7\x001cÚTd¿Ó'ßÕT×ÀpäÖ­\x0000±E ù=\x0016hw¥&\x0010t5»sØb{Ìñ*Ít$þ¤Ø\x0008;Ë¾%R´c×!ëA9/íäIºo\x0012p\x0006`ÄUëjH\x0011\x0016h×±®ë»IÐ\x0005 óYÉÑAâÔ\x0003"ØÞXn×§°ë½snëöX_Ðu\x0013çÏ)èòx\x0012v;±s>[k·\x001bÇãñKºv\x0005»\Oî\x0000}êÄ\x0008rp¼#çQ;?ÒÆæ\x001aGèÛE®»]Î·Yw;aSî6õå»­Ç¯­ÑÖ¨Rûy²cO¼Û)\x00137xÛk¿¶G\x000föê9*yû%Ódó!Ãd6&Gx;:ZdT«òÛxÝa2¥ÀÁ$Å³ïpKÅn?¦ã
wÉç×féO³Ô\x0016~ÚeÔ
ÞS±f¾÷cÌß$ðB\x0013\x0017PyN¿&ÕæÄYÛÄï×é+,<9{]xF±5]xdð­Æ\x001aÖg<¸å\x000büûeD5ßNbèÉT\x0013Y¹j\x0008â÷ô\x000f\x0013wéß/cª	ü<,·øÉwüß/ª	üö=CÓ\x0002Ú¹-\x0012!I£%gÌÓ
ÂCX_·aÕ-wT©\x001dGÛËíIÇE+\x0015\x0000²þñö=
æôóa\x000b­@ Òb¯\x000cr:ÊP±×3\x0006ÀÎ¸ã
Ì!\x001dñEQ<\£Ì\x0013×3&\x0000\x0007rgòP\x0004ø
>V¾þñüªÑ\x0003'z¢£\x0001\x001fbqý=c\x0003ð&¤Ä\x0013\x0010VpÇ{^	¥õ÷Lð=µíå¼Y´è]	ÜQ[OáÊ^#pø !àK\x0011@×¼ÅÖ¼Ùí:´=|#BW£¾ÍáìÙÑËÅá|Ñïb\¡!h÷Ô_ )¢ò\x0017Ämhv>cä·.xü\x000c_oÞ¾mÿ\x0006éÏûWÿ¤Ù·¯+¤(Ñ\EáæàpAKL7,¿`@\x0011tèÕ5 Höào[DLÂåâøÙ­\x0017¿\x0019:4Êû¿ß|¸ûáþÕoïßÞ½}|ó/Ï\x0016Öñ<LeöÛSâ#º\x0006)l\x0013X_ì+ÄÙÌ+kÁºU6òr\x0015ß×\x0014\x001dêuêH\x000cgÜ1²ØÞÇ7dx\Uw­\x0012²G&öl'ÑÑ
\x0017°ùN?ù&ÁÑ
ùôÀä\x001e<Ç¯é\x0003;Ô1\x0017³ä|t\x0007Èç1\x001f´^OÈö"Dvy{E/7äþswã\x0012½\x001cÐgì\x0012Tí*Àv¨¶é;QUor2ò\x0005 ýé¿4w\x0005Úa.T¹\x000fD\x001bÞ§±Ë
\x0019üEÏ\x000eYÛPÖÜ'3 \x0000ùô.\x001aó·OXÐWäéõò\x0005ûÔõ¿\x0001£X3,Å±çïM$\x000câúEò\x0013­^¸O:#×k¶øÏ¬6À?Ý¿ÿêñÂFûÄëU\	\x0013\x000bßnWÕáv°EZÉ7Nîªü¦mlÊ,tÈ-dÏÇ1wÏÞKI×B\x0013à÷¶\\x0018è¤ë°ÅÒ\x0008l%ê¹6\x0005\x00020äËäªêçµ=º2ÏçØ\x0019o+÷Y²ì\x0006à¡¯\x0014$jÚ	ÍG~¸I;ù+¿\x000b+ {{æPHLx#ÚL
ÀàT~ÀÄU¡\x0004_É&\x000bç'}p'2dä.!3ü^©ü\x001c\x0004¦i¡\x001b47	S2¤÷\x001a±JtÑÕ¤;ë,qsC>\x000fFÔWdSmOc½óu\x0007>v3dÌ\x001f`GèÍ:!%\x0003r%Ã­W#û\x001f\x0012üq¾:ÌL{\x001e9QÖÀøäl\x0013tu-Ã¯#>ßsQ\x001dð1\x0008tCfs.\x0010Vç"ç"&OqJEÐ&§ÂLÜn¢ÕÁ\x0008p0tV\x0014ØIÎ¯\x000b!s\x0010¨Z8¼ú~\x0001¾_
»Ï\x0005ªÇ¢\x0005úCY}Â\x00000\x001b\x0013t¨'ÐÕ¤Õ&«²ú\x0001>a\x000f«(Þ4Ì[½M÷«­°ÕZ\x0017,d*tqðØFÕä\x001bÓEV[\x001dÏ­Ö¬7h¸9Ù(`<'«çF'_h£1CAÈÐ[;q¶#
ÐÂa¤ATGÉJcþôfrÆ\x001aû"Gp>ä?éÌg\x001fðID!ùñ*ò\x001fØ^Å0õÐCN!fOOM¦9\x001brd²yÍ·â/xó\x0017>å*¼\x0008ÑáÃ[Ô\x001dyñïùAKÉÜ.\x0013\x0007Óvß|s÷þíý÷êhþáþ»¯\x001e&óD?5Ï\\x0005c2ð\x001eA´pÎi¯­ct_4ïþ'µb¶Ý2®¦Óvµó\x001bäD\x00135à6qDo×é]\x001c\x0000¹àã1¦¿eBÎf;ãÕ\x0004Èç¦m
¸Ù*É^E¬\x001ccn½=W§Â3
S{8û³\x0004¸%¾c"\x0006½S?rðÜÿ Èþìv\x0017d1¦NKNÔ\x001d-\x001es¦\x001f<ó;åàU\x0006Þ\x001apÎ3\x001b\x0013o²\"S\x000fÙs\x0007¬x\x0017ö¸}>SpKK»6ÉÕEöL\x001cUdwöîåZ|\x001b71 sj98ÏkxîÐÒLFä,ÏµÃÃ\x001c\x001aß¹Ñ»÷	
Þ·ÃP<)\x001aÅ5\x001c¦V5§ªsïÛs\x000bÞ\x001d\x000c%ºiÈ\ .M\x001a\x000e\x0001:üÌÓ1qì=·@\x0008²vIÂVÛÊzàÞb«ç\x0016\x0008]tx
\x0011µ\x0015²B>\x0002ÛJô@\x0000t>¡Åëtg ÷"\x0007d§8©!^Â¤ã\x0010 Ù\x0010ñRjOuìvª3\x001c<÷@hz
:\x000euÕóÝf4xuÒr\x0008Ðg
Ià0rÈÜ/«ö¤@${½5¬ñ\x000cJTÞ
Ý\x001c\x001còÃeÕËS\x0012öYùø\x000edôn\x0010?<yú©\x0018ñóg$cm§ºm®rcð^á\x0017^êÒ7h0Æ\x0000ÓUÕd\x000c\x0011À\x0017\x001aè[«áÊd\x0002£èA'ïÒÅç	LÚH_jÒ7hH4Êí\x0004Yh\x001dýÌµtoR%ÍÙé\x001c\x0003×j>¾úÍãÛë\OôÍr±~Ë\x0003*6p5°¾$y.nç?Â9cÆ¹¬<5|tÜ¹Ä+k\x000ba#YOÎ"SÎ\x0015¹pÆ r&°x\x0013x%\x00032äìr¡aÈÅÈ\x000fÃfËáú\x001d#Z}?D\x0017J.ãÍ6<É\x0019gb¸ »DT¨88¸)Öæº¯«\x0001\x0019ò®!u!SåïgÒ~ÈLLnWæo+ù±aèí;ßÛ9Ù\x000c\x0013;!¦c\x0006\x0000¹ð;¦Ã\x0003	¹¶IÛ$ \x0003«q:I¾geò£©ÛÖb×F,i"¾_=~ýøýï^ýãûû/\x001fß|óî¹j\x000bzcs\x0000ê t»Q­ÈYü^*î§Øn»Å¼**G	çÑ(×°ôÊ<à+O^eÜ\x0012MªSôÄ\x0013Å×\x000cò	ødÉ
TMµ§<äàçWJ1aÙ\x0008Û\x000b^Éx±éVr@g¼Ö\x001b2øltC¢oäË*°ï\x0013ãu àbÓÐ£OÛ\x0004'pø5}U\x00040aHÔùÈm\x0005ûa5,K¼É)Oé7h\x0008Ø5BajÂ14²Ä)3»G\x0017âÐdû§\x001f&OhðUt\x0016ñ1ãµ(|;ÝMý ð¢ÕDïÃOÎ\x0003Ù¶Éx\x0011úTdX¹³dvVu\x0010.^%.\x0000\x0019¼ºMC9â¹¼­­\x001cÉpjrb¸qMS<õäö·¦4yb)\x0007âöûÔ®Íe\x000b\x0006¯ó?n7IwÝ¤}M\x0013×é\x001a3òm\x0011\x0019÷ÿðæá\x0019ûA3éOçãé¾¹S\x0002D/Ä0
3{1_ºA$äÆ\x0010±*®¼:.éú45\x0000C	ZÝz|Ö:;\x0017Åe¾ÊÝ\x0018r½Ê³mPøDä	\x000fÇö\x0010|\x0012òä4ÉÅø?ß=þðð\®Pè\x0019sr¥÷vK}»\àr÷òÐ¥úË\x001fÅ	ë5uó\x001bQ}B\x0015\x0016%taþ¬_Ä@ÕÎ§\x0014µ2­i0_\x000b5V&Ïö~\x001d\x0008Èg4®YYxþ½öÊ6üN®ów
ó¤lfe`]rÅ\x000e\x001f\x0012*-\x0019%^Æ\x0007Û´\x0019¾ø\x0015Uc~óö ÓbÌoß}ûíýÛç{¨/=Aåv\x001e£/2\x0012ý¿,©24÷\x0011´»k-Æ·\x000c.ÆÈÐ+µòüúÉC}w­Åøä)èÙçO¥³;ZÊ¬\x0014sw-Åø\x00118iK\x001e:Zmg×Î_%1\x0000\x0019zr"udg ärä<BL¥\x0003dè\x0003F¾¡îLÝwã'ZÓ¼»Tb>\x0001ÖÏ¯·O¶Ï¯\x001e_ýZ.sÍýúîîq\x0003v¢\x0019ûx´Þ©ûvû
Eg­ÆðËsÂ³½½¾mÒ½ÏçíµXú?{ò&Ð\x0008?[Îÿðã_þíáÇÿïýuÚÈ§\x0019;ScLù<ö\x0005»!Öñ&+?²ò_çîº!c¯Ç\x0018]«½Ds\x0010Ó2\x0015êÁt½º)ÛË«qÖ<|\x000e¦,÷Û4ÌHÙ^1uë ¼!ôj¶¬ÕÚ®Ã¸\x0001\x0019»e=:-h@\x0017nï\ÒÛæ\x0019^Ñ\x001d\x0019\x001bZ\x001bP\x00070qú;Ó«\x0005xQL<§x\x000b!ï§K©~\x000crÞº+W_ºB=:Z%\x0018Z¡·\x0000tR*Ü¡¡bß\x00130\x0017Kòü\x0005aëÅ¶Q\x0017W\x0010û*ÃJÉ·#"dìeQsÛ¡!;T
¦ÈKÅ/(N'mFò¤fbÛÿúÿüû¯ß>|ÿ\±mô\x001cä<Áê#¹·ÿØ¶\x000eî_ú\x0015º^TÁê\x0011,VþÔ6Û>û	ùÿu÷¸Ñß½y÷hæUè¾\x00077ß¸yTCµðôÕÆ¸p6»¶ôÁEªò Õ7Òù!ìJ>A}C¶¹ò¯ÿâûÎñý,µ2pî_ýÓ»kz%LÕ_ÒÓG°'Ê®\x0016ë1*2k\x0007#u\x0000Z\x001eµ²Sü\x0005~ú_ç
ö3w¾iÝ¢wXÖ\x001eðFÌY\x001crHÉÉÏ®ä	É±HW°Óí
vCàâI
|U¨#Üò\x0019î÷ykåÌ3èôSe^s´P\x0011v»a«¾ïMS9\x000f
òFØ\x0011S¾z\x000eêD¨\x0001Áo¤ \x0005w§«ï¢ä'xÀò»	sÀÃ	Þ\x0002<\x0013òÿÙ\x0015_ø\x0004Ëß·÷É\x0017ÿúÕ?Çû±é¡ßþø?Ý½ÿp¯b6woï_ç±©\x0018q^eé.õz\>:a=Ü¶ªD@ã\x000bÚTh@mmÊÏm¿8²[­ý©}ù\x0010\x000f?üó×oÿ\x000c7ù»+1õ\x0013·½\x0010ÿ§4YÑ\x0011OH¤íª\x0000÷ËozÝ5û¾mÏ\x0017nüWO­ýÉ\x001f}Ùõ¯¾º\x000bï`××\x001dÖúTG«\x0008CÝç¸3\x0004.\x0012¦¸Ñö7¸ûÛ6Ñî/ÿäO¿|\x0000%\x001e\ÞóÏÇOù~ÄÔÏõ\x001d(UïÇðíõ¯\x001cwÙ{Î[ñ?Y,Ù¶Ê>æÝ\x0001c,§Ð°Ü\x0004ôæä¯ü\x001f@>\x001f¡Õs\x0002ûõ5\x0001v\Á°©ÿY/á\x0006>\x0002tÐÍÎHfU7!eþP%\bj@Î'²D¾)À©r$k\x000e@Øúí
C.ðGhËÚù\x0019Ï×®,\x0000@®°Í\x0019
¤bC\x0019£HAîµóÃÿ\x0003È\x001d\x001dîFÔéRÑÆ°Î©_s@£WSm£5èxÈ½ÜhÑ>oSÇW\x0007Ú£w\x000e%;M\x001aäjÆ¼\x001f¾\x000f¢I\x0005\x0000t
¡è&\x0006RÓ
éW\x001d¯\x0000@Î¡\x000b	Û!ÿ6Ì\x0018\x0018N\x001e:Ë\x0004\x0000rvÀÂËQK\x0015\x0015wºVN[ãåê|ø\x000eÐ\x0011r.²\x001d\x0011Îú\x0011\x0003_ÙMnïí6Þoïqãý×üç\x001f¯Ú\x0018|k³\x000b[²/çEYÜZ0sÿÊ·vÒÑØ\x001fqkËO··¶N¡\x0008\x0014gÃ¤&}8\x0003E\x00059º+ß\x0002ñÖ.P<¸t­ä
ô|m\x000f=®í\x001c¸ú\x000c+®\x000eçÉÉi&àêa<\x0007\x0007r¢\x0015Ã[ä­°ë¿\x0005\x0007l¦\x0005»
\x000b®8¨D\x0017ÌÎá6¥îò\x0014\x001cÀwø4öÚ#êúè©\x000cÚ´R:{
\x000eäJW_Fdg\x001efK\x0005¹7ä\x0006kÆpnÚ\x0004C§¦/\x0008r»Îï\x0002`xcB8#*p·»ì2\x0003çI3û	
oOaè
\x001fÐRÂºæJ×Sî~"\x0013\x0002Ðl~åD\x001e¹¼j}L(n¢\x0012\x0002À`}±C¹@\x0003ow±\x001bä	A\x000e Á\x0000}¬¾@\x0017ìµÔE'\x0003½µ³¯,Ð\x0005ÆJ§C)'|:<ßÁ[\x001bÞõa< Á
çWô×ûµ\x0006 Á\x000eu\x0002*ìµ<î {££W6Em¿2\x0017\x000fæ\x0012Q|LÎlÆvh6\x0007$lC·W§:À©\x000eC&ùL(¦Ðî»\x0012·Á\x001f«Ã\x0017àð?\x0001¹ â"³)¸Ï¯\x000eHHtâ~TvBÄÊ\x000bïGÊÞ\x0011¯¨
\x0000º\x0015Ì;ÏÇÐ\x000b«\x0018à#úNG¯\x0007\x0013fÔÎÐetúÅÕG\x000c\x0006\x001eC¹xP_
#R·9«\x0018á#zì\x0000ÒY-È\x0012\x0018ÉY6:ÞÙ¸Úê\x00081&6\x0001ZÅ:É³\x000eü¼Ô­[;®ö:B
U¹Ë°!\x0012?\x0007NDVÞÄ¾V[0Òè\x0018Äô\x0002\x0002}\x001cM\x0006¾H\x000c©ï\x001bLá\x000fwï\x001fÞÜ¿úÕ·÷\x000fo)ÅÖ\x001a{*%ß\x0008G\x0012W\x0014\x0010y¼òóTý§ýéüB°ªFzàOêQg+ræÝÊÔ×üB°ªË\x0011\x001d´\x001e\x001c½Â\x0012~p '\x001fwê«\x001eÈ\x00111\x0019+6D
ëÌU¬Róµû\x001b±>\x0006Ó9õN(Ý£õ±dî4Í\\x0004ë­jc\x0015Q(\x0013i¥ú+\x001b\x0010ÏÄôâä=yj§`½U§JÂ¬ãû2®¹x³\x0017\x0003ùr\x001cÈí\s¤"ö[:Z³o×ì'=Ú'ôÙ£ÝUö·ãKVqx@G³èì\x0016`Jp\x0006Ò:
;ý0%ªíl\½Ê\x00039v\x0015¤NdÑ\x001d¹¢=VÒ*ÖEoCPW¦\x0002^¥SO¸Ñ#éÈ\x0008cçãQ6!ñ­=Ú\x0002Â»uÓ-eÕÅ\x0019è4QÌ\x0006h°\x0016ÒI\x0012hºfÞâ\x0016épI·¿[Ý\x001aù«±LjuMÊ\x0003ú<Õäø6K¤jã\x0008Z¶zÂé\x0000hÈä8\x0018\x0001³AN«öÆ`F¦ïê¯îÐg\x001fµ\\x001f\x0019\x000bÝj0\x0011Oµþ'\x000c&ÒQ\x0000íá2Mè¯Jhèþp9\x001bäA\x0007[êS9ª÷\x0012Ù_5Ðâ°³§MiuôNé¨®ò\x0000	¼ÊÆ#vBÆV\x001e\x0007ç4¬ÎÞ)\x001dÕ»§Ä÷¨×(\x0006Ó\x000bÅ8FFÕ\x00019¥£ºÚuÇU^Ú¢y·b\x001f¾ðê+Æó+Ê«LÁ£NM'3
Ö	Eã²¶\x001a@x_£\x0006ìK¢ÈW®?i_²±É`ÛËÕµ$\x0015 £\x0005â\x001fî¿º\x0012g?µÆ\x001a( èÞÝZÃÄm
À8ÐkËÿÒ|k@byá]¥³\x000cT%^ÙJùÖjÛH³kPiÙÛ½Åvu-qÕ¼j.\x0012!×Å~íÕ\x0006äÓçÑÜiHE%Ù*\x001a\x001cöNÈm\×8ÇêÒÈ½âÏ<¿Ü¢Ý¿\x0014¸\x0005F\x001eÉ´ú\x0013\x0019\x001cÜ"<<òb5C (8å¶4HçÙ->aO¨æ~>E¥\x001ckg\x0013¥ekP~5 -\x0000fêóÿ|÷pé×ødB¤Be\x001fÝQå\x000fðtª¤Áà÷¾õèçùðI¶9Ïâºa¡¬\x0016tñv¾x5U0\x000br\x000eä\x0008Wz\x0002wS|mGyóXk¢¹mÄ¢Ë\x0013w gpÜâ9â[ÛköÛ\x0018vØÎåy;`+=\x0014ga¯h­Ð58G É´Ðy ÃëS­\x0015¹­ìI´¶\x0015öVßÏÃë¦\x0013Ò\x0000:\x0019ÿ¸zN+¦®÷\x0001
\x001fPûb\x0000¹°\x000f+\x0011A\x001eÕÕ=>á\x0003FÔ×cö¨¯(CoÒ«èá#\x0002%T®ü\x001ch\x0015¬Øm\x001dà«¯èá+ÎüÉ\x000bbêiîÐàiVmo
©ËÕ%%^õ¦«zu5\x000fèó+Ö\x001a¡fS¼8ZVí\x001dCÇ:w5\x000fèó3Ö©À\x0012\fÏ*Ó
NCÄîêj\x001eÐ\x0015 3\x0008 
t\x001cÿ'@sDÙÓ¦\x001a³úàjÖÔÞ\x0001íº.Ð®¥^¶k«¯\x0008¦\x00049I:v\x001e¥ 'fwôråØÉkRÿýN®ó\x000f¯~{ÿý{¹Þ¿¿¿{üó3½h=\x0006ÃIõþL\x0016xÌ ç:Ô¼_0\x001fèúO6ñl»e+×nã6ì\x000b/ÚÓc8¾ô}ÓÖ\x0010sÍr\*×®wä`Þ(_ llFn£\x0014|
\x0007/µk§Ys³K©&\x001bÙ$\x001aç\x0003/µk¥\x0005Av­\x0018ëWê°Y³¿ªA\x00022¤8Úæ)ÜÖ\x001c_SY$ÔÌKÎÓ|à¥z-¾.­XþÏÄD&.¸¤­tq
_/Õkù/©RTY\x001cÌ.ûy>ðR½VäkN·\x00138ß#gn2öF"Só\x0018sæå¦
Q\x000cí\x0017ùÀKY,\x0001\x0010E§ê\x0011s§%
[SôSæ÷
\x001aL¥\x0016,\x0017-ìP%Ç{>\x001dW9I\x0008^ÊÌ;G+\x000c\x001dÇA_ùFi»$\x0004/ef-åt\5\ÒR\x000232Ò>ouª¡\x0016ìTu\x001bVi&Ìà£Ñ+ÒÜá9áTO/ê'ïøyÒÎY§rzNò\x0013"z\x000eÍsªQ,>Ì3kîYÓyÊ'²xRX-pÑ,´á´^kÌÞÔõ
hä:_5P:Ðñç6:Ú$iç.I»}\x0004×mÕþ5'ý¹\x000b#Ô²ÈÙ¹KÎN»®`§we\x0013Ú9rµÃV\x0003äìÜÅú´ý\x0010¬7p"·«ò&ÜÕIççÑwLlæQ¶óâñüj{½\x000fvû»\x000f\x000fâä\x0011Å¿ÿñ/¯þðîñÃ»çÊE£m\x000e±	Qet1ù·V\x0001½Ý2!|îH£-r8è²\x001fBóò£¿¶-\x0003òiLÅáì\x0012R%&Y3Ï^ø\x0016\Z[º!¶T\x0002 \x0001!:áÉ\µ½ñvö\x0012¿!Y»¢â<\x001eð:k\x0002Ë\x001cïlS\x001c­ÞO+\x001f'ÏÖÄå¹\x0001C:p\x0017\x0011¼-¹¾ÆìW\x000e\Á\x0015_\x001b\x0001ø4~uq0ÒñôÅÙ-Q1Ãs\x00034£2·\x00119rP\x0002ómä^;¸\x0001¹ÓÁè\x001cC!Aíz0Ê@¾¸R\x00074d0õ4#´\x000e7ðt^Ò[òõnÐ§	\x0016m§\x0002\x0013¶»ªuó	ë±w\x000edÝ\x000eÎ³¸?>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=:\x001b6NÔáM\x0006t;Q5VìÈMeTµS?Å6ãH\x001d^eo´)sÛ¦\x0012/¯Ø¦´º¬~À\x001fÞe\x000f¶)kMÐ¿\x001a{#÷¶¨Hìò.ÍÛæð.\x0003:lÖ`ÛèÚÓú]Ë\x0001}}þá«oýÕáYþÇ»7o§\x0012¯ÍMóú(Ñª\x0003Pµnq>\x0005?ªTõé\x000fGÓ\x001cU¶á=ÓfüÈ$«C½Ê´\x0013Õ\x0001ðhàZgó\x0000îjy[¨1\x001e\x0014­\x000eIFC·$cW\x0002¹÷ºÝ¨ÁTîÐÂòÁg=7¥\x0001»ÎYZ=Í×^PÐ\x0017¾0ÉÂ\x000f:@·b|t\x0015]â\x0010óÁm¸ËåÒ+»Öq@·ryTâ\x0017¨9+_\x0000UnUrÑgq}ç\x0001Ýú+ä_¦¢s¦!Q\x0001K¹Üy¢Ã\x0010\x0017ÛG>\x0003y{\x000bÅ0ä³úÐ*\x001fÕZºæUØJ*Låø´\x000e¡\x001fKÿæ¿zýz	\x0015äBº»½~óâ_¯ÞÜ^
~i=½¿~ú¼\x001c\x001aò_|øÇV!\x0017[µ¬¾ZsÎz}þ\x001bJ\øÐåÚ³::×^F%9yOì\x0017òÄc¾C\x0000¿C\x0017s0â¸qr8	"÷8µ·\x001dð\x0000\x000eêðú Â|HXÔ/ç¬¼ï:à\x0001<ÛÊU.<ÓÊY\x001d>Fr
dåã\x0018®n
ô|dsM|±:<K\x0011</p><p>øH</p><p>ÀAz¾z\x0014ïaÑk\x0016×ZàuåÛ\x001a®¡/ÒóÉ\x0003zf\x0016Óäi°WÁÃ.}\x0004à </!Ã/Zx¨O×\x0018wèçÑÊ¬Ng©+nFîË)ÅÚ6ôà\x0008\x0003:ìÆdC¦séáIò\x0005ý\x0002\x001eweV\x0000·Ý\x0018</p><p>Y\x0005=yéK)ç\x0005}PÔ\x001c¼l@í\x0018AÈz\âLdBXO©ß\x000e÷\x0003:ìGåùÃ\x001dÓ¹h¦oÂ\x0002Þw©/\x0003\x000f°\x001d]°ö/ý¦i\x001c1zÚe¾\x0000Ü¶cÇ,²Õiø>E·\qª-o\x0018+÷91\x0005ÐÙ5Ìê±¯è[ú.@/p\x0015ëWôÄF)&Þ0³PyþE­ÚçT\x000f\x0017íýr7¦TØèq#\x0016Ú®¿u¿|¿>óß¯-k·ï^ü\x000e>Ã\x0010*&ó`ð\x000b¹N%áKàÙ)·ÈÐ\x000b¬y¯Í\x001cÌºÏ¦IA±Z;t:
o\x0004\x000f{k
\x0012ÃnT\x0005ÀAH^Y«4\x001eé\x00017.üfñ/v|\x0000\x000e:òµbç¨j>³êmë4Ñ{j»A1\x0000\x0007\x0019ymÉøT
xNw#Ý¿zÙÝÉ*MÎC6­ÒéSÝ\x0013lè8æ\x001aÆ**)XU§&¿'K ¸¥\x0006\x0002t\x0018·ÄTÇ|IC#\x0017~B
Ð0l©)KùZzÉàq±¸ÛöP\x00016ÎZ&è¡\x001a±0O{5O\x0003YY£¸Ýã\x000eè0l\x0019\x001dH\x0011Ên\x001ci\x000bú2±ï&Mäúº\x0003:O[B,¬·\x000eI@vùâ<±_Ã\x0017\x0008Ð\x000bY&Ó'uN$nòIkØuQ\x0001x%ÃrÞ 2XvzHüQÛtLÎÏ¨GzGçH{×ø\x0002p×\x001eú¶</p><p>ÐA¡Þ7ê¿nýpøêêi+ùeàPk)Q\x0006B¼p¾\x0018åþá¥Ë­±Ë\x0000:\x001dR \x001dR¾¢eÊµ\x0015nDréà÷\x0000:SqÃ\x0003]\	ÚìµU>JyßC\x0005à\x0011î]\x0007ÜØ^£¶Àß´y^út6\x000fN\x0015 'ZzÇäI_v{%Âyü'ïÐù9µ¼ÁIRÔ@{]iåÌõü\x0002ë\x001a¹Â1-¬\x000e¡[ÝóA5CN	Ðá%Í	gväùaµfãØ\x0007¨uKç</p><p>èpL#9ÊAJë1
ï¯î¶)+@Ç´\x0014º\x001ds¥\x0016Sè^ü¹ñ\x001eZË\x000c\x001cô\x0000÷¥Wâ¯Ð'¶º£°ë,\x0003l|îP\x000cZ\x000e)÷ÎècÊMqÎï5â\x0000\x001dvºsÐß2Î\x00113\x00174®]¨°VJ\x000f¼CÎ~\x001dQ\x0003\x0015\x001eùSÊ\í\x0012Î\x000c^ó
\x0003ÄCúòG¸\x0003$\x0012çEqìØ2ór<\x0010\x000f\x0019:\x0010\x000f©\x0013\x000fo®¿} úà£>\x0010\x000f\x0001zíèð\x0012X\x001f
mÊd³OÝó</p><p>¼C5y \x001eW\x000céa)\x001d\x000532ù\x0011Ï\x001ex\x0000\x001d>jp }>\x0006àx</p><p>UgVøNîâó</p><p>¼CUsîÈäZÐ»ã»w6R\x001e\x0018
\x001d\x0018KÏt?Ö¾4¢9\x001e\x001eÐûñß7\x001c½\x0000\x000eÑ±\x0015v\x0004øbÏüÞµÁº|àè\x0005l0KD¡±ðø.ñèT!+ç{½À^×Ø\x001b\x0003Ö8òD¸\x001d\x00177£IrnôÂ{=wÝJ½â\x0017£çcçÏOwßÞÇµyõ=úÿz}{{-1í»OÎ\x000fÛ</p><p>ªÜS9µæ\x0003¨=Þµ/!ØÏ9×mv]ÆÔ>3	Tâhº\x0000s4ò\x000b«¸¬a3¥\x0006ØÖ)]#\x000cúµR\x0010Væ^êO\x0003°#¬;ÃÕ\x0014Îæ.\x000b'÷§ºw\x0010\x0000nMØêAÖè/Õ@¹öv\x0002\x0000·	\x0018
î-I1\x0018Hý \x0014:"Õ¼\x001bR\x0003lëÙ¯=XPi\x000cÛ¨÷\x0002v_¦0{Ýuß\x0002¸
ÀkàrØ¸6£S"³q3t[o=\x0000·\x0000¶ièPÉh\x0017«\x0014þ®íT#\x0001ÜÆ_\x001aKJ¹<x¶y!í0í\x000eSj\x001aª5<C3¡dê³ªn[à\x0000ì\x0000fé\x0010ü\x000c\x0015ô°¥\x001dµ©k¥\x0000ô\x0004_4ã¼*fçå²Ísßq\x0003x\x0001£\x0007 -Ô\x001eÖe¬\x0004fVRõ]¤\x000fè°_Ô«\x0007ôE7,t×âlÔÃKs\x001fo¿ùêÀ4?zLïîogcËõý_?ý+#k[2£ìj	E{UNÆñÌÈ\x0007ûièiT~fÓ¡(xj4É©\x001aà\x001c\x001d<P\x0007cÌ½6öæ\x0001ð\x0008\x000b\x0016#9~;¥eáÜ1£­µg\x0006°\x0013,<;!/\x0018g«\x0005;»% s»QhÀÎ­³a@Jì+Íû\x0014WÙ²{f\x0000Ü¤^$`¦IU\x00133¯¼-Ù$·£\x000b\x0001ð</p><p>+÷àCY\x00023{-\x000f-qêß\x001fÀMHF'D!Ý3Hy¯´Â1GO;\x0000ï´\x00111S¥Ýilø}/Nlè É¤¤=P9Q:JÖ×ÉÎ³oÝêë\x0004Ð=íE\x0008Æ$¦àò¬g5½¸K¶\x0003:"\x0015¤\x0007ôºÌ\x0014ëVçfú%t8 gÚ\x0011ÐKgÉ\x0014A¯K:\x0015GÏ÷£ýè|Wù\x001d¤²ÆcuS\x0006tØ3®dW)¢À\x0017\x000c·	zÞ²Á\x001bº¥}eÏ4\x0010\x0015ôð7d_2Öâã\x001d^ÉÛ¯ÞüújO?x÷îúöÝß7ñ\x000f¤\x001c;òÈJºÈØ\x000bðnÅ\x0016¾\x0014ÚÝ{ §=\x0007RçH@½µ¶ø¤¹z q	´ÇLÞú@\x0002¶=òü¡Wk ¡\x0007
ÓY£¾÷¼y\x001f\x0001ÛN¶6)gÀÖ;\x0017\x001eyÝ>ìT¡\x0001ÛÞG\x0015©·R±É¢gí\x0017</p><p>\x00155Ên\x0008\x0012ÀíÒ³ø¸Ä±nÍ)ZfÌú<\x0002´=Úï\x000f\x0004´#5Jwiëe5ÊN\x0015\x001aÀí:\x0015Xõ£V¸\x0002¯iÌkÜ\x000fëë\x0008Øö:&q<\x0018\ûåè2êTiu÷]\x000c\x0006ØvÑ
þudäegægyè\x0017£¤²Á\x000c\x001d\x001eGûAû¡ÒÇÛ0\x0005Þ*¡mKÜîaíÐåÂ©¼v¿®}¤ä\x000e1\x001e \x0007Ø\x0001\x0007íÛ*ÛîU	?iÝÊ!\x0002º\x001d¢XÍ«©Ý\x000bwÉSÏ2</p><p>\x000eA\x001e \x0017°L\x001dúÛèªBÙ2Ýç°È!È\x0003tÛª \x0001ä\x000c</p><p>¥ÞÁ =Q>ãö°6\x001fãµ\x0008zeñ¡¬õ/\x0018ìÝwª\x001am\x001fÞÇ¯¿ý^ÂíûxwóËÿr÷îÝÕýëOÿJºÐØóH\eL
`F¼ÜSüßÇRè4Ãø¡Gr\x001a\x001fÉe·en\x001e`¥àÄû>\x0004ð@à
_2§ò(\0¨W\x0012°­­
µ[lµû\x000b9ïÚ\x0001<\x0001xç]\x0016¾hW*§ôëÆÖg\x0012À­-\x001c¶àhç	%·\\x000c°ÅÐ,[/\x000fÀ¶*ª2âÂÅ/!}g§s\x0011ü9wO\x0019`[\x0015%{ÇuºÈ¡\x0005\x0016\x001aPçÝscèÐQur¸<»\x001b\x001bÀí{¦\x0005Ã"_z\x0012¨»µew_\x0003¶<IüÄ1/ßòòF]ä\x0010üæçw?ídçýáþ÷ÿx\x001eÌP1µ,\x001f7¹Ç\x001eL\x001d	³Æ¼ª-áí\x0006öS`\x0007aK¾\x00064ªz7Ä,<\x0012Ã`\x000f§ÔË\x0008ÀÉ9\x000b¸G2gegb2çy\x001eøk\x000c<ÙÊUw\x0010ÀÅ¯.T_ô\x001dùtåÃ9\x0019¸1Eg%´6^á¬ü¬Ì[
ÐÊBíüæ2\x0002lãDÖAr»0ªÁw²ü»Äì|Ýq\x0000¸¨\x0001
®¦´6\x001bJÌÀÌÜ¡íG\x0001\x001ch¨½''7\2\x0003{Í\x0012Ûöª3t»êNN×Ó'sw\x001d\x00018\x0012Q£f´lÅJ6Ý¨Ø¢[qC.ÿõÍíwoVJÓáýÓï¿}suû\x000cs©Y^\x0000ºâ«Oþ¢\x000b¤\x0014 \x001b#Ô_\x0002iq=D¡xÚ}/´ò!ë|S^È{	»ù&\x0000\x0012Ù\x0007\x001eJ®r4\x0004	»JÛEÌ\x0000^
ÜuL­\x0004mo¥¹\\x001a¯¼+i=|\x0000~9|.ÖBu¨\x001cY+21yFý`°Ó°-ìà¦ÐÂKâ°S®\x0015®·úýè\x0014Ã¬À+Ý\x001aY~\x0006/ÛÉ)\x00001¾ÐÈ*J¬¼-eËÙôtt\x000c\x001d\x0006a\x001f	¿\x000bzc6Ce\x0010çµÇ¸Í&\x0003:\x000còyÊéy&ÃT·T¢ãÌâït\x0018Ê\x000bjünQÛ\x0018:[x\x001e«{HouËU;Õs,ÐY\x0001«&Î¹\x0014·á8 Û\x0018Ot\x000eS	Q®5>¥ò\x0014ðWÍ{Ú Cá© Ñ\x001cÔ£zÁl÷uG¼í"\x0006tåÓÔV\x0005ô%
"÷9+ñ¸R¶£Yn;2HJÙ-vo!ñÚë.<¿\x0007Ý\x0003r÷<²Ä\x0007OSv\#·hÊÿ[&e³\x001cÎjJbì	!ô<\x001b\x0014ÏOS²Ó$·üKx	\x001fÆ\x0012\x0001ËJk5~¾ÝÓáFõ\x001fÁó\x0011ô%_=s\x000bU_Gkx:¿ÚS\x0007tV©.\x001c\ÙçÂ.@-ç\x0014=;C\x001div\x0017\x0006\x0011%8¦ÞÊ\x001aÊhö=t?\x0002z0t\x0015q´Û=«V&ô¥'%Ì-Ï·{NNs9òLE&«Õ\x0017\x0002ÏãaÊç;&Îîv\x0000÷yÙ2!\x0004*
	Ô¶s\x0013Ð¡«\x0008»\x0007³gÖÓÍJ0·3ûùÌ°!ÇÆ±\x001cëËÅê¬Ä\x0017¦\x0010S>ßÙöãè\x0004°ôÂ×oK\x0016Z>ÂóK¦xCWýx{:rkË~Ô]Dèãn?ô\x0002¸mGU\x0019\x0004µQ\x000eö\x0004¾¸Iqó\x001b¬DCÏ\x0015J9¹\x0017f(Ìrt;¯|\x0014ÆËù^/	î¬Õ7\x000eùBà5Ñ\x0015#\x001fa\x000cCïÆb»QµVí|Xyç«7Îq¥rþ\fà>`ö¼Æ-RÊ\x001a@w@\x0003½ß_Õî¯Ú\x0013.]i?\x0019<q­H\x000e~Ñznjv)Úï\x000fÕÐSZ\x001c÷¥4õhÎ
SÍ0E¶:\x0010â«øú*/vmg\x0019\x0001óZW\x00007ÉY]AÞn-Tò0nwcñÜÝlw8°¦`\ DØJUJ]»)¯\x001d~V»Ò\x0013ø	ð5ªñàÉóA±ÞÚtØÃ\x0014c?\x000f\x0008\x0012\x001f?\x001d\{òü\x000fä~ù\x0003²õ{Ã\x001b!w&ÆÎÇ¯\x001cÔW7oÏc¾ü¯0ÊcPéÐ[õ9ór]øÚ§Þ¥êo\x0014\x000fC¯äAÍÛ±\x0003"{·ñÅ\x0016í\x001bß}-¡þª|ýâ®ß~suó\x000c\x0003óò\x000cqïFé9Ç¾M­' Ýt#	8E\x001eèÝÆ\zèc+ Ô¦?k
Ê9¹d/ê®\x001eÀ­\x00038hßÚáäð°'§\x0014Ç\x0004^ÛÑí\x0000¸uÑG\x0007êYÑ)×\x0013aË¨¯¥ºË\x0004\x0003¶5\x0017k¸@\x0007q¢:\x001c{N»Ô\x0019Ï­N"[\x0013}TQ\x0000\x001c9õÿD­vmÖ¼Ö×\x0007À­sY\x0019
\s ÜO&ï$\x000bÕ\x0016v\x001c\x0005\x0000n]ô1g¸º¦2Èä\x0012\x0006óÂ»ßQ\x0014\x0000¶5E~yèz)ñ÷läÃÚý¶ÇÂÐ¡Ï]<cè¢\x000f]ñÐ\x000b³o77øD\x000fÉ.@CÔ\x001d~Qï\x0016½¤A\x001fJ(î{,\x0000=ÀFo0.¢ÚàìÆÅ¸Ð·Ù#|Hw\x0001:\x001c#­.î¾÷|\x0001¬\x0019Æé\x001eÒ]n\x0007IÙã\x0000ÝÅÈÏ@Lû°ö2SFç'	\x0004Y¢\x0012Y ôPx¹<sÕ\x001d	»l\x0017\x0017ØìÔ|"Ñ5MVênguÖfgæùv\x0019\x0000õRPKF¾BfÃ$fl×Pa2tP\x0006\x0019¼ªðR=\x000c\x001c\x0001º_D$â\x0014ð:ÿ¨ Ý´hÏ³QÐ}é«pÒ¿oæÎ\x0001Ü¾iÒL1<Hr;È</p><p>-¹úá\x001f\x001e&Ï\x0001Ý>êxÂÃá	§÷\x0011\x0008<\x0008ç÷£M{-GzxK\x00137\x0014ÉwXÒhÐ>\x000c\x0003¸íT+Ì\x0011\x000f\x0011/Ú0Þ×Å.ã-=Ì\x00038ìx&òÏÚ®rË½ÿ¾\x0019<7tÒ4¡*Ü9«ØK[DÊ\x0018hç·o\x0004\x001dU7\x001dS27ë­³\x000cqÃ`; È6hÃf\x0007ÕÑ~tyñ\x0018'WA<¿}#ìHtè5,ÏµóDÓ&ÑV\x001c;ç\x0007\x0015\x0005Y</p><p>(Å2Ë,`tn¹\x0006æ q<?©\x0011å°¢ñ\x001dêHiâwI\x0019Ê8ËÛ|\x0000\x0007\x0005Zhéò·¸9O'\x0004Ø0#ù\x001aÏ\x000fj\x0004=¬Ö±ÖàµËèu\x0019\x0007\x000cãY:Lü\x0003:\x0008\x0004uJ^l\x000cS*WaüSçG5l\x001dù½A\x0003\x0016!Ku) íÓõ\x0006@ùQ<]xQU\x0017\x0004Ä\x0015æ\x0004¦Ëût= ³:#§ÔË^4\x000e9oìêèç<¤ë\x0001\x001d\x0014\x0014ÅL°ö²\x0014aB[:"W}ÈÖ\x00036\x001c>(ì=&\x0015T/W\x001eé\x0006¨Í\x001f²õnT~%¥,Ò\x0012'÷Z\x0018}\x0016xI\x001dt~-i!oE\x0006E]Õ©#J'q!\x0013\x000f=59\x0012Û¤\x000bzyð\x0007ä[b÷µü?×?àYqK¢1=PíêØà/Wà\x0003×Áùø\x0003â2û´ºÀµg»¿;ïy\x0007ËopÛè\x0017Y\x0010¹\x0010\x0018¿¸c3íÛoÓ7Cÿ}ñç«û·/tåÅ~suûõûëÛ»÷Woþô\[õJé*\x0017\x0015öD\x001d\x0015xHÉ4½ô.\x000eD\x001auî§t¬h¥ÁX~Ã'ë9sX³\x0018r9.ßpù/Ñ½\x0000Ú\x0010°÷öãZâæ@Ù\x0010-ÓæôøAh\x0004àÁgOðÝ\x0011vFÞ	Ý-ãÚª\x0007\x0011À­3Ý°säÑ»Z\x0003ú\x0000\x0002\x0007µo=¨\x0000|¥6T\x001a<í\x0013Ë`\x00086¢ø	¿>Ô\x0000_Èð\x0005,³2{Ö\x001a©#oÊ'ÖN\x0007·?<½eÞî\x0003}½v\x0001ýRj%&#\x0016í¡$´t­Ô i\x0004Iõr0tSéh£P\x000c½U¾\x0012kI8óuB÷x§øë\x001f}\x000bÛþ°;9"7Ï [ fÁ©,¡_xlÍ/ÜáÂ$fúì9Ð\,âr Ó\x0003-*èh\x001d\*þÇôü¥PMXgUýn\x0019À³Ç</p><p>9PÙ\x0014YJ&Ñh\x0001q×\x001e\x0006àÕÀ	6ªg-{\x0001§=æ4Ý³i\x000f\x0003ðnàr\x0011eX¹Ê9D\x0002/WÒ6«eèÕ*ãÂnd\x0017"Ýß..=o¥z\x0001Ý¬®³ÒÞ\x001bºÜÀ\x001d6üe²ò.3\x0004àÅÀÕ+Î\x0000\x001e(XNEkz·JÞ\x000c=%H\x0016ÍÏy2»XÍÞ¦¯vþQmf·¨¹ºô):vûèäÈ¢8À\Ð\x0008²È~È§Ä-ÂòQû\x0008\x0012Ðíj\x0015ØÀ¢e,^ºG\x001f\\x0007S&óÞA:ÈÀ£·</p><p>sr\x0015F \x0004·"ñïêÇ^î\x0016Ð/x©ÎAÿCQé Gk_ÑµÇ¸Ë\x0001z\x0006t,94e\x0010Üó}î¶Rºm½æ</p><p>QþÀ&¹\x0012H]ÑGâÔ\x0002tÛìõ¡Cñ\x0011]3\x0004ÙæefÎ·å2!áÊ%ªZVÞÏYCæ\x0006Ðm¿(SÍ;
\x0000©BL¥+F¸´Ë­\x0000º}ÑÁÁ\x000b»±:Ê\x000b¥ÂÓbÞcÞ¥\x0010\x0000Ý.\x0001-ÎÂfTm%ºz5
à\x000fª+ ßÀ\x0013\x0018Fû8/àÙ-4¶ÅS¨¦CXwïüÁ³8¼(I u\x0015\x0017«»^xéyô\x0011\x001dâp@7»t\x001aÚ.êôG:¥.\x0017ºabÝ¸l¿þøÝ«nVíí~u÷FþÇ3GÉWrÓè.éà\x0014®\x0017TïÔõÿrBÀ<¦=>\x001c\x0002N\x0013/! í:\x000btr.DCPS¦]\x001dSÎÛ\x0000\x0010À-\x0000\x001c)\x001a\x0000W²9L.IÌÉ\x0017\x001f#lc@·\x0018PùÉ \x0014QutÊ/Uy¨\x0013ÖÞ¶1 À[\x000cXc²\x0019ä\x000eM5Ó\x0014ÓÔ¶
\x0001\x0001ÝB@\x0015k¬hø5\x0004TSwÓôë\x0007øj¶Ñ\x0006ÐH¶IdÊ¶!& [©\x0001©\x0003:ßW²øÂèi\x0006\x0010\x0013Ð-Äl: Ö\x0008&OªÊLóâGhq1
\x001ebÌæ5>êæPM#X¹\x000c&úù2)È6$i`Ss×iÏ\x0019~Ýó#K^\x000f\x0011\x0000À\x0007X||	èÞS\d-ã\x001fÀÏw¼I56%¿$$Õ2Ü9ípò¼ö8*\x0010\x0000à\x000bìÉhR÷</p><p>_¹ãT6e^Îk8Î¢~_çpE}ñæý·ÿþÏ_¿¹y{ýìéÂ\hòZFË\x001bÍ²îÃOLr>9ÿ¿ý±ðµlñ×­7mLIW\x0001¢¤¦<\x0003]«ç^L\x000fwÊzp.ðSëbºåXVRv\x001afßç\x000b\x0001\x001dò²Z¸nSqÌ\x0019Wå?áã¼²V×\x0013à3ÀwLu*\x0001\x000fç­*U÷\x0015>¥ím\x000eðvë³Ü:Á7Î\x0017\x0012ÿÚhÝ.Û\x000b\x0017àíÂÕ¦øR\x0001¾rÃI­w|	áp.¿yÿ·Û[ñß¼½zñ_îoÄ{\x0006ê^	²©\x0013®¹ 1ÛpKä¹MìK\x0004ÖÆ\x000cÍçÏ¹í3öë\x0011Öä[ô\x0019\x001b\x000eªÝF|§ºØÃ\x000f^§õt\x00036¸§\x000eeFÍ</p><p>\x00109·\x0017êÀ\x0016ðqþÖÓ\x0007àF¡í\x0005ÆÂ'\x000bï|úªÓò,mÓw\x0008à	À±9¬BåW×#	õ´\x0013ZE\x00007:\x000c_ÁûI§`©,­Ð¼òèw´\x0000nä\x000cºGù{\x001cÝ\x0006ÏÞ@\x00007B\x000c¥µ\x0004mÒ·'ðÖ\x0005LV^ú®7ÐÐ\x0010#çQÁ.âPõÕId\x0011\x0008=ã ÷·ßÝÝä
\x001f«¾åïïï~x9nñ\x000e´ôÈ,!o\x001a"jwÐøUÿÒp£	j½4òZ\x0008ö|è^¿\x0014\x000e\x0010:hTr\x000bK´\x0004yÌÆÚf5+¯lÂé\x0004b6æW3\x000ffkÃ3È¯Â\x0005ø
Øt\x0004¿s![ÊøMË¯mð\x0019+¼8ð&tUÐû4ñ×û»×á¨ýæêÅ®¾º¿ùñý3ìe¥ßb¾~¡$XÓ\x00188Ãmü?H+{ß?Wj\x0006vKí&æ7*ê;ÚÃû°cI\x0001p\x001b\x0015_\x0014îK½ìøHM]·</p><p>7o\x0014'\x0002GÝÒÖ¹GÀ©3K¾dÜ1\x001b\x0002¸ÜÖÐ D\x000bF<¬ò;WwL
\x0000nóëÕ×\x000b\x001f².<P~HU¬X²µ\x001d¿<@Ûðº</p><p>_äFënl\x0014îãu×\x001d\x001f\x00147\x0000O6U*\x000b×Ñ\x001aÂ\x000eÄ^Ô"\x001f`wZ¸q×ëÿÃTÇTh½ÛS\x001b\x001a:\x0008èªB½RýÒn+fa=Te½9¸ºïßß¾:&Tÿtuÿ×«××ï´©ÑeTó {\x001f¿)+O\x0001ÜàÊûþ\x000fòÆ§1ù6ÒÆ	ì-\x001eãâ`*Þ8õåã6Þ8`_¼qeâ§Qô^¸ôÕä]vÞ8G[¸oPç\x0017"§\x0017âÄ7\x000eàÉV.1Ê%\x0003¢Ä\x0008\x0005"ã8B³¨;)
\x0000Ï¶r½£\x0013l#Ç</p><p>Bµ÷e\x000fÎöÙ\x0003ÑªW[yÎ\x0016\x0005Ï¬Lß´\x0011ÁG\x0013ý
ÕÀ;|P¤g\x000fê\x00089ÖÅ&~ËämÐ6H3,^Á(\x000f</éá\x0012ôtL«½ºIß÷ÓÖ¹»ÿúúÅ¯ß¾ùû}öÛtÚèö{\]Ñ\x0007\x0006\x001f§\x0018FM`$&rÖ	$\x0013oV]÷TãÌÃ"éÒ¸,üS]\x0019m4QèÊö¤+£å\x00122jÆkÃ\x0005J\x001b\x0016õpp#Ä\x0014v¤Ï\x001d\x0000;\x0011¶ç\x0018[±©Ûö1y»^\x0019\x0000\x001e
\§ì5Í­R§ SfXµ£ÝÎ9\x0002ðKÚ9\x0001~Ó¹ÎJtßy0x­«ÿ\x0002à\x0005Àõè\£+CÁÉgTÆÜ¸¹2\x0000¼\x0012ø%!3nV\x001aWpºìfaÇ!\x0007àÍÀÅID+¥Ü\x0002N11Ö­t\x0001w\x0000ÏÖÒ"à®\x000fÅ`\x0000\x000fW\x001eGLupa\x000cÝJ,YSÅ	ÐU¬%1zZìÒýîÂ\x0003t\x000fèÞ\x001e^¹\x0015z¢ÆãÎ4¤­\x00061 Û9ÊÊº\x0001k\x0017ÿ7ðn\x000cÑGmë08\x0008à\x0011\x000e\x0002{Jå\x0017iPk³t¿çÉ\x0002t8H*N\x000eÛÑe-ò¸úMÓ®9\x000c°3m\x0018oØÊ\x000bèxå¬ô¦C[Í\x0005@·TtØÎ®X#½ar¿4r×cð÷Ðaeè\x0001·ãö\x0019yú
ÚuX\x0001:\êê¯{[»x<È4%k\x001eýõèóà®8´X\x0001:Ü¼\x0001TB\x001fC	üdd2»O}Ûa\x0005àxóFS¥c=GïôÆV#&=´@\x00014Þ»ÍJÄCÈkôò1</p><p>~Zåün\x000cöKýâjå±ó}´´\x001cFï\x000c=:xíÜK\x0000×/À¦ÁU\x0000l;x\x0007Ø¸[º1½êdP'ÿXÀ\x0003\x0000E×ÝVó\x0015Ð\x0013ì\x0016o"AW²BÞÔ·.k¦â0_\x0006è\x0005ÐyÈª6â_.\x001b½ñFwÓÃ8ÿ¤\x0011>i/aåªúÌ»1Ð4Itm\x0004%¾\x001e	6ðA
Ù6)ÑM\x000e>\x0012QýE\x001bCfOý
\x0017\x000fã\x001cãZY\V\x0015MÍGñ¡ãÁ\x001d¿|ûóûcþO÷W·¿ÿw7ou4æYTXR ¶À\x0014B%-PÃqZ/ê_BB±[\x0013?ìO.	Em$ûi{\_í±c\x0007hc7 \x000bºzR\x0004PÉ+yv°R¬ë£\x0000à«Ì\x0011É
Ê>RÁV¼o\x001a&O½spËUª/hºÑ²ò-)ùDî¸×]\x0004\x000fà«Ô\x0015ÓnsJyå±.à\x001bO\x001f S\x0016Õ´\x0005º2)Còª\x0004º»7>`\x0003¥lÀM°µ	±sã¯éÓÎÑ\x0007pKU&6\x0004ìJú¿z(\x001dïÂñ­n>@[¦RKù°OâÂà\x0016Õ\x0014\x001e\x0018<ÖgÒÀ!QRÆÓ\x0013ù
u\x0007ºè\x0004¼n¹p\x0001é+ «\x0002g«4ÞânD\x0007'\x001fÐít*å¾Éh;å\x0005¨d\x0018OØæ.l½|@\x001eÐ0Áq£Ó<°|½\x000fàv<ål\x0003; /)T"ë\x0012ôºe\x0007\x0001ô\x000cè0W'è\x001d\x0008A/k	\x000f\x0014çG\x0014ÉpÅßh\x00033i:×>ÂC\x0010\x0001è\x0015Ð\x000b]\x0000>q#@R\x0016;^{Ù</p><p>\x0002:á¶Õ</p><p>e\x001dàc\x001a\x001d§åÃ\x0018I:L\x00008³Jw0»JCÒG 
ScØÅ?\x001eà :h¨Ô¥§åö</p><p>,ú,\x001btä\x001f\x000fñ\x000f \x0003kuJ~TÏª\x001eêÚ/Û}ø\x0007V\x0016@*{$Ã©õ°!ù\x001aHi;¿\x0002à@[]ãKx£ã¢R¨!Ïr=Î1ó</p><p>\x001cÁ:Qa;Ö¾\x0010nÈ\x0005Åêò\x0005Ðµº:h»#¼ôV\x0000_Ñü|Þ\x0000\x001dÞÒÄRNÙ\x0018\x001a¯Ý/\x000fG\x001eØ\x0007Ê\x0017@ZPCÎùÜ8¬=\x0006Þ\x0012cíbC@ç´yÚíâ\x0016ðõë[`Ë¹ÛÏOjZ¨öçkcî7];¿\x001ci¨\x001e"OCpRå</p><p>«ÞW»ûBDé!Sq=\x0001\x001dNjÐ´ã´ýo0.pè#¸\x001bí\x0001l8Jê!Án×B1?z+Ü²Ûãn´\x0007ÐñYò \x0000)èKå_\x001e½²¥¶e6\x0001tðî¶\x0017î\x0001­ü°'|Yvû¿oØA\x000c\x001cÈ¼5Çïµ6"ònäû«ÄÖal\x0008°!\x000ep\x000eXåÊ÷,<xtK«?ÎÞ|wÿíû¯\x000fzo%Þüý·×¿ÿvóê9jÅÌ¢Ss)½Y\Àæ)_§|\x0011Åâ}óô#fs)\x0016ë$;0t)É5^\x001b£ti«÷	àP-îÁÃ¸¼ÑØ\x0014ð¸+ý\x0000x\x0004ð\x0000ÒDQsùKÑ®\x0004þ~Wú\x0001p«\x0016ËÅ®fcAL\x000bº¬êËHÈ\x001c¸m\x000c<ÃÊ\x000bn#õ×³Ú}õ\x0003·aC±¸w"þ.ì
êÂÈ)·v<y÷?Æ·×qwò®ßÞ>\x0007U«DU]\x001c|Óó2\x0011üáZ=$®Z\x001bQéç?uûÞÇ\x000cõ0å'\x0008\x0014\x0013JQÃAdvÍÑÛn{\x0001xþ\x0003Ú«X&W) MÀ¹ÖÛð{\x000f"Ô\x0006^	Ü[:´)Ý\x0002N\x000e\x0012ûleË
»\x0003v4Æ0ØÔmmx\x001475\x001d\x001b\x001eû\x000fîëöv×0ð/W_ÝÜÞüþ\x001f÷ÏÑ¾ë9©\x0010ë¨Æ?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-5rxPdPnn3xSQ1T0Q8BwzciPJ73c`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-+wPQTnR+OulO1Xln9EnU1DHHs3I`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8115-6KTeliCYEoDHqZKs4yeDWa0w8Pk`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-/YmNnMsCnKQDN5vStff4qRiH1CU`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-gxl9fRm+lkzG1o0kGZgGnMyi2rE`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `95ba-11MHKgmDzLWNLMDFq02ggz73Clo`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-lWzskkVBBj7jqyYkAI5Y7nn1ros`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-E8Oy+RiO4kKRp+entqRCgPJkyEs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-MutZDW51uMJKvur7DjzBHYC8FSI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-+wPQTnR+OulO1Xln9EnU1DHHs3I`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��\x001f���=��|RCT�C�p�ȏ'��</p>
  
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

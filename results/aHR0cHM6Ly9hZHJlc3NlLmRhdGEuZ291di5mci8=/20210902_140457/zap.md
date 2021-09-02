
# ZAP Scanning Report

Generated on Thu, 2 Sep 2021 13:58:58


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
| Source Code Disclosure - Perl | Medium | 2 | 
| Source Code Disclosure - PHP | Medium | 10 | 
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#3SCm`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=íU¶0I<­e\x0016|3©H\x000bK}í¢¥"\x0007-Å\x001aë÷ïwU\x0012¬¿\x00190WÏ-Ì
SìâzpÞ
ÅÍ 'OÁ\x001a)â\x0011TY¢Ê1³J<
3Èfã\x001a\x0010º½nd[GPUªFPµ×Ø>î<LÃ\x0010§,\x000erß\x0010=\x0019aÕ%«\x001e2«¤AòÁ®:'EîÍ\x0016ºQH<ÂjJV3dWÇñùÅÓd¾\x000e)\x0012\x000fà¶qA\x001eAµ%ª\x001d2+74=\x000bZOqô)rí¢QD6êJT7dUm°ÌÝy\x0008
\x0018Ì´ ©T\6^µ\x0006XºGÌ±\x000fÀ\x0006ÂtûqÁí2\x00037T2y#_=ÂZùV>ä\5g\x0018\x0008þ\x0001\\x00034x«üyµòX|ÌeA¯>î,F¥<\ÎhkÆÉ`µò\x0002|Ì
((á<ÀÑÕ$ÁÃ]C(h\x0004¶Ú\|lw¸¥R,09G¦s2½5¬aÈ½V5\x001aÑÅÂ\x000fF¢ÀdºóðLH^ÖÑ;¬à¬^\x000f2_WâI1êÃí×8¢\x0010ô]?ßî-ØôÊ:ê\x0017\x0006q|¾@²¡7ðáômK\x0008ê®¯Ow\x0015lòõî\x0002º\x000bº1S\x001e!?l#§\x0015ôÈ\x0016+LçsÊS\x000epz\x0006§Õ\x0018³\x0014ËÀ\x0008Ò\x0010\x0012¦!4×Ï©KNÝÏ©Aô$¥ìBLÉïS\x0006:\x0012g£Cv:&\x000c©o\x0002p\x001e(ÊÃFú°Þ»I?\\x001dV>;5¡.-Û,\x0011 â°>\x001cGMï½´Ò´Òá\x001aK\x0005åp( 6Fíéeõöáç}¸®Âuc¸!¨2\x001a×£r3­6<[·!+ÔËÝzÍ¶Û¸\x0015¾z|ØO+õx÷v,\x000b§ÊÆ1Üï\x0012
¸¯./&Ñvýè2{£ðiÇ1gQá]ÊBZÖh·í¤]ï5ä²´íóâÍÃó=Î8þ°|þs\x001f³e¤­\x0015M\x0005.«øXßPù'âëÅëstüáøúîç\x0016%·Åm¡0:eô5g\x0000
ÚqY\x0018 %¹A\x001eN\x00088\x000c®f"\x0008¦¼L+;[Üz\x000e··Twh@y\x0010W·!­o×\x001aý3\x0003Üàv\x0016¸LSa õÃÁM\x0008-U\x0007]ä¾$÷³JîYQjµT,r9×x\x0018\x001c\x00007ëÍU&5W­jÁ	^Þ>=<?ÆcÇÓ\x0006\x0008KSg¨
nEP÷ :\x0010{vt\x0007GWxyúþâú2\x001e@ö\Ì!·jÙ\x0015N\x0001QjOFz;ö^v²ö/·µ½oç\x0018\å¡ïÒÑV08UÙjËvµw\x001bÿò±ÿ8\x0003^+¸è£Í]®^;7£æ,ô\x001aýf\x001e:¶*I\x0003.3û®Úü\x0001ö¿ÕìÃG*3®qb
²7Ê©f±ªÙ?Íc×¶Å.\x000e
#L}py\x0011~\x0010'~Ü.N\x001e¾=ÝÝ/.\x001f¾Ý>í»~	O­òÐ\x0012»"Å[B\x0008®
	põ:¹¸zv¾¸¼¸:}¿RªÒI¬D	÷AK¢Üyô"²!{ÒMiJJÓOi9fß!\x000b)=\x0018ï\x001aùÌnJWRº~JÅ¤D[²Àð4¥\x0003\x001a&Ç¿8¬Èõ\x000b·¨.Yß\x0016'_~û¶x÷ðøñóòîëþIo\x000c³nI¦(ýna\bj\x0014­Á?ùúrµ8y}üæÝÕâÝÅeøÓÙÛóéÄÚu üQÌ¡"\x001f*úÜâ¸(!¾1Mq\x0016½,éå<zP0CÓ\x001b:/Á\x001dÆ\x0013|#4\x000b^ðzÞÂ1*õªÛ(³K\x00037­ÈSVMcö.úmB;bí|\x001d~Î5juÂ\x000cNI@Ö0gpîzuìF·¿ü£·?ýcá±K4Ð\x000bg\x001eZÅb´ïÛ±»éu.ë¦J\x000fü\x00138t¶,\x0013Zb3µ8¥ÃA»æA­ÿWmý¿f­\x001d`Ö á­&ïX®\x001bÅ7\x0003è|=±ÊmîÍ|^/ÿx¸{Ür
õ\x0011Cd4YP XÒhj[Y÷u8)}¸8»Üuëµë©\x001d1§\x0012:(OHåI9No"\x000cõ-uÜÓ	eI({mè
%÷x\x0008í\x0006ò9P
\x0017ÃÖÄë>@U\x0002ª^\x0013¨d\x001aMÈ£\x001ef2¡ÄQ 0ÅdKUîtB]\x0012ê>B\x0001âÃVâ2Ô¨Á\x0014LÈ¤e¸MÒf:¡)	MïG\x000e×*
¤\x0010$Á\x0008\x001bµ¶$´½6t>µUh±iG:&\x0015\x0001j¿¥º}: +\x0001]¯	Í¾\x0006
?é#Ó{H¸\x00107"j\x001faQ\x0014\x0001Þõ"ZF\x0016DBE;ÙYy8ÂÊ\x001bò^wX:ìÈ99l\x0000;\x0011khÈ\n8a/¤xÈ
\x0019ÓçÛ*;öt1\x001e:îêÞ\x000fÎè+<XØ2\x001f6ØgÍÝÑ¹PBMË^¿\x0013ËÈïxz9âJe¿3ÐÖ&´&\x00140ÖË+´¡Â&àxD>BèÆôÃ>ÂeMØgÃHh\x0010Ð£@5\x0000:ÚÕ­
Ò	7Á1TG°\x0017á\x0007õÛåÃÝ\x001e:Æµ£&\x001fÁ4äâ»«\x0015Yí¶¥çµÊå_^mOY\x0010¡(	E/¡4V¨(@ÞÝÃ*DBÛX²$½ÐH=¶\x001c\x001e£
YVGo©\x001dt\x0012ªPuÛ0`át.Ã²ú-Ló¥üFçN'¡.	u/!¤øh~XUWxÒ5VçÿNÀÕÛ\x0000n}Á§d+ÊøG¬Qp´WZc3»!ojÈÞOíIGpM\x0002}ÌXêãT6ÃnÆeÍ¸ìu:ÚÞDð?|NÖìobÈh$¯½bøA5Åû*Ü¡\x0016¯n\x001f\x001e½Ý§q$Âù\x00155 BÌÃ/.-\x000c;¢¦X»c@íU¸@¿_¼:½¸|uº=õE,Æi4,ÒÑ\x000fÈ:?¨]³]§!G­ðµë¿)êª\x0017¯_náÿìU¿\x000e'²|?\x0004\x001d\x001eIúgLQ\x0004o]\x000fSáÏõâõñÓãðv©ý\x0013¬(aÅ\x0018,ø6å ·Ip@ä\x000fÐfk\x0011X\x001f­,iå\x0018-¨ôaá\x000f`âGZ`åæÒ\x001a¹&	åpµÈø»ç»§}I«¨+Jíç^°Ìc<Ýç¼ô»ë³÷;Ö+aÊ\x0012SöcÂ \x0007Â\x000c+MU2\x0004'S~×Kü^Ng[{>ñkÏ'áð¹\x000f3ökãâ|UUM\x0015\x001aNí*T¾\x0002Qù	¢\x0014ýFÁsH\x0014+Qp\x001cÆ,±fjgu\x001a¥*)Õ\x0000¥!AyéMî©1\x000ce\x001c\x00149Ì§4%¥é§\x0004Å5|#ËÒ

ýñ©£9ow2¥^¦Ó\´\x0017\x000fÏ÷·,\x001f?áKùÛýÌá/ä±\x0014ù}nO²1[ãÅÅõùéãËñüíÅ¶\x0012\x0016½>L§AdÝÊ{PaD-K!\x0011yM­ÍÒ6B\x000bu«U\x0005[+o
?ÃKZþ¤\x0018EÊûï
ûQD\x001c\x000b¾!Ç\x0018êM--\x0001ðKÇ¯\x001c£HIÿ]ëeI,ÿO V%±\x001a%6èVA2C£U"Ö¤!©X£©M¼%é ÖÏX×~
ùéi¯SÐ\x000c:>p¾D8¬ .5ÎÓ[P«Ù½Tè|
Ëùýû\x000eL¬?\x000b±./=¸\x0001\x000e\x001fË-·I#»ÊgºeI,G<Âq#áª ò\x0013³Ì£QäsK\x001f°*Õ\x0018°þk|ÙsÅñeÙsAÄ{ôÆWÀ»°.iõ°y\x0005UOp)óØÂ¾¦¡*:h_[\x0012Û\x0019Ä\x001a¾%¹\x0008\x0000æ\x0004Ü¨µ\x001f\x0004ö%°\x001f\x0005V\x0016D0&-YK'\x0007ó}°-Wd{ã¦»\x0019\ÄÒ¦¹\x000eirN*VÖù\`°srNÇ*Eö7\x0012/GYÊ¤Û8ÞÝÓ\"ês
\x0017ËÆ»|\x000f±Pk:ÿÐXèºüçÿ:ýõþîÛþQ\x0014VBMw¬a´ZqÂI\x0012\x0008¾Qü@\x0002
ÓWçgW»\x000e=jM9?6O`\x001aAsÝUX\x000eXé\x0010Îu
¯Ãð\x000eµá`uvýçÛ?n\x001f¿í}\x0001Vw
\x0003-\x000b1\x0019$¨w\x0018ocáü°«EáçÓ\x000f§W»^¤nVuÖ+ü f½n\x0017o\x0002ÐâÝÝÓÃÝ¾óÝãx#3¤\x0001'M8ë /\x0000S·j\x0003ß\x001f,Þ½¿8ÛæruÐðÈ¸\|¸»½®Á·_ö7_yGuÊiÒ\x001dgXÚ\x001c~Ü\x0018ä\x0006ýag§gÐ4øòôòÍÎïÎ×¿;¯\x0007ºÜ/î~ýú×Þä¹\x0001Ï\x001a¯)\x001d=ØÖÁ`5äüøýÙ«·ÿë§ËOËoO·ù\x000fë¢ä\x0014\x00030Â¢"æ¹
EsÒ\x0016·9¤áBZ?\x001f¬©ò¾Z>î½úXúí×<"U!»Ú·\x0015â¤\x0006¶ãËÓíj½ëV	¶V9ùz\x0019\x0016èþ\x001b\x000fã
Á(PhN7ÕÄR½3Yðú8,Ñ«í z]ÙF'eú\x001b|èÅþ\x00199Q\x0012_Ò¸a½Ò-9Õ¸ÍÔ7ÜÅ\x0005ÉÙ+KÜ¼ÁdÜÜ¼\x0013\x0007Ö¦¸\Ilä8xuÉ»?ÌËAÞÈàXGIâR¯$º7\x0003é\x0010¯-yí(/jÒS° »\x000cgj¥ÆÜ
îâ5v½¡Ë²¢jðêi	\x00133o¿þû¿¡oøþßÿ½_%\x0004\x0003¼3Ð×$&Fíãf{éÖÕûc\x0018 yúö\x0014ÏO'\x0012\Ì\x0001wá@:X0çØf\x0011^i|Û¼!rYËYäá\x000cã\x001d¶ìÛ,Â==È\x000bÝ\x001aU6L®Jr5Ïæ\x001cZrÈæNÍém4Øü«Eäz\x0016¹`(\x000cé<TÚÐ¢¥ñp\x0002êI\x000eGnJr3Ïæ\x0004\x0017ã:'rÃüÿ\x0016ÛÜÎ"ç\x000ee7ùÊ\x0016lN\x0003Ò\x0005ß^Z;@îJr7ÏæòÈÍiæ«ÑmîKr?Ë;¥4.èà©5¹s.qµ\x0004Ï¾µà¬×hV$rFSc«\x0011-\x001a},3ÛfM\x000e¡W¡ÏE0¾>½jCµvÖd´Xå\x001e¬Þ\x0018ðÜ~cøÚ-Õpº¥^>|ü|û\x0018«êöHêpBÍ¶Ö0å\x0019**rjýÆ%0`^Ãöe,­\x0003\x0005É½¤¢$\x0015#¤Lá#G$Å\x0001¤ÊQõkMº\x000eÊYs{á\x0007ÑíÑ5ðåò~¹7\x0002%96=sÂ\x0000\x001cORÉÌ®\x001eà}k<\x000bÝ\x0002_\x001e\x001fC:%¥¦â¿¯\x0013úÐ\x0010æyMp;Kxyìhå¤öÓÝHS×/¼\x0008?¨Ê¢ÊÊòc$ý9üpß^0\x001c;·Lî}
#ïÅÂ4ârýMÔZ9>Ø?\x001fîb\x0016%³ÃìQ\x0011^1x¾Y\x0005TjóSfÓ¼Óù/ÏÏü7ñ\x000f¤¬eOÚ\x0004Çúp÷%à\x00011*ÜGb6Ê\x001b\x0011\x001cj\x0005"M \x0001?x)! é3H?ýSzí½Âùýý¿Ld\x0000Y
ø×ùrñ&8ËûÛ»¯Û1u\x001e\x0001C;\x0011üd<\x0006@¿,<A\x0004\x000cÐÿt\x0005ÆñâMpç§g[/Bü?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=~ób\x0005\x0007ª(¦5\x001cÊ8ºµ%µø<±4ìzÅT,~5G\x0012'Óë8bt]	È¡_Õ\x00017Ì¼²­\x0006Á¤kÚ!k>\x000f\x0014HE\x000bkÈ)bÉ fZ}²\x0016\x0004Û\x0000ÒÏ*\x0010]ÊÃ15¤3õ¬¯¦\x0003O×r WN?kw*M70ñËð\x0008ÎÓk7Í\x0005­\x0006ÁL\x0010þ¬Úª"yH[DzÒiD\x0016qNÉ£ \x0005ÂU xõôeÒ¼±th L\x0003ÊÕ\x001chCìJ\x001b\x0002ñÞÒ4*pæn7\x0017BYéxµ 81ý¬\x0001\x0011R>\x0006î`$[\x0011ãíÔª®\x0005AkæVZ3!$õ®)|¼yèÀ%ÆM£Õ uÇ\x0015 \x0016'\¯jAÑ¬·høÓ\x0018;nEÐñ¦u  Z	Ï4q0æäVcàÙu+Ï.m£\x001cÅ\x001e4íRõit¿\x001a\x0004Ï®[yvÓü¸ìg<×HîÀÐ~*ó»\x001a\x0004ý[égb¼@\x0003\x001a\x0014j\x000cÃ3À\x001dyØk;\x000cVÄ­´"1è¡ëJº V_c\x0008;lE<:<¿Òáxb\x0005³\x0018\x0005Ú#\x000b\x0015µFó«AÐùµæ,ÆDdWà:n06Ð\x0013'6E\x000c 9ókÍåPÑ¥(ºßñÒ±ë\x0016K¬\x0006Asæ×3£dWM¼lWMÐ¼YýxÝÄég\x0015H\x0010ìipnN\x0016\x0018\x0000+\x0002\x001fß°aEðñ\x0010VEE(*9ÅµI\x001cÀ°Ì4C»\x001a\x0003íª_iWeôû3\x0017MlÆÐ6H¼Ø\x000f\x001b\x0011\x0010K?ëL(Ö,^±<Ýr\x0019?/hÊüZS\x0016ÿ·,­²4S\x0006\x000c(Æq£\x001c\x0001-YXkÉ pë\x000fî\x000eO&5iaæÝ1}ä^
,¬µd\x0010h\x0010\x001eKqhpÞ\x000cí
 hÉÂZKfDY¢}\x0015¿L(\x001buZå»\x001a\x0004-YXkÉâ¾ Kñ\x001ezÀpk°iÎ~5\x0007\x001a²°ÖÅK?M¤A\x0001I\x0003üexióïj\x00104da¥!C¯KãÇ,®
{]¾Þ\x00197m8_
¦,¬
\x0011Qß\x0015¡á×Ær;g´+ÃV\x0004\x0007¥uÎ®h¡YQ|)1³\x0016¬æ@\x001aÖÚÔèë(\x0001`°@}'_g¦?+94¶å¤u\x0019\x0011GyS{\x0004ñ&Dááht¨Ñ7¥U\x0014NbËRºt\x0007Kï\x00030\x0003¾t\x000fÜÔG~Ö\x001e\x0018O\x0002Ø
ìdÊ´Çé< \x0006\x0013ùégÕõ_z>0¨'H .	µä\x0004ÑTl%HªK?ÿ;×ÿ?þãË¥BÕ¬èÇQ>C±0ï½UV\x0019É\x0019MÄ,çádP¬Ì?'ÆR¸ï°tr/F\x001aÝä@à»#·:dA
@UB²Ó\x0014Z\x001f\x0012¾µí¦× )WÚnâ=XÊO<¿@ÍIÚu á<ý¬ÿpàË6%è¡Vf1Ñüá¦\x0005p+~Vÿ¸Vøl¡°¹3ý|{wýçýâ¦6\x0019M\x001bÉK\x0011gÈû	Ï·ç¯~ßÈ¾>¹ùÇ/ÿ\x000bp³Ôäw×77wn÷r'Åà\x0012er¬ç1¡ÂNëü¿;~uzz|þòìâßÖ\x0010ei¿§Dõü\x000e\x0011(¼\x0006àÏz&aw³\x0007ÅÛZ\x000e'X
@¸©=êÂ­¤º6\x0013u\e±\x0007~SÆ{4\x000f\x001dôÓà¢\x0013
£aüéøzÂqÀ1\x0018¿xèòõÂä¼u2a<?=;Êp0(´%Á;°ÜÛ-ôTy¶	CSüéY'ÅU¨{CîÄªòñô´\x0006µ\x0013
ãTüéÙQ<(%\x001e=ÍÂ\x0016ïu\x0019ÊLU\x0005:¡ø}µ\x0007Êð++Îý¤Q©Vrï^~\x001bÜ\x0002¥Ñ è>`\x0002wP¤\x001dÏ÷\x000bÖ*_èbÒO?\x001d[
åÖ©ÕÄ&U´PçUiÓh\x0017Aiú\x000cgRi©ñR°\x0010¡K\x0013x³ÙfÍ11ôMúé¡\x001cuÛa÷b u*Z\x000fb£îb²èÓÏj&\x0013\x0000(PÁ\x001b]\x0014±Ú*OLfyú Ð>ÙN#;\x0016ÊsEm\)¾¯I7HÑ\x0007Õ0é§3> ¨xMÐ­9¾iÒ¥	_LÓOÏBÒ\x000fk\x0001D²×ãw~©§af\x0017ÇòÄôót\x0016#¨\x0008®ÏrÆ=eÈr\x001aKÍC`\x0014¥>C¬¢
¯þf\x000b¡JVêîj{^\#K9on87ÚG\x0003À¯33\x0013Â¿;?yäªR8\x0000K\x0015ÓÏ\x001a\x0010\x0013ýOîÇ³øÈ\x0014Òr~&þÿ2
\x0006ÖQ(Vcår\x0000Þl¡¤x*xðPjuÚ8¹\x001a\x0004ÕñgÕw÷YDTadD.Êø@,
\x0018\x0006AÝdüY\x0005¢ X~ÐwÛR\¥fNöZ\x0010¼ËâÏº*ñÉ=¯ Ê¸e¹íTýu5\x0008­;Uû4B/à#+\x0004~\x0018QjZ~·\x0016\x0004ÒÏª#Ý/4CIêüSè3¹îm*T¾\x001a\x0004§\x0013áÏª\x0015Á£R8\x0004íUÏê'h}9ð>?«8v\x000f«J[
¶P·÷*LÇ©®\x0006A¥vüY·WØ1!¤h8Y¾Ì´Úy5\x0008\x0011¹Òà%bµ\x001aJ#9i§ü¸aÅFÌô³
$\x0000I+ì+Î=\x00038\x0019?M¾Ð¬\x0004IþR¯Ý«\x0002k¬ómÊYr\x0002c'ëÍªÆÃ~Vaà4¯&À,¦àû\x0013?\x0014Ùi0«A0êWnU\x001d\x001cùÃ¸V¿-gÆúÛåZ\x0010ìEÂU®\x0017©*Âzê1\x0004ç\x000c'àg&X®\x0006Á<®_¹U
Î}£G\x001a²e²\x0004²bÐ!
ßô³ê»à\x001d-\x0010çKo$×\x0012ã³ø\x0018H\x0013¶î'±Á\x0014±\x0004\x0017¯ÕTX\x00125)·Ý\x0005¢Õ¯ö'\x001eFp$\x001fþüpÿùÏ÷+t-tô·¹
ÊD*\x0012\x0016X /3í	?\¼ùý\x0005
[¬ÀAÓ?+q\x001cöå\x0003ö*d1BcÝh\x0008§^¤{pÐÀâÏJ\x001c#,ÏsTcÆ¸Q¸«ÅOUÖÓ¤épégí·
\x001e{Òâ R~þT^ò(Õ©\x0007\\x000fFQ¥µ_
®\x0006VLæ&s\x0011\x001cÓ\x0018;­\x000fìÀÁW«ô³\x0012\x0007;è²\x0012,(¬¬MÖ?$C\x001bGÍ´îÅQÿøéúê¤ òüoxèÍÕ\x0017GÉÃp\x001eG\x000eHÐâ.Ü×X\x001bÇ/ÔÓNo\x001eysò\x000eåQò(EÊË?Ýþt)ªÇ£ÓË£·wûfRØ\x0010Òc®yqÔ\x000c\x0004Ñ»pe\x0005L»1Þ\x001f¿\^±\x001d\x000b\x0016ÜÁj\x0018ZØtñUó®\x0010h\x0016Ú\x000b"l?¶\x0003\x000ePZÆ\x0018_\x001dÝü÷þ×÷·w7·û¸\x0000Ë¥eH]K2Íèã{AüóSON¾?;?={døIÁ\x001a\x0013F0\x0015·\x001eÇ¸\x001cÊ¸´\x0018	ö¡ùyÐ]ªÆTC«)¨õVÅ\x0015\x000fí³Ê2¦8Äjê\x001aS\x000fa\x0002g\x0005Ag<{Î^,7U|ê¦45¥\x0019¡¬¯tÞ¬&Líx1ýT¬\x001bÓÖvðÓè\x0000å\x0000)¾ÐôóÓµ»(]MéF(ãv´¾|ò,¡¬ô\x0005Ó\x001e\x0000Ó×~èC\x0019Ä\x0010c|>@PV\x0013¦ÕWý¡Æ\x000c\x0003>ðlîIS`ñß)§Jn½Õ\x00034wbè£{Ë\x0001ß»òjrÁ\x0014À´Zº³õA#NÈ;Çé:P%Öe=\x000f°9eãä\x0017\x0012ço`\x000fk Òõ¾C÷s6^H¸¡xïäî\x0005@i|\x000c¬\x0012§;\x0000gãä\x001fò!50§â1£\x001c\x001b\x0001\x001cÀÂËÆ(É\x0011«äq`\x0016wGÍ\x000f1îæþC\x001cwh;\x001cwïEÃÔ<\x000c0\x001e£\x0012}ÌtÐvpZõ äÄeÆürôüònïT¶4X\x001c¨º\x0004å0É
\x0015Dá¦r \x0019ñÝÑóãóÇf³\x0015@U\x0003ª^@\x0015ð2»5\x0015e+[Æ?I¦Rz\x0001u
¨{\x0001µ+C
8\x000cvÜ\x001f¥\x001e[éLMgàòÙ\x001aÐv\x0002úÀr\x001eJ\x001aMµ(jW\x0007&Íôª\x0017ÐÕ®w\x0005\x0001Ø&J|N+\x00172\x001eP£¦\x000f5½¡\x0006\x000cÝ+hi0¹º2ÚÌ§gäë×òIñðV+ÐÄ\x001cßÜ\]å¬Äåç¯Wwûç»£1¹ÀøG\x0016G\x0005_*´µ¶#\x001fä¬Äñ÷'çÇ
x/¬P³Â\x0018k<ÒYb1÷\x001bät\x0017<\x0002Q«iÝÏ\x0018¬ªaÕ\x0018,Îs¥¦UÍ\x0007\x0008\x001c\x0004gX1}\x0018Õ5¬\x001e(ÞC/IØlK°'¨0\x001dí:\x0006kjX3\x0006kË<2{ 1\x001b¸\x0004E¹©\x0000û\x0018¬­aí ¬áÂãôê¯H$£<baýA`]
ëÆ`µ,\x0007L¸RìçL)\x0007\x0008\x0007:`¾õ°Ë£tô\x0005V²\x000c
\x000cLíÿ\x0018k¨YÃ\x0018«\x000c»:\x000bÃmÒ¶PÓÎ±!Öú.,Ò]xhaEÙ²ÒjkÇù$åü$\x001f£mý×\x0003\x0013Y"Õp\x0004Wò2¬JÁ6\x000eLy0)-§g5jf\x001a.dç}&R\x001c¶ñ`rÌ¥rmU\x001aÚ¬ç÷t^[ÖÝÑ6.Lù0]»´\x000fÊS·åeZê:ÆÚx09æÂD\x0008¼¥r'Å°¦´*9-!\x0019£m\\x001cóa(\x0004Bu\x0015
oU$H¢yiåôh\x000c¶qarÌa9¿ä\x0002.QäST)6\x0008î0\x000eW6~A9\x0006\x0001¥¥8FÚT÷´<ëÂM\x000bWGhA7Û\x0016ÿ\x001c²_*ð¡\x0016¶ø\Ç\x0011¸²\x0013Qw½Á\x001dg|@ä\x001c|±¨\x001f8U
>Ãa.\x000cØ,Òà\x000eF41
×²Ôs\x0019þãPÑO_HhMãwSn{6\x0006]|Ð£úb°\x0006\x001eé»\x001eÃm¯fÐõæ¡BÙ?ÒØVvîTm\x000cVµ°7\x000b\x000cæ\x000enÖï\x0007+xJ<}\x0007ÂÕ-î ëu¢X1¤óÓ=×îN5qÇ`[\x001bf\x0006}/:\.5ö¢Ér\x0012¡´éO³Ôc¸¶Å\x001dt¾\x0008EÇ\x000c¥¼YUG®+9}£\x0018ÃmM®\x0019u¿\x001bëp´¸_?M\á¶&×\aYÞ?\x001d4ÖÁñöÐ\x0007Í¶6×\x000eÚ\\x00054
F¥ñ\x0011\x0014äbß\x0002]Í¦Ó\x0008ÆpÛ£fÇ\x001a`,F¸Ö>c\x001d
^\
Ó!i#´\x001akoÒ/\x0019ÌØÑcµ6áù­zFf`\x0008·5\x000czÐ0¤ü\x0007ü¤?¦/\x0008ùÅ\x001f/Û\x000cãå\x0010n\x0010%Å¨-gíbäÈf1-ëâý\x0010¯)MVü9Þ~â\x0017{qsû5±^Ý]ÿãöf\x00124n\x0003KsÌLº¦É4,µ\x0002ÀL_\x0007_½O'ç¯þßÙérê¾@B
	ý8 *¼$¯ B`E3pÓ\x0017á~H]CênÈt£b\\x0015Õ=\x0006.FSvZ}Þ\x000fikHÛ\x000fi\x000c\x0003u®µ´Ü9³­¶3ºÑõm·»ÓZAéÃx\x0001ã£sÉ~H_Cú'¹%¿Ï¶èD¯Y¬PR\x0000Ü{¬§~ÆÖþô\x001b ßd!\x001bû#û
\x0010úsR ÅÿHC:¡í©$[?cc~d¿ý1½æW-Mo/ZaY:}íéÅ¤²±?²ß\x0000¸\x000f\x0015Çt¾\x000c[	%ì\x0010~óZB{p`ääà|^]R×Y"Ï0}ÎP2íyJ]²ÖÙá`Úº÷ì@i\x0001.äFñÄÞ¼i÷HçbÆÅ{¸ý«	ØJIRQ±»NÜfºÙ¢G°\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=EC¼
5ñ\x0004°äRÀbïZ\x000b§ä·êÕ«â~÷+q¿;dB.Z\x001fy,Ú£¥ì¯i£¼äNµ)STíHÃ|\x001cø\x0017ÔÐÊ¶[\x001b\x0003Büµÿì`-üJAì=×N¸|«Ñõ[ºEi¾0W v1i9S#Ü¤iÃRä\x001czÃæv\x0011¥!ö$?ØÇ¬\x0011Ó\x0003þ\x001cb"\x0017ã©Éjþ¸È¸îÐäó½Ézê¦üEºyýË§ï	kùÃ÷\x001fÇÄK\x000b~ø­Ä\x001a^\x0014ëAFÆ±pp¿þæíµüáõË7ÇW¯áÝ->©xiªv
°EóÈSB¾D\x001fÍ4{/5
\x0003G£³}RéUn\x000e0æEFì(mÝÈ\x0012$\x00198ªÎE\x000cZÄ0-â\x001c¤Èl!\x0017ñQª04:ø9
ÞíipgUØ\x0006'/ª\x0014¶®ü{(pÍ\x0011\x0001×i\x0001;Ø-¨\x0004mè¥A]\x0012m\x0013\x0006\x0001?/_¯ÑúY´´Í©É×º(§ÛÊË5\x0011¼F¾ \x0011Ã\x0002bÖ_\x001fxs#\x0001IÂpÔ({\x001apÔã,à"W."R\x0004Ô.#\x0012F\x0006ì\x000eâÍ³¾siúÎ\x0019æ,KL6M·Þ\x001a^dÔn+)*b°Bl²áeÆ\x0015q\x0008w½µ]ô
ÄÞ*-®Ý'3
àm÷^0\x0018e¶ÉD^¿['\x0011W>ç\x0010\x0013?a»VR(¨Ñeê³\x000cz8.Ï"Ö®\x000ef]\x001dÐ:q)wj!u{£Í<p§\x0011[xòæA*¾Ã¶p¢¤	\x001813C`Éü®Ñ`·«­ús}æÖÓ~HïË2ÝÙ\x001du#Fì5âIW¢_I£Ë%\x0004Z&À-#¶GÏPg\x0011[-c;-c¹[\x0004hYq\5oÍ\x0011ÍñYÄ¨ì1}Î!FfiKÚa:óè±T0å£öÞÓ³Fg\x0011£0ÏA¶i1?è`Â£Õg¢¶UÚAh½,T.®/\x0010y\x0015¡-ª+Q±?ª¼otJés\x00121¸G·)Ý\x0000[Q£ÒÄYÀ:Ì³a&ÄrÓÚ£$Ð2bh*L¯Ô8\x001cµ\x0004E\x001có ÏYÄÃ6H©n\x0004¨i\x0003;#>*lE´Ó´}bºÊ\x0012]d.ÿ8b-cÄpQH\x0011oÝ8\x00151uãÌ!¦\x0011\x0016d\x0019[n v\x0005©ß\x0010_cØÐ© >'\x00117kV\x0011GÏËÀ]ù79¤HþÝî,â¬ô>'M\x0005½6wáÚ«CNð\x0010ÓÑRÓ3¦^\x0014ÚYÇ\x0011¡Î*4\x001d\x000eüä[4Âl\x001aqÔA}R¾I\x0017ÙÒl
\x0002ÕQ\x0018±\x0007î©w!hÄ\x0011\x000bÖYÀN>'\x0001h5ØDîhq!ÀtDÅs\x0016°®
¦Ùª P_dk\ $ì\x00189ï(Wã"ÀQÅÄô9	8\x0018>b\x00106\x0011;\x0017¯IR\x001aðdM\x0005Bñ\x001cà\x00180×¥
íÑkéI¸Y×áól!\x001ehò10\k\x0003ÂmÔ6%\¾æÊe:çéÔ9PK!\x0003¦­Þ
¯å\x0011ÈòWGB§\x0001£\x0006<qÐ´q\x001e+Á±åþt\x00079+Jx4\x0018r\x0016qP¡DíOBL\x001dõ-ö¡æ¶õ¨;\x000bàÑ£¯Äß¬Ë]"Ó_Í¹gêBnÀ#ÂcSåä¹ù¦Ü½kB6½{\x001c\x0015ØôWs
B~5\x0008!ø
z~\x000cCôG«»ÏûéÛk£xê§Y3ùõ\x0003h_\x0010 ´4/×L4ßë\x0015\x0006ÑÔ\x0015\x0006/þó}ùÇê~ ~\x0019\x001eëu¼ÉËm8W½¢9Ú\x000côâ\x000f/¿~[Ñ~ñêg\x001eú\x0005kTXã,Öü\x0018=µ<má¸<sHàu\x0016-*´8¶xhAk+*Ô!Ä\x0016^\x0014®\x0014Ü4\x0007×"´E
´iáçwQ<ÜCp\x0016mVhó$Úòû·GýÖ	E\x0013,;Éùiì$Ü[\x00032Á¥öã)¸%hÁÏ´:gÑ2
½¯k\x0015\;\x0007×RgÇÍ*\x0008\x0015O
²¥-\x001cÑ\x001dë\x0014\7\x0007\x0006LÛMó98jOiSÝÜ\x0010\x001b.\x001c\x0014~îà\x001e°\x00033V¯°útÑ\x000bÿØV!)g\x0016\x0019ï3ÍmµiófR9)\x0012¿\x0008®ògiÒýfÂUþ,Íú³dñd²Çhadég>b{8\x000bWù³4ëÏLäNªb\x0014´ºUduÅÎ%pCKÓ\x000e
ùuÆh¤K
\x0002OÔDêõ¿\x0004nV\x000e-Ï:4ï	cK½ýÜ¨Æ,W1ûâ,XåÎò¤;#¶ñ5¡á©\x001e?\x0019ì!ÅÃ9´Î*K3pg¼Ü$\x0015­hmüÑ
jHñàê\x001c^¯UÁOê\x0002Bd\x0005\x0014½b´»X|\x001a/\x0018Èö,ÞÔwxésN¾Ahu\x001du·Åhl¢ñ¨¿ù$Þ¬ñæI¼õ]«í\x0011\x0010\x0004¯\x000bRÒ<Ð"^gêmÛ\x0007\x0004x?\x001cøþ/\x000f¯~ù4LøêØ8=QsR)t\ñ¨P²->øîáÕoÞv![« Óç$fSrãmôQx`ÜÖ+\x0013Lip\x001c3jÌ8\x0019h5S\x0003az¾féù¾7l78iÄiZ3iãQ×XÀ#÷Féw\x000fÐãÌÜ0\x001f´3à¬\x0001çyµ°Bò\x0019=\x0012;ES\x000bif%Jñì´*»yUNØÊ!\x00136\x0018\x0017[%twc
#Öìf\x0015¹ TÿmAh¹JR û"ÌZÝ´*©ÄB\x0010RG\x0017e
3¸\x001e\x000fÓ8f­Ín^£¿i3pOwe\x0016Õèñ\x000ccöVaöv^ÎK'E7"Õ±[k«@¶½ÉÑaÈ»iW¼\x001fv=+f\x0010ÿ\x0017Ñnüá~c@;z;
ùVW­1NC.1g÷Y
TNb¢b{3_£vÙnÁe;/Û=Jª|+¥D1t±GÊ=ùÖSU1;7ÙÖ½)\x0015³<»MKjÄ\x0001b¶d\x0018sP7>gÃ\x000cãÄ\x0014ó\x001a2ub4º\x001bj!g
yÖÐÕÆV6Îèe½Ñ\x0014rg\x0018rÔRóR&^yÇ­°äY±pSÆú\x0006âì
\x0004*½3\x0001(\x0016¢ÍNÂ¹hzCÐ£w»Ù\x0008³ÞÍv\x000esHÒY2«Êß
m{tGÍJç1Æ\x000cÓA":ÚûÈuB7±.ÿ8ä !Ï«\x0006TnJ\x00113O),¡Ft=úqÌQcuE5<¿#ª\x000e{TÕ0A8þº\ ãQcÏ\x0001KïEÎ(äAFüvt½\x0001âaÈNß@·p\x0003
qû51;\x0007³F5¢ï?\x000ec\x0006-f\x0017sñÛ\x001cRo?'®&Êj.
D/H\QB\x000efZÈ\x0006\x0019% \x000bLâîÐ
Ñ_è\x0011ºáÕ\x0002\x000eÓ\x0002\x000e6	é@(Ð'­V\x0006Pö&¿*\x0005ZÆqAÆDÀ¼«4>Ñ\x001a0É v©1ëÜ$Nç&@9eÌ(\x001cÅ\x0016[áGëo²\x001dÄÚ`à¼Áø-0\x001b¨%P+Ù\x0002\x0019Ï>{ñÓOïÿúßT±ýü\x001f\x0007\x0017%R[1o­
¾êu\x0001\x001cH3¸bëÝÑcÎ«W/kÁöóo¾\x001c@\x001b\x0014Ú0ÚÃ\x0012£EäMt!¥\x001eGk\x0007O¢
mü\x0007-*´8ÖÊ°\x001d)\x0012ñ@EkÒ6ÔÉ+Ð&6ýË6+´y\x0012-d\x000e1©µßE\x0002
êÊ;N¸\x0004í­CþH
ºÿÈ²½
¶V´vÒ&\x0018Ëm*þV÷¦W¬·Xë]Ö)´nV\x0013ÒÍU>Ö\x00041`m\x001fçÀz\x0005ÖÏÜ¤âB²\x001c5\x0004\x001a­\x0012´­kçÐ*W\x0006³®ÌE®¤¸h\x001d1,U´ÎË\x0012ssD6x\x0012­re0ëÊ\x0000b×Ñòö\x0010¬¬G<ìK8\x0007Vy2ôdH\x0008Ç`ó£\x000b
,p\x001eõ®A«¬-LZÛ:0ñ\x0013e\x0011\R£÷±À]	æèQ÷\x001cÚ ¬m´¶å\x0012ý¢ÞqÇö\x000bx¿RHG]Ø'Á*ó\x0015&Í\x0017f^7êè©¿õ¹\x0007èA°Ä\x0008A¯0m¾~\x0013[\x001bõ
Ö\x000b
ðþÀª\x0006mõl0Énjp4u}\x0012­2\x0008aÎ \x0014SøÝ\x0008\x000c½\x001b5ë\x0015-çÀhÆüFÁFú?\x0005âg·¿øl_|øâ?¿{ÿðõ?¼ÿøñýs,b0Æ=B³\x000bNúì ÇRüòáo¾úüåÃ×_~ñòÍ=üvç*
~»_C;s\x000244ÖÓ¦\x0015
l±NôFúÃ\x000eÇ+NpÔGÜà'
?-ÃÏ<DîsìX¶^¼Ü{Ô=ù\x0003ìL4@\x0015#¦NóÖY\x0002×0i+´ç\x0013¸ÞÚðS?@F\x0005?ã"üJ\x0011Å7À9â\x000f1o³\x0008áðlò\x0007pÆíO@'\x0000Ë¾\x001dhÓq»\x0000hhP°½ìÙ\x0003>À¢\x0011B\x001b¥z\x0008ôÂÚ\x0014\x0008]\x001b\x001c:\x0010g\x000f°Ë`é\x0000>/ÿ\x0002uWÆ\x0002Ú7\x0005×[÷o¯úyî\x0000 U\x0008UÈ\x0013\x0015\x001dû.
Â[XÏ+fìqO;Á~ÉE½ÆjÉÅÌ\x0011\x0012¹/Ï\x0003[	x µ\x0004Û5À#nÉ#ì\x001a{ê\x0011tgÏÔ\x0011\x001a£%\x001dÁZY\x001aµ[\x0004áz'õ(î«&Å=ïð?5ÚÏ­EÚúNÃÛx\x0007=\x000fÔs$Z-ÍmçGSI§Ïá]Bomô:gÕàÄw?þüË\x001fùyì1&8¢Óâ%öÄZ%£\x001eG7áÖqüÝ_ó»o¾îÎ
t\x0006\x001d!Ë<¹	A\x001a(mcqÉÝ6ÿQÐ·ÅÅ\x0004ÚÙyIÇÀôq¾.^â\x0019·Ñ5{Ô+6\x0001Z©W\x0018\x0017!BO^LAÆ¬hÚù*ÐJ=Ü¼z\x0010xª/^x\x0011«¤ý&épôXw\x001eôÀ±öæBÒ^é´×éè-ÇÃ5!aI'YÁDiìeÖÃ;\x0005ÚÍ¶ùïJºÒLL\x0014õHGy\x0013 ½\x0002íÿ)¬Çíe´yÐ¹ìé3gZÇ
J³wÉöZê'@\x0007\x0005:,\x0016v\x0015OÏNQ6=ò\x001c@¬Wò*ÐQó S"bÝ
²"^\x00187Ðp´ój\x00024*Ð8\x0011i»Q+\x0006ÐTá½~iv}ù:§<¢÷Ôýh\x00184uè5;M\x0001\x0002º?>\x000cZyD?ï\x0011©_¬½Ð.\x0010B\x0005xn¯¤
G¼ò¿\x0006}@ÜæîÞÍ\x00081ÌÛ»h¥ÒRÄl\x001f\x001dßB¡U-Ýeö.(Ï\x0012æ=\x000bíPt\x0002Zèænó{_\x0001}Ô	9\x0001Z\x0019é0o¤#)DÅbï\x001c\x0007\x001eY\x0006|\x0011¶fÔ ,t·ÐÄAØÈÂ.¯ f¸ÌØEe7âB¢õ\x001bZè¤,tZ°Ð¿á-ÌÊ\x0017æ\x000e_¨W1púIì@ü],ïmÕX¤w\x0015÷¡é	«å.OKy@äzZ\x0010JT\x000eÁy@\x001a¿ÏÚ\x0010¿«A1èwózR«¯\x0015tÞ&TSä%\x001f¾\x0018\x000e6!ÕW¸[Nñ¼zläþcôÍ0Iÿ·\x0010\x001fS+\x001c,uWènV|ùÝÃ\x0017¯^|ûÜ»!#v{Än\x00161=44\x000f´¶KÄ³ÀÈ u\x0003ü¼|ý\x001e­F\x001b\x000c+qo¶-¢f\x0016ù\x000eLÀ
{¸a\x001a.Í\x00004´É²© í\s\x0004\x001c¯\x001eA÷hó,ZÚ\x0011kZ\x0001è¹\\x001d0ÈÓ%\x000c\x000cJéîm|¨Þ638È¢t\x001f¬gd(¶\x0018eßï«\x001f\x0010°SxÝ4^k¥ÇÈ\x0003í~D~\x001cf*\x0008#ã³c"Þ±\x000c\x0015È	'!Ç:\x001eÂJáôlpÅFðÝçøAÈÔX±×°\x0019Ùk\x00141\x0007i!\x0000/OÀp\x0014\x0011ì¢2kô9«\x0019\x0019\x001f)P\x001fß=Ï,3qhæ¾¯ÉnÇæDSöt\x0018)Ö$ÀDÄ&\x0001¹¥«ü'hPÎ
y7\x0005W}6ÇÆÈ¹ð%\x0000m¬"\x00053SÆFßí\x00195äil}¦½Ý\x0004Ù¡<¥ÇÀýÑ
Ì'!ÖÏO_>¤s±Ù8GL\x000cÜ¿#D_.ö6R\x000eCÎZÈy^È\x0008üÜï\x0017nÐt\x0003e¢²»\x00063XuÿÀNß?ç\x001c­j!uÛâ¬%ps©û¶<Y»\x0012ö%ÅÈ\x0019)&Òk,GÇÔm!ºqÅ\x001cu¼IÓAQ`2\x0014_¢"Þ(EM |\x0003}·e\x0014²Wf>§!o¼¢{\x000e;KL'¦ùª+\x0018wCD\x0015sÆ\x000cYÔÙ\x0017uNm2\x0007\x001d¼aÆÞnæaÌQË9ÎËìÙ\x0005¼/´V?LR	(yêEºF\x0005 hæ#æ"\@ÐGä¤ðâôÏCö\x001aòü
	í
d'Ö9YÜ\x001fP\x001eÃìUNMÓ	Jt\x0004>É0A2¢\x001a02\x0008>9¨Ê\x0005éÚK²þ¨Dú_·C\x0002/ÙªÍaN\x001aó¼\x0017Ìµ/\x001bazHÛKOq°Wa\x001as\À\B:V
/N0E»©ÆÑäÙIÈÞEe5ê÷lä\<·ké	Ñä²©\x000b\x0019Ä<»áÄõ =ñµv¸ëD- T\x000báçï>ýùýÿ÷û\x000fO?¯jNüÅº\x0000²þ¼ªÙË\x001ex8$sëùúüå·_½|øýë\x0017_?»\x0005Àßu"\x0011~gW\x000f\x0000Nzáµ©«¤Ü\x0018r·\x0011õä\x0001:[=\x0000
½\x000b$S\x0019Úê/ ½'xH¯=?«\x001f ¯þ\x0000nË\x0018æÃÚe¥{+\x00070±Û\x000bê\x0000öFB\x0007°>eê\x0004ÁË/\x0010\x0002­\x0010¬?@6¼Ùt»áõ\x0001»¿;2Í\x001eWÑGKd\x0019Uþ\x0010xÁ]1õ²µ!æ£m)³òßEát\x0002\x0015ÏÊ]Ð\x001byo\x0006kø\x0007©K¯rò\x0004hÔ	Ð¬ \x0008¾\x0011»AÌ\x0017í
ñ\x0001 ?OqBºÀµça
½\x0007ÙýJTzÜ³ç\x00137eaì×©NÊÇ@^O\x0017O@½üÜ\x0008\x001f¨è&Ù¼/(ôé¦N\x001e {uì/±g.5.±	\x0002ËÕØbW/vbÎÞyáe\x001d*¿@â0Â2³\x0001Õ7ó\x0016F\w\x0001ö%e\x0002\x001f¥\x001f\x000cgÖ\x0010
z6@>ßºk]Ó>Ø-;a*Ïµf\x0001 ÷`àMC'³1þ$È©\x0013x£@å:Z:A	Lm\x0002Ðný&ËZò8ï§Oõ	V»0\x0002yªÎ»ò\x001bø.¿îÉ\x0013 J\x0005ès5ö2\x0012U.´ô×\x0000CN`ºtr'ïAô·î
¹ËO¾à¶­®DäÝ:6Ê!ìÑ&óC¼»?Ä»ÅC\x0014ÄiY¸Qb\x0017èN~tò\x0010\x001dúý\x000f÷'øañ\x0004´·\x000føg²\x000fÁOvgº\x0003Z7l]y7"Ö\x0012ÍíyX?=|ûô\x0017:ÄOÿïÿ\x0017ý¿cð+L½ÌÑnËXÀ\x0004!7Ík£\x0005þÛo_|G§xõðâËc\x001djøÉÁìðW³v\x0000(Ö¨õ¼Eot%l¬\x001d \x0017\x0005ê\x0014ú\x0000?<ýñé/\x001f?\x001c\x001eàæë\x0001ö>yî\x0000Á\x0000'ö%"ªóîµ\x0019ËrÓ^6ñÒ_ÀÝr\x0002ú£Ûç\x0004\x0007hzÓ~\x0012`´±k6\x001bìe\x0005ç\x000eõ\x0001òú\x0001Z$W\x000f`\x000ck¤ÈóEzFèÔ\x0001¼Q\x0007ðfý\x0000\x001b'\x0014ý?õµ}\x0001<u\x0007³@Þx~ù\x0002@ÉdLdñ\x0007!eÇÄ,Þ;Ä8øboö
 bö\x0003¥³¿ð÷×KÌd¯Érm.ñ*Dÿ÷î\x001côÿ/8G°\äÎÇmØ
!ñ9Ü\x0011ãÍ\x001f£d|ß«FËò\x0017ûFËO\x000fo~ùôôa¬\x001eMKã¹kÑÌ´ÑÑ¡,r½n·\x000fo¾yûâõ3\x001d¸\x000c7ìáI¸\x0018¤ÕÓ,{k¢`\x001c¿È¾±lp\x0015­S¢uÓ²ÅÌ¬]¾1¼¶\x0016HIg=" <öfÑ	­6ègD[<©m½\x001bÖÛGÞv\x0005Âwc}_wû`ín´Öã,ZL×ä-\x0011\x0017·eb4Äp]ßë\x000c)în\x0017EEqV\x001bã\x0015	E\x0003û\x001f¨»oíÖ/G\x0004¼+Ù4ÝUÞT¼bÌ=õb·î£\x0008Ë­ÑôÞ\x0003\x0007åëlÔgåKtì|ÛhëGka`yëd$í¸\x0006ñíi§"Þ¿í\x0016q#Qõåä7\x0008!1ë.ú\x0018Fì5b?6 5ÀÎrÏCå0`×Û?1\x000c\x00184`\x0016±cNö¢\x0014k\x0015¤ÅNDÜkî\x001aF\x001c4âI\x000f¨ÊØÚ»ä\x0003;
¬þ³Q»\x0019tq=ÄYbgMqÚ\x0012\x0012\x0007*PfÐºPë
ÄÞ+­ ÏIÄ%h\x0004¹?­\x001bÔÑCî\x0011â
\x001aoÅ©;?ò½CÙ\x0018Áå³÷î9×±+\x0014V¸8-Þ,K\x0005¨."8 ÷\x0019½N÷Q\x0001'e×èsRÀV²\x0005qä:N\x0001j î\x0007\x0011öv0íírÉ/¼èpd¶]
"¿6ÐiÁ\x001eE\x000c*¼¤ÏY%l\x001dÏé©\x0000x
à " \x0008³\x0011P¦Ú¤\x0000ÎYÇ\x0018(\x0005\äívÛ1jnd&E$bØX)î
âà®q¸½4ÄyÖÛ9ÃexW²üÇf³ÔÊ\x0005ì­ó\x0018\x0005luúigÝ³¡WðÆÄCí´­"\x0006#÷.ö:ÜG\x0011Ge)ès\x0012q6­KöÒPËj¥N3ÂxNk¹®\x0001ZÄ8-â\\x00191NÜ«Et\x0002"á^Á à¨
E5\x0014ÉFaã-\x0001Pâ\x001atÌË>±\x000em^\x0018UæAÓMÄYX
cöFîÝh\x0019¥\x0003\x0018
)ÐL\x0014©NT²eCÇ\x0003GÅPð²¾¢\x0014½ö¥aÄ¨\x0011OFÅ\x0005qäv%S­(ï\x0016R\x001c
æE¬3\x000fÏ<c¦b)<c\x0016ÈâïÒEA#YÄ\x001eÂ\x0016hBâ!f´\x001biwöé \x0008µ©ÀiSAþ»K~Ç{S6JÝ@Üã\x0000N:¤HÓ!#¯Ì\x0017Ï¸\x001c8.\x001eºÿ¾6ª\x0014]\x0015C\x0017åO\x0000\x0007¨«n O\x0008Ëá7Ý°KÅ×â§jYû¶(,Ï±øö§§1r\x0008ÅE\x001bæ;#:¿êñ@ömQOKÿùãÕgX0\x0018ìnÙd\x0001kÍ\x001cZð10)\x0014­ªmh1He\x0010\x001dôFàÞ8t\x0008n\x0008sp\x001dµZ¶\x0012PqÅTâ&¸åç·k$*Ügõ (=\x0008³@³ì)Q<ûeÀBöØ@êcÍ
kÄê¤¥ÞSGqëf\x0005Ü*ð\x0008½v¸A5H°`\x0012.±¶0ó\x0013¥ø©Ý1¬\x0006Hs#\x0017Àµ·I¾zÉ|UÌ\x0017ÉM\x0013¤Ñ×.±	Ög
wV\x001bì6×Bxh.à÷\x001añî:HÒ¯;HÆñ\x001aÏýðÔÁÌî\x0001Êý\x0012ùº'ç!¼Aã´b4°Ço\x0005ª'ñ
\x0013Cºæ²ízÞ+\ô\x0011`²\x001a¦­<UÔaóh\x0003mE\x0003pv¿ÎLÚ]_"t&lIQü\x00100\x0014|lÕ`í,XLÄ\x0012QÁ\x0016W¡á§\x000cûo\x001acx³Æ;i\x001a~3¼ t×Ál|Sð\x0006æq
Üb\ÔA¸Rê
#\x000fÂÕáo|Üüp..\x0019\x0019¯ì±¹ßÁ1\x00067j¸~­ÄÔ#VáZy¸/Ú oÙôãò!¼IkCÖ\x0006/¯[ºþ\x0019®öw§¾ÆÐî\x0017§»\x0005åç!
ûM\x000eB¬]!	Ã½¿Æ­y¯l÷Ó×qØP·,\x0019Öh·õ\x001aýºÎ\x0010^\x001d6øÙ°¡èì£e¼%÷AqÃB¼ó5ò\x0005§äKú`Øö¡÷Äú°q\x0015Ú~\x0015ªPWÊ\x000b~VyÿîÊà­§"Þj|Ä¢¢f+¿{úùáÛ÷ÿõap3IÂ:R1SûeunôÀ,q$öÌÙËï^|ýðíË{ýÜ&
Üî6a\x0014àVÞEmP\x0013d\x0012©GQ\x000cqw¿Ù8ð]ÅëÝfgENÅkÞguºxf×{ú<\x001c5ò\x0015e)Èä6ZÚ+\x0014È­0SçØ_ivC~ð_a»Û*O]+2³°³ÙhÀz=OõG{y\x0002vGà\x000eª8\Q\x001c\x00127\x0016üÔqk7æÛ\x0012¿þ®qä·£"OfEæ10ózåkmKÉ$a\x000b$â§Tå6(Ü`Û\x0015Ø\x0016¸	\x0016=wr§:E×üéùS\x0002w\x001a¹[A^bçÄJk°©6l0ò£\x0005 \x0013È½S2÷nIæ´Èº¹Mg\x0012çW\x00059saÒ2ëdî½2,Þ/\x0019\x0016/-@
ÒÀÈ£50»k¦'|Áy\x0016ä¼Ú¶\x0000\x000fÌJ¨·[w§ÖqS¸és\x001e·¥§¦åj\x001eÕ &g¸\x000cia\x001cùá´×üûï?Ü£§¿\x0017|;¨\x000c\Õ&ëìÆcÝe¾\x001b\x0011½	¡>ì(¡hÝ>®ýâOO\x001fß?}\x001a\x001d\\x0014ú`PÈC@^Ñ0§~7õ\x0017ÿúâÍË\x0017oû½Âìç1ólKÖ\x0013±Ë6É\x000cTt\x0005ó\x0011j\x0003\x0014à´ dÃ±x\x0011rÞ\x0018B6\x0013s¿7*åÝòqbÖËó }âòM Þ"^\x001b\x0004÷\x0013q_7C\x001b\x0005\x001dÂ\x001e´.8\x0002]"VæDK¾ù xX\x0004ïw\x001fn\x000f:ºyI; Øµ©ß\x0008|x_IÑþ\x0003Ð0fu\x0007ãÂ\x001d,Þ%²ÝÀ¦ÆÍpôèÂÆA£RiWiü<°Jç«j\x000b\x0002È¯±\x001cIç´`­á²N\x0011³kE>¿\x0015IòÀãÊ¨2viÞØÙ\x001c8}\x000fu©:cKé\x0011\x001a\x000fc¶{ÎLÚHkæA\x001bÏåIH)Ë.Kç¹ZRìF/à\x001bÓ\x000c»£¿«aÁÔ\x0019îv\x0008ÄzÍÄe\x0008EÎ	\x001a´ aAÐ¸FR\x0014ÚRTcz¹9Áu¨F½àV <æ\x0006:È\x0007ï2
hì·\x000fÖA\x0007,\D°LÊTEÝ\x0008w=ñ;n¢¾ÊÛ Õ:,¨5qÖr¬d$\x0011ð\x000e)û~Á(ê\x0018\x0015jÝÉ|\x000eµC®D\x0015Y'îåñ\x000e£»þ2¢5ÎËÚdOjAV/ôE¬l~Àlû¯áCV\x000fõMÄèø
´ÜDä,ä,AiºNÎIË9-È¹Äÿ¼lZÝy\x0017M\x0012á¥|´óSvÚ¹\x0015Ü]¬Ì
\x001d$Y¶G¬:,èÝ\x0010hC=\x001fÒÝKì]RØ8¬\x000c»ñ\x001aöö?\x000c
ÚkÈ~\x00012\x0002ÆÐ\x0002GVhË½ÍØ¯sVæ>Wn¡q¹cvr
ãÕ1QìT-gy7
;\x0006¾&±A¨j·Ø£?þw\x0002ö\x000fw°V\x0011@©F¦¢-Ì-W\x000eÃÎ%9Ómüèâ.é~­yÜ)|úLsÓþôôðÕO?þ<V\x0011+î»`m]2Dlyu[&\x001d-v»\x0015Ä^½xøêË\x0017_~}ôPÀ ÁîA]\x0000Mw05\x0007SÌ vò0SÜKw\x001bÄ(ê\x0014ö¨SG
4\x001bÚ²D\x001b\x0002ëµI.°¤±7\x000f¸ÇÜÑ\x0010{+ãU
±~\x000576ï\x001c,­\x0003ofÄ\x0000oI´\x0000õ2à\x000e\x0014pú\x0007Go¯`D®É\x0003\x001et?Eä¡»Im\x001c9Ürªß\x0016Gg¸m(8*U»\x0018¹¬Gs\x0015Ý7Óaäa×ùV\x00070\x000bÈ\x0003:q:LKy4ü¶\UÒ)5WTL¬êû©óÚî¼ÄT6\x000bs7\x0017Í\x0014ÛÒoÉ8#úû\x0003ø\x000e\x0010ÐKxE½mI±"ÿÜooèÆ^ëá\x0015C\x0004wJóÅÓÿxÿó_ÿ{Ð¤\x0007¬û«ÆÓ®8&¿\x0002nKÖt7\x001b\x0010î/^¼þöå×/}©à÷ËÌìgöÞ®DLâq¡Êâe[c\x0015"ÊD\x001b¯D\x001fÜ\x001e}pkè£Ma\x0006çÝ#SðeØ¼i/?\x0005ÞZ\x0005>×Ðgb\x0015Q¤7R/\x000b~ßÝãq
=(­¿ëèÐ{J5\x001dëýVÿI\x0016\x0005½é5àjøÏÝX»ß÷BJï¢NbG¼x©­7hZ_rrQ\x001cß§ò=#ú}%ÈêJÐ\x0014|ê§\x0012øÀÝ&PûB\x0018¾í¾Ã¯¥\x001fW¥O\.áo3(ö
üÐ}\x0018~2
~º\x0012ÎÂ÷ÉtmOh\x000fÕñþRéïØÐ	~¾Ï?ÎZ|b°jYª£÷íÖÙmyv8Ùx©ê;-|·*üÔ¦à[æMe[çQÐ÷\x0006\x0005O¢\x001aýâÅ¥Ç\x001f\x000epßm¤à<7\x0014\x0016Ûy©ÅwZsÜ²æ@Ñ\x001cFoÈ\x000f¬ôì¯E5ú¼¾5ø7Á\x0015~\x0002?_\x0019éø¤\x0005\x0016ì¼Óº\n\x0012/\x001a)Vþt%ü¨á/j~ö@,ç
~â-ñà²\x0015E\x0000®\x000f:JÅ0¹dwÒ\x0006_ñVøà¬¸¬|©ôwtY
þªô£ç\x001d6Á{¡\x0011\x0001ïP\x000cÏF\x00132ùà\x0016M~È_\x0015|{Þ 
Zñï\x0001Þkð~\x0015<½Ü±ÚoãÌ´»Q.íØQ+=®*}IgMÜÞ±à³\x0008?÷\x0008ÂÏÁOÊàCZ3ø±Ü"I¯<\x0000¿1;\x001bnð¯½³aßõ)fGw}Îh?H¬ï\x0011¹ V´\x001f¬óýåA'O±«ëÈ)~U×9{ +¨\x0002M;ñ=ð÷øSô\x0008Ï\x0006OQ~éZ²ßñ/[Ó/}xúËÇ_>\x0012ÁÌ¼m}ñ\x000c9\x0001\x001a¥0A&!ûóBo\x001fÞ¼~ñÝoÞ>Ë\x0005Saßöm\x0012ìh\x0016`\x0017µiF³ÀFvÐ \x000cwÇ<ÀÁ=\x0008Ûz·m½ÇícâfE_\x0012)ÞUÎÈ\x0004=Ú\x0001FÊQÜZKìP%*ó<\´2U\x000cÏm8ë:ØQÃ\x000bâ\x0006¤\x0019*îNyhLRIá°?D=\x000e;iØiAÚñ6}H»rv\x0014XÚ\x0003í\x0003£¸Ön·¢Ý@\x000bàYÜÅ"6cÞd¡\x0010ê®B<ÛkÜ~\x000177Yæ\x00060¼@
\x001d\x001a¹¹W4Øá>ââ­ Q\x000b\x001b\x0017\x001dÀË\x0016û\x001d/%[eÊÊØ{\x001a\x0017¶·yÛkÎÂÛ\x001am\x001alï8è}Ø(pzê	Ü1(Ü¦å$n¬/m90!\x0003úÀ}\x00041¥\x0001æ±\x0011%\x0001£4\x001bÌf\x0007e\x0011\x0017qX¶\x001e\x0004·^ôJã²ÞåE\x0015¶[pïå_\x0016~÷L¡yJShq\x0006\x0018\x0000qg{A·iç\x001còx§gÞ[àe¢Ö\\x0017\x0004\x001dLhªä\x0012Yè\x000f\x0012\x0017Ü1ØMµs¼ÌOh5n»VN§MÜýä¶{£\x0018óËÔ;d-ï¼"ïâß3\x000bDJâ{\x0017bÙ400
;»{\x0005v\x000e¬Ý3¥©wt¢%v3r\x0014¶UA`´\x000bA R3¦ß\x000cwk\x0000Ã\x0008FÄ=@<<
Û+\x0013ý¿)Ýl`»híF\x0000Ô'8\x001cò7QG®q%r-ÎûÑ3QMñíñ¨D" ¤Pp]:\x0019\x0016vX\x0010völVÜ%jüß´\x0017Et$\x000c¬I\x001a\x00126jÐ¸\x0002ÚZrÂ\x0002Ó¨\x0011Ñ¦ÍÝ\&ë¬aç\x0015Å¦\x0001_¾´Y°9wt<YAÄa]HÅ¢\x000c¿bQ>'î\x0012K\x0005ÑÌ$AHK&\x0018÷¸Ñ~NCPç\x0008¸#$»qºÒÊ\x000eÃ×ñÆx]<tøVÂ¿ü-ü3B¨R2\x001e	ÿÌÀ\x0006¥aÜ q/TI\x0019á\x0014ÁÓj¶3³àæ¾FjÉ¼L³×òö\x000bòÎÎðªÌÉCÚ÷[þ{gOÚE¦\x0015\x0017Ðvù\x001c</®ÂJ5Ç\x0011ÉÀn°QÜ:ÞN+ñ6q4µ·Ú"ïÌìEÞB\x0007\x00076+ÂÖþ&­øÔ3\x0004I\x0013òFcz+ÎOÀÖþ&-øL)¬%9ViãGÜâÖëneN\x001a÷|,i Ä$)	\x001bÛ\x0018®ïÏ[â¦H;Üô9¯&\x0005·ãÂ\x0014¢¬:Ë\x001bÙõ,á9?µ\x0001Ì\x000b\x00060×¼@\x000c pkn¢¥Cy`ëä\x0018æ 1/¨µÍ\x001bJZcøÍ>9\x0019o/¡öujQÕH2Î×H2Í\x0000\x000bó&$ÞëD¸?,>Û\x001a{Üõ{\x001exJ\x0002Ç­Tj÷Ñ\x001abÚeõVú_Ó¸\x0017R´*¹uª\x001di¤ÍÄ­#fÛãuÀQ¿T^°i
÷û¦ ÷µ.2\x000e_¯*X­ÆçËRÅ»[îe\x0002Ú§Ù2÷\x0012\x0010{¹#+KÇ;àóL
þÀq	õc53è¶«9°Úf\x0010¶uZÞÖ­È»dcLdXòëGö²\x0012$\x0012«×\x0015Ö»ôw ç+ó\x0016&NÞ%ÏMÖ·-ÒÙõ%GQßi]Ñ\x0010âa¾zróemãf¼¯Ò\x0010§\x000bõ{^ØÎòóuIÝë2÷
\x001bo°{,Â¦&ï=júF]"ÔÊµü±¥7	êúÃV(¹ÌpÓ+ÞÓÓ^Bîöô«ó¸[±\x00113!m\x0016ªËëZ\x001dÀï?Þ¿>}o\x001bH(]\x001aèp¡ÛÙÔåDéµWYt/xªÀ®\x0008þ·,Âäî%ÿ4/ùbÊ»\x0015¬ZFO³D\x0002}`ÿéx;ÒmÊ\x001b~G^\x0014Åñ®	³õlXÌ[«ÉuêNÈßÝ!7ü7ìI"3³çd3³ï"<ýæÜ£X\x0019à \x0011!Ë*ð|"Öêeµ¢Sav^ÑSÉ83Ç¶^ÖÚ#$ÅdsâÉµûÝ=îyeÁL\x0000/ØÙHo\x0010A\x001eJ\x0006¸aÿp\x000f{þv"íòÌÜ,\x0003Ì]Hä¿
v¼&Ã§ø[«IÈ§õ$\x0013ùfcæÒlÉ%¤2QÒ¡K\x001d*ðw¿\x0002>­(ÙÒì\x0018\àxÆ?Ù,Q9æ¢r\x0002þÃ¯O«JvDÎ\x0012,\x0014Ýn«Í^(ï?þ
ö\x001f\x0017B\/\x00173{KÃ\x0016âÞr·\x00135üçnfÊAk8\x0015gç\x0015Ú|Ú^\x0003¹8K
+÷)©a¿»=o\x0007©\x0012$ÇGÏ¥py1IØç¤\x001aS_Çåµ\x001a´\x0010\x001ffë3­wl"G\x001eV*$äMæ«Ùómæ¤Å|¶×øËÃWO\x001f>¾ÿé/C\x0003à¶« ¤Èüôàc`Èè»ë^~÷ðÕ×o^¾úî8FaÔ»Ýy\x0005Ù~uÞYØ!x~è\x0001\x001f¥cÆ\x0017A3÷÷]nqØ{¶\x0010ó"\x000b9\x000b»Ä²\éô\x0011©5¬Â
6ô\x001e¨NÀNv\x000f[­)8\x000bì\x0007K»x/{ÝEÚ½
¦ã°w\x0004[q6Å]þ\x0011îä`íc`ëÌ]\x0008Ý.Í\x001dîçî£Ý-ûª ãÂæÑßkv\x0004¡ÇôÐ³!'dJ³ÕöÂÓ:Rrc\x001b\x0019¹Ñt\x0004\x0004woÜè\x0004l«a/¨6\x0004Ãó.EµAndô&jÞpò8îì\x0014îì\x0016pp·GK\x001e³â¦\x001adÃMë/Ã­µ;¯h74ßDÆí@äÝß03Û\x0019¥'ô9Û{^[ôD:\x000b<s\x000c\x0015Ô]òqÔV]Jg\x0017.åo*m«¥mW¤í¼0ÒºÆÄ\x0017¹§MÞ]v¡qÜN9\x001cç\x0016\x001cN±Í²m.Û;\x000f)¼Cwòu\x001c·W·Òù[i£ì}¢=Ê­£È[|Nîîg\x0019ó.j\x001d\x000b:BÁ\x000b|6âpÂM·±Kf3.ëè4î\x0005ËM³è¼\x0012±"Üíè!ù¼®ãwòYa£Vl\¤>¥E%à\x0005Ï
x\x0008æ:7éÂíÍR\x0004\x0018$r\x001bÙ\x0014dYqâóué
=uíqÃ¸62\q#HäêÄí­f9;¨dÒtÒåma\x0001\x001a1?³ÄÅK^ù\x0014jE.u\x0016u°¼S\x0006(\x001eM'ü*E£yIZIpQI\x001a\x001fVQÈ\x0015zR\x0012/JÒ%\x0017\x0019Æ
Fy\x001b0\x000bÞÆy©((17ó\x001d£\x0018@è.;?\x0003;kØ\x000b5\x0007GÃ"l\x0003K\Õ§\x000bîÌY0¸ëî$hç\x000e+ÎÝ9Ç\x0014:\x0000Q\x0008J)¯\x0011yCo\x0007ï	Ü l	À-±LÔ\þ+§\x0019¼\x0007¡.^ÿ²[Yä¢`Ç\x0005ci};ã¦Næ*½Ù\x000e]nÉqØYS\x0017Â)K
>-¡\x0004
]yÁEJ"îÐå\x0019Æ\x001d¬ºÁ.ÜJ[Ð\x00196	\x001f\x001d/\x0008[dÒ}:\x001bÔ­\x000c°p+kó`àÚTæYEïÔy çkjS\x0001u­\x0018\x0017®¤¡-¼
4dà\x0006<oífJÆýÍs£Ö¸¢\x001f\x0006¤·¾ÈÙËr-ë½èGéuô*&~!&)ß±Å0/\x000b\x00180t±OÀªâ\x0010ãBÅæn[\x0013r¤få=\x0018µÕ¥b\x000c\x001a÷¼f\x0003
'nâ\x000eØpÓ¬¶È;_\x0016º¢QòF3/oÈ&ÉÒÐÒvY\x0011\x0003v\x0019EOv\x001aô|à
)gÙ\x001c\x0011KVæsÃ\x001d%p
ÝµD'p\x0007-ì°"lg7å\x000eÈL.§ÄùMè®<\x001e­ó\x0004\È\x0013¨eG\x001eËB	\x0000
«lE	pLZµÓj§.·@*$à}.åM»ë°ì5¸³ÆWp#=¼7Ü\x0011\x001c7¬9zIm¸cccÐMfý0\x0017^&\x0001½P\x0010\x0014a\x000b9±Ã(ï \x0001ñ2SB\x000bêö¸\x0011Wí\x001b·,Å§-sw²ì³`¾JA¬Ñùoý\x0006] q'\x000cDc¨K`ÇÄÍdÿ.Óì\x0012\Þºx$Úþa!l]\x000b%\x0002LWVÿ·4¡;«x¢ê wE´"¦â\x0014<]Ç´Ü®VàgÙNYì¶À½M\§Ú\x001d¾ÿªØ?ûóï«ÉIÞ»Ì\x000b¹0Ë\x0006a&\x001eüÛFÅ\x0006_[K¶²üÅg:£üý§÷\x001f~øÓpíÕr]@çkÈ\x0007d\x001e­4d¿ÿöåë/þõ\x0019Y7Ô»\x0015\x000b\x0015µuó¸m\x0001Ûj!\x0015\x0015gÜÞñðsB?`
Gqß&_*îýàËYÜöR6ÚÕì#ªZ9PØý1v©o¸S\x0011ë\x0002íÍ\x0002h¨ËCª°)çô\x001dhãq\x0005\x001da@¯\x0007ín³¸Û´ $É\x000b/u$é\x0019ud2îtr{«äíí¼M®Àâdù=iû*3:c\x0018H\x0019Fqßò³û.?;'ï»óf«T\Pä¢±5^.ewmÛ8î¤q§\x0005ÜuN±]J"±à,>G¹ÝÜqØ m ¬Ø@ÚqÛüd¨\x001cìæ3\x001d²}?9;8u-és\x00167d4Ü=\x001aJ&pµ\x00078MÉ\x000f¼dâ\x000e\x001awXÁ
ÔæJ¸cñ	ò]\x0007!\x001bîÊÚ(ì¤¬IHóÖ¤$ÄD"5ëf½të¦D-\x0004\x0017á·Æ@Â\x001dï\x001a\x0003OáN4c\x001bî©±§â¶²'/×¹ðpgeM\x0014ÃÓiÜ^¨I#Í¶6\x0017ï²[«ÚÝ\x00196\x001b½Â~\x0005wÕ76ÞäÍf0]§&\x0008YÁ¼\x0000;D&¸«jÒ*\x0010¾ö1³ôèqï\x0007·9\x000f½KV\x0019ùQ$ºXT¦mÄCÃ]ÝÙ\'pë\x0012xýö;`+pâ°µÜEÊ_¹®\x0019¿ µNûøúýÏ!î\x001axÆyà%³â.~sJ.Ï\x0004\x0016¹Ä)×Á y1áwÉü¹ë	y³â4XÜÊ(9ËæGâ/¸0½M¹H4ûn>%O¯Ì¶üÑË táey.W#Ü?Üãþa>.,ñ	ÛI|UÎã7Üýç!Ü)Ü«\x000bÅá\x000bê\x0012hÔ\x001fS¶°½p;Ù¿\x0016+kÐ\x0012vJ(7Æ¾ò\x0017iÂ¾oª+¶\x001fþå§÷>ü×\x0010r,Èh\x0010FÐ`£cµÅ»Î\x0015ëÕ\x000bß>|ûªnÚ~øW/ß¾þ·çñïO
~\x001fñ#
-\x001bøÌÉ[\x0014ZJ°}\x0012ø;ôÇ7>@V\x0007ÈË\x0007Ãóz\x0000Ë\x0007°ávî`×¹#Ø\x001bW9\x001dÁj®ò©3\x0014kÚ\x001c#`fkY¾Ö
 Ò>Uzdíº"ECTëõ\x000c­Ñ~\x0007^j\x0013!ög_OÁé3¸õ3mÃJ Óí\x000c¡FÀÞàÆé#$u\x001blZ¾\x000e%«#Ö¼z\x0004kxø¤\x0004l2¤	\x0003ü)çÎà¬:³ëg²¶\x0001yÄ n\x000f\x0019ÿÏ°\x001b4 3hBÔ©3\x0004G4otHãW¡!ÉÆ\x0010ÓY¿Ð=\x0003ê3àúï`ä\x000cÔ\x0007<\x0007ÊïÐ\x000b?y\x0006oÕ\x0019¼]>C	O
Ðo¿ðÀ\x0001ô\x0019Ï\x001eÁë#,{\x0010¤QÞ\x0007"asÒ©Ëöqò\x0008 $XÀ	«d(Ô£#\x0014Ó!7:ô©(îÎðÃÓ\x001fþòñÃñ\x0019´&Á²&Q&Éª@¬\x0014¹YVðVT©¿xáD¤çn%ÌzõÈ\x001b~<+\x0019eÜÌjà÷\x0018L¯Ùø´"Eí\x001aâºk°~3IÛ°K´r\x0004È½]Á§µ\x001eåe=øyÊÓ/Â\x0001«5Â\x0011\x0016ÌÕ\x0001«7:æ6Ë?\x0003PvÓ¤6q\x0019
Æí\x0008}ZÐGØ
ÂÐ\x0011ôÞ©#Pÿ\x000f[Õ\x0012s·yÀhJüÍgÞÆÙ3ìîÐ\x0019îîÌF¨Úe@/óè!\x000bmKL§}Ûs\x0006	´oußìå¾vÖñ¢¦¤Æ\x0015#ö7ì:×\x0007XöÌ´j¯½{JCÛæò \x000f¶1Ö\x0002àøÆ¿|\x0007|F¡%4~Ò~\x0002?ºÞÜé+ ó\x001dXÏwhº½2\x0016ßl@rØí¬8{`Ô=\x0008fý\x001eðþH\x001b6\x0003ËB\x000cýU='\x000fÕ\x0010ò?ßàì]¢`×­Q² \x000295Óür0a-úTÿã·Ù¹¨ó\x0004ú^<AIþãÈ \x0004è\x0004°þÃ\x0000¯Ô\x0008\x0015ê\x0001äTA³4M\x0005yD.åù@Þ`\x001a-ðã\x0001ý&×iS¢¢ä\x001f\x0001Óg$¥\x0017ÿù¾ücµ]
Î½\x0007já®$S%ÍáÖ`x
\x0000|Äoüâ\x000f/¿~û²±ëw\x0017°SÝ$`ÊË¸eÔ¸õ\x0001
ó\x001b£\x0018è4^¯ðúI¼Ä-eÿ_öhzZHÉxm<O\x0003\x0006\x0005\x0018f\x0001¸Z
=l´gê\x00121ÞpÄÎt\x001aoPxÃ,Þä\x001bC·\x0008ØúMz¹N\x0003
pÖ\x0008\x0010:\x0012\x0012pææ[`*Ô"á£vÓQ\x0001Æ|\x0015N
p\x0005f®*ÉbN2[½±¶"

\\x0003xÿ6êÛÜ\x0014`G¸l\x0013³µz#ãµÔø§ñ*¯á¦½E¢\x001a©£\x0007gL\x0014
\x001e½\x0006¬¼õ\x001a\x001eümKcq«Q8iê^k\x0000+·á¦Ý\x0006Q0©¼q[ë^s¸Åó4`å6Ü¬Û\x001d`Ø(Ä6
Åâ6.#r\x001bnÖm\x0010ñ\x000cO@\x0018¢\x0006È\x0012G\x0008`T\x001b=
X¹
7í6h®ïA^l]\x00120\x0019`+¶è"+ìÛpÓnã·Saå6Ü¼Û\x0010\x0016<ÑË4\x0012\x0006yÏ«î\x0001\x001fä ÁUVøx©ûR½y}õéß?½ÿ8\x0004TT\x0018Dhßiµ42\x0019hm[ÆWoÿöåï î(\x0006\x000bÔìæ¡\x001aYµC¼Í­³7ØÈ[TÐB?Q}\x001eªÝåC\x0005ªµv\x0016+Ó1ã3À]±ÁÒö%ÆÚkìÙ°65¸\x0003\x001a²\x0002\x001aò4Ð¹Hzx­v\x0001êØ	ÛÔ7ï\x0008u7ÊOXõ2Å3X©^Ís~E¦íY6P+=Ï
,N¦QÿøqúÇ\x000f!I`\x0003\x0010¥>mdÉ\x0002úþ+Á³8Æ9}¡B
¼)§ò« \x000b\x0014`ãØëuüuz
ÔO+©Û8Áe\x001eE\x0008Fö> Å_\x001e4P\x0006j¬,{"ùh&Ê\x0004¡lp±Ç ò<Ð¬%ç%J\x0014-u)2ã_IÚ¥bãì°D\x000f®½Guí=N_ûâxÛJ±¥ób÷3ß{ë{­Ì=¬`\x0015V°ÿÈXa·\x000f¦¢\x0005½\x0010æ¾f¡\x0018ñÅ¤¶7Ù`$et>Î£ÍÿÎQ\x0015Õ\x000fº\x000fÿõÿþôçñ¹ú7¬%ãb\x0012+J¬ÒÀÒz·Wöõ¿ñÕóÒ
÷Îi\x0011áYÀå·{ÀsåÃ\x0010{A\x0003>Âx;\x000c|GÒAE!·"ð©þØ&Óic\x0013~gõ8p¯û\x0005àÉ[Ù:_¢mÊÐ\x001aM\x00078br\x0003äð£À­Q*nÍ§âé\x001cnJÞzU\JBW#gÃÈwÅ^Bna\x0005¹rYQ\x0016hd\x0000ÅµðÂÔ\x0002ÜôÇ\x0005Ç\x0007
<¬\x00007{ðË\x001f\x001eª ç¾\x0014\x001ca\x0019\x0019\x0006¾cã"àwl\gu%nâne¤(5¼\x000eô®¥@]²) û\x000féæªj±)È±q²½Ug\x0007eÅmX1ãÉ;x(pÜ4P\x0017k\x0008é:3nÖð°¤áPË×
9\x0012ÍU\x001dJ²~»îBä¨µ\x0005W´¦\x001d30ò@¤y\x0015¹ÛC¾Îª8«\§³+¾³²ï¤þ[FîO\x0007ý\x0000ãÒ8ò /i\x000bÖ¶í&sÃý\x0000.\x0007¡\x001eF\x0018 5\x0018F®ã,·\x0014h¥m_\x001d íû\x0008<¼YòÃjì\x0014r-ó¸"ól6fEÒ\x0016/,nvC>ÀÐ:Ü\x001b%so[\x000c\!eñÌQ\x0018åIxúÇ\x001fT<\x001bj«QÛ%Ô6=\x0002Y`¹qÆ49ýE30Ó;,o§Â,ïVÂ¬ì·z-\x0016ã\x0008ÇÖøý\x0001ÓQäèThn%´ýtÜÓQDz¯}Ð_>}øð~\x000cv	ÈÝ£ìÀ4ÜòA¡ó\x0011\x0007\x0014§½~Ù\x0007}cª&ÐwDÕ§P\x0013\x0017\x0010/\x0008,ám+ïÄ¬¬3½Õ'P':­ FÆDKà\x00186ZY8G=\x0002\x0003öÑ¦½ö&aö³YÐ\x000fbËcQS§\x000b+¹í_îûAIï\x0002ñªÔ° Ö6
Q¿Ïx/`ÌÑÊÚk\x001cØC6ûF®Xqß+ÄíxÀ¾hvæ7ør\x001b·ef£z\x0014÷­ÜZqg¿Û\x0019Iìé\x001d³1ÞÇ,
FÄÍuÙÜ­k"Ü÷ëNá&r®ÈrÖp¯zL	eåò\x0008ßÈ(îÛtÅ}·ñ\x001cîib¬É\x001bØOÆ\x0014ì\Î×Ùm\x0017~Óç\x0002î L­Eÿ(H©¸étHcÆM`\x000f÷m\x001bOÅ}·ç\x001cî\x001b¨ñuè­âÌ¬\x0018³ëM(ÀÂÓ\x001aî¼5¶Mº\x0005¶h7ËPïögTï~·?ã5!¦{îMÌÏËX{õØë@?£\x001fÄ²ô9ï,I5Øë\x0014ín´ÏX/4Ü\x0003$³þ}¿\x0000¸zøwó¨­ç´HÑZK\x0007\x001aÚ­ÂÒ\x001eXë5
û;Ø?ÌÃvRöñ9JÇ% SÖ-Þ;t\x000föi\x001d\x001eÛÑ\x000b\x001a ù¢ßýòç§\x001f~OïQxú©d
O?\x000f>I94\~pÅh0±HÁÌ(9\x000f\x001cÎï¾ùêÅ_¿¤G©?¼xUR\x0017_¿9Tî
zVÐó
tK"UO\x001cn­? ²!\x001dò\x0010O!ß+rU^\x0010zqÈÈ©@ÛGÞ¡QçK£BKÈ½åÕuV¡·1"\x0008ëlÑ¸£¡)èÛëZN¯kÓÐiÖ\x0010\*^¨=¯3üdB«%\x000fÌÊ\x0014ôm÷rNµê\x0015}\x0011\x001eeGÜ!¸\x0005{Ü\x0002âÑÎè9äJ_Ò¾ì6}AûÛ\x001dõ\x001eÙ(£\x0017ïSÈé5S³\x0016Ñó¦f-úÝ_ÿûÝ§?\x000fÁFZËhÛäq*.(ðÄ%_Ð¹·Åîm±æ¿~ñU\x0017ò­ Ku³Ö)ÈÅb\x000b¹ONûÑ£}\x0014É\x000eBþÛ.ñ¢Âóx©a§ñ´úT\x000c¹\x0011\x0011sQMRw0zLÆÖ(µ°fA/\æ\x0016®\x000eã#ò$t¶\x0012ô¹Ç0Qr\x0006³ hj9½5Mgü4Ì\x001b\x001fswùÛfGØã,âX¹Yy?ê­QÔûdr2oPÌA©\x0006yÕ°4×ÜÙ\x001b¥³·
¦>gÄ\x0018èp¸!Ðô9
:XYfIMZ§\x001f:iG&&ß\x000bt#8¥ÍÁÍk³µÒ, 0ý YF\x0000bN{\x0010±ÓÝ4bJt¹íÓ&!t	Å3n-ßW\x0018æà¢\x0006<¯ÉTÀi\x000f\x000e@è\x0012\x0002HËG#\x0000'\x0001k-vÓZ\x001c©ãwÒ¹íñ7\x0004ge\x0014+÷«c½Öb?­Åö1ÉBN¤·¾¤.²\x0001:
¯@\x001c4â0¯\x0014ÑH«-å\x0000-\x0004
wCNfÌ¼ámÞ­\x0018ÎÎ¹¤ä¼ÑÒ\x0013qmbÒÂN'KX«²CS)ðfÐ»Ý/Fó«Û«]1È'\x0013"ñJUÄ±Ò\x000f>\x000f\x001eí¾yÛ|«¢\x0012äÓKFbùqX[r\x0012Sµ ö]¿7x·Æ:õÂ,boÌ#w¹ÐÂZ\x0015#ì\x001c^Dïº\x0006\x0011\x001f½ W¸	öp\x0013L\x000b\x0018
/ì ÝDDYP\x0005\x001ceÉU4}'=&ak\x001a[3­Ç\x001e.\x0015\x0002¦\x0016(\x0003\x00125p\x000c¹oß\x0006D¼ì\x001bÞ8-ã£ÈØòû\x0005\x0010ow\x0003LÕ«d4æ4-cg¥s(Zä\x0001¢ÒÒ\x0010|\x0013xDÈ ®ù{çoíeÆq#îDQä^gö°1+Ì§1Ó±h\x000f \x001cµbt½Ö!!;}óÜÂÍËYÆö4ºm¨,qÛ¬Ù{Ô\x001f\x0015²ó\x001a³Æ\By\x00199ð+\x001c¤mÑwè\x0013\
BÖ~ÚÍ;jqÛ\x0016À\x000bL\x0001³GÐÓ+ô\x0002@\x0003ö"P`ñåu²£x£`	9]%ã e\x001cæÕÂ\x000bï\x0019l¸rA#\x0006¢\x0016ýsDÄ!h¼Óö¦\x000f\x0019/m\x0000ue\x001c$\x0014êó:\x000f8+óæò´y\x0014xÛ\x0006 §qOB½L$ÿÄ¨E~NÄ~GWðzMw\x0006o Í|â§&¿+`¼­Í\x001c
Ý:"ö>hÈÓZ\x0011ÚæÃæ¦<Se>Ø^Sõ\x0001N\x0000Ìë\x0004"W!Ìºiq.	ãí¾\x001awð\x0016\x001e[nJùÇîûá§ÿ÷¿ÿÏËÿéÇ¿¼\x001f{Úq1ÉÎ/ª\x000fñ\x0012*\x0008wi\x0010iYçéõáÕÃËß¿úò»Ï¤§
÷p«ÅôçÓÔ*\x0003÷A~Ñ\x000c;\x0003næ8ð¬\x0004×$¶í%6Õ=E6iþþîaàvW#ïkqç{Ál;@l5v»3ðîÂ\x0013À£\x0006\x001e ©ÑÕ\x0017àQVQ\x0005Ëãã©_`><häa
yÑrh\x001b\x001d\x00155\x0007ámLÖtw
#ß\x0005Òæ>@¬ÈÜ\x0015½1,óÌýö\x0005ywt\x001c¹Uj®çaÎ#Ï(«nAnýñ\x000b$ò^ëÏ8ð \x000c
 &;àÍ\x0012Mä¬,N\x0016óYÓ\x000bTÏ G\x001cW\x0013WBãÅ¬ÈyÅ]\x000cÌCQ÷
çãÈý­áû=;ìÌwÊi®´ÊÜ»MæÝØ#È#êQ\x0001ª¸iÜO\x000f_|ø_ô§ï~üùãÃË¿||ÿcg\x0000°;©ÀËíW®¸R¾ª\x001e{o³å\x000c/\x001e¾xý?èOß½øòë7\x000f/¿{óò\x000f\x0003'rû\x0013¹ËN\x0014\x001dí¡\x0013ùâ©"\x0008¹¼ívKNÈïOä/;QðDÒ!'jOKÊÛr¢^3ùô` ¸ò'j#pÕà¶*\x0000ýD¢t¶;\x0018<}¢°?Q¸ò'òr¢ÈÅqúþþ\x0007û\x0003Åë~"ËÏ¯JcsÃQ1ONÔå±>\x0011îOWþDÚ³(qµÌQ
XNÔÛÔ2¢´?Qºò7jS\x000f\x0001¬¡ßý¯\x001bEÿ>'Êû\x0013åë~#w;á¤~#¿¨ØÍè6Rý«¹òG²r$Ç\;ô#Éz[\x0014æO¤#ëBò#¹ÚµY2ÚååHöï\x00142Xí`Õn¿µ3yyßH ÇB¶ß%\x0003ã¨!
ÏûL\x0007Õv «\x000fd/;MBéú#Ñ\x0018F»IÖóìp\x0002ÛÝCt ÃÝN|&Ð7	®»JTëiW\x0017Û°½\x0003É\x0014 ?ó?ó#9§bza¯9ËÛ|CÈ×\x0008;LÌ wÇ\x0004'oÊ8¸xu \x0008Õ°\x001a\x0001\x0005·3¥ÞÚÙ3ù B!\x001f.\x000b|9H{h\x000bX²U¦ªÄõLÝyßY{gý÷\x001fß¸7\x0011ôW\x0017) -¢\x0010+\x0011[UÏÙ\x0010Dÿlºü·ò>êt¶üÅýäû{\x001a\x001fzøü§§øÓð\x001c\x0011µ´Õ)Êª\´F\x001a£1v-øw\x000fo^Ò\x0018ÑÃç¯^|]þöp\x000càöGpëG céívåmHÛº$ýóníÜ\x0011üþ\x0008þ#\x0000<6òè\x0019²MsÙÄ´,q>áÜ\x0011`\x0004¸@"ðe÷	#s?¡I²§\x0005qOîþ\x0008½ëp£i¡SÜ±´Ì\x001d\x0003¶m¹©à\x000e<W\x0017dä\x0008»M÷çaw#Ýt«ïGºç~\x000e+£ô)Ê\x0012\x0014bÝ\x0017j8¡QÝs\x0004}+~\x0010q\x00067Ú I9,¨D\x0003S¥'Ïáõ9ü\x0015çÀÊgPg9¼e2ùbg7Ò\x000e×8\x0007h½Kô
e\x001dSJnÓ«$[½1õ¦%&Îµ×Ëø½Ì\x0014^Xw²ø½(
îúû±{-ª®Ï\ñ{\x0010[ªÛ\x0018J\x000cëóü{$\x001f.·WÎ*ÿçì\x0005\x001eÐ%Ee%\x0002æø\x0017­Eù= ·\x001e{â\x001c^9Aú\÷äá¶Ò èUÛ¶ÎD¡J°GÓÜ\x0005u9èó\x0002¥J÷Ëç\x000c¼\x0001¶2Èlùá¬óüoáo\x0003]5¦òxÁ1¹\x0007\x001a=jOdhn\x0003©tù9ò\x001d>\á;hs_ëé±5Á`*éô2¶ÛEpþ\x001cIãùiî\x001c\x001b%½uÙh±Ü<@²yò\x001càÍ\x0005\x000f\x0014Z<<Vê1²,ÌÝ¡°cx}+L®É\x001cZ-Ñ¢°ùm]Ì\x0008ùÏÉc\x0004ýk+~
³mw³!=\x0006N<Ü¶DÆ÷Æ§gÎõ9òú9lF&"\x0001¢JãÀJ^Él]9Pù\x000eÀ\x000b|Í²\x001a¨ã\x0003ÚãÃ#áÚlF\x0005Õ!â5Wc?E)WC($M\x0018!";ùcdU\x0018|Ai¤ö´ð\x001c«\x0013ûí\x001c·Ý½¦æ³?FF}+Ü8íÝ`V¤y;Q¨Ë¯÷nZN¡¦EçïE\x0012nl\x001a»Û!S\x0007Öp	<×çðC8új\x000cUÊ
)¬IdS©\x0010Ï\x0008ñ\x0002a³\x0011\x0002ª[y1R1É!\x0006(ÖÏþ\x0018ºX\x0015®¨V\x0015«ÊuC \x0005¼T8£DþÊß")Aëgî±ý\x0014µYÉLAVTÅÞ4ÎÄ/Pâ\x0002#EûÕ@vî\x0004^eW"Zå¿CÝ0ê\x0011/¹\x00194_ËKcJÚÑÛò\x001bl7#÷\x0006l'Î¢Ïõs@ØÖt51¢Iìx}Q\x0004u\x0011\x0017/)âÒV\x0002Þá\x0005aË4P
¸4À3æ~£ÓpWh\x0014È¸\x0004PKT\x001f+TèB·Ýæìá\T7¼~/\x001f¤¸ÓGY§d¹5HGåÇ@¤\x0013KíWÑK<µ_E¿kð0¯ÅÄhöÉF¸²Âcleúºí¦Mïu×ôO?½o+8_|x÷Ë§¿üøþÃà"NKD­Ì\x0006¡¥¶\x0010W¦6\x000fI\x0013ÿW¯^¶5/^þÍÛï¾|ùºüæõ\x000899½\x0015ä^BrÒgëËMfè>\x001e®\x0010¾±¯B§ó\x0002ö`eÞ\x0001*öÈ³e>Ä£¸\x000búAóHÃí5n¿;6]÷Å¹5Æ\x0008ï\x0010·ýGãZS\x0002¿Ü
xZ\x0003Ø Àä\x0001Dïä]¸`?ê\x0019Â\x001eµÐãÐ\x0013¹ôÈÜå_\x0013\x0003ïöÒLAOÚ¸¤%ëB3Ìçí©fÙôÜS¸Ë9éhUõ\x0004ö\x001d£7a¯ÞkØ=Û\x0017\x0017yãUÁ.JÞ]i\x001aS¦Ñ¹%ÛèÌ´\x0000ÑM´ÝªØ\x0019{¥¸\x000c»Vw·¦î4\x0015Ê±\x001a=\x0000Ï(\x001a'1gvG\x000bï§°k¹Ç5¹§¸¥ÃÙÜa\x001bÂué¨ëq
ûn4°Ólè<vo^DZ*/{<@\x00189\x001eí\x001cÁî­Â^9OV°GYØ^¢`*6ì|Ui¹×ÐQC_2\x0004]VKCÕí°h¸Ã|w
{ÔØãy/\x0011£ìÇ\x0005éÄö>Ý°_©2p[ÄHØés\x0005»µÔ\x000c/Ø-»&'®É\x001dÃOa×a\x0018,aÂ¦èBâwÌ\x0002]ªêîðál\x0006{Ð¡oX\x000b}+¹Û\x0000qÜªXz¶Vti¿ú÷§¿þß±D¶¦¡<;yÊOßøbÎ½e©o\x001f~ÿâ÷/¾<Ö\x001bÜ\x001d3\x0016Á½cÆ:7\x0013µTâb¿\x0013Zû,\x0005òOtIM\x001aÜ0\x0014âàV\x0010ÿÀ*\x0005±¬£-?eÔd\x000c2jÈ8\x000f¹ÄãmwñüÜ\x0017Qb.©ñu{T"k¥ÈÓJhz_±\x0012ò¢HLDúÀx{å¼A\x0011{­Ç~^\x0003Ñãb#xæ\x0002KÞ&´¦¡·\x0011h\x0014ò/­BÖ|iç\x0014YÈö\x0018\x001f\x0002+²TÌ\x00009Ï\x0018â[5¥"Nö\x001f\x001dñ\x001e\x0010ßÑcR\x001bg\x00138G¬já¹U\x001dïÓ÷o\x001eÜHc*^ÿá%ì´ÝC1YH$\x000cÃ\x0015ó!\x0001;-`7-à6\x001eo*ö³¿K\x0008\x001bÁt?o\x0000oPF\x0002Â´À\x0012:;àg\x0015Â1R=\x0015¸×ÝÕ\x0008\x001fõ\x0006\x0014úÊqûæÃÓx­-øñý§ÿõð/¿|ú0XðöQµ¬m³\x001cXéJ9bòzóúÅ\x001fJÀÖVC|ùòíÿxøoÞ¾î¢ß5e\x0016ôÔñ²¾h8lZ5×¢¸b\x0006@sôÎ;\x0007ßjáÛeé'Ç\x001bhJ\x0014ê·\x0001³ÙCjäIüAã\x000fËø&A\x001aþ ­Yfë\x0006rGëæfá\x000f«ð³´\x0010|Ô[,±\x0012ü]\x0008ßæ^à×6÷\x0015øÎK«>Ðã	N\x0018t[gÿÿ©{·ì:äJt*g\x0002Âò÷cñ\x000b LÔ\x0002\x0001^àj}q\x001dd¢³ÐE\x0012)<R]õ¥iè·ÿúNC3ÑH®»Yðô\x0013\x0011îQy-5*Um÷0··m«¸«­øC?tâG.LÆÏ¼à\x0018\x0017ø¡³¯\x0012ö6âßÿ\x001fÍ\x0017~+w\x001d}\x0000\x0001¶mT-¬à¯\x0014=3xUÈ>þì\x0004ïiãv/"çz©uò5^þhv\x0008ñãìP\x0017~ç`\x0017\x0003bïyN/¿ÚØ_Bxðg\x001f~äãf\x000fÒp'¥TS+þ·Á7¥æ7½?m\x0007äB¹\x0019Þ®\x0019V¬(úãn\Äî;½?ZtÆ
¬\x001f\x001bX{.aãÓe¯!rz\x001cþ\x0003×4»RªBôÓï>·
#ÿ0Ì;ÐÆë ¸'L\x0008¿¢â\x0014¡è\x0016!ËÕ'DÈ#\x000cn6çÃYtfxá\x0019ÄÞl¸\x0013%·ÙÇíË/ÛûÏï\x001eç
éÄÿ'`\x0015FY4á§©7Ò)|Ä\x0013Sú\x001fo V9??½:4±\x0006\x0000{1¿´\x001c<ÊKÀÂ©|ë.xÓvr6c\x0011v[`·ØM¤\x0010\c£X¦O®8^Ü1r\x001f:k\x001eþ\x00061áýÌqØ÷®åä\x0010â\x0012ðrì(W²d\x000fm@ïúYc£Kà{ç|:qÙ®ÞèM\x001fz°V¤Fk\x001a\x0000ÅÍÒ^Å©=)ËÐËòîeçÝ£Êì\x0007Ø¹\x0010(½@;3\x001d®Z_\x0015¼-ÁÛNðæ$5®\x001c\d\x0000ïW½y]×}àPÔ» u.\x001eQ¯/£÷Ó¤ÖÐû\x0012}®DbOR/\x001d¹ÇØ\x001c+\x0019½]\x0015}(ï>tÞ=ö¼äÅ¥à\x001f\x000cc\x0014V±ØÛe\x001aço J±Q½bì^daå.%\x0015\x000c{\x0007nj[×¢7²°SFv\x001a*PÚ\x000eÊR\x0005V~reì\x0012ôðDÕÞítÍ¢Æ}^ùî¥ãëJÖZ\x0003
ÜAr\x0010F+MÀ¦Àk:ûòëöé)·\x0001Í»íýÓÃ×]\x0000Æ&èÄhå\x000cU\x0017´×Ô\x0019\5|öîýñõuî\x0003ÿÐã³ëË\x0003m\x0000\x0004~G|à÷¢\x0007¼÷4ï\x000bà%-:Õ\x001e÷ôe²¾X£­j\x0002/\x001bÇ=è­Lîµ!~!í¹\x0008\x001c¬¯íª[\x001eÐ¤nõ\x0011{~µGeó\x001aâ§ÇíÃËóLð ).ÚÈ{¤§É÷`Ô$­àõæ5OWÇ7\x001fª­Ó\x0019¹wcä{ã°CÐ%ÞÁ¿3zÇ\\x0019E\x0012\x001fÄa÷\x0011òkª¼vÕyïÚã\x0002\x0000¼w\\x0008;Þû\x0019s\x000e3ï\x001d&
è¾\x000f:6bfäQÑ\x0018µÁd8!fÏ[vï¡\x0004\x001f:Á\x000b?ò½só7\x00089Õ¹áÞgp\x000b,@?æÎÔ¿#:ZÞ äÞù#iéîùê]­ÞÐ\x0006>ª\x0002üÞÜ÷bðF\x0013
w!*Ìee\x000b\x0005ÿ½Ä·_\x0000ò}>£¥È£0\x0014C%ù±®=\x0012Ó4î\x000e_ñÞU©jT§ª[%lÊ6´; Ñè­.Ð[ÝÞá\x0016f¢à\x001bd-l¸\x0004Þê©\x0010p¾ÔØP"ïS5Ñ!WF\x0012\x001ao)SÓIÄÅ	nü4ÝÄk\x000f¥ÈN·}pý\x0005/[wÕÉ%\x001e³ï]Ë\x0002ºÐ@-{\x00013o\x001bwu\ø²äÖµ*¡«Ný¼´\x0013Oû\x001f\x0015åj@iN\x0006­óïÜÀm\x0017p.ÂÌ¯4ÈÄ&){3NNu-AnKäÚ\x0011JÈ\x000e°³Ü%\x000bÚÑ
ôÆ3çB÷%tß	\x001d'x\x0013eê¨z\x001f0ì^\x000b¹)åÜtÊ9·iÚ'e\x0005nqÈºj7AÊ\x0019ügs¡ë\x0012ºî®#{1*\x0004¢a5(=\x0004ÝNåÏ\x001eb\x0001=Ä¾Gjä¦\x0015 Yç\x000còsdèªZ1[\x000eÝ\x001eëóÀ&W¬Cäb·\x0001\x0003J¾£±yÙÈc,¼\x0000üÙ\å
I§ãT5­·¼\\x0001ÿvÅ@o\iå`oo.¿ECzòÀ;\x0012ìÈðÆ\x000bïkÅâ&j¬ø´-Ä\x001elÓ¶ç\x0013Ha¨·Ùz¡ø\x0013Xe9½$g0ªÎUñQº-|Ô¯nûò\x001c´_2F"µ\x0005íË¢\x0004n\KÛHûé¹¸xpû$Ç\x0012u*(\x001cÏ+_µ¦q\x000eì[ÓBíË>Z©>ÙÇ¬)\x0000ùè\x0003É~`ï@N¶Å/HÁýï¿^Ûûx\x0001!µ\x0017[ë\x0004ïb\x0017Y\x0019±¹RÚ~*v\x0000`\x0011¤d`zw÷ôôòËËL\x001e(¬\x001bøá\  5Àó\x0008"Î°UïN¯¯oÞÞ\x001cb\x0000aäj\u!§®,À\x0017'ìRd5
ß\x0006[aëî\x000bgâ±HÖpáÃ}O\x0016¹\x0017\x00017cà¦ó¾Q<òKràáÊ\x0019,QK¿·!·cäv­+Ç\x001c°â+ç\x0016¾8$m\x0001r7Fîzï©öhÖò[¾ói:\x001føn<<©\x0015ß<;ÇÔ²*Wj\x0002h@&J\x0012p\x001fÔ±Ð±G\x00198\x0010¨\x0008f4£\x0016Ê3%àJGÔ6é¢÷"¥¥ Í@â*Áy6!Q\x0010Ó am.¹EHp±Í\x0018{èR\x0012©JhV\x000bä^&\x000eÒ¬Xò0\x000fÞù.ÚH¸÷¢Åï\x001b­\x0001å¢²C4=0Íp¸¦K*Àa7
ª6úäííãì\x0002j" 
ää:J¯kí\x0015\x0015P¥ìÌ»Þüp|ru°za6Î!ìrãÜbÜÃbZìõ!\x000fí¬aÜ3ÃÙ¸]»ë¾-Þ[ì"Ï¾\x0015àÂÞ\x00125\x001f÷niaÂ-e\x0007nle#g\kfiÀØìûiõ=\x0017÷hz\x0019q\x001bÛÛq¿¯Å!âÒCÆÈ¬(ÞN\x0015°ú³_7ü\x0007¡6\x0019å\x0017!F)Ò¸\x0010í$5güp÷øeæ*ï\x0008$7eàÂkâvDÏ\x0018ý}¬\x001bá&´ÔñÃéÕ»êJÁÔ¡ø¥Úß ºô\x0000\x000e?ÞZåÁ\x001aqÖe·ÎÆL²ï\x001f`â\x001bHc3ýõÐËÏ\x0010\ö[@\x001bÚh´\x000fÃî°¸ô\x001bL\x001dÁGðÝG8f_Úa¯>\x00156p\x0011|>nþ]z\x0006[a;åò3(æ\x0006\x001d/«Ï\x0018I\x0002d\x0002³rÁ\x0019Ôh\x0015|zÎûËà\x001bC.Ng¶",\x0011mszÖúê¹ïY	[\x001e ÿ#àSú\x0008¸.\x0003ÍðÃdçÆÒOà\q\x0002·¿<sù	\x001cokO ¸òa\\x0018>Ádiué\x0019B¡UUèÖªHôKfp\x0006É½\x0010&\x0018ùO;C,%)vKÒ\x0003R[¯¨[Ò`\x0013e>\x0003¦]×=Þ%öð\x000cø³÷\x000c2òfL<C&i3Vsw96O¬}\x0006W¡ÿ= b~\x000fÖF®Ö[A©UgÃä^¥gÅ{Ð²û=(ÉÀ¯óD8¥\x0011+²¶ÆùÛ|ÒSÒý\x0012\x0012 yú\x000eF\x000e²¤(\x0019å¬\x000b-ç\x000bÏ`Bq\x0006\x0013Ö8Cö2 :£m(ÌX\x0008ñd\x0006¡ù\x0000¶PJe\x000fEã\x0001\x000c\x000fIY#¸ÄÆ\x000b´ìtsßÒ#¸ò\x0008n#x\x001e6²Z\x001dIþ\x0008ÄO\x000bg,9,=C(õjè×«4$h§É`\x00184ËÑ­ÖKàÇÂËÓ±ÛËÃO è\x001d`ÑLâ/ §¸É\x001eÁÈâ\x000b\x0018Ùÿ\x0005parþ\x0006N\x0011#±Öa3qtoêÜ¨XN~Þ¶ÛI²TÐ\x0016¢Pj2cg'';\x0017g\x0006¥öVoÃ_`ýmÇùnûË×Ï÷Û¹ý\x0016`\x00022S3Vq'\x0010Uà\x001cHí$\x0015ü»ã·\x0017çgÇ²Îjoß6âÖ=¸E q\x0006\x0015ý0ax£\x0013ÎL2\x001d/ÀmÆ¸M\x0007n$ïÌÆ\x0017.;Òä-¯"ÔrM°í\x0018¶ýn`û1lÿ½ÀÞéF-åw»P&²Gü±¸\x000béßxËB¼å÷#ß±À\x001d{pã0µ7®\x0012¢vyGM\x0008\x0000|rÇ|ÜºÀ­{p#_wÅÖJ¶:\x0010XRìTg²i\x0001¾\x001bJVGt\x0001÷Dåå	îkÒ2ð×èp\x0017Ðô(Bá\x001dåU4¸Ë:Ãva«5ï»P¦G\x0011
ð	\x0003	
x¸Ã}S­\x0013ÜªZÝ\x0004¼p«L_%¼>tá¥é'\x001e´tõ%¼MÀK¿ªÇ±ÂáÿL2¥\x0002N*æpÔ	Ê
Øèj±ß\x0002^éA Ôá1=GCðIÇU¼\x0018Î8#YND­ub9jW v=ÎwÜI·\-´4dfc¬õ\x00055ÉHa.M¹L¤ãÙì\x0004\M©/OíÁ6ÚUÕ`(.àöu©`-11\x0019K\x0004p6ÚnÍ&Ü½4=ö\x0012;\x000c%Ü\x0002÷dÜÚ3ðZ?v\x000bp[h\x0013Û£MPçú\x0019\x0000ßÕbE,)kâ.$ÜöJ¸£\x000bÇ»§pÞSáÌF¿¦Á´Û^	×ô4½á\x0011'ëø¾«ôÙM¸\x000b	·]¬Ølp+Ç\x0012nxi½jzõÏL\x0005î
÷Äõº'Í\x000e&àö|`¬å¶]á¸®¬\x000fÒÐù|Ûf\x0018³FòmëéÅóûÂõ]~,Â£G(Î\x0011*OÓüNT{ö\x0017â»ò"äü¬òÙèçÜ¦ ¯*Ä¸¢©÷¤ø.?Öx\x001aÈN\x0012©¡Ékv\x0007M­\x001b«	xay|å\x0011âô x´L¸!5»(ªÖÇÔ;\x0014>aèñ	qû·#\x0010IC(\x000b®¥Søé=b\x000b\x0017'ôX\x001e\x0011"ëÂ\x0000wïiêJ)öQD­íª	xazBé1\x0011Þ+d}È-oDobÁ\x0001XÓ
Wãi+
ño:.^P÷5èK×³\x0015ì«é}®Óøo\x0001k1lu\x0002ÃVçw×\x000fý\x0019ë>o¶iØÓÃ×yØ	¤^¤>\x001bP+È\x0011ñª6ep~ºy}	ð?`ÕçM^$v}yñmË?`Wcìª\x0017»\x00134\x0001$±ö¬C\x0006Oì, \x0017×Å®ÇØu'v£=ä%ìÂåÙ\x000eÃ\x0011|ïµÒ\x001bv3ÆnzïÝ³IØWÄX¥(ú4AÔ¡\x001aøI·cü¶÷îÁ¿Í#ÒZfà7Îóe¼¯Q?´]¾\x001bwÝà%\x0011-¡\x0002Á14W\x001eùòu¨\x0004Fmàý\x0018¼ï\x0005o¹BÂusë\x0014R\x0011\x0011xW3QÍ\x0013ÆøC'~+\x0005ù\x0006\x00129\x001dÇóâ\x000fÀ_Ë÷·]~\x001c½à±i0cÇí7ÙÊ\x0006+\x0018{¨í\x0018mÂ>pûd3%:ÁÃ¿èZ¤\x0017óÐ`pYrb-®nC_\x001aÙ^+\x000b^ãÍwï\x0015S\x0002èÇÂDYË¢·Ê½,,­ì5µ\x001eW|\x0000cP\x0001¡Ê\x0007cKZ'êZ¦´íú\x000b[+{-î\x0008Yá\x0007Áf\x0016\x0006F\x001fj±Hóõ\x0017\x0006WöZ\?ðæHo7\x001f@jÁò³®ð\x0017ÖVö[Ë2³«ãcÅ\x0013#ûiÁÔXôÚÐ\x0017æVöÚ[+3ÈÞâºìd"\x0002¡·µöº6ô½½\x0006×»H½ÊÒa6Þm¤ì\x0001\x0018¬Zg]\x001búÂÚÊ^së¦ò\x000cJS`h¥âè\x0004dhíw[X\Ùkr\x0013jÒûð
ò\x0004¹Lôµ)¢Ö\x0003¨Âìª^³\x001bF\x0007§^ó\x0017P¨é@ñÔf\x000eäG\x0015fWõÝ(uC\x0003£åh\x0011ûz\x001dWµIô6ðepÛkr±ÜÎ&\x0017'p2z
a:ÜZCc\x001búÂäª^\x0014Á\x0014û i-§Õ`	}¿
}aoU§½õHk\x0018\x0006o'¤\x0018Ë\x001aáXêemp®
|aoU¯½KñÉÙÌá­å-C&Ú¨S\x001bøÂÜª^s\x001b5o¨ð|\Î-h¡9¼õë¢/Ì­ê5·\x0011[¿
eF¸\x000bÂjÜ\x0011O\x0011½ffA\x0015æVu[\9KË3ÀQ³´ÔÕê!³ VÅ^XZÕii½\x0000¹QìèD\x001a³F9vtl­k¦	½.Ì¬î4³\x001eù;,?Y\x0003ì	½c3\x000bÑíJ\x0017fV÷YÌ§å\x0001\x001ap=×êá\x001f#¿Ù¥.ò£\x000bS«{M­F>{G×¯hF\x0017QÙO¨U|ñ¹ä^c«
ï\x0006{å\x0010ÖzÃ]\x0008Ä_[Ý\x001bÞj*ÉÙY\x0008ÄAfÒÔ\x000fÅçqá\x00078,þ½Õ½öVE\x001dË)JÒáÆro§\x0015ëz\x000bº0¸º×àª\x0010© /\x0003X¯H\x0013|2;VØZ}¹
}apu¯ÁÕØ%\x001f\x001bø\x0002Ý½¦¤&Dº5û6ôÁÕ½ñ­ÆÅïYï`*u\x001fò¢0xµrM_G\x0017\x0016W÷Æ¶àËsR-\x001aÉ=ûN©\x0001}Ú 	½),®é
l²¬ò£¦õxÆ\x0005îN5ºÆ6ì½5½öÖ"Ã\x001a¥3£'ìA[~±¾6»Ý\x0006¾°µ¦×ÖZðês\\x0008O;WC\x0008¬,«|mà\x000bCkz
­ó(eÊ-dô\x0017[\x0011¦Ó¦,­)+·½Öâ\x0016×|\x0000ì&Ê\x000c_-Í#OÂ/L­é5µ62£\x000cÖq§ÅÐ(\x0002ÖeUÉ/,­éµ´\x000eÉ\x0005éî½¥\x0005\x0006'ÿÙÒÖZZÛÐ\x0017ÖôZZ»Òwè5ÕP$w@ã3XYv
ckºÉ¸Ø\x000e ¸ö\x000c"Ï-¢¶|¹íö\x000bckz­\x000bi:!{È\x0010Þ*ª¡È!¼jZÄ\x0016ÆÖv\x0017oMâMè}À&µÞè¡|µ´aä0úÂÜÚîâ-8ÙÚz\Áý\x0010"YZ8\x000c¾0·¶ÛÜZK¤A\x0010\x001aj&2\x000fZq\x000e\×fúÛÐ\x0017öÖöÚ[\x0008\x0001iÎ%ÕOb\x0016û«¸p»ªà\x0014ÆÖö\x001a[ãÍ\x0011×ÌÙ»÷Z1vSÛ¤Ô½lêîÐÄRJ\x0001iË(§\x0013\x000cË«±k·¡/L­í5µ:#O
'h^@0L£ÜUÑ\x0017¦Öv\x0007µÚ\x0013¿¬\x000c¸·¤|«¥²´¶°´¶;¬5L\x0018'qÈË\x0010~v2Íº\x001a§0´¶?ªu,9¸ïRQì¤ùÚZ\x0013zW\x0018Z×\x001dÕJud	½\x0017ìb:7är^ýä¸ÂÔºîL2À¤\x0008(|\x0017i,\x001d¼5½¦ì¸ÂÖº^[k\x001fzÔ\x000c4¾â<x«Ö<]ak]·­³
¨3i\x000f³È~ÕV\x0011WØZ×mk£?òBó
`ºÜà)¬z÷µu½Ö6\x0018Å.^Ç#jd\x000fAq\x0001bí\x0004¾+{{ím°Ì+½äydÜ\\x0014¸~µ´Áîðí\x0017öÖuw%G^ójd	¯1¿°öõ\x0017\x0006×u·%\x001bfsØlG³A\x000e·_Ûª×¿0º®;º\x0015ñHsáÙs[xCÑß¬YyöÍõÝÁ-¦1Yö\x001d3\x001f¤\x001fj\x0016YêkNÝ¾/®ïoáñÒ\x0014
¦ô#\x0007ç<F³jáÜ\x0017&×w÷%+\x000e±là1Z+ô0F\x0013ú\x000bw_\x0018]ßktÿpÅï\x000b³ë»Gtàê¡¤¤\x000c]D\x0001¾ê\x0001
Ëë»-/\x0005ç\x0003X\x0015\x00192Í\x0013\x001d\x0010¯¯ÖôéõÝýÉ_/(|ªÂY\x0011\x001b|çUk¾\x001c\x0007êî\x0002È«CN`ÙßqÓN4¦ùò\x000bÃë{
ï\x001f¿0¼¾×ðzÜ$àkækrNÛp¥öÂ\x0013
Ã\x001bº
¯°D\x001a\x000bW\x0011zð\x001a\x0014'fÅRôS·\x001f
Ã\x001bºë¸q×¶#\x0005g©Â.âÂäÆº\x0007(¬oèµ¾\x000e\x0019³ø\x001b/c+\x0019­¬|ÂÒq¾ÃòSØÞÐ\x001dð:Þs\x0003^s¤VS\x0013Øï	qídI(loè®å\x0006ËÃ\x0005V\x000f;J\x0003SÍ@\x0000#×LrÂðîR®³\ÃÁDmèöÍàv.­hM^axC¯áµÚ\x0011%ÄÔTK7ç°æå\x0017v7ôÚ]pp¸û\x0005+\x001a3ÞqAÎ×\x0018Ï[ÀËr´@öÎ\x0016àÞ8îÀ\x001cË¯
³\@¬¾TêÚþ¼}z~¬É.Û\x0000tw\x001fÀ\x001fí4À\x0018/oÕ*·\x0011G#R3\x000c®y"Ê?14ÚÒÁvïgØ±ÍþÏm§û\x000f"\x000f\x0008|!¢2ë¡Ô5nÍg\x000c\x0007Øî\x001d`ÛyËÜ)Rc\x0012.GÀÒ³\x0011°~Õ.<¡Ë\x0003ènühÁ\x000cD5K3Z3Þ¯Zá\x0015¦Äoºñ#?*¥Þ\x00145TY¥éÐ*\x0001Y\x001b|[Â·½ð#ø<ò¡\x00155´Yä
àUá»\x0012¾ë¿ÞqQ\x0018
ø1\x0011	ø\x0010ë\x0012yêÇõjh\x0005uXä£\x0001?öÞV½ßÓ<ÝWË	À\x0006Xùê1SKä;«¶S\x0001üRów_½¤´¡Ò´9\x0008¤^
ì;«\x0019E(ï>tß½\x0008Üõ\x000e>>qÂáT.+M¹®ìòòC·Õp²\x0016Yâ@Èh¾ÿ*`#JyÿýF\x0017{³ü\x0018sÍI7¦Ê4®ºÄ¬\x0015þm	¿÷úýP­\x0003\x0005?Ø\ÉA{è³\x0007¦¼|)Vq\x0019(åé
§lÐCÖaÕ'\x001càvï\x0000½÷­Ë6±éH$\x000f:·j±TÊ½\x000f »?\x0019ÊuÆxü\x0016Ùçä³µm
­\x0007¸Ý;@ï\x0007Ð¼.]\x001a\x00156gjÔððc\x0017Ã¯ÝÎ\x001d¬ûâÏrOÓë¯s\x0016rðöyËvà2äè\x0017l­àMY¾6¸R¬hz}y\x0001ÿj¼EÈ\x0010cäø³\x001d¹\x0006\x0006\x0017c\x0012"W7N¸j¶¶\x0001¹\x0019-\x001bDnñß-\x001b\Üóv\x0010òÚ|çJP¢\x0007î|Öv2B^Ë6ìz¾{ÜGÕ|\x0000E:Úmx®\x0007á§¯2È.¼yYPõ¥æ0¸«ç»\x00015<ÙÍÓËãæüáå×yÙ\x001e¤^ÏYr+¤NT­¨9áöW\x0013þÕåÍÓ\x0001=<ÛÍõÍÕæüòæýä)t\x001c\x0002£Þchhãñ\x0018"\x0004Êk+Èi\x0008ímícXY|\x000c¹Â1 ÈÍ=n8ìD<l\x001agþ\x001a>ÆÚ°kÏ1\q\x000c·Æ14Õ,R\x000fÇ A.\x001fCE±ã\x0018Ñ|ÓÝÇ\x0000÷AÒ1¢õCðÞÒ1¼]ýkÈÑo8\x0006þì?S´yÐ
P±>³ü9¼ªd±:Î!\x000b©Âýç\x0000Ëù-­0\x0006]´\x0013´ÈW·-ô\x001c#Ç\x0008ýÇ0¶ÒbÛäQÎ°¾å'.jtÌ\x001d§\x0018\x0018\x0011ò)\x0012¡û\x0014JÑ\>|\x000cÇ\x0002Ç|&ð1jÓ=ç°å9V0\x0000\x0019\x0007¾Òç\x0006K\x0007ùqh~\x001c²6Hrà\x001c55\x001f¢\x0014)½HY«¨Øj¢á.3í#U|Àië\x001e"XÁCd3§I¢À\x0011wÙ\x0015qh\x0018}4µf¡\x000e2
Ç½çpÂ9Úe\x0005nÍ e\x0008L\x0011åC¬
9\x001c8Ç\x0001Ç6£4\x001bf\x0005³aÞ|*mýA;cïQól;¾+\x001f[CßÊH¤W8DKzàÙËá{ÔhÛÏ¡J»¡V±\x001b>`\x0005*Ë\x0015Ó_iMù{¨õCe
¯
ö++\x0011h\x0014Ââ:J+ov\x001aw};®vëÁò9ü\x001aç`ÖÞô=rözpÖ[=æP¥³®ÖðÖ­`ô=,ÃØás¬î¬«P¨+üÙ\x000cÅio\x0013\x001d¯DÑÞ±·\x001e|X]¬téåê5¼\,Vå¥§ ®\x000c\x001bhn[\x0003mµþçÐå+×k¼rlÜ÷>\x001fC;b>ÒÁS\x0007\x000f¶Ö\x0005Ó~\x000ecÅø\x001cø³ÿ\x001cÈ^FbV0#1³æs\x0018»º\x0015´¢8\x0007þ\á{p?ñ.PJcóúÞÅ\x001aÃDÏ9Ty\x0015¹`Vü=°PÙ\x000e0ÁOßC®ÿÌ­)Ónf¸\x0003wñx:dÆ\x000f#\x001c-"õ¡JÛ~\x000eW¾\x000f·Æû\x0008!\x001eñç°ÌS¥Øg\x000f¢F£Û~
_¾\x000e¿Æë³Ð&zæ!7Ê±²rµF¥cè"ôÀýÇ\x0000W7³Á1\x0002Q-*+\x0006\x0013hV·\x001d^ûò\x0018+xVQÁ\x001b'\x000b¨)\x00104\x0018 \x000e|}¡*\x0003Z¿F@\x001b>aÈôP\x0007:Xx~\x001c¾¶¨ã\x001ceRÚ¯*\x0012MyJXzãÎ°K\x0012j½Üíç\x0008¢pIðgÿ9 úÓä°\x000bsDËZy\x001c<«ÚZßcÈâsàÏþcÄ­ù\x00189%5\x0004!|Z­¯ã\x001c¾°äø³?O¢ã\x0011ëªaÀDÇ0ä¬j-ê\x001dÇ\x0008²ÂýÇ\x0010VÒBÜ\x0011Yª¬ceU#}ë8E,\x000c þì?\x0005©\x0001Ä\x0015ù\x001béØ\x001d±µN×sØò\x001cýn\x00136\x000e×*Í/Ã®¯pciÆã
fÜà42Lå§aì(æXýiÄòÇ5^¸T\x0016Ó;9vR<Ccæs(½¶Æ¢eÓïî(d·#Kn"«\' \¯\x001e\x0004ÊÑ¾ï|\x0010»²WÄY©\x001d\x0013OYÅÕ~Q#7m?Tå9ðwÿ\x0007ñ\x001c]äRæ\x0011\x001b\x0017i¼Ì©_[íJkËê\x0013þî>Õ¨\x0007
X#*?)§\x0011oïkÍm\x001b$Ù+\x000e\x0006\x0000:\x000f\x0011pñ\x0014e¦á¡Þõ8BÅJÉuËOJlúÝ}
\çé¬\x000e)	Oá­Î<Èj\x000fU{\x0011­ìFÊ4ü«î¨\x001c{h³SK\x0003êIFGY\x0012[]yÐÕH2Þý+r3	þMw\x0016¹\x0015©\x0012å¸#\x001bTîP1\x0008µvøZsÜ?
~5óÿS¡ówÇøíû;¶\x0008·§\x0019ÿ\x0002÷4ïú÷>n?ß>ÜÏÜ.[^s÷!\x000e[¢81äö:K³&º÷>\x001e\\x001dXM
V	2þ4b¶¸ÅAQË¤åüH4Vä­¥yÞÙ<\x0004\x0016¯õ¢&C§½5d#¬Ô÷â¼©Yìßþ¶RÍG	I2tl¿gË)s«'i1:*a»¤'ÛgÞ³\x001cÆ§3jLp5£ÄI«±?»3£hF]^:ú\x00025ö5´¢ÖÂ\x001a·âQ®\x000c~ð]ûÚØÁbÔJ\x00172?Q\x000f»®5¦^½fÒqj»®s-GmJõaÚõ\x0007R.KVz8±WÅ²Ò[íªwÁX\x0006mº@çº\x000f\x0006ïL1h7®Ä
¨K\x00011\x001d\x0002,§z@MK¿\x0004GÀº¶üh9jW¢v=b­ÑeLbíeÖ\x0003¾\x0003¾\x000c|q\x0019µ\x0017\x001dw\x001d)Û ½\x0012ØºD\x001cú4Iàkl_
 Ë«ö=Wmxz ZGbWM\x000eHLÿæ« 6¥ÏFH\x001bQ\x001boi®\x001cPKìõNô"¼\x0013\x000bP×ò!s¹2±tóà/ÐÍ;þí\x000eþU\x0008øÝÃË/h*Ô\x0010f\x000b\x0008L®~Èa¶¬Ît\x001e<½¸INê»Ë·ø7ÕkfÌjYµcö\x0016¿\x0010Ì}9Ò\x000ckT\x001c
õ\x0018²n\x000cà(P3R
\x001a¨}ÊÉ*+{\x0003f3Æl1+\x0000Jí\x0012ôsï¬ÖQ1æZ\x0006¿\x0001³\x001dc¶ím<tÍ%Cs!KêZ!«\x0001±\x001b#vÍµ\x0018]%ÈðÔ¼h\x00021\x0001Â-×FB\x001a0û1fß\x0019\x000c
e}%.\x001b ´ÃÕÑ´\x0006Ìa94c\x0006\x0019&Ú\x0018#-ï5ÖÖ\x0013\x000fxÑ¾âp4`cÌñ;f)
s"ÚEC;Ú©\x0008#÷~\x001aÏ=ÞR×tV\x0005hÕ\x000eZx÷.\x001b\x001c.ËÛÆÁP~ÓW´Ë!û\x0002²ï\x000cº:Á£\x0015ïZ

°¼\x0008µ.Â\x0006Ð¯á;
\x001f\x000c\x0019n\x001fúNKËéJ)j­]
 \x000bgÃ·{\x001bR{ê\x000268Aw i¥\x0006e'kQa\x0003èÂÝð\x001dþFô\{Gdºd£¢VÄ\¸\x001b¾Ãß°á(æ¢¨èÒ¥Ú\x0007ö7T­ä³\x001ct,¤#¶Kæ[ÆAgYC\x001a\x0011P':NSgo\x0014ÿ¢U@¤ø;9¤¤?T\x0018ü~S[´Óâ*íCw=ÐáíÑ tÀ¥\x000bÖÖÞÌvK+ùRgö2é xroÿãýÝ=\x0004R`\x0016pÀ\x0015i¹yô\x0006;ÁÌu\x000e\x0002òÉÇùñæãÙé\x0019\x0004Rà@lK§°ãSØ\x0015Ná"õ`¸8
qáöÅÈ©P£±8p\x001fBâCì\x0013Y´}ü\x0019 ®ÉÙkü\x000c\x000ef:a¶ô3\x00064Ó\x0019ô
\x001fB;®w:\x001fø\¢¢1\x001b'S3ÚºçP²x\x0014ø³û\x001c
¬ª³ù\x001c.1Lá9¦2\x0019£¶¦¯ã\x001c¦©½ükë94ç¼\x0015rºÓ9\x0014q¢;¥k\û9ÌÎqOãUr+¥E®¢\x0012¹ÖÆSW«+\x000eºæ¤µ\x001cCX_êZìæ\x0019	ÕËæõçyÁ\x001b¯)/¤Ñé±ô°¹æ e­ßl^_\x001e°g\x000cVÁêV°iE\x0019\x0015à¬åù\x0000\x0000ë\x001d£­­\x0010_VWÛ|·&÷¤\x0002ÚH¹ @ëXgVÁ\x0017¢U\x0005ZÕ6rt¤1¶Sdi½£4¬\x0008SÕ\x0005[éRÉXuU·b\x0005µA^\x0001øÿÊ\x0013G¥\x0007¨µñ£7;jÒ\x0002´ãõÒu¹*,7'ÃÍ@p}-X^
7\x0016pc\x001b\ä)\x000c\x0019­8®h1QOhHÇÏD;ê\x0011E^2Õz¹\x001aØ5@<â»
¤À°o\x0015´£fo@\x001b|ãÝ
\x0003e\x0006@¹a:Uç	5\x0016b\x0010ÅÀ \x0012Hhq¦Ì\x001c\x0008rñ\\x0001®\x001cM`¡²\x001dS-Â\x000b:6ß®ÂU7yÏÉHå\x00020ÅµÀr!ÞkiÄë\x0015õ9ª0ô3;é\x0018®«\x0011;,P·RXU+V$
O^ÁÓªM0`ìnÂG\Åð¢E\x001cã5\x0002ÒÜæf\x001bs:9;±"\x001bjÒl!^[Ê®m]ÃT]
'\x0006\x0003Ý¯¦·\x0006¢][¸\x0010¯/ñúV¼p©ÌJ(p4;áõ\x000cWÕhÈn(±F¬>)ÍùiEsüÖN¦\x000ff^lP%ØFkf¡*\x0011V\x000fJÁR<d£_ÇøÊXâÍx=¶\x0019d¼ø\x0005PÑb¸õÑp\x001b=1ë=2¯1\5È­d¸5öexÜsÉ\x001bý\7Ø`\x0015§N\x0003§$¯z*ÌñÐp\x0007P\x0001¶U\x0016<ïÿâ6q¸\jÜhx&Ø©ËUbÀx\x0003\x0011´Â	¢\x0001¼ßZµ¼\x0014o,ñ6:dØ]¬é~E þ@§xÿ\x001d\x0008Ã:þ£Ò%^ÝW\x000b"u\x0003#áÙTÚ1Þ©¾¯9²k
\x0007§ÈI-Óc¦«ÑGÇ[\x0005C{e­¯8,¼ÛÒ¨©F£\x0016RdG­\x0002\x0012p§¤Ètô«àÕªP¼ø³M\x0016@{ìb÷s.\x0008â$\x001c{»¶Æ°\x0010¯+î\x0017¶áEC\x0011È9×\x001c\x0004+\x001eC\x0000{Ü/»Úwë[ïÖ¥F£$»^¢\x0018'¬\Q³AÖ\x0006ZåÅÆÖÅÕå\x001e¥U\n`hVÛa»L\x0010L\x0019Uæ¨ÒJ¢;UÈ	Eõ'ÉsÖÎÌ4\x001dº[£Ü\x0002þl»[lÊÌãfI
èüz\x0015fJf
\x001a½Y¥q¹\x001c¥)\x0015XézµR0®0\x0012ø³\x0011¯§b;îa¥«8ª´ÞÔÆÚ\x0017â-£4Ó\x001a¥¡÷H\x0019\x0011\x001cíñ$\x000fá\x001aóÉ\x0012Ù-³x¦5gÆ0=a%¥\x0000Q\x0004=2·\x0006ÐP
mh\x0015ZÏM\x0000¸\x0016¢8å5+05E?\x0007l,%6¶J¬õìã?F\x001f¬	\x000bE`BbmÖ·­y}\x0017\x0003¿\x000eÍn¾\-h®\x000b\x0004afÉäÐåÚ¸&o\x0004Ü\x0002{}E²ßì#hËKõÜ
±+k;®µ¸NmÞ"¸R&aeWÜÉ©á³9XM¡
iT\x0005Î\x001ab\x0008R#5ä{\x0019ªI§8Õ,1\x0007ìû\x0012ÁZ×*±æ(\x0010è8¨\x0003æ\x000e°N¬à|¹XJAl¨&\x000e\x0019Þ
^\x0003«\x0003ð¾úÝZ/\x000bëåeG1K¬v6\x001fEãÌ©mÞY\x0002µÌ$øÖL\x0002`%ZGe´&¾\x001bx]d\x0014ª?\x001dêÕ^¹¬ñuEo¨SAip\x0012É$M U ÃÔdÓ2¯-çÝs5\x0012ÿ¦µ éãP¤7VT$Wñke´û¨1ÓØ
Û	M½FØÝBÝóà~Ù!\x001fVëwÓj¯\x000b\x001dþâUÑËò´9Ù>ß?=?Ìì\x0012\x00049´®KkÃD( \x001fxTO«É©·ëÍÉñ³ë\x000fz\x001c\x0019º, Ë>èfhÀÁ1vVm\x001bpôT}\x0019t]@×=ÐHÉ±Ü\x001cè3ç\x0017ø\x000e{\x0003Ýäõ\x0018ùAa\x0019\x0005\x0000{\x001cg6Üx´´T[+Ð)y¡	nä¢\x001bW)ù¸uqÝºëº=yåº¶ÖLNæfA\x0011Su×E¢MÜô!×ÜG¢V\x0007£(Ïnò">Ú,ÈC\x001frP,\x0019¸\x0010¹6Ç­Uª\x0017Î\x0017\x0015[¸í\x0014qÏ]ZzêNÄÔ\x0002¡¦'òçã.®Ûö]·álkzTE4Â2n[£5nÀ\x001d\x000bÜ±ï¾\x0003-\x0000ùvÄ%\x0000*ÅS£JQû:¸]a|\ñ	C6^«Èôä '<,µ\x0015_¦+´¡ë3>X¤!èH[\x001c_¢\x001b¯ê5Ü¸-`Û.ØÖ\x0013e\x001bH8ïÉ ¢\x0003ð%\x0017~\x0010ö(Á¥bÑ¦Ö àÞ¡\x0016É¦Þ\x000c^aÔUfè\x0006Øáñ}ÇG¦ËP^æí×zgékký\x0016Ã\x001e×JÑCQ]ú$àÊ\ög\x001dWq¬géÖrª³ä]\x0002Øa}ë~Ûõ69·\x0000>-S\x00069+£fV,Qãõ#wÎ\x001e{^½:þüù¿þï]þ~ö¨\x0005O\\x0011;±ÄÍ¤½4k«Ç¿úøüüô4~xD*ãÝ\x0011« ^äUiÁþ5\x0005©Àxå%ðoQ\x001b
]\x0008×\x0015p]+\\x0008ÚÙÖ\x0000ò<Gn¼c´ÚBî¥x\x000bq0â¥=ì[a\x0003C|ß&rós5·\x0014n(àF¸\x0012»2ICçh8³åîàÚßB¼±À\x001b[ñý¶9îU$¼B2Þê\x0006Àxw\x0017\x001b\x001dð
Ìð;\x001aø´X\x0007\x000cÉ®iu\x0000k)^Yà­÷+ì`úp|øÑ½\x0018ÂÅÚPðB¸ª«Z¯\x0017i^ÈÖY5è¡ëUêPþB°º\x0000«[Áy°t·CÃQV\x001a \x0007ä:pM\x0001×´Â$·2ÒtI\x0014Ém-¤Z
¶°j¶ÑªÙ\x0018Âà KIDòJé\x0001nQb!ÚÂ¨ÙF£f<\x000bi =\x0011Ìa<Ö×ÊSKá\x00166Í¶º8i9\x001b\x000fWZ\x000e÷Ddd!ÜÂ¦ÙFf\x0003<\x001c4\x0017"`)\x0014¿3Yþ^·°i¶Ñ¦%¾áÜ§\x0001ÙÊ\x001em\x0004\x0016+ÖÀë
æ\x001amZº_ÅµÃN9,\x0007E¼ÎõºÂ¤¹Ff\x0001&«])S[Âk,\x000bf·WÁ[Ø4×hÓ@9DNQHe(+ÚÅA¬u¿Ysf
To¤¾W<(Ì\x001a²²Ö\x0014¿\x0014oa×\£]³\x0011BzMÏ-Fê}5jíWµúÃR¸esÍ-#¢R\x00005ìi\x0013×\x0002áßz\x001d;ì
ËæZÃ5áÒ\x001aè|¹JîFs\x0007¿Ã%#ëà-Lk
× .áÉZµ{lZ°¿«âJñ+lk×Dà)E¥5êìëÁ\'zwisÍá\x0018&ØS8Aâ0$¤V\x0012\x0006_\x00186ß\x001a¬IM\x001e¯±h0b¨6ÕÆÁb-¬o
ÔÔÔ5Ó]ÌT\x0014ÿÆY\x0007maÓ|kº@\x001cDM=NÆx¾Üê6ì=¸\x0015¾SÂZØ3ß\x001a¦¡\x001eàT»§<c\x0018²+E¾°\x000f¾Õ>\x00188Ç.\x0001 öäÁ{\Ç9÷ð­\x0006âR`¾°\x000f¾Ù>àR\x0008DÔ\x0003m´Ýåoj;:â-ìÿ³Û\x0007_Ø\x0007ß\x001aúD3¤óÀÁÅþ$¼L\x0019¢ì:Æ7\x0014ö!´\x0006>Q*&³§\x001biºÖHÅýBJÕ\x001aøg©1­Ã§\x0002\x0019uG\x001a÷eóáîñùq\x001eE\x000fvfSF\x0004	d9Ï\x001fÅÐ©ij'	ìÍæÃéÕ«*ñ\x0016¡Õc´º\x0019­²D¤\x0012Y}vÊ\x0003o_µ^Ô¶Ï-CkÆhM3Ú`Hl\x0015þcf]5Q
­Ð±Ö\x0001¹\x000c­\x001d£µÍh­§² ²N°\x000e\x000b¼0ëªs'ËÐº1Z×\x0016wkjÚEö²|µN:\x0006[k~\\x0006ÖÁúf°4o6pd¤Æ1Ò4ØÔ4f¤\x0016¢^ê÷¼ \x000bW¹²ÈúZ¯É2´q66£5¸Iqù:oÔ1²òª\x000e®ï£­\x0006\x0002<"G\x0003ÀR4#Ö{¢mà^\x001e\x0013\x0003®»XÛÁ²\x0018±,\x0010ËfÄJñø\x001c«ÒCãJ­4-Æ[Ø3ÙnÐd UY
'étvÌÑl"tmr1âÂ¦Év£æáÏ4ÞC2!"ÏNU)\x0016#.ìl7lÆ3Ñ	Ð\x0013Â`í*N,\x000cl¶l\x000e¼0âA#G^C\x000c<
Zo¥\x000b.l·nÈ\x0001ìwiéQÐ;Ä3mñ$âÂÂÉf\x0013g1§K\x0013?Æ\x001c>\x000f»aE{8/2\x001fpaèd»¥Ã\x001aJ$³¬A\x001cl\x0007\x000b¹4À»
âÂØÉfk0\x0015\x000fU1Ñ28¿'Àlu[ÉBÄª°vªÙÚY« Ë¿æÉ]÷½	]ë£\¸°vªÙÚ!\x0015\x000eECÂðÂô(\x0002\x0003Vb%¡PeøÖ\x0015¿Yò\x001bVÑ	Åb¬æÆ\x0018\x000bs§Í\x0013zG\x0000±Üm¾rXÖH:\x0016#.Ìj6wÎ
Z\x0006Ø\x000e<m°\x0014L{\x0001öe-©(,j·xÎ
1Ú\x000fB¬äà\x0018Wéä".ìj·\x001fÔÃ\x0005<éÄ!ß¨¹£\x0004Ý""ß\x0005»Ç*ÎÛ²æ4p©E9í\x0003QNû =ó\x000f/_¶?Ï&-w;Æ`Aüd6FÇüÆÆ=ÜBÄÌ?Ü¼;~3\x0002¾\x0007x×{Mè\x0001\x000cf\x001d\x0001\x001bzË#Ts~Uªé\x001d²ÓwMF\x0008Øî\x0013«/\x0002,N|\x00114\x00158môJò
O
¿Î\x0001¼+h!`¿ÏØ½ì\x0015QÖ¥\x001b\x0016Äs¬¸«Zª)\x0012é9wüz\x0008xL¯×\x0000X`ø\x0001;ê \x0005À^
'w°N\x0002;÷\x0018\x0001'"ífÄ\x001a®8Ïcúîm\x0014Ü}&âôöÄiÄ»êØ¸\x001eÄ³\x0015Z	Cm@n\x0008B<k/\x0000!Î±Þ\x001eÜPpAg¹\x0018®ØR´@¢¬ÖÞ1JÏ¢Í?\x0008·Ð%\x000f"P{\x001føV¨Þ\x0012Z3ÐuÛ©ùíâ e(UF
¬âz¯ï\x001e\x001fÁàý÷üçñÛf¡Æù\x0016Z\x0001j|à}¼ÊH^{ïý´*¾>½º\x0002Ó·9~wróúÅÎGa|\x0018V8Bê1À#\x0004i¢¤#HZ¡èc­ Ôx\x0004)#àÏî3ß3\x0004&äf+Çò\x0001^¬°ì\x0000®\x0010#éV#­i\x001a\x0013\x0002B0éÎ@¤6ðTåä®eg\x0008¦8C0+A\x001cåo\x0010¥ ý5p\x0004Mk¦Â$iÄÂ#wÈ°¿k¤í\x0008Ê\x0013Q¼Ávã\Z3H\x0012¥¨Öú\x000c[\x0011D6=Æ+\x001aé\x001f·_î¶/©Êúúþ- ç{ãæ©\x001cûZi5mé0\x0010±\x0007!cÅÉúñøÝéñMª´¾>{{\x000c?
Û\x0016°í÷\x0002;\x0014°C\x000fìH¥¡´²¨ç\x0012\x0000v-Ú\x0002;\x0016°c;lÜ´×\x0012[\x001c.COQ\x000eQUV\x001cÛ\x0006ØZaãÈÙwqÛºxºçIFT>ÃöÈ\x000b!¶ N L­©~\x0001läâM³¤»Ö(\x001d_¥¹QÃÆ»û\x001e~zxù|÷8\x0013¼\x0005]h(\x0006òSÂ!ð*
¥¦»hß½¾|}ys~vz5ã\x0000¾<ï<÷FIc|«\x001dF\x001a°³aÕ\x0003Äò\x0000±÷\x0000j×¥æ\x0004W\x0011¼ãÅKJºÉ>ª%\x0007Ð£y8øÏÕ{\x0003q~\x0011\x0012J}z.¾zõÜù
À&En|\x000f\{ò1r/¹n\x000e+PéÆzoþ\x0017S
ðuÏ¾üº}zÊè¯î·_\x0001è<ìÉÔ¦Â$DÛÅ\x0008"Ö\x001cã³wï¯¯3ú«Óë\x000fÇ\x0017ð/9tý\x0019þ¨¥\x0018ç³D'|ãJ\x0015àË£¼Ô\x0016bBÖù±\x0016Z5¢\x001f=_øÅ×Û^jiÎOð¥gÝ_ëlC/]>ôÀ\x000f\x0019,Î\x0006æ2<èdê
R×RÐø}ßwã·r\x0004ü£èIù\x0003þÚÒº6üJ\x0014²?ûð;\x001eÒµ8³\x001d3|§\x0008½õlH#ú]sAB\x000e}\x0017zL8eÍ\x0003Ñ\x0013%|!¨bÇGÚZî©\x0015,ñ÷J	´\x001b\x0008ð+Ê°§
÷ßÕv\x0019-Æ/ô\x001eO\x0005öÌgßí.?ß¾<¢ÁÚ\=<Íõ<5¼YêIÔÉ~>NîP:MLw¸\x001fß\¡ÉÚ\]^Ï:B±8\x001fJIßËI¢(ÛÛà/¸½`6¯ÿz÷u&x\x000b!\x0000mÎ4\x0017*+Ã¹ASlwÈá?îÇÓ9eYv`66\x0013´$¢*m\x0004\x0011Uyï'Ú\x0014Æ°kÞ(Ü\x0012fÕY3'4r"§¬Ó\x000b¾êù'¯Z\x0017°u;lax#¬ñÃÊ4--§Ì|}Yx\x0003lSÀ6í°¥\x0017TY0Aq\x0007 Ë\x000cIï\x0015aÛ\x0002¶ý^nÛ\x0015°]Çm\x000b&¼3ArVÚ²\x001aq\x0013N`û\x0002¶ï¹mKýYé¶3O,Ü¶3ÃmO\x0006Nóa\x0002vèm\x001dñgB \x001d\x0006Ø\x001c3hOtG.\x001d\x000bØ±GH<e@\x0001
ê\x0018Ñ¸5£®\x000f\x001aP«Â<ª\x000eóø¶*,¤ê°Òù¡X#CöÍáÿ,ZF=M=1\x001fua#Uüc/»°ªÃF*ßcTD¯ª\x00014¿G½À²Wú«ÞnÁ,Ï¸uëúáóÝýç¹x\x0005m2^3É´ÖxU½\x001c\x0019¹¾<?=;?Pý"¼a74ãÕzÐÓÃ\x00066­q;6ëéµ\x0000Ç1àØ\x000c\x0018`eê\x00048÷5º³âS\x0013
3ñ¦\\x0000o9åòç¼áÑ\x000b"ú+\x001euÑÂ?]´NÀ¦\x0000lþü2¡\x000bÐ~Ðª\x0000¬Z\x0001cÍ0³\x0008´9,\x00030Å²"îE|+\x0010å(D9ÁéS\x000cQN¶/_î6o\x001f·_ïgúÎ\x000by\x001cÎvGºÛ*ßáÉñÍ»ÓÍÛ«ãÓ\x000fÓ0]\x0001Ó5Á4ö\x0008\x0019ê\x0010®T
¾OÅõYqd¤ð«\x0001©\x0004¤yò
yZ\x0003Hc\x0005<#µ¦ÖX_@ýiûóö	ûçèxU@M½ºX\x000eóþ¿þï#~¸\x0007Ø3\x001fÕÔwjq\x000e.ÏHkãÈ\x000fFO/\x000e{z\x0005è/Ï\x0000ÿ\x00017-£7z¾Ü¤ÞÞ\x000b$bKè]\x001cTD0\x0003ú)*üeè}q÷¾÷îB^«\x001e+OÙq31HB/§÷-B/\x000bô²\x0013}î\Oè­$²sm\x0005±Å\x0000ú0¹_h\x0001z©»ª[ðyÜÞ\x0008ð\x001d\x000b>\x0015\x000ct­ÒÝ^èU\x001fz-}\x000eîÞP±IÛ¡\ Co¹\x0011¾+á»Nø\x0007pùj}Ú:Zl¼öåëBð¥î|Iê8\~æ\x001eÒ ?
_þôf­%ðÇL±\x0000ßNø\x00002ïLOn
èÏÈ?5j°\x000c~°\x0005ü`{oß±ÖÔR°µ\'ÓËâ\x0016Wå»UÝï6x*ÏXx3x§hCDÐÕ\x0006Fø¶ß{÷Q³ÎÇù\x000fJh;.që*³N«¹-
|ÙäÏZä'\x0010:¿Å5ÊYü
«Îé%Ú³Î Å~G¤$Ï\x000eûÕÃí×Á\x0005RS\x0010]®W:ZÐed¯âdÏùÍæêòÝñ\x0005\x0017¬T\x0002,U\x0001XªfÈ6hKL¸»V\x001beè¦ÓPò\ÈU¯QÇ\x0012ulG
±fÖî\x000e\x0007b\x001eó\x001eø¿Cj&zB8cÔø³U<37WÈp*SBØÀw=µgn>fWbví×´4\x0002\x000c¿`\x0016{ïiª0
5½u}.êÑð\x0001¢\x000e¦\x001dµ6é\x0015þ\x001bâýYñ=\x000bS7mÀlKÌ¶\x0019³VÒFÚg\x0016iÐtänÅ0µ	j6è¨\x000bÐø³\x0015´<D
"\x001dùÆZ@¢'õô\Ì¾Äì;.Úqÿ)hiÃH!Ð¨:héZ\x0007ÆbÔ ?=ß=î+kü«?¿æ\x0003\x0005]Î.mûBcÃ­ËÎ"\x0001 ñ[382TõG©dñ¿(×n~xøú¼yýr{÷ø<s\x0006Ñ\x0007K\x000e\x0015¸µ·±\x001a;P®êéÉ\x001f./>l^ß^}¨\x0011ú\x0010ö]Ï\x0017b7¶\x0013;(|ÑÚ2é¦ÓÁñéEP%öªÌ\x0010|_\½ï½zcÏ\x001f¯öVò\x000c\x001f&ÀVÅî\x000bì¾\x0017{¤øY£ÆÉ\x001bÄ\x001c¶VgjÚÐKQ
½è½zçq\x000bä[³ËNN\x0000£¹5á«\x0012¾ê\x001fv·o\x001cô9k(uäÚ[¿\x0010¿\x0011\x0005~#:ñr\x0017ùú
n®öùú\x0003O>kW«p7â·ðKÛ)ýA\x0004L7&üÒQ\x0002Ã8l?
+ßÿ®S<á÷±\x0013¿´[\x001bei¬\x001fÙ£\x0018¬õú6â\x000f¥ü^ùÇ~\x001fº\x001bi\x0013
È\x000fÕ\x000c\µ0×`³,d_É^Ù7JÀnê\x001eÙÓ\x0008úºS©\x0012½êD&w-#7#ËãYq7fþÍ«Pb\x000f½R\x001f
ßà\x000e\x0007ORo\x0015¿Ú©ÌÝÂ»×åÝëÎ»ÐÒ¦ õ
õ :\x000c¼YêW\x001dmKü½îO[\x0006­I®¦	¬õd]+<ÈËTO
j]Ò#¤\x0013Ð\x000f[GM4ôÔ\x0008\x000eÞ¾Ð\x0012Çûw\x000e\x001b64¤ß£\x0003Üm_¾<ÌË8zi\x0001;-æB\x000eÁÌ\x0006æx¡´SiÓÍÉéñÍ»ËÚÚ\x0004YëX@ÆßÁ\x0001Ä\ûl\x0004\x0007×V¸ÉÕÑ\x0003ä6¢D¿Qk)õ\x0004ÛC4E°\x001aD|*93\x001föÞeË\x000eQ\x0013\x0008|²È4?Úr eªÛ=ÃÞ¹\x0002\x0019vé\x000b,mÔ°6Ú\x0007v¶*ð°°\x0016Ó,(3a[QÂ¶¢\x0003¶\x000cÄF/Æ{¬r5	þÓ
ÏÑîZÍ2f¥Û1kMÏ\x0011ô5ÅKxÓ\x0004ÙTóßô.\x0017Q{ÛZYjI¾V¦¶Ê[k7¹Æ}\¶\³do\x00077ì\x000f*\x0017ý[=íOÂÒ}*ÖµH\x000c#Ëu-?|¾{95î%¨¾@tlÈÊuãº¨3f¨~8?½©ÎgÀr×¥2ÍU\x0014<ïk­ãÔÔ\x0013+\x0004vëuDnYìª Ö½*\x0004úâçÍöå#åä#®Bÿ¼ýúÓ_g6û\x0018-±"â\x001aHâ±rÞY²1Ôèïwrñfs|ó?ò
×¢\x001f_ÀÿnúD£\x001dH®"V:RX\x0017Ö.Mjâ8OB©\x0001/¦_låD¹¼|P| °â\x0017âHÆÑw´\x0004Ó\x000b[)ïýBÒ\x0014Gf½3YÇ¼JrïóÊð'Ó~ü¢o$3qëÿ4$Ïw¿m\x001fÞ¼½ûú|ÿù¯\x000f_¾Ìsç-¼mî¾ÂasC
@Æð¸y5\x0005xrys~úñøêÍæíéÅ³ó\x001f/ß½;HÞ\x001aö¹PCâBí\x0001oÜnR> ç\x0002õÿp\x000f®9>màw\x0015W\x0004\x0005×.ð9.\x0014\x0012ærûLà7µh¤
ü(ñmÆ¾\x000f< ÎKpØ,vÒäÞ
fèÖW4n\x001bø]Õ\x0018ÁcÑ¸\x0007¼Äú\x000b>"b\x0017m£ä	ÿZÖ²	»´b\x001dö\x0007\x000bÇ
Ø{¨³Ì;#¨ýD\x001a£õBô*ìµÍàRð}Ï÷\x000f¨0g&\x000fÄþ<`îà#\x0010ãÁí4¹3{Fêéüxóþ\x0012Õäjê ¦µ\x0001ºÜ'^\x001dLÔÝyêûh[õm¨-MoÁ>\x001aY\x000cúUY(iÀ\x000eö\x0006û]4¤(f>,ïp{5ìº¸÷ß\x0011t/Ãnc\x0010´EÎàª@Ø\x0005\x0011 ¯ø\x001cBæØGÞBÐ{Ù\x0006ì9ù°\x0007<\x0005\x0019;õy'f\x0011ñÎÄ¾S4Ýî3\x0008/Æ®À\x0002Ç¡\x0007ìÃ0ãTcó"è¦nzÅ]u2>wgqç%Ð=kb/DæwléK¯Ý
|¶\x001ekRºìýð(^\x0011»+°ïsd/½wÐ<ÿ\x001a\x0007Iì´ÉÐmm²­	z( ï³ê/\¤42óR	»¦]\x001eþ=VÔî®x©®ï¥U%þl\x0003±<Ua
SÍ85Õµ\x0008xqé®óÒ%øï´#³ª\x001bl¥%Í\x001eIú+ã\x000bð¾\x0017<¸À¤]$¶=\x0019>YÚeÍ\x0005n¹øXØÔØéËHÜ3\x0015¤¸Ë±Ä¼ëmuõL\x0013öBAÆ>\x0005éwÌw\x000b/©¿ÌÈ@\x0002o¢]Ñû\x001b;ý_S9\x0019{ÀÛìCJ\x001e]ûÄx
Cæ5ì\x001aÅi6\.H+rAÓ÷\x000eÂ?g[Ê¼¥7#»Ý\x0019#\x0001´Íæ\x001ex¶«FNM(Î\x0002¯MZ0ZîjGllX6\x001f\x001e^\x001eï\x001eï>Ï¥\x0013Îó\x001eYUF¥©f\x000c!+e8ýtÉøzóáòæêÃéÕéùy\x000f#£\x001f­=CôE³D\x000bz\x0003CàqÑUX\x0005³\x0004UãÅ¨¯÷´füº¼}Ý{û\x0006®\1¿½£
\x0015Úi5Üþ¤]x\x0011¿= à·o:\x0016Ì[ì¤4)ç\x000coz\x0008ºFÇÛ|ò\x001bîo \x0015»å\x0013(\x0016rfØ1Môk@Ùâ\x001b(Ûû
¬\x0010\x001c¼7\x0014OàÕ@Bæ'
×²\x0013è\x0011)\x0008@\x0017=ÒM'P¼ÛÒ\x0004!©\x001a§\x00016SWhµî7\x0000È»j"aÛy\x0008
úÂZ8ù\x000cÌòåâÒðMUz\x000bÞæ§ñÂ\x0013t?ÓÂóÖ
\x0015¸y\x0008\x0018\x001cÀ1\x0001CÀ¶Ýo"?»Q\x000féÖ\x001aó­Í¨µ!&jc
*\x0016Ôbé\x0003Ò«Í\x0003]<#Ð» 	tÚ	Ò\x000cZ9j13~2tÕÜ¿â#Îõ]µÐÂ¤0v4/g^Ù\x0008\x000eç.\x001e\x0011Õ¼y(ahÊO\x0005\µÆ\x000b\x001ehË`Oò×áäÅ\x0015þÕ\x0014ìñðI¥ï\x0003¶-`Û?=låJ_\x0018}Ò\x0017~Ú\¿ü6»¬,¸\x000eÿE­BÎEê'\x0003-8Ùu½¹¾ù8VÝ{XGWXý3c
%ÖÐ5D¬fdiH±5b
Ê¨6Ô´Ü\¨#n:Ök\x0005/\x0015¶aõÑ	äáL×ê\x000cQr:pú$]kl\x0011c¬å\x0016;áÒÒ\x0008¿ë\x000cC¶>]à|
®Å\x0017\x000c0g:\x0016N¤\x0011Ôã\x0010á\x001fc\x0011$­*÷rº1özó\x001a\x001cw\x0018^Ö"4\x0002\x001eÝ\x0018xt}À¥¥íÔF©\x001e2(¢÷JÔTÙ·×[Ä\x0012x)[²ïÚ!²çàL)^Ü¥\x0003ö\x001aeôrr
b\x0011úP\=þìB\x000fó¦\x001a\x001cVbÊm/»We%èG»
\x0010}ÚUÐ^\x000et¨J{n\x0003ðT\x0006ðn:¢Y\x0000¾|®ªó½\x001aìwÉØá¹æúÆn7\x0002\x001f&[¬\x00167Ñ\x0016àÓï®GkRñ?i\x001be8#\x0014"øRNÍ\x0008Ï¯¼Iw?b}2¯Ô\x001eåÖÝýÓÓöåóL6'â\x0011
@À=GÞ\x0013tg«ìøcæ³ëëãó:£\x001cúë{µ\x0016\x0008 ËZË»{ðþ~½{|~¹i=1÷[­\x0003Ø¦¼åÚÉ§NC?£%õÝ\x00198ïO¯>Ü\x001dºö>\x0014èC/z\x001dèâAP2{±¨ò\x0001üdU´À^IßfàÑGÓ	|7)-Øy"Þ\x0007OÔºÎéÆë%÷.EqïRô^¼p}ÖHÆ×Á\x0001~Ró2\x0007º\x0010¿.ñë^±×´\x001d\x00139µ!\x0004ä^SW3rV­	ß×o;¯\x001fîzí´\x000f\x001aà}°¤ëÝ\x0014×ÓBô®}üÙ>\x0004Ú^\x0000JRÓ4
 \x0017ôn­µ|µáW¥ð«^áÇø¸\x0015<x	Ç\x0010\x001f§S¢^ßHò\x0000¿Q®Wøéå\x001aCu#\x000f\x0002EÝñàªM6\x0006,{¹£g~»åüD\x0013~ä\x0013MGÀ\x0006<6Z´ùÓ¹0é¦ÍWüÿv\x001fÿm\x001f~ç°§?+OEÇÌç4Ã/ÂÿÓ>þ:ñkê-ÑHdï³ñÔ(\x0000ÿo2ã¼\x000cþÏûðî\x001f\x0003/Ó\x000cJSnÃÇ\x0010\x0007Ý¯ù<ßÄ¿\x0015¶\Crýl8ÉûæáËöþë\x001d}1á¿·\x0018"¬<nk|p¼
QjÉ\x0014ËMø&ü7ïÏ.N©ò9ÿ)\x0016c>ÄÀs\x000eÿþ@\x000e#îh\x0003S'Wµ\zÇ	µ\x000eq\x000b\x001fáÓ\x0004ÿ\x0004þù\x0015Îûc\x0016ýþ1"µ0Ï\x0013 ìú%ýÛÚ³þ\x0007¥ã['Êû=ß\x001c]%ì©yù@	 C\x001e²Ò	2f¥\x001b!\x000b\x0016\x00072³BN`\x0017Ø@OPq\x0017"Ê\x0016¼m}\x0003\x000bx\x0006ä"C\x0018ËZ\x001e\x001b«æa®\x000bK·¬v\x0016ø\x000fÄÉ³÷·Ï¸&9ý}\x001e^ä*¦a[ø\x0017R\x001fÁ\x0010^ëjÍ0ïÏ?àä4tö¯\x0007®Øeú\x0012n;^E2\x001aã×\x001cµ\x0002^\x000eA¬«õòîá=\x0010i»]I¡Ü\x001c¹÷w\x000f/ódØÙÌ<\x000f\x0006üv»ç!läç\x000c³ÏN¯.o¦ ËÑ¦.,¥mÆì\x0005mû68¬o\x0008sàÎÝ4	²\x000efí\x000bÌÚ7c\x0006\x001c(	\x0006 \x0019³\x001cFõ&íã\ÌÊé1füùg
¸cGÌ· 4UY·8¿º{Yq\x000b\x0010ûä­\x000e:±=ç1w­#§&Wq\x001fäÙõéCNx\x0006½KÖ!è½TÝ"ÐÁ£*NÄ\x0007fÕÖ0EUlE\x001f@Wü¾8\x0016×\x001c{®g\x0016p$êÈZ\x001a¹v|ÍaÒÝ{ÍrÔ~.PÛµ£\x0006ëG¤*\x000eÃpxË1²äzLE-÷¨¨¢6a°`^2u¿ÕÒSZÈ\x0019±H«Q\x001e\x0014Q;Ñ\x001aâÉ<øª7Ôùl±\x0008Ê\x0001Í$MÆ$ê­Ø[¦x,hâ_¶?gw}ÿõáçL\x0002VÆ£qD£\x0000®\x0011Z?Ç_¯Þduw}vqùæ \x0001O\x0001ØnÙ&n©²X\x0014ôú¯ÿõçØÃË/sÛ
LP
b\x001e6¼V9\x0018ò¼25Æïa¥Íë\x001f³\x001báØåÍ[üßUjù »¹t\x0010k×9ð\x0014Ì\x001b
Y^Î\x001d4W]ê<Î1ñMFÜex\x0014U.ôj?1G>`@éÇ­B \x000ey¯]m±ë,¶<ËJEFâ\x00105\x001ae
É\x00171ùê\x0018xÏQBùYÂJ\x0005Û»óSAjÿ@ûß%÷JãlûÚGÑª8Vë\x001cÅG0eYÂà\x000bQË¨
»çÀ¥Ú\x0015¶à,·¸È\x001b[ww= \x0016ñ'6Òýe-R/¿Ì 5Ö'#1>DêVôJ\x0010
°\x00175RóÓÍ_±7êæí¡\x0001\x0007ãö¦Á£òIâòXS"×Ò£È\x0010(\x0017$qjÒ Áí}£%îº¢\x0010è^SÔ
é®y\x0007îõî,@êã\x0014
6dâbÒ!;µÞa@Z¶î0ÌâËÇæO\x000f!\x000fWæ\x0015u:\x0012DjäëÀ\¢#ø³\x0015hP¤\x000b´\x0003
Gd·Æ3ñ&';\x00084\x0014ß]æ\x000fÿO\x0017QU>&õç}MÒFUÜ*þnýþÞ\x0013ÙFD\x001bé\x0007¯ÛNÎóûßëB^5h}øGøïW\x0017\x000fÏwÿòf;\x0002)\x001d|\x001c¸d¨)òÞ=ðjIêË\x000f<>ÀGA0¥)`âÏÅ8­ñD<gñ«Óî #1¯X\x001f*O~³u´ehqbh»\x0014'®·
ÞFÆÀké ¨Íâ\x0019D¬uÎÀ³ßs7Àapù»éÌ×·/Ow÷31CÀ
\x001eJÂÊY\x0006\x000cøDèI¦òw©Lñúüøæúôê¬6e±Ù\x0000û^z9vÌHç\x0011#«àû\x000eT(
JÏ¼ßa¯û\x0019¾)áNøà-2\x001b\x0016<.Ð\x0015	Âºøu):ºWt°\x0017LÙ_iÞEç5
ö"³ÍñÒ9øMÒx»!MìÓvãY'@97!«ó¨óW\x0004ÁB\x001f1W}ÝZbr7
pry
ÿÛCi\x000cz´\x0015
A§­PÍ°­§\x0011Ô{J6\x0001\sj!ô\x0013ñë\x0018wå¡fÐ£@\x000fAS ×\x0004Úb\x00052×*Òü¼±\x0010Ì¡ª¤'\x0017\x001ek\x0017\x0000´K3h\x0011°fË\x001av\x0015EE-÷^\x001a]øbÌ¦Älz:ð¸R\x001cc\x0000ÍÍ½Ò×ýæ¾\x0005¼é\x001dêÁTBÜ¹öÏ\x000fO¨CÞ¼<n¿þ<S{ ÷H®ÂH,\x0014ð|(\x0019\x001e[e\x0005?¿¼FÝñææêøâÍY\x001c·W7ÂåEÝ(i½8p6Wé9©y«rÚ'\x001c\x000cüßd¥\x001dUu\x001bx¡ô>âÌÙaçSívÄß\x000bWTÐJ½~yüzö\x0018Íè.Mfø\x000e¬<Um\x0010Óì\x0017¯o®.ÎN¯ªYÈ\x000cX\x0001«vÀ8öñ"\x0005n«héº
fxl\x001e\=«Ûá"3<Ý¯`:\x0013\x000c%±à~§\x0016ÉÍ\x0005lÆM3`NÍzY!ùOîp\x0005Dñ
k·@Ø1`Û\x000e8Dª\x0018)\x0017%\x0013B\x0004É\x0003|\x0000}ÒÝ\x0007Ø\x0001»vÀp­DB\x0019&äòVñ0æ\x001b\x0007Ø\x0001ûvÀ.Ò\ÂêV®É\x0019[îó
ÛiZÞyÃ\x0018ph\x0007\x000caNã`\x000e³À
2¶ÎM
&ì\x0000O*â8Æ\x001c;¤ÂS1.]r =u­wb6æ<®¡äv°FÄ\x0010g\x001f¹\x000c8Hªd¨\x0008Zð½\x0014oiéÚM\x001d¸\x0010G¤'tÌ\x0003ìÆ\x000bª¬_ËrÈÂÐÉvK\x0007ajk\x0002ðÈìîWSÇ\x0001\x0008ÄZ\x0017\:Ùnë°xfÈ6{Oû%Ñb^óÓ\x001bEæ\x0001.Ll·u¸¸;'f\x0014¶Hkìa\x0011\x0016ÓÌeó\x0010\x0017¶N¶\x001b;ä¥;ãLWl(µ\x0001îÏÔ¾è¹\x000b[';\x001dÔ5i\x0010y^\x0006w¶¬c:daëd±\x0003ÿÒf¼ În×â þJ"QØ:Ùaì\x0002ÁØÖ£ú\x001d\UkÉ]
·0s²ÝÎáB\x0016M¶Y\x001bêB7¸2%Â®#\x0011ª°sªÝÎ\x0008Qs\x0002µ[â:\x000e"ð\x0015é¶ùy\x000bC§:\x000câÜ-\x0008\x0005OR#£E\x0018b\x001dS§
Ë¡Ú-AÕ@WìpÆ(\x0001æ@xb\x001dµ¦
Ë¡:,\x0007®×¦w\x0017yô\x0015¹°ÉpL·0Î\x0004\\x0018\x000eÕ\x0011%ùH³+ÊØí.Ùg÷ÒNçóç\x0001.ô°j×Ã\x0016®d÷Ç\x00183$5\x001d5²à^u.dBwDÎZ±L8ý\x001d$ÅÄL\x0008B1?ê¨Fä¾ÅP8ì[\x0004©8ûòëöé)\x001a¼~øüùnsþðõ-\x001eH\x000bmãn.+·xxÁÛ¼¬e\x0008ÏÞ½?¾¾N#\x0007¯/ÏÏO7ç\x0017ooFÅ*þò\x0004fô\x000eÑ\x0013ÀØw\x0002c(BÕpÍ<\x0017:¸(ýk\x001dÀ{ü\x0004z¤ùü«´öÍÿÇª¼xeN[M\x0014<å!&æV/©téD¬Íp¿Ù¤ÿI¶\x0004h\x0002ÄÄU¤mÎHÃÌµ#Þp§ªvz\x0016B)Fü\x001b0ý^\x0008\x0011\x0013)´Á\x0010{MîLò:>Lm\x001e@\x0013}\x0001\x0010/ýÈH?F;¤B@å>²t¼CÊÖ¸JçAtcÝ\x0005\x0010Óíe\x0010q:CÑb.¸Î¼æ
xbæqJÔ¶Ì\x0018¬( âï\x0010¶G$Ø:\x0011hkXè^cË\x0005Péq&\x001d_
vj/\x0002è±VNKdMÐ´Ù\x0000¼0Z \x0004ÞMm.w\x001eD§;L¿\x0017B´QñdÃ¹;*\x0011\x0002eI¬eðæ!\x000c¡T7ø{!B#\x000c2\x0011;Ú^fóEô¬o¤¬µHÎ¨E	1ý^\x0008Q)^\x0014\x0005:;ð\x0012;øú|¶Ë\x0007QéB%¦ß\x000b!âÕY\x0001¹¤ì=2Z!T±\x000f¢\x0017(¦ßË "¿%/»vHIK\x000c57ê9[+üÎèC	\x0011ûþAtÁð&=g5Î¼"D)ùACÌÝó Tû~/©«ü\x001dv*PüÁ#T®:;\x000f 1Å\x001d¦ß\x000b\x0001T­%§R0­>ø\x0012Ôæ\x0016t­ot\x001eD\x0008Á
ø{\x0019D\x001b¼§>!\x001d0Ë!TLK\x0014µfù¹\x0010ã\x001eÄ¸\x0018"\x0016¦L0¼7Ó\x0008$Ê·hkíL¡Dü½\x0014¢a2aði5¢üXb"ËmèK\x0003~/¨4;9àD\x001ffã]ð×}\x0010½-!ú¥¶ÅzÚ5\x001aý\x0010\x000f[#¶®uÀ\x000b®PÚé÷RxÊducàMÐ\x0005êhOÔ\x0018¯ç\x0002Ô{\x0000K¡ÄçÌ^FÑ\x0017¦\x000bT]¡\x0000v\x0015øð÷B|.ðT?<
I;\x0017àÁpë¨\x0015s¦\x0010ªÅ\x0018M`b5½HØ¿¿»¼ûüòÓ_gö²hÌËÒð¶WÄ3|\x0015ôµ¥.E¾?=»:=¿¿>f¤¯¼èNlÏJ8ê\x0007F}Á¸]í\x001dµàÆ=\x0013#ÜiíD;pß}Â3Ýg;öËZkY\x0013v_Kú÷îÀ\x001e84\x0010­qÜYÃØõtúv>v%\x000bìJöÉ:(6Úì¦ç­t^DÇ´TøK°F\x0011{1r¼üÞAP2\x001fÁ'K{\\x001c5«*?]Z[ÜÇ\x0002¹=È%Ê=¸Ä¬¶<=*§æc×®x©Úu½T\F\x001bÆ°µ2SÊ\x0018#4ï-ÒÃ&\x000b°\x001b]H»Ñ}/Uz&ñÇâ[^\x001fbltïÆM-\x0016@7ÈàÏ\x000eè\x0006G(y\x0005£ TøKÞÒ\x000cðÊÝâ¡âÏkWê(fI\x001cÍ¤Ü±\x000f>c×Ó%Ä\x0005Ø}!îioÇSÅ~@ZÛ6*+\x0019kµ±F»ÕÝ¹âÞñgÏ½\x000b&¬\x0002<d&oa\x001fm\x0005¹¢\x001f4GcèQv]»¼ÝÄÄá¡\x000e[®¦ú\x0003]XöÁ_¤°«ÜkþáñáþióÃÝ\x000bÒÍÍn9\x0007ÈÔTø<ÈôTP²±j®nrÃù«Ë³ëÍ\x000f§7È7÷áºz­È,µCÓÕ±H®FDm/\x0013<Â_\x001e>ßÏD\x000f¯5\x001b§T>'\x0005ï%\x0019V,×Â1æh»Ù þ¿\MC÷\x0005tß\x0003]\x0007G»\x000c!â´ï\x0004Þ-µA\x0010R2Ç\x0002yìºt/(ý\x000b®â©wÜ\x0002 jÓþË KG\x0015\x0006yAJ`øw>x¾zºûr÷õ\x0019ëÛûÇß¶ç»æÑc°z8»±31¤¨6¾_~8»¾>}wzñ\x0001_ìÛ³«ËÇçÓèÝ\x0018½ëC¼û³Ú\x0012íT\x001eÄáÚ©ôµ"U+z?FïûÐ;-y\x0007þÝp£:¦j\x0005î
 |/¨\x0015}\x001c£èC¤
öZ\x000c\x0013¬V\x0004òÇ5§¦\x0011ýÐLÐc- \x0007¾ÇmtYSÆè@H¢~Ìðm-/Ô
_\x0017ðu'|+xõODÚ,;Ò\x0010!ªÁÖ\x0016\x001bá\x0017/{Eß\x0019Z\x0006¯âú·ÅY)_ÒnE\x001f
ô¡\x0013½\x0011`9xµBì[©Ö¯
ÑW¢o¢\x0018¶ï /\x00070UÎFø¦o:o\x001fl,ÕETXÕLJß{z¹ÒÔÒM­ð\x000b¥:m\x0016Ä\x0005ì- âÉÝ3\x00163\x0008¬xÖUº\x001dÝ); ÛGt÷RsÏntL-|uÿ_#úÂÙÑÞ\x000eÒòÜI\x0018ÃÐ4\x001f\x0003;;¦æc.D\x000bº\x0000³\x0008#>\x000b\x001c-ABó»ì^^Üýò8{có°	\x0010¥În$çWÁÕO³_yqúöª\x001eIÝ
¦JGË\x000b¥Ë\x000b_\x0001íëÏÛ_ÓEß=¼<þ2Ó%VÞ1m2GJ=CFÚúÈ×çÇïÓ-^Þ\½­;Ä·\x0010¬&Ü;þbÍNØiúðåönsqÿÓìåÌ^xÉ\x001b¨t¤Á½T$ÚÑV74\¾;9Ý\½N;'Ð\x001a] Å-hÁ¹bï\x000bM\x00101ñxÎ[#\x001bw--3\x0013­Æ;RìÐ3?_o7?<nÿ~\x000câÛÇ¹\x0013?\x0001\x0004y\x001a?GÉæqZÏàùñæ«ã=EÚðã«qIÜõÊÀ_¼J¿_]Cd÷¼yóðõëv\x001eÙ9.×D<qhO-=Áñìkªæ_CD\x0007JâòââøÃ!°¶¨ÃàòT¹Þ~Ý¼¿ûûLå\x0010"ºOÄq&¸Å\x000c\x0017ê°ÔªJëúøbóþô_\x000fê\x0004R\x00059\x0006?\x0017B\x000eÌÈ"«rAhã\x0017ªVÄRyi
ø{1LxTx\x001d<mÏ\x000bøÖ½\x0010µ-\x001bs@D÷1R±8-¨Âqý§ÍÉç-®¹\x0012Aé´H -®Á\x000f/@ßR{Euç\JRá°þõæäü\x0018wÉ×T\x0004|×P§~ÒVä\x0002óTsÃCR\x0005Á3(®Y\x0005x,æ<NÐ=Çf¥óß§\x00067§Oóô\x0002&stnj\x0011Ìû¡ÌÐç§«\x0017Ü^\x001fÒ\x000f>\x0014èC'zì\x0008ã ×(JCØ%¸u[ó¹ø\x00001\x0014Aû	Î#bÐ~r·}ùr·y÷_ÿïÌ­\x0002F;S*I\x0017G\x0014óþfÍB¦*è'§Ç7ïN7ïNÏ\x000fuÅ'³<&M\x0000³\\x0003}ÞnNR?`ºûy&hû\x0004²Û ©°Ô³Tj1´\x0002¦ï$uøÃß¾9Ý£Ì#Ü£Y<t~B7pO¨\x0011!XÞð½+æCÌ5Y\x0010?\x000c\;º>vËd!°Å ÈÓæãýÃç\x0005\x0008¥å!
\x0008n#1+s3\x000f¦¶m7Cq½ùxvy>^{þ,Aï\Í\x0004:¹=¨q\x0015^¶Ý`°·.Áö\x0014\x001e¬5ñ-ÆíJÜ®\x001b75Ù \x001a	´	&H2çÕTýbØ¾íû`cÚ&SdE\x0010rÚ1«xq¢\x000f±ëÛ|òÿ~käO2Ç
2Û0ÚãÇÍÛ/i'\x0015qóöñåëÝ¿¼Þþú/ïÀ¾ÿ bú+±\x00128ð´WÉ\x00131\x0019H\x0002íá5îR\x001c'W7\x0017\x00103AÈô\x000eüã³\x0001ìñÕæíÍ»
\x000bD\x0001\x0016ô§ê\x0000ëDÚJ`³ªNh\x0015\x0012ÑªUÑþÑ=W+\x0012iºZ­Iº[Ch¥\\x0015-¨yÓ6ûJ	mÈ=\x0000-uK#ÚUï\x0016=¯`;àúó.\x0016Ù"MF\x001ból) U»À$ÚoÌ\x0011/ìÓíý\x0013¾2ü\x001fí÷«N²k2m\x001eÞ¯àûÅÄÍ/-V \x0003F¤\x0019t@Ú¿\x000c:8\x0006½ëÉh\x0006ýëo·¿ÿ:ÒeÇ¿Ý}}Ùm\x000f{|Üþ´
ÙãÖ6-þ£Ë÷\x001cL.ï74Êøÿ\x000eòñÇÓÝú°««ã×ÇspgµÖ\x001b[]Æ-}&4¸QE\x0013î ê\x0012Ý;+¸>ÜÞ¤m£é¾-8â2÷"îÝf«ÕpgU×;Äw\x0001Üà*ç\x000c-Î\x0010ìèt]ÝµÂ\x0006Á³½°]é\x0004\x001b<"Å\x001b\x001f*ávýëpÝÏ2\x0011\x0011·¹\x0008â
qVÖ$b´ú}5Ü |/npò±\x0002¸q³¨¤N\x000c\x0019qáv=F«á\x0006C\x0010ºq+V'8Íaè¾µ#Wé±iE
ê)v¢\x0006/#5 jxiqÞç\x0015A\x001e÷Õëµqc#WÚÒwÝ©A7	©n­Y¶^Ýä`CöÚJ\x0007áµ$$\x0011\x0017\x0018¤ë¶yÊ\x0010$¬\x000f\x001c¹ì5X^û<mp³\x001c¯\x001b\x0004Oö\x001aKd­ä[ ý\x001eâvA\x0010n9b"Z
8è'Ùk--Q¹ ph):p¼*'¥ZÿaìÉ^{,v`\x0011óÃÔ9y"î·ië\x001el+pø²×`:-ÓrH\x0004."\x001b\x001eo\x001c¿M÷O¸q¸
Ùk11õ«²¨`pê1ëpÉ7®Ãê,f#e¯Ét8Æ¥ÉE\x0011GÙ!ôÑhöPìê\x001e
¶Ên£	á¤ËJ%(³MØ®È#\x000cnu\x0010ÂT¯ÍtpÉÖgÜÒæ\x0019wÄ\x001dØ\x0005\x001fu®\x0006\x001c®BuÍ X\x0019¦9ý¬Åà'\x001a·º\x0016ÇÊê1I<\x0004î¨*N¸bQQvu{ZJõ\x0007\x00151\x00017íf\x0014£\x001e\x001c,Z\x001b8ØLÕ\x001de2D%ä^sê#K_]§`G ê\x000e3qQ\x0019.E­\x000f¦bWWâ_TÝq¦ôGü4E\x0010Má\x001aK¸«{dâPÝV3\x000eOÀå\x0004\\x000e\x001e­\x0012ëkqx3ª;ÐèR\x0013p+(Ýæ\x0002[{±~>\x0002\x0013aª×jz¸eRâ\x0001\­\x0018I¥ðËÄbÍÊ¸H÷ZM\	âRB\x0002\@s¤²FA"¥|ájÔÖ¹\x001apøº;1k\x0012+zz>`e$I
Í;áÜÚ~¡L*%ÿÙiðEZ6<\x0015ì!!/\x0006Oe}/)/s\x0006¿S)ªT´N­=be¾ól×²Bñ>þã·ûß§ò?Þÿôüð¸ùñå \x0000\\0Á\x001e9Ý;\x0006\x0014¢&Ô&L\x000búÇ³×\x0000yóãÍÛË94~\x0013æ`©*e¬¦$gP³ÎD9é¦,\dðÛ Ôós»TÂLo°îg&\x0013\x000b1\x0017Ùû&Ì1- N] ÷\x0008å²YûÔ}\x000bf\\x0005­ó=[pÃ\x0015a6k³ÖLúÞ\x000b1\x0017iû6Ìì8¤\x001cN1YçÙ`¬²N§\x0017b.RöM«"_³VG"k
å"eíh]ûJl}Û5s-Û
E®_Úo\x0011ëÕ\x0005£ÈÔ7!öiä7Av4a@3[.¿éªÈ2Ì{Yú6ÉPè.å\x0017(X2X9[+V¶'{9ú\x0016Ì\x0011óI6gÙÐó®X\x0016^\x0019toºhcRûSz6\x000f\x001eáÔaÐnº½\x0010tãn\x0002
rlè¦!âÙ\x000ej\x0019¸?Ã¹uÝ^¸
´CÚ\x000cÚäÑX\x0000­$+h\x0017×\x0006]fZÛGH»²\x0013è\x0019\x0005QypÏúérÙ2Ð{éÊ¦(É¨ ÓG¶Ý:hVwqåG(ü§ç»G4ø?zî\x001a\x0007$ÝuÈ\x0002Qé
ÞÝö¾FGéÓOè*ýÔçß9*¦\x001e\¥\x0007ÿÎ®îúÛO·\x0008û¶ï²\x0003µÂÀe\x000b
Íá²\x0007
\x0012&+6Qo\x0011õö;»ì°c\x001flì"	¤E,5£êlÎÃê^D\x00192òÇÃ¶~F!ùùû\x0012\x0012\x0019(ÿ\x0011Æù¦+\x000f&ñy¥g©3I?\9bá»ôìÍ7ÛEÇ^\x001f\x0001ýÀC\x001a¢IÎ_¤Úu\x0000'
e¼ìo\x0002zùÅ¾<£\x0018G9>dNpPî\x0007\x0011ñJrbÒû\x0003®*÷â\x001cÇùy=Á4BÃ®6´\x000e\x000e+ÓBLDk%v#Z-Y(|Ñø>\x001f-ïÚáDcp£À9Ì\x0004WYº\Ð uQX\x000e\x0017ÓÎuÀ86wû9Ì³çæJ¯g¸R¯\x0008\x0017\x0007ö_¥?e7Ä´\x000b\x0013ñ¶H#Ù×JÇ×{ ú²÷ð3X©L4Unxh\x0018ç&½&\x0013\x0012­û\x0019/W\x0019tMÇå\x0006¬Ø&¸\x000eêR`Å+%=rãM÷½ÏF«Eª±t õÁ±bÏN/ÍE\5ñ8_1\x001c\x0016\x0005m0{kt\x0007X\x0010&° Åh &QöJÕ
Ûò«Å<pú£\x0019­QüÊ\x001cVß¨U\óÐ×\x0007ÊËñ\x0006\x0014Ð£\x0015¼¢Ò&RO³äªAéz·â;3(´¦Kr±)dÁ¡ã\x000bj\x0003õµ\x0006¸\x000eá6Û\x0008¼]=X`)òþa¼]îÌó\x0007RËábî0ýÑ
\x0017kÆðê¼ó\x0012\x000bÝ<¿³®ð\x001aLW¤?ñzCÝU\x0000×\x001dq¿½ä·&×]Ôa¦G\x0016À<aB\x000b_)Wéf]8\x00107ÏÅº½u·6û6p©øÿß=|}¾Ëã§?=|N³ó¼\x001bÜú%rR\x0005ÉSs:\x0008ì&oAùº$¼»¼øpç;O__^O#©t@\x0016*S"­O
ß±ÂÛ^\x0013sÊ×Ë®kFö0¯Y"qÍµäN\x0007 ælÂ-ÞøG\x0007fï\x0013nºgI\x00013Ñ¢â=\x001fhTùë\x0003èÉ§Ô\x0001\x001aX\x0017CÖwOÿör?\x001b2.¤¦öQô}s\x001a(_;sæ>ß@ yzýÿÜÍ@³Õå|õbÄÆ×ê²]vJs'É\x001e¯\x0016ÄÈ \x0015M\x0017b%I½Y¬\x0003çðÂF*Ù¨\x000f4\x001b5 XFMt@)U!\x001bJT!ÄÐ®s Kß\x0019[èÒ\x001fíU\x000e¹£4åf\x001bÍ××\x0019¢.eÙ\x0019_¢=Ç>CUIpÕ¸É?¬!Êaûðåo?Ë7H·¶ýúõîy>Î`I\x001e0®Èt\x001d`>À\³»v .B®µãÓ\x000f3 âèNh(UäÂÇõ½9Ib@r:\x0007BÍ\x0005\x0010%æÒ\x001f
\x0018åP\x001bÅ±SM\x0018¹Ù\x0005s _r	ÆÁ5bÌ÷6\x00069Â\x00189\x001bb\x000f´/ÁÍé\x0016C,\x0019´Ï\x001bÒ\x0011£ç{<äà.Â#\x001aøG\x0003F*Í\x0006«9¥¤#÷ûp z\\x0002\x0010ÙÓ\x001fË\x0001¢+´ØÉêReu	y N¿\x0004"\x0012¹¥?\x001aÔOýx\x0011ß"µÃý<¸Úo¥7Õ\x001d|Õ·-\x001adzK\x0002N:8\x000eRðdêÉï0·\x0019æ¶éÕ$N¼¬}2{\x0011 Û
æÀ¨Ð4Ê_\x001f~zþ÷Q÷'îG¸~xyÞn®îoç\x0007RëÜÃïÀÇÈÙ¸\x0012?9fãª(q7ÂõåÍãÍÕÙI=\x001c\x001cAÍMPÀY=ÀãÈjÈ1³:`µ¡~£Ë±ænÏV¬VR\x0017³ÃeÕ¹~¬e¬\x0007FðcÍÕ¤V\x0011\x001c8ô)\x000b+µÜÝkÝ1Z5ww¶Þ«\x000b\x001c§j\x0019xZ\x000cCëæÀ\x0018Ûr¨¹©³õZ½å&T­\x0005ÕèÂóÓ:0_¿\x001cknæl\x0016\x0001KMënXÜ"À\x0003°Æ\x001f rY5÷D6k¬¡ÍFã<L\x0016\x0001éØÇI5UÖÛ§YsA\x001cJ/Lr#K\x0004n$µ±m\x0010Û\x000cÙõ@V¡\x0003oYå}?pËAñD;`¾\x001aBl»n\x0019;ÕÉ>(bO\x0006ÈÜøøV\0UµBÆg,\x0018ÚóRÒ\x0005ããº\x0007ùõ¯»ÿ»ûÛ¯ã¦Þë»¯Ï÷w)áöæáeû\x0015~ÌÍ¹!pGü½e2\x0008\x000b²À\x0019,,Õ\x0000_^|8;½JI·77Ç\x0017ðãz\x00127unöáN\x001bi6Tq¸j1álÅ\x0001\x0005×[&F\x0005ü£\x000f8xH3À\x0001z.-\x0018\x0008®é¾µ×uÿìÛ¸k¢½ÌôÇ÷\x0007\x001dódéï\x000eºB«þøþ §©\üãû; Ó\x001f}ÐÓ¹¬_À\x0011!Ûc\x00155^Øà\x000e\x0018ø\x0016õ\x000bý^¥?¾+ÿwõ¿Õö\x001bÄ¤©òóôÓö3\x0002§¡Ë÷·¿ÜÍ´\x001de£\x0004\x0016\x0013g80Ô:ó­÷æ`¹8W®_\x001fã	hüòýùñÛÓ9§);ùV8
&ø4ÈþOCÍrp\x0018w°\x0016Ðwì¯x\x0018\x000fv7SºáÜÖ\x0011À:RÀ«\x0003@OóÍ\x0007²;
\x000erí39wÅ\x0004lEH\x001f\x0006$N\x0005GlÞ\x001c`ðê:\x000b:N¯z\x0016ðéµ¥³Ð@8cÎ	(î;\x000bÜ[÷»]À:Ü%IÆ4uXw¦±ï, »Î¯û^43|Zx:\x000bC³¶}'WïÖ}ùØ¢\x001cé$Ca#ÆÈ¯E\x001e ýì:\x000bvWø_Fn­¬Å\x0004Õ
á±°}Q¦UÀ¦U2ö·øu¿Ì"ËsÐ	\x0006FìôØ\x001fæÙÜÿïs>1páW÷?m\x001fë¥¸¨%\x0015 ¬Á,uú\x0000Z;ö\x0001¨\x000e¤ýÎ^\x001f_½©ÞôýÓß_þ6fD\x001e.úeóîáå3{± Ò´Êó\x000cÁ.
®áÖÍ»Ësø\x0019÷|\x0006ÄiÓqýº¶XÏ\x0019£jBSªß\x0013â=èÏ\x0018£\x0002ß)Èyo,>=\x0012äòÓ\x001e"r\x000fùáö¯îgý-i\x0008eî··Ó\x0012¢»ù-aaw×\x0006Sk4\x0015h\x0005\x0007¼Á\x0004Jíìøä<-$:½©4;ü¿ãDl>\x001a#â`PÃ\x000cºq\x0007Hà;\x000eð;>°æ\x0003\x0018Ifß\x0019É\x0018
*ÎÈhv\x001c{óV8\x0000GÄp\x0000Z\x0003õ¼÷\x0002¢úÊ\x0001ÐèUDÈF.çIg}£\x0005O[\x00193´jî\x0001îÿúsx#óùþñáËÝ×-:&w×\x000f·/Oà©,¨)äãÏT¬\x0002\x0013'ýÀ!\x001b\x000eÌY¼¿º|wzq.	üýåÕÉÍ5ø(s°çÄwýé·ßþj¿|Ãm¹þuû\x0008ÞàÜ>\x0005\x001b".âzZ jP¤Ùby	\x0007Rã¬ì¯ß\x001f_\x0007XïW\x0018ð"qÐ+5Ì\x001b\x0010+ä{Ê\x001eGÌå8Áý	²\x0001ñ·ç\x0006¸héÒ\x001fíp!üQÔc\x0001ê=È\x000cw§Ó\x000fµþ,<6tÁ
»ºµÄ¯\x0019®\x001bà\x001e\x000ffÀ}ùíöå\x001fã9X\x000ehZyú¬¥©ãÄHã8 ¹ôîäVTdf²®ýãoû_[1>Î¿f7k¾ªvÎòÜ\x00082ÎØ<é-<\x0003wâÀú8ý\x001d­º\x0016îö\x001f¿}\x0018, ;ÿÄ?¾ÜnyÝs¤ê<NYËt¼\x0019±÷òPëÕõæÇã·7Õ
æüòøë?~ù­©\x001e{Sá÷÷¸\x0017úîqö4·1ZtþRïUðDÓìÕÐ@\x001b\x000fMë½?ÃÐ§Wo/ë(ÿþü×ó¿çÞ»Øüüßÿñàp<|Ý||ø;<¼Í\x001bl¬ýútdÿÉz\¨TBpûz&j¾Ø¼Aïûäòbóñò_á\x0019\x0012ß¯6\x001b£àã[á\x001cÎìÈx5ñ\x0012Yé\x0006[(§gÎQD\x0012+\x0003L¢§s@D©K­\x001cÆ\x001füd<Ñt\x0002o¯\x0011C\x000cN\x0001ïÁäSxNùDdÿg£ Å[á\x001càVåÁ@óÍ¹CÕÀõª¨§Q4£àë?Ò -\x000e8æRÑðð&¯l:GÁF·Æ÷°GR`\x0019òt\x0010|\x000fÇÚJ\x001e(Vuc8m\x000f"\x0015?\x0010¬¿åá
n³é\x001cå¢5ÎáY°¤LY:\x0007q·\x0007ñÏ±\x001e{pk#E"é\x001c!P_²<¬c^\x0010Ñtr\x000fÊ
\x0007\x0011Xã¬Åmy*\x001fÄj.iV°¦wý\x0007Ö
\x0007.\x0013\x0002)!Ïô?ÅìíIYá !\x0012¥\x0007\x001cÄâ&©ôE4/fðaé§å {Äxý\x0007\x0011Ñp
7å
é\x0008ÞbèÅ?Gií­ÇXá Æó2´`4[CZ\x001dï1?¾¦dI'ÈqßýE\x001a xxyfÒï÷¿ÜÏ-¨ä@]`Â\x0005[s\x0015y+Ö\x0007¶W7\x001fòûãÙÛ³zMp@nÇÈm\x0017r0Úy×\x0007¨¤H&FûÿºwK¶ó6Ò\x0005§Â\x0011ìÀ-q	=Ñ2Ëf$*(ËÑÝ/\x0015\x0014Ëfµ,vQ£ú<õ4úµßj\x001c5\x001eIg\x0002X?Ö\x0016±Ö\x0004}ºNÔqhm_âKü¼!óKyXófR8Ü<9Õ\x0011\x0014Øg\x0017\x0017¸Î\x0019\x0002e\x0000\x0015»Ëf2bq\x001a{\x0019õ¥¨4&È\x000eë®mvÓ´äK°ïÔ\x0018[`Ä®Ò\x0019\x001aªn-Àxî¹c·©cµYÅîÐ0\x001c°ÓO
vÌJ½¿{\x000bóB_Ø'\x000fÉç±Ã]wî.óðr=wÑwÙØíÖs#ö¨Âîc·úØf!1\x0013Ipî<v?»×{*\\x0001\x0008´¸½\x0013Ôuf#ò`\x0006äD\x0005¦@N&=1rËkQÛ¥/ÒMxHÎCO£Â$Â ôVâ\x000f6\x001dËEå¼²>Þ\x000fý7Ðh \x000e¸++æ&~9\x000fÄ\x0017ÝæÓBM\x0005g'LK÷9*ß\x0018ÄÐ\x001fuÈ\x000f¿|Ä(ìñoUK`v¢\x000ci¨JÔÊ¥m1\x0001[ú\x000e°r{Ñô7¯þô\x001a¥yþu\x0015é\x0012Ý\x0016Ê\x001dr\x001bJ^_ªPEh\x0015ÀfÈ3\x0013Ç¥\x0016Ê\x001fò;JDKØ&r\x001cÓ?¢P}AÞíµ²ëB£Pa£P\x0001ÃhÇã:W RÕUêpGoY*8J\x0005\x001b¥Aö['ZÊ*^½½Yo]ªx*nÊÊ{!eÔí]¥2¡oh\x000c7\x001b&Ö¥JG©ÒF©\x0000d:
µ\x0001n°Â×\x0000%8ëRå£TyT.YÙÖ¡\x0008F\x0016A.ñvYmYªrªlüVFÂ!¦Ì-;`4\x0017÷\x0019
»5\x000b6\x001b?\x0016X©FçÅ²\x001bÛÒí
¢ëbÅÆÐÂÉ¨e¦D0NJV9æÛ%«e¸Ân\x000c,\x001cMú>åÂéMÉI®Uøá\x001d"\x000b»1´p­¯\x0005ÂN	ò*b'ä j±ØÂn\x000c.s\x00121á\x000fL\x0008%IBù|\x000eË\x000eÁÝ\x0018]Ø\x0002ÔQÅ¢ÞWÛÄ
R\x000fK(áç\x0013k.ìÆðÂ\x0019/\x0013ç\x0000{{Âe¸\x001e&>XCxa7Æ\x00176E\x0019i\x0000*¨ñCPBÌg\x0016Õb
ñÝ\x0018`Øà¨\ß$0Öàâ`NF\x001eWîxXj/ìÆ\x0000Ã¢(¤
B\x000e¾Pdõé¥DËb¹!Àp\x001b\x0003\x000cü÷%\x001f\x000e¶0c¨V\x0007ç>£ÛrCá6\x0006\x0018DiÅM"zt\x001d$\x0013´¶|>ûîÆâÅÆ Ã\x0010\x0013v»Z>gîD
)2Ý-¾)4µXCá6\x0006\x0019D$i2Ïv\x0019nÕÃ¯eä]ÙÜÞä´.Ö\x0010d¸A\x0006~$1\x0019>Ûþ¦Ùßýã\x001d\x000bªÖÅ\x001a\x000c·3ÈÀÐóÝ²^\x001eP¨KNLÆ×L-Ö\x0010d¸Aq²Û\x0001¨ç95Õ&ºÏì»!Æp\x001bc\x000czWç@×cè\x0014Øb\x00041b¸ãa}Y¬!Æp\x001bc\x000c\x0011!»-¡\x0013\x0015³0\x000fGó9Å\x001a\x000c·1È0¡wÌú\x0010*¡²²X~ò\£\x0015Ë\x000fÞØoôÆÞùjap\x001cå¬õ\x0019~¬ºot[\x0018¿H»,-#¹q¼½àVQ\x001e¬\x001b+\x0012áaw¥>åÊè[\x0006Ó~ÃEB~b&Óú´ÿ_Þ\%þo6æIí\x0000¨¹ãxHRQ£u3/¯qc,ØZ§WIzÓjU¨&²5ã\x0012\x0011Fï£ú²'ÒÁ^é¨TÃMbYjC*RÞ WS+ß^iåÛ}1\x0015\x00032÷â
û3zXì7¾/UëfãÖfcp6p\x001a'³Ônîè\x0019]ðº\x0016n¯l\x0018\x00131¡9®Âµl+¡p\x0011è_^G3¹ÓJú ¤hNA\x001e_s§¯Ïºà?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=zq~röï'ç\x0002Æ\x00010J	\x001d,\x0004Pdp²ÕÖ,FèýýVh\x0011î`Ìw\x0003ÿå|Àå5yÙÚ\x000cÊ"ýL\x001aÛ\x0000A
 ¤8BlÌÄ¹ÒL¾eçD\x000bd0"\x0018\x0011çÖÒ\x001a\x001aE¶JÆ3bô÷ï(BD7"J·!ÞëÈõi\x0008\x0014-æ;'+ì83=SèÆUtâUÄw½ÔXóE\x001fZk~a	3£ce~\E/^E\x001dy\x0019>\x0004Ô8\x000cë)Ðn=Î½¶(\x0012\x00061¡qMq/y~¥­i-¸\x0019!\x0001\x0011¢\x0019·¢\x0011oE³×ÈVÞíë\x0012Ø(æÿæý;³\x000cÑ\x000c[Ñ\x0018éVDm NùgÏW[ÃÊP\x001ez\x0011\x0012hÖ,"ÉS+\x000fØ=Ohy\x00117çÑñ\x0019±ç3~/þhx^¯
+eüV»mÇØ\x0001\x0014\x0012: ¦\x0016RhOº!±F Z%CÔÃN´Z¼\x0013­n;\x0011\x000c?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001eó9­\x001a÷*:>î¡e×#gj]ë¸\x0003oó~»#ÆLk0KK{!LkGÕjN|y»Ý¥³9±þÅ$0{·"ZZ]Ô~hÖ3øUX	c\x0012Wzó]\x0006lñû¨~%êôa«\x0014Ïù\x0016\x0013àÍþ\x0004XzTPAPÏù\x0008\x0013àn\x0002¬«¿þ\x0004\x0008.kT£ÒUÞröÖÈþ«<¤³ÌÕ»ý¹ºÂª¿jÞW)ç\x0013¬&¦ïJú}üúþÝc!£OØÖ·[\x0008Ø,OÐ7w»¾g/^?}2§zÛ\x0001Ã$<Oy&%
\x0002b/9rc#'*QWSqëÝ^Êã(`´0\x0005ºûØi@°&Ôm.\x001eJU$¼_G^;!ÛD&O\x0007HXÅÚÇ\x0008smP}º\x0010%I3ö«{>Ý\x0000!Wï\x001cy¼cfUVúîþGiox<4
_|HÀ\x001e2.÷9\x0007±Ì0¾|rý\x001béqxt\x0012ü¢úv³\x001255q°\x001a\x0005·KD5á,°NÁº°±É{\x0010l»{VXèv=e³²l^iY\x001fZ\x0007úÓZÙVVyµ$¸õ@W\x000ejÍÞ\x0014XI\x001a¼\x001f\x0005ê	Æ@¾§Ìæ8·¨FÌj'³u\x000eu´ÐsÕ(C5Hr\x0015¿¿gqY\x00175k\=\x0007\KcÁ­³fÞ\x0010«-²ºþþfÚ iÃ:ZÜ ê5¤Ò\x0002o®®(Ë+Á9ö\x0002\x001bõ¬+g-%­±m)JÆ\x000f!ÔØ¸Ñú³LIòMää5¦-Ðj\x001e)+}\x0007\x001b#0¬³ç0­\x000b>WÑBË\x0012"Ú,ç+Ô\x0017sèýyh¦]·!\x0018H²L\x0019ÿmk£,2w\x000eX¼Oaés\x0005l
¶4A\x0012ïhOõ\x0014åe¿\x00148\x0003kpj\x001aÐç\x001aÖ\x001c[\x0014`½'Qôõ¥"&9zÐ²]¬gb]úÕ\x001a\x0003ã\x0000;\x000b·;U6q]»1e[Øg¦­a\x001dsÝÊ¸ÒÂ·F\x0013m+³RäS6Ú9T]Éû\x001eV½ï=ûúéïÇoW!K¦#¥½záJÝæ\x001e%½¾@°\x0015ÍVØ¢\x0017ûÕ7q×Ø¸F*Ä8\x0013H[D6y³'2õf<Öæ^Pêõ\x0014É(uÙJûj6¯Ùü\x0010[NMØ,?ß\x0000%¯
¹Ô/c\x0003Í\x0006clsA¯­È\x001aå\x0003(M#ª×\x001f[\x0007x z\x001eQª'Jh}\x0019ÌF¡éeàÇ\x0001î\x001d|lÓ[\x00154/\x0003êç2\x0016±\x0005½\x0010ÂàBÖ¢Ì\x0006µMn]\x0008Á\x000bÛÜ\x001bñ26½\x0010ÂØBÐ·\x0010e¶9N­Àà&2½\x000cÂØ2@7\x001c2olß\x0008tIdky\x0019Z¦×A\x0018>\x000fÉÌ5L'{\x000cZôx¦±ñÄ-ÃÉÆ\x00065ÄJl\x0010e\x0002lY\x0007I-Íåú"U×Ü^¡GRiÿXæôöá\x0006·\x000f\x001b8wÇç	NîSÁÎ{.B\Q	-Ä!4c¤¨ößÂÎãÀÌe\x0015-CË\x001a- hFh\x000bÒ0C³\x001a½]T4rH6 Ú=\x001c\x000cí\x001e©x~¨÷$Ê$d²åúTfÒ3\x0016¡eµD]\x001e\¢­¶Ðï\x0003\x001aä>ìÝ\bÓ\x00126oÔQE#f£ÒR^\x0007>Õ§d²[÷t}Kû^ÄfÕöA#lYv]uÝI?À´Ìi«¹1«áùäy²\x0019¨AzBó\dDh\x001bf×w\x0017?vw©lÙ¼¼ÐÚ\x0014¶°a×õÁü\x001fæÞ.Ç$ÇóÝJl`\x0002f4Ú\x0017ô¤T©«5È/H©ÂzIDV\x0007ªÉÊ,(SêzmÜ\x001dÜ\x0005Ü\x001dÌNîJ.iFÚqóðsÂé\x001e=n [GõÑ?4\x001aùçÄÎÂ2è[Aáy¢ÝÅ» 9mz-Íl&³ËO,\x0012~°[o
Ã¸ùz-Nv7DÝå+Ýdr	òIAm?³ÙÒ¼Ùm³aVÓs\x0012XÚlNÍÇ[UHó%Û\x0005/¯¸9Ti	<¸A¾Ö¾\x000b-O¾jî\x0010Ùat±O"6tMôÙ\x0012Â°ù\x0016Ó\x0011¥ÿ×êGynýÞK\x000b2«ea«#
ÕäHy±²|SWï±j×Þå÷áìªÐèªãY\x0015Ìg®¡\x0000WW-	Ú\x0010¦/`û¢\x0014zg9£Ð¼²Ñ\x001d\x001978\x0013´ál×Ðf×R}"R		rÍh oÇ>¹¼`\x000ei+Ðµ,\x001bhdÓX×
m\x001dÓlV/ñÑvÏÜªÕ·\x001bÅg\x0017¥$]¶èO¸ø8ßâ£í\x0016\x001dJË\x000e¡õ®\x0016«²]k6ØÇg6Û)uA\x001a\x000cÍÝ{ÕÒ/gî\x0008y6»ÙfvìY\x0007¾%ú =èTû*æ\x0013lÕO\x001aØ(¬Õ,`z§Û8yNt"\x0012¯³á­6Ã\x001bjQãF1U{vllÚÀX[Üq¶:³r\x000cÈÛM\x001egâcJ ËgRõu¾ÀTÛ\x0005\x0006uò+³eÉ\x001añÛ>ÍÅ3×¾
af3\x00197Ô¡_ÄÄ|u@e\x000b'\x000coù(é( OU¶ËQÈ*vSc:sLÃäLk09S~k¬sHrI  e\x0015¯I5ìB3Õ	<\¾ßI\x0003­`íæ\x0015­©\x0005\x001eFËáåÆ \x001f´è»\x0010\x001d\x0004UªéL¡æ4£n¤tqQ/O?Z}\x0015³ñè¤Î\x0006õ+­³¿ª6\x0015¸3Wí®PØ\x001ep­Óy\x0007w«÷4g{P\x000bÌm_8¨z+å¯RÚYÊSêÃ¢%³?ö¡\x0005\x000e\\x0019±U"ph\x0012Å\x0018û+àQ#\x000b´ö{?\x001a\x000f)C_fÜXà¹Y^ÚmgRG<Þt\x0005g1o<H*_\x0008\x000e´·>æ^^ÆpþÌÊåÕÊeÓÊÅªBL£ÖÓ·¬\x0002çòq_\x000feµrÅ¶r1jçîÀ.\x001fHÞ u¶TðÄÂÙú¶ß\x00166r\x0007Ò¦ê<HFýl;ñèÇ,SáòñßY\x0010ALç9 =Ä$##î°'<\x0004\x000fïúÇdN^ýÃ`L*\x001d^"dr5ËÕf¦·kC,ñ\x0019v"X:Bs×tP\x0016_ö
q<üó\x0019×÷®\x0007Pj0o¾U°»\x0012ðß¼þóspÞ%\x001cÿ´ÑñþÌ\x0006\x001c\x0002÷CöjK¼¦b·/Î|ÑÈÇÅs*\x001a$ÿ9\x000eÑèk\x0017Â½xyÆ3~Ü\x0008ãµ=Z/Ââµ³¸k\x0017¯]|Þ'ù\x0012\x0000c`©oéÓO®×ÆE¥öZd\x001f_¸\x0014ö6¾05éïàt:zL\x000cÅ«´ZjútÒ\x0001}í-d/ ¬\x0000\x000b¹|"ðH¯Ní½QZu¯=ßï\x0005Ä\x0015 \x001a\x0001éÓ?pÎQ\x001eºóÚQ\x0016út¸\x0013|iÅ_8xi$l_¸\x0017Ä§Vö*_øZ\x0019Ð^À²\x0002,VÀ$ý0@N¬)\x0017\x0011 WI\x0003ü®x¶|yuD²õ¬]Ã¹ÞU8\x00156z°Ï@¿xÄ\x0011>ô?*OT¼:¸ÔÞãô\x0008qq>ä¼\x0002´\x0019é\x00183J\x0003ðZ:`\x001cê\x0005¬o~
°®\x0000«\x0011°ôÌ:\x0003FM\x000cð(h]A<¹\x0005/²§\x001dpÒ=Ý\x0005\x0018%!@}<Iô]U§bÝ%h\x0006\x000c+@[\x0018ÓV°\x0008`è²}\x0005Å
b+m8\x0003¸:$ÅzHÒPRà¢«,xIâ9+~vsèn.¦rFÒQ\x0018Ä§Ê\x0019dµN- z\\x0001\x001aÝ\\x000cAÑ_=e\x000b\x001bQ\x0007¼¦°\x00170­\x0000­~Î\x000f59ºÓËÍ<9¾ßwÀpíav' Ì~d~ÿÜ\x0001Bí2\x000bD
jºØL\x0002ÐFZ_óíHf{ç\x0000L~\x0006LÞ\x000c\x00185\x0016L¾\x000bÎ4@=Äp5ñ²o\x0005Óê$ë!I1é
&§\x0015°éÂ\x0007pj\x000b&_V|ÆH&Ah\x0002í\x000bGÉª%p*àë5Ùç«-Ì[0¥{è_8Ö¤Ñ>$Uv\x0007íQc/`\\x0001\x001aÍt\x000eYâgÞö
Úº§â\x0004yEg\x000cdrÐ\x0007o\x001e\x0006Ì\x0003µ;:\x0011\x001eËz\x000e°®\x0000L"7,V¬Q½\x0013\x0014U \x0006­Hk'`\x0003\x000c×õè÷-ÚNN+¨¯~;\x0007\x0018VÆ@KÉ"ñ=KÈ\x000b+¿&`µou@¬Á~NE\x0017ÌSsx\x000cXó°×ª\x0007v\x0002Ù
§btÃ)k\x000f>`QQW21ÐòþÚÌ>ÀìæCÌ¿Í[0Ê\x0019aånÝªæêÓ¹3q´ø·ÑËe©Ëkn8\x001bRDÎnøÎi>#9YÏ\x0008}âþÛô¾èÆ\x0002âµ¤½|qÅg=#E¦'ò\x0017.Mt\x0001½¾AÓµäÜ\x0016L«-¬[0Ã=\x0008`öj\x0005Ñ9usåä\x0019Iu\x0005hô#\²ÕÑ%©ÇO8jmhcòÄyåG²ÙÔ^xÙ¬L¼ÏÝÊ è<7ï®MÒÙ\x0007XÜ\x001ciño#`W;e@
\x0005%)#V¥Ó\x0019G\x0017Ý\x000cØ~Û\x0000!\b\x0019¯±j\x0018£æàö\x0007ÞÖH\x0019Nnùà5\x001cÝôàµÓ×EA~}o¾®¨\x001d¼&Î¹ïíazôjËG¯\x001d\x000fÜì.ý\x0017,Ö\x0015zµ\º4¾ûkª»o\x0017!±qç|°9\x0013¢aÜ95 ÔFK¾s\x000b©Kzú©)d°jP\x0001I¬*bBQ!V\x000f×ê½÷/åOOò§ÿC²ôgÎËí³¸6GõýÇ»ùü@ÿöO¿Ý½ýí÷Oo\x0011R\x0018íõ1Ñå*V1D\x0017häzC~|{÷/ï_ûæ»w\x001fîÞ~øáÝÛ÷Ïb.¼3a6ßlÅäÁ:Ø%ë¬6,eH\x001b®s\x000f`.<LaQè\x0003Á4\x001b\x000bH¨Mðª±qn8y\x0011¸cÌ6~ÆU­Q\x0018\x0010Q)ÓzüÒÃôÍ=\x001cùèÉ©v\x000fU\x0012÷\x0014kózxÆ\x0001Î8sÆ#9É\x00050P(Áã(ðásµV<À¦ÍÙ§qZ9KÐf,æìµ³ô·åÂy\x001aóR×0[m\x0015³bk¨`ÌRtPNÒÇ½â3ÅÐ2cB\x0013Z6b&W[µ{«#-0bL@qååÉûÅ\x0001N\x0013àÀrRÜ­0àªÂRØ\x0006Ê¹\x000e+\x000fp^\x001a\x0018\x001bgk`4r²L\x0008 \x0002ðÈ3\x0004¥ÉáIht3M¶\x0013Ò\x0001ãI+×Ü$¯'§çûrÆ¢ÕA	Î/gRËÏ1QÈ¹K[G¥1p¹>ÉÚ9ñ2Ê9±26ròÅVZ[È9j\x0001bApç}Qwg<²;\x0003i@úþI(6\x0007¹'5G0Ëy +trt\x0012}Ô\x0006M:à^åöpÇ8À\x0019'£Ä?í£Ç\x0015\x0017E\x001d²vÈÓèürF1á\x0008¦¾`\x0012'J\x0001j\x0005UZÄõH#8S\x001eðDü|²O:eÌàrÖ\x0017XÍysÆCSf]¶Þuyo¾~mµc¦Ù"¥#\x0016©º|ß
Rä19â`ô(>?cÇÌyÂÌÙ.&mn#&\x0015´\x0008ã¨»<í/s¯DÅ\x001eu"yD\x001d\x0012\x001c£8	!ù çÏz¯nåÀÝ
=ÝÝä¬ÇØ!/Úü\x0019àôÞ¬n¬î\x0008d¼@ò£DßA§P´®:t\x000f^äúMøáÀU\x0018$ÝÊ= MÂ®]uqÆuô1ÒV¤?\x001dÊ-:R }V_À¢IÃü¤FÀB
Ðªå/Ï´ô\x0017¯`!Kúx÷óÃÝ>=Þ}õëç_\x001eé\x00067Ê\x0001HL\x0017´¯jUYýF\x0014(ßÞ}ýúîOïÞÞ}õÝûoß>Ë\x001aÃ5c¬ôý«ªe\x0016lY×µäÒAØK53Ã.UM°URï\x0004ÛÕTÚÂú\x0001{E°Þ
ë'X\x00086RÄ,\x000bËBºÒ±s	E]ÚV«6²^:\x00005§\x000b[ZÉH\x001d	±¤Uþ%@/u~\x000cZâAÐ :ðèü¸%'T1åu\x001fÔQØÉ\x000evïÇ\x0002Ë[e»&§\x0011Càý\x0004ëýAZ²\x0004"~X/`¨j¯\x0015Ñ.\x0014\x0016ÙÂ|»/$ÓLÛTçý\$0¹ì%hëd
øç\x0011Z¨UE13ïî\x0011`Ü¡Ø¶érj+Â1Ú¨£¥\x0003¿ÞôÐÐ^Aºè\x0012^}6ÒæÙ'äcN\x00010hË|&CÛ\x0016ÏEµÒr>GKÿl¡Á¥\x000fÑSh°\x0005ûÍÃç¿þz»Ù¯àÈB\x0005A\x001aø_Ð|\x000f<cm¿yýþßÝêû\x0013\?áníÛ=¸t\x0016\x0001\x001dàwï¾¸ë@´³>½\x000cnp·Â®Õu*VJ\x0006@_L*$Möf|Õ
Óf\x0008G7CÈÒ@¸¨\x0007­¶çü2{¹m3mÜò\x000f»hQ\x0015ì\x0001Y¨^5=
kÙ¿\x0004î¥oq\x0013\x001eÃåB\x0012\x0012\x0001<Ô 
Ehu¯2°â.:»	7oÙÜ=«ë\x00146Ð\x00157õVªÖO\x0016|Õõ\x000b©\x001e\x001f{Ûè!^H:ß\x0004¸¦¨;à:§Ê:_pw¡õÂ¼°uÏÙÅëõ\x001dÇ4IK·G}¯rîx|'ïBTyS9º\x001f@ï:LY\x0017çàT¶Üv\x000b>\x0013;îÄÍ3n>ëÆ
Â#Ó¦âÚ<Ó÷EN\x001b·O/yËQOÁ-±ò¶N×uñ\x0014¥z}dMÏ]$vòÖyûÖÃÛ×ÉuÎ\x001f÷á+2<wx7uG¼vÂª×=ùÕY¿ÿôøùósq9é\x001bt\x0001ÙEÇÅÖºñ\x0000Ó\x0019¿÷öýû[aXçÃ\x000fÍ|poÆ\x0005\x0012FWt\x001byt\x000e0NÑ\x000c\x0008\x00030w\x0011-\x0006«\x001b¯ÿ&¾K¾V>7´EÉÚ«LÊ^út¾\x001d°LÅ\x0008Hw©1îZR>\x0001\x0001l°nù´\x0002.ÆT\x0013`uÖ\x0015ä\x001b ¤\x0005äT·Ë`Ñv'ÏH	\x0010Ì8ÑePõ¡
Ðé\x000c(\\x000bº\x0001§3R­g\x0004X¸Jská¾ \PÇl5¿Ö·5\x0002Ò&Y\x0002òO+á\x0010¢n*%A	u\x000fn<\x0000ÃtÛ\x00081\x001b`ªz1z=Æ,.$éä&ô!ÍÉJX¢^âw	Á\x0004j^\x0017	ËLhµ4djÆðDÒöÉ^ÏÉyDVB,G³©É^Õ+\x0011Bk4ç,\x0019inOTÔÌóAA³­áN¢QV"\x0013S\x0003î7ñ8\x001f\x00144û»<ÞE&]\x0007\x000cîò>òô}Ì\x0004¦Æ'kD\x0003äND"\x001dCl³Gù$_Æb>6\x0013Îç$=r¬Ã#\x0007}\x0002\x000f¾x5×ñdPèó¼\x000b³Ù\s¿\x0012âXC-¾#Âs!ÃòÖäÖb\x0003t^=\x001e+ùJa\x0013[\x00185×ÇÏIY\x000f@.}\x0000²\x0000¾'ÏnWÐó YMkòtN©²¤¨PëÓq{\x0013¾§\x001fïßÝ*¡\x0017¼7á\x0012údÃãÐKÁ·\x0004­<¥©ãÅíåÛwiËb¼TxÜu\x0000²zE\x001fáý¥l\x001e×ê~F¼2}Übü¸\x0010TyÖP!«òz8\x0011n1	~Q(¿\x001bkùeçq\x0007­\x001c]Ð<	¬\x0007-Ùè|é\\x00040âù å²Þ£&Ðéà*_Zëq\x001aùòt0¦üV"zV)à¨"\ùJµoqÝlæhä£ûº¨ä{Ö`h4Ô£¹`Û4ïåã²¶\x0005\x001fÿ4òT¡Ñ¿,ídm24Ò©Ï\x000byÆËF<ÇÃcõº6\x000eð`\x0004]½µ\x0011oþº`ýºd85ÙáùùY\x0006Ì\x000em\Î\x0019>ºÉNnÃE#\x001fE©cýú»-êÇéØ(-µðÁìÖÀvz¡æ1GÖýBq^¿ï\x0013yN+_ùOÅ£Ï24
rÕB(2Ùç>oü\x001aÿ´á¤Õ$àzõC\x001b =zCâZ0ÀÊ\x00073ÍyÐAõzI\x0007®~õC\x001cM\x000c\x001be&>ùlÇø@;¿\x00075¡ðiçW©ç[XE}Ö°Ïñ¥6WT)Ä¢\x0017\x000fWaÝØiåG°\x001d\x000f:#váXgXt\x0019;½8\x001f\x000f4Æ}mr½,\x001fV\x0011Åê`|Þµ¤o>\x001eh­hý[³.óÞ|¡dUL)'cóñ@«w#,£j|\x0005IôB£'Ý³|óñ@ëñðcRºçF\x000fñ¾ñâ=Öú¡V¾<óÙB{ò²
££*õsP@5­(ô;u©\x000cóµ(\x0018ïEtRÓX¿¨orÐDì¥\x0005òÜùåû\x001aÍ³Î·tµÊh²Îy<ÉÛ~\x0018f¼`Ä+\x0005ôóz§rÄqõ8å=p>\x001eh<\x001eÀS¶Q¯/ÓÒ\x00087:2mÇcR#Ò\x0004\x0016L1ô°Ò\x001c£J\x0008\x0018üòlðâ\x0004#%ÔXG±ó2
(>Õ@M¶ò\x0008¦SûW¿xµ(wûr÷æß\x001f~|ør\x000f\x001d|è÷àV\x000c
Òþ¢SÁ]©ÿx÷æ__ÿðöõÇç	Ã0	c\x0018Ã	¥V¨5\x0012i}.
§	qIfB\x001eï!¢I<Ô`T¹n×³\x0019\x0008ã0	iád`xªúb>G­Ãu»À@É¾¥9b&LÚÁÊk(\x000f"p¥\x0018ß\x0000Ù\x000cHWv±¬*ÚÛ\x0003Ñ'?ÎÉvÙ\x0001°,\x0001\x00110T\x0016\x0006¹Qgs{® äÓß¸.	«0£Hâ\x0004Vúëºí<\x0011^ç\x0004V¿]Ë³p!\x0018Ûæ\x001b\x0011SæäUÆ\x000c½Ó\x0019Ï¾\x0006ÍµÕ^Ó\x001aÖ±Ñï_Ùklèý:³u\x0000\x0011&D°\x001b\x001bm\x0000âÆOP{\x0000!n\x0017\x001c\x001a\x0008'âí.\x0005@\x0007ÅXtÏCË!Äí¢=\x0003âäR¼Ý§àhíä¢øe'\x000fKôI§\x0011'âíN%ÒGÖ.îq6\x0002jèàóùÓ29\x0015o÷*~äY9ºb´µ#¬öÙÐÁO^ÅÛÝ
óè"F©ËCE<\x001b:øÉ­x«_!\x000f¢\x001aÚMS&d\x0010A\x001b¹óéØÁO~Å[\x001d\x000br¶_nTQªàÚ"j_KÍÛ\x0011a²Ûp ÎNÚ\x0013\x0017«Ö\x001dñ*êwNáìÉ*Ý*\x0012W\x000619(\x0015XaÓÉ\x0001»É©:T2æ<\x00161§Ë\x000cä³ir~Éìü¼\òZ\x001c\x001bä]\x0011¡8ñZ½²\x0001q:ÐÉ| Û{¬^\x0006@Þµ\x00072èe\x0000ÎZÅ<mÅ|`+6-4í`9Ðyt9®{ÞÍ´¦[i´Zî\x0010]U£SX^äß@¤ñ=­èa\x000f
~e\x0017ÁÏvññîÏ¿ýöéñvý\x000cfÐ\x0003Ã=Wý\x001d4z'Õ3¡©Ùo\x0016Ïÿðþí\x000fïÞÞ* \x0011ÈKÝ7Cb´C¦¢oÉ%k%\x00039@-\n*Âg)/"àLYÒ¥ôN;'
ù\x001bÙðE\x000bÀ)ª¼ÖéaÀ,\x0013f9\x0019T<±*G'¶ià\x001dóZ#à~ÈK\x001d8CVw\x0004²ªRDe\x001dÜ$ûr|ò¯5%\x00190aÂ#§g´×àD 5z\x0011\x0014ö¸\x00057Qúºº(Ð_´BO/þv÷ááË_{\x0002òª
¢£¡Y\x0013nðÖÄ\x0010UÚ±bÝÊ.~¸ûðúã\x001fß}x\x001e.NpÑ\x0004\x0017xÜ¼âÒÍ_ÏòîÖªï6¸p1ÙàjÕúàUûÅ+Æ\x0010ùõø$#\à²qåª^[xÎr\x0012ðªjêuCºÑÂV'¶jc^ssºåÖKÙÒVmÃn¸\x0006	Ã%o\x000bc\x001e:Ý¦¤(gÉ
ÜváÅ~¸0Á\x0005#\Ôrààø\x001d¿c(\<\x00077\x001dÖd<¬òÒÃpcLMàq\x0008\x0002·]¯·\x001b.OpÙ\x0008ª6\x0001T´1'À8\x000fÛåR»ájYÂÕb´$eX\x0012W$ß\x0015H|ÖÍ×Ú½p¾Ì6¸Ø[Á¤\x0012	¹ÎQ<\x001aaV<³t\x0010&:\x0008F:
îµ]l^×5\x000b\x0018FKXÜ&6Ð-
AîR\x0008²ÁÒç¢Ö²04âr\x0011~³:=ú¸ûö'\x0014U0\x001cûë>^#\Â\x0012Æ¸$&yL "Üp¥pgl	¤ù«&ãWÍA®D<gÃËÔñ¤ëVÖÓ©mlyfËV6P\x0005\x001aþ£´\x0013`¬ª6»]·º\x000ef:0¯6cÐ\x001fE!\x0013Ç[1\x0017Î¢÷\6î9F\x0012¸ÑFgC¥eE7Â¥\x0019Î\x0016n"\x0005À\x0012\x000bcÎM«¥ï:µ%eCîØBWf:\x000bcºªkWe\x0014Ñ\x0005=¯eCSt?]pÓ¡\x0008Îx(JPEèÄ\x00021kÖÏ3k·¬Æc:´\x001d\x0004Q¯²<ÿMzXRº<Èm6
\x001b®`\x0017
I¹ýd»KxM<s»\x001cZÈ:,»ºõN3ßÃïÁzKÔbKy\x000bé·Ä¡´\x0014}]':l)ë\x0004êÁør÷Õ¯_>ÿõ&Z!»\x0008\@Ñ7^Ö*Ðu¢}¼ûê»ïÿø,Ö%9ÁX£U}\x0017VÀ¡p_J¦Ê&.¸Ð¸\N6]Q0¢VÖCÔL\Óg¬¦Ï\x0018²çpµ¶è\x000eä
cÁÖãÎ
`~Q÷Â".YÈx\x0012\x0019
YTÍâlWÚ²»{Éü´Å¼7í±4Äå\x0015ÐEv\x0005ª\x0006¥º\x0011ûî&\x000b3Y0í²QÊ\x0004XZ\x00070Í<jïÓL÷~²8E\x0013\x0019¬
]X\x0007ptã[^\x0019>&Pe2m~ºV%U\x0003CÕ})®\x000ce¸­V½Ëµx\x0015e2ð&²¤ÏP@»MÔCÝb\x0005»ÉæÍ\x000f¦Í\x001fõ=\x0005Ôäa§ÖÊrfÁ¼õÁ´õé\x0003¦Ë\x0006óÂ5Ç
Y0ÁL?FwH^ÆÚ2\x001c·ÖÃda^²`Z²0\x001aÅXÇ\x0011Ä']\x0012nëº·\x000cç5CÓ\x0015!sÃöG\x0015¶jí&WÉ®\x000fN¸B#K¦5+ã¡\x000bx¤¶lë·sÉÀOK\x0006Þ²dÅw}Ài«cÉª\x001b}Ce#ÔÞK\x0016'G\x000eÑâÈKqÚÓ^\x0013D"²h1z\x0013G\x0013\x0016C#\x001aYµ¥ÞWÏdlÖD\x00194ð:n%÷ÍÁ5¢ëR±½l´·+ÔÁ\x000b­NWÖìD\x0001e^³bZ³:ÊZæ¹\x001bZÕgn)íåªÇäû¹ªK#ÓÌ¥´}Á|Ñ®¾\x001cN|Ê\x001af0Å¨±>ä¤DT\x0010\x001d¾Çå´©FfÉ¸S3×ñ)ûí\x001c]Ôññu+\x0013¹\x001b,Ï`Ù\x0002æúrÖ\x000bt²dªÖFK¶\x0010ÚIFQç\x001aÈX¿_>f\x0001ylAy¤dëyì\x00062N/ÈÚ½dè`LÂhÏ·ZY¬û¿ã\x0017L÷?Zö?:Éq75§tu£9 çãq²è&²èLdÙ«/G\x0018\x001f o1Ìa2?\x0019Ù¦f´Â1'
XtA¯Úx4\x0012ñÇÍl¼4È7²Ñ ¿ÌkÚµ¹¤½	ëË¥ã)æéb\x0012³áb<
\x0015uTAÔF£à´¸Ð­¾øÝd8\x0019B3ô\x0001Ç`7¯3¾0èÝÄ»Í\x001cín²4\x0019B3d\x0011ayaôAÔô0Ä1ÂZ²2\x0019â\x001fô\x00143J¥(ºQáÏ9!}Ô>\x0011gÄ2\x001fb9\x0000ñq\x001a3ºö uÏ]¥qÔÆlL3ÞO6\x001fb9\x0000@Ñ\x0016@Ö\x0011ëè¦ôåx\x0008Dÿ¥3ÅÐ2Y\x0011IûeP5é¸ïR¶ÀvÍG³X&×Úêäù\x0004ãW[·ª°vÍ'³XN&KSH4K½\x000b©cd¥)U8\x001egÄ2Ìb9¬À©=»t3é\x0013·hÅÆÉo©Gî%«óÉ¬¦âPF}¼F,0êâ]6¿IDË£\x0004\x0014A³y\¢ÓçÒr\x0004rö[\x001c»Áæíoy@p¨	Ð@7ÎBtiÔ\x000em\x0015Àì&÷5y&Ö¨\x0012\x000e7ºÐBVíÀZ·^\x000ewÍ\x0007ÀòbB\x001e<èK\x000eò´¾ÍØj\x0004´%%½?k¶ß'y³\x0007Kzj(Céµ-=U.\x0006íø\x0007e¸Öp?YàÊ\x0012Nåõµã\x001c\x001c\x0005ØKI\x0002¹$Á®OËåáªÝ«\x0015Ã\x0008ÕiDØRhÞ©Z\x0003r¶Ê\x0002\x0018
¿<ÉõÓÇJ»4Ã!·\x0000°Rûäaå\x000bµÏ\x001f>?þóîO?ÿüpûûf¯WPOw\x0003/)È0ÑâV¦»ÕÿùîOo¿þúõ³D<#\x0002Z\x0011#\x0016}ºóÞkesD-3Í[ãvm!,\x0011\x0017ú';\x0011\x0013oBGó©åÚúlú!Kº1¤Üx\x0007Ì±\x0011Ý(ð\x001eT'<9M¶åíÊz\x000bb\x0010\x001d1ÆLîÓIïC\x00014l]íM9.	/E»û	Qß¼\x001b/ii¼qdÜÊØ\x0010\x0003\x000bÝ«RÍq\©y\x000elwÂ!åËwÞ\x0016\x000b2 Ö¼D\è¼îF¼è\x0005wå£\x0012Æ­ò\x0005\x000b¡wq¶ö\x000fMq©së\x001eÈ\x000cEm:r\x0019ÊYÆå¶îÄA0ñzòPTmMx\x0003#Ì`gL¨ñ½+(½Ö\x0014O×1íf[ÑÂ\x00083#\x001cùÖ2\x001aè¤\x001c/\x0015-t ¹©N¶`¼úz©ó~\x0004û~¬C!Ï£\x0013Í .PR\x0005µ+\x0012[u\x000c~b\x000cÞ\x001cJE\x0014Kî_uÌ¨Y¼UÆeBS$á£9àe\x0014KN$KÕ*\x001d\x0014v6_ÏMiþÔÉü©ù_U«§µHOËH²Ûªµ0ÖÑìdrð:aç¬õ\x0011{¯Ï1.ú[±$3# ¾\x0014°|¨¤µ´]ÆjA¬³å©fËÉ:J©(¡Éty.ËÃòd\x0004\x0011À¾t¥ÊÕ¤Û±à¥;ï	ã$L§G{!L·ûtWm²§0G'íQØ¨\x000eÑ\x000cÎÈp?!%[n'Í ¥ý^
ØòPÊNç\x001dâ%\x001d¡.ñáOÄ:|¢\\x000bS)ãôlëQÛ0ZcþdÅ,86'äQÐÌÿU\x001d3mk&îÁ¤ëÌ³x\x0014ÝhâQ¿Ý½ùüëo¿=þþûãÍðÈ\x0002)ísCª(|VJ¶O\x0013åh»þp÷æýw\x001f>¼ýá··
Ã4N¤ñ\x0010iÒA¶Ð4×bG
E,\x0012d¥Ýz±J
é\x0010jI½í	RÑw°DþV\\x0010¬\x0001b]b=D´\x0019Ñ¢\x0016©×N^ìxQ¯\x00076¡ÆiQã±Eåæ\x0005ßQºÐäu\x001a;kn_\x0019\x0006kB]är	µC¨®¤?Ýs´µ,¹¤§
b½¢\x0005bA]\%Û©rÇU\x0000yæc!Rq¢ÉUÝ\x0000pEñÓ
nZÕ&\x0005fGEôÒþ\x00031«X³>¯ùzM¼d\x001f+àZd\x0005×"+2Lõß¾Ü}ûðËï·héþãïC\x0012Ó\x001aîc\x0017Í\x001dÃjÃºæ"h!ÃTÿðñîÛ×ßþð<ox·ÕîãÕ©ª·?Þ\x0010¯hì0ðY^ßr4\x0017\x0015]úW»\x001c±þððÓÏwïýåßQ±¡¨Y;­³\x000e3Â:ä³X¿hË¹\x0012é\x000f¯¿úúíÝûï¾ýÃMUN
KR8FÚ'iI_³\x0008@Õ¤2Zm|È\x000b%i8F
:È\x0000£ýJ¤8\x0006^nÕâÛIqIÇH}{Ânï*NµMk
úõÝvÜo%KÒxtLTæ°\tTQ×«CßL¤iI\x000eò\x0010V©Ýá
.HW£fqjÝªC±æ%i>Dcx1«,\x0008hÖaWµl?\x0016XAË\x0012´\x001c\x0002ê\x0000\x001a¨\x0014Ô¼«e;[b%­KÒzâi©Buí)AÉãjAÁÕé\x0016ÐEVÙOï&ÒÔ
+[é\x0003jQF­£ø?l\x0015%ÙQg\x0017uÌGÅä!'¥\x0015´í£kÂ¬êä£ü1'ÅÝjò\x000eÌÒ­Uwª¢ú«zM¨ò¼\x0014ß\x0002¥\¨d-}¡#5¤s¶:yì¤ò¼Tä~¨üäþú_(´\x001eÂR/aûýä¥ü!7ÅB®Ieuâpý^
@)W\x000cP'7å\x000fù©È]RZû§jvXÝ(úH-ìfÔÉOùC*ÒQò¨BJÈ?\x0014ËÿÉQùCïÚMNñjoÂÁ\x0002£ \x0012¶SjVÔÉSùC®®{CÂ\x0000F){uC)À¿ÈªÂä«à¯rZs	!K¾\x0002+Áo°Õ£o'\\x0015\x001csU<ùW\x000eU\x001aíaÕ\x0019pWF×ZQçëÔ1WEÁ©\x0006\x0000T¸âèäÜ\x001e'e%<\x0015\x001c»O¡\x001f\x0012tüÞ£êè¹sÛë¬¨«c\x0017ªÍ6£
R\x001bo²Q}­:¹*8äªòEóíkî2­p{\x001ctòTpìFUÇÌtpù^´aAó?y«ãÀ\x000e:ù)8ä§²TAð\x0008uÉ©qã±z©\x0008R`rRpÈIåät(\x000cK\x0005ôõô Õ%l¿§XI'\x001f\x0005|\x0014¿ªÊN7\x0015"Íª\x00127U;­¤arQájª;rð¥¬¨é,kZp{´°\x0015uòQáÊ.\ælj"-rì¯'ÿEÜi|T8æ£òè7åþ"Gß!²ÕÕiGs~Ç\x0014E¦Néq¸Ó1|¸Ô­nb;êä¤Â1'Üè­A¯ÓÓj\x001d=\ëA\x0007Q''\x0015¥ýX£\x000e!\x0000%\x001d×ixS59©pÌI¥.8Ôò)A
ü	µ\x000eÜ­î\x0003;êä¦Â±¼\x001fñ\x0015m|ÏÒÃ\x0014ÛUM²T/\x0012¤ÉUc?~UU!Ø$b¦d\x0000ôZËvÙ\x0015uòUáXê¯¡\x001eê»h\x000bSTá¬­&
3*NÎ
Ý§ªÓSÅ¨jVC\x0019ÝE/\x0012¥âä¬ðØb?íQÏ\x0017_5z^âëãä©ð§â$\x0002\x001aôM@§Û~kE<\x0015\x001eòT9_\x001eÒhM×À"	£óóÔ!O/B\x0000¡j)>¡êLë¶\x0014jì¨§Âc×©4$ËØ¨ö¹bÑ\x0007}þ¯¸ÝccE\\x0015\x001erUYT\x001fXõÄ÷@þÍêüñE.Ó8ù)<ä§
]ö£¢)úï\x001bKº)kFü\x0014\x001eòSd0ex3\x000b¶A\x001d	ªº)ºi\x0007¼\x0014\x001eòRnTe4¼öFº\x0008£ËX^4NN*\x001erRE[æéÒ_'s\x0019Å\x0017yì<Ta\x00199}EÕh:ÂèÍ/rï|T¡`\x001a4·U[Ô¡ó\x0012ñI<T<ä¡(¨S§ï4SÒi\x001aâ¿yS:ÙL:9¨xÈA\x0015tCtBÕ\x001eóÁh¬$cú"k:×O\x001cóO¹¨â3Ç|K\x0019wµlô¶¢Nþ)\x001eôO§éâDc\ÔhËÇ\x0017¹ÆÉEÅc\x0019¿\x0002b÷¹&)H|Ü\x0003z\x0019s:y¨x,éG×\x0013QnÄ!\x0015}ÒæøíÉAfÒÉEÅcI?\x0016ÂÛ	?§FÝ©Zè\x0015ãK$|Óä£Ò±¬_rÚ\x0012\x001c]¾\x0017Ò Z]z\x0011Û&/%ý8=cQ£©0\x0014âÐ¯\x001durSébK¥ãUr	\ôýúWØîß²¢N*\x001d»JÅ<ª'\x0002+Ô\x0004õ¨{üT<U:ôc\x0019\x0011\x001d½¢­átA\x001dZWW\x001aI­¨«JÇ~,²¦5©A\x001aí	5\x000fÁ°\x0017)¢Is­ßÁ§©¤\x0006\x00009A-¤:y½%Õ_tòTéXÒHåe\x001a«Jj/Qã\¥ÓäªÒ±¤_\x001d£3\x0018µ®wj|RÏ4¹ªt0ç\x0017[þ¤Æq¨ý_;?F'O¥ü(:\x0015u¨\x0018ð\x001cþ¿¾H
U\U>òËEK}Y\x0015$+ê\x0018ò"N5O*\x001f|ªú<\x0015¹¿\²ÓAj(½ß\x0014v3 ÞÉ{ñTÁ,ö¯_~WZnKxC\\x000f~þù&oHÝ\x0000@ÍN\x0012?ôWúê`}¥þîã\x000fË]	ü/¼~÷õ×;ã\x000c\x001c\x0002Ç¢wk¨,LÔcQÞ\x0014ÖíæÇóÌ\x000f3³wím@U­Wk\x000e\x0012d\¿\x0003\x001eG®3r=Ì}É¢ÉâÊe(´.¤¸nX8Ìç½\x000fïå6J]úÃE0(k\x0007}ÊkäãÌóvÎ·sbU·îØ\x001c3Ï*Ï\x0013´Õ½Ø:ÏÛ9\x001fÞÎ	Òè¾uÚÉ*>Ú¾Nù¥çý\x000fïç\x0014Øe:á¢àãuñÅÖ¹ø«{3÷	1PéVÑ\x001b\BB\x0015QIOZq\x000e3/$
J\x001a\x001ccF'ÕîP	2u\x0016[\x0017ëK1Ö\x0019üñu\x0017\x0012ÃÈÒ	ÊÉ­\x0014#ç\x0019ùø\x0011$RPý@.n0¯Kõ\x000e3Çé\x0008ö¡
³cs\x001ecµ¢ÖC%X?3\x001dfNóÖH·F\x000699j¨1äà¥\x0002
£98\x001eÍeïÆ¶à1´¢:!N_z\x0019æ\x0010&\x000f\x0018Âa\x000fØæÇÅà·g\x0011C	:;æõé8s\x000f\x001f?fî¢ztüôÍË0\x0019/ä\x0001C¨3óñãWP*<(pF=]PgO§'Sq:~\x0001\x001f¿<2\x0014´¢c´VPÝ½ô¤Ð÷8sAðå©Â¹8¦nÅ\x0011âzPÍqæù\x000câ3Xº¶|ÛÎ:[
q\x0004\x001aë7«ãÈó\x0011Ä\x0013G0Þ\x0017a ÏÁ´5ÔÒå\x0017p¸î¬Aé¬Y\x0011ÿáñ·ß¾Ü\x000eÊÂD0\x0004kºa&pÕ2Mu]_·ÂýÃÛ\x000f\x001f>ÞWX­¢­\x001e`M ¬AçÙ±°®úéº\x001e\x001bq5N¬\x001bw\x000f«\x001f£\x0012P\x000b* `\x001c°k±°yÝØ¶ÏÃR\x00141º\x0016»
DÑ2«TÖ£B\x000eÂN;vËeìÅ¢\x0015µj¥=d}s¡éz0û1Ø³@)	<\x0002\x001b$ÉR\x001btì×´î°>\x0008:­-\x0007±\x0007N\x0014*h½\x0017Ý0$'¹îEÖ_ØÊµVr²hýA\x001c¬·C½¨ÓÁÚò\x0007{Pý\x0010¿e\x0015ä`ùvâZnô ìt°ðàÁ
~è·B@ö\x0006¼´°/\x0002»xwAyw9`_KÖ\x001a\x0001G\x0006AÁ¨aÌn=ªð\x0010¬¯Ó6ðõÐ>à7\x000bÞãV\Ù\x0005íµõÏÄ^ûha¡³ÜÁÇhÁµ\x0005eZV[ìÆà¢aQà\x001cëNÚ9\x0011\x000c\x000bëlTçeÐ\x001b_%tmqÝÇ|vÑ\x001dÌ´­=øÈÚFmh¡Í$ÍWdrÕ{\x0015\\x0017_\x001f¤w\x0002\x001cÜ	1ë¾\x0005\x001f¤ñµAµ©mý¼y\x00106Í°é\x0018lÂ1RÛE©\x001b!ëÆÒ¾H`\x0000PfÚc\x0006ÌÇ:\x0006YÐ¶¤\x000b£	oýÆ}\x000cvbàX\x0018C»\x00165\x0005r
½·wíeÂû±82\x0010Ý\x0013xVx]`Þ§«Ð¥·\x000eeg2
ûhÖ\x001e¢ÅÑ8Ê\x0015zrÄÆ¨ê_d×¬YÝÈ¤ï:cyûtN\x0013\x001fn\x0004ß\x001cF¼\x0004­mð\x0007m¤K\x0006-ç*\x0012'8um×}NÇh×·ÛÛÖÃhËà©ªE\x001cÙXÛ´\x001e$v\x0016ý\x001cÙn%û÷Ð²\x0010êGUÍô»<ÆKò±\x0017 /¸xìK´¨Zð,Ë\x0005=+ãJÐ¢°\x0016\x0010;Fæ»ØVÆ|\x0017mÖèZ¢±Áª&_\\x000bó\x001c5¶x´\x0018Ü&\x001e}ÄC$}g,QXÕn%Õ\x0017\x0006|\x0002
x\x001c:k \x000bL\x0006cCWëø^dW¬¡yg\x001cæB.mß\x001bã!§í±·vô.ñd¥Ýv÷2ì\.ZMP`]|hdöm<ÖBÂuÐayú¾yüüé§Çõn:0.q:.1Ãu=6I1¿yûþÝWo¿~\x00160LÁ\x000cH\x000eÍki\x001cÈÍB\Ù°Þ#\Ù°{\x0001/=»\x000cÎ\x0008\x0008®\x0015¬ØÓH¥xîZv/^ð¢\x0019ÏJ\x001c.w½\x0012Ç\x0007<ìýz¢\x00190NÑüòÄìd¯ø)Ï®àeÒ)\x0003\x0016´® zµó1Ävñæ\x0015LpÙWD;\x0001ý¥×\x0001}ÌVÂT´$7f
¥»vÕBÇkÎs7_ùªy\x0005]ó4­f4èè\x001cF%&^K`î%¼T\x00194Â©Ê`×&Ì¡u°2!ûÎÍ$[~í
k7a	­v\x0010ÊÂä@æÁÓáÑ\x0016vxÒÂn&3¡õ óÅSªí\x0013\x0005]\x0008VVnÌ\x001e®^ëv\x0013Îç$ÏIâyZ ëÛ\x0010$µãOú\x0011\x0008ÓúA°®\x001f\x001d±~2I\x000c8pµv'\x001eÙÍ\x0015«#Á4Z\x0014KD\x0011&à\x0016\x0010ÙäÏ\x001d\x0011¼Lñî`%¤+G¤à\x0018>\x0013½\x001ajô×^vw\x0012Æ<\x001dâ­\x0018³\x000cÌ\x00085*B,Ò7íYú\x0014`ò\x0013`òv@/\x0013\x001dBÍx!Ô%píÒ¸°ÎV_\x0012ÓmXé\x0012.ß\x0018D\x001dÇG¼v\x0015Ø	a\x0002Ì`\x0006\x000cQ\x0015§5¡T>Ë»\x0007\x0019þµr£\x00150ÌÁ\x000eí9\x0000yfÐÚlQ\x0019ð	×ó¬e²üÓH¼Ôí ß¢ªVbËk\x000c¹¦¤À\x0014/\x0014°Æ\x000bn¤ÝÔ Z\x000c¬}ÅéI·\x0011¯Î\x000bXÍ\x000b¸þ¢¥S\x0007\x001eK\x00160.\x001d\x0019w0ÏVWÌÅöýå\x0002\x0003r²4¼I	×\x001eÜv\x0013ÖÐzLX2.\x000f@/%²(âv\x0004¸n\x001e·\x0002Öi\x000fòOë\x001e,¢n\x0001H[ðHRýÈ'?q
3ÕE¹Ï²*	È¤©h_êµ7Ýó1©f;I0Ôþ\ÝìÚêzµª7á|Lªõp»R|@/\x0007¾4bÖêOÞjI5{\x0013þ\x0014B\x001e\x001e-s·Q»,+ºS÷\x0012¿£Ó¢~ç\x001c\x0014ÙHZÊS¬rkZÏü0#\x0015¢õ¬ð®¿6Ò*Öñ³\x000c%òO¤ÔÌqEhv)N¤Þ¯è?²× Ge-Kj&Ì+B³KáêT7/¤"3\x0013|Éç2]~1D\x0010í>%Hï|[Å\x0010Ä©8ýÌWÕ÷"úÕañÖÃò¿\x0001quXÌÿ
«ÓâÍ§å?\x001fqu\¼ù¸D2G¨õ¬ñMu×\x001aw\x0013®Nùª×ît\x0011ÎæÍ*Í§bDïW§ÅÛOKªRìJ®\x0005ÚÜÎÖêýâ¹¬\x001c\x0011Á
Ñ\x0015i#yÕµ\x0014I\x000e\x0017Öªî×:½v\x0003\x0015 ù8c¹\x0017¾µ'¢%»0\x0013Q\\x0011O3×ÞwÏÅzpÈ¾h\x0014ëÙEÌ+Ä#Î¯½Q`tëT\x001dl½ö\x0016½°®\x0008ÍbÑì\x001c #Xé\x0000I \x0008î\x001c\x0015\x0011V§Ù~«Z\x000eñ2\x000c<y)L\x0002w­z}7áê¬kY\x001dª\x000f\x0007F~®Ã\x0012Q¯ÍµKqz\x000f«Ã\x0002æK+¢
HV;Iz)jò¦®EáÍ«³\x0002æKR#ñÒè\x001fèBÁõ:Ý«ÃbO"Ò	\x0019;Ñ©Åòè
Ü©r0¬ÎJ0\x0015Â*bqd\x0002L\x0013ÿ(ã¬äs*\x001fVÅ\:ÀI:¹<Ç0\x0010éÞ§\x0016\x0007Ö\x0003*Ì«Ãb~óáw(]E7JÊR\x0019pçòtD´:,ÁìXè:*×ûÃ;h¼Á9Y\x001fRÀ/n4\x001d;\x0015Ýì½ä\x0017ÉÈR\x0018!e\x0004	¥Ð§«ýÖÏke\x00049©ôGÕNûr÷á÷ÛJD-~7\x000b;'o·I(yDÞTòÇ»\x000f?¼¾)@Ô¹`â\x0002\x001bXÕÑm¬å(yv5<\x000fqCÌi/W¸Ë¡\\x0004¯SZC\x0002\x00183\x0005×Wy\x000bØB\x0005?d2q\x0010ã\x0015ì¢©áÂPh^»\x000e\x000bØB®À7rõ°\x0010	ZÌâØåÜ\x000bV'°j\x0002ãÔ´O³u\x001a±hd
k\x0003b\x0000óaú>¾eÀA\x0006¾Uö2Y\x0018l=	ÜFVf²b cµ:¨\x001b J\x000f] %S2Ü\x0012YÛI\x0006óiÍxº³\x000eûLQ&¨\x0006Z¨1ëwk.éþ5ûñ/ëUûeÙF7\x001f'\x00001HÂepÆîÞ3@ÿ\\x00166\x0017Ð¼Ô~cUÞ\x0015iâ$Î1×\x0007¶Ô¨
K÷Ózé~2\x0005p:\x0016_»4h÷Ú5nCÓs¿õX¯\õ¶¥ÞßKÏúÆ\x0010ÝE\x0017k\x001aâ³x.7¼ËÝþ¢Í@}óïûô\x000bG\x001e½Î÷îûÇÏÿöûãßþþ\®{\x0005Ð5L\x000c
d¯BmXW
ôoÞ}Ë1H/ö½ûþíû?üðöïoý
ô¥Ù¡¹8í(4fm×..Hb\x001f2â\x000eñ¥ /ú\x000cÍæG¡\x0003H\x0000d:é}C@ '\x001dÓê\x001a|\x0006:LÐá0tUF\x0010\x0001Kè÷Æ Ü¸2êÇ\x0017-p}w\x001c_éRâq7³ý\x000c=BÄÒQ§: N\x000bbUhK­ÒP^j{ÀE~°A³üàQh\x0016)
Òß­­[P§iåuýäqêE³\x0019S·f³Ã\x001b$éh%úïW~HC\x00034¿É\x000bó¦\x000eg65\x001f?U¡ýÝßýi{¨øGÆÕpí#Ô¾Q{w)»ÌíÍðBýåîýãoÿÇ¯>ßô~\x0014j\x0003uÉIc{²\x001b!GÄíññîýÛ\x000foßÿé»wïå\<äß=ÀI¦XºùJú\x0018B\x001fJ9áÊ²Z8\x0017Y!æ\x000cá\x0000gÈj\x001d
×\x001eõ`'8\x0011 ô¡¦óëyÿ;g9À	E
BÍ ²/äü\x0014øÄ°mz-8v<ðÙá¢²^ò\x0010@è´ì\x0016aÛ\x0006\x00188\x00172\x000fÌÙd\x001eÌ9ë©g¡Æ,Õß\x0019ù?s\x001a3Íé\x0000&ù®"_½f}:æ7&áù\x00058ËÌy`wrC´Wô2\x0008$ø¤bq=]á\x0008g¶'ÿ´sÊ¤wÞ¬²ßï]àµZgÃç\x000c3ç\x0001«D×?\x0015õ(Qgpû¼`\x0017à3g<ÀéÇT
ú_9F\x001eu¨\x0006úU¢é\x0010f1ó\x0011LP\x001dÊR4²=Qß½1×ÓÖ\x0013\x0016¥Ø³\x001eàt8Qu2î5ø0vçÃ\x000e®©\x000fE*Ê½*e\x00197ýüp÷á×/ÿróþ
¾y×\x0005%÷vòå:>¸p-\úúõÝï>¾s3IÐUü\x0012)+÷¾õ«ld\x0015\x0017Qs\x001a© »í­iàe¶;±ã\x0001N
Ex¾ºª\x001eä¢ªS°\x001eFmâô\x0005ZVãR7Rà\x0015W,væ\x0017\x0002º½-sÒÀ½4ò\x0014Ñç¯\x001eôç÷¯\x001eh\x0019þ~\x000e':4Óé\x000c\x001aäÞGãÎ¯¢R½zlvÐ]äº.\x0015#\x001d\x0017íJe\x0015Ç\x001cÚ\x001fàµ\x00101×rÕDvºç>î¢t\x0000«·\x0002¢\x0013%1då*Ù¾¢B\x00169^¿Pì\x0004\x000c\x0013`°\x0002ò»´¨,j\x0008øa°\x0003®º1í|uâ«V>\x0016w\x0005\x0017Üö¨¤\x000c#³9¼ÿüåvÞNwæï¢\x001cËêUÔÞ
®ÞÃv-_\x0019\x0017³uáqf­¬û©¥VÉ\x0017í[þ\x0019Óò\x001c^Îïúîµ\x0003Ï»C`uiyKCí[páj`»ï¢	Ù­_4òñK¼ì>ºÈ$ÉÕD°ÏWÒD»ñâ¼ý¢yû±ò4¦\x0004·Ë3xt\x0001×ÓìÌiv\x001fÉê?#-Ù\x0018ôf\x001d!emqg	ÓLÌ[0HË<ì´Z\x000e¶áÏXg	çCb÷rÜB­\x001d\x0001:Y7ÄXFuîs6ð9Â<ïÃlÞ\x001e%oFËæµg6Ö®¬Õñì³\x001dÌf;\x0008Q.)1­¬\x0019Î.á|P²õ pÝâ\Úò¤\x001a^Jk\x000eÏ\x0004ZÏ\x0012Î\x0007%\x000f
O\x0011Bnï\x0017Â.åç>2À\x0014+ðO£±ñå\x001ez3&p\Ó·!BÖ`a­\x0013e&\è0aÌVBPÍK
·Æ«>wÑh¸UÏ\x0005\x000cav)ÁîRX¾_\x0002þ¢ó1É\x001cöö¸¸}eÚKn
©Ûìz\x0013a`É¾.WU0ªé	Ê9BY|XE­\x000fÖ³÷PåR'×\TªÇs\x000cl.U\x0008\x001aÚüdÜ<NG\x0018yJÖ¾ ÞM0¼<y×>u\x001d)¨\x0006	\x0010¡´lX+,-z}
gïwu^GúÔÆeüÏþÔô­×Ú\Ò(¶ÄWÒl?éi+>¬·¢ñ3cMÚ`
¹¨lQÔ\x000cbqþìNÄ5£}'ú±\x0013\x0013meníÒï¼Æ}d\x001dÿ²^Ç¿X£\x001c/óAè¾R´4â°ªÙëíÝGú§Õ¶\x0017.nHc!G/}\x001eëxÐ¥½<\x000cñhóEóøÛÝ_?Óàæ5:ÁS	D'¯\x0003d!UþÉùz%gøáîÍwï¿ýøöÖ\x0003{g\Ô\x0014%7×\x0014í\x0014¡¦â	2Ä\x0014}V1¼k7\x0002\x0003ãe.|[GggäÚ;ë#ÃØSèj\x0002\x000fÛ9\x000by\x0019È¹Z!\x0003O*2\x000e::QHF?Úþ]¨WÊ*öC	²\x001cLØ\x0006N6È$\x0011\x000f:\x0012õîj\x0015ÅnÈE*!§TÄ^J\x001ed&{nýÐÒii£w9§ÄÒ|r\x0002Ë"ÖËóír§ÌUw
Wj\x000cy¦ÌvJïUn}c\x0015ÊñÎRþ)éK´"°ËmËåW0Íýú?~ýåæáN%IðH¬ªô@w\x0007Õ\x0011¦+Í5ÑÕÿöÝ·Ï±\x001a±IBíy¶TåÕ'´¢ºÐÙÆ;¸¶&6ÄiÝ\x0010më¼¾Í5K[CÔ\x0017ò°.3ÅEG!Å©¡ðy2,ªgN¡ZÂÊ:%]\x0017/×kC\x0003v°Ñ©øñ\x001fK:ÿê\x001f\x0006¸,\x0013ÚøÞLGCf¡û¤Dë*Ô½l°\x001a FÑsÛ\x000côßî¾yøòù£Ê:òJOþWâ\x0019
gä)´<\x0019#×f¸ûæõÇ÷7O)¬Ü0³%gc#Ç!´|7Ñüz*:¾dT2Â]Þ»\x0019®\x0014\x001b\x001c'^eáÊ\x0010Ä\x0012uåüZ£Ï\x0008W'¸jÃ\x0002ªë³Þê0êxÜâ\x0003`ó\x0000K6þiY®K¬{ ³¨\x0011ÒEñúÌZV.x#]i5Jí»&)[AÈ\x0003n­\x0001dËqËÑ\x0006ç¤\x0008\x0003×÷\x0008\x001e-,tñÔ\x00057-\x001d8ÛÒ\x00052 ñr$¢Ðy­W µ;s$ÀÎfé¸\x000fI\x0007MÅÑå\x001bÎ\x001b{2uÐ\x0008\x0017g8Û
Ugp\x0007`\x0011	©uc\x000cZ¹¥ .O+Î6¸ñÊÞ\x0014eÔ\x0011dmý(y«Ñ@Wg:­ãÎ7'#m\ÔI¨\x0010\x0007Ý\x0013áw\x001b]ÏD6	\x000fãLPÀ^´4ëð\x001b\x001dI\x0006¸ùHdã \x001fäHä¤¥\x0000:\x0004àNm»ÙØÑØq\x001b¨ôÐ²â	à{§\x000bkI\x001a#Ý|(²ñPð4P	N(NºÁ1¨Ô­èÝpÁÏA·}X`y^\x001dSw)j,AÏ\x0004lµ¬î§\x000bÓÒõ©Ü\x0016:}£?vÞ^¹,tõD¹.MÛ.$Û¶Z¹Ñ%\x0015ô¤ ý®ú²s`\x0017\x001d{"tt;,IÊUõPÔ'$&:tSÀÎ?-t|N¡\x000e¡\x0000\x001dÀRÝh>Åæg6%\x00062'Yb'
ìDfþ­ú]ýzÐ\x000ef:[PÌUÝâ'Z±!ëÂ%8ã'pÑ\x0016ÑàÐ\x0008WõrM\x0017FÕ;òq|Ö|òÃ¦.\x0019\x000f¬Óð$P`W.i\x0000PóZ§ÚHWf:Û=§\x001dèèÅZ\x0019ACm6?wOD?\x001fXo;°\ýn\x001cXï\x0015\x000eÖÊy6¸4o»dÛvíÇ}\x0002Ü°O\x001cèfK×~L\x001dù\x00065\x0015\Òaö.å¡W±¦b
\x0000f¹\x001e\x0004nø7Uí\x0011òµéó´0\x00004\x000c\x0008kµ7££]>?7W[UL`¯aÉÚ¹ÆS\x0008ud\x000eâ\x00109\x0017	5`±\x0002òtÏ,ç#ÜËá2&Pn©¥XÎÇú#ó\x00191~äÿÌcÒöáïýMt¹\x000fù¯\x0011\x001fèT}§âÂ:Ýq­ânþÎ\x000fëïü`\x000b\ª~gÎúôFð6\x0005s\x0004Ì\x0007ÃªØz\x0017Být¹âË7ï\x001fÿùëÜL!W\x001eÏÕ¢\x0017@èÔd­iO\x000bæ%¼ö¤òýÛ?÷ñÿz\x0011/ªBÌÈ?û\x0019Zê\x000c8ÂBy¹è-ÞPëz\x0012®\x0001ZªûòÌçi\x0019§nô\x001fî¾úõñËMÂâ¼>êÖ\x0018EZ!Ä1\x001eÓ.ªÖPóÕwo?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=üí?Ó	Â\x0013û\x0001wëÓýë_f×C;Ü&ù@{¬\x0016K·òØÚ¶I ÅÅ\x000e$®Îï~^\x0017­þ=¼\x0016ü\x0014ÓzÜÇ¶Þà=ñ×ùÃä\È\x0015Ð\x0001<Töi\x0004»\x0011!\x000e*qR\ër\x001fßz÷Ã\x000fwçØ½|¾ÿ5ÿGß~{xñe\x0014âù\x001b¾ø±S\x0010ï²eá\x0011ÜIºK¢F½9Nø9!ûýòú\x0013>þ±CpSÆJÆ|ØvXô6æ\x001ft\x000bY1ÁìMRXub)\x0013í¸R(À\x0018/ãÂTIÇiKNÛÄ©-\x0015±I2Ä\x0019¸ðçV¬ãt%§kã\x000c\x0018
Kàså\x0001M=ÓXu`[ÖrúÓ·}wÄ[\x0013x¾\x0018½êbëA\x000ebëM¡ä\x000cMÏÍa´\x0008\x000e\x0005)Ã§(AQ|\x0013g,9c\x000b§)K8\x0003G\x001b¼R]¤\x0006\x0016­âäÿï\x0013K;\x001a@}*[Ì\x0019KV±>~PÈßÄ){²Ó¤ìR+À\x0019¹ÂógA\x0000Tõ@UÛz.\>E®t\x000büáÕzÃ${^¶Yz!¸&\x0014Oå(ãOxh°\x0003¶#\x001f©ô\x00125¶%PÛ\x001dyiÌ
PÉ-\x0013û\x001fô':½Ì,\x0012ðpÿ÷y?D+
ZÅ\x000e\x0012v¢æï/Sêhf\x0016\x0008¸8ÿ×ãØªÄVk°U\x0012LÍÜ*øPT3þ§äÖ%·^Ã-]ÑÜÂtë-©É\x0002Ä\x0013rÛ¬àÆp´÷Äæ\x0003å0\x000cÑlhháv%·[Ã\x001db\x0012ÉIÜitXæV\x0014f4&L×p[iûÇ\x0012~0þû}{}¹ß½þm\x0016Ø{\x0013o\x001eÞ°\x001a	°¹\x0016:¨AÒ»7\x0013ûÓÝÍùöî_ê\x0012T7º4¦==`à\x0001o8£p\x0018vÎ\x0010ê O\x0000jJPÓ\x0002éÝ\x001cCÁÁ¬ÂdN\x001b\x001d¿´N@iKJÛ¶ÒÑÂsE¼A\x0001\x0006ZMgNÁéJN×º?5Z©¼?%'Í Ö\x0006êKPß¶ =0:¼¢AãÐUl\x0002
%hh[QË¾7ö\x001dPO;ö5ñ§\x001f4C´Æ\x001246Â\x000bº"¤Ö\x000c*¹§MÈ\x0013ìÐý\x001b!YPÑ¶ É\x001c¥\x00051Ï0À\x0005õÔ3ÒO@Ú·õmÆ\x001e¥}óº\x00141Ë[ìñ'8KûWB\x0002UmKª¸HîÝÄÔkIß~øLh"íÝJ²ñZ¢3\x001f¸¨\x0007\x0016»ð\x001b4v´aöî$Ùt)yL\x000fÑòX$
Lê\x0007ñëÆOÿç\x001f\x0007\x001fÿÇ&ØÈnÒÙ\x000eVJÓíÓS,«üói\x0014py¨ð'mçÊ\x00110F	\x0002\x001f,^]£N`û¥\x001e\x0001ëV`/¸Ü
»\x0015V¡\x0003>Á\x0015 \x0007»¡m3däOaAcS@Ö5x
¿Oþy×gÝµÞ\x0004Ä
þà«5°ïçÂiNÙnpÊ`±W)o\x0001\x0013p.\x000c\x001d2¾\x000cô)L,¬ëçþº~nÜ®2³
Ô"ç= é\x0012á=x\x0012Ö/}Ö/M¬>÷úT È\x0016(*ô>\x000e4SêXÿ?æÞ-ÉÜÈûÜJn`h;\x001c\x0017ë'\x0016*ÑEVó"ëo^dY¥4f\x0014KÍ"Ûú§ÞFï`fg\x0007½^É¸\x0007Üq\x0002çd\x0006\x0010§eÕýP¬£ô\x0013\x0002~\x0001àþwÓãkÙèñtÌäêî/ª¡ÿÔ³\x0019Vë£fvP¢éDøÖ\x001d·Ê3UÄLÞ¬¯Úùòö$,¬aa\x0012}¬U\x0018\x0017_\x0007FhnÑõ÷S´¸¦ÅIZ©yÑÎwWêÀJ¦Å­óÝ?¬u¢¥5-ÍÑ\x000fÏTã\x0002¬¦|Ó¸ðÛÇÁiØ¸°.4u\x0013¯ÊL\x001b¦@ºÒ>HkØ4	+2*y\x0011PSnâ@\x001bM>d«¶3K×´y6èó¦\x0014\x0002è3\x0017Ó6I\x0016\x0017¯´\x0011Ê¶LÒF°¬Kdnê\x001d!A°\x0008Á½
íé¸8[7M²#,·âBÓ»9Ó^2ÛÇÉà\x00109ÐêÙ\x0006SÔ\x000eB\x000fz\x0004cðëØï¢\x000c\x000fÑ9ik«!·ÍPáB|Øý4Û\x0007?\x0019\x001fb}­«[ô¶E±Í Ã­Ä­å\x000eX»àà'£ÃRQ«k8~=«.\x000cSÛ·¸\x0013õÉí¢\x000c\x000fm\x000bueÅAT\x001fdÝÍ°mÁÆí<®t¹RcN3¬c£½Ò¶í<®t¹°³lR\x0007ì\x0014=4ÈpÔ«àBçraÒåFÑïÖTA\x001eÈ¡âzlu\x001föåNÑv>\x0001&}\x0008\x000b»z(\x000f.\x000b£&¢\x0003É_ÇãBç\x0016`Ò-d gEû\x0011E±\x001eøg[Ü×Iq¡KÄ`2\x0013ËÐPÝ\x000b¡ÊZ.¸%\x0019nñ×Ém ³4´´\x001cZ\x001bd\x001ef]Ýè¢u{ú3Mï3¸ØY\x001aNZZæ«³!
vÅ G\x0008p\\x000c»ä\x0006'LÑ²¼É§E°:>+\x001d}±Knp2¹É1éùL¦lhæ\x00181\x001a-^)·Áþè;ëÇD©n]NoUl@²\x0008õc¶:Ø³¸cÀIÇ z\x0003*/Á×bZjøÒls\x001dÜ.aÀÉA$0ôÆé­tUÔZg»\x001cÇ­ñ,mçÆpÒIMALº¸^oyqlq¯äuCçÆÂ¤\x001b+)Öö\x0010ÆM õ½].k\x001d)Cç\x0017Â¤_\x0002\x0003Ý
Ùé³Tx£½Ò^\x0008¡£
S´|Bk=Þ$bê\x00157nn¸×ñ\x000b¡;H¹DtÒ¡©¸ÅÛ=Sn¢r\x0001ÓöBçÆÂ¬\x001b+y×¹à¢>éðßDscX®´\x0019:7\x0016æÜXAF®z]i5\
KWJ\x0018BçÇÂ\x001fãÍ\x0000µþq¥}B÷>@ÈÈëÐRçÆhÎE©QKã¦-nÒ¾2\x0019÷x\x001d¯+Oë&OjË\x0015Óâðv@=X6ß°û0ñø}\x0008^£\x0014÷çIÜbÝ*0&ÅmzËÅíËÈÂýó\x0006÷ÏsÇv>û\x0014¯g¬5iË\x0000\x0010ÃÍGp]Þ¼Iñ\x000fö&õúoÿözLô¹]¦\x0002Ò(Í?rðÑæ\x001fF[éõ\x000f|T7¦qÁ\x000bF¸DÕ7®*«\x001då¶¹q=\·ý\¸æÂ!®d¡Iäv®\x0017&ãrgÞ@ös5W\x0018á\x0012q]SÂtÚ~\x0012]3\x000bN^\x001f^qïç¢5\x0017
­\x0013Mâ* µ\x001d*Ê4åÊù\x0008WZs¥!.°C~
 ºq\x0019\x0010\¹\x001eÌ°\x0018âÊk®<ô\x001d­}¬ê\x0011ëþ\x0002
¥D\x000f½ñ~®²æ*ö¨é¹èü¢­WÓIwÓ\«~¡|zæÙ¹`ÙîEE ¹
8óÙþsß±Ö%ÐiIµï\x0003\x0005ûÏ÷ÿöñþË\x0013êaA;\x0017Eo\x0004UC\x0017SÑlÖ£ÉéÜ¾¾ýã2ÉîIØÜÁ>íØ\x0007+\x0013U¿3)l\x0004Ó,ÚÎn
\x001b\x001fh^ì1³T\x001a,ÖV\x0004d?\x0005\x001fSrÙ\x000f\x001dì\x0003¢}°¹MY^x
ÖÊý\x001fÓ¯ÚO\x001a:Ò\x0007ÒDûö\x0000\x0016sj¤¹Î¸JÐ{L@d?,u°\x000fôöÁâIÈ&©Ë+\x000e
\x001b6lS¬p*ûÙ+oXdÞtõRr¤
Ð¬M·Á4p¶aã5\x001f\x000có%½ÎÈ|­×\x0019ý	Xús²Cx¸ÆÃa¼b\x001d(\x001d®^lò\x0018ÏÜ\x0013\x000eá5^\x0018Å;
\x0011`¯.]_\x000b_
ÖSáè×¥5\x001f
ó%ëä(-F2\x001fé}J\x0012äc|qÍ\x0017GùDpN­\x0003\x0016ñ¢/cÓÈG·_Zó¥a¾ÐÖ/\x0004k_ù­_<w79Ä×|yOâ î¿`³\x0012Ó2!±ò±s<ÈWÖ|eÏÄ]MqMølýÒÑõ[%aU'´\x001f0\x0000JÉp\x0006s0ñ\-À\x0010`\x001f>ãG¡¦"Í'\x0017P\x000b.Å<L>w­4\x0004ØÅ\x000f?\x0018@dpU\x000c.ø¤\x000feÉûf"Ù\x001f4aß¹h?è£eü|\x0003ÌNÓ¯äÁC\x001e´¿ï\x0007´ÀüC?}WºW?ß¼ÿåÛãR,\x0014V59i2C.·
\x001aòçÛjÛêë÷o><"ZÛHqMS¤\x0018ª:\x0003¤#GÉ¥d\x0015[õ9Ð°\x0006
s M#·Z	\x0017m\x0001ä\x000bÍl¤qM\x001a§HU$(D\x0012g´`Vt\x0000þ|¯Å f^cæ)L×M(¨UöäÀ\\x0011x¾EhôäÑtÝ\x001e¸\x001fUÎZ\x001aAmªHdé·Ç¸ÕCí\x000cßOY>æ&1Nl\x0010Ú¢¬h/÷çû\x0006Q;òS\x0016\x001cÂu.#\x0011gkU\x0004-ÙÌà.ô/\x000f¦4M&Ò¦Kâ´²ÞRLB\x0006ÓvÛAÒÒ¹5õµ}IÖ4V}þP¢Ý®\x0005\x0007×XSð]òS¤Pªk}JVRö4\x000bt
?uª[Hi4Ø\x0015\x0017±5^\x0016Jöè.´~þuo nuoà\x0000±kE\x001côÅÚlU\N¦éWÎ70õÄ\x0017^¶pÛ¾õ\x001eÃæ²ïxÜ\x0014Åº \x0011õºJd¢\x0007å:6ý©'MÜ¶ÿ`½#\x0018@§9oÎËxêåÝµXþI\x000f®\x0008\x0006ÙÂ-±b%o\x0019ISO*H&°G\x001b\x0001äQ6Z³Ñàºe¹®×çª²ÅËf·çi#\x0015<J\x0016×dqÌ^,¯\x001a%\x001b¬[¤\x0001¹®ZÚ¾´
²å5[\x001ecãLR_ù3ÌLT·ÕÙ¥mè ZY£±\x000f*\x0003#ë÷ÌAû`¥Ð®½çn«¾ÆÐV
9¨\x0007íeã\Ü\x0014È\x0010\x0003I±ÝCmû\x0019\x0006ázß6èÜJ|¦FêlÆ\x000bµ\x00014\x0011AG\x0006cË\x0016Ú\x0010Æ,¡6 ÏÖÛªÎA¸Îïú1Çë½3y\x0003©óÖÒù\x0012¬/A
x\x000eÁu×y^ÏQÁÄ8Q¤{ëÛ \x001d§óêÝA¶Îñú1Ï+ê\x001aÚ\x0002S°./\x001b\x0000\x0017\x000b\x001eòn¾ó¼~Ìõ¤Ku¨¢ÈEÖ¦ï(\x0003\x0016uÝò¶ m\x0010.upiØ¾\x0005È`°dNÄ.ý¶Sr\x0010®\x000b~,0ÈÙ¨æñ\x001e$
©e\x0018\x0012á+\Éù\x0018\\x0017\x0019üXh\x0010iZ\x001dU/¯(z\x0015Rr{¥8äâ \x000c0\x0016\x0019LR¯j´ò[ûá#Fm\x0011AïE\x0006è\\x001c\x000cº8N? eÑJêÈ	Iåºíô´A¸ÎÀ \x001b©åÇÕÅ%mº\x000e­1\x0007wÈ@g«0h«R¬§pl\x0019:\x0017\x000f\x000cºå2\x001d\¹Î\x001c`Ì\x001cÀSçO-1ËÁ>kLö\x001cvÙ\x0008e#ÀÇlu$"[t8'6Ò!GýYkÌ   ¦æ@'p|(¶r9\x001dú¬Ø\x0019\x0004\x0019\x0004\x001fZô±Îl­ugßg
¹\x001c\¹Î pÌ  \x001e\x001c¼É¥\x001aYíB²¸m\x001dþ [g\x000f8h\x000f9kË¦?)EßJ\x000b\x001cú¨¡30f\x000eè Êtß¢eIì^¬ìóôCGèÐC\x00183\x0007ÞSæH|\x0004+AVKX\x001eÿ\x001cëÌ!\x0003½{±}:=ªrFb\x0017Ë|¢8t1\x0012º-\x0017Æ¶t2«#\x0001 \x0011\x001aZÂ¾]x!\x001f7\x000f­\x001cu{ÆöTÃ;ÍåBQ\x0001\x0011>\x0007ª±"ÿ»\x000e9\x0012êö\x001cí¹ \x0013Zj¾\x0004¨³×"&\x000bA÷@7f-u\x000b\x0006\x0017î-tblj¯òËÈÆ\x000bÖaä}"\x000b¯\x0010¢ù­|à^F\x0017ó¦Z\x0003Ðiù¾Ý¼ûúÄd\x0000"·¤"\x0016WK0¥»L+Ú\x001e\x0008\x0013T¶\x000f7ïÞË|'Ù`Í\x0006cl\x000cd3è¤"¸NÂ%\x0015ÂÉû¶Üv
×l8Æ\x0016rU®J@¯£hP$·[%àÙ}·Öl4¸n©>ì\x000b[U¦&S`°³A7WZs¥!.	]QK=\x0001dÄ*,c§´4sàC[mU#fàÆØdÕM'½öÂè³ÙÁvNã(\·×üØfùaúAÁ\x0007íÂªæò\x0018\·ÙüØn\x0013	4ªÒó^îoê$=ÉÄIÊ1\x0007â»
çÇv\Xôl\x0018ùYÁ¢\x000eá8Mãv¬\x000c$äuÕËÂêw³Ì\x0002çàü\x0013Ò^8èb\x0002\x0005\x0000XÅj8]\x0013)a-sN^GåíôQ¸Î\x0018`Ì\x0018(Z*ïú¤ñ2\x0002±n8Wø\x0008®3\x0006\x00183\x0006J(À\x0005.%hlçßÞö¢Î\x0016Â¨-øa²9dÒ%Ì¦¯êc8{âÚËF5Ð5`IÏlvuÔ»B\
kd p(ÆÎ\x0018â1 <öVKå#\x0018í\x0012\x0019
Ù´Äxþ¿?CZg5KZ%û¸ò¬h`MZ$ÃyRnyÒVqnðëýP~\x0018!,®5ND'\x0019çh\x0012\x0006fºC\x001eÅùí"úñEm26¯'é"ZÃ\x000cl«Öw\x0002ÛTBð\x000fëJ_oûéîñy"\x0013¥Ã;(GÕD\x001e\x0019#8o»·ïnøîù»§é`M\x0007ctìD,­K\x0014µ\x001a\x0002·\x000c`;g`\x0018\x000e×p8¸tØ\x0006µDI?vì¨×£xá*g7\XÃÁ#½±æã,Ê¢EÐ§/Üù8».®éâ\x0018])±.ûøLG!¡&\x0001>!¿>Ü
×py\x0010ó'm\x001bËòÇ
çOpîüuún¸²+ßU«EDësÇl-\x0012>æ\x000bï­{éVõª®/ØµvÓùêé\x0016q7ý²IË\x000f|
\x0017Ê6vãõÎnÐÛ±\x0005Ôö5^½DúT­#ï±Oë;â\x0007\x001d
qÐUöÆ\x0012vkúi&»Õî\x001b£\x000e\x0006áN9^\x00115Wá¯l_öBÍÜnºÔÑ¥Q¥zç/û\x000eÛû&ïðÂíðn¼Îhý Õr°°\x0019jY¦×Õ\x0012NGÞðÂÊ¹½xÐ\x0005\x000cEÃN½qÊÁÞ^¼&*^¼P\x0007¶\x001b¯³\x000b\x0018´\x000b6\x0007Ëð¤JMñ è3ÏîOÎ0`Ð0²\x000cô­w\x0001)-vìm.²§cÁ\x000c:ËAËÈR=\\x0017¯³­Í2òA»Î0`Ð0rv\x0002*R/QGH Iíú|á|±\x001b\x000f»$
\x0007³¨¹yñ\x0008,x±ÑùcÉqèS¼A:iç\x0004\x001d¼\x0017³Í´\x0008År¼\x000e\x0006ÛÐåxa,É#%uçe«¾
Ô\x0006Gæ|¡Pg7^åÁ4o)Q<©FÌg\x0001-çm3ç \x001eu\x0014eRÿó«çÂIÉª\x001e0~\x001eL\x0008bíc¯ìL\x0000UækZ¶ráulï§ï§á%h2UìÖ½d°!*þBUÌ\x0000ß{¾?ñI³xjÙ^}ÐÆLG#ù­\x0012Íp2Ú5tÔtý¾¸Ò£~å¨Çhõ
õáÁcd8M"ª«x7Æ´úTV±JÔvX^Å­^Ô^@ÂíT¤î\x0005ôÇOwoþüßÿñ·wß\x001e5å"Cr´e\x0017Àú\x0013Ùl¯®|õüõÍïnnx\x0013Ö0Ã\x0013Ö»>áD\x0015÷ \x0018L\x00179/\öpâ\x0013§ÖÝ5T4R­ÿL&ÃÍÍ\x000bo·#a\x0019¦³êÅ×å´º\x000b©§±r÷p¾)eÖ4Á)\x0005 &Q\x001dN({Ó\x0016ãqÍ\x0019§Ö3
É,"ý©ëéLà\x000fQWàLkÎ4gFþ'ÝhR\x0011­_/ÁVés3¯9ó\x0014'\x00069(WµÖÅrjJtþh0ÆYÖå7»¾wóS~þ\x001f\x0003ÚùO?å@ÿ1 gò3®é\x001f\x0004Ú¼ÿíÚ¼ïlÉÿv	:cß®1AgLðÛ5&è	~»ÆÔ?9×T´{-ÝP45òìO
ÔÙô\x0019"\x001eÁu!,ëºÒûâõtßÍ÷÷_þv÷ñóýÍ«»¯w>ÝùxóÝý7þËÇ\x000c\x00021ùªeTHóðAÓ\x0002j¤\x0007z7ßß¾ýáùË×"ã÷^$ýÞ¾¼½ùîö\x0003ÿåíÓô¹£Ï\x0007écl
i_ÕR°ÚÌäD\x001bm¦£ø§¹1î >\x0015YÀÎÓ)Ùô6þ×¯»øè;z|ëD;{EÕªäÅ7}í\x00146½±ñ±ÃÇã{Gg\x0015\x001fõ¢Töm}ÜÜ¶\x001cÆ§\x000eî\x001d\x0019Jg²të´\x0003úV´è0}êèÓAúPê-µ,~0ÙÆxJä·÷\x000bñK_\x000eâ¼ë¼ua%ù(_®»õCg¹á¨åBÒ!Ø\x000fTU\x00159-Ýâê5ñÊôá£h
\x0010%èÆ±ê.	X\x000ft±wV\x001bZ-o\x001cÓ\x0013Nyã\x001eIJñÊøÙÃf&§²èÂêÎÉÍëlµ\x0010\x000fãwf\x001b-§8¹é\x0010RRúh·p\x001e¨\x001f¢§Îjé¨Õ\x0012©JÆ2õFéÉdï¯µu¢ï¯¥dtÝôsá?ðÿ_ïþò¸x¦4Ðz\x0015Å¦\x001f\x0015g>É]jÊuó\x0007fùþù÷Ö;úþVHqÔ;´\x001bZþ;»ú,Á¶6]xZ\x001b\x0003kÐ8\x0007\x001aboLh\x0013J1Å^ÚªnÏ¦5i#\x00159µjo± 
UÊ)#ÅK-C¤yMçHcók1åTÒ&Æ\x0004THË´Ì\x0016N7Tk+J\x000eR»úMäÂù¦1Ðuïï\x0006HsTu\x0004þú®k	¦þI°\x001d¿3Ú;©9/\x0005 S,¼·±\x001fÞÙ\x0010Oz0åj³sQ~ÎG¡#;²$\x0008z¿\x0010Ái\x000f\x000f\x0010åk RJs¨\x0004§¡%v>Yõ>Ó¦AÔÎKù97%çO\x0014l¾
Z³\x001bð¢^\x0010£\x0018BíßÏY\x0010	tÝ«Qµ/:Ûü¸è¶óãfP¡33ioÄ¨fMn\x0001ÐDe:ù\x0015P¡CÉUµ\x001cN\x00068\x0005ÓqÁ\x001cÛ\x0000§\x000båpc¨\x00079\x000f\x0010rÓ~NÅk£t\x000c2ßÎyB
\x001djC`)y½»ÁeÛªþlÄ\x0010iç«`ÎWé0ä*ÜG:u=ENd®\x0010ý¡Ëý`.ù\x000b©}¥\x001a¼C\x0001l¶{t×ØªØ9\x0000s\x0000²U5\x0000d¯ªÊ²S©©!^\x0001´33Îì ¤ÅÒÔ\x0010OsøÎ7;
¢v6s6E\x0000z\x0004\ê¯j\x001a²iØD¸\x0006hgR8gRÆðQ/j¥Ý\x0012\x0015ôØÎ\x0010igQ8gQm>ov6u÷	îE¸FN]¢sJLÅôô¥\x0008Ù\x00165Ûa:íäã)Ôî<s\x0007*N 4¥wú6°èÛKØ\x0015²?ìR*K©\x0012óÄØn¢«fdçjO\x0008Wøþ¡ó¨aÎ£JacÐQQàjW\¦ìÕ5
¤¿H»\x0003U;PIÀ·E\x0005\x001b½\x001a\x0005Û®§Îû9ïÏg;¦fWQEDìXW.ó¡vÉ_KþRÎµó@îí¾vn¾i;,x
´\x000bSa.LEH6æ:\x0007\x001bÑÎ¿¶Üï¢ÄÏ\x0010jçþÃûEéð,	kPz
TÛé>S¨û\x000fsî?CËý*­>õT]Òvë\x0014jçþÃûçH$7¨5ReKþGÛ\x0000e;Úx
µóÿaÎÿKzú\x0018¬_&\x0016t6*_ãú:¯Js^u©\x001cVÔâLû±\x0018êvÐÓ\x0014jçUiÎ«¦\x0004mªèÝªÿ/­,ûøè\x0010içTiÎ©P«£6 \x000f	UûpT:·Jsn5ÉGÏ§¨Jêÿ¡Íê;/á3Úåÿ4ÿª\x0014Þyz¦SûÈ¾óZe¤]\x0000 ¹\x0000À\x001eÊ\x001e)
ªÐE\Äq­è\x001a;µóÿ4çÿ|Ò5Eh£\x001aeª×8¥RçýiÎûgQ­iÄ\x001a§
¥öH|:çOSÎ?9>\x00045þú<¼OmI¯q\x0016»ä?Î%ÿÅái\x0012\x0001´þ²ªÉSÒUn©c\x0017§âTJ\x0013\x0015U\x0015éiu©>X][\x0017ä(ÆP»8\x0015çâÔ2ÒVë\x001fSÒ>'	©mvâU6@\x0017¨âT bï	¦*\x001a¡Ë&+VËé\x001a®?vQ*ÎE)i¶I#\x0019TÜHf@¶*p³ì¢TRI*ÕïäµrIS\x00128{J¿<la\x0008µô\x000bS2üÖÎ~\x0006Ô<¦Xì¿Nî\x0017»8\x0015§âT\x0012uí¤Ì\x001e´@!\x0001Ù^-~;p{
µTq.RI
M?.Å6£û]£@!v*ÎE*Ï\x0011¿V(ð¢fUöMÚæ+|þÔ\x0005ª4\x0019¨r°Ï/©_
ÿ2±9¶Üï
'êÔ\x0005ª4\x0017¨<»Ô¤\x0002Ý\x001c³b
TØî~\x000b\\x001aR3Ú\x0005ª4\x0015¨¤°WôÀédð-Q¹ ´3FÚÅ©4\x0017§<¢ë\x0000\x001b¯st\x0013¢krñ&&
v*ME*öÑlÊñ)P\x001d'{LËWÉýS\x0017©Ò\¤ò\x0005Úd\x0005B-PJH\x0016©ø\x0014{
ûï"UTì=R=çhfTRÛTx¾çu\x0010µ¯OT 2ÇºªÉÙpyLæªø\x0014{
Ô.R¥©HÅ©Jy¦[5Ì+ó·J¾FJºHæ"\x0015×ÞlQb¶",®Ía:ßë>»P§BU\x0001j:\x0012DFÐÕ»ÿ\x0004mÎa.\x0017Ä\x001aÇP»PçB\x0015 ·¨
®Ø÷àôñ\x0007"Øã¨]¨Ês¡Jf]EÝ\x0000ª5îÐæ¬\\x001aA0\x0004ÚEª<\x0017© 8½P_F`Ôûóº¦þ\x001a¯T¹\x000bUy.TÉ4= s\x001dªIAË¨áøä\x0018h\x0017¨ò\ \x0002\x0017t`\x0007:ÿh;Â5Bjîtþ2\x0015Kgð¦`2ËèðÒhØ!ÔÎ¥æI*¯éÕûË\x001fµOPÉmU¯\x0011RKç§Ê¤öêe`T(6.
\x001b"íÜTsSÀÙ)Úè |¦W*GkRè\x001aÿÒ9ª2é¨ä9]¿¿\x0014~è÷'²Y=Ä\x000eÇP;GUæ\x001c\x0015 SA\x001eþIËi8NµDõòá\x0018jçªÊ¤«âJ\x0007Ñ ê^UuzäÓð\x0015éRê2RÌà¨g*öù:¯4\x0005\x0008ê®q¦*W-s^UJÔ]õÿè½Vý§P²\x0005rPUººÌ¥Ô|hz¦ª8­úM!§Jx\x0005÷_ú9÷>é\x0013µÌ«ÑrDv£Þ]£;Å§^4~©§ïf;
Ô~Ê´i-T\x0014õøz­ÞfBt×¸X#Ú\x0012óÑ$±¼©ØÐGð:\x000eO]Î®\x0002á\x001a\x0015\x000búÙ\x0001K{ÅjxÀX}lÕ²Atº\»hÉGW!Þîé5F\x0019¬Ùj\x0002u\x0004´J+<?äe'pt¢æáOMVüÃ?ÉßþÓ¿Þÿíãga}÷õîo\x001f??ñÎnsµSÆPtÒ\x0014
VP\x00176÷×/þÀz- ï¿þæÃË×M@ØjôA§ÑwÿëÍw¿üú¯ßî¿>*"(\x0017öp%£L´\x0010<µ9 H\x0017Þ\x0003ÞÝ|÷æÝ?¸}ÿÐáV\x000f:}¾ÝLD8ÃöZ\x0005\x0002V¯\x0012¤Úì(#®\x0019qQ\x000b*e\x0002¶ý¥dýTx)\x0005\x0018\x0001\x000ckÀ0\x000c97Eë ¥zôEæÐi[ê%¥æý´&¤qB>äk\x0005uôZFÖ;\x0011èÂÅä\x0008`\\x0003ÆqÀD¦\x001a\x0017åòL\x001fy]ó¿é0¦5cXD0%\x001b\x000eÖ.ÉnÍá]G\x0019ó13têè6)¼4s¡ËÊ×û\x0019Ë±3"j×I\x000c¤×\x000f\x000cnA1\x000b#¹\x0007\x0010OÝ±ëvÃ´¦µq¢NÀdn
'22ù0d\x001f_Æ\x0003L\x000eùÚ\x000c=«\x0015E\x000e	êw.I%ïGìÂ\x001f/%4QUé1Í­t¯õ^¸l\x001aìâ\x001f\x000f0\x0019£(a/\x000bÉAÐöµ\x0017ráq\x0004²1~<ÈH¹^Ò\x0016(y\x0013Õö\x0012Fùâ°ý]ñ\x0013q&fU­Ùë!8\x0016´Çzêâû\x0019;/î'Ü¸\x000c¸±P\x0013­í¹\x001d|È_Ð»\x0018ì\¤ð¹©ÒJ¡6h}5\x0012\x0010^hÌ\x001f`ÎýÀ¸û)\x0012\x000f[S¾Õeµj7Î'\x000flèL\x001bÆM»8\x0013dI>Ø2æ`\x0019]\x001c¦µ\x001f±³\x0019\x0018·\x0019©\x0013FkÃG¹D®¡ÆÚ\x001bÎ«c\x000f!v&\x0003ã&S\x0002ZeSbn58h\x000fF/sÛ\x000fÙ\x000cLa»Nv¡v\x0003ç(µ\x0016ñtØcg38a3\x0019¬!åhw¯Îì:úãvýqkÂfJv°ÚnTÀ\x000fÜ_¼\x0004\x0018ì¬\x0006'¬Fkµ}E\x0014¯P+­-ùý0
y3\x0002èÔ~ÿËç¯÷?~úôè-\x0005Éëå"°2úX\x000b×CF\x001dsÀÿ©^Z~ÿæõûÛ×/_½zäÂ a
	\x0013r_Y\x001ad#!
òÂÍå\x0008$®!q\x0006ÒÛ\x000c]FRQ6V9L:ëF(Ã2Súv+\x0005Åºÿ\x0002{#£¼4YrÖ4A©AfÕùúNÅÿ¾k Æ5b@¤,Êu\x000b¥
QH¨ÇÞãR}ò\x0008dZC¦	HlwRïQ\x000f²Aº*%äK\x0005#yM'(«\x0003k2ð	¢>Lä}o<?a\x000c²¬!Ë\x0004¤\x0007+}!=Ü\x0004yªÖ¥L43\x0006(}ïÎ'ü¹M\x0007ÅÌE
S*&¢a\x001eìÜ¹ðç.×:\x0014Ùh³Ï"j`ä]¹òîËÏ÷¿Ø9s?áÍ]Ñ¢>^ÇTä`a$ÍË\x001d\j=\x001cYÈÎû	oîNNÈËÜÛ:++JÆ_)Ã¡¨C7÷\x0013îóf;	Tp?¸\x000efÜK}'#G÷\x0013.sçZÉË¨äb2ÓóckÆ(;î'|º\x0013ÉÔê.}ô:Ø=D¯ÅQîbaü\x0008eçÒýOwnéY(9{Ó<ìÅ»Ô\x0010=Ù9u?áÕ\x001d[MD5 lîÒ¡yu¼0,m\x0004ó¤¶ä¿î7ºÐ\x0005\x001f	>.×¦­äðSeAN*¦ÛJãNaö§ðó\x000fYÍ.\x0004ÁL\x0008"\x001d¥ZK\x0010äÜcJKF(»\x0010\x00043!è\x001f²]\x0008\x0010$¢\x001a¸êsòjêbúr\x0008\x0004]\x0004\x0008ô\x000fYÌ.\x0004ÁL\x0008r©JH$iw·é°Zôæ.¶Pv!\x0008~«!\x0008;ß¿UßÓÄßªÓÄþ\x0012fÜi\x0006yÍÓ«"\x0017Qï\x0003GtM5=]jp\x001fÁì¼&{Í '*¦/ú\x0008\x001e0Y¤ôWH5±s8î4C\x0016hl6B»DhÇsMì¼&{Í\x001d=Ó¬\x0003£\x00161\x0005H:\x001eq\x0011#;\x000cÙùL\x001c÷!G-fÜÈ«B\x001c\x001fÏR±Üè
ÏÄqùXÊ~PV½\x0011îJ\x0001÷&%Ú	½ö2\x00071{»o½T#<tM¸s°Aõ¡ê¦ZRòæ=1\x001c	6\x0001ü<\x0006XÉâ·?~¼ÿöï7?üòíÓÇÏ:\}ü	ÁÇP¯@bûÙªÅ\x000f7|yûá_n~xóáÕË×O£Â\x001a\x0015æPãÒ\x0016¶ÔÝ	kE5u8,\x001beàYÒ°&
s¤èäîµY\x0016m\x0012áàZ%^5­YÓ\x0014kÔJ$uR\x001e&mqs4\x000b× y
\x0019uæ\x001c=\x0001\x0012D½ú²Ðx\x0015Ô²F-skÉf\x0011x\x0011\x000bYÕ^Ùà«d=Õ-\x000eÀÍ­k Ó±¦l*2´a~ÁóË£°½·sWÑén\x0011=I ®lÞHMÂB·²0·²ÈûÔ[5\x001c©s
%y\x0013³ßª¯ÌÂv[\x0016æö,',&\x0013Ë~JÏxt_
p\x0015OÝ.À¹]\x0010¢µ\x000b9\x0012={eõÚÙ(·àWñ¯§ãÉ\x0002s°hr!Rø¡\x001dCäÍ³	Û
´QXçc\x001fbåjMöù¿Ýó?µÔ/üp÷åëÿþòhùB\x0008ä´3Äs:¨»O(Ú-~ó
ûü·¯?Ôò\x001f¿}ÿ¿Þ>R½`a\x0018Æ\x0011sÒÞ+ùìu\x0015fÔJbþ?w\x001c1®\x0011ã0¢h­kÇ½h\x0004×,\x0015s*Æ\x00186×õ\x0013'·/âö\x0007!#¢\x0016nò\x000ej
\x001a\x001bºê¬"æí4¼	Æn7úñí\x0018¥{±nÇ(3ïêu(\x001fHl?n:\x0004f\x0018»íèÇ÷cVÚÎA¥U\x0014\x001aãv.ß\x0004$u4\x000cY
X\x001bp¦(çûå$k?
ÆÞaÈÎjü¸ÙDéªÔ\x001d¢Ö;ó?®Be\x0018Ü¦Rn\x00062wy\x00182«G\x000c)ÂoõJÌcÔæÏàÓaÛÎ¶aÜ¶äº'yQë¸ÂàÉüxØ¾\x0017Î@ö¡fÜ¸ôMVã"ØPoíÀ­dÃ\x001b:ëqëÎÏBÕùI\x0001µ\x0011Á´l\x0001CÜ(gÏ@v\x0003ã#¥ã¹\x0011¦¸\x0008S-×L&\x001b\x0019â\x0019ÄÎl`Ül¤(;ê:\x0016§)Ï@ªCAÛËÏ	HìÌ\x0006ÇÍ¦x;\x0005y\x0019èQÅ\x0012\x0002f à\x0003\x0011\x001cìÌ\x0006ÇÍF­ëJJó®¾^\x0007Ô+0$<¾Õà¸ÕpÈ¾\x0011LÇ\x001e­îB);\x000cÙY
\x000e[
ñ®6ÓÎ¡h{ gÉ\x0005m%¼f ;»Áa»!'\x0019nI©Ô'L²Tr>lÜ¡³0l7ätT«_TqQK\x0000lKF8\x0001ÎlÂ°ÙÈ Õ\x001dYMO»XÍ-¢ÜÉ\x001feìO6ÃfCÀ;\x0012ª\x001f/ddC:­c<l5¡³0n5½Êó{QÕgà\x001cÑ\x0016²àáÔ"tV\x0013Æ­\x00069}¬. B¢Uò6¬oX|<îRg54n5Éf(RË@\x0011I\x0010\x000f¯$ufCãf\x0013²\x0012Êi±ÞZx°<!\x001e6lêÆwä3c´\x001e ©xÆ\x000fÇCêÆRPi#`O&7,Ëõj\x0008ö©ÃáHCÍÐ¸ÍDÑ\x0006VDS´#lÑP¸2ÆÎdâ¸ÉÄLÚ¦ÄYë±\x0015Ì=dìL&\x0010õ[ip\x0016i\x0017TiÛ8ÃØ}ì8þ±eZa±ËA+£xGB2H<|¬IÝ×Nã_;cÐ©\x0015r(Ô£6I&dtØA¦îk§ñ¯-©£7È¨ãê(:×>÷ñP:\x001fÆ}¤L*2GNÙ>wl}ÒñÏÝ9É4î$³(©\x0019dÑÉo2O±íÉã<uÆ
§pª\x000b
)
ð¹BZ\x001f\x001e¾¡òýý¸üí £Þë\x0008=prï§CiÉ>v9\x001alüæÒtüÖT\ÞìrØv2óC\x0018¥ÀÃÂöÑ
é7÷ã\x0017\x0012¸U\x0016¤5¤æ\x0016r¼µ<\x001cmüæ>rüBRZNm%½\Z¨\x0019²sGýïï#ýødÌ\x000e%\x000b¯+YEh¶]oJØ¼6\x000cûò(\x001eÈé±A\x0004Þmü*¹qz?xÿãÇ/¢ÜåWõQ\x001añ ]ïYë50ûÃ/7¾¿\x0001òãW@É±£Ô]Ée½7M\x001e
ñð%¹ïïüø\x0005\x0010/\x0019è\x0000Gà<@\&Ô\x0019.¶)Óá\x001bß_\x0000ùñ\x001b $·Q\x0017Lj\x0014H\x0007MÈ×¾BTìújd_Fc²«I\x000e¤o³b²È\x0013épêKqËJqJhÏ; \x0015/±´#Y¸BJô`]§XE=+®«Åá@ÔÎ¸ñøåyt[V>M°ÆZÞP×µh'&Jó¡×¸°Ü²)VO÷ýì,:Áè\x000e\S£Ûê ¸^\x0007áÅ/ß¾üúðe\x0016%ºó\x0002òrÖÁÝ\x0008¨\x001dÈ\x001eÝ%qÑ\x0017o>¼}÷¨ì¥\x0011â\x0010\x0007	Q\x0004 \x00161t&¤\x0013}ÒK"\x000f9_hßO\x0018ÖaPü|Ö5´úVô%´5ô\x0017÷\x0013Ò	EÔT	\x001d©j\x0008z&ä/\x000f½ßO\x0018×q0d)·¬_9kÓ1zröË%YÞýiMF	3ð*{P@\x0006\x0007/\x0005-¼\x0000J\x0018.Õ±\x000fìÃ®0|Ù]aø¾¥L¾Û\x0017QÜµ8È¸¹®dþÖÞù?õ5áüÇNÿN×ÿ|óú_\x001e/^_Ê¢ÚzoIÞ\x0014XÏ3¾z.Åë¿»yýæåÛ\x001d ¸\x0006Å9ÐPôÚc¯
Üd\x0015áâÔ1Ò¸&s¤\x0011­È6¢\x0007\x001a\x001aU/'IvyuU\x0011,ßÍÁÊÄ`\x0015z#+
\x000f®IáEáð1Ö~«ÎíUÑy«\x0017\x001e.ÉuÂbÓ L\x0017ä«Fa¡9Xª\x0012	OÒgg))1éIº :
ÛÙ3®\x0004ÑæFxYUÄGrÓ¿½8èb5t¬aUg'2­^fõ¶e3]Åiñ\x0016XÜXwANæ^E\x0001Þ
£\x0006a;¿åç\x001c\x0008{:°Ë¨\x0017\x000c«ÅËñò\¦1ÖÔ±¦9V¹ê®úk2AT\x001f6¤<^Eâ®´	rÇçX\x0013ê\x000b0Ã¢vÞI
»ov¦HÁ\x000e¶LÂiug©o
{\x001a\x001apq8ï\x0010,tÑ\x000bæ¢\x0017çª¯Å\x0015h\x0015iBLt\x001dÖ.zÁdôªQ`M6 Ss
¶\\x0010j\x001fí\x0002\x0002L\x0006\x0014«ø\x0010ÃÎXÖ]`ä¥Ðæ*°I'ËÎÊ\x0018#'1úÈÆ\x001aé:¬ß9¿%µÊ\x0015l\x001dX²\x000f*l
ù*iÃõ\x0019¦¦ÝýPý)¢RkkøZ´Ô»	ø_,¾\x000fíustÔçÞÿý\x001fÿyûõîó_äoÞÝ}ûôõÑs\x0017ÍL.h\x0003>§\x0005ö \x001cÂåi8·ï¿þ^þøîùWïfÎkæí¡\x0011fß¦âÅ\x0008v§*uV\x0014\x000f6ñ(óéÜ Ì~;\x0018s\x0004ÚµªÅ\x0018¬´[v¶õmäKºyãÐÐAo\x0007º
B£A;;eg7Â´­'CÇ¼\x001d6Äl%\x0012>¢U,/\x001dqÊüÈ(ª½ÐÑoÆÎð\x000f«Ko7ïÿzÿñÓ£\x0002Öã±G7\x0002m\x0004½qA\x001e\x0002Ï`~¸yÿÛ¯f5\x001b±q2ãM\x0005\x001aJP\x0005i\x0006KgÓÅÝ`a
\x0016ÆÀHktR\x000emvW(Å´\x000e¶\x0015«£h´F£Á5*ÞåÔÓj\x0007\x0002\x0017(õ£»Ñâ\x001a-¡qÌÇª\x0005#b\x0006uB\x0006²óqt7[^³å!¶àbjÄlìËµ\x000cÇé]#^wn/ÚÉ/\x0016êØ8o3¹F){Ð8ãeÅrþÊo7\ï>\x0006ý\x0007goª=\x0015d½BBó\x001fåü
þn8ìàpÐ\x0018rÕ%g¸ÚÛËÖ ¯H.\Aîë\x000cÕ\x000fZªL-Ò\x000b¨oÜ´¼KW8w~\x001aËn¸ÔÁ¥A¸RÏ¿\x0002§Ó$¤ÿíü|Ýl¥c+clü)U\x0017Tlµ\x0016(Ã±=BîÎ\x001e`Ð\x001eJ6Áß Ê êH	Q\x0013³¹Ên¸Î\x001e`Ì\x001e+uä(Ãå¬½¦ìå(=\x001f¶\x001b®Ûr0¶å\x0002¢ªUfTUåEXÑR[7W6ÏüÃ\x0012S¿-\?ÞýøuN@ò2'«öD\x0018åPª=¬ä,æí\x0013Á\x0005ïÇÛ÷/ß?-\x0012P6OB\x0019g(íyM\x0016)-ëe{¡LkÊ4AÉÞ%´¥¬}rIÆÈ¶¥\x000cÇ!ó\x001a2O@²ù\x0002´¥Ôb.4á\x0015ÉiÇ)Ë²LPJ!¤6ýÄ w*ü`êÆ\x0004àJÌ T
aÂ\x0010êH\x000bYG°9×©Ans«\x0019Lßaú	L\x0004­ä¬b!\x0016kJ[e½\x0019Fè\x0018aÑ\x0017;¼´
R*ÎáÀ\x0015\x0012;L\x001cÇtÅKT®\x001d}IÊ'\x0016L¼5ËmGÎ`\x000e3Ì`¦\x001ap¤§¯Ød\x001dæÑÓ\x0015¾y\x0017vüDÜúÇ¤\x001e]*_ë"_TX\x000b\x0017
üÃ]Üñ\x0013GJî­ùÿ«³³<YÐqÊ.îøÀã\x0008µ¹\x0017\x0010t\x001b{úh<\!òø.òøÐã ´oîò³\x0012´D×ª#l\x001fwg0»Ðã'btõ5Ì¢õeìï­M1[\x0010t\x0001\x0008&\x0002ÐÒgZKhº ìK­åýá\x0008­\x0019Ì.\x0000ÁD\x0000rÒå§B0y\x0019ð¶`Bsî~{\x001eÁìb\x0010Ç é§iz5©ù#W,S)Ç³\x000eè;;÷XrÑÑ»>s¨¬}ÉeNeLÕì¼;{wÆ$sH|ÑøÏös²sî0îÜÒÛKG¦¬ÄLMê\x0000{wè¼;{÷¸ï©¶\x0005\x0016­ß§¶5ãö\x000c9Ùyw\x0018÷î©]¨¼6\x0014Zâg°o~µì|;ûö(*\x0007^\x000b°¥ÒH7fÓ÷"®ÃØùv\x001c÷íË\x0008Ç*8és\x0000;¬«}òmyî\x000cfçÛqÜ·G\x0011¶Èº\x001eõ=Ã¼=oÒVPi
³óí8ãÛ9=ª#\x0012½tø\x000e\x0016E\x0013LNôãÝù\x0002ÇÏ\x0017Q:=é$\x0006¤ã&» ¼i\x001d§ì"\x0010ÎD Ðô©2\x0003g@@¶WØ]\x0004Â\x0008ävIû¾e±
æü\x0015n\x0011°\x000bA8\x0013ÐÚ\x0014\x0017m%uÞ7Ù¢x<Pb\x0017p"\x0002eNU^RÀ×Û[KXx0\x0004~\x0006³sî8áÜ\x0013§ÁE%¿\1\x000b&ôÝ¶E\x0000\x0013¡sîaÂ¹ç¬Cbdkðd»2m\x000eÚJ\x001fOavÎ=L8w\x0019Ë«J\x0005õ0f0ý´E_â0eçÛÃo\x0017qÉ¢JtK\x0002²¬¥GóF\x000eyè\{pí¦ \x0011¬\x0015wlVVRó`Í\x000ceçÚÃkg¸gN7f(Ru·PFgf·\x00053k\x000f\x0013®=É'÷­@)ÚM["\!NÎ³	Ï.!\x001cêá"É\x000b²6 £U$ÉèÑãk\x000f\x0013®=\x0005_çüI
RÖ¶\x000bÞ£AÍ\x001c·êZSk\x000f3®\x001d¶ û$O\x000bf Vßu\x001b.ê|&ÍøLjM\x000cMÌú(ÀðÎ*ºâ\x0015â9uî&ÜQ¤bg$sØAµ0a"\x001e@Ô?MN\x0018zäÓ®^¸S´;\x0019þU¸\x0010ý\x0015NAÔ\x0010MPt`\x001d\x0004Ö¼	ULx0Ý|\x0006³3!0!Ê¹ö)x©¼©;SVS!Óvë\x0004dìr£8\x001b\x0011¯¥(C-ö­J2º1Áãñ¥Ç	3Q 
ö(E\x0002»+¾ºãÇ	+§jK\x000f©õoÛòAíñ\x000cegäqÂÈ9ÛµS¯|ñ¢ÚAÉr#¸F6\x001c;#\x0013F.\x001fZ\x0005f\x0003dmóá(ißÜmÝë\x000cfgäqÂÈ\x0003g\x001a'Gíë\x0001¬\x0006ÁgwÜRg@iÂ\x0002oM¬.\x0013¡gu1±I(z¸Bn\x0014©Ól¨Ûsi<\x0018öIí\x001el\x0002¸$³#·míºIØÂbýG\(¸²-3¬\x0003Q{¶¤]~	ZuBÞmMe!úzÿeÈ/ÃQÍÉiÎ\x0014¬ð]\x0014htÏB¡ã{Òveù?tjÏ¨BbØô*¶ä
ïD\x0001¶´\x0001¦h3&mHó):}Õ\x0012q,;++TVÐ\x0003@sþ Êp-Í÷ø\x001cU¤Íµ5îÐ³QÜLÙ¬Ê\ìý¯7¯>~¾ûòçÇ\x0005»¼´Ïj§\x000c×ª\x0019ér^ûÐò¹÷·Ûw7Löüíï\x001eÓÃ\x001b\x0019¡A:QÍÕ¾ÎäL¸dëG¹ø#t¸¦ÃAº\x001aA].Nå5£#\x001d|\x000f"âõ(ÝÝïÿ~\x0011-¬ÑÂègµ7jeN5jçUÓ\x000eb:\x001d,\x001c­éh.y\x001d\x0001âD¢ÔU³p­\x0011:{è\x001f¡kº8JtÎ[T^ë\x0005\x0002[ªµÓQÈkº<F\x00072\x0010U×Îe-àYÄ ´-{«$3
WÖpeÔ"L#£\x0019±A +\x001dû¬«RÌ¸*ÅÜ»r\x0000ÖË%g®Áùs%E#t½\x001f\x001euÄM*½
\x000e.RkaÏÇvï\x001c±\x001fôÄ ×\x0015ºxÉk	QôNuª nG\x0005\x000eãuØ\x000fºb\x0010SÐçã3õÄ)C9h\x0014¾óÅ~Ð\x0019\x0003'Ú^JD9ëÚ\x0015\x001b³·í\x001a£x3öÞ\x00188ù¯×ÏGÑ;
Æ¹ë\x0011ºÎ\x0019ûAo\x000c\x0018uþo
6T9z»\x0000JçnÌFèRGFÍNìW¶d\x000b³¢s®óÆ~Ð\x001d\x0003ZmÈ"äR\x001fàyã5õ\x0006î 2\x0007ËA\x0007HMm(eyOªßÖ<\r\x001c¢ë\
º\x0014>i$U\x0017JÚÆÄpz\x0003"(z®3Z\x00185ZyAõ)NºJ\x0017<\x001b«Å>åXb\x000cYÀ¨Y0ÎNíyÐùcçª}váù´9ó°É®öÝ÷_~þëý\x0013S:eí\x0016»äb*ºt> ;ïð~¼}ûâ\x000f·;à`
\x0007£p®0\x001dÙ],¦¬"î>ø£t¸¦ÃA:5V0\x0008\x0004F¥Ó:Hå(]XÓA:NR Ê}zò^èR0ºtÁ\x001dï¦£5\x001d
Òy-Èe:\x0017ô¸ÈHÚÇàñ(\\ÃÅA8\x0017ëe`*XJ%\x000b\x0006F\x0017ÂÄn²´&K£Ë¦Í»öQÉ4\1\x001e]·¼¦Ë£[.
\x001dñÉ,èÒ%SG
t®)r®¬éÊ\x0018\x001dÊgõ£\x000cyV_d¾ä¨=ønËùÑ=GT;fdí¼Öb¶ôÄ\x0007\x0019ðt\x0008¯û²~ôÓ23<Ë9NÄöiÏ\x0015\x0000\x000fà­G\x0017¤ScÇnWììÛr\x0002¯âË)5º\x0008ç³§Ýt}\x0014\x001b
cî´x¸h\x001fVb"¤s½£\x0003x±Ãx¢WmÁX¤\x0014Pð¤USüÏ?×;ãAËÀ\x0012*tjÆ	µ¢Î?å2\x001e+zr\x0017í{Ä1k\x001eå¬ÓZ\x001có)?Ö\x000e@®\x001fd\x0016Èö\x001eóôÛôã+É[PS¾´¿»Þé±\x001f<÷®½\x0011·Ù2J¶üüÓ§{\x0013T{ñåÿ.¯\x001a/þúñþÿzÈÕQv\5b° Þ*ói\x00126s	^½º½UQµ\x0017oß¼ü\x0017yÜxñ·ÿçÓÌ°fiæP\x000b\x0017f\x001fõ	\x0006³\x001d<m\x0007©\x001e@Æ52N#ó±I·<\x001aÕ\x001bÞà·°(¯×B\x000ekä0¿30¨\x0008N¡dý"\x001do«ì7·0_x\x0015Q`Z\x0003Óü\x001aWÈ\x0005¼J\x001a&¡Â¼Ñw9²ÈqÍ\x001cç\x0017Òj\x0016-ËâóM[ Ü½ÂO\x0002§5p_ä\x0014UmeI\x0002ª¦ah>äzè\x0011æ¼fÎó,ïWªl]e{Óã|E\x0017WÖÈe\x001a9yí­eök\x0005KeÂIAóÄ«\x0007\x0018	$n~\x000bÕ>+1¿¢}VX²v­yÚ>'\x001cî£ß|ø\x0013ånoÇ©¬W3\x0001¬í·3^-ø.üùùø\x0017³{¦&\x0008¢Õ²7Mt\x0008)\o¡»øçç\x0003 \x0008ù&2Á¥ª\x0001h\x001d\x0015ït½î" \x000fRºOº¥½Uñ\x0007üàó¿\x001es\x0017\x0004ý|\x0014÷\x001eÔÎÉR
°R_O°v\x0000º~>\x000c&*vCJÎ4©Ù\x000cÛÑàz[º~>\x0014fFz\x001eô®®4ú¶ÒÎ_-|û.\x0014úùXD¥*·:\x000fÒ.h®#ù.\x0016úù`£o\x0017\x000f¼¥½.4|ý-
]8ùp(-Ñ¤/\x0012QKÙ\x0003$l/\x0012ñj¾\x0003ºh\x0008óÑ0KE@]èÈ'kÕÍ«mhèÏóÁP*+ÔGóåjaÎÙ"øvæ\x00143ü©ïìgÇÛ½ñ×»o¿ç\x001f8oÇÚ,c£]^ì©°\x001d\x0001·ÆýÃó\x000f?Þò\x000fOút»#ö¦¥Îu!Í¨%\x000eX¬\x001fÐ/
]W@\x000eu»\x0011ö¡2\x001fØ¢Z\x0006EÄ\x0015uQ·Ó^çH±#ÝæB»H£Ë\x0016è /Æ¶\x001c+äEÝÜO¢\x000eu\x0001í[Ô\x0012j\x0011±`ó:ß\x0006\x001e´\x001c\x001fñºûQ©CÝ&>;Wj%\ýf-\x0008Î&îÁ#Qm?jìP·éÎ>T>ØÙªeÜój\x0015\x0012\x001f9îGM\x001dê6ÉÙºtÑÛ:eE-
õ1×º\x001f5w¨ÛÔf\x001f*oP=] ÷ÚT\x001f\x001c¨B(\x001fð·\x0003ççPKºÍhv¢¢åç 3aÕ\x0003@n³\x0017\x001f»
Ü\x001aºX\x0015¦b8«¤¾
ä\x0015^}¹ÕíìIÒ.V¹XU|-*\x0000:µ\x0018\x0014ºk\x0004ØÎwCíbUU1=\x0016ÿ£FU²û³£	\x0000Ò¦8\x0015ÓÔy\x000fùôñ×Ç!½8üØ\x001cª\x000eÄD¶IK9÷X%S\x001e¾õòÝ\x000e>XóÁ(qÆ\x0013\x000eß\x0014%àÆwî\x001dw\x000f×|8¼~¡
\x0007Å\x0018´_Pf§Ø[$lÇ­møÎ_\x001b\XÃñ\x001bka­,\x001eÚ\x0016ÄÜ¦¿íÌ²ÑÅk¾8¾xXÇz×¸uíB{Ç}|é¤Ëkº<L\x0017OU5"P¯9ùa¯îèÖ+k¾2Ê\x0007²ß¬$)ªf)Jñ¯½{xÜwº/^<X¿ºxä´Y^\x0016Ï¾­?×ú9B×û½aÇ\x0007)T\x0011¡ZnVkRÛ|élÝÔ\x0000`çøü°çóª¬`»e\x000f©\x0011oy\x0018\x0000ì<\x001fv}ÈHÙO]Á ¯pH\x0019­àÙ¦\x0001ÀÎûùq÷r;,PÐÃb\x0008ÅÎ
~;\x0005b:>\x001a^@þÂZ("õZá\x0015»Î	/àuÎÙ\x000f{gðÁ¾/F²ÐJ¨ðÁ,QÀÎ?ûa\x0007-õûú\x000c1Ûúwf!ÛÛÂaÀÎAûa\x000f-§i¯7V¢\x001d_ë¨.¯zc\x0005gëWö\x0003Bç¢aØEó\x0017´ªVçR+ÂfÁHÇ¾0tN\x001a4T	(¹òsæ¤£MÑâ\x0005<è\x0003¡ÏN´Tò$jQ¦¶g\x0006\x0000;'
ÃN\x001aå\x000b·*M½ÚQuPýÑª£xa\x0017
Ò¡$Å¡h¸\x001dô8Ê×¹h\x0018vÑí¾IFÎh%d´Ir¹ðûvN\x001aÆtrUV¥Ö¥£-`¶$ÎéY\x0000vN\x001aÆtB«\x0013\x000eÎ¦)àRlfYê±0\x000fÄq\x001fX@rûÆd½üÀ¥C¨\x0002\x001c\x001b\x0001ì|\x000c\x000eû\x0018t§<Ó\x0004\x00174MÈ&är\x0010°3b\x001c6bôÉ\x000eJTå?k¶']·'8Ê×mA\x001cÞ>kE\x001eô%3\x0006´#:7Âe$OHú©Ë\x0014Ò?ý4üVzèíZ+ú¶þÇP®º®tÕ|õTê:²ÉXé*\x0019+Ä-$Ä\x0019Èÿ1ÈÿCû;7ù_¾Êj«Á¿ýôåãýß8N.'S
-üGÓÄñ^\x0005;'àdw?|÷öåíc\x0003
\x0014Ö 0\x0003Ê\x001bOA¥VJOy		Ngu»AÃ\x001a4L¢{\x0016+§ª8¿PQSþãy\x000b\x001aãkÎ8Å\x0019l*;pìRoÀdQ0a>¿;Ç@ó\x001a4OFW\x000b@\x0019TÄÀë\x0016Yv
JÛññ3 «ªDGÝ-Ó\x0000©Lòð¢öq%¬PÒ\x0008çÓÈ1ÒÎü5\x0015¬âàb!Õ\x0015'\x0019åìlÉO\x0019\x0013oMd`k\x0002Ò_ú-ÔÎJÐvÖäçÌ)ÛlÔé¢^À3é¡oOeãñù\x0007ñø?~ºûYæhüüõÿ¸y÷íÓß?þüøL{Â·Z&\x001bK\x0012W\x000bnrÔÛ<\x0017Ü&vþøêù\x000b ýòõûw\x001f^ýøòÅ\x000eJ\Sâ\x000ce,zàÎrr¬\x000f9Í_ö¾Ã´¦¤Éµ\fò1%QÝR<¦SJ\x0003n\x0008§0Ó\x001a3M`Jâ^K3\x001fx´ß:\x0014¯oÕ.Àfòñ\x0010¦£­\x0013uZNßÿòíËÇÏw_\x001fí^Z\§N\x0013í¤sAÁDÎ(pûîæû7\x001fÞ¾|ýüýc
LÛg\x0018GbÒNBþØÑdôÜ§Õ0dÎ`;¢y°¬	Ë8¡«\x00074!ôÏj\x0007¶è\x001b¶\x0019\x0014gÙF\x0008WQzñ¤½AEþS\x000c*¥ÎkØéÏN½\x001a#\x0010Æ	ÑÆ¥àô¡\x0017ÑòÌ.èì\x000c bÃ¹U±Å´$5qËm:Æ\x0005
ª\x0001ÂÐ\x0011Ï\S6Ï¶Yq«ïLç&c!vþÆ;«S\x0014D»ñãïÜfÐÙÁ!ÄØ!ÆaDÑ¦ÔÁ\x0003\x0005m\x001d:;ÀGÉ£©#Lãß\x0019L1=\x0016áf\x001bcÁp^¬m\x0000±óÚ~ÜmK`®ê1¡\x000eiIè³­âÖÝ\x0001ÂÎkû	·]Nd\x001e\x0007\x0018?û¾?\x0008Ûq·²M7|°©7\x0019ÜztãàhdYS¯\x0002µ÷;\x0017QW¨:÷?³M0\x000bÛÒÁ	Â.²Àxd)`¬bX2²\x0005lÜ	·nEè"\x000bGTl:»ôf·ïl£N0S\x001fCìB\x000b\x000c\x0016p`º¥°1Ù\x0010mD:7Kb\x000c±\x000b-0\x001eZ8=,\x00086\x0011Yð0`\x0017X`8°ðo*\x0013é¥âÒÒ0+¶±G#\x000bt\x0005#\x000b8gºâRk­á\x0019£ÍîåØwØãt\x0005#\x000b³ÏL\x001cu\x0002%íÄpN¨}\x000c±\x000b-0\x001cZ3\x001b°Á+ÉN\x0004l"&\x001d}AÒr?!vn\x001bÝ¶,¢®a²ë\x0008^Ãh\x000e\x0007ýQcÁÎ'â°O\x0004lÆ"}¤õé\x0006Ú\x001a-\x0013#¦\x0011=lr\x001cþaÝk÷íæí/?ÿu/y¬£\x001f[} (6/â\x0014¦\x0014ï¡¸³\x0005¾\x001fnÞ¾yñÛ·Oã\x000e¯\x000câq¬#­^l f·âÊóm¸»éN¹Ð­úçöÑñI¬¸\x0008Td\x0010\x000bZ3\x0017\x0002í9Úç;<?ºx¥j 2^ö:.ñÚê³Í;ûé £Å3:ÒCY<;ºvØÑá ]¶v×há{ÈMÿ¨\x001c³S*³àQ<oÝnR±\x000c/Ùê\x0001í ØG\x001d\x001e~[¬38¥h\x0011ôºW,µ²Ïó=ÿûñb\x0017\x0007ñ°õos\x0014Ó\x0011\x000eX|kk+ù [I\x001d^\x001a÷ÉVñî¾Y±On=79\x001cü¸]ÈÁ!Ø´%¨ÈÑnÁ&Ö¸4ïÏá¹XTAJVðË·¯ö¤òãýÇ'zVRàõ«G%W²\x000eM´;#Ú¶\x000cáÍ÷öòãíËG\x001bV\x000c\x0011Ö0è¨Öë0c¶±)Ú\x0018rÞ*\x000f?düùîÏw¿~ýr\x0011×8ÎèÝY/O§5w\x0011±\x0017e| ,ùñ|c\x00015`\x0018\x0006DÞI?tú4"\x0018_Ú*èM|gZ#ÒÄwö6\x001bÝ\x0011=CýÎ`ãC·³£qÍ\x0018Ç1/é\x000b#ÚäÂ\x0014¥}¬2­Àù\x0004cZ3¦OÝòhþÇT\x000b;E\x001bËÛÑ¹\x0013yÍÇ\x0019¥R¿dÕõ[óiØÖ\x0011·]T\x0013eÍX&¾5èd\x0011Ï^ð\x0019è~´ó\x0008ä\x0007rñã§gÅ}»ôvÄ\x001fEUÙÓ2£ Búí
Ã\x0004d\x001fcÆ\x000c¦ Sá\)Ë\x0019ª~mo;Ò]a%»(ãÇÃ\x000cFå\x0005Rd=êe\x0012\x001fuK¦²Õ@ìÂ\x001f3È¾;+drö\x000e w7
·/\x0013]¨ñ\x0013±¢M©bV!DQïk ¥||%»`ãÇ£
FW5\x0010\x0019R\x0006FýÜ¨Ã RÜÖN@vÑÆO\x001b\x0019¤WÇ\x001a\x0014-Ç\x0012a~#Ü¾ùL\x0010v±ÆO\x0004\x001b>½\x0014]Fô\x0016\x0010)Ú§¦íÌî	ÆÎû	G\x001e\íÊaF\x0017©Í\x0004\x001bÂ`ûÐ<Î\x0008	\x0017)zd6,ë!5&A\x001eöÐçá\x0013\x001eR.è²®£ÍOIæ{ðø·ÎAÂ\x0004mpâuÒ\x000ce\x0004|\x001e\x000cõì\x001c$L8HoµÀ\x000cU)Ï\x0006é·o¥\x0013	\x0007É9\x000fé¬Á\x0004ªfÁdãhCèü#LøG\x0017+Ï:pPãk#iÊñd\x001c:\x0007	\x0013\x000eR²2Ý\x001c\x000cõâ\x001cÙ°«\x0007ã¤& »l\x001cÆÓq\x00109AýÖRS­&¤bÓÖÒñ,\x0012»T\x0017ÇS]66s­Ô§@m>RÜö¶M@v>\x0012Ç}$ð!¶(d ö$\x0019s[Éí\x0003þ\x0004dY1î$\x0001V:C,È+¯¾´ØÄm+ü\x0004dç$qÜIz\x0019Ì­Câ¤H_¬B±ÙiÛ*8\x0001Ù9I\x001cwà³Lsª+iêß	mþ\x000flßN'\x0010;\x001fã>RÆw¦ ë\x0018í\x0018+×fmG>y}ö$dç%qÜKJ±\x00103Ð³\x001cÍll\x001dé
\x001f»ó8î%9ô=³9¨ØÞxÝÉ´·c­'\x0018»\\x0017Çs]Ï\x000bél!å?Ù¬¶½yã¡óäaÜ{\x000f§­ÑJK|jüp¶\x001bº<gän:Z\x00172Ûu\x0000@0\x001fIÇï,B\x0017mÂx´qÒ#\x001fu!±}mï\x000c2n[Y' »h\x0013Æ££ªi­;²möJÐväáÜ"ô·ããÁÆÉØeµmé\x0000'´³M|0\x0002o\x0002²óäaÜsg;ýÖ$1\x001eOÒBç#Ã¸tÎæÓs&I
Ò6\x0003|Ûæ8\x000eIÿ¡aÿ\x0013\x000b\x001fºìk×\x0011#lí®ÍPßÆO\x0010vMÃÍg«ÓDp\x0019¿]Æ¥6Õº\x001cÏu©3\x001a\x001a6(\x0017>ö­etYÍ,©ds¾^\x000eÇ\x001aê\x001f3´)·ËH¦ª}·±3È\x0007#& ;Ë¦aËÅ:÷HnVY;]þÄÃÙ\x000fuMÃ\x001d\x000b\x001fd©úñâ-EcS²'\x001bNÍ\x000f[vì,;[6'ÞfÙ\x0005
²5Ù[q
ÇïÑbgÜqÜ¸åbÊë%>&­C2Ð.M·3gNÛ'\x0002=oÿ4Ç6	;C´kª`32 þxRîþt·á¼\x001b¿\x0018pR°eYv\x0003\x0007J-Ü6Í\±¬
ôeQ*\x0018½iqöís\x0000UNíÈ\x000e\x0011Ç¯0¶¤|°!
§ Éö®ý\x001c\x0001ÚuËªÛãÎ\x0003Ö2Ã*¢¦ÙÒ7M[µ\x0000ZÖq81r\x000fVujQZ\x0016ßjY\x0012Y-½)\x001f\x0019saK\x001afHEI\x000b\x001dÈ®V£·wÆLGn-ýFÈØÎ¹ûñËÝ:¥ZP*ý±}T¨	CÆË\x0012Æ?¾}þ»\x001d°\x0006Q@\x000fÉê\x0012N¹&u¡<"]¾\x0010×8¼e¢vÚ\x0006X YµlåpY]'aX\x0013á5äã\x0007]ÃdON­e«àeQý´&¤á5$[À¬V"Û±­ßemêtqM\x0017ér|fËíî\x000fL^ï0`Z\x0003¦a@­°I¡Ûöö2ËëGg«#Gðò\x001a/\x000fãÅ¨ApYÀjÂ>\x0001ã\x0006RÖe\x0018Ðç¶~*ÕãW>.ÏñØ·*PòîÁ\x000c¹\x001d|Ln@&A©\x0001KL[Á£NÐ÷qd4ÄR\x00070¢3E\x0004WZ÷cÓ0v"vd;\x001fnÇ*r(ñÚæ\x001dÇÐB	\x001du¾\x000b%Ûqp;V1&­§áU\x0004k®uÌÕäGæ4ìDìbÉvøÛ\x000f¬ OV±}hj{\x000eè.lg½í@(Û*j\x000f\x0014ÿ³m\x0015ÏWÛ v\x0011e;Ùm\x0007bÊM#z\x001d À©o{ñ°Aw!e;Æm\x0007!¨\x000c´,¢HËÁÝ\x0016ñðVìÂÊvhÛ\x000eD\x000e&Q­%=nºp
,ñð*ve;£m\x0007¢[­bÐUäsjÈå¨µ@\x0017\¶\x0013Ùv J	vh«X\x0005ñå\x0002Òâ_IGÝ"tÁe;íiD¹*±\x001d\x0002²ÞõD\x0013³\x0011u £çaÏS\x001dg'KÉÏBØº¨ÜO\x0012BÚi@7¯á¿Þÿíãç¥7ôÅ§_þüññÎÐ\x0000òÜQ\x0015[}ÎÖÇÿ¯½¢Ð!¾ø\x0003ÿéõÒ\x001cúâÕß½|¬5Ô\x0018qÍã¢\x0006QEeÖ¼
¢?HkD\x001aF\x0014y*0Ä¦ß\x001f½\x000bÆ¸©MaLkÆ4Î$Eì\x0011U <RhÇW1¯	ó8¡økÝl9ÚÈ\x001a­äÃËÌÊÃeÍXÆ\x0019e,6VQ\x0005pí`/Ë\x0008G\x0019O'Å¨ÝÄBÆZ*%\x000bÙ\x001a94\x0016[H<\x000eÙ{q×Ãÿõ\x0017ß]\x001895ÓöB\x000f[Ìél° ÂÄÇÎõp ëhsç0Ìz;Ûs\x0006²ó~Ü=\x0006hC¢\x0001QûT0%´>M\x0017C\x000e2CJ	®dÉ"	U¿¶³\x001d¹\x0019/1Ã\x0018;Æ8ÎÎ&·ÁR{V×Ñz­ÁÁa£qi}\ý¸ü0lßI.=Í	yuÅ&y±\x0013:àÌóFïXÞ%Ö¶³Hþ×ÿ÷õþæîÛ¿ß¼øëý¿ï\x001få%â,£NË.¢^U\x0010Ø\x0004#ç7)
w\x0016}óþöæù¹á__ßî\x0000\x000fkðp\x000c\x001cPÕ\x000189/ªBàôèÍ\x001e&_Xè)rZÓaò:Ý5ål\x0006L¾)(¥ÐP:\x0005Öàé xÔ4IéCPpSóvËÔÏë5y9Fî\-«M²æúlB^K½yÍ½¿KÏûÎ>ýA\x0003Ç³T\x0017^Ð3EEéûÜw\x0016ê\x000f(£¡{­B\x0011t0ôkè*ÈäMA*+Ã1¦hã8{TòkèéZe\x0001ÏÀL\x000e­;ý¢jcµ,É!\oÍ=unQþö\x0010»´\x0005U#&ºÁè¨1o'Ì¡»*||*úã\x001f¢¿&qñãûï\x0018êqPkÕ$µ³>iÌÑ¤sàÂÜã\x000f7üÓÍwüÃ¥\x0003,ÃNdüU©yH¦6AØÓÙ»¶ý|§Dá#7ÈÇ\x001f¶1 E\x0005ÂßØ¦ñBä#ÚdID§©\x0010\x000c÷Ëç¯÷²-\x0017ÒU\x001f<Å\x0004Öºít\x0014ïDg\x0014ì\x0018íÍë÷·;Èâ,I)ÅrUä9I'G¤¢I®y§ÈÒvÍ\x0012­TKLöEþôÃý?_þ÷ãv,2àµÜGU¼Ó+pÅ-õ2ý\x0017ùÓ\x000f·oÿ×Ó¸a\x001bfq×w&çE%ÎW\Ñþ¯¸\x0017%ÇqiKÓ«ë¬e\x001f|Òæc>­Y\x0001ªÛj\x0013MãÆ5nÅÍN+V8\x=^G}\x0002ç«ÆqÓ\x001a7ÍâF\x0013èæ¸L:»8±5Üx¾Pz\x001c7¯qó,.Øî]0=qâC?ß3[Ö¸ezuëÆ¡ÃEYA\x0007ÛÞ!Î².éH/é¦`ev~KE·CL[^®Âë;^?íÇìÕÅ{ÒüÉf°¥áÖ·\x0012~6L\x0010\x0004}k\x001aègê\x0018
.´É0\x001d.N³Öp>ñê\x00130yj\x0003Û1Þ³´]ðÓQ¢$+¹î¸¤ç\x0000jw[<1ÍÛ¹]?ëwI
íQÍ·!Ù\x0008ÊâÙBûqÞÎùYOÆ¾êâ\x0006§m¼yM¿°àù¶¤ý¸.Æ>\x0008;\x00194¾zæ|õËÍ»'®Mcªú\x001a"\x00026<\x00035ùÑ>\x000f;=r¾¹yñü±3Â¥5\\x001aËX;ÛEÞ\x0013´û\x000cs H\x0019ü¥'ØtyM\x0007éø|§sÉ%çvv¾k3\x0000£¿T«°®¬éÊèÚe»e¡äUºOwmjúVlhî\x0014B®«Ûµxv	±\x000c\x001bÕy²¢í»\x000cJôvâù\x000eÏâ\x0015{Ì\x000cRc¦xlÌw±<a'\x001etx0G.ØÉ8øh\x000f29©ò&öh¼\x001f\x000f;<\x001c]½lÁ9{ÁÌÑ\x000cÒ1§²\x000e#tabëW	Ïí<"{^Vv?\x001cup4\x0008ì^¡È;p\x0015ÌÄ:FÂK\x001fæ$Ë}Íx¿\ú\x000bf¸ûøÏ\x001fï¿<1]\x0000Zu|æ,Ç[OhÉ´÷\x000bòvÅóüå÷¯_Þ¾Ý	kLÁ\x000cÖàè3Þ$0q=äø|^6}\x0013×8ÃÉi
`[Nm}\x0001,64+kp5gúìÅF°H×qF+*#º0
hÖ4Áéòi=Á©oLàñ´×àkÎ8õÝÛ¼¼d\x000bfpÉó\x001aiMfV3¦ªÂÍ.YÍ¨ÏúX´ÕLÂÌkÌ<õÑõÃÈb\x0016"\x001c¨­æù9PceÍYf8WNI\x0004°´qÂ´\x000be9ÏO\x0015\x0019â\¥fâãÝÔwÇfEaõÝÛö<; u³E3ÁH\x001eöC[OUlòÚr^a{ú.\x0016ù`$MÚEªT÷§Ýw#mË]ç@»`äg¢¨tët# Q1\x001fOVM1\ãÃwÑÈÏ#eW_é\x001bG´6GíÑ.\Áú.\x001cù©x$ª¯\x001a7å^>ÎÅ£´ím\x0002íâ
Hàm aæ£­3õ!k\x0003áãì\x0015\x0012\x0011ß$?\x0017b±1\x0005ëWám`Î~[?\x0007Ú\x0005%?\x0013|:Ý\x0017çM¼\x000b²M
çgGrvAÉOE%i¹®ëRËì\x001c5SòWà.(ÁLPòt5ÉäÛeT­æ\x0015Ì\x0008º\x0004S\x0011©èµ\x001foÈ¢\x0015-¢Õ¬h«´1ÅÙ\x001f¦ÎG\x0019õ£´WÕ6´Ä.ò>½\x0002g\x0017`ê|äAî_ª[Jú&Ä2\x001aè\x0003%÷)Ð."ÁÔ\x0001©Ýþ{Ñ&R±P´¦g*\x0017¦±qv\x0001	f\x0002\x000fÁf\x000c\±\x001a\x0012äfîè®à>¡óó0ãçeü¬B\x0014Þ\x0004ª³rK\x001a\x001f\x000cC\x0002íü'ÌøO/â%  AoD°5'ÆKCh8±sM8usÃa}ÅiÓ5I+â\x0005ô
[\x0014û+)/ËìÏ
zlM³\x0007W\x0014p#´Á?ÈUØË¿ýýî×_+ëw¿üú¯ßî\x001f/å%ÉÅl\x0016É¡f!Èý-öË\x001f~|þî]eýîÍ»þpûh17nô6\x0013f8eÜ@}§	¿¦£EYß}is]<kLÁ6Zª\x0010ãR\x0001][h­*¶£úæ8Ã3Ìpr`¯ÉE\x0002;{hUå\x000ces:ã¤5'sòáØÕ2rYÏ&\x0015ìÙ3Ùg¿ÊwkÎ8Å\x0019õ,·|w§mü2\x0019ûß=­9Ó\x000c§7ÿÉßÝ[ÎäA\x000fÇüÝ7·LsyÍg8%?VÎàL£Õ{\x0013û\x000f9^c5g²#l\x001càA(t^Ç\x0014çª!\x000f«TÇc\x0002\x001dcëH\x001a õö\x001bèöÍc\x000e´GS\x0001Iª¦PA}ëÚ'Ê p\x0005Kò]@òs\x0011ÉÛÀ\x001e*IûµD\x0016#\x001bhºkò]HòS1©9]t(+«U¾FIxïÞ9z?áéy¶q32|Þ$Gm\x000bm»ßæ8;Gï'<½4±x\x001eÿMÛm®"y¸gò§÷\x0013®3» æ{ðzsÃyÝU0;Gï'<},PZbWÀ"\x0012ï(Kìð\x0003¥m3!ÕfÂ\x001f?Ýý|óîîãç¯7ß}ºûøë£B
Ä<Ã	$hMa\x0014uÚ;À¶áñÇWÏ_ÜÞ¼{þòõûï^=ùî\x0011)\x0005ckÆ8Î\x0008$_yadg¯í<ü³zxÀÍâ\x0004ãªè4×¢ÓQHéq­_ÏBVÊKY\x0001`Ó9\x0002\x0019ò&ëä\x001f$ëüwäÝ_L6ãõÝ·¯B\x0006¹ôt:VXÊ¢jñGpV¦÷`@ìÈçßrÆëç\x001fÞ?¶istã\x001fºñ®o?~úôx_	Êõa-î¦*,=ëuC¦c÷Þ¾|õêÑ¾´9°	\x001dÑI7Y­ÈàE>U+\x001d\x000bª­{épMct©èØ\x0014}!\x0011<b:(©ª<0ÝùÜýpa
\x0017Æàâ	N®´«×ï©p"qÖt4¸tH:éý	\x0007A.ÚaÊß}ûb5J\x0017×tqpír¬¥á¼vÉ´ddÉÐÖîÒ$Ü½tiM\x0006×Î{­(ã/Ô=C®}\x000cwA\x001dv/ZY£Q4¬sd\x0004­èá\x0015r²¯.MÞ	ç{W7èë¢\x000c½Õ¯o±ÑQtu.ûÍ»cö§wÇo7¾Üüp÷åWþë¢\x000bþX\x0005rh\x0015È\x0018å:­V {\x001b\x0005^¶jùµ_Mþ\x000b¿}Wÿ\x000bÄL\x001dfÀGæZ\x0011Rr©yÁz\x0011 o'YÏ`æ\x000e3Ï`ª¸®`J/­\x001b\x001eÔÈOPBG	\x0013Ä©ª'\x0002ÅµâßdµÉ@çJ\x0008G)KGY&(}ÑpRsÂZ\¹\x0016\x0001C3·Ð§12ËÀ$ÀÄ\³Béãµç[,65Ñ\x0003lf0C\x0019&0ùÄOÐ\x0014Z²bBË¹×ðQLê0if5©/A°Á­¼z·ëÁ«+\x0019Åì¼fð\x0014§Ð\x0005S¦fÖ½É\x0019·©mí¬	ÌUÿ6c1¡h\x001eáYÉÖÁm-ðx®|pÒw~ÂirÞhæôöDêÕÍ(\x001c· ê¾9ÍDÊ´ ¬¾=è\x0004>/mÍtHI]¤¤HIØB\x0010»&\x0015pÉêë?¾±³ó8aç\x0001½ux`lRjöÛÉzC\x000eúcª	yg¾º\x0017¨_%yûîþÓ§ûûöøaZ.t\x0000©c¯2\x0003Á\x0015kV(R/¼¦|u+\x001aQï$ûîöÕ«Û?~xä0m°¦	Ê\x0012ìòÄQÑêÆÐÞ\x001bø \x0008x\x0012×8AIYëÛ¤\x0018I_öÅå8eXS	Ê\x0004m-k±ðBõI¿øæ<1EIkJ Dí.ËrzÒvpÁR£ââ\x0015(ã2Î|q¶ñ
2¢ra$Ë8XãiÍ&\x0018ìFÝfoÁÙ¢ÏeSÞ4E×yæ{»¶+Á\x001eBCo½ÂÛ"¬1JÚÈáÊx³Íó×÷_î>Ë_ßýòíÓÇû/ë\x0004E,I\ºð&(ZË\x001a\x0011ÚËwÜÈ³¬/Æ¿ûüµüõÝ\x000f¯^Þ¾}T)h+$ãªÌ<y`×\x0015Üª\x001c#¶aò\x0014Ýåw±	p\ã1ðZ¹äÒ×Dg½ëlç\x001dÄ\x000ekìp\x0008[v¶> 8½ áÍaOÐrsMpZÓ1pÐ6<\x000eaQêQ*y{IW\x0005kðx\x0008ÜO7À {#_;­¹Ó1YqRæêRlð-¹t¹Ök\x0002<¯Áó1ðEY¯î`Zëè[\x000fWÝ*eM^\x000eçh³Îc.Z%À±Èf\x0013<R%0N¾ê"zP)2Ðj\x0012Çõz\x0011\x0017¡´&Ìk&ÐûØy,xJy ¨ÕC¼]Lìêj!Èo;}}^O\x0013cÜ»o`éWÚj_²À¦l\x001d`!^hçfÄç\x001f^íák¾8ÊÇ§öª$\x0008rþXøZ?Õ\x0012§q¾¼æË£|2aU×Ï9\x0011)Ô6µ\x0004Ëy\x001dÝ|+£ò¹ÓØ\x0007è,Zø(åbÏGãp¾\x001f~?_·ÿüè\x0006Ù&d{q®Ud¶\x0001·Òüã¡\x0003\x000c£)Øt\x0018½ÞÁñ¯mÒ;¯d±¯3\x0010?j!ràMÕB"ÅgQ\x00170µ\x0019NîÂýøQ\x0013;Ûz©öuö\x0016£c9ú¡3\x0011\x00185\x0011I\s[Àªç*%a¥-àÁ/\x000c½\x001eöÑ\x000eu
)WME ÁLäÂ´½ýÀ¨$Ñ	P\x0013áµ¬%+ì\x0004£M:ÛvÄ\x0003v6\x0002ãQ¤´±H2ùQ\x0001\x001b_¸0æìi>ÈÛVÜ×Ó¼øåo?Ýÿt÷åËã¥I \x0003¦å65Ë#n
s¡x\x0010àÂÇ\x001d{g~ñæïn¿{þöícãrò¶\x000f"÷e5»!½Ìë](ån­Þ\x0008\x0015§É\x000bþByÈ\x0008dXCß(d\CÆß(dYCß&äª¸<»µäo²7ï	û&>ÕùCÙQ0¡vÈúz+Â­Ç
Üw\x0006î£\x0016¾**Ïn-\x0016¹RjÉë\x000bYf¿hÅ¦hS¤ù¿áR­Õ\x0008&u4)ÙP¦Ö\x0016//yÒmg.NQ¦2S2]mÆJRpª\x0017è$d¹}";y÷åçû¿_dÌ\x001dcþnËÎ]ú	]ÑQm)\x0017»ä')6Ötéé|
\x0013:W\x0004\x0013®h©¶á(N¯³Ø¦êH9)\x0017»PF¹RÆÄoDC)±«.?×C£´5¦\x001c¬C\x0010ó¥cÿÓeùÆkF\x001cgt©õbð\x001f&¦ \x0002a+A5Ã\x0018ÖaQoý\x0016FHÚ\x0002.\x0007
ëgJ\x0017\x000eû\x0019iÍH\x0013Ð=¨ÀË2!ÀºØÜ¥ì|?c\3Æ)Æb
lüÙI\x0019©5°Åãû1­\x0019Ó8c9õ®q¶QËíøhM7\x0001/H\x001f0æ5c\x001e·`C~\x001dqÜIf×Î¾5ºK×e;Ú¶Ï @ÝTÐo7/îþþåãÏ¿|ùüøk-q¸®
7>º6Ð²HâVâÒ¦¤|¸yñüÇ·/_¼yûú1G¾}ó\x0004êFíÆn#R\x001cµÍê+\x0011ÝU8qÍ3ËÉÁPgµSj\x0015Ê%Þ ¡OçGCq5gYÏÒ¦8çÑ\x0011VüÛU¤\x001b\x0001§9NZsÒÔwÇg±Þø\x00112'lwÎP®ÂÖiÓG\x0015\x001c÷"D_Óô°Ü6UÎä®ñÝ¡*¸ØÒzªà~\\x0000{
!\x0004­\e\\x001dÀÛ·²1Z,\x001bç$
q~3ÌéûOw?ËûÒã	{ðÏê×çÊDòe\x001d\x0019é	qß¿zþBæÄ5'NqV5Ö\x0005\x0014Pï})\x0004\x001dô
Y~¯@JkÒíx¬ß\x0004)Àöþ
\7T£çÝ§ÿv÷íß\x001f\x0005-ää\x0001b	L\x0018mNÒ&#ö¤\x0017¶¨Ïç¯^þñöùy\x001a\x0013×8M''Ê\x0016­'\x000c\x0011N2ÌËCY\x00078Ã3ÌpJ)q\x0016½·ö_½\x0017æ³úÅùß\x0003qÍ\x0019'8óI1Z^PjÌ d\x0001´Àù@¿ÓMù\x0018ç
ìÞýë·»/ú\x0000ÎøüÄp¹>Hßr\x0010\x0016¸*A¾hD*=%çsÏßê³7ÿáõã3å\x0014\x0012Ö0\x0001	TGX3d	ZÈ\x000fI\x0019ÓqH\Câ\x0004$zËD8å
æ\x0005\x0012íHý¦\x0007x2¬)Ã\x000c%\x0018¯«gáJ©i2Û\x0015>ø:¼×.?Ì|÷*ÌêJ\x001bÓï^lsnz\x0014¦`ý\x0016ÖOÂ¢]-pZ§#\x0019Ö¾ÿ¶Qaâ¶\x0005<öOVÿüíãç_½ûø\x0004e\x001eúÚN!^UÔÏê=½\x00149¿Húç\x000f/_¿®ú=¸ÆÄ\x0019LLõÄÉ·¡õ¤ÑÈ??+o3¬9Ã\x0004'´îëÂ¦U+50:\x001b	\x001feÂÂqLZcÒÌrBÞëe9E*¾\x001ec+]' \x000b·CiÍf8Ù%Åºò(mÝk½¡~+Á=ÅYÖeæ³g¨9\x001dvQ¬fÄ1_·gÔ\x0014F8}oí3æÎG+ñD\x0002«´\x001cu¨¤m}ò\x001c$t0\x0001ér0õ,Å±u5\x0011@¿º\x000c¾½ÂW÷ºë½çÝÄ\x0006
¥Þ2±!ñ\x001fuþ¨¤©ÿ,[\x001dÑIÔ{Ôg<}0×Ä©ª\x0015ªUd><ÐàDý©Gýi\x0006\x0015mªÔZ\x000c\x0015¯ê6Çxþa\x0015<ÿû?þóÍ·ÿúÄ\x0014f>£×\x001eÙìä9+Ö	T¬h\x001eüùÁ7\x001f8³ßA\x0007k:\x0018¥ã#F4\x001cÄî²J;kB»éhMGÃtXo?\x001cº¨.\x000cg#\x0002½¼¶\x001dk¸8\x000cG&ÄÈ®¦-\x001dhc>ø³Ê3»ÙÒ-²Å 5P\x000e2JMèÂ&\x001dæ©»éÊ®Ò%¬Y\x0005Ó%§M
$]ïJ·UÖ\x001d[IG¹n^éÞïõÆÕA1M!þ®\x0006Â¡Mç{o2ìNDz¦\x001a,É¾r¶hÍZ2ôê\x0010^çNü°?Ézß@ÆÏ«Q`Ò7H¿-1\x001fÅÃ\x000e\x000fGñ
IÕñWë\x0018\x0017¼\x0014lõ9\x0014è\x0016\x0006­6\x001a~Ñ¤+Ú`\x001e¶T½ô)\x000fgOáÝñÁª\x000bdÏå¤%\x001dÖ¿|ýøë¯÷»ÿüõæÓî&:Gîd7T¥½=>è
~óþå»w·?Ü¾~ójW¿C#51L\x0013³;4\x0001MIlkc\x0001o\x0001{ÑÝ\x001d Æ51N\x0013gØ"2Ú3\x001c\x001díh»\x0003ÄaM\x001cæADöê\x001aZet¡Uq¸(à\x0001bZ\x0013Ó,1¸¨=j$Ó\x0008j©ºKTìy:]m\x001bÇ5p\x0006®³Ië¦pR£°\x0010Û\x0015\÷:\x0000ÖÀi\x001e8êc°È§[ÕwÐª\x0014àj{"¯ó<1ÄR]â¨ÏâÝm^ÜÆet¬ðUï¢\x001döIGúú2(²PIz.³o<)Gnõìèó´n¤ßHø*"1\x0008(­ õt\x000e\x0008\x001aÍ0PSºtâÝ\x000fHk@\x001a\x0006,íÒ\x0008êë\x001adãý\x0001Ù#xyÇñ
%ö1ÛíFQÄp«¹2\x000eXÖe\x0014P\x00147uâ´'ÔÙ°¡è¬.ïEó `wÅ^ÍD~\x0018\ÈV\x0003Y Ü\x0018-¦\x0016âk¢§Aq+±Ä*ç}·ÿöä_SL2F®VF-â#\x0008mGiÖwûÇG_úp+\x0012Hè>4OzR4\x0005"]:(¹ÀùsäN6Z³Ñ\x0018[*A%BSB»óë\x0001-mÍq+å6Æ\x0016×lqpÝ\x001cÖc¬ô
·><2\x001aòGÐÎ\x0017XãV\x001a\x0014;iÐ}k ]b.ç5 Ù@\x0015\x000cÏËªî]³²f+l\x0001ki(/Y4i>
¥æcÌæÎ+îdó½\x000eÚ(yÔ$s°k\x0019\x0016ùRÂ@¡­\x0004ÿ \x001cvp8\x0006\x0014µb>Î°UÌ¨Û
ÓùW½púA3åS«
±EyÍ\x0015.©hôøÃù3÷N¸Î\x001cü =üÏÂI7ó\x001a.\x000en:ù®9ëwE-òïZì»^¸(Û\x001b\x0019N\x000f\x001b56Üý&Ãö¶ÂémÅ©Öë»_>þzóöã_î¾ýùQBiÊ©½ªà\x0015}\x001fàeuZKàRùÜwo^¾»yûòûç\x001f~÷4(¬Aa
4ÚqÏpE«{	Û¼ð\x0014ÜUHqMS¤>ê1óS´2*þØ6§³\*K\x001b#
kÒ0E
IÛJøã£zEjÒ\x001c¢5}©ÐoÖ¤4E*}mº¦\x0001t
;-ÿh]SºÎ>kÒ8÷õ¶\x001dpè,Z¿¾·9_(N\x001b#MkÒ4E\x001aHaD\x0015î\x0019©écèñ*û4¯IóÜ>õ5µà5¥ \x001dÿ4n&7N5iÝ§úõ9¹¶T\x0004«í§¯Aº\x0012A\x0011Çïæ\x00165jÈ~êõ\x0008:­»ÆFõ}\x000bR*û+SÙ£=¡ÓÊ\x0000\x0014ßz
Ò.Hù¹(%*juMé×÷Ö(\x0013qó:1	Úy~?çúe\x000e¦\x000eiY5Ú]lÞ9m'o\x000c¢°yz\x000faÓÕóÃÝ£÷(CoUà\x001bù¬¨\x0005KlóÞ®ïâ¥v\x001f?r·hdaM\x0016ÈH 0X«©q¦Üæ!Áy\x001bß	\x0016×`q\x0008,ÄZÔÙ©õ;¢3ç;Éò,\x000f±]èPÔô\x0012Å\x0014l£ï:\x0006æ»]æ¶YâÐWôk6L>­/äCÛÌwÛÌ\x000fí3>3FYØÀb(Ú(\x000b8Öm4?´Ó\x0012d½½)Èi
\x0002úåÙb\x000f¡u;Í\x000fmµ1/hdmk`-^
É\x000e´\x0016æFÈB¶hì(
|\Õë`,é\x0015@ïk¬ $EºïhVÀç@u¶èR·×.´Î
`È
\x0002úBÆh®M\x0012"oÆ2	}\x0006
â¶=6ÖÒµ¯ò»\x000c¾¿û&1õ÷¿|þúÓ/ßd:ÎçGÇãPcÊry¨hÕ¨ê²\x001eRü\x0003ýyÿý¢\x0002/s¦oèúû7¯ß÷æËyýÈ¼\x001c£5=\x001c§§
mºÀ«ò\x0005\x001f¶áºð¸Çð!i¡c&çT¶¼#[zÚ^µ\x001c¥\x000fkúp>f}hcú¢\x0002\x000f$S\x0003>nUGÒÓ\x000eÒK=X÷ðÌ×r0\x0019bðÛ«£ði
\x000e/½¢½p Cßx;¾\x0012xZyw\x0000Tb%³¥j.
G\x0014q\x0006º.~ï-\x000fºKrA\x001d\x000eo!£÷ö|Ëôtõ0}ç-ýAwI]\x0004Ýö)ØY_4D*¾T(]\x0017¿óþ ÃÉD¤[¿éf\x0013x\x001d¬ÂøÛ®£øÃô\x0007=¦h\x0018Ö+Yf©éÅuÈÁ·hueüÎcú.¬u9eéµEµ\ÌêðãÆ£ø±ÃÇðE\x001c \x000ePÌQ^IUr¬ùM\x0019s]üÎåû>2IZð=Z
.ú\x0004ëÒ¾\x001c_ü¨ôÉÎyí^\x0006É_\x001e:§\x000f\x0007¾ô\x0017£/zª%,ÚrÌðáº1\x000b:·	ÇÜf¹I±¦øYNuççì5K.\x0012#GðÏ2¸à7/|ìØl\x0016Ùý¯7¿ÿö+Ã>UË\x001dbµÒ,pzàZ=í¿ÎLøº}wóû\x000fïîñ\x000e_¿yØ®ìa>v\x0015Ï-Ò\x0003\x0015¯
ÉÞ\x000eÿ\x001d¦Ã5\x001d\x000eÓ¡Í9\x0008>kk¼T\x0018k¹.<¼å{üÓ¦5\\x001avËGj´Ü)¢nC@wn\x0014ÞÐâå5_\x001eåKK\x000bßÂ\x0007YUÿeF{´Å;7\nÏw[Ï\x000fï½È!@\x0001©XÓYD\x001bK~óN·\x001f\x0010ÂVè"¬Ë£¾Ý|÷Ë·/\x0011·³z´ÊAÆMYOFÑ×ÏP¾Ôwç\x001bä>Ü°yûýÿOÝû-çq\x001bùß·Â\x001b\x0008\x000bhü/\x001fQ\x0012£0E*Jrmö$EËÍ]ôRbv£½=ûÕ{òÖ¾ïé{\x0007¹½·\x001bè\x001e\x0002Ãçg03µÉ®-Ñ%ç\x0003\x000cÐh4º¿M6çé\x001dÄ5v\XG\x0001ÎpiPí\x0014yÅ\³»2z\x0019uª©Ó\x001aj\x0018ô÷\x0000=³ÒÂÀâUD
ÃtØð²\x0008»ºOÙ&åªÛ* Z§R2fÅW¸\x0004Ç°[Á("¢O=2ópô÷ÿ'ëÍ_¯?MáZê-\x000b\x001cqÄË\x001f×ÍSÿI	\x0004¸aâïO¯Nð4=ýöäü0&Ô°\x00043\x0000)·dL\x001d8¬Dm®%Ð\x001dvvì£´5¥]Bé¡$Ç å ÜcÜÐ\x000ewâzJ_Sú%hÆ d\x0019[¯È¢eJ|ü\x001b|òXcÆ%x^YÇúØ¬|7´ì¥º\x0015Ê³"|¥\x001c½ÒÇp×ß|:$#¨JJ\x000cÅÅáXTïDÆÃì\x0014[Í~è7¸ÕOÏ'eký8ÍÀ×½V:(Iá)­fw\x0019÷¶\x001f¶ùî^\x00033AM\x001cËÈÅVF\x0014fîn¾|9¨¤É,µì-\x0019&Æ\x000cÝØÞ«$öúäâôýû)@ ¡\x00050Ôò\x000fò
6	å^­»\x001eJSS\x0005Þaàd\x001b¥r
ç,H;\x0016ë±#±7xûôø÷ÿûþnÚûYZ$\x0017\x00148#ùd>\x0004NVNAï©Ìx·ó\x000f///\x000eC\x001aÒ,¤RÜP ý sæ¹| Ç>ô\x0002H[CÚ~Èä¸S\x0007-JÈ\x0010¸Ä\x0005'aÀH\x0007£«\x0019Ý\x0002FeK#N$ºF\x0005øTéI\x0012ßû4Ý; c
\x0019»!=¥ß®áÔ_î&9°àd&õ³°N?¤n¾¶îÿÜ^ãT\x0016{\x001eñÖq\®ÉK«\x0001P»\x0013» Ô\x000b¦RÓVbÃ\x0015ri°eéRô×/Ê§^¦L\x000b();¡<Þè\x0018¤\x001b¡2¢\x000fc1ò\x0005Uº\x0002Rê§\x0004Í
¤CÒ6¨\x0014¨*þâfÒQ\x0007dcÍ¡ß{ðZO-)lr\x0015­çË<~ù}baO»5\x000eF§"þ`\èùöïÿÏÇ\x001fo\x001en'=!üÜ®¼·DeJ_ÚÖ\x001cpØÛ¥ãü\x0004½ <&¯Î&<!\x0001u5¨[\x0004×1,Qf fí(Q¹8~ÖêâÄé8°	Õ\x0005òõõß\x001e§m9xÆ\x0004ÅÈÑ'Ñ\x00024#\x0003Tó×'ÿüá0\x0014ÔPÐ\x0001EÒ®@á/¹M\x0000ù¶Ác\x0006=T¦¦2\x001dT¤:Z"\x0002j;<Ía*³ó"3ÊÖTv6'\x0005O\x000câ@Úv7SÚDtA¹\x001aÊõ@c]Ú\x0013\x001e¾A XÐ
\x0002)*-¦ò5ï Ò¸\x0013ËZ§\x000c}NÑ ú\x000baËÖE\x0015kªØCÅ½*\x001a	4E`õ3\x0008jìMuPUWN²\x000bêkÙ#ÙU`ÙÕß\x0018.ånîÉl¡\x0015tP]Óß>ÜÐUý»ûÉØ!µëàô\ÒÂ*)v&\x001cX7ªñ\x001b.éø#º¨¿¸
\x00192¥i(Í\x0002JØÏ%â\x0011Õ çà`O(¡Ò6v	¥£0GÐ\x0012#5KÁ;{Ìôaº\x0006Ó-Á\x000c"M\x0000ÉÜb nG^?j"µ\x0008Ó7~\x0001f\x0008Çg¬+ÔL\x001c¢ÄàãÎ&.ó(Ñm}\x0011üAå0âÏ\x0007\x001eº¤a¯Ê\x0015ÐüÐeå\x0011Óx¿Ó!a¾·é ¦^:[\x0014FÎ\x000foäñi§ÝOgj:ÓIç¨Ü\x0011]\x001aÞàì@·ó|Ogk:ÛOÇ¯nÐÐ±ûdvìùp®sp.\x0016aWÚ\x0000çÁxÛ\x0019J?\x000c§Ì(¢? =ñÔÙè÷\x000f7\x0007TGÉG`:MJWÜÙIÉUf;¶-=¯^NKQ0ø ¥·	þÛ;éam(
k\x001d©ñL7/¥O@"\x0003øu¥ÕûÚBÍå³5íåÃ\x0003#0´Ý <égaGqè~<Wã¹îÕ\x0007Ãôá\x0015È\x0002¯>~À¡@K?¯¶ã\x0013Ãªgmk^Ýþð8}Å¶ÊIã\x0012\x0013\x00147­ñÈ%­¬ÞW&ìWg¯?L)\x0003Ù±e¶êYËÃÆ±þ:1J9\x0007Ï~\x000c2Î:3\x0019]Í8nV3\x0011Ì± :Ù'\x00000LãTó¡F\x000cÝà=7Ø@ÆÈÉñè[q¤»¾1Õ©Ñ\x0006éff_ÐÓ{0ª?qOø,+¤z¿¼»¾½ûrôööæ@N«HEA£âà1\x001b\x000ej3~gBÒ¯~ôöìt²K§PBM	\x000b(q\x0011²ñ[ÜR£4©¢Òiç<öQÒ, 4AÊ
)u¬ô¥1__díNãÓGikJ»d.
=Ã/îD\x001b\x001eÒîV|è£ô5¥_².swú\x001e\x0002\x0014¬)ëÒÈºô~çkg\x001fe¨)Ã\x0002JUÎkîLR*©AD	´õzejÈ´\x0004ÒóûWrÀ\x001ao\x0008)ù\x000cÖÇõß[·vh!BÊÀT.'s)S\x0019ìÎ
ÿ>Êfë%[Öb1Ô
¥/Á\x000c6)mé\x001aL·\x0000\x0013|rOª.\x0013\x001aø©\x0001½7ØvÑÙìq½dëHï\x000c¥c\x0019öå'0ê³³Ø¹\x000f³ÙäzÉ.§¦¥=P«Iþèo5ÔÓm\x0003ÌØ`Æ%±hcSH\x000cÈzfLÉ\x000c¦®¢«×&¥®Ôd\²8}l5ãÃË\x0011$§zk®¶|gqªnóaI]TÒ\x0014=w30 ÇúY§\x000bVs·ã*Nf³\x0017÷éþ³<-ÞPÊõ\x0014c0)IVô×X½0xi\x0006ÌXâüòÝð¬H)×\x0001¡\x0006nÀ0È\x000c\x0011 ´\x0019òÜÆZÌ\x000b\x0008MMhº	½tJÑ\x001a\x0002\x0007Ì\x0002­P&±@?¡­	m7¡uüæ¨U|>\x0006*6dB5¾Jô\x0013ºÐu\x0013:Ç!Ñü=eïÖ¡_KèkBßOÈ¥ìHHu±ÜÑKâ|\x001a«\x0008, \x000c5aè_R\x001a£µø\x0019®C¾è@\x001aÆ~ÀX\x0003ÆnÀ\x00188vó9\x0017ãS\x0018V/ÃT\x0013¦~k\x0018$¼B\x001f¹ì\x0013tÄ\x0007À±¤Ù|@¼,B¸ø­5¾½½yü£7$ö~ ÿ\x0010.\x0016ÖY1Óï¤Df¬
]Ìß~ø§£7$ó>ü#¦¦4\x000b(ã¶Ú*?c,\x0007âdJÐ;*¡z)mMiPcJ\x001f%\x0003Ñ¹0@n0®ftýèÞ²  Bz©ÇsVúú /¹óQ¡Ò×~\x0001e4ÒE\x001e\x0007¹\x0000\x0013¯C\x001eÝYÑG\x0019jÊ°2*W¢\x0004>\x0007é\x0018gAH\x001bÌe¬)ã\x0002JD3ÜCEYÖ}wNìp7Ölî¢Tc;¤ÂÛ8¿\x00009K¿g*È\x0000n¬kUÐÒ\x0019pôR]LåìR0zOBHX\x0000itZ¤G\x0008\x0005R:)k\x0013w\x001eÚ¦¦4\x000b(Mîº¼ÛBi£ÄþÆÙW(mMi¿VJWSº%Ò^s!¨³q{]{*Õx{«ðä\x0003õ\x0010F¯XPìHâ<JDÀ;xtÍ£5£¨9þ ê®xst~ûÃÝÍÃýÁR\Ê¸+
_\\x000eÉST í\x001d¬Ûqzöúâôêrº\x001cW8mÍipM\x0005CÍuÔ9cÒû2xçp*=ºeSº¾Kt*_>ÜßþGùü·7ÛÞb¢gùòêòìÊ\x00028;ýçÃ¨P£Â2TôÔ#èQ±iµäójj\¼	«©YÍ2Ö$rKÈ\x001a8KÔj\x001ddZMØá´/`µ5«ý:YÍøiÏ§½·®?Þ\x001c½¾¹øáæóÑûûÇï¦+-X©|I&\x0019Ö¢5\x0008+(v¤ïûöüäåéÑëÓË«×§ïÞã6{1YkFÍøæ±ùóÑË¿ÿ\x0007êÚ\x001cjAÉWÒ>PDPÒ
+¾\x0012zP»%/\x0011ñåådU\x001bßy µOÍs\x0000m¢Î\x001dMbgÎZÏ¥Ê Æåbý©\x0006LÝV\x001f³v\x0003±|\x0007Riì!õòUÕôíóÎLÀüÐ\x0013'³¤eØìmìV,è'4
¡éB5\x0013:Ã¯¢Ö¤¡£.ì~%ë ´
¡ýú>r³uï>þ5\x0001íXQÔ_<<þr¨Ãèó\x0016Óí\x001dÉö\x0014ÏÒ([Ú6ÅàÕÞjä\x0017W\x001fþ4Ý[O(MMiú)©¹TyÇñÎJ\x0005ö12íK\x001aC©
¥©DrR\x0002¯o\x001e~¢ÞçGç×_®Ño{¸½9úÝÑGüÅÃdØ-å\x0000×Ä\x0018\x001a@»EÑ¥	füKÇâëÓ«7Ô	\x001dÏÇ÷,vuvzôâô\x0003þíêð\x0010R3´~\x0008àK	U@Iy ÷Tj	ôÇ!X]\x000fÁê
`%iê¹\x000cÁK
Ð3õùÕC0Í\x0010Ìú!\x0018(.v)c*½Q÷^js=c®\x001ekà6\x0018\x0013y°äÅO\x000fJ\x0016\x001f?\x0018¯\x001eB³\x0017ì\x0006{Áxºº\x001aà+\x0019\x000eA\x0002XÁS[\x000e
áãõ÷×¿<ì\x001dköÛ`/üã`Ç\x0015\x0005¶T\x0014<e×¾~¸¾û\x001eQ\x001cÒ§\x0001#M`
ZÔò\x0000DO\x0003¢,§Í¾\x0004ï×W'\x0017¯ð,ÅQLÜÙÇùû¶äï/ E·{Õ\x001bHR/J2³Lªô¾då.R_ú%¤!zîÆ¤Lñ\x0000JÈX\x0016N»ëzIcM\x001a\x0017¦Xîì4§Zz\x001c9;´°O»Õgæj7*ÇÕ.ã¾½þüùúÎ\x0017ªVä@<º)ÜåÈyyh3jÔçíÉ»w'¯;ÂÜB\x001bjÚ°6\x001ds¸Ë§|
vxq\x001b=¬vÃâ\x001dn\x001cOä£ýô3âöIûøt¬\x0007\x0001¯"Àk\x001biÔÁóì
Ñö\x0010¥qd>Ñ*XêU\x0018!±Y|UÜ´\x0012dÒ£ôá¥¬¦f5Ë¦5A\x0011SO´\x001cë:
¨à·V[£ÚeÓZJÊ
kàG.«´Àí8\x001d¥Õ¦q\x0017¡äª\x0012¸û_¦\x000fWÜåIú~RÑ..»W\x000f´ëëâòOSîpËôp\x0005	y\x0005j\x0018Ç>¼V"íC9=\x000b¸üXÏ\x0017u¾áÛæì\x0004*»¼¾»ü¶Î%SÚ¨Då©\x000f
K$s[\x001cp\x001aöì¢@'\x0017\x0017\x0013Öµï|Ñ¾[J×Ï\x001a(±¬\x0011â)ÄG¼ófÏ2ìdõ5«_Æ\x001a½8N\x001e\x0017$7\x001c\x0000?°Âè8êeÅË_»\x0004è6ØtU=Ãcéãäê¤¼\Sú\x000c`¤Z=z¾Ú§¤v7¦?:ÃÓèåDÈx¬Þeü³åI}U¿\ßý0\x001dAÄßÑÕäÚ$zîb\x0011fz3Ú;G§ïO.^\x001f¦\x0012Pzvª\x0019J¨Éóõ
ÿ¤ÛcÉ\x000fC^«QJæ*)ç÷_n\x0011ò§»/GÐ¥ûãõÃ÷·w\x0005ú\x000fxM¹ý^Éä\x0004¨Ëã\x00149K\x0001G²N&è§DÈ6Fv~ùþè\x001c½»?\½:»(yJGÀ+ÊÙ{ôN.$òñ( \x001e\x0005l5
ò¥â,\x0019x\x00141I*âø$];
SÂl5
º\x0013Z\x001e¦ð4Âª!)\x0015Fa¶µ£°õ(ìV£pÀ1+ÿ\x0019FaäßÑ%lí \=\x0008·Õ ¼ç¨\x0015ÁñU\x0002}s	¼¥q»Üµ£ðõ(üf£°R{ªæÖm8
\x0019\x0004¤m\x0007\x0011êAÍÖ§¸x\x0019ôsÇõ$7ÐdF2PËGáÆvÖíì«û\x0012úû©\x0012©æ@½Kó'¤¼¡Çðx²¾9½xôê²Ä}TÐøPãÃZ|\x001bè
ñCäì =7¾A~½5¿©ùÍêéÏ
W2¿\x0017%¶ £H¿»qîõü¶æ·kùÑ\x001f"K"ñÐv¼~¨jc~Wó»µüÑÉ3k@\x000bTü"<®eýÄéÆü¾æ÷«ù#Åû\x000b¿B\x0016tDðG·1¨ùÃZþ\x0014Ø½CþHßXþÁ=³+ñc\x001fWâk\x0005Ãò±N¶/\x0018)¡Æ\x001bó§?­~ÎÌA~:ÆÜ\x0000Ó3Wh\x001dý ©VÎ.µ\x0016\x001fý\x0007î\x0010|â"w¼\x001a(ÎlöêÙÝ`\x0019ÿw¸nrtJÎÞ\x0017´È4së×wÓòQ\x0001ï²äáäg\x0000kù¢æ1òVUvÔ&åû[¿<¹¸|?fr'î¡¯é\x000bE.­Íh/¼þég
\x0003ß?NøäÓ§¤éùá uxoä\x001awt\x0004`L÷ò\x000f'oÞR(èüòÃÛ)ÀB\x001aã\x0013`ø&ærÍ¿ÿ_U×£YM\x0002å\x0013jî-\x0001ÈÌ³h¥µ\x0004Îíè©¿nvôÔëh?®¥ $%¯\x0008.=)EI)<¿½C/q2f\x0011\x0013pzVIq\x0010ÈS]qaIïÊ#<»@p+·2>
\Ô©\x0014ûM¾þÓ$¾»~ü4Ý2Õ´£M×rb´\x001b9ç»?MÞ»\x000fçS³\x0016ÉÅÖC±ë\x000büÁ7ôÛoÎ¯ËcÎÍÑÅõãÉ
mÐ\²`]´8%²YE<7J\x0015pëægÓ£\x000fï§6pÊ/#éiöÐ¶ÑõâÍõíçû»£«ûÇi?þ#u­T>Z¢ø±AÚ\x0007øÐ~U´/ï./®.?Lxõ\x000cF²[\x0015\x0018ý¶,iI±Å»\x0006Ï\x001a\x001eN"\x001aÙñyd¥¸LÇ,Úâo¿y{ýåñ!¿'á¥é[JYîL!§Ò\x0007;zjwW>+\x0012ú¦6q£\x001c·'ï?\åÇ$¼'}K\x0019Ëï&8u¶ÍÆ\x000fxèÒ«ßÛÇY»Â);DB	ôFó)½$âLÊÛÓ\x000f3v\x0004c\x0005Uc\x0005ÕEo\x001aJ\x00035W-/pKÞ\x000czòk° Á\x000e,g\x0015KÁj0\x0003 04f\x0016pAÙ\x0007aà\x0002Ú\x0007!\x001b··7\x001f¹\x0013Ñí´àV4Û^'ªîg¹·¤D»\x0003ÿ¬\x001f[·g§/¹ûÐÙÔ:\x0003Ú\x000f$Ø5\x0010¢e§ènÆ£aO\x00075¤\x001bYàF
^=)ÖºQÒWÓá \x0019®§~ÛC\x001e\x0013«/¡ù¶Üo\x0006~9¹rNÑ
:hæ~ÛCG½Ç¸Ñ\ÒÔ®/Kl	[¥\x0013ç[\x0003?(\x0006\x0018\x001d¨·÷è~{ó0íhRXâÂ\x0001e%E/(RÜ2j4ÎÓÛKtB¿=½Ú¿%HØ\Xÿðïÿ-n2µ$¯yú0¾´¢{Jcß\x000f%.Ân\x0015?ò©G$¹Ê\!4¦s5[B\x0017Ôà\x0019S&g\x0000>¿¼¬:°»ób&èôøíIëJ;ò
½õÇÿ8\x0010ìöR¶­>æ\x0000«\x0016\x0017ÎíeDWäòÃ?íAq5ëAQ¡¨©àºþ\x0018ø	D\ÞÒ®dIP³\x000e\x0016²8j±_¢D\x001aWk8.Ó\x0001jÔ\x0003CM;9ýú\x0012'uÒ\x001f 83ë+å4\x0004]¥tó\x000fJkåGYÌ/®\x001fîïîrËXÌ\x0005¢¿½ÿûÿû·\x000c\x0014tðÕ2\x001d\x0004\x0012`3ßPpà2u\x0011}vyúÏò\x0017ñ«Ë}½
*<\x001a\x000f \x0013ônLÁÓÙd\x0011\x001eÚzWðL*Ïr<ÛàÙ><çbÉ:C<Ê)x\x0014
\x0015<XF§uõÊ?¨åo¾Ü~ASó·\\x001d´ÎiÊ^¶3\x0006ou8÷H§Ñùê¤ðO.\x0015Þ£·§ïÏÞ\x001fñÏ\x000eòÙÏvòE4ìY\x0008\x0003\x0017=Î\x001eõ\x0006A>Jd>(©\x0007+ø|Íç{ù¼-Í\x0016/÷]Î|EZåÆ+ñb\x0017{ñB ùØ§:re<\x0013åór6Är>Ý,?Ý»þrÈüqSi\x0000tF­\|ÐÌ\x001etN_@O½´}D:¼¢£½Ke½\x000chÃxóö~^øówíþý®o\x0002=\x0015¥ýk\x0003ÝGi
Ñ÷.!\x0005eW\x0013~l	?v®Aj²\x0011ØÄäs6\x0018Wºê)
\x001c®51ðçï[Äï;\x0011Ë9\x0011i>\x00191:¶Ñiµ\x0011?_·×vZA¹Òw.ûÄse¤ÊÁÍi¾çeð¤ÖIç\x001f\x000cº&x}¹|øéæ:{+ûöGQ§&*üÇåh\x0003'/Oàèl{wtyõæô\x0004=ýs¦ªjMÁ
]Xº¤M:R»;.óEJì\x0011DåÆóÕÃ\x0015k®ØÅ'\x0004OK\x0014.óÅö. Ï;>Ìz¸RÍz¸Hñ¥ìPrùVæBÇóeÔ3\x001fe>WuB(Õô\x0011\x0001\x0016J	32Å¾\x0013Ä\x0013\x0016-¬X`Ú6`¶\x000bÌÞ°Yô.\x000c\x0005¬h"!wkfÌ7`¾óSºÂU¹ð\x0014®¨V¬|ÝìHÝµ%ñâàøKÒÒç/	ÃåI}!X³%u×ºÜ¶H¡y0a¦¨ #W2ãó³«ÙºkOâébð©}Ø0\x000e\x000c¡Í\x0007=öÜ:ÀJG@\x0001\x0003Ý	Æ\x000e¶ìQ\x0012\x001cÜ
{!i¸L'\x0017E\x0006o)
\x001c\x000eVlIhÎHè:$æësv.4i1b)Â\x0019k\x0018t-1¤±â{[¼\x000c¦âpyK\x0005i®\x000eA*þAÛÂáêú»ë»ï'îÌ\x0000å9\x0014\x000f$ÈDRëø \x000cª:(Äò¯Nþtqrñê0©ÙL\x001fÓrãÓv8Ä\x0016§¶c\x000bÈlMfûÈL,\x0010\x001cçÉðIÜÄ\x0010jG{\x0001¯Ù|ç¬±a\x001d\x0008)\x000bâ÷DoW\x001a,ty=l\x0002PZ|\x001füâb\x0018¿nÒbÍ\x0016û&-D±\x001cÚ+}ÍlÖùÁ_kØ<³¼E¡oâTâ°!7-X8qf©í*¸f'è¾­@1AÏ§:Þá}Ù¤{Áã¨×Íkà\\x001f\|òÈ]c¸(¾P}.@kv©îÛ¦ÞªãbÛèqVo*ý0qÚ\\x001dJ]ÀÖl\x0006Ý·\x001b(Õ(òNµù\x0019#Ã9\x0010\x00172¬bf3@ßfÀÿ+)sä­s4ì¤ýª3Á¨æ´R]d	¿#_¡¨\x0013W	ðâ5O":UÓfi3}Ó(o¢\x001c\x000c$Sí\x001båUpt\x001aè®bk¶éÛ
	\x001c\x000cÒÉyÞ\x0012£´Ð\x0003ê	ð¬ÁU!{qýðýÍTL\x0008ÏûÄP\x000b
rXH\x0002k¸!,ìb\x001c4È^\½:\x0008^©º7·°\x001b]Ícõ>\x001f\x00115·õ(qÊ`ÕïÏnVW³\x001b^Íd5¡Ô\x0012knýY¹4XÝÎÃc>«S£5àTUBxsôúúîn2jî5UÇ@\x0012ÈO6\x0018q\x000cW\x0011QI|}rq1\x0015¬\x0014.¨¹`>W@\x0004qXTÑ:.7y\x000bÍ±ÛÍek.ÛÃGµÌ\x0015+\x0018çÏ\x0010×ùªì3r}ý!)o!a\x000bGÞÂb\x0001i\x000b/°4^`é©ïjÞ	\x0017÷ÿÂ}ê÷L\x0019è(×i2Ï\x0010Ó0eÏ.´\x0003..ÿ¸¿?}Ífj6ÓÇ\x0004\x001c³¡\x001e\x0008¡Ü'ÐG\x001e>çî\x0017ßÙl®fs}lAB<bË"#\x001eÍ­c\x000b5[ècÃãÖò=L\x0019¹V\x001bï\x0007¶ø,\x0008×Ã¦ÛõÖ·à\x000c5¨-ç­¦<¨òQ­xìx|\x0016\x001bïb
úØ¦UV&Î\x0017ÙÀËÍÚ©\x0019\x0010³ál\x0003gûàð0\x0008üª \Ä¬·²SYê`1\³âtß3Î\x000c·DôCñ­0&Þ¿×}ÖØÀÅ.83ÇÖ\x001cË³\x001f^v¬¬¹°j«>E3[ê8*bá\x0008Xà\x0013\x001e\x0017ÉÀ²A³U¡s«âÙ\x001e9\x0004\x0016õ0o*É{¶#»_#¬Ù\x000bÐ·\x0017ð\x0018½ BÎúÌ!°(\x0001\x0013\x001dEó»f­9\x0018 ïd µ\x0019¾PPâð6â\x001cEýì1«\x000b®YnÐ·Ü\x001cz\x001f\x001c;¤êAÞ§èh²#\x0012Ìóèù<8?ö)ýSRfûãýÝÇ\x001fo\x001e¦Î-j\x0014.prÑ\x0001ót6ì\x0008T\x0013Ü\x001f//Ð;ß×x«¦5]ì¤ÃÝÀÁj[Õ\x0014OÉ\x0004qz}|ÅÒIjºÔGG\x001d­Ê¢STEáùpà{,Âùöw6\uæûñ?.\x0006Iï¢®©ìØÄO\x0010\x0017w¹ùx®Ás}xV©¢nDxQ"êN;>÷ýJ8ßÀùN80E¸¢|Úz\x0006$H=|Úu»B7»Bwn\x000bkKOÔòe9(æÂðaÓNK<\x001b\x000eu\x0007ëTj-
ra:5|X÷ìM®\x000f¯µw\x0006ÏâÍãb\x001a\x0015cl%ÒI÷ÿutÍ®Þ]ti½tô\x0018V&Ï\x001b#>zþ4=\x000fOr§«Â'9²ÏGofòDR\Y}èõSòCÐÏ²õNß\x001d½Ý+\\x0013ÈÌ&
¡L¢\x0007ò$­U¦9sl
dç\x0003AIt§èÄ/DÊ\x001d(f°ÈÕDn6\x0011©³\x0016 ¼Y±SD·A"¯väÌ\x0003ò5
dd(¼úp¤\x0012ÐÏ\x00133è\x001d¯â³ª4\x0015ªÛs\x0014$¾·C²QÞ\x0001ÑèóWóú¹1\x0013	T³ÕÔl$e8F
¤÷Î{-¯Ë¤Ìb$Ý éHè*vAHd,\x0013¡I\x0010£éRè&Rq\x001c\x000fMäÇë[nk3\x0015Gc\x0017B\x000f^?\x0004¹`þs¬7\x001f®NÎöw³©ÙbÍ\x0016ûØÐ<)ñ\sÛâW\x000fÎaxîAÌc+z~¦zäPß§\x0008wVÀ¤"ù½l¤øJ3Kê±S@¢¶a(Ñ¬zIñ\x0013ÌB£ø§÷"Ù07EEr&!\x001e\x001bÉP\x0019B\x0007êÙ\x001fK4<=\x0012í¬«!M
i\x0016@âñ,y4\x000e¨9ñBÉI\x001d'\x0010ôSÚÒ. D×Z\x000fi+.HÚ@r¥ò:H_Cú%S\x0019J9\x001fM¥*#z'\x001crX6øà¡¦\x000cýÍâíl\x0016yºÚÍÒO\x0019kÊ¸`.\x0017äµtSViÇFUÉ-\x001d¹ Ã¥\x001f³Ù=zÁö¡\\x0017®¯ \$©.òôü\x0011¸\x001f²Ù=zÁöi\x0013K8Ó$lðÅu©\x0017,ÌQ	ç7)&Ïrsº1¡Y°`a\x0006\lBÍÝJº\x001eU´YÿÅÞ4óÑ£º!#:lÕ=naJ<¿7Øã¦J³`*)\x0003\x0005Üó\x000c\x0014IóØÒOÙì\x001e³`÷P.óC.Ñ¢l¥Oüów?üÛO×¢,½x{óxôêÔ#$õ5¯\x0005\x0004ðG\x0008FÕ?rRT"i¿\x000eP¹\x0005XÒh¡ýBÂ\x0000g\x0017ßfÆ\x0019éDNÊè·LøQ¡²¿\x0019
oð\x0019JÅrR[\x0017\x0016¿\x0016
\x0017é2I\x00106B¡«_7\x0011+Yh¦ÔêÂë
"Â\x0005Ê\x001e¯·®$L«Ð	}HK·\x0012\%lLPÞ!É¹ePÿq«¼Ó»WTnÌñ×|SÚI\x0015H|¿Pá\x0007³ÙJDÊôÎ\x001eªµ`r\x0010ý9TnÇñíÞRC'¿ýú¨p§ø>*
çGÕdðk·ò\x0018\x000cmkuyÀÚñ<«ésø\x001bÜì¶R¹¡Â^(\x001f\x00127)I:\x001auWO¡<3àLiØ½ªÞq\x001býsUqíXW_\x0005×3cõpíXñ¿\x001d×ïàßo¾ì[_¯o\x001e\x001e\x001e¿ìçû­á¢÷þ8\x001f9Añk\x0007®yëö®ùÓ««\x000fïgqí²[_\x0003×õõUpí²¨_\x0003×.úqýlÜcü÷}ëþü\x000cï=­C@÷/oG VèìÕ8_¢÷Ö(Pû ó\x0013ê-<\x0007kÇ²ÿ\x001a°v¬ú¯\x0001kÇ¢?7µ"Ä·\x000c¼\x0002¹â\x0006zn`Þ»¶æS=sM¿ÉÚ±\x00133,óð³UÛ·\x0011ßÜ?Ü~út·\x000c
+9ÎI'jMÑ*¼`p\x001f>\x000bV¥}ßñÍåÕÙùùåÅ,¸\x001dÛñëÛ±)¿\x001e¸\x001dàë{vSûÍáþþâ\x001e\x001e÷o»ÛýdÔS«tHÊú¬¹û4J²ÕªÔÆì&»8µs+üöX;¯\x0001k±ýÍ°î\x001f~øñ½^ÏË\x001foîî÷{cúµåì¡dlp¥\x0004<&ëTá2!äúÝ×ÓË	w¬\x0002Ûyü\x001aÀvÞÛ~3°_>]Ûï~Þù)³<\x001fõ\x0007¾ÙïXãº*KL
e\x0016§BÏ:\x0014!\x0017´`\x000ev\x0006\x000b³@\x001f5\x0003ÞÍÔ?åW\x00036>/¿\x001a°ñ\x001aûjÀÆøW\x000366¯_
Xü&w$ùJÀnn¹û×ë}\x0006¸÷\x0018±ÄBv\x001eJ60\x001a1ã%^Ô¾ã(kpÏ@ÚaZ\x0013¤»/æ»Ï»*"]Ý?þró°?\x00040\x0010U"\x0008½3ùÜ¶Tß@T¤ovC]]~øÓéÕ,®\x001d_ï«àÚq\x0005ùí¸¾¿uù·z¾ªÎ4M=±\x0001\x0013Ê8®¯dI#1Ç\x0006\x0000x}YÛ8øu'§\x001e\x0007{/âÿþéñçûzQ\x001fNØçÛÙZZå+¸¥îVÀNq0,©\ï&Läyw65O\x0015
ÏÓo¢>ýðãçöù3\x000f7_¾ì³A®!}+J+1­SéhI#Ýì1W§ïßKYVþës\x001d.Ì\x0001\x0016TÏqT(oãK\x0013/ÄÉÝgºp~6ñÇï÷íþ·®?N~-çUQnJ6ôµ(i¦l3ö<xÒg;y¿Ú$Ô­\x0010Ê¤X\x0013$Üæ\KH\x000c\x0004KªtýLßÿåögõq´³Ð
}ú4ÅBÂ\x0006\x001c	Ä\x0015¬,Ú!±B¡yz-Öçüü0ÂÓ:bâ7MG)©±Bê3@Äù\x0010x ÖÙå\x0007Ò\x0002~§û»¹ßû\x001c
kòà¿Ã\x0014A\x0003\%àË¡gÒÊ4\x000fY¨¯./þx¹ÿ-zÀ\x001a\x000bz°T\x0011u)% ^\x0005¯SÊ\x001b+°Leæcáç)eÒþ\x0019\x0012ûº¢é
,[cÙùX&ÄÒ=\x0005§ªjËl\x0019í\x000bU¤åT®¦r=åJ\x0015
MV¢öAe²JN\x000fN1k¯±|\x0007\x0016\x0004É¢^Z¶Lõ\x0014¢R4°\x0002+ÔX¡\x0003lw	\x0005á¼d}Æ\x0002Ë\x001f1Y­W`Å\x001a+ÎÇÂ3ã8pÊS_LJÕÊ­ù©J=seK
¡â1S \x000c;%8Uu\x0002F/V)U\x001dsE%\x0006Å:\x0010ÿDá\x000crjV~\x0005Vká;L|,ò>t½é
²\x000f]Zñ\x0011ucâuwÆHðÓbnÙ8ÀÓeÕ
cª\x001bcª;¬©³éÝL<fÊ	\hÎ8½Nù\x0015\x0006B7æTwØSt$sÌá^téò+DÝSÝaO]Tâ\x0006GåÅÌ»\x0018%¡Í¯9}tcOuA%gØræ¦\x0015\x000fÂy±\[ÕØSÝcPc® ÏÓ\x0015lI\x0014G®Tº¥à\x0013Ì
;¯\x001bª;l*-)I*E\x000b+\x000bñ3BZÁ\x0005Q\x001e£rn5qá)7¸<÷GÉ!+¾#4V\x0015:¬ªK\`´"W\x0010+ò|¹&³«u{¬jÒ¥\x001b\x000fÎ\x0016	\x000eÉ|±\x001fVB¯8 ñ¡Ãuö
ú\x0011]ýìq±\x0012\x001e­_ãH@cë¡ÃÖã÷"ÿ!ÅÄòdÅ>*^æã
ã\x0005­\x000e[ïK#%â¢2'v%<Û\x0008*Q_AÕzè0õh<mZëÒªPá#ê\x0015G\x00104¦\x001e:L½×Ü\x001aâBR\x0005\ïÔ×ÕÕØzè°õ¿ò|5¶\x001e:l=ÍWnßó\x0005^<\x001c¯ ó¥VØTÓØzÓaë½6åÖóGàïh<Ûz\x001fÜÝh\x001a[o:l=M+ß\x001e! \x0004I¨=c/j
WcëM­÷:¤äù
,aHó\x00159xÍ2\x001aK¹\x001a«jz¬ªö\x0003WéTSÖTÍÒsm)Wc¿LýÂÚ3\x0008\x001c©\x0006\x0015,¾\x0008QuÜ
³j\x001a3azÌ\x0004Þ\x001bCÉù6Z
æË\x0001_¢v+Ìm¶£íÙ\x001b¢'ô²¸Þó#¥NÖ®ø¶Yö¶gÙ\x001böìµ³p¬\x0005Ã¸ ¨#Ær¬6\x0008×³êÁ\x0012L¶ªTä#Qr÷uóÔÍÕ¬zÛµêÍ±/>\x000eþÚ½\x0015®ÀoÍxf®°ö¶Yö¶kÙÛ"¨B¾T\x001fÓwdªí3Û5Þõ,ú_ªYò®gÉ[%·
êðl*jáJkb\x0012®Yó®gÍÛDo\x0006\x000bo³ýçÄW.ZÕ,y×³ä£)bIã5¿´Ê¡8@b\x0013A×ì5Ï\x0007þ.§,TO\x0008ô¯ã\x0015c·tZ÷áýºñBÿ\x000cÏwá9ü¶ü`oB\x0011x¢ø8E\CgaL\x000b¥Î&x:ÄS,=òÙ´æÝÊ>£ëûÞ\x001a±÷ò'-îÏG§\x001fï?Md`àù}X¹\x0013\x001b\x0013\x001eK\x001cÖô¡Þª,Ñsúòr¿>OÅ\x00045\x0013ÌfàË\x0006uè9N
Q\x0012;Ôª91;LÍdf3\x0005åK\x001c;æ\x0004S\x001bØ§ÖÍÕ¨\x0013ÉÖHvþ4\x0018KäyrRËì¸Ï\x000bÍS\1O®róçÉx\x000eé(êL
1\x0016½ÉØI'¯üüòQ²H[³ØÐ\x0005ã\x000eÎÓ¯\x0017j¨ðuLTªÒ|&i;LhÝ]YåÎ´ææØ\x0007¥[\x000b5ßDEmÅ\x001c wC½´ÌYÙ\x0000MÔòU®U®ç/ó\x0018]\x001cEb\Ó&ÉG^×C5+JÏ_RÑeå<SÔYÚ\x0014*\x0013\x0007Ã©â
Ð~Ù(äÓoæÒÀÉQèXBqk"¥µÉglâõsÑÒøì{êCñÇë»£W?OA\x0004\X>ñ#\x0015 GJ\x0005\x0000\x0011¨¡úãéÉ\x0005\x001eÊo' \x0006(¨¡`>\x0014KFÃA#ÏF+³ÉÔL¦Éó\x001dV\x0005@'A3Tò2Q°ÉÖLv6\x0013úSÇZ¢$¶Y3|;3¹Éu1ñzÂ¥¥\x0007$Ø@+æÉ×L~>SL²ñH\x0019³\x0012-ðZãÝuÅ
5Tè
òÈOÇ½a(Ëî\x0014°âëÅ\x001a*ÎBnM÷x\x0010òD©É¯øx©FJ\x001dóÄ
ÐéV\x001fË]æ	Ìu¡ªTÄ©6s'J\x0015ÍÑ\x001c_\x001bª\x0002hÊÝ\x001eªÖÏ·æôÍ@æÊ8.RqK5«ñé×CÕXs=ß{ï$áÀ.]\x0005c2ÉÊ\x0017TÎ.§jl§î0HUÊÌ×©¢\x0012(ãC5ÆSwXÏ¨Å\x001e¿\x0011§VÌSc¦t¢+1¯t2YéC(\x001a¬\x0015û¯1
ºÃ*ÀÇ·±DºcNP,L°ÜtB³ù cóQÏ\x000cY[?\x001f÷zF(mo>hÜ\x0016ï·ø`$¸áñ@\x000eFLº\²R\sÌ4\x000eq>jÄ!Å¦I;®¬v-²\x0018VA\x0018\x0016¼^q.ÙB\x0017\x001bµÍð;g·æx\x0006\x0018yëøº-áÁj¡¤´Xøè\x0014µh#¬ ,O\x0019%5? \x001d®\x0013\x001aÀ \x0006ù`+f\x0002}åòT\x0017S\x001c¼\x0005÷<\x0010ß\x0001fj0Ó\x0001Fêu9}ÐÍ£Wt
9¢'ÃÛÒ©\x001d±î\x000e0[Ù\x000e0í,5¾,3æâdRJìªôüQ¬Ë×\¾\x000b]+h´ÏÅQ¦ºóC^Ùóü­\x000e°æu ¬ÿ*<g¥É¤¥R-BËL¼Akv¼÷tÁ}¹yháè\x0007ó÷gân;Ä7\5¢QüÖdÍæû\x000e]¤Æp¼ éÚÃõÝ÷\x0011ææûýå?:Æcy]Ô¥}\x0017µÀäìOêª´³­h\x0007^¼z??}5\x0014jÒ\x001dbI©
¡(ré\x0010¡<9âN¼s©\x001fJÜ\x0004ÕÔ¨ÏtÖ¾*T[£î\x0010³üP]:VåùºP}ºCó+B
5êXNè«@¥#l\x00144nxË})~ú~ñâþñáÉ·áàM\x0012É¥C\x0002¦q¸4÷¦xó~ñâòÃÕëÃP#B7"ú\x0013\x001e8%\x001fFÞÉÍ¨go\x0005ý¦F4Ýø±½$Õcàâr9\x0019\x0008\x0017\x0010ÚÐv\x0013>ðwÃ3Â\x0000èÆO\x001bý®\x0006tÝè§q]\x001cIÓYþÊV\x001cHc6X¾Fôý\x000b\x0011¤\x0016¢×½§HðøÑ£0Õ©P´ADÿôþ(;Å_KXÅòÈÞ¨nÄ¨9ÙÚòÈË\x000fòòg\x001d?Gö3¶6±ß(ºÀåãY»;X^Ãvyvc^ÀØl\x0017½`¿ü\x0003\x0018CÃ\x0018¾JÆfÇèþ-ók2j5
Dà\x000fê@ÄÑùã]i\x001eµç\x0016¢¬K\x0012ìÂ½\x0002R»#ñûôèüÃÅþÖQ\x0015\x0016ÔXÐÒPÃ\x001csNs¾~Â\ttV`\x001aËÌÆ"BY¯o§Ël%pC¾Ý®»þl,[cÙ\x000e,ürì¿\x0018Ê\x0000/TÊ\x000cåñð<\x001bk>«©Ü|**¼(5+x\x0001OR\x001b¢ÀódE»£öh>¯±|\x0007Vùp\x0019Ë;	\x0008&N,PñyVÝ|¦P3\x000e&êßÀz4èÊ§X­¼åå\x001e]ó\x0005c\x0015{°<iêì\x0005eiâÕþtÌg¥æcÁS$PÒRYXz\x0008°£`²ÃfÕq­b·ê¸ÖAÓe¼<æ~#°Eµ\x0012¨WaGñþ|:=¦Ó}tÖ\x0005£&ë¡8Gá),ìÈÜA§ÇÇ®27I\x0002éÍõméª¾çTk¬éW,å\x0002§YkãÓØ¯Ì}rßío©^qAÍ\x0005\x001d\è{\x000f·\x001az *_ÓÄáâ¥Ó³ì¨\x001e0S	ÓF¼Ü¨£È\x001bÌ³»\x001e,[cÙ\x000e¬\x0010´X²\x0010¢¬/jL)\x0017\x0004·êCº\x001aÌõÌ\x0017}ÏÓe(^_¦Kü\x001c\x0013§ÞõpùË÷LX2dÁwÈI%]æË¹gIË=\¡æ
]óåJ{D0/­¡¼-\x0013â³\x0004¼\x001e°T¥\x001e0\x0007\¢«"º\x0015¼Â¼\x0015õ
TX\x0001V\x001dKú)dæÔ\Â¢Bv>OÙÆ?O¤ì±?_·svÝfÕ \x0015A=µxÒ`¸·ÇeÛRÝ§ÝúúñòþñÓõÝd\x0000?àï\x0019E¹6¼îPe8=zyùáüäbªIÀÀ\x00065\x001bô±Å g9}\Çä3Þ\x0004káL
g¾®³5íd\x0003ÖUÆÉrs^\x0012\x0002Lò»¼\x000e6W³¹îy3"Ô©ªy\x001b:wÔwÁù\x001aÎwÂ92¢¼\x0000N¥p^ºí(HíB5ZìD\x001b²üÑZ<TQ\x001eºµ[¶à¾Ã{óèQ\x0014ez\x0014½.Ï´Gß^ÿð¸×¸e\x0011¯+\x000eôÂÀ\x0012\x0017Ö{éÊ¢¡\x0016=)´Gß¼þP¶1\x000cÔ0ð\x001bÃ\x001aÆü60èL}\x00189ù¯¯÷+U'jïÎg£Â@¾µ¡ì\x0008vz`¯O&$ª\x0007&¨`6\x0013ÞkE.\x0005ªUÌa&+:kª4ý^Èdj&3¢FRÄJ,¤)	ÚÃN7b\x001e­ìl&R\x0014ÃJ£ô\x001c	\x0008^ê³ßyß\x0007åj(7\x001bÊØ|$ãÀ\x0019AÔgj·Ã5\x000fÊ×P~>T°r/s¤Ê\x0015¥2R¤ûö8ôó B
\x0015fCYûT^\x0017
o=«ÄÁ%µbÇ)Îg
CxÐá/cùzÖJ%NÔN?~\x001eTª¡Ò|(3´y¥\x0002Ï9SÒ{vÑL¡\x0015×ãóM\x0017©á£÷\x000f7×G¼~¼XS\x0014\x0012)-íÐ$Ò\x001bÈ«±¦V Ã¿½ÿpuzòáè'\x001f.D\x001czÌ\x00025\x000bÌfÁëæ{!*\x0018¿ÿ\x0005\x00166Ð\x0004jÆ(;Î7Ý¥Lc#\x001a\x0005ãÇ\x0014PªJxxws÷å6gí\x0015á*¯U\x0011L£X\x001bjf­è\x000fGïN/Þ^Md´R@©*Åá \x0014e¯	\x0014\x000cµEÃÞèW@\x001aÊtÌ½OÅt2QcjÔ³+ü\x000c&5ÎÉU%'÷ì§¯?.YÔ!âèÛ©þ;I¤¶r(ó\x0007QP×¬½y{òî]Éü£&\x0011Gß^Môß\x0019\x0010¡FnD¡\x001c2Vb\x0010H¨Ýº^H=®x×®½7¿»¾½ûrt~óÃþ/èìóa°îÀâAâÌÚí¼É¼;9» \x0014¥×\x0013\x001fú;åãÈáÙV<ô7×·ïï^<<~ºÙoOiw²\x001cV&xð¢\x0014÷Ô:w2AÞ]^\x001c½¸úp~Ú\x0018Tÿgø×øó¿íéExtuýñúÕ[­ô\x0004ùöæËíß½ÁÏ7ø¿ã½¥Ïïòøë\x0000Çi1|×H£·§ïÏÞþîÍÉÕË?6M½¯N^|xõLÙÝâ÷\x000bu\x001eWùA\x0013¤!»ë/øÏ* ö·×\x000f×¿üîóýãçß½x¸½¾ýD%±8}\x0010ó³\x0019\x001dG´\x0014ùÃø Ò;\x0018Ñ¾=¹:ùÓïÞ]~x÷»\x0017Wg'gçTÿ:|i\x001aÁéÅÉû=¹Â¶5¶]\x001dt9E³\x0001:N
V°K\x0007¾­°}íc¢	±\x001dK\x0012"v,~\x0012$r&òVØ±Æ+°\x001däJwjýáñ\x0011Ê\x000ed	Öí¨9h+K[­À¦LJ^$&Ò2ÏÜ~íh7\$\'Ü°2\x0013
6Z4ËÓíË3\x0015ªÆ[R7[R¯ØV©â2ÑtC¹ë"wÙ¦<í°-©WìIk9§5pVÉ1>±L(P1Þ[A}Ð\x001fÔÁÿùÏÿ:ýáÓíç¹\x0016Ðf³GØ$üb3õ0ÛÔ¾dÿÚæ«ÎÑéëó³wûî:\x0015³«Ý
fíXM \x0019Ã¢ÚÐ¶ÜÈ î_Ö½Ä¾&ö+U}#°7E$\x000fMÑ'\x0006Êä
19¬`Xj\x001e\x0011Úèã²
=Ç	Ym8Ï©fNk}¹Ù ³µåI ,gÈ®ú&ÐZ×ÐZ/§&¹,\x0015yy¨ÔzØÆn¶<ìt¦¶Ë©ÑÉ ãLÔ\x001eoì;ÙT$~:ÂvsÝlD½b'ªhJ²\x000bQÇ¢¾E>µ¬ê\x00186³wºÙzÅV¤N¾V¦Ú\x001e»²¬-^Úì÷z©cC\x001d×PsÞ\x0007R-±\x000f¢V²@Ð&ÔÐlFX±\x0019©ñ\x001a\x0010\x000f9×-S+ï\x0006j·\x0019u{¯8Æñp-É±$3\ôÛG\x00070\x0016hJ$Ù\x000cÚ4Ðf
t*¯4Õ\ðÔq8\x0016K\x0017m¨\x001bç\x0003{\x001f¥Ç\x001a[\x0010ôO5Ïµó s­ö;z½Ô	å&$$¢W¡NL
)
Ô\x0010hsX~ä8öNÔe'\x001aN7"äÍæÙ4æÃ,7\x001f!\x001958Ï¾¬i\ënçÍv¢iÖ´Y±¦©;©\x0011êXê\x0011º¼\x0011´_*B£äY~P+y¾»~üôSég?\x000b\x0019\x0014/èèÔp&j[\x0002´Jü~wôîäÃùýî+h¨¡a\x00054±#´Öå\x000b¡\x001dXN®[=Ð®v¡\x0003µAÓ\x0005\x001aOD] S±@ûÒ§m#èXCÇåÐ Þit¦x\x001ehx}IKÙø)Ð\x0017´ZLºÒl9óÀ¸T\x0011:ÑmÄÜnÂå»r¡sÁqa.Ç
½I>AoHí\x001bj¿ÚQÚv(Ô¤tm\x000bÉÊ¶q»\x0015ýt
Þe/5õå}\x0003(þ´\x001a\x000e9y=ÔÍ>ÔË7¢3®¨P\x00125kLá\"JAÔvCêÔP§\x0015ÔªÔùH²®C\x0018Ö5é®mE
\x0005å\x0016Är\x0016\x001f/Öó1î2Ã\ûý±ÓnjÓPås
o·1Ëò\x0016h\x0017Lõ¡àX\x000fts&ÂòCÑQÓyfEj ËÝ ãv'\x000c4v\x000fÛ=C5î\x0005Úù3bðWåæÐÆ\x001dð¨{ \x001b³\x0007+ÌÊ5#²\x0015ËÓ¢\x000bvXÔ¥Üf#êÆìÁr³G\x0019{5îÊr·uÖz1ÖÎnw0Bcö`¹Ù³è\x001b9\x001a\x0010]:òâ\k%{\x0011ôvÔ¦1{f¹Ù\x0003*ÈÃ\óqnµ~ëí¼jÓ¸Nf¹ëdÁ<%k[º\x0003\x001aç÷ÃÁ¸Ý3±6ËµUað@ÊNôúÉÙÛÐ\x00011¥6Ë-5=\x0006±zª¨$¢Õ\x000bÃê(òÎ\x001bQ7VÏ,·zÆ¢©æ©&2×\x000eX=s(xÚAm5m¯i\\x0000¥\x0010RûÈG¹µ&_½ámÀ6KÚ._Ò@Ît\x001c Uñ¬rOÔÛMµy*Ö}2!µÐ|ï~DïCÎ\x0019t¯¡¬nï´ÀÃ\x0016~\x0008\x0003
ÐTØ|>z³fB£Å|kt¹Ü&\x001f3ª\x0001J¼	LÚoú\x0006]½·9»i\x0006¶¯±ý\x001al=`Gî¸I
A\x0010\x0004;\x001cL`éÀ\x000e5vX­æ K\x0010Kj1Ñk~'¯~êTS§\x0015ÔTX \x0013çÌ#4³\x0006¢1\x0013²nê*\x0003­ð@7¶ñÅÅvÉA)$Cl-1kHî`ÒÍ\x000cl4\x001cm,.6»ZÌz~\x0006Öð\x000eÄhøAÃbµ!)s(ú{ E\x0005\x000c5ð®IóÞpU×§T\x001bW:¦Ò\x001b®\x0013`Ø·\x000bljà]ýfÍ0\x0019é°eÆJ<Òq\x0004\x0015abUt\x0002û\x001axW\x0013¡YÀxçâ×¢\x0006ó(ÖÌd\x000f½íÏ\x0007\x000e5ð®n0³}äÈ\x000fH\x0018\x0018×.\x0003+8èLÏ\x00055p\
FÙò¦C\x0011\x0004ØÈ;ÑÁgæÙÀºÙtzé®Óe/\x00185ø\x0014I¥.n\x0013`Û\x0000ïj\x00196/éÊ
kBY\x000ewxé\x0017\x0004$\x0010°\x0015p³$ôÒ5s<$La×\x0005îP=ç=|>qjwõÐbj¬b´\x000eE«ßø¨\x000c\x0013'½a\x001b§ª«QªúË\x001f¯¿Ü\?þõæaf®&)qsÀÀá%»¨2\x0018\x001aB¦\x000eÞND\x001aæ?¼?=ù@\x0013Ù¡f5ìYº$09ÊÝ,¯q¼\x0019\x0004Þ\x001fÎ¢î·5¼]	ø1ÀAi\x0010W&ÑÚæè¾F÷ëÖL.ºÈèÚ\x0002_ÈCÐåõ\x0005sæp:u\x0017|¬áã:x\x0017HA,Ã?fv>k3i¿]YþäN«qî}?»Ös@\x001cþ\x0001N
\x0011\è­;|ëI¯ôh·*-Nê\x000b*ÆëúÄwòÁÎÅ0Ûçå\x0014öÉÇ£\x0017Tu\x0018ÓÖv\x0001&=2s=\x0006Ufp~)um¹dÒÉékL¿\x0000\x0013´ø¢ÑEªÊi@)F©ÑØxó1c\x0019»1CÂÃÛðG§RÆãml\x0000ÁÉÇ©ÆL\x000b0L\x001f\x0012\x0013á\x000c¬fÍ\x001f=LFCçaV\x0006\x00001%'¢Ój©\x0015rArGñöì>yÅÙìtÝ¿Õ\x0003:½$2PêÞ¸ÿ\x0015rZ¥¥îm:v8³Ùêº¯\x0007MDo<ÅQ\x0003e\x0013&¼ù®át\x000b>»\x001eÒçHø³oÁÉÕ^«éüìMÒýF)%\x0012Î\x0018¤¸JÇ(ëÓ¨IW}&gh8Ã\x0002N\x0012¾æª$¼¿ùb@¡.s\x0003Û©\x001bÛ©\x0017\x0018Ï\x0017\x0017\x00183r\x0015\x0012ºYB	ÓQìyU8ëzÉWwÃÁ«gSG3NÔ]Îç4
§Y¸:\x000b&ä\x000e/Nq?`½\x000eM%6É\x0018¹îfCñ¨)5/\x000eGÑ\x0006\x0013\x001a\x0004\x000blR\x000c¢RÙWâç¸Ø\x0001¥Þy\x001bØ$hl\x0012,±It\x001däM\x0004/W^\x00075TNÆ-8Í\x000eK6»³bBôÇ²@ÜN3\x001dH:©ý¸²Ý»¶
Ûëë¿Îz!añ\x001cU9qpÜ+_hÑíÈç\x001e\x0002ú¯¯N¾q\x00084ÔÐ°\x0002:ò\x000cãÁ\x0019v4A³\x0005\x0008ÉÇ\x0019\x000fUs¡m
m\x0017C\x0003ÒF®ÒJÒ½+I»\x0008­&\x0012º»¡]
íV@»Rcí(ý5rù¬ã"É`"ìÜÍ\x001cjæ°\x0019í/\x0017j§CiwM5¿\vC\x0012Þ3ÖæBÇ\x001a:.&¥ÁÌLzL|ò\x0006Ë\x000b\x001aíò\x000b:ÕÈiÅ<§Òð\x0015çY¥aAG/Ðñ°&ÆlhÝ,h½|E\x001b¥8¤3\x001d8\x0010Î4÷!W
6¤ö
µ_Lmíð4OuË¼>\x0005âÍaÃÔx¯kÏ\x0016üAýìj¾½¹û2ÛJ£3Áþ£æÎe¦Ý\x0005\x0011Ýá\x0007
ü_<½Ø«ÜS!C\x000cËh38¤ºÉé \x0015{à\x000e¾\x000bÎF65²Y\x000cJ®\x0016TÆÎ7_\x0007Ã£8\x000b{mlÏr:fI\x0006ü¼eåj,ô9\x000e>\x0003Í&v5±[L¬¼\x0017(]Wñ$«ÀOmaÊÔõ"û\x001aÙ/G\yþÔ¡¡Jð:\x0012\x001dÈ¡F\x000eK\x0015Z	~m#Ý\x000b\x0016¢±aÐ	 º­c\x001c#ãÅ\x0017\x0006_,~ ¯³ySÍ¯¸kUh
Û¯*éÈ¶c½Ìjç\x0008w£¬dÝáZÌh)Æo#ùòòÇnïNî¾¿ùt?óI'P;uÎ$°ê8éR4f£Ô"§ýï¯/ÿpúæìâèäâÕéùåä[ÎøñRåËÉB^V®£L\x0002	s\.F\x0004û­[/¯«yÝR^ï"d²\x0019\IhDå\x0002É÷ ½À¡\x0006\x000eKIiAsæCâ[6.f#©\x001ajÿ\x001b_'p%Û¢J¾EÄ.
ÎÇ³Ê£\x001dd"Âþ\x0014Ö^âfMè¥"\x000fÒSàw4\x0017u\x0014Óæö\x0017Î%n[ÏÙg­ç>\x001f½|øûÿpwý07¡2ØSäôýä8)Æ\x0019/yðA\x001fÌÕxwôòêôõÅÉÕTJeÛÎ>kO·\x0004Ý¾\x0005®\x000bÑ\x0002pVR³ñö=ãNÒnjt³\x000e]IzZôV"ÝÎpÇ*\x0011Øè`·5»]9íCéM¨Æ{qÖ§¢ KÈ]MîVë¨%ßG?Ì:GîqÖÝ¤ç\x000ev_³ûu³ËëU HA¤I"ÇàÕþùè¼£\x001agl÷³\x001bsÌe³^RªO\x0005 S{ºØ[ó¸Î>jÐ¢\x001a\x0010Uúj \x0004Ý\x000cOûwSøf½ë\x000b>kõÜ½* ?QÈÓâÁ\x0012òfµëuËÞ\x0005Ä@&]ÄqÍ³²U'r5ÀÇ\x0006>®\x000f"«\x0013\x0003xê,áè\x001f9Ï\x0003\x001dì©aO«Ø\x0015\x0002»Rb\E-jÛ\x001eªÐØ\x0019Xgg´-Þ\x0000µÉ.1\x0012ô¹D$neÛÍØ\x00073Mò÷÷?ÿý¿g\x000b|hIÍuý\/¥\x0016ölÔ»£ß_¾{7\x0019\x000b6cÏË4!Ê>`4}\x001c	öÔqù\x0010¿&ÙÛÑ³¹Ä¦&6Ñ\x001b\x000f2Å\x0012sp¤e)\x000f¢ñ`Xg.±­íbb<h@s=Ëú1àh&¼ÃNâX\x0013Ç¥ÄÔÈ:J}aMçý *¬\x000e×IÎ%N5qZL\x001cciIFÑ\x0012#\x0002\x0002AyIÔÓ\x0013\x0017>âÊ2m ª\x0013ÙZ	µS\x000b©KMÔ¤¦%\x001e\x000e\ÏEn­Ûbó»añ,\x001b'§	Î¸v&2£;\x001bó¦\x0017Û7«$p\x0006e¸ÄÚ+V¬Éû­¶nÌ^lß¬ËþQY\x0016Uò\x0010~+ûV9§F
	KV²d¢¯ÄY¸H<íEhÃòe¡);Ç£èÚâº\x0018T)ýáXûAd?ö,|ö,^?\ß}sàs_\x0005\x0002uâá*`ÿÓÛ äüðûÓ\x0012__Q\x0014êèêÃd\x000eÐØ£ðÙ£è\x0007õ^w#	þX\x0011Þ£Ùï\x0017Þí\x000155¨Y\x0002\x001aÃ`ÇB|T\x001b\x0016f¿[Ü\x0003êjP·hF\x0007|rÏ¼\x0002KÇ
jº·\x0005¨¯Aý\x0012P\x0013$@Y0Õê4´OØ/?Ú\x0003\x001ajÐ°\x0004\x0014O]ñÐã×\x0014¼ôÇÁE\x000f{\x001d\x001eÐXÆ% J¤*<µµv r¿Â©·øòºÙôzÁ®\x000fÉ\x0007jóV@\x0015\x000båÆ'ßvé¬úe\x0010¦]©Äü A\x0016èþ,ß\x001eÎfÇë\x0005[>¤0äÊ`$:Ô	èþç³\x001eÒfËë\x0005{>\x0017Ç¤0ò¹D1´tï!ÚCÚl%½`/D\x00013±÷JÞ©!Y±÷`7ùú©!MKHÑ\x0012)\x0001ç
\x0004?Téý7¯\x000eÒ*NãK¦\x0014\x000cG|ðNÒæ!èáë«-ÎPh½E\x0006Jùá¢\x0017[kæ\x001eµ4§ûÓ°zH\x001b\x001b\x0005KlTL¬8 ]\x000f,\x000fK ÛLi³õaÉÖ§ê 9	ÒAyQµ_R¤\x0007´Ùù°dçGoD~>G28Ë?
ñ­	ñ\x000eRÓì'³d?QD@Ä\x0004TËU5êUÖ\x0014Wù(%E·Åõ®^\¹ùôéöæa.4^Ø5%SE.@sôýs\x0016¨Eî¡0-u}qòþôüüìto\x000fØj\x0000¶\x001e]9JÊüuE\\x0014aRâ?Ü¬¬ß×ü~%?`2\x0000&ïÞÖ±,¢J~\È\x001fjþ°?p*\x000bòÓûD`
<Ö;Ö)Ìèr×9X\x000f ®\x001dJå\x0018Ä\x0001XU%\\x000c`"Tºl\x0000ºÙ\x0001zí\x0016À«Yq8#\x0005
'"\x0017x\x0000S*\x000b\x0007Ðl\x0001½r\x000fø÷8Å@i
\x0003Ó\x0000T´ò	fHMt\x000e Ù\x0003zå&ð$RR.Ï)ÅAª\EÖ²×	\x000e×òô 5#HkG`\x0013Ë¬à\x0008\x0014\x0017Ó9%ï»xÍè\x000cÚ7\x0002hv\x0001¬Ü\x0005>\x0014Ýò<\x0002ÇZ6¸Rå\x0003P\x001f\x0004U©%
À­\x001c\x0000.~®­Ç\x0001\x0018VéA;ªy\x00041m½¡ÙÆ°v\x001b\x0007\x001c@îàK\x0003Ð¬\x0003bâÆ\x00198Í¿@³aí6öèk<HÈ$¿AYï ñ\x0000B8,ØÓ9æ,YV¥*·Ïwc¾}Zo¼|©~oKÝ¹Záµ¸tYàõW7\x001e_?¬¶ÅÎ\x001d\x0012O¬\x001e|£ý¡ÊÞaH;ú§º\x0000Õè\x001e½¹¿ûòóÃý_ngWÁ \x001aFå\x0017¥!8\x000fRÏf\x001cjo./Þ¿½ºüýÙD\x0016-SÜ`â¶]'ÊQ.Åµc\x0010¤Ô\x0002
3Z/w ë\x0006]¯B7Cåg\x0000¾E\x0006jÖÂ³îf´\x0003î \x001cÖ+n%ÑK\x0006Ñõ@>£#p\x0007ºmÐí*tk¹ç#éP\x0014Ã\äàrp8ÍªÝ7ì~\x0015»+\x0002¼V\x0019Î²
^Z\x0018E¤6\x0001×ãvfºmgöúÓ/\x001foïæ\x0016°Dº°¢®©¥Ç\x0018;<Opóûíëó?½<»|Á\x001d·3Óm;³^hô\x000fÒS\x001cG
Ø!¼w¸·Ï|hSC\x00153í¥\x000e"(\x0010åUcÒPÍs8yi>´­¡í\x001e4HH|u\x000c\x000cZ¦\x0007!ö@»\x001aÚ-NV\x0002ê>Ä¡S¦\x001fÚ
ÚÃ©xó¡}
íW,\x000f5¨(Çñ\x001bD\x0006öî`Æã|èPC\x00153\x001dä
Øº
oD/V8Üâb>s¬ã
fÍ=Ñ½WOmTÅÞÍ¨$?®5ÒdújoäÅÍ§£Û'\x000b¤t¬Ës×þX¤\x0011:^OèËÙòâôüèäìê0³©Íbf£­<fS\x0005X9É)Ií\x000cõÌÙÌ¶f¶Ëç9XÉ}D÷Cd\x0003È<ë"ÜnfW3»åó\x000cV²xI\x001a\x0015CÒ4ÂÃ×Ð~\x0005´\x001b&\x001aÝl®('Ù¡Bû`ÕÎ|èPCåÐf¨Æ¥~¤¥ôÒGe2øÃ
%ó¡c
\x001dCÛAÛÛ¦A/jÑ{Çïvû°Öµö\x0012ÓGM]\x0004¹.\x0017 ±n°
ý\x001fÙeÐ\x000fÝ¬i½|Q{Ö/SM­Oõ\x0008`¤¼\x001aÍlFýw@Ôu}H'u \x0008!7<	5»ájQÒå9¬\x00164:ÅÔcÕ8b:/¼~üi~Úa¢¨ HÎyI;\x000c\x0012\x000ewp?!qæ\x000fo¦"RqüÐ\x001b«æ!ÝÐ¹ÊÒ²£>öÀêhOJ½<¼\x001ehSCåÐ\x0014qâY2%¬°b\x0006\x0017qZÜ¯\x000fÚÕÐn9´\x0017I·¬ÉBØ.¦AÅ×o¸<B
\x001dCSÕg-R'r\x001eDVOk|ö1§9-f\x0006=¤ÿâ:t0tDD#\x001b\x000e7p?\x000c­Ã8ä\x0011êþ£óûÛ\x001ff_\x0000ÐPKÊOÔ\x001f\x0012åÖâ&ôÇhðåÕÙëÉ[K\x0018ßiCS¦Ý\x000b®©ã[\x000b¦\x001b¨ ·C\x00083\x001e¥\x000e1\x001d¹¦øa\x001b>\x001e]Ýü|?»\x000f::KÆ\x000cñX\x0015¿C\x001bÚ¶\x001c°Ð\x001f®Nß^¾ûæúáãÍÏßdÂðç»no~âÅðÍ\x0006Â½¸ùWðÿüç]~ÿ=-`\x001b
føæííÍÃÃÍ_n¿|¹ùÝçÇßßß>Ü\x0010')fÜ¥Ñ£ób\O§¾Iå½Õ©\x0008%õìôêêô÷gïßþîÝ«ß_]<\x0005²¾8}gøèòÕ«}+¹ÁÇ½\x000c[àS)øT\x0005e2>\x000e*1¾)ÒL[ãã®¶[àÓ*	\x0005?øb¨\x0011\x001fà»¢È³5>î\x0015¿	¾ÏÅ/\x001fU	ú\x0012~ÑM@|_®1[ã£C\x0016ÿ÷âÓ\x0012ýÿj~\x0012ºôøóPTY= J9ÓI¹íVÏÇÿ×ùø×ÊôßÞ<\x001e½ºýr6ïèÅýíçÏ7×ÿ1Ý*mua×ßèñ²<³{ªÙÞÇ~~vúáèÕÙû#´G/.ÏÞ½;=ùðOsÐÙY\x001eóÃLA\x000f<íú\x000e
z	lÓaV¢Dj®± S.3Ïz(ò2N»\x0004öW@ÇÎ­F÷VÐÑ{-vÎñaDwÎÿ
èh\x0000Âê\x0005S\x001aifô¤KIS4ò6F	rÅµÝ\x0018\x001dÏí´ÅZ7¾,\x0018\x0008åúCk]\x0016×j³Yÿþâø·}\x0016\x0006­å_¯)çáólv0Yo\x0019'ú\x000bk[Ø\x0015°Ñ*Ìv´ßPÞÃ>ß±ßacºáMr%\x001bà¡\x0008g^î:±ÑFí÷ËVÀï°2\x000bà­:Ö\x0005Þ+î|\x001b
þX3¼µ¿ÊÌ\x0017¯lí²¡V(Å¥ô6\x001e{Sf>òfÕ!Í´î3Ø?¦\x001fÿõß>î[òoî\x001féFÑ³]ÑÅ¤Zß|µCvØôÞºyðo.?ÐedÒÔ<ÁïXòÝðÔY*¿\x0000\x0012|Rb&­+=}\x0010>K¾\x000f~Ç_\x0002ïri\x0010ÂkeÕ§@§¨¿\x0002ü%¿\x0000>1¹æÜ0Z3å\x0001Å© Ôvkæ_¸ü¿ì¼À¾E¼¿ÿ÷LdeÑa·ÏÔXìc\x001b\x0001ÑÁ\x0014öoÓ'ß÷-ýão>^ýù\x000bþ«å\x0017ÏiË"YFë\x0012ºÇ­yà&e!°Ú\x0005Ú\x0014çöÛÃ¹°$\x001cQÊ\x000f0Ñ«ÛûÇ¹w\x000b§r\x001df^\x0015xÍ°åbí´\¬°$CÄåÕÙå½ka\x0000\x001a\x0018\x0016\x0002ÓëN\x0012`]Þ\x0001\x0011Xi¾Ì\x00053± :M
l\x0002Ê¿.ÀåÆóíÓ0pý®U'°­íB`C\x0015¥\x001c¬\x0000}\"E\x0010Ê%ÞY\x0018g\x000b^Wóº¥¼T\x0011
¯J|kü³lCJûÏNàP\x0003Å\x0013¬ùN¬ñfy¬baoyEDn¾·\x0005p¬ãB`\x001dïdHéKzÄÃ;HðÐM\x0004P:S
ÖÌð0Á:=à­xukaÀ\x0019\x0006ÞrC
@¼
ìýáÍNàÆ¨é¥V
H\x001cACyo§Æ
Q¸tu\x00127VM/4k:+
\x0005¾&rÕZT69\x000e,H\x0013¼-\x001b»¦\x001a6XÍØ¤ãàË\x001c;'\x0018âþ(N'±oýÒ9V.geÿÇÖGÔ\x0007÷é6k7Ûx)ÖKm1Iu\x001a
{}\\x000egE"eYÉ}\x000bàÆ\x0014ë¶Xûhrñe\x000e\x0018\x0004ò6ó\x0014;í\x0007\x001fs+ÿG7¶X/5Æ\x000c9=Ð\x001aó\x0019ï­ZNx9WD\x001cLµpcSÊæZ¨À³i£u²\x0003\x0004Íé\x0001KO\x000fä@\x0003^®}!N\x0007@u¡9\x0014Ð:ñ\x000b½xjßëÆh/ÚÄ¹oJÀò¾[\x00107\x0007\x001e,=ð\x0014bÆ²*(\x00151ÍGÅB­NIÏ\x0016ÀÍy\x0007KÏ;pEà¦Øh
ZÐ\x0014ÇÄ÷\x000ez
Ûl\x00197ç\x001d,<ï4Ñø9\x0013ÜD\x0019§XñõY%x+ê$nN\x000fXxzèD
Å\x0018\x001bz¬ÈÀJ\x0010ØÚÍö]szÀÒÓC\x001bs;\x00118RùË"\x00189 x]é$nN\x000fXxzàÕÃA#b¼3\x001f»ìh*o8qA+îû¾\x0001±iÎ\x000f³ôü ÊK^\x0014ÔÕ9¦{*ÏqÚìÂoóÃ,<?¨7,à<ÇÆ\x0014M\x0010cHFæx3ãfÚÊBk\x0016­h:\x0017DåÅT8P|~¨4\x000fÒIÜ\x00187³Ô¸È0»m*ñc²rVÜ6\x0015&BÀ/o\x0016úòhu%Ð\x0006Ô0/ê¼ñ8å)Æ-¸£i\x001aklZc£4ÝõóN%4µ
8\x0015x¦1nf©q\x0003`ÂpFç<ÑÁ\x000bqØ,te\x001bSa
4Â\x0012l#IUVE°\x001c
ÒÆLäu\x00127¦Â.5\x0015
uqÜ""ÚâjæwB\x001cÝV®¦mL]h*\x00142ó0zö¦¤ªãÎsQË\x0007lµm³óìÂ§è\x0015Ár¾st?¥W¤å\x0000ñ>­7Ç&=pÛU/K7¾½~¸¹»Ã_|ÿxôþÇÛO³¯|xæ5bH)¡ÄXo\x001fíµQßmNß\x001d}{ruzq¿xõáèý\x001fNÏÎ\x000f\x0006êÑÀ6£ñ|Û6$¬Sü%*ç±xu8ÙmÙXL=\x0016³Ñ±J,$ ½1/ãJr÷BÚ\x001f\x0003[7\x001cW\x000fÇm4\x001cU£s\x001e«á<VÚ4\x0012Ò3q¿o¸n8¾\x001eßh8>qÝ\x0018_*p4rÅÄ\x000bÛD¤dÝhB=°Íhl²üÖ¬©Éµ*n°NC\x0018\x0005&®së\x0013ëáÄ>\x000ezÚqÄBÖ2øuB¯£Â¯4\x001cÝX5½Ysül	4\x0015ëäá8\x0004¹&NÅuÃ±ÍpìV¦\x0000äÒ\x0005ø¥8 \x0004xuÐó¯öy\x001aS 7²\x00056$	\x0001\x000cãÑQ
\x0015\x0006êp¦Æ²ñ4»Go´}¬¼Ü4É¾åF·MyUþ¾N\x0015Å&@m4\x001a¼0[NðA\x000e\x001e*¦,_ëë@ëâld\x000c,µ--»GDº÷4\x001e$V\x0018ìW¿p<:\x001cP\jè¾ýtýQªÊXÄ÷åÃýíì¬,Üñì|â\x001eÁóW\x0001(Y+\x000fÅN
åíùÉK©/cQßWgû3³a@=\x000cø_;\x000cS\x000fÃü¯\x001d­a7\x0018VüLHÙ\x0019T¢FÃ0\x0014\x0017¿	×lù0\=\x000c·Á0¼¢8N\x001e¨ýâ0¼dX·?Ú°|\x0014¾\x001eß`\x0014èM\x0006_F¡\x0012çÏ\x0001Ç/ ÖLc,\x0018\x0006\x0013\x0004Á´9ono¾ümvt\x0018MmI`SÄfm\x000e+¾Ü+ôçd5¾9;}ÿÏ¡M
m\x0016Cë¤ù¼SÆññ\x001dRHÀÞ²\x0013Ï\x0006ÝÐ¶¶¡©ÕD*¶Ç£Ç^®îCº\x0007L»]ì"Ó;8Ñ<+¾dà<ÇrRqg
\x001djè°\x0018ÚRÃ¡NQÌ¦BIÅ¥í\x0014þSüå\x0016Ða¼
\x0003mÃ³~¾þü¹h:½ùÛÎKk3V2ç5= Û&8qÊï_ÔgoÞ¼{WÞüi¢Çi\x000e5:¬Btk
¥VÔ,¯äz"p	¹©ÉÍ*rÈ\x001a\x0016eÒ¥ÈÊxå" Òþm¹\x0004ÝÖèv\x001dzî»Í\x0019ÿëFC\x001a&}âY¯\ë±g¬ô÷®ï
À,rO"|\x0005](åê>rÉ+µ\x000cúöòòÃùÉÅ~)
\x001djtX=çÀ¡IZojÎÃèsrq:ÈmMnW[%\x0019#x\x000b-jUH´\x0014æ@ñîÐîkt¿\x000eÝ\x000f\x0005Qè®Xô!tçg%wv Ç\x001a=®Bw¹ggFGûâ\x000bzÐb\x001a½öÎºVÍ.U«ØC\x0014ä\x00069C5XY0j¢xq	z³Kõºmú\x000fFo¶©^·OSâ×6ERV±\x0018GêªUØÑKKÐÁî\x001av·=Qf~à{iàLw`m9ºMíºnL^ec
¼Z¦Ýðó¦ò.v3#!¢=4ìa
{D·¼
ªè-ÛGPÀÉïÊÆJÝ%ì}Ô«\x000cd ù\x000eÞ©.ë¨Ð¼ã­T;·dÞ=5ìiÝr\x000fKËÝ8ïC\x0010fÛYÆ´Ã*ÓN-/d
ú·\x001aäY÷"Yã¦j»°7Î#¬ò\x001eSQ8Ê³n
ßðÏÈ{¾õsò2;ØMÃnV±;öÙUD\x001f¸<ß\x001a¢srU:ÀS	VJ4Ól\x001eñúLOA´`ì+E\x0006rSöæTu§RÐ¹}C\x000eúÂq9ôÓ>µnÓS	S	VJ\x0014¤N%:\x0017©\x000c§}\x00107¢äMÙS	VJ)&J6Íì"©ó\x0004wge\x0018v 7\x0012¬:¢ST¸YV;I¾i'%)^ízÓC	C	Ö\x001cJ®\x0019Í£Òb\x001eõà?Z\x0008#-`7Í±dV\x001dK1È\x001dUÑ/Ë\x00155E>lHÔZBÞ\x001cJfÍ¡dp×çÆ¢H\x001e$fNZ\_í7µí¦¹,U%jÍcôð\x000cÃ\x001b\x0016ßv±æ<5kÎSCíÛÁi'ñ·òöFFlû¬Üö\x000eöæH5«Tº,\x0005ö\x001eIMÒÊei÷°í¼7GªYs¤\x001aå\x0007à\x0013¿\x001a\x0001pg0§LHoYÂÞ©fÕL<Nl 
7'$ÿ1qfÓiÎT³æL5¸Rä­úóc¨$7qB+p	zs¦Ugjò*;àHq [H­Åù5\x001397\x000bØms.ÙUçRëáI]òî2»IâËÀ¶1\x0019ÛXw»Îº£ßX2ÑðdrÇì\x000e8)m´0§¦\x0003½±îvu×Nj­TÐö8:Î\x000f\x0010-)ü·lËÞFÛ×X÷ì\x0010xf'a\x0018-\x000eÿuN&ÛXw»Êºëèè} ¿T§ Ö\x001dmºXw£·Ýªu·k¬;LqX3N¤\x0001¬D6L#yÔÁÞXw»ÊºËòØ4í\x000e§=d\x001dÞ\x0011ì¶\x000b¦±ívm7Y´,`\x000cåÀ´*Ñ6~ÛpmîKvÕ}ÉSY0¤>U$\x0017¨;\x0007»zFÖ|v×Ü:Üª[A\x0003©\x000béÐÌó¼{\x001d½$ïèMçÝ5ç[s.ýÃ×k\x000e&·ê`
\x0014Ï(7&ã\x0003F\x0005ñ\x0007ð#o»fÉ­:þáóÞ\x001cLnÕÁ\x0014IÊó¾4p3ÍÀéHaÚH\x0007zs.¹UçÒ?nÚa®\x0001º©¤£<Ç\x00026\x001b]I\x0016XÀÕ^TlaAÚ9"9Á±üè 9Ôä°\¡Ã«Ù÷E¦<ê!¹TaX=ñ\x000e¼\x0004ÝÔèf
:ºX¬¡ëEIn¬ó\x0003J$ß¼)º­ÑíªõBR\x001c\x000b³¶ÈP #£\x001d¨f"Ñd	¹«ÉÝªIG>!\x0007`ýW*G\x001c&}"w	z¨ÑÃ*ô :ÙxW´ê3º5n·Ý¤±&ë&]ç\x001e|ËcóS4|F\x0003\x001eôT£§5è,c^BI>Äá:¡¶\x0000]·F}U§f\x0013bÕ)m½, %\x0004$ô½)zcÕõ*³~ÖqìöJ\x001a\x001d)\x001b\x0006ã¶öÆ¬ëUvÝzË\x0012\x000b\x001a(«b×)×Zæ}F»\x001eöÆ:êUæ\x0011\x000fLV
Å[vN9ÉW%-W%ü\x0004\x001e§º1z}tfx\x0016óÁ³,+^ó$rªæfw 7FF¯²2\x000eoyLîÓ0ëQS\x001a;\x001f\x001d\x001a#\x0003«\x000cuäÕN³Å\x00150TDÎ;ÕÛÃ\x001a=ìÍNU;5\x001dê5´ìTt)\x0007v;\x001a¾½Ù©°j§\x0006JêáwÕGw\x0010-ì\x0013\x0001ë%ìÍNU;<õ¯<UQ\x001fxÉ\x0018æ]mz2A³UaÕVE[(\x0015m¾4ÚÍ\x0017T=Ì»Q{ÒÁn½jVíUÒb+bñÊSà½\x00045ª×
{Ú\x0019Ó^VíÕÖÝi¶îC¯\x0012\å\x0012±V[ÝQuÝ\x0013½ü`\öóêæë»ùu\x001cIºß
ç:Jb~4\x0013¯\x001cu!Ç«Ó×'\x0017Ó\x001c0º`#<¬÷QäT!(Éo¡|0N	Ö.75¼Y\x0007ï{iR¼æ\x0008\x001dÖq\x0013Þû"v[³Ûuì¤Ìª°¾	Ã
;ú'ìEä®&w+g\x001dÝ/^ïÞ³rÖInªÑMTs,÷5¼_\x0005OaGWdW yiUW>Yï!Î«º
\x001fjø°r³Rù&¬\x000cë\x001d\x0019ÍÄ\x0013Ó"øTÃ§\x000b^\x001f\x0007^ð\x0014äJ½AË;LÜù°ëÖÄ¯³ñ$^Xr5\x001eEì\x0007ë!A?N\x001d­}ðf\\x001dnFÕáoï\x001f¾ÌÅÖIT¨yµk-yAMV-o.¯Þ\x001fF65²Y§\x0010Ë\x000ckm9\x000e¦)p-e\x0013\x0007R/²­íBdÊ+\x0006\x001cZfyVFò¶\x0010'R\x0005z]ìÎ2å!%n{3tÏTÉ\x000fmoÌD^äP#¥³ìÑhD3£VÜ½ÀQ£05\x00179ÖÈq)rPòÌÈ³\x001bIÜC\x0014¨'Ê©zSMÖL²eÉìäD]ûLRaÕfæ¢*t$\x000b§\x0012;«¥å\x000b\x001b§¡Y\x001bºz3±¹µÊKÍre°ÃºH¼.ÔàºØ\x0019\x001afXÊlñüPÒÙÂ°:hÞ}Z»
Fsè¥G	ÕFIÄ\x0003yEb/ÌFÇÜØe½Ô0gfÏ\x0002¡tb\x0007a\x0016äíLnì²^aµ4i±hðXgÒº8XYz\x001dó\x001b3§WØ¹¡ÉU =9YÆf>\x000646\x0003VØ\x000c%¾¿Uv8Kd=§8CÍs.s³\x0001añ\x0006¤®\x000bÀß^Ë­$Ë.¼[¬\x000c7ö]#oñîúÓí\x000fw¿t¹ú\¿\x001d=ksé§<>G²\x0005\x0007\x0013=Þ½¾øÓal¨±a96Ý©ÊFì@OÉ\x0019ÛxÑXP\x0013\x0012ýØ¶Æ¶+°é\x001eË¬Þ³ÃA
më\x0019Y³±}íW`ÓC\x000eW[Ë'8ÞÄ%Nìü.\x0012³±C\x001dÖa;)\x001b\x000er¹Blm;§Êi6v¬±ã
l\x0017ØöQ\x0019¶#t×\x001aªÍ$ÕØi\x0005¶ñÔ?¹õ\x0007nÕ©e®mS¦2\x0017ºv§]«\x001bÒKm¥!Jx4r\x000bW=(ä8Ç<»5Û+ì6]½Ù8\x0008\x0011àäM¸!ýÜÝÖk\x000c·Õ\x001c\x0008V1
Â\x0015ÚûD\x001d\x00056än\x000c·^c¹¥Øo©±aS\x000e÷qÒRÚÛ5ÜnÅ:ñ Ò	Á\x001c\x0008+	\x001ca"G¬»9qô#ü\x0012^' ¹¶V\x000få(nN×ÙÔÍ£W8Ú:îSSÒex¶IßQÃ6Än\x000e\x001c½âÄ!JÃÊ¦èm14&0\x0014»myPBc¼añÖQ\x001fsrR\x001cfÐén\³©[×u	¤ÎÛVÒ|AL7\x001eO\x0019Ê\x001bb7\x0016\x0010VX@´ÑÔ½\x0014Ñ>a\x000f½¸ñ\x0002¿åt7\x0004VX\x0012Mîåü^\x0018Vs8§:l6v³'aÍüb7N ,÷\x0002µ'!rÞP¨ÝsDG\x0017yaâ¬\x001a¹Ü¦1%f)± VÎ¥æé¶Ã99K*q6wã\x0007å~ u>´/Mµ¾%è`¨ÇQo=~ÔÏÝ\x0018A³Æ\x0008"7kÐ»AI\x0013¤\x0013gH£¶[rÛ¬o=h­à¾äw]éÎd©¤gC#h\x001akb[\x0013MeÕ¦,o§Biã\x0015©£4_ÏtØÒØf[ÚåÛ\x0012o9Ã¥ÒÄ(Ó\x001d@®Êo9ß¶YÞvùòÖ$lÇÙiT¥QÒÕ)!V$¿aNKúÙÜÍai\x001fÆ%õÈÔâoR$KÖæÈÛÍÆn·]±¼\x0003=×e\x0002Á±º0­`ò[:Þ®YÞnÅò\x000eÁ
8=p»Û
·k·[±¼=Øc\x0018\x000e\x001d~Ñ£¤u9tæt%Ý¸°n¹\x000b.ª#âÑü¬\x0017­Xoz_Ø»ÙnÅ®\x000c\x001aÄ
ê"SV^Ö\x0015WÆ8/ÚÏÝlK·b[zïäÊ q¾#?Iª88s4fpkH\x001ee\x0011!âý/7\x000f3Áqq\x0018~²&Ùr\x000f1Z\x0016áÓÞMx'ÕS\x000eþãË?^\x001dF75ºYîÐÒ\x0019y¤®¹¥Un\x0008r)ÖèÁÌzº>\x000eã\x0016D\x0010G=0/¿¿½¯\x000e%H\x0000Ha¸¡ZZùYM¡._]LÖ\x001b;\x000eA\x001cõºì¢¶®$d8ô°ðäa­\x001di»n\x000fsÒÐgc\x001aÛ¬lÒ{)\x001b39)/rÁA!!áí¨]MíVP\x0007?\.­âÜsô\x0005\x0013Ûï\x0008[.\x0011_Sû\x0015K$äVñyæl\x0008Ã\x0015Ä¦6Ä5v\íUÉ¦DlÕá\x0012ÝdJ¼Ç&\x000b\x0013AÁ~ìTc§\x0015ØQå¸	=\bArýí
~¢>¡\x001b»z"ë§VpS\x001a(Íu0ì\x0007B²\x0017¶Uó:ÈÍnMö
M©]¼F¬×,ÌlÕ¼´ñôÜpGêÆè\x0015j*);\x001b¹@óúÐ³*g#7FD¯°".Ö\x000c¬ð\wE¡+¦"¦gÑ\x0005Päèçn¶£^±\x001fm\x000c9Úí\x0012±\x001esÝ6ë»â?\x000csÊã\x000ec0:ÖMø¦ÉþëêèHE}ÜÛE-a\x0007ô§¸¸SÔ7£)e\x0018;¡uþú Maª^µÜ²\x000b8@¯u9y3¡m
mB«§[@\x000fð¸´§,µÂNÉÜ´Ì®fv£³\\x0005¤=ç2³	¬7Gù®õlf_3ûÅÌÎ\x0003k? sísk´D#\x0002\x0011\x001b®P3åó¬=÷\x0004Ð¾\x0010áDsÛ<\x001d@Í¹ÉÌdN5sZÌ\x001c¬Ôæd¯O\x0012\x0012\x0018øÅq¼\x001cVã,@åºÎÇ£\x0017\x000f7³±!òó\x0007ZiåNu\x0002>ÈCs
Å>\x001c½¸:ý0\x0007\x001cjpX\x0003î}N\x0004$p¼9Ö>·%\x0007ÁÃDs®\x0005à¦\x00067kÀsQÜ#"0Kà\x0013í.ðñWå\x000bïÕc~y}w=Ù«ÄÝO´22¼\x001bzrM>¸È¸/O.NfÐÚÖ.¥õE\x0012ad¾x\x0012a-´&M\x0004)»h}MëÒÔ¢Ëu\x001cãn\x0006z[Mn¬qã2\\x0017\x0013çÍå&g
=¼©Ëâ6¸Õ\x0015K+Ö2^{¬9©2yÉßB§iH\x0018HÎîãmv^¸Õ(TÍyr)ôÕ\x001ajM%%ÎÕvd\x0016Ðß}b}uÿñËÍãÃÑëÛOn®\x001fgcSâ{\x001c6](VÍI:î¹@u\x0001uùòýé«£\x0017'gçç§'\x001f\x000eÁÔc0ëÇ`ì°\x0013mäæ\x0008Ú9A¸ÃK»\x0010¶\x001e]?\x0008jhÆM\x0008MÖ\x0018.\x001fBRºüdË¤¥põ ÜêAØDj\x001e\x0003½§òPF>zöX:P!¬\x001fCRIF	\x0003E¿_Û¨Ä®©FK\x0007\x0011ëAÄõ«IÙc\x0019¢zü!´ô\x000c÷SNÖâ1¤z\x000ciý mÀ
µâÌ$m!i)µê×²p\x0010uK[\x001f^Ë·Dêk\x0015¤\x000b÷D\x001cÓT{¨¥£ÐÍ(ôúQÊ|\x000bG¡8\x001aIfè\x0006<ñ\¿t\x0010ÍQ§×u¸¹\x0017½VEì\x001f·µ-\x0011§2%\x000e¡9$ôúSÂúÈ^VÔ±\x000cbh¾äÓT\x0011ÁÒAøf\x0010~ý @I°NCn°G¡D®"ÀTuR÷(`,©\x0004Ï$Îï\x001f¯À¿¿øt}÷qn¤4§NRý \x0005¥]d½\x0013e\x001d\x0002Óó´Î/?¼Æ¿¿8?¹x9\x0019ê\x001dåÀ3±e#	.\x001f\x0012y$TtÀi-l¤p(Ô/ó×\x0018J¨\x00126\x0019JL\x0012v7¸¸$¨Êå¾8\x001452²f(©\x001eJÚb(\x0014*¡\x0010 \x000f<\x0017ç¡ü*_E·[e½T¤¤º2ÄoªxlH\x0006\x0012©¾l;\x0016=\x000e\é\x001c¸zûéúcNùô?ÿù_§?|ºý<W\x0005\x000e(uÕjlZ\x0011\x001f­xèn¢ÕÍÛó99æüèôõùÙ»I
¸q
«Î5¬kÈ­\x0013q#¼8³ð´ÆÓBÎ)A¯\x0005è¾F÷ëÐ\x0012/\x0010·¡_µt×ôSÇ\x0002òXÇäV\x000b])¸5»ROÛ×k©°\\x001e\x00127JDÏÛT°â,\x00055ñ2µ½Ù¤zÝ.u1dK]Õ(=MIZM\ÕýFs\x0001z³KõÊmªkûq­gùì\x0012R\x0004#Ût"¨¿d±ÿù»ÛÏí§\x001f¬\x0019Wì_Gî\x001e§\x001e¼Ó©Öò=ø0~LVRáÍýÝÍë¹YFG\x0010íf§-%@ÜJ1·ö~FiÃËÓ÷'SY0~ü"±\x0014\x001b\x0012I\x0005\x001b´/³Ú\x0008¶Ó%f6¶­±í\x001alËlèñ2i¡N
\x0004æ4YM\x001dkê¸Ú\x0004©\x0001Ôah{kÝ\x0019ëæ$ÚÏÅ®³FåòÝk;×lç\¶(ª»`¢$\x000eú4§?ßlîfè\x0015«LwI
\x0003mø±
 ÃÓâßçô2?mÔÈI4ªr\x0012\x001fÞ^?\;[Ñzé¡u²òe¥ø%Äk\x0014\x001bÀÿº·Ù®ë6\x0016u_½Û
\x0007Pø\x001fnQ\x0012-3\x0012yHIãdw<$Ææ$:èÄníîyÝ½½<GÞd?ÉE\x0001U °8¹Ö\x0004æ<¹LÎ8;
ãØ\x001fk\x0002õúy{p~tqôâdgíØºZ/¡T¥[Ëy¤¶¼ïÀ\x0005³Wow`Û\x001aÛ.ÀÖ\x0012+J\x0013¶\x000c\x000bQ<
Îï
ô:¨õö\x0011Ñ¢-TzwuûeöÁ\x0002ö¥\x0018<uå\x0000ÜØ¥ìù=÷õ\x0006ï/^ï<ÙzûhÑVýtb,òJ;|´òÜ'?c½Álè*þÐí\x001c».ji-»Äö\-¡øì¯-Ï­\x001anµ[pèÕÞ§ÙÉû\x000b¹¢¸«ö~<Úb\x001c[G§iZ7®cÈm/2ð¤Ñh0Wá\x0016ÛµÂmµ\x0004<»»þúõf~Ñ#.ÎÇ[\x0012Ù)\x0001­(´ÇAÀs\x001e½=¹¼<ÛY÷(ÃvZ"lÏHy{ýëæîï³S+ y«\x0014`:UåÔv&
rG#FZyyqòîèíÿÞ\x000f¯jxµ\x000cÞó\x000c¶x\x000e=56ÄÂýbÇl!v]³ë%ìñ¿´8%\x001e\x000fß\x0018+Í
;ä!vS³eì8&:½<+`¡$÷ìHN\x000c±»Ý-c·×bI%øÌ\x0004UaXëÐ\x0008½\x0015iÆóÓß?»æªÞ¢cÈ¯\x001fó\x0013Ø,Ã¯\x001f;ZHk]s\x0016uÍñ,|¨ña!~\x000c(h\x0004¯\x0014ü\x0002å4onWYÎ\x0018½­éí2z\x0017\x001dECô
\x000e5%¶\x0002\x000f0u»Ú¼Çð}ï\x0017á+ÞË.o®
mù4<LXïÈâvÂK±uðc\x0010zÿüüæóç«Û\x000f]99\x001eônïKûÇ,Y»k^\x0011ÕG½zu|ñ|gZkÛU¢®ìÆ½ê¥BR\x001eQBÉßî\x001aÄÕË¬jf5Îl
\x000f\x0015Fñt<\x0013u#¿QìjîÖ5´^\x0000\x001d
\x0010\x001d\x000eà\x001b\x0013JßÎ¨ôÍljf3Îl4­~B\x0007\x001e\x000cZÆÝZ³cñØ|fØ¾ ¶ÌÏéæ.:èócæhq\x001cù¹VqYK®±õzÇù¨TÈéÑÛè¢ï|JÜ¾ ¶LO/º×\x00148Kí­~\x000c98KëaÎ²Ý\x000etU£«EèÆrÕF)x®©6<«\x0008»4WE×5º^\x001eO	ÐÑ¾TÃÙ²MGÍÙ°×njt³ìÀ0\x0000uðùÀ.RÎêdnkt»\x0008=Ø:Î3Ë%\x0016i3ú¼öÒýèjÛÁUúÁ6ïóÛë¹zQë\x0018	Ñ\x00144%\x0014Õöèx"ç\x000cvi6¥_ìRjÛµUúÁ2ï\x001eð4ÍÀçuÞ\x0002©\x0017!g,=è\x0000×5øö>ì\x001epKës0dy%Ü¯\x0019¡9ºe\x0006·´Û\x001e¡eðû«O×³]ð¨±yWTifh¾l\x001cøÝ~Õ÷Ç§';]W»í\x0005Zö\x0002û@cxOó$:Û¤?\x001c;Ø5©m>¨ªAÕ\x0008¨çÖôâíÉ2úå»fWÍ\x0001ÝÎ·I÷à®½¼¹h\x0007¯7×¿_ýeÁ5j\x000båiZXà\x0019"»^Ãûòìmüo\x000f^\x001füÇÉëý¿ªíÕc¿
\x0018q6\x0016 8ËsEðÑíÿÊ¯bë_Å®ñ«xì	ÉuØ\x001d\x0019¨ì*µô®^%¿«í\x0015¯ÃÇ+äZ@p\x001e$\x001d/\x001e\x001feÂÙÕK~\x0015_ÿ*ÛÛëÇ¾p©M\x0015\x0007N`Û87¸;²«ÊÏÝ=÷WÑÛe³\x001a¶bw×?}¹]\x0001\x0008)[mØ<
ÆEëD}ã\x0000ó2ìïN^¾>Þù\·½TÃVÜÑ--§\,NÞ!nMK
£W¼£\x0008s\x0000\×àz\x001c\Xï¸ñÀx_u]\x000b\x001dóÏ{¸EØNº¼úùÏoW»W7·/\x001fç×W	ì)¢N¢2rÙ\x001d»8Åûü£7ÇGo\x000f^]\x001c½~±ÿWúWÅ¿\x0016¼*	ÛW\x0014¥b,\x0017s¹\x001dáêèo êß@-ÿ
4mùNë\x0019s¶1þ\x0006¥\x0005sÊ\x0019ý
tý\x001bèå¿\x0001o­Ðü\x001bhN÷\x001dþÅè¯`ë_Á®|hîn}f4úÏþ\x0015`ÛÉ\x0007Û\x000eæ{us÷i¶ÕRÊ\x0008ìxJ:(Ê?O±\x0005K+¿q_ü
g¯ÎÞî4Uj»c^µ#â\x000eÞÜÞ|ùpõéÓÜ Jj×Yà£Om±x
òû\x0018V{ÍY\x0012ÿæâìõóãÓÓñà¶È}\x0010_nî>}´³Ó\x0000÷#ëã«õ\x0010ùÔè1áåÑÛÓ×ñ/ñ\x000b¨ú\x0017Øv©û\x0001§yr\x001c®K)+¨yñs·Åwü
ºþ\x0015¶còî_A[}H\x0013½â«
/ª]ó\x0001F\x0003Sÿ\x0006féo p\x001e,\x001fvv9p åi £¿A¨°ø\x001b\x0018ê\x00158A¦¤hÍ±af|9ÿ7íM^|c?N`k2\x0017\x000bÞÒ*UXñ+h¹í>ËV¾»úúëíl/T«èCÜY\x0016½fRD1X±\x001cÉ\x00193\x000fÞ\x001d_¾»ØéÂv"\x0013¶\x0012¯n¾|Ü|¼k»¢ÜEZÅó^âàÑ1Õ4ïEî(¯¾'uöúÅÑ³]æ\x000b¶S°ÊìEçéÚ\x0011\x001d\x001b,óè9é§êY!ý\x001cÕ3\x0007}ÛùPsÿÀÙÿ|ÝóP\x001c°Ü-OA\x0008÷SJXiî\x001c\x000bþú\x0007Î¾ÿþ¤~V»wÐ¶M­°ÛÕ\x001c·7ÑU§\x0007Cd7!À-aÊäZ\x000e\x001d}9ù«Ëg\x0017gÑMÛ\x0019emï]\x0017[{×]}@Þ|ü8_YG\x0013w\x0000\x0015eVJy~!Ñ;2ÞûgÏ'Á½¿Ëw\x001f6\x001f7_¿Å\x0002ÿaûwúwÅ¿V·xÆïÁ>¾\x0006^*äçttÿ\x0012ºþ%ôò_BR»\x001b\x0003\x00173ó0s¶§vþ\x000e¶þ\x001dì*¿qåwð/WåÓ¨9Í¿¯	ÿïùKÔ\x0013¶\x000fý\x0016`Tv=ãï\x0013hé8ÖöSÎ*È\x0019#uçý\x0012æÇH_W)ä\x001fÜ\x001b¯Ñãyó-²"½¤bcóÝù?ÿqFÓG`\x001d}JÛT\x001cà\x000bbªa5Fã¸ùH\x000cè©¥K||&ËgU\x0019=ggoâoñæ¬è ¦>:£ß\¦\x0013:»Æ(zcÔ!¶NÕtª\x000e 
ít M\x0012ér\x0000Ë&rgÒ8©áL\x0017Ä,¤GWÄh#s"Ïh\x0011ò\x0010\x0017PNç8nÎÖt¶OtÒØ\1ñü9*\x00110ÚÉü@\x0010/É>Þ8«é\ìP)ü²ó^ä'%£¥ÌÃ¹¢ñÖyÀÄ8¯é|ì°Å3
r²ÂÙDï»Yvyçí8[¨ÙBäâgKU+Qr8ôÅ¥\x000b«¼ËµB1®
¹ôc46+;ÑË\>vØÄ$L´1yÖ\x0017Dþ\T3×êâ>e\x001c}'fÂ¡ôp&\ú²Ê\x0019ÍÒÓaº2}ÚXj\x000f$=\x0011MY¨\x0014?.ðµP°P\x001bËF\x001bË>u¦Ó \x000c¹y'J\x000f,i¼¨ói<j²d<ÝgMJ¬!\x000b¹B4JOä\x001c¯Xvqec.d§½\x0000oÒætö\\x0010].GWC\x0001Íò\x001bÇkìì3\x0018RÙ\?>®É\x0005\x000bÑ\x0011ðåÛ.¥kìì4\x0018éve­gÀúµd×Ø\x000bÙg0â§uiC0âE­ñðÓ\x0016µbÜ2GE6&CvÚ\x000cà	5\x0011\x000fL\x001e^\x0018\x0005æ$<­¹ ÐØ\x000cè´\x0019` u»&ér1 ð½µb3\x0000ÍN\x001b\x0003IOzÖzÚ\x0008S´Þ²\x000b­\x0003ßi3bDtÈÂ\x0013ø²èr*/¼elÁN\x001b¿è\x00049¡
ï\x000bN,3\x0018Ð\x0018\x000cè4\x0018ñ_Å`àî¸|/.\x0006\x0003ôBé5\x0006\x0003ú\x000c\x0006à~Ï´\x0019\x0004£\x001fG]ÆèGäAù\x0018þøeJ\x000f\x001a\x0001\x0006CDgÅdé)lü"é	ÏGOÚe\x0011\x00064\x0016\x0003:-@\x001c\x0008Ï\x001e\x0012]t±nat\x0006ÅNÓ|\x0005\x001d=©s	K\x000cl­*7C/û¶"	8%ÐÀ\x001ft9T&µÃ'ÈøGÈV×1BÅ\x001c\x00165µ
\x0019]Ò^Êèáå	(JN°à¬\x0001ö\`¡O_
\x0013*ñd/dÀf÷ô½¥H´!\x001cÇk³ÌÆIøñ[ÚÌW\x0007\x001fø¾øCpJÃ;T\x0014~XºÑJ©7\x001a¶%\x0019­]¯(q}#Ji¯òÞ\x0015Ou¡ÿRöSê@;¢(ã]W\x0014è\¤\x0016\x0019
\x000c^pa¶¸\x0004¶\x0011uºùeó	Û/we%±³>gÖ´\x0013Y;\x001aù\x0013m×ú
<væôèüè\x0014[,÷ãA\x0007x\x001e\x0007\x0011AÆ¦/\x0007ÂÆÒ\x0012²È\x0007KñT§z¥§î³¦1èÌáÑy¯\x001bJ¯Mé\x000eàé\x001aOwâ\x0005Py
JOåâ`\x00135á¯\x000bJ-ä35é\x0015\x0001ÒØ Ë\x00150Q|ä³¦Ñü\x000bñ\çzñ¬NÛ?\x0013Ì+1"xâ3Þ.ä\x000b5_èåC§3öy¡·AÇ1r\x0019luK·rñ$=M\x0013^\x000c®VL·ðìÉæêÊÞ»ë%»«\x0002ß]ÃÁp4Én)`s9dïíð:ä5®\x0008èr¡@Ô}ôê%Ø\\x000fÙ{?<ºÓô1Õõ²\x0000ÊAÀMdklÛ\x0011þ1\x001e¿Óho#Ôç«/ß\x0005~~óå#>#^í¼0W\x0000Àctm.ò\x0002ÜSX[Óhx#Ü«ã×o)~~öú\x0005¾\x0017>Z¼PñBÍ\x000b¼Ñ±>Ìß\x001d<MªÆcèÕ!\x0008\x0013VÂU5®\x001a\x0015/N ÊZ<ÞôrÑ}.âuÒ¯Ä«k^½@¼Çg,_~Õñ\x0001Ö¯©yÍ¨|µ+¼,RºfÚ·9Ï%¼¶æµ£¼Q±*:¿\x0008(éº\x0005NW4zu	®«qÝ(®Ñ¾H\x001bý$7ª4Î®µ´¯yý(oTµ9ì\x0001ìù\x000e¹À\x0004Ëâ5°Öu\x000b5o\x0018åµ©)*ââ¼HE\x000e¼dZXK÷Êl+ÄðqP\x001b
í¡·t\x001a2SK¥»5ò"ÿ .&9ÞÜýýàÙÝ\x001eûaS\x0010¥jÈFÐ¤\x000808ù|"ªÄ8\x0007ÏÞÎ¡\x000e:é¬@w\x0005é0j#
².züí Ó5î£\x000bJ\x0015:Ôc^§<É.ÐxÞq:[ÓÙN:ÆJ'ºèß¶w\x0012&x5Åêù²uV#Ý:©1ë\x0003\x0007HÛf\x00112Z'2ùQnäù\x0005£G!íöå°bkð5vçìLcÆ%§Ëãu=Ì7\x00183oäzg¦¼ÒÜ3\x0003
j4èCÃ§_]ò\x0005ØD©\x0001smÑF7ªÙT\x001f[¼´R-ÖWÄ`ÒQfÒH||\Âfj6ÓÇ¦<=Ð\x00006Y¦ix\x0011Meh®Fs]hØ'ò'á6\x0007\x0017øPCl[$Ýl¾fóbÓl\x0014ø*6¾Qv2@Ëv_"n©èPR{ñÆ¢SJsô\x0018ÚLx7\sOeçEEÏá<Õ¥\x0019\x0005îþ2,bÓ
îcál~ÅÇ$
ÇJ(ÅlnÑm¸/\x001fIp¶ï:¸û	Û¬á¢N\x0006¾ª~\x000cNJÓ\x001a\x0006ìM¹\x001f×wùmóqg®B\x0000¶\x0001¤L¨¤,<\x0006©%,\x001f<»¼=¸|sôbG\x0016T¤:,ùp©ä6P\x001cj9?&\x001fÐÙD¦&2ó°%=ë2\x00155®£¢<	d\x001e"²5O¤%9\x001a¸®jk\x0015T\x0008\x0017u+<ð$g3ùÉÏg²\\x0007º\x0007
KI3zøÎ8©*º¤\x00157s¡\x001c\x0014A	GU[Ñå¦Ç°¨þ\x001f\x0016§Ì\x0006
æCùT?)Lºè\x000cEe\x00158¦lI7Lz>S°%âE\x001eT\x0017\\x0011ÔÃJÙLÍ!óOyÀÉ'r1±ü¾®}ãPÍ)óyéµ2A¿wL ö^\x000e_=h9Ì?æAS\x0013à\x000cs­Kü9gr'êëf35§\x001cfr%âÑ¦W,\	\x000cÙ¶ÐÞP|Uu\x000f\x001exg35§\x001cfòøsÃ/"º2¹¬Ä\x0004§è[7pÌÛ¥Dù\x0007[­eÒãïÍªKÁáÈ\x0010Ã\x000fÎäÆc÷0øÞ·0©b
:Ù0ýgMs¡5û.\x0010\x0016¡©\x001aMõ¡aà¨³zj
è°Éep\x0013\x0005á\x001dlºfÓl!~G\x0016*MÒ8\x0016~XaÕÁfj6ÓÉf=³ÙàòDUm\x0012,¶ð0MÖfk4ÛæBZ¤b\x0013\x0002Ó\x0002ùràÞ%l®fslÚqNÜâ#¤n°"µå^\x001dd¾&ó½R¤>ç'y\x0015ÐXr\x000fd£>d§þÀ.}¢}:¤³&ÉÝÁ\x0008ía¥O\x0007[sGeç%LÔt\x0010\x001dÁâH%\x0017Ã(ó0#;mëaNÐÃ\x001c'\x0013ÿ|}µ3^ÄTq\x0008%^tITFs¼è¦JÒÿpr¼3ÝzÐ\x0012ô 5K\x00039\x001a\x0006Ê¦ÃX\x001au8åk,ß%\x0015?¹ÇëG¸bÑæØ²ýa&VÎ¡\x0017Ù\.\x0000õS¥¡øZs0;Ù¶\x000fKí_¶ëö·«o;\x0011¨»r<+ò£d:ô\x000b§­üG:~3\x000bj.èáÂ¸È\x0012W`\x0011\Þß¼³éæ¸y\ªæR\x001d\Öq_t&\x001b£µ¤ºO­\x001fi"¥k,Ýõ\x0019Í!}Eq¯ºè¹FÇO\x0017£Î£25é\x0011\x0016VB,,\x001c9Ï6\x0012¸±VL>rÍå²5íá\x001b~\x0003\x0016\x0014IûHíî<,_cù\x001e,ð5\x0001\x000b4eTJLêùXu¯ªÙêUÝÇ\x0015\x0003ît\x0015¥W¡$S§\x00127\x001a.\x0010l+Q}µ\x0005Äû¾S¤(´ç×hàò\m\x001d¢[l²Z}rupyuûëõ§O¿íÒ÷VñË\x0002. Ó\\x0019Ééqxø1\x000f./Þ>¶õ¬â\x000bº¸\x000c÷¢D.÷Ü¦R~!\x000b\x001ddª&S]dN\x0010V8TT³!\x001d{94D§\x001bk»@¶¥\x0004ono®¿\x001e\\ÿtóiç{.nµ£ìaô XÅJÃ:ç&B¸Kýwry\x0010vvúè®úñæúÏ?ýgû¤"¾ë«»\x0017×ß\x000e"ÔÁù\x0015|Mû@e:õ\x001d®Éüí\x000f®þðýí?ÿñõúS¢t)±óëqô»Äï\x001c/ôÆ&K`ckI.þôÓã?|q|yrúÝéÉñÛ\x0017'o\x000e"äÁù1\x000e{}t/PC\x001b?	ÓBðyªe¤õéVç	%6ÏyZ\x000b6~\x001fµ@´:HFX\x000cøBb¥j\x0012«=\5þÍôcàótý(Ø¨\x001e5\x001f¬²£`UÎ¬E\x001b?Y@­$Y«s\x000b
ó2Ô([åW=\x0007ñW·\x000bhcP%ï(Û\&dKú3ÊVä½skÑÆ¿[@\x001bh¤T­\x001c
EÙÚ<RÊj\x0017Ö¥¶Ö/¹c´Ì<Ê6:DëiNL<	A¯zn£.\x000cã´ZØÕ´8ÛÓÐ¹õE¶V¯©lÑgK5{ÃÂUéQ<	Wæ!¨Á\x0014\x000b7JwM\´d\x000bLYj£ÌgÁàäÅ$]ôñHãÚ\x0000k\tzä\x0002[CU¾h.\x001aa &³«âFK&\x0017X3#äaö\x0013´&c\x0006R8:
Vg\x001fp-Øx®ä\x0012sGÁé5ÙeEÙæz54¾kj\x0005|K\x000c\x0015y\x0013o¤õ6·¡93d ¢\x0019VkâF}+è\î²\x0016Ãä&µ@Û±#®^óÜâC&,QbÑ
÷ùàb\x0001RÚrö,0­k
\x00174X \x0015R×-Y\x0008*9´!×A Xõ(àë',¸gZeó`â}Kifì¤rä£¹[5þÍ`Á-Ãé,>ß2[] ã
>\x0008QÃ­znã
\x0005·,u\x001ffó`T\x000cÌlÆU¥+s\x0012e\x0011îGáoÝ_§ÂÈó«oWnî~c\x0019bô
Ù\x001b×ñReÛ \x0015\x00192ÌÞí\x0000=?~s|zöö|\x000eäV@ö4!·b§	¹\x0015$<MÈ-oûIB>ðZ\x0010åßÔÍõß?O§\x0007\x000eono7?]ÍÀÄ\x0012Æ´ýU\x001a=©É(\x00016\x001c%L\x0015ÿß8ààùÑÅÅÑËÇ\x001e=\x001bÒ\x0007Áö%}\x0010º>UÒ@ðÉ¢>ª,êÃ åÉ¢>P,êÃèä©¢N&O\x0016õaXò´Pÿòù÷>Û)O\x0014ýæç¸	+=êíAõi"¾+©áTÍj#´ó\x001aÎe\x0000»Üæç¸üêÑ·¾uâ9c>«r³\x0014X\x001b	\x0015c8\x0003döF$\x001d¬\x0013¯\x0019\x001drµ\x001f\x0008,6w,W«)\x001cñ°?î`xÍè`Å½é|\x0006lÞcKÅ\x001cçS\x0014¬y\x0006&Þ2æ³\x001a\x001bgSzÂçÆYãC\x0003§Û÷?\x0013u°N¼dt°Zsß1â)Í\x001dÈV\x0019ô("ÖDxÆp²>Bç¡±öF±:³æqxÄÏê¤IÝÉÕã\x0011HQ²#ýàìÞÜj\x0007ëÄ\x0013FÏ\x0011H«·\x0015[¾!³F-\x00016Ûî}yÏ:ùÑ\x0001õi9¼
ØÛOwKå¶ï\x0008kÅÞç\x000eØ©ç>\x0005KJ+`µ\x0011\x0019.k\x0019FP¬\x0004;õxÑa¹¼ä'M\x001ft.j:ÁæqÛøüâV´\O\x0017óaq´$X'ón\x0016«¤Êk­"¬ôï×µþÏÏ¿v_\x000eN¯½ºý²¹\x0001\x0019¾¼ÁV:üc~\x0015Ây\x0004«Ô>;{pzòîøâõÑÉ,Ú\x0007\x000eL7m>´\x000e$ÕÅ%ZÍ´û}´\x000f\NZwhT¦Å\x0015&Ó\x0002\x00194µ{MÚ9.ZlõL«\x0004å«qB»!ZcW¥}àÆôÑMmVÓÓ¶Ðôn\x0011aÃªÇöa¨\x000bVÓ
S<Y¡-=e\x001aµ÷µm\x0006êÕÏ7ÿù[*\x0000Ç±Þ°uh_Þ]\x0011wEN\x001f°ìTÎKí,¶mìy_9xùöäÑæ³\x00062~y0O\x001d2\x0014pO\x001d2z\x0014\x0010$¤õ\x001f>~ùå±\x0010ûûO®nf\x0019TÏg3hV£\x0010l\x001e<\x001fÝ\x0000¿?\x000eøþôèåñÙ\x000eZÁNÄØO\x0017v"p}º°\x0013ÑàÓ±,ìdàòti§§K;U\x001bôti£UÛé¡'Fûù¯Þýþ÷Ú0\á+f"¶¸\x0007/g<Ì\x000fñ/'LKë/·1ñ
3bîË\x000eWd
0!\x0005)OÔ\x0013&¤`ä©\x0011Þm6îÏbÒúÿúï\x001fî®?]Ý^Ïrõ¼¤¶\x000bì\x0006§\x0014µ0 8\x0014
{îõÁ\x000foON/Nf±n{P¬"\x0001"«Â1=ÂfG¬X´¶uk\x000cú±Áà)YÏ¾úuóS\x001e3º\x000fØèGÛ\x000cìiêÅÕ\x0016Ä\x001b¦Î@õüãwG/\x001f6ZÑBM\x000b£´*¤\x0019ÖqQ¸dáÉ\x0013;B«jZ5HÛ@²µ*w]Yá÷|\x0018ÔT2mW×¼z7Ì\x0017MiHo\x0005fÔ3®S÷l\x0004×Ô¸f\x0014W\x001bÜ­q¹ûBà½#^3ÙÏ0Âkk^;Ê\x000böÎ.¸Cs)N²\x001aÓz2[Ù«ÄfP¢Q÷üæóçë¯_7×·W\x0007¯6×?Ý^}sçlÚ©ÜÚ\x0019Ê­IirË¿5ÆÁÔË\x0000ôy~öêÕÉååÑÉÅñÁ«£\x0017ÇoöóCÍ\x000fKù±5\x001f\x0013íi\x001cxä·|¬|á\Â¯j~õï']óëü8*Ú\x0013?®\x001bÍ\x0016\x0006ÀÓû\x0007®½]ßÔüf©ü½ÀG,O÷Vâ`ùë©¼ý\x0012~[óÛÅòO{J\x0013?ÐÇ(E©q\x0003ý\x001dKð]ïâã4ÿ¾é\x0016eñ0õ|¶?Ôüáß_¶ê©þ÷¸¡+ócK¤ã\x0003de\x0008+©­ù:\x0012y,@=GÿõÍ·Hÿbóy7®¢êÌ=NIÃNÑäZ\x0008ìÝ*L\x0013WCõ_½è/^=î\x0017n¨¹a	wtÊ
¹
¸yG\x0013·0ìÙLzb£ÜªæVK¸£×HÏEø+äwya¥`ÌN¿l
rë[/âiÝ`rÔ]3aG}MyÛ,áV*
¯¢\x0000Ãfn\x0013J¬9ù <Hmkj»\x001a\x0004Õ\x0018ÄSâ\x000b5qEîéx~ÛÕÜn	7ª?Â\x0006~\x000bÅñD|¸'Ó%Ô¾¦ö\x000b¨Óz\x000eº\x001b&\x0005nÓdì\x0015©CM\x001dP{îLmë\x0006(ç\x0013 Äv+j\x0012\x001aßÃ\x0016G,\x0012·M#¬ê¬J\x0016lr´YñRÊÖT.²\x0002¨\x00188§ò\x0004®ùN*»&vc)å2S\x0007¿%ì4Õ,\x001cUä-&\x000b\x0006Á\x001bS)\x0017ÙÊ-xc+å"cù¯\x0005o¥\d-ÿ%à[kqó\x000f8	óòêæö'»u\x001dño¾ÌÊÏæ\x001dè~G\x0017Öp~¡
L\x001aKt¿_\x001e]¼Äi\'ýìõ~b¨a\x0018=(÷Ê¥44Ì'íÿXXÕÄj\Æya\"ÖôÀ %÷ADâÉÞ!b]\x0013ëabí¨É$å´r%|$\x0006UrZ«\x0011Ø\x0013ûÅÂIr,cÅa¤ö¥!º]MìÆ
¿5`àNÃ\x0010$Í}Ä6þõn^¨Ã8ñý9v´;\x000e
ËØNÎ \x0019!­v\x001bWoÊâ+NBªÈÃG¤t\x001d\x001e3Ü(\x000b9®-°ï \x0011óäÁ\x0008,\x001c
;YÓ?ÄÛ\<9~óþU¼Íµã÷N\x001a\x001aS\x0015m_\x0019X&\x0002{ÐÖL\x0006ãCÈÍ½ã\x0017\x000f'Âe#m¼`U!<G´ÖNv Csñ`üâý\x000b\x0007ã\x0017O\x0008NdàóçÌOëÖ«Õ«\x0007ÃWÏâXËL³Ù]VÈÂòÓ
>}t#7·\x000fo
Àé\x0002+\x0003\x0015QEdI·öv¬AÜ\>\x0018¾|i5EîT°ÑÈü>&\x000cûBNNö× «æò©áËgñIë+³û&¸|ÙD½S_&\x0000\x0017Ç'\x0000?Ißþ½T­n~&UÖÍ§i(Ð·ëo_\x000fýó\x001f·7¿]ÝÎxvÇ\x0005zÔ«µ\x0012ø\x001eÌÎP\x000f\x0003DWy2Ýf\x0002½9ysyðìøâìOÇ\x0017ÕÃû\x0016kQÊ\x0015äd\x0015[Æ\x0015'\x001dä\x0002Æg8¥÷ãÿü×\x001f}~\x0008ïí\x0016T\x0012æ^`/Sn\x0019Õ6Ï_Æ6Òéúûãg8±÷ÅÁÑ«gõ\ámFU3ª§ÉhjFó4\x0019]Íè&c¨\x0019ÃdíyF6F>­[\x0013ÿ^[Y±ø\x0003Î]n®¿|;øþzóávN\x001eÏyYê¾¢í§z\x0018W½|Ì\x0006]\x001e¼~sðýÉÑó\x001d	<F\x001a\x0015Q\x0015U\x0000\x0006ÚèXùa1É
ÀnVU³ª!V/BZ@ êt$Ø¥ Ý¨ºFÕbM¾\x0007Ë@]©²
+±ÚÕUÂ!\x0000Z\x0018R-ÕgB=æPÏC\x0015n;ÝìÊÅúãÍ×«_~þÃ³»7sJ=¤Vü\x0006$äJk¥¸^\x0002¼yìjýñìòøü¨\x0004Þ¾8ÛU¢â¶SÍ®Ü­nZ\we6Æ\x0019Vp±\x0001IM5\x0000«jX5\x0006\x001bÿ»´­\x0005a\x001dWaE'WÑíR\x00035çÃ¾\x0017Æ5}\x0016@Ý\x001fÏÞ|þ%mêÚ\x001c<¿½¹1R3:æìâÖ©¼¸Î*)¹;À{5YÈuªG¯ÎÓö®£ç\x0017g'ÿ{Âm6m\x0019ð³øìBE¯\x0019)\x000e^nn?Íkä\x0004j\x000e0\x0018¯*â\x0014yePä\x000cÓUÑc<xytqZu\x001bÑÖöI!
\x001f¶\x001cúh\x0015Ñ7Ù\x001c|s{õíàÝõæn\x0006ò1jNx\x0001Wuf<0¼ @Úé>£ïÏ.ß\x001c¼;9zû8ªáÔ\x0013Ó5~
pðãßü_~\x0012¿ý8Õ6³9x·ùôé*Y\x001d*Yï^ßü¶ùòí\x000f\x001fÿ£O®¯n\x0011L
|mÁì	\x0001\x0015OÚm/ut\x0011\x0013Yôò«áë³?\x001d½~óè´\x001c_Tm(G\x0007ïâÏ\x001f³;
ævÇL\x0007f^
0Èõb2ÉêÕAd\x0015¾\x000eæö<ù÷*FLnêÒ\x000cù%\x0008×HÛõ0·GKt`b½	\x0010&.BÊèjH¢4_r»\x001bºÒ§Æ}t6g8"eÈ³Ñ2,¥útó×ß¿M] W7_¾ýõîúË~HmRû\x000bRªÁi£/®E'ò(å«³×oþ×ÛÇ²\
äÖõéti\x0000V4iWv´y\x0019uz5È­Ë3\x001fÒÄ\x0008HfIj­ò¤T.X:xÉ×Ü'0\x001fÒâ
,I\x001dõPzÊ!=Dõ¶«@nÝï\x000eÈ¨¼4\x0019R9³\x0012¤×ÖW·T«²®\x000eÎ?mö²æÏ%
é´p9ÊÀk\x000e´Ã\x0001ýSlÇ\x0007ç§G\x0013}ùýfs79r\x001dGrþ|{ýõÛ\x000c6ÇÛE¶\x0018Àä &²QivÎ¦Ík\x001cti/N.\x001fó½áÇO·¿ÿe£)áÓl_\x000fbðu?\x0016l¨£\x001c.jB8°¹;#Þp¶t=\x0014ÜåA
.¿û°ù¸ùú-\x0006¢ü\x0007BçÌWÎaþ\x0001J0þÃÿù¼íÕõç¯\x0019QÉ®x\x0008ÀVZäùe8AÒLÉ/)é´¥íÕÉ«³Ë£ÇÚÖ*V¨YaUâê¼\x00153Â:wèóU\x0016.G8ó\x0014\x0007æ®A«jZ5(Y^Ä¢õ¬\x001dÌìpÐXV×´zP¶Ò`e¢¯É\x0006G¼Q\x000ee\x001b¦nù\x0000­©iÍ l]H\x001b"­úÝg})/²Mc-W µ5­\x001d­\x0008ä
Ç \x000fAgZÍ°FMÉ\x0001XWÃºQÑ*«Ï«©Q®õ
+¡ú\x001aÕ?õ3\x001bjÚ0(Xk1Õd+u(£­¢õò¸-H¯£\x000f\x0018ì\x00185\x000cîPð\x0015Xµg\x0004âIh[+6jÆlzQÍÂõ¹6
6Ê¡pý:\x0007W6L\x000eY2\x0014®È«dQ¸©© Ý1Déº)×`\x0000·±drÔá¤ëlÊTô\x0006
\x001d]gùèæá
¸)C¶\x000c-ozÉAæw.´¼ùe\x0006\x000f\x0003¬ÛØ29lÌ$±
\x001cyµgÆMzþ\x0003¬%C¦\x000cY]zK¸4R\x001c
+¸v\x001d+\x001b[&GYô»\x001dáÄP!«\x0005\x0011øàNF¨\x0003¸=C\x0006
¥\x000bL+\x000eñµ\x0005v\x001d§F6æLÚ3e\x000eTn\x000cÃc/É¸a2öêÇÆÁ¨=CóK*\x0017\x000cGcùõ+:Ð\x00184\x00185h¸\x0012ÎBÉ­@ÐF#VÒ\x000bÐFf£\x0006-Ú_rq\x0015\x001679¶¿ì.ø°ÎÙÆ Á¨AÃé=äÜhÇË`NÃ\x0001Kw­ÃÐ\x00184\x00185hÑþ&é<È)Ù_6h|\x001dÜÆ Á¨AÃ~|Ò\x000cFå\x0016÷\x000b´®/\x0014\x0003¸MQe$]\x001dÏ.I×\x0016\x0013\x001cüJg·±i0jÓ¢K#É\x0019Ã\x0016k\x0012®à£+õJg¡1i0jÒ´Äk\x0016®Éµèh%ä¦VºiQQ£&Ì!©1«(¢\x0004ÞEÂ
ëÐªÆ¦©Q\x0016&#a\x0004\x0011hù¢L°jl\x001a´i>øCGZ×úC:
ô \x0018ÍïJi\x0010ÕX45jÑÀãêì,[·h'\x0003Ì\x0007W®\x0014D¨6Ù8hÑ¢}Å
Ä	×©\)/Á\x0007vÌ
¸uâuÕX45jÑ\x0000Òºt\x0014\x0004Î÷Ï\x0006Øðav\x0000X5\x0016M
Z4ïm9\x000cÎçNÝ(]ï\x0019WÁ:JW5\x0016MZ´\x0018\x00052ÀÖäå\x0019É\x0000³ó\x0008b%ÜÆF¨Q\x001b\x0011\x0003ß@jÌ<WAÒ8\x00085ë\4Ýè\=ªsNë(\x0012,u£à8ÂD¯w\x001dÜFéA5tn¦ÅÆ\x0014½¥s^Ç@èö
bP+ø\x0000l}½É«Q\x0015¥°ÐÍ%ÓÌç\x0002!
ÑöÂõTF\x000bÍzPWæ\x001f©àïåævoU\x0008\x0006w¿¥gH\x001cwGî­¶!\x001fX\x0017]´©ª4ä+\x0015ú½<z´Fµ¢\x0012F(ÙQt.hìúÊ@ò\x0014Ó¾L/¦ª1Õ\x0000¦âÌmÂ\x0014$MÀvêöbê\x001aS\x000f`Tr1\x001d§\x000f´f·[ÈÉ\R/¦©1Í\x0000f4Tâ\x001eÒöÕ\x000e\x0014{)mMiG¾¹ÄûwQá7WüÍåd¶ \x0017Ó×~\x0000\x0013\x0002Õ\x000c%LúäÀI`ërÊPS~J\x0013ï!/Îáà%ÆqS®I'eõ\x0004\x0006yèS¿0\x001d=y8òH>.Å½Î#J\x0013ûéù;N\x000ci\x00011'½z9\x001bm$\x0007Ô[òWXN¾º\x000b|Ñ\x0001Öàl.º\x001c¸é:ZrM7]¦*sr
^^A!Éæ¦Ë«®=Pî=r\x001azá*¯\x0002ì
ú\x0008;\x0004\x0003wHÇ@TðWwTM\x0000ë\x001eâ)]A!Aëx\x000c\"/\x0003¹NË\x0003\x0017ß¢½øê²\x0015æ\x0012ÁÈ%ÂÉôÑAócÂÃÄ9Y\x0013ÚËÙ\"\x0018¹D ²cì<Ö§gLðÅC®Ò)ë
	ù\x0007Wüýæîë×«ÛÍ\x000cLf\x000f&Îè-¹|ÀPyÇòÖÇ9¿?z{yy|q´\x001f\x0014jP\x0018\x0000u ³ÿî\x0005èåãi\x001dî\x0004·Ë®ÏçT5§\x001a\x0011hô?D.Æô\x0016òä(ÐÀÅCÑ3^E º\x0006Õ#\x0002þ\x001c½¹KEÝQ¢ÞbR¸et\x0005PS\x0011ZÆÛ'¼^\x0016\x0015(zá&sýÝ ¶\x0006µC\x0012õi80VbáºÎ|lÐôéq-Æ
®æt#\x0002õ*Cwå\x0011X\x0019Ç\x0002õ±nP_ú\x0011j;)<Ä¸"\x000e'XÕkp;Â·ù¡æ\x000c\x0003¸¶]åä\x0002fñDþðZ\x0005ºJRÊ5@+\x001eµ½\x0018¨HÃoP¤Ú±HÓ,Òéw³nÒÖ.\x0018&kKqX<òÔF\x0003&°S/Ã.§~>icäeòZ<s0¬¼â||sè\x0006m,\x001c1M8\x001eÊ\x0004ÃìXÉåÂ ×° ²Q£rD¢Ãdò½7AÒ\x000bRáÑæ¯"ÐF=É\x0011ýä1
\x0005éE/ÔP\x0008âÒ¾ßÅ¤Ð|z\x0018ùôÎ¦ö©\÷\x0003l\x001cÑøñ×øöÐØz\x00181öÎû48jRrM{tîByÌìKë&m(XQ/5[{å$¿éÇ`¾¼5Ú5)4Ö	FÌW¶%áCH~Ï÷Àý-fòi©\x0017T5:_è|\x000fyj\x0004Õf¢ã}â 	ûË× müû!²Î¤\x0006\x0007d]ê\x0005HX3ù.ÞMÚ\(5r¡uR8=HÉâÇ\x0010jGd>is¡ÔÐ®¾qÓx1R¦cê¤ZöõÜã!m8N¯?Íj¹0¦(©\x0008Ï©ÂÚÝï§'§;¼\x0008\x0014jP\x0018\x0002µ÷:
\x001cEÍJÊP@'ûº»IUMªH£7jÙ@YªSâ¾\x0002<º\x0002kêTrÆÄãR>?¾ð¾Ô¤î)PIjjR3F*©g5£Z*S/ïÞ{ËQgÚÔ\x000e*]¾~<\x0008YIEÊR:qî&u5©\x001b#5&ME¨åë\x0002ê°
¨¯Aý\x0010h´¥lôqú;ÕÑ;(Ô^ ¤¡&
£¤¬¤4·'DÒRÖ;6é\x0005­gTûb\x0014ÊÇ7J3TT²|õ§-T7jk¡ÆL\x0014NÂf-eÈç¨¦Ü¨5®¾lL\x001c³Q²TØûÞkÃ¾©\ÅÊÆBÉ1\x0013\x0015AY¤Fäå±\x0003}±§]m&jc¢ä"M\x0018OBu8Ú%÷ÚÞWM¾4v£66J\x0019)Y2RXa\x001a\x0002£\x00030év£6FJY)¡èé)UÛ\x0017ýRô¶¢j\x001c°RØY\x0019½RUbS £
Ü*a`\x0015=ÕX)9`¦rmp¥¦TÐIUê¾¦twÝãLÔÆLÉ\x0001;\x001b*):Å94Fp§\x0011vJÝÜ~¸úå1Lh\x0014\x000c\x0018©<q{¦<uF %Û}=Y´Ñ+Phl\x0014\x000cØ(j®vEKYÅÍÕ÷ZjwîLÔ6\x001a0RY¨\ëyIj©%|tî&m¬\x0014\x000cX)$µPÎò\x0010xWËZÅòCc¥`ÀJåù\x0015ìõ\x0007U\x001c?\x0011Jñ¨Yåû7V
\x0006¬\x0014vö¹\x0012JYU:ûB)ÔcNw_ýÆ@ÁJS+êD\x001fûüåÁÌ=-g3\x0005ÚX(\x0018³PNóësªr&\x000b%JcZ%<ÆDÁ²
\x001f½¦D\x001fvn°H'ë\x000eº9\x001bû\x0004cöÉúÒd\x0016$7¿àT²R½HUc£Ô²¿>Î¢Nø\x001fØHMÏÈëFm\x001a3R¸Ò_÷,öËfÔ¢£&Ë·ºI\x001b\x001b¥Æl\x0014Î§ ì¹T¥\x000fÎ\x0015Ëo×ùþm²oÌH¼Ñ$}Yºæ5Ý3·h&h£÷ÕÞGGÏ\x0012¨ájPm\x00193YÐÚhT5¦Q5V;ç¯/J§^é\x001c0v\x0015¿O5J)*L£¸ò`î¹í&dâ\x0013òí4§º¹úzìê+wH4þÀM»EÚUçº¹Ozì>c§OãâO:¦ºÄ&û¦*ÍDmn\x001e»Q`ïQmi.Ö}\x0014·0Ñ\x000fnë':(íçÿãæëçë/3\x0002~\x0019tZ7
\x0011\x001f%Àóó=\x0003\x0012þxtùêäõ\x000cZ¨ia6*¨¬\x0001,®:ÎÞ_é tJïVU³aU
«\x0006a=ß-ÜtFC\x000cÁs*Å)±ûnÍÕ5¬\x001eµ\x001cù[\x001cOa]9\x0006Z®t\x000cL
kFa%Æ§ù\x0018(êÙ´ªvràæ\x0000­­ií(­àâ)+¹x*Òòó´ÓfwÈ2ÖÕ´n\x0016w\x0006\x0010­ð<F\x0017¬)²Ý\x0013µÌ¦õ5­\x001f§
dË\x000fêH[Îíd)ò\x0000m¨iÃ ­
Ô\x001dãq\x00100Ó\x001aîÝwzÏx¹´u[Û~	êÀõåEk>#.\x000f6ufOSñlÜÖ2ÌZ\x0004n^pKÝMW)\x000eà6¦LÚ2\x000bì%X%\x000eI¸XÎìy\x0013MÛØ29jÌp9\x0005E]»\x0011\x0007¬¹}/\x0003³q\x001bk&GÍ\x0019â^P:/ílp÷$²gÓ6æLÚ3S
l~ÓN´
p÷wÛØ39jÐ°&pu
\x0008¥5Ú¹=oÄ³q\x001b&G-.\x001aV\x0001ú\x0019ßÝ3am6ncÑä¨IÓå	Îâ %òÈ\x0007Â¹=áølÚÆ¢ÉQ¦kë±Ç;ÑJàö\x0004si¡±h0jÑb¸K£\x000c­ü¾\x0005÷ÕÌ+Y\x0008h\x000c\x001a\x001a4öÑä\x0000y6Ò
v\x001cÝ\÷lÜÆDÀ¨`ÉjÇEC TaÝ\x0013Ïfm4.j\\x0000­fb/7Eu"\x0008hT\x0018ª°èÏP~\x001e7\x000cÐ`qéù\x0019Éù=3Hfã6J\x0001FÂÿuÜv\x0013%4(?^á\x001eo/?ÍYÞ¦åPw¨b\x001cJá¸Ð»Ú\x0006Þ\x001d¾9zýòx\x0006)Ô¤0DªÃ¡¥¶`U\x0012µÒó,K¡õv¡\x000eTU£ª!Të¨ÞÍa\x0003	¢\x0001)J\x0007óäxù~T]£ê!TÜZu1ç<½¼\x001fG£'\x001f>ûQMjP>¤I\x0015¥Ò\x0019xû 
Õíh_ï µ5©\x001d"\x0005î\x0017s¸Ð*O(<®_ìj_ïàt5§\x001b»R²S(ã\x0015p¡;t25ÓêkT?
¸pRy*&w´
ÏÑ­PbGC\x0007j¨QÃØ×÷4«$¿~(RûwÞ'9ò\x0017\x0003¨\x001eSõ6K\x0015³]6éT\ùY\x001d¾Ý®ÂÚ¨9¢ÿ£,Ã¡Jrµ>Æ´i§\x0014NQÿqÎ*'@6UV/uy¢uÑuM\x000e@¼LdUØ5·d>)4'\x0000FNÀ¿´5ÿ#ßÿ_EÚX\x00181ÿ\x001e0qlòIÅ<g
³
Tïî$ìjrë`ml*\x0018U/%\x000fÓ²1ú£'%a¨\x00137
·Y\x0005µQ«0¢WÑÀSõC<\x0000ø¶¤úÚã÷ÌiuªÆ§V#NujgÏ[,ÓQÍ%EB\x0017µ*¦_êg³¾\x0017¡Ý6ö,þ`{éyÄ¹½:8¿ºý0g§%æ\x0006|öY0Á\x0015(T®å¢\x001f¸oõæyüÁÅñÁùñÅó\x001d»-\x000b¼®áõ¿\x0019¼­áíBxÁCÃ$Îë7; v1YÉ¿Ý×ì~\x0019;¶àeöèþP~rOÊ8|ñz\x0012<z=Kè±ß#I\x0011Aâ\x001a¨\x001c¨\x001b:6j2×¸\x0000¾¹¯rá\x0015i¬`Ç\x0001d\x0004ï(çìN_@ß\X¹ðÆYÈ>FËè©ÁÖ©é­\x000bè\x001b+\x0017^ÙxÖEÎ\x0008\x001c<M\x0019\x001eÜaéõäpä\x0005ôÍ\x000b/­ÔãD©%eÿ,\x0005¨N©é¡¹´°ìÒ`h°¦P<ê@IS\x000eÎdãË\x0002öÖÆ.»³\x0002§×äUÒ\x0019^\x0017x1¹*u¾¹³°ìÎâEÍÊÞâb7<\x0016\x001d%ø4únUxÓÀ
çÌ$ÉcÊôM`;e'ò\x0005ìºeêF8ICZq\x0013?íKnör8l]úFÝÀ2uòö|l\x0002÷ÔJåIÝ¤ÉykÒ«æÐ«^\x0005¬^OÁ\°TÈ®\x0004o\tr%]s¿·Ê\x001a\x001dl5]]útõmÆ\x0013\x0004¨2\x0008
ßÎò Z¥T)µÁúæ]O\x0010gÇ'ñÏov=\x0010¯ªyÕ(/Î0áIA£
\x0002Þ«åö=ûÎç55¯\x0019åúþ%Õ`iHâågÏæù¸®Æu£¸¸äp­àgj%xLºó{ú°æó7\x000có*Þ[f£\x0003hußéÂd¶wW¶×mô¾Åø\x0012©\x00118Ð0kt\x0018xOIæ|àæ¾ÉÑ\x000b'=ç}bæØ\x0007\x0004Ï³Þ=Jf\x001dàæÂÉÑ\x001b'(\x0016.&Ã
zøX±\x0012psåäèKå²\x0000\x0003W\x000f\x0016\x0001¯¤ÐdsãäèVóü8<\x00103e9\x000f5ÜÎ$åý£õ×ç?o>ÿòõàtsûqf\x0019m\x00010 hª\x0004\x0004\x001e¿ìÜôâæc»<xþÃÑ«óËh/^Ì@\x001a\x0019µà1·F\x0006Î\x0018øD¸é¶1`U\x0003«1`Ü\x00008@4Ë\x0018Êa#e¼#Ù¬kd=,\x0000G
f\x0019\x0003\x001bf¡\\x0011ò	ü½È¦F6ÃÈÚßdK\x0014Ntd)ïÞ×ìjd7ìºû\x001cNÆõöÓ4#	\x0017ð¬wù|ìG%ÅÝ&\x0006P\¥ÇO^LÉ\x001aÃ
5n\x0018Æ÷-¿vaõkÉ±C\x0011'\x0017Ç
!WåòRV/ÉÝÌ\x0016ÈDGUVN\x0005hK\x0007ÙÃ¤9ÆÜZA3+¥Ë\x000bxÊÃçÚc\x000eN½¬\x001dcn´²\x001cVË8è\x0016$8£°\x000fµåÛêjÌÃJ\x000e'ÿøj;W6%»¬]\x0008j=97JN\x000ek9\x0015µ\x001c/\x001f\x0001üRe¯ÇÙ¿½ÈÖÃjCKÍ9ímËæ/ê<.ó;vt2C£6`Xmàô¥q¦\x0019µ³YÍ-Wñ¾ÚqFmÀ°ÚÐÆ£NÎÌe¢--\x000b;fÃö\x00127J\x00036)h²4\x001aJ~mT\x001bL<\x0019?u2ëíU~:Õ¥Ú|Ðw\x0007¯6·\x001f~þç?öûÊÆÑb\x0000[,¨8ªcV\x0017f²{ôüôèyä}{ðêèâù\x000f»mz{Ne©\x0003 1´ÚMò¤XÐR+.¨IÅÖMªjR5*ÒÜ\x0014ä\´ ÊLÉ3Æ-\x001ckê\x001aTÔñ¢"'%ºÊ"¥²Ä(ÒIÅÛMjjR3&ÒTlHµ¤W\x0005<¦|J'ýÊnP[Ú§|J]MêFEjh?¦\x0011¤§\x0000\x00037vn&ÁºI}MêGHm´µ©Ò<âÄ(\x0010îÂt¨ÙM\x001ajÒ0$SLIÃX	À²\x0018"õ¥Ó½¤U\x001c¡sEêP
NE¡\x0006NëD§e:Ù¢ÔMÚ\x001a¨A\x000b\x00058v3\x000bUaeZ{÷qiö
¤Þÿ_BÚ(~9¤ù-îI¥Ë¯KÚÞLÊGé&m\x0014¿\x001cÓü^s
\x000bWÂh.|òiêË
¨êCº\x001f'\x00038ÒýVãÞ,Ô¢ûýäcJ7j£ûåò÷Z<pK%ÃïyD¼X\x0007´QýrL÷c ¢FeÝ¯\x0001F\x0000ºQ\x001bÝ/?\x0008\x00012SÇE;'_ÃFùÃòÇut©§7(UíK`
ÒFùÃòGÛ/Y¨þPÒî*u¿7w²§\x001bµO\x0002\x0014]ÁBõpÈ'ÕòíÃ×
Ú)\x00182Si	þ\x0010¸\x001bÉ(\x001eÄåk 6v
Æì\x0014Èâú9ÁKÜì¤úÉsQßÇ\x000fß\x0004}Ïð$D¡^å¨?­]¹¹³¥4hs¨s$\x001d->/1
\:ä`²Áóô8GüiïÊÙI½¨tÑÔf1ø9â´N;ÈóÄ0Ú\x000bã¬÷\x0015Bó!]
éÆ Aåõ¤N+Qf/ê7ë&\x0007t01\x000c1zëè\x0011×)#\x000fi\x0013\x0010_u+&7½ÎG¬¯#b*¾\x001e``y\x001e¸S¢L²KfÒX;YÌö2O\x0007ÜF\x0006\x0011\x0006\x0011¹ÓTiAÕ?5¾\x0015,£n õày\x0014è #%\x0004Ç¹ ¸oÀL>'w@Ú\x0006Ò\x000e@â\x000br`7Y(\x0003À
×]\x001a7Ù	½R\x0008«¶RñoÞï¼úíæëÍ·ë£&\.~Ðþ~äauVíQÿêOggoNv¥F\x0017j^XÀKÅ\x001aFDeTFcPôa÷L¦«j\5+xn±Á\x0012ÕlàEÄvßàÂù¼ºæÕÃ¼pèt\x000b.wðZ\L¼\x000e®©qÍ(.9º\x000c0®(¯-±Ê¯%^[óÚQ^éø8` rfÏèí¾å\x0015óy]Íëy-\x000f|Âó@»V$:%|\x001evÍçõ5¯\x001fæ-Å´FR£dÄå¹9vßDãù¸¡Æ
Ã¸²ì/\x000e ¦\x0008,¡%ñîV6·JP¢±\x0010£ÀB\x001fæâT¬²ÜxÅ\x0003ã­]ËXÈÖ¸
[7*¯²\x0014ô\x0012UYe¹\x0016ocÜä°u¥ú×ÄèªË~\x000bë'&x\x001f\x001fM°i£¶Mà¾U\x0016®áZÒrá¤5ÍÞ#Òml\x001c5nØéHu©&Ú9î1¯¬Ý\x001a\x0001n¬\x001c5o"¤Kï æØñÅ\x0012^K¾q£ÖMxËcË²¼÷Bòâ\x0003ì]_·1nrÔº	|Ã$k,|©4S¯Û¾3¯[cÚä¨m\x0013XûMÒÕ{Ð4/¼´û\x0006ÍncÛä¨qÃæ'EÒÅ>oÅåðî'<\x001b\x0018\x001aã\x0006£Æ
{5\x000bØ^³²²ÉN>\x0016ð6Æ
F°Zqq WiIi3¹g}Ç¼ã\x000bmÜ6jÚu´
Ñ`\x001at\x0003p×õ¹ø\x0011é6Ö
­\x001bÖfu+Ï±
S|ßölD\x000fÜX7\x0018¶n¸wîq£§ã@Id\x001böÌÞ\x000fÜX7\x0018¶n8\x0007YÓ}Ó¸~2\x0003ó¦\x0014»¯l>pcß`Ø¾aË8]8\x000b¥ö»¤JÂj
¢±o0lßpç$+´@kS"o(îäZ\x000e\x00044&\x000eMöåDDuA
§¡L\x0014kEÇÐ8\x00186q8æ­\x0014R\x0014\x0013\x0017äJWN5&N
8
´G\x0007+#È\x0014e°+YdÕX85lápí\x000f_8Qöý\x0012¾=ûTæ\x00037FN
\x001b9uï\x0001ãl\x000fÚüVz\x000bÝôCÞ\x0008p\x001c¶r8º2\x0010Vcãt\x0006¶å\x0004Of©G\x001b+§­âN2o|µúÛò¸áÕ\x0004Ü\x001895läÔ½æ\x0004	\x0012eq\x0013k¥ TcäÔ°\x0003ÍÛ	°\x001aU\x0013°-ë	`ÏöùÀSÃV.\x0002{\x0002v£8a}ðä\x0011àÆj¨a«\x0011uOVÃ{	sGº\ëI@7ZX\x000fka¬ö$¥æõ!·Brã&ß\x0004»x};Ô
P7ÆÑd\x001eXr?¼yM9®K\x0012;Lã¿Ï\x0000T5 ê\x0006îÈ¯«ö¾vBI®îöagØ<D]#ênD°\x0017Ërz\x00008Ë¤¸³t\x001e¢©\x0011M7¢pÜk
ðw\x0006K\x0005HÎO?¬6\x0004¼¾pøl/\x001föN\x0019 shié;îÈ`\x0011ÊÉ¡/\x001d|®æsÝ|Êp¥u\x001ax@ZzÓ§0<>Otî'ö5¢ïF\x0004 7Êá\x0000\x0001Ã%×Bï\x001a$=\x0013±z\x0011ñ¾iýÇ\x0008!=Ø$F,2'Fi\x0018wLË(\x001bFÙÍ³°\x0011çæO\x001dí\x0018+\x001c7¹ã¯±QÚ²[kCYÞ\x0014å(©\x0007\x000eÓÜê'ÍËLF»ÝBdëÁö6\x0007¯®¿Ì¨8ÁN,êvñVò´¾\x000c6·»&°\x001e\x001d¼:y½«>Ïn·åØzRü|LÜKÑRçú"'\x0019ÒO®\x001eít5¤\x001bô<$<`ÇC®Ês\x0007ò¤ÕrJ_Sú~J\x001fm5mVæð/%Ò¨5\x0019jÌ0Û\x0012\x000c.\x0001ÇÇcµórÊúñ¸·>\x001f\x0013×wg{Ü
UçqËì¿ë¥
¥\x001c¹>ëó¢ÖáÎ\x0006'=w6ÉÒæ^Nh8a@x·Ié2%izþæ~2éÔKÙ¨L9 3½àØ¶È\x001d-ÇÇy|ZYS7º3º´¥¡Y\x0018.½\x000f[/¦\x0007(÷b6ª]\x000eèöø]ù¦kIcíÀ\x0005ÏÂ|ýë¥lt»\x001cPî\x001eÇ8v\x001eÌµÂÑ>\x0012¦m{1\x001bå.\x0007´{0ì\x0018ÅSªËn,dÎ-áfr{h/g£Ýåz×mu4Ý;Z!W\x0014ç
âF½ÃzttÕ}ªp£\x0014\x000cï\]AÐèw\x0018ÐïXÜf+\x0014¨º_È¢\x0019Z³Ñï0 ß\x0003É9N\\x0010I\x0000\x0005ðj=\x0005O½\x0011
\x001få	÷òÌÙnçf\x001d\x001aÍ	#Ó6°û¸Éûðª(ø]«^fs6º\x0013Ft§çÝIÑ\x0010q±\x001aÚuÅ;fkÌçl't+ÏüJGo\x0006/¿"±\x0003¢q²ÆrÎFyÂò\x000c"SMòÄbPê[\x0011\\x001fAærNÕ¨%5 ÌOB©Ò¤\x0004ì\x001aÃ®Q;ó!Û\x0000xà®\x0007ìO&/IÙ2t\x00100arÍc/gãÍ©no\x000e9® Ô¸Ù>\x0017°\x0003»ð\x0016&þz1mi\x00070£¾ô\èYT<µöÖM\x0012ôb6*I
¨¤`\x0002%¹bðc99\x0013pÈOþên²¾¾³QIj@%É¨âÅýC¼ Yfë¾ÃäÈÑ^ÌF#©\x0011ä8¯éÓú,Í(e²ëb
\x0005¯\x001b¤G\x0014/Ïîèð³»äÔñ®p×uã'én?I
À}³4\x00187^¢_¦){ß§+öz9\x001bÝ©Gtg\x0000ÞI.£Át@þ\x001c¿ø)=9"¹³qt·£/©êìºräuZ~©Öb×JÄù^üïó£cåÉãOúSJ\x0012Mzv>\x0003Ý%,$#gÉí\x0018êÕÝ¦5C°\x000eý¤üæâÑ\x0005Íqã\x001dÉXé½Fô¾
\x001b#ø!ÑãwÊ\x0015NÔ§*ø^I=Y7Ö}¯¶qãÝêÇÅ÷iË-\x0000×¼\x000bSÂ¥ \x0017\x001d\x00050?¶í1\x0008ißÒOng5wXQZ\x00175eç\x0015h~CÁçîRoè	5&\x000cazÊ¦ªA6n¹ÊÑïéI©jL5iì!\x0017:î5\x0000Í£êß];\x000fS×z\x0010;g\x001b\x0005¸\x0006\=M\x0011ó8MÍi8ï«õ
`\x000e/sB©\x0015\x001cDÐËikN;ÆIÕj+gJ¬dÃä ^FW3º\x0011F\x001c\x000c}_Mü¾Ô=¨Ý%_ó0}é\x00071¹ßÁþÈÉ=br2^/g¨9Ã\x0008gtFî«®Ä)M)\x0002u+Ìê\x000bÕ»\x0018â´÷h\x001e<âÿHB´\x0015N§lÍÐ\x001dÂÅç,PÇ]§Àeìn:
éålì\x001c2D·'Eyz\x001e\x001c9K¡ÜnÈy %C¦\x0008øÙ=UKêm	üàÄä*È^ÐÆ\x0016É!c\x0004¥}7x\®\x001eJi§ÜÓ\x001e=³±ErÈ\x0018I_êê½\x0007åË¯qB\x001b[$¼ïWð	9sòÃIÏ³\x0017´1HrÈ"ÉòÆi<¯åU²¤ÀÝtÑE/hcäMÂx:¢A\x0016]/D÷´¬Ì\x0003ml\x001c2JÂÒÈ®T&MC¥¥ãæg\x0007{ÖÍ\x0002Æ*ÁU\x0012¶´ÇÐr95Vàl¬\x0012\x000cY%®dPvºrÔá`òM¡\x0017³
F\x0008*Á<\x0017ä=Ö²®W{êùç6F	F\x0012.Üdo$¤¥Ü¹w¼ÅÃdg/hc`Ä(xÏé9Éb\x00176){SºÔ.ìy U\x0011«$¢\x0017@%=Õ¨R\x001aA÷ìá\x0007Ú%\x00181KØ×j{ÖÈ½¶º|zmV°óÐ%\x00181KÂK|IÊ\x0012µ÷ E ïñ½U\x0011«¼S2|ÇK/½^#8Æ*ÁU\x0012¸#´S´¤'\x001apÓ²Û7¯g\x0016¨j¬\x001a±J\x0008Êw){Ï\x0019Ó·Î¨\x0015aª1KjÄ,	'øÝ\x0013G4sÏ/¸rVøòªÍ
©{«Ë\x001aFL2§à#jö4ÆÍ\x0003m´¨\x001aÒ¢¶t?YUÖ\x000e¾~z\x0017ÜLÎ÷ÑhµÏâ\x000f0Y{¿\x0006÷êàüæË·g7w·_7w¾Í!ÎÏ\x000c\x0010µ@ ÏY*\x001eã7f<-Kp\x000fÎÏ^¿9xvööâòèíéýèP£ÃBôìì'z°e\x0001±¦XNIoe	¾ªñÕRÉ\x0003nOø.qH§"éqtKðMoâs+eÄ×e\\x0016Ï:nò}r	¾«ñÝR|Ë#UÁÝ\x000fÏÂ¿ðW?û¡Æ\x000f\x000bñ¡é>ñì{ü\x0010ä\x0000[>û¯Ø\x000bðe«u\x0016ª\x001d\x0005FÕ ¨f\x001e#aÂ7b²|z	~suåÂ» ´Û\x0011Ôýá÷¼óÓÉìÝ\x0012þæðË§\x001f·îR=è@Å¢ø\x000eÆ§_N6k\x000eðG¥³½É¤L\x00177wßÒSè«´ËövVó¡¡!0ÎkÅ-\x000cÀk$¼0ÓKýÎÞ¾I¯¡¯Ò.Û]Ùn©2¹¥ª\x001f\x0016´Ç!È¹\x0015HÑ\x0003\x0004\x0008S
\x001e1u¾
¬®aõd£µ\ÞN\x001b\x0019â\x000e0l\x0013ègµ5«\x001dcÅü)÷\x0001¯=\x0014ÂO\x000eúè­^M\x000cu\x0006
\x001c\x0003|,	÷Ç ×½Æh{íc \x000b&Çn\x0018ð\x0008\x0015\x0017 tµ\x0008^)ã±{\x001dØæÌÊ±C\x000bÒð\x0002 \x001d%¨!
iåäÔ­\x0001ÚæÔÊ±c+äÚ \x0014Yl\x0019î»G\x001eiáï ÛV­"ç_î>\Óº\x001aLYß\x0008FñVkÏã\x0003µÜ3;åùÑùÛç'¯w6°Êm\x0005&ÅV\x001dB\x00170p0\x000bÆÓü\x001f\x0008e\x001cjt§w':mMl#¢Ró4¬1\x0001[\x001e­aÏ»\x000e`_\x0003ûa`U*fÁE>ÁX>\x0014JíN\x0018Ì'®¯\x0014ÛOÖ]È'¾ *\x0016T'¯¹#W«=\x0003>:'Ço\x001eV¨\x0001!;®PÃÑ\x0010¬÷ë@n®\x001c¿{ yô7e4¡¬MÕÚ¬FÜ\=9~÷¤æà-»<Ñ\x0000²×ºz²¹zrüî	îó³`H!K®³ÕÓÉ\x0011dhî\x001eß=*Z2²¡´\x001d6²º0{\x0006Øw ·Foøîy|\x0001cd~ôÆ¶\x001aF¶óM»\x0007ÃwÏçÞ\x001c°f<#ó\xmWS\x0017Ð\>\x0018¾|\x001e·e)+Éë¬Á;ö3µ\\x00088Ü\?\x0018¾~Þ\x0019\x001eP\x0003\\x001cµ\x0003ò.\x0006ìª]X5·O
ß>ïà¸¬ÜôN°ÂØWôØÜÜ>5~ûl ²w\x001f=	î\x0003÷{XõdÓ\x0010qsùÔøå³ÇÄ+ÍeqÅúG\x0012YCÈÍåSãÏ\x001a~£PQÞ´3\x0018Ô\x0008y_5BgßTÁ'ï\x001e0êàk|¢J®´Ap÷=\x001c{¦,Ï\x0001w®ybÁ\x001flÕÃÝn¾ü4#äÃçµr8´á\x0015
·³Sq'­]Àg\x0017G¯_îù\x0017j^\x0018ä¢8\x001ag\x0016k®¦!È\x0004¹[cÌçU5¯zúòÕ5¯\x001eå
\x000eÓUWÐViïnC=\x001f×Ô¸æé×Ö¼vX¼2oò¸;ed\x0019åh÷þÎÇu5®\x001bÅÅn¹¬£vÈOÅeýØS¯:\x001f××¸~\x0014×\x0007*¯ÕÆR\x0001\x0003Eºj­Ã\x001bjÜðÔ¥[%*ÐTañ\x0002Íq¼ª\6­|÷$æ\x0003·¶mØ¸ýË\x0004ÜØ69jÜã)w1¼üäÅåmVÚtlL\x001c¶\x0015Ñ±´kJe+pQ³k\x0019\x000bÙ(_9¬}qC\x0003m«ó¢dÊ¢~aOÑÓ|àFÉa\x0016ÝIÍÀeÛ\x0001\x0007ØM\x000b~aý ý!Ã\x0006ZöÛ\x0003¸íJíÙ]8·u%¯\x0006Ú¤\x001d£6}h\x0019¸\¸=âù¼Í}áû¦,¯¿Ð!p=ðª¬K+)\x0008hî\x001b\x000cß·\x0018ÓKÞï¤Kß½Óe¥]ÉÝæ¾Áð}\x0003E\x000fâ\x00118p(Åå{R>³qUsáÔðSÓj¸OÍÓ[/ÊÂ¯Éb	àGæ\x001d\x0013msÝÔðu²,;\x000ce9äjãùâmî\x001a¾oBsG\x0004(®Ý\x0013Zr#¶ÝÓF:·¹njøº	QV\x001d¥ÔwÖ\x000f{Zwæó6·MÝ64\x000cõ¯Á'0\x001eËq¿¯n%u¦ë¦Ç®\x001beÑ\-o\x0014ýTB\x0016ñºÉíá#¼ÍÓc\x0017\x000ey¡l7U¡Ìe\x000f°sÝ\x001d¿=ÁoÏf¸¸ù:ï!FÜ?\x00035Åâ«\x0006?\x0011È=½å\x0017g»§eogðÛã\x0019æÔb¦Éx_åÊ#¾²{RP3IuMªHµÄî÷$S\x0001åq«´ )·ç=n\x001ei\x0015^ú\x0007­Û3Qq*¹\x0003wüB¤8­¾oô>T	[?úJu\x0001Òóÿùÿ~»þôéæË~Xãø\x0005ÎÙx\x0002(=­}Y00ùUÊdÿpôæäôôìõ~\UãªQÜèÜ*Z8à
5ðá\x001dè.É«5Áû@°ºÕ£°^ñX!Ü I¶A\x001d\x001dÓa\x0007kj^3,\EC#Ó\x001a"[Å¸Ó\x0003w\x0007pmkÅËSqwbéÒ¨\x001eÜÝ19U½÷(¸Õ
²âaÍsp:=
\x0003\x000bÜ}à§Ãõ\x0011Ùú×òJç5	WH\x001a²\x001e=\x001bI¸jrÇ\x0000®l´\x001cUc\x0016×K|±ÁN|y^NÑÃ\x000baË=Akë\x001eüñæË_ï°@qV\x0002Rs\x001b .yÑ¼Ñ÷G\x001bµ§wég¯ÿ×[¬QÜÙi\x0015¶,EdqfÂM)Ü;E9\x0006eì\x0017î\x001edU#«qdLæÑë+NUÐÜ\x001bH®Ñ{¦*ô0ëYÿ[ÙÔÈf\x001cÙì
P\x001e f=9ïoÙÖÌößBÌ®Fv\x000bÄ\x000c<A\x0005ÇI()]\x0011óä~1f_3û\x0005b\x0016<NU¦½Aê¾"ß¸=©É\x001eæP3qfcx1¤\x0016÷#Nçy£v§\x001f:«\x0003
ø·\x0010´l­à\x00023¨¸±.êgÍ#íçRV£&÷\x000cMB?âÆ\x0011qc\x0003å\x0012#ø/\x0014sc\x0005å\x00023¨Uy=*\x0000qù-\x0017!ÙÉ¡¡cÐM\x000bJ\x000cùi ÀO\\x00106ÓMRcÈ~\x000b\x0014´t\­£Û,èYÃÃa`wægöqn4\ ê7ø¥ãÌ\x0003ø-Ïg5NÏ¾ûÄ\x000cÖ\x0005Z\x0003³Ù,æÀ}ÿBsú=\x001eçÝéì¹bæ\x0002Â\x000b(5\x0017:k\x001cÍOc°
Z\x001a¿gþ\\x000b\x0008\x000b. («X´º5­y\x0016^§7\x0006Ý\AXp\x0005EôøélhSöëûª¯=ß{ [\x0008\x000bnaT\x00164Ì]\x001bA½I
\x001f'yÏXÊ\x000efÕ\B5z	q\x0000½¦¡¹Q¶¨¨\x0013²r8\x0016«:©¶óê»f´ûó_ö\x000bWJC³\x001f\x001d ãuº4ïï\x0019ïýüìì|W"Cm§\x000cÕwz\x0000\x0013\x0017å\x0014¢\x0015<¢7új=y\x0008fb¾\x0017:\x001fYvëÅ\x001f¤×åÓ\x0008x{sý÷Ó»ýCW\x000f\x001aÈb`úæKkè)ÆÚéER\x0008xqvò¿\x000fNÏÞð'ß+¯³	\x000e_g;áBü{Ð\x001a!M~.\x0019`é\x0014XÉüð\x0016\\x0011â6nøt¿ðâ¥ I\x0006Qxæ~ICÍ#QvSÆv.mèì\x0000\x001dnD§©áP\x001aEÓ\x0011orNÁ£Vþ\x0018\x001doQåÍò\x000f0ovòùÍ×¯YíD\x0018z\x00054O~÷úú÷«Û¤"\x000e80'=\x0008ÇÌí\x0015Vao/¢¥©øIt'ÿq|qÊÉ«ó£ËË¬k"ñão\x0015¤©!M?¤¥aiñ_ñ ú!]öYq)¤RË!]
éú!M!]¶5\x0011ÒÞCº\x0005¢è°µ$ws}{}µP9Ç
F÷(\x0012ú\x0004^v\x0012 §R{ÂjüþÑÉÅÉc\x0003ø+>Só^>ër+òÙ|\x00110GS\x0008hÔR@_\x0003ú^À\x0010ò\x0000¯\x0008\x00086§D@­é\x0013§¡\x0006\x000c½:är	 Êå_VyI£\x0004\x0001\x0016\x0002¦#@)ºÏ )8í KFu¥uua) l\x0000e·\x0008
¦³³\x0008!\x0017Ø¢\x0008u¹%yHÛ\x0012Bh\x0008¡ÐÐ´X\x0014¡ÊÕÐç¡I(Ã{_B¨\x001bBÝ-C¹êL\x00088 aùÊB/%l4ìV5ñúªL\x0013wIÕx\x001dø+ÓØ¯%¶!´½8xÏ¡'e\x001d¯G9n©ª®\x0001tÝ"ô¹Ô\x001fE\x0018rÂ\x000e	A\x0015\x0011ú¥¶ÝêZ¼A6Û\x0013'é#Ë{{²ø¢4êZvëkAsuQ\x0010À>§zè\x0005ÐèkèÖ×"G£(ÂÜ\x001e|²Ø\x0013¹ÔeF\x0019B·2Ä\x0008¡\x0010å\x0014JÇ*,5(Ð8]Ðëu¡íÉÃ¶&÷Ö¢-ù&Å÷\x0004\x001au
½ê\x001af¿+F(ø®d(ò²P¡]zO QÐ«\x000cÁë²ÿòÑ¶P\x0000\x0010\x000cë\x001a\x0008eØè\x001aèÕ58âÄ÷«ù²\x000c·üa©\x0008UsUïE\x0006gs¥'\x0002JVÎ\x001b¶É°\x001dCõ\x00136WYõ^e$d\x001c	BQ_¼ká«\x000cb+Z\x0006¢å{ÀÿØìãÓ\x0003A¯FçÞ6ôþÙïwýÇÑ,<¨ñ \x000fO\x0005\x0013´IÑp\x001c¨Ï\x0015õxTWÏÄÓ5~rx¶Æ³xVä=ñ_Rä÷¨\x00032\x001c½ûG\x000fßL<_ãù''i\x0012 AÉù§ÍLø?ÿõßÇ?}ºþºçþÆ`\x0004<Ý_\x0007Çû+TQÒÛ>õùéÑóLypüòôäòx*c]!ê\x0006Q\x000f ìË\x0018åò(ËÈGÕQ^¹}|{¥h\x001bD;\x0018ý~AÆØQKI¤¢\x0005)
¼Ò7~R»ÜT²ÔÅÜiv»ßv\x000cg~ëMDj4õ\x0011&½pLïÍ·ë¯_¯>_}ùWæÅõÕï{ÔµS¹Ô2Ê1\x000fZhIÇ\x0011§¶§goN./_\x001d¿~÷æÅÉñ<.Ë\x0002ªjPõAM
j\x001e(Æ*m"V´ØgW_n®¿íI/Å8¯xaÓK%j¦¡0\x000f°Ï_<6ÿ÷í>ílÒôÁY®k\x0004B®[G%îÙ\x0005Û©¥\x0019t2ø\x001fÿü7øÛo_éÚlÒÿzðìÓÍÇ«h`0}­R8M×¯¯în¯â?ÍäÿcO¹\x0005\x001bb8¥Íw\x00109\x0005N¯\N\x0003ä'Çã·\x0017ÇõðäËg§g/£uÎ\o¡E\x0002½h
@eAá!¢É\x0018S\x00154»\x0002Z¼¶ª\x001b¶Ø'4i¸¦ï&GÉþúíö·?ßM~ÏÍÁÛÍ/×W·Wqá\x0000æÂ\x0014Mú>\x001a7\x0006Óy°ð\x0016ØÑÁ£óãé\x000bºµý-÷cáî(Ë_\x00120VB¬èÓ³¸ôb¨í¯8\x0003*
\x0008ó/\x0004\x0015]\x0004»^\x0010J-§\x0007ÝI¥¿ Ç¡\x0019êþ:`\x0016SÅ[cû¨@ØMKTEVÁ
\x0016\x0016í\x001e\x001fÀ\x0002õ[Ù	²½	äÍíÕç÷\x001e£²N«TnÁ\x000b2N{tòÓª3@Èö5TÇ¯Îz ¸öBÅ¯o\x0008	Ê£; Ð\x0005jê\x000bvA=PYû ¬²Xµ\x0013¡\0ØL"\x0008g¤Ë]HK¶ú~AÅ°\x0006T\x0016OÎE\x0012¡\x000b\x0018\x0005e\x0017CmôýÒ2g%¨u\x0008ei\x0012e
r1T´§¾\x000f
ç$d(¬»ÑùH\x0019¯³!4¸ãl\x0008Êýô»\x000fº|¯n¾|ûõöúËc
\x0001\x000fËjÊ\x0006}ûh\x0000
hRé"F÷\x000f^½~óîâdº#h\x000bhëâí\x00052"m\x001eÏ3fÓ\x0013,@8çr\x0011ÐÖ¥Û/!ÞT\x000483Pz¨s*P©í8ÏÖÛ/ ay\x0012Âî³x¢|lðózx¶îÚ\x001c\x001e\x0017è\x0004	l% Ã'\x0008&\½@ûð·Oö1÷éÙÍÝÇ«O^4©ÌäpNxü/±ïÆ«Ü£VL[ßggo_\x001cî¸i\x0015ÖC÷i\x001f\x00166\x0002Ù9¶D!VÐÖRr&¥\x000fë¡\x0003µ\x0017\x000b÷~\x0015¯\v6ã·Ô¬À8âX\x000f=¨}XNæô\x0004jK\x0011?bÒNÈ¼\x0016	µ¥
\x001bú°¢¼M¯´ 5ÛG,0\x0016KÒÙ
\x0015­§Î{'ÖCÏn¯´@§d[\x0014\x0016!fiyËÒvìz¨¶
Þ\x000caEÏ)G¥¸°¾¡Åfj¢\x0002\x0005K±°|\x0005ÿßM\x0014,-¬ÓÔYA`8H\x001fQ)÷ +þf²WCD\x0018\x000fÂu¤!$+.C£
û¹îþºù\x0016n\x001eñÏÏ¯¾ln?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÀóÓæ2{à¬«\x000b ?,.ÀÓ÷wo+Wks©ÿèW?Ôÿùáîí[yÒÖ´RàþF5ÜØ¼Ì¶5w¾ºyQ¼Úhu\x0019\x0000\x0001@°\x0004\x0000 £\x001e/I]X*\x0008°)äÛ\x0001øùî»\x000f\x001fßo\x0003H\x0003d\x0007¨déÌ÷\2ÔJ°¡xiL\x0008\x00107u+fv \x000c\x0000á\x000e8\x001eDZÚ\x000eTkÕ8\x0011¹ÁMv\x00006\x0007ZOìÀ2i\x0005Àóì\x0000x\x0011^\x000c\x0015\x001eÚòQtCxùøþG?|2üþ¥S+~çñ¬Àë¯Fª9!ÄMÿjbýËÀuý<pæ\x000b»\x0000~8?Þôü8Õ\x0012çq¯ÒÕ]-¨^6é`f\x0007\x0013ä-O\x00107á4ÀE±¹×>µà7\x0007*N¬Q\x000e_×ÏÊáfë\x000fÚ\x0005®\x000cà¯s»Á £â\x0002·n\x001a¬ `I\x0001\x0001]«}õõ\x0004q°´¬ß{Ä"
88\x000eß?Z~ÿIü;ì,:£È"ûj6\x001f¡'6`U[\x0001°¬Ý\x0005 &\x0014jZZáÕ6\x000c~ûÅsbýðÕº~.\x0004þÂLhKÐßá;ËK\x0012ÁÕ[\x001cåy ¥lå\x0016ã#ÜÍÐòÚ*ÊkmÕ_î~þ×O÷\x001f®¾½{ÿë§û·w\x001fO\x000b<GIÞh!IÊ°v\x0017â6\x0015ó\x001bí_nüÏ7·¯¯¾½yõôÍíï£Á\x001e
Z£)ÒT\x0017Î2 r¢þÈE»{\x0015>'¡\x001e\x000c\x0019añ²¢q\x0006èf¯\x0012à\x00044¡G\x0013ÑTh
¡ ¼Ö\x0012!iÁßU\x0018=\x0001MêÑ$c4Q'.AÈ"ÃKDkõ\x000fíVÿ\x0000¦ô`1\x0004zÐBRSLä£Ú\x0000Ü-îG\x0003£E³6i)IÂ\x0013\x0002w\x0008°Z\x0001Øm8?\x0001Î`\x0005ÀÚ\x000cä :?\x0010jØ$f\x0014µH\x000bÊnëÚ	p\x00063\x0000Öv /Ze\x000b\x001c¢yYáÈô
Çúê\x000cgt´ÈÉ\x000c\x0014\x0016©>°Ú6ÖS\x0013\x0017võNáÈ\x001ewkõ\x00168y®dªµÁ\x0006ÒO®Ò2_/yäô«'ïÞ¿½¿ÿp"\x0008:nªúrQ"EÒÙâvXT\x0012¯¯¼|õâööõq\x0010Ø@C\x0010ÙË8RàV·EQKé ÃÑB	\x0014Ô£ ;\x0014¼ôñ8·(Uä^_¢âÎ\x0004èy\x0010¾\x0007á
·Ë}=vÙñ\x0018å<\x0005­	JÉò@\x001eE0Ü
în;QW-RdX\x0008°î»\x0019ØC\x001báü¸¤å¸\x0008E6_¡ÍP¤\x001eE²CÁ\x001a¤­¢¿þ³ü\x0017±^´=Gn\x001eEîQdÃãÚ'GA\x00054|\x0011½zH´Íó(J¢\x0018îEPå>ËÁÕ¢\x0006
]+±\x001aá9ÃÍ\x0008Az¡])EU~¼¾+'·­É2b¤mCÞöäõ\x00056\x0007í!&Ô\x0019Y5TÙ\x001e­1\x000fc n0dîÀ\x001dl­ü¢T\x0012\x0017ÊSï#£Å\x0017\x0013 \x0006Þ\x0006CâöP®¥<¹DyÜ'ø\x0010XªÛ\x000eÄÀÛ`HÜ<ó8âm½S\x001eÞî\x000c·{ n0dnÏml­ÒÅ3RIý°F\x00071P7\x0018rwpYZWªÑÖ\x0010ÊYïÅñJÑ	\x0018\x0003ë!íq
·×á\x001aÌ
ëÅ
Ô\x000c\x0005\x000e||ÁÊîM¡Þ\x0015\x0004ÞÍrY]hgiq\x000c\x000c-­ç'µ´²7jÀºÂàY°f0\x00063f\x000egjÑèd&JÁ§íi\x001aó®\x0014¬eT\x0012wßÙÝñä¥ä¨þmR\x0002¯ËÏêl'®NðCºú"KJä2fWd,{³»-¥qÊ¶ü<nËÏvÛ\x0012I^|X3Qõ]kX\x001bÕ%Ù9!ðp[ÈtW8#*+Þê®(¥my\x0013Ü«\x001fÿýõïvÇ«\x0012¢Þú W> v²íHZ\x0018y¸%ÞtKêAR\x0011ê-j(\x0018¢F\x001fÆæë§ñüd^*Ûà¨H¿\x0014\x0005\x000b\x0000n4L\x001c>Ü\x0014´Ý\x001a\x0012¶\x0014Po½j\x001f¬ùÃtæ_äÍ;¼Wë\x000fú^Ý´ÎÿöÓýû§Y:  s¹YÌaÎn÷)´é?öõí«ïw4ÛuýØ¯\x001fMÖOù\x001aÚòW½.Y4ÖòNÅê	Ë§~ùdóù5st:ß+SqÕõô\x0018®ß÷ë÷6ëOòÀSZ
ßÚñ!ýþÛå'¬?ôë\x000ffÇ¿MÈ<^O¿.§\x0016}~ù±_~4Y~\x0000y,¯7Èl]Öñ\x001ee÷}yrý©_²ùü$ÓÚ3\¡^_OÒ#\x0006ª=zý¹_¶ùþ^:²3cè´yu/xæÊñ$^é×_¬¾¡=¥Ö¿¿íZÕùå/YÙ\x0003y9õWÙ\x001e*2Ð!Áa\x0008\x0015\x001e1¥ãÑ\x0000Föµ¡ßUÎ±õ¤C§½$kê¡rÇ\x0007'=zý\x0003û
ýF/]cõ¬çkùþZA#Áñùb^ÿ@¿`Ã¿õ\x00027åªzÖýuzå\x0000\x001d\x001fYóèÕ\x000fä\x000b6ì\x001bõm(³\x001bÚ#\%]ýüðÙÒ\x00060°/ØÐo\x0004~kö3é°òºnPû¹ý,4\x000f`à_°!à$Qr¬½%\x001b \x001c9ì$¾ç×?ð/Ø\x0010p=ANNPÒ0Å'H	Ìï
	M\x0002\x0018\x0008\x0018l\x00188/U\x000fÕä\x0007)5w¹81a»ÝëÕ\x000fô\x000b6üËXÛ×N\x0007fV§\x001dh¸ýä0½~\x001cø\x0017mø·8uCuÿø?Eß\x001chWÃ~\x0012ÀÀ¿hÃ¿©ìâ@T_\x0008\x0005@özÊî8£I\x0000cøkCÀ\x0005%çXO{Ñ9eÅ­\x0016hWgnrý\x0003\x0001£
\x0001óúå\x0006«L\x0003/¿è
ÞN6¹þÑK\x0012AzØÔò¹¢j9¸í\x0017y\x0000\x0003\x0005£
\x0005·JÌ\\x001b\x000fYW\x001fõð\x0018&p _4¡_®Þ×¯$\x0003M\QÑµì÷gGM\x0002\x0018ø\x0017Mø7:%\x0000®f1õ,+¬§'\x0019^ßÀÐÀ"\x0016)e­\x001b \x0005î®\x0004©Ï­\x001b°[s<\x001b\x0000÷#\x001f[\x0010<N|<=\x000e\x000e\x001aÆäõA­ÆaNÓpÞÐ\x000c­Ï\x0004]*Î
Æ\x001fCx\x0008\x0003\x001f\x000eà<Ý©Ó6þÌ5¡¤nuRRÞ¦>\x000e\x0002\õ½Æ\x001e°úÃSÿtõÝÝ{~(<MTßs*¢\x0014ëZ,Ú&\x0001\x0019i×­{sõÝÍ«'ÇWýÊÑdåÕÉJ@n\x00152Ô ®|×\x001bzìÂ©_8}A\x000b÷ýÂý\x0017´ðÐ/<|A\x000býÂ£ÅÂ\x0017Ñxy¯\x000b2u¥s×çº]Æ}ìºs¿îlòÁ«\x0010Û4¡ºr©.à¹Êòjzì¥îQ+\x000fõÏÃQá¿¶øè¥è¬³\x001aÈth\x001e)_\x001d·5»µÿ³¦êqí?þõ³ÕÿÕbù9I)×±Ze=5ÛUýùôõ TT\x0018+>ùÛÝ¿Ü×µrÌm\x000ct±.Y\x0006pøÔM ¥ã¢Tüùæ»Ûú·CÁ\x001e
ÚB)Ð|NNtâuk
\x000f\x0000Ë^T»Ã\x0011%\x0014ê¡ù®,¥OuW0HB¿+;\x0007ë$,¾Çâm±ðü ¶-<\x0000¾uï`
\x0000RÛ\x0017ðG«Êç°\x001eK0ÞØ:ø\x0005)¨­]¡^÷mÏXì±D[,e_bÁp­r.M>®²?.9\x0005%õPñ¶PSÁÍÑ{¯3·¼y³\x0015Þ&{\x0012ÜcÉÆÛ\x0012¯Û®d öðWw\x0005å\x0015´Ø|\x000eIé\x0014S$,wïÚeY´ðcB\x0011ÅyÚ~C8\x0005ËAhy¡Ig»-õ\Q\x0003B\x0006rj\x0003íu(Á)ÙWÉ^²\x0013z_ÜÊ¶;3Ð\x000b\x0018ó\x000b+Ëu\x001e\x0018²«\x0003cJ0d0¶É\x0015KRÞ×wE|ÊûGÕ¼§°\x000cv\x000c
\x0019ëµ}á\x0002hjzO>\x0014Ý\x0018Ü~>\x0005\x000c\x000e×\x001f¯hê\x0015\x000bdó+&Y	f;\x001d{\x0012ÑK¶¿üº/\x000e%ÆX@}`êÃàpùÑúòG®A_?z]IRÆN\x0019n?ZßþÖ!^± 
CUi¿¡ÒÎö\à°\x000c·\x001fo¿V@S}³\x001al\x000cy\x0005\x0013·Õ,N\x0001CÃí'ãÛOxÛ)£\x0018ä9\x0006ý2,o\x0001ã«O\x0019î?\x0019ß\x0004\x001ew³¡´qQ\Ì`{ch¸þd|ý]\É*ú§6Ä\x00079J\x0013\x000f3\x001f-²Ã2Ü~²½ý)gî]Üå\x001aþ{ñA±\x0004ã\x000b3Ü~²½ý)ùëv_°\x001e1qüEhÛ8l
\x0019ä^G\¾ÃÊ\x0011\x000f \Ô!õfkúÏy3\x0007µuñgî¬ñ,¢P9au\x0008zÍ¹\x001d·LþhùQ<M\x0003\x000eÓâô\x0007ÎaÞüÛýÛõAðéÝûs!KLR²\x001cxtªÄ4	H\x0015asJÉÍ\x000f·/Ö÷Á§7¯\x001e\x0006{4hÆ;ëÓÔyzµ)â®ÑgE!\x001aêÑÐ\x0005ö&8y\x000e\x0008õmo"×\x00004éÔR¶ò3' ñ=\x001a½©^s«
\x000eXM¤\x0002RÒª\x0010üfyð	hB&ØïMnÏ/Á\x0015Ò<s ©ÓæÛ
lN\x0012{(ñ\x0002Ç,'ézáþ/®^6Æ«B5[=;4©GìÑ¤2¡08"ØÀ\x001et½ÁÍ ó\x00044¹G/aãº7Õ%XÍ3
\x001aþÕ\x000eMéÑ\x000bì
éPO_²æÎ©¨\x00144Í§¦y0KZóÀî\x0002{Cî:·ñ\x001eè¼¨Q`¢H\ÍófÓ	pFGà\x0002\x0000W\x001c·¢-ÏÍK­y\x0005±Ä\x000cÀvóÏ	p\x0006O\x0000ì]\x0001Ê¥H-c¤Ó¤0"(yÆÍf¬\x0013à\x000c®\x0000\À\x0017ð<Õ³)x'X\6Sÿ	ãâæØ²\x0013à\x000c¾\x0000Ø;\x0003´¤Ð¨zõ\x0000$j[Eù©!\x0018\\x0001¸/À\x0002`~¡\x001a\x0008\x0004ñÓ[\x0005Îv6í\x00048;\x0000\x0017ð\x0007|\x001c¬{ã&\x0007]\x0014¡¿àò¦äÑ<\x001c\x001cÌ4^ÀLsSTkÉ÷ÃÍL×à/«]Û|H?\x0001Îpsð\x00127bÉî°¿Ì³Ð\x0000`3 >\x0001ÍpÖð\x0012gyØËÕYgýB): ÈùÍ¯Y8Ru\x0008
ø¯/à°erÖlô2ç¨Ñ\x000e=ÞûÜ\x001ez¡\x0001è\x001f÷]\x0010Ê?cÂ$\x0005¸\x0001j¬ #HbÈêèlràj\x001dtõà\x001fì£\x001aÊh'ïä\x001e%J^\x001dëh\x0015&¬tãÑûë½Oí\x0013^d£r°Û\x0000 \x0018\x0001×\x00012\x0019è2gïÒ\x001bÕòxH!ê\x000fB|ö÷¹ûð¡ÂùïÿøÏ·ÿûÝ§Ór¡Ri¡ªã\x0016eº!!\x0006-VWh+;õìÛïn^¿®(®n^üååã\x0010°\x0010\x0002	ý «\x000ev«º^et1¦ÍÑ>Ó\x0010¨@»\x0010$¦®Û×\x0001T/ê6ljLcð=\x0006ÿEnCè!\x0004Ëmp¬÷Ñ dÕtäRfÅ°YN>!õ\x0018!\x0018xî²\x000b*\x001c\x0008°Bð[8
¡ô\x0010%\x0004\x0014²¨\x0001KÑÂxt!+Í0y\x0016\x0003vÕÒ°$¯\x0018\x001cué¨«e|J\x0003\x00117æ¦A\x000cf	,í\x0012ßiÁà¸Ì´a \x0015Ãfòh\x000c)\x00039ø\x0007m9{}÷ÛÛW7ÿöÛéc û×ñ/\SÖNR=J2*\x0005öÅ|^ß<{ñýÕÍ\x000fÏvf¤èú±_?Z­éíkë\x0007¡ÝDàu|MÜ\x001d16³~ê×OVëç·p\x0019¿Y\x0000ÅKÛú3îuýÍ¬ß÷ë÷Vë 
]\x0001ä1êùÑaHWµY~è\x001f¬_¼GËç×i\x000fIGmÕÏ¿×Ø5³þØ¯?\x001d\x001f\x0010Òåúzùþë¨0.¥2Zê×Ö\x001f Èhz|41B\x001eôô'ØkY~î­>V*Í\x001få!(\x001e¬gÜSrYé×_¬>¿:²%¸(R2T/uQë¹Û9±þCùýÂ^Î
Ë<AJÍ¿\x001cÿ"â¶lý÷º\x001bgÖ?²¯\x0015ý.c1u\x0003P\x0014m~ý°«\x00038³ú{Á|ùÊf]½Êç9Íòùwf\x0000\x000cä\x000bVì\x001b«ùñ2Ðjoó\x0000Ù\x0000+ç\x0001\x0006ò\x0005+öe££öÇEn¨æ3àz­\x0000\x000cô\x000bVü\x001b=®î;è §¸\x00020¢_\x0018è\x0017¬ø7pËßâÿç	Er\x0003tìs=A1ý,Á#Ç/j@ýµkí¡¹\x0001\x001d\x0008\x0018¬\x0018|ÿ BÔTí×ïoå¿Á@À`ÅÀs½ê?\x0017\x001d¿\x0019]¢Õ62¡8001pÒ)>u\x0007¢NwõÙ+°ù\x00144\x000b` `4£àD\x001cö6\x001fÎë\x0018¢\x0008yõAwÅ\x000cg\x0000\x0011°\x0015\x000bWoS}h¾\x0003E¼\x0008\x000cÖW\x0000\x0007\x0012F3\x0012ÎN¾~Ñé\x0011W\x000f4\x000f\x0003¡\x0019µG6?7èTð¨3*\x0000«\x0010\x0000\x0007
C+
èu<3\x001f(\x0014\x001càp~Ö?0\x0018Z1Xª~?\x0013ZiS¥%\x0003º¬\x001fa{`ã$ÂÐÂ"\x0015\x0011c¬>Ó\x0014VH¸ZP+'\x0008\x0007\x000eC+\x000eKì¹\x001d\x0006|öD\x0016+µé\x000elf£'\x0001ÐÀadÅa\x0016\x0015@õâDÝ'ÄÕØl\x000e]ÿ@adEaU\x000cÅHAçdVË$6\x0008ÑÈ£ÁÈÁâ:!Þe\x001cys²\x0000lOÈ\x00040&q­(,qlûþÙk\x0014\x0010Z íþ¿ÉÕ\x000fQ$YE1¡FÁ>d
ã#èk\x0012U\x0010@\x0003\x0007\x0015\x0007'\x001eM*\x0018¹h\x00188f
Ø\x001d>\x0003`à02ã0.Í4hu¢eBlZ/\x0000ú]Eü\x0019\x0000\x0003\x0019qrXV©«PÂú\x000ccEÂ4p\x0018qX\x0013²e\x0000±ZÓÖÁGI\x000b<\x001b\x0000~à0oÆa\x0015¦²ÖLht
0úþ~ 0oEa\³*\x0007(V
\x0013\x001bA«	µâ0?p7ã05\x000fadY\x0002vêÌ\x0000\x00188Ì[q\x0018kØH.1r-Z3¢9è[\x000cÏV4\x00020¾DÑX5ýëSêÊ\x0002Õ»Ö\ÜvÐ,Æ¼\x0015åêû¸";P´2%G/<Ldåú!ôf¡dñÒ*ÄY\x001f¥±xxNÊ»3\x0000\x0006\x001eöV<ÑÉ\x0018äjÎrÎ Ù8ÝÉ\x00043\x0000\x0006\x001eöV<\x0000D¦4\x0004Ôlî2¼¹±Øî`£å\x000f,ì­X8\x0013h2[LB\x000b\x00042I\x001f r
0°p°banZÒ÷¼P¤G¢ÎØE®!5\x00020ðp0ãa_¸ Ù $íË¬
jÀ(\x0019\x0011\x0006\x001e\x000eV<ê\x0015ÖHZ\x0011\x00113®É\x00084º\x0003aàá`ÆÃkY\x001c¤Ö>ÖX \x0007Ý\x0001«\x00134Ðp°¢á\x0014Òp5\x0018Nú\x001eÀÃÖ?X°"1ÖÀ÷Â\x0001\\x0011'Ë×ªDVÑ|\x0018( XQ@váZLhð"BJi]~±:>q° ÑÊæ\x001a}i \x0010ÌVcY"5@»ÃÉfÖ?ØherõÚçç¬\x0014H\x0017ÈÊ`\\`³þáúF«ë[ªë,\x000cÆ³í\x0014@Ô@Ì¼è8VÄYÝß\x0016	>õ¢¥¤,ç\x0004«\x0017mdâp£Ù\x0005þÃ\x0000@?z\+St\x0018Çù/Ã´Ôãê»0ñ"ï¤åMV'	\x001fâh£+«q@dÿt¹\x0011T4(0K
Qy\x001dTxÝÂ\x000cÄu\x000b3dm|ÀVÅðÙ¹²±¨\x001fFI´8}ïã©­éF\x000cç£4ö2ÿbôjF"{\x0004Á£¦L×î8²-K=´þìX%ÃcåÒú\x0000\x001e\x001d?Å¶S+ðÑ\x0015«\x0012"úìX\x001dXÏUÑR´ æ*Ã¹Ú\x0014Õ®åýñ_?Ý=8Zå+ùÍ¨*\x0007Ö¶\x001aDhQÎZ\x001c¬ÂP÷É2´X!»&xÜP(\x0014\\x000bd7%¦Ë{?;Z&+Tp­r$}
p(±°º"Õd=ÀQMÝ\x0015)«o\x0018HÅ´«É"­TÈJmÓÅj\x000fq ³Ü\x000fU\x0001n\x0000	²\x001f®¨é
`´\x001føÙ~ å~°LcáËáÑ-é±2«»mG4Ü\x000e\x001ej Æ*¦¸:¼¤YKí\x0019 ÓÖê3³kfs½Ö±qK\x001dJ\x001fWÒ\x0017\gU\x0008La C\x0010©,iãæ$êhFJI],Vù?\x000c]`iªp}¦C]¡'eÀr\x000e/Ã\x000b]<ôeê\x000fÝ(À¯ï¿ºù7jna=ör\x001bXgIËGÑÇÅB~7üûæÍÕ×·Ï¯n½:¾rìWç¯\x001fàr[y½ÇIVNò[ñVNýÊÉ`å¡uñ\x0016ÏS\x0018³,\\x000eK¡ýFû~áþüó$j9,ÅIÿbE	¶PÜ53+\x000fýÊÁÊA\x001e;ëÊQ§FðºðÝÆÅÇ~áñü¼ÞÏ¬³^\(ÒrYW¾Û±;³òÔ¯<\x0019¬<m¯+OR¢PW¾Zcóè\x001e½ðÜ/<¿p\x0016ÖOÒ¦åBÖuýiÙ\x0013\x000b/ýÂÁÂe4\x0000[Ä o!<dPÏJ
\x0007lV¾ôW\x001eXÈ¿ôÊÊB¤\x0013ÊkX©¶öGÜO¬|äO\x0003\x0002]éx\x001eÒ¾`¥9Ýfå\x0003\x0001.
]má^ôø«1§Ý*À\x000fü	ç\x0013(æ,îVñ\x0014$·è\x0003½¢\x0010l\x000b\x000c\x000c
çS(r¹ÜQ\^ý Kw»éÝ¥\x000f\x0014
çs(V\x000fäòSeÜíLî®Kß\x001fy=±ôDá|\x0016E\,K\x0007ÇÖ}YºÜÑúßgô&kÖ©¦è\x000f«w~õûÿÇÞþZ\x0017s¾À^ö\x0013nÇt4®£õöîÚÉÛ«çW·Oë_îÉ¶u\x0002$+\x0014º\x0004\x0014­\x0000äB\x0016iÆE
ä§3Èá9hµé\x000fº)_³\x001eÏô9ò)]Óbì3ð¶\x001b¼\x0014Kä´|þ\x0015x/\x0017ûåâYËs\x0003ËrKâ\x000eÇíz²^Ú-µäz©_/·Þ(ú(y@£ë\x0015ñïºÞMáÒõú~½þ¬õ(!hÎ¥\x001bÏ%"ÖzFv»ñ\x001e¹ÞÐ¯7÷}´NåìPÚ\x001d\x000f]õúMqõõÆ~½ñ¬õú$¢É+Å°íµQ¡\x001eÝ\x0018âëMýzÓyç!/y`jõ¤³rÚïÏäzs¿Þ|Öz\x0011E>çj\x001f\x0016cV\x001c>Ô{ÄøÈõ~½å¼ó@×²\\x000fò P\x0003éqHåüÏÛ6n
mN\/Ïglö¡ÀjÏ¢Ð¬ß×ï>=rÁ#½Ço\x0004×bÏª)&ÉLe	}«ÑØõð\x001e¹Þßà<s¾Í«\x001fô©ËÅ°~à¸[~ùÈ\x0005\x000f\x0004\x0007ç1\x001c\x0008æºû\x001c	´\x001b'Õ6Õld#<0\x001cEqÄp2j¬¥9è2r2 d\x0018(\x000eÎã¸jxåÊ¹ \x001aYõÊI|Ur<ß¤Á@qp\x0016Çq\x001a[8¹DhT.Dáõì\x0016°>r½\x0003ÅÁy\x001c×Æõ² `_ô\x0003íù³_ðÀqp\x0016É-S2Û;A5î×EN°&\x000bªá°°\x0011\x0003ÉÁY,W##ÉnÔµ%H¨_XT~Ø4½^\x001cH\x0003Ï"
ª1©ËzåI åõüoÐp°Àx\x0005¦ä¥ª s\x0004Jr\x001c@*ö«ÕØ\x001e\x0008ùø\x0005\x000f\x0006
Ï2hÄ»òy\x0017\x001dgL#Áuç/x°\x0010x PDß ^¸2B¶z¨w\x001fµ`ÂÁ\x0004\x0013\x0017g8×d*Ç¹kq"¼2\Ìç\x0007q \x0019=kèóó©\x00079°øE;\x0017\x0014û'­z,vKï\x001f\x001bËýøïc4÷ïg¹ï:\x001d¢ú>Q\x001fáÒzSÞí8Ü^òò¦1¬Ù\x001eý³=ß½÷÷û·w¿,	Ä×~ùêTí5Ð®>."ÅÐí¿:q[×ð»W/¿½}qóÍJ|ýæã\x0018°Çf\x0018býêÍû\x0004®kn[¸â¶y\x000cÔc 3\x000cc@­5\ä8\x0011@OuÅó\x0018|ÁÛíCÒáàëh×Ø*Áã\x000cRè!\x0004»mH«\x0013·?\x0017©Ü	tPÒÚ2?ó\x0018b!ÚmCu\"­B0Òü\x0013e.ü"\x0004³åÊÎcÈ=l·\x000fÕ\x0007bONN¢z,Zf\x000fä·lê4ªîbZ\x001d¸t?·;­\x001eouÔ´\x0015\x001d¢Ýa\x001fì\x0008qÛ°e' h3.­;a\x0007b \x0008°c²¶¤³Ü®JÃ\x001cÚ\x0004¶\x0015:çA\x000cÖ\x0015ìÌkÊa=NèVx\x0010ÇØ\x00071Ø&°3NÙÅu'HÝ;J%®ú\x0012O}ó \x0006ã\x0004vÖ)³Êº5%U,Ïp7Ìî\x0004\x000eÖ	
­S¡k:Ô¡£×"Õu'6\x0003y\x0010£çgx±\x00194ªûU5¯Xû6/çA\x000c\x0017\x001b
/vµ«^Å\x0017©³Nk·ýfÉÊ<2(vDòR\x0001R\x0003Às
[·\x000c	\x0008,=§¾z»yOüÕ~°
¸ø±±è©ÈI÷v¨p3yy
®»Aá\x001f¾@ö\x001e\x001b\x0016[j\x0008å\x000f=`ø\x0010
ZB\x0014µkÑ7ÕÉ&)FËå³×Ö¨ÑïX$Rèêê¿}÷é÷ßÞ^ýãÿ¾úáþíÇé\x0007wg\x0014}\x00104\x0003ês\x000f\x001d+þöåçÏ^\Ý\ýpûb§;@Q`\x0002íP\x0014n[j(
æ\x0008+²óA=\x000c2\x0011È<_\x0013\x001b¨0¢>]ìªÖÍ£ð=
obÍ¢\x0015Ò\x0019·d)å\x0001æX­ì$ÐÃ\x0008v0¢RèõYK¨ôá`s öi0R\x000f#ÙÁHR\x000bî$¡7¼¸]=ôy\x0018¥Q,a´\x0011Å¹EÒH`è«\x0008\x001e«í\x0001£¹µ³·<mQÞ\x001eã\x000fÁ!\x0015o%î\x000eÇ1X*04UQ'\Zb¨C\x000b\x001b¸ ÄöXõï\x0013íhéóÍéj·8\x0008ZõPwEÑl'©N<]\x000fÑtýÕF¦K.Ë*»Æp\x0004MÚ/]}\x000cÅª®Üø¢Áj>ÝU¹{ÿóßî~¿úÓ»ÿv¢	5,dù)\x0011Buið»¯ùåæÕí?ß<¿úÓË'>\x0005{,h%k'XH+\x00137W°ì\x0016»ÎC¡\x001e
ÙB\x0001·¶¾³ÂS«.EG]¡?zaæ°ø\x001e·Årx8\x0018eÔ8¹\x0018´Ç7íNÇ\x0012z,Á\x0014\x000b´fQrG@,\x0007ÁEÚ­ÖÇ\x0012{,Ñø\x000e£äÁdbê\x0019+a½ú¶÷%õXý¾¬ÛÒ"^ÞU}3Íx\x001aÜCÉÆPôY¿^}NP±\x0004Ý\x0016ÔÃRz,Å\x0016\x000bQ\x00173òjÆüz[6OrxZÒ\x0019cA\x0019ýÅGÌËmñ«Ð$íÎmÇ2¾-ëwÒ\x000eµPiÞ>²o¦yÔÝ	\x0006ó`\x0006Ö\x0007[Ú\x0007Î\x0011É\x0019s\x0012\x000eWW`½/ûó0æ±\x000c´\x000f¶¼ï*Ù\x001d«¨JnX(kmÃ¾æ<öÁ÷ÁÑ:h_×±	ë\x0003Ø\x00073p%Ø%-å áCÒ¬FkÕIØ\x00193\x000ff K°eKW¯\x0014/ÆEÉaë\x0004¸;\x0002j\x001eÌ@`ËÕ¯a8{#)K¨§\x000cö[,¦±àÀ1hÊ1TJ^O\x0019K\x0013	\x0018WV0Îtcp \x00194%\x0019â8\x0019\x0011B\x0014ôù¤\x001aEÕúú8¦$C%g½2Ü¤Øâd%¬ÏC»m\x0010ó`\x0006Ë¦JõÅ¢Ü\x0019\x0016Ým9f\x001d`\x0004uoLÁ\x000c\x0019M-3\x0015\x001e¢ ;Ãó\x001b\x0016§Ù£ù×9,-CS[Fu
\x0004Óþ+~}\x0001}¹K¦¾?\x000e¼rÒú<ÅþpLeãÛ

ë¨ ý\x0019\x0005óñ\x000c<Ä\x0004Æê1Ë«\x001cK
·Ò\x001c\x0007ë\x00046_lÝ4ü\x000c\x0012oÓ\x001f{àó]2ß&\x0000·: >È¤KÌq\x001dÕévu\x0017O\x0008??ÃäÌ1|½X¤rõ+¼¡¶FEI1ß\x00178z2\x0014«Ò[X={kQú1¡¨Ù ç³m²6z~y{$Î:å\x0019«õV£Ñ6OX\x001eb*ö'/°T]Ë\x0019\x0014u\x001aêÞiv\x001dwú\x001f\x0005©õä<\x0016dÔ\x001f:)'ÿø¯÷ÿøxÍ'%Ê´¨¥«NtRk«pØ½9·WOn_Ý¾>¾nì×g¯; Ö¼åâ\x001a¥å±	¶'Ñn¿Úã×Mýºéüïé:Ê÷\x000e:Ë¥ /K\x0015(LÖíûuûó¿wôµ\x001fGj´s×vÑ¥xÇbÝ¡_w8ÿ{ó([ík,×)¶\x0007j+ì3ø£×\x001dûuÇó¿·\x000bâLÕ{\x0019®eÙ9ë1µÚsËNý²ÓùÛ;iC*\x0007R'éeÓ7`\x001b[ûEg\x0013\x001b¨ßÚk\x0014Ë6P?vÚ/G{ôºK¿îrþº¡Hô]\x001cg{U5A[\x001d?¢zõ¸ewÒ\x001fL9ÎÀ\x0006ÆµÃ ùÞQ«jXÕÆdá#W\x001a%\x000fö\x000fî*­Ä¸\x0016lD£/>%Ï>y©câ2\x000cíîN~eùM¬ \x000cl	çÓ%¥$tY\N«\x0014\x000fH¶¬,\x0016Ìbá\x0003]Âù|éCÒÞé\x0012dh¥\x001dÕÛ(°/füèu\x000ft	çó%E`Á.þàPý*	Eà¥þëLx\x001e\x0006¾ó	\x0007¥4Öåëã\x001d{·6_|`L82\x0017yÚ&Ä\x0001¤£[:WGûiG/|`M0 M\x0012úÔ5\x0006é's1Ë`\x0010æ\x001fu\x000f¬	çÓ&\x0001ÊlD\x001eu ªônÕëtLÖ\x0003m¢\x0001mVö	R^ç¹Þ¦\x000f­õuÎäãÀx>k\x0012\x000fÐleÀå\x000ebR@&dTÃ¾;céñ\x000b\x001fCÌóY\x0000D)6Í\x001aªER²?"úèe\x000fçs&Öe\x0017ùÞE§\x001fº\x001aPÈç.q7[þèu\x000fçS&e·º³üåE¹\x0003Q/¦ÛW£ôÂ\x0007ÎÄó9\x0013kLß¾7:\x001dyî|Ñu\x0003\x001cS}äº\x0007ÊÄó)% ZÙ\x001e¯QÚX\x0002JÑë²Yø@x>ebõas³à^V>ë\x0007G\x0015\x000eç3æ"¡/7H´}+Õgýà<_Äbá\x0003eâùÑ«öuaU1×G)_ÀÛp\x001a8ÎçL"Pà\x0017j\x0015ç\x000eQGsT&5!{\x001aHÎ'MV\x0015oZ(\x0005«\x0012E;¨\x000c=Ä]ÍÔÇ/| M:4YÉ=5¤ÌC	ÛÝà¾\x001e|\x001b?ÆÄ¬\x0001mRQ?\x001c+mºf
=àÕ2=ØbÝ\x0003mÒù´¡h\x0012Æ5Ãé£ò=Äý\x001a¬G/| M2 Mð:Ã<©îçô^Ó§ý
øG/|àM:7«'./¨\x0017µùzR¤)ºz]»úÖ_øÀ?t>ÿTW\\x0007D\x0010¦uÊ\x0002~q°I\x0003ùÁûóÍx=+ë\x0017\x000f Í\x0012Î¼²\x0015\x00164Yø`
½5"Õ^RÔ\x0018Â;uUp¬ÅãyóÇ_\x001e0ç/\x0016arh	\x0015à\x0011 AÃdÒ°Í&¾¯kÿø`í\x001fÏ÷È£@\x0008\x0015¹K®ãg\x0000v\x0015¼gÖþÓµÿt~ø\x0016äE¶\x0013°:zÔÁ\x0019¹Z~^l\´>ç¸ ,?¯Ñgu\ôÓ§])ç	:úñî\x0001!Ý[ãjfØw\x0011\x0017ÀÉ8´c­r\x0013§æîÁ©9{éÄï³E,û0Ûmõ·M6YD¢Ï
\x001c\x001bRýÙÊ©¤	s)®jbá]|¸þh±üÀñsçZÐ$î*KÅê\x0003'\x001bú¥x%§ø£è\x000f]ùÇ\x000fwþõÓ»e]'i£\x0000­rymÑ¢â@KßwçÖÕÿpóæ¾yùì\x0011\x0000°\x0007V\x0000XFdj°Í$
\x0018µXêXN÷ñ\x0000¨\x0007@f;@Q\x0007¸ûR®cÓ\x000cò:ã\x0005áÈx½\x0019\x0004¾Gàí\x0010k=BE¼ù
\x0000VÑ£ý"ý\x0019\x0000±\x0007\x0010Í\x0000\x0004§õ«<ó5Ë¼ö°\x000e\x0008ß\x001fû1 ÷\x0008²\x0019\x001aF\x00059CQ\x000bp½Çõ\x000cÙÝQ«i±E\x0019ýÌÑC\x001chgªª -'¢Úªq¢âØo(ÃÑ+-8t\x001cµ\x0001¼¨6\x001cNíâ*8U\x0015l\x001c\x0007R_kdô\x0007­yñîãûûÿñÍÝß\x001f%®ýÏ
OYe±\x001d(ÖÖA°VÝUÓ´Û
ùâå÷¯*ow¤Á£0\x0013tÖ¡ï~ûýÝûßNð+PêÏsJÿØü
)lfå#­\x000fß={þòÕ³ãëÆ~Ýxöº©p¾h;ÏÏK¹ i¥Lòû'æñëöýºýÙëF}Ï,
é¤Ì\x0011Ü:\x001aÎjÝ¡_w8wÝ¾õTöuâ&-sä\x0008ÌfÝ±_w<û{»"5\x00049eÇÚ>í|^ÃcJp]wê×ÎþÞ\x0019E#»\x001eeÇÚJ­W\x001aßr´º¹_v>ÿ(±V\x0008ÜíÖÓc\x0002Îè`\x001ff5ÒUÞlU\x0016OgçDrÖetë ¾cm\x001e;Ë_HÇ\x0011aÖò@R?û»O\x001f\x0017&ýúÝý§÷'òh,ZÃ)µú¡9»¶øÈuOåC²\x001d$¾|óýB¤_¿¼}ójF\x0015\x0000ö\x0000Ð\x000c@u\x0004¬?IÁiurZ\x000eu#hód\x0016\x0000õ\x0000È\x000e@nöº\x0013mû ë\x0016äm\x001f\x0016ï\x0011x»3­ñ!³\x0014ÅbÏ\x0003µ\x0005AÜNôÌ"\x0008=`@BÝÌãã%ËV\x0011ä,\x0008Û4³\x0008b Ú!(-½Ì¼
¬òÅ£" íJY\x0004©G¬\x0010Ô/Ïuî\x000b\x0002HòØY\x0008§§\x0008¶û\x000bf\x0011ä\x001eA6CP
èò²ën¨(HEÐt »²=ì|\x0016Aé\x0011\x00143\x0004èI\x0005¸>5n/^\x0000¤í\x0011a\x0000\x000e
@í½ß\x000eAfe\x0005BHR\x0016â¨§W\x0008a»ác\x0016ÂÈÈviÉ©\x001e\x001bT\x0012y~¤X\x0010Ô\x0018 Xñ\x0001\x000c\x000cfÐ·\x0008u\x0013ðàT$õ*Üö+ú,Á\x0003\x000f_Ü\x0018]¶
_v\x0013Ò^°8\x000ba e0cåÄr+¹£¬­Õ\x001aµÜ!ð«\x0019ÓÀÔR{vY $z\I-
¼=!t\x0016ÁÀ\x0008`F	uÕH.3H/®U©ñeÞVíEE3Ê\x001aª¹]ÀNF³¨)´¾¿z\x0015h»ýbÚ¢ö©O±ªKö\x0005\x0018Ö%¬¬ârË°
Á~ÿ·ßîßòøµ­8:T
Ûà4®\x000f1ì½ã}ÿçg·Y1ö+Æ³VÌÕõNW\x001c5&\x000ekÆªnÄÞÃïcWLýé¼oÃµ,§tI@ÖÑ¨!ïæN\x001e»`ß/Øy(@J\x001aëÓZïU$ý]W¼«\x0006üØ\x0015~Åá¼\x0015§uölôa­eL::î\x0004ê\x0013+ýãy+öë8×äöó{¯º÷1îF?vÅ©_q:oÅ,\x0008¯©â¤¥Å"­É¨½\ÚcWû\x0015çóVL "uqQ\x001bq<h\x0017h,»\x001aª]qéW\ÎZ1\x0014/\x000599Ó¾UÒ\x0005§°ûlóÈ\x0005ÃÈ\x001fç\x0011ÈÒáÔlEö¨òäÓ:ÌÕ?`°Æp9@ÒLÁS©õé@û2î*$<Ú\x001e\x001fjE¾;Ï$/v¸dÔ\x000eàh5ÉdqùBÅnfY³Ø'ßÁv8\x0012K±KY"hÇ~Ì»Bf;«\x0016\x001fî0³GPèæýo\x001f>þÆNÝûßîÞ:x¨ \x0012yn-#î3[\x0000\x0000\x000f±Û\x0001póêÙëï±g÷êÙÍ1J\x0004{$hD«æ+\x0012Ù=\x0015\x0014lñ,Ä½\x00034z$d$\x0016\x0015¯>&#«U#A²«?
Ä÷@¼)DB¨\x0015\x0008ÉãT\x0005²nß5DÓHB$"É^e1]\\x001a\x0017$Z\x000b\x0005Õ\x000fÛóÉ§Ä\x001eI´Euâ\x00027\x001d7\x0019é$êá
»½ÓHR$"a\x0011Y9]IkXXLOWÜ\x001ds5$÷H²!à¸\x001aätyÑØ©H\x0002q¦«ô@)\x0010nÄ-É:;Þ;\x001dÙ\x0005)í6üÎ"é³àî+Õ±±¢
\x0007õty}pIÊ¯+]Y¯i(#Å[r|p	t(àz¼Àgwï¦\x000c\x0014\x000f\x001c\x001fX¢\x0008Çg¸ÝszSÒî(i(\x0003Ç%É\x0007VÀGÙ\x0014®7iHtL-äýÒÔi$\x0003É%Ës*Mõ¯\x001dën5;\OrãæÔà\x000c$\x000f,\x001fÐeï=©ß$ñ<\x0011ùÊq·
p\x001aÊÀò`Ió\x0004£#8­\x001c®w\x001e\x001c©_\x000f\x0003Í%Ïz\x0017¤\x0011¼D6ÕcÉzUân5
eày°%z6Z DÒÈCô^-ñn\x0016o\x001aÊÀô`Jõð]ÁêÑêeD\x000cÔ°Ñ­Ô\x0010ïðLã\x0018x\x001eMy\x001eÃ2ë¡ðÌ«Ü\\x0016*N/JÙ2p
r
pMT· êXHn=Ñ]	¦.1\x000e\x0018M-1Vóëèk$\x0017EÃ\x001cvÇCLC\x0019Ì\x0017/Ä\x0003\x0014¾ó
IH«!6
¸h¸òdzåEd[ÿ\x0003ïOM)YÏW6²^åa\x0002¯¸^ãùowÿ»_ßÞ\x0018\x0002£÷2 \x0013Yi®\x0005)ä¼éãa\x0017G\x0014ÿ|óíw7O_üó>\x0001\x0003ö\x0018Ð\x000eC"n[0¸Ê­ÍÌeQ¢ÁÄ2`V\x0018¨Ç@\x0018P&ÑWZ,òF@K?ý!\x001eb;Á÷\x0018ü¹\x000f¡Ç\x0010ì0¼Þ\x0007pRÎ\-môá¨øã1Ä\x001eCü2÷!õ\x0018\x001dÊÙ9¶ûP~\x0005CÒ}ûÑÇ\x001cÒc(¦ûÐ\x0012@ÈBµ:ü$Ë»_½Óû\x0013g0ÀÈ\x000f\x0004QÃ@ÐÈ¢\x000fÃ\x001bu#öç¸>
\x0004Æ\x0007$q%¹§÷ïÞÿzÿáêÕýÛ»O¿¼ûx*\x000eÔò
ÃT&9§ÅXv³ÖOo_¾zzûúêÕí7ß¼Ü\x0019E­X°Ç¦XF\x000bIbÕËÑFëæ¥Ù­EæÅ\x0016
õPÈv[¨Èh]Ö \x00147êÿ#gcÞmßÇâ{,Þv[\x0002ò(íöXu¾fÑ²+Ha·qm\x001eKè±\x0004Û}©XÚ\x000b¢ã\x0014Òní¼&¯cÜµ¿óXb%~Ùûz,Év_bü+õê\x0014áH¿a/é;\x000f%÷Pò½-¥ÇRl·¥RJmÁ ²©êµ\x0008¢Úæ½hp\x001aËáÝjaJ÷Eo\x000c´oÌû%ö«\x0008d\x0007\x0001ÿ?m;»úvó`\x0006Þ\x0007[âÇ\x0000×É70\Ã)ÎLÖfUGSâøÁùëí:¾êE©ù%¢\x001b\x0003»/½ó`\x0006æ\x0007[êg³\x000cBxð#E½ÿ¦f\x0019\x0006æ\x0007[ê'\x0004\x0019ÉÈ­\x0007ËÆ6×ån\x0012x\x001eÌ@ý`ËýÛÚõ'\x0013\\x001e*\x0018Ú­È\x00073p?Ø?Q\x0014ùÅ\x001aÌ'\x0019iX\x0001ÈP"\x0008yWQl\x001eÌÀþ`Kÿ¸NXª÷?´{5Ì¨?ì\x0016DÍ\x0019è\x001flùk]ü,ªtURÀ´[F=
\x0006\x0007þG[þ¯ Õ¿Õ\x0000hÑ\x001dJÂÖ¥)câ@ÿhKÿ<»Æ\x000b\x0016Òõ@nLÜ\x001d9\x000ff\x000cûméªk\x0002&\x0015Æý¡ì\x000e>Ç2Ð?ÚÒüå}Îå¤8<VMÀìVkÏ\x0019è\x001fméj(Ä\x0005º\x0016W&ºõöGSS\x0003c¢-c\x0012«Ì)ã\x0008SÀ$y\x0011ª7f÷µq\x001eÌ@2hK2<+Lo\x000c\x001cN\x00198=eTLã2\x001aì2\x0019Ûå\x0002+K%b\x0019!j
3pÖÌ\x0012Ì`ËÈØåÄSÛÛÎ\x0004	2	ýk\x0014jÃ?þuÌ0ýÕ6dÒ{RCfä\x0018­ÌÊÿÉ[G}£®DÚbÕ\x0016GW"rò|qaMÍ¦Ý¾×S¶è§q~2Ý¢\x0018×¤9kIj`Ñ¤\x0006Ù^æ×\x0011Í¯¶\x0007Î_KÅ$\x000f_)rÞPkwôrNB\x0003ãõ\x0001Ûë,{²¶yÈË\x000c®WÇ8Ó¼èâw\x001bóíÆ\x00142[\x0013Qê¯\x001d+»«§À¹\x001báÜ}É·\x0006Æ[\x0003¶·æ\x000f=g03°5g(ò¥NZ\x001aõ! Ø¦Ïê9ûy<g?Û3é`Í÷$§Öv5ë¹\x001fwæþK=dàz_y\x000bP_3? Ko+!«Ò¯Ã Ú´ÛB@ðÐ·©¬fìÛð\x000c°Væ³¸ÒHIó«+m\x001a\x0017ÔÛs?Þ\x001eÓ#\x0007u_¤*ÜqÌÅ\x001dPoÀï{:åÔ=ô>¹÷´>t¦Î¾yMÜæócj¿´twú+úC'vü§»O?½ûôþ×IÁi\x0016z8üü¡þÏ\x000fwoß6ái~^[*jB=fjí²v´ß§þÍ«?Ý¼ùúåWOP\x000fø|Ï_\x0012\x001fioÅ·ô-ø¤ÜBÚ\x001föv"¼ØÃW÷Ì7tE-\x0014S+ºmM¬3àå\x001e^¾$<W®}\x0010|´Ê¢'ñ+*>8"c|
¾å={Å§ïÙ\x0000HÜ\x001b\x000féç\x0006àkÁ'\x000fõ!Å}ýý\x0013á
Æ\x0005.h]¨ø(
G
4ã¢í³ÿ\x0003\x00177Ø\x0016¸ q!.ziO`Áç,ïyXÿRñívuLà[¨
\x001eÖ%B«K|ò·û¿ÿöË+¿»zòþÝoÿ~\x001aËÈÏM#Ï¥\x000f**ø¹çÉo¿}ö\x000b,ß\=yõòÙÿu\x001c\x0007ö8ðËÃQÝq?ÇµNôîÃÇwo¯¿ûôo÷§:\x001d¥ö\x001fÅ3Ï\x0011.teßÓ½yýýË\x0017WÏ_¾ùávÇR\x0010Ø@C\x0010!JxÌÑÞUC¡ÃÜ£Ý´Ý\x001c\x0008êA!D×¡ú\x0010Rµ\x0013å<U\x0010»½Í\x0018|Á[nDY\x0007P\x0005É	×Hº\x0011û¢v B\x000f"\x0018¨7[Æî\x0000\x001e\x0003E\7bGx\x001eDìADK\x0010g°/(\à§º\x0005\x0005i%þy:\x0001EêQ$C\x0014\x00055\x0017GEëò(zÝ¸Ûú;	"÷ ²íy^ï\x0013%\x000f\x000eÔ~\x000bà$Ò£(v(BöJ\x0014t/"¦\x00085\x001c°;PbÏî%ß\x0015äù\x0011.u:Ä)í\x0017\x0014ÍÁ\x0018YÛ¶ëJr1XiôLÀð¸ÿ1ð6X\x0012wô×Ø\x000e(&­*`5°¶c=\x0018\x001b,©;hÅ-ð`f)\x001f
\x0005t7p·ýl\x0012ÆÀ{`I|DêF\x0011ául\x0011"H\x0007c\x0001`;úî3jÂ×É
I*\x0008Ç\x0004Ø^¥*\x0001Æ\x0003\x0001\x001aÒxz\x0008&Ù)^³5×¢è½»)Y\x000f÷!\x0018²\x0005ó\x0007:º¥,h¸¾\x0015ìKÊ! Eé»m¶lº°_78åÁ¶\x0014ã3õ\x0019r\x0011ùjWfÜ½z\x001cLKC~A8zq÷ñ·woï~?7¥·TÚJÂ¹¬CLAî~ue¨ø¿¸ùþÙË\x00177Ï÷\x0012Aá`X 5\x0010òÇ(3H«ïÈ!HÒöøùY$Ô#!ó-áXJ²¬Á¯m\>Ë\x001b\x0000Oz±Bâ{$Þþp-¢µË@¼Âç(>KÈqfÐ\x0004Ðã\x0008Ö8 «\x0006YàA*ÀàtGÒ±i\x001d\x0013Hb$ïH\\x001f(
>6\x000eÄ«×}\x001dg¤\x001eH2ß\x0012nªIòTdú\x0008²º³>\x001d\x00013$÷H²ùø #-C`-²¶'® `Ún\x000fERz$Å|O|iËóWÓ¨\x0004#²J!í4:L"éÞô8Ún
\x000fIMI ¢Ü³%/yy'N2\x0012¼9Ã×@ëZßìt!\x0016Oº)q»út\x0016ÉÀð`Nñä¦\x000c\x0014\x000fæ\x001c\x000fPÚLÃÂZ°L.­ªI­W
ì­\x000c\x0014\x000fö\x001cï°Ítco¥rcÛ\x0013Z9\x001e¶kµg\x000c$\x000fö,_¯ì	G.B)®d}?Üî2°<Ó<ä¥ú m
¨î~ý¤.¤\x0019æÁç]B\x0019\x000cÎY\x0017q1õQ\x0017Í×@ó`Îó\x0010T]¸:x¤\6I³yõX¶Õ£f¡\x000c<\x000fæDÏ"õE\x001eÚëñ\x0012ç+{uYÒN{ö$\x0014\x001c\x001eÍ\x001e<´YìGzÑÂ\x0012@KvòvßÜ,èÑè¹vLw¥¢òþaíÛ®[2ÆòæL\x000fDÒ2Ãb2m£:-N\x000fØN!Õ,éÑé÷j=¡ôec\x0006eX¶\x0005¬g¡\x000c\x0004æ\x0004YY]\x001aæ8Iq\x001däÚ;Ñ\x0017\x000eq§Å|\x0016Ê@hO\x0010¯I\x0008Ò\x0015~ÿmE±I+ÙvTg¡\x000c\x000cö\x000c	^´¸Ù\x0004¨+R²+;\x0003]f¡\x000c\x0014ö\x0014éHtSë® äðª\x0007¦é\x0014·\x0005¿&¡ÐÀ+dÎ+<Õ!Ê]I«\x0005ËÑ©ß²Ý¶0d \x0015²¦\x0015*\x0019äÉ.PvüÇå|\x0011©\x0001\x000bÛcvf¡\x000c´Bæ´²ø-b£W\x0017¬ú-´:VWÆ\x001c±5­,ª¤¤ó¨0É¼Ôº+ÞÌ\x0005£!$ó\x0008²þ[[»ââLfñðq5Å°ý2d H²&È?ôª\x000c¬BÖ¬B\x0005\x00173IÎs¯/C©á¼°JÈfÁ0
¬Bæ¬Ân\x000b_L:Ý\x0016e\x0015g\x0016
Ó\x0010xuàµìJÓXv%é¦øuS¬Î\x001føÑÛó#:=Ü|I)T}I«¸Ë\x000f\x0004éÍ	2ó`¶)X÷G<ü@ \x0006,ìL\x001d2\x0010¤·'Èê\x000bË#*Wtb\x0010_\x0012Ômw(Î"\x0019øÑóct-{\x0012ÓzË&XíîÉøjMT_{\x001aâydu\x0005qîÍl\x001fÈÑcvú\x000e±4¶\x000bï¦$ëÝ±
\x001eýÀÞ\x001bSq×m,k@\x000côI	%À¶øÅ,\x001b½57\x0012ÏkB(E\x0007´bÒr©°3fg\x0016É@Þ\x001ay@nS&\x000cPc/±ÂÞ(1WíX¹aàÆ`ÍÄ=­M\x001b\x0019_}¯j¾4Ï\x0012ÌìÂÀÁ\x001bc½*m\x000e]µ½Z\Õ!\x00167Òãv÷ñ,\x001b57Ö\x000b\x001bY9J^·\x0013éËº+f¦8\x000cä\x0018ÌÉOÚ Íàv#\x0016ÑígS`\x0015<\x001f=?Rh%\x0015\x0015)=ÆzUÈ¬V*5Fæü\x0018=éUq)Ki4âÊ*ÕÏ4»*Cv5XgW©T^²«\x0014
Ã\x0018¼z-f\x000eq\x0018¨>ØSý\x001fÈ*\x0003Õ\x0007{ª¯¾}äÄÒÒ6n
Ô´\x0012\x0007æ\x0004¹È[LqÝ ¹ô\x00104J±{~\x0003©DsRÉqÑP]pÀ%iä5ÍRÌJZâ`£¹%ÎÕ~\x0005ñËúÐ\x0015¼¯\x0005\x0011±HÒÜ~e\\x001fº046ÖèQTÂN÷,áÖGó[\x001dJßÐ2ÀQÄ\x0007}Ñªjâ¬|É4Üúd~ëS&~sl\x0011$¨/écÐ°\x000bÍ\x001c°4\ûd~íSD-F$&´Â=\
ÛV\x001e2\ûd~íGQKª÷Ãñl±ÆzW|&«74\ûd~í\x0013fUÿà\x0001^"R½ÕÅ]i¸öÉüÚÇU@=÷2\x0005Ôô<¨Ù\x0006H\x001e.}¶¿ô.i®\x000b¨\x0004Vy{»\x0007<\ùl~å£¯îW+©8	fhÌïøVL+Í¯|ôI&,ácS®P@£Çb éJëá¥-Í\x0016\x0010¿ ¶3Và!ðbÍêA\x001bÓV8 i_jy^\x000f\x0011UoÌ\x001cQuÈ¢v\x0016`
*\x001bV/¿z1ÁìÈùô\x0010O\x0017@ÄÎÐ&Bag@\x0019õÝöL×Ù®\x000føìÔ]àÐÕ½Á\x0010ÕÓw!µIKÑ¬vÇvü\x0005®\x0011%5wY(f!0HeÑíÙíÓ	E¨·OÉÜYÿ 3.\x0003«ø·ñP\x0018½zÏ\x0011·Gª<\x001aMzØ²ºÕ_î¯ÖW/\x0012äi¯\x001aë\x0008Ræºìí\x0019\x0004\x000bon¯Ú_\x001eÅ=\x000e4Ç~[UÓsZ"¦e	\\x0019nz\x001cd£î\x0017MG6ÎRÀ\x0003´Þü#'ëñ@|\x000fÄÛoÈzá+Í¬åaAk\x0012ªû¿Ï2\x0007\x0012z Á\x001c\x0008Fç×Gã¢ù×\x001cÄd\x0007z éË½ê¹Ç/CÚn«ovÀ¡=RG<ÌGÃÁb½ÉòQ£±úñ9iµzÚ·30m\x0012ÈpÓÁþª³T$¬ÐZ¯Z\x0001V÷¼ëóJ}ÝE\x0007>MËEÇeîs»è ¦7mÏ\x0016D2\\x0010°¿!°è87ù²¾yçµ\x000b:ý¼G#é:RßQd$;gÒ[\x0019¿ã*q\x001c³\x0011\x0012\x001f¼ø(\x00077ø\x000bÄ\x0003\x000fñÀ%ð\S\x0016Å\x0019*\x000fa©8U"ýåÓÕóWOÞýþîíýïW¹¿{{õôÓÿ9U	=\x0000oÌ°Â"ó8=ªx\x0000púu_óöù÷WO^>ùâöùÕ_no^\=}ó¿öTÞ\x0015\x001böØð2ØR7\x0005ªHÐï1F&ð;àE°Q.
]Ý7\x0019¤æ·±\x0011ä¤3\x0006èVñØ|Í_èL´ìÖ}\x0003\x0016ÝÎdÐ!q\x0004{ZO§c\x000b=¶p¡}+¢&è*Ë6ý\Oä\x0014\x001a\hÛb\x000f-^\x0008\x001aèuK9I\x001fY=EÆ\x0004·;\x000eïtl©Ç.fJÖ¹$#Ø«)É:Ò#Àeö-÷ØòÅd#²å3©ÿÜ¢âÉÐ\x000eÂ£\x000b»¹Ë`ÃÐ¤Ã+6nØj¦\x000e/ñy»üæ,p\x0003½Áeø
q?"]£`ó
íØ(\x0013¡
\x000c\x0000¡\x0000(	\x0008xæiÛ7¯|2fn\x000c\x000f<.\x000c½Çõô\x001fÿõö\x001fÿõþî÷«ç÷?ÿ~ÿþçÓ`ùR\x001dFUö 	"*Rá\x0002å¨CòôöÅí«çWÏo<¿}õä8 ê\x00015 à\x0000d4= \x000f×jvÑÅ"î#\x000b\x001c\x001a#ò="oè Õ\x0006_mUnÕù\x0010cÒîèÐS\x0000Å\x001eP´?s±ÈU\x0002¬\x0010(µ-\x0002é)»³NA{DÙ\x001eQÉRÞ^\x000f]X\x000f]5\x001azè¶\x001bÖODTzDÅþ\x001aiz\x000fØjåÔ\x001ePä\x0001!çÝ±'\x0000:/|í\x000c
qàa[QN]\x0012©-(»r­§ \x001aM·¹í\x000ePÓ\x0001\x0007\x0016<Îm\x0014ÂÕßE%Ó\x0006ã
\x0017°Þ\x0015XoHQH"\x0000yG.áDHõ\x0006{óÍ\x0003eXXÌË.:³Õc7¶ß\x0007pTU1cFr$¥X\x0000ÕÍ\x0013\x0003\x000eªõ\x0006;B'"\x001a\x0018	Ì)©»ÔÊe+þZ¹5àÈi»üDDi@ì÷J \x0003´sIî\x0011lw#\x0008i Y0gÙjïdjèÛ¤ ª±ó´Z\x0006ëC7P,ØslýgôÐ6úxÒH\x0006Ù\x001dË¼Ì"ÂcÑc\x0001AÔÝ«3·zª MXw\x001abOD4p,Ús,¤ Sá¹)\x0014M³¨÷å"¦!á\x0000	í!ù5Bâýò\x0002É£rìvÆ\x0006Å\x000bDH!rÁùÈe©\x000e¬7Ä\x0011J;d'ºß0=\x0014 YÇ\x0015¨^¸/ÒéU¬òí¶¶Ï©Ãg°Â\x0005pU;t\x0010\x000f×¡)9!)ß¢\x00059aJ?º\x0004°æQô5rõûÿÇÞþz÷ûo\x001fÿñ__=â\x0015®þ+¾úîÿjt\x0017r3w\x0007$µj:Wx
å=÷PÜ^=¿º}Zÿúû^6¬\x001fûõ£Ñú±\Ç¶þ6gY§ö\x001cp[¾szýÔ¯lÖ@ûÿ8.	Bàtxk\x000eiß'\x0002à{\x0000Þh\x0003b^ÌzDpõ\x001f\x000fë	Úne\x0006\x0010z\x0000Áh\x0007È\x001dv °fÌ\x0002@_!2«\x000e\x0001=h\x0004À9ÉEåP¢X"p>é\x000eì\x000f>\x0003z\x0000É\x0008\x0000+Ô§¶\x0003yð	\x0003\x0000M¦±eÚ%)\x0000¹\x0007­.ñ\x0012ç/\x0000\q-àbÑK¼?!o
Àd:°3BE|Äz	4åÌî¢ÞíÖ¤é\x001d¨~ÇHd?Ù\x0018¢zöÛkbÝ\x0004\x0014q¡z
PïqÜ\x001d\x0005;ánÄpgÄf^D«øÌHÏ\x0015Ozi?Ã7GÇâ(u¼úIçâ b}#ÉKS¥e)Ò¯8ö\x001dôc8Ä·\x000b\x000f\x0002»E7ÿvÿgJÝ¿{ÿëý«'¿ÿã¿þ~ÿöçû»O'º°T
¬¸z\x0005\x001e[\x0013\x0005hg{ý¯M47?Ü¾àáR·/_=½}}U\x001d½oo_<¹½ys\x001c\x0016ö°ð\x0002°{D[\\x0018\x0002Ø\x001b9ÒÙÉÈmÐæ°¨EU#©¦\x001d^a¹urKº[n³®÷\x000cX¾å/\x0001\x000b\)àiG¢S_äaºFR	Ë3P\x001eU¸\x0004*tú0\x0018(´Ýa\x0013\x0007\x00178±\x0015/\x0000\x000bJ\x0010¥ô
XR±M\x0015ÐÍÊqg J=ªtÍrYÊ³¹ZLu\x00085ry«®ù\x000cX¹/\x0000\x001båUÍ\x0017'!Ø¡1ëÇ.pµJ\x000f«\h·d\x001e"ÏâòYw+énm|\x000e«\x0002
wj¿]ÎÁ¨ÙÉ´4ÌB[à/`2`t2.áe@r2q\x000b\x0016µ=¨x§F#mN;\x0003×àeÀ%Ü\x000c\x0007A\x0014hÀ\x0007/·kÔ­Ã\x0005\Ìq
n\x0006\ÂÏà\x001c4
®Ub£8XÍÆf\x0005þ\x0019¸\x0006?\x0003.àhPY:o\x0016XÞ³`X\x0013Ôâ¾º]\x0017pvap4à\x0012k\x0013¡Û1D-Qÿ^/Ø¬É?\x0003×àiÀ\x0005\
Ê¹HÎR\x0013¢º~ãZ1{NÁÕ\x000bø\x001aÄåHz»hUH.é1Üå}\x0006®Á×\x000b8\x001bu»\x0016\x0001çVf\x00052	\x001b_kûps¬÷\x0019¸\x0006g\x0003.àmPÉkçA¿ÍlÄ\x001cÛK0º\x001aªãÂÁÛÀ\x000bx\x001b¨\x001ds\x0008^õùBL:Uz;7y\x0006®ÁÛÀ\x000bx\x001bTØ\x00173Ïn½ªõ0\x0004ºt\x0010\x0005\x0007VÆ\x000b°2eÖðjûE 
q¨¨å\x0012A2\x000e\x0017¡d2` :KYeùC	Z\x0008S.`4\\x001c\x001fR9Ræ\x001fþÁ`.<\x0004\x0017.\x0002Î³ªºÕ\x0006OÒÍ8×\x0004Ç¦¨ï9Þïÿúé®i4õN°üx\x0008ÚËØ\x0008à±JYB2@\x000eÉ¶^aÏ\x0002ù9ÂËÀ¿¸ÀA*:1Éë\x000e\x0002n¶`îÁ\x0001­è.rB]("\x0014R;³ñlè\x001c®Ö\x0005\x001cÏÐË\x0018j#eøOåï¤s9LÂß2(ç$w\x001eÂ»\x000c:\x000fÅ¯Ö\x0005ur<Dkç\x0012m\x001e^èhþ¡©jÇ÷¤e\ØW_=ùÛýß{ËµC_¿ûíÃÕ/\x0015Ú×ïß}øpÿá4Xñ\x0002§w¸\x000f+r(ÚjC3	Ó¹|òçÛo½àê¡¯_>{}õMöõ«¯_ßî4¾+.ìqáEpE!r\x0017Yw¬\x0008.yõ\x0003J¥ çà¢\x001e\x0017]\x0004Wâ\x0002ñ¶_^¤*.í$©\x001eÌV¦ç\x001c\¾Çå/«dÑ)©¸Tº×,\x0012QÀÎô\x0005pÅ\x001eW¼\x0000.\x000f\x0002gC´>¦è\x001eÂ²)¾r\x0006¨C\x0002k1\x001aá"»UÖÝÕÍ\x0012Íûë\x0002gðèY`¥KlVÀWQ\x0005©ý©°dÎ`µ;	×ÃT\x0017\x0006-¼æÓÇ'A\x001f®]Cã²èâzRQêklw\x000fIÅðæûï\x001f\x0003\x0001{\x0008h\x0006\x0002°±Ë52Y$/\x001bäÙÈEK\x000cÔc ;\x000cÕ-Í÷¹´ù>Tw¡aHy3^Ç\x0010z\x000cÁ\x000e\x0003¥¥0·B`5ß\x0006Á\x0017Ie¸T¶\x001bL§!Ä\x001eB4àÑ55Õz@õa«)Öm´\x0019ÙÏcH=dx\x001d¤\x0007©bÈËÚuº\x000b®ñ;¦Jöx\x000c¹Çíö\x000bïÃ!åõ,U\x0017M1¸íòÄi\x000c¥ÇPì0h(ÀfÉIÞÜ\x0007Ñ³¯\x0000È\x000cÂá
Ûi\x001b¯\x0011\x0006þøÍ´²n¥\x0015DÈvû\x0000#ÃÙQÜ2
X@TÃÔ*îëa\x0012Ñg\x0017!ÙV\x00188\x000eìH.VËÚ­u'¤7<ÇÒ)çËQ]»Ç\x0018H\x000eìX®.²ÍsâãTX´A$'s³](G´g@\x000c,\x0007v4ç«}¥" ÈíV\x0010ò¾RïÄQN3 \x0006\x0000;`É:jdx®C3°)¾\x0005×\x001e5\x000c\x0006\x0016ì,,«\x0004\x00134\x0010­*o¹\x0013®èqòvÖ	\x0007ëvÖ):º{]ýXÔ³hÕ,ì0\x000c÷\x001aíî5·\x0010x\x0014\x0010A\x001bsÖtwlºÆ\x000cáZ£Ýµ\x0014Û°!\x0010«\x0005CQ£Â9¦uüx\x0010ÃµF»kÍ³ÿ¨Q\x001dç³¤Å\x001dr\x0001¶ûR¦A\x000c×\x001aí®5ó8\x001dÜ\x001d$!\x0005³î\x0004\x001d\x0019\x00006\x0001kMv×º\x001aÓVó\x000b?0-§)8Êr­	LÀ~<\x001aÞ.­\x001dp¨2Ñ]~ Ëk\x00048kw9%ÑvÛ\x0005´'ÄÖ}¾Å×½lë¹qQË
,ñ)§æ\x001bo\x0007Î¶«ß¦·¤\x0007[R\x0019³-!Ð©Ì­Ü	¸\x0004ÚQ-UÞ®\x000b\x0000\x000fZU\x0016ËÛZ·nÞ~|÷ö··W_ÿþîí/¿½=
',m?
rab+b&ZíhÛ£}s{uóâû/½¸úúùË\x0017ß<{q\x001c	õHÈ\x0012	÷\x000eÉVÎ$ð\x0014¢ø!\x00188_aÄ÷H¼) ÿÀe_-
EÕ
+\x0012K\x0018¡\x0011,a¦õ\x0008HÊ&+ehýÓWx
ØÃ¦»±^t(.Ê$_
\-Þàn§õ4Ô#I¦\x001bßB\x0017$!JàG\x001eµÜ"ÄÍ÷Ã\x001eI1EâHÄVJ¥uND%è\x0005É»Ýû³@ºÄ\x000e¶æ\x0004ËK\x0012\x000e{¢½1õHç&Oò±¼î02)xÃçN¬ÿ¼\x0014\x0015\x0010ciP"n6"\x0004\x0005\x0007(h
\x0007ÝSâôE(ictÛù)P\x0006.\x0001S2ñ¤[\x0013çM(èUq{\x000eù)H\x0006;\x000c¦ØÇ"
<\x00159¾\x0015\x0008äU(Áôªä\x0001J6õºRÎ`dA9ñºª·%¥aÉíö9OC\x0019,1bb=,\x000e¤g\x0019üÅ\x000còvY\x001dÈí1«'@ÁÁ\x0016£©-æéö¾\x001d0@\x001d´D°¶_²#\x000e\x0018M-1\x0016îX\x0016ãößÖx.\x000fhö¥I¦¡\x000c\x0018M-1y\x0019æYOk0²dÔ£µ=ié\x0014\x0018Cl¦ÁI]õµÜ÷Fø\x000b\x0012¯Þpò»rVÓH\x0006>AS>áû^\x0014JTD
\x0018Ý
eW¿j\x001aÊ\x0010 iB.­V8fuXÖØ7ìÎH2p#r#ÁR\x000f¸@IúP\x000fSBmO'A\x0019\x00144R°\x0015J\x0006î½kÆk½+¶fx`y4ey,E\x001aÄYbùZ\x00115pL©^úäÑä\x0007¨ËMa\x0002âDä\x001bS6µÄ4<<¦(z\x0018Xo½\x0014[ÛÛ³Û÷2Ð<ÙÒ|ZæØ.PÜb\x0017(9*ÍíÇS \x000c4O¦4\x0015['\x0008"Eu½jÀ"w%ãîHi(c\x001aÒêkpØ×\x000bkÆðûî\x0002%©)Î.ÞëÉëÔÑsNEÞÈé¤j\x0015L#z\x001a¸L¹\x001e\x0000IÝÂI&í£0¶ç\b y2¥y\x0016ó¼\x0004²\x0012t\x0011Ù\x001bíÛÈaWíu\x001aÊ@ódKó.Hqü\x0012X5\x0011©øgõGK\x0018\x0003Ç)Ç\x0003÷x-(\x0008Övó¢³q0ï\x0014\x0004dàx2åxÈY^\x001døû_(=AA¡ì\x0011ÎBñ\x0003Ç{S\x0007ò­\x0016¹îGq!±8Uæ)`\x001fö\x0003Ç{S\x0007\x001etÑL\x0017ËÉµy\x0003ÕEÖ>ÐlëDúã½)ÇCQ,¥xà
Zº=r|Ù®ê=\x0005É@ñÞâ¡z[º)¡\x0008/ò\x0005ñd»ªô\x0014(ãS£)Å\x0003k\x00146§¤\x0015,z)ÞJñb~'A\x0019(ÞR|u|EQ\x0018i\x001dD¯¾^\x001aK¿Ë\x000f4ïMiÞ¥Âíì\x000b\x0012®\x0015$¨Ã%nJp\x0004e yoJó.ô@W( 1
»ó¤P,ó\x0012~`zoÊô.Fõ½ê¹6ªé^ú´;ºk\x0016J\x0018ø1ò#\x000f~\x0017ª¯±êB$\x001eÊÝ ìÎa¨\x001b*píû5|\x001aânmy¯ãHR^¹Pµ;c¦~qì%\x0004ÄÍç_,½1ÕÅ©¼\x000fºE}°ÆûÙYî\x0011¥{T\x0019Ìvx¸5I\x0010Æ@²(5lÕ\x0011Ø\x0014{8©ú\x0000\x0017¹èCBLä¢¿ÄWUíN´Þ¢["6R
Z^wÆô8f\x000f²1\x001aîo1×ú\x0004çUÒçÕXÎÎ!·¡ö..Gýý¡\x001b°ñôý?þß»ÿê\x0011"Ø{\x0003îSc¼S¬u!B8"±þôÕí\x000fÿ\\x000e{\x0000=\x00084\x0006Áel¾8èÚJ|nîï£!P\x000fl!\x0000"«,\x0010jôâ$<F¯û°?\x0015òÑ\x0018|ÁÛcp!¸ëLAÉ\x0010ñØÀG\x0008=`\x000b\x0002YN-7\x0010üTÔR`ÒÎÎeë6û\x0010{\x0008Ñx\x001f\x0008DÈ£îÃ¢Ä²ì\x0003tUÝÝÇH=d¼\x000fx\x0000Q²hõ\x000bIouÜõ¹\x001e\x000f"÷ ²ñNTÇ1uå>u³|Ð[\x001d÷\x0012\x0007Qz\x0010Åx'¼Î;äx~\x0015C×za\x0016\x001d<2Ìèq :È\x0003Ï9ã­¨.USî\x000c´õu§ÕÀúí)\x0014#[\x001bÓ5Õ(±y¹ÕIÌ×ây\x0004\x0019Ë\x0014Ò±ù\x0015Ä05\x0018³u
Ïe¦\x001c*­$\x0000=L\x0002s\x0010\x0006¢\x0003c¦#/-Ó\x0015Bu8äÁ\x001aqµ°ÅÆ8Á@\x0013`Ì\x0013, ¢\x0002jQ\x0006f\x0010\x000bÜvÛÏ\x0014ÁÂ±e\x0010â81\x0008O\x0002ÃâÈ£GXKØyâÝ\/Ë\x0019/\x000f±\x0014s,X\x0001è\x0015qQ$ýzÑÉÀ\x0019\x000cõÿüø×Á\x001d¬ÿû«¿\x001a\x001bÝ"c=f\x001c± luMn{À¥¡ì\x0000\x0005\x000fó,¯g¯|\x0001¤L\x000eô|åÝºó	&ÿì®8ó\x0003\x0006,<ÕÀP\x0006Ñg%Ç=
L8Ó+æ8ýA£ï\x0017ï>¾¿ÿ\x001fßÜýýì\x001b*­^I8¨\Õ+ÙµÁ/^~ÿªb¹ùö\x00118°ÇÖ8\x0000¥Ö±â(ª\x001fRP\x001f1ìz&38¨ÇAÖ8X P2	!ÊØH®àÐ\x0010¬`ø\x001e·Q#ÀVä\x0018hMXcfB"ÀMÙóY\x001c¡Ç\x0011¬qTOÝ\x000b!òð\x0011Ù 2!Ýº­\x0019\x001c±Ç\x0011­qEò¯%¨P¦deT\x0002n·®f\x0006Fêa$k\x0018Ù©²l¢>LÉ­×|ÏyÁ{\x001cÙ\x001aG¢äT9¯¡`öYOUÞM¶ÍÀ(=b¾\x001d$u\x0002<0Yú\x00141'©\x000ebe§=
ÀÑæñÐ¢hxÍã5\x0008j®@îGÔ ¥ælnNç9ªÓÞK×~Ý\x0011/v7ìOß\x00012Ð9óyõ¨ZEv¨QíuÒ\x001dÚ_3ndxaàs0'ô\x0002RÄ\x001c¸\Vòê9;Ý\x0011·;\x0007z\x0006ÈÀè`Né\x0005¹|pßÂ\x0001d¦}Ú#;\x0003d t0çtÎª7]ø6Øº\x0002ÑÜ¯4\x00022p:X:×6Iæ\x0001Z}ù\x0002¤ \x0012ÇF8\x0006R\x0007sV/"\x0013Æ\x001b\x0002*g³([Ô
\x0001+\x001a\x0019X\x001d¬i\x001d\x0000dÄj5O´\x0000èUçÑF8\x0006Z\x0007k^\x0007|Ó/D'S¯¹¾TÝú¿	 8ð:Zó:ÔV¯Ãµ±¨ÜVõ­üE\x001cx\x001d­y\x001dÀ7ÉØº#¬¾%¯³ '+O\x000b\x0007:Dk:\x0004(ú \x0005øÑ¼\x0001ÊxNÛ\x0019yZ8°\x0008Z³\x0008dã	ÖD·Þ\x0011¢Í\x0019\x000c³@\x0006ëÖÖáýqð¬¢ÍÔ$Bh<@Þ\x0008Ç`|ÑÚørÃHDÁ\x0001|ÈZ;¢TùT\x001cÞÈ?ÁÁú¢µõ%\x000fÜ«»\x0000iµ\x0000K¶\x0017´\x0001É\x0019Ýu\x001a\x0016Y\x001b-JN\x0012¤Õ¥JëËH\x0010!ÖÀ*¦F@`¬COxÝ\x0011\x00121~bA\x001b\x0001»o3@Æä¢µõ%n\x000eMmGÒÚQQ=\x0014Ø/\x001c\x00012\x0004#d\x001dP\x0002\x0019úÀêÄ2*ß¡ÅhAÞmm\x00012Ð\x0008YÓ\x0008¿\x001e¶)S\x0015\x0008h>®\x0001;äÝªÑ\x0019 C0BÖÁ\x0008\x000f¹A¹ì>J¥I\x0005"ÝàÕ´ªhàC²æC.ão)__+\x0015FÚmM1Ð!YÓaý[÷©¬W½ò¡à@«à\x00066$k6¬Ña]wÛ\x000eôê\x0010wr5 ¾\x0018]\x0010?Ä"Þ:\x0016ñäÔ?IÜ4"\x001bBZí\x0000»\x0005ï38\x0006V÷Ö¬î³ª>øXHR¤¯êvU(g`\x000cî­9Ý\x0007'³>UK\x0014ÐÖê>¼Õ±\x001a(Ý[SzpNzA}¨Ò;^«Ê\
ñÁÐÑ}:Ø+$-\x0007E_\x000c+\x0019ùX~`toÍèÁùk¹\x001e\x0018UÜÔ£Pð%mÏØÄ1\x0010º·&tÏªØ$@´\x0016¨Þs©j¯Û*ò\x0003¡{kB\x000f.sÒÃNHwd{DØ,Ò½5¥µ2\x0007\x001e©\x0014\x001d3d\x0003\x0019\x000cî­9½r$®yº£$ê$\x001dÝÒ	 aàô`Íé\x0001QÔMY\x0019[Ë0ëÓ\x001dAgd}Ã@êÁÔ£Õ.{ åÁª\x001d-ic­ñûætÀY \x0003­\x0007kZçq¯¡%Ox4ªê2\x0007Ô\x001d±;Z\x0003¯\x0007s^ÕÍªÇIz(êHuY\x0016­\x001cø0VÐóa=OE¬VÐ!íä=dG¶\x0014Ì\x0000Yê.ËîÌ]øò¾ãS$)\x0013 rÝë>Ñ#
ðÏw¿Ü}¨«Úv~\x0002Ææ\x0000k\x0001£\x001d\x001e\x0006ÑàT\x0017åoJÚkävõf§JÿººÒ¥øïîK­þ[;ûWDóY^IÚ»\x0015?òFiÛ\x0001éæé{F.ËãÖdó­Ix-5ug¼êo\x0004-Ø2»û]\x0015¶Þþ¿\x001a_\x0017_¤zgX	\x0016\x00195Ö2Ë¨<<cT.pùÉKOÙk
HÓ\x0011°Û\x0014=we@eTMà\x000b¼2ôm¦\x000bØfBU\x000cdwx\x0015o­ÖW í)v³\x000f¥\x000fñ`°ÇÃU\ò]ÿ\x0005:Ó@5êª`\x0005\x0007Òg\x0016:ÙÃá¾{©Dea1­Y)¢\x0018ê2"O¤Ï¶.À8Ø\x0001h×Ç_,­Ó\x000fóüÆf¶øÌµ\x0017°n¬@ _²\x0017kÌoôôX=µ\x0007Ö­zjæÖÍ7îÔ¤«0O\x0011\x0015+Îº}Ú
.þÀ!Î¬!ÇÚ<úáê{^Ø§ß?\x0007¢GÓ¯±s1©ë`P/Ó~Ëßë«ïù÷7ÏÿùT©\x0001
öPÐ\x001eJf²ÔÚBÖbtV\x0014ÔÊÎÝ\x001e9,Ôc¡\x000blç\x000c_Û\x0016¯:õögÝÝX`\x000eï±ø\x000b`	ò6\I²He\x000e«\x0005ké0\x001a±Ðc	öX\x0008$Á\x0014°ÂjF<E;\x0005h7	;%öXâ\x0005°¬=Ë\x0018r¶EK¿ÂîË\x001cÔCIæP\x0017C×l\x000b°¶þ¹ýß\x0019,¹Ç/²-)¬ÛÒf\x0001±ÄS^·Åîº\x001eK1Ç\x0012JÐ\x0014\x0018\x0010Å\x0001­íZG\x0004`&°t-)ÌÎ~cXºNºªMV*ÉÚ´µ\x0001\x00033Ò¾=ïóÎ¨ú\x0005'kä\x0001ugÌ\x000c\x0019\x000cÄ\x000f\x0017`þ\x0018Xt·µÉóàåö;mß¸+ú8e ~¸\x0000ó#q]´JWe9d\x001afF ýì\x0019,\x0003ñÃ%¿pR¶a)R\x0002ÊjÏª\x0001GÚËgÀ\x000cÌ\x000f\x0017 þ²L]U\x0006\x0005­\x000c«\x001cc\x0007f ~¸\x0000÷çxÐ!JªÌE¤Ùèw;
æHf\x0014ÊXÂCï¿!o.Yæê¥bÔ\x0012Ä@»ùÀ£ªóÍñä!*Ó\x001fÖ¨ìÓÕ×ï~ûpõíÝûw\x001f\x001f\x0003ùïîøÏ©zÆYë-2=ÆÅK®ÿv¹øÙûý»òæêëÏ^_}{óêå÷Ç×ýúÑfý:±®?^ç ë\x0017vÌ>ìN=\?õë'õW[Õ¢\^ipt!­ëÏûÑãÜúõJtgh½\x0012çÁH:Ë7/am\x00174­}ÜÍ"\x001fG!\x001a°Þ\x0002ýa\x001d\x0013ýû\x001dËiÞ}úßmõ§@ðÑ«º.®Ê­û\x0017ß°æÍ¿<\x0006\x0003ö\x0018Ð\x000eÓ.\x000eð	ÖªÕUç\x001cvÓws\x0010¨@_æ6ø\x001eÿ¢¶¡\x0012Ëx\x001b\x0002Ïj\x0010þòîÃý¿üíêæí¯¿ßýr"\x0008>ÜäB\x0016Í|¢¬ÚÌ\x000ewõLÿòòõíw¾ºyñôùÍ7ÿ<ã8àÀ\x001e\x0007â\x0000\x0019ïS\x0003À¤Ö(Ké0Ö\x0010nÏ8Íâ \x001e\x0007YâQ¨ºKkåp=_íPAI»}¥³8|Ã[âÀ,\x0003\x000c \x0006Kz®<ÊhE(ûSÖfq\x001eG°ÄQ]¦G	ÂT>\x0004#ú\x001f0Ä\x0011{\x001cÑ\x0012GÑÙ\x0018>ê$¯àä\x0004
Z\x001e«ÔÃH0¢ó¢m\x0003\x0018\x0017I®\x0005\x0006®×ÃgK\x001c¹Ç-·#õXÕk
^
Z\x0005\x0007íwÎâ(=b¹\x001fèdx=\x000fUÙâÜ ¤0\x000cîatýBÎ\x0012FuÐC£rÄ¤·<d\x0019²\x0004\x0005vßÜflnIçhù×s´$2Ô|½æ÷\x0003\x0006:\x0007K>Ï¬tÚÔo/U^1	\x001aX\x0002\x0019ø\x001c,	=FÔ\x000eàA½5¬D\x0008»²\x0004³@\x0006B\x0007KF/\x0014äyªþíE£(ED\x0000\x000c\x0010\x0006F\x0007KJOÔf¹¨¦7V
G.»Õ)³8\x0006F\x0007CJ¯Üí%ëJÓ/¯@X§«e\x0015 îÆ\x001f³8\x0006J\x0007KNO¬ùÔ\x000e\x0016KÂHóIT×\x001dò¾ä÷,\x000bÁ\x000cÞ2±YÕWöÅä¬¸;\x0019}\x0012\x0008\x000e,,yæ`h@\x0002píS3¾E®zönÂfý³úç\x0001È`|ÑÒøæÊíY­²HÄa
£°Èþà¡Ù
\x0019L\x0016Z¬u$:8Vnmõ¹è\x0015Ii7\x0001:\x000bd¸ëhy×sm
¸èd.'±ó(8Ân"z\x0016ÇpÕÑòª\x0017îÏÍöòMj¶PmoÞ-B\x0004BE~V`ÍÆ!|WZ<å!H-\x0010p5½!áá
Y
\x0019\x0001\x001b\x0010rrC<¹\x0000Ùo\x001d\x00052Ü\x00102¼!4áá\x0015aÕ\x0001iº®g\x000cÚc³¯ë×»#R'qø\x000c½!\x0019\x0006\x000e?äÔÐ°Q\x0008\x0018CÝÝ\x0011è³8\x0006.ô\X÷\x0003¸Ô·íÇ¹n\x001b¢&+àîtÔY cfÑ0\x0010a\x0015\x0008©-s©®Ü·\x001b^º®Ás+¡ÕOx\x0013WKßÓl8;®Eç gêr8ÒW:\x000b>CÆp¢fFp¢D£îMÊ»\x00032¦£Ý`jÄk
¦\x0010
Ï×>4-í\x001aóVpyw\x0005]\x001f\x000b\x0007\x0003¯#õ\x0007}\x001dùæÝÏ\x001fï?½¿zzÿîý¯÷¿#ôü\x0002g[©¯ÁEDÚ/{ùäûÛ7¯®Þ¾|õôöùq$¾GâMDÔ\x000cW(YJe¼sI&#£\x0007S$¡G\x0012¬4_8rQ\x0017 ¢ÅÇó}vÓgÄ\x001eH4\x0005RHf,UÇ\x0011D¶:â¹ºÃ¦HR$Ù^\x0013§ÉºÈú®I¯"	»9i$¹G
úïÙ\x0012\x0010¾÷xy}Ctû\x0013\x001egq\x001eG1ÅAÃÄ\x0005G$Mrx_\x0015È~åÌ$CfhfÞ\x0008I,Ò·\oI¶\x001ajéôðÅ\x0014Ê@&`É&\x0008jS­¬î¯z2\x000fªÓÅÏ\x000c»õd³PhB¦PêVdÙ\x0015\x001eê,»\x0012ÞxÜÁ9\x000be F°dÆ°»J²«Ú±Ö\x0006çY\x0007R\x001cÉ°_v=\x000be`F°¤FVä\x0012j¬Ñ®ÌÌà¬V\x0007ùýqK³H\x0006B\x0001KF	<-¸)ÁçÁQ(çKY\x001ehÊÚ,Á\x0012©)æ¸KKl*\x0004CÒ
#3-'à`ÑÔ\x0014C2Þ?¿4÷{L"B\x000ew8§¡\x000cö\x000bMíW
\x000fÕ±'rz¾È9}ð-»Ó~¦¡\x000c\x001eM/=\x0014-hàZ¨å	Dp¡F*û%ð³@;¦w\x001e¹\x001dI^\x0018ëö´Ñ\x0000^e\x0013«3\x0019vëßg\x000cW\x001eM¯<÷ÊÇH+\x0010õñöÛ+gýHìãù\x0016\x0004k8ÿeÅÁÉ±n3ùeßw¿ßý|õêÝÛ\x000fwï9õ¤´\x0016«äê}õ*ú\x0010_Âæ\x0018¿ïß<¹½zõòÅëWß\x001c_=ö«G£ÕGàYz¤PòÂ\x0002GÚ\x0017>¹zêWOV«÷×Z^SX×®-^´ØïÝr±&\x0017ïûÅ{£ÅW\x0007q-:2Õ§r_pË0M®>ô«\x000fVÇ^(\x0000±È\x0008ÎzìõA¡¸Mm±ÉÕÇ~õÑêÛ\x001a\x001e$XÀ<­ÖmJÖL®>õ«OV«GN´:?\x0014\x001dàúí5­»SV6¹úÜ¯>[ £§«ÉY\x0008­­Þ©kAþ«/ýêÕêAÔM\x0000\x0013¸7OòÐÊ]æÁqô°ãZÇÍ»O\x001f	º_ß¿ÿýÓ¿ývÿþÃi\x0010(¨\x0001äEQZFîk35ð\x000eqÓß~ùæûeî×·¯¿ùáÙí«ÞA7 ¡\x001e	Y"©!èÿÇÝÛ-Ç\x001b[Â¯R/p\x0018øÿ¾*RÕjvP¤\x000e\x0014öÜ8J-ºÍ\x00085yL\x001dö\ÍkÌÝ\\x001e¯Ño2Oò!72Q@µ°«ö®¬cbl©ÚöÉµ\x0001d&\x0012kå\x0016`¬p8A+lVÐM@¼êV\x000bæ\x000015\x0010Ã
\x0004z\x0011u\x0006"\x001dvb¤ÛB\x001e^IHBKz\x000e\x0012[#±¬H¬Ïíca\x0018\x0002ÉH`n¸¾\Ò\x001c$®FâX\x0018Û\x0001¥æä\x0013\x001dí®¾\x0000í\x001c$¾FâY(ß\x0000Ã@hªtÞ]Á\x0017$ÝkÃ\x001c ¡\x0006\x00128\x0018\x001frM-ÐDË\x0000\x0004'O\x0013Ø×h$ÖH"+\x0012ëò WB¢\x001dö!Ëd?¹®\x0011Î¼\x0019H6ÍúYy\x0015Jò]\x0016Ï	´\Ú\x000cÅáDÑ¯\x000eÎAÒÆEÖÀh¼ÏÕç0p\x0000ûÛKÑö
}Ú9PÀ(Y#cÊ§(ÆClÉ]\x0019éÆ9ayNç%"Y#Ê\x001f
¥ñÃÕ\x0011ÿQPÜö|§ÛÌw^ß?þö¯Åé:\x0019üÏe\x001b¡èö¤ñø.®Ý9×Br1_¯.\x0013eú'Þ@×\x00084\x0017\x0002\x001d#eñéêíÏ_y¯:-ýXái\x0012\x0004SC0\x0010<**."
%v'\x0008£rI ¸\x001aãàb~W\x0002±Áü\x001cÒ
¸ÑÝIæÚüÀg¾µø\x000c¤=ù\x0005F9G\x0000ü(GÔ\x0014\x0000èíªQ;\x000e\x0004Yû\x0017­ð­"ÝÈ\x0005\x0001£\x0013D\x00004H²y"
6\x0008ÁR«r$¢Óvìb\x0012æ\x0018KÆs\x000c·¤1x
]"ÁF:\x0008RôOÂÐcÉwAcÒã:DM$ð	\x000eF\x0004iFù#&ah\x000e³ä;Í!}ü,\x00076Â\x001c8øh\x001d\·\x001c;\x0015jÎ³â;Ï\x0001´ÈeÆ =©`[
)¨õ+;S1´¹\x0005ß\x000eé\x000eÛ×\x0003RÄ\X³ØZÑáI\x00183­øÎt\x0000þ@1¤m	ÈR ad\x000bBs¤\x0015ã\x0016D\x001a®öXe*WC0ZéQ¦½I\x0018#­ø´\x000fX÷Ê\x0017Ö\x000beH_Y+3ÚÓ9\x0005n´æ;ÒÞuðJá¯2´âsKº9ÒïH{#NBv­^GâkÓÞ£kU~´+b\x0012æHk¾#
\x001fß#\x0006«)ÝÖVÓ:D¶(\x001dêgwrôîÎq²)';]ä°Bk ]K?:
´\x000fbâK8\x0003\x0002ýîì)ß¥oÖ\x000f/ÿq
æþc\x001e´\x000e\x0012QS4JÌ5´\x0014\x001e°³C(Ùs³gWù2}³<¿¼MÒ?úÓ\x001eh\x0006Á\x0006Ï\x0015PZ¼2BúaYDÄ&;\x0011ûÃ±À\x0014_Û÷% þI{wùë}úO-n\x001f~zúéo÷w°Çf¿\x0019iËëvZ\x001eèÈª\x0006Ø3h»-]Ë\x000f«Ë´Ín¯ÏÏ®Î~X-ÞÁV\x001b}1#DªF¤ø\x0011yA}õ!\x001aì}VÑ`Ù\x0003ôp{ùtIócJ[\¥tÍ/É Ý]¶Û>\x001f©!\x0019~H@r*qã	Ê\x001f£v^wZ~>&[c²üR2\x001fr\x000b\x001b@áU=+dº¬pó!¹\x001a;\x000886v\x001e1Ä©¨\x000b¦~'î|L¡Æ\x0014I!9µ*bgCòyeënÎ<\x001fS¬1EvLÂz\x0014\x000cUÐ<ê4>º\x001cd\x000bÝ\x0016½Ù6õ®!6#'wâsÇqÌïÕù<	ì;´¾[þ\x000fª
¸ü\x0011W\x0000Ñs¾ü\x000båé¶\x0013°\x0006\x0003ìÈ½Â|LMÈG¹ÐD'
]DS·`> &ÞJþ\x000bcG¹uKÁÉÊÂ*ÐÃrN±»\x0008ÙD\y\x000bº5èË}$	@=QÊÆn÷Ê|PMÈü1WäNëäõ]+]S\x0003-Sìò~ÎGÔD\y\x000bRIEDIr#Á#ýr¢[J\x000fÊ7 <ÿ2é\x0000:C°Ré\x0010ÑmÖ{|ÅP¾Ïû;\x001fTGÈ#$\x0012	Iv{*ýc\x001cFN+%ÈË®ÈÍ|PM"!IhAÕ8©n·Ôì\x000f\x001eÜ TI(þL\x0002Ä\x0008ópI
º\x0016¸U°ÒSÔå?SªÉ$Ô\x00112	ECýJ\x001aEéGJ>¨á±\x001f)Õ^Þù3	\x0011\x0005ªFÂh\x001c½ø\x0007MCfÎò_\x000bUM¨#d\x0013Ò 	$0ùà\x000b´×t úãñó!5¹âÏ%DØ¸¾ 	ëD³òÎu».çjr	u\B8êÕ^¡\x0010»¼\x000fWÊugÐæjÒ	ÅN\x0008y¬óTÒ\x000fªø½>\x0005Þ|DM.¡Øs	\x001daä\x0011)Ò×¢\x0015.S_\x0018d>¨&Pü¹\x0004Ü82õ\x0012)9·tãÀr¿ê÷cÏÇÔ¤\x0012=Ð1E¥Lg¯Tô\x0018ãÆ\x0008\x0015úO\x0018³Aé&ÐGH%,\x001a¹vH\x00182YI»Owé»çjR	ÍJ¤LÁÐk>Èj;êÐ!
(øæºÉ%ô\x0011r	àÒË `\x0002\x0011Óso©Îçù\x0013YÝ>\x0004°§\x0012:ôtö}Ú)ªÇÚï*ên\x001bÒ|PM2¡L¤{T.ÈBË\x0005½\x0005xMìT¾Ïe<\x001fTLhödB(Ê
JHvL\x001dVê\x0008\x0019n	}dBäFÐtß=ÁbKòç¸JýFÄù\Bóç\x0012!åãF[\x0019+p6\x0019\x0008«,5IwÙ§çjr	ÍK¤\x0004ÉRß »+%i(ôû-çj	ÍL\x0004½i¤\x000eD\x001e¬,pfæ:Âëi	ÃLè\x0018,¾*¥])a×PJÔ»äCó15¹áÏ%<=ci(w\x000e£eé2åµ1M.aØs	\x001d¡w?×ZRZDzÖ
ÍÁ8vßgÚ\x0017xö°«75Ä\x0004\x000be¨3>PzÎ_k1M2ì\x0011*Ý94¨´ÓhjÚö\x0010»\x0012ZóA5\x000eÝð;ô®¹9ðj Çç@¢ë\x0012ÀÏÆd\x001b×gù]_HC|»±)Ð\x001aËdIWU}>¨ÆMX~7\x0001äã\x001egM 
\x0014}_:i\x0008*ð7TÙÆOX~?\x0011¤¥\x0017\x0001r$<RÆ[[Æ7øWªñ\x0013ßOøhË<G
Âx¦¡¹,©ùH¶ñ\x0013ßOø\x0010éÆkci0\x0006\x001b&´´]¶ÌÙ \ã(\x001c¿£ð¡)\x0007\x000fn¸RHU\x0000\x0013\x001fü\x001a?áøý÷\x001a${rs¯\x0007ìÜ.^0AÓ57¨ÆO8~?á£k<(ª\x0011&\x0011iª¿éÚö·#¸	ãP.J9ï¨4\x0005/MPü^¡þò÷×õËýsSý\x000eã~Ã\x0006O\x0017¨3à¥>zJlm©á
mÝ8UZø½P[\x0012\x000cè5X¨uåÀð_®tü\x001d¶x\x0004l:(wB¹£ÚI¹-åNÿÞh¶¡\x0019s\x000chÑ¢°C!h ÉYäéS!ð¿Xµ\x000cù´\x001daC\x0002\x001cª3F¡éÍ4:\x001cÿ'ü\x000eZ8Êa³\x0006i\x0015h\x0019¬µÇRkïÊq\x001cpçÿÝ<Æ²¥\x001bW\x0019OS^Òas¾Ü(ûÌ¤\x0007¼¡þå¥Y4ÿÝ\x000bÿAÓ´d\x000bC³TuO¸ø[»Õ_~\x0017×\x0011ÔR\x001eLAMøÒáMté¤u\x0007l\x000f(\x0002ün;\x001eã¤é`À\\x0007H®\x0010iºb\x001aË^^\x0013n\x001b;\x0004ZijÌ\x00170cÃHÔI¬Ù¥öqë }ä¯\x001dL"\x000e)÷gGU6Åê'TßBõwþBÛàæsõ0E3tFÇsì©cÂµÞÂµæw÷\x0008\x0006TfÿÊUQâ\x000fÇ(_m·|\x0007¿_Ôvho\x000e ï\x001b÷b´E\x000f¤uÙ¼7@o\x0006Ñ{Þþí5ü0 ã+´Ò B%\x0002\x0004¬X¢¥qÔ\x000eº­ßáóö»ôûùêz'jÎ\x0005y] è¡ì9@\x0000é¬a&­%\x0008ºKÇ1\x0019B»\x0008|« #>Ê¥/²u«@mr\x00179ò\x0004\x0008ª ø6$^ãh<9AÐ$Ë¢L/W\x000cA7\x00104\x001f\Ó¨î P'°TÝ\x000cu2\x0004Ó@0Ç\x0019'\x000cP)lfÕí\x0000À6\x0008,\x001f2]c\x001cõiÐ/!\x0008m\x0011\\x0003ÁñApÈK \x0004äÈO\x0010¨õ_ÂØç|\x0008Êû¿\x0008/u
ôÃw¨Sòé~qýðóãÀ\x0010wþ»ß½_Ã}Ê}Ëj£Ái\x0012âÂz,{\x0007\x001b»)ñ O°Z\¿½ü:OBc´ªV\x0007\x001am:1:[í\x001d²1	g°&A\x0019×îØÛjS[m\x000eµZKìé\x000c\x000e¤T¶:à(z²ºë.§Yíj«ÝÿÃV\x000f\x0007Qª-*ÇôCµC>¯\x0017g\x000f/÷³§×OÏO/w\x000f?ýmýú2·ØB\x0016\x0016\x000c¼H\x001a( Q¡0ÊìÐ\,\x0017gç·«ÅÙÕÝë«ÛÅ»ó³\x001fw·»ñé\x001a>\x001a>ä\x000b\x0007|\x001eýòÆ\x0015|£¢»à35>s4|\x0006w£L×(TGNø(å\x0010n´é\x0010|¶Æg\x000fFÈ0R1ó²B1Bø~ >WãsG[¿¡[&kz	z;ö iñõù8\x000eÅçk|þhëÚXáw¬±	Û¸vä\x0001ØB-\x001c
D-\x001a
ª4¥'DÌt7K;\x0014^¬áÅ£Áó¤©]7fÞ,zs}êõÃðmnÉRmØO\x0000ÐÐ¥YHüÞýÙí\x001a:\x0014lðÉ£áøà<¨ìYM¯6è(Ýë!\x0000ÜE\x001e-yI;Ôà	LkiË|1@Ù×Ð8\x0010`¼È£e/F\x0011\x0001UÊ*¡k4¯`É^dWöçPMö"¾\x0018AéYÚe\úFA\x000fåX+Ø¤/òhù±t+1>Ôz_ò\x0017±ë¶0\x001b`¿È£%0F\x0013Å\x0016¶¼Ö:Oba\lñ\x0000M\x0002#Á¤Ð\x0014OZ\x0004¢:ñÔ²\x0000\x001eí\x000c6Y<Z\x001ac\x001c]!ÞmIS\x0004Ðr¦\x001e\x0002°ÉcäÑ\x0012\x0019«üX´ÚÅ\x0007r2Þ\x001d)ÇVM"£È¤-êQ\x0015Ñë2¤ãm\x0011<=\x0017UM&£ÉX[\x0004]a¢\x0019Ï`Ð$ÁÖçP:\x0014`[9Z&c7µ6k<°äfF\x001fÉª&QGËd\x0012*AB¶¾PÁPÕ,mÑ#Ý%TÈ¨£%2ÐoNÔlîñ¡hÂö_\x001d\x000e\x0005Ø$2êhLºâJÜ¡Ú0\x0018¨òÑN`Ç¨£å1\x0016IdÂ²Ù¤YEwxóP|M\x001a£Æä¤\x000cPÃ^Íë·\x00018Ê*~\x0008À&QGKc ÙbÀ70y`¡\x0018øÓE©Kat(¾&QGËb\x001c\x000en%|¦}Ä>ÝïX\x001eT7I>R\x0012£cÔäAü\x0016É,]Ù ¡Ïf9\x0017 q[ÄØé\x0007z@üñ~ý¸ø1\x0019ýÛ¹bPÐÅç¥F\x0011F
½gùî§á5´èÇÕòrñcúm5¢ûE\x0010T
A±A\x0000AOTM\x000eB`f©uXB2ý³É\x0010t
A³A0¢4pz%±H¤Ai\x0004Waô~:	©\x0011\x0018>\x0004ÊQèõÊb\x001f»V\x0014vÝ·ôÉ\x0010l
Á2BÈT+½6X\x0006Ñ*\x0012%v£G ø\x001açÒ:«`¨YVÃ|\x0004Bð£\x000ex\x0012PC\x0008|\x0010Å1\x0016é;7÷hLá|û(Ö\x0008"ã"\x0004¤¿K\x00101ÍÖ `\x0010FT'BØ<B\x000cQAða\x0008J\x001eº®óYÐ(5Lês2&,HÆ¸ õÌÙVúâ'2ï$£i Ênõ6ÖÖ_^û\x0018¸ \x0019\x00037(&"½7òkmR\x000c\x0017¸Ö¡\x000c/4X|þ\x0008Ð\x00063\x0011Z\x0004¶³à\x001aû\x001d£ý¥,\x0010ôÀõ1@ \x000cÉôçF&Ch|ªäsª\x0016Õ4 ?!jãhðÅ¸Ñòþ$\x0000K|>ÕÂ¬&ª\x0008ôÖPsC\x000cí\x001c¨Æ§*>j}iî¼\x000eÄ4òk[Ö!x'ahn\x000bïº`§ \x0002Z\x001bEê\x0006\x0005\x0013Æ§*>
ºóÑP\x0006GÓR	CmÁ³­Cª*¾\Õê \x0003L:ÜªÜ``;\x000fM®ªøÕä7QM )ÓKù\x001fM­	¶<I5~I1ú%\x0010NÀó\x0010#Î:i\x0013 \x001c\x0018A7gZ3é?îþÜÈa#\x00119\x000e(@§¨K¨Ë\x0005`ma\x000fS¨ãªf(¹
%¹YN(Ú¢õÈ$RWª\x0007¤xÈub3c5ß-¢Dmï-6÷hí\x000c-Geú%âw\x001bKñ®"Ý¸PJïppå.ÁV¡ù\x001d\x0014^$ài\x0017aSÜZ\x001fÙ¶Vtå\x001d<ÕtºcÐ\x0005Õr\x0005qñ»ÎzÐu:\x0019\x0011\x000bg\x0006kæ\x001aºJáìàõPÂ¶\x0005Øô\x0003\x0015`ß¬\x001f~zMVÎ4?ý·
\x0013\x0014Ô¼\x001e,e \x00169V\x0012_^¾½ºK?î¶^×Ök&ë'á#i<Qà(,¦t9*&Zojë
õf°`ò(
\x0006qÔ.\x0019-M°ÞÖÖ[&ë£(Ìâ1\x0014ù@O÷!ß'Ph½«­wLÖÃû\x000f~{MÃc*
T¢VÉòXïkë=õ
HK\x001cRæZì\x000b×Ã\x0005\x001e)sÕh7ÎþÖÚúÀôí­@}Ðtj#
\\x0000v¡:\x001amÚßúX[\x001f¾½òDÔ¤´ û§(ÄÒ¡Ïð6ÍúMuX
\x0007ëãÓ´RÚ9e'jRò£\x0015½	Ö7ÑJr+kN\x0004¬Ge¤"ÞçMIj¢õ¿\\x000eß)LÞõ\x0011_kÓ·§W6o­l\¦äòN\x0016%\x0013K\x0015y0_\x0015óG\x001bXv\x001fü¶´qÛ/\x000fëÇÇûÙZ22×â­÷ôTî\x0003X\x0008\x0006âþÑÇÿÅåååX¢Fæ«Ú|Åe¾v¨%m\x0010Å~G¥øäÆgIö·_×ök.û-¥C¬°ÁRËR?Ub4åb¿©í7lÛ§	Z_êðÒ¶pZñîýí·µýË~gQ; yÎb¿\x0012ô\x00165¬\x0004ý®¶ß±}<¼É\x000b9Ü<<gJâ¸\x000e¯¯÷\Æ\x0006\x0000~|å@î`øø.*r<W`~¨Í\x000flgW\x0011Õ\x0015p*\x001bd ÖZó\x001a\x001fþßßþXÛ\x001fÙ>¿"¾áó[lrùóWä;~ó¢Ïðý\x001d6æÁÑEÏ\x0013\x001fNÆ\x001d\x0003Øûß\x0006^¶È\x001bâÆ¯/O<î}ªÂÓ8ùMàl×	\x0014(6\x000f\x0018§OIOZ\x0006.ë°+ÙânÜÄ]i¨©H\x0019`^rmþ&îJ¶Àë\x0005½
ÀáEª\x001a%+kû7WrE^#\x001c<¤¯§:º²jaÊÜd\x0013y%[èMÑ\x000b§¬´º)EEÎ´R\x0007Ù/É\x0016¿@Ý
·T5@Z\x0001®\x0000 \x0000 Ø\x0002@:Ä\x0014À\x0015Ïn\x001fb×å
 	\x0001+\x0004¤ô­~ù2áZì\x001f¨E\x0000´·/® \x0000\x001d²0\x0001°\x0014Ä\x0002½Éñ\x001eß)ö7a@q\x0001Ð\x000bÃö\x0015c-Ñ÷mÚ\x001a¥äÂª	\x0003+\x000c"\x0003TqX¸ÒZP\x001f\a@5a@±\x0001ë\x000b\x000fRÂ¢ñÍKYc+SM\x0018P\aÀXYè\x0013ÓqÔ\x0019Kq"vXO\x0001Ð\Â\x0014×-Ìx
S;©IR	E\x001bÊåD_Çb*&)®8fl$¾\x0014#CéM¦X\x0011¸ps\x000bS\×0 >
ÈT\x0000\x0003Fxma"êLN\x0004 0¬¹Â0P%Z¢2'hQþ\x001cÈßxìo¢°fÂ<\x0008&°\x0017V;¢L\x0014+
ë&
k¶(ì\x000fÕÁP!B[z:\x0012}uú©\x0000(¦Ù¢X(\x0002&Àx
Õº°­\x0018ÁäBu«7\x0017ú\x001eXNr.Hè´"\x001e\x001d©¥70\x0001äbLwÊm\x0018ÒðÁ%\x0010tµ¤xü(]î¹\x001cªt¿á\x0018a\x0004]`H¢¨ºU®g;\x0008Þ&dFÛ0RvÄ·©Ì_(äyIÑ-\x0012M\x001cY¢þ\x000e\x0007ã®2ÆÕØ\x0018\x0012ÕrU;ø]÷/ÊJ\x000e`x)ûÈUoô·H\x0015\x000b\x00195½É\x001d´^\x0013Þ:¶WqCi/Ë\x00194yàñ*qüÁrÒJ¬ÛXóUÞi%³rTx÷ôèÄuï­ÖI®Â/L%ì¥\x0014\x001aÞ%ä{y%úb\x0019ûâ°ÛÖv3iý.\x0019ù4w*\x001eN\x0000\x000e\x001cx\x0015èÖRÁÒâ×X\x0000Ûß¥ß®F&ÄíöxµÝW\x001ff·Ó(\x0002ìV4\x0004.;49Z±Ø×l]­9ÌÇU4[[ì\x000eÒ&\x0011R7\x001a÷µÛÔv\x001b\x0016»\x000bK×æM(\x0013Ô£,Çûmk³-ÙåyÀÆ-\x001d¥ãÑâô¾v»ÚnÇaw°tñôò`VÆ½ý¨gÜ×n_ÛíYìN	\x001a6\x000cCË*Í82ã\x001d8¾w¨í\x000e\x001cvÇa\x0016ìÎ\x0002È):QûL²ÃÄÚîÈb·¦Ç;oI7,]\x0018©Ñsè9?ØîÍ»¯­&¹\x000f2Ü	\x000fÚ\x0000Ùpl3ÚôÝ±ö5¼
\x001cñÒ	qBv["Ã°Ð\x001dvÕxö5»#\:Y\x001e¹¼-ÏÖl¾÷(½Ö¾7ñRr\x0004L'\x00051¸ú$-5\x0005\x001dGõ}
o\x0002¦ä\x000e\x0001Ð;R\x001aÓÖR+ª\x001e{TÜ×ì&`Jé(\x0007ÓÊlòe£4\x0011SrLÐn¦¡\x001bÒ\x000eO\x000c\x001f­\x0013ìkx\x00132%GÌt*RûOî\x001cÇ·¬SÎbå}_Ã)9¦WÏX¶
\x0005M\x0017bÙ*\x000cI¡l¦ä\x000e^\x000b@ÄSÒFA¼\x000frt\x0012sOÃU\x00135\x0015KÔ\x0004½I¼=øâ:Épºô\x0000I\x001dáMÔT,QÓ¡FrÚâ\x00016
Øí Îs}]ùç)v·L°B¥bÈ©8Qø5F»öµ»%j\x0006IÌü!\x0005P+\x0012N+²[sÜ{T\x00135\x0015KÔL÷Lò\x0000+WÈ«&j*¨\x0019K\x0015%¨ÂTç¬+#¸]\x0001Î)7QS±DÍ°áÌÈ\x0003Ú\x0019JQ\x001a}èØ×ê&d*	%\x0008¼\x001e\x0007\x001d\x001a\x001eúÊ(ýèláëÆk\x000e\x0007\x000e4Î%ljWÆ
\x0019}#Þ×ðÆ\x0011j\x000eGèÓý\x0001[ÔaÆ\x001c{Ì\x000fäPà&q¸áCÑ\x001c\x000e\x0005®óróÅñ\Êé3dº9ã`z\x001fK¡\x0010øÎòNI-
wì½Sê\x0007
Ü-ôBqà	$L\x0001\x001e\x0011\x0007	Ýf¿tU¿'EÎmóçe1?%±xÍ\x000fÒsj49\x0018Mc~÷í
Ó·÷:Q|´Ô\x0014ímÉZ`¸|ªßí\x001dÅ´w [Ôô\ngrtzyïâç¶ùÇz\x000b|AHgJKº\x0015å\x0006í\x000fJÒÙrN?T¢§O¯Ï??ýüx?Óz¥±Y\x0018\x0004iCM\x0003À4\x0008æÔø\x0010êjqzuwýöêíåj7\x0006UcP|\x0018¤¡9Ú©Ø\x0003äÔ	çìnÐ)\x0018LÁ°aÑ#Ý8HHâë®*é.ðOÂàj\x000c\x0011&\x0002\x000b²ù|\x000bQÑSævrÞOÀ\x0010j\x000c\x000fCòEÂ ;A\x0008n$~Ü\x0017M°)³\x000fGZðaÐþ\x0004'µÊ\x0007²Axbâ\x000cË Ã[Ò\x0001ÜÒÙßîyx\x001cÞØ\x0001ÆÇûçûõë?æ\x0001±&åýS$\x0019\x001fqP e\x0012\x001a9ÜGæÏ~X½;¿\x001cÞÚ\x0001Íéêzµ¼ûÓn<ªÆ£¾}<ºÆ£¿}<¦Æc¸ñH\x001d±\x0002ºÐ<â\x0011ø,(e!v.\x001e[ã±ßîúDi[\x0000\x0003µ?\x0000õ÷÷/ ðáþñe¦oÓð$d[)\x001e\x001a\x0015:Iú¶éQt»\x000b$\x0010>x¿º\x0005é\x000f«ËÛ\x0011/G¨TJý» Ò5*ýï*Äf\x0007Â_ùqyåÃ±:ñ `<Tÿ¤ÖõÊsqÉ­=8ü\x001fX4ù
3\x0001+PQV\x0008LÅ^p\x001a00}"\x000e÷b¨\x0017Â\x000f§éïùàÝÓëgõºø\x0001åQv	Î§ÿúw¿¤ÿ?4ø\x000fÔä\x0008­õ4e\x0002¼»9£³Av9áÞ]Ý]\x0000¦»EW\x0016¥\x0001\x0012\x001a \x0019²
U-Òö¢\x0016
"R®%Ú(º©éT tU®W\x0005~áÅ\x0013ÁÆ\x0002\x0003LæßIh|ÀuQ]ç°\x0007|É[1	ô³ñêüþáþù9¥ÚÏO_¾<}¾{fÒ\x0002\x0018ä^ð\g<Î	b£d\x001eïÏW××)ã¾¾º¹¹ºXÝy\x0002Â£j<\x001brÔ\x0001/Õ8Þ\x001dh¸XùÑF9pt
GsÃ\x0001%Dã\x0004*j³ÁêL?\x0006ÍÅcj<\x001bO¡úN»Íàh!~
bì:\x0007­ñXn<¡(6;ïi\x0008ÍÑ\x0010 nìi~\x000e\x001cWÃqìÞÀRW3Èµ$.C\x0015F\x001fbçàñ5\x001eÏ\x0007\x0018zQ¯Á\x0001E&â	TÒIa¬®?\x0007O¨ñ\x0004vwà¨Ü%\x00008q§hf3å7Üpb
'r/áý¼:á\x0004é\ðtzô¨\x0002Â\x000c8UkhÜÐ82.?Ñ\x001a'"/\x0001D\x001fZ\x001eæÕmjÀ\x001b¤­¨x	KÁÇ¤7®Ïx?É\x001c@Mn Ù\x0003ç¨ÉÑ+ºÒA F\x0005úæài\x0003É\x001dX-K/(\x0005\x0006ö\x0019.Ð(è\x001c@Mv ÙÓ\x0003ï\x001bÞ¹J£\x001aSÁ=^@Mz ¹ó\x0003«\x000bÝ
z\x0012\x0015Ò4«Í¨Îì\x001c@M Ù3tí!\x0017ç\x0005Ñ\x000fiO\x0004PéæÀ!È&Cì)1eTHú\x00132<¦èüÙÑ9\x0014A²ç\x0008QR\x000bó\x0001Ñ!\!î+j¢ªbªÁÒ\x0019r.\x0012a vô>ª\x0005·ÛVí\x0015;\x000cYPÍx 
}0ôâ®F{eæài¼¶âöÚViÒvÑÀ}u\x0000$Kgµ\x001e¥$\x0003¨qrÛÉYxxÀ°*èj\x0014u\x0003ÁabÆÓ¸\x0004Åí\x0012lºuÓT°(TN\x0010Ô¹X\x0001éÆ%hn`.Ê¦)ñ!Ý1SD~Í¨8ë\x001c@KÐì.Á2×,MQ)²Âª\x0019}ô'4
E9W "Fß­7õ+O*RÐF¾û\x0002Þ`z\x0004\\x0002r2.K\x0003ÆÚÆ¨*YNÀõQ8ÝO,íîû/·ÏëÇÌ\x0007K\x0008 `"ÝáÝDË÷<\x0011ó­HÚôÇw¸XÝ,Þ^//3'@úg#¤\x0000\x0005ª(^ &§>	"Zí\x0004Ä\x0011\x0012Ù\x001dÓD×H4÷XUDjZ\x0012YÖ¤·¿f!±5\x0012Ë$\x0016$9\x001d\x0005$ª éeo3Ä\x0016	ü\x0013KºüÀ²\x0001|9M+\x0019¯@
 ;ð1\x000bk±8V,VÓciÊ\x00030«\x0016ÑXÄâmwö}\x0016\x0016ßbñ¬XÍsü	!1\x000c\x0011µ¥Ó¢»£}ó°\x0014fÍ\x000c\x0007\x001fè5Èóxã	Nwl{\x001b«"&º2øáhÞLß{3s#Ò\x0001Üz1
C³ñò×ûGþë//÷¯Ï3C>\x0008Ð#\x0011\x0007ér5TÐ-¶-?¬.!ê/onWw×»íWµýË~/h¦^i	ä^ý\x0006©°dú¹ç§Ú¯kû5ýA\x0018z\x0002ù\x000fL%}aÞ\x0017²û\x0014:Õ~SÛoØ¾¿¡[²2Ô"­½Ea\x0019»u¦©æÛÚ|ËõùSúnL!NGP\x0018]÷ávËüÖ!Ï}ó]m¾ãúú±^©RÃl¾O\x001e	¿¾ëÞé§~~_Ûï¹>¿§^Hie)õ 7´ï½Ôvªý¡¶?pÙ¯Cá+\x0016ÔÎÓ¯D\x0016êº\x0017Ü©öÇÚþÈe?Ô½¾Î)â[å­Rõ\x0013òöWo!÷Õó\x0000°jCÙ­QdQB8!E\x0013k*6ürÅß.ÀtRîì4Ü\x001euéTêzM\x0005ÐÄ_É\x0015C>M\x001f¨\x0004\x0017|Q½é¸Oµ¾¾+üF`¶±Ø¹£©â\x00115í\x001få»l¿S\x00014áWrÅß>;ª\x001eî\x0004RÅH\v	\x0016Sþ#\x0000,Ù"0ÔèÝ \x0010\x000fH2F±\x0001hB°äÁ)q£9xx~\x0017ù \x001aêR±û25\x0015@\x0013Ã$[\x0010\x0003\x0007\\x0000Go%\x0001Õª[Eh¾jBb\x000b\x0001A\x0012\x000côÛ`ûC\x0014º¡twÀmr
Ú\x0014a4\x0014~`J%,Á0J\x0013k_Ð4/,ø.b¾æaÍé\x001cüÀ´\x001a\x0018mºð£ZyEF¦[u¾\x0018[(,#
\x0018~F94Qt(÷VXÏ\x0017
Á2\x0006\~)bkzÊ,\x0002éáD[Ô$]:õ\x00165Wv$QÎ\x0016ÊÜ¤(\x0019-,Ñ+¿pÛg\x001b\x001fÖ"\x0010\x0019Ó¾¬\x0005	0,×±ÐÛÇB3\x001e\x000bUø0@qLåF¦@üÂuÞÓQl­fô´Ò\x0012\x001f-ÐwK¼ó\x000bRú\x0014ºKÿ;\x0015Ü^\x000cÉ·\x0018@NVr6¼E¹¥äh¹|Û«\x0011\x0019W#Ú\x0013³\x0011\x001dF:5`³#þqwÀj¤\x0005óg¾\x0014Pé\x0007( ¾ÿ¼þé~q¶þ\x0005\x000c]Ü<<?=~·Çø\x000c¨8¿_Ã½\x0002\x001d¦G\x000bùI\x000bâö`~\x0017ùï/g«ÅÙ\x0012È&Vóë«Ë¥p~«\x0008ì|Å8qyÿ|ÿåo÷\x000f¿ÌuPÑ\x0011ã$Ð\x0007gE\x0001#,½h+½q¹º^Ýü°:·\x001bª1(.\x000cVBW\x000b*ØyC?FFSä\x0005\x001f\x0006]cÐl\x0018ÒÇ)2¸a W\x001fÖÁúL\x0014;¨\x000e&`05\x0006óm®­1X¾uÐ)ñ 5hR\x00012\x0012þxìBÁ×\x0018<ã:¸"'.Fy+)Q¦^Ì(?Û4\x0008¡\x0010ø ¸MþC\x0016\x00180É§RyF\x0019>\x000c±Æ\x0010ù0¤t:WA\x0002\x0016£¤¦#mF\x001b#÷Ã ôÖ\x001b¡Òèéõå\x001egOï!Ì­þëa.	<ÑfêÓà"¨äi×\x0018s#J\x0010} Ww·+C>]A¸[½?\x001fc2!<ªÆ£Øñ\x0018¯H	@ñd9 \x0004ÈhvDºF¤¹\x0011EèñÄ\x0015J¡$×3­Bõ²Hô;óç"25"ÃH¡\x0017\x000b.D£â6\x001d<×ò®¾XÇ\D¶FdÙ\x0011dSÌk¤¨wÈªt¹Â5Òýé×¹\È\x001d\x0003Ñð\x0008\x0010I\x0010\x0008\x0001ÌÎ\x0005äk@\x0019K¿c\x0004\x00196\x001cC¿h6¢P#
ÜTZ]]0
§\x0012­ÓÂâ1²ý\x0004.¢X#ìk\x0004O¸é\x0006r¼FÈÃ
Î}d\x001b^¹ã+PZcT$Nò52W\x001d\x0001Q·ý{. &\x001aIîpv]Ìù\x001bì:zÜI».Ò¦ëßfæ"j|·ävÞN+IÎÛ¥;sÖ7µX\x0018>È¾¼éì\x001c¨®¾ä<hèüæM<#\x000bwxñ´)\x0001Ò¸÷TÚe*0±MK%2-U®Ç|ú¿ÿë/?IYËP"DÉ@µ\x0007ä\x001f\x0006'i\x001eÖ÷\x0013î\y³X^Ü¤?ìF k\x0004
\x000cñÄº@9äl¤j\x000c#\x0002[#°k N\x0002®vø¢b g P\x0018dBàk\x0004o
@Õ)ófJ\x0015±µ'­A,]6ù©\x0008b 2®\x0001
°)i$¶\x0016ª\x0018IÊw9p&\x0002íAæ;É2`<Ì¤YÏ^EGºC^uCüÞ\x0010ÞòEJS]uùøéù·-.î¹ÿ¼~ü4·´ê-uø@\x0019Æ`I¸®\x0006\x0016ñûÿòòÍur­«w«ôÇÝ@T
D1\x0002±"kVQ¯L®ÅHm\x000b	\x001a«ÅLÅ¡k\x001cuA¢.\x000f£ÀF\x000b2ÂÐÉVvT¢|*\x0010S\x00031ßîØ\x001aeÅ!"\x0006#b\x0017«\x0011^\x0011\x001f¥\x0013
ÄÕ@Ü·» ¾ÆáYqduQjiÊMõFÄ¸iibÄ\x0011k\x001cw=41ñXÓr"°
ÛJ¶\x00113Xá%P8ä}%ó½\x0010´'J¢\x0018\x000b
¤ñ¼ÓõZ\x0011\x000cI:©\x0008'E$eÕØHýT Ç¼.\x000bfeè½Ôaã+äÄY¥º³?S8»¥Ü~  ~}ÿp¼ßóÃãÌXè¢:!\x0015v¹vÆç\x0015£Ou×«ËÕâ=\ù®ÏGÞ®	®QhN\x0014 J¡ ÊÁp;¾]óA05\x0004Ã	!¥º\x001e\x001cÓý5c(R¬J3LDak\x0014\x0013ñ¹:s]äÖ²¡ì'3ÊÒ2\x0011«a8Öýä©Ï	^áIÚ*ýÑ\x0012«ák\x0018\x0013öe?¥XH¿`}yÄ¶ýât\x0018¡\x0011XWC¾²¢HÑÒ\x00131N\2\x0011F¬aDÖÕ(d\x0018N:b÷°xçcôµq\x001bA<8l\x00116rBÑÄ¢ìÔÓLÄ!\x001b\x001c\x00134{æ£ÉEÐµ+ý±|¾J6\x0011\²píèxÀt¤}Uu7\x001dNÄÑÄpÉ\x001aÄØÌQHâ\x001bõw\x0015GÅí&Âhâ¸d
äÊB\x0017`ÞV~£ÝlUIÖ\x0019G\x0013É%g(·!\x0012\x0019Ñ\x0010\x000e\x0011(\x000créÿ$\x001f&KÖXî\x0019t<$:V«ËcèNxÍÀÑÄrÉ\x0019Ì¡ÿpøÂ\x0017g"í«~A}\x0006&KÖ`.Ðå\x001aOýãV¼*ôl§h"¹ä\x000cåÖ\x001b\x001aû5R6Á\x00115\ÿm`:\x000eÕrÅ\x001aÊa¼\x0002Ï¸5'\x001e×CÂ[\x001c¥*£½Är@\x001buá+wö\x0004# $}Ñ­ó
ÕD@Å\x0019\x0001a\x0016aFÁ\x0017ú-R^\x001eg&£q¹ÓåBEÄ\x0011W§%®Nè©%WÅ¯«ÆU)NW\x0005Ê$xÁH\\x000e\x0013éN®Ç\x0005Ó§áÐÍ)×§Ü¦ðíðZÈá}!²\x001c­UMÄÑrÍzÊeQ\x0000Ö\x0017$[0®³F0ÞÊu!jÎ\x000cÑ@36
g§õ@ºû`I¦\3&º9åó\x001b_T\x0015BÊyIU¡;\x0002N>\x001cÍ1×Ç<] 2\x0008\x001dÿEk"·71­2Í\x00197gÜ$k1[\x000f)ç\x000eL`¨¥³á\x00193\x0012©6óx]sÖ\x0010SRB÷YATÀÜFU«Q\x0012Ê©¥Ðº¹*CV\x0007
\x0004@$Ô\x0004E¬Ú£\x0013\x000cSÈ6\x0014HXá\x00007?RîZVa=
W\x0010¹
%}1Þ\x0011¡\¨t$Þ\x0003«Kò\x001b$ß>k5Þ14ò®Ì\x001f\x001a\x001dÝïà8^8ÆÅ\x0013òË\x0016G\x001bR\x001f·¡6'¶õD&ÖÃÁ³¿­?fûf\x0000Ð0 åE\x0013\x001dÒ«tíuD!0z×}³Zý°<¿î´_×ök.û¥¤)i\x0013-éF»\x0008Pi2ojó
ùÑSµÝDEn\x001dó¢08ø]²×{Ûïjû\x001dýÆ¤\x0018È=å\x0016\x000cå
1\x0011Ô¬¹¾}ó\x001aÐQ>\x001cF(Ú4éþ/i 9NÛÈ>AíaþC¹9ÅôCu?¯\x0017gO¯Ïõë?\x0016ï_\x0002¯4/h¤\x001c2-ký@>6ô$J\x000c\x001b6¨]bä\x0017ËÅÙÕÝõby÷§Åû»3pS{À³5<{TxQc;\x0007\x0005\x0017\x0013J8§\x001bmc0o¹\x0014MZ7\x000c·Ò¸ÿº8}zø²øñéóÃÌM.%ù, AAu\x0008)JbÓ~Ô¦Kp½íwÓ«óÅW\x0017ç»q¨\x001aâÄa\x0007¾\x0001õø\x00083}
qô\x001f×gÀÐ5\x000cýÍÂ°5\x000cûÍÁHöp¤\x001fw{] øëoÿgq»ji\x0007Ã>q.ò\x001a#=ÝPb±i8íw\x000bT~].n£\x0004\x0016Û:©®è¤²\x0001	ÈªLºÌ{@P±E73MFbj$\x0015÷\x0012G¥¡
9\x00001Òà\x00158Z=\x001ac¦"q5\x0012ÇD+Z\x0013`ýÖyB;jÂª?¾;\x0007J¨¡\x0004V(.J| N¡ÐC¥~",^Jâ¸êÇd(±\x0012yO3¨H\x0007\x001dYØ§¥¬\x0011¡Ñ´lò¡o\x0008_RL&DJ qJ:'\x000eþ8\x001c@
n1xÅÑÛ<<Ú7ÉÊÅú×§dH !ó\x0001Ø`s9R\x000ejèCL±¾KTÊÅòÃÕù\x0018©ÞfáÑ¾IS\x000eC\x0000¡Ð
\x0008à\x0019(\x0014µz\x0008LÿIq*\x0002]#Ðkp\x0003ôiåÙoö\x0017!ðýy©\x0008LÀð!Ð(N\x0012RÌÀKWZ\x0003\x0008\x000b­\x0011X>\x0004.ë1¦]\x0004Úk¸\x0004
S+kû7©\x0000\
Àñ\x0001\x0010'Næä0D\x0018GÍK@¹¡\x000b;F¹÷\x0007àk\x0000\x000f@È-°i\x0005G\x0000G·£\x001d' Ö\x0008"\x001b\x0002\x0010ò\x000c\x0019$eÀ!\x0002ã\x001d×)m4à\x000b\x0007>3ó¦s¬\x0005²%\x0004\x0001ï­fD7v*ÆJ>g
\x00084º¢xBkõ	Ò9ýbÉT\x0004'®(äñM8É\x0016Uxà H:ÊÝ1Ú} `I'£L?ÀQ>ûÛý/)1Êeï\x001e_Ö\x000f÷Óõóóý\#e¡\x001e7\x0014²\x000c¨\x0012ãË\x0014ÑVÛô?Ú;\x001eg?¬Þ¥L)\x0017z¾¿º¼]_®\x0016§ËëëUÃ0£ò»,ý\x0000¹\x0013Á|]ÀÜðÃÓËaÈ4¼\x001däþä¥L2Ré¿/´P\x001bîE\x000fBv·ùáó«ÛÝ`T
F}ã`t
Fã`L
Æ|Ë`Òa\x00145áïìx´'Âh+­9É)KÈQ\x000cò¤ûãù\x001cNç/ý\x001d¢¿òC
\x0001'`¬t\x0016óÈ¨ñõ\x0001z
\x000e[¢\x001coÄ¶>(\x000f\x0010?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=zsúiÚÓr»&©Ã·ÐH{6È.Å9sh|®Èï5#Ú]ËVýúèÍí\x0013àêíÈn¿ éMäªûè^õb^ãÿÕÓ+\x0010¾S_×îF(mÕOx\x0018LJ®JtØéé±²u\x0015í«VÛ&0]é\x00160«pâ\x0000­¹ÅÄí¦kÛ¸LÉe¸ÐO\x001fÒ³\x0004Ñjû!UßqçÉXlÀþî·Üÿö\x001enÎo¿ÞÝ¾êz¸PÜÈ%ù\x001ceöj[_áá²ïNÏO/Nq\øÙéè»\x0002Qº\x001d\x0011Í\x0011òÒá|\x0007v2±¤«\x000bÏz\x0010mhÛ\x0011·M\x000cF4ÏH®iJ³©ù|øQ>úø\x001fÏHi9ü\x000b@N^R\x000bt\x0003
Èùajöí×oî7ßü°¹¿ÿí\x001f·ß|ûø\x0013Ì\x0001Ï\x0002Nv2\x000eÀi¬7)âe°´1\x000f(»\x0007\x0012î\x0013`<=ú\x0016þèòâ\x000f8\x0016\x001emºð>ìDè\x000f
ÇãüñÏ§¶îÙÐ8Ò^%hl®\x001e&UzccZ¢jÀ9×r
Ã\x001fÞ\½\x001bkN/éUI¯\x0016Ò!cÞµå³©F	è£Y\x0017^ðz!¼£1eð\x000f\x001b\x0016y\x0002¼IOß.8\\x0007Þðf\x0019¼\x0012ÃêÑ\x0001\x001e¬ñ¡_
~àjò¶·ÃÛ\x0012Þ.<y \x000etò6¤B28yÏ\x0007\x001fÝÊ'\x001fJø°ðä]\x001a\x0006ÿ,üñéàC>ø4i`9üg\x0011]%nÞÀ\x001f ¸yÿôøü<DbÞ=m~\x001eö7Ì\x0007;!&-eº!\x0015û4È\x0006éôðï¯.onXÍ»«÷#Þ\x0012^ðj!<NÃó	>ú4¶\x0014àErî\x0000>n\x0017ô­B\x00061=\x000e\x0002[/\x0002­¹\x0007|CÓ<\x0018\x001e©Ô\x000eðS?çrüºþ\x0000oÎv\x0001\x0008îÐx|xÞüüÐt÷Á\x0006ÉÚÊ¸äyt,,L7)v¶Ë@p©ÆåÅÍÉû±òw¨òw¨5~\x0007î\x0017¢7ì+\x000e?CKÏoØN^¤Î¡Ë¡ÿ\x000c\x000bLékÀ\x000fòI\x0014é`²\x000ePê¿ágØògØ\x0015~\x00066\x0014\x000e¥×hpª´¼Ð\x001b¥"nÑI3¢õw>\x0005ýA«\x0007ø\x0011 \x001b®R¤
BøÑM\x001fÁÒ\x0005x\x0012^NÂ¿¿:¹\x0000rP\x000bUI¬:uÄÄ\x0001Ý~\x001c\x0000nõl³\x0019?©}[u	¬{XJèþ·e[\x0007þ^²\x001cìZÄ¦$6ÝG\x001c(®GL\x0007\x001c#\x001f°~-¸¶ÄµÝ\x0007¬m6ãAÇF2ãEêèEb\x0019Ö"v%±ë~uRn¯LIr^)+"p\x0001×"ö%±ï>c^^^\x001d±ÌrÂ¸\x0003¦×|âP\x0012î3V>åsð5É	laà#ö\x0007¬­ùÀ±\x0004½À*(>b
>éÀö!ü×q-b)*å!ºÏ\x0018\x000b© p¸ç#Y"[\x0017TµD¬Õ]·¾Ã5¸ÃìS²4\x001a\x000e\x0019ìp³èi¿\x0005¹Òw²Wá
V«Ñù"lµnoòZOOV\x001aOv«<ì¯"\x001díÀªtÊ%²\x000fâ¯0\x001f¹Ry²Wç¥aÖ¤ó¤`lá»lÍjw¹R"²[Hì*$0²/\x000fÖ\x0004\x000b\x000c=\x001dEiA®d²ì\x0016Ê\x0012+\x0015èbXF\x001aQl!\x001fãZOU2NuË8ÜQ\x0010uáIO\x0018d³l\x000céµD²ª­ãni¡\x0005Ç¸ÔÜ\x0005ÄTçz=äêR¨îK+¬HÀ
ý	¤÷,Ë7)×²uu't÷À¥ß>i\x0011QdÒ\x0007ËâÍµd®®î¾\x0016ØëN\x000foèâ$ã"(\x0015`q¬å6éJ"ën\x000c>\x001d\x001bÉ\x0016\x000e9	äHCò0\x0019W»\x0016@ÖÝ\x0002Yû2L¸cÅ¦y\x0019LÓR\x0001y=OOºÔWhÏÿ\x000cj«
UÒ«MhÐ0Ê:6\x0005¡61Y:ûÕÈ]j8,Î{Óí®ªTAç­Ñ~N9³´¿e°óç>Å×ÕÀ5ò\x001dä/ÝW$¤\x001a\D\x001ez'\x0013r\x000ea(?×\x001bAv»!_WT¿#Òíí\x0011\x0011µ\x00042\x0014
ËÆèL}\x0019\x001e\x000bN92à¦#¥©B½þ³ñâvã¤®¨ïþ
!FVèÃ(ú¤k\x00145\x001f\x000f\x0019\x0015U;ßÁæ¦÷ëÍÝÃó7\x001fïnnnÓÀ\x0005ZÿÜ\x0014\x000e\x000b,n0õg)zíã°ïô]Â\x000cÔõÉÙÅÍÑÇ³Ó««Ó£Ó\x001aÊ¦Ê¦ÖýipÇ8\x001a|Z{TEþiÓIü¥?M?M¯ûÓåÔI=:'YID3\x001dNYúÓlùÓìº?
Cà!ý4Ã"\x00178â\x000f'D»~\x0018u"m¯£ðE=ÃÛ§
üã·©D½!­NKá\x001fö4Ü\x0008ÓêYTL:WÛ}{uryqq:ZÄ^ÒÞ,¥e(b§#ù\x0001¶Æ\x001a\x001e5²
¾ÜÍÌUC¥ß>=>ßýüð×¶(e7\x0011ËwHÕXL§S\x0001S	óöêòæìýÅ¿°Ç\x001f7~ùë_$ÑÙÄ£«Û¯·O~¼\x001b* (Ä\x0017\x0013÷_\x0007ì¡ã\x0001h\x0001ÑÛd[ l²´\x0015¸\x0016\x001ahÔÎä0Ø¿
°CS\x0003§ª>\x001d]^^ýpy6V\x0016UÂÿ)Ó\x000bêhS4â,@C°\x0006 Þõ@A:»nP{L\x0007ê\x0004:35Ö«aUßzðC7§dÎH¥ÀjWÔP\x0010¿\x0010óñËýz&+\x0002móÛ¢So\x001aN¨*¹ôÂ¥,
¾kÆ+B\x0005ÞùédçGs¸\IP´\x0012~ûrôÓýý?O¾\x001c¦Ä½cî¤¶é©kðþÊ;\x0019Õ¾ÇCmBß~:zwtrõö0¬*aU/l\x0018¦7\x0001+VÚÄêòC\x000frß¶³Õô²ºT\x0015\x0007;Ì@I°VóÁÚu\x000eÖ°®\x0017Ö$»\x001c`­NÍ\x0008Ë\x000f^\x0004¹
k(YC'«LåÍøèAñ\x0003jH½ôøê÷ÉÐ\x0006Ôª`'ýAÝÒö\x000cªóÏÀóxX\x0008\x0004ÃXVp|p9È0gF\x000fkMVb\x001bø\x0018íÐät\x0003Ò
ÿlÔÏ)uI¬»ÓlëÛÕõ0\x0016*\x0011{áÕjÈ¦D6ÝÈ^£Ö\x001f±"Ð&ä\x0016¯\x0001²ÜB-F¶%²íFVbÈÐ 2&tBV)²
÷"õ(¯ìJd×l$6¹\x000e÷B\x000c-x\x0019\x0006\x000e®\x0003ìK`ß
¹}"\x0006s+ÙZÔ \x0001gìÍzÈ¡D\x000e½È`)\x000cJ\x0003A$'¥¡¥¥·çXï"Ç8v\x0013\x000734Á\x000cÄ6eÍØ§î\x001cD^í\x0019D²èEÆ21Þ3"
Í×ZX\x0016ÉB¯&e­EºÕ\x0004\x0007Ø%â\x0018H=ã6\x0004F¶vÔðiFV\x0015²ê>e°#lº\x0018è
aÉ|1¬ßk÷1WªOvë>i%N±\x0018C*ÇcÖY`õ¬TìÖ}B
#¥\x0010y¨\x00011é­§«\x00017#®Æ\é>Ù­ü\x0004FéjhCWC\x000b'H_ãÌÕ+å'{µ!ùIxÎè\x0013\x000frN\x0018HÿÙÔ2¼\x000es¥ÿd·\x0002\x0004A
á\x0003s\x0014ä/)°ømXïnT
Pöj@\x001dÁ	%}b¡Ø\x0003öó}a=±Q©@Ù«\x0003uMf(:gi\x0002ß
·ÚÝP\x0012T½JPG\x0002ÅÃ9G\x0016ÏÃ´ÜÄ¬Ö¸Ïv×²E&\x000c /n_\x0000é¯>'\x0004ÇøÀvN\x0013ÿ´>ÞÏ\x001eÚ!]\x0004¼\x0017§à\x000fÆ\x0003u30ê\x001eRî)ZRb\x0014JË½²­Ô¤¦ëLµL¥*x¦!%ãàL½bT±?BÑjKTÛjB
j\x0014EN
¸NPå^­Ô¤®ïóëT6\x0001¤ªHñó\x000bú)+÷:vÍ¨¾Dõ]ê©\x0001Màd:\x000e§EÓ¡®sScI\x001aûH\x0015\x0007Î
¯§\x0007R\x0002ÞT³Ê¡\x0016\x001e%\x000f£Õ©¶¢S
ÕHOuo,­µ\x0016ª]R\x0015\x0017tÉ\x0014¢\x0006Û\x00177\x001c\x000c¬üªdÜ8iGU\x0015ªêBÕ>ÍN
@Ñe\x0015ù\x0006uP+±*»ä*òí©\x0006
S\x0007OuËZ	+Ù%­\x000c¦¿IYI\x0011\x0002*ÁFV¹Îe
\x0015kèaÕÑ¤\x0001/àî\x0013ì\x0012ªI½Rêã*&ªdê\x0001¸®\x0000\x0018´©,\x0004XµÌº?HÝÌZ=,Õõ°pùTðÄ*X^\x0005éX\x0008ì\x000f÷ÎG»É*iG71\x001f0Xpdbº­\x0016w$Ýª,_\x0001]t\x001a½¶Y§\x0017é¨ªD\x001d[Ï|\x0000Õk,L¨65w\x0003ª2£ff¡ÝS5¯§\x001e]ÌË¢jÁÚÕòîÕVã§ÊSF.¦²¨V´ªÖ`Ý&Z6°@¿jº¯«X	W¸º\x000fW\`½\x001b
\x0007I\x0010vÔ\x0003o5%¬é<[\x0015SÝ\x0007-$ÀõPùéý¶K\x0007®+q]'®L~7]\x0005KYKoòáªµN7¸¡ó*8*;C\x0010Ò¨>À\x0015l\x0018h\x001bGÃ^¸±Ä¸8\x000eÇeiKF··9ÛnÇ\x0013m¸e`¿Ú~×Æ\x000b\x0016¢æ2 
\x0016
Æ°\x000c(L$Üx+9&;\x0005\x0016\x0004\x0007\x0017Ù¦Ê\x000b¯3¯_~{ÕnüE
ñ³_~Ý|ý:\x0014ð\x0002Ïæé§9ö·\x0019Bãx\x001b¬9vìo\x000e\x0016h\x0019÷îÙ'××Ca\x0018üÏ'Wï\x000eÃª\x0012VuÂÆüÒH\x0005\x0008\x001b\x0019Vø}r¬\x0003V°º\x000fV¦4%ÚàØäD\x0005
\x000b\x001apÛ:°¦5}°¸lN\x0016¸%W_Dª\x0014Qa¯\x001fÖ\x0001kKXÛy
lªGØF¤à50a÷Æe;`]	ëú`q\x0016º\x00068µÜ\x0010¬\x0012|²q¯\x0019Ö\x0001ëKXß	kÙÅ\x0005\x000b'ÃÊÀÅMb¯Ó\x0001\x001bJØÐ-
\x001c)2+Óp1ÍV.¾\x0006zWt¥yn<\x001fôëÑ÷8Ûêáë\x001cwÌb#W
RÕÒ\x0006÷e yXèõÑ÷8ÈêbdcjJTÓ
z êm%VbõÑæB¬}r«Õ¬®óX]ê®Âc\x001dê2Ó¹2kÑÌÖÉ*w¯¬Æ¾Ý|Þ<Ý>Ï@µX.ÎoK\x001dS\x0000\x0019Wl\x001c£68¾=ysruz3E*v]Ç´ås;;èÍÓíÃáÈÁ0L^S}M\x0010Ç!¥qµÕ\\x0012¤önG\x0004½¹:-Ãw\x0001u	¨Oj÷\x0004«U\x001eï_Ò:¼C¯Ç#Q*¹èÇ¤×Ã·F\x0016}:z?ÚåWàé\x0012O·âùÈºÓ\x0001©á\x0007\x0013øÅ±\x000fñù\x001fÍËÏòåe\x0008_Á/Ä¿¾½}úe°\=~ùÓí\x001f\x001fpEªöÏÿáòëóí=R\x0019\x0011tªôÊøà\x0015jrB¤JÎÿõÍéù\x001f¾=½ú0S®.á~{y5² \x0015~
¿<¦­\x0019ðfñ¯Ìôþöé~óòýD:FCkÜ\x0003!Z+lÚð\x0006V³N3§j¢÷§Wç'þu\x000e\x000f|8ük68Î\x000eypFß0»Öâ¦ÔÝ¨~Áf\x001eñù/·?}\x0019¾\x0019üoã_8\x0016öÛÇç»Ûçça8ì¾\x000f&\x0005Ñ¤þPìÚNÛ)\x0013<É¥Ùþ	\x0007ç¾~{yqsvqzs361\x001chÂüú¿¿þe8\x001dø_Æ¿òé|ûxûË¯O)F·÷
	\x001a[Dàm±V:\x001e¸e(\Î·ç§\x001f>^\x0007äü·ÿõË\y\x000e}'l÷é;EK»ä­p)O\x001b\x001cìö`øóì\x001f[ýÛéº\x001cú·+GóVáÄ4#\x001aþíÔ@õ{qö¿ü\x0017{÷Ó_ÿV¾çÃÏØkL\x000cÏ\x0018Ëð\x0015\\x001eù'bª\x0019\x001cþíÛ·;öï·ïþÛÐµ#ð¯ó´\x0010eóóØ%Pä^Z\x001f9\x0003ÍÒ5ÐBÄPÜÊA¶äEÃÿÏ\x000f£ö­|ö­¶ËÌÞ\x0008FRÚQl¢ï8FGQÑÔu:¼¿ìýôk­Ý\x0012Ý¹P¥¬Å28OGæaýP\x0014<!¨¢¾ð\x0010\x0015®ò!ÏáQ2QEÍýÏÞ~ªêûÉù\x001fÐ!¨\ª4p\x0000>¥0Ü\x0000ïÄ³ª> løZÐlY!}¾`ºA:Ý\x0001%ËhRúrçî¶]u/\x0013vDj\x001aÍ =íwv>Ü¿îv¾ß¡ÎÓILj6\x0013¼¿<ÃT¬Ó¿¸\x001b\x001c¯ØÍ¤K&ÝpN!­µMç4´à¤<OÏ
ËúLÉdæ3	2oX¥h¡\x0003£:ÏøÓýL¶d²ó\x001cÏðµÎècáÒ9¹<0#ÄþûäJ&7	d8KN\x001cjèÛåñfNõß'_2ùùLæs»®è2Eu\x0011£ïæ	%Oø}¼¹X2ÅÙL\x001a/5Ïþ\x00031îR.O\x0012\x000fÝç$+9 ç\x000b\x0002­Ô1\x0019«ÎS[\x0013í2¬eÿÇÕ£ó_ÖÛÅ\x001d]ºáÑéÀ¶ëª^lxvQ\x001dë<¼Â(á[îL7Sõêäüg§­Æz4ÏÇ¦\x001a\x0010ø»ày4^\x0000U==9ÿíiáSÜ\x0016O*w\x0008ÿÎC\x0015ìªÞlx|hç	½ÙXz;£yØ.\x0010
oÏgcÓK¬=\x001d\x000eÊJf¦[¹¨ÊRó-¨¡KV58rÚ¼°TjiÏ¤¢\x0002¨¶æO\x0014\x000c<grØpÌÌÈ×ÉN¢Jfªù2Ó\x0010ÈräßÃ\x0011ñ8*\x0010\x0004Ý÷[U¶o<iºH^¨´½
ÿe¸Qý@\x000cWóe¸16\x001dR\x0005>=ìã\x0017ÜíJ«ù"\x001c7VÆb0¬ML#3&uwAU2\ÍáðqÒÆ6|q\x0011gí\x000eP?^ÔÝ"\U"\Í\x0017áÆJ%ö>ì\x0006+\x0005\x001d½í6T%ÂÕ|\x0011nÀ*ðtP:pô,Od\x0004Ð}Íu%.u¸´2-
F¨Ê\x0005ñ¤tòtß(]ILÝ 1c\x001e2í½IÕkÀD-YÈä\7Típ6\x0008Í ØkñÞ¥Ê\x0019ri­-BnïNWRSÏVú\x001c¢\x000bTóïÈúÕBún³@WS7HÎhxÕS"
ÅâÉ£Zè\x0005'UN=_tb\x0006g\x0005\x0011X\x000b+£3T¿I®+Ñ©çN+H¥¡2øíÒ<\x0011$ý·¼\x0012z¾à´(Ái4\x001aºéIp*¯\x0018ÊîFê\x001a *Á©ç\x000bN\l\x001eiß¢cÒ©U\x0004úõØN'Í\x001ezÞÍü?ì¤Ë]4Ù¦àáW\x000cæ'ùU>D\x000e¸\x00065ú\x0004GlÎ*!þ \úvóôt÷Ûÿy\x001aÏré )ÈÛ¶É\x000cV£cQì 
ú««³Ó«4W\x0006S%j\x0002\x0003elÉ¡I8IÛ±\x000f*w}Ð60]é&°¨yN¡SÒ_`î±]\x001cp\x0015×\x00022S¶#[\x0017ÙQXÑÃ{b\x0017BÝ4C\x0013+É\ë	\x000e kV>ÂjØõ%fÉÝkVµ=|{w¿\x0019æ\x001cáü\x0007®!³t÷·Ë\x000fÃ®Ý~zôíÙùÉè|³\x0002H@z.\x0010&äÙnp\x001c\@°\x001bvUô| S\x0002¹@AcÃ*¯L²ì\x0001f/14\x0000}\x0016AWNÄ\x001b0£\x00131¤>o_þK)~\x001aÁ\x0012ÁxiÞª\x000cO1XºL6\x0014\x0011Ï!\x0005zúé_s%ÅX-\\x0016+´ø»@Ó²r(Þàß\x000eå\x0003¸{÷ôáèãdåi ²XZræ¸¥1\x000eÈÂrÿö\x0012wî^\x001c¥ªý©k÷ãÝ||Ò¤|ñt:ð/\x0007A3 8@¸ÿë7o\x001f_ï\x0006\x0012i¼\x0008\x0000
p8¢dÔ¤15NèüßÞ^~ºº9:IG4r<\x0015L\x001aÆù;Áß\x000b\x000cþ/ã_sià½§àÆ	TÃV@ Q4hX*´4Ñüñ×_ìsñÞþt\x0014å\x0011þÛ§q\x001c\x0018$´éA9pØpÂ1!)\'²G\à¼}7ü\x001f¿\x001emñ+°Y\x0014ÿOdE2\x0014üí±\x0019x4ïoÅÛº\x0007\x0014«,\x000cºô\x0007ÕØëÇ»¯_\x001fSÝè8\x001dpX\x001a-U	Ï,\x0001\x001dLµî%^î¼¾<»¾¾\x001c­\x0018-(UI©Ú)	ëXB2´ï)\x0013lê\x0002Lo×ÀÔ%¦nÇ1G1\x0014\x0014\x000ev»Ê\x0005OxTð´\x000cÓ¶\x0003\x001372Ò7Ç}¤.ad2\x0003¦2¯îd\x0007¦/1}\x0007¦ò4\x001c[bn0\x000eß<¦]Ôêë%dì¸h¥Út3µ\x001c*ábT\x0005Ê Vøâ²º²ýfz\x001f¨\x0001GÉ M*áQÆ´×Ñz»Â'ÕÍíWÓ²Hf\x0011X°6å6\x0000ÓÐiÚhì
ÕÅí7Ó{\x001c)\x001ePð\x001497\x0013ù«;¹8ÕÝí\x0013üô|\x0002î"Hz\x0017\x0000R«\x0015 U¥T»\x0006ò¤MÛ@eD3Év-#Évgä
\x000f]UOHu<!6P\x000f(ôµ\x000cs5Î³zBªã		D.´\x001cÖ©$\x0012Ó½¶8:8«G¤:\x001e\x0013¶\x0007íêÓ\x0008\x0011\x001cÍ+ù\x0011¹°ì»|é\x000fêÍ(\x001f6\x0000ópÀz³}\x001ctL§©p1i²ß¤\x0008¯ìÉí\x000f'ð\x0007c>n\x0001©JHÕ\x000ci\x001cµª)E`\x0008é<UØÜ2°\x0008Rº\x001d\x0012,"O'©uâ\x0008\x0019¥-Û\x0019MÉhÚ\x0019"5©p\x0018ÏP¦\x0001&C*
Ù-´%¤mÔRY
ûj]ºjÁ¤ñ¯ßM3£+\x0019];#H\x001e\x0011ù[«4\x001cf`\áB1´3
nOÀñøÝ\x0011ÒFI®\x0019ð/%dì\x001cTb¤\x000eBRµ%@î10[!©M¤h¦ÄN*Mog:«a±
ï\x0015 kIÞ.Ê5j$%5\x0018DÉ\x0006ÆÕ*rwÖLYrÙ.Ë±¦NðÓñ©"\x0012(b\x0011$ôk3£²å²]k¬¸'\x0019$t¾ÚòYî	k´SVÒ\¶sK)T¢\x0004+·\x0015,*¥YáWÒ\¶sl1öt>unã÷¶|k0VÒ\¶sJ¬Á\x0003©r	þ\x0016ü
:H\x0017ëÒ/Û¡6}n71}nÅOÇÄL	ÎÏrÊJ Ëv®µ¤:le¼\x0018¦%!$íû\x0006p/T¬T\x001d²R¥­CÃkaÒ\x0004AªQ\x0006±ü{«J\x0008©\x000e!$\x001d\x0005P>\x000bÊ±^¹¡*!¤:\x0008,*­	©¯\x0004(\x001duÏÂÿ²8L³+c\x0014RíRHåÐ¥\x001aVxÑ\x00177¬Á¹\x0016bÑQV\x000f\µ?ppiøé ÷H\x0016áÍÓbX²¹RWoG·¿\x001d=Ú\x0013aSv\x001di\x0001z:{\x001cÛv1\x0017d·\x000bLZX½¢\x001a\x00055\x000c\x001dNÒ\x0008<oFj\x0005©Ì+VÓ\x0003«\x0005¯k\x001e^\x0012Á\x001a§¶/i\x0005Ñi_ÁÚ\x001eX½ûI¯Û2©x\x001f8ícÝ\x0012o·5þà\x000fUéÇ§Ç/·_¿Þ=\x001e¾\x0000ñ¾0ÙïªÓ{Ã\x001b©òãÕåÛÓëë³Ñùè\x0005«)YM'« bW\x0010ò.îÃËÊ¡\x0018ëöJí¬®du}¬Öf\x0003Ù:6cÕ¤÷;éí¬¡d
}¬\x000bôÔð·,°¨\x0011`÷û
°¶,?KP\x000cHýasÿË¡4*Î	ìq¸ãä¼ñä;´÷ú\x001bïMÊ\x001f&\x0013©»oÉoi\x0016\x001aNJÞ/c¡{ég\x001fk»át	§Ûàpì}CXÂ\x0017 \x0002EÉ\x000eß\x0013^o³%mKmQJÛ|ó<÷·\x000e±åEl¾dó_U\x001d\x0013¢\x0005ÊøQYÙu¹ð£Æ-6²\x0019Úï\x000e7n\x0018bà\x001cTiöjÂ\x001bWkA¼u¹~uî·õ©.Sa¦¡/f)\x000e_v¯©6Pï\x0006ö5\x0007ö±ÂéÝËÓæá§C\x0012Or	x\x000e\x0012rx¼üWàrº=tXðôîÓÕÉÅX\x0001V§J<ÕU\x0014©²Â§M ð·ê3ÁýÚ oÃÓ%nÅ³üjÑ| §aÌ8î3\x001aZðLgÚO/RDÅ\x0019ÌÎ§Óüq÷$Ûè\Iç\x001aé°TB)V§nuô¹XäIm\x001e/ñ|#wYÍZ\x000b¤6g@Â>ÉÒ\x0017K¼Øõ*ôm
ÍAo?­Ú\x001b²G§vÅª
ªp\x0012ÔíÃã\x0001±çUÈ·Oú@%\x000c:\x0008N¿°ÇJå´&N:½¸~jW¼¨ª¢j\x001e¦ÃÉ\x0012ÊÒô0'¹ÒRs|ýÛ1u©Û1½c%bpôp`ê±wê÷x§í¶´í
\x000eÑÏIV\x0007McC\x0004®ËYÑ¾Ñ´Y\x0002GÛ<v¤i\x0002\x0003*+`Æ\x00123v`jIµ­é³)íØÃßSÚÚN)«[);®%\x0006E
\x0007¢4»Í^\x000bÇ(±ÂGÕÅ\x001d7Ó\x0004É^(.¨$§I°Ó¤ükUÓNY]MÙq7\x0007=¨·a=ò?\x001dÛ\x0013Û}qVwSv\NíötÒ\x001c\x001bÎjç7ôÚfl¦TþQí
Èá¶ûTÂ\x000f!
ÝDÙÄY\x0010M+¦ªÞêxC3¦z\x0010'i³\x0001\x001aB¹a·®ª7¤:ÞÆp¸§\x0002nÉ\x0002Þ\x001a~&°'i\x0005Îê\x0015©WÃV98\x000e\x0013Ç1§\x001b¯ûÏY½"Õñ´æs\x001c',\x001dËø\x0010VºzGºã\x001da´95g\x0003§ÉÙ¥\g£Â\x0000@\x0003§Úuc(Bbr DZ(£Q<ÊËr.QGîýN6ÿ\x0007ùTÉ§\x001aùvôÆ%:²TÏ\x001bt*¹ÐQýõT-º\x0004Ô­Ñ¤:%ðY#Õ­(Ó\x0002gp$ÝþÂ¹\x0016>Sòf>?¬ä\x001d:
lê2Ç\x000f¬¸¾\ê±èÝl@[\x0002ÚfÀº[¤5iõÏG
\x000fZî)+oÄs%kÅ\x000b&TÉAØ8úÀêÞuØ\x001b\x000ch\x0002ô% o~Á\x0001­´Tþa¢Î\x000fÄ/~Á±äÍß7ò÷\x0007¬ùþü~Ç¢xsñÚ3Um¼Ë'òù\x0005ÁÕÎQ*ªr×fvn$¬Et«\x00166K\x0003GhR:È@Ç-VÊï¯Rh!¬´lÒà\x0010\x0012 \x0013iÇ\x0001\x001e¡¥;¨Õþ\x0012ç\x0016ÀJHËF)í#$!5"]Z«÷ÜÊ\x0000&ÃÒW,+1-å´wi\x0017\x001eÊA.ò0!²Ör«ÕHXÉiÙ(¨}ô\x0002{Ò*K]£Cß\:ÂèÇR-³\x0001+I-ÛEuîñÃ<µ(E\x0011%\x0013ê¥ÅTlp\x0015YßÍ%Í+LÓÎ1eË	,^²ddÛFåªo\x0017Ô÷'\x000f K¦ù<]Ö1£¹¬\x0019»]²JËÁæCf§exß ½1ù}¿R¼\§\x0005T ª\x0007Ôù´î\x0018AM\x001a:¢¬Àæ
\x0002]Sº\x0013ç¯ûl8r«¬²1[«Ú\x0012ÔöòrK\x0004¥¥Ì\x0000J»8\x0011T¾zFM r×\x000f,&ÿ×ßÿóäþëæËí7çOO»\x0003ÝøÎá@Jl\x001aË¡´agrZyëÁîc::9¿>y{zt~yuurv1Þ¿3U70è"ê¯²Vs´*Dkºö\x0017 u\x0000ë\x0012Xw\x0003\x000bq¬MÎÍº\x0014¾\x0008Ns,Èÿv`S\x0002n`©¸j
kh(V\x001dà+±¿h®×¼¶×Z{°ãÞ!0£9AjÜZ7ÂÀ®\x001bØ)N­`
]ê\x0006VAr\x001fÑh
];°/}7°Ñ9o¸®%\x001f¯z­Éz\x001f\e\x001d\x000c.[\x0007íÐ`¿\x0016§L-FAÑw8å=íÌ}Ür[.àÆì*Ë\x000b¯s\x001e»\x000e\x0012yoB½û³pµ
y\x00030LÚ¹ýzôÃÝÏ\x000fð\x001f©"pÆ<\x0017\x0010o´ÁWi\x0005KàÂÐl)\x0011¤z\x0015ÒÁ¥F?½¿ÿH5;Ó]¶JÙïcuÝ»Íï\x000eí\x000c\x0003T£\x00047ÐRÕâ"¹·ìäèÝÉ\x000fgS2%i²<\x000c@áºPª uaÂÈ{GåJ*×rTë8,B¦NÖÜe2R¼6\x000fÊP~>Æý>\x0017pGJMI½Ü\x001f.\x0015J¬ÐpV8PÛg
)©æ%æbm1RX<\x000b«\x000cpù\x001càu\Zà<¥d\x001bm?â\x000cÄëØrZµïæá³àÀ.ü-
æoSúÎÛli.{¾}ªáð\x000ffÃ
U-æ"&Ë\x0008ÔHAó\x00018±[Å\\x000cÑDÅp÷õ :À\x0002á¸mB¥OOMùÑÉÙõ¤î\x0012»eÌÅ\x001cÍÙlæ\x000f½Æ)[£7Û^ãýÊ¹pºÓmpXWEéb\x001c_I!Fyn)w#¡èÃpjGþcÛ¶\x001eù¾l¾Üm\x000eÅ[@9É\x001468\x001f<E\x0000ä\x0018¥\x000ec©ó£·'oÏN\x000e3ºÑu0DIÞ\x001cÚ}<A\x0006
SÂ»\x0018ËÇÍ\x000c%dèÔ\x001cí5ËéMÐTRb4g3\x0003Òìz¯fð^yñêËÑÇÛç»ç£Ë§_\x000e[¤B-
WS\x0011vÐ-R\x0011^\x001d&ï]ýtôñôæìæèòêÃÔÕ4»«\x0011åØ\x0016Xìï£ÂIå¹: ä\x001a\x001b)_«Þ>XSÂ>X\x001b½\x0010VS¯GTõÕ\x0005ècu%«ëb\x0005çËC\x000cÕ2DÛ§p÷2Rµ«s¶{xßm^~¹ýúp(åÐ\x0000$×I\x001bÅ\x001d¨ÞJîÑ#m\x0016'>^_LÙvÕÊjg.¹ÐB@!KåUn\x00021rÄ®gJ<ÓxzXF
4VÒ`­_ày+z¤õh>+ñ\ëÇ5¹ùÈIö}.O\x0012{ËÉgÑéÝo«ó·ýþvóð@ÊûéËÁ\x000fì©\x0001\x0013NÇ\x0010bAi÷Gø¿?=¹¸\x00184øÕÛÃ¦Ä4\x001dV9Ð.\x0014x
\æäÈÙï©·aº\x0012Óu¦äÞ\x001fp\x0005x¹À¿pÚévÃÑ)°ÝGÿÃÝ6=0Ý\x000b|ª\Ý]:R
WÈ
ûºë}»þ³\x001f®NþmjºÛUãnPã­ÚåÒÓa¨6y
:7Rí±Ú^cwç»]è\x0006Ø	æ¸`	\x001e)y«,\x0007ÉyõÅ;ÎÒ®ç[\x0019¡­JèÑææ|a^Gò{¾xå¶:î{ïùðÜyK?|ÌRýNl¡Õzç\x0019i]î[ø~óôÓÝ¡\x0011yC¼KÓg÷yÀS<<X¸=3Pi(þ÷'WïÎ&\x0007äÉ]ñFâ
ôîö×ÍÓóí/p®{G<3ël\x0002Í_ à·z-\x0017¬ù×é\x0011¶N?\Ý~S>9\x001fþôß\x0016Ï?Á?Á/ý	\x0012g%ÿ\x0003ürjÁÁ³T3f^×!ôÿ\x0002\x001bv>
Ånß4LþÃãËý¡y\x0003C©%g¨#o\x0004K-#\x0019ÅýÎû'\x001a.ÿáòÓy9id\x000c5¨±\x0007U
#e\x0006\x0007\x000fl?EEy\x000bÀ¸Úoî ¦U'#å¸°°­Új;SËó£$æ\x001cl.Ý¢ öGî0u©;0áÃ\x001aêßh\x0011¤BãË#µ=M ¶\x0002µ] WÐJ4[©ÂÓ¡Úq¿)Ý\x0002º;\x0019%\x0014QZ?¿áÚG%\x0003}|ë}þÝ>>«vâ\x0010\x000fÏ_Ò )HpÐTEJ\¦+Ó\x0004w©\x0004}|)õ³|yqóv»6h 3?þÇÿH
ÕÖ=.py|y~Ië[¬MLæ\x000fOw??üõÛonþt÷Û?6d\x00026µiG¹/0cð-
ÖU\x0008!¦&Ã«³÷\x0017ÿ«$n¾;;½:ÁÜ\x0011$¦\x0000ùæÓøj5­
èeµ!¥É5`\x001c4±¦:\x000fdMí\x0013+±¦\x000f½¬^b¥ÄÀjÕ¥3°ä\x0002¬Ä
\x0006«ég
!¹+À*!ä\x0003kHÚ\x0014PMÚ\x000f±\x0012+Üu»U¥ê\x0019`ÕÃ^¤Õ'Å\x0004¬.MíY\x0015î¾ëfÅ NL¬Â\x000bP +Ã!Vá×|[`UùþsÅS:W,íLÇ2÷@jõ·\x0015LØª8½Ô'Ráù\x0006(aY
5_\x0016ï\x0012é¾\x0002öxXA\x0008W\x0000ô>¶!\x000eW ùØ\x0000¼XA\É\x0005"ëÿªx©ô\x0004YõÿN_¾ÊûÍ/;ªöãý\x0006þ©{*/Ãª°Õ3±Fop>4°¢uÄl\x0004§qJt}<?¹\x0000ÖóBu«j{X1ÐÆ¬\x0002§a\x000c¬:,JbVbÝªÚ®suiØ6°&Ãá\¥$V\x001cy»\x001eëVÕv«L)y\x001f@¹ ïXSv\x000fX­+²nUm×¹ÒàA`«\x001bU¦ø\x000b°ºIáÕÊºUµ]¬L!ªò\x001dàsõjÊieÝªÚ.VIok8WA¬2¿-2¼+±Âï\x000eý¬"\x0019\x000b®VÀäybÕ|®Ñ¯Éº5\x000cºXCZ¹w`n&VÁçêíaÐÈZ\x001a\x0006]°4¨\x0000`Í@\x0004~\aRqµÂ\x0016A'¬á[ 0S@°oÁ¯\x000b\x0003\x0017rØ\x00122µ\x001b\x0002¬\x001ffK%XE°`ß5EA2c¶]5¯,ôR\x0006Ë)ÒÍUYÒ®úÊÔ\x001b´
6Ý¸Z\x001e;\x0014.ð	×°°µ~Ò[hÇý¸Ï¶Ìç//ñþ±°\x000fN\x001e¾ÜÝbÆf\x001aü×ßÿóòOwsÍZ\x0017¨EÈ\x0007Ü{.\x0004ÉTÿ7vÂ\x0000{vYD\x001atptùÝÙ¸m[p'ý»[\x0014éò\x0001\x000bmUâÖ\x0014IBQß¬;éâeÜÖÇW\x0006n\x001b±sàÖ¹Y;éåÜÎ¥Êu\x001fpM\x001b-S\x0019NÄñê«s'\x001d½ô¼m\x001a\x000b\x000fçíØ\x0004óN+çÛÊ1Ó²\x001bêäâù?qàYþ-|ÑaV:É!89È\x0014Ú2eÔìlCÿIÿí×¿Ý\x0017wüüv\x001fýöÿ\x001e½¹}ú9U
\x001f&
l¡\x0014Ò;e]\x001aæ\x0014£°bÓR\x0012\x000eqó££7§WïO¯fÀbÙ7þÕOë)Ôã£f uä.\x0005)õ´XWuÓbð4Ñb|zX£\x0005´ÚÒÙ\\x001d3éfÓþ
þ}þß«Ð\x001e@\x0003on\x0018Íà½\x0000Î$2NÕÓ\x0016½3;[F¶{ ÌQ ×\x0010!½\x0006Â0ñÝg\x0010þåNº?êBÕ}{ûôË'{óx÷\x0015ÿóêñnæWÇnxMá\x0007ãÓ\x0015u¤æÀ4Æ)ÂûQ¿=½ú0$ÎÞ\]ã^]Í@f/é÷Ïüç/wòÞîDù\x0000ôíËýãóLTÜÁcè²\x0006ÊÓ@¬\x0006Áat£¦\x000cc |ûéüòf\x000eã6bÖÈHãã\x0007F¡RslÚxJ ø©N\x000bá6NÖJh\x0015\x0007øT\x0018Ú\x001b\x0008-ùñ@8i¯·0ncNØP:\x0014Äzð}
N"£\x0015\x0018]\q\x001bkjd\x0004\x0006,Ü@F8³TS\x000c/'
úÒ8\x0014%Æm©Q
ù{@\x000cÃÄê\x00011(Ftk½4¯ã\x000f¦¬3húààÎD\x001aqÅMº\x0006LVºÚ/:ÌÜ_þúåß\x000bñ³kìÝ\x001e}w÷ôuX\x00141G%y#9d£!\x001f]Ñh0ö¤\x001e3ï\x001a{§Gß]]®¨ÐTZ\x001e±¦#9c\x0018ÖMú4XIèA±§µ\x0000\x0015Õ2vc=N~»I¿\x0002Û \x001dm\x0006X«:fUµ³þwû¢\x001bóñ~ó%·ñþ|÷un\x0004ë%EHàAæ*eÑ02fd}<Ç\x0006è¡¯çôýùÙõxäçÿõïÿqû¸§²âÃæo`k=?Ï5·\x0014nOá'kíñ\x0010c\x0010*F2\x0008\x0014½hs}8ùÀäº¹°º>+Q6B\x001fßÀ\x001f\x0014Ã\x001fï7Gï7Os\x000fXK*e\x001dþþ8\x0005Ì"m(\x000eQ\x0017¶K\Þ\MÄ\x0018W¸ª\x0017\x001759\x0007^!÷AÐ\x001eí\x0000â#LÅ#[xuÉ«{y½¡\x000b¡áZ\x001b¢KÇ+ÄTxº\x0005×¸¦\x0017×´?\x0014x±\x000b6\x0015[\x0003BE\x00011©\x0008u\x000bo(yC÷ñ:´\x0013\x0007^trD\x0016¬ú@%Nª¾ù¸ÔÍMôò\x0006ÁµW\x0018B°xe`5[i\x0001®ì~oÁ³ß ¥\x00085öP\x0019\x0014Ý¨Ó
\]`Ù}#-ÈD`OØ²W\x001e\é\x0006SM+\x0003ÛN`,oJNr\x0016+FRyæ\x0003\x000e	¬\x0016^Wñº^^LbÑSÃå\x0018\x000eØqx&¸Öð\x0015°ï\x0004¶\x0017 LóXë<\x00104¦\x0017Ut\x001a+&{Ç2²tÂ¸!G9


boÄJÀ±\x0002½'¬\Ö\x001aK\x001cp\x000cb-7íÎÍ\x0007V\x0018V½bØã®ä\x0014\x0015ÃÍ \x0014\x0018Ë'\x000c·x%àÊHS½V\x001a\x000eK\x0007¬f5\x0013úé¥]ÉêQµÖ«6¼Ì7Â\x001a\x000b\x000c\x0007\x001fë\x001d0²\x0012o¥5T¯Öð2¦\x00169à\x0005),\x0014¶2
K\x0001`3Õl\x0005®´êÕ\x001aÖEJ@Ê\x001bl¶áFÄÈ7\x0002üÿ+µ¡zÕÇò²tÀÞb±a:`ë²k4\x0019Ýkà­´êÖ\x001aA³e	\x001a\x0004\x000bbt\x0012ì\x0018Ù¸Ö\x0015®´êÖ\x001aJQlÂ[\x001c$GONRô4*çV2$T¥5T·ÖÙvG·CKÊ´\x0006¾Â~²Zº\x0001XWZCwk
eøÍá\x0016¤Tu¨Xg¨é([\x0003m¥2t¯Êp*`¡Ùp¼1bO"\x0015<Pí©\x0014õ-ÀÎÐÝ:\x0003ç³%`\$é\x0002S£?\x001cp¬Ýi\x0001®]û^ßÞa·j\x0002ÆQ31\x0008#\x0015[\x0011j-gNWZNwk9å©Ä×ã\OMWeXDD¹Ö\x001d®îV\x001aVP/\x0010G4Ù\x0006`ÇBØèÕN¸\x0012Âº[\x0008[®ÖÁ*j¬í\x001a=Ë<
SI4Ó-Ñ\x001c5+\x0003nZà>à\x0006K"ØD¿ÒùJ¨n¡:#]aã8W±cäW\x0012i¦\x0010¦WBx]Ol«¦\x0007g\x00025\x0004E\x0019ÝZ\x0017¢2+M¯Y	*7\x001b\x0011h\x0012H\x000b%ÄZáJSYi¦×JCWÙY©u>`¬\x0017J¼ë\x0001W\x0002Ât\x000bÿ{/®²ÒL¯æEn
Âæ`D`­lÄJ:ÃV"Âö\x0008ý0Ï<¹Ú²\x001d¼Yi«\x0013¶Ý'½T³,1Épt­]Ç³\\x0001ãÿÜkHÄa±ªÇª"¾\x0013VEræ0Å»VÌ2·ãoãÅÆÐ¥ô9t	.Rò\x0008ç\x0006¤H ZúøptÃ?(rs\x001f7O³«"5V,S\x001däT\x0007^æP.æãÉÕD1dfU%«êc\x0015já´La\x0019©ì\x001eß\x000e¼¹¨ºDÕÇªÒX\x000eð2ü°)&¡RäÄ£Ù¾
«)YMç±Jì¿\x0019X¦ô¡ÂÐ¹b5Ï*¬¶dµçJóÕ:\x001cãÎÕÓ¹¸\x000eª+Q]\x0017ªò!Å¢l\x0003¦þ&GÒËOv¾Ïçô%§ïüü´Ô\x0008T\x000eË\x0017Ò¦
Öp¤öPz\x001ekNn&i%:\x000fU`Ñ9j@/úñl0t¬46y1l%®d¼\x0002NÖ\x00069r§¦LJbyç×¹­²\x0012\x0002²O
È¨É(·Î+îvÅÜP\x0005»l++«§%ûÞ\x0016\x001c"5Y\x0007"Ë\x0011¬¦º9\x000fVÂ*wVÕZ«ï\x001aH0\x0008\x0006ñj
\x0016\x0012¤+ë4u:z\x001dÄ*WVU·@õÝ\x0002!5é\x0002°\x0007#EÐ%¸:ÉxñÊ®c\x000e¨ê\x0016¨®[ "¯c\x0003Xàv©±ÍXG2\x0016ü­\x0002[IYÕ'f±\x0012#9Ö\x0007Û2©Ø;+×a
\x0015kè;XÞo\x0003\x000f	3\x0014Ip\x0019.Ð\x0001»vººw6l¬`cßÁ*d>è©Hb_\x0015áy¬ºR_ºK})°þ)én\x00158dt°Z:[ÒN¶¾Ï­<\x0003Ýç\x001aÈhX×:\x001d)\x0000\x001aR'ð\x0013ì:'[	YÝ%dÁ.àz_;ÄK'+,É-!â\x0010ÍLÖÚ7ès\x000ed,
\x001cb[Ò^Ô&áÍÁ\x0008ùLØJ#è. ãé"\x0016®\x0015:Iø?®¬áPmÖLØÊ;Ð}î\x0001®ìKÙ>\x001d
d\x0016H¶\x000eA5\x001cÈÿÎd­´îÓ^8î>y³\x0006§#¦
u\x0011\x0005Áºh\x000eÅ7fÂVÚK÷i/\x0011-93F\x000e»\x0007\x001bF°¦ÕêPAìLÖJ{é>íeq\x0011¦L\x0007»rRtàS.Äé\x001eÙ°öÒ}Ú\x000b'u¤ÊhÓÉ,°2°Á59\x0006c6«©´éÓ^&rîÔD1øáx°Þ§è\x000e\x0015WÌD­téÒ]*æ´¿Õ8¼#\x00190Ã\x0004¸Vb\x0015ÖJ\x001d.u p(C £\x00004NWÀhiÙÚr«ØÜ¦°¦KÂª\x0008ÎO¬psUÛlÀ¬t]+\x0001kú\x0004,v \x000c®\x000cÃÅG6ÜVY.u´¬©ä«é¯ >]E!+.pgÉ;\x0000§f\x001dÖJ¾>ù\x001a &1\x0010\x000c\x0017b
G£Þá`å¡zøy°¶Y¶Ofá\x000e°\x001c5A\x001ajqez\x001dÖÊµ}6¬¶´\x0000\x0007£.¦B\x0008ë\x0015Y\x0004Þ\x001fJäÎ­¤íZ\x0000CÕ­V\x0015)R -¥ì°[}\x0015ÖVF¬í3b1*/
:ß!¤å\x0006$çÝ:¶­CÜ}"\x0016lWJZ\8O1\x0018IkDádõ¡:Ü°µ}BVKZw\x0006õÀË¥Î
\x0007¼Î-¨\x0004í\x0013\\x0018Ë ûÅ\x001bMù#Ð5oõ<\x001bÖUÂÀõ	\x0003\x0005NVIº\x0005`\x001c	\x0016\x0006rH·«ë\x0014\x0006Ú£=\ÙíhO)¨"ÉãU`«÷åúÞ\x000b´
\x0015=ZcU\x0006VÅìÑ®bÇºÊ.p}vÁ°7YÜ¸¡È%\x001fÑQjÎEkW1
]õ¼\ßó!â.^u<áéq¹09t>jåu¹.¯K9¬è¡sÅý\x0019éqEÉ7@¯cnùÊñ}\x0016´ã\x0004 ¡h¼+ÜV\x001aµà_'à+¿Ë÷ù]6(*M\x0004g1P-%h1ª<rk»fÂV"Ö÷Xð«hhªq*ë\x0003\x000ckÐÉ®ä|ûJÄú>\x0011kU`"ö½¤k\x0000¶¶$«;\x001c*à	[Ù[¾ÏÞ\x0012FÑtO#ñRU\x0000\x0013ï¬\x000cëÀVúÀ÷é\x0003+$M1\x0018O\x0007>\x0019\x001d¬]'tì+sËw[8^bòÆb6Á
\x001580¿×\uaAò2ÁgßË\x0007ª£oF¥ëp²äfÂV*Á÷©\x0004c$õ]\x0000JW$õågXiV¹²¡\x0012³¡OÌ\x0019Èþ\x000cHã$eÑ½Úu23¡\x0012\¡Op\x0005@]zà"xÊÌ\x000f\x001aHÊúñYm°à
]K\x0006«©yÁ`é·Ncn#£\x001b
ÆUX+¹\x0015úä\x0016îÂ¦\x001bëí°úi8X©ÙC0b­\x0004Wè\x0013\AÑÆd8X\x0017p
Øp°c\x001b&Äu`+Á\x0015ú\x0004JÞáp²\x0002ý\x0017ò½h¢>Z\«Ý¡2»ÿêÞ.Y¯ãÆ\x0012Ê@H ÑOÄ²YA,RTô}r\x001cIçÚ¬+Snt´ë©¦QoýØ\x001egR#¹@~;?Ö·2S
»«ÝE\x001dÉêµq2±\x0000$°\x0010»Ân\x0016N×¬r@CP,kk¯\x0019`\x001b/\x001bû¼,\x000fó\x0017m³#¨Ð¬±1È1È\x0001â\x0014þJMäº"o\x0008¿¼X\x0016\x001dx¶,ß<±,OÜÌ\x0000ÛPBê£VæÄr`X~s±,hVëý>ÔDÞ©+ò\x0006\x001e¹*òqD,¦]D
9n\x0014ËºI`\x001b\x0002K}\x0004Æ{°õäµÆµtø\x0017ËÒz\j\x0008,õ\x0011\x0018Oß99³¸<Ð\x0014E¹¨gæ`m\x0008,õ\x0011\x0018.W oCyô0hE2Ã{»©ú~\x001ckÃ_©¿|2J	¼7Ø 
jW;ÅÉ¦¾R\x001f}!\x0019ÊÍv\x0005Ñ\x0019àåkV
»7Ðx\x0008,´=ýü]Í¹byþ$\x001bK¼å´Âø=]°@m\x000b´Ï\x000f°þ®8-o¼}r[\Mj§ä^ÐöÉó_ö¥àFúy\x0007\x00147PCY[àø\x001cÚÐ¢í;²\x0006\x0008¢ggºd\x000bZ\x0000-ÅÍ];ÇÑ¦\x0016m_\x0014!é%\x0017µ'S;Ð,ü¦Ìá)´Ð\x000eø@Wd\x0000)1R9bùv\x0010´\x000eµf°½\x0017æ8ÚÖ\x001dô5Íó\x0006ûê\x000eÐU}ÞZ4°~
\x0001´>\x0001º|\x0002põ8my\x001e¤\x001e£õNç§ÌÎ\x0000^Í#ôÙ\x0016C}\x000cÇlÛ òê\x00130ìÉK\x001cDÛÚ\x0016ûlËó`+åWýÞJ¹aF\x0016\x0006Øú[ìò·À\x0003AÑ.GxA\x001b´~DsÑ¡mF¾ntðÑ+´|2IwNS\x0004àj®Rà®ç*Ïuyëshþç($¥úà¹\x000e>eàãwÿëÓÃÇ²F@QçÛ&?ìiðóÚ4çl*O]Xé4sZeð3Kc·¥sx$é#¼\x0019aéõ¬M´sÞÆ@\x0016G]Å\x000e}Ñ\x0004Õ%QÔ÷ïyG^Ì5æ`z!\x0003·NÉã\x0013÷ýHR©ñÛÓQ:Zm¾F\x001c¡\x00171«ÌzmOÒlã>F³$ÔÃ>;Ì©û0'Ïå»¥ÕÞ\x0019é\x0003­/\x0010ùJÞ\x0014v>9Ýüß¹\x0001¯ÁM«±Ìäf¸÷:Iu;ÉÇô\x001cÿþî
4Ä}qY<)±µü²*1¼^Â9
\x0000ÙÖ\x0019ºÛÊV\x00061<p7Êä³N¸$s\x000býgîÙ÷ºgÌ	Ü½¦-iÀÉ!\ÂIÜMþ\x001a2ù^ÈÄÝwÅqÄ\x001c$C§5Ò\x0017ÖÛö'Ó¥Ï(\x0005z½Ý¯\x0015Ïéfµ¡»c¤¨µ?rì,M±Î\x00188§ø\x0017Ýg¤âºIÅè2XÊDÈ\x000bºó öäÙ)^#|F*¡TÚ§â £ÒíSñ£ñyT×}4\x001cÊiÎ|\x0012D\x0004¢>è¸<IÎ!Ï¢º^;CJIûsò?¨O\x001aÆ'}sÞ_à3FnJYq¶hÖÊÝ ¼ºI"4gæß~æm·v1jôÌÙ­\x000cL±¶ÃMJR>O¬z³*në/®Ðèè7»=IRì`kI\x0001Z\x001d\x000e
´þö_ÿñ§6º +\x0019\x0015\x0001±X\x001bûóíq¤ävzå÷V¡T´¸F½hA÷H\x0018Qd!ªàdNc7¢Ã`í\x001a¬í\x0005kê»²iA46HJZóLKk´4p\x0010ÖÊúÌ|\x0010t¥¼ã½~3Ðº5Z×y\x000eÅ¶¤£¿ÑÙzl·ã¶Ãhý\x001a­ï>	Az\x000e\x0017ÛÖ c\x0013lÛÍráa´a6ô¢ÍÙ¨\x0017ÓZÞWäB\x0005æ6®ÁÆ^°\x0001TÒ5Æe1Ã6Mv	Ûã¿Ñ¦5ÚÔ6jsw¶-Êî\x0008NÕ%Ð¶NØQ´\x0017A£\x001bL7\£Ïl\\x0010¸¦¥ÍÃp[*ëå2ë«xgÊ\x0001.ÃA[O¹eÐP\x0019ôrÍÁx°¨Ò¾|õ`´Ý(y\x0018mÃeÐKf6ùºw1\x0014a_£«TKÛ\x0003Já6ô\x0000½üÀy½¸\x0014ôä"XY°<lwñ\x001cÛð\x0003ô\x0012D	/~T)WÕU»Y\x000c<\x000c·!\x0008èe\x0008â&ÖÍ}\x0011É\x0005ÙI·-\x0015s\x0018mÃ\x0010ÐK\x0011­cÕ\x0017¥¢Öi@½Û\x0016½<¶a\x0008è¥\x0008
Fã°Ä"ûÅ¶¡v{hñ(Xl\x0008\x0002{	Âz¯ÙCâõ²\x001d\x000b£²¯sn±!\x0008ì%Ì®ò$\x001e3çèV\x0016H?xS\x0018¶ÉN7C°À\x001c\´ÒëÆ\æ³í'Ãp\x001bÀ^ d$W\x0006ëJ\x001a½ß~9µIv°7Û±9úòâÁ8\x0003PÁ(Srñæîòsp\x001b:Ãn:ËìbÚÒò¹X\x0017Ôù°]>=\x000c·¡3ì¦³tmA²:½\x0005}wq»
y\x0018nC\x0010ØK\x0010ä¼nµfÁ\x0013q¹Ô¸°-Ít\x0014­m|®íõ¹¤ú\x0004«QåiæÄ¸¶q¸¶×á:Þo,çeåÜbõ
;=õá6\x000e×ö:\ÇÓe½±!§jú("B¼üzÊ-³my©×ß:Dþ,.ã¢Q«ºéÁl+Ó\x001fÛ¸\Ûëry\x0002Õ£ hu0Â\x0014k\x001bk{=®cU\	\x0015r\x0002Q­ÆÝ\x001eÀ=\x000c·ñ¸¶×ã:\x0004\x0007Ég\x0001U¾.¶ñiN¢n\x001bk{\x001d®CU»Èhf´êÅÙÖd8\x000c·	ÉmoHÎ'×\x0015´9Û±IÐêhÖ\x001aKÝ>\x0017#'\x000cÕoJý\x000eQ×Ë\x0007»-1w\x0018mãr©Ûå¢ál\ÃõòVWÚ°¾Ô\x0014¸Ï¥nk\x0004\x0016ãò©(»*P¿.º~Sà¶5ýnk<aG@wÕ¢Kz\x0018p[\è0ÜÆéR·ÓåQ\x001b(Öµö\x00027èº«àau2\x0008õA\x001cya4ànD	ntµ9o\x0010\x0002¶ñ¹ÔëscÕÁ'\x001d\x000bÿú¤¶Mv{íÃa¸Ï¥ncRÀPcrLº.3¤í\x0016£h]\x0013»Þ{JLä\x0015\x0002¹O\;Ç¹"\7ExàçÿÅ¸ÜS\x001bkÔéfârt]Ã\x0011®#ø\x0019Ê\x0016ãæä·t*cðº'3Mz=síËd¯\x0013ó<¾° Í,ÆjNmëjåè·»,\x000e£m|ëõa<ÝH\x0002«ºÅ-\x0010ÞPbù÷)p\x001b·àzÝÏ\x0017M*x\x0018HúõtcAq»-ò(\ßø\x0005ßé\x0017È\x0018Ýµ®Êicª«­²_ãtãºåFx¢¶Ü5r \x0015,Ö¨üsþoÊH0':\x0007üÝÃÕKÚÃÀS>\x0002¯ßÒjïÂ\x001c*Fsmf4ýfþµç\x0004\x001d\x000eèGíx÷F¨1d\x0017ÁÖ\x0010m{áx¿Ðg¦îÇ¼LèÈñp²`\x000e"ÖÓ1§¬cÜ5d7\x0000Caª/¥þ°n\x0019qs;æ³Ã1p6XB#ú
ºö\x0010Õf\x000c7ép¤kÐià\x001a\x001a¸µÝE×vY
ãÝÎæû]Ì\x0008Wízù\x0007µ]ïÓÝ\x000f?\x001cÝß\x00079ûÔ\x0006\x0007f\x0016Y"`\ízÚÖ\x000e{÷æ'_mlïS¬¸Æ]X\x0011¬ÔR\x0003+H;iÕz\x0014¶§¦\x000fCµk¨¶\x000bê"e+õÖ-=DP+üöJ´ÃXiúÌÂ©Y\x0010
é\x0003ÛÎè\x000fcuk¬®Ï®I\x0017\x0008d»\x001a^ÛSì\x001a|µë\x001c¬~Õ÷]-^y¡n Õµ]éb×í\x0011¡ÃXÃ\x001akè´k\x0015c]Aìê¼Þ-¿]>5®±Æ>»Æº°Ïk1·PÝ«Û\x000fcMk¬©\x000f«Iz·ø\x001dPÖ
z\x00159O\x001e·9÷(ÖKwÞB\x0005¦\x000flðz¹øÀMëùs\x000f,´¼ÕI\ £4KÃõAb¿3¹{\x0018lC\ÐÇ\àA4j\x0002¯Ç\x0014\x0017\x001bèÒ[¼Ý¤y\x0018lC]ÐÇ]\x0000(!WÌÿJé\x0011\x0001\x001ex\x0015ËÒ\x001cî» ¼ ÿ3Å¬¤ëd\x0002Ê²Û-\x00176Ì\x0005}Ô\x0005@"ú\x0012
/q\x0013³ÆÚ?è·3ÊÃ`\x001bêNî"Iâ%®bzUËn«ÿ\x001c\x0006Ûp\x0017ô\x0017VÇ¸,í}MQ7Öû²ùa°
yA'{YË4 ¡ÇZ(ÝÓP9\x000c¶a/è¤/¢\x0010yY²øØ¨e\x001b\x001f·u(bÅ½°½ò)\x0000¨!n\x001e
©ÚuÊÅ6éä\x0003>±±ö\x0012ËúÙì\x000bôÄâvëóa°ÅN\x0017\x000bI\x0007cR\x000e½H\x001d¦ÞÒ\x001c°ãÂNÇV_Ss\x0000Çm¯\x000bØTÛ1i³\p\x0018kã
°Ó\x0015°d¡ø-¬ÛÐ|Úà¸]­;
Ö6×Ëv^/ôúÀc(È«:ð\x0014¥ú4å~Ùæ~ÙÎûeS}¤vQ\x0007\x0002h· Oiã²Íý²÷-+X\x0013\x0017Å°®bB\x0008¶¹^¶ózA}C59¦õÊ\x0008 ½\x0015fûÉ÷0Øæ~ÙÎûÅ
a/¤K\x001fx7s¿ y*Ø \x0016\x000fÏ\Ô"-\x0007\x0012Ñ\x001aKsë\x001bè¯!£ïÌ\x000b{à³|!¦Xó!Ïð]&ñ¦Üù\x0005wÏf3¼züøîãã]|ø©OÅÙ#OÒG\x001d$«-\x0000ñf\x0007À«§ß<ûæé]Æ»\x000fÓ®aÚ\x001e)Þ+J+5\x0003^G)Ç6ÒMp\x0006¦[Ãt\x001d0CþeÒ¬(¯¦I\x0016¢e7k\x0005g@5ÈÐ\x00052¸È\x001aÒ"ê*dx+\x001e8\x00033­a¦\x001e99t\x0002\x0013µ\x001fÐAµ¦½9 {\x0002&´\x0017¨ç\x0006±àr\x0019ß© È;®Ubö¦zÂ\x0001 ¼D«}ØÈ?àþìzøùgÖMøùîù§~÷øáñ°FM:qÊjFIV:'V&¸\x0001ùÙ×¯¼yÃ\x0002
oî¿}ó&ÿüéò Ç5z\x001cDOFå	¨,Ò.èÕà\x0010nn\x0012èDo×èí z/Ûê\x0003qá^ ²\x0019Ä\x0004Ü	Öài\x0014|MX¦¼
\x000cEE³vÛÞ­Ñ»AôI¥Yx9UÿÄjût³ñ±\x0013½_£÷£èëÛ	Ï,cB\x0011õÎ¶|êÃ\x001a|\x0018\x0003os\x000c'Õ^âæ\x0000¼%Pì7Ç\x0012NÏ÷ê\x0001ÈÙÕ\x0003Ð·ï\x001e~øôýQÏNªz=;hK«A\x0007îe!ß>{òÕÛ/÷Á¦5ØÔ\x00076ÂâM\x0016°à \x000eú:_\x0015q¯0u\x0010íê]%£]½«³mæô(MÈ)hÏC­JÄÑñãp¡\x000bÖ
V\x0003zÈ,+1è\x000e£\x0014Ý)ø\x001ck\x001b¸¶\x0013nNól=\x000b¥eÚÞ¶{VGÁR\x0003:÷E	%µ²\x001e
]2õàî\x0015þ¢u
Z×6ñ*q\x0007ó"TÑëIði{Yûa¸«Ú_»ªýKÀµT\x001dË\x0017\x001dQ\x000bT»ßvdf£m\x001c.öy\Ê×_´ßC¤(Û¬\x0005ÍF)m\x000fæ\x001f\x001b\x001b¸±\x000f.(-<W#5ks{±.ùí\x000eïãp\x001bÀ> ^­Ö­ãØ6;\x000bµnHs®m(ÂöQÄ²¾F{êº
KI'ÂÈmK\x0016\x001eÛPí£\x0008"ëù\x0005sóÀ"di\x001dT¸~×]\x0019.öÁuÜ\x000c[¬\x001bb\x0012mEëAß^×LÛí#	rH*5\x0013¢V¬·zt'Ñ¯m®ítºÎ[Y\x001cwòâbëâM;É¶×µ^× ;{s\x0010ó"9	Úí\x001f¶÷^\x001e\x0007Ûø\Ûésys3È¹ÍT\Ö¢çP]-n/<¶q¹¶Óåò±MRlËÙ\x0015ÛÖZE¤Ia.5>:}\x0018,\x0015¸LÀ\x0012æZ\x001f5\È×l\x0012Ü&Ì¥¾0	 \x0006æ£ RØ9³0±^³9'\x0017\x0004I{VO\x0003§\x0002H\x001f\x0002÷?T¢ê§=ÎiÑù|\x001aºQàj\x001eåE7àÅ]\x000e\x0006fù_ÕÖ9ùß-ÇøË?<¼ÿøááÝû5Ùìº@*=>²Úñ"Ý\qhÑ»ÍQ/ûäÅ7¯<{±QU´¸F½hó1\x0006*hý"aZà
]DOEgðÚ5^Û\x0017%Òñ9ïå*à¤Ï0ºí-Bgðº5^×ûI\±o&a©ã\x0018ãeú.BÚÌÎà
k¼¡\x000foÎ#;³\x0005¯\x000b2,ÓWY\x001a\x0013y\x0013Ë\x001c¸q
7v\x0017¹`AnéÞZvJyQÕf;g[Áýþá?~¸
7­á¦ÞÓ@Vü¯·¬9"¢âªÃå¨-Ö8aÞ>(^:O\x0003æAò"Þàm"~`b\x0003s_o\x0001¸)Pv\x0006pë|»½/?Ð³kË§lYH\x001cDx$"l\x000e(\x0001ÜÜ7è¼pà3àÒÈÃ®V°7ÒC·M1ñ3#\x000c½g²[(qçMð¾x`Kzçp[2ö\x0004`l\x0004ö\x001e	bAæâ$x)gØF[\x0001ony8\x0003¸¡\x000cìååÁÂÊ\x0019\x000e}¹túbÏð,'íl`±²iç
mô+ÄÃ\x001b3SëQÞY;C\x001eá\x001eÍ\x0001D@ÙÚ\x00145`ãá·{« \x0006{ýnÍj@ðëO?ÿí¯GüYNGÕC=ªîmf?Éïw¦sßÞ}ýöÍÓ\x0003Xí\x001a«íÅ\x001aU\x0015=9¼\x0017A°:+öê¿\x0007¡Ò\x001a*uB5ò\x0010­
Uõ\x0007©Zu[Sé0V·Æêþ®Íê×P}'T¨feI8ÕXÓF\x001ao¶Õ\x0001\x000fc
k¬¡×¬Pîr\x0014lU³LG\ÜV<\x000c6­Á¦^Ã.£¡EÞ4èû0«¨rì¶LäQ°Ðú¬^§\x0005¨µÿèåzÙºÖÃo/ZÚEîÊÃæ\x001fT\x000fûx÷íã?¿{¸ÛÁ`h\x000cñ^7\x000e\x0018Sìlúöéëo½Øì\x0014¸jMb¸Ø	\x0017\x001cJ\x0004ÉÚDuN\x0010U\x0002ÒÞjÄÃxí\x001a¯íÅË+\x0012DCKgÒT\x001bHGCp[Jé\x0004^Zã¥^¼Dõq¬t¯«\x0013£\x001c"LÂëÖx]/Þ\x0010¸Ø»àu$çFÕ5ÀÞ\x0012ÕÃxý\x001a¯ï¶/Tm\x0017ðé\x0000í\x0008¤¸]V?7¬ñnûZ\x001dÆãbÔ½U¡×lï(:7®ñÆ^¼V	.oIî\x001b\x0000éÓëÎ&ëÃpÓ\x001anêëd?aQ´SóêmÛÝav\x0014îºÈ\Î·ö%F£i!è\x001eÏlÞ½ý¿\x0001·ìÖKo<ý¬t5i\x0002Aqûð\x0004ÞÞ ß¨j?Õ\x001c¼*£Ó\x0016Â	¼
½A7¿±\x000e¶Ø7\x0007;Aum½nÛJ½'ð6ô\x0006Ýüf½\x0007^­,ÚZ¡vføí]\x001f'ð6ô\x0006ÝüùX\x0016Õä\x0000Bç/Räh\x0012_@ÃoÐMp¼\x0015\\x000eðj¼4éÄæ^»Ã	À
ÁA7ÃåôG-ì«²O0«§ØY\x001bnã§Â\x0019æNÕ#\x0001{ë\x000f\x0003n8\x000eºIÎR=\x0012\x000e5Å\x0008FÙ	·x\x0003Æå°åP7Æ³<ªçø*±Ff{÷\x0004àå°ålÕøÈ©´\x0013O\x0015¯\x0014õ`Äu³\x001cD­ë\x0005\x0017\x0001\x0015*m²³\x000cÜÐ\x001cvÓ\>\x0006â# Ê)]\x0006mv \x001aÃn\x0003§
ù?÷¨\x00025jß0
oCsØMsu!í¢ièv\x001bÙ¸­\x0003v\x0002pCsØMs R¨!U\x0010³UÚ:7ëÊ54Ý4^¹|Ò -¬õÛ\x0005¿\x0013\x001bÖÀnÖàIµ°id\x001f«pf\x0012^Ûí%
Þ«Qz¤<\x000b©}AD-Þ\x001c;·á\x000cÛÍ\x0019Ù¾¢¸åé2¡\x001e5³vV fÛJZ·\x000fÎ¥äÊ,óô\x0004ë>L0éÊÙÆ	Û~'Ò^Âý0<Ö">B-¼#Àv\x0002pãm·\x0017ÎaúìU92©\x0012\x001fÇÊ\x00007^ØöWÓH\x00035½pÐlY/\x001deM\x0002ÜxaÛl¨²~ð\x0010tz0õ\x000cï¬9\x0001¸I6lw²}\x001aØ«ò
7r¨·Û\x0011OàmXÃv³3Ú¾î2ÍE}\x001f\x0010ûbØn\x0003>\x001aÖ îT#$Ùc\x0011\x001cX\x0019jàU	wtBN\x0000nhú\x000bjú\x0005°ò\x0016\x0007¼ZxK£&Ó îL#:	Ü±|2ÊóÎ!Ïâdj(º).8­¶;ÒWÙüCÁ;«!Nàm\x001fº\x0019.Ä{*\x000cÇ\x000fÊÙó4V\x0001\x000c³^¨a8êf¸H*ÈÀ»D\x00135GÄ
ø¦$ÇY¼
ÁQ7ÁÅ$Û¯\x0002/\x001f$ÕUÅ>4³êíÔ\x0010\x001cu\x0013\\x0002VÅ-'Â\x0008\x000bäê\x0011m=Ä\x0013\x001b£nKþ^ýEÿ?jWçåg=ÀPÃoÔËoËä®:4àxXÕ£mOb\x001cÇë\x001a~s½üÆxUL!\jIwYdj\x0005¸!\x000c×K\x0018,{¢¼:®\x0007Ñªr6X;\x000bpÃ\x0019®3Ðê@ 0è*\x0015â`Ræ\x001aÒp½¤¡\x001eaëlQX\x0013O\x0013Ì¤;çÚ\x0016^Ò@[[Ð('¢ÅB(I\x0006Ðöðñ	¼
i¸^Ò@çõMÎÆªI\x001b½´¦&\x0013·æN\x0000nHÃõ\x0006}Ð×\x0001XØé«'à4¯Öë%WªWãµ7IV°z·µ	N\x0000nhÃuÓ\x0003\x001dæ$Þd!^Wò\x0014\x000bÏªõø6|7md\x001fQ&eyE4þf\x001f¡ûb\x000c/C\x0003¸I|w\x001b]ÎJØCÆhà\x001e½â\x0005³­\x0000|\x0002oCs¾æRÐRÍË
vH¨}2\º\x0004¸¡9ßMs9z\x0010'lCÕÜÏ¤QÚ¬WOßÐï¥9k\x001eaÞ\x0017`ÊHR9f5*úå|7Ë¥ Ã\x0019»\x0013½\x0015>\x0011JË;Òû'\x0000·t½4gÉê\x0013\x0001é\x000c\x0014Dú3\x00067«ÕË7,ç{Y.gËZ¬D\x000fÕÀu(ÅYqoXÎ÷²-KãyX$±:°\x0000(£9{\x001a¶'\x00007,ç{Y.'sê#¼¾"&§ó§ÉIw.44\x0017zipÙÿÈûâu7G
u\x001c'Ìºs¡¡¹ÐKsµÂËã-tR¿N.ªgu#æB/Í-J<A&¾CÕò\x000b2N\x001f=no<8\x0001¸¡¹ÐKs¼o·è²\x0007Þe+íSu÷#g\x001b³\x000074\x0017ºiÜ¹la¼XXO0â$/\x001c\x001a\x000b½4g%êá5ÌF­«\x0005¼qu\x0012ÚãB7ÇYÒÙ@Qwcåã \x0005\x000efµ_¶]¼ä,êÒ)~:Òãà¥äIcGkH.t\x0005Ê`\x000bs_lÈ\x001eM,LÓ^¸BCr¡ä¤ØÃA¥¢
ò~Èp'í±a¸ØÍp¼ø\x0013{\x0000ÒD.y%\x000c\x0017&¹³Ø\x0010\ì&8G²@:\x0018·´/xkØ\x001eÒ¶Hâ	À
ÃÅ~\x000bU·\x001b\x001aXí;ëÉ(6\x0004\x0017»	ÎÕîU©ÃH*\x0001À;Ü'\x0001n\x0008.öçqÄn¬¸`º÷zUÆÂM{ã
ÃÅnsÈÊ
s\x000eª!¥È\x001d¢ð6\x001c\x0017»9×ì\x0016\x0003ó²y©¸ç¨]ð¬Î¿Ø0\ìf8gïÅA×\x0017å¤1ìì};·áØÍ\x0017	.Þß^\x0003ò\x000cµ\x0000ÞYq\x001cpj\pêwÁK'Ï\x0014eFNê¦vVå$5.-õ»4/\x0013\x0004Ü\x0011¬åëTcà0íU95\x001e"õ{\x0008«1{âVwu\x0010 Yç¬++úJÝÿÄú\x00145¯÷24\x0019iÚ+xj§úºï\Îë¥Ôc´.E\x0015\x001ac=¯)áj\x0008Üt_º]bç9Oi4Hºp z3©U\x0006Ú¹jþËþÔ¾h\x001f9#öõ¢{dÍ¤$\x0019Ú!ZþË^3Ü<Çhy¤Ün%\x000b)NjÈ\x0007w5wÖí#2\x0015à¥Ç2(T'ÿ4«ö¿ûîêIã»¿÷7à[Ì9§íÄÿ`ö\x0001ó\x001f5|=|Ò,v¶¡U©\ºX«Jåßo#«wWçÃuÛÚ$\x000eßËù \x001e.(P\x0015åsT4\x000fóÃ\x0015æÞv_æ­*2_Ë\x0013hz¦gÅ\x0016ùLu¦¿ï¯\x0001QIIC\x0011n/\x0001½ÊÒÑ´>û\x001f®|Ç\x000f½v¶÷Z×\x000eÚVHú\x0017if~¸2sïÑøÕjæ3×1â9¼\x0013Å\x0010ó\x0017hG>ñêYù©¹\x001dM?n§zJ\x001auÕ`r¨§\x001apÖ\x00034¶71êÞh¶} §z¬­¨£,;èf=_Û:SB¿­­n§ei	\x001dqN^V0ÅÃ) 8%SçüJDéÕ?ýñÝOïi§ó·»\x001c¥\x001fÈG©\x001aòê*Ü«ç/¿~öòÅ>^\ãÅ^¼üø±Ø×±h´à±ÂlÁ»?B~\x0018¯]ãµ½xÙQ,EzgyxQìëEÆÃ½\x001aÜa¼´ÆK½x½ûù<@üJRõÎçáæ¶Ï³xý\x001a¯ï>\x000f ÏºÎa¨]Û ;­\x0002á^×öa¼q7vâ5IÞnù£\x000cª©¢@\x000eC÷:\x001c÷ñÒLzþAõ\x000fÿõ\x001fÿùò\x000fïz3W\_ª¢¼) ­yÉÆRÕ\x0005íÝËß>Ûòdt%ÎH±\x000fir¢¦\x0015-ô,¡­»ÍÝîÖ>Ô®Ú>¤ÑÜM\x001a\x0018tÝ\x00032oIãö=\x0008Ö@©\x000b(¯ÑEÐùÖ« ¿å\x0002P1)7#õk¤¾\x0013é2qÄH\x0017éà¢²hC¹T©tÏ#
k¤¡\x0013i\x0010ºNÖY\x0019É0ÓöûÆAq
3þ\x001d\x001bô¢ìµx(Ó\x0007\x001bèÊ\x0006F"m@\x001bË¢Ä\x0003»\x0013.>4.
ú|\x0014W],P]ªÞ4Öß¿Û\x001eÐ8\x0008µ¹úÐy÷QÇ¹µ\x0005j
\x0002\x0015ÌÍ=¨§\x001cÿ:ô.Î¿FÞ'\x0001êÿYî\x001cue\x0002³Ý\x001e³×§+JÍ1Pê×¿ÿp÷*Ãz|øÄáÀ\x00178.jm®ØJ,ÏRVX\x0003ln«Ò}ý×w¯òßzúä-\x0006_<ýíÂµ|\x0007®¿\x0003g|\x000bÚ| \x001a «¢¼~³á²÷;ìú;ìßÇE³9§Ê\x0012F\x0000Ie"ÿ>6ç9z¿ÖßA3¾#ñòt#\x001f®Z,ßá«6nÄ­0³÷;Üú;ÜsetD,ÙTÞûw\x001bègü"¿\x000e¿þ\x000c?ã3NE
>Êõ¨Ëýv?rïwõw)¿\x000e({\BÊªÞ*\4Í·Jþ½\x0011×\x0011§ü:¨Þ°¨\x0006/ß\x0011µ4ía3	ë¾\x001d
Û-7DÙî\x001fé¤ëòSZ~¾{ýÓ§ïþö\x000f/þÆR¨2+OåÃrª\x000c\x0011ÕÆákËKJüæîõË·ß<ÛYY®«PiUê-ýÎ¬wJ\x0002ÛI¥/Ùí]\x0004ç`Û5l;\x0002»¾fØ¶Z[eÈã^¢|\x000e6­aÓ\x0008l\x0013Äó ¯\x000e\x0005µiwÞ@¹]z?Ú­Q»\x0001Ô¬0\x000fèH\x0016ù\x0019«Ã9Ûßô9\x0005Û¯aû!cW©oLKýr]E\x00039\x0013\x0007;¬a!kW\x0005bË«kÕÚ(Á±3aÇ5ì8\x0004Ûë\x001e\x0003Ë=B(Ö®ÿ´ó<s
vZÃN#°#©
\x001b·\x0002@Yf«ÀÙÙ½|
öªTÀlcÌ*ØhmÚF>%NOßy>»eÉ\x0011ä\x000fÐÉm+/5fQk1Ò\x001díS¸\x001b\x0011ä
¦:Ó\x001f´Í;ãVá\x000f³·÷â\x0014îp`q\x000b\x0007boVZ\x0011Ü¨åOØëÉ9»¡\x001c\x0018â\x001c^O'óÜ¿agÔª\x001c;n§`7\x0003#Ã\x001a¢ûJ¦^KLªo\x0004¸ó\x0010y\x000676î\x0004GÜams\x0011he\x001b Hlì¼GÝ\x0006¯#·2\x0007ªªlÍ5ònf ê¶^ðÛëÒÏán¢W\x001c\x0008_³ó&íãSQÉãû£ö\x000ev\x001eë`ãMpÀðX!Kä\x0015Ü$-/<8¡2\x0016~çÝï\x0014îæZâÀµÌ)«\x001a=¼x¸ÄTÆ\x001au'aGfê\x0014î&\x0014ÄXEn4Å§¸ìZÖ\x0005ê¾ÎÄ}óp7± \x000e\x00049]"@UBYô\ÅaoÑ\x0019Ü¶qvÀ
BÌÑ ô½PXÄ§\x0016Ü:íìâ:º©ì@LÅÎB\x0007¸D\x0007e«kÐÎ(¶öDÜ÷¶\x0003ÞE½4ö¦Dºz´jÌ ÙÑ
=\x0005»-=8oçS
aó¥,\x001b^\x001dªæ"L\x0004Ýxn;â¹£©]Î^9Ù±nòDV:»\x0003í@\x001c\x0008Ü\x001e%\x0001\x0015ÏÕQñ$TåNMÜY­p
wÃ8vqòÿ¨\x000e.\x0005Wï$j\x0019ÒXö)Ü
ãØ\x0011Æ!\x000bZÆd½\x0014(cQ\x0003Xã&¦ñ¶a\x001c;Â8\x0019°Ö¨Ø\x0007æ´l±·Ñ}\x0000,\x000e6\x000fwS~°\x0003õ\x0007`µ*\x0011Dµ\¯*[£
hg\x0013Í375DI#Dé¯ G\x001eõX\x0016\x0007¨ºÄOân¨F¨2[VÓa\x0016R¶²b\x001eT´(íõlÂÝP%P%Ïx(ÅãR¦ZH'V%å=5«S¸\x001b®¤\x0011®dÕ0\x0011êãE§¡\K0¤Ï\x000bngÝâ)Üm~.YZÛ	Å;eKgj\x0003\x000fÏ'a7¬C#¬CÉZü2^n%\x0019ÝCdâÄ´\x001aÒ¡\x0011ÒáG(Q$Å[·q:ÓÍÄ9\x000fwC:4B:Üÿ$å\x0007K$ Í¾QU('\x0006°Ôp\x000ep\x000e¢j%¢¬Á½Xtý¸¡k8Çp\x000e×]E\x0019\x0018cÑ+ë»}\x000eçÛ5ã8\x0007ª\x001eE¯É°AÝffü¢ñ)Ü
ç¸\x0011ÎA¸ä9\x0008\x001c/¸­\x0016\x001fóR\x0006×øn7â»hd4\x0001o£ÛÊM\x0018¸Æ¸\x0011oÂÔ\x0012z#Ó=\x0008WVé1?±æí\x001awâFÜIb®â1wÖ'\x001dãQc\x0013?ñyØ7þÄø\x0013\x0013,+\x0003,¸mâ§(
£Õ®EX5!ÛtÍ°ê2ÕsZ<ÕÓR\x001b-§<]FË&v@ ^ÃG\x001cù\x0004ÖJ\x001bÕ¾|\x0007ê¡Ø
aá\x001a¾1ëç¼ªÔûêcÂ¥âfç¹þãã+ôüþè6¡\x0016lJ¬\x0017··N³NÀÆwæÚøÎ\x000c\x001e}Þ\x001c"G¿´ZpÑj\x0002fTóM²m\x0018w7®âß~úð·¿\x001e>ïÄ{°ËLv"à\x0006z>ïÁ¡*Ýªß¾}ýô\x0008`\\x0003ÆnÀÎñ+w\x0001\x001c9ÚZ\x0000\x0013©¼/ì\x000cë\x001f\x0007l×m/`@Ð}dÁò\x0016èµy;z·{¨\x0002¦5`ê\x0005\x000cÖÝ\x00028p\x001fª·b§Òqv\x0002ökÀ¾\x0017°AíÐô\x0001u;Étà}7ß9|×.¯ãµÇ;ihî\x0010\x0014=\x001c«Ô\x001e\x001f«q´³tü\x000cî¯+¸×®î,nbÕ\x0015n\x001bÀ]µÁ[Maÿøp÷õÃ\x000f?|xüðîh\x001fï¢*(ÔÈÍ¥EËy¯¥Á=ÔwÏÜ}ýäù¯^?}ýl«W°ã\x001a;\x000ea\x0007\x001elÓíu¤Ûà¼j
&\x000c{k\x000fNb·kìv\x0004;¦\x001cÎjå¾¼ð0v
VßÍ>ÂIì´ÆNv÷Z½wÞÔ}Ô\x001eêR»qíÐÝ\x001aº\x001b3{¾Ú®\x0019m5»mî)KÄî×Øý Ùë\x001a\x0015§ËF.>¤=\x001dÐ¸Ã\x001aw\x0018³9EÕ°!ê\x00169²µ³7íÉ\x0011ÄÖØÓ\x0010öÉH\x001bNå°ð ªæúÆUÃ)ûu3xZæËÎ{+\x000bµg	íÞúßØ[N\x001a"%9^A}ÖD]K¾¶oÚ=QÖà\x001bR1V2É©¦7«Cä©']²{+ÜNboH	ÆX)ÚÊòp\x0012
 év´«Me%hX	Æhµo.­²\x001c¾n7í,ö`"?,cMCÁ¨ÍLKÝLð
/Á\x00181HÕÕðà¶,ÇT»Uö6\x0004ß\x0013±SÏïµ0g¸g±CúÄìödÁNb
ö8fø`j]+\x0006eÖº
\x0019âÞúæØ\x001bb1f
U·ÇÚÕ½\x0016§=¹ÌsÀ±M:\x0006ý»uµW¨,T_2&§\x000f\x0016@;3(gÁ7>\x0012|$¦ìÕÅê\x0004NfæÁÕÎÚ]íåØ7\x0015 \x0016\x0012
(±¹\x000c?ÎM÷°9î8vÜ½µ*º¼xÑ¸2ù×qtró$xÛÄv(Ì\x0011¼®\x0005_ú+@\x0002xÕ92{}Íg±7±¤\x001d%½Ai²@nª,fwV·Ù45\x000c¶§±CæW7{ãhì £\x0001Ôw~¢¾6·ìmÚ8	¾áU;Ä«9ë£Úæçü}¼\x000ftyb©\x001e»Jcw5æðÑjKRì6ÕÕMµ;5\x0007Æ\x000e<·'/=\x000c¤ÔuúûÐfBoKbcç=b¨í\x0017,ªã%e­¸s¹øâ÷½*ð0°ld@WÚ¹á\x00185wÆîjõ¼sæ$ës²G5szY]cy7fy»#IûDî.Ó×¶\x0000Ú[¸w\x0012|cy7fy¼eð'ä\x0016ðV\x001fj&R}ã%ýt\x001eôé\x0000sXY
\x001d&^Â1{ä}ã&ýtTçú\x0010Ì½`\x000f¶\x001e=âõT¸hp\x0007§Ñ2v26z½°¾.×FÜÛ\x0019v6¿¨K ÿÃÐ
¡j°\x0004Ò¥rÆÕô½Fgî ¿¤Ýß
ùË\x001cTúêq^Eþ÷êÏ´»hùl1¾é'Y
ò+¡ë.ºbmnÑR¨¢-\x001a-ÑÞVÊÓ¿«_ÀÈùÿU\x000b\x001fùê¶gèìØ\x001cíé¿MâðyÀ®ÎO
-óÅýþêâ~ÿ\x000ftq1üîß®ª\x001fÿ6tn¬ªNsC\x0004ö ýLõú\x0019þwWðÇüÎ¯\x000c?ýîñêð<þ#\x001d+§Nç×ÿÝ\x0015ü¡Ãóë_Ý«³?æòÝ³\x000fW\x0013\x0006\x001dgà÷cÉRø°ä¶@ ë^hn=\x0004ÌuÌ\x0000f0h°9/á½\x0012u¢ÈH×5	aS°°ç\x0008}u\x0006\x0007¦B\x0006Áä3\x0014~1ÿùoW7x½xPr\x0016côeÙ¤Kí~òÃÃïþpeþ?ücÝà\x001f®nðPÎ=hMwYì£Dn5U·;óÖçÍÿîÊüïþ!Ì×:£è¯\x001a,zÿñá÷ï\x001fï^üôîÃQçãsÎE²(ÂêZ2$T)ÞD{ëß\x0018ÿË\x0017ß<ùÍ§w/^>{}à\x001bpý
8ü
.AÉ\x001b#ò(¶¨ó«ð^GÚN~]\x001dþ\x0002\x0016^ý\x0002\x0016%óÍÿÅ2\x0004ÏuÂ8ÿ\x0013hý	4~\x000cÈN¾\x001fe;\x00183ñôOpëOpã¿\x0005\x0002QmÏ¿\x0006\x0015\x0001C}>çÝ	;ó=ßà×ßàÇ
,á#÷\x0019¬\x0014ûêÌbÂ#5çß\x0010×ß\x0010Ç¿Áû2V\x001cyýni8BÒÑìÒ\x0001zò\x0013Òú\x0013ÒøQrªË\x0016QÆ²«Û2Ñ\x0012Mÿ-¬Z4Ñ_·hv}C\x000eBYza#Ë\x0001,`d{JñH1ôä7´ì6NoÑx\x0019P\x000e.0VÓeoÇtÇ

»Á8½\x0005Ð\x001e¶hY~¸ðCíiOé\x00178L
;À8=\x0004Ò\x000f\x0016)\x0013\x0013ù¥´mö74ô\x0000ãü\x0010ÉH{Utä¤÷\x0017u\x0019Ü²Áõ@×ÃÉhø\x0001Æ	"ði9M¼mEI.ápöL;ºc=\x001fÑ\x0010\x00043D`íEYoã^k°º×\x001d}.XU^\x0016x\x0018ÿ\x000cîX¾ÂÇ{YåRÉ<y\x0001ÒÞò»®¯ø®ýï¿"Æzµc}ªè±(1çÏ\x0008GR ³!GSYÂ«2LWä\x0011¢èÇDËrªº6IuoßQ\x0019êû|l#\x001fÇ#ªIùXÁ)¿\x0011Ð;\x001evô'Ï|\x0006Bh\x0013Óü\x0003MLü\x0013é÷wo\x001e>½ÿéðî*Ö;å0\x0000ê LÔ\x001cç7ë19~øæÉÛ{kÝ­ÀÆ5l\x001cÍ\x0012XÔprÒ/äh©¸·üêYØv
ÛX×C¢À®N\x0008LÔ%6~s\x0004ê,nZã¦\x0011s§º¸EbIÌ]_ü3q»5n7boçuw=\x001foZÎ¦z¼·Ì³¸ý\x001a·\x001f:'u×A57\x0018RØÎÍ4wXÃ\x000eÿ8ækÜq\x0004·µÒ\x001bÌæý}Ü;VÍ=\x0011ö%u\|·\x0019ÁcJy\x000cH\L¯\x001bütûÒfçYÜó\x0011ï9^àcªÞ\x001b\x0002âè½¡ñ0â\x0006)G,åxÇZîYTc
lÜ\J{\x0016wãM`Èð¢±%+¢»¼Ùl~?»¹0t/cRÜ9ÕoIú(LôØÆ&#ÇÛqDR\x0006TBJ2\x0019ÄórNh{^ø,ðæ|ãØùÖzfè88/\x0007%*ðè¶2½³À\x0003C\x0007ÜTÏ2V}FðV\x001cá¦ÌYØÍùÆ¡óMºå:§@¦n.µN\x000fxÚ\x001c8	Ü6ÄcGÇå Ð½sÎ\x0013äëÖ(·ýx\x0016ws3íÐÍÌqØ;zN \x0016Ü¤B!9PxPls1íÈÅüuq7÷ÒÜKçð7Èl Æº´Ómê×6øºN!F×BE\x001f~Z@@%²@Î?HÃQÆ¿)Jyú^^rE\x001f\x0006°\x000e¼EÞwP|9Z\x0015­pvs¤àtpxmzÀ1Ó³\x001e¼Ì^µ1¢ý%bDó\x0019|3\x0008ÿ×\x000cÍÍgÖ\x001f4>«²éJm$É÷k¤ëÒ\x0004ëg\»Úü\x000b\x00168Íÿâçw_~úñ§\x0017¡ÁÇ\x0013Ã9\x0000-6ÆE\x0005\x0016AÖ(Ò>ù2Ü¾?½ûòíóß\x001c\x0014\x001b¬øí\x001a¿\x001dÅï×ð\x0005¿7÷¾èS£ÕñæÛ
¡½ði
Fá»¥«n\x001f,\x000f|.ðAB±x[Ì¼\x0017~\Ã£ðí²no¬Ê>\x0014ºbt7õ7º­¿º»ò\x001bà\x001f\x000c~EÐ>)þô+H?ãf£ÑÉÏà)µkÁMÕ¢ûñÇÇ»ç\x000fßøéÝÿ>{Ù\x0017¿ð-ñ ¼)ò¸Ü«¹àöÞnÅ\x000bÏs-ýË×/ýÏ}¼¸Æ½x=sNç$>`a xa+³>×®ñÚN¼[BÁ[\x0006k}B2Iî=n¹õSpi
zÍkPuÉ§¥Uk9\x000eV¤\x0014ýV\x0004s
­[£uhCR[rÞ²Ðæ¢.\x001c\x0005¬Û\\x0013}
®_Ãõ½g!©\ÎÍ=õ
I^\x0012³q·¦¬OÁk¸±\x0017nyõ\üî\x001c76ö\x000ba\x0012ØKuvñc¦\x0017­!ÓÌ\x001372,g!ÅjÜ-å²S\x001bG\x0006½\x000f/ÉáÍ´-âÒÜ\x0004#§7nµ\x0014\x0002Ü¸\x0006èõ
üìêå²\x0011\x000bÅ.xDyù¶mí>=·9¾Ð{~&µâËX\x000eNÂ:Ã\x0014À´õ6r\x00060¶ÔÖ}"H÷ü\x001c\x0016¼,Vðn5}câV}×]\x000eÆ@+ã\x0005Ù©Y=\x0016É:
ÚJ\x001bÁ×\x0001O¼ï~ºûíßþúã»÷Çà\x001a\x00168,\x0005Àüë'¡H:÷\x001fr.°ÙÍñöî·O?{±\x000f\x0016×`±\x000b,+uÂ\x0002åx^7Ð`\x0012Q@ØÓÏ\x0000k×`m\x001fXït
å£p\x000f%ÒqÒ[â\x0003mk\x001eÆJk¬ÔÕrgRq
)\x0019VX\x000c+«)}òÛk	\x000ecõk¬¾ïÄL\x000eÛu\x001eêµÑä48k6{Á\x000eck¬±\x0013«3ü\x0006Í`CZ¶ù,`»Áï\x0008Î\x001e\x0005»\x0019âJ¯õ4ZË\x000396e§LA\x001b¢ÝîÄ>¶ñ\x0005Ðç\x000cLÈ\x0011n9³nQë\x0005­êVóxþ\x001cgÐÔtË%«½g'ï\x0019ï*\x0001ºã	ö\x0018eùZGÆ0»kjpWºìÿÌ\x001dfïÞ\x001fí-#VØ.­Ü5_z³$ûIÞ\x001d\x0018·ügn,{öb£¥LAã\x001a4\x000e&îÁ_@\x0007¯ÝÇ&ªò-¯2Û®qÛ\x0011ÜÜ²RF\x000cÿ±ÀNºð+G<û
¢ÇaÓ\x001a6
ÛÊ[\Ì×®[kµao¯Ê9ÜnÛýÃÛ¯aû\x0001Ø6EnÈbØ\x0000¨
¸F×R$^4\x0011wXã\x000eC¸õçÜ4ÊÈ	:`âã¾áã°ã\x001av\x001c\x001dA= x¼÷rL\x001c\x0013äw¹¸Ó\x001aw\x001aº(c&ÃÒ0©\x0010)ùÄS\x0002-á14uqÞ
<D_÷DÒÆyÃ÷æó-ç¤fÁ­N0ÿí°\x001bo\x0002#î$;g9'¼HZd§£Q±ò\x0004~âñÆÀ;	Ihsú¢-N¦
\x0008\x0007¿Ù}\x0016wãN`Ä@ÔuW
YAà~U\x001dÙiplª¨
¸AHfMc»
&Z\x0010ÜÙëy\x000exs1qèbæ<±è\E\x0004«K\x001c×fÏÈBó7\x001e\x001cG\8\x0016grzÒ
\x0007ÁªÁig±ç)Ü¶qávÄ\x0003zR¼\x000e¸g?RçjÂBÇ·ñ÷ÈIÉÑÎÀR²°èË¸L¥2I6ÛÞÏ\x0002o"Y;\x0010Ê"Ï*â9/ØSA4\x000b ³e;¹ðIÜ\x0013·\x0003N\x001c#K0\x0012(\x001e\x0005 ×ñD\x0007ÔX\x0003o¼¸\x001dðâèAW	Å\x0018'ÍEEÆè¨1\x001dPÙ=ÛeäMÊÃÝ<ÿ3RDå\x0005éºv7Õ£B~»\x0006qêIá vtï¬sÁ ²
Ü$$w4\x0018\x0015\x0000áIõ\x0019ø!^UR2ë_º
¾øðé÷ï:X÷Y¶Ù\x000c9§
º\x000f\x0010Ô\x0001­ÛÂÌ\x0002_¼~û\x0017/·*?\x0017×x±\x001b/Jë#oX1fÁ«O\x0002[eÀS`í\x001a¬í\x0004\x001b|0w\x0003ª¨Ô\x0001mÜÚ$q
.­áR/Ü\x001c·	¼×óKr\x0011Þ0·ÁmpÌ)¼n×õâ­Ö"Ý»rv÷wÚiðk¸¾\x0013nâ\x0008oq\x000fgz\x0008<\x001a²èé´Öx¶å¶­^
O^8¶¬ æ%´$ü­Ålk¶¶ê\x001d}½\x0018ê^bÆûãÃûï³/þðñ(ÀE\x0007Îig":írL\x001b\\x0018òó'/¾Ì®øõ7û¨í\x001aµíGÍî¬¬¢MÎIq×)êm\x0000¿Õ\x0015{\x0012´[v\x0003 \x0013JXêsH$cH&$'\x001d~Ó#E\x001dÖ¨ÃÈ\x0001	"¯í³]e²ÛpAPoÏ\x000cD\x001d×¨ãÈ\x0001:XbÊ\x001bàë±ÞìÎ¡^½Ûñe4c°cm·¼ zSô$jlPã\x0000ê|\x0007Å\x0018\x000f\x0012g\x0018~0\x0017ØÛïa'aS\x0003\x0006`\x0013©§©Òå&èd\x0003¿n¥'aû\x0006¶\x001fmÿùêæ§ S9iíæBÂÐ\x000c\x0015¶õ2ôÏ6¨\x001fI£\x0000ç`ccm\x001c°6çY²WÞG#qÉ\x0011(]ßÌSÎÁv#q\x0003ÄÚÈE`
¨\x0003GÆùPÎvHas§ÃIØM0â\x0006¢\x0011^eÊ!ÉÿVYÉ\x0013~#}LÉl®¨:I6Ð~\x001cGiNÛÇïU\x00145Ç|²ÂDS9'lVANÿøø¡\x0005Ï?è÷áF53f©ggg(ï5Ù\x0019N!LGWÑ«#^¿üÃã\x001fß½_F\x0014þùÇÇO\x001f~æ9£??üþè \x0002æ0D\x001e=æ0V6\x000e%\x0011P7\x001bÊò¾~öbQøççOß¾~ÃÃFß>ùÍæ¤|]\x001dÿ\x0008\x00105Ôâç\x0005É)CQ5~Þþ%¾Ã­¿ÃMø\x000eá>\x0005ù¥§gù\x000euËw<ü\x0002ß\x0011Öß\x0011f|£úûHukÐGµhð¦êZÇw|g¨íúùõ&/ãÛÇ£Ù¢\x0007\x001dýâ§"D\x0002Q\x0015±b²7¥i\x0005ø·O7®qEk¤Ø4§\x0014²¼'ßay\x0018u0vY\x00087\x0001)­R\x0017RÜ¦X¼;iñesÅ»û\x000b7O!
k¤¡\x000b)+\x001eJJ¹¿Ô´£î´\x000côæ³Í\x0011 ËëU\x0005Â¬éÂ<G\x001fjxÁZ¨ÊmrÁ¼õ*éo®¾\x0015¨\x000béìcuk¬®\x000f«wZp·9q\x0010çìAED%k3°5ÖÐ\x00159QÒ
à>N[Z\\x000f7îapUVÏ?XÕ_ýôþç\x000f?\x001c
ú¼.¸'~)>^tX\x000föj¯^¾xóäõWûxq\x0017;ñfFhòVî©û¢|þÙ,¸´Kp³~àl^àç®%\x0015@Wg\x000b÷ñº5^××J¢HÞ¤{[2.\x0007©âÝÒJ8×¯ñú^¼ä¸%\ñJØÿPñîÔª\x001fßF?3\ÕªOÞº|,p{Cjé)F³3X¶ú»\x001c\x001e5Ií\x0017ù\x0007KRûÅO?ÿ¯O<|÷åãw?¿{üp4$\x000b\x001cÙDQ£Ðg¢üßÑþ,goö\x000b}ñòÍ¿¾}ÊóÈw_>}ýìMþùVP	×
ÐÊÃ}õé»Ã*\x0008.êdÌ»\x000eÙÁì[U=6õWo¿ØoP°¸\x0006`3¤ò0KÑé\x001bFÂDÄÎÇ½ñ²£`í\x001a¬í\x0003Ë=c¥^à¸Ö»^2`üÖ
¹3h¯j\x0005t©\x0015·°Ua	âÕRR"#k}¤-µ¦# sPÒ\x0012\x001c¥¬3"~°õÓ»÷\x001f\x000f>×\x000f¾
c¹ÄZÔ<ò å$¾v;1ey°õòÙo¶ÔuÃµ°Xý\x0007G­ò	ß½\x0005xRù\x001a7å¿{¯´ðCÑÂ\x001fÎÝìÒiC$ôt\x0015z¸)àq\x000eyºåR\×d>-ª\x00119\x0006:s	èÃK@ÐÓ`¤ÛÍÆÝ\x001aÆÛE.âÿÙGkÄø\x000føR^\x0010û^È9 f-¢i\x0004ÒücWBöfóéaÈHW\x0004ÀÇâÕ\x000fß/=?9#ýáÓÁq\x000bè¤\x001dk)÷ÆK/¡\x001ce{{µÆ«çO¾\ú}rVúÕÛq\x0005kÀØ
»MQ\x0000{B³\x001bÔi\x0018kn\x000e\x001fE|égcÄ\#î\x000cZÂå½>¡ÔR¼WÕE7_X\x000eCÖ*Å¼É­j¯?}xøñî«w\x001fÅß}ùéÇ¿ýõq)Á=ÿéÓ\x000eÓzm\x000e\x000bÎq;þÂêIX=ámh>Þw¯ß¾~òüî«gß°\x0002ÍÓ§K\x0015îùË·¯Þüï\x001f~xøùãÇúú]þzâÎ/µ·'~|_[Ü~ópXÌ×ø"#/\x0015.c\x0004Hg×\x000cÝTÅxòíÓ\x0017µÃí7O^?ÝGkÔ8:\x001b[7°ó¼\x0019Ñcäæð[IA\x0007j»Fm\x0007P
\x00055q.¶ FÑÈHK<1
5­QÓ\x0000joÕc0uò\x0001êÖõx³FÛ:®QÇ\x0011[{UåÊÿ¤´m¢±ºn:ÜìÁ?\x000fzÕVáË8t7êh¤\x0004\x0012øuH¿¬W[\x0007gkhn#\Ç\x0018´ää$EÇìquË¢¿)£Û\x0001»9Ø0r²ÓòvU`\x001bNx¦G·ëúû:`»\x0006¶ëMÉê"{¶E³8©Þ\ºÝÚÚ7¨ý\x0000êÌô"Î\x0015\x001dyµÚèèæÀZ\x0007ìÐÀ\x000eý°¹íP6ïb.°YSæfûl\x0007ìÆûÁû\x000bfyùaØ\x0014º?J+dü·¢Â\x000eØ©\x0006¬^T¤\x0002²0\x0013
W]»±±Ùî<llÜ6\x000e¸í`\x0006Q<Ç#;BóVkç0|\x001eì&ôÃØÏ\x0011ÊÆ±`û\x0010½¥ì³æÅ#ØÆ~\x0003l\x0013À«Ûv\x0014XÓo)­>ØZ\x001d°\x001b¶Á\x0001¶	9\x0014­yÇ\x000bÆdi# \x0016xn/ìÝ°
\x000e°óIe­¥ª\x0008>|ßñêÝÐ
\x000eÐM@Ð³íS5h\x0007òÄ©Ù­rZ\x0007ìnpnX\¾øíL=º´¾Ù%s[¸\x0003vC78B7ò>\x001e\Îl$\x001fs eWô7ë<\x001d°\x001bºÁ\x0011ºI¾ZÛ1rK¢:Àpó\x0005ï<lÛÐ\x001d¡\x001b$\x0011Çw9\x0014Ý\x000fNå³\x0012y\x001ci\x001b²±\x0003dã1jügSb¡ºÅÖ*ÅÀÜìQêÝ\x001d!\x001bt²\x001e5xæH9ÙµVuS«¬\x0003v[i\x0018(5xºòÝ\x00145v\x0002\x0015\x0007¼YïÝp¤\x001dáÈ\x0019ÅÆÜ\x000eÌm,ÅÚº\x0007\x000cÓM\x0005¨\x000eØ
ÙØ\x0011²qæ>nÊú²e·Ý\x0002ìLk7^Ûxm§/¨¬¶Å/¿åZÎ\x0008ÍKl¨q#4âFØe\x0017Sóx`yHEêü ynûH\x0003÷·]K\x001aé×½¬\x0017*°ÓÄz\x00145Á\x001f
\x0004ÿøÙw
Ëkj­Ï!x³_¹\x0003u\x0013DÑ@\x0010ÅÉ¯\x0011ÇîÄØI\x00058p*ì&\x001a¡h$(=\x0002ËcÕ]\x0005OnJMí\x001bé\x0006ndÈÄÚ!hòëÀæØob\x0010å\x001ak»\x0011kçót¡ê"íXBÖTWNNËk\x001aE\x0005¯
#ì\x000c\x0006.±¶
Vñ\x0003ëw&(ïL¯\x001e?¾ûøxÇÓ\x001b¯Êÿ>ê¸ÒNDëøýo9ÝuõWt7a¿zúÍ³oÞñøÆ«ò¿÷q»5n7=wÉcÎz5\x0000¤\x0014UÍÜ-gÒ;¬q\x0011Ü\x0010D¯*
\x0007Ëq«xîxozP§5ê4Tl0Øu¼öE{sÒ±\x00036´{ät\x0007ô²Ç#"8Ñ|B§;l2ðeâ3Àñj°j(¹¼jó\x000fNµâ³v7DYd\x000b,Ò®×AÕS6¿l/ù»\x0011Ö\x0011¦|\x0006é\x001a\x0018ÈIrÙ\x0007\x0017ë6[>¦ë3ÜÒ7\x001a.¿Ì£áòëøêoýÓÃ||ÿ1Ð·Ò,ñçwï¾ûÛÿá\x0005ì?|xüÓ§ãªøZ£L¹û*.FR³Þn,eßÿên\x0019øöÙ7¼ý«×O_½}¶Ñq _\x0019aý\x0011~Ù¯tºY$,ã¶|eò:ä`«\x0019nà+Cóá\x0017þJÕîÏDîÅÙå¯¤:×}3à\x001bûÊÔü.Ó/ý»t2àSò\x0006¼YA¾ÒÞ$Ðî¯ôm\x0007\x0004rñß¸oß=~úßÅÉüð_ÿñ/ÿpø£òå\x0013\x0019¹\x00154
­Zy·µË?ó4ßþÏâl¾º{ùÛ#å×åç~G~½_\x0004éXï\\x001e²¨L¸d\x0016¸¹cdø«Âú«þ;.èÿ*\x0017L\x0019æ|\x001b¥ÌëE\x000cn÷8
VZVüY¢ÌòY^U¾øñK~YàöúAOÖw\x0010¡Ég¾È?|æÕw\x001fÞ-"õ«¹y|8Ø\x0016Hìô­P\x001b+Q.½¢Öâ'ÜMÝãW¯<{ýlÑ«_ÍNüËÓ'/n|ûÝÂ¿(\x0019N3ØÍ¿\x000füé=\x001c6\x0015ÔNQ¿yà¶èúâñýO9NdØÖsSTXî\x000cp÷ó²ÿ/g¿\x0012rX®ÅVÜÿôæ	÷8ÿÓ\x0017O_¼ÌAßªÿùÛü1Ù·Ý\x001agl\x0010gÏ#M\x0001kÎ@Z\x0010\x001boH ûU4\x0007r6\x0001
Aö\x001ei\x0005¯.÷³6Ç\¼Ù­ú!¼lW[ðF,«c\v4 ÝJTz\x000eâ|9â?À1öÿß_þýßÿ}uñþõÓÃ»¥\x0008ÂÎïÝÏ\x0007ñ:\x001bë!¦\x001c\x0013#[\x0012xép¡LU·\x000fÅ¿¾}òl)Ü½|öæÖÈA\x0003¶Ü¹^°¼Ö¢Þ\x0001a,Ã\x001d\x0019l\x0014Q÷ü·Wï£ã`3Ù\x0001Ë&Uà\x0003~;r(M\x0015,Ì\x0004[\C·e	EÞ\x001aÈÙ²âxy¬\x0013°1`ó­u#Ç\x0000DÅ5[Öß§bØ\x0010ôÈz7\x0013kñ\x0008½X]ÎHJO\x0013pé?\x0014°\x0005,P¼íÂNå¦YþO7Z\x0004yï\x0004î!KTÐ´{\x00108ºMi\x0007ÑþÅýÑýå/+oðìzøùç¥ûüîÉ§ï\x001e?¼øôÃQÌÄ{KÍ\x0008¬qâÁø½VhmQ\x000c¿ùÙ×¯¼ySj¹wOÞ~ñôõ'o¿zú?\x001e>|ÿø§òÿ~\x000e»øQØä¥×a\x0017Ì¢æ»`\x0000Ù~LüðÿJ\x001fÓÒ½ôôû\x001f?eÈ9<]\x001dÅºlB+®,\x001bö¾À¨#Sd#ÜÆûôËço\x0019î]ùÛÿ
ÎµÀªJ^~ "\x001cùÞýËÃ§\x000fû¿?\x001fv½¤Ú
Ë¦¼T\¯á§ØÅ¼n-¬}+\x001côÞýË··7\x0018¯Pã\x001a5ö£æa\x000cgÔ¡¬Æ"V/¿ ¶óPÛ5j;`ën &âÞÅ\x001b\x001bMËÛÞ¾~§QÓ\x001a5ØZëÙÖÈ»¦\x0016[´ÑäÀÞÓN£vkÔnÀÖ^Ã\x0018\x001eÊ\x000515È3rvß\x001b	ÇiÐ~
Ú\x000f;SA#LïÅÔ
\x001a&b\x000ekÌaÄÐZê0<\x0014\x001fÊU\x0004Ô0Þ9{;Ä8:®QÇ\x0011KLà6q Ò¬d) Ó\x001at\x001añ\x001f^&EM´ÿXü< ç Üæ³¨eÄH\x0019Æ\x000cÀ\x0006#/leâQ(Â^k \x000eÃnq\x0019£ÔÊ3lË\x000fT\x0019euf¢\x000b\x0019a\x001a-x©Ñe\x001fbø\x0019ví¨:\x0011w´¡¡F\x0018åF1¶áNr´½\x00113\x001a¡¡F\x0018àFkC5¶Éia¹FWzó\x0019¹²Ýp#£KÒª½_àFÂÂ2`iÝz,t\x0018vÃ0@6gÞ.ÕC\x0012õF
{õä=\x000c»!H\x0018bH+óò¬hÎ}bÅÚ2ÏÉ&N´vÃ0@9\x0011\x0015¤\x000c;\x0016]\x0013¶¶\x000fjí\x001aèiØ
GÂ\x0008IffG	²¹Y¤¤ÔîÖ²£°±!I\x001c!I\x0007\x001bð!qê\x0000ñrHæåaØ$d¶¶Wk/çE¬]\x001dàÄ³mú8B9*-VKøgj$\x0005jm?ÏocC8BÙÚAó\x0003d\x0005bm«!	Lµ±aI\x001caIV&\x0013c\x001bN\x0016ÿ%ËÙØ4Ï`C8Bù\x001a\x001a
¤\x0016{1¶²ÍD7ÒP$P$OA±µ_z\x001e\x0017Ð*\x001b}:L<Ø
Eâ\x0000EòJT¡Èh¿ Ô©Am=1úÃ!q!\x001dÊ¢#\x0013Ðpïølq~da^<
Câ\x0000Cjë¸	¹XÕ-ÍÃl\x001bz´Côè¥\x0005Ùp7²uê°5a·\x001bëÓ°\x001bz´\x0003ô¸ìi\x0017m\x0017ýbíÖX;/õµ
=Ú\x0011zô9)Ææ\x0019\x000c
X5\x0014\x0008¹-­\x000eP#¿wjEØÚJ¡fëvãýû4ì\x001aí\x00105&yL4<÷ä`¨¶ÞxÞ8
»áF;Àc=\x001d-²´Fy]^ùë^¤aG;È^\x000e¶]ª\x000b;j%ÈN<$
;Ú\x0011vä\x0014à=«ð-¨Õ\x000eú7²aG;Â!IE'ðZ\x001e¹\x0004\x001abSx²\x001br´#ä\x0008å$±A_; &}£ÁV³°©áG\x001aáÇ\x00082Xi\x0002YV¨(ÖÖ\x0010ÛM¼ÔÐ#Ð#Ö\x0000+ÃT²Gäêä3\x0013ëPÔÐ#Ðc´Ïd(!\x0014I«øÒ\x00020
tC4B<µíØ\x001a/åì°ÛÇÇ\x0011LFDj
¿§{¹N«P\x0014ÒÄûØ\x0010$\x0010äådsñLÎ\x0008\x001a\x0013ku"ì i ½oÙÚ0Û;
³ÃF×ØiØ
AÒPú¸zÍsõa,¸Kñl\x001eCRÃ4ÀõzÉÕ\x0013wa\x0014ÔzF(Ì\x000bF¨!H\x001a"HPZOXC¨¨¾/¹yÍ\x0000®¡G7@djKð¾\x0016U\x00158zâ£køÑ
¦¿Ú¹v
Õ¸\x0011ªáwÇEGÅØÑiä\x0017g¢n\x001bFF\vé9,g¤¾åAªgÄ§)%õsùAíßúéÇw'ÚPAÞ9ûãäyWH_\²;ñõËçÏn·\x001eV ¸\x0006]@sTpr	Dp¨EÛ\x0014q
N»Æi{p²¤\x0015:îD-@¥¡3\x001b\x0014wí1 ´\x0006J]@±ÌYgz\x001eZ,8µdâ^æ\x0018N·ÆéºpF\x001e^/\x0006õºA7:dO\x0000õk ¾\x000bhm<¶9Uu\x0012¬9«m±ÑO\x0001\x001aÖ@C\x000fPÉä:ËºE\x000bÐ C\x001eÍ\x000cà\x0000Ð¸\x0006\x001a{zý\x000cùWoï%¯ó¦dvÒÑc8Ó\x001agê2hÐ&n\x001e\x001aVþ(ïi´´ã\·R¹K+Õéß|õMÒB¡Ú\x0013§àlI©¢
sUí^nÎMQ£¦:\x0000´!%èb¥82)@½Ö¸-ÈÛ
-í6\x00136´\x0004]¼ÄKÚ@ý²y¡ ­g4Íp÷ÐÐ\x0012tñR´Õ2üò«sÚ	±álh	zxÉÓ\x0016}¯\x0015êSÛ	ô!mx	zÉ¡þÞV>,Ig>) \x001bN\x001eRÊ4)ýáÙQ[i­G5'îµ-\x001fCÚ\x0012ô°\x0012ë yùÅ{Ãû»\x0016¤º\x001eí¸ãH±q÷Øãî\x001dº{íY\x000cW®<%uN{
³Çp6î\x001e{Ü½Ë\x0013 ¼x§¼\x0013;è\x0002t÷±ð\x0018ÒÆb\x0017eQa
Ó6õ©êm²{­cH\x001b÷=î\x0017ÔD\x0019eu÷Ô9ýåoMò@Ú¸'ìrOîòÛæ^Ni\x000cúËGqñ±qQØã¢|þå\x0017ä£zR§[\x0017ò!\x0019ÔÂ.\x000f¨	åS\x001a´H_÷½æS\x001agx(Ûx(Ûå¡"ÜÿróCñ¥¤eøæÏ\x0000Ú\x0004z¶'ÐcUWÐë\x0004¼|}\x0001Ê:ËröÚX!mâ'Û\x0013?ñÆ\¡'²Û]cjê}
fMo{.>+ëy¹P\x00144\x001dq5mÚ«ï\x001dtPu¯äÅIÉbÉ³¾?Ö\x0008%æT_Îª©ãå¸1X|\x00000iKeù\x0007Z*[ðÜ}ýðáã»÷ÇÍ«IX{´\x001cÖ©\x0002Üia^~t÷õ×ß<»µ°l\x0005Û®aÛ\x0001Ø9ú#á\x0008¨íùÎ\x0005\x001dÊô\x001b\x000eçaÓ\x001a6À¶u\x00026xÞ\x0016v¨°w\x0012s°Ý\x001a¶\x001bíë!ñî\x0002»Îù¸Ñs°Ã\x001av\x0018³vÒqÁ¨\x00039'Óö|·Ó\x0011w\x000evZÃN\x0003°9\x0010Ø<\x0017QÂGGN\x001bh&ìK!ak!¦\x000f·\x0017\x0015¥\x00011\x0008lséèI ñ$0âJ¼­X'¥]mcÞ9>»¹0r)Yß\\ Ô~Ogv×Ý\x000eÏán.%ÜJç92*Í!ß\x001c\x000bã\x0004µ·Ù8Ûxsõøå>~\x0004ÇÓßÿxB\x0003ãÒëÄÌÎpôT\x0006¦EÒ¦.E\x0018âéoopTÔ¸F#¨À9`ö"\x0010\x0002é»ÝtÁ)ÌvÙ`öA\x001c`¶tÚILIOvÚi0;Ú­Q»!ÔÈ\x0005©\x0005µ×EÔWQÇmn?\x0005;¬a¡\x0003\x0012ë±ÎÜQÎH¨gd§\x0000t
vZÃNC°¥/\x000eÓ"Æ\x000e:pg<ó\x000cjh}È\x0013É\x001eå\x0004à'Ë\x0005·¯Æö\x0013a7\x0017\x0012n$OÃÚêHJbË*ò^qï<\x0006ÂÝ\I\x0018º9·-s¥\x0019w\x0012Å\x0008õìM ÂÝÜI\x0018ºd\x0004\x00050ÙzLtÁ«M4ó4\x0012Fn%ä´,ÈñæJM±wôÊí\x0019÷v,u\x000676×\x0012G®%Ð¢bXp
Æ\x0008J8´S¬?wLZC9*ZkèC¼ô­.è\x000bËó²~ÂålW&¸º2aAýéî?¼ûñøã\x0013µ\x000b`è>êË­¤9YÛ1÷[ÖG}¾\x000f\x0016×`±\x000f,\x000f\x0014#
\x001e\x0018÷\x0002¶jÎÄì\x0010çµk°¶Ó²\x0017\x001d-`3¯Ëø+&¸;o÷±Ò\x001a+õa½Tô!ÇÓFµ\x000b#øxé(X·\x0006ëºÀ:Z\x0004nÛ	ò0®ÝÑLÂê×X}a=º\x000c5
wäÀÂª]÷´d\x000ec
k¬¡Ï®\x00002´ÁBmÀ¨R²i§ãà0Ø¸\x0006\x001bû\x000cC\x0008\x0005¤R&9ò
vÒíJk¬©Ï°h4¬\x0007´ª¨¡]f!í°\x001ezi7\x0002i7:k×$F5^[a-T¹æ°#u\x0018jË\}ÔåP\x0005ê ÓAÕ
uZä
q/À9¶¡.èã®\x001cÿjJj"i©Å,\x001c´ag\x000cç0Øº »²ßªºÝ\Ò\x0010\x001e\x0004Úy5?¶!/èc/Þ.]f÷ò©õZ[æ]Ùvgì0Ú½ ¾H÷|IõU:Ô0é\x001c4ì\x0005}ôÅÝ\x0013Bµ@å¹H'U\x0002L
\x000e¡¡/èä/îízÃäeÄ&­Õç\x001b¶\x0013{\x001fEÛð\x0017ô\x0011KAcÙ|®îÅ²¤â(>í4£\x001d\x0006Û\x0010\x0018t2XN õÌZ£:\x001ddUwÐ¦ ÅÃ°Ã|&2_Åk`ä=T\x0002ÔIÞ\x0000\x001b\x0012ÃN\x0012U¨ÅðEª\x001a~Ú©.\x001cEÛæ_}$æ!HIÉÕ> Ú8~½\x0013u\x0008mÃbØÉbä\x0017Cõ´Te¯\x0003Nr_Ø°\x0018ö±çåyå-&q¿¯¾Å¨¶§9¤Ãh\x001b\x0016Ã>\x0016ó9>\x001d\x000edt±J{\x0006cÃbØÇb>\x0013¼='ç/¯:>áwÚ*\x000emX\x000cûXÌ£vüó9ËeÚYÎl\x0013yaCbØGbÙ`Lö¯\x001a&º:ä-M¢Ä°Ä<øû\x0015¹+ßÅý\x0014SÀÚÃl'E§º69IÐ!ªlpõ\x0006¸Ó»x\x0018mÃb¶Å<$Ý:bÓY\x0005
*à£ã»lÃb¶År¾x_Dl\x0012\x0018Í\x001b½Ñ¢_Ö\x0017Ì\x0000ÛV\x0011ûHÌ»PS1³B\x000bI-»W\x000e?
¶á0ÛÇaå\x000fJÿF2F«2\x001e¢ª¨¤ÁªÃh\x001b^°}¼\x0010²
±¶RX|fK+Õ¤SÛ\x0010í#$c6ùØFNx\x0017´zj'Q®mÁö\x0011C4\x0007¦öM\x0005{Q\x001dÙ{4;¶a\x0006ÛÇ\x000cùÿò³u9¶AyÌÛÚÁÂv\x001bÌQ´ÔP\x0003õQ\x0003KZ¨\x001a#r\x0010\x0002UùÁ4'¿¡\x0019¨\x0019¶EñÜ]1+EígÝÚt
iÃ
ÔÇ
¼y!ªt\x000bêÀzpÚÆ@{õÑ6´@}´\x0010½7²è"&NÊï\x0002õ´qgÔö0Úöy©\x0017bÎ\x0011Ê\x0006¥Ü\x0010«´`ØiÆ?¶Ém¨/·a\x0019\x0008¦ÏP_î|Ð1f7«@
Q\x001fE·´/¶å\x0014²TâEAÚMz»£Å¨Å\x0002ÊN§Ì¹Aj}Ú\x0007ìgÙ¶¡1ê¤± 3Yp mµeh¯Ïð(ØÅ¨Å"¨\x00060odÂbá¢ªæ&¡u
1¸NbÈ^K\x001bÂÉékcª×>Ë¶®q·®ÓÝ¦T­E®Ó,h±öãN×ýa´í\x0003y\x0003Fû\x0008\x00171Cu·¶.YhsëúÎ-«lkÓ·±:?óºp`GÝü(Zß[ßwn£[	Ó¡Î¤íw4ë!ÏÒï>>~¸JÊø']Q
ûÆhôeÄSmó\x000e;\x0013'0¯ú©\x0004sí§ú;Å\x001c>Ã\x001cº1c,\x0012=9E³ÚLå±\x0016mÇ0ãU'}þÁªóëÕOï~üt\x0014¬Í	¥6dæ\x0018B÷3ùX[»w\x0006ø3ÚW/=»\x000f\x0017×p±\x0013nvj¶¢®\x001fÃ\x000fÑvG¦é8Z»Fk;ÑælB»/yTR×1¥:¡°×\x0008x\x0018.­áR\x001f\Qvu\x0001r\x0001Zö¢¦jKÿå\x001c¸n
×õZ×\x0014\x0016ÚXW\x0013f7,h÷óÊ`ý\x001a¬ïµ-Ôm\x0013t\x000c·\x000bZ¿ßWu\x0010nXÃ
pb\x0008 ÔqNµ\x00170ìð\x000e¢k´±\x0013mð÷Ú²Ä/ê²­¨f?Ñï\x0017s\x000fÂMk¸ià,Hïb\x000c*Hiê\x0002¸'Ø|\x0018îª\x001b)Âtâõºè\x000c \x0004\x0019l)ª\x001b´3Hx\x001coKiÆÇAõ!¸º¼¯ª\x001dóÜÿ$¼
§A'©¡\x0007\x0015y\x0002Dé3ÛWË8\x0011÷\x001fN\x000eâmX
:i
YÄ¾FÔóiÐ}\x001cqooÁq¼
­A/¯¹P[/)rÅL¦îôüN»n
­A'¯aÎ(ä\x001d
XûI¶ÙD;¡!6èe¶\x00126\x0016ëZéiÌÖ­·
vÄÔãm
z©ÍÛËi°ò\x0004ÌcÊÄ°ß{\x0010oÃmÐKnN\x0019\x0003X~».óiúv Â{\x0010lÃlÐKm.©\x0004 ·\x000e¸\x0006½j{ÒçñbCmØKm\x0019\x0008Ä@NÛ@Í[û\x0001ÒÎ¢ãx\x001bjÃ^jãYm¹lèD£}5@¼ æàm¨\x0002{©Â\x0011·ºöìp:\x0015ªp÷Ô Ãm\x0002{Â&©\x0002ðø2g´\x0011/¸Yx\x001bß½¾\x0017Ù t»\x0006i\x001cäqJµ¯ß\x0015>·ñ½Øë{ÉÖ~×è«ïuîw\x0012ÜÆa¯7³Õ;\x0018\x001fïe\x00124N\x000f´£a|\x0018®míufh+\
5D]\x0011p¿*y\x0010oãÌl¯3ã×\x0014éjá}Û¤§Wí;ÒËÇñ6qºíÓ\x0011î/}ðI\x0003RíÊÛµ:\x0008·->õú^\x000buØÄ\x0006y·ÉÆÚ¹ß~q\x0010oã|m¯óÍæ\x000b^'dQ¯2ÞYömâtÛ\x001b§cª\x0013'\x0018¤tíëj?|eß,l/Yð\x0004àµ(}YÙ¾¨xa¿0}\x0010oC\x0016¶,r@¦æ5R1Ëæ­MñfVÚf8ÝöÆé´ªc\x0018¹\x001e_¨ÇaÖém¸Íör[9²:z¢·­6gñß\x001ar£^rãv7/æu5ÍÄ\x001aJî­°:·!7ê%7ô÷ Ç\x0017Lq±ª,ç÷dÛãmÈzÉ-çérÝTÀ\x0005Rµï¬ jØzÙ
/\x0012IUÂë\x0014Ê~'÷A¼íÛJ/»AÍÜQ/9\x000fPÛäÓ~ëæA¼
»Q/»ew\x0006ÒÖ\x001f]UA§ôaVå\x001av£^v+N¬´H'Yíëª}g¡¨a7êe·|ß¤I:JÆÚ\x000bçýÆÝq´
¹Q7¹]\x0006­u\x0012°'zû\x000fâmØzÙ-ß6§æ¥*´\x0006º{Ù»ýþØcx]Ãn®Ýt na\x0002ÖÔaÅýN`\x001bjs½ÔV\x000fI>È¨5\x001f\x0006pv\x0016ÞÚ\7µ\x0001/a,öEy×É¤êÊö5\x0002\x000eâm¨ÍõR[¶¯Nt\x000f5¯Âv$ãm¨ÍuS©cJ1ÞËñ5*Èãä\x001b\Û6ÐÍlúÜ¶L\x0002W|h\x0016ÞÙ\/³\x0019¸È'Ö×<Óh'²÷³"3×0ëf6S#\x0007\x0007µ¬cô
ÀÛi¾·á6×ËmÆU¼E,¼àÕeÕÞMºm¾¡
ßK\x0015\x00065pp\x000fr\x0011\x0017S_F;ûÀ£m¸Â÷r\x0005ÒÈp(J[']Ò÷Ç)\x000e¢mÂw2\x0005¤xq
F:\x0007"'ñ
7Nb6ß0ïe
ã+^\x001be\e%Kè\x000f\x000c
\x001fÄÛ0ïd
îÎAIÚX\x0001¥¸ÞX;IüÞÊãx\x001bªð½T]\x0003é\x0000n\x000ezTö\x0011*pGÒù8Þ¶É¬*\x0017Åê\x0005ËäØ7T¼q\x0016Þ*|/Uä\BfÃ\x0012zéáü\x0018/x\x000fH\x0008\x001cÄÛPï¤
n'Òãàµ¦£ë=Îj{ñM\x000eä{s \x0003¢ÛcRNæËLP6nÍaÖã`h-t\x0012\x001bÄ¤¸	Q+$1¤z\x0018f]¶ÐP[è¤6&\x000bñ½9¢$§\x0015Úç=+\x000f
·^nNvwgÒÑ­[©ÂÌªGÚB'µA¢ªJÖ÷òeÓÑ ]ÑñÃx\x001bj\x000b½ÔÆjôrzs¦Ç!Ôm\x000b{ËÑãm¨-tR\x001bäLØ VxÒc¬ÃÙÓºâBCm¡Ú¢ê5Ä|2Jç?\x000b\x0019+Ú}í©hÛöéNbãË&YdõÏ¤·­N8Îj2\x000b
±nb\x001añi°ª\x0013mëaD\x0015±¡ØK\x0015eú=æ?Jõ4:÷: òv\x0010nãzc¯ëõ^§x7ª\x00101i1ÒÑ¾¼×A¸+½®Nb]K\ZðÖ
T&y²ØxØë\x0019ã\x0003ëuï¸\x0006«3ûînñ1¼©9
©ó4\x0018\x00164/wÍeÒ(®!XÍà-ì,w=\x000e·9
©ó4,2ØóRÝ\x000b¨)\x001bÆYï®ùë\x0019¼Âm«\x0019¼¿Wz\x000bÁ\x000eÝ°mNèE	\x0010­Óªl\x001djÚ\x0017ÓÚ]p;=È>ù\x0012\x0002ÿæñýã\x001fï?~ÿããï\x000f'\x001bN}Æ²R;XíSÖåÜt³\x0003ü7O_<}ýäùÝó§_>úúËýOÀõ'àð'PUh¶äe¼;§Kº
äéO]\x001dþ\x0002\x001f´ÛÖr+¾N\x000eú	û
\x001b§?Ö@ãçHöôÚ(s\Ü.¬Ã¨q¿'å4~·ÆïñçpD7²'WÙeÖB>aÿÙüô'øõ'øñS\x0014u%EsÙö¤}bìR§BXB\x0018þ"LiÑä\x0001§b	ªé\x001f\x0010×\x001f\x0010Ç?\x0000¸lù\x0002S\x0017<\x001a¨7Ùí\x0017ÆNBZB\x001aÿTÝ)\¦ðP_µß/ýË¼ãBjfü\x001bªCÅ\x0014/+æ:¤½ýÁ=ßÐ\x0012ó83'/P>JIÅDÕçÎä÷§!OCÃÌ0NÍ5+k$,ªÍ^Üt\x0004
7Ã09[\x001e(\x0011fàÊ¬x%Ô+¹}ÓßÐ3³s
ÚÔ\x001cUB­ìF;[ª{¾¡!h\x0018fhË¢\x001c2´»"\x0019w9Kûéíéoh\x0018\x001a)Úr\x000f\x0008K°.JÐ³¤Â\x0012\x00074wOCCÑ0ÌÑÌÌ2UÎl\x0017«ò%û\x000bÜé¥a¦-¡È®\x0001\x0016\x001dÑå\x001b\x0012é7ýÊÎéohh\x001ayÚRî¨e¹§ÈúÑ\x0019²¥rò7`ÃÓ8ÌÓÖcÝÓfWî4TÙô¸¿\x0008èô'44Ã4ÿ«\x0014å×PßÁÔ+}àµîô7´	ô0MÛ.ª!AåÜêR®0?jÅ¦q¦½©\x0015\x0018Öì)®\x0015@KËi~´
Kã0Kg×Y\x0019Îx¾ÜË'øªwÀ\x0002â³¿¡ai\x001cgi\x0016Ð\x001b\x001d5jÍ9µNé§ý>§ÓßÐ°4\x000e³4\x0019y²\x0002~*\x001c\x000e«?¿ÀQjH\x001aÇI7¬IàÍãnVo´:Ö¸?eqú\x001b\x001aÆa& Uáâg9\x0011DU\x000ef¿©ëô74$ã$\MDóçD!i}þa_Hìì'Øàì0ÁQf\x0004Ht\x000fBp©JC¸5ó]\x0004×¬v-$·ªÍ÷þ6¢\x0015%cà&\x001bÑu\x0003gªÞÔ/Pì¶×b'|É¢'¡5ïP§|×âÀ\x0001=Ã_\x0002Æµ/\x000fù\x0007úòðêáç>\x001cÄMÄ-,Ä9i|\x000c!éhþ²\x001ba\x000b÷«'o¾yúöõ>X»\x0006kûÀâ%kÎ	tY\x0014"*¥\x0006ãÃXiú°f¦2±fø¥ø\x001b.S¬9;\x0004Ö­Áº.°\x000e¢.{³$H\x0008ÉÕÂÖvp\x0018ª_Cõ}P¹³\\F"\x001dOËÉ;XI<\x000c6®ÁÆ.°>S½U°I\x0003ê\x0006ÐE¯c
Ö´Æ:
[_L\x0017qP+Õ\x001dz9NÜf÷£`¡u[}~ËÕ®6°\x0000ªíeÜ\x0005í&Ãa´Ø Å.´¬Äì ,¥]ÛÖêÛÁ\x000fm,ôyYÏ=£òxÈjøåÐ$á6-\x0013
SÐ6n\x0016úül´\x001f\x0007ËA\x0008:i`Så°\x001c\x001cFÛøYès´Ã\x0005-N("ú¢¶Ópu\x0018mãj¡Ï×ò¢	\x000cÕ¶o\x0019äÅ¶ÛÕÑÃhC6ôÙé@[¶\x001dX««¡SÜé\x0007:¶a\x0006è£H©\x0004`-f\x0006KP_è\x0003L:\x0008
5@\x001f7\x0004É7,:æXÎ¬¯owaG{ì(Ô\x0012¹¬+=k×\x0000ªÃm!±ÒÅbØz¿vt­\x000fcmH\x000cûHO¬\x001a6©üçê¼îèS\x001eÆÚP\x0018vRX×f\x0006Qe!§mï»½\x0000Ñ6\x001c}\x001c\x0016rz \x001a2Ö\x001aYèM«µÇ¸Ó5|\x0018lCaØIa¼YU\x001d\x0017j·\x0011\x0005¬vgë0ÚÂ°Â¢1\x0015-Vc\x0019\x001dªgÛÂ°ÂRNg|¨¶\x0015­1ªýî)ìl>¶¡0ì£°h<ï\x0017QÛJ;¶­õlÛ9186\x0014}\x0014ÆÃP"·\x00043Å¶ÎÔ%\x0002{*Ñ6\x001c}\x001c&-ÍÚP&#rÖë\x0008bvÎ-³
Ù>\x001aKDö7]«\x0019\x001dA=	;³êÑ6Dfû,bÝlÏh\x0004±vºMCÛPí£2\x001eN¯T\x0016UÆ"ÿª¿Ýyl>¶­yõQYÌU\x001epr,«y¹µ6Ò\x001c`\x001b.³}\ÆÂ
"¤Ê¶ ÜÕ^IP\x001b"³Dæ¬l¡â×0%2ªBGÙ!L:\x0006
ÙN"KÙg­\x001cBq_ØôMBÛ\x0010í$²|ÅÔ!ð>2\x0016­Nê¤4vmCd¶È\Îîã\x0019÷ZvB+ëNbÇl'Å$2æÜÚ]^"yWÃ¯G¸£`©¡1ê¢1så\x001a"dç%º
j>\x0016wzõ\x000e£mhúh·,k-§þÅ#DSm»#¸r\x0018mCcÔEcÎ¿'_Ñ\x0006|ñ.IÎN³Îa´ísH\x001718½­õõ%[ïØÎ£åa°
5P\x001f5ð&s-yPÎq¤¨º¯IEEj¨:©¢¬ü+hs©RCô~C
5P\x001f5$\x0008êl	TÖ±¢ÖLò\x0008
3P\x001f3ð\x0004gPÓF¿»ÒNëýa°
3P\x001f3¤\x000c8÷Sæ½è0ÔSsN­k¨ÁõQ\x0003·è©uU8=¦IeE×Pë¤\x001cÐ@gD¶Ñ]nØNða¬
1¸>b\x001c*F¨õªøà.C\x000c®Éo\_~T
f±,yI\x0018\¨¦Ã¹®a1×Çbhê\x00086­¼%i¶iÛWýN\x001aauhE·Æ:¾v\x000emXÌu±Ø¢ª®ã5\x000eêÊ\x0010¬W,ÍÉ\x0018\Cb®Ä\x001c+\x000fëh\x001fo\\x0000k/¦Ý¬?¶a1×ÇbË ¢ÄµÞ«®\x0019#³·¨é0ØÅ\\x00179¾¥e1ÀbZW+¶³®oXÌ÷±\x0018O³i\x001d\x0019è\x0000ÄµÙ¶J\x001e¾a1ßÅbÎppñ^\x0005ºÜ±9ë\x001b\x001aó}4f/BÔK?¼lwt\x0012ÎÙÓ;¶¡1ßEc9MõÝvKQ1¬íÖìa´
ù>\x001eã\éN³\x0011ïe*6¶xà¤î\x0019ßÐï¢1g©3¼ùØÆ\x0012×\x0006\x0008¾\x001eÛ9<æÛþ´>\x001eãZbRÓ:y\x0015a\x0011ßjÛNïÃh\x001b"óDûh+ë\x0006\x0015Q\x0011=òI¶!1ßGb\íÒ¨6zyØOF5\x0019²]'\x0015g|Ãb¾År\x000cÔ®^Ú;\x0002\x0005Ð\x001eª9

>\x000eãàP<Wº\x00186©µ\x001eoBCa¡ÂRªm.hÕ>¸P»Ó&¥b¡á°ÐÉa´½ÚrV\x0016e\x0008J\x001eÆ²m'u\x0001ÃB\x001fIõEÄ9\x0013C\x0000Ekv\x0004È\x000f£m8,trX¬~<¶hdÃaUÊÙÎ:¶!±ÐGbùnÕ¶	ïª¸\x0016@
\x0014aN \x0018\x001a\x0012\x000b$H{@)§¼FfL¤64)s\x000c
>\x000e\x0003WWÂÛéÈcS¬Ù
MÂÚ°Xèd±ì¾$ËeÃJt\x0000 ZvN\x0008\x001e\x001a\x0016\x000b},\x0006lNM\x001cC\x0015tÕ´^obCc±ÆÅc6J³}\x0002ÕÍ¦ÝÑl>¶á±ØÇc¼\x0000¾úPµ\x000cõ\x001dí\x001c°
Å>\x001a#nï)\x0005})OX
ë&½ÆÄb'±ìf¨ÞÀª>¯,zfÃNBÛXì#1²µ]Ç+¥~\x0010\x0016ÜÎ\x000eÃh\x001b\x0012$.)y>´ª}\x0000ªCCb±!±ØGbdë¬'q-¡\x0018"©û5~\x0013\x001b\x0016},Æ\x0012îõÜV_\x000cVÓÎfbC\x000c±\x0018xõ\x000bÙ÷ÒµP\x0016'\x001fÔ0Cêd\x0006ª©#±{\x0019\Îç@]T[N
3¤>fàíÃZ\x0008¿3	/åÚY¶m¨!uRCÎn¥Ó\x0010¤ô ømÁ6Üú¸\x0001­­ÝÀÜ¡¤kô5\x001bRÃ
©\x001bø·/ÜNæ\x0003\x0012ê\x0012ü¤È65Üú¸WG=¶*ÆK\x0012ªK§\x001bR'7\x0004¬Ü^mpàøIÔ\x001ajHÔq­"ðx¼ß\x0004ª±â¤ùÁÔ¤8©/Å¡²u-6©ô.Æ¤U\x0004?É}µC¯DÆïúá\x0004Ò\x0019¤h\x0019,\x0016LCdü]¶Mæ$}´(Ám²<øYà93np¥-`:©,¤{5n\x0010-ã´DÎR²Å)\x000e\x000cL;¤k:©,G·ÒìC,×îÅ¸5\x0016\x000fsZl¡ÕBà¿ì{z´z\x0016l4µnµ\x0012:§Û\x0007Z5\x0004þË\x001e´çÅ+ØJf\x0016¼z\x001dE«ÃhÛ1]ÓGf¶Ôfô\x0011Gõèèò3ç¥\x0014ZI\x0004þË.ãB}s"\x001b%\x001cOÖb=¹nJ\x0014\x0006¦\x001dÔ5}|Æ\x0013ûõõ1ÜËK\x0003%_;'fVÂÿ²Ë¸9\x001e\x0017½Ñ\x001c(Êî2\x0016¬'wÎË.´*\x000eü}O»FUò?ïÄº¾\x0016íìD\x0012 e4èc´ìÆdýx¶®U5WÞë"p§\x0004\x000bp-:ÑÇg<\x001e »ÇY\x001b.I·G4õäÎéb+Õ>Ù	ç¸C\L\x001bïKùÃT-;'}+Õ>Ù	Ç=ìFÊ¼4\x0002òû®ú0»³è0ÜÏút'sA\x001f\x001dÈéÐn²Ü\x0008*Ö
S
¸p¥;Ñ'<±¼ñêÓ\x001e+\x0013©uS}Ñ\x00148^	Oô)Odã¢Êiq¡´°&\x0002¯aùÞ\x0012úÃp[Bëpü\x0012-Ò\x0013´Ì\x0012WÞv6Ø\x001dFÛ\x0012Zôs¼\x001fP\x0008Í×£K¶&hºÚáJ{¢O|ÂÙP\x000b£ü®#p9.û®\x0003­þ\x0004ô	P8ªÄ\x000byâ8g±®«'w\x000e¡µ\x0002\x0014Ð§@ár [\x0003G¨q.T\x001fv\x0012\x001d{%£ÔGhÞ\x0004U}"\x001føT,¶UAV\x00023)rlE( OÂe<ÚÊJ<\x0008\x0017ôE²Zwg«ða¸-¥õéP8Ï9âtY5¶p\x0004\x0005\x0019ÞÍ_3§ð\x000c­\x000e\x0005ô	Qdëzn¼.u&s/í\x001f)*£¹IV\x0002ú(r<ët8kewâÇ35î:øa¸-£õ)Q8®åKs
ÿQ¢14\x0002é\x001cé'h( OÂykT\x0019\x0002Ý\x000b£éÞEVi
ØÐú(²m£f\x0011sK)!\lsà¶J\x0014Ð'Emëî\x0005­ì\x000bq¬\x001f"û¶2\x0014Ð§Cá¸ø\x0001ª¾µ7©¬\x000f­\x000e\x0005ô	Q8O¨)\x000f >Ál\x000c X*3à^é\x0002vÒY\x0019&ÓÂ¾43"Õ0×Ç99D«D\x0001}R\x0014ÙºIß¨Å«Ê5s¨½\x0000;\x000fÃmé¬O"[·6\x0008ri\x001f¥\x0013ÄÕ»0ë0´|Ö§Gá¼[FÎu­îgs:÷\x0002ò³V\x0002úä(\x001cùt¯}§%±K¡<ÌikV\x0002:Õ(|lE;¢\x0017í²äH].L*,´j\x0014Ð'GárxxïjåYÊw\x0018©ÚIaM+ð\x0000}
\x000fNj)\x0019Q\x000fNjó$ýMî#hàvzÜ\x0018jzFZWÀZ³	s&I ÕL>Ñ\x0004G¬¿ik%Wæµ¬ñµ"6gè\x0001Z\x0019\x0002èÓ!X\x001e¤Âu÷VàBÐÇÉIòÐÎöCßp¿cnm\x001cÎ<¬pm=\x000cqØ\x001a´ãòÐ7/ï\x001cj]guß\x0005oQ¸s\x0012õv\x0004\x001dúfÐ³ö\x001e´ÜHºÙÂúZ×ª6îJD¸ï¦9ÞéjkuTkÏ¾¶Úì­§=\x000c·½iÃÒ#Ty\x001c'h´æHB;\x000c\x0003È9á¹G¹iùeJ6©©¼ic\x0006Üv¤\x0017:gz]0ª£A,á.:b4ç$´3²Ð9$ë8XPÓF\x00190J$B§4+Ýi§N¡sìwÊkÇB\x001f£¼AXSsß9Ð\x000erBç$§±VõC]\x00032[\x000bLsÐ¶¬s>Ò%ÔnA.I°ãK9lÎ%k\x000e¡sêÐçèË
\^e+u\x0010Ýò9£²Ùëí4jaÝOsúºÕµOÐ\x001a¡ÖyéÎV<~÷°Æ\x000f}ÚvP÷$ä\x0010R{dJ®Ú\x000fs\x001eÒ\x000ck3éµ²ÁøÿS÷vYvÝFîTr\x0002\x000b\x0011ø_~JR)*}?Î$µìzÑJIY\x0012»)¦+Iºízêiô\x000cºÆp\x001f=\x001eÉElDà\x0000'ÏÞ\x0000Nùº«Ê.úX?Ä\x0006"\x0002ø)ÍÂ\x0014ñrÃP&¸\x0013ÕÏ~\x0005í¡µRm\x0010ËÁs,ÕúD­{µßgNÿ­cÌT^ú\x0000hf\x000eIe~w§é\x0014\x000eõWg0óá3X\x0004m<cSÁ¦\x0017@øJÌaTÌ\x0016\x0011gx) 
È-®û*Ó4üðùþ±Ù\x001að;úe`køäW:Ëmg\x001d©jbÆ ¥/?Qíw_A7|\x0006Ãî½MíÃíîaûT\x001d©ýWö£\x000e>4\x001d\x001aëiù\x0014ñªñDU×\x0018ö%aTsÄt\x001b\x001a¥É\x0018ø¢:Nf¦´ýJÝÙauç°´ "Ü\x0012ÃNß¨­£Úß\x001eÉ\x0018m\x000f\x000cÇ®j`/48\x0017\x000bôº$í±/i\x00184Íá\x0010IcÈ/É4£tØ>UÿLó Í° Þu¦ÔR\x0013B®jiöx"\x000bn¿R\x001evXyü¶4|}\x000eaø î¿Ìð\x0008ÝæeæDï\x0007_íi\x0018ÞÔb°\x0012Æ@i]\x001aQÛò\x0016z¢»ê+wiÔYZ&rKcªnÈ½ß|D,\x0003\x001eO4Áéë[Öè%Ëø¤ñÊ4\x0001KC\x001b\x0016×£\x001asWQeð+9ãð*Yya>.î:Å&\x0012C\x001aoyØV¾Òxé\x0015Þ®K{<
÷_9\x001e~Ôñ°FÙ\x0012úT2.BÀv\x001bf\x0005mò!ÜÅçL\x0019¯úó³ÛûÇ_î?~>ûöî\x000fo³¬Ué\x000fGoù"î´Ü\x000f­]É\x001dÿæÝÙíåÍËWoÏ¾½xqþõ%z	fv	`\x0015ÝÅ%HÎÓiÂ®z-0²\x0004[/ÁN/¡ª<\x0001	é\x0005\x001fË-Ý®ô_\x0019Y«à¦à<uÉ¥%X·m¤\x0004QW.À\x0007Vp÷øÓýÄ÷5¾?Å\x0017°\x0006g©\x001a¿@©e]\x001fëÜý\x0005B½0½t9/\x001dæsÃ\x001dþ\äÐ¥Ö+º~d	±^Bÿ
(#p(ï>*yªÝ0µ½w	Uu¡b¬é5@\x0019\x0001ë¢þ_|\x00015Z­Ô\x0013¬\x0000\x0015ÀüW(½¯
Ýü¹Ãi,½ìVnv#KÀf	8ÿ\x0011ëË.Ýü½/_\x0001V&þ,¡1Ì0mËRç²,\x0007P¯d]ð7V\x0019æÍr:\x0007ÜËÀE%ÑE\x001fä,ë$%4V\x0019æÍ2ùafp\x000bÊÀ³§¡8½QÆ,Ã¼]VN\\x000bóèóQ§!þä®\x00054¶\x0019æ3Xñ-Ü®¿½\x000fòPîô[©±Íp\x0002ãìd@¼G%wÒáEëD%4¶\x0019æs:Ð\x0008ê(ÓÇ4
ýÉ\x0017eÆyË\x001c$o o»4ÄÉG8ùIÀÆ4ã¼i\x0006ë\x001aååòÔ½dØä$ø~Þ#khl3ÎÛf¥%6è5î>($szÛmÆ\x0013Øæ2?Ì9'c0½\x000c4\x0018Vú¬¡±Ï8o\x0015Ê\x001a¼ö2LÊ\x0012;mV^GÖÐ\x0018h7ÐéDs \x000b M}vW\x001e\+p\x001dYCcÜpÞ¸©R;èbI3ÞIwc
+í]FÖÐ\x00066
*\x0006©÷É]ó`%\x0004£q¥\s`
ºQ­zZµ¦d5u½d¥AT²\x000e'W­º
æÍGó\x001cJ
\x001f-½9/k\x0000IÀÔ+óGÐ\x001ci={¤Mt\x001d%LÖnÒË\x000b®ç¢Æ©\x001e´CW&\x0010¯?\x0012\x0008s8ÌE,Rs­ÕJÍõÐ\x0015è«¥Ø,åÿP6C\x001bò\x001e9±\x0014½kÌ\x001dµl°\x0000¥ i¥&sl%û\x001f\x0005NñQIÁÔ.»¡cIU\©z\x001bÜï/ä$çÄÊ`8K\x0019vÜkX{Égµ+ó\x0001{\x0016B9\x0010´âÓÒøÛKûüîÃ_\x001e\x0015nlåke(\x0014\x0005â\x0016ÔQÉðv¯×Ýñç\x0017×ß¿¾º]GÖ5²\x001eEè¤\x001f¦¢Ñ\x000fYØ{\x0005%â\x0012¹\x001ebS\x0013abj®ÁÄ\x000e8i#\x0018Sd¼ÛClkb;L\x001cJ£EÆÜMß³[JB^uK7#û\x001aÙ\x000f#û(uõìy_8Îè×õ \x001a9\x000c#'÷\x00159ù=ÜÚK6®7+É<=Ä±&ã;Ysw}zçË{îÔIÆëod[w¯\x001aD\½jô"+'Å\x0006Ê\x0004ê}o'2Å×ãJ\x001de\x000f34Ì0Ì6°EÎ \x0006E\x00125üú{ðfäF)Ã¸V¦Á¸Vfd~q¡Ów:äF+Ã°ZVÁH2p\x001c\x000eÔ22Ù¯¤¥õ 7j\x0019Æõ²)qd2_S\x0003ð5õ¤Æo\x0017Ç_Ý°'QJ¹äi\x0001^\x0015
+E\x0007=Ì-qcb<ª<\x0017+Ë¹ø\x0018x:äF3Ã¸jÖVHh=ïf©\LÈëAÉ­ÈØ¨9\x001cWs¹5GFÞ\x0005¿¢/b^ÉVìanô\x001cë9]Ê«¨Fb¿Sî×ª{ã;#ùø¢\x0016kâ]±ÚÔgäDÌºõñÅ¬hn"YûsÍbÖâÌÁJê~\x000fr£õ°nV>HÍÒFæ(\x0016\x0003\x0008æxÎ_\x000fq£åô°#=ÁïaÚßKn%5YÒÛl\x001aaUF2þ;d[F.k/Zi9²\x0019 Ç
vñÙtf\x0004ùþÓÙ»/y¼ßÌléÎ·ëþæ=÷_».+~þåíÙwßß\nÆ\x001a\x001aÇ¡­VZè¥Å\x000ee [ËcêaÖ5³\x0010t ÎT9	\x0011¹Rp)Õf9\x00009-|/üâ*1}¸;ûöáÃûûÍñ\x0017Ä\x0012Q;vü¥ÝZhàòìúâìÛ××WëÌºfÖãÌ^¢v*Fäæ!F~ÂÕÎ¯Ìøè65´\x0019NV$·éMÐÊ
\x0016hÃ\x0011IÐjÅ\x0008ö@Û\x001aÚCSWt¡v\x0014Ë vôS×\x0003íjh7\x000eM#¬XÐ2&.D\x0007²£ýJ'Ñ.f_3û	AKÕ]\x0012´¥V KµskïN=Ð¡\x000e\x0013ç\x0010¸ØgÙ\x001d\x001cñ'Ñî8!t¬¡ã0´V&h(}ééÜZ­O\x000ft\x0015CrUfì¨âxè²?x°"Â¢^ËLî¡nl\x000bL\x0018\x0010øæ¨5×ûÄ¥Ñ\x0004ËúG\x0011\x001a\x0007ãJOSïF©=r:AL>µÈz¥M[\x0017t£?`\h\x001b9\x0007"A	7ÀÉ÷ù&\x0011\x001aý\x0001ã
$ý/Wu+z´v"iozeP\x0017u£@`B$µçYíqÛT*g\x0013ä)å=ÈØ¨\x000f\x001cW\x001fÔÀ Ó?# \x0014±¹v\x0010]Ð­g:®=4MÄâsèt0ÒÄÂ\x0019·òÎÜCÝø¦8î\x001aò¢\x0019Zs´?Ç¤O§¨±Qy8®ò¨åz`óbq7\x000fºxÔúÔÎÃqg´ãÉë*&ï\x001a¹94rO`íp-¥¢ºQz8®ôöö\x0019Ú\x0001Ñ\x0010hêÕc\x000ft£óp\ç\x0019\x000b<äK¥»¡xM(íÈ´\x0013ª=Ý¨==®öhb4+\x00102^\x0002Á
ôÚûJ\x000fs£õô¸Ö3Öò$S\x00144ç'I£¨Ö\x001e²z¨Û\x001bùÖó¾èj\x0005çÜÚ¶<×¯\x0007:\x000b¹\x001e¿äþç¡*Ä]ÛÀ\x0013nµ
koY=ÔªÖ\x0013ª::ñ>\x0002Ý\x0004dò¢ljëO¨ªus%×ãwò¤á8®¨qYDiÏB}BU­\x001bU­ÇUµU&#'¯\x0001\x001ax8\x001cµõ>¡Êk\x0014µ\x001eWÔ\x0016$[\x0005ª'æ	|Z¢\x001fvm`B\x000fµi\x0014µ\x0019WÔZ\x0012²¼\x001c®ÍÕé"\x0018Æ©%vöóI\x0006¡\x0015è\x0013ÚCÓhi3®¥i\x0010[N8P!\x0019D¾¼h\x00197LÓ&O\x0007ÝÆM'\x0002§ÿÀ\x0008µi´´\x0019×ÒÖë²=3î¢¡YYÐ¸Òa´\x000bºQÒf\I[29y\x001e/;mWóz{ K\x0019¿\x0004Ø\x0018¹Ô:Qé;Æ8Qx°Ò¼ºQÓf\M;*ÓçH\x0019°2?*úXëéÚCm\x001b5mÇÕ4\x000eÊ¹\x0007ÊG'Ê)¢©M\iÑÒEÝ¨j;®ª]ò=Ø£öÁS\x0003è¥!­4+jØx:êæ\x001e`Çï\x0001.Ý¸r1Mµ¢ÜF7\x0016Y¯%§÷P7\x0016Æ[\x00184´
,kt£
<ÿwix:èÆÂØq\x000bã<æ¹\x001c\x000b³\x000c¿1a\x0007}Â³Ø¾Ì[\x0018Oý\x0019DÒ(íÛ!SpS7ÊÚ+kÔ\x001eÇ!½ò à$ÙßSÞÈ:\x001e¾uRË­\x001dB¹.j,z»øÑåì³9ö ­&·jøñ9öbn\x000cBq{ü¡I[I?PÚÊ\x000fw?ÝýþþîãÙËûÇß\x001eþc+6\x0018Ä1zJR\x0008bÛ£9R\x0005ðæúâùåÙï//^½¼¼yùú_×Áu
®§À¤Éb:=\x0016 ´É¤Ò\x0013Û\x001aÜN;iÁLÏè^:É	êH\x0001p_û\x0019p\x001b8]\x0008µÎMA\x0007¶!\x001eé\x000f<À\x001dkî8Ã´
o\x0014íK£\x0013;Ä§×~lhOæÌÑT±ä!µ9æÜucË\x000e?Ò
âkòÃÊ\x0004»90u0¼í\x0002ºPú ì\x001aÐ£}Z\x000f\x0008¼90s2U\x0014E¨ifrÆvEÚO{(\x0003ÔÍ©c©hÂsîC¹kÂ$1x,\x0000?Ý\x001cJ9ÍCÊ58~MOàF«º#
¼úÉ±98w.\x001d58Î-VMQ(VÞ§ã±þo\x0003äÍÑÄ£©¢ÝµÃÒMÃ¦¥áH3ý\x0001òæhâÜÑ4|_\x001ay³*´ª\x001f¹?ÎÆ7Ì'~\x0019çOÞ!\x000f\x0004\x0000]Z\x0006êX6û\x001e~î¼ÛìªÊj&öÙÝããýÙÝ³gÛ3²ÛÙÂîÝ9r}'ç[Ü\x0014Ò|vqssyvñîìÙñ\r^®W çW@=Õy\x0011\x000e9?;P·d^\x0004¬õþ\x0018Y­\x0017aç\x0017\x0011v½\x0011_ÝÈÝÎ,\x0013¡O¾\x0008_/Â`/ÝHz_v$Ê/\x0003\x0014O½P¯!L¯!Ral^Bú\x0013_=¬-Éþj­\x000ed`
U£ÚÏs\x001c\>òébÍó>Ò*Ê\x001c<µÖhd\x0015Ø¬\x0002çWîÚ\x0017\x0011yxyHNÔ\x0003¨M¥ÎEf\x0011æ\x0004Ðe SR$n©6Wñ_°\x0008×,ÂÍ/Bï¦)8\x0005N\x0017\x0015»%zÓ¹ædÃ	6ÚÒÖÝéóÀ«Ý*6½uô­\x0002³'8Û¨9(­Â
\x0005¥Ñ;\x001c¹=µ'.¼æ`ã	\x000e6@QOÉN°z2Ñí\x000cÅèkçhN6ÎlÊzáþ²Ú£Ü*ó2rkmæÝÐ*£óG;XfÊÑ0G\x001eâó\x0014ÿ\x000b\x0016Ñl?Ù¡\x0006×ÞîÜØ2T\x0017×º!ö,\x0002ü^\x0007ô½ýõá·»O´7wÛË"Mr¾¹ù;BÉÿ
ò0\x0018ÖêÞ~÷úåÅ--ãÍÅÍ\x0016v]³ë)ötQã·z@£%TcJ¢VA7¼©áÍ\x001c¼\x0007Þ8H\x000f*<¶R&Úê´\x0013³ÛÝÎ±k©.\x0003L®jäQÒ¶Ä`¥Q]7¼«áÝ\x001c|2X$oy*«Ü\x0015HòÇl7¼¯áý¤ä£\Öê\x00018yIükÅíÝè±FsèVSÒc»üi\x001d$0âJÉ^øj6ßõÔ\x0019¦wâ8PØ'\x000fk\x0019v
\x001c¿uÓ7J\x001eæ´¼\x000b¥9¦\x0001\x0019.îe
£]\x0019¡ÝMßhJSÿh\x001b\x0005Í¹\x0013ë¨å3u¥sxÒ6rbý©·MsbaîÈ:0%¬\x001bÜcùµ¯ÜÍyÅ¹óê hy
íÆ(yZ%¶»\x0004ÜMß868çÙ8´\s\x000eTÔèùÙ?\x0019ñ´ª\x0012\x001bç\x0000ç¼\x0003geC,Ó²E1\x0014¾9®8y\ÿÑðÍyÅÉóJu\x0005Õ|²LëË\x0005Ý®\x0014ÞõÒëæÈêÉ#«-\x0017x§»ÔÒ\x0013n¡W ·ZÐ§ÕØ6\x000cÎ;_u÷Oàì®´J½\x0015¥\x001bÉÉ§]ÒûÐ³k ú\x001a/Nf\x000c5\x000cer"êC(T{/K¨ö^\x001eßÿûûÏ÷\x001då§hØGV\x0014RçÄbå\x0014bµ~ùN~sõwo/ofNá~O]TmS\x0005$Û%Í;\r}x\x0001VZ9»Öv«\x0001¦^^@(5íÉëç\x0014XeC©¥UÂ=\x000b°õ\x0002ìô\x0002<·ÄS\x0014ºÕò\x0005Ê\x0016MUO]\x000b\x0008õ\x0002Âô\x0002pZ\x0000wÊ°Jú ÀÚÀ~úXÓÇ\x0013ÐóþÝö1Rè6¾uðWï`¨ößÁ\x0006\x0016 B©º\x0005+\x0001\x0012et©\x0005]k\x001dÛ¿VN+QPÜ\x0014YÅ´²\x0002W¾Á¶×£\x0015èf\x0005zú\x001bx7¤\x0015s'@b$è
ò7:\x0014f(ÆbÆBd
M)\x0017Ý¶ÜµFÂ´\x0012MRçÆY!ús}iªä\x000f°©ªk\x0001®Yý\x0002ÁZ0ç¥Ö'é
)\x0006s'w$ª\x000c>T{me>\x0001R%iþ\x0004(±Nd/ÒÛ^ã{VÐX\x00025\x0005\x0018ôO¢ä}ÃdÂ1Õ\x001fú\x0018`£IqVÒwà\x0015$oÚK0éÀ`·µ%êZA£IqVbRÑ\x0014â±!é\x001cJ=»ÖSµ\x0005*ÂYUéb\x001c¸ÖÐ"\x000f\x0007J+Xµzøm[Ap{\x0019NÁQÔÿê·?ß}ú$xy÷øñýßÿ÷ãö
P<:¯¥6ý\x000bi¹jôQ!W/ß\ÜÞÊ2^^Ü¼ºº¼Ù°X¯!N¯!(WJÒ\x0015kÜé\x0015×p¬£þà\x001a*¿(­ü¢ÙE)UôÇ|½1Ruväíkt
¶Y_\x0003í þ\x0010ÉJs³#/ïH\x0006<\x0007t¯Áïßñ½ª{â~ûðéÓßÿs{p"í¡àJHú4\x0005#óâWÛ%_Þ}û:­àX\bÿ¡]yU·ÄífÞeH{)®2Ã5ÙÌ5ý¹\x001dY×Èz\x001c\x0019@zRkêð&Ýv\x0019«\x001as;³­í\x0004³+1·\x0014<s3,	 ªUK»ÙÕÌnbká3éXò¸î´7|	8¯ÄÚz}ÍìÇö`dã\x0004\x0019Ajc\M\x0018Þ\x001cjä0µ58M'1Ú½Aï)k\x0011íÈ±FãÈÆH¡\x0016½¿\x0019î'¥Ýîýmí\x0006»¹
ø:ü1 ç@ÒÍÏV\x001e
Q©RÅ²Ú°p;tkQ&LJ\x0012/ìQnt ÑÊèN(èÆ¢ÀI2\x0000 -÷XEÎ«\x0019Û\x001b\x0002\x00136\x0005¡<ð¨XzI)éÛ\x0015ÝjD`;´i Í\x000b(PL+ß!\x0017|·\x001a\x0008Û\x000eÝ\x0018B°I¼F<
Õ±U\x001c'\+Ø\x0001Ý¨hÐÑ¤dv\x0015¹I²=ìjÐt34¶Ýø9ÔQ:%\x0003R7'mCÅ\x0018p2ûÏ\x0013Ns@	«ù :g%£FÌ¹\x0003ÝV½-\x001ad×\x0011a@ña©ôQê\x001cø<Æ"p»QÓ¥D¾b7SìJ\x001eö8}÷°êV\x001fö:.\x0002ûìsb§\x000e^ìô]O__²µñH%óVtÈÙÕø\x0014¿+4ürööáñç÷[e§[\x0017×¥:/\x0001hj\x0001r\x001cùÝÙÛ×7ß¼¾ºYGÆ\x001a\x0019©Ú_Þãn®¤@$m²>~3²©Í0²)318éòæÂ®ÕÇÚ,\x000edW#»adgeÚ\x000boÐ\°\x000cÅIµkMU:C\x001cUñ«ÑYN+1èàN¶wåø©Af\x0013£Ò-L7FÈ¥NI\x001aC§\x00133´*c\g$sÈé;@ïå,\x000fÿ>ÀêdÕÍÌÎQ¥ahX
\x000f#k\x001er5\x0003%­Hüú$æÍÌºaÖÃÌAK¨&hÊ¨ûXÆ´á\x0015ï`n\x0014\x001djºEÎ\±¶Ñ"æâ4©Ó!7\x000eF5Ý,Þ©\x0002]ï(vW[ángÆFmàÚ(ÚgDÍ·F°';ØZí\x0013X&h÷\x001c\x0011KÈR\x001c\x0010V3Î:Ý\x0013»YZÊ&LälËÄ,Ï\x0018A¯]Æ;í\x0013Û9­a½Ì£tEÌ«c\x0003¶#ëf7ëÑÝ\x000c·¢^.\x000b2
\x0016d\x001e\x0004X)zéAnv³\x001ewB©³UvBAKh)8\x001bVPkÅÊ\x001dÌ{¤Çý#PüÀ\x000bÔ\x0006Ø\x000bÕ(\x0003aÝJÚm\x000fslã8s,³º\x0011Ë\x0010M£ËDØµXéùp\x00155\x0003f/ñ½L¥C,d\x000f2CÚi©Jðf­ìv!Æ¡3\x0013\x000e\x001dÒP¶9á\x0005Ô\x0012sLûb³9y¢T]ï¿\x0015êæ­ðÙÏ·O¢¤\x0018©âÃç\x0003\x000fc¨P\x0014Y-(¾={öîíÛ£!\x0002½ÿV¨·Â>dê\x0005ÀÛ\x0002ÐHr\x0005õOäm\x0011Wkê·#\x001aÙ\x000c#käþ\x001e`4Ï¿ÊKRQXoÇ°ØÖÄv\ÈÒU8	Ù±\x001f\x0001Ê,ô¸v\x0001ì@ö5²\x001fF¶VJ&yÝ\x001c\x001a-½Ô}\-ðß\x001ckä8¬¤Ã\x0005Ð\x0016a)Å VÇfnF®¯tû|ÕÉlÔ9o\x000cmäPEIö\x000eêH\x0003Í^äFaÀ°Æ ¤>9~KFPÎJ@ØÂ±\x000cz?¨K,qaúë/\x001d£Ð£8E*$Hä¶»3f¥%ÐòÓÙõëwGkzô~4Qhâ\x00004)Íêu\x0014O.\x0014#Y½r\x0002» u
­Ç¡\x0013)§ê\x0019ÏcrB4^\x0012>ÍÊÏ.f[3Ûqæ¤ê8ßvbh·kÓ¼¬½
\x001aö2©Ò\x000f²¥ßÜ}ùpöÍÃßî7»FÔ>pBºµ\x001aÎÆ\x0003#E
k)òo.Þ]}óúÝËËcþ\x001cì÷,â\x001e@\x0007_FH{MÁ\x000c-9Ù«ó2» u
­'$íË¼;Îa~Ùôe\x0006ÛZ=W\x0017³©Í\x0004³æ"4á§Uy¾ÌªqNÆlkf;Ì\x001c);:ùK
%¿TW.T]Ì®fv\x0013r2Ì,ÚÀO>ioB\x001bÇa\x0017´¯¡ý¸ a7ÕØJm7âÙ¹5»ÒÅ\x001cjæ0±9l\x0019zmUn\x0011I{£o\I\x000eìb5s³¥¸ÀÂ<%\cñú^ñG{ «w\x001fØ%
QÃy`Ýa¤rÉS\x000c4CãÊà§.èÖ\x0018[Cö\x0014¸\lñ@\x0016hëËÈÉ#í»¡\x001bc\x0008ãÖ0ç\x0001(QÛb\x000c-9ª'dnl!\x001bÃ^j1"å5²ÂK[ªSW¢H]Ô5qs\x0018ÛýS=í¹fAÇR\x000f¼\x0012âèbn¬!LC­e*J¯(ïK
êZçÌ.æÆ\x001aÂ¸9¤Ê\x0004)ª¥w¥t\­´°è¢nÌ!LØÃt\x0007·¼§Á\x0018ä¢åÔéRhì!L\x0018Dí·ì9\x0017¹{/cqâJ.èÆ ÂELwBqþ\x001a¾¤ÙxB=EÄ	ht±ã
vûCf\x0003Û¸VÐEÝD0Õ­6\x000f¯%ê% $Õ£§ó§±½ NØD\x000b¥b4Ýa¤>+z¹äÆ.êÆ*âUtZ¼Óe:pö?Byµ~¥gC\x0017uc\x0015qÂ*ÚH\x0002\x001auçyBmNx\x001a\x001b»\x0013vÑIv´J'PNc@,£vWÚkuQ7\x0011',£\x000bôRáx¬1Ç¦ÛZ¨ÌÔê¦n,#NXFªw\x000bS^Rý¼R,ÔEÝF0^\x000cgÅûZÀ©]©Êê¢nl#NØÆÀ	JÎ%×±ÒtÄ®$Îô0ëÆ2ê	ËH)9®n%ã5AýaV:\x0014tQ7QOXF\x001ajÇ6Æj27:ñÞ.êÆ2ê	Ë\x0018dHÆ2LÐØ}j}Â¯nl°1ÉõÁèZbMéT\x0016è´».èFYëqe\x001d\x0015æ-é¾È@#¯35®4\í¢nÔ\x001eW{±Ô'¨\x0000c ÁKÌ×ÂéÌ¢i\x0014\x0019W Ô_ÉÉ\x0018i%]fBpe s8IÇ¼}zI?´êú\x001b:ø \x00024YæÀFWæ\x0004oê\x0011µ¥ÀÞ£"±ã$;p4v·fôàÄíÃ-ý@¶ÜÌ'ßO´IÚ.Ü7K=~RrW»irÅ\x001b=i\x0017\x0019Á\x001b$3Èª\x0013K=ÔìaÝsºwÚëpÙ%wÏNÊ\x001ekö8Í.£¡\x0007;/e\x000c\x0006ÖR\x000bûØ«Zì°?i\x0000ÞÑÐà\x0005ÒÉ\x0004>°OhÂ¦6nÛá[\x00059©!­\x0014½(§£\x0014:'mJô¦&ÛÙ\x001b\x0005	\x001aºóó·ÒòÃy-\x001dVÖKûØ\x001b\x0015	³:\x0012ä~ìMyFu^\x0006:\x001a³©ßÓvøFKÂ¤´N\x0012u¼\x0002\x0019¬á\é1\x0004«õ¡}ðI=iË\x0003vR\x0019ådFé¸ZÛ\x0005®ÁI]côûKÒ.\x000eMuKïï§}g\x000cjgìÙãýç»_>nå¦x´`¡ÂhäÁ{Qºf\x0003ÝeV¸Ý\¾½xñj\x00034ÖÐ8
m¦¥ÙÍÒRHK.¶)# Võ.h]Cëqh*ëOJè\x001cò\x0005Ã¬\x0016\x0016ô0ÙL\x0008Zvj Q*\x000b4B2«Ï\x001dÐ¶¶ÿliWC»)Isí¥Q²ö³¤­ì
Mú¶Cû\x001aÚOli/64y¶r\x000e\x0019:m\x000c9ÔÈabsà9ð¦É*R{É\x000fð\x0012ÌO\x0007\x001dkè8!g-r¦\x0012	®wXÚ¾­E¿{ +\x0017\x001c\x001a\x0017¼WÔ
\x0003sr¶S³C:ï\x000fÔ'ÔÒÐÚÃÿK\x000c"4¶\x0005Ë2î4ûN®Âeò¬.{ÔÇîtÔ¢	M­MÎv\x0006f'ÓM¹\x0010ÅÀFùÛ\x001b\x0007Ã:æ¡Hg2«,OòJ\x000e¢@t8¤\x0015îyyÉwâM}ñáÇûÇÏg7\x000f_>¿ß\x001e*´\x0014ÓÜEgxö£V¯(¾ëg7oÏn^¿{{u4ZÈèX£ã\x000cº¡\m'[N©Ã(m	,®Ä­zÉuM®§^µ ¦ê°\x001c¶Ò»\x001a\x00044Ç¥zÑMn¦\x001e|Ù/4\x0010kñÊÌ7\x000bþøéìE·5ºÛ/ÀÙÛ\x0001´Üà1"äÜÕän<©r\x0013$+	½$Ùµz¦^t_£û¹ýbK6*¯Æ\x0018Ê£ZéÙ\x001ekô8-u\x000eù{(B/aÂ*FhuúR7¹yÁBN\x0011ò¬_ÐJÿ!ãW¢\x000eÙÙ³GéoÌèÏ?Ü}Iôû\x001f¿|úô·Í\x0001\x0013ÀÒIÚÈ\x001d>:zðÍèvå>üüúâÝ7dN½»½ýÓ::Öè8®¸{ò\x0016wèòloVé{ÉuM®§ÈÓÉ\x000c¼Ó±f±¥5¢Ñ+ö¨\x0017ÝÔèf\x0006ÝÅ(ÓÉ\x000b#ùgôòb¸V\x001bÞnkt;ÎÜ\x0010©ÇÂí­pãJÄ^n_sû)î\x0000¢Ò=:IºTu£W
¶öR\x0003ö]\x0003\x0017ÿÏÿÏÇ»\x000fg/ï~}ÿå¯[ñuDÉSqÚÉ$%ñ\x001fËÄææ\x0007/._]Þ\\½¼øîêòÝ\x001f××`ê5ù5P,\x000f¬Ã(SXÀGþ\x0008kß`d
®^;Á\x001aPKN*}\x0007ÈJ¬õ¦FÝ\x0008õ"Â	\x0016A;Hã4ÅÒ }Õ^6ÝÀfºár*J\x0017Ë\x0011\x0002Å5ò[Ôs,ríÖ¦Êt,Ey¿gÃH\x0003æïñû\x000fï\x001f>=ÿÒ1Ìê"d\x00123b{C,én¥§Ðï___½~{öüÝñ9&mkl;2:¹JnS!ÊóÐZó>j_Sû	jmåõ? 7è\x0008»|
;ÖØq\x0002Û\x00133ý\x001cí\x001aµÜ\ÍJÝ`\x0017uÝÝ\x0017w~\x0008Û\x001a~ÕZª8B\x0013èI§Vüû¸±áÆ9nIa%G$qK\x0012]i\x0000×ÇÝh\x0012Q%D'\x0015\x001eºìî]D*NÇm\x001an3#ï¥\x0007ªTKpG,Ó	Óü¸GÙÇÝ¨@Ñ\x0016ÎLUD¹|Dí%\x0018\x0016Wåöq»ÛMp;-I\x00118L\x001dÓ¦/åm+>X\x001fv£\x0004aF\x000b:é@«¨\x0019­åci­OûG£.nl¶7Îlo¯¸\x0013¾ZZKf7:S¸O)o\x000c
wãæ&áÔÕ5wáKÜ¥çÐ.nÝ¨o=£¾=pt\x001dsrÅNbH^¯T¬÷q7ÇRÏ\x001cKo¨æ*w=ÔEÞ¢MüZ;ùØFï\x0007¾t	|ýz÷øá~\x00191þâîË\x000fÛ'\x0005,
¡®/Ýí¸/ßÅ|þÝÅÍõå2düÅÅ»ëë
\x000bÐõ\x0002ôô\x0002¼<RZ\x0005HÈÔ­õ©\x001dX©\x0017`f\x0017à\x0003µ>Ï\x000b\\x001eNÍh¥1â\x0000¿­ùí,ÄÒT'z	ü\x0006ët+Q¥þ\x0005¸z\x0001nz\x0007ÙÒÊ(iyN\x000e»\x0011Ë~¥y`\x0001¾^þ\x0002%¹8¦Óà¥4§´q+js`\x0001¡^@>\x0002Vf(­%,C\x000céÀºÒäh`\x0001±^@\@T»¾\x0003>Ê})1õn%} ¿J!+ ¦·w§>Fà à³+O¬\x0003+híØ¬!£Ùâ±´öâçí \x000f­Î\x001e\x0006:È
?N2Ü79<2\x001a/8»kôuò\x00154\x0018f-1U­ùÒôB\x000f;Ìzâ\x00054\x0018f-1m!àC`})»\x001eáÎ¬Ôh\x000c, ±Ä0mÿñz\x0014\x001aS\x000c³¶ö8\x0013¦tèKHlñJÆÛÀ\x0002\x001aS\x000c³¶¢« ÂLQ¤%CÈáJmïÀ
\x001a[\x000c³Æ8ú¶h0I.ä6Òé2sò\x00154Æ\x0018¦­q~\x0015É­l¢¨d0ªÃSo"l¬1N[ãü9ÆÆá¬5	\x001bJ®Èqo(ªt­OWÇ\x0002`¿ï;ìú¾/hg/î\x001fKØÊîÅ\x0011ÒÒ_8Ù³âHàJD3w}qyó2ýaÚÔÔfZÃîØþN\x001etz¥\x0005L'¸«ÁÝ\x000c¸³®o/%öí|é­¸©Ïðfn_sû\x0019n\x001b¥v"ÅyåÚ»¥\x000fõfìPc\x0019ì¨d´¢Ð(Ýåhòå>ðª¥Þ5³\x001c"\x000f¤Ëy\x0004Ò'-@Ñ+÷ôNòF¡ÀFIþK0b¡x5:)['U*Ð(\x0015Ñ*!È­${n¨î2í@¯\l;ÁÃ	3§38yå\x0006e¼ô/\x000c`µ|Å	è$oÎ'Ì\x001cPò¿\x000c'?@\x0007ÉÜfÅûêä
wÚä]÷e«xqZl	Þ¯ùì#ÇF±àb(CéU@®wKî¢¨µ7ãNnh¸aêp:ÚØù¹DË+f0ÁÄWú\x0002vë\ÏÓk\x001að\x001eW"òàd¶7+ÝÈ:ÉmCngöJ²¶\x001cNnÇ\x001e¼\x000còóf%
¥\x0013¼Q8£\x0010#ÍO¡Q±´\x0008ôA\x0014¢]nt7\x0005g\x0014\x000b5EWÁ\x0000ò@\x0012°¯4fï\x0003×ÍùÔ3ç3"]\x001e«L+Ùäk½':Áã©gçóÃ\x0002ß"#^±§4Aº9zêp¢-ÞJ\x0012¸Ù*n¥Õr'ys:õÔéÄ(3è\x00059p
å	ù¤FÈ4ÜLmrcÅÑ\x0002U\x0002^QéR~¥Nh#yÒ({¯ßI©$ð«ßþ|÷éÓÐÀ&0Q¹«¾rÒ^åÈÇÕË7\x0017··\x001bg618Öà8\x0007î%<\x0004¨¥Á\x0010?öd?B®kr=E|[-EÝW¶u>/6njt3.1¹X\x0006¿)+í½;\x0012Ø\x001dA·5ºBWFÈõ*Jâm\x0002ü¯él6\x001býtXÓFÿîî·û»/\x0014C|þðåñ¿}ùíþÃÍð!Òøo:¥.\x001a\x001d\x000cqkH²ÃhãÓý»\x0017ï(øüõ»ß¿{yy}½e\x0005º^^\x000eä(Ò
´áæÌTMÁÁP\x0004$â2º\x0004S/ÁL/!]¡­]Îæ!Åi	ì;"¨#ù{£+°õ
ìä
¢¦jm·W¹º5NæU!#Á£Ñ%øz	~~	&\x0007\x001cÓ\x0012\x001cä¦Ti	\x001ff\x0010©=ù\x0012B½0»\x0004KÜ1\x001f\x0005\x001c´|KÞ-B8ò.0ºX/!N/A\x0017,m9\x0016þà¹s/\x001eíý8È_"¨\x000b?EP'\x0017\x0010994-º\x0019¸ü
\x0002X^§sÍG×\x0000Í\x001a`v
é\x0004ðQÆÜiÖZ@Y\x0000#££\x000bh\x001aÌZµè=Ï£5Xòh
¨½µpäÕct
YY»\x0016éÅÉ±e\x000e*»\x0015é;HoE\\x001a4z
]YÃ¾CÌc©ówX2Ów\x0011ú\x000e§ßK®Y]C À¼Ø\x0005o½Ö&ïN¾w'?ÐJWõì&Ñ\x000f³nÎU¾É<¨\x0002§äÙÂ9RÑ¹dÚÂÞ2\x0004I§~ùþ§_ï?}w÷é¿ßmõ²M:\x000e\,àÓ\x0005ûe@i" Xgº\x0007¿¼zþÝåõÙw\x0017·ÿÏÅ:5ÖÔ8A®5<\x0017jÙ9Ö\x0003\x0011KÑN}ØºÆÖ\x0013ØX\x0008zJ;³\È+W\x001a+|ú°Mmæ¤í}Ù#\x001c±OÒe\x001c\x000f­õaÛ\x001aÛÎH\x001bKÃ\x0003J³\x0014iKÇ¬ôÇè£v5µ\x0011¶=\x0001x®DÖ å¹zå\x0005°Ú×Ô~:JWú¤_AîÔõíØ¡Æ\x000e\x0013ØtM\x0003iå@Â®³8øãQú>ìXcÇ\x0019iûs0,m©\x0005\x0010¥+Vr\x0004N¸µëâ¡$C[K7/Ú%\x001bJxSÄ½Ò£³»µ3F2ÝlV®ár(tÂ8æoõs7V\x0012&Ì¤Þeg»\x0010òÅ5q;I4j¥åK\x001fwc&aÊN*IGuT;*ûÍ¤¦îù§ÃnÌ$LØI\x001d¸\x001bc¶2n(³çÓ×8þ\x001aÒÝI²V°OÎ9'(\x0004Ú¯$=öQ7f\x0012&ìdò»e\x001cs%å\x0011Ju®\x000e+M
û¸\x001b\x0003S&GI±¿s ampQv_©ëâ6\x000e43:0]m¼l\x0013'Õ¢\x0010ÄÒkÕÐ\x001b¹­Ú»ßXUÊEÓåìóö7>G
Ò¸éo(YùÆ+ié+³èFööêÕï~ºûùîÓçÇ§am
k`mº\x0003ç\x001e?`uçÉ¤f)ÕÌ½\ÝJ\x001d
Ã®K¶î¥+=qº\x0005\x001c9çÂg#ÞS\x0012ðJZI\x0007óç¥§_ÅL?È9Ä|ß\x0005«Ê¬]cµÈY¯4ü[g\x000ezÿ®«Ë]÷îñýýÙ·wï?|xØÌ¬i\x001eB~	Cïe
"¥æ£\x0017×æ¸¿¼¸¹º<ûöæâêúúõ\x0006tS£)t[r\x001b0a \x0000R¨\x001d×úoõ¢»\x001aÝM¡'Qsê\x0011\x0006}\x001eÙÀ\x0018É'Ç^ Ð¹àËÁ\x001c\\x0001u­\x0000Þ7pÎÛÆI2)=õ,àîñ§û?\x001f8¢v_aË8\x000f\x001f¨cÞ/\x000fï7¿ù*kä¹Z\x0007Åé^Áñ³irWÄ\x0004\x0013ñõ5½ù¾x}u4\x0006û\x00014 Þ7\x001fî~º?ûî!YÆ³\x000f\x001fî\x001e?o¶F*±\x0001ß\x00178Î ¥ÿC0GfÈ½¹¾x~yöÝëd\x001bÏ.®¯/nÞ®£cSè6H\x001a&¿[\x0014S_¿LîD.»ÈÝS,ÆîºYÞ?nî¨Hý ­4\x000f\x0014LËý \x001cµV%u}ys´\x0007¤ÝS#¦\x000c¥è\x00025dg\x0018Ô\x001bÉÖÀMo\x000c%b\x00024Ô a\x00084ä
äÄ\x00199þ«A<a¥®b\x001bf]÷½\x001bÐÉi¹6P§d.¸Ñª|y\x0014hÜ×cqÑcÏ½ÿíýGj\x0017øòáËô§ëûOw¿l.)\x0003:VÙ\x0000zP»Ý{ÇÉ}Ò\x0016ÄNGëåÕ+j\x0017øòõ»ëô§ëËÛ\x0017ÇÊââ¾¸c\x0016÷ä*Ð\x0014[\x0018PÒ\x0002
SË«HFñiEÑ¿
¿4bÅªq)ùÏ¿¿¿ûxöÍ¿Ü}Ø\x0008o\x001c¯óÆÀaà \x0002§@\x0019µ6Cú÷\x0017DÿýÅõ\x000cEîÀ·«¾¡fH¥kæÛä¤ÒóÒ÷ïÉ&þáËýÇ÷>m¶ä\x001eË|ñ¢ò1\x0018»WÔ+wÆ$û·Éo¥g¦ï¯ÈJþáÝå«W··Çüä4´'"ýPç.Þ¼ÿåîËÍ¶&)\x0015©\x0010Ñ\x000eKâ¢-3§È­et¥óâÝõ\x0011K#ÐXCã\x0004´\x000c\x0011L\x0017(qmå¤$Ú<ÍC'­¸gØi-Ï>üÿù¿.¾üxÿøñáçÍ£6´³\x001co\x0005Mwµeßø2F0\x001e\x000bíìrèÎ®Ï.Þ=»¼yõúËÝ]XþÀkøQÅ$xÈy
ÏÒ\x000f¿[þõï®I{þ.ýÅg/¿¼ÿy{ÎÅsÎÐ\(v\x000b\x001ayå¶GÊ¸¨\x000c÷\x000fï.ÞÞ$7öÝÕ7·Oë\x001fþöåó¿ÙÿÁZsÑÙb_þòáý'\x0012xpX'â_îIý$Æ¤ÞµÊ\x000f\x001fÔoÝæ£éÓ­=ß\x0013aäDâ\x0017¤@²Ó´ÈôòÅõÕíSZ°áJ;\x0001ðk/¥9ÿ@jáÅãÝÇ\x00044ÞTéR£ò$íÍôImX¨Àæ	V9
XQ½¸¹x\x0006[ÇÁ\x001a\x00077âx'V\x0013Ë ½JjÕ
\x000e7°ìÇÑ5ÞcMöÆ	GåÆ}I:Iù3\x000eQé\x001aÇlÃI\x0017\\x001a=N8Ãºtlöi_åª!K
ðG¥ck\x001c»Q:ÁåNÞI:\x0007D¦¥ì\x001d;ü±\ã6JÇè<¢5I'Yg\x0016\x000e³x\x0003zÅ×,~£h¢YÜ\x0003ÒøþÜ`\x0001QÉ&l\x000f¹¶"©\x001e¡Dcs1¨¥þÍ~\x0010'Ö8q#J¶#kB\x001d°\x001còÜU2	ÇÁCÅ^¶h@µ	']PÕyÞÅ.æ3n@Îx²Îß
\x001a
\x0008ÛTàb'g\x001eXú\x0001x\x000e:\x0013\x000c\x000c~)hô\x001flTQc~cH0f©^>U4b´'Éôó4\x001a\x00076ª\x001cêãøcy+æJ\x0003|,·KèçiT\x000elÓ9 Ò«Ê\x001aÙ¢ËÑÔôµ¬ã\x001e$úÑÏÓ\x001ctØvÒ!éäÜ!x\x0014oô³ìåè\x0007µ 4\x0007\x001d¶ôdÎÙ`Ñd9¬xD\x000fú`\x0006ÅÍQÇG\x001dÐ·c\x0015\x0017¯zeÅ|\x0006?xÒ±q½p£ï\x0015ÓÇ\x0002VË`òÜ½$\x001d\x000f¢#\x000e*Bl}¯']¨òë\x0011M)Vkécy`T\x0013b£|pò\x0001ºªÈN\x0016\x0015.[yPó`£ypæ¤@sÊ\x001dñxjC½tåôá­Ü8\x0018¸ÍÃ °ê9¬ôÙtV\x0006Oz 1æ¤ã¶\x000eÊñ7âÜ½5ñ\x0004t"\x001eîÞÚÍ£³¥·-HËÏ]$èsiÊ:\ö2\x0006á\x0019io\x0011\x001b72\x0018iÆj0,\x001bLñ¿F\x000fnö²Þ¸Áî\x000ezr1\þXN«¨\x001fõ\x0007a7ßeçöÐ/Û)³ÿ\x001ebÎ?O[È89ñ³u\x0006¶Ð>ÍT17å&-íhLA¶\x00199|¹·÷R5óîó\x000f»y÷ÎxøtLJZ\x000e¾³çKé\x0010I)²¨´âYb·gÏ¯_?õ\x0004W\x0011aMÛÔ¹ËDV£o¨"40L¤k"½ê°ó£ùLÑòég]\x001dUãE÷\x0011ÙÈn%¢\x0002k\x001diJ2BÖGN\Ä&úÓ\x0014k¤¸\x00152\x0017¢]<XJï#$ïå®\x0011½²\x0003Hjo«ÝcîÏ_Îß}øËÝûÇcn\x0011Ú%Niì1?ó§;G0(÷C¬÷\x0013\x0007ÊÞ=¿¸þþâêæèÁSûJÑ¦êÓ \x000e¿öfw!\x0002¹¼:o'á\x001a]µ\x0000Ò\x000f=é~­Ñ-9bù~­Kô¡ñ+·2â\x000f\x000eþû/¿oÓ4°>~^^\x0003É îÞü\x000b=°\x0010OvØeMÉ©\x0004Ú{aµÌ¤1Ô¶"ýgó±¼¸zµ<ìBÞ\x0004÷êíï=øÃ\x0003ü·üwB£\x001eåôëü¸ßÔ2èxD\x0011Kf:ýkD[	è\x0000Òë£@]ç'\x001bz0;\x001cÂÆ\x001fîÂO5¿Vº~øü>	ê·ûÏ>Ü=|xÿ×³W\x000fÇÑ\x001aË\x0015	D§\x00174_\x0013Yàg²\x001dÙë·WI\//_½=»¾8{~óúêg¯^_r¢ÈòÏ_\x0013¦½£Io \x000bÏ:jë¶\x0010ìõé\x000c&\x0011Es£Ö{F\x000cK¬{A!0"B8\x0005bÚ¹~\x0014N¥Îæ</!F\x0011¢ñÃjy\x0005*
9ÿPÊÓî\x001eÿNï³´ußÿý?W¾4g\x0016â¸\x001eYÆñ\x0006\x001d÷6#ç+ý)\x001dßg\x0017·oHR1bÍÝ%r¹Rg9/ÌfFqkg\x0018uÍ¨\x0007äùÝ>Éz9E>Ó¢m\x000ciDS#^D\x001d\x0003gÂ$/z§")\x0006\x001bäKÛ0hkDÛÿ¥£.»1\x001a
\x000e,RL
SÄh§\x0011]èú¥îX¼\x0019]X\x00171¢\x0002AÄyF_3ú~1\x0006#ÇQ\x000fÀÌ\x0018c\x0014FÉba\x000c5cè#úr`Èið\x000b£Ï\x00053	\x0011Ý´Þág\x0003Ñª1y\x001196Ë@äåh1
¤x¬3­\x0002ï×àÔ¾tÉä$HE2]>¶)6NkGh48t«p½ðfåþÈ;2¹¬²#½>5Ð¨pèÖáT5+\x0003²$ÍGÛ;]\ÆyI6J\x001cúµ¸ü\x0012Gµ\x0018lJÑ\x000câ=úù=Ù¨qèÖã:ÐsEÈÛYÙ\x001e\x0002Bl\x00149ôkr\x001a¿»Ñh
×/b¤úêL\x0018u&lÔ8tëq\x001d<ær\x0004\ª!c6ÙTÒY¤lô8ô+r
{ÈÑN½3\x0003Å\x0011yE\x001e\x001bÆØ/HjÕÏ~YÎ\x000f1:î'\x00049°±16Øol\úØ\x0016øB£énw¤;Þ¿s
@6Æ\x0006»
éÀ\ÔC\x0007[Õv\x0018åî
ó\x0005¶×~c\x000e¶èñ TÈ,É²#ÍôÑÆÆÖ`¿­ñqwï¢L|j²²#ÑÌ\x000b²±58`khþwÖ?É®PÆÔ"HcÙµ@·Ç\x001ell
öÛä2æ2OR\x000f\x0017×" HRãüánl
\x000eØäZø\x000c\x0019(ß%é$\x001ak:g \x001bsýæ&m\x0000¤0ïIkóp¥åÚ0­Ê±QåØ¯Ê\x001dµàß©Iª$»3
©\x001b5©ûÕ¤Ó!G)~f( uÓýuèg\x0000²Xô« \x0017á½]µôè]\x0004i\x0003\x0014owÚGÓÍáÖýÜ\x001e1°sÓ¸½'AÎ_\x0013usntÿ¹q\x0016K\x000f¡@*±~^ëæØèc< Ë^Öâ\x0001i\x001eHÇÆÎßm|yâØù¼Uaå?Û«B)t.!\x000c)tî2ã»Oï\x000cùÁÊÁó;­Ö\x0013éTÃP=uq`¤å&\x001aQî\x0001çÃ¸\x0003¨&}k
 Ê\x0015eTån\x0016ÌT]T¸ùRñË¶¿-\x0019'ÖÜ!°À)\x001eðê¦\µ§k<ÝçD¨3à\x0019Çnq<Sã><Ê¸÷Y§ÛàX]bºç\x0008±\x0007\x000cO\x0017­ñl§ô¼/\x0001^%\x000e\x0006¢ÓòqÝ4«ñ\§ô¼\x0015<ë\x0017¾H/ÊáP:\x001cP]x¾Æó}x¦~\x000bv¤q\x0008Ï\x0004ggñB\x0017:ñ«¡M÷×ìâ¢5.ÈSõ$\¬áb\x001f¥Ú\x000fd8Ë/4èP^]ÕÁ;a\x000f^\x0015\x0011w±DÄ·ó©\\x0017øW\x001fg\x001c<óÃ4^«;µ²5¹¾:KÏ²ôvjå}ë¢Ã\x000e{éx²ÖêsÏtrKM¾Ø,^c2 ÓfXorÑ7IÏÐzáóåãâ¡g­.¾Æf@§Ñ°Nóe¤§øãZ+ç\x0016pR­@c3 ÓhØ¨Å\x000f$R\x0013&\ôåè\x001etñ5F\x0003:­FÚh¹*ñi+.\x0001%-|>ÆYñ5F\x0003:­FºjJ4Äg³ÍõÊÇ"¾Y¾Æj@§ÙH&?·ÉËÛ/;ÏÉQpåôN+Æp@§åp°S}(»Ïk´">5)>l\x000c\x0007v\x001a\x000e
mËæ\x000bâ\x0013\x0004®Ï Í\x0017\x000eÜ=»ð\x001aÃ}cé¹ wºÏ@Î_Û¹Tp(`ÜÅ×\x000eì4\x001dÔyTt³|wÇ 9¿Î/\x000fûs|íÀ>ÛaÓNT,_þ¾Ë(v\x0016ß¤åÀÆr`§åðé
¤Y·\x0018%g7·I¶Æl`Ù°\x0018ÃNï\x0019væµsÞÊ¥ÂÆl`§Ù ß\x0006ËÉu|r#çgOnc7°ÏnX¤Ø?ßÕ¨ÒÊeù%}Íò³Ó'£±\x001bØi7¼-\x000c2»ìFÌýäH~fR1ëF1ëNÅìÍ=sÏË÷\x0003\x0019ä\x0016L^t£u§KO	8rÙ
53FU2Í¡g.¾F3ëNÍ\x001cT\x0017\x0013\x001fû-\x001fLøì¤zÑm\x001c¨Ó©÷.pÆËA^è´dü)ã'½\x0016ÝhfÝ©\x00058/ifóÆÉ--~Á,_£u§SïËEÒY~ìVEgàTòøÃ¿íù}ÿÖéøAñëál ô¢`Èq>ð>Òx·x×¦>oï#;§\x0016OæÛÇ\x001fî÷\x0010ïû>4:ªÜÉjÌbåx\x0008Êàl`#þðó\x001eáÏ}ª¼Ùài(Óh$\x0005ú$¿î!þÚyC:Â²\x00155ßáh\x001cD\x0010æ\x0011ÙCü¥\x0013ÑSNq	rð-\x0018»ò9ûB»Í\x000bÈ\x0012Þ\x0017Í1Jª\x0015`§ÁZªZb`ËuÄMª½'¥%ÚKi¡äÆRÃ@\x000e\x0018Ù`%¢à\x000e=}u~îö>÷OÊÑç\x0016¬yøÖ®Ë¹>æùq\x000fñÇ>Dª\x0019Ôå-\x0004ùÐD(o!0|hÌ~ñUÅÞ^s«cï!6\x000fØÌqÕ\x0004èÜQp?uwk«
R×z\x00002É\x000f¶]ºÙæ\x0017¯¢{ö«/z\x0010£ÞcÔ¥ª÷\x000b½kÞÿôëÝ³ëû>Ü?þt\x001c3\x0019\x001ay[¢Y\x0000Ù\C,Wåp¨Lú9^Ü\>ÿîâúìúºk>_ÇÅ\x001a\x0017Gqz{,¸äÞ2n(a¹x((<«k\=\x000b, ÉºH\x0017Ê»1\x001cºÍ\x000cá\x001a×\x000câÒtEÞ\x000c6r4)©x*Z[ÓÚAZã83LIøX\x0005]ªÄNêjT7ªÒU3\x0002))#p\x0015QÉ\x001fAje{\x001a\_ãúA\oh`LN\x001fZÊzt o\x001bàO¶mC\x001b\x0006qÓ^EÉmC©ÎÊ¾=\x0018\x0013\x001aÂ5n\x001cÄuËÍ-'\x0018J<Xp½<ªBØ/N\x001eÅ­Ëty\íæ5ËÌÕ¼y]\x0011¯\x0011s N´y¡µh&\x001aÉsx
)TÎÇ6jæxÀ\x0019âmL\x001a\x000cÚ4¥QB®T® òÅ E¾Ò;x\x001b\x0006F-¹.rÃ÷.J½OTFÊ\x0002¤yÓ<ocÔ`Ðª%¶<Lä\x001b9ä	\x0011@x\x000f>$\x000fñ6f
Æì1d³dÚ¸|%\x0004ý§²mÐØ6\x00185nP¡ë}nòy\x000bQÊýð`Ht·1n0fÝt\x000c®ä\x001d\x0006Ï®9\x0004çve-§âm¬\x001b7\x001d=äAðTó $7ãf\x000f=¥\x000eá6Ö
ÆÌ\x001bu!®áÑ1n\x0010_G\x001fJE\x001cáÅÆ¼áyÓÑ!_Ô\x0002XÉB
Z.@híxå\x0010ncÝpÌº-ÕÞQN[8çÃ(Ò¥*ÛÓà¶÷µ1ã¦©U.\x001f¶@þ2®~t"GC¸mÃ1Û¦£vP\x0016Èld^\x001f\x000b¯=2ÄÛØ6\x001c³m:BÈí§r\x0015\x000fWµJ
=ê 5v\x0002ÇìDb-Y¶O[)¤«<iu¨Nx·±\x00138h'\x0002³lµåÇ\x0016pÆfH\x0013ñ6v\x0002\x0007íDÚ¥R	\x0019¥ñÁ¹/p°AÃ¡Æ)C¼¡ÀAC\x0011k[ðNö\x0003)îÒpè¥hW7B\x000f\x001aäê\x0014U\x0016·`½ø
\x001aOµuc)ô ¥ðTM¼\x001fJ\x0011b5¸\x0013ù½º1\x0015zÐTP_'~óJÎ#§µÒjEëC	©C¼mloÐV¤ÿHyH~¤¼\x001fä1V\x001f|^\x001aâml\x001e´\x0015ÉS_`c:w¬Ì,\x0016åp*Ñ6W =x\x0005¢­ÀÉ«tÔ\x0002\x001f5I\x000e¥£v*ÞÆ´éAÓF\x001dD8+)Ý+EÙê5²¦x\x001bÓ¦\x0007MÛÒFÆ°|}i~¢å©õÉTocÚô¨i\x0003¤¢»,_'µé4ÐPä{(«j·1mzÐ´Ñã8w\x001b	.J\x0005¸ñ:ÜÕiw³{&/§Ý\x0011õt¡pÒËJZgRï¥!×©"Q:¶Å¨¥Ú±WÚÔF\x000eßÒ©?\x000b[jßhÖÂ¿°/l\x00185Í\ä[½£Q~gR>\x0010ô©bÖz\x001fZo°$#çç·ò8\x000cº$\x0002ÄCE\x0005\x001bd:bkêÑ'±+2¡\x0018êS\x0005,¿¢qêhmé½Âe¼4øJ~ãåãÀèVbkºçæ\x001fä
ùâñ·»?½øG4\x001eñàÆú"\x0018P7Çî\x00177//^}söâÝÓ\x0013\x0019+<¬ñ°\x0017ÏÈ\x0013|Ú¹âD¸êYèP>>]óéN¾tl	üG¹°y[úëà!¯¬\x000fÐÔ¦WÉÃ
|pÐQfú\x0002¸;wÀ­é\x0003´5 í\x0005¤>«ü=Ê\x0015ÇC,\x000e5që\x0003t5 ë\x0005´¥íXPKëe\x000fFu46Þ\x0007èk@?ð\x001f÷ì¹;\x001b\x000e+ñÐcY\x001f`¨\x0001C·\x0004\x001d)¬\x0008A\)Ç#<é\x001czî\x00035`ìVEË`ÖN^ÒG0\x001c0.]|Õ3.)iÕ-Au®ù½bÝ,A_bêPÈ¸°5#ÝvÄÒ
D\x0019
\x0002äc,ÉR`\x000fE*ú\x0008\x001bK\x0002ý¦d×
l	Ç\x0002]i\x00002oK ±%ÐkLè¡wí~Ùað
K£ÚC\x001d}1nkbá\Ú;N"¥mXÚémØèjèVÖZ.èEè¬$:\x001cî[º\x0010pÏßJ?¿õæîÓçû/Ç=o3\x000f1ÚH¥95ë=·¯ÙÞ\Ü¾½|w³5\x0016nÇB­Jfp´æ\x0008T&ÁåN
\x00157cé\x001aKÿÓHËÔX¦CZÊI\x001aqÒ;
Á¡ê\x0003Gt3­©l\x0007\x0015Í9ÎP¦f9¥ì!ã°ÉÕL®GRZ,Q¥#\x000bXÎóô!Lí+_cù\x001eQ9é,j¼ú¥Up9Tô¿\x0019+ÔX¡GZJÊµFêIZÜÊÁ9Û±b\x0015{¤e¥Ê\x0018/\x001dèK.µ\x0007[\x0010lÅVvèÒtw\x0016S©)+7|½e\x000e½øoÆjt\x0016t(-¤°²ç\x0014\x0007µ=ï&\x00164ê\x0001zô\x0003
àÎZ+Ù@\x0011W))\x000cüïÍTÍI£Ôå-oùb§Ô\x0001\x0007=£· ÙòÐ³çÓïSZ\x0007v¶ÓAÂu¨-ÃV,l¶<vmùò ¢äpRÞ<«ù¤¹&ö<6{\x001e{ö<x¹`Ü¼ô£á³À&T\x00046{\x001e;öü­\x0003Í®Ç.\x0003Tf=Ð±ä\x001a'p¢»<Îl{l¶=v©zi\x0000»Ó(æÚ«CóV,Ýl{Ý³íBþà]áÒçÃ\x001dJEÛî4×ÁÞì8K¬wÛ\x001eS\x0002Gõj<è\x0006\x000cyt\x001amwR÷éL'\x001dÈeh¡\x0013 Ý\x001c6{÷ mê7÷¿ýùîñó§ãl\x0014h)=\x0016ø«*+:ß\x001fWµÄÆ/oÏn._¾¹¸yûÔT¹\x000fk>ìåK¾¡æâ/¿\x001dÏe?¥ÀX\x001f|\x000eî\x0002Ô5 î\x00044°ëëf¥K\x0005\x001aúK¥AÊ4 ©\x0001M¯\x0004ÒåÇ±d®\x0002»ÿt^ÇºølÍg;ùt4¥>ÛXn<gJ\x0016fºa\x001cz\x0007ëâs5ëäÃ`Ké3F\x001eô^.\x001aA}|¾æó½ò3¾ÈOË\x001c\x001bÔ¥Õó£3	\x0018jÀÐ{B\x0003\x001bh8¹\x0007M°ÒH#\x001c\x001a+Ð\x0007\x0018kÀØ+AÜuÝÔ\x0012ïC½ëãb\x000f=z÷ðA«£{4V
èË\x0010\x0016ÂC­4ú\x0000\x001b\x001d\x0008½J\x0010B(\x001d\x000cÐËh/Ð»^)Z1õ\x00116J\x0006zµ\x000cMÍb\x000fÁ%\x0007>«étóJ&\x0015ô¬¡æ\x0018Cï9V.ÊÝÐF÷­èK»(;-Cr³ZcücçI¡á\-®¤#kõ\x0013] z\x0011?·;·¢öºkc(Õ¬¾T\x001f×y\x001b0è°ùP{/µT69úì8 \x0016\x000b~^+â®1IåÏ[ç\x0019Ñd5Á.[¾$\x001ej:=}I~AjãähÛÄ\x0005À\x0006Ðö¡:AtªÇ¯¾¸\x001eøâ»aJVIvDÑþ`­ÔFL½\x0015ÐÍ¨ßíî6RòDöfãÎÝö»>/{²,Ó~»@±\x0006Å!ÐX\x001aÿYM\x0001\x0005\x0014wn·×§\x0000Õ5¨\x001e\x0001Õ%üa)Kç\x0001» qn¿ï]\x001aÔ:³\x0003
Ò\x0017dhQ\x0002uá\x0014 ¶\x0006µÿÄ{ÔÕ nH¢®¼¼h+ÍæA'\x000eØ\x000fÚú\x001aÔÿ\x0013K4Ô a\x0004Ôby4¢ÒªB\x000eSøª=Á zjÕ½æpÔ`A^L,­KôÂG·ÚÇK\x0019©mê¡*ík.>~~øøþãÙ7÷\x001f\x001fþvtÈ»A«Ê\x0008½ä4eBñ=á`3¼Wo_¿ºzX_½þÓåÓcÞ\x000b&ÖØ©éYG¦¡^¹zUp0·¥ÒÔ¦ÒäYF¹ØÍI0ÒXS\x0006«\x001dÐÑikL;ðÍ£9\x0007\x000e\x000cùpÎîgI\x0006\x0003<4j¢ÒÕnà\x001bU:PP\x0015)q\x0008§üâ¾ô#Ç\x0007Ï)Ù.ü.F0d\x000f7vc\x001a3ôcBð¥u\x000e\x001a9å` ä×\x001djæÜY¥Ø©]§.N_\x001aÿzÔå%\x000bË1÷ê\x0004Ú\x0008\x001am\x0004\x0003ê\x0008Ly	¤ª\x001an`«Ï~p¤pÿ\x0011j\x0012ác$W®%Ö{'ý¾´v%Á÷`ög?m]²ÐJ1J×\x0002Sº\x0010iyÊ,mg\x000e¶ÞÝjì92v÷0»Òýôxÿ÷V\x001aÓ%W®Ìù$ÓÍ»*#ÄU´\x0007c
ÔîùÍå÷W·ÇÛçÙ½Äø©G0¡Tâ;Di\x0004­\x000cÆtÎÓfÌ°?s+Äú\x0019êå]Â9ê&-y¿\x0003
Ái^[éÄ\x0010\x000få\x0002ôò"ývÌAb8¬á°\x000f.Ø¹O¾\x0011Ãa©­Ö\x0007ÛúuÀé\x001aN÷Áé ¥O\x0011|)Tw¥\x001eÇ\x001cÊ\x0004Ý\x0002\x0007Öí\x0014¬Û}Ö³\x000fwg·_ÞÿùÏ+\x001b
Êã\x000b¨Ã!­å\x000eåáÐÎ»8»}wõæÍ}'X\x0003b/ ·¿ä§óT)\x0008wt\x001a]\x001f ®\x0001u7 +ÎÙG'o\x0013h¥R>mÄaÂ\x001e@S\x0003N@MõÜ\x0002Ëp\x001c­h\x000fMlíãs5ëå\x0003\x0019Oâ­§\x0013
Z\x001cÈx°£Ò&>µ¬r"òó_ïKfð³Oÿþ`Ö^ ¼ôóH¶æä\x0017(Iïs_½<ÿîòåbënÏ½¾ýÃ;úñªÙONV99¹\x001fuiQÕ¡22\x0003\x000e44ôÖí>Ô\x001fÓWnPÑÓOú[^ß=|xÿ×³W\x000fkV¹\x000c¶^\x0002rÄ
eJ\x001dý\x0014Îô­ß¼¾úãÙ«×¿ûéîç»O\x001fïË\x001föÁt
¦{Àh8´Yî\x0005¹1ª[a\x001f©ÁL\x000fXº±Z)kQ²ýÔ®-¡20\x0003fk0Û\x0003¶<¸Kÿ+\x001e\x0018qY¿7ØpårÍ§ |
å{ \x001e1ÒÄÑËõ$ÙßÒdp?ß'­P\x001e0ÊÔÅm¶ìçyio\x0006qr¸bM\x0015»¨\x000cdç]ïhZ\x0000\x0007ÀÝ¯mÝNUî\x000b\x0015Ý5;°Ô¹Ë°ìRUZ(}]C³E\x001a\x0016 R\x0011ùªáñó_ï>ßß}!ãõýûû\x001fÐL¨~÷:±ýÇß\x000e¨'èk£M×6Ò3çé®q¹X$­æò]-aýë¤\ùùw\x0017o//ÞñúþêòÕ«§,WÅikN;Âü§°p¸LKY8\x0013N£NÂékN?Âé\¾©%Ðä¦\x000fD *ær\x0004ùUx\x00164Ö q\x0008\x0014²Ç@í2yk\x0001
A5%ÏrB
Vía;HmÈ\x0013)\x001a
ÆfÒ\x001cK¤>ç\x001dÍ6g	\x000eôùK¤j´ú¶0³\x0015\x0005m\x000e\x0013\x000c¦\mH &"¹|0F&P\x0003'!m\x0013\x000c§9ÙH\x0015%ÁgÒ ¤ZÛS6ç	\x000eT©ÍÛ4]6ÏQDª\x0019\x0014O"RlÎ\x0013\x000e§¥14Q\x0002Ei3&CÂIÔ=6G	ÇÊº\x0012§\x0005º/ç£=ÅDªüÜ¡·u¼&ÿP
8xûðå1S\x001d
Ò)~ÍÊ<æÍé¢Á#ßüíëw7lý* ®\x0001u7 Ë=\x0008p©&@O\x001d¿ä{ûY@W\x0003ºN@J@ãÓmÜÈEAËé\x0006õµ\x0011êäó5ïå3+\x00005íqhX4Åp\x0012]K\x0006¬\x001a¾o$Dqà´É^
QöÊ·ù!:\x001dªCþ¡¶~ùnñ\x001fßß?~z-ù:â\\x0006¤û1á¥¿Í¡\x0005»/<\x0017¾»NW÷WW7OÝÝ+:¬é°.zqÕìîô¢7¬b¬}éõâé\x001aO÷á¥½/6Úúe\x000eÉ\x0017µ\x0017<·oùzñLg:ñ¨#\x001f]/ÅxZ2\x0013Õ¾~î¥³5í¤Ó1ç	\x0013]¤ÂNk-xûz¥ÎÕt®Îé²ó(ðÀtÎð=\x0018¾Æó½xÓÔ\x0013\x001e¥c2l<ãsOÚ	ºPÓN:O¯ó\x000b\x001chzcZè8Æâ,]¬éb/\x001däÐ[ÂÓ(²ã¾-$»96h\x0014\x001etj¼äÕïî|^î'FG¡S8yh¡ÑxÐ©òÒâì[µL\x0001Yø\x0010dç¯nz½|RN­Hòû&]î"ØÏxBp%ç\x0004_£V S¯\x0018zÃa>ãÄàZ°r\x0007áçÍ	¾F¯@§b1\x0010r^\x0008É/Rt?Ë¯D4Lê=h4\x000btª\x0016Nm2^ê\x0016g;Â&ññ\µ	¼Fµ@§n1Få4ÏÄG+ùÖn¼ã\x000bvÒ#ÀÆÛÃNwÏ@\x000b³âP ×!£f
\x00076ê\x0005{ÕK0"?*ÈWJ«\x000bU³âk\x001c*ìô¨lÐlØÁ\x0010åç(Uw4\x001eØ(?ìU~a§ül²lÅ§rô±Ñ}Ø©û\Ò-J\x000eïÒ¾w¹êØ6\x001dììækt\x001fvê¾eÒ)«æ qa[Î®Ó_·Q}Ø©ú\R}òuud¿Å\x001b/\x0017ñ0i8°Ñ|Ø©ùh°·\x0011ÃVÕ\x000evgcvóiUóq\x0003[¥ç+>EoÕø"\x0014Ë1ëÐëF3ëNÍL74Ã¾²eãÞáÄ\x0017&\x001d\x0017Ý^u;5³
%ÚÜ¢û\x0013ùM\x001e]Ýh>Ý©ù\øLtKv\x000eóÉu-ùÏC7ªEwª\x0016\x0007ÜFu\x000bGùPÅ¢[fùÓ«;O/¥,ßb¹Y¹\x0018~úyÏ4§Ãt\x000eGm\x0018Cs|zwmÖíÛUõínFuUß¶ËÑø@½<Õ¦+\x0004
¾õuß=JFíîþQú»oö\x0012^ÞESóûÕ;M8-L÷0]·0-ØÜ¡6;[\x001cx¶ÞËë'§ã`ªº[Jþ¡ôüìý\x001f\x001fþýËýç£n*ò-)i\x001e#\x00166\x000bûêðÝÙ³«ëg¯ÿðîòí:\x0018Ö`Ø\x0003æ½ø\x0008
ÇÙA#`_oÁ.0]é.)¹xhg(¥?\x00059ÀpàÑ½\x0003ÌÖ`¶Kb1\x000fg¦ç´ãË3\x0017Æ¯ß°:°\åz°ÉYôh\x0000\x0012»µÊ\x0015.?ó!¡ÙaÐµÅ\x001cæù]6¢¥Ëx\x0006°­tW\x001f\x00053
é\x0001Ó%dK=ÿ$tæýwTn¬ùÐõ1Î£\x0013\x0019=\x0019HTÀ±] É}cdn_]¸Z]<þýÿýð÷ÿ|úuÚnX¼3»\x0012«Pñë§Ñg7ï>I)·¯'\­'Ö¬£TÈäè\x0000,\x000f* ZÂ: W·!\x001aÉt\x0008	ÎwDÕd-\x0016¢¯\x001b6\x0012¹Èm'rAT\x0003}\x000e¤c'áu\x0007vÓ6$_#ùÍH\x0006BËåÀû¨u¹Fü:ia#R¨Âv$¥sn2IIÉ}*Ùr?ð®¾
©z\x000eNHÕsð*\x0013²½IbÈ\x000fr¸»#n&ht\x0000lW\x0002ôéøù
Óù¾0á°#\x0007ÛÏö!·C¡t2-·9êg/édøõþF&Û0ÙÍLo/)n@¼ìÛgå\x000fäAldj\x0014\x0001l×\x0004\x0006±<\x0016åùhüØ!N;dW¶15\x0000¶«\x0002
Mk\x001cÙ
ïb¤\x0016ådÛOþ~Õt«u4.ÊYÑ3\x00124¯Ç·UsãÉhÕ¢õ/¹\x001aºâ!¤Û QÃ\x0007æ+4Ó¦c\x0004%zä4/\x0003%ðãì\x0001\x0017ynÇ}4ì!K?m3H\x0006\x0001¥!týßÓî»T»J²ÛûÇ_î?~>ûîþããû³û\x000f\x001ffÃ \x0001\x000bJn¯à£d®ý¬¤ÛË\x0017¯Þ}wùêæêìæòÕëWë¦Æ4\x0003\x001aÙ\x0005LÂ»P\x000ccË\x0003!')]MéF¹Ì@X\x0019ÜN\x0012ÝKjî\x0014¡Æ\x000cýT«ÎÞ-Õ
9\x0003\x001e\x00053(oÞ\x001cå»Ë¡é\x0015*Ë4Áò\x0005s'S\x001b÷Óõû`U]	¨sÓß½ÿðááË_\x0016¦AI)Gk%FÙrÏ<\x0010®~qu}ýúÝ\x001f×¹°æÂ\x001e.]l.R¤4Ë-]ñØÕÅ/¼ÛÁL
fzÀÈðõæ5
$\x000eC°\x0007ÂzÛÁ\
æºÀ$zA\ÊV\x00170\x001dYb4uª\x0017Ì\x001fâß>ÿùî7Y\x0015½{þááÓÙ÷÷\x001f~ÿH9N-PÉ(¼~ÿËÇ¿ýËýÇùþîÃC:1NÅ®PKðÒß\¼D§e]ºzÚ<\x0011ðêÅ«?]¾:ûþâúõÕmIg¾~}{öýå«o®.o°*-jú{á(j°1\x0007÷\x0014Rå%.W\x001amu\x001bGó2NIº\x001e\x0016ª÷Ù2SI£;·>\x000bêk³PMvOþ^fX¨\x0014Êõ\x00195¹Óê,£ú O)Õ¤\x001bì¸TU¾>RWnÅ×"-©ØHQ¤S¢¦3î¥\x001a¹üæÜ\x0006*
_¤\x001ar/$ÕèO¹\x0001±\x000eÃRe>_j<w,U\x0003\x0005Iª§1\x0006²§`XY\x0005Å
ÆÕ$-º°\x001a'Ç
ò+ç\x000cê¿þû%VºJÊÂ¿½ùòþó§EçßÞ=>Þ}zÿñÓ:rÒï¹\x00075\x0002ÐPº\x0005æVH\x001dRà\x0000³\x0014¿;{óîêííb\x0012n/nn.n¯^=ñ²ÓÂç-1\x000b4BÈÊj\x000b,fxóÏ\x0011ùq\x0012öþÛ_M}ò\x001e¾|¾/Õ\x0005«¸@)\x0012çy'Ó¥-»&:¹¢Ù! \x001cÔ\x000f¯ß½½,å\x00067·\Ïºüó×l|ÔúÙÐ/e$ÉK\x0000¹«%6>e\x0008\x001a\x000f²\x001e6Ä-Ñ¸\x0001¸x¾4\x0019JtZsÖh¢\x0013ÁY<ôûàè°ÜÀWÕr(C)ç%Ñð\x000f>AéÂ\x0018]2Gvç¥ó\x000fìJ%¸³ÄúË\x0006­ä$õGQU9§¥ï\x000bÁ07ï9¨\x0012ØYâ|ñ´:*X#b7"ºüæ\x0010>WÙÊ#Ø#J£EÔ5¢îF´ÌgD Ï°e÷ðµì 35é¦ÓKIwþÆÚð-\x0013oé\x001b\x001fÞ]¶F´Ý\x0001d\x001b(9@	O18\x00170ä\x001d®Ftýß8äw$EjÀÙ\x001aFôÜ\c
1Ô¡\x001bFfGâ2Þ;K1¿ï\x0014íô\x0006Õè\x001bÕÿ¥c\x0006F²KÃç1zöB\x0016#4
\x0007ú5\x000eµ\x0016È\x0007&Àùr\x0011Yã$4}¦¡9ÓÐ}¨½RùfNfÎ/î
 \x0013F;!G³o[-£Y\x001fÓ_ýþÏw\x001f¶øç\x0006Ë\x0005=X~ÕÎXöÏãa\x0007Þ77W¯_½¹x*à[cb\x0003Þäw4jöY¯e$yÂ|òrÞC©kJ=@é0'.Ñ\x0004D]¢\x001d\x001eYS£\x0013`Ú\x001aÓ\x000e`ÒüÛ|Ï¡\x0001c1¹¥\x0000}óÜ\x001di\x0012ÓÕn\x0000:ë KÓrø\;\x001bµHó$\x001fÝ×~\x0000\x0013bîæNÒDñ½\x001dh>æ1Éø\x0004¡Æ\x000c#áÜûòÑù\x0003î¾ù)(cM\x0019\x0007(\x0015G3)}Fj\x001b\x0008óð%«\x000f³²¦XÈNNg\x0010g°\x0006½ó\x0008§9ÁIFmÂÞ\x0006
Äi8\x000bI[~ë'Nu
NÓp~Î\x0010Mn>½\x001d\x0015¿ÈúrÖÕSö¼³QI0 BPb\x0006\x001dã\x0012Íâ¼ÁQL­öºVÕ1wbüöþñ·M¶È³§\x0018ww\x001f­D8¹+ã·7/7ÐêV\x000fÒ\x0006ÎI¡!G4#w¹+þüË\x000cßYZ·/[WfÙßÞ½ÿøù_¨iòû«°´\x001c÷¤Á[A`\x0003\x001fª\x0010üSêöâêÕÛ¥òÕSÍYjX¬aq\x000cV\x0017ÉÒ\x0004c8¾áyrO)þNX]Ãê!Ø¥ÏwU4rahY\x000b\x0004´OE`;YMÍjÆ\x0004KMÃ4«VW\x0018\x001fxÎÊ?åEuÂÚ\x001aÖ\x000eÁÒ°ulëâ£ÄbV}\x0013íXW³º1ÁæÜÔ¬c\x0003çÌQk±­Ê<\x0011Mêõ5¬\x001f\x0013lr«øy¦	çÌ¢¤ÄÊ£¡yÊ_éd
5k\x0018Ô[¦8WI+ðÅ§CÚr'Ú°±fC¬ÔNÊñÃ!X)xD\x001aÁ=ø8Ð\x000f[ùd\x0010ÔÞJ÷\x0013`çZ3ç«~pB\x000cÂi\x0014\x00174\x0016\x0001ÆL\x0002\x0000wI ôkÃ]\x0012tðNhÝÔ,4j\x0016Æô,Ð´u_R\x0008²ý
¡Ø\x0004ëO´\x0011\x001aÕ\x0005cº.-õ\x0001áe=kA\x0018·,mÔ\x0001é\x0003 ²D6¶SZ¨S¶\x0001wêÅæáà\x0011£À}ög\x0010y\x001bDÔA`á4Û\x0000[kð%wõÒ"[h\x0003j±·'Ò^ª\x000cÈÜ¹´%]­×ì¢\x0015¨\x0016½Zð¾\½ºÛleöû^­WÕ\x001c\x0001~²;{þðùóýãýçM/(O²f\x0019z°¸`ÖÊ\x0003²7OæA»³ç¯ß¾½¼¹|júWMnjr3KÎÁ­¤Ì¨c\x0012£\x0007~\x0014Ã¢Ãè®Fw³è|\x0012©_±ûèhL\x0019B\x000f5zC×¹gÛ2÷ü\Î/\x001b\x001c§îBCäoáw¾Å(:°\x0007o´#Ñ¼ð[óÔé\x001cCo\x000e)ÌÒäÀqpÇ¸r_öÆ	{xê]n½9¦0wN<Ø¡)-\x001cµ×|}NjñI>ÆÞS;¨Ô¶![!\x0013\x0003ù%\x000b;79Æ\x0004¯N»g
\x0013'UÅ\x0018µdcZòQYµs]\x0004ee<ù2ÄÍQÅ£JÁ,SØ©¡\x0016r4KòÒ)8©Q¡q\x0002\x0016%¹ë\x00070ª'µf=©9©\x0014¥èI}¢\x0005¸ýWLg«ÑG·üo\x0014E|óÈßoÏzÇ÷Û\x0004©­èÈäá\x0011wà6aÿ\x0002o^'ì«£¾×þ£¦«§
PSÑ7ë#o\x0018«YÞt}|êf>\x0004njp3\x0003nâînüÜÌ
¾dwÇ#Ê±ÛÖÜvÛ.=27Jú(\x0002§\x0013»\x001aÜÍS\x000e"ßBy\x001f3±\0¹UË©À}
î§v
ÜZê½\x0005®äªiN+ïPc\x0019ljØXâÑì¹\x0018/\x0019E\x0001iò~îXsÇ\x0019n´EÜénÏ¦ß\x0017
|*:]ÐlíæösûèK\x0011\x0006u"Ên®1%4¥N*ph
ÏåñQïrò­¤i\x001a£$¯K\x0015ÑEO7¶\x0007f\x000fZ4H«6(\x000fD}à«\x0012×
¸\x0002·çA\x001e5¼\x0019\x001b­@ÀÕI÷Jc5aÆlz\x0002Í"§âKÖâ¨$<\x0014Jé\x001d#oì&Ì\x0018N\x001fãéâ\x0013¤Çhy§÷úØ5´¼10c9i\x0012/çyÓÎ298y\x0002óOWw7\x0013¦LgºÆ\x0001ËÜ Ä[U%}ùÉÐç\x0010yc<aÆzzÏ}ù\x0012yRìe 'Ô\x001d»vccpÊ\x000e\x0005Wdî½\x0014{]Ò½Á#1®~òö*1¥Î ¥\ ù\w±²ÏÎø\x0019³ m\x0000z±¢ÕåsÒââVôéBÌ®\x0005À~B\x0008ÔÉ6Ï>Ü}üé×Mw	½K°Ðò¶nQ¸yxÂ\x000cQîÊ³ëWÏ¿Û5&`ªÜz¬%ôi¡$ÖáSÏhÛ(í>¥­)¥BlKÜÇHm+&L~ð õl<éD ®	[ç45§\x0019á\x000c¡¤W\x0005SÊT%8Vò²\x001dÔÕ n\x0004Ôs\x0011\x0002µ%=5z\x0010Ð§\x0012¼7âþ1BU·"xöðåñû÷[P©Æ\x0013~©\x0002sT±¼@§²Àxäí»\x0017¯\x001aµ]Ãb
c°\x001aò°r
Ü¤R;-¶-\x001eq»XuÍªXCò7%{ºÒñí»$¬EûdÚb'¬©aÍ\x0018lî¬Sý8jÖ;IÿñG]°¶µc°ÔHR2þ½\¬.©ôæTÛÀÕ°nP².7ÙÊE\x0014\x0012õ
([Ö?\x0005Ö	ëkX?\x0006\x0001ßÒY*^oT¥âÈ\x0003i\x0017l¨aÃà\x0001ó¹\x001f\x0011\x001d°¸;`R:\x001e:Ñ65l\x001c¬ÙU©\x0000\x0015\x0005äØ.u\x0015Oæ¬õÁVq!¬?ûhmiv*pkÛä^\x0015ÇÅÄ§ïÊ]´­\x0005\x001b3a\x0001Jôå¸+åTæH|¶¶1a0fÃ¶l[,®¶\x000c hO¤j\x000f[ß\x0012òn¨[V÷@\x001b'o\x000e´}x²¥ÞÆè¹
ñc\x0012nã%<#i'	_ßç\x00129³ýöîÃ¶\x0002;àjJÔÖp\x0017Aíá\x0003\x0015\x000eÞÞïµtÈ¹í·\x0017O*¬M
lF\x0011%\x0007;]\x001a%\x0004ëä¦ôºs"^¬v\x0005\x000b~\x0018ÃÖE\x0005'7\\x0013K*\x001e|0îá¦{ú¾KäI\x001ft\x001dûòþñáã¿=|ú´ìÓí]sPÞpÇ!¥!7LÄúà³4ÀH×²wW7¯_}ûúöv\x000bt{\x0004	~8
{VË-û!ÕÑËnö/\x0017f¹\¼ùp÷S®0ù?ÿó]þòáý:2¥C8IÊCíxpÞ2;½\x001bäÍõÅó\brvùâúj\x000b-Ö´8DK÷¶°³$Qf¸¤ÝD7\x001fmÇM§Ð7Â}FAË$Üo\x001f>þ¼ì»/?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=P\x0000ÿÁ©OöjÞ\x0004ohÏbP¢\x001d7¾\x001dÓgXÄÃ\íD)³S\x0013·d§(À à§7W¿~K·JéÂ¬\x0017Sqû·»ß\x000eÖØSRM\x0000Ë­xâ®Õ:ûËùÿ^\x0003äãíj(øÙÊYsô/­\x0016ÕË¸ô©`±êÝ\x0000% È?VB\x0001u,BIá\x0005â{`¡¤ÅRa\x000b\x0012º\x001côj$Æpµ@áÃebã@Ã\x000c\x0005R÷÷!-È?VBÁ$\K&9\x0012*VT2ÏP|hÊÕsq¸Ü;!'\x001f®n/\x000f©öÞð¤\x0013z² mA\x0008|fÆY½|´¨F'\x0017§g'kÐÅSó)ÿX\x0007&\x0011\x0002WÀÐ\x001926\x0010ÄÓjå\x0000o6ÿX\x0007\x0006ÿGòlMA@Y#pò\^\x0010ï\x0007£	^
Æ*îÞZKáë}N~\x0007z±ÊÜ\x00062jú±\x0012LÊ$å3%Þz²^ÈgZPÑ·\x0004&®~3ä?ù\x0001c¦SZ\x0003\x0018"|¦FÀ$\x0002VK\x0006ÓãBÙÞ _\x001bÏ)\x0004ùLËâ_\x000b\x0018Z>ø,ÿX+\x0019ËÔ\x0016¢¾º'\x001dÊ`	ý\x000f8å\x001fëÀPF\x0011Y!\x0017bß*`L°»-ÌÕ`hÀ9ÿX	\x0006\x0003râÁæð«<`+NÉApýo&P\x0014¬µÀ¾8Èü~y·\x0003\x0002\x000f2Á\x0000\x0016OXVk6]<+´Ò4ì-OÆjy2@·òúÁPÿ[Õ`\x001cß\x0001&ú\x00179Æ\x00032¾ï,\x0001]"Îücå1rAöetH\x0014{Ï\x001cÃz0À¬6yTÆáå$L\x001a\x0005KJÓ\x0019ÁBzmÖëµI,*emN×ùõ\x0003æ7\x0000zëücåj\x0012/$ðrE°\x001f\x000b©õúÀ.Ôyq9Û+ü\x0004³\x0011ÁÐóõÏWË5FËMu+\x0017P¯]?\x0016êûå\x001fk=AbµÖÔ¾+~@Ø\x001c,oø5Aqô^Üê÷òo¢	Êê\x0000ïß
Å\x0010ÕQøöPÀÚÕ¼\x0019÷ùå\x000f·w7\x0007\x000b\x000fA\4GQe%+H&±+\x0018|uvþâi\x0008zþ±\x0002\x0004êpà«¤\x0014¿âltMR¡\x0005DRö½û}¾õùå§'K\x001dÚ\x0013±j©A:§å|»\x0005)VG³\x0014ÅÛ'j\x001cÞ_EEsòÌü#^.¿¿º¥ÐA8h[éðu.þ)CuR\x0013rR(Öv7\x0017yvòÅé\x0019\x0015\x001e\x0007eÿöÉÿú@:Ï\x0004kx\x0000õñþòàÂü§\x0004Q\x001eXÆò\x0012*/$\x0002ìÉ\x0008Ñë7'oÿëi@°¤6@ÄrYöMiõ÷Mófdd"ìÜ\x0016H´2¬\x00145ß»ð¶$&\x0006N \x0003º1\x0011\x0011hþ±\x001a¶A<hÇ \x0012\x001f.
4?1\x0006)\x0012¤Ø\x0000	ß6o{¯<ðcÛ·sq±\x0011\x000f5Úòõ"*\x000c\x000få\x0015	·Â4h_³\x0005'D¾é£)ð´'å¹\x0018\x0016\x001bÃ{½\x001bÖ´@²Ô°ªå]c8\úVÎJ°[hth|\x0010\x0012©mQ5\x0003mã\x0014{¤ØDâ{F\x000cÒ²UÓ
myJÿv)QØ\Ó\x000b2<é©·V¸dMtÌ%RRcÏÂ¯äÚl¤Ô³#ÑÒc\x0013$»[=
é÷w×ñ÷\x001f3$Gr\x0016>Þ£ó¢c\x001d\x000få\x0012\x0015\x001f9Þ\\x0013å,6så\x0001Äóú
úÿC\x0001ùù¯~>ôìò\x0013þ-×ý>fá¾t\è¨"\x000fi#U\x0013µ\x001c³xvò\x0016Eó|\x0005\x000cGEæüc\x001dÀÃfÎí\x0012\x001bb´ÆÉ8z~è\x0005ðóæ\x001fkÐöwS¹#!Ì}§ruÝ@H"iµD<3\x0000mÓDÜ²Âè}Q][\x000fÄSÛ>ÿX\x0005Ä	;\x0011\x0015S©¬Éýdí[åñý÷ïÿ\x001e©-\x0001óÒ#DÍ9Ø\x001e$&ÜÄçÑ*gä\x0002¨KKJèÒ\x001eDÅY\x0005ÖÝ¥Fý4\x0018b7æJ,Õn#\x0015\x001cGÌ\x0018ÀÛÝÂÄZ0Fç»?z-\x0018\x001a /c\x0004ÿ+6qN[ákr>ì1q«ÁÐ\x0001)R~ú3áe©
RAÔ_¡jB\x0005\x0018ÁBh¤\x0010»â+©(E\x0012ë9ñu @ÊåyÒ©\x0017K¾\x001eeÔZ,N4\x0012 IÎSÄZä¢öTÕÖc¡odV#ú2BÎ\x0004\x0019~\x001cù\x0000\x0006³¤ßk\x0002CÕ=\x0003«\x0005CÇ,\x000b\x0006µÊòÑVú!\x000cHBa3ÅÃ+L`îc\x001a\x0019ã³è\x0008O©ºàÕ0o-\x00184ò`|äôÎ¡)G,Z,å±»60ôfìê7c\x001cÑ¶\x0011LÁãß.×ë÷5O×¡ÏdW&t<òf<J¦\äu·½|&³Vj\x0002\x0008LZÿf4Ï¶aþfä4µQ¼-ç¢\x001eQm¿[¯MV.ãP\x0005ù
\x0011Ú}\x0017!îIy\x000fùé×ûï.?RÝ¢°ücÝP\x0014:éx2ÌIpû\x0018½\x00003\x001bz\x000cÌwúÃå/¿ÎÉ P.§ø7Ü}úîæòö p"\x0011ÿÝ.\x0007VH`x_Ú$Ø3\x0018iÀÅùÛÏ_\x001d(s½W\x001f®ïH>D+¼¸<úòêÃË\x001f\x000eÎbE­8ÚÄÿáA^|ÑQÍÖðÅÉÑ§\x0017\x0017'_=.\x0019\x0016j\x0014Ò?\x0003\x0016jnÐ?\x0003\x0016jÍÑÿ\x0018_oìß¾Kó±oDòáêã;;Å\x0012QÁ¢¢\x0006G\x000f\x0012\x0019ÄåwÀ\¾ÎCrOÃ±ä
òµ,]Î¶¼,é¹\x0004\x0011¬9ÐÞz\x0018\x0002DCr¹(²\x0016PòÜ¼¤E#îÑ\x0005|z\x0002È-~V\x0001Jñï>×±C\x001eeÍÅõ£¯¨ïòýõÕÁEo*ck®\x001a[Ãl>4zÉå\x0007:¦±Ìö¿¢ÞË\x0017ÏO/\x001e\x0005¤~yÿóOßå\fk\x0014ç-__}øñ©¼eÊøóHv	¶@óH¸Å×¾\x001bß|}zñò{x\x0000Cc	^f\x0013\x0006cL\x0014ö\x0016E÷
KH1MÊ;³¤~k\x0003CÑë%C-B»äS\x0014ýÌW$ÜnH±\x001a\x000cå	^§Áh«¥\x0007¯?f¢"Y¢sË3QmP Àê¤¸sH[å\x0003¡«\x0011å¦I\x0013\x0010G@Üz(¾:\x0003D\x001f®E(^¨¦ìTèéÕO\x0017?\x000b
¦ù|\x001aNÉk¡+Påµ$·gå	0?¹û¿ýÀÐ|ñgùÇë»O\x001f.\x000fÍÈ£I<eh\x000c
\x000cXfÃt|Ù){~þöâäÍÓ0\x001cò§a\x0018\x001a#"\x000cöáp@\x0000_Þ+Éí'0üý.þ-³êæ­üã%úéÛûËCÆ\x0016«cIÞ\x0010Ñ±¶Ì\x000e!ÌiÊÃKôÑgoN\x001e·ú\x001fÔ§_b\x0006AôO\x0003üryssðl µ*0Kè9U
>±\x0013\x0002ôõ'!ñoN^¼8?{<ì½ùõþÊæea>ÆK\x000fõÕõí»÷×·T\x0007?\x0000Èåö@vt=VÉ­å4ÛñA¯^=?{öõó3*?
¨
´ B\x0007\x0014\x0002/\x001fÅ÷,L\x000bËc>kaýøéò÷\x001f)~\x0000\x001ajÏ?0~xusy}0]qTºâhÆQ±±xC\x0013È7ÞbX6TN^½8y~ [AÑ\x0004E¯BW¡\x001cCÅº\x0018\x0012_0Ñ/v[ P Àj(\x0013¹	Q\\x001b¡È±s
K\x001b¡Äß¾ûIýÃ\x0017ò\x0001JÞ
æo÷\x0018O=qjÉ
ã Á\\x0018wä\x0013dÑfO\x0004xÎÞ`@õøÑÿP¿ß]~û@;ôêîÇ\x001f\x000fÇv\x001a³m rÈàùuÂJO6h±D{þòå¡¨.þòëµùa\x0011f¢X>àßv°É\x0005´hX\x000eõbÆ'z}p\x001cG\x000bË=L\x0012ÊÅÉ\x0017Z\wIßüD»d\x0010Ib^.®~º;¨Öt\x0012Îe,Ê{`?\x001d\x0011\x0017Ïù¨Ýÿ£ÓWç\x0019\x0010C@Ì: T\x0016/-\x0014\x0015Ð3ør\x0014ß\x000fç\x0002¹Ò\x000bT(ïÉ®\x0001âØUÑpeÉ¢Bö¤Ñw\x0003	\x0004$¬\x0003BdÁLÜE\x0007\x0003Ê\x0001h¹¹EÜqÝ\x0002!öÇüc\x001d\x000e=å±1Ïg\x0014\x001c £`»:¼\x0016¥\x0006sþ±\x0002\x0008Íó.¨VÖqA(Rï%bw:'+@^¨*?WÄ\x0006^~ÓDjÉWX­\x001cë¡YöÆ7r\x001dÿv}õË2i}susõÃËÞ\x001f&È³#)ç\x0003pÀ&éx\x001fîçôèÍéÓ¯.N^}ý¸Ý¿¿ûñS4óíÀË£7®o®ÿõ\x000e.-bx%DëÂ\x0017Nö-Êä8ÆvÇ\x0007½yû¼ì*>F¸sÖÂIÑÑü~Ì£ámf\x0003Kæ&8æ óµxb°è\x0003\x000b\x0014x§\x0013³XQl°Ë±\x0016<@¥ðüc-\x001e<×}óMô\x001d\x0011/\x0001G/vçù´à±ÔÌ?Vã±¹_ñ\x0007<ZásËõ¦6<ð\x0006<N&ÉUJ¹-XðL,U°tMx()Ï?VãQfú^Zñö\x000c4.MÆgD>4\x0017¬W÷pÌâ¡)¢\x0002'Ê6\x001a%UípÂÇx	«è|¼¨üüæòæ»Ëw\x0007'i\x000bcº\x001bCY©Ô\å¾#
\x000c&r<;03<!É{åç\x001a$Q\x0001¯\x0002
 ¹!bbg\x001e*ô5¾\x0013	 }V~®Aâ£°¬\x0011Ñ\x001bS)EÔ­ u¡n kÐUS¦0Ë\x0019[	$Ã«yi°	É/¿ÿí^;²zd2ó\x000f|µåæê ÇLVÉ¼"À·\x0013µË\x0007tiñf¿É¤?Bù]Ýþã;ê\x0001ÒôÑgù\x0007:ðo®>üpõáàQ^/9¢}[G3\x0013|?;®£oN/¾:½80aöþã­ùkÊI[ ¤³o¨	x¸p\x000c¯®£\x00144Ni¹Ôì
þkÀÐÊõ`Ã§
P³\îÃK6-M]\x000b\x0018rõ2êºF2 ;(\x0008©\x0003·gïk=\x0018*ôJÿI0:9¡Ó\x0002º§Ä3xÁðÈ½SÞì6ø×¡úª4øW¡	ûòdLø3\x0008å\x001eêú\x001ezÜõX¨3`ãÚ¯¤|\x0015J fa&MÑ_gÝúj045áe¢u\x0005\x0018cxx\x0008Î<äÙ³©½\x001e\x000cc[ýh¶%CÌò¼Ý\x001fäbe·­	\x000ci¶[«Ù:i_\x0007s3éak\FHÝYÿÕX<)¶oPláÙG\x00079Í4)#\x001c\x000c°¼×Ü\x0006Þ¯_ÿ~Æbb+C3ÓÒøÀ¡Ò|þ±î#áÿr\x0013ÇÒmy¦ùG3u¶ú\x0005crÊp¡ê?e¿»ùxwóqFÐ3A¹?<º3KÛÀ)­'>C\x0017'²Å==¥æÍ¡é\x0007@ä*çô\x0014¢¼
\äC\x0017KP\x0003\x0018^ñ;E&Dª+ùÇz!i{\ZM\x0006¤y	\x0017ãÀå\x0008D+$bÀ\x000bÐ\x0002Éjn\x001b8Ú6RLy*e5OÍÂ1H ù\x0006Hqq,³<&:ö\x0014£>¢fk!\x0005\x0014\x001a Q|nËËL7\x0011ôi»§	Õ\x0004x:CüSA"º¾þó>Þ_Ùûú¨\x0002â¹¹9<ûd¨\x0018 e0\x001f,(õßE»ÓV@0/^\x001c\x001a~z"çXÖaÑZî¬[ª¹ÉÑ\x000eW)Í]»[ÍoÀÂ\x0007\x0002WaÁfÂ\x0012h}·xÔ \x000cYÒíæn,y°\­ñÜnÉs¹¼(Ù¢ð¹¦\x0005\x000b
	Ãj,4TÉ
x4;ÀWC\x0019á\x001dCØ\x0002ÅÒTîz±\x0004>ùP¼ÉK6ÔÎ w\x0003\x0016nõÈMãö8\x0001VB5\x0012ã\x000eqD\x000b\x0016ªSèO¤äéªc¹;,¤=Ñ|"ò°«¡¨¨ FË6¡\x000bå/\x0014Ì\x0008D#4«¡\x0004\x0010þ«èít­zúBÉ-ÙõZ°¸<G³\x001eKâe|Äò`è´l$·³×Ý¶áÌj,^35M,
ËHÂ\x0005ü\x000e1@\x000b\x0016òEëÍ\x0007Þ¡Krj0J\x0015)ÁÎr\x0003\x0014\x0013ßõb|!\x001be1e11%ùD¤OÝXhH$¬×"-­1|¯^J%(!±¹i \x0005\x000b
ü¯¶ÿ\x0018òp
N\x001cn
8\¥8Ï\x0000\x0014J5âZ±èD$å\x0013%ªz.MX¹ñåvZ°P°^,t\x0003::ÏínªÙÈ9ÀÝ^
XR^\x001c_-\x0017RãÈ\x0001¦\x0012,!&ÁFB¹GVË\x0005Ôôtít-­-XL?\x0014³oµ^h=O\x000eoz9¼)wL=\x0011X\x000f`¡èR­
/Õå«Q39\x0017\x0010¹¸Ý9\x00060tÑO­wq*8æ\x000b¯â¦ýOWç¾»^\x001fG=\x0010CÒ\x000e=³æ$rB(;Äz-`H.zµ\(\x0002>ðq7\x001fj¥H®$jj@§5UÚµYÿx­æ8§1k*ÔL\x0006æ1a\x0019\x0010\x000c\x0005º!Â4îX\x000c¯Î\x0017Iú\x0003\x0006MÅ+m\x001bR£8é6B±\x0010¦´ä¿o\x0001ãrúº>fpz: \x000bð\x0010J±TôNÙ¾\x0005
Ù\x0017×`_´´\x0013>]-·|9dðe\x0002¥\x0017\x000cé`þ±Ö¾8>J­y6Ã&c&¥Þ\x001dk\x0000C£O~½GJIx(rÔÀ×òú/>ÞØjéÕNt[5	\x000c\x0013m[%\x000c?Ó¤jIþ±\x0012\x000c\x0006.Ãz\x0015¦3¸Nyé;õç°\x000cÊÏÿ'H÷ÿøõ\x001ft",gãù\x0007yy÷éþà´?æ\x0002WAh{§;A'+ÉîàÞËó·o\x000eÌúúý§÷ÿøaÆåBåÃ7\x001f®¿»¼9Ü]Ñe1;CXñ\x0003\x0010\x00147\x0007mHv·Óþæâùç'/\x000e\x0014\x000fgp\x001eÎ®C¼¹\F\x000c9ìÌ²#³³­ØFîL¯\x000ef'%\x0001¡´þÁË`2&\x0007aùhÚðLõÌuxT\x001bàôTë%B\x0011ÆÙÄûñ<\x0014Ö}.\x001aa±<L£Õq(­\x0015ªò
=Cäëñ\x0010eög!4\x0008H£,µ*ð	äRK;Íè$Sè9\x0007ez+K±Eû\x0004ûÀ\x000e´gB¢\x0005\x000fm&K\x0007c%)\x0015At2\x0000&ñÞSa\x000f\x0005`\x0003 ê¤\x0006i§®\x0012\x0011g\x000ehÿøÊ%X±ËN\x0013½ò\x0008 *Ä7MT+\x0005\x0015#Ô~©1j½è¤\x0005\x000fñ°Ê5Ux¼åÅN ?ä'í\x0014\x0017ktØIyÛðÐÎô
/\x0008½'Ï\x0014\x0006gh(¿tx»¦¡41_´þIk\x000c÷he¤|±ÄK\x001bà¤nùÍNU¸\x0005P¤@TMV10ËÍk\x000båEËÕHgö±a7à¡v^\x0014û5x¢wL\x001d®+ñÊ\x0002@Ðì5V#O:R\x0017,ê'\x00141\x0016cÆ\x0011â,c©\x0000Fâ\x001f9b"¥äQ§\x0006·\x00110\x0005­EBÁrGÂù!	Qo.õVQë\x0008rØËx5\x0004Ïy¨M;mxèI¦'
\¦¥êÒ1Ä'm\x000f\x001aÆTj
Ñ4\x0004f*\x0006^a@\: \x0018!§Ç\x0004D÷ûLKdFÔìWAOnÃ
r=\x001e\x00032\x001bþ³_|føØüçïÞ_Ñõ®£\x0017Ww?ÝÝào®>\Ýþp^"\x0005ÙþV4¡S¾%¾ú$ûjq\x0011î]~òìëS?zqzþê\x001c\x0013ÏO/NÏ¾:½xô®`ÇDg?\x0003Ø1¥ôeJ®åHPG¦]4t\x0006¡£ÅA÷f\x0008:X9\x000c¨£[n`Ñ$\x0010C7\x000b?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-16.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-16.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=îÝ+ °$Á$\x001bõ\x0019f\x000fÄ0ånð`Uª×w×6®.Vè\x0008\x000e\x0004N{\x0003\x0017x0Ûp¼éF\x001cUâ¨F\x001c,6ÐÉ\x0000\x0018&\x0005'÷Þ\x00036ÀËpt£[qÀzéä0;¬S\x001c¢\x00108%9ÌÖîîà&\x001cSâV\x001c­²ÿ\x001eÝ\x0007¾ühz·7àÜîFnÂ±%mÄ1fô×áhÎómgéVv%k²ùj7	[Q\x00009
\x0007Ü2\x001a_ÒøVáhÍ\x0006*"ð]ËC á\x0008c\x0016â\x0012'´
\x0007\x0001ÓNÖ\x0019'D\x0005@Ò1Ö/ÂZ\x000b¶ªA«\x0004=¶D\x001ey$ß\x0015"ÏÔd6òTz\x0007\x0015\x000fÖ\x0018â\x0019ê¹ÓÑ\x0012Y>;þD#OuÒ¡ý¨4-\x00005Ï0à%ñX>[V-Û>P-h>\ÆÓY<&ßÍ­4Y\x0013.Ã©v34ogà(¹\x0012ÊðSY\x0018`
8Ú.S=²ÚÎ²u;0G9~¾öÞ°fÖ\x000bqªÝ,[w³ñvC8N±Ý\x0012\x000bw¬v³lÝÍÆq>¹\x000cZN}\x001e|]^SmfÙºq\x000c\x001céfïóC·óa\x0004È^/ÃNã&VRâÁ«ÇíýGÌ\x001b}Ü·*ó\x0008\x0013í\x0006¿þ;ÙºCÎ¨ôuþÅ«ëÍå·9z½7y52)©>\x0012{¥\x0004Æåô<+)Úó
ØNÒ\x0011hh\x001f±(LBAô[i]?|øi?WP&»¬¯~Ag\x001fQ]´WÜIëú*®ç1@]\x0002ê^@\x0005§¤Ìµ<\x0012¨#þ©ð+\x0001m	h»\x0001½g	J-H{\x0006iX«:\x0019v	 /\x0001}÷\x0012ç´À\x0008ÈÅ8\x0001-!\x0001êÒ;è\x0001Ìsßó+ô/y>yñðüøi¿ðpÈv\x0012^ô°\x0016²gÓcUé)\x0014UÇ/®n®_\x001dÃR%êÁ\x001acûf¼lKÎ:7V/òSYí¶×øîáñËß~ºÛî}OÒB±5RJq^Kz¶eºqYwúÝÕõÛ?½ûÃùfï£\x0012#Ê\x0012Qö#:ÅFj(I|a´*\x0013à!ª\x0012Qu#B*Ì\x001b\x00101Q#E1¢\x000e$#9:k\x0011u¨û\x0011¥É\x000bídF4\x0011ËËû2BS\x0012~BÃ)çJl;L\x0010¼Î\x0006æÎI\x0017¢-\x0011m?¢Í/
\x0003®é cR0\x0016XKèJB·`-ßÝ\x0014ð\x001bl0£"\x001aÖ¯³/\x0011}ÿy\x000e£Ê¼\x0013±gÓo\x0018JÄÐhU\x000c9ò¦\x001d?\x0006©êõ®\x000bq[Ï\x0004Ó?lh&ØÅÃÓ]\x0004øùöþ©Å\x0008\x001b^f-T¶(Â¦&jÇÒÏºzw\x001eÿ÷õÙå»c68ãÉ\x0012OvâùÀ\x0019BÑ]Ñ\4,c<[e\x0008-ÀS%êÅ³nTÄ&\x0005³òáq	.Ùt/¶YtáE.Ì¸²ÊÙux¦Ä3½x&{JZr©""\³r×ÙÍö²yO­\x001f\x000fæ\x0014
åªÚ\x0002<Wâ¹Þ3\x000bE«Ð¬%ÝÚP§À::_Òù^ºô©æR Ð¼éä:´P¢ne\x0017FæXp\x0018Ì!:\x0011Ö­+
Xc],zù\¾²)¼ÿÒ¥×æ#+«B\x0005|µ­è6\x00166÷-P)wàÓ2ûU+qÈýÊò
ã\x001fôA\x001c\x0004WVë\x000b.\x0007:\x0008ß\x000b?}ÆöÀÍ¢¶_N^mîn\x001f÷~¬Õ|q³%ç¬1ù>9©B{½y{òjsóîüìú\x0018,d;¬äpb| 4\x0015®Ù&V.FR%êR~ú2\x001c hÿ[ðj).t;ÉÙNÖ¼p.;Ö{¹ÈD¦h¼ÅÍQDËo\x0018V.ßI¶$²íDcF\x000eæ=ïlS§²÷ðøÇ7ó\x00102â\x0002\x0003g¸Þ\x0012LÌB¤¬àÓù\x0017\x001dLµ\x0015:3\x001bIMÊp¦	$^\x0015:éòán/\x0016e¤±Ë1\x001aOw'«E\x0019­'Ë«ó\x00030Ó°\x0014£!aèÉÞ¬##ÞyNg,îg\x0018%vÏØ0ìdÒf¥PG#Î\x001di`GªÚÆ©Ø\x0004dÝî>\x000c¤D}W{¡\x0004§Ý¿¹}º{ÂRÇ<ìíÿÊv\x001cåL\x0018~÷ÖFåèÞ½;Õ\x0000×ÿqµ¯õKÆ%ìÀÂ;c\x000eÓçÆ¸ªÒwRéJwPÅ»b\x0016t¹ÆNS¡ø»Jx?=mÊ^\x0007ªc¯?A³ó	.ä\x001a» CÚæN\x0004¨\x0006ªcÏ?a²¯h\x001aVß\x000cT_ÞB\x0007@éôb'!í(ÇÅ¸Z@µto\x0013ÏÛ¡Ð¾ÒôÜõsLÿO14\x001dâÛ\x000f¿<G²·\x000fÏ÷w
SNCvò^\x000fB;6q®LXM£!þ¸yùo7\x0011òíÕÍÅÞ¦a¶©:·MíÃ³\9¡±ì\x0005c»=¶Àe\x0011í\x0012<Uâ©^¼ xóãÄrºäD¥AÂ
­×áé\x0012OwâyÝóxßJlÒ²\x0015\x0014v%)ÙL/\x001b\x0000ßoâ-#: ¥Îx\x000bWVLËbD=àäåÃý\x000foï÷\x0017ËE?8{\x00100&ñ9~\x0011µ®Ôå	}/¯.¿»º8»Ü\x001féÖÄ\x0008[O:<æ¥Ê.©Ì÷jÀbö\x0001Í\x0004³
MhªOjÎå[à\x0007Aä\C[®h?.ÉtÐ´ÎMä§\x001eðügÜ*2S>ùÑ\x0017ù\x0007D>\x0006¶Ì.îG³%í\x0014\x001a§P(ìÊJ\x0000\x0002ûÆ¯îýh®DsR\x000bYï¦ÎKIïæ[)=´~4_¢ù>©Ù|Õ×b­"\x00101e=J?W(¹BÈÆª(©¼R²©2eÛ°n´|YKÚVt±\x0005Á­:V)5Ar^\x0001·FdP[>3à!Ç¦1Ãe¦-ÇHô*UV\x0000ºÌÆ²ÌÁç\x000e&¿ÿ{~tUbÝZV6\x0000úÀ`HÕº\x001c|¡³Ê®Ñ\x001aPéZèS¶^»Ìf\x0004gÁÏf\x001dÜ\x001ae\x000bF>íìÙ®«ìã`\x0017öÔ\x001a\x001b\x0005ê>ÝáÇX9Î&#C5Ùç5>¬Î¨ì<£A¦±\x000fh¥,åõ\x0006/0¦*Áíg«Îì;\x000b
\x0001KÌò	56¬Ùi²:\x0005²ï\x0014\x0004ôh\x0003Y(Õ<»i¦,ÞéG«\x000eì;\x0004Áä\x0010VÑô£1XV\x0001Ùw\x0006\x000eÙ®KÇçS±#\x001fV ©ê\x0008¨®# ãV[J:®B/r­Ð]ZÃV_	º\x001eú¿pêfrÓâ?£8-R/\x0012\x001aLÓèhJUæzó\x0018	¶{ËtÓ>M-Â¢Âpª´¨A\¼ÀÏ9\x001d8µáíf_¥nÆ%ìÁÊµcZÉÑ\x000eA-,qÛÖ8%Ôô>\O3D7ïßß¼BÌûÛOûßûË\x0015A:M*J7<®Á1U;4açäâdóâÅÙÉ+Ä½<{u½?TMoÇÅøNPO«\x0001\x0012#p²\x0008¶\x0000[
©JHµ\x000c2Ü*[òà-9eå_.\x0004Õ%¨^,M¾nA\x001e' òuË¸²	ùRPSE ^/Èâ 4çº²÷æRP[Úe\x0012Þ,QÉ¹V¦ªü^
êJP·P¢Ù¶(Ëm$Q¢9IVþ\x0006É ~¡jÊÙ*y\x0011I5ñ=R+÷\x001b,}(AÃB\x0016'\x0014îÑ\x001c0Ör=dq\x0015Wt\x0015_ N\x0003eÒ,kz§8¹HT>ÅBÒÚ$-³IÅsH #òº+g×$¨L\x0012,´I\x001eNvhÔ¢µ=gÐß@7A¥ía¡º\x001f£kÒQ|;\x0018ZÙ-Ç\x000cS_$¾HRw@gæ×\x000c!\x0015¿\x0005I\x001a|Z¥ÉtÇ`d	#\x001ba04D!\x0018íóùPl,
,Q%j\x0011&Ãä7\x0001¼WS¿\x001e6\x0016S²6\x0016\x001bòíR\x0004ÅèÎò{p5pç8Ìûhkêg×ø\x0007üìúýÝíó¯'ïî¾<ì¿\x00183L%6}ÄÖkSZUÀtâÍ÷çg7ÿ~òîüíÕÞ\x000bHf%ìb" I¦ÊfªM
ÒG¤J"ÕA4ôê¦+\x0012]ã?Ä­Ì°%ãr*]Ré\x000e*ÌR£\x000eF8Ü ¥á]¼nLHõ`\x0012Ët`yÛªu¼\x001eGx&,iõr,[bÙ\x001ei\x0005ö$\x0004Rü$\x0015½êuèK,ß³µ\x000c«'	&­ \x0013[}Öùa]HcØ \x0013D\x000fSÈ\x0015Ë \x001cÍ	\x0000gyZDÕ4¦\x0017«R\x000bÐ£\x0017¼Î\x001dÔ#M\x001bçý(\x0017zúááÏ\x000fþË_À¦z\x0002Û+á_/"ÍÉ·wCïwwïn\x0007@\x0012B¨G\x000cU|\x0013¿ë°øgèj\x0016o|ñÚ7n\x0007ì\x001e\x0016q­Õc_×\x0018¸D'ß\x000fy¾ßÇ¿Ûã\x000e¨\x001f\x001eß_n\x001fH»SÖPI}òæùnèe;\x000fd½\x0012i£\x001cæÐH§IµÖ\x0006ÅÝÄ\x0012ÐY*¦>yss¾§­úáþAÞÞÝVç¼¬íãýRÁ/C\x000f[ÀHøé0¿,ZJHCÎ£Ô4_ßâÍæz>J£~ø»ûôãö¯(®o¿Ü}¼½ÿÊ^>üüþö@T§Ã\x0010È!Û~\x0018/;\x0011;f\x0011L)ë³·çß]¾LõO/¯^¿ØÓf´"Ké%3ém/a&2ôI\x0012QëÉR'æN2§ÓHfÙ¼Èq9IfÜ^q\x0005Y\x0016ÐIãd\x001dÉLáÞDfÒ,k$c5°,õîJwH¦ü©s,³4>e¼,
\x0018è'st\x0002\x000c¶®Ëd|\x001c\x001dçb­ K\x0007zÉBê<\x0013É¢;Ã`*ðbz\x000b«ÁÒPN°è\x0018[âr§w\x0002M`A¬\x0007Kó«zu;5&9tã\x0019ZKÆ\x0014úÐt¼¹ó6úÃ:\x0013!d4·za$\x0004ºm\x0000Î\x0018Õ´Ï\<Ð<E\x0007}­\x0015h4ý¡\x0013Mé4\x0013	ð
=ú\x0012có\x0004Â¬_Ðø_n+\x0010}õ4¥\x0005ÑÌ)ðZ¡\x0018Í­¶O<±¢\x0013ÍÀ©t£âà\x0005\x001dj#æàý
´¸% Û\x000ehL°\x0006Ò¶áT²ÐÍ×ë·\x001aÍÙèÝj"\x000bÍØS`¡9í\x0019
Ö\x001fÐh\x0004 Û\x0010`\x0013\ «=FIhC?çd¢~S@³AzÑ\\x001aÕv=^\x0014£å\x0005Íó¢V Ås\x0004ÝÆ\x0000\x000f¨&4lß\x0000Yj¬q
¬> <Ð¤w¯ì§A8uù\x0014°k«ýz²h\x0007ä\x0002[`Ð6%2{*ùbÃwömWo5\x000cäÉ~[<>£	F\x000b"£é.ä\x000fâ/\x0007V¦à÷Íý»ÛûÄ¶}zÚÞ?Å?ûñ~ÿÝÎ¢k*`g¼áÊ\x000b\x0006ã'é	¢b¼ItËçgróîÝæò]ü³ïæË\*\ºY-Æ,ÎHô?ROëk!Ôú<ië·Á¥ëÖré*>Ò\x0018<W¤«<ßßü-qé\x000e¶\x001c7Ú´c\x0001;/Ñf\x0018fé
¸ÒÁjÜ¨ÐÊ8wú\x0003ÜÃÏÿù_·Ç·«àí\x001aN5ÉÓ\x001bÞ­PÊssqqvÖ¢J\x0014Õ¢ØþâÚ:>9\x001c,kk°èE·²SÅ\x000bçNü#\8\x0008yát\x001f./¨IûÅK$ÇID\x001f­\x0019Ø\x001c5\x0012jé¨æËh²D}h>+¡e\x0017ÅC\x00040¾Aïn£\x0006´ª\x001e'ýÁDjçwûÁÎ¤8H#Ø£¹À\x0012\x001c\x0018ÌKìüzÏ\x0000ð\x0002JP²\x0007ÊÈS.øcH!ÈÔ/ Ê
\\x0017P©JuÊ§fè¸½Ô©%*Ç¦ÕJX\x000c¥K(Ý)*r.e¼ý9 Qéì&©ÝcØJeJ*ÓE%Ð/J~¥K£CPT9*£võT+-¡l\x0017T¼"sÄ­8QT*/ Y¾×}Iå»¨\.ã3!@·U\x0015l2jªKÕD+\l\x001f\x0011c?\x0018Þ9´æuzÀ{\x001fÝÜ5Ì\x001fÁÍÍ5þá16Y²ÉN6ÌãË\x0001N±JFYá´D\x0007n^¶Ò©NõJN*Vö::¸ÃÛEt\x001d8X
\x000eæw+.át/ó92ï\x001c¹3\x0012Sæ\x0013²ó \x0015Îpæ+-ál·äô©§MagO¢ãà\x0007ÖÀ¬¢s%ûÊDçK8¿@t|eöåf²Ü\x0016¢QûÞÂù	¤æn¹uïë§§ý¯¯VcFÍðø#¥´\x001c¯Pt·cAU&¥½{·ïíUÔ½£Lv
{#Ò§Ú\x0010\x001a¹×\x0016ôÜ9m ºÙvêf\x000f¶\x000f½ DßZ©DæmgÉ!í``3óë9´Û>°S/ÛN½ì£d N}\x0002³òÔ\x0002	ÉË©æ[\x001b*ÉT\x0017ä\x000cÚx$£Çf)<)
=mÄS Ã
4]¢é>´ NUÚhÑmÌ\x000fBr(Ø\x0018Ðrâl\x001f\x001a¸ÉNÃ\x001a¾ö·Ûû1oòìËûû\x0003ù\x0011ÃK\x0010ÝPâòÚd°pt\x0014Ý3½©´î÷g7yööíÕå\x0006ï\x0005 ,\x0001e7 \x0016ó%d$Ï\x000b¾AA\x0015q[À§J>µH2éÞè÷b®I\x0012`~ï\x0016Â¬\x0003Ô% î\x0007ÄaE\x0004\x00187 3	\x0010¼ËÞ\x00124% Y\x0000¨Ò¸\x0015\aÏ\x001f0ß¯£+· -\x0001m? ¶Ô è\x0008¨]\x0006@\x0013\x0007&Æ¿\x001fÐ®\x001f\x00103-èBo£|Â\x0019Þuo\x0001 /\x0001ý\x0002	SÇ¨À\x0018ÛôbÜ:¾Pò\x0005\x0002Ô©ãgÓ8K\x0002tc
Ò:\x0001Rº\x001f«i±@Í\x0000g¯h0\x0014I{31À® Ôvd!Áh8éé@Õ6Ø]ÇæW¸:ÔÕOX\x0019\x0012è·$CnË"\x000c´\x000bE¾sÛ:ìÕOX\x0012X`K4u*§T8Í¬	[§h ²%°Àè§c¡SË2\x0004ÎÓðbå>¬	,°&ñ(³²V\x001eëëÓQÎà°R×@eM`92¤èÆú\x000b>)\x0013JY¹Ê9\x0005öDË\x001cÄ°
Så\x0006\x0019\x0006¶ÈÑ]g¡Ò×°Da[òªñÆ{*=­2'°RëVYVúP.Ðqó¥£¬ágMá=ëkc×y]²R6r²Q.«Ã(Mòüg
Î¬$¬²\pArV\x0018&y(Ú\x0001Zª¯\x0006p

m¥\x0011ð/\x001f?m?î¿Öy'è1LYçN%¥qK¾JÀ\x001d§À¿¸¹~µ¹ùö\x0018*ÑT\x0017Z\x0010¼Aå¢Ã\x000f)¹[ÛÎW^ºehv*5[HíåOÛÿzòÝöñÃOð\KI&DE3,'x\x001bÑì¬*DJx/ÿ°yýæä»Íuüá8¢.\x0011u/¢\x0017É=H¾<¤¡#Év8¬E´%¢í¢	ùµLÅENBôõ\x001f¨5n$ôr²Î^§ã¹c©ÛRZjÍ\x0017'?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=íU¶0I<­e\x0016|3©H\x000bK}í¢¥"\x0007-Å\x001aë÷ïwU\x0012¬¿\x00190WÏ-Ì</p><p>SìâzpÞ</p><p>ÅÍ 'OÁ\x001a)â\x0011TY¢Ê1³J<</p><p>3Èfã\x001a\x0010º½nd[GPUªFPµ×Ø>î<LÃ\x0010§,\x000erß\x0010=\x0019aÕ%«\x001e2«¤AòÁ®:'EîÍ\x0016ºQH<ÂjJV3dWÇñùÅÓd¾\x000e)\x0012\x000fà¶qA\x001eAµ%ª\x001d2+74=\x000bZOqô)rí¢QD6êJT7dUm°ÌÝy\x0008</p><p>\x0018Ì´ ©T\6^µ\x0006XºGÌ±\x000fÀ\x0006ÂtûqÁí2\x00037T2y#_=ÂZùV>ä\5g\x0018\x0008þ\x0001\\x00034x«üyµòX|ÌeA¯>î,F¥<\ÎhkÆÉ`µò\x0002|Ì
((á<ÀÑÕ$ÁÃ]C(h\x0004¶Ú\|lw¸¥R,09G¦s2½5¬aÈ½V5\x001aÑÅÂ\x000fF¢ÀdºóðLH^ÖÑ;¬à¬^\x000f2_WâI1êÃí×8¢\x0010ô]?ßî-ØôÊ:ê\x0017\x0006q|¾@²¡7ðáômK\x0008ê®¯Ow\x0015lòõî\x0002º\x000bº1S\x001e!?l#§\x0015ôÈ\x0016+LçsÊS\x000epz\x0006§Õ\x0018³\x0014ËÀ\x0008Ò\x0010\x0012¦!4×Ï©KNÝÏ©Aô$¥ìBLÉïS\x0006:\x0012g£Cv:&\x000c©o\x0002p\x001e(ÊÃFú°Þ»I?\\x001dV>;5¡.-Û,\x0011 â°>\x001cGMï½´Ò´Òá\x001aK\x0005åp( 6Fíéeõöáç}¸®Âuc¸!¨2\x001a×£r3­6<[·!+ÔËÝzÍ¶Û¸\x0015¾z|ØO+õx÷v,\x000b§ÊÆ1Üï\x0012
¸¯./&Ñvýè2{£ðiÇ1gQá]ÊBZÖh·í¤]ï5ä²´íóâÍÃó=Î8þ°|þs\x001f³e¤­\x0015M\x0005.«øXßPù'âëÅëstüáøúîç\x0016%·Åm¡0:eô5g\x0000</p><p>ÚqY\x0018 %¹A\x001eN\x00088\x000c®f"\x0008¦¼L+;[Üz\x000e··Twh@y\x0010W·!­o×\x001aý3\x0003Üàv\x0016¸LSa õÃÁM\x0008-U\x0007]ä¾$÷³JîYQjµT,r9×x\x0018\x001c\x00007ëÍU&5W­jÁ	^Þ>=<?ÆcÇÓ\x0006\x0008KSg¨</p><p>nEP÷ :\x0010{vt\x0007GWxyúþâú2\x001e@ö\Ì!·jÙ\x0015N\x0001QjOFz;ö^v²ö/·µ½oç\x0018\å¡ïÒÑV08UÙjËvµw\x001bÿò±ÿ8\x0003^+¸è£Í]®^;7£æ,ô\x001aýf\x001e:¶*I\x0003.3û®Úü\x0001ö¿ÕìÃG*3®qb</p><p>²7Ê©f±ªÙ?Íc×¶Å.\x000e</p><p>#L}py\x0011~\x0010'~Ü.N\x001e¾=ÝÝ/.\x001f¾Ý>í»~	O­òÐ\x0012»"Å[B\x0008®
	põ:¹¸zv¾¸¼¸:}¿RªÒI¬D	÷AK¢Üyô"²!{ÒMiJJÓOi9fß!\x000b)=\x0018ï\x001aùÌnJWRº~JÅ¤D[²Àð4¥\x0003\x001a&Ç¿8¬Èõ\x000b·¨.Yß\x0016'_~û¶x÷ðøñóòîëþIo\x000c³nI¦(ýna\bj\x0014­Á?ùúrµ8y}üæÝÕâÝÅeøÓÙÛóéÄÚu üQÌ¡"\x001f*úÜâ¸(!¾1Mq\x0016½,éå<zP0CÓ\x001b:/Á\x001dÆ\x0013|#4\x000b^ðzÞÂ1*õªÛ(³K\x00037­ÈSVMcö.úmB;bí|\x001d~Î5juÂ\x000cNI@Ö0gpîzuìF·¿ü£·?ýcá±K4Ð\x000bg\x001eZÅb´ïÛ±»éu.ë¦J\x000fü\x00138t¶,\x0013Zb3µ8¥ÃA»æA­ÿWmý¿f­\x001d`Ö á­&ïX®\x001bÅ7\x0003è|=±ÊmîÍ|^/ÿx¸{Ür</p><p>õ\x0011Cd4YP XÒhj[Y÷u8)}¸8»Üuëµë©\x001d1§\x0012:(OHåI9No"\x000cõ-uÜÓ	eI({mè
%÷x\x0008í\x0006ò9P</p><p>\x0017ÃÖÄë>@U\x0002ª^\x0013¨d\x001aMÈ£\x001ef2¡ÄQ 0ÅdKUîtB]\x0012ê>B\x0001âÃVâ2Ô¨Á\x0014LÈ¤e¸MÒf:¡)	MïG\x000e×*</p><p>¤\x0010$Á\x0008\x001bµ¶$´½6t>µUh±iG:&\x0015\x0001j¿¥º}: +\x0001]¯	Í¾\x0006</p><p>?é#Ó{H¸\x00107"j\x001faQ\x0014\x0001Þõ"ZF\x0016DBE;ÙYy8ÂÊ\x001bò^wX:ìÈ99l\x0000;\x0011khÈ\n8a/¤xÈ
\x0019ÓçÛ*;öt1\x001e:îêÞ\x000fÎè+<XØ2\x001f6ØgÍÝÑ¹PBMË^¿\x0013ËÈïxz9âJe¿3ÐÖ&´&\x00140ÖË+´¡Â&àxD>BèÆôÃ>ÂeMØgÃHh\x0010Ð£@5\x0000:ÚÕ­</p><p>Ò	7Á1TG°\x0017á\x0007õÛåÃÝ\x001e:Æµ£&\x001fÁ4äâ»«\x0015Yí¶¥çµÊå_^mOY\x0010¡(	E/¡4V¨(@ÞÝÃ*DBÛX²$½ÐH=¶\x001c\x001e£
YVGo©\x001dt\x0012ªPuÛ0`át.Ã²ú-Ló¥üFçN'¡.	u/!¤øh~XUWxÒ5VçÿNÀÕÛ\x0000n}Á§d+ÊøG¬Qp´WZc3»!ojÈÞOíIGpM\x0002}ÌXêãT6ÃnÆeÍ¸ìu:ÚÞDð?|NÖìobÈh$¯½bøA5Åû*Ü¡\x0016¯n\x001f\x001e½Ý§q$Âù\x00155 BÌÃ/.-\x000c;¢¦X»c@íU¸@¿_¼:½¸|uº=õE,Æi4,ÒÑ\x000fÈ:?¨]³]§!G­ðµë¿)êª\x0017¯_náÿìU¿\x000e'²|?\x0004\x001d\x001eIúgLQ\x0004o]\x000fSáÏõâõñÓãðv©ý\x0013¬(aÅ\x0018,ø6å ·Ip@ä\x000fÐfk\x0011X\x001f­,iå\x0018-¨ôaá\x000f`âGZ`åæÒ\x001a¹&	åpµÈø»ç»§}I«¨+Jíç^°Ìc<Ýç¼ô»ë³÷;Ö+aÊ\x0012SöcÂ \x0007Â\x000c+MU2\x0004'S~×Kü^Ng[{>ñkÏ'áð¹\x000f3ökãâ|UUM\x0015\x001aNí*T¾\x0002Qù	¢\x0014ýFÁsH\x0014+Qp\x001cÆ,±fjgu\x001a¥*)Õ\x0000¥!AyéMî©1\x000ce\x001c\x00149Ì§4%¥é§\x0004Å5|#ËÒ</p><p></p><p>ýñ©£9ow2¥^¦Ó\´\x0017\x000fÏ÷·,\x001f?áKùÛýÌá/ä±\x0014ù}nO²1[ãÅÅõùéãËñüíÅ¶\x0012\x0016½>L§AdÝÊ{PaD-K!\x0011yM­ÍÒ6B\x000bu«U\x0005[+o</p><p>?ÃKZþ¤\x0018EÊûï
ûQD\x001c\x000b¾!Ç\x0018êM--\x0001ðKÇ¯\x001c£HIÿ]ëeI,ÿO V%±\x001a%6èVA2C£U"Ö¤!©X£©M¼%é ÖÏX×~
ùéi¯SÐ\x000c:>p¾D8¬ .5ÎÓ[P«Ù½Tè|
Ëùýû\x000eL¬?\x000b±./=¸\x0001\x000e\x001fË-·I#»ÊgºeI,G<Âq#áª ò\x0013³Ì£QäsK\x001f°*Õ\x0018°þk|ÙsÅñeÙsAÄ{ôÆWÀ»°.iõ°y\x0005UOp)óØÂ¾¦¡*:h_[\x0012Û\x0019Ä\x001a¾%¹\x0008\x0000æ\x0004Ü¨µ\x001f\x0004ö%°\x001f\x0005V\x0016D0&-YK'\x0007ó}°-Wd{ã¦»\x0019\ÄÒ¦¹\x000eirN*VÖù\`°srNÇ*Eö7\x0012/GYÊ¤Û8ÞÝÓ\"ês</p><p>\x0017ËÆ»|\x000f±Pk:ÿÐXèºüçÿ:ýõþîÛþQ\x0014VBMw¬a´ZqÂI\x0012\x0008¾Qü@\x0002
ÓWçgW»\x000e=jM9?6O`\x001aAsÝUX\x000eXé\x0010Îu
¯Ãð\x000eµá`uvýçÛ?n\x001f¿í}\x0001Vw</p><p>\x0003-\x000b1\x0019$¨w\x0018ocáü°«EáçÓ\x000f§W»^¤nVuÖ+ü f½n\x0017o\x0002ÐâÝÝÓÃÝ¾óÝãx#3¤\x0001'M8ë /\x0000S·j\x0003ß\x001f,Þ½¿8ÛæruÐðÈ¸\|¸»½®Á·_ö7_yGuÊiÒ\x001dgXÚ\x001c~Ü\x0018ä\x0006ýag§gÐ4øòôòÍÎïÎ×¿;¯\x0007ºÜ/î~ýú×Þä¹\x0001Ï\x001a¯)\x001d=ØÖÁ`5äüøýÙ«·ÿë§ËOËoO·ù\x000fë¢ä\x0014\x00030Â¢"æ¹
EsÒ\x0016·9¤áBZ?\x001f¬©ò¾Z>î½úXúí×<"U!»Ú·\x0015â¤\x0006¶ãËÓíj½ëV	¶V9ùz\x0019\x0016èþ\x001b\x000fã
Á(PhN7ÕÄR½3Yðú8,Ñ«í z]ÙF'eú\x001b|èÅþ\x00199Q\x0012_Ò¸a½Ò-9Õ¸ÍÔ7ÜÅ\x0005ÉÙ+KÜ¼ÁdÜÜ¼\x0013\x0007Ö¦¸\Ilä8xuÉ»?ÌËAÞÈàXGIâR¯$º7\x0003é\x0010¯-yí(/jÒS° »\x000cgj¥ÆÜ</p><p>îâ5v½¡Ë²¢jðêi	\x00133o¿þû¿¡oøþßÿ½_%\x0004\x0003¼3Ð×$&Fíãf{éÖÕûc\x0018 yúö\x0014ÏO'\x0012\Ì\x0001wá@:X0çØf\x0011^i|Û¼!rYËYäá\x000cã\x001d¶ìÛ,Â==È\x000bÝ\x001aU6L®Jr5Ïæ\x001cZrÈæNÍém4Øü«Eäz\x0016¹`(\x000cé<TÚÐ¢¥ñp\x0002êI\x000eGnJr3Ïæ\x0004\x0017ã:'rÃüÿ\x0016ÛÜÎ"ç\x000ee7ùÊ\x0016lN\x0003Ò\x0005ß^Z;@îJr7ÏæòÈÍiæ«ÑmîKr?Ë;¥4.èà©5¹s.qµ\x0004Ï¾µà¬×hV$rFSc«\x0011-\x001a},3ÛfM\x000e¡W¡ÏE0¾>½jCµvÖd´Xå\x001e¬Þ\x0018ðÜ~cøÚ-Õpº¥^>|ü|û\x0018«êöHêpBÍ¶Ö0å\x0019**rjýÆ%0`^Ãöe,­\x0003\x0005É½¤¢$\x0015#¤Lá#G$Å\x0001¤ÊQõkMº\x000eÊYs{á\x0007ÑíÑ5ðåò~¹7\x0002%96=sÂ\x0000\x001cORÉÌ®\x001eà}k<\x000bÝ\x0002_\x001e\x001fC:%¥¦â¿¯\x0013úÐ\x0010æyMp;Kxyìhå¤öÓÝHS×/¼\x0008?¨Ê¢ÊÊòc$ý9üpß^0\x001c;·Lî}</p><p>#ïÅÂ4ârýMÔZ9>Ø?\x001fîb\x0016%³ÃìQ\x0011^1x¾Y\x0005TjóSfÓ¼Óù/ÏÏü7ñ\x000f¤¬eOÚ\x0004Çúp÷%à\x00011*ÜGb6Ê\x001b\x0011\x001cj\x0005"M \x0001?x)! é3H?ýSzí½Âùýý¿Ld\x0000Y
ø×ùrñ&8ËûÛ»¯Û1u\x001e\x0001C;\x0011üd<\x0006@¿,<A\x0004\x000cÐÿt\x0005ÆñâMpç§g[/Bü?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-XpGoF3jE56DtOiGBKmjkeWaOt0g`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-J1Yd6/jpwelkrPsLlIKIwroZliE`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-c9/VSvXq3KonrE0PGb9HMJKKVgc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8110-MkCxZ1shfPKaMBKxYixStFsaM2s`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-X5/EdWTTKe6h2QpXydGYJhujF04`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `95ae-DNZn1zmd/mgwA2O0M/AAIcjyuds`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-W/3cpjNgKgrG2biFP3WgiwgJxhA`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-0B5eCV5UQkkbz373bYlkYrQmS5k`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-XpGoF3jE56DtOiGBKmjkeWaOt0g`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-Q6JVcsyZiY6o9ii2tVMkLQ2XCFI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��y�zF�]�\x0013����\x0004����:� </p>
  
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

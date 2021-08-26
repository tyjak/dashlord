
# ZAP Scanning Report

Generated on Thu, 26 Aug 2021 11:47:06


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=r9ÏÑ|oþõâÓÑ\x000b\x0011\x00043\x001e`3~~}uÿeáô ïP]´RãuÆrç\x000fË`y\x0019úùñÑÙás2*áT\x0007ß`û 7¤8\x0016ªnh Ó%î¢¦lMtÆS9r;7Ï.6À\x0012ÎôÀ¡²,{dÉÃ6Tàêè!\7-él\x0017\x001dä!\x0010Vqå
2ÓÍã\x0006:_Òù.:ËU´ñ\x001a{\x001dòTw¹m \x000b%]è¡SùaÃÆû²%¹X`}ý¹|Êr¶ÝÀÖÉ.8É\x000fDÆ»¬Ã'Y¯>èV¸\x0018Bùå3º»ëëô\x001aúYÆÁ#dµÈ\x0003RlØ¥]k´Óã÷:\x0019dÐC¶&\x0004\"Y\x0016UTóÓ°Mlº-FT
\x001f¿"KGYÏ÷u\x0011E/-Ùl\x000fÌÉ-°»)¯¬I=\x0015þt²¹Íu°Åp\x000bv	`Ely«Ðóg²ål¾dó=lp@*eÊæyÛ\x001d0óÎäÅh»´ª+,H\x0013°4\x0000Wë<IÂ\x001a.é\x0016vÞâÝ°leÝDZ:®èý²Ñ¤ýµ\x001b
é?­RM²&	üV\x000c#ú>D\x000bftthT0c-äM8/\x001dÑ«Y\x00125\x0017ÈS|¸|º¿þrµ9»ü÷Dó'SØ\ÀóuYúÍä*\x0005fæg?l/Î\x000f6gÛ\x001fâ/¯BB		\x001aui\x0012\x0007J4¦z\x0000\x001cåâh¤T%¥ê¦Ì½Öéô\x0018fp>\x0007Cú!F]2ê^F/wÃå\x0015Ý8
xM~îJ\x001a!M	iz!ÏAPj:B\x001a\x0016\x0018_,\x001b!m	i{!æa@6xA2Áä»{?95RºÒuSJò3NhªrÜ ¨öæ6Bú\x0012ÒwB\x001aá²
SYöDéØ+)Æ2¡ÒpMñnB»ÒeÕ#9´ÓF¹\x000b*&{.z1Õ$Ç\x0015x,ÉÏ\x001b9\x001a\x0011kÓësL°\x0015S*Ê\x001c¯ÅJÍÓ£Ó½^Ç¨B<\x000c¸\x0005LHÍ£çUçj\x00069dÓê_.¯7?ýÏý÷éý¯®\x0017Az\x0015\x000eR\x0016cmÖWÐ\\x0006ä*	¹Ø\x001eoÞnNÏ¾?º8^À§J>ÕÇ\x0017#]¾ÆGwÚ­I¢p\x0011÷«é'Ô%¡î_ÁôÓ<TWyá\i{ZùLÉg:ùbÄC_Ø*zK°ÚÒVáåÈ\x0002ú\x0012Ðw\x0002\x001aÅæ\x001bI\x001aâ </a%oÜHX¨«ÉtÕêB´\x000e¹Ò"Æ\x0000tÕèx\x0011ú¿±¬N±ì=ÆÀæÄ\x0017#\x001eÊ\x0000ë`ù(3°Õ)Ç\x0004\x000f2URÉàØ\x001aÆLÆ^\x0013ÜZ\x0011mh{\x0011ã"²­Éz(8P\x0011m?auRdçQ	"«\x0011b7½eAJV®±c\x0011¥]\x0008¥Î\x0017Â7W÷¿\_m¶7?Þ_}ùeYv\x0013jÒ¬tK7u\x0016Èr0×Í|stvþþøh³=ysvtøþ4'³BÉ
#¬¶edÍ%\x001aòH½±»í¬ªdU\x0003¬(^NÝcX\x0007MFhFß\x0010ÛQuª\x0007P\x0005Ok°\x0012o7\x0014WpeÛ+ìlG5%ª\x0019B¥%u<\x001bD<ûLÍ%ÿÛAm	jG>¿ÌÄP¾¿àbT§æ¹ Å¬ñòQ_\x001añ\x0007¼4òõVA\x001e+rx~½Ìâ*¦}Ä\x0013Ö_ë'Ê¡$\x000c}è"S\x0013\x001dJP\x0007\x0017h\x0006´eb·\x00150+\x0003Liè!Ô9e\x001fP\x000c mKovµkeërDáêçðø\x0003\x001búïï/ãÿ÷õÃæ»ÇËëEzQ\x0001Õ\x0005-½cám'\x0015 X~Y\x0017ÆEúþlûñðôøóæÓóíñ\x000bQ\x0019\x0016JX\x0018á9Ï;MUÓ\x0013,¿VyÊ¼U¬jha=+ù\x001a`\x001drg=|u\x001a|\x0007­.iõ\x0008­Ô6\x0012­çú\x0019Ë\x001a\x0012æ=d\x001d°¶µCK\x001bO?íY¬n]\x001e$\x0004ÂôÒ
p³ð$þ°+°}Ø\x001cþru{õï×ÿß÷W\x000f_Uî»O÷?ßþåwgW\x000f\x000fw·ßùè@ç×¨=åe´\x0004IOíb_æáèóæðýÑÇ£\x001fPíóëÀª\x0004VãÀ\x0015A´QË´È\x0011\x001b}\x0005¾¸\x000c\x0012Ø¬@l\x000ehI×\x0013\x0004æj$¥ç=ÍÀ®\x0004v+\x0000+|Gâ\x0018\x0004¤C\x0017Æ	Ø×¤j%ö%±_a\x0017[ºEk\x001b­À»Ç\x0004íçíZég®\x0010Ï\x001a@ÖÆhTz5.!k"Öb\x001e\x001e6\x0013ËX®°-$½\x0018jç>\x000e¸-¸C2ÏQäÊ¸Éqë5ÜI\x0003\[EÓn4^iÞÉûRÕmÈP­2¬±ÊÿèÃ\x0017B\x001cÂ*&9Ðé\x0013")\x0015££­\x000cfO7e!1¾LÎª,cµë{ùáêþ§§Û%®9¸@ob8\x000c\x001er¦7	:nþ\x0019ùÑ\x001fÎÞ^||Ntº\x000eBöiÔ	\x0011$/
\x0003h¦D3­h8¶Æq"¢Ñ}ÁGÓ*¿\x001a\x001f,³%í\x000bÊS£
åþ?/5Å²BÏgÎ.ªÚrª\x000e&E\x0018mO©]¯¼eÛcçvËÒ\x0015E ´|úñrF¯çiçé@\x0015\¨2AI½\x0017².\x0014³¡eø\x0003ÚO×W÷÷\x0018__=Ü^.ªæ4w¼{~ìèÖe½\x0019â§hUÎ0¸>úüqûB
7sªSus¢f\x000bi\x001d`\x0000c\x000f,Íáç\x001a­¦ä4ÝÆrùB!ñt³\x000e6ëGìér,ä\x0014rVa?ð£öëË§\x0016½o\x0006-,·{Æ\x001bUx9¥Cì\x0006ÚãíÅÛÞ6å¼BN\x0016\x0015rMxØkLÏ¯Bú,Wå
òróqÄ
x²Â]x^lâ¿
ÃDG%IqñæiçåpPÁA\x0017\x001c\x0007ÓÚé~\x0015Aì<D\x0003ªðT\x000f\x001e\x0016\x0011àDtT$°Ê°NWtºÎå£\x0010FºÝÂén4S¡.´Å£Xi9\x0010W®\x001fÏVx¶\x000b/ËA\x0008é0\x0001ðvG\x0016ú¬«ð\\x000f^²&çyõ@æÕn<_áù.<ÇÊd\x0002+\x0011Èà\x0019êÒÄÕ¿\x000f,Ç«¼ìq\x0017Êår\x0018\=å\x0008ÏäS;Ï°,ÇÊ]@»p¹×\x0006WOÓÁÅÁC¼zÝ\x001f\x0017*w\x0001]îÂ	N±
¬Éâ;gÛýq¡r\x0018Ðå0, 4XøMùê\x0018ã³;sóð¯\x0001¯r\x0018Ðå0PÇZæÕK
W\x000e§ÇäÕ?ó-Ç«<\x0006ty\x000c+vfÙP\x0011µwKWoþ\º\x001c¯ò\x001aÐå5,ð6\=j[9kç]¦
tÓ.§aL¶ÊjNpYÉº½båtÏ.a\þ´qí\x0004[%³ÏO\x000elÀ«|\x0006tù\x000c\x0003»@O¾Q\=­òêu\x0007zPù\x000cèò\x0019\x0011/ð¹uØ©Ix.¯^÷¹UÏP]>C\x0019¬>M«\x0007TèP\x0015ñæÃ¿\x001að*¡º|öùãÆÕ\x0003rirwA\x001bX½Êg¨.\x0015Æ!¯\x001eÉlçÚ\x000c
pÇP]\x001eC\x0001çÇ+=¿\x0012`óýLu\x0003ªò\x0018ªËceu<\;Ö¶ñ>ãÍç`5àU\x001eCuy\x000cØõöãk\x001a¯È;¯ÿÛV\x001eCuy\x000c\x0000\x0016\x0006Â»·%é"\x000fnÞzÑW¹\x000cÕå2 Oñ\x0015ú"Ýîv\x000býF¥ò\x0018ªËcÄWyñXë(ÄÔ»ÙWy\x000cÕå1P\x0007ÃæÅãQ\x0014Üì*¦Ö¹N<]y\x000cÝå1¤Ê93Éª;É'\½n³¢+¡»<F\x0001Î«ÇfÅí\x001cÚ¼m¾\x0001¯ò\x0018ºËcÄ{cÎ\x000f°P­\x0013VC^½nºÊeè.!²â@ÜÊyUÙ¬Ì{\x001bð*¡»\Ð,\x0016\x0007äoÍîdÌ'«6àU.Cw¹\x000c<­»Õ£¨09åheÿÉ¨|îñ\x0019\x0010\x0002\x0015_NÙ\x000bÇx2Üù³z\x0003^å3tÏ\x0010;\càÃ\x0015ÍJÿ±­\îq\x0019(Ä§óÒ<n$\x001b¹zX\x0003]å1tÇ@:ËîV°&âå/;\x001fD¿\x001cÏT\x001eÃôx\x000c\x0008Kþ§ÄO¢S!Ùþ\x0002S9\x000cÓã0â55qß	ü´KKÍ_&\x001bð*az\x001c\x0006Î[)ò>WOí2¶ýß¶ò\x0018¦Çcw\x0007w^\x001eµôæzö
tÃ0=\x000e\x0003<ìx\x0001Èo\x0019\x0003énS9\x000cÓã0ÀgÕ+\=\x001e}åùÓù\x001c\x0006ºÊ_.áìÎåáVÅÝ{Þ)ßWù\x000bÓã/À¿\x0010lU ßÌ¼`¤®r\x0018¦Ëa88Øå-ø!õ.ßØOW9\x000cÓå0°§ÉåµüiÍnñº½­­\x001cír\x0018Ö³Ü6ªÄÐKA<ÁÙæõçºmå1lÇ°ð4¶8\x0006Dvhf®cÝWy\x000cÛå1,ìÜ­åRö©\x000cj8_k+a»<å©ËÓêñ´BLÇñêu\x001f
[¹\x000cÛå2LÀØWOÐ\x0004Î`wÙîî+­\ír\x0019øÎ²Û{É\x0006\x0017¯ÿdT.Ãv¹\x000ccò\x000b$*¼Óp,\x001fü
W¹\x000cÛå2"^jÓçs_W\x0010ÙáÎçÂ6àU>Ãvù\x000cE!põhÊ\x0000NÉ«×MWù\x000cÛå3PÖÎRå
&çUÌ|àÖr:WÙd×ecè4¶	\x0010móÁètMv]6Y\x0015\x000eW±\x0006D°"?\x0015ìu.Ç«l²ë±É\x0012¿hªÎ\x000c8#ú	\x0005ë\x0017XÓÿæ*ìºl²\x0008»0^vAÈý\x0000Öö¿Ì»Ê$»\x001e½·\x001ed¼ó·fàÛV6ÙuÙäèÅò3Îß\x0001ò\x0015­¿ÐU6ÙõØdìµU´õð&¶\x000f2\x001fÜþ·\x0002WY=×cõ¤ãÇïÉ®$=pë=äX¯?ì+³ç{ÌtÜP=áQCµwÜÝÂ
Ýx]ñ]vÅòë2ããqægÄxmÞrÐW\ßur1Öó\x0019/ÕsYoËx¥Ð\x001b§¼è¹\x0008I¯¸ß\x0017sSÒðáÈù\x000bè\x000e÷\%AIkû\x001b#\x0003Áê7HIê¬!\x000b\x0008EûÜ\x001f
sÊx\x0004;)ÿañK=åT¦rï.H\x0015czµ«ø¦ñ\x0003ÒïJTûRZ1
(&]åO7_®6ïïî\x001fïnt\x001eOÙ¢De±q\x001e&fÊ\x0002ÈO'ÛÃ£ÍûÓ³óÓ\x0017Z\x0019\x0010J@è\x0006¤ÔÆG2 añg_ví6\x0013êPw\x0012Ê,Ùê KÝû¬\x0017\x001cÊ|óbÂøW¬?2Îqç\x000e¶Ý ÝÏ_~ù«ëÇ¿.Ónµ2çØ°\#¤4\x0016\x001e jáÐ{=»)»\x000fßÿ¯£ãó?¾$äÊÔPRïO)o¤\x0016Üjnºc4?\x0011FôõñÌ-Äª$VÄØñÆca¥ÎZ	YÄ\x000e\x001b\x001eW¡Ö%õþ@õÆuF;J\x0005\x0015ß¹\x0015\x001b|ö¼{'µ)©Íÿ)kmKj;ºÖ
òZKV#r1ºãAø¬r\x0012«ÝÓi|f^w\x001b¼1>¤n\x0017¬ "Cm8ÁZ°\x0011x´µÐJü¡Ô¬8»º¹þùúêéá«íÆ\x0015otc\-·'º\x000e»¬Uáõ<OÆgG'Çï.>¿ÔhÌ¤º$Õý¤»á ]\x0016í\x000fÜÄí¦%ºÔ¤fÔp\x001d,Hu`HL=d\x0011G³wìJ5\x001b\x0013`×wvýãÝ"½"ã,;
©¸S+E0ç2	gÇoN_\x0010*b((¡ \x0015Ê\x000b.ó1|¥j!­9huvna\x0017R©JµR¡tW\x0014Tæ¢
+ø9??\x001d\x000b¡t	¥¡¸µ=Rå®5ûÂÇ÷\x000b©LIe©ò\x0008h£Eé\x0003æ\x000bð4È­ÊT¶Ê:v2zCK\x001dòÜª½4ýËTñ.9Ü\x0002¢O¸¹Ü\ÿø÷¿Ý_>^ß-\x0011*ð8ë¾¦vò\x001aÂó¨X=/hÁÛÍÉñ£³íùñé×Æ3«*YÕ\x0008«Ë\x0003Ý=MW\x0016Y8JÃsÃ\x001bÛHuIªHs±\aìv`\x001dµ8I½7ª¤\x001dÖ°v\x0004\x0016$ç-C~C=>Ò¸Ó~>¾\x001dÖ°n\x0004ÖæiHñY/TÝÊÎ\x0007D·Ãú\x0012ÖÀ
àr1Tc\x0005%áXMÏ¯ÛYCÉ\x001aFXuî\x0012ðyn§\x0015×^Ö¦µd\x0003¢\x0010\ê[Æí\x0004#IMÀ\x0004Í;ÖÀü\x0001¯\x001d\x0016*X\x0018\x0001\x0005Õ½\x0005TMs0¼å1Yfo0B;me¹äéÒÂóøïÑÞ*\x001eã+ö\x0003ÝVÚÊtÉ\x0011Û¥q®\x001cí\x0004\x001c)äý§\x0010×vx'Tæ@Ø\x0003%s3	jv$sà¤ä æ
ÿÍ°P1\x00189cXÒG=Ø!Í°Ä8ªçc"ÛQ«\x0013\x0006#'\x000côn\x0017X/n¸×>Âîëñ5\x001f°jFS:d>OÏÎÕ¨«Å;×;Ú¹<
É`Mëè9Û¶£Ðï\x00154\x000fGZ\x0001\x001a`\x000e
0\x0006
\x0010ØY8Aú$&þ3\x0008=/)_Ì,©Å\x001f0\x001c?¼{º.ï\x001fî¯¯î\x0017]Ü§Ë\x0002µ#EPÅ\x0005¾ÁÈr\x0004ÈáéÅÙçéæþáâìøèì[;CB		½&§|q\x0012/%âË(\x001bC: U	©ºW\x0012¨P B:\x0017'JÉ@({\x001c:(uI©¿Ñ¥4%¤é^J«âà®j/¤w²\x0010Æ(mIi»ÒrÞ3Þ\x0008\x000f¦µä¢$'ËÒ\x000eJWRºnJ/Ò¼D\x001b |\x0019¶vPúÒ«k\x0019JÊ0pÄi\x0018ó4³(ó#³ëZI\x0011ýÂâEeWS32×\x0014¼¿º½¿Þ¼¹|úòË\x0002qvT\x000cô,dcågf¯5H?ï\x0004{ôñìxóf{qøþ¥	¾\x0013'Ì8¡\x0013õÙ\x0002P1®\x0017h*\x000er*G#AÎs\x0000- f\x0006júAc\x0010MsW¬ò¦ùÜÊ!½_OZAËð#Ãr\x0000ÒÁëé\x001dâUi\x0003D#\x000f\x0017zx¥çâEÊÅ\x001fþrõëõ-EJî~ºÔ_\x0017m\x0002eY7\x0008[R¨á\x0018t~f\x0014e7@Äûpü¥O§\x0017oñh½ Î.æ\x0019q2â#ÀZsÕÎÔ±JÀ\x001bg\x0002{M	lÆæ\x000b Â¾ÚÄë¸~\x0007KfÆy]ÉëÆx)/>X\x0008\
\x001aiWØ\x000e¡¤
C´Óô\x0003\x0006ö,2Â\ùõS¯\x0000\
µ&hüahU.þ\x0017,Ú\x0015!WR(·Â:9¶\x0019Æ6óZÓfæÝ¬Ô
»9\x0006EP¿tÄ\x001f²äìåÓÍæÝåÓÏO×Kn\x000e{\x0010'Ñ4×.î\x0016~\x0016÷{ºO¶\x0017'wÛw\x0017Ç\x001f¿ûrùÓåÃãý×\x0019¡d^Æü¸\x0011/zÓ\x0004Ã-\x0013~o\x0002dÅøê:ªQu1¢º0/|\x0004W¼ç²ÍÚQºw\x0019sBú<Ï\x0017\x000c«·y=/°o[FS2Þe´ü:\x0004àó2:î¨ô~^{ØÆhKFÛËå5¥\x000f´\x0006«¹ÞA¾õ«®dt½ÇAIêâËG-ú¹rP\x001b¢/\x0011}/ân;Æ\x0010;\x0015ÉÅetü©çù²6ÄP"NÄx¦eÔ4ÙÞçû\x001eÎ\x001c8ÕÅPM4à¢\x0013\x0012òu\x000f\x000b(Ï\x000f}MüÔsÉðµéu3øNX2 w¥cs
µ6ÈÊÍÈ>?\x0013WrjxK+ÉÍæq%]^É¡¬l¸ì3âñzdY@\x0005;LzRyßkÐk¬\x000c¤ìµñ°P\x000b&ÖåÓã.«Ex7QiC¬ìµ>oõ\x0011QqL¡r{·w¡Óüyl&ªØìíÝÓ¯Ë*\x0016QØZº¤a\x00141\x001aÓ\s\x0010÷	ß^|x©Æ\x0001U	¨:\x0001
]5Î\x00030¬ÛU¸`þßDhJBÓI¨)­¨ñU²Ýb§­/çµk\x0008ÁÍ>rü\x0001?ò4öð¿ÿíþ\x001aIÿüçe{Ñ*ÇýÔN9R¼²;qS]ýMÓhãáì\x0018Y¿ÿþ¥ÍÈ®ätÝF²x²v82\x0019ñ`¸ÐSòå³\x0003TV ²T;$H=¶\x000f¤P7\x0008&E×ÝGªõìÓÇ\x001f¦ó}wûS¼$^ß>n~½¾¹Úüñîær	ª×
¢\x0017¤\x0018c79W`§C±EO?¾WÄãçxg<9Úüñôdû:-´0Bkvo\x001eñ\x000e\x0011hxªbá\x0004§ªÞÿ>Z]Òê\x0011Z\x0015²\x0018Zpdä±ÊÂ`gªÐ¨VJ;\x001bü\x0012À°½¹ùûß¨<ù®¡:IÌZ0ä'©ô)\x0013ê|YX¿=99¢ÊäÓkmÝØ2\x0011B'¡Ò\x0018\x0013¡\x0016té±NY\x001eðìÊ;x3¢*\x0011U'"J\x0017¤Dý$?Btç.¹¢fBS\x0012ÞEÔþgQá\x000eÓÇÀIm\x001dk\x0018Ýì¼µ®,|}Øüþòþ§ë[|F¤¿.ê\x000fÃN\x000fºS(lf3ä¸)5ç\x0006öý~{ööø#>'Eä\x000f/u²Á¼×\x000eªV\x000ebKMÔ<Õè	\x00167ð0\x0017é"V%±\x001a#\x000e67xÄ\x0013\x001e\x0013-vKðår¿`¤XÄz\x0018Gô\x001cÖÓÄg!<_÷TW»mIlÿOØ\x0015®$vÄù¢,µe
Iö5\x0011ýòè\x000eb_\x0012û1b\x0001Y\x00105xzvQa\x000e	Ìü&ÕE\x001cJâ0F\x001cCBîhÿH\x0015|Áñcskìã]vÇV5½]ÈÚû\\x0010\x0013£ÄÔRl¦6AZä56²¬]È\x000fkKês2+HGg9®ÝS\x0000ë"®\x001c;{ÚçÖ\x0002oÜ)\x0016Åië2³^d[í\x000b;¶/þÁ\x0006NËùýANºz\x001a{/þ\x000f\x000f\x001eÆ0ùÇïè ¹\x000bS(V6óV|íaì-¾úþ¼V´z6ÞÂ¸X\x000epìkêç\x0002ÅÓå¼_{~\NkJÚù\x001bz\x000b­"Á=&X´!°\x0008ª¯z\x0007;QmjG\x00166^r\x001cÇ>r÷>º[X\x0018ß\x0006®¤?ö7ÑjÉç 
µ,90Àqûê+ôrZ_Òú\x0001Z#a\x0017WZî×ÌùagÇW6¬óÂ&ÖÞ6(\x001ew\x001awªÎÙì¯ÖQ,¦Ýùa¤E?Ü\x000by\x0012\x000cêäi*¢¼kKÅÒNZYÑÎ«Zh-Î~¦×+ëÖ\x0008Å»6¨¯U\x0000-§­\x001c\x001cñ\x000cF+\x001e\x0001IfIx\x0015\x0012ãÛ@U¨óêª¦UæfFÅ¦Ö\x0000G6>ïD´\x000f#NÌ\x0018³[X`Õø¯ÍOêòk¥?Ëq+Ï G\±\x00015;\x0013®"Ie­r­ñÅ­l­\x001c2¶1¡K\x0014ö\x000cTkk\x0004_×*©Ns[µ}¤\x0008l¯>©)P0,Ø\x0016oBÜ{é$dÁ\x0006e-Ðsh=\x0006×	\x0008Ù­9rk¹è¢ê\x0008hB\x0002\UÙ?\x0014Í4uúäòñêËÝÕ²\x00020\x000cÆS\x0002ÍZÔZ2$\x0005
ÉF\x0014_}²=?:<}¹l
qa\x000bC¸ñRB~\x0018"sf\x0006£P{Ïdm´jF«\x0006\x0017ßË¬1¼ãâÂ/½	1¸z«p1\x001eO:\x00028).O\x0011ô
\x0001Rí½·á\x0019®\x0019Û\x000bRæ½o\x0012$´Z1@è¹¼s#.¬?=¦\x0007Üê´áoßà\x0013~®]\x0017à\x0004ûÉÓë«ÛÍÛûËß®½IãúJ\x0016ö1¼{m\x001e äµ½ë\\x001c\x001e\x001fEsv¶Eæ×9¡änNÍ\x001aéF\x001a÷àÉ&ä&,/æ%;­ªäTýë 7£/oó´k¯ç\x0013[9uÉ©û×Óæ¬£õ¬Cê\x0004?ôz9º¦ä4Ý`P\x0019)­§@ái=ãï¾WªÕÊéJN×Ïéøî(=uGL\x001e\x0010ÿ\x0005z\x000c3¡\x001bs7\x0001Sâàs sêr®\x0013Sûy%ÏVéè1RÞ^Å\x0000ëþòö§%Ä\x0010ï4ûÔ\x0012h£5<uMy\x0011áÑy¤ü*igÛo_Ç\x0012\x0013º1£Q"ÝJ\x0019è.\x0013M§ \x0005\x0006¡å\x0018¥*)UÿbZ®;À¶ðTº\x0015\x0017n\x0005¸~Szò\x0019ÑHrááO®ç¢Ü­¦¤4Ý\x0010\x000e<-&È;s.õÕiKLÛi³¦*XöëF[þè{:¥­®ätÝ\x0018t:-zâ¤2È¾SzÒ&Ð\x0010ø!Ô¨¼;\x0007íQ(!C/¤ÏC\x000b"¥Ç\x000bêD)\x000c\x0011ëù\x0004¨FNYÙMÙm8\x0011D\x001a±Ñ;\x0006õ¼£»SU\x0017þÉ|rkheRÙÎk\x0016¿4&/«ë[J+åL:7þP(¯½¹üëÕõÍÍr\x001el\x0003\x0011»\x0019L8·|¢Ä¸B\x0010³7/òíÑæÍöGÇ''/\x0015ô0£.\x0019u/£ÈòòRQ\x0000:3îUò´0Ñô1ÊÀÓ|µwºU<xÉë¨æ³5Ú\x0018]Éè:\x0019±ñ,
9ðÞP)¡\x0007Ã
\x000cñø\x000f}ëêô¤=Y(»4.'`MCBT\x001dSð'WÏÈTµ|ò9ªùæPRuÐõjd;ß]Ý_Þÿ´ùôËõÍõo¯ç\x0016<þk¢;§¾\x0010?©QÝ°8ß\x001büîèl{övóéýñÉñ§\x00172\x000bÌ©KNÝÏ©¹é\x000bûO\x001daæWÊ¹Íl¥4%¥é§ô¹%ð<L/,¿ù\x0005iä\x0018§-9m?§dÕ¿éùÌÒræ7©y1H+¦+1]?¦á\x0018\x001e¥Ä5/'¿@Ôþ=¾äôÝ2ä·S¼³LkÉ\x001d\x000e>Ì\x0013Ì­¡\x000cý)XØMÅ\x000b±åoÎU\x0014ÁÌÇÞ7rî\x001e£ÂzV3PîLn=îYÞa®ÜÕ
*+PÙ
j>ôç$xM ¬ó\x0019¿¼\x0018Û²²ñ²ßÈ\x000bÏF^)G%)>¿\x00073¿p,å÷­YG0³\x0011|
ûÿúïÓ/÷w×KJ2½!¬\x0013êÀÓL#Ãw8\x0008\â®±\x0001Ä6§çg§Ç¯\x0013ëX\x0011C\x000cì|rN6èü\x0008¢(,!zýqb[\x0012ÛÁ5vY\x0019Á)Ñ`\x0003çp\x0014ç{G}	ì\x0007c\Jã\x0019&`~\x0002¡òE$^aSTÂi§èoh¥\x0003\x0017\x0005:å9÷jý\x000c^©À6ëy{ÞµG¼}ú-Fª\x000f×\x000fO÷\x000f7ËË\x0002JèQB×ñ<,\x0013¸ëÑÏÇa½½ø\x0014ÕÏÇ7Î¶O^ìçtÁ\x0017S~zÚ\x001c^ÿzõ¸XDÊßsÒÆºõ¯Ññªº7æçíÅæðø\x0003^§_|\x0012\x0017úT\x0018:õë}¸¼ùõ/KVÒZÍ³Pq"

J^Â¦F­7ué}Ø|øÃëXºÄÒÍXN\x001dØD4t'ª|)ÑR¹>,[bÙV,'xzÆ©7Éæ\x0003pÜ¬î\-_bùf,éhië=¾uL\ÏªF14píb%O{`ZbÔ>á[Ú]C\x000f\x001ckÛ\x0007VízÙ¼í5ôr¥­<òOqÍv\x000c@æm´\x000b¹ªm/÷½C\x00019Z°\x0014¶M\¯\x0012Ju~ÈjßËæïQ)$e	lÜl42@å¾c\x0005Ð	Ví|Ù¼õÿa`Â^6\x001dKüaèdzµw2{ÍkQ¾A&\x0016øF¬¬Óù\x000e:§àÀÒ\x0019uD4-`{BZ»ªºmñfVw|Z\<öÕê©ÞÕ~d\x0016zhSO9üåò×ß.¾]Vñä$\x000b©\x0004ÐdyÝd?¦¸Cc\x0014=Oë\x001d¾ß~ø´}÷ñ¨\x0019¡dNF¥¨7hIÊ\x0010Ñ!@<`öUÜ\x001b\x0010U¨¾ID]"êND[B±\x0005'\x001d¥Ù«\x001bhc4%£édQ¦ Ý\x0018oöz°ð\x0018åÐn´%£í=1ö@Ò \x000cei@¶\x0013:+ÞýW\x0005FÎÊ\x001aâ\x000f¸\x001b'cóîòúçÛEÃ°è¦\x0008DkÜâ9HÑ\x0014O\x001f­y·=~÷ñ¥aMfÞüdRóS+\x0018Ö\x00060Ô\x001cJ¡\x001e\x0012±Å[|/+Ù\Ç¢\x0019ÈlFÓ¾³¥ìpôj/Z(ÑBÇ²Å=©µhàiÙÈ¹Ýó\x001e¯¢\x00053\x0017>2µðQ<\x000f¿-HÅátLLÅQa\x0017k~ZÉÛÍËùkË¤Ù\x0013OÃ§\x0017Ópf®{djÝ£\x0016>MvY:C£¦#`nµ\x0013ó7ÿ&@]\x0002êN@ÉÃ¤\x0013,Ì\x0014cLhZJhJBÓEhCÈ3é¬á>P\x001c\x0003ÛÜ1[JhKBÛIèx\x0013ZIº¨\x0011ûè\p#»Ð®\x0013Pça&F¨©\x000b	g\x000e\x0010 zNÀl) /\x0001}' ð1AÝ\x0013ê?\x000bÝ©Em\x0001C	\x0018ú\x0000Q½vÔ¢\x001e	³rÁó\x0012\x000b	\x000buG#juÇ\x0016D±wFî\x0006\x0017q\x001e»4!B\x0008ê =ðH¥YhÜ N+)Ì¥b\x0008+s-ûìµõÜ\x001b/#Tæ\x0018\x0011ó"Îç·5\x0011VöZö\x0019lëòd1\x0019C-\x001a,av\x0014Ï*O.%¬¬¡ì4Ix9\x0011ò¨ HÈº$Î>«\x0013½\x0014±²²Ó Ú@%:\x0011\x0007Ø§\x0018§ÆÈ½Æ\x0016ÄÊ"ÊN\x0004*+H2Ú6ÏÒ5a`\x0015¡²8ÐiqðuÎ3ÎÉ¦óÁ*!Êè\x0006*\x0003\x0016Ç\x0004îp\x0002è¡\x000b\x0015Px\x0015õ¼¤	±:ÐÐy cTmY¯Eó|b£w:yó&EvþìbÓ³Ëq¼i><*"\x000bÅLUËä\x0003æG\x0005\x0004ªJ¨þ8Þ7?.5D^\x001e\x0019cç×O®#¸Àc-µÔo\x001b\x0017\x0007FÖ¹ó^^]òê!Þ\x0018WÐVuõN¬ñ$\x001d!Ñ­óº×ñ\x0006|x±Ëöçí`Áã\x00127\x000cá\x001a~I1øxAYZ\x0013xª\x0014É:yeuÚäØqsï\x001d¦S.Åà§îªuµ\x0011X*\x0008µ$eü¡¤Ü>þr·H§0àÄ\x0018Ñ\x001c\x0004Í¡\x000f«K4\x001e·\x000ct
·çïO\x0017AI\x0006íd>\x0004ÖÞ÷IR\x001cÑâ¯Ñöe(_FÖIÕ\x000b\x001cìËïÿù¯ÿÞÞ<\~YöÜ\x001e\x000f;­\x0015¼\x0019=;÷\x0018¿ï
\ÝlO>o\x000f_0øb^È*v¬pàè6æu 2Á\x0018º+\x001e\x000e
óqëËáT	§ºàPQ>«òä.­ç	\x001fRËyc×bº]P4-èÁ\x0018ePs\À'¿´x\x0001µn\x0013Ö/\x001bèÙ*Ø5\x0015~¼¼½~¸¹|ØüðtýãÕý¢qZ8¬¤(ä±\x00146\x0006Å<sf¯íóùöãñçíçÍ\x000f\x00178ÑóZ0k-ha\x0016\x000c\x0007HJz\x0012kµEIÂÞ\x000c\x000eXUÂª!Xw`izRz\x0017L´ií<&^N{)fñ[\x0014ãÏïî³BÆFnÞ_ßßÝþtus³Lã#^ÈÑ@´ÛFç²à2z~zq2ðÏ:Æ*«£h>¿¾ÊBÏLzüaO\x001bîÓýÝ\x0017,°Z8ÖiªØ°\x0012k\x0000_td¤l¼\x001f}EåãÓÙé!\x0016Y½4UI¼7f­X©,I®¤¿\x0017#izÅ\x000e'X\x0013ëx.\x0006ÔHóÊ\x0018g$ñK'y"4þ\x001fV ¶%ñ\\x000f¨\x0018Û\x001aRrÄb\x000f}ùQ|¾_ÝZ@,¤¨\x0007×â\x000fU·ÕÃãÝW<\x001fÿ\x0015â4ftÒ(\x0016\x001f#½\Ù#÷§m¿Ù~>?}ñ\x0015	mIhû\x0008qv\x00115Xy R9¶±+|æ="M¾\x0004ô]*·	¤¢­\x0004¨M®YÙ»Û·\x0010îr²H¸ÓdmCÄ)°i
ã­[Át`Uy°ÏÌª\x00151\x001eùÔÊ4Y ¼l|º_&4\x000eÊp>Ñ\x000b\x001e\x0001¥\x0003tËðÏß1>½¤.fÃ\x0004&@è\x0004æ|9ÌÐ`\x000eI\x001eµ G\x0010U¨:\x0011uÖçöÂÐa¶g<JUU¬·3êQ÷1&á´ÓÄìTñÍu6Ê}iS"o\x000b1Ì¦/Ä\x001f8|>»¼þõiÉI\x0016Ñ{\x0003i4\x001eùb\x000cÇK¢LGuÏ¶Ç\x001f.^§
Z©@á3ÊD¥=å\x0008â\x0016äÑDÁ
ÛE¥J*ÕJ¥óÍ;F\x000eôâEàwàæ1ðB*]RéV*6Ð,§þÑ¸]5/ÕÜ-2%i²¯ÊjªöRæé	n® ³ÊT¶ÊIx\x0015¯±4bÝK0y[Íßc\x0017R¹ÊµRùÝ­Õ	*¡õr7XÙµQ	\x0011fu(ñ\x00076\x000co.ïÍ\x0001¼e4\x§\x0005çJ$Ì\x0015íßlÏ^kÃHªDRHxÑH\x001bÝ\x0008Ç\x001d_Z\x001a`¦¹ÊÕËLvÞfE¶¿¿üòoOÑÄ¿¹O s¶ïø®æ©\x00025Z)ôÝ­â\x0002Y½'\x0013÷ûíá¿\DÃþæ,þðõ\x0012'áj°ø\x0003}\x0019ÿ¿¯\x001f6\x001f®\x001f\x001f¯î\x0017k_§\CD\x0005®£(g(´'¾?Û~<<=þ¼ùp|~~tö²¢rõ\x001dmÒ£)ýùÓæíõÃoW·\x000f×Úv¼K"\x0008©W.d^®\x001cÛïÙGÍÛãÏ>~Þ\x001e¿ÔºcfÓÑñïrçÝýÏñË\x001fÞüýo¿^Ý~¹º|ý\x0010ãkW<%»r#l
ü¨ÝóÖÉÓ³wq'\x001c\x001c}8úxx´}á<3.¸0\x000bÃç÷C]Îìuv·óªWñZ¢\x0003©\x0008DPúÉ\x0019\x0003üè\x001a\x0007Ö%°\x001e\x0003VÜ×5þxzæÎ].Ì'
÷\x0000\x0012Ø\x000c\x0002;n\x0015!\x0005õô9\x0002«½VØÂ¶\x0004¶cÀZå\x0015FëËÀ\x000bFöfö\x0000»\x0012Ø
\x0002;\x0016Jø6Ne\x0005Êð\x001e\x000esý\x001e`_\x0002û1`Ô¼¤\x0005Ü¯lòÀÚxæö\x0014\x000bÚyCÉ\x001b\x0006y=Ûà|i6BäZ6;nÔdí3\x0006õT\x001e=¶ùÀå:|æüÐ=â\x000fs/÷æú¯WÊ¥-6±h*ðø4ªÓ84NWè¹@\x0011£¾9þãÑKõÜ\x0010fÎ\x0002ÂÜY,¦\x0017D\x001av:µØ§¨Ap
\x0019j\x0002ì)-,Tó*\x000e5«âxþîaóéòþîË/\x000bgFqgs\x0004uLàñ\x001f\x0012ð
p\x000eON?o>mÏN\x000fß¿\x0010á¨y_«J}­#ÀRäÞz\x000f<\x001a:`õ%¥1ôs\x0006K56aö®±	Ûé·÷?Þ_Gú¯\x001e®xnâ_èçÛ¿üîìêááî6Þ®\x0000³\x001aTçAðtÑ\x0012,½[ég\x001aN6Û³7gÇ\x0011ÿ¥ãÅÀº\x0004Ök\x0000Kª<V%3\x0016ç®@7\x001f)ÜlJd³\x0002²d\x0001\x001eíãm\x0012\x000eÈû\x0015´\x001fF¶%²]\x0001\x0019§ØHÝ²©*	W\x0007]¡XT\x001fò¥°µ¢ÕVØIÑª~ÍÔ³»ëÇ«E-w,¡«\x001fÙÐÀ/ÛºT\x000fªß2ãtz|~tò
lô?ä1­ñãåÏ·K\x001e«¢Eð\@\x0015â\x0010.p\x000fª/î
oß}Ü¾ðªÆ®$tó@v"O\x00154:/¤AI»VÀøÙ]erãgwhrëÏ~v÷ôóÕÏèÖ\x0016}ö\x0000ìÏb\@C	Ü\x000fH½³Rö³ÓwGïÐ½½pºæ£éÁ%mlo/\x001fïn(ç°ÈG\x0004¯³r°¨¡j»(í'eÕ\x0017Ô6¶\x001f·ç§'qXÀ
%+t³\x0006\x001aÏ$ª\x001bYS­å\x000cWÕ ÔªJT5°¬{Õ&Ô@Å\x0017\x00022«\x001d^V]²êeM©¹¥\x0013tËËJ¯RóâPå¼LDRÈT|÷ôÓ/^ÓÄD"ÉÿF¦Ô¯a}Þ¥b¯Õ ¥·ï_|ó·óW7»k­kAÓù\x0016®mV}õ_\x0005ã`^Àÿ*\x0017.)Q\x001c\x001f®¿<ÞÝoÞ?ý|·\x0008Ð\x0001ÖìODoXê¥ÜuYQ>î\x000fÇç§g÷\x0017ïN_GÔ%¢îEôüj©ã]*WÒù\x001c@i)(mIi¿UJ_RúNJ@ívþÜ³°¨nÀ\x001fÜê\x001eÊè-eµ)£·¸)ko	O×·\x000fËÂQY<äËQÊØÅ0!Í*#ºÚWÆ?çøãçJdâÕ²ö8¤lÏ»¿^.ª¢ó\x0013'1*Ás\x001dwÛI%åì¾ÿáôÛ\x0017*ç2\x0016XÐJô%ëy,ô\x0019¹æ¹¿W¸âç­£µøy§h­þ¼nóæîéßï¯®}dÙÛÚð[µnÏ©¢#Ë¡Ï?õ÷ÐéÅ\x000fgG\x0017Ç_vù"Ò³KnÄ:D||Ñ=º}¼¿úÝÍÕÃïÞ^=ýçïR\x001d××^þ¹lIçO§qy>h\x001fJ½ù£ç8ç\x0008Ó^üë&Us½P½\x001d-E½5ã\x000fYÝíòö\x001aë%7o¯nîî\x0017\x000cÔEEb«8~× øñ\x001d\x000cG\x001bxßÇÛÇX)\x0019ONÏ^¦«ëc?±Â\x0008+äÈ(zõ\x0014 GÖì/Õ\x0014]3«*YÕ\x0008+â6N¹0¾R¡ëÃÔ%¦\x001eÀDE?&\x0015¤«\x0013#È31ær¥ËY¥=¹Æ\x001f
h
î^TÖ\x0000E©&2nSIe5£8ì6Ú¯AfáÝ+ur~BFèd\x0007\x001fR5/\x0016Ú\x0018Ò4QÜ«µÑlBT%¢êDTNtÙ¨²2Ìsêã¯\x0013y	Ù ¼¿þí·»¿<^mÎ/¯\x0017Azlt¡D9ì&\x0008ékåå<düéÓéÉ\x001fÎ6çÛã%¤ª$Uý¤XÊGQ\x0008^5æÊ%ËØ4Ô\x000crIÁì\x0012)·aHÇ¤sÝ¢Å¤^Î
\x0018â\x000fù?m>\Þÿýo_~¹¼Ù\}¹¹ºÿ²(FIÏåüºclÜF\x0018ö
/6\x001f¶gGï·'Ñ\x001e\x001c\x001d¾\x000c%2\x000c"Ç#Oé1c´GãTª½®û.dU"«Ad\x0003¬\x0013à§x?ZÒ\:WMi"6Ã+^¤l±/Þýýo·ÿÛ}$~w}ù´¨°Eá_²\x000cÞ	j'Ç'\x0015î3{ÅÒ\x0017wG\x001fÎ"ð»ã³íÅ\x000bu-Ì\x000b%/ñâÆ@¼·±\x000bÜåe÷ÄÂÚqU«Æpã\x001d& b\x001bd\x0004>!7ôUUÊm¼ñ\x0000\x0015o¼$\x0000òÖ\x0004µùð÷¿=\Þ.Ë*\x0008htSÓ:P)ù,P\¬üê-0þIG·\x001f_Jj#ëW`¬Å9cúþêæêöjsø\x0017¼ ü?E¼\x0012Rµ\x0006u@#&
¿ª	
{)øOq7À{Áÿõî³óK«ô»pë\x0001MÄÏOW÷XI¶¨Y ÎI
¹dàªNëò\x0013 Û7\x000fñ\x0016\x0013íÃ»£3¬#{©Óx®ûlî3wÍ<mN.° QiFé\x0018AÃ[ÝîýÌ|¦êb\x0013öu:(é Nzq@í1Âr3¼w\\x0016¤ªB±F8YÊj¦å+çMÿSWPJ|È2\x001cüá»é¿§jÙ»¯î7ï~ýuÙLIí\x0014¥­Qô¬«¢k¥~T×</0>}wt¶ù|úáÃ\x000b#%\x0013f9M\x00181wÓ[1
NÄK\x0016\x001bõÓSæ
 ÷&³.ÃY\x0005#þPwÊ`ÙùÕýýõ²éÁÞ
ÉZZ4\x000fðöL\x0013Æ\x0014«¹kQÀ\x00063¬\x000e}Y)]Oª"²¸ôOjPu£äÿü×\x001fýúÛýÓíë\x0019+lâò ÐM\x001aî­ÏÚd»ÚÛ¢ø{ôáÓÙÅÇ\x0017RjRÏÊfâ\x000fåÒ¾¹¾¹ÞójYÊ*tA³Ç¤w[\x001b4KÉXU^üyaß\x001cDÏùR°µNÐM)ùý>\x0018Í³ÏæÔi´öÏ|þ\x0006J]RênJn4;1XÍöò\x0005^»Ñã¿9\x000f\x001c@7y}{ýë"\x000fé­\x0013Ôs¬ó\£.\x001dú¡lýÜO>òøãñÜ#Ìµ%a§-yøËåíãýÂ{_PÊ°Ð°Ü$ï¦ìi::0±ÁýÇó³¯|Bé¹JæPy{]æÃË{Z¤Í\x0019ðé+­¢ÕNÓévJrP\x001fö$ß¶'Øa¾9ÜþËÅK
jö?à*¾½Ú¤Ïýöêæòññ\x001e¯Ñ\x000f\x000f×?ß.R¢\x000eJp[	\x000eG£nt\x001egîËfhø»lÏ1Õ{\x001e·êñ»øîËåO\x000fñOÏÿ°ËñÍl®mRû3­Ç¢i5µöa\x0015u~©WÏ\x001c§ÙKíWyã:Ì/zzRaù÷«Ûùe$\x001aÿwOËzú=V)'}~\x0016Òç\x001e ñ>Rüpô±¾ÄÅ·½À¦þWÙ¡d\x0015Ø\x0006\x001d$q\x0014ËSÚÁ¬)SÎ¡\x001cbW%»ZcÝã]
H;Å±:ÅZ5¾fëµØuÉ®×Xw7.êb8K>\x0018R\x0013Jk2ÄîJv·\x0006;}(61MËîl¾~\x0019¤!t_¢û\x0015Ð½¬ê)¿¨q\x0016\x001f9·\x0012{(ÙÃ\x001aË®rûQ=ð\x0013\x000e+mb\x0016\x001e\x001aH±Æ²ãÜKR0\x0007$¸½\x000f\x0011z%û(kÛ¾qw89\x0019÷I4NÒ²óN%^9Ä^Ùv¹q>üY\x0011\x0004©Ôb65E´^i·ËÊ¸Ë5¬;¦z\x001dY°<%EA.¬$äà+ë.×0ï8ÐÀb\x000ev°¾ ã76·Þ7\x0015¼YË¾Ó#&Ê~_uWÞ«µàm\x0005o×Xy#yÏ£
<+%\x0006JtÕ[×\x0010|åXå\x001a\x0015EAøiV°6·U>ïyëÖ2òkkøV¿çiå£µ	Td))­ ])¿2Ä^¹V¹oõë\x000b¬À._CmÜÔ5-­+í\x001a¨¼+¬á]Q¼RLÒB¼6¥ç&\x0007I§ÍJf\x001e*ÿ
køWl'IÉ(2ÀÅ|Ú²RWtµ+m\x001b¨/Ok8X!K+/\x0015&U§ßÉ\x0019µR(\x000c5\x001c,vÅ8ZyïòÊ;\x0013añZÛ¦òQ°òµãchcèIÍjoshSêS\x000cÁWf\x001eV1óqÛØt`QË\x001b(:\x0010ÔA!­+6PJXÅTÆå¦×\x0003	õ\x000c°&¨­æÙÀ«ÊÚ¨5¬M\x0010ÑÎ'v-sX¦¨ñNÚª\x0001~½Îv¬q^§K_ Òr\x0019¾1\lâZ\x000b¾:¯jó\x001aÀ³¥«ÌCQCà¥YÉÁªê¼ª5Î+PSt^½:ÈbáCJ·\x0016{u\Õ\x001aÇ\x0015ãaVÂ\x000cÙwápÕ"=Â®«ÓªW9­ç%E÷ÊÃ~¢qT\x000co`%;©«ãªW9®1I]3\x0016`jJmg£2kVºEéê¸êU«WTbcAK®cµS«®ê÷\x001d¯«^á¸\x0006!¦`·îÀÐÊ;ÖdòUQþ\x0010|u^õ
ç5\x0008©±EqwÎ«õ,\x0011éåZçÕTçÕ¬p^'ñhÚñ\x0001HzÊºü`ï¡\x0014t\x001ab¯«Yá¸\x0006¡x¢\x0013je\x001dH*#\x0002ö®~­HÞT§Õ¬pZÀîüä\x0014Öv¤Óê4dÞèÑ;\x000f'õ»á¤\x001f.ÿzy}»9üåïÿïãB\x0011È$¦hÌNY^sIÜËí\x001f·gÇ\x001fñá÷\x001c[Ý_C-ÆãÄ\1ÀªY\x0015\x0003å¤×<\x0017Üë¹ËRT© q?]2ÿßí]2Üê\uÉ»dv]\x0012¯¢B
#¨À\x001b@+II\x000blaT\x0005Ïv4 ª\x0012U \x0006]§6d×°OÆä>ÑUÕ%ª\x001e@u\x0012³>\x0019î"þJÌë¨ÂÖ¢\x0017[ìH¶óÂX»ywýïË<P¹T\x001c'«ÍX\x001c%B&À¯ÊGÄ?æìø¯Óþ(@V%so0wJæN.wxÿ¿ûxýeI'".*\x0013&\x001c£å\x0003ZSÍ==ñ^VìÔíæðì_7\x001f\x000f±\x0017ñy>ù'i~»\x0015ÿ7ý©ØãîW¬:e¢Yº¿úùò\x001e¡¥Ip2òÜþÇÕ_ã\x001f\x0014Ãkì¤¼W\x000fÜl<ÝéõØkptúø¿þøÝÛÓ\x000fX'3uÉDstvôn{öµ
è
-\x001eohEÃI0Ð$MFhÒYB3Ôñ:\x0016ÿzª\x001dM¥\x0003}&&@xDã<é\x0018Z<¾º\x001d
\x000e¤&4<8¢¥7uD\x0015Èâ65Í[Ít\x0007d8ÊÉ&2ï3ãchÑØv´jW\x0010M¦¤=&Ô\x0002£\x0001]RÆÐâpÍh^ã½cBC%-Ð¤Jc>\x0010mU=ßfQ\x000bcªÞhºç#µl;$Å\x0008chÑtf´hËÌØTâ\x001dÉ(W\x0011É¸~v\x000c#AüOã\x0007
:+¸jâ@Òªé|\x000cDXábÅl÷\x0006a\x001a¶Èl(s;±¥Xzb\x000b+°E\x000b$ÝA\x001fÏ¨4ñÀ&IñõÎ\x0001þ;d³;Àr\x000eIh¨pB6×Kb6Þ8[Ü²²Ù\x001f`ý@ 6©z3²YòT\x0007î¡Eg Û\x001d\x0002\x0004vU&Ølu
¯Ú\x001a\x0007V\x0002Èv CJG2ÏÐR\x0011\x0012kØè\x000cd»C­®Ñô^\x0011\x001bPáV\x0008=ðÕH¶:\x0018LJöð1M÷[ØÒ»}¼çz½\x0006[Ü°²Õ#L!\x001b¤s`\x0000R½\x001eÆEJ2[áâ+<´»\x0004\x0011c6IÔ¥\x0002%\7v¤R\x0015\x001c)>²C»Kmqêw\x001bGFÓÇq4¼\x001f´{\x0004\x0010©\x000bíOxJùJCýzclÑ
A»K\x0000zèA³KÎÐ¶åOêü\x001aÛ-þ; Ã%x¼\x0017$w\x0015RÅ0ºìJ\c»Åµv\x0010÷¿£us&É^£+åo
 VÄ±\x001eÚ½Viü8²Ù4qÏ¢½Í!é^·ðøÛo?â\x001a¿kk<üåòéÏwO÷_åÂÁ-) 0éA\x0014kSa©WNâÊ·ëg<|¿½øþôâkmx\x0015Sº$[Lé\x000eú
0»W.¾\x001d«·^n>]Oy÷çy\x0000E±É{ «(\¹)ïO,ÒºÝ|:þêÔÆ
&%]Âe\x001f3ì§ÖÝxÃ£yx;\x0017j\x0004&å2Â\x0018}àÓqÂ¦\x0001lqe\x0003êh·ì\x0008LÊ\x0011|#)]½\x001b>SHÉÅÈt*ÝÀÏ¤é3)\x0000=\x0000ÃWÚo.ßÆâû×·A#`j'\x001cÿ×?éË_Ód\x000c\x0005ñ?'(Òôx}ssõøøu\x001a¬¼´{¼\x0017t]\x0010Á\x0003í\x001e-B\x0011¿E7§\x0017çÇ''GççE¾þ«4Ø0ÿYFcApä¡À¤Bk¥¶./N¯Ó|mmþãÇÇ\x001fEáB¿¿|B;Gâ\x0004BÐu\x001d»\x0016\x000c­¾øBßo\x0017ÿñÉþþÓþøä¬ÿi|2øÿ´?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÆÏý{Zd0:5ãS`÷3âî3EÅ*Q7Ï$¾^éÝíÍUü\Y×\x0002§\x000b\x0016(w tâF\x0011\x0004/æFâ!
v[]FwH\x0004¨D^\x0011¼7äWG\x0011\x0014e\x0004¢i\x0016s²k1Î1\x0011T%ê\x0016¡L×¤_!§Í¬çbW2\x000b%Ð\x0004º_\x0002·´D\x0001\x000c¡g&¼ªy,|SÁ7ÝðqÉ\x000c¥È\x0004\x0017¬­ç
»Âî[ÊÕ"­$°Ý\x000fYÚsÊ\x001fãfFzÇÜé ô¾õ\-\x0002¸J\x0000×-\x00000!i@9&w\x0008½Æ)~L\x0004_à»E@
×"\x0002õWáNnê+ÄÐa´\x0008¡\x0012!t\x0010>¯	0&:\x0015\x0012\x001d}	~Ë°6ª{H\x0004¨¬2ôZeÿH~	¸»Ëf	Ê¼YÚQ5XÊ(C¿QÆÉ-N¥jJvá\x0006\x0016\x0001Öv\x001d\x001c\x0013¡2ÊÐm÷4K\x0002©BTâlÒü\x001aø1\x0011*£\x000cÝF9xÞv\x0015½;IÜN\x00194±Ê\x000exHÊ(C·Q\x000e\x001eJÒ\x0014ãMC\x0012\x0000K0Ü=Ê.C·]\x000e1BàÊ\x0015PïÒ¾m\x0012`Þö\x0004]~»¬\x00029F¸~^e½à¸<¹Ñ\x0012T\x0019ú
³ñÜ±ëªÙµ ¼hÕäxß¢Ú.ý´^¸ÓGçdÛ¢\x0005öd)êî[tÛô[
\x0002C\x0004	¼±7þ"hâ ÄkÕé&î/\x0004#\x0004±MRÛã\x0007ÎEÃ¨Ô;}³ê\x0014\x0005\x000f÷¿»{%guO\x0012âýïO\x00088ù% ûðA\x0011ÙÁí§Ù}µ\x0001¸Þ)V7
\x001et;j)âÉuß§ÿùç-þâyßÙóöJÔEÛø\x0007yãóÙ7Ï?}zøürvwÿÛ/÷\x000f\x001fÎ®ï?ÿ)"n¨~Z_\x0006¬,S¶À%h\x000fz«§ýÝÙ7·¯Þ^¾»;»»xýýÅåõÙõÅ»ïâß·-\x0015Ì¥RésG)ñ\x0017¢ºzÅ±Tkù¿^©Ô\*5X*\x001aüÐÀ\x0003+\x001eðÈ¯Ò\x001a÷J¥çRéRq$ýV¥\x0012e.a­G°W*3Ê)¨c2Q¬\x0000Çë.l\x0012NtHeçRÙR	.m`©ÏÐx/>é\x0006®Í/ôJåæR¹R9Êá(\x0013×ØÙ+¿9\x000bv\ª©z4»\x0018+Vfw\x0003.C¡²`¡ôÚ^ª^¡js5Ô^q\x0012ÉwÈ\x0005Øpf C¬Ê^É\x0006K\x0004Ç[@ãµãÙm§,)A§¾ä\x0015¬T»\x001cªÛuRè(VÔ\x0017Õ\x0005	Å¬/&T¥ÙåHÕîs\x000f
%4Qj¯ÇúÍùË\x000e±*Õ.Gêvä@ÕÄ¦hù·ÂÁ,\x0015îPûbRUª]Ôí.\x0014E\x001fx\x0001¸W¼\x000cÅÚð\x0005õ¯Äò#Å\x0002ªÉX©§¦EÌý÷%¯`¨¤
ã¤\x0002ä¤\x000et\x0005
¨zg\x0003ßÁM²¨ãbAea¨!öL¯ ¥-l:Ëvµ)§W¬Ê\x0014ÃHSì\x0014MÅX¤Ws,Ö&l
\x0014wUCcGÃ\x001e@î#rD §eÖxÑ{¥ª,1\x000cµÄö\x001còÓðÎX/yvÝøM&³\x000e±*[\x000cCÃ,Ç¬1ÂOéI¬µÆá^©*S\x000cCÃ,ÍÚ]8Qzê\x0005\x0013·/©Þ¡²Å0Ð\x0016C\x000c®¨\x001f(`VåXQQÙb\x0018ic¨O´\x0010Ñë,
£0\x0017\x0019¹Ö\Ð)ª¬\x001ajµ4=-\x00134o\x001aÑ.xòÞµ^ëFîv\x0008ç[r
\x000b}Ä\x0010ãåY\x001f&bS¦bå\x001fÍ/¨\x000fëaµÿOÝÛ&Ùq#Y¢[¹\x001bxi\x0003\x000fÓ¯\x0014då\x0018Åd'²ùÓ²U|Æ"kRÌ²~ï×lcPë¨ÌJ\x0006pÇ\x0005®DdD\x0000Yªêéf\¤s"\x0000wÃý8û§²£<
g4P®ÈÓ&è {Å{Ù9}¢7~ÈYÝÏ\x000f_î\x000eßÝýõöþËÝ_î>}¹ýxwHö\x001a×\x0013¢1!\x0013¤+·\8ctK\x0008tçÁ^_Ý¼§ûÛóë÷\x0017ß_¼yþúbù×ÿ¾jÐ05
3Ô³dpOa;F¤<^§¿<S5
§¦|ÀÍÜd\x001bTXÎiÃ\x0001¡þ*ÇVs
\x00177gi)-­öÁ\x001a\x0019¶ê\x00132Ð!ö	
0LPr5\x0015Rä É·AI*ÓØ}Kì12Ç6\x0006"C_Æ*£1¸'ÚÙd=	ã(kbBHS\x0000K%*>·\x001bÒ" `B÷\x0004¸LÔ5\x0019ºq±Ætªâ@ZÚKVã»å½\tl>\x000c=>ã/\x0003'NRMrA4Óy.Ê4¦P6W¾t?\x0017l¹Lù2\x0014ÄH\x0003\x0004qáDQ3¶×Ì·\x000b4î\x0012`¿¤ÿár¹@C/ äm¢é\x000eØMÆ4.\x001eí"3Çûç\x001cQÁË\x000f£Í2É¸\x0019$v¿¨"t¯]ö	-çüaÚEfæ,²ôÿëRÐS®ã})0\x0005Û«xÚOÆ¶dì$2 Eö/$«¶È\x0016bôÞÚyeÖÆËfNÀ¬éÂ\x0001x¼<hË\x0019yÙBóm²úÿ\x00046@uü,Éh,\x0007\x0000NnGÐO\x0012\x0000 jB3zÂÆ¡´\x001b¥ãäréït\x0019)\x0006ýúÝdLã5ÑÌñ\x0006Dí\x0013\x0007é\x001f\x0004Kq]YêÝl°q5yHÆ\x000c6Vó¸FtTpÎlD+¹¯Y³SíYÍ±\x0001V3Ã
¶×ràÒQY\x0014x ;c7\x001bÛf3ìqé-¤ÎXÚ\x0019ÐJºLùî\¦½l¼jØÐão\x0013\x001c'ÿÐ¤ÙÓW\x0012o£ÕØg¯[6zÒ·a\x0017k¬4¤¢\x0015þ6ñI¾
6\x001azòm¨3\x0016uÊE1Ý¨®ã\x0018èp\x0014¨ÌY
\x0015óá9Nmf
\x001bðrÉ&:ãyÀseà\x0010
ì|\x00026±µ\x0002q\x0015 Î²å#\x000b×-ÅÂ\x000e£.¹þ$l´j-t~@'Ea!Ï\x0017MtÈú\x001cB{0\Î\x0018\x00025C<\x0005\x001d{BgN0\x0010HbÛyUä{k\x00174ßðØ¿ßKGÐÑ³è8ÇõöhQs]°\x000b\x001cCÓø'\x0008Ô´1-\x001bz±ÖA:i­,\x0007Ö±\x0010z\x0002\x0007ªm\x001bªåç)[n4ÓÁ3Þ9ï7ÒÎy
#­-°Il;\x0013;\x0010sý\x0011±Q®Ønân6®]jô<ÓÅ¦ñ:\x0003¾Ø´'Yg¾5Ñô<\x000b]ãhÀh\x0011ÝñFæO'	Ô4B\x0013¨åç\x0019l\x0016UELÿ\x0013\x001eg4øQ³\x0011ð¾;ªd?pBgJ\x0003
¢\x0004Ñ/s¼	O}
ã|k\x0004èy
\x001bêZ[\x001bpK\x000f=U2®èè~:±Ý9ô<\x0005<cC\x0000V\x000bÓÃ[¦£»Q{éxléÐó\x0014:Qå[A¢\x0003ó\x0004\x000eÍÌYè¸ØíÑØO\x0007NèL¹T\x0003\x001b\x00072f:j1Ó.-<¡ó4lì	9\x001eÇ&ÌËR£ÿ%9àÓJcã$§¦C{¯ç,µ(>\x0007t\x0014M\x0019g%òt\x0011âã\x0013&í\x001côÅ\x000fJ¸\x0016©%ï)°]èø\x0004i5\x001dMS¾gÐq)Bãl\x0007U\x0013²\x000fÍá³Ðy\x0000thò\x0003ùy\x0006H\x0005ï\x001c¯iàØ3\x0018iìÎÏÚKÆ´éü<Ae+é´WüR\\x0013cq»Û'd&9Ð\x0004{PYÊAe:¤¾¶ÐÁnGþn:¶½÷ÈÏS.r­â9\x001dTJÇf\x0000IË\x001dõ¾zÇGè¥\x0016æ,µôß\x0005.J£\x0005Ærý\x0018ôrÎñ*SçÓ1º¥§\x0014q\x0006äÌZ.âTK½·\x0017­o\x001d}wêåÀmn]5,7º¹lxÂ¥.õ[ñL7rBË-¨Õ2\x000f
ÕÔ
¤i,\x000c\x0015A¥¦\x001f¾!\x0001ó¿Ý}Zª Ýá¿=|øtÐ1'­Ö®5:çpÕP\x0019\x0018ÙFb¯\x00139ÿáâÍRüþå7où#$\x0000\x001a\x0012ô8Ìä¿\x001d\x000fëPËi
Iô¡\ãö¤Rv(c>\x0017\x0012Ô`2H"9z\x0011]¤»èåH\x0007tnÑ\x0015ËÛÅÂ·,ü\x0004\x0016\x0011ËMþÃb¼Ði¹\x00150=O¹+neÙ\x0015äUF\x0017\x0014\x001d9¥Icl\x001c¯($`t=\x0001Ì=,Þ$³ÈÎdEúçhî´A\x001d\x00037ÿ£\x001aåØ?ý[vsñÍ­uÚÜOûÉ»+öîo4SÜÒ\x001b)´×DU¾£©,4ºÉ½õÓYÅÎÓöûÌØË\lãV8£I5Çß|óÃ»ÿ:hûÝáÅí÷\x001fÖë9)Òsâ-\x0002\x0014¾A\x001fDéÙôú·~¸¼¸ù÷È¶_\x001c^{}Ù\x0011tb\x0012ÇÙ\x0011DFG\x000c³ÐA¦\x0006eó>!\x0016¥È¬§£³F5Ähä!\x001e<tC¥ÁûåZ)×ýF6¸@Ïd\x001e \x001b\x001eô8Î#øRXFC%xCá¡{N|\x001f\x000fs\x0014R \x001eô8ÌCÈ\x0003%\x0003D)÷O±¯@O(s'\x000f\x001b\x001b\x001e¤m<Ì\x0003mz|àX¶Xf\x0002Ä^Ié>\x001eÖ4ß\x001ey@ú\x0008v¹\x0001C
"iVðÐ½ãÇ>\x001eØ~\x000fñ=Ì1ém\Ì²ÊT\x000f'e¤éH\x000fÓ÷Gx\x001a\x001e\x0014ôó\x0010YCE¢\x001e\x0014«\x0011\x0007ò)³i8×+z\x001c§<ßy4&²÷p`yf\x0008h§¯*\x0017[\x001aq\x0006
\x0004ñåFÅåääÀE\x0005½\x0019ÆûhxÝl\x000ez|4RHÒ\x000ck\Â\x0012úe82Q¥°¦Þ/u¼è^&8ÛÉjoecÐ´é\x0007RÌ|ûñö§»ÃËû»ïî?ütøþÃ¯_îo?®gA~pÉþ:«\x0015otëÓ\x0013÷Tû^äíëó\x0017\x0017×\x0017ß]\_¾8|ùîýõùëÇY@Í\x0002&° *d&ü:K0ÐÛb\x0012¾ó)ö05	3\x0011\x0016Zæ\x0005z¬B¯Nï+\x001c~¿Z\x0008ØAÀ²\x0012³É}â \x001eÊ\x0010ze {?«Y¸	,\x0012ôåbÔY³hòÓgðrâ\x0008]\x001dû½,BÍ"L`ö\x00010	%ÞËLì\x0010z'Ø$¥ÒÙ8©9ß5¦,8\x0019@Y}ÐÎÚK£±Nzy¢hµ\x0017©,\x001f¤·
UÀÈþÇ¬®Q\x0019Zúa|3ËD)Ö&R2a øÊ~.\x0013_¸Ð\x000fÃ\R@"ëK\x0007¾û´A\x0017åÝÄ½\x001e\x001d¶><ýðM3æÝíý»/_6©¨;à[5tT¡²ÜqàK\x0007NÏ÷\x001de»ß__^¼ßSí\x0016üPãaüáLàkî¦óÅª\x0006¢]ðM
ß\x000cÂÚH\x00057á7<V\x0010C»{¥\x001a»ðÛ\x001a¿\x001dÅÏµ??Ä¬FCø«¡ã½\x0013Ò.üXãÇQüË"5:\x0004â\x0015uY>½
¼\x000b¾«á»ÑÕ)KÎÐÔt)1w2Ì.½þU3\x00106à÷5~??\x001c®Â&ë#(@?Ýò\x000f5þ0¼}­\¬:ªIàyX:l¯Æ\x0017þXãÃË\x00079R5\x001f\x000f¡\âu¯¿vÙÎÚ\x000f/ö³<±k
Ù3ÎÄ4å%$\x000355®\x001bY´e\x000b\x001c§,àvô£]ÌI¿Xb"mÍô]|)³Pøq|#pw£\x0019­Å\x0015C´nöÕ

\x0006ãi*#~s¼Ò~uûëÏ9#óòó§/ùðÓï6Dt\x0006Ä :N\x000cKD
DÄË\x0015WÂ¯Îß½¿ÊiWoÞùâO\x0017Ý\x00185&5b\x000eæð3\x001e¸@ïLGËÊò¡;®u©éYt\x000c
\x001dº=b:FÄu}0½½>BÇÖtì,:ÔàÂsfçð\x0003i <óqÝ©}#|\ÍÇMâc)+»\x0014\x0016;c]\x0004¸½î\x001dTøøõ}H8'æpº6\x000f¾ÉÞu'¤ð	50Oô,\x0018é@aV_ÉSØ¥ýÕù^ÎyO¬ùÄYë
äB ­7)tGm\x0002g}¯wNª9U5\x000f	H°}
'\x0017Ò´ è¯úÇKÜö\x0011j½é,wjm(IÁÖ¼àø\x001f×\x001d"3D¨q§z?¥lèrÏvæ\x001aÄ|ÊÁ	½!g#|\x001aªg9TK xl\x0007]\x001a,u\x000cÉ8È\x0007òî,¶n<ªåR­¬W\x001c°IpñéW\ãRõ4j}v¤d\x0013b©`ÒNrØÎõ*\x0002\x00085>HÏrBÖ\x0017B T]\x0012D¨;ü}\x00104V\x001b¦Yí\x0018y\x0010e¦²Ü[!ÌFp½K!>íaËM0¬\x0002\x001eÔh\x0011Yg{R9C\x001a\x0000³l\x0002j,39 ßk\x0011\x001f[lÜÂñ}|\x001a\x0000³L\x0002¢>\x000bÓ\x001có@¦\x0004§{\x0015Cl\x001a{\x0000³ìA\x0016bá¯c¬TÄ§x[&¦(óDA©iìe\x000fhø7Êr³\x0012e\x001bjW^F\x001fÄnN|Pc\x0010Ì4\x0010°\x000cÁÒ.Ì\x0013!##Ë0¬¨ÍÞG¨1\x0008fA\x0008Ç
¤=\x001b\x0004\x0003®}ñOFpíE$\x001d½«zó©§o®\x0011nNßï<=ÒÒz\x001e/ï½Q³)óB'S)RÈ7Ûâi¥Ú\x001c#µÉ¥5~,÷úöãíÿ|¸ûpOyÒ
\x000bÏDî8qÔ«Á	\x0005ðrOÁ\Çµ\x001eË½¾}}þo7\x0017×*}\x0005Ô,`K\x0006\x0018ÛåIrÅr

½\x0012½,LÍÂLø\x0016ÉL«#\x000b6jPæ\x0015v¶¯Pøýr)Áoküv\x001c?æòê<Ç»$\x000cIÞ\x001fkü8\x0003¿£´\x000eAô\x001dÈ¹ÆÎ&àj\x0002n¯mÒAFf·#¬¬ë9Å]\x0004|MÀO àø\x0005[Òµ(rÒ4j.X\x0013\x0013¶°\x0015©ÅdNc¾"s\x001aÌñlÜñx;
Ñ1÷°\x0013HôÒ\x0016KÄ!½C[²²s¿iÜá×Ð±oÞ
\x001cñª2xÓ÷ºv~\x0007Ó\x0018$3Á"¡%l\x000c_lxçØ	\x000bw²°s¶\x0013¼sH§]Õ\x0014%çþ,Çwßv³kë\x0004ëJÂs¦U\x001b¹ºthJªµ'¦¼Fhöv°·=\x0004\x0010H4¼´Q¢.ó@»\x0005òûhè¸UMØáÉÀÊÕDù8\*åå.ôj\x0014vò81µ3l­3Û.\x0012\x000fËz|hUItoÄwò\x0007Ìàá4\x0017h±gfÉÑÙã\x0004çØN\x0016Ø¸ozp\x0010Õ\x00148\x0011¦°X\x0006\x000ev;¥wòðí×ð3<¸J«j¡\x0011\x0014á¡ÓRêaG0û\x0018ÖVé\x0019Æ*Ø(©8À ·AÎÉ\x0010w¯zål;yÄÐð -¯a£«àLh(Q§°¥uÝ«é~äbëC6N0¹Þy®
vNÜKÙ´|YU8=Y`°YUô8as,3sÕN\x0011¨pZ*Þ­ö^\x001eÐò\x0010Xù(³*±%\x000få*µaó£\l¿\x0007Îø\x001e^YIBî![+\x001bCiwëi\x001fïå\x0001-\x0019ßC\x0019	t­µ@°R\x0013ü\x0003øã4vP¦B?=+6>ú6¿I2ÄµÉúõðöþáÓ\x001d\x0001]_\x0005j¬òÌDg8¸Ê
o´_TWeªPxwx{}óæþê»¯c3|]2|Õö2Ha®Y\x0018hËðaü«N\x001c
þþ\x0017¨ô\x001d¥`ME §¥¼74ÐYL\x0016q9Åz\x0015|o®ÞF\x001aÉ\x0010\x0014ãÚª¯8m·ïÙ°\x00114	\x0006\x0000YÍ:49\öTïüº4U¥ðúüðòêúUg\x0013\x0008v¨±Ã\x0018ö\x0014ÄjÁîÙ´ÚP\x001auo¤Ù\x000eè¦n×k·5v;øÚQªL²K\x000f\x0000µ>£¼÷^õù\x000eì®Æî\x0006±[\x001e\x001a°K\x0003\x001eM·å½ÏÅ\x001ejìa\x0018»^2ào¶\x0016ì\x0002½×½³\x001dzUuië\x0006á½[Ò¸)°\x001f×,Ø\x0004»10zÜÂpq¡¡\x000fV´
¤Í_õD]÷,õæj7/÷cëìn
Á\x0016KÃR¡ÉHâä\x0015ïNo\x000eÝéÍáÛO\x001b$;ti¸.ß\x0004¸v\x001c\x001f@dz<F{sþ¦ãRÝéu;½®ú\x0017F}Tp#Ô\x001e÷ÃV\x00118\x0012£!\x0019|»f=ç"\x0012ìØ+\x000bÚ
;6°ã\x0000ì`åR0ÄÀ\x0019-ëyàl
òµ^BY\x0005;è\x001avÐ#°KE\x000c
-[°\x0012ì¥F`÷
·Ân6d\x0018Ø*(a£	«YÉ,Ã¶Ú¬
uW¡viÃØÚKËbÆ\x001d7­[\x001f\x0002Ã¶Ý¡0+aßRUN\x001dÞSr>ß}þKÂ¶tú]~øËÝ/\x000f	âf¿Üå¹q\x001b`\x0013þx×g{Mrß]}þÂÒîw}uóýÅ«ô×;\x001d©)LæÒ]D*®v?¹+Ó]I©ýLlÍÄNa\x00124âcðg;$åI\x001dOA\x0004k"8\x0008uXð°^Lv·Z¢î*Dîgâj&n
\x0013'y6¤\x0011\x0016[\x0011¬äÙ´ê\x0015{ígâk&~
èÏS\x0013¹jM(S\x0013c¯Ìb?P\x0013	3 ÑÒ¯é¼k¹\x0014Ü(\x000e=UåÝÏ$ÖLâ\x0014&\x000eeÖ0¦S\x0018ë%\ºx~\x0002&å\x0008Ð\x0011lSËÒ7INÜIÙ\x0005ße¦ÄS|Òò¶PÑS¨\x0018\x0008(³_
Ê<ë´\x0000;WOû©4>^Oqò\x0012¸¼U=ãª|,ª®wO¾Iããõ\x0014'4\x000eI¶{4£ËÐWßSØO¥qòzÇäRDæ6Ù/úa©^P¡wºØO¥qózOVWæØ\x0013+VP\x0006(#¬c¯ d?ÆÏë9¤w\x001d=i\x000eY¼Ä^ª×ï±Iãçõ\x001cGoc.$ÎQ¤e9'L[	¾lç\x0018¸Jã\x001fõ\x0014\x0007i¼-ÊTJóøzT¦ª'qõÐx\x0015âUèÖ\ñ8\x0001TfA&hß+VßO¥=9Î9:X:ëÄ ÍÒ±J\x0011|
½
ýT\x001a·\x0002sÎ\x00188ùµ,C´I~\x0012\x000f	[9GÄ3·¸\x0015o´[¦bE¸W0³IãU`W1èDPÌS\x0019D¿Gæ=¸'±ÅÐx\x0015âU\x000cF%}:\x0008kþ(FÑ\x0015æ)ôÐ¸\x0015âVhÂ¶)\x001cÈó5Qú8ÓÕÙO¥9@Â\x0013$	*É(-¢_\x001aCà¯bL/QºJã!a¤¶èã\x0017gÅ\x0016óaØdÑöéTLs4S\x0006Ê^	±ãP¥ª×Äø\x0014\x000bÌ4ÎÞÌqö\7-Xr+÷J\x0019sæz,öSi½ãìÿ *mx³ÿ¨4ÎÞ<cgo\x001agoæ8{S&¥\x00002_»å{\x0008Ñz1¦×ºJãìÍ\x0014g\x000f<<?âê\x001b{\x0006ñ$W*¦qöf³w<úÅÝ~Þ)\x0012áÓ8ç§`Ò8H3ÇAþ!Llã\x001fí\x001cÿx<×;\x001a@)æ«Lì\x0016wí§ÒXb;Ç\x0012§¨ÅÊaXÚ­\x0001¦\x0013dO²y?öÊn%\x0006UY\x001e\x0013h©ðTõ½:ìýL\x001aKl§Xb ñlÖ¡6nE³±\x0010q=
ùýD\x001a;lçØaç¸0}\x0012ÃS-W0Ó'éÕÊìgÒa;Å\x000c
EZÛq\x0019pò(¡Ü£Fx-ß¹ì3W2´%Ó²\x000cä"&ÑKú+öDÎ÷3i<âQ \x0019_ä¤$|z"¹í{C¿wSÁÆ¥à\x001cì0OrtT:lÅ\x000ecÉä=Å¥06v\x0018'ÙaËC¬ÐÀeyÅ§ØóØNÌ	ÿ\x0010"\x0019Æ9¹¯?HcqN0üG\x0010idö¹X~xvõR*½¶½^XSæøñöðîÃí/V×\x001f«à©t"_×9jºÊaÑ+\x001du/St¬½{}~xwyþêÍ×¤6\x0004¹­Û!äb7\x0011\x0013@*.]l®ãQß\x0002îUíÒGð¾y¬ñãØF\x0017gø\x000etgLðçþ0åzÂ»à»\x001a¾\x001b}ý\x0010eÂsFdG~ý\x0014>NÆïkü~\x0014P/q¾áÚdÃe§
ôªê
ðC
?Âg%zý\x001ar\x000e^?
¨Zðã:a
øc?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9z\x0001v\x0005³ªËø_¿ýÓû«\x000fW_¿Ý_ßáU
¯öÃ«t_Èa®.¯Ïå±\x000f¼Á\x0013Âë\x001a^ï×\x001e³ªùYZbÒ(Á;î1kÆx¹´Â«¿þtmÿå8l\x001cÔ\x000b?¿{x\x000f\x0017\x000fGu(êOg×¯~¨w*àûTºB`\x0012K%ÁÖÒÙ2ÍÇäûøÉëãÿz¬x~~ïþô>Ùåÿs\x0003__5àDËÇ\x0010N _E\x001c\x001f)¯\x0016£Í9ó^\x001cøwÑ-Ö±\x0006 \x0002(\x0016¤%ë<\x000e`1»hào6-Æ)\x0017}0Ä\x001fÒ\x0004ÎBá(#·\x0007\x0007"6Ûb\x001c/©\x0001ãpîe2NPc²@T/\x000eü»¸í8\x001aÂ$\x001cîp¤Ä$S²
<Hì2\x000e\x001c¾Å8ÁãÒ öd\x0018\x001fÇNÙ=8\x0010ÿ\x0016ã(<¤\x0008'Í\x0005HÆñ±ì+·Ë:àcu \x0018QDcðBv¹\x000c¼­(Êï¤Á|þ ¢xÍ:à¸\x0019'¦È\x0013µç.8!¿Ýôâ KnñÉQÑ(ô­b6Îã¼2¿çKa-³lðÈ\x001aÇzåK\x000e,_í^h\x001c8rÓÊÑ(¸Ë8àeKìQ0YÇ'\x0015­´C±\x000fÕ~÷òC
NY\x0007\x0008¦+/èòâ>ð[´\x000e»¾\x0017x	Ùàµ²\x0006È\x0005%!<MnPÁ)áè{\x0005³Çñà	#\x001bÜ²±J\x0016Ïct(ðè \x001c{\x001e\x0019v­\x001fpÊ²Á1ke\x0014êá§õ\x000c<ìãò\x0010iÚÜ{\x0002\x001e¬À
Ùà ¯\Ö\x0014qêv:'\x0008¢\x000cÁÉ#½8àegåfóXâQÒ;^>Êìù\X­\x001a\s2O.\x001dG!G,ª!ûJ\x001a±çsá»jðÍ`Hs_À>\x0011M·/ö	{¾\x0017ª¨\x0006÷l\x0000#7Ôy":F4ä¢W0Ý\x0013¡bì¯Z¼³r\x000eÁ?Ya?'æÒ7<-DÜÃ\x0003®K5yC/¨ÿ\x001e-W\x000bäQ"·!ÚµÁó¨\x0016ï£ º\x0001ñbxr\x0008à\x0018³çðÂ"lÕ²Û±¤.ç2\x0002êÑ¦PCieº\x0010'îÁÁº1Ý²¹B.g\x001c7W¤¬z2ÏÍ\x0012Íºa5\x001b
¸®|-n8¦¸zv9CÔ~Ð
«Ù*ø\TW\x001aqvJ÷å°ª}·øxóåê\x001fÓÜÁõÑ7¿¾Í:Á³*Öáùd¨£Æ7\x0006Å¤È<ZJ;ÅN~<}ýß')Ñ±
4È\x001el\x0000ÒeZvÔ°óU¾u	zC\x0002 m'ÁX\x0013Ð °\x0001HÙ@Mc(o\x0000$":²\x0004\x0004kr²¢\x0006)u 	ñ\x0016Ý#êøp@\x0004\x0017\x0001HLs\x0008M@$Â\x0016\x000baÎ<2e<e|D°Ö\x0010\x0015 vó\x000c²\x0008[\x000c\x0019Æä¡12¥0Î¼çyâz7Ð °Á@\x0012\x0010}1mÈ)
ï\x00151i'\x0011P\x0013Ð °ÁBÏ\x001anQaÛrâQ>§}p\x0005¹É\x0011ßÄ3È%l0\x0010\x0004q\x001eÆ\x0001Bt}\x00176>.éiæ§\x0005hNØb!ôÆH$L¤=(Ló\x001bMDÃÂ\x0016¢<#Ù\x0008ò-\x000c¼P [OÓ[a\x0013Ñ0­°\x0008\x000e°Ü\x001d\x0003Gç¯¦(\x0007\x00046Ó³¾hXØB\x0004¦}f)E\x0006×È®z\x001fÎ0¯°\x0005G8</²RÍ!òÈlÐ@r\x001fÑ0³°HÂ\x00055\x0017jF|wxÜûh(\x001apëØåF©
@(ýUYÀDi'\x0013Ù\-&ÊjÝDÃäÂ:\x0008\x0010ßç´/ÜæcNBû(´'"EýõÝDÃôÂ\x0016\x001b9M\x0012¡\x0011»Rb6\x0016¶h×G\x001b]è7\x0000á+\x0018­k\x0015ÓB\x0013E/ù£ùi\x0010ÛD4¼Bo!*/\x0007@\x0014ó%\x0011ÒøÒì®E»~ÿë'ñéf.®¾½::»ù¯K\x0017\x000f\x001c\x0015\x0010h2bLSRÖCÑCx\x0008jf\x0015\x001d\x001fáÛò»w'ëD£ÀzHcÁS®Îr°±\x0000¯fË7¾µ\x0011"ëu\x001byë©oÉÁ\x001a¦Ë+Ç\x0003MàíG\x001aÅÖëH"HL¸"\x0012IÂû¢¢!\x0001Å7ö\x0011ëU"\x0007Ñ3Ý`]D]¨tX\x001c±¢ÞðÛFñõº,\x001cfÑæµm(ç \x0003\x000bU\x0004#f\x0002\x0016 Q|½ÍFYÌÅ\x0018°#Ûëæ#UÑö#"ìu$ðÚe¼£K\x0019#D\ñ\x0010ÞûÙFAö\x0006+å5{\x0010xE"+A¨KV
~ßv\x0004µ\x001bB¤³ÍËÜLÁJ7h¦¬\x001bþ~ýû×XyîÇê³«/×?Üß,úÉ`\x000cÔpá×9á\x0018\x0015+r*"yì£>;~sòú»Ó
DÙs·\x0010Á×Êæ@$èÆ«]w\x0015\x0000t\x0011eÏÝB\x0014%©I8­\x0014%­ñ©ü¤öÕ
²\x000b){î\x0016$\x001béU\x00114.3!\x0019ªe\x0000$ÙAtûÓ·ýÃÎ.$XÜ/a¡/®íÊÊê»`\x0017goJeÉÜã\x000fúzþ»\x001d½¾¸¶+¤ñJZE²8i\x0008\x000c "\x0016+,Hz²\x001fi¼ÖdÀ\x0007ò\x0010h|ÔQQÆ8`ö!Òº¥H	K\x0001q¡£T ©·Ñ\x001b·(¸
D\x0012\x0003¶ü(cµAÙA¢ÒO-Àií\JùkønØ¨\x0007c\x0008"Î)Ë\x0016\x0005eÙ|]UÐÄI\x0016&Çú\x0010s;z\x0019\x0016\x0010®P¶ßï[I"i!ògRgWÈD$\x0010\x0008DÖî[KhaÒ\x001cv\x0003S\x001a«¾\x001cÉ0\x0000[8O63Q\x001a Å\x000bøHpá\x0017TóúøÝ
.ö¬¦~úzûEÎÝà^_?ÜÜÞþ¶ø.\x0002·HJ\x0018XT¹0NÉ@\x0012øÝÌûõÉåéÙÙ_ÖYFw·\x0015\x0016T Ï×£<½çK¬ü¥¤ÍL9H\x0003ËèÖ¶Æ\x0002÷´\\x000b\x001b
"\x000e\x0010«Ø0b.·¾\x0019ft_[ñ*p¢ß(É\x0007¬-ãýLØ¿\x0019ftU[³Ô[\x0006Iªé3Q?y²ÌL&k3Ìè¶f\x00197¤å+%?ë9áø\x0015Í=0£\x000bÚ\x001aT\x0012\x000eè eBycÓú³\x0006ÑÕì0öÁå\x0017\x0001ß¢É2x÷!Ëx\x0008\x0019wÀ.ekÁ#Áe4½\x0006K«9\x001d\x001b¦gÛY&\x001eaÒ­^ùd\x0019|`\x0010t­7C\x000bnZæÕ@3¾\x001b®®`M!"öä8ªÛ\x0016B±mæ21iÆ\x001d+¶Ác<õ»â3\x0019e<áh"=uÀípÏ\x001a?t\x001c¦±(\x0002\x0012]¢±o­²U\x0012óý4ãw\x0015\x001aÑ¢ò2@oðY\x0017T+¡M³aüµüûÍo³w®çW÷\x001fn>'¡¥
\x001eQ G\^
K!\x0010T\x0011cÕÜõýùñÅw§¯QSh\x001dj|ëZ2\x0006uPrÈåàV¨Ò\x0017ÓNMa¼»¶@ï] $ÉÌGé¹h\x001a \x000c2áÑ±j|õÚB\x0005çU\x0016ÞR;JvhGC«JÌ\x0005Ì-Pù\o²Bñá®PLÛgß(½æÇ×Ý«j|'Üb*S\x001eÏ¤Sù5\x000f> .\x000e*îýù¤o³U(Q\x0019Ü¤)¥§#MCÁj\x00079\x0017Ê·P/«\x001b¨\x001c¸&±\x0004ITüT¸*ýmTø,L¶
¢\x0011\x001d±ív®öé-z\x000bNuÌÙXÝU\x000c?¡°j'\x0016\x0003MXÞHdIX>k0Rñ­LèÙÔl\x000bÖä¿\x0005\x000bïø\!\x0016¸ÀYz¾ì_ð\x001c 4aa1º§§uËªà24GPBtyÏê÷_ïæç¯G¯în>\x001fx¥Å\x001bc®LVåÆ4\x001cIsâÁÍ|¿·G¯ÎO_/>ÒV8£y\x0015G\x0007~éGex_ú£s\¿bìÌwÛ3:WqD 7D<c,½asVÆVÏj\x001d4££xÆaå\x001c'®¤!\x001aª:\x0000¸ë[\x000eá5\x001cT<\x0010Ùß*p|äºb_¼\x001d8£Ów
\x0007÷9µTETªÎßÊÆXRhnfo­àüúÏÞou²ªH\x0019¼¹ûº\x001cöÆÓÑæQË\x0006Jpg É1xQ.xsþv1oV¡P®j#Ô
\x0013Ãésé¦ï"\x000b\x0002`?	eª6À\x0016ÊÂ_>
ÉÈ6\x00114\x000b\x0008HêªÝV\x0012Ê\x000cm$ûQØ÷ø\x0012Ìé\x000fï
£Ô
\x000c­(Ùâ"5SãîsÄ\x000f{+ðBÑ;H(õ±DÐü\x0017 \x0011Tú\x0001$4^\x001cKtu7JÉ5lgÉ\x0007%D)!C,¼VLì7K¹Ûod14´Çc'E.:ðû\Ý8º	äwóøí_óõÛûëoËÅÁÐØ(Ãc\x0005làÎèç\x000fë·\x0017'ï\\39¬Wp¼)AÐäZ°f9ð
lÖán¥ÕkÆ	Ô\x0004WgéD\x0013\x0005=íF7\x0017nÇ\x001cÖkÆñ$`Õ@\¯H\x001e
¿Õüa½\x0015grX\x001fÆI\x001b*çîDy$ÀyÛd`gÞá¶ÓLÎêµo¥8Zh\x001dó\x000b\x001cÚí+çëç	¿/\x0005¼{¸¹½^.U087»á¥
1GæRðêN/¼Â¿»<=;Y®V¨°fJ\x0003Ö°²¤Û\x001b0R\x000f¹\x0013Q)®WÐÞÌÄXmX3å\x0001ëÖ2ÔK\x000faª3XcJÆ
jáµr;ÕLÀª±<_\x0003»Ù¥ t§»±Æª-XZQØ\x0003\x00000°eÇ\x0014ÌÂ\x001bø
ÖßãÕß~uK+þíÕýÝråiÀ¡`!ç«¤:x8Ì²VJª¹t\x0002@½=¾8_.òzDYV+HÖç-\x0018S\x000eZÔ \x0014º2~áó\x001dDúð¯¯¿ÿëç¹÷f\x0014§¼ºù\x0015´æãÄÀOÔ¡¤ûº´'\x000ex7íKÎJÇ§/Q8k\x0015iôì¼\x0001É\x0019Jåy4\x0018éÃX\x0017±Ür\x001fÒèõy\x000bRi ¤Á\x0019És\x000c;Û°Ø4zÞ\x0004W
A·\x001eÌçÑ­§\x0008Åx-w"^¢×§Ù:\x001e¥ì%\x0011)VØ(sçR\x001a=Go0R$^ç\x0010$&X*ªò2Ì¼çµ Þ7 	EQO
qd%\x000eû]kñj <Ànøn&l"åÒã\x0015Äÿ¬\x000fåüÎ¥4yøÜ²\x0014;\x0001©(õ
t%¤Þ4~oÜ\x0004Ê	RGÖBÒ\x0004ü¢Ts¯-LãF¦-Î=c+i®ÒÑå/g»ÏZÆ}C\x001bÎµ\x000eÞ\x000b	 Õ\x0014Y\x0015I\x0018½ïÓMZ60a³°ËLVòj¢ºa y¸n\x0001\x001aw\x000emùnú»Á\x001fØ²x\x0006b\x0014Jî;ã°\x0017Jµ­oeº>w¡àúÎi\x0000À3ÜâfÊwVþþ\x000feúe\x001a<\x001c}w÷ùïwp°Érip¡xJªÅ0¬	~º.¾;ýÃùëu¾à
¤¾áá\x0014cy\x0000Ç#Ä³]¶d$-¸n@²6ÁP~\x0004RÆnéÉ7Ú2Ò\x0015\3¢Ü\x0008 HÎ\x001a9\x000c;\x0008eÚD¹\x001de¤)¸f\x0015Cò
>Æj©8þ@qzmG\x0019é	®YEF}B	TA¤Õ#ÊôÇVàºU\x0002iüÄð¸V<o èf$¶¢\x0004×¬b9R T\¶
V1\Ü®æ\x0004Z¶¢D\x0004×¬b©\x000c"B.ª8OPÄhßFàúbñ¬\x0001Wª7Ö¬Igô.ËV±|àv»Hmd2\x001bÍí°ËX=ð0\x000bVtå*ÿh!FÎ\x0000RD~#Õ³Úo[YÆÊkv	t\x000c\x0005C'ò\x0015ÂY¾ G¸dô³U\x0003\x000f³h°K\x001e\x00131Ëú£ã*RãvxÜ`àY\x0004¿Ô 8ÊsFqOÓÝÊ2\x0016ç[aÁÎ«\x0015Sø\x000f§Hr¡qÇ'\x001a+á­°àq¤ö+\x0012t¹TR!;bêÜ\x001a\x000b\x000f¥	8\x0019ÃR"%r\x0012Sé9IÐ­,c·Ã,X\x001båz Q¨ÑY4e.UØ±&ònkëESEOp(jBG4³¨ÓÜv±´Û] tâú\x000b\x00174u\x0013x3\x0011Xú×Ï2Öu[q»RR\x000fjt¨×\x0014äg´\x0013½ÛÈ2\x0011u;ÌR*$?
è¤ª\x0012\x0002Kt8;½¬°¨põùûw#ø\x0007/¢$eÔ,%\x00194¤Å¥dé\\x0012ÁMËå.àÏ\x0017Q\x001enn\x000eaþôÇëûå\x001a\x0010¦FHåH\x000bL\x0019\x0005W£Y9óóöèÇå\x001a
gò@z\x0018Ç \x000c<Í¸H¯ØV`÷${ÙÙ
­8\x0017Ò8¸è\x000cÖgÉù¢þLyKk4]¡ÑîÅûoõpôîá\x001e§@=¿½~X<²!Y]¸T[ªÃ\x0010\x0011ëÁéR­§O#Gï./pèÓó³Ë%,on?ÔÅ2§¾\}ýº­8\x0004Õ\x001dt©È Ú(KÎÿÑå¾zsüöíGÿ
(ß#[d \x001a½\x0004$¹YGb¢ªÓ¡\x000b)_âZDÀÆÉ\x0014øzk\©Z©\x0012Ûþé?þüIÌú \x0017w¿Ý,9!\x0003ñ&wã\x0007¼WRd±0÷¼}yôâüõ»Ó%/ôëûëß>T+{0Óä?ÿ\x000f\x000f5·åáÈ\x0007~°3Xp=®¢é U¢l&¢È·)\x001cKB\x001a²\x0012\x000f3ºïÊOw\x0010e_Ôf#ÃCÒ£ô7\x0002\x001fÎ£ÇUµù;r¤ÍF¢ä\x0004T GQ°Q\x00191_ëJv\x0010å\x0004E\x000b\x0011\x0006c2Zè ¹å\x001fD»l\x0003mD:T||L`;ax\x001dÙjë·\x0013ñ½¼		¾\x0015\x0015®E#ùý\x0011\x001b	É\x0018¿\x0007®ÄMHÆäv°üÝhâ#U7ün!îA¢ëh\x001b§¾\x0006ì àTGJ|¸Ýâ\x001eÄ·Ò&$\x001bIú\x0002çyñÄ
ç\x000c{ÉèwY.§MHX#K?VfÒò¦ºT\x0019º\x0007ï¨m\x001fNñZ
<\x000eÆh®>\x000cvÛæ{jÛvc\x00195à©òýªmfäëjS²u\x001aïÏNxÄ]HtkmB\x00124Û=\x000e³\x0010®ô<¡Á×õ\x001dHtym;Þd)ªu¶ÔixÇïý¾#\x00040×þëÍ/sµ\x0014DÞ^}~ÿóbÉÆ\x001cLºH#¨`K)£yj\x000bÕm@÷\x001a~°Î4Ss·ÂdÎÆ(èÈQ\x0010pFSÌ¶\x0015¶0ÍTF\x001df2\x0010ñ(6äþY¥¸Àf¹°m3ÓL¹Ýì\x0004&¥\x0010	µ\x000býL Ð\x00075Sl·b(-ûÙPÒ±PÆRzòoÞk\x0011
Zûz8~-[Ê@\x0014Ç%h%\x001d9L£+ïÔ\x0000õå\x001f·æã·Ù­\x0007¿û\x001dîL\x000f·\x001bt§²7x£PêæÇÃ7Ì-*øÝÃÅéòl1}SaWú\x0016,5:u°üè\x0012ô}T?ýçýßf\x0013\x0015Ïïn¾\x001e}w³¦°pUa½y\x001b\x001cÅ¼\x0006k\x0013)õ7ç\x0013pDÀéÛ£ïN\x0017\x0014ÿºú¬¿ü:çº¸ûéæóR&Ç\x0018\x0008àLÎxÁó[´\x000b´Þ¼Ãz{tqþüôõR*§Âä¹Vp´a=L\x0017\x000c©\x0018j\x0017
×FÌ	\x0005m§¤¹\x000eÓØh¨fÚ9­èe\x0017\x00166UHâøöv7¿þãºiã1YòõèÔù¹(¥\x001e,`êµË\YÓa6£ôöèÔö¹hâZ'
$ 
±¤]&\x001d´AXgö\x0011åOÖBôXC\x001a]i>r>òs¼;òaÒd¤ôrÇÅ
|a%\x001bP×Mt!å|@\x0013R$Í
@²Tx/ýc: Ö<Øtëÿî?-îüÛÛe"\x00144 ïæ°B:\x000bAØfXyv¾\x0007\x0014g²nâtÝ¬ð`¡_NO8¼]R®\x0014¾\x001fk¼º9Á¹5 7ß®~þ<o \x00138ù\x0017;]\x000cªræ\x0007rç''J±'\x001cµ\x0013³9÷\x0013øýb§KE31ÏA\x001a«Á:¤îì¤Î\x001d\x0006O2òÊ´Ó|°ßþñ\x000f³Ð?¾;v£ç$2\x0019ÍíÌ\x0007
éç\x001b¤p®÷\x0006i¿Ö
\x000c·zÃ*r\x0014Òðn\x0017:Ì\x0004i+8wâêÃ·9ÍÛ\x0014täç«å¯%IáÈÃajøköPõLAÐ\x001fG7@
OÖmP*°lAõò,»\x0014²Ó¨¿j\x0018öo£Ò:#Á\x000c\x000eÙ*Jz(VqFùr\x000bÖoÑÿòól÷ÈÙÕ+¸m/_·]¬í\x000c·þÒÙ[\x0011¼]'ñÛc¸m/^·+QëÈ*Çk>bcÉnk\x001eå\x001büt
t\x0013Ð¨qd\x0015ÈzYn Ár/
Lsät|n\x0013Ð¨md\x001d¨\x0004!\x0001è¨îXE\x0004\x0016ÍÜÈ\x0006 QÓÈ&\x000b\x0005>ï\x0003Wfã([>ïçú\x001aF=#ë@8§è\x0006®%U\Q\x000fë|ß\x001e©\x0018n0Ðã\x0004fiñ\x0007Ó\®(ç\x00064ð´\x0003WyÒdDz\x0017UÒÇ\x0002W¸o}^;}+ÐD²oHxT¡â<¤Él\îÓÓÚÒu /w_~ù8ÛkûõèÕõç«_\x0010¼ÕÔt\x0004á³&=`\x0008ÊHôI@\x00102/bròúôøò¿"Æ~¿,6ÿ¾øùê\x000bÎ*YÞ÷D»pü1÷Ô©PÔ\x0006Ô\_=&h^üùø
+YÇIú­b\x0019KÛ{+©´FÂ\x001eTÜyä\x0016Ò~Û±fRl«X">ËTÎZ\[U´qIªxÊP¿ÙYÕ 7z\x0003õb\x0005OC&R\x0004 \x0002Év{\x0008¬ì®gõ±RâèÍù«W\x001d\x001a¿ýã×\x001e>ÌÇ·`ªO\x0007\x0014r|\x0011ÇJEø9¦\x000cÁfõb6\x0013%_-ÜÈ nnçÚ~±jìÓÕÍç$\x000fù·%
$èË<\x000f÷bQ\x001c	3\x001aTX<öêøôuÒü~\x001dl\¾±
ÌD\x0001¦Ùr¼`%ña?×ðR°K¦\x0005\x0008~­cñÃ©ùÀ>ÊÏöö~öK¾¹}xÿór\x0001`t\x0016\x0007ápëfÂe\x0010\x001c:y9#vtyôæìòÅ\x0017S¤ÆÉ»¯\x001fè««ow?/>\x0007È\x0010ñ)0ÞÅg4á«au©{7zWÇïÎ_¿^ìÞþçOw×ª~Í=»¹ïvóíèö\x001aG»Þ\~7åÚ	pêE~\)RµxîÙé	|²ÓwGg'8Úõâå®îß_É¿NX¸Én;5¤k3\x0014³Ì\x001a¾tó1\x001cm%¡ÙÈBýu
vñ,$¾!ÜmR§G\x001bQèév;
Ü´¹\x0004(ZtÕ]2lU\x0005P#
\x0013ÿhBáÚ \x000b
7x º?\x0010\x0013ÿØ¢"¿öaC\x001d£xn\x001dsUÕh#
½\x001a7 ÒÆ\x0006!c\x0016®c\x000b¶
°ÛXðÓâ\x001fÛYR(Ô°Â2Öëó}º.©iD¡ÑÛQ¤/\x0015GBÂ\x0015)ÊxÑËbÀ­\x0016×âb*xÈÕO\x000bû-¥F¦Û.X6lfÁöýÈ¥!4¹¥qE"Tª"m,VÂ?¶Û\x0005ü,\x001dÛX¢Êê\x0006«Âð¶ÖË\x0002£mq¹\x000e\x001fÈóÚ
:r9\x0011A¬éf`\x001bÿhb¡B,+,ã?Så¥\x001aYÀËÙ\x0016Oc4ò ¡tÃáo¤Þ¯*÷\x001aY`ÑÛ\x0016Wç¢Ä|Fp%]ggí	ß{.b,æZÖ.WSe\x0010¤eûÈ»r!íýFØÔä[\x000eF/U)÷ÊC³\x0013Ë£T¢ì]º»
-ÛÈ«¢Ä$\\x0007\x001ftA½(p\x0010Ã\x0008\x0005f(\@\x0019\x001eº[Á\x0012\x001c¾wÝâxÐô}¢Q\x001e\x001e/&¯[+F
ÝVÐäÿ­-~Î¸Rö®¸üf PÛÈ-Õ-¾\x0005Û-«r§Vb7Ñ\x001b[ây\x001aZ\\x000b
$q\x000e\x000eÝ?k6ùb\x0016Ý»"
±%\@
Éò\x0002ß\x001c­óEÎ²wµ`%zl\x000bè\x001eOhØCºûb,'tì¹±n0¶Dtpÿ õHLfP$rm÷çØt
²$\x001dKN¨ÂÒëYØMúe;ã6C\x001f ñÄX\x000cÍaKÇÄ\x001caú¥á
­©\x0005\x001f`,¹Â§ìÉîeÁ>sÑ´r½ä{+NI£ð?\x0014%ãº»§\x0005k&Ó/
×ùÇ´\x0019`±]Ìc1ì¼.&	@Ù[°u¯qð\x001f5ìÂ7ÏÎ$1}~i0L\x0011î\x0002Rzg6A®w+aC¶e:¬¨58\x0019eY¯'
Ñ½dP\x0018«-×\x0001_iJÅ\x000f¯Îº¢fÑ½~ñî~Ù\x000coã
®Q6\x001fH¾<E#;O\x0001\x0008Ç°M¦átÔBrÐ\x0000)ÝeS^ÕÇ\x0007×^ËàåU¶Ü`5.\x0014j!\x0000+p-\x0013øÁ\x0002#:wv\x0012I¿4S¯jª+áTÉ×\x0015\x001602Mi)Ô\x001a!Õ¤äN2BÙU½çÂÕ¢ZLê>#\x001d4½Üâ®¨}ïWÂû«jºÄâaP\x0014°J \x000eKã4¦é\x000cïCË¸&Ë\x0018GB58¥¢ùÿ©{»%»n#Ï÷Uê\x0005\ïÐU*Qå(~DTt÷£$¥ê¡Huå¶}5¯1o0¾»sé7'9@&6°¹×Þ\x000bÀj±çÄ	ÌQ¿\x0005d&\x0012ÿ,Õ£!¸Â Uu]©q¦1Í \x00138Yª9=ÇàÑêáÁ´·ëò\x0006¸\x001cTh³Éæüa´£gÉ¥¼w3À}Âó§\x0003i&H_¡\x000c¯\x000b&¾]Ï
¥Ò²:"ø\x0002G\x001aî2°È\x001eXA7è\x000b\x0014ÞcU×e\x0016ï$Ê\x0016+£ÈÊ8n\x0005j4±þ\x000fU×\x0015\x0012\x0000ù6ë\x000c«Õ@8Uú\x0012í¨ÉÃ{êº,áÍÄQw«sÔ:\x0002g\x000b\x0013\x001b¬R'îº¤`3«£=\x0013\x0005\x000f8\x0001¢µ\x0014\x0006cN%çé?ºÒBT3m,*$\x0004gË\x001a<M\x001aß\x001bu×££w\x0003àÔ¨I!c\x0018&fW5^
tçÍ@ÉÃñÍç\x001c-cúÎÒÂ¥\x0017}Xìü\x0007OP¿\x0000U\x001e®ïV½êãâh_ò iq°0Ê\x0004^|¸ló3Ï\x001eÓ5
&hW¢àÍ¤\x0019à\x001akÄqLC¹Á¥\x0018 \x000b¥Y\x0015·~UB`®ô$\x0015\x0007{\x0015mHìj\x0012
X(\x0017\x001fÏE®\x000e\x001b çÌ^õ}ä>¿_DÍ\x0017B{Oîn\x001fß|¼Ç
\x001eúÒÿÁ7×·ÁISÈaÇ6BÀ+dÎÇx\x0001Ç\x001cn'ö\x001cç8åÔÝÅ\x000f8Fj§µôäòâíõË·W¯¿¹ÿðÓÇ\x000f\x001f\x001eïÊ?|ÕÊ\x0008¯ÂÂ\x0006©_=1E/[ÈßoföD×\x0011¡øª%(\x0013@åP¥&QQsA?×_ýük­1T\x000e[ÃH:x$$#dð_éã\x0005¡ê¥*vç°Ñi@rÓj\x0010T\x0018	D£ñS	Ä\x001bÇ é\x001c\x0000Éu«Ap2ZæÀ)'!/Hào\x0004Q\x001däÈU+9À\x0007tZ\x0010¯òC\x0001Î\x0015\x000cBL\x0003 ¹¢qý¬¼\x0007 à°Eþ2Î3£\x001f&V¯æð6wtñ*+ãÂ`=\x0017rx+a\x00068²\x0014íê\x000f£$ªx¦õT\x001f\x0006»\x0016\x0010$äZêõ\x000bâsí$\x0004ã`R>\x00089\x0008Â2´«DÇ,R\x0006V\x0004<¢%IBéÛ\x0004§\x0006I¨{5ÃZé¼I$Ír\x0010\x001eà\x001d69#ëGIÈ3®ÿ::'ÀD³!ñ÷«sbôëÚÎê5\x0011Ôe\x0003_'ÒÐ\x001f\x000fD\x0012\x001e<Á,?»Ä*t1\x0004[mòÅ±\x000c´Oâ¨·a¹Õ$Aå\x0012Îö¹\x001eH¬±ìnòCù\x0000	
aXïøl\x0016Â5ÁÉØt
Ûyß\x0006+=$¤7´vM$V­ÇQ
ËýÓÈoôèð,ÕK\x0012b¾xÀÑÁY>´$Z\x0012\x0017]ûõ?ÿþî?ýC1É«ûT?¼aPi<EkZÓÌ\x0007\x0017"\x0004*ÂáàÔC\x0018¯®^¾8N±\x0017\x0008 ÈÛ\x00131\x0012y6é=aa½0à8!\x0001\x000cOjý\x000eûS4­°\x0007ÍÙi½(àÔj\x0004² \x0012-\x0008y\x001a°pôQBÌ*ãý\x0018¹¯j-\x0006\x0004 0 ,	Ù¸'¡Û¼\x0018ñ`lvb/\x00149A\x00017\x001bÞ\x001a2ÝJ\x0013\x0005ÇÌ°5ìàÖØ\x000bDN- ï\x000fßD°§\x0013BfÇs\x0002º1¾\x0008CNp`÷x^\x000e\x00194{\x0017¡%\x000e5Ê±ïúOp\x0018Cq8,8Àe\x000eO¥Oý\x001cûÿ\x0004Gp¹W\x0013-Íe¯Àá\x0015o\x000f°¼\x0003b1KFt÷\x0007_HG½¸{æü-®
âÂÚÈÈ¦\x001dBjOkãbý6\x0017¸x\x0005.x¦ÆÛWl:'ÉäK)ro"~9\x0015NøIºPÓN:¸¬¼Á1[<¥\x000fêsxRÔxxöºørÄø¬ËÅ0Àç\x0015\ÙÜGø+{¿®Pù\x000bø´¦\x0000'üsQÉI>×ðí«`älÀædLHqFæ\x000bqòûªöìv\x001e^\x001dI\x000fËC
ªå	OÉÓ¡Ï«:?¯°1GÒ\x0002;1²\x001f\x0002>ÅË'§ù|Ãç{ùD~-ÃÛ\x0007µ!jô\x0015FÍñéæøêÎã«­¦ã+<,eªñs\x0010þ\x001b²~F¾Oð5ÇCw\x001e\x000f-tÒ\x0004|àÏR¢Ù¥ÒæD'í$mVÏö­B]Ý4DÄ`vîdu¨JÂ_×ÈÉÝgÃkû\x000eoâKï\x000b¯à©7l[¬ Ìóî\x000föZ5\x001fÿväÚ/ÇÙ*+Qn{\x0010BsbDIÕªùö_OCÙ\x001aÊ®2>÷Jchm³h\x0013@)\x000e%M<ô1W2ùÉ¯gÂ\x000ewZ(IÅÀÀêr¸Ð}­5T\\x000f "gCc*§ÉPúP@·\x000eJêfKéÕTJÄsº	`YXL\x000f-©[+Ci1\x0001Õ¬\¿TJsÎ	Î¯Ë\x001bÝc\x001fGÑotÕ>µþø)m²æ
R¢\x000bRñ­	_9»©>ÙO&>.õ\x0001wû¸låS;\x0005i°Ëé!\x0008b 2TÎë·§ëË³ï.Þ\x001e¸·T,$-½\x0005\x000b'Ò<D\x0014ô\x001cÜfù9\x0013\x000ef	\x0017YþýßþõýÁuyõpûînùñPK\x001dr\x0011¥T\x0001®p*ò¦=±|usñíåëã,ûýÑ§X\x0014ÎB¦×U\x0015s\x0013£\x000bsR\x001e>ÝÁ\x000cÝi\x0016Þ/ìÁ±(!_)m° SAÚ¨ï4Ëí»¿üù¶kª·Ë\x001fo?/»X3Íò\x0001OÚyY¤¤£ä­;ü2\x0004Ûå\x0017o£ìå\x000cO¢(M;\x0017|ª¢¬2Îqôúpø\x0003­!ÙË
"qp&\x0007\x0011á~Ð¨\x0004~ô\x000e\x0007sT+H¾ÈoFñ¹s\x0004¼tôècIú+5ü}\x000e¹£,\x0016ìI\x000e\x0017Q^<ËD9òaîÚExÿà\x001e]ýd4{¸¿}öýíã\x0011\x0012ím\x0016Ï7
ì\x001c8Ki",3¬Qdï\x000fW\x0017×gß_¼=Dòó;ý}°þÉÃÇ¬Ã´¢Ë½\x0011\x0006;¾è¥
|\x0003	ÆÄÃof7/QéKÿøéQ~æ «Éï>¿ýô	Å:\x0017Æ&ÃdåàêaóÃ·"Ð»YðÊ\x001c¤y~ñú5êu\x001cZ
hï\x001c\x00062Ø£]uº\x000b¥rK\x00002\x0014)\x0003>è\x0002Ö\x0001}!M±\x0008\x000cZ.A2\x001agnê\x0014;XO¾:\x0004yp\x0013¯äÙß=+xðT%*àQ>÷¿\x0002\x0010§\x0017á²\x0018º?\x0010nï~\x0003Ðè\x001c~w÷ðp÷pÄIavî\x0013C!zA¹Ø`8\x0000sØì¥"3öÝåÍÍÕåMqTûÑ\x001f³Ít²qE\x001b°Y~÷\x000b°yG8\x0008\x0007ÊÖ³¹Íu±A¤AjzFG)raD6\x0007Q&\x0014<\x0000¶\x001853¯Ù|\x001fTýl\x0012Uc\x0013
ñì2³.¼PãÞ¥Cëñ¥@:`ôéÚW\x0001ºÝí,\x001d\x0008Ý\x0007Q'=ò\x001a-H\x0016\x0019nð\èÝtÒ6l¶MÜfÀ'º<³×%±T:\x0011à'à¨áª*Â5pxM£,,µ(7n¡%9I1ù]U³vªsí"·\\x001e¥\x0015|âHåbÎ	v6N
Ý\x0018bÝgu\Î¦uî¥H÷Kì;Ë.B¨\x0013\x001bï$_³~ºsýpa¾ÿj£\x001dN£A>fW'>ìÏã
_ìãC1\x001dvù&\x0013\x001edd<w¨µ\x0007Ï4×t~^EqÓ©/
ÌI|ÞM\x001e\x000fÓ=Óiö\x001c	ú¼ÁÒu(*¯yýb	\x0004L³÷LçÞsFçF'+g\x0017§\x000c1]¼ÆáNû_ÏgÍg;7\x001f\x000eÙ´yóYùóEÒPu
àâ;úq}óq}ßÇE5?*õF§âÔ<¥£"Ì-o£©¾û;ðæãÎ+Àqä
u-á©?\x001d\x0002Jz
ô'\x000cóÑ\x001bT\x0003§záBNx\x001b¡C\x001e¥\x0014ÁÑÚ	1é4BcõBÕû=¾ms6BïÙ\x0008\x001a\x0013Ï¥ª|\x0005ÒtÓ0jÖkælÞ³\x0001P¾/ú_âÓð¬=ÐbÓ\x0017£\x0011{o·Ø3¡èv«øå\x0018P#ßnÝ(ß¯?þå§w\x00073lO>þùÏw=\x0018{ÍUz:I±g_k$»\x000b«äB/Çwß]¾¹:PÚñà}Ý.\x001eÃ!ò(ìO¥B\x0013¸j,T/âØ_!5TÀ\x0005	?»ùg­-$¶pÄZ.Ð2gòñ¦öÖE»½B;»ySÖ\x0011`¹\x0001\x001c&p.+ráÑÙQâ8:²\x0007p
Ô¦\x0000Ë'ZG\x0012ÝÙk°\x001dç2\x0013xá@í×*­" M± ¼\x0006úæ¤×¢5Pz\x0000¢o\x0013×\x0012Ø<\x0010÷Û\x0011púîË5\x0004,ý¸Àåé&=oeõoé=U\x0004KCI;\x0001\x001c\x0000¸õKë\x0011µD9N	\x000c¥!°¸z`#â9vk·A´Ti\x0000ÿÏÏWp\x0007ÖÀy\x0017ú	à\x0013~\x0013W~TSëþ1\x0015ß¥¥Kòx)¡ MÿQHCnÒ¬Û\x0007\ñ¯1\x0005Iö\x0000ççÐg\x0008Ê¯EÀ8^ïv°7YàÿþÏÿõýÇ÷\x001f^f2`R³¶É3+¨#1P5c\x0012\x0006:\1söýËëÏÌ0¢©\x0011Í\x0000¢àW>\x0005fÔq æ¾+¬ÝD´5¢íGÔ»å\x000fy²_j
+«è\x000f\x0017t!º\x001aÑ
}hê£Ã\x0002\x001béCv¸TV»\x001e1Ôa\x00001PÖ 7NQ\x001d\x000fD\¨¬]\x0018kÄØh¹¸ViLaEêí²¥qv©ºq5â®:\x0019\x0011÷ª×mFK\x000fô
uzòN,gE\x001eª¾éâk³\x001c8Ï¥ê\x000cøBÖÖ5\x0014¾ìÄ}o´\x0011Ü[û\x0005ðÅ\x00047\x0010ëYÙ/\x001f~=ÂÝÑ.÷­YI³\x001f=Ä²¥_,ö~\x0003q?MÎ~yóü\x0018´ÉY]e¦\x0011MeæãÙ+@úÿðÇ\x000fË\x001eFÇH7<
ÿÝG\x000f\x0003ñ\x0007;9sÐ\x000e½={\x0005ÿý
þÃ\x001f_¾½9Mª\x001aR5@jLÉ\x0010
\x000eÍ%dÆéC«Ú©\x001bL=é\x001dù\x001e¢ti,:ª¶ËÄ¡ãÞ
ê\x001bP?\x0002\x001aIã\x0005@£<çË\x000eçä¬:X\x0015Þ
\x001a\x001aÐ0\x0000ÇH\x0002J bGº\x0005hl@ã\x0008¨RüD!¥Éh\x0001\x0014«gèÞ\x0010¶ uÍ©w#§Þ
É=",¶éq@mI\x0000\x001còìÝ Í¡w#Þ@z\x0000\x001a²\x0012'^GK\x0000¬ì\x0016çÞ5çÞ{ådyI%,©ÉKJeKØ6½Åir¦á4#Z\ÆÆfºÕ\x0014Y\x001aØ¤û·1RÛÚ¡\x0015u¸yE\x0015Ê\x0017ä\x0015åtû·à1ÒÆº\x0011Sj=-h É\x0015
\x0019Sòó>ÌÆº!C
a\x0014¥· Ý*XOËwz/·0O¾9õ~èÔxN+êU®\x0017Å«¿P¼¢bj÷Ü+\%Ø\x000fù¾»ýÛ±®\x0011OEKÊqÃ\x0012þ\x0017Në.·C~wñ¯Ç\x0002f"Ó5Ùþð¿Sd\x001cË§füÖ\x0006pd1£Y×Â\x001an¿\x0017í\x0004\x001cXÆÀ%U.Kiâ{\Rå\x0017[½ÖÁù\x001an¿\x0011í4\Î÷\x0018%HÛ8Áq½Yî[\x0007\x0017j¸ý&×\x0013pÑ+#y@s^ øû¬Ue\x0010ýÑGéÞpn©6Ê\x000eRÛ2]°K'åþõLî5Q=ÿøáóÇ\x000f?Ý½?òÀ #uÈI
<Ô!$8\x001a\x001a\x0007íÉó/Þ¼|ñôòú4ªùÔ\x0000\x001fÕká©b\x000eø(Óâ¢\x000e/a\x001d®\x0006t½AÍ'PËï\x0000H\x0001#Þ\x001a¦\x0001C
\x0018z\x0001§6µ[YêPÇË+«ÌòÅ/vóñK Naå¤0Ü½\x0013¢<ìÒÖ\x0003Ö=ê¢É\x0002­$ä{+l;Íz;ÂX^A}ð\x0008w\x00116Dv\x0012ë³Ü{Ö *\x0017Á«ó4ÒzP7ºÐós´Tf\x0018 â\x0007U\x000cc[ÒáN¶\x000eBÓ\x0010nBA:`p}\x0016(Ë	i\x0005õÁ\d\x000fj\x000cµêµÔ\x0018¢Æ¢ ¹NH±PÂÁ§.¾æ\x0018«ÞsV:7¾á}ÏQZQJ ñ\x0007\x0013»*I\x0004Ô¶\x0013Ð{MEë\x0002\x0007Âä3b4)Î¹T3\x0007h/l{¿°ºu\x0005,\x0018p%ÂÒp­ôÂ­n\x0005!Ü:÷\x0002{0c_\x0004öÀxöäýíc/oÊzKïà2ØHmë8²º³Ìþ#t\x0015Ð\x0000èÙë\x0017ø\x000ew5Ö¬qÕÃ>W
H§ù-	®Kû·\xKê­«Çí\x0018q\x001d­7¨A:¼À\x0015Üòs¤¨ÃË¹Å\x0004ùJÚ önQA|ÓØòã=\x0010@Dê\x0011iâaî\x0011¤|£·a!×\x001dh'¡L
eÖC)\x001a\x0004\x0006PZ\x0013|cÍ=ñàª­5T\
å¥ò5\x0019QýÓQ\x000f#µ\x0015yÓöRôAI_CI¿J
2ÒáÀ\x001cjg4¬Ý«äÁ\x0017­uT;ÿT­;NEWÔë#I£¡\x0014(u.d\2IcÿÔôMÀ\x001f¤b°jÐüÉþi·ëYö$¾\x000cåhc\x000e¦¯._s§ðI:ÙÐÉNº¢Õ\x0015r\x0005{¢st'÷Æê¦m=jèT\x0017\x0012r¾2hßz\x001c¬bé=_\x0010vZO§\x001b:ÝG\x0007GÒÑÚiSè4\x001bZf
Ð	¿wé?ø¦®Ì\x0005gðìñþýû»_\x0015þa7xnQW²ÒÇ-\x001a®5j¥>\x0012<Á³·W××7Ï	°0¦©1Í[L[cÚ\x0011LÃRá2°ÌXôÚ`½Wö`\x000bE\x001f¦l>ºìÿê\x0006î¬,4¨AP®\x0008ÜëáöÀNÌf5eÿr\x001a¼Üt-ã¦À¾Í­n®¡t\x0003Î ÍN.Ø§çÇ,ìì¨|\x0003ÌÀ\x0006{SÆ3ös¦:FWâé,\x0011!j`¹6ì\x001fäÔÍæÔ\x0003S\x001ag\\x0003'ÜE!N*;\x0004£\x0019ç\x000f¬n(¸Böv\x0007ÖÝHr\x0014ËÏÃ¿ÌQPó\x000b*e\x000b*\x0007@!\x0008¤\x0018ð7¶¨±È\x000e\x0007§;ôî$Þ\x0012¨\x0016ý àcó`fÌÂÊsjEwÄM¤1iÚ\x0003oúO¼òÁòý	ÂGZO0KÄéõBË|\x001f¨k?¼ëÿð\x0000ê(âU\x0002ôÒÅSÇ¦OÕ;Ó ¾ýð¾ÿÃ+\x00054ÉÁÅüá}T<\x0014%yK/C\x0019\x000605\x0016b¿ð¤à\x001d·ý{çüüW­iR\x0003¦IzÏ%\x00062
.y¨'ß¨\x000ev5­\x0005µûÑ§ÍÑçc)Ñ»üùýý\x0011A\x0015®RÌ½\x0012çT|+Ù·Ã©ovæ[*Ê»|v}õz\x0005®Ét\x001f\x0019ÎA§9+`á#IkÄ\x00138¥0fk4Ûf¸Á^+Ï
ö.2ñ¤)FïF5ZìC\x000b\x0002Çg&´ÀWþÈÎ)m7\x0002¶/ì,öÜ½ÿÃÅýr%C\x001e¹D,³Y¸\x0003'Q\x001d~µ}ry}vqu¬Aî\x0017óË½bþÓl¨õK3\x0013Z\x0014<ÖÀê·Ãõh®Fs}h8[GîNA\x000ejË	\x00045Xì\x0003\x0003GF3Cpø I\x001dJ2\ÛqØ\x000fWÝ[ä~õ4\x001d\x0002åÒ\x001b\x001eÊC\x0013z¸b5]óMeßGÅÁ3&zÀUÕäÐ:ÄbuÕÁú£\x000e:ßÐù>:\x001dÙ»âè\x0002ÇÊ¦§Á\x0008s¸a-Ý®X[|!£{Nç\x001e\x0014ô¡dRª\x0008ïö\x001aßi§è\x001a#gû¬ö\x0006E \x0013\x001dÊD¢ã6\x000c-¿lÜOáÄ½¬ùõíÃÃ²g\x0012û/*º´\x0007£ð\x001fÞ:\¹p}qssD^Ál
f;À¬Ö¬[
@¬P^³£<øh³\x001a,Ö`±\x0007¬È]K\x0015K1´ç»,\x0015¯\x0003«Ôâþ\x0013û)²ÝóºÛ@d\x0008|C3û-}dÍÉ®5Õ5êÒe\\x0006ÚeÑ\x001dt\x000bkÉT³ýUÏþw8½0§	tP¹&\x001d®²´ý}\x0000k¶¿êÙÿø\x001eÂ·mÇý¨âY1ñ`\x0011åj2ßù.2ïk\x000cn2ÀxûÇ/\x000ek¹*¦EÖsam\x0004m°\x0018dÊT(rjÁªÔYÌ©³Õ`à¹±3cÏ*\x0011(¾@]HsøÁm%Yó)u×§\x0004\x0003s¸\x0012B·ê\x0011OÏu¸^c\x001dilé±eÞs÷
%©ð´f¥lÆÙfÙm\x0016\x001c+\x0000À×\x000c¬;o]!\x0007kt×¹fÍ\Ï¡\x0006å\x0015pf\x0004Ù2WF¦Ê\x00012)ö\x000cø\x0003\x000c2^½¿ýó\x001eÏoï\x001f>¾`¡:
\x0013ÄNmÇ)\x0005z{	\x0003xu}ñS\x001eÏ!\x0000::F@ì×GT\x001fÙG'\x000b]´er\x001cWÔÃ\x0001nÜÀ\x0008^¬ñb'³Ô¨°þÕÒLÈò$\x0014ts\x0018\x0006ðªÒC_­:ø\x000cvFfm7¸W\x0016<>\x0000úr¯¤Ó
î¥sIs,3\é¼7Ær\x0004Ï6x¶óãbY=á\x0019Åbñ¥îÁû¦4w\x0004Ï5xî¿
Ú\x000b¦ìþ+ù«ÛÏïþð\x000e»?íI¡\x0003\x0002X6 .©7\x0017\x000eê0\x0001å«7øÏg/× \x001aÕ\x000c¢\x001aª}\x0017Îù¨9Ñ!.=£tºÔ¦SÍ¤ØWJú\x0006ÔL1\x0015¶ô0µ
U¨½ê\x001c\x000cÕþø5rMv(\x0018ÇdÇ³\\x0013+Zu0¼J E#é\x0014¥15¥ÙoëY#âT¾»GU.ª\x001f\x0017¬
®\x0016\x0012c« ¥Þ?JºÍÄ~J3ÿÉ¯:GeNJI	¡WHo\x000ev0`1ÌÕË\x0017Ç*uôþÔm¶ó4÷,íne^µçº
©\x000f.ÝZ´ª<LY\x001evMó@O!¼¤eã`ÐêÃu°§ÙöÅÃe\x0016\x000f¿úõ·ÛOî0\x001aLÚ8ËY'm`Ý\x000cµáå§´ã"«¿Ù4\x0018²°]=uñúõ%ÆI"çX'£ÞÓ_jB¼ºÏ¢\x0010`f.\x001e~¾û°\ûÍ ¬¤òÎ¹ä\x0015\x0002j\x000e\íáY2ÙÔ\eQ³g/\x0015\x0003êý(V/Úó: ü*E&ùÓ§Ò\x0012znÔËS\x000b»¡}
½ß¶×\x0001\x001dC 7
|BÈ%P^\x001a4âDÜ`¡Ýc\x0016¶e^5DY´D$ôà¥;nÞIò\x00045`ì\x0005\x0014
ß«\x0010P\x001bÁ}â\x0004o\x000f&Ûz\x0000­\x0001í#4iÀMVÚ\x0000\x0003\x0013@ÓP ©ý\x000bm¬~Àf\x0005Uç\x0012\x001a\x001b5\x0015ºiÕ¿y°\x0015\x0002\x0013 Y8A+\x0008ò{ùgøµMþ-Í9\x0001P\x001cuòþXõ\x0003V®ú\x0012°¹\V\x0010¬<Xþ°»T§'\x00003O®\x0006\x0018¹¿TÖ¤R BÌÃ\x0015%°Añ¹\x0006Q½à\x000evá\x0016ÚüzYMÃjXgõ8\x0000DGX\x00157±+q°ú¶Õ5¬nÕ*¾AÝ¡ôÇ½A¬+»YëPØ7H\x0007«ÓçÑ\x0010+\x0004\x0000\x0019ÕÑU\x001cQ\x000f§g{Q¥Nr<ð:	Õæ:\x0018pR¤\x00013¶½¬±aC¬ç.©\x0008¡\x001cLaxÇ#Ü¾òè\x0018«n¶\x001eÛ\x0002pq£lVÀÉf\x0015®À´®Ú-d(W³Úýµ{Ûõø|<\x0000ÌE¹i>\x001e\x0015»:¡yVßa%·i:ÞI*ÙPÉ.*KSû\äxÙ	.ptSáÇÔ~-\x0012{\x0017³'÷w>rÃ@Y/(j\x0004ßnÁ\x0004Sï{ð\x0007Ã×gO®.¿;Ö£ öGÅ¨¦­|\x0005æûÄ+#MHßÔS®\x0016îeÇÑ~SÐä$`\x0019\x000fæ$¯ñ­ýöñìúããýI'øÆ.é:\x0011íy®\x0005H\x000bEy³d×øÌ~ñöìúåÛ«Csý
NhpÂj\x001cl½\x0007Ü\x0019\oöpï/å~*Ú\x0001rú\x0012O¸^É\x0003WÐDH§ð\x001f\x0013Ü3¤(á4M¨õ\x0004þàz Øw\x001f?¼[Ñ÷¥¥¥·»¬à£Y®ßhÕ¢qýÝË\x0017ßÇ#l±fýlGKg\®·
"RßºW&\x001e\x001c¸®¤·\x0013Ôýx8ZF?§BbÇ\x0012ÒûÅÛ\x0013èæAr\x0013\x0006j|R\x0003®áX/Ñ\x0000,Eã\x0019\x0010s\x0005\x0001_U¨ûByî\x001eUB®&U²\x001ep¯\x0006ûI©Án\x0001Þ><üó\x001fGî X\x000fÆõòÛ>rôá£tË\x001bðé\x0005ÜÛÐ.tÓi+¹\x001a\x0011Usw\x001bé|3¤a%¡É1=Á\x001a©f¾kG~)paLê¨ÊµD.°p½OÇ\x0001ÂýÇ\x0011L]cê1Ì cé£'\x001dJ\x0017\x0011f\x0007¿r\x0007¦©1Í ¦·4¿.÷-äÏÖ c*7»¾Æôci<!²uÜP,ÛuÒ\x001e4:«1Uhö&þ×±Ýé%
¨ÿ¥¨\x001dw§ñrx=­Þ;D°÷kÌ\x001eá^¸\x0001|,öDçt\x0012Ä¤ta\x0017öðDÞ}ÑÞ\x0011i*@àFµÍÐ»÷gÇK,!b§¦\x001f\x001fòÇ\x00068VÃ÷Ú\x001eþØ\`y\x0004J5Pª\x00174<ëj%*Rö a\\x0012úE«ÿ\x000c\x000c\x000eç·\x000fïï?¤¾z|ÜMÿ\x00162Ü>¾ÿü×·÷\x001f>ßýáâCâÁ:\x0010ãr!\x0012V¯\x001b\x001cí¨ÎTiÞ;×ÂËÅÛë7x}qõâÍå\x001f.^\x0000Üóë«\x0017Íö
\x001a\x0018)÷ß\x0014
Ö;ü÷DÃ2[Õ¿lÞç\x0001\x0008àâlÀ<eb3Ø<lélí¯\x000fïÂû\x0007²\x001fÍÛ\x0013Ü
o>~J½õ'\x0019]8\x0004\x0019ý\x000e\x001b\x0001Ñ¢ÎsHÒi¬_ ')¸3Þ¼|½Ørß°âPúaVTûMâ<j\x0001am\U*k\x0014Ì0[ÂæS<
Ëh\x0008ë°4#Á¢°jf²æQò£¬Þ\x0013*¾EFB5lÊÏù0kÌñ,ÂJ\x001c`S<aÙnOÀ
eëGÔü\x0007i<ôc\x0006ÖgO¹ýõ·µ\x000c¯11G¼ÔçS*¾\x0013s(£´¾`Îý^¯ñ/üþâù«\x0015ÈªFVÃÈ\x001eV\x0002^BP0-³C53DÚ--s?²®õ0r\x000cY:\x0007'*¤\x0007Ê´Ê\x000e+ìÓ*/ZÛ~b[\x0013ÛQb\x00086èÜÁm\x0011)\x0013p4´åÌÅ\x0006Ä®&vã;Yäô\x0014 ÃmN_4ÍÈk¼á"û\x001aÙ\x000f/2V ,=B\x0017Æ\x000c\x001dy]¿ì\x0006È¡F\x000eãûÂç÷\x000c@V\x0002úhcð*c×VÈ±FÃÈ\x0004IÄ\x0001·Ï\x001c
 ¹yo´BÙ(adG¢V\x001eûø°°%1[l¼MÌJmvüdëH=	ü;9\x000b\x0001Ì.à¥\x0005%¾\x001bff±á:7D\x000e»\x0012\x001d\x0016:3CD,é\x0000ú`xoÍ\x000e l\\x001cö%ØMÑ[PIP\x0016d£á\x001dW?lÀÜ8\x00139ìM\x000cì
­\x0006Ü÷éº!±\x0014exãbù~æÆÈa¢aq}öÙ\x0001Bú ó~Öö³\x000ff»ýÜø\x00139ìP¹úÉG\x001f5¶î§uN\x001cYÛíìFcå°yF
ì÷Fjx"æÔ¾Ë(yfÕØg5lµÅn(Í3ioøÀûÙ-FúýÌ}VÃö\x0019¨mÞÏ\x001e..!cXDÈÒlfêTc6Ô°ÙÀ¡©t\x0004­Ko\x0005Ù;rÝøÀ¶\x0015³n¶\x001eÞ\x001a\x0006\x000b>ò*[ÁÖYköØ\x0002±\x0019rã\x0005õ°\x0017ÄU9wáq~IÞÌÚzÎ]\x0004?oèX#¢læ$%PÄHÒûóÍý_nÓ¸ºUÀoTp	Ä\x0002ê|\x0007ô\x000c\x001dìã\x000e%¿Mß\ýp±8Ä®¢V5µ¡Ö¹Â  ÒoE\x0011S/`\x0001·ÄÖ5¶À6\x0014Ú!¶ÀâÐ\x001duÁ>n¡û¨MMmf¨]Jí\x0007l(ÍéW¸©`\x001c¡m\J\x001dPÛÚNPÃÝÕej°\x001fò1=\x000b¦Á6¤v5µ \x000b\x000bï\x0010f %l¥8'c6Ý"¾Æö3ØIT c;¬ËÎØÑó\x001eÑ[b\x001a;L`c5>\x0011\x0011ð¦°­%\x001d?\x001e~ôaÇ\x001a;Î`\x001f
¨À\x0013\x0019[ðj\x0017=õ-°wwñäjÄ8·Â6UJ849q'­¼Üò¸Oïãn]äÄÙFd\x0001¥ÅLSÎ:ê(5Çs5}Ü\x0013^\x0012\x0005Và\x001b1=sL»[®wã%ådEN\oU¸w¼ÞîïÆOÊ	G£¥<åô¼Á)g9
éù
 Èöq7RN¸Ê4Heî\x0018wûÄñ>Ùr4RN¸JSD¹=Ø\x001aX\x000fV\x001b\x000b\x0015iµå§²qrÂW*½Û%Qð\x0017¶![ïM`ã*å¯TAçÑxøô\x0002¾2S\x0007Q^\x0005N\{û°\x001bW)'|%]ÐÖ\x000b¥Î×H¡ù¶\x001e1-°\x0019¶j\¥qÁR®\x001dy¾(àj+^m\x00176§Tã)Õ§TÖe\x00198\îÔ_Ï¤.Ë-¶\îö:9ã)y(6¾Æ¸sZn/8ånÍq j\x001c¥p*´;DØç\x001cN,ï^^Uã(Õ£!JÇWÑ4¢"sóu\x0001Ç{lÈÝ8J5ã(#
¹É6Ðäõ¢ì\x0013o¶<«T\x0013®RcÓ\x001c­·
(e¸KUM°nÃË°j\¥p`08
\x001fµGË¹9o\x0019Ù0 R¯T\x0013¾\x0012î\x0003å	]ê|Ñ\x0001nkx-¯ÃªqjÂYjãs\x0000=JÌ4ïèQzÃs©\x001bo©'¼¥v"KB\x0002·P(\x0011"¯·^¬\x001a\x001bánÜ¥pIö7ÎU¥õÅè°¡»Ô»Ô\x0013î\x00125$M(Ï½÷·´å¹wC©Ûôë¿ÔÞ\x0015{"4Å°*Í¡ËË½å=^7îRO¸Km
¿8\x0005Þ#^1´P\x001bÚ@ÝøJ=á+QiBÁ\x0000a¡çH\x0014û¢Ò-}¥n|¥ñ^dhËq Üù©:ª
/9ºñzÂO\x001a)9.	AæªY,\x000bp¼ÖrËW\x001cÝøI=ã'Y\x000f\x001c÷Î\x0005´¸Þ\º\x0013eÚÛ4þÆÌøè9
øLÉ{;\x0014ûw¢D§»ñ7fÂß\x0018C\x000f¸½c)yÁq\x0017´¿7]ïÆß	c\x00145\x0014£\x0001´\\x0012¥Ò\x000cÀl\x0003ÅûÛ4þÆLø\x001b,\x0015ä'M)o¨j\x0005Âñ«i\x001fü&\x001c\x000evÓý\x000c®¾ø Ö;Ò¨¸¥7Ï1\x0013>\x0007ÅÔc\x0003¶ØôÖÛpjÍ{½åþn|ð9Æb\x0007óÕ!ï\x0013¡{Ëtiì·°ßÆ\x0007êÌAE\x001c4´åò°I¢\x0006\x0010îì ¯*õQëé?ÿÏç¤Éöæ»û÷k\x0017Ýæ¡\x0000`õ$Ä³{gÓ\x0013[üúâìéË7I¯íÍ÷WKc+~Uó«i~\x001b²z\x0013Zm*ß\x001f "½ËÃ]íD4Ûÿ\x000btý\x000bôô/01\x000b\x000bâ\x0017H!nvGüFoÂ©\x0010±ÿ\x0017ú\x0017Ù_ºTxn¥à\x0000F)¾0\x001bl\x0006Úø\x0017Øú\x0017Øéo)\x0016:\x0005ÂáÄìZÉÒ\x001b¢Ìjà\x0007øú\x0007øé\x001f ¯²Âr.Q\x0019.K7Þð±ý¿ Ö¿ No¢\x0010¹pÓ@ôNucªt/\x0018{êi¥û\x0017ÈÖNÛRí\x000c'\x0004L,\x0001\x000cüòiÜæ\x001fA6¶HN\x001b£ª\x0014ÕÀ©vü\x0013$ÿS)¤þ_ÐØ"9mPkÇçèÇ(£{\x000b\x0010o#¡¶öhÕc®¯KÄ\x0001ªæ\x001fPúþ¸^ÁLuôÿÆ\x0018Éik¤¼Â
÷ô\x0013P\x0008Þ\x001bÓpô\x0013NfôúBh~Bþ\x0008Ze¡äü\x0015L.òÖÿ×}êÝÔ×åä?!`õç¤¹ÐÈ\x0005Éæ(õÈoû\x0013\x001a·¬¦ý²\x0014c£¤*IÙ:ît´[\x0005Ý8\x0005=í\x0014DðÂ ¨=Zq³¦[GwºO§}°
7\x000fÿ\x0002\x000bí|Ð»°ùOhöÞG¨ã\x001bx\x001f\dQ-p"uÒÿ\x0013\x001aªgmj¥ïÐHÇ^Á\x000boø\x0017è­ýn\x0002<=\x001dáÁµû/ð'PÁ¦/\x0011Gx¦9
fö(\x0004 ä7\x0008lB\x000b¹\x0006Ò\x0019®ÿÑá¿à¾ü§\x001f^ugÆ?¼/(G¡áµYP_¹Ýµ?HÝ\x000e\\x0017öGÜâw\x0008±»÷\x00184P\x000bï='ZÔ:~{	\x0018\x0015w	Ç³\x001fîúø+üW·÷ïßÿòñqÝ\x000f°¨J¯ZÊð£­.Í`£î¨·g?\=}ù\x001c~À««ëëï_.ÉV?@Õ?@Mþ\x0000\x0013#J¥\x001f\x0000§Úð\x000fàrfø\x0000G½ÃÈ\x000fÐõ\x000fÐ³_@û<¯
;\x0006a7%~8Ý¥aðø«Ñ\x0008¿©ùÍ,?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=n>£\x0018vÖBïî).ºGõ¤\x0012Ï\x0017Ý£\x001a\y^\x000fvòütwõ
\x0005±\x000fë¢W¿BÕ¿BáW§Þ\x0007\x0013//2^	¾ù\x001e3ç¿ÁÔ¿Áá7H3`òo\x0008\x00134¨^É¿Á\x001e»Rý\x000fx«Äk\x0003ï§g\x0018(bNã6\x001eçlþüÛWü\x001d\x0003ï¾WDÜRJ\x0003ë\x0005À¸Ño\x001dtQøÏ_\½|ó\x0016\x0002&Â¯\x000f\x001aü-|u1æ\x001fÿ
.^¯qiN³iÏy6Áwã£y¶}¿á°\x0011uKÓïêæ·O_»\x0017Þã½'?(\x0015XÎ\x0005±]øS¾êí»«\x001fOÓBK;kg\x0011\x0000-m\x001c~ùB»\x000eV,ûªDé«Â\x0013úìñþé~`Kà<ø`hK<§	\x0016Üï¯ÅÑÈ\x000b\x000fæ³»ëw×Ç·C\x001e¶Z¥KpÄm^ßW÷ßþÞ¿¸óÄÊæÌZºD\x0000{Sw¼MöÕõû\x000fa_Ìßóÿ\x0016·Õ{yöå1ï\x0000!MÜ|ûôð9/cð"·é\x0007mcl[8¢­Ë7ø«D©óºz{óªê\x0012}öúîà÷6¿ü»Q\x000fá·
êöËÓCCþ¼ÿülñÃãÏGÙ<\x0016¶§Y\x0010ÁD\x001bE\x0019±:VÍèPz2Ûíëw71îxyýê]2¹7w¯_õ!æÁ\x0015\x0013:½)&D¡èI78ÈÏ]\x0011'[¯GAM!\x001aÍP0&XúÂÁIPhK±òZÄxàô\x0014¢Õ¹Ø\x0010WQP\x000bmpJ\x0015ÄR&´\x00161þT3èsÖ\x0010\x0011->\x0013fÄ<ö\x000f?´:\x0013aÜ/vî;ì##a)\x0012ßÙóVÜÑ¯EnËM!âíÎ\x0015x!^4,\x001fèBü_?Y÷¿ý×ûx7NÿAÇ«/ßòµg?W\x0010\x0010ã¢ta\x0008\x001aË¦R\x0004-5\x0019AÔsn¹¢y~õúýÁ
z
Ð»Ë¨o6ëÅ&y¼#h>H°Y`!ÞxI5¢2zNK_Um/3\x0019­\x001aÜÎÑ½u@Ê\x001aRCF\x0013?+fÒÈh²Pü¬ZÂzFU3ª	FÏ{ÏX/\x0011Ò\x0016\x001b#ËSÅ
H]CêqÈÜ¨ Éù\&÷\x0012¤Ðr=¤©!Í÷º%Ë-¢lKüÃ(«V¹\x001d*²\x001aW\x0016Æ\ãWW~=+P\x0001g9åïsMõrMõÔ¢\x00024­)¶nÑq\x0007Á¬Þ­YÓ|¬ì&¾+ÍíýÇ?²êâ!'\x0013¨²!¤iö¹q!ú\x0015AA£E,A·ÛëyH[±âR5êç
qùóÃG0A²üm`\x00039?g\x0016[q\x0010¬ÞiÉ6\x0003k¦e\x0016\x001d¦¹¾/xMÁÝVß¡Zú@UÝO\x0012ÄûÇch¨´æFß\x001cÃjjh\x0017\x0014Ë\x0017\x0014\x000f{Ø®ÍÕ³ë»\x000e<YãÉA<\x001cÚC\x0007\x0017\x000fn®wóÑ®\x0018Âsv-ªñÔ\x0018w\x0016ut\x0010/(²&Ôe¼x±+ñt§\x0007WÏ:J\=\x001d¡oÙ0a%­Ùì 5éi5¤^>Þw"KtD:©WÂ¹\x001aÎ
~W\x0003tc1³¡\x000eTT·§µ\x000b(s±\x000eÏ×x~pí\x000cÍÅÅç7÷}x\x001dòSÔN¯]¼PÓÁÅË\x000fuhí\x0004¶Åf:¥,Ñ¥UxôË\x0016O\x001eZEÁFÉ£|MÖ\x0012\x0008{<Ø\x0010^k\x0007-²\x0007\x001f'âò)ZA	\x000f\x0014àÜZ¾Æ"Ã IöÑyâ\x0018KéÌGLü¼ûSZ\x0003|IQ,\x0014ç\x0004NHËë'CY?/VÚ=hl2\x000c\x001ae/]2¾¯#mB¯$o?Ô\x0012Xg\x001a<3\x0017]n.Çåã*m/½7¼|%­>Ë×¸
\x0018ô\x001bÈghù,Í®øLzÞYÇ×x\x000e\x0018t\x001dØæmóU#:XzKßw_0+¯j!,!_U\x0019Ùé|Ó\x0008Ýä@âG&\x0007bÐîg\x0007\x0002kÝoÕg²5Ó¥Ï¤÷¨x§C`xe0ýüÐ%¼ZïIv\x0016S¯¦4\x001c¤zm¨\x001c(þS~\x00191\x0005¬<ÒUWùæ£\x0019â]]QÄå\x0015É_yMÁ²®\x0019ö+;)\x0017\x0013GÜ¤§\x001czå)uXK\x001aJèµÒ½\x0008¿\L?¾¨uO<rÃW­-rX\x0011Éå­Nò­îíæáóÓÅ¿Þo>\x001fÃI*AQl-p.\x0002¾ÝaÎckØ5o¯n^½»ø×ë«Cõ\x0018\x0015¬Ñä\x0010Kº\x001d	Í±2_¼°_ÝM8¦j45\x0016-\x000cNñìÌø¡\x000bpëÐt¦ÇÐlæZÓnhÑÀ®û ¦F3Ch:Éàæ\x000b:Ð¨$\x0017\x0014çöã\x0005}×öUhûË\x001d*4W£¹!4Ô\x001cËÇÀÆ8?Wù O¡3jõ"Û;ºj¾FóCh\x000cqü°:¯\x0018hÇûÌ\x001f]±X¡Æ
CXyÆBZ±,`Ð\x0004=·jB½\x0006­¾·Éroë]2Y2AJ3 øÚæÝµ¸#l­½\x001d3¸8ß8QÔÂÌeØÎ`_85ÂÖ\x0018\\x0018³¸bëö³HU>\x0005RsoOÂv­±¸0fruÈ³0ãº\x0001Ð«oü7¼ßÌ¾`y­1¹0dsµ\x000fì\x000e¬¥ÕØFÄ\x0014ÕAÖ 5v
Æ\x000c\x001bo\x000cKü=í¶øwZµUn
\x001a«\x0006cf-Z\:£V»\÷ïÒ´draÆ°ÁeÃâw²lFi*\x0010q¹!£kä<ò\x0000l,\x001c³lP¼;N\x000e¶ù{ú\x0010xÙÄª\x0003*ÛhmÌx`]\x0010¡A\x0012âÈ­\x0018\x000f±­1\x001erÈxXÆ#\x001b6´q¹kË\x000bE¹¨G°
­±\x001dr,^3\x000fhÐxÉf³Ç¨\x001eº
Í6hv\x0008-Ô1z-Ê¥\x0010\x000eÂôÓ\x0008[c×ä]³ñ3c\x001absa¹\x0017\x0013ÇÚ¬2¹²±lrÈ²Ùüø7£\x0011·x¯çe\x0013°Êêªæª¡Cj±*\x001fèÈ~Ä\x0000Ä\x0016/£+\x000fi{­O\x0007¯õ8%_%,d~
ï:L>¬»ÀÔ%\x0002xÙ\x000c2îx5æ\ðuÙûNï¬\x001e\?y\x0016ùÚ\x001c\x0007é7¹`¡¸üÝöÐ­yI8úã±Ãüv¹ÔpBQ¬Ü,°·=½\x001fæ2\ÕÌ9(8Ó~Ýý9Òýº ûu.^m\x000e°SÔ³\x0019\x000f0ÕíiL=¬ÄÛ,ðF\x0007æ@kçq\x0019óÚ)É~V­Ú|îãîã\x0010gË\x001c
\x001d*WåÅ+ßÖM\x0007ê~ómõ÷;jt9ìÏ|Ö\x0015Ä$!É[{Ö\x0004N9Â½ÙëÛ«wÛX*2U©!2ÌYæóà\x001dË{\x0011,<¯ôÞWn4S£!´èÂr\x000eØ\x001c½\x0019¨²jn%«ÑÜ\x0018\x001aµúàs\x0004ñD4Ç«\x0016?î*´P£!´\x0018Öå7÷TS¾q)^5ïVí5hOÁÐ1À¼ £b
\x0003\x001cr¢Î\x0016?¸½¹òîekê\x0003ý¶4«oåbhm¯\x0001aÛ\x001bã½¯Å§áÄ²8K¨Ö|ü´y<^Î\x001do52¿$âd
*µ³\x001e:í¾¢±Ü\x000bwuw¸»É\x001aLÅµÊ¢ÖÁ £Ë]\x00198uÈ\x000c\x001cZ³>4U£©!´m>~Îü°\x0019\x000c)¢F4·¿è©\x001bM×hz\x0008ÍÊ,¬E»0,uîÍÃÌ\x000ciÍµÛÞ¨\&\x0016PtÈ¶cfæÈlMfÇÈ\x0002%P·9'ÒòQM§ØÿLÝMæj27D\x0003iÍ¼!Íñ`\x0014=É\x0018'í¡Æ®>4_£ù±E\x0003î¥ñ8?VÍ©R¢+÷>ôv£\x001a- YV'	¨uÎ\x001d*FXþ zO\x0012\x0000­z`\x0010MaXÏ²	MÍ\x0001\x0004oµÒ\x001aà´_e8 õ\x0003C\x0000'Ú\x001bÑ¼ \x0001l\x0001Çg¶\x0018ìæFØ\x001aW\x0000C¾\x0000sã´j(\x0005mv²kÏÍj\x0004­q\x00050ä\x000bðZ
.¦)©Ð*.¥p¯äª#
/!g`Ï
2qÝ¬+ë¦ø x\x0001«l.4Þ\x0000Ü-\x0005jÑ9É²Ý$Û\x000fo\x000eD}l?!`%¿P\x0010\x000cWùkQ\x0019ÙäJ\x0003Òx\x0004\x0018r	6w¡§uKã\x0013f\x0007ïÃè\x0008Zã\x0011`È%à»B.»°XSJÞJ/º¿¾L6VW\x000eY]«
}PlÎrqh(fWúª&³üU-#Ø\x0001è,mXô£«\x00083+?«\\x0012¶ES=FdÝÎzTKù}ZDì@Yw(êÞt,6C_Ç­0%\x001eÑJ²ûÚSW3\x0014ø.\x0017Ð®_\x000càÈ\x0018{\x0008¹Á\x0012°8\x001cµ+	ÕP
\x0012b÷\x0006\x0015½zÃr1¤\x0013%DßóØ5B\x0008;pÐ\x001bî1GñuG½ÇÊöÕë\x000eò¢PS,\x000b5»>³-¾CjJ\x0002c\x0011;Ç*v¥ÏÝ]ÄÑUÄHOæU®rû)=L»^³¼¾\x001a¼¾dO$<#Ák¤\x0014°I9×d\x0002?µ¶î´x"Ûi _\x0003ù^  ,\x0017\x001a`ÍÏ)%-Ë{È"\x00117B\x0014j¢ÐMd4É@ ¦\x0007¨%¢mQÆVñy\x0018©¾;twèdeà²$O\x0019\x0007ì±âæ9a¦©\x000eÌM
Ì;Poò"%&©KµÃ¢½`É6L¶)Æ VQAÇw¬\\x0019m4¿®-NÝ\x0008k\'\x0017¨\x0016C¥QÊ¼á¾B»Tì\x0018 ª£5¢µÞÝ$¸\x0012µ\x001c7q?a´ûóLÍ\x000e½;Ü\x0018ñ«£¦iÃ1\x001c*i¼\x001dAj6¸ìÝàÑB,³µºë×mP¥NqÑ\x0012:Âd\x001a&ÓÍ·&ª\x0007ç|m´GÜ±å`«\x001aAjÎì=søöJ\x0011Æ\x0017\x001fÊ»Ò9[Í~\x001dgjÎì>s\x0010í\x0000·ËZmÑi´ßö¤NÛpÙ8:Ùëé¼ÿÉ\\x001c\x0016\x001c·ÀX(ýÙvÞ¯ÈÆÕÉ^_çq\x0008.Ù&g\x0003?69\x0014:Êë¤Äô·SuR½ÖÉèë4Õp\x0008¶VK(eèÓ§N5ÆIu\x001b'@í/jÃðër\x0000:õ:À<Sc	T·%08*3_u$ær® ¼\x0013,û®G\x001aS ºMëc^í=ÕñÅ\x000b¶¢w.eÃt¢\x001aK º-T¥¨ \x001aO~²ô8!º\x0015þW5§Nu:\x0019#LA-Gñ@-G>p	«sf:rÒÍ\x0016×Ý[\bê\x0008\x001cÊÂpÙG
ì>u£]ü'ªôqÛkÔÓ¾N7!î\x000e	d°Ô\x001cX\x000cx<~ì|¢\#@\x0015ÐÝV@É\x0012Êy\x001c×-Sð¦T¦¸y¦f{ëîíâ©tâ\x0002wE\x0007\x0001ôÚ\x001d×NNr¦ÙÝ¦{wÇ\x000b.ß0ø¥¬0î\x0005qÅ¦··i¶·éÞÞñzDoï:ÆPÜk\x001a9¶\x0002ÆÏ¯S³¿M÷þV^qz xIÛ)\x0008.	Ñ\x0011O#5	\x000bÓ±ðÒKZ%0ù1Ï\x0007¡Ø,­p)¦ñr¦ÛËIgé=oMIFÔMcÍù#gØÒtÇ\x0012ëÈ\x000c \x00049&­8óf:\x0018°M\x001cg»ã8%t>æ²\x00143\x0007ËÅBnÙ\x00124ÂÔ9Û}æT¥ÓW\x0007²À²]o\x0004¨ÙÝ¶{w+-¹5:<\x000e\x0004pbÇ/{¤G\x001ab»}ö®è\x001e¸À	`É\x001d6¨Ë0ÿá3g»Ï\x001c\x000eö¡Êø \x0002¥,¢\x0019ð¬\x001f°T¢\x0019ajBKÛ\x001dZZÁÌ\x0018\x0002Hê±\x0011¸ç\x0008Üy¦Æ÷Únßk0?Cp(m>A:z?ý4k|¯ëö½&ÆJYÌ\x0011\x0014í\x0006\x0019¸¾&®ÿôvrsÝ~ÎòÆ\x0001Ö2\x0012,\x0001+üôUÜ5§ÎõßçbkónÂé}h\x0016CD
v:\x001cpÍ\x000ew\x0003;¼¼Êh\x0014(lR="hÿtÍ\x000ewý;Üë(48%8Ï¾	J\x0007FZÊ\x000e\x000c ùfûþ\x001d\x001e,õÖaó!&/\x0012%½\x00010>mÄ}ãé|·§3DÙâX®JQ8ô\x000eÝ|\x0002Ì7Îw\x001fºÆ^:¶M
«úó2\x00051ÏÔ¾>u\x0007NÆqÀ\x001b7³¤¢"§\x001dÏÜ4P³½}÷öÆç\x001d²L8Â'Ð\x000b6 FN/Rh"¹Ð\x001dÉYþG©&mø¹U9~ö\x00073Ô\x001c¹Ð}ä°B'dé2ÂTuU\x001cÝRÕo\x0004©9q¡ûÄY©0m\x0004ÝT\x0016¼¤\x000fwCsâBÿ_4¾Gs±\x0010õÃEÎùÛSh"ÞÐ\x001dñZÅUF¡\x0001§u\x0002f2Lû¹ÐD¡?o\x0019M$Y\x0001å·õÊð¡sóÖ24¾7ôû^ÔÒ¤dª-Ñ¥6Ì¤¶C¶G@4\x0000ÿm7¥ëÑàé½ ðä9ÜPÓo\x0018 d\x000bÕðlÑ\x000bÖÚ*G\x000bTj\x0011Íùl\x0017Dû8.ú^àT¸¬\x001d\x0017ï.Ü½ ÅôC\x001d´¥\x001føo{PcÂÑ²<&D;  @i\x0007\x000cÂ´PÝq¯\x0013¶(¹#\x0005õyð,\x0006©æ|Ô\x001d\x0014`\x0013Ýc7,°0 ËÇ6\x0007Ð\x0016¥¤" N(\x0014µ¢\x001dY:2g¼ét8@k\x000f Û\x001e`\x0002U³á@\x0003b²eëé
,KeºC\x0003\x0014J£Ð\x0000'Íp?\x0007_7±1|©=yÐ}ò\x001cvoäMê\x001bù\x0015
ëdyWó\x001f¯­é.Ay_.QC§LÆÜJÃ+5\x001d\x001cÀ¢V¦¿XÆav\x0017JsîÉ\x0004®oÖ^Î/T{ô ÿè9yILgw\x0007ãly¦\x0017ª-þz\x0019ç\x0003w-Yãp\x001eY®Ò¤ûh¸¦\x000bç@¶Xv{b|aÍéøße\x000c5äc¨>\x001bÚA[Ä\x0003ýU<XÃJëzõ4·\x0019\x0018\x0005óL­Ïë¯âÁuâñ>;P¼P´£âM;¶d\x0006úkfpL,\x001d=ÔÎ`\x001båIÿ\x000f
üüJµ®¸¿h\x0006ÇÑ¸\x000f³ö2\x0003¶Q©Ìh\x0016ªµ\x0007ýU3¨Mù\x001et<@JðåÓÙË'´E3Ð_5\x0013Ý\x001e©\x0001\x0019\x0012\x0019Éð\x0015Ýâýj©µQýe3¢r-íÙ@9·-#i\x0003¥Z\x0003¥ú
ç:Ú¸=»\x0017g¹IÅÊéj\x0010Pmp º\x0003\x0014G &O°ô,\x0015<pÀbítq\x0011´ÅEÐ_]ä±.Tscx^%¯yVD\x0006mi\x0011ô×\x0016\x0005Æ#äeÊÅóK5ÓÏ÷ ZÓ¤ºM\x0013\x000e4QÜ'aË\x001a\x0000îê×Ó\x0005XÐV\x0016AiÑè|\x0001&Ý&Ýk°ô\x0014ÐÐ%!h3d¥ÞMmµ\x0013ô;a¿SeÈ\x0003{+¶\x000b5\x000fÕ*ýÕEÁ\x0007ö+\x0018!Ð#g\x0010<ÆÓ.ç1@µÖI÷Z§ P\x0007=·,;c8»\x0012í\x0013=1¿£ZëÔ]õ\x0014àãÔ¢Dm^A\x0015û¤¦OnÍî5\x0007X$C¥´&NçÁd¢qãí<Tk\x000eºK±ÒÇ£Ì½³®Ø(ÏW\x0018\x0016Lû¶\x0016\x000bº±âJI®/pø6¬h¥¨\x0018\x000bS\x001aÓÖ¼-Æîj¬h¶%\x000fu\'*ñ\x001dï.ÖLG¿m5\x0016tc%(º¡cWDú|\x0011Êq#²qó_¯µ\x0007ÝõX)Ð\x001d/r\x0005Éó3u4çÓÛÜ´öÀtÛxõ*W\x0017°9P/Ãvº\x000eÚ*1è.\x0013CÅ<NK£¦\x0013­\x0014H.Ð6zÅ×k/y¦÷\x0017¡t	ZP¶#$\x0004\x001eId0e6
ÕÎîêµFÉÒJá\x0010;Ò<\x0008ÆL7i-§é¶æ>\x001eÕeI´y|\x0019ÖÓ¯yÐ\x0016ÔAwE]PÆq¡X¢uò\x0005JN7$áØ\x0006ªÛ\x0003ö\x0008S~Åå\x00058â4óÍ¶È\x000fº«ü\x0014åò¯hIn+2\x0005Ï¶\x001c¦Ki°¿ªê¶å\x0012\x001c?YkrdÃ@Ù\x0015\x001b3>\x000bÕ\x001aóîòÃ<õSÀ]±Ô¦Ì8ÛòCè®?P¥\x0006õ\x0010$
 Ö<ÿÓ,Çw@µ³»Ø\x000fÇ\x0004\x0002¤A	\x000e¬\x0004¿ééR\x0011l\x0000kºí¦´ÕÛ°Ý<	fÆr¡¼*Ìg\x000eÚ\x0002Dè®@A8ð a«\x0007	+#ÊBMW´k-§ë¶Jò§|ò\x0014g¥uîq¶&\x0012º"ÂÀÌ¦.&'\x0017Æ->ýá\k5]·ÕTñÖâÙ\x0016è\\x0015lÙMa>²kë4¡»P3(g²pOªXòy7ìZ£éº¦²%Õ#Ý°\x0012\x0002ù7*×F®;Ú[§<æ\x0019Í±VW
\x000bvf¡Z\x0003åº

\x001e§Jf(i\x0004eXÍ,åÎ\x0006 |k\x000b|·-ÐR\\x0012S¼\x0012[b*ÉM#§;Í¡-ÖîjM\x0014<¾\x0014\x001cEù"\x0004åj>,oëÙ » 
§±ApR]¼¥bð\x0002ëoU¡u/¡Û½\x0018Ô¿"¦piò5Ýêrq³Ù()Zå\x0002ÑmËMî(Ëù\x000c'D¦Îðzþò\x0019j½¦|Ùô\x0006æ>bÂâíl;Áò\x0003Ñ0o;å+ÚÃ^®è©/(¹ceÙ\x001doýñ´¥ËõÝëµÀ¤¤mP{ù\x001d\x0017ýXî\x0013öµä}.OþÐ]F\x0012¦úäxÑRÊÝÉX\x0001Nßd\x0016k\x0015ï2½ßPJ]¢áèu6
Mè=³R¦û\x0003¢\x000e)Ý°|\x0015ÜVükÅ+^n,Ý\x0010QÚÄl\x001fèê\x0010\x0004æÒó%\x0008jy\x0010U÷ADåÛ±\x001f\x0011è1T[~ÀùÇ¢h¸>,
Wç\x000f"ÚS½}qP´^(D/\x000eÓýgh¸>,
W/\x0017öÅ)2\Á°á2%É¨çí¼\\x0008åR üSo\x000bpµ¢\x0008+[2CÓíq`t5ÕrÅ\x001f»\x0013³ô\x000cò¼d"pi®1óïíëÃ«÷S\x0002KÅG¬\x0012Ù`0ó¥ÕN,=£\x0018ñÅ-»®o©Ó¡r\©Ír¥º£\x0008¥Pç1/\x0015äÎb\*~zÿ5ÝÖà}Ëå}·íúïñË1!b1&äöáÃýãæéáË±9&\x001e­ \x0012&Ch\x0015<~V-SîôßíÍ³ë»«w7¯M3!LYcÊaÌh2ÇIjÁ
\x0006ñ\x001aÄ*$Z\x001cÔ¢\x001eÁT5¦ÀÜÊK)ì²Í]Û8\x001fVó,©kJ=NåW4ï\x000c)Î²,\x0010ÿxHÕsÒÔf\x0012_Wøs?+È\x0013vÄÁI\x0014#¶Æ´\x0013ñGú8\x001a\x000cïLUTÎ4\x001c\x001cý0éjL7i\x0004\x000fI\x001fVµã\x001få!Åô\x0011L_cúqLçÊPÊ\x0018hò¬\x001b\x001cÅá\x001c«\x0019jÌ0±ÒP}\x0017Z\x001e\x001aÚí\x0015ð´ -Î°5ëF\x0007\×Õ\x0004ÉÊrZ²:®\x0007n/ôÔqG8[\x001f4îÒW×l\x0004Õ¨âW²9ÏÙø pBØ¦¬é«Ç
 hÚ¶®,ç!eÿ\x0011ÎÆ	Á\x0017r4$Ëoù«[zQâ\x001cËÙx!pC1Îçá¸øÕ-ýÞ~õ=3AÇ9\x001b?\x0004\x0013\x0008óæ4éM\x0006{ìK±Ö
\x000e)±`6~\x0008&\x001cÞ¢© ©ñ9º§\x0012{\x001c\x0016ë\x001eál\x001c\x0011Lx"\x001bwg õT\x001aÖ|¼<ð`?eÎa<\x001bO\x0004\x0013®H«¢¤ð=5Ó#ã Ïq\x001aW\x0004\x0013¾È8Y[¥Ü½é\x0002?¡U:\x0003§lpFqÿ±x¶\x0017"\x0008ï\x0014\x0007Jêà´\x0011Ìö¢1aä\x0015KvDJË£§\x001dl)Ý\x0019â$ÙØx9aãQH@Óî´}®Ü4öÈ\x001eçl¼0òÊ:ºk(§¨ \x0017[\x0018\x0014cê3\x0018OÑdñæ¶\x0019¾\x0008Kïù¸\x0016ôá}4pC=8¾jÈ¹·¹³äà[±þN+jÍ¥,ÞÒ<í Ë¡wçXWØ¡Å©Bl¢r|ã4z¢\x001bPg\x0008pÞE»\x000b>\x000cj\x0007"9'\x0015ÍÉ6À¿76ì\x001cËêÚíêÆ·+Þ@èúF4§ë`q8½TØ¼Ìµ~\x0002Ó)Áó	´Ôe\x0008§å\x0006²îv\x000c°H/ÅëG4úÏÿ¸ÿóáóÅ¯ß.îþñÿ\x001cýÞ1>&äGó³\x0002(Îùêåüµç/®_Þ¼ºøñýÅÝûÓ\ºæÒ#\¨ÙJ\x0005xe\x001bã>Ìå\x0016ç{ËÔ\fË((=iFsî^úÀÏ\x001d°¨â\x001aã²5\x001dY¯x5ãê2\x0000n½\x0004_T\x0010¼Zó\x001d]ÍåFÖËi.BÉÛÀ\x0002`<®\x0011ôÏèk,?²\ÖÒèo,'%)Ø
~
þ\x0018V¨±Â\x0000\x0016\x000eÕ¦RÊç·GT%bÕ\x0008·¢:U¥SRÆbä+â\x0011ÒÕA,J2FÙ\x0015ëU\x000f9?é_0	\õ\x00127\x0018Ë8A\x001e\x0019\x0016Yñ1®ÆzÁù2ÑwÒë£\x0017â4¸$[/käm\x000f\x00113z|T6\x0003­¨iMY.\x0006Øì:\x0006ÖG\x0018984Ôâ¾âÎÿí\x0004&g\x0017m\x0005ö«ã
Ã?ô¯[0\å\x001c\x0004°Ô²re\x001a^äâ\x0007?è\x0012/~ÔA>ÏöÌûRM\x0011ï@¼|Ë0cð ìðéA>¬ÂäùÐ@c*E\x0015\x000eVÙÛ%^\x0018£³Ø%E^ãÕÇó WîÄüì\x000c°¿,(mûDùbóÀÿøæþÓ§ã¨\x0011Þvu\x0010ü¥åªx½<\x0014¿¸ºá|s}{{ôUÕ.âÉ,§ã©a­/\x000cèÔXöþJCaú8²ªÕ,r+À\x0015\x0014!\x0004	<ñ/Þ\x000e%çÆu¬§WY\x0003÷Ói_$$×G¨EyÄ\x001a`S\x0003é5\x0006Áâ\x0000ÆH¶\x0007²Ü9\x000e'Çml§×X\x0016\x0011\x0018\x001bÒÄ« \x001dW9)wða{\x001cÙÕÈn\x0016\x0019ó9¬æ\x0003¿ËbW?­òÁÁãÄ¾&öÓû"^\x0010Hr6=PYdÜÎÆ«\x001aó¦¦í\x001b>\x0010¯°4·*@éÇRKÁå#È\x001f7¿n¾>=\x001eq"un\x0007ÝÈYè\x0018*Ð
Ö`\x0010­²bMæ#\x0019É	£\W£¡Yþ8½Ô[»öî\x001fZómæ&j\x0017¹Ô±ý,¸³Ñ`ÐCWrVPÖâ`BubG·Ê´«ÛLå\x0010¹V\õ	\x000fX\x0005[:
\x0001\x000ee­Æ×\x001bÚõéõÆÒ~jfÓ¨ªDâWî?\x001d»äC»KfÏ#ê5r¬6EIÞÑ´2Ý=ôÑ
½ÁE®#Ñ«ô?üpûåéáë×û?ï??]|ºÿzñúÛÇ?î¿\x001e}lS­k<ù\x0002é\x0002i\x0018Ó×¸·¯ßÝ¼}{ýòúÕ»Ûë·\x0017¯ßÇàùíiTY£Ê)T<sy4)Ã×]\x0010<f%þó ª\x001aUM¡\x0002«¹ÅU54	Õù`\x0015£º³êTÏ-ª&\x0019b7CJ¯F¯#\x0015ËÏ/èó§³õíâù\x001fÿø¿î7ß¿\x000c°²Çï^\x0006TÉ¼(µ'P{ñüÅÕ»ë«£¹öc\x000búØC`¯\x000e\x0014OmSª4Ø-s´£lºfÓclàøª*yT $ß.­ð{lç\x0000©ÙÌàºAQRlXâºf|+×±ÙÍ±	Ël&l×MgÔÕhnxÙX·\x0012Kc¨ÌUr6Ùìu\x0003l¾fóËfØUã³å\x0007¼"¼ïõv\x0000-Ôhaø$pK¼ô<KÉrJ[õIëªÆ\x001fKÚu9XP\x001a/Ñ©N0\x0000+º/½ï(\x001b4l0¸psñÌ	*¯ '¨}\x0015\x0019\x0003péAÛb·\x0014Ñ:Ql/p»Yê_\x0003×Ø^\x00183¾ÎXn¼\x0017\x0019*\x0004ÞG±ô{òd\x0003pñ1ëëòÄ\x000eÃ\x0019'ôÖ.½å\x0011\x0010+­/4&\x000eÆl\9/£â
ÑPá¬cñ\x0018©öU+
À5\x0004Æ,	Âñ@&çyLº¬FèìëÙè3B4$ýû¡#¡,·\x001ckÁ¥\x001e^iÍé\x000bq|í¤,h×µwÒ´óÊ´ß¦Ð{U´Æ\æ£ÀoË\x0013ö\x0014ÎØúò¬ÊfOp+Ë\x0019Ø¬HvdÒ¬üÄ¿ü¶ó\x001bó´ûF±Ö\x0003PHÎ\_gøÔ/O\x0015|\x001aãóØÑ65¼d>\x0013SKÙ¼aÛ÷ËÓýãb\x0017â_\x0018ö>\x0014M'E°8Z\x0019\x0012\x0008½<)zü "ô\x0007Û E\x0015íÁAîH_ùÃè9!UY;Ùò9))!WY|e;üa\x001b.+ÒJDDÃ\x001dÃàÖ!ÊåGã\x001f9ð¼H\x0014\x0008¥v\x0016¥XËÆªiW\x001c/ámô\x0018_N\x0005	ªq\x0015\x0006\x0016[ªQ@x\x000f\x0019þáõ»Ó`²\x0006\x0003`^¸Kî	(=t1xÙÖ°ïM\x0007ôr©K,/Så£\x001d¡z\x0007\x001f½\x0005Úë|{Át
¦\x0016\x000cJÕ¿
\\x0006,åºj·ß£õ\x001aÌ¬\x000bÜÞ\x0003=é²ÅZµÅl
f\x0007÷~.¡Ô(\x0014FÞAò|\x0008lçØ\x001b£ô¹\x001aÌ
­ ½/­çÒÓx« \x0005ÛÛØÜ\x0015j¬0\x0007§j©=5éx)é\x0006\x001bIíÞp¤
Z\x000b6dÂâÖe)ý%±Ì@¤Ýëâ{¹\x001aC\x0001CBk2úZ&c
c.%Ö,Xt\x001fÚÿa\x0004
(:hÀ\x0017x­!#&×-ZdÛ´lïM.]¥lzûóáóq@PªÉàÁ\x0016V\x0006®7òúP;Àó÷/o^\x001d}K)Û\x0002Óx^[~ýÃ	\x0005T$èPVÊ¡ì¡ª^<Uã©Q<ê¨1Á¥ªLÇ\x0017\x0006¿T\x0018§Ó5\x001e¤3eFmð¦,äDO*õ«ðLg\x0006ñ¬¦æÃ¸zëê¦~¤¸z\x0007åzñlg\x0007ñáâ\x0010#Ü|\x000eÎ­\x0017\x000eÖÙôâ¹\x001aÏ®^à`\x000cÁ/yñx0[Î7\x001a§ó5\x001f=\x0018{\x0000\x0002ªÞ\x001a>\x0019åÜ\x001e|µïÅ\x000b5^\x0018ÄS»\x000eJrçÃ"\x0008ªðÝwÑ\x001f¡«3ëòV/ \x0003ON T\x0016
ÅZ<'*ò­\=h}Æ¨Ó\x0008ë¹Ð*Ót\x0008kT)RÝ\x00179õñ[ø4LÊ\x0016¼÷?ßÿýáx\x001d\x0003\x000e\x001c*: \x0018\x0011óå´t³{³÷û¾¼~õêúçãE\x0017\x0004hj@3\x0008hKyvÚð3¢ º'íÓ5&ølÍgGù\x0014·<éx\x000b£ÒS/XÁ3Bïoi\x001c\x0001t5 \x001b\x0005\x0011Ð\æJhz\x0018ÓXÅ°/Ô|a/:/NBàf¤õà©P{±¿Bz\x0000°î¡qµé%ÔY\x000f5\x0002\x0006úÂñ\ó
zØ/L1\x0000h#bÏ\x0008\x0008.ï@{ã¨­\x0016ßò7¶zo	ÕÐ7n«õ\x001dUëq
Y>5\x0000Í×õIÓ7s:³·jjè¬T·tZ6ßßZÂr-a|-}íOÛ	V@S<tSk»/ã3ºOíZ>
\x001e\t¾·dõK/¨Ì"#}Ïý¡Eüð=}n±tÐ¢ÉÏ"ÆÅæâçûÏÇ.ÅÞÀµ
1`¸ä.!×\x000bVî}g~ù\x001aÿÝÅÕÅÏ×¯]RÖrÒXî\x0014ïéô\x001c\x001eÊ»$\x001cº¸÷AÚåýÝV÷÷¯\x0017/6OX±y¬\x0008.r Ý2Ý;ràW¿½_úí\x0005¦áãw>VþfW<[]ñ:éÀó°aíI¯'ÒqIZvÒÓµV'­ßÖêüÿ¾°|ËÐ&hî6?\x001e=Ê(ðÎbY¬ÒáA&s¨\x000fv§Ü]½z~ô\x0014/\x001f3 ´¹ÓdFR¹\x0019rp\x0004Ám~ñoûÎÆ\x0008ªÙÔÿGÝÛdÇu$[Á\x0006
ÇÿÌF \x0004I¨C\x0012lÔyù&:PE\x0011*\x0010TVæ¨¦½öèUo¡ÚI­¤ÍÜÍ<Ü#n\x0004®ß\x001bÊBv÷S«ø2_Øu·?·A©ÉÒ\x0015Gå×eCy@]h«\x001dÙy\x0012n»+Mç®´3<eåÈß?<Þ}<X¹.×)?¸ Ë\x00182\x0007y¡Ú\x001a°~Ç¬¹ó«ëw¯\x000f\x001d9£·ÉåÕÜøâþáÇKè¸ÂPç­ªãAdqójzØÁ«ë/Ö\x0011ù
ÝÆ²uöùñþáþóãíÉñ'ç7\x001fnî>¼{¸ÿëÁ+ë\x0013\x0019Þr+4\x001eC_$¨D4¡\x0017àûwW×Wïß]¿æìåÙåÛw×WÂÛ»\x0019ÔV\x001e\x0004äAf

	£²4Í\x0001m,îsF&ÃL¥³O¢¥\x0016-
¡Ù:\x001a×K\x0000ê@f¸îFO\x0003XMr\x0001±$¹0+ñÐ\x0017¼¸\x001bò¢ãÚ_dx$\x001dA³\x001d\x001dB\x0003)\x0014u´kçÉr\x0003)j\x0014½«RFÈ|GæÈ÷H:\x0016\x000f¦¥\x0014~¢j-tla
\x0003Ý:\x0000Ñ'yË$ËÞÇ]wy\x0000­h2\x000bm¦ØhÿFA£*ÑÒk_\x0014ø\x0001\x0010ÂD\x000eu­»\x0007fä\x001eDýÏ\x0013wi'¿\x0019y®\x0000AQª]ë:ÖÝ\x00033r\x000f¢V²ÙÑÚrØ|éµa{Êþ(\x001ath0FUÒ\x000clÙ\x0007©c¨óC^»·\x0002­»£fäÓ&oº>æ]ù"Ô\x0010~Úu­»£fèjíh
q\x000eié²\x0018ý BM§Mç°u&ÔØÐ¨È
¤ª?J´íå\x0001\x0010õÇD&r\x0004­3¡fÄFq+«¶@õ)åÒR\x0016È¡
°ÙN·Ù\x0011Ý\x0016\x000fòI\x0012µë]U»a¢åz\x0004­SmvHµÑ~¡²Íhx\x000ficI¹äí\x0008[wKíÐ-õÈÆÕTÎÍá~êwë'F^ uÔ\x000e]Rcó\x001biÉ3\x001a©¡¡Y³ÔYgImw\x0013ìÐMÀ Y\x001e\('\x0016-;¹3-jÍuÇÍ
\x001d7\x0013@z/£ñm¨vë[ÆD7Ù\x0008éÐÌÐMðQ YóMÕQdùW)7×Yy7dåihGy\x001d2S=A\x0005[w
\gâÝ·¦N1¤'p©R]E\x0010õÄÛè\x0008[w
ÜÐ5 
e±\\x0003Ú)Å¥Å)ÉS@Ü^p5È\x0006Ý5¡k`©²|Ò\x0004ûµR^S^Ø¶cæQ¶î\x001eÀÐ=06HÚ\x001fý¤ÓèXµPýUhÝ5¡k`£ÔÐ`°ndÚVõÚ?æ:47$5/ìJîËx\x0010\x001e¹$ë¤ÖQ\x00182£\x0006£\x0017ÍúÃ´:W<£°î\x001etþ$\x000cùT°+ÖÀ²;IõÅb\x000c&^Þ\x0007È|ç²ù!Í*Ç«Pé:1¢É;ù iÝ5ðÝ
õC7ÔÒ\x001eOÖºNEéJÁBT\x0013\x0003ÃGÐºkà®uF2´¦¦T£bó¢Ø¦GØ:cå£µ}åiAy	H1¼\×¥íå\£lÝ\x001dõCwÔB¤ÞÓb¬RÙ>r³Q*\x0000¶'=²uÔ\x000f\x0019R 8¾øáº4Ï¸âú'tñWÝÒÐÙÑ0dGÁ\x0005J°e4*
<â,
_§ÛBg¬Â±¢¥(<¹\x0012?÷%$«*[hm\x001aaë®B\x0018º
gÛ®\x000c*\x0013ÍÔÉ\x000c0m'*bFØºã\x0016Æ\x001bÍ<á·h¯å×ÔùdÚ¯ú¤±;nqì¸¡\x0006áúlãwE%<ÿÜg¥ZÒQCF[ù¢Úµ§-ÈMXÊ1ÖÝ8t\x0013¼\x0002ßf"^Xd´iw^)µþMhÈ\x0001`¹öTGyºJVJ'Uò«¢øØ]8t
hÆ®Ýõ\³ë4ÏÛ\x0007üW}ÏÔùFiÈ7¢ÉT%R\x0006CSø¬\x0005©ØÕ01j­»¢ièRfÙ\x0005´·¾´5S£\x0013³åìkØº+®¨7<X%1BrJÚN0ÂÖÝÑ4vGñCòº^g4×H¢+\x000e2nL­\x000b`RçT¦!§2oRå»@»Æùj~\x001a\x0002³J}¤ÎmKc\x0019JTµ¼îÕÒVÆ$R[\x001a&\x001avFØº\x0014e\x001aJQzz|äô©Í )Ï3)_ÔM\x000cÏ¦U§A´\x001aS!çbÊô\x0001ûìêàxK®×\x001a8ÓÃÝS4ó¼ÖÕza\x000c\x001aê\x0000\x000c³*¹«Uÿî­Æ.j¤8ÐQ>q
\x0005j¢ÚÍõlc\x00175hjÍ)GÎóô¦ä!É°ÊÒk\x0005=ÜÏ\x001bh\x000eOÝ¤:®Ò\\x0007´óGrLìÚ\x0019=Ü\x001fBÃ\x0019@F\x0006n@§¤®5Q«Ü7Ý\x0017§Ðÿ8\x0002gAl*Õä×R\x001aæT§r­ÊkÝk\x0012=¤I¨\x0013\x0018.\x00041ªàëØ^T3
·U?3ä\x0004\x000cJ9töÊVMÂ¥ \x0018½®râ´î/«\x001eº¬Ô\x0005\x000eEËy\x000cëË\x0013VòªÎëîÃV
ÍP\x0011

!:²þl\x001f¼¼\x0013KëTðV\x0011ÍX\x0015M \¯HÎI.­f\x0011É­òH´î/«\x001e»¬Áò~$J©r·(¸5>¦îËhôX\x001dM(ó\x00192\x001cÄSU\\x0012oÅ°YUH£MoõÍÕÏà
\x001bµ\x000f\x0017'Ó£\x0017Ålv\x0003¬û"\x001f=Vå\x0013R\x0010?öìð\x0016\x0014/Ûi\x0018ó:¸Þ°Õùàx.bò<Y\x0004's\x0011§Æ\°õWu¬&\x001a/W5Ð&ÄÍN¾êªü îkiôX1
=æ\x001a\x0002\x0008¶®\x000c\x000b22¦ó¯\x0013\¯FÆÊi¢º\x0010\x0008\x00004),\x000b.iÙÌ25Új\x0000®¯YÑcE+yg{´\x0019Ë°ädN÷«jfµíõ\x001dÓ#´/?kØÀù
·2z°½Ñ·CF?!\x0002/¡	µe.b æÁ¯\x000b¦µí\x0015\x001dR$f¨iþ¬Zâ|ªÇ\x0010¸I[#p½G2V(¶\x000cçx\x0015\x001aS+3¶`i{UbTI¢¥·Er4	c¤ëmÝ^C5
×«±z$9À\x0017&p\x0003}´^>k\w!\\x001f>¸ðj.è Ûx\x000foJNöúL
1\x001daëÕÜX±\x0014FÑ¢#Õöòó$ñq¢-o\x0004®wIÆJ\x0012úr<\x000c\x001c\x0000VsIÉD\x000e¼¬«4ëÕ\x001bQsøU\x0013·\x0001C(%ïå«¸fÕeík¦ôPÑTRJü:\x001eµd$£w«ÞÞhLÇ6¢H¨FÒÀ\x0014õçôQµ\x001a\x0005çW)¾ K\x000fUt%µI\x001aeå\x001dÄ)InßO
U\x001dë+ºôPIWR´\x001b%"ï\x001dO)\x001b¼ö³ö%]z¨¦\x000b
95ìH¹ªQ2U\x001düªZ\x0016Ýté¡®Æ·Á¸bº\x0008MÒr\x0010V½Áé¾¨K\x000fUuáuP5`Õ¾ÂiDe@«àzd¨®+é2*¢\x0004^3ÈV¯Òsþ\x001a¸>ðÀV0²Y¥âK_Øt;ë'¦Ó°õJn¨ê,iÚeÎK~éÕ¦4B£¦4ÄªZ\x001b
½!\x001d?EF¾ûJÆÐPD"[\x0017L÷%qz¨&.é\x0004uße \x0004²EIïYÕl¤}¯ýþÅ@ë\x001f|\x0008¥}Ød\x0013\x0018Ø¹©#l½ú\x001d*ØKFEYøEÃtaK2\x000bV\x0015ûR\x001bU6¤~
íwa%âáT\x0017¹ºâ\x0014ÌDWû\x0008\¯~ª	qV\x001c`o#ýk«ô\ZçcöÕz¨\x0010áj1/R
ì×\x000451·l\x0004®W¿~HýXóóø¨\x0002g\U¢\ÃÖ«_?¤~iÄ¬¤7ÜàG<ÈW+ïC¯\x001di+¨\x0011Z'èÜ . I\x0013Sñ\x0007ØB¯Ãþµ\x0002¦z\x0008þ¢vëWu_©Ê0\x00137æ\x0011yù*\x0014\x0005g«=U\x0013sAGØzÝ\x001bt¯Å0&\x000eq§å°Y_\x000f[Z\x0019é+DõPh²\x0001ª~óº¼]¢û&ó\x001dÐ0¬*\x0008Ò¡W¾aHùZZÍÍ×ÔùÒ?pZÊZ)¹Þ÷
C¾/-îiÀ\x0013çÊüv³òê\x000bSÃ^Gàz\x0005\x0017\x0014\x001c\x0015q6¹Bñò+9Öý.\x0003p±W"qH8##\x0000ðÌR£p±®±Zù\x0006××°ê¡"ÖD\x0003v4;J!QèÔw®u\x0005$}õ\x001e*ß£M.¢I\x0002u`\x0014×ÜË\x001cF %t«àz»ì\x0016Æ,\x0012ot
EÍy'Ùi\x0008kîªQýð\x00045d\x001dhýªa6§h\x0004Uf\x000bNØâÄäãYpþÑÎ±¡øöêv|4©æÍdíhÒ]OäÕe{\x0012\x000cZ0\x0018\x0000[2tË·\~\x000b¼´©Ð\x000b
ï\x000eWIÕÖâ·\x0001°Ð\x00110ÚÃÎÍ»í\x0008RéÖ\x001aA:ÀZ®4À¦\x001bT\x001c9.¥Sèé\x0006\x0011X\x0018«=\x001f¬©Êí #d4r\x001b\x0016»£NZw'\x001cÊ§ÈÂw¿~zp?ËµÌ«o?åÁ~yæ)
!Óüùö¯ÄâQo¦òº+æ8jÚDEùÄ¢hõ¸¨¯¯.þô\x0005í¥a~{§½u\x0018h0ìL\x000cc1¬)Û±\x0008Ã§ò ¯PQÕ¤Õ8\x0006þ7Ý3ÀÀkàça$j-ù£d\x001d\x00142F\x000cÆ\x0015\x000cíýòw(ÍF\x0019\x000c¥8\x001d\x001f\x000c(oéÈ`êêÈ\x000c&|Nÿúé»25.ï.Sâ~¼»}ØOæÓwó`©¯\x0011}\x0014\x0004\x0008U¾7ªÞ\x0016\x00019¿ºþòòâz\x0016Êæþ£ Ö
ÿ((Öª?ÈV=O¦ûñ¿ÿã?/\x001e~ûë~(\x001c¥M\x0011Ê\x0001_æ3\x0013l*3	Ïft\x0003U&Ñ}yrqýí2-
å]yu!IQ°l³¤v%^Q´÷Ù,²-/©@&<3%yþzºÔF)î\x00163AË\x0004\x0003L{èHyò\x001b3\x0002<RÕÃ\x0018ò-\x000f¥MÉ-\x0007G³,Ñ;¤\x0013å,Ë)h·üÛ\x0016)ÌG@cz©Èäätd9i¯\x0016C±W!WOÍ?æ\x0018g°\x001cMM|÷µ¥R\Q¡±^LÕ+\x0001`h¼¢)ßÏçWZú~ÜPßÏøÅçÜt¢2óE\x0005\x000eÕT9S^)z"¦d\x001d+©Í\x000eîa&Û\x001ds;pÎ\x001du\x001a\x0016(
î4;\x001eä\³ 0HZ¬9]'(7 (P¼ê\x0015¡ð_Á\x0016I± Üf»Û\x0000\x0013l\x0018hM\x000cF´7?Ü}<à\x0005]rØ\x0008EC2	Ö\x0001cÙ:Ü®ÁÂxöìüòõ\x0001÷¤¢\x0016- \x00194Ê9©Áv\x0004±=g4\x001b§¾â|4n:\x0010©¹\x00116\x0004)1[^"5©/ïéÈìÄU\x001c`
Øt(Ã-åéâò0Ì6¥&\x0006Ø|ÇæGØÈ§Q|1u¤Dqöi"£93¥ìç£5Z\x000c:-6\x0007Ê
ÙF·Z­<£mÊ"\x0017¡YÓ¢Y3æh!\x0018Äê²Ô\x00148/¾Dr«ØlÇfØ(\x001b
§Þ\x00146\x001b£Øo3a)\x0007Øº`Gn\x0002%%¨\x0015ØB\x0000*G6¡\x001fßR­Ý*åf»`Gn\x0002:Ìo)²yRt-¨$lSNë\x0000[§xíæuÔ\x0017\x0014Ê7¥¹¤10nõì©M¡ë2¶Ø±Å!¶`éCf6O+¡3\x001a\x0018\x0011Ûæn\x0011ë4\x001bÑ \x000eC¢Ò$hx+Tù¤1âUx\x001eW±u*Ä
©\¼TT\x0008
ÕEnè|³1UA)ËØºkê®©÷ÝZt6<%>R3[v¶SR\x000båæ¶Ý#\x0007ý¦W74VÿöÜh0`>n@3ÿ\x0003«'VÁS|V\x0007þ¿:£úûFþ7l¦e3clG&\x0007 7NíùrÖ"\x001b¼\x000eÎ¶pv\x000c.RÿEpáTT/»»¡©é[È\x0006-\x001b\x000c±Qb¿)FTå\x0006I²ãGU}\x000ecÍ·l~¦&Ç"·hé_=5"8¯Ý*¸Æíuìö|U.B \x000fèE¤TQt®Çé:Ñé1ÙÖ5é\x0014gz}2Qn«Si\x001d]ìèâ\x0018\x000eå-.¦%WT	«àÐT}Ñ}áQ§ç^à\x001fãD?~>yÊøþn¿\x000e¶xIK\x0004bèD½-\x0008G\x0003"íÖtî\x0008ï"úòýÉ\x000bÔÆWû°ÀÙ\x000eÎ\x000eÒy®;Ì!\x0004YgºÀ\x000eIèý":j	ÚRÃÚ\x001a¾üå×OnW2ÿ¸ÿóQª,ü	Îi  :'g¬gGmÃxùêÍÙÛ·\x0017\x0002É¿<t\x0006\x0019Õµ¨n\x0011*~á\x0012êäÂ\x001dWH½\x0012RP~\x001d)Ø-óAÉzYÞÐ>\x0016^¶sà®øÚBiµÊ.A\x0000q	TÐ3oh\x0003ËM;\x001b4-\x001aÄ\x00016´\x0019e\x001d@yN
%-\x0011­ç¤MÕß"´Ð¡\x00114¯L*e'ÁÐ"¶èç\x00177kÝ»2-º-º\x00116\x000c%8cµþÂïhù	\x0016¶­aKÝiK#ÇÍ\x0003\x001e7U¼cã\x0014gÁ¨ö4Õtï'5ÍÙmÀCÀèªÞ<ÜÞ|Þ¯ú¨\x000eÑL\x0013\x001e8r©HõIä¢iÆkè]_½?Í\x000cßõ®±­\x001bq»j}>;øÒû\x0015¨[Þ©ò\x0005å?\x0015BTÛ\x0012k*aÄ2-ÖTqÓ>,\x0017XZÔLãg8e·õÆ\x0008k±¦\x0010÷bIÐ
\x0000¹"c)'X:Ø\x0015X¾Å*?ÜF_\x0000\x0002Íx$!CÒ[¬QªÐRM\x0015}ï\x0015\x0016)i
nYQ °Ø\x0006\x001fl\\x0015[¬©rÈ\x0003Â*oÄeÉ:±°´`é\x0015'¾}ªÚìÝÇÅãáCÞè<sEá¸­óG¸lÇ5U\x0015¼7ªGmU°£§Ðü\x0015-¿^\x0007HiÛ\x0017\x001fÀ2Þ\x001cÞ²7Ê²nP\x001e^_\x0002SÃ1S~âÚl¬:U6GÎS«ÀN$ QâçuR«\x001cýõ\x00153³áÔv\x001eDåø\x0000-ã\x000fðåîáî×CcES©FpÖÊ\x0007hN¥\x0006Õ)V4çðåòúr\x0006iéÌ \x000bÅ'C¸P\x001f¶½\x00178\x001fWÂ¹\x0016ÎÂAÙWJ76ç%gKÖáA\x0007£x¶ÌÏ"áEj±)xÊô¢Yç[<?çÁØä9\x0003GË.%Z	jíÉ-^\x001cÅ³òÔLåòò\x0012È)\x0007¤ÓË^Ü¾µ±{Ü}{÷ÛÃíþ\x0007gG}Jß¸X,ZÌÅ^\x0007è\x0012·ß^_\x001czuf0Ó\x00110Ô%ÀîPÀå/É
ÖL&|çÙ\x0016Ì\x000eÑôÂ*1G# Ä¬øi°\x000eÌµ`n\x0004LKAC\x0006\x000bwãI\x0019lò-|.\x0018´`0\x0002fS©W\x000e¹\x0007NËS$\x0004CXuÄ|Ëå\x0007¸\x0012åÆËDW\x0005\x0016¶,0*\x0000]\x0005ÖÙù\x000cíü\¾H=\x0018lèc^çÓ¼1ñI£Í:øÌ¶©7ÙÔKèüç»\x001fî\x001f÷s¡â*ÃEÑmS³X\x001eÄu\x0010§RCçß\_íÛIÞPÊÌ§B[Ä\x000f@m?Åúªeñ\x000b{·\x0002ËµXn>\x0016_\x0005v½©¸§ä}\x0000/Âê¢Q,ßbù\x0011,GKæ\x0004ôä¢	V4¥¶´«Qý£ÐùÏ7¿Þrý½Ye\x0018<~:(\x001bsg12\x0002?ý*tþÍÙ\x001bZþ4]léâ\x0018\x001dª0*`Èx>ò»wTF\x001eÔTÚIj\x000câ5/T«âÆør+YI1Ç\x0004\x000b:²Õz'2Í§Ü¶³áHol\x0016B|ñp\x0007ðpÌW|5jù¤(¾\x0004}5tºÍ(lb\x0017|q}ÇðiDÓ"gh[Dû,\x0011]è%¢o\x0011ý³D\x000c-bx±EÏ\x0011±É}åcù,\x0019»+­å6ò6ÏL{ëíhVG~p@G&\x0010íß/¿þt÷pÿñPn8RóT.\x0015Ê{³\x001f\x0018å9D¹íä\x001d\x001a=²h\x0000_½ùúòúêõÓ¦%4Ãà¹ÂÕ¢Ã%ùEZÆ°]0\x0018¶ýèÐùÑÅøöî§ù9øüçÛC\x0005	Â&Ú¥\x0006föª ²KÕwàü½¿½üúu~\x0013>ÿæâ`åDØÎP\x0016âÈ&N\x001fàh röl¡f4lW¥°¸ÑJÜº\x000cÙÑf&~7ÀàÊç\x000c\x0008A¤ìºôÚ:fÝ1ëÅÌÞÓ`¢	jÕ\x001bxN¨¢&,e\x0018Aþ^¬´@\x001c\x0017ø\x0007yWé«»O÷\\x0017r (\x0004£\x001c_Þ	4÷¿qEW6K)Ta®=¾¯Î.ß^qQÈ\x001b\x0015l§¨Îòò¼/¾øææÛÏ(È\x0019­´ïáåON¹DÀ\x0006Ý\x001eS¼ø\x0017gïQ|µés_Sró-\x001fKàË(@\x0014\x001b\x0015®Ü(½ 7\x0016Â¥\x0016.I\x000eC×Ò&KSÎ.£*Íu/sÙÌw7~øõóßø»Ò×Ü<À{óáäÕÍO\x001fsDmx\x0019ùâÕíçÒ{þÅ\x0017Ñ(\x001a«P&Ü(êÂÊs)¨RªT}Ð´ÂRrñþºôoâ¿={yòêìë×{cë\x000e¯4ó>[¼ÒàûlñJsúóÂû³ÿùñ_éfÐî/ò?^Þ\x0012ÙìGì¥¢E\¹!QZ°\x0006ò´Z­ÌÁËU\x0016*\x0015ú\x0011ór¯\x0003Ñ¡DBsQB1»	u4ï\x0010&\x0012\x001eÐ©»\x0006H¼ú÷êö»²Á¤ì-yñpw\x0008BçúI\x001aÌ»#¼õªlë£å¼\x001a:\x0017×û\x0001ô_áþßnØÐgóNÀ¿íæ§ÛC¢@ËMÓI\x0016´©\x001aBQ\x0016Îð>CåtÜý*ø/g_ï5Ñ² VüÂÎf!\x00073'ú\x0012ÍR:ÌÂ
ð¿\x0016\x0015,g¡\x0006\x0003gfËÅjÞ\x0010\x001f$%\x0010ÞÔåJúx\x0017² L]Ëâ.u-t==næûìy9\x0000­\x001eØ=¯óYð¿ëÒl\x0016\x0014F,w\x0006-æñâÈÂ\x0003¼i<¸^BUiàg£*UHIÑVð<÷	Q¬\x00132Kq\x0019
\x0005^~>J2<:Q¡óF!]Ñ¸r4Or^ÈÚÄù,²ÛJÑ6KÏ§%¦XÂr\x0016Ú.\x0012æhãMO{ :_GÞ$¯¬+\x0005 ËXèí&ÎþF ]`¤éÜh6Î/?ºyÿXþÇLU\x0007ÜÁ,\x0018kËZ`oh!$\x000bFåêÄ~ÿ1S×¡\x0011ÌÍT|yj Éz-\x0011Jf\Õ~lÂò\x0007M¯ÒÛ_ïÿzðcEW¶)**\x0018õEËXÃëÐTqË\x0015ß\x0006Þ¾¹Ú÷Ø0ÉÌg\x0002Í³[\x0011/\x0019¤¾®©'uä3ÙÉÎg*Ké3\x0013þ«-&Ó\x0018ÅP6¤\x0015PÐBÁl(jx¯´Bs@=]ÅFxËPyÀßR(ßBù\x0001I9\x001a$%¥}\x0019ÒV âÖõ\x001f-T/)òY
D[æØ~ä¹ÊÂ®\x001eâÜ=5ðýäòÑûfdc&Û\x0011µ°©»{zàòÑ¬\x0010`ímËàzü|2Õy×O\x001d;Sµü¡+)sÃ±}\x0019³«ÀåÉKÍ&-ú3-8Zj[[©N[å×ow·\x000f9ÿ°æöðÇÄ¨'iIÉÆ	¶íúöòâzoCjèZD7èÓ)K&¬±§­4û+×Ð¯"ô-¡\x001f'¼h\x0015ÿ7%eD¶ÖÎLkÙYZm[JU-å77\x001f\x000fn\x0015K!\x0015
IÇ²G\x000fÉ\x001c°Wt\x0000vÈ¾9{ÿn_&³\x00012-	\x0004ä}\x001aö>óÐ!¶Ü¶z»º&mì\ $ùÛd%J°*±Egt±\\x000bäæ\x0002ÑüæÄ@¾l¹È~¨Ds1ì÷@Ð\x0002Á\ Ð
14,µWl\x000e\x0013ú~&oyü\\x001eZã\x00169\x0002*AeFO\x0005\x0014Z 0\x0017ÈÄ\x000b@uÊy	cSªÑÝîõ	\x0014[ 8\x0013ÂM|÷\x0012=èÍ\x0011òz×\x0018Î\x0004J-P+!ex\x00043\x0002é²:\x000b%¤Ä¿üô¶\x0000¨ñbÔÆyZD×±+\x0003PÖµ \Ð\x0002´T\x000bé^OÏUÔôÉ@3PÈ\x0010]z¨u§¨õ\MMíø©xTF+1\x001dJFSSzw©bÔ¦ÖsUµ+·½È\x0008u\x0012g\x000bd(/m\x0002ZüÕ:Í¨çªF§¼X3ô5E7RÖX2é[·\x0001¢N\x0015é¹ºè$ê®¾{÷mòÚ\x0018§Lw¥1ÖÀ©¥@¦»jfîU³46¹øDÔ@ìóUCFÆ]wîMûîfë®ÝÌ\x0015\x0012Ô¢`,#ÃWMñJ\x0011$å¡w\x001b¯Ã`¾¾ùôxÿ¼Û\x001fþípÛHpÆ¬\x0006\x0007
­	q÷Ó}}ööÝÕkrmÏÿ¯§éLKgÆèVT¥Ù¬¾¨\x0003zÂg<3\x0011\x001cáÙ\x0016ÏáA¢­ò¥dO'¬!^ðtÇð\çÆðh§;pvÜxj©Ì\x0019ÆÄ\x000bËHç¯Å\x0016\x000f\x0006¥çdmog¡¾i\x0018\x001e±\x0002Ï·x~\x000c/b\U6\x0010(k5L"<¯Å0\¼\x0002/´xaPzè"GÎ\x001b)(\x000bjÈEvõìÁÚ\x001b[¼8xöÐ\x0007,[`Pzydc>{àªôÖ~ÛÔÒ¥A½b\x0015¯V£÷\x0007Ñz[fI¯L$\x001cð6>kVÊjPzÖ1Äç$þ\x0001\x001d+ßD8Æ×\x001bQ«!\x0015`)¿é[~.°õnðH§\x0015|ÙÐv#Ðp~¶j\x0018\x0005ágdyº5Îì:\x0000c|bÖÙ§@1dáË¡næó0n"\x001cãëT\x001eÔ}ÒéN7PÙl©\x0008÷C8W]Ýé\x0016=¨\<íª±Õr¨Âg«Ã­4l¦»¾fðúz
bxiº¼dÀd;¸2i­á5½W5x=(CÇé\x0015G\x0016NÐùgvÓ=cxÝí0·ÒcÀtÀÑI\x0012\x001aÚ²®»\x001bfðnÐ\1ÖÍy*\x0016\x001b^¨o=_w9Ìàå\x0000c%3D\x001f\x00178w&ïí·RõÙînØÁ»\x0001x!X5ç³Ç¯8FCå[×]
;z5T-ãÈÒã,¼ð®ÿ¸¶»\x001avðjP~¤Þ\/\x0003}RÑÌÉ¯¼º¶»\x001cvôr`È6Åf©e­Ysð
ïÍ çRßql\x0008r{e\x001b\x0015%æÖú¥[£4áÙ±k`8æPU·èÕ\x0001[O\x0007t@K6Bµ¼ÑrÌ\x0006©Æl=\x0003Øz\x0004Ë«öäîÓÉùÍÇÃOty°³\]EeàÙi¶`\x000eDãTi}~¶æn\x0003fZ03\x0000F³²ØbPg<GNIÅ\x001cZU`¶\x0005³#\x0012£º#\x0018äá\x0010YbFÉ»«Ð&\x0003`®\x0005sÏHbÐÁ\x0008Xò\x0014jwþZ\x0013êR0ê\x001c\x0000\x000b-X\x0018\x0001\x000bUñBHes3­	\x0012Ã@£\Ö¥\x0016,Ñ%®¹£\x0006'\x0018TmX·\x0008LÛí7s«¶&aß|¼KéM\x0019^Az-Ð½\x0012ñØª×Üd\x0015\x000e
½¹zýîb\x0008Ù´Èf)2u\x0008®®\x0000°»\x0004\x0007líRbÛ\x0012ÛÅB¢0\x001d$'´9£f»è~
2´È°XÈ*Ò]ÊÈf£â¦Hsºvf\x0011rhÃbdÃ#\x001f\x0008\x0019ÄÁ\x0006Ì8Ø\x001aåUzÛRëzõÎ~|ª3Zr9)\x000eø\x000f¤\x000b»Kxöå¡v
dZ 3\x0017\x0008BÍó¢æÒzçk.k"Ï;\x0013Èµ@n6P,ÓËHBã_íä	ÒXKy å¹<4Ð\x001dR+¹4íA\fmw¯ÀL\x001eßòøÙ<ª¶¥j$j¤é\x0013¯Ö3B\x000b\x0014f\x0003¹Ò\x001cI\x0015Xê\x0000ùÑZ´rtlâl _+
¼\x0017k¦¹!2\x0017,\x0006J-P
\x0004eÌK)	Z\x000c/å:Å]Gs\x001eîµÐl5DÕåÜPç	4\x0007ÒMAÏ®9÷Ö71V¾÷7sU£¥oUn\x001alTc}Ð\x0013ÏÖO1¹m]íTß-úâáóÛ¿\x001dâ²\x0010ëq¢\x0015Wåë)U¿Ù*{ß4\x0013¾¸~ÿòâ\x001fÀÛxqËûv#-\x0004\x0007"?'Ç*k,1iS42Y®Fï+Ú¡¼\x0013AChZB3N\x0018j]\x000b\x00064b7Ja¢fc\x0014Ñ¶v\x0014\x0011/£d¾tÔmÆ:#Ò\x0004·Õ®EtÃRD¯QjÌ²t$úÒz2È\x0019C\x0016\x0011¥Æ2\x0015[\x0006@sUNð¾@b>¢o\x0011ý0"Fdº¶X\x0006Ï\x00190\x000bµÅr½\x0010CK\x0018	ñ¶\x0018®'B¯[E~ß)»\x0008uJ\x0018­F-b\x001cÿÎ\x000bu°Râhw\x0012_\x0016·Zå4OÈ±kÞ-EWº\x0013m¨Uõ<\x0011¥\x0018ôzÆN-êa½Hö¹\x0003:QË\x00103zÍ\x001dÐ\x0007¶/cLÛÆ%M\x0018Û<¢î@¸ÕX×ÔHIÁU»\x0002\x001bÈ×\x0007\x0006Õ5¦ÅÜäÓ¡ä3©ÛÞiQ=:\x001cúÞs1m¹ceæ`zI!k'Ø@\x001fZì9¨!çbº\x0016sÇÒÌÀÄ©O¡bL·K¥­\x001aý®ÍvúÊt~\x0019Fú\x0014ôß||<\x0018ìg7¶\x001cMQ\x00087$jñÌÀlÙlñÌ0È§xÿìõ»Cy	³¯2ª\x001då1Ñ¦ yy;¤X\x0004Ì\x0019À°åj/´-¤\x001d\x0017$X	ºi"$\x0001â¦Û4­gt-£\x001bgt5ÇëiR\x0010×üËÛ\x0015¨­6!FµOU|êÛÇ'ïlÞ P
µä#u\x0008^^\_¼{â:oçLÕ&g:\x000f+Ôç4*24\x001c\x001bÈs³h$Oe[*;@¥\ÙsHÂô\x0006St ÷"¬ÒÇùXÐbÁ|,\x001f#µ~\x0017a©\x0005®6JM¨æùX¡Å
\x0003X\x0018 kÉ\x001eäÙ]ìSK¬>êZ¬4åj©¥Æk~ìNÕ-Ha70\x001bK÷\x0017qà&Ò ]±8Ô´ö4?|\x001aKo?Ïêò<[6\x000b¼ºyøéóíÃÝãíÉõí\x000f?ß|þ÷js)}\x0012ïÙºZu\x000e[åyeÉÀ«³ë¯ß_\_¾»8¹¾8ÿæìýÿz\x001a×¶¸v!®æùbTËê¤Ã¾\x0016Ô­b®å°ÐÂÂBXÃk\x000fKi+wIÛ §*\x001bZÜ°\x0014×qç!¨s'$\x001e
ywÓvµp·\x00138:ªÝdè\x001a	>èÇ óÂMÀù\x0011Í{Bépk2Q?Q\x000b=C²ÁOcú\x0016Ó/À4\x0014G±H£þBÍ-¡©ñ{|Â¹ a[\x0011¬\x0008ÞÞ~|¼»}¨3Êîï\x001cR\x00167yE<\x0006u4T»`xÐôíÅëw\x0017×uJÙÕåÁ1euúÆy(\x000elÝiðâ\x0003B\x001ejì×\x001aÃ\x0000¾ûÆ\x0004ê»¢\x0011]µ g{@WÝjðâ%²\x001djíÏhÚthÚ\x000cÂÕ!fÊçeØÄ¦i¹M	QüvOú\:½ýÂ§õVÖ\x0018où\x0003þWð\x001f¼2è}q6\x000cPçQQZv&çpûÎ"^ñë«×¯ñsïÅüw\x0011FIå¼ \x0016\x001a\x0002ñÕíÃ/E÷>Ýýps`
ö´T¦T(h
H\x0003Ùq\x0008øK\x0010¥s1u\x000bùÕÅõ«"Æ«·o/ÏÏödÓÙ7, ^õ\x0007üOßýzS¬9g{4Ò=þí®ï¿¿}xÄ¿z\x00125mÔ\x0004;=4~{ÃãV­bÐßýïë«\x0017\x0017×ï²Is}ùúüòÍÙ^£Þà\x0016ÏáE­x?XÃi\x0007ÄK²àË*½\x0016ÏµxnPzÁÈÚ\x0014*µ'*ÂsG@[Ç­
ËñRÛÇÕôô ø<mÃá­.è\x0006eWM«äëÖsÞUµÏw|~OÉZ]ðÊ\x0019ò \x0013¾eðÊr¾Ðñ1>\x001a9Æ|TKß\x0003PC{Y¨âÁ®<~ÜJ!|qÏj\x0011äÓ ß7\x0006+ëÏýÚïË­\x0014¢\Ô ª» iS;ÍB¾xMN0våõ0½î\x001bT~7\x001eQ³`KÍË¶Q\x000c¹ÒJ¸îîÁ»KïÉ<§;:®	Ô\x0011a¼hÖ~Zèð`\x0010/éÓ²o\x0017-oÊ¢ià¹,\x00003q­ô:Íb\x00065CÄ_7ðH<äÓ±.®ôk^§YÌ fqx\x001d,k\x0014KiÎËQY~\x0016Vj\x0016Ói\x00163¨Y\x001cF¦¬%´«OâÓo­ø:»k\x0006
¯CÃ¦äóúREDx²ü6òÖÔE|íZò\x0007MØAñÑçpä4¼Á¡oOÛ\x0017\x001cÂÚÄ+]Ñúòø¼\x0006®øö\x0014\x0019í[Ý ¹\x0016Í
 Ñ+léßAët)\x0007ÓÊÛ ëÔ\x0012ìÈm\x0008
Z4\x0018O\x0014DæeR\x0018«Ó#\x0008JÍ9öD}\x000czÔ´nÑ´\x001eaK¨B|Ù\x0013æ.CÑÌòez¼Q;ÚnÍvlvMG\x0019.L\x001e¼)Ã\x001aUJ¶ú z×
±uT|SC5¢lÃÈÿ,§
ÄüC°ë¾hèÈÂ\x0008K^ö
záÈö!È\x0006?oÕÊ;ÊedõÞÊM¶Ùû20\x000b¿)D³c\x001dæÑu©ò\x0007ÝÃeÙËsûxÿÃÏO¨`KáuATº°BÄP5çÚ\x0006±¾hý<\x0017ï®ðOfµ-«]Æ
\x0014JY,oJß¦Éõl.<¬u-¬[(X`e\x0003Ô¥bE²\x0012¤­VÃB\x000b\x000b\x000b%x48gJ37TÖÁi$XßÂúÅGÂ<ÎË±d=Yçw|ê°±\x000b%«$vr¢\x0000¸¯(Öm;½\x0014RÝ\x0019 ÿy\x0011,M	áEH4¬¦øc\x0000\x0012(»´£ê§yë<ê½¼ßýyøÏË\x000eCnb)ÈAbg\x0008â#ò\x001a ¾ûí'ÿù/ù8ÐK"ý\x0007ÞÁ
BªOî?\x0012Ç\x0000YñHq@¨²7éÚÅ\x0004·}^¼}{õúkÚ»;=¾[}\x0007ùþ/ÿ¢s^\x001aþÇËXÝ÷÷ÓÚ2zpÂ¿\x00169SB\x001aÿ~§×Óßï\x0013+ôü×S¡\x000c%R÷\x0012ükxøÛ¿ÿ~=u!Ûí)ïÓ"P6p÷\x000bºY.(!XBèCÙvÍ\x0004O
1WÛ\x0019RU3¤=t{Qh9A\x0002ásãDÊ(1ñC\x000cºÌÐ|Íî¹½Ça+\x001fªj>t\x000eµüÖâ­õTÃa\x0002×{\x001bC\\x0006ã[\x0018?\x000fFóy\x0001CáMq\þàdÜaB\x000b\x0013fÁØÚ²N«W¨\x0000?ÃHY\x0017Ç|%¶,q`\x0014ðP'îma±\,\x0001Á¤\x0016&Í\x0013\x000cª\x0010f	ê´%°\x0003(\x0011GQX2J¿\x001bó\x0000Kâv
4O}Ñ,Q)ùHÆ/;¾\x001cÓ	GS\x001b5<?ÊK\x0013¹þ&.¤éÔ§gÆò\x0001N*\x0015\x000b
\x0017\x0001zçÔ²ÛÄ1¥ÐØy4´\x0005»|)ê¤
åKIù\x0001í;\\x0008Ó)==OëÑ¸g]Î0þÅ\x0014Ù\x0012çõÒH\x0016aè``¦d\x001coBñ4\x001bC¾\x0013õØ³h)\x001aÝi`=O\x0005ÓXeW\x000eóé´Iïyë¼Ye	L§õ<\x0015Lo·sæ%ñg\x0012ÉD·ð>u:XÏSÂfs»i9\x001c\x001aÇs$<h\x001eQ3LÓ)a=O\x000bà+
½%±l<oÄÂ/¥\x0017ÁN
yjØØÈ-\x0005i@ñ"¼6rlª\x001aÓ©a3O
\x001bAóùCY¦1\´K\x001fj!MïíÍSÃÆÈh\x0008ü\x0003ù7D\x0003Wx\x0011\x001dbÓ©a3O
\x0013Mä\x000f\x0015hÁ\x0008ÃÔ\x000fei>Ó©a3S
£¿§X4\x0018æéò¡0\x0016e\x000f<¯(\x0018¦éT§úðOÉÈ4\x0010Ê*X\x001açQM\¦M§úÌ<Õ§æU\x0000´þz\x00043\x000c(Q6Hi:Õgæ©>¡\x0001[\x0005¯µ\x001c\x001b\x0017$Cçká\x0019îT§ú´\x000bâ
CÌ-2MÒ|l¼öËít§û´S<ÆSÑ)&ÓE¦²Yf\x0015l§úì<Õ§LðC)d·"Ã\x0000oÇò^¶ª
ÓtÊÆÎS6vï¹B÷ã~T1¬ú^oÛ)\x001b;OÙàMëM-­ºèa+#ä3í2Îé³ó>å¡äJÓg#7¿à-\x000c/m§úìLÕÎ9g\x0001¼®Î¹ÃÀS]f1m§mì<m£èÝ©¤j¨^±x66)ùP^/\x000bvm§lì<e÷{Èé\x0008Ñ7Ë4V,f0vÙr²q3
Æ
¥\x0013\x0003ÿ?¾Ü^r59ì]Ò`7ï\x0004kZmI"^sg\x0019Fst\x0019õÂ\ë\x000e°wUJ<®Þ'+s¦\x0011%lZæ\x000e»î\x0000»æR\x0019ZQQh\x0014uß\x0015\x001a4\x000bÏ\x000ctg\x0006æ\x0019>p©cõ)äqïF_C\x0019Ñe4;\x000cóÜaÚgQbîþ+(|f\x0010o\x001b\x0001A\x0006!:\x000e\x0013\x0002þo º\x000c#kÿ|Jfyî\x0004ÃL\x0015\\x000c./N
ûÂ\x0001ÿ\x000bË´^êü4×¨iaoòj¬âG¤j\x0010â\x0012US_ê	V3\x0003Ìº¸\x0003¨(Z\x0018C:qa5ýêÓú5u¿ßÆ·¡?u,k@¢zör½8~aavÂèïn·ÂÞÛY\x001f-\x0004îðÈ$UÀDÉ\x0012CZ\x000côÃ\x0016Ð\x000fó¾tøây	*¦\x0012üÑd!ÍxÂdû£é4÷£è8\x0000vôÑ87\x0010$EÓÒh\sYÆFF7óR'^R'úc9Ã8x¬&N¾ûq\x000bçÇygÈÈEs6Ûr¬È',ÌÿOfæ~²\\x000fâù\gË\x0013¤bM\x001døÅ2ú~KFßÏË/in¥ó´Õq"Pò9f{Ú<@·ÊñÏsÓoÆqV'Ï¤àôhGgF\x0005.\x0012ÚØ\x000erxZÂç\x0017÷wèIüÛ»ÛÜÆ7EÁyÉ²C Écù»i\x0015Ê¸\x0016ÿ×
U\x001eðþäÅÕå[z\x0006ÿöòboó^ÃgZ>3Êâ)ä³\x000e<6(|]{*5Y
h[@;
\x0018¸\x0000\x0005Ñk`@à©ã\x0010½µ®\x0005tÃ_8ð\x0013\x0013¨¥°\x0000ã7'_Ø§µÐ\x0002Â°\x00045?ûC°ó!\x0018èóô\x00012\x0002l\x0005 o\x0001ý0 â\x0014	Ð,0+A\x0000\x0001VK0´a\x0014ö°\x0004u`¿Tc,m\x0018Ð¬æ-_\x001cæ3õÜáZøðYçÖ\x0002¦\x00160\x0002BäaÚø­
µ\x0011\x0016@n\x000bQ¯þÂÍÓyW	5)ç\\x001eD\x001d\x0017©\x0010J¨`í%Ñ½!\x0019¶$èþÛ¦\x0015¡ \x0005L6¬%ìL\x001e¶%Öòºv@§¦§	N3ä®×k	;[¢@è/åÆ"CÎ£\x0002os|Ë\x0008;c¢­\x001b¼ÔAÊ'Rà \x000f¨vµ¹ëÜÐlòê:÷ùVOóZK*ðä÷Eêu`IÆ®k3l;^aãxý÷üçáB¿DõÒüu\x001eÛ\x000býx¿%JÐnqb¿'qLcæã\x0004ÎÊá\x0007M4«p@)¹¶4Ly\x0019mì\ \x0018ª±È\x001b+X>ÀÛ6Q¹è¥@®\x0005r³bâ\x00116hç-M®Ì@\x0017Y¢ÉuÛªw.\x0010´@0\x001b6Ì\x0015	9\x0000Ñ´6Ã\x0004i©|Ëãç\x000bH!Ó@Î°|0Ïuh¯Ò¶JË\x0013Z0\x0007uTy²Æ *oÍò	\x001c2à	Zú½bË\x0013góxÅãµ¨.\x0016\x0015ù_xå\x001b"4>Å\x0003dO/\x0002¢\x0019Ó\x000f8´^©'HwWLÏ¾cÞ\x0006ôcñ`-h9ÒÎl;\x000fsº3¤g\x001f¢`\x001c\x000f\x0003\x000eW\x0011\x0011m\x000f(@Î¹¥"ê\x000e}\x0002u±ä'\x0002 ½J\x0017"Ù­î×R½hºcdæ\x001f#ÊÈ\x0017KF[,ä\x0018\x001døÿl»õsºcdæ\x001f#%å!@ÁÙ¢ùò,#\x0003ÃÇHµ«Ë\x001f4\x0013>ß<|.^¦<Èvm	ø\x0014i8»vÓ+Ô¦ú~ÿÈ¶Dv.\x0011% ¼Âi$
%Q¼¼4m·h>\x0010´@0\x001bH\x0007©¢ÑASóH\x00063âÆÆíS4\x001bIw_MÏþl le"ëÏgï
ìÜþùL®cr³Lí RX£\x0017ÎÔ\x001bå·Íì|&ß1ùÙLè\x000f,+¤¦\x0013\x000fQçTTÛ÷m6S[ä¸Yã9ãÊ\x0019[1@\x0010Ï_\x001bnP@ç(nÛùL½\x0016¯\x0006\x001c\x000f{Â8Ý#CAâ-\x001c@\x001d\x000b:-`f«\x0001OË\x0000yC(:X\x0019IKÂ^¹|Â|¦N\x0011Ù]Uñuü$OS¼ÉØÅ -ð:¯a\x0006eV8~¥tÊ\x001f'y¥vLî| Ô\x0001¥ù@ æÁ ìmkéäÂb&Û}8;ûÃÑt$)fÏ/Ñ4\x0001®>"¤ÅWÎvªÉÎVMÞbdTÄd4WK¡Ü9c\x0016[^Û%;ÿ,Q\x000eß2h?©f5\x0010I/¿sm\x0011\x0017ä"®yL\x0014þslB{Ôtð_²\x0011\x0001\x0016[\x0015×ip7['ªÜçD¢á;çÉßá\x001c[|\÷åÜì/\x0014\x0000-\x000fà\x0008\x000e\x0018\x0002/v\§\x0008ÜlEQ4\x0006ç%\x001e°²\x0004"ì<<Íf\x0002Ý2-§À\x0013A!Ð89Î%%-oa&l§Ñç#u\x000eæ\x001aºA;ï£Èii6*^j\x0003éÓ-V\x0004Ð{¼sõeTÖÔ\x0003®åÉÐ{éôv±\x0006÷âg;(\x001d7\x001d^mbÐò¹Äiòj+OêUó@}þóïÿÏãm\x001e1Ý\x001c))Pª\x0017©\x0018¸D*ºö9E:WÛ)ÜóoÎÞ]ìÑ@Ù\x0016Ê@\x0019)³èòR«\x001fÌé\x000fw\x001fb¦JfKT\x0018D·\x000btï	êßs;FÁW\x000f¿Ü<\x001eðÊÔÞ+JñkVèEï¦whqà\x0015!þ¯Üß~ruýêlßpÖ\x0006×´¸æÙãÚ\x0016×.ÅPcCÈS\x001fË{z
Û±\x0005Ëp]ë\x0016K7ñ£\x0017âZ®ÊÓJ&#®ÞqªáB\x000bq\/ÚÁdø0H?¬±»!À2ZßÒú´Ô1\x0011\x0003ÇäÀ
~èeJÉ£QnÇà-Ã
-nX«\x0015ÅèE¸ê4\x0015áâU«g!\x001céèÆ\x00167.Å$5\\x001aÃUÎ/êZ\x0007H±ZÜ´\x0014wSÿªñ\te·¥Yóki¬?\x0019	µ\x0014vÎðM£¦	ªbÐaÇ-äíÚR«F¼ §Ás©¥ÚYÇÝài\x0019ngÔôr«VÛm1\x0010ªuaµCFw
®ËxÕ¶\x0011VM}Ý«ûÏ\x001fî>îå³ ÃÑid\x0007SÌ\x0005~3y`çUêýÉ««÷//÷Ìnldç"¡P8ÿãt¿4o[iîL;\x0019ÎùHÐ"Ál¤àd>\x0003Pÿ4H¯½Gï$[æ\x0013(Ì&JÀÛÎQß\x0000?n*r;¥\x001ay·\x001er\x0016QW÷d\x001aÔL(÷?\x00141¹ZÜjDSãçÜ{öWÿ\x000bUSrêÌ§¹GÊ\x0006á¥\x0003ß\x0005)\x0004\x000e;\x0006z¸ô¶³®;gýEfú´7H\x0014ÍÈÐ\x000fÍ»2!ÈÈÝÇ·'/2Ô¾%P
i©Ì\x0000Ut	Ê£H¸ÑÄÊNø2³±legc\x0005E	sÇÓc\x000c×§Ð*\x0011YåZ,7ò
k7¦¥\x0011´å`\x0018+ÖNÚlÊ·T~@XxùØ{¶®6ë[+±M~ÂèÌÆ-V\x001cÀ¢Uè¥
Ò\x000cnÙÉ.ÌÇjü!ÝûCOr¡vgÍ¤$ÅlVBínêsª»zþEDª$³f\x000c^DÃ­µ2\x0006²êË©ºk¨\x0007î!ú+üî@ËÎ¤xÒ9Q\x000f´»d\x0005Ww\x000fõü\x0018T¬^·AÁñXMç¤µiç	r\x000b:.\x0018µâ_\x0019j¯ \x0017Ëv×Ð\x0003*Öò(\x0004\x0003µQÇYi±²¨|\x0019W§"ôÐÆK\x0016ÈX®·Q\x000e8ÃâZ¡¸L§!Ì ÏÀ§\x0006¡\x0004\x001e\x001c!CÝðÈ­¸¦ó Ì|\x0017"w¤Y®âZÅáe·\x0011\x001e¹Ýb\x0011cÝUàf]+pçÜIãNeD £åÅY\x0019#
«TÅ6vct)/TÎß\x0014Ã\x000c\x001eÔçm±f§y\x0016ß.Ãõ±_\x0005|þpó×ûÇÇ\x0003}å(\x001f\x0014vâ%àZ\O\x0005Ã;Yøg'ç×gºz÷îP¯ß.Éõ±_\x0000ü4±â[\x0000\x0019qÙ\x001c\x0000z÷
l\x0008Îµpn\x0008.¯ùåhVBñ7UI$gw_1Ø e1Á©:\x0005\x0006oIo¿äYúÆ¿%l¾eócrã±\x0019\x0018\x0010ÉôLë£\x000cÒ\x0013UNCd¡%\x000b_4ÖYÉ\x000e)_t¢\x0018d\x0008.¶pq\x000cÎF\x0019×àPÃäv×\x0014V~ÓÔÂ¥18\x000fbá]¨\x0017ÕÖxO×Á5	=ß4
Í\x0015]àq.¿ö`¢ë¼ÀÆAºNÇé1%ñ.hxGÛ® 9\x0019½¿®S$zPXéó£!p¤ó\x0008FîDð»åvóè`»¥\x00056--·'ç?ßÜ|ÚëTh\x001aÊë1yL52âS\x0006»óR{Ao¢go\x000f¥7aÛdAk²\x000e#ùD³¬xð\x0003M8(\x000e\x0012­PÁ\x000f\x0013\x001fr.\x0012´H0\x001bI%I°Ð»\x0011\x0017ê \x0019a\x000f»~Çl¤Ð"¹H1)	êhC Õq\x0005^Z¤4\x001b)\x0018y¯Ì%øÕßT)­8Kº?ÞsÏ·Îp[\x001e^±(Þ\x0005Æél(½p}æ2ÉÌf×ã__'ã ¨n7/6©»szö¥Ô3Áù{O6(×\x0000 ¨\x0006ÔÝ9=ûÒÑÐ\x0000CèêP\x001aTób\x000cw\x0010g#uwNÏ¾t!ÈH\x001a@yåúäRôÕÉßÉàÏG\x001dR/%K¥	ªR\x0012ß\x001eµùb¦N\x000fèÙ \x0016Ý\x0001PI8¡À×\x0019\x0013Æn&S\x0010ØÖ?ùé|\x0013Õá¦Â$ïSa·b6Q§ÌlÕDýôìMQ\x0017\x001e\x001f&]§³ñ\x0018ó:Ídfk¦@e&,$ô\x0006XF Ê\x0012`·&b6ëÜl$[ß\x001dFÿùÅ\x0005êK°i9ïüü/§ÅsÑ9kôéê¨j³¸ÍÔé\x00013[\x000f\x0004´¸üØâ+Æ7¦\x0018c
\x001dÒr¯Iwyì_nÒ6O:OHbsç£D\ÆJÙïÖ£Ì%SvËë%o³uÉ_ÞÑÊßÿk¯ë\x000b¨ÌyêADÜò\\x0006°RÓív6È%yI;e\x000e\x000e\x001c²[é$d3Clä\x0017\x0004n;±yïUéñÚîdõdVd6mÙìÜ@ÉÜ¡úÂðH\x0010#s\x0012LèÒ\x00116hÙ`M×i *ü,w¤q\x0010Òn_ã\x0018oÙü ÜtÒ\x0010M-s@\x0002+|e§s6³ÙBË\x0016Ø\²æ\x0008uÏG²*Ø&ª¿GÐb\x0016ÇÐJ7hfóõÕ#mZ°d_ÝR¶Ô²¥16\x000cÂìæ¸ñ\x000bVr:Öã¶JníÒ\x0016º±cpÖKHôu¡BvQH°ÓÜ?\x0006×ëÞ1åK)$J$Ê¸è¼*TNÜ*¶N÷ê1åëL¤÷÷Âæx¤P?ê*\x0015¢;Õ«Çt¯SªÞÓ(c4Õ,Ànáß\x0010ëØÜ\x0010Ëæ Ö\x0012U\x0015ÌmÙ}\x0006\x001cBë¬\x001e3\x000bÖ§ÚyGÏo\1'\x0010ÐN´qÀuªWéÞ¼Üá´>e6Pµéu:ç;Íôlf\x0010ÎëÄ¹
\x001aõuj³©ÜSÊZ¬rDúÁ¶{¯ü\x001f¶ù	¶|Ì\x0004m±Ø·w?}¼ÝÿXIó98r±ÚHe\x001d~N¦¬*\x0007ùöòë×\x0017Þ*Óö\x0008\x0004mQÖSPhèKdnUÏx4U¨L\x0015ÎÌe	f3\x0001*µ µ<JJè¡vô\x000c0)ÌgÂðÐ\x0006£sïäPÉÇ³»ÏD3 tØúxdø6\x0017¦düôáîÓ¡\x0001²uT@eÁóc­ªãòwßçO^\|ýòòí¡Î\®årc\&Ûe.£h¤\x0001Á¶ÁN½
Í\x0006ó-\x001f\x00013Zsbô©dÔ6\x0004¹>î\x0016?
Å\x0016,\x000eI\x000c\x001dm®e\x0008!I}+h%//1MhÖ¹`me]è<Ç9du}\x001bÍñ¼RIº{`ê%íi²¸ýP\x0015ëCÕ×7\x000f\x001fïn\x001fN^Þþðáöáýæ6iÈP:©PKä¶¿å×g×¯//®O^^¿¼¸>\x001aÎ´pf\x000cÆµrÐ¡ØJ\x0015êÌ\x0001£ÒJ<ÛâÙQ<ÏW\x0014©]Ç*hÑ \x001bã¹\x0016Ï
â¡ê$Fî\x0003âÅ*½pÐÂÁ \x001c\x0006¡eg&p\ªó-ÜÚ\x0017Z¼0ç\M-eÄ\x0019O{Á³1¬Ä-^\x001cÃ£éôñð\x0010r\x0011qr²F4Áux©ÅKÒCÿC\x0011\x0001´Á\x0007û'\x0010\x0013AÝ\x0010ëð\x001am\x001c7ÓÞfÏ\x0007\x0019xb|Òâ\x001c©¸]L3\x000c×+äAì,jJudÔÃßv;´\x001aæët²\x001eTÊÎÆMrm1ÈÊ.½3\x0008f¯ÓzzPíÑ¶ÖXòöÊZéF¶öòéíg a¾NñéAÍç\x000cÈÊ3E$Cä}\x0011ýµ|æÓªÏRS?f\x000ed:-;rñÁB:å·³ø¾Ïâ¿½ùüéÓÍÝ¡m#û ¨\J}\x001f\x0015ðdOf\x0007ß½ûöìò`ðì·ì-e\x000bÆØè]-2¯[<5\x000fþA¸ÝÖý¹pi[p\x0004wþóí/w\x001f*}o>þtûp\x0000\x0006\x0016s¥4úÅ<èÆËÉÕµ­OpþÍÅ«Ë×LI%¿g¯¿¾¸>\x0000ú=m¨ \x0004Hñ\x0005y¸¹§þüþá\x0011Q_ßþú\x0001Ïà~oÔ\x0005ÎÆZ­÷µÎLíÂ°ó«ëwÈ÷úâÍK<Þ9ù\x0017¢²ñ»\x001foÃ_>ýJn;\x001dü(®Ç»\x000f\x001f²¬Êl\x001e\x001b	åãÝz{s÷ññÞüþð\x0019b¡\x0016\x000e<²ÌSý*~Ob>|DÕ,µ×/OÞ¾;ysq}ñ\x0005ÉììÝÙåË{úth´»1ÿc\x0014-àmÕ\\x0019@]¬@pÎÕh,ÏW<\x00087ù5{8MpúÂ\x00193Ï\x0014Î\x0012\x001ds\x0018ÀÊt¤©âà¨¼oæµ\x0015gÎ\x0011["9'Ó\x0017\x0001#[2\$¹(kÑtíp]!9 8x¦pàâ\x0012¸HSêJÙ#ÐóV\x000b2ÒÃI@»\x0002´] åhÎ âµ\x000b\x001e\x0008Îo¦¡*³^Ï¹ï¾/§îûgùeMÙÔÍ\x0004ýË³T*î»"Ãg)C
_ZÀ´çlºWîT\x0013XKpMí«\£\x000b}®Òï~,ªïÇgtú~»ÿðù§ßÈó¤'\x0016hGÎï\x001f\x001fo~*ÿ'\x0001U¬/èAç
r¥@q½'8c'>p3\x0010äÝÙ×û\x0003òá_ÿ\x0012ÿåî»RhYÊ+ï??Þ|yûëÍÃãí/·\x001f\x001fo>Üø\ù$m´\x0018bGg£\x0004\x001aspÔ?E´¨«Ý\x0011¾¾zÿxß]¿»xuñúÝÙËüW>EÍã\x001dêPÅèx\x001eÑéæ¾\x0017gÑæP\x0011À©õÖñë3ÊOèòaôGóù³\x000ch_ò¾ºÿüÈÃÌsA]®:»;¶Ñø,iZu]r2\x000e­Ð¤ù\|uõþ\x001aãë\x0003'ã7õW÷áot¿èå¼ýüPr÷?üLqÓ<±FÃó\x001d\x0015¬ ¼s\x001c\x001d;Â\x0004çÛ÷×Í?ÿ\x0002¨½´-wÎç?Ø{oZ\x001eañÔI¦'_£yro 9}åÚù$U\x000e.Á\x0001ñÊµËc\x000e1æ:Éÿ¹§i9Îï@¥Á\x0019÷P\x0006ä\x001f\x0012%@tIM\x001dë?Ä¶?dBõ-ù!4e\x0015!½"J;ùD)×9æ\x000fqí\x000fqGù!:y^J7êy(?\x0004$PqQOx´k\x0008´?\x0004óCbº\x0010\x0002íïÌ?Ä9YPÓ®Çü!¾ý!þ8?$Ôä6m{R|Ù­ª?d*ÆXûCBûCÂq~4«ºü¼5&ÿ\x0010Í-¹Pr\x001dówÄöwÄ#ý\x000eW×B\x001e²R~,¹r K\x001dùCRûCÒq~\x0008Hc9¢!Wù(+Ú\x0017æxo?D«Î\x001cª#}\x0012-uÁ\x0003U
_äøpü;¢{Ã~\x001cËNA\x0015ö iB9\²ÇÏME$kHgÙõqL;í;á\x0017Wê,rüClraÊµZûK:Ó®cÛuT²Eæ³!©\x000b\x0000\´ÀÙêL»>mGÈ$NYÄ\x0018o\x0011ugÚõl{²u'lLôzYªãT\¼öt¶]\x001fÇ¸\x001bª1äoRöï\x0015¿Ñ»U×Á\x001fótÆ]\x001fÇºS*
9ÊÖ$Ê\x0012W¨ÏÈÇü%y×G²ïT7ekP\x0012ù@õSÒ\x001fñK:û®dà«é¤È\x001d.¿ÄzO\x001fîÆ#Ýø`¹T\x0018­I¬ñ\x0001YY÷\x0007ØwÛé`{$\x001dLË\x0008Øw4ô¾\x0013f©:ó %fÇü!Ý}·Gòæ¼=£ó'>_bDs¹?ÀØî¾Û#Ýw§yÜ%RÁIýÎ©ãß\x0012ÛÝw{¤ûnAðT\x0006I¨k\x0014íñ\x000fëüyw$òü;ª-¡9ò;Ôñ#,×¹óîHî¼	<\x001d\x0014¿Bn\x0005-¿dóEÒ\x001fðK:Þ\x001dÉ·ñDj\x0016*¿¤Xî\x000fø!;ïäÎ#=ïÑ\x000cÎÑôrID½îø$}ªîX¶Äònâ@\x001dR¬£lKÃðýø^°ë¬»;u'£\x0018&¬¢ù\x0003­¢ëüyw¤d\x001dØ¬¼â£ü\x0012Ù>ì¼:~Ôë:ûîdßiH#Û\x0012\x001aÝ(:¸~\x0013\x0003ÇL\gßÝì»APøKrãFþ%`Äw¬[bùK:ûîdßiu+{:7æ_²I\x0005ë?ÀÎÀÃ\x000c<F²àM\x0005±`Ðþø§\x000b:\x000b\x000fG²ðÊòÁ$_\x0007Fö\x001e:ÿ\x0005#\x0019xU¯Ç\x0008ØË/©y®:Ùö¿¤³ðSu\x0008\x000b~I®J`Õ¥\x0012µ&rU|\x0013\x001dÿ_ÒYx8§_â¡þ\x0012QÂ*Ô\x001fr|\x000b\x000fýcÜ,¼òõÍD\x001byj\x0000\x0019RD:ø\x000fø%#Yx­yâ-þ\x0012Oõ$EsÉïpÀÑêì;\x001cÉ¾#¼h`£©§§ü\x000eÙèL<¾§\x0002}cÙwÃEøK|ß¡æì\x001fð¥Òwë_äþv\x001cÿÑÔ·\x0006\x001aÃ¾JªÏ?î\x0016Óº
\x0015*SëÆ¼¾Ç¥½P/ï?ÿ:¯ö'ÔÝ[Ùq4¥fMÚuÈ²ïû\x0001Ôðú
ÿ¶D½¼zÿfýOE7-ºY\x001etX\x0006\x0005ÔÙiP(@·WK-·-¼]	\x001f«\x0005\x000fÎH¹\x000b5\x001c´aïÑY\x0002ïZx·Vòè;ÅP
\x001dð©ñ²øó±\x0004\x001eZxX-ùXS#4tÆI\x0019i
ÄõÞðu	¼oáýZxz·ë<nÜð½IÜ%ä¡%\x000f«Éý©\)ê8ÎìÉÔº£¢Ç\x0016=®E7¡æ L\x0014E\x0003
Bu#ªhR\x000bV\x001fwÙá\x00036¬³à£ãàÇ}S0­ZKo]
\x000eìFôZV£¥Ú\x001b°-¡ï\x000c^k¡¢Íã%SVÞÁ¾\x0016\»ãÊ¾Sòz­Ï²wõÊFß<âíOÄ,ïô¤^­(Í¦Öö\x000eÜÙZ\x0007²?\x0018[Bß)\x001c½Zã ²ä\x0016þ\x00017¢-åu^\x001d\x0003þ_ïþíþoÃá\x001c\x0004¿\x001cm) |xó¨]©&iªk©m'Ø×9Z\x001bo7y ÒÝ¸¯_ï>Þey¡$©Ù<°\x0003ÈxC5ÙÿÕLØ:{sIÍÖªÈÛfaa6k!NeäNB\x000cÔ\x0001F<¨B\x0006mËlWÉ\x0019ä±Ùê¼è»ÈY\x0012ÊOµ²-bv-³[Å\x001c¤dÁDØ
)RRÖ\x001fÔv\x0003ÌÐ2Ã\x001af\x001a¯Wt\x001c\x0014,>¬$\x0006}KìW\x0010+r¸ËiFË-e\x0008Î3¢:Öi\x000e-sXÃê0\x001aÚ*VÍY[s0D\x001e@-r\ld»:ÐÀznèqÔ¨Ý_¼=ÆÜÔ\x0007g·u9tL\x0001ÄÝ Õ\x0016ºÈÙJ¿\x0017ØÉ\x0006ØEÐ½EYaR"ú\x0019âzðR]n=¯9\x0005»¿\x0000x¹³(zIAA\x0007	=]B³l\x000bs>\x0003ÌvÖ+Ô3M£çñ\x001e(gGÓ2tào(çcnÝ);½JÛÕ~5ôØA\x000c¸DASiß4ôw½~ü\x0007Á¾é±oV`;%\x0012Mb=íd.\x0018¥\x000f&¥°¿ï±¿_£«eÛ(Ðv9[<hg¤Í\x001cÏ¼ôÂ+÷Qæc\x0002
k+é\x001ck£¼ÒÉ©,ØzÛý×Õýÿ|bâÉÙýïÿßãN¹\g\x0006³üâH\x0005R·Â®\x000bTå5Mü>ÿeWïß¿ëIbÓ\x0012UÄ_¯ðh8©´1GP»`÷Ö\x000c2ÛÙ®aÖ\x001bæh\x0010n2')]\x0008{ßwF]ËìÖ0£ó_ÜR\x0012P	`f\x000e¾2§c
ha
³õ<e\x0018\x0014Å.\x00059&>\x001aQ}ñÊ(²oý*äÄ\x0003\x00120\x0014\x0004ÑÐ&Õ+ü>Ã2Ê\x001cZæ°Ù')	UhUxfBÝcï¢Û«GcË\x001c×0£dXÎ\x0016h\x001fbfÖ\x001c\x0018º¨Ý¾(k9µÌi
séÏÌ)§i'½ýÑïóï\x0006ÛEo"eg#Öó\x000cFZ´HA3³Ù[M4
Ý\x001bÁ\x0015V0)«) $hÊyðû{®E+Ðiol8
ÝÙA½Ê\x0010¢½.\x00035(y$UÀÖHÚîÍæBwP¯°4}PFRíod\x0007'îê@ÂÕÈ\x001dÔ«\x000c!­ÿb9\x0007-®¿\x0005\x00042=øl\x0011tg\x0008õ
KH;9øeQCNe1G^ùê¨·õHÌ%Ô+L!m4<MlVR1+K\x001eÞ\x001cÉ\x0014êÎ\x0014ê\x0015¶0×\x001cr^¦½\x001bÎëj#¹hcäsèÎ\x0016ê\x0015Æ0Ñl¹@\x001c_E\x0010}··;e\x0014º3z5,\x0005·|¦½ãIu\x0016,¿T\x001cè3\x001dd654+¬aRÁ§ÿáSs¬\x000f\x0015*\x001cÉ\x0018Î\x00185ÆPÈ=\x0019:¨Úï#¹]¬9×aúp-¤M"Rù«RK½lp¢ïööBw¶Ð¬±z³¼C-?¯xÎr ¤÷Î@\x001aî¬¡Ya
QßÕÌ?Y\x0016Ëõ¼ZN´>§d:chÖ\x0018CjÎác½Ir \x0001\x0017k¸¿m\x0014º³f5D\x000bR&ü\x0002\x0006\x0013
F®¡qG2¦3f1Ä\x0013!ª#Q\x0015hiç2"gw$§Ãt¦Ð¬1ÚÕ"b\x001a\Â\x0012Èìx<\x001b{_ßF¡;ShVÂÍ\x0003¸yÅSy\x0000\x00171\x001fé
ÚÎ\x0010Ú50Ï²b1GG£Èy\x0004è:w¬ãl;KhWYBoyAT\x0016)G1*\x000ed½mi\eT"Èû7Í\x0018±2f Êác¹I¶3*vQ1â\x0008]\x000b¬ÜïhdÂ ;«b×X\x0015£ê¾\x0018f
MÛ¢+ô±$ÝY\x0015»Æª\x0018\x0000É\x001a¾i¿ìy
ÇòîlgVì\x001a³bL\x001d»F«¾"KZfT»´6Ö(t§£í\x001a\x001dmPyx.± ýaëéHÐ®SÓn¶*ðÂ20ÉHÒ?È\x000cHü«d\x000c]§¥Ý\x001a-m¢Éi\x0006\x0003RxoReö\x000e¿\x0018î\x0002\x0016·&`±4k¸ÔÏ¨(æ0*©#Up,\x001bî:ÓâÖ\x0016Ú«<¿ÊZÑÒÉK\x0001>Öë,[cY¬±¢:,\x001aÒRb£\x001a	åv\x000b;ËâÖX\x0016®´çïÀv®JúXÐeqk,µFæYÊì\x0016èhe¢¯p,èÎ²¸5Å
,\x0011\x000bñ+¹QtG8V\x0008î:ËâÖX\x0016kë´\x001fëäÐ£¸x ÕÞ:Ahè,\x000b¬²,èxðT^Z"]LxôRJª÷w2w\x0005ÖX\x0016KU\x001c\åþ¿\x0008Úù
}¬wNè,\x000b¬²,ÞsÞÀ)YÛ\x0011ÃáõÄ\x0002e5Åõð\x0005:ÊÌè¡B\x001f+}\x0007iU¦%\x001a\x00114\x001aF~¸'§® û½\x001ds£È}yÄ\x001aÃ^\x0011¿
9ëiþdA²*í÷ý\x001deîT4¬QÑÎ8	³\ÒR\x001e¤ÏÌ\x001cí%\x000bº¤\x0012¬I*9ãéå;3Ó\x0008rÞÏ\x0005ÉJÙÝÞ\x0006QèÎ¬À\x001a³òwsï|gUü\x001a«ò÷\x0013´ïÌ_cV\x001c(y¸\x00073Z,\x0018¥ºqï\áQèÎ¬ø5f\x0005tê\x000c4L©t¾©(\x0006ÜØcù¤¾³+~]\x0001{\sfQÉqñ¼9Vùï4´_åúÓ+>\x001b´\x001a±ìóAÿ@*_ÝÞ\x0006ÃQè¾mëïI¸Ò¥ØÆ«)ÌéXïö¾3+~Y\x0001'df\x000c\x000c]é&TuÖ9ZUïT´_£¢Á\x0007z¬/\x0015Æ^\x001aÆµ4V\x0018¬¬Aè´]X£íþNw0tZ#¬Ñ\x001a\x0006g\x00147	¼.ÓÒQUÓc%£]j«ÏsTx³&,\x0004z­/aaÎ·he VÇâÆvÜz\x0005vLJ\x001aP\x001du;h©|MjÐU©T\x0016éµÜe£Þ'Z½©H	ÜoÁéú®|¬2\x001a\x0013¶Ùñï]ÇîêNþM\\ö&îì6;j©Uì·Àé\x001dt½\x000eÝ¤Tß_RàÅ½!Êè\x0006å&÷·-»£ß÷wôû;\x001añû-¸\x001c;¡Ö>UÜ\x000bÑ\x0001;ÚQZEÐ\x0005HG\x000eÂÎA	+\x000f
ÐâD6BàÅ\x0011Ôu4®	{|Ìdÿ^éXN
s¿È%_|qþáþ\x0013Aõpû8«ó)P\x0013CÉ²Ó<?*âDXn\x001f×O£O?q¬Ï_^½%Ú¯®/Þíïyª¦Å40©­,SÒÒ
] µâ\x00079\x0015¦*Ó\x0007!m\x000bi\x0017@FT:Ôðet45À)ïDS%®¥tD	PÖ¢£.FëQDé8ùåôäÛ $´°DôîZ2Ó\êß$QZÃ¹P^×SúÒ/\x0012%JA¡Ä\x000fîXÑ0ýTCÛ fh1Ã"azà \x000f\x0019¹°ÄXhÂLëïxl1ã"i¢¢/w\x0012á`YR³cÌ\x0011®Oj)Ó"a¦</\x000bÓpTDW)''îAÖ¢ÕÕ3¥îÏ\x0012ë\x0013éa{Xi)nÙl«Ö¬àZÎÎúè%æ'j*\x0006çå½*òö@$æÉêx¦±8µë9Ý"PjvçU½TÙT"IJ]gp\x00069mÏ¹ÄT\x0006Z\x000fï«z/êÖ8Éw0*Ï\x001aêVÞ,\x0011i	"U¬äÑ\x000b
7å§\x0012ÕsYßräè]\x001fÿ·ÝÜ}ºÿxòâÃÍÇ\x001f~·NØ\x0006' $àÁKÇUSO¯Î.ß^½>yñòìõù73@M\x000bj\x0016*q9\x001d*SÏ ÀA Ò©÷·QPÛÚe ¾ÆN.D~VAPéj2ÁÓ(¨kAÝBPÇuT\x0018F~KñàÄ[2«äGA¡\x0005 yüv\x0001Õ\x001c\x001aù:y\x001fAÕ\x001e\x001d\x0005
-hX\x0006
ydO\x0006u\x0000Ñî2VøfrÔá\x0018¨v±»õTF±\x0008Õòü\x001bZ\x001dÎ½wÓ\x0018ÕN
ÌD¥\x001bß)¨¢\x0002¾øâÍíãÝãí	\x0006ÉóâyòÍý\x0005¾NÊ4ÓKzí&Ówï.N04~\x001aÐ¶v\x00182iRåNc*¸PUt0)í9\x0002\x0008- \x000c\x0003\x001avÊz³Õ¾jÍ\x0018§®Î\x0008`h\x0001Ã8 õRªz=OóX\x0019p*e3\x0002ZÀ4\x000eHp©cÒè~\x0000\x0017P[ÉÆ4\x0015T\x000e\x0000êþ,¸%4EÛÔ^8.L	1ÔÞßß¸mù5¹åwôØ(ãwUt2Õ\x000c¼ô6E	K3B\x0018;Â8N\x0008N¾2Æµ§²OÏÉ°\x0008u\x0007\x0000Û\x0016S[L5Â\x0007¬ìp@Ã'~ªíxÐtfPG\x0004\x0004y_ÀO\¹aÂ \x0000º\x000eÐßd\x001dh6]QÖQÆ5ùPÛÍ'k?G\x0008»ShÆO¡J{©\x001bñAZÓbr\x0013ñ÷\x0000 íN¡\x001d?\x0006ôÆ$Z	u\x001d\x0004\x0013WÐv§ÐB¡¬t\x0016YujEiA\x0019®S×¶;vü\x0018Z\x000cù#Û@½ÝKj¥º¶Ý1´ãÇ\x001e¹\x000cV\x0007
ÏÃ§Â©ÚÝ\x0001B×C7~\x000e-	®<ª)E¦¥¼|Ël\x0004Sµ\x001cC"l\x001f¼³\x0010o\x00161ò]Iê\x0014¤>ÞJ\x0013Ób!:Õ\x0005ÕYÍ,Ìÿþÿ¼z¸»ýø8\x000b3ïåáJñh\x0008Z¼Áu­Vï_%{òòäêúòâõ»§am\x000bk\x0017Ãªº«\x0010ÐÈð\x001ckå9ÕªC\x0003gÃº\x0016Ö=sÉB\x000b\x000baÑ/Uj¶Ù##ó.ipî\x0011`}\x000bëÃ¦S\x0016¬å]\x000fI¥d.\x001fõ¨¡E
KQ£©½\x001byf«¬üÚ<rv=llaãbXzçá¡¸ÎÊª\x0006\x000c d*®;´g6ljaÓbX\x0008Òoé)Y\x0016Ás2*9À\x0011tA3)-\x0013-¦Ey²óg$òÃºÐºÌ\x0000Û\x0004½Ø&DSaõÀïP²u8²z\x000f\x000fk¶VxåÑ\x001fíá\x00177>Ýâ?\x001foî>|gmÓ2î6¦ò6&\x001b¥GÊisp\x0008õ³·o/ðïÎ._¾<d|ÍÖ\x0012/7káñÞq¯§\x0019öE£Õc(ð©<×rxÛÂÛµðÖÒ\x0008´X4°äëR#µ·\x001ax\x0011¼káÝjx#ø¤êÆ\x0006/J$ê£ÂC\x000b\x000f«Ï|¨ëÓ0\äUX6ºÙñðûQxßÂûÕðPwÓ wT¶Ð"¼\x000bûÄzQøÐÂµð±Î¯ÎñÎCtA¸\x0010\x0014Àìí\x0019ÇÀ¡Wø\x0007Íøç7\x000f¿ÿW^ªóÕïÿç·¹Ûj£
e¼!\x001eyÞÁ^_S"\x001cè&}s]vê|uñíõÅ¡@i+F!pó\x000f\x0004îZp·\x0012Æçr5e¬#¼±®¨m\x0007\x001eZð°\x0012<XN÷¸DcZ8§§$³\x001cÂÞ«óÁÝ:ãÆÖ3þ§ßð?z{òêæáñîãý<çÅ\x0006ÍÎKÎVñl7R{$ý§o¯^¿¾8yuvýîòõÕ\x0001ïEpMkVà&³Ù¹ã¥ç\x0016®0±Ý·h`\x0018Ù·È~9²SI^½¨5½,æ²yN 7ÑÛ=Îì0rhÃ
)G¿sÿêXÊº\x000e:1{\ÚaäØ"Ç\x0015RÖJ*Ç)!'\x0007Cn£÷yáÃÈ©ENkÎ²½\x0007\x001a´À£ú©mBoì\x001b'3¼	Ë²¶PkÄ\x001cäõÞÄyª2½3sÚ7Ïu¹×p+TSZRÈ¶¼ff#Ñ¤
û&A\x000f3wjN¯ÐsÆm0s¬\x0013;ô\x000cê½ëCml×é9\x0015\x0002Q¶Î%+\x001eªJû¦P
#C\x000c+n Ï¯2YÏ¹º0 3sÓÑNFgMô\x001asâóØÜÝ\x0003·Îá\x0011W²j'î[ð1ÌÜéf½F9(¡C®ÔNa¤+³Þ·HeÙtÇÙ¬9ÎÞÈv\x0001>\x0012ï|F\x001b+Ý1i77lPºîâÏIsÌ3=ÕÊo/ÚñE;·N.\x001eî18ë6+É`x"«'¼ÖÒôöç|ß\\_aLxÀa\x0016TÓ¢¨VqhBq\x0015=à:ì_I=j[Tû¬¥êZT·TªNÖK _Éù<*Áä>ØaRhIáY\x000bÕ·¨~!*O."BE+£
!X\x0019Î4U\x001c1L\x001aZÒ°\x0014\x0015-'*\x000cwx_Kéö®\x0019A-j\*Ô(«\x001biâ\x0015ÇEP\x0017£k3U5Ú<¢øfÝÌ(+xYÙH¥Ëü \x000eI\x0016zjµÏä\x0000k§VõR½ê­õ°h±´íS>x¯öN\x001aaí^ª­Ðº²_@\x0005·R#ªê\x0010ÐÉVaÖN\x0007è¥JÀo"\x001f\x001aL/g Ö9û_Jæ°ª¸å\x0005¨Øä[_Þü0^Íä='x\x001eoæLôò\x0013\x000eÌÎyyvþ4 i\x0001Í8 1R\x0010TÕê¦º¯\x0018ùì\x001f\x001d1\x000bÐ¶v\x001c\x0010£EN1\x0005­¹ÅË\x0019	Ê\x000f¼æÍä\x000fùr·6¯|§)'<eóÜèâþñ³\x0000}\x000bè\x0001«s\x0007"\x0000o²)É\x0017ÎióU¡\x0005\x000c\x000b$èøAÜ\x001bð¼7Ì\x0019Å%·Ô¹å³\x0000c\x000b\x0018Ç%¨\x0014ùC$Á´©íOV\x001aò>ö\x001aÀv	[ü¢YÂ6fKð²ä¢\x0018\x0019z*~²c°S3z\Ï\x0018iÀ³ò¥¶¿A*\x0000_Å×A=~\x0008c\Oæé%X\x0012-ol!D-t`»É,Âî\x0010êñS\x0008>RT¯	¥ú¢ÌSb\x0019Æ¸·Êe\x001e¡éN¡\x0019?¶þeUè½7B!dÑÕþàªY½±\x001b? aØ®\x0006	¹\x001aäò_ó£2¹7ÿ|óðãÝÇyîñªnçÅ£ÉåÕFFÈ0u\x001c/_½ÉÏÉäáüóÙõ¯\x000fy8a»\x0010!äBÅÄ´Éß6Q£Ë\x0013a\x0008\x0015y*y7¬·ë4l?¿¹{¼¿E\x001c#:gðW¶Ö°ëd¥ãèÐ\x0018zÔ|sùîêr\x0006¯iyÍrÞ¤¸ØQY\x0019\x0001gB\x000bûÍä\x0008­miírZ\x0014idéf$
u%/-\x0006=\x0006¯kyÝÓ`% PeLg9
ÒS\x001eMÚ¯\x001bFx¡åå¼ÎJÀ®Ðñ\x000cÌëk\x0011Uäçòú×/çE\x000f{	h&¯KÔNvEw`\x0004ñ\x0008ohyÃr^
âõ)/uVÚ?rhoÑ\x0008olyãbÞàj\x0001[ÞìX\x0012xªîYÉí÷RGxSË\x0016óú¤%1B¹§29Ê$\x000bï90Bo·q®óëÚ³\x0017°îÍÛrûæ½l°R§Î\x0017ñ\x001aYl°û]î\x0011ÚNýêåú×'SWÑùÑ|\x001clJx¤ãÐ©3½\Q©¹1Ë\x0016ÑF$yr\x0007Ö¿\x0000wúA/W\x0010ÞÕ=\x001aV*\ML ½RþÀÖè¡\x000b÷Ý\x000f[WîÅÌ1QñH9\x0014wN\x001arå\x0014Û}Õ:£ND7Å/;\x0012Í\x0010¿qÛç\x0014Û¡xD	Úæº8Ú>Q.7Û67ÝiÙ:ß,w×êoåG\x0014¡»æÅp\x0007²0³í¶ón[çýüç_~=ùñ¿ÿã?¿¡gáÏ\x000fó\x000eª¹ÉõI^-®ûrÌÞ÷'çß½zsòåÉ7ô2üþúitÓ¢(tÛ¢Ûµè&R?mn¾SZ\x001aW}}1æÀ\x0004ÙathÑa%º¶ZÐ\x001d
×ä÷Øº\x0007#í+\x000b]B\x001eZòð\x000fu^b\x001eÿ!ÐÑÍé\x0015\x000cþA\x001dÈ5þçókûi\x0015DÐÄ\x0000YÕæêRÛ\x0003+¼I#¾<;9ª¬?nWÇÇ¾:~ö¼p\x0011±Qò\x001fåÁÉQ·Å± m\x000bm×@G+Ké\x000e\x0010\x001b¥5Òí-ê\x0019gv-³[Ãê
ï,èZá\x001a« v: \x0015ÐN\x00050\x000b¤Ã\x001d/M©ÌñpH0ì[d¿\x0006æ|q	6òþ¿${­=©\x0001æÐ25Ì6Is:¥äU«)¨z	\x000fè»AèØBÇ\x0015Ð j\x000f¡r×ò\x000c§|ÝÄëpµ\x0007 S\x000bV@{ªÙ¶5\x0008ãÝ4FÕ\x0001\x0015æÀÓÜ\x0018´îíÊ\x001aÃò÷¤ît^£<þ.ÔfÛ\x001bÕw\x0004¿ºûôéîþã¬&Q+0§\x0014ð\x001eò²t¤Ztr¢Ø¦7ïÕåÛ·W¯¦5-­YLk\x0002¥i2-\x0018ñªMÑÚS\x0017ÀÚ\x0016Ö.ÅÃÀÉ\x000fP²âØøº^OÍB[@ëZZ÷ÌEÛ\x0015;[\x0008\x000b$N%GÖÙ§:Ìmï{Ï<j¥ûÙ±%7öÅ\x0017g\x001f>üþ_·èêÿþ_\x001fo»7ç6\x00050u·w2C)Y÷3¹;ç\x000cµÁ\x0005ºø\x0017¯/¾½zw`Òm¥5-­YN"ÅU\x0018\x0007B¦ã;á
ÓÚÖ>wÙºÖ=wÙBK\x000bÏ]¶¾¥õÏ]¶±¥ÏV«moAeoáÍ\x001f¸.ä·û»y9¼&-\x001a\x001c\x0003çT7:MU(½yyvÎµ!ß^]\x001eÊM¨mOAeOa\x0011©÷\x0012-kêkæh9È41}\x0014RÛÚe¤¶p°Ãèyo\x0004-3\x0017«;ÙÐ<LêZR·P¦ôø\x0014«ÀÅ+©\x0006lÚL¸¶Ã¤ÐÂB:©Qö4Ih)"©GôaPßú º&ý4X®¨£®e	\x0017ôÔ\x001a£aÔØ¢Æ¨\x000bá8fIñþ[p\x0017\x001aý2JºyÎZJ-ýüZgµ¼\x0003¿¿\x000cÐ¥)ÅËY¿WÁÎw='\x0001¯\x0017½k\x0017\x0017\x001fnî>Í+n1¼q:9Å9ßàä	\x000c ê	5õöìòõ;*~ùöÐüsÈ%Ô`N\x0012Å 6¶¸=ÙÂx+Ëm<\x001eSk¸ÒN¦ÕâNMg;ÒBÞB\x0019ªTÍa\x000cÝ¹ÆîÛ»>ÎíyHK@A¥$[¼½2ÃÛOG\x0004hPsÝ·_¿>89c7é\x0019jØ¤üÌýçÇÛ×7\x0018¼Ü wþO<\x001dÂ\x0018å¸§ÌÑB¦rX2\x0014]OV(]½wqòúì\x001d\x0006/g\x0008×\x000f7?Þ|zÄÿ­ò/\x001d0(¥Zàü?/B´CñteG­ÞE\x0015xëäU_ÕÌÛC;	ª©\x0014}ýùÛû\x0013=ïôZ»)ºT¼çÊúX×óM(.)¹|ýþÕÅõ\x0015þEûP¿§\x0005¤b]\x0018ö\x000bÊÅ¿¼ù#Ú¯î\x001f~ÿ\x001fóÐÀX9Ô]\\x001bèÑ¿æg}§j=xjê@\x001dÆ¡íWW×\x0017ïN¾ùrOðëFOÐò\x0019R\x0014+@T(lYD\x0011ä\x0005ÔèºßaÊ´
ò§ï>|¸ùËocýAZãåÍÉ¬7~ÿ¿½ûHjØpÑvª¤øG\x00084&â¥V¹¨À[]Ô°ÑÊú|@0ÐéRþ¨)./H¡Ñdª¬6.Þ\¾Þ§;BüÁæy\x0013â²Ï\x0010]7÷¼	ÑiçMÚÙ?oBTÉa\x0019¡K¹Q\x0008Qéä¡¬Åï³\x000e:\x0017u\x001fÝÍÃ\x000f·¿\x001e@C÷!>oá¡3\x0011\x001aÓ<DbYdk\x0014O¡¦f½ü¨/J/Ó&\x000eAÁ®\x000c+C\x001f4\x0008^·=f)\x001e*\x0017ý¼\x0015\x000cÕcêe÷7 \x0004cA\x000c*Q\x0010µ\x000b\x0002G\x0010 ^\x000e½ìXªõÎ¤2\x001b\x0015é¢ÐuûÒë\x000bùý\x000154ýÿõW. ø¥\x0017\x0006\x0013rdos8¥ô\x0007SÕÛ¼TáîÏéGÓèé\x0012G{xÞùÇ\x001fînKdù$¢KA´ur¡ì32*ªS²4ëqR%øò|ô×çåÏö´¡-ñ\x001fV®ù?
.ßû\x0014Üþz=kêùí/?lÎ&8ÿùæó§O¿ÿ×,MT©J@H\x001bx\x001d\x0012\x0006b¢ö©crZ\x0015sö\x001e\x0001E\x000flÅ^
W\x001b¸¨ÕT\x0015áYçK»\x0013\x001atÏ²3f¿1«úâc\¶Ì#Éò
´T/sy
¶\x001f~¹\x0008«:àcXøíRùNÇ¼ð\x0008©J?
ÌØçÝÎÆª^÷\x0018V§Å+³è4¦r¸Ãµª:Üg+æ"O\x0012\x0016Ö2V`iÙ}Vz6Võ²°B*K/	Ëª2\x0005eØ(nÔÉ\x0012.Jkµ@^Î27â|\x0019`0»ú;R*[ë\x0005\x0012\x0003ç6\x0010\x0018Õ¥\x0014Y+ßqµÀPqé\x0005Ê+xÈu¢Äx\x0017#\x0001+	\x000bkj\x0013\x000c\x001e18ME{e\x0014.\x001d1Ç`«õ\x0004UÈé\x0005j5\x0018Më±²ÄP­\x0016.äKî.gsm\x0002£1®ò{\x0011	\x000c~b\x0005þNï;f¡Äõ\x0002Í\x001alÈkòtåm\x0000Á´ÜÉ¸Ï
¶	ÖÆÊ/\x0019,º²?¤ÑùÎ®>bx«õ\x0012õªÊÞë|)ËH\x0008<bÀ°~µÖ\x000fÅm\x000c\x0012
\x001e43âìW\x0018È\x0004ÏÀZ<ÍÑ­e|\/¨*Õ«tÞØ\x001f³vãó[¼ÿ|ÿïMþú1\x0017û¡Ó}÷áÃ_&K*ò«¨wìú\x0018^SH\x0013ø¦}ìw¹Î\x000f]íË/ÿÄlù»`Å]\x0000æ,»ÖÎ\x0003/ZG²2ÙÈ&oÂdd.GÑò\x0007Ý£h.¼yøû\x000f7³ò\x0001IY¼´®¤Wh¯¬/42"Ý¢ó¦&õI}\x001cÍ\x0015g×ÿ|õòìP\x000e£²ÛÝ®b7.·dvËë«\x000eÑ²õÖc1»kÙÝJ¹;öUÌGEìº½{È[\x000e-:¬B×îZFWZâ `|`tå§÷Rtß¢ûu'Fði\x0007WÖr¢Øu=í{²ÙÙCË\x001eÖ\x001d\x0014ëaj8/5ùF{\x001eÁDulqR\x0013/fO-{ZÇncÞjÙóÜÄÌîä¦Æ~ÄÑjv.\x0019\x0012
©ÖÁÇx\x001a
{BeÉç½7Òq·>ýbtÓ¡uè!\x0007m=\x001a	,=o#¤*M5éÆ.×µ¿jI.ä_|eS~°ËW6\x001cû\x0008FÔM0Çý	zû'èµ?Á:kMè'$n¢0:ªëôådö\x001d5Ýr
m\è¼|¢©\x0006w³ÁZê(æªÑÈÑQÉ\x000fÓBü\x0012=·4Öàò¸\x0019Ø´Àf)0\x0005Û>°bO\x001c{P¦"bC}\x001e±Ú\x0016±Ê"þúáæã²Ôøé´«V¹`Ü}íÊfHJ»²*tx.&\x0017__½þòÐZãÐ´fÐäí>Dh¨D§ÄKÖ¢N$\x0004;yãF\x0008mKhÇ	kÔa@Ëi<TÎÇs\x0004Ðµn\x0018öÿlhï	ä Ilí¦3T#Ð\x0012Â0aâ	\x0019\x0007ôNG³"¡IZiÐ·~Ð±Dh¥î@Û$	wm¦\x0013
#±%c	ïçø\x0013¿r\x0012Ó^\x0010N;#©\x0005LÃVQ~(\x0003¢ËèÛ\x001a²\x0002¦µ7¹ñ´ò¥\x001eF\x000cQ÷
Url\x0016ø*C;mjF\x0010{=¨±\x0011Ñ+ñ@H\=\x0004õ¦ôsª\x0017\x0011v
[\x000fjltóÞ\f]Ýknõ§«âV#v\x001a[\x000fªìDµ°­FÔÿ?uç¤ÇÜé«ô\x0005ÜLü\x000f}jR=\x001a:Z$£I*<\x0014-ML"å&9;ãO¾o°>oâ,\x0012ÈÄ\x000b4«º\x000b¨²V]sµ\Íìó¢ÌD"ó%\x0012µ^*$ÒÁ^\x000c£G\x0010;
F.)	í*m£tG1B¸ÿ8Cg³aÐhï,&1Ý\x0006Ù­82\x0013¼¸¬\x0019Aì6\x000cZínØ·"Öì\x000b5¼QËùÌ\x0011Dß!úñï\x001c«UL~Úð¥ÈJF\x0013`9>Ø9\x0016\x0018ö,NaÏ\x0002®Lk¢;g=Ðýdß)ÄÎµÀ°oaU¹ò¡C\x0011Å£\x000fõ¸,\x0017V\x000e bç[pØ·dí¡r) a\x000e6Ù¨lÞìýÐØù\x0016\x001cö-Óôù3;q-*.¿ü\x0000öwa×BþDÎ³2eæ åX\x0003_\x0006TØíý°³Û8l·T:\x000b"\x0004W3\x0004F	âJ`\x0004±3Ü8l¸1Ô\x001d@º©r\x001e&\x0018t\x0018÷ZEì\x000c7\x000e\x001bnV\x0015ÁGIR\x0004WW$*v"v\x001b
w\x001eÊ«èOIó ±¢rË\x0005\x001c#áÆaÃnM'DÖ¢UÔò¡Ù½áÆaÃ­H\x000cDÊ²QòàHiÎº3ÜzØpSbËiót5Ç\x001fZEE|;\x0011;Ã­
7Ïâïl¡'Jh\x0005PÇ½·\x0016Ý\x0019n=l¸µÍ3¼\x0019H\x0005(B¸û+÷Iá+\x000eY\x0008©ûÐ[#zo¼­;Ï¢=\x000eþ¼$Â\x0000½Da1h1°\x001bvE\x000f;\x0016L"\x001f\x0014°\Ïé? \x0011r{ãDÝù\x0015=ìWhz£çÌ¬L·Hÿ!mä6ø½\x0017?Ýù\x0015=ìWqR\x001bÂ\x0019\x001a¤\x0011twØ½\x0011;·¢Ý¡\x0001Yòn\x0019¤ @9YÃGs$+\x0006L×y\x0014=ìQ\x000c!ùúDcÎK½Côj¯_6G1Ã\x001e&\x000c§}VJ\x0005"eòû\x0000H±HÜK4C1Ã\x000eåÿ$Î£abÓI\x001fþ\x0015§éÊ'ïXj÷Ït.Å\x000c»\x0014C\x0013Ñø3S
\x000e¿\x0002qÑFíuË¦\x0018\x0018v)¶DùE\x0016±LÄt\x000bôlkV{ý²é|\x0019ö)\x0016£\
\VC\x0015\x001erÕî+é\x0019v*F`z@÷\x0016(«Èº#i\x0015ÕråÏ\x0008bçTÌ°S±4Z&Ô§wÏ¯|:\x0004»û@w^Å\x000c{\x0015§PÊÔ/F\x001b]`èÃrgÝ\x0000í¶\x001d6Ú\x000e¯\x0001º<e	\x0003ðWönw¢Îv6Ñ\x000eÛDîW\x0010Yè:\x0011ÆÈGÅ÷c§\x0008;hM¢­ß&Ï`Ôü¹ãO\x0007Ð{
íl¢\x001d¶ÎH\x0003ªñÔ9UVQs&QûtÞKØ?\x000eÄv'ºÀMÆi'J	\x000f°{'v&Ñ\x000eD\x001aËWRLÆ{ä·\x0001ÔÆóVtq¹¡k\x0004±3vØ$:\x0012/	¼rÏûÝ\x0011ÛÙC;n\x000f©*%´;âP;d{"½^Åv¡¶\x001d\x000eµIJØ²EvH\x0018¼,âr\x001dÝ\x0000¡ë¶\x001b7Ú.¤ÊXaò"Z²ËuÙ#]¨íCm§
©t\x0017«\x001d¹ºIÔÞzãö\x001am×¹\x00157îV"p\x0008f<
\x001f*ÁÊYv{²ë¼\x001bö*Î(),\x000côpax
9\x0015ÂY³{#v^Å
{\x0015¼]yC3ÔôÎ1¢QZ6¢]î\\x0018AìÜ\x001bw+éxF\x000cêM¶­^E-7\x0019\x0010ö58Ã^&\x000b!DîBª\x000eâE4ËÅÞ#Wqã^%â9Û\x001b\x0013%\x0004ÓAl¶×{=³ëÜ\x001bv+´ûØíÑäôÑ#m\x001a¼\x0017±s+nØ­x8E`\x0018Ê¬\x0008úÌNÊî0ÖwnÅ\x000f»\x0015oò$ÉÜR\x0013D`ç%Ä^Ô{
±s+~Ø­$ßË]ÿé;\x0007~äCc¤RÙéÝ~Åw~Å\x000fû\x0015ïÃy0Ü$½hX\x001c\x001bÜÞ ÌwÅ\x000f{\x0016o¹q**j·ÏKèä0ÃîG\x000bßy\x0015?ìUBÚìÓbIþÆF¹ZÜ\x001dÆúÎ«øa¯âÊóxóQ\x0001\x000eoÒ¥@L6µîí$ì¼\x001fö*ÁK]¢±NKôàPÚA¬Úí}çUü°WñÞR+f^D'å-4M¢q¯_ñ_ñÃ~%Ð]¹,¢Î\x001e&/¢"}\x0013v×\x0008ùÎ­øq·B3¡ò\x0016X?ÌÍ^ÄÐù0ìW¢\x000eÀ¡\x0001kìV<°k6f÷i\x000eW	Ã^%h#gÅ©XDË©ËßÂurÍ»×°3ÙaØdSrNóqR~NIÅÝµ¡³aØ&\x0006ï¹Ì\x0014ÃªÅ\x0017>K[}'agpÂ°Á¡Óìy\x0011\x0013\x0013;æ8ï\x0006ì\x000es\x0018>Ì\x0011@º­ÓÍßV\x000f|2ý¸\x0019ÂØ\x001d8|T"jé$e\x0004¶Ù.[Iw½1bìJ\x001c>*dnx\x001b¦\x0010Ñ²µasÖuïQÝ9Ãç$:)÷3ôd
Å©xce\x0017êÝ½?±;(qô @nõ\x000e§R¾r0òöcö'bßv1zT 98RÖË6 ³µÑJl»»=	àûO·w-$ÀWô7Eù\x0016j\x0017÷hBm»»Ü\x0006\x001e²|ÊÈÞ\x000c§d
ÝKÉJ0»?%\x000b}ÃgYKúÁµ4æ\x0015å4÷\x0004êñõÜ\x000fú>iòÕã¤Á#+¦\x001a[;jSô-Õ$\x0016vû\x001aãî\x001a7AJoWÈYÆàË\x0016¥Ë<\x000cíÁ\x001dÞ\x0007u8\x0001J-tÈæÒÅäc­\x0014»\x0003]\x001bïÚ8Aí\x0011¿XZQ"!ï\x000eHè}±¦~4¸s~Ï¢§\x000eÎëyùø.ì°OÐN\x0012(ñU×iuëÏþøáý»­\x0006ëøÁÈK5xR¬\x001b°N=Þe~Ç\x001f_<q½\x0001\·àz\x00178Ö\x0012ÇSG*\x0000£z¤9}\x000cÜ´àf\x000f8(-ê\x0000é\x001f¹1\x0001ØtûxDaÜ¶äv×+/\x0015@
¥ðÕ\x001bQðR¸\Æ>KîZr·kÍókYYr}Î\x001d?Ú[®\Åö-¶ßMA\x0004o\x0015ß
T\x001a\x001fI\x001dZê°:KE W¥j96Ø­
Acà±\x0005»Û*².µ
¤3Lj-ãrvo¼iï¥fdØnU£Êd\x001cKì
\x001f\x0007\x001a#ïÌ8ì²ã¹^t¼Pmt¼Ü.ÐCØe\x000f\x0001Ë@xBwAD\½/E÷@Ê\x0018zgX`e\x0001¨g4]O¸iÊAE_zDï\x000e)ì;¥$ü\x0016NRXÒ3n »#
#v§\x0014wR²¢û¢­*KQ\x001eTãJ\x0001Ç0º²Ù46i)5u.øíÙ\x000fSHû)Ï%~<\x0019\x001eE´Ä¤Uf¥=´Xs+¢,
~yöäÅ\x0014Û¾^LÜ\x0010cK³Äê¡J.ÈéZôò*l`¹sc\x0006X·Àzz½bKbÒÁZGSu\x0017qù\x00166\x0003lZ`3
lPÊ+è*^_µÁËUü°\x0015¶-°\x0006&ñYä<ºHY¡\x0011\x0004m©nú b×\x0012»ib\x0010Çh¬µò~BR	W_."!ö-±'2¼à4µ¶ÊÄe­ù\x0019âÐ\x0012Yb\x0017u}\x00147J\x0012ïº\x001ad\x0013çÌ\x0010Ç8N¯±B)'±Úñí\x0011ILN\x0003½q`è½Ç´ûp>på§MûÃð\x0012»ÓÛÆr¹þ\x000cqgaÚ\x001a;\x0007R4M\x001dÜ´FÍîòÜá2ÇÐY76o®J\x0018j%b\x00199
JÞ\x0016VÞ=ÜóÑÉ\x0003ä\x0013«\x000b^½ýáöîÓÿ×\x0016b£¤Ûh¨b&1D&Æà×	,-xõìÉåõê°ð\x0006Ø´Àf\x001a\x0018UI8\x0019ncsbBÞÇ¸\x001aºâº\x0016×MãÒó{Y_tlFéË\x001c\x0004%g½\x0016á\x0002\x00168L\x0003\x001b\x0019SQ\x0012¼\x0004ç
°k\x0017ÁAàFúËWÕ)bé73¤ÏËQ\x001bõò\x001dNÜ9?tÎ[^ã\x0014#;Þ\x0014µl\x0006
\x001fDÜ\x001d:?uÁËÄ!Ð[E&õÔ-?IN\x0000wÇ\x000e¦ÏÕJ*R5"O\x0001¢û©»¸Üq3AÜ;>x¿\x001e1v\x0007\x000f§\x000f\x001eEªÆ)r\x0007G@i­ç»L\x0010÷ÎnúàQíN(þ9]5¸´010\x001cå=°;w8}îl\x0014ød`çä\x0015\x000bE(¯ñAÄÝÁÃéçê\x0014\x000fC\x0002\x001dÈíVxeÐÕ\x0008°2÷\x0014¦KR¼	\x0015·ÛæT\x001d\x0011ídt\x0015¹L\x0011çÃèvTÅ£ÐºÖ; ½\x0012Í	m£h\x0019%\x001b!»ôr[æ\x001cµm©í\x000ejìø¬N\x001eEÉl6QH{c¹~|ÚµÔn\x000f5È¤;£¬LçD':pèK(ç¨}KíwP§{)ë4\x0019j?ejãd_GòCÔ¡¥\x000eû¨Y¢2\x00110\x0012\x001aÙÖË sÌ±e;Ápý*M+ÀàyshXÖBnÕrM	gS¡xÐXòÈØèe,Ï#Ã!jè¨aÚ»Y×Ò¤ÛTAw"-®W\x001ec§¨MGmvP'\x0007SgkA³x\x000c×2ÕÍ/+UÍaw¶\x001av\x0018k`ÆEI4½ÁZ¬^\x0016ô£îl5ì0ÖÔ½ÂÚîé4Rn¦6uòÊÌ\x001cvg¬aµöÖ¦8©`kY\x0000Ð¢Mþá8\x001f\x0003µ\x001dæ:ÏQdlzÀ4meh\x001b¬¼ÕOaw\x0006\x001bvXlvFä=\x0012eh\x0015 ÛXå\x000e½/g3<çmÞCêÔ\x000cÕâÓ§ÛNZûà<\x0001nþh:©£±àêHÄ´ßÅ\x000e>ÞBC\x0013XÚW×ü_}õÇoo>3v\x0019{~¹}êyî¨Èäþ43QÉ,\x0001ÊE.ÿñâÛË7¾eT{¥Ç\x001ewÒ\x001b%Q7Ñó0]@u¢_´-óôº¥×;éUÛ¦woÎP+nG4Ô\x0001x,¼iáÍNxj.ÆaÔ*Tû¸¢;Oo[z»ÞEË	\x001eë0p²\x001dd
¹ñËí0óì®ew;W^+\x0011¦ÞA.©MKÏôV-WþÏÓûÞï\ygH¶6Ó§,Ï\x0006< \x001bz* <>´ôaçÚ;)sTøÁQ:+vÒcÞb>Ï\x001e[ö¸så±\x000e¶!ËSJ*T:È|Å°+5\x0015ÓôÐzØiëî&K"0r\x001d
Q\x0016eÄÃ<~g.a¯½´2ùÔ\x0012\x0006	ìûå¡yüÎæÀ^£"\x001cöUÙmqÃ
fYfu]&Þ®²wg\x0016v\x001eÚÄ|®KàBÖ`*\x000cÙ7Ç\x00068àjo¬üÍ¾¥÷Òã\x0005_Ñ]/Ùb1qù&²ç\x0017|º÷\x000b>íÜ<µ,ÑQ_\x0015ïýÚ\x0004bWÔ+öü\x001fîý\x001fvú\\x0011Y±YÆ¿\x0001øêµÒ;¢æÂ\x0011\x000fýÅ.\x0007@å1¡lE_Eë½lËªÝÃ?\x001eâºJyk+[¿¾½»Ël|Õúþ\x001f¶>tUIå(ýêÔË%®~yÜ©ÄõëËëkú;¾t½¤¿ü§`ûSðbQ2Â*\x0006Nè ÉkKeú²VþÞ¢Û¢ù)ZdÙ,\x0018Ïs	h\x001atîèe\x0019é½?Å´?Å\x001c´Áð\TÙmV\x0005S+ê¯{m=æ pIjì\x0002?º[ù"+]Ì{k;æwÈÄ\x000bÜ1>G\x001dm²ôÜù3|û3ü1?#Ýe\x0002J0"K\x0003ÖÖ!-Ë:\x0011{JhJ8è¸G1Â`ª3(34p¹ÿxïOíOÇü\x0014åD»Æ·³:,\x0018\x0019HúØ\x0018è©\x001fÒ¼ve¾{¯tÌë/ñÖËÿßø%½?ÆÇ(blÉúKê¨ ¸,º·÷§t~\x0011qÆ>ðH=£¤·%Ïú+â\x0007+#õöþÎÀ1þÄ\x0018[,:%\x001ayÊÉlôþW\x000cXßßO~?wüw\x0017Á÷ÿÞGÆÿ~U®¡1µO\x001b\x0019N^ò\x001c¼Õà~\x0013\x0018Ø.Èÿxvuóùîöý§[èÑH\x0005[ºÐJý3xIï¬¤\x0005+ü«\x0004ýæúòùëW\x0013cKóÄ$\x0014É:1)hD\x001e¯§äR\x0008æ¾ï\x0011fÝ2ë\x001d«\x001cYÕ\x0000\x001d\x000bqi\x001eé\x001d!¶-±&ÖµMÉjåëÀ:Û\x000eVnÆ-ÜÛË6?­=ûù\x001f\x0013ôç³§ï>lâ¥v5nî0 NÍ2ÞB»ådÇ³o_^¼zß=½z±\x0015[Vcu\x0012ü$V+×6zAcV¿Ü´6Ìª[VýÛ^WÓ²9Öd\x0019JÂË´gCýÈãKI|y1Ù;Ìj[V;¹\x0007,\x000f2:ÖáEHsuå¢8ÌêZV7¹®R¯h²réagYTßúIPæ\x0018MO<o)J\x001f¶ËBõÃ¬¡e
¿áE-hü.*Ü¯¿\x0006s/>¸¸ûe«ã\x0002<4#ùZËÓ¢À\x0019]íò«Iã¸.®_>ækï\x0017_¹\x0017\x001d\x0010Ç(e,ZeÑ¶\x001céJ\x001c\x001e¹x
\x00108Ì\x0012#\x001aÑ:Ò(ýµ¤Ò$!X|Dëh+1
vkóÿ}vg\x0005eÖÕ\x0001á\x000e­Ü£V;\x0013ïC¯=¤ ¿ÿË\x0017ØÞÐûxÒvç¬¤"ÛyÿJûÏ\x0006&?\x001b|÷ám¾\x0019¥ËÐÏ¿¼ýéýß·¼vDòÚA\x0013Ä¹ûÁ 2Z\x0016ìüîÅ³|\x0019J\x0017 o_>ûæù\x001eçÅ\x0017gyÝÉ\jÈ\x000cÈNVË
;\x0013¸ºÅÕ³¸Á³¦¿\x0005ª¡-Ïñ¦V£ª°<hn×´¼fz;HHF¯29Ù`Õs\x000bËí\x0013¼¶åµ³¼1Hé=M\x001dgïa¬ÜÕç&h]Kë¦iu4Oý;iuÍm/\x0007\x0013¼¾åõS¼òuì|º\x0007\x0007iã¥G\x0012Ü\x0007á\x00167Ìâ*Ã"Ý\x0016¬aEZã$Ñ@Cr\x000eÂ-nÅÕ2ÅÀ\x0002\x0006Q ´
\x0017ZÞ&nJ"}r;\x0018©\x0005Ò¡fc\x0016@fÌêeýé	àÞ·Í97Za_S}@:yAzäÖ$\x001e'x;g\x0001sÞ"Ò¸%	\x001d\x0014i'1°U2ÖÅg\x0002¸³¾0g~I\x0004LËRKå7¦{GycÝí`=»4ÉVAÉ\x0012×IJh\x000fâ½'
]61ýÍÜ¾0ZR¨ Ô²&\x000f-^Y-HpC¸¦\x000emºÜ?Ï¾½yûîÝÍÝ·PÓ7NU+ïä"ª¥tù\x001e
Ë5ôìÛgWW\x0017×_?®[t½\x000fÝpfÕ¨Ò®NK_\x0019	6
nZp³\x000f\5\x0016\x0004kúÏË8³ø°²Ý(:I5·ð$Ô¼\x0007ßÓ9:\x000b2#ÂX\x0019
øðÛì}øµõ÷7ºÊ\x001býé?ßþüö}¾ì}wóîã÷\x001b.{T4©%^F´çÜY!\x0006c\x0016]øÓ?^~ûìy¾î}wqõêÅó®{\x000c-0N\x0003§XFêXM\x0005Ü@\x0014¥\x0004	Â²BÑ\x000c±nõ,1MR\x0010?\x0018ÑÈL^F¢\x000e¿%!6-±^cêaæ\x000c\x0000i\x000bHçµäÜr%ê\x000c°kÝ<p<çMN]¿xë.^6Ô3¼¡å
ó§.H×!¥XØ£4¦$Ï¸\x0018N\x0000·
×!GÎÄ;yÓÕ\x0004¸¶7ÈUjYÚe\x0006¸3\x00130m'Òÿæ\x0016\x000e´ªÖ"{)]\x0002í\x0017#¥\x0019âîÐÁô©ó4X\x001fm),µÒuRg(ØÅàyf\x001bß\x001bB\x000eþbvoÄsÍ)-#µºÉÔI*z9\x0003>\x0007þoo¾`ç¿µÏ_ÆrEBéê¬%	ËÕ!sø]G*±Ó_Ìnq{J%ÖÆB\x0012Ò¯¹ÄÝ§\x0012î\x000bêjk)²rñ?ð;ÿ\x0000)E2\x0011/º z@9I[n\+\x0003¼9F*ºÅüÐÿ8µn©õ\x000eêè¸\x000b2ýã\x0017\x0013êJ{¢_"¢¶-µÝAMÝ\x000cå)=<\x0012³èÊÉ4Ñ@ÂÀQûÚï ¦É
E4Y\x0010îÁtáµÖË­ÊcÔ)ò¸\x001fE»NÚ:ýC
ûÿø¼ÝtÇ
\x001aÙ
\x001aþÑð`T/\x0002¥ÔJ¸È-Íáé\x001fRàÿ§ô\x000b^>tÑerÝë\x001däN÷¹¸VrÍ%ÑRN*¬\x0015õ»ÿìê\x001aSòôÃ»m\x001a¥Þ!8)æçC¬nÒ<¸?¾¸zP\x0014î¯.¸Ærl4Z4¹hNKIë#)IÌÿÛÈhZF3ÇÈOg\x0010Ûê	R.&îÁ\x0007ÊÇ(\x001dÞ;a\x000e9!söÛwoÿvöõí»\x001f?|¾ÛôòpÊ\x000bXðç¥Ï\x0001HÃE¤\x0017V_ÙÏþpyõìÒF½ºxúâÍõãÄØ\x0012ã<±ì\x0000«@ôPt\x0015\x0016Ñ¤x\x0010°nõ408y}°ô\x0010QâÏ\x0014»6[Qù 6-±ÙEÌb")®àÇ>][-VÓ\Ã¼¶åµÓ¼X\x000b/L0,lN7\x0011/¼Çmb×\x0012»iâäÉ8HzU|QÕ^ôî´^Ñk ö-±'öòDi¼h¢ª°µ\x0016ô\x000c\x00138ÌïÀÉ\x000bZb_7\x0005Ô%^\x0015°Þ
\x000c÷SpÐ§à>½¾½ût'H®>|þe\x0003Iq;K-Ûd×x8%xyî1¸¼9äþñæìõåõëë\x001a³½xórõ'üÀN\x000fååòI\x001eÒ§Ìuô·TFÿ?ÿñ?½{ûq£
¢â\x000bzBî­gý¸\x001aÒÃòcë©xþìò«g¯Ö»ÜOÈÍ¥O°éofÉÁ+¾B¡Á5¨¤56¬\x000cÄþüÅV]-Ô<ó-×BM¤Ä
¥ñsx\x000e$ÜáVÞØú\ø\x0003¬îU@`ÿ2Aëë\x0014Íx
µU2ÄùåAÙ[\x001dT¼\x000bméáç³·Þ~:«	³×w\x001fþ~»±¬Ïô\x0004x¤F>è$æt\x000fWÐ¿9{yùúÙë³\x001e8{}ýâO\x000ff5âý$nlAwý\x001asÞÃäæeÔ\x0016,Wu=ú[VÞT´¿\x0017«¦\x000bFû¦röäîÃÿüaÃ\x00056ORíc\x0015\x0004u²?\x000bËaÉ	õÉõ§|ñÐåqu«gq-Êó³5²F¢\x0017£\x001e¶âÛyÔ.-/N¯/È\x000b\x0010é|\x0018VXµÒ)²lýFpAßJÖ½¬Á»tËþñ7wlÑøB6*ÎQ9`§ñHGÝÕÅ\x0019Q?Ö©¥ï_°u¯a0ÈíTd\x0011§Ä-ÓÝ\x0010½\x0015îøØÄËÜ÷lÀ	£c©/Ïw>õÅ¢¶¥¾¾¾GªîGþ¡º\x001fÓGVOÒ_´µ¡\x001cP
(#¼bñE9Õ\x0008³[í.\x0012=u1vkÈºEÖ{#Ö,yL±¬õµ\x001d#È¶E¶{© Ûñþé\x0015\x001cÅ;Ø\x000c®oqý\x001e\eëvÆ,i\x0015·J§ÛÍòÅq\x0019zy3ûïÿõïì¿üM\x001f\x0019¼é\x0012sË·»ÛÏ_[Aõ\x0015µ\x001cMº1$Try<OY¥{\x000båtDÒ¹+Ö¤3Ï\x001cõ¿L\x0017K¾\x0010\_^¼Y±\x0015\x001db:d8RU§4äzÌ\x0018YY/1vZQ;\x0018£7\x0010XEB¥ÏKÉÌ\x0018¸\x000c?Ý=c81m\x001c;ÇE
bs,2\x0018HfÛ1)¢t³ÑÐsdFt¹¾/3:/ÐÙ¦\x001décÉUUªÓ2úzb,ga\x000f7\x0007}iï¡iGÒÿ1wp \x001e\x001cY+\x0007GÕ³ç«?ÿë_~¹kÌÏ):LqËë÷n·@Z]Ió×Ò&FÊJ\x0014F\x001dpa9OÑaX^_<_\x001dßá¿÷Ç_ü|IwùË¾Iÿò»M\x001e¤Î&«zÝ©-ûz}Âõþz¾¤»üå·ß^<OAË\x0006\
¸\x0001wñÒè2¨¼à\x0018Øy\x0001îf£Ì\x0001ÿôoÃT\x0004ÿ¸º9ûÇÏ\x001f?½ýqË\x0006\x0008Fg¿ã|Ìu6*\x001f¨à¹×\x0011£~áÐ§ïþo^½~ötýËë·\x001fþõÇ\x001bç¸Þ}þïÿÚ´/\x001d}á|m\x0001ª:öüµ=¤ÊûNLçõ4\x0005¥«N»*6h\x000c*yër\x0002e5Ý\x00033\x00117ãµYØ#PÉ"ÄQ(\x001a7\x0010ËJÑKj±2<Y\x0005µd³\x0007¨¶þg\x0006³1\x0013I|2\x0014òä%\x0015°+ÅßJõÞ}ü\x001bf*z\x001c¦ÿ¹º=ûÒU?mÂNjWÒ%Óñ^w\x0001\x001cciPKuyö\x001deª¾Ù\x0000\x00059ò\x001fcdä+-¾4W´ø
¶\x0015`ÌBµLñ@m¾¿ ;üÍÝÍ{zþþ¼måb$5ëÌg\x001cM\È+çø}.mÜ¥möÍõÅszñ~³n%*\x001f¶|8ÈçU
\x0000ÙÖ¦{6ýcæ\x0012HÓ6ÜÇgZ>3¼~Ápwk^¿X|A0\x0012F»`ÍFðlgGñB¬\x0007C§Tå¼¦¨Zø¼Z0l#|®åsÃËGù\x0014ï
=	rOjçúùÏ\x000f¯_
\x001c9«¬F|Î½Snçò\x0016/\x000c/\x001fÍàåK~Õ¯kÐ\x0005µ\x0010àÅ\x0016/\x000e¯\x001em9>¼*÷ûæÕ\x0005Ôî²ïðrY¯\x0018?5\x000cHiH¬×tW\x0016Ð\x0005]¯ézõÞ:\x000fç\x0014\x000cùCTÜ
A\x0000íR¨9\x0002Øg\x0018µÏé\x0013#\x0004¥üW^AÐõXwzx\x0005mµ0l5\x001bh«ë\x00191°\x0010±\x0000v\x000e\x0004='EÈØQ6\x0003\x001a`%\x0005ëä\x0008`çB`Øx8­ ©\x000cH\x000eÆÈ\x001eÔKÁÕ\x0008`çC`ØP®\x0017ÐËErmòµ]¸êðu>\x0004r»PÔæÀNØXI¿(´\x000b1à\x0008`çE`Ø¸ÜÁ\¾°ä^jBC«[°ó#0ìH\`:Å{2>-ßN:ì¼\x0008\x000e{´R\ÿ¾¤\x0018_\x0007/\x001b\x0010\x0012B#\x0017Áa/B\x0019 Ã'Ä\x001a*\x0006Ê+¨j\x0014Ø«L\x0000öAþ°\x0017IWmn«QÔ¦\x0013àYåäF÷EØ9\x0011\x001cv"Nç\x0011\x001cÏ(ªoÎÎs*ÝÝ\x0005Ø9\x0011\x001cv"BS|Ft8Z\x001bñ!Jí3Øù\x0010\x001cö!\x000e5¿®§ËH:R[ÇÉ¨¸\x001a\x0001ì|\x0008\x000eû\x0010\¯æ#ù´d@T\x0001Ýy;'ãN\x0004\x0015çÍÒ¿ñ\x0015,o_´;¯"Ø9\x0011\x001cv"6\x0000Q'ê$Låó;ãTì<\x0008{\x0010zÃ¯WVOa\x0010ùóîãÓÖÃ&ÚzL¼yVNÏùúh#\x0003î\x0002¯½nõ2L1Oû:zR0à|B½0-½v`Â}LÀép@Cü´éy;fÌ\x0017ãÓ0Èºô\x0017É-­H-3tïQ\x0019y\x001caúè
wf?Ü}L7VÓs\x000eI;yõ>Ê->¸}ákÓ\x000eX¿ù\x0004¥\x0013®·æ\x0019\x0000$\x0019v_£xÒÑé"u3zQÁÈ#*;ÈÅ¶ùª'Ä\x0003ÛÌÄû+3+\x0019Y
&Ýô¹ã´<©1ý·ÂnÊ{g\x001cgÎx$aBs°ûrö{w=qå/º¸?Ü|þÛ&Beiõò\x001b,dÅä!U¼}XûÉþpñæ\x001e§Ä\x0012'(C¨)¦ÄF\x0001Å¤ËCK×ûAJÝRê)JÏU½ÊY¨\x0016\x001dx$Ò~)Q<HiZJ3Cnú¥È;S\x001aN·k°rÁT\x000eRÚÒÎPzÅeTÞ\x0018]¹¯&\x0003*Ñ-Üf\x0006)]Kéf(\x000c!SÉQsæ]äo\x0001¿\x0010ï\x000eB\x00162Ì@¢SaD+¦2\x0005¼+i$ünÈØBÆ)HàG[E\x001eHsÛ²\x0010RVíÞKÙdâó§ÂÌ*«\x0019´W\x001d/&7&Ì°{1¡30e/ÓöIJü¨¡¥úÃøý\x001b\x0013:K\x0004S¦\x0008¬"l§á(q©ªf\x0010³3E0c
]\x000f hð|yààÞÅ<qi7fg`Æ\x0018ù"0\x0019ùÜ)¨z!Ô\x0018dìL\x0011ÌØ"\x001f\x0003¢N9Û"+a4´n·Î\x0016Á1r\x0006å\x0006I
gr\x0013¯\x000fú6.e
Æ0±3F8cèh (üÆ\x0017ÓUÊ¾©v²\x000b0q&Ât\x00084Y0)Ø¼\x000b¢£#º\x0017³0gL¦·F
&\x0003©&ñ+¦óc^Y\x0007)»\x0008\x0013gBLJïx1S¸®¤\x0008LYYÌ¥ÜÆ fg1qÆbR\x0013­\x0019ÑHEL
1å÷æ0}ég0iodÌ<l*cÊ(0åú®Ø9ÌÎhâÑ´Éh*Á¬¯¯\x001a¤DÁ¡Ú\x001dt`g5qÆjZã%6ÆJu4:)THAÒîî¬¦±Éx³\x000b4Ô_!ÎI\x0016{÷ÖÔÕÔ3VÓ¦ýÈ÷h¼×¥ÿ`ö\x0002ÓsÕÔ3V0ùIÔeLÉµæ\x0000~/f\x0017hê@Æ\x0017\x0016ÛNÚÁüÍA(Uºýî_Ì.Ó3\x0001\x001ci
\x0003þåÜ:1-ò\x0003îå ºÜ[¹\x0005åÉ}Ã¡;i7pèn
pÑ\x0019xãÊºFMç}Úd>çhÿ7óG\x0018î\x0015¹¦¿hz"\x0012ì¶2\FËhªø,X&£ê¹\x001d"±~ó@¾P\x0018±eÄ	F
{.b*
2£Ñ|cÓ¸.\x001ccÔ-£`T¤ÈòÖ<\x000403*y\x00087\x0018\x0016¼ú\x0018£m\x0019í8#\x0019$Çé\x000e¯H@²X$+7ß%W9èZD7³Qªæ¼\x0006©#ý?IuØ33Æ\x0018ZÆ0·º\x001c\x0019ªBäÂ9¨YBKQâNÆØ2Æ	F_KÓ\x0002ÙâÉÁó±~){0ÄxJleÓ£f\x0016²^ÒHmEóB\x0006/wI½T}3\x0006ÙÙ\x001e0>F\x0008\x0013\x0012§­!Ã±v©ÂjÐtf\x0010¥A0\x0004à|píg³aÉË!v\x0007f,3R\x0008\x0016u>K°(	\x000b1ÈÎôÀí1¾VºÐ5KÀÉJ:Xj	\x0018ìl\x000fÌ\x0018d¸Qî;N\x0012\x001b)\K®{?7v\x0007\x001bg\x000e¶\x0017Èè­uL\x0001RÎ-Dic»Æ	|\x001dD*zrj$ÛÊ^\x0006}a\x001bH\x0016Øhù\x000e¸D\x0011\x0007QëðQ¡¼£x¿3Üç\x000cs¿Fv\x001fUO.© 7«O¬ª<¡¥ºÔm¨¶\x000fÌ\x0001e\x001c6w*?½û|»
\x0013UyC#ùc)/A\x0014\x0019\x0002Kå\x0006$ûVÚKgá£ Øâ\x0014hn]ÚºÊoÐ\C;W\x0000Õ-¨[Qtk,í¬ÛÐJâ ÝÈnd£ ¦\x00055s \x0000µï\x0016¢THÐtH¹/FÃ¤¶%µs¤Ns-\x0007(4y\x0006ÏÆÞÛÅ\x0007QR×º9RCgR\x0017¤ÈHC%]¼ÿ\x000cúÔÏ'\x0005<\x000e	RHw*ÊèÝ÷ÓxgICK\x001aæÖ\x001as<}¬Mëµ®Ã[XJrÆ4NÚ(S\x001b´©©\x001f1\x0014ëùÅ7ôAÐÓ([}5ùõ%¾¾\x0011Õ\x0007ãëÇ_*©\x001f&íýÓ¢þ\x000e£ËÒòòSL\x0007J×ã¥èd\x0018µóP0é¢/#îÓç·õH\x0005©¡ðA\x001d±ª9'¥\x0004pAJ@?$%0Úy)sS4!øPQõ¸þ\x0019É\x001eÇ%maÔÎMÁrÞóhdý\x00157ëºªË5£¨9GÎ\x0015¥²ªQ\x001cU"\x0015-	µt[\x001eFí\x001c\x0015Lzª_\x0007µóT0çª\4t\x0015Í¨F\x001c\x0008a\x0004Xª0\x001e\x0005ÅÎþãý÷ÉûË¡²Nr FÆ¶¤óïöDTéÃß«â\x0005ßUñÇíÏ7YzCøçåv
.WOð¯Ô\x0006`KRiõ´<.¿½X¦np±ÅÅi\kåMÖs·iA¥±`1M?Ã«[^=ÍkäÝ\x0018tÍ¤ q }\x0010á¡Ô\x0001\Óâi\­Ev\x0001ÒµqµáV¬\x0010\x0017o-\x0013¸®Åu³¸4¶§9S\x0001¨\x0002\x00027pÓÌÀ¥Lþ\x000cohyÃ4¯\x0007©õVic8NÈ»7YN[lyã4¯sò
þ5ÉL\x001bíðpÝÐv\èmÙ´13Ôkä³2\x0018Í]Ç²\x001fTtÜkæÃRærê¸õí(E÷æ\x0004B
s½dÞ\5\x0012\x000fUêl¡f\x001dï¦Â$ö9­o>üôùöÓ6\x0001>g ö4GÔ«\x000eµ©Ù,IWüÛ7/¾ysùú\x0001\x0005>Õ«¨3/NóZÍ»
S\x0010\x0019¹x'Ö6{½Ô`:Ã«[^=Í«CU\x001eQÕih\x001f¤çÙ-Ö\x001dLð×Ló:\x000eO­#[	\x0003RD¬âb©æ\x0004®mqíüò*yþÕÉÝIa}&J.ùÁHr;¯kyÝüq´WÚ\x000eêÜÊq\x0006!e\x0017Z&x}Ëë§yIÀXú×@r\x001eÄýk\x000fç?¶ó7Ìó:i
$Í.)4Fa;è¬Å\x00166NÃ¦¨Lt±h¼"H³|¨¸Çð¶m/ñ^&l\x0004ØFÏ}DÆbo@#¼Q\x001fc\x001c ÷móÎ
SbJÓð\x0001~
1¦ªõ\x001e³y¡óm0íÜlòhül|¼\x0018:\x0017\x0017%Zf;ç\x0006óÞ-¹4î`O>¢jÊÈÜ4ºÖ\x001d\x0013=@çÝ`Ú½Y¨}\x001dtYæ-LsXy\x0017\x0015>f;ÿ\x0006Ó\x000eÎÆ )Fç	êåÌYQ|$U¾\x001d¸sp0íáLðâ-
S·|ÞÂú°-Ü98öpéb	ZDs0H\x0007\x001aâÃ&Û;\x000f\x0007Ó.fNðp§^\x0000\x0008JVØÂ1\x00110t^\x000e¦Ý%ç\x0012\x0002[8!uì\x001cB 8+9\x0010Bt
û9 ¿=xF
¹Ó¤üÍR;­\x0016Ûé¦°»\x001açÈ%\x001f¿YlhG¿ûçóÛÏÝ¦Ð¢bÝ\x0013ÁQ\x001d¹.Ò(\x000fK"ùüòÍw\x001bè°¥Ãa:#6ÒÜ\x001e_%BÛZ¯\x0005\x001bétK§\x0007ér\x0007%Óa°ÑVÙd\x0000VÎ7ÒÎÒJ\x001f×°§Ë/ößFi6×vçµ-\x001d¥ãô¸£5ävI¢t\x0011ã¾\x000b-Z\x0018Es§ÏzÊZ\x0013cíPX±ëÛèZ\x0015Z¬íxÚ³p
Íæ¢Q\x000bµ\x001c×\x001e\x00177Òu\x0007\x0016FO¬G<W\§Ü«M\x0013kÌâSÂv¼îLÀð¡Hæ/"4¨PË+¨§´\x000bwá¹\x000eÏ
â¹2Ê¤tá;ªÆËxVTÌZÉØ£tá¾1n'Þ|þÛÙÅû<apCö\x001aøÁ0·\x0000æG[y\x001a¥ÍÇ%\x0017oþéìâùêdÄ\x0006Ó´f\x000eÓ\x0006\x0016¡J[âà\x0002
Aì\x000fÔ\x000f¶\x001aOzó[fý¡gýá7Èªî¿Â*~~w·qìD4Q
ëiÊ\x001a÷y*«oÅ i;\x000f÷ß1?Í\x000eß\x000eHC!ïXêI²¥¸Ü=\x0000hZ@3\x000c\x0018\<ü\x0017)
·V»¸\x0015Î¶pv\x001c.]Å9f¥\x0001æüTâuÍ\x001dY	­·\x0002º\x0016Ð\x0003â)}äj\x0004qÒWÅÅS2\x0002è[@?\x000eè«sn\x0010µ$éoÍcýv\x0001\x00160\x0003*àÂ4eXäÅ)QV¨wÒÅ.N\x000ewÎ\x0012ÓÆ\x0005	­]
?\«ÛÈ×¦}\x0010\x0007\x0000= r®JKê§N¡Åi#|½}\x001e7Ð\x0004ùP1\x000fK\x0019ihÅF\x0011Bì\x0008q|\x0005µÌ÷¥&Õz·S®¦ûv\x001eaè\\x0008û\x0010\x001f¼\x0008\x0019c¤ ÊÆú4KG\x0000;\x0017\x0002ã>Ä­\x0019\x0010Tò\x0000oB}\x0004rK³F\x0008;?\x0002ãÄëÈ\x000ftmâW*\x000bÒùîT;ÏIçG`ÜÐ¬H¾(\x001b\x0012µ¢×(»p§£^\x0000´\x001c\x0015ÉypF{Îs\x000ciápÁ#ëuÓóÃZr|ófü\x0002ÔÌ²h\x0001-©³ø\x0012èÊýoó'ÿ\x0002ÔMx.sÀüIöJ4À¬½ðm>;_pÚ\x0019Î¬\x0010È¡6Ô¦\x000c[[ñÀ­eè\x001e\x0007ûw\x00018×|<{òùÇ¦dìkO?´FÊI2Z(xÑ4\x0004\x0017W³±¯Î¼I7×¯ÓÍ¥W[£Å\x0016giâO\x000f²E#Ö\x0011pziFØ¨.¬nQõ\x001cjZ6iÊQt5dO\x001e¬ÃêÉ7-ì£´¦¥5³\x000bKãáøæ(^=ÄÓn]\x001as:Ak[Z;»¶A×\x00171ªqäa{ÆÕ0sQ:rÖµ´núéz+Kx2Ú.\x0019\x0008GV\x001ft`C\x000b\x001b¦·­ª\x001b:´dÛÊ\x0015W­\x0005O°±³°º\x0016äÒ\x0013\x001eó>l\x001fºõÑ\x0011ÚöÚ\x0001_ªSFq©¾µÐªªØ\x0018P^Pch;S\x000b¶6\x0005\x0004Z
Á,J¥RPÒ\x0001v½ýq¶³_0iÀ\x001cÎ9y®\x000b"ìæ½\õ\x00034cÛ\x0007Ð\x0006ãÔ¦Îë±'y\x0006\x001f¥¾
ý~ÍÄqë§Aäxáôðü\x001b]ê{ã\x000c2ôìJ{¥|
r §ÞgÖK·\x0011ßï9W¥ç¼\x001cÿxöÇ÷Rè¸
6F¹Á"
+\x0005\x0014Q&NÇ%Y½:rüÕÙ\x001fiàø\x0016\Óây\ëDg-Ýþå>[Þ,©¥g©Þy\x0008WÝÏWòÿîÝíÙÓ\x000fïÞ}ø´-3\x0010%&Ó¡ÛXs\x0017¸43;í««Ë³§/®®^¼~\x0012[J \x000céË´O\x001beX+ZW|ð\x0008¥n)õÌZÒTm¾ÞDy³uX ¬\x0014¹0ÑÌ¬¤ÊóJz/óÚ\²µò½÷n×BºÙät\x0015jVRºnÏRâýáÑØjêê'wo?Þl¬ÞÑÁIOöyèkîyÑÒÂ\x000bø\x0012N)àyrýìÕÅÃ\x0005<x¤4ªÎ>R\x001b²`|ÈoïÊÇ:ùp)i0
­Â}+\x0015Úkù\x001f>|ü¸ÍÁ`eÎeÚ\x0006Ò26\x0004q-\x0017Cæô\x000f/^½zØÞòV¡½\x000fpbYkÓ&f¡g§å5¤U÷sêSOqÒTDæ4UÉÃz©ñ\x000f²[9mËig8=\x0015¯sÄ­mÕð¶^gÜ\x0003ÑàVN×rº)Î_&
g\x0010=¤t\x001fýéÖªF8}Ëég8¥z%CÊ\x0018|UR¯¸Vè5Â\x0019ZÎ0µ')+yB~&´"µ±SY*yKb =k'W¥á»íE;t\x0017í\x0001PzùæÈ$jé¿3Z&a ^T"ß

æk¢§é }yóîíÆz¡*O
Qº]¥µÜ.ö-I\x001bæË«g\x001b0mi§0-Èæ\x0004rF\x0005\x0013¥ç9\x001a|¨x#¦k1Ý\x0014¦®y+ð¹^{q\x0005s±°e\x0010Ó·~
\x0013L\x001dOé4ÝýK$bªþÁbÝ gh9Ã\x0014§òUøÀË aåÜ@Í3P6bÆ\x00163ÎaÖæJHW%VSÖàÁ³y¶a¶U©æ«n"ÓfN¶$çyÀÕyfd3óAq÷ Øâìiñ©Y®\x0018¥\x0007§8läìl'Ì\x0019Ï_³³J0gþw9õ½H\x001et¹£úZ\x0006Ø\x0016Í:Ü\x001c¬ÔO;ô§¬Óz\x0005ã×¥Ò´\x0001\x001eç5-¯æ5VÒ$\x0010j!;}»t¦fxmËk§y-ÒÕ£T-êg	XxÍÒì\x0019^×òºi^ï¥\x0014	\x000c¦¤cµ¶Ä\x000bKö3¼¾åõ³¼Q\x0005-¯bÕcöZòÁ\x001dµCË\x001b¦y©L¸àÒd­t\x0015q\x0016·Ô$7\x001b[Ü8â-¼F,\x0019õ*øÍR\x000e}\x0017¡Û¾\x0008ó\x001bØJÒ\x0007ÒEÒ¨\x001ej\x000cópÒg\x0003°2÷3>¦ÆúÿøÏËÞ~üxóã,:ÀiÖ6\x00005cPs\x001cÙ6ÑáXìB,¾âìòÕëg¯^]<}\x0016[Z¥M4"c`¢\²"éÛ³
_\x000f\x0010\x0007`u\x000b«§ÖZ¹Ã \x0013Å\x001bO
®L\x000bE.Ã´¶¥µÓ´ùa\x0013aØ«T÷ìaV×²ºiVÔü
Á{SXµ\x0008õ+³4ð`\x001cÖ·°~\x001a6ÔyUHª,9
Î]ª°X1L\x001bZÚ0¿ik\x0001\x0011%sem8R½Ó\x0011´±¥³´H"¹¼¶ÊpzÈ©\x0017[·XZ=JÛ&ºËØð\x0019\x0013	rêyá7lO¢Ä²\x0015\x0016\x001fÞq{×0í\x001bÐ(I¾AÚ¹ÅÜ¦ýì«RÞbéÈ0nç\x001b`Ú9 ²Òf\x0004$¶\x0010y3@ÍÆ\x001cbo¡ó\x000e0í\x001eÐÔöÈ\x001aúeq#oÝ\x0010\x0016_iMGk¦i© Ûp\nù½Ðs\x0007\x0006B\x000eàvÎ\x000c¦½\x0019\x001a-\x0005 DÞC,=Iiu}<ÂAçÏ`Ú¡¡\x0006y3\x0014 \x000b®¯{a±4¶sh0íÑÐ\x0018QÚHÿ¶ø_¨\x0002þ\x0019À\x0003.â^!BÉAÄü,
¤¡ªq#Ü¯\x0006¸'=xG/	g¼y»±.>Êµ'¤@Õñ«C§L|X¡é\x001e\x0014ÎþxñìÁÏý\x001ai{\x0002Ô!Ô\x0019O\x0006Ï¥ë Î¡Z\x001c\x001f:Ç¬[f½ÙV),ï¹ý@Im¤	\x000fë-\x000f!\x0016ÙìAöFè-5B\x0016õ.ë5ÞÃÔ¶¥¶{¨!HU\x000c\x0012ðS¶RÙiôâ<Ô9j×R»=Ô\x000eù¦\x0011¨áGd\x001fë9\¼hÌ1ûÙï`¶ÉÄ±\x000e\x0012ÝD\x0019ËÔaë
\x000bÃÐ±{ K)G¦&}\x0002]k:Â#ê<\x0003ÌÐm\x000eØµ;\x0000ÎeKëÓÈqi³¢©RGA\x000e:ìÚ\x001eª\x000eSê43»\x000e\x0001U(
`¤æ³oQ{°½çÔ\x000f©ÀÆ¢ê\x000f\x001da·GüA~,Öô\x0017äÇ¯n?}÷öRô\x000f?m\x0014gÐT±À+}§\x0010DvõR tuùêì»g\x0004¤øæ!J-1þ\x001euK¬\x000fÄ¦%6¿\x0007bÛ\x0012Ûß\x0003±kÝïØ·Äþ÷@\x001cZâð; ®é·bÕï\x0001¹w!¿\x0007\x001f\x0012;k\x0011÷\x000b+iCKW\x0015.ã\x0011áPö»x­»÷D\õùæÿ;ôzH\x0014ï\x0017ÅGÕV@_¼ÿñííûgO?üüÃÍ§O7ï?m+<$å^\x0016ÒOá>òx3c¤»D¯\x0012PááÅó§Ï.¿:{úâÛ'\x0017¯__<½á\x0017ö\x0017Ý¿Àê*ß¢Ó\x00161\x0006ªÜ÷º¶þä/pí/pû2T	Rzg Î;2[\x0014Ô´Æô/\x0008í/\x0008»\x0001\x0017×Õx®\x0013\x0005\x0018\x0015Wz¦Aó¦áöÿ\x0004Ì£<\x000e×¶\@QyJæâà\x0000ÝQýgÙ`
×éPðè\x001c\x001aô-?áè_Ð\x001deØI\x0016Í¨ÖP\x0003yG\x000e\x000f5\x0013ý\x0004£î%]jG}<{y{w÷ö¿ÿïÝ¶~BL'³@[©¼|Ê¼ezáx 2úÕÙËËëëg×\x000fz\x0000&Ö-±ÞA.Â2ÈJl\x0018½%H">.Þägmlç-\x0014¹J@©ç÷èêÛA\Ì¸\x000e!+}¿>Fw£ã¾~oÿ¾\x0005Jº<\x001bv¯dºu<é¾À\x0003ïËé?#Q?=Î-+Î²ÖHQ;\x0010ÁöX¥^iòñ\x0011¬ºeÕs¬4Õ×Øbª}2Ûâñ\x001f\x001e\x0011¶\x0019Õ´¨f\x0012µj·\x0011*òÓÀ\x0010ð'û\x0001TÛ¢ÚyT®÷&©\x001a©å"\x0011\x0015	\x0005@u-ªD¥ÙÖL¬ÿC§­jê<TA¿Ô·¤~Ôôf²] ¤¢Pc\x001eìÙL\x001aZÒ0GJÅ0ñ4t\x001d\x0018ÐÛ&i-\x000e@\x0018f-kd\x0005/\x00113\x0005=ÀOÈNUåÅÜù(+ôN`Ò\x000b *ªcz¯]ç\x0013¤a;Ë
¦\x0015±F`\x0006=¿³Ñy>þåÆîÍ°\x0018ûÜbNE4§\x0013woHUK³\x0017é\x0019'bK]iµ]á\x001bìæû·û\x0016Üï\x0003÷ÕQ9.N¶R´\x0011ý¢\x0013Å\x000e-vØ\x0016¥	i\x0014cö\x00136X\x0014òÿoÎ \x0003ìC§9f\¦b©©µ\x0001QÚ\x0019âCÍßÛSb¥ÝÒÑÔ,ýåûOw·gÄ\ªÃ?ÖÓ¹)ú*wob2ålRÔ+­ÁKS.¿¾¾<#ìR&þªÓ\x00072dô\x0003lú	Ý\x000f ÿûÎ\x0000$-)ï´æ­l^¬«Úõ\x000b¾ÿË\x0017¿á/{D¨\x0013¤zPJr½HÿÊÐ¯x|#5µL²èoöý\x000eô'åíS\x00185÷h\x0016lýÔïÐù,»Ó\x001bNá[~\x0004;{yG¯¸7É¤S}|\x0006#\x0013d|\x00153×\x0003î¯.Ï^^ÓãíDG
bI\x0014ñ¼|wóãÍÙ?ÓUõöìòçoÒêÝ¦Ü**éGµÉÚ\x0015\x0011\x000ewKÉ÷W\x0017O/Î¾~CÕË³Ëo¿½xþæòê´Óå\x001fªT÷\x0012\x0019¨T}swó>íô®àÎ\x0015Õ`¥ !\x0004\x0000éÈ.[Ço®/§]þñqNl9q3Èºj\x0017¥«'DÐõZ}\x0000§i9Í\x0004§Ák¾§\x001aOÙÅ¢ø((D2vsÚÓÎp¨Ä+jR}eEBOù5ñ\x0011N×rº©õt¾\x000eÑ5 E\x001cÉ{Kà\x0011Õ\x0001ßÝ·~j=\x0013¬§
Ü\x0004áNíéJ½\x0012Úp3L­'Ô\x0004 ¦hù`5\x0011\x0011ÌØbÆ©åL{R¤Å>çNTÒ®c\x0017\x0013Sc§çl=Õ\x0014§ËÒRe9A4±\Ðò\x0008â×
ºF@{3?cç¿4rÇÃ\x0014GD³¡~x»X=\x0008ÚÙy1ôéËW­&
ÙF\x0015Q9]\x000fÒZMð\x0008¨î@õÔZ/\x0013`0X±ôVW\x000bjÖ4]G@;\x0004S.)AQÔT>½+we\x001a\x0016êßÙ9$òH¤Ï¸÷prÈìê~ÐÎ#ÁKò4cÎÀy(gª  i!îçì<\x0012L¹$Î9«³¡sµ#Àú*&·öº9\x0002Ú¹$òI.]DX`¾<Û&ce\x000ckúò\x0007¬hç`Ê+9®9 m>-rM§åÜ¿Ø¹$rIiá¸êº1\x001dW½\x0002ú\x0003¬\x0012v\x000e	§\x001c#y\x0019>FÖ\x0003t\x000ceN³ßsbñrHN\x001b\x0011E«d`ö\x0012¬pvþ\x0008§üÓ ²\x0012ÔÉyÚI6mÛý ?Â)äÒ«.P:ÛÔ\x0015U\x0007\x001cwì<\x0012Ny$ZZª(é\x0019ê]^\x0019V'v\x001e	§<U×\x0018S\x0014ÊºÆ\x001aUí\x0017_Ë+v.	ç\R¢ãl\x0003jÍÙÌ´¢Ú×\ìþ['v.	§\
@\x0011HÍÓó§WJÆþÃÔ¹$sI*J¾>½¬¨®bHá|îì½²÷6ÅJÞT\x0015ANà`Õ½³0èHAlgFP\x0004s\x0000gIÏ®?|þi\x001bh2òüéé²Ì:èd²£SK§$"Ëõ7ß¬¡ºï«¤yñLå/\x0016Êç\x001f~º}OyQ4Ó	çÕí'úïKQGIH	!}\x0011*=¥Qå{
¥ystuùúõõ¥t¶<ñÍåóµ¤h\x0003¨[@=\x000cîÅ\x0001ó\x0014ë\x0002h*`«`1\x0007hZ@3
>­*àü9ÉÁ\x0010 Â\x0007cSðìö\x0002Ú\x0016Ð\x000e\x0002\x0006RÙÉ|Ê¥[FþÂ5/ø`/]héÂ(]\x0019\x0007ñ¢¦	g\x0019ËW\x0013Æ½ßÓ3\x000cxªöÜHH£Ý]9"é_¡"çLhd\x0007RJy/!t0Jèxü\x001føäøÎù\x000b£akö\x001cö} ü\x0005½\x000ft&ûóáK>\x0013|úªÕÂ áóA|_Ð5¦úQ4Ý¢é!4\x0015K(­Êê8\x0019
J33¡ù/\x0017n\x0004Í´hf\x0004-ÐDr_Ð0OL¡o\x001aMQJhaaÓ Ù\x0016Í\x000e¡ÑkT`´WËh<b ¡ù\x00051æZ47\x0006¬qÐÒ%Flï\x0019Ú!Y\x0013d¡%\x000b#dã³¼hÆPâ<£q-WB­>Ì8ZkãJ
z;óº¤w\x0012[úG,Ëæ¢ã\x000fjÑí:\x0006Ð\x001b!ëá!«­u\x000b4MØ¼µl=¬Ò»¬\x0007`Ç¿©uë,\x001b\x000c6g|éÌ!6s^Îhº0\x000bYØe= 3l0dÙ\x001c©¶¸âN%}PB³é"Äl¶}`ë,\x001b\x000c6êóæ`S¢ªÌæ¼¬ÝÖY6\x00182mÖÛsÇqRò¨à\x0018Í8Fs\x000baæ\x0008ïØü\x0008\x001bÍ\x001cVüI-I|\x0012\x000eåB8ºîA\x001dZ\x001cB\x0003S·$4\x001aÞ\x0002Íx^6°kÙ°³»8dwMàÉë`Ê'5,ß>iô»N)vv\x0017ì®v,Mn54þºRôAn5ÞìròØY\x0010\x001c² T\x000bíùÆ\x0010I°7Rî<IhÆì\x000bô÷?ô!å\x000f¿©pûN+ÝÍHD\x0002
]\x0004EON9vsAb·}\x001eK&	×Èþb$¸4\x0002\x0018Z	ádõÔ\x0006øæîÇÛ_¾VY£üE«Ej^?½{ûñq8méþ\îY^v^ä)Eôe×/ÓWgß\={µ¾?(\x001e·(^ÿI&¦ÔS\x0002¼øñÇ·ïÏ¾¹¹{ÿ¶L5|80ñEÑ&M\x000f
9hRÊÖ`óËÏ|uvñôé³çgß\\?vy½wú+Æ«uyû å|ýáóÇ
{tEKÆ$\x0019åx3*¹ú\x001bý¥\x0011Ì×/Þ¼zuñ,Ý]Aí÷ú_ù»\x0013	Í¯JçþÙwoß½»Éé;Ïõ©V¸ÞÝüÃÓ\x000f?ºýø1ÃtN:eN\x0010Ó§¥'zs\x000e1KÔ\x0010_ô]ãÕ\x0005µ\x000e¾¾|¾ñÕå\x0019	)_¬¦ïhCºöf]þBvåË»´9Þþrón\x001b(IÒf}Ä\x0004J6'fP\x000ceþK\x0002í*\x001dZPÚ/¯=úìåÅªîs\x0003-,ÎÁ¦À*\x0007\x000bTIZ\x0002\x0004ë@VÕw7¡\x001d°ºÕs°\x000e(oW6ä¦XÕô0_`m[³\x0007Ö´°f\x000eÖpª4­¬R\x0014ZdX(£Ui\x001b¸¶maí\x001clrÝ¡,l²V¶-\x001d\x0004ÕØcH]KêæHC\x0011Ú¢Ã°2©ã¤BÌM\x0017°úÕO±¢ueâBu®X~ I@au\x0017\x001bí
-l¥\x0016!àÃ¥è\x0019"Ã¢5~Å¾\x000eÂrrDl¬£5¾Ô£\x001dëhzA¦åºL¢moì¡í=ÂK ÒfÇ»Ö\x0000éT\x0013­\x0003/k\x000bê]\x000bK9!{Ù¶¹Éh-+ÀÓ¶u\x0007Ñv>\x0001æA±hIT½,mÔ\x000cë:¹=°O9§ Q\x0015ÁNZÚüPÖòã@ZÚ£6Bç\x0014`Î+\x0018\x000cÍÒòÂ\x0016ç¼°Ç\x0018/è¼\x0002Ì¹\x0005\kF\x000b$uY\x0016VÌ>\x0006µs
0ç\x0015\x000cÝúx\x000f¤è\x000b
ªg´°þ \x0006:§\x0000s^Ád6¯+	ùbÙ\x0005\x001e°Z®ìlìhãÜ.\x0008<	Q\x001bE\x001b"Ój¹,\x001ed\x000c°óa8çÃ45é³ÇM/>Ì2² ßhÙ¶Øù0ôa2Ö2­-F\x0018ÉkrÄ,©~\x001fBÛ_kæ|Xº¬;.Oàù)q\x000b¤p\x000cmç\x0016pÎ-ÀóaÈ$Jë5I°Ç2ìl\x0002NÚ\x0004êÝ)´ÆeÍLk\x0002G3ª ÕÝ)Ós§úô¡2Ö¨xßJÉJ¤ách» '\x0003\x0004g¨êh1Ýt<[0Å	ËDí\x000eºâbM\x000eÖ\x0004BÖÔ\x001fgVÑÊ
S$ç;¸î3\x001dµ`\x000fÀâ}ää&&uà\x001bÉézâ¤n<ÅnÛkïglÎ(É,±ÏgßÞÞm¤µÊTg²\x000f4ó¼x ¸ª)íæîÝ¤¡qboÎ¾½¼Þ-.Nâ\x0002ÔËY
\x001a¢f\IÓ¨x\x0014­niõ$­¯æR`%Â\\x0012J\x00190\±fÃ´¦¥5´$h'90 ÞÙ¼¶VÙÇ.¾Ûpõ÷?úýxïfÍë\x000f4\ãöçÛ÷ÎÞQ\x0015Ôç¿ÞÞdæ,Câ\x000b²þêÛÿþ¯»¿ÿÃÇÏwÿðêöíûÌë¬³P\x001a=Ñáib!\x0004¾Y0)öÉ¼×:{õæúìÕå³ç_]½ A\x001bß^>}vEuQo¾»¼Èàkz$\x001dwÚ·ø{äN;Xÿ\x001e¹Ó^6¿Gîôßh÷rS\x001dL(Ü$\x001bè
w(¹Sâæâ#¹ùt»¹Í¹`ë2 alID\x001c"\x0017¿\x0017[ûºMl \x0010?só$Eâ6ápîôß\x0018vs«"\x001c¸)ñÃÜ®<
\x0011w<~¤KtÜËÄÉÜ¡è£$n[²@[÷\x000fä®\x000f»À!ðó\x0001\x001a~Î\x000bn¢[u<8ùËÝ\x000e\x0013Ô9\x0015Ïc°m\x0001çþã\x0004\x001eøÝèHðä-a·Çüÿ\x0001Ü%ìu6DÎl\x0018jY´\x000c\x000e%)kÁJUÒài)`¯Ï´!°
Gß\x000bw\[ùÃ¹W½>æÎDdp[D?	\\x000b7\x001e¿QÒ\x0017½>ÓÆ@¥~ÛåºÉÌ\x0018\x0005üpßC9fØí4\x0015\x0016©]âfEâ\x000eì|¬>Þ\x0014¦ÝNÆx
w(rðdQ´\x0011îã÷Ir°ÛiªH\x0014ÛCé2$nÙ&Ú\x001d~.)\x0005û}¦)º×ÄmJÓa	+øñA
e£q¿Ï\x000cç|.½ç\x0008EqD.ÌG²1ÄÝþ\x0012±´\x00125\x000b\x0018æÐJÜáIgG'_»¯èK]\x0002§n,6ß\x000eÅ~\x001bwü§»ï4º\x001df°e²\x0007ûºâñpB-ê¸û©YåÀ#ÅµåÖSÔ²\x0012¸Åã-Jò¸û©\x0003?Ã\x0018X=½\x000f\x0012¢XV©9\x0012<-\x0005îvFEÒ|=\x0016KhÝñÜÉ]ânI¹\x0013¬\x000b\x000e\x000cÎs#\x0008üøû1õ\x0013àniñ\x001c±nqÅ;5ëó\x0016?\x001eônI7\x0006Þ)ÁþwâNl?ÜS¸¦÷'fÝy¬Þ'\x0016_\x001fyÌQö>o\x0014>¡Þ
§àÊ\x0016½\x001e\x0002·5(ßÖ¨òYïvNñS\x0002WTUQÀ«-Ô<AâHðäÏôn·Izm|¯7EZ6G³I	öø<¦Þí5ÕéºªæÜ´\aTÇïôß¨w{MêÄ\x0003\x0006·52Ô\x0012`x|.*§õþ¦¢Ò«\x000c®-ì¦ØBe7âiïé½^.ö¦¦ý]ï"
r$wò
z¯Ó$ ÆNñâ«\x000f*R\x0000\x000e_o\x001c¦Ùí4ÓÉä,>eÜÌSÂm\x000c{¡Ó¨cNÿufÿ\x001d\x0013JËgIþ8I(CÍ¶ùÃÍ \x001d\x0017³ÛajUÍ õHËÓ«\x000e3\x001cnM¨xÂìv4~#+U³m!HDhÌáæ:sÌþ§LËeÿi§(I[Ez¶ãâ\x000ewôÔ¡av;L§¹'ÁbN"([Íàñ\x001b%}B³Û_¦m-18¸s\x000e¬ÐÔ\x0000Å\x001d2C0»Ý%
\x001f`îä9Ù¤D-ñÇãÍwZ	³ûnåªFÝ8®\x001cÌ(wcs|pBsKÍî\x001b&¥4m}ÊtuXyÊÔÛä)íþ+f«1½y{d{RêÍáÑ	)ÈÚ½\x001e\x0014×\x0002'4\x000c²pû\x001a~ûAóý§\x0004Ýë,©y@Ê9b}S#
Â<¹99\x0002»ûý²Ö\x001aà\x0007zïåÑuôNù\x0018prv÷»¥Å":B'Ñ\x0017\x0001ÎÄ,Èf0	û\x00182Uùì~²Ô'ãáñ¼¸t¯«é\x0018t0!§aw¿Vb\x0010ï\x0002É`sFÍ£\x001c?wðñK'ÃîõÄT¸j#\x0018y©än\x0013ÚÍ¹´ÇÓg³{½¡½!I22k8;\x00189ý×Ù½®Ðpîk¼¤Êùs^Ã±»Ù%\x0007èö:AjüèDµTåª;ZÍó\x0018sú¯s»\x001d`òzo0¦Æw.J<}0rò}n·ÿ£i\x0017Á\x0011
§tÂ±ÀÉ5¹ÝÎ²bÝ\x0017-[ù±ÄÉ3¹ÝÞOë¢±I§/Ç{®dô}\x0019ù_Þþø·\x001aî?ç\x0019c7¿ÜÒÄ½Gy\x001d\x0004ËÕüÚkÇ%Ñ©ÈÛBÑÈ\x0007¿Î\x0003Æ.^^ÒÄ½õèóÄüeýö(s$á«l\x001cÝi32Ï\x0006LÈö±¢Üaä/K·\x0007Q\x0005ÎjoÍyÐ¦\x0014f÷X}ùË²íQf´Ü:\x0003É\x0007dfg¼0ÇGÂÏaæ/K¶G8Ä\x001cÙD\x0017<VæGbüaæ/ËµG­h¤ýõ9Ù+É\x0014¤ý|ôÞø²V{9Ý±\x00033'\x0007Ì\x0012*c^ç/ë´}ÑYKÌÀã}YÉ~ÖU
3Y£=¼7X01§ø³Tò§½!i
eFê³\x000fa\x000e?ueS]§ç,ù{,ñBaö(±7¹´Ìy"GöÕlÀcÉÑaè¢ìáý¬Ê\x0018ø\x0004nÑ½\x0001Riûè{Ü0óB=öOñbë"\x0007ÍO9zs,b\x000fH±L±,ë¬xstw(\x0003Ü\x0002·AúðÉþýs\x0013ÖÉüäooî>ýý.}wsvõöÛ»Oo?¼ß\x0010zÚBèJjU}­tJè\x000b&OÆ({qýúO×ylìÕÅÙÕ³'×\x0017¯½x¾å\x0017iÿ/ ¹3Q\x0010EYò0'Ï\x0016Ê-½Þ\x001eñ\x000bJ,rÀ/ðR¨} ¹½üðbdû~Éá¿ xùý¿À+ËÃé\x0017DúÇü\x000b8NPK\x0007à_Püçþ_\x0010Rü
å\x0013d2Lú\x0004£\x0015¥ÔÓ\x0001?@\Óï÷\x0017¨ÒÿÕ©\x0017ÿ÷ô;ôO·7\x001f~hCÞ,Ky»%õ ï2Ú\x0016¯l:MQL³*ªÅtåEV£l´(Wj\x0013Åv$Íc`Sh¥Pr\x000bÈ]ºi÷\x0000Õº÷í@ia8\x0002qJse÷Ü
v.Q­RÞNä\x001d×è\gÅþ¯Rh1a;@$Õ°èK\x0012=8LÄUSÀ\x0005v*­>únFò4îº,Moñ©Q9ùnAædÍ"Ñ;\x001b:m>äbÏrkpekGUk÷eþá4Pú»Á5\x0002	Té!¿t¬'"©vS{:È_¡ÓæÒÈ\x0006©¶*ÈÞ\x000e\x00153Û¨=þg`\x0005¤²^'\x0007\x0006b#õbçÂf$ $Vþc;SPJ¢u\x001a®\x0008¼¹\x0017&\x001bv2Q\x0013\x001a²\x00013¬ÖóPR%¹Î\x001dÉN |cÏWö\x0001 _$\x0012\x0013rñlÌI\x0016fZìæ\x001d`¢«b¾+\x000e0Ùs6JE,ï¥è\x0019),\x0006ú#HÔÜ»[·#YËÅu\x0004\x001d¡\x0004+"0\x0016sã\x0003HÔ·
C\x000eÎ§ÏåjTRÊÌcò\x0001V>Ü>o\x0002¹%\x0015Æl·ÏÖÌT+bÎÂ\x0017&X|ó\x001f`¢\x0013\x0007c'.xîúÖÔG-Öû6TÄÅ\x0017ÅÍH\x0014s}ÿØä[V<u\x0014Pd3¥c)_³\x001c\x001cy¹àòÃef²\x0014szQyXl2ßÎä©sÕ\x000fÙ¦h#×hª\x000c\x000e\x0011#W(g\x0017\x000bû\x0007¨)þ\x0018`Ò¬òþ
ê([\ÆKÒ·û¾\x001d©/ç?\x0006H\x001aW¤ÿÐ¢ì§¥´Â\x0008\x0012õ6ú!{\x0019Ò&C-våØñÌ´B\Ê¢\x000e åæ¿!ã\x0014ÒnâX×¤Í\x001eê\x000eçð;äòÃ\x001dL,A\x0018
QÇç^!mi³\x0017#Nÿ:{Åw\x0001$úraìË%·R4*µû®"\x0004ÎÚ« \x0017g\x0007rÿãqJ\x0001Aé\x0005ËßÅ@s\x0008~À§£Ë\\x0018ò+4¯hÐ¦\x001dî¸y'\x0002÷î(\x001fqß\x000e§UÆÁ <ðöFä2zÞ8'àýRw;&[ÿ\x0018Y#\x001b¯	Q\x0002Þ\x0014
ÊõRïe¢® 5¶hl\x0007ï¥\x0018ä\x001d-Å^¦îï]\x001fNSü­Çð´\x000eòèDRÑ×	½ØåNû\x0001¦ÜI:äè6ÔiTb\x0019óNgN.\x0006a¹|lºDaÈÑ\x0005íX±^[RÇÄ$AJ°P\x0003LôX1vYIßÅÓ\x0013S¾\x0004g&ã+Óbü\x0000\x0013õvÂØÍ×J£DºAiIëõ²ÇÝb×\x0000\x0013u\x0011Ý
\x0013}^mõÉ\x0016¤ð\RMûÒ(dQò\x001f#î\x0017Îåî«¥\x000c\x0000¥t\x0012»û¶8%ÏôXÚ2\x0004Ì\îãIº.iß§³¹åvìò\x000bÈ\x0015Æ)\x000e\\x0014\x001d®!¯Ú÷åhó\x001f\x0003\x0019°èI1#\x0005'\x0012\x001f1y¾z5Ø¹LÔ·iÇné¨qD \x0015JWl¦´Nz×\x0015JÓxþcÉi©(2ó9*ÐF\x0002qÿàµîÑ×\x0014MùíTL8úP»ãä.Y\x0014\x0005\x001bX$2Mc)g\x0017<ùÌäÂ9²Ô\x0000JÚÂ-\x0003mg¢ë\x001e»ÓÑfâ»dèé¾l&ÇvÀÆE±º\x0001&²\x0003c:ÊÇ\x0017yä#%	\x0016d~Tb}ÉyMBùÄ3°HQM
g; \x0011¦Ùw1ÐT?ÿ\x0018X%k¥N\x0001|Ö°`M\x0019¾¬Øe9³\x0001&:raèÈ9ª.æjX¼\x0008\x000b)arzWàdÈÚæ?¶3\x0019R\x0007,LªÑË\x000eO\x001eP>\x001dìK`\x001aª<É\x000c0Ñ\x0007+»	µ\x0017
\x000cg,39\x0015v¥Rr}\x0019K`:\x0003\x0012`Ò¨\x0000Ñ(¾nå»e¶3QÌdÆ\x0002'R\x0015æe:Ê¤íTöåy
Ýó\x001f\x0003H(z1Z£á\x0013éÃ÷
íÛhÍXD\x00105Ê]S§\x0015Àt 	L??ËDÁ\x0019\x0008â'±ä´Y-7\x001a%A¸\x0007»ïÃÑ=5ÿ1`Á#J\x000eL«Úw <÷]ìÅ\x001c@¢\x0016î±^\x000eÙ©du-~\x0014\x000b ûÛ.&mg¢lþcä\x0019ê=3Å\x0006½¬Û;]évYp\x001aüõUþcì\x0019c9\x0012\x0017N\x0004\x0010$\x001eÐj×2e½ÒüÇ\x0000¯Ö2-\x000e·Ð\x001b\x0014#áT.üGÿ×©
F6|ÿ¸ºýxö7w~û~Ká(5¢sRÕz¾\x001aÐH(ÙÂ°äë._ýãÅõ×Ï¿ZhÛQJ<KûåöË|úÇãÔ­Ï\x0019q1S°\x0001ìßÝß>þ\x001buS\x0001\x0015Úä?®nÏ^Ý|þëÍO·\x001bêÃ\x001c\x0016m\x0003ª¡¨ÇPÜ¾vöêâÍw\x0017ß\¾x¾-ÐyPl^i)RÁd\x000bÊ-=,Ãl*\x0019­Åï¹Mr\ù{ú¶\x0006x ^Y§
·\x001aÑ½&/`UµÔ/õu§\x001aåÅ¾³
-$NA´ûÎ¼£Þ(ÂÔ W8ÃRlú%èÚ]µ²êUÏ-¨GÊ\\x001adK¹í¼¤"±£Ò´£KjZL3·¤wç%Mç1£®¥Òe]\x0013Kj[V;·¤¦ÆH¹¨øZ%}-\x000f\x0015¦\x000f°ºÕÍ­«
,}>?ÒÀ¼® ³jI-t\x0002Õ·¨~nY1Y(i¾\x0001\x0016\x0008ÉÏH\x001dz¨Ö|5´¬a5\x001a\x001eê©½QB\x000fQKû=h\x000bÄ5Î±¦-À©uç-\x000f&Þ[¶üém²\x0001±òôd1ÿjÒþç²·ÒôÁ\x0007«PI\x0017ä\x0005ÿ9AÚ;ªIOEÒõ\«\x0017\x001cùý¼¬®îÖMõAÃ
¯9g>zµVôÚSU `î\x001c\Ê;O,jç\x0005`Î
h
ÊÅ´æ©\x0019V\x0002¥§Î	ØÎ´Âm¥A®\x001c\x0006î\x0014\x0017±\x00046Ê[`é½q\x0002¶3X0i±°>?¸ \x001a¯1(B·¸$\x00128\x000e\x0015ÀI+\x0000Z\x0012mtcÓe\x001bøzùHñË\x0003\x0016\x0003°}08yÀ~-Øîáä\x0001ûµ`»\x0003\x0007ì×í\x000e\x0018N\x001e°_	Vw\x0007LÿF\x000fò¶¿\x0012Bcãh¼»ý|ûéqRk\x0015rÏÑÊpI|¢é{>Y'}ruùæòõ\x0006Nl9qÓØ*\d\x0012!cjÑA° \x001f\x00076cê\x0016SÏ,'=«Õ\x0004%M\x000féf óvüÀí0¦i1ÍÌj¦03)H]Q¥k3]gªvýC×ÁÍ¶å´3Ë\x0019P\x0006tÑõEæ\x0000)¹\x0007Ø°TJ3ÌéZN7õÙÌµÒJÉöô¶\x000e_X|è\x001fæô-§àÌó x=\x001dJw\x0004Ú¢Á0fh1Ãow9cË\x0019§¶gäV\x0019££¢U¥OÆ9³$³0Êyºøe#¯~³\x000b
½7rG\x0004Z8S\x0014Ív)ÙO¶KN\x001fqÞ¡óF0ã,©WÆº NÄ\x0013ê\\x001ew?Î\x001fÁCB©Ð04afx\x0014É?wCÎ!ÁG²AË\x000c
<\x001f¥*fcýRÝÆ0hç`Ê%!\x000czæU)O¤òü¸Ñ0gç`Æ%©w|ä5Ö\x0011\x0001â8ãÒãà0fgéaÆÔS\x001f&ÏBÓ\x0016O\x0003®xwª¥ÖQLì\x000c(Î\x0018PW¦qc¤HF¬\@õKÊîÃ }<eb¨ç=B-z@««Kz \x000f±\x0019´;ð8wà£Ì\x00176ÊK("\x0000à\x001eÒzØÙ\x001d#ì|d]\x0005cÀ
¦\x0012	nç\x000eùîÝ9Â©z?9k©©2z`¹Ôt\x0014Tw'IO"ÖR=eùî ¥éÎ\?üÒðÃaÐî$é©¤
÷Ð¥XD×\x0015ÕòZê*>9»¤§\x000e\x0012Õb3§Ót]Ê2
ä%\x000fàìN9I&jn\x00004Ú¸z\x000f"\x000bè²øõnÐî(é£d¼qÖä9ù\x0012OÓâ;¸\x001cî(£d \x0014\x0015Wá;#¡
KÅ·ã6ôû{Vôf&}£E*;²V}\x0015Ì0ûVÔ\x001bÕ'Ò_´I¦ëÛ¹¹ÛI\x001an\\x0015ëµ\x0012ï\x0019#T9·ðqº¾üöåÅõ\x0016RÓß2©kIÝo4´¤á·L\x001a[Ò8E"&W\¾\x000e¥êÄ<$|·\x0019ôxðÙZMZÏ\x0003Ö²4·}À	¨¥êÒqPè@a
\x0014\x0014zûdõ=kH\x001b?,vYêTÏZéó)FáAZHuÆQmjçN?\x0017Ò,\x0007IC¬kºT°7NÚ\x0019)²Rî +N´<ã«\x0018ª8ôCÏøÛQ}ê§\x00165}ôÈ«j$ù1W5\x001cr¨:3\x0005sv*z\x0011òõv\x001fU°RopÈ÷ÇÎNá
ôp\x0013ê¢­\x001a\x0014îyQý\x0011¥Â)K\x0015 6z«Eã\x001e\x0014Ö³¥qÔÎTá©¢v\x0015\x0015¹F\x001d¼9\x0016µ§p* 
QËà\x0000JÚb\x0004S\x0005\x001fªâÚNÚ\x0019U2ªÔó\x000eº\x001e*ä­ªeTÕ²ºË8jgUqÊªÆdÿÔ\x001c"¹\x0018ÑÆZntÈñïl*NÙTR§±ö´ôÇÛºQ\x001fJmGíl*NÙÔd<kutb ª5u\ÄR7á0ªî,³T\x000eD9¦\x0017Èñ÷PÍÿ$Ê8jg©ô¥òêË¸Ì/P+ãÝRSô8hwúõÜé§4J¨\x00015k\x0018¢\x0008)Qô÷@f;jw¨ôÔ¡dýyQÁª\x0019Zf­\x0016çO\x0004*Y¸\x000fVZEâ(Pó°·RÎÍA`\á¦Çl\x0007\x0006\x000c}Õ\x000ePæ÷«¯.þzþ­³§ï>|zûîÏ·g_ß¾»ùôáóÝ£À.]Ði"A)è¬:ÿÚÕá\x0004¸ÔvrñÝåó\x0004ýtè¯¾&ú«×/Þ\?N®[r½\x001cHH¤ÿ}¬}
¸ÕRÛÿ<¹mÉí>r/ñWZg~Y:\x0014wÅ¥·ßyrßû]ä¨Î\x001dk²&ÓÌP:ÔRõ¥Ã<xlÁã>p][-Èà\x0010\x001dªPòRÝÊ48ôçsß\x0001Å:eÚ¶y¯ÄZ\x0008¸øÎ5OÞí\x0015Ø³Yl±fn0\x001a»¶2[\x0019sÈ6wZõFÑÑ+Sñ7/ßÞÞÝÝ]Ýüðáý·të\x0007\x0010-Æh\x0002Æ~KaFãWãËg××$\x001dÿäÅó¯×eN*­niõ\x001c­UÚp2m:E0¸z;NòA´¦¥5s´^!ï\x0007\x0003ÊËK=ÍV+´:¬ÝåFimKk'×\x0016¬HôGÒ/ä\x0002\x001d%m\x0019ègh]Kë~ëkë[Z?¹¶ZQIs^Û 
+\x001eeN\x0003ú£`C\x000b\x001b&aIÒ/¯,ipZ7 $Ë4¬\x0015@ÂÆ\x00166NÂ\x001a#m)à±z4XËL0¬µè\x000eÒRûÙÚª9\GÚ²eÛ¦Käw©Û\x0016b¸\x0019ÜÞ9Lz\x0007\x0012Tå¨d\x0012éfÊ¥\x0007²qæÿÍÐbG«AKUºÊp\x0008Ñ_\x0006­q%%1Ûù2tfÔSjù ¥ÈOu¤ðøs\x0006/Igæ?çµµÓ=´¸|3ÕK¡Í\x000clçÊ`Òy1!\x0006HØ\x0019ä\x0019EÏ\x0017Ångp;_\x0006ÎÌ9-Î,]¥h¿\x000e£\x0000\x001a,r\x000cnçÌ`Òy¬F\x000cPK¤\x0010£òÅè\x000cnçÎ`ÒQw!°\x0011\x000buèYÔ \x000eÍ­ÕOâv\x000e
&=Ú¯¶ºØy4õhÑ±M²bÀýü!Jõ¤ök\x0005ý£´CÃIöë-nçÑpÒ£j(»\x0008PµÆ;ÝÝø%A®\x0019ÜÎ£á¤GûÕÌ.v.
gïg$ÀXh!\x0011î1W\x0018Åk5!£´OÃiökmÝÎIà´\x0008¬F`ÀD¹ªGiZm»\x0007»,GPã°S¥\x001dGb7sq®\x0019^)º±,D\x001f¼<ºn
naó}º&zÕ×¡³wÿó\x001fÿyq÷óÍû\x001f·¬*½_qY I¾P\x0012 $?·o?»:»¸þöâùÓ\x0007¶°bË¬\x0016iÌ@fµµ@@i¨\x001d¨Ç°êUO²\x0016¥ÊÌê,N÷\x0012iCÅõ²«\x0011VÓ²Ù= D\x0006½®3¹grÕë5"#¬¶eµ¬èYìÉà©=-Fl­Y/²\x001fau-«Ý\x0003'\x0008\x0018\x0007³Æü¬_X\x001f¨½\x001aaõ-«d\x0005/M\x0016ÔMÇ\x0005mÔÛËÍt«/#¤¡%
³¤Õ³NÐÜ.6@mð^zo\x001bg-kdU¾6}¢:Õ	J¨õKZ£Ã¬M{*y\x00025\x000b\x001bÊì2£u¬ëê«\x000cA\\x0017R\x001baí½Ö¤ÛâÙõ¥AU©y+-T4x\x0000kçµ`Òm\x0011«=u|£ëY\x001d\x001c³®×I·å;?µª\x0006·áÔªz\x0004iç³`Òi9ÒOàUMÆå£gwgfÉÃvN\x000b&½\x0016åcÄºÒP\x000b¾v\x0001OkHëº.M4\x0002Ûy-t[ô¢.ívNú,Ó­@XÝ1» óZ0é¶h¿j¬-þ
k4\Ça;Ç\x0005vá\x0006AíjÞèÔp\x0019Ö®\x0005c°çI×EClK£1T))D'Ý~]\x0007`\x0000\x0016;×®ËYÃ@
Iù"GJz½Z×\x0002\x0018í|\x0017Îú.*t,+ÑpÁ)Ãå¨4á\x0000ØþÊ5ë¼L½s åª®êqí9\x000c¶ó^8ë½4\x0018ãòp\x0002+\x0007ÌÃz#æ\x0008lçÀpÖÅÀzæfTyÎÌþËÛ¥\x0019¿ã¬ÿÂYÿ\x001cA^Ø\x0014Í°ÿ
µÆÍëµw»1ØÎáìµ«Ö\x001d$Xài é`d\x0017èõ¶á\x0011ØÎá¬\x0003K°Ü4Nõ\x00122µÁJw{Ú\x0006ÙÎáìÕ+]h
Y\x0017¥6SYÙ\x0005pÌÂvþ\x000bgýW2\ÜäNíÙ\Ô\x0018.{ÕÿÒ³W/£¹ö=y\x0004uî9sUtç»îüõ_ÎóÀ?c1È«xDéÑÌB\x0002\x0007ÀvþKOç\x000c
¥KÌ\x0005ô°Tr¾1ë
¦#°}ÎpÖy\x0019Ðk¬¶õ
®¥\x0001Ò{}DSwþKÏf
½Ì±QZæ¨Ð\.	½Í!°\x0003Ó³\x000e,D.+3]å\x000e.\x0012
Þ\x001fÕ\x0003Ó³\x000e,8¾Ñ¬\x0000\x0019kïãIõâóÕù/=ë¿¢\x0017:Rëà[õu]\x000euç½ô¤÷
ßâä
<³)ªë
GÜ\x0011tç½ôtâ\x0010i´z±±®Ns<ý.ÙØõf¨\x0001XÓy/3é½B
_È\x0004Np\x0000¿¤bÔÒÐ°qØÎ{Ù\x0007/Èø¼²ÊóüzÊt÷2¤bLç½Ì¤÷¢yÖZòÇ±6i)é²a]ûh\x0004¶ó^fúÉ+]hØ!$ßÀ½F
$qäa½ug\x0004¶òô^AÞ\x0012£ÈÄF0ÊËÛÌº:Û\x0008lç½Ìì£\x0017¥	X¨«äø¶¦7\x000eÉuÎ#Ù$kë ãYd(E\ò>ãâ!·\x0004ÓÙY3kgËhÑåòÒtª¬¬ìAY.Û.;kºwZ\x001a¾Ä\x001dªf¼m<bamg\x000cì¬1Hq\x0001V
<È¡¢ª\x001axk³c¬ýòäñ
J&\x001bMÃ$0÷oñ\x0008+k»ãe'W \x00192üòeU\x001d#®eÜSë\x001d#°Ýñ²Ç+èSÈuº}ú-{ÈåËu§ËM®`¥q)]\x0014E}&ô\x00149\x001c±°®;^nòx\x0005**âKYÓ\x001aÁK_/%íÎ=_Væ]ç:\x0008ÍçËEµë²s#°Ýùr³ç+Ýb8ÕI\x0005&ÖðÅZ`²Þ0?\x0002Û/7ë¾\x0002Ê\x0012Rß
GÊ\x001dX\x0002?\x000cë»\x0003ægÝR\x0006)úâ(ÆÈ]ñeõÝéò³ÎËÔb\x0018ÒÊ³ìhQ2È&¬kâÀv§ËÏ\x0006ºV£\x0003Mi¢EÄvËì|\x0002po~Dú\x000b©à£VÖ·4/qSÝV¹véD,Ò1pð¢â\x0003!ìÕÅ³××\x001b\x0008MKh	ã\x001b¶)d \x001b¸þEE\ÙJèZB7Lh]í×W(#M\x0014zé\x001d×ëC\x0019·\x00120\x000c\x0013:_'\x000fåÔÙÊñ\x0001ã¹°Á\x0016NRü\x0003A±}×\x000eLJñ,¢]Ï¬lE\x000e\x0011\x0011)¸|VTMQ8#­öj÷"v\x0019ÆOsá%Þ\kÒÈw~à	`+¢î\x0010õ¸ÁÁRÍ¦-
hF\x0005¶îm¶òuÖ\x0006ÍMPpÎ:\x0010ÖP,WdÙ¸UÅ\x0007*\x0003·\x0012ÚÐ¯ Ð¸,¡ª\x000fÔ¾\x0014X\x001f­±\x0015Ñw~\x001cQ¦$D\x0019\x001cb²b³Õª£ÞÝaÆñÃìª\x0003½¢;vÏÆÊQy \x0008x+b÷¡qüCÆs;
&¬\x0004fÕ$®'î¶"v\x001f\x001aÇ?t¨ÃséaW\x001eH¥;?\x0019õ+ú#?¤\x001fú}ÛNñ$'Â\x0012áÏr8öò]Äþþ(¤S¤.ÂºPQópO\x0003ÒÒªâbØøâÍë\x001c½¼JØ\x001eçÄ\x0013g85\x0017yj_\x001aÀ¢Qr\x0017SaÑý2êQÏ0&ÇW\x0018\x0003x\x0019=*\x0006\x0000\x0017#QJÓRIJËÊ¸¦±òÅ$ò(¦m1í\x0004&:Í;\x0004Ñ¶4Ú1Ãâ¨QN×rºå
2'Õ\x001c\x0016Cd$â@/Î\x001c\x001eåô-§àé\x0000ÉK\x0007UöÒ!¢ïZu\x001aÝÁ\x001cå\x000c-gùî\x0016Xm!}w8rØmMi-j?RÆ2NP"%°ÊWl3SPÉö\x0008qñÆ0\x0008Y/
Å¶«µLÑ\x0010«Ù\x0004²7-æ#Xs\x0004hgÜaÆº¯±ywiÞx\x0006\x0015\x0003\x000fq1?<ÊÙN±\x0016Tt¢4i¢å\x000fï¤û\x0014çrv6	f\x0012$½ÔÁ\x0007é´NR­à\x0017e\x0007A±>p&üøu¬\x0012`#õ(»4K=\x000e/l¬Ö)BÕ¥w(2
é\x001fvì\x0000ÜI\x0017ÖÑ_Ô.ÙÏg/ïÞÞ~Þ\x0014zj/Z¿y¸|íâ«c¥WCÏ7g/¯]¾y(>\x0016Jl)q\x0012'¦¤\x0000Y+É¯û¤Z»¬
PêRÏPVÝüôßÀù¡<ª]Ô\x000f\x0017·è ¥m)íäZrº	D3\x001fªFã\x0001\x001fÜ·~\x0002\x0012ôéFäXv4äÏÌ\x001f|õ}2¶qRYnMWKWG:Ø KéÖô&\x0006(¡?â\x0013gÛk¹¤«Ú÷&Õ é\x0006¼r\x001bÀìN\x000fL\x001c\x001f\x0017\x000cµô*ÀVbÌªîðÀ'VÊ·ØÌªä;òåi\x000e\x0019[Ê«¶ìªÿ\x0006VÀ{¶\x001d°Úö§ÿ|û×w\x001f>mÉ{ DJF\x0007\x001dK©\x0019ÎÁùµ§¼üîâêÅëÇ\x0001±\x0005ÄaÀP%Ñ95æ;\x001eÞ\x0000×Ú.¶\x0013Ð\x0012RM%?Ðxp.ýKç	Z«XÞN\x0018ZÂ0L¾,_ÑM¨#H	q-ß¿0¶q\x0010³8f&t¡
ß$Ó\x0003à¿ÙLØ<ä»aD«d4¡\x0017|waùQ\µ\x0002ÏíýQ\x001e>Ë~áÙAÆÕÔ\x0001=+Ê"®YðíºCÔÃ)È
|VR Éó-àD\x0018v\x0013ÚÐ\x0013\x0006\x0016-I¾µP¬Ý«²fçND×!ºaD\x0017¹@S¿\x0014¿0ì\x0003]{Øè;D?¨å^cÓÑÖ(n-\x0012ßNØ\x0019\x001c\x0018¶8éöÂÕåÚ:Ç\x001d<1]ÈÅ&Æ5ÕãóÜ\x0011|¦%\x00189Öy¶Z9Ö±JþDN©§C³Û¿ýÔÎæIËËV\ÞlY\x001b_1\x0010LÄ©J8q3\x001cOhn6L\x0001gõÕ\x0014Oð\x000cú\x0014O¬Eã#zÈO£)\x0016l&©$Cj\x000c_lÒÿû^Hð_|r?óÉ·cDÅÃ\*æ½8îÕ"¼ÇI5Ø>ÂÕdÜëáÛ÷·w7ïÎ®n|w{÷ãëb\x0010Yví<4¥ðQ&&øUà\x0014sùüòúâêìêòéÕåõÓÇ©±¥Æ\x001dÔZIïÚ\x0000g´èyWËVX\x0015ÚÖ-´Þ\x0001­äy-¹¨
m\x001dÛ¯VgÃM@\x0016ÚÌC;\x001a5L}j1,÷ <¬V?MPÛÚî¡¶<Á\S}±\x0012j^j\x0017V+â' ]\x000bíö@{I/ipÃ\x001bÄÔ]­V«\x000b'¨CK\x001döPçôP+Î7\x0019´u[¯grF©¡7{;ì^nüä}
¡*!k)\x001cp«ü\x0019ìÎîÁ\x000eÃGRÞÍµ©³ä£{õKÝEØs\x0018StQZAµ¦QÒ\x0017.!sG.uw\x001aaÏq\x000c¥:
±õ8jn
V.®9M`wÇ\x0011öÇàxZ\x001aMH\x0017Å\x001b\x000cN¨×\x0013éÃÐ±; }qdHo\R\x0006¡n\x0011uÜ\x00169I\x000bå(DíYkÃ3t5úF\x0011K¼Ìª8Ã\x0004tgùpåóZÞZ[Þ¥ÝY9³Ú;ÝG|{,_ÈS,Êb[zâ`+"½ÚÞ4AÝ|¸#æs4»7¶¯y%1ÓGn.æÃ=Awò:C-O\x0008\x0018ÙÙ~U6k\x0002»s4¸ÇÑ¸zA\x0007\x0015[tUÃ¥Yd³Ø£Á=Æ[y¢Õ ¨N¾¬¶$Q_Ï1í;l¿gµAÒH\x0005ÈreÒ\x0017áÔA6vþ\x0011÷øÇdþ$ÊN\x00172Ylñ3kC|f;÷{Ü£,V£©:¦\x001alx¡¶quXï8µî¼£Þã\x001dI)´@\x0007<ÉÙ\x0005°Íª\x001eï\x0004uç\x001eõÿ£îý¶ë¸ûßWÙOÀ?ËWLk8"\x0019RÔün¼¶lÚÃ\x001cè¢3«¼FîÎí¹?o7É\x001cT£
\x001bØêÞl {tèX±8cç#4PU(T}k{ÔÀ\x0011¶\x0012Üê½!ý5aÜîQWîQ/qÖ`IWZm\x0016YÀ\x0008/öÉ\x0005]Yl½Äb+à"x\x0019ÃmV=°ÅÿõL®,¶^b±±Ë¶¶G¬}È0+\x000f\x00144SW\x0006[/1Ø*\x000fGAQít\l\x0017{RÓ \x0003»2ØzÁ6\x0007*«Y&\x0019(öêS\x0012=ØÍÖKl6(Ñ´µÍ\x0011-¶æ\x0003iÌd\x001fO;5T6\x001bØl-¸æVÅX=
ëa	ãW<P\x0019mXb´e\x001ef/§±\x0013gÆ¬\x0018®Be²aÉÆG@:kâ\x000e\x0001v4=\x001dÔÕ\x0006Üh0\x0012g2ú\x001cKaä\x0004\x0001¹âÆ®<
,ñ4Bó`LiEÅgÂ­Ý{¤ò4°ÄÓÄ\x0010î\x0006¸±\x0003MÃc\x001dkÜÚ+®våj`«Æ,%ºJ¢\x0016×zR®°\x0003ºr4°ÄÑ\x0008AuÒq­s\x0011ªçáxqg¯\x0018°Båh`£18Bì\x0011üÖá¹ÞÓL
ê´CÊ`\x0005\x0006\x001b»2Ù`kÜ+ÈìBÞ!rÅG\x0003SÙ>³Àö\x0019¯¹×CÆkIûÚåÀÏLw¾v`Wé\x001c³ \x00136\x0017KHp;l~\x000e3j´Í«\x0013»~Ã[`²Q\x000f\x001a,!oic;\x001e"0½\x001eve²Í\x0002\x001d\x001d`ö4XÙE«­h8{<ùkîíÊd%&;:sEØ*g¡Í9êÀ®¶Y`´¸hZl·¶ä:r\x0008fEóWÙl³ÄfËÅ¶ÕíÀ.¸\x001d\x0018L¼Ób\x000fâ2\x0003µà`\x0004Â¾ÆVq¶]\x0010g\x001b\x0019hp¨Æ	îIØÛà3ö¤\x0018R\x0007vålì\x0012gzÅÖ&\x001f	»½^4b+3b\x0011Ã9#5kÑDê¼Ö£ÝÔ\x0015±\x000b¬ÈP\x0001<¤\x0008\x0016#a§ó\x0008~Å÷G[\x0011»Ä`ñÎØ\x0014g[ÎfGêõ6¶«¬[`E \x0006×Tm(ÈçQ³_\x0007w Ù«ýáàÇ/·{\x0007ø×ÿ~ ü®®3\x0015él\x0017Õ\x0016\x0001\x0015éhR ÀÒ".ð\õ­\x0006Ê*Jz,Z:Üs»6÷ÝIÇÕ\x0001Î®\x0017Q)Y¯ztÓ\x000bÝår\x001dåòR!;L«W¬ÆÐ~Ùµ_¶ìFåÄ+ðÛõî\x0016\x001fõV]»zÕµ[²ê
øe\x0012_\x00154'º\x0015¿Ù\x0003ýp\x001d§ôS}J?-8¥-#i\x001e ÏÊJnZÃµ\x0001Üì\x000b÷pßûÜ~þ<Kx'pt\x0002i\x001dµ q7z\x0003yñ¯'çç\x0007øÏ|¦Oç\x00169q\ÒÎIrª¤}6-ùl#W¹{Ü ¦?é+û\x0002¦ªÙçòíj%M¡67\x001f0:·@\x001f8nK\x0010(ÒM­]Sñçl@]\x0001êV@O9® 	hIÁ\x0001òäÐ¼Ù|PñA+\x000b\x001c	Ç[*ÅïA\x0006ö¹Æ]\x0008X\x0010ÙzD°¿Ô\x0004ãmÎÓúIÃëgÄÒ\x0005t\x0015kå£,
ÞßH]C*ËÛÏ¸¥ç#Tt¡Îñ\x0015\x001e¯Å<5D\x001b>ÀVO¼¸Ï\x0005TÕ\x0001VÍ\x0007\x0018x\x001e²ÆÑ6Ü\x0011g\x0014\x0003º©dålÀê\x0000«æ\x0003l\x00025q\x0018°¤Ñ\x0017p2')/=¯ÚªyÿÅ°rÔÆBÞZÕ\x000fÝ[0n½>u]vñ¼}¸ø|{¿ùááé)Ò>ÿ}¿\x000b
S¹ÆWêYw9Â7\x0007B·\x0017g\x0017ç'g\x001f.®¯#úÍ_^&W%¹ZD\x001eÃ@=Ä"dÅK
üÀKy\x0007¹.Éõ"ò\x0018\r	^¿©	Ñ:îTí\x0002\x0012\x001c\x000bÇ\x0004¬q¢%76/ùt|Ü\x0001nJp³tS9-îrÏ.´Î»|UrW»?\x0012y(ÉÃ\x001f\ìÛD1ØÄÓ¿ý¶}zB\x0005©§ÍÛ¿n»½¿¿}z\x0011ÛJ\x0003l\x001c#Æ\x0003$4bÆFNß_\x001e__£Ôõæí/OÎÎN®_fV%³ZÀ,9
êR4"'F:G"ÆNd]"ë~d«³òøÌ8uI\x001e%FËA:¡d~æTIy}°$#ÅhV¦\x0013ÙÈ¦\x001bYiÉ9S'\x0004\x000fL±Ü¦\x001bÿù±©ÀÌ¶d¶¶\x0006Ý \x001d¦í,o
Çë<öÈÕÉìJf÷ÇXg_2û~æxî<É4ãL%O\x0015ÆÞ;C\x001cú!÷ aÎ+Ð2{$\x0014R$\x0017ú\x000b\x001b\x0006\x0003¼þuµ\x0013ì÷8PÅÚ\x0016vryfçûy5æÊ	Ê~/ë\x001cò2\x001cÍ#.ã:¯Ç\yAÙï\x0006¿%så\x0005e¿\x001büÌKý>EÌÌz\x0017ÏÒ b4ëÜÉ\gÙoqB']pã_ìS¼\x0000\x001eé0ªªÓ\x0007­*c§ú\x001dN\x000fó¬È©9;è\x001cçÏGµ.;ëè¹ßp|Kæê\x0010ªþCø-«C¨\x0016\x001cÂoÈ\\x001dBµà\x0010~;f]AýG8²¾§\x000cxÝQ¿åÜÃÂ+º\I¨.ôXÅz#µ6{:ñ\x00079z»y÷xûû\x000cV\x0002¹EãvÝ.;¢¼l¬<Ù¼»:ù8QºQ\x000fZAéAäZzÃ\x0003Ò¼ì\x000eÏhJFÓÎ(Q®é©\x00012c~hìQOèJB×LhP[\x0008ó@Dï¥È
-	ó\x0019CÉ\x0018Ú\x00199âç\Çï|~±,·M(ëóÒ~`\x000cN¡\x0003%sTÝ§\x0002ëtË\x0003CÒçBV\x0007F¶o\x0002Y\x0018Ù~d´øH3@\x0006C"÷Þ	nú\x000f»\x0014²:4²ãÔ|\x000bH_Aú\x000eããHU3^\x000eødkn\x001f:a2V'[¶\x001fmpa§\x001co¸LÝ\x001aµS_l"\x000bY\x0008em\x001a\x0016\x0012£i4^¤Ôÿ¤òöy¡s\x0019+\x0003¤Ú
\x00108I\x001f\x001b#"êâ³Àj!,wd
2ªuÔ¹0\x0005»Ã©±Sìk&\x001b@æCVFRµ\x001bITå&nÔ\x001f	©"4OY\x0019dY2BÅ\x0008\x001dNÛçð\x000cá¹ù1W0)\x0001ì\x0006ÈÊ«vC®­dYRçri-å,ñÏh+FÛ¾\x001eP/\x0016&·d½Ì FçgµAVv\µÛqã\x001c.á(7©±\x0014ê\x0004³\x0019ue"u»4Gé\x000c\x0013X©gÛy.]ÇÇÿåÇ¦ªãMG'×ñ¶ÝÜbc³n\x0002×g©ò¤øb´Ëm±EÁ°úÅfÐ´ª67\x0004{`¬ölùÕªê®UÑ\x0006I¡ÀóYcH\x0004y²¨_\x001c\ª²ð?\x001d¦mÏçêC\x000b|µu\x0001vG~ù}gIC×º¬0\x001bÿ\x001eµ²ÓÊ\x0017Ü\x0000ý_ßýaO"'
Î·_î\x001e>oïg
kÍ³¾öÎT\x0002\x000bÊÑ\x0002#\x001f8½8?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=?9|uz~öLÐ ãZ@«¶ÜòbyìzÉè>\x001bUÏ~ÇgÙ¤¥¹0Dæ)`Àã\x000bO~¿\¼_<<.¯XçVmn5[Q\x000b\x0019xbURÁ\x001fà;)ÕGë6¹Fq3¹Þ\x00174J'Y\x0001yYé`\x0004¹iiä(Õç\x001bï7°\x0017£âf÷w\x0004¹mÛÉäj*¥á	K@Î5²Üî4ÜµÉÝÄÝ\x0012°Û×ÑXØ¦Õr\x000f*«­ ÷mr?ñ}ççx\x000c<ÏæêtÛ\òÐ\x0006\x000fM¢¥éRíkÉ6ÉeY2h\x0004ylÇiä\x0010\x0019ñxÛ¦\x0015þS¼WdÏíS
Þ\x001e°)Z#fF7F\x0011ëåéé\x0008Ó.¾Ím.»\x0017è´\x001bT	C­iÕ
\x0017ÎIÙ¬ú\x00167ºìÜ¡rÚ%ª¤ä1¡ðOîP\x001bW\x001b}û¥s\x0013ÉiWM¢iÑaý9a¹ðYKC_\x0008ÛÕ×9¿@\x000bÀr\x0011ØQ\x0004úÇPì\x0010yÈsFQ««\x0000l,WýaQÊ4\x0002:j?ÿ\x0004>\x0012¬ûýÃòã­\x0002wVylVËbò\x001b\x0010\x0017ß\x0000r\x0019Ñý|\x000bÿô\x0017?à
Ò­hÇá!ô\x001aÌ4\x0016Ã¦\x0008ÆçR\x001ccª*ÍpÓ?^Ìþm6A\x0019ï½ãÙ»¢êûýòs¼ËD§\x0013\x001düy|õõ#\x001f6²A°ÒåèY{\x000b'\x000e]?Ü°Ñç&Zãuîü\x001b\x001d¬\Ö,UcuØLb3»ÃöõOÿðéÏÄ&\x0013\x001bî¾«§½7{³»ëÛÅr3!\x0010¸Ò4î;ìã\x0018\x0002\x0002¡\x0007îüeñÅãyÂ£Ãó½Go÷f¯_\x001dÏæeÎårñøÄµöèÚÃ!x·øñðpsµ¼\x001a\x0000(rtÊ¾ÆG¹\x0001Ð\x0005ÓÂ&\x0003÷<àlïÝìggØ\x0007P[üñ°|ÿ½{4\x0006	\x001cÁåèLà¢å3a\x0002	D\x0001Ããð¼eq¿ßüqe\x0017\x000f\x0014YüÎÂÞÿOÝ»,Ç$iº¯Ý¬b÷p\x0005H&S@
\x0012®Þ\x0004É 	&\x0008¸d¹íÙýyçè79O2ª¦ª\x001e\x001e\x0008\x000f\x000f7\x000bï\x0019©èìdvÕWævÑë¯Ox¤ì®ÝV&áê²Û¼*ãtp·EGïpÓðn; \x0011²tml!2\x0011çÃÐo\x0005Ó¶X\x001eÑGWô)qÏ\x00126§>íLÛ\x0016j!óìÈ\x0001\x000bÿ<,v\x0007®ØõÝÅííòë\x0012\õ£Å×oxÑ½º¾ÿ1\x0001\x0016£ ÆÍfá\x00166¡Ð:MÉ\x001eÀ´´§o¿~}üâ\x0018\x001cõ£Ã\x0017¯ðÚ{uzþï[7Þ;àî¹\x0001\x0005AKM%°¶<ë\x001dN\x0007v¶[\x0002æz\x000f\x0000\x000eå¡Þ\x0000®t}H×\x0000\x0019©ú'â5ó\x0008-rL4è\x0013 íàAYc\x001c¬ê\x0001ú> ¯\x0007DGC«h<Ä
`4²ioÂÐ'\x000cõ°\x001bÕjcjùÎÔ\x0015\x001bsð\x0014U\x0000Æ>`¬\x0006ÄúKzéàIóX\x001d]\x0000y>\x0010\x0000pÿ>©OêP³:9,!Î¬dÂ 7QÞòÒU\x0010æ>a®'TjXcQ{³¼
¹ú\x0016ÖÐ\x0001{\x0010²gÆèU/¢¡ì\x0013ÅºEôI3¢\x00196h*\x0010õ\x001a¢®ßÉÐP[@LÅ_/FÉ\x001dîâà\x001d^hÖ\x0010M\x0003bÂL\x001f­¢ÇYÙ(gÅ¨=Ï^{Vtý»iàÒ>ÇÙâ\x0018B¨¬ÜÑì¸vgëúK[9Kº¼±èö%²,l\x0018÷¼²õÚ­ëïlÎçÒW\x001d`¢\x0014\x0011~æA¯i\x0017¡ÿçgûó½×3©\x000fÿ\Â\x001e<[^ß|ZbUÓí\x0005XÝ\x0000§Y\x0014Ê#â×\x000b,t\x0002´à3&~JPÅ¸l(ùæ£õT³­Ñlð\x0005íÅs,VêþâðíñËóãgÇ§gÏÑ¹{ýüìðÍã÷×_¿Þ_-ån`¢\x0018\x0015þ«3¥LÞ	<ËàÌcQ!rZòN3¢y3\x001b'>Qø¯zÎØ{7¨÷U\x0014nSQ¼Dã4+'¼-ø¯zNÐü¢õLtÁ49\x0008fD½©Ù01ÿªÇ\x0004\x001a\x0012\x000c*ËYBÛÀ	Ot·v>NÌÁ=.?õ :²^¯ñÎ²6º`	T+T6
\x0014Ý·òS\x000f
\x0007Þð§ai\x0005ÔêÀ \x001aGkÌ\x0006ærù©\x0006Ô\x0002C $,\x0006Ü8	v6NÔú*?
 q`aJÇûS0çjbMiù©§\x000cº»¢¢i`\x001e¥¬<\x0019çs\x001a¬x/?õ àÇ&\x0002
àÇfºèµ\x0007I£9\x001f(¾\x001aå§\x001eÔ\x0004yV8j­Z\x001aÑ\x0004 \x0001ág\x0003µørÚ§\x0013A#íÑ`5¥|
¨x\x001c	7\x001f(*\x0017jÐ\x0010d
¥	¨<IWòòÆë<ãÓiÑ¡(?õ\x000e¾<aHC\x0001ºòq9õß\x001d;\x001eÛ&	lM´è»\x0003'aê(©f|9->Ãå§\x0001Ór£\x0012,'ka §>ÎúÙÑ+-?õ àþ$ùîr¾\x001e\x0015\x000e\x00044Íº¢Ø_[~êAáÞôüá\x001dë¶\x0002h´Ý§\x0013í:ÛdÜy°éi\x0008°ÁM\x0010#qÕ\x0019/&ãFËO=hL\\x001dWN\x0012½ò!;¿:Ks\x001eyTã.?õ ¡¨²\x0014P/7(\x000eà7É`çùl \x000eå\x0019ÊO=(Y@\x0013ÝM!ko3ÍhÜáØ¸Çå§\x0013Ìz\x000f\x0001\x0019
g\x0004}é\x00044Ï¹ äv¶ø^'qB,3-
hÔü*¡*Å \x001eA\x000e½öø\x0017å:\Ð\x0013Ý¯Ù8qÄmù©æD¡:1ïÀ.±\x000cÚÙ¡\x0006\x0013£3â6Ý¢®È
;fPÛ}ù9oÑ"ç\~VÔñ¬çæeä;J¶Ïè)9¬§)?õ8ÅF0¹\x000e\x00100yò6r9×\x0013eùi\x0000Õh-\x0015Ð\x0014I\x0004\x001fAå®·3ÞLX©ôØ7YËÎî ¡Kï
fLràÑaÓ g\x001fï¼ï¬lå\x001cE®ÿÄI@jFÇ\x0013»\x0006\x001fjP\x001c\x0016a#hTp3Ñã	\x000e|x?ëb»ü4úÄ+ê\x001eRÎº\x0011Ïdù©¦4°)©\x001eßD@,>\x0006þì\x00163\x001d¥\x000cçüõÑÉ!ðìÍ\x0001Ø\x0014Å18V4fÖhDØÈµ\x0018\x0014\x0015\x0016ËAËO\x0003,g=\x001cüy¤ee\x001d\x001byeø¬°	+úÊO=,V\x0014\x0011«ÓÔ|¬üÚz½³¢b\x0005YùiX×Ä³"L6\x0004Ý=F y]]± çÍx\x0004ÊOÓ&àp\x001eJFæ$Y3
`ÍÊê\x0014°ºÁâ­Ä¬auºL\x0012Ø¹×\x0015§[\x0006Ö\x0012Ä\x0005V\x000bÔz\x001bÖ\x000183°~øðwº\páÊãÕ\x000eø}¹¸:øÇ(ÂÕã)FË2\x0006m«à8Å(\x0006ªrqÌ úýøðåÁ?Þ¢f\x001eUï\x0006ÅðvM¤Z³,«ÁjHÃIÆ`ÚüÕ¤¶ HíjMa'w\x0012-W{\x0001©WcÖ_5é\x0004^
i°bþÛ 1¸f´\x0008>ÍGÙÔ¶¦°9%\x0015\x001e¬ÄuÁË\£õc.t-éFjl:jP¦TÜ\x0008*(0ÏMG:\x00162­&õvò¶ÔyI7ºøþÞêîð«9ÁbòSZ*\x0002BXÉ<\x0005-\x000eªÂ{`FT\x000cB\x001b×²U\x0003ü½G\x0015W¤D\x0002¤FÌ@\x0015g=S\x0016íjÛ3®kHÁLnönÆHÞq<\x0018=\x0011uùn?^ Y&eùYÐüäT\x000c·\x001eýl°É\x0012)a³\x001a\x001d+\x0016ë\x0018Qâ\x001a\x000bÉ¢2aG¹6þl\x0007`ÿâËO\x001d N\x001f »IuA	¸¨d\x0011Çâñ\x0005\x0010]½òS\x0007høz\x0008è(Éh\x0013©n\x0016@=\x000b ÆÎ Çô[Epà\x0014\x0001æ2\x0005½\x0000\x001avïcñL÷\x0001ü\x0012Ý§Å\x0007\x000céà¿Qùéøn\x000f\x001677ËÛí|\x0011§ËSìÞãL2;Òg2µ·)\x0014Ö îèðììðäõ\x0000ãêÏv2b|ÌúZF\x000c\x000bc n0`är\x001cdD#a?Æï^½7`ä\x0001Óågõn\x0016W·÷#\x0019'EÑÔ\x0008í])]DÃØE\x001bª#|}ü2g/_\x001f\x001e
}fù£]tøÄ\x001a:c
\x0006lÎrÑ\x0000üm\x0015\x000eßfºìü\x001fËï¥{\x000e]*>8#¥#m;^2QbÉ\x000eKõñ	JÞêì½¥K¦ë1{{øälÛY)ÿÐ\x0016ÎOÿ2ö\x001aM\x000b\x000cú\x001fáÄ6¿Ûo\x0017WÛ[\x0012UØÂ¥ÆÅýÁ	Dô½wbV\x0004iã×¯¿<|ý\x001a\x00126 \x000fúº\x000b\x0013k¢ÊO\x000b&« 4+É\x0014Rv*qß¤ehù©'GÐ±KÙù\x0014Þ'ÇºO8·d_Ò?®Æ~(ö\x000fÞ¸µ-úëâòÓ=¶]B\x0018GP%þéQ\x001c¡`Â\x0003Îc¾C
¾Ç¿\x001e<;§É/\x0003Û³÷§ÃW_>«ËâMb¥]êC,þ\Þ\}\x001eyk+Ã(}ùæ)Âÿ£\éÑ\x0003\x001bçìåo[Î\x000fÿÙ\x000e<\x0015ìå§Ï&Í9\x000eç#½\x0007ï7%\x0006Ì\x000eÝGøå·Ãó7ûP:\x000cF*J\x001c\x0010E
ß.¨LR`h8jÆ\x0001J¬hÒcewù©£T#1Î\x001bÓQòùÎ)eÖü­?]]^Y®U§
ßýHWbAúÈÑÆVhº×5xÞ*òpdØøQ\x0019ë\x0002D\x0012ëÎ7AÏ\x000fÖþ|\x0018öÏwKX1
hâ
;÷ÅâîórÔNsT\x00173ö*Ò-0#KeYÑ\x0008óÛñvC­ûã]h¦5[m*&æØ4\x0016ÇË\x0014Òl-Z:B³ú\x0012iXPl&¢\x0000\x000c:ãE¾ÚÛ(\x0006Q\x0017\x0013ËËO5¦É¬úhT\x0018+¶ó BãÓ§o_?ë\x001f¥z\x00053Ù*<$]Þ|Z¼\x001b{|Ìc\x001aZÃi²ä-\x001añiC*¾òã³gO_ÿòäpð
BTþGv¢âÓòS
($Ýõç\x0012(0ä\x001c5¼¥ø\x0010ÍHZR:~Ãÿ@µg;IÃ^\x0017T\x001b©\x000cPqÀ
uûe¿õzñáóÇ÷%µ9ÃÍ­z}yq5¾YSÉeÍ
6q¦|\x0011XrÑ³³\x0016pÛbë2ª0\x0010Ù«Ãóm\x000f\x0000ÿc#ÛV¨M©ú§ß\x0006l-S]È\x001cÁá£TqG\x0013U\x001e¯ãìÍÕ7ôÛÀëØQàýÒ(=Î#\x0000\x0015Í.\x0017Ø`3\x0016ý¶ì\x000bÏb.ø¢
P\x0011`\x001dýLÀñê{°¥?-)Ìz>À}Zö7KÒ\x0000Üê®º¿¼ò4W\x0007å.¨\x0002Eç¿|óËá\x000bð<·À\x0016\x0011û3Ô°ß\x0005«ÑcÖþ¡c:\x0016üy\x000eYâ<[©\x0014VT÷0\x001f¬¡³öð¨MõÇn\x001a,m]u4èTÇìs©+8xsöß\x000c°h_\x001bÓ¶²QqÐÄÀÅEzs\x001eK³ÀúVÝÜß_õ;×V°¤ón4õöÅo±8´ÅQ­¸ñì\x0011¤i¥Ç$ódðdu¶Ï¡\mù©\x0002Ì6p\x001b\x00188e\x0011UÙ8\x000cÊ!\x0014,gß\x000bðú»ÿø©¼^X}Y~Ö\x0001Ë?\x0017\x001fF\x0018CÆÙ<ÅÆ\x0002k.ÁLÁp+P,©CÄ8>9~{øôø×çO·ò?²\x0013\x00163çå§\x001a\x0016\x0016ªs°°	ßÜ\x0002#5
,';7mB£0­[Si£÷v(D´Zh=¾3Ó¢]T~ªiá\x0008Q\x0016\x0011>ºÃe.´ØñK´8³zöåéY#îÇ\x001b³üäú	Ú\x0015íÙòÏëË±¨¤O¢\x001a­£&Ð L"\x000fÆ\x0014Å³ã·§'Chô\x0007; \x001c¦áÊÏt*\x0013ÒÊ1r6;
AÒ\x000eQNzÄÂÖ}±ðÖ-?\x0015XVs\x0014ÏY\x001c{ê	+r¦(ÇRÌÕÄõ÷ç?¯<réTbkïâÙõQû\x001e¼:©ø·Z\x001a¸Côlj\x001dÅPg§O#vô\x0007Ã\·êÃ2ÒLcÙOùYq\x0001ÅûÑp"Ö{QÕ÷6°U\x0001v\x001c\x0015(\x0018\x0014ã BÅ£a2þ-h÷ïßtyÑ0©\x001f¼\x000112ìÓáÁB°ÁÜ£LÛ^e~KlDãì¤\x0010\x000c¡ó\x001fì"#1§\GVæ`\x00152©C\x00044Í¡âìLíhw·]3¥ì\x0004kÂ\x001aÙòflá 4Z1â8´Çb\x0017ÁöVRhçC6\x000c`\x001díÒ%ÿØO?î¦ÊìÅX
Vvö\\x0001Í÷,¦\x0000ÌÞX«©XÞX1¦JR
¦
W\x0011¤ä4}DøO¯Êä?T1 ó·v¯¾½¸¾\x001c7GCÔ\x0001ÛTñ\x000eS8\x0013±%\x001b\x0014ÇTw´ó\x001e¿=þá ÅÛç§'#h\x000f\x0011Ý=mj\x0011ã^UÁ~M/=üoXb`\x001dD=àýO£n©×Fág7«\x000f\x00074¶¶d¼\x0017·w\x0017c/|ÍÊ¦^PxN)La(`[£É\x001d}røúÍó§=Îgg/\x001eÐ´ÚÞ?°\x00036¡Å\~êaM\x000ex6
¬Ïè ,Öµ\x0010¬IEpn>Ø\x0006iù©uZ\x000e&ÀÂ.¶SÐQË¼\x000bcó¬+«t
ý6ÐÙD\x001d¡\x0001·¡8Jt,´¬\x000b3Óbª~\x001bhi\x000c
 FòN\x0002F©YmÞÌ\x000cê
¨k\x0003õ3ø.w ÊÀpã¥¦d.ÚX6AlÛ\x0004I\x0006\x0013úAO+º!'&`Õì´\x001aeÅè·Ö\x001bÝmY|Ê)¼\x000c4¥ÛcFZ£K)\x0002þÖÓÂ\x0013NÅE¡S½\x000f:ì»{=ONÏ_ÿÛùñ½i\x001d	ào=-ÆRiÏÖ<*½9\x0001
K¾iÑ\x001dcm/¿\Þ\x0007Í\x0012ZE8Kflqòly5^Q\x0006o\x00007]£Ü+¥\x0002#x\x000f\x0012tÃ­·2R\x0013,gÇ/·OWlè§¹XÇÆÁ2\x00172'ªÀÆÎ&å¥T&½¿°Ë¥ô (T\x000f[\x0003{±¸¹¹\x0006¶\x0011»\x000eö\x001càÈsfÒe\x001ag\x000c~â¯ûììù¯¿bù¸_ÄÓÃ|qxvv
¤Ûì¼\x001eªÅ4j=*ÜðI\x0003Òx¼\x0011R\x000eïïMú\x0019¾Ô·2=\x0007kÞlo\x0014ðë»Ã¯«1×\x0015'·\x0007®a\x0005Oß¡l´0jGÚN\x0003ÑQA|ýæþdK0GýüjJX\x0014'èÞ\x0008Ý·Ë»í;1¢ª+÷}c¸ª\x0006a'Â]NG9R\x000có\x000c\x0005û\x0015e\x0002ööøìÍÖ\x0010SGULPUCeÅó\x001b)Jw\x0013µQ\x001bgoª\x0007\x0007w'²x\x0014ª¬IÀ\x0003G;G\x0019Ô\x001bK¨¿êÝßßomÑ:Ã\x0000o	ò\x0002Óâ\ÊÏî/pÖäÝ\x0008 8NqvÃQê\x0008Ü±å¾ÓÃ2=ÈvøL.ägçÏqÆä	 ¢Å×\x0004ê\x001e­\x00121\x0014å\x0006o£«×v°¨»\x0019\x0015Í(üW\x000bª÷ò\x0004V\x001c\x000fHJ\x0013Iú\x000f´\x0019Õ¡¾L#jf\x001cP½MdläfÖ8Ø2[Éúãâ{øþ©ì\x0000ÔÙ·=Öû³ë±òÕ\x0010­ôH{ã¹C\x000e\x000eè\x000c?|\x001dßùÁÙé¶ÒÕ\x0015ÜÐÓ©B$ýu \x0002G*§£ÂyL\x0015\x0007{L&q]ªO_È\x000e¯¦Æ<YÞ,¯J­"]}¸¾¹\x0019û¸\x0001ç°òÇÅ"`:Þ9ÉÊ©á\x001dDñ\x0004Þ½¥b>òË§§gg[-¸4Ã¸vdS\EÚ\x0005\x001b¢ê$øhVÌÌÌ%\x0012¯ÛQô*vQ²Cu·Îv°k/dikEÆ\x0013é\x000c\x0018.È®KÂ»Á¶£½%	Ó\x001c´v»T\x0014:éÄ,ÂæÎÙ1´\x0014Û£\x0011=IKø\x0008r¹úáÞÎ½ÑCÉ{ì°
1°8/%?Áy½\x001cÔì;C£Yùieµ~Ï\x001c:\x0011¿ÔyGÁ\x000e?\x0012û@c	}ùiÆ¦\x0011QÃÕÒ¤ªºí\x001cæ¿ètquhf\x0006¼Î°V^=­lh7ÿ\x0019Ô%\x0008iT;´ö¢¡w\x001d\x0015KãL¬®ÁzþF\x000b§ü4/´[I%spÇãH)1!ã°\x0006ñ~Ð\x0018ÜãíÚø#^\x001d^vë*»%ë\x001a ?qþò¶ßy/C»°6ýþGH;æ_ûÐJepµ¹ú\x0008½Ö]0øº\ÏñCÒ§EÁàüßËøÙmîõ\x0010£ÇÆ7\x0010Êtkiz\x0013Yæ-£\x0019f"\x0014W»0¹n
M),^N+bX³\x0010Æ·XOè£ìH,êIâuR >ÏFP²¨á+wSv
1øÊb;bØ`/Âåâûýû¯ÿ\Éõ¯\x0000Áù¾¾ÇÍ£ç^KE²Z¤4tàÐ^òE b;á38Ö§ç8 y'¢ÆJÂòS
¤åßâ0u)W²\x0015}	³Ì\x0003Ù)\x0013ÔCªG:óJzñmt\x0016IOÕÛ\x000fòëÏüçÇ¯=å\x0014BüíâÛ·ëËw%2ð\x0004;nïÇ
-¬TÅ\x0007éK 
s\x0015\x001cH\x0003\x001f\x0007\x0003igGÇ/û!+\x0002ýíù«W§'ÿxSB\x0003O°ëö|'l)#ð´:±2Y0X\@°DI\x0000Ö ï°RùÜ\x0002Óa¨ö\x0019üÜ3VyÇÉ;ç0\x000e;+-\x0006\x0010R#mÌ\x001c¥
¤N´ZhméµVH´Î;AE\x001b\x000cüefÜ$QWÔ3çÄÅ*¹òÓ´º`ÐÍ\x001f4Fy/ØÈ	1§Ô¼;WDnlÞºÆC\x0011®aÜÐmpoWïî~\x0016»	kË×Þß÷#ä¨GÆ½&û¢LA
±?]Ä6üí÷ëïðî¤òE²ÊZÖÈAÓbiB'¨\x0005¯ûB¡°£©2Qäº±}D¢l^¬\x0011ê&(«\}¹ê+M\x0011Ôï÷·w\x0017WàF¼»\x0018Ñn¡ÑóÔ%±ÉµØC)\x0019z#±íÚ\x000e_>\x0004ûýüõç/Ásxò|fËíåmºýä0Á½ÀIGðz\x001f\ß¿ãÑ [3:Þ<¢ñ\x001b!`"óL§\x0013cè×\x000fet\x0008ò\x0005\x001e\x0010xÁ\x000fNNÏÔâ0iº~>Qò°H÷§\x0012/\x000e^\x0001ã
\x001cÚËÅÕû±Fá\x0012dp,/¥Á\x0011\x0016
\x000eÔ\x0019ÚúKs\x0005 Á\x0005wìhk·p\x0015UÄS#k\x0004G
Ù-6&×9f¿M&]~úë[ü²"Òûò\x0017ã\x0013\x0018øcXò©8^cdì
<\x0007µ\x0001\x000cy~Pþb«PGö`
'%®\x000b3Ø¾®yees-8\x000b\x0019ö\x0011\x0004]E]¼f*sY\x0000|g\x0016:\x00006\x0012\x0000Nvs\x000eUdà\x000eòÁÀ5c°2D×,\x000f
ÚV%T6ª#Ý\x0019Î\x0018#î¾æl\x001dÆ
Y­ë>§[%:à°*Ç\x001bMZM26ñ5£]ùà,Íjÿ¹ÿ½º¾»c¬:\yÏ­ñ`\x0018*ë\x0008X\x0002ÏÅPÙØ~ø¤½:={ck±DÇU»ÚÔÃQ¨7ýÅõ\x0008'¥ZI\x0018Ò5tëÙ·taµtA\x0004xuìAÙgÃÂ1W»t(\x0018yé,OAñ¬+\97buî\x000b\x001fÍ«ôOüùxu\x001aÞ.?-ï\x0016£ý.%tÈÚÌ\x001cKË[©°wq{léíñ³ã7[ë°WT]\x0011ÂTª2zÛ³¹é1ÜP¨Vâ·ðÿ÷¦Â\x000bj¨ç¢U075v+RÙ\x0014ss«	<iÝ\x0004Ä¤pü\x000b1E*M-­\x0008bo\x000fÆL\x0001U·«>åzY°×4G\x0003K\x00123Hm
\x0007î ÊöË/ïúùÙõý]¹ø\ßß~¿\x001f»ú\x000b3\x0016\x0010xbX\x0000óÊ¢êÐW`;;=Snþ®\x0008uK\x001cõÎº?\x0014ö,á\x000fÓ-\x000f\x0000dùeq5Z\x000b\x0002Ú¡\x0002\x0015·!b²p¨"¤-Å°x|p\x0004çø÷ÃÛ\x0016ð¿®>g]\x001ci\x000cSà\x000f1\x001e-¾]^c©Í_ã1òãY«0s$:;3\x0016C©\x0017yuvøæõ/Oy²&"EG¯NN±Ìf[=Sw\x0019«YlùÀ½/àà\ÉÄE0_\x001fÅÐufKÊ2E4»i\x0017ÿq<ðïà-»ïËòëÏ»¢°GøCp=0j\x001d¿ü\x000c9ªÚ\x0002/\x0012#w\x0016\x0003MÜ¼¨Q¹E4p{D\x001dä'¿Á_n­íØKà³ü4³\x001bxÄHÔ¢ü;É=ûÕ¬Ö\x0018¶J³íÇñå-?­ì6íBÃ?`sEÎ¹lÙfN1Ûÿu×¡Ô7ßfxf5Õýêàøat`\x0018²	n=Õö¿:|.Xsác¼~ÛñUþ&ât8­$óÇö¿
\x001f'Ðo3¾\x0012\x0005û(óåâTpl\x0004T\x0015ÿâ»¹ý£ÈR¢CÝQn\x000fN\x0016ïGÎ\x000c;Ãè´¡\x000e\x0014\x000cfäáúzr\x000eoÝ?Î°èqà>DÆ£mVç
=ò3
§ÙRTà&0b\x0003Ka.6ôÊÏt6¥8¤\x001dK¯æëÖ
ìf`£¢Oú\x0008\x0017QsÁËXÐDH6°*ÙfÜ®\x000cÌéw:7Ò×ÕWÔ)gR¶\x0012Q,%û"*I¿Ápê9ÕU'Æmê\x0001e¿5ù0\x0007Y(d¡Ì[åÁÖ"z\x0002Ü;µÊp·ýÉJº5Û\x000cÇ!ZÞfp\x0006\x0012­\x0019ê¸ò.c)à½À´-
ÄvúÅ\x0008k·P±\x0001¥\x0019KÜZK_nò.ÌA\x000bYÍa?IvÝ6L&1ÌÞÏð15>ô[Af%éeèÁ9ÇaF~§sYÍ\x0000\x0006"(¬\x000f`Î
I\x001d8d©¥*2pÄ<¹ôHq¿VÚT´µ÷\x0004+ô;\x001d,zEkêZ\x0001,ËîÇ\x001aÆýÁ¾pù\x000cQâÝo35¶\x0000¡Ó\x0002ægX1æ=¦ßé`9aTZÜ#ârÞHWiØl\x0004û¸üË|]\x0016ë\x000c- ezÑ\x0008Ô}9v¨&EÁ\x0008RÂT\x001d	gIøª:_Q<öåáù@8BþdÎ|^:Ô7ÓEÿ~WxE¯h\\x001f^}\x001a«ø
d)2á(5Z\x001ePoX7\x001aÓàS³^ãÿ8|ùìdÀ(:ï\x0014\x001d\x000fø\x0018ÆþòùânJÕ\x0007ü»â¿VßúÕ=@\x0005ZM\x001c£\x0006ü#jCÅ/B5\x0016úWçUôxè\x001fC\x001f½ü#;	³ÂYJÕ ý­\x001eiÃ¦o¢\x0019Ó\x0018²æ\x001d	ö¥`_\x0002Þ~¾¾S_úZq]\x0008\x0005X\x0016ïo®ïG4\x000eÝ{aÁvâh5<þ|/{EºÌÏ_öº\x0018
üÃ#øß¶)\x001dwt:\x00148ÖâyÏ¢0pMg*9\x0007<çÙj
FìÍ·\x00121¬ã\x0003/Ñ2\x001fv{\x0010^4IðX?,{ð`3ê_
ªN\x000cýVº,ó0£K;ÒiÁL,\x0016\x0017(\x0013Æ\x0018û Æ¢\x0011\x0010C%¢w¦CL<Z\x0008>°á¼±i6D\x0007~ë\x0010³ã¨m´¶\x0018ô\x00051¥ÌÎl&±\x000fâ_/Õ\x0015úe®ôß\x000eñíâÝX={Ì.â\x0014
«R½fÎóêYãC\x001aJ¿\x001d¾x\x0005/\x000e\x0005GifÅ.ÄXJÙ£«ATQ,.&U\x0017¡Ö?+ÂÁ÷}ó`dF\x001dVÀK¿\x0015XI*]=:·D\x0005;©°hb_ª2\x001d£o\x0002î¤JYqÆ\x000e¨¤N"'k:,|è[°þøú\x0007x%Û\x000c7\x0019Kcpðôæz¬ðÉÃE'E\x001c	ÇÜP\x001dx>\Ã@©b]pðôìtkéS\x000fK\x001a\x0010\x0013Öý\x0011b§äl\x001e*ÒibÄ^nÛ´:Ha[I&*çl¤kBáùQ¤\x0000ê\x0019­\x0012\x0005äèÃâ;é(ºÕ³\x0010vf`5¡24\x0005¶6URÚÜ}éÜv\x0013c.`\x0013£é¦ç²Ì\x0018Ö¢D90ELu\x001eD,GÉ-¡k?I.¾¼òSÌ6\x000eå[\x0018W
gõ`Us%\x0014J\x001dKQO\x0019ä¶d¤öüëfùýú<ñæQ\x000f®û1qã]P\x001cµÒ\x0018O \x0015±¬
¬6$~ß<¼³"<ßªlüùîò§+ß\x0018\x0003¶%h»4ÂÐ1åuÔ \x0008S\x0002'Äq	7z\x0012ÉÃâ\x001e=-#¬\x0005Ý®·Þñ9Ô~,?U\x0011®\x0017jókÚI­ª³¬>ú[,h%\x001cõß~Üþñ1\x0014%Ôb¿<XÄÛÛÑzÚà-FÊm¨R7$\x000f§8RF4\x0004ÃCM\x001c¿~½.ÆÓgä?ÛÁhT©ûT&{6TÁa×¢Ê»ÌXzÏçbìÔ!ë\x0018£DQ\x0015è2¢Û0¢ã\x0004á\x001e?Õ§o\x0013ãÊO\x000f\x0011g!2ßï£\x0010à»óÛ¢Á~DF\x0018¬¥\x000c2¡à
Ï=,õ¼ÿv>\x000c»ö\x000fl©øûc\x000e·¨\x000bWZËÊ/#?\x0019ø\x00154\x0013À164î6{\x0011´°%0Ï6tã<Ù>âkJ§KÊqp¨J¹\x0007ÁN2©Ñkn\x0017`[§=x¯N¿\x0013yáp.Úî4\x0011ÍñÐ	àñh!´ó`2~§ñø,º!èô°r[vûya}öâ±¥Í¸üNä§z§°\x001e\x0005K>Ç&Y\x001e|SiÊ OúFã\x0001`rPÅc³³¨®;³Ïê¸ôtaòê8l$õÌ\x0013Yw*Ãcä:ÓõõÝßþ(ñOüÖø/¦9\x0002ÇpÇ?ü4\x0018{/ÁE¨9¹J\x001c\ÄÆëmÁÅs.zr66àoÅ÷ÀÚÂçá
sâ-ë~\x001a8ù2øl&>é\x001a¬á³\x001cÍlèb½.	À?°(y/¸Û¯ð@\x0016­&	Å\x001eÛMa¿øs´»ÄP­.ÜKÒ»¡ô;©¤\x00065 :¶³Â\x0006ñvÛK³â\x0013]ÂZ@ÛÙáÝöÌh(þéáQðMRZ½N\x0004õQ@;ì´òT
SÎÄ(Ú;µZrãc×Ù¡µè&h;¬mÔÄ('Õë\x00188KjPDÁð:Z¶yÓ\x0016¸6Äuïuú2¦GF\x0010ø×Ò\x0005~Pê¥Q-\x0017?J:\x0003ßîB¼?8ºx·ø°\x0018\x00199\x0006#×Q)"7\x000eÎoäë:ìºqÎ\x000f?9|z¸mðD\x000fÎê½\x001a8oX½%â\x0010QËÕÈ;è\x0001n¤\x0010j
¿¿ø\x0012å²ÁYk®ÂÑõ¨à5V¦\x0007p\x0013(&\x0001N4\x0008è2ßgPXtez\x001fnUú»ñù~ùµßheJ5º\x0007(9BçµÌ2*Z=*¢êtÉ\x0006;Ù¬L©F\x0000u3wÂI/J\x001d4(\x001aÌÿHoEèt\x001dÃ°\x0016áTº?onÜüì7£ôé~[Ü+9ÃWÊy,h\x0013:i¦-Ây}8\x001cp¸\x001bnè»îCU1î\x001cóÎu²bf°\x000f°\x001eN¤0«àBêTÚ¦\x0015Ô\x0002òò]íp[[=\x001d¾<.TÒyü\x0004Ç!\x001c\x0014éNu3-]ÿ*\x000cR¬ÜF\x00192\x0007Cfù
¤Ûy"&ÂñT*8kyZÁØiòJäPí¼M&Ñ­t+êðB§Kf\x0014>\x0018ç½4zn·\x0002¦àù¯Ûïa@	
ÇòÓ{%n®/~\x001c\x0014\x0019÷±Ù\x0016sø\x0015nJÖ9©æ²ÖçñüêÉ8;}þï!Ý	lñ¿xù©\x0007Ö8ú¼ð¢\x0011MIo´a$\\x001c\x0007û@\x001b9qGÚ\x0010Z8UÑ ~UÍµ,Ê\x001aQ\x0011°ÙüW¬¬+I«~Öj2±ÁÉèD£½#OD³Ö¼J\x001aÔ®©\x0002ýøóûWsÓ×	&ÎÛã÷×ãó¡\x0014êXp­³ô:\x0007\x001aªH+=[ù^\x001f\x001c\x001fn/­êqõ^¿i\è(1ââVÚ:Uf­í%í\x0015ËeùE\x001dÈMÂåêÚ~­\x001d9)¹ú÷öäåâs\x001c\¥­ÈâpÙ!Ø¯z.M£,ª\x0016\x000cîh.R.ñäÂc7}\x0007îI\x001eg_$±Oo&Ìvð½ÿóýg»|h\x0001\x001e_Âkòêzt^³R«Òïf]5Øú-Æã\x0013xE^n\x0012°"B
ä§\x0013a+«f"°\x0012bzÐÊêÝRÑ0i¥Á:\x0019Ê\x0004Ilgã98\x0000þE¦ßÁ®ß*¨õôÍ$(h»4q¤o\x0007LRÙ¥\x001cÇöþv|vú²ËbÖËJêk
W\x0008Ú+\x001cËN½XRJ	\x0017q\x0006.ÌjZ[Ã£ØuX£¬+;áBåý¹p\x000cJùÊ\x0015ÌÅ01e\x0011!\EulíËå°.ÆÙM\x001fCâªT\x0013Áæ4Ì\x0005¶\x0012q-U;Ó0\x0007_~&#sÏÒ¡à>Ê´æ'ì\x0012Ðò+S°\x0016w\x000bóé¡_îøÛ;T±\x001dÝ[`å°?\x0003·çÆ®ËRá!\x0013Ýåþú
êÖî&Ã\x001cg
d\x001a»J@ÎF\x001a h\x0012Ö,³\x0002f@Ãþ¤\¹h:dÇæT\x0016ÍAÂE:h¶2\x0015µüÔÀaÕ\x001a³\x0005>!')eÒ¥Jj\x0006¶\x0007)ñIl\x001eN\x001cóR \x00047\x00168\x001b¶\x001e	pêÝ\x001f÷\x0011\x0007u\x0016Û¤ü°ÙÿëâæfùóæzbiNAT\x000bPN\x0003ö2Èk	/ø¯ggÇÿ8;=\x0019Hêt¶Ýäé\x0018-(å§1 (­HÙeG²(Z«\'r¦g¤ÄÝb{Eu)E×Î*ERè®Ý\\x000eïòSIé\x001d>óÒÆRÎ/º
³A¢!_~j!
¡Zü!½HFÞù(q)mýR(nQ`Ëê¼yEpÞÝ|\x001e#Yå§\x0012n\x001d^Kðød\x0008\x0001_¬@\x0012Ó¢>Ô\x001f¬¹`Öê¬Dà\x000e§ó2eVû\x001fÏùýu¾~\x0018¥ýpðëõÅÍâb$ßã³ÙEøÞ\x00103"%¤Âö\x0000òÓó_O\x001d>ßëé¸ðF{\~¦i-É\x001e¸`Øg\x0005\x001bP¦éè¸{\x0005§\x000e
°\x0004§ÃqvÑ'Êa\x0006\R)ð·=Ù=\x001d,Év¹\x0006\x000c®=rÅ<x\x0019$T\x0005v}geùañ½:.5°FÕl1på%ÆFn¶þLÒ\x0002\x0016fX/j_í¢ÓÖËpõ¦	N*¢	V*\x0002ra\x0019|pM÷êN]°ÙÃ0²õaÁx\x0018f»Mº\x000bìúýÍÇ\x001fîA1Ê³R%s#\x0001¯FEíÀÑqHô`zNÿë R¢q{NçY©9ÁÁ/GD÷:À~'E\x0005¡ÓÝx3HDè»¬Ó||pl®ç+ÃãÏ>\x0012¼Ü-`Þì¬\x0005ì;u2¿SY,ÿp¾%\x00149¾JBïeh\x0012ê|pt§èü0¡Þ\x001d«&fÚJÂU6]%O\x0010­¬"Ì1\x000f \x0006|ý)	¼~ðÌF.Ýp¯8#\x001ej¦z<Û\x001db¥EüY#\x0017%ik%T-!v§ú0v2Q¸ÇÐi\x0014kå5\x000c[
§ZÂ~üº\x0010ì95z\x0012¡ÑÝG¶³\x001d\x0012´´³«\x0005LJ=ò2ûÌ²\x000ci4\\x0017ZlÏ¹>òj<K%¢u0ulB÷ÚíÑ¡ZB[Ú/«\x000fr²¹«\x0000\x0001³'8h»Eô³-¢Ç)\x000c^U#Âe(Ó\x000fS7à&;q1Àz\x0010cÞ:Ô\x0013b«\x0016[$±M&½Ô¯Â%6Û\x001aÒÂZ}!¦¨%¸rVôâYÝ
ï#VîXqâÌt²\x000f­éö!ÞöB4ñÛÝ{Ô¦
¨<R~V\x0000Ïn.>~DyÑN#õñº»Á\x0010Ä¢3,MGÎ
¶9l\x001f¡¾*\x0008Xûó-ñÕ?/þ¸|÷ÐP\x0004\x000fàÙýb;b¶àS:Ôç¤ÑT,Õü^ê@º\x000e_¿yþô!ÝùÁ³óÃD¢?ÈY:¿>\x0007Ã\x001ao:XücÊx®=Öªºw\x0002a¶J¤C\x0007í¹yQç´÷\x0012é"Ü©ãD$Sd
É$ë\x0003<|\x000b\x0003Q±®Þ}ûy³Ù=\x0000þ·ÅÅòàèúòúf9^\x000f-õ\x0012x¥u-\x0004z5a,4\x001f\x001eüvøüøàèôäôìxëù\x000eÒðt&J8PÉ>âLß*ÊÍÀ\x0004VHkX\x000f	&\x0004pcîfgg/\x0011û447°RfUS\x0006¸#SfF¿v(¦3!>ht¨YÈ ê\x001f\x0018½ìÂ¡ÏÏÑ[0]\x001fÿv~v\x0002 /ßì\x000búà4Wbsè¿j.ÍjØ\x000b\x001e¶ùH1^¯{Aû
R¯¹ï\x0013HÝ#+~{'\x0013\x0019¹ù@ñ=/?
 \x001eK\x000bhÈ¬t\x0001Þq÷ñãë!Þ*N\x000cõf^ÐÀ£¦´ø èaÍuzªXÕÑò\x000c\x000c8I¹sæ\x0018¯¡4[ÎD¬kÂÔ¢H¤1\x001f+\x001c2á¬¨ýÌCY\x0002ðFµQÊl\x001d«±\x0008L;¤(<Yß3aâudÚî¤\x0014ºg(+µ\x00102ò¢ç4"¹3	ó¯ð.Ü^?´^[^Ý\\x001cü¾¸ÿp}5ÂçíÊvPôjÕÀq\x001a¶Ìr¢ß_=?øýðü)üÉ.¸6Q¬\
lÐæ Aï\x0010eâº)­ÃÊ\x0004´¸°êâãC=%B{½¸¿YEþÁ|äæâR[Ä\x0017WÙäF:\x0008ïõáùÙñ¶ðÿ
O³ÕàaÝ!ùx!Hð?\x0004>Á\x0006\x0000sÁñ$±*8\x0019PjPrë!t²åÿd&¼~Ìu*6\x0012ìÂ\x0006ÀÀxZÞ<£(î?\x0003^\x0019´R~*øLÐ\#lP°ÁÒ·-s})\x001b6ÛÎ+Û¤üÔà\x0019+¦(7¦Y"¤»ñ´÷³-\x001fÖÑjiÈ§QÂN"HÁÐå8	Ï\x0014j[·|¥£cÁà\Q<=tcGt©\x0007¯hUÎT<»{Â'ßr³ÐaúÚU~[¬çÄºãùAÁa!$·\x0013Ï·xx©Ê¥ôf°B\x00006RÒÑ°9ÉÑpÔ5\x0007_,më^
mä!JK1ó¥®\x001d»~³ðnG[ùè¢ÕÌ\x0017\x001f¬dÈ¼|\x0012ã\x0007ão®gÍRF»\x0016/JñlÀamù$KbTëtX\x001cR~ª®\x0016#7sÄÎ0>ºR§M³¤rvþúèäðéÃ
§\x001a>]UÎT®_JÝÍÄ\x000fÎK½áÒö=\x0000ÿÎÆüMeÛX\x0017Ø+òýízlqÆX>°a4©ñØSgy\½-qÚ­QC@þítë4ãËËwéÊ\x000c©f.ÀF¾ùpq5ªÀN~öÔÝÑ\x0017ÊÝLj?ê\x000bý~xöôùË\x0011ùµ\x0015a7Ö­0'Ö\x000629Ø®²Hw-1ÉèQÖ\x0011ö³+\x00081ÅÉ\x0005¾^K­1";ê0@¼\x000fà½¿¹¹þQ\x0000= ¯v\x001eá],oÆÄ°Òf8\x001cnH¢(8çCFVgÊ5¬¬½GpÏÏ¶%lVp\x000f\x000bó§Á\x0001\x0002A¹l\x0003¡â¨\x001bÍp!lÎÓ\x000cçãer÷\x001b¹\x000en×@\x0006\x001eáâ³^
d`mB\x001d£\x0019a±\x0006·µ7Eßý}_[\x0019ØºÚt'»ñ-m6\¡\x0015°ïÏsr${I×È´°-
î»ÃçoFvÝ\x0010ÿ­zJg\x0013	Çr]jGT¬×¯\x0003|ZiGTa6Â~uÇdB\x001c\x0001Åc]0cébºkÌÁÏFØ¯î¨ t\¼\x0008î§Ê\x0004ÔÔ1*Vë±¤\\x001d!öðåjB£Iü\x0001Þ6CV\x001fêjuiÌ÷ýÈï>^^ý]$PM1K	ðdy}õ~yðbqóý~G['q\x001b¬'	wGq;RÚ\x001a\x0008:9>}yS:Îþí|»È\Çî¸DÓùBbÝD¬IeÃ\x0014{ßÄnÎfkM-_/Ó4Ïw2K\x0001ü7IDQ6j{ùN\x001dßz@c2`Ò¦«£IZB(\x0019b4mkáÉ$À·öGé0F
ßk­±øtu}y±\x0018Ásà¡ñ¼c0¹%"ä¨Çf,ÈßYð\x001a\x0010½<=y~¸\x0015Ò\.>åö&2sB\x001bÕÀi~v¹¼ø{L=\x0001[Æ
µµ\x001bøK\x001ec­y\x0010\x000ci
Î±æÄ6·sOù.Dx¤\x001eûTh\x0012k/\x0005ð9¹sJF\x0018±âf&Æ5]\x001aF%Cüpô«\x000bÜ/ê\x0000ð·ç[G¬ß®Qey
¶só:\x0006·úÖÛ\x0015\x001f*\x0019{£~« cL±\x0013v	\x001b\x001drà\x0017N}ÇÔñ\x000e9i°·\x001fnÂ·rÀñß2ò
ùâúêî= -ïÊ\x000cÑëûOË»Q/ ÃcÍM6\x0011åC#÷²\x0004	MÇ0Ööâôå2áùM\x001ezzþìøÍÖG±C¶èÖZ©©©e\x00067Tñ@\x001b*°¤,³Åûc\x001b­Ã\x00019a+}~újd\x0014\çRÈ\x001c¥3'¡\x001a\x0011gÅÊ\x0008É\x0015Ú\x001cÈ\x0018e{E\x000c¹\x001a9d\x0019jR¢)}Xs*¹(§£}Ë¸óòÓ\x001cÅ,Á\x0011\x0010ìá \x0019f.#æeÖ¥±~ QµÒÉÈ\x0005ÏÕÚ4hô
Ðª	ú2üð·-\x0005[\x0018î[ÝoeúÚõÈt8uÚJºk\x001c\x000bá%\x001f¤Ì3nWýêF­n\x001b
·âÂ\x0012^)ã\x0008\x0006×\x0016\x001bb<ÏOï/1ð¢â³?Ùzï42¯%¯}è2ÍZêð56×6\x0019óÇ»¿ââ»Ëû]z½¢|æ±\x0000QÞ\x0008á ÏËãó­£+\x0012[»&¢anè»%\x001bxÞ<ø8I&dl)\x0013FÒï/ÚIâK\x0008N aÓ"ê e*6ú-¡°i,}]êÝ,NBê	\x0005\x0014¹-j¢ÍyKÉÌ$\x0016¥Zê\x000bwÃèîÕS¦Ø
Jb~[u\x001aLÁ\x0016§î(%dðfïÝó"Æ´­®d\x001a\x000b\x0006\x0011tº0A¤hMÎ¹óÏ£ø¿¾(Û6Ãà(ÜÇågêÂpa\x0010ìµÕÂ0iøD×îÇb¹)\x0018wðò\x001aX\x0016¨Öû\x0015µÑÙ\x0019:DÑ\x0008	Rv%_FºGkp\x0003Âå÷öø\x0010e{_à£v¶µ}Å»6©\x0017_b~ItûÚ¦®á<éQ\x0011ß
`ÿyùá\x0002©¥º\x001fÀzµüV\x0002Ð£Áû(#hLÂ\x0011l¶\x001bÔ±Å\x0006Þò´\x0014×ãÕñ«\x0012ÞM¸Ö"0\x0010Ûäø"\x0003\x001f]Y%w-³ïæ!ì·jÖ\x0011z\x0019ÑI,\x0012	u7¢ÉíPi¨ì\x0017æT@:Ñ©Å@\x000cKq¸½¹¦o3\x001a=Ï:¹\x0013<\x0011,ua\x0002OsE\x000c£%ÝÓùúnn
í&×Ù(½«Nz\x001bÇ¦ëÕðaÓO®ÿ¾¶k	Çýè8OØ	Ldú\x001e|úç§wß.»\x001f^]..®F\x001fÖ53'~ÿáÓÊÇUºýGUÍ_ÀOÀ[S&g;¹\x000b¸¯YçÉ®\x0013·E\x0007\x000f\x0007ÉÇÊÕK7PÏ"+vç¯´zÌD·y6vÓu¶\x001dí¢º(öÖv¬¶d\x0002÷W?/>=t\x000bàQ~uy=ÁìÚ/Bí)©M7ºÝmÏ`\x0003ÒéN5\x0005»]<>\x0007ìK*<ÆRÁp°\x001aÍMâA½pÖ"ô»'qî*hÿH\x0016G\x001aÞbÆuÞ\x0006[TLe¶4\x000eÐnÖ2û:¦°ïêàðì¦ò\x0018Ã®\x001cjEñ¼!\x0014·µÂ¶{ñ¬ÖÜÉc­dk±\x0000æ\x000bYãð^ÑýxúHvò X_b\x001eKµªÀ\x0013¨ß\x000ey\ÛþY^}¿¤ptyÆßëly{ña)±ËåÁÏËÑêwµÇY;\x000c\x000eð\x0019$cR\x001e-×:;~ýüé1¦ÆVÕû»`ûFY-lÆÔ6ê\x001b©}Ãî+©Õ\x000fceµ-°ýY	Í±¼²Z±X\x0000Æô¤Ð¬t@Ïº´ë³S+q]æ~K\x0013º)´Ø Ê9yÓi¿~\x000e?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=<{sqðÒ³{\x000c \x001d~°h\x0003w§r8Ù(ÙbÒÚÔÎ\x001e0ç¿{øÛ¿ÿð{3#íæäÕÍý/w¨Ã¤M4Ñn~{ûñ¸ù>ßþË³xBî?Þ"\x0016`\x001asWP\x0006$Å±6@îñ5A¤3^¿ûê\x001d\x001e³ëË×ç_]¼:»|vöþb>káhnÚ \x001c¾Ï$6¬\x0014åá×Ø'¾×}ú)¿VR{{ó=M[ÿøøóíÇ/'7¿<¤wGAã\x0019ÅwÂ=n(%\x0004òu\x001bûcÐyØe}{yöü<Ç\x0001__¿:ýþäìú_ã/Wû¦âµìY¨[ÙA¤ðA#¼QÄÎ£k=\x000f°ÛÈ®±qOÞ½V¸ÜÕZK#É±¤ÕÿS\x0004G\x0017m\x0016¼¦Ým¢®\x0007Ú4&{¨³à"ø<(ïÿG\x001b^üûïâ·¯\x000eëûO¿}úØ\x0019°èU$N\x000bÑU\x000bI8ë³¡¹\x0013ËJäýÕ¿¼Ù\x0013H_~ÿð\x001fÿùPkÝÛo£®¿ù±O¯\x0019\x0019YiÛ:ûEÝ&s²\x0011N%óËK\x001f
é·Ñ:½<ÿêû\x001fn>*ÿ0GãY#h\x0013Û2\x0003ý\x0016\x0010ÍË<\x0004TÐÔú\x0000Z®fÞá'¾Ê\x001b£\x000f*Õ{{rÆáî¡Ï4Î×o\x0014aÔZ\x000e 
è
MþØ³\x0001ÏO¸¸:`$
±ªÕjb\x0003Ø\x0001$\x0011c\x000fH:3%ëù\x000eþ\x0014ÈºFÖ«±SV(Bl£g
EÊúÉ¡FõÈ­\x0005Áû"\x0008²f^Û§\x0013²©Íú}!ð\x0011!ï\x000by­eM ä²ZÃëk^¿\x00173\x0016L°ÔIÍâ\x0013'Ù­÷±ÍÈ&ì(\x000b\x0013ª@ÇBÓ8þü[ó`£t©\x0011v®¥Ç¯]Zºµ³N;JªjRµ\x0014ù|FÅ2|ÚÓ\x001aÜúAÖ\x000f`ñg2?}}ûð3UÜÞýú[\x0007ªØ5$£b¡f*7´FPý\x001ch©Ã²ýÿúüê\x0015ÕÝ^|»ç\x001ePÜA?f;_ãO^ÞÝúÒÅ
2»YàzÁÙx½Q¤\x0011\x0004ìÑaÑ å×ù\x0017oö¼+Ö¬ªfU«Xñ!Ù¥³\x0015õXtm!Ë5äÆ, [\x0016k/kjsÓ+U<¹ÿó\x001fïï>÷i.£\x0015dÑRë`ô\x0002ùîè1 °wÃF=prþòòâÝ¡Ã¥ÔÎáRÕÉQ\I\x001b!åK
²¿R1-Øe½5L«kZ½V\x0007_|D-¥\x0005h{÷¸\x000bÃ¸PãÂjÜ<\x0015q=ä\x0012>ÄUt]÷îò\x001aÁ55®YëUq\x0013¼=Í{Á\x0016Uë¢½`kZ»Z¸\x001aü#mÐäÔXÏ·-ï}ÝaXWÃºÕ¢õ©qO\x0012-õ>CZÉ\x001b×mZáFì\x00183Ã77?GTE@Çq-fgÑºèíf\x001b\x0018\x0012m0aù}sö
ÛF¼>9«j\µ\x0012×Ø4\x0017ömJ,´ »\x0018Ô²X«k\½\x0012×Ë\x0014E^lv.\x0018\x0019ÈO\x0010Üôâ	x¡æ¼N\x000bk¸èâøì,DULZ,8ùdòµ5¯]Ë\x000bpJ¾¸O9»È¡xæõËÞí
^_óúµ¼ñ\x001a)òþu8M%oè0\x0011\x000eX\x0006ö4ÀR4êA¬%öÕ\x0017@®.ÄMG.=nÃ
âFCÈµ*ÂF~§3:J§C'r5=\x001e:±\x001cÒ_AÜ\x001c:¹öÔùx¥Ty\x001bãÔ\x0004äg¹H¬ôVâxÞÄçkÅüFyòì>â¥ÉD\x001dÁgGg\x000fÎé5ÑÎÑÈ6Ì\x0005r\x0007Ìr¹®<»Äÿõ8¸®Áõ&p°\x001c5Ç\x0008\x000f+Áo>Î\x001dð~ÆÉMMn6Çýìd!'ßÂx~¬äO#saw6ØM\x0015}~óðpws;\x001c¸@f\x0005¯Ë\x0014F\x0013\x0014·å=ÁÊêy÷ùÙÕÕÅùÞ§Ý\x001aZÕÐj\x0003t°µd\x000cEÙ&ÀÎFÀR³§À]YCÝX«[xÀwÕ¼¯M´ãi\x0018É¯\x0012Ú/«R{LÔ/ýªÖ jì¿BG0î
\x0003\x0014ëQä$;)\x000f^ºQuªW¡zÇ\x000fYM|Wb\x001f\x0007l%\x0014Öâ\x0013»'lCd\x001b÷kð5²9xóèF55ªY»þßäj×´ü¼S{\x001a¡ÚÔ®\x0012ª6Eå\x001aà§>j¬OÍëÔ×¤~\x0015)Å¢ úÄô
£ÒÑ¼=DWÕX\x0003*\x001dph\x0007´&wÇj¯\x0003½zùV4¬§8·qÒUuíj%Ç{¤añh
ø!È)} >¢\x0004va%ñ?[\x0017|\x0010Ú5¶àYü -x\x001a¡wyK9\x0018:p°/þÈ:\x0016\x000fÙT\x0002Ãgá½¼¹é-2´-âMÃi0âR¦¼h:\x000bËFl}`cø]ïÀ×\x0001ëç\x001e¿<>ôÙêùtÊP\x0011¸¼\x0005Ù=¹N\x001c:;yþæúýõ¾\x000cÎWÕ¼j-o\x0010EQãä,\x0003EQØÃx\x0004X×Àz5°b_\x0001&\x000f,
ïDðt\x001265°Y\x000b\x001co÷\x000c1æÅµdÞÃ1ö	wÞÁ=¿¸µ¾í3g\x0017·T\x0016msà\x000f\x001f¯r)ú`2YÅZÛä³Ýª j\x0015\x0001>ûðpûøë§».W\x001c£gd0|ylñB°ÁðúÈsÀÙ³«óëoß\ìÉÏÏØ»gMûÅ¸.b|\x001cTS\x001aæt,9\x0007·75§\x0000ë\x001ax)\x000b®/ü °µdÎ}ó¹q\x001cÆ\x001fJ
Ø\x0013û[\x0001\x000c5ðRæ[MáÎ	o³Ã>ow¾Û^ÞxÞôîyÓÍy\x001b\x0008J\x0005Zd¦cíOU\x000eµ[ÅÖ-ÚÎ#?XÈ
ß}ÿåæo?="-v½Æ¯Ë»ÛÇ\x0017w_Nî1&òéûG4Ó\x001cÎðÕ·üãã\x001fÿxøt\x001f¯ïH¨#Z6¿>\x0004G}F-úPFçëçWo./ã\x001düòâüúäÅÅûK\x000c¼y~½ïZ\x001e¾ûOõÃ_oþNÂ¬4ÁÛO?ÿ|ûð)¥\x001c`3\x0001\x0004¶\x0013lNãôä1ê\x0010rvcð\x0018\x001ekáèä¿}óêUühorH3ÜFÑ0%	A1s\x001dsDfì\x0013åôÖQ2crXDÓÔXË¹\x0002:¢qwémBK\x001e`{\x0017è&´js\x0012¡¤$6\x0010*?è !¨ívú í¼hÎoS]Â77\x001f?Þür{ä\`ÆLÎúôÑ>z\x001c\x001c+ìd6>ÁKOMH'ÈhÅ#æÉ7g¯_½Ý\x001b­ª U
©V@F¶|¯öÎDõ_Bt\x0010@\x0004Çöf=¤®!õ
ÈB%3Ò\x0005«ñ¥4C
nÃ¾\x0001\x0012jHX#IL\x0005MÑ»Ì\x0003xâeÚ8\x0016¤æ\äõ¦f4k\x0004©Uª\x0019CA
Èãa¢ m®Å,þÐzH[CÚ\x0015\x0006\x001f\x0013Ñây}µm^mìQ\x0004\x0017Àl>7®tk$\x0019ÍrÈ\x001a(npò"¢/\x001dá\x0008É­7@ú\x001aÒ¯2_4½¶9·?³Zï\x0010hêß\x0006ÂP\x0013\x0015R:²Ï\x0016ÕOêFí-²}vø¼\x0011ÿöï¦ÉïÃrô6»qGJCõ\x001dZ@[Án l4¹\£Êµ\x0017©W¤t<È5\x001exßÓjÒn¥l´¤\£&e0L9/9 á=i½Ý¶-\x0010Í§ßÇ9±°>\x001cLÃ¡
å$­8x¹öxÿòÁ|øøeÇ¥ýúÓÇ/7w\x001fã\x000f7?¦\x001cÍ\x000fùÊÛÑåY)Ñ± A¸\x001dõ®\x0008£÷óõ×ïÏ.^Ç\x001fÎ^¾yO·ô}\x000e69´c`!7ÐOJQæ¹\x0011\x0011,\x0018ÖÜ~¶\x0003\x0007ÁrÕÐ0R2\x0007¼QxifgÜt^ÒÑPvæ
Åÿ.»Fb&wYÄ¥\x0014|Ý×8$&ôFE»á×e?+\x000eì>MG¼&}ó\x0010v=10TÄün1D&Ó\x001c\x001e\x00047brýUÀª\x0004¦¥Ý\x0008\x0016w¾\³ûeH±Ü¼É\x001c>T$2P7Úu¥{ÈDS+M\x001f«0æDÆÛüãß\x000fÃY\x0019\x001cß°â\PJt\x0019ñÎ/À½89u~ý¯\x0007T®¬ß¢	NÁ¥á´>»¥ØÃÒ±\x0004\x0008òï­Z\?®áô¨äÍõ\x0010Qr
èò\x0015É\x0004\x0017ÕîÒ]³\x001b\x000ej8\x0018\4¡&/«
@ïKQn\x0014D°RnA³5\x001dF£ |Dó*ÏàÀ(¥\x001dgBX°Rýp®sÝÓò\x001dÃá\x0010¿\Ö
RÈ@³n×ï\x001có5\x001fr9=JNSãX\x000c
}÷Æ¸MË\x001aj¸0\x0008\x0017À©1ä|\x0008zWHÏw
\x0011¶\x001c\x0007Ùj¹A5g\x0002Ør\x001e ·
ð¼é\°§ýt&ªÄ\x0004MU­NV\x000bK²óF-\x000b+MCgFé¤å3a<På(K¼¬mÑÂ²Ñ&r:ñ9(9r\x0005\x001d\x0008rÈ}¼è\x001cÚvËïÑõ¶+ïÑÓÖ+ÉU»ObÍêl÷m3²»j1º&þÔ&åâã¿\x00195¾fsæõ+ÜÃXJæ\x000fªÄÖ¯?=\x001có°\x000b¥\x0008ò\x001cR	bSÚ©¥Ãq\x001d=¨«}¥f\x0015ª¹Ô\x0010Ï\x0013\x001d\x0012á[MP¬µ
K«Ú\x000b¦k0=\x0002OC\x0014`Ö:äÖû\x0011\x000c\x0018LÍcP#`PÁÄ\x0004T¹dYI¼Þ¬ç25\x0019\x0012â8S¦Äh\x0003§\x0002»OUC`¶\x0006³c\x0002KÁØ$0kOéJ\x0006Ò¼ñN³ä*õr¹Ë	\x000c°²:?aH^H§È^ÉRM·Ë×\~LU¨²ó±Û\x0018©À/TaËÆ\x000f5W\x0018\x00176åÍáugpzTÂ2lA%ÀWÙÉU\x00052e5²SU¨9ï üÝ¨*4¿6nR®²UúCZ?\x0008K1j'å\x0018u ÌÎ(3å6(\x000bÙ¨}9¤÷Ñ½Í`*¤qy1õô@»EdÚCz\x001fç6Ób
zÑWdº¹\x0008X±uc5J_\x000ei}EÚ¥°\x000cí~¾ï)m6IÙ(W9¤]Ì^mÉMPl¤\¾öR5*Lé0mrW\x0013\Åô\x0016Z·âBUÊU×5#ùz.Ú«Ow\x001f¿eZÁKi/Î¤\x0011öèüÝÉ«7\x0017¯\x000fFèu]\x001cBtjÎ9v\x0014
MfsÉ±,\x0008bñõ¿\x001fO×xz\x0014OKö\x0017Ó-OÓÂrúD¼å-\x001d\x0001<¨ñ`\x000c\x000f\x0002¸\û\x0018=ýà(%\x0006[sg£\x001eMþ¢ñ\x001cÀ35\x0019\x001e`èñU\x001fµâ+²\x001bÖÖpvPv>È\Ó\x0018\x001d¶è§å\x000eeè³g¡A<Wã¹QÙá\x0013*	\x000fk\x0019óÎÓBm~ÑbâN?¯ñü¨ô\nLÒsÀOQxaÉ;\x001a \x000b5]\x0018\x0014\x001ev:1\x0014\x0012\x0004NÕ×VÑ·vñ65¢U¾û¾Õ+ß\x0011b/V²ûøt\x001f\x0018´óPd¼Ø¸¼ú»/-á?\x000c?´\x001f\x0006e\x0018l£2ÄúSz¡\x000c,Bë7\x0002B\x0013£Iú¹X×§¢uêç\x000e¤) QE\x000bÖÐO ÅV7&\x000e#¿\x0014èÂ¢\x001cªñóï±+²\x0014u}tþ Êûü\x001f7?ßýøñ·Ã|Úc»tRB¤¢
)±³aJI°lFNþÇÙ»w\x0017/_ïk	U\x0001ª\x001aP
\x0003\x0002Ý-\x0002@\x001aQ|\x0002ÛUf¾°\x0018\x0008\x001eáÓ5\x001eæ\x0013\x000e­\x001b\x0002èmå\x0005Øq9\x0003ÆKäÒ-c\x0004\x0010j@\x0018\x0006,lÑ¡±GØjy|âz>SóQ¾¨ÿ(Ô\x001f\\x0014`¾\x000cÅ¡\x0015°øÀ4\x0002hk@;,Àx[Ë^j08BVØ¦\x0019\a±øæ:\x0002èj@7,AcÈ×
®G\x0002¯EoÏ#Ø\x0008¯ùü#KpÒ$¥0Q3d\x0001YÂç(`¨\x0001Ã°\x0000µÀî}I> k ð\x0016Ä±\x000bÛ\x0000§TÒÒb\\x0002{\x0007%\x0011ZOo\x0011QËÄE\x0018ödç÷\x0013¶vdØà`i:%A\x0019º\x0008 ¦Ú\x0006½|Õ\x001c l\x000c\x001c¶$.4\x0010e\x0018¸.^
­é\x001cÚ
ßOØ\x00129lK¬\x000f¹\x00066Ê\x0010\x000bxe®\x000fÁ\°,C«7dÙØ\x00129lLóäÎ`vq±v\x0012ß\x0017ÒIjë>l¬\x001c6'Ö;ò\x0017å¤'³ÀX\x001buµl\x001c¶&ñB\x001bÙy|\x000f£B;\x0011Ýj:'\x0006o\x00035Ãæä.ÁÆÈasâ§Ë]ôýtÚZ³¦[]BÕhk5¬­mHSsCï+×yIÇu^në\x001a7\x000fÜ¤\x000f«ò ^QúÜ\x000c]/yÊ98ö¼\x0016S@\×]LXAé£=!ÿKqOx)°÷cv`gesãW]L½J"÷\x0004Ò\x0004nÃèàÝ|\x00130»f
'Íç\x0007Ûe6j IvÐ,??ôp"a\x001b´\x0016¦J!xöðÇÿ{¬bÍ\x000böf\x001dV\x0013\x001b³ h?¨=ÑþgW×ªÕÄnù0Õc}\x0017ó&÷=C6ÃÉäÁ\x0016ýºÁl
f\x0007ÁpÃy\x0002+åJNq¹Rd[~Rêdó5\x001fdÓß-1I¹\Np$	xFÒ:¶ê±Wú±·\x000fNä\x0011\x0008E3\x001cµslb1/´­9\x0008rð$XÌsÏ±#\x0000ÍÄË\x0012\x0015Ä\x001büR\x0002w\x0007®[tä\x000fª\x0004¤2=û ÜlÙp8þ\x001b\x001dpOØvh~vÍ¦j65Ææ¥ `\].\x0004W(N^ImÏ·Àé\x001aN\x000f
Û3eÁ):\x000cÎ°àö¼ýö²AÍ\x0006lÑ	ðôÐOÔ\x0004Ç%àiÎ\x00064S£14ÍG©Ô1µ|MÇ\x0014´"±©Å\x001að~6[³ÙÑ%\x0015TÎ\x0010ÅV
Ô\x001d,À5]t÷úá|
çÇà ®©Êµ\x0016N9~cÕØ\x0010\x000blÈ \x0016ù'Ã	Û>1àÊ\x0016éO³¸»~\x0011\x0013¸Y¥(ÌYMvÂ{>\x001cA\x001e<¸\x000b­pRÛ±\x0012Ò­+Âs&ÌÏâã$\x001c\x0017ÄRbÜN©Ïä\x0012·c-¤[U&ÊÞâr>ZtE9Wß/9£ºÆÔ«DI]z°\x0008\x000ehØ\x0013J³\x0014,½wbB	+0qFV§Z)Á\x001e7\x0015\x00199\x0017´õ(¦©1WÕ:JAyEV:N£VÁZ&öÄÚikÌU¶T~cr"¥p:#øx¥ÇìQL_c®ªT^´mjð@uÚ:8\x000fKáÕAÌ:³Ó­¬ôJo-¦¹qñ¡âBR½²5ÊÙh¤uEØbPgNÁé*hM.¶rKÙGÃ»³Ê\x0012HûóÃ8©<¹é5^Ñã\x0006 ,vÌíz\x0012Òï[ÒïÇI£T©¤Ãb\x0017_Éi?
O
ãEÄ\x001d¤7-éÍÓ\x0004²/,&\x0003qå:ÆæòirK¯¢Ý¤j'w\x0000CUêãË»\x001f?Þ<üp4»Á(n7\x0013O
=XhÏù{éo1¹áåÕÅË×gW/\x000e¶(ØI\x001f@Fµ\x0011<2)m:nUºâGk;¤®!õ8$¶\x0003£LHi\x0014WY
\x001a¡¹ÝËO¤CPCÂ
HÈ]¸ç4\x0002\x001dBàlj»d,\x0007	MMhV\x0010ZNÁJjÇ¥9t(í¬ûÈ8£­\x0019í\x001aFàÊxåñTÁ­<\x0019)îC²Òêéd\x0018ÇÔº\x001c\x001b¯¹ß\x0002vgâõ^,#\x001cå¼i9oÆ÷ÔK\x0018O©Ú\x0007_²ü\x0017£\x0016BíèI¡\x0002\x001fOÝ\x001c%\x000cB\x0017ÎDÃÓÉÑ%	Û.¦\x0011¿>yvÖ\x0001§k8=\x000c'¸ÐÖ@\x0003\x001atP\x0003 °d»;á\x00063)ÛCQ>ï¸QÑK#\x001f"¼¥#ÝÁ·ü/lÛ¦8µ <f¥¥¤¦$ø®ÂíÖâ¥ë÷üb\x0019kjDºN\x001e\x0007T5 \x001a\x0005´ØÌÂÛ\x00004~J[ËÅÀz±Å\x0008\x001fÔ|°Fü "4OXüÃÏÌê\x0002Ú\x001aÐ\x000e\x0003ÔÖ1êh®mrZrý^ê 4\x0004X+Á´	oÈÙâ\x000e$·§7/\x0003\v»'õæ(ãhcü\x000c­S>Æg'/n?~üaªç?U\x001d£~9\x0006íhrÇ\x001c\tâ\x0006bB0ËM#Þ½»~Q«çßæQo+ô)®\x0016v¦\3\x0019	úcjØFSDHsÑQ\x0004æ@½_Èÿ¿/ô\x0017v£\x000er\x001c¡#eF=¨(\x0017B\x001b	\x001c\x0010ZòÊz)a·½'VE¾½ýr÷åöäìááÓãM6xèá9Þ­Ñ'Ãg\x0015µe^aÕ"=<ÇÛýÞÃþöüýÅûó³««7×gû
VØºÆÖë±A¸@%^\x0011Ûça@\x0012T^N6\x0019cnºyç\x000fêñEØÍûñÇÇÏ_â/Ïn?ßà?~DØ.Þuò[\x000e©Ç\x0007ØôÊï²N\x0008ñÃÁ=þOÎ®_^¿{\x001f|vþîìõó½]È+n]sëmÜ\x0015nÀÞP²{4Y\x0004ÌIO\x0004Þº'Nà\x0016vë(<\x001bÅk(î)0µ¾»YV±Ãîå\x001dDµY®\x001e\x001fnîS[ê¨Dº?sÕ³æòunGÍý"øÕõÕÙeêP\x001d\x0015ÊÔ2x¹ßwÅ®jvµ]C\x001e	°Û\x001fágý¡7Âë\x001a^o7*OÀú|_\x001a¡Ð`n¬Ïß-R^\x0007ÿ!Õá¶mÎ%:ã¿`d
7ýÅÃ±}n\´ß*\x0019ð4þOPF\x0007÷k¶\x0001v÷ùåÉù[K½8¹¸{{\x001fåß)o¢$àýkJ FAövZÇ\x0013JOípHûÅ+\x000eeàÝ\x0013L85Z_dôâ;ùïöo\x001fÿØp\x0010¿.~þåæóç|m}vûøÃÝí\x0003ò©,k/°aýÝï·÷¦¼Ñ2Å(¤::Gz4>_§\x000bÆ~iäP^üÛùåW\x0017¯Þa¯z¼°>;¿~qq~µçVÓ á¥
¿\x0006Ñ@çÍl4z\x001dïù²l<¾d\x000b\x001b6\x0003À¯Q6ËX"\x001b&°©Ì\x001bh\x001c©ë·£á0B·BlÔ9¢Et\x000bLWhIl\x001cØ9­a\jÑÏR:£i¯Ï\x0011Í\x0019Úmñþ÷\x0004+UÚø5È¦|º\x0005D4üÉÐAÈ]#\x0010í	6\x001b¶ôý*}\x001bÊ­\x000c\x0011.½\x0017e¸@l¥Ùò\x00166|¾JßFåFùt
«\x000biMM~¶pûÊmCÁÉqÁå\x0016À\x0019\x000e²Û3%§\x0000\x000e-Bú6
§òmIbß\x001bLÑÎËYk\x0011Î<ÅÃWéÛ
É©\x0002\x0017ø<\x0018]àÜv83+$çp`s67¹E8ÅpeRç\x00168pn\x001cNçÓÂ\x000cm8x\x0010É¢\x0004\x000cOÃ
Ë CN@±A\x000eý"/b³O°¦X¾
Â\x00198Íj\x0004[|\x0015ZØdx\x0002¶K\x001aÆÔè\x001c\x0017p@·@sáäv8\x000c8}¾
ÂåÚ¬\x000cg0¾pZx¶\RlW#

Za\x001dè	,²E\x001b¬áâòn?
Ø\x0000å«ôm\x0010Í\x00056\JQÛç\x0008§Uí¶!U\x0007¤opÞáX×\x0004'mÐ Éä+¯Vûånn~Ó÷\x0014þª¹1¤¡Ú·\x001fo\x001f½ÝÏ\x00066µE6ëmª±´N\x0013Ë!ÏWëo÷Ä\x001a6¼³I9\x000e\x0017Õ\x0008Y|ëé2\x0018á,o9'`YpctXW_£t83/+VeÉl\x001e$(ZÖinó&:ÿ_kèHvæ\x0013 f¸§XW<T°MY¶]N\x0014Ã*!-çZV%t³j'Ì±d¤\x0013|±Ò\x0017Ñe\x000f}\x000e+ËÜ
ÙáÌ|`\x001dAÉë*â\x0003«õòmu.ª\x0012·B\x0008Ë×|']\x001eftEvz\x001b<D'Óx\x0000¹Fxø&±gJÎ4Ix¬P]6\x0013cxP¾âIËç$N\x0002ÈÍ\x0002âÎ\x0013×6ì¹~á\x0019Ä3kð\x000c«\x0014Ä\x000bt.-tO ï$¶¥Mßéh\x001côXçg	jÁ´ÅÆOÍ\x0010Ò·a<\x0003ø\x0012;çNü(=Íx¥\x001bÎ
¼\x001fÃO¿ÿÎY¬_µ]\x001aØúæîóíýí½xÑÿÕ§>\x000ccSË
}
BKOk³ÇÐ^¼¹xw~y¾'#ÐcX;TÙþôA\x0011øöáîçÛ_ÿø?\x000f·û}¨ ¤\x001báÀ\x0004 " ½g ¹q\x001eÎÛ«Wçß_íkvTã©\x001aO
ãù\x0013ù°´Îd>\x001aò|ÒoäÓ5\x001eäØJ(áa
§Ï«+¬$ÅbTã®Á\x001a\x000fFñg\x000bNe£-Û\x0003ée#ÜÈgj>3Ê§\x0005\x001f^p"§jD¾ yû°uymÍgGùÐ\x0013PÌá.l[«ÙÜèÑð¯´ài`ÄãX,NìÙçk<?g\®ÍK+óå,\x001aÚPÄ·õh/ò¤P6X_\x001añ`ñ	¯·áIÑèe1Ê§\x0004ßÑ¢\x000eÆz¶\x0004\x0008ªl?»ñèÊÖp\x000cZ\x000eìÁYÀÊâì\x0006\x0011\x0004ÍV	6¦C\x000eÛ\x000ecù\x001eibÏ \x0012²òÓ\x001b7 lL\x001cµ\x001dñ\x0006GKgÛË|Æb{·
°1\x001erÔz`A±R\x0004èùm1hÇ¾Ñ[\x0001\x001bë!GÍ\x0007\x0011^a¥O\x001d\x001d\x0011	Ìç7ª@ÙX\x000f9j><ë(óQ\x0010(X©\x0018Ð­Ü÷¿ýõã}*VÑèjÒ.÷ìÝÍãý§\x000entè)J\x0000Ar\x0004\x0007\x0019¢ÓÒDê2R½;»¾|óúÝî\x0010·$¿å&\x000cæ+7õt{~óøðéî\x0000U2§Cf[æóJbØäÜÖ<?»¾^òUÌ\¾áò#\ñFaä7\x0014(ë'5¬ÆBÔXR\x0001.0y¤\x0006ê^+\x0012"*K(`~2ûÁB\x000b6"0£øñ:Y­\x001c/\x0006ÍE\x0013\x001dúõ`A@°ª\Ä\.Î`Zå²'ç\x0007ççæ´\x001bLµ\x0012S#\x0012sÀ7x?¤Ð\x0004XV±)L¹\x0016ËÈ\x0006ËÈ\x0001¬xo¥Ü
lZn³ê 8y#
[ß\x0006Ì~0'UND0Åo®Ñ>\x00150»KA#0üµ\x000b»qÑBê[æD®\x0012\x0002\x0003¯×ï|l
T\x0011y³¢\x0011Ìæt5\x001d¬d?-*Ü
\x0012kWR¬¤\x0017%\x0007\x0007´¤w/\x000b%sÉ-¸?Ý\¡å
#\J\x0014.U"üÖÚ\x0002¦Ö\x000bLË\x0006LË\x00110V\x0012Ý¼Å(gÒú¹;Ñ
\x0006rÅ_ûÁ¢`s\x0014\x001dEµ¾ã R¼\x001e¬Ñ­Rì\x0004°Xu	8êèx¼wû\x0015\x000fÎ;ÌiNl±Ò,ùìè\x001c\x0003S²\x0001CdÔ0
Éó\x001c_#ÙâÝ¤LL\x00112ë8\x001eè|n4"ãx\x0015.u7kÀÜ\x0010X (ªdÿÐQa=FQ\x0017Ìd?m°ì\x0010ÏA\x0004£)e5bñs±»~ô\x0008o ü\x0008\x0014öà¨©Ü[c\x000frïX\x000c«uÉ)æd)U¯\x001f
õ\x0003ß)]Î·×Øß#¦Fm\x0010lÏ¤\x001c:Ø >\x0007\x000bBîØ\x0011¹T	WÙp"¥¶
¶#\@ÍDð¾F\x001d°ª%Ö>ý
,\x000cQóc\x0014æcé\x0001ø\x0000Ø²Ð¢Á\x0010¥i(´Àn¢·%öã¶\x0008Í@Cf`HhPbÞ!¥è%2í
ÚbÜ¬\x0017Í¶Ó\x000e\x001dNî³höÎÈ`U¢µbèlºTªË\x0017^
×FW­Ü+Õ\x0006¡)Ù\x0018L%G,f°!kÄ\x000bÄ²³æ8Ì\x0008Ao8\x0004±Q£©¡õÄ\x0000BÃp7IÍ\x0015OÖÃ&4ß¢ù!©rÓ>·øÀóÉ\x0019Ñàå\x00164h\x0017\x0014Æ\x0016TRÌ'Þ\x0004V|Y³Ë´Ïeh6i-ßÝÜ}üò/oïn\x001f\x001e\x000e<tc\x0011Êd\x0005(¨,g\x0018mwmú»³×ïOÞ^_]íâf2Õ©14©ËÅ$ÐD=,ø\x0007(Úv÷Æ4ÄfD#51Â\x0006Aq^\x0017NÈÇSÉ\x0012*Y\x0010{M7lzÍÛrÓ\x000c?jzb,#Ó×±ÙP³Ù0Ä\x00165®f¹\x0015+CYS,«ÞÀæýæö\x001bÄK
¨âwÈì\x0011I_\x001eï@í\x001aª!6ß°ù16ã¦\x00058%4êN¼}»yÛ Ù1±é(Ü\x0000\x0018sRe9
~7¦×ÇÆ]´¦÷lYÞ³ÏîÿúpûÃÉëO_¾\x001cÌñQÁqÄÑD\x0019
ºLIÎ5~\x0016Ý8»üúêüÅÉë7ïß\x001fI¡\x0016o
 \x001c&\x0004[níÆã\x000eÌñ\x0017N52e4çjÂéæúMaBÉ\x0018Êé]À\x0006¶ª&ÌÂïÃº!Ô£Úp\x001c>­r>\x001fÖ;>º\x0017yºÐ$À0\x000c(§m\x0008g'GÓÏ.\x000e£`k@°£Ò\x0010ÀFn	Ïp2ñ3õ2×\x001c\x0012\x0018>$Ê¡B.Ù\x0017°Îc<\x000bÕ\x0012f\x000bá-¨RGÎD\x0008C\x0010Ö¤(7Ký\x0018%´Í1¶ÃÇXSM6\x0004<\x00176ÄUfEíåV\x0019ºÐ
\x0013FÓ¦Xlå,\x0000[¹2-e= o\x0000ý `\x001auDLPEZ²q³xÎ(¡o\x0008ý0¡7%\x0012\x0006\x0002¯ù]\x001f²Û5Æ£¡\x0001\x000cÃlItô\x0004é`Æ\x0006ÑÉ]~\x0010Oªf\x000bJ5º\x0007\x001dZ8N\x001aSK\x000fnSÎÀ,Z1JØZc9lqâáôÆò\x0000\x0011M\x001c\x000bQÎîl£Ð"Â0¢	§tsæ\x0018$\x0011rÕC¼¬'ty Æô¦êLI3{	$÷'Ïî~üxûáæ\x0000 *U>XUîHÚqY¡5f÷¼:»z~~yòìâåëógg\x001dº!Ô&h.~°\x001aø¨hÃUÀQoï\x001eQBåjBåF	=ä©èHèù=@\x0003¯²µ³\x0010Õ(¡nVY®²ÁãAUUQ]S2¡ÖühËÀ¨ÕÛ	lvx\x001f*\x000eÛZL¥Î%übÃLÛ\x0002\x0006Ð\x0002FÌùÀÑA`·F«²
g	.Õ»O:'üîÓO\x00189\x000cUÎyþå\x0002aS*çvUÍ(`\x001fäªü ~@L(áú9Y
\x0004ö\x000cãMy×i\x0018EÔ;ºfXÙDo«\x0014ÉõKØkp*ì:¯Ã®E\x001cÖ6JSF\x0013æê\x0000wlà´V§ÅÖ8Å\x0003\x0013!\x0007\x0004\x0007\x0008\x0005ßQ°ÖhøÝÊÍ.Q£¶%´ÃÂR\x0004'Ê
@i¶zNÙVOº\x0016Ñ#J~÷À\* \x0007F[¥X%&Ä0rÊKIùl´ÎJó¬7Zfé[)úQ)B¼§\x0000\x0017;Û<¿	ÃÓüT?w³	[¥èG"`»aYH\x001cqqÞÕ8"ÖE\x000c£ÞCB\x0004²ÍýlUj\x0000m=\x000f#ú\x0016Ñ¯Xgº0c_ÉÏ\x0010¥¦}\x0016s\x0018$T¦±,ÊZ\x0016°UU)Ð£Ã|§Çé¶E´ãâD©¹NÖqú×\x0002\x000e\x0003\x0016pXá\x0018Ïõb&H\x0010Ëx²	Qm=ÎÊ5^"þ:hù]ÇÒ.åÕÕÙºÆ¡å\x000bã|À\x0019ä&\x001e\x0014
aK«yÕ¬®m\x0010Qf\x001bâ¯+DHÁ/gòð®$EÎEn	mK8.DÇ$Qæ#¯³àu³(ö(¢j\x0011Õ0"Lqb\x001c¯@§Ùð:0«\x0019Ft-â¨#R\x0008Ú\x0011¢É\x0002êFÝh=¬n`ªpÓ%H)H·UecáF\x0008Ãv\x000fC² ªÒ.¥D97Ú=m[©6£·R\x0000Ã}«\x000c#Ý3T6\x001e´\x0006ÑÂ("¶Þ¦<SeùiTêò\x001e`·º`Ú·[Ñ\x000foEmKªQôcIURÝ*ÄÐø±øë ¡
åÙG¼\x001e©|yß\x0006¹uI
\x0015ìÞC\x0019>ÖrJT¼\x000fÅÖ=´:\x001bÆu¶Ò¹Ñ7Æ³ýD(J»­W{°¾Á_\x0007\x0011Íã­r\x0017µ@\x0012a*ÞØxRÀµnPpRWD©\x0013%\x000f\x0003\x0016pø(\x000bWRó" +½JÛhUh\x0014"þ:¨ãEs.E©\x0014³\x0008ÀÌêEG\x0011ÛX¢\x0019%F\x0015Ê=ðGÊ;\x0013®¼¬´-× ¶1w3\x001ctÇ¶H\x00141Ö^2¢\x0014lAëÇ9g\x001e[\x0005ÞyVîÐ\x000b\x000b_ïCn\x0002S?°8±^Rç\x0007©È(ºLªª2úööáÇC]\x0008ÓØ\x0000JøR4\x000eöX!µ­üR¾è·çW/\x000fµ\x001f,\ºáÒ#\ÚpÄ!þ\½U\é¸gÞM\x0006
\x0019\x000ciÎÍoÈÌ\x0013Ìüdf\x001b2;B\x0016ï"ÔNEÉÔV\x001dÉd	 E³i¹Ì\x0001Î\x000f ²<¿\x0008&¹°ZÍr
¸|ÃåG¸¬æäZ\x0018ÄJ\x0008]Í\x0013ÈBC\x0016FÈ°©j(d"k\x000ciØ\x0013U~±\x0006ª¬ªþÃH¨\x0018"\x00036ýJº²Ë§!
\x001c!ó:OôÉddf¹Z8-ucê&kô¿\x001eÑÿJ¤>\x0007úlG²\x0000ådÎb~Cd\x0005Ð#\x0016@éÒ{\x000eûãÜ<-~Zd¶Pù=@ÖX\x0000=b\x0001°{uÑfm¦²\x0013ØRuV7Xc\x0000ô\x0001\x0008|ÃI`$27)md\x0001Ð#\x0006@E'Òêr\x0000 ·ûÒ£Qj¹`¦¬1\x0000zÄ\x0000è©ú\x0003fÖ\x0019\x001a¦]\x0006\x001bvô~HÑâc¹-«éÙ6i-\x0015u2Z\x0019'³¦v³1ïÌ\x0019\x000eé¨<ð#kZî|·ÁÍP¡Q³*èY\x0005Sû{©r)\x000f¤þ\x0013Ybn\x0016\x000c\x001bnÝ\x000c=ägÄ
^$\x0016É\x001c \x000bÚ!\x000b°\x0017Mä\x0003`§ØHD³ÓÔÉgw÷÷¿í¿¨`éMJF¥\x0016ï&>fªyÊÈóx/¹¼üËËSFò²Fò²\x0017	§xP±¤4\x0002óª\x0012å\x000b¼Rf¡\x0015I\x0017¬ºÚáq*%ÊÉþÊR\x0007Ê\x000b÷>%Ú}tBÉ\x0016ª[RQ\x0001ðë»ÄÑ'>KJq!\x000c³\x0004n¨*\x001cPv8
/`yK	O6(Jªtv©R'\x0014´PÐ\x000fUJÕd¼åæ\x000eÏ\x0011ªì)±PêÝ	¥ÛåÓýË7ÕI!rÐ\x0019\x001fðê-µtêCvñ ñ rä\x001d%\x000c·|óÞr«é¥Æ\x001eL¦=z¦ÿèå\x0017)\x0008zï¸¤t\x000bÅÓ}PJ4R¢_P²doÇÖÎë²v©x\x001dÓÔ7 1M}\x00032	ÇE\x0003Q©äÑË\x001aû\x0001Ñ&b©
]\x001fi¡L?T4vùÏ¨\x000erÐ=Bq\x0011á\x0016\x0008\x001e2ø­î¿\x0018·SÝñ\x0005\x000eZÍ£Ü\x000f¨)úJåÄì¨\x0010ØU\x0006?{|D{ü\x0002'«îà^³ÙÍ±\x0005Éak) \x0015Zú
[Êu³éM±áÈ#î¬&1\x0010ÙBé\x0017`üån¶JMÄ\x001f\x0018c³¥§p¼	åQ`Q£\x0002¿ÖYAò\x0018lØä\x0018(
{m\x001e\x0019üÒÊz\x000bX\x0014Á¬\x001e\x0003©\x000eES6i\x0014d2e6-¨kØÜ /Y\x0016B'(ìTÄ½t\x0001êFóP£y\x0018C+cç°çg 4_¤6{|\x0018Ck¨\x001f;¢nª¿\x0013z/{\x001cÃb[¼u³æ\x0018±càø\x0018\x0018é ØJ*Y¼m÷¢ÕMIQë1õáÜÔïVbÓ¢,7¾¢\x00193{Â\x001e\x000b-\\x0018+ÍP0ÏCÐzêÖµ	®z0D¸º]u\x0007\<\x0001Ü5@ó
\x001c^^Òd\x0016ûÛtÃ©\x0016N
Â\x0000O\x001aéJÇAJE¿Ø\x0017¨\x001f®õBÔ\x001bâJ^\x0003TÇe-uÛVU·ÓCÓª¼¤Ò«ÔÒàÛÏÚ¢\x000c±A£F$\x000cê\x0011Í¦ÞXEÍ$±7t\x0019L2«0èsþ»¶\x0019D¼®Vs]\x0006J\x0013\x001d\x000bá(KÁÅ%ÙÄª¥¹3\x0003åS6r\x0015häáFîÔûÆØRãi\x0016g2bÖuC>=\x0003câä2n½g©ßj²\x0017\x0004º4eh³\x0011§^%N]\x0006\x000bàtkêoÊ#ÔÎ^M\x001a\x001aÒ°R¢´¶ô)c)k¿4nm\x0014\x0014\x001aÂº\x001d:\x0017Å\x0011\x0008jKCÈæÎ±Ô4Ô¬Ú¤´%5ºÒ\x001frqó i]{§¾K<°ú\x001fþÐK¤ôx X¨s±FIuKªÿ¼¤ÐÂ4ú³íB\x0007\x0017Ê+ÄÉÕíÝÏ\x0007\x001d¡2kL	n¥íæør\x000b3YN®Î/^\x001dì\x000c\x000cøTLÆN(ç\é?¨¢$p$Ë±\x000eØ\x0000%[(Ù
å%Æ\x0013T¼çå´ï\x0008Å)[ `!hÕ\x0005åt#)§»%e±7G<
/\x0014o®å\x0016í}PF5PFuC	ÇV\x0019så³µs8$¡fe\x0006½P^ú\x001a
íN\x000bçA1TÇäâFÆ\x0012,Dû ª$(² BE÷G8ä\x001b\x0017Di+$\x0016ò:Ú
åû7T*ºà1\x001cî»\x0011ª43^\x001a\x0011Ö	\x0015Z1n1á \x0012ÏsÁ:lÅóXÊVÔÒä\x001e()Z%~ï¤Ò8¶¡$ÅéLSË¥qA	HÊ¼êJ\x0010MNuw|öðøÛ\x0001=u,\x0016sL9Ý£\x0004zÔâ²gW×92?(³UÏm­Nìs½KÌ¶W\x001e¼yÔptâ®ÝÝpU\x0010\x001bÚ v\x000f\Óx7»ÞBn@l\x000bªtÍ43cÓQ¥¶;*?5G6]?ËÅ¨g7màì \x001cNAF\x001eÒªêéÎ\x0011Ð
p¾ópzª°S³e¦Û¶-WUQG¸àÇà,}Ð-P¢)öæ;`úÙqL;Ï\x001e¸èå°qç\x000b\x000ba1q¬Ðå©Z{Ðt³¦R\x000f.ª÷¥;¯Ð3ÔaÐ¬©±E\x0005a¸»\x00006 ÒY\x0003G\x001b6óÙr\x001c¤m´cZ\x000e\x001b@\x000b¦<~\x0016,¢[Lºë¥SíS{\x000e@Q\x000c\x0000ð-\x0005áR¥ö¬{\x0008N6\x000b«äàÂFÓZùµè(½Ç\x000fcpV5pVÁ\x0005(làØz ù´úYÿÂ1:ÝÒé!:ì¬¢óí²¢³SÊ ,Üúá´q5\x001cþ:\x0004çÝ4NJç\x000e¤ *uMnñ\x0001ªÎ6GBÛ±#að\x0006ÌW<Ç)Ïè¯ÿ-gB×#\x000e#\x000bCt\x0016Ã®²ÈÎ³üX\x0001³Æ\x0001Cp¡\x0015]\x0018\x0013¾Ì¥ÀàJáäBÖY?\x001c´®0\x000cúÂ\x0016\x0019¦éj*¯«Ç\x000eç\Ö¹EtàK\x0004¸±ku¥\x0014äÓðÚØ¢·X£dMgê©6]²3¥\x0019\x0004\x0006Yvåòe\x0016K'ºéZïÄ\x000cz'Öpþ,¾g\x0003NºR½8"µ\x001b\x000e\x001a;a`ÌNX]þá\x0003IêÄqËSºé\sb« _\x001f]¼çðÂÆ\x001féöê \x001cÎîè¦\x000bíÂ±Åùa\x001cÉU¹D7ÂMa\x0008m·ÀYÙX1+\x0007­\x00186ê!8yêó=Çú2íI/\x000e×>\x000e'eºçL¹k!=å®¼ût÷ùóÁé#:¡Ëè\x0004.\x000fç4\x0005\x0008³^\x000f/ÎOÞ½¹x÷îð\x0000LVÒuvX\x000f\x0019Ê­åJBâ4-Í*í&³²&³rLa¥ºôm¼ØÕ¥Là~²Ð\x0011²èúòU¹Ò@É[Z\x00089w9¨É\x001cE3\x001aÈÁ`\x0012ÙB·\x001blê`ÞI7ßä¹ò>¸\x0012¥wj!~ÙM6
\x0006E²j.h\x0007YÄa'D©SËé\x001c¥^ÞÍF¢\x000cÕcõPi!´¨ÿ©f\x0000¤ã×`ÊW»`¨úÑªê0DÊÃ:Ð\x0014\x000e¸ä~\x0017ª\x0003«Z°\x000bÞG?\x0019´d0DfaêÄa¨m  ´âXÈkêGkÕ\x001cÒ\x001bÊ2G;úåRö½zplA\x000b­ÔÂÔdI#\x0001URÕ¼æNÈà\x0016*Ñ»ÑhT\x0012#:-U\x0006OC¾
å\x0008k[ÚR1V7j\x0016T©\x0005AOÃ5(ïEÉH_ÂÜ¦\x001b³®ô]ÞÇ>\x00123Á\õ\x0002¹0óu\x0000­]P=² 2^ç©&ZÊR¹"ÊÄ"¹\x0010§éGVj0$µP:ôbÃ+:\x0005¢8K5ZÝ`­¦Ü4ì{\x0010¦Ø\x0016\x0002gK>@X¨Ë\x0018@3-Úvw\x0016wZ ²i\x001cáÒ+`7Yës¨!§CNmµ1ÐKÇÓiSÂ÷[öYh\x0015G\x0018R\x001cÑé\x0000(^wn\x0017M¡§¤CB[~WÈ\Ð^S`è\x0012ÿ³Ð,\x0010j6ëñÊY¶\x0019¬rÓ\x0004
JB\x001eÑ\x0011ª\x0002\x001egßß|ws°\x001fä\x0019\x0015ÿ©¡\x001e.®Ô×ÈÅ(ÛÙó³ç\x0017g\x001d`ª\x0006S#`\x0012ø1!î«ìr\x0003Þ.Xbrñ¨\x001bL×`zPbôv\x00155×i \x0006FLµ\x0018âè¦
Ä¥ø-2­£"q\x001e_ÛÖQ6ë(Ç\x0016²l}mUîåÜ©¥\x0010x7Y³rx%i¹Ò¾Èqq\x0008Åèw7X³rt1­"	\x0006Õ"\x0016Ó4dfTd|*íL`KÏ@ÝT¶¡²£òÒEWØùæ\x0017KÝÝd®!s£ò¢ci \x00178WÚB,ÖºusùË\x000fJÙ\x0019ç&\x0015²ÅÒÅn²ÐAQ*¤QÙPÖ\x0002Û²ï«4f4FbJà@\x0004:Ñã	\x0005%aA,ïv5ö[\x001apV¯\x0006g\x001e·òÚ¤[U£ÂÔ¨
sºl|åg\x001blñ¹½L7GR\x000f\x001dI|é¤¥t\x001fx¤(\x001e¿Z|\x0007è%FÁ¨\x001a#WL\x0007ìù×\x000cg®l\x00003	7c&\sú\x0016S£?ËÕ§zÞz¬ÑcfTÑ\x000b¶V_:+-¿töÙæ\x0000Ø±\x0003À]8\x000b9'8."Z/	úÁ\£ÊÜ*«U¿Hí7HdP\x0016s\x000bXã[¸1ß¢Dÿµë'\YK»ÜÔMÖì27¶Ë4wÇg®ÛO©M^h\x00163-¦¦ä\x0017eÌiÙýd´µGîãrbçV\x0019wX4Joïo¾O\x0017ÞûW7w\x000fw\x0007Ægã¨(
FE9a%Õ¦(\x001ePmC£3Þ^=OwÞË³Wg\x0017W\x0017\x0006h\x0013ªñÔ(â:\x0010ë'<éy¨°[ñ|ç\x0007ñ.c¼ÎO®\x0011OðÔ\x000c'VK+ðd#=9(>\x001bL3é|ÎÔ\x0001J	Û×àé\x0006OOq«#\x001c?Hs¢(ÓýÚ¨Þ\x001a>hø`P|ÎqÕ\x0001./=tãð4%}\x0013jv\x001aÜ~\x0016«H~gÕÁp®u[×·J§w9þÏÅ\x0007
\x001f\x000có	Ú|ç¨\x0001pö
Jms
\x001bó«Íl4\x001a¹¥NÜ|\x000fGûþ¿Ï4Ã\x001e\x000e\x0003dÓ¬-\x0013ÔM­7\x001b¥g\x001bÕb\x0007UÅñ;\x0007:ßqëq\x0003Ok·ÚµzÔ H¾Ý\x0010\x001fx\x000eO¢ 
ÍnÛ÷q
^³ùÜèæ3¥b9úÀØ\x0012+ãñì9ã·â\x0006/J¯D­òÔ 2ÆºÁÆÕõÍÙð£g\x0003[®óî§4=9Pi÷5Þû
¾Ð,o\x0018]^íËÆòÜ\x001dùî3r£ß\x0012õ
£ë«JuGÊà¥Ó!ÊémGºó5µò"×Ê\x000f\x0001Æ\x000f
Â°B£\x001d§dÇ
ºz\x0003Úl<¦
\x0018­\x0014L\x000fÌîåÍÃíÇûñ¢åSQ°<Ía0Å¹±à`áu-¢½<»:ýú8mØì R+\x0016Ù(_\)\x0015
\x0016òÚ\x0006è*ÅlEuéî¤VwJRL'9\x0011Ä.\x0014
ÑÎ\x000cÒ¹Ò^LÂ)\x0010\x001c·¢ÕFÑù\x0006Î\x000fÂÉk/Eéf\x001fJ*¥YJ×\x001a ó®¦ónXt\x×@teD\x0011,ÕZ\x000fÐæPÑC!ñ10÷;°8÷dÇ+\x000bK	²ýt²zHµ§GÃ\x001d´7¹¯R\x0012\x001eãÍêáÉæÌÖ\x001d{¥Gæ\x0016gþp¬Ø×ñ4±s\x000bkñÆ·\x001eOMrPÚ¢\x0012d_êT;@Wµ\x001aFºªÕp\x001f\x0000\N\x0000Mt¬ÅRñ\x0008mñì ^éf­>\x0015ÖÖs~ÍÂ[Ó\x0008\x001d´\x0007\x0003F\x000få·i°\J)Kù®\x000eK	Ç\x0003t¦Q*ÒjT£ÈO\x0015&ø\x0012x\ªô\x001cÁ³í±µ+-EÕ4ÌÆs©G<ËÛ^ë	ÈQW\x0000»%\x0003á¹Óü4 Jr£öKÍÁ\x0007è|»¶~ÔÅ+ewéI\x001a)¾/ÚùmÂ\x000b/ Ã 3\x0000¢äF¨©	\x0005\x0014é-Í\èÃóùízZÛ¨
Ø`¼½ùüåöñáã.¸2Ëf½ýörïÖ°»¨oÏÞ½?¿¾:\x000ed\x001b Û
T"Ü8\x001aÊ<0\x0002@D³á½@Õkµ^«\x0003IÅw\x0007\x0004J\x0015Ø\x0011G_Y-º\x000eH7\x0012Ò½\x00122Á\x0006¬Aco,!YæÏJtº\Cäº×,*®\x000cä©Ð\x001a\x000cGGä¬\x0005f/P¥ï#\x0010«ûã"r\x000e/ñ(\x0007C´.c±gÉ\x0005Ý4xL¯x°^w\x0010ÎÞÊÝ#£õf"1+Dë%rÍv½{ÚørçÄ¾ ¹\#h(Õ¢aÖi»H5DªhJh6²qè\x0010§ZYÁy7P³h®{Ñå: c\x0004\x0017ÂéR\x0008\x0017E¸V3FU^Um sMÄò1ÃÖ\x001fÜ_iÒI$«G¿d<|7+u½Ç»«\x0012\x001c0³7ù^ *×\x000f8Ù¯c\x001bI~¾MC´IYË=ýdGZÝ(»£1\x0013\x0000\x001a¡\x0010TÚrÂ¬¥M/\x0012´Rn)A± Ø$ê\x0002ÑÃãÂµBª\x001e)Ñ×ÝD¦Ì$ð\x001ff÷¥ÙZ¥-Ûó/û\x0015\x0000²pE\x0000Jg.1s({|ë\x001aùnËÏMt\x0000øIM©i~5Oh÷QèÞGØ\x001a\x000b*¸ÛzPS\x0016~ÕÖu")Ù¬Ý«¦¦°V¼CIÚHVOµ¸+¤RÚVª[oGÕ\x0008¥.\x001be¦v j¥©Uºuhu·õÇI©<ûÛòkÂ	Ý\\x0012¹R#©Ö¥Uý>­0Ü\x000e\x001a0Ñ\x000eV¥\x0014R¬tûil2½¶
|\x0019¢±P¾\x001a)Q
`õNòíÂùÞCÕh9ì(iYó\x0007@Ï&·v#©\x0016©×oÃF\x001ci\x0014ülÆ·\x0010­\x0003Ò¢½\x001cÞ
Æ$\x0017!xª÷
Ò6-J®<oºLB/\x0012¶
åÒ\x001b8\x0015Y\x0005HWRwåìîß¤\x001aÍ­U¯æÆú7Éé×\x001c\x0007i¦ ç¬eA/n®lZ÷ÞÙ°ð+§ µÇHHÛtb0g-R»pº{á4ð<âÔ4Q\x0013\x0012O@Ã²\x0012	Z$èG2\]\x0019#M­Áæ\x001cÂôböt\x001fÌ<¾ÑÚwkI!J¥\x0014ÔÆ¤ääÚµ.nïHºû¯EÑÛ¦\x000cDáÙèÕ¶
Ú\x0016tG´´\x000blÛp¼)-0%ê\x000c³ù½HºY5üµ\x0013Éºf\x0006Fhñ?\x0017NÇ\x001fL+%Ó-%ã¹+\x000e\x0013ÜÞ3\x0008´µLíE²­l·â,e\x0000\x000ek	ÅÍ
ã~\x001f¾&I-ÚØ(öúU^Ç\\x0001¥×Æù.y?\x0005Wºº(½kÑ5Z8Ñ)¨é\x0014\x000cÓñ\x00014Óô"\x001d«ñVjãtÐÈ\x000eÆeGÚsºC\x0005Ì° nòúá&g\x0013á\x001f#¿<=°ðÂrW¨èó-eùôÓU½u¢×IGjL\x000bÏ®^¤ÓE³®pn'>\x001f-\x001cÇç_ß>þz(eÚ\x0000ÛCQÎföàøúüúÛùP\x0019F50ª\x000fÆ\x0012¡Ë3ó4£\x00122
¤ìÑdt§d@qnÉ
ªòÌ"caÜÌ\x0012vÒ4¢Ñ¢1ªDÍ4EwMU¯õÁTÏÕX6«û`´fYu\x0016LIç4~¦Ù;ilCc;\x0017JA¦Ä§¹=%\x0018?{aê£1Í¶1ÛF\x0012	<P
it	WúYæM'M#\x001bÓ)\x001b-9Àìd©'\x0001à¼L1{
ì	
Lè\x0014
pÖ^\x0013Ýã."Ãì«Æ6¢±¢Qû á[\x0005NÓlË¬í¤idc;e#m\x0019>\x0015¯Ý¹¿\x0010ÖMqê*\x0014×\x0008Æu
&¢Ð­-nV~'1
¦\x0007ÀÝÀM'M#\x0018×)\x0018a¦Ç?ûH`M\x000fçÙÅ-¼N
ûF6¾W6%
\x0001Q.\x001eãwci×É¥
\x001fG\x0012\x001e\x001f!±Áó\x0015$Þ¸\x0005&ÀÛWÎ.²4¾¡ñ»tGÁÑ\x0014\x000f1Þ¹¡³Þ@]4R4:85éÚ4ª<>\x0006Y¦ãÏ¯fÄá¨Ü©eZªx\x0008ê\x0006ÈÑý;ÒNUF\x0012.Z¶&{\x0002!ÈÌ2XÞ<KÞßÁ^¯fk4;ÆÝ\x0004\x001cp\x000b_9õµ^\x001c¬Úæj47&¸i#JM³Ô \x0004ÿ\x0016Z÷³ùÍ±ùpêB\x0011vÌV¤¶8\x0008¤\x001b-Ôha\x0010Íó;\x000eÍ0*×H³iI«t)5¥KuÃ´s\x001b§ÿ:È\x001bø8làä0$Gc\x000f¤c¿\x001fRÖäz8h$\x0007zV¨\x0012»ðu®Kt@-äu\x000fÀù\x0006Î\x000fÂEãÈ±U¯¦æ\x0007e=BÀÉªL\x0004µ)tNàµè¢ºãÀJIÿ\x0000½Øû¦Î7Dú1U"°ªäëSñh°¦T\x0013,Nî+iÃ_àd`¯'Õ:d_Ójãmb\x0013[\x0015*@¶zìöq6\x001f0§Ù\x000c;ÎAÖ¹föì1D\x0007-\x001d\x000cÒE×Fu(¯i~zß3³,¨NºÜ¨¹òGä4×íÿþÏÿ}öýoû×SÙâÅKµ\x0004y¢\x001b\x0007ù43=ÿËQ*´\x0019ªÇØ2,þHz^gÝÇ\x0003
\x000ftóD-Ëã[@s»rºôà\x000féâ©Ò{d®AîãÁÙò$xkµYëkQÚÝ[7S]]<®ë:ÎâeRÙK\x001dÀB¶A'OhxB·||i\x0004-Ì$ÒØÛÌ{;uñT)õ²\x0013w\>g\x0013	ÊWÅ¥k]Íºp¤h+]ð:y|	=Gj^p\x0010\x0010¾Y9S\x001fOhyº×+@ñéÑÿ£	zr*`¥úª'F\x0004*Ý\x0004o ÁÝç8\x0014\x0004©#-áÌ"½}8Ê58ÊuËÇq\x001c\x001cK¨¨ÀkJæ\x0011ó¾[]<­zýúÙë©Ë¨dùèRL(×\x001dw	ÍñÐ}¾¼ÁdÙü\x000cUnÒZp5ºPë64´\x001b\x001az74vÔâ\x0005Ã©Riµ¸2%ÈuÒ©¡d]\x000cu\:¡.\x0015NùpRg4ï'×ÇÓîfÛ»1\x0006?aÊ\x0005ð¤Q~3\x0005}ûpZÛ%ûWzJÇ±\x000e-§J"¹îtU\x0017\x0000\x0004*\x0017\x001emÈÏBÝ\¦;i3\x001fvÚ\x0005\x0014ÚÝ\x001cúw3O=AÃ*Èjî\x0015Ü*o£Z ©\x0005Ç\x0005TfüâÞ´¦Dáí]@²ñìõ±O\x001dÝ9Tôé¢«§ô\x000f=ïrÙ\x0007ä[ Þ-úG0\x0010ì!e·\x0011\åp(Õò¨~\x001eÉo+é®Á<%±IÍÀt\x0001évÅtÿÙ°EÉ´ \x0000-ÌHè\x0002F)*èV2pv¬&Ìócö\x0011µXçÒ«ö¡ºï\x0018¨éÐk9ñ°IJjÝ¹V@®[@Z *L@ØíÎ-@\x000b£\x0016\x0000Ý\x0010~¨BøXúöÓÛ\x0003U¨ÞÄÛ µ1ràø\x0005\x0013_ç3³³äØ\úöÍûó«U¨a·áz¨\x001b®÷Ñ\x0019ÍnSÛßiÁjÉÁBär®Ê£ÀD\x00119FgËÈ\x0001&J8ßÙù-dÎ6tvÎò£jeõÔ\x0018raÖÝ\x00080ß}¸ûÜî<üàÏ±ù|zù«ÞÚâvüw]üüËÍçÏ\x0005ðîöáá\x0000|4#ª/\x000e°ÚéEÒ4QWoÏÞ½+\x0017çWW\x001dºFÔÃÞòc²õÀ¥¿ÎLí?±Lë\x0010Mh\x0011ãÎ-Ö{®-sÀiÜNØíRt5¢\x001bG\x0004¶î\x0016ë\x0015!ª©ªÚ\x0018jÄ0\x0018<Oý´F¡o\x0010Ë«¡mB­Bíq\x0019?/Ñ5SÓ9J½s½¶2ÂuÍyÃ\x0007&è©­ FÖònô+Ô¬VZ6\x0007F\x000e½\x0005éÄü4áajwÐdb¯\x0003l\x001c>/qßñ3±ºâG\x0000~y¾Ìz!J¹3v\x0004}ËØÇw_n~8)áË]ÜoÙÍJ[¦ fæe]¼{ö¢\x0003)4H¡\x001b)".\x0003¹³VDR'aÝ¼!x/S=\x0002\x000eKú$ÇTpR´a&¾?X;¿£w3Éô2y¬&9anq>¶¨8ëf\x001e{/\x0012ø\x001a	|?â\x0001V;Î»±S\x001bR;Ïqée2²fâlÌ\x000e&i8üdu(KWòx£\x000eÅ{z¦Ë\x00162»Öq&ey NÏvY#Xl@@ª~ûëeò¶fâ¼¶\x001e¦Òe\x0003{xJKLENf>M§©jÙTî
N²[n¼Î¨:ÙåµrVüÛÍdUÃdU7©¡ÊÙ+Ñn\x0007;%­ÝäÒ¶²½
bê¨g¢J§ËAP\x0018bçÕöÝPA´¼[k\x0006\x001cÍ«\x0007åõÛð;GZ;°AÅº\x001bt2ySzí\x0018SôsBAZ»xUª@bþ\x001dåKé&Ê:îøÒÖ\®ÖP
BËÔkã
¬6Mà	ÓqC¾jõÑS¦qVéõVB< øZ\x0005%Yo\x0006] æ%eÝP¾Ñåøk/©T\x0019¬\x001eÀ\x0015¨ÕGOµÊ\ukó\x0008UªïSh Li¿³ðDÖ\x000b\x0015\x001aï@^÷ \x0008c§eÃ\x0013B%{>è½\x0013J·îîö\x000füX­\x001cM¬§\x00055Ï¨ëe²-íf\x0012ñúJñ|3åã
(¡\x00141Ï,íò-TÿêùRÝ¦\x0014Í\x001cã$\x0014\x0013f]oº|ëû^\x000b\x0013\x0017O²Ã}\x0002¨b\x000bcüzAvõBÿ\x0002ÅÁ\x0007lð$sèZthÿf
P \x001bIì\x0014\x0005Ó
\x0000wÆ
Í³k×\x000eT#&P\x0003b\x00124÷,\x0015JQ\x0012°n­}\x0001Ý\x0018bÐ½8"\x0005ød´(Ée¶Omïf
-S·!¶Ô3Úòó¹Ô®@­ÕOU­yb2ÝÖEúrõ4Ñ\x001b¦¹ÒrSÇ¸ k­\x000bøÆ9\x0000ßí\x001c`«ujÿjâ4HOr\x0001¼Ñ³2ÀãLÑ\x0010|×Î\x0012î«i;½º¹»?p£²ÀÊ	æÒ%§JÑæ¢¯ùêìâò8\x0010Ô@Ð\x000b\x0014ýqÍ@Åùu{\x001f/å}ö\x0002Ù\x001aÈö\x0002Å¿Ö<TrR(\x000bÓ{y|Íã»yt%à\x00021ÙÀ\x0013eÍ¼p'OU/!ÜWÚ>\x0002\x0014O<-XôwùNîË9SóÌ«^ fKËî=4HBñB®9rQ´ÑBê^/Q³§e÷¦Vc)½ä5Åw8}Æ¨yu/Q³©e÷®À\x0005Éà]\x001eªC2hD´dmûm-»÷µ(Í!zq\x0014²°P4\x000f+è$RÍÆV½\x001bÛaÚ~öH¢W­Z$Ò¥a¡çÈö\x0012µÊºwgc;ß\x0005Í\x0017^[.¼FÏàz­zw¶Ã×JÊ#\x000e»mXYüH=1?F$U¦ÜH5Í4y÷øûÍ¡.Ü)Î¬¹ÂG\x0019g\x000bÿAÏr\x000bß]ÿÛÙÁþÛ¨\x001a ?JÕ¤+¢#É\x001b¸AÌ.%½@Ð\x0002A¿\x0014·ðÇ²\x0019\x001a5¤¸9 v³Z^¢vÑdÿªYQZ\x00039ÊÓ£J\x0017.\x001dv7öQ"!wGÊËz¤üÉ=¦÷Ü}>Dêïù-~u©¹7[­}ryrvñ®Ì5dn\x000ck>2+ï²fê\x000f\x001e\x001aáwrUÕ²®þëâ2Óë-[Ý8^H\x001bæç~2ÓA²rl­9åêïÒ¼À/6çï\x0004s
\x001b\x0003s%S\x001c×\x001auÙ2PÕ.\x000fÔè%k6\x001bÛd\x000e(ßÎ\x0006E\x0012³ëÂK©Z\>Ô\>qy6ÌNxîíb%\x0007\x000e¿\x0008wÉêÇRØ!4\x001fJ~ÜA)ZhÉhe:ÑT³Í\x0001êDÃ\x00109PêÊ9ÜèÎ\x0018=Ï/íAËÖZUàâ+5\x000eÝ|È1v\åç°©'í}Ç³ÈÝ¼»`t\x001f=?ÊSµÎ<UPú0\x000f\x00065)Å.n~N\x001br\\x001eìü¼Ìæ\x0018OH<U]K¨Ê\x000e\x001fOÞ~º{¸¿ýr ¦3ªÉ4ò£'ä¦×9ËÔ/\x00052Þ¾¹¸º<«ªo	ÕÌ½\x001e.c9-CÅe¤IÁÁsIZ(*éç2
\x0019áÒ¼ti¬\x0010Ì5Ï|ïç²
\x001dàÂè@\x001eN*Ïy«kí\x0017n\x0013Ç±l\x001e|RM®1i¨òón¾ûºáû\x001f\x000f(\x0006¾\x0017\x0005Í=H~"&2\x000fM2ËóoÎ_]¼FÝðÍÙåÙËSuÖª¬¶E\x000fLÀa,\x0012ù¼ôÜ0OI^5\x001eÃpÕt
Ã~8\x0013K/Ú^	Ná\x0003É©I^5£Úûád®×ZÿâR5àßÞÜßÿñ\x0003ÁFoÂ\x0014ãçÜh$Kß<·g\x0008Û·gçGét}ûÀþ¶bNãôË\x0012¥q¦HSZ¦\x001a¹'U¸®zD:oÇè¢Fì*\x000eÊ¸}c\x001d°ÝÄ5l¦ôO>ÃæCùüî\x000bUì?<þv¤×5Ç\x0016\x0018!8ìK±i':=¿xO%ûW×I%ûßßüpóùËÃmùaÊ&LJ®Î²\x0016_M9ô'oî>ß\x001eÔr\x001a»O\x0001½ÀR\x0017
²<ÁÍk"ÐËxsñî\x001c\x0015]î`¾ï@ÕÓ¯DÕÎ¥*\x001a+¾^è<æ¡uRZ.8´b1±\x001fsßý§üøão¾ËiÀüûüÓãÃÛ/w\x001f¿ÂäD\x0011­c¤øá./gÚWØ8-r`JUtû³\x0011ÑÒÿC¼°{øâ"­Ôó7×WÏÎß_¼^ÞS
\x0008\x0017üê$Q\x0016/´	%.T®¦\x0016'\x0010
gt¬A
¿úP(\x0002¥â¨c4iu\x0012J\x0019;×òóï\x001f?}ù+=C¤ÇO?~üt\x0010CÊ¸I|Æ\x0000\x0019°Õ\x001dfsÀÛ~Äp¢<ý\x0013ÆÕ¯ßt1ÄÍe»\x0018DH\x0013CtÒsUÂ¹MÌ°\x0016!þs¾\x0013\x0001R£-´n+\x0007ö8q\x0017W#8«G\x0018~ÿ"ï®âÙ§Çû\x000cÊÅÍ\x0019H\x000cxYOïø`±V\x0016ö­\x001c½¹¾<ëbÈKÑÃ RúG\x0003¾e\x0006ã
\x001c0{f\x0015\x0003ê.üê°éBGÃó¤RÐEaØ\x0010tD{ BÎ³\x0010\x0012%!âýVe\x0008gÝZøÏÉ¾åÀ¼]ëbáN<$)1\x0007!hKXW:\x000e\x000cCDå_=\x0010Ñá\x0019Bê@I
\x0010¯®´'\x001c[	\x0011÷3~õ,Å1ØY\x0010:\x001d@J\x0011&Aðü«a¸ñ«K\x0010¹0\x0004\x0005!\x001c\x0006A%\x0008iV\x001e\x000e\x000cj¨ÎÃ¡s\x001f[Ô\x0012NÐ\x0013?ä,ü¤%@¯Ü\x0012!_]Hyí¼/³Ã\x0013·7¼\x001cvåÀg!üêg\x000b*\x000c
 CIð¾´víjÄ­¤út¶
ñl 
¤!5¤!LàDÿaøÏ©>5åEªèKBÀzeÚ¬¥¢·v!¢RFCç\x0017\x0003dFÔÆ¤¥,¶Á[\x0007\x0011áU¯òlÁ±-\x001aëk«\x0003C¬\x0015DTPªSIAj\x0018´çcaµ!O7^¥ä:\x0008é¾cáÿ?êÞ-9#IÐÝ
6Ð°p»Õ\x0013D¡$\x0006IYÏyA\x0012º
6\x0010Y\x0005ÕÕýÔÛè×y:õ~vP;éð\x000c÷ø#þLüHÏÄi¬[*
FI<Ã/áá\x0017\x001dª\x000b/Á\x0007oäuÉÈÇ@»¡\x0006»îDd¨o¶¤\x0017>rñ¦+D¬\x0019É¨T3~ù×¿ÀL\x0019²ò÷Ñ\x001f¯>}üò§¯?Ý>|9\x0019Ö\x0015Dá\x0003É\x0014×ië%2`Óx2_½yýþû\x000fß\^?}\x001a`($¤?ÖÂËOª'4\x0014ù¤éÃX\x000b90L<
µWÀÀÿüÛ§Ïú±BQ\x0001ÔÕíÙ?}¢«á\x0013'5ÓìQbÉÅ³r\x0015\f/âÚË\x0010³\]½ø~º\x0019®a)¶Ë¯f	Tù_íx¶¦ÎÅ)f\x0014ø\x001b9dÇu(õ
°\x0016¥È¢Æ|åÒÌã:·\x0016\x0019Å\x001dR\x0008x-)W$0,i8)ÃØ\x001d0å?\x0004Ö\x0000Ó\x001aÄ
%þrïG\x0004³ã#ID¼\x0012ÆSôQÁr\x001f©ï­ÎY\x001fø¢ä"ªaþôë¿ý\x0014¡¿#\Ý~>ûvÊ§|ù|ò&\x000fü¡\x001c8ÂUîÕOÍa=FÃywöíuyÿÈ$É\x0011¨Ig-Åi\x001e\x0001Y.'¤Y`\x001c,G*Ù\x0005Äwõ@\x0014XP8·\x0015\x0008¨\x000bº\x0002\x0005{|U@\x0012>¯\x0004Bz°á<\x0010Í[æ`Á¤"\x0003E³ëI(½ZB\x0008nÚîG@Q&[\x0002Ðvè
â>	¿þX\x000fD%Í\x000c\x0002ÏJ\x0004DIF÷\x0001q»\x001eÈ×Ù{\x0004ó9óxË\x000e+ñz_?~ùkº\x001b\x0010åÉO\x001fï§¾v2?\x0014`Uë¼8	ëÏ\x000f\x0017\x001b\x000e#î\x0015\x0008å×°¦YNÚ\x0015±\x0004q
h`#\x0003\x0007»+\x0018hb%»íä\x0002§Ì:EÖ!ðXNB|þ×¯ö×ÔkÏûO\x000f7w÷÷·§u9FÃ\x0007Ãftu¿¢3~\x001az:	#øñ¤¾s}ñòêê±)¾#
_GW¢isá$â%¹\x0013ÇÇ "Gq¯
Uø· \x0015VÞß\x0002
ß\x0010\x000b(åÛÒ\x001f¿\x0001\x0014\x001a @¬=¶Q\x0012Ï9·®6IæD	·\x0014=¶¿
]ûë:d¢8@\x0013ÛÐ|8Y*ùèê¨B)&þX+\x0015_ý\x001eZ´^DBõ\x001cÕ\x0011Û¤Äø7ûo.þ­?&ä/¾Þ¼ýãí§»ÓnØ9¤øpÒâüM%"Õ\x000ftìþÞ]|¸z}ùÝeÀ×@ñÑ@7gÊü6\x000c.[¶»q!xZÁôçø¯þ.ñÛðï¦Cüõ\x001e_éï×ré?\x0005åBê\x0008Ê\x0007C|\x0005*Ò»Â\x0004h;ÄÑûpM/°ôÐGWÿG¹Ì¿E\x0008ÿs*t,ßþ¸º9{uópóõÛ»Û'\x001dÓy=Õ4#qjQ0\x001eùì³W\x0017×\x0017\x001f¾½¼~yyxB?\x0001ôãÍt£bÂú>ì¨©6ð
\x001cÚ%3»[\x000ePIé'Ã;I]ý×þø
w*ß|ñéá§ÛO\x001fÏî©ÚåëÉÏåZ)ùvC×ð`\x0005\x0013$§wBzñæúËë7¯Ï®¨äåÃã±\x0001ú\x0001Ðo\x0001Ä\x0005Àðla\x0000\x000cZ@3Mó­ÅzÔ7E#tvùÓó¥/©ù¦0L&>CÇw\x0002æ\x00010o\x0000LÑ\x0007@ÛøöáÕNaÁCÐâ¹Ô½åªÈwåY,v\x0002Ú\x0001Ðj\x0001i9=¿ÒdÞÑéÈ
 \x001eÝ\x001dÕv UKÐÀ´·SöA4\x0004DC0\x001cWÈ¬\x0006ÌîÐD0\x0001\x0016µ£jÄ\x001f(îxø|ö¹¸4*¤¾¼ùzÑZãù¡	\x0001óùô½Í\x001aõéÈý@1Èõ»³wÅ§]]^|x\x001a\x0011\x0006DØ\x0018è\x0001¬ B¶¶\x000eü\x0018«©öÁ\x001f=ÈmÄ\x0001\x0012õTÑà§oôt
\x000cYþ\x0005iv3ÚÑþ6\x0005é\x0006H·E8í\x0003#AFé¿÷À>¦°ûDúÑo`ÌuX21:©lò6òÛF\x0011cØË\x0018\x0006Æ°1Ú©Lp#b;öÎEGîe\x0003c\x001a\x0018Ó\x0016FCqae4\x001cã\x0014Hß \x0001wBÁB
\x0016\x0012\x0003r\x0019\x001b\x001aª.¯ÓÞÚ1Â^AÁú-ÖÇG¾¾a	KxÃ/è¬Ù\x0011öB\x000e\x001d6iöÔEÖ't\x0016¿õÔe¿
Ñ°»6âj¦+0Wýák¹]\x0015¯ýï§ßN½¦%Ñ;®\x0005I|¦¶#o]Èþðn\x0005ôÍ#£Ð{>ìùPË\x0017[:'8ÙEèÄÁ/|T=§Ç³=ÕâeäÜukj³sË^#Wà®¤ã\x000b}\x001d·Dd§áL!H\x0005\x00032´ «à¼
WMK@ö4íé¬.ÄúY½Ï\x0014ÐNh´\x0002¶¢µ	\x000f[Ñ\æhTÈ®\W\x001cÓEÉ\x000bAØ	ç{8¯\x000b^Ò\x000fÓ¨Èì	\Û\x0010½.ötQIç[E_ùçU]=$ù®&m=rµ+\x0010\x000eÖdêà?,Jüîáæ¯¾|9~${E'¨!¼¾M\x0016{Xzhªd[âw×\x0017?¼yÿþD*²!º\x0001Ñi\x0011i\x0006ç@R¹Â{®E©\x0008 ê½~@ôj)K(\x0017Ò^ð\x001a®º\x0010"e9zrÞ\x0018\x0007Ä¨FDÎ
 :Jo\x0000qkÑïþÌy\x0000Ìj@\x001b9Ïk7b\x0002©@O¢qv'"BØ¦­GtII!{~\x0002,NC*ÎÐ¹¼\x0017Ñ\x000eVhÏ«:GhÕ3ôôÃ;TÅø#\x000f\ÌöÁ\x0003¯ª \x000ctKª¶\x0010êð	\x0012\x001fJð²¨$gOÔ\x000f60ÛY\x0015\x0018uÄU.ÚôÉBcÝ5y\x001fë±\x000eËÒ(jU<o:/\ò:\x0004ö¨OI\x0016z²ð\x001b ûÉ`&\x001aw¸®ÑFa3fÜ¾¹9­\x0002@Y6®X6¦Ns6¶vYlpûæâq\x0015hx0à\x000eÏÐbµÌ\x0019U[#\x0002\x001b=
Iç+WÑá@Jº\x0018¤)^$\x0001*\x001ez~p8»ÿ(ñìgõÂCNö"\x0015¹VáI·aðøsÃ*:?Ðy-]]±:=\x0018nò²Vuóc\x0008>,_\x0017\x0007¼¨Å\x00133g¬ì+tV2åÞ\x001cß\x001dty ËJºäX/¬¡ý«Xñ,×=Ñö­'\x000fÜÑS\	Bk\x0015h1vwÏþp{ÚÞÙlTÒ\îº1\x00143èä\x00153Îj²¾yóòÝÙ\x001f.O;\x0006K\x0003XZ\x000fF»Ù¦ø\x0002F[ªK
nzK``Í¬Zv=\x0018b\x000f¨XUW¾[çä¨\x0005%\x0006Ço
+ÁpL\x0003|3ÅµàO?ÿ½ýröþáî¯§+Ü< ¡\x0016ýÉµ}Ñ1MZ&·\x001f`^GûÍõwïÊÿ^¾?{ýr(x\x0008ÃôÔÑ\x0011Ö\x001fü®Áðßÿù_o>¦\x001c«ÃobØþôõîþÐÀhë`§<Í\x00140è·üs¦¸Ø45ýþÃË«Ë6á¬°=\x001eëÀl\x000ffu`ÖSQ\x0008!`½¡¡­:L­*p\x0013ïÑ¼\x000eÍ ]ý+Z¨\x0005õ\x0005Í[\x0011Z\x001bÿ¸
-öhQæk3ú²w\x0013ZùGV2»\x000b,÷`Y\x0007æbÝàNÓôÙ!`ùÞ3kµa[Ð`T\x0001\x000exälÍ3Kò1\x000fuQ:0çdVnêEfåjõ±\x0004¾%þ=D9à©UvÚÇàk)\x000bZ\x0013¨lá³\x0003U¹T½.Ao}DêdUHV+\x0010ëìlb
ÓûNA¢1ÕÔ2þz$; ÙÕHÆÔ½\x001a«\x001fGªm@fò\x001063ùÉ¯e*}J!\x0015¦Xð¦Vk¤Ú;\x0010¦í_.\x000eHq5\x0012Mï\x000b,&Ì¾&ïÜf¦áÃê\x0013NõÕñLLÓ.LôÄL~óqÂáãê\x0013nSÂB¨ _Ä´ù4ápÂqõ	§§Ó<®<eÆ]\x0015SÌIÌ/\x0017úÀ¦þ eW¾½½ýr÷åìíÍÃT,ù\x0018/¡LÝ
Ï­¤\x0011´ß°\x001aNßD2\x000cåº|ÿòýÙÛëG\x000b&;Dì\x0011Q\x0018j\x0005!àuZXà(#>!\x0016åw#Ú\x001eÑj\x0011iY5ª&\x0005¨\x0003É©.&r\x0013ÌûÙèzD§FLb÷M.ìÔâY>4Eì\x0015ÑÇý\x001fÚ÷^Hg\x0018êct\x0011¢OAÂnÂÐ\x0013\x00065a9ÎWÄ¢ÇÓ2ÈÎ\x0013è
s7aì	£F\x001a%\x0016"OÆÀÚ¨ÅBtq7bê\x0011^Y\x00025Ú¢YÉÉwnv æ\x001e1k\x0011M²Sëô=Õ\x0015\x0011"Åò¡÷K\x0011Ì`¸^Pw¾\x0016F©³¤³h9\x0016fìe\x001c,7¨M7øØNcâý¾\x0008Å0
"îG\x001cÌ"¨íâ4ÃFÄèå4;mbt»\x0019\x0007«\x0003j³\x0003PKL¦ã8ñé8Ro\x0005\x001fGØ­1`dóyw$Ûêóõ§²\ø­xBWÓKåTÒê7¶?Ïàfâ_n\x001fF3I?P
f±-§©
\x001a2øÃ»g|\x001bdj=/¨¡\x0018­vøÇ\x0016y\x0013÷ôp\x000c\x001a¶|ülêÊÍ"Ò)\x0003[c\x000c°¸ð\x0019÷º\x001foÆ@èF+N´øÅg¦¤M³òÐ`²Òå£¨Üå~zäí¯¾{8uWp4ôÂfNþ$\x000eÔL2Yr,6,»gW¯Þ¾|l\x0005u=\x001ajÐh\x001f®AN3úóÌ\x000b4SGÒ\x000bWAf{2«"\x000b©nNÉtÊ8v44ÜÈL>¼\x0004l#s=S$¶\x001bH=jffÐp\x001fïÑ¼\x000e-Ô5J\x0005-¦:Ð\x0002²Ôò\x0001T,hÈbâ\x001da6×\x0004h ~t&[ºO)Ðb\x0016UhXßO¦f$£í£WÃRØ¥@K=ZR¡9OY¡	­ÄØPÀ\x0017OÇhÉî;j¹GË*4	54\x0014%³Ô\x001a?Ê:*ÉºXÌ­Ñ ÑÛI`-\x0000_\x000b`¦·\x0013±\x001dÖï\x001a®@å\x000bB\x0008\x0012ÒZÏi|uas\x0000Ì\x0006hw±
¾\x0000TÎÖÕL»\x00142\x0019±ÆFÓ*\x001bâ.ó\x00017\x0000; mC¬	&ð

zv
,·â¾ó6ø\x0003P9àx?+}SÃ\ä\x0006Qä\x0006Ké,\x0005Ûà\x0010@å\x0011¦¹NÕî/Y'Ö\x0015¹\x0005ñ£é0\x0008g\x001bÛà\x0012@å\x0013\x0002ÍUª&ÄÐÂra\x0013oÛexað	 r
ôÄÏ¯©N\x00133ì\x0014RÀK¤mp
 ò
´µ\x0003òß(zôÂ]Ù\x000e3|·±
^\x0001TnÁÛ:Ô6fÈê´Â&o°&áÒÕf=\x001b\x000e~\x0001U~¡¸t	v©7]\x0016º¦\x000bv_\x000c_@_°4Ak\x0012\x001bå,¦íP$È©\x0012÷æ]&\x0004Ç+Ê-Ðû¢MlàXlMh»\x000c/\x000e\x0017Uwu\x0010ëaY\x001bäÆ\x0006ûÂ#\x001c\x001bª¡n5$6 ¿:±ÅfÜÌ¾¨\x0012\x0007\x0003*\x0003bµÂVÁ¦]Ë\x000c¶3rË?þtd?~R}ÓZFOlá ·ÄÏ´tÁßç\x0014ò?\x001fáý¬º,äsz=ËUoòåªvEoGIéÕ6+o\x000cARñE\x000f¸@¡Ü\x0018Z
q\x000b\x000f\x001a\x001bÃ1aV\x0012\x000cür:Eç\x0012eÆZt¾°|à£\x000f|£±vàêÖïrþ|Û=½Ëù³;ë_ð¾¨ÌJ®¯»\x0005¦@FV\x000fK"mÝØw{wûQ\x0002÷Ë\x0011Ü/¿\x0001¸G	Â]ðþæìýíÃÃTwx*éê*Â£*£\³×\x001e%Õja9à¼8{y}MõO#b\x001b\x0010Û»=¦O\x0011¥ö\x000fýÒëÑöv\x0003£å2\x001fJÉI.ÞÖ¸¶`ñ¹TÉèzF·I|¹ ýÂ5ni\x0017tc|\x0006Fß3z=£·T¼^k4¢dþ½$*Àe\6Ó\x001aÆÐ3mr¬\x001eºtrÌûU&õi\x0003b\\x0014]Ûj\x0019·sÅ4es7bî\x0011ó/mh\x0002È¤14)µÚJ	¨¤V\x0014]:£Ù\x0004\x0019Y\x0011é±¢ÖÖ¹Ýß\x001a\x0006ó\x0008[ìcVÊ\x0010¤ØoZÌ]	\x001fyJÑ\x0000\x000ev\x0007¶\x0018ºQ>5ðÙ
¸M~÷qA©aV'.\x001a
>Ô\x001ePb´ÌèàûqÐjØ ÖÅ:ríUÈ<Ò 3;kçA¯í\x0010jOÞ°\x000bµUSQió·\x0013\x0013\x0014¸8§D;\x000efm\x0012éb\x001fê^ùÝïÞÞßüL³Þo\x001ehfD¡ýîæëýýIN4S´=9Ej`­ß}y\9q÷Û«\x00174öýâºN>ûîâÃÕÕ
VìYq\x0013+ÐöZvàE¦5%\x0002ôý\x0015ú36ÃÚ\x001eÖn
ÈUÆÆÓ¯jÀJ`YÜ¥_\x0005»<\x001d²u=¬Û\x0006§OO°Óüé\x001a\x001aTi\x0003$\x0003Ï#YßÃúß¸dC\x000f\x001b¶é×á%ÀÎÔ3¢\öy¤zÐ´
ÔZyùw-dÂæ£Ð®\x0014êÓ' KTMgà§mvËÒÈË;-©vKz{ðÐ~·×\x0016tÉ\x001aÜüÖy\x001ayãòÁßN~ðföãð¿Ù3["\x0013t½
ïîî?´´.J¼E³ =»\x0005Zw\\x000c
?½{yõæi(ì¡p=\x0014:nK1¾\x001eNõ	øúiÙ\x0001e{(»\x001aÊ\x0014\x0007Ê!¾ËFÊÅ\x0012FE³X\x000b·\x000eÊõPn=\x0014\x0015¯ÈEÝÏ L²],³_\x0007\x0015z¨°\x001eÊ\x001b\x0016S CÙÀ\x001c£\x001c¨¸\ký\x0004KG§¼D´|Ê_ß~ýëéh¢ÜÈ8»ft9A	ÚY	!Îo¸¯/?üp2o\x000exáÁµ<è§-LÄs+O <iAçV\x0002Ù\x001eÈ®\x00042¡\x001dm[b\x0004~ÛÈY:!ÂÍûV\x0002¹\x001eÈ­i¹Æ¢_\9\x0006­\x0008
`á\x000c­äñ=_+ b\x001a]5H4RÚÕ\x0014w.¡\x001fó´\x0019(ô@aõ\x0017óRZg«Ã0èI\x0017\x001583×û@±\x0007kÀJ	\x0000rMGF'Õ®\x000boì+aR\x000fÖÂ8'5\x00163Gäô\x000eÁ¦\x001a\x001a\x0015V\x0002å\x001e(¯\x0003rò-Ò\x000c~(Tv^*[ûQ×\x0003õõ|©%\x0000W|/fFk¬AÈå\x000e 'z¡ú`%Ñ`\x0014a¥Ut9Z)±ÅÜ\x0018hRhÕ¿q¡¸p%Ñ``¥\x0015*_
DëÑ»öÕZ
·Ï~Ì@M¦Z2POºb\x0011
[k\x0017¸v\x0015È(î/¼T>ÉuÜ!ëú	 ÓìÙ?Þß}>
¬\x0012ºV\x001e
\x0006­¸~³I>»üîêå»\x0015tØÓ¡n,\#qS×¯Å<\Ô\x001fI#¯¦s=ÓÒÑ²W¾(\x0014Ød¥(\x0017\x0005Xê´Ðàù\x001eÏkñ\x000cy·§»ÒÈ#y\x0010*¿c¹u5^èñZz^ðhÁa¼¦ªHSÓwáÅ\x001e/êð\N ¦Í:	@KÈ ·ÀnîF¼Ôã%õÇ5í\x000eèXÞrG×>÷HßÅj¼Üãe­ô¢áÐÔ\x001f¼Â!4ÅåGµl½ÿ4Ã\x0003Ú:Ù¹&;Ûn%Ô38ÌWßÈ7d¥MvÙ¡Å[H\PÞ(`¯YÁ&Ú(°»^)Ð\x0017³Gñ\x0004úû^_\x001aoúÒøâ;TÇÓª\x00116,	Úñ3T ¯æ\x001b¼\x0006(Ý£!,>/O;TÞ-âsiSÁkÒm¸q\x0003Æ§/±øh÷\x0002\x001f¿¸S|Û\x0000¥ßp9´×Fk³t(%ïE~KÙ\x0013
Þ`Ai]®3<ê=æ\x0010\x0012Ck0.ÜË5|8\x0018?T\x001a¿òyý¹ç¯\x001b¤$=I	\x0006ßgé\x001d¡)léßi#K>¦ÌjJ7UDvc\x0015Ev2[\x0006p©\x0017|\x0015%Ø£È¾\x0018ÁC~øÅ?þ×ÛûÛ/Oec$|)"ä:\x0016Sâ}±2\x000b\x0017¡o?½¸xyuùØ¥
{6Ô±æu\x0002I`²\x00145L×µ=l¶g³J¹ùvÇöØ³ÞµÚRýÍõlNÇ\x0016êê1¾ÛÊs°\x001c¤ñËEV³ùÍ+ååÒ4þ¤>Õs;?ièÑRlQ:¨ã\x001cx\x0004ÍrÜ\x0016; \x0015l±g:6@©£¦\x0017\x0016[¤ÜR ª K=YRa¹¡Ì2ªXaIí _\x001cv°-÷lY-5I5yT&Èl\x0018²%{Øºû\x0005\x0019^£\x0016\x001c¿\HóÎ$¸,mÊ»\x000c/NAé\x0015hÀ%gÇJ\x0014
(/bxÝ.-Á)Î+ keD »\x0004h>\x0016\x0017óC1O»\x000e\x001c\x000c^\x0001nÁIÔÉH\x001b\x001cV¤åÉ\x001f«Ù\x0006¯\x0000:·@£Ï¸ðúây|\x000ef.¿+\x0007néº­\x001bÜ\x0002(ýB\x0000Ñ\x0006,v\x000b\x0018ÁÊ[µK	F\x0005Ü`|Ag}\x0011[

!µ\x0019Sh\x000e3r÷éÃ`ã@gä(¡\x001ey¶°)w
\x001e#&YòY\x0016_×²á`GPgGh8Wà\x0001\x0016ôÄÎåS±õUíóö8¨*êTÕ¥vy(ñ\x0007\x000fñ\x0005\x001f4¶&»ëÄá \x000e¨S\x0007¤#:ªç²Yú
³Ûç¹pP\x0007Ô©\x0003]§Û\x0014\x000bÃµf6&aóKÙv\x0005Û 
¨Óÿml.\x001c?¢î\x0011å»»{^}~âÙÊ\x0013ÍÜrYÞ¥Ï-Õ\}÷òêÄÞó\x000e
{4T¡ÑúÜ2a|a 	[ìòZf{4«BÃ(å\x000b\x0005CZ÷²s2úºBö ¹\x001eÍé¤\x0016¤>\r!«q-\x0010	K#ó\x0014h¾Gó*48\x000c×È<*­
E\x000b`)DR,èfÛxò¢^*­d0^ù\x0007.ö\x0000¬F=ZÔ	­Í
2É·&l\x0013ILÜwÔRThIÆpOCú¥>
¥s*\x000fv¡å\x001e-ë¤f\x001b-ã³\x0006rIy1Íº¬Â	ý\x0013Î\x001a´åÒ\ä\x0016C·-	&é*ØFg ñ\x0006.\x0017ãÁñ.U´\x0018.ò1 S\x0018ârúw5Ûà
@ç\x000eh\x0013\x001f-ñF\x0008\x0012\x001b4±-æ~W£
Þ\x0000tî Oß±Þè3\x000fZ\x0007Ú>Äiéh7\x0000;ðÐ&¢Q±D+ëU^~§^Í6\x0018]ÐY]JA3[p2l)'N \x0015Ê¥dm0m ³mÞH\x000bS	Êe QA&ÉírU8Ø\x000fÔÙ\x000fãÏ#{QÚ¯-¦MT4»]þ\x0000ÇM£¢.''a\x0011m2rò8hÅê\x0006»OlãÄÖÊ×½|¬´"RóEÃ\x001f¹b\x0008¤SayàÒj\x0005ýL\x0012
ÆVÑA\x0019£$Te \x0004UKìdû2²}ùí\x00189jÙ\x0018á~ú
ÁåãµçÎ´T¹¡ws®~,ÑºxÖåy
ñý2ï\x0017
]0íÜ_&)Uk'/úFÅ\x001f7ú©©ôå¯¾ùüY_ßÞüùöËíÃÝÉgÕrUV¥Ou/N*´CËbBrã7~ùêíÅ»wÒ\x0000ûöâíåûËë§\x001e.ýqW©ºJ7À:Z6ÏÅuàä!Î\x001b©\x0007Æ£'àÍ¬¶gµÛ\x0004kK@*Í
P·\x0016Á\x001e^¿">\x0013¬ëaÝ6Á&3­*\x001dêOÊÅ1J	;ªïÐÃºãö&\x0007ÇGvÕ\x000b{Ñhy\x0012 \x00153<\x0019Z\x0019ó×\x0015¥\x0000ÇýN\x000eÏê*ÊD')}¦Ò¨	3¶Fã<0mi·`fÓ\x001bx\x001e:\ÌRl\x0016ÞíÀã¹?}ÉÂÍý_oNO$ò¶¨yf-àª\x000f°N¦Z`G2ÞW?\\x001eJ\x0004Ç\x0013\x0000û5p¶.qÑñ#°1H­¯\x000f$n×ÂÙ\x001eÎêà2JòÅ\x0005	z\x0017ß~¹õn=ëÙ-â9×©\x0006+O,\x000e9\x001b\x000fèwÊ¬gó=W±¹\x000fE´ñ<ñ4 c}\x0006üì\x000b=\ÐÁ¡oÕåå
Êã|Ì¡\x000bÕ?R\x001b°-ölQÇd*óQC©¾zäe-YêÉÌ¹Ö/ï
5ò´ùG¦ÖÂå\x001e.«à<\x0005Ö<)ãP\x0015¬x
´Ë+ VÃõ\x000b8\x0014.¬Ô\x0006v\x0010$:\x0010eÀ&¹}Ê\x0000£oÐ9\x0007OQKn\x0003QL
\x0007cK^!.U¥jè\x0006ç\x0000:ïàR<MU9þó©ÁíÕU\x0018\x0003è¼C0Q&K;ëe«WôRpå\x001a¿np\x000f ó\x000f4#\x0019äÃ&.H¥\x0005ÍÎ-ÍY×Ð
\x000e\x0002t\x001e"DgGGû«ì6ä\x0012çí3'0x\x0008Ð¹\x0008ï[²ú£¸d&$Û¾ìN\x0018\\x0004è|DH­ÁÑx­úaoóèÌc\x0005\x000cké\x00067\x0001:?\x0011i¦â÷ê'¢smhÑ#ïÉ+áp°Ä¨´Äî\x0000G7
qbb\x001dî;t8XbÔYbÚu!\x0018\x000cËRX\»}Þ\x001fÇ(]g£Ö:\x001bÜ4;S\x001c;Ý\x0004\x000e\x0018u8ÒÄ9Ñ×ÈÙ]ÈÞ4\x0017»ÏÃâ`Qg#´IC´b§P:K\x0018i!ÆÁ\x0010£Î\x0010Ó´6i§=C|ê\x000eM=´Øl\x0017Ý`Qg£ñm\x0018o.6I?ÙbGm°t¨³tÑ¶õjt\x0017\x0013ÉY¹äÀâÂ*:s4SjR¶=ûæÓç¿|=YØ\x0013lpõQ\x0012]Ô#MýÈ	8\x001begõ²ÙüÃÙ7oÞýóµ=æ8Ãg¦\x000c¯vuã\x001fÒÒìúi19ÎíYs<Üp\x0003 ï\x0001½\x0012°ÜQk4¯¨Õ
\x0012ý·¦næóÇ\x001fØÃ¿y $Ôé£ËÁ\x000cU\x000eÜJ++¨ü±!ß\S
êt¶!±Ä
¾{(\x0001sô
¤Ä¡\x0006«Dt¶´ZÈé
Ä·Òò\x001cä	DJÍú?´®Gtz9f\x0010Ä\x0004òJ²Áâyií¤Ñ÷^/Æn]\x0017Ñá2*#\x0005Añ\x000eG\x0015cè\x0019^É¶Í\x0000^\x0002Ôî%8?:AWÁ\x0018{Æ¨#­¢ç'¹2^Ü´)ò)=Î¤\x001e2mÒ\x0019\x001eçFËpyYVQ\x001a©XÌÜj!s\x000fÕ`P¦§6ý\x0006úÖä\x001fY¢ì²CdÇÍ\x0006Ý6ÒäUâ|)éH\x0019E¹Ý#½­*ÊÑÛ¨Ý7ù°¢RRèÚCñ#\x001bFU»\x0001µ¿)1ÿaÙh[À]\x0013eMW@\x000e¶\x001cÔÆ|\x001aYÅ±£¡M%òª\x001dåU\x001bjéµ¥\x0004µ©ÌP[ëæò`\x00123\x0014\x001fç ó9C\x0001ÃäwÆ\x0001ÔëX=\x001eªÅc\x001bÛ\x0016³¬ct¬c\ÇjãQÀV\x00145èÛÛû/_X
b£TF\x000f\Ûc¼3\x0012`,v4_]¼òÀTØS¡*:¹ûQ1W¹ùÜVX.=¯Å²=]°eiÊß)£¦o&a)ë»\x001aËõXN!­äära©ÝÕ&Èü\x0006C\x0005Ú;°|å\x0015Ò²±Ye
²ë+y]xUk©BO\x0015\x0014Â:\x000c\x0008%[ç¥Ägò\x0015ß¶Ø°\x0016+öXQ!,èa¢ÙH\x0008kñÕt5Vê±\x0002+%) *ÿ\x0010©tÅã2],ÁZ{¬¬Ár­æ\x001aÚÑÎËv9·ôæ·\x0016«Èõ\\x0019Û©\x001dË\x0013W\x0016MLnq½íZ®ÑÈ+¬|±\x0000Ípû8q*ÓåtíÐE\x0018Ì<(ì|v2\x0018§D.-MQêrÝbíëZ¬ÁÌÂÎÓ\x000fùåz+s>ÚñZ\G¹k°ó 0ô\x0014Ë¡|Q\x0017%\x001aÍ§´«x\x0003W>Núä.éóùì»?~¼ý|*Æ¦¡ðÒ%l­¯©\x0014·,°wg?¼üîõå»§Ñ°GC
³STSk2rýòò\x0017\x0017÷­G³=Õ á!2LÖsKmz\x000f\x0016w\x0013¯'s=S}OeûUp²\x0013\x001eiû]'õ­Gó=W¡@çÐ"YÛÚ«g­oû\\x0016\x0017d®G\x000b=ZP¡\x0005ËO!É4p d\x000bKIÏõd±'ªF¥Þ®	­YÁ¶..fm\x001aÙÍÃÏ·~\x0014+õXI%0°2\x0001¸`qñ¼Çº¸8ôn½¸rÏuâj\x0019m§b\x000bm^^\¬»N^]tûÌ*°r®dQ\x0004v\x0000`tbx\t\x0000«e\x0006\x0005¡Å\x0018¤û'æ$ÈI·b\x0017×¨­G\x001bL\x0006(mã0#Ò\x000eln%·2ñÖ¥1Ü\x001a´A1A©ÚQcÏ²6í©£ö´Sïz\x001c&·þFpÑ4?PdRË):jãâÆK
ÝO#ÝO¿-ºîæ·E÷óH÷óonl;¢¶Còl\x001da»³â'xYÃØõ-\x000eõ\OÆ¯t_\x0016n\x0006Ö[Ó,±Ëâ½Òâ\x001bÃJ
Ý\x0016âéÓÞªÐIpÔô#~UýéÐí4X\x0018e\x0016t2+\x0006ÎònZª_\x000f\Q/cÙ_*ü{\x0012Í\x001fß^¼Ü^îïoÏÞÞ|ùôõä¥
ÌØ£\rÕ\x0004\x0013\x000cSJ\x0011fpuuyööâý\x000f'N?¾¹x¹¹¬Äòn|Çe\x0012\x0005+Ê=ÇÙí@e{,»\x001e«ükÛÕ8Ùs\x0016V°.6aö	\x0015T®§r
a!ÈÅ\x0018\x0019§1\x0007y:ÅyY¿\x0002Ë÷X^!¬¤\x000e\x0017åy¡ÑF\x0019yó\x0016A\x0005Vè±æ\x001bæóÃt,ßÐËCÏ9WPÅ**¨hã²¬Ð°L{\x001f3óuÆ\x001a=\x001cüïüÑº\x0013fÛ\x0006.(7PÙ2\x0001I^$\x0016\x0006)èà\x000ettT©,3(âyàãï$§\x001dçÓ¹\x000epfõ§"íÁ¬~Câ/JôûÛ_Áÿïÿü¯ïo\x001eþx÷×û\x0013`Á\x0014sÁ\x001d\x00064©n\x001a:ëå%>\x001d=\x001fÿþòúU±ùgß_\÷ò«ä\x000eI´|dîË[[¹º¾7ÎMfb*þ)([øRHëëÊ·¾3î\x0011wÄ|Øó¡/¥VýH[:8ï.\x0015|à\x0016¬®ëÛc@×\x0003:=`@ÙHYÂ3C%ê,À|dÛ6 \x001e1è\x0011KÑO\x001dÎ,ÄÐf8.®ÒT!¦\x001e1m@L\x0001Áx@\x000cR½<[§£Gì_3òoP2\x0008W\x0006$c°2\x0017(Æ$Å|á(ã¶qÐ\x0016Ð«K¦9léÀÈÑRNá\x0019\x0018óqÑkµ\\x0007p 9US\x001a[Mi \x0017wWk6­¯\x0001G»\x000e?x\x0012ÏöxVG©â\x0015	\x0017êÔUx¾ÇóJ¼b\x0001ke\x001cztÃÇ(-KC\x0014wâÅ\x001e/êð(»\x001a¹ ·\¸jS)F\x0019Ié¹ÅÊ\x001e\x0005^îñ²\x0012/\x0006®}DÚÛ^;$J¸â\x0004ÏÎ/8:<\x0018UC«\x001bY\x001es1Ð¼s®g\x000eëKÀ°Xr¤\x0010ß\x0018^ew\x0008¯~\x0003?Ñµz\x000cµÌ4òêöìOw\x0015Ûî#M\x0006®·FªiàM¶nÒ\x000f¢Äpti,Aà7o^¾;;Zx_Cc>ìùp\x001b_\x000c<ã­s*ôMb	À`\x0003àÑ\x0003æ7üÉ±ê×³··_î¾½}¸»=\x0015­b¹0¶Tñµp\x0014sRíàú&9\ýpööòýË÷go\x000bÜÕ#lØ³¡­H¦UÓPQkØl'\x0011\x0006\x0015\x001biÆ°O®þ ø}Wn\x001f_ï§¤N®\nâ¢[Égâ*'«¸éé7¦,³3¡ø³rDh{9M]/Jww-©óþeùË\x000fW%ê:<ìñPçÁ¬&<Ë3É(½^\x0002w¨Úg{<«ÄC¨÷£G}¹âÑî\x0004^\x001b\x0007¹\x0015ÏõxNçki?eÃ8\x0007UèJèÏt¶Ío¥ó=WÒYÎE\x0011\x001eÖ\x0015\x0005/ßÉx~¯ðb\x0017xnÚ¥Tñò9¼é\Ëvn¥Ë=]ÖÒÅz9´Ì¦n&<#ÂËûàøÚ!FÅ(é²kt\x0006ë\x001dXë|dºa'ßhôV\x0013øX¿mæÙi¶S2_«ÝØÊ7X=Ð½r¯Föül\x001dxHE\x0012 \x001bìÞï;=PÚ½`8a\x001biPjM¿LE\x001cÀ|q7ß`÷@iø\x0002-@ñÌ\x0017h-ÊÄ\x0017£ØåÃp·­|iàKJ>Ï}Å¤½IÜ³´½»j¯ß«\x001fq\x0001¥u	%Î¬¿åné«ü\à¨zëÐìÚ\x0001\x000e\x0007ãJã\x0012\x001c²ßÈ4r\x0013«r8Z#ÇÂ³;-3\x000eÆ\x0005Æ%©ÃHxX/l`½\x0007áíÄ\x001b#*¥m	K#MR¨Yèì%±}9ïÔ
\x001cl\x000b*mKD\x001e\x0008JâsµB¬¯Ä|"¾´Ó¶à`[Pk[¢¥.*¿P%ü¨ òí\x000eIq\x0008[P\x0019·$Z4Ë¾#ÄúL[t¦²T¾ÃcÚV¾Áö¡ÒöÅÈc\x000b_m
|\x0006ù¼vgÔéC¥éKàëpÀ*>¨Ú\x001b¼\x0015íÅ½¡\x001d¬UZ¿U\x000b(ÏÔ\_á#¥`ù¹½|õ³Jëk3Â7íe ¾r\x0003NÂ÷ò
æÏ*Í_2ñÜÄ&?Sùüv?;Þ(æÖ}¶ó\x0007uDPQ"Káó;½\x001dÌU¿®ÖõTõuÕ<\x0010Òsé¯
\x0003_Pò\x0015\x0003^¬ê\x001b
`û¼;é\x0006ãgÆÞ´\x0002;_ÏC\x000bh(¥i§\x000föJo°~Viý2U\x0014Ä\x0016[*¾M\x000b\x000epgÊÀ
ÖÏ)­_¶üàFÎG·\x0016>tÍùîÅ\x001bS\x001a\x0017ªúq\x001czîN£
)òyÍNßëS¥\(4±Óì\x0016ºVfL³ÃvíÝ\x001bZ¹AwRw3åY|èIkúº!HÎ%í¼\x0015¹A9J9`j8\x0010\x000c"?7õC?S¶Ï\x000fÊáµÊR»x@¢àUyd
bØ)??\x0006^\x0015\x001aÀÔÝj%´y\x001f{^v_<üàÙ¼Ê³Uå^QkR("k\x0015ñù¼÷ó\x000eÚáUÚ\x0001µ4\x00088!\x0019Å6çÈ\x0017\x000fmÞéÛüàÛ¼Ê·Më>é]M\x0012L½Ó¾¨ßi]Â \x001eA¥\x001e0ÕaÊ[\x0002êM|ülógw¿08 r\x001e@ïS|1¢&f\x000e]AÉ§hw:·0¿ =¹Î­úw#[?+9ÓäÃÞÐêðÎ{¸|ôUç«",k[ê¹Ü?°^/\x0003»Èýcó)´ý;eýAWIòî\x001fÿxó×ÛÓÏmù #å\x001bË\x000c\x0000´o¼dcÎÞ]¾¾øáÑªø
{6T²ZXØÀËÍcZ ]ÙÒâÍr=ëÙ-ÙóT\x0013ö):Ô)ïðÕz¶Ð³\x0005\x001d[äñ5­ÄÌP\x0013B\x0010='s\x0013Ø}rK=[R²ºJ½°!Òç­lòI\x000fû$7¡u¯Dv\x0018P´-4è¨+\x00108\x0013T¢\x0005»ëÂ \x000b Tà$V)ÿW÷¾\x0012ãX/F³t
_\x0001\x0007ÇïºÐ½ëýáö¦ü
_\x001f¾Ì\x0001(×\x000c(6\x0003½i|õdã`ùùïì\x000f\x0017¯_¼ùpýØ\x0004Á\x000e/öxQç/\x0008¯DÄ
Ï#§0 Ù¥8´Ã{äõÙRÏ´¢³uH\x0011]ù®üòç¤\x0000\x0017Pèrµxæ¼:/2õB\x0017#g/àÐ¼®ÓXèßu×â¡$§Ü\x0017çni|¸óàuJ\x000bý»éJ>_×\x001c\x0014<kê\x0014\x0016\x0012gß\x000fa±E7¨-¨õÖÞ"mÿ\x000bòyE1rÚxøþFEr}lò/ôËC
U1z·OÚ<k#Ýä\x001dïº.ú@=KÍ£}T\x0003\x001e×(\x001d¬ÞPÔ°gB\x001d\x0013­Ì¤©0ÒQÀtÉþøo¾?þ+?\x0002MO?W7T¼õùÓÇòïG~´¿ûáæëß¾Ü}$\x0006g]¹mMueÅ7;¢%\x0007_îXÓ&¶H¥~»øð/ï_¾þ\x001dí\º~ùîÍëG¾ýñ/÷\x001fÿ\x0003>óq\x000eùÕíÙ\x000f%¸½ùãíã\x00181À9S8[+\x0018A¾¾\x0014
_ßÜâòì\x0012Ñ^|wù»o~¹ùL³Iä\x0017A\x000f±Ý\x0007ª? ±\x0008åãÏw¾¹?IÄç¹ ¾yFªÆ´ ¹úÔÉHtd^¿xùöâÑÊ\x000eËõXNåxÊ~Áò¦Vk\x0007Ú{o\x0019+Ô\x0011Å\x001b±B\x00154X¹öÒ\x0007ôµW°¢`y\x001fv`¥\x001e+)°0W­/X4÷"U¬ò\x0017\x0011¶c±¿a,ñ7ë¸ Î*HÕ©\x001e.ðÅ\x0005KÝÈ5yÐ\x001czHub}á¢\x0019ç,/ï\x0019\x000bý3\x000fÃ\x0007Í¡§:\x0017¬Xûï\x0008\x000b¹lÚ#®áÐæÔ­%Ã«8)«\x0016¨ÁZ>£«Y\Ã©\x0007Í±§grþÅFÖFÌY¸Ü\x000e.\x001c=*} %¨ò\x001dm½\x0007\x001aÃÜ¾£ß5ZzÅ©\x000ftåàCïjAP US\x001f÷Hk8õ¨8õÁGªB¸À×Å\x001b+Öç>2\x0012y¸SSOc¦\x000292^¦¶¼\x0004Êà¼Ì6[ï\x001d¶ïJªÏ\x0008áçüýá\x001f,\x0015;1\x001dûr¤]<v\x0012m,\x0014¸¨	¢üåËGgu`®\x0007s:0ëkMf!KU\x001b-Õ2\x0010Ë<)}+ï¹¼&õä*±ò5)·8\x000c£èoæTh¡G\x000b:Ñ\x001cb¨"¼»¾HÍ2\x001a
;öE*´Ô£%\x001dZæ%\x0016\x0005­\u8ª°ÙgFK¸ç ua\x001f®±kØ²Íuh\x000f±ñ:ñ@ñ­6\x001bnE\x001b\x0013tÚICäÃAll7<$\x0014±í9k0¨'èô3\x0003\x0017ö\x0014´rÍfSë06©c¦b\x001bô\x0000tKÄ/_JkCeãcbó{Ì\x0007O\x0012¶¨c£\x0014¬°ùz
4Ì°É
w±
J
:-¥\x001d\x001aÓ\x0013±åºßØ,¶oºG\x0015pÐRTji\x000e±¬
ö`A¶©\x0002\x001c»Pè]èO_\x001f~®ùGÉ|í~Y<Bªù\x0000J{G/J	\x00175Gñ$ëá\x0012Î\x0007Çp©¶\x0010\x0012\x001c48\ø¤\x001a¸ÐÃ\x0005\x001d\x001còÆ`òñ\;ësJÂ0nÁ)hØRÏl¤U##S³_úl\x0019.îûªÏ\x001aS¯«è«# ÉÕÛS÷Tl\x0019ÄÕãq «¤\x001b\x0014\x0002t\x001aQ±Ù8ZËÎ\x0008]ò\x000bÊª¡\x001b4\x0002t*á\x0002\x000fã(t\x000ejc¡3)1]8N\x0007)á\x0006\x0000J¸r)\x0016ÑY¨\>ß&&ØûãöÃ¶WõÃÇíÚ§WAè2òé+TO\x001f\x001c|?\x0016áÂÎ\x0004Ó\x000fô¯?èf\x001f¼½¹y8\x0001j¶ bjw?P \x0000\x0016¬ÉÛëÇ?þñOÿöc-´ÊëÌ¬ç45N$ÿtûñ~¸}øõæã/î¸H\x0002ãTØ\x0014rÈ4´¤Ø9\x000cõ"S^~_*Pg¯Ï~¸¼~uñúÛ7/ß=°¥ÍrÃºú®\x0002áúÓ×?ÿû*L\x001c55Qâ6P\x000fk-ek¾}Ð#L\x0016ãõ\x000foÿÇ£b<Ú Á ¸\x0005¥\x0019\x00142
B¨EYà\x00184X|\x000ePÛÚ
 4\x001fi\x001a³B AÊc\x0000±ô\x001c ®\x0007u[$JµY±}z®Q-QhhþY@}\x000fê7"-ÃÈUÊmÒV"UÈTP^^´\x00174ô aD£«3\x0004\x001aë\x0002"ÑE¢ÎÁsÆ\x001e4n\x0000µ²´@
Å\x0013$Ñr
DëmÏ\x0001zÐ´É<ÅÃw\x0017ÛT\x001fÁ§ïþ,\x00074÷y8#¶ïî¥K×9Sß
¨±Ï!N\x001bÅÚ-Æ	S]èH"\x0005.\x001duæàl|\x000eÂè¶8¦@9ïJ
´!»Ö\x0008ÇàY¦Ôÿò\x001c¤c-	Êe~ª$©2jïM3£Ï$ÒÁ1Á\x0016Ï\x0014
z+"5¹î¥\x0001pÀv&Z>\x0007éà`kkuäpL¡M¦ÏB:X|Øbò\x0011ã4Y@ñ<WÏD¯ÌùX§ã\x001cì(l1¤ÿG8q0P¸Å@aí©a³\x000cdpè\x0000g
ÏA:Æ£[Ôþÿ\x0014é M¸E,½±\x001f-hXëÝËýõ\x001erÎÏA:h\x0013nÑ&\x001bríi%R\x0019fB\x0019@'¤ö9l)\x000eú[ôÉÑ#c\x0005E'×&\x0017,\x001b}ñ9n#vP(»E¡Ê³Å&\x0006¬ 1¡âsÜïì Ov>9Z[È"¥huø\x001ejz¼çí Nv:¹¢í\x000c
%,­×Þ³s\x0002oE¤:Ù-ê\x0014rª%\x0017z¾¤$y!5Ïsg¶:Ù-ê\x0014çÝ\x0011©åm.EÇúd|~\x000eºAÜ\x0016}Å&\x00065\ã_ND}`"Ðð\x001cÔ
úä¶è\x0013Õäq\x0000M
EµÿÅåb¸ôYî¢¶%\x0015[Î¤Ë)*Ü©©ÃÌ)@ÉÜsâ ,w½}Ñ>\x001cçË Ï}G0w\x001f×eöÊ=¬¾GlÑÔ:rË7 ù\x001dwZ©¾£¼|ýØÓTG=-n¥Ú\Qh-¯\x001a"Úv=îô]k{\»\x0005wj]åÊÊ4©\x0014\x000eaÿ\x0013ÉÈõ¬®gu\x001bYi\x001b×!%É=5)É\x0015\x0015}.\ßãú­¢µ¢a\x0011¥¥ \x0005Å'îÓëaC\x000f\x001b¶Â¶\x001b 5 3\x0001Ó!õ\x0013O[¯õ´±§\x001bic¤lCÝËV`©·ÒÂ\x0013	Êõ´©§M[ek$v¥þMÖ2Ð²'BÂõ´¹§Í[ekjm½\x0013p/G¢\x001d±|'x&Ú.½\x0006CzMë±N\x0008§x»õ\x0015­\x000e·×Ó®l/£A\x000b¶Î-­÷\x0018nDIÖ\x000bnz¦\x000b/MÎ¬àÖrùzGµ¦êÜ\x000f}&g\x00063­Þ\x000ck\x0017×ô^Z§$Ñ\x000b.¦g²b0ø3ØêÐ0Kd\x0003)Õ* ÂÚéuþt¢`=ïàÐ`«G+­±
øX\x001b)h¸\x0000Ï&ßÁ§ÁV§\x0006X'ÚQ¹\x0010ÊÀÂ\x0018ä\x0003Ï\x0016ßÀàÕ`«[\x0003'¶\x000cèÍg(É+IOä×ã\x000e\x00026z
©ÄÒ¥©ß|\x001al\x0000Io?[KÏä»KÒ½ùö"\x0013QÆ¸%Øâ²ý&
/?Ø.?´ãËÃ-
Tj,Ö¼r6­³Åªñ\Æ\x001c\x0013ÛC}Ô\x0012ñÙåûëK\x001a±p¢ú¢!cÛ}æa½k\x0003IBø,¼]ªmOl7\x0013\x0003:£$dÊà\x0005~û\x000cÈ¦Íú|*»¬Bv=²Ûì\å¥Y¬<\x0014$­('åÔ­XÅë{^¿ã\x001cç: ºðl]\x0018Hcj\x0002§Å-w§?\x0007rìãv\x0011vwÅáqQ\x0011¼9\x000bÒ³!ãhã°_ü¹Ü¤Z*[T°È3ûÞñ*9ÄSfNwy\x0019m;Ñ?m¦NVv\x001d
\x0011Ìü\x000e	Yä}òÝLI}3RßüßAýËHýËÿ\x001dÔ?Ô?ÿ¦©m¿Þ£þ K^¾½}(¿}e6°\H¸äF*×±
%x¶âºÝé\x0000ôíåõ×'c
kÜ 5}%§\x001bÔdñ\x0008\ÆS
«;i×°º~TRýA\x000b2¾½ÿôõaêQ ã°î0dXÎÑôÛê´ÁK®µçS\x0001ó³÷o>\OÝ\x000bt$\x0006w=¸Û\x0001´²¼\x000bç\x000eÅª\Ö[ÀyoØs\x001e<ì\x0001÷rÁ¶Ô^\\x0005^T0>¼ý	\x001f~Je\x0015äN\x0005äËÙ?Ý|þ|ûõ¡@&SQ}[ñõî\x0000iÅ´u dOï05.²ÎcíõÖÇÃ\x0010î\x000f/¯¦âßËë÷g/¾¿x÷îòÃõ£Pÿñ§\x001enå@Ní»»_?}<ûýí	"oiº\x001cEå_\x001dmÍ¡X\x000f±E°Üù)D$ªw/_½y}öûËU8EÛíz\x001cë15º\x0015õÊzú VpÀÇ]8E/B:ÞÖ%k$\x001d¬5RÔk
V¤\x0013a\x0017N9íAÕ\x0006\x0012M¬©Z\x001aÄP[QH8û>UlÔÉF>UÈµmM\x0016Ù¸}²I¿ö*\x001ckvN\x000e?\x0011ÐvÚk2}8å\x0016u8,\x001cZ\x0017
BãÚ§Ê{h(\x001f-9é58T×kø ÓÊ»XyààaåÓ&\x001c² À¡E;ÐÎ\x000eë\x0015íTlggÓæá.4ª?èB£û³W7÷7¿<Ü>ÜÝ ó\x0001kÝ§\x0001á¢g\x000eåãAÀtLW7Ù½º¸ºøöúòúåãî£Ab\x000fzÈrãIaj×¬çÝ\x0001²\x0008\x0001\x000fS¶CÚ\x001eÒnd¨è\x0004éjå&I²¾Ö\x0014HiÑõn s}ôð\x000fF\x001f\x001c\x0005±D3»¡gô=£ß Ç\gIzzê¨ýß$ÇÌ~ÈÄ\x001cöC\x001e2lRi\x000ev,á¢6"ÉhgþI\x000f\x0019{È¨¶ë\x0002iLmÊ(ÍòÏ 6©L\x001b$É\x001c}Hiúe¤DAÆgdî!ó\x0006Iâ4ú\x0018DjÎZÛ\x0018÷ë6?Â%7\x001b ykf:X6@-H)Wý¦\x001cF³ÁáD\x001e\x00182³%·Q¤=,§ØÎ8¸\x001bÐû`°
ûàëÄ²o.&º°ß\x0002Áàn`¿Iâ¹C²xÎ[î2Æì·ä0x\x001bØàn¢\x0017¿èýZNdÍ3O¹þgøÚ¿
\x000e'qgP¡4±ÜQ+efF#+Ó3rð7°ÁáäT@½DZï21ò;N4i¿)ÁßÀ\x0006C\x0005¬\x000cxp\x0017Q"CvãÑ·C\x000eþ\x0006ô\x000eÛÖC\x0019iÆ|\x0016åfQ¦4»\x001eè!\x0007\x0003z\x0013([ÉôX[i\x000bdÎr(1=C4y\x00186ßî\x000fÝc®&\x0016 2sFÌZ¿Af¨a\x0013+]Ù"\x0001oe%«é2Ë5=Er3X·\x00056ÐÀ\x001a\x001ayäytRëà×â0<eB~}9¸ËßXäú\x0003õ\x0007ýM÷¿ÿó¿¾ÿÇÿ÷åöþìÛ»Û¯§\x0012nÖñÇ/:eê\x0010\x000cÇâ9ø\x0008\x0017?þÙ÷oÞ_^}ûòòÃÓØSâ\x0006Jk\x0013\x0007\x001fåC§ó\\x000f\x0000B¹l T¶§´[déM­ReYV§!ù&ËE¤¢t=¥Û"Ë\x0012\x0018¦¤¶¥ªî\x0010l\x0014J¿hT¾§ô[d<gÊ'YBuî¶%Ãræ@\x0005\x0019{È¸\x00052óp
É±m±\\¼§©(SO6\x001dKÇ©HO¯"Uw0Z'Ë	\x000e
dwOKÃÂ\x0007\x0005%\x0015\x000f\x001d0c%fÛdiw+\x000f\x000c\x0008¶X"\x0017³ä\x0006	3Tí±æ ãËI\x000e\x0015æ ã°EÉ½©\x0013ïÒÕR½Bér³v·½ìÂw¢\x000c[(©{*5LScãb ü³|s{ì"­¸Èïo?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=
Ñ×îéìø\x001f'»»ut)ø\x0019Kg\x001cÎq	t\x000eåT\x0015g£¿	\x0006[n\x0005/E£ñ|-\x0013ñ´@ÃÇY\x0014ñôÚ[N+^
Fã\x0005?\\x0014WÑcZÐêµÍßÊÆ¹
Êÿ#ôxM
_.\x0019)¦ìvö^ôFãiÐ\x0002Òx2 e\x000c¿Za¶\x0002
FÃÙÕW+lþjc{^Ä[\x000b>ZéR|:N©¤:Ó§\x0013T¶î±[ÀK5LãÏKJ+ÐfT>\x000bºU0a·bU(°\x001eÍ'U¶zÌ¡÷æ0o\x0006ù¸ÛÊ·Kôã×\x000efâ3à>"¢g ¶^ÕÊs3FóÁ}5­\x001f\x0014\x001e¨\x0014	zO·xè¶4Æ\x000el*Í¾\x0002³B\x0005åi<ñ\x0016à°´n,\x000e×l2â28_"G\x0008\x0017c\x0002i­àaÍÝø­'S»iÀ\x000b¿Uh©Ô
êã·upã¿ZJ`õXþv´|j;'\x0003ÓÆ[\x0016\x0007/iùìÊ²xÄs|+ËGc\x001fÆ\x001f\C\x0011*è7 \x000f\x0012¿]¾\x0015§Kã\x0017FóÁË\x0015\x001e\x000ee©*Nyxf;^JÝÆÝ$--ã8J¢£Àx½\x001d»G#\x0011Zð4ÇÍÇÆBä#Ûbõv¾]lÉ\x001aÍ\x0007
\?+¨ÄØkN»ÏmÇöÑ Ñ|0éÂg>|JöTì
-\x001d\x0013¾_õÞ?Yç&sûÇÇÁg\x0006.$F{jD*×\x0002K!¼Tk/Ë9<?+?¾¬È\x001aW\x0013M;MÃ\x001aðaê¤õH$h ú]]Ü~»ziþöôð8R2N/¨,ÜÅ\x001cÞþ		æìþv~z6XAÑ|T©LÂPÎ(®\x0001TäwÊ­·&UR\x0019ñùî¿øRô¿ÿù_óËÅ%êÈw;\x001cA ca_jTÜìÊ¢£_7µ«\x0007¢ÙüõüõúíúÆqþÔûû\x0013n,ïgWO³WûûoOW Ã¢_\x000f¶Râ×z\x000c~5_»Tÿý\x001c¤7vOfoÎg¯æ''ÿ¨áJ÷®q\Vo÷Á¹´ba\x0012VK¹\x0005®tá\x001aÇ\x0005£S^6xr2«ÖPí¯ÖÜN\x0006£«ÂÈoR¦Ô h%Á`Tô©tÓ¹°a4\x0017foChF¯,ÖáÞ\x000fnRO_1ê,\x0018ù]\x001aÊô\x0010>\x0019J§jÃ§¯\x0019Ù±qdÒ§¢"\x0010¢Iò_\x0001L»¼dNN\x0007ÃF`.Í]\x000ed ¤æB[ÚþVµK½||o.»e+çø³§Ça'©¸¢Öf\x0011m¬Ã²BàMÔ¯µø\x0006v~6à(W`Ï\x0004«Èàj^µ\x0004$ÁjBG\x0015È.j M#º\x001fãÐ \x0001É\x0014õ18ÁVd[X²¨D)»|Uh§AhÍ3ìèuLzBó(l#ÛòÖü¢_ræ\x0007!\x0010»¸{º7\x0000ÆÃµ\x000eÓ1é\x0002îìZc±ÜþËd\x0007!\x001a{ut~ò¶\x0002
RNVfi<*±i\x000fïÍÒXêõ¡z¶¿>ó\x001bÿá¥eÛ}øt3T\x001f\x0013®jò»\x0012DÆYiPq'ÓFóëÂáÜ==Þ\x001f(YA=\x00139¯¡bi\x0002\x0001P±ø^{©D#¾üSÝ½¼Ãî7\x0003_¡àN`¶TÂ$T{,Áï¼äÅ¯ðüd·$kØ¢Dî\x0018*ã0Q%U
HÁ®!\x0010ò¦
H?üe{1¬^ÎÞ.î/ßB£2m\x0019kMUúþ\x0014Õq:«J\x0005¦»³·ó×\x0003\x0011ÿ
íÙp:6\x0013ÄÃ×\x0008Ò¸·`Zb[oå\x001cÁöÈ?ß\ÞvãÄ»ÛwËÅàýÃ4Z\x000eÁ9L"Kt\x0006Þ¯z<\x0007GowKú=\x0006LÍÖ1$\x001e\x0019ðñ:0Ì`\x001b\x00190XÃ\x0010ÜG\x0006\x0018xg\x0001÷²±|í.]Í@áT
Üáy\x00190\x001e35q\x0015t\x001b\x0001Íª!\x0010ÔÀ\x0008\x0008\x001a¯£²Ã`\x0018â­,~Ô@(z«gSµç¯¢m;H\x0005Á\x0010||Çý UtHÕ\x0007ãr8%\x0018Àøñ=! %$~|Ç=¡ \x0007\x0011?¾ãJÄ!\x0013ñã;\x001eÑX®\x001d?¾çJ@¼\x0017?¾§qÎ\x0011«ïz@\x0002Çeâ¸ü\x000e\x001c7_/Äï/Ea§ûûÅÇÅýÅ`;
\x000c1À®#%RJ@zaéª&¼,\#Oç''óWóW\x0003M\x000b~ùôg7õÚ}gøåîþqyûp½¡:?Üº©\x0005	J¾:ACÂñò#õ/G'g»§{\x0003á~\x0007ñyáU%¢wi´+ jª\x000cw2·l»òCë8ÂçÅMu0mÌóÜ\x001fGÏIÏ\x0005Ú\x0011×\x0010U"rEÏÕ ´\x0019P§IþOx&¦ ~üzùõñ©p]yu¿\x0018zà\k\x0014\x0006áëNJwáj/ý\x001eìYñ>ðêd^¾
t¨°Ãi\x0014\x0015ÇÇ.i\x0005
\x0002\x0002\x0015O¶ÕCýÚD,	i\x000ciG©4]]JãÍB.\x0013ÄÛ¸$ûvýrö\x0007¨î\x001e>?Eµò¢µsÞcIàZ>\x000cì²ð\x001fÅ`¬.ä\x0000íèüôïçÅ\x0011=<ì\x001bç5Ã÷\x001c\x000cMçkjï0¼l\x001cC·\x001a25\x000fÊS\x00053& F\x001cÉO\x000f\x001dj@\x000e~\x001f£\x0001ÁBÉ°:´\x0012ë¼~S¾Þ/lñðYw«Õ2Þ¯ËûÅõÍÍð«¹p\x001exF\x0005\x001ckÐ0Û\x0002ñëîÉé|oàÑ<Ó½0Ò³\x000eOÂâq|Q1Ô£g¨\x0013ÎjÃ
«×Á+õëuðò8x DÜ¬çv¥ýFZcÊòB&k\x001cÞ³¡=_®u¤7åBÐâ\x0010þâ«\x0012bóâmün£îbü\x0018I§$lw\<í¨\x000cÁ*¬\x0017²³BJkÌâIÈ¡ÄÑß­ÄlnÜz<+\x001cÒÖÓ¥Qx0\x0001+~>¸Þ3Xð ÚÑ\x000fÚFª-l=\x0019G·Éñ'C\x0018|	nDj
ÔâO\x0015%¦n=\x0019G¸Éñ/¡sqk X¨æ4C4\x000c9\x0015[\x0017m"\qü\x0018K&\x001dÉu8aÈÙê¬p#-8Û1x
\x000fãÇØ#Ë(\x0016àÞP})Ó´õºôcÓ\x000fJÿ^¥\x000c#^ðµ\x0002Õæ\x000c*Z\x001enGáÅi\ª!\x00140d¾±!Ò¹\x001fF	½Ù\x001eoþr¡Ú-~]½\x0000ÍÎFé\x0018\x001aË\x0005)\x0013¾Ü§?Ù§¯_âã¼·ÛÁWR
Úxé
+\x000f\x00053XNÇ)Åqoå'Ò\x000eÕZð^A¥\x001c©QIP£JF\x000eÆUÓMÌ\x0015\x0002»\x0011T8bÔZQk¸Âé8µ/@Yz¸åávÖF¥\x001eÿp©óðyÖéfññî©JzÁ0ÎS¸Î]\x0014Ù§,@hÜºü*û\x0004C¡Ï7+/dÔ\x0018àÄVXÇ¨zF&6ÀRôny)\x0008¨5\x001f?]±®hùþ"\x000eùûÿ7\ \x0018þ\x000fi\x000cfú9!ÇÚIÆÝ3\x000f\x0018ò7T¸b¡"ëJ\x0018Èó¦³ @HQ$Ç <½r¹þ2?\x0006\x0006\|tóß\x000fæÃ__þºY\x001cüRü8^>Þ_\x000f¾*Ck%Å\x0012ö=Æ¸ÎPÁ0k!øñîÙÉ\x001e¼%\x000ci\x0007\x0004ÞPá£
D±UJÕçêLç	Ä­\x0015¨\x0000»øQ\x0003¢´£d¸õàª¸P\x001aÖ\x000e\x0002	>j@\x000cLJß\x000cHJá;¢µ+±\x001eßÌ\x0001V\x0007>ª¾\x0019O½ò\x0001$kù,\x0001&×¥iGp@\x0018|Tq@Õ'Â\x0005¾_qú^äºPÜ\x0008\x000eHNÀG\x0015\x0007cTt\x00105YÓFUtã\x0017·s@\x0016\x0002>ª6jpïÚçï\x0005µïCTNòEr­\x0003w\x000c\x0008ä\x001bà£\x000e§a° >\x001c§+BµÛ\x0010¨|\x001fU !hÅ¾K\x0003u\x0010Tà¿ö
y¿øQ· \x0002º<-\x000bµ/×*ºÇÀÑÕG\x0017¾\x0019¶2ª@ìjPD;\x0008]]yva¯r\x0012\x0010vtñqb5§A7\x001b38öñ£
ÄkÊv\x0002\x0008º;¹\x001aZ1#¶lV\x001b\x0011EºãQ\x0013\x0017D­T®mó.±øQ\x0005"ìjBOÑn\x0000±Ô&½i?4`Et¥\x0015\x0001\x0010Ü!\x0012gf\x0003$óÎ×*çÇp@ ¢k\x0003\x0011\x0018N áßLq\x0008µÀÕ¸\x0003ª©ãGÝzè¼C§T\x000b[\x0018AÄZd?\x0006$\x000eÓ¨Ý!`Ât^\x0010F[Uå\x0015YKù\x0001\x0001ónjÍ»7ðx@\x000c½qà÷qEX³ç§æøQ\x0005\x0002ñ;®\x0008L:¦RrE\x0003FÚ\x001d/úøQ\x0017ªrL;\x0004\x000e\x0007-\x00011Tµäg¤dÍ[\x0004^iãG\x0015\x0008\äñ±Ì{¸|ÒáUëÂ#@À¼ÛJó®y\x001c'@4U²ëL\x0006i7«°ËãG\x001dÊ²ÆÆäë&Ï\x001b÷ö¯\x0006N¯­>½\x000el\x0004q,ÍÓë(a«yóéµ±ï´6Jîf\x0002ÑÙHÎ¤Öí+\x0002fÄÖ\x0011çòx /°¥!Ä"ÙÓ¬?h\x0001\x0001Oc+=r*\x000f	¦Íµ0Qö\x001b
(\x0018Ç:\x0010½C3Pdv½¹iGÚuñü\x0011\x001c`WÝ¸\x0019ç\x0004Á0\x0016C\x0017	ºÑÈgSPFÀéu§\x0017ö*êó¯#GÙ<Sà\x001eÁ\x0001×U_ñ¨;;ÚÃ7CgÆ¯ÏÝ\x0018\x0001\x0002×Õ\x0006gÁÑ7#5õuù|ÅS¬dE6ç«\l\x0001­ÍW\x0019N\x001a\x0004!\x0002Ù!\x000e\x001a\x0015©¢,c#\x0007]W\x001b%\x0006[*ða\x001dæR	)\x0015ÅH».è_\x000fâáìúÚ0Ñz:»+ùüÀAÁ+\x0000\x0015\x001cày}¥ç5PÂZÊa×b'Õ4TÀ¬O¾¨Þ©\x0012Ìqü¨â\x0008¡\x0008bH¡þ
Ýwõº\x0008ì\x0008
xiæç%üû©×\x001c®wV¡\x0010È3\x0016|«\x0005Úµù]eY\x001e \x0004ë¦QÌ,ts\x00161æ\x001fem~\x0017l;£ýá¨\x0001Ùñ\jÖ'5Ö@\x0016BÖ¦"´È£8Â\x001dò».M¨b>sãS÷SüøÎ×\x00190C?Å:[&)mÖC¼âdCL)hÞ¼"\x0010\x001dÊÚ\x0010QkÚ\x001c$èPÞ3os "awÉê\x0010Ñû<ÇÙ\x001dY®LÖÍ{5Ôrä·¢¦$q)Mk¤ª\x0018îÚ\x00001I\x0006Ä/Æ;j°*¿\x0001Ø\x001cüþ]Ç§3\x001b\x0010à×ëÇÙñÝÓ_wO×ï\x001aGÃÝZåäj\x0016>	Ôü®ØZóÆëÓ³ÙñÑù\x001cïýRî\x001cU\x000fêóU¼¯\x00167ï®o\x0007\x0017Ã[MJÖÈ8¯9\x0015\x0000pé<\x0017°K¯Úóý·{\x0003g©\x0003ÊØÇÁ­+U=\x0007Sm\x0000BX,qf]T·\x001e¿»·ïlç]¸[_°|XÜ¾\x001bªç\x0008\x001bIr-£³ÎDÖH4¾\Z°{:?|;PlÒa{.
[ÃfaÝ"\x001ddjM4ã-Ée°¡Âÿ1tÏ¥W«V\x000e&a§(\x0018ZÎyzõ÷®°ËrwÇ\x0008¼\x0004:«V\x000fRt¬¹£A=^Ò\x001b\x0019\x001a&­|¯ßiqóB\x0003Ïéâúöq¶ûçÓ§å°æÆL\x001dÇIâ<ü\x000fÿéµ¢bâ;ï\x001dÍvÿÏùñîîH\x0007°2ê\x0001½ÅªçpD\x0019ÿàJYªÄ\x0005!ÂÑýþ¢\x0011±O,\x0002£¢,\x0002RÏ\x0002ù¢­\x0000öÏo- \x000f{*\x0001ÊÒÓÁc\x0011 /Hì\x0006ì\x001fáz@a(ÆJÊÔ[\x0014l¡&7öò	\x0019×ï}\x001a±~\x001e
 ä7¸²ôP¦ÖE©ùú
Êõ|áKEiq$Úc?Ï*\x0007¿þ´Ù\x000cØ×P®\x0007FR:#ð
\x0018,XÝ3¶\x0003¸n¤ë	¡!\x00183² º3Âç¼\x001fÛÎ\x0011Y×Q®'Ô,§zRç\x0007_qWÜmÇÄ¬Ë(×ãY
\x0002ÜZltË%äRÛ-á­É(X=\x000b\x0005Ú)igqÐcø~)gÇ\x000b³\x0001F\x0003®I)W\x0003\x0005ÌcuÖñÖùiBmÇ\x0004®k)ø~Ir%hä`à+Î>\x0015Ú|G\x0013Æ÷Ø\x0015\x00149Ð²Êá3\x0013ÜFò\x000bàNðÞsý\x0012ÂT*¿Ê-$/§¡Sb·äIHpü\x0012BÒÁ­ÞûÓ)12ïBá·\x0013\x000b®kR×\x0013r¾³zÁ\x0013¸¹§A-ÅëªÔõ&'Ã­ö\x0014N\x001bK\x0015b
\x001fï\x001f¿¾\x0017ýW7Ë§åãð\\x0019cU\x0015üHÒBÀ&\x001bÒlµ¿{¾{6 [¼{Þª_\x0003\x0007íG8äÃz¼\x0007cMn9óòö\x001b	÷¼K¿\x0006.\x0018ÀÔ3\x001d"gO§W2ªev@E`\x0004Üóþü
8Ï8ä*#\x001c´Â§¯U*:\x0017 ß\x000cÇ¿=p}ýbS÷bö·»ÛÏO\x001bôy¥ò\x001cu\x0008¿M\x0002ÂÅ\x0006+\x0019Uè0ÛÏþvtø÷ó
\x0012½»ÛØ£\x001fûóL\x001e³tü?ÿ]óh¤(\x0007n¬"iËÕýüÙ;I\x001aµ´1ïÛ¡rQ\x0008Åýtñã-"ØâÇ\x0003»`?\x0004Ø»p\x0015½\x0005U×wO×wú~R0T§\x0010>å\x0006.É\x0014:~§ÖëNº]ï\x0001ìlï¨¬]ÁQp<[\x001c¤ ¼â©;ÀIõ\x0016¶,\x0006±	NÜsÿ(^Z¹ë»!\x0006ã![pé\x0002Kut$*(´ß\x001dì\x001dMY\x0007G\x0005WóÀðÄ¤0¢Aý\x001c4ög;¯L\x000bÐgî¬z±Õnñeq{¹\x0018PS\x0008_è0E¼bG)9#}qÃyé»ÿ:?|=/k)¬Àà]Å±d UÀÂï<îxâÖ\x0008Vè\x001b\x001b\x0003\x0016ü¤±cÁ,us¯4æÂ`È\x0004öM®+×}ürµüúí¥¯òõ\x0002F\x000fÞÜ\x000cùH® Ò75Bé4\x0013\x001a\¸·8\x001fÎ±g\x0013ìõ\x001cæ\x0010îï=ä
-*\x0008ê±lÐmêq l}T
/\VÌ~6íb\x0004ÛûûåÃ' /è \x000b±Å ¤H\x0008®qh#A£ô!¨ Ö:g\x000b}Äá¯°¬ü¥f:\x000e«\x001f?ÆóÙÜáÆ\x0004\x000c\x001d\x000eÓÃ­+´\x0002¼¾4÷ïz÷ÒWw×\x000f 6~|}9e¸\x0004e\x0014µvZ=U5
èWG{§ 3~¼÷º\x0006oxßæþúJ¸xik½½~¸\ÜnÚöÐ\x00059\x0007È°F\x0008cwá\x0016\x001aJßî¾\x001f\x000eîû\x0015\x001cådFÓiL'Y¸8¥w@JuNsÓN÷ñ?üqSùßÞ.¯\x0007\x0003þà\x0014R3QüYáT5®9¾Ùx¡âÁóÙÛÃÝ½pßkóu¥²ç_áÿ\x001a¯JóÛËëåíC\x0008{>^,\x001e\x001f\x0017·Ã×&	é|Ê
zª\x0018\x0003Í½Ôê\x001fÍù¯»çéÖ\x0014ÁÞîái\x0008\x000e^ÍÏÎæ\x00037¨\x000erº\x0018O@¶dØb&\x0018e\x0013\ÄX»èM'NNS\x0016ÙS\x0013©Ó\x0016S\x000e\x000cz¢sîo\x00199]ð§,2£»¾Ó$\x0013\x000es4©´r]~:r
G§¬²Á\x0013Ç]RN[ÙÒ\x0013\x0010ÛÞ\x0018)S1\x0001\x0019ú\x0012ñYÒ\x0018Xð¤\x0000BJ¬E\x0015ÓÓ\x0003ÛÁA;"=\x0005ÒK*r½D¬Ø¶÷Ezq@\x000cRHl
µN<RDÉ5\x001dFäË¿Ñ/*N\x001c\x000f'b$-%c|ä0"ùª'\x000b\x0001ÜñPVh\x0005ôL\x000cn\x0013\x0011\x000cÛÄ
&#\x0014Nm\nc¸\x001c\x0017<ë Ñ\x000f_¿½ÿÒ\x0012ýzýøxw= L\x000bó\x0002\x0005Ö¯\x000cÅßBÄPüÍ\x001b½Ö\x0014¸R|Ù;;;:Ù+kÔ®ÀhÐÏ82áa\x0012æ§DOCÞ¨uqj²«ÇOxHnðø,\x0004\x001fûQ\x001cç~Ó°í<[\x0013jS\x0012ÙVéº\x0012]TÄ9\x0019ÐÄÉ$\x0002¾¼øQE¢¹§¾4\x0017 4Ö-4©Uz}/e\x0012/Ññ£\x000e%ìe*\x0013ðD\x0003é¥hG¯gzêQÂW\x0003);ø.¿ÛÂ¼û]ÿñG7Ow\x00026ó)ÞÒ®o`¤Ìa¸e;¸®Å\x0018%Ð\x0016ðkÕ¶'`"Ïãõlï°\x0006(Å}õ@Â<\x0001Á=Ç.Bîòkêu8þ¯§?\x0016/\x0019 ïî\x0017C@Áè±\x001dzáØ$´1¹\x0008Ð\x0015ôÏGç'ó\x001a&\x0015«pGAÅà,Åi2Ü\x001aqvæù5lâ\x0006ª¿¾¨å\x0017W*\úOîSÚàc°éÉ7¥
SàS¥Ü×îìäè¼¼¿õy¸ûT¡êôËâi(%\x0011N¿£¼!W4ÛÅyjÈ,»PÒ/óór^"³rØúñ£\x0016D¨Rö[Zì¨
´4íÅP\=íÝ×§ûëw\x0010ñ`y»a\x001c¦ð¹f-ø@ª\x0003×
"¸^«&>Ø=\x001c¹B "¦=ÃÕÅwÝ\x0014æ+HB|y\x001aâÔ\x000f'CÉRü¦0$fëAü+È;üz^\x000eV\x0010Q»¯Bà&	¦Àá`Ù@A}©k\x000cÇÃâÃÇO·\x0014ÈÉ\x00122u;\x0018Ò!\x0016+?dñè¥t\x0008\x0005F\x0012IûóÙÉ.ä\x0000+6ñW#?þ£sgß\x000ft¿\x0004#úq(A	âJ4nV@%jnÓ .\x001bÅÚËÆì`=\x000f\x0006+\x0012ªæù\x0011P°*æ»¡,Þ-¾Ü¿ìT\x001efG\x0017×\x000fUJw!|l$
\x0008v·iJLêRÅ~¸Ö\x001d½Ú;;Ý¬u÷ùýK÷çËowï7ÃË\x0007=ºIÈ]ªÔe\x0016k9\x00186:'eÁÇ\x001cì½þew`\x001d;`év<\x000e\x000cÔfÒÚ)¸\x001a¤»A¸\x0013p\x0004+?,VsQò{ô)ÀBôÞÌ`Åhàðwz²((\x0019?F¡àv\x0019>~àÆäiìØÒã5+ì·hú\x001bÿp\x000b\x000f,\x0002\x0004¤ãGø¿~¿x\\x000eÎ0`*\\x001a0­\x0018þC6\x0008·á£³ëO»³×¿ÌÏv\x0007Æ\x0017|¹÷^\x001cÖ\x0012L>èy^,oo\x0007§µØ\x0010Y)\x0012¢v)§%½_
\x0008XWªéZzPõ|µ{x8B @ÎbÀZ\x0010¹ÈôÂÒSËº\x0002¥@¾\x0007X\x0014Þ%@	ÕPñc< \x000c×Ä)¸\x000e/c\x0012úIÌ»X-QCÈü'ýÐuëéþñ}\x0000»\x001b|Æf?\x0014ß×4¹>,\x001b¤ÏÈ!ô
\x001a\x000cü<\x000b>aÿè¬\x0002
¯ki¤DMpÝ1´F$³¼_{ôìÂ6W\x0007\x0006«\x000c\x0018\x000c!~\x000c\x0018\x000c"~\x0008\x0018¨ù_Õ0\x000c\x0012	\x0011F\x00197`PÛÄ1¡ÖßX7ïà\x000fâéök\x000cjÀ«DÏ²ýí©¦(0Oá\x0006÷5TJIÑpëñÁ|ö·óM¥æãV¬s¸ÏÞß}\x001ck\x0004
)(é\x0015åÎÒS¥ðT°Ë×
BÂ\x001cÌËyÂ\x000eAêwÛL\x0000ºY:\x0004\x0005½»¤\x000eÆµî\x0018DØ¸\x0008«¤éf\x0008ã4½l@µfJ\x000eÂ¢\\x0018¼öäU»\x000e<Ö%ÀGÅJp\x000bá>FÎ©Ó*,j\x000c>*VB3ÒÍaZL\x001eKì¦2~½¥\x001a\x00022ëñ£fO(\x000c¹©j\x001a÷ãÔ5ºö¸_½' ª=~T¬×ÔÓ\x0003ªføÏ²ü/[\x001fx]¿\x0012ÑÛU\x000eHå'«ÅÃ\x0015\x0007B÷\x0004÷2/
\x0008HLÁGÍé`Ô
ýÿ
÷É=Ð²y%ÀÕÂG\x0005\x0004TR$\x0006®qB\x000c4®Q¢Å´"@ý	|T ¬t\x0015c;h$£d\x000f\x0017­G\x0003,¨³TÚ~ªô\x000c^\x0001&"\x001aK#\x0004X*Qe©@ZcÎK£È\x001fg(½\x0004cÌZ\x0011 ¾\x001a\x0004N-P¯¤¡ìký.ÀV:[)ró}|úÃsAó\x0001BÌá\x001a
¶\x0004[)«l¥\x0011Ô]À%/¢Þ\x0012]ià²\x0001L¥¬3ãpx8%&AAÑé\ËÈÔC©u¦{j0S,ËµÛ§z<e,-¯3Ì½ãÉH«=Û\x0008ÆÛVBBÜ\x001d?*:¥I\x0018\x0005Ü§Ä6'K½Ù¶=\x0011í¼¬[Z\\x0017;\x0019ãGÅJ\x0004kV\x0002Ú#RëM°0T
]\x0011m+\x0001øQ\x0001±RH\x0000í«Ô\x00116uQB¤\x001e\x0002:~Tßpfµ\x0012átp>µxóõÏÕ\x0010PA\x0013?* D\x001e \x0000ýw\x0018fCFVÂ´}\x001dQ#!~ÔlL\x001d\x001fð\x0006\x0001ÂùicfI\x0012._õ7nL\x0005\x001b:~l\x0008ËUÃsVü±UÓBÀ=%~Ô\x0012úÂ?\x0013\x000bC¨/HxGëÆo\x0003´(ãÇf\x0008
\x00031à
ë×ø\x0016âßÆ\x001bh¸tAã\x0019Ü½.¾ë#p,\x0012Çâ;p,?ýuõ{wfÏëÅ_A\x0004HÝ¦|·\x00005+,\x0007BQ/g}Sñzþ\x001fóý\x001a\x0004P~_5\x000crÇ¥,¨Ö¤y¡\x001c\x0004\x0019¤}	¡´+2\x0002÷\x001b?61¤q·8¶HYK
u<ky³V1T
\x0001xñ£b!4
e\x00150¬\x001e£\x001aAÃ_\x001cÈ)øº¼Õ\x000f±0\x0010ê0T·0áàîöêîévð1Dèp\x000b5\x0018ó£ò\x0003á2_øJ/[GoÎ\x000f\x0007^CþøðÅ}½
\x0005C§×\x001fïn³_×C}|\x000c¤_PÝZs2fBâa^}.(\x001a:Ý\x000bP»³_w÷ÊM|¿}ÑüãËM\x000f¡\x0011g!ö\x000fÜé©­\x001a;4Úy§diâïëùéÙ|`ÆY\x0007km\x001e\
a¨ó\x0018\x0002\x0000,À²X.ípÇ¶z,¨ztc+l.,e!V0fÄ%KÝ#¸Â¾rb$s%,Í¯\x001f 1­0¥w­M\üæýÍ\x0007ßÙ]©8nvµ½Z.îï\x0016÷WÅ\x0015PQ\x001ef¤Ñ\x0014×\x0005Á¥skþ"UÉÍÞìÎ^íÎÏOvßÎOÞMw¸Å|)Ô\Ý_
ÔÅZ\x0001j\x001aøb\x0014L)	!:ÍN°Ò|ÐÓ@T.]!Ñ;Í\x0008&h\x0006Â\x0017µ\x0006\x0013à\x001b,øøyÙY£¿?-î\x001f¯÷`P\x001f?Ý,®\x001f®ï\x0007]¾È¦Ë9IêKçNµÜóßÏç'g{»'`QÏ÷ç{§{'5t©/äG¥KÅ\x000c?(\x001du\x0017þPx¿/þ|4\x000fU\x00155\x001bJ´U#
µpBíN*bóØ¯æäºr@© f°@ËÉwïº¦îçåýÇ%¼\x001fß,BÔñ8Ü lhD\x0002X7\x000c\x0008¡î\x001f'«*¿¦¢ñóîÉÁ.<e\x000cAÇYùÙ¬\x0003\é(0-=¶(®-\x0014uYaÔb\x0012HÛ
öáëÅ{Í»_p@ZÞ<]
\x0016\x0010x®±ÂA¥+FÔP\x0011kó\x0013\x0001ewÿüM\x0015H\x001eüY\x0001\x0002\x0014)!\x0007SÓSQ"\x0013\x001ckÑêÙ#g=\x0008F=U Ù÷fG§\x000b
\x0017xÑ5f½\x000bh\x000c\x0008ÔZ[I\x0012\x00152]"	\x00046!p®¤ÄQ|&\x000e\x0005?Bü¨[\x0012x`Äï\x0006®iI\x00043´IÔz!Ø\x0018\x0014(À:Ô{\x001a×D;êÑÂA!R\x0015ÏfÃn\x0000Y¼³üt¬ ¨ÊtÌöU:Ö\x001bàÖå(e\x0007\x001d\x0011©÷Aþ\x000e©ÜµÉûM:ÚÃ»§C\x0018N\x0000üúq	á\x0015\x0002~ýÀ\x0014?4!d¬ÕGø×ÅïÜ½Xûúî÷ß\x0007Ý\x001eWúï%¤\x0004PôÒãC³¦x%:úùç*¤ÔP\x0014\x0016ê%÷\x00020\x0014ß[µî÷ê®>³¯þåJø\x0010fA³×Ó\x001c\x000e³TÒ\x0007Î±T0\x001cïä\x0004g\x0003ñÕ\x00194~\x000fä×¾|zb7½v%4ÈB	é·¡\x0010é)jû¢q~áB«5ùú\x0000ö]è\x001aÒÿSñúÃ;é^ÞROW÷wò^*Ô)\x0015 \x0016ªvwåköÑù£²pàÓÏ×¿ó\x0017{<\x000f÷ÁC9Ç³\x000eb*P4³\x0004\x0012&\x0018}Z¿>*dõÚ=y=\x0013Nd9Ïî?~í¬\x0018©ß½]\Ü_/of?C\x001e`ðÁD\x0016Bòä]Eu¦p\x0014×\x0012¶¤÷vþêdowö3$\x0002j\x0000û"æõ0\x000fÛùH\x0000C,F
}k#ùúÂõ|Ââ[e¬¹µøVÉsÍ­\x0014/«\x001b\x0006ìkW\x0003:Lñ°p\x000bâÚ\x0014&W\x0004¿¬;\x001a®¯\x000cY¿zà¤ðë5ô­ ¹«ø¿
À¾Àzýêi\x001e¿ÝÔ/Â\x0005\x0014Rã·»fVùúêõ|á~â°!iTWãe@5åx\ÉË'÷Ç\x0016ùéâzC£²Å©´C+\x0005hÐL¯¥Þ2Øç¯ö\x0006\x001b¿\ûøW\x0004Gxø\x0015î\x000b\x0007«ûÅ»Án7\x0018®HÝnÖZò§*«1K%ÖÒ×óÙÁüÍÉüí@ÃÛ\x0010\x0017wì¥e:\x0014ÀåÝÇa(\x001eU£èp¤ç!i£çE°cH\x0002ÊD
\x001cIó¥S2ëÖQ{MK1\x0011åÃim§»´_mW"õdqù~1Ø\x0013èàQ\x000f\x0005[¬Üqq[	åM»±Ö°x2ö
8ÌW1;0Öê8(!óØ?Mµ:J¯mí
\x000cWJ=^¾¨\x0014{r÷0xÊ \x000e\x0003¤ÑÒS£K*i
^9é©ÑZÚNN\x0014
2Rîÿ«fâÁi#ÔYtßQß±×kn§\x0012É»/\x000bÕí\x0013\x000báÿü÷åû¡ò}(u;Ô24VóUNkMÒ"\x0004»¯\x0019è#XaÐõ±
\x0003\x0015I \x00045z\x0007G9ØQlmQ2G)Y±âç\x0010øU·\x001cÐiË«\x0018í\x001bÃ×"ªz\x000e	Í×ñ£
$ì\x0013\x001cÖ.\x0002ð\x00149á³«sí  ú\x001f?ª@\\x0008ÓaæÒf\x001f*ð2c¬]+\x0008\x001d\x0001\x0002f ~Th(ËUZ3ø"\x0017¾&ÓkB÷#H`>Zü¨ûn<£\x0006y¹5¨(Î,Õ§*V85\x0015$ðåØê/\x0007\x0004=Òð\x0000ºð"Ü6qµê³\x0011$0>;~ÔÍßÈ\x0019Ø°w5Õ\x001b1ÓºacÊ4~Ô\x0004C'G0\x0014é\x0006WD¯\x000f¯\x001bÁ\x00015`¢v¿:,\x000b\x000cÁ;QK&éQ¼õQ\x001a$MtífN¤Ô\x0000\x001c®\x000e\x001cÕLV\x0005Æ:Ùzl\x0014L\x0004\x001fuÇFHüb\x0002\x0014µ\ÿ4\x001ax-k\x00061\x0000bjA\x0014'µ^x 3x±ÒlZ»WPh\x0019?*Ï¯§ª8Ç\x0003»³\x0015\x0016x\x001b\x0018²ÔL\x0002kbj×ÄÁ<4´óVÓ6·7Ü°\µ@ý&|Ô(\x001a¨\x0018Ü\x001d£®\x0018a\x001díõç­\x0011$`XUµuÝvl$Í»o/NÀ<'ïÅíåàHÖp×0aD*z\x0012\x000e]±\x000f?_áÊ\x0018_¼ç¯ËW\x0015\x001asY7-\~Ò8æÀfÓ¨\x0008é%\x0013$nÇÖ-êÙ~¿ã¥è½>ÌvÃ\x0017
)âÁ\x0004±Ð\x001a[\x0017D¸ì¤Ç8-è"bù\x0011ÞÎvOÏN 3\´;<(÷þ£ðÀHsøU	=^FT\x0007Ì-]\x0017½\x0012ëoÚ]¢ÒËD`Ü\x001fõkäWk¤\x0018ÍÓþÿ©{Ûì8r#ß{+ÜÀðàýåèSIb«éC\x001cJês=_ú$Zb\x0012»IQîîO³ÙÁuÌNf%\x000f\x0002@\x0001 3@Öõ#ß¹U6i·óG$\x0010\x0008\x0004"þ¡­§¨em\x0010¢\x000fÉÇ¬ï@
k\x0002&æ:nºp\x0007\x0014Ì\x0005Dû\x0015H
þ¢øµ\x0018;IêUÂKÜÂtÇàX\x001b>Ztû^}Ôö!\x000bµ0kS«'\x0001M
Ñ\x000bT\x0012{.:©Ûá>4·Ëq­.:æeJuÂ\x0005×\x0010{í\x0018¬¯sÐ¨b\x0018Ný~ówóíAÛ~}wóñnöu
h"yB\x001côTS¢\x0016¤\x000bdÕT¦ÐÙéÛó\x0017og¬Ã\x000e\x000cfqd\x0016$Ô
_ wMø¬2\x0013é_~ùåú¡!;Ù~»¸oË\x0002#µÎ`RPôY;TésÊMél~:z=×Å|½úÕÅïÏ®.þxÿi6"\x0018<\x0006[uA[14òZìZ?|³|vrô×g?ÎÄÕ/×\x000fÊÈ`Wï«O #øêâîosgh;nsÃéÚBK¯è@ï's±Å÷É )øêèí\x000f¨¿¿Ë»2á\x001cÚA\x001c<¿ø5ãÅç/_·«YS¢H&\x001fJÃ)\x0014£%¶¯6º	ÞCKçGga8@n\x0013þ³ðÉÐïÕûoU1Ï>m\x0005I8ìÊ¶ùòaþvAi¶.\x0013òkp¶À	hYswùìÇÍ\x0019ÈÃaS¶Í«ç3·\x000büío¿TI\x0017\x0007O·7ó=\x0015¤EâÍ3H8"ÑujÍ»=:xº9?ÿënC ÓbD¨øµ\x0008ÄäÆ\x001eÜy\x001c,!¨=\x001cÙ\x0003_8 /KJøÔv!Ê91*Ó¢
Ïwx\x0000ñ\x000bA²z'÷Z®uØÅjÖÑÅ \x0012&HüZ\x0004"I4P@ZÊÖf
7ÃªRÃ\x001c\x0010º¯E\x001c*nskº8	Þ\x001d´=\x0017{@ \x001d
|-\x001d\x0010\x0012é\x0015*EÃxä%cü=Á¯¥\x001c\x0010i_8ÂÅ.Þ@\x0008hpz3M(o9\x0014ëøµlíÆ\x001e\x001eä\x0012×®#\x001dW­ZY¶å Pö\x001e¿Y3M\x000eç*É±Ý\x0014\x0019µ" ëð$~-[¼b#>xg\x0016×\x0004"Ì¨Y};ã×âW£qD<õÒ«!¯_\x001bÝ9Y¯ûýý?xéSï\iÈ¦{öéâó¼¦4$\x0001ãá\x0008®
r¤Ó0±mêQvÎ4$Ó\x0005çåñ«I¾ë¿1ù\x0015¶ûøõôîãÜýc8Ô\x0006ß^*,¥s)\x0002ÌÀÏ'\x0005F=âéÛ\x00177\x0004Û÷g\x001fe¼À,\x0018£]ßÎ§¯såæl¾¶æ\x0006
­07­íÏ´9xvúúÍÑ$»¼úb£\x0010$l\x0015\x0018bÌ¯Y\x000e\x001f|¼´\x0003

.A\x0012³6(Aî\x001a5CÌ÷¸øíöoûPdµ¼\x0008~çÕöö\x0016\x0017L\x0017ÎÂñ^PWygiÐ\x0019¦fÀ®É©z\x0011<Îpx}
ËOGÊwÝ|R¢\x0004c\x001a·G®¼ä'÷BW´½tÇærñp\x0001jÛxèñ$\x0017(û¾\x0007>	N@üê\x0005´a\x000b\x0015\x0014PÒx*í·0 dÍc\x000cPAíGüê~¿ÁN¥I·\x0010ZéÜêH®\x0000¼þöùO\x001bCq\x00107\x0013ÑV£ìowÿóß³¯1\x0014\x001fÐãÊ!\x0013î/N«)`ÿýíô2
ÿü{´\x00150Fðy¹ýº}\x0007çýÙÁ	Æ"	\x000bF½2êg¯IxG¶
¶^nÞl@ÏïÅôÈí»÷qQñ>\x0002*1\x0017xy'H\x001c+\x001c\x0017È\x0006ç$Eeã ¥]\x000bhÀ%²i¡$=?PÔ¥ëÍÜ\x0006^±¦L'
Ü,ºÅ4\x0006R{¨a\x0010%jÁ9w¹`khàn\x0011>KÇÆèCt\\x0015£\x0016áT>Ú4Êª0Á[Ô|9TXÍ=#Qáðß£X­²ë&Wø,¥	.¬Â¾jaã£\x0014SIÇ-eLN``à³x\x0012[*NKr¢ÞjË&;iÏÒ\x001aN£`²D\x001aèæn×rÛ&á§\x0013\x0005\x0013½|`¸¤;r\x000f9YÐA(~Õ1à.\x001f\x0015I\x0012pÎHzE\ØV\x0013RêD±ð.\x0014,qá´úJ\ä¥Ô*MuÒ¹¦Û<+w\x0017V\x0015¦\x000f\x0008Ì\x0003µÒëU7l&ðYJzR¤\x0019Ãrn¶ÍKÉ¯¿&X_³Ü\x0002ÃØàÝqoªÅÎ©\x0016k¦0(\x001då&ØxX4ÁP
w§]kÆ5Ó\x0006J9Ír\x000b\x000c\x001ctÞàQû&1Q'\x0011Ù\x001c\x0006»`$È$Ä¯Åû%tè\x0013
BR?EÍôi#a£_Kç7ÔdÅYÙÂ\0ÊEUmúI\x001f\x000e\x0004ã×â\x001dÜ\x0008OÉÁçt44ník'ñkñ\x0002gÙÅ\x0012â\x0010+W²ÔôrS#!\x001e¿Îb\x0011÷880P\x0008ÒeSìô\x0017\x0005áôøµtp¡v±apHá,7bmZu\x0017²ØøµxkÊÇ\x000cÿñ!-q*ÓRv\x0015
TÆ¯Å*·\x000fóÜR\x0008\x0001$\x0015\x0008Ç÷íígý\x0005tv8dëÅ¯Ø%|>)\x001cÆQÏ0E\x0001T»ÍÀBkHÞBW\x0005\x0010 î+õ"\x0008í±~â\x0018G¹gÅ\x0008BµÝ¤æ!>¼w\x001f®ÿ\x0004\x0008èÝ\x001d¿Î.þxws=Ó	\x001c4¥=í×:lO©¬\x0016\x0014$\x0011B7ÀÏþúôüôÙ\x0012
Ð\x0018¯%\x0014ÁÏµ¤N(`_J\x00144S³hG1@I\x0005¾b¤\x0000)ô`\x0011H¡põ
Ñ\x001c\x0003:( \x001a\x0002¾P@\x000fY\x0014¤\x0003Î<£w"D
µ\x0018\x0003z¸=_\x0006ÃÐ\x0015¡ö\x0014ñ|Þ\x0003¡¦\x000bãîæýo¿øR&áìòcPÍ\x0006­Ã9>Å¥{t\x000f\x0015\x001c(\x0014\x0007ä­Cyvü"F¥\x0016pÀÆ	%\x001cÁÅ>ë5õu\x000e³\x0017\#ëº\x001cBÂ\x0012_(¤£Ñ0\x000e[0\x0002\x0006£Ñh\x0003\x001cËATC© \x000bº\x001d4Ò¤\x0012Û°q\x000bCâV¬1¡¸_Õ\x001f?5R+Kzr\x0015>´¦Ó\x0017¨èh\x001b\x0016\x0016J8S0\x001fÿ¾ý\x00125ÀÑÏà2ßJ\x0007Zã f<^CÅæ<)ÈË|¸71³åÕ4Çß½Kw·à\x0019±tUùæ&fµÌßêCjhê©&\x0004Ä0Y°½
{s\x001e3XOÄÜbÔå#\x0015ëêÝe%Y3ÃÖ°@Ê"óYÀÍN]^\x001dÅ\x0010´»}ñ\x0018Ë/ÿ¸\x0013
\x000fêpQ\x001eîâà'½Í\x0001ñ<{MØþ5v
·ä¹
y?%å'¸¿-\x0019FÀD\x00118[\x0016Àò«ÃÃ ¦»~§¨)z`Â,gRöøµp`¦\x0019YbFHø\èV³¨\x0005.s^ÎbÁ§s Ç$è¬¿Ò\x0001\x0003Û 0aÂ\x000e5\x0011CUÈjllæ3\x000c#ã½\
\x0013æ\x0006]x:.%
ò°5ï\x0008º\x0012Ç¯$á\x001d¡ª4¨¯k4u*Ãûi\x0019\x001d0§§Äb\x0018Å1\x0011\x0001ô_\x000eÑØ\x0019E'®X^8Ê\x0002q¼øµô\x0015í"<
Â\x001e@5¾J­¼&úp'/t¥¤<¯°5Rí±ìíí\x0001sg\x0016;ÅãIÇÔÍ\x000c­¤·dÜ\x0019\x0003Äñk) \x001e/\x001e\x001adb/taiU¶¿\x000b\x0006rñ_>eìîZ\x00198\x0008¦m\x0013Ö\x0003\x0003u¤ñk)ÎùV\x0003F>L\x000e_\x0018±bþBÞxüZh|A£\x001cC)É_<Ï_Ý*\x0005wÁ±­L½\x000cÒÊ6í\x001da\x0018§»z-ï%+vÀÀN`\x0017ï\x00042\x001cÐP\x001cÃAPÜ#=nÕ½n¥]0à<ØåÎË}©á\x0002Ø\x0011\x000c	ë(¥×Ì\x0019XÚvñÒY«²\x0001NPIO\x0013X¹\x0015¯ÉÁjrWt$.\x001fÎFæL¡9cÛ¼«.\x0018XMnñjRÁßätKd±Y¥\x000c§¶p¨\x000b\x0006V[¾ÏÁpèWy:¡(×VuÁÀjrËWW9¥R²þË²ÇéÔ\x0001÷×-vaÓ¦­ÞÝ$¥Sè¶v½\x000f\x0006<\x0008·Ü\x0008ç|4À:ö·IùÈDÒxvûà»\x000fR\x001e
DQ6§½jaî÷Bî
Ëý\x0007i iG\x00119=Zg÷×¯ñ\x001fÀ\x0011_Ka<mL\x001e¸pd\x000cÅ´Ãº^ad 3~-õÅ\x0005ÝTÁRÒñÝÝÐ
\x00160x~¹Á\x000b§jFî¯¥sAîÒ¥¬ä+XÀÞù3£kèx+ãbIaK­YÔP\x0014\x0010¿£V8\x00168½¹Ý¤²­\x001ao\x0017\x000c;¿ÜÜYïç½¢cùô¦e÷é1O\x0015Ú»_P«\x000fw\x0007gÛ¯ó\x0006õÇÄDmFÙU>\x001fâê\x0015\x0005mF¿=8Û¼9¬¡"(^AñåTÅÑÒ³ÜuÎrjÊr_ÉªJWTºJã\x000eá<eqÁy!»èï×\x0005e+(»ü\x0005ú|Í\x0007n¸Øx\x000eÚ´gK Þ\x0005¿
+àÒ/BUÁ®ÇY\x0017P*={±\x00027\iãPa¸L\x001a.\x000e7méÎÍÙö:66ò8Û¼~s\x0004ÕÒã\x0012OôâIÊè$rEoù\x0007ÛtÐÉNvÒ'¶±\x0006±]ËÌ¼^K§J:ÕK'èÞ\x001fZ!Ò«®S½¿µÜ§K<ÝÇí®S£EõSFYPáHÝ¦úôÂ\x0012ÎôÂ	LÚÕa\x0014\x001dI÷c\x0017\x0019\x000býWÒÙÎvÒÉf	ÏåÛP¾kr)Ûd ^<Wâ¹N<%s6\x0001Ë\x0005aÜP5ç½¶æÝxU&}w|Íã½F\x000f
ÅÐèÉÜ%ó\x0013Ò^ÄôóUvw\x001a\x0016\x0010CÂ\x000eçv+\x0017d²\x0013¸W{ÐËW­]Þ¹xc;\x001dX!#½^æé\x0008\x001a¼ëðdµ:dçòpÎ\x001c\x0012]z0ß®d+w\[9\x0004¶Ë#°L\x0000\x00056*uþ¢s$\x001aÍy¼ì\x0004?'EµxáÇÎmÍìZÊ::¸p|¬½\x0019ì\x001d>©ª]
~ìÞvõnÛÅþ3\RZYØv×­\x000eéê\x0001t\x0003\x0018Ýb4/á\x00101@Îè\x0002Ë{\x0015)¾\x001eAß9Î\x0011Æ.ÒÐæ_«\x0010ÒK§j\x000f~ì¤cT´¢\x001d¥L\x0017m¾fåÞkùÏÛf\x0001o¿ým\x001bÞmåÓo \x001e\x0010b\x000e×_/oo£vÉ\x0012\x0015\x0018h\x0019Ýã­áÔ`Ä(ºÔ²½\x0007<}süúu\x0014.yT	&CÊ\x0012RöCÂ¥`4Y}\x0019N.ªh#$#ªdT\x0003\x0003)PKÇ¡¥6\x0004úo)\x0000ê\x0012Pw\x0003
oh/T5LAÒ.©ÙÇ6%¤\x0019xÓÔ©\x000b\x0012\x0005°û13ö¼0\x0013öðªm	iûG2\x000c\x001fÙ\x001aM¢~âÄÚ\x0008 +\x0001ÝÀ«¦BG«=%\x001aè|Ï%E{>ÂèKFßÏ¨
ê»)d\x0018EÈ=#T+ï4\x0000O'\x0011\x0012N'#¯\x001a\x0017¶\x0015X>Å -\x0002\x000eeì9¿W¼ÒPÿ\x0008n´ õ súD\x001b'\x001d¬6\x001aÞ¿Ó\x0008kP\x0003Tÿ(rª
¹Ríá}W\x001b
ïßiD0:´Ó(KÛ¡\x0016:çz7ÚÝCÕVÃû÷\x001aPRÄ¼xëcÞWZà\x0014mµî\x0010eµßð
GxìØ	\x001a´´kkêz\x0015Vø\x001eL%¯6\x001cÞ¿ã\x0008hwêÑ\x0001ò¨T\x0011Þ8­\x001dÐ]OYí8|`Ëa\]ã4]äüò~ön^í:|`Û1ôl,tBÕd¨Úª)î\x001c¬¶\x001d>°ïHm\x0002 \x0002&\x0017èÂl3ª\x0006 Eµím\x0007%\x001clÊ½:#z»~FjÏ\x0011\x0003{ØyjÌRÎò$\x0003&Ü\x001el¨O7\x0003Ë6ÈfñÍ`)©³R\x0014º_MYí:¢×áÞSý\x001bÈ¢¡,ö¶jr²ÚuÄÀ®£s¸\x0007\x001aº{\x0014<V$t"lL;BYí:¢×á"'\x0006ZÍø¸<4ê
Å[Ú\x0011Êj×\x0011#»+´ôÆ\x0015$bl/¿ñõÎ¨ì¹\x0018°çRÑU)t"Àl{
G0\x001cÊ6pRV¶R\x000eØJN],AàngH\x0015\x0003*nÖSVH\x000e\x0018"¦éÌ\x0008ý·\x0004-q
\x0011HÝj\x0004vP¾\x000b/;V»îõáX\x0002?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x0016¶p>\x0012dAâ¤\x0019©5Åbæ@\x001dPÜÈ´Õwë«Ë\x000bÐÅ¶Ãvâ\x0012W´âZ\x001c/ \x0015? iA¸ªÐÄåXeÉ*\x001bYµ$\x0013V\x0006Aâ»¬(ïGúAÿâV\Uâª¯þ$è\x0012W7â:M^h©-5\x0019\x0012T\x0007\x001fp\x0007­{ZqMkZq-µíÊQØAP\x0006 ´\x0003%­Ö´¶\x000bM\x0006ÂâJ\x0000.þ<5MºAÞg+®+qÝWt}ë\x001bW3HSMgÁ\x001càø]I¿ÒØi¢ÍÆEz!Xëêj*9ÜQã)Á)'õ ~£·û¢µ>iÞSd@
AÝ`¾\x001bñÌXiãí<i¼ñMvÆ\x000eKO½Ç±'1e
,ÍVÞÎ³Æ[ß5© íH\_æ©/¿È¾\x0006©äKÎ»Æ[\x001f6uUh.\x0017!\x000b+Ñ\x0002|\x0017âí<l¼õeó\x0006¦C@ç\x0017Úæõ}!áË;/\x001bo|Ú8#OIà³ðÒù¥\x0000R\x0010¿/ÅÛy,xãkÁ¹RÄÈ+9É³p
è<ÁÒ	ÞÑHMå}õÇlçû§ëÍsÕ+,\x000f°¦Y1\x0001S\x001fE?¨ø:<»<Z_-^TÞ×uyÌ!®æLÐ\x0012¨ x»Ô*\x000eÚ4ê\x0012T·Z\x000bÒ!µBPf\x000f%¹a\x0016P[Ú\x0006Ðp\x0016©A\x000cÏrÌ£ì3Ë\x0006NÒ\x0016N_rú&NÝóDRÁRöx®ïµÃÙ\x0006NÞ½I-WI2#­cÞ\x0019ö¢ÒºÈ;\x001b´w¨ 
¨+cnî»ÛÍÇ\x001c\x00149ûøôp³Ëí¬°\x0013e0è\x0014['Úmõß \x0014ýÝÉú\x0010ã"gçgÇ»1E)Z0ÊÁ\x001bèB½(ÈåuûCÊ\x0012R~¥ªT_)¤.!u=dPù\x0004õ^ý¹C?Ëµ§¨\x0001³[n\x0015/\x0010üà«\Òn¹]d\x001fÔ¯l°\x0005©\x00035(Ó\x0018\x0005õ4ÕÄ\x000cté!ìÔÐ~²©ÚÆ/BÍÉg\x0001³E±úK¹-:îN¨gBJý<Sµ-_¦r;|\x0018ÃJ!xj+\x0006cXG\x001d¬ÑT¦êÐ\x001cÖÕÄY4ç8·\x0014x÷ãå~ÑLfªÐ ´RK\x001dVw
õ\x001f>P+:dóçÌX¶
\x000bJ¦TÞL;[ç©Á%XºbýL
\x00153)Þ]?Ý<]¯\x0002á\x000e°`ÙPÝ.×¹n×èé\x001cwGÇG«À7\x0017dè+\x000b|[Èó\x000c±%Ðnvm¥Ì\x0011\x0006ë<¨U]PÉ'vòð»5¨5»áD	'*ár¢Ñ$)à\x00133ªkÙdÉ&kÙ\x000cÎ¤Lªrµ\x0004ÇxÑýn¸\x000fPÎÑõY\x0010)9&\x0010zM£Ä@\x0003äT3ßød'JÊ \x001a÷ú¥¬'³e\x0004C8üç.67wO«õóÏO7wó+\x0008m§?Å\x0004­ù \x001aQãhUaØ`\x0010ÉÅúøôrµ¾zsuqy|:NÇý÷âë_?<\x0001\x001fôf_o6\x000fçO#Ò\x0004\x0015\x0004h½ÿ\x000c,,¬N^Aì\x0006æ¾	Ot<\x00151rídn\x0011Ì÷³«oÞ¬Ï×Wßïb`ð?=üãö\x0013úr¢\x0007çÕýÝæ×ÍÃÓõ\x000crA:Äæ,Â\x000bc\x000fd¤`Z ¹2Q¼:;]¿[_NÌP\x000e \x000f¿þñûóÏèÄ®Û\x0000òÓæùaCkÏ¡âÔÄ[æ \x000f\x0015@¼I¸5<»j3Èwë«óE\x001c0ô/åX\x0002ÂÃß\x000e¿M\x001cÉ%\x0014Ìp­\x0007\x000b2ÏñüÛ\x0017aÿN«èªzþ¾\x0019
®f\x0010wÅ\x0019#¡$\x0000(\x0014¦ðpÍ|\x001eì(Þ¥ÿYÀ\x0010þ=øµA\x0005¥3\x0016\x000eRÓ\x0003pØ¨1Èèí ÅJ\x0000\x00182\x000f¿v\x00038È\x0011\x0000:e¨´\x000886/ÜZÑ;;\x0010î¹qwø|¥ s1i|\x0002\x0006­ÄG!(:N\x0004\x0000
ÚJpí·cáÓ_¿kÊx$Í;^H¢±2\x001fÆI¨@$"5P\x000b(2ç\x001fµ ¤áÆ\x000bQ¸¼²\x0012^%\x0016\x001b{ãUïÔ¡\x0004±®\x0016£0\x000eÂ3¡Xx´#æPì\x001e$á[è¥$Î£ú\x001cHÂ_ç«Ô5>Ü¡©\x0005%\x0008\x000e³|\x001cIu£ÕL\x000b·Ü"Ê\x001eg\x0016\x001ccbñIQÈqÆ[ \x0011qú{ZdîÀ\\x0015Qrÿ»{üã¹\x0014¨·8yúµe.µÉ\x0014\x000e2cE\x0003\x0018\x0016Å©à=ÃõùÑå\x0012p¸b+ìÝ\x0004¤\x001c\x0005q\x001aÔ\x0010èP
\x000f\x000bKÊQ¨BÚ\x001a\x000f`É3ju\x001d~ð*ªåá½
oþOÁFØüqwþ8SØ\x0010w*\x0008DJãÞ(ë\x001d^\x001dëy÷À¾
\x000fÿwÁDXÿíôøè|\x000e-u¶6[´ ­æúÿ^m\x001eç*¼2),\x0003}«
TPÀR\x0005á2;ãGjõj}1ÃÄõ6ð\x0019 æ\x0015¶ý»ÍgôÈÂÀ½ÕÏ»T7hË\x00155qfÃÃÄÒV:ÆîÁüBÛ~ß­ß¢C\x0016î­Þ\x001f¿\x0005Un'«ì°Ê&V§\x000eI¬`î_Øe¬Û}+kÑ,#±Æf\x0019\x0019õqõfóøñþynË
èFÅ-wA«t\x0014J³aÂõT½·-c^¬Þ¬/\x000eÏ®f·¾èA®\x001aÑ±\x0003±éj$\x0004QvB_\x0012újBÏR\x0001\x0017ôÑu	\x0011ÑJZDf&öz	¢ñN«\x0008Ù\x001fà7^z\x0012ú\x0012ý\x0019(Ùà\x000c\x0006\x000f. Ì\x0001éÒ-<¢¨\x001aM\©jôÝýíêuxfEMt¸F³#r\x000b.\x0013X2eÓP
nQ=¨³Õëð:Í®TQIDP¹\x0008²÷e"b±\x0010&\x00129\x0014ÊFújµÈ}ÿÃo¿ÿzý¥Ô|AÿÝ}²\x000c1\x0011A\\x0002yÜ|Ù<ü\x0001(0GÚÁ:¤\*\x0006\x0001H ·\x0005ëõûõùß¾9Y}wÖ1\x000e;Vj\x0007\x0005U«e(&\x0000\x000e
Ml\x0007MNµCíðj\x0014\x0001ß"~,ÑXl$\x001aßñ87Y´H\x0008ßÇ¥Ë¢\x001cÆ\x000bv<1Ã²\x0008,-
;%wÈ¿öø±\x0014ÆRÓt£¡iºI0ZÒ\x001emóõû0ãN\x0002ÆC\x001bçøñ?\x0007sóå\x000fù[:0`¶ÁÇÉfõîaóiç=Êú\x0014\x0004?vdñT/\x0016^\x0016ßgY¯Þ¯¿Þ¦\x000c#¡4~,\x0001Ù0\x0002Ú$\x0018\x001aË<á®%hÁre,Æzx¥"\x000b8lZ\x0018EÃ\x0016YPZZa¢\x001fðô¹FÓHM£l>2¹Ã.$¹MÑì:3<Ýôù?Gsýé÷;ù\x001c+Dì÷plÂòn¾9Üüñ0\x000f£\x0013X7êYPÎã±áÔ&ÇxÐ|dÿÐ\x001c®ÿv>
òÄµº¾þA!o¸Jñ\x0013\x0012¢Þ>?`Â4\x000c³á¡Æ\x0014\x0013G±
& ¥#­ær°2AÃy{u>]\x0010îþxúñË/a«D|%ãgØª·þçãæîÇù\x0005\x0000ÕlÍí\x001dkÃÒ(9gz ×«·G\x0017ëÓ7Ó«äÕ§ß~\x0000­KÈhsËíÙyÚ!ÿ\x0004\x000bÏ\x00015°·8Â)®\x0014\x0015\x0001\x0016
uïø\ÎÈ@þôxýá\x001f\x0001ÉÂÙ´o«·÷Ï·Ñ÷>\x0007\x0014(Ò)E0uâÑØë\x0016\x000exVoÏ®NO'i>|øx\x001fÛ¡Áë\x001f?Ö\x000fw÷Ïáïþó?gq¤\x000fëb\x0015Á\x0016Ò\x0007Qµ	Z\x000e>\x000f*jf]õùéÙ\x0015Ä\x0006&EOã\x0000Ç}\x001d82Jô¹GA?tÇÒ,
@è¡V\x0008$r\x0005È\x0010hj»~úõþwuß\x0013ÍáÖÿõy\x0003%jï¯ïv\}\x001fî;¶@.¶xó!ØDù[pqóÿzµ¢´÷G§S!×\x0000§\x001f>ý`®ãe\x0003uPÆ¾3á¯¿û4®gTR\x001f¬ÁÅ\x0008ÒÔÃLúþÖß~;¹q\x0012.
HÇø¹Å\x0007ÃÔ"KxÛÓ%ÓÜRÝ\x001eL®`Z¿Û;öxßÑÀ^ßÞ?ì\x0014@AÒ(lÀmÂFÃTmx¿` *EÛrn-±¼>9;>ñò¶»0ï777þsÇ\x0013\x0016\x000e´¤\x000c\x0002\x0018DôöèVKcìã¼_\x001f_\@Íîô3öû?níSáÈpîI¸`«³»ÍÇùÝ~^&èC³'\x0013O3dÌ¥Ã½\x0019\zè[v±:;?]\x001fî\x0006ãÁlü&~T¡A1,ÌfAù`(­\x00156Óæ¾\x0008NV¢Ý?þ]Ê\x000f8©\x0005ç³¼	\x001aHò\x001eì\x0010IÉëf öÄD[ÇÅ\x000eT¸ý7öMPB:Î\x0019ï@\x001f\x0016âhKÓL\x0002\x000fR)JH¹ã°½ý»F8"èßn»v \x0004càãíæáósò,O²p\x000fÊq²n\¨}` L@å\x000fäíú<hC¥syDÆ+>¢pÌîÐqñ\x0015PÈ åÛ\x0019¿\x0003©eùù\x000fê×¸,1FÅRìábóð°Yð	ã0 ëóxËHÂ:]ô(\x0014õùùzö1#*\x00151Ùÿ8Öæï/êsáëyµyø°SZKmÉ¥áÃJÉ|áfazæZõµ³WëóW³Â:@ÏoâÇB\x0016-Ð*ô:ùä"K\x0008#\ß*Ì0S\x0007z\x000b\x0003		ñc\x0019\x000c\x000c¯\x0011:íæi¾väaÑÁ²ë\x001fèå01J\x001a?î\x0012ÃÉ\x0001>æ)à&	\\x0017%«Qü²Q7 õ@¥Vü\x0000lýãæv^\x0015mÂV¸Áâ±)Ñ\x001f
ô\x0005GõÅ\x000eèbë7ëÝ8ÒÂ6Y¶\x001c'ïæF§\x0002Có>8\x0004Øqx4Py6Sð8\x0003þÈ#mÊýÆoÎÅ½C<Ê\x0018÷\x001f>ü\x0010Är|5ÓçùýóÇG1£û0K·­á\x000c27VP]¡Ø¦d½ðêðl"g\x000c¤ßï\x000f?~ø£\x00103?m>l\x001ef\x001fð(Ò\x0006¤ÑF¥^?,¬\x0014ÿ\x000cêÀª8ün
QÇiÂ}º¾a\x0005Hnëû¼:ÙÜ<¥\x0008è,S\x001eõÎéN[OîÜ aôµÜÖ÷ju²>¾Hè¤\x001eæ´¿}ë\x0005­óãGxFoîïæßQ\x0001éGØÛÐ\x001bjÁÁT\x0010B\x001e/»éëá\x001d=>»:yÕ\x000b\x001a0ác)M0Ù¥H4B¢û]© \x001fÐûÐÈËi\x000f¨D\x001dcÙâ¨\x0003ä Ü\x001a\x0017\x0007£\x0001:ö:ât=ü~û\x001c¬® >à²ÇÏ·þçíÿ¼Ûaê\x0004Kæ^
Bõ+è)¹'ª\x001c\x0004'Þ\x001e\x001cMUåþuóýø+ì\x0003O\x0002|lVoÀrßaæ0ÁpL×ÁÌÓÀaÂ\x0004úw^¡ûûÉzõfÞ@8
þâoÒçb\x001eE'\x0007ÞõdBj\x0001â\x0018;â\x0018{3ïGøùùIüüÐÜ¼\x000fw~s»Ã"u\x0016­cã´D]**\x0005\x0011f;,uk\x0002^\¬'\x001aÞ [ãø\x0006$ü·¾þ9ª7\x0010
¿ÜÿðÃ\x000e\x0018jÇ0ªæ4ä4$B\x001b\x0003\x0015\x0013}¿½~}>}R
\x0010ÐÕác\x0011ð¤@\x000cÆ± ÆM\x0011H#zyú\\x0004\x0012Îhê\x001a@4yPh\x0010Fà\x0018xM\x0011d2Å?þô\x0011Þ'\x0001)FñãÝÍÇÍÃ¬uÉ½\x001c]
S\x0019s\x000e\x0005.øúêÌ»ãÃõù´­K ¥7p\x0019¥iU±³©F\x0012ÂÍ\x000c¶\x0006A¦Vä\x001f··úOAÎª¨T)\x000c¼¾¸~|ÚíÈ¨\x0010º&Kµ4ñ-Òøb3§\x0007¾ R^\x001f]\Îzs>úüî~\x001e@\x000e\x001eÀäÿOÙTó\x0017\x001a\x0006%¡^#½O\x0003ñ\x0018<Ü83)lûÀ[¯R6Õä\x00158pr¤XcÃá18Äz
\x001dA)vÂqFÕâÄøø±\x0014GpcdÌ4Xï$\x0019è\x000e\x00150ð\x0017~\x0013?Âä\x0013á÷h'\x0004µ\x0018g\x0007A\xäô,Æø±\x0018SVô<J\x001cß
Wn`´TÀ@PX©sãá~G\x0018p¶¥l\x0002+UVÏuû1N!°ô¹ôZ1SÃµ©0ñZ)l\x0000\x0008
©¦y&}Èò\x0017y\x0003;\x0019?Nb{´»û»3£Í@7´]ÚY{ ãÍ
×\x001f\x001bà\x0004½S\x001e\x000f×§g§\x000c	(\x001eMºôYA%\x00150Úå\x0010\x0004w\x001eçLqk\x00072ºC5in~â¿þ¶ù>(¡ÑÝN.®×·7¿=ïÐÑ¹\x000f$\¥Ô2ÒGº\x00053v´z}r|ñ×«\x0019-Ý¹¾þ)ÆD]b§é<>d×»´Ñ°S\x0016½^ê¨rÄ\x0013%T2\x001f¾ïáDÇ\x0007íhNC&,\x0019C¢é³\x000bú&F*r¿Aw\x0007\L\x000cv°Ã5íRþÄê\x0007\x0018\x0012:	ÊóûßwéíÌ¡ý	ÉhÓp4°¤sÃs\x001exÎÂÖÍø\x0013nô¹E£
\x0011XÌE\x0013¢bZ\x0016ùÑ}ù9&B@u@ü(ÿÖ\x001dg\x0008³,¥af/ñ±Ç2² µ\x0006\x0001¿ò÷ÓæçýOÿ\x0011ð |ýûfù)À"Ç>©"m\\x0005N`¬V\x0014eÅ\x0002½?ú·õéôn\x0011Nø{A"iÜ­%<Ú\x001b\x001aÏ'¬@\x0013TYOá\x00085a8j´ûô$ÊâÎÈùÃûç\x000f»VIñT=©
ßÅ5¢\x0001ß\ë>Ý7xvuþj\x001aýv÷ÉCÖ§\x0002í!~}|ÿüt³cµXô?a2!÷èZ\x0011FâÕ\x0017:Zÿ\x0003\x000bùìêr²­G\x0001$âS>\x0012Ùðì\x001aTØàÙMRêA\x0000.ïýÛ\x0005ô£¾ó_£ Ò RØû\x001f\x0017ÄncÛ¹\x001d\x0001ÃSÒÆ-¹Â«bGtÈ÷Ço®¢Â?uÆ\x000b&ðÎÁÇR¦ð¼	
fYdÒ6\x0015Ë3.Q
\x00043`_X\x0014^\x0001\x0010
=-K\x0018\x0015ðCõ(´L\x0012\x0015&ÅF|ò\x0005Ô®½+C¶5\x000be(µ%\x0008b¡\x000c­Úgóz±ÛÿñÅúðû§_\x001f?v#*Õéýó?ÿ¹#ëO\x0008ÈObJA\x0013æ\x0014ÆP\x0012{s5pÈ\x0004¦Ó³«7ëó£¤È\x000cU¤m-^I\x0017ÐACJ]\x001f\x0003Á¾\x0010\©±³¾¥Z*±ùû§/>ú£Áà6Ø5ñèñ×ÍmR³Z/w\x001c\x000c¥ý\x0013\x000ek\x0010½\x0006Æx®ØÐµ\x0018´Þ£wë ©¦ñ¥â[ÃT
õÞ+\x000b|\x0001ÚD,ÎÔ¬ê`Mj¾Â<ÿúax\x000b7\x000f;õKé¬Oõ)é<F1\x0015Eù0?õ°}³~X»ùãú7Ø?\x0008ÔÅXrÿaóüiGH;OC>@\x0004¸\x0018wqÍ\x0011,;=¦E\x001d½Z_}[\x0016ùN#ÁÅHPÔ*/\x0002\x0012£r\x0007WO)hbÖNTÆì*VÉc\x001f\x001b\x0007ï
ZÀÎãÍ\x000ba £J¦ImÊ³¿Ûçr\x0007d>½JÕ\x001ce\x001d\x001bìhr^\x0018ç7¸¡	É¼\x0002Ã\x0013\x0015«]	Ë¼}v\x0012Ç5üñj¡æ¢2A
ÿ?sï]ÇdN\x0005\x0013(,ÿ\x0016[ \x00041¡\x0005\x0002LÐºY\x001d­C\x0012¢ "\x0001	\x001feJ­ê¾!T÷µ*ûo\x0006Iä¹¹ysNXÄ©¼X÷^Ü$KªÜðp·ï¶m\x0018\x0016ëZ\x0005\x0013\x001e;° \x0002;Ö\x0011~wò·K\x0018Ú
	|sþñR ÉÌÓ)?_\x000e¦¬\x0002¡äÂä2&ÇÂ$ié¹¼\x001bT¨è\x0002aÒÃ°¸ic\x001a«>\x0019¯^ pÐxNÈÚ)»iøÌ³ú\x0010W¸\x0003Í$ø\x0001C7Gw·;\x000cqÀ/\x001d%\x0010Þ*fÝÃ¼w1	Þ\x000eð\x0007Gç§WW[L(\x00012ùfÓ\x0011Õ:\x0014\x000c6\x001dÃ	¦m8)Û\x0019T\x0015Ñ¦ô»[ýú»n)PÔ¼øtswóüÛöÐ3ÚÂpÉà]J±'U¢1cußËoNÎO®¿ß\x0016|>ÄÜ~PcI?ÞæÿòÇ\x001då:r,Ò#·9d £\x0005¾Êz\x000b;ÿç«-\x001d~BcrÀY~N\x0003JÂ±\x0004,N"[×Ù¨5\x0006,Ñl¦¬ÿXý¸\x0012§öíÿÜU`
Ð
,=0\x0007ºA¾äè@ÊÏwÈÑoO¶s¿¸Ç¯?µå°ËU1o·wu\x0000f\x0008\x000e\x0006¥S*ÄAE×Ù\x0018¹\x001e¥\\x001e¥Øòtsóø³ÿòkpv
F\x0017i«çÏ7Ûg:RþmHðIÞsI¡b òL\x001ci4\x001c\]_¾99ßØ!\x001cÃ\x0012EÁÉ$<øEY|6=&<ÞcÃ ú0,\x0013MÇó?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ág\ëZê,üÅ$u\x0006­c·¿Þ\x0007SºÊs¡PéÖ[hjÐqBÓ @'\x000ftÆBãØùÿy\x0013\x000cé\x0001i6ä\x0015%¯èå6Vàf¥\x001fy-åç;ò:pe+»×Ä©\x0015¸¼¹\x001a\\x001b±ùòªWu/¯ÆÁÄëPÚG\x0018O"9óSv:xuÉ«{y¹ÇöWàey;(7M\x0011?ÐDßÄkJ^ÓË\x001b\x0002SjcÐ´¾Ö¢.?0ö¸×¼¶{ÿzÐeI¼\x0002s\x0006Ôâü|¿n\x0007®/qýÀqóK½\x0017zê\x0011ÙhóòÚöv\x001b_© ö\x0013ÅMòVa,éölµ{yeÍx·9\x000bæÁcoAÅ\x001e\x0002¡¹e#ÞÊñnsf\x0018´Ä§îx¼\x0012gÆit²\x0011peÎx·=.N¹É*=\x000c\x0017´L\x000ei4ñVæwÛ3«qCÀlt\`A\x0012!\x001aÚ\x0008¸²g¼Û I?©S¨c×wÒå9¤ÕÄë*^×½£WK\x000bÌó(A'ù´À´Q+\x000bÌ»M0Èg\x001d
ïAN8&Ï¶·\x0003Ê\x0008n#¬u~*+^`Ã\x001e)Úø­Îÿ~··Æ»þE¶h&Â6y\x0005V2ðCÊ¢maOí]>4å»'ú\x0011Y:Ícf1ú\x0011$y4zúõå(üE©\x0003ý¿ÿù_§\x001fÞß~\×Ë)ÅÛ1Qô2>æØ.V£ºÊÑéËgç¯\x000e´r\x0012¯(yE//\x001bÓW9t\x001fKM¸æ»kÁ%®ì_^ÆØè\x0010hfã¦\x001c.¯ïçnçU%¯ê^^\x0010£³yy-
xY£õ=(3»W¼º}uÖ¯ëëx^_¼Íõ=¨ µWÛ\x000fì_¥\x00152\x0018\x000fKÅh}ç\x0007§¶óVû÷o\x0008OOFËüT\x0013Î\x001b\x0016X;_\x0001ô\x0019ðlë<ÒNÒÑ8°~ZO¢`ûfë °0lßakÆöÍ\x0003Û7\x000f?Þ¬JóÝ\x000b±p*\x000f"\x000b¬KNÎñC¹\x0008ÀýæìÐØ\x0019¢U%­ê¥Õ\x0006]²\x0011êY?tzùaUÐÕ°ºÕÝ°
+!-3ùi6ÀRÁæ¡{\\x0003¬)aM÷>P¸\x000fÿÂ\x001cD'áø¡ ¡\x0001Ö°vd\x001bdUG\x0008-n\x0003\Z~èJ?Ñ.\x0019=z@u½¨&\x000eqJë\x001a\x001aÊÓ+:_â Pßêõ%­ï¥\x0019\x000bi]¹AðY\x0007\x0016s;âPng=,g%,g½´ª°\x00066)lÀ\x0005ÒÑç|Õ6x\x0010WT¸¢\x0017×ã\x0004yOÒÆ,õ6¶WæwÛ\x0003Çpm-(ÖdáT\x0003å\x001c \x0008[G+ª°ïu\x001bh-^àÁ  _ 	ÇçÐWãrµ7ù&üEù\x001ctv}³[§9Æ'©e3Àá=\x0007/ÂgÏÏN\x000e](Õ^l\x0000²SðcgËcÁp\x000eÍ«|5rªSu­gØ§v²¯iiÔ
ÓjäÔ%§îáÔkv\x0002ÆPÎÍ\x0017Í4B\x0012Òô@`Pæ«¢xU4\x0012ç\x0010Û:à«9mÉi{8
\x0007íØÈi
¦8É\x0012eÚ\x001e:í«1]éz0ab\x0000b
´¡Æâ@\x001dëæ\x001b\x001a9}Éé{8½¤\x001b7<÷&Ïd\x0019f¬;\x0014£¬å~´¬kAÅ±Ê\x0017AïÆMCxÍ\x0001§´ST¢S³)¡\x001dÖïYA2Lf
Ê+ãÉ{¬§\x0016¢þpµÎCÁ¬²\x000bØâ\x0017_mPÞµC¹\x0004}¨ä5EVÝ
VÞSìtHêý\x000e­Ò°iyØõ¼ðì)MûÚ]\x0008R)e±ÅNerWvâþµËËô^ð\x0014þ§û£§»÷·«\x001a¯â+B\x001ed\x001c&ÇD1\/b¾9zzòìüdYt0E)z0AKOãðATÑ\yUFNYrÊ®åäØÇ\x0006u3"¿\x00148Ku\x001dó
ªäT]ë	44/Í£,¥\x0006\x0006-%ë9uÉ©»Ös:F6E8Osvô\x0016¿tSBÇ»¶ä´]©¡¹Eãa§²\x0003±èzNWrº\x001eN\x0017õëp¼\ÎE\x0005×FÉ\x001d\x0018ù³Ó¾ÓrÌ¢ÃD%\x0012´4íÀ«ÕjÌ"±£\x0018¯u=¥ß;3øüCÅP\x001b,'¯]Q/rzäð\x000e"%ÕHz½1}\x0018Tx^ûÌð\x0017à3Q»2eH^Ýÿ|õ~M$üo\Tu®[£³Øf¸à\x0008\x000b\x0003\x0017Ô¹bê,`	IWo^>;4wÃóÚ1\x0001³ìg\x0006a\X¤¹>&1ó,­\x0017^R:±°ÌbÙâk vxÕ\x0007f|\x001dÖ­3¯Ö÷/4gáÞ;yl	G
ÕMõü¼¡\x000ehíJh8"ÝÐaK°ÜGn}%\x0013.VXedô|Ý\x0001mm	\x001d~ê?:êùã1ô2m\x000f/é\x0018Î\x000fiæ¼6\x001d|Èxxü
ÔÂeã!	z#f¥*æØ8ÒË+ü g ó2k¬ù\x000cÝÙB;²\x0010Õ2Ãý¶CY\x001cÜ£R(\x0019\x00114>k\x00199_wßCmkê-\x001db\x0008\x000cfùòhÄ\x000clø§ù6vjYSË\x0011ê©oVÝí´\x0011$è,õFÖCèjSÃÝÔ0V
\x000fbc\x000cg@R\x0007\x000fâüÌvhÉX	
?\x000e@³	Zæl	Þ¨\x0017ú¸Ú©Ùº@
/jÝÔáÃ-¤ÅÓ[¨ÑÊ`ð!æËd:¨k(\x0007"³\\x001d\x001bCâ*é,*µ=á,nµ«\x0005ÿþûï\x0003¦OÆF¿¸GD<\x0011L\x001f'#2ÿÜÔ\x0007þ~\x001füý\x0000¸&±õ\x0000n3·ð\x0005÷ûÜ\x000eXmêR\x001fólµIì\x0006Ô6ã~·Ïýn#\x001fù¹Ü(z\x0002êíSÿk`µÝ±¡ÅÖy(EÇr^î¾{·Ï½\x001bZmÇ§\x0016Üo\x001fðïoöÁo\x0006\x0016Üõ\x000e+®r(¥èF#ç+YúÀØ\x0007ÿa`Å
\x000e¬\x0005{âL^q5mñíÜNù|®\x0007þª\x001bÉÓë<'Ó\x0018ÆÈÓ
WýjÕ¯\x0006V]A+®º&÷C\x0007t6ÓÇýÓ>÷O\x0003Ü\x0002;;VÁáOÛ|£l\x0003ÿ¸\x000fþã¿WnZð¼S4vÜlºà×ûÜ×\x0003vÅc\x001f\x000bØ\x0015nÓÐz\x000f²Ìî¿ÙªÔètwÿûQDµ®\x001f\x0004²¨¹X2ìç< Ã3Ã)=TOqtzòæ\x001fGq(ÕÁ\x0010»ÿxfYÙÞJí´G\x001d-\x0019.=&kÆÒÎÖbyQ;µ,©å\x0000µ%ÚêÜ\x000bà9ºKÍ\x000ewò¶A«\x0012Z@k¬X.êm$hÃÀØ¡Vj]Rë\x0011êpÓZ'e?Ïi\x0019?TØÊlJfóµlj[RÛ\x0011jÕVc\x001f\ ÆXJ«-wµ+©Ý\x0000µS¨a!%^p<·Ùê)s¨6¸\x0015ÚÐ~\x0000ÚN\x001bDÉ,Ý\x001a E¾\x0006/Åê.Þêl]ÕNÍÁ­Dj\x0013_\x0012"µ\x0011¨»0p¬\x000f»ö\x0003ñîk^9F>â\x0019­\x001bd\mJÕÆl¼:XHÞ]yF>â\x001a¿èjW¾8G'²L \x000cWJ4"\x0018ï)s¸º¸
ºr|Ä7~Ñµ®¼#\x001fqÎ\x0002k\l!rc­ç\x000eßN>¬ãÓ]¹G>à\x001f\x0003!ÊÍ`û'ó\x0007¢\x0002\x0019ÏÏ±ìÃ®ü#\x001fqÞcnG2Û®=÷*\x0007«jáÝ¦\x000f»ò|ÀE~ÑÕ\x0016\x0014\x0003>Ò3Ç
î\x0016[0Zl1ÿÜÔG]¹Hñµ¸HQß\x001d\x0007\$È\x0006r\x001câ©r³\x0017a\x0018Å\x000e«M´aW.R|-.RT.R\x000c¸HÏ\x0005FÚáVÄ0\x0019\x0001Cí®­Ø\x0014_\x0014\x0014\x0003NòË®vå$Å×r\x0014\x0014\x0003Nò®6\x0013eB>%ÐÊzþÇn\x0010ûRx"IáQ\x0015æ/_ÿøáê~Õø\x0012\x0011®èÐÊ\x000bÂÃLê|¿qRæ\¼áÜ\x001d~AÌÏ¿yyúæ|\x0005µ/©ý\x0008u\x0014æJÔ&
­²ÕÜ:\x0017¨çU@º¨Ò®¬×-³ÀnÀ¶Ø\x0000$EN\x0018.æµÐú°e-G°EÔ¿Øþk,ºö}ø©ZWÔzÅó\x0008Ôa\x00078´ß õ\x0003Ui-Ø¢Ú#bd\x0018\x0003ó\x0018\x0012¶ÆT9îhÌë`uaKVbK6Í¢Ê\x001f`k{Ìs!9çx"å|\x0013^\x0017¶©VÛ\x000c¬6³\x001eå±pSÐYÚçþ\x000c\x0013¶þf«úDª#É­ÀíPó{{ÂÍ\x0003uÏ-Ø¶²Úðc?v`\x001d\x0019óüÇ¸Ú¹\x000cÐ0¿\x001d¶Àx$!àéß%*jEluì37\x0013Ä=¯ÔÅ-UÅ-ÕÈ.qøÐî\x001dµÆq¯òî\x000e»ÿp½T\x000b·q\x0015·q\x0003ÜÁdÍ7oâ¸ÈÈí\x0018§Ï:tq{Qq{ñuì\x0013\x0018YÚn1t,9\x0014ÇÇõ\x000e¡kv\x0011<?Z\x001bæ6¦¤ª\x001b~ìÇæìX§\x000c¦ç\x001ad\x0018ã6á\x001e§Êð
ÍTUýN>UýNóé´ØRá\x001d>_\x0002\x0018®º} ¼a\x0015>\x0017ûÒú¤õ¿»Ú}8z²ûåÓõÝ'gp³j\x0008ÿÁ¬¸´v\x0012]¼¥}wzòòèÉÉëËç\x00170ÏàìÕ®,D\x0017%º\x0018D÷XÐhý$\x001fèH\x0019\x0015r[²«]
³Ô¨?v®ÿ"tS¢1tiPsÝAö;/»W¤\x0001=_9ÕÍnKv;ÈÎ±v×ñé\x001eáp$ª3\x001b²»Ý±+ ª-¤bF[-¾pw¡û\x0012Ý\x000f.»Ç\x0018 N´Î÷ Ïè
=è^
ØG6Æ®Å´e$&U\x0014ÉN\x001dÒ2î¯û uWÔ®E¼B'xlµõ\x000b3Çºá+óÎ\x0007í{¸\x000cÏm\x001e~îÐ\x0004¿)º¬Ðåà¦Ñ(c\x0013E»}^w*ãbYÅ¤\x000b¾rM|Ð7uÇ9äaÓd±°î¤8¾,Þ\x0005¯+x=\x0008/ók¡\x00136O¤\x000fìhhÄ|\x0006´\x001b½ò«|Ð±Z3Í\x000fQYV=%í¹¬yÕÅ^ùU>èXCüï=++M~c;SùU>èX§2_\x0007ÆÞ£v'\x00064z~Öq7|åYù k
wê<ï2ÀfT*TþÀÛP\x000fº¨<«\x0018ô¬Î ÔSÙ³y×(çõ²c\x0017{åXÅ cu\x000c³1°g8ÊfÒä\x0016½¬¼ß\x0005_y'1èÄ§9XøßU\x001aÛJÃÊo\x001aÊÀA\x0003\x001fv
4ÁÖ`©Ç-oØ¦&^T&^\x000cx/	Þ³cM<Èq$x7/\x0008Ð
_Ùx1hãÃ¶ÁTâ1ªv÷vþ\x0011¦\x001b¾2òbÐÈ{AW\x0000/²§YVÞn\x001bÔÈÊRÊQKÉY\x0001ãH\x0014OiTtI\x000bü¼z7W1¼\x001cá½/`\x0017\x0013N«Õ\x0017;0n§kÙ«@X\x000e\x0006Â\x0001>g®§YÒ=?1±m\À|%J\x0018oÝXÄÐ}ÿ3¸üpÊ\x0013+\x0014ÃZ~¨£Û6.Ûÿ\x0004î¿\x0001tò\x0005\óÉì`-_ÓÞ=øì\x001bØð7ä\x0004&\x00114¨tåû 
zsÛ¦YÕþ7¨áOø²\x0019K.?û-ÈñßÁ±\x0003ùÖ\x001c÷)\x001bb7{¤(\x0006j%[º{ün@\x0004;T%Ñ \x0005h'77W©êõÍîÓîÃºR*\x0015®á6½gBy¬1:·¸¨8\x0003}rvv©^\¼<XH]ìºÃ
Ö¹ìòN]Aâù\x000e¹\x001eb_\x0011ûnb&¢\x0004bísû¸3¹ùÉH.f7ö\x000cñÁ=!y\x000bï¶}¥©M71g1ö\x0005b¸uä\x0005X\x0012\x0013þaöèu +]"Ã#óc_dU;õ\x0015;Y
Ì[\x0003þ¦wHwÊm|°;\x0004íÙ0«|_»X$íâ©\x001fÿ"\x0000}ºú¿N>|¸úôiÕð\x000f#C`îynt\x0010`éÑCbo\x0017áçàON^¾<½¼<$)°¯\x0014,RðWE_È\x0001½\x001aÃ×~*\x000e´
\x000bc\x001ctjå*»\x0007ê^ñMoFñuT,ø\x0002ßô\x001cÎ"Á\x0007y\x001añ]µúntõa||®ÌtPy\x0012é%£¢ãy¡ñnzÏKzÏ\x0007éCøgóâ\x0007Þ$¦\x0001\x0017;Üú|>ïÛÏh0Êþ²A~#¢pB¬BV8#Çq¥L= ¢ÕÈ/ªåçbtýEüBn\âW\x001aðæ\x0001õF~Y\x0019Nøq_Ûã¼}à:Ï.Ã¹Ä©\x001añUåµêjÙ.ü(jó|ÖuÖ[âßÖòsSo3ºý¥D\x0005lïiý­ÍÓ\x0018
³|[~[¯¿\x001d]hèv¹ÚÍdÑ§Ào°XÏÌ?èå\x0017¬ZÁF×\x001f4±s¤á8ºÓ*µjÛõ/åW¿_íàgSV5l¥\Öa¥Aþx³ßV¾\x0017~\x001câ)T2ï4=3ÆË\x0016[~ÂM~Ûõ¯½¯\x0018u¿0.OXð0üGæë¶Áóû *a\x001b¿ÕúK9ºþSµª± «\x001dù©/©mCOð]ñ»A~f§óKÑá\x0018ù3=?sµ_Õüj£f+ÔÄc6YÜ?ú!µ¿F~#*~#Æø%4tfûciÚvÖÓèSÚzùíàòÀU\x0019_ã\x0000
m5\x000fÚn\x001d}Öõæ)\x0002­õ"{ÐX¢8\x001d!\x0015òóùöÏ`~_¢ÎDÝß?~ø\x0014®Þ^_]ßÜ¬"géò\x0015%Òd_NRþ-OTùû«áÓ£·ÏO­V%´\x001aöð`fýiLòp !ü\|»o§Ö%µî§æ!ÒWy\x00128ùOàtj+\x000cÚ¡M	m\x0006\x001aÆ%ûh\x0014ÅÜâ\x00180{à±¾ÚÔv`©\x0019)sjç³\x0008±öo¸­\x000b
2?iu-¶Ôø6\x0019\x0002w«Ë¥Al¨&Û
[ùê4ú\x0001lhnÊ#B¡//6Ös8¶,\x000bÓLmª-b\x0006÷H\x001eù`Bäk< íùbMA+6¯\x0008üØÏÍIØ(ë\x000cÆrn¶ØWVó\x0001;Âa?ç­
ÌÙøá{i¸ðm-jl1­±ÐÊp\x0005\x0018\x0003¶ÄIHj¹>¯[ÕDl\x0012æ-'_CÛàY±<x®Û×Ü\x0003¦ë@\x001fÉ°6\x000cg{Yª¤[Ë[Ë1\x0013¨3·e Ûl V»[¶<²ÛÕ\x000eÇx\x001c9%Ä°,{\x001c]XÆoæp¨[å\x000eN=ßú5tM¦ÕÎÈ-Ö>¶3ëyàH\x0010B¶Û:øy»±âÅX¾áR»\x001aÛ]\x0010òØwÍ<ÞÐ¸Ó¨*¯æ\x0013Ô]Üµ\x0005\x0014#\x00169CËÍ\x0004Zî\x0010÷Ñ¼¯eíÜfnÍ+nÍÇ¸Eà
>¥»
ÍNØÎÁ\x000bW\x001fI7t$\x0005doq¼Z®
ä\x000e¯7á\x000e¼ÙõFøÊ\x0002Â\x0003û[À}\x001dÅðÓ|ÆpÁÁý­ývë-yu\x0003|è\x000e<
¤\x0012\x000e;\x0007&emç»ô»¸eµÞR¬·ñ0·5i¨cíIÞ%\x001a
¥6£\x00165õH\x0004¨34Ê\x0008mHÌ,\x0017ï6cÛz±íàbó¬üëmP\x0011¸AÁºí·´õæ¶#ÛÐÉðý$Aa°\x000fLå¤vnWs8K¸Hf\x0011qk°\x0017\x0007ßÜË²­ÜªÎñÀCÆÄgnÂ®ãöó¯X¹©©\x00167e§v\x0003A\x0015Ã¡¯ÆúÜ¸\x0016>\x0007ç\x0017³ù×Ã6n¡}s\x00056Rv=ºÙ\x001d]îîÖ%¡#çâEÉqI¸zät½°Ë¥0xåäèòäâpÛ×©Ö('×Ç*t4\x001e£ÚeÎ²\x0006Öå&£&VS²ÎuMêý¸®YO^s·ñººÕu²jTë¬8õÃL¬ËC·\x001bXËB!_ÌFhÜ\x0004iªòÞÂ*b=0Ëa=ª¨VçÙâ\x0016ê©fÕf'í¹Ôx¶ÜrgG	»Pwíö\x0004Â_L\x0013\x0000ôíõÿü÷í*ÒX\x0018»\x001f¼ÂW\x0017%HêÇÍ+CM¤Áf\x001fZV·'ñ\x0003°¢\x0013GéªÔ0Ã1%#)Ð»	¬,ae'¬dÔÈ,\x001d\¤Ro\x000cuuÊåF\x0013¬*aU/ìÔü\x000b¡°ÊZ,$p½n\x0013¬.au/¬+¶·+\x0015\x0008Q%®¬RÛìYSÂ~Xl/â¨\x001e`
­ì6¬¶dµ½ÆQSa`\x0017²ª
.ìò=®d=lµ\	êú·kGî\x0004:íJb$f-4¬ª/a}'lØ£(¥L\x0007æB°Êl²\x0005
'ëôm£u¸´\x0006ôj2-ÚX1?·¶ö^½î\x000b\x00164Ë_ÍËPþ
õÄ½Z~]m¢­Ü\x0017ïõ_Ê\x001dË¼\x0013B0ã\x000c
/a«\¾»7ÑVþ÷:°/\x0014\x001aðÊñ^\x000f¦Ádrr[6#\x0007&Õ6Û¶r`¼×}©¥­¼\x0002ïv\x000b_¶r
¼Û7X|ÿëG%BR¿óM\x001c­´¢2·bÀÜæ\x0002à\x001c8î[LÓ\x0004ç°
menE·¹Õ\x0018C¨CÙ;\x00124Õ&Ó­\x0010D}Uè¶µ\x0016§p:å'[Këºü\x0006Ð´®ñ\x0012½ÆËÈ)D°¨@©$\x000ez\x000e»`¨"ZÑ\x001bÒéi	\x0011c¢Åw
¯\x000f
\x000bm ­ìèµ\x0007FOºFÄF$Å´óM9­°²2\x0007²×\x001c\x0018ãÊÕPÎ`\x0005Æ3vë¬Îì=cÆ ¡õ$=0	ÁÓÕ\x0016´Õ!ÝÌEp\x0001<Ãúâ|gb»\x0013«ªz]%vÒcos
\x0001\x0006\\x0008t\x000eh\x0015æ¬Fæ×¤ð\x0017Húæv÷aÕ\x000cïTOn\x000c\x0016:àt.\x0003Ã´°5\x0016Wöów#¡(	E3az(0â3\x0005JÔ¨ã£²$í\x0006UM­eD¨\x0014\x0012:1L¨JBÕN\x0018ÌQ^BZ\x0012BáLZg¯k\x0001u	¨\x0001ARÕÐ6Ì\x000fBc½³Ë\x000fk	MIhÚ	éÈjq´@5LgÆÏ-\x0001m3 \x0004	Äç1ý#¬ ¼ì|Ö\x0002º\x0012Ðµ¯à´	
v_±¥\x0015\\x000cÖ\x0002ú\x0012Ð7\x0003ªX¾K(sñÓ\x0012.>T­$,t¬ÁZ³ö5ôXn5§Úÿ\x0010\x0008á"ªÑmÈkÒîQB\x001eEÓ5Cx=ÅkÆZÄÊ£ðv\x0002
ê\x0010ó½-Ä\x0010\x0017càµKáí>%\*¥Ós¦àÊ\x0011\x000b×"V>·;\x0010Õ\x0008G«\x001dâkn>.£OáíNÅ\x0016k¨ñ\x0016)ùd³íðy®
o÷*Ja\x0007R°ÔäU,\x0006áN
\x000e¼r+¼Ý¯X\x0003\x0013!0þÂg\x0016q97·°ò+¼Ý±hu`\x0014ó\x001azÅ\x001bfyRöZÂÊ±ðvÏâhr¦Õ\x000c×Pä\x0017eí\x000eT«­$\x0014c\x0011í%`ãé¬ ïów^~¡_X9\x0016ÑîX\x001ce.¬¢F\x001b\x0019\x0010\x0005×"ÖWvÇ\x0012Â\x00065ý³ðVq°ò+¢Ý¯xÅÅ­2\x0018?HÕµn¡O¶°r+¢Ý­\x0018Rr°Ê$wò|ÔJjç\x0017­E¬\x001chv,i¬­ÃÏÂ\x0002ÅåßZÂÊ¯v¿bIaÕ*É\x0007ÉÞî÷\ù\x0015ÑìW¤pdµC<\x0015;4Ã·uH"VE´;\x0016KO~`q°VnÍË\x000f~k\x0001+¿"ý
lÄ<HÚæó°\x000bi\x0001b+ùdåUd»Wq¢°6^íû=í\x0016s`k	+§"\x0010
Uÿ­¢\x00067iÉbëeùöµSíN\x0005*ÐQÖ8\x0002MGyÔ\x001eÊ:ÿÕìT@HØ¡É¦7F9]õ²ðZÄÊ«Èv¯âi\x0002U\x000c=¤¶âòXµWÍ^å\x000b\x0018DY¹\x0015ÙîV¼"u\x0011Ñá\x000bT\x0012/Î\x000b*--[Ín\x0005Þd­"£±¨n\x0003z¹ºh-båVd³[\x0011 í'C;sZE¬^\x001e­³\x0016±r,²Ù±|½¨*Ë­:,·&ç,-eH,]LÕüHë\x0016ÄÊr«fË\x001dÎ\x000bvO\x0007÷\x000c
à	M£\x0011ªL·j7Ýð®&&Ó\x000fkô4 /Ïª~»h6ÝQ\x001aü¢óÕTª)G2­SéVí\x0017\x0002Ë)Î!íËéM=,â¨ÍQåVÍ;h,UEÄ+£\x000e\x00175\x001c©Êr«vËm5êÚX,¢Pö¡\x0018µª2ÛªÝlKzÓØ"9 =±\x0016±2Ûªý>\x0000MÖ¢Y7¢R\x0014å.¢®n\x0004ºùF\x0000îyÚTO¥=a\x001fF\x0010ºr,ºÝ±\x0014 ÛâL)ÈY(»\x0016±r,ºÝ±@}\x0014ú>IÃ(¦­¨G\x0013ºr,ºÝ±x³mÁ&fm-e¦;ÁpÀ­+Ç¢Û\x001d\x0016\x0014Íªi\x0011LÎð"Ö¯âí~Å1¬ç&\x0007­"ÝNÕpBQWE·;\x0016íPØ+\x0006³8\x0017ÕÉ\x0019N×éÊ±èöL\x0013hù[:Ð9
¡ëé²øÎZÄÊpëöx;DÒÐi±9\x000cóôT¥ßLe¹M»åvþxÚ8wX[O[q°²¦Ý*zOÏºa+âi1~º^ZLerL³ÉFO[Åò>ÄK\x001b\\x0007L]äÒ|%LtÃ\x001brá´\x000fí\x0014ã\x000c/a\x0015æ0LJÇ\x0001C\x0000>§8vY$nõï¸ñ~Ë»æ_³Á`+'£è\x0019-#\x001bu~ÆìQvJ(ºâS6\x0007×\x001eÔ\x000e\x0014.¯~P«f~¥G5,¨ly\x0013âô\x0006
\x001d\x0002ùYmzÍXØ[[:Ä÷Ay\x000fg°dôXÅ&AÜ\x0019®\x001eÀ¯­\x000fþ¥®±)B¿]}¸O³mN®o×
¶\x0011J`tkBèã2IJ­V«Y}òöôå4Ùæäùù¡±6HëJZ×I+i³\x0011J8\x001cVÚAÎÍ´¼¢å½¸°¸<Ëüi\x001c\x0000\x0013\x0016\x0017µ å|QL3î\x000e\x0007\H÷â¢êEÀÍ³k%ÚR;/Ò\x000c;å¨X|´è5,-Ð4ÅD\x0015Ç æõÍ[aaèW¹\x0011L'­ä\x000eohQÉm9QîLÎÛÖf^_o\ß¹s%x]SV\x001e\x001cÞ¡öªaó\x0007­¸¢Pb0õõãfá>\x0015\x0000qX·ÅfgíæUðyUes£\\x0017¯`¹8W	I}¹(5¨\x0017ÆZ5ÓÖtÓ
¼À\¬\x001d7m^­çÅymÍk»y%&7%h\x0008ã\x0005\x000foOZÍ«}6óúÊìÂ}¼àxqÆ\x001dK·=¥âóùâV^¹ç&zý\x000cáWÖnÚÐkÀfóÃ
y\x000býCà$V\x0017¯uè¥¡YN\x0001S#ï|©ùz^%¨¦ÆLPP
W÷b§ÐÛë\x000f«&Àrß°4\x000cã !H@u\x0001ã\x0016RÊ¯Þ\Æ6¡·Ï_\x001eZ+ö\x0005\x0005	\x00027
\x000fu éví "!ÉâÀ¤ÚdrU8eóÑm\x001bëì¬1ÛÓ¾¨*B\x0003U6\x0008áÂÍsk¼íhcnÛ5^·\x001f\x001f«ÚkÐ\x0001eòrØØÝÑùÇ»«ÝýïkhcÅR\x000f\x000e½Nq\x0017\x0013BÖr¡(&T\\x001c¿º8=yóMIlºÃ¾ÍUàPTÞÃ-\x0007_¾bÙÞFÄ¾$öýk¬\x0011ØçK\x0004\x0008q\x0012ð¼ø_\x0007p¡:¢R;Jï\x001a{ÐuKÈ"k\x0012å</EÖÌ+dÞ¿ÈhÎ\x00022v\x0016L+!Ï_ÕzE,úÓLÚÌs\x0017D\x000bVy«³W¨Ô¾ÒlQ\x0015\x0017V\x0019÷²aVy³½¬*d5báò\x001b*¬r*f\x0003\x000bÄózÏ=ÄIæ\x00036Ùc¸ÃAØ!ï\x000b­RÏ±éA®l2ï7ÊN\x001c£½yiÕ´È³\x0001p\x000f±­m7±g(%\x000bÛÂ(:|\x000bW\x0011»þ5\x0010úâ"£µÀ&79ÿDÜ\x0001,*,úM2ô&àÉÓùU\x001b`2Éz+/"*O-ú]µ÷X³\x0002ÁÉöÍNÖbþ&×¬*_­º}µa$¿Æµ \x001aµTóÕ\x001dÈºr|ºÛñ\x0019cð¡\x000b¥#­Ñy8¬\x000bcÚ9Ûú98kÌg·Æ*bïÔía®ã\x000bÖ¿ÎZ\x0011sª\x0017Ì
NaÌäVÌµcÝVÎð>wP@ªÊ²Æ`G4ØÁ÷¢åþpÙ2Oûó\\x0004eÃßâ%
òû\x001b1×{£?ø\x000cV\x0018\x0007/q!rBØÏzÚÏ\x001b!zkî­aÅqØÍËÕ3mv\x0004eåOàÇ^f\x0010öSm¸µÒ\x0012³Üê\x0008ê:ÓÝÁ\x001ct.ç\x0013È\x0001á\x0019\x0019\x0013\x0018\x0002äR7B®Y÷/³²tûcæ8#ch$\x001eõ¾ØÖÙöofx	ÍÑ\x001cãy4¨µ)dÞÊms·\x0017ö3\x001b½\x00180iIe;gQ
B,¼Ò´3\x000bYÇ ²;\x0008uaqs1s2\x001aX\x001cí¼<q\x000f²©»Ï))nfVÂë~bÆÛ0óJ^=ÌuÜÜoç\x001c³ÓÖ`~Á9\x0011ÂÎW{w\x0010ëê
?ö\x0012\x0000Ï«¬Xa\x00070óC5;M½Mÿf\x0016¤h\x0003óÒ Pëè\x000e(\x001e\x0018*¿\x001eÙï]¨ú7øöÈùÈO"0:#/ô\x0012¶3Ë:]\x000b?ö2\x001b9^\x0001ÇÀHèùÇÝ\x000eàz_Èþ}áÈ5tL\x001b¨\x0005d¯°»K¨yÕvdU?;ÄwØNdi²zTØlÇ>e3<õ¯\x0008ñÀ|õ\x0015ÈáVR?êA~|ï	òæuOkª-\x000fÑ~®9æTëä|ÉZù\x0004yöúà)ßàÍã\x0004ï\x000eZî½ÄîX\x0003z«©>Ñ;¤®ºMheI+;×6Ý§ãÚrOãqBMZÛ­hUI«zw\x0002u\x001e\x001bop¦;§Ë\x001eLIßV´ºwm-\x0014ÿ$A"1jB\x001f|é_\x0007kJXÓ\x000bKò\x0002lJ6iò«íÖÁº\x0012ÖuÂBm®	Y\x0012y6R´kç\x0006Úi}Ië;iA5djéÏÝµ\\x0013­ïôn¦-¦ó4õ¼\x000bW+ð	©@X\x001fËTpÍ¡®ïù¹¹í¸µsèõ\x000e
\x0019´éå^p\x0003'=(¶\x0011må\x001cxw\x00101ÜÝW\x0000ãTÔê\x0016\x0002ßvÚÊ9ð^ï\x0010\x0002H?uu1U¨i+lä\x001dxå\x001dx§{IÕ2w¨Ìãdp\x0007MÌëv¶ãVî÷ú\x0007hÚÌ[AbÅ0WpâF°{àþ\x0001¤s] ñ4QiÆ=Ä\x000cÛàÚ
×ö³©G[y¬\x0012å4tÊKó×áVþl¿Ø}ýêê\¦bò>\x0010\x0012«'¬÷Û·¼rf¼ÓñàpsåD`E­sAZç\x0001w\x001b+*o&:½\x0019F¥\x0019+±ë!\ \x001câÎ÷q·ãVÞLtz3Î¦x<\x000erI\x0016´Bôüä©vÚúªÓéÍ8´¸å}\x000bÓxQ­\x001bofÖ?\:¾\x000e·rg¢Ó`\x0018ûc÷ZÉ¶Ú\x000b;\x0013½îLh¨H«+@ %âjÔq°NmtÒ*w&:Ý\x0019\x0007wF¶.(Êã^ØÆÊ^¦=¾\x0001\x0018I"V&§AUã6¸?\x0013þ\x000c\x0004sPn´#\zµîá²üu¸?\x0013½þÌI\x0018¢\x001a\x000bqÇ*wÉQ\x001bÓòù2ªvÜÊ§^\x00164÷\x001a%1g#¨ÇÔÎÏo¦KÛoØYM\x001bâ¯\x001ck@U=)Ì5~¾±¸\x001d·ri²×¥\x0019*E2ÒÓÄ\x0004\x0012rµfþ\x0019¶\x001d·òi²Ó§	æs"D\x0007j
£1³ ­ßN[§ïz]\x001aLeÏk\x001bnYß\x0015«\x0015aªÏ6°CÛï}Y\x000b\x000b|¹¾D3\x0019S\x000eG\x0010\x0015-ëp+&{\x001dZ\x0017³HQØ¢` ÒêRO§\x000blÇ­<ìôhÁ\x0019ä;f,?ö8%p&°\x001b¥\x001beåÐd¯Cs\x001c÷áQ7-{\x0008\x000c\x0017Ô¼H;nåÐd§CS SÛø\\x0008nÒÖ
¾
{PùÃm[ëp+&;\x001dZ\x001dQU]úZ\x001aÅ«ì¼zG3­ª<êô\x0010Áæ¢ûÕ0=w¦SÑµY\x0018.Ð[ÙÜýîéÕf\x000cjãòI\x0013:P=æõ~¸\x001fy\x001dnýfÒiu!!uå)Yn\x000c5b^=ª\x001d·2cªÓééGy\x000bS1\x0000×
T53b^E±\x001d·2\x000cªÓ0@Q¶¤aª^t\x001dÇ\x00074c7Ú\x000cº\x001dugìXô½\x0018\x0010X°\x0019w¬à\x001báV^Bwz	e(Á -Í)\x0008wJ¡î¼ÌO;nµ\x0019t÷µÇAT\x0013q¡Ç!+C
|é±|~8Øg¸\x000bÚ%µr\x0011ºÓE(g°\x0005Útò àéBÉæ'@4¯¬©\ét\x0011\x001a&eæÍ1ÏVÚ¼-ßèÇT.b_²b5®Ö8¸)*Ã$«`\x001d\x0005æj£`LØRk'g\x0018àoú®Á\x001abÉ8ÄI5ñ¦æ(güF\x0001o Þ\x000b"ßu^ÖHÏVC\x00022_$\x0016\x0004\x0004û°M¾©ýuVÝË\x000cõ,\x0002ßÚ\x0019BsNÚeb¾Ã³#
9éZåDä®3û¤1ã\x0000^\x0003çYÚ\x0017ó:à\x001dÙ=`ß\x000b<Å<pþ,
>Á¬ÿÐG2ò³ógúÏ\x001fêÙjV\x0008^çQ\x0017ÐÊùÁA\x001då-ßÿz¿ûtu[9¿å¿{Ô¦Ï\x0016¼ÿ ²iÀT©ü\x001aÏp_;¶Ý¾~··¯ûì\x001d×¥\x0017\x000cªè¸è¸'Õç0ÜúÎ¡\x0016M\x000eV/?\x0016jF¢\x001cj¾£¨£\x0006j[ô\x001fÃ`7q/[\x0016µûS-¡Z(¿S	np·ç\x0006;ÍÝ\x0017;¥ÙÃ5\x0013K÷}U°\x0013þ&[íîo¯¾	ÿÉë5"QðMJåV\x000b{Þ\x000c\x0017\x0008ÏNÞ\x001e}srþôù\x0001Q\x0011ÄU\x0015®zì¸ºÂÕ\x001d×T¸¦\x0013©©ZÖ`ä¦,M§\x0016Ë²õm¸¶Âµ}¸Â;¸)¥\x001d\x0012ÊP5Áü©ÖU´®q}®\x0012Òjv*Eæ\x001báú
×?Ú­køç¤Á\x001f\x0002,ÁÿâãýÝÝÕÍõ³¦!½Ð²bª\x0016kÍø¼\x000c\x000e°¾xõæââôìùËCÂ¯T¤¢Tc~ÊrIcÎ$
e\x0016Ë3
ZHeI*»H#ùi6¥Ø%­èâfmáT%§ê]Q£É\x001d]*$\x0015EÊùÛf+©.Iuß
\x001aZ\x0002å9*VtQ¿Ó¦û4yÚ£\x0016W\x0014µ5jå[ImIj»H­ÆXãý1¾±Ñ\x0008\x0013>ßMÜ
êJP×\x0007\x001axpR«ä/\x000bKº	©/I}\x001f)¶A\x000bJ\x001eº"\x0019	ã/hQ4\x0016ÃíÁè³>TAÊéá\x001ecpf7mÓùöÛVÒÚ=õù'#Qá\x0017\x00165ÏÚ	?Q_Ï|µn+jåx2\x0016ëI¡Q\x0006§þ2:Sby>U\x000bjå xq"xúilðb*Ù^PZP+\x001fÅû\x0014Ô\x0008Y2ý4ìy:U¸S^9)Þç¥4N}6£|>u÷Í_\[1+\x001fÅûa¹¹\x0000N ¢+:P[pV÷Y~m¨ïLá»ðljÙØÄV÷Y~¥©ÜIpôQl¾\x0003¢\x0011UT_ôY~å%\x001d|YBF¡Ô|Å]+ieùEå^\x0016@\x00147çi\x0014]\x000fiE­o&}_s\x000cû\x000c\x0014&äEÅfN®·PDe÷EÝ
g4\x0019gAi/Õ
S0Åæ[Ò[Q+»/úì>Ü³
÷©<ªP\x0018\x001a%Ìæ\x001bÌZQ+*ú\x000cj8S\x0016\x001b ÐìâËcf[8+*ú\x000c*´`4á[êq`xRYY)Ùg¥¾Ì/\x0017Ùúï:×h\x0019\x000e°\x0017TFåØ|\x0005þjZ¶§\x0000yÙ¦¾¿?úûÇûÛ\x000f×7«H'­.\x001bB\x0014z\x0019Ô³ùF\x000c\x0000}öæèï¯Þ¿|~ö0¨(AE\x001f(Çü¤5\x0002ç\x0008z\x0007pvyÆf\x000b©,Ie\x001f©ÆaD\x000e5V¡q\x0008Ã)?/d»\x0007ºð\Áö\x0004\x0012RõQzj×µ
\x000b¤Îí\x0003CZÖÓ¤¦T0ì¾±Na\x0014MMÎÏ7ß4\x0016hÆè\x0012ÝF
b[\x000c!5ÞL8Êq;»|ß_\x001aÌ]}`ÒHÝºpùÓÕíÏë^ÖöX¦\x000c÷¨ôSS1÷SÅËÚå·§ç/\x000eÎk0{÷~ ÞëÞo@¶ÖCR2!ü¤
zEîpXÝ<H\x0001ä½	)\x0012\x0017Ëqm÷Î\x0008\x0017\x0001¸\x001c.ZÉ×zz[aóÂýíÄÖj­yô«ÌÍtç«lö\x001b \x001dt8yJ\x000f¥iKGÐ\x000fvA®\x0016{ÐÝV\x0003 ñ\x0000 \x001dB«í¡Õ\x001e´êÖÆ¼\x0006èT¥á¹6´¥ç\x000b{ õ\x001et·åÛÏl\x000f»ÝJs·ÿlèèÙðåÕýo+\x0007´\x001b!§4§ç4Dw1àyyúæí¡8×í¿\x0015:z+\'¦\x001d\x001böAN\x001bÈi\x000c±Y\x001eC¼O|²yùè
\x000e|Ø¢é(¡½<àw%*ñT3Þôvi¢\x0014cúíNÚ#óe³
|ºäÓÍ¿^Gg[Ód{\x0019"DÉY\x000cºVòÏ´ò)sp¬ÕX§p&\x0016Äx¶Ä³Í¿^NÏýá^«î¤£º\x000f»þ]ÉçJ>7p:GÍ&éiýìÂ¦õ|¾äóÍÛy¬*v¥_ïâ,ßuxÅÅÄM¯{
ë'¨R\x0006îy\x001e­ËVÛ×¾£ÙyTj6/e8TÐu~ù\x0012è\x0016®Énÿ
ÏMoxM¿Zß\x001b¤j\x0008Ä!À\Lã®\»ÊqðfÏ\x00017ã|6¼Á\x001eiiQïPöæ\x0001Àp­\x0003ð\x0017\x0010\x0018<ÿùÝÝ]e^ßì>|º¾º]y§àq\x001fJxµ\x0010ÈêmNÞ8iÞÎ<ñúäâ"3¯ÏN^^>?=?\x0014enYrË!n\x0011{ö"7Gû\x0003É2âu/ÜºäÖCÜ
"1Zï\x0014UxuË·æ¶%·\x001dä»'r«ÌµV¶æö%·\x001fâ6ñÅoo`\x001fpÏ\x001a>n^Ë±iª\x001bEñ¿\x0004¼:|ìdÚéd\x0016;%\x000b\x000en
^L>v4ýt4­b¦->ëõÁ÷g¥\x0016\x0004WG7; þáêÓ§l\x0002\x0007U[ç§²POiØùÞåÛ*V@~zzyyÐéì½\x0016âµ Ø¡®u&µ\x0002µWrßj1²m%%±ì%\x0016L\x0008ðÔ¸*5*~ú\x0003U\x0003­Äª$VÝÄMÏG&MqÒp»=±.u?±¦ë¬7X9.ß=\x001aMIlú9ª\x0006o\x001e\x0010\x0015íùÎ³\x001eb[\x0012Ûþ}¬±ÌzO\x001d8ý\x0000Äï·\x0002v%°ë7\x0015\x001e\x001f\x0017]p%y¬½T8\x0017ÃÏ.÷\x0000û\x0012Ø÷\x0003C.pZáÌ;må[#p1|«|\x0017k'Î°Ö[r\x001eî)\x000b#¬\x001bpÜ\x001f" ÉÛ=ÙÝ¾ûx}·z+8*Ý t¢+)_î,yrrþäÕó\x0015¢¤\x0014=µaZN>auæ9Ú e	); Ã÷
\x0013|q®&_îzYO©JJÕAi\x0015*®Ã¬µ\x001cFJ.&IÝÅ³´Rºg-EYÛ³©µ[nKSRµ¤Dp¨ô\x001bgÞ¯Y4¤ë)mIi{(Sü\x0007ã^\x0016Ó:ë!]	éz 5ô\x000c&AWC\x0016$ÇXÐ:·Á\x0011÷%¥ï 4(§®øI;Á±åÜÕÅ¨\x00029¹ ¶Å¤áF°\x0012\x0017sRÇu!ÔzÌÚõôø\x001e;UB?ÃãJ0~~Ðx¹Ð-÷¥þ%£c\x0013£ö(®\x0003æcõ½¤ªåÒ¶õKYKÞc/ Q\x001dÀåâA\ÊñãÃ+KÄ{L\x0011Ì
ç´1©C\x0004[\x0003ÃÆ|ø7þ\x0010¦¨~é¢ç\x001e`Î\x000f³OóÚ¡mÕ/]ôüÒÃ·\x000e\x0018]oüÂbûbXÍñCTNRôxÉppoj\x000cÞ\x0005lÈL9·j£¬üèq@z\x001aâ IU8\x001c/jíü¨6\x0007Ä\x000b\x0018°ï:baIÝ+\x0002rÇ)Ê$\x0005
~åº¦\x000c{³\x0003SÑ Q8C\x001c­IÌ-÷¬® Õ{\x001cá/à§?ýÏÿóéjw¿êö®\x0004Î¯·FdVz°¦\x0002V+\x000f\x0015°>ýöäòôäÍÃ¨¢D\x0015}¨ab¢!ñy¦âtÃpË÷ \x0016TY¢ÊÎUeØ¶h­Ä\x0002vé©ØË\x001dÈ14 ª\x0012Uu¢J*qQ;m\x0000z÷tóÓfZQuª»Q]Þ«!ªÏ¡¼bÓóûr×r\x000bª)QM'ªPíT\x00072må2¤\x0016T[¢ÚNTNCÈ:\x0016¸WI\x0006À/Çx-¨¾Dõ}¨r:åcôËC\x0008õPqøZR^ÕN»
#þ2©B­Ú©Rd\x000bÊ+CÅ;-\x0015ó©©ì\x0001+nH®Â-'DZX«3Å;\x000f}ÉWñã,µ­ÂE
¿Vª;\x0013¨J.,*øÎ¥õÓÒ\x001a<XS½\x000b;ÔtñðÒH\HWÇ*¸iöë}\x0008YÞí>®urÊZÐá¦çs¥¯ã¹òJûù¹\x001c8úõM\x0008[¼Z«*\Õ+ÒÚ*-·\x0001eû\x001aõ×7ÁÕ\x0015®îÅU\x001cU\çd§\x0014®îÁyç«i5/i5ï¤\x0005é5G´i.ç4\x0001g3ZQÑÞµÅé\x0006Ê¢æJÅ6ySÛÎZ2Ý{ÊÂ%'ûÀdX\x0014Ù\x000e§l£¥­Nî=eÁÉ\x001a5­m>e\x001e«mõshÇ­Nî=e ¿S¬.î[Ú¶ó\x001alí´¦¢5½´\x0012\x0013\x0003°¸¸\x0015ÔdÁ6¢µ\x0015­í¥Õ¨n\x0003k+\x0011×Ñ1×ÍmÅå¢Ú
qvd\x000f¯×\x0016g\x000b©ðé×\x000b+qëÚyq«V^QÄµ\x0002T\x0019|\x0017¯dÒcå³\x0012<Gá^Z\x001ebaÜv3¯¬\\x0004üØÇ\x001b.ãù£8O\x0007^:sìZÌ§2qU½¼ªwyÆd{\x001cØ\x0012ÃÜðÑ\x000b£.y\x001d«xÃ}¼Þcì\x0018.
¹jÌ+y.Íæ\x000bh[ye1ë"ðÂ]¼ðv¯Ô2Ë_z-Qþ2Äh\x00183iª\x0001~ìÃÕT-&µË³?½Æ\x001e&e·9lJïE}Æ\x000côoñá ¬×äD?¬æE\x001a[p÷ë)\x0004ÕSÜ~ØÝ¿"ËÛëÝ:yQ\x0018\x0019¯Ó´\x001a-*"x½\\x0013trþòäÍ3¨\x0004¹<~r@\x0004\x0013eÉ,\x0007u\x001br åÿè/üÂ@ë.dU"«~dFÝ\x001e\x000e\x001aS°\x0010g x9_ZÚÅ¬KfÝÏ,\x0015FÀÎ !KqÃ®ÞnkÙô3sj(ë5yT0&årmÉlûaOÞ\x001b*x'\x0007cy7cv%³\x001bXgOfCi\x0014Î\x0016Ç_xµÜ ÔÌìKf?°Î1ïg,Îó:û\x001c·y»äie.J#ÄT\x001aÑeëä±È\x0003\x001eU²­cÈ¬Ùfg×.eÀ§(u<Îz|ã\x000fÿ	4\x001cóù©.fQ1\x0001cÇ1_í´ 2ÏÑ@ëåòãfèÊ\x000fò\x0001G\x0018\x0016:×¥;È\x0008;|f£\x001d½üüß\x000c]yB>à
Ãõ)_GÀ}34w\x001cM´ÞÎÜñÊ\x0015ò\x0001_¨iF[ùc7nð6ÄÍÐ/ä\x0003Î0l\x000f6(s©HõÆ/$\x0007»+_ÈG¡§@É\x0017\x000f\x0007\x001a·´ÛpwTÎ\x000fxÃ\x0000eÅ\MÐ\x00119/AWÞ\x000f¸CÍÉ§\x001e¹üD.Üo\x0017*Ê\x001d\x0001w¨c²0¹\x0016*
V\x001cEð¡Úq3èÊ\x001f\x0011øå\x0002\x000fQ9D1à\x0010õÔzaIÔUa1\x0014¨QoÆ\¹\x00161àZS\x0002\x000fÜ\x001dâåºööKVõø\x0018/ZøøøèïZEÕT¼míz±¡)#\x000f\x0001rrHQÇ÷rY¥´ý*¾¿âjdÅa\x0000%r¬WÓ|~\q\x00179¯\x0017÷/8Ü»\x0014z\x001a1)\x000bP\x001cbk\x0014;°ßÕØïú±5
ä\x0013Ç,\x0013§Íü(Í¾ðip3t4¿@\x0014%ÂZW0üE4S
òÛÝÏW»{ø'èi^\x0001Îµ\x000fÂ\x0000Î`DetðV\x000b,\x0017\x0013l¾\x0004sÊE~{òâôä
ü\x0013´5?¯+|=\x000f/mÞg\x0015Ä\x0000ï¯Ïg\x0018ºé)é\x0019¤w\x0012\x001b0`ñSU©ÕÊÑâ?eo¥w\x0015½\x001b¥×XW\x000eôB%z5\x001b[Ó\x001bYÒ\x001b9JOuÜ°uR+ÕØæ*¸zà)¼ÞVôvÞ0~,ÕD7>?9\x001aýøÕÖ1[ÇÊ®ülãã­BÀïzCz^\x0012ð¿ÁcøÆ­ÅöÁz\x001aÁæÕûñM?hvâ<øiõOø\x0002Ë.\x0005W¸ïæWÍçjÐèCw¢Õ´ùS\x001c\x000c£qû,;éçw5ÿèîO%c¸þ©Ü\x001a,{\x0014ì§àFz]o~=ºù/ÐÞÓî¿ôóÛÔtzj³ÑtæÝã\x0014Å\x000c|SÓÉµ¯ùý(¿G·k\x001cæ\x0002ÿ¶ëojëcF­O¸\x000eê"lÈëï\x0005mÿyåên~Ë+~ËÇøa\x0006 ¬\x000fÏÖÓç¿\õãË\x001a0î\x0001e9m$`-ÞTÄü\x0013s?}}xíàác§ÙL7rPÆß_ðúºÂ\x0007]Õì\x0018÷ËUw\x0016ª×è¶µ-¾¨l?ü8Ï³¾óÞçTµ\x0013þÆ«/ë»®\x001c¼ì\x0004n2\x0011?Çm\x00164fS×+tuv\x001e=»©í\x0000·O**´Q\x0001o\^¹a\x0015¿a£ü67'ÆõOÍ)ÖÁ³aäç0\x0006nC~å*ë\x0003?\x000eòk¬ÛëßÓµå¡Õø|¯!\x0014\x000cÏÔ¸ôúãÕJ-'K=ÕQº'çç%©¡C\x001d+¯_\x001eÔ\x0018âû\x0003-xÙ
º\x001e2ì,\x0004úM¹\x001cGiÌx¦\x000fµ\x0001­¤T%¥ê \x0004	=K5\x0016¹±J\x0019K	zS\x000fQÎ·*!¢.\x0011u\x0007¢áT\x0006ÂiÌ\x0012(ë@Ö/¤+)]Ï4Øî¸,FÚT\x0015Ä[ÓWS\x0016ÂW\\x0003a\x001a0%et\x0005ÇI¥JaM©\x0017ËÀÖcVg÷\x001c¿n[[tmàZ\x001d~5Q8,ýïþ×·ÿóÿ~ººÞ^ßÜ¬ÄSø¦l!=\x0017#iNõ|/}\x0011bGß¾º<=|ûüììRsþ\x0004Q~Øà\x0013\x0018Ç\x001b¼\x0015~zÒ"\x0011"5_~>ð	²ü\x0004ùUþ\x0016Tù	jß&o¡§zY\x001a\x001e°ý'èò\x0013ô\x0006\x0010\x001e\x0005-Åô6jiÂ¸0ð	¦ü\x0004³Åoîi°çØo\x001eü7~Â|>bà\x0013lù	vß\x0002'AÆ°§LÞHVÐ¨çùùOpå'¸-~\x000b\x0002ªäÌ= Ks+ç¯6\x0003àËOð[ü\x0016ÇÅÁU¤¬,­¢Á«óu\x0002ýPLg\x0000×ÆÆ¿\x0001äl,J;jR4\x0006ó±3¯½ó\x0016î9\x001c\x00062*O¿
 Ío
|Båù&îÙÞ¢|¦ó¼¢\x001eøÊ=ó-üs8
\x001aU»ü±h4Éam½*ÿÌ7qÐ4DA&\x0006=ÉÍÍg\x001b\x0007¾¡rÐ|+\x000fÊO\x00064\x0015ê&\x0006ëæëÅ\x0006¾¡òÐ|\x000b\x0017Í5M
#Í1Ö;¬L8ð	æ¸è/þk¨\4ßÂGð\x0008Åj§ºTiè\x0013æ\x000bñ\x0007>¡rÑ|\x000b\x001f
\x0003²UR67ZÂÌ\x001fÔ3óåBýß *\x001f-6ðÑP\x001e
² í_Eµ\x000b3Û\x0006¾¡rÒb\x0013'\x001d\x0013eIßO`\x0012Eb^ÏÚyåþO¨¯Ð[8é\x0010gCÉðkð$©·q!*ÿ&¶ðoBÒÖ\x001e«ãÃoT\x0016çi\x0007¾¡ò
b\x000bß\x0010v\x0012C¥H\x0005Ñé\x001bð\x000bæÇl\x000c|Aå\x001aÄ&®Abo½¤\x001d\x0005ÔS·~~Öò7\x001cÌÊ/MînN2ªØR\x0016NòìZÿ/@V\x0006UnaP%IT¥i*¥øÂÌö\x000c|Ceä\x0016ÖH
ìÎò(Ôòu$$o6ÿ=TæHnd¾àA`¢¬¡NUø¯/­ÇýT{#¥Ý\x0006;JB2,\x001dlÒÚiÝúò#Eý\x0019á÷¾Ág\x0008wÌ1âc4#Ó\x0016·/¶\x001bI²Ö¡7ù
3~ú\x0004Li8)7srf$³¡Û\x0017»ÛO×\x001f^ÿt}sýËªdµ4]ÓYÒç\x0017<¦^Ô\x0017qr~ùüåÑëo=ý0¯(yE//(Ûàt&«ñ\x0003¯&Z.6\x000b6òÊWv¯/Ãõu|5_ÎÒÁ«J^ÕÍëh.GË1X\x001az(_liäÕ%¯îå¼Unñ:W\x001cÜá±Ñ"ÛðÚ×vóJ|¶Q\x0002á`&ç_¦\x001by}Éë»yI³\x000böÅù\x001dFu-ë'·ñ\x0016r3=§w\x0000[Hd¦
a¦	¤#Ä\x0007Î5\x0002×\x0006¸Û\x0002øe`!P@hEóbùu½\x0011¸²À¼Û\x0004\x001b\x0012!tl\x001a<ÃP£Ö/´µt\x0000W&?~\x001bÌ+\x001bÌ»° wó\x0017%^|\\x00066Är3/s±/.ðã¢\x0010Í©ùÁ\x000eÞÊ\x0006ó^#\x001cþXcç¸F¹\x0012®±!ÑåþìF`W\x0001»^`HGg\x0013áQô;\x001aã} »¹WTFXô\x001aa¦åñ´\x001fòí*¸j\_µ,\x0007ÓÈ[\x0007½&AÍIË^Kòr|Y%¾
XV\x000b,»\x0017Ø\x0006³\x0016BcbO*Aj+/'YqSJÈ»ÞM¬Q.<\x0004xEâ\x000eGyµ\)Új&jæ`(z­Ä66«°'0c9®3ó==®cjrÏÎã]§÷4Ã\x0005GC\x000c]\x000eHÏ53ïö»×ÙQ}®¤Ia¯)È®c^(eûÅÎ,Þ§JíÕ­Ec\x0011\x0002M±ÜIïÍFÎW\x0012O\x0005Ú\x000fUïW<³x[î!Å>\x0010\x0005J\x001e\x0013/rf^'ª\x0015Sª\x0007ÓÂX³,[\x000bÝÜ0áqì~°Ùi\x001d©.Iuïf=ààmn£4zð\x0012\x000fô5­\x00035%¨é\x00025T^£¸ÏµfÖÐ@h(sÚÔ¤¶ÔjXÈDj¨ÑÍa·\x0006Ì:ÛÔ¤¾Ôq<MÌaG§ÏFÕ°´ÁWÃÓ%¸ÔSJD¥gk9'±Éiâµ!í³¤Î \x00162Øéb<Î²4â!yu¤!å}Ô
\x001aÅ\x0001ù½ndó`Cã*RQýîE×ïÞ\x0006\x000b*Óï^KK4­¥9fAµ®\x0015µ2¦¢ËZ© n¨\\x001cãN
V4£.¼5¢jUMßªJöTK\x000búX©§\x000f×ô!)U ®\x0002u} T\x000b4/z'ñ\x001ecÌü³V+juú]×é·0D*¢è_XR\x0014v1\x000bï¹­¤áw]?\x001c\x001e¬\x0019ÖeEVhH%Ô:RW¡úÚGu¢x¬fj:S\x001aÏÞ"8åµ¥â¦K,
	ÿæ¬ \x0016,\x0015íU©6Ø«ÜÖ¬¶Ï¥:Q`\x0018¦8Á\x0013Á\x0016¬¦fí\x000bþ;6\x001c?tª4}g~ty\x001b¨`{®ªoQWÍ¾JÂ\x0010Á|¢No½%jd\x0015²b\x0015²Up0\x0013Vä\x000c\°VØ¥ô¼
e\x001b«¬ìóV |\x001f\x0014@;Ó&' É\x0007KÉ¦\x0004­aUuô\x000f?v°jo²¶\x001aêÄ\x0014¶c¨\x0007UV¡\x001aUô¡:ÊÐ¤²Áê\x001dé¶XU]í\x0000ø±\x0007Õ¨cL+\x000c¶O¸\x0010«[¤yHþd
«.ÚtÁz3×Å\x001aâ\x0000B\x0016NVás\x0017,n#\x0005ÍÒ2\x0008]\x0015.)YÔ\x000b,&µc©Üæ\x001aàXYòcAøÇ\x0017\x000e\x0006S³_\x0012GÀüvõ\x0001z¯î \x0013x\x001bþ3×W·wkòRO]rCQ\x0010ä\x00015NTqj>\x001dpòöô%4\x001b^@6ðüÕËÏOÏ/\x001e\x0006\x0017%¸\x0018\x0002\x001a\x0006fDðp[ÈÃ{5æ1O·õË\x0012\\x000e{K³Ã7ä	Ùá\x0016Ýdj>WÔK®Jr5D®\x0018ª\x000cYÁñá<ltj
oGì%×%¹\x001e]ó<JÊÂ,õÏ×|6è\x00057%¸\x0019;Q\x0010wyÑ\x0008ÏÒ6MÓ÷»Ü+hÌ%ÐÞ¥ÉÎ2OÝzówø^p_û!p1ÍZ.g\x0011|¾Ï°¼¬ÂIóbFÐ\x0019\x000c\ÇÆóüxf¸§Èy­^ôÚ

ù!%QEÈ+)ntC
îÁïoyDyåø'ô4®:è/W@·\x0001îE¯\x000c:\x001f²èJkìl¶iÉ{ÝPUö¦®W\x0006\x000fYt¥C@
zøÌMÅ¿j^r­\x0017¼2è|È¢+ÃQ\x0006<»"ciÁ··Êò4e\x0000Ü2\x0014"mnó6wøb¼¤§Ð^¹"þ\x0015ù"QYt1fÑÃ¢|Åêkã8¢ÏO\x0018í%¯Ãó!«¨%´]Zs\x0001[>.ºF)\x001aëÝ\x0016\x0006ýw¶÷|ÿ\x000fïÏ>~º¾»»úùêÃ§£«£ó?ütu{ôþÿó¿^Ý®àgPÉ\x0015PR¹d-XFì2Ï^0Î^]>¿¸8}qúòòèìôèüU¸Û\x001f=;zuþð7Èò\x001bä\x0016ß yÎL*5¡Ã7`¥«\x0011ó­#ß ÊoP\x001b|äZQÜåþ'c$Y\x0006#ß ËoÐ\x001b|\x0003óÌTLæ±xÁ[\x0019|tÏ»|)?Álñ	^dA&}öØç®ý¬!\x001aù\x0004[~Ýf'å÷\x000f	B¡:ï$ª{ñó\x000elä\x001b\ù
no\x0008aÍ\x0013Ó\x0019¦ðáéÎÑ¯as«äËoð\x001b|±(\¡ºàø
ÐV¿a~¾ÇÀ7Ð%+~\x0003\²Æ?\x0002_S\x0015×ùÝ/|\x00036Ð\x0019è/Ùø\x001bxõ
|oÖ?z¸Ê¾!¯¿À´òÊMó-ü4
ä\x0019÷á{xöqJEæ§9u|C°Hð\x0007´]Lñ7U$\x0003ï~¼ùøó»\x0010#­@\x0007a)\x0014Ýëº\x0007!l~j\x0005dó}ú\x0018"½9zúêìÕ'!@z\x0008\x0017£t\x0003t\x0014Ôþ
¨½®¨½þ\x001a¨ç%5üø\x0015PKmJjøñQSý§\x0010BÎóuåòêç_nÖ^V\x0004S8~Áj9?Iý)Î,\x000fµÊåé×g¯Xbÿ\x0005D¤\x0017>^®IQY¨@É¢C×óo£\x001d¼²äÝëí)ÖÈ<HMjN¹=¹ÕêªVu¯.Í#°Zì¢ÅW<·P(×Á«K^ÝÉË=IuXËq`§TØ­ä\x0016jP:xMÉkº×7o]m!¹¶®££¶<#¼\x0011Ö°¶{qÕ¦Æ\x001f©p!oÄëJ^×½¸RºP:ûÙúnwØ|Éë{×\x0017D\x0010òú:g\p"¸y\x0017ôMÚyRïüÒÒiË<ÉDCÙG6f~Zß­x+WÁ»}\x0005s(\x0013®'$å«Ix¡â¿\x0003¸²¾¼Ûü2MµÖäYH\x0001X­O\x001c¯Ì\x0019ïµgÜ;ìP²66\x0012g±d\x0002\x001bÙ_^\x0008Þk#@Ð\x0016'HÀ0¼ÂÃ\x0017¨n\x0000fFÔá\x0019È\x0016\x0014uË\x00019Ä7×\x001f®Ö\x0010KhW\x0003]9	ócbá\x0007J§\x0008Â\x00083ÈÄºÀ\x001cBÊ³ç/O\x001fF^©"²\x001ebV\x001a3°\x000fV\x0002µ\x0010OÕv@\\x0016Ûµ\x0012\x001b\x0017|@\x001cÜHj\x0018N@¡õ¼¦h\x0017´« ]?t\x0008Ñ`~óls¥¨W"w¹`ÿ\x000e\x000epi6Õv6\x0003ûÙÄÙª\x0011Ú£¤´WÁfdh9ï¥{ ,¡\x001cXi\x0019{Ç\x0000Ú
\x00089ÓJk¡ùá\x0006\x0006h^L³SXÎ¸z¼ûëÚÜé
ò\x0005©me?ªqn\x001a\x001e
jøñ+ VZÔðã×@m+\x0008?~
ÔUÔ}
Ôºö1zÄÉ|AÏ(Ü¤L\x001dú®;\	Ê\x0013Ïñ´W¨f\x0012b§Ãc¼Wq\x000bé÷*àÉÕ¶ïüú·ðçûû£·W·ï?®+¯\x0017\x000e»\x0016\x0018\x001dI5ën\x001aÅ)\x000fÖ×\x0007öóçoÃÏÞ\x001c½==öêPýzú\x0004Qø
?¡èÃO(û°¾OpõoÁ}}¿\x0005]$t çù¯ï\x0013$¯>Aò¯ï\x0013tý	úëû\x0004#ªOZ² M~ïp^º\\x001d\x001c¾\x0001Õý94¬lú
VV&ÉÊq$uÆwÎ\x0019¨\x0018Nß­6ÍO(èùpé«\x0017 ¹<=Ü\ý¾ûðþöêèÝ\x001fk\x0012FÚÐ *\x0010ÛÍ]BÖ+ªý<XxrvúÏÎO¾9ù·\x0007©§\x0007ji\x0006°¡\x0017\x000fÉhDcÔ°r¸¿
{j%\x0005lÃF°\x0005ö½YÔé(©ÍÁrÕ&jÎ+jÎG°DþL®ÉvÌPðÁì6lUílø±\x001f\x001b\x001e|³z\x0017¼¥ú¼·Å¤õw¨®¹[[å\x000e;ak»ùá¥\x000fEAc ¸\x0019vÙ"èðW#\x0016%?«9­i³ðI~l=ÎØ«\x0017"X~¼ÿ\x0014Ç/\x0002Ñ§£ï®VµwFUH³ÐÌáC«wt1±ó[åüÕË¨9~\x0011~¼<úîô`§ØKê\x0002´ø: ¥,¡¡ç¹\x0013khæ%©³\«i¸?9\x0007½4ï \x0011«X=~bUm\x000cõul)\x0015\x0003ÐyüÐWÐÑ7>~jÐâ¬&xD\x0007óx7¶Ü×§Ó¨ô«£ÝÑÙîÃ§«Û\x000fë¦uBp=\x000b\x000c\x0005Ë0\x000e"k
Ï\x0007}éqóèì$ü¿§ç/\x000fM{Ê@lº­A±à¿³ÔÔWíÙ|q}\x000f±-m?1;V\x0018ê1£.9	\x00035\x0010mÀ®\x0004v_Ã¦ð%±üK\9©ºG¼ÆEç±&\x0001ô,²ÅVìÂá&\x0014Dñ\x0007#XÌOñ73½V]\x0004Þ£ûÛ«uSo8\x0014¼c\x00087®Fp\x001a¥õÁäøEà=:ys~zpâMb\x0006=ù\x0019~ìôr´áyj54MÌ¹ù)\x001c=ÔºZéxÇê¥6\x0016
3\x0014öLí¦1\x00062gmÐ¦6cÐÊ§Ô>óA\x0019â&f#+f#\x0007¶CuukãèÂ¬LFC\x000ej=5QûÚ÷SÃ 3,eÌ*¹õAA½\x0016jQT%\x0005jQ%µï\x000f\x0005]&\x000ft²(¬«Ñ±Ì§iz Ee?\x0018°\x001faS£Æ×\x001a0Vµz\x0008¶¡eJ,\	\x000bMàæ
ÂIlÙºIÈ!<ÛlHQm\x0010)ú7
7\x0014ùq\x001aoN¤£	Dþ¤a\x0013µ¬×Zö¯µ1¶u\x0008D\x000c*Fz(Á\x000f=\x00114QëZì\x0010\x001dÚP]î³|°¢ä#Tê¡^(#uñBÙnø\x0018\x000est *µdµ¢y9\x0007cVQïÂæ¨*HO »\x0004ÞÕÝõû«\x000f?`ïêîèï\x001f?|Ú­,,à\x0008\x0015UCxnL
·oRS²óõç§\x0017Ï¾|\x001a"¾Ó£¿¿zyyr°¸ØEÉ.\x0006Ù)T
ì\x0019\Nàó5Ü½à²\x0004àâ\x0011©¡{9±Su´Y(6îe×%»\x001ec\x0017´ @.3»\x001dAÊ!z¾Í·Ýìf]f¥O\x000b¯1Y@U2¸õÂð^tW¢»Atz	å\x0016npÕå|ÒîKt?îQM\x0016FZ\õ+p'9*É8²1tÉpR¢I\x001d
\x001dý¾×0ídç¼6ì|Ð´³©Hú<æ1\5qV³óî¿\x001e\x0014Î¿¯:
áY³®âl\x0002×Ð¼\x0003LÖ7	.Ô\x0013øAã\x0016h®\	
?vc\x001b¥@\x0004$½\x0012¶1\x001cÃ-ó`5Ãznc*nc\x0006¸Äì\x000bÿZ¨Ä»ÃÚò-ÜBë\x001b~ìç\x000eb¸D\x000c\x0019#¢t :<\x0012a\x001d¶\x0010ûC\x0004
:\x0006\x0015ÜûUO»,DX,"-f.¹ä4\x000f4S¿9zýæÀ.\x0012ÊP6\x0013¦\x0019=)\x001bÅò
\x0007\x0008)2Ë\x001df+	uI¨Û	9M\x000e÷ÝÔQ\x0016n04\x0014x9ù»Ï|¦i\x001a@©%¨$@\x0014àó\x000b#\x001aZ\x0008mIhÛ	)¥TN\x0018ä\x001c\x000fº8Ð\x0014½Ðî1®¡/	}Ï9É0;YãIV4ëyþW\x0010.L\x0013ûÃDñò°OÂÑÀVgOë\x001cý\x0015óÚ\x0014¶ÛÂ¿þw\´	iÈpË"r\x001aðnuNk½§îÕåQk\x0011+sÍ»ìuÆ\x001ajçX
³7ùöª"Tí>Ï\x001dO¾<\x0003KMá~¾Æ¶°r(¼Ã£üÅg¹2¼Ý\x001aNS¹ÁãÑ\x0012\x0016så{×,!W¬67ðs3¤\x0005Üô{&
T.q\x0012·ÏB7E6Õ0\x0018ÝÄâG\x0013à0¿wbÂ_'&µë´Â\x0007RJ\x000eÎv*QÜS|~~R\x0006Í1íay#¿7y;òn^\x0005\x0012
\x0017Õ\x001f\x00147ô¼¶<;~%¯°ûÂF6	\x001baùÎÛÝÍÕ»«Rµ\x0002¤\x0007 tG3/Å\x001cF\x001aÍí|¾\x0013KwÞ¾¼xu(¹¸¶Äµ½¸\x001a^,QdXcÔ\x0006¶ôçýe\x0007±+]/1\x000cÿq)kâ5Cµ
§³û4á¿}~\x00077\x0013«Â\x0005\x0004b\x0015}@\x0017³\x0007­ï¸-\x000c\x000fAIê¯\x0013&?KKüÂìßvd[m8¾\x00139X^­ÌÓ>|ø,§`Ì¼Ì_;²Þã¾ð²\x0013Y\x0006ÿr\x001c\x000f\x001f\x0001ÑIÇ;sÇ-iµ"\x000bV\³ 8mY'³\x0002é+\x0011¡PÁ\x001cÃ:{æM\x0012\\x0008\x0012æí[\x00034ÛWncõ\x0010û£§7\x001fï\x0000ýiøëãÂ\x0014Â°\x0004pñËé¿lou-$çÎ^]À\x0007<
_òüPkÍ¾\x001b«'ÙôÑ\x000bÌ	\x0003Äò¤+Ã°hC-$¼ûéeI/Gé5
Ã\x000bãqXk,NÎKP]½\x0019ÛjãØAz)0O \x000cZ@o4\x000eoSó:ßÝøÒWkï\x0007ñ5G±$¡\x0004\x000eó6
mJÌ?ivã\x00179M¬Ó£ø\x000eß¿T¹0\x001a\x0002\x001cP«ù¬}7½­6¾\x001dÝùÎÃGú`8i6>\x000fJï7µ:|Ïf²Q«éL~¬\x0002|G¹p<¹`'¶Ä/ê&â\x0000\x00106o\x0015Ã»\x0003Hp)\x0013ñåìa7¾q\x0015¾qøãî\x0001A.ËÇ,¾\x0015J;_ÉÙÍïêåw£Ë´&\x0013¿À±ÖÑ$ÁùËE/~1\x00035º\6ï©ô{åà­ãX ç#Ê~|Wã\x000fî\x001e\x0007#1eÆgXÆç\x0004LJ»­ß\x0012¼2ðã0®×âÞc\x0013ø\x0010'í|Y7¿¬×_®?§Ò\x0010Xÿ´ù\x001dIèI»­í\x0014ªÞýjp÷»ip5wv?\x0006úZmCN¡êí£F·O¸¨<ÅÔ[¿\x001cùMÂõ¿]uó\x0017oÐÀoÌ ¿41Ö¹Ü,\x0011l'^X¤9<\x0008ªßÕëïF×\x001f9óòÓ|n/\x0018-ÿÁîã\x000e|_ã\x000fÍÎ1Z~¯ò\x000cÀ¯5ñoz|%¯î\x000fÞ\x001878]C":á+ÌCK³íòC\x0016¾Â\x001f\~\x000f/²B\x0007®ëæ·I³mà,UukjðÚâÃÇ\x0014\x001dRõKøOùéôn\x001aûHåjþAç\x0005JÖGäíï\x0018Ç¾'©·u¾ÅõÈo\x0006½×qÓ ~a\x001c%\x0003ÿ¦Ö\x0013bÁß\x000e\x001e_o\x0014íÿÀ\x0015ð¸ÿõ¼m7¿¯ùý(¿µ86òçý¯(zÐÇF·ó×	+?è½<Hó\x001a:¿i Wà§às!7ÛË¯jó¯\x0006Í¸û(âw2\x001frÌbÂ0¬ÿ¦çW©_òÃpÀl?¦Ê
Î4ñojÿ­\x0012'ðã\x0018¿ÆÚj~òÄW® ó¿iôPèã%ü±àSÎ3f\x001eEóÃµ¥ã»­ûWí\x001fêó\x000fc+¥£|rÌz\x001e³\x0015óí\x001dü².	ñ·Ri\x0016:ìn½_÷¼)°S©¬¡%1S«í\x0003\x001afÐnüääüÿ¼9ô¶"ë)Wuó\x001a(°J)\x001eéLNpÂèÔ¼ÐÏo.fW2»~æ°£sã|órÓóRbJÙÍcîaVõ:÷/´fK\x000bÆ	ëÄ,£Ilü°\x001cx\x000b³©Í\x0000³ÁyÊúc74W
¡ç'¹ô@\x0017\x0012Õ [aû¡¥Ç´Ò\x001eäq#´ÆÈE»ù±´\x001dÐ¥¶ZT)`ýÔ\x001aµ\x0003Áp`¼k¡\x0011\x000cmÇVûsUS\x000fljípx1y­¡*3SÏ\x0017ï¢v5u¿ý\x0000e²ì\x001cUØ,6Å\x0001¨ç\x0015z¨]½ÖnÄR\x001bÐ'Ô\x000c{Ñã\x001c\x0004-ÍVgQÊÀÝÐ Ï¨³{¡²IÏ­\x000e#TáÔvÀÁÀ\x0008ñì\x0014Ã=4¥N¨,;­vµ¬ã\x000eø±©}.aÑ³g\x0008pæêCâ£-Ðª\x001eØÔ_\x0010Ú×Ð¾\x001b\x001aDYò¼\x001es+Þ¡QVmµ©Ë´\x0016P+ÝO­\x0015wÊ\x0010¤¦Ú3ÏIJoæ\x0017¥©×Ú\x000c¬uºü&jwg\x001a»Ð6\x001bØjm¾¯:f\x0018¨\x001cýío·»ß®nïÒ\x0015æ§Ý§«Ýý\x001aæ°}¡®*\x0015:ÇP52RW\x0010³Èçáör~n/ß\¼y\x0010¹\x0010
	ÈPJÑË\x001c6²Ff\x0007\x00039é\x001dõ#©Y×\x0005m+h;°Ð$RÝ<$S15éX3+³\x0017SÃûg\x001eñþöæúþûv\x0005óØ>g¬Ésk¨eÄñùé©õ~s\x000e\x0003º\x000eíêD^¸Åý¹Wl!W.\·°[ÞæQ6ÙX\x001doæëJ»ÈyQ\x000e\x0010þkáÇ!t\x0006\x0015©g¡\x000eÒÓPÊ\x0015wóµäE
äGØMäÖ\x0008\x0014¹7OÃJç%ÌúÐ\x000b\x0003è;&tlÉ¢ÂA)ODn\x0012º^ásÖ¢ë\x001a]\x000f¢\x001b\a¿HD×ö¯Ø0®2/ðã\x0010º]"(\x0006ÉqÑí[ûJr1µ\x0005\x0000¹`]ÜÈ5#å;xþOÎSSËv»EÈÊº\x00089d]d\x0008S°«ÁùTU
?Ü-^<0¡
Ý×èWMèVÐ0Î`ÞU²é 
Km´+2\x000fkÑ]îÆÐÇD õ\x0006Eå¤RtP[©
½|à\x000fèñ\x0000\x001djaQJS`yE\x0008ÒqÕÕ|\x0019~\x001fº¬ÌCæ\x0005âðl^\x001c×¹íÁB\x000c¢\x001fT\x000fkD7Q\x001f\x0007ÐW¸×]\x0008Âr9¯\x0010h\x001aý,êq¼\x001aËØ¾èð\x001e(<R!IÔOÉÃª\x0016-èW¶Q}×lAçVD\x00045÷¦EgÖb´×:èC\x0017ÕªÃCè\x001a_1¡tBÇ¾d9_Ón+Wª>Ï·¡3)ò\x001cÅò¥f[yP%´\³Ê4êÏ³XMäÆbé\x0007ÊäK!uBµ&=»\x0016½¶êzÌª\x0003z¾ÙEtÑí_.kt9®Q~&3\t
`¶3ºöFzÌ\x001b\x00017w\x0013¸Fp¹=¸®\x000e(ü8\x0004®HyÎ³ÜT\x0005ùÎ|>ùvFQkW\x000f%\x0001¸b]ïQ©\x0019IFÑoêªÁ4Ù\x001dÁ_
\x0001rRáÔRÅµ¡cúÀ°ñu_À÷û¼yêó.\x0014¢^ìîo×
Dy\x000fM%\x0011ÐÖ_ciN\x001b=ðØvqôâäÍùa(d\x0016%³ègñÙ8©å1*C$U+\x0007£¥·b%³ìgÖ\x001ewÊÛ\z5¥ø|á\x0017³*U?3·ø8\x0018|Þ\x001bÖOãÛ¢\ðFÌºdÖ\x0003Ì\x001eêòP0\x000bú\x001f0¯%\x001eÆ[MÉlº×n%;6Ù`@èÙî\x000cÚÙ\x000e0Ó-Ù V%kç-§ýüÀ}­ÙÌ®ÙÒ\x0013qÔøç\x0015.3P{p-2/¦yyÞÚ\x0004í\x0018VC\x0018Ç¡Ë>AcÑcó:K=Ô¢ÚÐ\\x000clièSÉn%Ùºpa \x0019\x0019¶Ù(\x0012ËXõ\x001b\x000e'
Öæ\x001b­0«<uÖX7ßØ×Cm«CÈíÀ1\x0014\x0006õK2¹¢×:ªèµîdÕzjÉ«\x0003~ì¥¶ãe,\x0010\x001egõr#Mm,\x000eÙ\x0006ZW[Zêþ-m`ô ÍÐ¦zXl~°\x000f¥4\x001b¨MeñàÇnjH~LÍIàVc\x0004îîÛ@+^-5üØ
\x001d\x0002\x000fÎ¢\x0011h¹Ãc\x001e3xí¨mMÝ\x0016AL$\x000bZ@	ÊÚ¶\x0002W\x001aª\x00117\x0016ÙS¢ßìé\x0010$eu\x001dlv\x001ae\x0014µñZþÔ½Ër\x001cI®ù*ñ\x0004\x0010»_\x0004« \x0018d¢\x0004\x0004P¸P:Ï&%H\x0006Id\x00003\x00000µêíyÞÌætíg1g1É7é'\x0019U3U\x000f÷p\x000fwóè\x001a°EÊ«®Ë\x0007ss3½þºKH¸?uhRïjÝSô-b;<Q\x0007\x001dyì(Ö\x001d@m\x001aÇ1åÇ\x001euT,cQó) ¶²ó¼Øá\x000f ö
¿\x0005,¦Ö¢Zkã9rf\x0005¼Ø\x0011i\x001d´¯y·¾³ß\x0015Ç·|£[ÏÝv^ì³\x000e\x0003¿\x000eþ¾|DìLæ}Â+îÂjìíø\x0003ðù:øü9¯ø;)Ã/Âªã\x0005Ví¦\x000fÏoç\x0000ý_ÿþ\x001fÓ§åü]Ï±$x\x0007PW\x0017(\x000e\x0013k
I©kk¶»æç'S`Æ$Ó\x0017Í$Õ\x001aË5al\x001c&S:\x0007¤?Ý½yßöàTÒ+î]GÉwMSçÐL'ìí\x0015¤<unòÓÙùñÕô¤cOÈµ¶\x0015äUÅ¼¨N¼*
\x0003M¼èRøÀµØ\x000eâÕu^]¾¾`\x001fQm!Y\x001bXÞÊ£5¡s¨_\SÇ5Å¸¨\x001dKË+$UðÕ|.¡ê:nËpU¹>\U6«\x000e]Z\x0013Ò¹Ä+òÖõÕÚöcÝ¹´®ëqQxOUAÑ\x001c\x0001WKqPT¸v¹ÎA¼¾Îëÿ\x0016ë¼±Wñ\x0005rÔM\x0003?1®ÜÏ&\x001bË+Ë××*>\x0019D
Õ%ÜàX]Tmï7\x0018Ì«Dãà\x0015å¼e¥>°xu\x0015\x001fïP\x000f\x001f¶}\x001b3£Ó\x0016®T\x000bv¨*¥¢\x0019\x001b°+ª¹j{-ùpl»mGaÿ·|:®]Ëàç4ò²'óoý`V\x00072k¸*-©B(O6m\x0008»Toû°:«)cÅáªbÍ	µ(
5
\x0002«Þ÷îÅêê¬®ÕÃ	#\x001b\x0013«Ç;
¨{Ã©Ð9F°?k¨³BV:î5Ð (,\x000f\x000f;²:=Qëó¡ãa³Úg\x0000«I#\x0003u²¢`õÌº»ù¹\x0017kãÓeß·ö¶«á¡o(DÎV0ûam|Z²ìÛ\x0002o2
VN°\x0006+\x0003,ù<\x0000kwóöm|[²ôãr)\x0005`5i¾Eáh&\x001dÀîîRì\x0003ë\x001b;Ö\x0017îØ\x0013uªK­`£¥m\x0000ÿ¯}`m\x0004¶\x0010Ö¥^\x0017á}Cq´(\x0005)R8m:çk÷Íë@Â\x000bAº\x0014?Ói*#ü7\x0000¹ÞXêI[\x001f\x0013\x001fó¹µ95´ZV*ú¬0§Ýî¾>´ºI«ËhÈEfimW­"\x000f
ÖvwÓu\x001fÚæ¶û\x0016LÙäû"m´ÔG\x0011Q\x0010;Ó\x001aÔaÞ\x0003ml\·iXt	-\¸X¡&\x0011ÉBD	\x0015ºÅÞÑ¥TãüÂ\x001fËhcE\x0005 D\x001b)ù\x0002´3³ûÒê¦} \x000b
5ò\x0013­3ä4D\x0015IQÐ\x0019¿[j¤v\x000e¶A#Æ4Ec¡1ÚöÃ\x0013à¾ï\x0013\x001f
Ñð0^	ß\x001bM\x0011³µð×ì6ùò\x001axvÓ:­)§uzEKå\x0012cÙ\x001fl¨ÃRØJê"ÁR­aeI Ý1£¹/m¬ÓÆrZÒ\x0002H´\ÔÁSv÷F+\x001b\x001bA\x0016ï\x0004\x0016üFZÏ²rßÛVº\x0006­+¤\x0005£FÑV\x0003ªáL ªNéá´¾Aë7­RuZ¥Jwç`T¬\x0007[K7tÛà¥Á¸¶kKqW¡"P\x0003ºO*Z´s·ûdÃq\x001b;WîÜ\x0018QÍ$ãF\x001cK¸¶ÂÝ1\x0007º/ncëªÂ­\x001b\x0005Þ°´u%ç)£\x0015\x0015nË¸°¾¸°\x000b|3¤Ðó?<<þòuþð¢u7÷=eç«ú.Ç\x0019UJqØÃZ»]{õøÍùôò2ê.ÏNÛ¦Ù\x0011¨¯ú"Ðè\x0015o\x0002ç\x001c¹æ¡òv­o¹\x001bÖAw-êª\x001a\x0003Y1ý\WuÕT¤ØS[²¬VrÃ»Ãáq¤=ª¹:'l<tUMcUMÙªÂ\x001b¦¶\x0019T,Ôev©¡Ð{»Õ\x0017\x001bÊ\x001a\x001aU(û®à\x001eàF<\x0007þ¹§3+p8Vì\x00036Ê:,%J`áá
\x000ek\x0010©2\x0015h	ÖØ­XoXðe\x0019\x001cbÚ`}L¿Ìï>Ü,ýJ%`	\x0015ã8Pç½æY1Nnl]\x0011_N¦o¦§/g\x0017]Ç[Õ¹Õ\x0018n°e¨\x000eßXÃW×,gääöª¡Bn]çÖ£Ö[\x001d(âv\x0014Ò=*ï\x0012övBlSÇ6£;¦xnZnÍW±×¬LìäöâÔBn[ç¶£ À\x0002¼Ø§tiVÎ¾ WÑ´·Å(jÍ\x0006®\x0015rß<[Nl¯\x0014)ãÖÅÖ£VÛx<A2·À¾¯Ä]õïº]Gõ\x0010nÛXo;j½­fq\x0000£\x0003¥V;Ò±mãv]2p×Xp7jÁÁsþ&)\x0003øÈm¤6no	,â®+\x001bá¥#F­xäÁÔ\x0006.u Y)\x0019/Êý«Æé?cÀÑ§)4y`ÜqË±Å"½ûÆ\x0001ÆâÃÎ¶$¥u[\x0013yX&ïñ¦WÍ\x001b\x0013\x001cAî<\x000bìhíy&SÜCj[dËÈUÓFQc¬\x0014$W¤\x0003h¸é8J\x0013Xs{oU\x0019¸n^@zÌ÷\x0019e'QÃ7ÜbU
.
ÛÃFCÉE¾VÛ\x001c6
ºÓÛÛ\x0005aß,{\x0015\x0007+M\x001däÉ@QÄ ]Õ?c¶×\x001dLONf\x0004||ÑUÑ\x000c[\x0003\x001fµ!
C1ë2#¯°ÎÉôéÝbù©Wg7ö d\x0017\x0014ôÅÊ\x0015\x001b"n.Ýèì~}\x0001«=L¯_Ì.^wu¨ç¿båî¤¿"ÊñÎe\x001fé¯ÐX\x0005d°\x0002GkD\x001f¡nþ\x0015ëº)?Ä_¡kÂ{ðWè
á½\x001fã¯Ð¾ñWèu\x001fã¯¨)	â_±¡$øcü\x0015!4þ°.1ü¯@ÍÏ¬X\x00120¹DSAåÈÜÕ&<ü¯0¢qÒ
)Í¿\x0002³xtÒbc\x001a
èÀ´üWH¹[epè_áÅºpLÉ_\x0011)Êþ@ï³¼Rn7AÇü\x0011²ù*6´µ~ÏÂÔ$\x0008S%Çºßð¿ÂkKFGÂTÃfYU\x0006¶Óné¤o³[?Â«0R¬o¨ñ;
ë\x0004\x001dQÆPÿWÃÚ¢Å©,ú3¤\x0016M\x0018~}b\x001a ô·Åünòæþé¶ïÔâ»'µ¶\x0005n\x0012óàmr\x0017¤ê\x001cø·Ùôtòæìú¤kj\x00101¯&æ&æÚÄÜÁÌCóÖ\x000b>M¤RDëåö\x0002ê\x0002fÝ\g]¼ÎA¨\x0003Å-
~=ì\x0017Î}ÎÁôc93KÔÛÎ\x001d²ûzÃ*Ù5\x0012w\x0008±7
b\x000c7\x0014\x0012«J«ÊJ\x001eväC5\x0003Ý¹Î9¦CCsgò!\x001d\x0007/q\x001a\x000f-²cEY\x0017L×ì½AÈ¡\x001cµääÛG¬«s¸í9ÇáÈªyÎ©òs.hÃß\x0015ÍqÊ\x001b!í½Ç\x0005ÌªÉ¬F0W\x001a\x0006Æ\x001bÖõ	å"ÚÛ:¯¨ÄNT)³:àyR¾Bö[ò5\x0005È5\x0005\x0014D¶®\x0018\x0019Ï6b6+Bäû\x001b5z÷Ã¬k\x000b\x001açÖÊbf¸¶éhÖ\x0018¥¤\x0012\x0015Í\x0013Ò¬Ú\x001eº)`ví\U;\x0019 jÅ@°¢ºå,SF0{Û`ö¶Y¡ÏCÀm»hØ<²ûÚÎu½\x0016Mz-eÈÉ\x001fÈÄðoÍk<Ót\x000fr\x001dÂk\x001bK?òÂ¥GÃWý\x0004ðb\x0005A\x0013·«Á\x00170ûe?2Ê\x0002Õ{¢À\ª2\x0003r{Æq8³\x0015
fü±\x0019[ùÙEJ¥YÊ9;µ/sÎ6
}[nèAÄ'³F]l\x000b­ùkÑ}-`6Ï\x000f,f\x000e¼qò¢YÊºZçí8\x0005ÈA5*Gö<\x0015\x000b´"\x0011K^å°]v´\x000096c9²¬5nð[äª7WÝÙÛUí3»ænv#v³÷¬ig¼å>pxìN©í­H\x0005ÌªÉ¬F0ÇÔWÌ(£K\x0007\x001dsno\x001f 3û\x0004,E\x000eò}xàhg8\x000e\x000eo²§+Ðùæ*ûòUÆÈ\x000bIQi®6
+Ynç·7\x001607ÝVWî¶F/¹\x0006ÝÖ@×å\x0019¬®¥Ai8³7
fü±YW©Zm(þ\x00029\x0008³½ß£\x0000¹¹Ì~Ì2\x001b\x000ctXe\x001f ÎôÛÛuòËãb¹~¥à¯Jo\x0015Ãòþ\x0006õ#è¸C3kmö\x0016Xlè^Pp\x0011U\x0018_Ç|£à!7\x0005½Ò\x000e\x001c·ä¢UUµÄ¯¦pàÙòK¯
\x0004\x0001;&ppvV!rÕ\x0019\x0017vSº]¼éÔTË´«\x00022¤u¶\x0016WWPôV**ñpð
r.ê]*©ýpWcÂ\x00107¸R\¸\x0001G¾;[ztq§u/ZY\x0013û\x0002¤^ëZÙjêwv\x0018\x0012çxþNÝû~¼µ(\x0017ò6r\x0007ñ*®k³û\x001b\x001dîY>àvÌ<îËk\x001aw]Q¹?¯\x0013«|	W³9ðDø
q;õî{ñª&¯ú\x0001xY¬\x0013/]P0'fÿ×\x0007\x0006!ÛöpçíÒ~îü~\x001dù}!r`ÓZØsÆñ\x001eÞÏ¼\x001f×y?í
«¸&\x0013rsU³Uÿ |»4{#¿[G~÷ìï×ï\x000b
OQµØDæ	¹ÒÅõÛ£Dý^\x0013¶Tº&lù0¹X|ù:_>öªcÔBSäÞ[É\x0003SL:\x000b-Ã²Ü×åäböæ|zqÕ\x0003V×au\x0019,Î¦cH«s;K0ÎT£ueá\x0010XS5++%÷\x000cyòGMàIâ]Ú¦C@]\x001dÔn\x0001Ã=Û°7Ií\x000bö@5°ÃwéC\x000e¡õuZ_JK#¸T`Pø\x000fñpB\x0015¶·\x0014\x000fF
uÔPº\x0003"\x001f^>jMhcµ°q{½ÎpÚX§¥\x000bë8\x001c\x0011´Å>Ø¼¶÷º¥»|(íªº\x000bi¥(]\UMð\x0005cwB¬±o·xÓÊ\x0006­,]\Ï\x0006oÐàZðyPa×Ûåôã6.\x0005Yz+È43$áJMf5¤m-ûi\x001b·,¼\x0016À\x0017æ´h0\x0015Bá°­Fn¿qã6î\x0005Y|1ü\x0016×6hm)m¥cÊO$\x0017\x000b\x001f\x001aã¶tD\x000fÇmÜe²ô2Õ\x000cûM»d#°:\x0015¬nØj0\x000eÇm\f²ô6SLÓ¡kY½\x0012ö\x0002;î8Æb?¸\x000bMÞhpGM\x0013À27|UÓ¤Íöºìá¸\x001bM^i[ðË¨b\x0010?4¦ÝÏw¦\x001a÷*¾ÏVC:%·\x0001`ÙÓIª4{Ám\hªôBï\x0012\x0001ÁW©8î~{]ãpØ¦S|\x0001\x001cÍõ<\x0002`9\x001eÝÓÚ6î3UzÁ\x0005A]¬æûûqäâ~h\x001b×*¾ÎªÀMuölåÌÃ,ß~p\x001b\x0017*½ äÔ
öKæfà`\x0005Ï\x0000¼CàºÛ"òB¬ÛA\x0015ß\x000eëB¨\x0006
\x0018\x0003´±EyøÒ6n\x0007UìïHÎ\x0015U$9­*yòN]ç\x0003puãÄÕ¥'.0Re\x001af­òâZéyßîËjÔ\x0003W\x0017\x001f¸\x001aïÛ´\x0017bý3cK!ìéTÐ#W\x0017\x001f¹Ë\x001e¢17Éw¯ÿ=á6\x0003KÅ.çaV(\x0001\x0014É\x000e\x000b,w¥zûÁm¹ºôÌU
O®|0HÞº«\x001d0:6þ\x000cÓ
ÿAú\x000f\x0014¯Áe¥Ã¶r{\x001d
ÞîgY\x001bç­.-\x0019\x0012%{\x000ew¬ð{:½\x001a¶­.\x000e×\x0018R±ª¾²ÏÚ×Ø.ZÓø¾Lñ÷eÑFÌ¸\x001e\x0007Te\J¸}Ek©\x0017\x0005äèíj\x0018Æó\x000bàj¹Î\x000b÷C9°¨\(¨Ace\x0016\x0015ÖÁÆ_gV~\x001c3ÙºÑpMmÝÄÙ.0_àIlP«\x0011Ôÿ"gMèýQ\x000c­¢«"¦ÎR\x0015âjö²ß5	ºVSD\x001aSºA[mj·±AÆnká×æÚÁ/\x000ekVÚìýýmOQ\x0010»\x001a×îå\x0001Ù¿²ÊünûwvtvÒ)	â×ò~\x0008ª@£f
^µ¨UÇ@\x001a#¾\x0007R]'ÕeKª¸OÎaÁ2mZ¼)ÚC!Òí\x000ec:¦)Ât\x0012Û²Ì©g=N##Ïø
Û».¨«º"Rxß´E¨ÖÓp;ï6rúrú:§ÆßR¨\x0012PÌ>\x0008]}K.rú4TßR§1Þ4ÖIcÙ&\x0015iòLz÷¡JôÊª\x0010¶;yÚ\x0013´&Þàé½!kª9,ÃÓØ{ôºQ×yæ÷%møÅG>ë\x001bÃ65Dºê¤\x000fÛEñ¢6NRYvzÃ	^Ü¨Ô<øÏ·t<\x000eEm¦²ì8ý\x0017ú«ôXâ´EÁ³¾ª\x000bö@\x001dh¹íg\x001fGl|ø²ìË5í<ú|ßsëvÛ\x001bg\x0006¢ªÆ\x0007¥Ê>(°Riô\x0005\x000e $Ápã¸10è\x0011\x0002CoÒºaoÓºa=\x0004ØÓ8MüªdÞýRïA\x001d\x0016,IË¿x\x0001¿8Ä\x001f\x000fîoo^ôÉÍÝbþ´Uy©\x0005~÷(Zbá\x0006Èn¸ÂÁÙ	ÖD§·ÓäùÇ§³éõ¶I¹\x0012\x0005LI\x0014ð\x0019Qb¹õ/MI\x0012¸¸$	\x0015ú½?cò\x0001q_,\x001e\x001eú\x0008Á$%À<D"\x0004Ç±8­øÓ\x0012®sVâëé%¸'/úÅìò²K\x0003FdÝESÇ\x001fÇÀ\x000bô¹³M\x001aø\x000fZéI¦³%[Èn½¬³ã?ÂÂ\x000b\x001b×üC\x001b×UÐnç7ËÅãc¿##Õ®ñÌJQ
S3Õ¼Â¹¥u½Ë£\x0013\x0014¼ºê<ëìÚ¨U$WãÈ³8L\x001a¬æ\x000fhRá	:l¿GJÁu\x001d\\x0002uæ\x00118*Vfrî±÷%7uró\x0003-¹«»qK[~xÉi\x001c£¥\x000eãý-¹ZWûWº9P\x0018g O÷=¨¥\x0001í¸tª\x0008\x001b\x000c\x0011Aæ0Û{_k²^éõÅ\x0019Ùë¦Îh#£\Í
EFÙ\x001c\x001c:RØJÄQy\x000eBLÉ³CáÞ>¸{\x0003sã\x001eÏ¤JºÆ\x001boÎc}V¤Z6HS-\x0015ilìP\x0015Ë÷è3©ï]Ëò/þ¿Ô9ü¢VÅ ðCüI/âqòòþnþØTX°\x001b(æ\x001cçÖ\x0012VZ\x0016MiéÖ ÒKøájòòìtzÕ\x0011ÃÏþYå©1&ºÒfûð4y»X~è5¡FY\x0014°¢è4ã\x0016Ï,6ÚíÕÔTûòzòvvñ²sNÆ

ÜPëtêEÌ¢ÞFÂÿUmsª«¹½?mmú\x000fÆòd!­Ø°hÁº¡à\x0003ì\x0007çèÎ^üÞ¸2Æ:.þXÄëWeÚ(:÷Bô¢ê\x0000ÞîØ\x000fÅU«\x000b\x000cqñÇ2\gXUÐDG1È\x00086cQ³íuÚ\x001b¼-E\x0016\x0004«°ª\x0010ÖZ®\x00143QSanÄ\x0001ã\x000cÛ©ÑqCcëâÏwqu­á\x0008óOÂÂFl\x0001Ï\x0012.>´(°>dg¶G#.®®\x0015i#¯\x000c¥¼«LU?\x001aE5¦¥K¡?¬n
Z
ÿà+ëKWÖ\x0007.c1s=QXNFwër\x000c9Â\x001ai:ÆjÚ\x0016Ïjµjú_ð5ÿk>¹¸ùvó×.{I+ËKu¤ÁHÑ/\x001då(
¶[ï0È¦ã·Ç³Y7sÐuæ°>Ða\x00084rRdE
E­^[\x001em't\x000fYkî¨°HÜÑÕ¹ãºÈû n#©a\x00065q\x000e²º»vlò\x0008½}êéPlÊZE!,\x000bü\x0017/ï¿,îæ\x001f¸.äv¾üôÔsl
¦*hÁÜV¤\x0000\x0003+x\x001a¹Ý\;¿8{3;¾äúéÅëëîÉ1Ä¿Ò÷A~÷\x0019Ã/M\x0014Ôx\x000bÞ»9pYfr\x0015åÞ®Z\\x001fM\x001d\x001f¯QË/Pv9Ûà×à&J±ãjê·Ý>\x0001§¿~ÃÿnºÎ¨ý£]lü\x0001(½ø#ý\x0001VÆ\x0007~\x001eù	\x0008Ç§ó\æµ¤æ\x0011\x0013Ø×&Ñ7+>à\x0017+;à\x001cÉåýÃÃý-\x00069û¼\x0001C2y6rL98\x000eÃy¹}P\x0018]«ç{1¼¸8»¼<;Á\x0018çNöU*\x0018Ùe\x001c	3©¥\x0000GP'L%É\x0004×A2a\x0001¿\x0008¿Ì«?\x001f»üUÅ«\x0011»jó\x001b\x0010\x001c_¡KwsÀðN\x0004ÙÈ\x0002½_`\x0016è\x00046ýOó§Gø§ó[ ë\x0015\x001bG},\x0012ÃØ¸Pòn\x0011ã!T\x000fí·pá_M~^_Á?ÀoÚ\x001c*\UÇUÅ¸ÆR\x001b,HÒC8\x0011KããV\x0007h\x000bíÎõ
uàðì×7ÖqãsÇ­j³òî\x0015Ï~?T$´\x001fÄ\x0008dÃ}ìØD9W«V\x001d>Û{f
«ÖðÌ­
Ï\x0019}µì6¼E8×®óopç[ýÕýÝ#`õµKÓÜ\x0008è­\x001a\x0011À\x0011eáí·úÕ\x0005\x001cÌ\x0017ú{uvz\x0005¿Ý1ÒèU^ýhôºN¯GÒ[Íã#|pè÷çDÃ¥Û?ÍVø\x001a:"7uró£­»«Ó»\x001f^6Ö^þh_+¿D|û£á7öüá6oàû\x001f
¿ÑæGû\x001fóÃÒnü\x0005ö\x0007ù\x000bT\x0010kñÞ ª6¤§ÉÛÅÍíä§ûåí}¯IzJ:Ã³\x0013¬0¤Eà\x000e/»]ÉøbÓÇ³ãÉOg\x0017'g]#ôZ×©õ\x0008ê¨\x000e\x001cQKEZºÊ	EÙ!è5\x0018ÚÔ¡Í¥v<Â\x000b¶\x0005ë÷h\x0011YüÂl\x000fRQÛ:µ\x001dA\x001d0\x0014DKÍÿVÜ\\x0015åö@E\x0019µ¯Sû\x0011Ô«aMATµ\x000fÕDØÑl99Öã\x0018f]}Ø¯OÌ¬êYí½LC©eãSc¾EXjCK­,ÉuãRó¶VÛseØm-Çìk¸6)/å©Ôå¢W2\x000eÚìo_ëæÁ7fµCà\x000e "iò\x0006­]%\x0014¹]¼{\x0010ö\x001c\x0016ºáNñ_b¼íþñæáañeq÷8\x0001°ÉôöëÍmÏV
<=°\x001cI§P\x0008ö§x9\x000fprÂoï:9»:¾¼½^MÐ·\x001ftumTôºN¯4zS§7?\x001a½­ÓÛqô\x001e® Iô\x000fÆ(â\x0000]LA+ýVÓªBwut÷£-¼¯Óû\x000b«Ï
¢0pHð[s\åô¡N\x001f~´µuúøÐ\x000beò¨ÚÕÕjpTmsúÁÅÍü{?p\x0003×\x0012|¢©ó@É\x0003
FgIÊØ)ïw?¸8þ¼Xù\x00061þXJ¬¹#HZG¥\x0000ÁXvVöö'Ö«©ËH?\x0016\x0012£}H)\x0000km.§8e!·O©\x001d\x000clbcñÇ2`xë©*\x000e7\x0005\x000elÏÀÖ7Ê]Ó\x001azáZ =áâÏÏ7\x0015Í×÷ð¼t\x0013çº¸b'gÈuJí\x001cáÑ{\x00137¡q\x001bBÃ>\x0016y\x0005Ê7ð6æ]¼=r5\x0000Y\x0018ßô\x0005Öí¯Z£æ\x001fzÊ\x0018Ó.ÈÎ{ «\x0010\ËÊî¶ÛÇ¼r§ñÑôe\x000fÎ-rÖÕlûâ:ª
\x0007Ûqó~´ÝÍæý8MÓ\x0014qº=\x0014,¾¬yÊZ%ÊÞ27w\x0018¨Õ\x0017¯K@©ä¦¬à°M\x001a,M+\x001a;\x0006ú:U\x0007uª\x0004T[; ¤"VxËÜ¡a ¾\x0001êË@ý¦-j#ß·5\x0011Ø8GoÎÐxó¡èÍKÇºBI}=\x0019}ÿcÐØhPß\x0000õE ªX¶ªö(¬Ê Ýâ"½@kãÒ\x00104K\x001bL\x001aP¯!V¯>Oåð±\x001aw\x0012]G°¨7©nê"R/¸{*8®ÛF9!>ðýö)tÃH­lZYH\x001aV¤Î3i¨HÇ\x001fP*ÄÆÕ\x0014b	©P8N3T\x0008KE«>ðØD'dG\x0004¼/©\x0016Ë	\x001cG*\x0003IÒ\x0002©dïK¹æ(¹\x0016ã1©#ùæq19/ç\x001fnz;D8¡¨\x0004U
\x0003ÐnWx=:¾MÎ§\x0017ÓÇ= m\x001dÒ>SHWtÏ\x0014Ò×!ý3uÈ8\x001cÒÃíN\x0013äÁ4¢iìÞ
Òâ<Õ!Û\x0002t¦QG\x0008±n0bV[É
¥)r\!µ½h\x0000¢j ª\x0002Dl$$a³j\x001bÂ6M:*·\x001bI\x0003\x0018uQ\x0017lGáqt=¿iÃ!*Á¯º%ó3±q@ÊgzB6
"\x00143ø¥{tÛÑ\x0017¡út<+vK×âÃ÷¡++¬\x000e]Ð\x0010¤Áö¥«å\x0002c½ÖV«4©5F"ih\x000e9ìÔ\x0018Áþ¥«\x0019\x0006(ws:·\x0019ÃiJUqSX[bú¸õ\x000eUAÜ®ÎíF­÷XMAÜ¡Î\x001dFq[Îß$nRÑáé²È½Õ@-ã®M¸ÿ\x0001¼\x001eF-8\¥( ­¤¢V¡ì°}8c!xãÃã¾Ì	8\x001cR)jUSE\x000bi
õÌno\x0016×Ëù·¤H½[±Â\x0003\x0012\x001e\x0015Î\x0013ô\x000eYÐ\x0011¥+Ú\x001bJf'Ç³Éë)¶Cîdv
f79ðØ\x0002Tw¤g«h\x0006ÇÜ\x0013sPuæ ~\x0000æúu\x0011rÐà\x0007\x000eMèð#@;ÛÆÎág\x000f­+­~VÍV?ÆJûÆáQ×:yÐà¥ð}-è\x0004ÖNldó^,æOýÆ+ãu³§bu iñA\x001b\x001eRê¶\x0017Ô\x0012M/fÓëÎ¹àD\x001cT8¨\x001fØ4Í\x000f@ÜØ\x0015áùï
¹ÄRRdé\x0015\x000fÐ³*\x0005ýsÕ¢¢d³Û+0ÃÙÐ´êð°PÍ}ñv~×¯NwóÒR¼vÁ\x001aMsÛkjÄo§§«æÊ&%\x0016z×(SÝ÷3Ä¬)û¥Å¥«	¬.$9\x0010Y.²ÖÛõ®7)«·ß\x0004­	û!hSØo\x0010¨\x0014ÄC\x0019.:æ­¼+·ßF*Â\x0000¦ÐBURûjþôîþiù©×ç\x0014#N=Êeâ\x0002p\x0002ªäºcÖÁõäÕôúÅÙõÅëïXc5\x0016²
î/	R\x001e\x0004*XÖ«òð®zå¨ï\x0011ß\x0017\x0002ËÀàõßÞ? \x0007ztÿôxÓKòH`n'K2DRã\x0001«@Ð¹\x0004n¶½û³Kt=Î®¯O\x000fßÏ?Ì\x001f\x001eí¤ªNª3©®êçLjë¤ö9º:©{Î¤¾Nê3i¨çL\x001aë¤ñ\x0019ÖT\x001fð<\x0015Ï\x0019µyô?ç³ß7¾~_òùK,£!W
Ø\x001cU#\x0004\x001eÉgdK¡r\x0013uÇª\\x0003\x0015,aÅ:)2OEÒÉM5\x001eµ\x000fuhIYö[Vx&ÖT6ü"KeWc\x0003ï¿|½éW=\x0001\x000eÄò³´	¢¢ùôÎÅ@Æ\x0011;æ£½9?î.õ ùª®\x0013Cæ¨iw;Oµ\x001e÷Ë»Eïr{t¬h<\x0017ØTTëÍwU;ØöÍp~2=¢³ÓÙR{- ¦­\x0016\x001cÐ?6þ\x0007)\x001bú`5|vIE¿\x0011vCó[»}H]åW	mf6«´
2f^e\x00103N?ËINk+\x00176Ò ,g[\x001c­!È*\x0015\x0002\x0019»Ê¼¡\x001bgqd\x001f|q)rùHªW}¾>'à$K^G©7EÊ-å¹µ³-Sà£K¹Ë+R»ÚâveÔ\x001b¨èÆ>STØ\uTü±\x0010\x0015Õ
r+£:Ò°)\x000f¬ùª0ÊlW¿ÜÂº6KÁ­Ï\x0014uµ¢J;ºÿòåé®wÃeäQ°¶äuñÁëc×äwÌ¢\x001d½ys}Ú5âÆ­O\x0016uµÉ¢q#Ç1ðCÜ\x001f*ªY]3&\x0007ñê:¯.äUÂp'?\\x0010\´¬
+·â}¼\x001fÞÚhDW\x001føì\x0016xãÅ/JåY~\x0007¸ïàþþ4_$\x0015â^ÐÑ\x00037±Ö\x001e\x00033\x000fV^òìZfÖÏ.á\x001e>\x001bnú÷ëé,I\x0011ï\x0006W
p5
\x001c·²ÙUÚ\x0012·ÈfKÁè n¡\x0004r»Õ\x0004=øÅ!þXÅ¾&çó\x001e·²\x00015¿IÑ7H)ÃUDÓ¥¬
¶³
çz\x0002×ÜWL\x0003LMø\x0006¬Ôb×ó/óêAVò¥1
.0K\x0004ÒÀ°%\x0002¯§o¦â\x0019\Ö\x0005â!þø£+Ó W\x001bGCÈaGPáÔ\x00143Á ÜðÔbÅ\x000f%\x0017Iå¦6\x0010R¸4\x0010re\x001cOo=s$ÆLrt:\x0016é¸s;'¶ËÜVv1Îº\y\x001eü/*X»V\x0006¿¨	.>öáÔØO
\x000fÞG6ß­V<c3noÕ Ïîtvýj7¢®#êáØBMs@âB\x0013ùª\x000b.t\x0005ïû1:£\x0019ÎhY\x0015;âp+Çëh¹åEtæÄú1ú:£\x001fÎ¨\x0015Wïzjo³²J>=,b¬\x0003Æ\x0017-XZ\x0004Ëx%MQ¶o´]3z1ÊÆf\x0005»QÛÔBÞ´á6m\x00194zÓ\x0017U?HÛ´\x0005+\x0019\x000eX\x0011ÇV»q¥$÷°Ý(\x000b¶ã¿±±!eÁ£fW\x0005¥ùè±ÅÊ£Ú.\x0017?\x0004²vÝà	.\x000b\x00162Vñ¨h;rÜ\x0010ÿÿc	mc\x0019mÁ2JñÃ¶[AMàË0¸íSúCÊÞ5þ<ü.ÄQ\x0012¹uÀRê\x0015ÎpÇ­\x0003ZØrÝ·
ß\x001aG¿Ý}XÞßõ¬À¨Æ7»ªcU[¾µ}ØÞ\x0000Î¾Ôdzúòâì´ËºÈ¸µqu«Jye\x000cóòÿkºsÞu\x0007\x0003zðfs­.\x0008ljIØJ°_\x0012ÞÀÚmÞ9
\x000fÉ­Ë\x0001ÇìµG+=ÂNûUX\x0012Ãµs\x0010Æ
'å3\x0006Û/¥\x0002`]\x0007ÖÅÀ!	\x0012eàj\x0008ÎtgâÎÀü b['¶ÅÄ°\x0013hpw\x0006j¥!eÕ¦Ø^éR@ìêÄ®\x0018ÎZV8u,\x0008Î¨¶qËíU@\x001cêÄ¡Xû\x0003cé¢\x0008\x0015±²|QD±·}\x001cëÄ±XùÚÍyeå>®¤Ý\x0010ÜZ\x0014.z:t(/Î\x001fw\x0004ìðÌÈqn¶\x0017p¸áXd¥S®±>xH¤ÁCu­#W¼§±Á\x001bC}ÅU\x0007MÈ¸Cò¤6o¥
}\x000eNVcsLÑëõ@Üíbr´è\x0017\x0004Ð\x0002.çh©ÑOçk/\x001aÅýRB¶4CWQ¸ÙähÖ\x0015\x0006\x000bÙq3Åltq³b>ºÇ~ºåý7ü©\x000f¸êª%]Ä«\x0010Á]4<õr{\x0017Ìûè\x000c\x001bë.ÎÞâO+ø*Ã+q\x001f«Z!\x0012\OøãáÉbòbÆ
ôÊK\x00119¤\x0015\x000c8ÙP
K¸DZf
L^LÓÓÖ¥}'Mh\x0016vÁ/Ð¦¸¼zHÛ`p6ÚÙêxS`bÐà g\x0018W·\x0008$]]_¦½Ðn#Wur5<(Çyt©\x0014ÍúðÁòÁ¬Åö®ÜÖÉí¨5×Y*	É+ËÈIDouVR)¸«»QàR/}JøeN¯
B¶\x001eÔ¥à¾\x000eîGí\x0015pHCXxG¡|\x001fP÷#òßz:y\x0018·Wrå­<\x000c{yÁ±\x000ccØ«ú¦t¬Q+®-4§½b8²ïC­hx{\6\x00159î\Ñ§y¥¯S²^\x0008/úö<U)¹nëq»\rj\x0010\x0005¨s>Óã\x0017Ê\x0007Ùz¹¢7ND9êH\x000c^±ô¤É=l\x001dÅèrë­YÞø@å¨/\x0014,,xÈèÔ==\x0018&ÕªowtKÑc\x0003=C`DÑVgál¿:ÏÍöÁ{äªq¼¨qÇ\x000bXÊÒñ\x0012Vä\ð\x0007î>÷j\x0018\jÅNÇ\x000eY'\x0011À©)ö¹[TãxQã\x0017¸ó©È\x0012\x001bVÈà\x ÅÖPd)¸iQàNae\x0006×\x001cØ¸WîÆÉ¢Æ,>²@<\x000eu´W$\x0004ZÕ\x001d/Eo,jÜÉ\x0012bÒ`ô@Û|5Ôv»Y!ºn\x001c-zäÑFÓgtO"XÖ¦ªUß'yãdÑ#OÔ÷Èg+7\x001aR:³Êo\x000f\x0007¢7.=ÎèÂyê´_PWÑy\x0000©
ÛG8¡KÛ¼Dí¨½î¥¤ÈÔ\x001aÏ¼Zþ7Xººiéê±¦nà2\x0006©$\x001fØÛÇg£ßãÙh|c¯ãåì
E©}Vb$.g\x0019ñeT^ô~6»skî?Ã?Í¿,æO\x000fuzZÎ?.\x0017=ËààË¤¼\x0013x¸\x0007T¾\x0017¹æP¶t*ÿ4}3^O^N¦×\x0017ÓW\x0017³³.ä#]Ýýxþê\x0014ÊâÆlÙìÃ¢×RcÈg\x0019x\x001c!d,¦³Ò¶eªjµÊ'\x0013 î\ål\x001bÈö\x0007@vªìÔsF¶b­
~qØªzqó
8Îf±üpßë\x0014AUÍ@\x0017¦ÖÔÈì£ãxRÛ¯ÕtÕã·ðÄ¡6³g»ÿ×ÔcÿT\x001c¡QqE\x001a¡ÿ\x0004Ù"µ=æO°?Áþ\x0013DdUs\x001cðAÁ¹ýéù-ÈíY²?am·\x0015Õ\x000cï¿Í\x001f\x0000
áÿÖ§Î\x0016î\x0018-¸_Ç[3lÎVý:Þù­7(ÿmzñ\x0012þ5BÿmÚø\x0013nÎFøùß0i¬6Çzôï}±à\x0002IÛ`¨JÑ;C«²Åë_éAý/\x001dàÍëçß0»1gr¾x¼yL?,\x0017}\x001c@Ù#²\x0006À©©Õ2¼Ú®ûÒÏ®¯&Ó\x0017³«@5ç3ý\x0001rc\x0016ÏÐ¿\x0000ÌDìOÐ4ªÌyÍ3¿\è³þ½þ\x0004!Snhå\x001fá/T1	gïO÷_o\x001eç·½D*TIe!¹µR±öCPÛSµ\x0001ø¿wv~|5=¡ô¬cÒ*Yehá\x0017RÖóXï|¾ø¾\À;èµßÁó\wfQL=K\x0005UÂär»¢[îÄzçóÙÏ\x00173Xþµ.\x001fÂ5¶kìóÆµªkÕsÇ­OJeä¤mú\x000c©ß5Ó\x0017"Kuõêþi9ùëÿ\x001c}?ýÙïs\x00079S\x000f\x0017%»
«dävÉJ8\x001d^]_L¦#¸\x001fÿm}QmºÅÍJôÌCSo {3¿»øý©_«Ô\x000765J%ª Ix\x0019¶\x001bPU÷ÜééÙåß¯g[\x0002\x0002
ÐølA­¨ZñlA£üå]\x001d5ÊÃwÏUétu­¤Ìà\x0017ëRfÙæÁ"¦uiLh\x0012µ<ï%Hú 
Û=a?XñpYé,5À[¯t¹z²~V\x001dÝ÷\x0013Q¨\x0008¤Ó
+%\x0005\x0007Ý=\x0001\x0007\x0011¶\x000fhSGg( Úªê¨ëÁ³@s
íj6\x001fÖÐzaÎåü\x000e·ÂãM¯rà"ápìÜ\x0000Ø\x0008*Õ\x0019ÎkgUÎåô\x00147ÁÕñôt»\x001dÆ£R5;Æ\x001dâÍÅM^Óä|~ûô¡\x0007³Á\x001dA\x000e\x0007\x000eÊÆk\x000bµ97mcgãI^ãä3MÎ§'×/»Èm|Ý¤yäÊ¨fûÂ$lí\x0018¾¸Yü£\x000f¬Ié­Üm\x001d²pq3\x0003t\x001e»üºÎµãÙÿX`ËlVÖÙÒ¤g\x0000\x0007¯x½>Ö,\x0014b¬ð¯ÿì\x0019,ôÕ\x001d¡xaÄ\x0002dºNåµ\x0014,äpávXUUÏ\x001cV×aõ35uXóÌam\x001dÖ>sXWuÏ\x001cÖ×aý3
uØðÌac\x001d6>SX\x0019UóR_lØ±éþ_ôë<\x0007£Û±f3ü»(Ëy\x0014è5Ý²\x0004ÙéÆÛ­ç5\ñËÓý§Gý=éJ\x0003c~NËÅcr\x0014Nîn¨Î\ÑØHüñ§O\x000b\x000cÛ\x0001^T\x0018ÂÕ\x0018\x0017U\x001eC(ÉyàL0¹?Á9ä]_¿aÜmz\x0001Ïä\x0015\\x001e§Úòíýðâ\x0017£ÍÝ\x001f÷KÄ"¼ôÿý·7··óO.,\x0019MÈãIU´T\x0002\x000fXÒbá»9ÀÿB»\x0005ÿòíñÉÉôu[¦M`Õx$ü\x0017é¬OXlÛ\x001dÝß}Ã«Þ\x0007. dºú%	-¬¡±\x0011wtvúr
oµ
Qþòå)¾K+\x0006èRþõÍcz\x0002òðõünþéþÝÍ"ï1ØñÙ#U8s\x000ei°í\x0019ÍÒoÓÓéë³\x0017Ç³\x0014}|Ud7^]\x0003\x0004\x0016Zõ\x0005Ñ:Õ\x0005 HP91\x0003 8V6qä-ã\x0000\x000bB÷^\x0010ÙÃ+,J\x001c¡s¡\\x0019\x0006îä¾\x0018.&û?-Ë
_8}%Vë¡Ë9à³}9¼Ã´=\x00026È't\Òö\x0018ñZà?êúr`íeúªQ¼"7[`)£f\x0010\x0003ée p[û¾ !
\x0012N+âÀÏ\x000b\x0012\x0015.AÙ\x0011/\x0006>µÐûÅÀë ïÅúXHoÆ\x0013ô#\x0016\x0004.ÙØ{§úT,®È\x000bâ,iAÄò\x0003\x0004ó\x0018ø[$¤r.Ü"Êf:Ü"WÄûò½½ì{¨¢6¥Íªm®æÇ\x0012sG !k¤À[}\x000fU\x001c¤&òçëp¤P>Ýª¾8b·b2^ö=V\x0003\x0019ÐÀ.ôrlä5#¶+&\x0000eß\x0015\x0007 ÑÉê´ËùD$\x0011¼&\x0014Ó,#\x0017+{­6òUãdW¯Èg	u¦À^½OWoSuZ\x001385ù1 p²Ê¾§+66àt\x0007\x0004	2\x000bÀËq®½¨\9)/\x0006¶\x0011þSÏ3E¦ZtíèÜÜÇ=v1çûÏ·mí­üåÖÌó¿6Ì£ÉÅí·¿þùá¯ÿL"í4F±±\x0006\x001b6\x0017\x000eaPÐ\x0013qv}u&/f'oÁY¹h7\x001ck@l'=\x001b ¶
\x0010N½tV\x001eD p=\x0015Ù×IÍ!\x0001y·nP\x000e\x0003b\x001bêÙ\x0000±-õlØ¨ê\x000bä¼$WÉõF\x001eM\x000fÇÒôÑb\x001e¶­	ÏÊÆz.@©õ\ªKýÿW t­"Lù\x0017+À§ÿ¶/t\x0001¯\x0007@Rõ:CªáC×°\x0004Ò4 Íót
H÷<!}\x0003Ò?¯Mù\x000e\x000eÝÆó\x0002Oaürîï\x001e\x0001py7_~è3èOºälã¤±\x0003\\x0005ëPèÖðìô
À.N§\x0017/·c\x0005ÿËwù1,¾P×a]|-)á/ßÝßFÊ}OÁ\x001f¢àÊÍâî.)zhÓªiasXÄGðª(|\x0017Â"\x0002ÔM9Îê\x0019G?M/^fM\x0012ÒR¦Þ\x0000Äví\x0000q¬@vrtÒ²ò\x0000§<ó)ª7\x001a\x000f\x0002gJð2¹Â\x0005>\x000e0\x0018m^@çøã\x0000W]íPbéEz\x0014 \x0006\x00063 ¢ò¹\x001b\x0013çë\x001avÎT¿\x0018æ\x000c\x001fæçpÆ¢eÉ©\x000e¨wòÉÖ\x000c(m\x0016B)\x0004üöð«ÿý)mBtOêxØDtZÁ°=ÎQ¸\x000e\x0018v\x000f| x?%6t÷·³a¿Ð	ö\x000bí Â¿Í\x000e¤zÊ¯Ôb]\x0015QÙ|ÖIÌåL\x0018®>LAP°T\x0014\x0003@í®¼ÍàGRy²Ê`ªO\x000fð½Out°Mcí\x0013x¼\|\Ü}èÜYØ/(óÎ2°ûs)l.
cÿéVªk\x0000{5;}Ù¶­*,\x001eaz\x000câ²¨]l3¥VWG¦*ÅL=þ\x0001÷Á\x001d¡§âóÕK|5ÿæÛ¨tt2I\x0001ãiëIÙÎ§\x0000\x000f\x001d¸^¶Ü\x0007WÓ±4~\x0007\x0013
z(SrÄÉ(¢pB:2Å\x0011G\x0010a®õB\x0010y¶=\x0012åÎ| \x0004¤TËyÚ\x0008ëöÜ@¢(>\x0003¾7\x000ccç\x0003AYIÖ\x000fN\x000e\x001dÅ\x0014ÁÃbØ{\x0013pÙmátî3ò8h®F8\x001b¶ïðÞLkçAuòúÀÑö\x0016GÑ5#pþü\x0018\x001e)'<l3)pFø.D(Å»[Q/\x000e\x000fÓc\x0008\x0011¨\x001b Ë}V\x001eSÏÄdCÛýÒÅtçî\x001eÓõ¢°K+=jÂk0¡±°¡ëÐ\x0004CÚµ¡*í(x¥ÒÐ½\x0017ÚÎËÉk°¤±¡íØ¬è4\x0006|Òc(]ÊpR.\x001c»êÓá	÷¡Aú\x0016Sa7Ý­7DÚô¹¡~Ùäæ¹öÏ\x0010O¨l¡+Ç&¾²\x0004QíFr;xÖMç<(\x000e"Çø\x0003ÂQO*+¶oø.\x001c¹XßR¬\x0005¶í¡rõÝ~2§Fñã\x001cÞ[\x0002\x0012xt\x000bÊ\x00198ÓjNLsKøvsê\x001fïìÇÇtéÁ_¤\x001buÞç7÷Y%°Õ>ÐÒ'#´ÚáÐÊ§¯r.¶1\x001f%eÀ\x001dLx¬¡LB¤â§´\x0004\x001bÃ>Í9ÉîlqÇúR¡ÍÙ´;{PéÜ[|XÁþM\x0010UJ=¶ÞÇ=©P;-¸¡T\~ð[MbT×Ò[+ßIz\x000cÁ2.\x000e§|îÀö1Ý|t'·]ÉPöÃ;õ k) \x001aÒò¯ÿõÿþß\x0017÷O9HÒîjÅÈw³¹\x0008=­À¦§ö­\x000bvq4yqv}%;\x0000ñ*l^\x0003\x0008¬¬,x½>ïéxB´û@Ä+\x0013\x000b\x0011ÁÒ"U£è¶M
\x0003Ò'ªÚ!hM6Û\x0018\x0007 úª\x0014G;D\x0001Ñs*?Ú°UÄþPÓÉn
Ù$3ºº0mlsùwóýöýöÓ·ßÒF\x0014I¨Qßyqÿôý¯ÿõ×ÿN±Îv<­ènpØçaóKÎóyR¬S¶8µ©¢óâìúç£k\x000cwî Ä!lÁ\x0017\x0011J\x0017ÓÐ\x0004ü(#¯¡u´*¸6«v7àÇw\x001f¾|âÎz½<¶$ÝÜ=\x0002âûÏÝ!EÅ\x0017\x0006v¥y*
NÊëØv
^NO¯\x0000ðè§pÑ¦t!²G Ï)h +]\Ûm6\x0000\x000eM¾P\x0002\x0007\x0008\x0014eW¨ÚÏï\x0003²à¶}»ýéðýP5¿xp»Q\x001d\x000f#H
gÓÑ"s5p\x0019ûtÿñ.nýr\x001f&oo>Ýu;\x0007pª%\x0019\x0002ü"0$¯7}Áiå´­ÞÁÛã×§­®Á\x000b#Á\x000eå
.IÇ¥/µ²~u\x00124Éªo
`÷ãXô\x001eÃÀKJ¼IïÆð»T±©l[ø`\x0007Øû_ûöû×º³PíÖÃ76\%¨-
ZI¾qå¿4?ÏÚ\x0018·.çx\x0005ÌV\x000c\x0012\CSbö\x0016dà\x0018Ñ%TÞ>¬OµF\x0015Ôn·\x0013ÇüòIá²î¦Ç95lÿµHbÔåèÕòÙ?\x0000ÈTá(\x0015
\x00075´t¼F£hr\x0019Í\x0000\x001aôÈ\x0008\x0012{ 0\x000fHË\x0013Ýp Ûß??ÿHg\x0014ü§õÆ¨ÈóÛ9õ\x0017´\x0016\x000bè°Y£\x000e%j%ç³¤kÝßØ-r2M=\x0006Ûm3óÓ»I5èú\x001bgRÚÕ¤±èpÈ+ÎY¸\x0016g©!ö0 W\x0018¥²\x0002'\x0008\x0013¤§z°±êGðq/\x000eN
'J!½¯r«B¡Õ±f§ÈE)äÍ£Ry
ïÍx¾\ôz×TóGHÌ¦26|\x0007Þl×\x001a~µþéÏz\x0005Ó9ÀÍ?-&³ÇåüîÓÄ |\x001døÅµù\x0005ë°Z;ÛÐ Úôõl2»¼º¾n
\x001bÍõû/þVëÃá\x00014·ê}ß?<v}Ép\x0000;J©Â\x000e´Y\x0013\x0016\x000f`Ïõa-,ÂÓ;ÓÈª£ô»ÉùÙåUÛç\\x0003Í§_)(:Yqõ©D²@ø`Æá`£@?<}ùôñK­v®ª-9ú\x000cÊÿó¸?í24íC\x001c¯N¯Úª\x001e_øm×£&W³éu\x0004/éÃG\x0004ÃÔ(þ£êNu¿|?¿ý\x001dgÌt\x001bI¶ªz\x0011)\x0005®@\x0011q\x0001.Dó\x001a©ÚÒ_]\x001cMOþ#evÑ)¼©Óc \x001e|$*
q\x0002\x001b.À"
\x0007oK´\x001c\x001bå0=\x0006¯\x001e*üh\x00159®±')Ûäq-\x0016=\x0000ïÛ?~³õ\x0004EwòÔé<çô¢ª>\x0008KñhU\x0015Ó·¬ÙI»Ï\Ñ¬T½q".!T\x0017E¦
ãxiFð¤ÃW\x000eâ\x0001ËR2a\x0013E+Y]­Ê\x00002\x0008d\x0006\x0001yd-É \x0011tÒ\x001a§+SwÌ\x001bCÓ==ú\x0003a\x0016ïuÛvðD5ÕÝ´À\x001b\x0008µH
\x0005«Ý@úïÊÈ\x0011?¬¶çXøZÙ0\x001eô¤\x001döÆ,}ø\x0000ä8«­bë[¶}øý¸|fÀ\x0002åÉf\x0008TóÂæÌôc>2´\x0010ÓcÐÖ\x000c\x0014²¶yÚÓ¼Ö+ï\x0000IaRÓ¸\x0003p
 9Ø»(ó;"[	Rá[úË<¬*;\x000fë07îó¸±\x000eR¤i\x001exõZQ\x0005a\x0005{JÞ°èòøõY\x001a-¶\x000b*çRAÙ$² ¨%\x000c¡e(\x001dGBå\x000eAPÎp^\â>ç¢"öp\x0014×8(<\x001dÍÐ¥²=pôt-QÉP5ÀÆKÅI¡k\x0015iWEÅ\x0006^\x0015k¶\x001eÝ½©ÖÍ^T²²a­\x0014`iaªµÒã¨<\x001cN^\x000c¤Ât\x001cùØ8KÞ u\x001cÇWjä\x001bÄ@\x001fºÛQ[Våò|µªÁ;|Ø\x001a\x0004\x0015MN VÞªì\x000c*3ò\x0013ÄjÅ`R¥9i³{@ñ\x0007í9Ó\x0016DiÙ
¬£\x001fD\x0005NK<ðü\x0002uuõÅjWq»Jâ¹\x001e¨`/YîÂ0\x0007ÁpÎPåZL¾Xx/,ÅÅJ\x0005\·e«\Z\x0018w\x000bb´ç0=\x0006aÁå\x0017i¿c\x001a"[¦
~`/Á(,tÂÒc\x0010¼áÕ\ã`jr\x0018#\x000f4ÌJ\x000fÝ[à:q#¹ÒUÑ3¾Ú;\x001d4Öå¥Ç ,e¹¡sÓ\x0002\x0002½D°þÆÝ:©\#=\x0006aPa¡>\x0015º\x0007£8æ2ÒÆ28e&=`a\x001a!d,¸M¹\x0004ØW
8.´øXÝTAè?ü×z\x0015ÛÅÓfïÍüfy³#±\x0000&\x0004\x001d\x0014Q£\x0002%\x0016Øknmë_¯ÇøÞL/Û8ÿ¼ùõnqâö=\x0016+Îy5dºÛÄQU½[YÎßjðk3Ì7­¦Jï&£\x0010ÿ1,VG¬MAçìU9w·V"\@"Mº,PÖýÀ¹Ð4\x000c3»ý\x000e «èad^b!`>ÑDm7}\x000cfÝ²èK¦~ýó·¯<g;M×~J¡äóåâáÝ÷Ç¥1)öÀ¶t°\\x001af?Ò°
í\x001a3\x001a/~¾ê(Y¡qb{0ÛªÙ\x000eË;\`3/õ6\x0002¶ÊW\x001bÆfp\x0006\x0012£UUc`­Aa,\x001aÎ°òÃ_©\x0011y$V\x000eØ
þ\x000e¨l~\x001c¬ZÄvûÛ·ûûôJõaÊlWÇùÝM÷é*³\x001f>\x0003Ëï³²ÎÖ&Àu5»¼\x001ew@UäñpõZ^\x0005Â\x0017_¾Î\x001dP¨(èb\x0000!YÙBÛÓSÙóéÅU[\x0012\Ð\x0008<~Úcqí^,\x0017_îïºÓ¢\x001a\x0007äSÍqâÌT[»å¸}\x0001Lg§m©F&Ò¡NÄçm/"Á\x0001]ì25Mæ×-¡>Lô6V¿@å
ÚüGÿú?w&Æ¼^íûªyE¯ìÆ°n	]SZlÚ\x0015c²,\x0001ÀdR
D3«\x001cD\x0011«\x0016«ë|=2\x0004Më:ÖÃÐÀ¥à3î{v\\x0015LY¯/\x001dfD\x001dÍh
©LU\x001e®]u7Y=\x0006Í4ÐÌ@4ÁUÃJ*Kl+eE³ýjê\x0016\x001aha\x0018\x001aÎ¢¢\x0001'½¨¸Üo ¹c®RèÍ\x00057¦¨J°tDÄ\¢PgfÝ7\x001fæ\x001ahn(Z¨Úæ:0\x001cc\x0011|Û-\x0007Ú\x000e´ðËîiñ.u½á§Gå¡T®ÔËùÓ×Ï©¶Cg\x0001]Xz¾8½Ò4ä2½R)ÀüNªï\x001eÃQI>?ÚTF|«4på¦TÕËéõùO-u\x001e5ØÔ4\x001e¥°BSòHó[<ê\x0013gV\x0015´Û\x001b+Ö\¦G!«@Ã<%(\x0004\x0016äe\x000b\x0013\x001b\x0014ha¤Úë}À¢\x0005\x001e¥°k|°µ</¬Aõ\x0019VF§÷\x0006é¹ô(ÕÔFåk\x0005ë\x0006\x000cÁ²Aµ\x0007X;@Ù\x0006°9O­lÔgî\x0003öofX+ö\x0006\x001b0S\x001e¥°Ò¢¤!ÂHc+\x0001Öº¼
LjoÛ à\x000e\x0008c¶ZÁ@5->8O\x0003cö\x0004+\x0005\x0015Ù´\x001c\x0014¡0ÝEgW\x001eþmK{Û\x00062Ççgé9.ÃZ5áRp>aÆ¨öEZ¬ó³Öaß/º1\x0012Çcª\x0013im4Y^Ý`Yý¾hQVú0?\x000biCù\x000e©\x0019\x0011Q£Ô´
\x0004g­Ç£*,:9ÌÏ2T#LòÀ\x00105õe\x000f\x0003\x0010V{·¯\x001bL\x0019¬jÉÏBX)ÕÎ»\x0000·òfa)°{¢5Åpzz.-¸FyÏ\x0006\x0005{VIZZ7BÊ¨î\x0016W5?K÷l Æc ÕIB0Ê\x0010­ûúÂPV>Ñêâµ½M\x000f@ëqr1%[±N$Ó×¾¯}%(ó¢
p#uÈ\x0011\x000f	W%\x001e"u\x001e|
¯ã¾ÖÖà9s;\x0001»&´ÄwõQù\x0004\x0019û¢ÕØ¥7\x00036gæ¥õ8|-_\x000c\x0016¼iiÍ\x001ea±¦#?Ka¹×\x0015i\x0005YÁ¢gL´f_®1hwåg)-\x0008yi
\x0010&C`\x000fûúÆÃÏ5?Kaa«ºtye\x001di×\x0005ãLÞµ2½Ùµ&¦°zÒ»SVacÙÁDï\x0006°>ÌXÚ_õûø¡>\x0002ez÷ay·Jw>~þëwýs±Ã¨Õ6ßb
}."Å\x0008r6Á\x001d\x001fØË³SNx^ý4;m¾7 sO^!$.§Êp
äè;Ü\x000cy:@Zµisõ¼ýðñýowuÈo»\x001c\x001ezyÿþqñ´\x001cÍ\x001fn¾Üà?ß,»Y\x00156Ëå
t\x0019¥À4ròiØ>tÉöZc};;Í!£gGW³ëÉÑôòøÍ1þóqKf£k/Ça\x0003k\x000bJtr³"^òÅxõÆ>\x0018»"Ga\x0007g(Ù qú»Ì\x0004¯¢%lJÔï:÷\x000f£6â×:\x001cd¥Pïb¬¶³Ùû\x0016ÉÂà£¨Ñ¶Éê2ZAG2cK-ö¾Øyº÷aè=nÍ£ÍÎ\x0005,:·äÀ\x0008¬zõ]Ê»y<ý#þÏ«Cü§Ñû<×oÄæ»Gµ\x001eZ{±y\x0002\x0016Ñÿùxû¸x¨_+\x0019ûv19_<Þ<N^,oæwÝ´\x0006+ÚÒ\x00069Aìe\x0012MA('[hOfóÙÕñÕäÅÅñôt{«w\x0003²qb\x000f¬"$VDòßÀÃ ûÇ\x0004c6ü·BÈÆù<\x0010RP%%Ø\x0011J¬\x0001R;Ä$Î~ \x001b§ñ0H0qrw\x0001Xzò \x0010ÒD~ÛIòy/¹¿ÑqxÜTå?\x0000ÉqQæÛ\x0013dã\x0018\x0008\x0019©Ì\x001f\x001d½\x0003\x0013y%\x0019ÕÆCæz \x0012H\x001d5	.\x0002¤¢Jv\x0005\x000c\x0019÷ôqs¯s\x0019%\x001fðoã\x0012\x001c/bJ\x001föEI#\x001c^¸ö\x0015¥a_ÜKí8\x0000¾%J[HI£´Ê(#¥³Á7\x00023v%@aO_7ÏØ*ûrDµ)£g\x000fA\x001aÊÑ\x0018²ß\x0013%Íß*£DqÄtãÛEÆªä|"\a_o¦xA¦B¿D	÷x.)ò)É)Ãf,¾ÆvÞÞ)\x001e\x0000ð©S\x0006Q:ú¼£ûzß4Ò«ôöÖd\x0007a%°A»2
»¯C\x0008Û\C)¥_½pwÀÆ­Þ·Û×ûÆBÂ[ÇH_}à"E$J,× [g³p K²ËNJM
ø7Èê\x000bWÏsÓâD\x000f¤!\x001aÅV!HÁî'X\x0019|5}½pÎ)¢Äöý|5j\x0014ë'JÇ¯×fOß\x000eW«QZ.\x0011Áµ\x0014üñ¬^ø¨]ùùûjÞØû§ÛÅ·ùòCª\}3_>~_>°Úá_ÿ|¸ÁbÛ÷;Âi©)Ópäm¶TÖ\x0012¹±g\x0005ýâe*f}3½¸úùâ¥\x000fgÇX~ÛÒÑ ÏnÚ~è£¢£Ò£Ä~\x000e²+Ëô8\x0003uÏôÙÛ\x000f=£§9E\x001c\x0005\x0005há7ÑèÙ«Û\x000fºâ³\x0012\x001cl\x0006\x0006ÜADo6NàÑôÙßÛ\x000f½ãÛ\x0012§øf5È \x0014e`ñåÞw}ö\x0004÷ôÍ::h`ñ\x0015©æaÛw |½aÆÏÓ
÷ï\x0015\x001eyõ5ï|Mù\x0010Ø;nýb\x001cM#{úh
µHo\x0002ÕÖ±+iqë¾á³{¾\x001fø ©E\x0018v§bä ª*Æh6\x0002cñÙ%Þ\x000b?\­ÕÖ\x0001GTÒ\x001byõ^OSÆ'Gt?ø2É\x0010åëÊP\x000bUÀÑQÄ/7ÊÆÊøýÞ9Ýb+\x0010ò×§w·7¿?íJ·¡ªK\x000e[ð`²zÍ\x0016cþëÈg×'³·Ó\x0015íùõã¿_÷ Ý´
Ðª\x0008þ~V¡NI*qÂÒ\x0016:\x0019·\x0004(ÆÐn^¨Ãh
+Ã\x0000­ÇLaN\x000fZ*\x000ezÃE\x0018C»y\x000e£õ4ÃDÚUx*X¶µ¼Ûð²ÇÀn^Ã`±h£¯2<î 6"~c`7/Ç+kªµUM±¥\Å	Ü{Ý¼N\x0006nZVH\x0003UÕð\x0002´L»y}Ón»=\x0006âú\x0003:¾¡¡d+\x0011­\x000f{\ÛmÅÀm+«m\x000bBQæÝ\x001b^Ü°Ïµ¥À`9­P\x0014\x000bÅÔÝY`Í»×­@Á·b\,ÕÍQ´\x0017\x000cÕ\x0007¤Öº»QÞ2\x0006\x0002\å¸'8\x0002®¯¥y=ï\x0005½a«¹yëÙõ\x0011GfÜ\x0006½:Ë\x0014eqÓ­\x001d
ýëþ ñ2\x000f(©èöË|yó~WÅn\x001a?\x0015\x000b\x0003Y\x0013=U>)¶~CÔf=L¦'`\x001d\x001fí"\x0018\x001eÍ)}ý\x0011ñ0H¥å\x0001£^¤×F\x0011&Ä\x00106>¯\x0002D%Sø°h\x0015Ú\x001eU\x0012\x001b-©
"Dky\x00157í­\x0002DfPz\x0014 ¢\x001dhri¶<"Xþ´ôû@LªØéQ³êRÓ\x001eV´E®¾Ô\x000c\x0000­X³p\x000c¢Ls9ó³Q*ãX1cI¥Å§aÑ¸ñ\x0002FDÒ³Q¨7<ö\x000c¤>M2Q\x0005]öð_ëÊ×ñß~Ã\x0006Ò$\x0019\x001e8ývß]\x0002j\x0015ÐH\x0019ÀG\x001dò `ggC?´,ÞôíY[Ñg\x0005dQq?=z\x0003Y¶\x0014©ÒÓá<W\x0000\x0002ç³ a9e1PD0ÖUí\x0006rN¡`Ã½\x000e@yÚ­Tr¶Nê"ÙÝ@ó/·\x001fÔç\x0017Ü\x0018\x0008ô\x0002?Üð|ö®«BQ¯\x0017\x0006©èóÊÙ¼­Q\x001bwZc,ÐéËéååñ¬µÎªÆýßBNÏ	'ø\5-(Keaf£\x0005¥r}VÚ J\x001cª\x00113¥pÕÄ× x5Å[Ì¹>fi\x0018'Ï\x0001AË\x0011+3rÛ	9\x001d7ê÷9³g^Æ)e¤98JùÈ°·8Y\x0015sf§¼p= Í%¥\5Y\x000bËãÓû½­göÇ\x000b×\x0013Ç÷HZOQÉ\x001c¡d\x001eqîí3ÊQéÒ×îhR³ç±L\x0014;rIå\x000cç\x001fË»ûßc=	¾\x0002}qs{»x7ú°Ë\x001bpé\x0016Æ¨3Ð}\x001cè\x0011J¶\x001cêÀøâøädöbzýr' \x0002\x001cjQD\x00180ý©©:Us[¿3Zrá§Ý\x000b"±êÆäàþðá\x0004JÑ+ïj@td\x001d\x001ao}»§Ò\x001f\x0011eÙ\x000eÓ£à=\x000bVD\x00128ÔV\x0011K®¨\x001dÚÛv\x001b{\x0000b\x001a0Ù0Ù{\x0015Q{J\x0008¼§ÙyÞ).\x0019möÅ0B\x001c5nbÑVôç¤Oß³±*\x001fØÇkvé\x0010\x0017®Pèªé\x001dìµ\x001cK3ZrÁ\x0003ØhU\x0018@h?ý±üU¶^÷_ÞÍ\x001fv\x001f:4q\x0007M[_´Ì-UE´íxÓx0½y1½xÙq2®Hñï5\x001b7MT]e³ÀÔå44\x0018áQ÷F\x001aPa}hgR\x001c×BMW5éP!©bÚj½QhQ*qB¡Ü\x00180:`U]ï¬(\x0019\x001dó\x0006Táõo´G\x000cdÿúéû§ çªRéQûîïîòp¨vF2IO\x0017ö2im\x0007*º³Ä\x0001k"oýÎNOÛ¦CÕØ\x001cþé1M{¾´y¤C@Uw*TT~£$¨/Ü§¯J8l\x0001L\x0001
Õ<æïæw;¬\x001e\x0007_t8K¯qa6ÎH"Db¼©ìhúbÚ"Y\x0007ÃCV5¯^`°éò\x000bõ\x001aõ\x001e³9æÉ¸°ýÚ÷\'ÙÒÆ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Åç	þs\x0006y\x0014fÆ\x0000aèG6Y±\x0011õ2"¸.f%«ÌØG*lû×}3\x0010ÙÆ~doXâ\x00036Iª<Æ»³­Û×!\x0008<®\x000ci\x0006V9\x000céQ2»?à=$qØ}7Ò,}1ñc'³ÆÆ2+xû\x0018§SjÙÑÜÄ¬¬\x001b3ãÇnf§Ó\x000eN\x000cÍINQF£s¨Bt!ëõQ&\x0019h»¥Y©ÝcÇ¤CKÌä8o·%^»c\x001c\x0017 cU¬Ê÷>
@ù Æ÷\x0014.nw\x0001j$\x0006ÚdâFA6X(v}\x0003ðäòæö¯ÿïËüÅ\x000f6ÔÓ\x001c.*¢à
ï¶õ^ù\x0002àÉÉËWÏßÌ\x0010Ã>ñ(vBç\x0007B/\x000f	P\x000fÎa;V\x0007¨¬(\x00011\x0002\x001c
kðúêòîîò»gw·\x0000<\x001bU*e3cY¾àJMI7hð½)áÄ×ÏOÎÎ`\x001b>{\x0005ÜÓÀÊ\x0015ÀÊ-!¶i5¡ÀQ\?$\x0007\x0011],0ß\x0013³/}?³µ\x0014\x001dÂ¿Ý\x0007\x0019xÂFµ\x001däèbÖëÂÈ\x001f{Qd+\x001f1\x000fBØVKÉÌr·
}\x0013³ÑÅÜ0ºnxðÄ#Ý\x0015¥;*B9à	Â\x0006`·d"°\x0013v\x0001°\x001a¤]àX\x0004\x0018âÀ²Lf)³\x001bùÚð2_;²_ÜÞ|Y}¸Ý$¬T÷/¢·\x0014­sZðá#"8kàÓã\x0017¯^¾9~ör\x0006×¸®\x001f×:ª\x0003È@1\x0001§5ËVª)²\x0002\x0017òåA\x0003¾±qÐ\x0000Ú§«ëÕûYI\x0005kU.Å\x001e\x001aE\x0017Vt©aw×Ã$Ö§Ç§ÇßïVU RUª>Ò(sgbÔé\x0011ìÜ`b¶rwºM\x0003ª)PM'jÈE&Ø\x001bR\x001dÒF\x0016\x0014³\x0013{E5g(8C\x0017' ³1pj.·\x0012¨&K`õÔ\x0016Q\x001ay\x001a:ç©Êe»Éhù!×N\x0018~ûnJ¸v\x001eUç³û¨x\x000f\ñ
[ðgç¼0p\x000f"ß{`@úgå\x001cð¶{WÈÅÁÓWàÊîö\x0014õFê\x001aR:ÑC)\x001cBJ¬Íw¯qèBäÍöÅV+æZï\x00051êÀÔÎRÊðKJ\x0018°Tµ\x000fÛ4õR¦@ÂhvÊ#[äÜ<¹½ºÇ¾¾»ºyW\x0011ér\x0004Sl7¯¸Oy¤í:³åÉ«ççøÏ×gÏ_>0ý	:\x0016Ðq\x0001tÊ\x0018¢Nê°µ*JÇñ»Ò©"Ã\x0016èq\x0005'@oTp6RKK$Øø)\x000bO`B\x0006ô¬}-4ü'RÛ(µÑ\x001eBÖ`¼Îßõ?=È,}\x0019\x0002n¥Ü?ÍíÌÀÌ¦ë\x001cm×îÓc\x001aP?jvëðã\x0008ôÉ_ÿ|÷±F/ÍêÐ}\x0001^ð|2óRlKº¬AÀoìÖL\x0013.g´Ê\x0007ðVyvÙÜFeäØà!O\x0000Ds\x000bµGnå×¹xi3¸ØÝH kÉN\x0004õª\x0007Tãä¤Îyª\x001cË?áõîrJ[PÚ.ÊèSòMja\x0000@ý¶6J+¨4n\x000c\x001f{H;¤áÜ\x0015ì]À \x0014oW¾Í5¦1òBz1`!µ\x0005´¬ ¨}TÒ³ÐDRÍÊ\x0011-·\x001d7|<UÉµ^C\x0002K\x001bÉÌÙÿ¨À,9_=\x0004\x0016³\x000evÛÛ$\x0013&á:\x0016p#\x0016\x000f\x0007¦ÓÛ\x000fó	KØZ'kI\x0008\x0017\x0015Ë¢\x001c\x0012½_1Õ\x0008æçpd:8}õòÙî%\x0002^ß½!pýÀC7\x0005ç\x0002\x001b\x0015©`%¨°;Ý¶\x000eXdµõq¯
Q8)÷\x0007Oÿú_ÈõÇ,­É}y1 \x001dã +¢$G´'dENÎÁÂoÿÇÎå#`_\x0003À,\x0015èNá!:e¬\x001dTd¬	l\x0000C¡\x0014Ã\x0012ÇF;n®\x0014\x001e\x0011\x001a¥©Á1âþËÝhátþ\x0018®\x000bà/ag Î¬\x0007/og·ÄÔ§´¸ð´\x001bfXÔ¹åDàí°/uf=xù
·C¦â_$:ûÓ\x001f¿Ú\x000f«»´%ÂÞb\x001a§«Ï_V\x001füÃ\x001ae\x0018¢´\x0003åÍåÃÏß½ÿ¿^}»DT\x0015
Øñ\±¨`-ãòã\x00078u¹\x000fMbgGG§ÔÕ.y[Wï9ÛøöaÅ?ÆËûîûWÿ8\x0019¹MO_¿9~\x001cë\x001fwvÕ°?Å_àu'ß	þs²°\x0006O?®>}N«æ'yÊ\x001a³ZÉ$6\x0005?ó6_hX	´K?\x0011ÚA\x0018°	þ\x0013T{ñ:-·Yp<øi½\x0004ÜsÞ î£28uq\x0006ðtY°wðT\x0015U´Rm&÷ºBj	Ç\x0001¼Z\x0005pgòÍ=&dàó¾Àoß¼ùíW\x000c{c E\x0015Ñ{\x001f0\x0001þ¾\x001bå\x001d©Á\x00118\x0001IT\x0017ÏÞgÃB
ä~§M`\x001f¼FÃ¼£XÃþôYþòþæT®\x0001V©²äønu÷g\x001d2v´´\x0019Y\x0019\x001cu\x001cêh5Ï\x0011Ì!\x0002äáïÜf\x001e\x0017\x001c\x001dý8ËÊ«GÒ~hìÃC3\x001b¬5Ä\x0013µÏ=w-@ÿ\x000b¨¬zôRcÓ¾´±\x000f\x0011Qö'QËÇ\x0011/\4{¦6x\x0008Kî	¢èBOá6\x0019Z³=÷¨°´'èÕÍ\x0007õç¯)¸\x0004n¥+Ï\x0011Oîà\x000ff\x0007sÞ`´_j
þ¦ÏOS\x0010ÄJb½Ó\x0006dä²?9ßØu¹kºz÷9þröx ¶å@?{¸üónõðþö¦j´½\x000b¬\x001f«±±\x001f¸\x0003Hn)\x0013ÝJé®&??\x0000§îÇ³ãï_½Ü5ækzL$j!¾wùÜøé'A|\x0013f||«ÿ\x001a|6e)>÷cH£ï4áçîí?»ñôâ?fÆ{ðs)8ja\x0012\x0006á+ÂOêÃÿ\x0012|<´ÙÅ£%\x0011\x0011ßùõäÑ<y\x0014fï\x0011?þ~«ÿüFwCéFè1ü:xtY"-\l°®Ég\x0019Ö­s\x0012\x001fc'ÇÔ\x0014»<PäEÃ¬G[ÈQ»=£Yÿ¶\x0013\x001d,ÕÐ&õ\x000e
3­%\x0018z\x001eõ\x0014ÝúW ãlã²Q\x0017)8F]£\x001c`/9I\x0011Ñ1Ìð/@GÏ\x0008¿úÑ1C1W$jªÜ1xê_\x0002\x0017\x000cQ,\x0002Çv;´F±ù\x0001yàÉó{Dÿ>&Ç\x0000Æ{cÈ_\þùíòæ·:o&jv\x001cQ`Gåi®£\x001dÜ\x0019Õ²-½8ùñ\x001f'/ÿ>K	\x0002j	¶çë=À\x0016ØO=a{\x001dy¸}a©ÅÆ8±ö\x000b°ÑËe{(Ñö·¡¹Cs\x00174³^4Ö"¥-¦5©ñD µÃÔn1'µØ¸©\x0019·\x0000Û
~º6¼õh7Øï¨[ìw-õcÖ»Z¤\x0018\ÚvÒÒLØ6«c£íÖ-v¤\x0016\x001bµ¡ÝÁF«8ì<Ú:\x000e»elq\x000f§±o¢úð5E>1æá6¦öËÛ?/ïêÎ\x0011»\x000c&è$Vc&wÔ°Òc.ôdLeÌüòÕ'g»ìõ\x001a\x0019e\x0015íG¶&Ýa#3çLÌÌÚÒüð©fßÌ°R_À¬ùà\x0019Qà1\x00103;°ÞìXb4\x0019y0\x001eËh3/ÇÚ|ÿ\x0002b<cnÚ»Æ¹ì}FágCÙöQÅ=AÿòûÃ·ä7a"s(¬ÝÁkôÞ}¬¥DÌ¦âB\x000f\x000eJÇ²\x001e9 \x001fÈij	è¢+¯Ñzú·]Ñ/¿\]}ý(x¦\x001cú7xãøp]9ø°ç\x0019£#&Òª\x0014\x001cêt¾e¿Á»ÈÓ¾ßoTÅEÜ¹î\x000fÊpTÓd\x0001\x0005û#°ÇÏD\x001b¸ýòéÖ¦i-øù¦ý3_cO\x000f×W÷uA8\x0007ç`É>IÄÎóÒ)öIìÜîI¨'ùÞüàäÙéó\x001dÉ¾cî\x0008Ë\x0013¿\x0016pëÁ|cÏÛ»1<àY¹wnéÑ\x000fnq³aðG|NP´W*7\x001bö¬\x0006W?Åð5eSÂ$I\x000f*Liu¹Óýç;º\x0013æ¨\x001ee5*"çè¸^Ð¦ôZí\x000cUL¦,<ìòtþúlçõñègÂî1GqTúß÷3Et³r.\x0003\x0004E´à`oÙv¦]ûÓÏ÷-q$ïÔû3IÃõÒNy¼ÀO?\x0013õ/ÅIüï{OX\x0012G2\x0008½?õÔëDaU>=\x0005\x001br®´Å<¹ñôçûßÕå¯?	p¾à
ågþþíöîòþËÕ_ÿãÝÞ½«1\x0008Z\x0004 ÏÉ \x001a\x001b:)t"ü+d\x000fÅûåáoÜõ3üÛ«³ó7ÏOÎ8éÙ«³\x001d)ö'qõNÿ\x0001±\x001c5LMi\x0004éÝ _UÌsQVÎ\x001fí\x001cTfî5¼\x001fñ-à·æ¸%Ú3)p;M\x001aXZÙáâ$9-&kü+°=bûEØ\x001d
å\x0005y§0Ü£øûÜÝS\x00077\x001eÄÓ£[[º¡Ô¨M/ò~m½ä¤½7èàF«#Ý¢ñÖÜ\x000f,]×\x0004â^ß\x0019`@aßÜ
céÑÍíB$}G­Á¦X\x0003·\x000fsq½\x000en¼P£Û\x001dÜØrC\x000f\x0017\x001d&ß¿[!ø\x000b£vpcT/=ú¹\x001d§ôc\x00036ìÄüÑ\x0010ùV2=·úé·ëK\x001bÓ¹\x0005·<¹qÞzz½ú|\x000f»\×ªRnÏíõ_ÿ¼½A^\x001bM1\x000fg\x0013*\x000bÕ\x001ebúy3ùÔò.g«½xýêôäÕËâòôô\x0018«ûÎ×m[ù\x0017[\x001d­*\x0011uî\x0012èÏ¨\x0008G*E\x000bd\x0016"jøIµëCÌ]¹\x0011\x0011f«"DÒõöIÞg/Åç*\x0011UH÷)hsK«¨\x0019Ñ±ÖãBDLºÙL¼©E\x0014)\x0010MªÝ?í÷ìä~¦âcSuÍU\x0010\x0003Y4&çª\x0000¢uK\x0006ñÃ·« Çê'.z,\x0003wð\x0004|Ëë\x0019>[SZ*ÆQVù!6±Si\x0008\x001dÜ6_2ËÔ\x001f<\x0001Ïñ´-]Ó\x0006ÙÌ
\x0005B\x001a;L,=ÌC\x0002R	Í\x0019·\x000cÓÃXk¶,ºL\x0016tRùKhFÍyµ\x0018
£\x0010éÑ\x0016ÈöY©].`\x0000´(3Ü\x0010¼\x001bMiÜHó³Mf¹+X\x000c°¯åB0d´\x0018¢]ÌfRgz¶²YÞÖðÐKfKhR(¹t\x001d(\x001by~6²	¢÷ÀåS§[\x000e,\x0003\pKç²¸
ò³ÕØtºF80&©\x0004'\x0015kôÃ¹\x0004ç:àp5Ø\x0004ç\x0003
Í5ò^ª¡¿Î\x00122Èl3\x0019Øc\x001e6LÑÑ\x0004§òé\x001dà8ç\x0001Ãµ­l.]%\x0002\x001b*#zCl´¯J¥67­\x000e¸\x0006.¶\x000f\x001cua8Ú±ØHl³¶\x0014Î£ßp^'õHs"\x000bú¡Ò«`8ÏJéKàBkÞ\x001aLÈjS	Îó®eç×\x001aôÒ×ª=öhÈÏ68)|ª\x0018á1ð·\x0006A±¸kÉ¥\x0003\x0007T*±©V6ð`Òh!6¹ê\x001a¯	ø­Æ\x0010üb8\x0006N7\x000f@U\x0005\x001a8ø%îa\x0008'½e8¿ü­b$.?\x001báTÊVÉp*+4\x0003\x001c[à8ôDïg\x000bØÃ"?\x001bÙL ×Ü{Ìé\x000cÍ¨<pJ ¬ïb8àÚ§ÉjP	N\x000fS.'W\x0001[¾\x001cMl¶Mkò~½\x0007\x001735b\x00056«\x0001.,5À\x001a\x001b\x0010\x001fåg#)Ý\x0015Ù¢ÈJ¾8á"±I-ú:¦\x0019\x0017;fLêÑÀ\x0016]/\x0006(iÌò³iàlÇÀùä»!\x001cÏ4ÃisKMA£ülbó1÷ô\x0000´¨mîâ§`q\x001aBS®{ßº}÷»óÿ?so\Çäûn\x0005\x001bx°øþ0 
Rá\x001aH°ARvëNd 	Q( 
$XÅ\x001aõô.¡§oÔ=z¨ôJ»{ÄÉs2"O[É¬MP%ê§øðððpÿ»¥@^ ;Í\x0011¼wô0³gä\x0012+FÃ\x0015\x001aPØ\x0000Ã
f5¤gnÐGWÏðÙe\x0001C!\x000b7ê2³.+]\x001eNÇÒþ\x0018\x0005Þ\x0003<7ã4àáíò>Íx\x001a&´\	\x001dª¯\x0004òIÐ\x0015Ñ3iû~mÂÃTôl{ð¼\x0011NÃ\x0006¡~çyðbrÛwE\x0003\x001döR8	£
tpqeðTì§ý-\x001b\x0003ð|Ø~¼¶àáù\x0010FD\x0003\x001e\x0016IzÆÓ\x0018Ù¦ÁK%\x0012ñV¯¼9Æ!vl[0ßêQ\x000enå\x001e'kd:°ð«ñÐ½¡O;\x000eå¬p\x0018|
©Ð\x0019/SkòöèW\x0003]Äy´]t¾("\x001eØ<Í+/N»p½Èiûõµ\x0005\x000f\x001aôiÇãåxÊ\x0014\x000c\x0003¾uÑ\x0002ÆÛÏô¢\x0007Ï"^UÁFà^F/S^\x000c^\x001eöí ³\x0006\x000f'7tMnpô á0_!±\x0017±]m#F\x0010èÓ\x0005X%àäðza\x000bu:ÊÚsÛýö&¼x]v\x0005®Ö)Ñ¾¼IÀàyYz~&èÔB/°ôéØ\x0019ôÇin=Eyhgd\x0019¼0\x0013\x001fnÀÃ{ñIR=;\x0003\x001bx{¦3\x001cXÎ#taµYy\x0012óo Ã\x0012o]ðBÑA<¯ØY	6®>oñn|Bv<°zå-\x0007ð¸=·Î$YzvÆoÁÃÕKf<pßIæð\x001cµG@<NA¼{c\x000b\x001e¦<Ñ§\x001d\x000fü;Þ\x0018°yc¸èdé=yí CW>ítÖsx\x000c8\x0014_2¢ËA3«)ìÑ|c×àyM\x001d7	Ï\x001bOu\x0005·Þ&gcåØµôá#Ãf0Ô\x001a[\x0005\?ó²\x001fï/ê½ýÛ¸Hzs·}v÷éË«­v\x0003d\x0019£îÅÇî\x0012ÂÄ¾Ù@Ï³Ë×\x000bÀ4J8Ð§,Rü\x001aÉøÐ ²âC\x0001\x0019\x001d@+É0\x000b¥\x000eò,"ó$Îê0ëÕ°!\x0001²" \x0013±o6Æ³¬\x0008\x0019o\x0013\x001a,¤²Ð4¶9.!Å K5\x0005lW7\x001b¨X
)1­~è_\x0002\x0006ç\x0015y%XY \x000b\x0016«r¡\x0015É³Î\\x0011ÓË·qÀ¦\x0019r¡ò^ä\x0011+e\x001b\x0011µ%fßÁ¢¡e,ß64äq\x0005
eFx2QËóõÅh4j¦yÔ\	m"\x001a[jpl¼ÏÅÜF_êÅÖ¡QýÖ$ä¿\x0004ÍFêóhàÂÈh\x001c¬ó
¯°}hßò//¥\x0011/ý£ZGÎÝÞ¦¼%Å,´hø\x0018Aþ\x0011*æf¶\x001bv\x001aGz7GÏ/ß\¿XÂÑÜÎ\x0016\x0002g2açªãòVí"÷)C¶é«f\x0007\x001bê\x0004EÝÎ\x00163?\x0007gHN?p£`@æCZÍo-øW3¤à\x000fÇOÐÂÔåí@ÃRCü«\x0019-»\x000c&ª\x0015¡AD+Rx~ÆÕ£¦)Sw°L©AtZÎ>pIqú!\x001c¡ÓV\x0007\x001cFèÓ
\x00077h\x001c\ÂfÂ-)½z+h| ¡O+\x001b¶i\x0012¶D\x0015ÈÆ\x0002\x0008gW³¡/JV6cÅà¤f1°¹(\x001e[ÆÒ;àð OóÀ)~ÀCôÝhà6ÛÁ¹N¸ßÿjþúÛ±JÔÕ#qé|ôüúá3üÿ`ö¼~añ<¿ðµËVÞå½ÕªéÍþ
¡á¿âôêUùWì\x0007\x0014\x000bÜ\x000e\x0003ú#¦eÎPJ\x001e«Õcµ\x000bPÌp3 ¶W/\x0016\x0005\x0000\x0010\x000b%p\x000cÂÊ\x001c\x0002pSHÙNè,çbKVòÙ\x000cÉ\x0008Ó\x000bM\x0017!ùtäÒ5\x0013¢²\x0000¯BWªG(ÙH	J\x001d\x0010LèÓA\x0018¨ÄÆÐ\x0017}_$ôC&Ì\x0000]\x0017¡£ò\x0004×C\x0018$\x0000\x0004Ë»$å!\x0017Æ¯âð·»/\x001fèá\x0004UlõÃÍÃÇO÷ï÷]]±N¶1/7ZüâæA´³)\x0000?]Iü~ÞAÞðº¯\x0004¯QN¾è´#_Ñ­\x0002¾(S#\x001e¾» /Æ3òðÍNgöù"kO¯káÃ·è;øã7ETë¦{\x0010y.Bggoe-t\x0011ébÏä\x001a>ä(Û.xqúøsnæÅ³/á¾H=CÁ}Qö)JçäZÉäF3\x001b
hÀÃö4zno\KC\x001a>ÇÑ\%Óëf¢ÿm|x¢Oóð¥¢g\x000f\x0013\x0003ø
é¬\x0017¾Ùw\x0003\x001e\x0016êÐ§\x0019/:j\x0004E¦%\x001dóåÛJ¶\x001d¶_êÆû¦þñù\x000b¹§¥ëÌ¬\x001fíÓãíý\x001e>£
y¥À\x0017¬¥<*r¸Ódgg÷G»|sþb\x0011 \x0006£êXÔR@ùý\x0004\x001f¸\x001e\x000b\x0000µ\x0010ù³£p\x0010îé\x0018ÂÌ©¨(DÎ> Ë`l²/&j"Ä\x0018¨=FQ\x0008\x0013¿S`ú$ù0Xö\\x001bÅz Ls\x0003\öklr/§h!ÄÜ\x001búta9EBöÇIFPVá|P´	\x000fUæ½íÜÇ|\x0006\x0007l¬ày
(\x0004OOm!D\x00051ú´\x0013:Rï%Âø5Êe	p`C¡$ØµM\¤¦\x0008H¨SéHEÕüYÒBÏ\x000e6wÍ²µÇliÌ\x0010MÈÁÈ.ÑOn}þ¤tËî\x0002ô<É&sv9\x0012-Ôóç]\x0003¡Ãtf§R\x0017¡çB\x001a|=¦>¾DèÄ\x0016ùª²6Â¯\x000bãu\x0007dð\x001c÷\x0000H©6÷$\x0003Z ­:\x0014äÛ\x0002ù¶\x00032zêÀ^ñHz¥\x001c;_Ìµ\x001fòþ/o\x000f÷Çí'é3J¾»¾·¯´\x0006¶0=Éàß/\x0003²æÐ@ê73ÉÓ\x0017§/-\x0000ÃE}\x0012&E\x000e\x000bÀ\x00146f/µª\x0018,Ï%Y\x001f.$ÙP\x0004a-\x001b\x001eaR\x000fº
&²äèa+cÎ9WÙK\x001díTB`1ÚÇ\x001fâ[zþ6èÇà£\x001cE"â®tÑÛyóåe!E¬øá{ã=aËÿ(\x0007)G\`\x0003½\x0005lèÁà§-sý1Ü\x0012Â±c6±)OÑ°'ó	}\x001aÑ`wr
x\x0006\x0012^s1)=çº´³aâ&}ÙÀk1\x001b·/o~n_Z\x000fGÅH´M\x001báb ¯9\x000f\x001e!;	«µÀa&-}Zá²\x001d\x001cf¿¹ÃÖ\x0010oêIÂe\x0007\x001cVÕ\x0004×1­SàéÎæ9`\x0015³\x001c_æ\x0000k\x000e³TèÓ<rËÊQU_.Cq³YýZ©\x000e8Ü\x0010¡cCï^UQìéXs(-\x000f\x001bÂ=)½èC]î:à°XU\x0012	¸\x001e\x001f|»'\x001dl\x0019Ù:\x000c°V\x0012b¦Y5\x001cåÛ\qÕ4FÚ\x000e±e\x001bÛM°ÖòÉùê#ñe£Äø'%p\x001dp*i;à<Ç\x001fñ\x0005+I.Á°âì,©f6
ôi>VÝ`H|à^âFM¸\x001dø#Íp\x001e{ßsæ\x0007Ç¾R:JB^Ú\\x0017¤Î¶³a\x001a$}Ù,	°³¤Ø!ó%õ¤À¬\x0003zt¬¸ Ùø\x0000çÈoB8lÉÂéÝ\x000eïßßÚw^L1P¡«;ìÕ'ð÷\x0004lÁÔT:X\x001dö\x001a/³\x001a¨å\x0018¹À.§ÙÇ«Kðw\x0004l7t[âPètÊ\ í¤4r5>cÍ\x0006Ñù0S8ØBg°VÕÔ\x0005«Ëèr)\x000fÀ±Ã¬|ã\x0002\x001f<Xgo­
pØT*\x000e8)-\x0003[2ä:$md^ç©öÁ©_ý×øq,²ÿÓ§ÛöüúáË¾4ég°ÒÇÖ¬<âxC`"ædà~º</hÏO¯^ïºFÐð%µ£%¾= JË sãøm\x0019ÕjýZ4G3}ZÙ\x0002ßðÇÅd\`M¾L\x001a+ÙÆíãbaZª·÷eärf]v°
\x0019
l)v\x000f\x0006Ûz\x0015¹\x0016Î$×%©%[¦\x0016µ¹Ís"C@\x001fÓò¸\x0005A\x000bÓ]º\x0018Í|ûõoÿ¸Ås\x000bÝTúS|ÈÚGOÃÁ\x0000qQ3CØ%:>ä»GÓnÀ£÷^ú´ãY®`Õåè2VöªÕ»ò£ò¡ôI¦¼/ãÓ|ÛGÁ6±%Æq\x001e²x{]Í1\x0006Nf>k94ì3\x000c%K\x001a\x0018XtÏE¿#+!Vø6Q¾­(¼XRyÙ\x001cÚ(UÔaý\x0000êRò¤@e\x0011 7BÇ\x0011Ä+ì<eNLjþ)´\x0001"%Ø
Ç§8
ùz³\x0019À7ØUx±\x00180ÜvÐí\x001a»D\x0017\x0013\x0003Ç\x0017\x0007\x0000\x0002Üî2\x0003Î\x0014À·ñE:ÔbÇ\x001e!>Í3<âã}án¾¿¦ðÕÿBmQ`\x0012äB\x000f\x0012p¥Ø§G¢¼ÂÇ
¸<Ëó\x0018\x000esj=u\x0006èRo\x0011p¡ØQê¶¡Â\x0013ÛúF,\x001fD
*zslØí\x0004\x0013Dó\x0007±V,ijÒÅ¥=åØOó\x001f¦îf3\x0013mDÓÊ\x0014H´Ä4vH/X^Ê?ÍjÆBu\x0000×\x0015õqÉý\x0015ÚàN££@M\x0013¸[¡4êÓ§Jn?¢5ìC?pÅËzèÓÄ\x0005\x000b+ðzWID;Uâò1gÔJ.TÜ¡O\x0013W\Í\x00131?"°~·ÉIMJ{¸Â¯¿¸÷x1Mx'MõÅô»ëÇ{ÐP\x001a|p~ 	u]§¡µ6÷ævvúæù"¸mººËà¢äEeXÍ\x0006è-=/,¶\x0007ÎüþõëC¦û\x001fÆjðszÿîöæþþæ¨¹Ö9éÄWhUàÀHÌ\x001fU\x000fÓGÕÓ\x0017ÏÎÏ^¼8;Z\ô¼\x0001\x001eÂ7+mæ\x0008\x001d¸½Ô6
\x0013Ò1°ÆÖ\x0000Sý,~V\x0000£öC,ÀÞ\x001f3¯	¬càÍt\x0003­à%Ùaú¬àE¡RýläLLûåêwìs8`|\x0015 O?p6M\x0014L}f¡Ò¤¹:-$7
íµó>üß¿ÿB5C¸åØy	nßÃÍÑó»/{¬¨7üÌ\x001dñÅH!#Zo³îèõ]\x001d=?»8{½\x0000
ßôB;Z\x000e\x0007L=×KVE\x0018Røyâ.%ûúMÿýëûGýì/no\x001e¾¿ýrt·8¬5Ûø\x0010À¢¥\\x0006¦Á\x0017X§ó³7Gß¿>º\x00186®\x001fÞÝü^¾ÈfòÏ7û5¾¥V¨\x0002ÿ÷ì×ØÍ	À.ïn¿Ö\x000e½ÉHööÓ/°\x0016K§ä\x000bgL,â):Fî\x0019\ð"ÄðÝåë×°²ýéìùù\x000b²ï\x0017ç?Õþü¨íFÅiµøW#È\x001e\x0002\x001cªäQv,±\x001d\x001cz¬{Ù¶t\x0004©Ñ¸Ùo+Z(\x0002V\x00163¶F4lçÊã¦¤py\x0005\x0004[ÙP\x000cç\x0014\C\x0012²a%\x001f\x0019Ø¬Ü!W°aÍ\x0004þÕ<¥%[Ö-F\x0019§Ô	òà~62Ìôi+ª$\x0008\x001aVe½a¾\x0016Ãe·zR
r\x000e8Ô®FMFãÞ98rÜ\x0016\x0002Ø$Ùn\x0005[\x0011Ãï`sù¸32t\x000c²O#¾cô¡=Þ}ü«º'Óh£\x0017©£W×·÷_þïÀðO§l\x001ec<@ÀRYn&³\x000c(ü]I§`4ñ^^¿x}ôÝ%\x001c¯¯÷Â
V8\x0007·\&5ª\"ñ\x001a\x0005\x0005#ó
Eß«øHGµgð\ò¥KSÆW<rÿÏ'Æ³E×÷á¯·\x001fþéèBoúääåÝõ»\x001bé\x0010úÏÿ+-BçW\x001dªlS,Oaö{æ³KÂïàýd·¾¼8}v¶¯\x000bh
)\x0015}`%\x0017\x001f\x000bÇ\x0006\x0002±î÷:çµd°Ú|\x0007\x0019¶~Í,Ú"w¬±÷\x0019ï\x0007¯Âj²â´Á©ÎUü@æK\x001a
Å\x0012ÚF²É¡µ,~ùÇO7$~e¤.ødüöæáË.«\x0006»ZÑúÅ±G4:»\x001a_1x°¬5õYuAOÅß]ÍÉ¹\x0000N~ÿ·\x0014¾=p¢¹};½!<\x001d"L¨§\x000eÀ£\x000b\x001a\x000csw£ñ)Îùw;n\x0004c\x001e\x0006>\x0014 "Fõ\x0007\x0002¤
ô/\x0007zÿñþ\x001f7_GsÔ%o×\x000eSÂÏ¸Ãàþ^6÷,¥çÝÔ¹¹8;úéüââôÇ³%$ÅRþ\x0011Heü#\x0014Kø¯'qx Ï¿EêîÃxÍ~úrûùóÍÇû/Gzüð¸{\x001fazG$?\x0004*%×T\x0013åºåt¨OË×ç¯^=?\x0003/äOo~|s6çaÀðrß\x000c\x0006ÿzW¸L¹<©Ëæ\x0010WsñÖjãò\x001d·L¡åÃÔ9#9+°\x001c¬©öá²T'XGq¸RÒ<\1éÕ\¼ÿÛ¸àr\x00154¯/}lËú²Ëp}¹Õ`¨ÙÞ\x000e\x0016(\x001f\x0016\x0015\x001f×êaÄ²N}`\x001f¾}3·¿Õyª¨ÖÙ·ëÇ÷;ý£\x0000\x001ed"ÿ(\x0001\x0006\x001fnA\x0007·(Z³cZg¾:}3S7æÛ\çÿ¨xc¦Ï\x001f\x0014p\x0013Mÿ\x0002zì@B?* F/éóG\x0005Ä\\x000eúü±\x0000?¿ÿò5¼C\x001f\x0004\x001bÉÒg-\x001dÝ]\x001f=ûôx÷ÏÿÚå \x0004\x0005é{\x000fí8ÁíXg|¼!\x000bÌ\ÄðèâôèÙå³¹«aútýõ\x0013:HÔí>èÙ}þòÏÿüºÓ.c\x001a\x000eå¡°r4%ULûìYùÙá{ò\x0013ÏþìÕë³v8öÖ}ù%S½B\x001fäùáúþÃÍõÎc\x0002uÒ()\x0007»Q\x0016	<\x001d.}³Ï1?ùáôÅg§s§Ã\x0006e\x0016Y\x0012´De°*ôÆtª¹uÝ,\x0018Ã¢ÏR\x0016TôÅ6ÈÂ÷wX[OïïQD.¤aXJn¦
Fs\x0014e±¡°²>Kað=×U\x001cÖ\x000bóX\x0001ÆFß\x001e³¾ûªµÑã9>ºßµrÑÝÂg³³µñ)#³\x0002aW3²@òéám|¤×:j-Xµ¯^\x001cÂ=x\x0001ÊV\x0002xA:\x001es]Ï¦yõ¾hþú[üð{u;\\x0016b§n©Å
¢æ /DÜ~>8¼=²Mpýúýõç/\x000f7Ã/FöÛß1!°(ªâ÷åÍýûÛÝ¡10oTE«Ùl\x001aµ'Z6ù4Âyöâû³«ó×ÛÞ0ñ1\x0003bß ÐØè\x0019âêúãî5Çá«ETC48p\x0013
¸óh»ýxutuú|ve\x000b«è\#]£5§á¡øÝËÈü9åÜ\x001a:ù÷\x0016º \x001aé|Ù|4vF^\x000cC2rý\x0019Tªºèôdf§Vùc¾ËÚRrcç8\x000eël}ùZ\x0002WO¬nY¸¡yYkK!6>~<Ðù5xõÌêæ©Å·\x0008¾Ù\x0006S¤+\x0001Ï9¹ØÆÙ·¹EtõàÖÁ³­\x001a\o\x001di0¡r½MfÍÜbÎÇ\x0008R@ðT¦X\x0013âiGu)g¬w¾Æ}x:Tx:´áÅä
¯<ÍGÏV"\x0003*®a3õÐÆ¡Ã\x0002Ä3\x000bG{ä bN2tÁ¯Ù\x0016ÆUÛ\x0002lÃóó^\x0012¦]Q\x0003\x0012øM~¡u\x0017ÖcSo\x000bÓº-¢Ã>¥Äú	@ç¸³C7­>¼X\x000f^l\x001d<ð¥yÝé ê\x001bâ®ÈkN\x000bLÉ\x001dÓåÖÁ3ù¸¼ùÃØ¥\x0019
xFAvnÍÆ°ª\x001a<ü±
\x000fü\x00141yZñu6z\x0014¯áÑ³kL­ÏZÛzÖFÔøÌ<zªðÅ*eYzNÍ&èìÆò8ôÉæ7NP\x0011rD÷¿®ÁßZlEÁ\x0015ð°{u&<¯"7Nu&ÌÞÿ:}vùb\x001fwc>Êoã\x0003×íJäÊ\x000fäsQöòëøà\x000f\x001añaÀ§Ïiq\x0007ð%¥Î+\x0011xÂÙé]Ä+¾ÜÌg\x0002\x001d³4~¥ÇÅ±v9? ò¬]^gF\x0017ßdóîçC! ÄÆÅE¾\x0019bé¸\x0019NÝUó]ëÆ)´\x0002jÇ\x0019Ep°Òß\x0015Óx²8|ÁÍ:|K\x0000-Ü±Føc\x001b ç\x0014bòZJKK\x0000I\x0012Ù\T³>Õ\x001e@W,ÌÆ\x0000/?n2tÄ(îw?º`{÷¢\x0018­´å\x001e¹äYqX\x0002Å¶§=ño]¾\x0018=»ÔxºÆÓ=|	\x001c*Å¹2p\x0000O\x001fùÊ~B?­ùlÏøqé'-5oÀ\x0017Ü0~ºÏ×|¾gü`Ý\x0019ÎÏBIaÏ©Üé\x0015ø&n}\x000b_¬ùb\x000f\x001f¸\x001c\x0016Ã÷wÉ\x001f³,òáá4¶½|z:Þ\x001eZuðÁü*æRKIÖ"Øë~>Wo_×3~QSq9%\x0006ZÉGÅ
"*ôòÝ?`#÷¯\x000fóK\x0019·Bíh¾\x001b%o%?ÐÙ´Ê\x0005|õþµ=û7\x001bÃ\x0014¥\x001a;Nn÷r÷þµ®\x001e?×3~1rk¸¦\x0006	¹d%ëÏ»Ô?¿¡æ\x000bí|\x0006<\x001d\x001aÈ\x0007¦Sµ³\x0013ûL* |à\x0002ùíáÒp\x0005³å\x000b\\x0002ß£·AÏeEïç\x000bõüù5\x0006\x0003\x0006åü8;©XyÎû7¤~¾XïßØ±A\x0001WÂs»éd<×0`±Ô§ª\x0003¹øÐµö÷ò·lQ6 ç0\x00047ÄöÞªmá4òý§É\\x0013ÆX1Æ>FÌ|ç38Ä¢µ>Ìî»µá	âÌ(¦0õ\x0011bî;gÁ\x0015d/!øá\x0014QnÑ(nG\x001cùYH~VÏLè.eûÒÛ\x0004gÚ\x0008£Ù\x001a\x0004\ÊèjF×Çh\x0012í\x0011GñXJãCÆ\x0014å´Ûzc_è«Ö¾oª±·\x001d6\x000c§\x0017\x0006-öÚl
áïEÍüsÉÛüÆI¥ªröîáv×u	÷I Í\x001c3E×\x001fÑ,Çc\\x00027õ×gÏ®*=¤éuéüÎ·Ñ%¥8ÖQó+¦¼\x001bM\x0007[ÙtÅ¦\x001bá2\x000b²$ì¬SbEèf1\9EÒ\x00195¦«»¯üëéRE\x001aélÊqP,5ÐÁ_\x00021.mwñ\x0007¼¹Kz¡ËÕÌæÆµÎ\x000fY·\x000fà¨$Â¡Üvïo\x0019®§U·Î«+C\x0013V \x000b\R\x0012@f»w°\x0014¯Þ\x0013¦uèl©¦÷À(5µàûÉC´Í{ÖÝn<[m\x001d½ä¹\x00043¡\x0003'âª$á+»×ÜíÁ\x000b5^hÃspi~ì5,«ª£ÖR!jó*:?±w­s5\x0005[Îq§g2Ãc¯[ttãà³,¡Il\x0000S,6I²Òm\cSPÞbW7_oÑ@-M3âù '­Ok6®©\x000fZ£\x001a'×qPó[8h@]ÔyôÒÃv7«ñ\+ORé\x0004\x000eO\x0011V\x0003¼\x0014¸s\5z¾>lý\x001fë´\x001d¿¨"^lÄñ\x001b\x001e\x0005£ç¤IÚ!yÉæí\x0011¡£\x0017ëÉëÑÍ³<¹^&×ØáÐ\x0008q{ò2<[o
Ûº5¼q\\x0015\x0017¸RuÐà\x0011ÌÅ\x0017âÕG®m=r=6µõç9;7,p~Í¾\x001dÇÓ\x0010Îµ®¼¨©½\x001eï[õY\x0005á{Ñª©­Ím5+\x001e\x0018\x000f.iÊrý<æ{µÊ\x000fµ¡Æ\x000b­x©GùvËíÌâ½§^Vk¬­÷­mÞ·ÙQ%5â\x0005*TCº UM°.Õt©\x000e*\x0003Ó9-a*Äry\x001fïjOÔµz¢Ô¨!ò®uò\x0005c&çmyäXWûz®Õ×\x000bAIU\x0004JLgÔ\x0007l¸Æ×s¡\x001e½Ð:zàA	Ê\x0012ÞKãÆ¬¬¢«\x0007¯uÛ\x0006p ¬ì\x000b[úqàÜJú§A?^í
¸Vo\x0000\x001bL´ÃLú<vAüä´Æ\x0017ðºóº\x0011.ZEÊ¡\x0004\x0017$ycñRXsôuÈÇ·Æ|0©EóÐa[ù$s²+Ì*:[ÓÙV:p
Û\x0014\x001fI²\x000e¹Ö
ðV.|í\x000bøV_ Òj6m\x0014Q+\x001fçóÓÌ×>¼oõácÜ Ú\x0016SJêaÌrYWOn«Eþ\x001f¾bøÚ¨øV£\x0002+V\x0002É¹ô\x000eÅ@òpLqÕÚ«\x0001ßê\x000c$Uú"\x001e>ß;$KìÂk¿æ<ó¹\x001e½Ü8z	\x001cw¦siÂÛ$±ìÖg¡¶z¡Õê%c¨S\x001dá=ÝÃ)É_¢fÞÄ5;#*ð\x0013Lcà'Ly®'9i4ÀKk¬r¨ïg¡õ~älf£ä3\x0007Óò+Æª;F¨]©ÐêJa\x001a®x\x0003I#m»dôô*¼Ú®V»râÚ!\x0018=%W ðDÑ[\x00017~­\x000fª~­_du\x001c®Þ9sD\x000cR#ám×º»V¶<É¶8ÅZÃ¨	\x0002¾|ÏO·7ß	é\x0012ÃÇ8%	ëÉsøÂÛ<\x0011\x001bk< ìË+øüt~öæï\x00036c`Ó
l¢äW)\x001d¤<!aS¦\x0002\x001cô¼\x001aK\x001b°\x001d\x0003Ûn`ð»,0o®oKA\x0012"ì4¡®\x001fØ]ÿ(½\x001fyãàK¸a\x000fÄëÇ¼¾78îWÒÿ\\x000f\x001aSäÓÛ;­æupÚÃ\x00188ô\x0003ëÍ\x0000J%\x0002ÖÃ\x0012¶Z\x0011q\x000c\x001cû¥×RÉr){Lò¬è\x001d69\x000cp\x001a\x0003§nàäè\x001d\x0014Í\x0010¹ÃX°?\x0014p\x001e\x0003ç~#\x0011¹£.üIÜÍpvòzÖ
<ÜÀË¹¡:
Æâ9ÏP\x0019%\x000fj`!6\x0007:8t}Òõ\x001fup'çÌMmô`×\x0010;ï\x000fE\\x001duº÷¬1\x0016ánÎ!ï»l\x0010ÛCuº:ëtÿa\x001cwÂAHò.\x0019ãÉ[R?quØéÞÓÎ\x0013¡yt*åË:É'7ñP;¯:îtÿyØ
¸@®c6C\x0006¼\x0007: uuÞéÞ\x0003Ï¨¡®Â;\x0018×\x0014ä YxÎ¨CquàéÞ\x0013\x000fVE¢\x0010\x0014Ui\x0018J\x0008¦U!B2.Lå[º«\x0013O÷\x001ey\x0006£RýbT*â1J\x000fe+ª#O÷yFÄ\x001dù°
èOc\x0011Ù¡×±©Î<ÓæÙ=æ¬M"\x001eXÏ\x000bõµ\x0001WGé=ò\x000c^84§èâ\x0017\x001fÒIÙó"®\x000e\x0010Ó{\x0018½\x0016XýF\x0019~\x001dITîÇG=Ð\x0001b*slzÍ±QqsÎ_\x0012ÒÃg\x000eäjÊ¶~Û\x0012×f°\x0014XÇ,Ëx\x0010f\x001bqe)L¿¥àÉtvÄJ
J¹Bë\x0003ÝðlµñlÿÆC!Oöçí @±Ùx6\x0003x¶Rôo<7ÔM*3dÊcÍöpe:Ð\x0018kýóÛÛÏ\x0013\x001e§ÿr\x001aù¨Æ»\NYïWZ\x000cÌg®â\x0015à\k\x001b<¿¾ýüépoïîv¡jUÔC@U\x0018H®_âô¬ÂÆóÓóW/÷üâb[¥Qª­\x001b±\x0015°ª¤òs5«öÛä­_Ït/eµ\x0015«]Áª\x0002Ã3\x000eç:s)Ñ`£gõ\x0005²ºÕ­\x0019WÃù²%tÍã\x001aõ ª6/¡³\x0014Ö×\x000bvÍÀÂ!¡l+o<ÎÎwëWl¨`ÃíU¢U¢VW|w§l/ïWìèÝ"«ÐÚa;fSjpÊ>âG\x0002¿z{å5¯`ME¹`õ0°qx&5óÚ;\x000baumcµZ±\x000cò 
Vß\ôB;«±5U\x0003«SÿÈÆ¡ÆvÖ\x0012´4¦½YÈjêq5±ZuìY\x000c\x0012l\x0001§\x001a\x000f&ÝÇ¦\x000fª\x001d´¦\x001aYü±\x0016¼s¯Vr@)R\x001chç%IÒÖgYq(`\x0006Qi5µò2àýÐ\x0004l\x0010ÛAë'Á
Z3ä;Y0´|÷VÆ6Z3+³Öêj%XÝ¿\x0012Õäað\x0012Á/íaX·Q­X	QW!>\x0012¶¯3)~üôøa'¡òaPü£*j\x0004\x000cð¿\x0017Yç0£\x001cñêèÇË7?Í?g\x00178WÁ¹F8\x0018 é\x0000\x0007?§Þ\x0005í\x0006ñ¦0ç¾.Wt¹.:ÚÛH)\x000b\x0005.IN%¤¹\x0004%pãÚ(×Fº¨½\x0008_aªQñ¡Ì«Õ3%ûËàÀ[\x0018Ãá-p\x001abrÉ·\x000bì$½ÈÏ'Þ-ÂK5^jÅÃ¾ÜìRJg#}HmÍæ]çk¼¶©ÕF)*\x0014D<_úxàè\x0005©N	ÚÏ0,Â«·ElÜ\x0017ÚL7bÂË\£\x001f²ÆzEIªKª\x0015Î\x0007Vÿ'·Ç3SÃÙìçRd\x0016á\x001aÏ´â%ÇeÈW^B>Í¸\x000exÖTxÖ´á¡z
×Ea¤Ô\x0016³Ô¬ ×ìÛ\Onn\\x000b+/»aôø~«¬\x0019FÏ®Ù·¹ÜÜ:¹ÖãrGD9qV1\x0003çÓy_Ggk:ÛJÊoÜDwÄVxeaºÙ:éEt~rÖ¶Ò\x0005EOÿ7<K«h\x0007/Õ®±yyâ
´Ú<¬L­¶tUÁbP%Çmð³%\x000c\x000bèôÔÇS^¶Ø.cãã³¢¸Ö/\x001bâ\x0003M+3ákÝ\x0019\x000e«\x0018\x0003ó%	øÁ¨2^RsIðì\x0004¯uk8¸~jqã-Å#\x0010/\x000c\x0017º4£_¶ÏMø\x001aýdíÀOæÙK=§\x0013èäÄ°¤u«Ï\x001aÏ7\x001a\x000eË·\x000bQK\x000eF&ÈÖ]ã\x0011P\x00131\x001e5uhÁó6Hq[ÛD3\x0008Ú8[(°o²útëêóvèIlÀÌ°DÉQ®¼°\x0010×ðªT¯.SY¶y¹Ð\x0002_Í+\x0017!0~sUÌ7[\x0008Â\x0001l=;¼WÃ-<\x000fõÈVm4aÕ\x0004	_håCÝÄ1
Ï^U´C\x0011W´³Å\x0016Kø\x0015\x001fIdµð\x0005¸o°Ïlµ\x0013ûb\x0013'M zè
¯OÉéfZO· zs}yü²t-nÕ\x00066ÓÍ´nADKâT}N\x0003"i\x0015§êö|¶ÞÀÆ6nà`Ji\x001e\x0019\x0018'«NKÅ~$ÕÅgé­m$ñlOl­ð|þq__jíµÞD\x000b¾çfSNãül¬úüyiO½0¤1!FÚ\x0008](Yë¡ÎÑHbªC\x0005ÇUÕ!bÇêy\x0011áòáø
×Ë)<\x0008ùi\x0005p3á¨ê\x0007	j&´F\|\x000cs6ÆÄôhã¬Pö\x001eD­¨Ly\x0013wÁ^sÔ ¸ÒÎ»YÔ&Ýié±Î¢Üã<ø6Ë\x0012Ü¶ÆKÇi>
è\x0016Jo*Joú(m\x001c|ÖJ:4ß>\x0005QJ´>ì!ÜOkÊÜIu\x001fåÆ\x000eæm±
\x001aCºI\x000cµ
2¨
2¨^HÅ/e(Ñ¥ÑpTÁ[½K-q?äæá ÍTÑq!¤\x000etòQ¾+\x0007ò}\x001a$]ÚÚ¹g1d¬G2ö$ª+9,JéÃçÁ¿¡ô;ÇMzmhWzmð1È¢\x000fïçá\N!³HBò1r'\x0010¿£»Õ`=Ì«ïç°\å±,·#×¬ED\x001dÂ\x0019Ko\x0017Ú\x0005nÉ\x0018\x000blãJRä\x001c8Ø©l\x000bDl\x0005&{kÀh\x001f\x0019YiÅQt|\x0011\x0017I­)6;éøa"WÍÛ\x001c·{3û¸ìÆÑ$4\x001eZ¸<úA´à\x000b®IEJÏ\x000f­mÊÛE¼÷r¥Xq¥ØÈ¥E|#\x0001\x0003
"
Ç+l*ÚÇåôÜ²ì1%µ\x000b\x001bAYGÅR«X\x001aËmjìçò5WÓú*\ªpIà4}àJ¹Òv¡½\ÖU\Öµra}'ex¼4¿©Ù¼½jz/¯±|#\x0016¦C\x0015I¦\x0011fn\x001cyq\x0015»Ì\x001bK^\x0003×Hðu\x0019+\x0015ÈåD½Â»\x001ce¸ÚzéÞÇåmµìñÇ6.kEÑÆÈÒÞ
«kû¸\x0014ËUÃ5JYó1\x001b	o8Á{©¦Ñê[ôÞ×X¾\x0011\x000b\x0003%ö\x0004\¡\x0008~ù¡q
`mGÞ\x0015*\x001báC£ÐY\x001a'
-ÒX	SØ.«¹)ÖL±Éhf^\x0008Äº>\x001bïëMè[7¡±ÂIt&zz\x0002À¶ºßá<Ú._´+×\¹yY\x0019~/I\x00181d\x001b\x000fw<>\x0013SÜþÂ¾+¨+¨V.oDÌØ\x0006Ï)þ>X/Æt»¾Ã~,]c5¹8\Q:\x0010:\x00158U×\x0007\x0014wbk»\x0014Ð~.[s5ÚR\x0003\x0017_¶ñ\x000eo-4Vz³\x000fû|ÍÔº
½;Nì=hzL'ª\x001ce¨ú¼yÔ\x001acF/\x0010\x0003ÙóPYr +r
\x0018­>K\x001ab½´bãÒÂxQ%\x0004®Ìù~>Jì\x0014V\x001fWªVj\ZV\x0005Vdw&p\x000b`ùÁ	Ü®_»\x001f«^]m\x001f\x001a®\x0002e½\`£rrH5ëºº\x0015ÊqÞCÂÐ\x0019Sy5\x000cêr\x001d¢©li4¶Ôú,âá¨rÎ+cÔÃï¢²5m¥ré\x000c·1Çt>:.¿\x0007ÿOõq¹j½ã£\x0015¥Mª³[ Áh
³··ÈÚËU{Z±ÕÓÂ~IJ¸\x0014W\x001f\x0012d\x001aóö\x0004Ö½\µ·\x0015[½-\x000b·±Ro\x001bNê¤äÑ\x001bï{]\µ­\x0006Â©¡]¦\x000bò\x0018ï1"Á\z{&È>®T¯ûÔºî1d\x0006¬\\x001c®¤ÌCiß5)ÔX¡\x0011\x000bÊÓ'p\x0015\x000b<l«<Ë=PZÕk~n£B¥Ïb$À'"Õ\x0019ÌÚ6RÌm\x001bºÀ²­Ár£ÀÂ½ò\x000e\x000f
\T\x0012TâJjÏ$=`ºÙhÝ\x001a´	¦t^E0Ô9\x000e%Y[ËÛÎÛs(æÁöÄquO£
ÂÎê\x000b5hB'+\x00021ô¢¹½¾iÚ[mÇë«V:ºRéØH*éR4\x0006Y%BÞÍh\x0007/&tÕ\x0018nk ·¯&$\x000cjýÞZ¿\x0017S÷}³\x0019(Ü^-	Sh&ÔÞ3©.Ì
=Ð\x000caIðX:ã\x001c\x001eé
ÖF\x0018rQrêÐüÍeél-\x0019V!«ÁÜ¤\x001dÈBDp#\x0019²ðø\x001dNýM\x0012ãî.{\x0011]¸­\x0015ë¾L\x0019-UÖ\x0016ã3e$Qf»O¹\x0018Ð¦jmjfÌ-[Å\x0019=¨¨+É%K6v¯Ä@55c\x0015z}bë,³o\x000f×ïw¿cæL±~r\x0015×^ø$W©xÈ(\x0007àìÏW§o¾ßËg*>ÓÊÙx=,"þ>g9â`bfËå\x0011F=&Ä\x000bs\x001b!\x0019ÇNâaxSOòã·¾©7\x0000¦
05\x0003z;=¾Tdö«67Â8[Í¹pÜ\x0019IäØL\x0008G±æë½µGAeqn Ï8ZD¨uµM´nÞ'.i\x000e@Ø9ðÍ\x0010\x0016qz6Wf\x0019`½OtûF	\x0018Þ\x001bP`Y¶ ²l\x000eëÖáøÐCDß<\x001e¼B~Â¶øªWn\x001dYZÕ`X|6)j\x0019b\x000c\x0015b\x000cÍå%è\x0011\x001d}-A¹igV¾qê%ðQæeë,«!. 
Ë£Ç?¼ÒÎ×¼/C¬\x000f\x0014Ó~¢`Û\x0015®´!skG\\x0012r5qÝf\x001e7#¢o\x001fEX>"aO»\x0012å\x000cÒô\x0007æy=¬ºuéÒ­«\x0011\x0010Å8d\x000c\x0013wM
ÚªáýÏ¯ÛÌã6óä7´#¢AEÌ\,\x001c½Ló4z\x000bâõÃ»ßç\x0000}
Ø>É¨\x0005\x001a7[Es5³\x0019\x0012-¶æ
6a½mÇn\x0006kãÄf+Î\x0001Äa!fµ\x0012ÑÔÓl:¦9ñU*QìOÊ®·&÷Úì]Ólê14íc\x0018ä\x001faä/ñ24²\x000c³]gm¬­	m;!ì$Ïb¢\x0005\x0015P'^<Ä¼\x0012ÑÕ³ìg9OfË%\x001bÁ\x00187læ°ÎË®ú´éÒ§­\x0011\x0011N¾0¼j\x0012q§\x001d\x0002\x0001kmÛm6Jed6AS	\x0011¡\x0017{£W:`®¶Ù®Ýf#"_¦¬NÉAVrââÊ»¯­¶o·ÚÑà\x0008Ì³gÍé`\x001aÞÜJD[ùÞ6û\x0011[za¢KVm\x0000¯F\x000egíÖíg_o\x0016ß±Y¢\x001a\x001c\x001cØÏ%\x001b=\x0018	\x000cãá¼ÎÅñ±FíØÚPLã\x0002è`µ1\x0007BÃn$B8ø[ö;K77 ÕéÊ#rJ[¿×öì:\x0002­Â	L;gLEé³Ü
¬22éÓ}m°§¸¿;8áo\x001dymºáÄ&.ÆLi\x0012\x0011Ki\x0014\x0011ãÌùÇ£×\x000f}¼ù²+ngÕÐ©Lãé]\x0002ÈJò
\°vGzÿ£§WÿöæìõÓWÃ\x00181>Ä,\x001d\x0010Q\x0001¤\x0014áaqóLt¶p\x001c/\x0001ÂQ¼¤	Ñ)Ñ?4Þ\x001es»p¥\x0006j{Db)b®\x0011sçDg©öB#\x0016\x0011\x000bâÖ­½\x0017QO\x001aøPßúQàîñèõ¯>^ï\x001dç¡ãµV<Á6l Ìðömòæèõ.Î\x0017gMzõ\x0010icó¬\x0010Iý¤\x001d'sD+ÛÃÙ°ýÞ²ÍÙlã¸ÙA\x000e\x000esíÜ7Í·ÎKÙÜÍµg¥ÕlaÜ¤\x0003¢Jëàü\x0018Î7\x000eñ\x0012Íaè©o\x00002«jûù±\x0010NW#§[\x000eã
ÅëJQ³ï
GÐYg÷ì¹GG=éÝPðZ\x0007Ïv48xÄ¹¨7ðvµ1m\x0010/\x001c¼Qâ6Î¬j¥³D§ÈÁ&:éª
zû-~!]¨Æ.´]vÜâ-e\x0013¸$&º(r)OÚg5ÒÅ.6ÒEí$ç\x001d|RNÅÂ|:\x0019»<£5»ÎèjfnÚè7Âs®ÈÎäFznÍ¦5¶\x001a;c[\x0007/Gñòµ\x000cò²-´]5x¡\x001e¼Ð:x&Ê®MÚ
\x0013Âg¦Ý\x001bñb\x0017[ñ¸°D\x0005ù£<\x0006éNoâtð><¸\x0013ü<n¥Bbâ:Ö\x001eÔw×\x001foîö\x001dg%1*Û\x0010\x0013cPJI[cÅ{úîôÍó³§Î]!\x001bÝñúâÉbÍe¨(±\x00188,Ô ¡±5ä¶ÌWd¾Ì
Ë-xxå¹8\x001f\x0004m«vÁ\x0012´X¡Mk iñ×-÷,%4\x0011~aëCñ\x0012´T¡M\x0000\x0016 éÀ\x001b\x0015Ð¬äË8hÊD=ï¨Ï¡%_;éH¹ÉÿïÿËw·7\x000f»R<\x001c©·´fÌ)[\x0014ÌZÒ°=×èèòêÙùÙÕ8\x0017jÊeÇ\¶Ë7ggUdg<!¥à·fòï\x0005«ô»}ÑïnDÃ:\x0011\x000e aýJ!\x000bC<Eo¯}ØmI­k0Ý\x000e\x00164\x0017XìèQ¸Ò\x0010\x0004w¶ËÔ\¦+)¹na­iI§ÄËÂð0m¶¦bí#\x001b·¿\x0005²qûÛd\x0018\x000b
e*=ï¦äÏÃÁ'©±zk%Ò>°T¥v0p7X¤(yp/¹Ô
;YKjlØ`·ÌW|ód¨Ey'Àg^.\x001c\x00063Âþ¤QÛK\x000eöå,·\x0019C\x0016D&2ÁÞXÉì4ªo6sm1r»ÅÀ CÉ£KøÞW[¼Érh\x001aÓ7¹ÍÜ:\x001e<(Ïà!x~©÷Tý]È´Û
»L«z\x0007ÐÏ­hÑR\x001f>Dãã*ç¥±7Ü»¶¦­ïEÓ\x00134Ý¦QbJÐ¤¤¹ãÖ3z\x001fNh¦\x001d
n \x000e\x0018ÞÁÍÑb×&ÐfrlÖ]à\x0015\x0016ôóC2^JY		nSr\x001dpÛÿö¡ÙÉZ³ík
ë¸þ&\x0004\x0002öò$ætÞ®f»ÌOÈ\x0007Í©ÈêÝ	Së
º8)Þ0ÛÓé÷M6mß\x0004\x000e\x0003¼f]\RÌöRª½d=`Û÷\x0000&\x0010\x000eå\x001bYNõÝpDÙ¾6ñl«+f¤ 
SS¤ÐË\x001bÙ\x0003Ó\x0006P\x000bÝZmódØrû°¡\x0008¶\x000c[à4V\x000f^åf\x0017ì¹\x000bl\x001f67Ù\x0005®c\x0017`\x001c
n
âtd/¯	f°tØÜÄév­^7²âY2kAlGö¢¯o\ß\x0011ê&«Íµ¯6¸xÊ\x0011¯\\x000eYÊæS]svfÛÑl\x0010ë\x0011á>U.Ai-v-ê®=ê|½\x000foÞ\x0007`÷%#\x0004%ÙÊ\x000f§ûLè>4?9§|û9\x0015à4à*d´lE\x0006\x000ePV_\x0002´Øã|ë<\x0019µÜ<j\x001a[ï^\x0004p\x001c(\x0016Á\x0008"ùâèêÒNfTm<èçV2+ª)\x000e
\x0002>AòR6Å]æ&h®\x0019Mo\¢¤,Ô\x0018¹\x0006ÿi|y) 5ß\x000c46ãàüd=¿õ¤¤1\x0007\«zÜoSuÑC´Ð"üæ\x0015_CÂVó\x0005ÍvE`\x0000%OÐr3Z\x001c
ßSô¢\x000c§\x0015;\x001bºB\x001df\x001c\x001c%´Ø1¡k\x0003\x0012Üô83æa©ùíªô{ÉÒ,uìAM$#îy\x0013HÉ¨\x0011dÞK'd­!\x0005 Û¨Ý%¯)§\x001dÑ\\x0018\x001e\x001e·÷Ø¦ë£~nD3`Õ\x0002\x001f >q7Ü²<M\x0019ï»VÖ\x0013´æFÝy\x000e*Äà%}/{QØ63ýö¢	ZóÕ@£"yÉ®HØw¯\x0008f\x0004|fa´i\x000fáhë±i¿\x001eãZnz	Õ­Û\x0001\x001bÏv;Í[69\x000bLûY`±Å\x000b£YË\x001b\x0014\x0006-Ë)»6è¸ÐÈbû|&+=ß\x0012v\x001b*	PI\x000f\x000f ]\x0017wðë1óíF
W>«ÃÄòè£4\x0017r¾Ï¨å\x0008í#¹åëqröZx¶\x0017Fï%ó\x0013²v\x001f2f#\x0007;öÌfñ \x000cé
^4Ù©}wâ\x000367nÍPB
1\x000c-q\Ø.=·ÌªúþiUóýÓ ~sànBøºR\x0006
UÑ9	Ðo÷Ø6y÷±Í\x000f?\x001eÏ\x000eéí=¬£*Óåi¶+½í»¶[S\x001fíôs#\x001b¶ÅãÖ &K×ð¤$À¨tÏÑn'1?Û\x001eó3ØS\x0000QÐ¬ÈÁýßË\ÔÛÅF÷¢M\x0016m_l\x0006\x001f	Ì@¦#a\x001bDÓüÆhK*Ç&¥Ø¢ºtÿìúË'øGvÅ`ð2ÌQR­XIÆg#íÈÝ*ºNIÙÏN__¾8\x0003³z\x000cfu+K\x001b\x0016?æè-\x000cxBóå]»¹\x001ds\x0005ÛÁÅO²\x0011\x001c[Ã]	DHcèäqÌ\x0015c+\\x001fcæ^(F þ¶2³U\x0015»¹FáQë§-Æ÷q9\x0014SgK\x0006·'S< LêkÝT+ï)×SKF`z\x0014D°\x0014¯j\x001d1ðh\x0013;ÛI\x0004wFax«õl\x0011æÎ!3¡"3¡Ìä(~FDmb~Të»Læ|\x0015ðN2\x001bªÉ´¡m6áwÀUkÝF\x0006\x000eãÉr\x0017î[e6WCfsëi¼þ2q\x0014êC0élgñ \x0007l\{jÇªuÄ´\x000fÃ
\x0000|FïßEÛ·È­Ál3\x001d^\x0006R	p v²úc-ãÞ
¶\x00112'0ïZÁX¯,7äùÚætô½dõ¾tÍûRa½d&Q#un³ú;É¼©&ÓÖÉT(ù\x001e\x0018UÉóöÃ5³s*½­\x0006ÌÛæ\x0001ÃDGÙe¼
\x0003//ÞMV\x001b2ßlÈÎØ\x00149Ë<`^|Òlyû\x001e²zÌÚ\x0017\x0019·¤1K`¾ÞÖò®\x0005çå¸rÓú'ûOrp÷\x0008-¬~îÏ\x00037\x00089Ê}§)\x001bÇ\x000c,µ9!\x0003«5´ü\x0018\x001c¬îËúTò§\x0012ù<\x0004Íræ¢fo¼íX;¯À´,Ô;34îLLùRwÀù^qåxÚ%\x000b.\x0019¦ÈeÎÃLêeäZÙm+Æá\x0015¤ò­.lÆOySi!Ã5\x0014¤NG1Ô\x000b?4/|°\x0010×3¨
å5Wò¶\x0017¬vúC»×­ÜÞ\x0012v/#¦¢¨¬;×}½#Cóü¸øI} ü¿Qo\T\x000c¼½»û´3Ï=*M6ÙÌ\x001c\x001eA±Ï5Üózç\x0017\x0017\x0017³\#×Â?UNý\x0017L*ú¯\x0003\x001bç¹\x0003Ø8Ï}\x0019YÐ\x0013}sÌ\x001cºNÌ+jÑÎë¤\x0016²'¿Å\x001a,6EQYÆL¡VQ:\x001c{£ýÖç^2êE6\x0015ÌÜ?Y±½\x001djù\x0014±(Éê\x001b3ë'«¬uÌ\x00128®Äí°
°øü1D'dyêíN²T¥f2\x00113YôRÃ\x0016"·0BÏ¬\x000fl¤R`9´9#}n3úÖå\x0005'ê¡£î\x0003ó¶ZeÞ6¯²\x0004&#Þ!qT\x001dW\x0019ÓÛ°ûÉBM\x0016ÉðZXYrhc°FzJÚí\x000fÒ{±®XÐÍ\x0006\x0003e«\x0008L\x001bEÛ¤\x0004¬e¼ÂöÖ{ÁbmÉb³%\x0003\x001fçl?\x001e¶ý0^ÜÎ4Ì5RÞÇr5)·ÎcHr,\x0011ÌFiñ\x000cWây\x001f¶ç
î%\x001bçÁ/óTyzÿ
\x0011K2dÕ\x0019£O¬Î\x0008cæú\x0016Y®×~n_ûQQ\x001a(,\x0012A\x000c¬ÏÛ;Ïì\x0003Ó\x0013\x0007~nÍ ÑCä!ãåjZ2d¾ËiU\x001fôsëIîÅY\x001búe#,øíM.÷¢éÚÆÒÏhÎSc=GÚj4\x0008Nf²´=e/Ù¨^Èn%ó@ÆvÖFi&\x0014mð²\x0005òöâýhfÖìe{¥¨j
ûÀ±Êî´°f\x000b\x001aü²Ën\x0000 µÚPÌEQh°Óf}Ø!c¾\x0013+NF,¶\x0018¸äý8rX¸û_4\x001bøøØåÁÁQÙfCu'\x0002<ùÛØ^\x001dSe\x000b6}[sâÊêv_\x0016%eÑ»@4|÷åÎïNzj}hf\´FLÕ:j*x\x0012®sØpj\x0010¢
Z\x0000\x000bÜv
X?Ë¼Oñ*\x000cgÜÅ§/·?\x0002ô\x000f×G/n>¹ùº+&¥_T¦\x001eÊlæ6Xqµ§I,\x0017¯Ï_½*Uè/¯N^½z}öÓÙVý²\x0001ÔAM\x001f(&¹\x0002jè\x001fø44þçü9Ðíú\x0011\x0003ª\x001d£Ú.TXn\x0014Ü&¯×m:ap.²wN/\x001bÓ=¨nêúF\x0015\x001bÓ³ý¹8ï+»Ì¨jâ w¢ú1ªï\x001bUp\x000cbÙâZ'ÞG(l2¸ìÆ\x001d\x00025QCç¦²Ç|\x0019³iè&#ÏïÞ¦tùcÒØ7¨)Rf\x000c
ª¥ê÷Ç§³¶zèDMcÔÔÊpyTÅ1tre³Ó¼ÎNÔ<FÍ}ó¯HØöæ\çµÀ²ÿÝ!H\x0007¯±Õ¹\x0000Jz £.J\x00128ÀÚ}\x001eÕi\x0010¨µ>ªzÏª¢û¬)K4\x0001\x001b²\x000eÑ\x0004{\x0008Öê´Ò}ÇU@ñ 8«\x0016­\x0003\x000fku\x0004è¾3 `XrêøZ3\x0004ÛòA\x0006µ2«ºÏ®XR\x0013(ÊÅE!\x0011CL\x0012ä
8\x0001te¬tµBWÏ±
\x0008FZMÁm'ÉÁ:iïÚÆm\x001cñN»\x0011 ß8¡Ç¯FÏoßýºO»Ö¨Dy\x000eß^µ\x0008\x0017Ì`|ó-LÃolñõûëÏ_\x001eæ0G\x00039I\x001dX©{¤Ï²J½Or+Ên>\x000fj93¹<Ûl\ý¬ªÆSG/o\x001eÞ}ÛÁg0Ì³î*h¹\x001cr\x0013­{yvõìÏ{Ðr\x001bÑá2Ì¬mæ\x0019N\x0008WÐüLâÅ"´ñRæ7¥¦aãwñL\x0015_2jRÄ
\x0013<§¸ÍTÃ¦Mã¸ O7\x0018$.)I\x000f\x0015æpÏIî«òÕq¹Ü8rXÆt°o\x000eòÐùÝÓ:+\x001ej&»\x0001Ç­JÂ;z}}\x000f\x0017àÓûûë1
2pÆæHÉè0<I'é£×§/à\x000e|úâÅé\x001eLL3\x001faâHN;RìÄá¬rrfOÎ:qf~äL\x0006\x001c_áË¹\x0019sÎ,JÆLõ¬§i×yÐ\x000f\x0002Nn\x0004´\x001e\x0012ÐÜ\6Õ\x0012Lå+\x001fì®[½ºþp¿§>Æj91[tJbþ%~Fj\x000eW§?¾8=Joór|\x001c¾½|XkO¢\x001c\x0004ç\x0010`\x000f»àfD\x0017ò6ß¤©Å\x0002Àâ~ÑûåBÓR·Ì§æÓE\x0017ñùjü¦Ùöó¥ìä^kÁts<0)yx\x000cvÞ©Y\x00028\x0016\x0005@c[\x0007\x00105½<

\x0011ûi?åmhGæ"ÀP\x0003f@t\x001a\x0002\x0003:~vx»Jq6óv\x0011_®ùr3&{ÄsYÚ\x0019DÅ\x0002\x000eÞG?¹¶\x000f×ÇKãø\x0015¹\x001c\x0002\x0014í\x000b\x0018@yÇòa>éo\x0011`ª¶Hm©­ÀÒÈ\x0000\x0003çòD\x001f\x0001T«&Ø¥j]j`£°{	øZ\x001d%às\x0012\x001bcöÀÙ\x0013ÙO5´½z¢-Ø\x0016üv>p9\x0018B\x000b%Ì¢ÉY\x0006Rí\x000cFZì\x000f~Fgú\x0004Q@G\x000f^G¦m!Z0%ÖktÉÞÅ7 9R`\x0014çezæzDsïÂÙÈ¾òiÓ¡m\x0008õºU#ªGI 4¢áI§¥Cªá¯K
0¸Þ\x0014&E\x0014yëÍ%;QU¦Æ*£D\x0017XZ|W·ooÿùû*¨Á½U\x001cÐÃc?ö\x0019'ygâêü»ºFóÉU¦@Æ
2v@Òs¢»ZPÁ\x000c!s5{»_È«Ì=\x0003	\x001d#§¥ea7vkgË\x0017#j[Ïµí`\x000c9àu\x0006Ï,K@«K½uóÙBÊPS\x001eJ\x0014?å<º$-°£Wò·£¬g!d¬!c\x000f$jñlkQwQ<íý1\x0006W½ßâoàûíË»ëwô®|w}ôÃ§û/×·;\x000bj°`sÓÒò$bÂ 3í\x0007úòâô\x0019=-_\x001eýpùâõéù8í[~1Å4cLóÅ´cLûÅtcL÷ÅôcLÿÅ\x000ccÌðÇÃô¡zÿÄßÀ÷ÏMïûëwó.£("ËÃ^ÂÊ.\x0006+Q>½ÕiÃ(ß÷W§Ïf-Pá\x001a§P\x0013ãÛÀ\x0012U°üå´Kl¨ %::Óá~\x0011­FÌ¶
\x0019ø\x0012¥Ê\x0016\x000f" çbNNl6Þ½\x001fÌ6\x000eÒ-dØÈ«Dð²2Z0\x0002ÚFËÀû\x000eÓûÐÈÃ\x0019g¥i»×·\x000f×\x000f;X`/<\x0011F¾ùÀ3I$ôB¿R}wuzµã¥\x0000¦
0µ\x0003j©\x0004B#}L"k³£¥ï"À\\x0001æv@eé\x000e:²o4^TÃÜsÆRÂ±H\x001c\x0010êiÃÜý.\x000fA\x0006ËÑy\x000cíÐÂÐÏß«w#¾UÚTnÍw\x0018¦¥ýqýñ÷£{¼~ør{ó°kPø;¨Àp°,ýÐöI$þôùË£{szõ\x001a<®é\x001dj 2c"ÓD\x00145?ë%¥°Â\x000f]Z°zz1YDdÇD¶(\x0004©4\x0000g¸òV"6\x00053]cÜÈµ\x0011Yöæ\x0013öA)\x0006\x0017þçNZµED~LäÀ¸
\x0011E2Ãè$@¶oÂ\x0018(´\x0001\x0015ÍC\x0004
^ÊYÁFpä´HZD\x0014ÇD±H·DX\x0002À@ÒY7MÓ)\x0017\x0002¥1Pj\x0002RA<1T¸bÑ\x001a½\x0010å'ïò(·\x0010ÁÖ¦:\x0017\x001a"#\x0002'àJÈÞOz.!\x001aò¶}TMHÎ¢²á°\x000e"I
\x000c =±ÞjÝd³\x0002G@\x001a$
Tâ\x0006 ¤zæMW6[7\x0019íô­§ÇBä\x0004(<	\x001f.\x00002©ÚýøcËâ¶^Zp\x0018\7Rlf>¥T<Ób^\x0006¬:CRÛö? \x0010zôè¹¹ó9~1y»Øã\x000e\x001eð¬\x001er
\x0000ND6j§W3jmoà\x0016öæjÖk%G¥"Ã\x001f[Ð¼!ÁwDËl)±»]{Îl+Ï\x0005d£ð.Õ=Z÷a{[Ë	*Ëkî\x000c~*ßfcfc\x0013\x001aæ@\x001527Ô£\x000e×>Ï^Áå\x001a,·-´Àç\x001eeißi²ôªòó½O\x0017 ®`VwÇÜ\x0006®9§i_ä©Kôa}ý+ÍØ
ÍØ6´Ù\d|;2ÒåY´{°Â¦\x001fÍ×h¾
-\x0014{jx\x000e\x0017'£&
ÏÓðÅ"´PíO\x0013Úö'|±Ö)\x001cÜÒ\x0018s\x0010¥\x000f©oê:S\a\x0013È\x000bÖÑÝÿûÞ~xÄ
¥û]gÉ5|ë
Í\x0008öâÓ|ë
yGËø³££Óó\x001fß`©Ò§¯Xutó\x0007Öôä¹m9,¶·/ÞÃ^VÌêD\x0018\x0006ÅÊ×±kñ5×â÷Â:ëE!Os\x0016\x000bfP±\x0016\x0000·ÃÖ\x0003ë×,dCã	twÖK\x0006«³[ßà\x001ahC=´aÍÐÂïXÖ2\x00050Ê§EÊ'ng+­«iÝ\x001aZ\x0015ã$\x001c@%î\x0017­è¸»\x0018¶y7M°¾}òöÞ2´VDÇP\x000cÜ1­\x000clzrëi`õ öã ÖæõýôñíÍÃÝý0m´Í¨½ô¦ÒFô}ÃNÎWG§o¾;»z½åá½@Tk\x0011r#[Û\x0006©D´bÊ,Î¬¨dÚ­j¿)S=O÷ÿ2JÔv8¥É.Gñ\x001d\x000e(·6
_Ji\x001eSâ]°Ï½4R\x0017YÌÁà9mÐ\x0008jÈÔ\x0007ºHÞ°Dâë°ÂOuºÛ íH\x0014[£ötè\x001bIìÍ"fV:vcd<Ç5Òò\x0018\x0010ÒnÉ\x0003Z\x0004©æ4*(úbd$Ù\x0005´\x00072ÖÛ\x0016B\x001c\\x001ab@É#éÌÖº¥ã>yx;W½\x0012n\x0016\x001bHÑÜwnÕööºôº\x0013R\x0015ÒÛ£ôUY\x001aë¸´õf¶ÒV¦r_·l£O\x001f~\x0014ÜÚ\x000f;þ1eö]\x001bü\x001alyõzrhBÉ;`¼¼»ýz{ó°;S)yRÃE´R\x001aä¶É\x0015ã¸øì\x0002\x0018//Î:?»4cHÓ		d,¦¥ÀG©èùÆÿuvLi;)È*fpTäIÏGÙ;ÞMº­6Sº1¥ë¥4t)§HPà®@éeÆC¯7]DéÇ¾wÆ={lY£ð\x0000\x0017\x001bg1é\x001e\¤uaL\x0019:)±±(×U\x0019îï\x0005ã+}\x0010|Ô+e\x001cCÆ>HêlÄÕ_p#æXQ\x0018º[x¯æ\x001böPNÅEô\x0013qïnîîn¾>îÌ¬ó1X°	î%GtµtÜ}¾£Zû»³³ÞÌêê©°~",²\x00082\x000fú\x0007\x000e½5/êD\x000c\x0019SZ\x000fiÇ¶\x001d\x00123ÌYO\x0004ÕáJ$ê&qº$¾L¯tcH×\x0001	~$ËÜÀUq#Ae¤ßÛK!ý\x0018Òw@ºDJO8Vr¢\x000cxpçÏÅ¥aÌ\x0018:\x0018Á³×êu©¤'£OzÜÃøV\x0005Ò\x0002ôu À\x001fO.®¾»\x0006Ì£w{Ræ\x0014öðàÐF³oÕ"ì\x0000é0Éûº8=úî\x0014\x0008^^ìL\x0013º\Óå?\x0006\x001dfgãü*ÓP8}\x0013ªþéöæñï;M¶±Ô'ä+´h­D%:nÚ(£Á`¦ßüï§\x000c¥UL¨pthà¨ûP\x000c4Ê\x000c³LMÐAä\x0014RÚ\x001aÓßÍãk\x001eßÀcK_$*¤ñCêú á\x000bÿLËøÒ«iTÏê·V1ÿù+LóÎ\x001då^\x000f\x0019+pO4\x0012wðs¸õÏ?]¾x1«äP@«:f¿½y/©QÛ(>ðò`ÖqÐs©	_
ÿæzLá7N¦íY~ýôx··u\x001e\x001e¶F\x001em¢ÌµÑ<×.äùbgº|s±;¿8Ç]K=f5t&#7)k7)Vòoã´yo\x0013¨.gÆFþ\x000e!}U\x001aþ
§~gØ>kéÁö\x0015u\x0007\x0017\x0015\x0017\x001a:og'Î^áïf\x000bÙÙðÇ\x00168OKåg£åú(G]	.M½p*XÕqú·=ñª.ÒüáúþÃ
\x001c\x001bîwVÁ®¦'z.X6\ªÍB\x0014a©dæ{RýpúâÇ38>._ÌfEÂ­±ÎCÂx7üG/Õ¼qúRQaT¦¡.¶·¹J;fPeá_\x000cÃh#1«kd.ï\C`Oðã«µ\x001aâ¼;¼\x001dºË\x000b¹\x0014é@úN\x0001C\x0005\x0018þhUcä§&æ\x000f@8~[\x0007Bãÿ Vÿ¬ßÿ=ß}¢\x0003\x0005LhÕF\x0011«7Ã\x0007¿~yÍ\x000fV¶6ü/)Ïé\x001d8Ó×H\x000cj\x0017Rõ V\x0011@R[òØ?nHàXx\x0014Ùç?²§|:²6à\x0006>#7\x0010~ýò´z¼\x001aíç\x001aèún¥Öjõ\x001auøt¡¶®Hã\x0002µÂÐÒa©5Í	}ú±¢WÄ¾ôð\x0003ì¢ý\x0000)l}hj,)ÕU]iÏ`Ó%\x001a¨ÁÑ¤êg ¶åa\x0006ëòñ\x0012}`l\x0014\x001cªTZ±uF\x0005`\x001eì\x0010Ë\x0001­2c'\x000cÝ\x001f\x0018\x001bD­¹Ñý\x0008BÁ\x0003B\x0001ï:Mjñ\x0007Á¶\x001fÝow0~Råç<»ûô¹Ô{~z\x0004öÏ;Q
5ðH;ðô0¢æ=&·3257¹\x0018ýi[¸ß\x001c=»¸|U@/ß\x0000þV· ¢F}]\x0013W`³ô7

î,Ç¨¿be]ëýÁ±1µ­NokÂN:\x0014ÝIÜ®tÒ\x0000lìÄ\x000bÄýO`£ìø	}z¹a5§²J¢I%Ð]\x00194\x0001Øl\x0002âþÅÜþnåøÜÉ³æáÓíçþ×ÍN»\x0017ðíüÇS`»\x0007·\x0003UÁWÀ\x0013\x0012;ßWç¯Î¶:ã5$¸µ¹\x000b2
)@º\x0012<DÈÖ¸\x000f\x0003\x0015DÆô
e¢Ê\x001b¤RÒ0¤Å7\x0003AÂÎùNT©@¶¨=\x0010¤\x0015J|E=\x0010%¸'&ôR:¡ä·?¤äí\x000fØ³c
¥w\x001f??¾¥üááæÛÃí\x001eHl\x001eK\x0017C¸ÇFn#¤/y0¢&ïÝ:?\ýùê|\x0001$8\x001ffê-TÜ%«P*1\x0008ÒòHZì{{ H\x00137õÓ\x0017A¦\Ü\x00014þ¸Ì¶æf0Û	û&\x001d\x0011\x0003\¾1f£\x0010£-
!` S\x0012\x001b\x000eéO¡\x000b1äâ¢ b*\x0011dÜ5E\x0003\x0015\x0011ýÞ]³\x001bò÷\x000f:þæùiídj%¼~x8;!£/A(ôºäíÀdãCZYXu¾\x0007òÇÓ«ïQ\x0015g?%Ø²é­`!¥c\x0005À\x0012C!½lmLØ:\x0014$¾\x0017kÛE\x0019,K÷dT\x0011\x000e¼qr0²¹÷8)1k§>ÿ2J\x000cæÚBéByÖ÷Ñ(±&½Û{9&ÌË0¡@3bj¤\x0001&¬LÆÜ|/¦Ä\x001c ßEáþGYYË·ëh\x001bl¥ÝkcâÉw
&jò`:MRçiÃ0çúp»\x001cób×\x0006JpëO<pPz^>\x000ey¯Å\Ïeiêÿ.Ã4\x00083s$(ÂÆÊbÂÚµùÍË¿¾9©×·×÷»!Q*¥4`ÈpQ+5]>dãØ°'m¹à÷íKýoÎO·¿0U\x00184y\x00128Y\x0004é)G ])ïBÈÈîPR)¯¼ùxÿÛ·GZ°Ãc­¸~õI2\x0008w\x0005G¢°<Þ¨}\x0000ûT\x0016¥uØïåOÛÆwÇ:p\x0016\x0013\x000fÉØ\x0019yQ\x0002&\x0016ö\x0006Æt\x001cTu\x0016íðZLókøûïfÍ|<zuóð°sº5ºèJÂ\x0008¡\x0014£vjÉÀ !Fþ£¶ÞÅ_]]ÍÍõ@bÐ'ôiÁÙJ\x0003éH«Á\x0007åÙ[`6\x0007Á3.9¡\x0011ÏªÒùA+o¸èÖã;^\x0008%ÑwoÒð\x001bFøsR=x{âµ.\x0007¹2`ç2r)«²s;÷1Í\x000c7\\Rë®ïçò¬M\x0003J\x001f3\x001cÏ)é\x0003pi|T¦O\x000bXÛ*S\x0018,²w¢ÔÐwýåæÁÄ{\gxý3®\x0002{ýëí§ÇÝ+ÍÀR+"©\x001a»
7×Ì¦\x0004þDK\x000bMþ¬­|¯ÿt~ùfv±\x0018-2ÚvFU\x0014{5Ú"v¶\x0001Rì\x001dº^\x0007¤²\x001f[ëZ-dB
\x001e¬+sìæX¯¡ÆRë\x0008oLøëÝÃ¶k\x000b\x0000¢\x0003òx·û\x0000\x0006yß\x0002-ZÙ\x0006¾F'çÂuø\x001a5Qß\ì\x0005\x0006É\x0016\x0002\x001aiH\x0003N3\x0003\x001a+\x001bÅ;{(@°,µ¨Ú2@Cub4¶´C@o\x0011Ügb\x0002Nï|\x000b\x0001Á©.Úå\x0019{\x0007ñ\x0014&Ë\x0008îq\x0004\x0003N£9ËGÐÄ\x0002h¹tF¯ÍpÚg\x000b\x0002Nc9KGPÑKõÃ\x0014«$§VñP°Cû.ær\x0000Än;GPÉñ\x001béJ\x0018@Ø ¡}À\x0008ò\x0014û\x0014JÒ\x000e\x0002J0\x001e</(@Úñ[\x0006)øNT\x0005N{$eá3ëàçÛëðW©\x0018ªÅcÿûßÿãìÃÝíç=7x\x0000\x000cÅÁþ1\x001c\x000eÑNÌ%\x0005ý'wÎþåÑÙ\x0017ç¯æÎ\x0011_$6óa¡a
×cÅ±/kðmW÷\x000e>øÏ´=|Q\x001cTí½D½4; ¢\x001eÜûùtúíÃo÷[ç·R6Ýu\x0012\x0007	Ë\x0005e\x00190dÇ©\x0003p\x0015Û·ÈVÓí_ïÞwco{ã>\x001eÉ\x001f¼\x00131\x0006òbp \x0014$)È.±¢E5Aä\x001e¹o°GîóïfýÖ\x0011?!ñôF¼R,Ixãí\x0017\x0004Ïo·Íxè\x0013á_mxÙÊ\x000eÁ¢\x0001SV Ò2Á1Ì\x001csÍxb£ÛðByØC<®/ÇÑJÎ°ÝÏj§c\x0003ÝD÷KÍ§dðBJNæV\x001fhð¨à>m£ç
·çÈ\x0001s%xí\x0005£ÅEHÛ]f>Übôiã\x0003
¾\x0006ë4¿^\x001ep\x0013f(\x001d\x0004\x000fscèÓÇúfä\x0002\x001a¾¦gg\x0006\x000fÐ\x001e\x0008\x000f-\x0000}\x001añ4§\x0012ä\x0010¼\x0018Ý7Âaì\x001efþÐ§
ÏäcÍx¶\x001dä\x00127Ä\x0012\x000e"\x000bôiÄ\x000bÔuðb)C<#îóÌÁÖZj>ÕXBDÜÿ\x0019¯\x001fò\x001e\x0006Fæ0Ïà->m|Úc\x0000\x0013IÏ ä\x0006¾\x0001gå\x000fcZ6Ñ¢6>\x0015Jûì\x000c\x0007,§Ù\x0000fÇ4x áÃØ=}\x001aO\x000eÏ=Óñ\x0007ÂdÅAS¥¶_~Ûé0¤\x001b\x0002U£"³EÊ\x0005é2±ÙÓaøðå>m£g¹	\x0011¸Çºt¶c×È±½[eZ¾ù¯÷ÔÉÐ`]ú0\x001e\x0015<>ìÉïCµBS\x0012W\x0015Úhº\x0015y£H%¾\x001f]lþ°§T\x0016òf¦êghñ
H6D_R?(NÐp5üäq\x0010Bzm·®0$R©%Â\$ù\x0000[µ#"fû¯B¼sþ/\x000fï~\x0006\x0013\x001aå+G?~z¼ÞIh-*Äû\x0012ñ¢\x001eÊ+{Ê®¸Î\x0008»¸ü9[à~¼|sº\x001f
KsÊ·	-sÁOôKã\x0010#\x001b*áJ´ÂAåÛ\x0016
Åª\x0008Mö\x0005ÆY@-ûÈ~{ÿWó^SL\x0012¯ãvÄ\x0005÷ÝëÇì}DwJË±ª<¾X¾8¼\x0005*Jð¸\x0018ýiÛ áÎ{qúæÿìxI\x001f¡b\x000c?õ jzÑBÒX\x0012åÑ\x0008bC!õXøqHÒÉ\x0005n9©
§´§Kfn\x0012D°¤Ô\x000f;¹ÚÍQSfÁ	\x0014A!ÿ\x0015QÁÜ0jÖ\x0007<]Æ'ÌrTo$¼à\x001e\x0018ç§&EB(\x0007DÕ´ß«í¾|\x0005$¹(gíô+®\x0000\x000eÀ°Ú\x0003³âBÕ}«Õ¨\x00155G\x0008\x0015/õ\x0005U[s`Ô·¿Ø³\x0004¨sñrsi4¨d5y~\x0007D5\x0006mºV)â÷x\x0012rBÖì¹V4]\x000eÊµ\x001fôi\x001fÖ\x0014ÙóÐC\x0017>â
êaI-&RÑ§4x
Ðx[(øÕ²þ°¨O¼Íå¨°øa<²\x001d$Õ^|â`\x000eVôiGµ1¬Ã\x0013¹O!
ëa¶ÕWßþþ³2\x0001_\x000fÊw¸\x0006½ütÿåævÏó\x0010&MÒö(Éç8¿Åë2¦ÚÛxq3üaÛ®B//_¼>;{!Ú0¢·]¾m6\x001cÓyÞ'ûÈ\x0001.\x0011cÉÿ:\x0008"¶\x0007.ß6DcJ\x001fòð^\x0019ä6\x0019\x0019Q\x0015=\x0008b¤í3m\x0012¿qÄ$­È1;fÄ\x0004C1fhd×Èè¢ç·¬Ýb]±ð1°ÙÄ\x000b]<\x0014cÂòmctKbÄ\x001a'öD¹Ä\x001b\x0010õ¡V#ø	TÞ¼a0Ò\\x0012#¢wÏtI
S¹xõ!D1êòm[øêÁAÉ\x001d)åÌ÷Þ\x001câ¡\x0016£Õ\x001e­8}\x001b\x0019#ç¿D\x0014éd@ËX\x001d0@G­»ÅGUJnq£xï;\x001fâDÇÃ-EÔÁ)ß6F\x001f9Ã\x0004\x0018Í\x0010gój`<ñ¶ôRV¾mÛEÅ~A$OppK¹6ùpsiÃäö
\x0013\x0005QNä´\x001cÐ\x001cF17o¤)F&H6VãEÙ\x001elGÓ^ù¶M´q\\x0011\x001d8e\x0012È§4ßË\x000fC¨ÉÉÕ=K\x000f@Té}@Qó!\x001eè\x000fu\x0000\x000bîÈ\x0011o5;\x0001¼\x0007_b(å%q¯a\x0018\x0018<ØùbÈìf³3mx¦m¤ü¢òôåÑ\x0007}0Fô\x0016Ë·\x0011õ\x0011ó\x0012¸[ß\x0001cÈ\x0007c¤âúòmcÄòDkíÄÙÉ¯\
¼ÝµæÛ~}{û\x0011[ÚR\x0003%ú\x000c·-Ô¦zI4;!H~\x001dôE\x0017\x000f\x00062H\x000e\x000bv[
ØpÍB©ªô[û\x0008=eïøvB+>ci/bÝ(\x0006iù)\x0011þ¡mÅð=¥àc;¡J$Q\x0016#Ëw\x0000¡;Ô\x0018N\x0012\x0015\x0012¢Ë¨J¦\x0007Ø\x0003Þ.!gV¼0Ø?è O^Ï²Ê\x0007ë\x0015eÍP	<?)ú­yx=|RWÐ±
¹\x0008ÑºMe9×\x0015\x0018Ì:\x000c ºKôi\x0006T¤dâÐ½vô¸]\x00009\x000c¬ú¡\x0008ñ~];a°,Üm6¬rÇ2çó\x0004t\x001a\x000fAhéPI\x001d¦\x0006\x0016Ê6q}¨!Ì\x0007²\x000e³^éÓº±ýL\x001a\x0012Þ¸°XFzwVÊ~F­ò\x000f\x001a\x001f>I÷¾\x0003äÕõÇ|VÁ9/¨¬JäjG°aPCÃ}ýqû\x0000^>ßÏ\x0015+¶p\x001cª\x0006É\x0019y*ö.Þ\x0019õ»èáúýï¿Þqþ	DnLõêæ\x0001Å5aZ¿í)\x0008rÁ\x0010<>%¥Dòút\x0019eý\x000f«BØr\x0015|(¶	SûçÙª 
**\x000cNT¸,³ÎJÔ\x000cBÚ¼$%µg\x0005¶¡b3¤Ôj½ì<ÔÄ²¯¼3K¥\x0014þ´¤ûH\x0011ý×?.HÔs-ôAÇT[Jó¶]¨\x0016\x001b¨ó b1>¿ÏË«·Æ
§\x0003¢âE\x001eT|¦w¤\x0012Ô£·dÉ`ÑIïLkfEçÌå>VðÊ,?ÏÀ\x0015¤¹\x001c¾y©Ì¬\x0016	ë:µ%Bªá¿Ù\x0016^\x0018ÄG/«ÔÎÔÍ6VM\x0015xåÛ\x0001ò5å@\x0002wW,«ÍZä9±ÕÜ\x0016
Ã^ÔH¨}ëUùPòáðÔjÐäÌI\x0004P)Ü°5_ÿöøùïè`Õ:}6ia¯n¾íÎ3ô"Ã©-åï¢rÒrRaèrÞ&+ìÕÙgÂ6éC\x0016@l}X"t\x0013TA~Ägä\x0003\x0011f®\x001f?q/"T\x001c¾G¹\úWxý ½\x001aí¼jb+!&áøä\x001a	u,7nÔ+õ|ÆÃ\x0015rYÍa^E³\x0010+÷éÓB\x0018\x0011­à\x0010\x0014+H\x000f"\x00044ùP\x0001³xèÓ\x0004Õ°\x000cÁî®ÏV°Q|çP`,NNèÓD\x0018JÊ$¹ês}Ö\]aSØ!ÚL¨P·\x0012ú\x0005ÒÊÔVPÙ,¶Û\x001fÌØD|Ê¶u\x000c].µe($*Yî>Im\x0019\AÍÁ¶rÄGú4\x0011Úrë!aÜ²S\x0018nca^æ´\x000e_\x0008£o4ÖÁùrÀ]Rza!`ÌÃ.±é`$v\x001bgX\x000f6G0\x000eD»Ã\x0001âÛ[L­Chµd ¡·â!\x0013OnÜI\x001f\x0010`j]°3¬¨_'~®ö°5\x0006ôÃmÝ#èÓFX\x000cüræ·`85ãp\x001cn)g"5\x001b\x001aUäYø¼ò{¸8&ñ\x0019\x000ew"gÜÅ¹}+\x0017í!!r¥r Ø\x001aåg4é,ÒÙÖ£Ä\x0007/Ûð.ÉF\x0014Ø\x000fÃö4ªX\x0017º
|}\x0012pR$\x0014O¾\x000c×OÛ\x0010B>\x0004&içòmâ±¨4\x00002û\x0004Ç°xbgà£ún¥[}Aí\x0015\x0013íR¤\x000fÍmâC$PÈ!øÞî:Zezç+ÀÛrÐ¥f5\x001e¶\x0012<)ß\x0016<ï&\x0016¸p±T\x000c^Ô×Üav®6ØR¢|øPIGL.ªS(:X>{ÙµJj´ÌÚ:9;<ú
+¹XCÓ´8Yæ\x001f¯\x001f\x001e®¿¬°ÌT8Ê·	E3\x001118VÒñÆIÌ.Òóû¡\x0010\x001d!6Þ85*!óéá
×*ûAÖÕ¢ªïá\x0010\x0003!6:	0Ó¥b\x0014'Ús4ÑkIj\x0003D\x0013\x000eø4al\x0011"&vóVÆâïÀQ®#!çC\x0011âËñIù¶\x0010:8Kb)BñÙ\x0012áfI"«åA,Ö
@Ìÿ(ß&@pò¹*\x001d\x001b\x001d§b
ÃÐª¥(\\x001e\x0006Ð\x0012`£'ußë¾cæ\x0008\x000f~(
\x001eìÍz@âÖÐ×V\x001e0\x0016W\x0002pX\x0013!3¬âAøÃ,¤òm
nE-\x0012ñV;$áã;§ñ1\x001dfáºä~¾Æ\x000b;¹n¼~téL\¯çt'\x0019Fð\x00107:÷óÛø¶
QÇáÊÏ,ìÕ8y±ÄÿþúwÿíÝ¨oÊÕ£T<»ýH¿,Oñ;\x0005°:\x000bÙ[+\x0012×zÈ@\x0019mOúo¤äÙùsúåO(äµt(&íA\x0005ïË\x0016Û\x0008>ð e´ Æ­jÜÝ¨\x0006ûQi\x000bQ·Ê
©\x0008rû­ªc½¤Ò±¢T±\x001b :vÏ¢Æ¾¶j·r÷¢\x000e\x000fë\x001d¨¸4ëã\x0013\x0001ge»1ak\x0013nT\x0011\êBÕ4ë4ªiÈ¾LyX\x0000[eø{Q#E;QÁã\x0018\x0016´\x0003qÒkÃom\x0008ÒÍ	Û)vn)lñTdÊÓp\x0015\x00146Óù\x001fY§x#¦Hc\x000f©\x000eâ(¬&×¢XÆ[ÊR³Ã¡J)y\x0007*«q¶r¢a\x0011ÐI\x0011Ô­M-zQaÒNð¯®Qõ34aþ=?ªoò\x001f)ûP #5³\x001eR§¹â#a×]ÇVÒøP¡u-êm¸þö'cúxôâúÿßNÏÄD\x00179\x00197e¹\x000c.êå\x0018¥Þ	ÛùÞ\x001c½8=óG\x0006&Mq*
S-Âgs\x001e² \x00037Ú\x0008Yì\x0010öÌ^É$Í5\x001b2×¤ì¬äUÇ4\x000cÔÖ\x001e?-P\x0002úòÙË¥ fÏò\x0015\x001a\x0015(M¡øUPCcÌåPp\x0013eú`¨X\x00041\x001a%ZÉÚ®B;DåÓa(Í\x0016ØÔ<
Tè2áíÝß¾Þ&Ôf ^ÞÞ¼_èu
úPÚ8±e:8éx/³h/ÏÏ¾ßg\x001fF"YÚÌè\x0006	qm¬Lª\x0003×y\x0017¦\x0011ÓM\x001f#§Ó\x0002#Þûy £\x0017ù\¿Ën4Br½¾Éf_=´ç¡gÜÚ÷¦\x000bÒré\x001côØµÒa³-Íyv6FÌªs}³m¥ÐEaäD\x0018¥ÐÅº­Âº ±Äç.È!©VÅÀi#¸$\x0005Ò\x001cn$E½\x001dÒ'*óDH¸ª\x0008d\x0016Q]l²p0HÖfï\x001aÉÌØµb\x0018IfÔ[\x001bSv1Jó \x000eÆÀÇqV¨ôg¦³­w9Sm(Ñú\x00062±\x000e\Æ\x001fEÐG·ü4éço!>þíãø-ê¥´S\x0006wI@{{óùËõ=é"a\x0005V\x0007;|£)'àH\x0004oK\x0001·Cw\x0006\,úîìÕëÓ\x0017'\x0017g¯JÇl8¯ß_þòp3üXâÏï~¹3ïþ2Ò\x0014¿øôå\x0016@>ÞÜ9ºC¬Ow>¾½½'4ÍhñäÙÍÃ×Ûþ'*õ¡àMØ¾\x0000\x001fÖ.iêö^)#	Ì2²]ýt~\x001a~\x0017¯ÏìùÙ×GÄyyqùü»ó\x0017ð·nïß}º¿¼\x0019~ñµèÇw³¼\x0011dýÕ*[X#Åù\x000fÆZ´ä{Y%ÝÅ`NtÉäFÖ$¬	+Å\x000eÆZB£Ý¬¥PLÆÕ2ki´ãvò`¬¥µ{/«UåãÊ}®Õ¹a
\x001cr	#\x0014V ºò\x0004¨pÝS¼\x0004\yÍ\x0004ÔxÐa-íS{YQÛÓ2k*9ØO³Ärq¹z@VøïNý¬Ñd<\\x0002þW@NÕ!µôAïEMÅ¤ÒÎrb]
7Ë¢\x0015\x000eÇ*\x0017µ^ØLÍsÕû\x0001\x0002¬&\x0007Y®æ¨$TßE\x0019\x0019X\x0012\x0005~gV\x000eh]QH÷W\x0015; Ëm³\x000c¬,7×u°¿ñ·7\x001d»\x0003È÷ëõÝï;ÙrNþm\x001cz)Ôâ\x000bÍ}ÉyL>93Y Èó§Óó,·ñãÇ»»\x0011ËÕÍ/\x001fn^\ÿþéîÿE¢Ò³D.r\x000bw\x0006.\x0016Ü\x0018Û¡\x0015ÁzT0Ìõö¾:ûáÍgG/N_^^]¾ÅºþôVýýÛø´¼\x0011úçÿûåæúq÷¾p±T¢ä\x000e\x0006'ð\x00184!º8Ã!z}vúfÖ}ÛÀ\x000ck!
wf¶~Ã\x0019¸nùCéüF·)=|&	<S"éüéþýõ\x0005u\x001eõ`\x0008Ç¿P^±\x001beé½Íþé\x0002úáòÅ÷ó®íû¿ÁÎ£v>xõÁ¿N¿ÞÜë\x0000l¹£ïoÿñéúáýÎQÂÊ)ºD\x001ba;E£\x0004xNÃQ_\x0011ÖéOg/ÊM\x0000vÛÑ÷çÿçòôêûëw7¿/Ã½UÉñÒ.¿ñ\x001d>Mh¿_.noö,'¥Ëü¥Pr\x0010p5i1³ÄÏ¦ówöÃÑÅùÙ\x001b\x0006\x000cØÀdÆL¦)Ép%ØFó- 9zb\x0006\x0016CÙ1mîÉ\x0007&ôJ\x0016&ÛÍäÆL®©\x0008{\x0010/\x0015äèÓ$PÎöBù1o²¥­\x001bCiòÁ\x000c#Õ½¤Â\x0018*4A\x0012|A¨Pd\x001eÐjÚaIu3Å1SlaâJdò¦ôæ\x0006¦èø¢Q³³\x0013*¡r\x000b\x00148[ÂTddÉó.yßÈd·.tµÌuÓ:îvbgPÅaö¦ëb*S[©&3CQÂC\x0005\x000c·9ûÄí£ncT2-v
î\x001br%¥a\x000bÊ\x000f«*¸nªj\x0006MË\x000cfeK=AÙÎ`sf°ª²T¦ÉTenD^zÎ2ÃX©^³`*SelU.\x0005
|üy¹Nx\x0019+{­ºUÕñ§ZfÐF	ËàÂ/\x0001n
nXì½ÁVÎmñ^2(bR?.\x0003eK?\x000bXü\x0014¬îCª¬m±
\x0019nÖºÉ\x0019\x001f³­²Ü\x001d©\ïJ·µóÒd\x0015À\x001b\x001e)\x0013S¹5X]ÂÑë¨*«`¬Iì|fcK\x0001\x0014f?Ú\x0001ªÛ(ØÊ(Ø6£`$\x0006\x0002Ú)òöãøcTªÛW°Q°MF!äÒµ\x000f©LiýG ûÄQu[*[90¶Í1EÜ\x0012 +UbäÁSS÷\x0004¦*5PEØÏJ&h4¬¸	P1ö2U^mq«¢·Çrü"¯\x0000H>
×,×\x000bå*îZLzÛræëWÇÅSPFütïz-º«,ºk±è\x0018Ó0|!ÅæÁ¹\ÃÏv»z®2ê®Å¨\x0007\x001fK:\x0001P\x0019n[\x0008TÖ£`mïBwQw-F=¸æa\x0005ìí\x0014\x000b0yV¦×Õsõ´Å¨\x00070ê\x001dPì/Z¨ÀÕ\x0012·Ø¤^÷ÅUVÝµXuâ\x001cì¬[[
2Û
%\x0014Sï^íUw-V\x001dÓVeµ#.TÜYö é¥ªÌºk1ë\x0001\=ã\x0006»\x000bUÖÃºòÓ§¢åTYw-f=DWÊ´*R\x001b¤ò)\x000fqîuU\x0019v×dØa\x0006Å¢_¹\x0004*me\x0006c¯aða÷M\x001d&Ð³\x000fáþâ,¨Íbòºª2í¾Å´Ç0<#\x0015»{*©Á[½¦ÝW¦Ý7öÈ\x001dæ{Øìp\x0007ÌÝ·x_vßdÚ±à\x001d\x0006|µ3|à!¶à{ý=_+ßd®¸ú\x001cv]R*°¿\x0017>v.§ªÌo1WQ>ÇDÄ\x000bUb®êIÐ1Ue®|\x0017jJ=.ÝMMáAïªô4DªÔkÚ}e®|«\x001f\x001aªtQG*láÃT¡w¬Be¯B½JVâØ`-\x0001U\x0004ñÖQUö*4= ¬\x001c_¹l;³öN®\¶{µÊ^¦¨cÈâ^QHÆË#¾\x001fÆª÷*\x0011*{\x0015Ú¢yzxîóÕaZÆÊõ«Py¢¡)¼à<½"T\x0008C`%l\x000cPÓ¬§åT¹

æÊÁ[ü	#Ê\x0019?ßý\x0014*k\x0015\x001a¬S)rÐ#`*\x001eKY\x001eØõ£ª²V¡ÁZ9LA-±ì øVAêÿ\x0012\x001fÊÛº\x0017AÅÊXÅ\x0006cEóWÞ\x0003*K+Ëó\x0017e\x0002SwÐ#VÆ*6EBSäÔ	@W^¾±`ÀÊZï>mbe«bS,Ô\x000e¾UÆ1C)-\x0011ÚØm«be«b«­Jq \x0000_pr2Çþ	¬Ul~ãJLäd6ÚÉbOº×\x000fÕµ96\x0005CM.Ý\x0004*f¢øljä`Ý\x000fÌ±rCcS,\x0014s\x00162[PK¾\x001få\x0007\x0004YëÁt/öÊÆ&/]\x0000*®}Âëõ\x0003U/TeAc¿ç\x0014]\x001eè\Îò§\pÆÓ¦{U¥ÊX¥¶ »U9J&\x00055&æÞ}µIQHmé\x001dïñpÔÒ\x001c=Ãk
Õkz©ªí¶\x001fjÉ\x0001èyû\x00196P½\x0019\x0002©r`RË}+»pÌ'òìmµ80ºß×ËÕQÛrréa]YT\x0011ñA`¥r ªf£n®«0Û\x0007\x0006ü5ªz¡È]LØÜeu\x001c\x0012êr(^<fz}vuuvtuùæÇ³Mâà0Fz£KbÎÿûÞ¿»½¹§²ëÝP°vÒPbîgüÁ!½~j\x0011N_<;?{AÅ(§@6)7\x0010æ1an'LNNÂ\x0014V\x0018=$8N¯]mf|û?~nfKNä$ÌH>*¥ÉH>ß4qg\x0019aø9N¿û2NJuôý-fø\x001eýÛãÍÿOÝ»lÇq$	¯\x0017\x0018\x001c¿_\x000eWI\x0008E¡\x000eH°páéê
O\x0002L\x0010q¡\x0012\x0004%rÕ¯ÑÛÙL×¬ÿåìô&ý$cænæ\x0019ÌÈ\x000cª\x0016ÊV±»¥¯,ÜÍínßs¬tÄå\x000ba¯\x0012TÀîÜO\x0005´¤Y½4¹}\x0014+{³
Cgxð÷~:Â¢Þ½¿]\x001cþýtÖUDÛä*\x0005¢U``2Kâ$-/ðÄZ(GapÆVKì\x000fv\x0010æEO\x000c#îLJ¿O
-@É¿O
-b5Hþ}bhZcä ÿ>54Ö
§ß'f$+ù÷ ]_ëùL·ï°iá\x001dn?¸NoP7\x0001Ï1\x000f0BJªgs ud\x001aÆ±bí\x001d\x001cÏ^ã\x001bÕÅ y\x001a,
YÔÓ`o?à7úðob±o½üýûûF\x000bÌ·×wijÞóÅ»ûÇß÷§lÈ>{þxýðm\x000bØÒ\x0010ÁûJ9zpÐ°ÙFÓîngIÕ
Ï/ÎÎ°\x000f\x0001ìæG¯Ò¬¼ç?\üÇÞóÙÆÁ\x001dm¶ÜÁZËSXS\x0014\x001eÿÛå÷\x0008G1$ÃìÓx¸Ü\x0006Z
ÙßáÀkôYr*OyF¶dàeË½µl\x0002lgIh2O¸\x0007´<}2´ÜX\x0006Ös O\x001aóp\x000e@£ùwÈ\x0012ÁØÄß¿üö­ÑÝû¯pc®?ÏSÏ~\x0007TÀ
`\x000f\x001aöÅã|¶ýìs8'tªn-DØ¦ÿúô\x0008ú×³\x0006}ûV_½¹|ß¸G·±;[ýe9ÿ\x0006ÿi\x000b\x00116>¦Y\x000c¢L¬ØKÍy­PG/_c>M´úËéìïð~h\x001ajqe\x0011==®¬*\x001eWnÕ{z\¹3üéqeõðD¸ÐG¤ÆäÕ\x001f¤\x0016å\x001fô×VÝ\x0015Ó4\x000fJ÷-é®<ý\x0008tWØþ\x001a­\x001eñ5½Åp²\x0005·é1ß"¹\x0018r	\x0012¾Ý^åà4RZ~,\x000fãðt\x000boÓ{¾\x0015/¤<¿Î­¾)I\x0005xJûbhl§ëÐù\x000cg[pÞó\x001dp \x0010c°\x0004\x0007ª\x0001ö;>í\x000e:ß¢Ûô¢o£³9¡d¢yþ²Â:º\x0014&§ëá¤\x0017\x0018gþ5\x0013òåâñîz±Üú \x000b3íø\x0012©9D¢K\x0015\x000b\è^\x001e^¼\x0002ãölÓ}e6ÕdSOM7ÙôÓb3M6ó´Ø\Í=-¶Ðd\x000bOM­ß\x0005õÃ]x½üã\x001fHx÷a\x0007¡\x00172õ .q"îdÛÔu\x0010\x0005ÒÚøú4q¾zÑà\G4MDó$\x0011]\x0013Ñ=IÄÐD\x000cO\x0011Q¶Î¢|Q¶\x000e£|§Q¶N£|jÇÑ¶ß9¬sÒko_¶¡EÚª\x001a1}#\x0013\x001avJA/RKr\x0007ÚßÏ7+D½f¸À\x001f¬\x0019.¯®¯îo¶\x0005"\x0002NÙç¸WeWCùâj.¡½::89mDÓR4z\x0010ó\x001f¤\x001eDf{¤ÅPÝ"³8÷"û@Úèý\x001c!AÇ(sùÍ1¯\x000bÜ¶|ºÑ÷ÉLÐ$&üÿ~(ÕRO\x0003Ê¶¡ìò­#ÿñß\x0006eÞ.ìò×ÅÝ[ø\x000føÅòïóûÇë\x000f÷©V$h½ßwoø\x001f/\x0001ëYD\x00194\x0010;C\x0004\x0002á/ïh\x0010¥6U·¼\x001d\x0003s|øì9ü\x001e½8é\x0018\x001c\x0014ÂÛKÊ*ä?x¥o\x0019,	gïùý·Å²-g/ïï¾ÜÞ/¯ïaó\x001c\x000e
A
ªS¦t\x0000hqAv\x00024Þàd\x0015`\x0012ÔÞó¿\x001f®\x0018°ÔÛ÷î6|ý¼)Ô¼wó¿ÿõß\x001fn®SLDÆL¦@Lüã{Rúðõ0^§joÒ\x000e\x000c5+¦®QN¥!cÏO\x000fÿ3©ñ¢ªö÷\x000e_\x001c\x001fm\x000eSª·ï~}ô7ÍÙ¿>.¯ç4Q¬\x0003\x000c÷Þ¥!ÐÚãäç\§pii:Whùz½\x0011ìlï¯\x0017§G³Wí´Ér ²ÌåòS$y?@"SÈP£É~Èjô"ÃÁ\x0013.á&F"£©@¦C\x001cMµdÁ¤ÑIf:\x0004²»Ì6\x001f³\x001a²\x001f-}È29¶ç,ÿ-I§eã9SãÉ~Hµô"Ó9ÿ¾fþÈòH=üã/@.\x0007ª\x0005¹(NãFO¿O\Ô\x0004\!
÷\x001a\x0007öC\x0006¨\x0017ÍEh¤3ÒÄD ó¹µ\x0006¿¥\x0019-2?Y}ÌbjÉE4QâÇ\x000cfS£ð8´´ttÀ9\x000b©¾Ð\x0014¡¸B\x001b/5ªïªFó+U\x001bÓJòDV4­\x0019¨Ï®þOW$ÇÊÞy}ÿøqSÂ½óí\x000c1·âÞX¬øO\x0017\x0001\x001bð2\x001e\x000eëÞ¨:.ö^\åAÜï@üº|ô\x001b\x001eÐÇä½!â_î¯·\x0013ú_N ôZå`JÈ<òÇ(+7ß\x000btï/'G}øÚÏh\x00052õ£\x0002\x0003a¦Å\x0014©I6?òÊ\x0004µñ\x0003×\x0002¶_Ó\x001a\x0001Üµ\x0002´rä§éjà¦*9ïî»pßßoä;¿\æ\x0011¢7Ã¨Ô\x0007MÙ\x0016(ÀÕp-ÜG¾ìüäâôäU\x0007Ó¯¿~ÿUÆ¡{±ß N\x001f·Éª*¶Ñô¹\x0010¾#¼îô\x001dmÁ¼8½\x0002á^t¦EÓ\x0013ÃX¾ØÏ]\x0000Ãä®yÀ0~(F¶-zb!\x001dm±©µÊ\x00186¯ÁÆ²m=X\x001cÙèÉá\x0014\x001fÞ`b®%\x0003\x000eWÄ¡ü`yä÷¹/G®{H\x001c
3Ãiæ°f \x0007Xî\x000bâÈ3\x0004\x0010[o\x0011$\x0014´-÷\x001a\x0010z{û8lêaµ7: Þõ
ÎÚ\x001c\x0008BKúJ$_\x0013\x0008¸¥WüiäÐ\x0016õ¿2`z\x0007R Êåf{ä(_&­ú\x001d\x0006ÛÂúß È\x0018\x0002\x0010§I\x0000\x0008MªLÍ)C9píUÿ;\x0013R±\x0002bHKç"Ø\x001b¤Om´r \x0006>Xªÿ\x0001\x0007×eqx,áÓ\x0004â)<`×lý\x001a\x0010û,Uìyc0ý\x000fÇ=Átc¤aSÆË¡7\x0006ý;Õû Ç£e\x0006\x0001uâÈd¡)Â\x0000b\x0007_\x0019´uTï\x0013 "_]\]Ã\x001c9Æ¦®û2îáF~¸ÚXWö°÷ÓüëõÝ6S\x001dìK\x00184ÕS«·Â6_Î³p\x000bÏª¼\x0006,áÙ£W]¦zk½®¬\x0017ñi¢\x0008ÂïK¹h\x001a B\x000fã\ÊeF~8þQ¾?þ±ààÛÉrþe§\x0001ìB¥ôoÌY]x\x0007ÊË&\x0015\x0016¶'¯Î\x000fsEÒÞÉéì|q©no/¿?4¾æëùU©\x0002ÐùõÝv2¥Ó´táÊ£\x001d±b1/\x0017[¾ÃëãÙA)\x0002ÎÙÑ«.¶o÷÷»uGÛ¸Óäó-Li@ÖFpÌM\x0001# óhN#m\x001bx´|;;ßÍB·û²¸\x0015´òBå\x0014Îä%¦bä\x0008lmöFQ¹\8zïpQc×mRÌt0Jv{£ø@\x000e§rÜ\x000bbOD(ºý×±dã·¿Xd
4¦OärG)%ä	üDcX²\x0001Ü\x0005\x001eñHbqyü  ÐrC\x0014KÐQÊêÊ¾,ASL9§:ã7r¿Q\x001ep;\x0010\x000còÞ0 õ"ß#Z_\x00070"OpN÷(\x000c!£¼7LL»ÞQ0p»c>0Îû"\x0011wº,ïì}zÁ2\x000f\x0019&X¦åôj1üô²qÞ\x001f&\x0007\x0012LÌ³Oñ*YÖ0ºmôÔÁÞÿ.±)¨@áçV\x0017¼LE2é»\x000f!+½7\x000cvæÒ]yê\x000e\x001c\x0019©ExØTïÍb\x0015¿\x0003¨|)ëT\x0011ïð»T\x0016»öÉ­Âtd²Ý%VEåá*}þu®Z&§\x0018Æ²á ÄpÇþCÿ7R¤M\x0011IÍØ<Â
M\x0007Ã*O\x00110äCô\x000cÊ#Ã\x0001ù1°>N\x000e)+l{ÃD
(§óþ³ô2\x0015\x0018\x001fßl¶Òû&G\x000e
Î>JTúLnµ#\x000e0íè\x0003\x001daY0>%\x000b\x000fÇ5\x0012©Ë­û\x0014çß\x001aþ\x0001Oõb¾¼\x0002çàËV·Ê\x0006ÁqäVqÀFsä^ÄMF'8U/f§\x0007à\x001bwùU
2jµª#ÃQYñ\x0018ë5E
è­RFëMß­¬å+ô$\x000b\x0016.Xª Ó~$¸üÞ9Ç¦NØôÖµÌõÞ`Z³\x0012ÀéØ¹n\x0000<gÍÎó@\x001dYN5W~L\x000fv3E[´×9þ\x0004Þ»
ä½©ºé}­"[³û
ÍáHÉ¬ÆáØçÝ?Ê\x0004¿\x0017q4YÛ~íMÓ²Qi\x0014ÃD²È\x0007-nt|z ýöþùåíZ\x0003³¦w_\x0016_¶P¥¥\x001a&\x0007T\x000cÙ Q*:þ8\x0014i³uò\x001a£\x001eç»ZÚ¢\x000fÅb\x000e¾8\x001c>ÒEÁÒÀ/Ì>êM°?ÑZtc'Ñ¹¹\x0016\x000c.ÞÊÁg§ÈTpì7?9}Öâ
»@¹s|ÊDÁQ _\x0012´zã!ï\x000f´æÑ÷\x00006¹Ä0#\x0008!ópíÒÆn¶··\x0003}|÷îî²y¬\x001f9Tö|±ü°X^ï\x0008\x0005Z}í¾åÅ¡mý\s¨/8PöüðôÅáéQW ¬Áµê:®àr>\x0015l§<¤ËEW\x0018]¤¨úÁ\x001cÀEG¼\x000b4§#.¶Æ%b9\x001c-/z ë¸¼âj@;\x0010ð±A?Òk\x001aj\x0000\x0017ÝÀJy\x0005r\x0018\x000c¾4å\x00159'eÖç\x0001\d7Ôqa?#'\x000f5ùXëÃò\x0012q4\x0017Y
\¢\x0015\x0006-ÇRÓÊÕ\x0008X¡;Âu\6/³¡|<©÷Èï2¯v9Ó\x0000®\x0012Ø©T\x0014qßä«¦ó\x0015}I¾êaòº¶_ï®¿¯ë¯G`ú¾ÍÙQ\x000b¸%/µÙÛ	44Qc6öG\x000bùÏÝ\x001c
}µÃú\x0014ÑÑ8"ßìg?=Ð\x001a7°gùQ}öÄh¨§\x001e\x00186ÿP\x001càüQ½qÐyÉ\x0016p\x0008ÿ£ZêÉÑPG»9¢zTãÔ}\x000e\x0006êd\x001e'úé!@nÄ­ZÓwÉj\x001a8T»¸ì~\x001cðì\x00079¤âÄ r:`l¸4=)\x001aJ¯ÇWá\x0012?4¦9\x001a\x001aTà¯¢ÚÕ5\x001c
%·CZj$¸´b7>S*ÃÐSZ\x001c´~ pUµ§ëbÊñ|:Ä:¶'\x0006{c=åá©\x0008L\x0006\x001aØä\x0011eQbåAÅ´}A\x0014\x0005Õðì+âÈK\x0010Ã©:¸\x0010_¯×eÀ¸øõq»ñ×5ß\x0018l\x001bÊãüÐìQ¿_!³¿]tÚî
¶nïsÖó{\x001c\x0011À\x0012\x000eÛU^lV$}yÚÊµ\x000f§Á\x001e!4ü\x000cÇvÙ`-N[ÇîÆ	AsåDÀÀ,7J(«FI§­j{HG)®eÆ]RxJ§R0\x001b/ÔV_[^üá0gÃéþñf~·Ûvú\x000czòë\x0018«Ët:¹8½Úf=5Ø~ð²z²)±r\x0000
\x0007iq\x0013×N\x0007°î\x0007¦/J+ïÈÝ2è¸¸Ú);\x0001\ãUÁé4\x0017\\x001b£ØEe\x0017Bvy65l?8\x0011=Ù,ÕÖJÓ¼v\x001d½.»üÔtï/ùíøÑd?¸¹ÿÏçËÜÙ©5²FÅË¼¤O\x0001&\x000f'Jýã7½Ø;8>9GÂç³SìÃÜ\x0005ÖÒóýÁp÷UÌl¶:3Ô\x0006\x0006ýñV³µ\x000cûþl&/@6T"¤jK±ULå\x0003cÙZïQ¶à(Zc±Ýyêr¡¦*\x0015lØdèV²µ\x001e§þl>ÒM°ðLR\x0004.Ã¢\x0010­eWÈ-÷ì!\x001bö\x0019î\x000e"å\x001bü¦ç³\x0012­e¡÷FX0\x001b±RÍí\x001aAn|ÚëØÖ¬öþrüÎÜèÑ\x0002¹Eîª
^¿§k¶|É\x0015/\x0007.\x0003×·	­ãË°14Q	×¶ï+>«J*\x0017áLÉ\x0004\x0017\x0018ÎÈM\x0006d%\x001cü#ä«{átV#\x0002;É|ÓÕ¯Ö\x00139.%ª³©T0G~£ÏÝ\x0000g\x000cwìø	î» \x0006Ü\x0008¯}î¶µÂ«4K\x0014\x0005g©Ó\x000b.ë¨a5\x001c>öCî\x0003<ª:&±©8\x0017á\x001cû,Añ\x000fW\x001a(?ä>¸ò:ÀÿU6â\x0000.\x0018zU}Br8R~Àó
}~\x001epà#=\x000fFpÚû0þÌi\x001c>äÌEG®Å
iôYô|\x001füÆàV%\x001c7]æ,üÒ,\x0001øßjvÛ"-ç]\x0018jcÞÝ>.­^3~\x000füÏ×Åÿup¿x\n­\x0001ÃÍQ6ÄËlûbs\x0019UbæÓvpzø\x0006~O\x000e/Nw#­LË¾HNc

×pomq¯ûá\x001dÝÍ#üwçî7:Ì¹_~ØáS\x0014\x0007K®²Ìk©Ñ©\x0012%\x001fé~<òÔPpú¢Ëci\x0010­»É="UJ{@«tÐ\x0012¥3Ñÿ¨¾jÖ]ãÝDVRô\x0012\x001cOKb¨äFeWn´'Ñº?¼È}:Ö8÷V\ú[É~4*v\x0002½ÿåû¿Úpþ÷¿þûç?þÏçë/ómõp\x0016W$\x0006I¡;EÑUaVh7\x001e¥½O^\x001fÏºªâ\x001aXí³Ô\x001bËr¹R~Ô¦^%¶ÍFYõ§j½~Té©±²4yJ2Zc,yZ±1ÒÒ\x001b«eêWpaQ(á)ï(¢Ç^¯qÈG\x0014\x001fw\x001f8[\x000f{/ßíè\x0016C\x0015e©ÍÐûÜ¨¥\x001cÖq×Øð\x0005Ïöþ:;ý©»U¬AÔ<V=\x000c\x0017%x¬07¬4¹\x0015Ôn\x0008[Ô\x00105UTO¢°O"Â\x0002\x0013
ÛY»jÜ\x0010T¬\x0000jñ~@ \x0001HBð¬hÕ±%]¬£aº@6Ý²ÔÞM«@ñYQ¬3×Z*JM
/¼8ÈrüÎzn\x0017õ\x0003¾ÚÓß~û}£5ðr~½+),7°b7¾ Èyãú ëËÙQw\x0004³Á´^4µÉÆ&Ã'#NäÄa)µéxìú"­(=Äë×b±\x0008<\x001do¥ôH1­×Jõ`\x00025iI$\x0013Jßêæ\x0017¥?ÓºáÔGNëK±ÅêV«WÎdZ¯ê#§R­ÆÓ* ØxÚ\x0010;­bZ¯êÁd\x001c9\x0006¼ó\x001ckFMÀ%6\x000cbúôýÛ¯\x000f_6^»×÷\x000f_vLPiùAÊ4\x001c\x001bJÓ\x001fØnr]\x0005[¯OÎÎ{\x0010­¦\x001eD±\x0002b	,O`G¥Ë-èÉ³nïæ	\x001cÚK#eèÑ
!LÞH	­§¢z\x0010Y*OÅlfíDU²w\x001eþDí7®'R z-@ÒûQ´e¥ì¨¯ëÄ-\x0015H±8O`5\x0015!qû]=~(÷ëA¤yô\x000c>'®¿(ßMêqBj`û"Ù"$Y	S\x001e81ê¶Î\x001a"ZÚß\x0012G¦ð,$áF!fÊþHh-ñó\x0013a,·5E~JÌ(
PZ*+¤ A¶ðäÛôâ)F!tXK=¸±²\x0006ÉÐE@\x0012¥ÄVq\À\x00065àÃÉ«»Kg6x¯üÏV³\x001b\x0007.%F¹ñ_(ÁY\x000f¿±´6ÏNß
Ó|hûÀ(Y*h@8¦ÙEÉ\x0011J·¡¦7LÛ³Ý
c]rfS9å\x0008ÒÜ|ãÛèôi´}`p\x001a\x0018Yýs
8Ç\PE\x0002YÚ\x000eön\x0016pª§¯D#¹°N¡T¯»MnQ_¦
Û\x000b&ñÐ:¦ÐH	|dÄ\x0013Óvôw³xM	uø[CÁ5eY,zS³A_¦\x0019Ý\x0003\x0005¯\x000fû?`NS\x001aX\x0005_Þu=âÀ´ã
»a¤/rÁ\x001e;ÊÁIVÃÎnÈÁõiöúÐX_Ü\x000bo¸cS;ÉUzSE\_µÀÇn\x001a2MÓe9ìÉSµºL#dÓ,"èE\x0013"M^I\x00152W¢(`3¦eö¡ñÙFFÙ sJÙQÍÇfS\+½[Î)d_¦óåü+üëRzïüqyy¿õéö¾TµR/W÷v}Àùéì
üÏÛ;¿8}~²\x0011J¾ýíÝ¯aR\x001fi!³Y\x001f?{·\\}\x0004$Oû
ä³ã\x0005vÍ<äÍº\x0012]\x001aª.#V\x0005âB4ñ¦ª«?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9üçVBÄ®y\x0003Rñ@
x¾¨ËäyPÂFóT\x0007\x0013çjZ©9ÆeÊ­\x001eï²Nj\x001e\x0013Î1më¤ùÝ\x0000ë¤H=\x0010.\x001dûë`CÍd"\x0005\x0016&\x001eXc°\x0002Îñ¬ÍÚw3<f	Ú\x0002NÛÈLO	<×ÂJ¹)Õüµ®¡=\x000e®³ oç×L¦ëÜY÷5\x001fjE\x0015»	+ð\x0012¶\x0007)áçJ\x0008Ãáò}'Z¦n¬»½)H¥
l*\x0012¸:©'M+*\x001fñBðD\x0017cÍXkS\x000bO\x000e\x00076ðÀS q\x000b5\x0010ÆPgBõÕzJWÚT$á¸'
G1ù¬0\x0019ui$\x001c¤ÖFoFà¶i¾PDÑ\x000c5bÄ\x001f@tóÆúõÛ]­Ë·\x0017\x001f?îV\x0014\x0007×JhT¤¨²¤¨¿»FÇçGÇÇ;Ä\x0007Le+µ0\x0019É2ì\x0011sÕ9ðcq\x00131×]\x0005V°òùZÀàÑ\Àr\x0006Ý:ÁTnd^Ö$ªÏÞêNQ(d~T¹ÔËËË5½\x0012;xs>ÍIaYf.l¦T¯tqkUïËÅÉÉÎÞ§EêæÝ\x0014Ö'#Íìp(I£ÒÒ\x0018iXSr¶×\x0014¼«·¿ýùÇ0¿\x0003ôãWÛO¢\x00118Å\x0006:yM\x0013§·l®À\x001d\x001eEøûããÓ\x001d\x000f¼5\x0000ep¿\x001f\x0000eeï\x00050\x0001ÞÙ¬\x000f\x0012<æ?_TÒ\x0000
>%Zïýóáâ"±\x0004¬$¥$¯Ö\x000024\x0000,ßýú«¾¬·ÀÓÛ¿þk»1ÆªZ"\x0013Á\x001aó¨éhÊ£J\x0002Àß±)xÂ_vÀwúóË\x0006øWþù\x001f\x001f¾^¤
ÿ-ük\x001d9xö×}\æðv\x001eø\x001dR¬6Êq©\x0017Ññ,ò ÇY\x0007Ï\x000e\x00179\x0015<\x0001\x001d÷f<lç Y\x0002\x001f(ÿê'Ý*lÅWûÀs(øÝW^+'
l®Ê
w³/ß³t¹ñ\x001d¾lyµ\x000eðüx\x0008°\x000e3ANvÐ	Ç\x0013Þ\x0015¼Ëh<¢p,ôm¼\x001d\x000fô¶áa\x0017Lðíx.pËQ`²ó«Qð,\x000bãÜxd²
\x000eýÎØñe1[\x0018èÌ\x001aÁñgx\x0018±GëÄ\x001eÎ¬L1ÙaS
4É\x0002Ìå1¶éÑCÉí\x000fs0²çãZ®Ï\x0003>G{ÏÅX^\x0004ÖïÁ¨¬'©4óIC\x0007#p%Ü\x000fåØ\x0006³\x000f¸p¡\x0003ND
\x0019YÑT=\x0008|ÞÇÚÙµíx
µb5=?Yo×\x0004¿å+ShÚù$uT¦û6'=O[æ3{°{
ß
éG+õ\x0011\x0017-ßh½Qo·_á\x000f\¬þ\x0014\x0017\x001f\x0007î"Ó\x001d_Ý^|98^¾¹¾Ú%c\x0006\x000bQ9\x0016ø²Üà%)\x0001ã «±+÷øôüè\x0005¼i\x001eîR³\x001aàeo²\x0011/ÍÞÊÞVEA\x001f7x]²nU+|?]vöé´áB
­\x00027xÁá\x000býtï>å·÷Ã¸ñ0#øì¯ÿ\x000fÞ©×;4!(ª×ÑòÔn-)jdMÜrã¾8xv\x000eÔ³\x001d¹Ê5\x0019|R£ÚÉ82jQÌÍR\x0015ªä\¹z[º·\x0001í<\x0015Ê¤uä$%ñ\x0007rö¢ÉT"ÛÑ4'áòIÍzbÊ
^5Sµáw²á%&C3rX°Øt eU¯\x000cuµ£\x00035~G´°á<»ô£
Üs\x0019³*°\x000e-¼Ï\x0005\x0017@D?fCØÆnilº7g©G\x0004Ø¸y	ìÛ¶ªûØ>zùë\x001f\x0017Ã`ê×\x0015üS ëþý?\x000eo¯¯>¯\x000eÎ/w\x0004»tÀ¹¥ùê÷\x0001\x001c&´nþ¨«òØÅ«Ãó,=vpx~vúüðàüdG´k@H¡Õ\x001eBÁ¾\x0013\x000e\x000fÈ#ÃM¬fg Rµ\x0003\x0011>,½ËP;>÷ÚÃ9¡RZ\x0013ëA«3\x0010s\x001dk\x0017"\x0017¯\x001b¯4\x001e[ÍJ|Á«¸\x001fÄ\ÆÔõ¡-MfDò8ùCG&´û!äÂÎ®UäH ñàFþÐTÀmà\x001f÷ó¡¹À²±Rº ¸lÎ*u\x0004NÍ~Î\x000b:þÐTrØÉH2£Ø®-	ÑSÏ×>}?"1t!º¬-nläª\x000ft\x001dèLûz¤À\x000cDj8í<ÔyD¶±ðts2\ì\x0004fg?_K\x0013{\x0018%&À*½Ú\x0015,«Ý\x00198,¥Ï8FGå\x000f°\x001d\x0003}ë¨¹$CV3Iú\x0019±öL÷mÇb8JY"«½ZïKÙÞÏá¸}×:
ùl° \x000cxÑ~Öì\x0010§öÙÆ¢´ù¦ÆâEKin.\x0005ÀÖÈý z\x0014aíCÄÁ\x0018y3j\x001c¸\x000fÓ\x0019ÚÏAÕ\x000eÓõ¡qVF\x0002
Í­!\x0007Sààýø\x0012X)bº¾sÒüåbÙh¨]7\x0012\x0014TrOÖk­z\x0018C N(ØRákùfi÷³\x00159[ÓA¨+Å8_9éXFÖÃwû\x0011¹ª¼\x0007ÑÁP=Ò2OÎÃ1ÝÏaÁ(í;,ªøµi@k¤\x0011\x001c¸\x00033c]ð7\x0011ßXvñ_u\x0003¢´í4ÿ2F\x001cÅÛwb´b3í4\x000f\x0011"DVQ\x000cv?G³]\x001eæY\x0010Àh\x000b£ÚÏ=­äÏ¯/¾$\x0007\x001cÿÞåGÎÛ\x001bAºl\x0001EÈÁ5ÑÏ@½\x0010âø6üäqËÛëT\x0003¶#ü¤´À
G,\x0002KJ^4;X±tº¬çj\x000c¦Æ-RôiG-ßo\x001f/®¾|\x001bVS}Úßo~»]}¼¸ÄQï¯>\x001e<_}¼ÙÞX\I\x000bWzÖËôÞkún=ýß\x0017ÿq~x|t\x0003\x0001\x001e\x001f<?<~¹£íkÍÊ¯ÖNÖ\x0010x4¥ÅMj	V2¬\x001a)þï-\x000fÞÕ<Ùâp\x0015¥-
ÆûýÁâ#É÷¯¬çRY¬ZÉz¤iÀA»;²¯U¦ù®ªË{FmX\x001aÞ\x000c\C\x001c\x000coÍß<Z¬lM?ziÁI§ñ×\x000eëùs~78V
¾]½iW×\x001f?E]WµÝ;±ÄyË]CÀ¨dDÄ8üwêÂ.\x001eWòfùvùåæz\x0017F©î08Eü-\x0006)¨H=©PõÏ\x001cß?5eã¡V\x0003_¤T»\x001fR¥OJ#sÄÉÔã\x0006\x0016-ô\x0014\x000c\x001b\x0005¿îÐÿwÍÇÈÔnÓjpìuÒr`ÆÃñJ\x0017¢Í¡£êÞ\x001c\x001c_¶Ic)§ñ\x0001\x0015]i®þÜªÓA½ë0B¤ÜÀ­^JòâMjªØÅ\x0004«\x000fo¿~z;8²ÏÁ¢l/s\x0007«D³\x0017B/a½æ8±äús0\x001dÛË\x001a\x0006x®\x001bøNxÎK}§?<¨å\x001fn¿]·© \x0002³ÕºöÅíX\x0019Æ6ï\x001a­«µ¦\x0008\x0014ö¥\x001c5¼{ÈdÃoÞu)^ÿ\x001bÖÅ§¡Í;ë®Ù6z§²©ÈÉL¸ùù\x0015á÷Äfå]\x001f¢\x0019nÃÏ\x000c\x0017ì\x0003î*pTH\x0012¥àe«Oo/\x001aÜ4>¶£¦)«\x0015EtÜaªòêN¶\x0000×O\x0010\x001dË¦éRÄà,Õ\x001dÀºQh\x0002~SÝíD\x0008wûõÏÏ\x001f.\x0006w0yXj¨QO\x0002ÓgW·ï·¿þ¬V2·I©à|ÀÕ y²ôcs²X`úìôüé2õ?¾þòîÝÀ:ÁËtñöúbuyð÷«Û¯÷\x0014-Q¯¤\x0000¿ßpI OBÙªì\x000c\x001e¤'ðÚ;9øûéù«IHÙf7 Ãl×HÐ8L§ênà\x001e¢lÈ'\x0013é\x0018\x0003)ôê\x0002æ9ÁçBéx÷UÌ«\x0007)÷\x0016¤ÈÃBbP\x001c¶v\x001cö0JTÆµ\x0007)×8´­R U¤¤¼£V-¸ªÊÐ\x001e¢¬\x0013ÖFDo\x00060\x0002¬QíÂº\x0019¤*¨éAÊU\x0016
HÁgû©\x0003V0ÒNr\>\x000b\x0017Ð\¢,\x0019Öf\x0001$\x0005îb]!¯¸CEÎ_¤ü®iY¤Hzs°Jä\x0013\x0003¶/ð*U
0\x001dHüÈiÙK²Ó:¢koÉrö .jëa¢\x0007O\x001b¦O'\x0003½\x0003;d&;´ÄZ4Çc£òÃpTgà\x0005dæ^(!\x0007bCÃ¶¹ò\x0005q\x0008¥"9ú*}\x0015Ì\x000cvsñù0|\x001a
G{Ý7¢V¢RhXW2å^\x0013'"9{&ÊZÕk0ÞëÞ¹k°»S\x0010')v\x000c¼,16Á2&ª\x0014¼\x0013ìî ¿	`\x000cM+ËDp\x0012k(+¶m Út°õá\x00162Ë)P 3\x001cCåõ\x0005®èØ\x000c&²¤É~´ )¡\x001c	 X\x0000Ñ)Å\x001dW1EmD¸ÿcãª)Ìºç$k½SøKU¯¢eu¡Ý\x001d¤3	äq\x0011-b[N\x000eoÁïS\x00018ü\x0017gP/	í[W
' ÝÞs\x001fv¬@\x0006fc¶Ý02f4xO³ø¤£\x0005¿*hÎÌÞk&{æ\x000fj$N|Ih°×"­g\x0015~Ø½³WÍ£Ô`úÑ¦¥áÂt-8¯\x000evMÖ1ÝýV{+~wÔ»V«9¼.)O&W¹ÙÔôA¾\x00066O¨ôcý¬~vu{³Ü\x001eç¨Kße
Ì?]\x0016»½òZËÑ5;?xvzþr±Czä÷åç/Ã>ªÜ.¯o.V×¸X>/oÿØõ\x001d-×d)\x0015xÖ¤õ\\x0008cl%\x001aúóÅÙË£Ã3\ªgÏ\x0017çÿg+ü%ê«_ª¬É=¹ä|n4Ä\x0018<\x000bÅh\x000cCTAàC\x0007:+\x0001|?u\x0000¾ÏÎ¢ïó§þ¿òO\x0017Ú	Úsëßà\x0010ÓO«Ëëg\x0017×Ë×«]s\x0006´ç\x0002z£Ô]ÒéÎÙ\x0019QÕ\x0000¢çýÓáÉÙÑÁ³£³Å£Ãí
ø\x0005N
áÔ\x000f\x0006§pº
N\x0014u50,Ï Ye\x0017àÌL833?ØÊÙ!móÞsT Ö@VgV°r\x000cÏÐF87sÕq\x0012Y\x0004Kw=¼²8ä7î<8?óm+\x0007\x001bÍ¯\x0017.UiøAªeÉ\x0016l¡
ð¤Ì £jb/KÀ\x0003þ\x000b¡68)*3'Úèà[ê5\nßNPAÏ\7ùóÍêº¶Âø\x001bMÖ³\x0008¡*¼D)~"¼\x0013Wk=\x0014)4S\x001d\x000c\x000eÒL>\x001bÏ\x0006wô°VáíZÅ
BÙJ\x0008Ö÷¥Ï¬Y\x001dDrY\x0017ìAß÷¡ý\x001cÄFÛYÎýtûz\x0005îçåê`qûæ#üãö\x00185üñ½B¯\x0018ãÔAÓ»Êw??:\x0004\x001fôäð`qþø\x0018þñ~B¡øô£\x001dÑÄ@\x001a\x0003:ÂµAñfaY]EjD_?#6É§\x001f\x001dURÔ\x0004\x0004EQKînv¸\x0011ã³éG\x0007£WT\x0004\x0007ÿ@
µA(ÍM\x0001u¹f+ão¾U_Â¢ÇË\x0017Ë×\x001fá\x0015´#Æª0¸D#HlÒ®ÆÃáY^^¹z¢ÔâàÅâÑn
Á5G)Ä\x0006Â¡qÊÙqòRó\x0018	_GÚ@°Ï\x0019ÿ\x0008")Q\x0013ê¸`ÌË²$¾V@ryóëå·_S¡¯À¡î\x000f\x001fþíêòfuyJ;\x0006¤GáY?Ø¢h6ÿZÒq±ÿíôäåáÉ)ª<ngyýívõA\x000c¶É:°P\x0007ÇË¯Ë\x001d¶\x0014{24½à­áÁÒ[zÁ«ñX\x0011Â\x001d\x001c/^-¶ÛÓ5\x001a7ªµ±It6LfÓ\x0003Í%\x0005ëYÝE}lëòÒF8%hNÂDb\x001eäà\x0000µÝR¬Ý\x0000'Ó\x0008ßü³N:¬ÐLt\x0012G¨\x000cIR\x000cDém#\x0010'À½×þòÃõ07U3\x001fW\x0007ÿ¸½ZÝü¹#³½Cþ¦¨ÝÉ!zÃË\x0016Ìht\x0006~ã\x001fç§/ÿm+Z}Qâr\x0010$x´¼½ùð×í\x000c}$@BßÛØ\x0016<­~Ý=Z¿üépG,mõæííç?ÇÂVÜ¥p³¼|¿#tå8¦ú\©`ÝVkiª\x000c~YÜ¡ðrqòt
Z\x000e\x001fýh9¶ôC¢å=õC¢å¨Ôöõí·h>\x000fûV+Ußã«O¯×ow4ê(]º5:\x000fY§ÙYE½¿àÂ
ëÍ²¾Ç§Ï\x001e-ÎìèÓYóqÛS3Ô$¡±ÜcÌoMp±·Ê\x000e·ð¡îsÐ=ë\x00170âø¼á\x000cÕÜeE\x0018Ï\x0017´ñ%ß ýh\x0005T8ÝÁÒ\x0002Jª\x0014tsÈ°[-N?\x0001Q®\x0000{àóÍ`\x0005UpÃ\x0003Eû\x001exÁ¤\x001fÍ.\x0015¦f@ý\x00160Ðx?|@íc\x0007Ê£`Âæ\x000cæ)|&> \x0013"\x0004*\x0002'>Ë
ðÆlñ+'ñ½ûãËÇ÷è[\x001cÍ~\x000cZívh\x001bíÉ52Â\x0007.
ð½9\x0006^Á¸mÙ]¬]<Òø&$ð²iÊ\x0010<lE\x0011\x0000×»H&Öúï\x001dD\x0012d\x000bR4Ø(i¨ÌØò|j ÚRâ1H#n$¢\x0002
%=%UÖHÆm©Lt7i|/\x0011ÏÅN½&ÙÈb1\x0013ùû( Qh"r,Õ£Je\x000eúÔEZÕõOD\x0002G\x0001þÐ²H
\x001fù³i\x0019P¯\x0019á4Ýö\x0012$U
2¥d\x0012<ÎjAöAÈÇ­ôÏ£øM\x0007Qøíòóa	øåÅåÍÿµ¸}ûåæârG\x0018	|	Ò©\x0012Jó\x0014\x0018¸	9d+Kþbq\x0004O´ÅùÓó\x0017/N¦àdÿÁÉ>þ\x000fýúïó5¾ýü\x00063Ì( ö0ý(ùËÁãåõ§ímã*bº0àMÓ\x0017I[.²V~Ë\x0011{qðxqölGÓøûO¿XýKÕXMcO£\x0018p:Í·]ÇMke© Õ¢0¥qu!f_ÏF_	¼Ô³ØÓx\x0006TóÏ]o@ÊM?(éïþqûöÓ0\wuûñêöõ\x0008¦ÄüÚ°\x0018Þ9\x000e&Y\x000b©ª©ìñéùñéù£\x001dñË\x0001\x0004\x0015¦~\x0007Õ·_Íå
\x000bð°?ýX[ðWKä¹G0AhsGc]`TK 7\x0004\x0018òñ«åÕ\x0002Ñv\x000b&0L\x0012#ùg+0å\x0015+À{ÉÝ\x000fÚ\x0005ºiÐ¿!\x0000S&$ÿl\x0003T\x0011å:iX0æ`Ã´ü0[\á)ï®ÿ\x0016\x001d«yVÛíÁã«ß\x0012ÄÇ«\x001d=´Fx\x001eÝs&Hj"\x0004AÞð\x0014«4h`ÛùÁãÓ¤ß9>ÝÑåüõ£]þö\x00157\x001fh=°¸yªäÛëååöN7eÁRä<ôÓ©\x0019\x0001ûHÂ®\x001fy~åÁOÎÏ\x0016'Û\x001bÝÖhXß~´¡IVÈ\x00034ð	ÍjVÞ8¨]h¨ú~4¡à©z\x0000ZÑM\x0005ç!\x0014ÍdÕ»jïo?ý¾Ô ªb\x0010ëµ\x000eN®®·³¡1)ºú:Ò²½_\x000f¿S£ñ0,\x001bÄ\x0002®Ó³íx×ï.^/Þá³«Ëåû\x001dBõ"½»²,·Å¹iÿkà!ë|Uóùìôäåâé\x000emú\}¾x3ZSy\x0005^Ï;^4iEy´\x00139cl<Í2Ñ"V³LÖks
~Ïû\x0000i#(ý# m\x0004£¿\x001bÒçß~õ«7þ;øS¬>_mß;\x0006¯^åF\\x0017ÀSäFÜz$à1\x001c=?Ý¾wn.à¡\x0016Ým««Ûkøkûå¢±f\x0006n\x001aEÍ\x0018ð\x0014e
\x0004/ª\x0014þÙáËÓó3øk+þâ¯Þ½­×áùò\x000bÜWëë-#§N\x0015y{åÝ\x001dM\x0017È²ã\x000cP²µù~(êýûV0T\x0007ýýêëÅ¤6>Räßbæ\x001aéDPõLä¿¾:Úó²Ëøñ\x0017²ò¤<ûdyý\x001aÎÊ\x001bJxÞ\x0019:ÆÁ5ÀctEzx²8{\x0004Gd
ýù59|øú_\x000e±¼ýåÏ(\x0007'äxRTz«RT[î½\x0001\x001fãàÞn\x0014'Ü\x001f\x001cý°ò\x001fýR«ûñÚ~^ÁßFPjp*iîMðâ¢z£6
\x001f<ÙpÁ-ª%ü\x000fwQÖ\x0003\x000c¿\x000fÊõêý·[]U°)Õ#»æ\x0006ï©©&rã\x0016ØtÊTX¥ª¶ÓcxVsýÈ	0|h§ÒÀrär
\x0001v*f¼ã	,®ò ZiÐ3t×FE°$9}\x000eöÌp%Ñ¥Ø(¸90°®ÎL_\x001alÉÃ\x001bdéô8rhR·R#Íå»Kÿ»M\x001e¯C\x0017~<\x0002]Í:ØóÂA\TdY| eáH\x000fw\x000c¼_`Î67áwù±ê\x0005~¶ü¸¼ÝñVW(=#\x001dE8\x0005MÆsÆ²i@ë¸8^À\x001ds?DÛ~Ü ¬å×\x001bøÓ<åKq³¶ÓU~ï>÷ê÷_Y	Ç&\x0003æõìêöëî±º)ÍHº½R<¨_à~£\x001aîìôüU*ýÚº\x0016ï¯ÞÛa\x0017Ì\x0019FÎþú¯/«ë¯W\x0017×Ûw\x0006vÎFzaM\x001c5@«XÞ?Õ{û\x0005\x00185\x000c,Á\x00069<{uzt¶ê×_?ª?k;^ØËë\x001dñ.øÓX\x0002Õ	ãÉÚ#\x0007ÀMt\x001bnbzX/ÀWÛ"vu¿
üÆ .íïW_V?\x001c\x001c/?ÃyÞU·ç\x0000Ô,P7;K¡w¨%z,þýôÅáó\x000e\x0017Ïá3î>\x0015L5ÄTíà¾q»}ÀÒR¼\x0008v\x001fzH©;\x00163\x0006¾Q±¾Æ\x000fhÁeÝÂªHO3¦\x0019bÅ4$g\x0007(Iz·XU]ôõHH¯\x0019Ó\x000e1mÇjzeÓé£o®¼dÊzÄm/¥\x001bRºvJtª¡Æ>Íï!ö\x0015pXü>\x0016Ó\x000f1}ÇbÈ\x0015óp[³jÒ¬ó¿\x0007Ä0D\x000c=ßÛ
|oÁv\x0012^ùô\x0015j¬Ü§\x00193\x000e1c\x0007¦\x0014l<¼n²\x0007\x0005 ,\x001dêôH·|+¦¬
{e·^ñ\x0017w>`EtâÔ±HeÎ9+Ë.;L»5ã÷àºP
K\x0002:QÅï9+Û.;;ê\x001cçÎu8LK`x=åX-P3geÜeu\x0007÷æÎûÓ\x0006ÿ§²
aLÏ¤²²í²Ã¸ká©ÿ	Ë\x000ci\x0002\x001c{jáÑÞ	;4sVÖ]vw\x000cãä«Ò)Cõ0ApýWûøäm\x001dÆ]b°¥'Ró£y¦pÐÝ>zeàe76²ú6\x000e°¥¦Ë\x0018Yz=x±ÍYYxÙaâUî+Çdk.\x0013¥Äè­Ü\x0003£\x0012CÆA_Äôµ×'e\x0015­-1£&\x0001*ðìöq©«Úqï0ïànÐ¬\x000f«\x0004ÝB>\x0004þäðõ÷p[ªÊjª\x000e«ó\x0015!{dÙ\x000bjñÀ\x001eíÃùP=R\x001dö\x0008ö\x001föÀ%N©èq\x000bëINF©ð=pVG]u\x001cu\x00054ì»/A+¯8+ïØÃMWÇHw\x001c#Ìá\x0008:íVÓì[çXEÂ\x001bµí©«S¤;NÄ\x001aZ²ðÒñ¬Y'ù"ò£[Í¾±üyYÇ\x0013íî\x001c¼<yñX[Å(ê\x001cyñcuR\x001d¤¿Õ¤¿µÂU\x0019ø½aùI$Kü\x000e\»}êa'v\x000e,ào4?;0ÙhèÙaÈ­uåfèÆªH:Öõ¦^×\x0007ä#\x0006èÒÃ#ÑIÚïÃDÍu\x0005Ã×³°ZÇ\x0007ìÂ?åözn\x001f-ño&mÒÂS©ÖbÇ,¯:\x001a¬+-wLD=ÖÒÑ\x001e»\x00190äø
þÆ¹i¥¿³¸¾kqÓ\2Ú\x000b'Â¥Å>Gß},î\x0006®í³\x0008\x0018\x001f+á1\x0012\x0018¨âcûxAÝ9f²ïaí 
ÎCù~OÏ|]\x0001Ïç9K+­Ãáð\x001b\x000f³´Ä*Ï%¼z»;±åàÛS¦Z+LZ§\x000c¤R\x0014Ç³©\x0010kCg ÷\x001e>ÙU WÐÔ\x0010Mµ¡q¿ÿ£\x001a\x000fx°Ö¬
#ã ZÐô\x0010M7¡ñ¤^{m\x0004\x000e¦t` 
=cÍÈð\x001643D3mh4]ÀÀÞ"\x0010 ãv\x001f\x001bâ<2;$³Md*R
\x0016Í= |.«3\x001ak*õv27$sMd¨S@}$!MHJhËól¨®îv4?DóMhÃF[.fB³<tÆÞUSi\x0001\x000bC°Ð\x0000¦PÓ\x0017ii©(yÉì¼¯\x0019d±íkb-#4W
\x0007\x000cçöà¸;(¢\x0001m­"¬­hZ5gJa\x0010Ü^´ÓÐ}áes³v¬o«@E|cé°ñÍ1\x000bÌãòVS}ÔPußú9\x0008ÿîõkðxõõ¯ÿþív×30\x0008{Kc¹$=WKW#±òãÃWÿ8ßu×\x0013\x001eré\x0016.°ý$Ó«àÃéäkìy:Ë\x000c¹L\x000b\x0015BL\x0003]©\x0014\x0010|\x000e\x001e æÇ:Ü'sÙ!máR¡\x000c0\x0002¿#ç<¼®pù9ëå\®é;jn\x0005ëñ?#\x000f¶©¿\x001bË\x000f±|\x0003
Yê\x0018Ï«e"GT­\x0015X¡eµxøX,\x0006Ì8\x0015c¹þÉPq\x0008\x0015\x001b×{á
C\x0015ö°X\x0017KÎØZ´$p
Ò\x0013ÀÀu%\x0015\x0018Lþ(\x0006+·Ñ¨\x0000úd°Ê¦Ê\x0016£*bÊ:&0'Kí¡Õ¡û9+V\x0019/Ùb½P4Ópm·ÀÈ¼b^sy×-&+ë%[Ì\x0008e\x0019\x0014W\x0004&XaKãL\x0006«Ìl²_àæäb\x000c\x0003nE)
ä0)ÖéÍ\x0001«\x000cl²``¶,y`-H\x0012;YiÅ±Xãd°ÊÉ&\x001bf\x001dVc$ûNsù
ì±9+V1ÙdÇ|¤BSpX\x0005×àb9\x0000É1yý©`ü\x001bº`¢ñTwh\x000c«Äã©4¼bq$A8\x0019¬2°ªÉÀzG3m\x0001,R"¬%;æÌ\x001cË¯j§µÉÀÂ=Ä`®¨%âUD`VÌù\x001dSMvLp_\x0000Ü>\x0005M¹+]ô3\x001c\x000bUÙ1ÕbÇàÿÁ¢\x0017\x0018æ/Y\x0014\x000cÃêÝd®Ê©&3\x0006ÖÞ\x001fVKÎæ\x001aËCë¼ã ªÊ©6W,d\x001dÄEé1Ë2ÀefX1UY1Õ`ÅTÄ¢!\x0002ó\x0001uÄ):@ÆÂ£TO7®¬n²bÊ±b\x0008öè\x0016\x0007ËV,\x0004'sU¶B7Ù
ÉycX0Gd\x001e¬½æ\x0005±óuåé&_Lz\x001eÇd½æÒÒÄ
\z/¦+S¡\x001bL\x0005ì0Ë\x001dµ6p\x0013¢/wvÎKR
\x0012Â)V±l8^qGa\x0002UÆÚµÐë(Tyl/\x0006y)6VRÅ\x0007¾Õ\x001e\x0008rÉÊHP\x0017Â­&6ùàx¶ñ\x0014Mt$cË'!\x0006æcùéÏM¾:¯3ÅäÆ\x0007}m^èmàW¹Óc\x0019é·úÏ¯7îõ×-÷Çêû|±óDLÿÌk\x0017ç\ìöç7\x001bloZ\x000e¬àØ\x000fr°Ó!¹ì\x0000HÏ1qwö]ãwýßµtpnå|n\x0007©åïv.Ý\x0018\x0000\x0003¿Á\x0003`ÞÞ\x001e¼¼^~]^ìèKG­
\x0007¡e±TÆì*Ø	ÃOÎ\x000f^-^-vèù3\x001ab©\x0006,0m\x0014hÄ2,¢âú& º3
²J\x000f©t\x0003´TK\x0016KSo4\x001f\x0001X«Í*-TfHe¦S\x0019P\x0011æyØn¬MQëºµRÙ!m Bù\x001dù{&7aY\x0016Ã2µ²z+\x001bb¹\x0006,xÉ\x0015¬2f\x0014î¥7GX´`ù!où\x001a\x001369²\x001e)!
\x001fQ¯#þcµ[°Â\x0010+4`\x0019µ:¼·(þ\x0013£.	\x00127Ç:Ä!VlÀòeò#æ!<\x000fW\x0018ì­\x0019X²¶¥
Æ\x0014ËóW´Ô¡ËÅfËU¾Y+WeLe55Ú­óIjÃc\x0019´m¼a·deMe95*ðü,Ls\x0019â*\x0015\x0005ÆUµ+­\=-\x0006õu×ËÊ¢Ê\x0016*"õ§t¥¡\x0016\x0019+Êöcéee»dñR»\x0013¥õr>\x0014®\x0019·µ¬¬l0\x0013\x0005gÕ&\x0019Øå
G aV®KUfB5	éÝ\\x0018¾\\x000c_\x0018F9Vµr¥³/Á3¦\x0019WÇ\x0015e¸û\x0005M\x0000Òëäó,Â\x000c\x001déLÇs²&¹`f\x0017	é(IE:J@\x0017çÜßjsíTÓÚýïÒÕ\x0005£tJ>-ì6R©uHtÅËpºçÓzçë7\x0008GõÕ%Ï\x001c8»º½þ¶cÝ¢(É	ÅrPA\x0006v¢ÒbxqxÂã\x0006ÎNÏÏþy?\x001e¢é&4\x001c6ÅÙLO\x001d6AzU7\x000fÌ\x000cÁL\x001bf'\x0008
p\x001eÅ\x0006`\)\x0008k\x0016g¡Ù!mBCé\x0017Z3ðfùszÖuv¦\x001a\x0004Øæh®mÕ¸ç0%§MAã\x001cªÄËÛÑÂ\x0010-´­åaàùÐÂ \x001d?äà\x0016÷A«ázùâo´,^äéÉ§ÖtJ9]áT5{: tj£\x000c\x001a\x001c¿¡"=Êóþõßð÷W«ë\x001dµ\x0012EK³²GPbf%Æ©\x0008î§Ã\x0013øÛ«Ã³»ÊôT
IU\x000f)ÊðÐ²
ÿ1\x0015íkræt0s\x0013©\x001eê\x001eRíØ4#
WS¹£V\x0013;V»×Îi¦wE³ÕÙXQ»ß\x0015µCRÛµ¢\x0007pY\x00135,\x001bFnÕc)vP7\x0004u]K*4¶\x0016å%ÕÇ®EQltTL+©\x001fú®%E´Ï'I)o¹dÒêÑÈvÒ0$
\x001d¤**G\x001d%VJG1¯ÙÌ£\x0014ÙèpVÒ8$]kªbYSx?\x0015Õ[\x0018âÆû8úzl4û¢÷ìëÁÙ§¾]½×/ëû©ë\x0012\x0000\x001aI\x0015/\x0006|i¼g\x001b%Ç\x0007\x0003¶V÷ì¾ r}aµ¤*Æý.juAÉ®\x001bJfíÅe²RjÇê(ÚQ«;Jö\Rð¢6\x0018ÝM*op¦(V"UQ¹\x001e\x001dæÓ
Z]Q²çR88BÐFu±$èu1S£ÕËí¨é]¶\x001fGòu
l4ÚÛP¾þ>.)UmTÕ³Q\x0015\x000eÓË×©\x0004Wö)N±ãÓ¿\x000fË¯ªmªº¶i´\x001cÉ\x0006OrïA\x0013H_,Úª+\x0017Ewù(\x0012gsÒ-óHù³r`§ör¦leümßëÄiÒ½Ä)«\x001cøsÎ1\x0019cý\x0013Í¨¡Ú©¡Ï¤b3©$jªÊE¥Ãè´¨VÔÚêq¨p\x0014¥ô²ì-·rQÍ\x0007\x001boSÑ÷ý¥¡áêðý%>ö\x0013i(«Íø\x0008®FÖ
óßeÿµÄ\x000cüz\x0003p\x0015?×Éìi\x0003H½qýw¾P
\x0015Ä\x0002«¦°+¼P}qTÇ\x0007F¶²ºµË\	ïIh\x0004ö[·mÝº\x000fR[»Ô¶Ë§\x0016`­\x001cïVÍ5ö\4Æj\x000f·´µ\x0003`û^N> ÿ\x000fË¨/M{^S=>O²
UÕ^µês«±\x0016DºÑm¥ú½T
A>À>î\x0000¥k'@÷y\x0001QS=\x001aø+BÌXÆ6@ìã©B\x0015kÏc\x0015X¹(\x001e<\x0016Í(]+\x0015÷á\x0005(S\x0000üekmY5\x001e%þ¹|_DFÝÇf5¾&í9W°¨Õð0¥~¸¤ø
\x0010ÆÊÀQ]}®\Ï¹Eã"jX\x0004Å(ËRü£Í\x0007­¬ZV{UË¾½ªËå¨!G\x0001´\x000fÌZK÷²ÚÊ\x000fÀ_ö°
jX\x0015\\x0002²­¨ÌK¬z\x001f5\x001dëu]ëCvUd\x001d^¯B9VjLõ²\x0015Ô¨Ê\x00114ªÇ\x0011T\x0001n~Ú«Bpß²Ò5ÝKTu]\x0005ãªËû
cÕôfQ<
\x0005cÕÅg\x001dÓ³\x000e\x000b®YûA_
u\x000f¾®.sZ;\x001c<[^\x001cÈhìvJ\x001f<÷j\x0005¯(PÑ\x000c¥¯¥\x000f^\x001däÜ6ü»\x0017Gùß}/¡\x001a\x0012ªfÂèiD¢$ß\x001f\x001e©hb¬4¥ú\x0010õ\x0010Q·"\x0006!I­Ï\x0004¬ã¡Et\x000cX¨t\x0001! i\x0007t\8\x0003X¬\x001de\x001c\x0017+§¶¹vh\x0011%\x0017.\x0007«sx75×å#Ï\x0007tC@×\x000eèÉ«Ç)õÔ\x0004
4{ÝD\x001fæf?DôÍ8\x001clýi¸#\x001cìòõüUCÄØ\x0018\x001c÷¸ãÈ\x001cs\x0008¶äê£©$×º\x0010×yd\x0012E;£áYöh|\x0002!²½©û}û\x0008k£Ýlµ£\x0014\jæ#gá\x0012ç\x0002Ð¨«æ>ÆÊlËf»þ\x000fµÁÉ v°`CYGåç¯ce·e³áJS\	\x0018%\x0015:ât?6ÝÊÌ_ÇÊtËfÛiOj4ñ^à ÌXî?iæ¯ce»e³ñÆ¹ÎT¿í½¦\x0017|iïqö\x0015-+Ó(mc4®\x001cj\x001cÐ·£+ú\x0002Qù:T¡1\x0003ÚÀÓ%á|¦o\x0019+ã-­w\x00040ª\x0007O½EÇd¢³\x0011Ue¼U³ñNÒNã
½¼;\x001cBT³¯@UYoÕn½Ãz+ê2 ÊñD\x0011\x0003÷ÏlOBÕNw»õ^W"z­è¥\x0005\î\x0017|¿eT­\x0011Ç+a~\x0005\x0019]â\x000b¾&F={7Ö¥ù¿ÑøÁyôÆ*³xâ¨\x0005\\x0011óÍ£º\x0003ª:H#zá¾\x0018!C~\x0005+Â¾çàºÓ7?\x0008_7¿Y#/§¬7MÉìW
r½Ë\x001arÙül\x0015¨×}qM²1@Éza1Tá6J\x001b7Wá7ðíÿèêöãêëòúm»ºÝ>5ÏHp+ÒÕ)\x0019Y©9
úaEêð:|tz~|øjqö$ÍÎ=<?»M
ÙT\x001bæYºÎ
v(Áq\x00053¾\x0012éÓC8Ý\x0004£Kóu\x0002óö\x000bÞN¸êÕ\x0001gp¦}åÒùuà¼ô\x000e®£³Õã¥\x0003Î\x000eálÛÊá¬\x001aW\x000eU[ògÅK+gÜÌ=çp®må²\x001aVZ¹&i¥Ó$!à°ù|\x001e\x001fÂù¶Ã¡*1¯\x0014\x001c{Àä´rª
1uÀ!\h\9®ÌsX~O\x0013 °+?/®&Jv°Å![l\8V!wpèË,N-\x000c/w\x001eÖ±dEãÊ\x0019r`\x001c\\x000cÎÀã¥~Þõ\x0005ÑvC¤9¦9Ù4ó
\x0016\x0014/»tÕ
!\x001b¯\x0008Øt´çð"Ó|Zù\x0010bÞ¦Õ
!\x001b¯\x0008\x0007iNSDl6Ê'"HªUtIbj\x0016]uEÈÆ;\x0002­óÒIM.^ÔÔ1æ0ú5­º!dã\x0015\x0001N'%££7T9
+ÇÃ¯c43ODuEÈÆ;BEó£ØMÎ?\x0007\x0016\x001dsZT¢Ç\x001dlÕ
!\x001b¯\x0008kÈs\x0007wÝrW[\x0010\Ê\x0011ë4n\x0007]uEÈÆ;B	\x001a\x000câ°Ð\x0002D+âá7Õ¼«_Vl¼%\x000c<(r!\´G=\x0006A­°\x0015Ã<k¢ª[B5Þ\x00122ò\x001d/¤¼\x0011Xi\x0006~sæ\x0005«ª[B5Þ\x00124\x001d>\x001aOC\x0017àkËÂ0\x000f­~E4Þ\x00112`Ø9-\\x0008å\x0002cG]Î=\x0011ªº#Tã\x001d\x0001þ&[:#(Nåi\x0000\x001eáyçAU7j¼!¤£)\x001fN-É=A!DÞpn
VÕ
¡\x001ao\x0008m¸¸\x000e®û²å\x0002%¬£\x000bW]\x0010ªñ(Co\x0004{L¢Pp£òèwkgÒUWj¼"ÀS¢ª´¨\x0014)}a¼ª'¢yõ«êPmW\x0004\ÍÜà\x0011½z òÚp\x0015\üz¦%©.\x0008ÕxAà\x000cè\Õ\x001f0ßFlKd¢yõëêÐm\x0017\x0004>¦©ã$®[³½÷ü]çnêêÐ\x0017\x0004	Gk2·¼v\\x000b\x0019ÅÌ3¡«;B·Ý\x0011¨\x001chÈU×ª$XÐÌÛwº\x000e55^\x0012CÍI@!ìxÍ­d\x0001\x0000çÑU×nº&t,\x0000ií\x0008\x0013°tó®W]]\x0013ºñ\x0010\x0014çlÀO\x001chå(ûlQ=u\x001e]uOè¦{BG/I±\x0000Lç¿\x0017üÊ±fæÒU×n¼&$YÉKg8]\x0011ÔÿOÝÛ-ÛqäV¯r^àc$È¿è+JÍVÓ\x001fEjH©cæª\x0018mF¨I7E9fÞÈ¾7è\x0017D\x0015»°ë\x001cªP¹ÕCG8lí\x000e{	ÀB"YÓ\x0019.­ß­ef­!0-\x000fSM*:Ü\x00031W(¢(ºcÎ~\x001eìdë]mE)¦Àá	rñDl\¨\x0013
W-¦\x001bST-¦It'ÈÅ\x0013{æWÑ©Tòx\x0015-¨w:[o"Ã\x0013äåü¨É©\x000bØ\x0015ÊJ\x0013\x000eK%ÈÅ\x0012ÝrA¯þ%e-\x0014Ô¼®´6Î¾Hø.\x0013a]\x0004ºDâÚ\x001e¡dº\x0007&5tX2<A.,ØÖH\HE«;55ÝdÕ\x000cM&r\x0015:¼UNÛ6sÓËN¿YÌÝ\x0012Éð\x0004¹xbicúpá¶lù° 
î¥âä5<AÎëD\x0000\x001d\x0017«Q§ð{\x0002 $Öí8\x0007ÎÐ\x00049i¢ªxp*,ºq9uê³\244ÁE¦Õp,%5j\x0018Nm.åL$$*épeÁQY/\x0010åÂÜ\x00156\x0019H.<õ%qªÚ3SäÁ¤[³Íyk2$$QÇ`záº\x0014@êþsó¤å\x000cI$ßU¢ò°ÄÎf¨':5Ý]x\x0012}·öêtvÛ%~ÚYm7\x00086Ç¹Ä)\x0019H>¨ý\x001a&2SKâ$}¶Q\x001dÄIÓ\x0019H^@½õ³Æªµb:µ\x001cLúáä»Kt*åø¶&N$"µßøõz\x001d&ûL!ä%	H%´qG\x0004½$TçH"\x001bÈ>¨IUùÓÒf¹Æº4ª:¥ÍyD6,½,\x0001¢ÜM§+\x0003úõº©¿¦ÉN6,,Qª¨$/\x001c&§®\x0004½èÙî¦lx"{y\x0002\x001eÚ.j7GÑJgIO×ÙÐDvÒDÇ 7ØN«ZHQ+=q\x000b'ÙÐDöÒ\x0004È¤Z7Ý¥\x0018ªú\x0004/¯Bgû4!eN6´Ê¦Øne7Ã\x0011ÙË\x0011amHHgÑÅjZ-V)ö\x00046C\x0011ÙYn*¤ß47Ò7ÜTÍ×kÏ¡3\x0014\x0014Á=\x0012b:j²[fsA,æ\x0002]1\x001cQ\x0017	\x0011\x0014Í\x0012Dr\x001bß4Nvú\x0015C\x000fÅK\x000fM\x0011RfMA½ó«ê]®qî\x0016C\x000fÅI\x000f9ÈNÓK\x001d3I\x0015\x001eâ$=\x0014C\x000fÅK\x000fU-s§Ö
\x000b¸Ì|Sà\x000c=\x0014çÄXnÚDí~e¡(1\x001dL¾ø\x0017C\x000fÅK\x000fYåRs¨ÇN|5O>\x0015C\x000eÅ[iÊÒ*Ñ-7tÄ³öJ¤«E'ÐÙîW/AdÂ©Û\x0010GJ¢n²øZ\x000cA\x0014'A¤¤5ºLËñ[Ï\x001a;¦À\x0019~('®\x0010k2Ç"ÙY-§eëlõüèªáê}ÐÍºÜ%¬rÖâkç±9ÛUÃ\x0012ÕË\x0012Q/)mÒtI5ólon5$Q½$ZÝÌ8Þ:q
ì§«$ª$H\x001b¯R
I2õÀ"q8ÙM\x0018'Ð\x0019¨NÈ Õ\x000c$[jºí@mWâ¤í\x000cKT'Kð#Ý\x001aì¨½r9©éòì54Q4ÁË/`\x0003èÔPOS²Òÿd9§\x001a¨N`iýõØQ¹¼o¢K4Yó¯vJÂK\x0014U¤ÖR¿H¤uE¥örìl®(ª(bTùÊãµ$Ö®SÌs¡¸\x0019¢hN¢HÌ©GeKXÑëk¼å4Ã\x0013ÍÉ\x0013,î³ò\x0004ñ#]¹mý°,ö5Î\x0010Es\x0012EZÎÚ\x0001l<VO]¼¾6Ã\x0013ÍÉ\x0013<y¸æNý¤\x0004\x0000õ5'É\x0017Äfx¢yo\x0013(~ÝNÚ¡³¶Ád$±fh¢9i»%WËÁx\x0007\x001b\x0013kÌa3,Ñ¼,\x0011´¨Â\x0012ç4R§É«N3,Ñ,Á/¦\x000b0TOCuÄkô\x0008C\x0012ÍI\x0012=sÒHG Â.=sRÓ2é\x0011vÎÉ\x0012\x0010¥/¼\x000edQ\x0008Kè±«s¯t\x0010\x000cKðÞs·j±\x001a¨qä¬ðR«S\x001e\x000bWóÖÁI\x0014\x0000\x0015÷\x001cT\x001ba3DÅ,2\x0007Ï\x000eÔ\x0005'SÐ2/¼X\x000f.Â\x0019*±ÜoÞèìD]pREÈ²½½§"u8®¨¡4{òìD]pR\x0005g0.<úi¹\x0015Q/<S9\x0000Ø±kþÓwò\x001eÓÅo©$\x0000f1N~Z;T\x0017t\x0011{óîcíè¤á¶	`'¯ùOßÉCír)\x000e%0^ë_\x0003;{Íú¬\x0007ú\x0010KÜU$tFA?î\\x00176ØékþÓg¼ Íÿ±_l«¶udµÝ\»\x000e\_ûæ¯Wi-á³\x0012.K\x001a;¾9ã]8ûfôX)]ZQ¯=	ËÔm\x001b®Æ}sÄK"%ØÔ]8õ +<KBájV×7¬Û^ÓÇ\x0000êÎ\x000caäÈÙÀÕ@¬o"v!4IV8
Õ§» \x0003
=\x000f£\x000c;s
¾¡ÓØl),ëÁVlZ]¤
s_\x0016¯Fÿ~ÁëkÈÜQ,m;­Dj®S\x001cìð$ø¦';¤4R\x0012µ\x001f«iyÒ\á\x0018ì"øF\x0014N»\x0016%*ª\x0011ª\x000e\x0001ôH3UL\x0001;\x0004\x0008¾)ÀÈ-â\x0002\x000fX@RºÙÔkin¾\x0013ì¤\x001døFí:¼¢³ëyÒö¤ïí\x0008Õ\x0004:´/Çè}:þ/@\x0001òVe,­

üs\x001d×\x0019YÞå#\x001d÷U5Æ2Î¶É\x0006ÜnÊ^ì¸lÊv)Dy7Ë\I&>QÙ\x0018¬Õ\x0006øëOÆøÉ§àQå;÷OÛt>»iÎ'}$Ôxýkt~æå]´êu\x0012Æ+KÑ\x0006ÁTg\x0015Zè¢#V\x00157>5ª&äózé\x0002©úHÕ³ÀÙ¹T¸¶b\x0004¯³\x0004$å\x0012\x0016\x0006iÍc±ÌÁ_ÿaOâ?\'1é¬`!>\x0012UÕ&Ñ:_í¹8\x0005ïG\x000bïÇ/ÌQ®BMw\x0014_¬ùÝ\x001fK!ìÎ!W®¼îÌ\x0013ðÂË=Ðk&hã\x000f\x0015£×(ÑÍ,ÝCVrÎ	ì]êQnêêdÅ>=ä;¡´µ«¸:ÍU	UÄmV}!_4+Óª]ñÚe¾ ËU2Ä¥EyÁW¤\x001b>\x0003Íe¡ì>qñ~ãN+E^Q3wfêK ö\x0015â¬¤K¶¤Òmè"\x0015\x0008QU\x0004\x0001ãHntì¬ÿ8ù\x0004Âµ
SpÛ07\x001dÜ[T\x0005´9S9%M\x000e)ÇÝwn_\x000eøb·\x000eÜÆ¡iÊeÌ{VeÓ~ioöð;ûrÝEÃê6a"øâ^&Ï¬A\x001e0s\x0008e_Ü}g¾É;\x000fcmUVôËüè<L-ëu9§IiK²a|Qñ÷ýÐ\x0010vþÌ¯^^¦$Âª¼²OeBrjãÕp2×¦|çô\x000b7ÏéQ'©\x000eLÐ;UnUµÂÂdÛ\x0015\}hp~iXuÎ\¶\x000eñ¦\x00062\cÆ¹aÚÝÉ{{¬%-Òµ\x0015´-±aÌqàêZå$@Ò°\x001c[}¤Z°Ã\x000fa\x000cï÷iâ¾"âÍÛûÊôÅÞAç\x0011ü}ï+=û¸×YÅ\x00030öLæ\x0011é3,ò?®\x0013:VOT&kÚ.whîpØ²\x0016éx«ÎaEÙê*a+I¾ò\x001f.?°îúË_ßÞ½üðæíÇOwÿööõûÿõÝ»·\x001f?¾}\x0018a,(ª\x0013Ä³aÝ¹Ø é\x0006Ü¶¡æå\x000fOî^¾øêÉËïïþíÉãçwß=}òòåß[è¹<L,(»ù¤É¸¨îd¿M5º\x0001È¸\x0005\x0019OØ2ª(+\x0015\x0016ï\w­rª¸ÂlVZô,LÚÂ¤\x00130>ZP¹¬.l±êB\x000c·°fÞÂÌ'`¦ö\x0008uïG!~\x0005lz2[¼5Ë\x0016f9\x0003\x0013\x001fÉ¢³"\x0017ÐQ¢~s»
ú,ÊºEYÏ ±M£ h.\x0014ÕÑä&½[Ø²mQ¶\x0013(óøäý/]¬Ü@úT³zï$ÊËCý\x00122Ã\x0019Af\x001do\x000e\x0012\x0002æñÍã
pÚÐ~&¶× s#Ôf\x000bNÔ^ «\x0012}\x0016¦	íp"¶3\x0005\x0015Yüº\x000f«õ±\x000f«¤\x001b\x001cN0a\x0013ÎÄÍUn5'È{eI·½4#Ðx\x0016§p&p¶8Vlæ¬k´ÛP\x0008[ZÌæq\x0004'b\x0012\x0005\x001e¢Z«<3©Kr\x0014°ÝÀÝû¥{sa\)ðÒ"ï\x001fTxÿ¦|}6£Zò-Ð
ùÓñ\x000fþx?Î@Á&S\x0014LKc±W½AâÊEKçÐþk2z¶BË=<AV\x000cf\x0015ó.ÚIÖ¹t*ËKxØ÷\x001f6Ë¿}ýéÓÛ\x000fÞ=\x000c/aåÕ\x000c/²BõZøÁN	ïÛ\x001aúíãï¿òâû§¿
\x000c·ÀÐ\x00037z­ñ3ö8/¡ª\x0007%¼o­àq`q\x000b,zõ\\x0003²\x0000\x001b}\x0000\x0010Ê\x0000\x0006S\x0016£-0rY¬IL\x0007Fú \x00174këÿçîY\x0014y\x001cWÚâJ.e]¾\x0018¡êX\x0005ðõf\x0005\x0006f\x000eÚ
,oe\x00170Ueá~N]
<}³\x0002\x000b÷m£=\x000e¬l\x0015\x000f0ÖØ/\x0019Î+\x0000Ès\x0011¯t²XÝ\x0002«.`\x0007O\x0018\x0018Ö&D\x0000t4Õ{\x0016Ø\x001dÕ¶°\x000bV\x001dÜ1hªU\x0001£xd¿
ÌkÓ«a»ù\x00000\x001eÅZ?$ b\x0010u\x001båÕB872\x001bö]q¼Þ\x00136ÒA,@Y»Òm÷ìv<ÌÄ}p\x0005þLRê$ä¢¬\x000bm«'J÷­T?Ì\x0004~pEþD«Lb?üIKØ\x0010cÖÓO3\x0004&ð+ò_îDxYz
ºÞâT¸\x0000\x0013ùÁ\x0015ú3i\x000bó¨ú\x0003i½°ß2f",Ð\x000f®ØÏÏckÌ@\x0016FØ¥\x0008Ó=k.#3±\x001f\Á¿_È$#C\x0000¼
\x000cÊ\x00142\x0013üÁ\x0015ý+c\x0006£O\x0005ò\x0008ÿ`\x0006^ÜÈLü\x0007\x0017\x0001´*\x001bB\x0008ÃÅ\x0001jÖs\x0016ÚÍÐ0\x0000º\x0018 0õÀÐéL®_3Ü·ì÷82Ã\x0000èa\x0000AZÅ\x0006	j\x0019\x000cÐd\x000cxx\x0006Íü]\x000cÐÃÙÚKÍg]*Q=E\x0001Vq&¡!\x0000ô\x0010@\x001e\x001dXÑË\x0012\x0006½'óó×\x000c2Ã\x0000èa\x0000þU>fªCÛ?&
M\x001d3C\x0001è¡\x000c*¼EËN¦Õd oZ\x0014K\x0002f\x0018\x0000=\x000cAåg;°±	CP\x0015:f\x0001ÐÃ\x00009eÙÒãVaÝè\x0005Y\x001a	÷m³>Ì0\x0000z\x0018 SR\x0006\x0008m,C\x0012áì¾åÐÇ\x0019\x0006@\x000f\x0003ä^ÈÍ$ªR\x001beã\x000caIg£!è!\x0000\x0016tºeXÿq\x0005&é=Ä\x0019
\x0001D\x0017\x0001ðV£"ÈP{
pP\x0013Öûö\x001fGf\x0008 z\x0008 F¿eÅ¡Ù¢\x0005~9eÑ~\\x0004PT©BJ¼öcAVõü£m\x0013q#3\x0004\x0010]\x0004Ðlp[Ú\x0008$ÏÀÁæ0å\x0000\x0000¢\x0000jA_Þ¹¨rXµÊ<\x00140Ì0@ô0\x0000·0¬õETö,F\x000cBçh5ðÜÈ\x000c\x0003D\x0017\x00034í§éùaÐ8\x001bCQ¥©\x0014\x0008l\x0003äzCç_¾K:Ú¾½Úù\x0017GÞE¬ \x000caþË-*Î{¾6 f\x0001K¿tÂzô.
îQ\x0006U{B>w+h;ó5ùrI\x001bX>8Ó\x0006%úÐ¦¾oÛÙ¯ùìÇ\x0000Dâu\x000c\x0019ò}¼WÕ\x001dÀê\x0004`½:æÈ0\x0005%±vîa¥^¿øÔõÅçÒgöêÓëß½ÿÛÇ×?=WË¬ô!-óÜK;\x001c¯sZ\x001eSá¡©Wß?~öôù7/\x001fÿñ·\x0011â\x0016!º\x0011ö»ÖÚ°ÇùÜæ&	Ú\x0003
\x0007\x001eq\x000b0ú\x0001â£*&¬úÚB¥
\x0013>°	×0m\x0011&7Â ,8{4\x0015)üª\x0007bÙB,~QÈ\x0002õûØ0«Î\x0006¤\x0007fj=\x0008ë\x0016aõ"ì\x0011E\x0007»9åõnUa°_·ïFð@l[ÍoÄ ÉÜ\x0005¡O¥4Ä·\x001eØ£æxy\x0004©ò\x0008â5cäw¬õC£¾î\x001cîomõ@´!Ñ\x001d\x0013K¿ÑÊÒRÞé»6·vY1ÆrÿÌ\x0007£	à¥¹ß¡ÅaqÃCk.<\x0018M\\x0004w`,,\x0013ªv\x0004-­\x0013ë\x001d§\x001dæòVRå­Ä	ÕàÅaî
!\x001aa\x001ePnò@4±\x001bÜÁ¿´¬äpr¡ã§_Á\x000f(`z0f1ûÍ¨b\x0001\x0017éÄÕ²5<=8xéhø\x0005Ü\x0004SXcMdyQ§4þwê0ö5å\x001cFÃ0à§Ër¸~²õ2@CÄ\x0016â\x0003\x0012v\x001ebà\x0004ÇTMg[á×ö5PõI\x0008ó\x001a
Å bê\x0010\x0002äíØ2>±È\x0019\x001f\x0010íò`4\x001c~ábH\x00133N¼ñ+Úñ7\x000fFxû9¦4éQo­\x000eIO#Â4Å ¡\x0018ôS\x000c÷*Wç±Ý¦cã\x0018Ú|:cÐÏ1et\x00175B\x0011\x001aÄ¦Ñ\x0011\x001e~ô`4$~é®,õÌÖï«2·Ecâ(\x0007¦=\x0018
É dx\x0002ÄeÆ>9BkðÀê\x0016\x000fFÃ2èg¢ûî©\x0011h]¸cÔ&êr\x0003·6,~)²¯q\x001bw .3}G@Ã1èæÂ¸$òDP5RBÝ¸\x001cò<ÉD\x0013À£?ó~\x001eñê´\x0007@UOB¬ó\x0018M\x0000þ\x0000¢W\x0012	<$\x0005U\x0010ì\x0017°é[u4Ñ1¿ûi4íæ\x0012ÃíDæ1 E§xTVª\x0019kx`üÛsÿk¨×:7kz0zB¦¨7mÔ¸CºÓúR¼\x0008ñ23,Ðë\x0013i,\ãmð2úÏ=\x000b
= |íªñ][4ùöÝÏKo\x000f#¯,I¿}~@ì×gÐ7W\x0006}s"µl¢£ª1Q\x001c%\x0016Ûuçbº+ã_ÿûÛ¿¿{÷\x0013Wíÿ\x000f\x0019ÀÆË#Y[¿nØåQ
¨44
Ìëî×~òíÓçwäªýÿõb;~}\x0008·Ðyª@B\x000f/Ðtûu\x0003ÓÚ|\x001cRÜB_h|F"®yÙB´\x001aIµ7|8\x000e)m!¥/ÁHy(ûø\x0011j¸W`5V`\x001bäê8¤ºT}´\x0003±C*ë4AG¤;^;8¨m\x00115\x001f"ä9âUë%É³v¤k¿-!\x001c´\x0019!à\x0014|*§p«*'v+¦z9Kñ\x0014&\x001b'}Ãjâèë+%Å\x0014MëÐqL&R3T¶G²*uzÖ\x0007¹AK+
Ó©P	&T/VöÈDzª,0èvæ¯n§x*2	àckq- kZËÒê"f:g%\x0013+Á\x0017,»×A\x0019§©ê	Wåé³§i³n\x0003AqajYiÞ§´\x0006\x0002Äñái(?
	®\x000e¸ïs
VÞÐ¸ê%vÂØT\x0018
ÂH6ó\x001eP¤kr \x001e©VL*ËÍ:cù\x000c&\x001b1Ñ\x00172+%iË
¯#\x001dT
ªahCfôÅL \x0012)\x0018;¯KÄ¤2%±T´G*:TÍª+\x0005\x001dÅú\x0012Vâ\x0012Î¸^lA¹R\x0015ï§¥ÖÊi\x0007E\x0017Kq¾\x0008Ír¥\x0006Ëç[¥µU¶|>©XtPõ¥È\x001ctþÓe©"ªjÛþe¸<<µf°"\x0013A%Ã/ü§\x0007TCÙ¯y°d\x00081©-S¢d¾\x001eÿéÂ\x0014$ÕÌØÿ1ÊJÂz9\x00068C{Ôì­¥ù\x000cÕÞuh#÷XòH0a\x0014±öx.#§V-&_8ÏQµ;¦È¯\x0005\x0014hèg¾^²×;þÓ\x0003*µuð²c*ªí\x0014u\x0001YÇÏ\x0018\x001b\x0012¶È\x0017¤Pw\x0016ðÞ\x001d\x0015\x0019CUËdL\x0010mù¢ÿÀåï~~ýãÛEkâîÛ\x000f¿þüîýÃå~¹ÓËj\x0017>¬Ow\x0018µ	¼$óTòÝ³Ç_?Yu&¾}ñÃ³§Ï\x001f®­(8ÜC\x001f8^ä½ö4gVè\x0012pMÇº)ùÀ\x0016·Ø¢\x000f\x001b\x0016V=Y°aVyæîj¸jÔ)O£-8ú²\x000c¶Ø\x000f\x001bhÝr\x0006Ý¿¨"vÕÌ\x0003À¶Qõ\ýá÷»Ê,m\x000eEÄø»ÊÄj±}®gl·­Þ®öã\x001f\\x0018I
sÖ{kÇ¨Ó.=Ð¤Y\x001b¾¶6|í;~$Ét\x000f*C\x0005*Ä\x0014é\x001c>ÅF¼þªRö\x0008üõ¿¿þåÓë¿½ÿð\x0019p\ÕZ³2êI«n\x0008$¹9Rp­§×#ð×~üêûÇß<q\x0000[ÚbKNlA¶´\x0011Ö:°!q­©äV¶Ð\x000fÚeÂ\x0010\x0011õý\x00136~×òTNpm\x000b®9Á1fNQwDí¬¦®L\x0003{à'%
à2ù"CCcÐh'èD\x0017
ºè>sâ¬Hy´|ë\x001b`Gæ\x001c\x0002CÓ#X±Q¦ ©àª\x0004\x0013ë\x001dÌ3.\x0001Nh£Ã
1ê\x001aÅª\x001fÖ6\@g|\x0002|NQ*Äè\x0005mª<;ÍC\x001f44\x001e>è¼¥m\x001bú|ÕÖTäæ|\x0010.pE\x0010Ý·.à~~}÷õÇ\x000fïþïÿõòÃ¯û\x0004[âu]+G°°©H}ÀP\x0012#º'\x0012?{|÷õË\x0017OÿÏ»/~øæ3
l\x0011·\x0018Ñ±SU¨OÍ@:\x0011ÆZAó ã\x0016dtÌ\x0001ÂXÕ
ÐTÍ%\x0015¼ÇC¼\x0018iü,2X×í¨r\x0017)D×¢'\x0010¦-Âä·"ÁÐCKE\x001bÚR¼!Æ¼ÅOX±=\x0012e´~0%\x0016Bª.q3É<Æ²ÅXüvÌ(û{î\x0007ÚÅ%ä/Þà8Ö-Èê7dÏü¤á7ræªÿ¢\x00072Ý\x0017º½ Û\x0016d;aÉ$k\x0003UÉQNd!\x0015aþH^*úK\x0014\x000f~SòP´|ï\9\x0010­áG¥DRª7@i¹ÆO6ÿ\x001a[\x001a¶\x0013tÓª,»^U/F%\x0019óNú\x0004H\x0013ÉÁ\x001fÊ;ÁÛcÑ!Æ\x0004·äír¹\x001c¯aèõ\x0017ùÅ;Î7\x0016ç/\x0013§YÁ¹¦\x0019*ëÊ4.÷úÍôtÐééTvjä\x000e¬xÝ)k§Ø\x0005ä^|÷7nm{\x0018bL²æ{\x0019Eû\x0001å}¸ÞïO_>ýÛÚ~\x001b\x001dnÑ¡\x0017\x001d$]ÜHõíJ-ÚºØÊ}å\x0007\x001fÀ¸\x0005\x0018½\x0000ä.¸\x0000l"7\x000f:ÜJ½çÖà\x0003H[ä\x0005\x0018Ne5þGÙÏ6JP»¹\x001d\x0000Ó\x0016`ò\x0002U·gñJ{\x0010åö éxj¦-·\x0000³ÛYdl\x0013¯Ç.¸iôu\x0018ÑS\x0000Ë\x0016`9aA\x0012C\x0004µ[P'U\x0015Î<\x0005°n\x0001Ö/Ðm\x000b°y\x0001¢ªò/MWÒMTÇVö\x0006iÖ¼\x0011¥wÎ\x0010[Ñ¦;h[XMº7 ÝÊ\x00157B\x0013©Á\x001bª±¡ðrâ\x001a\x0014¬O®<ÿ)\x0008\x001f¸!\x001c\x0001®
(\(2]+úðþÓÛ÷\x001f~}÷óç æÐd¤µdU\x001a\x0003[L¹¿wåO/ÿäù\x001f>;\x0002\x0013·0Ñ\x000f³\x0003\x0016Àuª¤*ééèbH÷·oú`Æ-ÌèI\x0011U\x0015·åË¦V\x0015æ
0Ò\x0016#0%ï"	
îÁ\x0011rÑyPobÉ´EÎ $}~lñBÔÆÜ\x001dÜ\x0002fÞÂÌ'`²û»õXV\x0015m\x0008Ðîï©ð¡,[å1Q\x001a©a\x0013¥\x0013Þ\x0004tü®Üß#ãY·0ë	XÔÉkJR\x0006èxYStß\x000feÛ¢lgB\x0011Ê\x0012Û\x0012u9UÍZ²oíÁ
\x0017Ì
7&¸ê+?\x0013Ef¶`åÆ\x0002M\x0007\x0005c¹A,\x0002Ë>'è'ò®41&(ýô\x000bVúZ®÷7\x0000ùp\x001aú\x0013ü\x0003ÝRU©¹­-¹~ôüÀø\x000f§á\x001f8A@È³ ²K)È²ÓRZ¾À¼\x0001¡ 8ÁAPv\x0015f[5'J\x001e2 Í\x0016©ÎÂ4\x001c\x0004'H\x0008é²È±5Ñ(%ë^f\x001b$Îâ4$\x0004'X\x0008x¿O\x001eæ½Iy\x0014ýZ¦[à44\x0004'x\x0008;ùÈ\x001b6K2­ïÿ¥DÕ¥íô~\x000bo7<\x0004'\x0008BQ¾¬ý\x001f×qõª&Å-ã-ÜÈ0\x0011 ¢þ¹3XÏg ¤;HZ¢\x001b\x0004y4L'eþ"^çz<\x0013Ï~\x0013s¢!#<AF,I¯d\x0014¢îmÍ9+\x0019¥[\x0011Ú»Ð	2bÉ?y\x001e«0\x001aÖ\x0013\x0000©=Û
Ü\x001d
\x0019á	2\x0002\x001aúÀ5Î·qG¶Ú³Ý SBÃFxú'á:ï3\x0006Ö§fTtcN»É\x0008
\x001dá	:\x0018/IHÒÒ4Ï\x0007\x000cv¿zÂÓÐ\x0011 £P«®Hd:
r>s\x0018çnñÝ
\x001dá	:\x0002®}èþÖ10Ænnq-BCGx\x0002«~\x0008NHº;]¾»Ý5u\x0016§¡#ôÓ\x00116YvfRuB±]Zo\x0010ç£óÑ\x001fç±Q}TW{¦´Ô©ñr_nàíÑDùx&ÊóÓäÈ\x0018t-*¥6¾z¾A\x001cmÉË\x001få±ÁÐáKýtÊÕ(z{	ñ\x0006§3(\x001fÏDy¶ç%©\x00136¢¤]íQ\x0013\x001fL\x0013ä£?Èc]\x001f~jQOïJ\x00183[d ÑDøèðØÆ\x000c-\x000b7 Má\x000eYMäá\x0006L\x0014Mþ\x0008µ\x0014}\x0018ï!IË X³t;åToáC&ÂGÇVF\x0006R¸Ù]Î&Mâ!ß?ÖêÃi"|<\x0011áyôúrJÄ«¯×Eíºó
|Ìü7\x000eluÔás\x001d\x0017bn\x0016&Jí\x0006ß\x000c\x0013Ñ	&ZÊ«9ébÎ$Ï\x0005ã\x0003ÓÌ>ÈOEÈòXEmRÓ\x000b\x001cE½pÔx\x0003o'ÃDt*o¸^­	YnÃ:éá\x0016|I&ÀÓ\x0000Ïë[S-êa´
¶zK;ÐI'Bgie<\x000cÆ¶n÷*À¤E«ÜàeLä¤3¤<îDÜò¯¹Ü-rx2NDNÎ­=\x0015-Vå²-0Å[¾éDä¬\x0019tRQ&Â²2&Þ\x0002§éDäd{j\x001b\x0019/:/jO5g½AHJ&r¦\x0013WI\x0004]_Yõª\x0001c\x0002oQ©I&r¦\x0013«±¨Ö\\x0007Vk®Ñ[¤ðÉ¾	\x0008¼j@\x0017´CÓt\x000e¦sé6æ4±3=ýÐi\x00109.83
\x0015±ÿ
p Î\x0004%Þ§§«¢ôb\x0016Hc\x0018À.ý;3\x001bgÏg½\x0004ÝÉ+­¥\x0019\x0000¨(gr\x0003jÏÆò©\x0004Dd¬{{Ôö\x000f1\x0005÷6\x0007f?\¶îu¢ Ô³t- sj'ËjÃ$z¼\x001b/
Ãkë\x0002ÿàFÛã»\x0004'îÈ]W¦Öxp»IRÜnÖZûø\x00077ZN=Eÿ³{i\)e ½Å\x0013¬mÆ^Ñ²m¿mV\x0015ÿG\x001dQ\x000f \x0002]\x0010è\x0016
,õ\x001am=6öä$©¸¬®|(-hOb ©wÎ\x0010¯\x0016pñvPi\x001eüþ§ÿüï»Wÿüïÿ|ûþÝÛåCbáIDY%\x001c
uÈYßà#ëÎÎÇÏÿøòÉÝ«'yòüé¿
\x0010·\x0000Ñ
Ç\x0005\x001f©"F,:½\x001e¡\7vzñÅ-¾èÆÇ\x000bà\x0014`[ñ²cõf\x0006¤-@:c@yn\x000f²"Íþ<D¶è\x001b]]öÞ,æë±(«b½Ö\x00109)\x0004·\x0000³\x001b //
¥èJ÷¥_i\x0001Ø)~öû-Àâ\x0005È[·¤¢
=\x001bVmèª»Àc¹¦ñâ«[|õÌù\x0013B\x000c¼Íqµ_nºª¶í¦²½øÚ\x0016_sÛ¯\x001f»S 6ÿ`\x0011µ\x001fíæ?ø.ÍqK\x000eg\x000c(¢@¡ÿ#\x000c\x000bê\x0006Ç&}\x0018,¸Iß¡81Õ±±¬hf\x001eÓNíÁÐ\x0008øY¤'7 kQgtãeÇ4ë1$/B\x0013¥Á\x001f¦\x0013)\x0004"Æk\x0019~ã+ÿøú§×¿|úø0BãÇàwäTd\x0003á²êTÏ!¯\x0015.ëY3§
Ñx
ú=%\x000fªÀ}¤U4QH\x0001æÉc6ñ\x001fÃZµgó³\x0004k\x001c{ë\x0011&5cþcÈk&%\x001cÂÅãpeÜMy\x0011\x001a>F7!s\x0013ôgA¿k\x0015\x0015!ÑS\x0018§ãµYØ!Þ¬³£.\x001eÞ,\x000b¢\x0016üº3Ï°\x0003\x0019N\x000cÚ\À«ó²¦ÿêÓH8Ë-a{S\x0015 ü\x0017è¸úñ2GMäE\x0005Þ0Òä¹\x0004üë§+ùä?$ó\x0015¼?O\x0001bÓ»
ÆÉ«Jøã\x0015Ä\x001fÝÉD¿äÉm \x000eXÆ6è:{\x001fØyÏ)çé0e!Xà\x0005ÑÂ³w*Ü¹\x000fr\x001fÞ[&§GæTZ­èí\x0019vú$GF¼
ï?èõþ·\x001f>þíí/w¯ÞýýÃûÏhæõØ¸\x001fx\x001d¬ÐÞ¡Z²\x000e¢\x0005¼ß<yñò'¯î^=ýöÅóÏæ)¾¸Å\x0017½øzî-;Õj&µ_A»\Ú±Ý\x0000i\x000bÜ\x0000>5\x0008\x0018Ô{¶q\x0003Ì[Ù\x000b[+Å=¹]e\x0005²n Ý|½\x001b`Ý\x0002¬nU³FÖ\x0019êmÁÑ^Ù¿ñ$ÀË\x0005kñàFuxU£XP6³véZÐ
\x0010
@ô\x0001­gÛÚ[GMktYïP«;D7Bã%àtð\x0012gWu\x000cÑü76^\x0002N7­ÄK;ô\x0007ôãHÚ;»\x0017Át\x00034^\x0002N7-ã\x00186á»ªpHëÕ¶+Ô\x001dF\x0001-ô\x001f¶Ó×¿Þýñÿý\x001fÿü?}ÆG"Ê¢êNz*çX²(_÷¼\x0001ï+eÿp÷Ç'ß½øþ·á\x0016\x0019ºqÑu\x0015¬ãZªóÔ,ÓY<"|_Êahq\x000b-º Å~¥_o*\x00190Ìd*ïéüã}\x000f¡Ñ\x0016\x001aù¾g·Ú:°Gå¢Ä«j\x00041µûÞÔ\x000eCK[hé²ZÞBË_\x0014´²V¾(hu\x000b­~IÐ6³Ç\x001cÖÂ\x0017Í\x00046ðE¶ß\x001blðE60¡
|±í÷Â\x0016èúÁ.\x000f®\x001fùç½_tjýÏwÿü¯,*i\x0011GÍ¥äª¥»ÚÐËWO/Rµ?ü¥_\x001a?÷(L×o®tysu`D(Ä~ÃQâÐ´%(\'~q\x000b18îÞÜSGU1îªÝÕÛ¶\x0018é4cÚBL' "ê¸\x0016wÎ
Ä1­uÕéy\x000ecÙb,'0FÒ'N
:ê1iÿÆé\x0006Ù¶ Û\x0019C\x001eO$Zµ¥ðòµ\x0017u§jèÆ¸y\x001f¡Íû\x0007d\x0006½Ç¼l½\5\x0002t0å
ßõ"\x0011É8«HD~acú½Ö9
\x001e¤<6¬
Q\x0012
-êz>\x000c¥ë[²\x0017·EÙëÛ×?}xÿ\x001b
0«,zâ[0v[W±Ü-qÓÔ³Çwß>þãç\x0007\x0000â\x0016 :\x0001\x0006n\x0001!Ñ\x001dkº<,U\x0002Õ\x001dË÷÷I9\x0000Æ-Àø\x0005Z¶\x0000é\x000b´`Ú\x0002L_ \x0005ó\x0016`v\x0002\x001ce~$µTE\x001eûõÛð\x0003³M\x000ee\x000b°|\x0016¬[ÕmÁòHh[
L%7Ýà\x0018"Üßõì\x0000Ø¶\x0000ÛgÁÍ²Ð««è!ý®#[z;¦ã\x0017E·Òç@\x000f,¢v ´Tò\x0005r	\x0018.\x0001/@\x000bÒmùi¤,\x000cô\x0018> qç@hÈ\x0004¾@6\x0001Ã&à¥\x0013¤E¶A]Y\x0014[Ê¸@\x0007|`úËÐÐ	xù\x0004z®]T¶èÝ/óÐ5\Ç\x0007¶ý:\x0010\x001a>\x0001/¡`\x0005\x0011¤íGnRÕuõoççY&^7`cÕÆå%ÚD9º\x0017¬G\x0007¦â#D\x0013\x000fÑ\x001d\x000fyjN¤¹\x000bð}VÉ\\x001c2\x000bÐ&®Þ`Ó/¦"\x0019Z®¢|äZt\x00116\x0017L"4®^W¦¨µ¦ÄªÃëÀi
:RË\x0003ã\x001d\x000eÆOÐë'T\x001aO,&ì·fY)\x0015jTeéôÀW\x0007Bã'èõ\x0013¶X/x\x001d¡êlÕÐPõ×Ó\x0003ëq#$cCr'¯!¬3Ú©ò\x000b¨=\x0006}ëçq6ûOÆO{b³
Ä÷ð¢{´³H¤ú¼Áq|ÍäÖÍ\/\x0007\x0002°æGAè\x0004ªÇ8ùáê\x000e\x001f¼\x0017 È Vâ>\x000fÉ®UÓ #|@ôë0B,Öû\x0014¶
$n"]3¯rÉ¼&!F×DbYÄp{\x000eµò^²´kåfoy±\x0019+òN=\x001e®
Ý`I'ïù[ó\x0007FÜ\x000eC$a;ÅÆÒ\x00034éê\x0010&°i)Í:9\x0010W×ÌAvXY?4ÜÛ¯àXLnÃ:!BÏ[\x0005áF;h~\x0008\x000f¬í>0ÛÝ!XxLJ"y¤\x000e4b\x000b÷K\x001cGMØæ?½Ô\x000cbÃÚª\x0008ÞöÜ´h\x0013\x001f\x0010'9°\x0018_á?ý\x0008s\x0013¨Óc\x001d¢&\x000fñ\x0001
Oép[È^Ëv\õPõ\x00068}]>6-8¼
Pp/ \x0016¸z6í?Ø%G/ßþÇ¯o~~÷_?\x0003°ç\x0008ÚæÓ¹P7\x0001v.ÓHûVÖ\x0015ÞË'ßýðÕ³§ÿÇ\x000f\x0007 â\x0016"º!öDQlØ
*\x0002\x001d¢\¨\x0012Yyýs\x0010ã\x0016bô[\x0011õÂÂ+]\x0014¡&bËöàY´EH~#F\x0011Oà5`, º@,2ÞÑ!>°\Ï\x00031m!&¿\x0011ûÕ^ázæ
z\x0014\x0014ân¸Ã\x000f1o!æ3Vâ-<g$\x0010ëVB?¾²ÅWÎÃ íg­<Â*&\x001c_¹î^Íü\x0010ë\x0016bõ0È¢cÖiÑm½©hÆÝ³y+¶-ÄæX%í\x0010	ÌÕºÏ#Öû\x0016û ^JÚKØ\x000en¥jµ\x0013k\x001cþ5nóÌÌ4FK-~néÀdÃ\x001a7CÆ(Uïß¡çh¨\x0005üÜR²H\x0004&ä=ò©óp<\x001d\x0015ÁP\x000bø¹¥5Å©¨\x0010BR¥\x0014Ó
N£!\x0017ð³KQÍßþ¥Ç´DÊ±/=oGÃ.à§R×!²\x001dÓp\x0018ÉiûEp\À\x000bøÙ¥Ð#5"Ê¶ºPõx¢]Âu\x000e¢á\x0017ð\x0013L¿õXew\x0003ûÔÄx!ò4FC0àg\x0018yÁÀu¦c¨³·ÌÇEC/p_¢S¯Þ¢I\x0004\x000cgþÎhè\x0005OÐö3u{U©}ö4bÐ\x000b¥éØ^ÐO/%j
\x001eaèWq)G0ÂNâÄÑ^]üü³ì\x0010I_PW;~kç@4\x0004~	Ä*Æ\x00188i\x0014	²é¶
Ó\x0011
¿ _²ö¤.f\x001cÇqdd8í á\x0017tó\x000bkQ®/äÝá®óóB0\x0018æ/Xh\x0008\x0006ý\x0004uØ;q¯&¶c\x0003\<\x001fy\x000cÃ a
7\x001a¬7HÔ&faÇ8ïÕaÐÏ0©ÈâªnÇ(BÝA½\x001avCó~dÐM2,\x0000ÔðHÌH¢àà\x0006%hH&úI·¾Kpì\x0017þ&^\x001dÇ?Ìg¶ÑLtL)ºü+Ò2R\x0019(1cÝÍõû!\x001a~I9®f$ÕàIQÕûbÈÓ\x0001<ÚúcXc´©\x0019A\x000b'¤Â\x0003Ý»Ns?FC2ÑO2=ÑY\x001bÍ\x0013/ú\x0003¹!`ÑÈÓhÞe\x000cÉD?ÉôV[#xèXUF&\x000e;>°íØÑ°Lô³\x000c©xt\x000fÚc¬ºC\x0013·ÆºÓëðc4,\x0013ý,Sôå<d\x00101ÑJXÕ­KNË¢!è'X4KäI\x00105/+;i-?FC2ÑO2¹iÝ;¤!B@HÃó×\x00042,C~ô(¬ß{iµà(óL\öFh8ü\x001cÓÅ uÝrõ´»¡\x0018òSL\x000cZç\x0017­,¡1h}\x0007ó|ø&C1ä§~«Vÿ¿¥ÕFBíÉ\x001b\«É>Âø)\x0006eÓG¤5Õ52fw\x0017Ã0ägTµ\x0005\x0015¶TJ
Â0ãNÎÑ0\x000cù\x0019\x0006u\x0015Z·#ºò¢´,vLóá\x000cÃa:\x0012yXe\x0005°XD´j\x001cGÚ£ú1\x001a!?Å\x0000r§\x0015]Àë\x000f5ã¡\x0008°\x001f£¡\x0018òS\x000cq\x0001T\x000c.P\x001dãN\x0003Ó1\x0019I~	E::X9O\x0018Æ« ÆùKB2\x001cü\x001c\x0013/\x001c\x0013t?[7£\x0016Ë`¯?èÇhX&ùY& æ%nË\x0013\x0019rÊUÝ:N{u2$ü$MV5ñò³¬òÚU\x000b8\x001f\x001cáäæ\x0018^ÙÓ«dwK·¢
· îtü\x0018íK¿d\x0010åXIÄò²VÀ\x0001æ©:\x0019Iná:Å\x0010\x001f¡PLB
0Ð0Lò3\x000cT]k×jx"ÝÔ] äéè\x000cÃ$7ÃªÝxx4\x0007v"Õ~`` ÉD	µBÛÆ4\x000ecÏ¿³!ì&RUz£Û1Ä´R¼ü`\x0016£aìg\x0018\x0000\x0015toýZ\x0012\x001b\x0004Ã
Ù\x0010Lv\x0013LáÞ8jË2\x0014q1â|¹1\x001b~É~~	,9ªLp$i°íVÜ©Uû1\x001aÉ~)Y0v+Ìb\x001c¥å4oGC0ÙO0¼pI\x000ec*ÚÀ/ bÇ:ÿîm/a
Ê\x001e«Ôÿ3<h.E¨aÇ²\x001f£áìæÜ´&Úí\x0018´ùG\x0019Å¥Í{µáìçî(¢¹\x0016¸oB.þ u[(;Å\x001a?FC2ÙM2¹GmQZit¹Å \x001eÇ\x0012§Ýº\x0018)~á=EâÖýSkÞ\x0018¦\x0013yþP\x000cÇ\x00147ÇäFyE\x001f0#Ld-dd\x0012lëPAjËA\x001b\x001coQ*ffr-²ü§Å8TÔA3Ç°ß|áhX¦øY.,\x0013/ûa\x000e!):Ñ°Lq³L®ÚÝO
AW\x001eË\x0013;&<Å°Lñ³\x000cAiKàÍ¸±zÞ^óÇÑv-ûY¦ÓßZ^^Ô I¢cPn`GÃ2ÅÏ21qâé¬¬u¨±#v+&ü\x0018
Ë\x0014?ËdÞ	ªm)?2F¬EÃcÿÖÕÐLõÓL\x000f8ú \x000eYD\x0010xf=;Íe?DÃ2ÕÏ2Y\x0007\x0011º\x0019GU_;\x0002Î_eªaêg\x0018XeLË¢ û\x0006Ò¥,:àVÃ2ÕÏ2©\x000e;ñß:\x00166â|#O5$Sý$I;Ô¹*ªë²:\x000càN`ÛÑLõLjÃ©¹\x0019%\x0015µ÷-ìW,ù1\x001a©~áBc\x001dõ<1ciÔó¦ój8¦ú9¦\x001fF\x0014±w^-¸:\x000c¦N
óÕåjGcü\x001c\x0013ªÄFj¥òåp½ýçQ®UC1ÕO1¤ÃxTsÓ¸Y/2a¾ç¶\x0019i~	uÞµ G²{ÆËÛ
zÍPLóSLÏÊÆ\x001c5+Ã\x000cÃó\x0017Âf(¦ù)&\x0004Ý×¸Yn	1\x001eÍc4\x0014Óü\x0014Ã¯k}¢ö8\x0019ÖocwukóÖfH¦¹I&·Ì\x0017þÕ #éý÷0jzaÞ&7w\x0000çú\x0006ð4\x001eît©Í§eÍDÇæ¹
@J£\x0002M\x0001é\x001e\x0004\x0013xøO7BQ­~¯n²ñdh2\x001d¾ÁRó'®¬E:VU\x001f \x0003	!ïöaøAÚi²à÷¤½ËËÇ:=\x001aÇÇ\x0007iµßeÊ2E¶^þ#ß
×KëøÜiúù
ì¬-ÿé¾Ê4©öõ(áè	iúÁ\x001a®FYý³¬¹³KP¨;Z°\x0005ÝµDóûjPÔ?)×Ð½ìW\x0005ÍÂÕ´ÛæhÝÆ?¹¤¸zomªbÔIÑ0ß*\x0003W3þ!ÇÆI\x001eø¯r¹\x001eÓo\x0001§eàjÐ?B©é>Q¾¹Jï-êj`¾»N[ÒèF/w(Eo4,)³bÔ\x0018	Ó£ËWÓÕ~§!Ðç#ÖèÆ+\x001càlv\x0006v´\x000cü³e9\x0016näYSñªs[´	n)\x0013O?\x0015nµdä¹PUÑ}íÖ2
ÎÏ=Òk­ìºÛéwB8á\x001ag;\x0001]F\x001e6Yv«éÜÑÁÌ2ÕÆz´_ïN@ÈÏ\x001fë$J\x0003ó»¶ß@[Ò5ÔþÉÎ|üÈ[¸ôAD¨ B~/²à5Ôg b\x0016ZÊjYËjFYm~jª^v¶uÀâGwûk\x001br<"'\x000cM/áXç\x0007§ò\x0015ÌìYRÖ9çP\x0008\x0000òbÔK¿Å|/Ãf·À|ãYÆ3|B%vÒÝ\x0012	Ê¼ÂB¼\x0019ý0¹w<å1¤M¦MklXãy§ë5AtY\x0013ô¿~ûæ³û·Ë\x0010ÆHZüKº©0\x0011ÄkûýïgO¾úÜ®[º^	D@¿	§'å QEß»xÔz\x0008F]ÓÍQ8´CGáÄG"\x001f!ñ\x0017\áèÈ-]ÓÑQ8i\x000b'\x001dU\x0008
µOëMj]x\x0014NÞÂÉGá$\x0019g[DÜt<^ÛKh7Á\x0014LÙ)\x0007Á$}\¤ªõj#IÜ\x000f®\x001dS·pêQÛ ´É&^yStX[¯n÷³\x001dÓ¶pÚA8T¸T\x001eóí	RÎ53
\x001f_ÿôúO\x001f\x001f\x0004s¹3\x0018½ÿö·JT/\x000c®BÔÃAòm.ÚQ\x000b\x001c8n\x001cdÎ4F\x001e±ªqÒ®Ûì(\x001c\x0013áhHî'9Èz­¢ÞÈ'yhÁY<&$ÃÑÌ
\x001cê%^ª*Ë®cð(\x001e\x0013áhPNA®ÉiÑå/b\x001fm»ÓQ8&&ÃÑ \x001c£tr/æ	jVyÎf\x0013áhT&mæí÷ P\x001f¬Cççºdt\x0014Êp4,óá\x0011å¦¨+á¹EIv³Gá¨\x000cGÃ2qM¤<|+\x000cq8¢³æ1a\x0019ÆeÞ×G"1ºïø\x0017FÜI\x001dÄ&2ãÑÈI^º}FïS³\x0019MhÆ£¡\x0019Ç\x001c\x001e/S\x0005¦£O\x0011vu»£xLìÁ£±w\x0001ÆqsW<µ\x000cI ³I\x000f\x001agÇ£Î\x000ecÞ\x0013!ÈÛ\x000fi¥+ÂY¦@ãìxÔÙWYU\x0013dè\x001aR¥&ÈIoGãíxÔÛa´+ñ6&*®:\x001fÃÙD#\x001aï\x0007½×¹Éif­\x000fI
)ë{'¶ò°ßÄc¼+\x001eõ.\x0008Cì¡qy\x001eÝ)K/ä9<&ó\x00073\x001f¶¬aû¤¨ö\x0019æ9y|¢½\x001eM|B¾\x0007dÓ\x0005OØ\x000ei]ÃòQ<&øÄÁµ¾$ÓR/Z_mÔ\x0010N&>Ñ$>ñhâ\x0013¢êz\x0001kf·\x0017ÐÁÙv»¢ñ`,ä©?õ.V©ÓT\x0011ËÙRF4Ñ0\x001e\x0001Dú\x0013jÒ6íÍ\ñÉÐ\x001cM(\x0007C!Ïò\x001a\x0007U\x001e³\x001dÑØ-\x0006>
Çä=ñ`ÞÃ®j="hN"èÉÂ
ÈLG#s\x0019eD\x001aÑ³¬iá¾õö(\x001a\x0013é`\.-ií\x0015J\x001e'k×7ÖÝ\x000bÖQ<&.ÓÑ¸|©Ê\x0001W\x000fd\x0010\x0014uö\x000eËî÷(\x001e[;\x001a\x0008Kä¦«\x0005\x000fiÇ\x000bÅ!Ö·_ }\x0014	t0\x0010²Z\x0014W\x0018ê\x0011ÑÐ²<Ç\x0004B:\x001a\x0008ûµOy»'P\x001fB0½ä=t4öNgiÙµ\x001a9Î\x0012\x0017àCGOj2¦[±õMk\x001cçÓwädO:\x001a|x!<\x000e ,mç'\x000c5ÏéBj2Ñ'\x001d>©°òÀ
\x0007µ¡F³\x0016F:ÇDt4ú¤¨òE8º"HÛtðt¹'¤0\x001dL
ìí~\x001dÕaÅ¬\x0019\x0018­\x0014&\x0013\x0007ÓÑ8¸Ê\x0010)\x001ce­ ÷­	<öyâh LA¥5¡_\x0005A\x0010un\x0017ñìsI20\x001d
T¸\x0011{Å3î[Ë\x001bâ9À'\x0011¦\x0019a¡1ø\x0001¡h -©§ã®ë(\x001e\x0013ÓÑÀLcO\x0010ã	ª\x00165|\x000bw=ÂGñÀ\x0006f
êé\x0001Ç°:\x0017½\x001cg\x0013óÑ¨\x001cG?	ôLT»h=;ÙDå|4*cÙªHh?÷\x0010\x0001Â°Sÿ=ÇDå|4*w¦JXà©?ÔQ0%Ñ°\x001bb:ÇÄÂ|4\x0016vnPû4-{÷_´ör´GáPBÈú\x0013x/´Ì&\x0011¯}÷ýQ8ö¥öh$ä:³´ñÔñÍ=°jÂÇQ<&\x0012æ£0\$<sÒJa¤6ÚÊÎÂ10\x001f
ýk6»2sLºx\x0000öC'Gñ@\x0006Â@*`ÔsÕ:fFSK=é[ÅÂr4\x0014êH,!ªkÆTü~GÖQ<&\x0016£±0<£gN<Ò´Î¶\x000cï*g3ÔbrÂr0'\ôJ´	i(CÆ8ÆbËN·ë(\x001e\x0013\x000bËÑX\x0018òPìw/RïÒ:s÷®9s1Á°\x001c\x000cWnª\x0002]ò\x000caÏg;3åh,\x000cQX±rK\x001bÞ¥Æ9\x001b
í[9\x0018
ófõ\x0000]TÔÒ\x001cä³·ãbba9\x0018\x000b3ÒÊ7?\x0001
!#r2/&\x00100_6n*Ö\x001fÇU½'a'K+ÕDÂz0\x0012æËZ,^è«JY0¦<÷ã7Gñ,¬\x001eÌÂr\x0019¹\x0010\x0003¿û¯ã@yØg§÷z8Ïøë§åÿó6×à_\x0006 U£)c]¤4è½|É	¦\x0003{1Õh\x0015þí¬pÙF:nxÎGÛçN^Kº6V\x000f\x001ecU=S«ôb,i'³wø\x0016vm¬Ô\x000e[«tú([ó+¦õäÑ|
\x000bòñÈa@ÞtSÒ\x0013?6¥\x001eÊá¶ºëOØ\x000eÁN§*!=Õ]±86ÜìÕ«\x000f_]/­Çry}sðëBâõJÑQúØ\x000fÁ\x001côú
Òëÿ/Ô®ÏS¤ãÇü÷zT-é\x001aUIÇQu\x0003ìO¬Zóä\x0019\x0017
	íl3ë.$\x001c\x0008gH\x000fPÍ\x0015¦|<\x001eðUIë\x0010õ¢t×<{ª`Gp\x0000yÈC[JÛØôÑ.;HÏ>Ý©:~¨êªí©}·cªó}·¥îø¯\x001e¶Õ2¿.·\x0015C\x000e\x0007´ª\x000eÙý\Uòj¬^F\x001e[Ê_~xóöÿx÷öãÇç5ø-Hî\x0008«²Þzªªî\x0003­í\x0016¿|ñÕWß=}òòåç&JòÕ¨\x0006\x0003C\x000f0@¾Ï­ÀÆSlEiºèÀv£c.`q\x000b,º,²#hy°Y¯xÜ
¢¸vº\x000b\x0017mqË`e¤«Ôd\x0014{I© ã*×gÞ+mq%\x000f.T¥\x0005ìh¬ãCî
.`y\x000b,{tty¸\x0015\x0019~)^¯\x0014´ '-°â\x0004&'\x0017\x0000UÅ\x0015\x0015×®àìÂU·¸ª\x0003Wà¾£¶\x0002+E¥7¾¢Pgë;¡\x000bXÛ\x0002k\x001e`M\x001b÷5³ÑÝ\x000b\x001dÖ®\x0003É\x0003k£¿/\x001fÇp\x0015ùì.²¥ÁT`(`1\x0018Ø¨ï	û\¼D\x000bn¼h!\x001ddü%¯óx\x00170\x0013õÁ\x0013öy\x000bàÚ´´¨])¨g,î*Â.d&ì'î\x0007Þ±§\x001fsùÇ\x0005Y
ãcîöG»À\x000fÈ\x001fxË1Í²^JVÑn!\x000b	°à°¡çam=e\x0015Õ\x0014V`Ð\x0014ÙîõÃÌDXðX.Ö¬ÉôÁ\x00169eÒýO!íi\x00170\x0013bÁ\x0015cûµ\x001a\x0004WU­ã\x0000¶{üt\x00013!\x0016\1UýÄ1)ëúÆ\x001e<ª +;)0\x000f24Q\x0016]Q6\x0005Ñ\Z¦^äôëf`>3Ç\x001fm\x0006ëe¤º»+09þ:ßÆÈf	ÍñG×ñg}<\x0018=ÏNrþã%dìºd}9Ùf|ÉÊÞx¨)®3\x000b\x0017ù­jöÃ%ñ)h¯-´×Ä\x000cFÁZ!ÊFf6E¦¼#4 wÞÑCGâ\x0016&Ðèò`Ïá\x001a_÷S\x001f¾¥°Ò=b,\x001aï×(ý¸ûWc\x0000éú\x001aLæ\x001aüñÓÝ>üúñýÛ\x001fÞæ~¾ÖÊYª\x0006¹|5\x001f4ª!ª;UF÷òû»?½øáåó'/_<xX!â\x0016"z!&Æµ\x0012aFM@·É\x0013å{s]\x001fÄ¸\x0018ÝV¬²ÄØ6à#HO7Qûm+þæ¦-DrCDÚÂò¡¥âºÒ?ô}WR\x001fÄ´ü\x0010\x0003WC\x0019bä{ªh;i­R¸·.ã·\x0010³\x001f¢îîîVl*Xõ,ÖD\x001fbÙB,~e½IS\x000c,ÊÐ)-BD³\x0008ë\x0016au#YuLå;\x000f&¦¶ñöCl[Í\x000fTÓ2vÇfN2ÚL	Ò´·l.Ùd/Ù\x00071¶:\x0010¿xÊVeçnÅ\x001f¢%\x0017?»t¢º\x00191«\x0016\x0016êÐ\x001fñdâ4FÃ.à¦¼²\x0013+ÈÎ;Ìª÷î/ù0\x001az\x0001?¿PãÇ\x0005#b×Âð2ê±bÜ÷:û1\x001a~\x0001?Áð²ä<\F"£*´\x0011OL;5l_"Ö|G\x001f"\x001cùD\x0007Ú¬yS»ä\x0013Iý&ß úÉ\x001a\x0017 Û¤ñhâ£\x0013¼Ä\x000fMÒ×	Y\x001a-:Òyï	x\x0014O Í¡\x0014­ßQ³È¦H÷={ÇV6Ñå\x0005)ý\x0013=þùçþ÷Û»ï~~ûîýÝ«\x000f?3\x0007\x0011òrìõÉ<v42-ÞÓy\x0019%\x001aùÇÏ=yr÷Ý³'Oß½zñúM|¸Å^|,·´ÞbÕÛ\x0005\x001fJs,Éä>gðÅ-¾èÅÇÓ\x0004+¼¤+VJjàòj¥8	¶ðÈýyUq3RÏËÖ&ÖAJ¨ýZm\x0002ä\x0019|i/yñaU?\x001dÆ4mòÕzöóæ-¾ì¶_¿\x001d,\x000e\x001cS \x0019JíîÔ=ªy9¯lñ\x0015/¾XøÊ¢øÖá£j)\x0003ßéóÓUxÉIïÑy÷ã§\x000f\x001fïþüëß>|®\x0000\x0001#´\¶½\x0014ôÛîúqÿòôëï_¼¼ûó\x000fß¼øm\¸Å\x000e\{×È«*a\x000b#âÝ£®âÂ\x0015·¸¢Ç^5J§^\x000fÅ_>Öªª~JØ{]¸h<ö $l4\x0016?4\x0012©°ÀînN.`i\x000b,y\x000cÆëFa\x0004\x000f-\x000fêª^nb:ay\x000b,{,\x0016ªÈE#ïNN¦ò
\x0019\x0017Yæ	`e\x000b¬x,VTÇºÓ\x0015i>R²4~ñ<ÑÔÙ¯[`Õ\x0001Å"Ö"4ÖVuü¶êê¼¸Ë=À.WÊ%\x0005\x0017²,é;/wÓeFU\x001fº#î¯A.d&'±þHH+²ÅI\x000bm?f{Àîë\x0002fâ\x0005x\x0002\x0006pÕ¾­ÀâØÕØ¿«2È;ÝW\x00172\x00130À\x001310GM70¶¨µVäÝs_t!3\x0011\x0003<!\x0003Ú2b´Ø,\x0014í$jÒwÜÓÌd\x0007\x0018\x001a\x0012G\x000f#_¶V\x0016_rñ´Ò%HQçkf¢?\x001aºD\x000f_2²J+²\x0014diR\x000bÚ­F´[Pë\x0002fÎ?ºÎ?\x000f\x001b.I\x0019\x0016ôÕ*o}=éÝÍþ¸óóÏz¾ú1¼	µå©»ï§¾¥á%ô\x0010SÿAÛ\x0016Î¢\x0015\x0014\x001fúÇÜ
Ñ»5¬ya\x0010Ù\x0015þn²é1ÃÝ \x0007Y4\x0019=É6[\x00154"Ê:vdÒQÄçp&a6õy&êc7`|\x00145fhÿ!á®¹ÕÌ8@t\x0011@UéÉ¸\x000cÿGAVõx\x000bñèñ\x0000Öo^g§#ºW¼BvÌµ\x000bñèñ\x0000F&¤É\x001dYM¿¦\x0008.ò4Á\x0007ñ\x0000ry@\x000c2b\x0019yü}mBìÒylSç\x0007Ç\x00038jHÝ\x001bPã\x000c\x000f/Ó³3È\x0007Ï\x0003HÛ=¸'¥Éõ\x0017dq*\x0003"ã\x0000äs$Óñ1`X\x0006¦Ç,î\È\x0003\x0002 Èú±¸,\x0000D#ÉB¼ØsÉ\x0003$\x0003ã\x001d\x0019È\x0016ê\x0016t­\x0006#±Y2\x000e\\x000e\x0000Us ^@\x001e³e¡Þyd¶hàÊø5]Ê\x0019ëCÂL+ÊØv\x0003!.dÆ\x0003+	B¶:\¶WJ8ËQ/Áe7|èBf< ù øHê\x0019üH0²3­gä©ì,\x001b\x0007È.\x0007@\x001aþZÌSqÙþ¿bl\x001c {\x0019 ÊÇì^J\x001242èÇäÎ×	dÆ\x0001²ï\x0012P¹Ëo\x001c³¦áÆ1¡l\x001c û( H\x000eÔ]ó7¢\x0006
Ü?Ý»\x0019\x0007È¾\x001c(óÛØ\x001aÎ²\x0008\x001112\x001cál\x0006Y1\x001eP\÷ó5½XÏYÕîýVå±³\x000e£\x000bñâº\x0005ðÛD\x0016d 
-å\x0003Ì\x0004b\x001c x\x001ce³\x0014\x001bKÒB{ã\x0014AJz»Ð.d¶<ëq\x0000hU4P{ÖTù}SKz;%z\x00172ã\x0000Åå\x0000¬ëKRÓÈ|Zéë\x0004ÄÝhµ\x0007Y5\x000eP]\x000e\x0010¢\6×ÊÙÚ¶ ë#¹p6\x000bm­\x0011}ÅÆ\x0012Eh®ÿSÕ5\x0010=|g2u?ç¦\x000fSnüÃ'ÏÛ\{¤¯ê¨Z»ün­¯þ4Ù)pñOí8\\x000e]§vy7­Îã5.¯.\x001aw\x0007¾Ç°käÃÇQ7
S¥ªâ>=êTm74åsÔ\x0001\x0013 OH
\x001eíÉë\x0013ü=-¾××kèÄi;àò)*¡Æ©û\x00017\x001aYçxãq2^ÉrÒ
\x0001%Ñ\x00133e:¸L\x001d¬Ð^{ e.t¯Ð\x0006Û$­O\x001dÚn\x001eô\x00106\x000cWêý\x0007~Tú÷ÿxýË/oï~úõîï~ù·ïyýî3Mý(­\x001anÖ"8·#´*JATÌ=áé·ß=~õêÉÝ\x001f¸ûãÓWß=yþêñÓÏuö+È¸\x0005\x0019OLA=øei\x0010
 h¥ëüY´EI'Pæ [i(³°ÀDyÝ¦RÍ+ÂYi\x000b3En_ô­;D¨Ãí\x00060ó\x0016f>\x0001³TiéÖD\x0010\x0008$dÜÿ×Fö,ÌºYOÀdÓuCr\x000e¾Þ\x0002SKMTy ?	óò\x001cÎ0ù9Ü³'ªz8\x0003éôS¿ÇèW/xÃ	&\x001cÁxÔ\x0012ë\x0015ç²fÁu¬8QÜ²á\x001aø\x0007¿/5Y%DËX
/éøb©æþëEÛó
ÛÑÅ$jÿôö»Ç?¿yýñíÏ?¿ýåAýö\x000b¢V\x001cSÓ~8JºR¾ãÞ/È}u÷øÙW_>yöìÉ«ßF[tèEWTT>\x0006\x000eOÉÓNÊ.nÑE'ºÚÖ^Ñn;m>èàTxX(w\x000e\x001dmÑ\x0017]æyE(§j£\x0010¥±ö¥ç>xi\x000b/ù\x000fh\x000bÇ¸(¯ÖSuÚ_ô¼ðò\x0016^öZ/È¼à"~´ÿ\x0015cGZ>ze\x000b¯xái¼æÔZæ³úÇÕí\x0018\x0014w=|^xu\x000b¯:á Ò¿¢4ô\x0017BU'»»\x0017\Ûk^puìC$¯ýÓªÜ$Å.\x0013Þ\x001cø>hð^\x0008)\x001aàL»\x0015P^|1¼Q4Ýæ2\x0018NÞ¥î¸\x000b3ÀK\x001aIÕ¥Xn_îòü\x001fÖq7eîÅgX\x0003¼´<ò­¤&ç/¨\x0019Ánå\x0017á
ð\x0012GD}ã\x0014k
Ì¼PEÌ»2\x0017á
ð\x0012\x0007
sîdXG\x0016»{ÐXJ½Áñâ3Ä\x0001^æè·&Ñ­ZDu­Ä<61iû\x0019æ\x0000/u°\x0016£lÿäöÉÕ=zªê£e7ÚëÅg¢3xÃs\x001cKÇ{åø]dHw¦Nxh¢\x001fz£\x001fT\x0001Ç!t[bªº\x001et/VìÅg¢\x000bz£K¿fF¿*Z.%\x0012éñ;I6/>ã¾èuß!Ä75úÅKb»&/>ã\x001eèuN\x0019ùO?ïÈ{L<\x0007ï
D4×µ¯ú\x000f|]ûúÃ¯\x001f;¶_>½û¬Àd\x000eºÐ*PP½1¬YÕT³© ýâ\x001dÖ«ï~Fbr@Â-$ü" Å-¤x\x0018R\x0002VH\x0001Ûg/\x0017\x0019jsõA¢-$ú"¬·òq+©xÑ"H/ÊæX¢À\x0008»\x001eB\x0014âµLK\eZ\x001eÿçÛþºûóÛ÷\x001fßÝ}õúã_ùå3%²>_qA¼E\x001a«Nû_Yëñ_<ï.øç'Ï_>½ë.øÕ\x000f¯^}¦b\x0012¯Zâ*Ôâ\x0005\x0019dè±ÁEì5
d®Ö'AÆ-Èè\x0006É"<­¨\x0017éseG¦¢^vÿæI´\x0005I~KR\x001cäá=]é#Ë­	ì=ö$È´\x0005üÌE\x001fiJ+\x0017µö¨Rw±¶ye\x000b²øAzgí9»|ë\x0014\x0006Â\x001b\x001cÇºÅWO8öl­\x0015ô\x0001³uÑM\x0000+0z\x0012dÛl~#!jX*ª
*sÆjF4j(ç0^\x0003QäP¼ä[8vÖ­\4t\x001dæ\x001al\x000c÷\x0007ñZÆk)¤Áýº1T[Íæ(M\x0010\x0007\x0014¯\x0018Eãqª\x001dóÐü,iÞ«ÁÄGð\x0007HF6\x0004\x0010µY¿R)*\x001aq\x000fÁ\x0004H8\x0011!kÒ¾åpÄ(Yslí\x0016\x001f<\x001bùL\x001eæ\x001eÇÇ¾n^\x0010¤qæã$8\x000e'\x0002y'wÖêà£Õ*õ]Ó|\x0004\x0013ËÁ\x001fÌkÖÅZ4É®ñäÞïØ7\x0008&ÃhÞ²ô¸ñ°½jç&ÒAiþT¢	çè\x000fç5ë\x000eÊEx2)³!óa\x0008MDGDç4Wñ3UmdLYçY\x001bOL£´iùÞé»ª\x001cýò@²ò\x000e¨-\x0003Í\x001fK4y9ú\x0013ó\x0016uñ_Ìd\x0002±¦ª¶ìÿ\x00167øâxð\x0004ñ\x0014Ýç½lDÖ=\x001b¨Ã\x000b­Ýà\x001bÞA?ï4^T¸L=¿\x001d\x0019T1¢Æùl\x0008
íà	Úéä\x0008
±~l¤[%R¹)
í vøUBæÈRÊªîQG*ùD\x0003MHGHocûKL.(µm¹Â
PF\x0013Òã^
RnªÒÔ¿¸h	w[Å¹'Q\x001eOÄôÎ6k¡=&^¶2ÖC;q\x0012¤	éñDHoÚB\x0013óª}µRçÈ\x001bÜ ý¶Òr"¢÷\x001c(J\x0018\x0002)¯Ôn\x0000Ò\x0004ôè\x000fè7
íPÔ\x0016¯tè;ÙçQ\x001eODô\x001aD\x0001r\x0011Àji\x001eâD¥Äù-\x001eý!½\x0001è\x0015|é8D)¶¼ë\x001eODt¾\x0016[KêßÚÚÕMO3¢¹IDÿM¢Á\x0010´Ë=ÇRt*¨\x000c^nààd\x0002:ù\x0003:¿IÊJÄoÎ±59nP\x0017"\x0013*É\x001f*YJ¶8$ë­%=ñ\x0006\x0005
²\x0005ß\x0013a¨c)g\x0014-ð\x000fÉ\x0012Vê\x0007iüNø7·àÈ÷¦¬±2\x000e{Vy\x0002'ã;tÂw.9æ }ìÊcô¿´6ÿÁñtÂwª÷\x001eu6©ç\x0019uDôyÆwÒ	ß)C¬\x001aêJä!½R2Þ\x0000¤qtÂuXìD@òíL\'©ï\x0014*7f\x0012HB\x0011ÿâöó ª)Kn\x000eAã:Þàa'î°ÆSXk+ª;/\x000b%5YÇ\x001b$ë\x0008×H\x0011ÎY5ê+Ê">¢g\x0019IÜ<Ø\x0010ÿú£1ê\x001f~ô×ÖI÷ïñÂUIãè²\x001dªÞ"ù(»Ï_N\x0019õ_(ÙÌ,\x0005MþÅ}Tµ½%gd±}\x001a\x001a¬n\x0010ò¡]Û\x0015Ú9·úý±"\Û\x0015á][Èª=Ê\x0002ï¤÷Ì6¢\x0000N8\x0016Õ«æþNj<ûðë»_î½þñãO~ãºÞ¤i\x0003aÔº¶ÝÂ¾mùÙ\x001f¾º{öøë/¾ÿþ\x0000<ÜÂC\x0017¼þ+òV\x0015^\x001cCª+v
^xq\x000b/:áE-`'VL\x001a{ô¢vµ°\x0017\x001emá×zQt©\x0013«àê6=Må\x0012ì\x0016¼zÑ¥-ºäDG:\x0013°7©R\x0014]Ü+\x0006{áå-¼ì5^ÑyÞdGkÙ¿ lH°_VãW¶ð\x0013^Ò{YZ\x0006èÖ3Ô~ô½Ú\x0017^ÝÂ«Nx òÙ)\VÇ\x0017]ò
u'\x0006ç\x0004wéwX^p¢ë±DÚYy3º|ÚÑÍ
­^·czá \x0007Þ¨². ßÊÕÔ\x0015¼Ö&¤Ý¨\x0017*à
+Y\x000bÑ=Í*Xi¦Æ\x0002×Ê(^|ÆqÁë¹cØ8±È°ìÍ©A\x001an\x0012¶¨\x0017q
ðúF\x000cÒùµ4\x0003ëbLÕ¼éøv»\x0014øÐx\x0007z½£³ÌGò¨ÀË¢²Íã9´6%p{GÕn\ìtá¯\x0013ß\x0013fS.Ä´¼qg-«ª\x0017·à^çÝªIÕ^VÃðGðG_Ú×P$^]Í\x000ctcEÏ«Nso©`³R\x0016°áôû÷wïyÊùå?ÿû·\x001fÿóÃ»w?½½ûùõÝ«×o~~÷ÏÿúÌÐ3r£$,c¾\x0002î\x00167ÙÔìÊî¯ÿüä[x~ùäÕyñôåÝ\x001fû¿Áã»W¿zöôÉg\x0017C
|ÜÂÇYøT@j)\x000f±\x0010\x001e\§Y\x0005=\x000f?náÇYø¹\x001f\x0017\x0019OáNÐu|!¨|Râ¬è¦èiþÇ\x0019?má§ÿqG?oáçÿqÖ/[øeÞúÈ&Vë«\x000eb1ÕÐ¹ ÏÃ¯[øu\x001a~jÃssÐ±U(ò¦Ø\x000fO¾íái[ømÞú êÝúAú»;ü\x0002j}3ö8
³UY+Ì?ÉnÇu1\x0019dÑ]ìæ§Ûâ·¬;M»ÿjç\x0005C»0Í»%EU4àØ)\x0006Ë°ÿM\x0017\x000cíÂ4ïþ«Í_\x000cñiæ-A'\x001f\x0012÷Å£¸¯<×¤j[Xfá\x00034{ú§ÃOæf¦\x0015i\x001dñ÷$ÑïëGªÝÒü\x0010môÓáGòÖ¿iô×ÖôÎ\x0008·LÛ ÙàÓ¦£O7¯t\x000f¦R²ô8æ¦÷ä\x0001¥âÏ\x0016ÿtê6¦/ÈMµãGµ2ú³ÿ\x0002hóæåqò_`h\x0011ññÏbÿ¤¹OÍ7
Í\x0001â?§ãg\x000e~ã.«¸0\x000b¥É\x0001*éár²ð§3Ö, ð£¬®ëø\x0003(þÆOÊÕþ\x000bLg,\x001b+økþ\Ú°·<ÿ)øÉÎâç¦záß
¬ÿ²ü\x000bèH.o ½e\x0004-hþ\x0005øÏÙP¥\x000c_¸\x0017EðGY<Û#h¹M\x0004p=§
ã)ò×¿|úðþîåÛ¿½ûåî/ïþöþ³\x0008M»Ú\x0003éaÕ]-iWúæñ«ï_<ï¿yúêî/O¿y~\x0000&naâ\x0019 MÎØÚ\x0018Õîñ\aÂîÝï\x000cÌ¸\x0019OÀäIÑVç
ôHÁØa·@I[t\x0002eZ\x0016\x001fdY"­29èvdÞ_{\x0003i\x000b3YÓeí@N.m<¡ÜÂy11%u\x0012Ü\x001b!çR;J#ìÞµÎ ,[Å\x0007¦D»bQ\x0002~Î¤ûhÂ®\x0006fÝÂ¬gÙDê`5¦\x001cË±Ï\x0007n\x0012Ú\x0016eûB}|3]\x000e×V\x001fLUàX$$ådfLÃn`L0q\x001dü\x0002¢È[bËñÖ\Ç:ý£ÿ\x0019&dÂYqÍRµ+;Ç2\(\?ÁÁiâ\x0011ø\x0003Ò¿ÊÆÕÁïëÿ"Ñ¸Qô»Ñ¿\x0008§Õí_s$Õí÷¥Ik>\x000b³c\x0018\x0003Ýºt&ÆÝ
¡SF5½z«aù/Ô¶pm[8iÛ&Tß3å"{=»mÇVÃ¼{¥?gÜ+´Ý¸'àþÞÆM×o?éúíç»×\x001f_ÿôî3\x0012m%&\x0011p%\x0018Ë:JhÒ«Iý\x000eu}WzúoKß=~ùøO?£ ®_vÒõËÎoë_{íy ^É»v{\x0015Ð>Hâ\x0006Ó)phÀ¡\x0013]iÌè\x000bºîò¢¾\x0007Iú©(r;é\x000cºË\x0003£KäBW\x0003²ºÒ\x000edì¦@N9ZD4gÐeÜ¢Ëèü²Õ2\x0017t9ÈNûþe£¢«åºÆãCWñàt*ºýÜ¡ôh\x0016\x0008²¥£\x000b×\x0015@ïÝFoùºü\x000bd7áÀÅ7B\x0018¾\x0011Nú\x0006áu5ªÆ¿½}ýþî/o?¾ûésQ¯êÄWÿktz\x000có¥ëÎ¿=yüüî/O^>òýo\x0003Ã-0t\x0001C£©,h(Í£\x0010\x0006®ë\x00064\x0017¬¸\x0015]°@WBWÞ[-|\x001f\x0014Å±tÍ\x0012.`´\x0005F\x001e`0\x0016\x0011U\x0016}Q\x001d<êÀv-.`i\x000b,¹Õ!Ö1j\x0013u ý	§>eÞ\x0002Ë.`ãA\x0018\x0003­¨X\x0017íô]¸Ê\x0016WqáÊ²òÅöEº\x001bLwìæ	\°ê\x0016VõÀ
åQ\x0012Ù°¹<²Ú+(,ûÖå\x0006Ö¶À\x000bXSõ\x001aqÆ\x0015X\x001c\x001fr·ÖØ\x0003lÓÇÊÂ\x0011d\x0017eÈ PiU+\x001f¹¨KÆÝJK\x00170\x001bô\x001dQ©\x0011ùIîÝ(	PÝ\x000c.\x0013óÁ\x0011ô7MÁdmP.C0î0.d&ì#îG®aà\x0010Hl:\x001aB"MÌ}pÄý~ÆèÑÀºÐ2ç\x0011-hW^s!3q\x001f\x001c)¨²\x000e¥¨d¦¬Ç_ëu!3\x001f\x001c©M©°)KÖÈÇ¬
\x000c§r\x001e0\x001f\x001c¡?ò\x001eã ~9Ffú=YúÂnq°\x000b	þàþýcÆ¬ß¥Ô\x0001hH[îåË]ÈLô\x0007Gø_\x001egPm\x0006ò\x0004Í\x0002NCü,Í C\x0013þÑ\x0015þ3
ÝÅ2ìóX\x0015X¯k\x0002ÿèÿÀ£jïáæÊ#Î]­ÃÌfý.\x0006ÈÚ\x000fÁû\x0018dÍ@·YP\x000fÝ\x0015\x00172\x0013hÑ\x0015hiä±×ü\x00082H#í¶-»p®pF(K½{8\x001bª<9Ôá»*¦\x000b\x001aè\x001a¬D©Ç,«k&jå&\x001f\x00136ËQ%\x0005zãI\x001bã%9+J\x0002Uõec"§t\x0005-9 ñ2Uèå£¦©v,Ã	p
Üfs«ØíµÇn¤±ëV \x001bL@»M\x0011NË½¾²ÜqpÙAe9°i\x00117
Ë©ë9lvUå>yj\x0007QSµRÓ#\x0014\x001f7tÜÍÃ:
÷ãá~ôdÞªy©9·FÃþ¡Î	ëÓ\x0015¬ã&ý\x0012÷\x0008U`¹ò\x0002\x0015i\x0017Ðì6ìvF\x001d\x0002j³u3î\x0018d)Áþç¿½ûùíÝwütðëÇ·?®l\x000b²ñx«½`HCÀôØ<~öìÉ»þ×wülðÃË'Ïþðã¿ÿý×÷oõ^£Ã-:t¢+-hk'»¬ì;\x0006CÀ.kp£[tÑ®§jm-È³~WwÒxÝÉ«M¡£-:ò¢KAJ0Ô(É|n¨«Ê]\x0006ìG¶è\x0017\x001dK­àx·®T£ìH!¹c·à²\x0013\æhq
lº\x0006,\x0014\x0018\x001fÖÔãýèÊ\x0016]qØuwrí)ÓºD·\x001b®ÉXîRºV·Ðª\x0017\x001a ,\x000f ÚP:9KhA:!\x0003ÍyÄ¥µÄºà\x0017¥¡xÍA\x001cðÔ%bú®`\x001d¸£\x001d$Ñ9!.Ð¬7\x000eOZôº\x001b)§\x0000\x0013OÀ\x001dPH¯5Th\x0019\\x001eê¾\x0006é\x001c¼îìÈú\x000fú\x0000ô\x0015¯üúÏwý¿}&CQ\x0007Á±Ä!Ù\x000b0D:vUð¯xß×_öÿvá×k8q\x000b'úà´fHÕ3 ýeWý>\x0002¶pÈ\x0001§ÿ?­ºK\x0018d9vWÆQ8i\x000b'y¬S$\x001bêpÊ£*Ù\x0010dÕ£©»>Ô#pò\x0016NöX'£=ÙÐë\x001d\x0016]¹WãuB{\x0004NÙÂ)\x001eë$y§f}
®¼¬Ö!ýX
®sÅ#pê\x0016NõX'=Ô,æ¬¢ü:\x001bÄ\x0012°'à´-æ±\x000e\¶×\x0006I\x0007{j¨býúáG³Yø/o#Ç¬£ýé)ñ\x0002P\x0007bÛU:à±aÐ\x001b\x0007e92"Ï´¬\x0007å,\x0013à¯µYè/O!Çì\x0013}zb }Òj\x001e~	9\x0001ÇepÅå¢ËgywôX|Rtï6Æ3ÇÇÄep\x0005fMxq¦	\x0013êÜ í+KGðH\x0008ÎPº[{¼Âô(­Þ»í¨bÛÛ¶¶¶\x001dûj÷\x0010$\x0017g¾P'«å\x000c}ÕkTÕê¶Êu\x000bL\x0019\x0019Ð:ôìÝ·\x001f?£5Ó/ò{ü9;ce!í]\x001bË\x0017{v¹_
ÌcGÏ~õäågÅpÊu\x001bL\x0019m0\x0007ÁñC¨Ã¨kÛ»çI¥\x0012ó=k³]àâ\x0016\tZ\x000eE>ri[Pí\x0006íHÜW´Ðh\x000bv»|ÔNx \x001fµHDïØà:d9Á¥-¸ä\x0004el©CË®{(ú\x0000®_màò\x0016\ö«UnÜÁÐT\x0012BïR\x0018wÁÞ	®lÁ\x0015§å¢*ì¶\x001eÓ\x00068}¼Å¸K\x001càê\x0016\u\x0003Ýâ°\x000ccÉ5/'õUÜMä8Áµ-¸æ¶\\x0016Ã]Ú8%êòGÝ/xö@ÛôÉK.xøÈei¯àE\x0018ê«ãE\x001eq÷Rê\x0004gÙÁK\x000f \x001a¹ü¾¤\x0012/¨èÒ~³½\x000b¡\x0007pòC?hòªÐr\x0019ò?©¨·Â¤·á\x0007ð\x0011Ä2¿¾M¶BC\x001e'WÂ»®D'8Ã\x0010à¤n:µ\\x0018­ÃIwLbÈsA\x0018L\x0010\x0006g\x0014.ã½¹%ä	º\x0005\x001d\x0015]\x0011l·\x001c@g¢0xÃp¿é´Û´Ö<\x000e]¸ÎwàL \x0003o¤«#\x000c§K¨+ò¸ÐM·k¼ó¡C\x0013NÐ\x0017NØtê\x0012|WPÛÉ®vsÁ\x000em¶é\x000b'\x0015ôÓÇËêâõQKç8 ä¹p& 3tt£sK;
J(YíÓ®
ÉÎÄ\x0013tÆ\x0013hºÂ´ßqªËu<ÛÓd¦nn^kz¢7/OÈ\x0013.ë\x0001¦2­RÙlj¯!f7Ä§ÜX÷ù°"b¤I3BÞ´\x0018¬ùµ\x000b ·ghxÉR+*Àÿ9á]qÆ\x001b7OùklþÑåÃý*V%Õm¼\x0010¶¤ÔQw²ên®\x0000~rçÉ8B IÎu#q\x000fô7ý7ë'~ãûÄKaB?±¦|Ü\x0014¤x2©*W\x0000\x000f`Uõòå\x000b£øHÓt?ùï÷+xÿø¢Ò\x0003¸\x000e3\x0000þ8óû¦¦!^c^<Ï°ÞÄòJUaÕx©¯tär=8VðªjÆb>ï~ùôúý=$¢	KEoã-á(²ÜB¿|òêé«ï\x001f?ÿú\x0000FÜbD?Fl¢Þ²Ì"¡´é@¬Ã÷h\x000fÆ¸Å\x0018O`\x000cÚ5±Ø±IÖ\x0015\x0019ïOk<\x0010i\x000bü\x0010c·]\x0011Zn:¤ÚoæEi¹Ý¶z0¦-ÆtÂUW3¢|êËi¼?ìx æ-ÄìØ/$ÃU\x001aé\x000bÆ6²v¿K{0-ÆâÇHA\x001bÛú'Ñ,\x001bõa·cÌóºn1V?ÆU+xÅX\x001e­\x0004ú@Ö!î&ü\x0010Û\x0016b;aF\x0010\x0015¡e°Inð£âFÓ\x00107jÀx]t;1¸\x0011j­m\x0014ð\x0013\\x001bwÓC;?¾þéõ/>>ÑrÌ	¡&\x0018µi{u:"Ï\x0003¥K!
ÉÀ	iA§¸\x0019T.VØ\x0016â®gÛ\x000fÒ°\x000c Ô¿¶\x0018\x0012Fì¡¬ñvÜ~&Ã\x0018¾\x000eWh_FW\x000cw;î6Sø1\x0018\x000eþ ÎM¡Z`jM\x0003dL:Ø78&?7\x0018åþ²d\x000bDÐ¡\x0010\x001e\x001f£áà\x000fâ¼,S\x001c\x001b-ºq¤·y>{\x0004\x0013ÄÁ\x001fÅyîGÊ°¹jy=æA4»F\x00037D4A\x001cÝA\x001c["\x0019ç]d\x0013ä6\x0018
²Ìï4H\x0013ÅÑ\x001dÅ#Ä´ÚqY\x000ck|¼tòãC5	\x000fF{Sð\x0007qV'L\x000f¡8&¶1íÚ\x000fý M\x0010Gw\x0010@º*Íek"Þýcv\x001a4w\x0005ô_\x0016\x001ao\x000bW¯Izq¥0:*Â\x0003\x0015x\x000fHÃ4èfnÈE¿u1d-2m^2è­+Ân¨Û\x000fÒP
 \x001aDà½[rø6ÇKµäNÈÕ\x000fÒÄqtÇñE\x0015U¤¾ÚºOb\x0001Iú¢Ñæq4q\x001cÏÄñ2ÞÓz¶
÷vß\x001e-\x0017q>G\x0013ÉãHÞ²¨¸ðÜ¦º£ób7ÉéÇhd<\x0011$[ëe\x0016P\x001aH×Nöx pæ\x0001i\x0002Pt\x0007 Øïé²3|¹3oSTñ\x000erþk\x001bßnß¼z­Q®Èâ6\x0015.ØiÆµã	×ÎÇî´½@*á)\*áe\x0012É¸
¸ÅöÜb\x0014UHf³\x000b\x0015LãkÏ4~Cn¿âF½j'\x001dQ¡TG\x001bÉ\x0003M.\x001e¶ÈwÂoz\x00064>w\x001cÄ­SL7ÓgßÐ	¿a\x0005
\x001cûuJ¤¤K}j·ÝÓÑø
ó¦O ;tV¿)Ãm·ñtÂoê\x0018ê
üØ¿Ò
ï§\x001c\x0017°éi2~NøMMªïÄRÒ²!)E\x0015^@¯F&ã7éßà#\x0008Ô]Hö\x0008Q\x001b ën#®\x001bd6;øÜ=Mä¢ Ï£­Yba¾DÍ×Îg¢¤nÔé·\x0005Òû6eUóÂ¶\x001b¹ò4_;øÚýæ0¾vÓ\x000e\x0000ªðbÏ.²}h8\x0011%3©ng ]Ò\\x0012qã¿(f\x0013&³?L\x0002ÖqM£g&5Pæ®Ó\x0018qrÂmÖýàëx@\x001bQ\x0012U)\x0010Yl\x0016¤ñâ÷þY¥¥bÉ%¥o+å4rÉ\x000c\x001f¤ñâ÷\x001bKì.T\x0004dQUO,i:\x0017ã7Åï7\x0000G+×#Y¹\x001e´¼ò\x0007+\x001c «±d=Ã7YnÜý"Ó/]hÂ\x001bã\x0003]z®\x0017º¿þã××\x001bíÛõ¡N~s¿<dn_'i9º_pÆÓìN¤ñD©÷¯Wh;\x0013X¹b\x0015h\$º÷¿4sKó¯È´í
Y\x001fämoÈÁ÷îýªU³*\x001aàðé\x0006ï´x\x0014O!=ÛÉâz\x000c½ôTÉsè\x001b·_Í¿\x001eøöWÇÎR\x0016ÓÕ\x0007pþöQ[oÊøøó'åúãsÚ¯ßo@Mn\x0014ô2´L®i»Ú-ÂÕ\x0015ÖëæØÃï¸z\x0000\x001a öehì¡Ñ'\x000fPØ\x0019õM,î\«ñº\x0003"îä5Ï|ÿëZNETnÆ¹t\x001dGyè\x0003myGÜiLñþ\x001f¯¼ÿG^_Fë1\x000c
\x0016\x0016<Ñ$êá2_@½²)rÿ\x0018.\x0001_(×N'\x001aÓ7hjk×\x0007µ#©Ì\x0003ÚzPt\x001d6\x000ejæSØASX¹0§37iTC\x001d\x000f\x0019u\x0002jNW-9]Z.¹{ùáï¯?¾{ÿ¹5\x0002µ¬ó\x0005)ó®_5d\x0012­Âï×è^Ý½|ñíãOf"Ã-2ô ãÓ¸tçti~IM·PâNEÆ,nEÍNgîËÑ^xgéF»gxÏ\x0003¶ÐÈe´ \x001dÝjº|¨`\x000c

Ëþ´y å-´ì²Z\x0006Q LçÐÆðôØK»\x0013;õA«[hÕ÷A¥ÅFYÁ¦PmºéØ5\x000bV\x0001V1YqU¹AUA\x0012i\x001f=ÐoË9K&¹u÷0k
\x0014
\x001bt\x0007ñ\x0000p¹@ÉQæ¹ÖýÁ:\x0007O\x0003Û=+\x001elÆ\x0005Àå\x0003ý¿¤\x000e°¸§D\x000eÌpqÏ}.èÁV\x000c¶âÂtJoÁ¦ÒM÷Öwû\x001a\x0007ñOp9(ë{Ä\x000eF\x0014\x0000±\x000c³û¢©'£>û\x000fØìß~{÷íë_ÿú¹]ÃTÅx©\x0011.ôÞÿRuØ¦¶¬{xÜ}ûøÙã\x001f>·]XÁá\x0016\x001cºÀ-ú\x0019kîÖ\x0000q¼³Vû^t\x0002[Üb>ÃÅÂ{5\x0016Ãqõfµ[Ö"mm&îÀF[läÂY¬v¨µ\x0006{"§íPVZï\x0004¸´\x0005|ë\x001f5®'.WE²9F\x001dt«\ú\x0001\x0007æÄïÈõûdæÔC®\ËyVÎ\x001c|ßî,\x0007:sæÀwèB$ÉA(Q^\x001aH¨¤pßÞ1\x0007:óaÁ÷e\x0003`®è×ÅÆ\x0015]Ñ~Æl%bO +\x0006]ñ»\x001eÃª7I­Ê L÷X½p\x0010ï[\x0015è@×\x000cºæCÇ\x001dD«W\x0010ïHX½È?OáM¡CC\x0012èd	V_]¿lìèV­Î¼4\x0015,èUY<Îx\x0005ú¼\x0002ÃØw\x0017\x0016§;Ïj,N³\x0011\x0005W Ï+bÔnÅn;P¯Ð}ª\x001d\ü°Æ)Ðç\x0014\x0011Ddû\x001a\x001e­\x001bÒsO1å»>\x0001Îø\x0004ú|"FP@~­\x0005±8,\x0015sØhéßwè\x0008QæF06Ñ\x001d]d\x0017\x0004½C\x0000gÎ\ô¹n%).\x0013.*a¼sÇ\x0004èÌ¡¾CÇ\x001ay<\x0000:!\x001b´Y2Æ4GbÑ\x001cºè;t\x0004Ú\x000f%ÈÅ°çNªõA÷®Î<L\x0018&_\x0018fEgÍëZ\x0013wígn,E\x0014FÆrä³\î>ª½ãEk7=ëÔt[«fÐÁFL	6Ô/*³C´7\x001dô%\x0015µÄeI¯¯¹ê&Xhê>\x0011cµÁÎi¼°¬ZÐñsàJ\x0014¹ê\\x0000?­ÍÀ\x001bÿoåäàcDòðÃ#¤,a°ÀC\x0018Ñ\x0018¦2\x0000"{\x001b#ß}¬§ÆÚYUösªÜõ;ÏÔÇeeÄ-<þ\x0016®$ ÈÆ÷\x000e¯ºLNYk\x0000ÔhÊ3([ëe§õ¸}y+XÇý\x0005^jê¸­NñE*ÆqùOWö z\x000f\x0017c¬ù]ÏëkS»õ¤-<ßÇíÙ±&Q·ÏKê.\x000f$ý)t9\x001aãñ®E\x0019½n±æGb»±\x00087\x0007"´\x0012íøO\x0017ºú ØïÛ"IãêP§ÂJ±a¥8ÃJà;c;#È»|æ\x0011
½3©°Rªù¶ü§¯\x001cø¶³^¸QF92Q
0+%Ýèj4Æã?]èº¯¦õä¥F)EmWâLLíj%W\x0001\x001f¡-
l+ºÜc\x001eHL\x0013½aÆkaÓÜ½ÂK>ãqñSr©\x0012\x0006cÄ¬»;*o\x001aÁWlIÿöá:êT¢¸ÅXxÖ`*\x0002®:\x001bpÍ\x0019UR\x001bà¨<R|- ÜóÜý\x0007Fº,ø\x0017\x000féæ¢¥÷»ªt\x000e+Y½3\x0015\x001dÈè\x0005iÜ8A%)_\x0004ÌÉ\x0010OÆçÐÀ¾¬pkÆ¦1á«¯ÿöúç\x000fyó!ê I\x001fé°(Fó¶û\x0018¿zùøÇÏ^|îÕG±á\x0016\x001bú°å¡\x000fµèpj²Oûý°Nlq-ú°5xÖ%m\x001cfHú
L;$Ì»µ\x001cNp´\x0005GnpëÄl7\x001cé\x0016´TÆB\x0015®\x0015NK[pÉ\x0005[É¥¯\x0003 vi7àHýv_ó\x0003\ÞËNpAÞËºåÂ#OkU¿ê}mD.le­ø°á²noÁYN;ÇJ§\x0002ö+Æ\x001c¸º\x0005Wàhòõ82´Ú2Ê´;\x0007Ih[pÍ\x0007<æuËÁ\x0000Gºx\x000féQ|\x000f¸Í:\x001dÀÁ.UÝäÅ¤+óí9UEW&\x000f\x001dX~ð\x0011\x0004Ä*Y\x0013Ae\x0001\x001aß VpxO³²\x000b!\x0008ð1\x0004¦Ë\x0000Æ\x0018d®¤èè\x001eÙ\x000f\x0017:C\x0011àã\x0008¨E¡êîî\x0013Ãv°ÛâDg8\x0002|$\x0001-ËtfG§¯´¥\x0004Ñkêèî\x0019\x0018v¡3$\x0001NÀ±'ô$/¢\x0004;åI\x001dý}\x001dc\x000et%ÀI\x0013\x0015¸\x0017zµ]Ð9fÞÐ#¶»o¶ÞÎð\x00048\x0002öfx! ç\x000ev\x001b²à\x000cO(ºË\x00161]v ¦\x0001¨N»s$\x0006'ÀI\x0014X\x001fÃvÊ°E±M&hh\x00024Q¢\x0012&\x001eÁS(Qh\x0002Ê=Úe.t&ÐyàÅ}²´¬ÖÄ\x0007UÅrI\x001dÚ{&þ?æÞ.É®ãF\x0017J	 ÿ¢JT\x001d\x000eTðGqÏyQ¨j\x0011\x0014iS¤ãóÔÓè×ûtz\x001cIä&Ö\x0002r¯Ü«XÜÈ\¶ew[ònYý\x0019+\x0013\x001f\x0004>T\x0015Ëã +ÁR\x0003wÏ·	\Ç\x0012`d	GÚÛV²¶AUÓ\x0005=tpÏÜ´	]Ç\x0012`c	pAz**Ãzm]Omså½Z&t\x001dK%\x0008ÄÓ\x0011\x000f\x0000ÈpZä¶b»{;dOè¾(©è:?\x000cF?\KVÛBÊ.èbÐ\x001bÑ	t¾\x000e¾.Ç¶È»^Þ"ÑIÃ6\x0019\x0012cçMÐ\x0018tòz¹õÂ²ð³Ð$*ù÷
d\x0003àúÌßvakØöÈIà¤\x000cÖÄ+½ÞÛ1n@×]	´]	ð(;\x0002Ïå;¹° U\x0013¿ßíjD×]	´].ÈÎ£à×=®	ö%Ï¥Ø]	´]	¨Il\x000bëPeV>CÕ°î\x001e¥l\x000b:ê.\x0005Ù.EÍ\x001bøI{ÍÄÚ¾¨\x0014\sÅnîËöók-ñ4uY\x0018PV\x0014\x001f½lM\x0001¡Õ\x0013ïm"·ÐÅ9F\x0008V¾\x0006Åë\x0005&m\x0013\x0011Ø\x0008A\x000f!Þ£¦{\x0011Èúÿ°¯Ý1zd¾ùðùÝÝßn?þrõÇ»Û÷W¼ýüñïÿ÷\x0001g\x0018WæàåÈ²ÿ\x0013@ëÚ%u×äç¯ÞüxýâÛ«?Þ\?»ú#W/@\x0019¶(Ã\x0000Ê\x001a#Ë\x0013\x0001ë·ËÞæzL¢<\x0000dÜ\x0003 \x001djSh={ÒPëMV±K$\x0007Q¦-Ê4òÁ¶ýò\x001e§uiýàE_[b7N32oQf;ÊPÚm®'Ô«-u¿d	\ä Ê²EYFl\x0019¥\x0014¹|ñµÿ¬ÚR%Lë\x0017·åfi¢[õÛÍÆ¬Á¾¼]%¢^éu\x0012
ÅycnÖ'ºUÂÝnMÒ\x0010;×XÌëÉÔÁúÒo±\x001d	\x001dL\x0018±&i¬Í;VWä³¶Í\x0017,ó¾h³OÑ­*îvc6ÝH^À²æ+\x0019ôn1à È{ü\x0000ù\x0014u\x0004oSòbK\x001dí£âË¼Çô\x001dùø\x0011öá!ÜÕ®È\x000eÈzßU6©tµA\x001dùø\x0001ö		dé-¥\x001a¯ÊmÙG\x001d¡/.\x001eðÉ;öñ#ôS³|\x0019\x0013Ëti=\x000fA©1\x000fð\x001dûø\x0011ú©ù´KrÙT[ª r.xÀ¹ìØÇ\x000fÐO½Äª²»,ªòBØüºÿäÐÑ\x000fÐÏÚµN\x0006ê"ë¼ÂdÀm\x001edG>0@>!kÍ³^\x001fjüä1]8\x0000fG>0B>õj§(ÃåÑêÕ=éÖ¾z©æ\x000f&tä\x0003\x0003ä\x0013RÜ»Þ\x001fPLºn8óî¯i\x001dûÀ\x0008ûP-"\x0014CG³ìQû¢2ø\x0003`vì\x0003\x0003ì\x0013¸ÇW®\x000f$It«5[oYî&á\x0006avü\x0003#üÃÓÒ2\¿9	LNpe8ù\x0000\x001dýÀ\x0000ý0Kêx7OP«gW¹#|QÇ>0Â>,\x001dº~ñ\x0008ú"YÓ ]f
\x001cpË;ú\x0011ú©!4z'§0ª-Q\x000f&ïº\x001dýà\x0008ý`f\x0016â@N\&¨~qJa>«Àp¸¿p\x0005É{1Åej"grìØ\x0007GØ\x0007³Ö\x000e8ö =º<ïL]h\x0010fG?8B?¼|W¾xöÄ\x0013\x0005Ý±{]ÿA\x001dýà\x0008ý êPHºí&{OR.Jæó
ìè\x0007Gèg]\x0019ITkjV¡º\x001cÙÑ\x000fÐ\x000f+©\x0012î-Ë¾MN$\x001f\x000e¸A\x001dÿà\x0008ÿ¬ÒÕ±\x001fE\x0003¸,Þ¨^¦\x0003>zÇ@8Â@vD\x0017:\x0004ÐÂW
Þ\x0004\x0007\x0004ÃØ\x0011\x0010\x0010PºÓ*²úHÑhXÉÜùywD\x001d\x0001Ñ\x0008\x0001\x0001<\x0012§	¨÷Üi\x0017*Ï}Ì»#ê\x0008F\x0008( \x0011ðt2µw<å\x0003êZÔQ\x0010P\x00108.ÿ/Öô<q¾\x001a3ê\x0010MÍ-æQv\x000cD#\x000c\x0014\ÓtqIÚ¢ói7xê§W\x0007aöo?#\x0014Ä³ðë\x0005
ÎÉhµ&êÑLyÞiRGA4BA¼JqEI_,<jù:\x0005O-¨c \x001aa \x001fuÜ»f¸2)_©Û=ã\x0011\x000f+Ô1\x00100PMÎÔµÇ,OvtïzÂ\x0003¢vê\x0018F\x0018+E2Ê´ÐáÊjì\x001e\x0006Qv\x000cD#\x000cDNvØ\x0011Ðd{±HpÀý	\x001d\x0001\x0011\x0002ò§±Í¤ºÿÕúd\x0011OBÇ@aP¶hÖ\x0008.)J\x000f:\x0014à
Bè\x0008(\x0010×Ý³ËéºÚ¬\x001aSë\x001c\x000e¨
Â\x0008\x0003aS\x0015\x000b¨\x0013M5»Ð5Éûy¢\x000c\x001d\x0003\x0011\x0006rQ\x0003¨æéRCpIë1\x0011hþÎi\x0011§ÉÊ;«Õïälz\x001dQùçèÐ9Í0â4\x001dª\x001c\x001añZS5ÔC9à\x0006uN38M(ÍÎµàÈéÑ¬QÇüÑ×#^Ó%©XFñ%l_\x0014|E§j\x001edç3ãÏä´WðHJØ\\x0012<À/#¾\x0008PÃLJ-ýÑ«\x0013`>,#C(kÍÅS¤y§:"Õ 4Oå±\x000bãH(\#vÕ\x0010¨9Fh\x0011»\x0018\x0013qÉcß\x00085\x0012
»¶y\x0006iãVcêyeú\x0003¾yçÕãW÷'òjW¥rmØæK[±óqÄ_úEõx±fæÕ³:¢|@#u(x"ß*[Xó
\x0007þH,\x001cÂ\x0001yìäÅ\x001fñ/¿?å\x001c*1¨)µ5lmQ>iÇDv\x0007DrútV4üdFZM©[±¸³Gj°Ëáö\x0011é\x0010Û5Ð]]Ð=Ê7öN*\x001eQ1\x000e~Ö¡E\x001dÝ¥Ð\x0016\x0001pvÔRM÷UÏÑB\x001eCKYNñÕ·
\x000cZæv\x0007Ü0\x0017ºí\Á¿Ýµ}¬ÝH\x0014ÚÝÊ­\x0001í¸v\x0006=AlûûB\x0004\x000eWäaK2\x0011\x000f(Ëçþzæ	þj÷\x0004¡µïjWçÛ\x000b6\x001dðhäv`Ð\x0011äå>-5óõ\x0010¨o9¢»¼õç3³þl7k­Ü\x0014u¢5»&è\x0008*Ø\x0015\x0007íúOyàÌ§Nb×7CÏ]êqÝ\x0004©\x000bíñpæùÝéN¯;ý Ú9×¿þüñÃÛßî®\x001e×?üÛO_ÆxÍ ìGCÿ\x0008×SZ3Sùö>úóIµëï¿yñüÉË«Çõ\x000fÿëúÕ×!Â\x0016"!°>taÎQFÕ\x0017GA\x0008»·v¸Ev¤»Èi¿1©ï+ôc\x0000ã\x0016`´\x0002¬>²-g\x0015¶5¿#Ôgl\x001fé|Ó\x000e1m!&3D¬Ô\x0013Å­\x0000Zo36+\x000fÖÙ!æ-ÄlÈ\x0005ïxúÎkñÕ»\x0015ânôß\x000e±l!\x00163D¢¶È\x0015sn\x001fÚOÅ!n´bÖewVÉëJÆe7ëê\x0016kr$\x000eÜ\x0015>~jÇØ{E³[¬pd²æÆI^`8n\x001338ý¥}ç\x0015½Ù-æT¤\x0015[õN³¨1íÛÙ1v~Ñ\x001dcË²÷Õ^&>yú³¨\x001dýô¥ÞhÈk\x001a2\x0016ïÉÑ\x0007Ñ\x0007ª\x0018U°ziüÅ\x0018:aäÊ¬³\x0015cÔ4µ\x0014ãNÂ±óßÞîÀsÑ ,<Ý»zÇÐü7î\x0016ñÙ!vÎÑ½cqQÄ¿Y\x0006R3\x001dÞ¦\x0018w;VÍ\x0018¡ó`öÅ')ÅV\x0016-rD¬=Ì{pè¼#½#c\\x0007\x00141ÖI¼Å¸\x001b·cìF³{,XxéÑÊ2Yt?r\x0014=J20M2ÐyG°zGb":,Ñ\x000fC¬YÑåù/Ý9G0;G\x000eÅ\x0014¡×é¯è4â©2ÿ¡;ß\x0008VßH·Ð¥\x0016N¬«Õr"}Qs9\x000fÃÛ1vá7ãïÂzGr\x0018³ÓAó¨
ÎÞïv{Û!vî\x001b¬îûcÆ.þ\x0006s\x0000^*
f\x001c\x000bY\x00173N\x0000ÕK=±ã\x0018°r\x000c±\x001cw+\x0013U,7§¤zÜG8\x001eì8\x0006í\x001cSÏ`æxV=©\x001c[+{½ÖÓá\x0004v\x001cV¡\x001a#®ï\x0012¡ICY\x0006m\x0016ve·fÚ±OûÍ\x000eÜCûÖ\x001cI¯Fãz¯i«±óàh÷à\x0005Úá}kX\x0016Nsºù°\x000c;\x000ff\x000fîdwB
'PdÎs¦\x0016ðLs\x000cvþ\x001b­þ»þêeòpÉ°×5T+(-×:×Õ±cì\x001c8\x001d8\x001fFÉµrúgÒ~Ö¥y\x0016cçÀÑêÀë¯¹9GÒ¥»9fÆù¸\x0011;ÿfÿÍÎRAa3Ê`
x63N_\x0018êü7Yý7ÕW\x001eÅyQ¾¦\x00167¦8]Í£Î}Ý}S\x00109Å\x0012ñäØÂ#ÌØ¥\x0008dM\x0011ª\x0019\x0008,f\x0014\x0001Ô\x001e«\x001d§#u\x0014Cv:@¾\x0014S$«®ÿ\x0016NLS5u\x0014CV©¡#È
~ëEs5tÔg/eØQ\x000cÙ)¦F QÓ§\Nftó\x0018;!;Éð¨3¶g]!TÍ¨Y®ÌWÀ©sàdvà¬ í6\x0011øze¸É¥ÙñbY§¶\x0016ÌT!ÍR3ËZfæº\x001eh}ÔêzóÏ2ù\x001cj\x001eAÊ²äú:*¸A¨ëA«\x000f8à\x0001é\x001ci\x001c@r\x0016-2,ÎéKq½]ñ¸\x0002Zýüî>}~þÅZÖ%Vg\KÏÀ
ykYW\x0007´}e wnÔÊåf«\x0012KFCYi(6\x0016OÆvW
\x0007®\x0014×õZ \x0016U3ÉÔ8}¾D@°3)·ÂâÌ5^Op×w[a\x0006^µÏ\x000e\x0000Åì½tZ/E~ñRD:DãÝDÔ\x001eÝY@ý[\x0004®ÿvWÿª«\x001fn?¿»zzûþOw{ûþ¡\x000cR÷#ÆÖÍ\x0014£´\x0008`¤®éúÇg\x0015å\x000f×¯^=½~öÝÍO}\x001d"l!\x0019b\x000eÒ\x0018TærF×ÆjDLÐ¹¥1¸Ef)I[ BqªÄPÿízw0d?\x000f¶\x0010ÉnÄÜ\x0008¨Ó(1èwN®\x001a\x0018¶\x0010\x0019bL2Â\x001b\x0017õ\x0001'\x0002\x0015±â¼
ã\x0016`´Û0J/\x001d§@­B)K\x001f0öOÛc\x0008Ó\x0016a²0®\x000bµ\x0011*@r®ôà¡¾ù·\x0008óÈeL<Ç%\x000eATY\x001f>§!-Äb7bxäV~a}y	£ÊÛbp4
ñÔf±xmg÷8 ñ/¯wâ\x0013Ômw[+Ç öÄbgÜº5ð¼ºäY$ß¦Ò\x0005¾c\x0018;fñvj©¬¼J;!oÈÍR²B¯»àôö\x001d·x;¹ðCÃZúó\x00194ÒÊ,M3
±ã\x0016o'\x0017VuJÂAön×\x001bS\x001aÿuzIc\x0018;rñvv	íÉÒK­%zõpþÊtüâí\x0004ÃO`$·Ú¬®,­·º«\x0007aì\x0018ÆÛ)&$ÞÆ°Ø±þ©È¼DíúAó,è;ñv­>	ÕQº\x0016IÈqì\x001b"Ç v\x001cãí$ÃÏ°+D*OF×¼#¥éã\x0008\x001dÉdª\x0007¦\x001f\x0008Y[\x0018¢Jw!oCÆØ±\x000cØY&´ç%N`I;Ad?
\x0012y}þbgPôÊ\x0000z\x001d^nÛÂj`¿êÂ¿¸
F1v,\x0003v	S{§\x001aAH\x0000Ó$\x0003\x001dÉdxóú£\ñßîäwÊ´ßc`c@\x0006k©(TíDç¡Fg~Þ\x001dÇcHg.\x001fäÂ´\x0005§Õi\x001ecÇ10À1 Ït®Æ\x0013N¿5HtKîKÝq\x000cØ9\x0005Ä×KíÔò0R\x001dÏtÈ\x0003\x001dÇÀ\x0000Ç¨\x000bºdwW5£\x0014É9\x0019®í`Ç1hç\x0018nBùÔI\x001dO(íZ»4}­±ã\x0018\x001câ\x0018Édê_#ÚÑI±\x001f#¦£2ì(\x0006í\x0014SÍ(=\x000cÞ\x0007în_ÍèõVÃ|"}lb²ö9;÷\x00163Ø<"¿)ÎBì8\x0006\x00078X«ýÒYeÇOfÄ2ïÀ±#\x0019\x001c(\x0015éÚ\Þ\x0014µ:!mIËvi\x001dÇà\x0000ÇDQo¯flÒ7A5âx\x001ehÞñt\x001cvI¤5[G®E< :LWÊ°sßhwßõ\x0004\x0006aAäC£ìpÇ\x0003ê¡Ô9o\x001aH\x0010t\x0017GE\x0008Úª\x0012}V#RöÔ9o²;ï¬\x0013¥\x0015£o$ÒT1Î?pPç½i \x000cy|fÁ\x0008¨\x001aÉõSbtÓñ\x000euÞÆÊPkàxR[\x0018­M`÷;Ô¿q\x000c<r8I\x0011\x0005¹Z>Q§ï4uÎ¬Î»þZ´ÂÃírZ=IÍ{C&Aê¼7Y½wý5JJ
ü:(}\x00001&=>ÎßêÎ{Õ{óQVÐU;BKû³Ó[
n:Þ¡.C kP1ên·jG×J<)*F?_¤§cÈÊ1ËÊúB]1f=:!Î{§ouèX&XYfí (+Æ\x001c\x001aËdTó/¡#`%jÆ"¯èë§cÙ|êé¸1t$\x0013¬$S1ª`\x00010ßHÛD,jÆ|ú8ddÈ\x0015¹.(´ç>%}ët\x001d;	V¡\x001a×qegÁ\x0018Ûcr\x0012ó@v¡G7§Ì¦c94¢¦Y>ûép"t$\x0013ì$PÊPPÓ\x0002UHAó~Ó\x001f:v:/µOEªPê¹'§¢fù\x000b\x0013»\x000b\x0013Í\x0017Æç"#¤ÔªP¹h¥Ì»ù\x0008<vÇ1ÚcÑEãÀk²äÉ¿\x000e*ºBó\x0010»p"Ã	¨á\x0004\x0019}Qñ¢-eaæëßÎDÖV­¿{µ²\x0006=Ü«%*\x001a§À,R: gÛø¶öñð\x000fö¨,\x000fp51lí	©µòÌ{É¸C\x001a\x0007 \x00128Ç]Ë§¯~äpêûÑÙdä`wÙ9R\x001c±iö,\x0010¿>\x000e\x0017Q­º¸\x0002£; n_ÎB\x0019A\x001auåO½Ü #\x0003õ
µ.Ný^vNJø\x0003PYRE\x001el6õ>ÐWXÿõ¹¯³ùImJøü¼Ôª k£IÔ@8H7(ì\x000c
#\x0006
E\x00057ú·N¼ü­óëÏK;¨i\x0008jqeÑW&í\x0008qq:LªNÿSïô?³q¯½5Õ­>Ò	ÏÖ/w@{îî*
Ý¤Ü\x0005\x0018'éØ±ó\x0001õî\x001c¨wCäTì+F\x0015¸jR*G\úÏ.ýÏÖK\x001f½\x000cA¨Ý\x00179È¬9ú0ÿà\x001dè$)ÙÐ­õ|òÈ¬\x0004ò,ø¤:\x0017ú\x000e
éª\x001bn§F¤~É¿X3à¨O¶ZV×ÄBZØ
ó\_¡þõóí\x001e­üh½û¤­Õ+µº°JÚ ¿G\x001dà¡~î=õ ÖøFdfyLGÛb
­¥÷\x0010³]}\x001a¡þ	El·;¬\x0003gu u.Ã·iÚ¦\x0011Yr}þÓßöÞ|ù«ÿL(£\x0019¤ySýòòéOó\x0006:s¥d?¡él\x0018&èÄ\x0010i±aÂÙ=
\x0003\x0017	Ó©`\x001bLÎnµð>ÿÍïóO£î	\x0004ÏXïU\x0014¸^ß[â\x0001-0ÕªoÎ¬j
]kx\x0013/¸Y?¾\x0016ìí;Þô7És{\x0019Î	mn#êüPr\x0007Läs·GÜRMBÅ+ÕxOsPõIügó·ýÓÙm7GÌ¼>B*À\x001cr,å®qg#wõÍÈÝ\x001f?¼{ûáÓÕãÏ\x001fßÞ}ÙT¢Ècåô$\x000b$¢\x000e\x0007_î¡ ?>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=r9ÏÑ|oþõâÓÑ\x000b\x0011\x00043\x001e`3~~}uÿeáô ïP]´RãuÆrç\x000fË`y\x0019úùñÑÙás2*áT\x0007ß`û 7¤8\x0016ªnh Ó%î¢¦lMtÆS9r;7Ï.6À\x0012ÎôÀ¡²,{dÉÃ6Tàêè!\7-él\x0017\x001dä!\x0010Vqå</p><p>2ÓÍã\x0006:_Òù.:ËU´ñ\x001a{\x001dòTw¹m \x000b%]è¡SùaÃÆû²%¹X`}ý¹|Êr¶ÝÀÖÉ.8É\x000fDÆ»¬Ã'Y¯>èV¸\x0018Bùå3º»ëëô\x001aúYÆÁ#dµÈ\x0003RlØ¥]k´Óã÷:\x0019dÐC¶&\x0004\"Y\x0016UTóÓ°Mlº-FT
\x001f¿"KGYÏ÷u\x0011E/-Ùl\x000fÌÉ-°»)¯¬I=\x0015þt²¹Íu°Åp\x000bv	`Ely«Ðóg²ål¾dó=lp@*eÊæyÛ\x001d0óÎäÅh»´ª+,H\x0013°4\x0000Wë<IÂ\x001a.é\x0016vÞâÝ°leÝDZ:®èý²Ñ¤ýµ\x001b
é?­RM²&	üV\x000c#ú>D\x000bftthT0c-äM8/\x001dÑ«Y\x00125\x0017ÈS|¸|º¿þrµ9»ü÷Dó'SØ\ÀóuYúÍä*\x0005fæg?l/Î\x000f6gÛ\x001fâ/¯BB		\x001aui\x0012\x0007J4¦z\x0000\x001cåâh¤T%¥ê¦Ì½Öéô\x0018fp>\x0007Cú!F]2ê^F/wÃå\x0015Ý8
xM~îJ\x001a!M	iz!ÏAPj:B\x001a\x0016\x0018_,\x001b!m	i{!æa@6xA2Áä»{?95RºÒuSJò3NhªrÜ ¨öæ6Bú\x0012ÒwB\x001aá²
SYöDéØ+)Æ2¡ÒpMñnB»ÒeÕ#9´ÓF¹\x000b*&{.z1Õ$Ç\x0015x,ÉÏ\x001b9\x001a\x0011kÓësL°\x0015S*Ê\x001c¯ÅJÍÓ£Ó½^Ç¨B<\x000c¸\x0005LHÍ£çUçj\x00069dÓê_.¯7?ýÏý÷éý¯®\x0017Az\x0015\x000eR\x0016cmÖWÐ\\x0006ä*	¹Ø\x001eoÞnNÏ¾?º8^À§J>ÕÇ\x0017#]¾ÆGwÚ­I¢p\x0011÷«é'Ô%¡î_ÁôÓ<TWyá\i{ZùLÉg:ùbÄC_Ø*zK°ÚÒVáåÈ\x0002ú\x0012Ðw\x0002\x001aÅæ\x001bI\x001aâ </a%oÜHX¨«ÉtÕêB´\x000e¹Ò"Æ\x0000tÕèx\x0011ú¿±¬N±ì=ÆÀæÄ\x0017#\x001eÊ\x0000ë`ù(3°Õ)Ç\x0004\x000f2URÉàØ\x001aÆLÆ^\x0013ÜZ\x0011mh{\x0011ã"²­Éz(8P\x0011m?auRdçQ	"«\x0011b7½eAJV®±c\x0011¥]\x0008¥Î\x0017Â7W÷¿\_m¶7?Þ_}ùeYv\x0013jÒ¬tK7u\x0016Èr0×Í|stvþþøh³=ysvtøþ4'³BÉ</p><p>#¬¶edÍ%\x001aòH½±»í¬ªdU\x0003¬(^NÝcX\x0007MFhFß\x0010ÛQuª\x0007P\x0005Ok°\x0012o7\x0014WpeÛ+ìlG5%ª\x0019B¥%u<\x001bD<ûLÍ%ÿÛAm	jG>¿ÌÄP¾¿àbT§æ¹ Å¬ñòQ_\x001añ\x0007¼4òõVA\x001e+rx~½Ìâ*¦}Ä\x0013Ö_ë'Ê¡$\x000c}è"S\x0013\x001dJP\x0007\x0017h\x0006´eb·\x00150+\x0003Liè!Ô9e\x001fP\x000c mKovµkeërDáêçðø\x0003\x001búïï/ãÿ÷õÃæ»ÇËëEzQ\x0001Õ\x0005-½cám'\x0015 X~Y\x0017ÆEúþlûñðôøóæÓóíñ\x000bQ\x0019\x0016JX\x0018á9Ï;MUÓ\x0013,¿VyÊ¼U¬jha=+ù\x001a`\x001drg=|u\x001a|\x0007­.iõ\x0008­Ô6\x0012­çú\x0019Ë\x001a\x0012æ=d\x001d°¶µCK\x001bO?íY¬n]\x001e$\x0004ÂôÒ</p><p>p³ð$þ°+°}Ø\x001cþru{õï×ÿß÷W\x000f_Uî»O÷?ßþåwgW\x000f\x000fw·ßùè@ç×¨=åe´\x0004IOíb_æáèóæðýÑÇ£\x001fPíóëÀª\x0004VãÀ\x0015A´QË´È\x0011\x001b}\x0005¾¸\x000c\x0012Ø¬@l\x000ehI×\x0013\x0004æj$¥ç=ÍÀ®\x0004v+\x0000+|Gâ\x0018\x0004¤C\x0017Æ	Ø×¤j%ö%±_a\x0017[ºEk\x001b­À»Ç\x0004íçíZég®\x0010Ï\x001a@ÖÆhTz5.!k"Öb\x001e\x001e6\x0013ËX®°-$½\x0018jç>\x000e¸-¸C2ÏQäÊ¸Éqë5ÜI\x0003\[EÓn4^iÞÉûRÕmÈP­2¬±ÊÿèÃ\x0017B\x001cÂ*&9Ðé\x0013")\x0015££­\x000cfO7e!1¾LÎª,cµë{ùáêþ§§Û%®9¸@ob8\x000c\x001er¦7	:nþ\x0019ùÑ\x001fÎÞ^||Ntº\x000eBöiÔ	\x0011$/</p><p>\x0003h¦D3­h8¶Æq"¢Ñ}ÁGÓ*¿\x001a\x001f,³%í\x000bÊS£
åþ?/5Å²BÏgÎ.ªÚrª\x000e&E\x0018mO©]¯¼eÛcçvËÒ\x0015E ´|úñrF¯çiçé@\x0015\¨2AI½\x0017².\x0014³¡eø\x0003ÚO×W÷÷\x0018__=Ü^.ªæ4w¼{~ìèÖe½\x0019â§hUÎ0¸>úüqûB
7sªSus¢f\x000bi\x001d`\x0000c\x000f,Íáç\x001a­¦ä4ÝÆrùB!ñt³\x000e6ëGìér,ä\x0014rVa?ð£öëË§\x0016½o\x0006-,·{Æ\x001bUx9¥Cì\x0006ÚãíÅÛÞ6å¼BN\x0016\x0015rMxØkLÏ¯Bú,Wå
òróqÄ
x²Â]x^lâ¿
ÃDG%IqñæiçåpPÁA\x0017\x001c\x0007ÓÚé~\x0015Aì<D\x0003ªðT\x000f\x001e\x0016\x0011àDtT$°Ê°NWtºÎå£\x0010FºÝÂén4S¡.´Å£Xi9\x0010W®\x001fÏVx¶\x000b/ËA\x0008é0\x0001ðvG\x0016ú¬«ð\\x000f^²&çyõ@æÕn<_áù.<ÇÊd\x0002+\x0011Èà\x0019êÒÄÕ¿\x000f,Ç«¼ìq\x0017Êår\x0018\=å\x0008ÏäS;Ï°,ÇÊ]@»p¹×\x0006WOÓÁÅÁC¼zÝ\x001f\x0017*w\x0001]îÂ	N±</p><p>¬Éâ;gÛýq¡r\x0018Ðå0, 4XøMùê\x0018ã³;sóð¯\x0001¯r\x0018Ðå0PÇZæÕK</p><p>W\x000e§ÇäÕ?ó-Ç«<\x0006ty\x000c+vfÙP\x0011µwKWoþ\º\x001c¯ò\x001aÐå5,ð6\=j[9kç]¦
tÓ.§aL¶ÊjNpYÉº½båtÏ.a\þ´qí\x0004[%³ÏO\x000elÀ«|\x0006tù\x000c\x0003»@O¾Q\=­òêu\x0007zPù\x000cèò\x0019\x0011/ð¹uØ©Ix.¯^÷¹UÏP]>C\x0019¬>M«\x0007TèP\x0015ñæÃ¿\x001að*¡º|öùãÆÕ\x0003rirwA\x001bX½Êg¨.\x0015Æ!¯\x001eÉlçÚ\x000c
pÇP]\x001eC\x0001çÇ+=¿\x0012`óýLu\x0003ªò\x0018ªËceu<\;Ö¶ñ>ãÍç`5àU\x001eCuy\x000cØõöãk\x001a¯È;¯ÿÛV\x001eCuy\x000c\x0000\x0016\x0006Â»·%é"\x000fnÞzÑW¹\x000cÕå2 Oñ\x0015ú"Ýîv\x000býF¥ò\x0018ªËcÄWyñXë(ÄÔ»ÙWy\x000cÕå1P\x0007ÃæÅãQ\x0014Üì*¦Ö¹N<]y\x000cÝå1¤Ê93Éª;É'\½n³¢+¡»<F\x0001Î«ÇfÅí\x001cÚ¼m¾\x0001¯ò\x0018ºËcÄ{cÎ\x000f°P­\x0013VC^½nºÊeè.!²â@ÜÊyUÙ¬Ì{\x001bð*¡»\Ð,\x0016\x0007äoÍîdÌ'«6àU.Cw¹\x000c<­»Õ£¨09åheÿÉ¨|îñ\x0019\x0010\x0002\x0015_NÙ\x000bÇx2Üù³z\x0003^å3tÏ\x0010;\càÃ\x0015ÍJÿ±­\îq\x0019(Ä§óÒ<n$\x001b¹zX\x0003]å1tÇ@:ËîV°&âå/;\x001fD¿\x001cÏT\x001eÃôx\x000c\x0008Kþ§ÄO¢S!Ùþ\x0002S9\x000cÓã0â55qß	ü´KKÍ_&\x001bð*az\x001c\x0006Î[)ò>WOí2¶ýß¶ò\x0018¦Çcw\x0007w^\x001eµôæzö
tÃ0=\x000e\x0003<ìx\x0001Èo\x0019\x0003énS9\x000cÓã0ÀgÕ+\=\x001e}åùÓù\x001c\x0006ºÊ_.áìÎåáVÅÝ{Þ)ßWù\x000bÓã/À¿\x0010lU ßÌ¼`¤®r\x0018¦Ëa88Øå-ø!õ.ßØOW9\x000cÓå0°§ÉåµüiÍnñº½­­\x001cír\x0018Ö³Ü6ªÄÐKA<ÁÙæõçºmå1lÇ°ð4¶8\x0006Dvhf®cÝWy\x000cÛå1,ìÜ­åRö©\x000cj8_k+a»<å©ËÓêñ´BLÇñêu\x001f
[¹\x000cÛå2LÀØWOÐ\x0004Î`wÙîî+­\ír\x0019øÎ²Û{É\x0006\x0017¯ÿdT.Ãv¹\x000ccò\x000b$*¼Óp,\x001fü</p><p>W¹\x000cÛå2"^jÓçs_W\x0010ÙáÎçÂ6àU>Ãvù\x000cE!põhÊ\x0000NÉ«×MWù\x000cÛå3PÖÎRå
&çUÌ|àÖr:WÙd×ecè4¶	\x0010móÁètMv]6Y\x0015\x000eW±\x0006D°"?\x0015ìu.Ç«l²ë±É\x0012¿hªÎ\x000c8#ú	\x0005ë\x0017XÓÿæ*ìºl²\x0008»0^vAÈý\x0000Öö¿Ì»Ê$»\x001e½·\x001ed¼ó·fàÛV6ÙuÙäèÅò3Îß\x0001ò\x0015­¿ÐU6ÙõØdìµU´õð&¶\x000f2\x001fÜþ·\x0002WY=×cõ¤ãÇïÉ®$=pë=äX¯?ì+³ç{ÌtÜP=áQCµwÜÝÂ</p><p>Ýx]ñ]vÅòë2ããqægÄxmÞrÐW\ßur1Öó\x0019/ÕsYoËx¥Ð\x001b§¼è¹\x0008I¯¸ß\x0017sSÒðáÈù\x000bè\x000e÷\%AIkû\x001b#\x0003Áê7HIê¬!\x000b\x0008EûÜ\x001f</p><p>sÊx\x0004;)ÿañK=åT¦rï.H\x0015czµ«ø¦ñ\x0003ÒïJTûRZ1</p><p>(&]åO7_®6ïïî\x001fïnt\x001eOÙ¢De±q\x001e&fÊ\x0002ÈO'ÛÃ£ÍûÓ³óÓ\x0017Z\x0019\x0010J@è\x0006¤ÔÆG2 añg_ví6\x0013êPw\x0012Ê,Ùê KÝû¬\x0017\x001cÊ|óbÂøW¬?2Îqç\x000e¶Ý ÝÏ_~ù«ëÇ¿.Ónµ2çØ°\#¤4\x0016\x001e jáÐ{=»)»\x000fßÿ¯£ãó?¾$äÊÔPRïO)o¤\x0016Üjnºc4?\x0011FôõñÌ-Äª$VÄØñÆca¥ÎZ	YÄ\x000e\x001b\x001eW¡Ö%õþ@õÆuF;J\x0005\x0015ß¹\x0015\x001b|ö¼{'µ)©Íÿ)kmKj;ºÖ</p><p>òZKV#r1ºãAø¬r\x0012«ÝÓi|f^w\x001b¼1>¤n\x0017¬ "Cm8ÁZ°\x0011x´µÐJü¡Ô¬8»º¹þùúêéá«íÆ\x0015otc\-·'º\x000e»¬Uáõ<OÆgG'Çï.>¿ÔhÌ¤º$Õý¤»á ]\x0016í\x000fÜÄí¦%ºÔ¤fÔp\x001d,Hu`HL=d\x0011G³wìJ5\x001b\x0013`×wvýãÝ"½"ã,;
©¸S+E0ç2	gÇoN_\x0010*b((¡ \x0015Ê\x000b.ó1|¥j!­9huvna\x0017R©JµR¡tW\x0014Tæ¢
+ø9??\x001d\x000b¡t	¥¡¸µ=Rå®5ûÂÇ÷\x000b©LIe©ò\x0008h£Eé\x0003æ\x000bð4È­ÊT¶Ê:v2zCK\x001dòÜª½4ýËTñ.9Ü\x0002¢O¸¹Ü\ÿø÷¿Ý_>^ß-\x0011*ð8ë¾¦vò\x001aÂó¨X=/hÁÛÍÉñ£³íùñé×Æ3«*YÕ\x0008«Ë\x0003Ý=MW\x0016Y8JÃsÃ\x001bÛHuIªHs±\aìv`\x001dµ8I½7ª¤\x001dÖ°v\x0004\x0016$ç-C~C=>Ò¸Ó~>¾\x001dÖ°n\x0004ÖæiHñY/TÝÊÎ\x0007D·Ãú\x0012ÖÀ</p><p>àr1Tc\x0005%áXMÏ¯ÛYCÉ\x001aFXuî\x0012ðyn§\x0015×^Ö¦µd\x0003¢\x0010\ê[Æí\x0004#IMÀ\x0004Í;ÖÀü\x0001¯\x001d\x0016*X\x0018\x0001\x0005Õ½\x0005TMs0¼å1Yfo0B;me¹äéÒÂóøïÑÞ*\x001eã+ö\x0003ÝVÚÊtÉ\x0011Û¥q®\x001cí\x0004\x001c)äý§\x0010×vx'Tæ@Ø\x0003%s3	jv$sà¤ä æ
ÿÍ°P1\x00189cXÒG=Ø!Í°Ä8ªçc"ÛQ«\x0013\x0006#'\x000côn\x0017X/n¸×>Âîëñ5\x001f°jFS:d>OÏÎÕ¨«Å;×;Ú¹<
É`Mëè9Û¶£Ðï\x00154\x000fGZ\x0001\x001a`\x000e
0\x0006
\x0010ØY8Aú$&þ3\x0008=/)_Ì,©Å\x001f0\x001c?¼{º.ï\x001fî¯¯î\x0017]Ü§Ë\x0002µ#EPÅ\x0005¾ÁÈr\x0004ÈáéÅÙçéæþáâìøèì[;CB		½&§|q\x0012/%âË(\x001bC: U	©ºW\x0012¨P B:\x0017'JÉ@({\x001c:(uI©¿Ñ¥4%¤é^J«âà®j/¤w²\x0010Æ(mIi»ÒrÞ3Þ\x0008\x000f¦µä¢$'ËÒ\x000eJWRºnJ/Ò¼D\x001b |\x0019¶vPúÒ«k\x0019JÊ0pÄi\x0018ó4³(ó#³ëZI\x0011ýÂâEeWS32×\x0014¼¿º½¿Þ¼¹|úòË\x0002qvT\x000cô,dcågf¯5H?ï\x0004{ôñìxóf{qøþ¥	¾\x0013'Ì8¡\x0013õÙ\x0002P1®\x0017h*\x000er*G#AÎs\x0000- f\x0006júAc\x0010MsW¬ò¦ùÜÊ!½_OZAËð#Ãr\x0000ÒÁëé\x001dâUi\x0003D#\x000f\x0017zx¥çâEÊÅ\x001fþrõëõ-EJî~ºÔ_\x0017m\x0002eY7\x0008[R¨á\x0018t~f\x0014e7@Äûpü¥O§\x0017oñh½ Î.æ\x0019q2â#ÀZsÕÎÔ±JÀ\x001bg\x0002{M	lÆæ\x000b Â¾ÚÄë¸~\x0007KfÆy]ÉëÆx)/>X\x0008\
\x001aiWØ\x000e¡¤
C´Óô\x0003\x0006ö,2Â\ùõS¯\x0000\</p><p>µ&hüahU.þ\x0017,Ú\x0015!WR(·Â:9¶\x0019Æ6óZÓfæÝ¬Ô</p><p>»9\x0006EP¿tÄ\x001f²äìåÓÍæÝåÓÏO×Kn\x000e{\x0010'Ñ4×.î\x0016~\x0016÷{ºO¶\x0017'wÛw\x0017Ç\x001f¿ûrùÓåÃãý×\x0019¡d^Æü¸\x0011/zÓ\x0004Ã-\x0013~o\x0002dÅøê:ªQu1¢º0/|\x0004W¼ç²ÍÚQºw\x0019sBú<Ï\x0017\x000c«·y=/°o[FS2Þe´ü:\x0004àó2:î¨ô~^{ØÆhKFÛËå5¥\x000f´\x0006«¹ÞA¾õ«®dt½ÇAIêâËG-ú¹rP\x001b¢/\x0011}/ân;Æ\x0010;\x0015ÉÅetü©çù²6ÄP"NÄx¦eÔ4ÙÞçû\x001eÎ\x001c8ÕÅPM4à¢\x0013\x0012òu\x000f\x000b(Ï\x000f}MüÔsÉðµéu3øNX2 w¥cs
µ6ÈÊÍÈ>?\x0013WrjxK+ÉÍæq%]^É¡¬l¸ì3âñzdY@\x0005;LzRyßkÐk¬\x000c¤ìµñ°P\x000b&ÖåÓã.«Ex7QiC¬ìµ>oõ\x0011QqL¡r{·w¡Óüyl&ªØìíÝÓ¯Ë*\x0016QØZº¤a\x00141\x001aÓ\s\x0010÷	ß^|x©Æ\x0001U	¨:\x0001
]5Î\x00030¬ÛU¸`þßDhJBÓI¨)­¨ñU²Ýb§­/çµk\x0008ÁÍ>rü\x0001?ò4öð¿ÿíþ\x001aIÿüçe{Ñ*ÇýÔN9R¼²;qS]ýMÓhãáì\x0018Y¿ÿþ¥ÍÈ®ätÝF²x²v82\x0019ñ`¸ÐSòå³\x0003TV ²T;$H=¶\x000f¤P7\x0008&E×ÝGªõìÓÇ\x001f¦ó}wûS¼$^ß>n~½¾¹Úüñîær	ª×</p><p>¢\x0017¤\x0018c79W`§C±EO?¾WÄãçxg<9Úüñôdû:-´0Bkvo\x001eñ\x000e\x0011hxªbá\x0004§ªÞÿ>Z]Òê\x0011Z\x0015²\x0018Zpdä±ÊÂ`gªÐ¨VJ;\x001bü\x0012À°½¹ùûß¨<ù®¡:IÌZ0ä'©ô)\x0013ê|YX¿=99¢ÊäÓkmÝØ2\x0011B'¡Ò\x0018\x0013¡\x0016té±NY\x001eðìÊ;x3¢*\x0011U'"J\x0017¤Dý$?Btç.¹¢fBS\x0012ÞEÔþgQá\x000eÓÇÀIm\x001dk\x0018Ýì¼µ®,|}Øüþòþ§ë[|F¤¿.ê\x000fÃN\x000fºS(lf3ä¸)5ç\x0006öý~{ööø#>'Eä\x000f/u²Á¼×\x000eªV\x000ebKMÔ<Õè	\x00167ð0\x0017é"V%±\x001a#\x000e67xÄ\x0013\x001e\x0013-vKðår¿`¤XÄz\x0018Gô\x001cÖÓÄg!<_÷TW»mIlÿOØ\x0015®$vÄù¢,µe
Iö5\x0011ýòè\x000eb_\x0012û1b\x0001Y\x00105xzvQa\x000e	Ìü&ÕE\x001cJâ0F\x001cCBîhÿH\x0015|Áñcskìã]vÇV5½]ÈÚû\\x0010\x0013£ÄÔRl¦6AZä56²¬]È\x000fkKês2+HGg9®ÝS\x0000ë"®\x001c;{ÚçÖ\x0002oÜ)\x0016Åië2³^d[í\x000b;¶/þÁ\x0006NËùýANºz\x001a{/þ\x000f\x000f\x001eÆ0ùÇïè ¹\x000bS(V6óV|íaì-¾úþ¼V´z6ÞÂ¸X\x000epìkêç\x0002ÅÓå¼_{~\NkJÚù\x001bz\x000b­"Á=&X´!°\x0008ª¯z\x0007;QmjG\x00166^r\x001cÇ>r÷>º[X\x0018ß\x0006®¤?ö7ÑjÉç 
µ,90Àqûê+ôrZ_Òú\x0001Z#a\x0017WZî×ÌùagÇW6¬óÂ&ÖÞ6(\x001ew\x001awªÎÙì¯ÖQ,¦Ýùa¤E?Ü\x000by\x0012\x000cêäi*¢¼kKÅÒNZYÑÎ«Zh-Î~¦×+ëÖ\x0008Å»6¨¯U\x0000-§­\x001c\x001cñ\x000cF+\x001e\x0001IfIx\x0015\x0012ãÛ@U¨óêª¦UæfFÅ¦Ö\x0000G6>ïD´\x000f#NÌ\x0018³[X`Õø¯ÍOêòk¥?Ëq+Ï G\±\x00015;\x0013®"Ie­r­ñÅ­l­\x001c2¶1¡K\x0014ö\x000cTkk\x0004_×*©Ns[µ}¤\x0008l¯>©)P0,Ø\x0016oBÜ{é$dÁ\x0006e-Ðsh=\x0006×	\x0008Ù­9rk¹è¢ê\x0008hB\x0002\UÙ?\x0014Í4uúäòñêËÝÕ²\x00020\x000cÆS\x0002ÍZÔZ2$\x0005</p><p>ÉF\x0014_}²=?:<}¹l
qa\x000bC¸ñRB~\x0018"sf\x0006£P{Ïdm´jF«\x0006\x0017ßË¬1¼ãâÂ/½	1¸z«p1\x001eO:\x00028).O\x0011ô</p><p>\x0001Rí½·á\x0019®\x0019Û\x000bRæ½o\x0012$´Z1@è¹¼s#.¬?=¦\x0007Üê´áoßà\x0013~®]\x0017à\x0004ûÉÓë«ÛÍÛûËß®½IãúJ\x0016ö1¼{m\x001e äµ½ë\\x001c\x001e\x001fEsv¶Eæ×9¡änNÍ\x001aéF\x001a÷àÉ&ä&,/æ%;­ªäTýë 7£/oó´k¯ç\x0013[9uÉ©û×Óæ¬£õ¬Cê\x0004?ôz9º¦ä4Ý`P\x0019)­§@ái=ãï¾WªÕÊéJN×Ïéøî(=uGL\x001e\x0010ÿ\x0005z\x000c3¡\x001bs7\x0001Sâàs sêr®\x0013Sûy%ÏVéè1RÞ^Å\x0000ëþòö§%Ä\x0010ï4ûÔ\x0012h£5<uMy\x0011áÑy¤ü*igÛo_Ç\x0012\x0013º1£Q"ÝJ\x0019è.\x0013M§ \x0005\x0006¡å\x0018¥*)UÿbZ®;À¶ðTº\x0015\x0017n\x0005¸~Szò\x0019ÑHrááO®ç¢Ü­¦¤4Ý\x0010\x000e<-&È;s.õÕiKLÛi³¦*XöëF[þè{:¥­®ätÝ\x0018t:-zâ¤2È¾SzÒ&Ð\x0010ø!Ô¨¼;\x0007íQ(!C/¤ÏC\x000b"¥Ç\x000bêD)\x000c\x0011ëù\x0004¨FNYÙMÙm8\x0011D\x001a±Ñ;\x0006õ¼£»SU\x0017þÉ|rkheRÙÎk\x0016¿4&/«ë[J+åL:7þP(¯½¹üëÕõÍÍr\x001el\x0003\x0011»\x0019L8·|¢Ä¸B\x0010³7/òíÑæÍöGÇ''/\x0015ô0£.\x0019u/£ÈòòRQ\x0000:3îUò´0Ñô1ÊÀÓ|µwºU<xÉë¨æ³5Ú\x0018]Éè:\x0019±ñ,
9ðÞP)¡\x0007Ã
\x000cñø\x000f}ëêô¤=Y(»4.'`MCBT\x001dSð'WÏÈTµ|ò9ªùæPRuÐõjd;ß]Ý_Þÿ´ùôËõÍõo¯ç\x0016<þk¢;§¾\x0010?©QÝ°8ß\x001büîèl{övóéýñÉñ§\x00172\x000bÌ©KNÝÏ©¹é\x000bûO\x001daæWÊ¹Íl¥4%¥é§ô¹%ð<L/,¿ù\x0005iä\x0018§-9m?§dÕ¿éùÌÒræ7©y1H+¦+1]?¦á\x0018\x001e¥Ä5/'¿@Ôþ=¾äôÝ2ä·S¼³LkÉ\x001d\x000e>Ì\x0013Ì­¡\x000cý)XØMÅ\x000b±åoÎU\x0014ÁÌÇÞ7rî\x001e£ÂzV3PîLn=îYÞa®ÜÕ</p><p>*+PÙ
j>ôç$xM ¬ó\x0019¿¼\x0018Û²²ñ²ßÈ\x000bÏF^)G%)>¿\x00073¿p,å÷­YG0³\x0011|
ûÿúïÓ/÷w×KJ2½!¬\x0013êÀÓL#Ãw8\x0008\â®±\x0001Ä6§çg§Ç¯\x0013ëX\x0011C\x000cì|rN6èü\x0008¢(,!zýqb[\x0012ÛÁ5vY\x0019Á)Ñ`\x0003çp\x0014ç{G}	ì\x0007c\Jã\x0019&`~\x0002¡òE$^aSTÂi§èoh¥\x0003\x0017\x0005:å9÷jý\x000c^©À6ëy{ÞµG¼}ú-Fª\x000f×\x000fO÷\x000f7ËË\x0002JèQB×ñ<,\x0013¸ëÑÏÇa½½ø\x0014ÕÏÇ7Î¶O^ìçtÁ\x0017S~zÚ\x001c^ÿzõ¸XDÊßsÒÆºõ¯Ññªº7æçíÅæðø\x0003^§_|\x0012\x0017úT\x0018:õë}¸¼ùõ/KVÒZÍ³Pq"</p><p>
J^Â¦F­7ué}Ø|øÃëXºÄÒÍXN\x001dØD4t'ª|)ÑR¹>,[bÙV,'xzÆ©7Éæ\x0003pÜ¬î\-_bùf,éhië=¾uL\ÏªF14píb%O{`ZbÔ>á[Ú]C\x000f\x001ckÛ\x0007VízÙ¼í5ôr¥­<òOqÍv\x000c@æm´\x000b¹ªm/÷½C\x00019Z°\x0014¶M\¯\x0012Ju~ÈjßËæïQ)$e	lÜl42@å¾c\x0005Ð	Ví|Ù¼õÿa`Â^6\x001dKüaèdzµw2{ÍkQ¾A&\x0016øF¬¬Óù\x000e:§àÀÒ\x0019uD4-`{BZ»ªºmñfVw|Z\<öÕê©ÞÕ~d\x0016zhSO9üåò×ß.¾]Vñä$\x000b©\x0004ÐdyÝd?¦¸Cc\x0014=Oë\x001d¾ß~ø´}÷ñ¨\x0019¡dNF¥¨7hIÊ\x0010Ñ!@<`öUÜ\x001b\x0010U¨¾ID]"êND[B±\x0005'\x001d¥Ù«\x001bhc4%£édQ¦ Ý\x0018oöz°ð\x0018åÐn´%£í=1ö@Ò \x000cei@¶\x0013:+ÞýW\x0005FÎÊ\x001aâ\x000f¸\x001b'cóîòúçÛEÃ°è¦\x0008DkÜâ9HÑ\x0014O\x001f­y·=~÷ñ¥aMfÞüdRóS+\x0018Ö\x00060Ô\x001cJ¡\x001e\x0012±Å[|/+Ù\Ç¢\x0019ÈlFÓ¾³¥ìpôj/Z(ÑBÇ²Å=©µhàiÙÈ¹Ýó\x001e¯¢\x00053\x0017>2µðQ<\x000f¿-HÅátLLÅQa\x0017k~ZÉÛÍËùkË¤Ù\x0013OÃ§\x0017Ópf®{djÝ£\x0016>MvY:C£¦#`nµ\x0013ó7ÿ&@]\x0002êN@ÉÃ¤\x0013,Ì\x0014cLhZJhJBÓEhCÈ3é¬á>P\x001c\x0003ÛÜ1[JhKBÛIèx\x0013ZIº¨\x0011ûè\p#»Ð®\x0013Pça&F¨©\x000b	g\x000e\x0010 zNÀl) /\x0001}' ð1AÝ\x0013ê?\x000bÝ©Em\x0001C	\x0018ú\x0000Q½vÔ¢\x001e	³rÁó\x0012\x000b	\x000buG#juÇ\x0016D±wFî\x0006\x0017q\x001e»4!B\x0008ê =ðH¥YhÜ N+)Ì¥b\x0008+s-ûìµõÜ\x001b/#Tæ\x0018\x0011ó"Îç·5\x0011VöZö\x0019lëòd1\x0019C-\x001a,av\x0014Ï*O.%¬¬¡ì4Ix9\x0011ò¨ HÈº$Î>«\x0013½\x0014±²²Ó Ú@%:\x0011\x0007Ø§\x0018§ÆÈ½Æ\x0016ÄÊ"ÊN\x0004*+H2Ú6ÏÒ5a`\x0015¡²8ÐiqðuÎ3ÎÉ¦óÁ*!Êè\x0006*\x0003\x0016Ç\x0004îp\x0002è¡\x000b\x0015Px\x0015õ¼¤	±:ÐÐy cTmY¯Eó|b£w:yó&EvþìbÓ³Ëq¼i><*"\x000bÅLUËä\x0003æG\x0005\x0004ªJ¨þ8Þ7?.5D^\x001e\x0019cç×O®#¸Àc-µÔo\x001b\x0017\x0007FÖ¹ó^^]òê!Þ\x0018WÐVuõN¬ñ$\x001d!Ñ­óº×ñ\x0006|x±Ëöçí`Áã\x00127\x000cá\x001a~I1øxAYZ\x0013xª\x0014É:yeuÚäØqsï\x001d¦S.Åà§îªuµ\x0011X*\x0008µ$eü¡¤Ü>þr·H§0àÄ\x0018Ñ\x001c\x0004Í¡\x000f«K4\x001e·\x000ct</p><p>·çïO\x0017AI\x0006íd>\x0004ÖÞ÷IR\x001cÑâ¯Ñöe(_FÖIÕ\x000b\x001cìËïÿù¯ÿÞÞ<\~YöÜ\x001e\x000f;­\x0015¼\x0019=;÷\x0018¿ï
\ÝlO>o\x000f_0øb^È*v¬pàè6æu 2Á\x0018º+\x001e\x000e
óqëËáT	§ºàPQ>«òä.­ç	\x001fRËyc×bº]P4-èÁ\x0018ePs\À'¿´x\x0001µn\x0013Ö/\x001bèÙ*Ø5\x0015~¼¼½~¸¹|ØüðtýãÕý¢qZ8¬¤(ä±\x00146\x0006Å<sf¯íóùöãñçíçÍ\x000f\x00178ÑóZ0k-ha\x0016\x000c\x0007HJz\x0012kµEIÂÞ\x000c\x000eXUÂª!Xw`izRz\x0017L´ií<&^N{)fñ[\x0014ãÏïî³BÆFnÞ_ßßÝþtus³Lã#^ÈÑ@´ÛFç²à2z~zq2ðÏ:Æ*«£h>¿¾ÊBÏLzüaO\x001bîÓýÝ\x0017,°Z8ÖiªØ°\x0012k\x0000_td¤l¼\x001f}EåãÓÙé!\x0016Y½4UI¼7f­X©,I®¤¿\x0017#izÅ\x000e'X\x0013ëx.\x0006ÔHóÊ\x0018g$ñK'y"4þ\x001fV ¶%ñ\\x000f¨\x0018Û\x001aRrÄb\x000f}ùQ|¾_ÝZ@,¤¨\x0007×â\x000fU·ÕÃãÝW<\x001fÿ\x0015â4ftÒ(\x0016\x001f#½\Ù#÷§m¿Ù~>?}ñ\x0015	mIhû\x0008qv\x00115Xy R9¶±+|æ="M¾\x0004ô]*·	¤¢­\x0004¨M®YÙ»Û·\x0010îr²H¸ÓdmCÄ)°i
ã­[Át`Uy°ÏÌª\x00151\x001eùÔÊ4Y ¼l|º_&4\x000eÊp>Ñ\x000b\x001e\x0001¥\x0003tËðÏß1>½¤.fÃ\x0004&@è\x0004æ|9ÌÐ`\x000eI\x001eµ G\x0010U¨:\x0011uÖçöÂÐa¶g<JUU¬·3êQ÷1&á´ÓÄìTñÍu6Ê}iS"o\x000b1Ì¦/Ä\x001f8|>»¼þõiÉI\x0016Ñ{\x0003i4\x001eùb\x000cÇK¢LGuÏ¶Ç\x001f.^§</p><p>Z©@á3ÊD¥=å\x0008â\x0016äÑDÁ</p><p>ÛE¥J*ÕJ¥óÍ;F\x000eôâEàwàæ1ðB*]RéV*6Ð,§þÑ¸]5/ÕÜ-2%i²¯ÊjªöRæé	n® ³ÊT¶ÊIx\x0015¯±4bÝK0y[Íßc\x0017R¹ÊµRùÝ­Õ	*¡õr7XÙµQ	\x0011fu(ñ\x00076\x000co.ïÍ\x0001¼e4\x§\x0005çJ$Ì\x0015íßlÏ^kÃHªDRHxÑH\x001bÝ\x0008Ç\x001d_Z\x001a`¦¹ÊÕËLvÞfE¶¿¿üòoOÑÄ¿¹O s¶ïø®æ©\x00025Z)ôÝ­â\x0002Y½'\x0013÷ûíá¿\DÃþæ,þðõ\x0012'áj°ø\x0003}\x0019ÿ¿¯\x001f6\x001f®\x001f\x001f¯î\x0017k_§\CD\x0005®£(g(´'¾?Û~<<=þ¼ùp|~~tö²¢rõ\x001dmÒ£)ýùÓæíõÃoW·\x000f×Úv¼K"\x0008©W.d^®\x001cÛïÙGÍÛãÏ>~Þ\x001e¿ÔºcfÓÑñïrçÝýÏñË\x001fÞüýo¿^Ý~¹º|ý\x0010ãkW<%»r#l
ü¨ÝóÖÉÓ³wq'\x001c\x001c}8úxx´}á<3.¸0\x000bÃç÷C]Îìuv·óªWñZ¢\x0003©\x0008DPúÉ\x0019\x0003üè\x001a\x0007Ö%°\x001e\x0003VÜ×5þxzæÎ].Ì'
÷\x0000\x0012Ø\x000c\x0002;n\x0015!\x0005õô9\x0002«½VØÂ¶\x0004¶cÀZå\x0015FëËÀ\x000bFöfö\x0000»\x0012Ø
\x0002;\x0016Jø6Ne\x0005Êð\x001e\x000esý\x001e`_\x0002û1`Ô¼¤\x0005Ü¯lòÀÚxæö\x0014\x000bÚyCÉ\x001b\x0006y=Ûà|i6BäZ6;nÔdí3\x0006õT\x001e=¶ùÀå:|æüÐ=â\x000fs/÷æú¯WÊ¥-6±h*ðø4ªÓ84NWè¹@\x0011£¾9þãÑKõÜ\x0010fÎ\x0002ÂÜY,¦\x0017D\x001av:µØ§¨Ap
\x0019j\x0002ì)-,Tó*\x000e5«âxþîaóéòþîË/\x000bgFqgs\x0004uLàñ\x001f\x0012ð
p\x000eON?o>mÏN\x000fß¿\x0010á¨y_«J}­#ÀRäÞz\x000f<\x001a:`õ%¥1ôs\x0006K56aö®±	Ûé·÷?Þ_Gú¯\x001e®xnâ_èçÛ¿üîìêááî6Þ®\x0000³\x001aTçAðtÑ\x0012,½[ég\x001aN6Û³7gÇ\x0011ÿ¥ãÅÀº\x0004Ök\x0000Kª<V%3\x0016ç®@7\x001f)ÜlJd³\x0002²d\x0001\x001eíãm\x0012\x000eÈû\x0015´\x001fF¶%²]\x0001\x0019§ØHÝ²©*	W\x0007]¡XT\x001fò¥°µ¢ÕVØIÑª~ÍÔ³»ëÇ«E-w,¡«\x001fÙÐÀ/ÛºT\x000fªß2ãtz|~tò</p><p>lô?ä1­ñãåÏ·K\x001e«¢Eð\@\x0015â\x0010.p\x000fª/î</p><p>oß}Ü¾ðªÆ®$tó@v"O\x00154:/¤AI»VÀøÙ]erãgwhrëÏ~v÷ôóÕÏèÖ\x0016}ö\x0000ìÏb\@C	Ü\x000fH½³Rö³ÓwGïÐ½½pºæ£éÁ%mlo/\x001fïn(ç°ÈG\x0004¯³r°¨¡j»(í'eÕ\x0017Ô6¶\x001f·ç§'qXÀ</p><p>%+t³\x0006\x001aÏ$ª\x001bYS­å\x000cWÕ ÔªJT5°¬{Õ&Ô@Å\x0017\x00022«\x001d^V]²êeM©¹¥\x0013tËËJ¯RóâPå¼LDRÈT|÷ôÓ/^ÓÄD"ÉÿF¦Ô¯a}Þ¥b¯Õ ¥·ï_|ó·óW7»k­kAÓù\x0016®mV}õ_\x0005ã`^Àÿ*\x0017.)Q\x001c\x001f®¿<ÞÝoÞ?ý|·\x0008Ð\x0001ÖìODoXê¥ÜuYQ>î\x000fÇç§g÷\x0017ïN_GÔ%¢îEôüj©ã]*WÒù\x001c@i)(mIi¿UJ_RúNJ@ívþÜ³°¨nÀ\x001fÜê\x001eÊè-eµ)£·¸)ko	O×·\x000fËÂQY<äËQÊØÅ0!Í*#ºÚWÆ?çøãçJdâÕ²ö8¤lÏ»¿^.ª¢ó\x0013'1*Ás\x001dwÛI%åì¾ÿáôÛ\x0017*ç2\x0016XÐJô%ëy,ô\x0019¹æ¹¿W¸âç­£µøy§h­þ¼nóæîéßï¯®}dÙÛÚð[µnÏ©¢#Ë¡Ï?õ÷ÐéÅ\x000fgG\x0017Ç_vù"Ò³KnÄ:D||Ñ=º}¼¿úÝÍÕÃïÞ^=ýçïR\x001d××^þ¹lIçO§qy>h\x001fJ½ù£ç8ç\x0008Ó^üë&Us½P½\x001d-E½5ã\x000fYÝíòö\x001aë%7o¯nîî\x0017\x000cÔEEb«8~× øñ\x001d\x000cG\x001bxßÇÛÇX)\x0019ONÏ^¦«ëc?±Â\x0008+äÈ(zõ\x0014 GÖì/Õ\x0014]3«*YÕ\x0008+â6N¹0¾R¡ëÃÔ%¦\x001eÀDE?&\x0015¤«\x0013#È31ær¥ËY¥=¹Æ\x001f</p><p>h
î^TÖ\x0000E©&2nSIe5£8ì6Ú¯AfáÝ+ur~BFèd\x0007\x001fR5/\x0016Ú\x0018Ò4QÜ«µÑlBT%¢êDTNtÙ¨²2Ìsêã¯\x0013y	Ù ¼¿þí·»¿<^mÎ/¯\x0017Azlt¡D9ì&\x0008ékåå<düéÓéÉ\x001fÎ6çÛã%¤ª$Uý¤XÊGQ\x0008^5æÊ%ËØ4Ô\x000crIÁì\x0012)·aHÇ¤sÝ¢Å¤^Î</p><p>\x0018â\x000fù?m>\Þÿýo_~¹¼Ù\}¹¹ºÿ²(FIÏåüºclÜF\x0018ö</p><p>/6\x001f¶gGï·'Ñ\x001e\x001c\x001d¾\x000c%2\x000c"Ç#Oé1c´GãTª½®û.dU"«Ad\x0003¬\x0013à§x?ZÒ\:WMi"6Ã+^¤l±/Þýýo·ÿÛ}$~w}ù´¨°Eá_²\x000cÞ	j'Ç'\x0015î3{ÅÒ\x0017wG\x001fÎ"ð»ã³íÅ\x000bu-Ì\x000b%/ñâÆ@¼·±\x000bÜåe÷ÄÂÚqU«Æpã\x001d& b\x001bd\x0004>!7ôUUÊm¼ñ\x0000\x0015o¼$\x0000òÖ\x0004µùð÷¿=\Þ.Ë*\x0008htSÓ:P)ù,P\¬üê-0þIG·\x001f_Jj#ëW`¬Å9cúþêæêöjsø\x0017¼ ü?E¼\x0012Rµ\x0006u@#&
¿ª	
{)øOq7À{Áÿõî³óK«ô»pë\x0001MÄÏOW÷XI¶¨Y ÎI</p><p>¹dàªNëò\x0013 Û7\x000fñ\x0016\x0013íÃ»£3¬#{©Óx®ûlî3wÍ<mN.° QiFé\x0018AÃ[ÝîýÌ|¦êb\x0013öu:(é Nzq@í1Âr3¼w\\x0016¤ªB±F8YÊj¦å+çMÿSWPJ|È2\x001cüá»é¿§jÙ»¯î7ï~ýuÙLIí\x0014¥­Qô¬«¢k¥~T×</0>}wt¶ù|úáÃ\x000b#%\x0013f9M\x00181wÓ[1
NÄK\x0016\x001bõÓSæ</p><p> ÷&³.ÃY\x0005#þPwÊ`ÙùÕýýõ²éÁÞ</p><p>ÉZZ4\x000fðöL\x0013Æ\x0014«¹kQÀ\x00063¬\x000e}Y)]Oª"²¸ôOjPu£äÿü×\x001fýúÛýÓíë\x0019+lâò ÐM\x001aî­ÏÚd»ÚÛ¢ø{ôáÓÙÅÇ\x0017RjRÏÊfâ\x000fåÒ¾¹¾¹ÞójYÊ*tA³Ç¤w[\x001b4KÉXU^üyaß\x001cDÏùR°µNÐM)ùý>\x0018Í³ÏæÔi´öÏ|þ\x0006J]RênJn4;1XÍöò\x0005^»Ñã¿9\x000f\x001c@7y}{ýë"\x000fé­\x0013Ôs¬ó\£.\x001dú¡lýÜO>òøãñÜ#Ìµ%a§-yøËåíãýÂ{_PÊ°Ð°Ü$ï¦ìi::0±ÁýÇó³¯|Bé¹JæPy{]æÃË{Z¤Í\x0019ðé+­¢ÕNÓévJrP\x001fö$ß¶'Øa¾9ÜþËÅK</p><p>jö?à*¾½Ú¤Ïýöêæòññ\x001e¯Ñ\x000f\x000f×?ß.R¢\x000eJp[	\x000eG£nt\x001egîËfhø»lÏ1Õ{\x001e·êñ»øîËåO\x000fñOÏÿ°ËñÍl®mRû3­Ç¢i5µöa\x0015u~©WÏ\x001c§ÙKíWyã:Ì/zzRaù÷«Ûùe$\x001aÿwOËzú=V)'}~\x0016Òç\x001e ñ>Rüpô±¾ÄÅ·½À¦þWÙ¡d\x0015Ø\x0006\x001d$q\x0014ËSÚÁ¬)SÎ¡\x001cbW%»ZcÝã]</p><p>H;Å±:ÅZ5¾fëµØuÉ®×Xw7.êb8K>\x0018R\x0013Jk2ÄîJv·\x0006;}(61MËîl¾~\x0019¤!t_¢û\x0015Ð½¬ê)¿¨q\x0016\x001f9·\x0012{(ÙÃ\x001aË®rûQ=ð\x0013\x000e+mb\x0016\x001e\x001aH±Æ²ãÜKR0\x0007$¸½\x000f\x0011z%û(kÛ¾qw89\x0019÷I4NÒ²óN%^9Ä^Ùv¹q>üY\x0011\x0004©Ôb65E´^i·ËÊ¸Ë5¬;¦z\x001dY°<%EA.¬$äà+ë.×0ï8ÐÀb\x000ev°¾ ã76·Þ7\x0015¼YË¾Ó#&Ê~_uWÞ«µàm\x0005o×Xy#yÏ£</p><p><+%\x0006JtÕ[×\x0010|åXå\x001a\x0015EAøiV°6·U>ïyëÖ2òkkøV¿çiå£µ	Td))­ ])¿2Ä^¹V¹oõë\x000b¬À._CmÜÔ5-­+í\x001a¨¼+¬á]Q¼RLÒB¼6¥ç&\x0007I§ÍJf\x001e*ÿ</p><p>køWl'IÉ(2ÀÅ|Ú²RWtµ+m\x001b¨/Ok8X!K+/\x0015&U§ßÉ\x0019µR(\x000c5\x001c,vÅ8ZyïòÊ;\x0013añZÛ¦òQ°òµãchcèIÍjoshSêS\x000cÁWf\x001eV1óqÛØt`QË\x001b(:\x0010ÔA!­+6PJXÅTÆå¦×\x0003	õ\x000c°&¨­æÙÀ«ÊÚ¨5¬M\x0010ÑÎ'v-sX¦¨ñNÚª\x0001~½Îv¬q^§K_ Òr\x0019¾1\lâZ\x000b¾:¯jó\x001aÀ³¥«ÌCQCà¥YÉÁªê¼ª5Î+PSt^½:ÈbáCJ·\x0016{u\Õ\x001aÇ\x0015ãaVÂ\x000cÙwápÕ"=Â®«ÓªW9­ç%E÷ÊÃ~¢qT\x000co`%;©«ãªW9®1I]3\x0016`jJmg£2kVºEéê¸êU«WTbcAK®cµS«®ê÷\x001d¯«^á¸\x0006!¦`·îÀÐÊ;ÖdòUQþ\x0010|u^õ</p><p>ç5\x0008©±EqwÎ«õ,\x0011éåZçÕTçÕ¬p^'ñhÚñ\x0001HzÊºü`ï¡\x0014t\x001ab¯«Yá¸\x0006¡x¢\x0013je\x001dH*#\x0002ö®~­HÞT§Õ¬pZÀîüä\x0014Öv¤Óê4dÞèÑ;\x000f'õ»á¤\x001f.ÿzy}»9üåïÿïãB\x0011È$¦hÌNY^sIÜËí\x001f·gÇ\x001fñá÷\x001c[Ý_C-ÆãÄ\1ÀªY\x0015\x0003å¤×<\x0017Üë¹ËRT© q?]2ÿßí]2Üê\uÉ»dv]\x0012¯¢B</p><p>#¨À\x001b@+II\x000blaT\x0005Ïv4 ª\x0012U \x0006]§6d×°OÆä>ÑUÕ%ª\x001e@u\x0012³>\x0019î"þJÌë¨ÂÖ¢\x0017[ìH¶óÂX»ywýïË<P¹T\x001c'«ÍX\x001c%B&À¯ÊGÄ?æìø¯Óþ(@V%so0wJæN.wxÿ¿ûxýeI'".*\x0013&\x001c£å\x0003ZSÍ==ñ^VìÔíæðì_7\x001f\x000f±\x0017ñy>ù'i~»\x0015ÿ7ý©ØãîW¬:e¢Yº¿úùò\x001e¡¥Ip2òÜþÇÕ_ã\x001f\x0014Ãkì¤¼W\x000fÜl<ÝéõØkptúø¿þøÝÛÓ\x000fX'3uÉDstvôn{öµ</p><p>è</p><p>-\x001eohEÃI0Ð$MFhÒYB3Ôñ:\x0016ÿzª\x001dM¥\x0003}&&@xDã<é\x0018Z<¾º\x001d
\x000e¤&4<8¢¥7uD\x0015Èâ65Í[Ít\x0007d8ÊÉ&2ï3ãchÑØv´jW\x0010M¦¤=&Ô\x0002£\x0001]RÆÐâpÍh^ã½cBC%-Ð¤Jc>\x0010mU=ßfQ\x000bcªÞhºç#µl;$Å\x0008chÑtf´hËÌØTâ\x001dÉ(W\x0011É¸~v\x000c#AüOã\x0007
:+¸jâ@Òªé|\x000cDXábÅl÷\x0006a\x001a¶Èl(s;±¥Xzb\x000b+°E\x000b$ÝA\x001fÏ¨4ñÀ&IñõÎ\x0001þ;d³;Àr\x000eIh¨pB6×Kb6Þ8[Ü²²Ù\x001f`ý@ 6©z3²YòT\x0007î¡Eg Û\x001d\x0002\x0004vU&Ølu
¯Ú\x001a\x0007V\x0002Èv CJG2ÏÐR\x0011\x0012kØè\x000cd»C­®Ñô^\x0011\x001bPáV\x0008=ðÕH¶:\x0018LJöð1M÷[ØÒ»}¼çz½\x0006[Ü°²Õ#L!\x001b¤s`\x0000R½\x001eÆEJ2[áâ+<´»\x0004\x0011c6IÔ¥\x0002%\7v¤R\x0015\x001c)>²C»Kmqêw\x001bGFÓÇq4¼\x001f´{\x0004\x0010©\x000bíOxJùJCýzclÑ</p><p>A»K\x0000zèA³KÎÐ¶åOêü\x001aÛ-þ; Ã%x¼\x0017$w\x0015RÅ0ºìJ\c»Åµv\x0010÷¿£us&É^£+åo</p><p> VÄ±\x001eÚ½Viü8²Ù4qÏ¢½Í!é^·ðøÛo?â\x001a¿kk<üåòéÏwO÷_åÂÁ-) 0éA\x0014kSa©WNâÊ·ëg<|¿½øþôâkmx\x0015Sº$[Lé\x000eú
0»W.¾\x001d«·^n>]Oy÷çy\x0000E±É{ «(\¹)ïO,ÒºÝ|:þêÔÆ</p><p>&%]Âe\x001f3ì§ÖÝxÃ£yx;\x0017j\x0004&å2Â\x0018}àÓqÂ¦\x0001lqe\x0003êh·ì\x0008LÊ\x0011|#)]½\x001b>SHÉÅÈt*ÝÀÏ¤é3)\x0000=\x0000ÃWÚo.ßÆâû×·A#`j'\x001cÿ×?éË_Ód\x000c\x0005ñ?'(Òôx}ssõøøu\x001a¬¼´{¼\x0017t]\x0010Á\x0003í\x001e-B\x0011¿E7§\x0017çÇ''GççE¾þ«4Ø0ÿYFcApä¡À¤Bk¥¶./N¯Ó|mmþãÇÇ\x001fEáB¿¿|B;Gâ\x0004BÐu\x001d»\x0016\x000c­¾øBßo\x0017ÿñÉþþÓþøä¬ÿi|2øÿ´?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-T5D9dexZ/cCiUZh975uzyTlKbxM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-86EQoaZAvfTOi7RAh2+UJDJm2b8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-HSuDxH0A3TToXbLpTgvcCFykcNg`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-fON6yvvOQsyoQejlzuD6s2z2r/o`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8110-Xyb0v8ex0eRZ+eaRRBKsCVFPn/8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `95ae-oOWfcmDM0eDI944f/deNKDEwXlI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-fON6yvvOQsyoQejlzuD6s2z2r/o`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-0et8+JuflGKs31rYghEs50ClDXg`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-8LIGTYDLT8XjxMEJW7V5Jh01tDs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-2J6wyeHZbKRS+yfW5iM3V2FMihE`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>ᶞ�>C�ױg�\x0002�Fa��n�$�)�L</p>
  
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

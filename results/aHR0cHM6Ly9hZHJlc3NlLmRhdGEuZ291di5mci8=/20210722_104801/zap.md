
# ZAP Scanning Report

Generated on Thu, 22 Jul 2021 10:42:27


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-02.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-02.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#3ELR`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#3ELR</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-04.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-04.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=~x÷w_?<=¼V½Ù×_lx`|MÞºo®u)çº\x0013¹;ßK1|ÉxBà¯+Ì¿íyo·²¦È\x0010Æi\x001bo'dgÞ=Å oYÎ'2Z¹àµ4éÆ3¸{ýµ\x000bñPÞÏ\x0011hñí_%¬»xÉ\x001fÈø\x0017¯¯©Î£÷\x001cö¯í\x001b2|?yÈ{\x0002¦©\×\x0012á-í¹\x000c'2\x001b\x0002=µÞnò]µî\x0003&4|À\x0013cÕ\x0014{çÍN\x001fu«oË±u@sþ¨ó.Þ\x00074¼\x0001µc)x:vVm\x0002OeKÛ?ÔnÐ¨bPè]¢¼1\x0014h\x0005Ã¾Û.H&t¢K	r\x0004Ù\x001dr¬\x0000Í1mÑZêÉ\x000b×rRfûüî·\x001füÿ¾¼ÒÄ¡ïZÂ»\x0004¢ñö#ªrù¯K»jú8½5\x0017¼'
:Ý²\x000c¯E\x0005àÇ9?Þ7÷iµì\x001f	¢Ó±ÈKð­:ªZ-#àÎÊÜ\x001aÌìrá\x00138.àñj-&3©ß&öÝsa\x0002ç\x0005\x001d0\	0ø^¨0/À»z÷\x001cä·ÿ('ö×_ÿáéí£\Ô\x0007£ÿ5®ÅÌöÙõqC½­\x0003[ÇÇO\x001eXÙLS½QÆ%Ê'OÕFÜ1ðlÓ7ÙîÀNd æÇJ\x0001ä\x001b\x0007ûrV%w[r[þ¬\x000c\x0012\x0015	'\x000c4AnÑ÷íO\x000ev"\x0003çoAROA\x0016K\x000cºÉíÛñV9\x0019ÃDÎ°Ï\x0015º¿«Ö²Í9¿Z;:\x000bO÷ï\x0004\x0006>áÉ]Í50M¼¶³YrÙo&òz§È\x0007¡Íhü®:UùÊw±Ù\x0004\x0006bq«\x0011Ws:æÌñ\x0014,¹ïMnÐ\x0010)/YÇ£Q8k\x001c
\x0013JiYm[fÐËRZH¼Ñmp\x0000,èî
´ß3Nè\x0000Ð\x001eISF\x0002VÍ·Æ\x001dúêD£èÊê\x000eÝ¹Ò©¡;C}ûðFi\x0014\x0007)GÍò^Ç\x0015î¬'ò: ­b®[\x001e©iÈÜ vêsàwÀOîI´CyZsÆ1¶D[Ýý\x0010Æ8\x0007~\x0013\x001a¨o$¦ô\x0000\x001d':b'Î&ÿ¸O£Oh ¾q\x0015uBôqiC:÷<«
Á6×=¡¿ÈGh/¬#\x001bÇ:9îy¾éçMÛÍÝëQÛÍÅýùÍ»wÇtYe9Â~ûôÏÏ¯D¢bæúÔÄÿÝ­·dSé¿VµgÝF¾¦/~Ü7÷eó¤Èöë¹´ß~xøîI\x001bn^)L«³æTZ÷úâY&Òo¬òoê+½!]¶Ã4¥
CÆ.ýuÏàkM6æpWÀ ö­uÄuõtx¨[y¸·Ë-·\x0015\x0019Èi!kÃçºyú-¿\YÍ/\x001ctçÅ
9/ä}AU^>ì²*Õ+µi#mµ-'rmnÈíØ\x000fÛ]Î¼\x0019¥l[a&p]ÀÚ£\x0001KÖn\x0010tr[\x0014Þæ¸¥Èm!{M°Í¡_°ã5ç$9\x0007S7è\x0015L)7\x001bÒFöYÍ¥:"9èãû	\x000cG#yiRú\x000cîÐ¨õüB\x001d
	½{ü\x0007øøµÕ\x000eH\x000fõpt>ÐælÄÍm=1R\x001eþìùá£üo¿\x0011O!Näµ¼òHãbi÷«G"?ðj\x0012Ýú7ÈVÛ\x0006ý×\x000b²%æñÙU(\x000b¢õÞ>46ÏòwÚÊ´ÏÇ§ £\x0014eíÍ
6#6(AÈV÷¡ZòKAî0ý,kfú×¨bÁìG#×ùàZöË\x001eT¾e]ÅòsÌnp\x001e&\x001e\x0005ë![¾ÇÑ¬\x0001Ø</Zv¼\x0019Göür©îQq\x0018¯ù\x001aÚçÂ¬ÑÞÞIXºÇ®\x001c<\x0005~(Ü×*³1ÆÌÑ&3å¸kô'X´éÂhc\x001eyíå"'rEã\x0005Òò&\x0013t¥§­Æé~û(ÐËÑ\x0007U*ýP:NÐÆXÒQx8
't_Ð\x0004àe"w­6¦\x000fQí´½pÐ
:ÀÑ«Ã?Ô\x0003é+6æ\x0003G\x000bá¹miB/K\x001e\x0006\x0012w·ZVIç#]4-M`8y{§ûM½mÓÐð\x0011©Z"Ðá¶;Èëªl{inÐ\x0011vZãF®\x001c=;ó?uýÛ·½4\x0013zùimü\	¦äG89| ý\x0006\x000e*ü+\x0007²ziÄñ\x0006TvÊcöD¡Òå
Ý¶
/\x00139\x0001r~ßÀÊ»1E}~3ôÁÑweå«/EN#×¤|þ\x001e\x001f¼c£¯Çê\x001d\x0019G\x001aÔ¤½Îò0p5Ð#L<7xÜ W81Ô
\x0011èÊ	ÈhD] Ó;\x000flNhøÙ£Óó\x0013½\x00052¤Á'dÿFÈõ[Íù¿N¼å¼g\x000eÂ,N(^d
âö\x001b;éÛ
·r|Ql(\x0007E%Ê\x0015
UÝ9ê^ËePSÛq¶¼Xí¢ïÐæY\x0004EÄúå#+@¥Ð·ý\x0001\x0013\x0019¸çz%äFr7JÄËR\x000fÉÍÃ©óÃé &[sµ\x0007#V;C~6­Ý»©s¸UÂjÂMn¼`×¡h¾}°uÃ
´ËÀºÑccZB\x001f\x001b#ºo\x0010Ðð\x0001§Í\x0008\x001cÕÍðürÊå"$ºA#{ Ý0L¹\x0005åÝp{\x000b\x0014|\x0015{ñ\x0005Ú\x001bÆZø\x0003Æ²ï\x000e¸A\x0007øÊ\x0007\x0012lßÎ\x0019:äòê9Ý:¡\x000b­\x001aø][íÔüu^µ/»÷i=ðoÎò_ëUÚ:½÷Ú qsø\x0012ÅÁëJyúßZ	ÿjüðôªáÉ½øqßÜÍ\x0007j¶jýüøññËWË:&ÿ\x000f>Þs\x0006ªHR>Ckáíq:ç^2h6eàÅM/êí*@î®)Õs~Ç]4X42Pd¨ï5%}ý\x0016²Øüv&p"cº+A÷|F'ªzÏi4ß¶¢È\x0013\x0018Ò¨O&¸fD¦²`º\x0000$ÇÙ·6S¡Ui(\x0014yoÝ¼d+(X\x000cÁí¹oÐTÌí=$f4ü§Ômç<h\x001c÷A/e¿\x001dã\x000fÖªÛ{He»ô¾Ó+¯ùú\x0014sþö\x0006]1ôùñ}î¿\x0004zãn½\x000f>ËùôÇ\x000fÏß¿\x0016¼|\x001bbÌ¡NêÒb\x0011"=ïÛ[H¡r¼ì%û\x001cí³¾Z¹û\x001bÙì\x0004YÕcôvãrLÃniòpZÜÅ±[L°5^þñ\x0012p"GZ2ÈOÆ£Ég\x0001'&!Ï£YlãÊL#piúÄ\x0015;\x000eºt¸W\·ê\x0015\x00139Ã^ #{\x0016ÇÍìÕrÜøôÅ°eÈ+äjò¨^ÅóñùPÌ[þ-ò95\x001féWH\Õ)­x¸2T2ð} 5\x0017V	É~?à<WpÛÌxV¡û\¸ÅIÖ¼ç\x0004ÈÖ¼\x0006\x001b²^Fô\x0001çmvqß\x0018}CFEÝ\x000c\x000bEJ¨ -×\x000fÝEïÍ\x0006\x000b,t84j7¶#É¿³T5Ót]T$±ÀéðZÛU¼Ãx½1¡xqÐ`4ó=VÙ\x0012{²¸¬ú"9ÞLC·n%¤(UºRØ:\x0018ÌÉëûäø
:óªnJ+%³k%ÎÏZ¸x
6Ó+>DW²O6«\x0005®²\x0002µz©¶
6Ó+>Ü\x0007\x001c)#§«$\x0017jºÈ`7Ó*^4ÄÄýÐ*
9éÊÞ?¼{±µvî_ù\x001f>¿ÖÀw¿ñ[\x0003Gyuø*©_\x0018¿àM]Î%x|ÁíÜL\x0007kIðXOÄ2}yøy¼\x000fGâÆ34ÓÀZT<3-àÈòyÈ \x00058\x000f»_h¦µ¨2\x0003\x0002\x0007.\x0013)\x0002§F3í«¥´åËt+é~4\x0000${á·í«\x0013\x0019ÆáÄ)DDN¦Ë4¢¿Qä´ÕÈ0ãÙÜê}LJ=ª\Ð\x0018Û\x0018ù\x0018>ßÜÎÍô¯Û¼ÈDîçi\x0004ÉÉ\x001cÕå³i¦U|Âb
×57®.\ÍËVãe"Ã\x0000_\x0005\x001e¥þó\\x000c¥5«n\x0003\x001aZc«¼,|Y®Gy\x0004¶Ã|ÂîÛÅõÜLk¬®Ú¯E\x0007¾uÑ\x0016FOåîvn¦3V>öºøeÑÍØ`æ\x0013\x001e!Å\x0011z4B¿ÆPtÑ\x0015){Õ\x0008[åE_\ÍÍtÜV\x0017×\x000c¦\x0012:f-
\x001a|<F@vWsã«ùX3@ÇJÅ²\x0010\x000cò1\x001fveÐÊ[Ýj\x0002ÔSWF%\x0011\#º¶ç\x001eÈ8ìV&A 3KôÉ½UÈ=Ç£ñ}wå7Ó%\÷/Án4î|Ý0ÛÑ.
â7h0ÃýùÍÛö"h¦\x0001¹jA\x0000Î]<J)[Ë{]ÇXÄ}dB\x0019\x0016¨(¶i}¢Î\x0014Aîc\x0012àÜÚ<\x0003\x001d¼ÎûAm\x001e:YÌû1ìpSÅ¿AóeXáìug\x0006#(&ÔU»M\x001dÿ\x0006
×¡ò[W6³-ÙB:þ%L7­[_QkÍfø\x0003¼Ò î+\x00047èÂÎ´\x0003t'\x0019G¹\"YLò£ïîL?2¡+E4k«UìÏl5ùtA\x0014=áBÌu=ý\x00049\x0006"'³)ÅcPóÊ\x0012\x0003N´×5¿ ÈÑ|C_\x0012C\x000fÕºMÃÄ\x0001
ä#Ê.Ñ`£ÅæIî50e@ï9¨'r 4\x0001p3ûìgàÞ÷M
7ddñp\x000b7Eª³û\x0016øÌ¥¼gð° iÞÓê\x001dQjçÎAúm>\x0019#E²é¸AÃ|p\x0007*GU$\x0008\x000císæã|P"I<&ô:Î\x0012\x0019\x0011æÈ\x001d/:\IÐùØç«\x0003
$\x001eYßê`*Õ´-ùÈ¾4\x001d$óF\x0003\x001a6r®«[B\x001b8<½¯£\x0010ô¸µ6}\x00187d\x001fÐN©<Û"ÿ
#×ÄãêÜ%\x0018 »\x0016ÎGîCÄn! ýF±{&ÚÈpôd\x0005¡Yµ.:ªtøç\x001d%÷D.´æ\x0006ß°\x0019úAGm<´KÎÜ\x0013¹ÁÁ«\x0018ÔÄ-#ãíè'0_¼NG\x0002úÞ¤o4C¤Ý÷d-Ù;<_¼Nb@§£!r¨lâí¨¼´Mb?X\x001bG?ûý#:CAè3oõ6EÒMÍtä\x0017Þý_O\x001f>¼V$µÂ
Þ%ßç|ûAã4K^:¥ÞßX$+ú9Ir²º3)®-kþ ¹ÈN'5JûjQªn_Ù7ä
È\x0001(Ujó.%9F,Ê^üs\x0002w\x0000ÎIµjÈLäSr\x001dþxco«\x00072<W\x0015\x0019Æ-F+ 3oFM\x0017ïÕ\x001btø¥>ûÉ\x001br\x0006ä:M\x001bi	ÇO»F\x0003cÑ\x001b9»ûºQÎîg­ýdÄm¤vÐ\x001f?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-06.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-06.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=£¾õz]Øó¦\x000cBÈMb¬Í#\x000f]&1ÆFÉYÓ6\x0003\x001bÕï³6\x0016À¶Üø&·ªÐ¥ÁózN\x000cb4¶¦ÌfÖö;v\x0013
Ýµ#h-\x000c
èíKªª\x0008Ðy"&7Q/M\x001b¶Ý\x001cB\x0003}W¹`ÕÜå2O´yNµäj\ü\x000e\x001e¡§ yã\x0000x­¬û*\x0001ãÙåÒ×dP\x0007w\x0019\x001b}Y\x0005[^Û|
úÀ1^\x0017ók¢cû§@!Àò$'eÔúÒ\x000fÏ±¯\x0006
tzÊëÛéy\x0018·wÔ ¥¸¶RHýLþ\x0001»§
üZD\x0018àPDÐ\$ä\x000eÛö¬ª\x001ci\x0002ï,zZ\x001e\x0017b¨Ì¢WG\x0012n­fDy\x001cwgÃÆ×\x001f<à%¢r²Ä£D°0ópè\x0015Ê°R+;v@\x0012½J%CXãªcá g§¥Òø8a­O\x000el´\x001bPç>íÕÖ\x0002¬N(]ì;µ2®©\x000e\x001e!ÕaÔ
ôzÅ\x0019pÆUüÂnñ\x0010×úá\x0000\x0008î2(\x00198¾ÚÿÏ#o$\x000f[_ð+ÿÁ\x00128õÓiVh:kV9\x001cä	û \BAvù¿±0aÆ\x0012\x001f+ýIº\x0012\x0014\x0007v@lG
Þ^_Ö¸ªã§tH XÖ¤^\x0007/h`
9cy_ÐøB[`X«:ÔVã+§C« ¦Ú\x0018¥\x000f\x0016½\x0018\x0005ÜOÂæ=V-k¿ò\x0000Ç~eµ-ÓÖKÀTpÎµKÁ[/tÙ\x0004Ù\x0003\x001c.O}-\x0001õY#\x0018#O/æhû´,¦u78|P}.M#SKFnØYFÞ´\x0015Òaë\x000fþZìõÍÀMÁO{¨f\x0000WS\x0003ØCêþ\x0008\x0012H\x0002ÎôÇèrÇ>ÜBõ¹=eàÄ³}"&»¶Pp'ht-÷R×.±\x000b¼>àI%¦á¼\x000e!yDÚ©õ'Î!\¹O
¼ýà\x0015ràUûdñ075xî¡XëZô\x001cèOÑSXî"ÅC\x0012YqÛ8¶´Ä½\x0007wÙÌóhyæJÆô¯g¦á<¨xk\x0015~ \x0017\x001aº£ðVÕl\x001c
oçrpeÿIÛ\x000f¡\x001bG7QÎØg©v\x0010ü\x0010\x000e©[ªmJo\x001d\x001dJor\x001fËéâ1Ä\x0013S2K[i\x000b]W¶X|\x0006zz|$µÕ#ÞE\x0012ÍÅ©ÎwfE®±ë\x000f±Ëû\x0017,ä¼AÆ¬<eýêéª\x0008ötcØ3c³E©f-2áj/±NÖ]\x0006@@\x000e_µcÏ¤nÈ\x0005\\x0013'üÚr½çDEb\x000eè\x0016Î\x0018%\x0011\x0016A\x000bZÆÎÒDòDêÉå\x0010¶\x001f\x0000zB\x001dA­h¹ÄèlÁ7¶êt2Ð+Î°\x001e\x0019\x0003g´ Ñán\x001cµÑ§YY³
Ý÷¡\x0016ÒM¯Rt½M-­H^3\x001aþ®éØâU\x0012à¿½üþ\x000f\x001f_Q\x0005\x0019\x000cÃó^OØÚÝßý\x001b\x000bíMý\x000bWfo\x0016\x0000kÐp ozêwÓAQJ{(¤5\x0005ßÁ\x0013%
I\x001b|zÆ{>@Ki<£´\x0006P\x0003\x001b\x0003¨hé\x0011"Á\x0015\x000b1MïÚK¢i½V\x0006v¡qÛÆ\x0010¹°IÍÃO\x0007s
-¾ÉkûUGÎTÑ\x0002´ëT	\x0003¾äzdî¸m9Ê²Ò:va\x0019°p«u*xt\x0001¼§|³BõvÃ\x0014úè×ÊÜeÍ_>ò5;Ô°O\x0003GA\x0003uiGv
iã6@%¤¶ÒÕú¸\x0019àø¸Ñ¾±ç\x0016WÁ\x0014\x0016ÕtÁm7Þ\x0010\x0018\x00078æ\x001eDb\x0001NI^\x001b\x0016	[\x0017÷º\x000b¸~½=\x0005´¢-×9µdKtBD\x000bUÓÓXumìèàÕPÞÁ£¢A-Sß±¾×§à+\x001f}£Å\xrÌZcãt£K'»\x0013:ëJ\x0019ÈöNõ-sâØKÙJ4'vÄØëS²¡[çËtê^À\x0014#6\x0012ú¨1õÑ4Ðåí\x0013â^'#+\x001f-£÷´ vßîÑõ\x0007\x0017Dh«ev*\x0019z´\x0011¤s,VÁ§î\x001dP\x0018ôÉª9r­)&ÊÊgèµÎHßÁ\x0003j&(\x001fÄâ8)~Ï\x00129ôjçièÑQjÝ`M¼ZvW]\FÏ=<\x001dæ\x0016\x000fs­ÖCs>ÃhìÚw]xì=
^s¦\x001d¼`9Ë\x0006\x0007'ÌúÔÃ¤RÃ|Ut^wYéJ\x0003\x001dÛ¯Ô»à]á¹µS^Ãi:r\x001bøÚÄ8À±Ñê3\x000cæE\x0015i^Râ\x0005ãb\x001fúá\x0018h?xjr ?§vy°\x000cÉFú.H)\x000bþ0+Ôo2R
b
Ù\x0016IÖ|b§]KÅå¢O
ðO®\x0012FraßÏ\x001f´E×«VEÃn?øk1é·âÙVÄ®Ë³£ë\x000f`\x0017U°UÕe
µ²n9ã;±Ø\x001cFîPqµäýK2/,ñ\x0011£¼ÎÎÞ\x001fêí\x0007\x000f¸\x001aÌÁå_\x001d\x001bå¥iKÐØÐKÞ/öçì2:Â$É\x0012\x000bÅ Jü¼NÆMÙö>\x001c'\x001f>ÍQÃªñ×dÊ|/iew\x0003Ç_"?jÃ>#ÃG\x0017~&O7l\x001a\x001böü;ê\áVÃx<Ð<ñÓíÌÂ6]\x0001R÷ÐñÈÏ&·¿\x001cñ9£RBìtYI¨ñ×WfÚ\x0014¹ÿéÃ÷?~þòî¿}ýÕ\x001f_é*ß|ÖÍµr%NEi(][oË\x0001VÄòÆ\6J²3\x0015K\x0013BrnÒã\x0008s]±ìÕP\x00076;\x0003\x001bÌ£)6J7¨C°[Áu	\x001f.ìÂãv\x0001T\x0015}v¼g\x001b\\x001fê¾2ÖÊ¼vWÃûõj´}ÍÃ5·äõ\x001aK«[I\x0001¯Ð­d«iÙýÐºWCK«\x001aZQê\x0015Ôþ4«ÃÓÍU_ùËzA¦U\x000eMM!n¿:6eÜiªú·ë·,©\x000b\x001bÝcú\x000e\x000bGÙ0©.¸Þò´¾§ÒFjMs((q\x0015I@%"f«KQ/±Cçg¿~|ù÷_~ýî¿üþ÷ïåüùøîïßýòòñµò[uALk=ºþêÑu¡È[4¼­ìe2-3\x001f>aG\x0008]G	Ò¯wþ1ú\x0004`Ê\x0019×Ò\x0014\x0018BøpzïF1TvSbsY-\x0012·Ò\x0001.9{\x0015d7Ï\x001bm"!»þìZ\x001e\x0017\x0003Ü"!£$e6	ô*\x0017\x0008åäë-éÄ\x0000\x000f¸ÕTï\x00062ìÑPÏ¸:\x000f27±Gº«\x000cÞ
Ó
úZÖ:-f3%ØCéäÃ÷´Ñð\x0001\x00140ÈøÉ[æóëµ\x000bá­Öä\x0003<\x0017¾¨ =§®áXõWm÷²¶òÒ\x0005^âttV\x0016Ë«EbiZjoº<|Pgéììî\x0017øÌHNùßÖõþ¹Ev#¬x\x000eWM\x001fÀùý¯\x000eîíú^ìc\x0006v¡ËÊ¢5ªÒÐe2ëÒªne#L-\x001e/\x001dÜcæüpJ~óí\x001d?'pä÷Ò*ùJ[h*°ÐÙXKøÆN<+\x0015\x0007ø\x0005r`ð\x0016ì¯¹¢\x000b"&9¦® ¿ÛÏÑ\x0018³wÔæIÁ\x0012Ò\x0005\x001epà5Ð§Ê&\x0006ªÉÇÇmË\x0015ùE±ú\x0002GÅj\x0015ït\x0005ÀÍ¤S9	õÈJkÒ§)\x000f8åU¦<añ«2\x001bkê+vZomT¯Ã\x0018ÐÜI_R`ÿQ\x0004÷ÅF
c¸-ì\x0006'1Vw³\x001bx@úNÓHÀ[L\x0016üaÎÇ9c
Ì\\)åOáØÓPkfñ\x0006Çç\x00064
ÔYîJ×b/\x001dô\x0017vD-moA¨¾XjàT<ëÔ\x000fÝÞUD¯cÛÀG¹¹\x000b\x0016ã(·|3©Aò.tã7FL÷õÌÏdÝ:ÀøÒ\x000eY\x000fÈ£d¯\x0011knBõKÄú·/ï?hõÝß|úÍ_þíË\x0016ã½98K79ÓLy¯<xv·âC;}ê[wÎ%mþwËTN
ní¾^qm\x001d8¶He\x0003%©»^\x000b$ÄCB;\x0018Í÷8¾\x00028/.\x001fËíhá\x00176]èÎS´à
µti\x001f\x001aoê\x001a{]ìM\x0017ºy¤·F°@ÐÚÌHç¯f\x001dÛ¢b»Áß\x0001´\x000b\\x0014K\x001f¦\x000e¦å\x001eØ\x0018µædnÎ.L}~R\x0005\x001fÍj¼ØâÊå,\x001aØ\x0019ÝOô\x0011\x0002~ê6ÑssÊ¨æ¹E1l;2ª\x000eýOJ-\x0014ùÞê:ßn}\x000cl|$½¿K±J@Ì.\x0013\x0019W9"­?j9E\x00078^-ÊÇCl\x0016hÕkhü\x001av9¬pýÁ­-Í°{\x000cë§¨hB\x0006^÷ÑY\x0007§è,É\x0006\x0007²ÖWNvvàéªí+
ÿ&\x001a~\x000eø\x0014®6ÓÇô¬å#Èæëã	;"vt÷ÒÞ\x0008¹U$¡8ËÝv\x0004~4Ó\x0005\x0010\Þ\x0008à&RÕ8òò6Nñ?)\x001eÏ¨\x001220)SuS;p§Yéqßao\x0006rª³\x0016-½ê¤
`\ôe:\x000b{h¶¼V\x00078Q2ÌÓ74>'Y¨+ÝÁ\x001bß#¬^\x0003\x001c\x001b\x000cÕÀ%Òþ!\x001f(7Ç¥=nÖþ\x000b;\x0010k¢òþº\x0000±Óæl¢Rá´\x0010\x0003.D95ÐÕfV"53á´µT,Üä\x000b\x0019ùýAuà0÷
©ô\x000b\x001f´M$8.9Ä\x0001\x001e1èUÍ\x0004^\x001fvj\x001bªS$\x001c{×Ãâ}ta£÷Q0Lhá3?ø&¯i'.<Ó\x000b:Â°5
¶JEv\x000f<µ/azµÎÊ\x001e\x001bØÄ\x001eSò7\=Æs÷¬6q\x0000ßÆ½
>_ØX5S\x0014¼È\x0016?\Ã±ÕP²µS\x001c®D\x000c\x0018\x00131\x0000ÊÓÛ]kïÛ\x00165Ù\x000b\x001bN7äÈ¬ïk\x001c¸|Gp{Õ¤S$0\x0003le¨;Æú4¼9â®â.\x0003\x001cÅ]d_\x0006\êÉx_R)V\x001fM\x001a»å¥áá\x0002Ç qI´­ìîåüôxï-}ùô=3}OíoBpÖª³pZã¦ûd-5ä\x000b<O8>YÜÏTWé}ÝÁ\x000fAPÆF´¥A\x0003/lãbÒ\x000eµ«\x001f\x000eZý\x0001P
>Lw[ßÝ\x0019`å2\x000epæ2Fr×÷ÊDõâYéÊQåt\x001c\x0016<\x000ec
¸?Û;Àírôç\Nñ\x001b\x001c6å)eqà7¨÷q*	F7\3ë\x0003<ñmÄÔÖi\x000fù)q×µïÊéd)x²$ëiÇÉ¯wê¤Ó¹}Í²sa#e'É¿\x0012#\x0017$ÃT4-¼
/
l\x0014^2j7ðæl\x0001\x0013\x0002Çz\x0010m[.pl¸UGö
à9ÍÖ¼âJYW\x0017¿%ù?¾þáu³$6Íµ\x0004à¯\x0007ï)ü*­2úÔ\x0002uÍÜP\x000bVøÜ\x0006-:­ª\x0006,\ZJ\x001e¦À©0µÀ\x000e_ÛÍÁß Ñ{Ñ«%@ûÔì\x0010YÔilït³es
5ðBAÙqsS0C-{÷Bíà8òúHÚ\x000fpz0)yv\x0007¾pÍ.päí×Ï7×^Ë7lN¸Øò
\x0018xÏjùÙa'}\x001a!ÌaÆ\x001dÁrì\x0000Í\þÍ¢êX¹ºSÏ7l¸\x000eÙxðÞ#¯üþ³g¼;ç¹Ý©Ó){\x001f1*ONï_ë-ç½Í
-îZQÅ¨NÂó3Ò®÷²þ]àhú§m\x0010îQ¶&Õä\x0003ñ´ÈM¯àK\x001bÚ\x0005^)v2`!¢²5qa\x001awñµú~Ag\x000cnÈc±\x0019\RX9
m«í)ÃZñÙG?Z¹)8÷æ³.íº@ÛlF\²\x0019! mXB<\x0012\x0018ÓLàñpKÂ!d\x0010\x00062MrôºÛ«}1r» ÑÈÍ+\x0008ó\x0006Ïp¦8:#ÏÌÓÃ:.\x000fëìèñ\x001b'Ç?§;<äUöÆä¸%çüíç\x001f^þð»w¿üðýç/¿~¥»»z"vËÐ½~(éÖô[ßXøFÞG\x001b;·õy\x0012Wjr·Ál<ú©Bèíc«k*/+c`#CK\x001ah@\,'ÇKüÂ­Ê½29\x0006629\x001a[þ¹\x0000³6¨\x0012M7°\=ä<\x001bÎ4½ânfN33§Æ]\x0013R¾Q\x0006Ê) ià\x0018Ðèëã­kFÕOÌR(oËp¢XX\x0017xÂ«'(ú³kö7MvÒmàkd`£þ[ôø¾O¥ò¬L=ê¶¤Þj\x000eS\x0000àö6ynàY?*Ãà£§à\x0004^ÉUp»a¿¹Û[\x0005å0-\x000e}®¬Ô$\x0015<&ªëáÆSÞEèÝJå¸Àqä5ÜvQ
.?	±ÔXi%ÊªoáÒÒ"r©uÆÀ´¨	\x00053\x0007E"ç.\x000cº©@ÆR$Ó\x0012ñI´\x001d¥Ð´Ð±ÈÜÒ$}aW\x0014¬\x000c]æÂÖ$\x00199r\x000b¶öÍ7ßM	²{L\x000e;ßcM´?uÑçÒÁ7\x0011j\x0007'
;ðHnà
\x001d3ãXbÈFûÙ\ß\x001d» £©· Îë.7¶L9ïOÓ¦<,\x0003<  ¦­\x0001ò\x0014&«É¡mT=¦9ÜA\x0001\x00151%è¿ûÏ\x001ax¡ôvÎä	¼1PN\x0003÷¤#ëo"dÛû=îLæ,s	-+\x0019N<Ð"O\x001e¹3zÜò¬ì§#±c\x000bËû\x0006ÇU\x000ef
ímt!òÍ)Öëà¸X´q\x0013\x000esm/ÄEþ'qºZ\x000e;n\x0012
<À®Ï·µË{Ì\x0016UïÏF\x000bgÿ\x0002÷8-æ1Dl\x0017ÿTÎ«s\x000e;´È}uý¹À\x0003¶ä9swX·h(qT¡)VZ'T\\x0014d.ptÏ2]\x000f¢!G\x0003\x0012ûCjSJiÐäi"íý¢zOÍéq\x0015_}M0Û\x0000û×_ßIúûþwï?ª\x001a÷ß½ÿQÂPýoÿíý\x000f?|øí§×jÆ©¼\x0015sÖ×ûý\x0017>n,zrÊAª\x0001Þ
>Ø°£\x0015­$g37ÌXÇU\x001eU
À$²þ§ÂvûÌ»JÇ:Ó-\x0018R`;R\x001b8ÚI±G;+Ï¬Í8\x0004D4ê&~¦³eZÃyûX\x0018ÐôXPkzP¶L¶\x000bCûî[»²ù\x00064R\x001c-\x00152r$oràpÞw\x0005\x00032¶ë¹	Á¼¯d[©>³ÏÖR¾\x0012..lä)w\x0012èÉ©Fû\x0003xO¡ÈpÀÆÜd\x0017\x000eÄúÂI<#aî]ü+áÛôN\x001cÈ~(ÙÌà\x0003gæÙÆÌ÷Võy\x0000\x000føìS\x0011\x0006¸ÎCâvOÆ8Ú\x001e,®Ã:±D?N\x000eg<±<Nc\x0008O¡|«vÛµq§i}C\x0004
Éðk-<v%«õÅ:À+m\x001eéà¸´{$Ç\x0011qßný:¸³¸XjÆ8©G\x001b½Xý\x0014åä[#â\x0001Nnòîñ§i'ab\x0016¬<ôø$ì-6nÑ±¼Á]"\x0006»üÁ¶az=ug5\x000e¹°Q³ÜDÌ%;S\x0003µÒª\x001fj{­Ïá\x0001NÏa­ëF¸í"w{ìù\x0011Ò4ÕÜ¦\x0007¦cgzjooÒoÝÂ-«zXè!¥X¤¢h!ÊºÕv ÙJøîà\x0016	ß*\x0005ðÌxÌ±Ñ0à\x0019Ï3;ÓnMOë)£ôn@(ÕæéFnßPÕ;8RÕå¾ÇwBTëòÓ·
|}&\x000clz&È¿\x0002Ç­æYEÂN[ßwðz\x001axÅËS\x000c\x001bA¾\x0000¿,	µÙ÷Ê»76>A\Å@^N$fºÔêh§Ú\x001b\x000fÖ¬L\x0007\x000fQÚ9|ÍÈþàÊ?¾fã mzë:60\x0000¬³énÔWð!f\x0007\x000fm\x000eU´ï«\x001fÖ!YÉN\x000fmeäÚÓÈMê¢Á)\x000fR\x0004¶§eÒ_kÄdðä\x000fk1uC1ÕºaºvÏé¥m]âïÙ\x0019²Mw=\x0013×\x0005:I\x000bx/Ë$ûµdbâL*-ïîÈ¾¼sþñý×ïþÓ§_ËSçu\x001e4ÖOAßÈ!c¾Ele0µrñ[r\x0000\ëÃ]8\x0000KìTK\x0017ÇmPk\x0017\x0010é6\x0019àäÍÁf,¾o¸ÅÁãF\x0007\x000fùWY¹À°hEt]µ=¥]*\x0007lØêRþ@{&®X_éïÉ¾\x00134\x001c\x0013^vòc}*Ø¸j[\x0018{\x000fØ§ðÊ9\x0004ìÀ6ßv²bñq§ãØ#Èõ¹ßý¶^>|zi\x0004O¯e¸å\x000cwyç¨ùÉëôP·DykÃ-»\x0015t\ý(ë²\x001bLÎÔÞ©7\x0006ÅXL\x000bW¢e#ý­Vq\x001d;ãÕæ,²\x001cíç\x001cUî¦KCí\x0000wè\x0015æ$ª\x0005²|f\x0007\x0002½Û\x001c0ÌW\x000fàõ @6Sj]}i9£Ùn\x0008·ê¯
ðiPM$òt)G&J4Ã-ò
1ü\x001fØÃò´ÝT÷È±w²f¥à¬$d§8ÙÚØ<¥y]¶Û.\x001b\x001b'%Õ[\x001d­½hÝgÊg¥;',õí1³îÃZVahÜ\x0014\x0018æÒýª]6±0å´n\x000ciu­\x001dÑ¨\x000b\x0017IJ³èõ«4â£ÎôlÓ\x0015\x00124päÈ0õn©s]ZR\x000fØ7O@\x0005Oë\x000f3_;\!^Nì-çlå¨3æ}8¯ô\x0007\x000fvÉ·b\x000fZñspµ.5¢M\M0:tæe¹\x0012Ö»Ã¨j<ãÔÛ#Ïª&G\x0019Ws¯\x0001¡¶'@\x001e5DnÙP+j\x001ex°­ÒpZ*\x0011×\x0004pHWím3ÏJ\x001bøÆäºc'ºÀ\x000bæ±ÂDÜÄÐ®õgÆùwÇÆ\x0007¾¼²0Ý\x0019¬ec<ïïeS«\x001b¥¥¥o`'O\x000b%PrÙ\x001b~(\x0007ÞÔ\x001còM\x001dà\x0019²©6&º5õ
]×6Z¾\x001fä\x0003Å5ºïívWXóååÇ\x001f_´ñóÏò_~|`Æ³~U{GöêwYüÛFö!·,À\x001cË¬¤t¼\x0016oSòá¯ùÖL¬\x001f%Ö¸ÿ(¿xÿñÃ§\x000f/¯Dºöê\x0017AK$t­Ñ(Ð¢2eîmEÃclþë/.¿)ÆôMø9ûl1\x0014øÀm_V\x000f?9`Ã
ìÕk\x000f:b\x0014Û\x0005æK ±Ýwýã\x0003\x001bØò\x0015Êw\x0016>\x0002³:}ô\Ö¿£ñV=m!|Õ#\x0004[N\x001b\x0011Ðe>\x0014Æ.¢´¦\x00066¤¼s\x0019\x001b(Ükøóq*<û^ì·k\x001a|C\x001aÜË£\x0015«\x0003\x001aÌb\x0014ècq\x000cå\]vY6]öóß½üþÃ§öûÿ¯ÿû?ýúËË÷¿{¥\x000c«}ò\x001aªÈ	æçÞ¤·~ÉjãN6qmÂ	l\x001dbºTà,§(Y'©\x00176é¹»Üò\x001auÍ\x0010tè\x0019\x0002-»=þ`²\x001e<\x0007\x0001%\x0010»ËËT®B*Ð½ùè?¼ûO?üáËû×òb°S;}\x0018öòd#ZûÕ\x001bw³äöÜ¿ø¹ûg6n\x001d
 \x001aa±\x001dgIÜØÅØä\x0016V¾ÐÀFY\x0010HOî\x0012S\x0007?F]ê	k	p`c	0ø~Srïq)ZÞ\x001eL¾]\x0007\x0012þJøÁ elÈá»	M\x0013ÂÚ(~thRü\x0008. :¸æ»©\x000f]\x0011\x0008|\OØØN'w+JF¥fR'KàOr{¹µÔÕÁ\x001döÒ\x001e\x0016ý7wL«Ñ-÷Ø\x0000'\x001b;Õ\x0011xº\x0013Ë\x0013a>ñçÐª\x0000~
\x001c:¸GAfí\x0017\x00077¸ä+õu²¢M=º
~\x000cd\x0014üW

;yö«l"¡
\x001c½«â0'\x001eµ4R\x0000w¯-jñ¨\x001b3·þçÚäDÂâG:À\x0003úÊ\x0012FwÌ¤ÖÎl¿Çr\x0008Å¶]Ú\!µÛ¤x\x0004·7_µ\x0013·EÁùk.\x000ef71OC·\x0018ó¨d=êH*O\x0010\x001d²J¥Wª÷ê|¶²Ë½\x0014¹ì"¡ã]2n+Æ°\x001cv¥ðr¬v½¨¬	ëEõõÝÏÞþÚ.¬ÿýó×ò\x000ej\x0019o¼:s·®³ fxÑ~·øÆ\²à7
\x001cëê¡ÿ3Û[yBÿ\x000bs7¥²¹\x000bo³\x0012Õ:¸Å­&=·¡,z>l)ã\x001fßx¿Ðê\x0002Ç¡\x0016ó0OQ\x0012½\x0004ä»u\x0006ÅÚÚ±\x001dZÊçÖUîV°ÓÖQïb\¸<\x0003Ü\x0003ÁµÍ=Jÿ^kî=ÙÙø.d¼´ìØ(iiÕ:Û\x0007»f¦q×J
¯j\x001a×2«k÷Ø\x0000î1½LÁrÂ\x0006m×ì\x000cK0{_ZÜ¯l\x0001\x000el\x001b\x0001/wÃ«;Vo\x0014p)\x0014ð6ò°XÃ\x000cð}J*ñNV³F¬
^\x0016y\x0007?<\x0018\x001c¹6þ>¥5LâÀ#\x0011ÈçnÜ°ö¾]ØSáÖÇ D½\x0005(\x001bç¦èÉÎâ\x000e§I	0)ê¥bïûÖ*´\x0010v%¡\x0003yJÌ>M
øôZ\x0004z<5ùF5*ìÆ³[ª/®2¢\x001d<¨­¾¢#Ú<¢)S÷\x001b\x0004¹\x0013'\x000f«<arµÊÞî[yFbÈ9Aì\x000füP9\x001c,	ù6ÕVôùIT1eºO¶é(lôY:6ê³8u'í39\x0017ê	yà5÷¹\x0013xAð\x0010p±\x0014W[ùæ\x0001gQ3¹2ÛS6/®7ø³Xº"\x001a\x0000W=[ÜB\x0014ùÜÒ.e¥Ávä\x00024ØÓeýÍ¾åbjG·XLUÏÍ»:¡n/6ÑkO\x001bÔ2.\x0001éð³Z©v\x0017ú³÷²\x000b\x001ec%[µï\x0015§\ÍN\x0008Ý7\x0013\x0000eÐ¨¶çßÝ\x0017³1ðþ¬¬x\x001fôÐlàÕÒ~pk\x000cîOÕ×CÎ´Ó¾exe\x001d®¡öçVN\*Å8.$ÊvùÑ\x001d¶qâºÐ¡\x0012ìÔÚ><7¨º\"3ÓÅ\x0012x56e@-´\x001eÀA+H\x0016\x0003Vvó\x00113SÕìf»þÝt*\x000etàÄ95Ï5î\x0012U'Õ'¯0ºé=§±'\x001c»Ç\x0013]|*¨*{41eÄDîÞ~ð 
f\x001a*\x0018GÉ
Õ\x0007¤±×Npvñp4¶\x001f<ÝDxå8	3µu)»¸r?\x00076p?\x0005;wÜ=SàR¸GÌ+\x0011²Qy×\x000e´üþE\x001d½0ºÝ ËÉ¶y ÝQ4ûúÈ+\x001d²(-LÇ
%çqàPÚ§J5P9Ã\x0007Ú\x000fß¿R\x001eQf\x001e\¸{|Lqù\x0016|\x0018Ý\x0014:ñoªv\x0017u½N]{aoJC¢âßdd&'2+EÙÆ>_ù_\x0003L/T¼\x0016d\x0010ÕUØ'í¼ÚôBÖnÝ2EJ¹K¤\x001d]±\x001b\x001b`s¾ulê\x001fÊ¤\x001e/1%k^»ÄËc¸âlöY«e\x0008(_«§TîMÌØ©7¿ïÔ
KäJ4¯zÜS¦ÇÞw²{~tp²\x00191HËÍiê}\x0018g<n¡~XÖu¼sr\x0003qR¶v\x0007¾

p\x0014þÒ÷$ð´³ô#3uªD8}Z+Öå^³À4k&\x001aCõÝ\x001fq!¼\à	\x0017ùþ¨ùæ9¥à»`¸Ì#\x0007;l\x0003[Ò&ËEêÚ=6F \x001d@$vÆ\x0016Õ$Á\x000eÉ¡ÅJÇvîvÞaä(fÐ¦\x0005n\x0012°büC\x0006ïU·ø¯^àè¿ª*ìÝR?\x0006ÈéxÍ'-î\x0002G»è\x000ce!f\x0007b${Ä«-Ì¯
m\x001dÚcC[\x000e$²(_¯ñ!\x001elÇ$£2Ò=»Wv\x0003¨J.Ñ)°æU=?2øD¤ËÍm2\x001fà2Ï\x0002>ç\x0012ø-Aý&*°q
$$øñóÇ\x000f¯\x0012\x0014¨0$×xJk h+*I\x000eyûÆ¥ä=Æ®j2m­Kï~ÊnÿoÎÁæ[l\x000bü?¼ûÙËû¯¿ùñÇ×ÊkÇ1\x000eÇûrÇiNUfÀ¢É
\x001575FLqÃ£YÅªm«Â©¨úS5Ç;É\Mè°Q_¿\x001e×¾¯\x000em\x000f*o °»\x000b®\x0018§^\x0004l{<²	v:2\x0004;j5~+\x00176{ÁÌy\x000bç&ÇEß\x001b¬\x000b\x001c^¡Îâ;Qßç-hd\x000e{*_EÙÅ`ð\x0002\x0007A\x0019¹Ç\x001a¡óÍ*c*-úç­àâ<ÍfÄM_:'iZÓ§k·ãµ+à\x0019'\É¸Àý´Lºt²_Ý:¸·j­\x001ekÉ:ÿØ|è´àG\x0013^}Â^C\x0006 Iì±ÜÓ>c½#\x001bf Fà¶UÁã®-ëÞ>üü¬õ)\x000e:åËÐà§B¸w²íX,Úò³\x000f\x001f?~þðåuºPêq(Ð´iû	-\x0001¬Ee¡X{äöÓ{nòà®Ñ6<¸kÚECEPPñéÑÒ½º6iÙýÜe5iR\x001dÕÀ\x0002f5T\x000cl3é6ÝX®c\x0017\x0018w²	c"íåðXé×j\x001e\x0007ç­Od¥²\x000cìÊ"_ØQ\x001cÊÀÚP?Ä«£´pË®>\x001dÛZ\x0013Y=(¨ÅÊ\x001bÚBÌ\x000f^å_Èÿ\x0017ôCþa\x001bM?I
\x0016\x0010Z\x001fV\x000f?TÁ×.ß\x0001þtùº.-\x0001sR°i[ç_¥ö·Ði¾-Î·.\x000cxñ§\x0018X!ÇÃ¤bÑ¬?WSô\x001b<ÃÀÙg"y©
Ýëüä/Ýü{Cðéà@ðÑY© H¢â\x0001°Ó¤Ó»\x000cîÊ¯\x001dØ\x000f¿öxÎ|ójùÌÃ»\x0008S.$)ÍÛÇÇiV\WªÝ¼W\x00068LyqËcÈà\x0006#GºrÍiã;Üø9[êeÀ²ÐÈí¬H×µô6¯ò\x0001#Wö7L6áã\x0015\x0012k\x0013\x0014ãúÈ7!S\x0007/8ç\x001aQRÀ³Î9	³*õ³kìVKÕ¢-OUm\x0002Ó\x0012Â¤\x001fOB¸\x001d\x001cp\x0015\x001cúäÙ³Aùis×\x001d.y\x001b\x001c9Çà@~A*- ¸~÷|¼\x0004OMÒ\x0012M\x0003AgKoãÏTêó§ß~}¥\x0018¡Àmä±i;¿GI\x0013à²¤ÎõmÙCQìM§jXS\x0004ÞµL²}¾×´4\x0010ÏÇ&'z\x0013Y\x001cÛÒ^ÿu`GØÎÞeT\x0019È\x000fmeÕ§µec÷£Ú\x001c\x0015\x001d\x001b6îgåJÌâ=)\x0001Èþk5çõ¤\x0018ØpRxµb\x000eÏ\x001fù_²\x0014²¼ø`Ô*]9 \x001féJÎ\x0015­FÃ.ìpg£ë\x000f ³\x0006	
Ü\x001a\x0008\x0012´a
²wÿ\x001fsïsi\x001cm¥1Ïb"îç\x001eQ\x0012 j¨á\x0002\x001aÉf\x000e§bÕLU¥ 	h@ÛÐ\x0012¸\x000eîD+{xóÅ%\x001b ~ K\x000fZe\x0019|qñp77÷\x000b&ª\x0004|éí>ÝÊsG8á.Ëþ{f¼8/Óâ+L\x001aFê*l@uOÀ;«^ä)òÃn­BµØ·ÑPÕI
m¹\x00076'»Tv­|\x0003\x0007­|\x0005o]÷*b\x0012\x0008®ÚÔ»Âï÷¸a'¸Ç\x000b
â+Ú\x000e\x0007\x00146­¥cOæ._ít8¿¾(\x001fÎÿ®¯z8\x000fCMKÉôçÏ¿ýðåxêÄÂÏ\x0014ß\x001aòðl\x0005»X½i;|ÏÙWw uîB02ã`Í¬\x001c	øúJPÆ³3W®~d? w\x0019\x00174le9¨Ï2\x0014z§´Y!Pþ·1F/ãö\x0001Æ­Ò\x0007°Ý¼º!ö¢\x0002¬UÞ]Yt\x001f\x0000ê®\x0005>õ'Mü±ÎN±Ä¯øãçú¨\x0004ª²Ýh¡Ê\x0007}\x0010ZÃ!ñr\x0017Mõw(ý²\x000b´ÈäOe\x0006s$}ý5\x0012¨.g2VõÁx§ó5-ç«@Ëá
¾Úná\x0008Ë4¹\x0012"úÆ;À\x0013Ðx­ö\x00021&Q± >)+!=õ¾\x000f\x000c\x001cXHN\x0015,áE =\x0010óÒAÙFÛ{:d:
\x001bå\x001bk«härf\x0017\x0008\x0015î]xÚ\x0006\x0007>þ\x0008©ÿøù?JõEb#z³E¹ÆNé>2À[±\x001bï÷Wà94zÈô-\x001e·?çsqú.Tè×ñQ~þõ82\x0012ÚJ}|\x001a¥<Ùê¸Ví{7H\Ò ~w&Ù\x001bç\x0013v\x001c\x0002ïçæ\x001doÅ¸Uíàú\x0002aà@\x0018­ÒO±¿9\x0000©ã8ôBØq0Óü®1ùÂÆ7\x0014Ç·A¡Ó/ÊÃÁýxûv8ý\x0006x+\x0008Þu\x0001\x001e_¡,÷@ànÈØÒ~iIûÉ
Ò·Ç­\x001a°Ø+­DtÄ\x000ey\x0010CÂ=:°\x0003°G£¾\x000eò³8{§X³K-xÓ%1Ä6§'h oòTÆ'«ó³R³\x001d#.3$ø!£­tí¹cAÌa\x0019¸\x001fÝq\x0007¿
\x0005Áý°e0KJ?\x0002îxàn¼D\x000e~Ø\x0006~Ø·óàÉ¥øeàPüÒød«fHÆ wÞ@\x0012­\x000eìCûa\x0007\*½@¼XU¾: v¥çÙè øËI¥èKENûw?âÀîd!à\x0007\x00079\x001eR'\x0006\x000ejØ*\x0008ð)>K¥åÂ³R\â\x0019÷L{âLpT2ð\x0001fE»HxÊË2-¥ØdWÔ3ð\x0004zQö\x001fDlU)ÌH!
25ó2tòeÎõ\x0007¼&\\x001a\x0007U\,\x0016¬íÄÃ¡ùö=3~ÏØ\x001daÓI[CÅM=öË\x0004\x0012×Ð´º©\x0012 VË?Í§aRG½=,È·
é\x001f?ÿ(/\x000fb~:\x0006uêEÜ\x001e9¡Å±\x0005~Ìý\x0019­Ó\x001fh\x000eÞ÷OO\x001eÕ
YßÁs=@\x0016ËàÐî\x0007¦AglZ	þÓó\x0006eKWÔ\x000eíFKæîü8¡ÁùQþÓFJ!5\x001a¦`sÆf6«^r¹//9ù¾\x001dõìCN$`¦ô\x000c~½\x000f?ì/Ãý%Ø	õjäÂ"`~Ç¥\x0010Íõê2ÛZ"\x001a\x0007íggÞ\x0007'ø	áøCíÅ°;:9R«Ù°ÙÊ$9óN<ð~³U\x0018¡ù((ýùyÆy-\x001fSÓçú¼$#ÇsÈÃdëhÇ.\x0018ç*d\x000f\x0017oÓ\x0010ë¢³ëx9\x001fè³\x0006\x000eôÙ GØ6ljßLÜ¦\x00188¤z\x0005\x0013­ºýDÓÎÿÇç"|x½ØR´õGºDÜC^qÁ¨¾k1§åC1çÐ¨&9	RÝç¶¼8ú±Êþ´5èâv<ú7¹/Ç0»Â:kMÜªaWJ<º:%\x0010ÿ=ó³9¨çÚïaØ(]"lTmRÿ\x0008"zç@\x0014u¹ÇqyèÕ®fu\x0001/µ\x0000j\x0004\x0005\x0014\x0017Ëì<)}T}ýî	;ÁÑ\x0013¶°Ñx/TÆ\x001fÞR\x000cn§Ú¡ÞbØÐ:è\x0002\x0019`åRJýi±ºï¡U»,LyÑã\x0018üfåñGÙ©ä\x000b¯Âj`»GÇ\x0004G¬²+\x0000®I\x0010`*ó\x000fe²è/ßSxÀãSªVð¤\x0001pyNÐBÔ¶×ñ^¸|Ïß3«Ä\x0017¸ÂJ(:
£~Aà±Pÿ~M\x00198º»çô0aä§9X\x0016ÇôÄP-2>ÜSÕü¼pä\x0012fW®'XÈ+f\x001cý£¾\x001fúrÿüåËO\x001fX!r"¡µ7½¯õTQåE]Ïò÷6Ê':ùþÉ§ÆôCÜh­\x0004¼ºý\x000eëÊùÅHæxx~öÅI°%°\x0007lUNªX\x0016¨g\x0015|\x0019BUû%eØÀ\x001fuÌ\\x001c5Ã\x0002È%2+ZþxÉÅuÇ¹¸Ðôäy:57'«Ú·Ek#X¾ìÐ7ð--E<s"ïl¦p\x0012\x0003Z[ÈÑµÝHj
5\x0017`áhN2<³"ÓI$3¹NÒLðé¾1ÍcªÉe
'ON§ª\x0019+\x0004éø²IMl\x0011; ~Êû"eK°;\x0012J<4\x000c\x0019vñF¢öµ
}Å\x0010VÇMR(ZX\x001a²Mð\x001a\x0010<¾-\x0006x"~\x0013\x0005OÀGxÚD'xòPaõ>AÏ¯\Õ¸fò9ù~-e<\x0000Ó!©eà\x0001¨/\x0012/àÏPcÊ\x0004Î©¾ÐÜà¦C7 #û7¯W§E\x0016bÉ´Ê9¯#7\x000f\x0010S&øA§ Åkä\x0012÷ñ\x0016âÜChë;x7¾äqZ(_»#á>\x001d¹çÍoÞCùp¿\x001a8RðÔ8?K±N×ªgµôÊ#ïCö#\x001fHA\x0013\x001c\x0018*.5CÐ&XÒ\x0007\x0013piä\x001e\x001bb(\x0018Õ\x0014\x001dm"Æ´S¼\x0013xc3úÙéXos^aÎ:|'`j3Á
õx\x0012\x0014Ð@±\x000f4VÃ\x0006\x001akëµ¼É\x0015;P
A±Ù£w¾íþ
»¿é;àQZ\x0019\x001d¸ÔÕ]¡\x0002\x0018\x0003»]¶þð`«ãs·HF8ò¿\x0013«<vó\x0007ª»Ìã\x0004ïx3«·ê\x0013u¥Wã¬Ô¸Ä\x0018÷v»\x001b6¨5õs|À«|\x0001\x000e)Ø7t3Ên\x0007²ö\x0004¯0-)à\x000fÿS\+±ppÝ­ý³\x001fÈÚ\x0003¼;\çÈî[QáH¸].þ\x000eL\x001c8C#H\x000cY\x0017&'\x0018º	­ô\x0003Ékgò·E,1\x0004»-ÒÅôÕÜå¼õàn#à©\x0014ï8o=q±3z´®\x0001w(#\x0018:PÁ[\x000bdB#1-;
®Ó<ØÓúb2ô\x0002\x0013SS|»lÅq¦\x0011H¥pè\x001eêæôÎ\x0001î¡3¦©¦ù#øåjép\x0013ùør¿Ü ã\x0007;4ºU
	G.ß'½f.ªó
t¨óÉ÷Ï\x001d5MUÛ
ç\Oå\x001eÝüi¸^­Í¯Ë¿5b¾ÖÎ9\x001e9O½½_xdõþå¿}LFÏËÉÀ>1éýÆS-7lÛÐÀ}ç
E\x001b\x0017ÕF\x0002<\x001cÈ¦ÃB1B^/²WÃ\x001bgB)\x001aê\x001d¶¯aCÓ¡ª³¢\x0016öe¢fªáâ×ÖÖV
inØ¨\x001d§"¤¨!¢¹\x000eTë«Ë[IãÄ¿\x001c%
\x001c%}\x0019\x0014*°G6B[¼üeqqz
ìé~\x0015¢\x0003sLy@¢Ì\x0002{gÌwØ)¢É£î\x001aÉa×OKê^"\x0014þÕ<&\x000f¤u\x0003\x0007Ñ¡Ô0Á\x0016 ¼º7\x0012])§\x0018R±\x0013jRÖB6M}\x0003IbÔ-~Á¦!vÑà	"*¦	^§\x001a bÒÚ·Ì5§6G~èÀ6ptäQ\x0014\x0008<v\x0002g£\x0015\x0001O*c\x0015dä{±E,¡çÖ\x0017\x0017ÖA£Í¾\x0013ÊÊ1VÂvá\x0019×3ð/GAb\x0003'Ï\x0019KqÙ\x0007\x0015mèf\x0017l\x0011êm±T5ÄBÒ*êëI}¡²(L±Þ¶zhqàXýÔtÃ3-iö\x0016=àK3Q	CÀ´\x001e>&8\x0008êiA\x0018NÄ\x001cÚR\x0011æNfùCGJ \x001e\x001aÈ
\x001c\x001bÈ}ñÈNÕÑ2W-µuä\x0007ê²%Ú7\x0012À\x001f?ÿôÛç¿ù»/¿üøQf}rf{^\x0002Êg³ËÂ¶±düßßÞÿn½!ó7fp¨´\x0013t×E¶Ö+/¶±ùzìO\x0016R­eðvÓ6O²êw=C'3\x001bÛÎû\x0017tå\x0003\x0002z¤] }F9\x001fèuì«µÌìú\x000f\x0013\x001a
¤´S\x0012z»UL:+©'÷èíÞÎÌÝð´Wyrè\x0006,y;¿_}5Uým<±Á\x0002aèH¢k¶ì8r À{qý5åÇ]Ç×À=êøvåGÂ±V¾à\x0002_²F<³}Od4û>ï¦oîÄQèÛ\x000eã
F\x0002z\x0013¿\x0015H\x0015[\x0016
IáºÕ«Ø^ô\x000ei\x0003G\x000b\x0004ÑÅ*b*xµAi<+Áô$/#\x000fhíÖÕâ\x0014­Ý\x001a+\x0004;\x0016ÚãuÜQa/\x0014Lð#o\x0011­ÄS2QÏ\x0007|¹ÿÜ4ß\x000eú\x0017vDlª§Ôùr,)+\x00037'Ê]Lò\x0005x#¸lsÙYÄç)á¹+®MpP\oëÞ

®y,Z,KË{n'½(³ü<ú~ùùë?~X¥O-=¹Õ¼¸Øáµ\x001cÖp¢üø
¿Ã\x0016ýÔ\x000clÐL\x001cü5Åü D÷lËZ¬ck'
Mì@\x001e¡tÚ'UN#GÌÌ\x001dÀ%ú\x001eÅNlbey½\x0008§æd'2¯¨Z/ï@\x0003§w` Â¦1áÈµ²DÈ\x000bÙw±ã.Ö\x0019/Ï]¢F\x0011_Çò|æVNNã!Ü:Í~ýíó?`Ù»G¦I{¥½k\x0000#w\x000eê²|úwÞ\x000cgÓiÁ\x0006^°¡\x0017í0§QG#TU\x0014·Cº\x001e¾ú®¨¢PôV^eV
\x0005lú\x0002ÔaØ(\x0011Q#HªãÉØ\x001e\x001ag4åo®gâ¦\x0003qS¿°Ã{^Y× \x001c¯Ëµf³Å';\x0019`bc\x001b¿fêAe¥V\x0012wÚÏ\x0003·Ö\x0002¿g^à¨ÊáÚ»\x000c;À#%×»ÊÐ3øÐ\x0011:7'8	gÈ°ªçYInÑ'íÞÛP\x000c\x001cÚP®ê;ò/Gû\x00178\x0004[òè«É\x001dPùt\x001aÝ³	åCÀià\x0005ÅJzD]\x0006­\x0016ü \x0012\x0003²&O\x001c®÷ao+à
È\x0006²ÿ(e9ý½ÞàÙ/²­y
ÄÜ¦\x0005{ù\x0007í\x0010æÜWO\x0010¬EMÈzù\x000fÙo\x0003Çì÷\x0000÷rÉ´\x001cà<òtb:Csñ\x001fÿí_üòëoòÿõ·¿|ùá§3¡õk}µ½\x001féêÜõé]>õNz¿ï_äx";mf4¼:Ì)©z|×k¼¼¶X°y2ÖÖ |Ôö÷CÂ°¡§$(£ðÜ\x000fC@1¦\x0004à£B¶ùO`\x0014óÏ¡¾\x0019ØQD¬íBDàÃ
A{ÍÀz*A[{§ðtØú?qFzÌ<ð2¸¾§\x0013?-'¾+éýñ8ñuÉ\x000fÊ]ÆEæ`aÛ.e6ÁÁÇ<(iÖWB<H½\x0012i1SúCl0À#Iù÷TÅ.àèT6X\xH¸;ò÷W£Ã«1¨\x0004uöÏÊÀ£Vãi;\x001aO9\x001eÒP\x0013\x001cmÛõ[}°Co\x0003ÄH\x0019E\x000f\x0015XÁ8úÅiK&Î,øe%&uÖúø\x0010kyËßSþ2\x000e\x000ffU#íõ\x00178ÌJS-t\x0004_TeË0#¡&\x0003ß¯ª	\x000e}#Êo\x0000;Îî2¥dõùBD
+$¥Ã58[ô\x000bÎJGG\x0006\x001d8¾\x001fbX\x0004vå¢¬çü½sùt}m¡Pí«-²¼Xê\x0010V*»%Î\x0004GK\x001cíî|Ìþ¼6\x001dcyM	ÖWù\x0010ÜN\x0013»C½'æIª\x0005K6Ç?gt\x0016y\x001cÈH\x0006\x000ed¤¨W6ØÉÉþ 7rL(êj¨\x0003o{öÞ°\x001bfï5aôår®TÞú±ñÃ@å\x0001\x0015|W]àè,­\x000cùs§ÿ\x001cÖb
\x000bÑ©I;¼À
\x001b^àcRÀ5³§²ÌcV\wC\x000c°íåé\x0017xAð¢¸\x0012'òÖO.,lñ\x0002ï;ÍÑÀ;öîêAòX3
\x001f\x0003P&ÓiYÉÉ8=7ðà3·õ&qªKÀ£Uûør]ÜÀ#w:FNº«Co`\x0019ù`®õCðnà-VûÖ·­\x0012@z^>({JÉ!7¿}\x0017gà Î\x001cuéÑomað©\x0001\x0014ÛôÒJ\x0003|ObMðà\x001e	Ô*S\x0019\x0008{1\x00115\x001a²\x001cç\x000f:~¥ØýY35ê©ìÂâk\x001bHµ7¼Ð±W*/´[)ñûZÎ%\x000bå.Ç¹G\x0007Oõ\x0012\x001e/ê7E³ppìS\çÐwÑ	¢\x0003úIç¬ì$\x001fy½ðJ7¦ûçxkü\x0000çbÅ¾ªiVjmf²Pz±¹\Ð\x001eDu­\x0017´¶UÚe#qWKu/×ÛG­øQu*×çº®èd\x001a!c÷7\x0003µÞ\x001c\x001f\x000201K}Nn£Âà­±Ü%º\x0018?ÀÑ>=ß´¨\x0003l§ÅÎTÊ_#?0\x001e\x0012Uv\x001d=Öo£WÂ"¹£¼þÚJý6ë\x001dgÝwä*=6jòÊ{4\x0002ó!m;Ð1m;n¤'D\x001fDLlËzúþrkxO\x0011Æ4Ø|ó)+Ç]zí/ón1ÝAï\x001dÖúø'ÀPBPÊÆÇÈK^B»ODh¼ó×?üñÇÏ?ý??¨ü¢]
ËÁñÎkÿ\x0003\x001c\x000bê_\x001e¾³CÄYïpå¶ñÇ\x0002­[Vük°á²[ÎÏ\x0011@\x001d\x0010
\x0019\x0010eg\x0004ì¶(D\x0007sç¸\*#
·k\x001e\x0019r\x0000Í#/G\x000eðkd§Yrn)p£Ùð`ä3±áÅwûºßZ\x0019§%\x001aïKô\x000fÿËOÿåË/?|\x0019\x001fö#\x0016kàNK~Ë]©ñ!¦©ÚïPÔb?\x0001[\x001ce\x0006,\Å
YÊ`Äû^KÄË	û9£eØÑ\x001a¥BÕ\x0011ËæJ$ìÜÍjü~\x001dàh±6*n\x0019>C#:¹GNÝäj\x0002³;oì\x0005\x000eEÎ8\x0015e_à\x0012§`\x0002Qq¼>Üt\x001c½\x001cwqàgPJ
SÞú<g:yýVåàXåÔLP9OèS\x0005Ü\x001aOô\x0010\x0003GzHh\x0004®ÔDàì\x0010\x0015rË¦{\x0001\x000fÈ\x001aU3Óð¬Ä´ÒqäÐ¡8"gg\x0016ìi	ÈÚÁaX|'\x000bvm\x001f"loÊNçÀFÕ(\x001f\x0012z¼ºìÍX\x0010¶\x0010OJ¯Çóí ®ø>ßþáëû·ýÈ\x0003Î³¢\x001ci	\x000e8ÐsG~\x001dY´ï)³Ø}>\x0011öv[3Ç?±­D|
ßKEÝsèþiËÅYÑ|\x000eû+uë\x000fÄ*høÔó¤Ý£Ý\x0018ÜI\x0014N\x0001Xô\x0017\x0012ÌÏ?þøA\x001a³ªçMÕ.Õ:xdê£Ú\x001e¿Y]I\x001eß7\x0002+êo|¸Ô¶Ý.s7.5l.ñí:¡
\x0004ZB ×ÎT±X\x0010·ådàúÃ\x001b\õ\x0004Q;ANØ
;\x0012ÑY\x00125\x0014ì]ã/p +¨Â;´¤;Y]ÔØ]¸£.NJâ\x001eNl¬ãj­
ÚiU\x001cÚ»Jãlj½É`\x0006\x000ed0\x0001×û÷\x0015MyºTýC\x000e\x0008rcgw$'<9¾I\x0003 rî-Ìòó^0x!\x0007D¦'\x000e¨`¥bs±g¯ûeJ"vu«Wj°§dÑ[÷ãèÆ{\x001bÄ\x0004ÐHÞ¯ßÜë½\x000b~Ol\x0014üÚ\x001aý`Ë²Aÿ\x0010m"¢	Ef}ô·qW\x001c·òX@¦&Ej¥k¬¨b/£"¿·Nlô÷I.`÷F÷æ'ñ/Ý>O\x000båí7ðåþØúû\x0016\x0019mD\x000eû\x0014\x0004¼p~ÙYú'í·È\x0004\x000f0+)Ymð\x0005®YxÀî³?\x0012+²Õþ´{a£¡\x0001TÆ¬¸Ñ)ò;Îþx+í%Î
\x001a=å¤¦Ù\x0019ò\x001cXÞQJ
\x001dWëeà\x0006®å
3Þ°EI»yã+\x0013e4Ì\f<[\x001e)ÏZiÑ±Ñæ	¼4Ó¼l Èü"bÛ2¢H\x0015A}\x0012\x0008<o'mÆVý| \x0001A;· #&#\x000fGGu6ï=J\x0013¼à´Ìîó÷´eZ\x0002ª³½w-Â	Þ\x0013¼¡\x000eyå'
âJ\x0008\x001fEÎýácà\x0005ômzþo¾\g
cRciïD¿	D¿¬ÊÊ0ònÆS\x000fx_\x0008sf­vK¥\x0001>~x¢=Ý^\x0000"]Ë\x001fåtöv°\x001cÒï³eñí\x0008
×L×|0,YTuB°Õ~ý7ä7þ7²\x000bï¢ÇX:MY:?\=8Äpn\x0006Ö0ø£XPÚ´)Ñ2ê¥oêÃc:­%E9\x0016ê÷µZ¸=}ö\x0015Ö^%}1¿\x0015¤ç_CDûªS1.ò\x001b4ýu\x0005ö9Wöÿ\x0002}z÷´A±~ï¯?~ùå¾¸ë5ÒÖ±¸Ç\CK`uxin¿KÚ°Uzdö\x0006Ù\x0019$\x001d}E%!íF#\x0008µ\x001c¢Å¯\x000c(=\x0005÷Ç°!¯íT«þQäO\Øâ°q3\x001cFõþ\x0002ztÊìð\x000f´æèfhè\x0012á[ÕqÏ·\x00198æÛ4#ô\x0017Ù\x0015âð,\x001a2\x000f%.¿wØLpè°Ñéw\x0015(x%Ç\x0011§¸<)ÉÉÎ\x0013\x001bÉÎ]å«aà¹ ¦E/uYÖ¡PímR:NJ¬8î\x0018=ú\x0005õ+Ox<êý¶Øp[ªtKÀ¯Ù¤]"©\x001fÉ»Æ\x001c%ýeÂõ\x0007ðødß}l[Ð\x0012Xgæî0¡#ÒSD\x0012æi]¥q·å\x001c©\x00078Rà\ÎÿõëG\x0019®»\x00162{ÍäöÎß©ÇÛ^\x001e¼#pþýZ\x001c^½&\x000b.´YJq­qÅ.]`Ø(Ô\x001bZ\x0011EÕ@Æ§QK»c
V¬»Û{\x0014¤êýÍ\x0017PðÕ^ON¥ÝÑJú;quCS¹á¤\x0004\x0015\x001bÄIûýºÉ^¼7\x0000WJß\x0013í\x00065á%\x001d ²t
ÖfÆ)'ÑE\x0019+¹<NRZ!sÓ|þ'ûå7¡AJivõ@5·CnÑ-moaTHOi?\x0003´_ëìK\x001aZà§n\úñaï$Ý\x0011;=QçðB-3M5\x0016	·ÒÇ~\x000cð\x0010QH+tÌDîOcÆ	»LìýÄØ?&4)ñÛ%dl¯èÿÉ\x0004O\x0008î<öÔ\x0005_Ù,Q®Å\x000ftð'$¤¹g\x0000oò&\x00071u%ÄãYß|#-f£%Cw½¨	zQ¿©0->Ò[´\x0005Ç2"9"|æ\x001b8|Ï*Ë\x001a:ËÕ \x0012Ã*GÃr5X¦µÞF^qw*õûÁ\x000e¤\x0008®S¾,ÄÔæ¬Þ¯¡w¢L|Ì¥lpÎB{¤ò\x0012é\x001d\x001e\x000eiXÂììÿøçü¸á"Ë}Ëêq·\x0008j­\x0000ÌJÓ×ý®·ìP/Þ:fv_\x001d¾q]ÁÎËnPÈ
	w
p*|jøú]YnG\x0014yo\x001ea®
uyù Ñ\x0016³P%\x0019àÛãá\x0005\x000e¯\õº\x0004¥À\x000cbµÚ#Ãä³`¶ë»°\x0001\x001fé1\x0008Õ7Jõ¸\x0005opYÚ£MRFt\x0006FÝQ\x000c^Ó%dú!ÿ	åKZ¦î´Ý\x0013\x001cÛ	tã¢¾aÏÄøu½è\x0004ºQ£;+#+_¾æût\x001b#/£µè\x0001\x000f,>ÜÒ(\x001cÔj
\x001cÔjcP'#èÈÑ\x001caÄiÉ\x001cøÚ\x00070íµ	\x001eÑä"7TÃksWf"É¥>Rm»aÉ\x0004GÃ\x0012ù¯?AYõV°O)­\x0003÷Cj!íÂ0/l\x001cx/¨¨\è39ïÇJL;õt\x0003õ4ÈÛ
)@Mµái\x0007-Z©uìmàm±\x0015A­Z}ÑâÆ0%×\x001aæò.TmàÙ¡K!qCí¡¡Ö°¸4Í´>IyÏ\x001aLpdÇiÊj%y|òûÈ²ß\x0016yÆE®ZP,\x001dÒì¸Èc\x000e¼ª7)°Ë:Dcª\x0010CW\x0002\x0015cCo*epñA^G¯BÞ)Ö\x0013\x001c{ ¢®Hß³àÈåñÅ¼6Þß\x0012j\x000fÜñ\x0003\\x0013\x001e²¯ÃÒ\x0002u\x0000JNò\x001e\x001aJB²â\x000eáÇ{52cVß
¦§\x0005LNh\x0015Èk÷\x0007/ìN
u×ú[½ßûí£µbãHÑkôEj\x0001â¾*`ô½}µô±G »öÌßh¬\x0005&¢¦r ½Ne\x001bHü#¶Ì1BòözÛî,\x0003÷\x0019ø­)÷vJý£P£¬£Ì4Ç6\x0014\x000f*\x0013¼ ¹L] Áþ ;ÈÓÉÀ\x0017ÁßRF\x0016!ì\x000f}Ã\x000e(·¢­Ì\x000eù|\x0012<#¹l9)r\x001bwmØ·Û\x000b\x001bøÉyT\x001ckÉÀ¹\x0006÷ó`G?Á\x0013\x0010£ü\x0010ò%øD1³Ää!\x000fá®°³d&vFzf¨4áò|Fã\x0015\x001f\x001d·×ÉçögJÈ\x0004ç¯ÙÞáÁïeW$Y,tÍ¨1ìõÕ\x0017xFðsv\x001eáÇv_\x0018ãsîTÞT^ýÀ\x000eWßÄ\x001d>r1ó±]/ô\x0005^\x0019¼Âç\x0008xí±s\x0004ÓHÜÄ½£ÉÀc ;à÷¤Ä=j½0?c0\x001fíÆØ¨«$XeH\x0014Æ*ªqÑQ3®÷R¤+e|T VeWÑ0ã°bZ;(Aäx4lûäÿþòË\x000f\x001fs¸ÜØ~§µð¸i\x0011ï)\x0017º!góKaçûÄïù#==\x0013ºVÉ«\x0007âZõIÀG§ü'Ü°Õ¼Ù\x001d·ØãÍ ~"aD&\x0017ûÔDIý\6lxwj_\x0007>
GÝ\x0018©göËh\x0006\x000f{Ê{cáGÝÓ\x0012¼ó=YÇ¨õÞBXµ\x0006´\x0007Í\x0006°Ô¦:\x0010WJMF\x000f¶2È\x0016íï\x0004\x000fÃÎÀl\x001f#\x0005!êEáM§¹Eö-¬½ÌxÆÒfUtü	ä?\>çh\x0003;\x0004µA­foßÜ®Ñ[ã¨µ_)s:å\x000fÓI)ñ\x0006\x001e\x0011Ü7j×,,½¡ÏP^*iØuÛ\x0006*¸Ts
ý\x001d\x001aÕÃ´÷rÉ~Ñý5pÔý\x001dM±ð\x0004ò\x0011Ê\x0000\x0002\x001d¸\x0007B³Ø\x0003z¿N&tÄßÔ©6\x0015hn­Ô\x0015Zi¬Âz\x000e\x000c»à*,	»\x0014Rèk.ÍÚÝ×UÝ½\x0000^àèèPi+·ìMvÓ\x0019JKûE¤¿sUU\x0015ù·ý ì¨|~:*ºÏ\x000f&ªÁ\x0018(	\x0004k:ýI¯\x001aäoL=üI~¥»¨Q\x0015h.¨ñ-i=Ëc\x0015ùÙ÷mfØà®¨2GÐ oàÈ¯Þç¨'Êè¢ßwaCû¬\x001aKÃiï5É:1aA®Öµ÷r\x001b4	ó\x0004J\x001byíJGßFÒHs,ªA½ï=\x001b\x0013\x001cz6BT+g\x000b\x000få\x0008\x001c÷ÊàïÍ¬2we\x00178\x0008±Ç\x0008tr½«d\x001aU~¢!\x000eèý<ÐÁPáÇ§ó@/\x000eÎÀü\x000474o3\x001epÆ£ü'ïRåX\x0013æ|÷b¹î½ªôÂ®MaêàíºLlô®lØ\x0011³cnèÍ¢ª.\x0015Ó®¦ÄÇu_íé®	Né®ó9óÍCJÁ\x000f\x0007²Ã,#GY\x001eC!lN£÷8c¥Ë\x0012O\x001e·æÔ?~a×À\x0005ÇÛMÈùÀ6pàN\x000bxJoÛï¡'°\x0014\ªcp-Í*ø0à0Äý®ñÎ/{\x000c%,\x0018#?<4'8,D}=y¬Cu
ÅB­Ì@®q8Ô½èbà\x0015.ÉµwIY_j-|â7OEê!Z2ìSîÉ
+§´¬r¶`\x0008¹\x000e*XÝë²\x0013¼â×[HÔ³ÑyyÛÖvÚ\x0007x£TwÉñèKé/s-\Nö!@Ó\x000e\x0019\x000f\x0003G×\x0008ÔédÊt"2µ/¤>¨}ý6òN#çVl\x0001À~T\x0015\x0016XH&¤\x0014ê#øø\x00016L±z>|Tn¼å§ÔÁë8_²ÑÉ^\x001aï#Ý`\x001e»~9ÓOÙèrn\x001füÛ¿þòçÿúA¤3\x001f<3Ñ}h´aH\x0001\x0001ý¾æ±\x0019¾k\x0003a9êGîI£b\x0002Úh¤¤u*´\x0001\x000fn:²+ÙÙ\x0014ð.ØdÒÔ,÷üÂÖ`,
2§¢]\x001e)ÝÃf3lL/*}\x0003\x0018P]éë\x0008Ý\x001e¥T\x001eñmØPR\x0016è=-]n\x0014t]W\x001dû¥yÃìÛvI3\x0003÷ iæuû3ß­UoY]|vÊ	xfèNlÔÀï¬ê«Å¶HØ
\x0013z3¡\x00156Á3\x0019&t²QÊf\x000c\x0003gÊY7S\x001f¸

\x001c¯B§9Wè¨È\x0005{*\x0005¼S[dðeäÁãÈµ)	µ«+[W¹B\x0011¶ÚNlñí{\x0006úõa\x0000O=bÌrÄJ;úËÑab\x0019Coù\x001769=dªo>à·YA¢Ó
äÃÜ\x001aÕA\x001c¹üß°\x0004´\x001bëpÛù\x0001õïdÍ3¸#}ª O\x0011\x00067Kè,>Á3.\x0016\x0015\x001b\x0002ð^ÐéS\x000fo&Vv?0·9ÇðC)hÃ¢cFNT9âFB2îÚÕ\x001d=ÄMNé¥°÷½cÆ_Èâ0á»ÎùÄ\x000eø9KCÍÿáãHØuq"sÃ7îäÇ	\x001eqàµ¾+\Óm¯\x0012x#ÿCYãu\x0010\x000fùe\x0003Oh\x0016¦-\x0010¸Ê\x000b\x0017Ú=«+Yr¼jnØdDÖÉ\x001e¢Ê¡ET\x0015íÍ"ðjFÙä\x0004ÇuØ\x001b9É\x0001Ië0,Ðã<Lî2îä`Ü^S¾\x000f²_¸\x0007Å}3èÃ{©,M²\x0002\x001dâÛ°Yýz# \x00018aj]²û«ÃÀ æå)\x0000¢õ\x0012+0	Fë\x0004î¬uø¶P\x0012.\x0014í\x0017{¹ÈÕ\x0019^z¾yóã8\x0014
¼¡\x000bYo9!ý\x001eùÙ¡ÿÿxZ.TÚÛD&x'p\x0004ùYÚ-,òh¾yb>¼Æu$â\x0007m	)¸Å7²fÑ\x0008<#+ï\x001aà\x0013\x001c5À}§«4ÝÑó-¡
h¨}x)oyÚÿéó?¨ÕÇÇ\x0004íQ^41ë\x001fn¼¶ýxÓ¼ø¾ÑÞjß3j×\x000e¼Cv¿_{\x0019IZ9íÍ\x0018]HÄt÷1fûÏÑäH÷\x001bÐ°¡l¦ý\x0014ØEd'°ú#÷yI8»9.\x0003÷Ðµ\x0017½«h#\x001aåÐ	<ò\x001dº5\ìò²\x0013\x001cåe½Ê÷\x0000v£ó8&.âøì&­f­
\x001b\x0018Ñkfï	"Õ\x000cd«³[¸èÉ\x001a£\x000f×\x0017\x0014Íî­Ñ:ý¥X±ðÀ£iî
1\x0013\x001bk½\x001c68)ÂvÙ®ÌsOSt=Ø {\x0016õ\ÖX:%böìÂ&Aßí×ë\x0000×\x001f\x001ep\x000bê\x0013ÑDM^#väû5ÍÒð®ã?±AÇ_½h9£¹	<3\x0005Ý2Éù\x001ez"&x\x0001pd
æBj1³~O!Z6eó&8ª\x0016oê¤üJ\x0012
g½6ÿ¦¾ìW·#/¸È£ZG\x001ayáiñ¦rû\x0011¿gH\x000fUOàîøì¦a'7\x000e¸\x0013ú'²Gpµô9Q\x0004R}åU³qj.GJÄ#E{°¿Eþ\x0006Ú>¹³QN¬ã½\x001eo«0Ò*ìíÝ Ó\x001d¸<\x0013óbÒóâm¡D\(ÚZ\x0005"\x0005!&V	/(Ããã\x000eðË1\x001eQør~ó*Vð\x0003)ÄÀ\x0014\x0012C)ø¤\x001eÝP¸Ê\x0012YÇdï¤Cgà
?¨Vú;|ÐHÍòz 6
ùÿ1\x0011Ò.kà	ÅÓ£sopíø©
»Û\x0004\x0005³|t£ù#í&Ù\x0013\x001cL²õÿÁLëèc-+ýB\x001bý\x0002ù#\x0019à\x0019u¼GbüÙùòÁx×D$p-ïYær\x0005e¨ED%·\x0004à\qJ=fp3T?N&8¬Aí|\x0015¯Í&\x0004ÞøÉ\x0011Æ»7\x001f2

\x0006\x0015tÆ¾Êðz«ïNYLåRý1lHyi\x0018Þµñ?\x001fðÎ\x0007¹fì\x0007å2ã\x0005J*»9j×\x001c»2´ØyÆÍ×¤Üî·÷[ý	Øòq±WH"\x000cÆ{|duo§VÁS+u2Érô<·¥«ÿÙw\Î,ýáÖ>g¡¨\x0001²®~N\x0013. Zèy*r¼¢O*r(­\x0000¯¤3V\x0008_Ì\x0011µ¾´=?zYÿøY^L_ÿéøö\x0012\x0018rf²å§á¯åÏ>Õ	ßùµTKÉ_õÈÿ÷\x0016,í\x000b\x000eòR\x0017Ùv¹él«Sm{\x0016Llì³òú:\x0002å»\x001e¹Ç"pV\öÙx\x0016ìáÁÄF³)}Î@Ús\x001aÙà\x0007;3@~Zã¸\x001b»|ªÍï-\x0011ámë?Qnß_N~/lìmQ¾\x001bÔOÊâs\x001fÝ¢OUÌÎq»¾
Û\x0007Ê¤$Ô»TÏ\x000fätÈ±A°\x0014ß¥é^ØÇí2`\x0007fâ(y°ý8ØüN_à\x0011'Eý \x00023.,þ!~RvÇó°¡UÝc\x0001;:z>ê\x001a\x000cË¤sÝgglhmè¨ g\x001c§\x000bãÒv*3ÎÜ§Ü'yï=ÆD6áÔÑZ]á½öÛÄÆÆ¤¯\x0012Ä\x0000¯¨í8ýx¥øqÜÝõÈÀ\x0003º\x001eÅYCzg\x0016B\x000e©1½B\x000f9Z\¾À©ë´Pýµ4¤¹ÊGJ5ì½\x001fobS?<ªAõ®×J.
ò9Yî[\x001f£ê³E\x001d\x0013úBY¡çÌfk_\x000e{Ié\x0005¾ÞSñ¤O´Vòj*j\x0014÷]hpb£¿·JÃã¬$R¼\x0018­Õ\¨NÎ^ì·ÏYðsæfð]\x001ebYN\x001b\x00154î\x001cåªÛWrU|µ\x0012#W
\x0012»ãiÖØlÅ\x0012Ax>¨Ä\x0013r\x0003âÒ¼µ2ZÂwÞò\x000b\x00197g\x000b¨ì0W¹Ø¥Ó°÷F²	\x001e®±ø¨¦®´R	\|ìÉÔh/GVÄ²©2ü\x0002|Í\x0010\x0017Jebj¢\x001cxFÂ»x8!ã@ù\x0013¦¥³b\Û&ëz\x0001O\x000eÁ#3\x000fäZ\x000e4rÇØ¦rèeØÔË"êè´éá«jùL\x000eHÝ*VÅðÎW^^MËà9-uÓ!vqá\x001d³U\x001d&\x0019Uë6gæ¨ÜQöÉ#K ,ÎVÜiÜn©S\x001bµævu&¢
w\x0007ò%µúeÜlD*ø`ß¦~\x001bwÇq·i\x000c\x0005§ã03\x0019£\x0007õ 1ä>AÉ'<Äkì|ý%ÑÌ;ïÒz\x0013¼#?V%\x0000¡>Ø+Ó\x0012eØ\|ôÃâ´ÜÎÂgaÊ
+².s­ä¸`\x000fïÇ½";¡Á*ãôHé,0)	ç/\x001b×fÙ9$\x0013\x001c­Ye£½e	FÑ4SAÁiÛ×> åö9\x000b}NÕs-\x0000Þ±\x001dX[¹\x0004>\x001d1wÆ\x0017öâl|#:«ô
¦­\x0013\x0006) ÜÞU\x0005ßUÙ·ðÆx\x000f6\x000eÞd\x0012¸\x001aÛÇm_öé\x000b\x001cMå\x0008\x0007a©¦ØòGæaT3\x000e){~~C~^/\x0017|\x0011ù\x0011Q\x000fTM­¬îÔuÃ®H]}l#\x0007o5{\x001e¸\x0011\x0001ëN àH )\x0003pUÅÁ\x0013¥ÅÊeä:b z{oV|oj"U×\x001b½ïµ£j\x0019ùð>o·ïÙð{ªé\x0011ðXÌ\x0000g\x0019w¯-,ZiÝ{m\x000c¼´¬(\x0003oNLL\x0014·Ð\x0002\x0006ºï´MîÃç\x0014Î·Ò?}Ë\x001etÌ\x001e(\x0018¸ÍëSN{½xRF»\ßEw&8îh\x0017aitÔVÌÓ©G\x0017*Î<üv}>~xÐe;Þ@,\x0011=·
û\x0016¦Cà^ÈèÈ7jÐ\x0014£èk\x0003Î9Æ6]-ÜN8z¡W\x001c{|wû±§uì/æ0ý\x0007/\x0011Åøá®Z\x001eü\x0008z^K6/»\x001eúÄîè\x0019<¾$dÏ°·a\x0008\x000b\x000fëåWyY1ã\x0007\x0018¹{[ù\x000eW%î\x001d|9'Ë\x001c\x0014½\x000c\x0014½\x0006«\x0016ç\x001d²ôeÂTÊÓñ|¾xô\x001aäT\x0019Wz®ã±×>\x0016ÍNßÐÑ²Ú\x0017\Í-\x0006ª!ðrlæíuyz\x001f\·Ëø®­rÓ!·NË></yæâÜåê\x000f\x000fºÏï¶¸1ë}a¸¤ÂCOÃXÀ\x001fÔ\x001c'zDô\x0010§V\x0017=\x0010­X-\x0004»\x0011\x0002ø«¼¡£«|ÔZ³rêÉ¶6'þ¦qpÉüí9äñ9\x0014}An \x001ayb\x001ftÌ!ñ¥\x0011Av2Ù\x0004GS\uøBâ®ËK\x0005­_åJyÊ½r4Ñ\x000b\x0015¼=Ð\x0016ï(%\x0017\x0017:³\x0004ð3My\x0002Æ\x000fPÎxfU7ÇG\x000eÐK³/zð¾à\x001aCÜ«\x0003x£¾!y¡r^Ú_|Þ¹E\x0013\x001d¹E\x0012(c\x0018e5FFçÓ±â?¸h¼ÐabÅ\x0001k=7~÷ÇÒ"\x0011ÍÌíæB%ïò	gÝsõµtÞH¥Z÷jÞ[Ð_àX8v\x0015-Åq× sá¸Ø\x0019Pn\x000b¦àÑwÁH=2]¬²è¸¯ÉÒýåÄ\x001d?<èÁ!O§d\x0010¢{ætÕ\x0019gÛT"ëcÂ´E)½ÎÕÇ\x001e&úeµL\x0003ÙJ\x0011u	­¢\x0004}I É7µfêËóËãó+&	¹`è-òboy¥«z#ÒíÄ	Ä¤o»\x0008\x0013ÃoØ8-ò:yË%;~\x0000ªAÂªz\x000bË¼\x00088÷cÔ)­µw\x001eLôóâ\x001cfÔ»\x001a\x0005bcîÈ`Ú\x000eC´ÛbGëjmÁ
øFÊ¸¬Îçj=)øAàÂÀQàBUí;\x001d<I\x0006Èz©Ka¼ÖõYpAÏ8ëÉÓ£·;&J¨Lðò\x0002ë3\x00128\x0014îßÁÀR¸OZmBæO\x001b[\x0002Ts }ýGä7þGR µúê¸A4JHÍ«³¼lénÿ1¸Í2d÷n*\x0005\x0001oH®¯\x0005j\x0019¶ë¿!¿ñ¿!ÝÈÀ¾'+mº<YFéá·/¿Üÿß\x0006\x0011üõO\x0004¡Æ¥T\x001c÷lÉÔ\x001dôAj9\x001b\x0014ü¯_~úí_ÿû×\x000f3)(\x001f¼-ºx¡º\x0011q³¼îH	\x0007Ýw\x0016é«\x0007ßí$	üÓ(Vÿ÷_ãúÈb¿/ü§k©r>Q}\x0005GÂü\x0002NeòdÄ2Ü\x0012\x001f*öw6\x0011-Ð\x0015§BAhÖ	\x0014AÏ¾ò³¿Ì ùí\x0013}ù\x001eÆ>~_r9V\x000fÎåq;\x0005Ö÷ª\x00076çÅóÍ§àq{JLð\x0008ö%zX@Á6§w±zp6\x001ey\x0018ÑÛAÔ~¨}Wk\x001b Ýhb\x0014\x0018óª1í´v2iøÛ´\x0014\x0016MîÃ÷¥B>\x0002r&¥åÊ1\x001aô
¼5iFZ{
|çÔ§	CÞhí{\x000e÷\x0005\x000eÓ¢\x000e×V	M´i5-	¨2º\x0014Â^\x0002à\x001dM>CªPª\x001c'j^Ú²¼RöC³\x001d\x0005_ÿîóÿø³\x001fåN&A\x0007³á\x001e\x0010é G\x001f}\x001dÿó{\x0012ÐÂè{ùëJ2Z4$\x0010Ä\x001a¹Ö9A%Á\x001c'\x0004uáwê®{TWó\x0007\x001fÕªûáQ`uuÜ\x0006ô^<ÐX<R_Q\x0008ì²ìh,fÄµ\x001b¶4\x000b§÷à\x0004§ Äu\x0010ªç\x0018¨& õ<Z­%WoØ\x001b(
<`\x0003¥å UW·°.OêÁ¡Ù7a£´J×X\x001aÎµ@]¼Z`ÐMlñ²RBÂVÆ3ìíþ¤Þæ¼?÷Lp,	t­,BÄâ;/ÿ\x0007Ü:RãE±é
9\x000cÇ9\x000cí ÇÊÔÝ8r;qW?7ìêçê]\x0004õh-ÅR.PÕáxà£Ø}h\x001eàÔ<2\x0015æ_àí¥Dãâ/óØ@\x0007\x0003	Þ1Ï¨$-O6Ð>=:\x0002«»Øô\x001a6ØôjÓXÆ¥\x0012½ã6X¸L/Qû\x0000ßº\x0013\x001cºó÷·ï
\x001e\x0013\x001c\x001b<äæBðYbn\x0003­Y#ïmZ\x001aN2D\x001fì©Í\x000cØ\x001cèÉ¡2\x001a\x0019ö¤agLê8µB\x0002g¤­ùªsÈàÙFËîÌ\x0001;»ZÆ\x001aºÝPu'²­¨&¨Ì§÷rf¡Tþ8W
ô1El¾J\x000fXõH\æ;c:GÛaÔ\x0015\x0005;ó|gkmÞS/l\(!bñÕ×ò¾åÂ*>\x001böí[bZA\x001f\x001b\x0010)é®å¡<:%ÿr´è5p°èÕNT*¦\x000f¯J|é§¥AFc2«\x0013«\x0004ê\x001cAÎySW\x0012ê\x0016­lþ­V£säð¼àØÒ©T¼g¡8ÍÀÒÈ\x0017²·ÎÈ\x0003Óå\x0005\x000es®=K #áõ¦Ûm)`\x000e®|¹X%R·h¢¥"ë\x0010å\x0008cö¼\x000eÃHY½î:±\x000baW4rm½t.\x0012\x0015Á¤\x001eêmÿTÜ?A®\x00088ÆåG4\x0013\x001esÜyå÷wÛ

¼9X¡T¼ä\x0018þDÙyÖõò³\x0000ØnË°á2TZ\x001e\x000e\NÚBùs¦\x0012«nÒ\x0010j»­\x0016(}Þ±#ZNJþ\x001aiòÈÇ\x0006jg¯G¨ É­jC.³áIT\x0011\x001eùhÐm;'jc\x000f`è\x0001Ñjº¹Ãk\ãÃÁF¹<ãÈ½Ç«f-¹\x000eUêòAÌiß¥¡
¼\x0017,tòæs$µ$`ã@HÊ\x0016ì\x001f2ïx3];ô!æWnz¬\x0004æGÜ!^¯ÿü¶ü\x001bj^\x0005\x0015®p\x0004\x0010êRzY«2¹ï\x0000cI\x0017ûJ 9\x001b,I°¼¿´[?ÙýÝ\x001f~To7uyûõÛògrr¹\x000c¯\x000eû{´¸§¾¾i¾¯½Jq^Ïõµ½ï@ÃF\x0004Ù¬"ñ$\x0012\x0002×|)iIQ\x000eñ©]&ubLª×\x0012Ö:KÃ7óÒÃdaß/ìØ\x0001IruÑ)ßIÝ·lÊË·qW\x001cwëDÀq¬»!«Ë\x0007á¾nO¿\x0017vâ9\x000e\\x0015ý!7\x000e-(s\x0016q\{\x0017ÏÄî4ß\x001d	Ã«\x0019	{ÑW\x0012Æ»Á²{\x0018<@3q\x000b®\x000eëyÎøT{\x0017Â\x0004\x000f\x000b8$nK
Ôâ°×>ËV[zã\x0005ñs\x0016\x001a¹FÎF<\x0002\x001e¬â¶=·'84Êê\x001a&:B_\x001c
;Ok\x001aqX\x0018îÜò	Þ\x000boNàÇæZÙ§d\x0012«É4íöÌcfF¯\x000bJ9uZ\x0016Y\x001a©¤^\x0015Rã+­!#)³yü¼\x00149Ýh\x000b{Åýy{BËW¸wú;cOË\x0007úÚÓðD¯½¾ÇÖçR1ò½®<Á¡®ìÜ2¤Ê\x001bGô~©Í<\x0004\x000fÂmï\x0007Üûz\x0000Â5ÉãJu+yjñ]À#tðùû[zÌJÃÈØçPxà\x0016ÒÇÛ¹\x0012ñ\\x0019FJ\x0010å$n
g\D\x0005¿-ÃHËp¶ì½\x0006.\x0011a¤¥RxäãI\x001cwU©\x0017tÁ	7Q#¦KB\x001d{\x001c·ÑÅ\x0013÷>Ò	ú¡55Ô#Ñþ\x0015\x000cô\x0014Y
5,¾Ýn
o7õ\x0015\x0000²ÍÈVpVQÞ@{^ÆÀ;äe¼¶\x000b@5H¬ÐU)-ä\x0006ùf]\x000eáäû@d[%5Áñë4´á`GK8ÕìßÇâúO"¼oF§õà·Á\x0001ëúúåÃBÖÜ¸%­\x0005=j^E^á~-Æ#úýÉ0ïORÆQ!\x001cû!ÿ¤¹ÿ.Ü¥ÛÅdn¸t'jåÒ®ÙÄ·\x0016!Ç\x0011®Âl¿Ù`G0\ØÅP\x000e*Æ\x000eÃ÷n§qMìÃN
+\x0015µ:>AKfµµn­\{xb7\x001c·»×*tª$"?ÇET7Yfá\x0006_s9*\x001e[iJV
Ö\x0011õC`ö&\x0018!\x0004Êo©$(:8ß­ u\x000cUý\x0016ªj±\x0006Ê)R²_~g	Ú×¶'\x0014_àøªq\x0001\x001bçÔ\x0011\x0003\x000f\x001eÖ°PNé]\x001fÂ½\x0001
Üy¯4\|Ô(I.ñ¥ÐZ6Þìå[z4éT*kÀ×ØòbÊ\x000få/6\x0013»ÐÀ#µ\x0014øHí\x00102ð¥a¡dÓÒ¾¬oë;kS\x001e\x001cJª!ðE	¸%cýß¡Çe¨àHkmLýÒ!þ£y§ïÕ²\x00178XæÚñDH×a.Ë"·þ°Ó}
<\x0000ÝW¾mB
·Î9úøìø(l3\x000c¾í ö.­\x0011sN%1)_¢Í%-àF-.ÜVb (\x0007-h"ó>hZ4XÍý`0ú\x0002Ç'zÕ\x0014Ïmb\x0012ýðË£\x000e¸P·\x000cñÄ®\x0015\x0007¤£|.LmË¿Í÷{µ ;Üy e\x001e)ý,Ç6Ç|y	Vkm×§_\x001eJÁ¾\x0019ÙëhÇ\x0005;\x000cÒA\x0007Ñ°Q\x0007Q\x000eÄÕOýº¼?\x001bw¶ÔhJÝ§gß5r¸¹åHÌ<ãqVÊ/K59\x0017,è\x000bnNy3ñ¬6´\x0010÷Òê\x000b\x001c÷~êøöÈr7\x0002_CxgJÝ»<Á\x0004\x000f¸Vä¶®\x00169\x0001M*\x000f¶Ä¹\x0018ó\x000e<>Èüú Ë|A\x0012£V|Y§ÅÊZòÙÑûü¤\x001c½ÿ{>ë\x0016½÷¡À±©0ÿÝ¿~\x000c
¶ëWq\x0004UsÓôê\x0000×ëL¶ÿ;\x0006ì©û|Ò\x0014Û®\x00139Ç<Ð`«oÒçpGLxü8%.V£/x\x001dØì Ú_u´´jÅÄ\x001fì´\x0018}i£Ôás×Ëcí×_¿þóGq½vJ­EÄ×º\x001dÎÌO·­J÷ú¾Ìgõâ>YåÔ-øé\x001bQpÂ=ÿ5ßÓW9x\x001fË&üùëo¿?þøõ£Dþ¸Øèä.PwÃeeþ9ò÷\x0008÷{òÒ]>I¢ï·ÌâØH@k\x001d+Z`bm;¢ð£Ém§+Md¤+ùT \ÜzýÒ\x0014Ó[Ôdß/&ö\x0001Å\x001aµç\x0013dþÙ1tÉ\x001552àû>ÿß~þá×/¿ý søA\x001bÝó-©æÁÏÞÈ\x0015§_¢­ïí¨}Ùê\x0007\x001e¦ÌàÂÃ¼ý9ßÃ§IG*õÿßÿóÿþ§_þåßþõcv¹ë	\x000brï¾µ<eðxéJÌ¦¥ï%K¥xÔÛGI£\x0018nÇ©>/[µxUÝ\x001cø&zqÂ,¨ïä¸r·Ó\x0006©&R}»¢(tIT­7\x0013õ&«ÖÝ¨ën¡íÄ\x0006.¥KjÇ\x000eÃV\x0005ô!W5Âvvì,P\x0003÷À\x0002uCb\x0016Á\x0003½±\x001a ¸¼æG'èÞ&?Á#\u\x001a\x001e/`W\x0002]xDL5_ú\x0013¸#°v\x001e#`§\x0014vt!÷ì\x0014®d½ñìÜIO\x0006\x001eôäÔø\x0001i£çù\x0019!põ;\x001cº\x001bx\x000e\x000blé\x0015b³2B÷VLa1JmÅÊû\x001d6Á\x0013¼ç·;Æ´¦¥Yá&Äáp?°/S\x0007.ÖG³%\x000eæÏø\x0002\x0010½\x0010t¶Êèm\x0007^à\x0015æDIG*Ó	äÍ|:¿h
\x001c_´N½)S~Æ­ÎH\x0001Ç\x001d\x0012OÊËØj¿Ú
\x001cMåõÂõ0)Ú\x0000Õ\x0008×øKp\x000eà\x0019×¡vOT\x00189û\x0015i±\±÷~¶
â\x001b.¨Åã¦)\x0017\x0014eÎnuWq·é~ãR97¥q³l/}\x0010Ë÷Ba'(t8í
\x000bÏçl]ïr$p7\x0012N\x0007+$\x0003G+$­{£]¯
P~GÃyº'[­góÄ\x0006¦Ó\x0006\x000fBe@§ê~l\x001bmJ>D
\x0011¦\x001bÊÃ]ÐÏIüÑù~÷Ãfø \gà¨\çTµ\x001eB¥N£ÞÚ\x000cÞz3¢óeÆQæ@"ðüÎ	)x&ó6\x0001ÏìÖÛª3¢óþÞ2p`¹8
é\x001f\x0005_õW\x0012'G1«²¶RMJí6+>T_à¡\x001cýrÊM
xm¼ÈËpÝn]¡è¦É~S\ÓÎ&ñl\x0015z\x001a³î~>\x0013¼Á\x0005¤Æ¹ =ÜRB§\x0006§­ý\x000cnûº\x0017°^àxØÊÓù\x0002¢³Q£MêÀu÷¢aã×ÔvwñX0ï©\x0017\x0012k¾NÐÚ·"ý\x0004ï\x001eÀå?\x0001+íQD\x001dÇ9cÒê,ê]ÖxÐ±©
v
\x0013Wþ\x0013.ñ¥J­Ás¾]­\x0000v\x000bñýÎ'VÇe(ï°lÎ<h\x00117ðà*k\x0004\x0003Ôïå\x001a»Ü\x000fa¼]äh?"GçgÅ7\x001f$ZéÜ-
¹?ÄªUÐº¼eÏ§aÊT¡UÂ¯bß\x0016xoÐñ,ß
\x0017øÀÆ3o\x0015ÚBñÝ,h\x001fØÐ?Ìã\x0013ì|¦pÕ@w¦ï,Ë	^\x0013{Ü>h4«ØlJ,«Ð4Î.'­\x0007>a\x00182xGHpHG­{¼R\4¥°Ëãjüð Ëy\x001eWòWEjÖçwçÝÙ¦>Ûå\\x0019?<èÅãrQÍ½3\x0013X$'=T\x000ebì\x000ebìÚëé>U\x0000§èSÀ\x0017ßu¹\x000c|ïrà\x0001Àµ\x0010Þï+§ztlùÄ\x001fµù<EÎ.+\x0006^\x0013pÏ¸\x001cåÈC®²î9yÚçØ/'îøá\x0018>ÁQy}JgÆ65i(\x00196Èääo\x0014á8\x0015IüÍ©-\x000c/Ç`N~q÷÷è
ã çÁõ,GBÆyqlÙÑg}üàÜjààÜªÿÇ\x000e_\x0014ú\L¸Ö\x001d¿T\x000fÀ\x000c\x000e\x000fINC÷'\x0006\x0016LS;2\x001az*\\x00190pÒÎ¡ÅøáAÏáM\x001fqàHQVü`1¯ÀÕ\x000b\x001df&Ë\x001f\x001a\x001eUw5ÝîøÊèÉÜ\x0019/oþñÃ3ôÔÞÔ1ô\x000e9Z¹¸ãª¢ÙÀ/³Q#ÉÎÁgyÌtôj"ÀMzÞ%C'xiÑ6*H(ô@\x000cw×\x001a;Ì©\x0001`0ôËNÊ\x0005vRLé]Þ\x001foPÏj\x0013¹ùQ»\x0007úíNÊx'Å\x001c1úï±#\x001bDÐÙðAö¸
}§Lð\x0013\x001eGÞ\x0001î°×I¾¼Í)cæ~\x000e\x0013\x0013Ç\x0005#ÿ9O{q9\x001cMmk\x0017Ä2ðâàlËø]\x0012ÖÕØ\x0012]§ò¿)\x0012ÐÇ¥IËÝNÇ§£6à\x0005Ðµ\x0012IC_WÌ[¸î\x001c×\x001f±«Q`õH2v\x0016%Öi\x001fû´ì,àqfTÖ\x0013\x0018=èq£6®Óè>Ï#æP-2X-×sÌsú5uÃ\x0006 K\x0019é¦¿þ#ò\x001bÿ#Q9\\x0011æ(ûrä°ëdtÙVlÏû?RêòH(Ü!èS{).êñ×üÔ\¥×C~ã#äè6n¬í\x001e*HÓ\x001bkìbÿoÿ>qøßhê\x0006é*m2Æp!/\x000eE=Çt/çößþéç_>ÿËç\x000f*t©8'ÇÒ]Û\x0010^T\x000c½ÝWê8¾«t;°\x0018\x000eùÏR\x0007=\x0018Éj\\x0004ëË×A<xHùa9\x0005ó`P\x001e¶ºa#á_eoÅ Ïß\x0008{	\x0011ãxïïÍû/l`\x000b\x0015	|à\x0014Ñw\x0017!/Ay²æà=84äFi?N¤74©V	v"Í`òý»[òî8ÙòþL¶F@D­l!-oý)$½\x0007@\x0003Ü{l}ò
Srr,lì¾ä'ój÷­'âÂF\ó²
È\x001dT>uY²\x0014öl>¤²
¼âÈS\x001e¢(ïël!gÕõl0$HLp¤µB)\x0010sî×L%\x0013üná9Á\x001bò\x001bsÁ\x0008E¾×B®÷ËK"\x000crs8<É\x0007xÀ\x0016?¥5Ü
Ï¹\'KºÌø{¿Ù\x0004Ç~³,Ag
\x0000ÞH\x001eIÙæ\>HÝ÷¨pGtòPßÍ£¨ï"OKuÖ·usëñªoU1<)Ë×¾Ü$Éx\x001d\x001a«®=Üé²Z\x0012\x001d³Ùò¼\x001aà»BÒ\x0004/8-ù! kVÞeZ\x0012åÿbÐ'\x000fÁ²\x0013/»w|\x0018j\x000f<wU~ëw;[Òáq5À£³Å½y¼\x0003<¶/ì:¨ø
~¨«\x0018x&º:E];T<-K}Ïg\x0003¿¬q/ëoÞôÐ\x0000ÇW9j,½ûöi\x0015ÍÔûE±\x000fyJÃnÏ­÷É"\x000bÁÑvÑò\x0003Â¯Ë.§eØ\x0005ä´ìØzï>&_ÒýKÏ|®zÛB\x0015·jH6\x0000Wÿ\x001b>\x0013ù%î\x0007·íL[ÃnÈ´M­¾Ó=|ÂIÉ\ØF\x000fám©4\**èí)7\x0001ÕÇÕªf%´jAÅeï·²tÂRIn9o3Ûk«©¦Ù­^ö~ÂW=´'dñjBNWöL¦P\x0012ÃHó_¢¸\x0006\x0015íUEòZ\x0002¢Ó»O¥pm¿\x000eß¾{\x000e\x0019x\x0007Ï!Tåå\x0019x\x0008dØ%ßjÁCïI±\x000ffÃÆ:µKòå^ÅM¨S%\x0016jO±Bs?¤V'8~Oµ¸}¦\?¯§NH\x0012\x00131e3\x0005º|Îw³Jh=,DOºôò{]>çpÕÿô|\x001f`ZÂ§gà!±\x0001y\x0001Ï½ë¦Nl°\x0005Ò\x001c.\x001cZª\K]MLvéò÷\x001e¯ð©bO£\RlÈ/ÿí¨öï5ÃÿÂ\x0010î5ÉÝ¾q¹¤Õmr{¨jAòÈûûü¿ÿáË/¿|ùÃüåç\x001f~û ¯-Å½êE)HóÏÑä\x0007j'jà¿/É×LïÆË\7µÎ¢>¡ÀûÄk&
[P¢'%.9\x001f¸£¨´q/noá\x00176¾Ê\x0006"µ\x001aÕúuö²i0¼°Qa\x0014HAÊ ³îo¬5'1ÏðËºM	¶*i	\x0013tìRaýÊéë\x000eØr\x001eVl9¬Ø¯²\>Ù?Är	\x001bi8yÙß\x0011ì;½c³æ{æU²W\x000eÈºP÷µT©
t\x001aÃk¼èÍÆîELD*~\ÉãÊ\x000b\x001b\x001cWer\x0002ìL×½Z\x0000P4.o¹qo\x0005¦	8ú¸F\x000fô¤	G2êì¯gÆqK#¼À! eæ·/·uV{²F÷õ9Áõ©,´·\x001e«.sR(%S\x0004ß(_à¾gÂRª*0nD\x000f<òÐ­Mò\x0006^\x0011¼GLWÇ²¸éEî\x000e±
°%@Þàä£åß2D\x0003<³
`lÞ3ø\x0008öãíFø Ê\x0012ENz\x0001vnâZg´üGÜÌ\x0000ÞØ`B£\x0012ké¹êõZ&ïD\x0015??_àð\j\x0007\x0000M¨¨Qv>ÍJ0uÛ-ï9±\x0013ä=5s3\x0004¡_Ø\x0001\x0017J^6~0)Ý>ë;¿Ç¤DYfòÔJÔãÂ@ðC0{\x0017ü}c£4§Ú­>2ø2èqÏt7Î{ªöñ¥<ÁY#VÞ;â­E2±:ÆnÝzåÖwÛ\x000b»¢~sl¸ïü\x001däX\ä\x0019OÎTE/[³D\x0014 ÕöYÊl&\x0019ÊX¨"\x001eÔ¥~</'V
$\x0012Þ}E4ÈÂL1;&­Éq7Øv·UXy\x0015æ·1üX+\x0015hs"ééàí5{Ãn\x001d|ÆÞG7-ÑßØeá\x001bÉÃVoØÆ\x001dp÷¸Î4õ#ó2UcùøR~7Úö\x000e¯e§uYZ+³Á~V\x001fwóOCgóO-¶\x0004%±\x0017Z(Ë¡b\x001a´~oôèØè\x0011F\x0016öçÒ)\x00162¯w\x0017Ú\x0005;\x0010¶£\x0014|PQ6
)\x0012Pu84
Õ
Ý\x0003º¼Gð~+Z\x001cGóß^8\x001f,\x0011j2\x000eÕyÿ\x001f \x001cXÈ\x000fj\x0016OâðÌ*Ó-v÷Óx£¥¸¶x\x0002}"æÆÞy¥\x0017äö´bøÞP?Ñ±¡þ\x0016ò~+\\x001eà\x001b	ù\x0005\x000e$ä \x001c>è\x0010[\x001b¢siè/cMnùÎÅ*ß\x0005è!³¡«w<ö8«ßñ²OÇ\x000f\x000f:\x0017á4®è4t.}HL,\x0008½ÌzÜM\x0018j+Ïzà<\x001d3¨b,¤Ë¸3ºNh\x001f.Ñ\x0018\x0016\x000fíÎ¶|A¯\x000fC¿|Ñ6\x0008\x000eô,MpE\x0006oüAÃ´Ï<»ã\x0007<5 ó)	$\x00128{C\x0008ø\x001cùåÂ\x0018?<àrGC\x0001!Vp\x0003lOÓÞò6ç\x0019ç\\x00166\x0006¸«Á}§\x000ehÌí`Ì\x001bÉù\x0005Þñè2ª×ûMáHâzX?\x0011¸ÉôÛ:,¸\x000eÕ\x0004=Â"r\x000fÄÊü½y8n^\x001f/tôú(îQUÈãiqyyk\x0019µ´\®ñ\x0003 G<\²D2áWb\x0006[kÆ\x000b¼á¤«\x001c¼\x0012\x001dU\x0010\x0003\x0019?A|kx\x0007\x0006\x0007ò§
VÀèôIM1ªlùÏ76,ê±aV:UmFå§ÅÍõ¶ý+mÿHÌÒ\x001c\x001a\x0019gêb\&}¸u³x:GlùR\x0005EO+»²r\x0019º1òJº|ÐÆ\x0001@Æ[Ty\x0010F^8\x0019Ì\x001e²mÝ\x0002op\x0016e(eÌoP\x00199\x001fe¹m«Â¿Ð\x0003.Sç"ij_\x001dÝÜaü^Ðz¡£¿R©\x000e·QIu*wÈ
0\x000e¯vIZ\x001få(\x0017¤[ö°ÓUÇÜÏ ÿñØHí¶K\x001bîÒ\x000cfB\x0000Î\x0001©ÕÓr¬ÁVÌíÜm|îF\x000cHâßiÅD¿|T\x000b/Úåõ?~xÐ}ÀÞ¯¢=Ó|ÂpTWf|ÑoÁtÇ`ºx[i¬v\x0002ç<TÖ¼ývÛu¼íPòNÁÕ»Ñ¬sÜUÑËûmÚ;N{ÖÎ]8b:Û¢V¸·¬\x0018¡WÞ\x0012gôñÃ.AEÕ®köÆ
lzA&C?'0Æ\x000f\x000fº<Z K+HÉEYÝ\x001cØe³è\x000eîrÊ\x001f\x001et-ø%8\x001fù9\x001dZ¤ºþß\x001bz:_Öã\x0007@'ª\NúN!
ãÞ8ô\x0002\x0007yv½eðÌ*óBàì"É=åÆ{¡7\x0018e÷p¾V\x000c<\x001c¼IömÍ7\x0013Ü{ü¦9àéä!Ig{óKÚÕxgaW7x¡GB÷È°JÓ\x0002\x0018ÐyÅ¤j«ÝovÎ/t°sÿëNÇ£\x00169%Ôe§Yßg/p`	xÁá\x0014\x000b¥\x001a&\x0017xè&\x0018¼ùNð`Á$WÞöß\x0003|9|%(æY¯6ô°9(¼ÐÁAAÂØa¯\x0012Â1y¤A\x0014e\x0003b"\x0007*Àøá®*\x0007ðQ9r\ëC¤\x0014GA½@üä\x0003Ø_¤ÉQà!Y"\x000fLO_\x000e åÛvºþ\x0013ZÇX,Län­\x0018èIãÿ\x000eWwa oú±Ç*ôøéÊÏx\x0008Q¯ª\x000cYü~\x0011«À5\x0014ÏêsmGU }K÷<ªÏ&+rpKr;±§PÐU7\x000e !c ØZ\x0000uî¦\x0007\x001d
´æØÄ,\x000fºawÂNïhG±seksÇ½QmC|<ÀÑ"hõÙÁD\x0016>r\x000fÓ¤\x0014SÉÝÁ/l \x0006\x0007e£ÏÙ°=ÃÌc
&÷z7lñoðà\x0019äè2²xà|qI\x0018u|³ââ;Ò\x0019à)³¡\x0000ÁÇs*l(\x0013< J¨jÏQ-U3	jÞ÷£\x001bî\x0002a\x0013»Ø½W\QûèðÖó÷ô£\x001b-l&/p0!¼\x001c\x0006ß<H.uNÃ:gPw\x000eò¨7"
r.×Ñè\x0016\x000eùH\x0003oô
t ×<Vâ\x0012åð¤\x001f¶>´\x0017tÇLJi ìÙ´>KÙ\x000ey2¶	¶n\x0014¸\x001d#®\x0014÷\x0014$\x0014»ñ\x0015\x001a§\x0015H7P<PZ\x000c¼â»;¡1yS+tþÓøÈ\x001a&[7èT\x000bG¬¢ªl\x001fü	\x000bÇ[æ;\x001f¯¿K·Ðú8Y<'Q"7Ä\x0005_ÝBÊ\x0011
OÕÆ«Óÿ¾§7ÅÃS¢[7ÅÓï)Ç·Ö\x000bÑ+c\x0013§b®Ö]z\x0012µjñ·åÎÊtgÒÐ:ûp)=Î\x0007x~Jç\x0002®V@\x001d®T%Rð°)wè¾¤¼;ù_XDõõ×?üÏ¿Êø
­To\x001dnÚpé°?©÷
ZE[«à÷$LÉó_göÉ<2³OvyXòQ\x0017_ÜU£q¥½z£ïÜ°¡XÖ-ò&f
°\x001f4±S`Góã¹`G\x001c·JA½Zö;ÐtÜ¬\x000e£9\x0013­WoñÄn±ª
A¾D ccÚ7ÒÑþÈ3lxäÉ\x0015T\x00022)Uéôcää`pÃl.ìçÄ\x0004g­\x0012²\x001dílð¬½²\x001bô&Ç\x0013÷4G\x0007
Ê¥g\x0014òW!»Ó\x0012\x0016
\x0004o¸s2&x\x0000\x001d\x0001ù\x0001ýæúlûTbSìÊÜº\x0016_à\x0019ä>YVi¡\x0014*ÈàF;Ú\x000bx\x0006<êqÈñïv¬DsÎ^¯Aµº\x0014|/²Oð\x0000-ç\x0006\x0007s\x0015!í¦à¸GÏÙ*O\x001bÆ\x000b¼à'òP¢[ß/å^Ùcå|ð\x001b8\x001eü\x0012\x000c't\x001c­jDR",°äec\x000cõ³­Óm\x0017\x0014Èañ\x0008ÉpàZÕ&l#{ý±9±\x0003\x000e\æ8>\x001bT«Ö@\x000eP\x0012b|ÈÞ\x001ff2»[ò\x000b<¢Âx¤ÅR:#\x0013aXÎ\x0019Ý?ò.À	dÑ³\x0010r
pÃ7¶Þ³_cO\x0012X6\x001d¡\x00178ê\x0008%¶T¬¬\x001d(×eb\x001aµêä+øþ à5â\x0012\x000f øÛ \x0004­ÂÎÔrùçÍÙóö1\x001b|L-b¢\x0013rUqàý^ä\x000cKÇ«
\x001dW×8àAÄà­_NZè
Jo\x000f¾quzRøÐ;o·ÁÜÛì^Ø¨d\x0002Ù0çHç«µÕ`gLxÝU\x0013\x001bå=È8p)ð%oÏ\x0015hûý\x0005nàÝÃRQ\x0001¸µi\x0006TOXùA¯ÑÈÙý%VÑ\x001f`\x0003Uô\x000eT«jÔkQ9YÄ¶bfßZ^Ð(]\x001b}\x001fâ/¯E\x00183+V,¾Èz|\x001d\x001b¢ÞØ¨\x0004Ó=/Bz!\x000fÅ\x0013þ>[Ãe÷Øp¾û»5ïå]G\x00129\x001c\x0008É[+×N|à¨À\x0017z\x0013%ÕÊ¹uþjçà¹\x000fvZßÙ\x0013¼¢ÜInèvZ¦CE¥ZØx¤X÷ÜíÄêxb.\x0012ðÝ-\x0011«F²V*[ÞwoIÃË0Á\x001bIûtô\x0004cÁs<òQaèúó\x000b»ÃÇD\x000eÝÊM¡^­\x001eó5\x001bgïPf\x001cèÞa|\x0018BBûg_6ñF/Ô#¦M¥£tì.íøá\x0019z\x0018N$®ÔÉÐ\x000bßoê#e\x000cÒó\x0005çÁöN\x001e3\x0006ÊO-4r
|²\x000eqAº{WpèeìÉ×ÉÒÈag\x000cf½Ô2å'nè\x0001Ñç)øB8«Ò7TVOË1í~ç\x001bMôp9½5þt¦J¯Cµâ ³+''Üz­_à¨	\x0019óS Î¤ø\x0014õÁóÒ,Í\x001cn³\x001e\x001c}ÒíYÑ\x0005ô4o\x001ay\x001fIO½<l}Àí8»"]ÄÁ\x0018g\x0017
=5iØ\x001b0&xBðZp1êÚì¸^
\x0012Ë§rá¾\x001azD%;Ð\x000eV½¿ÚÍ¶ª©N\x0002éÎðè¨\x001d&\x001b\x0005O\x0018¯ÒsÐ9}lJv·\x0013&á	£è`-Ç\x000f\x001e+:M{
ÃËVÿ\x000b:^Ó:3àõäÔÀÙJ.yðAÊnR÷ÁhZ¦Ï¯ÜÙ¬*¦zã\x0004\x0019zkëÄ<	gUË¤yá#@ãÞ\x000b­Æ°;\x001dë±`¾¹-VÈzJ\x0019èf<¸×ß&x$ð\x0008A@ÓdT§\x001aTdO¯­¡û
\x001b)¶'\T\x000fJÊ>	6\x001b\x000f\x0006g%²\x0017l\x0006øøár½ÞÞà\x001a\x00034Z-\x000fFÓ·XôP~£\x0008YuPZP`y`´å+¡@=äNO\x001d¦;ýùë\x000f¿|þï\x001fåy\x0014'~ü\x0017þíH\x0015´\x0005\x0004ÞÉ§Qïú\x0019ù6.Þ5kz/­\x0017\x0014ºe\x000bX\x001a*è\x001bô\x0001À·1N7\x0015Ã	î\x001dWtÍ\x001bµ],\x001fy>år7râÎ§ØÈ§r
½§$\x0018ñÔµ\x0015<÷¼/Íø\x0005\x000eÎÄÁ¥\x000eQ½Ý±Ð¨2¹\x0004^\x0006)É\x001fb4\x0003/8òöÁêØÑyà|\x000eå<\x0002ãCÝxbcÝX\x000eq#8~N\x0015 ZÀÿrRÂzcCÔõY¶Ø\x0017\x001aç7T6ì°÷=øÉYÁqk\x0007âyGº,ÚÈ17Ï<<±<ìå\x0012Ô£»\x0010¥'e\x0019Þt°^à µ\x0011äæÅp^ÁÑ¹D\x0012|Ùæñ<\x000bôê\x000b»@eWûù\x001e·¸®\$"÷ªR
c\x001bêðöm½PÚ{Vú \x0001,°ÏÑ<nnKjé²&)fmìÛ\x001aÁà#6\x000b;\x001de#\x001dEîÆ7çyÖaä~M\x001dy»¤ï­¯\x0017Z*µÿ\x0012½
MÃrÍsT­#9m&¿\x0013<É¯Dòí¹jåãøTI¥®\x000fK]åióø}aÇ¯\x001cHïö\x001bÅ\x000e¬÷¤ðüò«#èËî\x001db·BÇ¡ó¤÷\x0014r¬\x001c®Ú3áÐÚë·ÖÞ´\x000bé´Ã´ü\x0005Æ\x001dµ)ÄSp0rÈ»üÄÏ_ûüó×?ÿ×\x000f\x000c2ï
íl0MÏ½¾¿K{Ò\x0010÷Ë;µq²Áå­æCÐ[(¯yCÐ¿3·r!Øëm?!\x0014Ý£[o\x0018SØtí\x0010³*ÂiÃÐé«\x001f½0çWÿíÏòÿôA_>efÛÆðhä¨ÿ\x001aè)+a$\x0000¾gLh¿êL«Sø'r¦Õ\x000b3Ù¨¤;º\x001aãâ«Ñü¡6À=J\x0010äÞ	ÍÑVÎV_!ynÌÐ¢´õò\À\x001b¬Y}BÜãÈ\x0017Æ´ìCªd`£¦
-vBuÔ<"óÔCJF\x000f»L
ZË6´Ò*agÏkÏ
Ý«xÈ\x0006\x000cì\x0018ñF;¯Ío.ì\x0001~ØÆ\x0006\x000eÛ8L·À\x0017Ï¸t\x0012¯É\x0004ø`ri
;\x0015\x001c8¹Ohn \x0017åhb`qïØØ\x0005\x0013\x0012ú\x0012:\x0015¹G\x0011PýTHO6'ªa7ðôN¿\x000c~z'Ö©üÓ,\x0019)\x00115\x001f_F&\x0008ª\x0016FÇ²&ðxÿtî\x000e°mwòþ';µíÿúYÎ¿\x0003ë·\x000fb·i÷\x001c
¨öòbwkI=7ªÊÜ¿ï¹©¤Ã¹¹}6hÒ¨Ù_ºÃ~
mßpDqX\ïJ\x001a
mûÐè\x0019Y¨[#j\x0002÷Y6RÉ\x001eNhÈçúÔô¢	Ä£Iz\x0005°@¼µßì\x001bØ 1£_S\x001e"¯	QS3\x001côÚñÔ¢éï\ ÑQ«Æ²ö±wr¥èJÏæ	±tv\x00196§ËÙ-ÛÑÌï\x001ehï¸íÆ\x000bjoéÐÕáxêºwn4%\x001cõHÐcí%õç1W§®\x001bM3Ðú+KËcòÓiè\x0006\x001exqCÏÊà­\x0003SåÒ¬KþpE\x00198&¬z
<\x0003<}kç4k\x001eÞY¡\x0013<#L\x0015x 1YW!wæL\x0015óDõ\x0007BÖ\x0004Gs§Ík9`L0L¯xÜµ_\x0017&t¥Ié¨
>Ô¼\x001bÏ8¯C³»Ù}£&8ùFRÒ£O\x001c\x0002·ß×4[¨.\x0003'[@ì\x001aÎÕ3ëï']¹?D
:#Å&ÕMq½ä.¥«µæf§ÕeÿBü·Ó]ôÍ{l`_ÂuÙRÉ]HýÌÈ*\x0014\x0016ÇªÍ\x0006~¨U\x00198ÖªJ-ÔÀ\x001eM\x000bÀË\x0002[w\x0019y¢ËÕN4ú</<-.ø¸y\x000e\x001cÃF\x0007Ààõ\x000bZé$\x0004©¯«v8¢\x001eè\x0007\x0003;#ý N\x001b¤	®ê÷DÛiñÎãö)WÂ\x0004/\x001e¸Î>\x0002ØãÒì¸ÄSò\x000cn\x0002V»{á\x0004g÷Â\x0018Ù·óêbÑeJìýÀÚ5pbíºmÈZ½È´\x0010Ûrq¶S¶%£Øçþáç¯\x001fôÜV#dA9Iß\x0016ù³P¸\x0016³\x0005ý®BÍ\x001f,é÷gLÆ\x0004ðÌQÒ!ù\x00118OÊÞ®vÊ \x0007£&íoí	
oía½ôL\x000fc\x000c \x000exuPM\x000bô¨ímI
^$®×\x000eQRkz\x0002;ÄBÊ"Ø\x0001\x0006í¡\x0018 \x0016ÎäQ×¸%PÏÅ_Ï:ë6Åð7xCðú\x0016é\x001dàçDâ»Å¸ÂÜÒöÝ5Á¡ñYÀÉ~]Á\x000b
|9+	ooÞz/l0\x0003÷Z\x0002%AU-Ãfsý ¼N¦ËÉ~÷Mp\x0010ûé/\x0018Þ)8j+ÁMsb\x0010OðF#w(jÕ*ký(ám\x0001\x001fÅ´]_mbwÄ.¤ÆÓJ§Yñì¬§ÖgÖK}Ù>(j'Ë¦¡Ja«j£c\x0017,àåÜ¬4Á3,\x00155{\x0000Õ)í0Á\x0012üa«iÖð_\x000fû\x0013æ\x0005^\x0011¼àæ­ê\x0019{¹A¬5UÖã\x0005»ãÀ;û^7î{õ>¯¶2Î\x001a\x001c.aÌ s\x001ddwBY§\x0018y(ø¶,jàÂ\x000b\x001c=\x0014Úé>Øê\:×ayØiSC],Ï°SÄ+¥\x0014Ü\x0012%«\x0006%°Ùì¹rÃÎ+×6ËçkÊf}"\x0015UYÜúÆ».ï´Û>\x0004ÊÒ\x0004+\x000f\x0017\x000bè½¼ÑÙNÏÄ\x0014òíÈÊxdEYÔÏ»NÎ\x0001Ïv\x001bÉ«jB2\x001aòvö\x0004ïh·Qü#ò¥:\x0008\x0007SY=ÆnaÄw{ÐkØ\x0005JôÃÊÃ\x0003¸òûÈÊÃ/IÚ­Oàr\x0003\x0006'²Æ\x001a ¶\x0007¼D68qã¨·W\x001c¹ênyêf±y
Å¥j5zÉ.Ë°á2\x001cjdO+ªL\x0001ú¿\x000b»3Ë¼àÐ6îÕ\x000c±ÂÀ\x001b×ÔèGÞG­»í*Ó\x0013ÜÇô8ÞÍisf®5Ì³bï¯M¾I¤\x001e<ìMH_©
\x0004^ì%pÙ?\x001d-Ù2ëyõYtdâ\x0013(u\x001f\x0019Þ÷½¾7Á¡¾§úP+ñrlðíV"ÅC\x001f}0Ë/ÇJ\x0007É á\x0010ôøº\x000e_@#l?¤¤\x000f#h·þøáAï\x00012]>r\x001aMØÔ2¦lè{¡g¢£oZÑæüçF9}ÉeEUc´\x0015¿»§¼ÀÑ=E-2\x000e½|Âe^ù7é$®ï´¥	\x000e´%_$Ðz|]åå\x0015QõT\x0007\x0019¼\x00197ßFQê\x000c@\x0003tÄ \x0016ôå\x001a'°±¿oóâi^çº\x001ftm<\x0014\x001bó³ãÔ<»E·¢[ùBÐäUwNÅÆÔ%Y.æc~(:Nt(:Ê7C
>9ÞYÌZ\x0005ûxèÖ\x001c|0§£#ÁH\x001bÍßï\x0015#ø¶\x0008)3zw¦\x0019n;)ÐN
hÌ&\x0007ebÇâ8K2ÌÃ.¨ö\x0002\x000b£z<óª7ép¶´L{w7Ùæ\x000e²Í^þT\x000f\x0013§³OXkT\x0013Ù\x001c2dÆ.[)ÐVnO¯%Ó
û§5î¤Ð\x0013&\x001bú9\x0004\x0018?<c\x000f(­æ]l-Õ
ùXÈ)`Ð\x0003µk¢\x0003µK{¡\x001fhyÉ!mÃ7VVÙ	üAÇdB£SXÍ\x0019oRp$\x001b²ÎªÍ*\x0012?Ð\x000fÚ[Ú[¾Vºï6!¡³gÌ¹\x001aúÞ\x000f;ÑA|IÐiQ³S²­«¡-\x0014UE÷\x000btê<-0ny\x0016\x0002g\x001dþ¨8\x0003¼\\x0016þð÷\x0002uEuîã'n_¬ü³¥\x0018÷ÔD\x00079=X	]ÞôÓÎmB\x000fviÄ^üBÇ³±gx\x0016yí\x0002G>ª\x00005<5îeÚ\x0013\x001e0MNÇÈFvUgUh}\\x0012z±³1]¢¯ñ\x0003 £¡f\x0015\x001b5Gè³gèÀ×èÀ×ÏH6%.\x0001omü~Éæ\x0014ªÄ½\x000b:¾1´y?<_µæÀ:.°Î¹?Ê\x0011}\x000eîÆ\x000f%ýúÍÔíHDí2\x001e\x0006^Ð «;Ì~Ë\x001fRX\x0018Z"\x001eõZ&øùu4~xÀåÎxÈGr\x00166Ô¿\x0013ÁÛ\¥]£þ\x0000è\x00052¹²s"=\x0014"êV§Éñ%§3~x(Ò.@=Ðwê\x0000ÿ Oã[pW1¸ÓlÇFã}êÊÔ±kÛ\x0015N\x000c¼¡zå8\x0018yO,ô\x001bÙ\x0019&6ùç
ý²Ô\x001b8¬\x0004Í.>e;ù\x0008¹ãó¢±ß¬¬ËñØ\x0012Ç\x0003Æë]\x001e\x0003Î÷]k¦<ÐWà¨¯¬	FpìZ8¥YÊH­ÚÉÞnË±5$a\x0002©Q\x001c\x0017íÓ¨qP"G[ìíx\x001d?\x0000:$\x001aÆâÌL â$¼GúÒí\x0003|ü\x0000ÜÓ\x00089FX\x0003EA65\x000f=\x000f×à÷\x000eyC÷È_\x0019¡F³\x0007:ZÌ;±Gk6¸|ÓñÃClUÖ÷rTÍ\x0014Ê2\x0006yÑ7íí\x000e·\x0018&`\x000c\x0013r¨®\x000b\x0011@;!\x0015ÆIÞYÝþ6ôCÏ\x001a
<ó¢F(\x0015\x000föVI\x0013V\x001fx£tnCO4tW ð"k{\x0015@nÄóNÞè@áà`èäMæà\x0005î\x001bRmÌ ðb\x000bæ\x000e\x000c\x000eTk\x0003àÜ\x0005M±z_#²\x0014óûVuö\x000b:éüöúÖQt9À"	\x000f¶\x0014\x0019}äãía\x001d=Ñ?õ´}ßÖZrbeh\x0016äNÕìJâ­ú\x0012±ú\x0012¬ÿÜ§Ã´\x0010\x001fÖºO	¼gL¼_"y
éú{ÔÕs\x001dEJ 8CÐÇ\x0003/ÝÐ\x0013\x0015wúT<6ô(á\x0016£\x0007nðÍò¬O3D:4>¾£$¶\x001dE:\x0008¦ÞÂ\x0013*\x0015±5¸\x000e¡5UïdÍÿüó×_¾|\x0008a½®Æ\x001ak¥c\x000bUîæý]{\x001e[;´6ìBW2yß\x000eD\x001f3¶£ê[\x0010©!m!ÿj8¶ó~\x001a6Ê;8\x0015ÏéÊÖ\x0012»Iùf~ñúa\x0017Ð7TgûW,2äW\x0012
+fFò£eëðÈØ8nçQÏ)÷N×w²7\x0003ÉC\x0018bÈO\x0018"£n\x000f\x0011gô8ìw\x0014èÄ"#Í\x0002z¿ÇÄ\x0003[x°K~\x0013\x001c\x0014[ +Ø¬;$ú2ðÃKÄÀAP°iüÞ	\x0004\x001fÕÕ±«k] ï\x001dóëº\x001a\x0002@Lñi×W­ùn½@'\x000e\x0005ÛãTÍÉã¸åò¡f­\x0016­~oìà\x0015>æå øæ)2jùûlà@\x0007k]¦\x00015®¼ÇDª®Ù×¾ô»dÌ\x000b\x001cG^\x001eqÐ¹1\x001d.CÙ-¬fYpxW&£S\x0016\x0016]ÔEBmH£ÊÈ\x0003;?ë¦\x0018Ó
<!¸\x0016jPu	í@dà,n'Çx=ÅÛQ\x0018á(lýyÔÕ0
9M½âý3 ÷Ø`B?\x001c¹V[Ci;µM"Å\x0015Ïé\x0013\x001b÷eãGÜø\x0012¦¬Ãk C\x0003¯£Hs0¾à\x0011&\U¦_á9)´Tà|Ùù\x001aw\x001cÂÊ\x001fòäw0j\zlòÖ\x0019i´wÚ¿`=Î\x0007vfù\x00032'\x0003rÆÊkl3ò\x001egüÃç\x001f~úíoþøãç¯ÿôQê
òåÚ_Ð¼ýûY\x0019\x0006Ýþ]òì7ûûë¤;¼yò¦÷ïå|
\x000fl-«\x000f$V$6;ÃQlØÜc »Â«]+&n<)åc´rü\x0005\x001b[äô\x0003;\x0019¯MzTsâ«OÙ/þrgçåÎÖ/\x001cGFï]ïÈÓ^c.Æ;?Å.Ø4ß\x0005É}\x0014Ãf\x0016\x0013~Ùûnîl{£ò\x0004Ï\x0004~\ß\×\x0003|\x000f6&8äÈz\x0019=/à\x001a+\x0007Õ§ÅtÛ»@v`¦¡ñ°zF^I+CF¼±÷.Npì]ôj\x0007\x0001åò°4tÆÆEþõ¸Íy 9Ï\x0011\Bµ.ÂÓ\x0012[àJ(f~\x0003¯\x0004À\x001cÈ«¾Bä¥Èì¨ïû©y¥±Só?þüÓçß>æy&_\x0016ß­N?èäâºNfäY\x001eÎzý}OB´\x001f¿Û¡¹ße&I\x0003T §Ä. ×'W)oé´Ó\x001c§"'o"Ç\x0017ìØZæ.lí9#ØÁ\x001cÐoØ@ä\x001eÚ9àd%!
ºqËÅ°\x0018CÉ®ë2±A×eðôÁsra\x0017bé½Ü\x0015Ûþò3è\x0006Dn%éAp#\x0014m\x0018\x001c\x00020\x001a»úm¶;Î¶C&LP¡ú\x0016¾ÙÛëb\x001bcÐh\x001b#£ö4êêH¾D	 <j;Ñ\x000eÙç©þØ)|õW+µ¿Ëì± {±$ëé\x00121l8ÐF§14^¥Ú(o®]0<poVÖ»Kî\x000b\x001cæ;Æ\x0006ÕyïH­ÞÚ\x000fÏ«»¹i|z\x0001/¸NGSUõu!ì¹Îåá¡L<¥pàª¸k02)ß-îuóáw ,\x0018vÃ¯é±\x0014*ÛÒQ\x000c6myïÌêÓeÏ{0¯sJl\x0003\x0016·®\x0015¬ü\x000f§bQc	»¦\ÚB°Vd(Ø\x0019¢éyêDíÛ7J,Fã¾\xÀ}0LÂ\x000fO/¨ÞÃê2iÏ³\x0003áÒTtp)«²Ð÷TÏIììÕóÈ\x0007Uô Soà S?\x001aÜÐè!µFªÏ]É\x001b\x000c>*¡§¢ÿ\x0004\x000fÿá¯]¥ß¼\x0015üvû$¼}ä À^ºL2\x000f½\x0018ú©AÚ5H'v)\x001feÏ¬\x0014GÂEjÿÅ=q\x0004Jy\x0017\x00041ì\x000c ºr ËUó¥ \x001d7\x0016[\x0003mÞû'tÀùV-!\x0018¶¦p¥ÂýhÕ\x000cló¡\x001dÇÀ±ÙM^@P_ujôÛ	ÜqÚK
éþ½ÖÀ\x000b¶Ðjo\x0002+Ê½ô8+Bh¨µ
þew\x0016Èùh»
J	iß+õ\x0000æå´­V2?Hì¿À\x001b\x0017,öé)\x0004àÜdQû\x0010*8XXOpì»l¹Ñ\x0007íºhÕ%\x001c±5\x001d©AÐ¡wk`W\x0007\x0003WW4h$Ò$\x0010kÉ\x0007\x0012\x001dn³
~`)\x00188ù°\x0004\x000c±´55ãæL;8j\x001f²|õÀ"0ìäpRâ'\x0013ÕZÃ¥²8Ó4?\x000e¬zè#2hjoWÅTXãÅ³êDòlEÜì=]wÐ	ÞP
A¹Ï\x0008\x001eØÒ@âgþn4Y´ÛQÛ<ZdèþU/\x0012\x001bI¦ÊcÚ\x001fjcñÐj¯/yÉüöÃ\x0007©?É×äUòóúR[l\x0014\x0018ÈV,þ)«8èõ[ql;Ö¢õuBêI£s¨j1&¨¸Í°±ÇöÀzbc`­´¢B\x0013¬WWkæ§%îÜ	
ÜÛGøÖ\x0007\x001cÅË°}¤aõ¼/ÄvÓAóaéÌCi÷©3ä\x0000>uÚâý¢J¥Ãî+máý\x0015GgJn\x0012ô{R¨\x0004ýï}»é´Ëþþ/¿üòAam3Å¡Ä®i©\x0017C­&ß
Õ.ÈßºÞ~öÉì]|;­vøk<IAöOfîûV0l$$(êf¥m\x0019à!ÉÐ\x000e¼\x001d¤õ¾ØWÿò7üùÇå/þ¨\x0000ë¤Du,]\x001eÔûW.Ú«Ñ÷Lnµx(\x0008ì¦
e=l>5B
YuÚÐ·Â+©±£%Ö·\x0018cbÌ­Wã$è@U=|¨ZiÏ"\x00070a2Ü·Ë\x000b\x001bhÜÚ1ó\x0001^â\x0017Õó©q\x0011FÈ\x001eÿOä-n®¡è/iÐÙñ\x001bW"]#nÝ°±\x0017ÒE\x001au&7ù£ú2ê!?µ\x0005]\x0013\x0019»fÕ±çaÊ©\x0006!w\x0013Èï<êf>l·\x0019IG
-ÐªvÛ	Û­b#Ct8\x001a&vÃïØPYAU7©qN_fì\x0011äîb\x0013\x0013\x001bÄ&Ô¹\x0013ê\x0000Z|\x001f}\x0005\x000för»Oì=S?±+a\x00174R\x0016jLË«<>"èÛ*©Øë+G1\x0008zO9J\x0019ö¢ÖçÛY#cBwî\x001c0S¡=â\x0018;h|^\x001cbÂdc²Ï«ÚSÔQV"Q\x001e½`ó\x0015Í¦f×µz\x0003]³d0ß¤ìdà¬u\x0019sºäú&4¶¨ã
ÈQ*-#\x00104«ÂÅÙ³±·=¼°qÂ#KF&±ð)8^ß³m/tMð0V\x0014\x0017
)­à±ícîÙ\x00176t=¤QT!¤@öí:i<ãÓUcçÕLð\x0003ÏV{³\x000f§ÀS¬ssÏñ¿Àñs¥Þ\x0018y£D¼ü\x001e8¨ËÆ2ß/pÜÊïiÎ^\x001b5	<s6ì4p\x0003\x000f@\x0003×[\x000fú)Ò¡R\x001b<^ãá\x00195Á;X\x0001·>j\x001f\x0003Ë3¶7*õ
\x001b»Í4W[ñÈ*XA×@±ÃÀ;éÍ°#¶ßèî´pRE»BeI²yÃÇ=\x001f7ÁQ\x001eG\x001bú*Ü\x0010aé8\x000f¥UçãíjxµÀ~gV\x000e)ÄòUGuHÑîMþ\x0013üe\x0007ÁQë+Z
©b\x0003*ÁåmÜxG¨\x001d\x000e»®-þKbòiÏ\x0019vÂpS»ðQúWå ((xU8\x0004ç÷¾	\x001e\x0011\\x001doPW8ò}×S%\x000f>º\x0005\x0013	\x000c^\x0013\x001a(»È ÚÈOEËBìâ\x0004\x0013\x001cÅ	R\x0010\\x001bAùH!¶}³ÐtC.aÁFsõ0ÃQ\x00172\x000fð¡æÊØ£\x0001¬ììß\x00176*µ\x0004OÅ¥}h¼ÀS\x001a\x000eºu'å\x0018x\x0005RÎ`mT«\x001aöT\x0002ï¬£J³ÚõåL©Øê\x0018ñ\x0003"Ñ=°\x0018Ü7\x0014\x0019¦6ýE/+¥RØ)Ï\x001eT[Î÷fì\x001cc¥4R(õv¹U¼Ü¢\\x0011 3\x001c1®½Ê7ð÷1òv\x000bà\x001a\x0005pä¥´qÈS0\x0000GÛ¥w^à\x0001Á=
N&Y\x001cé/éìd\x0002mmÏñOð\x001b¨uÌ))îÎ·rê¦2sòFñDËXfVß5
\x000fû\x0002=úíúN,1è\x001eHñÄa4´\x0003^ÈËöÌÞ,)÷\x0014ÿ\x0004GÁ\ÜÛ\x0017m\x0008+²<<Çó²TÆÕo[ÇË-Ë)åxV<\x001e,r\x0016Ã÷½0ÁQ,ËfO°õ\x001bµ\x001f©¬\x000fcOÀK¤Ò±#6ë\x0003\x0013&¥yäçk¨Â
92Vß&8J¿åZ\x001b&¡J¤\x0010K.Vþnx\x0006y·;ô\x000eðñ\x0003\ËôUë*Z+%v\x001e¹\x0013ý\x001c×\x001f\x001etUÝB>Oãp¿:N²ËØM>qo.è¨ìS\x0002Y,(\x0011&¦ðÝ)á¤%.çøá\x0001d± \x000fE\x0012jQmf\x001eútG½,ã7º
cÀ;(iÏ*\x001e[Ý\x0005åª°ÎÅ¨¡{L\x0008
É\x0010@_ÍõeflÉ\x001cz:&:M{wÐÇ'è2í*¿Ãèòâ0ôËÌxL9U­ª²ÚÎñÌ\x0010¶ñÝOú8\x0013ôqT \x0010x	êÿáiä<ëÙ2á;\x001c?\x0000x@ZêeE\5rXL8<Ü¶i mZ#]\x0012a¢Ô´b3AÆMoÔËûÐÓûpÁV2M
w8<¹Äá\x0012p\x001f`±$,ð+c\x001f)¹¾\x0016r<ÓNÊÔ¡³ÔIOø\x0018Ê¬GÔÙ7èÃ2¡\x0013)z4Hå\x0017MÖøÔm6+\x0007Æ	1nU
JÖySiaJE®ÍN.8O¸æ\x001b\x0016áU;\x0004Otí¡\x0019¯³ë©\x0018?<ÓÒ:í\x001fz{¶¨qãÒî¸jÐÉá¤4G÷vªJcÑó¬¶öÅ\x001eP)¤j¥:3¬eì#~ö\x0007õðr*n\x000c\x0001ÀP'Äîcm;X6é¿ìÔ¾jD=Ùê{£Gîm7\x000e_ÒÝ4Tò®Fdè\x0019ÕT,\x00044qåïb÷Jùõ'5ßÎÜgn§EE¾§è_'\x0016·dèßøái'ÐÇ\x0004hÙkD¼yM
\x0010z1)|¼Æ\x000f\x000fz\x0008ó+)Ðn!±N3\x0002¡£\x0002LÿIcC\x001dÏ¯ ÑÓâª0\x001a[Ô\x0010ü\x001bÊ\x0006JKf½£ º(Þ-Â¨{{¡W·Ìû#3åÔJtwü
­Ù´qêí¶«\x001egrE*êCª\Hà\x0006}JÓâ:\x0016kb9bõøbúSµÐ¨î¬çm\x001cëeU­IxÒI¶BIJfq\x000bI+¤òI\x000bzÉUmo!Ýå0ÏÐ/iÿñ\x0003½¢­\ëbo+GÃøÃ\x0014Ýø\x0001ÆÞ"ß$:"	+9ã\x0018ÝÄ\x001f|»m¥Æ[©yÄxu\x0004¿¤¸[ìßÅ\x0003
½£x 
ù@*M6Ê'ú¨LéÖ ö\x0005\x001b\x0015`¼\x001c!¡½Ø$ã¹\x0007SÅIÇzì\x001aÔø\x0001f=á\x000b©kÇ	
½S´
ã\x0015ÓwìÞq=ÊÅ\x0001\x0017v×,,IKø´Ì\x001cÄO\x0007z@ñÓàºå\x000fáÂ"è\x0011\x001aÅÓC¡k _*­\x0001+­AùÏ Ø¦öÐøb×JvbtëæÓ\x0005½\x0012T|\x0017:\x001fí+\x0000ÑM\x000báË´\x001f`è\x0001Z+äQË,aU\x00106ï?àë\x000clï±!RÙÕÏ!Ð¹	uUUÜ w+«	\x0016zjOüTç¼SYeêã\x000c¿gv¦utIK\x0005ÏúUå	×½*_ õ¨8\x0013x²þ9[,\x001aèä¥/î±Ð»1ÊS´½\x001ftU':9^?ßd

ÚÉ.bgè\x0001½xòM\x0011ÝSKUHëÌô	~\x000e{\x0003è\x0001¨ÂTýô\x00065ñOoÇXÒGý\x0017¦ØÀmè\x0005.çËS[ôº©(¨NK;§w6ôKÄ\x001eÂÿOÝ»ål\×S)ð]¸_\x001e-êb\x001bR·`	|%RdL UÕU)Ø\x000f\x0002<
ÏÀò48\x0013¤÷ÞqÎwÖK-ÿ@ä\x0017S¸2þ8\x0011;öu-ä: nQt,ûX.KGíÄ\x0002¼\x0001·B»'
qÕ#ôK\x001d*®s®7:Fã±e1ë4*N6£\x000fb¯¸ÎÉ]à0'§ý\x0013Hi­ôçd\x0005¦,Ý^¤NV=¡UWI¿\x000cÛ^\x001dK,ê\x0019=Ö{ë\x001ehc\x0002rå\x0006­ÙÓÚ=wtt¹\x000côÃÎ`\x0008\x0019\x000eÀÎ\£\x000fzg\x000böZ{:­=ÁÚSÀ\fF\x0000ººÌÐ£è%Wà`a\x0012º\x0001Z\x0002ºì\x0010Ù+-(ríæC\x000eÆ~xÖ#\x0014_5AG9Þ \x000cg¼ô1\x001aO\x0016&£¿\x0003y	­nL\x001bÃ¼^-\x001f2kåð&é\x000f°öô¡Q(¢øägyµ\x0007ßY>T¼í\x0017¸¶ü=o©n3O£7O\x00125ÕvÊ¡ÇÀ~xÞ"ä2å\x001266â­3zªC×þ\x0013°\x001f`c\x0012®=ÆÄ®]ÍLè¥³\x001cÞO\x001fµÓGMtô+ðÚ3s|ÆnA¸\x0004û±\x001f`ßqdÖ§ä'\x0002¾\x0005=V«PÅ\x0014ÉCR	Á§&(¹°íí&!c\x001c\x001añq£\x001a}¡£j´\x0012¼<]Ú¸À¾@g.¸\x0006ïìÿagB#òÀ\x000eCÚÂ´\x0011ÝñGQë Ø@\x0001.S&Åk­\x001c±×\x001aópælz\x001fñU\x0015YTå(\x0002^¯I1º»æ8\x000f;V±hë\x0018²\x0014W\x001aUöL^{º\x0004Wµ\x000b\x001dÔ~¦GàÑ+Æ'¥U\x00017ZþÊ>Ö°\x001f\x0000Ü¡²îS ìK|0Ç²Í\x0000Ge\x001b5Þ¨¶l>v%[!ð\x001e\x0006Ò¡_Â~\x0000ðHÄÓroÑúh\x000f£V¦rZzÁ¥«Ì"(-(I?:íf'\x0010]ÂvÛõ
å!A8[¨9&òÁÉ¡í¬§²²\x001c\x0019¸ýð\x0002ï\x001d\x001bß*k#{Üúý4]èI´1½ÃO».&Å\x0013x´}IýÐ\x000fh?\x00108p«ÆDÅ^yéÅúêR_ùz.täëé
%(B¬£\Jè}L\x0016÷çk?<èâ>µª 3Ñh\x001e\x0005SS,Ö(N=\x0002	{\x0004
wFçh±M_!ÒyO)^=Åï¦ îL;\x0013qvR\x0000qÅM\¢|_Åì¹~e5NÿþFÿ`$h®WáF\x0012¤ÐèdR»\x001ax^ÇD~ã$¥Dl;©P¿ \x001a&úGÔÁX{?LM~ø³¿üôñÇ÷ÿøá§ßÿâmf{:+ÚxU¡|,s÷3Üu\x0016äÛÎt9Út­³l Í?Àc¦¼½Àüésà\x0008®:J(\x0019·Ày
lolryúÐ\x0014»8j,¯N®WÚ_í£9­»ãºå¿ët}ä\x001d¥ipógWÆÅ\x001b\x0018ý\x0018_l$
¬)4¼\x000fr\x0016xÑ/í=8åµÌÝ|øJU\x0006"ÚZ)o.ÐyV,Éç\x000b<g\x0004h
<Ò(Î MàißéaC§¿Ú¯Ä¶b'Ý
f 5Ñ=HÙ\x000f\x0012ÙH6-EXwj\x001a®\WÖâ\x001a^^\x0001\x001e°R¡¯·+¨àÚ\x000f\x000bo,¸§\x001a\x0013}ß.ãó¨ìÎ\x0003øþh<Å.ñn\x001aqþâ6\àä"\x0015ÎÀ#Éajà\x0013\x0018¼\Ù\x00138Æ=\x0012èÜ¡²Ù°Èò\x0003,ã©ú²}2)3\x0010ÿ`W\x0016P
\x0005%4fàk.þ\x0002Ç\¼öå\x0014Xx	(\x0001¯lïwÅBüIAn\x0019¥7·Rù
äH\x0005+ÖGR\x0017q\x000f®?\x00008oxêÔMl\\x0004\x001eê\x0015\x001cÀ±ì¤,\x0004.Â×
f	\x000fô5\x001bQÃ\x0012L]à\x0018ï_»¯¾½úÝ\x00176úÝÕ£Éj­q7~è¾ñÂ5\x0013Ç}ì\x0006Ç]ñå5\x0014bà¯~\x000f\x00142ëcveÓ9s÷)\x0008tå\x0001¯Ä£b¡=Q¹ºqÈÓJ¡4ÀSÄm	O/Ë«ÀI¸\x001e(\x0011/\x000f£lã\x001b\x001c¿§\x0004>=+\x000fS8ÙüA½É¥Ó\x0003\x0012­¼¾\x0002)\x00050-ó¶Ð)×£¦Økçù
çÚu\x0000O~k®PÛ\èÜyîúhkß´ü\àd´¦+]1\x0019-GÔ5^Ó½\x0006~xRÁGHU*aáaÊ©R\x0010%ë¶\x0014|>Ùv¥\x0016<'á\x001d®¹W¢öcbà|:Î Xñg?4\x000f¼ÙÄp¤\x0002ðCa÷ð%3~Éæ\x001cð 7=îñÔn¢íðj®r9¼lúÃ³î\x0016Ñ¤TÕ\x001f§\x001eUÝ%WòÚ\x000b\x001bÉkÛÕÁ~cËé¦ O\x001c\x0000>F¿¦h\x0007tÁ\x0014m»:ï/èÒ\x001aµáj®k£¡­¬Òô7xFðú*Ö\x001ax¦ÇGì\x0002\x001f.lÌB¶è^½Ï\x001d\x001bµ±(Á$î6x/ý	Ý3ºéÁ	÷\x0006ûT~?§\x001fÕÔ\x00146ÁéË\x000fâàT¯þóîwmä¢\x0012YóÌk¯ýàÔ\x000eø*wñ÷ï?}øé§7\x0012¼PáTjß»ñÐPË\x0003\x0016_}ú-´Äúm9}xÔmÃ6²6JÊþÍ\x001c?ç«{±û0kÖàú0ÞJD\x001f\x000cN`\x0004­·\æ\x0019\x000fÐáb;oß4a`LóËgY?ÅÇ\x000eÙQsAõ/§r]ÄsY¸ÌÇ¡þµVM\x0007¸ª©\x0011";ø5ü3\x000f\x0016qý!ÎÌ\x000bëeê(\x0014¥°¤\x0016§:\x0000\x000cÛhÎ:w\x0002ï/¡\x0006\x0005Oô\x0014[é\x0013\nÈD­ÏN\x001e\x0001UÇ-\x000f¨Þ\x0013¹*)Å<ØÉmãæ)ÎÃ»'Úbä_ÑÀ7EÞSæÁ.cw¥·\x001aà	é­RôØ\x0011Un
w%¤©2\x0016ÒÊòv78+±&.Èz\x001cçÓ\x0002\x0004í¸Öïõ¡ß¸±yP0"ßm!u>9	Dt¤\x0014ÀÌ±-_Å¼Ã®ä´òbÂº#ÏPh\x0006În¢Ñy§\x0019ØÈ§©* 1®³Ó¸á³yÊjnZ;kGÿÀ.ÐÑ¯µM¬ÄêQÁ^[\x0006§úºùße¥î¸ÀºCùÓñkJÌÁ¤Ën^ùJêª&6À+¨i^\x0005µÑjhÕÂ\x0011x´Yº§.pØ\x0016¥wÀö\x001dW1\x0015o¾±\x0018µ\x001f+uÓ\x001bàÓ3ò\x0015°¶Þ¡ðºré²ò§`ÛÂ×Rã
¥ÆA\x0008\x0000\x000b÷/Ôð©NàúÝt\x0008\x000fpì\x0010V}BlhÐ¶FHI\x0008x5
ô¬ô\x0013vGìÃ{úÕÇø_¶\x0013±\x00178^}k%65\x0002GÇ\x0016æ³2ÆÊÒÆ\x0013ÏCû÷õ=­#\x0017ôÛT D¼z`MQÍ\x001fc+{[n?¼À5ß\x000e%u,xk\øñiÌ7äM®ÓÀ³\x0007âX	óéõ\x00155\x001c-þ£}qÌÄäuÈùB\x000f°tñÜPZ\ÿ#øàâç\x0005n;íB_/ô\x0004$©:vøÔÑ´Í\x0008Ûdg\x001c\x000bsêü(Öí~ûáAÈgmjÈ\x001d«Í\x000cîFNm'½À\x001blÌä\x0011iÛQÁ{$ÿÍ©ÛË\x000feáuÊq \x0017ÔÓ.5Ð\x0017\x0017³UuAwTì)yá\x0000å\x001bäîØU±mR×ÎOtòã£Wd?¼Ðå\x0000ÌÖ¦ñ£jÀãºÛð3\x000cpàg\x0010ðË¦¼ú\x0002ÖuÇ¶1»ïétQ+]ÔJÍ\x000c±vt/äÈ4îiRÂ 1ú±7öÃ³vOÝªZ{îiÍ\x001cxnÄû°	¬7M_¾ûûø¿{+\x0006EÇ|sj¹ÚwqÓÖù©ß6Û\x0008×\x001f\x000fJ&	CÜk\QÿZb¥O|9jNõÅ:A£|y¦ 
ÚóP>+`«£yÁ\x0007ddX0ÂmXtìLÀÕ\x001b+¸Ar¾+V\x001a8\x0016+O÷kGcá\x001c°;.\þ+ \x000f§ÿä¡Ùå1®±¶Ç\x000eè#Êâp!7»}\ñsÇÂl£ësA#[ öÚ@áY\x0012n2\x0017çÏÈ¥\x001e}Ú@S&×pï½î\§­È<\x001fWM.n\x0002\x0003\x0003\x000eÁu¤ïKÒA"jõËFã:<xaÓð`BS©!à<áÇ\x001c"J\x001b·1fu\x0003úîÓ{±gß¿5SÊbV\x001bMQ=ÅÛ(Bæl[-Ú]Útl\x001cª:(±QdÔ\x000f\x0012´×í-8:®J \x0013'Z\x001aÝOOnàÞ#xxT\x0004\x0014¼\x0010c¡wRë\x000cãùÓÂ=-<Q®Wÿ)ô2VÐqj×¤ëj\x00078Êê¸\x001fXyå
F\x0006\x0001Ùo.Ù=¸þð»
/ÆÍàâe²åñå@*xg\x0000×®¯Çb¶ÂÊ'M¥Á	ü\x0012,[ûÃ/p\x0019Õq0õ-wäáUp¦£òÞªqm®\x001cà\x0011$$»\x000eF?%0ù;("ÏÝÄõïòHm¢µ\x000b<#øÃImà\x0001G-\x0014¼N&¹CG@:\x0002´;;½\x0002*\x0005\x0012\x0015\x000e ËæF¥j3±tè²EÃ\x001dÒÞ\ÈÕ¨X4ÿºÁé¶«}×©ö-àêrÀÊ\x001d\x0015Ö\x0005<s/C\x001fìÇétû\x0013Üþ®Sg\x001e\x0016îØñ\x0016g·ÜYëvZ\x0016/ì\x0008!ÓÓñ|Ï¢:ô=\x001b¾{±JÜï\x0003x\x0006Õ	ßòë\x00154ÁÛÀà¹SVÂ÷1=·i\x000b¿À\x000bîJ~(\x0015\I¤pËåà±,­Y]üZGÅ\x0014?gö¯ Ðc\x0013Ë\x0000KðÃª´F^×!÷\x000b»Ò9ì¯ M±£çé\x0018Nê±â\x0005\x001dª±uªÆ*vÅ
×u·@ëæ¦4Y·ð¬d\x0011\x0017x\x000f|ÆËs\x000e³qVDçU%1ìÓóýqø1åHOØÑó{\x001b'ÜðP\x000cpà¡\x0010píD\x0001aí°á\x001béÛV.F\x0001NzëjÊ\x001f­ëtyÃpó)\x0005,Q¯ì\x0002ú\x000b\x001c¾§WµÀç\x001cªî^§wî¦«£\7é+\x0003¯¾ò­¿æñ\x0014\bdÔi¹Mà~ðP®£\x0017xmñJ~þìy§^¸TiEK\x0013CçðA+&¯¼s<+=¾£ÛIõ\x0019é0¡uð®ðx'zÔ^ÎìY/ºá¤ºÒßÈ\x0005­¸ÃÇ-^CÑð-öS©åÈqÓ+QGn9 ø°~7¸jÅÓÊ¯\x000cn]\x001b}\x000b\x001cõ}´8\x0001x$m<\x0005ï\x000cÂ\x0000?ÂF§0Õ×p¸È7?ÂÛbÍ¨m\x0015ßº°Q|ËkÛåó¸#ÃÎJäûâêÑ¦L8À3ægÅ</ò=iüÆµâ¹ÝºX&¯¥?<\x000b/ýâT2}éj²ì¿F{ÚÊr7÷>¾´¬\x0015¼\x0012#>´á¹\x0005£BÝô'\Ø_|H½hZ9zÂî\x0013¸EAmÅ»ÀÁ¦HÈ.ù=\x000f\x0006_·<èíú:Ü7À;ªÀ©^@\x0005pÕaÇ-/÷@Åäú¦gg£Z\x0010k"¬<Û\x0004G&JÔÉ\x00028·r\x0015\x0019ºýð §\x0000M!ã\x001b z÷Åt»[E.ô\x0008ô\x001eë}¡7~&J©\x0013ú%urðÊí\x0007@ÏÐ¼l\x0003\x0011½\x0012:õa	D\x001d\x0004\x0007?Î;ôã´h\x0002ÆÅ_Óó\x000fzãI¶T@öGÆ~\x0000ôÑTüBwH>#èÌq©<ÁZôpfASÐ»Ç\x0019\x0000OA¹@óÂ£Y.­î¡=ÆYÑ»WI\Û»t&\x0017³6½ÛäÆXÄ=ó\x0002`\x0017\x000fi¯æ\x000c}4½Ð3.]\x000f\x0008Ì\x0017»EV·²2®\x0017ß`psnÆs\x0006zEÅ!ºu
=¬j\x001c>¶@sSA1ô\x0015é¬»ÐØ;om|\x001c\x00041ÊHqB\x000fÞÐsÑ@k\x001coR\x001c\x0014zqÓújà1ÂÒsHè_È¶!·°kJüE@ïw-ÒPU±èSút\x000b>¥·º\x0006.îêE?³¿Hö\x00034i8\x001aÀâwMó\¡ëï\x00000âk¼%=KWbZ\x0012%æ\x000fò°\x000côýg?\x0000z~×\x001fðÐi\x000cHéèÀKrñ ì¯ýðË+ä+ GjòTsD»\x001eé ´J1ô\x0004S)\x001aón¹:nt*D#àý\x0010>
ùðäÙ\x000f\x000fº{jû¸\x0006\x0000¤GÎ#¾ÊÙaÉ¹¼©ò\x000cp¨òHdÙVm+¦4«V\x0012z\x001eã\x0010=`Ã´<~õ%%t
¦PÇ]æ\x0010Ã·:83\x000eÝ~xÀs·º©\x0004$òÿê\x00009]S?Ð¡lfj\x0006z¢æÓþWtåü\x0001pÑyé£ÝAùW\x000fà\x0015z×jl0Ö$ã\x001e°T8`ôCå+ÔMUßÐ+JMWÍ]Ààr\x0017ã'U^nB¿¸ÖêáÉ³\x001f^è6\x000f\x001b\x0013\x001aw\x000cËkwÆý'ÁáÄ4ì\x0003kJ\x000c\x0001íä5³\x0004¬£
\x0016ÛÚÛf¸s Ãp§öÀ@¶¸\x0015e.AåÊÂóÚ\x0019\x0014Gp·k'¿ã;l'ÿ?ñÎÿD*Ó?\x001bfÔU±cÈÆ¬g°)Y,³-ýðåóoÞ¨Èïø¢Ädóä·Un¨Ûã5q\x0012¿mU,kàO\x0011¡Ýûõ$B«o\x000cð\x0004ªN"ÖÕÀLT5Oy5Óí\x0013iqB e$étN&SÊMÀ©NÍ»>Àé]W\x0001àØ\x001bÎÍË4\x0000\x0011ü\x001dëqÊé|m\x0018ùòÏ\x001f>¿#Eã¨ôcü\x001aihpÕñ!tò¬Â7î³\x0017Ë¯§iµ³y\x000c¢G\x001cw+\x001e\x0013\x0000âc2Ícz\x001f9-;_\x000b\x00176rcT%ç~b"³ãi£	{¤\V_èÂÆ	ÝÚ<VB
D\x0007¥Ý¸ô	ÓÐ
÷kà\x0000÷\x0001'Çð\x0010r\x000b']ã¸½àÞÖq
Ötè\x0005Äjâ\x001bcUS.8Ú #6fÜë{AÓ\x001cÊ*<n¹f£\x001cÇMÜè@\x0016ß~\x000f®?<;Þ\x001bÌu?)åi«<{ÎÍNJXSþ\x00178Î.ÚLî\x001d
qBª\x0011»üµ\x000eOå]\x0011»w\x000eqÓIñSrN\x001c×Ññ²D\x0017v'Â n-.¯\x0008ÑO\x000cS
âE§};Í
\x000e³»Dy«|\x000c=u(øpnWNÅ|M\x0003köVÿà&õè+\x000fs«¥¯\x00178R*öÞ)<g\x0004\x0007\x001bl\x000e,sb\\x001cò\x000b<Â,j
Æ»sÓ( v!q bÐ\x0012#ù(ß\x0013\x0004\x0012ÚpB\x001b^çwÁOã:4q#¹¶Z\x0005Øq\x0015S%ö'Ça­\x0018
«Ü®Îø\x0000OØ
@b\x000eé\x001cê:\x0007\x00126_³Ê\x0010_Ø\x0001	rÇQîÞ<©«Ä\x0010Ê\x0014\x0001©M+Õì
Ø\x001aF\x0000°3Ò×É-r\x001ajÁ£3P£û\x0000àÙ\x0013\x0011¤Î\x001aðÊG²!È¼ÀÉ·ûÜ¸\x0016\x0002Éðé`\x0017O7ôé×|
\?àbL\x001bT¶$\x001aw|té\x0008î\x0006c`9=o\x0005·x\x0013¨Þàiþu>§®±D5#w\x0003\x001b¡òÒá\x0014ºx§\x0018«:MSzÕzßZ\x001bØÈ0©S~2³©k$\x0015)PÒÉãjÅÄµ²u?­¨º\x0018qV
ÂÃò<\x0007jþº¶]^à\x0015wEG½\x0017Î*8uFjY¬ï«O\x0003\x001cªO*½ê¡ \x00169<f~á´6\x0014Ð\x000eà\x001dä	ä<ø\x0014­dÄe\x0018qP¶M ùzy4Z\x001e\x0008"¸éæ1õã×l\x0018µã¿!¿MÿòðB\x0016º°ñ3k\x0001¬ÁGØÄ²_¾û÷\x0012É¾U·ze@Sxý\x0015I%c1Tìþ\x000c'¯Ül\x0005²À\x0017°ÿc¾º\x0011O\x0012·ñà?¼ÿòÛ7ú"±D\x0014â+ÊwëQ k*\x0006iöË`0\x0016.`p5q\x0004`\x0002Uø±¯ÚóJ,¸QÛæp'r\x001cl¬KÚâÆFGFx°UpÊÓ
d\x0013MÄ\x0017±úm\x0003;5ö~\x001e-Ã&bMßëm\x0003©~m\x001dàþi§¸"qXm<Ô²¤iÝñ
iqy,=´ô\x0008¶c\x001fB	R\x0018üóYï×\x0000:\x001e´\ô\x0010í+xâIZ\x001bâBpï\x000f}Â\x0003;à¦èpd ã¬Al\x0014}ë,«A\x001f\x000eaðø\x000e7\x000f=TµÈ± ø¦\x0015WÉZO{\x0012hOZâÌ:uÃ*k)e$´í3\x001fÂµ8k:,\x000cdMU³ïÜª21\\x001c×iÔ\x0001\x001ea\x001a5ê]\x0000®mk´+\x0014|[ènØ«\x0019a¸G]\x001fè0©JÝÔñúd¦\x0005×dÉE~}\x0000ÈDE\x0013^ãy\x0006'­R\x0014«Äzcncu\x0008/ðàPa}\x0000OÓÊ,'n\x0012\x001e\x00178n¹æÂ`å\x0019Çu^¬aïæàÇ¸È\x0003<VÞsøJC+W\x0019<\x0002\x001f\x0013\x001b½÷\x000b<5v\x0008\x0003\x001c\x0016Ù¥B'±syCskjk×:á\x0000O\x000e½ÍÖ\x001fÊ¦ª=ÂMd'*Ú1[\x000falÃX5¡~*àÌÅ"àÓç8z¾\x000f%!\x000b»
?BoIÔ<:±ü$òÁ½AÆ\x0013±\x0012$_à@\x001cu04Â¶- Ô[	\x0008*Ê)hàèaWòÁ\x001f}S\x0005/
¿bÈQ^£è,mK?Dýá\x0001¨8ÓÂïL\x0016\x001eË´ð~\x0008cã\x0012Æ*{ÆS	«ªäIII\+	{¬y:\x001dÌþð\x0002Weà§£¼æ5jÒÀÇ\x0008OÙ$=âñ{Æ
-åUU½ 5æÞè~êójà-/\x0001·¼4`³\x0012¯º§ÕãÌ\x000c>eËÚuw÷_ü\x0011ô«Þ¬b¯,\x0014\x00176°PèÈ:~Ï¤Ú¸ÍgE\x000c²È'ld¸Ð\x001d\x001a­ä+¶7ë8£»_GgF=ÛæV;yà\x0006©¢\x000c¥RkB§¢È\x0019\x001fÜ\x001c§Xé æ\x0000ÒªõEJÉÉ+w6×´Ø»À1¸O*ðÜÏ¨\x0003O§¼ÐÁ/ÙN¶¼¡-Oª\x0002\x0004Û"^\x0005\x001d\x0016Ù\x0016²Z:Ígà\x0007_«\x0001\x001f\Ô;\x0003\x001fTm\x0001ÅÜÄ\x0001uåæ\x000fµuDö\x0002\x0011YíãVaÙÈW¨öÀàå\x0002?¼
D{ärû'UPÏî\x001c\x001f\x0016g'±orÌÝ#aç®ÆX­¿clôXä\x0018vã®ìëüÎ
\+Q»l`Ç\x0012\x000008\x001b­ÜÌ×ê+GÄ\x0005\x000ecªWf'ï\x0006gb\x0015\x001d! ð<´Í×.\x001b\x0003·\x001f(ò\x0004\x0017T\x001bÁ©¸Ô½çm\x0019£J\x0004v@\x000f\x0019ÑGVùFJæNài`\x001f¾§ý\x0000Ø\x001dÒÀ:*f\x0006°\x000b\x001dìÃ%W¿7-\x001e£f}Ù­åðXÕ¡Æ¢\x000fM§ð\x000ecò¶{Üu/ogt~Ó\x0010Nw+1î\x0005^qÓ£C_Né(üP¬b\x001aMñÞmjË\x0003½á¶+3\x000c,=gVêè©ÒÆ?5V\x000fá­§_³\x0019ÐÌ.Re'wè£x0]öÃ\x0003®Åç\x001f\:öF÷(ÅÑZ¾+]_àxKK\x0001ï\Ãt>-ÒiLeÅýÁ)²\x001f`å
Fµ^Â\x001et'n.A\x000fCLvC[¡'Ú\x0017>0q¨îÂÚkâM\x001fz:n×6õ
s)
l\x0001cÅh´°'-§#£ä\x0017Cxü7ä7þ7T®\x001aBX%P­0gÑRÛ0}æ²'ü\x000fßÿñ­x>µð
n\x0008Æ\x000f~÷ëü¢NYÝìó|Ë¶)	6Ü(³[,G\x0008g×¥ôÔ¤õ¯XôM¾¶bÑl¬tsNµÉ@2×\x0006©ívB(6Íµ)K
ì4Q>z\7ýªô\x001dc·Q =­;áº£Çu«%
´'eZwµiu&÷Â\x0006ái@ÀÝkò\x0016\x001dEºsÊÜ£UXRªJR\x00150¥T\x0006ßÉ¼ä\x001dóõ%þÃ\x000fv\x0014ß¢t0IËí¯û¥ÌU/\x000e¸ Ñi\x001c\x001eí·¼_Ýº>þûU§û¥ôg\x00100·¤mM\k\x000fÊ.C¼t}ë/hLïçª\x0006\x001a\x0011>ÔÔîÊ\x0018õZ_.lYSÞ\x000f ïO®â°\x000ehX_ãxSÙ\x001cTÃîØ!P´:^£ûÐñáyKÜ\x0018ÄÚd'\x0007ý'á©ìýQ{à\x0013\x0013=Ëõâ\x0018Y}·\x0001¢\x0006r\x001a±\x0011&tVÑÕç$þ±4¹[A\x0012ä°\x000f¦!\x0003Q\x000br;cÓÇÓ\x00186®ÕB$_³áÔW>ú7E=\x0016\x0003ßX´\x0001ø¨Àç\x000c9°ôÓÊS2vC_rã9ôØ\x001d$à4*¢÷4 ¡ÉG?&G\x000eà	ko­ 3»\x0018_\x000eÆÍÔ\x001049Àgå¹>²\x0005Ôê\x001e)ëYµõgÜúÃ	\x000f$­Ö¨I?x\x0016\x0015lê;R\x000cË¿oÍÁø\x0012\x0012w/Ð½peý&sÅ¬.V\x001bzë\x0014ã\x0005\x0012±Ú1õ|Ku©á°NÐÎe
\x001aÈ
\x001d\x001a6\x001diK ÉÍi\x001b&a\x000f6¸ð/ðÉ^A\x001fRÔ\x0007\x0002g¾%=\x0006åÚ7pîPÓXóÙÝå\x0001gÆSS\x001eý­ôÅ\x0005í£ÚAI\x0017§~
5ìvrd´s8I\x0003®?À¶xèñ¬ú	2O®\ûÚ\x000f§\x0018ø v§Uj(.\x0004\x0005nw9]ö0í"ÛjMÍ/c\x001aõ¾H¹Íoÿ¥æ¾\x001b\x0015yY®ù\x001f\x0008x\x0012W¦p"Aþ\x0005þ'ªíßé'Ü\x000fé¤ _ÁãcêÉëÛ>å1;¯¯ï£ª_½ÿôéã\x001fþçç·RP°¤0.§Õg EÇ¾pê«hóó7f¸wCÓ¶Itóô}â\x0013üÔImrÊÇ¡\x0010£¸\x000eÖ-¿i²\x001cØÜdÄ[ÍÚ­Y2½ÝM|ÒçøÄÜ\x0010PÑy3îMÔØféûÁ¾\x000c>hkèSÜmÚB\x0019ù\x0005\x0010/ÄX\x0015ÖJÆÀîØ[Ý:´\x0008væJFà\x0011\x001dÁ\x001e~ß¦%«^\x0017ÈÙ©â^z¶[E¹¨X/ï\x000bw\x0012\x000ef÷]\x001f~ûðO§þ«WÆÕ\x001aà0y+à\x0015F6\x0004Ü±øÌ4¹äZ\x0019-)§ïHT¹Ò'ï%ÿÕÎ-)qîÞ,§=~jÓñMUÌäÓ=83WV\x000b;AAÀ!Fm¹¡Kü1zt<Ð¼ÃÇB:\x001dÛsG©ñ÷¬Ùí/2À±Ú ytÔûq$K\x0018³ã£âËp\x0016Ö\x0017× \x0013u(ëà\x0019`3±»5\x0018ñG#;Úµ?÷¥ýÙiå\x0002ºkæ.âÐ¦ë©eå\x001a¢MKW£¾R?|ÿÝÿõ\x0018ñ?û\x000býõm8EÇº­ÒR½(õ\x0003Kºæ-¾i¢«³·(ÑÎGvQ­'Ñ!êD\x0000Ì´*y&.ÄÆ\x0013Râ*Zì\x0004Dqêd!ÍUeÚ&¦«î\x0006QÜ\x0001;#¶6ÁÁ´¯\x0012×\x0013Ñâ4QÚ EñË\x001dàÞ\x0003US-çûª %ò\x000bÅÂÃ:5\x0006ÇÕ»½°bÐ<\x000bO¾ci\¯\x0016\x000b£ÖpéÜ.Oá
^\x0001\\x001dYàS-$	'0jôCv±ù\x001780#5\x001d3z\ZÙ\x0016Gº\x0015M\x001fÏÛ2ÞÙ~ÚÛ¢}k@åÆ,Ì\x0002>Q\x0016Ô4X(ÖLÜ\x0000\x000fO&.\x0018ÿmQá\x0000Zyd\x001aÇ#¾N\x0008_à	\x0008bRh\x0003¸oL\x0017|ám	\x0003|¥ë¾À3\x0012Ä:Äròê*L\x0003£¥\x000e¥ÛÓ\x001d
pZk(¼jôy\x000cîx¸KÙ\x0016­¯tyh/p`Îlíj³\x0001p\x001c×p2°\x0017Ã	\x001b¹jg\x0002\x0001öQÐ¨¿Fý|ù\x0007íÇª¸ÁqW<H\x0019\x0011]@«%a93ÿåñ=×Ø\x000b¼ãaIÓí/\x0018\x0019\x0008xîÓí\x001fÝkRkÇ+w\x001e|Õn\x0002\x0004´-f\x001dÄñqe\x0016¼ÀYP¶\x0005{yMc¢ò¶°ÄhmCëvuop0-ª´ÚÙâ\x000cj1fÛ
\x0005Í\x0005Þ`åJË\x0001/Ú­\x0016×\x0015fZ©e¹\x0016§ìÂ~\x0012ÚÝ\x001cNqÏ´îù95Ërcg\wÌVW\x0003ÂVGûäÚn7 S\x000bT\x0003\x0019 sG]\x0004e}$vw_G\x000bUZÛínp8*+
¼¶¦tÇÐy~ëèrJñ`Vô\x0007Ü\x0013po\x001bÑ®hÜ9\x001dÃ6a±ºÁRêúÕ\x000fêMþîË1Ó'bàWU·ør2bqÇ]ÍÕþüæÂ:\x0012'g/	Ê¶lþ¯îÂîôý'ùñw\x001f>½ÿí[¥¡¬vÃNgºÕ\x0002¢\x0012î<mnâLý[Î.Tþ¤i2Ù¾yLy`°^ïk'äQ¤·¦´ûZù¹°±òS¹â	êt¼\x001d[[·\x0006ñîæ,\x00194jV
ÒuNÿ*y\x0001-;\x00147\x0018WVÃgà>C®¨ô¤:>	}\x001d]¢Ç=Xæ×÷õ\x0011\x001bØ\x001dé <Ú^\x0015\x0014Ìòç¬#	V!<lw@¥ÊÌÕ

äÞ¨D\x0019ü¢;lx Åi\x0017`*ª\x0007ïX[iJ	üª­Ä7xæ
\x0007Ê$å(Å|¹\x0012x¶"Çffã$jbâË.¾0eôk2øP§ÇH2ö¸Z:@êçd³âð¦Öþ\x001b\x001cêaÚñV!4vãÒx'/Fq3®#]\x0017xÁ»Ê$ÐzM/y=û\x0018XûR\x0007x"ás­d<ØúÖ}h=íÊf\x001eåÂ¦y ß­«>W ïÙx\x001e%{âÙù<\x0003\x001c)8\x0014\x001cÜ(ß3g\x0002gÚÍlq÷[òÂÆUÕÚ)\x0004$ÝM;Î^}\x001eÂQ\x000b»\x0012vD>¢$;\x001aVqöx²\x0011âeØ\x0013ý\x0001ö¤¿«\x0010»VO	hU
!'3\x000f¢Ó¼]\x0007xÎ¼áO4¢íén~'Î7_%·s=\x0014ýáÝã~®:ÒÙÐ¦©d©¥ÕÇ\x001càÄ¤\x0014r7+[\x001dMÞñRâ\x0018£9ìJ	¸+[\x0017ã«î¦ÛNÏD§gB«\x0013 U£¬¸ô\x0002eæP\x001fù¶¾&Î/lH\x0007U[\x0004ÖÚæºJ¾6ïxwVgW}î©¡I\x000e­íñ.4KYUV\x0008	â~ôµfv¡cÍ,]|\x001ew7¢&:ðÅèÝôTòF¯¸3õi0îÖYBK/dmµð;Æ\x0000Vµå\x000b\x001cÔCjP\x000béªÞVh×Ò[U»Êh/ÞRïéÊù(Ï®¤È\x0012_5M\x0012_þâ!^é\x0006xp´ðòâ÷°^YÏ¶¼ráLÅÊ\x0006øþù´\x001f\x001eðþtc)xÊÄÕ\x0014*èéØ¾¿º)\x000fÇ% [Zz
G(záNP¹\x0000\x0015B¸6fH\x0019è\x0015\x001eP4ydK
l®MnÖ\x000cÆCì7,V\x0003=ò¶wlQvú\x0015*­¸â'¶ÁÐ¼2-^è\x001e÷½FTÓ/OèõªôfýËÿùBGG4i½¬\x0000z¥\x0002tÐ!\x0017F·9w\x00019ö\x0018á´Ç:Æ-ntåGtÙ\x0008Z»îå@?|Uâà÷*ËGkgóXXçD>j\x001a5ÃSj?ÀÚ\x001fÊ\x0019E×©Fkç¥çë.íè`^w»IR{\x0018øí¾òTÝzp\x0006á¸*§CÝ\x0018þ7jN¤×\x0012\x0003Ï¿¹¨,ç6
BñøoÈoÓ¿\x0011\x0003þ\x001b¹6"b°F\~`ÝPõà'\x001bñ\x0017\x001f~üÍï5hÿðãwûÃO\x001f¿£l:*Ôö\x001d«¦åÆ¢óô¯,Ø¡Wô-ër¡w¼Ó·Ñí³bàsý±ð\x001dÜÈìÅj:
\x001fáá"Ï·ã\x0006Êh\x0019Ó§J±5¶BWyMô¼Í\x0016ïÆn ó\x001a£\x0003nYÁæ0éuwßþl4.p\x000f-®>Ö~<#T\x001a÷ÝüÂ\x0012\x0003ÞÐ\x0005÷$D\x001cdÐèµE\7·"\x0004%Z¯gÏ5øOÿôÿ¼ÿñÇq\x000bþ6ýë[
Ý½¢MÌùá\x0013r¹$PUéìôoAiê	Ï·`qEuû¦ö-\x0005Ò«+G©dUU\x0005ÉÓS 
%yqmht[nldÃ×Ñþp½\x0016ØÆ¡½ÝtÇÄ·\x001cNôü8_à\x001eÉðKz(ò\x0003·B=OÖ:GÖí;Gs/lDÒNÿ8-QåÍ\x0008ÜñûÝE];\x001678\x0016.Ë­Ê°pmÈÆÉ\x001b±\x0006|ø|\x001cïþász$eÏ-¿\x0006'.ü'ð2ý9»Á{ZM|î°¶fxúü"ç0qòì]H9að²Þ·JB¢Ú	b\	r¬âæë	¼"øþÊ~õ¾[.ô°åÁáçßS«zÖ<\x001b=©òZºr!-¹Á´Ä)e\x0006ûÔ#åMt\x0019Á\x0015Èæ\x000eW(@«ºË! \x0007µ±\x00199öÅ'Ï¿D~	K%ò\x0006ï¸-rùk\x0005ðD\x001eJ÷ß\x0018¼¬ÝÀ×µ\x000cþ¿ÿÝû>|úôV~Ê7.,&½ü7UÅ\x00041_MoÜ\µ±\B\x001aÝ<$ÝòY\y²9è`	oÍePëÆÆA-ç\x0002B%\x0006 &ö ågÂ·"×\x001eÜãLSb\x001a\x0010'íc1Ï!Ç!°´Ü²\x000b\x001có¼oüÕ\x00032Bà\x00038F®\x0011Gt\x0016\x001f+à¶øæ§üá_ônð+\x0017;}O\x0006
1£ÞÜ²~p«~ùþþñóï?ê\x0011{\x0012töôæ«³|g\x000eµb0¥ò÷XÐú-ïZ*iSï\Dot\x000bÍµB\x0019p c×¿¦\x0016Ö\x0018O\x0012üÑIvq÷àúÃ³U\x0012VBæC%Ç±D¢gÞf7Ú
\x0017Â\x00176ª»úñì\x0010c*\x0017î¯ÜÁz\x00078Êjû­{4&Ä{Á\x0018C5Ri68â\x0017qZ9éÒî\x000fÐWOuí-!Ì\x0000\x000f\x0001UÀkùtG\x0004]Rbð1ä\x001aæ\x001b¼£¤o/NE\x0005¯\x0011HgT1ð®èìmùxvÔbZ/\x0015Âw\x0015\x0017âv¬ÄDÞÑ·\x0012V[\x0011PÞã¶\x0015¿|ÿùû\x001f~z«\x001cDtàë3-Kt¯Êæ\x0013³ÿÖ*¹\x0018[ÄÒ\x001210$2Àu?&cNÚi\x0015n\x0004±RÉF4Ë\x0013,æáF\x000eì ÂP2Mü(4!wË.÷÷FÆ¼L\x0008\x0002ôÆaPg"x¼h+[\x0013"{ÈÈ(0úÑÊã&`«Ï3#L\x0006ë-Úó?8+  1e¢¤9P³(4\x0001«i)Ki\x0015sæü\qÑ\x000ep\ïHf\ã\x0016\x001byã6\q~\x0007{¡at$d7!¢Ü	¹ó^@°"q\x0016E¶º\x0019¡ý\x0010\x001e=`{Ø2\x000cPNäG¶Øûwö¼!\x0005¡ë|:¦\x001d)ug\x0017KÛøP_¾û¥Xlpñ»_}üðå¿¾\x0014ÖC0¡Ëë/J¥bRGùzÛ¿\x000f\x001bYÚl#\x0000\x000fþ\x00165x^Sj\Èh6ü°\x001aÉ\x000b: tz£"cêK2#±\x0013rDäôÎ\x0003r§V\x0003\x0015 ärà\x0010âYä\x0018¹7Æ6æðvô­¼3\x0002gbió\x0012à4·²5\x0017rù\x0005Æ\x0008ûÜ\x001fgs-¶ÚÈ\x000b\x001al¤68X´D\x0018rzf­f5\x0017lÃ\x0015?Â¶âBsªÌ\x000b¶±È\x000b¹ã\x0003å¼o\x0017Ì5îèÂÁD\x000el4àÔuOÞöÊÐÖC½\x0019ð~î
²ì¾døÚPXøÂL´>\x001b\x0006W-í7;~øQÛkÿæýé4È¦.Ç<K ¼Ù»ò¤~c\x001byHëÌ\x001fGöo17¡¿úÔô\x0005ã±3Ù\x001féM¸qÑ&ä\x0000(\x0012Mq}Tþ]Ú`\x001dÙÝ]Ü\x001b\x0019/nê  ¬\x001dÿ¨Û¬\x0001%Å¯;\x001am\x0001\x0007l»\x0011Ã+¬Øòõ½rwM\x001dýù½±Ñüú¯F#BNjåëy$sNØh'C~Ý_;mòù&þ3¯óîËõ*=¯×ë?~øþóÇïþÓß¿ÿüÛ7º]Ê;Mæ$@¥8¸Æ}\x0019ÉÚc~ã\x0004Ës û÷kf·:ý5_ÝõÃ\x000crÜéÃÈ_÷\x000f>}ü^þbù>½ÑÇ	=³ék1?þ®R\x0008@UNv¤~Y¶Å=-\Bh%5\x0003ç]|
O\x0017Òq]Ùw\x001bÎ_ÜÃ\x001b\x001ach±Q\x000e¬jáZ@siÔ\x000f\x001eÅDÝÐ¡\x00119\x0010Sén2ò\x0018D>!c¨\x001eVtû¸Õ98\x0019l ÄÎæÍ¾¡1 Õà6ò¹!ä§3v^ÑÜ\x00199sè\x001f\x0008£ó6ÒOt!SØ¨Æ\x001f£]o¡\x001e¶\x001dðN×Ñ ¶q^"#ç W{Æø\x0000rs¸|+è5q²\x001a·êë\x0011ÏlZÅ£Yå³\x000b/¢ºhÓ/\x0016	üüÔ×òz]Ò\x001béªJ¿¾G#\x0016QZjq{.l<MY,h´Q°{Jó.[_À	;0¶sT¹\x0006¥ØM\x0008ABç6çè·_¾û»\x000f?}üé»¿z3ÞL	6\x0012Ç@Öµp\x0003%½æªs½tßÊþ-	\x0008	
*ü1¹OaUç{.\x001d 72:ª\x0012cWì¼­{]9ä®mç¸¿ÑqoÔ6à/\x000f@®S¤¶{\x0004^Èè¸k,\x000cd·µQ/²îÖi[z\x001b\x001acã_úc\x0006]a^\x0017ÍGntÛ¾!¦ø´k=D¦E77mÇ¦\x0017Áû¸»[\x001f~üîïä }ü¿¼ÕH¨,ÇórÜJFC\x0010äðÏÏµ^¾ëÝÚÿ1_ÝÍIuoô~øòÓû\x001f¾üæ÷oó]b$(Kò¯QÝ¨íÜ zsµjïÏÏ«^ú
tÿ~m^è/¿&'`HÀ¿Ñ\x0000Y¬Ò|ñÅrvË=¿°+Êß\x0010ËXÏÅ1÷Z­<ßYR²>uØû@J/>C¨Ý[¥\x0006gYx¬ÛV\x001b\x001cZ9bIán´&D¤\ü\x0004^lJr3®{w\x001d	8,%G\x001fmTRÚ\x0001ÄÎ%\x000eÊõ¥74ZÏá³åJQRRòT\x0002OÉÑ÷-ºýð|PìÏ=·H)¥óVÆçÜ4Ñ¿¾(\x0013ö«þ\x0012|Ô\x0010Q¯s$æ ­f"¾³ßJ(þ_~øòá§Þ,ñiX6X±6Ó-~LPý;ðdÿVßÈQ:ÛujòÓÔ>³È\x0007\x001bÒX,Ð
MÅ\x0019=ÊÁ¸:3
ß¤¸«Î¼ #¯\x001aú°?Rò1sq5ÄmÆô\x0005\x0019:ÀDO³ë
=­Úï\x0016ÏëFÏ«<ëFª©U §\x0019³8ÚóOßü£¨D£täã:öDãxÔiõzýýûßÿôgó^OÕ[õ¤4IbTÁ+eÝp2IþWÖïø-¯¯n#÷»|¸	=®§ñõÇx\x000b«`'\x0002¦`y¢åzÝÐx½rÀ¼wÓ\x0016)N6lÐC,S¿74æÈsÃÎ|ï¸ÇT¿ß´jk^¦Únèò?öu¿z46'5n*Pã¤þíÇßüþÍ²°¹\x0004®¼4x\x0007²þ)¸ìæ\x0014}Ë*fïOy\x0007dûæ5\x0017MA¤\x000eä÷<µÁ]þ\x0005y\x0012p<Õz¤\x001amr\x0012n\x001bßÐ\x0011W\x001d¨-HSE¼j\x001eÃö£¾µÞ\x000b:áª\x001d2<íGÛ.¿û\x0002Î¼æ¹ºÈE"YóèÛ^®\x000bºà\x0013^.7\x0005É¹ð\\x001f,\x001dËÓu#×_ðYÇE×w¼\x001b?áà\x0018X\Ï\x001b¹!r']\x001fe\x00106zZ´}Â%¸¡;/ºÀ7lË²jÎw÷Á\x0018¸ñj_ÇSÇrá6\x0007v¦o9UnÛÈPÅ²iÞ\x001eÖìW\x001f>¿ÿþÍ\x0012\5
¦
ýJºFnÒ^cNb=¬Å/~Ööoùê>ì´\x000e\x001dõo,\x000e6é(åòªÁ:rwögý\x000c=¡&ú&)\x0005e\x0016:#½*?Á½\x0011\x00031l\x0012\x0007Óôh óyXÁæ¼ãÐwØéº\x00184éwMËöêOºìI¿+ÁF°cL\x0012z^wÂu»IÃËOâ`±m\x001a\x0006Èoÿ»Oï£Ý8ø×Ò¯üþË\x001bY81T<\x0003VJçT¹3ú7öØdúO(Go<ö8úö_¶Ã³ë\x001bãÔ¬X[ÚU£7\x000e»Rí\x0006NésYÑ$ÈsÛî¸Ö!T\x0017Åµ§Å§fcûÚµ+nb\x0001#\x0008N:M~$^õÔ	vîÛÄ\x0002
MÕHúßë4·m+",0\x0000£:TCL*&v×\x0006òä
MÝ×áEmoÕ¤Ê>g\x000c\x0013ÛÊPðYªèqS?qîÅ¯hiÎ\x0015ÄX&3Öò¶ðyAÏÝ×PTõÙÍ{=uD}:Ø\x000evæ\x001a\x0000«\x0016{e¾clï·íZ76\x001d?\x000eEc¡©AeSèÓ\x0003¶íZ76%õÕTOdì©|½`NÇSRÛKRÜ>e!®?S@ÒHÖÕrÚïûÝ"z>w\x000c]ùF&kôÝuD¼ìßÔ\x0011Q"©P\x0008­É,Y©ø?}ø|Æ×\x001f\x001fü^õ\x0003;0'ôßg#[¬6±I7?·hú\x000bzÃÆð0ÕecNd²\x001eþ?¡¯\x0002^Uï¢Vÿ9á¶\x0011È¼43èåÖtöÿþïÿã/ÿù\x000fÿë7¿ÿÃ¿¾Õë§kb4|ð~gøÜ:öûsl\x001eYïTÖç»ñwÑA`:Z#ÕÐ\x0007×ú	®§SÛ
\x0007{\x0013·³×{×ýÂÎ¬\x000eytþ\x000c¼ô©ÆÝ7ÆÊª1\x001f©¿\x0013ñf~ òÝÌÐ6=½\x0004ÚÚ÷3b¾î4·Ñ´¦nÇìöÊWÊT2£ùÀÝ¤\x001b\x001aS·)â¼\x0018TkChÞã!
¿x74VFrAF\x0008u21ÊÒó¤
l²XËS|C'^5\x000e®Dgy¸ê<\x0019Õ¶ëy¼¡©M\x001dy\x0003Õ¥¢\x000cash¸\x001dÁ»©äâq[Ý¹\x00065?ñ»ìÒ\x000b\x001aµÔ°çN®\x0013ÑiKÿ\x0004]¶ól\x00174\x0015sR%K\x0010úÔ¢\x0013¦°0æ@^o\x0003I\x0011ãe=¡|ílïäÓ/Q&~½¾|÷×ßÿÛïþóûÏ¿ýøV+?{ëVI¿{»¡¤UÕ¾u9v/ñ¼~ùõù
5áEÐ\x0001oØàÓä\x0017õº59ëã\x0015Ú#¡p\x0005DäëêÌ\x0016C]\x0012þ\x0005\x001d\x0011:¾XCì\x0003Lqm\x0003¢äüÖ.Å.\x0004}\x00129ùhCò#frVËP\x0016Ë\x0010*kÕ»é5\x000f¾ñ\x0015q;|vCã´êS 9j\ÁM=Qµlû¬oè«\x0018\x0017\x0008õxL\x0015¿¾\x000f/`\x000fCÎ40'Ï\x0008óø>¥Ðj?³²3=Ôññ/?òºyà\LeÚÆ76<J!=ª´W®jê~ââ
Í\x0014\x0016¹\x00176¾K?÷U?hÜe\x0010\x001cWt6|\x001b{ÞØ\x0010{ÊBèdk-¾\x001e>O¯G\x001fÖ§Câ;?*Öt¢o9=§Î¾å¢þ}c\x0007<'\x0012È\x0006:&(,nÕ+Þn\x000bdè\x000b\x001aIñ¯2[vâM?í\x001bDY'ë\x0011³|\x001a¬\x0013ú\x001cQY{³Ùu©uÈ\x000b°ÑüiiR¸¼è©-ZO&*T¾Ð©«5Hb¡ô\x0013µ|W[õÉFÑDTp\x0014ó¥©Æ³>5&\x001bu:#HQå{Ã\x000cëÇ²½ç¯u£h#Ü	»!6
Æ;Uj%èéü´àÂ¸#'<Ù:w\x0003í¹wÙO¼{r\x001am³\x0017\x000eå\x000b;Ðcã+×'\x001a»¡:ÑÈÄüý­GwíÉäÑýö|\x001dbiG÷#,u^\x0002Ló¶ú¢5»ãòk]=ÿ)Í\x0014ºgk×O!ÊìZÞU\x000eÂZÞ]Ü\x00134rt*ö%ÌQé4#î÷ãL=uæðÚÑJ¹ÎlËLpCÓ0\x0003[v\x0015¦P©ÌÐ{\x001b¦\x0019\x00022\x001a»¦V¥+_\x001cF¿óµnhfdV]óänù­GtAS×iæQ³¾bc~á«ër\x001d¾±ñ;jO3úÌe\x001aCjSkä;}GtR':uM<gnö¯sÛlÙ:D766I\x0012øÎ¦\x0018Ð\x000fÊEäM
\x0001DÔ®éàJëîSf-}¢ÿÆÆi5\x001dälñ²§aµ>üæÓ\x0001D?N\x0007Ê\x001cÆl½Ô§\x0010%ÞÜu\x0010®-~\x0012º¿ät!Çcw:ÛèÆ©,KãÒÛ´ÙÓµ\x0019¢®«\x001fwc\x0007>X/ïn¢8iS\x0015Ëµ¼õãnlì%SÑ*O\x001e\x0011]É>\x0017¬&±h½ Ó´%¨\á¸!¥Oé>?ÓµAÂo=#	Ôü!ûT3\x001câ¿\x001bã¶ø6U
Ëö{{ÔÁE¼ #ÍaFj;\x0017ÿùY:_`Á÷Ê«xCÓ\x0018fá¶ó©òÝT
In½°éC6Úmm\x000egì9\x0005º!ëôÎïòf÷á¿}~ÿFV¨ehO§Ø{Ê\x0004!íõóçÒ}[Ê=1ôv<â9#9)Å]Æì\x0005åÐ)ÝÝX@H\x0007Ï§JM3®c£\x001b\x0006>YuÄÆ>%úôü·ºk×xAc½\;Õò\x0002ç\x0015$ ò
}¤A#1AdSS\x001c7>¨üã&E´4®º
\x0007_ \x00027_+\x0012ù©½oÝÃ\x001702\x001eJiÜÞ¯íFµìÐÒ·ê6$|!¼æëlÉ\x0001U×õ
æ©åÆí|/èÎß\x0010½C\x0015)çÝ¨%ì|Ã\x001b\x0019}Ã\x0008\x00045\x00172ª¾¨Ý;ìÓñ@çPþ\x001fÍädÏ~g:¦URiµ©/¶ñï¿|þøfM°±NCG>A\x0013¬<\x001d\x001d`£@ÿ\x000e:úeÛ Ô{äYÕÑ\x0013n²hn
_Â®í\x0005¦±sZÞM]1O¾Rh;v¼\x00174\x0016\x0019µ\x0005.
c¡Mh9 74F/âdà¼2ñÓ~Ìâ¶í±l\x0000\x0006åª%FÍ µÌnG³õÆÐÅwìS*rÞÎ*7ÁêÙbÁnh\|¢ôb«È¬\x001b&è¾í¼¿¡1t\x0016ã\x0008]\x0018ÚÔÏ\x0014¥=rÀu!/#¼\x00176äy2éº#L\x000eÖ¦jWö,\x000376ÝFÜ;J`Ð\x0019ïÛI=ù\x0004\x0004^ÿå/¦óôÝ/ßÿîû·Óæ(^üú¢
ªÅþb!k\x0012p\x001aïê·Ô.Ö\x0001øG5§uç¦g%\£&÷\x0017quùT³âk7DWz÷\x0001
ær0H\x0007Uu\x0016IO'¦k6÷\x001cÃ\x001d+b agT\x0005\x0013Õn¸x}Õ#\x0018Ø\x001dõ\x0008{5·\x001aõ^c=k	CXÃq\x0008¸úE÷\x0002÷¨Æë®JÀ
.Ñ\x0002J\x00088»\x001f:T¿\x001d¿¿ÁII\x0001*S
.Ñ*²¨\x0004\x001cïø-nsØòÁ\x001bq·ì{Ms\x0005
\x001b\x0006ez2ðÃYñ	ÏJ{f1lå\x0011Cx=,Éé­¤±\x0011·¹°AÜF]×\x0008a7jüÒ¾g^øx|]	õ/pÐAÕL:HÏ¶É
ÐÔ"+¸\x0011994{ð\x0000Oª\x001cüòT\x0015\âa\x0017iå,FÒS\x001a5»ÃI\x000cÚ\x0008þÒ÷½Á%\x001eCI©@/ØC	 °\x0013bÇª\x001bÍ\x0017Ì\x000c%óÂG4\x000ebÀ¨ñ\x001c`ÇÊð:CeÝ£úZO\x001b^qÃU\x0002Î¸\x000fä\x000eè\x001d¯[\x001e\x0003\x0003?m
êj\x0003~xJíÏø¤ ÞÝ¨-¬uú\x001d¡N\x001f¼
9<'¥ÖJ!o	 Ú(¯ÅÓGÜp\x0015\x0007±ìªbQxó#1]ùÖFoK9\|ýáÁ¤ .QÝ;R@\x001c2é°5Ôm4q\x000c<¡&ÆL :­\x0002ñ¤~jä]1«\x0016EÛ\x00176.\"Òþìxéøhô9[°R}Ê\x001d×\x001f§þÊ\x0005èÂåªbiZÛèxárÌ\x0015|U\x001a¼ÀQm>ÆöJ©ëÊkbEøìX\x0011¾ö¼\x0017?¿ÁQü<è¼ísÊÕj\x0007ÛÂ7¨Vk®K«\x0016ß
\x000e:¿¡×ß«àÙ¬CJWnõUYýÂ&eõèè¬\x0014ï\x00172¤LéX_Ó\x0010~:ÙÚ¶V.(BëÄ¶\x000b|\x000e	[us
ûð\x0002eTâ.q½Áå]¦Ï9\x0011û:lV^&ÿnpü\x001bT^Y\x0007c®iÔ·¤ªü9ÇA\x0014è\x0000ñzü
F
Ü¿ãÛÉâçÕ¡eÚ»"]N°å\x001dD9Wl»1Ìç|Ú»"oeh\x0000Î³ªGÍ»âìîKØ~\x0000¯ÏkÇqçÃâyå`/'¼ O\x001e5¥\x000e\x001cJ½Ñ\x001b\x001a_ý\x0012-aW\x0016½æ\x001b\x001bõ5½ãgBe³I<Wâºñe\x0001Ëé \x0016>õÕiläOzºÅû8±5^Ó\x0017Úr­;À÷sé{æÌ÷spy-ÌR\x0017vmh³Ä<fEÙ·ÈùÑ1´\x001bj"«²âÀî\x000e±adBmVäD\x0018[â²\x0015ïÆ^ý~\x000c;Fr\x0018Þ=ÇPsR¤¾=øy16ãSN\x000b/¸ðúh\x001f\x001aÝVe­ùÄ-\x0012¦±;\x0004\x0013\x001egÍh\x0001Q\x0008yþ´-bN\x0007_î"í}£´w,D\x0015æÝt\x0012\x001b?üb¬\x0003ÀµýKa?À%zHtíJ§nùÄæ¡\x0002\x000f\x0016|úÓb?<ècí\x0005îù\x001dÊ\x0018\x001bTKcÄ\x001c\x000eý\x0000àõ%H®èNü
Zz#õ\x0003?\x0002
ï\x000f~¢ýð«|í\x0003\x001ez"Ã%×·%]ý³uÿöÛ\x000f/ðì\x001fþr]¹J1ã+WnZ7}\x000c¡cÀãM«Â®'¢É\x000eÜÂ Fþí`^ì\x0007<?Ãº/©`Ö5Â_Ô
IÉÐV
½\x000b\x001cÄ\x0013s¯èdñÄÊt¾Òô\x0003}ÿ^Ø\x000f/tU?n\x0000îù\x001e5æVð¡pppçì\x0007\x0000oè\x00061éØo(èÑk\x001f4kÇÁ\x000e\x001d\x0007A©\x0008ÁçÒâ%9µq|\x001bÓ¥Îp·<Å[En)h?hwm¤µó-\x0017%B<¯æ«HÀ\x0005QhÐü\x0005~Ó1Ú\x000fèe,=­ÂÐ\x0003=AéBEj_ý£º1*«Ö\x0018×\x001e\x0006ueZû<otÜ\x0018`Q²m4\x0013\x0014¸a×ÇØG£ûÚ¢Câ[`ßáÊ\x0013ºU5©òÊÃH\x0016\x0006¦6\x0007G]ûÑ°\x001b8ªº$b\x00012\x001fü.ûá\x0001\x000f\x000eò!J-E/F$\x001a\x001d*\x0002qXxÆ<kU¼çÅÐ¢Nm¸rÇQÈCU6\x000ezÆ^Ãã\x0019I\x0000Ì©ç8#Ô\x0018-(¯#hxé\ü\x0016?Cî¿D¥yv¼à+\x0003\x000e.ÝQ*T"2Þ\x0014Æ·Ó¦4Ü\x0014	Ïá
iJ\x001c¯ÙèJ$:¨Hûáê\x000f¤xñÕÂµ\x0018®½\x0003¼xÜ4\x0006ÁoôZ9mÑyð\\x001bzøËé©+øÔUñù}{Ð5)B»îxc\»ÑOkÇ×¨ÖFèê¶ÓéÔ^-èÖ% \x0007C\x0000ô\x0008Å¦9h¬ªQ`t\x000b1$æ=¬½úé<ÖMo­eJ\x0001DÈ ô2*\x0016íd¼\x001a\x001a¯î\x0002^­êt\x0007ûDKwroÇ(Íé£vü¨r¾Á¤·R<\x001b\x0018í\x0013Bô6²Ð~íð4pûá\x0001ýÅÚ)àÙ\x0007ªÃ@ý)Ni,¾ó6ôrÞ²\x0015\x0010}µØyÌXsx\x0004ÈrÅá\x0010Ú\x000f\x000fxO^lJ®\x00069\x0004»õ\x0000¸\x000ec\x000cô\x0008Ã\x0018b \x0002¸¤M%^(¸s\x0012ÜÙÚã!=b?<èrº\x0001=¥B9]q¨!Sg.¬¨xÊ\x0018\x0007Ê\x0018÷æç®©U¥¥{ê3p\x0012ÂÒÂFÂØÀÓ#a,K¯H`ÝtD
kæv%è\x001cv)îºýð`\x0017\x0007ÒXMÇö°½[3\x0001´rív4ô~Bï.\x0007æy6Î\x001c#\x0015jjëN¼F;ë¹ìmýð ë\x0010êcÙ]\x000c\x0003ö¨Ñ\x001f¡g\x000cý;¬½ÐÚkÈ±©H,2ÜÄÈöË\x0005kªÓ·l\x000f^¡©4jQô±0\x001a²P·JÛÒi¼Z<äóìM¯ýð G¼§\x0003}:ë\x000c>:¦ÛÁ8Ú\x000fpM\x001bpµ×î¸ýR7L¯¸\x0002é×wª×wÈN£MrFÓkêÀ"kÌX½êÆþ¸ã¿¡ELþ7ÔSÔ`s\x0013lÑsék\x000cñÉí9ý\x0013ú\x001b3 »ØÞ½Ô\x000eD_
Ä¢í4j#¶Ç=­%?|ùüãßýðåÓ[58Ï*SÉ§ø¢ùpVýyu\x000e©­~~\x000cèk-+¦§¥\x00040
ÔÔrQ\x0000yÓ\x0004\x001a\x001eâ¼UÈóê\x000cð\x000c¾³xóÕ¿â%'¦\x0005¹\x001a\x001ck\x001br¡iÕ7tûáù\x0010Ñ\x0001ºòjQ\x0011Ái_\x0015.=\x000f\x0018_\x0017	\x000b½f@7Gi2ñwZ\x0010!ôRÇüI[\x000bqn?<;£Âf½òíú;èÎÅ\Fµ_ç[\x000cÝ~xÐ\x0013vrÉÍÄk¯u\x001e´{ÚØÕ7\x000c\x0017uwÝþú³¾ÉEsâ»R;M)½Nfê\x001d\x0007çc\x001aÓß²«¾!\x0000ë8ýÐÇ¯Ã\x001aZ\x0011¯\x001f)Ñ4§	÷Ll.Ó\x0017ÄÜë8ý]\x0000[5ðÄA!Ï÷4\x001eÇ\úÚ\x0016qaC[KÚdñ`«ø	2 jIMKÙøÂ­ü\x0005\x0006î¡ßUÐ
ª¢k\x0015\x0003ý\x0016Í\x0003g>\x001f#\x000f°\x0019Ö\x001fàx	¢6¡\x0001¸êc#öÄ_ý\x0018×Kë öÀN
°ý+9jën\x0014[¨t<5Då+Á¸zÐ\x00176xÐ*w³â»S\x001b¦ÛÍâF¸¸×Üà\x0015ÁA\x0000ÖÀ=åÒUaVfKcÑ\x000c`C®½ÑÈ7¤"<ÀØ.\x000f6\x0000¿è76\x001e\x0015ORÙ1sÆXíCdðñ¬e\x001b\x001c\x000e¹\x0016é=­\x001b+R:)ç'ì°ï\x0012\x001bØØ%&ËÈØx­Z6Å1'<qâ°ð\x0000ý\x0002Nj#=¾QjêÃ9\sô\x00176äè1R4Âô\x0000ÖyáW¸u\x0002O\x0008.\x0001\x0010Þ|\x001d§!ðÈ\x001cbV,bÉ¯?<àøOoBÇ\x0007|"¼È~$\x0016êÊ¦1Àk@p"ÂK±Õ-'c\x0007¿MÜP%\x0018x\x0014ºÓF1¼­blîzc¢\x001cË\x0018:<Ø¬\x0008\x001dïNÉ#"Ø¬2CçÉf¥}0+\x0011*r:rvi²¥\x0010xc
^qolSÖrÎ\x0005\x000eå\x001cã\x001a\x001b®éI\x0000g\x0012ÞáÚrqãÊkÆ\x001bTÆÀ\x000b7½ç<ÚçÒiå	W®\x000fÚ³-&ZRiÏYa#\x000ffâx:å\x0011O¹6,\x000e²\x0016;\x001eÄ6V¨\x0000\x000ebÆ2²ÿØ\x001c=^¡æ§©Ýný\x0005\x000cÔ
{.\x0006\x0016\x0008SpXru6â£(¾µùBG(Bö_ßiTH!¢ïë,YÇ÷s5ä¿À!ä\x001f3¯pZ"UEt[xà8_Í§'.â\x0013çãÓvaérÏ6Qbd>çC2¹ÃiI\x000eOKp¯|\x0003OÓ\x0007u< »ÝÐMîì\x0002Üs­ Å|>tY\¯ÅÏ+·6ÑÓ%Jxt\x0000æEu[ÀI\x0014ðÈä.yH¤Ó;ð\x001d\x0012g
i.\x0004¬ùWp6æ#ñÚáë\x000f\x000f¶rhvÂ¦Û_ÝtAÇ¦¬9¹\x000b»ã\x0007d\x0014I\x0015kpSJcqïâF[áBËÀ³Ç{\x000f<|JÒ0% ÿ
:*%Î¿
aÔÀ\x0006¢\x0001\x001dY\x0016Å]Êm\x001d§"ãCáTS\x000c°\x0003öýéº9\x000c\x001aêyMS^Ð\x0011¡uþÙ\x0013­Ud¼>¥Oû\x0007ýçZª¸ÀR
ÈØ$ê
î&%`Ám6üüø+Îkö\x0016¿Vùõ¢RìÞçµ\x0003åÂn\x00136\x0004Ú\x000cÉ»\x0012¥tkåÊýtRz\x0004pù~
\x0017Þ&ðÀ#è¥X¥µ"ÏòDÖÎÁaÖAà9\x0004\x0004BïOÙÐ	\x000eð§WÁ²´@¦Ã´+òyø¬TËÆW^<äëúe[ïCÞ;»¹qUUÊÉ\x001aàÞ#
Uâ9äîRGè:ås!Wø­»W
Á\x001b
\x000b
tHÓX6­¢ êàþ´Lc¢9eö>Sc¥Ò­â_7ü\x0003üTp
j%\x0010a¿9±;¡Ó~}2X5À)\x0014G\x0007ßMq¹±óÄiç%Ân'¥.gÅËÙÄÒ¶\x0008æ0!fv;ß8È¡NrO°rq	Qëä\x0007Éÿ\x0001\x0007*ÉjBý£èO"ÈÛÕq\x000e5jû)bótÆ\x0012º)\x0012Õ\x001d°;¬[þWÏx*\x001f
r\x001eû1ò»&£oàv8Olê\x001eø)%VãÇ>ÖÑwzðÞì\x0007Ý'Ì7µt\x000bNÞÉM)#³â\x000eÏ½\x0007¦¥ /À;Èð¥j³~ÏÊy¸/\x000f=\x0005·6(]Ð\x0011«\x000b\x0008é5\x0007ÑMñmJÂèJçX\x000fèÉã®\x0004#ý>ó¶Lrõ\x0011ï£eûáÁv\x0019	\x0004bì`ùâÙ_\x001e\x0014Þ\x001dî¦ýðB\x0017\x001f\x0015µêÖO)¾Ú¯6âÃ¦{\x0007~H-énà\x001bZÎ\x0001\x001e\x0000<K\x0004\x0004Aªx|Ü\éS¼ë!°\x001f¥·´ó:í^ðuSÂ\x001eöõ¯ñöuJáFï¸ö\x0004 Úíð¼¸Ùi\x000eÑrþ`\x0012í\x0007]\x0003OX{¢¾PAq\x00024(óÊ	½\x0000ºQæB Ò0íZu~r\x0006ûñfLö\x0002¯pØÕý\x0001r\x001bÕx\x000eüQ'¯<¹qdNÝÓaw\x001d9ùô\x001bg<ìâÄð+7ä\x0004äôQ\x001b~Ôä/F·=ÑioË¶\x0006îu4l Ã\x0018®Þ%	9%\x0005£\x0013\x0013¦©Ã:	hcl;0®¨k\x0001åQ×äýç¹Ê£a\x001d$¼Ð\x000b¼HÖOÛîØ:\x0013ÖyÛÃ\x0000?ìz(°ëÊ\x0013£\x001coè\x0015ÉËÙg\x001f7Þó	
-ÏôMÅ \x0011xdNu\x0001\x001f$@\x001b¦e\x0003\x0001lLl\x000eItu\x0008mLkÓi\x001cÌVÚi}\x0000/ðPÇÒI\\x000f'íK«ìtÕkt&öÃ¾è\x000f\x000fºÚ\x0014Z´Ð§\x0003Sã0i%s\x001cèÉÃq4R§ç9-bqðQj-°ñ­£[ÎÍ\x001e\\x0000ûå_
W\x0000íñ¬k;\x0003üd\x001c\x000b\x0019Ç8È¡ÁÕ­¬#³g<Æ	ê-ÚÐk}	Û)q­¢K?å,FxÝðE\x000fôè\x0010ÿ¤ü\x0007´öà§\x001cñµöÓZñA
ª·\x000b)¨HÖ¦\x001fqJ¤\x0001~0\x0002\x0015ßÓ(>\x0012Hq)z£GgæÅô^K_Ç/ôK×sô4*\x0019\x0001@x_F\x001e×·Cn?À!\x001db\x001d1¤Ñ\x0019_B·§º\x001dÒ9ö\x0003`;_B']KÅfÞµÔ­Òâû!sa?ÀE¢²v(\x001cÓV\x001aGÒr\x0019l_ú!Úµ\x001fà¼8¬néált\x001a'¡§4\x001eÓÍÌâ
\x0011<½úÌ\x0014<pXÀ¹J¢å.äÔÐ+¢ë\x001b\x0014	=É¶Lw'ôÉôv4½Jk\x0001i\x0000å4§·ºx¦¢JÑnRpë¨¨¡\x0007 +\x0013ôêÐ«\x000eÊ\x0003F\x001fÕ³Ô<V\x000eu«DáîÁö*7\x000cÔÎÕÌhÀ²þW?±ÛP\èp µ)\x0017\$½YØ(ÕÒÄç®_wpïì\x0007=D¤D\x000bZ[\x0005=N_5\x000f®ÞÃg?<àªâ\x0004GFÓ1ÀÙI#®V"\x0003z¶\x001c\x001b°xÀUå	­c8\x0012Ó +9yì\x0001=öÖ\x000bqui¸ÇÇÒ¸(\x0012\x0007óm<$éí\x0007=g¢wä9\x0014AOì¥0Ô¿â!\x0017h?<èúÂa-dALU¤¢k£±`o\x0006ì\x0017ºWâD×+n»~!zèõêã>\x001cGýáAwå5jèÒ¯mf'2¾\x0003zv>æ\x0008`ídÛåÉùKG\x001f÷FãÁÐË3V NIîèøjE°PØÔÐ!gÈö½¬\x0017zÆ\x0006·J¢:dP\x0010¼s¶>æÒ¯\x0000u§ópÇ¨ØE¬q*1`«Ò\x0000åK]é\x001c\x0018DóÄdOÿ~\x0000êTÖ={Í\x0002Yöc´í«vr<®ÉñßßøïèµPô¤l\x0018rÓSæí\x0014É?vü7ä7þ7$VÄ;l¹|Ê-'.UZ6lÍ¡íz@ÿþýÇïú³ÿüáý÷ß[ä[úÉMÁo'ûþR9Sî2¸\x0017>â¿­>F`Gê7}\x001cÝ¿TiÁ^$\x001fÚ"\x001f\x0006	nu ZK´äßÒYqcCg¬)cª¥öI´©°»ß\x0006´_è.lÏ2Û\x001d¤~µÁ+ûã-Ç[h-/l¢µÀ\x0016ªZM'\x0015$~">mýj\x0004=-\x001c¹í5ë\x000c\x0004¥-Tð÷<R\x001dZ\x001dÃ}ËDÒ\x000b\x001by+¥\x0014¦U'¢VÍ¦®}2\x00178öÉx\x001dð\x000e¼Ú&Y²\x000b¯<X|äÓ\x0005Ç³
¡Î|_zÈj3¾³¼\x0014ä.ì°¥;Ll5"·V\x000eö[vÆÀ³PÜßàHq_]C©\x0002ñ/YzR\x000e=ùÊòª\x001awÐ2­ý\x0002³RZ\x0002q¼\x0013kîÉÊù\x0006usWF¥\x001b\x001c\x0018"	\x001bB$>f	»æªM]ë¸-ßàÀ)ýÜCdÏËî\x0017ÿÎ"Nr!\x0017\x0014'ÿs\x000cÛºg6å\x0010z²l\é'ìØ\x0012äC	§WOíå\x001atzÖÊÂ§í®´Ý±\x0001\x001b¼N\x0010ojüÑ]¥Ûeäî\x0006;\x0001¯ \x000fáµ\x0008¿Å1¸,^Áé\x001b\x001c¦CdW:(	{\x001d"IØV¨&\x0017]j9è°òz0:¨
à\x001aQ\x0011=±V\x0013\x0011<\x000cþ~ZyÇË]¢³7KTÅ¼ïx©\x001döeêö\x0005\x000eôØÍ{pÿ¼fý"\x001eÝ´ò0ªÎØaÐA±ì§	¢!)¦Ä@4¢\x0016/IÌMu {R³QrÐ§&ço¥\x0007½ÒüzÔÎAC_\x0008nt lR¾HHNxeXÂ©Û \x001e(oL\x001fjMîðMí\x0007½bW²\x0010Ð¶\x0007\x0017\x001a¯½9l»Çù\x0012ß\x0003Î>\x0007Þsæ6jcy\x0015+ãÿ\x0000÷Èø¯\x0014»ÏS1ä!p°Qì+íK\x001cô^~¥Ü½Ñ¡wP/
\x000cj(Ï9æÊté\x0012q$âÖ¢Ù
\x000eä>¾Ç\x0006o¿8_3Í1KÚÉa\x001cdÁë¤Æ\x000b\x001d7&÷§äïµü³ÎA§H	|\x0011Âá¹°\x001f\x0000»Â+çµÑ¨\x001a<ü\x0005{¤áÂ2Ôs£rS¯
¦òTªhÛ}çØF	7¤½7g?\x0000zyû)ºj~ÐÒ¹\x001fçf°	çÈ~xÀ»{\x001c.*ø¶)\x001eÉ_\x0005³Ó#/\x0001´-½9\x0015Þ\x0013¸mK<xçöÃ.gÑÁÒcÚ ¥k$ô\x0018..¨Ã¦Gâ8×y§\x0000è´ÏTïº2z¾ª}{\x0014A4+8ulaíÚÇ;£õ\x0014B>ÐOk\x000f¸vùï<e\x0004C'?EÐÇ¾/\x0015Ü\x001b\x001d©`å\x0017H\x0013ø¬\x001dþD0]i6!¦«è\x001fOf=V¢#Ç6+¥Ùcª)MÔ\x0011úhXJKÍì\x0002OH{zØ¿\x0016í\x001bø2}w'dõVR¿Ç|\x0015ñpx6Dn;¹
Î¶tº§	yO\x001d\x0010A+z,oh\x0013zk©#Üè\x001dé±×iáD'âÝ÷&±\x000b:Cð\x0011Ä\x0002ÄTUæ%êýbwof¢ÃYÌ\x0008\x0012:Ó5S¯ç	¹8\x000664=A#µ2BBDì\x0001Æ\x00003\x0019¬\qEó±}¡#\x0013´«0\x000fbè(U¤õ±\x001dxYû.ð\x0014ðÁg¨N\x0018¸Ã=Oóça\x0019ËÒku£\x0007Ú'±É±'Ò³ycêU½-KoÞäa:\x000f\x0006q­6'{ugì£¥óF¯¸íÊ\x0017\x0000=1sxêaB÷WYûpG+ª\x001e¡6,\x0011jaÞV¹8üUÓ~HØ\x000f/tMêÐYÏ^Xü,2¬z=YõV\x0013Ì¶v\x000c$ îR\x001a=Eõ´ïµ\x0012ù±'tíúEëUxBIsücgúigzcôgþI \x0012ç.	Ðý5â{ºM
oNlJûNÚ\x0001â}ùißí6µe\x0002ÿFË\x0015RÑåÕ ûXrgôÜGÑ¿\x001dok`|cï ¼¨R\x001eD¹\x0010ªO´D \x0004\x0011}ï ³\x001at¢
¶vSWK!ÿ®ºÑÒO&²£Ì9#\x0019ªd\x00173µ£Æ U	-x@y¨ Oÿ39#^î\x0014\x000etÇÎcÍWñyé·ºÑH0_Þâ\x000b½³óØSÐÇÚýÂy¡{G\x000c«Ø¾,\x001bÃ\x0003íÚ\xcÜ¨\x000f/\x0003¹/tø¨%!¥N¿ÄüI:2ÝÜ;1òûýð ×Ç½3õl\x0014ï¼ê\x0016Æµ_fOoðlÍA¯|Â°8\x0007Ö-ä«¸}Úö4¥ÊòÇ®º}H"æ¸t\x0015³É°¶.^è\x0001\x0019ÊJ~\x0018¢£\x001eV¾©ÑM\x001eA\x001b;ñ*÷VÆ~x¡ËÝêNPÁûîYm9i«\x000b=!ÏzÍ\x001d^&ò³Ræq4Óã.N\x000b\x0015òTÈE	\x001fÊ\x001b§^$´rZ#ck×Ú\x000f¯jÀì\x000c¦cU\x0005»ç
qì\x0017YÁ:ûw¡ãì¡?±*ã¡^FÈÄÖãJ\x001dá#f?\x0000x\x0000\x000fU\x0005ÛÞZ3AÀqëðâ\x001e¼`Z±pn"\x001aèýªê
\x001bÉ\x000f\x000e\x0014Á8XßÒ\x0016µBÑNÕÎbQ\x001cØ@ày|Ñ\x0007\x0019Èð\x0013\x0012AiP\x0004úEÓ¥¾¬9¡-xDµÎ S)ÏkPÍDÖ\x0007ÝR\x001e\x001d£º\x0003z@ôÇÑðwd¼\x001a¥S
Æô\x0017×\x001b9\x0012\x000b²\x0003'FI¼Ñ1ÏB¿Óx\x0016Vâì\x000b³¶#¼\x001c\x0001uÁH\x0016J\x001cS\x0002øÑ6e\x001dú¿ÁQ×&«\x0006Üc\x0019A³Ñý\x000fÄ±j1\x001e¡OèÐS\x00002¨\x0012ã¤­Ö+¥îR¿\x0018\Ä\x000c­]\x000fOº7|#Wu\x0019Y¶OÏ^È®]ÏÞé\x001fÑß/O[]\x001eizKÕémå÷Éã¦Eä©pò\x001f¢\x0003vPA­Ô­¥Bîïê®´µ{#nµ\x0018G÷Æß½ÿòéZ7Ä¶2½ñMAªù®ðéhl-æ*|SYY£Zz7\x0016¯*^Xi)OïjzÈí&­æiZN¾S\x0019v±Ì\x001efÎo»a*'(Þ Dh{¤»w#c©B¬g\x0000îXZ	\x0004\x0018|\x0008-¤\x0018\x00178b\x0004îÃ\x001eåSÈé\x001dó\x001bgoÁxZ#ý\x00010Òw\x0017\x0003þ}|ºcRy7	nªa:mw¢íV'öá	\x0017ËÍþ\x0010vJc¦ÿ°ãhíÄ%p¯B¨·À\x0002Äsæ²p}\x001bÛBþpa7 ðª\x0006Øb\x001f(/ì«#?Í§6ú¨][<Øxi@\x0011DIåqåò\x000eô»¼Ä|Ûµ:´\x0007(í6=_>È\x0015þQõ¬ÿæÏÅþ¼
 WYöIÇ9¾ÚÆÄêF£Äyõ$:ó¿¡éÑ^èéY¸e÷~=ËNëü\x0003jCwªÙ\x0002íÄð\x0013\x000eî\x001b:!´#åî)ã­ÜÇLöãóÕõéÿöÃßýÏ¿y#RV±#<z Å×\x0010¸\x000fK³ÕîÛ²ÊÔþx îÚÔ h\x0005ö_º\x0012» ;ñç\x0018"´ë!ZµËå>c¶\x0000£ªjô1ô0yKW÷
\x001d\x0011:`ë¡°ú\x0003UØoª
L¯çsE\x000f\x001dÙ\x0016\x0005ÊZÙ`ähá×Ò´ìVUt{NP»¼ä5&Áu«²/ÝÿnE×\x00145Ð/è}uü\x0015Iø# c\x0019Eq«*zhÏc\x001e{¥\x000euÚi³\x0004ËX[UÑõ#:ü\x0019¹\x0000ì#ÉÈèÑ[zÛÝª®<-Ö\x0014z\x000få¨ñíöCÚbilw«(º~E«ö¬@?Ñ70R¯§»þj¸ÁWt-¼£óáû´êQ9ÝE\x001fø3\x0002#¬Ó!\x000bþyzÙFéø\x0004wQû\x0018\x0000Zì{£Íö<-~ë«.£ÇËØ\x0012R\x0017ècA\x001d^²ÎÎ[rÕ0OØ×

JÉOº²nê½×\x0016\x001c+I°ñ>Ê§\x0003Ó'!\x0015qQ«¤21bµòÜØx#/rè\x001b[£\x0011ÛO-©ªn¥\x00136^ÉæÌRO ç#X·Gðt'±+M)>ñt§È×ÝsN\x0015ÊGnþ:ú"78\x0004\x000fæ6 -Ó\x000cñ	\x001a/e¡±-\x0017;Õ\x0016\x001fICxû·rÐ\x0004¿\x001dHÅF\x0019¶­nPn%ö¡\]Iµ	R e\x0017>%ehcneÀ[	
6vs\x001a1)k«[ãc·rUÝ¸±ñVæ=Ñ.t\x0012ÖÎ²Äë\x001e3O§[\x0019ðVi*pº/5\x0008X7sòh©A±O7'àÍ)
ç\îTàVU©	{¤³N§;:¾ñèoæ©O\äùÆ[2{ipaã\x0011,ØÍ©ô\x0007¤\x0016®}®|¼\x0015(V\x001e»\x001b\x001bÏI	PÐw\x000cÍ´ª.ý/;\x0016ò\x001bºð­D_Jy\x001a3aóhØ­b9\x00136~ÊÜpdÐÅ©9×7\x001e\x0019Ô©\x001au.O2á§Ì²a\x0007d\x000bVlÓôc,.>eÂOáÃÃdÞç\x0019{Tãwâ\x001d¯÷\x0013ªtî\x0013½¨º­\x0019\x0012Þ\x001eò\x001a¼i)xûó÷?üÍûß¾®\x001e/¾qY\x0014\x001cû\x0000WÊo\x001dÂå\òFWcÕñk\x000c×Ð`ºÉ\x001fõL.¨"´»\x0000îÆ
ìÅ`¨\x001eâ;r¾&þYAË.~»'\x0011x\x0005tÑtTu,¡Ë6Êº¡3\x001bùÈÐ(O·\x000b´ßÅB74z^Z\x0010\x0005\x001bïYùH.ØôîeóêV%+¿\x0006,rw\x0003®au¨M|¹H\x000eØ\x0014V¤4\x000bú\x0019ÉäÔÉï*n\x0010\x001f \x0003î*åáá+$µ£>ôäe\x0018-ÚF¬É¯¯>v\x0006dsùv§4xv2A÷LÆ,E
.äsÒ×,<»-PëÌª\x001bÆlÙwÞ÷Ë÷ÿøùýÇÏoyhÞQò\x0013&pt¿­r\x0012.ïJ\x001eËgI%Ëª\x001bÈ#Æ/ù=Î1YÜ\x001a³´\x00183m9ùF¡"!³lêTÕ­5K5Shôý´\x000c\x001e\x0019­Y¯mº¡á\x0012äè(Bh2ýÞÛ²5i1Y=\x000fLc4Îð*ÃëÞ%£nèÂkÆØ×qÌ.k.Ónô­\x0001N\x0001Î1bxê}f+)¿OÉ\x0017ëªÛH	.\x00068Gª½¶£Ðª#³£jûô6etacÊHi\x000c)ªn\x0008óÃY\x000c7\x000eN7\x0006»Ò\x000c³ªBR¼ÛK¦¾úmÒèÆÆ+Þõ©¬'ý\x0016yµÃ6³scÓÁ&z\x001e5[õk_ÒÇ¼MìÜÐt´;
!øÈrWºlNH¥¶\x001b»ð²)ÑÚHLX¯ÓµÙ'_nìÆG°òéî¼'snh\x001f &HrBàFÓ@^Õ7¦Dë>q\x0003Og\x0004âuñ\x00088~Ì\x0013{ËØê­ßõ\x001að#A÷Ð,`¦æ?µ­ìaôQøÊ¿\x0010æ¡#f3\x001c¿9ì\x00064»@õ+ÿ@þ1VÕíg#\x001eËºý«\x001e¡=\x000bàhüòÓ\x000f?ª·ñ7ï¿¼2³²x½þtÕ¹^\x001eY43ö-=\x001aÜ\x00123ÉÞÍFê¨Â¤"¸
UªüM|2Ó¶jù]È\x0001\x001drì)4
kË6Æ	Úï¼\x001b\x001a¦~\x0001$\x0004òzt´¡\x0007%ÍbØnh0l©TÊ\x0003¹E!MÅ:ÑÜÕynèÐ¨0¬ÿÃ\x001c
)Né«Ai¸¼Ú7tGh"\x001bÓ H+$(`1æº}ý.l|ýNb\x0004Xö\x0014X§éÕÖ u[3¹±#b××\x00191I©ª"ó`ë©Ù>Q76~É\Þ!4II\x001a4»fëûªô8»cä»\x0015Í '÷+>AªFüéÃçã¦üZü?Þ\x001d¯ÓýO46ÇÿÖ¿âü/ÌoVÒ{¼¦mr°&\x00030bùó.É?À»T\x001e?Øfýr£RÜ¼(s×Ì\x0015ºÊ;òv\x001d3\-æÖA'\x0008hnè\x0010WøÆm\x0014®÷?hIwn~Ol$ç©\x0006ÖlQÆ"®T^\x0014y'd´C®¢úØ°wD4\x0015D´\x0013z\x0017·ÞÈÈUÔ\x0013foê
qRaÛä\x0013×&\x001fS6+L\x000fUuèh\x0017¸ÞÐH¤õwàô¦ eÑaÚ²\x0003Ë\x0012¸Ú7ÄUç_©²/«óF»ÈõÈUå\x0002á_¼H\x000e¥bNÓñhûçµ,m\x0014±gþ[èfvÆ\x0018ê6(¾¡;®\x0002× Ät¨3ó6Å\x0011¬AñA±ê¯Bcî\x0008\x0015ÌbáH*\x001a)nl¼µb\x000eX\x0002SÃ÷1É,
ÉÔÓuD·@,\x001aVptOø\x0014?\x001d\x0012ËÉlÜ²´RÄ\x001cÈh^Îö¤H\x0010cß·RÜØØw×``Ûã6òO3\x0013¹*Îo\x0003î\x001b\x001a¯d"ÍD]6å¿dwyÙi`î$z3*?â`»\x0003	\x001dèº,&¡µâÆÆK\x0002æíÄ7Ó¥tÓ}O~\x001bËßÐx)¹\x0001D3²ì8}ÉAsºØH¡ËF\x000b\x0018¦mÔõÆ²7ZÞeI\x0013Df
\x0011õ)õÞÔi³G°}º7ZJ#ø\x0004\x0015 dN%ÅhÔk;Â'[IXy?¨±$FN8^L*kËÀÇ¯d¬ËP9!\x001d§4©8<aÛ2pcã\x0019)nf¨f+\x0015æe·mÇÀ\x0005\x001d\x0003¦XÜùÐL:;r#ã¶càÆÆ\x000fqè{\x0010<Ó!ñ¸x4¢Àµæscã§LÔmh e§mÇÀ
]øÖ ·\x0019=Wõu\x0014± mí\x0018¸±ñKÆô§MQüïøÞ$!];\x0006.lì\x00181aóò½Ó)Qeé¶÷S!ìõTr¼¢ªß±Ò\x0017¥\x0004\x0015\x000fè\x0019_ÇÄTÎÑÄïþâßüôáËçïþüãQ·j\x0007\x0005gA[ÂU¼RÊ£®×à[¦¨TæàO\x0008)ÒZÖ¾1V^ì*Ì\x000cÊ>l\x000bûi-ìËY\x0007þ\x0000%æ&ç<µO÷´)ÒZÙWh«NSÓwæ<RôV\x0011^%¸.ìD½ê$¬Ê¾Üê¸é'TËö,4?/l¼Â4\x001au`°}íÔ¼ilIu\x0013Qÿïÿþ?þòÿð¿~óû?üë[EÕu*2ôöÀ%çQÄ«|Û7îl)N\x000bÔü
Ôõ
Ô@Ó	½p¿Q8óÇhþ	¼\x0011R\óäÍ\x001fÈÏËþ\x0006Ôõ\x0006Ô¼á¾ÉÓáÆËè,½´¼72¾
\x0005­Ö&§²ðÐÊpá\x0017\x000fþFF\x000f¾¡r.gr2·B_DóË³{#c6RU>a,ª
\x000e3H_ÉÔ\x0018ýßâ¾ßÐ\x0014S\x0017lÇQýóÊ!Í¼ÓæS®Ö .1uW\x00168Ó½ª\x0012S\x001aÒqþ"4¼\¼÷\x001b\x001a½÷N9|ÏQXÉì;¹A:sº+\x0018ô*±bJ\Êâ\x0005÷étÔm¤tcÃV'¥â¡ÛBOQì}z.vÆq\x001eÙú+19:÷Ý¯>~øøéÓ[å\x001cÅHðg7Ñaè³\x0002G-\x000f\x0006àoi\x001cSIÑ­ÕÐì "þ-Ú{E=tÓC+\x000fÃ6763.DôÔ!äñØ&3Ämô6c\x0000uÂvSóxÈSD÷1fÚõÓ\x0017ÒÌ\x0014#ØÓ²\x0007ôj\x00116ýÝ9`³Ò\x0001SCëÎ-¥´êf]Ø\x0011ý\x001amsâ°»s\x0017]¶Ä¦ÙÊé\x0014<$Ú×RèS\x0012\x0001³¯s?äxÚiO\x001aîÏ\x0014ÀY Îk%#$ì\x001e7v¡¸É.üõ{¹\x0006?ýôþÍ\x0002\x0006GGæËÇö¨[èòèõþwPm[¼¥ Å¢mh<õVYE68{jWQ'·ºK\x001aC_^O­aVöàûvóFFo)ÐØ´.:L\x0006qË¶wîFwI{Q°íª\x0013Ã\x0011ñª­\x0013xÕq«¿ä;úx:óFÍ\x0012\x001eL])C\x0018ý\x0004]xCpH¥MóöªâÈ\x001bbyñUVÌ­\x000e\x0012¸@gÞL#\x001fÊ<£vþÒÑS qdýdÀJÖ\wÞÒ
ÞÔ§\x000b;5\x0012Mã)e?ÉyaS\x0005ÂSÚCMù|\x0014n1V³­3vcSìþÐ=Ø|Jã
É\¤òu\x0015n\x000c\x0015	\¥&4ÍÿÔ&ì´/\x0012ÜØxe|ÅºöBQF<LÅ5?ô¬6|n­\x0012Ð\x0014]\x0006GÒÔxT\x0006ÉéÆPÀ'leÕ±.ê\x0014Ï}º£%ïtc¨BàHW§Ñ¦¹ê©W \x000c\x001a¡Ó¡\x0012§W_Õ½¥_öÔÜú6aS\x001e_;à;æÄÕçfg«d®NÖMÉ£NmóêCóº9%î[\x0008ÛTþçï\x0012$}í:ïÉ<ÖÕÃ6cã1q\x0005¸!Çü)À:Aç}&ÿ¦äQ¤Þò8M^M¬âmyëp²\x0001- d¼ôÚPõ+¤©§4ÅéPÀ9 ù´Q´C£:_òÞ£½±)S×°Då´÷äçéSk-Xë\x000f76ÑJ\x0010×³p^4²8¦Ï&ã²\x0010\x0000½°)¤J<s\x0013\x001f\x0001»"×$;´ÛnOv©702
ºñ O\x0007åÔ{ôòÿ¦áßä\x0003Æ­fÝ}f¦±^±¢ßÖñþs\x000eÃ\x001bË_Ü*ï]ÿBÿÿ¿_a
*æjÄ\x001dT¨o.X¿ûÃ¿¾U¾AÛõiAN£ÌW$Ý^î­vj\x0015oÝ*ß´gÖ\x001aøbµE~Ý;?Y¹è®~\x001a³§v£~Ñ\x0010c£6l-3ÇîÓØßÏÂßÐx«\x001b\x0012ªçJ\x001dTan!O£ö¼:5\x0017tfhÈ#kO4\x0013&©#7mGëÊf´®\x0017¤²Ó6Eö|çNÈÁé²ySüæM©Ø"*/ø9"ïÀõÁ¥yúbÐ@]³%ð¬x¼!röÖÙ/ÖÙ¬guÏQhbËïÆüþBØýÂÎ¼%\x0011.ªp¹¶Ä±«ûYõ\x001bÈ@P\x0015D?Åd0ÃD4\x0012û¾:|aó<y~ÈØv\x0017ÎÜû:ÝHw'¿±\x0003ow\x0013\x0018\x0013÷Ì\x000e«Fs»Ðá½°\x000b;\x0008
¶ÛM\x001aJºOØÙN÷ZÊ+»R{Õ\x0005\x000c;\x0011£¾¾ |¼óØîÝ\x0003uïøô@É6ãÎHäHc¯g®´qa}¢jØ\x0017\x000bÿ£ZóOú~õYñÄ¸ÚÕ\x000cÕ1´óÊî8kúw0Ø!ÿgË`váV"\x001d\x000b¹\35XÞ%ÁndlÄUY5f®ãé\x000b7å\x000büpjOÐ8\x000fH¬Q'\x0004)ü@1F%¤º¡±\x0015W¯m§K	¶äúr2vY°\x001b:ãª3'Ø~è¤ç ^-Ä.\x000bvCcÙP<ã\x001b2é\x00065rwn;DzCc-Kµ\x0018p>5sÙ0ñn¸Èå¹¡±l<Q3Í¼ci¡O²
íòdßÐ8é¢Òâ<$l¡ãÎ
Æ°Í]Ð¬Ûhô§Eî\x0006I!sv÷4zcãmÌ¨kÚä\x000e§á§uçm'îM\x0003:5\x0002b\x001dJ\x0016$
Ôü]Ü&Ânl¼5Õà!fJ²¥0_ÈÑuµÓÌ~ÁÏs(Îa-ÓanÊµmHK\»®Úwûþãwò\x0006å7z;T¿ÿØð´\i1æêµ\x0016}ËÇC£æõñXD	d¹ó-ó¥\x0012/eÚ)z\x001eÎëB\x0000|A£\x0017èÅ\x000bDªæynÁ»é&ø\x0015ù
vG\x001b¸*`çÎÝ,b§{#\x0000^¥=.llºòr.;b\x0007~\Æù[O\x001bggîú\x001f¾|üñ»¿úòý7"\x0006W½ñ)w\x0002Äàâ¾Ó\x000e%÷Íãð}càjøÖæ¥ þã,)×¢*aKeQ×æ%#`FÊ®À~¹¯sá¢î\x001dµ{)¨\x0002
æ¾<Î{î°óV\x0000XÝµy)¤´d_\x0010±N	Ájoãê+¬-Fzl°´\x0010\x0003É¨.êëjA»¶pÄ|\x0011\x0013ýù-;\x0002ÝÔEõeyu>ÓXèï¾qCà f9m¥Z%a\x0002Un¹\x001f?LÞ}\x000c[âß¶R­¨ \x0018\x0011xwNå¨\x0014\x0003Cû-ÙJ[ÉV´\x001d?\x0002´RªÓª}`\x000fkÛ]×VªXhE,Ó\x0000kÚ\x0018m^c9ùm¥Z¼\x0013\x0016Tùb\x0005Ù»×vñohÏ31j#Ä²\x0006Ñ1¿^(yë%·ÅEåát¨R\x0014/zjÛ«û¨¶r¸è¢!è\x000bÂJ7E
£fuÛÊá¢{Ýq¯\x0013W¦Ú\x00145\x000cÑÕGn+K\x0014ÿ\x001b²ªJ\x000fÃ}®mcH%m\x000bÑ76ÞE±»@Ö¤<+T@ÿ\x001d_|ùÈ'l\x001a\x0004Aàù3ö>\x0001\x000fÑÂÓUäYµ½ìýÔúÞÙQQÝm!º­ä0Q^¸
]£qîÈN_Þ÷_ÞÈt\x001b3Q©Ëd\x0016î6u`\x000eèÓm¤2trØ\x0001åu"/#Qª[ËÐmeÆyô¦g*_ö8ßô=ñL[g\x0014\x001bÛ¬Ó\ïÌv\x0019JÛgõol²×\x0006
|N¶ÓS0F6\x0013ü¯7'øuä\x0006ßd¦I»©L\x0017Ë¦snhB_ñ·ï\x0017õÍ\x001aç¦øÙwý«_	\\x001aÃve\x0010~S
\x0004Sü£9ÃÖ66H´4C?ML¬NFY¶\x001eÓ¶\x0019µáäïs'FÒÖ¶Úß¶\x0019µ)VUÇ¦<nÈÐÜvÐàF¦6L\x001c{\x000e&\x001aúà·úKE\x0016f\x0010Òâ\x0019\x0017Yæüus­¶·­v¿#Á½ã9\x0003yØ¦aÛ\x0006\x0001745\x0001Môm'¾Ct
ü^\x0002án\x001342þ\x0017Ë]#4\x000e1Ï[W¨-®VX¨»mîIFgTÜhï\x000cµµ?¼7jÚla²½izù½Ë{g¨-ÎÖ=±ÿ±¦©a\x0016$9e\x000coìÀØÁ¯IþÂLòçö£û7ôÔ9\x0002sêªwÏG{R$ñýà\x000bµÅ\x0017Rh¬×)&×Ï)=·÷Úâ
îéÖLM:¼àA°zº$ £8Z§ÆÊè¦½h{G¨-v	`#r©ç§\µo}át\x0019Yü £hHSÙ0Ì¬öi¯}pCÏz$DãW`Lð-í{ý.lÒ>hûñÚ¤¿±0ä
~ßÓeä¦\x000czÐLÓ$¬03Ï;¿wàÚ:¬¡¹VfµçGó¡ÞHÁÖ~\x001bú=\x001cñ4§·RûR¦LaÞv(ÞØ\x0013+1\x0010Èè¶§eîÇÓm¤f\x0012t\x0014bãü°¼*|²«ESkëã
\xCðÝÀß\x0002?\x0011ÔV#¨]ûTnl¢.ô)E+*LÅðbEÀµ¯òÆÆ\x001bÉ²\x001e\x0012©ð\x0018òÕ¦åÖîÇ\x000b4\x0015@xÎ]&l×çN¼´íP¼±i\x000c)c&ñk§íveÛµy:Ä]=\x0012\x0002:M8¹05m}Ê
M
4B$JÖà¦>·¼Kô÷\®ÿûËûßüÝ\x000f_þÛÛD&®ùÂ]-N£_û+ä}\x000fÏCè½þ­\x0003C=*.óºy¿v\x0017/Ûýçh{åÓj":ÎüêV°t­»²ØwC·\x001f^èÚÓs÷kVåò4^èaÒä0oØ÷õõ\x0018è!\x0000z+	5/o8o"ès÷ÚÓê
\x000côô¸\x0002¡É|e[\x0014]<~;3\x000b®ä¾9­{
¼¿{ÿñ¿¾Q\x0010çF\x0005S6¸n\öäq×Ô¾1¡jrysT×½\x0012àÉ)GOuâäÖ¹õa;|ÖW\x0002¼ìý«WÌ ÃÄÌ¯
\x001dw!t_\x0019ðnmZ&k?HæYÌt_	ð²/8ªï\x0006Û,\x0000»©¥¢oùïúÊ§Z½èÜÈ¡¡¦<uÊÛV\x0013úÊ#\x0001î9\x001a?*m ¼¯$uJìï¹Åºº§y¨àvZ\x000b}\x0011ýü"Wõ?~R7juS/fVÎð ÆðíESß=-Ë\x0017ÙLÇÂ!0Ê¤7ûvìò\x0006F\x000f%:*µkê¤L2w\x0017û\x001a¶|74QÑÖÜ^ßýÄª&«Þç4úfæ=&"\x001aWZ+*ªO:XCwlMiÜÐ\x0018E-êXQ-Í§\x0019{\x000c\x001a>#æ\x001d|õXZÔ¶yjTruR\x0003Ìæk®aCßè¥9\x001eEU-6úSW¢¸öû°áÆÆ°!\x0010ÄAWÒ\x000fÖ±²v·ßÐxJ|D\x0001\x0015¥¡ª÷=ÈNÐ\x0011¡ÿ?êÞ-G³ã¸\x0016Jï.äýòhQp\x000e¨\x0003Â2Îk£Ø,vTì"«»(Q\x0000OÃ38þ§áx$DæÞ;WDæ.\x0012Ý]eûÁ&?öêÜq]Á=d¢ÿAV[;å£Å¼®¶®óô.[£\x001c¶Ôà;U§iSsZÃÙ!	xHø5\x0012\x0011¤LÖ$}¸ÛºÏD\x0012°dª\x001aÙ¥Ê)ù¿Qân­Ðg$e<ÜÂ¦ÐgÄ\x0014]}ÑruùìºgÐFLalÿÔ½é÷=;£¸,õrQÆ\x0002Mö+]Ï´k\x000e-]\\x0014\x0016\x000b}£nÝWåLM\x0015¬ôJFÐV\x0013´ ö3I7vuì3\x0014\x0014	Ï¶[)Õ×.q\x001baXÎNIÁS\x0012dÑS¹43©×\x001d5'à\x0016ÿ­Z&gÁË«	W
úìÅ±øâ\x0013OÚ"-Ò}¶nÔ¯{ýe4I`O¡Iv6A;v\x0000\x0013ËÓÅô¶sáÈHVË©îHÁ`WÄN\x000eû\x0017S\x0011õ
¦\x0006ÅÃÖMrgNT¬\x0013usô8bû\x001aw\x0017\x000bUåU\°ôª³WÇá«Ã³\x0010UÅºS+^kc\x001f\8ÙMþ\x0001ÀÅð*Ë\x001eCð¨«O\x0016µÂfj8!óùæçKå½bß«È³ÂE>A*=ó2òtÃ/×_²Ô¦.7ÌUñ1.MMvK·ñ@\x0016e/Q\x00145\x00145\\rµÊÂ¹; Uq
NE*®s\x0008"rÐÐÍWGèëÛ\x000f×ïo/t\x0014\x0007\x0004}ìh¤m\x001d2È\x0004Ø\x0019Ù^>­!ËlêQò¢=KÃEG \x001aÇTËjVÀ\x0001,Z¢¨Úc6\x001dÙ6#Qµõ£Î's.	à\x001e1D.A#Ë¬«qU\x0015p@G	
\x000e#omÐ²¸ÎÅª*àÆ6¢`ÄM­jÎ¨îPò}6½VÉ\x00074¶\x0011ù*\x0006èÕ¬úª,ìð&¯%\x0007´h#5j5ªæ''\x0004{³s c\x0017QðÈïmTb"¨\x0014§ßÆ»kkf]D^îb\x0015Ù\x0003V\x0014\hJÛ\x001fÐªÑ\x0007T\x0017½éÒPRõ\x0017lÉ®rë\x00074\x001ekÎh\x0002\x001b)2\x0012¼ÚEæ02çFæUÅíÝ«¯n~º½ÔHcWäHRï\x0012<±<v\x0011¤D^°}æ:ï_×ÅÉâ*²\FÁ¨ølIò½èa:Mvñz À\x0019£RhEöpðr\x0011N> ½Z5Î& õL°ê8 \x0005Y\x0015\x0003\x0005LTõME!U@ù@Æ¢,'¬y>7BÛ¸¢8I]^ª_»°9¼G2ªvÕ³2Z@yR¿vîâdyà\x0014,88Ô¤&IûÚ¹Ó{Ü¯ÌÆ(k²ªæå+î×\x0003Z§[1\x0005Æ\x0019Ù\x0007àJU«î\x001eßÙEäV(ÉiÙªD]WAÆ\x0003ÛKlà\x000bgªQU#,MïK\x000fN\x0005,\x001d}S'·GÑª»®\x0006Øt­¹Õrh\x0012MóIÚ$=ñ7$õ7x/¨09\x0019¦Nº8³ðÐ\x0016Ã¤?´äöÇÇK="º\x00102\x0006 \x000fÏÒ\x0014cá\x0004y¸]\x000cæ\x0005âbxQHª­9µ¶ù	gI\x0007òõª=c\x0007UÒ7ùUQï\x0001L\x0000ÅËæ\x001859+dU/\x001cóÒ¹\Ì\x000e<Ù\x0014)î³\x0018\x0014Ç}³þæ7dnp
ÌÌ\x000fÐd\x001bKF©c\x0017Ýú
[èEÇ\x00177r
;;êfUÓ\x0016<;\x001a8'XË¢\x000eH4K\x000bÞÎ-Níèá=Ó\x0004èèéN¥\x0005¿S\x001dªÅ²^î\x0011'¯¨±Ýau@\x000b\x000bËx´t;²j&MÔ³	¿\x0018%\x001dôx½
å¬zõÃ¢¸ß\x0019©\x001fÿx}ûþã?üïÇ»ÛKeéYT\x0005\x001b\x0001Z)kÀ#c¶BÃgµ±[ðOúÑÕÙÆüù\x001c±Á&Eßìì2\x000c±#é
ùÊc¯»O©j¡`j¥\x001eÝµæ©q¢>É0ª\x0016ÄÔUÓÃ\x0001-\x0006¤É
nfn\x0013½S\x0007AëªÔã\x000e-f\x0016
R>:5¢\x000cH}äüJ;îÈIî!ñ\x0015eÙÐ\x001ejQ/Õã\x000e\x0016v´ ´§"¥§Mlô\x001azÜ¡Åt´*²AüæÉ¹ºe9²ðFýh¼\x0010\x0008On\x0010\x0002É1³%QÊ-G\x0016:QÅÍÔÌr\x001fÕ	éÌR³ù¾c£±ÂDä¬\x0011ðY^F[Ó²íáÀÆëXå<Ú\de»OiH\x0001\x001d[Ì$\x0011%lLb"ªsê£nÏ¶cl\x0002N\x0015äD1ÛÚ«\x0007Ïv\x0012]`ÅüÝrª`QY½Þü°*?Ôr\x00081FR	ÿÔ\x0007§jÖÂ"Üî5eï¾b.ËK
Ô
NÑV¹8\x001e<2dñèXn9ûP¡È¢[EÝñUªY¯\x0006«hnl^(\x001eÐhÞ0O\x0006r\x0007\x0018\x0015XµÊ¨è\x000cèÓççZ\x001cÂ.\x0008mÕ¬g+c¶´ìÕÞ\x0003Z\x0004?\x0003g*Mgèª¶G¿t\x0008vht\x0008bÄj*îo\x0015¥CÁ«RBï\x001d\x001aÍö(Æ&o}%Á\x0012×._\x001dW1ly\²¬¬\x0008êIâÑóÕ\x000e|¿°¸}óîb<7ÉèÒ¼2ØbuäÚ÷®èg-Ql#2ùÂÎ\x000e|4V¶­T5©½è¥êg\x0007K×=*§2\x001aU¢èW\x0015Å\x00072V\x0014\x001bùÖFÌªQõÄõuýw.ÏÅkúóV\x0016\x0015ë¹¸gq@G)\x000fÙ%è\x0005h#TµÈ2ëìgï=zÙ£\x001cª¬<^WÕ\x0015ß\x0001qÍY²,êÆ£¶èÉ<õ³÷\x001eE>\x000e\x001eÞ Â;ÑKmnSc\x0018Ìì¾Gçäñ\x0008²Æ*ZU;;ÈdÔøÙ!\x000b.â \x0006FÆ ë·ZuâlBúÙQ2M\x0014>\x0015ô»ni²Ëè²yDøà5'=\x001cå\x0019Q³!rÿÝ\x00194Oc\x0018¹6>ÈÈuR½\x0003¶óÌNÍ³\x0007vÇ\x0004ëL£â\x0003^«§µíëg&\x0014Û£vÔf9¨%e¥Düræõ·NE:U\x0013ó!©Ë\x0016\x00076ÜD\x0005ÖTr&	o¤®MôvÙ@{@ã½EÏSIòü)÷(õ³g\x0006\cò¢-ô|ØÀNzXAg8;ÛØ\x001aS\x0011nP;\x0019U8îÍ¥äÀÆóûüS¸²åF»½òv*\x001f<°ñ\x000ev`ÛÆô:°«W]­\x0006aª;°q/×6Ê\x0006Îß\x0017ôã;6ÒÓ\x0015wÒGá&ýDÆ>\x001b=.\x001c»CâÒ±tÈ1\x0008\x0010[\x001aU¶\x0014zËñÿ
F\x0011rW\x0018v\x0002³]ªZ©ÔÃÖÌò0³ÏÀß ØgèÕ\x00155ÛÑHë<:ur²u\x000bcW7Ïuc÷ÿÞ<\_*\x0018\x001b²&ñY\x001c¯ÆÑ¢±OÝ~ÖdUøUÉ*?·Ï\x0005®ëA¬W27#)\x001e²[ºs÷\ÈÒd"7?)*ë³\x000eÆú¹{®m\x0000xL1ËsÈÞ©®mÝ¹.`\x0016,X\x0007BE¸kCwî\x000bÌ\x0000\x0002Î#é\x0007Að\x001a¬£p¡Z<Æx\x0015"[³³B¶J\x001aeié¦E¢JLWcyX¹h9á°#Ï/öÜ\x00178\x0006\x0002À^öª\x001c×nZä©²\x0018Îª"P®j\x000f·	hgwEÄJ9\x000b\x0013¤LÉÞ
òÔîÀÆ3]Åt+æârÝ*HÔ VÅ\x0008Ç-W¼Ï<í\x0013þ\x0002ÕP\x0010$Gq<\x0002hÒ½Aó>7Ý{ó\x000fÿtwûáúï.¥¼Â¼b$YÛy\x001dÿ\x0007D\x0007\x0015ptÇ$­tV²{Å\x0001VíjØø\x0001-ê\x0017\x0003¶\x0006ð\x000cl\x0019\x001dÔsëkXF\x0007wh<®Ñ\x000bêÈ\x0012ôª¥\x0013ìê:Ü°C\x000b
ôå\x0013U\x0017]\x0006\x0019ÁóÆ­¦\x001fÈ*8\x0008Ç¦ôyé¬Èï¸\x0014}¡)wd\x0011\x001b,XÎÉ¥Ä"Ó\x0011®m&eÙÁù\x0007x¢zë\x0006ÅÜ» xÑüòÞ.\x00037ÿðÕã\x000bNúÐ¶8êCØÞ\¥Ë>ëËcÇ¯ì¢ÀçRWqDeA"¥Ý^\x0006ôÃ\x001c äY\x001fø×>\x000f\x001elÕé·Ëdpcmë\x000bE1³\x0018ö\x001clTå§ni'9"\x0016|ÂHST¸T¥ñ6/¬úâ\x0017ºùÿñïßß¾¿¾}¸Ô\x0019õUæî¼\x001d¤\x0018Á\x0006TÄü\x0019å	\~¥YO¢(Ó?\x0019Dæ§h9óEòõøN©0\x001fÑ
ÚIè¯¯*©!hÕÛEh;4¾*ÛÑ\x0001U'ë7WÛ·"Ù>ñQ1U*h5`Ö\x0017}ú·j\x0003R\x001a\x0015µs\x0014íM´b©\x0014ûTÂÉ®ßB¬n?\x0008Ë\x001e\x001d\x001a/¬d	áxÁá«LÍzß(<çÇj.r\x000b\x001d®:)Êñ"H\x0019,\x0007'ïØ¢PÌ
~5ÇÃf¥DÔ¼ú^94\x0007wl<Õ"\x0013á¬×úRä²_*ìÐxö¬Ã\x000bãlQõNÕ¨e÷üïÙÁ8_pFVH«á\x0006Áè
i3\x000f
`Çå\x000bMGôÇ×ßwÿðíe4¯)jßm\x001bµ}±N\x0010Àpõy	Èi^·ÍE\x001e$:]äqò5ObÑò8Î4¨ÿ{{sÁél*\x000bÆ¡ôQI¢èÏ0½ÏêÀ{h\x00165IÜAvÔÀ\x0002É\x0003@¶ÿiùÆ*§\x0014¦·ò\x0011×ÛIÕáj]g; ÅÔ	\x0011/ekPpÃ\x0010´24[¤}n~\\x0006Òª±ê^q/W]\x0015ô: e\x0016µ<Ð\x0002_q+ÃF^åÕØ\6?.j\x0003ùLâ\x000bà¤\x000bçÕ^ïÂ\x0012ù.R 1K$_e\x0019'ïqÙû8W\x0006ÿÓÜ|#Ò\x000eÞ«&\x0010o×©W³¨\x000c$QG´Y«ä<"Q«ö,·®\x000c4se O\x0005ý\x0005ÅÊÈm<rÕa]\x0017h\x0016u»ôª·ìzRm\x0011ë2'Up|'«¸²\x001aÓ©H]]\x000c93µ\x0005è6\x0015ü/\x000f×?Âé½1¸¼»}©Î\x0018¯>Õáx¦ð\x001d²J½wàå\x0011\x0018ÌtI|-M
-g¬cwÉ]ÉBVe	µ¤äÌOº#*ê4FLW*
\x0005¼MåsÃ¶3Cs\x0007·bVÅÆ¸Ç,ãÕ^\x0000#½½Á\x0018OÓ×\x0017;K&&ÉðÇRÚ¿Ãd:=;©Lã(íÿøò¢0qÖØ>óÇ±+<ö÷h\x001aã¯á)(\x0015EåëÈ´\x0016_Ð\x001díØ@wD
8ß,6AMb´¦S¶Yýuìâ\x0010Û\x001c)7ÆæQ0\x0001±£lY7½àßÎy\x000en!`r4{\x0005\x0007c\x001b\x001d?J~pÒ±46íûÇ÷·on¸¾ãÃp\x001c]:&×ï?ÜË\+\x001fÏ\x0010
q6\x000f¼¶¸Ð"e\x0007\x001b£Ï\x0004\x0001Ej.d`LâPW8\x0002óÃý\x000fôïnù¿²ñh\x000bÄu|Ö	'DB¯\x0010Èë7d¢üt?$ðÕõ«¯ï®ßÜ|ü8\x0019â,ùÚ¦§¯­¡\x000cK¼yMØrq£ùÄ¶QþÃµírøo½¹.\x0015»x\x0006¤e±NãôE\x0015\x0006}ð\x0017y\x001c+Kâ¨£Òm;\x0008³9.À\x001dç:\x000c®.®$À¡>¥×EÏº\x0000\x0008nG[`_9¤µ	<vçm#õ\x0004Æµ\x000cÁÎ/ßÝ|û~óï¾¼¿ûþöúý¥Î\x0015Y>â\uScûèËÕ\x0013ç0ªîcÅmZ\x001c+£vE(­aú-£s|\x0007ëÂE§´ïÍ ª0\x000e \x0013Ba^0´(ú$l?jµ:v\x001bâõÝ±=W®\x0003«E`ØvDã:vë­úªíØ\x0011.Úz<\x001e­\x000c±®±ù\x0003;0Åy\x0004ðüwÜµZäº;'¼Uäz\x0003|ë\x0005Ã·ÖPÅ\x00006\x0011DéàÍ?
V_ã
<X¸Äú `qP\x0003¿C)IðÖ6\x0011ÎD\x001ePä6\x0003m43ÕyFp\x0017ÕQé¤åDæüÃ\x0000\x000fÐðLàN&p¤}ä~\x0006ÝÍÊ°)ÌÊçñÕï\x001fHí¼½½¼ê1@*Ñ4a®aG\x001f[\x0002Q×P½'­Ì»B3ê`×¹Ñ\x0018\x0014Ïhn
Ù^\x001fÖàvd/\x0008výH2\x00108ù\x001fYÜ´dåÖû\x0006xNÛ\x0012¼\x000fp;¶¢·-_qÓª¦	\x000fé\x000fU¶«\x0017í«Û\x000bZI1\x0004e\x001fzw|Gñà¤ÑwªÈ/çHÍ'*[m#±w&
\x0007*TØvæ\x0004\x001e\x0000Ã{C+\x001ad\x001b\x001d9#°óJÈ\x000b¦\x0007@sZè	(p	F\x0010sT\x001a!è^¦»²ZÌåávf#ù´£\x0014ª¸äí×ñô\x0004è\x0012öÙÒÓ_^êAó
ÏÝ\x0008\x001bÞû×Tá\x0011 \x0013\x0007G@²u1?Ò\x001b0>ÒÌÀ:°[iJ\x0004ìR¥1l}Oöùù©kàÖW´\x0000ò\x0018H\x000b\x000f\x0005{eiá%sÚ¦xL§É¶Pìv~{óáÍÍû½¶àæa.+ødï-\x0008\x0019zcðÞÀ2=Ù&é\x0008ÞË9Nú ñ­Ü+°MÆ!¹,\x000bë,ÒJ}ìÈ >&Iå+û´gº\x0002@N\x001cG\x001bGß$¼6u¼hÚã	gé>¼¹¾»½yxuü?t¨¾ºþéþöáB§\G¹(_Æ©Jtõ\x0002\x0018¾¶<ð3ª\±å²ËQ?vÉà`ë¹Ç\x0010O«Ah\x0012\x001fìÌ»\x0007Ðp^É6\x001a¥\x001f]RYHÙT%å4¥ç\x0000Ù\x00032Y\x001cÑ
7B*Wt#ú¸ÞY³nÐ\x0019åÅõb@'Cþ\x000e\x001dõà\x0012\x0006Àø\x0003ï{S}¿»¼Ô\x0019
ÎUuq nåa \x0002ß:ßf\x000f?ó\x0019­Éþ"9dÝ\x0014µ"g:¡~8\x0002¡.¬qs©.@£R%c\x000f\x000f©µØIÐÖJÇÎ¹ô	 Q«:hçU×+ì¾Ns- £Vu\x0015Ã¹¬¯¡©¡å\x00195a\x001e}\x000bÈpüéÀ7VÛÃDÒø%§Z@ó@ï)Ï\x000bÐå\x000bq(­\x0017\x0018<ÑjÕNWÌ4{\x0005|è¯¯?lÑ»?\ßz¡»åWç³CAm]PaæÖËú"­·\x0013¦\x0007 ÑUÝ\x001fwËG\x0019M 5½\x0008\x001fÐø\x0000Y\x0001^I\x0008EzÏ>y\x00154im­s i\x0012\x001a_á f 2´K
ZÓ­´8\x000fú´ÄÂ«/ÉL}¸ë|>õ(©xºoÅ¾û°èhÒ¥Õu>ÏqzÔ/$ÝPAC
.Áv;}ªÔ\x001dÞ¶zE¤ÖLZ¦áÒ1U\x0006æ¾\x000e=Ó7\x0000²GU\x001a0xÁ\x0005åI-mÝÌ/\x0006Ð¨ÿyvP\x0010v^ÈÃhè¥Y½Cã\x0003@X\x0019¡\x0003Ò/ÒªÒ`viV¨?kÓÿü×û§·w·\x001f.æ¤\x0005½ïp\x0005¢Ô>¶wº½Dkz>§!NçÔ\x0017Q \x000bX¾q^Ù¼½Ö>M!N§)ÑÇßOS\x0015o~4JÓµ9\x0011ât"\x0014wõM0â\x000eDë\x00154ÓéSì×ß\x0000z\x0002&~V¥I\x0011±Î£\x0011\x0017\x0016uYÕëW¿{¸èÓ_ªrJB\x000b\x001däÓo^ÂÓÿ+\x000fk,Óó¼\x001e\x001e\x0013\x001aÍÒ\x0005LÄÚ^þõaÝ ê£Q¸C\x000b\x0003ÕWeUwßoaûé°ÒS`­Ø\x0004a°\x0013\x000cVø\x0015¡ÊÀÆ<f¦³	\x0002ñ\x0011kOVUÐfb¶f2*6ÖÒ¹MþS©Q\x001fÙnèá\x001dg¬ZØ\x0011_fzy!MvEÐYÌßc¬È1£2×óÒ®Ø¡ñ
DQ\x0017ÃçÔ+àTä+²2,vhQ\x0004`\x0017í\x0016ª<§6¨UÇU1Ä\x0001Æo°"F1\x0019¿ÚgíÀÿ·CcøÃ«p`áå[\x001eÒLd\x000cÐ\x0010VNä´\x001a,\x0012pÒ\x001cr5Is(´\x0011¹öìX\x0011ÅrÂ'ìúÆ\x0015¹ê8w\x00030î"½àøx$óø®¨§14
.7=ÇáÃ§chÆ¥$\x001fÈ÷t¸ÕåM¹¡pþùþñãñ4Þ?üÇÿ7±F~bÞ&\x0017u^Çpû\x000b
HQ¶ÆÌgV9ÅpåÂT/;ç@¢k¥!pX#_W'ö= !G®R\x000cav];tÛ\x001b¹½LøÛ\x0005\x001f\x0019\x001b´^èTá\x0017½AW,h1^ª³qí
æ¶R\³x\x001b]Kc¶º&á(±µ  e\x001búD\x0008³\x0008
uìØf\x0010à0¶ká¾\x0001\x000e#®7E
ñ\x0000·\x0008^ìèØ\x000c\x0006¼d<ÄU]á&\x0015w²ÖÁf\T|\x0012WkªÒiÍÅ#a`{Q\x001fP±ø È\\x001f \x000eJèØjÇÆª\x0014E	\x000fÈ¸ÂØJóô°¿
'ÇÐ\x00068\ÿ%xDmL.
ÎØÞÓ7;ì\x001b¸Gð$ü ¯ëQVk«O²él;\x0013n§l.K'ËÀ\x000eÞ¦Ú|&bqÐ\x001aÜW.n¾	2Ð\x0016eËÂ*nØ\x0005¬bnuD[\x0013$x\x0010\x000b«ýtñä\x0006¹\x00087»¡0Í)/¬ÚªI\x0017³µ®Uo\x0017\x0011g\x0006÷\x0016,\x000eW«(¬â¡VXµU Û\x0016®§?»B\x001e¯+u´uð À³~¾[°O\x000b'§'pr\x001cÇ.¤³ï±$¬Àpè~XÚHkÏVqå!¦x\x00067W"Áo³Ê¶RÚp¦Ê\x0003ªò×úÉ§þ¤Ä¯c£S.rOVh\x0016RÎ)pÛ\x00189N®\x0010ÿ0ªð\x001b4Þ\ìeýÀMQéÆ$\x0012ÍÉÊ#ÕÖ%QC¶/ô};²Î¼¬¢)-Ê\x0018Ã\x0019x\x0000pCÇÜBÝ\x001d7\x0001T\x0004w2
ârsbb:±Vb\x0002kÅ¤<\x00085	^
ÜÏX¤#ïr{)â¢J­ccáVH\¸º±\x0004U[\x001agt=QæüÃ\x0000'»

\x000f<½\x0014X\x001b°Û£·^Hwr=ùí(Kó2I\x001c8Á$±\x001bU}ª'úØ»=jÍU\x001cDºû\x0005E\x001erà-¼QO6\x0018ÐÞ]E@6¢*¹rdXlÓêè.¬±³ÏÍ!zØL&O\x0004[L\x000cUþ\x001f\x001aÑmN'É?\x001cà%g<â¬Ø±üÌª°\x001b©ëûÓ~8ÀS£#ÀyÐ)\x0014£ÒT.t®Qw"óöÃÎah?Þ¦\x001a Ðm\x0016báên~=³[ÛZí\x0003#åã \x001bìâyÅ\x001dîhð¹)-îWZ¢·\x001fvôR\x001cÜ\x0013\x0014'Æ@0®fñ8Ó\x00167½âçàm÷'¢G\x000fu"<C¯X¥N*1¯ÒlafsP?´ºç·ª+äªgU=	¥`\õ\x000c[î\x000cÎÏ\x001e¹å¡'\x000bª\x0003?_N?áñ­ú®¶í'Ø\x0011r\x001bBEÏ+Ý1É£ÂnjMÉ]Átäw Â§Ï¨¨¯*ÕÐRÂÎó\x000fÃN%s\x0000m&¦\x0011Y¥Húx\x0011ÜÁ\x0011\dÄ\x0014d\x0003ãªHåõ±\x000c®.êÌ\x001bxÅ:s\x0017P/ó$>*ýíJ,m\x0018_´¹4pm.Ì4Q&coJÏµÄ_¼\x001d»b{\x000eù\x001d&\x000b©\x0008\x001fÕ,ã$¶÷\Ø\x0007á\x000c²5Ð©áè\x0008\x000b\x0014'`Ó\x0012Êia§6ðvj¶"ácýdü\x0010Ë\x0017¼ò\x001cN\x000e\x000bÿ\x0000]Kañðõ´BåG:x
¼Oi:»\x0019ï'w[Á\x0015Y\!Â®ÒfJí¬E»UÃ.¢Ý­$Ð+\x001cH\x0015ÁT]Óy\x001eV
\x000f
\4<\x000b©YæWè]+-ªV\x00171¤\x0006^E\x000cGÏÂKå½èþ!ïZÕíÇ\x0016t¨s|y\x0003Çør\x001b\x0012\x00058\x0015\x0003º\x001bv[x]T\x001c6ì¥ÖBó\x0003Q'¢\x00149íR³Nî5xÈ\x0017Ç@¦·A\x001cóP½jìå=ÜZ¿Fç\x001f\x0006º\x0011ê\qw°-#=<ú½Ye'±ý\x0000èeð=s\x0005½Áù®	\%\x0011ÊlÜìw\x0014\x001b¾HPÆT52#áëì!ÌÖM­ÇWÿ|sw=\x0001ÿÄØ»uò\x0008xãa\\x0003v«Ðvgï K\x000br<âµY\x0008\x0019LñDºÒeyÕÐ\x001470ð²[\x001f½sr\x0011®mà\x0010®=\x0013ÖSrnÕ¬j¬@ÿiÓ¬Ã²ñÒ#ÁÊÇª¹a¡ñ;v\x0004Ïª&16
maãû<Á³'\8ó-â+û>Ì½¬ï¥\x0003÷³aÓÁ=ÆÈ¼\x000c51e6ú\x000fE5Áø\x001a:ø¬\x001f6pÐ\x000f¤½K+aK:Y\x0014ÖýÁ8ëý\x000cÝ@\x001eaðâ­²Ô\x0016\x0015Â¦\x0013¿*\x0005È\x000bÕðÇ··\x0017òz¬Î?6ö¨ã1\x0007ºTf÷ò\x0017Yªê\x0016ÙØFàáÐò\x0001f¤\x001e\x000fhlNñÖ\x0016@;ÁEzèê`sê^X±Yå\x0014\+\x0002ÏÞ\x001aEhÂ\x0016r\x001aüâ\x001d[.ò\x0016µ\x00131\x0008?»f:I7¯ qªüÌêGo^4½/<®ºz¦mÑ\x0003ü8±Dr­ZYæ^Q'=ô\x001d\ôÐÍØÅUôN8.QxÐÉuú8;»\\x001b8º\\q~\êÂUÃ\x0011\x0016ëE¯gb\x000eÿÑb¡£j#ýýÍõÃÃ¥ô\x0012é\x001au\x0017Ý8KLu¬ôµ\x0005ù,ù\x0016üåB:;7æ­¿çIa,¶Äe¹%w7¯¾¼~¸|{±âÆ¨
¥\\x001arheUª/ Dö«{\Ó»º¯!)½+J\x0010uÙéjÚ5@¾\x0006rs0¿­¨h|Ò\x001a}ÝÖ°!ce\x0017m~,ÜÁ¨\x0016½,¿Ú¡±ü*\x001bÎóþ2\x0008Î«êÃ±,¿Ú°EùUò¢ÛUÙf\x000bJb÷
½Ù\x0014Û-ª¤È"ÅûT»¼r\x0015ÀâÑ¢^\x000f+¯×¥;=`¦r_
pb¬(«ã)UÏÞêA»`VT»sÿÁÄdÀ	óê!Ê
\x000f\x001f²ª©ikÑ51Q\x0019$\x000e\x0012a¹\x0015wÈ¬¹ÕwÄåíÚ ÅíÂÌcÞ:ÙêäÕ\x0016¦¼nÈèÐ	o@Õ\x0006±@tUJÇ²\x00034d\x000cé£Öì*	t³kç^\x0002tAd¡ó}EÂd\x0016HÛHÿb©n6hP7\+Ý~ä\x001dË*í"]@¾`jÐX¥j\x0012UnÞ+Yg­ÙËb|$`ãé«²g]\x000cY\x0013¯+#Ê	UNrÙQJD¾\x001aÓ²Ýb\x0010#`co¥\x0019$ê\x000c\x001d\x000b\x001fû}{6ÚðåYÿîÇOèßjDÝRPù\x0003NÉBÿú/´ÅùåÍÃ)`¶ÃäGF09m\x0015U)Û´Øº±hµ\x001b¢ésðk \x0016Y¢u?\G\x0016ýpöÊ	d\x000c¹\x0012²êqu\x001e\x0002\x0004È"áR\x0006c~¯ÅBZÈuíjÿfvjÆ®ef\x001a\x0001Õ\x000e§\x000b\x0016B\\x0012¿ÿ\x000eÀõíÅ\x0001½ª6µ\x0010°IQ¤\x0002\x0002Ï|vÇè×vnøf\x001b<È
¹VÝÜ¥Û³½b¹½¢1±¤7ÏJ3êÄc:i^ú69\x0002\x0010:«fS\x001fVÐ*¹s#ÕÂ< j¹
*ê`Ã<ÿ\x0003 ñ-''\x0014ÙïSdúâ6nÛEqÌÜ¸AÖª°î¤\x0008ñÆjè¿O\x0013\x00074&a¹½\x0002=)'Ê;s\x001d"v>\x0016µ+Û\x0001Ñ~u\x0010'$(\x0013¤åë\x0017oâ-ßDòx°?ÁÅÉöImd\EabÞÄKrX\x0015¹7à0;EÄ"Ðð"\\x0012o~qÐD\x0017Üô$27¸d®\x0010§4Dé7poÍ#dâ1hý±X´\x0004keê\x0019bÖJ,L-OäluÒ³UÕØ5G\x001eÄ Ç¤áFF/Ù*7ä2\x0008]ïE[¯Eú\x0004§²ìµ_TÙ®W^<\x0016FÚÇéugç>ÆÃáª¨Çà²Ë_\x0016ø¹ÚùÒÎ$b§#9M·8\x00148TlÁ³\x0003	TÁ\x0017±F9\x000cÅè\x001cT`\x001d\x0010¥¬Ñ©4\x0005ç44a«ÒÆéÎ\x0004âð½¨^8:Ö]I\x0017Ê«\x001ex³HxÐA[\x0019cåyF*é\x0018x= $´ñà>»-Ö6æWñ¼L.Cbv\ü\x001e\x0019\x000cUÁ«XæÁëä+ñ¨û\£¢¥ËàwÑ¶÷ã«¯ï\x001fI\x0017ê_d+M®Ã\x001b0¼
)¼ÍþýeNn #¦QÜn«® ?±»Ë¢­Y\'¼\x0000hy¥z¤w6»ËlvÓ\x001e`\x0013 Óf·M:{±\x000eüEÃt]z:\ieý\x0016Écå\x001fÙZ£3J\x001bvw±3j5[\x0010$h\x0017u\x001a6ê1/9ASfâ©hÄ£ï:É\x0019m¯\x0018e²«¸Y \x000bã<\x0010²U)÷^M»8¤aN'áS\x0014Ù\x0016ã:r^§~ÊÌhåeH\x000bk/TÓé×Æ`A^3bY\x001crÑYci\x000cÉ\x0018LÁIä"ÉèiWâ(öÞ
<Æó\$6fM8:×\x001b;\x0013ÖÛ\x000b\x0008\x000cþJ:7Üä\x0006%'µ[\x0007ÂP\x001d>µ%'\x0017d\x0019\x0013_\x000c{XN\x001aº\x001b<,%ç5\x000b×\x000e\x0010sKn@ÑLÖòdÍv6AÞÝ¿Ùåh>³À~úñ÷×¿\x0011q¾/ïïîn^ýæúÃLwÇ-<uÜè\x0005ó\x0019\x000c
nò³6ïV¥iÈQ%ÈýjId]ß}{ó@oÊ§A+\x0017¾ø¥9Cc\x0015zÒP^N\x001aÚ\x0014$\x000f¶âvÏcveJÎ\x0012o\x0012Ifl$\x000b'&¶DpÐP\x0018å«r!\x0017\x001c5ÄÝ\x001aIÊäõÞ¾³7ofã?ÿõßþñÇ\x0015¿ð'\x0010:8ÃªVëqBB0µ0[\x0017Z\x000búõ	ùe2òËå1»\x0014¥æàBY#¾	\x0019ÅY ä\x0012+Sí5½§èV Öx} CÓ~C/bØ*£Ï9;\x0001\x0000äï\x0002{D	

¹wx»sh§ «ÊÇìèò®ÔN>ý)zö_üÒ9zò\x00102z=G¯^aÎ#¡Ë{ÎCrí=F^í)zµÎ\x0001+@·y8\x0019
=ajn:eÇ©h¬\x0003Ñp-#\x0008ÞðP\x001a\x0014|¨bæ(Ï%Ë\x000bf
÷°úHçÑ!¼\x001f±aFÁçö§¢\x0007z~nÓLfày'Pô\\x0001(á[ÐÜóÕ\x0007+á\x0003®~Do6ô Ñ³_pw\x0008t\x0014=yÖ¸ö4:ô:z-\x0012}c\x0006Éçè\x0019ÑÍ\x0001wÑT	_h\x001a[U=]\x0002¾Høcv\x000eÃÑ\x0002¸Á\x000b5VRí«?ßØ\x001bë]+Õ[Ô6Ñ\x0019§6V\x0013%×ïÒÿöWù}ýpû¾½ò2q|JZïåqy
Ô°±Zs-\x001aøÜ\x000fXh-wOÔ»ø¤QÝ?	®\x001c³Pä,ä!ÕQlY;½ë
»Nj~ä®ØÕ57ðÀv%\x0006ù
´Úóé\x0019èøÆpãBÀÍð#\x0013ÐVnª\zgÊwú¾\x0001zFô8\x0006¶ôµ\x001f¼M\x001d=JôÐÞ\x0018î\x0001\x000b{ð ¥tàÜÛ&¥ÞBÔ\x0016\x0005p\x0014{j\x001c^:\x0015·¥ËÖ¼ô6ç\x001c\x001d¯²çìt\x0011èV$r3£·\x001ds\x000c '\x000fs¾Á#¤n£ZzÃ\x000eçØ\x0001°«\x001dÉ^Æ\x000e#ÂÑÀCuêÀ0¸V \x0000^\x0010<\x0010_?QØSÚjðÝ&9¿¥YÜR3èÆYèÀ?Ño©Z+62®|~rúâÔÚ:ÑÏÏzÆ³N\x001e¯ÍBÃÈ¥\x0010M_zëº=?\x0005m5ðÙ²Iì§|²\x0008k<E®\x0011-X`jÈ#CÕÁ«\x0002o¥sT\x0014I­Ò\x0008LWÂø\x000eÐ\x0008ØÐM'ú2§§Å\x001aec\x001að\x001al\x001dÎÝÆtrñdAÿ}&´\x0013ðpÔ¹n5~	QÙV¹<>7#Ð¯Þâê}h-Jä£4E	Jò\x001d]{T\x001eU7ß¤¨¬{¿¶,Ð½D bH,ÑÕsÚ,íé¹±V4ºycËhæê\x001b[¤lH°Íy8\x0013²I­&\x001f\x0014d\x001b[\x000eëuôçOªÅ'¹óPÿ"«wJôÛ,Uw~,\x001d\x001eËd¯àÂía\x0005ºj¦óè[¾±\x001e7
TbVºùÈ\x0000Ô×¾Áj`h6g·Íj¤B\x0008E)\x000e.\x001a/DSÇ\x0019ÞX3zÙ\x001b|Hjc{">¬ü\x0013xÌAxÌÁ*ø¨^'ßõM8UÅ6 *.æ*>!zõ8ÅÆueË¹h
:>¦^a(Á\x000fî/«HB39µf\x0001k&wàL4ø,6wY\x001am×àOåîLÀµg!wë\x0006M_¼êÀ´GÊS¹;\x0003r'§lTô-´
ýõ:TÑ
)Ìéw&}þêÝé3âpöCk&8àc+\x0001ÖI°+3ç?®à
$\x000bÊ£¡\x001a[ÿ\x0019îl\x000b\x00129.z¢·	í=2\x001eT Ä8\x0019ª¨ÃôÛ\x000fOx}¯¿i´
R
-®3v-r\x0004JAy8ÉêÌqxMÌõß\x0016SZ\x001f_}}óñöã«ß>¾¹cjÉUÜóX6^øZs"\x000bg¬ÕØjÏís«Ðª¤Eßî.Ä\x0016=Ò
9Å{Kßä\x00075|G5âI¹±xýÔ\x000fð8éÓÁÃ9xø|ðs±Ï\x0016KÔ
{ïSMÛ92`¾\x0011xÀà,§\x001cä\x0019laëx.b²n\x0006/£Rc;à
Üë^ðúãíÏï~gÙ~yýáãÍÝÝõ\Êÿi·\%#.lu\x0005íC\x0002û¶ð!äÈ¶ÒÎg¿m¹Ø\x0005'úäu\x0011¢KÖ¾	\x0013\x0016©Yª\x0014°\x0003B\x001f­éÅ\x0001ü \x0018gp6Y§(ñ\x0018Ð´g\x0018\x000bô\x0018zC~Ô&Ì@ßéÛ\x0018Yi\x0007¸\x00194
Ü{y!º¿¤I\x0001ü \x0019æ\x0008\x0008O	\x001f5øÑÔxÉäu\x000b­%£ç^JhOââ%±vç¥mGjvi:]|ûiHÆÅ3;\x0010R43Ï¦z^?\x001b=¦ýôèõ\2õó%S§(Þ@O\x0003Ýq¡dm\x001d½\x000cjg&5¾ [§\x0004Ý@ß\x0013t±ö)¤4ÐËç¡k%ýÞg
&*`pÅ\x000f÷·½L®Â c©eßzµ\x0002Ç#\x001d¼9µ>ºçVÒÜ^²\x001a9®÷¦°½ ÇÞ\x0014¦d\x001bùDÖÕ Mdyd'=àZ»Îth\x0007ø8´\x0003þfÄ\x0006Ev\x0003¯A>ÏµÏ4Õñ\x0003\x0000÷_üÂn<¹\x001c\x0005ÕÅ\x0000/aÁ\P£aÇ¤h\x0014\x000b\x0010KìÑD{*tkE:¡\x000cYnÇ5ªÂAúQ¥§5'/mï^\x001a/=Æs´ï(Ï"\x0011K\x000fUÈ±Ùp@¨
S\x0002:H2w
zi<M^¬=õÉ\x001eSÔfÀïQ\x001bÞÔ\x0014)ê¼p`yZÔs±Ë¦ÈÄ@ÇÈÏ\x001eó[j\x0015ám'£*%õ>óéõ\x001að\x00153-ÙÁäò%4G\x0019^Z%í9GÑ'\x0011Å5¡É`vN¦Ãû´%gNáAxçF\x0007Ã»Ñ\x0001×v6ª|5yÌ\x000c?\x0006<\x0011âqô¿"gá:ó\x0018ÞM^Æ@(zóÁÁ\x0003'½{o\x000ci\x0016\x0008uñ|ñQ,>ÊS¯\x0002èÎgyêskwçzÒ\x0014Éâàä(Ô
	ÇHøÒ¨\x0006Ýù¹tâ\\x001a+ò6î×¾ú(ã6¶ÍµpSý
ÀCXÇfX\x000cÜ\x0014¡qè\\x0019\x001dBoèÚ\x0000t
9\x0019¶êÐÛ¢b¶¥\x0018ýù¡÷xè]\x001d
ì]2FHÆyUÔÇLõ+\x0003=\x0008t\x0011Á\x0001ôÐæÒàU<Î7>Co¾9}¤¼\x0019¥,ú1\x0013xK¿b¼ÏY8^ø¿·ïë_ÿöã\x001coÚ\x0006\x0011¾Z
"üD\x00174¼XOf·®x )¨ä]oè{nëÊi½
8Y}õº\x0018ÛK?Ìvn\x001eÚÄs\x0008 ÊQ5\x0019\x0010äÑ<ËüÌ@wÃMÅ È\Î£Ñª{\x0003ïìtThû0ÀkÀ\x0000 ·uÐ'¶¥Ë P\x00086-Ãø\x0007¸\x0003÷ýd³<(
]ë\x000c@\x001f\x0007ÎéaäKÏ\x001d¢\x0017%ußLC7@\x0003Ýù¡úÑ\x000b±\x0010z\x0011­ÐSzÎiÛ\x0010Ð³\x00146#ù\x0010»Ç²\x0004B\x000f5)¹çå+<Ð÷W¸¡û1\x000eµÇdJ\x0014èQ\x001aiùH\x000eìø¹Øåô0º2\x000ec\x001bX5Â=ÜSmpGK\x0019µµûþmvß§U\ýo~²>Ñdi\oOw·n#<¬[6\x0017M}\x0001*Î¶ñm¿è@v\x0001*\x0007òä\x0007\x0017ºè#5Àsü\ðÙS:ÐÑSú$t}ª~´ïÿËâõ<XòUd}ËjÔPÒHn\x0015õi&öÄÓ³¬Xó¢ßO+ñ.CÙFß\x0014eÂ ³\x0016CFñæ\x000b£cÝGLyòÕ\x0004:ÙÙÐÕªOÖ@\x0017Ò\x000c.:º(Ó©(ô=_»Hæt^l5%1Ëðtç¢\x001fÀÆ²âb±´WîETCûUæÀÆ\x0012ÍX\x0012\x0016ôñÂe·¨\x000co\x000cn"\x001bèÁ!ºÁÞ\x000b\x0002¾ú,\x0016í¤'Ã/+À\x000exQ\x0001Æ,\x0007W,¨ÊÛ$+@\x000bWhieáÓ»?ýxýÅ²kèÛ7ï.¤+¼ö+ÊÑ½Î;\x0012SBÞ	ö¯Ó\x0015]ZW0g(¹®²úÏëöÔüs}%\x0000\ç1L¬W %\x0011[\x0008NÏ¥ÅÄhDÇú6Oª\x001bº\x0010¸6/¨N°ª\x0018§\x0005Ô&E4ÐQ\x0011qi1VA%`îè'%Ï\x0015	lò£cXî*\x0016\x0005bÞ&\x0019Xh\x0013Z&M\x0004à(ö$È}¸\x0012+wÒäb\x0016N\x001c\x001f(jÑ\x0013vO8®l\x0011{
½ÈdÇ¶ª¾Uôx \x0017÷R×ÊâÆ_ÿ-eñê·\x000f×o\x001foß¾¿_N¢t*R+Ý\5®i\x0019~`üïh@ýD§|òº\x0008ÛC\x0001~
}f}ü\x0001ýRÌö	:S-?\x000f÷Íó\x0013'Ót\x0002;&\x0015¿nüQ«\x001d=`\x0007x\x0012\x000f°@ÁUÆ£U¬OÞ\x001b\x000f©øÐiª\x000eðÍP\x0004.#©ÇOçlý\x0001Ùzò¸¡È6ñ`,Â ª´+¥lý@l}2f\x0010õ\x0012z¶Ï±£ËzJeÄOåÍ\x0007º·n¬\x00043:#Sâ2\x0006\x0011dIÒõÌ®ÏíÐ\x0006z\x0018¡ÕízòZ2t:_x\x001a\x000bOòó?ÚbYØrÜ8ÙjN\x0017\x001e`áöÐV@\x001f\|ÍÙO²®Ô·ær WÿíÍ\x000fß½?<~}»âuøDÈB£ÑcÏ$£Ç>»m\x0002ñ³«¸u¡Ûô\x0000u\x0019N\x000fsh¬òó&la'¶§´¦Î¿ÏcÏ\x0001\x001e\x0006ó?dQv^¬N62\x0002ÆAù\x0016½Ó6ËîÐÒ¶>
FMF÷ÒM0ª«^%¾\x0000\x000f%¾Tw°áe\x0010S4ø¾Yij²U\x0001Â{ð\x0001f rþÜÈ.\x0017\x00130*Ëð¥O
Â;|Æ^1#ª²Íù
|?Wt[É\x000f»>oÞ]ë\x0007í|`^\x000bºy÷?].h!Û¿-aøkÜ¶Ið>\x0006àÙ/ÞÚ¶ò×]ÍÅÅ
ì\±\x0002Ø0MðAå\x0013]\#á
\x0003\x001cS¨19\x0011\x0011!sÛß¨üçPËªXc c\x0012\x001f\x0008ôÎ»ÂäµÎûs.
báòáÑTÈ÷ÆØ0;Ï²Õ:\x0016ËR\x000eÆ|æi\x001eì\x0013ÏUV
Ðanô\x0002u1Ð¡hi7Ý0^*ë\x000bTG9Ë\x001eÜëÆ§V¾\x0003Ýb+ß'¢\x0017­J\x0007z±>Ùº\x0003½â®º1ä\x000f;ðdö]}Å·ZÃ9m}À´õ§,^«:ûg÷áýªûúîúÍ¦ìî\x001fï.§ç¬¬\x0007*%KtE(ºR7øìÎ·Ú6­èôî\x0012l1\x0011Ôs<¥\x001cô\x001cO,\x0011,NS3tfWm¾\x000ctì(Nô·êDËr´ªU£´æÙx¾ô>\x0017|Nl\x001eè²?é\x0013Ðõ¡ý­ýËç0á9»ü§úýVW÷\x0005wx&¶`:K\x0019âK8µ©ý'f!mu\x0019¶\x0012ä´}©[£|9/ÇË-\x001a¦\x001f
\x0000/\x0002Ü¼<O5l0w}pöùÂ1\x0019O§ª8\x0000/HÌ@àN\x0006	¹^xÕÿ1À\x0003[ñ|z\x0011hkD\x000b¥®\x0018\x0002\x0006vÄ-s'\x0017yXT¢ß>÷\x0014<ãÂa\x0008\x0019;\x000c?ÒÊe¹\x001dI¼ÛM¥\x001b\x00078n|"øùY\x0011\x001b\x0006~~XDåÆ'k\x0015ô×\x001fßÝ|{¿RAt/¤~¸åVEÃ=Z{B\x0014Aj[\x0014æÙÕÏ[®ö¥¯=Ç¦çÊ\x0015zHA@÷db/6)i,\x0006\x0011!6¶¶%4Å8\x0016Ø&%\x0000¸ä\x001e±\x0005{&¯fª\òY\x0012°\x0013´G¨¾¨¥ÊlfLí¸sð\x0000à®)&\x000c.z&\x0013+ªÀÝ*d:ÀGÈÀË\x0015J%cn±e?v>ºë\x0000?¨»\x001a¸\x001d<Á¼ò<¦þvtY÷\x0018¹ÜwòÅßü)?~ÿf
þÃíÇ\x000bE÷¹W<¨*CðÂø­@\x0005dè+Ï~ÏÖ5)SN­OçÔZ\x0000é4Ø!\x0014}¸>È(Ih\x0005`\x0013qÁ@\x0017Ä\x00059\x000c
ÿõ\x0012Á5²\x0004\x0014ßEOM×a \x0007d¡ÛÅº>Ë&kÚ0ÎÓõ©ú9÷Ã\x0007 §ü_ßÿÀ¥Íñùß×\x000fßÞ¾¿çã£L\x000cÔÚÂ´,ð\x000cpãKH\x001f­\x000fV´]M#å\x00117`ÍmT©foUÎÓÌÄã\x0002\x001c\x0013ª¥Ác|´¬\x0008\x001fù  #«ÂÃj`{AìãÄ±õN-\¶UçÈáý»~~\x000büËG\x001bÖ×·w\x0017#£çC)Ú®8\x000elÃ\x000fÒ»ð"âõ\x001bsð\x00146b\x001d]\x001c5ÆXÇÉW=)iw\x001eã_\x001e¿|
oÊýÄ¹TÙ%@>IÜBzóÍmdµ\x0015¢¿ÔM1:\x000cÑ%×\x0003\x0004ÚÙG=)ÙÎþî
øò_\x0006þòÝõã÷7\x001f?^*ü¦ch\x0004`ýhyÇ#f{ù¹z	U§Ì
»xá¾0]-ö8.\x000cg°°²¿ÊZ\x0014Iö\x001a¯]Â8\x0007|0gÂ¶QÁAðaÌÄ`x#à³¶\x0019@WÉÍß]?¾yw{s\x0019~èTyì¢8¥¨ì
zH¼ûÐ2kÏ¾÷Ü\x0004¿xµÄ\x0012ÔîÉÐlÔî(ù$0bj\x0015\x0013gë\x0001
þ\x0019¹\x0007Ð6Àa[Upåd,¨-½âö\x00166lþáØ\x0008nÒP¤Ã'Hêf3ÎU\x0004\x001b6Ô\x0010Ð&\x000b\x0016õè\x001c61\x0011¶W4/¦Õxù)/´c\x0016Þ\x001c6
ã\x0000yéA%àc6á9\x0006êL¯q$ù¿º¹çSq»PrÎbhCqº:ç\x0011v\x000e*\i½8Ï}\x0017NÚ·mâÍ$FÖáØT­LyÚ+;\x000fqÔ"­\x0006ßÉ=grç\x0003û8±$Ë-:ÁzQ&UjPÝE¾Ç¨¦¸à=¢©ôÜâ±\x0013G*"ßÕPz£é\x0014ZÛÝ\x0008¬¥\x00123ðí¥P¼¸g¥*®ÐÉ\x0008ÝäñïØ\x001e$â¬8=ë¢5g\x0019\x0003!7­UtO\x0011\x0003øÐilo<1Ê´s\x00178µÐ±;;"\x000eHf:\x0010\x0008Wby\·"g$eÒªÅ§Ðñ=¶1×\x0002Ä\x001bÀV¾!ÝÆÞù©ýì\x001d»úmÊ\x0018JÕÛØCxY½Ä&OS'2ñ(\x0013S: n.E`W½-X6¥é\x000fì£.Ñ\x000b$ª\x000bQ{éä\x000c©×tM~Â=èQ\x0012-\x001cÊn\x0012ë}×=Õ ã©nã8²n;ö0vS\x0001-Ïj\x0005\x000f7Ç8¥ÛÚ`'â×\x0003\x0018\x0004ÂMöÈGà¤¢}S¶+ïc°'ÐÁ\x0002´\x0007\\x001f0¢°Q4
{\x0007vãB¶C9*"{)ä\x0001it+a²2vìaep¯Ú\x00104éA¬²,ª^¬\x0000Û"Gg¸	qE¦hàég!
Y0L\x001dzäYR¤we0u&â\x0004vV÷¼wâÄoÃ\x001eöãàøæ¥d$j¯Dm\x001a¡y<ÓO\x0011ô\x0013ÓGÀ6ú\x001cåºéïVÝ·¹cëÊ]ÅºÇ\x0013ænüñøòÎÝ tM \x001d±R~{óÃõÃÇïoÞ¼¾»yå\£ñ½Dï5\x000ff\x0016\x0011ÆÒ>nÀ¨©ò\x0002ÜwÏgïYøY-v<Õa\x001fs±}¥ÍÂÚ×ÈÈ ÂSW[ó>±\x001bv\x001cM>Õ#-\x0015ée\x00161P£°Jí³rÓÔP±\x0001'7J°Ù\x001b=	tä"Ô¦¨z¯jw?ÒÔ§¹C.MÏ¤\x0006¿\¬äé\x0008
&&\x0015£¿Ôiª\x0007Ý±ÓG.0¥Ü¦:äàs½©+:¨ÉÂÚÏY­È¥5\x0012»ÅZóáÝ°3äw½Ïèá{çH61É¡SJ­ñ¿O\x000fÓ=Ö]h'a\x0014+O\x0004hke7uMÚ3Ù\x000e
ünócu@Û*»\x0017J9Çfy.gË.°ìjð	á\x000e:§Ä©y+.ØNr^×G°ý°ËÛe\x000e\x0011¹1\x001c£T®x 7d?X C\x001bG<ÒÝF6\x0017Äe¾Û÷ªHë'z\x001d»\x000eEâJ\x0004Î\x001d\x0002WçÙÊRg¿\x0011l© e\x0003\x000fPòGÐ¦3Ø~8VNê#Bô2:¹±ØgX§ínÇ\x0006®;'ZsÉðOÂöb::\x0001]m¾àéÛ°¥ÏÕ0:\x0011(ä\x000b	prËÊß4}\x001b8ôñ,\x000cnÉØÄ\x001fTv\ÔF½Eë»>½¯¯\x000bTÙI\x001e¯CII>;äôcÎêe\x0016Ä_2\x000b.\x00137\x000e¶ÈáÉ»#nl
÷Ó Ñ´'õ¹\x0002:Èe¼[='QÑ	¸\x001ce'(a[\x001e}£ôDZS<ø
9`Ý÷§\x0015ÚÉëÛ±!7äÈ\x0010\x0001|zoA\x0007evFd\x0015iÊ3­^A\x0006O\x0016ÀIÅ´	Üû.O	ÙæÄ:J`{×¿Î°\x0003bÊ÷p¬kù\x0003\\x000fÄ½>8M)\x001d¼ ¸Ç\x0016\x0017úÉ£m@à±(µO9\x0003Ï\x0000þÛY&²²
»ÄÏÆ¶pm\x0003·\x001eø\x001d÷8È[0\x001btÐ;+\x001dLcÏ«¨+gÏÇÔ¤´ôBÙ¢'"o?\x001c+7.À\x0015ÚOI÷@gCÅ z\x0010ÌÆ3ô\x0008è¶\x001a\x0011Í$ëY\x0010¸iã\x0015z£\x0011³g\x0007ÝâA·%bÍFÊª\x001f*ZEn\x0017c\x001fõVÝ	:ÿp '\x0013ðE,jP(ª8u²õ¨ik=ûßY>·Â\x0006©²`g
7ð\x0013ÕÕ~øÌ³îüÉEj?\x001cráFüRëOâ\x0015¯¬pÊÿmÈý³\w\x0001\x001c%JúÏà²²ÆMÄ
}*ÖÛÑm\x0000to±Þ¶ø"Xá¸\x0004Vîg×¹.Lå;º\x0007ôgûÉ7¿¡èöÃçnh<¹Fí\x0007±tp\x0011jHc@x[º:Lp×\x0012pÓP®
=áH®*\x000bÚ+\x0007¯aåUÙÃä\x0018ùNPu²ô\x0012P.L\x00109°ém\x0012®Ù%µòNÉrv\x001a«ù|ÝP'n(Çö ÁWS\x000cQ1Ýæ>¥Ò\x0013ë¢ý0Ðié r¦Ñ\x0015³M¬þÎÎ¶¬§9Ñ\í\x0001nEß7\x0019\x0013%¨\x0016dÛ¹jìÔ\x0010¿[ÁøYz÷~l¨Lù)õbk\x0013¡\x00139e;:ÿ0Ðm\x0002~ :/Fö :Ó'û¾EògBÑ\x001d\x001d/i³s
 ÇD\x0012\x0004Ñk(÷44\x0005ÃÝkôX¡9ÇX9Q6X¡¾HñÊY\x001cfméæ%hCOþÈe×E0©\x001a9íËi^zýz.{"	ÚÁÇ\x0014
Î¢K\ÉýFÑ¥$GBåÃ£Û{²§yd\x001ek1\x0019É®éM\x0010³_\²òÀÎ àó\x0014ÜßÁGp÷_t8úx%¤\x0012dÍaÎ¥/|b×Û±\x0007·\x001eÝ\x000b\x0003\x0003SVFô\x001aÉ \x001bw\x000c0x91^Ú\x000f;8\x0017¢Cö§p6\x0012EîUW\x000cÉi\x0003?ÙÏâÆ~&¦\x0001\x001cê¥TQ-éz©>\x0015Ó³V'Z×W\x0003\x000b¯ØàÆén1¬,\x00119O\x000ebË§UTÀ\x0019Q%n¡AÓãÓ\x0006#\x001eàÖÉÀ\x000fá´
b;!ßÀ­=W\x001cÆ\x0003~§T\x0008Yq¿»2\x0017k¯)ºwp\x000fàUDd\x0019\x001cR§\x0004^eÀûÊË\x0019x\x0001p~¡Aç¢A:!ËÝìRçÖÆÌâN.ûa\x0007w,s\x0010\x000b=Ñ8dÕ¢hÓG¸Y!ÀiáéràFA}­¬¬e\x0005ÜO,öÃlBÅâ\x001e2Do³MIQIÞ÷eÐí\x0003<\x0017ì½(ô\x000c\x0019±n#[¿È²hü,n\x0011ÂÈV\x0017RZ!ã:\x00044,lÌFnfj
å!¼ý!zÀöV¼ÎÖH©D+3{¬¨í<\x0003Ï\x001eE^0$·dð\x0010y~.¼ñex³ð&\x001d2½4´tÏÂ3Õ\x0014Ã}Í½~íDÛ\x0006Ð¶%\x0019\x001cRJb¦­µV\x001e\x0016ÒÎm?ËYÑ~ØÁ¹x\x0010\x0019_2] PZÖÈ¸l$#¸¸Î¤RA*<ä\x0013ûtäÛiÈ´þ³mï[4'w³ýðÛÉ\x0006Û"è»r{Ð·³¡\x0018|ãj\x000fd§ÊëâÜ°AÊf1ò­5ÜýþþáíÅ:î¬ºtö¨ãXßØÜØ_¤ç\x000eöúèËj\x000eûdIøá³}\x0008ö&\x0017[\x001dÔ\x0010äJ±
5\x00188wd\x0007Èä°##5fm¶J4×`:«\x001bôP=\x0004í\x0006Ù=!;dÒçF;\x0005Üje¦Úµ\x0003\x0018zÕbF_-§Köê\x0015é%gÂð \x000c²LC\x0016bÉè|â²\x0012s\x000bNO=+\x0007t\x001dÐÜ¼4Äp·ªdÑæÆ	\x0019GÒ}Ê§\x000bë\x001aÑ¿\x0019wwÿoíïo\x001f®\x001f¿½L&Ö¨"p­ym¦Ã(x5|èÙïmµ«Æ\x000b;'.I­ñz¸Þ<\x0002b)\\x0004J1g9¤ì\x0016îªóvl Ð9×ÂnqàÉIÛÀa`½óµDc<bq²+¹Æjo§\x001a¬\x001d<\x0007X9Ó`³C\x000e\x001aÇÌCç>k¡ý|¶ò\x000c+\x000fäÞXp^I[\x0000¿\x0000%ÈFÙ=
<Ñíà@Fæ\x0002½¸\x0010{§	W®SàmNÁÌ¸±#ßkµà½2}qÅ'Y³@&m+ÚÍ©
\x001c"ï.ðIP\x0011\x0014z\x0004®Æ\x0011e·\x0005$ÏÀ\x0000÷W8\x0010'È±)\x000c.Ãz)dÇ:¸È¥l¯*z;Q\x0004$éÎXï(ëìX\x0007Ï\x0002;\x000cà&é$úon®a\x001eëà\x001es)U\x0011{7¾Â\x001càQúi\x0018bð3\x00179\x0017IZL\x0019xJ5QMGt#ºÌ6ì\x0006qCÙ¥È{µ8ÎyÊRq¹pÁjè"Å\x0011Aè¥MÕõQÃ\x0003=ËDÚèÐ\x0017\x0019¬.Rµ>5zx³hxz|õåýÝÝÍG~\x0018¿¾~x¸¿P_»uj6\x001d¹$ùðªø\x001e²%^\x0008{Í¸v*þ&I¶î$ðíl@\x000eUÒ\x000fÒý"×\F^º=4²nÈ0Â¯³Å\x001bWÛ+6}Ðù\x0005VDeªâß Ë\x0018ÒèÂÄ(ÓD¡ïe³f8m4QsÀ\x0006]\x0001z½ÃO\x000eêwè\x0000«N@Ô\x001cÒnmQ\x0005s'Ïò
\x001bôW èÌ¡y¨å`×\x0011WíU]Ú&ÐMå-;6·d®ø\x001c7éº $Reÿ\x001ai¨f~m¤ÌÅ3â½y/3¢ycN\x0006"nØÎóW$o\x000eýg.õÁÐØRó.A'\x000e8t®5Ú ¹ºUÜêÉ¯\ógK£ãºyx¸ýÿw)Z\x0017%0\x0019;\x001fNeC ´0Üú\x0002J´yTr^tXO¶8	±¹wÇq­ÜQ&ÒwröÓ
-÷is¡×\x0006\x0001w`qÝ&÷NÚ'y\x00041±lÐÖú\x0001M¯ºÈ\x000bX¡vHëHöð\x001cz©Ç\\x0000¾a\x0002p®Æ\x0011áØ¯Äª½ì9Î±qeÙ¶döcÙÑºÖí\x0008ÂF{Ð®m:\x0003÷Ü#Ú±!\x001cé,büË\x0016\x000eÂVê9·dæ<\x0010kÃqXìÖcým%\x0000Ñã¼"MÊ½n»Û±!AF0¶S±_ËöYrµ\x0017³MÃ:\x0012\x001a\x000f`\x0014kÎ²4¥\x0016mqs±ý\x0006<í+\x0007
ø¯ä\x001cãç¬\x0005(Î÷AgN°h_Ï¨ÒÑ\x0016\x00172\x00188*\x001biÎä\x0003vhþá\x001e½ld\x0007Qæá\x00177u\x0012õ¹j}Ã\x001eUëd\x0004ÉBêd¾+\x001aÅ\z¦~ÎHíØC$\x R«.È£\x001dUmN½{ÍÌíæ
;\x0018Èéz \x0003£eG¬s&hïHzÿÚ\x001c9Û Gä ±a\Ë ø¸èd"­äÔ3R'·\x001d\x0013R'\x000fÑSoXKëA"á\x0002ÑaÀd¶¢ ®¦g£¦.Ä\x001dºÂ!)\x0019¼ÊlM\x0016.«U¶Vß\x0002\x001cq®réØÑâ²ë\x0015¬º&1]N¶tX«ë@%ºC\x000fK´òócmÉ-CSÔe'M:&\üûL|ÃTâÙA<·\x0006
Á%\x001een¾öÈbN.NAXÀ`å\U\x0002¯UfEjQÎ÷S:K°å _\x0005\x001eÉØÀÏVubR\x001d\x0019Ñdt\x001eaYÈÁ#"f£ÑÖ²2\x001a¿|wýþÛ/ä\x0000sòOÙ\x001a;#Oá&rè.[ÿôsÛ'S&^`ßk`\x0005nÅ;ù
C7\x0001\x000bUéÚÉ\x0008%)¦>Ñà\x000c8\x0001pÄ\x0014{árÛ U	m\x00050óû±A÷£4l\x0008Ãå*sÖÉbÌÛ»73? çg£!ÓA	rå\x0002"y8Úªge¹A\x000feI\x001a[0e\x0014ÅÖND"w§}\x001e¤¶AÛÑÉC\x000beÉ\x0017!rÃñYiÏù\x0013óyÃv½ìÙ\x000cÝ¡\x001f\x0019Ù^}LV`*«[¨vR	½¨[\x0010ólåWÿøþãýíûW¿½þéöBI#CÇC\x0006VB9bc	~!\x0006Á±¾\x0017ÐØsB
4\x001d*\x0012£ìö-L\x0012,§rF¼ô0É·¦;Ó¶ïÀcÛ}\x0012w,oD;\x0000,5\x00037´p\x0002=O\óLc´!\x000fÂ\x0004X1ÄãØ#";¯R\Û(§I\x0007wlk@\x0007s?	ÖRdAûnªJ+*\x0017\x0017¡.y±î®_}u}!nsN\x001ekfér\x0008:\x000eDÂØ%ò_\x00061å	'Ú¬ýH¨ýÚ7¥L/dxbÁ\x0003	$[ÙMùlçXÍ\x0006î\x0011¼fkÂÍèí];À¹j\x0007Áé./ò\x00036!áÁÆtÛR\x0002ï/ÅFjÞ©BþæHí5L\x000eýòÂ\x000c/!]NçÑþ
«\x0005¨¬¢h=\x0014r%\x0015ÆKýàÙ¶:ÕéDíÐø\x001a+úL\x0014	JÃ¯¹²lù\x00074\x0018/¦b	\x0006.#ßS/ßjâªÒe\x001e.)ï",:]I\x001b@r2Ó{}ê	p°+éLd\x0006óÂE)é,Þ\x00192 ²@[ÄhN8lÐp`\x0016;ÌÕª\x0011\x001b¶dP±\x0015`O±¨\x001d:\x00014¹þPñÞ01¸nT\x001fS¶-ð2Çíwh\x0010\x0008Ó;	v³IÊL´á\x000c:#tDÕÏÙ.7bê\x001c%ë°Ì\x001bmÐ7"YÄc\x0012.
äº«£vÃyJÿul\x0018¡HöÁb¨\x0012Åùðª+"-t¯±_,éüo\x001fn/ôæòù\x0014SËþ\x0001\x000c\x001eØÒD^6?\x0019Ï®zé,2²	ÇòÓ&\x000fXÊ½&Âõãª®%¶º©Aè\x0006\x001b£ð\x0017äW`ä Rb½ãë\x0004\x0018\x001c\x0019/X¶Y:29¨\x0019¢\x0019}f[Ú \x0007ÛRq\C\x0016­lÈæ)òpvúã¬z;t\x0004\x0003ß$aÚX¯$íUeEh\ÓÌ\x001dzLÉ¤UgaÑ"K¹¹FZËMÓÌ,;4
Ä	\x0013ßxQÈÆ£·¥±ì[3v>[uU\x0017AËè#\x001bµcÒN&;t\x0019§u¡I¡1{Á~µÌP»\x001e¸È;ôH"¨'ÕÇ*\x001ar@\x000bãD³AªQÚ\x0013L*\x0017Ýi\x001fíÉáë´[\x001dÚò\x0008\x001bµ\x0015\x0016Q£ÛD_7'ì7dä£0¸µ\x0015\x0012[\µ´zrÔé\x0003|°\x0010
6`l<|Ã^±2zHÞÜì«ÙÎ\x0003·òÕ¾¾»~ÿãã\x000e\x001båÖûdv\x0012ãÖHL¤¾Ó\x0012=ûË±vÖ¼vdÈy%3v¾\x0006QB\x001e¢u	Qe}î#çSµaCò\x00077BoL°I\x0014ÐÙXdXßóxiß{¦^ºj_]ÿt{17Í¨>ôrÐVÓl®
Tä^%óì;¾=6é\x0010P12\x0006\x000fºê=O}ôÏôÆìÀãá1ÌèHÅ(ß\x001aTÃGn£/gÏrÆx{öÈÞ£Ì=\x0011´tùéÅ\x000f«û\x0001=Ââ\x001c©\x0015eYÔÕ¶¦wåþ5Ïrz¾6hhúTè³U;Ì\x0013 õ\x001aÊ¿Ðµ²oªY2ÛsøÜEOÃWwè
¢\x000eE\x0018©d8È xPqÆÚ£BSÍmGM|ª!\ÔblòÉe/ØÁ9<ißÝ?^HÏ yc¸aýØQçDÅ\íÐÏ®gÖðE\x0003²¾(^%Øí*º\x000bI\x0018*Qa|ë ÂÊ;ò°°É\x0018úgù:SÕ!\x0008_F¬7èÐHàW$\x0014`CE\x0006lcÏi\x001c6d~°­\x0000\x0016g.¦=»C\x001eµªÓßìÂ¹ {\x0006;ÙWÁ¯«|Â
]jL+®·¼¢Æÿðê·7ï/6ô´¤¹8Û"õ+Y·ñê%\x0004DK3~ù\x0006üð\x0006tFa)®n\x0016Ü\x001a1Ê\x0010à\x0016\x0007_Pvl\x001c|\x001fµr\x0003È\x001dç£Q\x00138}kg¶5¸ÁZ\x001cû\x0014MÆTTüQ´ËÚw²F33jlà0az½ÃO\x0016{ê;¶ÇA½<\x0006\x0018²\x0002:"í°U\x001c/6l\x0018´Å¬82£\x00145fM\x0011Ëî/úÀ6p\x001c¥ÎÃ| ®i*0¶í\x0013à7É\x0013hS'pe\x0017Î(­ÞgÙe\x0012B/Z\\x0004ç>à\x0000Wn%xRóá¼ºF6àÎ¶ÓávÒ»#\x0006\x0011p\x001d<î'\x000fNSØ¯çD*\x001eixþ\x00188»É§Ö­º.M«\ôszjÃöx\x0006Þ=æï\x0012\x0017¨ÈZâXZhfÝßÁÅvfAÈ³°«Î\x000c.ÐaZT\x001bÌ}	Gú7×\x001f>Þ~{!G:VÅM\x0016C=´½Î\x000eEÛýgW÷¿¶*ÈÈüWû$6§ Â\x001c\x001cb¹õ&-#;vÀË &ñ\x001bú-±\x0015#°]kt\x0007\x0002mØû@ ½\x0013Õ\x000bÛ\x0019=BÒ\x0019ò64;mîBÝ\x000b.Ú"-^áª\x0018\õYÛ+ïN°K\x0006lC- ±Ô(¥<:\x001bòL+µAWÜG'jöKâEÕ\x0017³y@g»Xq\x0017¹À\x0005D½ñAÀªeô8´BÛê&öcÕÀþàÚt±lTk|°õÂ\x0017\x0015\x0011)­'Ñ{õnÞ^ªÁ\x000c
Éo\x001cË1\x0004tAÀÁ\x0014R+\x001a~vÝ°¸<s\x0013\x000c_\x000bnbCEù\x0004ª\x0008Ý*âÌ\x001b¥è<sk\x000e\x0000<Î[NÞÊs]»=Ãsê\x0006
<+L\x000f	t¿O/Æ¢J\x0006Óª;¡þ\x00194¬Ú{«1´HvDÍ|ÍºåfXv[µ\x0015Ð9>½j¿®¾ëØX}gJÀ\x0000pbÙcä%DÉöÌbÐ2\x001bÙKWëw×·\x001f>\ÊÙbIÅÑÁffûÌñ\x0005L­0yÖK\x00087¬_ßE\x000fÉ²+ó´#èH^Ðõ¥ªªêcíäTgÈcRÎ&c/T#F\x0011\x0003Í\x0015ýGmÁÇ8ËëÈq0dîÍ©bÍ"aT(AçåýÚ ÇýÊ%«\x0013URä%(¤ÜÊZæîò
z0$å¼QÕ\x001f\x000e6ª\x0018'Ö:\x0013\x0000nÐ\x00000sÃ¥¤Y\x0011¬èt\x0014±DSevÑ\x001aÑ íH9à°¥ù©"f¸â£êUÖÍ\x0013\x0015;´\x001b6­\x0000\x001crV¸At\x000fUdÇù¹(\x0008(Ødÿöæî»Û÷÷\x0017R\x0008µHîg.\x001eÆ
«\x0011eÿ2ò\x001cëùØ3O¥oiXu]\x0006IJ¸uZÈQ²èA\x001b°#cÊ`cj9Då)NÐ¡d÷z\x0002
õ<\x0013\x000fR(ÅH+¡¶\x0019"B¾qY\x001c¼.[\x0014û_x&öãÝ¥\x0012fNÖo2I\x0003Ö5b®®]~	Å5ëYj\x0005HzmS<ìw\x0001\x0012 Î\x0000"!
¨ª^öÖ'?éÿ\x001d9BÖbc!> ãT{¨\x0012i©ÿwh°¯>mÑyJ nÈ\x0019\x000fÁ"\x0004^4²zs6Ukf¹I:¤\x0017¹É\Dk°5VÆK¹ç¹±¹@( ±Ó Ë§ybVÌ?ô\x0017®±-d>#39¡\x0010dÍdT|\x0018¥§'çÄÖ­ BüÔÈ|~.=d\x001d{ªÀÚ±¡þ0Èi\x001e-rf^§ÌæÁÒÖ)ûøêëÛëË\x0018²LI-ãÂ.§½\x001ea¸Ç\x0001ù\x0017@Fp2î}\x000eÚ²\x00001h{þIOc\x0011ä\x000bá©Èò?ÿõßþñÛ7ïþ\x000b(#¼w²R]Ó\x0011ÏU\x001d<ßë%4\x0001zã\x0017¬s\x0000*f_@2iÙ\x000b|QJ9Ùû 3%µÂ\x0003ë\x001b4\x0006Öy6ÔpEÒUÆ0¯×
«Í7ý×\x001d\x001a:myªå\x0018ÃNgMV\x0002z¯¦ì0½ÒÒÙ°#J$e \x0006ÏÎEd1ðL%? \x000bÛÐÖ´NQ3w«^øxswwýþæÕ\x001f®ï®¿¿¾½Ð¹m\x0013ß¤+dÃ^þ\x0013èÿÅ(µÏ­Èg?µë@T6ÙÂÇ{B\x001f\x0014q¶
m7Å,\x000bi\x0016Ünçºð
\x001aêÂeòµa\x0017\x0007\x001b °³\x001c¦\x001dCÜHÇN°c\x0019ØÜn> `åå±S^E{ûTà9KÛ¡ý¨Sð<Û\x0003\x0006 \x0004å,!¯ÙYsè\x0005pgØ0"±\x0014¤o
\JË&GPr¼åÞ´Wçà\Ãn?ì"	Ö"¡UÜFs\x001dà¥F]N3÷Am\x001ebÂ[O\x0005}ùpû×ÿgÂ¢øäÊü°ÅEHháµg¿odü,¼Ðùt4u
+þ
¸\x0015m\x0008"äï,\x0015Qÿû-mÇ\x0006¶4ÏmPpá²U¥×w,¸Ü]Ð\x0013vhüz®ÞHLÊ¢[Üp\x0002]F¦\x001aÛHøvèaä{îß\x0003è,&\x0013 CVi6\x0015hÁïÙ¡\x000bÔ¢G1a¾¹Wbª^Jj:tË¯ÌÆò}\x0018Ëý½·0\x0013¬á¸ùåÎI9\x000b mØ#Dî\x0000H´	óQ¬;¨ú>°Ãº\x0013qó\x000f¿p¥¼­0blØ¶¨S-zWÉÇBÍ\x0014£Õr\x000b2ÚToÇÞIõº5Ã#8E"cÈ\x0008RüBMw:sÍ?\x000cl\x001crÜIÐ\x000cq)\x0015ÉlÉ½Ü}AìÛÁ± Ãó\x0010Ø2À¹dX`+\x0012 ÜË>\x0017¤\x001d\x001b'öyr\x0006©MdYQæñ½\x001fç\x000c\x001c«\x000b¼Å$U¶<\x0005ë9(Í³&ZÁ<gd\x0007·¨\x0007ë\x0015´$#Q¹àTü°ûÂ'fÇÎ\x0012;Qk%Ã\x000bËxUµ½ ãì¬x<+®Ïr9°{j\x0012°%9RmqD?\x0005vè  s[èí¬\x0015qÒ\x0003¯ÜÓ?{àia0³\x0007þñöã«ß>¾yõ»ëÇ7ï.ÕÔÜQå;ÂVâ\x0004Aö­\x000fíÙßïuÄtãXí\x0005v:K\x0019?¶ÏC\x001aI5ÝÔÞ\x000f;UµïÐn@;+ÈûIX\x0005óJEW
¥:o\x001f\x0017"·ÿ×·ï?¾úöüá¿\x001cç	Ã{TZÒq¨\x0002É\x0013\x0018Âzö#°v&«åVEÓ|á¢åNä\x0012
»\x0000ðgKvpu«æ00"gÐ¿]Õöþ)RÛ±\x0001Ë
%\x0001´`FZNº\x001fµ3Ü¸9æ¹cCM¤e:DpöMµ­\x0006\x0011B1\x001cÛOã]7pï\x0010ÜV Ï\x001c\x0002[G@4%\x0015¾±k²±
\	/7­íªe2\p¾vX&ÓÃk\x001fèÞÝ?þDÿ÷7\x0017
}æ-\x001f\x000eÆ\x001aý8âll\x001fÑñì7í¤e`ê\x0010É[\x000c\x0010Å,øë¼kÕRC\x001aYÂ²\x0007´JâïÐhñ\x0014µ\x0008ÐU\x0008IÜÎå>÷µlÐ\x0015VÍuÌ0ã°Di%Ý4P\x001aûó\x0014üßÁ°áNIHbÒÛ"xÜ}®õ¿ß\x0003[æ{ÐKYJÅe;¼Á&\x0018Ñ\x0003KëÎJ$i¾\x0008¿é¼\x0014ÛEøêæ\x0018<òõõ7×\x0017J8z_0²\»£{QlìÃ\x0013÷\x0016«ç\x0017\x000281:ÜDðñ
°ù\x0010 ¹[ÇÛð¬È×ãJÉ\x0003\x0014gÊÖ^[=õ>ïà\x0005ÌNî"&\x0012®p	½	<\x0017§®L?¾þûÇ÷·on¸¾c©\x001e\x0007¡	ý»{erðv\x0007gx#Æ^\x001fmy¤ò\x000cÌtð¥º8ÊhI\x000c\}(\x001eÔ][oò\x000f÷?<Ò¿»åÿª\x000cC®ä³¶[gx\ÌR(¯ß~¨ñÛ¿àuøðê\x001f\x001fþãßßÏïAp«àº\x0008ôídÃ\x000cWúölªß'ðð0c:¯¯|¡¾\x0008]\x0012ÿÍBÎ.\x001e\x0004n©\x0017ußkÓ~\x001aÅd8\x000ft5
d\x00147øF.HÊË¡Û|\x0018w$&¦F)Ch\è\x0000Þ\x0011µî\x0012o*69SÏð©cõé®ÓÀ§Ó|Øwïrµ\x0002?Çã×z\x0002ñ¦ éd;4\x0005oz\x001cZ¼á;u`\x001aÕ`rñ\x001c>Z\x0010\x000fá\x001dÌ\x0011¾Z\x000eñ\x0008ñä$ð-W*eñúþ¿{Hò^üæúáÍ»¹Öñî3\x000eÒV¼\x000cç¶jbËswÑÄöm¶çK¸\x0016¶õ¤Î×B\x0015ýîâãk\x0011\x000eÛàì«È´1ßÜþÂ`c®_ýæþîîv¦¾û4}ÅL#âvÒi\x000fÇÙJÁ(§G½Ó\x0015?÷Æ\x0004ëb@2*\´7f\x0004è³¬\x001fÏ+}\x0016\x000f\x0003O ÜØÆ$ã´Æ\x001aø\x000e4VJV»?\x0011¬\x0003¡Qøaèøçëw¸þÇÀ&ÂqTavü*®<\x0019:\x001b~8Ç\x000f\x0003;Ü^í6mDé|¼ò±¡\x0017¬\x0007­q\x0007þðïºü}\x0002ùû\x0011ÆÜä/ÏdlãÉçë°~.ÞÏãÅ°\x0005&5üÄÁ\x0003
\x001a~:_Âõóø	ÐèdY±~i\x0002üºx\x0014¥4Â\x000fRiÏåÊÂñ$i¥Û\x001bFK[~}ùõüxV<!ãñ÷<Ê#¾­b{}öýø×óãYñx"o/o¯»\x0012ð±T¹»±Û\x0003ötùÖ:<y·±Z
£\x0006³K_Ý.úã
?iµ=ðÓPÛ~'¯Øð\x0003³<áé)i8¢¿5Ø&[ÏñkÛ;¬¥¶½¹ÊíÍj{7{æTüNh·µÒ~RãOïÎwßýåíQ½;\x000foo®ï\x001f/ôò$ &ãu´\x001a¼ãuê}\x000fªûÃ"(mÙùá±ÚVëòãaí\x0017â³ÆÉ
\x001cO®B"FÜÚ\x0014d¢¾\x0019\x0003>Fó)MÑWÓð£'·ö\x0016D=\x001eñ«X¾Ð«¡\x0002Cy×«NîhË\x000b';\x0019â\x0007¼5âY\x0018½\x0005dõG3z\x0011\x001bz\x001dô4
=ÛÞ@©\x000b\x0010Þ\x001a	\x000f÷ÉN¬|\x0015ä«\x0019SuìùæZÜÜÈégØÝ\x001c\x0007£c×KIìn4ÝÐ·Yßëñ^»,v7ôÍ{í|B®ºöÜ¿¦ìöúAÆ®ß¼Ü¥NE\x001c\x0001[#Üjî¦\x0019võ=Xöì·úÔÎ×\x0007«K¯3â`-?ëIL\x001bSïÒÍí=&®ï~ºÆ\x001f~ê¶\x0018iÑÆ\Ç¹åq\x000fp/Ètºðó9v%µryW¼\x000eJtÑñ®ø\x0002×1»\x0017¤Ïòu\x0010+t#V_÷OÎëgüÀw\x001eñèÜÕxÅI\x0019µ¼ê\x0001\x001f³D¯ÝDvÓ\x001aèx¦\x0018ýè\x0019ee¥	y$I)ÃÒñµ	ø`c2a\x0005U\x001eêçÒð¢¤)g#áúç\x001fÓwïæÜöÍ«¹þxsûpóñãÜÔjjF£é8Á9PÂ?íòÙOpnÝó¿ÂMíTn*=f|SJâ-/H¨Ý\x0004Rº\x0015jö\x0000<\x0000¸ª7Æ÷5¹	Ü¥,ñ7'ÆéÇ|à2f\x001fÙÇ;¯	t¤õsÊ\x000b|úú>À\x0003?%Xò£Çí2\x0018qÝÖ­ÃeÝ¢\x0003\x001f¢ggêÉ\x0003Ù\x001d}Á\x000f|;\x0018NH>ÈÀïKÌ0¤É\x0007¨È\x0018?Ö<íb½ûÓÃ-\ÀÛë\x000fsJç\x0013¯\Uö9{&GlËq\x0001üÐ®.Ø6üúÙ¯Ï«@¶Ö¸K®pãÆÑãÇ\x000coúª10áÚ\x0008<ùç®u6\x0011\x000f|H÷Ô\x001fôJì\x0019ÇÑãÔDî¬\x001cøir2AüãÛ;á}yK_üá\x0007#\Fá:²û½ð\x0015l8\x0012z>sÀ¿6r÷ºû~Úý&BÞ}?v¾Ê\x000eúCþ*àih"1EJ¤±\x0012$=?\x0012àÝH{n`\x001eÙ\Ï¨\x0011Yâ2Ï`CãÁ?¼·vïáÆßÝ¼X¼ôÞ\x0003¼å¹!ÅC6cx	;\x001emYÔ}×­_©.¸æËY­äI)\x001eH¬ZòÄ\x0006¡å«í\x0013\x000f×\x0017~à{ð	3Ýð8öÜ\x0004`&h>[vÂ.'µ»ÌS$òÀ·"\x0012É½Ç+[é\x001fED!\x0003ïYÏ½\x0015]¡æ_ûï¾ùIúm
ûR¢ÜËB,ÅìÓu|à)A	vÀÅöì>ûÁª­\x0017j*H¬UW]z¯Mûi|\x0016Óºçy,få¸ª^È¤WÓ¦Éß~\x001aø<TgàTFgAÃ¡(ýà\x001eê1Ú»\x0001üë7\x0018\x000e!zZ\x0011æÕf\ÙóÕ[\½\x000fG©\x000f	\x0007Wz\x0001.\x0002èôW-ÿr\x000eï\x0010~}¦<íÖym\x001b\x001eøÀdHød&që2í\x0005Fª2ë}¹¹[Xã þ\x0018YÉâx«ï«\x0016!\x001f	OÆ|ô;wÀ;xçèì¤6õ80«Á*ö¶0µþ\x0014 þøð·[d\x0006ªKe£ò\x000e\x000cØÑVPª+~&0xIoQÂMvÍã\x0018º<19IàÑxi|º(
\x0005\x0012hKËèS5ðk\x0004|²?yS\x001a×i\x0015øÂÞ§§¥öÈ\x001c_Ýñ\x001dÄWÛ¶dpø¾e[~ðS±ýÓë?ü¨Cøý5Sc\ª>Ç[/üf%;JAè*xP\x001c5Î/)\x00146tùµ¼\x0000T ØT`g*Ð¡:¡ÿ@\x001c¬Ú'<7iÀc9Xà\x0002éøYx5Þö
¿\x0007¾£¾\x0018\x0005:\_6.FÉ"ÈcåSç{¶Þ\x0016}/\x0006|\x0001mËS©3Àó¬TÄ·U¾FÕNUþþõGsý><ûûûÇo¯/\x0016¾MFøtGFäôóab&2<^6\\x0007¿H©è3ÛE×\x000c(¬²ntØ{®ª\x0017YÌì öEBä»	¢ÃÃ;~:&5©Õ:fùpü¶¨\x001a\x0004¨dî\x0001ÜÜ³Ôæ\x0014ß\x001aÄ§;3ø¯Yj\x0011ßa\x000e³nùOÅÀGÏKË¡F#Å4\x0006\x0011÷õË,;\x0019l\x001d^ß9¯(~\x0003¹8ªbDM
Rú¾1(\x0019s.,ó\x0016ÞºJ\x000f¡ÌÓE\x0011Òá·éÎýåg÷·?\x0019|,^ýþöE\x001fÕ§\x0019!dË£käf7OÇïjä|È?n\x000fÇóßºJÎ¢ßð.<¾\x0015e¼á<g
K7<Ï3wð#sV¯ü)]×N!í\x0003ßBH»M_/P»Á\x001d`ãX#Ý\x0016\x0012yîOÅdã\x000c|°q2ùH£-ðVp$¼ÙãwÚ±8à\x001dx]ÜW%R°Ö^E(é³N8EäÛw¿ÂYít
x\x0001é~ L\x0006[H\x0000ï]u\x0012âñ¯ÿäß[{=nÅÿzOçíýeò»ÎG/`<\x0010x_~©É\x0018QpÌ\x0008_BLø,½;Õ\x001buÑµbx{gõH¦MÉªïþò#nÊÇën\x001e\x0016s\x001b>ÍB\x00081'\x0011¨âÆùý\x000bl-	ÎUqô\x0005ö%TÓkÖU]z-ö5t36@°¾8®7$$\x001bd\x0006Åø~Ù§(Âï ÀYúAèíÉOâ
¤÷»\x0008»3¬ìÂ·?ÝÄ¿
æÛu\x001bj¤é\x001e¢=¶=\x0006òf]KOúË\x0008Ò\G7åhºì¬èú«ÈBùóÇè~]¹x;O§ûÄ=N{¤=VÏ\x001e&\x001cÚ@fV|Á¥î¤ìtn£ï¢\x001b/×Ùg=)yWn\úó·"¤ôëoï/Têî8Ü/\x0003\x001c¥\x0011½`ö\x0002áázö93è¬6ºôÚã\x0005A\x001ffÑµ\x0010ôá\x000fÇ&\x0004þp\x0011T²
82åÌ\x000eü\x0002\x0019ÓÈ³\x0008 ¦°\x0012à\x000c\x0013Gzº\x001b2åÌvx\x000b93òjê`ÁöK³X¾UA¥\x0014{M`\x0012²\x0007~,S#\x001b\x0010Ïf>\x000e|'C¡±Ø\x001ejú:ð
ð³Ãü\x0012\x001f2#ðmG<ù
ùáÁÿµÊ \x0018\x001f¯÷êÍIRÙÂ½(¶\x0007ç÷`1Sg¾{±¶\x001dÌ\x0014«ìÂk×\x0002ö¥ÄÞòq|UÀ2ÇlÄÂvè¾¿ú?\x000et\x0007ý\x001f_\x0014À{ß\x0001\x001esÖòÖ4{tÞþùû¿|£6ýöúR\x0016£ãù¯Âb¤\x001e
Y<»Ã\x000cMµ¬?û®\x0005B§¢.¾ÕÂë\x0012fÍÈÃJM~!Iñ[Q\x000ek\x0000~\x0001üõ\x001dí²\x0018oDØ$eß«öLÙ\x0003?cGÍXTU·Ñ§\x0007>û\x0001býýÜ)i9à!i¸¦ÊBRl«,µ0­ò¢Õ}÷&½úvd/\x0015\x0005Î<\ú0¬\x0012w×A\x000cÚ÷ôè=°S¬\x000b®m8\x001c(úf+\x001a¯<Ä¦kQÌê\ÿÞñ\x0003ß\x0006Øq\x001f\x0002îxõ\x0016ÓÈØÉTcéR¶è÷uà\x0017x_	\x0013¢ Í\x000e\x0019ñe¯Kâ²À\x001e9Ã\x000bÇsä3¬ßDÑ©ÆacydÒÜ)ÿúÃwoþú
ÔÄÿ©®ßÜ¼¹½¾Pü>º Ê<rH£´&\x00031±Ì3ª^B\x0000ÿ,éõÑêòk¥/ØDHgi\x0018Ôgt\x0000u¬U\x0006ÀmÏfzmØ\x0002|\x0004x#Ê»3ý#vU³.\x000b\x0012¾OÅÒd¦Ð2>GtGR«\x0016ãÑp¶¤ÅÉÊÅÔE[õ\x001bóá}TøãÃÅÞðXE\x0008	À-X!\x0006¬í\x0003wûXk¸ÖIï¨NLtáµ'\x0016²ä<Û\x0004B°6¦+|¢¸ÄRH¤³^I\x001f\x000etÔuTÃ5ñ\x0018<.ÀäÞk^:Ñ)Ú,\x001cà\x0005ÌBr=°,%2wÂ:(Ê:p½Ê\x0014í,\x0001>8K9'ì7·ä\x0019Lðw#\x000c|OY§­§\x0003ß:°èÌcMSq¥ùf\x0007¾J#ç\:|Ð®ä\x000fàJ²56\x0012fm2½¾ñò©p½(ÈÎÝø\x0003\x001el§Ä3\x0000íÄYä®j\x0008ê©°¹/rõ\x0006>ºz\\x0005\x0004,\x0015YäãØèWYä6\x0016Óso±:\x000bè\x00038\x0015É^yqv&\x001f®'N&?~À£\x001fOO\x0014ô\x0004\x0017òÇ&\x001d\x001fTMP/×wSKùï ¥ÓD=\x0019OéBC ¨
-ã\x0016¬ÕÏ\x0001àC£põ',§wÌ¡£Ö?ýò¯Ó·ñ®u¬â×·÷\x0017«¬ÅIs-·Òí\x0013¸Jczìw¿BÈW=¬x^ËøÁÆ8[¡W¾:¸VDª*eë\x001d¯Öêc5Ð-\x001c+ÚE;ÖÐ\x000ex\x001e;))[iË9>0	pM'æ\x0000RM¢Ë^\x0000©è/ØjOÎñ\x000b¬ßza¿ò\x000c$Ñe\x0013O\x000e÷au|­ô\x0000\x001f\x001eÛÇ\x0011®\x001dY1ÈT@ö±i+ùÒJéwP>\XÊÂ7©Åk»Ê\x000cÈ\x0001\x000e\x0006$\x0019ú\x0001cg9ÀÏvtRï\x000b¶ÊÛ\x001f¿ùá£¼Òw\x0017sIm _\x0016åUX`\x001c]Åèe(µ½Ï~¥×1e®÷Ó½Mz­4gØ1/Åh¤.1ZÑ\x0006\x001e­Q¹O¿ \x0010­2\x0000¨\x000cò
E(>FÙú\x0016¸ùHâ^Û\x001cÏðÛO\x0003?\x0006hx%ãDmvPmìL§ÒßÒåÀ·@ÏÂ\x001c\x0007¸Ò/	ÙÊ¾½z²Ñ\x0007¸l4Ç¨ B£p6Ìd\|(R#Å0\x0007\x0017ß¾»ùÃé37t>^ªÛ¸:Õ¾1ÿ¸\x001e¤oÓ<~ì%eÀ¦CÛ§*OÎ>ëIÌÑ³7ù¿øêo?|x¼¿PO\x001f­LÖ\x00103Òpy«P¸L+ô"zúN«_õuìâk×\x001d¯£±ÐªX<½áQ¨\x0013#¦\Ç×²çøÀË@ïmÀ\x0018]°Âm´!\x0004é6¦Î¦£ç\x000e\x0000ü1y i[½väV¹ü ÉÒæÚlhÀ\x0003ÙPnÃÄ\x000f}\x000b\x0017¡ÓHçÃ 2Å.^Ùï??#­âõ«¾óîB\x0019õLfäÌþ8µÖ|\x0014\x0019åKÐ'ë\x0006¢d¦mïÂk=,PÿÊ¢#CU[a\x001b6àD¯h\x0003C·lMÕû>ð+ôÈøZEC\x0004\x0000.yg=´S|îÀ·\x0010\x000b®º1üð¹\x0005ëw£1jý=\x0015b'®\x001f±\x0007Ç×+xg\x000bYY¬?G¡oÉåÜîvç\x0007~6ï<ÜB¬?NQEÞ÷`Ê\x0014¬\x0019øE´@%ô,"x õKÏ¥\x001cÝ\x0018Úz>ð\x001dxFçP|ª
¢3vS\x001aQuóç§@Ù\x000f\x0008Ï\x001c_¸½\x0011ýyZ¾-bwgfbÿúÇÛø]A+¤
7úÃüûÇû\x001fîïn?^ß¾¿yåb#c¿\x001e´\x0001N}óá~Ó×\x0005\x0008Ãÿ\x001dÚ(õg×#k»£çj£º81
¯ßÉg=)¹ëøO\x000fß|\x0004r?^ÿts¹þÐZ6"6²
:\x0003¡¾àÂE£UW[\x000bêâX\x0018XðI¼¸Lmæe\x0003¾@ë9Ð±ó4Ó\x000bîÁ{RôrÌó/¼³X\x0016´£÷?¿O\x0011%È\x0010ý#Ïª¸Ðû()ú¬Á&¬l0üË¨¬?KMÞe×ò\x0016°é¶`Og5¹Ê¦K/L&àV¥ÓU\x0003¾\x0000\x00053\x0007\x000fYÂ\x0001,qMçÐO:v\x000f|\x001d»+@`WØ(Ex/lèlb«.¯ÌßÝ?ÊCõøæ2©0G\x0006ì\x0002«ñ\x0008Ä\x0014ç1ö_m\x000c/£¸ïÌçL\x0013AP\x0013]«\x001eºýì³É´+ùPÞ@ìß{ýp©^¤1NOe\x0014Õâo%\x001aõ\x0012®úYÃÀÔ¾Ýe×\x001cB\x0008y¯¿êIL»r÷öúæúû±+ÿ²¦úÊîµL\x0015áL±ZÂ.©`\x0003ê^íKu±5Ýý¯lËCcµWf§¸\x0018È»ìñÄ)÷4à!÷ä¹71cæÆ\x0017'IWþ§:è þÀ\x0007¦¹¶|¤êF[ õ\x0017\x0019\x000f%{|:PßÚoÞX¬'¼~õ/\x000fÜòáR\x0014mµ*Æ°\x001cFA¡g3\x000e¾¡öúÂ\x0017{²¦f.¿VG
iSG^4|VæàlB(Sú[þÉdmÌ
ü9\x001a%þüHßdÙú6¦i;¨\x001dð\x0016HÔ\x000825¯s/\x0016Õ\p'\x001b\x001c[ØcÞÞ`/ÅÍãd]¨Í}\x0012ñ1¶³Ä\x0003\x0015ê¨U%C§9îÏ~´Î¸§.Á¦U uG\x0005jpii\x0015©Ç"b} 2ÊNáa*\x0005ÿ\x0003Æ7¢ÍcÌx\x000fªòÝå+ø|ùÀrÈ D6\x00086\x001fea¡(Ïb6Î^ë2\x001c\x0001x,üËAäx>(&\x0007kødv{ºêÌ&àCfÓðT<(ÜwN\<ºRøÞõèUèvxþ	¤0[ÀÝÛòâE+/öÆ1î¦öí\x0003ßyLÌÚx5àC)R-1¹H\x0003ÔiÐ»ý\x0010Þü\x0017.Ó]Sx©\x001d³â\x00112f.a\N©Ìý\x0012ìÃõÍu
½v\x0011¶LÂ³åDQ,\x000fü\x00157[Â\x0018o{úTß<^,Æ\x0003fÌLW\x000fjnIä^¥7£ÙðõÕ\x0003ü"ñÁ\x001ca|qõTd:µK\x0010úä\x0002:ð~Êl©Îûp&ö\x0013¬Þ¸¨+[y½:[\x0005átÚO#\x000fX`.7W\¤6\èÀ§¯Z\x000c¶Ù\x0016Ï7ð\x0013ÎÞâ\x0012m'ïZ¿,3a\x000eïü¦/y°~ÿÃ«oÿó_ÿ.Ãíe.6=(²ã/ú4rÀÞè\x0004!°ÜÐ³_ì3ÂÞ©[í\x001b\x0012`3ÓãVc.E	Éª\x001eÈdåa77 éµ£'8W6bu\x0018Ó7\x00035\x0000¨ëÞìl'\x0017i\x0003·è ñÄ.¨Lå!TvÚâ­luæbÆ^¦¥=¤\x001d\x001dz\x0010	½^ÁSe!xñÞDùÖ¹wÆ²¾°t\x000bô\x0003s\x00178ò$G#ï\x0003[úõdO­Ã=5\x0006sÇô)Íh:ÐÊ2Å\x0018æ¸×o\x0018\x0000}wÿ)²ï®;Ëââ_Lï-"pÎ\x001e\x0014AÅ\x000cõÕ5\x000føÙïÛiÍÎÑ}cRË\aè§\x001fõ¤D\x0016{ÓH÷½á
éüå\x000fßÞþt©p\x001bÕ\x0005éëâú£,Ù6F\x0017»5iÖ'Ù5ó\x0016ôÉÉG=%ÅÎ\x0014£væcáû»ûÇK\x000e¦óÊ\x0013é­êGû´¨/å!î\x0005ï	Ó\x0008%b3Q°\x000faýQOJdÞ^»m\x000fï	]Û;þS\x0017Ê\x0011\x0015Y0³9µý\x001bð^\x0013©àòÙ\x000fS\x0007Ä7$½¶-@£ç¬½ÂO\x0012ÔH,\x000f#Íö¼\x0013æÿÿÔ½ÛXGr%ú+ß\x000f÷Ë£[m÷\x0019ÃÆ\x0008Ý_\x000e\x000e¢T-Õ"Õ¤è¶\x001b00¿10þ\x000eÿÉ|ÉÈÜµòÂî#ÖñË´JZ\x0015;#2®+&cy\x0003YJPfsh\x001b<v-_à\x0012!2ßf9h\x0000Òt¡Np¨m9±Ç[>\x0014y>Ù3ZÊåp\x001f&ú@·àQ\x0007]\^\x0010}\x0014L¦|zkªï\x0005ÓÔmE©;ÜEWRæmb\x000bæ`æXþé6G×\x001f\x0000¸¡üZ/\x0013aóÁãbøÿW\x0016[$¾~ü·w/~óîíûgJÛj\\x0018]Ý~Ï¹§MÜ/¢y£gSoÏ+[ÚmÎ\x001eU:È\x0014õ"°m=
Óù%ù#e;½|'8¦Õ
\x0012kèÞJ\x0003wC¿ç\x0019æZ:\x0003\x001aúOtnç_}~ÊôÚÉ\x0005ü©>A
Ül%ã~¬²cö±ÚGtì\x0014y\x001fèÖâÑ%Ä­tÚ~\x00160n­5\x000fg?®§Ñø\x0013=cT¯-Ý0x¯­«øQEk¹Ä³âÖÿ­À²ñõ»\x0007õ\x0004óáéû\x000fo+Û\x0015)©*ß>ÜA±Ï_ ñYþ"­n}i\x0011Ì+ß7Ã\x001aÍ\x001fõQL\x001fÆôu[gØÇ#~ú§wO/~÷ó_?¼þñáý³QcX\­\x0017ïä`¨\x001eic5-VþR?ê\x0001*ÍöÆÙÚüQ\x001fÈâ3Åñ3}xñµQ]÷ë+=ÓG²)p¹ÑäûÏ\x0011\x0016ò\x0019º¼'}	ßhÙ76(ßÇ`\x0005»ýA0)\x000f\x0001\x000f¯\x000e[çuß[_76u\x001bwôö\x0003\x0016\x0017T#\lâBô¡Å<.\x0002\x0002çÀzþîáéÍÏÿ×¯\x001eß½Hú"j\x0013'b¼û\x0004u©-0úè
ã/XmÛº0=É"¿¯&(k0L\«×K´Ä
âdxJÇ"ã8=\x0007z¾\x0002\x0003¡Æ¥$¼¸!/QÃò9ó;YþîÀòä36ë:Ï\x001dÂÕX\x001ep«Dµóf¼TÏkE\x001c÷ffÁZúcµ04^¤/!ú¯y¹ý|Ú^ñJ¤×²Ô\x0010ü\x0007hoüùÊ\x000edíZzïÍ*S4u¢{´$\x0016«¾¹1ßØ\x0003\x001e1ZG9¥\x000fì\x0004mUÃxR2¹æLCcëÑÆ3Íâè8\x001b]æ\x0000Ù³uç!bvã¾;;pÌ+[\x0008ÊEÀ©Ük9(ð»û¾~6\x0012
ÛzôÛKj¤@'øQ4½åR¸¢¥éõF.\x0016;PÚ\x0005ÒJ4\x000f_´GöS)ôÄÆBhÔ.Rä\Ä`Æù¡¢Q{Xï&ô\x0003Úy$\x001eÐÈy8\x0011\x0007ù-Iuõ¤y?Z¿{ûþñ§\x001f)1\Íx©®}l\x001bÀ%óùË^Ë:õAËgñC\x0017tLh\x001atJÒc8 Ór$p¬¶Ø\x0006.tÁôúä\x000e§JµãÇv)Ó\x0019JÌ´âD5\x00141dª\x0005i\x001dËgüÁ\x000e\x000eéÁu9mé8Ð-ìèö\x001d þÃ£\x000fdÃò·._Ë0Þ×¯¯o?ÕÀ\x0004äÖ{|´^<S\x001f±·®}ö\x000b»c\X¿\x0013)*/ñ(LðWÝÝ\x0002©\x0016¢Ê&¯~ñÍ{î\x0011v8è0N¦úZÚ\x0003w£[ÞÈgãb6G>z\x001c?úïþó?^=¼ÿùéñ¹&ºCNì¬åx¯ß-z±ôø"xßwYÂ9u+"l\x000bìr\x0010\x0018ûã¢ÅÔmehoHæàjZ|øÎÔ\x0004Ê®M.ØÖY\x0002-\x001f©×,h:¾gÚ6'·\x0016O.>Ø½\x0003A,\x0019û
\x0017VÜ1<õÿèØý£ËÔ\x0011Åx\x001a4©úÖÒÑmgäuÓâ¹\x0003ÝÁÚ¹X\x00024é\x0012)\x000cIäO\x001b¶\x001ew'Ìí\x0004ãH0(Ô'(0è+âBÝ\x0002E$o?|ûðâW¯åÒ=\x0013Y`®ÃÜ\x001c\x0012¹â¯CûR*¥µ\x0017}v]Û±\x0004M-î¯\Ï>a»ü·ÀéÖÃ9T:Êæi\x0015ü\x000eE\x0014\x000ctÎdñó©ÀSm\x001eÊGóÕÎµÔ\x0003<à,ó8}.þ/¥µÆ<~LçOkÚ/p\x0018ºJÅÐ\x001e@ÝØæ>vSÎÅ]sÕî@O4h\x000cW\x0019ÀhKb-Ü­Ë;ß>¾½ {\
JEfmA¯\dÎátïç't÷\x001e\x0013#\x00077Å\x0015ó\x000c+ÇêHU»,a»îÒÛ\x000fo4C)zð<ì¬µÜÙÔ';\x000fâ\x0005[<ÌiV£4\x0006_"oF[§îÍW"¼öÍo\x000fYî§mÃÅ\x0007øÚÚÈ\x0013"5Æ>Ó¾H5t\x0007É0Ý\x001bÁ,o~pV>\x0013Öj§ÝäGúæ"zz¶6,	vDy¹÷Vêz\x001f`òPê|ÿ%\x0014xÖÜM¬òQ:ï\x001e&\x001f\x0002Ñ<Dqa!(j\x0013$åqòúÍé¤\x0003\x001d÷±û|×Q\x001dÍ@èìw²TóÌüÝÃ\x001b­ =ßw·b½\x001cÍ×Öæ{¶\x0001i9MÝ3n¾\x0004]ßå¦ÓühÇ¶T2Á£íäïô ì¦ÒVÆ\x0010mâ®\x0016¯Áõ\x0007 1KÆ²Þ!aØøX'¹9¶Å¤·K¶5L_ß¢Ð sàw6'oÅ!Ê×o¿}x­gâµ^¿øõÛÝ7Æ$ìÜxýðíã¯\x001e$\x0018î\L«;ç>~çLH@n­^1W5ÙiöáÚQì¶Û´8¯Þ¾yóÌ7î

ëî-è\x001f\x001e_üúñÍöú½{Ô8vZé÷\x000bE¦\x00114,GÌæî\x0001\x001d"\x0013'sìJÿrDfS\x001eïÖß=YûÍÓÛ7S·Â/\x0015\x0016\x0014}UXâÕ[XÞ_K¤EXâ×6¢É/RX}ßÕIúáÝûÖHú\x000fOï\x001e¾]l\x0016þ¥êhï§NÅeïF*§ÌËZêÝ*iÌæ~AârÐ\x0012ýëÇ÷ß>¾QLØó{}&Gb\x0011\x0006¯Ä¿/X\x0014ÿî$®qJH\[Þ)±\x0004u¯\x001fÞ¿ø¾\x000bìë§ï\x0017\x001b[~é\x0005ó7µc·÷å¶÷1Å«{«Ùûðå^0oÊB\\x001f^üî\x000f\x001f\x001eæ\õ/¾\wý¨].\x001b\x000b\.sE*íru¡/TZu4õ¿{ûÓ\x000fO/þþá÷¿úùçgX\x0014\x000b÷Ë/e\x0017o\x001egWr
ê?~\x0012ûëNävHLN¦ÎþW\x001fÄ¿}\x0016Q%	âb\x000chë},×ÞEy&uÂé|\x001aÈ¾7\x0001ÿï\x0017Õ-Û÷ÿñÃ§o~:ew\x000b¥\x0001Åñÿ\x001còøQ \x0017^ÿãÄ)¨àWVRËdÈÖÒíòúK~ú ÿìIÿ-ëÅ­>Å'ù¤PgÜ2Qja|óæ}}ó\x0008^6¨µrÉ£Miæ¿ýedª»GóE\x0006ÁúÿÖy^.Êo¹\x001dI<ÿíÏÚ\x0004£æ1ÿ\gÚ)AîMsÊ8Öbþó\x000f
\x0005ènD\x0018ánìUa\x0018Q\x001e	×Ü\x001eÛ\x0001vÈ·K^M\x0016«c\x0008ÜyOÎ\x001fÝïÁ=ËUö\x0000n[\x000f$ÇJà¥
J=x@ðBÁEm\x0012\x001b\x0012M$;íÁ\x0013_J¨à\x0019ÉÄ\x0004ÜÖ@à±¨Ìó\x001e<³Ìáfg±Â£'wOÞv6=xAð;éÜn\x000ev=øÍwß5§eúë\x001e»"¶£¨ØÀ}]\x000f+\x0003\x0011ý^\x0019øK¯¹Ýëýd\x001d²û{ný'Ç=x\x0004p\x001f®|{\x0003uR\x0001\x0007×\x0006^&
\x0019÷ÍïÃ«ïÌ;¶Ì¿\x0016;üöéñ_Þÿó4þ\x000bÝ\x001bdTU÷Æ×ýÓå áìå\x0010fíeÈö³eQ­enø2]~úeî/yxK¾&ôOr	{ºE\x001eÖ[Gî\x0014,ã\x0005ôûÆfÙO 0]¸\x0002&(fWQ­8\x000e
}¼²î\x0001½V×<Ñ}Åyîéì%©Ý¯£»Ño\x000c6Z\x0014@\x000f¸UO¹\x000b³\x001dÐÕð»º\x0015¼« øX|{¥Nø°\x0000o¢fþI4Þ«é÷qÔ¸\x000bÞßë\x000b\Ö%µ\x0011<qk9XàË\x0000?Ïº¸oòÏïþÛïÁKnqÅÏGÿ7ß¿~x£Y·ç\Kà'ÃÇ\x0004«Êçz)­vÁäðÙU/º(hºÑÅ8xD)Êíùþ8\x0016	Åá\x000c£-m\x001c="ÀvoÞë]Z!\x0014±\x001dc·ÌQí\x0000Ü3øYVUðbÚe\x0001\x001e\x001aUþè\x0011\x0001x`ð\x001c\x0000W\x0014ÒÙAwG+sÌ\x001e<"xyyß!¥m\x0018\x0004\x001eùþÕ¯\x0005È	ýÅî§ÐJdGØ6²LR®\x000b_\x000bÀ3\x001f¤\x0005\x0017xÄ´\x0002\x000e+ç\x001axn,é£¯\x0005à\x0005Áï¶
\x0005wþ%}LØ×Ö±\x001bÃøèk\x0001öík¥¤\x001dLéÆVÒ5àqÐø62¹Z78¸Zº\x0001\x001cs8
¨\x000bx\x001a>gj\x000b`&_\x000bÐ-¢ßT¶í\x001efdèQôÊr	Ý\x001fÚë§uîÁY¬W*ô 6\x0007=¹qì\x0011ùÏ\êOª\x0003x\x001aI½Ü7?þéÇ?:ààýêÇ\x001fÞhòí\x001f\x001f~|ø·gJ%\x0012<¥sN\x001d.£Oþbh÷²¶¾ÚÏkðuFxaðÃhÛº\x0000õÛ\x0004öäÿn¢Ê§éîã%\x0012Û6g4f£¸Ñ#Dd"¼-®)[%+arõ¤\x001d|_¸´G°ió9>ú-ÕzùFO\x0018\x001fòV|Ý3òUépB!ó\x0019M\x0003\x001fm3'<zl±é¥\x0012ÜDùß\x0014\x0006ÚwÌî¥Hê79æñ\x0018ÆJR§Z¢ ·£çýÑ3\x001cÝ\x0015wuÂëÉå\x001d}RoZ{TÙÒ\x0002Ô¥\x000c_£j¤-2Ú¸=æ[÷\x0000\x001e¶î9}_[2â¾ 5¥rCu\x001d%¼ïáêhBoxïP4	\x001eE£K¯ÑÁ5J
2¿-##\x0003 \x0003'ÃR²òvÐáå×±Î¡}VoÆ·ë÷Æ\x000c×E¾kEmÒN\x0011º5¥õEø)¨»á\x0013ÂÇ\x0004×ÆÚ2d~²
¬¬^.ìO\x001føô\x0015r?ÖæÄ)ÌÙÝ nZ°7Ìd	W\x0007Ó]ß	\x0002\x0015ÞÓÃ¼­
~«S! 90\x0005ÝWW\x000c[²\"åeSn9·\x0010÷ð\x0011ákïv½ÒnN±T\x0014\x0008©ªµ{ÑG\x0014}ÐÆT¸9â¬§ÜK`\x000bi÷²[Êì·ðÙ#¼.\x0010º\x001d6¹ÔÍÅÚ&ÇrnZy/ú¢\x000f\x001e-h\x001broÑÐ\x0003(:Ü\x001cÙÉ#¼à\x000b%ß4ÌIðe=6ñ
|á<°¼·±Áo-N±f\x0016#`\x001cÜKGÞ¬<ZÜðäìËÞ^\x0016²\x0002áôÆ¼dôáùÏ£èq/²©õâãTÑûÇþ+\x0004:ûNÙßú·>@îCèvÚî7ÁéSpÝâ¼úÉùæ\x0015èF=·t\x001d´¶ò/Ð
ªÝÞoü~Aa\x0010ùW4;%Gö\x0013lì·gÿ'ÈÏð7hú\x0010ì¦Ó'+±ò²aöø\x0006ûß\x0010\x0013þ(ÖÆÂ\x0015uñ%=¹Þ\x000eBj®\x001cóácÂÃs\£?ö'ü\x000c{\x0010ò\x0005ü
i0Ï¾Q»ÊÇüöc\x001fú[´¡\x00012ÝV'
½í+:9å®ii/%ù\x001bPJö\x0004)Y\x000eM²àó\x001bJw}¶¿A~¿A\x0005_ïl}Õ'ýÄN­¯¹\x0007n{ô7 :DÒh\x001dj\x000bh£»\x001a\<ü«í þ\x0004ñ»üÖÉ\x0003\x0002Çï!ôwØì/«\x000cü
ZA>ïÍ¸@I?Yfe³¦{\x0011a\x000f\x001f\x0002ÁË[ìÁ$Ecªò\x001b\x000c«B\x0017´7yò\x000bð\x0013(«\x0005{ÁFÕ\x0014\x000e-_¼;*¯ÞÄWùF\x000cvµ\¤HM£ýKr¶¦«j'y¯Ðb2~FWºà»æm"\x0016WÚºA\x0019Bÿ
¿ÿØoø=ü\x0006%ö §<¨[\x001e~ÚÕ1çño?ü)<@óÃ¯ßþØ6Ëi\x000b¸6(ñqO\x0011<GÉfC¾«W'¸K%\x0005üîºº }©e¦1Jîb\x001c3¿è£âXd0\x0001¼|2ø\x0018$\x0003xýdðÉc½Ñ1ùKÑÇ\x001c& ÛOG\x001fÝa@w>jÝ\x001fþõ{û\x0004{AîFÒ\x000f/þnæoù¥\x001a¨Ìèl¹ö¯ËßaÒ5f«]~µs¥fmÓ÷éÏWºøÆÊR17\x0007þEI$ÄMë~\x0018\x0000÷\x0008\x001e¯ùØ\x0006^¸ÒQC±,ëö`y@\x0000õç¾ÅG?ä¢\x0002àhL¾¨ \x001b8­á\x0011ðhY,­²4	ÀF3a
µVr¼\x0005Ú
ÐiÜæ%Ïûç?ý\x0000Û¼z\x0017g'±û§§ïß<,è<aæ=ù¡õ§Ô;ó®®\x0012t&j;ÕúúúÐE8ö­ÿ 
cQi\x0005l÷©Ø£ª\x0001¶ÿTì)ÛpcOÅ²ù7vüTì)Ñpc§OÃ\x001e\x0015íçï_g¸\x0015M·½ýÐ¦\x0016\x0016³~¿LÅÄ­æîNç¯>¢è²¹\x0006×ôÈv¤\x000cû\x000c*v´HO*VÆËÚÅ§\x0011c¹/ëîoú<¦\x000fóêÝÿò\x0007\x001cxüùéç\x0017Gïÿ3ù\x0002¸ò»ÍG|\x000fwi¥ýJ=\x0012]\x0019IJ>Ç©5,(JFûÔ7uÔp7&è¸m¯7Â`\x0011Gëï\x001a\x0008c³VÅ3Ë M'ö\x0005L¯LÎñÎñ/<úä¾\x0002ú§
f¼°þOÉý\x000bÎAAã\x0017Ç.k%Á_?¼{%ðýÛgj \x000fÙpKf¾\x000c&\x001bîA2]ùjÆU¶_®OÛe:ú´áhÀ8ÿ"Ó÷ÞÝÂðCeÂU»\x0014»O\x0006\x001f
#ûO\x0006\x001f5\x0010ÀA\x0003Ã1JÇHY®VÿáM£õ\x001bßq\x0000\x0007o\MåNcF%jÌ¤ÞÁëÄ÷ë¾I?üÛ\x001fßÀæàÿòãOêÈ\x001e~í¯\x001eß}ÿøîéÙ:JìPô
\x0017'³f4ý\x001d\h½»w\~f¥ðe5^?*EâèØz\x001c³Ñ¿hhÂ\x0017\x0013Æý\x0001G\x0011|\x000f\x000e­ÏwãA-k]CÈ\x0010Lc¶\x001a5\x0002Á¯õ\x0012yÁwÐ¥ä\h\x0019Züzcí¨\x0010\x001dèÔ/Óí\x00135>j¯\x0007cÇ¦l£>\x00006øµ^Y\x0001@ÜÖI
¸·äãøÜwwíÁ±nìhZCþf\x001erásû^1ª[7¸åêÅ¢È¡pïQæAÈàJk7Íc2\x001c\x000e)\x0019î#uª$?ÖçÈT¸ÚêBy|ÇãËeoéâ¨\x001dÏ\x0014ã	ß÷Fò<Ö\x0008\x001fjB>:H!\x001b%\x0001dW\x0012Yïfgàuùî÷üÓmé~ÛxcºûíÛç\x001a,Ô×#'²êÎ¥;|Fï|TDj}æ_dp§êu\x0017¢6\x000e@õz÷7}T Ó÷±ù¿½{óúþ>-Yoeÿû\x000fß>½}¶\x0019íóãY\x0019ïÏ£õx|Ùs{´Ïÿ%£}]Ã+$¡
ö\x0019¶\x001aôU±ÍÉqL¾í\x0003p$-ö¥\x0005»b\x001cU´çj°röª]LcÚîB×\x001fÝ\x001fÃkU~È\x0001wãÔm\x000bm\x001e¯í

Â[´Z\x0012/áÊ#ç±'Û\x0012!#å2¡¿¢\x0014à&ÕB&×«Õ$ø¾üÙæñµ\x0003øð77[÷4ø(w¼\x000eð½=pjm\x0004øð\x0006ª§mÂ5l\x001cYs4Xç1Ù\x000bð\x0019à	\x0002D\x000b²â)<÷\x0002éªÀ\x0006?Ö\x0000¾ |º?\x0015>ÕÖu}ÃÛÂÖ·âµÍû{ñ^ê5\x0007á[_\x0018\x000foK\x001f=Ú^\x001cý\x0011Ýzhl¸,¢Ç\x0001^g7GkúÇoÿÕ¾º­é¹Í½\x0019Ô¯\x001eÞ}÷öÃë§ç£µ\x0008\x001aÛ\òî.áø\x0012/Rá6n^Z¢ÿ|òäp£ñè¢Tº\x0002éÍ\x001fõQL_)¦ðêÃûû+5j©ßë\x001e¾ß<¾Ðëý¯ßþøÓ|¬ç*µLtS¾^¼¤.Oô#m­ògûvßiøH]S©mý\x0017}T\x001cÓGzüã?Ç7o \x001fýøâWï>|ÿáqÚøË>uÁ³{\x0014®ýé®ñKGð­Lh°/ó£X3¸.<Q\x001eaàæú¨Dæïò§\x001fßü\x0011¸ \x000eÒ±¯^?|hù¼\x000fbÞ«$\x0017\x001di³á\x001e;¶¶Ü]}%WøR=úQmº\x000c\x0007µÙýE\x001f\x0011Æz}ÿî§ðýèÍÿÃÃ÷oÄ¾Î¡ÝµîÃsÖª:p¿°õä}fW>%}\x0019ÿlµo4gÙß{.[[a W>\x001aÃ%¢h«R);\x0006\x000f0orxö\x0008Î²'ne½Á=G\x000c«ªFÀyÈÅ¼\x001aJ\x0005ðÀà	[\x001du\x000e(øpKüªZ
à\x0011Á
¶Ô*×$¶ô\x000b8·ÔºWY%\x0000¹T%²ÆÙ'm\x0008f±!í\x0013ü¢¡\x0002À¡¡B\x0019Eî&TÛtzûÈ\x0005\x0016\x00174/zº\x0000º 4;8Î;×2¤5M\x001f¾ÙßqÑÞ$\x000ez
{ôz£\x001b\x000e$HSyOcI\x001aBB\x001a¯ô~i@ç-\x0017[rÓïo¹ÇéÎh:Zµ>au<'\x000eJëìÙ_s\x000f×¼íd\x0018Ð\x0011ÜóÜûÆH°\x0007k®«ÑXêR\x0017BOLêr\s¿¿ç>1zFS[ý\x000bÑÙpõ±\x001b¿¿è>#z¥I¹\x001a¨\x0017ZÐ\x0007±·©\x0018¿¿ê¾\x000cà0È&0Ü3tk§òc\x001c	Ø8]Ë\x001dC¨=w\ä¬ièÑëQp\x0018#\x001b=@¢ìíSB\x001fÎ®,\x0003ã;þþOáûý\x0003½ãÿù\x001f­ú÷oþðl)9K\x001c_¡áI¢í\x000c#\x0007\x001aí~	ï¸kÌúsø8Ú¡.ÀÙºíPôbðOâ\x001bë\x001d·D<rKÞLÌ+\x000eÍ\x001eþ`Á:á­§ÞOï"1¯ø{ve\x001a\x0007\x0006xL=EwwÓ)¼¡ùE9=M_
|K
M#»N©¡\x0004
éòofà®P²_dÓr~SØ~£CØ.®k¡b\x0018S7&srÅÔ&)wsÃcîF.1)9GÝôÞ¦Þ\x0012Ou/ù\x001a\x0011>]+D\x0015þHs\x0001ü(ø&:Zi@Oîï~jtS¥Ën\x000bÁ§Ù^¼5îÝ?û½øÛ§ï?<\x001b	´·<èkuþþC¢\x0007v¦^é³'2vl4eôº\x0008ÛÅµðqr¾¹;;\x0001¥U¨=VsáíâÑ \x0001¼Ãoï0¯ðØ7,ß~Hiú®u£A\x0002tì>ÓÅ®/
Töõ6¬3íeT:@G¥eIíì­©õsÕ¶«E\x0019\x000eàQéÂ Ð2ã\x0000_\x0018Ý4sWF¥\x0003tT:o¢)å^Ë­Î\x000cèC¶×\x000e?ZSÏ\x0008\x001fî®jUÂÉdë
[ÓÚVÚ2zG\x0000_\x0010Þ¶\x0019a0Ö®#o]ì]è_vt\x0000\x001e\x0012íÎ!].àzI·Õ
ïX+¡L\x001c_7zÅ· ¤kïO³w\x001a\x0006äZ\x001a>|ÝXï5¶¢ÆÆ\x0008N¯.¥£\x000141aE/~ßklE@©Ð\x001bÏ·2°­.®ï\x0015¶¢ÂÆô\x0012ÒÑÉ#Ë½N\x000bßÝ7o~ÿôúçàñ½üøôæ¹G_x¨\x001eÖv¸¨\\x0015ª&6×å3?\x0005¥Õ¦§ÀLüMúq ú:§\x000faC\x0016ÿ\x0018ÃL\x0011\x0008§$Lï¢±f¢à¼á+Â'\x000c§;¼Gç&7k:Sp^èÐ6\x001aàóNÖ·å\x0006ôjùðÅtZó·\x0008^Þ\x0006#\x000bD$ðÌEÑN÷b§¦T\x0000\x0007\x000bÑ¢k£!þ\x0005\x001füò4øãó÷\x0008ïo¶üªCÂ­\x000cðLÉ¢´WKÆ\x0017g2d\x000fÉ&Ább+\x001f<\x0007áÖtf«Dô\x0008éV\x0011ÎðÈ\x0007o\x0006Ù\x001f§èroøð	c\x001chÝ¢Â3ié¤)ÖN¹7<¼JN\x00011MË´b½;8n\x00035GxÜæHðá#Ü\x001c\x0017)½¢ðüÊg×e¿WY*+Þ\x001b$ÍTeùôgM:z±÷:ëPgcÁ^\x0003y§H«K\x001a½u{u¨°òÒ@£A[9GG7Ý«¾7Ðº½ÊºAe\x001dÄ{%\x0013ªX\x0004&u0¾e¬Û«¬CU7\x001c|CqÒ©Äè½ÿÅí5Ö¡ÆÊ-´àþh\x0002\x0010Áóà÷;ãöúêP_]¢"eîðið]wùÝ^_\x001dê«\x0005ì©óÕûÙÈÛîÔº½²ºÌr1\x0018O\x000c­5>\x000fÍ)6ôë¾WVÊ\x001a"\x000e1¥X[í\x0002¨¡í(ô+¹WVGï+²¶PO_\x0006?¶@nâ\x0008ºÑ=êªÍäðË{XèF\x000e%3-ë4ø½ºzTWC\x0003^zøJú\x0014\x0006çÀtô½¶zÔV7)ø2b@g\x001f¿ûCø)Ï~ç\x0017ÿ¨»â>¼~.·3/MðtN\x0011ðrêçZv®.&¬ªÂMÍ/´ì\x0017¢+­OZ¥{H âÛôq¢ñÛ\x0003¼c¯\x0016BÉ¬Jí\x0008}7-<5øÑR\x0003¼ç«Eð\x0007àü`jî>óÔÐp£¥¶:k\x0015I¾¸R¶~´Õ\x0000O¶:¶Í\x0003à>P³è\x0005[¤\x001c»lF[
ðd«xW\x0005©(&/Á u©\x0019$3\x001ak\x0000Gc­Á#X:¾3Í\x001cJ~÷§oMX&\x0015÷ðáõã¯E­ß=>\x0017ûfßùDÕß¹E\x000f\x001bLÏ\x0013}8tW¸Ô»$[´)÷H\x0019®,<%~]áiq\x000e{"d|O\x0001\x001e»1Å\x0007ç:³J\x0010W5\x001a\x0012W4øñ=\x0005xìÆ\x000cfcfßÚå2M-`\x001d\x0017Ö\x0002<¬¬UøDQÄ¯Ðô_mí¦\x000c×^èðl8\¤\x0012 wCÎô¡\x00157å nxÌAé`FÎ\x0014ÖPHéÒÐ%\:OÔ\x0002x,cÍ\x000c.H\x0019àÍ\x0011Ù§\x0006?Úl\x001fêX±aâ2YC'ì¢}ïóþÃl<ÚòÀ\x001fß¾®f$/.*W_¼zZæ½Y3ü}âs7¹<U$º\x0008ÛÕÅüfðh	\x0019.Pî×;NÚ¶ÝM5\x0003§\x0014¤{yÛ¤¨Ëd\x0001WÒ\êèã
èÑ!¦\x0004ñÊëK¡=znJ»\x0003<¦Ý\x001dÝÜXÂ0no
§gµßiÊ ¦o7÷¿¼{z¦këj.¯í=µ\x001aLÀ7p_@gãfÏÕ¸êú\x0014~\x0019ÌeX]0·¶´ÿy}\x0019åã[ÛúÜÎ¸áA)¬z;\x0000¯¯EDiÊÒvÍus:ãw\x0008\x001f^\x0006ø ²\x0019Xå|\x001bú\x0018\x0017u\x0013:¨ö}FÐ9Í*Uº*Äª/JárÒ\x00197<8ÉV\x0013Õpr!'Y\x001c\x0007¥è§\x0012\x001a7<¨´¼¼|ú@\x001b;t¦ë-!ö/;e\x0005nø§\x000fd14\x0017\x001cèôCuÜ÷·n\x000e¬/x\x000c¬­E~ø\x0006?ÈÞ\x000e¯KKÇ¸9²¾áñâè)]ËH²ÉCÎµÜ¯\x001aß\x0000\x001d/\x0004W\x0010î*[\x0003ßË:ô³ØÖÇè¦ö1O\x0008op'ºD¡¡ÞK~\x000b¬éðS:éÏ(\x001bÄÿâÕ\x000cði¸8vÞÉð½¼øqi«%ÑÉãÏÏe®K1tR 81ºíþ\x000eA7|þàd=C/\x0002\x001b¾N¡~\x0000wKì\x0004\x0006'ÑúÆ}\x001dcXïLãPp\x00139À\x0007w\x0018(.¶Ô³NÍú·4«\x0011F£\x0004ðhBh\x0003¤'|±ÔW!sÏíæNÝ\x000eaäõÊð½Sj\x001d7:'B½x÷M­Ã¨\x0018\x0000\x000f¡ýÈ·^è
:ìó\x0012\x0007_Rì\x001f
* \x0017DÏì\x000b\x0002+W\x0012µâjú§\x000b~\x000c¬\x0000½"zA[l?ÕÇ\x0005>\x000cßÕ5øiäùçg\x0003õzm04\x0011x~;³C\x001cß\x0002\x0000·\x0008Nñ¸rx\x0006g'¢´ÄK{tT(Ýó\x0003ÖTéùÒðS`\x0016+hJúþOÿú°0w:Mÿìl]m«\x0012)Ý\x0013RQ\x00100ã\x001dKoÿÿÜs\x001e&-22nª\x0017vIê7Âz¡Õ­Cb«J^j*ÃÚÃ©^\x0008ð \x001cJ\x0000OðDÓæuÑ»«1ZÔ\x001bÜ£ç+l)\x0010û:äc\x000cAèkÝáG
ð`QmX\x0014Sxª3\x001bÇ[oàtS»7 \x0017ÑORJxzlx½¶º\x0002Çhjø\x0006t4J£\x0003\x001f(Óêj´ì`ÛV#wSÇ÷
\x001fÐ(r3vøBðÁ\x000c§ïTa4K\x0000f)g ­já]fÑ»Ç\x0008g\x000f\x000f.ªê1	'3¦ö\x0018¾¯Ü{øð\x0012:
fßÊ4t{þ\x0014O\x001b\x0000\x001e?­ÜzMÑÌÆ$\x000fýÐU{ì4­ê¼áå\x001e*
B
Ï<ùÏ\x001bü^8Øn´Mè^ú¢a#Zpio\x0011\x0012úXÂ¤¢"'¨\x000eí¡}o\x0010°\x001d]nJÛ\x0018\x0005\x001d\x0002336h\x001e¢\x0019 ÏüÒ\x0003÷L
np\x0010s\x001càË<ÿöé'óðÓâ½|ÿâ\x001fþó?Þëkùlù\x001cÞïØÂ\Pa²É·%9\x000fYÊ2¡35Ð6!¶¸\x001c}à(Õ¦k;H\x001cÃK\x0019¤ÂÔ?{£ã×O\x0001\x0008«bÊ´³F	óEÃº[ol4\x0019FbL´fJÀ\x000b¿\x0006~1 SÒ?Ûw0\x000e\x001c\x0018ÿñÅW\x001fÜHÎW³å¼kh\x001b\x0008ú_¤¡ôÄ\x0010­öé\x000bH\x0018&m\x000eûó#·]ÃÈ­\x0013ÃÃGb\x001aof+\x0015G\x0008ìç'×Ã=ømuu/é\x001d®\x0013¯\x0016ÀK!\x001a7]·¢'\x0006pÿÉà³E¿À\x0003[([Zlº\x001f\x0006î9á£±ábä\x0016Ào®³¿wÅ­èZ¨;tkW[D}0­°0\x000b\x0000O\x0000.q¡½Å"1ì=^ÔÀ=£½\x0012ã/Fn\x0001<2øì^à·kêÄ)¿múAo\x00124Å»GÖÂ7;7;/\x0017t\x0005hÍ¨%6W£Y6ì7úÜyf¯ô\x0004_çµì5½¾6u+zä¼©ªÐ¿/(\x00008è§®\x001dûp%\x0011\x001a¶á\x0004ïyÍ©ß\x0017ÀA?åÚ¾¼­Yª0ÜÐt¿ð$ëqøÔ\x000bà B®VÒÏ\x0008ZÝ²\x000c*\x0014ú\x0018Ý^ \x001b×ùNPx}Pß¸5oðÈå-´³îu\x0008zq.4pÍu+=	\x000b¡¡7=îU\x0008\x001aqåûø;
\x0010ìbï­:í.\x0016~\x0014C´}g:\x0014üË@à\x0001\x000f>,\x0017ðÞR¹×"ZtlZ¼^¿z3(4ôÌ\x0003\x001fçi\x0008[t(\éèâM¡ è¦§þÀ¶Ð\x00024¹.½Üº×#¨[ÍÍ@á'	÷°p·¹Å\x001ej_à¶GÇÎ;z\x0011ôlo²¤ö\ðBMy¯{:cÿÒ9|éB¸ý(ò\ÓcË \x0004ÝãK\x0017Í½ûVMz&ÓX
\x0017¹ëÑ^K\x001d¾tJ$fï'¨Ô\x0007ó\x0015q\x000f\x000eZª­Iõ~F³\x0004a\x0006¯£mc¯ìõ\x0014\x001cc§¼\x0018æ>z\x0016#oÑ½ßÇ×÷ÉøýujXÓS\x0007\x000bãIQ=mìðÚòï\x000b\x0016\x0008@w¨¨þ^Rõ-¼9=º¢²\x0011cY²@\x0000ºÇ³\x0017¤\x0015Ô¬C' 
]þÀFÎ»¿]sÁbN^Ó\x0002À
ñ4øXã\x0005\x0002Àá>\x0006]úvk½6âeçÆS\r@\x00006>\x001a©bÞNÃ6ºë1pzçØ\x001b»ÈÛ]è\x0005ý\x0000b[t\x0007j
Ù\x0016åè­Ñi·»ÐÁ²+%r-àvÂö\x001bÙ1ôÅkô5{Ë\x001eÐAª	¼å¥
Í_\x0002±s^-f{\x0017Y»\x000b\x001dU©8hî´\x000e\x00161·\x000bS¹|rÓÓEÎî\x0002GM¸­Ww¸¾D#\x0004Ïëú8\x0005ß+Rð\x000c\x000e½ÕÄ\x000e\x0019ÄÙÒTMÃ{ô÷1àx¦\x0015\x0008ò¿t¨ÐëfQóðµ ¬ýêéûgc¬\x000bÁ
©\x0012~]¼éAq\x001c\x0012´U¢>wCêºÕ|ø2*¾!â\x000eF\x001e\¸ræã®Ú)â\x000e:ã³¸/h`«5%£eÖêXJ¶ÙÌEÁ.âí\x000bÚ\x0003´ÎÝ.òD6\x001b\x001e\x0019q¥Mç7õB\x000eõç¾ïG/Ç"Ô¾ 1]<\x00000÷\x001agGÈ?ÙX¹qÖù\x0015³Õ\x0005\x000cléâb¶ºz{díÌb¾ Í
=oÆ¼Ñy/fÕÞ$J©-¯y=S\x0008|A9­ä\x001e·ö~õÃãOo4qöì»@áöÿÔÒýO(ÀÃh½ÚëÏ46-6&U\x0010	\x000eªtjç\x001eþ²âUR¯Q¨YÄ_ZmÔ¸ \x0002K¢}Ø¯îE¡yÞ.È³¿Ò\x0013\x001a	°B\x0004\x001e\x0006íp§µ \x000b\x0005øÔ-u3iÃ	ìW:©\x000f;­\x0019hÁ,ßÐ-Úè_ÐH}%ÿAÅ­ä%Ë©W/D³by» øJìp\x0006Ø¾]\x0001N\x00199®òM\x0017råC_¡\x001eºó;Á¡yòPBü²J7Ø¸HÉ?ÇÌYGKyåÔ¼=:ÄWÙ¦\x000b\x001b©é4 c\x0017ê(	ÚzÀÐnkº îXøp\x001d;´<"\x001c§CçG\x0006Ë/lÒGC{ÍEi\x00123êAiÚ«7¥±.lTÈai;R§ÙúÄ¥««$Ö\x001aé+#ªÚð-\x0019¡ûÌÓN#mb\x0013\x0015ñn'êl
ú\x0008;­\x0012X\x00172*¤/Èt§Z5\x001d%\x0018\x001cîv\x001f¦Úi¤-l¢\x0012bgÚ²!§\x001e\x000eÝ3c;´¨:È÷ÏÓt}\x0018ìôþÅUêêÄv¤¡qÎ\Øedt¬lIz\x0002xJ\]Ø¨\x001eMoú¯\x000cû±åþ¥UÚêÂvl¦\x0002`;Ã&ùeÆê\x0002Fô\x0011ÆéÒàÐxÐ\x0000\x000fÝû»v
éP!%ª}á\x0012DÑìr¨>òRXå«.lRÈ\x0000i¦5Ø\x001c#ç\x001eìvj¡ä®º°\x0013ÛÖ\x0000wÛ9\x001a&	ÚQÁØí¹U\x00176é$¤û\x00054Î=\x0018îÆÚ1µ_Ðm«»í¸uXmë\x0000Ý©@|aN:hKcW\x001aQc\x000foB¿Óøí
ÛÖ×$òÖ³±g"¤eòî&´,\x0012ÃÄø¥úAsÂ2uwa;¶®\x001e`\x0006¦Oã\x0006´æ¯)qwa£Vêì9[î\x0012éÜvp¥Ò2mwa\x00076¯$îLrn&o\x000b¹ïëÚi%1·jï½£+8È{|\x0016é²v\x0017vbóJòææh}\x0016ØRå³Ûi%±¶º\x0002ü\x0013í
\x0012ù©tã\x0015\æ\x0003/ì2XX74i¢Ï\x0002ËÜ*1S6ðÂFµtØÞî`¥{RmZ¾å´õÄ\x000e-¬\x0007÷ü±<r\x0012¦,à:é F\x0010¹\x0007>0\x000fÖËGÌ«\x000cà\x0005ìØ´ ýK¾{L	\x0010rË\x0018Où¿\x000bô\x0011ÛÛÝË|ìaÇ]§Ì²\x0017v`Óà\x001bØ1?¡çfè&6\x0006ÒÆ\x0000ÝbVùñ,:\x000e§nó_S¿ÿØ²&ð\x001b|äØF\x001eAÚþ}jö¿°I\x001b,XoÞ¨a¸$\x000bojõ¿°I\x001b
Å¿b\x000c±á\ÏÍÐ=½½SÆ@ÊèÈ÷£ö2pÜÞß©ÉÿÄ¤\x0006¤%p%$Òâê©¿ÿÂ%e´/ù+ZzÖ\x001bÜÊSë\x0005í·\x0000tFføÔCôÑ3æÓàÀMúh(²VÏÏ=¾a}'ùN\x001fcà·\x0000µ&ðÌü6ü\x0016w\x001a\x0019#Û8º}ü>\x0016æOÙò§;ß\x0002´×Á±·Í\x0014û¡³÷Ç>FÔG[§¸}IGÒÎC:ª4£\x001dwú\x0018\x000b½\x0006\x00144i\x000emT\x001d¤Ý|í©\x0011úÂF´Ø/'Ø
%\x000fqScN;}L\x001f\x0004Ð\x001b	ýðî\x000e§nµ¦©¿úFP\x001aý\x001cMôÐÓópGÕ«/lÇ/\x0002B'\x0004××]ÒjÍ\x0013Ó÷\x0005*i\x0013EÖÁsö¥ä4\x001c»-iº¶/ìÀÇ6¨Ú¤áÜÍÕz¶/lTI\x001béù
apÏr\x001cÎÝ¬vÚ©dJü9Ä®Ìz¯»Ä	»6W{j\x0006¿°I)9¸oiXÞ¼"%ô\x0005³;L\x001f2\x000cöâ¨79kÒX±w:H'W²}JNd\x0016rÚ¢xbgÃ\x0019¤\x0004â¨8Å\x000fÇnÈ;Ì¤(iÞ+G\x001e\x0002½ÚvÞ)dvü `®+z\x000ejä\x0001\x001enHSö¼ÓÈL\x001aé^:ú=$ÍûWV>^Ð¤4ÞÈhÙÕÎ&/$½SØfWDm.\x0013_HvÐjSÇiÕãM*cÈ¯T
	N§]ûÊäÂF»¢Êä|«\x0007\x0017­6?jZñxA£Æ
»\x0004:0t*Ã©Û\x00039­ 8¡qo \x001a/_¡%.eà	\x000bµ9Q\x0013#Ë
c
åâ\x000fúi8u\x001enH+\x0005íT¦8~hàZ'swð\x001eÏ#Z7.)ôNc
jÉdô+Ò½NÌÿ\x0019j«\x0016NÔð\x0017vàÏhÀ:)áDúÈí¶õLO\x00142\x00176ª£1ôå8\x0004\x0008\g¶õaM¤ð\x0017tâ\x000fé@$ÅÒ ^¿ÂØ­Ûh¢¦¹°3\x001f\x001b
«\x0012¸#ûg±¹vâÊ:°­1ü)\x0003Üí^\x000eÇ&\x0007-\x001e½Ø;wÄ;¢õ¾Ú\x00057ÄÕLQ¦sX­f³¹¬¶á\x0010!ç!°Ô@ªBéëb7\x0017\x0005\x0017õ¦X
LùXíwk\x0008\x001cþÆÚb²yµÂ	Ú£ÓNÚöÓæÅº!\x0019U{CóÆ  }
¾àÛ^yu@Hë6JËúï«iÒ\x0003\x001bgIS¬°\x0001R¤"\x0007§Âuaù\x0010{\x0002z¢ª<°=®ÉÛ4T|´\x001b£er7Êé1	\x0013äû¥ûàò\x001fswCª\x001c*¤Î\x0017áwFÅ£QÑ¡Ô\x0012Á\x00068/%þ<ßrzá\x0006<`C0TÏR¾M$\x000e\x0012_±Xú\x0012®°Kj\x0004Lj\x0004ç ãÇj³'¹ÝrõHùÅV4ð]x\x00160<ÓGü 
\x0013ZøöS\x001fÐ©÷Ù\x0002CU\x001as\x000b\x000e¢¿¤¹OÖiÉÄ	\x000e+&îr¾E®dS\x0004\x001døÜ9µÊ{ÚU\x0013V]§;¡ÇBó±cèqÎFà	}o«#;÷¹õA"è=\x0007hºç½olVBkkcÂS£\x0013²YÞ[Æî\x001b²Øòo\x001eP"¾AàéõÌÃ®¹ÔI¬DÉ7øò\x0013Ä\x0017»íM!\x000f­\x001aåT\x0017CÆGh\x001b=\x001bÏ\x001e_ü2\x0014¿z÷áÛçé;s5ñÜ¶\
\x0005.xñ­ïÛ\x000c>sß¨îbXsâ£T	ªo\x0003l!k¬qßZc¸¨Ù8aP\x001a¾µ/|¾`ã[Øv/â\x001cp\x001cÞY\x001fûFµ9\x001fw`C>.ä\x0016Öèl%Ç\x000b\x0016])ß·JÌ\x000eÂ
\x000e¦\x001cÑAÐI|ãÑièT\x001eÅÖ ±\x0011
ré	xÎ"S\x000bG\x001cº²`%\x001fÿ÷\x0015_Ü\x0005\x000e}¯EWäA³n	ò!´F9x`'<x	ø È\x000f)[vm|nÞ¤Ø \x000fp
»5à\x0006Sk´\x0004cÝ¹2²?¦³Õ?ÀÁêkôUS«K]Á2;ñ&ªi\x0013ÓÙ\x00078¤³. Ä±e`:pu8xwÊæ7üÀ&\x0002\x000b\x000e<L´àR>&ò>|_yèw·ÜÒ\x00085H¼\x000f\x000cÆZ0IÅ¸^ïÝ\x0015fE÷UÑm`DÆ\x0014¹ëÅçö^¹¤c\x0007$\x00154Ús
w%VrÝØöâ;kHk\x00078sù{òÃ\x001ay¨°DþÑPw3m×íÂß;°¢J|0X.,FUàr\x000cÚÝÀ7\x001a\x0014"ò3\x0003\x0005C½+îÊPèô¥|vÉ\x000epÜú¥óX\x0016¤âéù3e±ø¡U\x000c7Ø\x0011¹¢=(v\x001aCL×®\x000eÊÙ9kã\x001cÕØ(ñê1º¶¢kÎL«oD\x0004qbß¿°\x001dRb·+ \x001fvn*³\x001far?øækFäÆ·º\x001f\x0014,V¦ö?¯Õ\x0012¶X­j¸¹à.¸øHt.¡\x001fZD\x001b\\x000bâ'6BD6dj\x0007òflÙI½Ü9gä\x000fðü[Öb¯\x0015ÕL$\x0013;f\{áp'\x001cYÜP\x0014²ÅIóýîiÑ8Ç§\x0007v!ìp³c	´\x001f¸s-¯Ä}ûGÚéN"ÝÑ\x000c\x0010x,Í·;ÈK]Â±h}§<	ÇÓ\x000eÅk[
oY\x0014_sS}+Jû\x001b\x000ep$2´Ù`D 'Ç¨Ý©2Þ"±9]|`Ó¾Z\x000cëV¹Õ°\x000bÆ\x000f\x0012?ò$i÷j&bØÖ\x0006NGç®\x0003ö ñ\x001eN»!/pÚ\x000c1ÊSjaÞù\x001c_qºT6úx/$õ`Ù`5»qlWnbÉ;¯6#C´x°=¶?m´\x0006·æÁ·m\x0008yîÖ;À=ñSÇêûOK!ËÐ\x000c}Öq66+ÓêdKÝøjÂhGøÀ\x000cÞÕó´Çá\x0004§-\x000eÚË/¾epÞT\x0010lãO+s?j\x0007/¸µÈëê;\x0008S·î\x0002\x0017\x0007+.¦¹\x0013u÷A+­/³\x0001T­rø o®~\x0019üÚÆºWw
ZQAu!\x0012úµ·¬+­\x000eû¾êÊlbûÁ±¿N÷	b!Jc\x001e^áÞ\x000bü\x001aBnÀyWb&¹ÔBÖ^.ö ô¾¬ÚÌ\x001dÝ\x0007:-\x0000\x0011×
V\x001d·¥­qCfWú\x0018¼ÍS\x001eæ \x000f\x0013ª«´×h¥bd+\x001fuøª}!`ñßnãæo¾ÅàÖÛ_ì01\x0003§zæ¡\x001f\x0003¯Ç\x0007ø\x001aéR*á'ñùÙ4\x001cZýH\x000cÕ«­	ûæ\x0015Ø\±W°\x0011ùÓv;ôóùp\x001c¯Ç\x0005Ò\x0010\x000b=FÍs¢\x001b-\x00013»è¹\x0015{ä¯«çó\x0004Ë%t#\x000c1:ç\x0006o·\x000f½¸¾ü\x0004¤ßhú¡R\x0012e\Ô× áçãæld£7\x0007d#f\x0013=\x0019\x001dàÅ  YNpúÔÔJNø¸?û#=\x0018n1åæfoç^"«Åäkç?\x0012ÿøîá_\x001eß½ï£ë_?¼{®Áu#8\x001d4î>ÿ\x000eqçÒÝ\x001a ¤0µ'¾È(9\x0015ù}Ãë^ùûnn¡ªä\x00198\x0002nx<Pì_`ü\x0003\x001aFA¨®jÐð\x001a\x001f3])]7V
S\x000764LyM`_e!eþIÄ,jªaìÐézçmÂ\x00078î\x0012ÖÅ£ÈYVä%Æu¦8\x0016×©ù²"ÉÂo?4rÃß¾ýöÇgÚø%ÎÄ0Þ&PÏ¿Á\x0019|³xû=M\x001e{~åÏ_Ó_AiÄhã2xÐUâ¬­YgÊ"¸^Á+Aüí~<´¨5àE\µóÇì =@§B»\x0007c/]\x000047\x0008ÛÚÒ\x0008SzÂMü
\x0002\x001dhwn2Ô3m:*B÷\x0016ò\x001dtDhKë±b}I\x000eÃÂåÞF4+íL°\x0010"qlë.g\x001cÎ\x0016ÿ\x0007\$fi-[;èÐX&nòHô\x0015Ç5ÑµõÙN!Ä	]\x0000:àö\x001aÝo\x001déÐ?¢ëmD³9ÑÎ÷gø#\x00162Ö\x000fâXO\x001fÐ0QîuÙ,PÜäh÷¢\x0019h©åÔ­
böÀOlÔE­
xÈÍ
¥ÎØ¾ÈvÚhN;rb\x0000nÆ¾wgúø:ZTG`_Î\x001d)þ\x0016{Ê5sg\x001aÝÉ<R~b£>L®¨2%s3-ë6ÏÀ\x0005ñC\x0016\x001a`0Cÿ¸3½<¸SG'×-ÒH¼³§\x001a)m³f=Q~b£>j¢\x0017])Ó."ád¸¼]½<¸Ã\x0006ôrPØÈ55Nâö\x001c%8\x001bûâÇ\x001dveàFõ©Ì¯2\x0019Î\x001d×#å\x00076Dôº3\x0014æ)Û¹±Þ£¹áÜÍÕÚ©$L{_,\x00046íµç«\x001d¸\x0011[Ô¦oÚaJúéhc\x0012\x001aÀâ¸×Ñ¹ÖÕ<\x000fØ\x001eE\x0012 A®i\x000ecûÁ\x001c;v\x0003ßÃÀý°â@Ð\x000bYÜ \x0012Û§ólö	?YÜÖ/¨.CÅTAÁ:º,\x0007MUï\x0007CØ\x0017Ïöõ:@´×la÷2;â«\x0012[XëÊÎÎð
ÿODÆµ\x0005úü\x0018rÏ­\x001b,¢kÁêKé²\, åø
¸MV4Õ
Ö+¶¦Ðú_Q_1í)¿û'D$f¸mó#¿Á\x000c¿!øHOR¬ÔÄ.Oéä\x0011uv%Øþ\x0011?·\x0010\x0003îª
tW\x0003Yâà»Ú\x001fü4ü\x0006\x001d|b8Î++	Î¶a¡²ÿ
¦ðo\x0008\x0012¤\x001aOV9·ëãàqøUö ù¢gûÒÛ\x000fïuªï\x001e¾}6Ö»Ø;kîæ¥\x0014ÅK\x00177sÊXýùþü¬w"¾!*Kº«åf÷Õ=]Ü³LfaØ¾]p\x0007í\x0010:\x0002Ev%¿\x001c#¹©Þüæ\x001cÈØ}¬)R!k\x001b5
\x0012&\x0018Ú%5Ý	°Ñ\x0002§¯îf\x0019úI\x001dMÙ\x000btSçùÉ9 ¡qR\x0017C^#*jÏC²¬d4jöy\x000eh\x001bº9ÛÓ­4têè+½\x0015:6²OEôy\x0004;\x000f\x001c\x0012)²º\x0018MHOkÛ)¤RþïÇ7ï^üêíûoß>ÞZ pîN¥${ÓcFxþù*;möUYÛ¨²­\x0018~ ì\x0007"\x0008-y b§ÚÙAÊZçþXÝøö[\x0013\x0019:´FIgOhÐYíúÌ\x0001 \x001dÙvK¦Ê\x0013\x001af4¬D³Æ\x0003tåÆ^;\x0003\x0017Z\x0011o2\x0007'4\x0003«MÚ ë\x0010Ø<ZrüËLÊðÐ9Ð¯h¹+ÞrW¼rvû¡9¡ÁÐ¬nûG´dD9QaìMl(Ú\x0018=p$`O\x001e³\x001eØ®Ì×	
æ«QuC\x0001^;Çîó}EÖF9°Ï&{WÕû±	[ãùrÔµi<±-\x001b\x001e\x000bÍ2ÓØÄ'|î¾¾b§HÌgõµc\x0007wS÷ÏÈ¯§ë;ç,ÊíùØ\x0016­ì"\x001fDâý&rb.*\x0015ÁÍ¸/"ñ/	:Òp¤ó¶K{§ÈË§CF÷ÅÖ2i$aG
§4ë·Î£ÐO
Ò." wÛQ7¤
$.Ó('tæS\x001b\x00166Í0ª\x000cØË½\x0012\x0017vÁc\x0003¡¥`ûÊn:Ü4dÌË,Ê	]cD¼ã@àøØiê8°<¯agÀÎ\x00136ß¿Ð\x0008\x0005Ó<°×ÁS\x001a.`Ä\x000b¾Çñ%qn\x0015fåÄ×O\x0012n¼xÆý¢aØ@×Ö\x000b\­®\x0014%5dÝoIò%\x0017¡Æ<{'2Ôï\x000e³w!ß\x0003Ù¦èþ\x001cd`\x001d;sP3\x0019À\x0001qHÂDòÎlbj(ÜÂg[ÇÇÜµ{@C×®rB¾ÄÄp	Ív\x00129sm©³ÊÍ
Þ'6Îxâß/\x000bê­Ý°{\x001f\³Ù\x00076\x000c\x0003¤\pDBé\x0019Ñì8íÁ¢\x0017Û\x0000|³Î\x00076´ëg[qe|>xoìÑ\x001eò3Ã\x00076Î¤¨+\x0000\x0002s¤wÏñßÔ\x000b*s[ç\x0016\x000f&Â¹kâk\x0012=çQlª=ç·9¸Å\x0005®.Ç%¥9Òø\x0017\x0003É'\x000f¦/mã»\x000eK¥½:â°\x000ePç%°oD®!/X
ýÅÉ\x000ep o
ýN³FÃiVµ×\x000cnúÃ:·ÔàÐíÇý\x00181W*Ä{	\x0017\x0007±tÏs#'8´z¹\x001a±ª\x001bq\PÀ\x00073ò<«sã¬.#½!Iû\x0013È`\x0015
X¿|J9ÁÑ\x0014LYÃBô\x0014:yÅV%Æìß\\x0016\ï(ß3Ñ5Wâ~ê\x0003
\x0003¸\x000fBv#\x0015çq)V¼æÙs1Kçº¸âiÕAs¤C\x001f©²¶\x0000ùQ_Ò@¨\x0013\x001a
>7L\x001eà\x0005O^±\x0012S/K\x001cÄÓQ\x0007lØ»\x0017<x
T+Ó9\x0012\x001a½²¤"¾u ì^7¯[Í\x0006úåÙaI®!ý\x0014SÞú\x0019çQû\x0003»âp²_B\x0011Á%lÊÐ\x001d³ÏÝæg.\x000e\x001d2n\x0019u	7%äqÖ­\x000cû4\x000eì¼CÁí¨k×è£~z;ýI¸\x001eU\x001c\x000f`\x00061±2+\x0017ÿ­J><=Ì8"6¬QÆÒ"no¦ÑÒ£þÝûá}\x0012LaÉ&ÏN£#ôâ{ñ[ÿÄ\x000eº\x0010tr­ó:w àß»LiQ_ú0ZÙif¡Vfù|°V\x0000sI÷íáíÅÛÞ\x001b´EÚ¨\x0004¸¸êVyñ[&Kî×\x0018ªEÿ\x001b©Xt(¢åÝ¼\FÛL¨3V>¹DÃ¹?Ësï|©:.uÙ6GY6+>Õ\x0016(Õ45£^^\x001c¶\x0002ç;çsµ<4\x0016\x0003\x0017øÅµmµ±y^ýF@ï¶P}²R\x0013N$°}?ûw{ôï\x0000=E\x0018\x00074µ!\x001b>òä®~é¢ß^ÿ¿\x000fì\x0014LN\x00116~©SD\x0017G	·»\x0015NAx%\x001f¸GwLcÞÁ6l\x001f¹¹GÕt6\x0017G¥ójðt-{º$üë yºs\x0018Üâ¸ýñëwï_ýÛÏï)\x0004@pøK\x001b\x000b\x001aôrÀ,¶\x0012ºúÏÞª+Få/jLejT2CXé®Û)¹¦><¹Urg'þÆ®+%©\x0004oÕ1K¥.*b\x000f$§u£â\x0001QDd£.Ì1ªÞµe©íÀÅîPÅÓ\x0014&¹\x0019\x001cÉäm\x00074öEÕf¥]æÞ¥a~E7E-«x\x000746T\x0007\x000f¸\x0012ÈrwQ`\x0016n9ôºKñ@Æ¦¨;uL[A¢¶ì·Î=8»4\x00074öD\x0000äAFX=A{fß2ù¸Ù`c¢n@D_L·§ÐÍ3ÜIcj\x001b\x0010^Ô\x001e\x000flj2wÑ¨_\x0011Ëçö£´ýºOñÀÆ¦¨HM²ºQ\x0001ë ê×	ö\x0013z¢\x0012%_$©Ô\x0002éxRBoÍºðÀ¦(Nì\x001cï\x0014ÜAÑû\x0006ôEËßw;9`64Ê
©cÉ\x000eI£k/ìÊâFÛ§eyçáv·ÁýU'Îi£Æv"ä!4ÊÅï¨\x0013-\x000eÖõ`wýÈo\x001aèÅè¡i,
òY½ªM*øªþ¯ÿþ?þëOOÏT\x0006Ë5l k= ×W¨Ø«iýøÙsÊ±TóÔÂErÓjuW.h¡¡sS\x0006:Ä£:Û\x0003^Tß\x0006MVÊ-+á'°çÇéND»Ã-ôrM#o^ê\x0003^j\/¥¦`<òp5ú\x000eóÙì\x001cÐdvp.N-ØÐmèÛN\x000b1ËÇúNì_@¾JO=ôG3%ëÜ³A; 3\x001aBù¢ÙÈë²\x001a~"ãc}4J]Èyì]¬Ãí¨Ë5u'tå\x0007Õ8æCÛ¡U.ÙÍcÝ±é±.\x000esIE«áÜèÇÓ¥.µÝ\x0007õÀÆ\x0007Ué¤ 
#®\x0011÷ZzðÑÚüº9ÿÀ\x000eø!ãK¬\x001eiÇ\x0007Èa\x0018"õR¶\x0013\x001bEdúzÌ¸&Q^&fóp}iË¢ÑýÀÆkb*æ\x001fJà2ª¶²Fæ\x0016ç-Ñ;65£\x001bG¶/&ö2Ü&(Ö
ã\x00074|JW3ÆîJæ)0\x0003¯r¹¯×+«·ôÊØ«Ä»b:;½<È{,¬s\x001fù\x0015nü\x0015\x0006«&j³Ø3õìPÍj¾ú\x001ccúý×ÚøîÉó¡\x001fÆ:bçn]öÌ^"â®\ã¨>\x0018«túÀ>À.ò3ç¥Ç\x0006oï×»]MÁÈ}k¹]¥vâ±ÄÃ	¢T\x0019\x0018å2,ùÍ=ó¶tøN0|ßµ3óQOH¿ï\x001d»¾ï·Ï \x001d¼MÏ\x0000¿È/]ë>r;ÝØ3Ù${;Öß9ä6×´\x001c 8¤Q=î¶vÃðqñyð\x000b\x001aæþ/\x0010ü¡¯Þaù°87äLÆÇPWÍ.zÒasóç\x001f_¼~xñ\x000f\x000fOï-I6ìÏ±­ëàrT)?ª§þ\x001fãÓ\x001b?ùôÝ9Xb{ÒIa®\x0002æ²\Ä~BÓ¤p¤j}\x000bAQÎk¯ÞÛ§Û8/ÎË\x0004Ct¾¦\x000eDÄöXµF·>óDeë\¢S\x000fÙÜÒæW\x0017íîãöi\x001fí*\x00134=ôÕ3Û¥íë~f·ÊÛ§E 	yX´u25LÐiÝI?nn£±\x0001ÿ!\x000e²6\x001céÛ\x0012Ö~½\x0019·OË©Ytr¸Ò©_ÄMþ¸}ZïöVÓ0ÅSåÒ¸nr=°iV8fFT ?#'&lßcµêÿ\x001f·Oû`,\x000c92E\x0019\x0017%Ø#¿·ÓG\x0015\x0016[åñÜå%	{`\x0019³ÝÁÙ©#¥àt¶ÌÑ©+ÙöÄ[5mm\ì`ÄË§åK\x0006tmÄ
ã4þ\x0019Pn­uzÏË§Û$\x0016\x0014µ}{xUy`ÍÖ\x001dX\x0004:fÜ>Ý&z!@Ë1\x000cØy°#GÊs§:Ìã\x0018a_/wí	æJb\x000cÕ=p0T>öÀ\x001c±Ù\x0011}`S\x000cUcCé
8£Ç3¶¶@g\x0011Dq³\n\x0003eílðÓ;Lm}Á\x000eÂáB_2ÙÌnÂ+*Å\x000fVi×Ùw<Í\x0014M~þ2CµtìÎwr$¦»æ±ð6>
¹ÅNñ#¿!\x000e¿!f"OÐ-ÏD1\x0010É\x001f\x000f½µ;\x0011YK"2°[­\x0019\x0000GÉl\x001bÙzýf±ëmãÉÛJt&ò\x0004[Z\x0007ðâö±÷©Ms¦¼fÒ(Ï&=\x000cÚÚæ-f®ûü8¬}'\x001eÏO·>ÆÅéÝ2ð8uj\x000e<ðö$æ\x0017Ö¸` Õñ4¼m+7ÁmÿõãÓß¼{zýúíçñÚW[û­½JÛI©@aN§È+«ä3³P² Á_ôôÁi?§Þ´è:)ÞNà\x000c])çêf&Í\x000c>{²\x0005ÚÚÐoy\x001d¹­<ènõ	\x001c>	xºEÝàß·èõëNfö×ïúáíwÿù?o*ÙxÚuå\ÐÂûñ§q\x0010©5hÛÏ}þÂ>	Õïá2)Sf¸g8Z\x001fh%Y\x0010msqÍ\x0015uB;¶4We¹È\x001eLÅl\x0011à	\x0013ñækï\x0003\x000eíC÷ÙÉy	Õ\x001c\x00109Ý\x0003õÐ\x001aî\x001a]öy9ï|BÃP.fYl¹Jÿ0\;»ÿNäfà<m\x0010IS¦Êc9I}Bç\x0001\x001aD-¶Äá)µèkÞy·ß\\x0010¹\x000b]fzy\x001eGI{OÜ\x000eºâG4ð):Ê\x0003°Î\x000eòèÍóºC&ùÛeÐc\x000fû\x001f%wÀNËøïÄ¶,«w5nÌi8QÆ²æ:±I\x001bÍÍ	×µÑ²LxÚÞõI°9J;±Qi
ð£è%Äÿ.Q\x0005wyò2:±ñnç8Z\x0011Ow;0k\x000bwiw\x0005-]Ápg{º²{¾ÝïÉ1y·»'îIAöl2µ\x001fë·\x001c°Û\x001cÉ\x001cîØø-QiÝ!Fª\x0013û-îÐÂ-C\x000fuËþæÇ'yS¿~ûáÝ·¯-Ê]\x00016\x0000=¨?0Ýjù\x0002Ö\x0013ý¥éT;1|øP\x0003µÒZãn<ó²\x001c]¸·tÍ&\x000f¦I\x0013ædYaÎëû:\x001d4¦SÅÀ¼ a@¥ßw@\x0013ñ"5&§j9¾­aHhõE\x001c;dâ]L\x0018ù¤Êk84\x0007ÌI'ï¯é	MÙÔ@°gNG_\x001dvâ%i9`oI\x001eLéÈ¥"ó_½¦'2fnÄ#
ì9)TÝp=Ò1`"<\x00183À"ìI\x001cfè]÷;Æð©nuõÌé¸wÔö]\x000bÂK¥¥"
$Ð\x0010ìZñeÝÏxb£2\x0006\x001aåÑcgN¦\x000e·ºÓõíi\x0017\x0003µaêb">6ïT°ÇÆN\x001b)ê\x000bìk\x0010lÎ
Óµ¾û\x0016;e$ÚEG\}©º¡w´¤ñömø\x0002\x000elÔFWÛÊ}hf³*µ\x000cçî¾ÅN\x001d)=kz\x0019zuÝ ¾¹fA\x0018p`£BÒ.\x0005Á®Cg©ÃÃØýÄJR§\x0018?PIõ·¸¡Ã1í³{;Ä,m\x0010ÿ
éÉáòF)Ì."i\x0019àJ\x0012ïbÂ\x0015^íB\x001dª¡ÝíÙ%:±©#*Q¦J÷bPæÚ\x000f\x00060v¾ÈN\x0012ï¢Zm<·§af97¯"±}íö^>±\x0003Jx\x0011ÔMäNt7¼ë±oàÝ©Ãn+¥Èì )-±Ã\x001byì\x000f]d7¯grÌ.ÓÔTªy\x0017«O£r6\x0003÷¿Bw\x0010	Å²ðg\x001dË\x0004ðõ\x001cS\x0002X\x001e \?âû¸ÑèCð«ÖËâ¬x­¥*¦
Ã\x001fàgg=fh} 2ÿ_¿®É°gÊ~y1\x0007Ü\x0011nv¯¨Ëlòm\x001eª¨°ýüÙ¯5e3zìÓ\x000b 2\x001c\x001c²¨\x0002xÉÏ§0\\x001dûLWÉÜ\x001dØ´\x000eus&A§x·¯çÐ¸\LB¡]Mã\x000e\x001c:«ÃP»\x0004ó}µÈ\x0006;Ã¢8£.\x0007ô3éH4m¡ãn&×âyøô@ÆáS]ÿ\x0005ÏVIeX[f\x0007Ð>Na¦ç¶c[\x000bº"Q\x0011Ä}
º1û;û¨²\x0003\x001c²¨\x000bÖ u£ê8ËÇ¶¹ÒK\óðö\x0001ÃÛY}«1ä(m\x0013üðøv"·´[Ì{\x001c3)Z	¡EWsç{/ù¼*®'X\x0015'\x0012õ8v^!\x0017\x000eµÑx\x001c|²Í×Éi?Áõ9:þF·f
°ÍÍNö»­rÂXkÔÍPF\x0017Ç\x001cå\x000fµ-_»êO¥¹\x001b\x001e\x0006RµÀ\x0019v~\x000e|Ä±Í¥¹&zc? Zì-Ý\x001b\x0004ËÂ\x0003¹ÎwJoë§í3×eÇí3Îö\x0006áóè\x001a:àÝ°vÉ¥E½F´ý~±¾zxýðÝÙ¯÷·oß5+þ,\x000c²Ú£É\x0018;òdÊRRîd~LþKÈ/ìþ¢Ê518Ìó·ÉfÌ='.{ÈwZWþüT«Iææ\x0005\x0010A	0z!\x0015z«tÿÁÒO¥\x001aý\x0006ÓJmXè\x0003Ò`½ÓÉevÉOµ¶V\x001e\x000eÍ4Wº}8´]jNd¤¦-\x0016üÑ\x000f\x0005\x0004ùÕ`\x0015=ZöêÐÏNÎ#\x0001cT.#ÌÝfË\x0004¦÷ÚÎá¬j5â\x0006Ý£§r=ÄñdBÝD\x000f¬¨¹[\x000eÌÐ\x0005OmêM\x0013Äz
ñPi\x0017Ìr¯Ç	]?ùÔü5É­LÝg-à0Éª9ÚÞv*\x0005\x0015%+ÂDÀ$Ò¹3E³][Sö\x001cJ\x0003&>)s\x0000Ó%Ï\x000cÆi@Of\x00115ôÕß\x0013»Øàz|÷îéÙ¨\x0005t 3umÏËñhN!@NA?{×tÒtÃÂ\x000c/¶ªIº(þÛÇúñ½ÉLØoKËkÅ:È\x001dÐI·=CØ`*%`¼¶S\x0012v²-¹8ßÙ\x000enáÎFç,º¹Dº³~\x0018:¾r¢U
\x001b²;\x001d1Î\x0015hÉ\x001bÛ\x000fÚng°\x0003\x001c\x0018Â¢Ä\x00068]¨^´ÇÖ)ù(Î»g8¸Ï8H¹j\x0007íQÃ(¶ëéÜ9:Á\x001dçÖRv%\x0018\x000cÕm¼\x001bÚàÍvÍ{h3ÜC\x001f¨¥²Wðs_Æ4\x0006¡}O·Úé­à\x000eé¼<TØÖë\x0002uBH @l¾JdàZÖk±Æ¶ãêm]\x0016kR*oÔðòT)ô½ØbÛ±q-qÎÄ\x0010¦¸éa8=5Ç^Üê
xÄ(\x001fÐ¡\x0006\x0005*GËÁópp®½Á
ºFü\x0008Â\x000cW£½\x0004LÐ\x000e7\x0013IàÈ*dû=\x00178çA(ýà»Yñcâ¢\x0006\x0015xáØÛ
k¨äßh«Ä\x001d\x001cw\x0012GG»ìmîx\x001eøÇú°«%Ó\x001d\x001cÉ\x001ecÀtVVÒ\x001b\x0002/¼\x0016EÛ}õ
_-öUp}5mLS\x0019}\x0014À¹raj+Q9ßÑÁ\x0003æ;¢£Ì\x0013¯RfàØK­½ ìÏD\x000cV¹hë\x0008Z[\x001e\x0012×Ã
½3ä\x0001
y¬\x0006lb¢V\x0011\x0019¿\x0012ºQ°o,yÀ[ô¼åFç\x0008Ü\x000c5¾\x0002>ì	¼bõ¬è\x001c\x0008Û!\x0011]JgÙÛ\x0005ó4É0¼\x001a´y;VÎÓè\x000e"eÌæsF\x0008î¢r¹àÎÏ"·\x00043Ì\x0007\x001aKe)M\x000fp 4\x001a
¤ûä*%z&\x0002?\x0013¾v"I9Ô\x0006<áÉK"ê1[9ña=1m)êN\x0012ª¶nÁ»¯%#ìóÙ\x000f2\x000f­!/Ç
¸þà\x0002¯É`VÏ%Ã\x001d¯Æ0E`ê´9íÀ\x0013\x0017]é\x0003uKçéµZ\ñ55py%\x0017«÷\x0013W'+ã\x00020Éfuwñ*\x0004{ûáxA\x0017'\x0014óW¾z*L\x00153\x0015â
eÿ\x001e\x0002\x000bÈîø\x0002ÿí'ÃòÃ^:?À_3\x001fú§]ì>¾-f\x000e3Lè\x000e$¼7â~ñ\x0015uj¬\x0011rÄ
¸\x001eþ\x0015ÊÆÑÄC1Äc/Â\x0019ê¤íÁ\x0013n¾¬\x001d¾lc¢¸áÅ|SS§\x001f¨\x0006¼±CöÅØçñ!5\x0019V·Kö¡8Ý;Ô\x0005ãû=ú÷øe=ïyc\x0007-\x0004\x000fÂ±ðw÷>\x0014¾÷\x0016	¥TøH/Â\x001f\x001aG\:Î?¥´oüïP:V¤æB½\x0012^W
ò©\x001dÿ÷{üß£|\x000c
Þ£Í'rIKÂÉØ\x0015ww9£áËùÿ_q§GÊÃ&é¯\x001f>¼~ñÕã\x001e4Çð<Yçâiù©³çùHÝè+ugnRp_BÒYËzAÒY7&n¡¿Ç2glÈÌ£+Æ®.'\x0004NhH¡é´\x0001l0IÉÑ\x001eâPx´;r\x001dSh|BCÚY+ù\x0019RåÚ]ÐÛ¿¨Ú²©ñ\x000e|ê)\x0004<¡!ï-4­©¬MEÃ.uuZv5ÐéO=Å'4ä5,«fpqU«Rü\x0012Ì/gÄOhÈ;+µ¹³å)Vê¨
òPÞÙÆõø	]QÖ\x0010u=EÚÙ0°Êeïá\x0001}ü-H¥yJ\x0011Ë§N,>1ç\x001eOlß\x0011Wó$äÏÈ\x0017$5ÝáO|T\x000b²V)Lh\x0017Þ°ílîf»SGTGO[´/:ÖÅ\x0017ÇÛgkµÍv	K¿}ûáçVQüJ
ûst¿èk_\x000bçÕ¹×Ä¸¶«úºèÕæ^ªøÌì \x001eÐhÙgå:Þy\x001bí\x0003§\x0016ÅÈsp\x0012F4VØÅ\x001e\x000e{4¼\x0004È-\x0019y:²ÁRt¥ë\x001d9ÐïÝ\x001eí\x0005\x001d\x001c·\x0017h\x001d·\x0017¸Ìó&8*ýÙ\x0002}¿Ð°\x0006î±\x0005×Z°ÕhË£\x0013O¡ÕÒBÇ\x001avÂNYË\	Fl\x0010QÆDäj^
\x0005ßI%T\µî^õ]j593áÎIçB\x001d<ÃF!mi¹Gîj«O\x000cACRUW&«+\x0007\x001dº@åÀåoVµ(A¾
ÐÙF¼ëëØ\x0015pNçõ¯6\x000c\x0001wÃ¹ÅnÓ¹]¿®óÒì\x0003\x001cf»\x0012ÑÎ×Tx\x000eÑXî_\x0010¿EuNc\x001fàÆû\x001eîÎP\x0001 üjMlÊPk×±·V\x0017Ûª\x001bºÅ¶j'q×Ëûªèí\x0008<1çº\x0018û¾ügÞ\r{\x0014º5\x001aýÉ
=RÚF´ÂõF¯õ-o?¸å¢µ\x0002\x0010ºwñ­3+¯w®\x000fð×èú\x001b½\x0000áH©\x001aQe\x0000/\0ö¦ÇÇv±»ä\x0000Ç£T\x001d\x0007¸\x000fùîè\x000f\x0011\x0017¹\x001a\x001bÝõs²¬£{H¹¶ªè¾0ÞB[¢çÈôztÊû¹u C!KÜã\x000cÞAõZ@\x0008(À}\x001cÕõBVØ¨iû\x0001 ;Ø(èéü\x001a¸§\x0001\x0002\x0001ï\x000bÌÚ¼´\x001fÐÉï\x0011V9W½\x0000úÉyudí\x0005Õ`6÷%øéà~s_ô\x00077¸Ø«\x0019_ÉìÝæÙÁy\x001e´¾<ìîK û¢ýz·Ýµ¥ûÃ÷}É<[\«b\x000bÈÆÀè\x000fàìö®ðÉÙÅ\x0006\Y²~vn¡)>ö³ÝÙ\x001b$SÁ\x0013Ëw'TGg>b;[¹8±;ô
è)Þ\x0004=\x0001ádCç\x0017òu'{ã^´\x001f]\x0007fk\x0001W².ú¨C¿K.Ç:Í3Ý~\x0000è\x0011æù«n\x00196¤¦:òÕ$õ
có\x0016°\x0003=âGU¿\x001d\x001c`ïè£\x000b/d\x000e}Ð'¦.é\x000fnte\x0008êïM]í>VmrvMb£ö\x000e\x0003
\x00068èKÕ.gËa6ÜIªÒÎ|%2_¥×Oð\x0008iÏ\x0006
SÓ}ÒÎÆ$´1Å\x0004
;\x0004ütã8RÍçÙ7.©EÔi×@³ûüäR8êK\x0007Xì
xp|a®"~#»r¸¥q@GßØÇ\x0014è=Íw¦M³Í,u-{,¾ó\x0004\x0012z\x0002ºö¦zCW@\x001cE>z_ÇaÓ\M<Ð3ú¼Ê]A0fpÀ¸èÄÕè§e£§ú\x0003ø¦DR">õ½î²TÙtï7/\x001b
;[<¹ÜFø¢9Üq]÷<\x000b½WW\x0004cc\x001c3\x001aÇ_
îÖ\x001euû\x0001H¥Þìfº¥ÅÜMD]*Ôiïbiy*\x0001Ù<\x001a\x0019v9\x001dÝ|Rõn@¯Ü©\x001cKwîvá¥ð+"\x0001UN|Ðs*ñ\x0001ÝÆØc;qÛ7É1È\x00117'ë0\x001d»½¼ç>\x001e\x0013­ewc
Ý\x0018\x001bîæ-]'=º\x0002\x0005cúôDÝÝÊ7¦bgª.\x00001lzyÁ±íß´îlc¥p=$xJ(\x0003s¶¶'pÒ46¹ï´AÏ(õïn<=º¹ËMÝÂðÞgë;ÙÞ<#ÚÀ\x001dÎ:]Ó\x0005Ù¼ËÝÕÖ/\x000c\x001f]î×Ro?\x0000©»»v^ôí¼\x0002ý5å~`××¥9SÖ\x0017¦ý\x0000\x0014\x0015Úº8»ÍÈë\x001cÒ\x001aÙa,P-åå@h,Õµ5-ç+öT\x001f»R
P\x001fÓI9àü¨UÃ`4\x0001G¾|(Íð
ÊT?¼ñ\x001føI\x0002×Qéê°Y{&©ºêÅ{;.ûb^ñºï4¯èjÍÀ­\x0014cähù\x0017[ÉaÞZFú\x0013Q
\x0016\x0012\x000fNÇ\x0001(Ð£+§´@?0p/\x0000J¸N¦Þ47-EK)\x0019SÙ\x001eäîþ
ÊT¾ñ\x001f\x0001¿»G'¼-~o	9vÏ\x0015O¬?ÁO¬Ý§\x0016²>\x0006
\x001eýâÝÆbQê!ÿ©9âÿ·,ÿq|à¨OBm2õõxbE\x000eS\x0011÷Ð+tÊè\x000bì[d/\x0015È^xsô\x0017à
ÒÅ\x001awÜjÄfz¬230\x000fP\x000e\x0011mþ\x0002\x0015Ñ+\x0014\x0003·Rs\x0011iÐ8RSþÊ\x0019B¾U\x0011@\x0007Æ5-º\x000e÷ÀUb­
ËÏXcÁ\x0007W	:^¢éçgE7ýöã¯/P;>\ ë 5/90Ñ(µ\x0008'=­?Ä¿O\x0013ÿw|C=ÞPÏÙÃâ9\x000eÔ\x0019í#a³\x0015Q\x0018XKiÞFþ³Í\x001f¡\x0014ÿ\x0002!U®÷¶~C¡QÜqÖ\x0017´}\x0002T1Ñ©Ûç©¬#+äuTòø\x0004\x001b+§\x0000¬\P*Ý±³ù\x001en7Èð'(Ñ\x001d^ßX!ù	^¢,f®ÞÞú¤Ã5ò`?×Ùy~æþ\x0005øTúrol_\x0010Ê½É¹ý\x0002G
rì\x0011ï¬áO\x001b\x0015õ\x001dó-´OÀ±¼ôîø\x0005?@Á\x0003>4Ðk£À0Çá\x000c½üûîL)l>þ\x0002Ôcmäo2oU1ÌÍ¤ÞR>~ÁN\x0005\x000cÙ¹"n?T\x00014\x001fMÎJ4Ë± ìbÁD\x000f×aît<{CÑ©&ßx÷ÐÈ/F\x001eï}0Ü\x001f²!?ý) ¯"øßãKY0Í(ê\x0010Óeî(ÚBa¦NÅû\x0017ü\x0000_À\x0018P\x0002¹CÙ-´0?ä`O	=íÁ\x0013?eøG«é\x0019Ý]R1£h'JÁ,²xoÌþ¡·³vý\x0017dk·oüß\x00029\x0015¾\x0005FK\x001bìUs*&ÚºÚà;î\x001alsv¿}üéÃ«×OøðlûIÌÀí",ñÕ\x001eú¥]·!¹÷¬¶¢ö_°ÅwÚ9(¾(M­Æ\x0013ù·\x001bÖ9³l=;Ý\x000cM¼bÎ
Cs¯¡ómÕÂb%é¼tP\x0013Ð)IÝ\x0007N~èÅzàié ®­\x0005.,\x0016o`þç3»¼¤Ó;iç ÁýWjùß'Z_ÑbAð´sP\x000fR%Þ/q?4K£Í©,V¨Î\x001b\x0007#õ\x001aëÌ\x0004/¤´C\x001fvY5À´\x001dØm®L\x001d72äØõ¾Á´Ø7È­ãòÆg>ò@8Ãn9ð¼oPÇphÇÑØr\x000cT6Ijµ\x001c¸dz:'Ñ;üÄ(ñ~¨s\x0005üN\x0013y9°C\x000e)}\x0014y§ñxóên9p\x001dÉôt²\x0013ætµ¶Ïë\x00063/Âµ>¬ÉôNlÔÅhxO¾ãè~î9ª\x001ee¼\x001d6j£\x000eëÝÇV¢d²MÛYO\x0016[IÒ¼~I"³ü	ì\x0019úÛ:ûN\x001bK/DdkÑG*Råa\x000fs-k*½\x0013\x001aõ1\x0014\x0010G>õ\x0000¹²DR3{¥$i^ì\x0018=NÒhOhbpÃ|ês¨»{Mtú\x0016ãRÊûä!g]O¥owù5.ò\x0014µ4ý§oXxÛÎî\x0010k\>ÜødÌ`ýÌ0k\x001dZúc®ÀØf Î¤¦@qX\x0007.´Fb»ûÞ°¸\x0011ºd^åk\x0019\x0006sÛB¿ûÞñ\x0005Äýå§\x0005g­oÙn¿û\x001e?¥\x001a\x000e°Q9ñË+	Ûõsï>¥OK´ó°6×a³¿d~÷)=)%­ÎMòÊ\x000fçæ\x001bh[f¦@8 \x0003}JóòöZ#	I»Dî#Ps=úÆ/é+1~ÈÊeP\x001c\x0005Þ}Æ@Ñ8<\x0013\x0014(cÁ°s½5våÕóÜ\x0003\x0013bè\x0001î%\x0017C£³*A,Í\x000cî\x0019\x0001Æ£J=áíÐ\x0003?[ç=^FZ\x000f1ÿ\x0006ôl\x001e\x0016Ùa\x0000JW[Ï¡V}2ûðáÕÛ\x000fï¾ñ»§7?¿ø÷?IÐò<±^,v¨Û~ü-QÙtÁ\x0001È¾\x0019Ï\x001ck\x0007³ B}¼:®'%¢Ý\x00176-Y%p atÂÚÙ\x000f; Á\x000f\x001e\x0015ZEJCh	ýé=¥\x00039"²#8ÃÌ|VA\x0018Ú,§ZNèÐD?k¤7VÕk¶ÖG'tehD64Ô¢È\x0003\x0011b]¯8 ÑS×[ëÊ$Ú*,ëÂ!³E\x00076}ÆJîc1/Y \x00035¤µ\x001b÷õçé£¸öL\x000flüG
ð
z7Õ]%ÅÊ«¸ ³k~ÌD¥ô·¢Ëõo\x001f¾{¶!\x0014?L5õ\x001dàG¶JÞl
5Úðùs<ë¥	eæ\x0016sE¿OÁ¶\x001cÛÇHÏöènÆ£ÞÊÒ®Ä\x0016ç
ÜBæbí\x000b|®Î\x0016Ëý9[¨\x0004/ýÒnNn#ÜÝ	âRµÌãéà¼v'ùAw\x000bz±í ,\x0016åq ¹ÃÕòZiÍÝþû!çÀÆÑ yZhÂ¡Ö§ÀÄ"ÄÆ§ïî\x001a¼B/d8zANð\x0004ËI\x0014<ZZõ,RiA¦û~;¸Ç¾_`ñSµÆR¨¨:%Ìsê*æ~¿\x000e\x001d ßÏ*1\x0014Mu\x0017#v\x0013Ê\x000c²âË´Ñ¸ ùnà\x0011\x00026ýPJh»aàÜ:h0d±Õ³JsàÓ¡\x0013\x000e[Øê±\x000c¢\x001d¿ÔI¨\x001dR\x0004Þ&$Ó\x001cøØ$î\x0004eºÖ\x0003IÞ|7íKæ¹e¶CghµÕ!/du1Þó¨]Ü~(À6\x0017Ìç\x001d\x001cbX§}\x0019\x0005º C`­·\x0005^Z}4ÏT-\x00076Pµ8SëÍ¦¢UÌÅ]­\x0010viMù\x0012YìÀá¨5÷PVTÆR¼á×8]ÛÛÀwRÁ®PmKj«ùæ\x0014là6qÁ¬±zäº¹)ú\x001b;$l}Rò0GR1ÜZU%ö×tìLEÖÁA©xC\x001d\x0001ò»\x001cÚÂá\x0005wµ/\x0001-Í\x0001\x001dÜáÉM¥A\x0005\x001fnä\x0006\x001e¸QNç\x0001\x0014|î\x000fp'ÏÔË\x00104%±ðf6¯{
\x0014<o¾§þ\x0000ÄâPæ6\x0001R;yæq¢Ò7AÝ«\àU\x0016'ÈÀ\x000eµê´FVQ?3ßÄÒ[\x001fËî(\x0015ß$\x001cU\x0012¹]²\x0006ÎD¶¥ïIZLüulø³Z×jÕ*=ä\x0016ÔÚ?g°\x001azûÁíOä¾%úò'r{Iï7ßQ
ÕÅ^³K1õ\x0015\×\x0005û
4!	m"\x001eVñC\x001cúÂû*cAyE/üOÆWaµñà|1¸ú^
q¬6ü\x0004ÿ\x0002yãaÖBþ»ÉÉú\x0017Hü\x0001ê"`\x0017ÕÚß¼}£{\x0014'w0/\x0011Í\x000b\x0004\x0014i\x001e´ä\x0011>;!j\x0014ouÁK=Ð©º ÷£\x000c\x0005´Ørð@ä­_ÒxÈ´è³Þ\x0015Ïc#"r\x0012AÝ$8ª«bê	MK\x000byA\x0012u"r\x001a¶èÆÖ4{S1U\x000e
«\x001492Ga¾5^³GOÅÔ$Ñ+P^«Ê\x000b\x000bÇî´Jv¸¸æS\x0019ÿðÈ>\x0004]nÂÐm¨v¶S5µ-+.÷\x001cïÚ<9·¬åL\x001c=\x0015SÑ]$p7ämÅ3û±ÑQ\x001bAÅT;\x0015SåÐ\x0006cÒ\x001c\x0003_aØµ\x0017Ú\x0017{É¦Rª\x001a'\x0017vËÒ®L-f½ßóÄu|bÜ.+&&\x000fG\x001e°\x001bÉßb)ÙTGÛaI\x000bÓx;Ì°\x0005¶ä¼¬£Ø¨\x00125Ã TNÉc\x0002mÀ\x000eË¬ÒMhèV+m^bE¬\x0003ö²zB£"\x0003\x0010Ú\x0008G1\x001fv8v]æ«NhZ¹ë¡ó¯I;YzYx¶Uä¥Ô\x0013»°Ñsp¯sxÉ§\x001evîö*Åb)Ù\x0001êH¯~Ñ®	¢×3vX/SµS¶-ÅKû«Æ/`íÄi;t¨\x0016\x0014´¬&-Æ\x001d\x0017ÌÖF°-¦\x001ap2{ua;Vìçf\x001e1oZjkRjÀI'Xel÷à \x000b¶]ÖOl¼ÝÕâ\x0014ÞY%Ø.\x000f2±Ë\x001aðW°&êÌ-\x0017 \x0018\x001e\x000fc/HÞL\x0002bû_½ýðúñ_\x001eÞ}÷â«woÞ>SõÇhf\x000b\x001eù¢\x0002òAé´`mì(ÿg4ÚðÆâO°\x000eWù+8¬æ+ã\x0012¢V\x001a\x0015§is­îåªÄÞ4PdÍÐtâúö¼y
|6×ú\x001ai\x0001C§]òCõ§ÅóJë4o®Õ,\x000fVÃbÕÔ:\x0014z{Ù¼\x0007>M«k}¡&Í¢¼³$ëÈüä.¥{xBã²ÌÊ²>Æ:ïS\x000fÛ\x001bÏ½`;hìï)÷dn?4Rc*Ýÿð\x0015íz\x0011|W×j\x0005\x0003vTYKÆÝÔÌ}|\x0002\x001dW.â	ývB\x0019´ÆõWÁm\x0016Á§ywm.·ÃÕeM­C51½`Ç¥xbSßkæÛg¸q£ð²vÁEði^^«ãGxGü°yØHàBg\x0013Ø)$5Ü7\x000b¤_ú)©á¼ØQ×û·FÒöÚÄ«ú\x000e®V8·\x0019®IX7ÆØ¨7Ñð\x0015\x000cÌ'V½\x001dT²oÔÚ]oZ\x0004+Î³\x0001#eÓ ïyßâfÉ|·µº´áå`&'lè\x0008\x000e}GÃî`ÿ\x0018´{>¤ßAþ\x0005tué»Øø-
1·{B&¹\x000cØa½õôÄÆ¦§°Ù@Ô­k\x001aÛ\x0018Z?ÕìºÐÍ	®8kÂ-}!\x000cæ¤®û×\x000elê_Ë\x000ew(ë5±Ôôé¹ëéX\x00197qNlÇØ\x0005MU\x0019v\x0011\x000fÛ"cïuß}Ij_­`¡U8ê\x0018ñ-¾Û×Nlj_«¸+ ØJ¢>BlMbè\x0015¹
6ÑÖ\x001bHoW«$x»u>Ä-Æ¤-F\dA¯wxØûZ\x001d=«È\x001eD	ã\x001doéÈû2*(\x0016åØ\x0001
Ü¬U½/\x000båVc¤\x000eÈ¨$¾î¬¥f°­vþß`ß\x0010¥\x001dckoeÎ\x000c½ô½×tJ\x0015_ÚÛ}}¸ÈPÍ#O5Dk\x0007ø6#°C7\x001eH6ñ%\x001d<hñÿGDcGáGråä[ðÙóÐÎïÝä»Ã[>¼¸¶A§
©P+\x0004/±ì\x001cÿj$dý_ÿýüõ^=×BbÝÁÌ\x0014\x001em©ôy"Eïº\x001e>~î8L»H\x0016Í0uòüD|úe*Òlê"\x0017¼£'fýEÑ¶³æ±NîY\x0007·\x0010/µR\x000f)\x0003\x001cmàÜx&v_£e¦\x0000á\x0004Ç6+Q¹@aÛx\x001eò?®Õ¹\x001d¸\x0003ª\x0014\x001d:O4ð¼ RG9(q\x0015L\x0017ËÜo|C¿±Á(u*ZÇ­\x0019»·=·\x000b\x001càØ.P\x0013¶d\x00128;°ß<s­³;ä\x001d\x0013?·]a#!B'{Ó>¨iÇNp ÀªHPDÀ´\x001bIùø²øsó;lØ¢§7g):úO;OßiÃRÃN[®?¸±c\x0006B³vW"6\x0019ÛÇÚw

7sÔà\x0010¼kJ¹@\x00025Õ(\x0014ÏÉ\x000cù:öäïØPÏ¯ò\AÖMN)ÂqÎ³!ìSV~^\ÖÁ=,.óZJpUbá\x0000Þ\x001bn\x0016ð®\x0015ÂLÄÖÁ\x0003\x0010±y¥ê\x0003peÙÅ5ê-aÈ\x001aÔÆíó¼¾¨g\x001aÕ\x0014\x00173Üw%\x000e+ôL\x001aÊ<¡Ñ\x0002æ¹³äÄ¦@ÄòÁ
mÌ0{ZEäíyÁP\x0007/ØPî»=0Ê=¤ùôj%\x0012µ×ÔæPäÀv½z÷>úf*vÚ\x0008Epc§w\±±\x0000ajð#¸æcÂæë\x000f \x00197Ó¶×Àë-%\x001f\x0004?gc\x000eÛ\x000f.p¥`C\x0006{ÝO\x000e_ÓZÚº-W¼\x001aÛÍUi?¸Á5ßH*¸JÝ*\x0013\x0012£wBS;GÛ\x0007:FÛ\x0012AÇZ9\x0017×Þèû§,µs¿Í\x000eý6^ü\x0008*:zÎËúòB\x0002íÇnoó\x001cºvt¡«ò\E¼/\x0018mìp[\x001d»~Þ\x0017×±=ìÓÒ"\x0010\x0003\x0017]\x0008ÆÜßÍä\x0003}#u¤Löµ84-z\x001bñÈ=¶ÊØÐÀ7/ûÁ}ô`éåÏ\ Ñ¾"~ùûª;\x0001R'z\x0005ôêÈQà\x0018w	ÙX¹$æ}g§\x0008\x001b5m?¸Ð­x\x0012@ï¦q\x0014
&y®\x0013z³#ÕëØLª§+âî\x0018ø\x000bC\x0011Üôõ\~&xkàí\x00077xHTqsNnÂàY¨â\x001d6`»/#q·æÁp·¾£d\x0006\x001dÊ®»sS\vùsØÝT
x.¶9`·ã2ZÒ\x0017/.¹®7\x001an5æ\x0003ß¥\x000cÓçrrv¢½ëg9q.w\x0011{×ä]¸³¨êÔ\x0005öF-Ï\x0000÷y\x0019· .»%ó-J&b_¹Î¼R\x0008 Û X:æÀÿnÿ\x001dâg´\x0005yØ½£&¸\x000cø´Én#ï;
G³W@>ªÃu¸\x0019mvySêSÌ3_Ð-|\x0008èåóAÛ£²°ðå5"ñÄ\x0010û¾.èr{Iü\x0012$aGÚ|\x0014¿\x001bÔªÜäwW'yº:¡o\x0010L\x001b£	ÿèå\x0011å\\x001f¿©í·øz» µ\x001a\x0008£µtvèÖK¹;¨s[ååER¦©{sJÇ\x0012LöÃûÒyüõålÇÿ\x000e­NAÞÊä*mz\x0016«Só·\x0011ºj7\x001fW/'rA\x0019"\x000bÕD4\x000cºò£Fë-æe#\x001d5<\x000fh=©®üÏ@6ÙqèQKï
sYð1Â³>(fð)-ØjzP¶½.g±Dv\x001ay9«Ñ\x0019:öüÊ\x0011­îT7\x0011WYUDxÊó@ëâ,b\x001eµ´EOÒ½$¼¯uBp
?å!\x001eAåF8vöy±[0VöoQÐ\x0008ÊçnwÒÖî$T\ã
¯ãº\x001dãÚ2?¢\x0000[ñ°Ýt\x0015\x0003©b*GÅ£k:üöîD\x0012®mÁ|Aá²\x000fìbêðk7ûÛWÍ²«(â\x0003íÞVWÄ\x0013J=2@ÛWHÜôM¿DÈÝôÌVisâ«Ù/çÃí\x0007\x000e·\x001ab­è\x001bIÄ
º\x0007lÈ\x0003ånx6Ò	D\x001f&\x001eOÂüX£&¥=QvLx¶ñ°`y¼ñÁ,Ûh0®R3JôÐ[°Bìk¨\x0016{roÝÂ»\x0019\x001d¶º'¨}ÌxãÙp´êu÷¤ÿðøâoß=~÷øîéÛ\x0017ÿðôþçw\x000f¯'O¯[ÙÌ:{1%Ë
Æ±æ*~ÞD}(eÑñ>7
ú<ôK%«\x000bº!·-E_JwÁË\x0003M_17Èuì©GÓÓWÇT.¹¦KkS\x000fy\x00177
\x001c3\x0001É\x00014E%ìà\x000cO²\x001cðÃøÄß|øþñÍãß<½{øðÝ3Õ}
OªË#[¡9!Ñz\x001bÙûÜCÐ­½å/¸O\x0013Ñ]HÈ\x0006$Ö!Ò\x001aÈÅ\x0010»ÕÙÚwÐÔïch´^Ù\x0017ÐÓt\x0000/iîN\G¶ÄA$G®Ô{â\x0007Â\x001bVOhjõq/ñÄeèb\x000bÜ1c{WËÜ\x0011î'»\x0010iÿ^K\x0018½\x001bÅ±\x001eÍð\x0013Ï]À4u?5kMÐ½=wûéNÇ\x0006+B*6;î°¡Ïùí\x000b#{ü¤*'\x0006ídÎs?¸¸îBô·ç£Ðö«
4÷É.ë!
?ñÑ`Z.íRÃÔÕ\x000e[ÌûZºP{÷TB»¯Æ®`>v\x000ck>º\x0013Û3vMm\x0019x\x0010µ_ÑÀ¨0Þ`\x001fX¶VÒë$Ø\x0017\x0003ìT\x0006ÓuÚé\x001c\x000b\x001eBOÁ¶¬ýfÂOtºÎ½ÀwÔYj®\x0019sÿíSÃ1
?\x0011Òio\!a\x000fÍZ#±Vï\x001eZ=Ñ\x0013#6g@oRÒ×­	\x000c>wØÌQøqBâ£L&ÊV¦¼->²\x001déÌÒ9
?ÓÝÕº]JRg×µþ\x001f×s\x0014~£ð^#?üfäùä\x0018_ÏQøK/6¹sa\x000fÅâ\x001dû
Ý%r;¥tD×ê_Z&}/##U{\x0010\x0016\x0013\x001a~féËØcÖ Y i¸$eMÒwB\x0013©jº³
\x001d9åQÜxì®8«Þ¬Ë\x000c
H\x000e&ú=4¬?\x0003½j2\x000bZd[<y¯_?6º¿|÷<K·í9ÁãÛ5¾"\x000fÓ%öêÔgv\x0015Sr	Oo
=4Ö¸ÿ\x0004Û),2çêä\x0012ú¥§x Ã´î9ÄTHNäw\x0007Û÷4Ú¬c\x00072\x000c\x0010ï³¶%eº®b{âÇg»äD>¡\x0003Bã.vhÚ,n\x001aïë\x0014çïñA«(@\x001ebàÐ¢Éµ\x001bOÝÈ8fý= \x0013CC)Fûxp}Þh.KÚ²\x0013\x0019¦\x0007µÈ\x001f1$iÏ³ØÇçGï@.lùzdÊIü?\x0014\x0005­K_ñÙAq×p·#Ö
\x001f1¯i\x000fhäµÎRFî\x0007Öë$R\x001fÊÓýÔ\x000b7ôÀFUtÔ~%¯'Ï®ZÇ¹I±Úuí\x001eØ¨bo\x0003~GG=ÛrnÈç×­ýÐ\x0003Ûó¹áØÑÑ°\x001c·U\x001e\x001bvÀ¨\x00166yë¾´td3t£u\x0006¥ÿºwËÙì¸C§Rè\x0001\x0014ò~yº}ìcà\x001c\x0010vÃ¯BüET"ÕÅb»e@§áéy$^+sï\x0011y)
ä\x000fTÛ\x000f­_/+wæÊuØx¡\x00172ÝEê\x0003Ð@k\x000ei:×ýÁ;]Fåµ6bÃæP-}Æ¹5*ø=-ò×Ñ%ÆÎäq)}3¯;ô®Ó­±tk"\x001d?¹DPÓTÂÎù¶¶Ñ.Äv\x001fÞ½ùêå¯\x001fß¿||-F©ÑÑ\x0016uk¯J#å¦Àþoy¤u\x0007çG:C\x0006C»º\x0005A¸ åvoô\x0003\x000cfAg\x001c+ô7\L"\x000ftÜ#à¢Ùqm<Ð`\x00154·\x001faÑª*× \x001a&n\x0011Ã¹{¤\x001fh°\x000b4å4¦&)¡ã:Áßl\x0016\x001eàû°u7é\x0018G ×ì7/ôþáçNäçNóæ~3"£\x0003§=»ä\x000bÊ!o£Ý¼Ð\x000frÁÃh$<F\x001awÔÃÁÌ\x0001ûIÊ\x0007\x001alMÆÄ®ÚS÷fÒùH»r9]\x0016|F\x001e!-ñm/\c\x0017};ø@ãÖ\x001efÜlË&²¤éL_Ýéìá¤ê
Ø®\x001aV
;Nj¶?w§3Ïrèd8}fbó(>5uûl<Øø)åI\x0002\x0013§¤K(aÚ\x0013ÓÊñK\x0012àÆF2\x0005í·X3ÓbÌúÖôrçé[:üÚ\x0014\x0002\x0003\x0006¥¶øt`[\x0016\x001b2µwÐ¾¥oj\x0002\x0006£X<
SIßÂ]ìÝËèÂ\x0003
R-GÄR\x0011÷<ië²£íiûþá§/>õHú·ï>¼ûöý÷¯\x0015KÇ\x0002Äúò:EcÈ\x0008ØÒ>Èÿ\x001d×²ó+­#z\x0005úmf:¥È}\x001d\x0012\x0000m.7²CäÐ
`\x001b(2Ó³äò\x0011ëFöì®P,aF¬8W\x0007;éì:ËyAÃ+Ý>/¶Z\x0018ªëÑLü6¾##CN\x0012Çx\x0004Íß]nèÐ]häYt 1\x0010'ª\x0012ëö¡ô
q«+\x000e\x001dégyÕóùHÛºË
]pÕ¤Ø¾¢¥UÏ~Ë\x0015ëF®\x000cúº\x00028©LkÞ\x0004&Çal~#7ó§7ÿßËwß¿yóÏ?üùëw\x001f_^©i@~bBïm~¢\x0002ßÒ"&²ÈK¥þÌ\x0017î3Q·ðg£\x0002ÙÄ¹Ê«\x0001ñè\x0012¬Iu°ÝGj}ö6¥Ù\x0003ó\x0003*:6\x0013Áfê\x0001ò¶4gaysoXH-½U\x001bÁ©=\x0018jòò oc\x001b\x001a²ã\³ªÏ$õÞ'êh\x0014d»
nd¨XUnpU2;Ô7!½ëê8KTpCCÞ½Êí\x0002UÎÆ(FûÁ-Úâíµy ¡^%\x0015r`5WKÓÖv¡òÞ¤\x001d\x0005ß\x0003]\x0018\x001a¸u\x0018C\x000e|	Ã®Êû@WÜ\x0008NYÕ	SC\x001bâ©ÄûmâîFF~êë\x0008j	FÊlÈ·#ú-½Ê\x0003mù+Qª½ÒÈ8#¦ê\x000fæ\x001a9aÓE\x000c·«U\x0015¥hÔ£\x0019\x001fNÑÌ·QÞMP¾®v\x001aAò»`²KÝ=Ø8Þ$W;!6s[XýÏ¦um¤tcÃTY\x000e3öÝS8Öm
¯û¢9ÝH,!kBd4ç
vhÕjÀæí\x000e9n°\x001bndlÑâ
­dÜ¸l-½\x0012vêÛ}ºXA.:$U\x0000;P\x0001@\x000c	±Îi·Í6¾»¡áJj\x000bÌ_Íf:%\x000fwjÔK\x001döÆ:l.éí´!¸hW§57îà5Jºa¯%â¥k¹ÕÚ\x0018xÕ}úbO»±q>-Jp\x0007JÇE\x00032Ä6ÒqÚÐÚ4O¦Ä)I¥O¢ßëÖÞp\vJ|üzÑ{amy \x001dB§Á\x0000¡Ð\x0005hlªq:~
ûdI¼çÛ^\x0011;PÃUQ{Â=@9Y\x0012O\x0006\x0008_Uð*]øSÆF½Ì?Ø\x0011±=è?ÔP(¬²µé´½©}É!A¶\x0019\x0015ø\x00015f}Ø"c[¾í¶uûÓéöhI²CZ½üÈÓ$^0¹ûÞ×ÖÁµ\x0008±=Ø\x0005\x001f³ðvØV­\x0013U~Ë<;Ø©	ù%ñhIöþ÷g÷¿mDÞnì@#©}\x0012¦\x0012lJ\x0008vK(Ó¥\x000cèg\x0017,\x0016Õ¦ïÛ\x001dLe§¤1ú/\x0002r\x000fôô¼\x0003´ÎÿPÏl]]iDát)\x0003>ï*©7xÂá-l`\x001f_^äé\x001eèo\x0002\x0008Fvq\x0013C!B¢J¥\x000eÿ·	Ó\x000c¿$9®Óè²6Û´§l\x0019C} Ó¯>]I¤,(ò¿ëç\x0011Wåo¢\x001déí¾Î»¸®\x001cæYºíèåôµ[sº¡þ*ä%è\x001dp§þóÇwÿ*\x0011ìËzy/±ýO\x001f¿ýøzm9\x0007}\x001c\x0005?Y\x0019¸²âi5}/IÔôìßI
ÜÍ\x0003`ç1\x0019U\x0004åNÐº\x000cTâ
M]9ô\x000eÔ»£êtâcqwâ.xCc\x001f/H«Ü\x000e\x0017\x0015=çÎ|z]r74µå$LSX§\x001e8u/Ä]*ñ\x0006ÆFèßb[DßwÀå\x0002o~ËH¼\x0013\x0003\x00035¶6sp÷SF\/Á\x0013tahíO\x001cÿ(4ÂÔEÈN'zPj¦þ§8å\x0000bÜT\x0017,$üº\x001cÆo~óñWÒ´ë-±T{T\x0001\x0018çÐ¾óÑß©\x0002»ù'ú\x000evkaÁ.>å*Ù\x0008
nP\x0001ÂÔÀRªÖvNñ\x00134ö§§Õ:ÎI\x0004\x0007\x0012\ó>Û½9¸¡§\x000eèª×UÓ(gõSÃª-Û\x001b\x001a\x001bÔ\x0018Uy¾ÅOjé=s±Ö\x0016ìíÓ¹\x000bôÍ¹r«\x0005Óë®\x0007àÆöô@¨I½\x0011Úëé+º6¾\x0016ìì#tÑÓDÖ¼gS¶K®/ (^%?mÇ,;îÊMÙ.¹¾\x0010êÛÏ<G\x0001~C¿íÒ» LYy:<`Wªwë\x0014Ú´ê¸WÜ¸±iX$¼Eõî\x001cy¸Ú©1½qSm¸íìÓ\x000eo_HâÒLGqíó^tãÆEr¡+CÉ*L6¾ý¼Èé±«z»¹®®ûN½\x001b\x001bï£\x0003É~i0ü7\x001a4ñº{Nøt!-µ½Ó®\x001b\x000b¶Êö§uïe7nl\x0017£ýI×]&õë:Í\x0018¸Ã¼ÈMº÷~´\èºÝ4¿`\x0002ïß·s<Øx+\x001d$vë.ê²\x001b§ãH\x0015  \x0007i*¦¹1ð¦ÏØ½ãât¼qì"\x0018\x0013z¼P>Mc.nÛÌñ@#Á~-o3Ù\x0012\x001a\x0012_ÔíV}:$¦ô*QhGx`)º	»\x000f¢>¤ÃÁ\x001f-®¹Ï¬;LCmn¥¼¡=ÍæXö¯Ê4\x000bÅãÊrþz\x0006ôô!=q¾çá7+6\x0013Q)YÇt¶[µm¥¼±ñKjÎÓ³}¥-aÊwÛÛä­ÙÑìÞÎ4åâÓ[z-ÉÂ¦éxw¢Èõä9)Ì	CÓ~úîÐ@hq5«kÞ¾#Sì¾¼ùíû×9Ñê']4oê£T\x0017½\x0018\x0017 ÝW&ðÅç¬SÐ÷{\x0011ª[\x001f>oÛW\x0019\x000f_ðâ\x001d
a\x0005«ä\x001fXf\x0010]\eÛ\x000b{\x001cÖ59ÎRu\6\x001b"¶þwÔÇ]\x001f¾\x001dÍ+kK\x001aëÖ~"ë.|É¼¼ê0®¾WÇF:¯ÙR\·§Â³
Þòùè¼½'ld¿\x00151á£Z³¥\x000b¬dxüåh¬\\x0006\x00178p\x0019hhâz\x001eÒöÖê¿ÙùÓÂ\x001d.\YF\x0007´Ö^pô§\x0019kZ·m\x0013)nÕÊ½°A+7hS\x000eª\x001fL^£600÷vlÉX¿r`vp\x000f\x001cAþë¸ãEÞÂJ§ÐN²
Ê/\x0005\x001b\x001c
\x0002\x0012ÖV\x000cª|]:r_È _<~å\x001c¼ÀsP© ²ÕÜ/:¥òõ&Jò>*!¿q\x0000\x001eÀÇéÔª¤ÀxVäÆÛrUIV§ c×\x000c\x0017ß[t
ªü±*å¢cO]\x000eC¯	\x001c¬JðhU\x001c
\x0016\x001eÌ\x0004'µ N\x0015Ê	¼ ¸\x000e\x000b×Óðl·*ÿñÊSK[Æ=h\x000f\x0002\x0012G
\x0014ó×5myg\x0015ùpÌõ\x000f\x0003¼X#Ò\x0011&<åÙLØ¶Õ\x0018ãª«|cÃA41 Ò2cÀhS,bVL\x001b/¯'ðò¢»ZAo¯@®+©VÚ)>W¡\x0008\x0005?}ÏßSËæÈê\x001f#Å\x0019®¸I#Ç6Ç´Êßà°-ÑgLjiS!s[¨ÕB\x000e¾@ð¿A\x0017\x0008ÿ£ÛiaÝÁòí¬<Ä\x0019zNËM@ªà\x0016\x0003Òèµü\x0007J\x0019Ç½JaÒº;í¥5°ñBÏÿðs\x001eÒgÝ«¾\x0006\x0017zÁµGÌ]è#é¥wÉ\x0017T[·¡o¤r::LGï2sUB$\x0011ì&ÛÒgÌJ®{¡\x0003¹nôÑ`&ªÔCPÞIgÊÛ.ZåÉ/ð\x001b-IñøHÙ\x0011?µ\x0014'\x001aº;}T\x001fU^QÔlÒ\x0016\x0006lÓ$\x001b-ý\x0006_)ä/p Ñ§ÑV¬þV 2¯Ä<7&42oê!g\x0019£FÃ¹Ðþ³HèeÉj$²\x001a:\x001dÐ\x000b|Ó\x0014I`®ªl\x0008fÕ6¼dóé¦f¼©µæátY%o£11kX§(Ør\x001fNLÆ«TU4t(þ\Gý ËÀ¾KêMhùðØµ?\x000cô\x0010F\x001ci½Î3\x0018'µÄÖ<\x001f¬zûÃSâÿ¨õ/Ü+\x0017×ô¤µëWÞgHËÒr¡\x0017\x0013ª\x0006u¾¬\x0012\x0016âS\x001a´3Ñ{±ö¥â`\x0013ã\x000bX\x0008^»gy_
\z\x0000°ô¾ÜèÐû"è~4TËÚë¤¯ê#\>_ÀÄ±¢;*­Éqjµ¤I\iab4Q´¡\x001fvÆÑÈpeP/Y{\x001ae¬Ýrî8æ\x001e9sp\x001b\x001dfN\<H¯YKÓcrqh[Ämïr¹«.H¶XõÞB-ÇªCcqÓÅÅ¡\x0003#qÏ8Ö\x0013zEôtedeéÙ\x0018h¾E"ÌNQã\x000e\x0001LûÃ®ÉÒ2î©Õ¦s»H¯R¸T³\=¡WDÏ¨d©üÔû+\x001f£t	:zR3\x001evFÿð 7«±3rëÉö	Ü÷ôDµ{\x000f¬ýaµ?­×cq'j#-§Ú:{O9¤/Ú\x001f\x0006z±bÈSÜ\x0018'oÝäÎn'\x0007cMµÝG\x0006RmIù\x0006c=í¬1\x001bÄÈñ]º&¹V\x0012Ô'¯\x00034Aüý·ã³Fñ\x0006po\Îg(×*fv¼M0%"\x001buB¨dä§BCÉ\x000c§ëÎ®q÷¥\x0005&Úä\x0014ÑÓµ¥\x0019,}øÚöÑL»¡¢\x001d?ð
Ë¦Þ)i\x001d¾Ó(@Ý\x0013Výgh?ð-\x0006\x0013àZW\x000eUL\x00013\x0012Å>E¦0\x000b\x001bíø\x0017´=~ Fn\x0001-[\x000cþþ\x0017üþü\x0003¿\x001f(0\x001e+n'Õ8ù\x0002ìÄ¨ZP¾;ã\x0007øúÏuÒcáC¤\x001d@×\x000f.\x001a±Ì7Û?"\x0006ëäPÇPx§Ä ¦ëÑ:üü\x0005À&\x000bé\x000eÙ¡Ì\x0006ZâÉ²þúÃ5Ð\x001føï\x0019då\x001aµQqÏxþ5¤Þwª\x001eÙþ_ ÁÈäaL\x0016[4ß3ñ`&;íýõ\x0003ûAû\x0001ø\x0017¨i\x0008`ì®?vü5
}&Kaö\x0017¹ý\x0000\d¥Ü\x0006·G¾1¦'[q]¶k¤¢\x001cîqÃÿvògá\x0011ö<j¢2\x0014|l¼½åý=n?\x0000÷¸\x0011£%2"~ýÆ³rãý=n?ðûWùýEn?\x0000\x0017ÙÄD\x000fV4i
S lïCôó\x000fü\x0001¯A\x0019s[ò/CD\x0004Tn~
jOÌ\x000bÌûó\x000f¼Ç\x001f  ÅEÇá*¥ñÒ\x001aðtÏ,Þ3±\x0005ÝPñ\x0014i\x0018%(í?ý\x000bLWL\x0012Ó=³xÏ$\x001a\x0005juùäßRÔÅ\x0014á\x0016Ó-³xËb½,ÏãF&.3=.1¥÷\x0006®Åk\x0016«Ï ~ªPÄ\x0004f¦ç8ôÁ\x0000E9Ý2·L\x000e\x0008èìõ/LÞ®òÐ\x0017v\x0004S`N·Ìâ-ª0
âòsË=\x001f(v:BåÞ¡Ó-³|Ë\x001c¦K­K=\x00161Dô£x ×\x000fnÅ[\x00166zÀ\x000fT®ô¨Ð\x0005»D)ßètË,Þ²Ø&4\x001cÿ\x0000f\x001fkbþ^ùzýÀ\x001fÏ?ðG¼\x0004\x0005:ïÒDTgir_={þtþ?á50h'Tó9pZÆNï±½3J\x001fÎ?ð\x0001~Àa\x001aR(ø=\x0018nú|\x001fÓ?àÏø1ª¤T?×cJ­r^?ðýù\x0007¾ÇAFCä,çtdêZÕ
óÃù\x0007~AÂ>Gù\x0006lµ¯MÏ\x0016~À<Çô/ç\x001fø\x000bþ@\x0018$
ê:â´\x001f`áôî5*Ê¿ñÿ\x0005K Åè^#1Wqå{VÓý\x000føxþð\x0003\x0001&oå\x00074gFÍáyºÈ=ç¡0\x0000PàGö\x001ak\Fºé"?×àÓù\x0007>±G\x0011á\x0007ä\x001a0Waáêj¼æ\x0005æ§ó\x000füÿù,\x0017&/ÕqÛÅ®b\x0018O\x0008ß{S*B²î\x0010äkäÈÀ6Ù8\x0001Ù¿ö
þk·cØWà³¥æg'¯Ý\x0000im²î\x001b><÷&¤|vÔ¶]úDï¿\x0017qO	\x0004­ãR\x0002!(a@bÄ\x001dXVÐçSóZµÜð\x000cA»ÑÍ\x0006øÓß¾ûá§×é7-4XC\x001a\x001fj¡»Rÿ¥ûb¶;\x001eÀe^P7ïwÓ¼ 6î\x000c/O¯ÉÔ!Ì5
ù¯÷`mÓÆÛÀ-µñ\x0006å{#W\x0002_\x001e#\x000f¿§Îäe7ùé\x000eN]ªàöÒV\x001dàG%to\x0006£V^°>c\x0015¼Å7LüÎd\x0017©¶fÇpu\x0007GájÙ\x0016ÛbKb%¿\x001cyp:.Ò¼)9tp\x001c·ÕVJü ÇM.ÔJ)O]ç_^u/p\x001cJtÊ½Î'n\x0019L¬ è³\x000fW\x0002ù\x0000\x001e©\x0012cJýW\x0011-^ÌÌà®%\x0000Ëáê\x001f \x0017\x0002Æ©ù¤NMÏØ±SÐlZ\x001b¶'v\x0014Û©Æ«X]äïÉw¨ö®£M¡¤S©xSÐ¬\x000foâÖXJFèä|[ùé°xO:\x0001ù-,Ü\x00139Ä¼á¥ÏÓøe\x0012ôÆIP®Â\x0018\x0013ËkäÈØñêº=í	DãÆN\x0015Ô3sjù\x0012úQ<qý\x00035~Ã\x0005ÒîCG\x001b\x001eUC|Ç¾òÓGÜpè`°A[piF¥°&àÍ	K}\x0000OØE\x001d\x000bÖH$þ¤W\\\x0012$?¤õymZ`\x001ax 	R±Õ9hìË2=¤,ïk\x001f%3±s\x0011îóÂÍÎ¾1ó,»cç6p\x001e;òÅt¸uCîs3ýF e&/^å³§\x000f°óB2x!ÿïÿòîÇ\x001fûL¢x$¯&\x001b \x0017\x00147)ï\x000c¼P\x0005OR½Ô\x0010¾´'\x00125výùÄÜ\x001c\x0011\x001cIôÍî-Çq¶Jp×Ij\x001dÄ«sA£S=Úç"?Oå$Î4¹ì·Â\x000174MÔÁe£Ðg·JáØZ \x001bÃ	\x001a§\x001aq&¢M \x0013t\x001a+ËìÆ\x0011(¨SN)?y»d¶äo»Ä\x000b\x0014s\x000cÌ+dù
\x0017û6ulíE¦ndª8G¤Ù=à­vZtjbè«U¾ É*\x0017ìì­[\x001dÖ\x0000\x0008Ú·DÞú\x000c^Ð¤2\x0015p"¬Ê`\x0016Ø°
º¸ù0Ø¡Ñ"ûR!©`t¦Ü\x000eyR§Nê-\x0001Ù\x0003M#´´¢CJ~®å÷Ôéé6U$\x001f²VnB\x001d2û¦çBN\x0007ÛNU\x0015ßÄ¿£Fdj+]gê°ßú\x0007Ø\x00009\x0016£G\x0012ë¬~j±ÍBÙrØqý\x0003óýÕE«¬\x001e\x001eñ¨\x001f¶ÜBWâÒXØr¹£Äo6©c\x0007ï\x0006Ûtfä\x001eÍà¶ÐÌ£¶²\x001eTå«R3µ0c]Ø\x0011±ô\x0003_L»âé{Vç¹Ô×5ÉÜÎ\x001d¸ßÕå­Ñ\x0013ãx\x0008ªîNLY*·YA}×\x0013&mô&\x001d®ÍôU{ü»fî{D\x0003\Úø\x001daíâ=ñÚýôø4\x001e!ëÖÓ\x0003\x000fÒÀ>WwlpK_Í§ä\x0012xJ\x0017UëWýôwßýðZÂ
QÂR¢\x0001Ñ\x0019û_µ}\x0010\x0018ø5of¾<'t\x001ba×å*ËæM¾LÖ²%J«È%v*yæ\x0013t\x0012³ï¸C\x001fè\x0004ÐÞÎ.v4­Ñ'AwÅï$\x0005\x001eè\x000cÐ\x0012}¾ËÔÂ)éËqÛ§ûF.\x001cÍÈ\x0002	´vX\x0012tö#-Sñ
]\x0001:¹áª\x0004R¡ò^Ôâ\x0015AÇ°»/lx»³Å\bs/v\x0006MGºìÅ'olë\x000e-·qckíÁ}nÝÎ¥íã}cãñäÂcá6<íµ`ì®´øÒ7¶gl`û\x0011O¹=·=­Ûô¾Å¾±\x0003`Ëÿ"\x0016Ä¦M\x001e\x0000÷¾íÅã¸#\x0002\x0017:Ù\x001a¢Ïq¶{2\x001bîc\x0018M\x001cºfCÊQÂý	û ûscãtP\x0013TÅ\x0013fVÊLØ¶î¹\x0004nh¼¤ÃÚe/\x0004M-Xº%{.\x001b\x001b¯¤M(:ux°=ë¥Ûê{Zö
ÚYÛ£íÆÿ¨5#^wÚkOÞØp%µ\x001fTT\x0013£\x0000%öb)ºç<}°áJ¶Â\x0019\x001cK\x0014n`ÏfÛö>íÓÌfÖI3×Æ\x0011!xtÙÚU[­ëÆÿz\x000c,ù_Yûé\x001cìzà´\x0018+Ë¿`ÛdÂ®qõyw¦_øEo³ç_pvþ\x0005dæl§2Ó¿ÁÍw©%Å×Âßs*Á
Ëâõ\x0002ëbQ1\x001a:Þ°B6·ïûýÌ/Øù\x0017¬\x001bShý\x0017\x001c½\x001bn+ª½Â>ó\x0013iþø6ÐwMÃduÚØâÒªô8FÐªU%
keÙ åGJ\x0010¨Ñ\x0012&§/,è_óÊ2Î2÷eÔL\x0010û]-Ñ\x0010dÃ;\x000fÒ\x0016E¥i	Õ]ô_§àKÕ\x0000ágÄ=Ö\x0002\x001f\x001d0½¬}fÉ­5éqô¿Á£_\x001a¡Õsô#±\x0016Få\¼>kq¼YnV6(\x0003\x0011Ä*\x001b¶®\x0017ùÜqõV/Á\x001f­ÞÑ\x0008 Àg~\x0008Å
[ã§\x0008dCýî«¿~ÿþë\x000f¯VôUTiTýT	X=£mç/L²väwkùH6P?
lÈ0¥
PäEè¹â2Ci\x0004<ëxÐ]\x0011[yÓ\x0001[e/*mtâ\x001aLìvfõÚ\x001a¸Å\x0014¨M\x0011Ê½V¼1Þe\x0012q=ã·>õ\x001d\x001bé¼äøQÝ¸ò$¯I¬®«,ÚF\x001b\x001crÙJ0	©3ù1N°FÝÒ ­/|Þ78òy[GLM­÷	ÁÃD^]L\x001f?\X·\x001fpÈg[Sé{ª..nR\x0014\x0010¸O×¸ê	\x001còÎ&\x0007Z6öÃà¹P_®p'ö$Ò\x0013\x000f\x0007gÊ%LéØ§-ß\x0012|iw[Ò' öØ\x000eë)6\x0007l\x0012r\x0012\x0002a§\ã@ÅW	äúÑ	Ü\x0012x¥æ\x001d97Ôw\x0011cå&\x0000×Á7áC\x0007Géz
9¢Y\x0019¹\x000f\x0005.üÕ7r RaÃ*©%2uÑÔîà>¦£Y\x001c\x0016°ñ´'LrèÊrk¸ÖÁ3\x0014?\x0004~h\x001b+xæÞdY³Cå\x0010[GÇi[`êX¨Åb«¤\x0018mX#%%×Ç
O»\x0002T\x0012¾MFëcC¢\1 Ác«Ql¨^:8R½x§)«Ñ\x0014%NM MñüBÄÜ¬xØä\x000c\x001av@\x0002Bç=r\x001a\x00128,?\x0011±¶	®°Ò1\à\x000eÁåá\x0012­Qý5ZxdlßidÖ®\x000b;RgQEf\x0010±L\x000bJLg>v°¶E\ÐÔ\x0016\x0011"rË«*\x0008uç\x0004æ$WíJÅ^©X.ì[í\x0018ÚW\x0015 Híç&\x0005¶*Ó\x001a'×È¾cÙFgI\w#Q\x0012/<7÷4n
;bO\x0017>dé´\x0005hAÄ\x000c\x000c\x001e]'\x0003;ØÂîw>¾\x0004iõ¨0}"U©±A\x0005MÔÐnu.ðàbEÊ\x0010GÒâ5ÝÍ\x0014øn\x0006Ûfb>mK¦mV.]yfþÄ\x0014'q\x001aÓZÙãÉbE´XÞWHè5pzótÄ1mÛR\x000e¶Vÿ\x0000í\x001eåÊ\x0014¼Ð\x0007eu$Óº§ÓZáëÐÉÐç4(ô"á'\x0001ÇÂ_ÓÇö5Å??a\x0007´)\x0005\x0015\x0014ÄÉ¡$»\x000e\x00191xhT\x0000étT\x0012\x001d\x0015ùÒKÓñEg<\x0019\x0016\x0004r=íÓÁbé\x001f\x0006¸Î+¯©Ê²ôþ\x0010o
VèAÉ§w3gêÃUMW!b\x001c\x0014¦I\x0012;ÛÁ¹Ö]¦\x001eÎú­Î\x0016¢IÒÿ!å2JZ*²É\x0005^PÙD{\x001fýø)4±Gì\x000f%;n;\x0019X'ìw³f´ãQ\x001b#ÉÖN[n¯\x0012¹98è\x0012Q\x000f\x0018l¥\ÑFpÜZk¯öl\x0012©\x001dÝ\x0011:°Þ\x0008º\x0018HjVN\x0015õuì¡Ûþ¡h\x0018»î±õjlÉ\x001e\x0016V\x0001­ÑõRÒÊ¾rCO§\x00054_tô\x0017î87XÅjÅ¤µ\x0013º£S'tÓ¤\x001e\x0010æÆ@ô^g\x000b\x001aú¦\x0012ÑÑÕX_
?6]	ê©HELK'zvk7È\x0005\x001e'ÛÆ\x001dÕ\x0011[\x000ei3\x000cµèsÚîðô·?[n -^Õ¹-\x001cÓ²RzîæÅn8\x0018;ºgîA&Mënó\x0008¬v;\x0005£ÝÐ$^à¨c}¤¥;ÎW+é
ÙÜÇFýÁ\x0006´?K\x0004ÆK´òl\x0018ÛÅ+\x001aß¿Eí\x000f°-\x0015éZA>)S\¸tÑùz0\x0001ú\x0007pÍÓðp\x0005=±\x0012¥Ä\x0001ôD+)Iêè³®\x0018©\x0004¥,\x0019ÇQGäÉÖæmBï´ØÈÃ¶\x0007Úv_pÛ%fBÐHÃGÊcÓ\x001d\x000f\x000eº%\x0007]G±Fr½ÖéµÜ>ïR\x0017v\x000cùðMõ\x000f\x0014\x00109Ø\x0017cèò»Ð×\x0011\x000b\x0019GD4k?\x001c.}13]ç*\x0011=^­}Ñ\x001cö$R;lH¶¯âº8ËV½0zhI­M_Õ}Um\x0016z{Ç¾â,Â\x001c¯yÇxH¶?¥[T7\x0013Óè¸;_b":,1vn3jÙ\x0019Ínô=«VMá®$qé´DÓ[\x0013ÓéÉHôdTêù(b\x0002\x000c=¦SÅ!v%ZVó\x000bhÎµD5v¦ÄÄ\x000cêâ.ÑÚ»¯+\x0018\x0007ûç<Tlt*~\x001aHâwrMz+Â"w££\x001cw,\x0011¤`þ¦Á['Âéfü¢Ê¨å¡\x000cS\x0002§\x0015\x0010Ð)õC\x0007?ly¦{g¬7ñPB$[¶\¡Ö	ÈaÏ3¦+UïÁAýK¼<2]©:þ =£hó:ús¡ÓèOr$¥j\x0007t\*®%Fw×¶ïÊ¦÷ÎÏó\x0010Z*ä\x00028N¼pKÅ5\x001c.Öñ7äoü\x001bòÚK ¼aGÌ°#fÌÞY\x001a!ü\x000e6B
æÛñ²ju¥\x0013Y\x0004<^]\x0010s¾9oC\x000feÎötW0Æ\x0017%\x0000¼P-Zé¬\x0002³\x0010=\x001fø\x000e c;Ä6Ü\x001f'«SÚ°ìÂZ¾~öç[Þÿ\x0002\x0019°ì¹à¢á
ê¬òê«ï?þ;Q
ÇÏ$	&GOÎpí©AuaÖRííÜ`/ªf×á\x0015}Ø\x0005J\x000e\x0004r÷åE=ÀË_\x0010^#áùÉ[Î\x001c&²(¶¼¶-nMÙì\x000f¦!è\x0000í+¨-¿^¡ëá\x0003h\x0005|\x0000\x001d»\x0018ÍKUå,e\x000c
K\x0008K\x001cFÎáBä1Nè{ø\x0017ñÁ\x001b\x0010X0,r#¶»\\x000cÈþð\x0005Z\x0008^á
´:'ÇÑ7Oi\x0018Ñz{xÍê\x0011|NcF<é"×g.<y"\x000f«¿\x0010¼Çäà»É?\x000eýãÞ'%×ô°|½Àt>Ík\x000b\2\x0011¿\x0019¥~¡ü¸5±ÏµUá9ß \x0007NêÖ+¿,þ#ÿØ.þã6Ä{Ã:\x0000z#$\x001cöYUËÈüTÊðæ"\x0004#¸ÐØÃù\x0007Üþ\x0002\x001aëEE®é_ æ3²ý|\x001eefüÀ\x001fù\x0007\x0012á£Úâ×	¿\x001fÎÃó¥\x0013¯\x001cÐ:Tã§w>²qðO²0Àåÿ\x0019\x000fÅ\x0015]à<hä&ÕXü¿pä\x000cü?ñöT\x0008T[Âr\x001eD\x001fè¹\x0010	rNæ?$2ÿò>BÔ/ágæ\x0002pt\x0012!÷ªÖÉp>Ç¡\x0018R+çÄÃáâfÝ©¿£\x000f4÷Øµüb`à\x000c;Ð^\x0018¯ÝDW<·ãõ/ôÆí«%OiÈ\x0014£=1\x0012ò¦Ñë®rÑ\x0003-ÙÏ\x0010g\x0003Ä]_:ÅÛ°\x000e\x001bA\x0006Ú¡\x0007¡'¶æ\x0006;9¡ñ:¢'\x000b]\x0003 ð\x0016n8ê\x0014y\x0005&8QÇ«Ìp0Ðj@qù!\x000f\x00015-\x0006d®x%;ëW×¾ý'ûéük\x0005Æí×\x000bÌÏ/Ç\x0019b\x001f\½ü«Vÿ
L´­\x0011×o|$áfÃ\x000e¢ø­C>\x0003
õéç à\x0017Õíd'N8O¸@¯rU'½P]#pÑ$tåsu\x0005\x000f>:ø\x0003ÕG@	GæLøaëz\x0001bj\x00166¹a~ë'â\x000e£¹\x0002z=««Ç®I¬_ò°~ýÆ°~£Ñ©%'Ú_ÈÈ9	»¯\x0018ìàB¨\x0002'èUÙÕvß\x001bÚý\x0004O¼\x0001fJ·Ä!R÷ÐìÎ\x0001_þB!à¤4ye\x001aÔÕÙFÎÍ¤;ÆÛßfðûÊ\x001b\x0006É\x001a+WQ\x000bÇÝDuò\x0012>o óouÖpxÐ:(F;\x0014cL\x000cn\x001bÍ}:}`ÈG4$Ü$+ËÀòýn'úð\x000fP'úÝäD;²Ñü\x0003Ø\x0000àê]9½aß0SQäRY^9qHÙ`ñZ[\x000e[@NA¶Kô\x0000ÿÂû+ÇäðÂë\x0001\x001f0²?uäÉªÄ0\x0014dxîV\x0017óÆ?¼\x0001o±ã\x0003kV¸²åË@r\x0004>½,,uã\x0011Ð?B\x0018\x0019±LµÝ {5åp\x0005J§o,V\x0008¾±V?¡â_\x0005\x0006ns¦*®ªUûkN´Ò!5âG\x0004x\x0005´A¾\x0001gjR'Qoçð\x001dqûd¤\ËP¯°úË­W_ß©Ã\x0017Ö\x0017ltÀáQ­´ôm*iòüýDPÃ¦\x0002\x001c
úÜ\x0008=úß½ÛÖÂ\x0001bï¿ùðòoï|óúðþEi'_[\x000eZÇ;lxsÀ¬ \x0019é/Ï­Lë÷úYn\x0015Ù¾ßÍrïÕ£\x0004jÎã:³NL&jJDºU*øR£²Ïê\x0004Ü*Êx\x0008úX§ÙuâÕ¥tw##\x0019Xñã©ÔE\x001bÒ8ÓÄ$C¶eV¹Y%GÔ	Ï¹°®óÛ\x0010Ò	\x0018yU2Í,è})ÑÅR=¹¿mF³o`¤UÑ²\x0011\x0002[îx«.×Í\x0007\i74Òª¤bL
M$z5Ú\x0019Z=þ¥Cê&©wD\x001f¹¸é\x000bºIZÓöÂËRº°éJ\x0002	c	8läatÏ&n¢i>\x001ca\x0005®6MëîEãÓU$b½Õú¬ÉûÛn6ûÆÄÞ\x0013î§gOÕ^&è¿í&³od¼ÁiuE2\x000bÕN´ ×(òé6Ô»7(\x0007ª«&v¦:É^É²{­ø\x0017Ò;P»ië®=±ï¸q÷wÒfáhØdúdGÜ%y{Â.\x001d\x0000ºP×¢¾ÙÜÈÓ$¡wí\x000bÅU'nD+3aseæÓ\x0015Aâ=h=ÏâgPq»LTë®·r¬ÃÙ76ÞIS±g^ª³yâó]séMÔcÄ#Ú8pCe\¾\x0006\x0018OW\x0005ê#_2±qáV·D¡OwÒ!õX!ú§,îC$è8\x0011¦¹ÚåNØx'µQ>$\x0019©æ\x0003ØO7\x0012Ç\x0013\x001a±9\x00120Õ,0\x00136M)öéFºÌ;B·½Ð\x0000°6ªNÝ³N7Ò!ck\x000e8«¥âS4óTüdI.ÞÓÓtØI,~BDlÖ@PÂºI³yg§kCÍ,Ô­õ0sg-\x001fVãºö²ÜØØW\x001d²¦é§4=)¢NÁy¦¦,³
MÝ±ô\x000e]êf/yÚÇ\x0017Æ<mPÎ>8&¹r3ExÞÅ\x0001l#\x001b,êã\Ní\x001a	iÒM1Ä(YÀo\x0002+¡ÔX>V+1ôåS¨N/q+¸Ï¬ÞÍ«¯ÓÃÆ=ó\x0012~N§±kùMá±`Ð_ÀP§Äé2¥À\x001bäÚ÷õæÓéì\x0018`©íÏ¨¦[ÌäYV\x0008×7/ùp¿z÷ãï¾{Q\x0016óÿú/?½{-V¬\x0010YØ×©^éýï}\x000eC^§(»\x0016¿<+VlÖèg#\Ù¾)ÂM!; PH¦R8\x0010"wKÛf@\x0017CtãzÄ
¯\x0012àÂnJÎÀÈ­¯b1D7tDèú\x0016=Q,
òÄaÛ0ÐòXÝÈÇP@;bQh^´mõêå=¹¡QA²P\x001b`¬êhMq¡{[êé\x001b¢i(Äö\x0010å\x001d$M©\x0018M\x000e´ÛÆ/76~G¥ùCl?\x001d8Q\*Ø§\x000fiñC
Ø¨*a 
t
v\x0013¶ÝF\x000276~J¹ÐX\x0012Å@gZwÝ	ôO\x0012Üõ\x0014åé\x0000N\x0013¶´ìÄ%QÛõ©VúÂ\x0006Z°\x0003\x0016££ì~àeOÛ´	Õï½±=b\x0017è\x0016¥RËeÊ\x0010
m·¾é

_2Z¤
RhK«ÎÜf`Mô[\x0007òÎ\x0008êbGJ|X&C¢»óÃ!\x00175ã7\x001f>¼¼¼ùêÃ»ùIiAÞ«¹|§£z&4¥>\x0012\x0018)@¼Ä¦¾prÔ¶\x0002þÏ=\x001dºóÓ¡²µ #Q4"Æ\x00035'\x0003mênÏ	Ú1´\x0007o!{ô5CM{¿÷|	\x001edÈ\x0011%$g\x00199dÑ¬c}/ö \x0003BguëjN\x0013të5ï×\x0003M
Á\x0005\x0004ÓÄVQ	T9Ð±]?}ý\x001eäÄÈ~\x0004#Ê\x001eî\x0003/·Út>ÅÓW´ø\x0015µy\x0013\x0016í&è2	ïô<ô2qC{T5¶\x000e$ê\x001a3}Ê	Ýø%>{°-c\x0003a¿¶ìDþ¬9,Þ|óO[âqKÄÁ\x001aêrF
K|VÎbZßýKè÷@ãÉ6	ôOåª\x0002Í\x0011k\x001fÀXb\x001eh8Ù©\x0014"Ì8\x0006ÄìQf0µ×*æ þÁ.¸ì@G»Ljé59^vj\x0003Øá´îë\x0016\x0007£àº\x0013¿Ô5LòÔµtâ\x0013vÄ=É±òÁ\x000e­\x0006\x000f{ÂU\x0016SÛK½L\x0002>Øp)ú¡ð)­e1Þêfìæ</J4\x000fvFìÉb
{\x0018uRÍ3Í´Ó§\x000c\x0005¡
-áF"	§í.-×³¨¢<Ø\x0015±3Ø\x0017ÃÂ²lêÂ	¦SO-\x0013©76L¤Ê§ô¨¸RL×´Oiy»Ks\x0016\x0001À\x0007Û"v\x0005
A£cúÖíëô)û£p2&Ñáñ\x000eXÒcB2¹Héò9édM\x0012X\x0014+g{2¿8<x"[Ò
ÞétsRäc\x0002Èúâ$ÝÅk\x001d§ðâ(í\x0004¤ItrV=Ý>³´°\x0016<Ðxot\x0014\x0004\x001dhK YÚØ´itº6	¯Mrx´³6}34WûLo²O§k*FÔÖÅ\x0001KåÆ\x0012zº6\x0019¯ü/¤(Ë\x0006ÑÑVNiÂ-¤]èD\x001el¼61p9ØSÏ ¬{r´S«4çÓµÉxm"ð^¹ÆDØ×Ý§¸óéÚdº6X"JÔ%ÀÛ%MiÜ\x0007\x0017_²\x0008\x0013ù=gL2Ê[ÂØ=éqº49ñ\x0019\x0001¬¢U\x001d>~e²"­G|éO\x001e¯$ÿBß!.\x0003\x0018Ãr£¤ùb_ÌJÍ+ïyé
îõ¸øÊÆ~\x0016x$__6_Vç´1À¿CKðÏ*ÂÁï<+EN´\x0010¾Ûñò |&1ós5dXæYý;vx)nOg¢\x0017(òö»ÉÁjJ^³Æ]¢ýùEPXfïàd"º¤âó§Å37­,¾S~¥5©\x000eÛIuùÀ¥ÑÓãÕ"'Ñ¥é'Zëd\çáðÓñ´T7$\x0015'ðeÚ fÓñx¦éx\x0012Å]\x000ei
²ìäsu
Ç¸4&Ãêñx\x001aÍDêA\x001f\x00109\x0012\x0017\x0007º±#-]½Ã\x0011Xî\x0016Ô3\x001c\x000bÆÉâYå]eo7\x0005\x0007TáøêÃ»o^Þü·^«ÔàÇÏù6.yý\x000b\x0004tq\x001a42J_=6Ô&¼ôó¥4\x000b%ëL£Ö ÓZ\x0014ÕØJÁ{vÍt74<éV¸ ÇÝòn¹ìé®	5if²¤Ô8`¬è$@y-tÅ¯5if11\x001d;Çá2ÒfeèÄl2Úö¼ö|¦©çóÛ7\x001fþ÷ÿü_ÿéO/\x001fÞüÓû×":.ÉOn@z´b¼øc\x0006 êDJ³\x0014_¸*ÒNÝw-Ñ§µï3\x0019t·\x000fÜÑ-ïÚ\x0014m¶nµ±%-}ª\x0008Õÿ¤ÔjÜXÀvÉ\x001a³ïûLkß§§ç2éð".u}5-Û¾Ï´ô}ú\x00120µ©cØ\x0016í§tÛÅîw¦V3ú]Iy²HºrPJÝêòÜÐØ×"î\x0003dSLÜT Ï1' MÞ7¦µùÓù·\x001cìÔ1S¸÷S~(n\x001b4ÓÚ i
:m)p2Â¨\x0006ÆäR\x001d(ÓÒDékÂÈ§as{Ò|Çã¡Ñ1-¾:ôeÓÕS	Ø÷eÂ\x001b|\x0013w'\x0015\x001a£Æ0k}Èúô\x0015-5'¹1Ð¡¹9ij Réº}S_Zú|¡\x001c=|'\x000f%\x0010â¼f'®Û4Þ¥¥ñNÙS\x0001[¯#
ü\x0014k¦ëØ\x001bïNß4\x0003L\x001b*væuKP?­»\x0017\x0004\x0016rl
M¥}UjþhÐ¡83ÝIÛ\x001bûv½2÷êgb_ô/X§Å\x001eÂ\x001d\x0016[üe=ì\x0018«¿ÑÁus=òÕUp}fõìõ¡¹þ\x0019&r§ØXß;Î¿ð-þÕßQÔÝ^l§C]0£©T64dê8aäc\x001f\x0013ß@ºùÅ\x0016ó\x000c\x0014*:Ií¢Þ\x0007¨Èy÷`ßÈp×<\x0016ée\x001cÛLîÑ¸{°odx°\x001cK\x0018¯.¼¸£<5\x001fRÞ>Ø7tDhd\x00121Ó$É$«näJ\x001b
\7?Øº\x001f	&5¼¥AºiCB\x0006ßàºùÁ6\x0001*Ê:\x0008>1ªû<3ù4Fõ\x0008n.pôª¡ùleË$>;c¸Ä\x0008®Ã-ýì\x0015ß:\x0003\x00176:\x0003&@òI½¬Â¤Ê>3hÝÐ\x000e6:\x0003ÆÃpS'æ Ís&\x001eëqötþÐ\x001d«FÛ\x000e"]H3Yê`îç\x0007nl<%Î \x000b¯ö\x001dsî'¶ÙÐ{ËVàÆÆo©å\x00198&qÞo7mdÒ.lt\x0008ä?C\x0016£¢´ût\x0004yK|M[wàFöx¸\x000bÎ\x0016¹ül¢,åàôyìØ\x001bZý¿\x001cTñ£Ñ\x0016ñFu\x0006`ÙnÊjûê»´*y\à ä\x0011Û\x001f¹Ûè\x0013¹\x0001\x0012qóµ¬WÏìªsG\x0006Ì[,·¡²tWÞ.ÏFZâ\x0006O\x0008îÑGòâ e\x0013é"ðÐæ¨Üª\x0017pg\x0004\x000fàMÇ(-Ö8¼\x0008;Þ«|°ú\x0007Â6\x000bòÂ+©öúÚ+ nåÆ¿À\x0013\x001ePqr-ÉGK\x001d¦X»uK¹ó\x0001÷x\x0012-EF\x0015\x001a·
×>&³T%\x001fpü)\x000e¥.£¡0Ãéå0£³ú»¥zøãËûÛb\x001dS	8õJùÚãÝR>|À+;Ì_kC,V\x0010\x0004Üó\x0005-¦>h¦ÛP<>ê\x0004(­Üð#Qc«Ãíºæ\x001f7#\x0001£ô \x0003ÌdrSbs^7BÌÆØa{÷æ·\x001fß}÷Ó+å%Î&\x0012`}ú\x0006\x00166VAL·k_:¹¦køyOÝ§%·V¨O)_qòØÌ
gr­·úsJ\x0007Àý°©
:8Ó¸\x0002Wóp!{^3N\x0003é»EÓÉçºlé4u'h\x001cã\x0006ã¢ÔÚ°Áý`}¾|}¡.\Ì«é¨6ö+°8¢¶#q Ý§Ö'äÆäW.4Àd#Ybbø\x0018¶ªÔ74M>G¬\x0016kÓ\x0005\x001fÀºï¶ó=®¶ìÆÄZÎ|*ñUîß°¡v
\x00032Í=ç-lÚÑFi5Ù	;\x001e¼ô\x000b\x001boKNT3-ï³Å!\x001cô\x000b\x001a\x000fµ¡ý!îÑ\x001a§þÝ>Í¿qÒ/l\x001aç·xúË<\x0008YÃÔ.Ó\x00035õ9Ù4nU
Í*ùÊ´¸bBxÃsë)p»ã6#ür¨)ÁO§\x0019½¹6ìz\x001fþ.Kõù\x0017òèk_;sôßÀ'½6¢ð_\x0008Ó/È7¨Ð\x000c¥õU²<º!×´}e`o|¯y,vZEð.*Lø\x0004~£Ñiñiýá§OíqýÿßóJïª-S
9¸ø¤À´*\x00085Ñ5/í\x000b÷ãF)2?¬«ô]¿(&\x001eÛ/] é%kâÄ(\x0012êAÏºccV8
X^	ï©GM·Çxã\x0015ï°ÁVÄP\x0016±¨Æ71¡dÎ¨ÊO5~¸Óº\x0003®[»¡$Q¼\x001eóô{kÛÛèthÔ1â\x0004ÐÔtÍ\x0012ß÷dó\x001a1\Ø\x00101x
ùÐüô
ÈN\x0014(ÿG'»Xå\x0017\x001a¶Å\x0019õX\x0003¶_NõGÙ8¹2¶³å\x001d ééhõ\x000e¶ÛYjí´v~\x0008c§IZC´\x000b\x001bB4\x000c(Æ©{ÇÍRVÐÙ®¹\x0013Ù6%á¦h%\x0008\x001auTÑÎwFÉ;MÿªIÕ¡QJ\x0001LA4¥g>ÜÄä\§ÇÛH£tlF5R\x000bfeÕ5\x0001\x000eJ\x001fUpë\x001bÞÁ\x001d¾á:
î<\x0006!Øót}7'\x001b-­ZZÉ\x0017ê×Øts|wòüF*¢!{®×+ð<ª¼z¸#\<õ®5Dù¥oùFN¨¹Tû\x000eÜÈ*ÏÈû$}§±ôå`Lô\x000f\x000f¶ª®
¬ÞRzÚ:*
gS\x001b¸f5;xÀ¬¦>Î ßZCf±(e'ðh;\x000bð*üÑÁ!Gb3¨»­·ÜzéÐ¥ëÿ\x0006®\x000fï*ß\x0016Q\x0004]\x0018¶ØN§£6OÖ\x000c,l²\x0017¡µòn\x0002OØs£UzÃÍT¢\x000c\x000b7\x00140Z?H>7ÎÇPN\x000b/¸ð\x001aiË³\x0016¦-Ï­\x0002#\x0011Í\x0001¼ÂaÑ\x000c/Ä£µx
l`ÇW\x0016ÓÛu\x000f§<¢`æ¥#@\x0017Ò¡³Å¬ü÷[/ÕéG<äª	ÀUeð\x00064}Í¶ìæF.\x001aå\x0006ýªÒä¸n9I¼'©{Ò§g-â³V Z×])M-ëfÏJóÔ
¾QYíà¨²ª=xR*óÛPü´ã½\x000cXOÛRa[ª\x0012òÊ±äj#KgÊÊ\x001bÙHÚ\x00087ðìV*­4\x0006\x0000äìB"\x0003Gñ\x0005¼Íû¤Øb\x0007G±E¥\x001e§ê¼²ASð\x0012lëÁJ\x001b\x0019·\x000b\x001cö\³£G<Ìôv%³\x0012QIËäÂ
qÇsA%®|\x0010#Û\x0005\x001dhíÖ\x0007ð\x000c¾fi\x0012T>\x00004Ä»âÔ»¦\x0017\x000e{aOj¶ÁÇÇ\x000eÉÛ¬¸³×Ý:­s><Ëú­m¥q{Ï'%OVE\x000cX[øéç¢ê\x001dè\x0004e¢V\x0010\x0007u"<ìE¤²Xjà\x00052¡:ð
®GFñlZ.5\x0007 àËß
\x000es~â['0ZÚ]DÓÈâÖóàYp-u_6âç\x001d\x001c*T\x0002n!+eµÛ\x0000\x000bõ\x0002>ïylÛ²Q´¾Àqåû¸ü³A½>hÁ\x000fê\x000cZÄ¶-VNTÉ²ðÖr!Öm]!Ã¨,xpúÂÑ¬[yá¾s|\x001c\x001e
ñOPQ«ÎQR\x001aòÇÜtl±\x0005kuº£;¨N\x0007ÕÁ}QJi*#YÏé¨K'ÊßhÄ6t\x000f©Fùb§:t^äÁ/¨jÐ6ôÓÎxÜ\x0019bF2í¤³#,ÊhyÌÏbÑg	\x0016\x001d^¢l%\x0017Ôéñ!uý	³÷Û\x001fÆÒ+ôÄK¬ã[,\x00005¡{«í}\x0012Ëhõ
\x000e£Õ¡\x0016,R[MÙ\x0019ªõ&.µä|\x0011ûoí:z \x0001Näj5Á¾ü<\x0013F\x0014/ôÓÚa8\x0014\x0017[Ð*ã\x0001&/]ªT¾P\x0006^Nà\x0005À.t\x0018K\x0017\x0004*È\x0006fÎ,W¾¾\x001cò+í\x000f\x000fxãj\x0018+×!]:ë\x0013«8ß]3ìdy-YÞ¬ÄY\x000fx#$Æk\x001aYÏHëÚ½;ó´/\x0015÷E\x0007À/Òq.\x0014ãÐ,ÚtM84ôÒjG¯®Ý\x0001\x0016ÖîHÇÕeK=iQÇc®µ¯,Ý÷âa\x0016PÏ/L!X%XItf<ãçFa.ïý_Àïþ\x0002ï·Ø­Ò2g\x0018Óå\x0017"öî´êV\x0007ÿ÷/»\x001fáùð¸û¬\x0004ÃÓ£jüµ?«\x0018Ê³?_Ãþgç\x001a\x001bg§\x0012ïìOó×%\x0014ÚÃk%\x0001ÉzÎ³çóî:²\x000b?÷ç\x0007Ø±^¥g\x001fç¬\x001aGÚÿÜizÅ®\x001cöGþû£¹Ñ§a[;\x0012u¸É.ô$,señþ\x0001\x001fÑS¥q½Æ \x001evf½0¢(\x001d\x0015Ûzðÿ\x0007Ô`ê«ÔHE+9 \ò\x0007à: ûûÕð¿ùÕ\x0007TÉ·ç\x0003\x0004$øJ²	é\x00011Ò(A o~ÂìÿÕ*æõ,ÿÏ°|-¥BW\ûLîIÆ\x001bÛ |8ã\x0000|Wh\x0014Yb\x0005>sÍÐ^Ë?ìÂÃîÔ!£Tb?n×ë/ëö?ÎðÿãW\ùÃá¿ ÂÍ!
Ù6ú¸qÎAÖëì¯ò\x0012ÏòßÁÝ
\x0015J`Á¦¥T¯³¿
>ø 4Z\x000b6áèÂÉ4QKÞ«-(ÿýÿßaýâï\x0004¨$DfüÈÃ[×öÑÝ	IÝ	f.\x0008§J\x001dtÕVêÛ°ê»pvüú\x0004=ÿ\x0013þ
ÿ:Äd5\x001d©OÞ2½¦Þ/ë¿êh>èïÑ¸ufª'ûÎ\x001csjýéõõ÷íúþ\x000cÿ=\x001e\x000b~?þ¸ÿ92ümÛv"[w\x001e\x000e[\x0016¬Ü8J\x0001[/\x001e&\x0017jJo;³\x0007\x001eß^yÌ\x0003g?) <^èë2pò\x0002î×ßÞF¸_:A0ÒÂVÛ\x000c\x0003Å\x0012¤(ëâº_«\x0012â³ÿâÏ\x000b­£Ú\x001díÉ¹*hE¼ÍÛa\x0014ÿë_müåC\x001cðÕ¼Á\x0007PßÊB2TéaÐ|zÃ\x001cÚªñÐ×ÿé¼þOx¹RsFÀw »:Åìu½þíÿoèä1z¡ö§Rüo³÷sîJ Î¿#deQsX\x0010)lß7SÍ"t\x001e¤}VüïÐwðÈ3®ß7ÑþÇÃÜÕ«òwX¿ü\x0005×¯d\x0011Pí¯\x0004Åvòóë½»Òi\x0007|ù\x000bÞ/«ª{2DÎ)ÇsJH§ëë®:¯Ï×ý\x0003?î'ã¶wÛ\x000e/»n=º)é\x000cö-%\x001a§Z×\x0013Ðä`x4h).\x0001µ¶n\x0004ý\x001d\x0013¢F-øvÃyZ|&q6-bÀøqu&'l4SÙhÃ.zu{\x0013KÄ·/O\x001bÐëô2\x0005Uç8	@\x0001ü\x0014#Ò8ËYoÖíK³R7ôg{e÷¦\x001eáÔZ½7O\x000er\x001aÁt]â5YæV^¶ \x0008-ÐÒ3!ñ(»B»]Ëí
,¸*\x000c«NL¤¤£HÜÒJkÖçB\x0006¦(\x0000>oòô¸È\x0013­
ÞöòÞÈH¯\x001b=ÄTX*1ëníîIs+oRñjd¥Î<©çyBnm]k²:Í­¼)\x0001\x001bbu²\x0002õ\x000c9krUº.óéè!vÛ\x0006ºJhèÅÌSZ³]ÃmÇígO3\x0018°ÙÑÏm¦uÛýü/@\x0013rÑ\x001a	=%ç\x0018»ë÷Î¥3FÙQ¡ã´loyKRè\x0019Í\x00136\FND±\x0013µG\x0014Ë´ì°'ê¾±ñt)Õ\x0007:3CgØÜÅ2·)ùÓ)!n1\x001b´Ûu:%¡°±N]êjSGjà÷/¸íëØJk±¼Þ¤ü\x0012]ë£ôÛ\x000f\x001f^þõµ\x0006W¬s4D\x0017´\x0004=|¦RI;K¾<+:ÏWiíjwqîj/óÖ@"\x0006{'ËÔ\x0005{ \x001d°Q'©ì)`k\x0015°ý$P\x0012÷¯7vÀ\x00060\x000bÎ¥,»PI"\x001d®\x0003¹ÒZLÊ:DÐ¡\x000bö9ÉTÈ»H\~«=\x001c×^Ú¶ké­c[l\x0017RÎ\x000c\x0014Òî\x0015KÛm§­ø¯
&\x001786(q\x0003ê\x0002&GÖA»I¹Wµj\x000fÇÄâ1QÞklTMD\x000ec]æP¹#¯\x001a<\x00172jðhs#ºB"PVl\x0001S[Ä|ù\x0007ð;"!2äïªvSzÈpþUóE
ü´òH+gSyCPC[À¹{RÛ6ö-¶\x00178¶Øæ\x0018Hd*v\x0017\x000fN!<JÀÓ-ýáb:Ô«Óm±ã\x0014ê'àîIÃ±µ-òÛM@wpG\âHØsÍ|ë'F\x001eß:cÜÚ
{S+lÅ¦}eS¤Öc7µz®ÌíÖ\x000b\x001cÛ÷¸-ÚUD.r×Ânákký­õÉ'dfLÚ¿J»2ñ\x001aç\x0016
»µ]èÂÎ?'ä¡ÒOUÚ\x0014îèKÖ°O{ívÊ;QYQû{ÉH5f1ëhcCö8Û¡¬ÝÏ	CO,Ò¾yw~mo¼°±½QÏ ¥'¥õ\x000cÆ¡êW\x001dµ\x001b\x001c®fª\x0019ç×ÛÎàÌÛ\x001dZ~À¯-k\x00178\x001bxº÷Q\x0013Ðô@È\x001b\x001e|§Ó?<ú\x00070*\x0011_6Ýr2µu&|nÙr¿¥\Ø8¢l0ß¡ØÈ\x000b*/ò4\x0011î/²þÃ	÷\x0001\x001f%hÁ)ü<ÙñIÉËøÖ\x000f£T{ð½Ç\x001ektíæ§m¢Ë× ÄRãzÌ8U\x0000c!þî\x0018øzÃ"öêXÉuÉö\x000c|,BÉ±pùµ7>jfzMëuüu*îÁÇ,°)H¥¬ú\x0003ÜÆ?¿ ñZþ:÷øÀc\x0012²\x0014zä¼S7¢Ê°\x0012¾ßrOU¤¼¦î~|ó\x001f_>½\x0016÷Tpâ\x0002	rüHV9L\x001b\x000c.ö\x001abùÂqAyGlºª¬Êþé§\x0001ÕduvðôøÂ\x001dâÁ\x0019"apÅ·Ê»ß¸Á
Ü\x001b\x001c\x0014êÈXe:P!Ã«Â\x0019û.O,Ñí\x0001¼\x0002Ãf<,]§
UoÃ¤\x0000×ßÚpZyàÛ1§[JÑ>«+7\x001c%_ÌHÙ\x000b<àÊq|YY>Uvl\x000b6ß§­è\x0016Õ.cQ!Í0Î¨¼¿&ôóm»LvÝïíî\x0006Ç§EK¦I"¥Ð©|Zºr³[»;¸ÜiÔJÂ3J${\x000cÉ2¹\x001ax_rn¿öt\x0018-\x001dÆý(ÃêIg.\x0013	5#ôØ¼\x001c[NèÅà=*\x0015Tòª\x0018
ÙTæNcî,]¶Ð+¢»\x0004Iòêgy\x0012Ïn¥¼\x0005ÍCº\x0007oxÀññEÔ¨9b³\x000ew=uN\x0004ç6^T\x0003w\x000eÕ\x0003;Îöù°b¤âµë,oxu:6ðê´¤¤n
Ó2§H\x0013r\x0004C|²\x0000\x000e-@R)8\x0003¦Þ\x0015RÍ÷²{±'Û\x0005cGÛ\x001f\x001eðTákÊ²1\x0014\x000e%Ð\x000c6µñÄ¸\x0012\x001atÌ\x0008­j\x001fcÝ®NUÂÔçN"ñ¶åé´+	wåVÊ¾×î,ÍX¨ÙCNbëÄÃ\x0001=Cc®Äí	\x000c£X)¨Ý×|\x000f¥|X{ð\x0002³gâß\x0005HW}>Ð\x0005û\x0000$<j7ÔÕÓ%ªp²¹XR)Ó\x001c]
¼1vYV¸£E¸WÏ\x0005Ñll¶¦\x0007ú
ît\x0017ë+¦}q¢Jôj+ù}ºü¨ÿô^~î^É:\x0017E.uëÁ½\x000f¶Ô¢âk6èK×ýLÝ°x.qlá\Ól"&å@\x000cOöqqp\x001e¶\x0014Ö7t`hÔwKTä8!oË~7rdäÈÐØ×¬ÐSF¡	¨,	\x001b:MÐÈ1`©%R¡Ý\x0004mw¿\x001b:3tÀUÖÐS¥O6 Ë\x0004í\x0008\x001a3f
=!wÇì\x0000mÑrJ¤\x000b\x0013ùc4Óà¹Å´ÝØ¨û'Ñf\x0001Fâç\x001d4vRôX2\x001576êþElïkC×Í|ái_S¼éÊôA×\x0007Ù²A6\x0013¡²+âtg,Þ\x0019q
`$0ç@~G4ì¿\x000bv\x001fe8Ý\x001a¬W*iOÂÝêu	4©ú§kcñÚxO\x0004Uú%\x0019ÛM6U|µ«8Å\x001cvî·¯Þ¿|üøòû×\x0012VÐaSÞÃ!« ó\x000eÒ	.6ï/­\x0018\x001bâFl|3xÛIùpð6jy\x0008ò^93r\x0012¤®¶&¼µEâÜ«
³C¢Q\x0002[&øøÎ$\x0008vê\x000fn\x0006î;6\x000eÜ'k3Sç¿­bÎuÛNÂeÖâzÃ¶H¦¦\x000c5£ñNî'Ö:\x0015¦X\x0010ûÌÍ¦\x0002ÞÁsV\x0007 ë1B\x0013`ÖN¬ÇµsÎÚÍi\x0007Çªâát~æ`ï\x000b\x001d\x000b:º3lCð"5«||¸lå\x0015m\x0019Ìµ	£a{â©\x001e\x001aÊtÈIjÉD
)\x000ed£fð
×?[*y\x0007Í®\x0010a\x0005OóË7\x0010U\x000eà\x0005\x0012»E^
\x0010LÒy>ôä\x0014Z\x0006wµó'¬±
<Z-Wí.XùÕo:À\x000bs\x0008Kèßº\x0004\x0017mÚ\x001b\x001c´ie%\x0011h=hêÄ%óÆ6£\x001dO%ÒÀ½çÚÈDG(QýÄÅ\x001b»k·æ»/pÌw×@2RÚyDÛÑ1Û¹ÞxÚsçOT
ÑòÀæÏyìô\x000cë\x0019+]O$yñâæ\x001dàw%·¤AZËQ\x001d;a9ªÖvE±©×_\x001aÏÜ6×è\x00055Q\x001dµ\x0000.\x0018X\x000fÓÊ«ÁF+7¦yc®\x0015Ñ¦å?å°ÅMå¿Ð\x0018ev3÷\x001dfî%þJ\x0000^,3°\x00157½oµ)¢ÓI,	Ù\x0002²'±@1y\x0013ðÎ/´;´IupL)§\x001a¦Û_gýÜ\x0008Û«9Üþ
Q¹c\x001fn\x000b±T)3/Ö-\x0017â\x0004\x000eã¶Nü_ 7Ò©dêã¨\x0013m)®¯üðA+<ÎA§\x0015I\x001a\x0013(L|\x001bòä©e©+qó
ÄÍ:]\x000bW\x0015i\x000ev~p1ÇuðÃ;T¸9x¹4\x00188ÊaÁ¦iu¬\x0018»O8M[C<\x0007%ÐÊÅ« \x0006þ¶­X§\x0003vDlÇÐ11=CÍLr \x0007³uÏ5ÕyCªS¶Ü \x0011·¦KoÞLÝJ6÷fu|\x000eè\x0019\x000fÊSB+Tâ¬­O\x000bBÁ\x001eÎyû\x0003¬="CyIf>.L.!þT'=<Ðí\x000f\x0003Ý\x0018RiÍ\cµS$\x0017£»¸v\x0011ª¾ÑA¨Zg½¨ILlpåµó`­K®¯}í[ºÑqg\x000cñx<±ùÔ:­=Ö«kï]´?\x0010:\x000c\x0008\x0014O\x000fÎû:u=HË'2cÂKÎ$yºrQYçXsÑ\x001d}ÿd´?ÐWEÆ:í¢\x0013YÉ§\x000bþêÎskÑ³£;k\x000f\x0006=FuÃ°'ÅÀlÞö®°éÃnèÁÚÉáÀPj\x0004@çai\x001f®\x001e¿\x000e~ÜA\x0000µ\x0002ÈpÑ&~´Æ~]oó6y7oyuÓ¼¥
²KM3I¦²âGî6fÖ\x000cÂÔâ¸DØÐÙÌÜÿb{Ã ,í\x0018\x0003´c\x0010=PY\x00148kålbÚsÓÚ\x0019d£×¹ç\x0013@·ê­~½F\x0005Ô-a¹/UÝå\x000b\x001d\x001dzð¡]BcwÄ;£c7ùÖù\x0006ßïM\x0003§V\x0015\x000fÌ$æ ¼à_¬µõxäo|ô	\x0001Ç)TÖC\x000b3©RøV×Ï¸¿\x0004í\x0003Ãèö!Mwà\x001fÐáÉ\x001bNu(k\x001a K«ùW/ýøòµö¿B¦LE.l
t_b\x0013Vêÿ\x0014gt<\x001e$ôB»/+Ó×`ÍmµX4é\x0004ÏÓ\x0002?­í\x00036#GòTõ®Eµk"á\x001e\x0004\x001d_h]\x0017´\x000et<\x001db]ÉÄËAk±áj·;6¼9.¥Ð&wol\x000f=J\x001d¬x°~õR\x001a6z)Ú9J[:`õ¼
x½\x001cfð6TÑ\x001d\x001czò\ô@®§RG¢m¸å_
§MÁXkæ¨ý\x001e%\x0006¨5ÀÛô´\x001bNÚ\x000b\x0018¾d\x0010gÇ\x000c·dá\x0002+¶X²BÚ Þ:ÎN;aGüp©Êà\x001fð:!»K\x0007ruª:rM°\x001fÑÀ\x0010^Õ¾Ù'®j[Â4F^eQ÷ÝÃ\x001d\x001c»]K\x0018ÀÊS\x000bOIöWz\x0015y²éà²qÑ\x0015ìPÑ&ùÇÉoà\n\x0011ÿ®ë'mø:8ð/©=a¨ªæØá¶$¦\öêÅìÛ|;8¶ù*Î`°\x0010p±\x0001\x001d3V½þK[\x0017ÙÁVé\x001fÆIÑæØqwÔ\x0006\x0018<,1Ú	¼vðÃañxX|¶#Ù¤àv6pGýÉ^·ZÚaW\x0002d²xS¬\x0000<\x001eN_8õÊzßê«Á\x001cÖ\x001d x«0¨>çC\x001e\x0013EÝ,JX\x000b¡\x00178\x0014B%,0Ã=ÖCîGv¯]ÏÌo¥ËÆ=¬:^\x00178èx9§D<Ã\eø\x001c\x0006N\x001fÈZZ\x001e+n\x0006\x0015\x001bxÂ~Oh
¬÷h\x000eÅmæ»_[Ø°£êíàxÈÅ©Ä»/6{°Q_à¼rÛ5¥6É\x000e\x000eIg+\x0010üè\x0007
-8ÀíôAm+ßÐéupèÚqÚ\x0014ð´¸Á\x0018ÝÀ§\°÷M\x0017)nÂÌ\x000epå)ÂoUî|÷Ó1)­\x0017×C¢¹C¢ÙÙb¡TVöÐUjy=i7(m¸Å\x001br\x0002nqgbmøt9§·´êX\x0018;ÛNÓ{8)ú­\x0004Ã\x0003ºhjØ>ñAiïfÚT:4Tñy¨Çë²
\x0013Ëé{Ýy\x0013\x00177ð\x000cq±3\x0015gkQ¥M<'òÎ²ü¥kbùäNdt'î0¨=¦Ä¾Í¶fL'¢Þ\x000e\x0011\N]ApÇD,\x0019;ÿÖ&ùvChei£²¬à ­ÔÑâ/³Rjì\ºÜ[\x0003/{ëcG\x001fJ\x0001ÚÑRÛ\x000e\x000bÇñ1µ©r:,\x000eË>nùlÐ£à\x001bY\x000e\x000eýt:­Ýz²
l\x000emåº[L­åUÍ\x001e\ÿ\x0000+O£EºªðêÈêõÃÂ¶6uß³nz\x001d\x001czÎèHßÈ(ýMÅûi#M:ª_kk1*¢[lÇÑQo¤j³.dj_:»©ôÆ\x0016³Qoéè	×n\x001d&S,9\x0007ºÿ¼ëò4÷°½¬\x0019ò^* K\x0010\x0004\x000eÖéÀpÁCÅ\x0000zViÃÜÑ\x001fYÙWÇÈêø\x0016®Ý\x0014V|Ì½\x001dØÚÃóÜþð+}P»Ópéà	Ï£Xªu\x0005TÁÚÆÂ}ß\x000b\x0013ö`½Ú\x001fÆÆÈW"ç-?¡âûiÌåêÓØÄ\èã£Ú^Ëh²?[4_ÁMÙª>êì\x000e7µýa¬]ÉFÇÕÂ;£%oBï\x001a\x001dr-öF¦ýa {ª5y\x000fô\x0010
Ýè/%ôqr82ú\x001eh¤Ê'Ï\x0011®	l\x001fµ4ÒÑ\x000f_ÕAKUõ\x0005
2fp¢¶}ì¾ÔK
i§rs¡güª\x0015æî5ºsôQ'¥êZLßö\x001dp\x0005L¥zpÀ¶^æ\x001c\x000es\x001e\x001d\x001dç<¬êæ\x0000ºÎ e:î&ò¶^ó\x001bä\x000e\x001cÉ:3D<õdÝÕ\x001fº*z}Ò\x001f\x0012\x0000í\x000fðQ\x0013æ}£!\x000fI³$,q\jo6Y³ÖwV\x000e²Ö¿4/\x0017Öõþ\x000eÐ+è=\x0016mö"\x000b§¬í\x001azÝ÷«×¿àêe¯¡Íû)²\x0008¦°iº
;eÃ'FYk\x001dýÃ&þ ýö\x0001´DÅæåi¶×¿a¿Gíßð\x000eMÁR¨VA<\x0019\x001cÏéK1g±G3Çüÿ\x0011*Û\x0011=¼T¾²)T}ò.]t:ÒÄX£Ï\x001c"¦ÚÜ?"ªýë,[îáÇñ_Òô\x0019\x000f£´Øc>K\x001eeÃ©£Úkn?T 6ûçïþõåã/o¾ýéÍoß}üøþuZ`NZÁRÄáÖºÒÕÌ«U¢"¡\x0014UM_<±¯#|&Ø%íûÝÄmµR4è}t\G¦ù<×i¬·òÆ.s9\x0004­8Q³Z(®\x0010mkí*Á¾±\x0013\¹½Ç$gö\\x0015dj\x0017¿ñ-Oð
à&\x000eq¶T\x0015èÌÐ¶â'hè\x0003OJ2\x000cGÇÕV°\x001eç.ñ(ë&ËÓ~Cãø\x0010Ì\x0016¥Añrùü\x0011cëó\\x001e72LO(\x001dÃ\x0018\x000e­¶<2ç¨ûÍéùØNO\Ð8=\x0011«\x0005b)MÑñH%ºi§÷Ã\x001374jSÆ\x0018nu!þÐÀ½/N±·\x000274Îâ)\x000b\x0000,ÛñÈ|ÅÉxäíÀx?ÞëL3²!¡û îé iZ
x¦Ýpç»Á#ßLû\x001cë	\x0018fAõyÅóá\x001cÏÈÊÉäKîZSÇJkva#­Y2ÿ)Ú>N_1\x001b
éM}\x0018tItÜØH~§>ßXwª¦yÞ°ÙÔ\x001a­[ÒÊ2§#âü®D(h\x0016­?àÌ³jð²k§<A#ù]Î£ÙM }!Ð ï.cwbß°\x0010³>V\x0015Y\x0002¢K¥î +)¯6À®u´:{\x0003ýë_}¾ÃÒ\x00011Ð¿ýÕk·+ÙÅsÊÁE\x0012x\x001bßÞ\x0005ºBÓ3él'\x0001ÚxHÏgåIPíÏ	ì!ò¢\x0005qÊd\x000fÛö,Äc{¾ûõv\x0011\x000b\x0019è¿ÿõÿí±óöü¢\x000f\x0010^ÎëùÕëw»AßÇ½Âç]\x001dà8sûÞ¾¿ùþöº¼\x0016eJ
\x0013\x001bW\x001cZå)]½cw§WêÏë\x0017vßi¯Ý-ò/º[R¾æõF_K¼PòI=ODvÊ¶µ½åÆ
\x0019ÒY$I°§¶µVÄX»Aohô(k¡ðb§ÉÂ@\x001e¥N\x0016¶i\x00134:\x000c²\x0005\x0006ù2ËÑ
ð\x000cÝ6du)/ht)\x0002¡Y\x0008Lºx.!u\x0006ðÕ\x001d¹°+:~\x0016gXTÈ¸ÔÏíH7¢kÙòÂFj
åg\x0002Á

ø\x0008.oÛnhôtJ ñÓlH¬H\x0016Í¢qÊ\x001bÞê'l\x0008Ã\x001aE ,[~ÊÓ!qóÙ6} i}\x0018ï\x0013\x000fc¶\x0016g 5Ä`'Ç¹MmÛi§\x0014òlúd:+´\èøeÇ¡ú©/P<
ÑT\x0000¢©«/ð\x001f?üðcã¡ýøîÇ\x001fMy\x0005ÛÙ´­0¡sZO"¤^ów>*ù(ýÂÚ=ûwÑÐ\x00063\x0005D.c\x0018×rGÈ¨Ý3<Ê-#¾Ú·\x000b\x001aìk×wÔhC\x0001QFÚÏG\x001bÝ§Æ6T±\x001d\x001b¨bRÇ¥Q\x000cj0¥\\x0013'¬MÏm»ôÂ\x000eM
\x000e:\x001aé	«V×\x0010Ðf¶cã\x0010­+Ú\x0005=ÎOL¦àfpê\x000cì|\x0006\x001bÚß\x000e\x000e´¿®Y:í\x000eô1ã\x0004nª]§Q/p+/@3¨å\x0006æÑÔÊ$e{íÕ¡¿aéà0\x0014­
rcìB\x001b\x0004-ò#¶æsÎTç.üp8*ú\x0007ØòW6\x0006\x000e\éÓà.wª¦ÃYqXÍ?ØÏ\x001a\x0013\x0005_ÛJ.ph+Q2¶ÖAvëè\x001bêä\x0008\x0016«8ts·öc^ØØ©Zìx\x0010m§^\x001e\x000bº3ÌÅì³vÙ]àÐe§ÿÊ1½´RØ\x0019\x001fä½öÊ[[npEµH¢+74Ò©|Jïg«YodN;8ÊÊ©-H'èt6\x0015·\©²iËk<´e]àPÜôÊXeÆýÔ¢r&ð,¨¥&7®
fhm"S«äd¨\x0006¨)DÊ\x0011KàüÍ§°ò)ä+¦<NñmÊU\x001e=¸þá\x0001÷)`w x\x0006³#¿ÉÛÞxÖzé\x000cÇ$\æ÷²£|­ò\x000111mU\x0017ù§¯ü÷¦à@\x001cQeïÛI[ñkÍ´-í\x0018ÊQ>àË_\x0010ÿ\x0017\x001es±NKÐüØ-\x0008\x0005Òà\x001dÕIwú¬6fî7Íºµ®ö<¡XÊrsÛ/èd-Z]±\x0001üøw*\x0019ÙäErlÿ\x001fÁÄX=ZFâ\x0003Ù/jßï\x0002Jaev}Öþ
lMc\x0014J×nÚ$öXûTôoQúÚ\x0017ù¹±ö÷°vèÑ²¦÷mä|vW\x001fâ\x0004\x001cØ\x0000ìZ±¥O¾b»_\x0003¾Ò\x0010 Ë¹eF\x0005eÉD
üïÐy<öÚÆÚjÊÖJ§Þ\;³d¢\x0006úï\x0001=ùÕ^9Kv[¨eõþZýáÐ+þ\x000bÚI~FSÇC\x001fx0C\x000e¿\x000cåÆ\x001cø0È¥Cûp©¬êâ©\x000c¬\x0012RL	\x0016ÃÁTøopùõm%V?gä[ÃSYó»ãÐÎcÄY\x0010\x000fX÷¦L¾õ\x000e®	Þ\x0001ÿ-Þ)S\x001aÚay\x0014\x001cøNÙÜá\x000f\x001fVáÑ¹ñWòDWoUí\x0002AeÍ\x000eøß£5³ØX©ð\x0018&«úFaøÆ"oQ,\x001c\x001föOpk½Çæd¥gÀar#×Ï¥\x0018ì5F¶\x0001Òÿå§7ÿñã»ï¿}%y\x0016S<H	
<¼¶i´)5¯\x001d¿¼<K¶îï\x0011
}
ë>`|ÙÉ\x0003qÚÙT&\x001b
Wåtñ§nhð§$\x0008é\x0014¦\x0011s#Ç¡m\x000b]\x0017§þö\x0008íO\x001eEÏÐp¡)[ÊÃ\x001b: 4Ó\x001d$GLG\x0002Í|\x0004»ý
\x001b\x00116aó¬ÂY(IÚÝ®Zã"
HXss[Âaæ´­-Ýµ<AgÞ	ÌÈHuMY2äÙÒB%ú¸¡\x000b®\x001a\x001a\x0001zªÌX¾*ycñ8!W>\x0019@T¥óCtåÐMûáý¶\x0013àÂN\x0000\x001fäånÖ\x0014í´!Õ
.9Ñµ\x0015àÆÆ{(v\x0005x0´î¤²#<®Ê\x00134ÜC_+³÷0MÊÆræ³å±W\x001eÅ\x001bÚów\x0004Ê@qÝ#ÆI\¾3T­ùº\x001b\x001a/&u`Ê:FÒa\x0010²í-w§sm)`2HÐ\x0012Ñ+\x001bíxaèX·m\x00067tå\x0013£áòÚyÂæ¹ LH§\x0002ã³r\x001eoÿeûb`æ9ß\x0018éúQç%Æ·tyRâShÚòwÃùÏÕVÿ\x000b¯güÌ\x0006ÅuÀl5\x0011ð\x001dr\x001b\x0016Ë\x0012ODÅÿñåûýø^_ØWª`Z·èµæ7-Ä·àï\x000b{\x001bÉh"dá²¿lâô¸&%Ã@Aco(·\x001aJDÕß\x0013
ÇP8\x0015\x0018{SèL¥V_XËÞ´Îî\x00195.ÂIgÑ@ÆX\x001fBª\x0004:\x0012V\x0015G¦ç¯Âq!\x0014\x0016l\x0014'©!ÐC(ÐÌ¬ælØ¾±74Ö/UÃ\x0000Äµ£!Ö_9xnòìLØ=²74vSÅäA
Ñe¨¢\x000eàm\x001fÙ\x000b\x001bÛí\x0012ò×(Ë>­ÙL¼A¶çÇW¦â¸0\x00157cw©RêP°ãô\x0015íö½¡±v©)2øÊ­\x0018	¹NéÓE+Uq\¨[#\x001f|FWê4èÜ\x000bc÷½>]G¤*V%"0J8ixÝÌ°lkÞ7 ÞØx\x001fõ\x000ch\x001bHOInúD¼W:\x0013Âé>ZêPMm®\x0002M:¢J«º[öéBR\x0007¢*î\x0006ÀNl¡ä®óºk9ÝHmm4{°=@¦Å\x000c×Û}ºÔß(_Òà)ñ,î[Í$9ªªu\x001bùÓ)®þÏ?üøò?¼ùíËÇ?ÿðý·¯\x0015_§É¿ÒDØãdqi\x0012ö?xÙÇ
!ÍFùk
¯a&5AÈ\x0005¥¯Ô\x00140ä]p}\x0003cp­&\x0007=µB$r\x0002¸Á¸­odôé£Á°½]6Z³iÌü\x001b±Ì5¶\x000e	çSU[¡mbï¯§
7úmk|­\x0012k¡9#P§Uçm}Cc­	Îdf{Ò´³¶
2oÔò6\x0011v¹¢4±\x0013jªar·\x001b{ÁZÞskíèERjÒ9vâíÛ#c£õD\x001b=¹×Üº$Û·ÿÂæ\x0000Ûá\x0013Ý\x0008U9|bb?Yµß>ÿ7¶°1ê\x000bSÊ!M´¤â\x001emßÿ\x001b\x001b#ìÔ®0&#l»Æ\x001c»çÿÛèU"4A4´%¬b¤Ö4oÿ\x001b\x001b®£×ç\x001f>e®Ô)f
ûö"+:]GÞ}©L;\x0011ËæK\x0013·Ïÿ¥Ôè\x0008[M»={-×ºO7\x0012s\x0003¾X$ÝÔ»ÎfÄÏñu(?Ý\x001cL\x000e(%\x000fB\x0017.ÉLÓ@\x0002ÝIN\x001bF\x0010dK\x0012\x000e÷)±
ç\x001d\x000cëÈ\x0001¬Û\x0011\x001b\x001bO V\x00051á\x0010°£YL\x0012Ó3Ëµi{§-t¿SÀ.W\x0011¡¦Õè\x0014DjÙÜEãØuùöåÍwo~ûîÇOïåÿùßÞ¿¼\x001dN=õ¦b±<=SÍS!H*Fc,5ü{\x0018½såíg]\x0018ÙÆÉIÚÎ6JEµR0þqÚÜ<ÅlÞÈ\x00106)-Ø(6\x0015ÍâSOf²Tùw.µÎåÐÞÐ\x001e\x0017mM¦-ÚóªYPV\x001dvNÌ

A6($XuT\x0018ÃÁ\x0005y­²ï\x001b:âªYòZu¥UsãÌµêÅhÞÐ8µeìx¶&f9ö[P¼5Û\x001cÆ
qÕ~Øãëð^¯[½\x001eÖÐýËÚç\x0005>~-gö\x0015ómòôðPÏãî\x000c]:mlÖ}ñ®×¿·º§¹ÜéîZù\x0007ì¢O%¦:M\v2ÚÕç¹ áòZ,h)t&gñûxNÄtf¼\x0013²ÇEwRKÆ\x001c´òÜOón;{\x0003\x0007\²Å!ÀT\x0012u¤È'£Ð2@«»s!G^2Î\x0010«¯\x0019i§Ýpq«fvC'\t~\x000bk®\D
ÊwÎkniÍÕ×¹3.Ú\x000f¯U\x0017=%cÍ2ç»
>.àKvÐ\x0002QtØ\x0001Û´l0íFsãW\x001fê®¸æ3ÙT"o\x0016èi;¼ÝË¤]Øy´®S<Øö\x001b\x0013ä=ÝùÞÀx\x000bvå¢=\x0003Ï\x001d+W:¿¯íÝÐt\x000bË[ð5ì Õ¸\x0016=\x0001_Ä\x0014'd¼,6¿W&\x0019\x000cËÉ÷ëß§óÉ;í\x0003¢¬\x0014\x0004Íå\x0019åöÛüÚ
çNN°EìÌ\x0003\x0018ÚwÏþDç8\x001d<L°\x0019í"Í
U:³Ä[|ë8\x001d<\x0014Â\x0016+LÃÉJ¢iÝÓ\x001cxj\x001d³+yÔ
\x0007ÄRÕM+°\x0013ë÷ºN«·\x0012ÒÜØ\x0001±
=üÑ±"«¶:n°·¡ÁývñH¨AÅV´ÆÍÛr\x0010'çÓìÒ\x000eù®æÉËzG\x0007ÿÏ\x000f\x001f_k&¸Ì~o}^×¿ÃiL3¾°JYyñöPÊf\x0010qmVð~v+ÐÀÿ\x001cª\x001bLÓ¾kB¯
\x0005\x0017²Gd\x000b48E§Hhp\\x000e\x001dÇ¸¥Ì¸¡á\x0016\x001f¡3³q8¦õ\x0013è¼óSÛôáDÛþÓ|÷áÝ·?¼ºa#²a:d->\x001dzÊgoFñC\x001fÄüÅRRFòõ,­4\x0004²}ÍÀ`VÑTÑèÇ¬É¡â\x0018x\x001e}'®\x000fo0m£\x0004q@
­[j\x0013å¼BkfÌ«ÍîÐÙ tÅ\x0006[õ«\x0004=\x0011òÆÞæ×wìÂ\x0006\x0006×â\x0013*Ý+sf¡-áq\x0001\x001f}¸\x0016÷à\x0016	Æ4##ÿgbµh\x001fÃ¥¯qX¹5¸rS°ÉiØÆ\x0014æ*¡8n\x0012Q\x001dÜá|Hö[jà,«ÉLÈ\x0017B\x001bµa}Ë:xÀY¸XKPù"±Z®}öÔ¶\x001bSW]\x0019b/pdU	,è82KO°c¢Â\x0018k'Æ:}ÐÓ\x0017¡ÿ\x0003^hb¿ñóÊm\x001fû:\x001cs\x0007v:\x001c5hd®4\x000fð6#ÈdÂ±ôäÏª\x0013vc\x0003\x0005r¶Ôld¼\x001bS_
{âó¹ëÜN¢ÃØ¨uFRÑ$ð3ûp#S\x0015§®)¹!Ë¿À,_SV6Ú'ldmO¢x¦Í©:\x0019-FK¹½¡eÔCFp¹ü=;ÓÕfü°cãø¡öß@mÏÄJ²p*°(«x+H®Dü78\x0012ñ×
Í6äß2Sq*mBÐoB¨íÀ9Ù}2J¹Ì\x000bÌTz3ß\x0004Q\x00178\x0010¬&mC*\x0004\x001eñ jÄÆ³ç!WõÞ\x000b<Ì+-Ï~\x0004ð×Ê'ðÖ°ïWÂß\x001b\x001c%!®öÿ{Ï%Ò&lË2¸)´@Û×Ã!×?\x000cle\x0006Ê\uH«>6`³Q\x0010èà¤ \x0010=ièh\x001cqåybùL©
ò\x00050,úq\x0010\x000béKØ7f$"Dµ|\x0012»äkX98.pR1á-,\\x0004Ð2_®,ê®S\x0011Ð©\x000c\x0002V;HdUMµt!ÜÃó\x0019p\'Ó@\x0017ÉªÖ3~O%>VÞh8VµÊ\x000e\x001e
\x0007|>m(2S¶¥¶\x0017.nâã\x000eîð$J \x000f\x000f7myæ\x001ewßçÔ7$ÿ\x00176ü\x0007æá9%Å ]É¦<®78\x0007C¤\x0013V¢\x0019[\x001e+ìÊ÷l\x0013¼+Mù\x00054å>gT\x0013[Àdüyú|®M}P¾ò\x0001¼Õrú\x0008¡\x000bêGv·YÂ\x001eKêóo'§"¡SáUÁ\x0017V®bÒ¸çb\x0011.;5Þ»tz)\x0012¾\x0014\x001eiç«Ê$2åtdÆ C\x001b÷Í?{TU\x0011Ï\x001c\x0016n\x001a±a[í·±·³ùÂ.(ªâ*xzqvù¬Øéû>y²å	m¹øÎØ4î´úSés²7$ºZÙ\x001fv\ÿ0\x0016nê(ãéG¢\x0008¬õÜÃ ÓngÜm§$\x0003àQ(=+ªP9L?eWm8#ß¼\x0015\x0005çÄIðHy \x0008Ü7Ò¼aÖèàÈ¬a\x0003÷ê!¬À=\x001f\x0018º¦ñaå\x0005W®w\x0013¤­úBø¼8»VÔ)+cû\x0005z\x0013Î:¬Ò8ÈáÝø>gì²Ãe3\x0004ßÁ\x000bíyÅf\x0016ÍM²+Ó+\x0011[Â°¬rJ\x00178Ê)©ó.)Ì¢+\x0004Þ\x0007ãâçy)\x001e8Èó\x0000$YÎ¦ÑdÞ^\x000bÇ³£ò];÷e:þü#ÇW\x0005#¨+Ì¸0E.aÓ\x000fÑ90<Õyÿõ»×¨¤ö\x0010_/9G~¸½Õ`S¿Ú­¾´²`H[ÒTóÍûÝÔoi¸\x0005´\x0006b\x0006WyîÖØr2\x001bb÷í[¥VlMó¾´¢íÀ¦Æ µüA`#ÄÛ ÑVh^
\x001e\x0015\x0015ÅÞiÜÖÐ¢à¶CFK¡Ú\x000e0Ãç\x0003ÂKlHÄ¸ÝVCqa£¡ÐL\x001dÌh£ÚDÚ2éÆ.\x001e³QîØ\x0010\x001d\x0008\x001c©­s \x001dó5\x001e_ÛõÅêØ\x0016_¬ªî#¬[ó¸ß\x0012T1xêó\x000b;Éæ\x0006G)4¢"l¡r-³r"´\x000cÕaSô\x000f[3\x0010ÕxeA§ìWÍÓ§lUÕNF?µ°Ñ\x000f"¤Liæ£r¿ísH\x001drHâêã+®mÀùíBÐ;\x000eÚbË¬°îXy²ÖNüµå¥]8-;à²­Æß <DIby¿U\x0010¬¥a\x000e÷\x0012Õ9\x000f¡@ \x001dõMb\x0001
Û·üÊ¼ÕÁ=2oeµ{cåÑ¤V\x001fàq\x0012\x0016©]`z£ ×ÁQAOÉRa¾Vi½ÉÆð\x0007m¬UðJW\x0007Ç\x001clòàªò^Ó<³¤\x001bÕ2\x000e\x0007pý\x0003$\x0004\x000bÄ\x0005Ê1E\x001eYõ<£#ÎIØÖ\x001dBk¥i\x0006÷:(=;\x0017OUí[t;U\x000f¥à\x0016§ÝÃ¥6\x0006àüö¨ÈhP7jä
\x001c³Qeg@SÄA5 \x001bÎL_\x001c$ñð\x001eë\x001f'\x001d éx=Åõëe¬`:=m	¶pMçßV%Ç1¥ÚÀËdi[r*Ã¦d¨ö4\x000c\x0018ñÀþµ¬E\lËæµ
øÂv-N
8ïúÿ%.åÃâ
=\x001a;Ø¬Y57IõÇÂÑÌ`»â}\x0017;ìxâ¬`~WGÖ=:ÖÑS¿¸XÄÎù²äíà$É«V
\x001fÎÂÛ\x0012
s?ÖÞS7Ê
¼2§\x0016\x0002Á1,3!°Ðjízòuí:¹Ááz:ãC\x0012É1¶¯Ö»ñ}.o´ä¯7¨pR$¨¹¢f¹ÏÙ«,c÷Nø>\x0011~äØ\x0016ò\x000f§x¬ËÞn¥Þ/;æÈLpÞåçÈÀh¦_£¦Ð)ÏåB¶ó<¤H¶\x0013Õï\x001cÑ8\ÉÓ¹é¾qØ\x001dEÝÑÂ\x001dì¶,Ó4Ie²½-w"(\x000bÏÀ\x0007.C\x0008öÙø­ã/\x000c\\x0003ÿ\x000f°~%ï\x0001-­\h0@L\x0013\x001b\x001c.'f!à\x001aðßýêåË£¿ª	Ýî\x0000\x0011·\x0019c]êÊÐ]xdByë:üBa5à[M\x000c:3Uâ}NYâ·çí\x0001©$àºÔwk<®iÊsxÅ1íÑ»û\x000eï®Ç7Pàë¹	µ±Ñì1OýQ|äSq4\x000b¶!\x000c-æ\x001e\x0019þ¼¥x²ËÛ¥ûÿ5Ú§3ZËF¿f39-\x0014\x0013\x0007æhäolÔ1HPR©S>K\x001c Î}v½7ùo ß\x0018¨Ò¶Á7Èa|ãÞN\x0011§+f®3tø\x0006Og4}VÚNº\x0003ÁN!|\x001f.K+µãx_ð\x000c0\x0018ÆW^¿-\E(¾PPNgHðñ\x000c×\x0007û'¢¡QfrÔ\§¶IùpÇ\x0014ÿ[Üÿ%P¯ÍÇÜq2á{sÜ÷EñÌMl\x000eÀ«t\x0004máÒp]P5åÃ\x0003 ðHæ\x001bJ-¨£åÇ)±;\x0007sÊ\x0007\x000b­ø`¡³rl@\x0002Û?µáãí\x001cÞ\x0017ÿ\x0003ÃCc·~Æç\x000c}q¹7+Ärþ÷púu\x001a\x001b\x001eÔêªsLW/D\;\x0007ü\x001fñrUì*ðNàË¦å§ëù]¨ô\x0006þ\x0000?\x00184\x000e^N\x000fL©ÓöôVxAùpÆÿ\x0000ø8º¼±Þ\x0015Q§Ëå:üÏð\x0006xC­(Zë¡"½¶éýjõ.Aùþÿ=únä[Å/'ùÖ<Õ^µ~F÷8ôÃOßWï>~óZmÃÂ\x0003\x001bÌÃÁ/Æ\x0010ç\x0006²róÙ/Þê\x0019{ali\x001bvk\x0013l^Ó_\x001d¡XÑb}êÊY,(åëÄyh3LêcúÎn${\x0015½ýáFWu\x000f\x001cÍÓ3©/\x001b=Ñq«XVsIý&roè\x001e"÷Çá°¨ÍSÐÅ§á7µ=ÛÔ2^vlÞþp£Ç&x1\x0017e2ñnÓÞ\x0016ÓÞzá÷èÕcósXnn6<­å"\x0019#\x001b»I°t¦¢·?<è5e  ÎúÎãÜ¢¸Ö¤Rfôò5ô¼ÿªí\x000fcÌ@çrnó\ÄiAj<?1;ÙÐy\x0008õà­nÊ}$ÁM)Ê">ÚÙ³Qª_xhzû5É\x0012ÊfÈ MÍ\x0003o>üïÿù¿þÃ7?¼Úè±5\x0012S\x0018ªòÇá³÷A\x0012MMü»\x0014<Zç\x000cLøÝ<gà\x001dIQÚÌÜGrã¦ù&¿=¾¡a.Æ)A\x0006LÔÐ\x001a$À.\x001bÞç\x001e­3\x000c\x00174Î0\x00187Ò:\x0016H\x0014@ÙxÕ¹ßµ\x00134\\x0005\x0015J\x0019$þ)ÒF\x00077O©.\x0000uÆ\x0011F¾Æ)^Ç¤J6³us=\9J/h\x001cù\x0001Ôò$ÿ$\x0017vFÖ(i¥r¼qQ\8< e^´¹é]mÌl+Eé\x0005]\x0018ÚÁ]Ò¾MK«æPKÓXY"/h\x001cb\x000c\x0001\x0005#!WíYyÑ¼\x001fb¼°iÑÇA±£sÞÜ/\x0001\x001d\x00138ËÝÜÏ1ÞØx\x001dµ\x0005f\x0002\x0013sêÁæ±@Õ}ßt&Øa(#f²\x000fzõþûW\x001añvòºQµ&ÝÞëµë@ªöè¿´\x00147Çü=\x000cS²wôÆD\x001eD!ÁAé¹[ÜÚ-óL-\x000fø4d
OXvÞÒ3ÜÐ\x0017
$éU[\x0019©ãÁql\x0011m#ÝTÉíd"½\x000eW<\x0015-.o1æõÁLûÑÎÿ&Óo'\x000b)N0î¨\x0011\x0004×eÑ¡÷\x0016òF\x001d\x0019K\x0002ö
M\x0012\x001fHW ÷Ë7tæUç¡ñPå(ÚOºïÑ6c³©×ÚÉDY"*(c\x0018KÉ[	946¯MÝÃN\x0016Òk\0^gY´cXïçýèM\x001aº¾,dïäá
!j"\x001f¦3Û´iW\x000bycÓe,teÔ§§.!\x001e¯¶Iê®C
74ÝÆ\x0002Njß\x0012:}\xÏ¸§¼¡éÊT\x0008=ÚªùÊð4KìZâë´÷
\x0007[9Ä=@Çù`çyG\x001aöéøY<~Î¥\x0019oVFñ¡ðì,¤kËùíð¨ø4XÙªÆÉ\ÊÜ»
°b[²Ø*\x0003ònòTb0\8ÑFî\x0006~8&v&úz\x001dØ"N¯À¬¯:¥ÜW~0ÛÌv"Â0#\x0008d¶	l¶»gkW±\x001b\x001cO¡òÆÀ¯¬0&\x001e\x0017\x001fÃ\x0014ûç<ì¹=-5?rQ¼¹\x000c\x0011ªJòq&½ºÓ;Øs¹\x000fö-\x0014&&\x0014o"ÃÚYÐÝiË\x001dl¹\ã\x0013>Qî¦ap3u!õV¡Ó£¨X6ùs\x0005w=I\x0017ÕÔË\x000b»~Ç\x001dü0áÝÏBâ\x00121:n\x0002¿Ôè\x000efÅÁ{\x0019­\x0012'¢\x0013WéQsµráB|Ã\â
ÿáç<ÄÏºÛÎ%Þàæ±Êó\x000fÛ¢í\x0002\x000cÎOM¡oËáÙtðlÊ¶>k,ÜW&þÉT³¥ëC\x001fL¢wS\x001c%s1³¹=ûáZÁÎ\x001eNgñ~ú4rk
nÚ\x0004×8-'dµg£î§Åû\x0019"'rò:ÅÅà©¯ütA-^ÐØøð\x001eìLa¢×¾?Æ=¡yºîgÀ\x001c¹Øj
÷år;ií=Ç»¾÷S7\x0018	±Ì»É:½ùÎâå¬ã[6µÓõñ¾ó\x001cî¦ÍlÇ\x001f8\x0006&ñöª\x0000Mà®UuË¦^y¹³( n8ÆRrH\x0014Q	[w\x001eþ¦"}¹øPþ¥èå^\x0018=C´¹µìÄùÉÍï*ÇI´1rò
¸,f
'¶¢ï¥¾}-ýr\x0005ÒèÈ ÌÄD$û:ÅÎÿ\x0000ò\x000bÖFH.Üc\x000fëå«O?}÷Ó+¥a­¼ÿÔ-\x001a«{Ò°^§¬G\x001f«uª5ýÅS\x000cÑ\x0014µÏsaKÕ-ü\x001d]èÀ3|~ë\Á\x001b­\x001c¨D\x0001¬éùª\x0003¶5í2a{KÄJÖf\x001a¬\x0010ð6fl7ë\x0006ÇXOk°pÚÚÚ\x0015Ægä^è\x0010³ëÝ\x0007p*§Å÷Qî\x000bÜhý\x0018Ü'qW©=,t"u°ûÁ¸©D´üVat\x0013l\x0008ä)öFÆÄ7]ãe\x0008H\x000eà\x001b9UÞÿZ·a\x0012Íap\x001fyÍ÷¢brÿ\x000e\x0012Éæ¿GÂD6pÎ/µé»agsuÒô¼ùBay/l¬É:[>2L¹råÀ$¦Î³w<,¾áìÃ\x0005©´jQíoóZ½}\x0000½°=Ò\x000fC\x001f.;ò´NbÍ4Yv#Mö{uC#û°59Â&ÏTI>G±ÛäêiK2nI\x0008PòOiy:*OÍï:ò¤	¬Å[¾°aâÖ{\x0007"SÚ7kXÏ+È{ÒëK\x000cB\x0007§\x000c\x000bÊâS\x0006!so¡WAá­Í¼ÁÑfz]\x0015p1öÖÒ®p[ªËý­¯-×?À)´@H*ÔÄá3\x0013\x0004©ó¾P:¸£c\x000fÉ¦T<'ò\x0014Ëe.½ü\x0000÷\x0008^±^ï7\x001eî\x000f\x000f\x0000:ÓÛmÖ\x000b<£zA\x0002Y,\x0001Ü\x0016aJ\x000eüAM"ÖÁò\x000b¼þ\x001dQ¾
 [Ò\x0006='º6ñ¡Sït=l\x0007þ\x0004¯\\x001bðAS°¬GªD0\x0008nû¼ðÿ¡îÝvô<$ÁW!êzóáRRfP\x0011ª\x001a}±7\x0014Ee5ÅT%Éé\x0005\x001aè×è×ë'\x0019÷ï`\x0016\x0011\x001f%ÿ )`1*vYÆ\x001f_\x001c<ÜÍÍ$¤¸\x0002u\x001e\x001dµ¦pa\x001dTB\Ëe-úvlòX\x0003\x000fÜQ\x0001X®ÜäyàÍ\x0011®6hÀ
ª2 à\x001c+ ²6®·]K*\µ\x0001ÏZe¡@© ùn uBgN}ØÜrÌ>¦\x001d\x001c'%f4.ê|\x0011\x0010|HMúØf|!Ë²C%B\x001d\x001c\ªhÆ+ï Z÷wU°:xÍ\x00140Y<µ\­Ôyiå@fò\x0014{Ýs~,7ôö\x000f\x0007ºê_@=ÂfÊµÑp9nthç&¬
\x001d°\x0004Ýáj±½äÿ¼\ä\x0001µYSÍ²i\x001dÝlZP\x0013ÂE¦D>"r«Ü\x001c=öF\x000cë.öû3ºC©¶VzÔZíù\x001ff¦ï~NttêqÊÑa(Ï'!6£ÇÒðä±x^Ï5#V¼ÿuj¨ëÕFO¹\x001b\x0017MÏòYyµ£\x0007P^\x0015tÛ\x0016É®ä\x0015KèÑ»µ
\x00177Fû\x0013\x001dÒN¥ì­Á'xd
A(íI&[fÊ&\x001c	³	²p;É@¶#Ö³A«²¦®ØùÇÙø1\x001aFüGbn×B\x001e\x001eÞöÐKîµ¹}ÜxèO\x001e´»\x0000Nwy%3ä\x00192î)]4ã¿ãñLq\x000cã\x0017Nº¾ìe\x0017ø:þ»Ï\x001e¿ \Ì¿âãü\x001b\x0003ToW3ø\x000e*þ\x0016Í,2:G@3øz\x0014èé¿!g()MVþ\x0013rAlS4ÿÏðê³§HîéË\x0010Fk\x0012m5ç2Íã61ñë£ÛlÉfºøÌºÍà3k]\x0011~<âùôÏÄÛ,º²Ý+\x0013Eÿ¸X¢\x001f<qB<gu³¦C(Q^]bù~qÉ\x0019¿þ\x0005ú/ô\x000b,(\x001eè!Wè#ÛÀ? ÇÖ§(ëÚðñ ë
"cù¯8É"Ïqº\x0001ä­\x0019¶?°^Fí\x000fÀ2ºHO|2·±}©Éãü\x0004÷ð	J<yúj{ÈåAÛS\x0011ð\x0007ÍÛ\x001fÚ<Î?ðWø\x0003òxÈ\x0010>È"²ôYUG¥Nãö\x0007¦Fó\x000f\x0018*ªzÄË\x001f(îVã@¢ã\x000fL­\x0012ç\x001fø\x001bül\x0015^ÕZ\x0002ë\x001crÉSòÚ¥®* 0S«Çù\x0007\x001eð\x001bdðäl(±¢nÚ·Ù?òÔqþ)²õ\x001cÔ?x\x0015¥\x0018}Ö»å$Ê¼X¦ò/°Le#Ó\x0006TVQ0dâmcv\x0014#\x0016Óã,Yßí\x000f¼?à\x0002\x0018ÄÈ2õhócc°<CeéââÁ7\x0019\\x001eÿíþév\x000ch¦tºSuH\x0014ù¨Ä«CKK}ý\x0012ãG©\x001béÏZì\x0002"q\x000b\x000f#wõ5e¶¯íÍ\x0012WÐè\x001bQ
\x0019ÝèËlEJ\x0019,:òþ¼CûOÚ±­éÏ¶åÅg/?ÙG+GÙ\x0000'wt,mÆ\x0006\x000f®É\x0019Íºg~²vÛkô '
x%²\x001f|EÜÒ\x001eiGÎ<h\x000bóQ
Å\x00102èÁ
Å®}wh$\x0012kÍ\x000c\x001dKì`hÃU\x0002çºíÛBGÑOvÉz\x0011:`m«H#\x0019¢ÄÀQNÅ\x0010à@8êqï_|ýôñáýûû\x001b1~åH`[¾\x0018NÅü`Õõè¬\x0001i£ñó{:ÅÆ2\x001cOÞbC¶=8L[KDT*eÅlõt\x0015Ð\x0005ógÈ\x000e
ÂÖÁ%Ô\x0014K\x0005+Q6=»êçÕ¨\x0013Ú¸Ú\x0016QD-\x0014¥WM]!Å¡÷ù)ð¡õ4\x000eB\x000b[{ÆîÏ¾HwlLË\x0004Ð°*\x000e}êò0eû×Ð\x0015ÿ\x0016¦2\x001bvEl\x000fBÅÖ*\x0003ÎÒtS\x0013Jn\x000b/°A©)È\x0013\x001dºg­<x¾\x000byLÈt÷ÅB§¸cçajG0¬ÀD,\x000cY\x001bøÅB±\x0019\x0017¯ ¡f%BÉ«;òÇ,VþÅB± \x0004\x0013ZØØ*\x0004
\x0018¼ë³-Ô-;8ÖµY9\x0015\x0007¬<ù)Ï.³ÂN\x0012Õú5U¯#UO[GKe³;>?§3¼}j'¥]­q,\<]\x001bö¬
¿a\x0017ÆÌÖesªü·YaÆNû2-îæ±âu|ó¸uÚýöþ\x001f\x000fïÞ?Þ¬¦\x001dnâµ ³¿\x0019£9ë\x0012ª=Ð¼ò`\x000f¢\Æâ°:qBð¯Ét¢&i-ò\x001c¹¥æÂM5\x0005ç°¨]4+D©¦äØ¶Ã4ì4ï ?¬\x0012qÀ\x0000w¥R+ûe*³¿ÝWónÞ Ñõ;\x0003\x0003C3Ïl{«ª}\x0004íZvÉÎ<ÍmÉC[Ï4H+¥¡½¡\x0004VNðfKø_Ìuèê,G\x0003¨>ÈäFì© ÒÝ½]v\x000ef7pôG$Ì©\x000cðDeíDfZPj#\x0017+Eÿ
(=\x001cýPL\x001d¶diS>7\x0011oØ\x0019­ç½Å*\<M9çkãæZ¾P×îØXë+ÿ\x000c\x0011z#\x0002UÌ%xæIÙ¼F\x0016qx\x0003wì[È\x000eJ·Å
ß²Û:ÏU§
\x0018«NÉfd(TuÕÆÀÆp?¤®Otõ%\x001d~É\x0010Á<°\x0019\x0018!ÛÞ\x0010\x0012M\x000bÈ\/ íÃ£\x001e¢:Uº­L\x001eDÑBî\x0014EdÓÁé\x0016Üy\x0013*6¿]e°sÄ>)y~soØ\x000e'¥%ÖóF,qRB\x000f\x000füÂ\x000c aûbøcV\x0000\x001fhÈv\ß!·,¦¯\x0017_Sÿ\x0001Npó\x0012'¼pSÖ Ii%þ¹\x0006·cÃ1+\x001bí$\x000b÷#gk\x0018M+EXxM6ðÝGQÎ>¸\x001eF\x0001:HÈ\x0019ÑMF.f< \x001fD%°EÍ\x000fq¶óÀ[Ð\x0014\x0016¾.\x001d\x001cé*b`\x0003©+\x001eíMv¥Õ²}qa	ÙÀ#\x0014&}Òë\x0006¾gJ¼ñm°Ã\x0006j5¸psÛÀa­¤\x0008\x0007¡\x001aé`xm=KýViþjÔ\x001eG-Ï\\x0008Qj¬ô,Ã\x0007Ý®ã8+ýnÐHäL5a¡ª*S\x000e¡¹@.£nwZ\¸:tl$ßÈ:\x0005sõ(Ì­Ú\x0000å\x0005V\x0019
ên¯F\x001a\x0017GxÂ8â"\x000eýT\x000c«ØWóp¾³\x001c!hËWòµËÜH\x0016jkL\x000bS¤\x000e\x000e¦H>#ãA½2\x0005@J\x0002`cÐÍ.ÂÕÈ\x0003¼¤Ó°^ã\x00082¬·n Äî®î÷Cqd\x0017£ØèOi\x0007·hSw\x0014¼\x0014TõE»~ÑÀS²-y©Ä®fãÅ¢ÿ\x0000àæL\x0015vz½á:ÝÐ\x001fÐÕÚó,©¾¤º¯ ®ª~\x0005ègÃØy\x0010\x001bÇº,lù\x001ar	H\x0000±\x0016J`y\x001b\x0012w\x001c¦¦`VÂÅQU\x0002zÔY
°\x001døÛuèÃ,\x001d<^LI8%Å¡<£ÖE¹²;t¦Ð>æBs¶W¢#\x0002ÂkN\x001bóüøvó»¥Òf-
\x001b´|$Ü¬èm§I
Z(i\x0004wX\x0017º\x000e:ùO\x0010ákÚ\x000eÇ¸«­\x0001[Wíú0´èÐ\x001cô\x0010\x0016OeQYñ\x0013/\x001e[³°ýêè\x0011ó/¥5Ðþ8Á¦@ëpÖN^«³\x0006Ñ1/PG\x000fÍþì#sr²£ö¹ÍÜÿ[âU0¦*úþ\x001d ûBf7Ê£¢Ñ\x0007îßIÑo\x001fuªNøPÔÌe©°h<\x001f]¹° }¶i©8yâCqÒVÇ@\x0013öBübGøÜ\x0017üÊve_óDõÐ¬\x0003viJO
yØ°i§rÈ*P¿½xñç7w7±\x0007nµ¨1àTÞ^ÈR³n£\x000eÊú;¹Üá6ÚÏÐ7Iÿ2j@iQ\x000b~\x0019\x0015E'\x0017]Õ@wdª: ÷\x0014õ© Å£ÁP£µ*­j ;4J@i×ÂY+!¡UGp\«W5U\x0005t\x0007Æ
hÍhÞ¼5ÈyÛ¤8ùB¤C'hwê=vlTe¦ý\x0000Ýä\x0014\x0016MÏ\x001dºüÖdÄ\x0018\x0006WoËlßë3®ä\x0006zG:ÓÀ\x0010ÕÌeáº-]âÊÜëÙ®+lÔ\x0008SåHØ¼ö¸IV×^»Q®>¤E%/ySG\!4Õ\x0003ñTóóYÓÝ¯¶³æ¿ýðãÝû÷]Jé\x000fr²½úx£âj¨\x0008¦¸S¢R7ç®.2Ú¬óÜµÕ(:\x001dÇ¯"ó÷/C­^«Ü` Pì ÝV3p²¾Ú\x0003;tAèz~pªrÊµ6hf\\x0004ÓlSä³C\x0003
 ûJ­ú\x0015
}?ÒiÒ\x000fèÛkÆí¥­E \x0010]d·¡ß`\x0013S&Ä¬\x0019\x0006;¶åaa[1ZGtÜ<Ù¥KL[wÇ­;\x0005¦ªÉ\x0012wbÑ!Ê¡:ÌIWn\x000e÷\x001dÛ#vnp`3m<\x001a¶5	ú\x0010[\x001e\x000b;vàqÙ
£YR4Üh-QKtæWÃ\x001dq\x0005f\x0014XÑeÅOYqXíî3m;6\\x001e;_æX'dg´aØ8Mðjº£ç=	:Ç¹\x000e«;s\x000b¯i¯ù9¦ßÃgOH\x000c¨ò§¨2eK`y\x0013½Ñ\x000fßsI«óÙüfA«ûç7ïî_üñîã[qëb`\x0002inÛo	\x0005)%ªøzxöÃ¾®\x001cýæFªlÆÀ2J\x0014r6ôP=&\x0014öLÐT\ëvd8|BÎ(å«\x000cc"×ÅÀñ»Ëíð\x001bb6hX²Íu\x0007Èd[qè\x000e\ªwÖõß\x0015tBh{ª\x0016Èç£'14å¶\§ºOWß\\x00109!·.n²ÖL\x00173µ);Í­S\x001btEh\x0010¦PhCDÈÐ~-\x0014·aãÝ§%Ã³û°4Ù\x0018üM\x000864,ï¾\x001d\x001b\x0016_P:]\x0006ì9Jµãõ\x0004Ý\x0015×®\x0016\x001fÞ|ê]\x0005\x001cÉè
\x000bÛJ(ÉÐ½o¾ùvl3Òe³vl
\x001dÍHå\x0019É-¸hõÚ°Ãç{nÚ°áæ\x000bjö\x0006Ø*«C_-Ôdº{\x000bÜÕ¶ÁïûjãXÜ8Ùpn+ÃáÕ\x0017]äÅ\x001dºÏÕâv¸¸KEy[%RT¾\x0008xKúVX4¾mÐ°\x0002£6C\x00012÷ìÈbà\x0002ÝÙDW\x000bÐá\x0002Ì$p->\x0013^£\x001b¶¤o]3obÇ\x0005\x0018}&\x0012\x0007iú RôÝ*3\x0019oÇE¢GÅ»&SëkHl§îT_NS
s[mÇ¶Ú¤Îá¸
V¯ä\x0000\x001c¦»çkýÕéêát\x00046Õâ1\x0015Ë°\x0000]èºî\x0017Ø\x0001¯_	¾b&lÌ·©¢\x000eïÉ.T\x001c®Iðø)=^ÀmhÔ:»ÚçªÁ
gIÔªA\x0004l&è2áq·n9õ¾CãT]hîòÙÌÔ©ãB_}É_2¢\x001cE\x000e´¸\x0019f¤yH^}È\x001f2EÌu\x0005U\x001b hO¢s2!=\x0003suYºÍä,9{$Þ!\x001dÎ\x0010X>TÂþ\x001cººÍ,ÝfÊnÆ;âA&7üö\x001eººÎ,]gë`ù¶&3Ó´;`ªÐ\x001bt\x001bì\x000cQË´pRÔ¹&»è
ÝW(\x0016üÒðuÑÙz ß!zÁ¨JÑ-]jÃQ(è\x0017«ÐWð¼\x001eäQô»w\x001f^üùñÕ÷·y
©Ñ\x0003	8Éÿè5rÉb¹)É±kß%µüïO\x001b×±#È«»!\x0018ª&ùyØ¦(\x001fS£­ë¤u\x001dÛv¼ÇEÕÿ»A:%ÐÍ*OøFcÖ\x001b4µ½&ð+pñYÉü\x0005[4ç¬7äóAöG±:¶òÎ.ñâ~³îÐ¨SãJE?R5øM\x0004m3'\x0005B¾ÈYoØø\x0019\x0013Jµ\x0019}Å¡IuÐÞZ\x000b©Ë
\x001b´äE.Ç\x001a/:U\x001arjÝ»g\x000eß QU+\x001b.þtóí£\x001e ·Q_-\x0011$9y·A«ú@£\x0006`\x000fYÚ\x0011\x0017\x0012Ô\x001b6.X1©@däXÍ5\x0018\x0017\x0001ú\x0006
Ôj\x0000\x0004BÎªB
	É9s¤Ø³\ä\x000e}ÕN;þPÖÐ!/ÿÓÌiµ.æ:wèw8xlQÍ¿&OÃ¾ì~òWèd:]\x000cçÝªb±ý§À¬s®14ÞÆ|?\x001d§ {KNÄÉjIÑ\x000eóºbùÕ¼[é\x0008¹Ý\x0013;¼ã\x0017l"Çó./ÿ¹\x001bÂB7Äá5ôþÅWOoîî^ÝªðcëP[õáÌ\x0006ÚNoÄRóîù³ë¶º}eËTgv\x0016\x0003¶â\x000b?[Up&#´jðLHÛ ©è±#¶øÌ!OoaFèÆ\x001d	5\x001b4\x0016%ôr°.ÖJ\x001ej¶]\x001do&¼lÈX ·uïë
õ½\x00057¼\x0018\x0004zi5´C\x000f½¶8Õ©s]µ½ÎfÛùÿyåÂ;·áû°îâÝ3"ãÙW.¨Õ&Áºº,ï¸h3$·S.4\x0017xó\x0005ËMcúA6C;tåÉ\x0000s¤¢¯\x00040zka¹À&¡DnQÅ±APí.\x001eöE]pÇÆ(7\x001f,ªÎ+\uÕÂhí¢±c#çCyUW5µÔ\x0007ÒÂk=)ËðhÇö¼c ÓohØÂsâºÈÄÕÁ\x000c¦<áZdq;P]08V«kr{Ã\Ü\x001b?<~|ºÿø¿oVEJü¶m\x0001\x001eÆ°h,ýjèI*¹=VL>Ûõ÷xÎì©y\x0007¿óÛ³i^«fº6Ô<\x0003tà\x000eÞ\x0019Z¢ªåµa¦k#àcOG\x001dy©ÆÈÔ'Uû_Þ\x001bfº7*´VúÀF\x001dã¸8Ö÷î Ï\x0002\x000e,a+ëÅ4\x0010\^\x001cfº8~!ô|séæÐuÀ¹Î|yDGü\x001a×cáùî0ÓÝ¡È)Ð +×\x0007ºZjþÑóÝa¦»#¤
Bí+\x0012ï#:\x000e,dí-Õ\x001füo\x0016úÓ_?©\x0012ûÛ6Öó
© /Úa*½¯æ¹ÆõÄ\x001f\x0016íÔ¾¥äáÅYB`eQÏr\x0004>Pêml\x000c¥EG`ÇÆ@Õ60Y\x001b©÷Äö¨]oK])K4ì=6!¡û¤!ovÃhzWÆ\x0005v\x0002®}¬ûë\x0013uÖÉ
!¾¥««s^\x000cäKÅ*pÓ[å®\x000cÃ|xzÖc%¤ÐÀ±¤FºTÚãDÝAa°%r¶¿\x000cüB@Áõ\x001fRQ£°äD\x0019\x0004-;¿ùÜä-ãìÀÓÁ#\x001cÁ\x0017P
ÑöhN¼iUõ­KËÌES`\x0003/(Ì)«d÷\x001bOº\x0018Ùð½\x0010R¯°+bg\x000b5Õå/aÞ£ÉOÐçT©±Ùïl\x000b.qÔo\x001fß>¼»¨M\x0008\x001aãå¨wÐ^\x0002\x0003\x001a>®Ñ¾ìg?Øm\x0006`S\x001cµ0\x0017\x001d\x0019\x0011±1IÏº*bÎÇJ\x0015i«¾©Ë\Ú
¹´¨«Óï·&ÿ\x0006ÛÌ\x00175¶9´zÉ\þÚ°#ÛUh`-ªW¯,\x00197½Vä
ÐÈÞ³¸î
âº©s¥ÚÊ!IÓb´Ô<v>;²ã¸\x0019¯×\x0013Ü©µ9:vëcÀcÏ\Î­±\x001d\x001c¥Òc»tÏ`¶ì,Ó\x0010ðtý¯ÙU¬C\x0007t\x0015KÚ5
]YöÈ\x0019UM¡ÚÝ«Æs³Ù\x0006\x000eÍf\x0012OG|diJ]~\x0014ËM×ÊÆ³ôÌ\x0006\x000eÒ3\x0002^@½EóÖIªÌ7«MD1Ìíß\x001b8´GÕo\x0003.kÈ]P\x001dS~*Ôf\x001c±héíàØÒ\x001bÕ\x0017á\x0015õZCj§W%Ä¶¡l\-DKENcx§-\x00029×e¯l{{ìÜ·¾Cßz,²ò*åT2\x0016båYQù\x001f½£®Î\x0004\x001aù\x0002ÄÄ«Ôâ!7ûP$um­Ô«Y©8+Ú©\x000eå]y1ÉUaÏ?ç­óëþ¾
\x001bH\x0006Q)Å°TT\x0005ûÖå^aæ¦Ï[Vhfu4t¬X\x001cQ\x0018ªv÷ã\x000fÅÝ°	Ò¡[âGÞF³Yr¨c¿¦\x000eUBeq5ð-Ôþá\x001cy\x000c'Ó]F\x001eíç3Ë3¸Ðý
%n½@·^µ
"ì\x0002Zõ)£M´k¸¹½£»kÑ6Ø\x001d=±þÊ×3zl\x0002»°xèèhñ ÿç	"&\x0015%êº¢\x0010xNJ?ëoà cTÇ\x001c\x000e\x0012¼<}Ôaè½	K.³å\x00181;ã£C³\x0004£ZTDX´TÌq1làë\x0013½ý\x0003`\x0011Î.Aã´¾ÊI\x0010xï××ÇÅ¬'X1)j\x000c|ÞtE.>ÔP	r\x0000q6Q^X\x001dýbbô\x001f~*|üdìÙÑ/6j~pAO(z`b%Ó\x0010X6Û©Ð~{3Íâ2\x001d=ÇÍyÊ5¨\x0016îKú¦j©Ð
tWàÀ9eóôx,S	W»\x000b\x0018yîP\x0017'eÙJp:ÜVçÙ
`\x0012½±
]öúzÅ´8À~ÓsÒÕB\x001b":3°vBê´Ë«¸ËaÜï\x0012_ÎrV½?Õn ó.¯f%à¬hãã+\x0014®¨\x0007*-­\x0018\x001d¯¦%Ò´¨CÍ¹KåD F Ì\x0001Æf/bö\x000fg\x0014-\x0012²KnØ£8]W´T
ô\x000blh{É¦s¶_A\x001dL­ë\x001aMJ­À®>gÏù\x000bÁõ\x0008Y´¾\x001cÇ\x000b·¾È\x0002C})9÷¹Ê\x0017Câ}ZÆn«?¢ÿ6ö×\x0004\x001fU>\x0008\x00154e·\x000e¥ÄÚNI	û¯þ>	èo¨\x001f
\x0012­|wçJÉr[ÝÞJ\x0013ãàx,\x0001ã æ)\x000fJ²§C¯SUwêø\x0013åàÄÿ\x000eðe?UÀH\x0015û}\x001a\x0013Ð1uB¶ùpÿ\x0001æÇX¬×)³¼Ðø+7ÈWÙÆÿ÷kü¿#~<vúæËT³Sù\x001e~É\x0017S6!\x0017"vË~õÿß½½¿YÒ¦ZpMÐ-Rä7òGQ¡¸ço!®²ÑÓ!%3Ø²Ñ\x0010\x0002¥°ÍRoK¢ÐÊÉRy6W^ã;v@lD"±\x001b7Ì:Ã3\x001dÑÕ¬I¹cÃ£\x001fâÈ»*vnA(|Efàu'Þ9ëºC'6'ÙC§¤2{Vþ«ÈSÒ\x001e3ÕÇÎm©\x001b·ò3_mxØ¹vsaaÇ.ù)çôxÑþûw÷ÿxzÐÅu£ÆÜ\gN	¤¹éó\x0013È«þKðßÍ>.ºÒçFé\x0018Æ\x001a³ú\x0018\x0014ø9\x001bój"}ØÈûsô\x000c%æ$+¨z\x000e$í\x0017F\x0001êÎX»v7d<\x0019>[\x0008\x0019Ó\x000c\x00120Æ\x0011Ù¯*Ì;4\x001e\x000c\x001a6gNÜÝQ\x0003Ùv­¢:·HoÐx.Ènµ \x0013\x000bÔK£ÈiU`ÞñX(öX\x0016àÌM\x0012Õ\x0017ËÈyÉLÚñPÈ\x0010\x0002)ôà/Pùz\x0017èº,0ïÐx&¤\x000c¢ÓFv1ó\x0011LdEgÍ²À¼C×Ï^\x0008\x000bÄIXàb_}GKÇ{léÏ\x0003ÛP°£7Ç°DzÓÈÕ´ô%=¸UêXÙTõÈ\x0006ìàºúØJ(,\x0013uv¤Ck»=çwõ!meàH¸)3.±«%z-Ë²Í\x0006)VµÊ\x0000é[ùùÌæ+#ÚKBWkÄá\x001aQÕ\x0006¶tÛEÊ\x0004\x0015o_ö?îÐ¨=a¨Ý¡ºHRar¨Ú8`Ûe\x0003äb\x0008\x0012\x000bÓg,IS\x0013Q¯Ô<.;ò6ì@SbPdKÎ:Î8ÕÀ:"ÎvÃ¶ùs|KlüÉª\x001diè$\x0002TÙÁHÞbÅØÂ~ßðc°åàá£jº&'f>	m\ä_X||ñíÝÓÓ­\x0014¼ÔÑÅÄòéWâJ2\x0018øJ\ÛÖÏsë,¤cú\x001c\x0012»n%\x0003!±·ÚkpÁ\x0007V\x000f}¶ÕÂL/ì¹\x0003£cGàÃÈYt6\x0008
¶+ÜKã3ÅÝ[á\x0016í\x001d~ô.ðò§°½ÃÁ¥REâ\x0011<o.qîÔéàÑ!¸A©\x0017§7	Îç¾Iù!-­à\x0017­:
Ü\x0003\x0017ÕÉ)S®~däRï=\x000bY§Ò\x001ff
üü®è\x0004­BÍ/XZÝ¬«Sè/³iñ0-®¨ L¹EU\x000eU.ä\x0019¯ízõ³&ç\x000eqRìY&ÑHÅxÇ2rÙ÷§ÙÕ¤\x0001±S±cÜµ\x0003ïÑxÃ"ðòN¼¨ïvp¬ïJ\x0004W&0Á\x000c
\x0004ò£ÛY½~Ã\x0006õzMÍaRBý\x0002,O9KÚv?é8»tì\x0008¡º+ùnÌ$1u
#wñÖ8;?lÈàü 6çû¢KÌcvQö1Ë\x0013Gß¦;Ïõ×\x000e¡þª¹K45V5õ}Fô\\x0006AèèÌ¶y&ÃÆc÷a£ì¯\x000cÝ?4/*;º}º]@Y\Ç©EW¡«!` \x0012±øM]\x001e\x00043Û¡(éõåJ\x00079Î«\x001bê×[Ç¿ L\x0013T³ÇuÃùÂ´Vb£!úéê~è¤Äf£,ìTJLûÔEþ\x0005e\x0012C=ñ_1>Ä
?0~^ãO®'þ\x001bÄ/<~ËÆ·²ÒÆmÇØdyâ?0~J_xüq\x0018ã\x0006ù·ôÿ\x001d®MÉ7F&|¨äëSÍÛêìJOüÓ®Ôey\x0010Cê¡ñ\x0004ð´T2;-~ùÅ\x001dÿí5þ[<Ô2>\x0001µí\x0003eY´ 8($··¼ L±'þ=â÷Ãcù\x000fM¥6Ûaýï×Ôä¶zâÿ
æGU°>S!õ\x0000mÛµ<ÿa\x001bÿäzâÿ+ßx\x001fyÞ\x0010w\Í¥\x0007µÞÚÅNÒ\x000f×ø?ÀøE\x000f\x001a5Ëx<×ÊÇófuÓ»køwpøËË\x0010\x001ao«§¤T\x001cÜtÎüx
ÿ#^5%áð·§]C/¬Rý>ú§kø'ü\x00180RP
\x001bfzF¼:üT9áÿ\x000e£\x0017xTIÖ.I\x000cZåfáµö½õxÿ\x0008\x001f#ý©îóÁÂiÓÃÚ²·|\Ðs\x001d¨0oO¸ßËÛHuó¾ù(o\x0008æéxbà\x0012o-áàèº`,:_y¥\x0014}\x00016aqi\x00136Å¸2í\x0011pk k¬\x001c\x000býcÁ×¡,¦7¥µÎ¶>\x001b6ØúÈ¡ïA\x0011Mâ\x0017F-èbM\¹Zcù(
ÛBTVUA/¯`Üy"5ìáÆ1Pgç\x0017è\x0006\x001eqà\x00064\x0000\x0014\x001c|}\x001a¸áã®'Î|\x001d\x001cùÎZUåp,\x001e\x0017óT^½.\x001bñb&\x0001upHø¸hëi¡ë3
f

\x000bàÔÜºÀä¹\x0000/g*]Úp\x001e£¥*,áÈgWòRzùn6>éà\x001e²ÇNÛµ
ÜWd\x0003\x000f\rÇY\x0003¿Zå\x001eWyØÔëwðäO;¯\x0006>ôqÖ¾ÊýÜñ±CÇSÁBë`äöì\x0006k\x0007Ê àX÷ÐübÎLwuà|ò´jõÁéa¾º´ø³fÚGÎÐæî¯Ö§µ¢³\x001c_ò£n}*aö}ëÐ\x0001|ß´\x0011\x0016\x001aûd\x0003\x0015¥Ø!ê²7Ý×9ÌOþ\x001d\x001b\x0016:|Â"Ô\x000e'ÄV\x000f¢Å¬XK
\x001bYK\x001aEA_i8àÌe6ðJ²^S¹­eábàÑÒÀA'H,?èGÕOõbè?\x001càJ\x0010#ËoÉ¿\x0003Ü&n±®±Ir¦¹DÒÁ\x0013H´³þÏØ¶\x000f.BÕDä9o'yÍ
7p07H/A§fuòAé<\x000c&\x000eGV7%ºø)à÷8ï´Ó®®³q¡M¹±<pß­gMº\x001d\x001cö\x001cåhn(X§yH\x0003wLs­¡Ò¥\x0005;¯G\x0004}\x000fßÓe\x0010RpY\x001d¼=mÓæY±\;8&¶¬Ü@Ðu*¹±¼ÆË<åmï¯H®\x001b8ÜorN\x0003q¨]Aø9]ö|fzçúQÇÎ\x000e±C\x0001qªýùÃÀ¹· äf'Á×z¶8c\x0016mò£@Ûb@YmåÎ¹~lÍ³ýÜÂ\x0014WÙ\x0010<\x0015ÍKü¤ah"U\x0012x^°'ü=\x001e^\x0015\x000eÆ¨Ç\x000b\x001eèÁ\x0017 ÛágBÛ\x0001ÿ\x001dÂ;<Ó½¼Çéö5
gc`\x000c\x0013xr*h[\x0008\x001a0aú\x0019CÊ_¾Wxe_^þ\x0005G¯:ÀxWøð9Ø!\x0018m-LrÆNé§ãôÅôörA§­W±\x0015º\x0019Îß´áOÉ¿\x0013ÿ5\x0007\x0015Ôl\x0016t*\x001eôÌðaãÛa#³p1ý:?w=?r¯(û)ÏéQ\x001fQ|TNúü\x0012·W(ÜZ§\x0012ýO|¸áçÐ<§ÉÓ³À;Î!K\ÂO/¹Ë\_¬"ý
°Ôí
ü8<i\x0006I¡Zjß\x0003s\x000eðÜb\x000f|@C±\x001e\x0010®ð	\x0013Âöá_|d\x001dþ\x001dÎN.¤ªÅ\x0016©O|©ôò»5\x0017{@×Ð«Ï^Cr±\x0007\x0014ÿõgãE
óþïùæ\x0002î´j(\x001b<Aõ¿£\x0013ÔoGÜ\x0002<ñÿö¹çõÙ<~Ü¨§GuÔ-Ý^C\x0002Sß\x0019}ôS\x0002ü\x001cý\x001b<á½\x001eÃp;zO¬5oSØú©üpâÿ·.Î*á\x0013>\x0013!¼v©uüÕ\x0019¸@ ùðÀ\x000cÑÐÄÂ{«mz.\x0016gàêM]°õ\x0018¾9\x0015ûÑàá7\x0006jZóî÷\x000fP­VÃóD\x000fP+È\x000fú \x001a}­ôf·´®Gt÷îõ
¹¢É\x000f½µÍînc¨\x001aüQîP¥^ßÚ
¿H"Ñd¦Û\x0001Uaç\x000e&>XÍìÒ¢D¼Ðè®AÔK7IHÇ¸$îÐ¨×\x001dÏzß¦¼ÎV\x001cÌø)ºã\x0006\x001e2ÊÅAÃN¥Æ\x00088µ¶Ð"J#S4ÆòxQûPhÌÛóo\x0017äBh2bSc\x0012\x0014¢÷áÌ²öQ\x000f\x0016±½Î\x0017ZDiäÆä°B\x001d\x0005HÐ¼eØ\x000bÁ 4ò9[¢\x0012Äª\"\x0003òøJq*g¾äsnØÈçM>$>'ñ³Ä|\x0013Á^KÚîÐ¸ò
õ\x0012FC:4Õ\x001bd®íBçÈ55\x001aôçùøâ[9\x001c\x001ent\x0012\x0007bÔ\x001d±\x0011|5gJ±lm\x000bÝ~\x001dtwºá\x0000óªnnÎ
YÎÜ)A.#ÊC\[>nÐÀ¹RÕ\x001a´\x0005\x001d\x001bS\x0005ÒGMäruÖìÐ(r]\x0007³!\x001e¬R\x0016\x0007«\x001e#«£fG\x000cÊÜ*Ç`*A³¤³­m×Î¤¥
\x001aå³\x000bQ!r2¤\x0003§óÁM\x001fr³¯\x001d:óWtg%2k\x0003\x0000E\x0016ý¶y­{¶C\x0017\x001cu9Ûµe¼>Â¼[ê¾C\x0004æ\x0012`B´\x001cIÜâ\x0007î®Ik/½
\x001b¤¼ú·\ fÙj÷½>"wlÜ3¹"vêi\x0018öàÒ×ÅÊ¯¶¥-\x0013å\\x000f4×#\x0007;µ\x0015² )nÐ\x001eH"g7ùÈ"*Éò|za¯¹AãnÔ\x001dúÑÑ	\x001dû\_m\x001a\x0014\x0014÷z ÃÞ\x0008ð0×¼Ó­+\x0017zâ\x001b4®lUôå\x00172ËÙ\x00177H[×²\x0016AÚ°QPÜgÐä\x000bÝÐMéPµrl"\x0011\x000bQî}à¤=2Îä¾gÖMaé]Y×dEiÛ\x000f\x0013zrÈj¼}8â]?4Öm\x0007Ê'þB\x0019þ,>q®°g+Ý\x0010är,ÎV¹¤6¼ÿ3K®Ûº3×õ/°Ì÷Z\x0000\x0004rþ\x0002H-5ô5®ÔÅ-\x0011à\x001f?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001dütÇè~âmzö]k}H§ñðQ³
0[]\x0015Ü-~Ô\9Pö¦Õ²üùµîáZW¥\x0016\x000bèZöCôb&»4ìósêáæJb\x001b¼cJnº ñ)ú\x0018\x0013e£88du¹.\x0013n\x0018ñAi;ÊÃÚÆ¬[=ÕËVð¼ {\x001aB¥\x001da¶£lår\x0014<&ô`\x0000=µ¦¯\x000bº³8fBÑ+}S'ÿ­Ö~\x000e1§VÝ \x0000Ò\x0012Çß
\x0017»&ñ!æ\x001cØ\x0010s¶9\x001epLµ1\x000eCÙ§t¡\x0013ÏïÞ\x0000wïeJÈî8t\x0013ôÀè­£Oþ\x001dçèÐÇ~LU^¥Èè¦0zKQó=ÀÍ^
¯]ø*Õ)`v±O\x0019>÷4"x\x001aÕ:õ¢ÎéZÝd÷>NåÒ\x001aèÒª\x0012Åx\Ð]»-÷HA<^Êô9º2Ë©e"xw5váK°;t\x0007	z.M3è|ÏDØ3ºØ\x0007ºj\x000e:D¯÷Íá\x0010åÄp÷îO\x000fP§»ýþQüûk¥+\x001d¹Ò\x001aöG%]£S¼_,S\x001c\x001bCýyèn+"êï(¸(¾ Ò£æ\x0016(ÏUäÞh\x0007wÞ\x0003;`Ì\x0014Ú%s\x0001W\x0004¼sT[ÀmËæ\x001e.´\x0001I4göÑ
^3»Ù\x001e\x0008ð
<Öu°£Ï¹¨0ìRmÀ)Þ\x001e\x0019=÷ù
ç±hõæynß5ªÂé\x0017µ¿(ø\x001d5Y¤þê'x[\x0016Û§NL#\x0016\x0008½ÀÒýhÓlÃß+§¢u\x0011¡{ßÓÿ§kw\x0006ófç\x0016+ºø%ÐÚ\x000b]\x000bwG\x000e¡c\x000c/è£ºPî )
Ý¦îM\x001e²6;º7eöWJ\x0005-n\x001c\x0019Æ\x0013¸\ômÎÁ\x001fàë\x000e¹mÀ\x000bxLìe\x0007èxlè¥/K\x001dMù\x000f+iÏï¾~£bDo\x001e¯ÅiHµ\x0013\x001ad«'xkmKt½È­YóJ\x001aá°ÔhS.È\x0016OA\x0012x¨®§`Ð6*ÙáI¿@Ãn³Ç{G¡)$1É»	z	º !\îí¹½´&\x0001
Ö¬¢Ð«4Ð\x001c\x0007rÆ
RÒÎ$hB\x000f¡\x0018Ú\x000c¶÷\x001d\â\x000bræ5ÃµÞÎl¶Æ¬3`¸Å¬ÜðxhG5ÝfJ©o¹ÃËt®¼æQgH\x001aKK¥üLj\x000fWÌ<Úv\x0004¹\x0018µ\x0014M\x0006½h\x0019×ÚcÏ\x000e\x0002[·%3À\x0003Îå\x0006¿_Ím\x0017ºlakT·\x0012Ò/¸5õU;®ÅÜ\x0007¡\x001d\x0015\x000bGÅÈ)t\x0010\x0001³@,;ò¾SruÃ½Ó\x001dÛ\x0001¶»\x0019\x0006Ñ«\x001cÆ
tà0O\x0002óu
o\x001eÆÿ0n@±G)E±Hd]Gò,\x001d\x000b4¸\x0015Æ\x0006ô¨3÷)v*lí°L
îÐ°jí[ÇÄ '?1è`\x00016¶í3¡Î°!däÂ\x0000* b{2Iáý\x0017º ÙÙ9GoÅè\x000fßÑ#XÃíÃ=Ï\x001e\x0001p&dkgÚ"¥¥e\x0007ô#ñÛ¼¿ÃsNxÖG¸\x001bÄ6N\x001bÜ{ÑMÆ\x000eGí,ÄæË\x001al­ýä´Eìúömþ?;ì\x001e\x000f{tðÂd£,øê\x000b\x001cÐÕ.øpvØ½\x0007ß\x0010Áqð¼}u8Øã¨mÿù³½íCüç}s_FqÏ^/¯­\x000c¡À3\x0003s\x0008$Vo ggÆgX³Kût{Å.\x0007ìÊ¿\Ë\x0004à\x0005» 6½çrýSÊ"tÞ8ý­Ä\x0010ÎNMÀScìÍx\x000fjô¨­ÑÆ\x0001°Il+e\x001f³s\x0017èÀÐ\x000e°C±ãl\x001bL\x0011ÎNdÀ\x0013)/@\E ¡\x0017m\x001eÀ\x001dòÁý~ÿîÛo±SgÓÆÞüð+¥,R)øqÄ(áÂ¹É\x0007¨zµI\x000c?\x0017Wö'\x000bä5EWÜáé6k\x00144(9\x0004\x000fyÒr¹.¡ Q'\x001b´Úà!!2À\x001dÀ" E{Ò©¤`î}\x00077Ç©Í\x0004\x000e>KÒÉ2\x0019VNú\x001dZèI\x000cî\x000e»¨üé?ã÷@µ`i»Û?ß^/«%3|\x000cÔYÙé¹d \x0001¦ \x0017P}¡½$o­z=½4}n¸Æ´ûÁ.9ì\x001dü>\x001e©Ì\x001cR¦"Mê\x0003®f\x000f\x0012 Ý®\x0006ï#@×Q¢=*ÀÍ;õçÈ\x001e-ðCÉ!IîUþn=Ãs¸è\x00068\uâîí(\x0002\x000cõÁ	xtè¥Ú5+\x000e¾\x0007§¥HpäÆ®
NL\x0007\x0001¯¼òÚTA\x000f/â\x00007±Ä\x0004~dÅò\x0003âÔFPÂ2Ý8À!¬Sí\x000e\¹ÄéÈL
ÉóÂs÷­\x000fqÝ\x000e]QA\x0006X¹× ç\á]Ø½c\x00086ÐÁ/+Á\x0001#P\x001c%Ë®j¢ÄT*XÖáF\x001bàà\x0015eLí\x0012uV\x0016úªÉd6LHkr\x001a ÃÒÅÇî\x000eo8ZJøI;8L\x001a'tH\x0014\x0010æStGWµÏ+ó\x0019\x0015¯ñ¨~FèxLLiëLÉ\x0004î¦\x000b 'yËL¬\x001dàe'Ö¼ÍÐ¾\¿5R!Rõy¯þQÏ7»Í~r¹?û0,©\x0014\x001eií5\x0002ºÁ)MmíôQµAjBÞÑ!¬	\x0016è
ìËG\x000e\x0013|oÁ94$ºTÛÄÑµg\x0012\x000fR´!\x0013z×-=Æ|\x0003\x001döK\x0016¯f¼µ\x0018fVä>±Ôv£;¸ô\x0003\x001dúì©\x000e\x0019læ7p¹$)\x000fìf2¡ã'Uú+Ø]¢a¤bk\Évo\x0013EÑÙ\x000eñYRvÜHøâ¨¤¯móÀu\x0016ðì6½3ö?}»È~¿y×eíÞ¿¿VGJQQ"|áC&#\x001fow	£y¡º¡\x00182­t\x000b¦oÒ-Ç~S2\x000eï\x0012l"H²ÉS)Ú~í§z®\x001aFr@\x0011)úØ2\x00016\x0012ÉMßúxøâßÜÿéáý/þÙí÷ïÞÝ~y¥8K\&ÊJ©\x0000ÙHâ#G/)}Á¾\x0010ç5èPùEÃÎß¡[KµÝ¿<Yæ\x0006\x0012\x0001Öâ$h±A1d°-1¬|Î°\x001dØ.£ç]\x0002M°×\x0014<óÎmKÍùÃ#°{ÌhÈÂI®m?
{ÞÞÿñ=þÇØÿúæÚÍ ù6¡1ûú}	ÈaÒfÐ\x0017»þÎ,@·×\x0005ð\x0019Óv:\x0004pÞq¥,¸F:¶sìØPáó:RÏ\&ûæÄàý-éL\x0000\x001e\x0000<b\x0007­}n\x0013ûéãåc2éáë÷ò]`\x000bÝ¾úýãíwß]+ä3BC\x001eÔ\x0017ë
«Óeë\x000b]o'}\x0016
Ô­5m ßñ	\x000e¡>}ÿ×¿Þ­Ýß=<=~y-§"*/\x001f\x001c·ý.ú¢wÉ7Ø{3}n¶©kuý+5æoÏ¡ÃGBÏ\x0018@§.çÐå£ ç
úôÇúWl\x0003úû÷¯îUÆBþkíMeþqEÀÛ=åYkk³Ý« ±\x0015ñ_dszþDa7\x0019;¼g?ãY\x0013,2í>\x0016{Î\x0015\x0002¶ÿXìùT\x0001vøXìùr\x0006ìø±Øù\x001c;,öì2\x0003vý8ìùÐþÇ7ß|ÙZ&g\x0001öûÛW¿{óxÇð*Åä)ï>bò.C\x0000t\x0004íKE0'>â¼ºÉx\x0013%o±I"ùPN4\x0015E&èõÿû0À-\x0007ÔæñÑß8\x0002/¾2x(Ëð\x000e)a7#­*þ;%²Rôi'ª
ìwöñÞÂ&júNo¾z8è2~à­\x001f\x0003³'ä\x0017î\x001eüÖ}~¶°¾d©qí#\x001e*øÝ^Ì@;û\x001dÏÚàÈ»\x000c\x0011ÆýV~Ýk¼Ë+åP8\x0015.æ"ªÌ±\x0005£ì{ÁôeÈêqEV?òKÄf¿n\x0012~\x000b­Ì¡Vf\x0008ÕqÜd\\x00138}/ÐPô5ª<^À@¤AB5unuÀ#ßkF¾W¨Ð\x001f'ÐrY¡TV5ÐÆUãð\x0005\x001aIY\x000e[{Sv\ª\x000e%1ÂØÞ[r\x0006\x001d\x0011:\x0010NÒÁL%KÜdlwkÏ \x000b\x0012à,ÖE²Ä\x00119Ú	¹\x0011à\x000eyè\x000b2d¡kIÀÀ\x0016dGý*rD\x0014czö|Ù±|¹<BÏ\x001e¿5¹nÃ&\x0002R>	¹Ì=uÄ\x0005Î5ôÁ\x0006Ç"Ô\x0005\x0018i+:£\x000cN¥y\x000cÄÛºq~íÜ´A\x0013¹)\x0001$éäP:ÚçÉÐ-ýr,\x0011]°+\x0013àeMûà\x0004»p	:;¸t¿ÿÓwé»?ÂówÅx§ø0ehì^ËÅ\x0003	³ewH\x0008÷å_¾#½±Ûjê8ù!Ï\x001aáð\x0015\x001e¾ñoÇW¸²\x001eÔ m&÷\x0012dEF3m5ÇOé3\x001c®n¬/H\x000cdù+ýùG÷Ã"ëìW÷÷ÍûxóîÕoüUÉòZß¢Zf4NEÀM²YZ
ú\x0013r@¤KëX4]OD\x0006\x00011\x001dÁC\x0004X\x001c{åÅ7)c×À\x0006
Ýl¹¢þ`#:PÂ¹ø¤á\x001a1æx^ ±\x001bqsËk\x0003®åJ¾ë\x0004£?ÖQQ©Èë\x0002ì0/9ÛÑºûÜ\x000b4t·+'!3Ã\x0010MY¶á­ÖÝcÜ\x0005\x001búãt+V\·ç\x000e¶j9áÃº=î\x0002
tsy\x0007±È®\x0003,\x000c\x001eWyÙ$¡¬%(.Ø}<AÏ\x001e>u~\x000fí\x001b´³¼ì\x0008\x001c\x001eUt þj&úQÆN
;Bg80 ·I{Õ[~È·\x001aM>\x0003Î\x0008ì ý#é´A«Þ3¶ïª\x0016æä\x000b6¶³gOØÊ&hfÔ\x00189\x001cGýà·_~s\x001c"þÁ>&¾\x001b?.Ý&\x0003	~e\x000c?ìëOs4[¼GêÿE\x0011\x001ezµ\x0007]¤Iqê	5S\x0008nbÍ¡È\x0006
¡²Aè\x0014X¢Ãr÷s6kÂà\x0005\x0019îs§#!4å9¬å¦\x0016ñÛMp\x000cV;6êÁ¹mêßn\x0010Ë\x0002\x001a\x001a)óª\x001bÉiuñvl¸x2¦"XÄ³\x0012-SYØ.õ³uCLéÀ§×¯HÊB¶N±j/Ö,\x0019\x001d$U V\x0008\x0015FñquL\x0016É¦·´\x001céd;6Ôµ5	\x0016m\x000bîâ´èOîÜ2ªò\x0012{æYG\x0002ÝÊ{´ê\x001f\x000eC"\x0011\x001a\x0016m
¼\x0014º=è\x0011r»SMÈk©¢\x000b4$3¼²áaÑ¥5\x000cèRø(Æ
vÇö
\x001a×|*è\x0001eñ\x0000X·r\x00127ÞwRÿ\x00196ìjM¦bz'2=MçgLØ±­û\x0018\x0008oØ!<¹d½ ´½\x000bvÁ
µ!ìäYÄ\x001f¶vëW_xA¥\x000f\x0011Då¶\x0004R¥6²ðCââ·|«²nNÚ°ÁOÖIàp C¤Nã\x0018ÊÜevÏ¶v­\x001d5{\x0006Èr\x001e\x0011Y.ì9	ÓÎl\x001dH,µüýàqì\x0016&Ã\x001dò¥\x000cÌ"0:l¤Àþs]Kl`[f0ÖÚtS"0\x0017ll)ñ\x0015u\x0005R`6m­i\x0015"¸pV´ÞôÙû{\x001dwp¥4u2aº}Â.\x000eP´5Ò1Í/ÕS²æ1,\x001cu\x0013§,¤ö¿'Ú£(É\x0013ãvj9ðö$â2s;u±Ó\x001dYÚõ\x0000Æ¡9,æá
\x001bÚç¼\x001a¸Gs¢ý¯dxÞÿ=ÀX$8/ØÈøèOç<õSÏjeF[\x0010ê\x00158ãWïòæÕoUgöí«ßÝ>ýõjj¦iRd\x0002}xMûB?»v¼ú\x0017ÊcDgÝJ¿âÐÌØæÇ:|I¤\x000e\x001f2ßFâ°<|j¾éL	ØÙ©¶Å³?-ÿ\x0004+rË\x0016^\x0010\x0002vdp<@ÑF\x001eçIêûQU2nÁÞÙQAÜ$LqG1	q'Ç½\x001dé\x000c9\x0003²E¡l-\x000eÓóê§Vü\x0017¤ \x001d·|ì\x0017íÛ\x001d\x001aép&¡B\x0016ËÉö²[Y+ÚËòÚ\x0006"Sr·Àü\x0011/ÿ<UQ}JÜT}\x0016j
\x001d\x0019Õ«å¹CÙ}Ï\x0014)?)úÇ¦\x0018¾èøíÀ(¸³eà.À¦%\x001bÀÛûåE«.¸\x001d\x0019\x0005·-
P°»Wå;ðÖðå8@\x0015 3BW 	´c×?ØÌöð}|ÚÙÎ°¡#ª\x001b5{°|ºöÉÃÓI\x000c«dè­Vy=*Æ©?-ÒßÜ¢µ?ô \x0002üEØ"Ö0
Î:oÃk§\x001aFY¶\x0003] !ÕöB\x0018©S<ªÆY¬Þúµ¨ê\x0005\x001aýgm\x0018\x0000pK\x001fX=°}mÚ\x0012Gª
\x001bUª¢J\x0004\x000eè\x0010©Dª¦ûCæ/dd\x001a4
{Ê}@²¡²l÷-d³i·ÞJ7 cC1J¾\x0013´\x0019jÚ¥äRä+K´}\x0014
½`£ú®6\x0014ú®xld\x0013	«\x0012cwáÍ³]\x0012`¤H\x001dW\x000e;606\x0015\x0002ÂN-p®¼`cb_î>\x0014,¥%'¡S\x001fºhø	r4Zvæ<)@èsÅ
\x0010]\x0012(\x001dÉ\x0008G2»@TR\x0003OÂ.µé'»$¢(îÚ={ÖµkØ'^S(\x0016ì°^}â\x001c8Ì\x000b²¥v²Åß\x0014cøxì\x0013\x001f'Â\x0008\x000fÆ>ñFô\x000f\x0003»`Stue:9rðmûì³o	\x000fpbHt	væ«;g\x001e\x001d#ØzâãB\x0016¨cC¦¥cG¬_å1Ã\x000eT-±\x0018Zê=îgnT\x00027ª©.hÄQ4Â¨\x0004¾©¬o1ZZ¨àtl%ùù J9²âØÜ®´i:gÇ2Á±,&Þ$.ÜRb°pY:óx\x0012VÜlÀ\x0006Î¢®\x0004B'NHZÛ\x0012øùì9ËðéäU¨¸5miÎ<éÊäÚ|©3§5ÓªË$5­Ê~Iµ\x0013Ã%µ6årö,\x0014TÖUª\x0016\x0014ÆtØ0ißÀ\x0015¦ÔÚ·ëI*DO8\x001c\x0014ØSKZÃô`õù?gÐp¿V}Ò\x0001Ú\x001aæÓ0µã×ö%ëÙ&©°Ij5ÛH@u2e*ùn&_Çjb&\x0016Oc`l.pnZ±æÄ5±Ð+&ß*Sé^IÆÔ¬j¨!0ÉûV;øÚ*\x0016"§Ög\x001bQ»¡R¼¬#¹Um£lØ'7¬\x0010G°\x0013\x001eù(ÿ*k	)\x0007ç^ß½;Í1|ñº\x00156?"V=rgQ³T'jk
õ÷woÞÉÿòÕW¿{¸»ÚHC
üÕ%-{\x000eKîi\x0008«³ÝEú\x0004'8\x001cT@èj"üØdÕv\x000bÈ-6Y \x0015Ë\x0016Ñ\x000c¨Òs3@Ë\x0015ÛÉgg\x0019:Äµ\x001b4(»RAÙ¥A£²×p\x0001}t\x0005Â¬\x0004\x001a<×&A\x000c=×^cd6Hº8Þ:á \x0004j\x0015+\x000ch-6\x0017Î~²µ;aºæ9Çlmf[G*xq¼\x0002\x001b¤ÏiY\x0010gJqOüÍÐÐ\x0010lnOõJ\x0011bìxFHíØ@Hµ9CC$P"Ø«ö\x000ca·\x0008qE\x001aíÐ`\x0012gQµN>¤%ª¯
ªjí¼.hÚJN\x000cM¤jÅïB_T>GâMâl\x001fqb\x0000Äâ\x001bs\x0003;\x001az÷¶Î¥?Ü}Bç¡~seÍÀ¤okÂ\x0019oC«P\x0004ø¥ú\x000bJZdÅ\x000fßXì5ewPÿPÒDÛ© à'ùÀZ×¢Î\x001b4¸íNS|¼ØDÎ\x00074k\x001ev±£Ï´\x0001Ï¤\x0010HÕ1¹ÏZ¤Ãrüå\x0005\x0017jÚNGb °ç8C\I\x0001²®å7hpÅl%U¤*Û\x00129¦rÈ(W[Xg\x0012;6f\x0012µM\x001fôyTÊÃ¦ð²mOäÈÝqí\x0008\x001bÃh}8Ió»ØIö¡Ë9\x001d\x001få
\x001bÜê¦]0\x001c±j¦ùoò^ñºsoS;Û"Èvtäòå\ÖÌS±ÄÞºMoç*Ú%AR<rÃ½f¾l\x001f\x0007êoÇv\x0010}Ù\@%N3Ó*\x000c'n­)iÍ\x0006Ù ÑÜµdÅPæ¸¯Ú\x001c×Yá\x000b6,;Â8
MJrÒB¹G\x0004]pô"+¼ACVØ*{\x0012Å'²¼+\x0005pwö%\x001d~ÉA\x0001<É9a.¯ô.Lmyòã»¼ACR¥Ö±¹%W\x001aº\x0010j:bGýWÑ±=ð*¬u0G£Õ¬©)§N£¾5éöÃRÍø
ë¶DÕ5ºAÚlÄál\x0003ýÙæö¸¹u\x001cò\x000e\x001d«\x0019×<ó¨\x001aü8xì
ÙlU¢ò
c{NøÔÖ}ö-=~K²(-m>bsÚ¢tjÏÙ#\x0019PÎ]\x001e\x0006xsÏKó	j¢g2ÕØUÏNÀ£#ïYÆ¼E¸aèÌ\x0014\x0019ql\x0016.V\x0002Ñ_½~ýãß^ýþÍãã\x0015õ{}à´}Ô«0Í h\x001bN_,\x0002m%¨v³R\x000bù\x001aÊq]EWê`:4\ íhðÕâhLo<8ó\x000bÑE»¬_ ~àiÔ¸¼¢¡#W°ñËÚø\x0006í\x0010:¶°p¶Loöa\x001eÞê8« C#[³âU \x001b¦ð¬P?yÑôà\x000cy¨\x001cH\x0000Ónñ\x001d9pu<r
G.ù^E<AF\x001a¨üþ1èFa×òsÜâ\x0008¤e»ì\x0005Í\x0001ù(
¿û>òÖ\x000bu«\x000e@G®p4ãäy
4}D\x0015ÂUèCáý\x0002\x0001\x001aC\x0005:Ý Ò»Bs¡¹ø%ÅaCNlj¨M\x001b3\x0017®iÿì:0Ù #í\x000f¨»»0\x0015*d0tNiM&ëØ>#>\x0014²÷\x000cé.(6Ë6Õ¸¸Í9¤\x0015íøï?þíÝÝ»~Ï])hv$é-\x0011\x001cB\x000ek¡¹|óB=¡Ï¯/ôã
f>±Vû\x000fÆ6RG\ÞÌ# ·w{¬4S²R¼Ò\x0008¨å¡WrL2C·y]öe3M\x0016KÔA\x0001FÒ®(\x000f©\x000e®ÒéÉ\x001fóL:6Î3±â=\x0003Á§L³\x0019dGP%£ÈÏðë°¨cSXä0äjãØ$u7­ië^\x0004\x0018\x001b6­{µ\x001bÝÈ?¬\x0006ùnÐ8Æ×ª¨þ< \x0013_\x0002ÇEäi3}KÎ\x001d\x001dÇ
\x001bû´
Ñ\x0001v¢~\x0017xÝµ+I.:óÍ4\x001a¤9Ó£k¥aS	C'PLØ»¦7g0qõ¾zxº}üêÕ??>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=è¡©VP\x001c\x0016w=4½\x0011dÍC ?¿
Vã$±D.:¿!ý<ÑMNî¯+Õ¶N×Þ²·(uÈC©Ë«t}öü&DJ«¶e!t:¼ú\x0016\x001bÀ\x0003Û{ª(»-ÏÈ©X\x0017¹\x0016j¯D-\x000fÙ\x0013{<d}*¨Nª\x0002ù;\x0017\x0002cÚCþUN¡a»Aó;5\x000eu\x0019U '«ì<³|sH6ä¯\x0013\x0019fDÓuã
ÎÆ2áÙMåõ¼JÈã)áõè)°è½ÿ\x000e§ÚVn\x0008Ì­\x0001Î/\x0015\x0003Ù
WÞ?TFÔ³\x0002[Yþ 7¢Z·­d'¶\x0007ìâ¡cäu<Õå /)\x0013{¤$îO\x001e!Z	X\x001d;\x000eb£LUVäÁ	D;ÔÍ\x0011±kÜÇx\x001d\x0007v&\x0014\x001f\x0013eÕ>d\x0018»Ý"qÉ¥Ø#âeÂ1ÚVlì@JJ\x0000aì\x001e¹Þ­í\x000ckÛ%Â¤Å°Á¥ò¡'£Ø§ä§ç\x000f·³ò\x001býá\x0019ôCíz¥ø7¨\x001e¾ÑI\x0005f'urý\x0015P\x0016ø²¿bn'bcµÓþíÓ_?ÿÃÇß¾}ùãÇÉ°ÚJv­\x0000¬J4ü\x001a®ÁPZßÔgä[gHý\x0006û@~#ÏýsòÊp<\x001b]!ô\x000e\x0019ÔN¢ÌÏÅ\x0012Ë¬ÊIÄ\x0012\x000e=ÝäÓfH\x001f±ÅW§fYóô\x0005ë®\x0019åB\x0006½¦3mÌÔ\x0013ïØ\x001eà\x001có&U7{Dj>\x0007×Ö1'6eÌ[Á\x0013\x0019\x0004Oúµ\x0004C®4ÍìQ¢À­`x\x0007¿vÈfÓÙ#Ò\x000cÇZC¦¶aèXSä&¶íÙ<¾!«{|É
Yº\x000bÀßüíÓË»Þüâå­ÊV>æÌ).²Õ>G.^SªØ¬Ü´r^Å¡ZN|½çOT{\x000c=jZ\x001bGCT4bøÉà;5^È:\x00130[%fE+V}ò\x0012µE-Ôo³½C\x0017A\x000em-øAS³vfbã\x0000{Æ%Roi¤E£òÄ\x001e\x001a!&\x0014D¯oYÛ×³`J-g\x001d\x0017ÉÎ\x0003:Fänx2S÷8Ê¹°\x001a]I\x001b\x001b5Ì\x0019;AÑÛç|úðns\x0001=èî¸H¶^ö²Ká\x0003È\x0013:÷*rHµ|ÒÎát÷`øâÅsÛ³°/Ý\x0016p
vW±\x0018¡OÓ«O¦å³§Øº¹w/àqï\x0006\x001f¿3x!\x0014ö¯ôSSr¨Í½{!\x0007ºÃP\x0018ÍJ¾j$\x0006®;kæ\x000b8Â)ç¥ÈÔ\x0005-\x001båÚ\bÖÐ|Õ\x0019û¢Y^_áÎX°\x0015ÓRM=\x001cYúJÞ\x0013;5°\x000byHºè\x000bk¼\x0004¹°þÜtÉæëvwK\x0019(\x0015û½ùÉm½ËÒ]È\x0010ì¥\x0000Yp_Ü4h\x0015ùæîYË»Åa!&þøâ\x0002/fW'\ýÖìz;\x000f0}È)óôþAF\x001f5Ï
pn\x0008Xk¶Éã/R_IcüÞ@yQÑ9l\x0005¬ñÍ³2ëÇo$OÑ[¶\x001c\x001eÊh\x000e5K6ù@\x001e5v³B¯b\x001eäÇÃÄë¢îKwÀ\x0005
ÖbÎB)¨-ÔBÐÞð¨»>àB<¡+:\x001d@§É\x0010-ÌÛ«¥¢\x0016\x000b:\x00024zJ
´£~	9\x000e9SmcÞu]]È	æ£B±\§÷²_\x0019úPf¹\x0019µc=ki\x000c&Ä\x0006lI×Q'\x001e¶)ý3®/ñ%é\x0005Õ\x0015¬¶µ¥¿f&&­½\x001e)¡\x0019Ðàéùð+y>¼{ÖþÏÞ=¨\x0004
à4\x001c¼
VÚ\x001b\x0004ÏqÛ\x0001¾ù)\x0011å­÷9ªái¶\x0003JAsc\x0002(È²{Bäçit;Ö\x000bÙ}-òÚL<\x001b
¥P+Æ9\x0012O¡I³\x000b6oã§\x00137\x0010.¼§½e§ÏÄýÏ*·ºNàÁ0&#ÓYÎ06ôJu\x001ers@]\x0004\x0007r!'hÔõ¸ú¦ySBÞEO',Ôeµ×\x0013a#ÓRÓ\x0016©;ªë\`À\x0001\x000fáöh%dce®ïÂ²\x0013¸Â=ÞI
8Ó9\x0005\x000fóçpØOA]68È©Ëç«D×Ðº¬Û¬¸5â;¡-nÒ;\x0011ân-ç´÷Ìº\x001d­\x000cfM1² ;éÐ\x001d«ïö\x001f|£IxÛ%yv[ÚÙìåUoWó½ Ç\x0016z\x0002äe"gó4è\x001e[ßíApê]\x0000yª&k!¡»êûÝ&\x001c­©)Jü3ìP%ÔÎü\x0011%¶¤NP\x001bõÝF\x0004ÿnù/ÞRÈ\x001bÜdîtQ÷U}·\x0013G\x001fÃCÏªi\x0003\x001bÌ¿\x0018}\x0016|\x0003ôa)­^j\x001eW !
\x0013ó\x0019$´[ó1ß[ÌLÎ²\¿xúH¦$ò!vEBqVz¸\x001c),%ÄíAê)¬o\x001e`Ü¨³-ú\öÈRÖ¤d
°8¢u,åX¡^
£êæº¾GcRäF:;\x0019Êi:9¢»5¸#\x0013\x001ae¾÷»çwoÎ'èüë¿}ÿòOm)<è	ª=®)1ã	Z2\x0000äÃÛàûè£ß¤ææ;HgrÊ¡µC\x0000M\x0000HÁÇU¹\x00178\x0004¬e\x0013ö\ÀãÄ5!b\x0004\x0018\x00137!¨.\x000bávE£ùP¼ËW\x0002/AÄ\x000cAÄ\x0017"ßM\x00068f×\à³g¿b\x0013¦2Pj9´Mz"\x000f6ispÆ¸UÕDð66ÉpF14\x000bË|·4òX\x001aU\x001eã\x0011"Ì\x0014X¼¸V?½\x000eº9ô|ÓÐe<kk*Há;\x000fï9Zë&ßvá²\x001cÐ\x0016ÜìT¬\x0018½'Ò¤K[ãü¦érÎq¾ê/ì\x000cØ¬©³û\x0007v\x001e	©1Nl¹mýÁ­ZÙXq\x0013CòüÊ¹4íâ\x001exb{ :¨:¬æGêê5dy¾{ó[ÜÉ\x000fl\x0007¹ò¢¶r°Q\x0003½N\x001a<^E¬ZüÍÔ\x001f\ØÎPT¯ünÓÙTRË7;RðgNòOÞ\x0002ôt³ºõ\x0007#i¿Ã/YTsù\x0000M½8ùB= õ\x0007't²\x0005ÅN³*\x001dàq­Ó°[Ay\x0011é:±AÐ9ªH\x0017d\x0003ä\x001f
®\x0018§ýÞ\x0019\x0012ÑÜ\x001cS\x0011
á1¢§§`{öS¶N|Î\x000bKÁ²·\x001fs;Ó¤èôã\x000bÛúé[&ÎÝ\x001cÈC\x0010«\x000c\x001d\x0008Ð9;6mW¡eÞ<M+.»9\x0008\x0007ô!],ï°Éþ¨ÊfJtÉ7RûÝ=øïà\x0004wÐcØ\2àfª°´YÏî{ô\x001f\x0006º<× q(·\x0005-iß«É\x001aÚE³±\x001bTSÌç\x000fÏï?>`
  
  
  
  
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
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=~x÷w_?<=¼V½Ù×_lx`|MÞºo®u)çº\x0013¹;ßK1|ÉxBà¯+Ì¿íyo·²¦È\x0010Æi\x001bo'dgÞ=Å oYÎ'2Z¹àµ4éÆ3¸{ýµ\x000bñPÞÏ\x0011hñí_%¬»xÉ\x001fÈø\x0017¯¯©Î£÷\x001cö¯í\x001b2|?yÈ{\x0002¦©\×\x0012á-í¹\x000c'2\x001b\x0002=µÞnò]µî\x0003&4|À\x0013cÕ\x0014{çÍN\x001fu«oË±u@sþ¨ó.Þ\x00074¼\x0001µc)x:vVm\x0002OeKÛ?ÔnÐ¨bPè]¢¼1\x0014h\x0005Ã¾Û.H&t¢K	r\x0004Ù\x001dr¬\x0000Í1mÑZêÉ\x000b×rRfûüî·\x001füÿ¾¼ÒÄ¡ïZÂ»\x0004¢ñö#ªrù¯K»jú8½5\x0017¼'
:Ý²\x000c¯E\x0005àÇ9?Þ7÷iµì\x001f	¢Ó±ÈKð­:ªZ-#àÎÊÜ\x001aÌìrá\x00138.àñj-&3©ß&öÝsa\x0002ç\x0005\x001d0\	0ø^¨0/À»z÷\x001cä·ÿ('ö×_ÿáéí£\Ô\x0007£ÿ5®ÅÌöÙõqC½­\x0003[ÇÇO\x001eXÙLS½QÆ%Ê'OÕFÜ1ðlÓ7ÙîÀNd æÇJ\x0001ä\x001b\x0007ûrV%w[r[þ¬\x000c\x0012\x0015	'\x000c4AnÑ÷íO\x000ev"\x0003çoAROA\x0016K\x000cºÉíÛñV9\x0019ÃDÎ°Ï\x0015º¿«Ö²Í9¿Z;:\x000bO÷ï\x0004\x0006>áÉ]Í50M¼¶³YrÙo&òz§È\x0007¡Íhü®:UùÊw±Ù\x0004\x0006bq«\x0011Ws:æÌñ\x0014,¹ïMnÐ\x0010)/YÇ£Q8k\x001c</p><p>\x0013JiYm[fÐËRZH¼Ñmp\x0000,èî
´ß3Nè\x0000Ð\x001eISF\x0002VÍ·Æ\x001dúêD£èÊê\x000eÝ¹Ò©¡;C}ûðFi\x0014\x0007)GÍò^Ç\x0015î¬'ò: ­b®[\x001e©iÈÜ vêsàwÀOîI´CyZsÆ1¶D[Ýý\x0010Æ8\x0007~\x0013\x001a¨o$¦ô\x0000\x001d':b'Î&ÿ¸O£Oh ¾q\x0015uBôqiC:÷<«</p><p>Á6×=¡¿ÈGh/¬#\x001bÇ:9îy¾éçMÛÍÝëQÛÍÅýùÍ»wÇtYe9Â~ûôÏÏ¯D¢bæúÔÄÿÝ­·dSé¿VµgÝF¾¦/~Ü7÷eó¤Èöë¹´ß~xøîI\x001bn^)L«³æTZ÷úâY&Òo¬òoê+½!]¶Ã4¥
CÆ.ýuÏàkM6æpWÀ ö­uÄuõtx¨[y¸·Ë-·\x0015\x0019Èi!kÃçºyú-¿\YÍ/\x001ctçÅ
9/ä}AU^>ì²*Õ+µi#mµ-'rmnÈíØ\x000fÛ]Î¼\x0019¥l[a&p]ÀÚ£\x0001KÖn\x0010tr[\x0014Þæ¸¥Èm!{M°Í¡_°ã5ç$9\x0007S7è\x0015L)7\x001bÒFöYÍ¥:"9èãû	\x000cG#yiRú\x000cîÐ¨õüB\x001d
	½{ü\x0007øøµÕ\x000eH\x000fõpt>ÐælÄÍm=1R\x001eþìùá£üo¿\x0011O!Näµ¼òHãbi÷«G"?ðj\x0012Ýú7ÈVÛ\x0006ý×\x000b²%æñÙU(\x000b¢õÞ>46ÏòwÚÊ´ÏÇ§ £\x0014eíÍ
6#6(AÈV÷¡ZòKAî0ý,kfú×¨bÁìG#×ùàZöË\x001eT¾e]ÅòsÌnp\x001e&\x001e\x0005ë![¾ÇÑ¬\x0001Ø</Zv¼\x0019Göür©îQq\x0018¯ù\x001aÚçÂ¬ÑÞÞIXºÇ®\x001c<\x0005~(Ü×*³1ÆÌÑ&3å¸kô'X´éÂhc\x001eyíå"'rEã\x0005Òò&\x0013t¥§­Æé~û(ÐËÑ\x0007U*ýP:NÐÆXÒQx8
't_Ð\x0004àe"w­6¦\x000fQí´½pÐ
:ÀÑ«Ã?Ô\x0003é+6æ\x0003G\x000bá¹miB/K\x001e\x0006\x0012w·ZVIç#]4-M`8y{§ûM½mÓÐð\x0011©Z"Ðá¶;Èëªl{inÐ\x0011vZãF®\x001c=;ó?uýÛ·½4\x0013zùimü\	¦äG89| ý\x0006\x000e*ü+\x0007²ziÄñ\x0006TvÊcöD¡Òå
Ý¶
/\x00139\x0001r~ßÀÊ»1E}~3ôÁÑweå«/EN#×¤|þ\x001e\x001f¼c£¯Çê\x001d\x0019G\x001aÔ¤½Îò0p5Ð#L<7xÜ W81Ô
\x0011èÊ	ÈhD] Ó;\x000flNhøÙ£Óó\x0013½\x00052¤Á'dÿFÈõ[Íù¿N¼å¼g\x000eÂ,N(^d
âö\x001b;éÛ</p><p>·r|Ql(\x0007E%Ê\x0015</p><p>UÝ9ê^ËePSÛq¶¼Xí¢ïÐæY\x0004EÄúå#+@¥Ð·ý\x0001\x0013\x0019¸çz%äFr7JÄËR\x000fÉÍÃ©óÃé &[sµ\x0007#V;C~6­Ý»©s¸UÂjÂMn¼`×¡h¾}°uÃ
´ËÀºÑccZB\x001f\x001b#ºo\x0010Ðð\x0001§Í\x0008\x001cÕÍðürÊå"$ºA#{ Ý0L¹\x0005åÝp{\x000b\x0014|\x0015{ñ\x0005Ú\x001bÆZø\x0003Æ²ï\x000e¸A\x0007øÊ\x0007\x0012lßÎ\x0019:äòê9Ý:¡\x000b­\x001aø][íÔüu^µ/»÷i=ðoÎò_ëUÚ:½÷Ú qsø\x0012ÅÁëJyúßZ	ÿjüðôªáÉ½øqßÜÍ\x0007j¶jýüøññËWË:&ÿ\x000f>Þs\x0006ªHR>Ckáíq:ç^2h6eàÅM/êí*@î®)Õs~Ç]4X42Pd¨ï5%}ý\x0016²Øüv&p"cº+A÷|F'ªzÏi4ß¶¢È\x0013\x0018Ò¨O&¸fD¦²`º\x0000$ÇÙ·6S¡Ui(\x0014yoÝ¼d+(X\x000cÁí¹oÐTÌí=$f4ü§Ômç<h\x001c÷A/e¿\x001dã\x000fÖªÛ{He»ô¾Ó+¯ùú\x0014sþö\x0006]1ôùñ}î¿\x0004zãn½\x000f>ËùôÇ\x000fÏß¿\x0016¼|\x001bbÌ¡NêÒb\x0011"=ïÛ[H¡r¼ì%û\x001cí³¾Z¹û\x001bÙì\x0004YÕcôvãrLÃniòpZÜÅ±[L°5^þñ\x0012p"GZ2ÈOÆ£Ég\x0001'&!Ï£YlãÊL#piúÄ\x0015;\x000eºt¸W\·ê\x0015\x00139Ã^ #{\x0016ÇÍìÕrÜøôÅ°eÈ+äjò¨^ÅóñùPÌ[þ-ò95\x001féWH\Õ)­x¸2T2ð} 5\x0017V	É~?à<WpÛÌxV¡û\¸ÅIÖ¼ç\x0004ÈÖ¼\x0006\x001b²^Fô\x0001çmvqß\x0018}CFEÝ\x000c\x000bEJ¨ -×\x000fÝEïÍ\x0006\x000b,t84j7¶#É¿³T5Ót]T$±ÀéðZÛU¼Ãx½1¡xqÐ`4ó=VÙ\x0012{²¸¬ú"9ÞLC·n%¤(UºRØ:\x0018ÌÉëûäø
:óªnJ+%³k%ÎÏZ¸x</p><p>6Ó+>DW²O6«\x0005®²\x0002µz©¶
6Ó+>Ü\x0007\x001c)#§«$\x0017jºÈ`7Ó*^4ÄÄýÐ*
9éÊÞ?¼{±µvî_ù\x001f>¿ÖÀw¿ñ[\x0003Gyuø*©_\x0018¿àM]Î%x|ÁíÜL\x0007kIðXOÄ2}yøy¼\x000fGâÆ34ÓÀZT<3-àÈòyÈ \x00058\x000f»_h¦µ¨2\x0003\x0002\x0007.\x0013)\x0002§F3í«¥´åËt+é~4\x0000${á·í«\x0013\x0019ÆáÄ)DDN¦Ë4¢¿Qä´ÕÈ0ãÙÜê}LJ=ª\Ð\x0018Û\x0018ù\x0018>ßÜÎÍô¯Û¼ÈDîçi\x0004ÉÉ\x001cÕå³i¦U|Âb</p><p>×57®.\ÍËVãe"Ã\x0000_\x0005\x001e¥þó\\x000c¥5«n\x0003\x001aZc«¼,|Y®Gy\x0004¶Ã|ÂîÛÅõÜLk¬®Ú¯E\x0007¾uÑ\x0016FOåîvn¦3V>öºøeÑÍØ`æ\x0013\x001e!Å\x0011z4B¿ÆPtÑ\x0015){Õ\x0008[åE_\ÍÍtÜV\x0017×\x000c¦\x0012:f-</p><p>\x001a|<F@vWsã«ùX3@ÇJÅ²\x0010\x000cò1\x001fveÐÊ[Ýj\x0002ÔSWF%\x0011\#º¶ç\x001eÈ8ìV&A 3KôÉ½UÈ=Ç£ñ}wå7Ó%\÷/Án4î|Ý0ÛÑ.</p><p>â7h0ÃýùÍÛö"h¦\x0001¹jA\x0000Î]<J)[Ë{]ÇXÄ}dB\x0019\x0016¨(¶i}¢Î\x0014Aîc\x0012àÜÚ<\x0003\x001d¼ÎûAm\x001e:YÌû1ìpSÅ¿AóeXáìug\x0006#(&ÔU»M\x001dÿ\x0006
×¡ò[W6³-ÙB:þ%L7­[_QkÍfø\x0003¼Ò î+\x00047èÂÎ´\x0003t'\x0019G¹\"YLò£ïîL?2¡+E4k«UìÏl5ùtA\x0014=áBÌu=ý\x00049\x0006"'³)ÅcPóÊ\x0012\x0003N´×5¿ ÈÑ|C_\x0012C\x000fÕºMÃÄ\x0001
ä#Ê.Ñ`£ÅæIî50e@ï9¨'r 4\x0001p3ûìgàÞ÷M
7ddñp\x000b7Eª³û\x0016øÌ¥¼gð° iÞÓê\x001dQjçÎAúm>\x0019#E²é¸AÃ|p\x0007*GU$\x0008\x000císæã|P"I<&ô:Î\x0012\x0019\x0011æÈ\x001d/:\IÐùØç«\x0003
$\x001eYßê`*Õ´-ùÈ¾4\x001d$óF\x0003\x001a6r®«[B\x001b8<½¯£\x0010ô¸µ6}\x00187d\x001fÐN©<Û"ÿ</p><p>#×ÄãêÜ%\x0018 »\x0016ÎGîCÄn! ýF±{&ÚÈpôd\x0005¡Yµ.:ªtøç\x001d%÷D.´æ\x0006ß°\x0019úAGm<´KÎÜ\x0013¹ÁÁ«\x0018ÔÄ-#ãíè'0_¼NG\x0002úÞ¤o4C¤Ý÷d-Ù;<_¼Nb@§£!r¨lâí¨¼´Mb?X\x001bG?ûý#:CAè3oõ6EÒMÍtä\x0017Þý_O\x001f>¼V$µÂ</p><p>Þ%ßç|ûAã4K^:¥ÞßX$+ú9Ir²º3)®-kþ ¹ÈN'5JûjQªn_Ù7ä</p><p>È\x0001(Ujó.%9F,Ê^üs\x0002w\x0000ÎIµjÈLäSr\x001dþxco«\x00072<W\x0015\x0019Æ-F+ 3oFM\x0017ïÕ\x001btø¥>ûÉ\x001br\x0006ä:M\x001bi	ÇO»F\x0003cÑ\x001b9»ûºQÎîg­ýdÄm¤vÐ\x001f?></p>
  
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

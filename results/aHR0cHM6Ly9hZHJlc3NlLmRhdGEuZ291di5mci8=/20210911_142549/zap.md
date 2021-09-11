
# ZAP Scanning Report

Generated on Sat, 11 Sep 2021 14:19:56


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
| Source Code Disclosure - Perl | Medium | 3 | 
| Source Code Disclosure - PHP | Medium | 9 | 
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-10.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-10.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#tb37E`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-16.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-16.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#jDrXL`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#tb37E</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=?î|C@=/§ÁÉtô8í\x00195äÿvïÈõÕõåÎïØ?|±|C¾¿½yþ\x001dôóóã§\x001d|à-q:Êr\x0003\x000e¾\x001aümýÐóñýéÉõßA5__¾ÞÂè7?È¸9{SñÀm2<zmSUfØçTýrù>ÝHF*ö\x0007¯ÅÍàµ©h\x0014FSàP\x0003;|Í-éJô\x0012lïWµ%md£f©Í\x0000W[6®øÔÉí9x®Äsx¦+9J]\x0006¹u\x0018ô\x0008÷^k»çÐíþ¬±d­¢³´4à*%öÄÆGÚ®\x0013la³U´û´9Á=\x0015Qåºná\x000c\x0019¦\x001cKÀs¸ðëª>¥j§\¬YöRê>¥n§4\x001f\x001ar£èøí
rÖQ\x0014¾ÿxxQå¼¿}7w¼\x0004WQsg_\x0000FO}Ú÷\x0011\x0006ãôß^Ãs»«É%ôÐ³W¾ßi	À7åö (iêçÄé\x0018·Ç\x0011¢%ðý\x000e#à}¿7è\x0005õ\x0006å¹«w7SC0\x000eÇ=¥´×òñ8½²V¢nyàé«g'½8Lú¨Ý¿vöÇ§ç\x000fêFðºL·Æ¥dC\x0019Äl\x0001ìîö»»nf­Ö¤h³OSêqCA>\x00042i<¿dg§?\\x0014lÇ¸yó²³£¶±²¾hú¡ð-@tp\x0003îÖ\x001fGÙ\Ø{ÛÍaómÊzÇhE²á&`+:²S@np	Î/_|Ý\x0002Pº\x0015PÑ°=\x00044X<Ð\x0001ÊÔ)ô -\x00004% ù\x000bJÐ¶\x0015PÇT>\x0008ðævñ\x0016\x0000¤G\x0000è¨ju\x0001 +\x0001Ý_HàA\x0015Ú8ýÚøûÛÕåúóÿÞuuì\x0016aàÏbq\x0008Ü\ø\x001b¸ts-Oßc¬ï/NOVÇoNÆ4^Á£J\x001eÕÀ#ÒPLPw¢³ô:$Ê\a*È¡Ã¤K&ÝÀ\x0014R\x000c\x0000\x0014Öµ%1¥Y
²kõÍdJ&ÓÀÔgwLÆ¦Å\x0010ÈJf$nÛ³\ÉäZÎRêÖ\x0002&ëÓÊî8ñ·3zþyò%ÎäMÅ¢\x000cêIe1ÉùH¡D
Mbâã\x0014üçO\x0012zÀäåüO\x0017K¦Ø &GP÷é¤"1ñ\x0011Ogç«lËfu?LE³\x0011éö¹´\x0014²Ó\x0008|ù|ûå\x0013Uì-ýP°`ø¼xøòe'\x0018\x0006Ü¼KÚ\x0013?iRUjÌ©,²`÷¼¸x7ZðZ\x0000\x0012Ð´\x0002Zj\x0011±I12 àsYï¥|¶ä³­|N§î+àóÝ`ë/(þ´ÎË=\x0003\x001eJAçJ:×JgäQ¤¯+.\x00136Û(<·Xx¾ÄóÍ\x001f7\x001c\x0005ú¸.¤¥ø÷t\x000cÈ£À\x0017\x0000\x00120´\x0002b¸\\x0013`÷XuÚòñsrß×Ý\x000b\x0018KÀØüÙ*ë$È\x0000ÃB>Ê<°~\x0011-`6ÆØÍåI÷zÅðWÃv\x0007 î!\x001c`\x0016µ\x0006lVF²µ+¢¡[¢³
\zI¤ª\x0000U+ î £CA\x001bR1BÒûï¼^LXéhÙ¬¤H$\x0012¡c@\x0001>"²RÒ²YKku\x0014²æ[bTþÄÞ,\x0005¬ô´lRÔxMBÀ)8\x001d!6ÈøtMÍß8,¾ÈªÍº\x001a\x0014\x0008Pñ'¦6cäs%XijÙ¤ªQÚgë\x000fcWþ	¿n\x0008£Zªªe¥ªe³®{,è\x0014ò\x001egOU-½ÇªRÖªYY«xäI2\x0015ÁÁ"¥êPZ-\x0005¬tµjÒÕ\x0008è³w\x0016pà`D/lþÈK\x0001u\x0005¨[\x0001qM\x0001I0¤9j(VÃ0RÖ\x0002ÀJU«&U
ÿø \x0005\x001büQjþÆ¸\x001fc\x0013Kï±ªTµjRÕ\x0000èÁÃµ\x0004h-\x0007ÂìÄÉ¥oªTµjUÕ^¦"=à\x0003º±cøN³çk\x0016kBUiBÕª	-¸$Ý\x00161§°ÛGu&\x0003\x0006µø5V"TMÐár\x0007r'\x000e÷#Ñ'\x000efÇKì?[ªªuuKtã-\x0001{%bm£ëFµÔú\x0003gP\x000c½Öbé=ÖÕ5Ñ×\x0004\x0008l\x0002\x0016¾¢ÎÆè¬I\x0015GÒ\x001bEõ¶\x000b\x0008+A7\x0019\x000cH(©\x0019\x0019\x0008qú¯N2åàð\x0000_¹º(ºñ¢x\x001coÕµt;#OS6ºL.ºÅ2¬nn¼)^FÅy\x0015j'&B'è+»\x0010:ÈR-òñª \x001e\x0000\x00196¢[÷ÈV¡Yls-¼Ð×\x0019!µU%»!(zE6\x000eåÒ/-Ý\x0016¨\x0001ê7ñ¸(Ó\x0004Ï\x001ff¶ÞQ¦\x0017/TEÛËóêÝÓúãî\x0018&\x0010x2_±Â!E0@lJ÷\x001e¾wuüj\x0002*±T\x0003\x0016ö&Ï	_fÜwe5\x00194Võ}»&,]bé\x0006,ëR¡<\x0016ZÄ#Á9 \x001c\x0017\x0014R-À2%¥\x0004ö ÆVÈ\x000e @ZÑÆq¬áH%3ÙÉ6
Ì¨täqJ\x0008$)\x000eÛÛØ'$åJ*× )eÓL7'îò/\x001dVT¤Û\x000cW\x0006ÎÃò%o9W3	å\x0007\x0014Ó>à^¬XbÅ\x0006,/R5\x0011`¡UL·0g8ìV¯\x0005KÖ:«EiÁ{DXZc{R¥9¶gM?(ÐUxÙrä¦l¿ôpÎ\x001ci\x0007íépYmpUK¶®\x0010S\x000f\x0017pÿÊkcY^2ú\x0005\Õé
ÇKIÍéFgºÁ6\x001dç$ÿUl¡RÕáR
K)Ú\x0010âÀ¨õøn'\x0015AgÞÈ8ç*
Ý+@W¡®k~ñøüõÏÿ
G\x000bÐÓOá&\x0001×2þpÄÒ$\x001biLP\x0015%XÜüâòú\x001f'ãÅÍ\x0005¥*)U;¥	"U{CÊLFjwÆ #\x0012Ñ´#ZééÍ\x0014.\x0004Ht¶r¸¶©
Ò®\x001dÒa_yúÚ\x000ennè áÚP&\x0008_+µÒ~Æt*\x0019DwÓ4i&@ÚC@\x00122Ì\x0010ePdQ
\x001b#\x0019ºJ\x0006rºU\x00078±3$é}*!\x0007IÕdHR\x001a\x0006ÈãbÊ"÷§·º&azáÓ¨H¥fL%ó\x0017vÉå	={ÓËó´Þ?Þ<ßÞí¼Þ<JÅ	ïã\x0011ÝnOZ\x0012\x000eÃ g¸:yqyr}:VË[À©\x0012NµÂÁ-qI÷x¬%'
Iã"\x0011Ï\x000fæ\x000c¦ãé\x0012O7â9Ö	\x000f§"¸tUD ­ãìpÚj:)ñL³ô$O:éEú¶ÑÙ,½x®Äs­xØ\x0006\x001céä\x0005²jÐE\x000c'\x0017âù\x0012Ï7âE\*KÊÚc\x001d	ÒYÁÂ³¡ïi´Ò.´
\x000fç§ñµí,NxeçÍ`\x0018~:],éb«ì|HÍ´Øÿ&ð\x0010vÂsõ·ªÉxj\x000eUYÆÄë4î¾àké³äFâÅ\x001d\x000c4Mç«ur£RV¸Ø)h²¹dJ7+4\x001aH|Î/Ä«´²lUËh­²b1\x00113÷ø°ÖÄç\x0016~ÞJ±ÈVÍ\x0012ðÙ ÏÅÚéóbÛ9ñÉá¢é|ÕÝ­7\x0018Awù\x0015Ò|:\x0018>~*îæ\x001b©\x000bý,x¨²àÓÎ\x0016ÓzÝÙÓßpÞ\x0008V|v8qÑpw«PqèÜ§É\x0010g5kz= Ø\x0006N§cËÅøÁ<ß~Léz\x001e(\x0016YN*]¯Înßß<>ýùïIÈY4\x0019 ª¬*æ¢\x0011Y\x001b¥Ç«³Ó\x0017'Wc1GFT%¢jG §E
Ä\x0004øÖÊ½u®ÌÕ½!Ä½Ô%¥þ«RÚÒÎ Ô\P¸ß\x0012¦Ýçö\x0013\x0004:Êå®¤t3(UH;!Ó¡\x0014Æp\x000b\x0012½8,}IéçÈÒSÒ¥Ôt%âôÍY¡¤\x000c3(Ñ¾ö½¢0\x0019\x0014WÇöÂfAÆ\x00122ÎÄ	; =CÆ|*!7ÖX§*Å\x000cJç8Â%¤+Ñ"Ë\x001f|9e­Ðghté\ÿæ\x0000â!o¬4º£ÒI¹SÍvdÌ\\x0012-\x000f ISQ9*]cgxêkÐG/á¯mÅ~U¹óe6sÔ9<:T¸m\x000c^óôæd9ö\x000b±ä(ªÉÞé\x0007|¿O?ÿºþòå&Cÿðp·»Ö	w×§\x0012\x000eøï¤ñ1{Åm!Ô§oÞ\x001e¿{ÇcÑ_^M4%¤\x0001	\x0017ÚPw,\x000eÌ`HÃÝ±±çlÍt%¤ûJ2a$i©)JÒb`$·:tõ\x000b!KÏ:éòfJ\x0017Ór3È¸\x0000Ï¤qK\x0000ÙëÉ\x0018`\x001c¹Ú±\x0017î±¬àxóð|w{¿\x000b\x000cÝdG\x001a\~\x0019R´UÔ\x0010äû%c)_õæâúìô|\x000f*T\x000bò,,
¯J*qÂÖq*qj8EKTã:öâõx	`Öf0\x001dÒÌR\x0000³i\x0002\x001e\x0008«j\x0004³%m\x0001sÕÖX\x000fÀ°\x0015À+\x0013¦\x0012,4IÌe\x0006£ÄÈ«ã\x0015\x0006k^&\x0015FV\x0014åê×	di¿&ÌRóº\x000f*Ì.!«odËôJÓdpã°¥rbCYZ\x001c5X81¬º²ébâ<W:f²ÖÉæ+\x0002[ö5MEfZd&\x0004õãÀ#ª\x0010Efwê±½`ÕÅ-7\x0013Ü3
è\x001btB"óx¥:2/EXBæ*2×$2C\x001dZ8g
W¦&yË2[tþ}\x0005æ[ÀtLûáüÃë$\x0015û+\x0016Y\tü+]&[\x0019nÌ¢Ò[S	uÊññß
¯µÅ,¶Á3Z\x0004HD\x0006gËsQp?õÑD¦*5«ZÔ¬W2Íµ\x0005\x0005\x001cÔD½\x0011O\x001e®ÅJV\x001b\x0019-ÊÌk\x001asj¶[\x0001ÑYÍ\x000fRKn¦ª¬\x000c5ÙÌè\x001aÈÉÍ2RDv³D L\x0002|ÌEú_U*C5©\x000c+y"Òmmç©8\x0007n¦Xr\x0001Tu5Õä«Ù\x0015kªD6\x0002»²©¯]\x0018®Û7jÞËÔ¯¼uåÕóêõãÃÕûnEÆ¨è±i\x0003
\x001cýÀ6mðO	½w`³¼àõåÅ»ÕóÑe\x0019\x0005¨.Aõ,PE8\x001acc©.xË\x001d\x0010&Ôº4\x0012ÔÌ\x0001µrÑ:à~O@=\x001bãÊ?\x0004¨-Am;hð<°\x000eÎ¦vAPí#wlH{OïJP7\x0007Tê£(<®Ê$P­ø\x0012õÛÄfú\x0012ÔÏ\x0000µ¸\x0011l*¦ÛÆ ¹û\x001dl*u\x0010ÎPr9hÉÓ³¬\x00025\x0006ÂE·»\x0007dµÆ\x00124¶úh¸rB«\x0010ùìÁÅM'ÔE#+ÇÚ8\x000bo­W;6Y¢Æ*¶
\x0005.|í¨Çx\x000fIÔ
×µ^¥2\x001b®\x0013þÐ~\x0000Àä7éÁØÎ'5Ò\x0001ðb\x0019¯R½JÃ¢¿Y?¿Ç)«ËõýÛ\x001dX²\x001c\x0003Ýzi\x0004×ã	Ô©)ª«©?þ7Ç×Ý\x001cÍÕåñùËÓ)x¦Ä3mxZrÁÔ¸H2Õy\x001bÁtºçr¶ÓÙÎ¶
Ïs½7.è¶,<N(Ó«ZhÇs%k\x0014\x001eö§!ÊÑ¤¡ÉS.¤ë=æíx¾Äó­ÒG§\x0017òÉ[\x0008\x0017J¸Ð\x0006g\x001dm÷u\x0012çÁPs\x001b\x0017T0\x0013e\zòb\x0017\x001b?­à2hn¡Dº\x0017|ðdXøe\x000e\x001b¡Ó§MÚJ\x000bx¨Uèäqf¥]ªTdumeã½Õ67'á\x0010a|,c5%Ó¥´Kùª!\x001boQ¦táÖ\x0015¤Ç¥xVÙJ¯Þº~(GÄáü»§§\x001d5ÜÎÀI½ÉI\x000036-ÔQG*Æóz¸V«vruµ³»Z½AªÐàÚ\x0003júÈ¦¼V\x001cÝ2Á\x000fÏ\x0005iAÔ%¢n\x0016"V!\x0007F
|\x0010\x0005;0²\x001fhJDÓ,Eë10\x0011Î!å\x0015àÑ#Dø0Ü$ÝhKDÛ.EEíÑ\x001aÛ4\x001dÅ Y ~\x0016#º\x0012Ñ5KÑðL;\x000bLÎ)ääGGÀ´ ú\x0012Ñ7#b'%¯?äëb²3\x001dF>¶ \x00121´":Aë§0ù ÒòG¼ç\x001c®sfù%alÿÎ \x0014\x001cE\x0008g÷Yö£cíE&ÚÖ+§
QS©[õ
ÒÏG1å:GÖoKóãb|ä²\x0003	\x0012UT·ÍÞýð\x0004\x0016ÄJ-Êf½\x0008ý:í\x00140D[?%¨E\x001c\x001eøÓX©EÙ®\x0017EL-ô\x0006'ÍRzS;Îë{ÌZ,E¬tlV:\x0016ÀÒëbp%
Â];Äh\x001b6\x0018+¥#Ûµ$FC%}hÇ_Z÷ãÊ3\x0010+­#Õ\x000e6Q"O¦:ÁQ°©ãM¿s¼QUwZµ\x001b!'¨òh`t3\x0007^.¶\x0018Um16\x000e|Ð sMVNºËNbX|\x001cUe2ªf\x0011\x001fAII+¥Ùf\x0004c\x0012}\ÌX)GÕ®\x001cÄÒ$ÇqÅÄHãW\x0002ºÖ\x0019+í¨µ#^ëÔ+k\x0014Xg\ÚïuÀ®±¥Õ¨ÍÆî[Óy\x000cðGþÔÄ\x0008>ôbÄJ«f
î0ÙLbLÝúI¼äcd\x0014U\x000ba¥\x001cU³rÄ:uêãjä´\x0007	9`\x001cÌò§ZWFn6Ê°Î2¥Ü\x000c.\x0004ë,\x0013cq±þÖþÖÍú\x001bÅHú[+sä
\x001b<,F?2t½±ÒßºY\x0003ÛQº.¸HÈ\x0011¢¦\x0014pPfdPV\x000bbíñ·«ïM
«-\x001d©ÆÈc\x0008q±ÚÑÚÑÍjGÛ@S¬Ô\x0012÷8 £t4578±ÜäÑÞÑíz'í Kfc³ÌrQUÔý
9¾`Õ×ùåì¶é.aL\x0002®-H)Ut	ÉkuZÌ¿Ûà÷\x0013à^VÅ	oÖ_Vß¯ïî\x001ev\x0007CAé¤\x001d1\x0014I\x000e¼PAû0<ãzõæøÝêûã³³]95¢T%¥A\x00194\x0007¼­µG\x0007Üþ¤:\x0004¥.)õ_U¦¤4UYÚÒþUeéJJ÷W¥/)ý\x000cJëH\x0011I\x001b\x000cu÷\x000bã8\x0013hFËZ(cI\x0019ç|qÇÃÆÈe\&g\x0004ÍhaG\x0003¥¬õå\x001c\x0019
&¢;Lå85hyí[\x001a³0U¥Ô\x000c]¤¢;¢=hVZ\x001eÝ¦\x00039Ý\x0016þÊ±²s¬É£G\x001fz#ÉÞÞ<~¸Ý=\x000e¨3~5W»+v$È$r\º\x001a\x0019Zôöäòåéîy@Ì©JN5\x0013#§\x0014Ä7à<Föjs$ÈNkÀÔ%¦þëÓö¯ËéJN7Sù
§¥¡ÚQÀA!ì\x0012_ÎéKN?\x0013cæäÀæä\x0003p\x000eë¤6ÎPr\x0019Æ[öÀMÃ1))¸/8ª!âðCÔÆ\x0019KÎ8G8?Ä\x0019óñ\x0014&ïÞ\x0007¸î²ºFrÆ=
8Ö%}w+d8ê¦Ò\x0007p(\x0013g°B,âtýöB'j\x000fãlý¯ÛÇ\x001d¯t\x0007m\x000b\x000b:4Õ2(¬ÏMu4à	\x000f#^¯Î¿¿8½Ü§K<Ý\x0007¦%Í+38q§$R\x001e*û±Ç|*-ñl#á\x0011Û\x0002ïöGYc\x001f3/§âù\x0012Ï7âa«&á9A;%­^FÇÑÒæ©t±¤t±s¹ÓÑ¨¼;<\x001eØl0µTx?®kñ­\x001bå\x0007ª\x00198Â\x0000©\x000f\x001cNcÕö{	EßB\x0013Æ­Ëß<Üü²zùóú×»ÝÍË\x00118yTþf\x0002½Ñc#è¹}ùóWïV/¿=~{r¶«ÍQUªf¡â\x001e\x0011BõþÈÓT»?¢\x000eBªKR=O¨6ï\x0011Ä1$Ó<î¡ïÜÎ%µ%©Gªéé\x0016
BÕ?¿ëÝ¢VTÑ_C Ò\x001aM}\x0007
|~Ü5ZT`­\x001cÍùÀÆAÑô\x0019·U\x001cÔ.Þö-þñúrWh°¿@¤Å\x0004í Ú³g\x0016q\x001aM\x001cò¼Ìõ;\x0013T z\x000e¨Êë8£´¤AÅfõ±°\x0007á\x000c%g%ÐÀ\x001e9¶Wñp$\x001eÐ\x000b×)MX\x0006ÚwwÅ»{ò´¾ÿ´\x0013RàpðîÊ[¬\x001b´ímôàíH\x00050\\x001d¿\x0000¨J@Õ
\x0008R\x0014]Çj°+¹óÐ-\x0014|\x001c±\x001a\x0000u	¨\x0001-\x001bàEn\x0006\x0010dJ\x0006¯íp|¨Ï|¦Ï`G'@é°Ò/ñÑjÓàÝHÃO\x0003 +\x0001]3`¤áËVãJD\x0012 \x0015ù\x0008êQ÷k"`Q¸´íÔL Ä	¸ôA5ró+åká\x0001r³ïÒýu7Zô.ñåÃý\x001f\x0013X+Ruv!TçÇ1\x0001Ì:]\x0017ç?ìqº\x0018Sj\x0006¦-HßHnåÜà\x001c¶tâ<LSb9¸Ñ*i\x001der(È	
\x0005\x0005/ôè@ð\x0006NWrº\x00198ÊÁv\x0013Ì`Ä³vôò\x0010Ý~<\x0005ÍØ´8?ÁxÒÁ1\x0001\x0017Çïx\x0003g,9ã\x000cN\x0010\x001d\x0016\x001awòÔ¹ 7:¢\x0007ß¯9Å¹©ín»\x0003\x001a,\x0015âÀ³è¸h6|@û\x000bvæÖj©Y/u\x0006¢àÅ\x0006\x0017KKyý\x0008/Sh\x0000­n¼l¾òÝm\x001ax-f|¦WÈ\x0013gPê\x0010\x0002µ\x0015§Ãii\x000f\x0015pæ.!x¡ÈÞ\x0008rü1À)|ß¨ôåPÝçÕËçÇõ¿]EI8©@\x0015\x001e#VJ\x0006\x0013\x0007azµv4ïzõòúäòxçdbß·(}9Ow\x001aò\Âf\x0001T\x0004äå8ÚkâR<]âéV<ÃÝÄ&Dª°\x00031r¡¢ÒÓ+§Ð	Ù\x0013\x001eöþrËÆa<xAl&b\x000bvògDÞ\x001aì\x0007[Föõ\x000b3.±ôt,	^µOms\x0011>-û­Zå¥[eJ,Ó&-Â
`LHËÒÊ\x0001ª¡â´©T¶¤²-ÂrtøeLí IXTÖ\x0007ÂêoÎjÂr%kÁ2´ø\x001e\x0003;©l^V,\x0008ËT¾Jr§¼ÄÙe8WíÕ"a\x0012+4¬<¯\az%úÞ¼ò­\x0017µ
+X±EZÚC£ñ\x001baÑf'ë·vÅµP\x0015=F@µé1r´$YòJ`\x00118i--xSw\x0018Ü3=KV\r¸°¤(ôÅå\x0006[\x0004§bU:^¶(ùèéíî¶r\x000b>\4®ß\x0006¥\x0017hSYé-Ù¢¸þ¯«Ò\x0010²EEn­F:]¼\x001a\x000e¸\x0014ßÅáí3ïbUïÙÝÇM½ç\x0014¡qi/èÕSë\x0012w¬W\x0007öÒõ\x0007¼4àu3º\x0019ÇÏ~º»Ý³Ù¬^q\x0012£°Îo\x001f4Äºù³¯ÏNwn;îÏ{\x0015iÞk+¢\x0015Tí\x0017qTb[CÍÊ
éLhJB3Pr\x001e,n!HBÌÑp­ÆæÆ3âH1ì§Ùe\x0019º\x0003åçO7{¼\x0015\x000cò¤,¼é\Ön>77\x0007\x00197²¦î\x000cÜo.®_ï©\x0005ý±¾²\x000cKMÄBÄÀûÁr\x0015"/\x0007\x001b.¦i\x0003Ô% n\x0007ô.ò\x00060Dw@@S\x0002f@v\x000f;Ú4d¨úçcâ¦¡å¶d´ín#DcÙBqÂ©|\x0014\x0007c;m®tíÑRµ)@\x001aV9§r\x0003¤<À×ö%¤oÄQ\x001bùR+\x001e\x0005â"½zÆá(n\x001bd(!C»$Ékë´ÍÊó½6z0ï1\x0011Ò»zÇª¨¼Þ­\x0015ýf¿9¸¯*=} Èl°rx\x0000éñ\x0004"U\x0012©©DØ¥\x001bh?}\x000cyIpö¢\x0010ÃÓ§ é\x0012IO\x0016RàÌ\x001fN{ãE\x001eÚS®ÀZÑwì\x001bLd&K	8\x0002/·y	¼å
	\x001bFæ\x0000OA²%¤'\x0013¥[\x0008ôæñ×ÖD7ÿ(¹ÈM&Â¹\x001dÉ®s:Ï\x001f³XDìï&«)xÝë,âi\x000f¾\x0019Ïò¸\x0008\x000e¹¡BOø|3¥l?gë\x000c\x001en2¹Z?ßî*i!KNÄl¬lÉ©l¬¤\x001epÉÕñõéÎ\x0016ÆÔ%¦\x0016wð Z²ÚyK\x0008n\x001c?7a\x0012ÓÌÁÔ)JÞEXÖÙ\x001cQ\x001aÉ:4QÚÒÎ T*\x0017\x0007aIªåä\x0008{µj$+ÖDéJJ·LvH\x0013D9ìd0a(	Ã\x001c9rWVLûVR\x0011æèÀÑ4\x0005Q^B\x0004~èÝõ/ëO7«o\x001f\x001enî¿ÜîÖ<\x0002+/È×uã\x0017uOpkj!b%ÐñëÕ·\x0017W'çïNwêFB´%¢mBÄ".\x0011gO2 yÜe\x0014cÌ¤[LèJB×L\x0018ô\x0011Ç®sß*Ü\x001b\x000eô«ÞWCèKBß.CÃ»\x0005#\\x001a\x001aüýË,Ã\x0003 Æ\x00121¶##Êè®\x0008>åy²ªW½!\x00133\x0008e}WÚ.KW0\x001byiÔ2h'ò\x0016\x000b.ïÇ5¼(ï3o\x001e»ùc§ÆVç"D­1íëËAøûÌÇN~ØU'ëûQ\x0003ß½Õ­?4fWRñaÆÓf>²\x001f\x0000Ùù\x001e¹R<î\x0012\x001cÇ\x001cþsÜWÙ¯\él±½a+FÓ%nEÃIã,;Ñlà¸©ì\x000fè¸\x001cõëg\x0015£ÌîÇd<í±"¥\x0016
6ú¦¾S½\x0002ýf<[âÙfémÒfð.\x001bªP°\x001fþX¥©tªuïuþ|{óü;VçÞ=<ï¼\x001b8d\x0018'tm\x0018±ÛN\x001c1\x00165×pÃ÷§'×ÇúÜ³ë8ôc¡.Ã;üæÏ?­o\x001fo÷X7¼ºÛHm)\x000c­¸é¼Û\2jÞ¼9¹:>½<@jJÒ¾Í=\x0014»Pi÷¦îþØnÖêî¤*åAÊú¾º võn}{ÿô\x001f¯\x001evgF$øÐfolCN{Lq6\x0010-Ï6ý\x001a
è»ãÓó«Õ«Ý)\x0012ÛÏ?XQ\x000e3úðü¯ÛO÷_w\x001b\x0004\x0016cFÅ©\x000cx£ó&uÀñ¼¸þþôõù?v|uÕ7lU¿|üõãúþ\x0013þûúùãíÃÎe'`ÉÒ
>ËëLy«²ýÕMEYÒëËãó×øïÇ×¯N/Í'ú\x001e4
¢æ)2/ànÌÙzõòñáö÷öÅÃíî!2iMÿ\x0008]ÿn\x000cê\x000cp\x000ejï\x001aÎãËËÓ¿w/.NßÑÓ1\x001fù×ÃÓ?5	°j\x000cyFýóùWüÃå\x0003~^+\x0012\x0001 þü÷Ýí}'3©´i\x0012zÐ88­óþ¤\x0013ZuRÀc\x001a¾99;=/ú\x0003®Qý¼y¸¼øÇß><|þü\x000cSú÷mBø»¨yÁ§"\x0016$\x000cØ\x001eÜK4±q)!\x001cc=PÂûÜy-puÓ\x0000LOLªg\x000c-\x00021óDè$:¤\x0008áàé>²7,ÂH>þRB¸^v\x00089
"\x0004i
DhR\x000b\x0008ÈÐÒÞ×Y\x001f~	Oï+!©@Ü tÿtó´\x000c_»Ö\x0005xöpæe:~J1åÞ\x000f"#õw½zsq~urµ(}Õ\x0016"CCÆ(­\x0012Ý\x001ey\x0006¢\x0005sàk\x0002Ò8§xº.ötAS&\x0006ì2	ÁÙ\x000cm@S R2%°:¥¦\x0012\x0013T©1\x0008k\x0019ÃOÃ{\x0011É¦\x001e'@\x001262	íH·?ÿ|{ÿ8ô\x0002`)ïíûÛ®=l
ã½]çUPÒuÓàu×¸Â\x0019Z^\x0018ÖþXÈ{úâôäòÝ~²æF\x0006G)
Ö\x000b
\x0017Út¦T²ß5\x0018qX§¶õ\x0014þD08âÀ¢M\x0005 3©:\x001fÈxÕN3Ù½}xï¹1Ôn\x0000pçñêWtÒðB%GÂgL±=Ðð¼Ð¤>^`¤\x0000ÜØñ**½9Ht»AÒ³-11DÞ'»\x0011|TÒ×k!2:­\\x0004·\x0000ã¥/\x0017tª	\x0007"|m\x0010U|\x0012¤T\x001e~5ËÆeÄÃ^æ\x0012Uª|\x0012v8K!É\x0008\Ò$"%Ù\x001aÄ½%@*öÑ\x001cÛVÒK¬O\x001fÍ*"ÒzHoN&ê©òIH.\x001c)BÂ\x0015vÉ
.¥©\x0001IREÛ\$ø«eÓAÒ RAP\x001e·évRòR*:H8px\x0011\x0012"Ùt\x0000É¥\x0011¸n8\x0011E&ÒË.\x001b.[UMß
g¼c\x0018
ÀÞ\x000c8d\x0000¼N[ç4¼ÐfÈ*\x0004WC5©m3`\Bg7EUpX5=¿BeDðW«&%©áÍHû8ÈXºo@d\x0019I,ºnØ\x0000ªÚÎv·¦¦{p±\x0006\x0018§làª\x0006aÓ A
'jÎIÒÿ¼×ÿú4h9uÖÜãÃó>=3):% \x0002h;¥óÍ}([V@gÐ\x0001ã\x000e¶¿­¹ýµ`;ÃBÛçÇO»h\x0008d0iøS¥
ÜAëHQF'+1aíõåëàLE\x001eÿi\x0014:\x0005ßp=¦Hë­ÂÄÈ\x0014µ\x001f×B\x001eüi\x0014¬\x000eA\x0016>
\x0007B
§Â¹\x0014éD\x0001\x0002è:¶"b{dGáe\x0016E\x0013ÃþçðÏ\x0011úôËõãÇ]+\x0018ó>
V	\x0016\x0017\x0002%7Í\x001bÖ­j¯Fb\x0000`·¾{w|ùjÌn-Àz\x0011©`4i
À\x0014U#Xê@0k\x0017%Ã£L§­\x0002ÁzÐDª¿46*Í${¼7â\x0019ùoïÖ÷\x001f~¾Ùft\x0014in)}Í.
\x0010<%óQh#úçÝêíÙñùËoOÆÐþø5þüÕ ½¼{øx»\x0013,¤}K\x0019hr©\x0004\x0005\x001aÌ\x0018×Ë³W§\x0013¨¶\x000fÙ\x0014*ª«ÑÑU¸¬»£¢	8èèÊy\\x001fÔ/<ø!§íûÛ\x001b,\x0019ùéáþãn\x001f@¦É\x0013\x0001-\x0010æø\x0010)4\x0017­\x001b~p¿?=Á\x0011%´\x001f­ç½ME3"-þ\x0000÷\x0004ë1ÉöVl¸hÂ\x0001Øz~ÜT6åR±7- \x0017Õ±ÈÚÕX\x0005Ml=n*©\x001f\x0015¿ä\x0010\x0001öí³æ\x0017Ã®o\x0013[µ6³áì\x000b~\x001a%}PëXhñ\x0000\x001f´çãM\x0003Ó`¬u\x000e`\x0001\x0007J [Ì^\x0004[f9\x001b8ChX¤Éª¡zC`\x0013"\x0007Ñ¡\x0008g\x001bÛ':Up\x001d-
&\x0007\x001aï\x001dÊÆ\x001eqkàP¹µk7Ý5&3\x0019>kê×F¸%ç8ì-íúMc Ö,9GÓY¿éhG\x0013\x001c\x0008_¶+83§4ÙóÚ\x001cÑu°"11å×a+Ò0Íc:¯#ã£\x001bùÎzÄ.W¾[1pRÚ´5&½ZÉ\x0011òÂò3\x00078q[Ñl¸SIÌ\x0016RTD)ïóºü®nùØ\x0013á@Õ¦9>xâhá¹ôÚi6EÆ"¶MpðEÕ¯ëL4½÷Î¦Ñ(`T3Ý!$çÿV-{\x0008g0h"\x000b C÷®F\x0011\x0015e~1\x001cîOÒíg\x000eCÿ©*\x0002à Ç+Æ£|¡±â\x0000p (uûû`qô£L\x001dÐ¤3\x0007ZÎQîÐI?\x0017nýåñöÃmaþ¦®Ö®8gõfýøt{¿Ó{Ç9¤Tv\x0000¾\x0016½\^æ*«ËZZS]ÎãË«ÓóýXÉºlÄÂÎFz²\x0002G6¼\x0008\x001c_ÑuÜi\x000eVJ\x001a4b9}B\x001d Ë8ÔágÃ×ù,ÀJfe+V8¢o}"É\x0010÷T\x000fXªfÎÀb«­Ëp
AÁ;\x001fè3ò4!Ú¥\d\x00135ryÅòÒ
_ª$¯M©M\ú\x0019ÙähäÂ=ô¦Æô!MÈUJnémds£\x0015,lÊ§l¯
`6º\>µøÁß@6ü(6Î¶­\x000fvó)õ,0÷ÁÞßÞ\x001c\­ïïóô°Q6g$©V)@oèdÛ\x001a®9Ã$äh0æêøü<\x000fÛ·\x001d½ûç»\x001emÀÓÊ¹\x001cÜ
CxÂÖ\x001e4àm±&â\x0019ª\x0001O¤ÑòÒiA\x0007¼*£%\x001b
t½J®ét8éµ»©"zÉ	\x0000\x000c×\x0010Õ\x0010^z£æ|[{d\x0008\x000ft°¶ôm%}Û`Æ#ºûð¾~}úú*CÏ	íøñ#Î\x0012ß	\x0016pèc÷"\x0008ðìÒn|\x0011H(/z¾èu:¾|CÄ'0Q­)Ú\x0006\x0007á|N`\x0004C>¨²±ç63Q\x000ck:\x0013x#âÞXõÓ]~R¥ÖO­Ä\x001c)ýr÷õñaàË¡ýº»\x001e(`\x001c\x0013)ÐMy·èsLÍ\x000f!¡ýÇh-PAD±Û\x0006"0uÈ\x0013æßp\x0003£f\x0011\x000eLÇñJd·\x0012ü¤À'òä¹©á½èùîËý¯qDÏÿðç¿\x001f\x001fv\x001e#ï
¦&ºê\x0008Î[w¢ÈÕ	£:êË	LÛÊ}?SP´ö=tV~z²}\x000c\mÍxNg\x0017Ö'ûå·_~Û:Ý«×ë»»õýÇNiîäÂ T6\x0011,.øJX\x0014_Ä¿b@\x000b¬^\x001f\x001d¿B¹«<ã¹"|8Aõ\x001c±³§1\x0005³º	ÌÈ×\x0006V*Íé\x0002³Â\x0001 1Mz3I.Ybõ\x0003FF0éÉàYS\x0005êb5\x001eÁ¥`¥Jþ)qg{$E¡}Ï\x0007f¾ê/ë\x000fCé9,òø¼~\?ßí¬>16Rx0g¨ÏMzcÓ¸\x0006-A»
Ç°Ì\x0003TØñõÙXGÁÖËÏMcÃ¼xJ\x001dz¶æ\x0003Vï©E1^á0l\x0013[/?7Unp\x0007\Ll\x0000c)^\x0017È?ÆáØz\x0013[/\x00076ÍÅ4ß\x0008¿)'½\x0015&Ë-\x001c
tÁ\x0016]j·Âo\x001f\x0001ËRv8x½l½þôËúqðb¤ný¸3\x0003~.ab3	¥[»\x0014~µÃqº7\x0018¦\x0003ók?U_^\x0013¨¢¤\x0006èOv\x001a\x0018ÔÕÏR¿\x0008Eõ-T½á$*Å¥ëÚxÃ¥þA¤µPØ"äS7©¶²qÓ°<GÐMô,,P²°ÔBYmeº&\x001d,ÜÏGPóSJÚk*ôÇ¸ðÂFl<Y\x001a\x000cT\x001c2å5¸xÜ\x000c©HE8ðbk|÷`}øY_í`ô\x0004lé»n\x001e\x001f×»ôU¼w3è\x0000ª"½\x0011\x000e\x0017õ0f$A}öÍÉååñhË­ß\x00191Í\x0008Åmf\x001e|Xü
ó\x0016¤#´#¾u\x000bZ?01\x0011
w@¦pÃ¡ØÄfÉï·*ùý{Ùü×î?Õ·7Ï«W·OÝ¸³Û/7ëçßwfh¼¦$¹rf<ãD\x0007®\x0001\x0002s±
é\¯^^ucâÎ.Nß\x001c_ÿ}´n°à£:Î¿\x0016ßÓcxr\x0007¯ÄÕÅãç=t ce²ÐÀm\x0017,
K»¸°\x0015×\x0006Ä..ßtlÃ_¶ Ûn\x0015Bæ8\x0006«|à\x0000È\x0014¥\x001fL°r\x001eÙW¿~¾}?èýNM\x000bâP	ê¸\x0004Ç7­\x0014Ç\x0011ãÞN\x001dü"Ù{ûõ·/v8Hü¼zñxóÜ­\x001fØ\x0011R	GT	¤cÚ.!sâ
v8:|½zqyr}z¶i«\x0017y\x0002S\x000e
ÃÓ¤Ó
\x0011
Tò`\x001ciûNµÕ<ERúHg(\x0016\x0014·9â\x0012×L[-Çû|´¹\x0004<æè¾Óã=ÚuO¥Új3HEÅØ\x001bJ*eg}?ãÖòãç\x0001\x0007óËêÅúÓýÃÝÍÓî`æ\x000e\x0010­à°SÜ×EÃ-`q¸æÝêÅñëó³«±°OAV»SÉ0B@9Jk°/E¤
ßC\x0011\x0007=ß&²ºÀr*Ui÷/I¬±O©yÍ¥Â
úoMdµ;2\x000c;3HÌw\x000f%Ø\x0016Tø	fcù1å\x001fw\x001f~ûÏ\x0008õ&_[z\x0002®m\x0008©É×Z¦½ë)Ýª\x0005Q\x001d¡ÞO\x0013ª(ú
¦kÄl\x0016\x0012ÙHyyí½\FTç:&È\x0008ç\x000f\x0008úp8xNÒü\x0001êa×Î]\x0003Q\x0019¯D¤À¬I½\x0007 ÅuZ)#m´\x0014
FãB·\x0013}ü*ÿùÛçþW{^½~xþºÓÖÂÉ´\x0001ÜGaÒIéb0äÕ
S«u\x001a[úúâú\x001f£¦sASÈg\x0012Mà\x00110?%Fsº"?I=#à´m\x001f é0E\x000cs
R¹pÎÆÅH=sVõÛø&ÐÜ¼ÿãéÞm]/\x001c¨qÿ£¥nvT-îþIí>J*¢>\x000c'È*\x0016ý´kÙs|~S¥N®®Æbª\x0005Z\x0015\x001ef°
2å:ÁqÐ\x0014\x0006¥Î\x0015ËøBïeËîD
÷O÷óûÏÿ9h\x0019§­Î·ë*Üâ+Ü	kSP5¢¢åÇÓë¸ÑùôxT\x0017h\x0003-,\x0013ÑÒÜ\x000fk+,Q¡çµ\íhw_?üñ¯»\x0011©Mq\x0011³T l°ÔÈ
ïp :\x0018-­«ÒA\x001cFûòûïïïÿ5ìêÜ­Wï>"½ÝuÜÀô3\x000fÇ8í7\x0005#l8\x000fìÝKÐ¦§cW¡ëÒ©pà\x0018æÖ\x0002Åñ/·±²¼\x0018ñ\x0011÷ÓýþüÓoëÏ#\x001eÏÃóÿü»\x001bÝAuo¢íÂa¤ñ\x0005å×\x0000r¤Çõ\x001a;\x0019áÄÍ&\x0003;KO\x000fvä¼½]ÿëv_DB;êb\x0001'Z\x001cqK
×	\x0011F\x0013¸o¿?\x001d?mîù?}ð[vÖêÝúùîÃþü·é¤¡w~J»éîR{w|}örG\x0002«\x0000ªÞi@ð±(@n"VÚ&M+¢P\x0019j \x001a \x0005ªz\x0001&BIAh{(;JóiÉº¡©©ÊNb2¸¥(E¡»¹ú×<<ÜØ°©JN<MØ½à\x0012T\x0008iO\x001e\x0008ÊSQ­3½^êP¿þtóåN\x000eÅfnVo\x001f><í£JLÝ­Ãêô¼àV´aL]½½xyµ\x0003+>®{ú2àáLP\x0006O
)Ê#©ÆÆ£h\x0006\x001d=oÏ\x001föái½}ùîxä\x001füë×=c0°9Î ¼¨\x001bÅsë\x000fr úe'ÿÁ¿þctP@ÁWù\x0016>kÑ\x001c\x0003¯9\x0017*<7}à<¶Ù|î÷`~þ×¶6tÌ°Ã*\x0014öW¤Ö\x0000#rg¬
C
uÏ1+ªO:
	\x001dI\x001fÓ±mhòx\x001c\x001fÄÐT}ÅiHÂç=GauØã´é\x001e$¯Ãô:âËê»5ü\x0017wZª{ °XDòÎh\x001cµãLß\x001d_A
®íü\x0014.\x001cfX|z\x0018L\x0019JQY;^þ¹Lüñá§µê\x000bP_ï\x001f\x001f?î¼8XÂZÂb	h
\x001e9j\x0007Æ±xü\x000bPa8;âÕèE,è¶è©t`g¥\x0005\x0013\x001aSaÕÎ¾26ÑûùÌ¯îÓO#öà\x000f?ßÞï.ëÝúñ\x0014\x000eHGÜû£\x0001~d)\x0019¼üöô|4 ¸\x0001Û.9\x0002&tÚu\x000bzTÄ#Â»ÀK!z°F\x001d£Ýdw¸TlØ¯YýcOù½ï@º\¨\x000bø:uå÷z¬
CåiXùÃh\x0005müùéÃÝÇ\x0001\x0017\x000fp°öÄCª\x0014Pj\x000e,yÒ\x0015
\x001cÜA\x0017\x0017pÆpÞÀsqÓ\x000f/°=\x0010s³ë\x0015a\x0002o§²PÑÓ¡R6û?®£Q¡î#\x0017Ñ0w·!ë#©\x0012I5"y._W Dqtcä¨\x0003ÌÔ:[°\x001bJþøñI~ùôPÄ»sn§ÛHPäßNáØ?þzsÿ(\x0006ü@Bq
7cu\x0013\x0007ð!¥éà§"ÚS8ÍoOÎ¯6Yá4æ&M2îþ`\x001e~s÷7å\x0008Ò"Q½zþj§¡F\x0010CuãÔw&m»ÆÑÚ´èJÎ\x0006ÎÀjF\x0015ôÓN¬ÔöWÀÒ?Þ¾¿{ÏõH¢Ëç§nBv ó£ÿöÝÍý\x001fë§\x0014>Âùy!s¤\x0011\x0011C
ÃØ.|ôÝÉù\x000fà¹Ã?ûòúª\x001c]¹ðÕ?Ä²÷\x000fÿÔ´\
4¦\x001a²èlj
.õ¡Nýçãº'2\x00046?ÔË¤^=><ÿñuÇàðµ@'XåR\x001ape$}\x0018]\x0002m¯¿º¼¸þal¨ù\x0006L\x0012L\x00062\x0015;2¯È	Áóñr\x0011«À\\x000b\x0018ö§3äN\x0001L\x001b&KÊz6¯È|\x000b\x0019Ï#±\x0019\x001cKf0lÙ·\x0015Xl\x00003^ðõ\x0007U@\x001d»¡ÛPÈ\WIÖN¦Cñ¤\x001fê"b°\x0003\x001eoo\x001eGï£ÀNÝ\x000eL`uJ
¢YÍëYép\x0004¶)p\x0003+à\x0012\ýd¡$\x000bMd2âsVq;q4Nåm_Ö.AÐdÔÎf±\x0019·hÉeh®Bs
h\x0006s©Ý4g'±^¢ \x0008[çÌ¢\x000fZ\\x0002DMh`­\x0018^íiÐîÜToi\x0012x\x0015r	Õ5MlÉÞñþ\x0003ðó\x0015-±i!ï|°ú~¶\x001cµ.Ü IhXäf(ªEµn\x0011®Èt\x001b?¢Õ±:f¡Y^±bÓ±ùh¦B3mh24l\x0010$6Ã\x0003
.¨²\x0015mb£¯é"×)FlSJ`&ÚeB«4jÓ\x001c8ª&\x001dv¡%6Ò\x001cVECUOjy\x000b@f>µ\x0006¥5ÅOy\x0011I3\x0018ç³UZM5i5,UiÕ\x0010ZòP\x0016e[£º9³Ù´(Ùªá/ûå&L\x001aBç°#\x0002Ïp9ÈÚ¶Æ/®4®nÒ¸ÁÊÔéè¤2Í¶
\x000bH:4\x001dý"«+«t..3£
\x000edJJ-Fþ¤nÖÕÖÕMZ\x0017§£¦ML¶@n\x0002¼¦ËÄVi]Ý¤uCØ6«iRjÄî\x000e\x0012Åÿ©\x000bØ*­«´.\x0013K5yö'5\x0017Ü1Ø*Å«\x0014oð	Ì\x0019EEL >x¨1zÚÕ¾\x0002óM`B¦$-\x0008M\x0007\x001a\x0001º½\x0003¬ã]ÄV=	ºéI\x0008à\x001eÐúg·yâ õ\x0001R[t\x000fL¥uMÖÅ`¦ñùE rÖç\x0017aÑ'5j3mªÍTQ\x0008l¢ÛnÚ±Yö\x000fìFsÌg«ôiÓ\x001fÆ§z¾ô"\x0018bÓaó$,c«î¨i»£î\x0001¶Û&Å&#ë\g\x0017é\x000eS]\x0003Ót
º\x000cé5e¨.JÜ3Øi\x000f[]\x0003Ût
¼ËK\x0003­ð\x001ckÄÙ5¦ÔLã£ë§\x001f8ÝðúöîýÍãÓêüö\x0013;ð2¦NiÁÕ\x0011lÜä¼8øëJ¹]¬^½8¹¼Z¾\x0006ÒýpªSmpQÐZU¥¡á\x0011ó\x0004ç+'a\x0006.át\x001b§]\x0000g=» 7XrÞÁæJ6×Æfc;ä\x0014¶!¦\x0015wàQQÁIå\x0017Âù\x0012Î7
ÎbH²\x0013ãùÁ\x0011ÞPþªÑéep¡\x000bGN§j\\x001c|àTû\x0014-oºÆeñq\x0019\,áâ_\x000bNJF:Çß\x0015^0~Q­#¿Ù©®'z	]¥Jd.\x0017öË*Ì=§\x001bá¨k\x0013W\x0018p¦3mp`Ãèpù­"EG­ûHW¹Î3è*e"Û´Ô2b¸4ÐÌRñ|\x000fÉM·L
ËêÂÊ¶\x001b¹è\x0005\x0003ÇêàhH\x0004V\x0017,Ô&ª~À\x001aO\x000f\x000cçáGÂyarºsîÕÜt°ù¡ló9{~úºjFÐp)p \x0004d·²5}Uc9\x0001Ù¿\x0011]àõÕ·]GÍ^0[Ù\x00160°,S<Du\x001bPB\x00023´M\f¹\x0012ÌµÁáOÖ¯
Rä)iºÃÕ;ÀRÖzÊT¾JIÚZ	Ty_ô9£\x000eçß.\x0011W(ÁB¸°ÑFæ\x000c7\x0005ìáó)>`n¸öÅ\x0012,¶H\x000cíñ¤mqÐ Åw=\x0012ã4¶þ¥l\x0002+\x001eQ\x0000ãGtÈeuG«\x0012`I)©LµÅ.ÆÖáJbR³sÝVª%§¬x=Ì´|M!(q`©\x0015=âþó\x000c¶D[ÈJ[È\x0016u¡¤e\x0007\x0001;4È\x001eò2j&[rüUuÊTË)SfD¸nôrÄ\x0000ç?²ÈêHÛt2¥z\x001e\x001f¼ªÚ_\x0005p_º¢ÿÛç»q[\x0012Ln\x001eëªgé
0ß\x0000_\x0006gÅõX\x0007÷®«û?½¸>;ÙÏªKV=Ur6\x0017ûPù;\x001bëÉ<BÍr\x0018XSÂ9°&zZçº½\x0015©/\x001aÉFº×æ@µ%¬'Y¯RbU\x001bi8²	b\x0012¬\x0017ºÔÓKX}Éêg±¢qÐµ6\x0000¬É¥çN:u*\x001c\x00066°q\x001e,Î°é¦¶Z²ÒtÒÂX¨s\x0018ÉJYÂâã5\x0016g\x0014\x0011­5Ô \x000fF4¥S<ªÒÃÐVgVÎ;´ ßÓ\x001ac u9°ì¢fZ\x001f\x000eD[Z9óØÚ\x0016ë85lô¬\x001bz
p\x0006ÿ`«S+ç\x001d[%Óº$Y²A¼r|j½?îþÇ÷Ý\x0006½RºøË¬«fRç9VÝ)j²«F1s¯¢¦\x0017FÜÈóÓ6?`\x0008øõãúþ#Ö ?\x0005Øaë*\x001d'Ü¤ õ
¼¶P\x0002¯/Ï_a\x0019ê.ñEîb-`Ô$\x0018Á£\x0004\x0003hÀ\x0019eßJ©0ºÑÓ$\x0003\x0006\x0012O\ÿ!it\x001b\x0008Æ\x00047Å,v\x001a\x000bx(ÉºP`_\x001c©ô®H#¹bR»q%\x0006£5\x0007ä\x001drÑW]Ðkñ%\x0006AF*¿M\x0019I³Æ\x0001Fº)0a\x001aµdWÁg²\#U.lÕ3\x0005\x0013K8%ÒÆE§lðl7a©!ÄªÚª\x0006Â³E-#&\x001e`ÅÑCL´¦y p
«²D´\x0005¦VyÓt^Àè*2­Ní\x0007Àä3£\x0007S©<9Mçy°\x0014È\x000fÃí@z¶*!ISé\x00199MÑouô\x000c®ü KÀ!hþ3\x000b¦ºÚrÚÝ\x000eX@æ( ®X4Jj\x000e9W	¬\x0016ênËi;h~\x000f\x000c\x001cHéxÅA\\x0016^Î©.·v»5Tr­¬\x0008¬ö¨\x0018\x001c\x0004£ç	FUw[M»Û\x0001Þ\x0003>\x0013x\x000c¹H±7)g^'UÝm5ñnã[N°ï¶2ÂzªªÛl¡©íi\x001b§ËSs23	`H=W6A£¦Y41hºÜÊ¹\\x000b/=}'°Læ\x0019\x0011Em2Â§&°\x0015\x0001J³ÓðTò}23¿SeÑ¨i&MÀsëówô´Ù|§4¦Q\x00135¡AñNéhs1¦K\x0007\x0006Å¼§[UªFMR5\x0018 g£\x0006\x000eP\x001d£U>\x0014hÓygXW÷[OºßV
Çf
î téM°Þñ!Vó4®®·x½Cà¬ÆD\x00155FÍ\x0015Mí¯LºÞVJfëâò9\x001c\¦)ã¥-4ÕýÖî·\x0015¦[â´Ç\x001dÈ1b¦êÓ]£'Ù5V\x001afÕ¢Ñ\x0010ÙÂ

>Ä3Ý\x0004]\x00196zaÓex\x00024É{rÂ\x0001~wÁu¥nô$uTÎ© h\x0001Xä\x00003,])\x001b=MÙHÆIß)z.Ð^q!ZY3Ý\x0000c*ÃÆL2làÐHæÂ¡\x0011\ðë\x0014¿Þ¢ªîj¡©4¨ùÐáç[²\x0001ê\x0002\x0017`tnâ,JõIª¯ËëC³\x0014=](ËæpZk<¦R}fêS©C§£±9X³l6ÆÊÆTªÏLS}Jld\x0003®¦ÔPiô<CËT¶dÛX8®T­é\x001eÏ\x00140å>Ã8÷\x0010WÏLÓ|ø\x0014hºRX\x0005KÑÛ`¨
6Z9¦Ò|fæ\x0003\x0003/\x0006\x0018J×x\x000e«Yøã<³ÏVWÊN»RÊ)Î®ã	r\Àý\x0005´	}\x0006Mu¥ì´+¥eGJ\x001aË¶
\x000e¡^è8ï~ÛêFÙ7Êû4\x001dÙáàXvw}tü¡´÷`Ú:\x0018;ÍÐp£|z0±fÂ|àSgOð3ís[Ýo;ñ~ënÉnGã=w_{£X6j¦[g«+e'^)*MÅA±äîzf±àóÔ°«o7íùî\x000c\x0008G4Y×\x0004Å½Â!úyGØUÏ·ö|k+Å\x0005v~§ç;DÁ³\x0005¤÷|»êv»·Û\x0006\[ØÑ¨È²"\x0013rÞ¡qÕõvÓ®7^(*\x0012¿¨`5_(;3hãª7ÊM{£4xuÆ\x0019¸ÜçEq	ëç¦Z\uÜ´ë¤1=GÁºV:5G+\x0004agFúdÝL\x00016üeJ\x001c	|p*Ô\x001aÜ^j£uìK9ÓúN~ÍQåüü\x000f}¸½\x001a­fÂ²if0NîÐ\Í¤ÝLî\x0018¨æ{yñæíÅéùÕ®r&Ó/\x00112ª¬°Ã"¡å®c£¹7/\x00187P4×fJ4Ó&\x0002\x0007Ø\x0012yh\x0001¸§tÖY&5[¢Ù&4\\x0013Gh>V`«5T/þ\x000c4W¢¹\x0016´@\x000eªHÓ8SW/\x0015éÈâ@Át\x0003W(¹B\x0013WÄ\x0011¸IoáÊD¦À=½Þ
\x0015g6Å,¶ÞNJ_\x000bL\ðDNËO_ÕmÜLVd$¬¬µ 4Ï%\x0007h3±\x001f«¸¬Èú¡ú÷\x00064Y¡É&©á^;ÒiÊòQÓì*ù\x0010¡U*M¶é4¡\x0008
\x0006îéÕR²â°~ÑYâM\x0003\x0017ºPo;Ö9òa\x0013/ÚoTidó\x0015oS\x001d¹\x0017:¦-G)`Ì\x0013(¼\x00143å¦y úæbôÕóêÍúëÍÓêãÿùoÿýäÃÃ®ê*øÒQÌw¬D¸¡\x001c«û.RêõêÍñ?N®V¯V'//vViT[`ê\x0019&}a¥)`iîB<Sâ\x0019x¸ÕÝ\x0014cäÀBÔ<×Oè¾òfLWbºyRäøNk\x0016@)\x0015Ælõhe,Û |RÍÍàIêMl¯[º¥ð¡\x000c\x001cM\x001bñÑÌY]\x001c9çæ\x0018'ØÁÃå`]\x000c'j\x0018öÃ«¨ßLNUÉSÍ'Üðd&(3'Mâô\U!\x0006¦¹4cÖzh8íf*\ò¤*\x00013rU\x0001Üôí~ùfÎê¦«9WÝ*Åª\x00164g_Á»oÑÀ°´ÉR\x001f«ÂNø\x0001\x000b;ßÞ­?Ü¬¾[øí\x0019ÞW7\x001fÖ÷O;ü5\ÚÃãVs $\x000ftãõ\x0012ÄøöìøåÉê»ãÿßõ	¾<>¿¨KDÝH\x0001
\x001d2÷µçl¡qJÏG4¾'EPz)ööáñi}{×\x0015ò~³s2Ë}§D\x0016ótT5`Y¼½¸¼:>=ëªx¿Ù5È1U©f`bg\x001bQzvê
Ümª:')uI©Û)Á¦àº7+Y¸\x001a\x0006æ9=Ø²ÕiJL3çëÍDÜÍ\x0014'ë£ÕPÿb3¦+1Ý\x000cÌ¨ø%wàÔÓ$½<£\x000b¤©ý\x00010C\x0019f|t`£0\x0003Ä\x0013ªZ.úäÁõ®9\x001cªºÙäûÛO÷7ãæ9¼düje-u^Àåç!\x000e·p}úúüdqÎ`ª\x0004SM`.R\x000f\x0016Æ/¡é®D]¾3ÈtI¦[ÈLt\x0014 Ô#w4Ë7\x0004î{«êíf ¹\x0012Í5	MZº\x0013Z\x001bMN*N\x001d·ä¹eßÓh¾IjÆsë\x00164í/xö\x000epWÉ\x0012°ÑÝÝ\x0000ÑD¦$wªhð\x000eRAp;
¢5ËØªK nvC4Ö\x001c¤Öûà²o\x001aÅ\6ß7³¼(
+Po»CH+Òèyài¡úÃXç
TÚ\x0004\x001cUâ¨é81í\x001dLö½á¹\\x001c\e\x000c\x001aLId¦\x0013\x0019.0Â3ÅuÜÞ²lúH¶D²`ë\x0003+Yh9ã&\x001bûSj\x001a\Iä&\x0013§3\x0018p|8«24Àa"/üt\x0019\x0019
}­lH@ûB¶e}Õ¦ß5Üúf)Üu\x0007PÅ%'SªbóF&]1é©L8V*\x001dÁ)eKV³Z\x0002&áÆûù\x0018¨:Û²ápÿß\x0013Ò&\x0000Ñ)%Ñ¢(ÅÉxªÐR<×3ÄÙGIUJI5h¥Àáu
AÔÐ\x0011r±³oªt®\x0004@SÒóàÊsÄêÑ4N$úo(Þ¶ÕÝÿùoÿýÛçÛ;ZÊ:^¯JO
.*¦Îç\x0010\\x0008[`«³Õ·×§gÝ.Ö½pªSpÖ\x001fQEY1ª¨á²[G«Mlº
L\x0003®ÙÔ?¨sKºØò\x001eàL	g\x001aáºAY\x001dìÙâJ\x000e\x0016ÜÒ\x0012Ml¶d³­\x001f\x0007³\x0002æ¤¹ãâ3\x0010á2¹¹Í5²)ÁªLáÐØT.MËZ±qû6±ùÍ·~SîäW8yÆð;á¶§\x001a5Á\x0012.´Á V¸\x00128«øü²\x0013\x0017K¸Ø*¹MÊFðjÙ¦Oþ¬[Á½\x0016¸Â)C\x0005,\x001aE\x00174\x0007N$æHt&+\x0012Õ\x001f4ÚHWi`Ù¨×ßW\x0019¦¦\x001c­i\x0013É®Rs²QÏ	«±Ü.\x0015H\x0006\x001e\x0012\x000fÐ\\x0000­úÃ\x0001\x001béªc'\x001bÏ\x001d¶WEöD\x0004»kVyóT\x0008½\x001f~¨Âa¸\x0013÷õúñã.É#IÛs¢¡=\x0011\x0014 ¯ÏñÁ\x001d\ûúøòU\x0001×Ò%nÊÃÁ÷\x0007,/¿pfpvÑ\x0004&[2Ù&&é\x0014îØÏíù¹â·ÔúáVû¡B	\x0015Ú\x0004\x0005&dÒh2®#!©[ÍRe·\x0005*P±QR\x0001ÅÓI*l,"ky¯·ó dõùdã÷Ã{ôý\WjNÃòÊ#«çQ¹ÊµQâ¢
\x0012(+Í¹Í§Ê\x000e}'PùÊ7ÊÊã\x0018Ç$+\x000bp©y-ËJ\x000fU÷S\x0015¹í\Ë\x0016*ðzº]msz¾uÞ¦ef\x0018í Æô³f{í²\x001ewë§õ®eÔc:\x001eË¤hå¥ñåØÕìR\x001egÇWÇ»#\x0004§J8Õ\x0008\x0017ÒsCÿàà¬°/ë\x0015æÀé\x0012N7ÂyÕÍ¥åíK»Ã­(µü\x001c8[ÂÙ68+=pï¦%d9'h±cv\x0016\x0008±WÆ\x0015b\x0019ù}}ûx3\x001e>°FÈ#¶\x0004÷iEË\x0001\x0004\F¹\x001d@x}zy²³¶ L	e&Cé`¨]b¤¬~¼\x0005\x00045`XOr%\x000ee5}B[{©Ê-ru1h³HËT&_2ùéLÆ\x000fLÝRÑTëï²µå\x0007RÍS¡B	\x0015\x001a $ï\x001aèP:âêu7\x0010ú\x000cUNUáî>*×:Æ4Áº£r4Ùº¡pâT(YAÉÉP
´(÷¨Üh\x0019\x0004ûh.nûhÓ©* §ë\x0004-e>éF±i\x0013\x000c9qûù|ªJ'ÈéJ¡ë¼LPAozÖ$\x000f\x000fÁNeªT®\x0013TÔH\x0007êIæFY©6EÍ\x0003aó©TÕýÓ/ ôÅVBðN\x001a[`½ÿíTuùÔôË×fç®\x0011·1ÅÜ52ÿò©úå~Ì±ßPr\x0012&W}»¼(\x0005zJUGJM?R\x0012÷¬Q@?8L^§X¡à\x0014Ñs\x000c=Ï\x001eÎSáÙ?¯^<Ü\x001dsóøññfý<jÇXlJ\x0005\x0012xÊ\x0002»xAâ ¼ëÕS0fN._]\x001c_ïÇT%¦é
O+^qÚ?D\x001c\x0018RÛÌ¨KFÝÎ\x0008²äé´Ò¹#G\x0015\x001dyM\x0000ò\x0003`\x0012ÓÌ\x0010%¨¸ôDiì\x0015NqÐÝ
\x0012¦\x001fð1miÛ1±J?¸ iLÁZ8\x0014\x001c¦4SºÒÍøæóãÝ¹äÒ''²0Õ@(£\x0019Ó~0á¥N©hÆÐ0
\x0014æ!Nf()Ã\x000bÄvfGiéþ\x0002CËê[)\x000b{\x00135¦)\x0015%ôt\x0017É¢\x0012¤<5\x001füÁ\x0003HSV÷\Î¸èZqþ\x000c8Aµt<O¯
Ò
DnÛÕfÕDÜ©ÎrBòtZ}\x00086«%\x001c¢Î´a Ð5V÷"9è×)ðOw·_vÍñ\x0013GFÞkF½2ØÃE«Û%Õ«³ÕÉë³Ów£3u/Pª	J\x0019i\x0005\x0016Åfù­âU[qÛ_ÜPí.Át\x001b<¢Zd©¸ùi3DTË¡TÕT,[bÙ&,0\x0011\x0005rç^zÅëµÀ§\x001cJRMår%kãb\x000f
äå7Ã\x0007yw\x000fÜ¡üÔT0_ù60ÃM\x0019.Í!H`¼"Gí¾Ý\x0006°P6°ÀÓO±ÅÁóO. Õz{CN\x0003X,Áb\x0013U<ÏÁW¥R0§\x001c\x000fìTÎUöÒ~\x0006y\x001f\x0018<V4ÀÙ<6Q¹Àc²íK)kÍÚ¦ZÝæVÚÍßÜ_a·\x001b\x0017\x001aÀ*í*ÛÔk4yÌ¹
|úµPYd)÷©d\x001em\x000c<\x000cJh;\x001cROÇßñ\x000cLíäVø¤¬R\x0018²McÄÈOÇêq\x000bnC1r°b*Yu1eÛÍÄü\x000b¥b\x0000Eq\x000c?JF÷¡N#ëj\x000b_\x0015°­Wß<Ü?½¿ææi¼ý­\x001bIubÒE\x000eýÚ¼=noÂÌÕ7\x0017çW/.ÎÏO®vµ¿ {æOhþ~þuýå\x000bsîN¯)x0
E\x0011q£\x001b\x000fã\x0001{¾zÔOß¼=~÷){ùµ1<Uâ©6<\\x000eCù÷¸éZw\x001cÉ°¾LþÍ¢3%i¥\x000b9µÂéU@_!g\x001bÌB<Wâ¹ÆokCNÐf¡Z;ïU®¨°ó¥×_L\x0012l7õÛõ/\x000fã»3µÈc¢±ÇÍsø2mnl¿òÛãï.v®õì/)	¶¿z7Â]%´r\x000e\x0017\x0018óp1Î\x0001\x001a·\x0008L`ºMby³rÀ­\x000bDÆù6g­X&3[¢Ù&ád-Oùð\\x0004\x001e$à&ôÃ¡h¾DóMhNp\x0011¿·#µÞóþ6c}Ð2Õe·*ïa3S\x0000\x001eLr\x001e\x000céxÖªÑÖÎbº_â¬7%ÎØ\x0002ÿ¸¾ÝµAÐr\x000fÂòDz\x00136F¸\x001b¡~µ°ñýòøtWz^÷õ¦xx?\x0012¶bq\x0013Mî£Ës7¶\x001céH±D¢<â1\x0006y$by¼ò¶\x000f5¨h¢ÑE\x0013Í\x0004¤À;´\x0012y´'Î¤~¬­
æéLÕ¿\x0006\x0003
\µ.2º\x0010.ô\x000b§3ùÉOf².G±yÉF\x0014yÆqØr4©:MròqÂj
z\x000fµÏûÕ£¦
Nbþ³Iþ3mìV©èËÇÛßWonïînv¬\x0007CÂ¸Âä\x001cª5Üêç\x001ev¦ÄËËÓ¿¯ÞìR§¦ÿp\x001b[õROFÒ¥©ác°QÖ5þu¤.è±BÄ¤*ö
\x000e¸Ì\x0013Fp^ÔÝúùãom0,J}ªR¸\x0014t'¤\x001c\x0018vó¢Î¯_íüÞª_f¤b1-j
\x001a\x000e¥c\x0018iF&\x000eåaçXâö%hºDÓmh>o\x0011.e\x0011ÍvëV¸-A3%iB³F)ÜeÚ)\x0014\x001c\x0011$ó\x0011¿=,¦\x0005Íh¶	
L³@Rëæ\x001eàH 7ø¸íqU-\±ä-\ð0\x001cñ:xf*I\x0015yÑ\x001c£Õ\x0000&ëËÙt;Á/b\x0007ÀàíLçL:u(Pµ­º\x0002²é\x000eà&±ôÚn¡WGf36Û¨
²\x0005aUgL6\x001d2Ê_³ËJ\x0001Xä
%JYWs
X®=Æ?Â×<{xº\x00057øóÍýÓê\x000eË5p¸íÕÛÇñêÎä\x000eÓ´$÷ÝxÏKÎM5Jöìâê\x0014Üá7'çW«3¬ÝÀq·ïVo/Ë2Ï>¦*1ÕLLÇÊzax 79\x0011ËöÕYºÄÔs1\x0015ÏLòBl0¹ÊXÇ²=s\x0016¦)1ÍLLÅ½\x0012Êa.0yÚ½Óea\x0016¥-)í\J§üøÍl¸ëj\x0007Ý,LWbºX(JË\x001e]±#'\x001b]éKL?W¹ãÏÙlJ{ÅÚHÛ2j8\x000b3aþÑä<\x000eXßMG?º\x0011KõQ,1ãünIÊeµ¹¹èjé\x0015Ê!¤ÝÅ|ÎÈ©üpÄúHæ\x0011Tz\x001e%ªõ½\x000fß\x0005¨çÇîu<¾»»Ý3Â"P\x0016Ó(4Â<{º"ñòâú²{\x001aÏÎNw
Åb*UR©\x0006*ëó\x001aÙOâ]\x0017@eÇ©F\x000c	Ñ\x001f©.ºêÌu\x000f^æYgÁÑ'T¡;5KÊX¦\x0001Ëå6S\x001bM.{p\h¥EUÂ4\x0019KöFt¡?T¡x?\x001eA4\x001et\x0008/u{0D`Hùå@ç;\x0003	°(p\x0006@9T\x0002¶Ð\x001aéÂD¨i¶b\x0008ÆdB³«\x0016u
aQÅ\x000bj¨âo\x0017¡ñÜ2³\x0014¹ZÖ[ÇVuÔó	Uot\x001dÂ\x0016ÞÈêåÏ8>ón|\x000e©\x0001ÅF3:´\x0000\x001e*\x000ck¨¼\x0003¶õêå·8;ólç\x0010Ò k\x0015\x0002?Ô!ï×Ïÿºy¼ßu;¼uÜ"nqý	í\V<Â\x000e\x0017f\x000f[¾?¾þþäò|ç\x0015a@S\x0002V@áyh¹ÿ_8ÁZE\x000fG®¦\x0001öâkr\x0006ËsÏ\x001e\x001fîw\x0015;ê$Ä¦F\x000elÛ<Éë­°\x001fÏ=»¼8ß9Íö?®-;Îö£aq¤^\x000e¬F .ãÜË¡¦\x001f5éL7áª(¶n,oÌ³{½\x001cjh@s%kB\x0003u\x0017hWô<µGE»ØOÑµ\x0015C­Z;&IðÑ©\x000bFHvØ°WÕCS¿&°Ø/C²7ó5<µ÷;£ß:R4(jÓóÈ&sÕ\x0007î(\x0018nðÚï\x000eGÙ{f£ìMÂÜOçræ5â¾Ñä÷DÉ*ØáÔÔex¦Ä3x!?`\x0011\x001cI¢Ó¼þ\x0019Ç¯,¤³%m¤×E|+\x0002õ®R£¡C«j!+ñ\\x001bé$d\x0007×ÆÀÓíÈhØ	pª_A¤ªa/ºÚ¡]1åpD»\x0010¬Ni\x000cÕ-\x0010¦\x0014ÕPsmª\x0019\x0000¥K(=\x001d
\x0007OÒ\x0006kãó¸`\x0003\x0007\x0007·äLÆ2%iÀ
g­\x0018ÑM1HWÕÊÒä\x0006,[bÙ\x0006,)y_¨	Ý¨ÌTã¢r$yÉ7\x000c%Uh Â¹j\x0014¬õÙ\x001f'Áâ^Þ\x0005X±ÄÓ±Ôf\x001dÝô¸{Ë]7Ê.é©XeB K¹Kç	Üè¾Ë\x001cèäyæ¨ÏUÝDÙp\x0015\x0015N(Ðx\x0007Ç\x000cu³¾KC¥\x0002ú#WT=r/ÈÞSÇ¯zárÉûv¡ô\x0014aEÝ71t1²ã9\x0005V/o?ß<Ýþù¿\x001ewÔÄÈÛ'pe-ú÷ð^\x0015n{8Æu
\x0010­^¾9¹\x0002`ç\x0016¾O¤j6)Í-³&/\x001bfR\x001bãö,\x0019 ¦\x00045³@1ðÀû«ÁP¢8&¯þ\x0005	÷vRø;ô,'*\x001fúÝúöþiõúæñó:yïÖàPï\x0018Æ	Æ¦Ký}Ö	nú\x0001:Ý\x001c/½\x0018ÈÖ®Þ\x001d_­^\¾9N\x001eâ»cp¯ù*õiMIkÐ:`JMp}¸MÑûî\x0006j\x0005Fa·¢Ä+ké.\x0011/Æ¤¨­W\x000bISj\x0005õõz¡ríÀ®\x0002vK$FMÂoñ¦Q»\x0015ÍðXYy\x0000`UIX-06ê§\x0012\x0017\x0003ZÂsÌqàøÊ\x0010ëX/!v;Ò
ª\x0004¬©Ü×à\x000fq¯ý3!\x0004MÜ\x0001ë[O%\x0017£rà
\x0015oÏ\x000b\x000f¯¡,
\x0018½ñH"h\x0015£7î jBÅ8.°¤\x0019µ ä\x0017mñ@	Ètb8S=!ø­\x0012õÛÏ¿®\x001f?î\x0008¹ÜöÓ÷i$¬ãk8ËcuÍXNùjWù°ïù\x0016×/ºÞWÌÆðð©@³ÑØ\x0001å\x0010\x0016âù\x0012¯_x½\x000f\x000f«Ô©A{îcu÷t\x001f´Tz±Ämx8\x0016*SáÉçÜ	:HÜÓÔá<\x001dOö\x001b¥©:sW/no~\x001a¿\x001bRpÑ3£Â¸\SÃq¨sãzõâôäýXªÄR
Xhl\x0012ë¼3I©ÜÓgÂ\x0002,]bé\x0006,n\x0019Ý,WgJhSN­Ì$M/¨	?°öx{{óøx³ººý}WÞ\x0001Û©È\x0015
r³åW:\x0013û£ÈÞ\x001d|y²º:ýûî¤éE4\x0011M7¡®*¡åD«¹g.ö\x0007çÖhcïý
^mûï÷?íÄò\x001c)Äì´¤ÕÐ\x000c1gÇHïÜ\x001eÅX¦Ä2Ó±,èh¬\x001bê°â®Lc¸[\x001a|¡ÑÛ\x0013±le[°¤ )ïRÒÆæ&%?Üô8
ÉH®\x0011\x0016\x0004ò¬5¹¥k{ôÞd¦²EÚnµHïÂ
0I\x0011^\x0017ç¡N\x000cêÈ%+.ÙÂe\x0014á4¦fÒô£h"Û\x0016Î\x000f·!ïáòýKè«´ß7\x000fÏ_Vþ\x000fL<?ÿ>\x001e#\x0004Uê)-5+ÔI\x0012|äùdf  úÍÅõå»Õ1æ¯ÿ¾QºQðÖF3Ì\x0002\x000c\?e½\x001eÚ¬ÓÈhJFÓÎ¨6S\x0016±JR¼ÜäÑsC!à²¿\x001bZöwC?<ß-~çð~}7Féq@%\x001dÅnEQWW¬Lnøªººy×éÅõ\x0019Øà§x"ÏÏö\x0012ÔÌ\x0001ïL>´¹H)\x001cSO~¤\x001cÞqÛ
êJP7\x0003Ôà6¿äîJÝm\x0000Ììkµ\x001d\x0001A\x0019JÊ02ämuCî
K;=Ç\x0011ôv¥{\x0003(|ñÞE\x0017½yÁÇ÷\x001fnoî»
ëï×OOë\x001d;Ö­pb\x0008ÊN¢$Íe\x0006®ÕV\x0011\x000b±Î_wÛÖ_\x001c_]\x001dïÞ·.úÓhDop\x0013²7l\x0003vÈÔ¤\x000f\x000cÿÚ\x0017\x001fªáí_V\x000f\x001fvÅfxH\x0013®*äÐÄ;
\x0003ìÈ¦ÇË}¿[ýøüÓïëÈzi»ÝÿåÃó\x001fXÕÍLPTÏ þöÝúîöÓý×ÿøòüø\x001f/n¾¼¼A6c±´\£\x0000\x0003°KµY6\x001a
\x0003´4ýûøìôõù?þãÝõå¼8y÷âò¤×Îþòâú\x0007¬Ô\x001a\x001d§PÃ7Ù\x0004Ð
¥Ò[cÃm\x0019)é
Ü^Ãs¦Ú\x001a\x0011ÐÊ­Tê>\x0000pÜã\x0008<Û\x0004pæ\x001d\x001e\x0016\x001cl	¿\x0014\x001cwak\x0002ïZN\x0011ÜJÅ'Å¥¢ÃÃÅ\x0008KÁµKár6çSÇâ\x0016HàÖ\x001dþ¨ \x0005ÿ·Pä.=\x001f@\x001e\x001c.\x0014éÈ\x0015\x001f\x0015ã\x000euTÄíO_¾òlÔºµ\x001bÃ²~þøp?Ù8@ó²cv¸¸\x000b-\x0008!\x001b\x0008:¨To·
½©\x000cì¦³\x001c_¿º8\x0002\x000cï^\x0000ìx±àÂt¼\x0006{\x0002¯I\x0005*\x000byã×ð!¼/\x0004ÓoÀÙÿyÚyÀ:ò®Ð\x001dÎ\x0003ÐìVuö#º:ç\x0004ß\x001c_\x0002ö\x0014Êô¶Ì£4\x0018)M§V%£\x00071SO$\x001eÛë62}û¿¤,oºù#üR|ñ³ÛçÕ«[l¸X½¸Y#íýÃíã\x0014Zu$]\x0005\x001a\x0018\x0010àñtS0>åKtÐZaÜ³ÓëÕ«SlÃX½89FìóÓ1\x0007Wý¸\x0006ÕU\x0004æÔÇ¨Ë\x0000ÿÛõgFkç;0»ÄÃ^p°piìgÀ]iI\x0013ö8{R\x0007J\x0011ðoß .ÚAß=<ºü¡@Ö%²lÐHOÈÞ¥^Kì\x0018t~\x0015
Ä>\x0008²-í	dW"»È\x000e§MuKTÅ}¢N&dÁ\x0017P*q8d_"ûÙR\x0006Ó-=Ç¸
0Íµ\x0003dÏ\x0016\x0010®®=\x0018r(Ãl)Gj\x001b\x0000YQ\x000b «´r\x0008\x001cyÝf Ç\x00129Î²piH>JY§\x001b [Iæ\x001a\x000e>\x00142E=YÉÙbFë´±XûÄlød\x00041b\x001bÏ`®\x0015ó|Í,u@¦£¡f4\x001b©;\x001a#ïô\x000cfU1«ùÇYãøNi`õMÌ:äi/¢\x0019±g0ÙÌ×\x001a\x0002k\x001a;fërfXRwÛA«çDÎ}O@Î\x001e-áîl\x0008Ò$g¾&Å×\x000e\='rî{â1\x000bÑ¥)ñ=\x0001O½çã,\x000f\='rþ{"4yÔ\x0016lÒa6\x0006Ü:\x0008rõÈ¹ï	HÙ\x001e\x0005BÆÒf\x0012²åçD\x001dPgTÏûnîJ&ÙÐ\x0008ôj+\x000fwÿTõ¨¹ïI'f,\x0010Ì`KÃð\x0005Tö`GCUïû84<
ÉÙ.$\x000fÈRjVsê`ªYU¾oé\x000bÉf3\x000eS\x000eô\x0004\x001a~N¤\x0018sUg0WªYÍ7õeÀ\x0008rbG´³Ì,Ç\x0002s´FÞR°Ñ\x001cøË\x0002\x0015íé&Ê|\x0013½Ïèc±æ\x0019Æ¨ÜB_@\x000eæ':UÉ5iã#x±\x001fD%íÁ\x000e·}ò8ÜÅ4\x0010!YÓ*[L&û,Á-¶Lá
·UÈ\x0000è5(~³þðóÃÝTj©ÍQÍà´£®àÝá+É¹0¦þäÉ7Ç/¿½8Ä­Kn½[¦ù-\x0008\x001ePwàTÖàfÄ
\x0007nKp»\x0004\x001c¬é²\x0012\x0016\x000c¾\x0014¦\x0011Â¨\x000c>\x0012¥ÇíJn·;¡\x001aRôÖºº\x000b»Id\wS\x000e\x0008îKp¿Dà`£j·?Ò.ÉÛ>qqÌÀ\x001dJì°\x0000\x001b\x001bLs9m¶²\x0005Ç¼Ns=\x000fÅ\x001dKî¸[WNâ1í8vBR\x001e\x001e¸ÅXäf\x0016w\x000e+$E(\x0008Ü(z3Aà`\x0014$pÏ/\x001fKºÍ\x0003¯5ø\x0012\x0015MK.%h­¢ÖL\x0010y´E¾/­Ò\x0004®*pµèwÃÖÄi¸\x0015H<p,ÇÓ*àCWºP.P^á|\x000bRâ_\x001fi8³ìíA/§¬t¡\¢\x000c¤µÐ\x0001Õ±£\x0017Ï£6^ §Qw\x0007"WÕ)WKN¹÷©F\x0014$\x001e\x0015«ñ`\x0005ë\x0015ªâ;\x0014xe¨¨%JW4ÁgÅ"\x0017ÚYºÃ2âFÌ#¯,\x0015µÄT	Ø\x0002I÷3Tº\x000fä^;&×<æª:æjÁ1÷Xªd~<U²ÅØèr·/5Þôz.\x0010äå¹\x0019F¢NÍ:h´È4z\x0005OM6ËÝA¬D#ê\x000c$þþ<¯Þ=­?N¬è
\x0017×Jãµ2	Ax5¢Vhú÷»«ãÑ\x001d\x001d\x0005§*9Õ\x001cN0]m:ÒQDÊE[+\x001dq*î6NSr9\x0018J#\x0005JûN\x00004ªº\x0012ÔÍ\x0001ý°CiU\x0002¥Ö7xÀ\x001cq\x000b¦JÑwx-÷"6Wú`Õãâ*\x001alÔQ8.®Ú	<¹ÌÁu	®;ËÙðIIàz{»:¼\x0017p\x001e¸)ÁÍ"\x0007ª\x001fô±3±Às5\x001d\x000b£Íã¶%·ý/$pW»%àèñRÅ¦HñaàVÒò	\x001f{üæqûÛ/âBÇµÞ©\x0016Àµæ*<ì; x(ÁÃ\x0012ðàÓêU\x0004\x0017T\x00171\x000cîÇ\x0012éóÀc	\x001e\x0017sÌÒaC¤¢#n<\x00171\x000fl\x0016xá­ºõiF5u8Ò6óYñReòCªqY¿?\x001e \x0018Ó\x0010\x001e$÷i%\x0011Ö2p¡H#\x0001©yàª\x0002WÿD^=@rÉ\x000bäqå)ir\x001c@FÅ½i0%¶\x0012U Î\x0003¯^ ¹ä	Â~\x0006Iá\x00027ª½·F2¹#~À<òê	KÞ ïs$¤¦di§1ðH>XG^=BrÉ+5ª\}{\x001aÙGð,sevÞÍäÕ+$<C>\x0018vnp® {±9-4Xdõ\x000cÉ%ïP\x0010>\x0010Òj\x0003\x001bi®-ëj\x0016U=CjÉ3\x0014¤JC«\x0011\¦ÆM\x0004§Z\x0018 \x001f+ÓG^=CjÉ3ôÿXäÕ3¤<CAkn{\x0008©H­\x0003×c
æ þª\x001c8µÄ\x000b*p
-
fý\x0002¹
\x001c}0»$ÍàÕû©¼ÁÐød\x0004×in [ªÞ\x0008Â\x0015]Î#¯\x001ePµä\x0001
FSÔ8JæÝ\x0003¸I\x001b3\x0011üÏ§ªOµäùÄº\x001e¡\x0008\¤2W\x001b¹µ\x000bT\x001dÒ£PÕó©<Ý¸\x000b\x0004Ê´Ù\x000cÁ-qwP[KU¯§ZòzÐÍÏKä>Õ\x0003yÌä^\x001dRäºzô¢G\x0008¼8IÁBmø\x0011òGÈõ$Ì#¯\x001e!½ä\x0011"¤y$\x0018=\x001cbñZ«\x001c=<(yõ
éE¯PôÜ\x0008öâx\x0010È<\x0015´Í#¯ÃK^¡(\x0003ûÑ¥`\x001cþÊ\x0002÷Ôäºzô7(ÂãÉ\x0011qt(RÅÓ¸f$\x001f+iG^½AzÉ\x001b\x0014q&#	Ü§æ\x0008NU±AÊ\x0006u¥Êõ\x0012U\x001eµËz\x0005GÆ%OÈ;>+ò 
]¹\x0013z;´©yÁ\x000b\x001c
ÎJPù¾¦Råf*w`µQ¯;¦,`;%³\ö¬Ï#¯T¹Y Ê\x001d\x000eþ\x0011$sl\x0003Oà^°È½8äõ4&7\x000b4¹\x0013.¦
H/@¯Ø¤È£¡$wqgê²\x0019¼Räf"wà¢¥Ñg@n
wÿF¡<ÕrÌ#¯\x0013B\x000bt9îM\x0019!l#â\x0016[Á>üõ´ÊM¥ÉÍ\x0002Mõ&Ôà\x0000ÆUd\x0019|Or'\x0000ü\x001aÑTþYàO`W\x001f\x0019·\x001e7Î¤²j¶\x0003wär¬;q\x001eye\x0005f9Ö~§}\x0008xXr\x0011à\x001ew ÷\x0007=-Õ+d\x0016¼BNFK\x0011\x0016/µ "\x0014ûná9:äa±Õ#d<BÒÑþv\x0000ÇÁd$rÇþÒ\x0007=,¶zìGHjGÕ\x0008@Îu?èkñ1Wñ¯­^!»ä\x0015X`À±[4q%~Ðh­\x001e!»ä\x0011V¦É³\x0008.Ò\x001d§U¢>ì)¯\x001e!»ä\x0011R\x000bA<6Aè$sÜ&É×Ó\x001d2Îo+en(sÜ¶*b&w\x0004NÕ§\x0008~Èëé*Åâ(\x0016-h\x0012»vË£ÉËN³
%¯®§[r=q©¡Ã\x0012hx\x0017suÐb¬:|fºùÇ÷½óû\x0005y!\x0015¨ÇÑ\x0005«xsqÂ\x001d4å\x001cªjÈÕÂ_æÿ\x000fÝú9NÉYOEfÜ!Ý9©¶øÕB~ãx\x0002\x000exr©ç§.ÅñsqHMcD\x001f\Ò%üØL@\x0013\x001cy\x000e½\x0004\x001f²Sª\x000f¶?®+éÛ¿­äþ=õQ;\?"\x001c¦r,\x0000ëaÿ½k\x0017Ý\gÓÀ_XÔòÿ¬vÄA\x000b¢@ë¬{Zgàÿ\x001fÕ¹\x0018Û/
¶Õnº\x001fn\x001e\x001f>N+»¶p¢IQz°\x0019q]'nç9áv+Êw«\x001fN./^í¬¸¶õ\x0000¥\x000eWÏÃ
¼$Ùé>ÝËnØ2Ù^»C¢
¸¦Ä53qÁ\x0007õä=cÛz
':ýq·ßßkK\;\x000f7*Ú\x0010\x0010p.ÿ\x0011Ç5ä~lÌE3­+iÝLábV\x0014S\x0001ÓJQÂP³\x001d.ãîÚ\x0006\_âúY¸Ø©KÍK°f}zÑµ,]»[³5à\x00127Ì®±<\x0014N\x0004AgÁñxÈ äØ\x0004­fÚXÒÆÂ\x0005{lUÜ¦GÏu\x0014*«\x0003\x001dM='ÒJ1W´\x0002*\x0003©ÈÍñ°\x0002pÚÇÚyeÅ+g\x0017´§¸k\x0008<W6â¢f:
cÃBy«GMÎ|Õp®³t\x001ebêùÃô°æ\x0008Þíu5ðVÏùN`¥FdÇ\Rù:·áfØ]³Ñ@[é]9SñÂw§~~ µ\bc/7\x001eê4TLÎTeðñC!±*RnLfÍë\x000ft\x001aT¥\x001dÔ<í\x0000¾¥r/8½ôLø\x001cp×zé#\x000cïYÝ`\x000f\Ý¨züøñöîîöæq\x00121Z\x000e\x0014>uÆhê0ÂW2|ÝXýhÑ»w|ùêôììôär\x0002¹*ÉÕ\x0012r´] NrKór<
ÄË±êèºD×3\x001c	+½ÀÇà^rgÆNÊLtS¢ERCÂRÇv\x001d¤ÎãpÏAÉmIn\x0017	ÝÑúe\x0010ºæÀ\x0000¶éðpÑéu3Ñ]î ;[vàì¤Ù\x0003pI9ú\x000b÷XÀLt_¢ûERÇ6¤nÉþðÑþÿÔ½]¹qç»ÚÀ«@fâgø¯jv©Å	6É!§ùÇQ8\x0012_P¤l:ß_Þàux'^É \x000f2qÃ{î=À¹Ï#Û²*©¥Oå\x0001\x0012Dæ7UÏÓÖ+ä$zlÑã!t.ò\x0012ô\x001cE-jkÝ#E¿.\x0001>Zôt\x0008\x000bDpH\x00132:&]ëü§\x001b¢bëå@2Çö©\x0011\x0001ÒÅìEÝ>ÝÌ~½|½;àÐä0j\x0017¦¥Àý
\x000b;©4¿·[ÉÓIön£Â¡j¿/f§¼QÓ\x0001\x000b!¨<»»µÙ»
v*DÔå\x000eùh5ÅµëijyLÑ-É»}
6*xPQ|àô²Q­4\x001eå{\x0004ÜÔèØíS<²O)fKKã.\x0018­èáG$ß½\x000bzñPÔ\x000b:0/³\x0017õ
f§èÅÇ°èÆm\x0003°ö£\x0004a+ÍÑ8å°E\x000b/\x0012ç{8$`5\x000fÑÜØ¡£´ç\x0017\x0000XÝ8¸öæ4CûÛÝ?ý?ûFjxtVÃ\x0018b!"yÄ®Bn»\x000cYG`ýøêå»4þCq±ÅÅIÜªKé¡g O×²7]2[×¹QZ×Òº9Z[Æy²¨\x0007\x0010\x0013\x0016\x0017\x00187\x001b\x0019FY}Ëê'YsxBåþd.AÆÕ×\x0016»®\x001eÄ~ÝN.\îÃ-\x000b×%2§ÏäP\x0012ø´ô\x001båí\x0016.L®Ü(o-Ü\x001fÏ#\x000b/TÞ¸%!=Ìk;^;É\x0019®xy\x0001]ô²êemOP\x0018æí¶\x001aLîµä£\x0014(ºXêZË
2f6õ<y»í\x0006û-\x001b²°:>´Uº\x000eEH(\x0000Ä­zQÜÐáIÜ\x0014ªyÁ\x000e>¦æÀ\x0012p7â\x001doäµ Äò	\x0016E\x0000\x000bWµQ6\x0013£¼©ãMS¼!Ç\x001f|%\x9SÄ#Á©æq[IÕAÜ¦w\x0019J¸9eÞP½/;6/¸&èn\x000bæFË\x0001;ïsÞ!p­^ÑÂ\x000fP"-ÉuÛj¶Þ\x0004YW;S\x001cÚR;3eå \x0015Ù§{/ó(\x0000uQ-å¿ñ3ã;l;Í³3+Xª­øhÖ\x001b\x0014l
\x0016îÆÆÕä+þA\x0013\x0002¿¿{ñô·L÷õë®R\x001c­C-áüFGd´\x0001ÒlÏ\x0016b®6yÿÕ·o/T(4¶Ð8\x000fÍB¹\x0002Í½øÙÆª\x0019´Ùú8ÁL-3Í3Î,ËÓ\x0005±rÐ\x0010(¹­õ\x000c±mí<1×ÛÉð9À¢G¡ëbq³¤g\x0002Ú·ÐþÀzv|[TZ3?ÈÚ MFºâï c\x000b\x001dç¡y8}¹xP-©Hì
ióÝv9µÌéÀ\x001eÕÐAZ4xu\x0018ñÐÑn¶ÃC2º(#°¦-íª\x0014®/Ç
\x001bZo¦!Þp\x001fB·\x000fáÀFÄªÁÄéh(\x000f.\x0004N%YíyºÛpd'\x0006\x001d`­TUåhëSî¦\x0016Ð\x0004tè Ã<´\x0001\x001d1Ñó\x000bÝò \x0018¥@%8³)\x001e:AÝ¹\x000f8à?þ3MÝù\x000fw §þYI»Ø{y0Ï×?M\x0012Ñí\x0002\x000fì¢%\x000f2WY\x001f¬ÍY¶":-À!àí¨ûpé@¼cQ¡&%\x0003Ãqu<½¦Üº\x000bp>b
\x001e¤WÇ#Ô£\x001cIÕO-mê MPwÎ\x001a\x000f8kS\x0003\x0010\x0002#mè\x0011®kWÒÊCÔ³Æyg\x001d\x0012Ô\x001ch\x000eP¬ë å\x0008ns0Ö\x000cuç÷pÞïåhN\x0004s0 ²¬Ñ£z[îÅÎíá\x0001·ÇÍ \x000fUE[§\x0012§o%d7\x0005¡Æ©©ó{4ï÷|¨­ ¦\x0014ô.Ô¨ë#·³5u~æý^ó5áK
)$}U³·õ¨¿%Î;=\x001f\x001fL\x0016C\x001b[^¥25è\x0010\x0018´½\x001f\x0013ÔÓ£y§\x00178¥+$ôýOï·ä7Û)&¨;§GóNÏ'Òú¥	D¨U¿"oE¸á¢îBT\x000fQ½Ou¶CéÊ<ZVÙ\x0014ñ î\5Í»jªd)$ë\x001a5\x0004!ÜÔ
\x0019§¶ÝuÑÎ_\x0017}°Ú}h¼dº¢ÞS¨Í¦ì\x0004uçöì¼ÛóÞéØ\x0014Ñ)·\Ç$+ÄÇË)õ!êÎóÙ\x0003/_mu\x0004*Ùòìæ¢I"8ýöÖ\x0010À\x0019ê>G6ïù¼'}\x001dJ1êÝ\x001cT% m*SNP»ÚÍS» CR\x00161Ó¥m­7F\x0013¶ªOg¨;m\x000føk\x001e*\x000fÉ.òìçÅÖêön¨¶³¶\x0007µóRÐî\x00027¿£\x0018Zçú\x001a·Ù=AÝ9k{ÀY;ÇjNËòàE­Ð:¥z³j\x0006º\x000b¬í|`ÍÐbi\x001eâ\x0010\x0005Z_íóQv;h×\x001d0îÀ\x0001Op\x0014KgÌ"\x0014MÔÇåì´oçª]çôÜ\x0001§¯\x00002Æ<ä\x0005neUú$þv!é4\x0005ÊÃQó>7\x000bYê¾ ÀÒf]r!I\x0005\x0005à·Fë×ìy»\x001fgw\x00022Ë\x0012d¯Þ\x0014\x0019@ÏÑÍºÆ.ñ\x0003ãó¿þí)s.åü¼s\x001eó\x0010EP°è?rN5\x001c9?\x000býüç×\x000ft)\x000e||öêò41Æ\x0016\x001a§¡]Hüx[²S\x0019\x0002¡9Ø)d³Ø~\x0006Ú¶Ðv\x001e:z\x0015lÎgz¹¢§üwèK®Û]3Ãì[f?Ï¯`rIO`U¬9ÿª¥¾õÄ8Ã\x001c[æ8¿¢\x000bçFwQQ'ª\x0019¼¥×8\x0001ÝÌ}ámh\x000eP×«\x000cëÁ¢,iÒVa\x0013¶²©3ÔÝ>ùÈÏ¡:#ª\x001c­ÔqK?eº[Ô0¿ª=E\x001déÇó|\x0007k§ªúëF¤:ÃÜ-j8°ª3ÌMd
X\x0011{¡Tµvq«QºÕ©anÖ©66¨ÛË·õ$Æ\x000eUÊsKpo\x0004Û¬gÇ\x001bïaÏþòôëû§o»p­{\x0012Q\x001d~ë/Þ\x0003H_\x0018S¸¨\x0010øîîÙo\x001f~y|xw\x001d\x0016[Xå@OÔ£TØ\x001d0ê\x0000º\x0008Sî¥\x0016&-[\x001f\x0014¹W\x0004N³ÛndXÛ²Ú¿sÃº\x0016ÖMÃZê%SJ\x001e\x0017X]²
Â£°¾õ°(#\x0013#\\x0003S­\x001bL\x0001/I \x000c \x00165L¢Z\x001dj\x0012|T\x0015b@½Få8è\x0010þ\x0000llaãßµ]S¦íZ*ý2\x0005LÍªË\x0015oä\x0008>SßÌä\x001b5ü^¢^«¤3-U¯uyZínØþì<¼¸ðR<CÕÇÉ@ë\x0018/+Â
Ðv\x0017L^ÜX/â\×£N\x0016ê¼Ú\x001bí/èN/<¾þÓlÛ_0yeÛ¦
'ÛÖYÀ.ÞÆ!@wÁü	&½~!;\x0007RO«\x0005é²
Õ\x0000mwÁä\x0011Fîä¿¬êâ@­÷Ë÷·\x001b­Ûî\x0010ÙSÌóÂ%uÅ©ÿ27
d ;Ã`ò\x0010#_Ô8ó2\x0008*?\x0005à5ê\x001b\x00052Ðb0{Iñ5L[\x0007Ò®tm6øþ`¶ë\x0005^\x0002Ú*x:¾ÉT+\x0017ëÜJÐY¡\x001cÓ\x001e´nfXõ> i®a/>ûÛ¾\x001c°A¾\x0017	½ÈJó¥F«JèùËöÅ«w¯¯SbKs$,ÝëRnäd.\x000eHÜI-&cò\x0018{\x0012)çå\x0002\x001e±Î]¹P\x001a4éZL7IEP"@B®u+òÅ	®¸Ô}¡\x000c3(£±Bþ7ÂX¦$ýä\x0017'cí¥L-e£4Eë5ï\x0014TRT\x00129-w\x001c³©ùGÓF×\x0003\x001bH0¼k¸\x0002¶<õH Y¸8{q/gï&ÜQö:í";øZ|¤z*s^,¶³óG0å¼\x0011\x0007BuÍæ¬Û#ÝFîy\x0016\x0011Êg7êÝ\x0001tÊ©5\x0017Çìåìö:LlvWGk\x001c6ËKdX\x001a2Ë6¢-õ²}a}X¾QðçÏß>~ø´OàïOòæÁÓ´E\x000f5ÌËG»öâûó«w/¿¼dU`lq\x00128D\x0014%LÏ]æZí¤¤+]Û\x0003ÀÔ\x0002Ó,0«^y¬®uÄÂãËm\x000blg\x0019K-´RUÙVF\x001dÆu-®Å%S\x0007	\x0004S\x000bkÓÉ¾Wâv\x0003û\x0016ØO\x0003Û\x001aN³}eA\x0018{²ðµÚÃÝÀ¡\x0005\x000eÀÞ%í|à\x0015\x001cµìÐ»já[ñÆ7ÎòZàò{u\x0011A
\x000es,¨\x0006v7Ûq©\x0005NÀèD:\x0019\x0014+\x0007§\x0013±Àm\x0006°£°Ð-_\¿l?.,,×ÀÉ¢\x000cìS\x0012\x001dlæÍ+ìøzèÊl5ÑUÙ\x000c-\x000bð§ÃêÉa\x001cÔcSS{?·Y½'¢YÞ\x0013úòô)ãæHb×ÛAä\x001aE-&Îa£Ãzf'ýéÍÃËÌãëØ2â0c>ÀTÒÕÊE®\x001eR<Õ[Ý\x0000ZH\x001a7d\x000eÅôpÈ7\x001a)RBÔ°Õ=\x0002i[H;ñµA6çñ\x0015 FÐ¬´á\x0002F ]\x000béÆ!½Ñr/Ö©"±d¨Üº\x001a0úÑ3"FÃX\x001d¯uÔÝv	à\x0008dh!Ã!µ$_¬ôm\x0010£N*;Î\x0017[¾8ÎÃtÚ2¥<¡=
\x0007rÇØä\x0000Lya\x001b¥´é4>
E3olwßµqg\x001d¡ìÝø\x001fÏÎ[\x001eØ¹»Ü\x0004\x00136ã~6^'F ;?\x000eã<Sê«Ddmv-î'SÞÀCç#aÂIfÏ¨E ü\x001a²o¬¾¤-±¹\x0011ÊÎIÂ¦Æö\x0014k	!7x\x0008åV[@Cùôåïÿ¶ØùHp\x0001uô:f$ùÜ\x000c&Ùü­þü\x0011CvN\x0012&¼d¾æë%\x0014k	\x0005U5.s²s0á+£½?|i= I§¯ã©cLã)Hê9C{)\x000fÅ J~ë=w\x0000\x0012;w\x0013î<6Oóë\x0016)B}Çõ[ÊO#]0ãÑ¤ÏöÓüä¹©­\x0014­j~r[ïKC[ç4-O6Ï\x001ffÌYk\x0011Eér1§¾\x001b½ÐÍTs2|þxVFÒ(F9j};\x0007ØÇo;kXaµ9xóPYõMÜ¥\x0013ë
\x000cÛ\x0014Ñ¢\x000e{\x001cöòA\x001eÄ#¿2«gR±n`SÈºZ\x00000µ\x0000ºXª\x0010O\x0011ñr¾Á®zZíªqþ§Ié;£¦\x0019£z.cÞ8ñJDÚëüÖã\x000eØ§ÌÙå\x0010\x001eø\x001bå°áÅç_¹çé¯ï?ýz÷ñý×»_þòíË^±qÏó%Q\x0013KÙ-Ä1Õé\x0011ÞW¿pëÓÏ/¹{ñøöîß¾{sQo¼òÛß\x001eåwzE\x000e\x0010U\x0001$é\x0005yi2º1¾oñýQü@r\x000fX^Òe\x0016er¦þ\x0002[½Qó¿@lxø\x0017ðr</¿@"H<×V\x0013[RêÓ¿@½Ç.¿\x0000ßc\x000fþ\x0006V<LÀ¼åú\Í¬nU
Îÿ\x0002Ý\x000eÃ[>¥f$5[@ª^óo°U5ÿ\x001bt{\x0018\x000eob«£2òo\x0000ÚÎ»]¢û\x001bÿ\x0006Ý6Ãûxò_Àjb¥O­ÚÙª9çïv1\x001cÜÆìòë\x0017±æ:\x000c[)¼a|C~õ Ugo>|úõýÝ³§_ÿòþËO{Sâ¦^­Í2)w\x000ekÓwº4*ùíÃó¿<Þ={øå·o¿¼\x0010)(7¶Üx;»xBìY	$åg¨Þc7\x0005Ù¦À©\x0005§CàpïbM
9\x0005¯ò»iSèg
Ü¶àö\x0010¸ãwIm\x0013ññhtFIÚÖ+\x0002w-¸;\x0004\x001ek\x0013ô5»4_{\x001cÜ·àþ\x00088¦{]âI¬\x0012²v,ñKEøãÜ¡å\x000eG¸!`z6¸¯éx´5;»9´b
<¶àñ\x0008¸M2¤´¤täZïí)¥s¡ªl\x001c<µàéàJq²TH\x0005y©Ô\x0004é¦Öû\x000cøé)d9~Ì\x0011rTÌ/\x001a{o¼J¥äóç&þà<rrºÒ\x0003®IiÍ\x0001Ød¯%¥çÈ;\x0008\x001cb¾ôEí;×©\x001c)ÜÔ!BçXàgq®¾æ\x0011Å×l¿4¤yb·y
YêÚð_aµ\x001bøî\x00178Æ\x0017÷½_´R¾·j.9\jfÜOoÖ\x0002*f- r÷ñéN¸öµÚT}x.½7Ít^r["R§Æü»\x0017\x000fwòÃ«à¶\x0005·GÀyL
I·säg:\x00067±Np[é9pßû#à&i\x0008\x0010bí$5QÇ}&»õ@;\x0007\x001e[ðx\x0008ÜH;ç²Ý2\x001d#-2*\x0002¾0\x001d\x0004__äoÛåkè^bx Ûsü²,n_óæ#µÕ)_?÷ bS¨	µ 'ä\x001bs­¿ªÆu×:Év¢RJ³¨rºsK¼ðdÔÚSºUà4j[T;êXÅYø:|\x0015NÕªWÚ¶w¢º\x0016ÕÍ¡z_Sª\x0001¶©/»nSü}\x000cÕ·¨~\x000e5êQ­*WF8ÍÈ¹Ò>¸3´a' §Úü$¤@U¦OÛÅ¸c¨±Es¨Ve}xûÔãA:f·ùú©EMS¨Øl¯
UµLÂm\x0016¼\x000f¡¶²
]cÙ\x0010kÔ\x0002\x001e\x0016¡7ZBè5ºÙÈ\x001ccíÏª©ÃÇ¯k§¾	æ\x0019ÕÖ\x0015°9]h\x000cµsU0ç«\x0008«"J{#p¶¾F:¼¢°µó\x00010ç\x0004\x001ctç¢2BZZXÛ¯u\x0011ïeív\x0016Ìm-OZ(Îm;"±Ê·Àµ.ý+¬´JGe*]3Rúõço\x001f¾üißã\x0004ñù/½q\x0008%è
úFG[%°ÍDé×¯Þ½xxóã¥Ôþzø\x0018ác³Ø6/Z'Øù®\&	kv\x0007zmøÚ)èØBÇ\x0003ÐÙI7<CÛ2Y:ÿô½\x0011!Î`7y,\x0019å5Ëí\b\x000f¡ÍÒnÄi¸§K×Èqõû¹±ãÆynn0\x0001á&	¢Æ;¯v«¯\x001b;{ã\x0001{óº©
|I\x0004yÃbÂ¶rãCÜÖ·4ê\É·»\x001f>øºàÿüôå}{ÿëç=µ.×N\x0017\x0013¬Q/\x0018ÜV\ww?¼zþvùE~~xóßß=þòêRþ*Øþ*x_8)Wdç½\x0005
\x0000ïó?/¿Ç-)à¿
µ¿
Ýâ«\x0018~q)¡\x0014\x001fSå~\x0012ª4OØú\x000eþ&®ýMÜ->
ÅK-Uþ\x0016r)\x000cÆêà·ªþ\x000eþ*¡ýUÂ-~lÎÃ,¿JÀ"?ãc\x0012ülå7&\x0013XÇ\x000f\x0000mjæÇ§oûË]3xMUã'@Í;jqL`ñØ¡Î\x000fï^ÿöùÅÁÁ«]
ÐæfFXñZÏÌ¢õI\x001f¦«TÝvú ¬maí\x001c,\x0000·j·!Ø\x001aðnÕ±Âú\x0016ÖÏÁ©ég_Eèüò½w7llaã$,éS"\x000bAJA\x0008ZÝnyßÝÆ²­twõ\x001d[\x0007©®@ZÞ^»NÃf·Ò~X»Þ`¶\x0013øñó_ÿöáý}\x001f\x001b¹oR4¤ç¼mÑ-©
ôH×:ÿ|õóëço.Ý\x0014Zhæb\ÑÀüEpCÍµ±íCÌ¶e¶\x0007\x000cmd`tÈÛBulÈX5ôf|5\x0003íZhwÀÐV\x0003\x00115³Æâf[w\x00029´Èá\x0000r[¼Ñ98Tà\x0006ÌÕq\x0003Ð©NG 8Ý«À=it_\x001b\±\x001f¸õq¶\x0015=H]q)0\x0004)tÎ·a_K$¯
\x0018\x000cPCG
\x0007ì\x000c2@0ä;«\x001c|,&¥Ã]Ô8@Ý¹h8à£)rG©Öô;±µÕ9\x00106~&¨;\x0007\x0007\x001cuRÆ¯¯J"¹%²ïý<r\x0004©C	hA}\x0007U\x0019\x001cò7\Óë#¾£\x0016[ç§J-yMÇÝâ'û©±Ûxd'\x001a;\x0002ßqIU&5?\x0017úµÙ_\x0003Ô]ÜG\x0002\x000f#W`ÈIÇ<S«¯Þ.8 î\x000eq?Åg8ñz1JRöÐÚUxuÎÚ\x0000uwã¼¤>N ¯^O(hóÅs\x0002ºÛ8¿\x0019YÊ×4
(³^-©ß³°Y<\x0013N·ÕT%¤î}F\x0017w¨b41ÝkàT£êÍB\x0011t\\x000f\x000bÁ2,äáãÇ÷EèéË×÷o§½\x0013ÉÑèc¾vËÒvÖTá2³±!\x001f^¼x,zD\x000foÞ>æu\x00074¶Ð8\x000b¯TÅ"XH`a¦uÂ-	Æ\x0019fjiÞÐÁÖ¡_\x001eu\x0016Suh6ôÆ)3\x0003íZh7\x000fÍ"\x0017º:@ï\ü¨SE6.03Ð¡\x000eóÐ@rQ,Ú1êB\x0002Uè
o=\x0003\x001d[èxÀÒ¢¤á×Ébi\x001d´)o7ÁÜèÞÈdYhÌáReö²:\x001a}°\x001b2÷þnÞá±n¥êðHâêª [\x0003¦ü]Óï½x¼§YGÎÚpÆ6"\x000c\x0018Õ-Ô)cwíß¾öÔÏ®\x00134¥\x0010¼·çNkû\x0006ì&®_öâ)É¿\x0014>ûËÓ·¿îX¨êÉÔö\x000b¨mÈÆ]T#^
FýöáÝÏ;±\x0005ÆYà\x0010ë\x0000>\x0007ÚZ\x0004ÔS§Í$È00µÀ4maË
+\x0016×¼ÕÂþb=Ö\x0010°kÝ4°	â>aU³\x0000çt\x0007\x0006¼ô2\x0004\x001cZà0
´½/qÓ2bÕPKstS\x000bþi5jù³Ïþ\x0003þ}·Â¨·B`5¹ëu¢¼¥­áZWþìáç\x001cì_g¥æXsÄÊâhÔ\x0003cpRQhÍ{\x0018u-¬å\x0014À\x000b5I 3\x001f²OÛª}\x001bõ-¬÷|\x0006îy_eD\x0003Ùk3DwÂB¿dçÖ,wV\x0007E\x0019\x000cÈo(¨°îJÛÌ5Xtk]xgÚëéR+ð%ÿ-»;ñsìSç\x0015å£ØËAQßZyÊÊåèa)\x0012xóêåËËøN-:\x001dAG®\Ð]\x0000ÇãVªÀÇ§x-h\x001bDw-ºû/\x001eZôð_	\x001d:«Ã!³\x0003g\x001a\x0017t$G
×Ï\x0016rg¶j \x0006ÉÉ¬\x000bjM[\x0010óúó§_÷íM\x000c\x001c\x0008.eW8ãO}á+L^¿zùËuLl1q\x0002§KÊý#ÿQ£ylÄE/\x0017©ïÃ¤\x0016&0óQ"×iJÚJjt°s¦¼RT²Ò¶vN\x001d»ê¼VðUôvK)m\x0008Ó·~fiÆ*'Â~r!2uDÇµ\x0019gû0c\x0019'¿¹êÞF\x0019ÃÅ\x001f½b^)(ÛÙµ
*a?J#\x001c*­tkHTi/·&]¦\x0005»®Ó³[zýñéå>ñ\x001fÿò¯þøáëÞö¤¤½)y¥:m¤ªâ\x000fo¨¯_<<+7»Ç^<{é)Á®6?3Ó\x0011fP\x001axsÐ:¸:EpcwM0»Ù\x001d`æ\x0011'ÌVrÛÜ¯xu\x0000æ\x0004th¡Ãß94­\x000bV«ãéîÍû¿}ûÃÇ\x000fÿk¯úg8É
ÙÀ,·äÓ\x001e¤««úáîÍãëw?¼xþß/AÒºhµLÆá=Ö\x0012TÛE¡\x0016÷¥­n±YöÐ²ÿbO-|:hx£uð,$ÚÆpÒ6¹î
Ø\x001bY\x0016*­Gà]\x001d^Ìg¹¬­õ;Ë\x0006»)}·äáøGYó\x000eªé\x001d¦\x0004\u4côÝ¢«þ?~õ²Í£pN­9¼ÉÝûüõýßþ²+×Á³ÏÝBÎ\âÃ
\x0013\x0011d\x0002S¸õ´-m\x0006¾ÉÝ{õöñõo¯ccÇ°Ë\x00150\x0019mRejÉÔmÎ¦\x0016\x000e@'+u=g\x0005ç©\x0010£¶ÖfüË\x001dCcØ¶Å¶óØ¬^PlÍW\x0019\x0010ê\x0014ÔÖf+S0DmÖí'\x0006V/S?¼ÿòë§O;ß\x0002=ëê\x0004ob©ÓEU9S÷ÁÕ·\x001f\x001eßüòæáåeÑõs\x000f¬{\x0006±\x0013T©\x0008¥<&ñ¬Fã\x0017+ûG©mKmç©«\x000525AËÙãP¤XC^:W_\x0002\x0007°]í\x000e`s\x001dt¨°\Y#Ö{Í¦Íb¤\x0019ìÐb\x0003ØM÷\x0007(.\x0017L[\x0007¬Ä\x0018nZìt\x0000¬Ê\x000c|\x0013Á\x0016ÇbÛ£¾`\x001aÄÞ\x001cð$OôSn=	7\x0002,Üþ¢zË(7vÜ8ÍíY\x0014Y4,ø2\x0001ÁçÏ)o±ÁÃEÝQînSÂ]\x0019&¥r4Uf\x001cç¨«ÑmÎ¹Áî6%\x001cÙùt/Öö|¸,§9ªÀê·£îö$\x001cØ<
G\x0016·ÏÇ¤äS}\x001d\x0014i«y\x001b»M\x00076et¶.\x0012¾ª\x0015×í\x0014ÑçXðbær:nçÎûÏëIé,hB%jD\x0008x198ÊÝ%óqÉ"U^J½£¤\x00126ÑCå¾¥¹;_Bó¾Ä\x001bnë,ÔèîKX\x0012êY\x0005n¸¸©s%4ïJñ\x0014"mÄâQ¢\x0015±UZ mÍwKÚ¼wMjÞ{*ª²Ò*âyâ³×¨ª'hvÓ¸ª\x000cË~¬×\x0004ùáéãÿ|ú¶WïÆ [zé\x0004 ¥CK´A¸­\x001eÕF[ã\x0017¿yxwQ[C°]í\x000e`ç\x0008PÛ.r\\x0008®`«rcM½¦)ìÐbyìE¾Dj\x0007]äÄÕ}ª?N[1ì\x000c6tÖ\x0003æ¶Ü¾\dÊ¸®|Xz\x001d×µ\x001da§õe85á¯wþÓûúðþËû}/æÎÖ'è\x001cIU]·|rªµÓÅÐûí]Æùø»ço\x001ew`Û\x0016Û\x001eÀöò)Ú*ñ\x0018Õ¶ñºi{±)¬\x001fúÃJîæí¯OÚ\x0019 jåtâVìÑÔÆà­æ'Ù·¿<üx)\x0005\x0018Ö\x000fþa%i3KK[Á<ÑfÁ%pµùÓÛk[\;Ë\x0003Íe=ÔÇ|]\x000f[iaZ×Òº9Úà|mÆç\x001a²ë\x001ci1lvÍW|Ün\ßâúYÜ$o}!\x001f{ú\x0012£=qÉ°C;g'nhqÃ\x001c®÷(K7qZS,XíWÆ­ëí(n£\x0016z½´!Þt:¨C]¼V'F!\I´\x000f8®aq\x000eü©
ç\x0012ãeÇ\x001e|0zpÄë*DW¨a-	
¾Kü\x000e>Xó4EIéqM¤'5Fð`«àXÏëoìkahð]KÂ pv»Nµ\x00015qu\x0005^k¢Ø
L-0M\x0003G¨\x001aç9rÁd\\x0005Æ+)êÝÀ®\x0005vÓÀ&Vmó|±B\x0015M2*\x0014»9&}
|~Ü3¸ZÀ!þÃê-÷7?ýú´{\B¨CB"<Ãs«²ígk_\x0013óêå/\x000f\x0017\x0007\x000e(8µàô_\x0000ÜÕ#(/Þe<|úã÷ùÆz÷ìÛ¾Ædg9¢Pí~{\x001f¤d/:Õ\x0013·Æ<,Ëäáå³çùÒz÷ìÝ¥îdÅÇ\x0016\x001fâ{_\x001d\x001fwÑjÑ¯Pa\x000cÿübWvjÙé({\x0001YÂª@¾®\x001b¼Öæ4jzÛâÛÃ+ÇViß|»Ò×ÿ ¹ÈKÓYfà]\x000bï\x000eÛþ­±Ú½m\x000f
o.ÛÁ÷-¾?l{§]Ái³F7ºìapÙ_Å-~¼\x0005¾Zô)/ã«T¢¹|1ß\x000fëÎOXw~¹ú|ÏÕwjë5ÿXÅý`SYåÝ£\x000fëF´:MëÁæ9\x0017£4M\x0005Ì>G²Ø¢ñ\x0017Y\x0007õJòfW÷\XÏñ	©KLB§ #\x0019\x0002\x0019Ða¹T©a«\x0019{\x001aÖ¦bê×O_¿>ýynä
©"\x0005Jñ¨WÏB[O\x001dÜEõðÓH ÖÌÒ\x0003xÝä\x00155]V\x001d:¹
\x001b³n\x00084]CàÜ¾yp¸+s\x001fýiö9lå±×£|®¦à	×ÅhèNï÷Ù\x0013þæéãÇ÷ûêæ\x001dçH4ÿ\x0010¸x§¸\x0014ÔôÃÅØñÍcv¿á\x0016ÚyLÿø§Oúö']æ\x000cúâÃûow?~øUvä\x001fÄÆÞ,¬Ù\x001büöÿô5ÿ·ú|ÍE*RR\x00138°Æ¼+SÀ\x0010Ò2¬÷·¿ÿñí?¼xþøîîÇç¿È¶ûaÛ=Sv~æ	Rþè\x0014S´Âä¶CLù? \x000c1ñ«ær
\!q\x000fIò©TB\x001ebÊNL¾<í0g	\x0002UJ
\x0018jI
\x001câ\x0002\x0013\x0018[Q<Á*¯f\x0011Eeª|0A¡ò~I\x000f\x001e¢Ê¿Ö2)|
\x0007\x000c;\x0016(ÒïÇI£PÙë/Ã¿\x0007 Ø5ÐB\x0005e\x0006S±.¶P¡¥£TyIÁØ²²Æ²ÄBå\x0002¯°Êø\x0004\x000fñ¨­XÙ\x000cÇ6`\x0006(ÝÃÒ\x001ei
Kõ\x000bÙ\x0006¨²pÌVÈï7©¬+
\x000cÈT6zµUZ\x001aâÆ©x¼Âéð\x001f4?|þöåÏwâÑ§»ß>}ûõ< OÜ
·ø\x0008\x000fvù®\x000ch8ÅÑ\x0019_©ôiýðêÝî~¼{|y«íc§"Ú\x0016ÑN!.µ#\x0019ÑYÎÕ\x0017DPDpp\x0014Ñµn\x00181êm\x0011
ºËBÑ{`DHG\x0011}èÇ­ÈïüI\x0010\x0017\x001d½\x00051\x000b#z:\x0018ZÄ0nÅ\x0018J*×bâCbAôe\x0004öbÅ£±%ã!N\x00196¢ç¬ÁBèB%\x000cö(bj\x0011Ó8"³éwFÖþ\\x0010é´\x0014éèwnCÃøÎqQy!ÌüÖ]\x0018£ÌÏÉhüQÆnGÃÄFSnÙ/ª\x001dýÑÕ\x0008ÝjñåÃï{ùÔ~\x0019\x001d» bÑ+c3.ò"G\x0010Kå¢""#fÏêqh\x001b¯3í\x0018\x0001Ôüo7?å;c¾@¾ù¶q(çÿõe*E±,\x0002¸l\x0011«\x0007-µC\x000bÔOù./o¶Z\x0010lAp\x0007\x0008k¨\x0007+ ¨ñåáAL\x0001¡\x0016väø¶(\x0015èÊg\x0002]ì¶Ìj\x001c\x0006±-Ýc\x0011Òëæòi<ÈY¯G\x0000+xÌ¸\x0016Äí±H¬( Ø"!`ý4\x0016g@|\x000bâwZ$ªE"\x000b\x001e\x0015æL\x0006qS&´ aEPDJ
ú{_\x000c"õé#4ÃZ´ÃGªá ,Ã`\x0016\x0010éÍfà'@ÀtnÄìñ#QÄdÊ§I¤ñ
è§ñ3k\x0004z¶Ç£y\x001bô>ÛD¯dX/µfH:\x0006{\ZôêïMZúGJôª#3®\x0015ºm\x0003{ö
w2Ë·ÉG\x001cßÉXõñ\x001e¦¾Mì@â\x001e\x0010L¥ªI\x001cÏÁ]|k"[If<t\x001b\x0007öì\x001c\x001e=êÆ±%xuü¡ÝÆÁ]\x001bµa±$ ÄV¡~\x001cù8Ø\x001fÀ»+"XÃ$Ëà´B\x0015dÊ$Ý¹{\x000e>Öµ\x000bòqò\x001fÀNÃvëÃÌÁÝÆÁ]\x001bÇx
ÎM
<Ür!ñ¤G°?E#$ÝÎÁ=;\x0006WÄ¥n%xLu¸eBÝ¥=\x000b'-£ÜL¹\x0017NHHR^ÄÏØº\x0005K{\x0016,\x00179èµ×üX?N \x0019nÁÒ\x0005Ëí^Ã\x0001}\x0018À /\x0003ÙL\x001d9Ô-XÚ³`9TÓä\x000bk\x0010	I\x0000u°ÁÎD&Ô-XÚµ`\x0001208~\x0004\H,hÐ\x0018Ò\x000cí\x0016¬Ýµ`My\x000c+ñX\x000cÔp`fØn¹Ú=ËÕçØ9ê·I¬·Wµ\x001a\x000fDÙÂ¶¿XìY¯\x0019å¾\µ\x0000A.\x0016è£Õ¨1Nù\x0012Û-W»g¹zÊ|@&÷ÞI¬$ÁL@o»åj÷,WÇÃÃ\x0005Äð¼¦\x0012\x000fxÝÁÑÅj°¾\x0006¦SþôôñÃÓÖ
Ç~\x0019¸dq¹à8[\x001dí²\x0018?=¼xþpZ
ÚAÁ½"r\x0000óÜ\x0008Á°z¿q\x0004a\x0002Ã·\x0018~\x000fF*ãuKúNÞì­	FJ\x0013\x0014±¥{>ÌjâÌRP1\x0013Tc`\x0018Á0m­³üà\x001fÚñFÏ>üü×?\x0014¡Ú3<9F\x0005Nªó3áºe©*á±Tq8}\x001c\x001dòìÕW?ÿ°©HÛa\x000b\x0003`dËÈ×|\x001a¥Î=så¨I\x001f'{Z.\x001aáI¸8bR±Ô d®ìwp+\x000cpe×¯ïa|?,WfÃ£×\x0004Ì5o9ã`MÖ×KÖw/\x0019ØJÆÞp±	\x0006ÕbñÞ\x0018\x0001C³ZúhTóøßÿ­\x0008,~yúÓ?o^Ob\x0019Ï#àÍ%áÞ)È²¦úFy}w÷úÍÃ¿¿N-\x0011î'2\x001aö@\x001aâ¨\x000f\x0013!Í\x0012QKDûÂ½\x0000e¯%<©ærñt\x001cå±-ÝÍ\x0003 w|ñ´(\x0018½S¢³³D®%r{¸ËËu;{)Òw\x0002\x0010oÎCÛg|Kä÷\x00139^Ì(ò¹[4\x001a£8m¢Ø\x0002Åÿó@§¼â²óÍÿA¢|'Y=ëáO9*ø²y§°È«y!òoæK,\x001fë=«Aª.òÅC\x000e\x000e¶
t[(ÛBÙÝP,"¬:È`j\x000cËõÓL®er\x0003L¨9Pt¬Ò&	jqIÎ\x001c¾»|Ëä÷3·\x0012¡·é¢¦Ài\x001c*¶Pq?\x0014{£RIÂ¢è´Ü@X(¡@Ù4ÿõ _æû×yþjüÑ\x0016*zUt)F¥ïCÝTÔQÑn*\x001e+ï­b^óPVº3^îôx`¡C·ÐaÿJ·ìiòÄm\x0008\x000ce	eUaó\7N\x0015:ª0@\x0005ò.ãXÒ½DåhQ\x000eHtà\x0003vk\x001dö/v\x0016£"+T§ö2\x0015ÕÚ\x0011¤t*uTiÿ²âD,«ì¬|IÛ\x0000ú\x0005áSo\x0006x½ÝTä}i-b[\x0019ÍAc¢ú\x0005O9a*ê\x001aÚ}Ö¸TØ#\x0014CA 2¯=ßÝ«Þn¤Î«Ón·¾HSª.:qëÀ\x0015+*Ú3×ÝTÝR§ÝK¿\x0014Ó\x0012\x001fÊÅTÎX-\x001a\x000fó\x001fÏvKÊî^R.À©G>,®
¬õB\x0008Í\x0013é8\x0015vT¸ÊóPl/åõÅt\x0017*£ß/$úþ>¼ª©ö/ôeNYU.GzeûAv ºÖ£§rÝ\x0017tû¿ GQ¿ç²+µD@(Od³-óT]´àvG\x000bÎç#°¤Ê\x001cp1QYì$r\x0018<¥\x0003T]´àvG\x000bÎq¶ J6#qäÇTè¥H"oÐ#TÝºrû×ç´"Õ$_ÐkZ*\x0018;ï\x0019\\x0017.¸ÝásàÅ[AþSÉ?\x0003È`\x001d®p9[Ü
ÕËn÷¹ì\x001cy/üýô]\x001aÐ\x0004Òïçç-å»\x001dè÷ï@n(&\x001c\x0008\x0006ò±¬ÅìÑÌ[Êw\x001bÐïß62ws^^Î!ûP«)Å#TýukÿÁÌÓ´#pïM¡2ùÃiÄ\x00184t\x001f0ìÿ\x0016i7¥ÍÅJ1Y¦Bí½	v"É»vÞ·®\x0018õì/Oý\x001b³½~ÿåO_>ü¿[o\x000e!ÜK*è­L>4±HëJÑg¿}øù5\x0013¾~|óãçÿ÷uBl	q0ÊüyNh6LªÉ\x0006ÂuIð8"µ4ji«_	\x0019\x0011Ì)G³îæ\x0018'ô-¡\x001f$ä:½JÈUk\x0005Ðë}Ã~×(1\x000e\x0018ZÀ0\x000cF\x001fñóÂ¯×\x000b¡Õl©Åè\x000e#¦\x00161
#ÚZ,ÄÏ\x00026\x0011kaLó,0\x0008ýn\x001eÝÎù;'ÝÎ.ÛBèµ\x0012\x0002i]á?NØ-D\x0018^Ë\x0014=)Ì+\x0001\x0012ÓÒkJßÕÎ\x0003v\x000b\x0011ÆW¢·ZÆµ>X^a!ÅS±Ïq#Æ12"¸ZÂ\x000eu)æð7h:\x001cöÐí\x0016\x0018ß.<¦\x0004ªËAYÉßÎç2\x001dËÉbÍh\x0016ð\x001aþÔ¥M´ÈB8h;D;H_dm¾µ7erjà^Ëã®ctÃfÌNäKçû~éÃË×}u;\x0014ò,cçvpØí\x0010ÕM
(\x0017Æìx\x0011\x000f#R·\x001aix5æu§!uÊÎ»ÜÓÈkãxÞßöp\x0018A],F£ÁXàtj¹v'ëäM¼«O\x0007x|ÇP·\x001aix5Ú\x001c$\x001aW\x0018óÂtÒé\x000eõ	\x000fñð\x0019CÝj¤áÕè¬v®.#JRU$ÅsUöaÆî\x001c¤ásÐ\x0019\x0003ÐUÅ\x0000\x001fõAmþéää\x0007ë'ÑßùøþËÍ;\x0015«3Ñ°-ë§ô\x000fy{ö÷óã\x0017o_ºëÅu9]ìk®£QÔ¶.ëò\x001fÉk\x0019\÷ÀMãíg³-\x001ddK\x0012ÜðTû(hÒ;\x0013LJgÓ±ûÙ|Ëæÿ®ì\x0006Ý`Ôpÿ?Áu3Îå\x0007'»¯wo?ûÛeVõùz(\x000fÌ\x001e©
\x000cèµrÑþÚôøöîí«w¯oÍ¢n|ä÷"ESË±YÔöT(RíØdìºdÐ~·-½ÿøq»ç³ö\x0015\x001b§\x0015Ñd¼Ó \x001eÓÙtÕ³Ç\x0017/.æ`ÖZ\x000bö»\x001dy\x0011Ë"ZÅ\x0001¨Æ-2\x0014k\x0004zþur'k±Ü\x0000±ÇNäôÑ4%mÃ$8_Kq
kíöÍÊíÿøùßo*)EMU{J	\}mK¡ï~|õû\x000b
M\x0015Z Ú
DU ¯sIKêrbS@=Èc[\x001e»ÇÊCg\x001f/k©Ö\x0008:¦*à\x0012ÿÇ÷ÿßÿüôG/&bÃüðáóÝë§/Ìÿå(éPÿ\x000fÜ=ç?-ÊZD¬\x0008Æ;Í\x0011÷»E\x0016³\x0014\©5Íß+¹eI?d7Ï÷ø\x000f?<u÷úáÍ³MOÆ'ÛPüÏÞß=ÿô§o_Í\x000e;/ã»Ìõ·+X,ï\x0017,JKE\x0015c%®È]°xdHõ?^½|¼{þòÇwoÉþ;¯ë»\x000cºp\x0016­Òåÿ\x000b!¯éfe\x001fôzoþýßÚ!\x001b,*·~ä1­uEtÞpÞ³·ÞIàðÚ@Ï\x0013[NâL÷o¥©PúR(`¸«?ÜZJ¡ô®ÔÎåã"oS\x0012ïÙv\x0019épÓµn3`y¶Èül3\x001a±g¾\x0004Â
8}Ëé§ìÊKbæDËi§bÏ ö,.ø fh1Ã9c©â¨ÍqyF1gTst\x000bÎÔr¦\x0019N\x001e8'|¤ÉfO)*Ç0¡÷ISN)I/5g\.Á\x000eJðd"{­\x001bvN	¦¼R2ùlÐhïËvw2^ÎpV\x0014oÀÙ¹%ñKÖH\x000e<\x001bÔÑ}ùî\x000eÕ-Y{ïn;L;eÎ°´3fJÊkå³Ó\x001a\x000bsvÞ\x0013fÜ''¥Ì\x0012rXx[b\x001f% )ÜÀ}Bç>aÆòw·ÅæXº\x0018â\x000f_:U3(Â
ÎMè\x001c(ÌxP\x000b±è°dRâµºZ\x0014:ô·\x0000\x001dh²h\x0010¿d5XrEDÏÔá\x0019??k\x0011ÌÖô¾\x001fck:ÙHNt~Êc\x0006ufê³ËÌpöK¡Lá¤ ¶Ì\x0010:
ÚH8s"åXÂÏüý#?8\x0014\x00065¨¿Å>Â>J9,\x000båËP
¾L´Yö\x001aÔ§\x001b¸PìN$:r8çe¦P@ÚÓ\x0002
ñ\x0016öìN$9ø»{98\x0013p^±g©\x00051µ±ý hw$áÔT4¥Ù¬I \x000eÔºänà°;pêHÊ\x001f~y\x0002-g'éVÒÐ®Ï<ÊÙ9zrôèîON
A\x001dHÈäà&;¾óõ8åëÉ®¿üám¬;Þ[9$	s:WOS®>/Ð¥ª*\x001bÔR³,PÝòxD\x0003u®¦\½ÅÒ
\x001a±\x0008µgÐ`åË{wh:_OS¾\x001e\>S^}óTOù\x001b,Qê"3¾Þåà®¸&k Ì\x0000³,t$\x0006\x0015I¯§)_OXRöùÃ=½&ExäÀ
@;\x0017JS.4où(+Tâ.[¾úú\x001b$¨s¡4åB-\x0014	¿ÌÉebº@¶¼\x0017mÕc ¶ÛIvj'9SÆ½dÐ\x001c59¹xæëÚòJy\x0010´[¢vjºx_8ÑX~TZ8SuMÁÞ³[¡vj²\x0015Ë
EVV¨(_>ÐM¾|·DíÔ\x0012Ë\x000542:8¢=\x001flº\x0001¨ëO7u|²òdùôd¨\x000c@ã\x0004¸îù rm\x0007A»½äfö\x0012w\x001aJ<ByÓû²Fó¡)é\x00169\x001c×m%7³òáx\x001fÅ yû[åL²D£q78æ]·DÝÌ\x0012uù2ïÄ \AAr|êÝ3(Î1Pß-Q?³DöBð9¿ôB, Q?}¾%ßÀ;ùnú©%J¶/¹%*Û¼¯nË¥nñ¤jO/JüG\x0010#Î"é±òøåê#ÈMÒN°ÆÍ&ãå²B+IÈúþ%+¬&uö¸ªï\x00074.\\x0016Û\x0016AÞ\x000fµ,ãíÓO¿Þ½þòáý×_/\x0010f¤ Èeò*ç½7!­¶Ôò|ýöáùË_î^¿yþøvû	»"º\x0016ÑÍ \x001aAôûd\x0004±\x0004÷\x001ep}\x000b@\x000c-b\x0018Et\x001eXæ\x0011óU^\x001c\x0013åPÏ
¢[G#ß#þñéOO_ý²ZÄ4nÅ$ï\x001e`\x0001Ëò\x0018Jù¨a=ýÃ\x001fºyïÊ'\x0001Ý<ýG\x0018)Êc\x0002Y@\x0019ã:\x00176ÁH\x001d#
3f¿³0ÍùªiäS'qA\x001e\x000e#vû\x0005Æ7\x000c"ì\x0011ã¢üÈÎXÙ0\êz\x0014Ñw~\x00141äËZyä\x0000mVR Ù¶FÜ\x000eu\x0019»=
Ã%ÆË\x0011ðÄ:(_Úi@#ãõÓÖ\x0004c·©a|WçS¥\x0004\x001aàøy¸ì\x0018~9\x0012Æ°~Ç\x001egl\x001e7ø1ÃßÚ\x00051À\x0007'\x0018n\x0016;RZ?
O0v\x0007Ç=\x000f¿
-Ïj~1ZìèJQs¶c\x0002{±?©jÖÇ*f\x000cùÆk\x0015¥.Ðxþøî|#ûÆX4xyJF½äBjÎ\x001f\x001aÖOX\x0013¶C´ãF,¾;À¢\x000eUlhe%~ÿj9\x0001ØyF\x001c÷<¼¬Ä^B\
Fik×·	ÄÎ1â°c\x000cÙ\x001b(\x001c²Ç.SS³\x0019A.à\x001c\x001cßÐ±cÃJß7\x000f¨Z\x001az\x00163×OíáøZì7\x000e;oñöbG\x001b«c´F÷KXß\x0012Ç\x0019©sÞ4ì¼Y\x001b¿\x0014EBð1h`k£=\x001cîPç»iØwó<m\x00103zÔÌsÊ¿1ÆÃ:ÏHÃGK,áCê|ê .Gs\x0003;va#
¡<î\x0015ÏãXr¸ÄdN¿µ]§&\x0018;×Cã®Õte9ò(rÄH_\x0014;p\x001b\x000f#v»Æwu\x0014ÝÁH$	ß|È$¹ ä;ÿáOm»]mÇwu(Òð\x000e	ä1¹ò¥yÌaÄnWÛñ]\x001d#÷æ\x0015\x0007ÊLqvàê¾Ãa÷m»xÌ\x000eÇc<\x000c	ßIh¹Ab±"ç \x0015ñø¶Ý¶Ã{:òU_Ádù´Y¬håí>;ÉÃûÅv[Ú\x000eoéH¨'u$+ï\x000eùè\x000br
rRú0c\x0017MØáh"ñëåS£q51DËø`×U¸\x0013ß±Ã~'.&Å.Ý\x0007±cB"ï¼?¼©]·©Ýð¦f0¹®²¤§\³¢ÑcÐÅãÇuGµ\x001b>ª£\x000f¥[#HU\x000ewÖ8uëí8£ï\x0018ý0#«´/ë±d[Ö#iJ4°ööQÆî¦åGoZ6É\x001aY¨±\x0013\x0016¥\x0017Ñä\x001bM8\x001cÝúÎ=úa÷´&:\x0004³)/vÔ6\x0000\x001fâñ\x0008ÜwûÚîkkxDH±c>	ïm9\x0008h¢\x0018\x001fg¿C·\x001cÃèrÌ\x0017\x0016³\x001a1_\x0012¤h\x00004xñDÇÃî1tf\x000cÃfD#ú¼\x001c>É¡ÖâåxÜ=ðOý;ÂÓÄCIg\x001e\x0012ô­cÇCÂ\x000eÊ?ô D¥tR\x0017Æ^)äéM«­V~pêçû!ÿðñý×ËÑíéõÕÛÌS<¸Õ:À\x0004ëd¶B?üðâq«\x0013ºA³-\x001dAãî^[Ðò\\x000f@í6KÜr\x0008ÍµhnÈjÜ°·åT£É\x0004­l´t¶þ|?YhÉÂ\x0010Yv/åFeyåyAóN¿g:[É½\x001f-¶hq\x000c×{ù¤OtôI`Î¶»íGK-Z\x001aZj`$åÀ¹.\x001e9Y8å¼\x0012Ã¹·çÝh`º
jÆÌZÂããâòE½íÐ÷Þu\x000cùdPka<EiÃàû²\x0017«ùxè¶v®é´Ûg5Sæ¬8Ë/\x0000(ÎCHÙjëj­ók0äØ8/a\x001bÐ°ÂóÂ&êDÍâ1¶Î±Ágãì²\x0013øÉV¾©¯ß4í\ØÏæ;6?f7½ýÚ@ËHºb7I°&pÇÎ*èÜ.ù]\x0016¬ÁêÜ¬ú]ðêÜÖÕA¶ÎïÂã
I{'\x0002\x000byÈ\x0011ÌcVëÜ.\x000cù]î~öÀ÷Gñm9îÔ]zè\x001cÅÎíâÛ
Úo;e¬40J\x0010Ö\x0001lsÃ1çæEV1³ÅÈÕ4%þ\x0010íælû~6êØhÌnV¢ùÍ&É'µÕñº³ûÙ:Çc7_¸äÀ
§G×HN¿©èéO³u\x0017Ç\x001c/?÷Ë\x001eõR\Èj\x0010v¶\x0008r?YçvqÌízÔºÇE34\x0003\x000e²ÚàlÉë~¶ÎíâÛõ¡èëó.
\lTÌfÕ³\x0015ãûÙ:·cn×EíUÌW{Ù\x0008¨\x001b\x00019±|\x0004­ó»8æw}í¦\x000b>ÕP\fàd³ÅuÄ\x0018\x001buÆ\x001c/Oº\x0010³á\x0004%§\x0018­ÚÍ\x001crnÔE¼4v[öúD\x001d\x0008\x000f\x0016Õ\x001c3[w&ÐØÀRåv\x0015m¼\x0017×\x0006êÚÐ-÷ÞÖ\x001d	4v$øz»â
\x00146´ºÚÒÙÎ£ýlÝ@cG\x00135ªl¶|:$µÞüð \x0003¡îH ±#!³I	4ÃËÂ\x0016
ÅÔ9^\x001as¼Vf]jÄT½Û:«>ÈÖy7\x001aón6hG^¤ õ,QJE2Z<f;\x0007bÇ\x001c\x0008÷ÚÙlÒZÎh~R\x0017\x000fó¶Û¦vl:/]b©ÑMZ¸ÈÙ¥\x0016Ö\x0019ÊÐ+É@í,CZ²ä~idIÚÇ°üç¶\x000bK[ý!\x0017\x0006S4h¶E³\x0003hÖ\x0000²\x0016âvêWËw5í\x0008a\x0000Óh¾EóCh,4"}J9"\x0017-\x000fcvÕàf·ç>´Ø¢Å!´|R\x0007b.ô­\x00137E¯ö¥\x0016,
åk\x0004ºÙËªlR\x0007\x0017ãvûá.´6\x000b\x0018,à>¶¤\x0007qmkéÉ\x000e\x0003íì-~?[¿AGvh¶\x0010I6<û\x0012\x0014åØV÷\x0000m\x001aí\x0003Ã\x000e\x000cÇÀ@û\x0017£I÷#\x0018¹T±Ñ¶zàö±QÇF#l<³!h\x0006EÜ\x0005S?h<öA;·\x0006C~
L8íÐÀ/Ó\x000bÊ[ÝûØ\ÇæØ\x0010x\x0014¬¾F+ËÍºÞÖe\x0011l¡c\x000bClÖiuc¤²YÑÍÕïGë|.\x000c9]àxòE£ê¼«^ÖCchØ¹\x000f\x001cr\x001f\x0010Ï¸°%TyA\x001d\x001cÆfs\x000exì<\x0008\x000ey¼æË\HÇó
ù:¿Ø­6¤o÷¦îCë6)mR+c\x0018³Ù\x0000D/ße\x001fóùÉýhÝ\x001eÅ¡=T\x0015\x001c¸«3\x000c¨ßµ\x0002ûØº¸\x0008\x0002#°Úh®ÝT,ÙâµÓüØÿÀ!ÿ<,@w×ÕF¨ªºùöp(hÃÎà\x0003a}\x001bq I^!³ÙB=\x0012ì±OÚm8\x0014·!+\ÀBfåÌÍ4j¶mõ²m£g¸QçÙhÈ³q¢Ck¹ö£äéó§U÷\x0011ÏçÂwu\x001b6(Ë"{'\x0016CéJá¦{ýÛB¾»¾&u6\x0001Â¦Å\x0015¬\x000fm³\x000f|\x001f[·Òhh¥eÏ¦B¼Òª{Õ¶©?·\x000bÍv\x0017\x0004;tAÀ¨F\Ü¨|-Åz\x001e2íö\x001dÚ\x0007Ö\x0005ñ\x001dÛ´Dx(9EÛÖÙÖ\x001dðvè'cXj Íq¡hÙ¢êQu(t\x001d\x001bb³¤qYm"Ñ\x0016k\äã¡MêºàÃ
\x0005\x001fÜ+­ech9ÛF\x0000\x001eðáìCÚ~´îwC\x0007¼MApÞ®¥\x0019Âz\x001bªL\x0007\Ü\x0008\x0017®ëNP7t:0Rù¹h°Y\x0011
òT6é<B;\x0006¥ü \x001bióÏ~ýúôA.5¤òßÅq.kyiG6ø|Â¹ÊÙ÷W/yûðv0´a0Å2ZÃå}ÐRJÏ£\x0006Ùw«n\x00062µi\x001cÒ\x0007É¢\x001a'\x001dæ^%LøÕè0`©É\x000c'áýToÐßÚ¤õ\x0018u\x001dæåy®d:J\x001a§Ì{×\x0008e¾òKq\x0003¬JöøÇn\x0012\x0011Lé)]ôz|\x0018Îç;Ñ[Qñ"Ö²9NÙí\x001b\x0018ß8.È\x001c¦ôúÈc*µ%7C\x001c¦ì6\x000eï\x001cJ/gJþÕ\x0007±È«~ñµüô\x0004%v»\x0007Çw3Q§
?|Ç%ª^ÜáÙféAÊn÷àøî±ÑHºß(¤!¸æ±@\x001a®/g\x0010Òvv\x001c2Ç7¨¾ú\x0010@¨2
Ñ¦µÞ\x000ce·Åq|óÆ(bã\x0017[òÅ°PÞÂÝÙãw>\x0006¥"xÈ·HSå»<]ØóÍ9\x001fÂq?ÄBEE¯a'Qr·ùßN:\x0000á;¯	Ê¦ö$sºø÷S\x001a
»3¥PÄPÅåÏª\x0016
BÆ\x000e2\x000eCòA	&\x0017Í\x0018¬\x00196\x000cg\x001bÆ\x0006!;Nã\x001e¸p²0r¿|©\x0011\x0000¯G8Ú³2,c¶ûÜvüsSM\x0008\x0012·ò3F¾ç\x0005Ó\x0006\x0019±cÄaFQr"¬n"Úxu¨\¤\x001b\x001c:¶;tìø¡Qmq¤î\x0015R_Û\x0010×Zò3Ý¡cÇ\x000f\x001dnº¾RJcqª.xV\x0016a²óçvÜ£ó|ÞèRÖhT5&\x0017N\x001bdì¼¹\x001d÷æ<5S¦q«@iôÆÄC´\x0017HH·ØÞ£´ã2JJ\x001d\x0015µJC\x0003¦ ­È\x0017çÃ§´ã\x00128R ­\x000e4ÁDZH\x0002á\x0006×\x0008×yJ7î)!Ê\x0013\x0000åÿÑ\x0019RóQ\x0010Ïj¼
Bvñ¹\x001bÏyA)þÊWÈÈ\x0017]¦I¥Áãñýí:WéÆ]%\x0011eDòe°öBi¥\x0005(\x0002­+¦nd6k¹-Ú¬W\x001e
ªÍ\x0003\x0017Óù¦×Ç³\x001dô{a±ÌÌ<}ø\x001c(4Eu?||ÿíý¯*×l>XôK\x0017$åGtñl\x0019ÖÛ»\x001f^<¾{üåRõ°aËCl9(Óº\L\x001dò\x0007º\x001e]Øh¨Ú
G-\x001c
\x001a\x000eµÅë*P\x001f\x001c¦ýÌZód\x0014Î¶pv\x000cË%kÁò1ò¢A§éI\x001bý¢»á\\x000bçÌ%\x0001.µ\x000b«§Z¿>¡GÙ|Ëæ\x0007Ù\x000c×"ªá²é°l¸óE¦»áB\x000b\x0017F
W¬æP«\x0012	xì\x000f®·ØÅ1² Ùå:K é\°Ñ¹-µliø .:Oª³k§A¸¦6Ý¯\x0019´ÜRÀVü¯6´òM¯:à>¾Ýtýá0x:Ø¨å\x0001Àâ\x001b ¶#Ýª~£i7]w<ÀØùDFKÛí´aß\x0004ºó\x0001\x0006\x000f*d\x0011Q«\x00149ÑPßmXè\x000e\x0008\x0018<!,ê7õ\x0018¡«×$\x000f\x001bmL»é:/\x000cn8Ó¬;»d:NçØàÙJ£\x0001ºÎÙÁ¨·«Ùö\x001c\x0012kA\x000fÕ©©6÷÷ÒaçQpÔ£\x0018-_ç[\x0007J\x0005\x0019hHÿcë\x000eûntÏ\x001aq'uødè£ºõ]m\x0014­Û\x00128¸%x\x000cjÕYÅ'è)¦AÏr¤èº-[¢>!ª:I¦3¶ºÙE\x0007ëÉöplÿíîÙçÿú\x000fï¿\>d¤+¹\x0019W/\x0011Içe\x0013xw÷ìÕW?ÿðüñÍu6lÙpMyx'2õ\x000c\x0017\x0014nÅ\x0018¦£Fé¼t',Bb:\x0012EðHñ0Ã\x0010méì O÷FgµÚ­Î@"nXÓ\x0010kéÜ(]¨ÃêC\x0014#~­ÓÀÏÜ\x000fè|Kç\x0007ér(\ä«X©çÄÛÕ'\x001b
ëQ\x0018Ãx¡Å\x000b£xÚcñ¼hvrÕUãk\x0019Â-^\x001cÃã\x0002P«Ö£êï­Ö;ìTR\x0006ñ\x0000%2¦\x0018Ã=È S·g3J×Ü*Ø\x001dQ¼ ïÃ\x0019\x000ft°»5©î3\x0007í\x0010^Z\x000c\x001e\x0017ÕzÉD­ÖÎ÷3}\x0018>×29×\x001d\x00180xbPÑÙ]¬j]\x000e§Ô)'wôëvG\x0006\x000c\x0019ZÍE,	,BVwn\x0015Î\x0002CxÝ\x0001\x0006±Ônñ,ù£C\x0013-j±YþÎÓæ3¸Urh\x0017ßÃ?½ÿTª	\x0017qÁÿë÷¿\©ÉçïºDÉh×`\x000fIêÍ\x0002p!IËøð»Ç¥ª°è\x000bþþÕËÕ¸

xNð\x0014¨\x0011õ~´E ®Ê%7ä[\x0007Ü\x0002Ô¶ v
Tg \x000fM}Ô\x001a¤`×o ®\x0005u3 ±:\x001e9-±$Ãl\x0002øUMõ$¨oAý\x0014h©³ÈÊ\x001eF?½è(\x0005ëoòåcË\x0019§8¡r²6\x0018\x0014`Fs\x0013{¦3MqÊd\x001csfì\x0011Eá6@·X Ðû¦)çÄ\x000f×BÊhVIË=9 ¬Dd'I±#Å\x0019Ò\x0000"Y)\x001fJ*w\x000bÒJ\x0017\x001c®«¤\x001b)?ÃÝR«Þ¨D=NlJî&¤\x001f)Gêw¸Å¦6ÂºEÑà\x0008ßÕ\x0018Ov~\x0014¦\x001ci>l±(ö\x0013ºfÈÞõ&û)t a
T^ßÑ[s¯nT^'\x0002®A&9;?
SuëËÉ\x0012è$_Húå£½	hçHaÊ&'i\x0001\FÃÉf²¨)ÞÂ?açIq.ÌóêI}pz\x0007G«ë2ÙIÐÎ=á\\x0017¥³\x0000Yª\x0016d3Yy±
´ÎÇOv»\x001eçv}ÔÓ>Ô\x0002i&ÃëÄnAÚO8\x0015?QÚ}ÊÚ¯¬9Áû4ñ$i·ñqjãs×wI\x0002\x0002\x000fþ\x0014ù\x0003/ ÁÐ-öS+-Kyï8(_7IÁåèT´\x0010äy<°æÐ-@»À¦\x0002\x001342p ä­%\x0016µz¿ËÉ-¾=õ÷»¹ÀÄÈá\x0014)jÏ.¢tx\x0006î\x0000½\x0005h\x0017ÐT\\x0002^$}@Ñ\x0010Î&\ÈËô&¤¢)\x0017å­4 2Ëã&êdÚ`¿EdB¢)\x0017\x0005zu"x²Ñ;I79I©sQ4å¢¸:¬|}~rJªñs¾äÝäëwÁ	M\x0005'Îkp0Õ1!ºó9=q\x0003PÛ9S;åLJ8\x0013ºÚÕ
Ô¤x+íÂ(;\x0013FqÏh\x0019@\'N*/	¹âÇhnbÓÎïÛ)¿o±ºMã\x0014E2D{\x0018Úv~ßÎø}fãÅ¦¾V7\x0002H\x0019\Hpýd;\x001fe§|\x00147eJe¶,S5é-\x000eRÛy(;ç¡¢f§\x0004\{S<\D27Ùø®Ûøn."}U%NFZ
£$±·\x0014\x001f!õf%÷³äÏÿú·§¯_KÉÁ³§\x000f_.ZzÖô+\x0013óXCAFµ8b\x000caÕSúüç×\x000foß¢g\x000fÏß\Ô¶\x0014Bl	q0 J©\x000bxJèóùT\x0010×Ê\3Ô\x0012Ò°
mÀ>ÇIIÛ]\x001d\x0003){\x0018Ñ¶v\x0018W`Çê×V3\x0017dÛx´+©Ü\x0019Dß"úqÄ¨³òò9!¦:~~U\x0008>eÅ®â±$ÿ`ó
bLFï\x001a3®Þü§6Í\x0014'Hs°^:Îò=\x000eu\x001c¦×\x0010ÙÓÚY\x000e¦uÕN*U;Ú<ñ»\x000f\x001fßzºçâR'\x00061ËÃ\x0007Æ²`6Úe~÷üÅãËëd¶%³cdÜÀSæ±ò3v©eQa['éÙbË\x0016ÇØ²µJ;\x001f{¨³¹ÅYÜ
\x001e4\S¤*a?
¾Ìi\x0000Ê÷ÇR2ÁÝàuÛºJ|\x0014®[o0¶àlÁxjB\x001dùãF\x0019³\x000bñìpÁ\x0001ºnÍÁØ¢³ÜmR¶«
FØ¹ÙD= \x001dT¼\x000eh\x0015+\x0000µ=D?¿ÿúôéÏ\x0017}IþNïAËÝûMäÁß\x0015d}{÷óãÛ?]t%-\x001e\x000eâIrÊQ¡<KkÒ"£ÕS\x001cA£\x0016F-GZèB\x0015ðä\x001avUHØ\x0018^²\x001fÏ¶xvÔrFdô)ùS5j=\x001eÒt\x000cÏµxnÔz5{\x0012Ö:\x001dÔ6Z\x001eçp\x0010Ï·x~\x0014/\x000eOöwcéòq£Öé\x001aûýx¡Å\x000b£xÇFùEC$i>ÏÖ\x000e6ÒQ¼ØâÅQ¼Së$+Í\x0005±W§ò®Ö0^jñÒ \x001eªÀbAÕïìI
ê¼ý\x0000^[\x0001H]_Ñ^\x001cU\x0012(©À>\x0017ÇªÍAëAb\x001e\x0019XKúxÌ\x0003UIë gîÈÑ3¬NàÆ]é|âÊ@ý¼\x001bOûùºs\x0003F\x000f\x000eÓÝÁ57QJ\x0014«^_+>
óu\x0007\x0007\x001cT'_åXÂ)«Ê «ÂÑu\x0019F=3&\x001d\x000cj¢Ikës~\x001dÄïçóëÃS;â?þå_\x001fÍ¢=Ê_´LýY\x001añ]	ã!é±\x000b~­Y"zw¿d¼ëp¡\x000bcp¬C
%Øs1éàztúmál¯ç~¶Ø²ÅAÃEä¯²^ûùµJµ\x0001ìAÃ¥\x0016.
Â¥öF\x0005Ñ	AõRáì\x0004¬ÝlÍqá©\x001b±ÏrI\x0015I\x001cÇ*òUM¨_õå\x001aoì©E±Ït^_ò«ãrQ\x001fÈyvÒùÉ'{é¨££Á\x001d\x0001ª·H.ßº\Î4]\x0011¿«%\x001eÞ®}Âg¥ÎZ\x0014C\x0016\x0004.*Y\x0016\x001f\x000bhXù¾Ú¢\x0005[\x0002®2B\ß\x001f#ß\x001f_|úã{wýùéÃ\x000f\x00173â>{aÑ9p)Ò6FÝ\x001bÁ¬&þ½~ñðìQ4^~xþæù¥t¸ bÃ¡êUb¾ªÉ\x001b
\x0003\x0006rx\x0018ZD\x001aFô5háæ#)"Z\x0004\x0015
¢]Eô3¶E´Vt-¢\x001bG¬£H0ÕÑT1ø:¹¯Eß"ú¿K+\x00161ïhRÉfLNÛc<YÑÑaÄØ"Æ¿K+¦\x00161
#òT\x0017µb>ø
aº¡]<¼\x0014¡s0î\x0017sXS.r¬x ×ôTû#À*E4hÖÉIÓ%'øüíË×Ë¡¾áÐ¡\x001c|6^D ^4óMbCDèÕ»7o/Ïç[§&MÜ\x0005GÒ6wRfI#ÿ=\x001b"\x000c{ÙlËfÇØU50nrGÊÄ\x001asùµ¼ã(káÜ0tMóTóóJ³gç\x000cÀù\x0016Î\x000fÂÑ½Ò>ÉíÙ46G
\x0017Z¶0ÆV\x0004+\x00168²÷¨\x0013\x0004.¹MM­½p©KcpVëß;t¤UßÔ4Ì?×U;\x0000\x0007½#\x0019ô$4ÛìYñKFV*0tÔÑÑ \x001di¿´gm\x0012ûª[
a#á·®ó%0èLXªG\x0005/k¦Þ8LxNH`®s&0èM@\x0003ES:n\x000cÔËQ:;\x0010l®ó&0èN\x0008µLÐG¬¾N[Uã¦\x0016Î^¸ÎÀ ?ÉIiEöÉhYhþ©lÙ|Î\x001eó'm[
õJ=ûÜÌ\x0003ÖVªÓ²ÃMí¯½t·AwgT¥o©d\x0012Mïô}\x0008í¢ËN¸FF#\x00133¸êªàx`Áqù°Vç\áºÚ{®\x0006\x0003'8.:\x001d³iª\x0010¦-¾½tÝ¦À¡MAÉYyY[fËËw¥¤ò\x0001[¹ùÝpÝªÃ¡UÝÓ¸.\x0006[F#QÒ.ØHaãÕo/\x001cug,
±Ä
è%\x000f¤ùl:ÕLù.\x000f4L×­:\x001a\u9>\x0011I7â\x0005(ó´½
pv¸ënc@\x0012®\x0005\x0010úAß/>üáý_¯Ìnò:U+
m9ÿ½Õè$¦µxôâù\x000fo~¹¨3»®çÂ
Ó^@þQÞ
x$\x0016bxoN[Cv\x0003R\x000bH£\x0016äé®2ý*G¤¹P¾n2S¦v\x0003Ú\x0016Ð\x0002fOçe\x0018\x000f\\x0011¹\x0000	§õU{\x0002Ðµn\x0014ÐE\x001dÂiCb\x0017HË´:é\x0008	7\x001fï\x0006ô- \x001fþÄ¶\x000b^¯f\x001eô#ÁÙcc\x00080´a\x0014\x001ed8\x001c·O¯úisjînÀÔ\x0002¦Q@ðª\x001béêèÜì¬åhKî\Ù\x0010\x001fônpÔ\x000f.\x0013ÁañmÉÞÖyM)¸£K\x0010:7\x0008£~Ðæs
N\x0006ò+à
,Øy\x0019\x0018v3&éèUU¾Ç©æk:_6\x0004Øy\x0019\x0018u3\&º¯îÒãÿY\x0008Söb[\x0013¹w\x0013vn\x0006Fý\x000c¿¦JõCÞÈ;sõ55Å³ñ!ÂÎÏÀ¨£!"2aYEßJhp!u\x0017÷\x0004aì\x0008ã(¡Oªaî\6gùÈzýHi=io¯UYæz´oEòÃ©èU\x001fÛò*<¼O°\x000f¸F=
läèOe¹Q\x0000á¬\x0008ü\x0010`çipÔÓ°J]¹cæEhªP\x00188ÝÈçóßCÝFÆÑÌëej±(Oû|Æx!Ü\x001e+¾°Û&8ºM0Ô­<2Ô¿ÏÉøsò¦CÔm\x0014\x001aÝ(,q./Þ\x0005_!d¾ï\x0018çë¶	n\x00134^µU\x0018Ô`ç¨ú°³¦î\x001bÓè7lÁRÃn\x0003y°\x0007)sNpü¸s]I9Û\x0012ÅÜË# GJ4ê\x0010íF\x0019Ì\x001eN¿Öýó¸îhüùó·¯_?ºxwù
¥7ø|\x0002JÙipK
ëéímÛÓÏ¯Þ½}ûêåÅâ?\]3&N`\x0006ªå0\x001cá\x000f\x001e¬6T°±oI-&cú\x001c)Ê8\Ê\x0014%½\x0000Ô\x0017Z\x0007÷cÚ\x0016ÓÎX3Ê\x0013ðR\x0016\x0013|ôénñÍ]Ké&cm©&pª*\x001fõ0!Ø[`ú\x0016ÓÏì \x0002Xªcä\x0015,xÍ¼~W\x001d3\x0019ZÌ0aM»Ñ[¬y¾Ï\x001a­í\x0008)Þ\x00003¶qÂÉFôR%#=\x0004í"\x0008nU7ÙâR\x001a:¾Óm-B\x0011\x0011ð\x0010O\x0017zE÷CvN\x0013&¼¦\x0007-°å*\x0000\x0010ôNÝ\x0011Ü`iBç`Â\x001f-¯Ç²ÓMTÅ÷àív×ú~ÊnÃÄF÷§°B\x0019µR Î
~5ùz³ÛA0±r¤ËÉäâ7A±6íëÝØm Ù@\x0005\x0004Tn\x0011¨\x0017H¸;Â>îÙB¸«pFmY¾\x001eá\x0006î\x0008»\x001d3;(\x0018)ÅXÄÁ³6\x0006£Eg!Þ`§c·pf\x000fåËL°ãSHÊ\x001eb \x0019Öº9sÝ\x001eÂ=\x0014ë{nÌ"-ÖTÁó\x0010q[¦b\x0007gp«°8;vu~»{ýôå\x0017\x0008ù¦{\x0004í\x0017Ë¬PÇlI@¼»{ýðæÙu8jáh\x0010.ê®áÉ1¢òúìá7wÍ^6×²¹16Öíi{)é´ëÚ\x0006èÛ8mö²ùÍ\x000f±Q\x000c÷úM\x001d×¸PéIP»Å´q}ØË\x0016Z¶0ÆfÞ¹ËÒ¤ÈjfÍ¤ÕU6ÿ'u¯\x001co?ûòG\x0015\x0013zøôç«\x0019*\x0019_­ÈûåÖ\x001d$è	)CÉ·î·¯Þ½y¦BÜÖv\x001dÚ¶Ðv\x001aÃ³(å`êô±üÅ¥ÐÏ­Ç¢\x001eö-´?\x0000MZÿçrl¤¢u\x0018\x001f·Þ' c\x000b\x001dç¡sH$:ÝËØÈZ7ÛVrk\x001c\x001aú5}dQ;\x001d_b½ãº²¨uyÀ
G«VÏy¦NªåÀý}e<íï;7ïg:j:`j¯%è\ÿ :Ôõ¸îv"\x001cØ9HRuH§
uRõF/å\x0014uè¨Ã\x0001S[I\x0011+mY\x0019iTûMÌ-×Gê Ó¡õ\x0001â@ð4N°°,*t3jìV5Î¯jNî`eþÇ½Ì¶ÕÒñì ÁQhp«\x001c\'s=òv<ôU*T=?\x001a/¤\x001c\x000fÕÚÞFùëA7¬nprÎ{\x0001«ùx\x0011ö1ª\x0012æ´-ó(mÙì 
ÒÃO)Ç\x0010eúk^¢ZgÏkàù\x0016Ï\x000fâ\x001d&V¡U<®Ý,x¸Ñ\x0005²\x001f/´xa\x0010\x000f+ÀU´K\x001cÔHÆÒÙ7Ã\x0011¶Ø²ÅQ¶¨=*\¬Z
ñ2^ÕÍ9ëÜGèRKÆèbÒÙ´\x0002ÈlZûS:¿1±y7^+üâzá]|QÆ«g>F\x0010\x0007\x001e«¤ÔÙÊ\x0011>×ñ¹A¾\x001cJ¾ÎÔØ?ûAm¶°éÜ`¿!¾nßÂàÆåI"wR`Ö¯vóç_`CTj7_·qapçFÖä\x0012å\x001c4zb,yN\x0011öñ\x0007ù°[8ºþ,jW­á¾ÁXøæ·\x001dl\x000cªÝÏ×\x001d¸8vâÚh\x001aûEÉ:8SuÀ\x001e<Õ°?q\x0007ÜHª¶ÌÍ[)v,\x0007­|çû
ñu§.\x000e\x001e»#W\x0011\x001e"Mi:cOö;\x001a\x0015`ç^pÐ½`´ÌÜD¯ÂMy'«ýüèÚn¾Î½à {	Ñh/÷Êê\x0003£²\nK\x0019i7^ç]pÐ»pÂå¢oå1:¹\x000fF³1µ~?_wøâàéËÝ\x001c1÷ò>áôºÊ:5ñ6Z0
\x001bu\x0006=_ðN¦Z:X0%3åÁoKç£AÏç¹¢²ð~X/l\x000e~Vê¼\x001e
z½¿e,uvRg¢FËÞltþîçë¼\x001e
z½/\x001brhäH#çÏkHêélóÊ\x0008_çõhÐëyWßí,v&E«_w«©k?^çôhÔéY.Qo\x0019Z\x001a¼v®lî¦ë®\x001b4xß\x0008ùj´n h}C\x0002¨u\x0003G#>ê|\x001eú<©XËg¯\7lÔ:\x00016Ûù<;èóxXV-a\x0015\x0011M\x001c\x0004ÉËá¼Æ~¾Î±ØAÇÂMÉe\x0001K_ªLgLZU\x0015Í¹)çC|ÔñÑ\x0018ó:ùõÔ±Z½òæ8È×'Y\x0006\x001d\x001f¿\x000cËÖÈx ïÂzÚ±¨í¼\x001dôzÜ[!NÏU- ­ç1mhì§ë\x001dtz>_$¥u	e\x0014M¬>q=b¯s{vÐíù êÉ¬&Pk=n]Ö8=Æç:×âF]K^påÌ°<¦YJf<j¿h +¡ÞU¼Î³¸QÏâ<^³8{\x0012\x0014§Á^LG3·º¢ìrp²÷\x0016\x0018Bíº
Výsð±v<\x001eÝÂä¿ÃôÃ1/À ¥\x0000ªooPË\x0014®À[a½]gèmÿÖþúó×+Ýp\x0018tLSAò¸Ö9
\x000e6\x0006ø)áõ«·\x0017kÚ\x0005\x000e[8\x001c\x0003=Ý(ðé!Í:(:bØz\x0006ÛÉf[6;ÆæÊDnt\x0014¶¤5Z´® \x0018ó-\x001f u·\x0014î\x0006WeÊbãù<ÇÈbK\x0016È\x001c?\x0008	Y0:½Î[Õ\x0008g/jûÙ [n0¶Þóª"\x001aOÒV\x0001T_Âf×`¡»¸M¡[m0¸Ü|P\x0001Û^ÒzKÝr![wL\x000cÛ­[m0¶Ü|Ò:ÀåÍ Ô(Yßª¶ß«÷Ñµ)[»êe¼J·¤ÌH2ò\x001aäe·VâÏêZ
À¹\x000eÎ.\x0007 Q(ð~PeØúÌç7\x000bXvÒ.Î,Eû^F<Hý~\x0002}¿=¯/4\x0000:¸4\x0006t/ÏhÉ²»[ØxÎ½<dlvÞí£îX¥±s3*RrjLí¬L^k|l:;e::\x001aÜ\x0012b:o²R\x000fëóP¶ÄY¹²=pÞ¯\x000e}ïùÐö÷ýði~óôOO_þtY&E\x000eÊà»|Á¾¥81yéÑ÷Î¬æ<=ûíãÏÏ_.!Óo\x001e~÷ðæÇUÅ\x0005ZD\x001aFÌ\x0017Û\x0014\x0004±ÖÄ&ÌÛ´JªÌ Ú\x0016ÑÎX±Hæ\x0000v"È´u­x\x001cÑ·~\x0018Ñ¸f\x0008<á¦Èv' *#®ò3¡E\x000c£3@B¨¢49¨Òqïõ(al	ã°\x0011!ÕïôÅ¨"\x001eÿÎ©ELÃFÌWÈ\x0012Bá^!aåKùÚ\x00160¿Ô\x0014~e+á\x0015ÄZ»ÆY\x0011W-`3Oa§\x0018y^i½\x0018ÔãDt%¢;à\x0014_Ý$¯7ÉëÕäÙ3«t\x0013(r\x001bù¡òöö8×õ*÷õY\x0012|½@^g
\x0016êS\x001fD	JÉ{\x0015)ÉnûÌ	¼\x0017Z(Úo¨rû_\x000cå½º\x0013[oÃ¹Ù^&×2¹ýL\x000eT\x0010\x0007k}\x000e£4ÑèÓ¹\x0001Ú¸ñµë
¾p]'b]aª½	QFPÖ¡vç"§½6J-QÚOÄU= HN¦Yscv/Ã¹7PÐïºýÛn\x0016+ryµËT|Ðþ+Àí/wª[â°Ûr\x0008-TDòÆaU :«¾Û	©p¿©o~\x0002åtà\x0015\x0001XÝxx.äÝKÕ­*Ü¿¬ {yígÑ§Å\x001b`ª\x0000ÑL¹\x0003\x0008ë¬`è³×Uïm´ueQ\%\x0014A}ÂÖíåº,X§ÞBz»NçX«Fvcþ£\x0014mûPÓãÙ\x001a±\x0011<×â¹A<\x0016¨r®)×\x001båõÉl)ìÅó-\x001fÄ#/)ßl½*\x0008ã;Yï ]héÂ ]4uÈK>D\x000528M9ø¸Þ\x0017[¼8\x000fK\x000fÕx!tµ§oSås/]jéÒ¨ñ´±h1\x001e©ñ4awpåAïU\x0006Ý
Ë`¹§â\x001aAó«þ¼Lú\x0008\x001evx8\x0017ë! ç©:$9ú³¥»
ÞVþ7¬\x000eTf£A6@\x0015\x001fE4ÜµØ.ia¢G·-t>\x000f\x0006G¬R\x001fO\x0012Ôù2\x0015*ßÁ#\x0003:·\x0002~Ås5ç	Oò¬¨Ï5\x0019ozéõü-\x0013ÛNÇ?~þxYxkÂ\x000cq1IûEA_1Còë¹æò>øøìÕËªÐë¡V&¶(;Ð¸OXÚo3^\x000bY\x0008JvöÂ2@æZ27DküÒn\x0016õ%	-f¤¡Þæ[4?f4½-¥$sê-D\x000fbµ³W\x0001´Ø¢Å!´¢M½ ÙÚ¤\x0007É(Z>\x000f¡¥\x0016- !ú¶Wv\x0001Æ+½¼»Ñ\x001cQFkûNöÍi§X\x000e\x0001tÒ\x0002$M&³\x001d»ûÑ C1³\x0019ÖXÌfk0#uí`Ü\x0018Ô¼\x0017­sk0æ×xô±ö9×æ}Ô9¯lÁ\x00114êÐhÈj\x0014tZ)ìÊó=\x0019Ò\x0016[³1\x0000y/[çraÌçz\x0011Óá\x00078=ée\x001a¥=ü¬ â~´ÎçÂÓåä=\x001akã)èó=ÀFsÎ^´Ð¡!´¼/¥±É%Î\x001f-hú\x0004
tV'b?YçraÌç\x0006¯ó2rÄ¡ØÏ2è\x000f\x001dïÐù\\x0018sº>JQ?±\x0002¬ä|Å\x0016»ÙÒ¤lØy6\x001cól9\x001c÷Ò<ÌZçÒPîµ8\x0018¼;_Üµ­ó\x001f8æ?ø¹ª&qq:ÉN\x0008*\x0003áìMk?[ç?pÌ¤\x001aNr¹*¾Z_\x001bñ7ºHö²u\x000e\x0004\x001c\x0008\x0019«Q\x001b÷kxYoIÍýßÅ.jÃ¡°
êÅlhï½øÝP\x0003J¿ÑD²\x0017­sn8äÜ8})å?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¯Z!j«èHIÃ\x0017\x001aãbç¸\x0016ù\x001ft\x0010©\x0019ÒË&
z\±ûñ9ìÎûW|Ò)ÄUj
q¿¿{ºÈµê!ºTs©Ï6K\\x000emJÒkùíE¶ÁÉSûW#[5×CbÄ\x0018CÃF3È:ó3ÄµVÇÉwd¨Ø\x0016\x0016îÈÎ\x000fÈos¹iÛ![Z3L\x0012JæÆý¸d-ýz«rH\x0007r'fÁrYÚ¹\x000e¬Ï[õÕts\x0007jH(I EÍ\x0003káàÅÕ¾é:ÝëÔ\x0007/\x000c	\x001dläD*?ÚY6ºwä\x0008KNX\x001aÒ%(¢Ò1\«(ïú´
kwd(³Èë	Öì,+NóSz©ò¶ã\x001eiÛ`ÅÆs\x001b³áWkã@sX»!CX+}:\x001a%êÃ\x0012Ãñ]·=3?j½Nt\x0006µ\x001b\x0019GKÞi\x0019ÕîÐæµ>³?\x0008j}9¾\x0010ÔjiÄ5s7p9\x0019y­ò¶#¸®#É\x0018%\x0002:d'1Óe*£¦ËÀs²¡Òtê¢öyÍ-\x0017n£
>3\x0014<Eõ\x0018>ðXwbO§ÛÏ\x000c\x0005\x0002O\x0011Aît§I-Àjæs¹ÞeÛõ\x000e
m×¢­\x000bV-©Û@¶2Xw¨<Qz\x0015Uô½æZçö{êÏ9\x000e	D\x0015Ò\x000eZíÂ¨¯\x001bycÚ\x0004ï*æê¾\x0016oOYÇ\x001f2ø67V±4Eý£¢:°Ð£ÿSüMí8×XtÑÍuxVÞ÷ÀûBHOEìDFÅî­_v½ÂÎ_^åT¦Òöé7ãüâÇÛßÝÝ>|¾{¸\)ªs\x0015\x001e\ì5iè:xw\x0011¨º·\x0016ÔE-ù»1¨J>e;pÃËÀ
ü>5¸QëÂX4ãjlG;4Z\x000b²åÂ­e..ù\x0006Ëq
\x0019ÜhE¦\x0003Y8wHþ<9ö­ad\x001aRÛ \x0003PHã×±\x001dZXLOE\x000f«¶-üj;4R\x00039(nU\x000f86\x000f;ík!;­:Âª%+åè#v\x0003_s8?\x0004d;ëóÿ%Óãqö\x00153|Åòxt¸\x001f\x0004²¬Ô=x?Ú½¢N6D+dAZ¼²!½Kã©n)SmÇ¶@s»`s]Wq\x001cc·é:;Õ\x001cwl&S	¬t	Y\x0016£\x001cäÈ{Òh¹ÝÉ?\x001cØ
²\x000fÚØö;°\x00153Ø	ÓfÅ>[·ÃuGúVóx\x0016ÏM¹7gÐÈC\x0014Èðt½bM(×\x0014ìµªè\x001b°!I9\x0014\x0000lÓÀ5 \x001d\x001bMló\x0001á\x000c;06~G7HoxmùüÅÔbÈ³ó\x0007Æ\x001e\x0015ÒÌèì\x000eM$Â>\#3ìØÞÖR\x0017â3¢¶<Ä\x001böÔ\x0002°c\x0007Â\x0006\x0012\x001b\x00132÷a{­yOZ8£Ó/?à!Q°'2*øMJShÍ»­;ãºáÄÌTU^SFM°5é:u4\ü\x001cÊ@:¥¬9p\x000baf
vÝ\x0006áæ±å
[#¶¦3=Ê~0\x001d¡7Mlh[Þ±2.W]¶
ÚÓ¨y«Yã«ÜbµF?\x000fÓîÐ\ÔQèF|n#+»xÙ(uR"Þ±\x000f%âèË§\x000b\x00104\x001d¢A]ëýxG¶IÌ³ug\·*§¶\x001e-º\x0012Zvn\x001d{þd·å\x000fÇncKÐû\x000eß\x0017¹ÜN~\x000e£M\x0018:Ô>>ß|ó_þ¿Ï·ç+ÅÐ&p_\x0012ìY\x0000û\x000eÒÒ¢ñ\x0006cèÚõ«Íifâ|\x001c\x0007Ö\x0004½fv?\x0013-Oj\x0007ÒdÅf"}ô¼|/T\x0005¾UÍÐ÷±IM§ÊL´ÞPÛûÈwP\x0010r0ËÞ43Ñ>z\x0013Ñ\x000b=!df\x001dJ¡NRNñh\x001f½ÑÿòåyI)W3ôc¥¨\x0014 f"~ô<ñ!¼3_Ú¨\x000c fâ},nõ] sÏßonÏ«Þ43Ñ>úo½#«wû
y\x0000®´¾S´e&ÖGÙdìòOCpa\x0015§&ÿ:\x0016f"}b¡½H	\x001czc\k{óÑ7ñªâPÌ/Õ´ù\x001a5\x0013ç£ø­è\x0008:Û/ù¼dÜü\x001dÚÒ¢©Ë;ñëgÜè\x0016\x000b\x0019 vtæ°U6E~\x001c\x001bÖmhCµ3õø\x001e¥S\x000bêsRÝâ37TFsX¿çwd0\x0013\x001dßaóx\x001cÍó\)·\x0019·³ã\x000cEsA6KY´ãã< e#dwÍÞ\x0012ç\x000cü¨âõjtY\x0017¯_»NÁqîº®\x001b\x000e^&Z÷iG²j|¿§Ø¨+%·ã°Ó\x000c¢XÉçõôl÷ý\x00036ð·æ\x001aE\x0018Ú cUE_ÌÑ÷óG»âÉf²ãÐÓx&TJÙ/\x0006çb\x0000]©ßþMB¡ï/÷Uüîò¹\x0006òúãåÓ§»??\iNÆI
4£ö¢q\FÂè\\x0003÷ÿ±QÙÚ!6\x0012ª_xP\x0016·Í\x0007Â
JÔåôùUp´#\x0016 \x0002³m\x0016`à\x0014iíÙkÞÞ0£\x000cP=sÎ,ÌmUÍ\x0001N¾yG>Øxµ	Øß\x0013Ó:EíÙX½lÜß!·øºÍ\x0003%vYr\x001c¶yI½#W.yrú;0z\x0007\x0016ÙÌß/é\x001aÖ¯£\x001dù`\x000f®\x000cH G­ÅâÒÒÖÙ%'ö\x000cÂ§¢\x0001K6ÌW!£»¼d\x001bÑÑ\x000cÒEF´ÇÛð6ëÈÜã:¯ÉÑvdýÊ\x000f8GG;2Z ÃN\x0005Ñ¦ÜHù/\x0006\x000bÔë ffÚj Ýu\x001ck8m©PZv£å\x0013Ï,\x0005ä^¸\x001dg¢_k)sZdG\x0006:lc°}3I\x001f\x000eé×ó­Ëö´Låe ¯\x001bY\x0006dþ\x0006"°
ëõ\x0018M¬n¹iê¬*¼O*åÞ¢|HæÄIñ¨@Ò\x0016£á_`}{ôKWðªoï¸Â¸#É
\x0000¯­Ê1\x0007=s¹É4"]½¢Õè\x001f\x0016o=¦/Ð6Óy·C*PÛJ6GMýfÕ¿ä\ÎuX\x000c¾ùËíOw\x000f\x00128}ûtyø(ÁÆÓûò¿®6ê¨0tN:)·§\x0003²U«lR5³ôÖÂ%cýj¬x¯\x001f\x000cSð:µáí\x0007VÊ%Øì°U»²tU\x000eä8W +´üaß;Ñp:B&¡vçæuoÑÌ¥+¾\x0003Øo\x001dÐ&äòÎìw®Íu(B	â\x0002Ý\x000c<Ìwã\x0006}ÜADIô\x0001\x001d^·<-Co¥¥õÔ?ìÈRsÔ\x0019 ¹l¥££s¸½h«m\x0015Zþ°C[ ÚfEy	«ßå+ó\x0011ßÈ=Ë¯±å\x000f\x001d8Ã¸8\x0005\x000b\x0018Þ\x0007I8<jU¢xñ%xýÃ\x000e®´yk¡åK°à>4
\x001bsr\x0002ë\x001f6p_<\x0017Z¯°eb=O¨:\x0002oåõb\x001f\x000b_Úm\x0007}iÐR
JÇ7õÃæDé 9ÁÍþ.×`ý]Õ ®\x0013sº»}úóZ
,î\ÚY\x0014$îC\x0016\x0008--oðuX^\x0017«¹îé­UvÓ`%ð°è\x0016¤LqoòÜÔhZÂq²À\x001dúôlÖàH¥ÀÔYÖÕ,³MêLÏ\x001dù\x0010l+_\x0008%-d\x0017\x0007ñ¤»;Ö\\x001bñ\x000cd\x0006yC[Ü¨Æf;æ×u\x0002ÓÞ¸03§õeC(ðÂë<ÍÀ\x001eè\x001f^>ï\x001eèï_>1§\x001dè·¯þ¤ölíÆÂÚ_ôU§ér_\x001d>é\x001fúëåÓ§Û?þå\x001f+ïÓoß_\x001e®\x0015YySXwuôÆiëá\x001dìZõó­y%ç¿Fn[¶uHZ	É\x001a&ÔP\x001d\x000bixØ\x0006µ\x001cáÝáÉ¼Þ¹/îújÐaG\x0006ÚeIm\x001f\x001d'"\x0011Dt¥~Mp+j\x000e|Ô\x0013rÈµl\x0007¶û\x0013?ÅMZÑùwÜ#eÑ\x0008vb *L\x0005M«4MÝÛ;ðñ\x000e\x0000\x0006Z6$ÅhSæÇiÃ$Sûö\x000c)+éª\x0006d3&<2«¥Øô#G\x000ft|>ànLÙ¨\x001fª Ñf;|A]\x001bO·ØsíQ»Ñ*²°¹õgKðZÝÇó\x001f$YQó¡\x001aû\x001a£ç·ý{´ÏÁ?ÃãÓ»>ÅtËI%>×±\x0016Ê&·\x000cà¸+\x0006;ùÄÎ©k(êÑh\x001aãü¢Áº;.\x0013ùÇ´L\x0011×uÜ<im­µøÓ­ñWØñ.­ùðJw27\x001f\x000b?Ê8YSãÒ\x0003uã¹\x000fq%K\x0015ç\x001fn?ß}¾ùáùîóõø\x000f%GÙ­Á]:\x0006].©7IºôuZ¦²ã¼_ð,ó4\x000cI7é Æ¤W\x0014g\x001d\x0019çý°=R0ÛqYV(~W·à\x000eô\x0007\x0019¶\x0000;3ûy÷+\x001e}Id±#ã¼Â,4a\x001cfy²NWÓµ©âØ×"qx!U\x000e\x001cóøë0(5òÛY*}-%HE\x0006ª¨2ß±\x001b²jeäY*-Î\x0011\x0015I\x0008\x0001ôÀ_CMNL;2\x000c2±l¬0±k:t<6ËcrU¼éÈ\x0019Ö\x0015B4Y#\x00185ûeoË\x000eCeÑ \x0013\x0018Fb=xD*7)yêoÖ´jÈ\x0017WÈ|ÔÒ1â Í-\x001d\x0019Ð$´h¸äTlÅºÅNÏS;´¥EÃÁn|¢Ï\x001d®$Ê\x0015j$!ÕP\x0017£ÁÀÒ³[:°'SQ¬ßñÙà¹ö¼lnéÈ`*"ós\x0014&âH\|]`#Ü2gÐp¢E8>\x0001´\x001eSyZ@4>Vy\x001d\x001ax\x001bdð\x000c\x0012O">çh¾Ù«Áu4òæ³Ã\x0001®`ÁS[Z·ÉuX:vålTF ©oæðJ8sf3¶¯\x0005?ÈWéz\x0017¢/­\x0004v3}C¿
	îär¡ÖÆùr©¼ó:\x0007¬ü=lÈVT½æ+qT¬H´_<êgÙ¸ÈZ\x0008:0¯A±t2\x0006Ùo°¯6#ß«ø)Â<ÖÙÔUtÜ¼¸ñ/ÀÛ~êÅ\x0008ñâ\x001fn/\x000f7?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÝÝ>ÿåh fjçµ©¤}éÉ¹\x0017öÃéÛóËÍõÕÍ\x000fç§78\x000e«jX5\x0006\x001bRc\x0004k\x0003(+É³tzÍS?¬®aõ\x0018¬Ñ\x0014E-åw&_âÎîÏ7í55¬\x0019õ- ,	\x0003¥«a]{/X?¬­aí\x0018,Ø&w6p2àKR\x0003y¶\x000e¬«aÝ\x0018,Öo\x0011k<	O\x0002³îÏ-êgõ5«\x001fc\x0015jöTª@ã>³Ü
ÙÙý²ý°¡
÷óá\x0001Vö³=Sg÷§\x001duÃÖUÖ®TYwomäÆÂÆiM;kÊÎî®í5aK'2cúÕÃóã\x000f·Ï?l~z¾?f\x000eJOyÀiJ\x000cÏ\x0012+óÜm ¯®n®_Þ¼Þ|}sq\x001cRÕª\x001fR\x000b
0c_Ê\x000fµ¢Çe\x0010\x0010»ÍÆû!u
©\x0007v2Ò| -ð±º]\x000bJH72î¯è45¤éT®LNpG\x0011,åfóqM\x001f¤¯!ý\x0000¤}¹\x0005eÈòµW8±f\x0003_;\x0010c\x001aÁCí\x00047\x0012Qîµ£º +I[\x000cP
\x001e\x0012¬çéex[\x0014qWÁ>ÈV\x0002 SÎ¤Vô| b\x0019>âö§ôõA6[ÜnÉß;ÄÈ<\x0015é\x0001ß\x0015Ä¤´
¤í\x0014l{\x0004PçTsbÄ¸\þÈæjË»-$ï0 ÂItª´Ò~¿ÜGÙ\nÙ»e4<²\x0012\x001b\x0012ºÒ"geí\x000fåtAªæÞ¨þ{)Mf\x0017ïÁ®sÜÇ}¢QT§ên9I}s,§K¤\x0007
\x0001\x0016\x0007)pÉS\x0014WAßÞ¶BývDÇÜB\x000fHñÑ5KuÏªg\x001b´½¡Òì(\x001eQK}òåÐ\x0013\x001cQî¯÷;ò3aåv#3Y72;{xúùX3=\x000e%Eµ#©Ò¥k¦Ê8»úðö@'½§j<Õg\x0015WÀag[î§¬\x001d'ÅØÅxºÆÓ½»çi\x0008ÃHc`÷JÏQ?0\x0017ÏÔx¦w÷\x0002§ÄàôC{É:£ù\x0001ÎL¾
ÏÅ³5íÿ¸î%_Ìó·åWL?5ÎÕt®.xn³æ±\x0008^xIæ|ñçk<ß»yË·\x00026m¥O+¹M°|\x0015K\x0017jºÐI}xó<y\x0007ÊEîÑ)Ôd³¹x±ÆxNbv,Ü§	v¯ô>·É3ñ*¯@6]àfnÃ±Wyûxú\x000blå¯«&ßæòµJ£WkÄ@7\x0017¯â¯Ë.Pfêåt.^£4d§Ö\x0008`¿R2\x000c~éÜ\x0004NyL7àÒÆrO6ZCvª
<sÔ\x0006;uæw3à+ÝÇÕd®Ø\¾FmÈN½\x0002ï±\x0012µ½ôeÿöûÍ\x001d|Þ#`ËU.ØT*á)ÁZWN6×(\x000eÙ©9°(¯Ô Iªò\x0001>ËyäSSDæó5Cvª\x000e\x0010zÜ\x0005\x000e\x000bÌ\x000c}^Åxrw\x000en'^£:d§î\x0008JÊ_¬;WÈË¹lb:\x000f._£;d§òÀDcÁ×p* ×e0ÒtK|ªQ\x001eªSy`÷{ê	âåÙ\x0006Þì01Y\x00062¯Q\x001eªSy`v±foU*&«|æòµ.G¯öÐ@Qr/"ãqsâ8Ý´d.^£<T¯ò0
ûMçíãAµÀW¯Xj\x001b¨Fy¨^åÃdèøiËNwªä®,µLU£<T¯ò0«|Ò(Bº¾ÎrgÌË×h\x000fÕ«=·OQ\x001e9à\x0005î\x001a\x0011zEªQ\x001eªWy`Um)§"$ïCÙ½ÅÂ¥Q\x001eªWy ,m\x000fX÷r^}»\x000c¯Ñ\x001dªWw¹Â\x0015Z\x0016Ë/Ä®ºC7ºC÷ê\x000eç¸¥O\x001a\x001fJ¦AT¥õÁR¿M7ºC÷ê\x000eLÚÓåóF²
¢åó.<~4á¥ñ-«¼¸î¥å*ïhYB¿À\x0013f<*\x0004xmÈ\x000fVN{xöÓíã§»§ÍÛ\x001f?Ýß\x001eLªÈ«4nRÈm,îûÓ5Î¾>½¾<ÿ°y{õæòâô8¨ªAÕ\x0008(\x0016zÇrc´áòÅ÷w¤î\x0005Õ5¨\x001eÚQQävêA	^´Þ^³\x0017ÓÔf\x0008Óà\C¶¾¨\x000cMÚrÃ'^À{A]
êF@¥ä\x0018\x0003º(D^\x00048\x000es\x0005ÎPs\x0001Na_n\x0012>Gð@WÅqÂu>|¬9ã\x0008§\x0017\x001cé÷ØGg0ûÜ\x001a\x001f^¶¢iD6a©_äÖJ¯¼p¦GÜ^\x000b­´¹òräÎ§\x000c´ôá\x0015
\x000bÅY{ìGëýÏÍ½¶Á´#Òp \x001d{å½tö)Ðn}yk¶5%óõáîùñþt\x0004Ót
i­(]¤#7+
rNÉ«óë\x000fô§ãºÆÔ\x0003FóÃµëÜ½.Å-JíOÈëÃ´5¦\x001dÀÄv¹4*Á\x0006`Þ×jÿãO'¦¯1ý\x0000f4ìY,+Ï»\x0019JK8±û3\x0006û0C\x0019ú1Ád;ñ/I\x0005M\x000b2püRJøÏæã_\x000fí'\x0015³+D
k\x0003va&Ðý¥WsAßºCà?Ò\x001dúúùþÓ§»/GøÔÜÎal^qß<öoÚ«×¿¾¹¸¼<ÿx\x001cÍÔh¦\x000b
'P;X«X+\x001em\x0013Ñ[Bfk2ÛE¦Té_\x000fÒ\x0013Ciã,ökÄÙh®Fs}ßÓpO!g\x0014Jü=­-h{\x000fÜl4_£ù.4Lh ï©K\x0003N|\x001a¥»\x0010÷ç÷ÎF\x000b5ZèB3_æ±ïµ 4Yfì÷\x0010gÅ,ö\x0019n;\x001c£ªÛäSØ´ý)+sÑªQ@ãÑl
5¯C1Bl¥tðq¯JÍ&\x001b6ÙÅÅÎ²°àÕÆjÒýéÏ³ÙTÃ¦úØôKzË}Ý´QÜ¥ÞËEâC6ê@öé\x0003¯ù©Û	sB5âÖ\x0015´ýáÎÙhÐ}R7xþ¤6J\x001eø£½e6»ßUÍÖH]Ù%v±5¸Å ¡äGL\x0016f=¿ð*4bWvÉ]lo¹.0â×Me¡Ñ¬<6Ä[ÂÖÈ]Ù%x±-.½Xr,
6ÞÉ6Ñ.6X#veÜÕØ'¯Ê\x0019£C¼¶¿&i.jdêmÁO:8\x0010Ù¸Ä\x000f,ôý}òg³5²MuÉ6­\x0003÷Ýßs\x001d1\x0005mù¡\x001aÑ¦ºD6\x0001ÓÆ\x0010
.&^×¼müVâÂ26ÙªóãXõ\DÉæÆyökÀÛ¡\x001b±oò<D«¶â¿Vqü÷ë[\x0000ûr¬bWz_P|`7[)Wr &l¤S\x0000ûx°PWmÇ\x0001Tñaæ¡¹2Ëc\x0013z2Çq,,ÅP÷ë¹d¦&3]d`½qã\x0000\x0011Ùé>øû/ê\2[Ù.2lYHq|éy.¬åYÝïÍFs5ëBÓÛzâ\x001cAEÁÅ[´û'êÎFó5ïÛµâ-{Ð\d¹É¨TùËv-Ôh¡o×JÜÛak;Þ5Å\x001ft"ü9\x001b-Öh±ï\x0016ð\x001bµóÅïA¹$ûæÉF¨É>©öâbg\x001cÒ	Ò½LAÜ¯åç¢5BMöI5+X]ád2Û°Û\x001eâvÀX}rMØ\x0013eºòZ©-Öî²mkäì\x0014l¶Ìf\x0004å¶¯h0ûÛ`Ìfk¤ì\x0014\x001fÇÑ:Yjò£|j¹_»ÏEk®¨ìº£Â\x00174m¸Gxnº\x0015p"ò\x0010R[\x0011ð!@\x001d¿ÿtûýÝæçÍ¿ÿíóßÿöxû	óßÜ>\x001fï\x001d"¥.;cä\x0019t ÿè)\x0012ôÇ\x000eëûËÓ³óÍëÍówç×§ø¸ÿæôæp\x0007\x0011µm3©d3-AÉ\x0008SQÁRá~\x0017\x0012\x0007¯®kt½\x000c]¼\x00148xGÕhRs\x0016£»o	¹©ÉÍ2rØiÍmô\x0005§\x0002¨Òf]\x0004³sí\x000e OLsÈÜØO°&Çn\x000bØu\x000c®e\x0014:iã>fWbô£í÷BQÞ\x000b\x0001úÕßÿß/¿\x001e½¥\x001c\x0019U)­\x001b\x0013üý)67W§\x001fÿxèÑÕlÝA`S}lJS«P¸g«g%÷!ÿíÏ/¦k4Ýfè!X	£x\x001c\x001fv\x0013ÏhÊMdVÏE35éü¢4lL¡a\x0019Ë\x0007¥;£íþÑl4[£ÙÎ\x000f\x001a©+(\x0018\x001c»±áÌ»Ì<ú%l®fsÛ¦ÈTÒ\x001bîÁ%yp5NÝYöI}Íæ»O[vFá6§>Ð¡qbÂÄ§¹l¡f\x000bûF}Ö\x0014ððûËKSE=\x0004<\x0017-Öh±\x000fÍKªy\x0005!(\x001a\x0005\x001a±YµLT/0(wE¿àÍÂ-52àóF­h´hE3\x001b®\x0011¼²Sòâ4,:pÒ¾H^¶vÚßn.[#Þd§|ÃQ¨¹7Ò²¸	ûcýßl¶F¾ÉN\x0001sWò\x0003Kì[ey\x0016u\x0013EÖsÙ\x001aù&;\x0005æ\x0019­J\x0019GïC²\x0014+\x0019\x0013]F¾É>\x0001§Dù¦FÒÜÁ³Ò²a¢¥ÿ\¸FÀÉN	g,rþÝRîGoÜÄ8¹l}"\x000e'\x001ajÀ¦¸@\x0013 FuSÝÞgÂ©FÄ©N\x0011çE¾\x000b¢(\x0006Ðû,|'&$Í\x0005kl^Õgôb_(R\x000c8ó^r;#N8tzb\ñ\¸F¾©Nù\x0016Ón¥s{-ÁÉ#eoíÄø¹pÍ]P}w\x0001;H:oàðÅyf´sj¢jeögm^bò§-U\x0003seå¥C\x001a²	wK·~¢ûqFé·Ü-\x0010s%"òæù×ÍWwßÿtûüÃ±
ÎäÊç\x000fûüQódÅÔd£ïVÆeçðÍÍ\x001f7__}}zóú8¨ªAÕ\x0008¨\x000fS¬»Ü5DÙ¢8Ìa
ÎXsÆ\x0011NË­ÐâÅ -î6ø\x001c\x0000­ÕszÆ\x0000)[\x0008ItÓt\x000eÎ\x0000«o73·\x000bÔê­#
7ãõÃw¯\x001f¸\x0013WÄä|F\x0003zôÄo¹ô?Úý·èúêÍùõæë«×çGczë\x0002«\x001abUú®<Ü"Wº\x0011ò¸	øûûÃÚý°ºÕ\x001bË¥k*àÄ\x0004É\x000fíápS°~XSÃ±\x0005úüÆ(J\x0003õH\x0019OØTo8¡\x001fÖÖ°vlgI5\x0005\x001bÊ\x0014óÒá(ÆýiÚ=¤~;¹ØSrñÙOw?ßÞ\?SðÓíæããí/¿Ümn7\x000fÏ¿\x001cÉ6¶\x000eÇö¤}\x0016Ú\x000bUk¤&9 \x001av\x0013SÏ¾>»¹¾¡Háåéæãõéû÷çÓÍåÕÍû*ûøEÙm
fY<þñùîññöó\x000f¹<ïùûãå3|\x0015¡L=e<g\x0011N¼¿{ss~}}úîu®Ô»9;¨tí¶.³,%\x0006á8sö¹Cw"\x0002L¬öú@CÀº\x0006Ö£ÀêeÞÅj\x001eÊ\x0014²<sî¯ñ\x001fB\x000e5r\x0018E\x00068tD\x0012²1'£á:¹ßëC6Ûe&Váå÷\x000f¿lÞ<>üøùhæN\x001a^ÂÅ2](\x001b\x000c?;ªY¸7÷Wï>nÞ\x0000yw0Çl\x0017FX{P¥å÷\x0010\x0013@\x0017ÎZN?õa¿0*·ßü¤*U±\x000f¾à1xûüió\x0006~÷plX\x0015~âÌ£¨Nt.Á·±Ì¦h\x0012võîÃG<\x0007ïOo.7oàwW\x0007'\l¿öÉ!5\x0002­Ëì\ØfzPU\x000eçvQC°ýÇw\x000cZ×ÐzÁN«Ò\x0006\x000cujõÂEÈ°ÑûbcÌ¦f6\x000b='j\x0006°%u^\x0013l´©¼¿:q\x0008ÚÖÐv\x001c\x001aÌKGya±\x000cÇ´ååGý-Æ ]
í\x0016ì´Æ2ÕÜ¥-DÓaJ»ýïÇ C
\x001d\x0016ìtàúê <Í(.3Êíþ"Æ!èºË*¡ü!jÍm30Ü\x0006ÔÙ³v\x001aè\x0018t#ñä\x0002\x0007ÐÁÐ¡ÜÉª`îÕ+Ôf;|b|ÕeõÓÿç]Ý?\x001dMw\x0011Z¥õ,éR;
~Xjüq¹¹ºøpÐ¾\x0017ÛÎ³ ÀO²®~¼{úî×/wGÝ&\x001cÓ÷ÒþCq\x000bàÒ|Æï}\x0016»¼ÌÊúúüÃ«?~<¿>\x0004+¶§ä4%çâç_nî6¯î\x001eüüp,KÁãP¹
qÚMÇóq0Ö³yñöýé\x000fçWç×oÞ]Í Ô5¡î&\x0004_N3¡ÂcjrëÕRm¿34\x001fÑnûCÖV	\x0014×Ï÷iüÅ±m\x0002%p*8\x001c*)ã\x00191æ3õ\v}sF_\x001cºëÛ\x0011\x001d©ëCyÇå¬¿]\x001a\x001e¹æZ`1\x0013s\x0002 Ü;d(\x001dÌó\x000f[Õ­ßßþpûô\x0005.\x0003ÿf\x001bZ×Ðz\x001cÚhÔ´»â¥Fgo¡ø ´­¡í8´³<--\x0015\x0016).\x001b/nÅ\x001bíkf?Î\x001c9i	KÈ½ç\x0012òâ\x001eïóF(
n³ \x0012í1j>Ð©¡[f\x0016¥ |o#¨^hµÝãZ¥\x001e×§¾ûüÌ3ÔÞÜ\x001eÓ\x000bàV*.ò
8B/	3\x001dy^»ýTO¿9wÃóÓÞN8JéjJ7B)°]_¢ÄÒòHeÀzÜ1\x0007\x0006(CM\x0019\x0006(µãö\x0011A8JÊUZó¤káv+\x001e\x00070c\x0019\x00070½ÁÂ\x0016G­Í©\x000e²§i?e]\x000c»$÷ï¦ä©õ>JîÖ¨KóÝ\x0005\x0003ª¡T\x0003¦\x0014É\x0005Ý9\x0013¥á÷\x0013l%±\x0002§i8M?'vØ¢Î;Î[
¾miÎ°g¸B\x0017çvPTÙ*úõ&ë.\x001f¸ÏC\x000fÆÌ\x00035\x0018W8¿YoÍ½ØÝQ2^Þ¤XÝåÕÍëóëã°¶µC°pmÈûVØR\x001b\x0011(~~\x000e\x0013åþý°®uc;«¸÷¸Âðxîð¨qr.í¬Ú\x0015£c°¡
°\x001fÍ\x001dæ¶\x0006åáAL¦DtÂÆ\x001a6\x000eÁ\x001aaËà\x0012p´(ÇÕrí\x0011~K³nØZ¬Ú:Ã¯kkµÈo\x000eÊ¡*pôÊÓ\x0019\x0002úZ\x0005V6°rlku\x001a\x0000äh\x001a\x0019eb¥4¢üÞ7Ñ§¶]rPxåvI\x001e(S\x0017¶\x0008Ì{;QiÕO«\x001bZ=¶·à\x0006H÷Ö\x001a.tFðÞúÝ\x001a1ZÓÐ±½u¡LrÇ\x0010Z,'Êï©r%Å \x001bÅ Ç4\x0003\x000eyö\x0001 4{[ÎS"Q\x0013#è»a\x001bÅ \x00075CHõõ9·"rû\x0015Ë3ÿtt\x0013Ï»i}Cëh£0¤ÇÒ¸dr\x0019E\x0001\x0003Ø÷ÉzNÖFÉA5\x0016}ÙY£ÊÎZ~S@{l\x0015ZÕh\x00065¨\x0019<Ç5Ò\x0008;¥m%õ÷0à×¯³·ª5\x0014\x0007mä..*H	ÄÖ\x0000RlbÖF7l#½Ôô2¢d;µÍÁ:Á´v[~ÚF ¨1rwÉ q\x0003\6ð$6±òw?lsÇÔØ\x001d3`Ï|Çbphã8â216®U77LÝ0LïÍJL\x000bå¹ìßi\x001ed)÷¤ÕÑ67LÝ0\x0013T\x0019O\x001c,%\x0001\x0012+Æ×D?\x001eÚíW\x0003^
ü%"poð\x000f×Ø\x001aõh^GºìíÇeT¨"\x0004g½ÜÅÆÜ¥w½¤S(î
þ!õI=ÿx|\x0005º^^¼\x0002,\x0015Êq\x0005cyº$4Ïí[Ôî
\x001c_ÙÎ²0ªzux{ûø÷¿}ÿ\x0013,ãõÝ§Û/ð\x000fbÜáãíÓÓý$ßhçLi¢\x001c-µEPV²E,L:ðoS\x001eÙåéÇ×)
ññôÃ7ïþx|!ª^Zg!\x0018Ò£´\x001c,¸v<:IëÉÊñèz!z¥/\x0012y¾³Ä7¹_²%b5Ñ3xÑ:L½\x000e³Î:¼\x0015ÜÄ-â\x001b,Í*Ó\£#wk±\x0017¯ÃÕëp+}\x000f ¥¡R`Ðò
yñ\x0019E4ºÆ\x0017\x0012ëÄµ>\x0008\x001c,Òâ ø·3ìEÈý/LC\x000bù\x000e¼êoÁS+^û+ìÆþú÷ `ßß}¹ÿò´9}þ|l¦\x0003x¹\x001eðµÆ6\x001fT\x0018U-IÉ\x0019·\x001biBúþüãÅÇ\x000fÓwçÓ\x000f5Àé\x001a\x0004\x000eEÒåíæýãíýã=ìðÿç}}ÿøt,-\x0002~è¹Ñ»´©Î
\x0002ÿ¬\x0014Ý¹¹§÷×§\x0017×\x0017°­¯/®ñgûYñ\èz\x0006EþAÒ\x0003\x000fÏ_ÒAãq÷ªK\x0013¥BÊýt÷ü\x0017Dée1m¦q\x0018\ÂLSøCÌcq\x001dè]vÎ¾º¼8¿ùÃï¯¯n>¦/þöôúüÃT&`Å¦j6ÕÉ&s"\x001d°Å4=±Q|Ã´ÛEpºÓÝ\x001bç2vø}\x000b>.Ü7[£Ù>40¡"}Sºe&6§8ì#dÁ¹\x001aÎuÂù\\x001b:\x001fä*yã8£sÍ×l¾
Äyª\x00021Îú\x0014!Nl?ªâ¦\x000c£l±f}l×
h,±éÜÝ\x0019à\x0004w\x001d­\x0014é\x0014#à\x001b¥*\x000f S
í®Dgè¦zï8ÙÜTÙyUµÌýk@3àó¹'¸E\x000ctF~W\x0011¶\x0004°\x0008\x0000~õ÷¿}ùé\x0016þ©çÇàEfÂx)ÀË_78úº
§yíG|uþñëÓwgW7×38MÍi\x00068­É½¢\x000cúØã"Kü\x0014
\x0012¹ä/Â´5¦\x001dÙÎ\x0010ó+/ÖV+\x000cè¥íÙ¡tJL^.NWsºíÔ1·b\x0004N\x0017^$µàý,õ8CÍ\x00198U\x001e
\x0001!àÛ~\x0016¹I:ì§ôË1é­o\x0018áTY%\x0007\x001f@irò\x0011@jv0\x0016QªRPÊ²Ã£ÈvP¹T\x000b@]°kæ6	ù\x0007P:»}þùáóAÄ41oÚÕ\x0001¡\x0003@CçÒ¸syvzóöêÝ\x000c:UÓ©N:år\x0019\x000b`\x0004Oz\x001aL\x001cöFÃÐN\ïÙxºÆÓx.æ\x0014IØ=#Hß8åYßD?q\x000egÓÎtÒáË¡¤ok0->ÑYoùÛN¾Ùx¶Æ³x\x0012_PÅ(¬WKxÑ±Ñ\x001fÌ&çj<×çØ'ñÆ1\x0016wÏ	
8\x001bÏ×x¾\x0017qPñi|sÍxõ:r1öô«ÐB\x0016úÐ°\x0008w\x000e.¤Ó1\x0016]7¡DfïÜKï"õRë.Á§s\x001d\x0014~ß\x0019-éø±\x0012X^»ôømSº~J¯ò|\x001c Ô©¾:Q\x0006Ån»3\x0013öö\x000cÊmV¶&íÙO·Ï)´4­ß¼)1O ¸>,µº¿_Þ¼ªØ¬ÈTM¦ºÈ%¢\x0010+Ã½È>%§nïL8]Ãé¾m*\x0017*à¶YVºXøÊ;§¦>êL8SÃ¾Ã±=\x0014&\x0002\x0011Ñ¢`¡,'UÚL4[£Ù>4åøÊ&kN\\x0010|eÕTHa.«á\\x001f\x001c¶æKo´\x0008'uÑ\x0017eDý(\¬áb\x0017\x001c*XI'ÎªbGYCîGfÊ\x0014\x0007'[)Ò'F|°h$:Êt\x0019×\x0010ìBºæ²Ê¾Û\x001aÌÓ.r\x001cËæ+¡-_à'mÐtÍ}w\x0002þë'è°ÿ^rØQ%ZäÄ(Ù¶ß®ì\x001e?Ý>øY£Îe- »b\x001aà6NªH6²[²\x001c®n./¦ª\x0003+0]é\x001e0PªÜ2Pªl\x0018âÙm¥Ú\x0007fj0Ó\x0003ÙsüE¯³?\x0001þ¢\x0019â¢ú;¹êëìþç»/÷ÿ¿)Uý@\x0018åÀ×\x0014ibC\x000böutûàÎ.Þ¼.P¬øTÍ§zùDÈO0¨\x001c\x001c]S\x000búÊ\x0015Wq\x0018Ïlo_Ý;ùì9õqùpûýAõà_Ü	BµC\x0011"Ñí¿\x000bg7©cËÓ³ã|ºæÓ½| P\x0003»;\x0012_\x000b\x0013 sÝíÊL@ýíýO¹ýÂ2Þ§ÍO¿~\x0001Ï\\x001a¹î?}úõw\x001fnï?ùÝWh #!ìÄ\x0008\x000b`ó\x0001\x0008\x0015ðæ×XØ`>\x0017\x0004 w\x001f7_]£	z?lÞ\þñìâÝä¬÷\x0014\x001a&5)1+Úì:\x0002©ÎG\x0011\x0018Ë5Qá»èñMÍXÐ¡Óf\x0001
GBñl®U8AvqÎüå­\x00129_ÞÐ~ÃéWä\x00049a9Á
Du¨Ø¿MfTó\x0002ªe1´
*¨n\x00145M­\x0019ÕÚ¬\x0005q>ã]5,VA/äwÕë4-\x0008Q1\x0011 æ]ÍÎ\x001cºUIÁ1\x000cÃJï\x0011H£YóQ
6ð*¡éUPAÄñ£\x001aFBÔà³ÕGµìª_óVa¿TÅôo«a5iÒgÚV£_¶uEî\x001c×S.½¥mÕ´§·+WÁ\x0004á,\x0014VîZÚÑÔú4ïhîD;\x001a×üúpèå\x0002%å÷ª*úÔÊXêÛ
JJ\x000e+*ZêHª:JeIS\x0007%³®H
ÿ.9®ªDòÉ\x0014§ç²ü\x000fO@©0_\x0015ô\ «\x0002ïª\x0013eU¡YCXQ¬â\x001b§\x001cWVÚ¤è\x001e²j_N+\x001f\x0000°ýÜ¨ ©ä°¶Â½$½
¦>RçmÍ!\`\x0015bÅmÅÒ\x00175¬\x0002ôXöXUÄvI5úÀûªV4Vñß¥Æ\x001d\x0000\x0007/"«ñÅU¡w_x\x0018V¼ZX÷¢\x0016XÖ"ùõÈá\x0007öªH
ÄÒ¥l\x001cU=?ë?×\x000e`n]ß>=ý:RÃ×\x0007k\x0017)qÀZ¦4)MTV9Øu}úáÃT¬«\x0001$¿¯\x001f\x0010?yæ\x0001Q\x0011ÐH\x0002
léÉmì$$7ª0ÈTS\x001aðÚ§iÇ	Ñ\Bït\x001d@²ôû\x0001]ùÆB\x0007|öJVÒG\x0005LÞðND2ñ»\x0011
¸É!ÉvÐóÝ;øºd3+oÖB$Ó¾\x001bÑ<	< Ñ,q4"b2uFvÚ\x0006íC,&}?#*\x001b\x0018QEì1ì\x0018E\x0019·Mù~F,îI2\x001ch=V$}#òD9ìz´\x0016"ñý`kæ¸\x0008Ü\x0011uB\x001aÑæ\x001a0l\x0002¬&µ÷\x001cÄO?\x001fÃc-¶ïð¹úÏ\x000f÷O)Ýu¥µñö$gK\x0000Ò\x0008?)¶Ïññú«\x000fí\x0006Äv7 ´i.\x0010\x0002ªfb"¡2¤©u\x0014vÒ±ø¿Üþdìvìóysy\x000bó\x0018±hB4\x0011û\x0018%¹íáÉFÕá°§v³¹<\x0005Êë9UÔ³Q\x0008{èÁPÓ\x0019R\x0018º-F¹O\x000fd\x0015ïìÔ¹y%B:áî\x0004iòPQÌ¦·\x0007m\x001eÈ*ØÙ	é8xl\x0005HþÜTµJ\x001dô\x001fz «Hg/¤¤0Áé 'Ñc´½U³\x0013\x0012\²x\x0014rn"ðNêõ>w\x0015Ýì\x000cyn
îd9§\x0001k\x0017sB=¶E_ïâTÍ>È \x0003¹´\x0016\x0007·»|q¤s$À\m'«fçNFÉ
[Oc"ídNY<òêÒ\x0001Ù\x0004\x0008{·2u¢Í\x0016{:$JIî ËÝCY\x0007Ý:)EL=\x0010\x00129\x0005)I-M>ípõRÖA¬NJP¥ \x0008\x0016ü\Ð^qyÐÍîÒß~¹{Dí\x001a9Â­\x0016Û\x0013\x000f§ zðÙK)ã ª~þç]«ÄsÌÔîñ>Ï!e\x0012Ù4K7½^+\x0004&#Uu\x0001\x0007îQîúÒ]_LO®«Û4H.Oö½Ñ\x000cÎ:z\x0019\x0019Ø\Øµ_.Ö\x0018°\x001a\x001b\x0012&bW<]é9\x0011×Þá;6\x0008ì^­ÉUK\x0000¬m8\x001a\x0019\x0003õÓ|ÃÁ#¡tjÿÎ\x0004;\x001eJ\x0006ÇGÂ\x001e\x0008\x0016\x000e\x0000ã\x0003ZtÿGá®ÕÄù\x0007/é2ö?=?ÞÏ=\x0017ZRÔ+ø\x0012ç\x0014\\x0013?ý.O\x0003Ì\x0013ó?Ý\_Ì@V5²Z\x000cFu æáïÌL
\x0018'\x0003#Ð%\x0005¼ã\x000fFÙ1
ª]cSËÄîóH	d²\x001dæ£Çúé_kERÕ_Þÿu^h"80Æd"õ8±5\x001dgÕ\x0013\x0019Ôh1)0ªÌù#Õ)¤?î\x0012+8Bè±WË*uJ&hB4\x001eL\x000f!ùc{Û\x0001#¡7\x0014%M$OÐ8é\x0019t\x0011¦#
MmBßVº4 \x001aAm\x001aõ@­¤ci¼\x0014^GIP÷ñOU\x0004Ú÷=>ÜÿeóêîÓo?ÍÃ:P¸\x000c¿2="ÚÈ^\x000c\x00186jÊ\¤\x0006>g×W\x0017Ø¼:¿üæôò0j¾:ã¨¹1aBÅw4J:Xò3uºQó\x001dZjR\x0007pDÅ.\x0018´«¼§V¬¶§ù*-\x0000\x0014»w\x0006\x0007mxÚS~ïö*LÝønÔ\x001cXYª°î\x001fQutgS\x001bÍ*ÌÿGÝÛlçu#Ù¯Â\x0017(. ð¿jDË´E/IÔ¥D¯Ì;ÉEÛ¼ivÛ¢òfÖ¨^£¦=éÊÕÓ~\x0003¿I=ÉE\x001cDà\x0003>ùà;\x0007ªÒUù#S²s\x0007\x000e\x0010;\x0010Ø±vôwCMé~¨X°:QHO\x0010TÇÏÝN¬>wï,\x0003ç?,\x0013
àñÎ?\x0005±N­^\x0017wCM©U\x0005\x00065¶nÐ¢ò\x001b÷ÅYHS¾e`«\x001a~>Véâ?\x0017<ÆÕ]\x000b§öBå÷¦!¬ô\x0002ª´H-x¬\x0002c5zÖ\x0006à;í\x000bé\ÅX²Yè­èB`a5a°\x001b+=@
`M\x0002l\x0011+øe$yÚ\x0003ØÊy{®ÞC{@'×
xõffåzãÃZ\x000c½\x001b+\x0015
a¥ò\x001c@9\x000e¦VA4`ìêµ{7VÊ\x0010\x000c±«Mì
ñâx]ùIwâÑ¢J²\x0011¨	g<b£\x0000Å8ñ2	(u\x0003õÁsÄ"ñ)±æï/W«
vc¥:²\x0001¬r±VZÚõ\x000bVásZ«/B»±Rrh`\x0003\x0004æ\x0001cgÙ_iê$Ñn\x0016T.y\x001b
\x0004¨Lê¥ã?E\x0002v³N\x0015'°\x0006¢+\x001cR¾¿JªU\x0018\ñ¹Òa5µ\x001b*Õæ
@UùûûEùtÁj\>Wó°F2!¾ÂvlEþÊÒ#&buì¯Ô´ÍJu\x0003XaiøD¬ RÓýU1\x0007ØYq\x0000vÑÀ\x0010_)à*Ýxîq4DÂÊõï[gÅ\x0001ø^\x000fC6\x0012T'QY5Aõ¼]×\x001f6wCt\x0005cw,CÁ\x0000¡XÙcY)¦aû\x001e.YÙc-èdYMe×[uvC6Ã\x0010c)»h).7o.ññ-kZê
åÓÕ\x0010eE¬Ö\x0015çÐ\x0007f\x0002Ê\x0008X\x0007cQëß~yÿî»weíñãÓ{\x0012É½{ØX÷,p>Xr¬1¢FIïåIä¯e¼kU×8\x0008p\x0011Ç½¹¸zó\x001b\x0010ÿ×ý{õÝ÷E~åÅýÙ³\x001e?Üo[Ã ¹äËb¬*u-Ð
ºÈ¦k_ûÅåÙ³\x0017×o/kÝþUÿåÿËÿ.2©oîß}àW¯p¶|úå³\x001fï~¹ßúp\x0015ã>IµÖ\x0000uùãhn©¹t5«òæòÕ[~ø
§Î§_>{~ñ\x001a´~Ã\x0004¨êÇ \x000c±h\x000b,Åï\x0011üÏ¿lÜ\x0002\x0012wª£-`¹­\x0010¸<Ñá4éÆ\x0016Xß#Ø¯×Kß3`_\x0002ö½qFAò®\x0001GEúi>\x0002^wY;\x0001F\x001f\x0001^Ò.½©u\x000b^º\x0014j%^
µ¶"\x000cxô¦ióhÞ×\x001fÿ|ÿ!µ¿Gdg¯\x001fî6>¶)-©2Ëúx\x0011\x0017ic\x001bÎ\x00148áÖß°n/Ï^ß~}ù6µÆão¼¾º¼Y\x0015\x0019(Ò\x0008\x00186B*àÆIo$¥â\x0016§B\x001e\x0017ý]«r«Ó\x0008U\x001a¡ÆÀ¡¾á`¤"]\x001f²\x0011ómÐ¥
z
ÀGy\x0000ªªÑéf5.\x001a°Á6	68¦Lo\x0004Õ*Úåï¡ïÐ,Mí4ÂFØ	FEúyù\x0010\x0001\x0011ô¶\x0012ø\x001c»ÉF¸q#LÎ¶ \x0011k´\>Öë­2ýFøÒ\x0008?Á¥\x0006;\x0019á¹!	¬Î_¢Ù}ØiD(\x0008ãFXÃ1\x0004J¼Rÿ\x000b*\x001fëùGBÖL7NuÒ-­\x000f¼Ø9\x0005)óvú\x000cVTT''ps\x00144{­\x0000\x0010\x001aaØ\x0008açóµ¬¨NNà:\x000fÔ¾Uº'EÕ?ÓÉ\x0015ÙÉ	l½4ìBÑPcü\x0016MÅN+*º\x0013ø.àf#èz @A6b¾
\x0013lð¬äQêÙ°\x0011\x001c;f§F§\x0015ã^6\x0006¬¬¨ä±½>9(L±x[« Ï
\x0010¥\x0015Ü¹>bMIg\x000f\ø\x001fonÔ­çÄúÃã	\x0015SÀ8S	çô|æ!\x001d\x0008-\x001cðWh\x001buPßÆiBÉÀa\x0007Î=\x000bÉÃê@¯jNØÏ\x0010ÅBÅ\x00130Î\x00131ÄÈ{$&4Í*\öÒ|ª$`$T¼Òó6^°µ¦yÏ\x001f¢ÝUÔiEE\x00120N\x0012ÿ-i\x0002¨î\x00130~¡øï±¢¢	\x0018§	-Õ9±\x0010TbQOöÌ-ÄQÖI\x0008Î:}s÷®È«F[\x000b¼ÌW"ðT-ûvýæòâUO¿»Á\x0000(
Q\x0003d
\x0007;\x0005­t|»wV¸Ñe*
PÃ_@ó{+
ÿæ/À	3ám+þî2À\x0006	\x0006°W6©ï£\x0001:\x001b §o![\x001a`G
w\x0007Ò¥òBRE)öII>Å®*ë2À\x0006¸á/`¨\x001dÍK8ç
d2«5µºàû\x0012¾\x001f^óS|%\x000c%¿Æõ\x0017-7Úe@(
\x0008Ãëo\x00179ñe\x0003\x0015NÔr¤íV«§{
8¼,, &|t\x0002p
	ð	à§X/ÿí6 ¦±q\x001e³Ë0íå\x0013Ð ¶å\x00130Ù0ÛÊÇä0y±Ìâ]¾ä\x00085óÉ<\x001dy\x0005\x0015Éq&3\AJìý\x0010é4Pd\x0010¿\x001eÆ\x001fX\x0016\x001cRéE\x0001#þ\x0002fú)¨L\x000e3\x000bÌd¨ìÎÁå´ªhklvYP1\x001c§2MG Ë.ÇPHå#0ý\x0010WL&Ç©LÓ\x000eJiz:Ã×µ\x001e­ÛÉä0\x0019Ï/8woe&\x0002½ZÿÙk\x0000TL\x0006ãLK\x0002!ô6§¼TS\x000e·\x000b~Åc0Îcú\x0013\x0006ò	h¦»\x000c¨¯cã4¦¹\x0018Ë\x0019Åol2?\x0014Æ¿}ú'¨h\x000ciÌ\x001ch þ£9uØCÓ?AÅc0ÌcÞâË2h,{¡À<Ö\x0010»ëµ ºQÂøÒñ\x0014n"zÍæ°f\x00131TD\x000cÃD\x001cï1Ô7ïÉ§ÀåS ³#º,¨\x0018Æ8Pf\x000b\x0011Zs\x001cI4¥ºðWL\x000cãLìYT\x0006
PäI]>ÆmA¡.\x000b**a*ö+©pt`¾\x000f0þuÀNüªbb5ÌÄAæ`TÙâ\x000cð\x0017\x0010ë½\x0016Td¬É8ÞÃèÕÃ©@ò}x-æS,[:?}\x0016Tl¬Æ³£ÀÏNÃ7\x0008|Åjao·\x0005uvt}a¦nÿ2¤\x0013Ósª¢c5LÇÁe\x000bP,ð\x001a@ÃºªF¯\x0001\x0015\x001b«a6ÆÚ
>È2³±uy\x0013é\x0007¹¢c5JÇRH®\x000eq2«ùcI>}\x0002?\x000cTEÇj}ÖHs(% 9¦c:\x0010«=\x000eÝ\x0016T¬F	Y
Åõ¨Nøh\x001a]îã7X×¿éµ "d5NÈ\x000eÕ­Ó78D¥Y$!\x0004?;,Õ\x0015%ëQJÒ°\x0014Uü7?Õ@\x0016GÃf[PQ²\x001e§äÀ:qÝ9(r7ÑüçJ]1²\x001eed)]\x0011Ê-	Ò]\x0013]kV>vYP1²\x001eed)\x001c*\x0003¤MdÒ pX¦§ó&Z¤ïµ bd=ÊÈRrÝæb\x0000U÷Ë<0\x0005Û[&\x001bP1²\x001eed)t\x001eM\x0012D¾á\x0007ÍÈÎ÷D\x0015#ëaF\x0006ÀÖâÅ\x0002gr\x0008WNØ`óµº,¨\x0018Y2²\x001fý¬Ërý òÈ\x0015c§[P1²\x001efd0üâXh\x0018\x000fÀa\x0012K}9Ð\x0015#ëQFà¸KÕê3ìL¡YÓc©\x0018Ù\x000c32\x0006sô	45°G\x0003X\x0018 è¦Jo\x0001\x0015!QBñRFõ6Þ0)[
8\x001e/Y W;\x0004»-¨\x0018Ù\x000c32v¬¥µ5\x0007¨â¡¤A­\x000fèµ bd3ÌÈ(KÍª\x000c¡\x001d?é7LSW\x0010
óòh\x0017ãÌÈ[zXÕè¶ â33ÌgñZih¨UP°\x001dv9c_XWI½¦ÐnÔ\x001cËVóâFºËçÞ}[vØáÆíÀ\x000fBoÉ8ÌÕ8þ 9ÀX\x0008í-*ÇÈ	ßÃf¹;\x001f/4u~\x0011ô»«»Rû±\x0011BCÇÓ\x000f°¼ôâ/÷ï9ogÏ~üõÿùp÷ñÞþ%²\x001bg\x0006\x0005-i\x0006
t{uJ\x000buÖâ¤o/_-#ß°#ûíåÅíÙÛçX$»>A([\x0001¥\x00150nõ\x001ftÈ­ÃU¤ùF¨Ò\x00085áSxÃ!«D9BH"\x0004Ë2T«¨\x0003VèÒ
=Áxu°\x00071%ÚO§\x0005\x0018¹:jÀ\x0008S\x001aaF\x0000ì\x001dãØ[¥S§3ãiã?Ãr¥\x0015n\x0015:ë\x0005J\x0011¨êÎi\x000f¬Ò¯?Ç±\x0008¥\x0015a\x00158ë9mó'\x0016#\x000c8\x0016\x0003»æa\x0007¨¸"¹ZüÁðá\x0011,¿àX¤àèT4\x0005ÜV+9G¼í±10Å\x0018\x0017÷\x0014
áUñ\x0014h	ðö²z5W¶nÌo²ß°usÅEüÁ¢ýý\x0005kÞ|üþé~«r¾\x0017ZPÆ;\x0017¨¤V/"ï=²öêåúÙU\x0016©ysûìæ²%C	\x001cú»\x0010$]|p´uÞ\x000b\x0002Vó\x001a]ÀU	\¬¸á×Zeü\x0004ÜYzäñ(o?\x0013¸.ë\x0011àÂÐõmQ×V<\x0003òñVÅ{\x0012¸\x0019Ýã>­8x'´#9\x0005zg3qÛ\x0012·\x001dÁm\x001e\x0011¼\x000b¤#µsÔ¸\x001fwÊjò±\x000b¸+»\x0011à9Ù\x0012ýA£\x0005¸²¼SÄº>o\x000fp_\x0002÷CgÓeàRÐÁx6¥\x0015?\x0013x(\x0011àà¨\x00180î
W\x0018ÈÇXtUMª\x0003wîêHô#V%¼O"Xq¹\x0019¶÷«E]°kÖ\x001c¢M·EÚ(ÎåõtEA2s£È6å\x0000o.ô\x0003ä\x000b-%N´c\x001dÊè\x000c§n5å\x0010mbæV\x001cå'6\x0005MþÀÉ3W¬)h\x0013/\x001fÄ>XE[Å\x0000o\x0015|ÿ¼¢M9ÄÂ\x0014¬\x000fRS7}$|ÏÈÝj«L\x0017ò8å\x0018s\x001aj\x0017F}®ñ\x001d\x001fÏÈJ«âÀ=È+æ\x0003ÔépÖiÊ},±i\x0016¶Þ³'b&ò:å\x0010w\x0006CåW\x001e«\x0010SÑN=\½dw!¯¸S\x000eg\s`\x000e
8TÄÑU\x0007±ZIß\x0003\x001c*\x0016\x0001\x0016rÁg\x0018pd\x001b\x001dPKÏrñ\x000e4u³@åÍaÀÇ¥
¨¼ \x000f·¹¼äz5Å×¼r0à\x0014\x001d&'S5î@\x0015ç\x0011yÞ,fUM«\x0007¹ª¢\x001ap\x000e\x0007R;r-uÀ\x0010¹â5_¼ì
nËÔ\x0011å)ð\x0007CøyË\x0018\x0012»ðÉ3"ü©<ê?ïð{)\x0005½½y¬	£=ï5iXÄ;Þ{hÜêè$~a\x001eÊ|ÿþìùãÓûwï\x001fî6JÕFÂÇpkIo9n\x0012ÁÖ\x0010Ênùö0áË7gÏ¯oÞ^¾zsuÑ×%ÔP¢~ÔÎÐn±*H*DÑ"²çµ9Wx'jU¢V\x0003¨£K¡¼¨Â{\x0005­5põ)jßM­KØz\x0000¶¶$\x0008§"%\x0005Bíøe\x001fö'¢6%j3ZZ®	Q>Ó%Î	Å²Ö7\x000bÆ÷Â¶%l;²Øá<¨¼G\x001fAù\x000cÈ°CçwÂv%l7\x0000\x001bûlpµ\x001dm\x0012Í)ëÛ\x0003ÞwÂö%l?âGø*aU\x001eIj7|"]S=s/ìPÂ\x000e#Äp\x0019;:í@þÏå=²Ê5\x001d¨\x000bMt¤\x001a1²Ú!OÍ³ê¦£OÌ'rýå·\x0007vÍ\x0003\x0014Ý.£æ\x0013é³×n\x0017Kï]Q¤\x001cáH«Y£W\x001d^áDàiªÖ¶
²öÂ®8R¤aÌ<Z;®µËs\x0015ÝÌ-R1¤\x001c¡H§x\x000eJ~¨ãÌC\x000bÛeÄ{AW\x0004)G\x0018RC\x000eý"PE>Ûfª1ÍÞÈ½¸+#\x0014\x0019D\x001e\x0012©4mã\x0014pÆ­gr¬(Rp¤U,²¦ôlB&\x001bÓl\x0000Û»âH9@ø)ys\x0003;\x0012©³#iW±íÅ]¤\x001caÉè\x0000\x001dãVõæ\x001ex.'â&a&Q÷w\ïôNå²\x0018\x001f®÷DÏ
\x0015OÂ\x0008OZË\x000fJ\x0019\x0001¥È\x0003Qõê³I\x000fîú.9@(FÒo(\x0008ªy½=Ç®¦ÙÏµ\x0017wÅ0Â*\+Ð9æ¶\&kÛ5ã{qWd	\x0003déã5q+G°q½s\x001d£ö3×»âK\x0018áK%¸rQa\x000b2­·Éw\x001c=ÕT|	\x0003|éÍÁR\x0007br\x0005ã/a/\x0015ðÌ\x0012\x00052÷q½\x0015ûoÕT4Ü»âK\x0018âKwîm®\x0018K¯°q½\x001dãnvöí]Ñ%Ðej«_`KÃÕ Âä{NSgb'lU±\x001aa\x001d\x001c¿I5ÑÜ?Z¼Ø°8î]§\x00027×tDÜ6onÖù¸'n\x0012Uù@5tgPç if

[ò&iOtÚ»ò%jÄèw'Q?'\x001cÏµÐ\x0007±\x0017vu&ÕÈ4\x0007×\x001d]`\x0000¾\x000fçi3³º:z(\x0014T\x0007×­P\x001b;Þ&&M
Â½¸«S©GN¥\x0013õÖT¾3t2å4'nlÅ-µ¬\x001fq°q\x0000ûñcz~zy÷ñ»­\x0005Ê^êÜÅ\x001c=`RpYì.þ|Ý\x0003^ß¦§§\x0017·_´j¬\x00190¡\x00130N M­\x0013\x0006_\x0012^¥ø\x001aìíz¸½\x0017¯.ñê^¼Xî\x0007&]á\x0006\x0003éyÍzÞr/`[\x0002¶]\x0001ý&\x000f¶2ÆÐ\x0008\x001f§¹ëÌëu½¥½x}×÷âÅ7<Z`\x0015(/l\x000exa½\x0005|'ÞB±\x001aOè\x0004,mòm:(ªUs1¦Þ\x001fçWghïk*¸¦w}àæb\x0013	%=®GF$\x001d½¸!f\x001d¸B\x0017\x0001»ÞõEm\x000c 
!882d¨qFÁêMk/âP!\x000e½ã\x001fI;B³\x0007¶0¶¡¢\x000cèã\x000c\x0010 \x001c8m=¶O!bÇ\x0019ë}\x0016e@M\x0019}\x0001\x0002_0HrG[ ælJ<¸«ÞXUUï\x0012\x001f\x0002|­¹|ËE/ÌB»i+>kìTFì\x001cµ \x0005Å²FÎ­ì\x0005\Ñ\x001côò
;ÿ4\x000e|K8X2]XÛ¸rlÐëØæÐ\x0007wqkÞÁ}]\ù5èõkøOÁ¥ö\x0016+\x0013%Ö46\x000c§\x0004Ìâ\x000eU¹6ÕëÚ´4X¸Cqö%F]k0ûnÀkS½®M£âZa$çeOx\x0011×÷ÄºìÄ^ÀP½~BÇcGïZ\x0006J\x0014y)\x001d\x0005¬\x000bïE\9
Õë(L¤;Kõb~2X\x0010K\x0016Æ°au\x001eûnÄ£P½B+Àú°e\x0017C 
\x000f/¤Î1ñ,¼P}~"]øm¼8@q]ÒNYúÙ\x000cØ¹£Ks¤ÒÒK¼yüùçûîÞm¼ëë\x0018\x0015§\x0018HiÌ­$q\x000eÖtÕ\x0002üÉs÷æúåËË\x0017\x0017¯ZW}B
%jèG­¢\x0017Nu¾ñÆÌ·çx/¥\x000c
îôÖØ\x0001[°U?l5!-¶ÉC)·VÛL]m]ÂÖ\x0003{$ÆA\x000c\x001b¸×Ñ¢\x0014ÁV§#\x001d°m	Û\x000eÀ\x000e"X\x000blÕ~<À>\x001dßý¶:_àÀlÎ\x001a~ÌýöÛ0GâÎó«À³
<ÌÅ\x000cÐL½Ýrýi¼Pâ>¼>Ê#ÕâîLw)\x0006ëùÍ\x001d`U	Võ..,êó	lA\x0017Þç\x0019¶Í¹N{ðê\x0012¯îÅ\x001b}\x0004UÁ.óIb\x0015|¤Ý.9Ù×xM÷ú<½O9*ëËÓu¥hNÛ×xm÷asÇõ54eJò¤2)Ú%&;ðº\x0012¯ëÅ+Kp}iÊ½°ýÐ~vÚ×x}÷új.áÁõ
äÌ$Ï`ëm¡;ñæfr¾¢\x0017pô
§¾\x001fF.aj\x000075ú÷\x0000®Ù¢.|Ü\x0012Øù¹hÄ9E;Ø\x0004G®êv
ô\x000eÀ\x0015]ÈN¾Àv=nþð\x001a()oEPWØL:r²¢\x000cÙÉ\x0019qC\x0013ãcG+|\x0005Æq²â\x000cÙM\x001a\x0005ö\x0015vä©þlæ
W¤!;YÃ{\x001fÎé%ÁZG¼<A¯GÄ;ÑV!»9C²Ð
¾ QmvôÁ6s\ûmt\x0007à3d'ixol\x0016ôT$©e<\x0004A|sÓ\x001e¼\x0015gÈnÒÀá\x0004¼À\c\x0005J8ó\x0002Ïri¡\x0002\x001cz\x00178²@¢µ8TÄ¥\x0015V&ßúãv\x0000å å<öß;·°¥\x00059hw\x0017ìÀ[_1ºï\x0018Ñ+ðXnØhGp£O\x0004\x001c&ma¨\0tº`\x001f Q\x0008ØX	^Ëé+§\x0006N
k#\x000e+¬2É\x0015e»\x0001l\x0007àÊI@§5~1²LR×&pÜ'\x0001VÕSÝg.ÞMà{ò¹tUv*_']åTuèT÷¡;ÔÓx\x001cWEU\x001e%\x001fêÃ{\x0000WNu\x001f:ëî=&29PÓ<ÊO[áêÐ©ÞC\x0017rr;\x0006g\x0018\x0015/\x0005ïáædÈ=p«#§z\ä9~QZZ3|¢¹ÀN-ºãIë««#§{\x001c\x0002¦wQÚû	pe¿*&º\x0017puätïÿ\x0001ûe`_\x00027®\x001aºNOõ\x001e9\x001f¼0h¦Çýxû\x0004\x0006Üx<Ø	¸:rzäÈÑhz'
=ãcqûÐî½Ý\x0001¸:tºûÐ9ÉÙÖ8\x001a{h|\m\x0002¬ÚÍÛ\x0001êÐîC§=\x000e\x0006L·È tè4w%\x00069kKTÚ+sg÷à´»TúpÿtÀt\x001eO¾Am*º;gYÞàÔ¤
-Õ'Ë­º×\x001bÕ1\x00197Ê%Üy_ûYw&¡qëmbKJñn\x001a(?Èã=bØÙ\x0000PÀþmáy$}?à§¤gw¿<,Ã
Î^£nsü¯\x001e¿ÿ\x001bg\x0017\x00008~ÆâÒ$\x000füTåÕªT;"vñújXpö\x001a¥ã½¸~ö?n[\x0018Ä\x0017S`)\x0002ØÅÄ;UJh`\x0011ùpßV4é·D¨)¨ÜRlãWle]þ(Íùæý¦Ò\x00143ÅxÏ5E­*}\x0015\x001cæÉ\x0005G­\x0003Ýo-M±SLùUÈ
npÄ^uË\x001b¬ÙÙo+MqSL±¹4ÐÈ|êµ´üUd³W³ß\x0014_âg"½Ãhû%h.\x0012\4è:\x001eýÒ0Ã\x0012%\x0004%X#¸Ñ\x001a+!¹Ô-4Ç(wRTý¢ñ¯\x0012øÒmâÔòÐÅÒÊtõÛR3ä\x0014Ä\x0016-ºÍhÏ\x0012êXÊ;\x001aìg9,²¢H9#£5¹ÄìÃxd½õmQ~[tecçlc
¿"«<\x001bÑÏô]*'&§x±¢\x001cÞ\x0004Í%IÊå&\x001fß¼vÛ\x0002ÕÙ)g\x001f0CH{Ì8ºL£ð\x000f7éõ\x000e ![êrNL	³ÆHÆ\ÇºÙ\x0019ÛoKu^`ÊyÁ=F3tL¼¤Ð\x000b¥r¹³P}\x001e~*\x00149±Öÿ0:Ï»WÞr\x000bT[ü ßêìÃ³¶\x0014!ó\x0004\x001d«8\x001d\x0019Me©êè«9Gß\x0014i\x0007îjÁ\x0014¾øë·¥:újÎÑ·*\x0007Ij#ÅÈ¬\x001fã¡Y/ÑoKuôÕ£ïD¾\x0001RX
¯.ðöXuôÕ£&9'[r¡V<ÍÇØó³ØR\x001d}5åè£jµ_RhÉß%üå»èêìë)g_û^<pl´ÊmÍñªý¶Tg_O9ûÚ²¦%6'¦\x0017"\x0014iåÿó\x001c|_Í&MS£ûÌàTÏeù\¨¯\x0003wøx·*>x\x001d+Ú|%ã¤öà'J\x001aSË7ÂF¶ô4÷@;õyîýR\x001e$)'}$£\x001d?B)'8ëç`u
×õ>²ï>RÜws>R§^c[\x001c\x0015ª\x001c\x000f¸ðyöpÇ_ÉMúHÀQ§ð\\x0017®5g\x0002<j­Ì4GPçý1ï\x0014WìõÓãÏ÷ïî~H2._|üðá~cï\x000bÄÈ+ñ\x000fwfïs¹Éjöúæúåå«/Ë\x0017·oß^¶´g\x00089Èá÷\ÈÕï	¹.ë!äÑ³V[0ëÞ#Ñ3\x0007bUK¶\x000fº)¡ßÓ¢»\x0012¹û\x001d!Õ\x0011cg\x0014\x0002Ï}^¦	i~¸2¼_V\x0013ûÊk¨3Ç­®_C\x0017Hg7÷?ÿíìîã_Ï^FhÛ°{¯\x0007\x000bý:\x000c\x0004U(xEõÅF53Ó_ß\¾üãÙÅí\x001fÎ^Æ7[\x001aÍqß«áWÐ\x0001\x0013¬ ©V§p\x0004Hz=÷BpglSW¬Ï\x0004U ÆM\x0008	ô<ARUfüÚÍÿ\x0004ºÄ¯ñÇ+i\x001aäPCQ5diÛ­M}&Ò\x00043þ	º!\x001d
þ*M»j01Í(§Ï\x0004[`Ç¿\x0002¨t:Þ«ÓóSü
"\x0005?ÿ ¸Ò\x00047lB¼N§Ìsü
zù+H>\x000bÍj>\x000b|i\x001f¶@²\x0000sü\x0008^f\x0017$!àìúP¼~\x0013BiB\x00187\x001f\x001d¾*j\x0011\x0007NhV^vP<Ç"­q\x001b$éó9-\x0015M97¨\x0003ÄauP^¿
55s³sÞI²ýÆy¥?ßq\x00155Ëqn[)I;
pnø0\x0005Ðì\x000eë³ bf9LÍË\x001cn- î\x0015\x0013IØéÔ&+vãô,4õÅ.6¤wÖ¸¬Î6L7¡bg9LÏ.HªÝ&,Â=	1à&\x0013TS\x001b¹Ïå0?;ì4#\x0013X,~\x0005!³	Óã<YÑ³\x001cægç\x0003=÷)Ö´LÔ`µ¢+Ã\x000cí\x0002$m­h\x0002@\x0007¦\x001bÆÏÐ|IÙgB.SY\x001e/mÏï~¾¿û*._<!ÎmÈQ9>Å\x0016q«óD\x0008RRh\x0011qËµsüüâååÅ-J¸|q¿}\x001a1¡\x001bqR{<,²e²ò¨2\x000b²*!«^È =©\x001eDÈ(+ê@X»\x0007ìG¬KÄº\x001b±\x0003û\x0015àE,-r\x000c×\x0014C^½ºìlJÈ¦\x001b²\x0012}Áã'tðÔu«ÖÕg÷#¶%bÛ¿-¸Ø="ó41:\x00047òjíè~Ä®Dìº\x0011\x000bà
H®B\x0007#\x0018®Z\x001dï±\x001f®/áún¸ °$7!6<,7p\x0016-B^}\x0015Þ\x000f9C/d\x0019¸³YÉH*éQ^\x0007È¾\x0002V{êvC.&."~Ì:cÂlhL®\x000eÊKÆ¼J\x001d$R>H%"Á\x001fü\x000e¸\x0004Ê×Á\x001cÐ<®yÈâ5#wS6ïßN\x000e\x001f`ÿËÇ»OÓÏ:Á\x000bKÙ\x0008^ËÔ)¼avÑÛ£Ì¶?îóñâ0¾\x001aÇn¿Ø¶ÝÆAÐÉU;\x0000+¿Dx53ôù\x00188tûmüÍöÐmF
%j\x0018@\x001drÆ":\x0010êN7\x001cêäqÚ«öHÑ}°U	[
ÀF&O7\x0002\x0019tÒé7(ô@¨¡Ý*¸\x0013µ.Që\x0001ÔÞ\x0016<¾!.6\x0000/v3Û»\x0017¶)a\x0001ØRSµ¢åÂ\Ú\x0013aÛ\x0012¶\x001d[íT¼\x0016WÛÓPQ\m>¾yåÚ\x000bÛ°ý\x0000l\x0017ò&qt\x001c
\x000bGad2\x000fsþô¢§Ü\x0001:Þ\x0011Ó<e\ÎçQòRÃy¢;ºª8Y;·ö\#ý650¼¿Í1z3^r]cä\x001as.	<ëiªpb\x0004íÎÃy\x000cÞ÷öhw(?¼èfº|7ù\x001ccWcØ5\x000fw\x0010¿!ÂçÄ^\x0017Kß\x001d+ÆêTòuòìéñá¯g_Üÿô»±UÀ>äTÕ+ã/=\x000e\x000ei\àÐâÓËþìæúê\x000fg_\¾øö¢\x0015Øªã¼òu¸Ò\x0003\x001fx: .`­ºÜóâl[ ²\x0003¾*á«Qø¹-\x000cUöéÕ:hÃÕæÄÌÑýðu	_\x000fÂW	êÄ|²&½\x0011\x0015¸ôX­O5èoJøf\x0014¾æé{(ÂJ<Y2RÁìÅ·%z;\x001e'LÒâGÒ¢÷Å`<\x0017KËéïJøntëkR{'d¥\x000cÍ¥ÑX\x00031\x0019¾/áûAø¨þB\x0007E\x0011M\x0008¹\x000cÚ´Å­:Ð\x0012}\x0018]üÃÌ`«\x000f~ç§ ã\x000b¿H\x001e)\x0014^ö9\x001eÍ³EÖ
R!Ï²ÝpÁÞ¿&ÝQÖ&ã\x0017:Ë\x0004«<K½-ÝÕ\x0001¿"]9Êº\x0012Îl;øÃæÀ»G¼\x001f~Eºruc&\x0012ëâ#
G\x0012ÂÆ·%;ðW¬+i×SÂÃ\x0002ÊÐ3í²ç7öÄÄïýø+ÚÃ¼ë°¤yÁ\x001fY 
Ü\x000cßÖCî@_Ñ®\x001cåÝ\x001c5`"[ÒæQ¬\x0016a ­ÖÚ\x0001¿¢]9Ê»XO6¿t\x00078\x000ezÌ	±Ù\x000eø\x0015íÊQÞ1LNèíÁõäipñÞr:E¹\x000f~Å»rx³ëØ×nx)bÖ~vÔ\x0003\x0015ñÂ(ñb®Ö_9\x0016\x000c;qbø6ùðBE¼0|Ý
¬ð$ ÷²µoëÔvà¯¯»ÃÌ\x001b8jNgü*°ë\x0017fòñzaøÂ\x000bt|Að£{Üþ,ë`Ôú\x0004ÕNø\x0015óÂ(óÆû:µ
Bü%G\x000e5\x0003\x000e³¿b^\x0018e^\x0012	@é\x0003\x0017ÃÙ\x001f*ÞQÞ\x0005ï\x001cµ9Ï#\x0014çGmP\x0011/\x000c_x=ë\x001a\x0000N¶ìz8j«e=½ø+æQæÅi\x001béÊ\x0012ãOÁÙgÐOg®yay¥\x0018r\¢\x0014´¢D§5³]ªW2/hÖ°Wö­Ò¬"c]Æ¼ú¸ûU/Ý¯Ï~¼ÿùáÝ¢ÒùÓãûmÀ#7åù\x0011v \x0015\x0013xX[Õ-öüòåÕ«E¥óÅõÛË
¡D\x000cÝQ(7ÝOðªâ\x0008±<.À­Vúî¬JÈª\x0017²9¡\x001cEz¹Vj\x001eÒáVß
÷CÖ%dÝ½Ê8üí°Ê*ipðÔ\x0016·ZÒ±\x001f¯)ñî%Vç¶à£IJXZ'\x0006H¿ê¿÷C¶%dÛ\x000fÙPA[lð]3AÎS\x0019Üª"Ø~È®ìz!¸Óû«
\x000bÚ¬ã\x0000\x001dØýïÂ[\x0012rèÞ\x0017^±J$N\x001aÑi_8i\x0019rXm¯Ú
¹Hü"ßÃ2ËGd7è Xù-Ä#M°\x000eØÉù0ÁÉ©£Ò5;ê[òw¿ÜÿôÓVuG­³`¼\x0000\x001e\x0000íY~+F"§ãç\x0017¯/_¼h¾e\x001fÕ®!l\x0018í\x0003³¶f5ÄHUðs]]ë\x001eØª­\x0006`Ç\x0018ÅCI*º`\x001cÐ¹¦\x000cø^Øº­ûa£Þ\x0000I³ªÀÒåùÍ]lI?oÆlJÌfd©-¡Á7¯\x0004\x001bx²¶õñò>\x0011¶-aÛ¥Æ^¡\x0004\x001bËbXv
o+éÚ\x001bä{a»\x0012¶\x001bXm\x000bYTYÛs`Ëª­Ì¿\x0013¶/aûÕÎ\x001b\x001b"N\x0012\x0001ÑÝqMÁ¾½°C	;¬vàðß¤eµ=°Î ÜR\x0006³\x0015vù{\*¸\x000f·\x0012É\x0006ÕkI\x00169þói[r"q×\x001c9BNæ\x00071`ååæ²\x001d/¶¼Bl]q¤\x001c I%%OFÁ²¾vTnM{(À^Ü\x0015IÊ\x0001Ôöèæ0ÌÀðDG\x001b}è{qW#\x0007(\x0007åþ¥¤Y`\x0015c-µÝ3Û»òÝrÀywÙ\x000bÚ<vYgIIã·Ô'lÆ]yA9à\x0006!\x0008VÀüº\x0016q;v'\x000e&îo¨Ü	\x000c¸\x0013äxzÕÁ&?Æm¨!\x0018ã¬\x0003Õ¹s\x0019îå\x0005·ÊÑ«Î¯fS\x0015ÔfÜÕ¹s\x0019\x001c)?cýA 7îm¯8aWÇ\x0012\x0006%\x000eªàº\x0015i²;±\x0005[N\x000c\x0005¡:0p,\x0012'È%\x0013$°©-O=1ëM\x001d¸Uu,ÕÈ±ôÝ JHÖ¢òÓÉÝ{/gU«ârA«KÒ÷¢\x0007\x001e\x000f\x001evb©ö\x0008f¢ÑËãúðU~.SÑæ§r9ß¶'©í

ÿôÝQpøÝ@.\x0002°(+å"lí%\x0004\x0017\x0016ÛÕ6Ñ>èß\x001fAÿ~ °UçD¾e\x0017\x0013ã\x0001Îþ \x0017	ýÃ\x0011ô\x000fÿà«~'to»@Qot2÷ï\x001f~¸÷=ÿúéîÝÒçúño¿þÇÓF\x001blôð6½qké¼ËZÞ W\x0003Ë7W_^¾zÆ|}sñji{½ýãåÍ\x0006{ ´\x0007¦Ù£8p×ÒrVÎ;Ïß\x0004Öê\x000eÚ£J{Ô${ÏÈ\x001a#\x0014\x0018û\x001cu°>beÐ\x001e]Ú£gÙcÝ¹YÌ.\x001eüAÍ{5\x001b´ÇöYö(ËotZs\x0008\x000eâý¦×kD\x0006í±¥=v=ø0Êö8\x0012\x0016µÎä\x0006\x001b½ÞK9h+íq³ì\x0011(ðïS$è4úºÀÿ 5¾´ÆO³f@Ü¹ckx0a£bÐP\x0013f\x0003/\x0018Ö\´Î\x001dZZ>99¸TÌ²'\x0018`\x0014õ|£®?\x001f\x001e³í\x001a4¨\x000e\x000efE\x0007ÆÂ¹ÌGXrÖüÂÕh\x001d4§
ä¬àÀxÁ\x0003ì±
+1©Í­þ31¬"\x00039+4°ÑµÙp\x0008
Røé}\x001e¹\x0000Í *4³b\x0003Ú±\x0014â\x0018\x0013²'o7XoMí³gi¯²Å¢/þú§»hÊÅ»\x001f~ýûÙ³»§\x001f\x001eßm3AXÎóàÜv#¹9ØIµ:Üïõ\x0008?Â¾Áñ\x00117_^¿:
\x001bJØ0\x0002Û\x0004j&ë_E¤Ò\2§W;;{p«\x0012·\x001aZnzÉ	w~<ÊdÜ«B¥=¸u[àF½½äX}\x0000jÞ·2\x001c­ëíý\x0006ì5u¤#Åpü¥\x0019Zk\x0006l\x000e\x000bÍe]f]í¿cmÙ\x000e®3u»\x0007LejZg\x0017z-Ý\x0005Û\x001dh¸\¢ñUt¿þ¿\x000fïÏ¾üøEä\x000f[{\x0016\x000b\ûèÕå#òV.í«è\x0000]_½9ûòöþj\x0003z]¢×£è\x0015$ \x001f¤é\x00181d?ØÊ¿v 7%z3\x001eG°ïr\x0008\x0018!\x0010zÛ\x001ckÚÞèí(úüÂíÏ;Ç±K\\x0014ì\x0004ïJðn\x0014¼Î¥Û""²<\x0012E6;F:Àû\x0012¼\x001f\x0005_EÁ³^³ÔMÍé\x000eô¡D\x001fÆö
V\x001bkö8Ë\x001d}³Ñn?ú¢¨Ã\x001d:úá[²\x0002ìêÌ?wíÒ\x000ew(í\x0018Y|z×D
å¥å¸±=Û¾\x0003=TèaÂÚÓÆ\x000f_ÑQ2YÉ¹d%+ª£\ÍQìï5çð¤ãÅGQ¥©è+ªÃ\ë¹C\x0010#\x0005\x0006¯L\x000e\x0014æºLYQ­\x001cæZÍoAk\x001eï3D¹0|6ükå(Ù\x0006Á¯WA¨sAçÖ\x001c`6GIuÀ¯ØVN [zß\x000f8Z\x001f­>f1p\x0007üoå0á\x0006nÐ_"SãùEØÞ;\x0017~E¸rq\x0015i-ÆÕ×\¥3÷ZÅ,ûáCÅ¸0Ê¸8®´ü^\x001eÝæéªNø\x0015åÂ(åâ-ï}\x001eZd%ÅÕo\x000e9é_q.\x000cr®\x0014ò\x0010®\x0019Î5c7\x0005¯þdÏ\x0003\x0015çÂðýVr¸\x0016â°\x00142p7\x001eÈæÓy\x0007úsasãÖ\x0007rûJó´[éãxmòí\x001c*ÒaÒ=ì\x001d\x0007\x0019¾åt\x001f´ÄwÀ¯H\x0017IWòxx9»àø¦\x0002bòM\x0005*ÒaÒ\x00154ºÂ\x0006ó:¼ñ¡9;½\x0003{Å¸0q\x0018×x~\x001e©ÍÁÕ\x001dè+ÂaÂ\x0015\\x001e<+\x0000ââs¸£\x000eûá«pÕð\x00157äl¦å¡¸ø¦\x001bî¨pÕð\x001dWäÞà\x0018ùä¤ âcÛ\x001egÕ\x0001¿"\5|Éõ$èÇXP\x0013Ge§9yõë|ò(á:)\x000bõ\x0011(^0\x0005-æ;ªb\5È¸R\x001a~ì\x000cÞòêäp\x0007Ôäüª\x0018WM`Üå]Ð	ë¨QëÐÉùpU\x0011®\x001aN)çV×à<7{áPLÞú/éª"\5L¸¤#\x0013\x0017ßç@ß²REüç\x0006kª¢\5r%\x001f\KÓ¸øì6v\x001dè+ÊU£ë\x0002i\x0006;!!o\x001d\x000b|nÍä[®(W\x000fS®Ë[\x0007\x000e¹µ¼ô±W|«ù£ü¸ô{ª$ê'ôvrVVW|«ù6PíQ\x0008¹½þ\x0010iêÉ\x0019q]±­p½\x0015´öÀc©qíyéW\x001f;Ñ×¯·Ã)eKEá.òà¹Ïù|gÙkõ0×
§\x001dÿ$\x001fÚür\x000em]\x000eô\x0015×êa®ý/^ûjõ(Õ:E1~\{Ö<QfNª¹æ\x0018í\x000eø\x0015×êa®u<%ß,SÑ%ÃÒ\x0015Ùêa²õç¼u<×ÓJËdÀO¾¡kÍ0×\x0002\x0005:.2!÷\c\x000f-ÃoÎ4é_Ñ­\x0019¥[§ir9V\x001d9Þù\ú\x0007¡ÙüÖ¾b[3Ì¶\x00121'ø\x0007·csé'¯}E·før«Î	<j®°ÓáÛUX¯òï\x0003_±­\x0019½ÚjAMN`ï;É\x001fÔSbr2ÖÔµR£lë\x0004ÍP\x00128\x000eÓ
\x0007@æL\x000eô\x0015ÛQ¶M½;qÛ\x001cÞýmÎ)L~A1\x0015ÕQªEMNr86<gÄNãLâÊ7{Ê;àWTkF©Ö¹¼ëÏ¥Ò&äÅJ6\x0015ÕQªµ6Ãw&ï{Í+%ó@öÃ·\x0015×ÚQ®EÌ|luæZÃ%ª=P£\x0003~ÅµvøíVP§Ã¢;Îp§¹SÐ9é_­\x001d%['s\x001c\x001e\x000e3Ya+Âµ\x0015ÛÚQ¶5&ï}Ô\x0011!Ï\x0003|t\x0012së\x0016lÅ·vôv\x001b½¥"øÞçPGs©æË\x000eø\x0015áÚQÂÕ<XÙI¬÷¢£\x000b¤É\x0011Wr2ÖÖÕÉ£\x001b7Oª\x001aðm¾¤ðÚëf·\x0007øsí(ç\x001a Õ³¸ómÎf\x0002\x0007ùJ©Éð+Îµ£\x001bAÒh)e~@oC«?ùzk+Îµ£«X_ÄI\3"B&-Ó\x001c6º\x001f¾«8×r®æòð¸ú6çF$ßoU[\x000f¾\x0003~Å¹ns¥âxS¢\x001cnòúñ7¹ÇUëF9\x00173"4¨\x0016G@×Ï^ÓL¾àº³Ü(gÁaëã6J{GxÎ«),=
¿â,7ÊY§ÆÅ\x0017¿µwºF\x001dð+ÎrcåCtû"¨C\x001bhç#Ýèëî_÷Ô²\x0016ÈL¹Jq¡fÜ<\x001c-Ow\EZn´jÏ-¹Í`¸F9î(
M½\x000eø\x0015i¹QÒÂÁ\x0016ßrAx\x001eÔ¬l\x000bßW¤åÇH\x000bÈÒ¾\x0017ïè\x0005V­¯\x0018Ë2\x0016\x000e©eï¹\x001fKX¾eÙÉÅí¾",?FX>h}Y|
\x0014(àø«íä\x000c¯.~ìè±J';\x001d÷½2ÙéÌÞ;\x0015áú1Â]ÆÎÙ\x0004\x001f0Ag\x001d\x0013ci?¹ÞÈWëÇ\x0008×/åtI´¹N3Æ@L¸¡9æ»\x0003~E¸~póäª¸úþ\òÐ<Wr\x0007®¯\x0008×\x0011n\}I3\x000bqH\x0004Oa\x0010à)ZÓbò-××m¬£\x000bÊdñ±<iMÇÅWyñ'? ûpý\x0018áâ+º§¸,U $×iêöÀÂýðCE¸ap!_³À\x001dF\x0005óÐ9§Ãd·\x001f*Î
c\x001bCå@e¦\x000eWµãÍÓV^í_n\x0018%]!9ØDér gS\x0006&WtÃ(éÒ%\x000bâ}§-zk9Z[nëÃ^QV\x0018¥,-9«\x000c\x00180P¸Ã7\=û\x0018*\x001fF]~\x0017Ò°<,æÍÇÖp3v3¡îý\x001fuÛ±°ÀZ\x0011qF3;Íà§ÞR¤¨ÛçÅ ÛñÑ×\x0000màóln@7ÒLö:âO\x001fîü>þdì#\x00005\x0006E#T×©t¶br0@%¡ü'K(¤RGÎA~¦ÈÙÙc+\x001d·Â»¬õ»c~aÔrV®YjøS%æ\x0015PN¼öõÓ¯ÿñ~Û×Kà\x0001`\x0016«Á\x001a¡\x0017\x0011µ°îFy\x0002Øå³¯o.ß4Ö]\x001f«¦i\x0007}<pvù!®û\x0013²±|ÇPÐ\x0000î¤ù¤áMÙfáÚ·ñóòìòm\ô¯/oN\x0003\x00128\x0000÷*?¨À¡\x0006Ã:Î*[Õ\x001cG°\x0017¸.ëÁ\x0015WTú\x0012\î\x0000Í1¾RíZ{Û\x0012¸\x001d\x0002.©k{yýä¾áÃÓyûõs7p_\x0002÷CÀ¦	Fà\%\x0005¾×íQÀ;Q\x0013\x0010Ía\R\x001fl\x0013	(±ÀëÍ
{J©È«£)GÎ&¦º)¤îKðA±\x0010jO/Þ\x000b¼:rälJ¥QÙ7Åñî \x0011¸Ïq¼iQØÜTÈÍ\x0008òô¬IQ$uè©|qmVaîß)Åü´W¾\x001bqä×\ª\x0018ÿr) +(×B°\x001fü÷Gà¿\x001f[vÚè\x0001Î¥¢\x0007¾r¯O°ý-ì¿-')áóã\x000fê¡/\x001e¾ûõïOw\x001f\x001e¶3êæ\x0015\x0008Ï\x000f;-N¡iV&¡×\x0017W_\Þ\¼½jÉ32t(¡Ã\x0010t¥}\x0016z¶À^Ñ\x0000\x000f­p¶©ô¶\x001f»*±«ÁesK³qP\x0014ëe\x001eý$rWû±ë\x0012»\x001e[÷HùÔ\x000b©¤;Ìõ<^m\x0018\x0016²\x0007»)±!ì&îqL!9«Bô´etó\x0019p?r["·c«\x000e\x0007!+aY£K{ºÑÙö;Ú~è®îÆ\x0016\x001d{NÓë¥#oYtÃûE»v|¾\x001bº/¡ûA\x001f\x0013))U`6\x0004
ô4\x000bÊJ1×?\x0012{\x0018[v\x0012¤[\x0002£\x0019ðV\x001b;u«\x001f¢ÝÄØª\x001bËÓà!^îHRÌ(Rö±V4E­ö¯	uQcTÎ²»qsà HµÌ\x001fÈ>FÍu2²¢T9È©¹!§æG3Ã
TÖ´£ÝØ+Z¼ä©	ÆÆÎ}õ/­ñw|åÜå w\x000feYÀ8ÎaÀS¬k¾µî\x0007_ùH9æ$µ0¼Hàó];\x001eñ\x0013L=­P¹\x001a\x0018s5\x001aä¹'ì*ï¸ùyH¡	§Çí
	Ê<i
\x000bêyycñX\x0016Ý-ã±
ã}wÅðÇ&À°	 \x0012~Ue´çy:ñäNÚ?òøú$óõéÇ÷÷¿üxöâñã¯ÿßÆ\x001b\x001fî\x0017R¬ÜÄ²£¤bìÐòß\¿¹|ýüìÅõmëªÊ¡\x000cý\x0005'î,Îù õ'\x0005<\x0002\x0015k>¦aV%fÕ\x0019k\x0012d¦y<Í\x0003\x000b[}u	Y\x000f@Ö\x0014M!H-ykØæ|ó}MÙtcV"Ï
uñ§ÌRò\x00055æ­³-1ÛþuÆ±²	³
óÐj\x000bQ!l\x001edWBvýË,ó¨:'
\x0013½öTTeC¸5|Ù\x000f`V<\x0010×Åû3Ï©öÔ¢Br-\x0007½\x000fs(1~Ì
h\x0006ÀYF°rÍ"'9	rqõ«O\x000fæ®=.ÞÙ"X\x0001ì6Bó¹s\x001fè\x0004ûY\x0010);ucY\x0017/Ë³p4{Ñ	Ù>ö®hPöó Ò
E¬S¹<Í\x0000?¨,¥³@W<(ûPYqN»Ãèó^\x000bæìxü»ça®Pö3aÄL[#ðhÞ·F[fu\x001fâ\x0006å\x0000\x000fÆk/ù:hÐpÅçédE²\x0005[ \x0013dBo	2ëÇ\x000bÕldÞ\x0007º¢A9À>\x0004u.ðÈcãY\x0005\x00165fa®hPöó Æè¸Û)®¦·	\x0011¿ðG\x0011¤qöt÷wïÎnî¾x·mw(ã\x0010\x001b§$GHº©0ðÍåÅ«³gW¯\x001aãû\x0018°.\x0001ëNÀ\x0016\x001fC(Ú·ê\x000f±$ñ6Ó »ðÚ\x0012¯íÅë,ÏìôAQ³±ü\x0013Ú½9»ðú\x0012¯ïÆ\x001b8ÏdUÜ\x001bWæ	4k ö\x0000.Â¢\x00088Eûwåq¡\x0016d^a¼Ä¢©ò¾\x000bquædï¡ñ0'­ÈU¨Vñôsï)¥ME8®þ
ÅÌLÌÂüç¿ýûó_ÿÿ\x000f÷?á_}\x001bnÿ:0\x0014\x001ay½Ä£I\x001a\x0000xt\\x0015Kãú0\x001fsöüúíå\x000büå·ñOm°\x0003J;`\x001dKø­7&Ï\x0001óG3ÈÕ¼Á\x001dª´CM±Ãq9Çò=¸(ÂØlÇª2Õ\x001dº´CÏù\x001ek"ñ{°\x0010ªÏJÖM\x000cØaJ;Ì¬ïA\x0013ÎL¾îÈ\x001c J\x001cÇ9Ý\x000c[ag!\x00057G;tVÊ\x000bZæÏñ\x0019¹+íps>¤\x0016ÁhÇ*9>ËÇcõÅjÝa®á¸\x001a1,Y	\x001fCæG\x0008ü\x0018Éå0yO­Þìú¿EQ\x0018RÖb\x001d\x0013\x0018hçê³Ë]\x000b.\x0006ì¨)p\x000e\x0007º\x001dVó4Üþ%aµz~À\x0003å\x0014\x0012`Ê\x000fBó\x0000òÈàS³w÷\x0019\x0002òÌãÊ¥(*"¦·¡g\x001fzúg?ÞýüËÆz\x0010ö0 Îc[çòn¡²0¦haDÐôJôìúöf©­öüâåëVu=¢JSÔ\x000cSPh>	6Øz\x0011àE,}\x0012\x000f\x0008|À\x0014]¢çb)Çí&Tb\x0002X1H´.\x0003Ò\x00123ÅHåüQb%>0ÏIsôç)¶4ÅÎ1\x0005¨í9bK,ä\x0001²áól/WZâæXbÏiÊò¹\x0002çòÉÐ(\x001c°Ãvøßµó
¥)á÷lJ\x0011¬DS(ð»³%¸ã;»;To¿?»zzØ\x0008Ýáx R§@Q^+nÚÊ\x000c\x0008öêæj\x0003T(¡B\x001fÔìPD"½wF¨À\x0005e'j;¶"U%RÕÔ\x001f^9Á-"è©i&Ô`1V»Lu+T]BÕÝßßçªÔôîß+fDS4y;TSB5]«
bx¶¨½\x0000Çbò¢úfÊ|;R["µ}Ê\x0016+ª<5mæÚ\x0018»~#Þ\x0007ÕP}\x0017Ô i\x0005Ï9:ìÑüýÖ¡wDW\x0014õî;V'¶á±ò´W°ùXµ\x000bì¶b­|ìrV\x001e¸Ô\x0008¬¡äx¨y*nÖv?æf¨\x0007].À£\x0004\x001eW»\x001ev«§IrÖÌYÔêXÉ®sÙ¾¤Û\x0017o9¬_ú¸Â²=
f;Öê\É®XyUK¬j.T¨Î\x0015ô+*=¬pj=\x0019h\x001d\x0000ô\x001d*ã9ÎZ°*Âjüd¬Õ©¾S7ZêÓ<Ú\x0001÷ÂY7åüCuª ïTé<ü\x0018ðXAä¸êT?Ð)¬ñUG«ñ\x0007\x001c­ÞÜ¿ûõïg7ÛÕØ%\x0017¸¼{ý4KG\x0004ð\x00130Í\x0002ËWñ?®ÿx\x001a+X¡\x000f«Ð$a]\x000c­¨\x0006Ëé\x000cµ\x0019Ye¨+ýî(«8U\x001fÎ s}[ºãûH\x0004\'Ö\x0014×Ú¾¦ÄiºpbÙ\x0001õ!á[yºªØ\x0008ß°\x0014Fsîãv¬¶Äj»°js¨¿sUÑ­gY\x0003¡Õ?Û±º\x0012«ëÂê¢{¢éáÆJzÞtÂÑûõ¦YGº\x001d«/±ú¾u\x001fªÎ\x001dÞ\x0001©\x0017M\x001cjªZE\x0012Û¡\x0012jè[V\x0014¨¦eÅ
ÒDVÂòÓ=4ëe6C-j#\Îgì^Ö`¸ï\x0003ë¾h8£SÂåº¯Ö-`;Ø\x0002ú8ÀÅÕ¤Â\x0013l\x0007
´°o×KÜ\x000c°\x0015\x0007ÈN\x0012\x000b½0ê©c5³\x0000¨)KVD ûÀAn\x001dÓñ
ò¤è«(\x0012p¾\x0015´lÇª+¬ºoaã­Ô\x0006\x001càRÿµs¹X¸9Pt;Ø¹d\x001fua\x001b\x0004Ñ<ß\x0006\x0007èÒÅ\x0005£°)`+ê}Üe°6VV9nðù
yyT\x0001¶â\x0003ÙG\x0008.2K`µSTdëDà\x001eçä&°Í(\x000b*\x001f\x000b}>\x0016\x0010©L\x0015#\x0019\x000e_,_^B3#°yU¡\û¼\x0016¶G9ª;Ó»BÈ¥}ÍB¹íX+G\x0000} ú'¬`Ïu@g+7ÏIßJ¶m\x0007[-è;[\x000e_7\x000f]s<¬Q¹k®98~;ØêlAçÙR¹wÞÄË\x0016å\x0006\x0015\x001c\x0018¶¥î7UÕñR}Ç\x000b]U\x0012¶²Æ\x001c¸ËrnÈëæpïí`«ó¥úÎSëìMÄí8¡\x0019\x000818l=­î\x0000[\x001d0ÕyÀ\x001fOM*ÊIA\x0001ÉÐÆ;Í6\x000f{\x0012ku¾TçùÂºÞtGÔÁS¸\x0015ÃWö\.è)áªÎê<_Òr>[{®zÀAÅ¹kN¼%TÕe½$
¸Ëz/1D§E¥NJ.½ô\\x0019º!ÄÄ3\x000b)J TÑòFûñìÙO\x001fî?lC« w\x0004d	Ç]p\Á`[3|wÙÛ³g/®ß^¾=
YU7d!¹\x0007.RAÑ;Ë0ödÑÅvÈ¦lz!C»<!\x000eÜL¦Y;Ë¡Fø4Ä®Dìº\x0011kÅ¹ sx£|.\x0008iÊLÔW
<\x0013^Yïãî¼\x000cM ú(±L;Lk,òFniðî\x0001\íbÙ¿Q((µ­ÇqM°\x000eÜ\x0015)MK¨i\x000b`©ÄQR9\x0006\x000eqS\x0001ÇÇ³wOw[3à8Ó âÞ`?!øi\x0019\x001fWEvÛ³\x00177\x0017Í\x001c8ÁU%\Õ	W\x001cJÌ\x0004wÞØ\x0018=xÞ
k\x001c·\x0017­.ÑêN´JqÊ.¡ç\x0005+\x0002ç»¶w÷Â5%\Ó»¸ËËr+XBD\x001c$Üjë^¸¶k{WWòû}tÄy0Là¡Hñò3\x000b®+áºÞ&¹\x0006§P¢QØ¼\x0019üjKÐ^¸¾ë;ábÃ?ïÝè#hqYæWúÕôh,.º1Ñ\x000b×ä*ZÅ"ÐÂ»\\x000f¼\x0018Ý
\x0017ò
ÏDYxöü.ÅÖ¢LÌãrà`\x0019.¨Ü7âÚ*áoÎ_DªØ\x0000WpU/\ËW \x0011v	nàÕµMI=pM	×ôÂ
T³\x0014\x0002gþmJÝì\x0001ëJ°®\x0013¬^ú\x0012ÚCs\x0011Ìh¦)¿²\x0007®/áú^¸*G7>¿ì\x000eì\x0017ô,¸²>hÝ'Íç\x000e-ç¸­\x001ftnÄTÍ9Á\x0005Þïï~¸{ÿái\x001douÒd÷Q2Ç*1b°ÔkÒ¼\x0018ïY_[áµÿðû¡:m²÷¸Åý@)Sê0÷\x0003gøýÖýp\x0012o¨ðÞõ\x0015(Á\x001aÀÜç\x0012\x0018î	uæÍpËj*QUSík\x000c¿I`á\x00079³|\x0017¶Y£²\x0007nå\x001d ×;èÀY\x0012\x001f/T½\x000e^\x0008×Ö§ß·ò\x000eÐë\x001dþËN\x001bTD\x000c½Lü_·òfÐëÍ¼<ÔX\x0018Ë8\x0014Y,	Þ·òfÐ\x001d<ü­o\x0015<@gôÝ"$é/,à¹[$?¯N#¡r¾Ðé|Á\x0004\x000eÓ\x000b±(}Ð?`\x000e^U¹3ÕéÎP±ÈÍÅ\x0018
\x00034&!Õ,ïëª9Ui\x0007\x001fÔK÷o
ÈÕ\x000c¤å§T.\x0013Í\x0017×]\x0011å1ê\x0018Uö¢>
,Iâª
,§ÅíÇ°ý\x0000ê@º\ÞËÜ
¨y6^üíIÑ\x000fØOvíG\x001dC\x0010ò9$yaÅïÜx\x000e\x0007ýÆw\x0012TúBâ\x000c¾þç\x0017\x0011êÛ§Çg\x0017Oï\x001e?þ´1\x0007\x001cÁöW\x0004,¬Åù\x001aK]±ÏºñëÂ\\x0011åÙÛëÛ³W×·/\x001a\x000f\x0003R\x001euÂ¡þÐavÙß¸ÿøtöÍÇ¸Îg¯\x001e\x001f\x001e·¡÷X÷@*¬0pid±±,×\x001d\x001e­å¾=ûòúÙÛËÛ³onÑW×W7×\x001b\x000cÒ\x0010asb\x001b|:H¢GÆ{V	ÅWÏ`*íP3ìPËñéì0\åáÛÝ½fèÒ\x000c=e_eM,dLÃ7É]Õ¢ÝÃÔk)í0S>\x0007äú;ÐÔß`Îõw¢õ¶Úo-
±3\x000cÃ]c¨Y3\x001a¢²\x0018ægù ®´ÃM±#ñc@\x000cÉ\x000cÅ¹ê\x0018A4ã^;BiGa4ñI×\x000fEº}\x00068+\x001co\x001fS\x000fº0Ç\x0019mÞ\x0011\x000fã:/ÿüÓÝ»\x000f\x000fï¶25
3Ó\x00117XÀóuL.ý^9Ìì¼üúÅÅ«·W¯qF\x0002_4,"x\x0018B\x001f÷\x000cûY#í¡ü30z¹ê¡:Ñ«
½ú­½®Ðë±µÇ±uT½¤Y\x0006ÅkÏ\x0005AaUR±\x0013¼­ÀÛ!ðV¸sEEÎÞSÎçWç·LªÝ\x0003ÞWàýïkß¨
½ú¡×¢D¯Åï\x000c}å/õ¿ü¯G_y\x001c=æq´Ó|Í1Â°x2¶&p3ÍjAòNôÒ\x001d\x0017ì8qè\x0002ýùîiãµRhÃï°.ðcü²)N´}¼¼¸iE5\x0004\x0012JÐ\x0001R9Þ\x0014\x001eD\x000c\x00159ñ'ú*·ÁT%LÕ³S§Î8RxK÷\x00044µë·¢4%JÓ\x001aiÆòHÉ\x0002ß¢\x0019ÚnéJ®\x0007¦Ì³-°PZ\x0013LÒ	¡9\x0000u+ÌPÂ\x000c=0C\x001eX'¶¦\x000cÄÆ\x0013$ëc<êã}Jõ°\x001eòÀ¼¨N¦êË)´2^è\x001fTYo4¡~.õþén«lsVó2^\ÎeÚ	à,7NÈV²¢Ðz\x001e½êåÍE[¿LÒO¤\x0012÷\x0000<\x0011\x0017»W)ë\x000f.7ª@+³Ûi*MøD"q·	Ñ£yC_\x0001rÁN<ü\x0015Ü6U®=&èÒO¤\x0011w*\x0017ÔÔ\x0002å\x000e0}Ç_A5\x0013&ÒO4\x0011÷à¸@ÑàÜYYK;Æ¯ÐzMì4Á&|¢¸Û\x0004epÔl2Á¢¼n*G9|Ò}§	®4á\x0013\x0011Äý&h\x00056Òq<\x0002ÊpÃle³;Mð¥	è\x001fî6!\x000f£\x001eIr
"ä¯Ðzì4!&|¢{¸Ûx?0*\x0005CÇ\x0019¯0ÝRïPýÞán\x001bÇÉy
).[\x00089ð{o\x00059&Ôì<NÏØÍ^5\x000b¯à&1¿®\x001fßoCåUå°[E
|ÞJØùHÁçñª5\x0010©\x0019ªçÌ\x001d(¦\x001b"\x0008dd8÷\x0014+iÏD«o³Ó\x0010ù§\x001fêïápIq\x0011àpIgkÝ¤º­ø®¶â»1+|ÂPÛ·Ôç6½!\x0004G:¦6ýj¥Ýèx~ª8ÌOÅV£»þr÷ð´qñ\x0001{¸dÞB^Æ5?ÕÆ-Ô,Xº={vñâÛ«Ö\x001fOO\x0015é©\x001d\x0005ëCbÒÅR±Gf2Ñ.Q)ð¶WW`U7XÅ÷Åå=ÊÁt¾	¬O
Ù½º¦\x0004l\x0006\x0000ÓvÐÁrªÒ¬iåBS{i\x0017`[\x0002¶%ÝR°iªQàøØ*×Ô
ÝÖh]7ZMíZ([@¼¥LÚÚ¶{ðú\x0012¯ïÅk,o\x0007ÿËì\x0001Ûö|¸]C	8ô\x0002vY,FÅ[8µ÷çë\x0006&Á&\x0001.ÃbÞhÇ\x0012\x0003k/µ¹^ßp[¸9QO¾\x0007qÍ\x0018½\x00111±´Âº\x0012Ú\x0014.+ôSÕ=Û\x0011W!{9C\x001aÁª<¨}©xyB±iö,ïC\ñì%\x000eD¬YZØqÚ6^vB\x0016XWu/bí±|xA\x001cïübQÃÌaLSc\x0017âêd/×EßÅB"JHËÍ¨^Í"\x000fYìf\x000f­¸\x0018Ô2r;û6\x000b£*·Ù¸òÆ²Û\x001dã-\x001b\x0008ª\x000fÂ\x001aWÞ\x0014º9q\x000fb¨\x001bt;7å9ý\x000cÂñû¸Ü\x0004XMGÎ\x0005®»7sÈoJ\x0004.ä+O°'eZ(t\x000cÜõãÆÊ\ Âx\x0017Ï¹+\x001ftS@s\x001bn8¾0ÁÑÆå¾÷ËýæN¸ÝáÝÂ\x000cuHÌÂjÛÄa Ór×{}ybÓñÕ	\x00063î.,ëw\x0018%YÒùqâô ¶=ÈU\ ÿÏyXí¹ª8n\x001c=ûU]ÎE¯S6¸ðø\x0011\x000b; ?\x000cÑ$n\x0005";lö·É\x0002u¤\x001aý!uaÞ·\x000fÞ^Zå$y\x0011·±X\x000e©Wö°vC¡Ã·W_·K4ÔñÜ2µÈGwV)7uçL=qxÆ,6TmÅ¬JÌª\x001fspD2\x0016uv\x0008´å°O¬çé;@ë\x0012´\x001e\x0000-hºµ±fÉ\x000e/ 
«õ
µ.°\x0003´ôÇY/¿d½\x001e?~XNã\x0017O\x0008pk"^²¬`°?6±%\x0015o¨°.\x0003ss}ûv9_Üàï\x0006¬JÀª\x000f°\x000f\x0007\+p\x001fpâwK¾Oy|C\x0004ØM/`Ëï~
¯µ4ò<xÏx×³¡ñz{´#¼=èi}yÿôôðë<E?½³[H9ËÅ\x0016\x000b¦Rf\x0019;À\x0012í\x00114ñ_77W7Ñ[oix"; ´\x0003&ØAójªáÜ®\x0006ÍE5'¢ïN;Tiñ=blkyZºbxdå¼õ¦#vèÒ\x000e=ÅèÝ)ôa/éYK[|ë Û\x000eSÚa&Ø¡¥Ê"âXjö\x0015^6Ø\x0013MÃ}vØÒ\x000e;Ã\x000eÈi!ã<\x000b*YÈv´»»:Íp¥\x0019n\x0019ñÙ]YåùIÖµ{\x001bûÌð¥\x0019~\x0019êP\x000bºÒ\x00173tÈãí\x001bl§\x001d¡´#Ì°\x0003]-\x0005ù\x0002YT'f1Ý\x0013Sáºì5\x000bÎ A±ç§~ÅçPZ?Èç8\x001f²¢\x000f9?°PwÖ?µù¶~¢\x000b¿Ë\x0010U\x00105ã(«©\x001dÕJT²ðÇá¹UJµfÆº*\x0011ñ§\x000f÷OG¦àO¦XCe\x0018h\x000eÉï\x0019BÄö|0KW·úÚ\x000fmå#ÇE8îç7Þ<9ÎÌnøDy'\x001cã&£\x0015+m\x0018GÒ×±<|=ã	¹æ¸ã\x001c[rt\x0017¹÷³-_ßmL+ú¸Øçnñ]N\x0019EÚÆ{î!7Õ5'|ñíå«[Nµ|}ÑL,ºã\x001c[r\ \x0017yZ@{ E\x0018)RÅ°ºä\x001d M	ÚôÆù<	4¾i§'â\x0018ÓrOör\x0000¦v%h×\x000fÚ\x0008ªtZ.%ýévÊÊøD1
tñPìÒCq/jçè>çtä1j\x0010Àê7V­¦á:P×'±û(F/.¨'Ùi'Ï­bÙRj±«é\x000eÐP~Ðñ(¦+Ó6gÉåîè×çíjYù\x000fÙí@BôÚô@\x0018÷B\x000c\x0015(C\x000e@J8ëz¶\x001d u\x0005Z÷/ujMIûCgÑàÀ\x001a\x00028Hg\x001eêÊëÉn·\x0017wµ#	\x0007\x0017i»£(ß¹UÍ¡\x000eÐ¶\x0002mûAkÇ¬¨C® x©ýD_-+_-»õòNo³Æ?ºHÔÂæÖãÄ\x000eÔ¾BíûQÛÃ\x0006ÎÄÑZg\x000f'ÌDÔ¡B\x001dúQ\x001b\x0013¹ Ö\x0018\x0007\x001b\x0018õjEñ~ÔP\x0011#t\x0013c\x0010ñ¦*\x001d6p£\x001båk[\x0010Ö\x0001ºâE\x0018àE\x001bjÃªgz5Ç\x0012`\x0010;\x000ftÅÐÏRÐhng´å×z\x0010,\x0010\x0017]õ<·\x0007\x0015-B?-àI!9¢ö4¤ÛÊÀ\x0013\x001acà:/Úa a¤áA\x001b.nåÜ9\x0015¯`Dæ;@¯:ó«ºB.÷.üAïÕËúsAW/o)\x0017oÄÊñ-fõ\x001e¼cµ¥<îú7ïþ\x0005\x0001n\x0016à°¸Aîi±\x0003¿»\x001a×Öïß\¿ú\x001fø»Í6~yÜ!/Åá¥§\x0003´ÉE?øihÔ¦í²Æ¨UZ
 \x000efbA¼ÅH\x001a3Å#\x0012q\x0002YûUj\x001fj]¢Ö#kÛý!\x0006|<PóTr+ãöÂ6%lÓ\x000fÛIÁo+à§3cÃi÷¢¶%j;°Øñ¢(\x000f§&9áÎáÚLÑN
îíJØn`±µÈ\x00052óÌ?~o5º]¹\x0013µ/QûÅ\x000eÙ\x0018Ë1_Ài"äü² {a\x0012v\x0018XlG\x0019`É\x0008^Êµ¥ê¤²ù\x000eØÅ\x0011)\x000eÕþ]îÏp\x0019[üãäHÈM+Xb5\x0011wM\x0003\x000cé|îäxãMs\x0017%\x0018ÆÝ\x001ce¸\x0017vEr#ãÖ\x001a(È÷Å¼G¬>¥ûº\x0007tÅr"£{ã¾1\x0019O§L^;^\x001e¹6]Ô\x0006Þ»âH9@NÒ&R»ÍGRå-2"eEr#½Êu\x00002\x0006¯é©\x0003#Yr:4¢ïÅ]¤\x001c`I\x0007Zõháã¼INj\x001aïA]±\x001c \x001bwP$xñå©Ó+¾v\x0013ý6T~\x001b\x0006ü¶3¹ê\x0005¤§â]¡2»OI ¾#8@\x0014Ô¡Æ\x001c	Tå\x0012yÒ1îõòÌ\x001eÜ/\x0011_âtnÃ0D6RèLî§¦Øì\x0001]\x001dI\x00189Þq\x0017äÑQ#¹!ßÖ\x0019ß\x0003»:0r&ãn¿øù\x0006x¹af¼­ª3©\x0006Î¤\x001fÔ>ð]R\x001agrL2'Uu&ÕÀD];Òc^N¬.Ç²-\x0000½\x0013wu&ÕÀD¦¤ é<½Õ Sê\x001cÌÜ'Õ±T\x0003ÇÒcA\x0019­·Ì lfø\x00135YûpWçR
Kou$\x0001H°%3èÐn¿Þ\x0007[WÇR\x001cK\x000byXEÍh\x000e\x0014dÜ3¨ò;¡ë\x0002ð/â\x000f0\x0007øâ?ÿíßß?ýüðáîÏ¨÷ñ¯Û`ÇK/Wá&¡æ\x000b-¹ÒÕ²Ö\x0017gÏ/o^^½½ø\x001aeónÿpÀ×X\x001cÕ·Ä\x001fp¾òû»w8«òáþìÇ§w\x000fßÿ¸µË\x0008\x001e±	èþ¨(p\x0015®Åß\^¼Â©Wg_\ß¼ºzö¼p\x0015Ghh\x0000\x001a`M`©`JË¸@ó"Ü^èÕ(z\x0014\x0006£,\x0015\x0006$±\x000c'ùv\x0019}\x0002]\x0006èÒ\x0000=¼\x0002ÉQ º\x00036Ô"%¬?Qvã7%~3?4Û\x000e3WÅ`tîë÷Ó
°¥\x0001vÔ\x0000-óÂ).²S^ä\x001dÔìAï2À\x0006¸A\x0003°}WÓ\x0011ÐÆõ)É/\x0010¦yµèïKø~ø\x0004g=d\x001c\x0013O\x001d\x0019Êå;ÝzWU/þPâ\x000f£ËÏDå8I\x000eYMÎ´g%ö /² â yÒ¿ü8ÆvqyrÍ·<7\x0001dÅ_rÀ0çÜ9ÐÅÉ*sÈ·Wº\x000c¨\x0018@\x000eSÔ\x001c\x0019\x0003ÖÙÐ	Ð:\x001b0\x0013U.T\x000eûP)\x000e.H\x001fH³`¶ÙþÒe@åä°\x0013\x0012:,iÁB
Bõh	ÕvY\x0000Õ9Ñs,C^\x001eY;w	³Y\x000cª8\x001a\x0003igÏ9\x000cõT\x000el5ð=Ë6uvû\x000c¨ãèQ?$cüÆ\x0002ÜNIYÌäwÞÖý¶ËÊ\x000fÁ¨\x001fÂg\x000eE	?È
Î\x0010rVØ43"]\x0016T~\x0008Fý´îßpÐ25»,ä¥Wå)º-¨\x001c\x0011:¢ÿ\x0006\x000bTåÔ°#2\x0007:\x0016ÕifO\x0004Í:.\x000bª¬\x000f2NµåWÖÜE\x0014½*[ ñ»,\x0010ö¨\x001c)þ¯ô_Ý?½»{÷ÃÙëÇ÷ï\x001fßm\x0003/¬äJ ùiÇF¨R\x0017'©5ÀuyóêâÕg¯¯¯Þ¼¹~u\x001a¸.ë\x0011àqÕI
,HÕ¸LÆÉõ&.à¶\x0004n\x0003?]\x0006á9ø\x0011Ái\x0006ÞÌ\x0010î\x0006îKà~\x00048\x0004>©8ë¶\x0008yú­m¦\x0008÷\x0002/zpì¡|£\x0013y\x000e×,,#xf¦tØ¼:rèxJçÄÍKêYàBziùÝÈ«ã)Î§t\x0007äI8ò\x0011yv#¯Î§\x001c: Rñk·G©3Ãkn\x0018ùÔ%¯Î§\x001c: ¨\x0004ÌCnËqÜ¸\x0014£Lô,µØÖBDÜÇÚÉE!»t7sÅý\x0017¹¨©«º\x001d¿9n\59±ùóÃO1\x0000¸÷ø°q§ó\x0019Ô;îd0Îf"RëÂD\x0011õåË«\x0017ù/_]_5Çv\x001eÊÊß\x000f\x0019ß\x0004\x0019²\x0017\x0014sE\x001f\x0018ølêfé>Èª¬ºW9h¾¯bûjÚ\x001b\x0006[r\x0008²oWí¬KÈº{e~k@¢§f\x0017<ogÛTÇØ\x0007ÙM÷*KÍ\x001e$ça9»\x0017ÿj\x0005ãû Û\x0012²í_å\S\x001aâ/¦UÎÜ\x001e÷Ë4È®ìúWÙÑ\x001bNÀY\x0016@lx_Õ\x0019û\x0011û\x0012±ï^d\x0000Ò2[<sRm7^\x0004Þ\x0017ë½@^W¯0Ç½×æ°îÙ\x0018_´än¾\x0019ØÉ¹fh×2ËJú¹$Þd\x0003zó´ÌÖPRË©0JdE%²K\\x000c\x0002ÅÖÚð nçx/Oó\x0017²òÊ²Û-;Ôi }\x0011×X[6ô\x0000æ }]ß¹òq²ÛÉ9\x001cÉ:\x000f±I5\x0015 øt
P¢ùêµ\x000fså2d·ÏÀÂbêðÄé=DÖæÍ¬E£»0Cå3 Ûg8Zñ%\x0018ªº§Dµßæöá­ã¸þÃÁÒ\x001aÇà\x0018Çÿ¥}AERNfÄ¼\x000fsuþ ÿü¥&åäã\x0014s5&;9=-êüAÿùK\x0005­\x000bfcs\d¢Oåç¿£k1Åµª\x0005µÅ7òÄ.«êhF.×¥\x001aö#ÇÈå\x0008rá\x000eI\x001bO©\x000fã<Áëz@\x001dÜò	r=\x0000Ý9s\x000e´è.Ð(Nã4õ°80/ôÐØWÎb_\x001dÐQ
/E 1x¤}&ú\x0019ôÀÌ>Yõ
cñ\x001dHÒ\x0001w1[\x0015øbÚFè+Ý×\x0000GèºKî¾1d\x0010Ð£$Q5î4!¿¬+|d-æã)dë16Y\x0000¥\x00050n87dg~è³
«ÙU\x0003Ö·\x000e\x0019 J\x0003Ô°\x0001¸uH\x0008ÎäÛâ0O¯ÊÕö K\x0013ôø7°Ô¢m\x0002\x000f\x001aHd¡ÚÕç~\x000bLi\x0019¶\x0000»CS`R7¼\x0002\x0017U¸°úÜo-M°Ã&¨W ÃWÈB¢ë-ý&¸Ò\x00047þ\x0015X\x000bÂ.ÚNô<\x0015¯\x001dô\x0015ÜêóT¿	¾4Á\x000f {ºT$½\x0007YÚù_!&ñ¯à8á¢de]»\x001fâuuºO-GçÂx\x0019´%u¥8Éë<ôñ3jÎ),sNGw¢L±t\x001dW©y³Ú<bÁwµ\x0005ß
[àQ~+q3·Ñ\x0018ìVÎÁÅÉI\x000f­\x0010êø\x0008\x0007<S2ìåÝ\x000f÷??>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-09.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-09.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x0002k\x0019\x0016WLm¨\x0013\x001a.ÅHÊñÝW5jöM+®âÿ\x000fd\x0010ÿwê±Ý3?;uíÃ¼DünÔ\x0013\x001a/E\x0012ìÞ³ËpO¬h!rÞ\x00165â[K5]õ_¤ñ·\x0014ôjnÜ\x0013\x001anÅ\ð\x0001)k\x000fKW\x0002ÝÕ\x0002©\x00167âN0!÷9¶üvõD/«\#F¸\x0019.òý\x0012ý7¾ÈÙ]f@g\x0019qBÃNtdé¢PK£®I\x001f«8°ÛÀ²l8ÑÄ1Æ\x0013²+è`ªÿÐ¸\x0013I¿[\x000eT*(9-èS¶X\x0017'4ìÄBâ5]³¢j/GÁ~·\x0015u1®j¼Ê{L,-*ä+NµÌ[ñÆº8¡=Õ\x0019Tz%×Bx®)åÁàMÒÅ\x000c·â¡ï\x000c&BW.ëe\x0019	ßX\x0017'4_\x001dçêr+òF\x000cÙTÿ?\x0013=\x0012 $(ÕtuJMsÄ\x0015\x000cPs¤Î1\x001eP­æ¼²³Õ\x0017\x00111#²Y~õÇ§/o¾¾ù§^ª-"êÊá\x0010\x0019\x000f%Ì)\x0008óàµÞ~p½%ê´ÈÙÁàKW55É½Ò\x000fwÍÖ\x0015:Á\x0010\x000fÃy¨·\x0013W,jï]7_÷hÔy\x0000\x0016*]u©
ò%äu´\x0018ùÅÈ¡¯´)n¥Òï]\x0019ßÅEËÞÍ4ÞÊ^B\x0013¹Äm\x0006±\x0005U½Î3ÅpéØ\x0005ö©(!o4CC­:ËdDiI<jø§w_>¾ùÇÏ/´Ê\x0018\x000eÇ,]N#u6­»×jÉô¿¿Rá}$©
|h5¹I3ýj§ò<v\x000bPQ\x0010Éya\x0004X9M'¸\x001c¦­QPWTÁÂëg?ÝM£líå"§
O$W;«º6M®IùÚ&*ù¸×ÎþJ¡+ÕÖm¡½¤|íe\x0010xë«WÐ\x00182sµEanÓO£líEþô÷ü¸/³z\x000593vB£\x0004#ÑQäÖ´2\x0014·°Ä¾ÑçNÊÖ~ª;¢Æé8ªð\x001dÐºJ¶mÕQ¾ösBPÍxl\x001bVadº²ÃV§NáT¨\x0013SÚaÌG¢©nêUÜF û­RQ\x00168öÒ¦È,@óÊ+¥mêû\x0007ôUÝs\x001d¢UaË\x0000ltU\x0015³ü¦¦p²Ëû@MxÂ\x001a åH1¸à¹Mçs\x001c\x001c¬XÈ\x0005^²´\x0017\x0015Ù2×`]9¥iÜ7¿~7ÎÝ//TÊRtRÊ¡§7þÛ\x0002­\x001f¡ù6ÂëLTy]ÜêX÷}T\x001aï£(Â
ù\x001aü8\x001a3r7*ú¡¸>þÑ4Ô>ó\x0005\x001cP|=\x001d\x001a¾&Æ\x0005ìÑ¶1=\x000b\x000cÙã\x001b\x001e\x0011XS¢4>ë\x0005,~â\x0017ÑDøÜHÌ\x001b3%\x001erÈöF: Û\x0005-~«é®Üð0þÙ1Gfåî¶´\x0003º\x0003t\x0008Ü\x000e´t«\x001bÓØ\x0005}¥Ç µÐ\x0018u¦ó{ü3±sÔv[ÚìaÐh\x0010ÄîÊÑTgµß6iã\x0013:\Ð½àò(NMG«QMG°;Ó\x000eäk¯xM2ÖG§(¶5ïÔúØ\x0008ó\x001fÈ	±\x001cÄ¦\x0011\x0013J\x0003Ù\x0013ñ«ôY¯0\x001aÓ\x000eèk\x001fú@åm\x001cOlÊÕZásm}ÂÝ6¼rÆQbúëè\x000eb|åÙÖHfî\x0016»1í@¾ö¡'mîñH(ü	;éÓ\x000cä¸\x000cwûðJ\x0019oÎêg\x000ey»ulá^­c1\x0004^\x001a¥èE±3ô<\x0006¯\x0003úZ\x001bA^î0Ï©S.©\x0017uPk£ÚmX\x0007ôõ	E*^{¥J¿\x0006L±t¥fI=\x0016\x0008Þïcd¤\x001dª\x0016¯¾yÊÇJ7.øV¯\x000bþ¿|ÿ§§Ïß¾ùí§§ïÞ¾Û=±¥÷>=\x0012K¢¤ÙPÅ¹LæóëF]Fð÷){­þ\x000ei*2ø6\x0006)G®±>ws6eï@¾
\x0002ÒÏ\x000eYûT8 IA©swgÊå>A¨s\x001cØ A\x0014Ç\x0012Å¸ï&/êãâöï\x0013\x000c9¡2üc¥\x00113Â×©Ïp?b\x000f`P\x0000P\x0015,&kÒ¨Z\x0011ÞÌO\x001d¸\x0005\x00061².+¤,Ê} ã¯ØþT\x0007p\x0001\x00072cÍl\)|w6®ìsÈ÷óõ@\x0006­ÜT°º\á\x001aCèE}½éwæ\x001cÈ +'÷µµûè\x00183óÞÆ\x000b#ØÁõF±\\x0011céhì61\x0006Írh!lbë\x0003\x0019µr\x0013ö²Çu
:p\x001f[´+#¶> \x0003
\x001aÍ6«S«\x0013Í~eEà@\x001dX/\x0006Ú\x0008¨û~g9Îj­\x0011W\x001f°¸ý:Ùô¦ª¤\x001dÛ»]@p Ã>É×Çøè?`3è\x0011Sï\x0016³Å=8ô»2»°&oH z\x0017ïtrÈ½ñåí§·ïß¿OH\x001e'\x0000§=\x001cGOJ«Ó\x0008	þÕ\x0015lM»2´Ó~"($9\x0019©ã+«\x0014Gìfyá\x000cÂ,cã$&\x0011PÓVJÅÏká®uî´¿ ¨zÀ[WÂ­ÒÅÌ¹Ñd+;m\x0003YXY¨³ÄnÊÊÐc¬åj\x00074\x0014.Ä>\x0016EÆÄ\x000c&º+:O[öt»o\x0008ì\x0002ê¢(õ¨æÆªò¹6[]ç\x0001hy\x0004 !uÅÊª_\ÀÌÃå\x0001
_qDªpï4(§V.EoÏ=\x0007ó|y@VMá¼S9vµ@æ¢¾Gî\x00074*Ê\x001b\x001ei\x0004#êcE\x0019u\x0017ïlÙ\x00074lEi>Ç*q`\x001f¹¬º5JÖ#÷0ø\x0001{Úæzb\x00071×Q%Ð\x001d­> q3b\x0014\x0015§Q\x0008móÜtêÕ¤!Ðð\x0019Ç\x001eÁ
õ\x0014\x0016Ö"W*·wqæ¤ý¾}úöÝÓKÝ\x000e©FU)=kÏ"Õ\x000eõ\x0005\x0011\x0015ñ¯]{.ÓyüïG9.Q#|\x0006ßWÕáúÝ,K¼)o~\x0002C©UTJQñC«Û%­ø1qîo¬\x0003M\x001eá\x0004/=(­¿ªÊå~\x0006f÷gÖ\x000cåò\x001eñÖ)ãz£=4+\x0016|²MA\x001eÀ(3\x0016IXýP«\x0016ä\x0008f(r \x0008\x0011øäY&()½ämµÙ\x0003\x0015¥º"6@÷¬íZ×¸\x001b7Û\x000cn¶\x0012\x0014Ë(*õñCÄxs\x001f°°\x001eb"
·ÞÔÉç¢Z\x000fÅ:C2!Wíý?½ûÃ__¬«g1\i2ÖAÐ\x001eÝãëKn?À\x000f)¾g½ßýØïXs\x001e\x000f\x0016¢ø®¯z{Sf½)\x0008ú`¼³\x0004|Hl®·¡2Ô#s¶°\x0015éB\x000bjÀ3Z3 zan>ã³KÀÜYoÍ¸Z5`È¤ì#Ô-õ(ÞÔÈ\x00172*ø»þMAÆÀjK¼fCy¢\x00157»>ë]\x001f3ÒùÚírêåÚ½É¹ÝðKv÷ë§z©2e	Ü\x000c\¾\x001aú3¶Ùñ\x0011çSÿgÐ}lp	ÔÞtyB\x001d\x000b4P\x001a<¨\u4½FNd(ëH\x001fÎU\x0014\x00109\x0008,T)¥Ô}.³ËÔ`\x0012¨]ÿcl\x0010	Ô]\x001c\x0014{}ÈÒ¹±ªUR\x0010\x0011?¿iaÐ\x0008Ôq\x0012:LD\x001e\x0016>JôD'¼Í¸Q§ Â;*deZ,À4\x0011)­|£!§r@_r*?zaXN½µN½Q:~.=qQ£s¥UXÙÜfå<Fÿû:z³\x0002óø¬±3,¤ÎáÚ{.\x001fM)\x0018[éä19XàùQc¸"º_ÜÈ·\x001fßÏÇË»OO¿z±:j\x0019ó¸\é>1@Ñ¹q´WNe7Y\x0011?À\x0018-Æà\x001bêÄâ
×cÊ\x000cÆ`ª?Á\x0017\x0003ç2&©V\x0002fç\x0018©Jþ@\x0006cÄÒn.CFý@í?\x0016
aÈ&OËØ\x000c$1eÈD\x0006OÜB\x0011g:ßpzc'±L$\x001d8\x0006L¥©¤\ÝÇæ6+=\x000fd°EÌaV^aÄF\x001cúzÍ¯\x001eÈ`\x0018ë7\x000e'¹R)C¼¨1ol\x0011ÙäI\x000bÉÕK÷BöjÌf©ç|zD¾ÊU\x001a3\x0006CI3Ç»Þ\x000cìò$Ð\x001e\x001bÝdÐØ½)\éj¬fË\x0017Ñ©Z¤73\x001ao4Ò|Jr ¨\x001dhS¾\x001fÐ°\x0007]äQ×)\x0013Ðê#.É¡Ý&ÄbOCÏéâX^x¥\x001ayyCïv!Ö{\x0006rÃA7®^\x000eh5Õ½Ü²\x00074\x0014\ÅvG®á)Ûa×íto`Û+ô\x0015Ç¨\x000b­½ ¤ñÂêYßmEpsLãùáöÜn¢òk!Ø<Í\x00074Vª*yàe\x001c×Öø+.§é;»ì\x000ce×T1rAÓ|:\x001aô&G½ \x0003]\x00139<A7²T-#Q<\x000c]'ð3ùíû§Ó\x0019ò_þö×?}ýýûwÿíëå=*\x0007½qæS\x0008QÈÞ(I¸$æ^÷ñPQ]3n&%¡8HÆ~·Õã"\x001a\x0018Z87KÒ)g(±?%â\x0002+@Ä%:d(;Ý,M
)|@ µp§Î¿ÛH;iKÈþ¶ò%)	<7è\x001eù´¶4\x0019K\\x000fÆ\x001fò<Ïj6Z°5éºö4ù	HK._aÈOpGó¶ÓX×&1uJS×Æ¥¨ZFc·M\x001fÈWIz¯P!¾rm]z¯xÍõ´¿'ºv5ÉÑ³²©\x0006ÉHÇ´ß©FiWñÐø&#4s³8ë0´ÛuvU\x0016{´F®&"[NÈ,\x0010Ü\x0014D·ô¨´_ ãÛ²EÕ?§Þ%cÐ¦ É	
Ð+\x0015æ8ßm8joAïv!:[ºÈ_Q' ST£ö¶aó\x0003\x001aZ{ùÆs\x0004I 9*ù¸ú\x000c&J×)QEÑ"íéÇ¨\x0019Ýò®0Èé][¦DÇG\x0008¬zNyÃséÚ3eB7z^âE< y§Ù¬lpÓ»¶L\x000eÉÇÓl©ð ³ºYí¶­v¬\x0011j ¿þ&5ëiQñM_\x001eFÉJÿ\x0001Ò?.4OÑdít9F¯´û,wRÃóAÊTú9DàMz¥Ïì? ¦¨\x0014rDÈÚW¥¿bmkÒ\x0019·ßüã·\x001f_»\x0014X\x0008$fà.É%\x000c_9¬\x0000ÿgè¾íîîÛi\x0016\x001fA#"÷4ÿ]½û
¥\x0013×öÛ¢¤¶ÑHMûUÙkí-ENàDÀá¨\x0015µm7ækÚÌZì\x0012¾ù\x001b8{¶\x0004)mz/µ3´DWä\x0017W\x0015\x000bCbe]û»\x000f5_¼>ruËJ}ÌEÛ´\x0003:u\x0011	;\x0014èÎTå÷7S3V7 6oN\x0001ýëÝM$®ÎÝÃÈÌèËuê\x001eJã|ÂÛ3°ÝjÎ	bc\x001boS÷|B´VôÜÙuÿiz¹ºÙ*ò/.ìÈ\x0016[m?r`þO\6\x0017Þ(A\x001cû\x001b\x0014ÝG|\x001f2\x0005~q&ÅÅ\x001dGpßæðÝ=/ê\x0000ì²ç\x0011¿ïãýüþå",\x001dç÷¯?~y÷ùóÛïß~ør\x0004Ë¿}zÿôáå"åñ¼§_\x001cZ?ÏrQm\x0002BÝX/S:æU#e?©_÷34u\x000e¤SÇ^)ë»BK4ÔlÊ'rø©ÈwY\x00039\x0002rF·±ø4w.)änÝ\x0013'r¢1iïaCV>ÔSw\x0017X:Aêl¬p\x000f#îd\x000c¥+³%ùq\x0002\x0017\x000bÈ\x001cfõ\x0003Ï\x001arµ¥?\x000fdT\x001cL\x0018fåñL$Ä¢
¬\x0013\x0018´"}e¿\x0010Ay\x0004¨z¯\x0015ãÊ<Qä,cßC\x001eïDÏÈé\x0008Ý-\x0015\x000fhEÚ\x0011ç¹F¶»t,U\x0017z5Óì'2ì@vYÊ"eÈzÜ­\x0011z0Óì'4lÁD*x\x0002ÍªMÚÂ¹\x00073=¡a§+7 7Öõ\x001dëÙ²?\x001f±
-ÿâ.x×Ïª\x001a	d\x0005\x0019ÿ8ïzÃnåútý\x0018^Á¿¿aQÛ¨Éò
ÿkÒù\x000f\x0004d`'T´N¨ý\x001fP!'¸Dr.ñÂ?¡íªì×¢þ@ÅÚ±u\x0014\x0006ã(´ÂÐkõP\x0018*úµÓgN¼8YñBÜ#&\x000baÿ\x0013úÊ#Æêô)ãø5\x001aVG\x000fÏüÀ¿àþóó\x001f¹nr\x00010Eô\x000b\x00126Ê.#\x001eð\x0018ÞeÍ&;\·èmBa2\x001f­Õð\x0013Ô6}É\x001aÆuåÝiÁOàÕ7vêÚ[¶¸ÏàûÛ*ý\x0011o¶ÿÄc
Ñ'\x001e'EÏ\x0014É8(Ê3ðE­ ²s]ÆÃojÍÄÝ3{Ì©=6æ¾/é¨\x0018Ï\x0015Ú¸g¶SóC5Q¹q©%h\x0004ZêòòÕÈÅT$\x0012>¬L~óîÓÛ?}|÷\x001f/Ä	³\x0012cnòY¹sd&dQ!¿n±kjlþýtLån±$Ç(3J\x000f|åØ*_gã+$3\x001dS¢ØzðÄ;!á\x0001F¨«:\x0011½õ?¯"½ï¤þ$B#¾T½¯Í.vU¦(¶ñ?GQ
=\x0013\x001d7ùÈI9©èÅ®Ê\x0014ÅÜH\x0016l<ÑiS\x0008ÌÄÓÌÌ!Uæ(×m
XöÊ/eRr]júf¹«r3Âv]?»'ÌrWÕ|êÉ¥\x0004û%\x0011Ç!C¹zä"´íVÊ|êÖ[\x0008HÃ\x0019ÓJ½\x000ebH2\x001cò\x001fØå®ª	ÕBa\x0001_'GËy<é*#B*ÙÎ§UÅ¦ö"Ùs¥-Cuj·5"çÄõªÝbø@\x000e?mÄ»m\x0002Ïwñô *ã3ë`¹~£®ÐM\x0011ü\x0013ú\x0012î\x0012W¥K:7\x000fÏþ«)U"gÓF½ë¾Ô»Æ·¨Hñám\\x001a=¸ÜØ&Í¦n\x001cÈW{¡o"Í\x000e¤RÑs-8~'èèö&73ä\¥+\x0017¨v\x0003O\x000fiL§UÝõ¿n\x001fËï$Ý6iE\x001e\x00049©pÊ£¶Ìö~¹\x0003\x0018ÉÀ\x0013üL\x0006úRáÉu\x0014Õ\x001cÍM^üC+\x001e»ö¤2§ì\x0010§7ã\x000eÌJþ"Ë4¹\x000f¦½c=)Éø\x0007\x00126¾©Î¬é_2>äDµåØ¡Ïü\x0004øZr¤ÃÃ\x0002üâ\x001fÉ@øFg=ø#>Ú¾¾ù×/Oß½T"³(í8\x001bY\x0019ïÎÜyßÏ@\x0019ÆèâUþãBJDF\x0013e\x0018²ÁöªÄSË¦í]ù#º\ù\x0011]\x0014ß Ôª\x0002Ébú=ÛOE¶ÚÞ½ºê~,ôn¦±í=eÈe¦Î´P].	K­×j\x001fW¾"ì\x0014¨q2\x001b%{õZ9lLÝö7±\x0003VÓÆ\x0013*³´8Sÿxcègj0\x0018<È
\x0015$Yz¡ÑÒ£ºWQ2±ÖÕ¾\x001b7ø6äÄ\x0014m¯È[ã­ÌÕ©q\x0018\x000böÍ^á\x001d=;ksbÞHQÊDñ¸Oo&\x0008'v|\x000e\x0012T\x0006ö\x001a·ÑU¿°¯ÇK\x00166(ÌIam²\\U|V\x0008w÷\x0003\x001b-Þs 'æÃÚ\x0018V7K\x0018Ä4Õ3ÂÝãýÀ\x0006÷<B 3¢cz9)ü-ë|Ã]b\x0006ìÙØX\x0015o`³äO~'ãß@çB\x0012\x0004¬JÐ§WädiÎºÇøÁ¸ÛÄ ïÃò¾¾P/G\x0019ÿÔG» \x001fÑ\x000e³m|êW×£ÿ¡\x0000Ás¡n7øg¸\x0019å\x0007us\x0007{\x0004Þ(*¡up¶F÷|i\x001aÏ\x0013\x001cý°\x0012jL.fCÌ\x0003ø4ößÒdÆd^dº{ _Æ1D²ð*\x00153\x0005FS.¦Q~PÏ\x0008/d¨iÜ
ê[U§{Ú6®=&l4£»ùxaD.O?v\x0008«y\x001bÂ<&üö\x0007ÐH.ÇÛ\x001fP+p¶oè`ø"{_XOGuÈUÇ¿@\x000e1?_­æ_7ÿBRýiDô´%äí|æ/|\x0006\x0002_
ÿ2µü@Kd­¯(ÚñW×]
-qKSµÙ\x001eå×y"_)¿V2ÐlR¨´üSílpØCµJë'ð\x0013Öë,Ha¬{\x0012»\x0013÷lBövò¬kQÁ&þÂ0b±ëÄ\x001eª\x0018»+ùoHµò_s\x0001ò4þ\x001fÑæSå\x0016¥¶T\x0019,>·\x0016þk\x001e¥ÇçcfäX·jã2\x0000Ù­\x000cè\x0006«c)t\x0018´r\x0000JEQèÚQË1\x0008ÝZù¯Õö
\x000cZ´®p:ã4s_Z,\x0016[+ÿUÉÀrö×Æ¸è4oe¥¹vË\x000eZ¶jÄ\x0004h\x0012ÿìNó\x0011¹JÝJÚ1£\x0017ôµð$\x001f|±Ð\x001fq8Z[$eõ8.lAÎ\x0012ñÎ2¯K"M\x001efD\\x000e¶ñ\x00025ó\x0014Ð¢ôàÎþ¿ã0û7ÿôñóç¿ýõ¥(´±³
Oþ¤]»mó«w7ÿÐsvÌ\x0017¿æÆ\x001b¹#S¥xOùWaJª\x001f^­ÇÜ\x0003\x0018#"r£sSmD1W\x0015ç¬«\x0013\x0019\x001b\x0012\x0011\x000eGdD¥¾ñLä0 nÚÝ­AIÊLPÅíiÖí±\x000bÃ<h èÖ½\x001c«óc©óD$ó\x001d÷\x0000\x0008á\x0012CM»uNVÆ\x001aTm\x000eº·\x0010%¬\x00176â4ÂrÚ´²A·>D¹\x0007ÕÔ\x0015eÞwÓ^øF,|îÌÇ}-9
ÖÕÝºÀÔ±\x0012{Q4TçÕÂXÎ\x0008»}-¹Pá½+\x00124³¹Æ'ßI ÞZO*Yp\x0015\x0014Ó<*\x0006{twe_::`O7û)"1ÎOO\x001f^èM=4Îg¸G>øpIjKRïg °j\x0018\x0016ò	+VZ¹<sßRj]®§aXÈGì@NJ!r7¿\x0014\x0003\x00189X= '28Æ!¢$ûÈ´©\_tqÃ®OX\x0001.(\x001fç>põzO\x001bK{>a\x00054åº¡vûñNR,Ñn\x001d³'rYØX!Ü'öZWj\x000c¡û§=÷
2\x0019øÎ\x001fY¿ºÂ¤§Z-±\x0013¹ÑÊB~NA¯È°49
ÓPî\x0001\x0015OÙ}gy¼}ÖÐ=wJÙÕf¶ª»¡I*
­Hv¡uBÿÐ!ßíA4µo.4I¢ùÈNñ§òÚª®\x001dÙÞ
Ú#dWÙ¤qÝ\x0014\x000b?a\x000fÇ7&i=÷>sCïnû>;¡\x0013-<\x0017é~'ùmi á[8\x0014ëñm¨®=ç÷·_>¾ûôR²k#z!m¬æO¨±\x001f\x001aL\x0008³ÏãäçGõZ[5HH\x0008H]TÛQºK\x0002	üácóyT¯ÅUO7¡\x0007rt'oÙ'F.æ½p"Ç\x000b9&\x0019²2ªÕÌvz-\x001aª´Â¬üÂ\x001a« QÙº9[oñ|)¤mÖÈ³ëkóU,ñ\x00053JA;ÏÛh|ÁLt¶'ë1«è6¡\x0016z½Mþ<º±?TËÝv\x000bx@§\x000b:ª03\x0003AGÔJ\x0018Ð)ÙVy\x000fè\x0002\x0013\x0012e+­
$¹\x0016\x000b³\x001bZµê3u£êÿ·>üáÅºbkãÆÿ2=$\x000f¶SÉ\x0018\x0008ÊrÄÇÏ`À¢
éKp\x0018cM_o"k\x0005\x000ecEØÒ¦aj¯\x0012\x001b^þb6Ý\x001exFãòKÚ\x0001G\x0000öÓ\x001bÀ¼\x00060\x0017;Ê\x00122øeÚ \x00146õV6|¹Vn2/µÚªÍ\x0007r\x0006dªFW\x001fw×ªMßgl\x0010×´½4Â_<Zº`²]W\x000c=oX\x001e2d|«ôÀJvcGd5ËÙ¡¬Ú6¡ãûr!\x001fá°ã.æ8[_³Þ'r§YÎ¡^\x001cç§ÆñÎö¬Gw©AµÓ\x000c?rÐ\x0016\x000f3Ò{S \x000bº&K{bãzc©i£\x000cr@ÃVé\x0018AuÇ°¾yö**a$\x000fäÉ\x0008L¦iýB«\x000b,ò{­:}ZÀøü	GdÍËîè+Û­\x000ePÁRæUqq=ÄA&£úuÒí¾`à/Ø`\x000fÆÀÊ\x001dc>(}R>\x0019[\x0004È¿üïã ¹ß>}úÛ_þðRTºt8\x001eNõ¬ÉZFõÊq\x0002¼¶jøÆCõö\x0011¶\x001f:,ÄVR¨&ÑpUÞÉé\x0007pøÀ\x0015ÓM|\x0004¨é)î9õ*u\x001a£ÍÍo79r2#]z¬¢$Ýf\x0007áÅt\x0013$\x001fOÍÀCfÝp§R²ta¹iûeË¢K³Ñ$òî\x0003Bªwì%|Èl ò\x0008TTÐ\x001d7Ê\x0011M=¥\x0011\x0015i\x0011¢½IÈ%¨á7\x0016¸M±Ñ\x0007²û\x0006NP\x0014ËÖÏ £7EF\x0007¦.Ç³nÈ1Yp5ùm»/\x0008^7Á'äúH&:
ÏÉÀ¶¨s;èôSOÝ'\x0004«\x001bß)TÜz@\vÜ)\x001aÃ|\x0000\x001bö©\x0007ôõ
}%§¼Ü\x001b§ëÇµ® gïTÜ}Å\x0008ÛðÈvÐUy/hÆi*99ë\x0001û° \x0000\x0014F"ÏµÒ\x000bS¶-;ßÿ1Ù þá[£å\x0017:ÕÇtsoq\òà&èqR\x0013W>´Î\x001cËÌ
Þ1°yÄ¬$\x001aÞ Åâù\x0001ÁÿùñÅlÒ³KükÇÛç¼å]!<eókû\x000füÐx5\x0017] é\x00154ìÇà+S}zÑ´Hæ²\x0003\x0019øÐâ!ÄÞ/ºo°ºMßà\x000cÒ\x0000c¥_ùò¤\x0018Û5¯é÷@Ó+dà%Ñ¨ \x0015\x0006ïBî\x001bC¢^\x0010.V`+KÍ·SùÕÃ}à\x001fÀõ'\x0002\x001b^)E=M\oD\x0012\x0019!6i\x000b4¦³¾³J)*ª\x001cç4V]%)ÈÝÂ¹¨(*m¢Ê\x0005\x001e\x0017É\x001fn\x001c1¬¢ÑY1¸Ô\x0015Hí6
D?\x0016z·SðAõ#¡w[\x0005\x0002V\x001fú4æÚ©M)t¹ÞD¬\x0007t\x0006è0£\x0019.\x000cÍ29Ï¸Û,ðZ\x001b£\x0002ÆðMà½Y\x000f\x001aûfñÉ¿¸Î»ÂçcÂVÏ]åwVÞÁTµz\x000cî5\x001f\x00124\x0011®Ág>CâmôFí\x001f\x0012±WíÿýÛÏo~õôéãûw\x001f^*\x0017|Rât`»¦K½QØ®/{â¥ªên\x000bu\x0004;»´'~xÏVKü\x000c-ñ¹Ì¯,ªJÈLû«¯Ê(<r2v G]óL\x0017J\x0012­[¡ñ	{\x0015\x001d\x0003U¥Äà\x0014«\x0002¨të¦öÏØÜ\x0012»\x0014Ö\x0019_È]ÅÆ½ZA÷|ÕþC§\x0003FÅê±²_Ú¥ÎÄEíÐ«k\x0018?÷*\x0018\*NFå3±\x0002ÜÉ\x001b sò?Å6#Ïü QùçL¬ìÃHÖ\x0000½2[Aôf¦	\x001eÀP÷"mÂA´[U\x0002¢73\x000f{B_ÛOô\x001c û\x001fsI\x001aÚ¼1Oèkÿµ;
A
4R
Fè£>a3-\x000bOèk\x0003F©,ðzÆi\x001aq\x0011çûú®ðÏn¾\x0003¹Fòÿèl7SpØ@ón\x0013zT¥\x0008zá|ðAC\x0007ë.>¡¯]\x0018Ç.T\x0007\x0007¹\x0019-äÝ6\x0004s0\x001e9­¨Wu7ùw't£\x001f%Å#¼Ñù¬<\x0018ÚÚ0»\x0008Î\x0011¡xt\x0016\x0011V\x001c´é\x0014r·\x0012>\x000fd0\x0008÷\x0004\x001a5ÇÑ¯\x0012\x001cm\x0003Ü\x0012ê'´çC:\x00104u\x0004¸®8ËYûK:¡á*ìäö,ÐitÓ±Û\x00016¢§ÌÉ\x0004¦ãCy\x0007-á®[êD\x00182ÝÞMYÚøäÕ1½\x0012'»\x0018`#ÆFÜ=¦ÓTñ,×ëòþ:a\x001f*/¥ÖÔA]³³ÛmDh\x0007¢\x0008ÈÈtké··Òj'.\µ ô\x0000ó©¤¤Ñ\x000eäÝ&\x000cp\x001dJ\x0014ö[%\x0004§½Ev0\x001a\x0018~óôáó»/èM­K\x000eú·cã\x001cW_X[å­b°\x0011n\x001d\x0006=cfø1+Âw³«8õÖ\x0007 ù\x0000Ì¨7N!§¬î²Y\x00040*û²\x001c¥¦{dµáTÔ}±\x000bûÚM$\x0005öüðRh9uu\x0002îÔt'@:	0Ç¤¾H\x0012:s7\x001dbUw\x0002\x0008Ôyf÷\x0002é¦¦L¬|Ý´qUÝ	 ëTÑÒ²ü5«\x001d±2\x000e»áY¿\x001d\x001f\x000cRÅ`ùï¤TÖWì¾j$ì\x001få3ÛH|+§ÄLúÊIÒ0Çt³Øµ/$\x000f!F Ô\x0012 Ýß¢ydÅú\x000bí(éû8´>}\x001eÿ	/tlù º%ëi·+²¨Ø·(ixmK¨»a}ÏâEîlr\x000cø§Ò|&BÉÓü}	ÖÞý\x0001\x000c9¼\x0011¨_¼¯$­6¤íì\x001bB_<{
/rË¬\x0014ë0]*þr¼¡Bàgr_­­÷ýt C¹56È$ñ."ÿç T.F\x0010e%\x0005Ndð¢É\x0019§9V²#ÌAÁn$ò\x000eXr\x0005\x0017òJ\x0006y\x0003\x001fß½O\x001fû\x0019\x001e«:ÃÁo<E¡9\x0011*uá-e\x0017÷\x000fP(
'êÃ2zÄÍä?&úV6à\x0004¾2èâ»\x000e\x0005\x0010\x0001&³\x0010iû&ã&\x001e«º\x0019\x000føårå¢Ü¸\x0014B¶óç;eDÞ )\x0014ãß«e\m\x001fÉ\x0007t MÐÙñÎ»v;\x000fçÉÓþH+Î^ù\x000fö¶á\x0001? ¹Ð\x0014á\x0010d^\x0019Ñ÷6E1¼|äd©& 1:I;!m>×<%­óv^þ"VC}¼\x0001í­âJR£^R»
\x0008<5'ë\x0002·Jÿ&Ò¨êY_Z ÆÝ~@C!kDN0\x001f\x0005+Dþ\x0017ÈÑ4³Û\x001eæ\x0013´Ù¦èu?NW\x0007h)\x001b)Â\x0005
ì\x000f'%\x0010\x0018õØXÜ\x001foJ^ze\x0019\x001fï6b@¯\x0007O}öeF{ã¬\OSÛÁ \x001cÈPñ\x001d/_Ô`è,à7 \x0011ØÓ ÝmÅ\x0000%_©c]3-ÜÖi¦9
Õ\x000c8QÂ¾Bf|ê\x000e°:¾Ï
ye0v;1ÝÃ«¯,x*õô¤d4RÞa\x000ehÞ\x0011äEÆë®î±\x0013Õ¨gË\x0010\x00078 +\x001f$
º²0t©Õ=ÏûÐàÙ\x001cÐÀ³\x0011³\ø]5M{¥;°\x001aÁî\x0002i\x000fäNç©É{fWóo2\x001fv\x0006gA\x0003gÜ\x0018@â\x001cã£ÚUN\x0008÷:Órwéµ\x00074lÅæ@Ù}\x001cMKì9óúXMH\x00067è@­X\x0002/½B¹fq²éÆú¸kº= #m\x001f1P±afék7ê£¦bDzø0Â.çHºjÅH³Ü«zX~ýô¯ï>¾!>P\x0012¹,\x001cIJþ\x0015©\x0002Uì¯y\x0019`ý\x000cò:\x0006Í¡ëiª}©i_I<ëèçh÷¯\x001cÈ(.\x0011\x001bn+¿²G¨®§ÁqèºdZ+6>Õ¢RT\x0002z\x0000Ûí+\x00070\x0014MÇ\x0005\x0006êµ(±\x001b§tIR.¶eî\x000cib×Ðm¬ÊÎ%HÖg\x001dwÝ¾r CX\.qÌù
>*[Ô¼á\x0019u]4\8tN>µ¦MÁ\x00072¤G(PqÈåÉE3wL£NqÒªå}|@O%V\x0015ò\x0012ü5Fâ$.ßt\x001a3MFç<\x0015g\x001dT3_ÃÉ_?}øÃ×·ß}üö¥\x0012ÐüäJ@pä¼ÆO\x0000a\x001aV¶ñuí\x000eBýA\x0012e%¨D\x0004éØ Ýt6×³0ð×Ìsê@Ìö¸\x001b×\x0016\x001c"kçË6÷>Q;'ÎB\x0013T%9g®AÉeÛÙò@y%Ðt\x00189°ÿWò³Xv?©\x000ed\x0010ÏÉ(ó[#vG!2p±\x0010\x000f`Ð^¡v¸ê¼Jr¸'^íæ9uà¡°h*Á÷ó\x000cI½\x0004SØS\x00072äå9\x000fçÔxc:J\x0007æÐ¤Pì>»\x0003\x0019ü%h'AÎ¸Âô.Þx{/hÔü)\x0005»Fk\x0008\x001c(óMÔcÙø\x001d\x001cÐF
õê\x001aR¯rL¥KÙo2:\x0007t \x0002Ô\x0011æúÏêàövNç@=+ª/H\x00179­\x000eÇö\x001d©,ýºÝ\x001eD¢q»4¼Ó³*\x0003)ýçqÙl¬½\x000fèL\x00069/éO/T\x0008rê!RmzÇ	Û\x0010s\ë±Jæx*;ûí\x0003¹\x0011r\x0008tù²¶\x0012\x0017ÙS]í+»5\x001d\x001cý@féè|ö;=\x001dóð°j5ó­¥³ÿ\x0006·£gúir
?.a(S¥õ±\x0002Õ\x001fhü\x0010fA+.¾\x001c>!f©é±ß3vE\x0005ÿêUð'2<~oYc\x0007hÎ§E@}©HJNI\x001cLbzë\x000bkÍÖ6í²\x0006¥&CPYÛ&I\x0017\x0011úÁ:%cU*uî±v7\x0012á6|¡ø@|q±VQí[sÓ\x001aºÇÚÝH´És¤E\x0014µÈYÇ´òì±67Ê-\x0013{$TSá´\x0008H}ÐÎFYÔ\x0016àyrP\x0007®ñªÔåNz\x00027\x0018¯Ã0J\x001eT\x0011\x001fø)k¶Mµ=\x0019\x000eh\x001cÄ\x0001(ÕóÙÈ»\x001fÆû$Û·fàÆLÙ.
e¸jáâM\x001aO]nyã\x0014\x0014¸3S \x0003\x000eº9~¡\x000ch%m_?û2\x0007nnxÑ·\x0014Ô&	ÜøpÙ­
 \x0017ærm¾&øÎãeê£ïa·4[(¶½×ÃµåÎ¡{
\^Éi2©{-pÇçö¸{ö¨´Só;>\x0005\x001a%~b\x001bëÙ34¿ òRâ0\x0012è;>\x0005:#\x0001¼;ú~IÚcgoRÜû=\x0005·\x0013®çÖè$·.BÅÿÛ}Aà¥É\x000eÄ~H~I\x0016\x001d\x0001û9f#W\x001c¸ÛS
«\x0013õAbï§Ì\x0004ðf1ÒÈ\x0006îöC\x001f%]Ç\x0013$²lXâfÏRçt7Òx ãu\x000c~ñóã\x0003©0«¦ô©7\x0018w0Â'ì¨0\x0016Ï
\x0018©0)¢º¥µûñúÅ±®En\kÒw`
óµv\x001f19Àçô!S|Ç¦³£¦yB§ÝGL\x0001 ;\x001cwÂe	Æ¤*dµN¥­´û)\x00114\x0014P}èêQÐø½]ûÖ<ëq\x001bu:,I,Æeý1.¯HÁ0Ò½®.p\x0011\x001d¿ ¹ëîj*#*-ú|¯\x0010¸ÜÑ\x001e\x000c8£\x0015RD-TutîU;\x0004\x0008÷ã\x0003MNñdf^«c_7Ñ©äw6~ÄgþBÔ!CËþØ¤Ó¯IµÙÖöök7	ÿ\x0010(?¯½éT³Ô\x0008¹ç\x0007°#÷\x0003ÿ\x0001á_Âó¤«t:\x001f3©-+ g~@à\x001f \x00173\x0004àM2\x001füP>#9-7Ã{?ü¹èr®¸ÔÓ8)_
§6ºúPµño=Ûú$¨zÿý\x0008VÞ}~¹õH®Õ®ú v÷§àgåñg Ýht\x001cÜôcf\x0000rþ¡¨îP^¨\x0005Ñq \x0004\x0016\x0005]\x0012Ó' Q¥7qæ·Õd1íNd ûÛìUoãÕÓéTs"\x0003Ç 9ØTcÌ«du!;~ó·ºÌ©wÈH1ðØX..ÀÛ´¹a<W7Ò»\x001cµ	O¤\x0002Çll\x0014Í@Q\x001f°4+j;é#É,ZÔ<ËJÖ¤U»Üó@4ªK,5|R$"×»±4¬^6-§31$5\x0006ºµE\x0000R
ÙpbXAÄÍ1ò\x001f¾~ûÇy¿¾ÎãÉ\x0013·ßsy·\x0015©\x001cgc\x001a\x000fÊW×¹ú¡f7ãÒàJ¸P_T¼[U
>^u©øéTk¼ö>¨âë\x0001L¦ôUõH8gs\x000fd`&ø;Âg²ÀÍ\x0012u"°_\x001c\x000cã\x0015éôA;d>Ç\x0005ÂCÏõÒñ\x00036%§)ÑªihAïYóÁWö-\x000bÍm2KN\x001dS>\x0014LèK\x0007
¼ô};#àÔ1%ª@Ð4EpÄ@:ÒEÜ¬÷\x001cÈÀVj¨ä\x001bSS¾gÞk~
v«\x00192¡4¨z$¢ê¹òué¹¯¬cA³l\x000f1ñbN«\x0013\x000bXÍ\x0019\x000bëZèf\x0018pL\x000c\x0001ò\x0007"6\x0014¦¢Ô]Æ+ó¦n.îþÌ/èê\x0017vh\x001a(Eý\x0001Þ=-ÍcàdøÛ÷Oß>$¸óôîÓ»zÃEª§Å\x0008(±ÉËX®ùµ-ÆòÔ
ø\x0001:¹ÊÈp®Sè;9\x0008Òêsª\x0007Ów»Ê^ÝàXp\x001e©wÏ¬\x001aVýÞÐèT®b\x0001@&'µñÒº%Õe»ýà@ö!\x00039ð\x0014»\x0014uStó¨9¡U gÐ:4 Õ¬CbXý¨æ^z@ó^ê5ÈßrÚhz_{ÌÊü\x0001ë¸9ÿ\x0000\x001d7cê=\ÒâoÔyêÙø [n3»ÈL_ýñéËÛ§¯o¾ûßÿóýãÓ×\x0017*UEZ}E+Dm1Ìëú<9óÔ\x001bxÝ\x0003!ø\x001fÔ\x0015\x001a\x001d\x0008cð#è=uÇ	 Zº\x0013»Mè9ÁXN¬\x0001Ñªzé\x0008\x00022ÛO©ýh¼Â\x001a42ä\x0008{+	ñp´ï£o¼Â*ð\x001f8¦&e=ÂPU:Ü°y\x000e`pIL	k)2\x0003i\x000ciã~\x0015ågXS\x0005¾*}¾¤
fµ5l³n\x000eàö
7P÷[§÷¿¼ýþOO¾¼T«wP\x001d¢ò9LÞ*¥¸Pþ\x0019ìKÃQ\x00071A¸\x0010@Z\x000bÖ¢Íê0L\x0019u\x0008\x0013"wMÇÆ\x001d·¡(\x001bÅú4<\x0019u¬!È Á?h\x0015Ð©Þ\x0008\x00112\x0017y×±8\x0019C\x0014#\x0002Øl\x0011?\x0007Êaºj³Öº5Âaås.¢f¹r./¶_0lFu¬\x0011\x0012«\x000cH7\x0003w7r\/ê\x0017v¡dA'è\x0015ø¶(Ôv\x0017r×lìK\x001fË}_þëÇO¿'\x000bô\x0008&\x0019n«ÿí*kCQ\ìÚk{ØÄZ@÷*ucæ\x0018pgÆUÑÁqza,ÆfÝ\x000fd¨5
³ï:s'g«ý\x001cã¹­\x0014ë\x001c\x00019 ¼43Ó)l\x0007þXÞ¤Ô?ºÂÏþé\x000bÀL\x0018t«ò¶3\x001f¸@#8üÎ¹ z2°\x0010ÃbK\x001e^àEýôýÇ¯\x001fÞ½\x0010Ó[\¹BÖÛ#TôÓ§\x0017\x0018s"Ìòê¡â\x000f|\x00196~\x0019ÊàÝ\x000cl#ãã\x0001§ê:Íñ;ÃOE¾ßnkÂáÔ­ü%vÆÌkqÓ@Þ\x0010Øæ·á@v\x000ewP¦d\x0004NÜ\P´î×fã·áv<»¾ÌËí@>/7/"D_-DÉ.Y5oJ-S&£\x0019ªà-ÿâíä¿@\x001fÖD5\x001b±×Q"ØÑâ:¦~¿þùýÓ·ï^ÌÃ¸*\x0006~äàkNóãWkÍ«îNéú!»3qÃØ³\x0012Í±:¶}U½\x0012!Ø&\x0011»ÅdN<Ê¥T©>¿n·nÛ¨=\x0001>^ ÃW]böð8\x0006¸Ð\x001dÌÙÿÇÜ»-Ùu\x001cY¿\x0002ã{Áâ~7u\x001aSÏ°KeõJKI\x0010\x0012\x0008P	@bÌúµ?¡¿`¦¾CÒ_2á\x0011çìXË#vH%1Ö3ÓU)-Äíîá×å\x00072ôR{âDÊÎó\x0014Wf{ú÷L@G¤\x001e|\x001bvÄÀL²?Ób_GMJÿjÉo×þàª7¥>IeÄ;Gôõ\x0017TdªíÚíS;q¿lA­ÜV\x001fÙ\x001b\x000b\x00111¡üVä\x0016V7d7DL\x0006ùË$@d)Ë·Î\x0014ò¢@Í>EÎ)ò\x001aiU\x0018vg4\x0007.\x001fzäMæç-åÈ\x0011]å\x0018Õ\x000eiYýÌå§1¦¼è¼5t\x0019A-¼ðj´ÛÔ\x001eÀ0ÇdicÔY8%¬Ë Åì3*y1&2\x001c\x000fÉf_ÔÎ\x0019näjAï~Ü2ó¸åØà;ÑÅ5¡\x000eÜdåòÊ«r½ÛìÜîF)	çhcw vËÂªª=LäÜj¼C»\x0008×a"fñ$Ö$"ðö\x0015ÖN<âÊÉ±å\x000f\x0013Ûc\x00051fý\x001a¶Úàb:KÞ¶Yëª<C"\x001a\x0003ß2\x0019^Ý·hL5«_õ!vwá·ï>¼~ÿþöÛ·\x001f½¹}öÕwï/%3±ÏÕôd¹ÜÛä\\x001a-<»¡ÒöÔsù¿¬KáF/9ØMÇèöÊCÒU\x000fú\x000e\x001fzÓ¢ ±ø\x0002É\x000c¡v\x001cEØ\x0017ênMÇ\x0001\x000cíTÖ¨Ê}\x0013ÛQ¥è°ïR8\x0015g\x000b8Z50ÿ¨!#o\x0007ó\x000fd¦lAî\x001aÕÒht\x0010\x0014öíTE=\x0014¦ÎîÖb¸¥X8D8Ð4a×¤pÀB/Õås\x001d\x0007V\x001cUFM\x0019Á³i¦*ê0<á^ºc\x0015²ù\x0013&ó¢\x001e	C \x0017Å·ãª\x000e\x0006·¬WhlÒr\x0005\x000bû¹$õñã»\x0018,Ç;.ó¢ö_¥Ã\x0012Õ¶øÌñ|([¾Ì\x0003WC»4>óvt55ZbÙm\x0003_ê\x001bÝ®v\x0003õh\x0011¬\x001a,6Ìø$Ó\x0014i\x001e\Å£\x000bÞ~ý\x0012Á\x001ab¶I\x0007Ü7\x001cR>Ù\x0005®k'>Ð\x0008K.¼uÎW5ï_ã¶@x\x0005\x0006G9p¯vÉÊ+j`|0)mvëâø³ø!\x000bW\x000b¼ª<^&ê6ë©uí¤SÜ\x0015:2­ñew\x0017kÖèÒÉÃN¼Y^n RKÌK\x001fîXO{þÝ\x000b4ú³.b¥^.Ã±§¬2\x00055ì\x0000¯Ð s¶`¨KP÷\x001cÕ\x0010à¨J¯³óWh\x000cüh½EÎÙSìWÙª³½è\x0003\x001a\x0004Údbj)¼¼¼}Eítê8ëÞýãF`Ü	Yo§º`ô\\x001e\x0006sn\x0010½\x0019?É«HMQ,xx;.~\:;ã²WÄÑÅ'¾\x001d^Ù/~äÔt3cOÞ?¼ÿñö®ÑGy(Ú¿
Ùé\x0014¯u\x0008W-\x000e\x00119\x0019ËtOMyn³x¡¿ ÓéøháY\x0000)j\x0001ÃÌ{ä'·ßí;­í&×éøè·2qKfßBî/ÔÔØ/À\x001e-\x00027È\x0012.¦}b\x000f\x00028ìrüúæõO$/2_É'¹¶4µ_\x0010ësÚK<mÈæ~Ycy.Z^_1û¼drGK¬\x0018ÿ´ß\x001dü¾n\x0016ÑûÌ¼t¶!£=\x0010öîÕ¹h	\x0011ºá$¨§DYID}!g¶ûÕYÅl
¹Â8IS¦Ò3Ú\x001cù6Ý÷{d\x0015³5ä\x0002ý]íÌÌø³"û~¬b6We$À={êI+ÉáÐÜF\x00067Ù=\x0015¶5d\PÓÎl©­±é\x0004FAræRAVak\x001f»§5{\x000eT(Ég¶&ñ¤T\x0005nN\x0002YÝha¦Èv\x0013¾\x0014Np*ºjZ\x001e!\x0006\x001a·\x0011è6|Q·ÑÈ·Ù¬xà\x0003ÚÏ>é\x001c\i1(_Jðô!¤âÖl\x0007Te³m|ûîÅc±¢ª¾ì\x000e}ÿ1ÞIö`ÞVö¶;\x0007ÁðÞ\x001aH{õz©2Ï|«Ë©\x0010¯±tÐ\x000fÿÐ6åÕ+ê]3]`nsûÆ-	Q\x001a[a×DWÏhCv\x0010Ý¶\x000bÄã[¸QÕí\x0013Y\x0017ä0Å
Î\x0017ºEØ
¶¯\x0019aøØÅq\x0007r\x0004d\x0003\x0019sj ´BQoO»õýV¾\x000bpÀÖ¡®¦Z(«Ý7Ê1rÝõÀ\x001dÈMô6\x0019È9Ù|£pÍ{É|\x00171í3Y\x0017à\x0002w56Õv\x0017¿_Î;x ×lÀ×	ã
-MæíTp{»"]\x0008îÙ¿¾~óæöãÇêD°EMÂjæ!N3\x0019¬ð~s|7íÎT\x001aÇÊ6p+è\x0004UkKtû\x000cyÐ»d\x0010l¦.¨\x000fdx4}ÚQ×\x001eÈÐ\x0004Û^:àR¶iìr]	2ï#ë«e	zsX¿\x0005<_ã<ÓÔ¼Ï_¡»Ö9±mòMn\Ãå¦Ã2:\x0011VÃ\x0012ôz&ghAL_óXáÖÀÓ.Ct Cs­4bÌ#çÀÕÒTNÀa»àã\x0000\x0006>óbûÊÂãÈ6\x00186UãÙËÀñjX.È0!\x0012\x000e\x0005Û\x001a:^ïÎ,±?\x000c,yÐ»lr¸¿G¼	OÖsÝ)n\x000f\x000fh\x001c¥Å2­ðaR¾³ù4z°;í³äAo²a¬\x0015<-1ùF\x001b¬:ônJ'AüÒ¥òÛï¾{ýá±räI-\x0011KñèÁ41FÌ×4B«§]¥ÜIZ~\x0001Ý®ÎGKS\x0018µ	>Q#ÄÊU4hl¨>u\ÆfæfÛ±f\x001eµ3:ÞzMÜ÷`&=a\x0010*íb¬zÉYÌ×O¹ì{0N¿\Á 4SÃtQíÌM#½!úÔÙ÷\x0013\x0019¹W¾¶¡lÒé÷(|I¸\x0008¾°u\x0011RÉûîÎ¤óïí\x001a±o´é8ï§j¢ÀûÎc1Ü0ê\x0004|t\x000eÂò\x0001©Tb¦ÊõpW\x000fEÈRAh®¬\x0007ÝF¶lN7}ßªtj?¶`!°¦\x0010ánr
n×sÒ«ôlw\x0014¦,\x000f1]´ÚFãâoW\x0017
:=\x001cÜ´ôÒÜE\x001e?Iiì\x000c:ÓB(\x001a\x0008\x0016pCÔËryÕAºe'K.\x001a´7\x000f`ª\x0006Ó©3o*+úËqw@G85Í\x0010I¢¦²e7GôÙ3î\x000ehÐÄËC_ThªFÉÞXXu¦°D)	ãÉ\x0016\x0006$º¦õÐ°\x001e^ \x000b\HÀ\x000b©Þ0¯@6Ê2¹|²Eé\x0002
Êh\x000b.ó.I
?\x0002\x0002zp2ï;40\x0005Ë\x0010í!5Ë¯÷1òm¶(]- \x001bü%ððg\x0013\x0010æ+ñlÒ\x0005z*cr	[
Kbj»=×ÂÚÏè§>SFX£¬ÅU\x0019rjÚe-G2×Si\x000c,;\x0012\x0016Z\x0018ÔîÐ$ ¹c¯ÐgbíP¬iG}&\x0013b¹\x0017í\x0002mW^¯«_\x0003Õ»\x0010°µºù\x001fj%dTL¾¬¼[yç\x000eð\x0017äÜ \x0001¢<;ä69I§ÐMöËsðà$l\x0002¨U5\x0015ÅÀ£âB£´úÄv](úåÍ·¯ä¿øH#+[{:b³2\x0002Óki3'ß&z²,g}ìº@4µÉSÈ\x001aU\x001bÆÉ~\x0018«÷gzáKqû\x000f*Ê<ÔrÙ³>>VoÐFZ ;\x0012¿Ì½Û\fOn_Ð°Ë\x0002ÍJë\x001c|U,
m¸ÀÖ	´Ë\x0012ÍJ
òrb\\x0003\x001f½î\x0017Kû%vY¢\x000b\x0001\x000bÃ\x0017u3X«ìN|\x001e«\x0017G>\x0014úL2,r\x0010ýNnB°çrÁ÷=gÍßÝC'êw)Ô'«x|E:õì-ÇU>\x0014¡EM3ôíSò4e\x0013]¯×½n\x001f}ýú¥Ô¥÷îã»G¨!eüµm/ä¤\x0012© èi;Þý%éva\x0014ÍÚÌ\x0005±çJËsÞ@àKÜ\x000e\\x001d!äË\x001b\x000cWäº\x001fÛº"Ãä°Ë¼ðÇ*júªJÞ7Óyæ\x0005Ùó\x000eÚ«}©Í÷ÝFóW`\x0018InA\x0004Ì\x0016¤öÔaÝ!´OêÈÛÂô\x0015\x0019Eg+\x0015ÞÜ,\x001b:óà<Ç%µGöÌ"ì=\x000f¶#o!_Ë\x0017¤0|äRîU6¿-L_ç¯\x0010)µJàiõö@ðfõ²Ï^¡«¿=¬8Â*ï¬óC5_Ã>¿"O\x0015\x000cÒ4æÈ~ '\x001e\âÑã\x0016»l;\x000fè©\x0001r&BQä¨íêÇê3=\x001d\x0000ÁÒ\x0002¿$\x000f3~A\x0017õm¤]\x0017ZÔTI£\x000bíßþñãë÷¯?¼np´úLÍ\x001bù<WÃ-5Ç-=õ<ü/^Ñ¨ú(x²ÞMü)Y\x0013Ô(ÏÛ\x0012ú\x000c½£\x0019Ã~-ä·´\x001bU\x001c7[jÝ\x0003\x0019ZG\x000b,\x001dîGæýd¾ªOåöÏ¢\x001e\x0005ñ9§dM\x0005ísòN½d{ã}\x0005\x0006\x0017¼ùphbÓ({\x0003²R¤âw \x00072øà\x0019\x001b\x0015\x001arQë\x0014c¥4soð¨A\x001exæÍF=\x000cò@ä-­äUì¸Åµ	5d5áèÀc\x0010cKÙ[þG7_°k¡Á'\x001e³\x001d{\x0011\x0011¿¬®çoÆ\x0002M¡þw7¯Ûÿ÷ë\x000fw¯_þáqÌWjÿ!Ò	ã\x000fóUMA=\x0015.E}ø\x000ciknÚ)óUeQÁüÒ\x0012C#RûÝÌZcÊ¾Lïµõ[$¶K´ÊLî³ò}ú\x001dÏÛ\x0001<´ºAY\x0018\x0003+\x0001ó´\x0014Ëöí?Úxu\x0002Ù\x000bjó%ÈUNFq'\x0014w<\x0007lXXKÕÈ8Ë$ 8¬5¿½yûm\x0013®»G
²âç°ÏPº£pi\x00198?ËîßÄ\x0004§²î\x00066û\x0002%Z¤¬\x001c17Ú\x00196ùa«b¬Np
£¹2PGÀhuiOg8U®Ê)B¥BÛ·\x0015#ks«Ã¾ªÉ¼©ÒË\x0018°ª)»À°\x0010ëkaã~AÞd7µ\x001d9fZJ"í4èEKõ¥k×q\x0000W\x00006Ìz\x0017ü>\x0018ÅÑâ¢zRÅ³ÊówÑ£+d¹h\x0015d=«âYåø;áéäØ?\x0017âcN¯
-g¢aA4!/+ñú\x0014£öÂµØ Æîy¾J\x0007­~yØÉ·ý¿\x0007>®\x0006±M¡\x000eÔþ7\x0014ÖJÁS¼nÿK=LåÊoï^=\x0016Ç~Ð«+LÊñú\x00134FÀsÑ$ò©×kç²øy[hõðº0%#ZU3®AåÉ­+{nW«¹]¥ì íVxµ ÚÕd{"kÂÕÜ®²º
FÆ|áþ9Y§Ä<¼¶ì·7ZMî*ÈHG»Ù\x0001EÖÐ\x0006·ç§¶ÝUjøîûeGz÷eÄ¶l Ù]¥\x000fgö%ð0µÞÈ:{R6(Êï¥ú^Ø
4m¬T:!©ç¥\x0006o9ª\x001d®vLÜoê\x0006E=
É{ñSTdÅ\x001b9\x0013\x0013Ë\x0003ì²\x0001^`)ÖÐ\x0006&Ïý\x000c&åÄg\x001a\x0008N\x000fx b¨³§-\x0000bÑ\x0008~Ûw@ÃN³Hü\x0011R\x0008¢wû;Îw5_§\x000eJö\x0011¸
"\x001a
Êí¶ödUó\x0005\x0018v¥Éj\x001b8rö¼<.\x0016ÞFaÜi}¦P}FF\x0001<¾4âGÐ\x0012ª¦ILDiÜÉ®Ì\x000b4(¡´ÿÀ7¥\x001f Õ©Íh¯<SCØCÂOGf#Y$D3µÖ1Øs¦+vêPÙÁ&âÛ×LhJúvèºco\x0006ØK$ò/ï~h1÷#½»Å3{t¿]B)\x0006W­\x0008\x0013êTa³(¿¨m³jØ\x0012Á\x0004J\x0017\x0005bQlÅÍuÚ§«æZ­â\x001dÕn·\x0016YÎ¼KwÔÎ\x001f¼üÁÛî¼Á\x0003\x001d½Áÿ:úZ´júß^¿úxûx{?¦
+emTL
BfVzþk?D½\x0016'¬ÒEÉ´C#:f®\x0008*bse¿ºè\x000càâh1MR\x0014\x0002Aµ»Ñk³VÛ¬\x001ayzØ7£Ôn±b=òþýíÝÝ#	Nj\x001f[o^\x001b\x0019
¥÷ÔôöÚÏ2Õà )í)óÃ^æ[ç£fìvêOÉ>ïÕx\x000cÕPB²!c=%É`ýòHm'Õ\x0010^O\x001cB?¦s¹\x000f1`ªSå:O¶^e-UfÀ\x0017p\CHVqNH\x0017à~2YMáIêÜ¹v9è)&\x0017ÎÏö\x000epr\x001f)@{{%æA\x0013¹\x001f³Áe.F6wôá¡µïz!ÐÈ·¹î¿~Ùß;ÁKD\x0002V!Æ\x00086é¡º&_ýäk#ß\x0001þr^¹1Ø%#²\x0012Jz
¬X\x0007_[\x0010\x000fð\x0017prb®r²hÉÑÉUZ¼§!÷£ÕnI­4í)\x0005Î>wFÚÒË¼sñ"`þÍ\x001fnÞ>\x001aûråüN3ÇòBá \x0007\x0007¯¯Ñzê,ó/\x001b§[Òµ`\x001bñëÊá\x0015\x0017«*¬T«®2U\x000c,/»â¾»¬2 cÖj»ÌBÚbQ|¨°ØxjV\x001f«·ó®¶Ë,©.Ñ*G½pÑgU
6}P{
dÌBm*3ßÂÖ­kJü%ö:ûÈ@Úþ\x000b©<¹u²ê-á$m{ª{ÈØ¤.ÒáWæ\x000ea?\x0013ç^ A<{\x0005\x0004÷1\x0007¦$
Î*èn\x00107Áè\x0005\x001a¾b"vÇ¨'hó
z·ZÄD¯ûLÞ?û§»Ûï¾{¼Ý"Í§T¼Û.L»R\x0012qv±ñ)íJsË/ZÏ\x0017½¶+ûÃßûÃw	sø\x0006ÿüÃâê>ûòÑú3IT;Ì&\x001da»\x00101OÊ,YÒ;µ? iøò:ùÜì\x0018K.\x001aZ\x00124§1Ç³I}yú\x0012"_\x0018ÑqKÞîÉI\x0017öÍMzÊ«ôT\x001e:Àkõj»»Us^©ìø¦Ü:ð·Z¤§vÙÒ"=\x001dV²Hï©YÊ~ñ\x001e½¬S>Âº»=z¿p^V¥\x0002~Æn\x001eç+Nèe%ë}\x001eTpb%
\x0004Ù¢ÇûÝÆÖf\x001eOg-z	i»E\x0013\x0002g[ôx:ã1·èñxÆXUX Ù"÷õæTÕ¢OénÖèñ\x00189"zû8KUüënMJv\x0016YxûxõO\x0016Î\x0010U]Éyl¦núñä=OQÈI~Ñsª¹ILER®¾2\x0001\x0013\x0001ÑT6è®l\x000eddïN½À\x0000Î\x0012Éb-zp8iÙÔÜ$F\x0016\x0000áÎ¨VÞ§¤R'\x0019£RÌÚÎ\ðÌXm(jál<Þwljf\x0016öÈíÄ=FMM¹N:6£RËªØöcäúu\=sc\x0010}Ó±©©I
\x001b\x0016MÂÓ\x0002\x001d£\x0006²\\x000e{Q+|\x000b~0¬Á/<²e¾]q¶¡PÔÔ$Í§Uîí¿N»hS'¶ûnû\x000b2?KdY¶R\x0015!WfIo>gÜ\x0007YQ34!¢µèvô
ÍC\x0007V\x0013\x001bóÉ\x0014ú\x0005:à»¯A\x0014v©H6[u7\x0013ê\x000c¯\x001d»Õ\x000föjõi´,Ð¡\x0014æ.Ð³0W=/Ô0Ìâ\x0015Jåð­¹n?s= ÝüÙ#\x0017>\x0004\x001aôhÍÐi\x000c\x0017}E\x0007K\x0010ÑÇ\x001a&\x0011Ù}(+ Ò¸µ\x001fº¾@OïFHÁB>UÄZ\x0004êÉÐõ\x0005\x001a<Z\x0001¡étORÌS\x0007~{%3/Ðg²ç\x0002Ü5\x0011\x001bK3\x0019]HR4ýÞuÃäÎÏ%¸\x0010òË
´ì<$ËÞd\x0016\x0005úÌ49èÍ¨òæNQCJ@ÆW<\x0013k\x0007õæ\x0016uÆ\x0010Eoh\x001f[#CÏÒø3©öÐ
5]úÁù<\x000f­_ÃØoÚIµRí\x000bSz_2-Þ\x000bÎ%Õ]365÷\x0000ñ
\x000fÚ8ÕXgc÷Týèyè¡Øûc÷úr\x0002}öû\x0008§\x0014ÂdËåeçTä6¶=·~ö9øH+yB\x000b¬é+¶G_EÛÇÛüèù)z²;\x0016w¦æÈÑÍ1i×Ó·bÉ^²çBÕWMÍ;&òÀ\x0010]\x0008ôì\x0005=±Îð.
ã\x000eê¢Õëæãàû=³¨aZTé¹Ä5SíêñÉõB\x000cÎjÞ\x000bIáL¬\x00035Ï?DaµÀ\x000b±.¨w IuRíLÀ9\x0011AÆ¶1/ë:8ÎíÏ@83¨a\x001aT!÷Ãû0ÔÜË+C÷¾¿p&{\x0001º+U0Å×Ë${Ú}ôþÙ3ÙSö¬@6Û4&Ó¼¹\x00175fp]	H\x0002ÒÓZ\x0010F\x0017fö%)ß×ôÕwñL@"ö+7/âèö\x000bùÔ-,\x0012è3ã\x0014§q"nÆà?Ð¾Ä ü¤1ò\x000cÄ3ùS>Ì¥vs¼0â-_rÉÂ¨Ô½\x0008mò¦âÛ ~FQ0ÙÐ)âÙS\x001e\x000b\x001cÚóÛògöLâFÇâf{Ú\x0005\x0019dºé\x0007nuµ·4!í;\x001bÒÙ'L0Ð\x0001X\x0004Ö\x0002P*mùªÚÙMíì\x001ag\x0017æEÛl(ÌhzImæ÷f;ëûÏ®#Íë°ÞcË(K¤3«½gî²zþì
Èó
hÿMì

Å1tQ\x0019CÓ\x0007\x0012ò\x001aæ©¦=ä´\/ö\x0000}"GÞah/K_Î¾a$x\x0016{©çëÇ6 \x001eóÓùì#æù\x0011eEÞÀ\x0010ik/F5«ç±\x0007ùì#æù\x0011C´s!¤çø\x0002äÂâa/lÏ
dÝÿ0[8-Nhv\x0000
`~¹6t@¿\x0019¹-Åù{IÄßýpûáÃí#ÏBNì#Ú¾ø\x001259\x001a\x001aj®Y/G}7Âs¢ðÎô.Ã­ôj6Eà§Í¦³m}K\x0016^r\x0002 í\x001frÇÊÍi7ñp {Bxá6a6ä b\x0005²®oIÄ7±\x0007þ®öq\x0013çu¬eZ4¿¤bâWMúÞÉðÍ»Ç\x0011Åö¡#¯Ì\x0008ñÚpéÓüï2ÀêºoN6µD£MåQó¸\x001f£Û£¼Lü6+÷u==Z²HWäÉÜç¬Ú8ÞÒ0¶óf\x0014WóåÈK]mÎí³l¿[:#ÿåÝÇ\x001f^¿}õñ¯ÿßcuGÆdq¸ÎÔàã±=¶g\x0010\x0016g$ºc÷\x0019T]Ù|å±\x0011\x0016zëJä©+Ù2ct6¾sÊ},¥ý\x0007Ï°gº=\x001eà0Éîm._ÄÈ½ax½MÖÎ°'³@<õT./=*8\x001f3ï²q2\x001b¶ÊPO]eè:¢üìöì*úêæîÝcmæ\x0008¦ð\x0018¬°k\x001c>kÀNi0\x000e\x0006-\x001f~Éq½hW&ê\x000c9®ãßûÓ7\x0002ù¹ÚOþúÍÍë·æånÞ?Rëfe´Ö×c\x001f|\x0008°3*D3\x001f>\x0007k½$G_Î²ã\x001dèÃöô÷þp1×Kvô®\x0004½ù¼öüóþñãí#Föt`l 4§Ç,l1°6HÒÊ>õ,ìÙ\x0017^­©·ý3Ìø¢ð¢
a\x0006 lMæ­µ¥gNÓRÆ¸`',cD\x0007º9°BÛ\x0013×Þðµ\x000bçK^tß¸YÓ/ß}|óâÝÛ·ö&ª>t:\x0016Ä;§¤åÉ»¸N\x000cj\\x0018\x0015_õ0\x0011	Ì÷Ç¿÷§ï¾\x0006ÄdÿýãÍÝ×·w½ñ«woß?Þb\x0018á£#ó^çhQ/Ò´¦<Z4?\x0003³IÇ6íCH\x0004"ÀÙ J§Ç(aÿqêZÖ	´üáÎ\x0019Ûw\x0005;Ñ¥z
½6«~IÄBó\x0013|öåÇß?\x0016½@ R\x0000õ\x0018
òôÚÑ z®ú3ø¾nI\x0016¾\x00187.B{¶¬DÜiRìQ>0¬Üì\x001fXÇòWì2[\x0007ZüD¥òæXÓö\x001f¯Gx6_¸î¿ðµ»Q¢GúÎ*\x0003\x001dtËâ\x0002\x0000Ç«\x001933O»¤
ñÝæ+ë&|x\x00110\x0019ÄÇ<BT%z\x001fÃv<þ=øÎÑþòªÈË½Z·\x0013Mß§½è¯Ð.ø\x0000»½èiu¯\x001b\x0018{\x001ewÞ\¥Z·ÜF"l#ÓÄ;Í[:¶Ænì\x001d\x001c9`\x0017b
;¿¼&ÕKÄuc-+\x0015¤î[q\x0017z¥LVM$ädZªÆ\x000742#G,'¥yÝ7\x0013µôDÇ2·v¹5g \x0011BØùIê\x001c÷dJ\x0002}W·;pá\x0013ÖB£eÙ-çY»zÍ¸}ÃÊß\x0010jèÙéååYFÂXäZÏ¾aÅohQ
ÆÉ­¹ß)\x000c:´zvÏ\x0015JLÀÌ{'gSë5tçÝ¸b\x0003\x001aÉ­-²${Ô2÷¨¦ }Ä
o\x0014\x0004Á*5}§oÈ³{ÁÆÁ\x0006²Æã\x001dÙ\x001e)}\x0019ßqh::I\x0003
w\x0015Þ{Ð÷nðÌÅ³8à!k\x000fðÔÚ{\x001a6×À\x001dmkgÖÔ¢5Äú<\x0006]"£Ö\x0001ôþÀjä\x0000áqÙ!\x000cfZØè®+ªX¨cÈÅ¦`Iö$©.wÄË¹ODÄZ\x0014\x0011b\x0013\x0013Òv\x001aÃJïÚÞ×¸tÛ]¡aÃ¬ø \x001b%#ªÉ]6öuì³ï\x0008;ND\x001d\x000e¶ZÞ\x0016ÒÔi¹L\x001e\x001cÅ'Ï¢gÑ7\x0005\x0004kÛcÙcã×+¥/vi];°a ÃTh§ßÇÒqlN\x0010IìËv#\x001bØ~Þ·
^]!\x0016C\x0011lj¢\x0008Î{[_é\x0017l\x001faÕÁeªðznÏçÇÑéç ³äy\x000b\x0001¼\x0005[©óI2(4Àè\x0014yL4£¾KYÕt5Í/Ã;qÏ­\x0015¶W­ÝIÂ;Lm©y9^½êýõMùDNä\x000fè\x000cÃk\x0013ÂVäaMNváy|'zöB	òúÑ·Ùjz\x0017Õ¡\x0019\x0001xìa,>uj?°äÏ\x0017í´\x0012aÁÀ§\x0010¸Ã{!û pr?FÕÎ5Ì£ÛýÆgâ.ø\x001cxJ\x000czLu8öKßæ\x0015ÛyÌÜà¦èý{EÓö½¢nã'_°!« K° û%oØjQS3§ãÜ«é½`é<ØQÔ°&M|'¶/u\x001bv`\x0007\¬g±)Éxbx`÷¾{CnéD»BGxé\x0012ÏÐè5®²1¯Ä+mí¹\x0018ÿðñíë¯¼y#Jp¨ï¿Þ|¼{ýêíÍÛ¿û·¦'?êÚjDy¦\x001e°rÆ¦\x0003Í¬\x001e
\x001e6\x001bI;Í«½\x000e\x0019\x001eÅ¬\x0016ÂÄüøîÇí'Ì÷ÿ3GÃæ4¿@MY-]{Ï+ßÁ77¯^¾²?}¡\x0007¹~w#çÒÆªnUûÁ÷\x001a+kCÆ°V$äÊB\x0013ä^¦\x0013×\x000e©[BNWÿè¿EJ·\x000f»ÝÛÖq\\x00135vd"XáhÆaýæ«fìh^À¸4v0¶Ø\x0005±\x001b¶'\x0002#kýð=:ý9¶ØÙ?cçÞ\x0015¾M>vÈË,\x0017C	]ëLÊ±
®ïkÇÆy 9u\¦®\x0018:\x001dÐÖ\x0002·\x0015"\x001eì/hÐ\x0001yÆ¤Ø.LùáØi:\x0016
9Ìä¶Ñ!1¦z±Ë<w\x000b	¾7+ÔD8\x000bÝ°c¦ëNc~»c×m{M®;á §\·g)±½µç¯\x0008üÀ:ÕÍ{õzI±1¸Ã\x0014Ü±î´@ZIJ^9(\x0019|*Wûãà¥]tp\x0016ðØ>×B¢ÁØ\x001e\x000eÎ¢â*.Úk\x0007÷&ðÁÃºSÁ§ú¸\x0008\x001d´VöhbÎ£E¨¶\x0012x\x0018tÐñ\x001c;þ\x0018>¸Súã±áPfòJÒÁà\x0019ÀóLå5pk ¨³Ï´Ús)· åúAð\x0016åÒÉ³c
ª=¤pçè@\x0010eT£Nõ\x000c\x0001[%\x001bxa#\o\x0000vçÂâ@XR;¥ynTÈ·\x000fÞ\x000f~þ=ÝüÂrxW6
C{@\x0012²7\Æ\x001eÜù×tókJ¢b(S\x0015e<S?m¤Üëîükºù5e¹Ç´Y±\x0005ÉØßÎ]XT\çüóç\x001fÓÏ)dÒiÞ0\x0013D<xª>f;ù¬fðù1C³®\x00075?G~ÜÜ Yóç_ÓÇO4YI1s©·\x0013¸¹Äp9ªÛ\x0004½ÚEÿIÎû\x001c¦¿ï\x001fpÿ
´ÂVzÉ{kþ\x0010é1j1Rö|sL\x001enããÖyG1\x0015l\x000eèv5Yíóóêãû\x001f
ø»WîÅÏ¾¾Ýw¬<Ìé\x0011\x0019EÄ÷3îøÖÕMîÞfÏZÌUËÓ:½¦;4?çõËR^¯«q6\x001dÛî:¨Ædøån
½ñz\x0001\x001b\x001eîv\x0015%kZ
Ýªa×täüµú\x00026¨o;·ØV¸^Q}	ìã²¬blx·k>©Æ\x0007®u«\x0005º\x000b=\x001aC'8v\x0015çvìæöÆDÇ.,híw,Rï_ÜÜ}÷vJý×MFWm\x0013ù7MÞÖþ\x0007½\x0004â%¶ÖÄk<,áÑ\x0000#ñðÈ°=¡Ø»b7Ý;I\x001bèq[4'$Ñ|ë}Ûé\x0013å%§ðCj»=¯©?2\x001f\x001f¹]\x0001ÓÖ®&mn.¢å[Ë\x000c\x0012Cç	\x001dÜ\x001c8oÐM]¡	Lv\x0015Pøáeùâ"?ï²ïo±Õ¯}¡gÿZ&A\x001eÛnV\x00153wË\x0003àÍè¢
O+@ÞÔð\x000b²\x0005ãº\x0016»Yñôò!È_ã¡ñn7\x00172&Æf»y$ÝÅn\x0006Lè[ñØ¶²\x000c0ö´Â£\x0008®½u¸\x0011U>²?}´J[M@\x000e_üÌ÷¼W\x00166f\x0013°§ÙôÑÌ¶\x00059µG
æ,8\x0015Ñ
£Kd<Á!2©¸\x0004×]£µiTU1`Ò]@
ùÃO/zõÓF§þõæÍ»µïaö¸\x0005+øò\x0008£;,Z\x0013È#Úü\x0001Yoú´æ8å]WÖvmÜ\x0014
æ5WÒ\x0000§_;}öÏK¥_N\x001es\x000bi:³HÖ9\x001b\x0000Ômuºmñ\x000e\x0016;Þ\x0008\x000bM
Ü´|`û\x001fõíë\x000fó\x0003ÿÓ»¯ß¼¹¹ûö¾mÍ\x0014=6¡\x000cÇ[[ä­=n§ëlìgñqµ­\x001c·DS¨íø\x001eÓ	íø\x0016Ò©ì\x0002ÿôÁhmu(è32%¤)\x001b>®°±H\x001b¸îÒlÀzÓlê\x000f\x001bíýòöîííËï\x001fé\x001b\x0017H­Ç7Î6Mêÿ\x0016}6GÑ<mî¼©Én&2i\x001d\x001bÕ\x001d©c²8ÌOÇD6×\x0001ýmo\x0018\x0016ÏM0Ée>Áë\x0004\x0011\x0015¸óR%\x0004gý5ý+kë?±óaýe\x0006i6p4ï©©\x001aZ!Á&ù±ÙIê¥hÉàeJ~e2í4p\x0017pr«ÇL'·~q?þô?º?|ct]*\x001fëQ)ÄúÞ$òºK¹\x001d¿iÒLëVç\x0007\x0003ÝSÊdHeÃËW´¯3.©ß¾ÿâgß/_n?¿x÷Ç\x001fvïú?ÝÝlæ$\x001eæ&\x0017m&x\x001b®ÎI«\x0019KKÚç×ÿ\x0004Uk×¸©ÞA7}«ãß÷Ë×p¥¤ò~÷	ÞÜ4ïJ\x001eáo\x001fëCÈÒ{<N0öxd4«ùnlúõ?DÖ&tÜ\x0017ñ\x0013\x001eÿ¾_¾|ô§»·ÿNãCïýÃû\x000fï>¾¹½{,\x001f×~&ö!K\$ýùó¯a¸\x0015¿þ'(ú\x0013êæh¦ÊOß/_>Áï~ú.ßÌOðÿÜ>²\x0017Jûn¬Ï
Ó\x000bá6q³j\x001fnûõ¯ñBÇ-i/tü{úæ1þñßoÿ\x001eãÿöîí«ÇJ¸U®}EWêñ\x0018\x0002¬lV¸]Ïâú~	Æ%ué~ÖÉñïýékmê«?`Ëãg<ÉMõ½êvI½IEÔÛÓßÿ/KxKZ\x0012ÿõö¥]Â\x0013À!á)Swp3\x0005»å\x0002\x0005©*%)9úDÌÀÄ§/\x000cËÒIcÑ÷·Ö©/Vµ}õæÖýáÕ\x0013£ùXZk#ê	óuÇ`H¶Ä¹+Üö²½}ÚÐ]\x0018`n\x0003ÍqE:ËY8¦¾}gj\x001a²%Ø]\x0013 !É\x0019Æö©#]è(h\x000fÔï/wÚ\x0013ðKWÇÄÆ®äÏô\x0004DêF©jZ¥IÑ®©\x0003°¡8ä*UprÁ®e©íæÈwb¶\x0017\x0000\x0017±£]Á£åR½÷-vÌÁé\x0010\x001dÀ±uÉLS¹ÜSnÐÕ\x0011\x0002\x000fzgíÜ\x00008tu8Øì2î<\x0010xô|r3HvÏÅ\x0010»:Ö xû·,\x0017»\x001d+`íÉ¥\x0001ÀçÉÅ\x0014:HÿFËDoT²có+\x000fpå2¤\x000fØ¢!nºR\x001d@å²júüà\x0001®<Wð'û%9ê2°Åi³$fW?×\x0013<\x0019¸r×\x001a5àIX¸\x0002Ñ{!Óù×L`T"p\x000cèLõU«¾f(ý¹87+	ÍJÅJ¬¼sT1ÜW
ëSÃb¡zâ¤Y\x001b«>\x0019×p7t¯-eªoÉ$ÿô\x001f>ÀPøoo^¼ûxónÝ~òÀ×z¼8÷¨óû4\x001fêËXïüëç4r¿"ý\x0018¹\x0004\x000eXÉÙ±ÜøJ¹\x0004qØÒæ5\x0002l\x00148×5li|¥\x0017k.ËW½\x000eÇôã\x000bsÊïoÖ]Æ\x000fû²9TzZZrTSC¥è6æ\x001c:8óMØA5UîIX6dFH¡±)"\x0006[µÉ\x000f{ Ãgm\x0006wÚöXeõ\x0015é«åÚÊ²B\x0003Á\x00124'7\x0000²õÜhØâ\x0008n44}²E»\x0018\x0007røÔ3kÿâ@ÎzfýÒ\x001dÈåSÏ¼Ôg¯ÐØ·ü@è3¹³öSïcéZ> §àÉÏ¬æÄ"N\x0005¾ÍI©rcÍ×äs+û}fÁ¢ÅÕ¡7pMhu!q<ûw{@O>µ@\x000fhèomÑsHÉ\x000bc;aJgcïpµ:þ< Ó'Z;Y\x0007ôt±B{r\x000cXÕ8k\x001dwbÚ£\x0014w&×Î|ê©\x0017ùr-¼{³\x0013£Ú£=Íx÷äÔ½á÷L®Ý'ËõÒ_}@CG_\x0008\´8~\x0005rtüúe\x001b\x0016¢\x000er-½¾~6)KUÎ ðåÀÁIHªãL®¡o[Í9Ø¢T\x001eÉÛÃ övgrí WP.w*z5veÛ
\x0015v»ð\x0003\x0019:Â\x000b,4Á\x0004ó\x001c¯£\x0018îÙ¾\x000c»³À\x0015\x0010½ý÷©\x0006ä¦^\x001aÖæµí\x0002µ\x0003yªb³óÍä®Ì\x0016gÙóµ?SE\x000fE*àÆ­4\x001arä\x0003äÒÝ¥Íü@2Ý\x0014\x0004¥#I#\x0004^Ðû\x0013tó\x0016ÏòKò,¿ºùáÇ÷âY~ùîíëGó,ieÚãÊÆ9=d4äic\x0006ïÙñ^ê¤ÿê¤ùIÄÉGcE
åöÃ²ý\x001dã'\x0002kÍ|±ºh\x000f\x0003Öês\x0000×O\x0004ögÈ\x001eßÈÐyª\x000f\x0001Éí¶÷\x0017ßO?7\x0017l\x000bþ{°\x0006òaQ\x0008zhÊ![\x000e¯Ý.nÔ\x0015ÚâsSðiÕ¨®¿äX5Û?öu{:É\x0007
P<äÆ7A%Ô[¿~sórP5þïÿñ¿þú?_½yýþ±RØ>s«ø+\x0005ÌT¹Ie$\x0019O÷\x000e8Èm©ÐÒzN¿'Ç­´>Ý+cÛÆ\x0011r*²´ÑÁxLïo¨l)`d¿è=ý'\x001eyã\x00059\x0015XZ\x000f»¹l¯L0pä&Ú\x0012â²5\x0015ã'\x001dy#êé\x000b=¸þsû\x001f!ë»\x0008à<Ý\x001f¾É:	ô\x000c'\x0016ö`D÷~°'-ì1â¸v'ã§\x001c|&ç\öH{Òy\x0014\M ¢Ã\x0013
VÌ)ÎØ¾vì?\x0015y#îIçQ\x001e¼qÌêF·\x0015öqH¼	£!«¹øÒ|ï}\x001e%é<ÊÃÎ¼Ë£$G\x0011ª®YÊ\x0013AI\x000c<`Zmß´Kv$ìp6\x0010´/PcKä{\x001dL»DÒÕ6ïpXØI²ÊÇíëX\x000b¹K\x001b$6pÆ ¶È`D-ô\x0015yæ¯æp\x0012Ú'\x0015Ú;éO%Âp©`Oä=éá\x0018¸µ«k1\\x000b1RXùQÊÊ\x0017Î\x0002\x0018Ã\x001aV\x0018ZÎðÏ?üxóþ}7º_ßýõ?}õî\x001f>>Vx!dÕ\\x0016Ó»(T8uÊö³¨Il\x0004¿j' &\x0014|aA`éôjP'»e¯
"Ã[-\Ã0:¹\x0018\x0002Ô\x000câ¾$\x0001S^¿yóæ¯ÿ9^Õ\x0016B>z\x0004éx\x0016»Ï\x001f_\x0003\x0004\x0003·Ô\x0002'\x001e]ØvÍl¦eTªZ\x001cÉO%sz8U\x001e
¦»xüUQ^û¾X¬iÿ\x001b>>Y}ÎeG"r C0f*ãW5Um +ï[Ì´\x001bg\x0016Wìo`\x0015T^%Çcâ¥iÁî\x0010#ÍcOí\x0005ûs\x001bá/wµ¸aGì*\x0003ßËvØ­\x0010÷¡Óù\x000c\x00034quÇZO¬eïÀôQÕw:aS¢Ù=g}SjÊ\x001c\x000cçÒé ×Wö\x000c¾l\\x000e\x0008¯8\x001c|aÒ\x000cY\x0004¾U"§S%Ò\x0007&R8K¤$XV"YÁ¶õÂÜRÍ2ªü^Ív¨­Ûea\x000edhÙh¯[\x0004Ñ°P©ù\x001cêÁ\x0018k¿W§Ã-u2í­Éß¢¢ÈLªû:[êd¦LBYyæ".©ûPÝ ù¤LætìÒ±)9]&{(ô¶ ÷ÎCO½sð®\x0007gòü\x000bç\x001f¶K\x001c\x000eÞíûgÿ×ÍÝ·¯ß>VÇ¾\x000f\h×=\x0016/ h\x0002Þ[Ð>ËÜQÖv\*\x000edl+Q	ù¤¬í¨e\x0001Ô{<ä \x0012\x0008¯ÙFêIë\x0000oã{(ð&Á\x0004ÏC7AXÖÏìM\x0001\x0018³JYô
-Ø W×¡r.~É¾Üm\x0008{ ¯ª+5NòC)}¨·G$|\x000e\x0018\x001bIJÒ])DÉU
7oÆ¨\x001apZ´¼\x0017õ¨\x0013G\x001cÇ\x0008Ý\x001awoxþ¾9wvÂ}(\x001cw¡p6¨¤6uºÙ¯
l¹è5<½Àf@~¾|w'6²}¥×oÞ<Ö¥P\x0014PzÉÇX\x0011Ú¿ÙïýH%ÿú\x0011pY\x000bV¦\x0002\íð³q.{5+¿r\x001d¥÷r\x0016í\x001dÈÍÖ
¹ùwÉëðz±è\x0019Ø\x001dØ\x0003a\x0014þáQk'QS
¥#,ü\x001aÆcmvjð¿A¿2².Þr:9(£ö\x0000\x0006ý\x0000>\x000cyó\x0002\x0006ý\x0002îïûÞoµ\x0002~\x0002\x001fvæÍ\x001b\x0018Ô\x001bØ\x001eë2FÞ\x0011n@Oªý±¬1ûT>9Fd¿º¹dz6ë\x0019\x001fhÈ¨7$Öäîb\x0013
\x0004¾U¦öó\x0013S\x0018L¨iÉyqÉ«\x0016àºÝ\x001fþ¾ß½ù\x0008\x0001úº¿¾»ùÐ;5\x001e¹ÁÛWÊyG\x0011êÙ#\x001d®dñÛ>!A­\x0008/Ú]õO\x0000\x0019ùýáïýáoà dþO7?Ü\¾Áwí=Î\x00170>à\x001aG\x0013=ÜÀèe;ïñ#ªZèg1°oPÿE»ªop¿Ëééïýåê\x0013äyÀcbÿêæý\x0007Å5Ö©ØÓ\x001dF\x0002k\x0002RÒ[ñÂy\x001c+âÝf³¡b?ó_çboVÙó-|óâÎØ×8-ûìlì0í¤0ß/F¶\x0014P9·öW¿¢àRAç)ØQ\x0019^¥ðòÿ\x0016Gí´J÷;\x001e×kb×#H\x001cáô\x0015û5M½$üËí:\x0010@ÐnBË¬ª#lÐhM\x001b´[³\x0004}¤BÏ\x001bÎQÕ¦*\x0018F5lâÙõ²<hñj\x0008:\x0000´²¹]-V\x0005\x0019µÒ\x001aV¯ã'\x001e:C'.\x0018\x001bKÁuB'&BkÉý\x0012v&ì\x0002"b*\x0006~\x001dEd7Ë@ØebÛ07t\x0008¶Ãw¨ag«®;¯ù_Â®¡o(\x0007Kw­\x0014ÚtÚ^ýEàÿ
òx&\x000f\x000e}yÔÄ.Ñ1øè?×Çù,\x0004I.[<uè±	^:yî´ç\x001a9ÀAjüÀÅ\x0019LÄD¾S½¤÷\x0015ôö\'-èd0}ø\x0017\x000c!tà6#j¼ÓFtíM pÐÊW\x0010pzvs;Ç'w#®\x0016\x0014³fhÿî\x0012\x001e\x0011I¯DX6\x000f
ÙB:ï-½,e£;ö\1ç\x0008sð\x0017fÃT¹Þ\x001dz`[.%5å\x0019SÆçiA3eK\x001cj}ÁSóª²Îy\x0010rýÄÛvçªé@5KEj7QÍ@\x0007O4~ \x0002\x001e×Q\x000f\x0002\x0007Õ¬°EKîhMääFÝ÷èc9WM\x0007ªY$½¿;°åZÀ©··\x000f®þsÕ\x0003\x001fÁ7E·\x0008N³$
¼pæ¨Í¼\x0007aOÍô41}\x000b±\x0003As'\)»\x000fÂ]ùX\x0018ðéN*5}4l¿\x000e|\x0010ôÔK\x001f\x0006S¤0áHÑ%e|ÌsÍtù\x0013Ï}®sì#È¢Ì\x001964hZ\x0013×Îmºï>/îÏÕgg\x0004ïãÜÂ9c||ý0úeÛì\x0018 p\x000b'¯äXQÈ)\x0007wêRú^>®=Þ}ò­kMøgÀ\x0014\x0006ZÖ
]ïâÏµÇÃ»=,.iØñ9A\x0007¾êËXx
Ï¯dh\x001b\x0002>\x000fòx3vì\x0017~®>\x001e5`È°a\x001b¤[è>\x0010\x001bZ?¶\x001b«\x0007Óa×g{ì+²óVÕÉ»âÏ\x0015ÈO\x0005ê!-|Mï`X a\x0007vÂ]ýùË6ç3ZÀ¼Ì¹}»Þ«=±­\x000e#;}8×ÍOEZ9\x0014ú¼DC$¥ïÞ=ðê?Í^Õs\x0001¯á\x0013¡Ï¯»Îëö\x0002\x0013ñ<ê¼r$$àüË²Ø\x0017Á-ÄÅ>Y2hë\x001bz´Ês«y3kCè`¯dÃ\x001fi\x000f»ÊYiýð
Í©jZ\x0005sENü¾}^ähøä¾/Ï±æôÒ-DUÞÃ÷!ãîÅ&Vü±?ÇC\x000bæP\x001c\x0010Hó-KQBÞO^nîñh'{q\x000f\x000c?è\x0006Iø£Ãá\x0006Ã»\x0000ðÞæ`ÇH*Ê\x001bÄ\x001f×­$ù7ß¿üé-ò#ß
óãË\x000fúèCYBðM¡l\x001f)UÑÖ#Ý'+4ö\x0002þv¹,Y\x001a]×\VÔ6rÜ|c»åÙñïýåË\x0007xõ§ï¿ý\x0008\x0005ÿ³ýÿd.æöÙWï>¾ÙLÆ<è+ÈÔ\x001b%\x0015gfuG\x001cco©Iæl\x0010ôoø\x0019òv\x00124éçdÜ|\x0004{\x0012]¹áTÏ\x0003ÄÂÀN¿ÝìX¤\x0011<cË¿iv9\x0012§2ý\x00155¤zÔ¼Öb<:lKýGuª\x001d¾\x0018\x001e9i\x0018ágÉ\x0000j!úîýÞþÇ-v:üûÝëÛ
wâ\x0003'1ñPMG;¯ìW\x0011pûCzzÙ)^?Ãx½¤þ\x0001fñ÷äü÷ýô¿,ä>\x0015[û¬?\x0015[»¬]>	[Kd)ww©ìÌÚïnï^?ÎÛbJæÞ\x0014ëÑ \x0018¤c¨NÅ
\x0017ÌÏ@2³¶jã²ºáN²^Îåïíü\x001eÉ\x000bp|©ßÞ½¶¬\x001d\x001f\x0000ô;\x0004/¸8Ã4·\x0012W
¼»YË=OÐd\Ñnú¨7æ³¥þJ\x0001ï'OÚd":8>²Ï÷ ¹ÃgòKª\x0014Å6ü¤\x0007°ó7¯¿³¾\x001e¢ßÞ<ûoïÞ¼{¤
^ózÉ÷ê\x001bÇé«`Í4ª\x0010	æ§.à¹-¡WÐ¢3î¨\x0007StNÎßO S[cÀ\¶íO\x0018,[¡qBÊDêÕh¾ïcWZ,\x0001|eiaþS\ô\x0007 sîIÚ\x001a\x0003ôÌ TiôÐ6p¦¶X¢<õy\x0010º\x0004m\x0001\x001bvÜ@jBjc8Ê(¤X{ï=¿í
·í3&Udï[ÀÈ­\x0016f\x000eÎÃo²æ\x0014ÝBùQ\x0018fóSöÉ0zfÞP_r_À\x001b²¶\x0002xã`\x0005ªÌAX¸\x001a£Ú¥GÓ÷ÂVÑ/]w ò½c\x000fêî>{ÿÿ@û\x0011H\x000bÛdÐ!-lû\x0011\x001ejRÛï(ÞsG\x0011öçÈtÕ\x001cß\x0017»K\r\x001cõÝj)ß¸\x000fï\x000282d¸Ù#÷0C\x0019-³~½æë\x0002ãgû ¦?èA\RtNgÜQïz9\x001d9ÿ\x001cêêçw{P¿]
Ù:£\x0003Ø3£âØò}`GNo«¡o\x0019yèËm´ë\x0001àÓõ\x0010Ú¨
\x0007\x000f\x0012¢5Ô¨>Z^3\x000b/b\x000b$ÿ\x000cMs¯|¬þÂ<²ÍU:8M$ÈF:ô\x0014zþ\x0019¤\x0014Âïê\x0017Ôu¶~qÿñïýåËÍÿñc¹ù#õ'¹ Gòºk¥Üo°éhÅu3%EüvÇßðúcÞ-»ªZeÇ-õ'\x0011Û!lßd{?õq|¨3xZv%&»?:p Ëf;bp¨\x0019ª\x001a*\x001b\x0005\x0019ØX¾î]¸u°#öËöC_Ê\Ì#\x0005U5x&Åm8v	×Ñ,cÖ$ÉÞm#ðÓdí¼{â^`!ÈlM-\x000c2~;õ[µªLv0\x0001<\x0001x\x00065Ê
×HàÔî\x001dKéð¢]L\x0000Ï\x0000î`P«Ý|åVÀí«\x0015ÝÆ¿ùàoBV²³]
û@ÉÉ`Èa>	êö5¶\x0018Î?µa>\x001cíÎ[ê÷?ÝÙT\x000bxjµç\x0001\x0013½"®¡\x0015mõ\x0001¼~'¶±ì\x0005¶{µ,8§°jOabWô\x0014<´*Ä§\x0019ýd\x0003\x0010<»eYZÄÈ/\x001cìÈüò®YuòàrÃMf2ë1@ab®H\x000b>:½¸Î¶øãú5_Ü{ú{÷rõo_äâ¡B3Ê\x0002ëZ¨¥v]$Þ¡Ô\x001c9âÛ$ç09WOÏ:¶Ë²À¸#]\x0016aN\x000c9Y\x0002Ø[úf\x001aÓ{Î¬÷N¡¥*0±±*\x0010Ýäuí_Ï\x0013-"ÉÄÆZ\x001c§§[ó7?~øðç7ÐGþ»¿þç#¦FsVéÁtK\x000c2åk15:¦3>\x0003[¼¤FÇ\x001d-©QÿÜÎ/+Ï	ÀöÁ8{9ÚoÔ(cj´b5Lz{Ð\x0018Â R\x001c´Ô(cj4NÎóvó>#¤F©Xd¯Ã"7_6#=¥æ_?¾´ú×·wwï\x001eç!FNê\x0008Í-òGN¤&\x0018Ä«Í\x0001zþäéK6<zq)ù·{ê\x0015Ûãã>hÀDúíN+ô\%¬c\x0016¡\x000bU!
·7äNZ\x0012\x000e¥+òq\x0016IZø\x0015c\x001eÊÌÈ±\x000f6Ä¥=é\x000c¹EgzY\x001a\x0010Ôî°¨ S/\x0003Ä%½BÏµÞ\x0015àXªÂþE©\ÇÉÅ¦\x001b}²!-ÍI\x0017è¹Á&JGï¤\x0010jÐøaö\A÷¾´4â\¡-\H\x0016ñ\x0019£½£¬\x0013OìL>*ËÇd÷¯FZØH<¨Á'6£&yóz&\x001f\x0015äc«÷*s\x000f8¹\x000f\x001akñûhN0r\x000b
Ã]ä«Îë;÷åhÛ?Ò?õ)w»Õ¢\x000f³WÅó¼±ÇzWYRæc'Iïý\x0010þÓgÖ\x000f`}Ï\x0007Áéýéïýå\x000f\x0010\x0006A¦Wýýíg_µ\x0003m¸b\x001eæÃgÎ]4\x000féàA\x0008%OWÉØ¡\x0006³±êVè\\x0005yÝ²#NWCÈ<hª,É
\x001bñ\x0006Vã{¡%Éè6.&cz8Ujm\x001bím+«ñ½@WvðbÔZ-'(\x000fÑ|ºs2\x0012PÅý[ûDïDmÿþöÅÍfÚöa2ã\x0013yÉÍÕ:r6Óã§àKoe|rµõ-&ØïÃÒrÙ®ª«í\x000cºC)8ùäCáô¼çU^íw\x001cöÙ+ôt~Û\x0012gNd°\x0005w\x0008´Hd]\x001fÖ\x0001=wz7ã\x000fÔ³8ïïªêÇO½dWWa¿@OaO)ãºpï<®hÞSs\x001b~Õ©KK>|ê±í:~wÁá»+ß¶C¯NÒnj\x0008'vf¾à&ÎCH \x0019lêþÿ\x0015=óläÉ\x0008¼XÍ\x0005Ú_WE>V¨ßv/ß4i~¤\á\x00150Íõ9úÀbÍa\x000eÌ9#\x001c<1¼eÓ*Aæ<Í°àäô÷þòÝPÛ<µ|óìËGKÌ'?\x0016÷à°øÆÎýUüú§NÕ¤ÉVÛ0v*\x0014x\x0008wg¿÷Wïî>+Aÿ\x000c;¢\x0007æÌ2;Ôu2âÚfè§»Üþß§÷uN´`õ\x001a\x0006ëV\x0002\x000eËíáïûÙã;\\x000eôæÝË+\x001fzGÎµã\x001fOß4
\x0003¼n7Ï¾n_h)\x0014\x0007³ûRéþ/¤åú8²{^BésYòkKlÿÓ±ÁµÙY\x0019 zÄÝÍûö1þîýÇ»¿»||.ÓôÅÏ\x0012hlþUM¢!w±h\\x0003Í\x0012r\x000b\x0007¯fûaÉ_\x0019«,¹K¦¯¢G\x0012
oýa=ÎÎô_fÒðí.|\x001dßüþ&ýñã\x001d\x0018Í×\x001f\x0006åoî¢¼{³XÎ\x0007ÉAlþïL6\x001cÈª½«\x001cø<Ö¶ë²²\x0015©<¾ üÞÊªõ%Õ¸Þ\x0018j\x0014áj9Æ\x0011å'pK^ûùifºûÏ\x001ft\x000cî\x001cÛ\x001dØ¾\x000eâ½+¶pX!t°|³u\x000cÞCû	-\x001b¶-@G¶x¼C1¾v\x000e\x001d&t¬ÏáféùXVc@§u?\x0014AÇ	-ÓSyb7o³ 4Ôê\x0006tXX5\x00089Md\x0017\x0005ä\x001d9cSn6ÏÐ}`(cçííò\x0017ì8ÜÚ&ñJÇÎÁ/¬\x001a]è²¯#\x000cýÜ¾ó\x0015ÃmÏ~ß]VV
Â®\x0013»£\x001fær'hË¬>¤ó+±\x0006b\x001f¾}S\x001b\x0013¤K	éL´ê;&»²j\x0010òTHâ14"Èí\x001frx#Õ\x0004\x0016m\x00177ÄÊ\x0004\x000e\x001a)ê
\x001a)½Û|'¯ÛÕÍ\x0006R\x0002\x0007\x0014\x001ek8¹K8T&únØô\x001dEö\)m85%6<7°\x001dß\x001fÛ3ÎÕÒZÖBBØsÇ\x0007êVÆ0ß¹fÚ\x0004bP{ú*\x000b\x0012 Þ\x0017ÛYÔí¹jÚ©2u8%Ü\x00149ø
<=\x001dÛôâ¿=WM\x000bªYó±O¤{dý\x00076)&o6¨\x0012x¥ïéç÷zká[ñtå±\x000cösåt\x001f\x000b6ê³g\x0006#¾;WOêéñ½4ÒÔäI=ÙÐÊÎYÀA=Óä\x001bé'ÏJ=MVßÓÚYÀA=ÅE+\x000f\x0001}ôfjûJx<ùn*~&iQ\x000enõÁÃJ­AØøjº
·\x001fÜã,¬<ä¶wª\x0007w®\x000e\x001eÎdèV$RÞ\x001c\x00076,êÊ«§3aiÞòs\x0008<ñ\x0013t¡,;×OW\x0008ü:Ü
KUO>äÕ2}¡ï¹~:ÐÏæÊz|i¦¼û¢Þå¤G\x000bÓ7\x001füÝ«à¢_¹vo}u÷îõOòÿï\x001f_?VÀælRwé®¿¦ý£4w1eåWðÓCñf\x0013_k»3®MùéB=:½RÃëhÛu \x000eÖsh\x000fÐ\x0004)%dk\x0016ì °û,¶\x000b=íB{ã\x000fÒ®^\x0016_(\x0019¿-Ê\x00167
ØÓ.´\x0018ý`\x000fè_µ`î¶\x0018`N\x001b\x0012\x0011W:ÂfA$\x0006\x001f?^\x0004*Â¦\±\x0008T[\x0005ÀÎznm\x0014\x0000{\x001a\x0005Ù-\ÐÁ#ºU8çÆ£­ßÕ	\x000eNo,áàõèBt
\x0002îÅqýÂ«~ü\x000eôT\x001d\K:¨T.Æ®ÜjK<\x0008ßtÿôD·³º½º£û¸Ýc\x000flC/Ê´íÃíÝ=êùüùÓTt\x0019ùaMö/8wÌuö+¢\x001fÊÊ.Ùe]ß½ÿåâA?Âûþ	kèx\x0018é·åîÛðâOÐüÕÍ«·kSé\x0003s>>D\x001b½¦ÈúØÕÔÞTm\x001fX}ò´åm
ê#kRFÙ´\x001f\x0005Îw\x0012N}ôÖB¥_ß\x001eu#\x0008AÇOÖ&\x0019 Ó'B×ócW8¶=Ò×Ï½ð\x0017Mè\x001cI"GÊ§\x001f»Îc_<\x0017èvlT(í]Xë¢=­½
àñ9bgW<cçº!þ\x0001p\x000bÙ;s\x0019Ð¸Þwó\x0012|¤û¶¤#¶GQ%`É\x0010/øxÌ;ÈÉ-Õ]%_Åþe­=\x0017Vóé½Ô<ïÅ¤ér4\x0002yÁí1\x001d:\x000beö®Øv¶\x0006·oß.<%ÃY\x000eo(­Ôîårééìbì,'{MÓ×~=À×yzO·&G¯íô.\x0013z\x001d[»Zh\x000f	9»¾Õîzx\x001bp±L\x0003\x0015.\x001fä\x000b[T>¿ú<\x001dUÙxå\x0003À;ìmºdÈÈ\x000c\x001dgí\x0001|wÓ@ÓGÚhÖ.ÇQæM$~$\x000cOÒÎÕV:|9¿\x0002ríÑn'ð
#ãÝËBk:½±\x0017ø33fçRoþSb=i5¹´Þ\x0011|\x0019¥ø\x0006ø9ñÝàc@;ÔyçéSfÁ\x000cf,ª;5ýOAÈé`>ïS\x0017±Ù`\x0002ßý \x0002sæT«\x0001­
ö9MO\x000eÏÓ\x0003ã]?½\x001bÓðnÉgMøÏê`\x0013Ò`?l\x0014ÂÂÈZ;2«nI$\x0000<\\x000f|zÇù \x0004§}êÅ\x001d{{÷æ½½²XFÿòÝÇ7\x0016å#
±Xï\.ì\x0018¥}Ôt°K´ß!tÆþW\x0008òÛ¿;Ñ:<.#ñ\x0016èÍÙò\x000bÚSÐ3.£Î<^E­a\x001d'v{¨ \x0000ò&sxU8
]F¶È\x0016­\x0000\x0007¸=Ðl¨9È\x0002äàÍ/1\x0008^\x0003»ôÍºX\x0007m|®ðvò\x0004³CµesvN/^\x000fï,ú\x0001ïf\x0016=	ÿCkOã§wNÉ\gIW4]üMN­"©\x0001Ì_
7³¥¯Z"EmÅôb¥q\x001füO»\x001c­¿º
ÿ¾TÝíû×ßÞ6~öõí¿ßÝ¾úøúÍã(°<#\x001eÇY9ÞåCD\x000f/°¬ ëÉØ'Wa×é\x000f\x0017\x0015.ÚZ[ûFH[Íü\x001e²ø0§!7]\x0000fâÔy'ñ\x0002ü ööEç\x0001\x0001Ý~*z1´\x001eð¤5H{å!NÁ§aVó¹,\x0015©ýXsÐ"Süö7À\x0004y~âRp©p;âò¦knØ"­¿ÿéÇ7?ÝLiýÍÚwº}ö\x000f\x001f_Ý¾½Hì³¯ß}ü°nWzhn9Gö\x000fÒl\x0002i	ª·dàé¶iË¦ãx)jõ«SÉå,Õ\x001bø	@7;ÖKf©iMì\x0019FfïñMJC
;DÆ¶vÛ\x00052±g@e \x0019â_Juzhþ\x001bÀnþ\x0005`Hÿî¿é½ò°k§Øþm\x001a\x0015\x001cE1Õ#v²\x001cµví\x0014\x0013{ºrB#à!¬®­ó*#0Z5ÐÄ%¡¦\x0010¼PMUòøIE½ÛV\x0003\x0017²ÊÉ\x0019,\x0011dYÆAÐl/Û¯[trÞÿt$\x001b³?fï;ºå¦ì©fø \x0007\x001aÒ7ïþè^õ\x0016Ðk²ñûÛ\x001f^¿íD«7Mm_Ý=ÖëØ^~öÂü\x001eE\x001eÇ^ùf¦Ígô6f­WãÎºù\Ó\x001b,+Jg\x0011T[s\x0000Ëêûï\x000f]>}Ö\x0012
è\x0015\x001c­¦Æ\x0014jµØ]æ¶\x000e/t)\x0015_áûÃ\x0007Ì\x000eö/ jB5;î\x0018õ}ÀÏkrB¾\x001b|\x001as8&?ä\x001f°\x001eÆüär\x000c¹¡Å-+\x001f\x001bÚ\x000fï~@ì¿¼¹ûðúöîoÑ\x001aYJæâ]§1¿V§\x001d\x0006ô²»ëW¨¸^ÚÎrõ=Æ¥-­i»_pï_+àîÍw\x0001Æßþ
úSêª×Î~iît\x0018\x0011[{ÿÁ×*ÿ°Ù$¼Ô½ûeéþTS°\x001b³T|\x001c¤Õc§lüÎ3\x0001hlOu\x0007¥Ò\x0005\x0012ÜÕkì_jê\x0013\x001bmR¥þ{r\x000e;y(	w\x0005õ	Ý©áXvÔ=')KQ%Àº-Þ\x000064ÚÀÜ\Çv{nÁÂÞ\x0015o\x0000\x001aÚldQ3öëzä³kÐªï°ô%gK9}BCô\x0019³\x0006E¤É\x0010[ýÔ\x001d¥>±Á\x0006rÐÑvl\x001cËv|!Ù;\x0005ÐÜ
Í©±bÓ4©©"hµoMÝ©\x0011óð6%än\x0014­á\x001b)¥o\x0004
ýo1b¿mþTà~)Î$oË®=\x0015ÀA#óøv\x0007¸ï)+hëV½¯>lÛS\x0001ÜÃ¥djÖµ0¤î±/s­öTÙÉ]ôÍ|áêRúF¬¥;\x0015°§VJ>\x0014ýmû¶T³©)ê]s*`Csª¬ÂææÔDwUk·-i×
àØj1é.Ü\x0002l j8L#h8WLhN\x0015JnHÙI~?úDÕ3\x001a\x000eæT\x0000ÇæTµ\x000eÓl9\x001boO¥æ\x0010k÷Rdþ\x0004§æTG·"¼ªe\x0014?Î\x0011³t§\x00028jgB\x0017UØØ¹Ç³Èà©ìºS\x0001\x001c»S©5ÄYõ9
·êÇ8ZvÏ\x0013S³¡³ÅVd\x001a³\x0013Cõ»æT\x0000\x000fôB\x0018<¹áfcÝø\x001aÆk'6§zªê\x0019á;EÍ/Â×0\x0006ñ\x0003°áÑl\x0001Åv`û#\x0004[õâô²ÏÒ
Øðj\x0006ËÝV±ÏA\x0003¶n\x001dïméKE	À\x000b\x001bì«\n+;
\x001b\x001d»çÚ­©.ãðpõ\x0007ºXøåô±?ÊñT\x0010åOhÉëô&\)ü¾Õ\x0018è^r\x001dO~<Ä\x001aq¡â\x001b$=ØT(¬ªÓ2»ÑÃr*.5¢1÷\x0007s7oj¨5³Ï\x0019¯\x001d2§\x0002S#\x0008ôãA\x0003-ýUBoYiÑÔI§«&Kö\x001cüeg
·aW® ìzõº¦SË%Þ'ùCB§Ã}ØÁ²§oÍ æ9\x0017\x0004"S\x0002ÜL()rñËDî\x001e
£o`íeèÐËâÛ³	ÆKJ$<ùâ\x0012G\x0012±/#¬õüì\x0015ÎÞlJÈpvMä©×\x001eøì££ÐZ0\x0016,F\x000c±Í68YÓ\x001eeÏoF¸t£Ú06,\x0008\x000f?\x000f½\x0005D×	Tüð¡ãiï:\x000eoFùé*ñ-ò¢$°)F=¦~>}X;	´äôÏë«\x0011<¦¯
\x0000ù¿´)¹\x0019v\x0012]Î¾\x0004Æ@V\x0011ºê¡\x001cÆØYºÚ&<tµ5°ÓS÷²~æwJd59òÝ?½}\x000b,ß_Þ¼½Yèa\x001e\x0015IÅxª*ø%égw¥=«njTMcùögE±ÉMéwdÜ\x0012g\x0001\
\x0001£°f\x0003PxbªÀE×¾ë\x000b3µØ\x0003vØÞ£g Øè\x0019$Ù'¨°í&
\x0000Øib7°\x0019nTïÔ±Mâ¯æÍ.
\x0000ÐyBÛ1µwÅ¶\x0005÷Ê7(¯Äæ¼I\x0003\x0000ö¡ªNPb\x000cnf%j¿ñÆïfT\x0001¹Nä\ðÝ«Mpþ5\x0015r\x0008\x0004z;£:±g\x0016 aûc\x0019lÃ.5?§\x000b	.ÛÕ²R\x0005ìã½vÙT#GêÍ³ 1¸fRÚ¥\x0001\x0000ÜMðöj@ÍFÀÑ\x0019Hs\x000c\x0002^w¡:OÕi\x0008s¢U¬:¤RÉ1xÙN\x0002øÔ"){8y(¸Í¥§¢®Å§]°\x000eàSy¤Ë\x000c»öfÐ´g³y%<ÞüsõÁº\x0006¼é!Ué\x0001C¥/6+{\x001aË.X\x0007lPöÒ%Pûl±­)Êàµ\x0002\x000fu\x0017¬\x00038hP\x000b \x001dHbû\x001f=ÜU*Õ¶h ìõ	îP\x001c¸G
¼Pî¥}M\x0005zñz	Ö\x0001Ü\x0002xFÿ¢6uÅ\x001cF\x0010ÁûÑ\x0012¬\x0003øÔ!!1r\x0011\x0016\x0018¢°\x000bÖ\x0001ÛOS+¤;`´¤M
¥\Öñ\x0010xî#êK°\x000eàð´HÂÒäÒ±-F©PïZüQ\x0000\x0007\x0015J\x0006Àû\x0002E~$\`å¯=Á¸D½\x0000bî@?\x001b¸z8U×Rã6ê\x0005p\x0010óöV¬\x0014K¬\x0014)WÃß3ûÞTt.å\x001e¤Ü9\x0012ÄiD=±«(ãÕ½ýí\È=\x0008¹uÐN$é-\x001a$m\x0016Q	ù`aðçBîAÈ½%dGWRSÈEêìáØX¿éß\x0012cév%>m¾¥?\x0017q\x000fOP\x000bGgz$éæv'\x0014¨·À¾wÄ¿@~¾@Y\x0008nó¹\x0010
Åð^¤>W\x001f\x000fê#º\x0012îX}2·òø::ÛÎ\x001f \x000f\x000fl. hCw\x0012]PØ]NÎ5ÓfÊ?|Ý".`\x000bW6%õ,?×L_áÆÉ§Í\x0001\x0017do.<õk8×\x0000nVrXW¨\x001cÌ\x00047o%×
\x0017$O\x0019Ï><\x0007_¥îãN/+\x001bmú6¾s\x0011\x000fSÄ³s\x0016­ÍÍµøä7­gÒ^¤¿,«þ\x0008\x001cdÜyH¡K?gI)g¿sQ	STrû~0õTá·g\x0013¯QÄ Ø\x0011Ô\x0007¸\x001dªôïÐì\x000b\x001fÚÙ
©5"Ïhßå`È\µÇ¼ñÌ\x0011ìðüËÂjMØ`Áë`	ä»\x0018víÙó%u\x0006Ø\x0015sÊ`Õ¢¬\x000eÞ\x0014¢Ïe0æàß½¸@ìIXåHôa¤t.	\x001c}IxDo
QrTïCî-ãé\N\x0012ÈIØª_e¹"9\x0012I²Éo¶ÿ\x0012x¦\x0007"{2´,à@	1´ý{kO\x0002CkËs\x0014Cj¶WgãÂ[F×\x0000\x001b< \x000fªÖË{_ÙÑç×¾7äs\x0011ÏèWPúd¤£\x001cq\x000e	aX°Ï}\x000c>J¢BK\x0015VtB§r\x001ea³o°§';\x0012ÙG>¥Ð¼]I O\x0019I¾S9´(òY°³ÉR\x0002¡&j5GööT\x0010-
b¹°\x000f\x001f©\x000fÃ/¦òÅËæé7µôM¥¶ÂrV\x0006)ç§/è®\x0018 »JBî­\!Ã2cGÿ3§ð\x000e³Yi²ûö(8"ÚÝG\x0015KÄ ×½¥oÞ6Gó§
m«Ý¬\x000bMb½Rd&'Ä\x001fÓsi\x0011~ÿ\x001aOÞ®*øóÍªã¦t³jó À\x0010¾\x001dØ\x0015!ýäÙ]¦Â×^U\x0000)Qu¥\x0012è°/¹}qjGiï}¯ê\x0015{U=9Þ\x001a®ë!¢³»°&èÿÓÍÿPP~>þþÝ75ÊgÔÜ¶ÏÚ\x0014^²X§\x0017½>öÑö¹Ös¹©^1\x0005Êío¸÷ç/àúêÏ/ayÚ?¾ûx÷öõ_ÿóqÊ$%\x0011ET\x000cÇî\x0012è,`x0\x0018Ú>±ªl\TçGs¹¡xä}\x0012\x0001¬ñ%Ì\x0019á}¯±Å\x0007<ÐËô\x0001´KBU¹Zf÷}ý²\x0017fI']á-¤ÚkÑüH"¬f:¼Qi\x000b\x0013@>;}ÿÓ\x0015^6¿ëP\x0006íÀ\x001e3õ
á(ü.Cp\x0013}\x000eÁ\x0005áw\x0015Ô»\x0005
ß
{þ21²LÁ\x0001¼ÏcÉ\x0015>r{mÓ=e¿æ¨nê×wÂ×É\x0004p"û÷©Í\x00187=Êþ§ãðÍ\x0012ÀÄW	Ñe\x0005\x0007\x0007=Ý¯fa:ºÂ÷?\x001drã\x0002ò¤Ôö[Ðu(ÙG\x0016ú²sç~ÿþõëiv~û¿ÿÇÿúçG3ü>0Ïm5î¦Æé÷H#ë¯2L'SX«ÕqËÌÑ¸¨o¤h0+û9y$'n±\x001föÉ8\x001d·ùÜçPV²\x0001@9¬¦¸38\x000cB)/»7<BSýf.á§þðû?\x0000{Òoo^¾k¿ò^&$aÑ«_\x0018,µ?&!rõ¿_;±ð2°¨Ø¸©op\x0019sû\x0011³õ¡\x000f\x001d¡Yö«pM¢GÉV\x001b6@M8²g\x0000ÝG»#Þ¬7\x000c\x001eG#ñÂè\x0003à\x000e\x000c\x000fF\â¿S?¡4³q¨ÖA]£s9~ärP;¨8IK\x001fñÅJuÐä/ë\x0016B¼8²]Ûyö¨m¶É9çDB\x000cã½Ò! G¸ö\x0008DÉd.gËkÉïIîµò²´\x001dèe¶y\x0019Ã}ý«â\E3ïJdB§\x0007)K\x000e
Ðç½çêð«6Sñ\x001cÁ¥ðÏ×~¹3ðþ§ãb¢\x0005Æòdeî\x0013\x001f\x0013_\x0005Jæ\x0003þ²%Sð@¦$â\x0000¾X_ä=\x000bé6\x0007¼\x0005^\x0016	ú!H·2\x0001\x0000èÜaÕüõ½tWLìÙ]Ñ\x001c\x001c\x0003]-óä[fùm|ïõ\x00008whb\x0002T\x0015\x000ca[q\x0015l\x0008Ü\x001aÿÍF~Vþ»»Ç\x001aOZ÷¢³µ:L¼æl>9Õ¨\x0015vÜQOÔÏ~Qiáî¶f)ù\x0001\x0017.:üí²2wamä¯ð\x0016»ô¥\x0000;Qé\x001d^-¹GÑD;üRHè³l0Äu$³ëÄ\x0007â\x0015q[\x001ar¿¦í&üLÛÉ¼	Èê©çÄ¸ïÛû´!\x0006þCño>\x001a\x0014L\x0019¼}».u|`û_Í\x001d3\x0007£«²£\x0017Â*\x0013~ÔÂ|\x0006Ý\x0019WÕT\x0015p(TÝþ\x00173ëfÇ>ï\x001d!ó(\x001bD'U\x0015§«²kí0ò\x0014.=¯\x0000>ë\x0003=a¡ã\x0002ðpd5x¸Ìé½X¸\x0017/-º°\x0005Cº±\x0012<ãÙ0Rtnõ¿I?Åð#Êæ¿ß½ûøh±O¤¬³¯Ý[¿X»·	È\x0018	|ò¾ÔÜÃ³%öY¦ûEq\x000fô\Ã¶Ð¢\x000ffûHj\x0000I\x0012*;Ñà0Ð¹¾rùzAÙñ\x0000~¤÷ÜÒ{\x0016É\x0004ì\x0002ØÈ\x0011d\x0014²uí}\x000c>Ö¾h?\x0004À+W .\x000cÂ@äÑQHÞÀË¶ö;Á¡Ó[
L0~ ©\x0011u+D¥éûXÆRú\x0005h\x000bÐ\x001eªø
\x0006á\x001a´§\x0014Tî\x0019®Å+\x0006p|d\x0013´§=ÄýÀ\x0002®Ý×i/~%`{À.À\x0017HÏM
\x0002
{[U\x0006è9ÂSd
\x000br
øumÐi[U\x0006ì\x0008ØÈÙÀ\x0013\x0006
b<¬:wÙ\x0015\x0001;\x0001vuÃÎ|%!¨s÷1Å'\x0000lTL\x0007{\x000e0ï±|Û¢4ÓíJÊ\x0019ðÊ%ê\x0016l*\x0013úfEó®¦\x000cà,\x0001Û"³\x0010î±(#üÈçzA/c5¸öô)BÃã
¼\x000f{-ÕM\x0000·d®,hfT¤9Í\±¤ä^<]JÖ\x0000\x000eÙjásFZ¸*àÍÕXTµ¸\x0002¸'[hA\x000e[éØ\Qö³÷`x)\x00038(§Öpç¡pr,ºÌV<õÉÝ%c\x000eà\x000c-ØÙÀÄhbgÙ\x0018¦Î7µÔ\x001a\x0001\x001b´39º0`À¬0tOÆ/´¶\x0000É`K7!\x0007Ã2ºQYÓ\x0000\x001bSZ¹áNbfVýÈu"ãýNÎ3W²1rZ2µÁv.\x0005	^@;3Îu³\x0012ÙÔª÷>÷¶½¥<\x0001àl­ÇÞ~ÆV÷G¹kg\x0001íÌÞ6Zk&ØQ9*=Su®\x0005t3cl× +Nu	vRØ}ÑÛ¹j@Ø\x0015\x001d,¾yw\x0015v/ÅkfÁw3\x0003qÉpÞÈ¦ÂÖp\x0013/ÌÇ\x0000¾ø\x0019·ü>¾ñSåÌÀÐÂ\x0008¼ñ"Rè.[fÓðü,/ó\x0013Ü±¿<+Áæ\x00047ý ÕÏ#ß.æ>»åC/öKÖ4'öRî	°¼´ì\x0002:\x0006\x0012\x0011éCÎW¼õTy\x0011EÓ~öóH"c$1ëoA
¸µß\x0015éà!ä>6Z4ø\x0001]ÃWhó'\x0015nó\x0006ÃsT¡\x001c©QßÇÔÃç²dÁ\x0001\x001cî\ò¯Õ\x0012\x001dA\x000eqA§´ ¹ê:·Hðk±f!J\x0000ì\x0008ââ \x0017Û?}¥£sQ°YäI¶KÃñ\x0001ogÃqo_\x0006Y\x000f=¼$æEjÂ6úic\x0016Fú±
ÂG~RtÔ\x000bdÒ¥pI\\x0000|\x0002øO]»Zd¶\x0017xf®kÎ÷ÈU3qïð¸Í«Á[,ü4x¶½Av\x000cø3]íºê!ßÛ~ËR*¥£®ù.»ôÑLxè£iV	ê Ù.J9V§à/ègouÿÓD\x0008
¼àrÓ\x0006^¸QÊÔK`É$\x0003º\x0003t¬@hÆ\x0002XW7ß[Õ\x001bÄ­éè\x001e_&$Ø§ èA\x001d~´AØ­\x0002àA§*¶®6øÈ©^µ2ÉÔ<\x0006Hñz@\x0007j&}6"Ë|;r\x000f	¼ùzù¬ç\x001a\x0005d\x00182Ä\x0004
\x001bÖ®FÍ¿[s9û¹BÁûQ/÷nÕ-\x0019Wat?W(HFI\x001aÜê(\x000bÃÈ-à\x0006ð`ÆF¶qæX÷?Møîi\x0017\x001bz[ST7?ÖtØÓTÿÓ\x0018>ÌWBwJä\x0007a=ÍIõ?Mt\x0007³<]aùnÔª¦°CnN³RýO\x0013Þ@º\x001bÌõÌ¶æblNóRýOXùÁWª\x0006f¿N\x0019öL¹\Í¹¾BjJ\x001e)Èf\x0004YÙAv827¸¹öf§ú&¼©]ÃË	\x0012\x0013ã´¸b²ÓôTÿÓ\x0004·h
æ\x0005O!)#o/2y®°Xµ 2My\x0013=Þ\x0019ò[{¹ösm\x000cU\x0011èÂzÓ!É3\x0017\x0019¡dÃ8×VÈQõñwby]`òL\x0000sá	±§Yªþ§n1c"~SäZ¤gÏ\x0017Kv§êñM]½§Ó\êlè\x0017FÞÓDUÿÓD\x001eÆîQ*¹¢¼¦Sv©êè\x000e\x0003¿Ð\x000c\x000fiºt±Â§¹ªþ'\x000cýÐå3\x0007KËºl{¬ê:Ðe\x0016\x0004´'×%²Ôwã.ðçê
ùªÚ¢\x001cÈÊ\x0006\x0019W çÕFåQÉ\x0013{³êð|
\\x001bhq1kìÅ_=ÍZõ?MtÉ¶ Þ1\x001b^4ib\x001eì4mÕÿ6¾\x0016\x0012yº¨næ*ò§y«þ§ù>Ù%ÎáH¡è8gèëiæªÿiÂûn\x001bÁØ8ö<T^ÍiêªÿiºM@2Ñ
%ÈËìÙÖPf¯úÐåClÿ\x0018Y¬¢\.g?W×\x0012È]E*jK®Ðoð\x0003eÔ¦°úÈ×¶ôþÑV\x0000á±PùØë+$±jó4\x000cÆP\x001c&DK	\x00179WÖÂ\x001d!èuxNa¢\x000e.÷r®«\x0005tUz8>s|í^»{Ã-\x0000¾ÒW-èîÅå«*i¬³õ\[«!¤ÐÕsñJG!rxÃ8×Ö
Úza¸À;±>©«¿øñËB^@Gmu±\x0014\x001c:SvÊY½<!\x000bõ\x001cÀ£ºÒûW2­\x0002ºùË\x000bRÏÕµºæÂùÃÈWrù.ëäÎ\x0015ÖÖ Á{x|t3)(ï\x0012\x0019/äj\x0000?·Z¼\x00056!úÂ6¾\x0018ÞÕe]±ëðß\x000f7æÏ°Ñéÿ¾¹{÷ñýûwÔa\x0015\x0017I°&\x0013¡
GäHlÏg²m\x0019Ïë\x0017¥x¹¼¯ÈG+¼\Ô¨Ôl\x00085¦ºÚMæÂê0ÁÕ¡×ÈÍ'dnD\x001033sy?(#´à\x00038Ì\x0004Ç\x0000,½Ý6[ÂV<\x001aÝ-iD­a^(ÖfëÔ,
]JäÉ\x00127Èn¤Ä\x0004I	×\x001e8\x001aé±\x0011{u8Ä\x001d½2ëgänq0]¶mN"ÊÔùéÊyAì¼¬\x000eÕv~ÂÏ(ªÁWhÜ5j\x0010Yd®eQØ?þñå÷
ûÈ×ê¼r)]nFÏ8ì]»<IOä:Q;®JOÔ6¯>Óo ÷¤ª5xnDkëR·	KÝÂhï¾\x0016G\x000cËÉfF*Ä\x0015ZWº\x0001ö\éæ}¾³B	XéäÌ%\x0011Oq[:Ð±\x001e%[k°
¥=\x0005C©Êrá«ñkSäËì·áý\x0017´Çäë»oo\x001ekIª.³~çpmt\x0012æÏêì¸ûU\x001a#xÆHý\x0015ú]õ÷dÈFÙì|¤Êz3øêççÁ+³$*&xV|lp?BºK\x0014-\x0005BßK´ä\x0011\x0000[±á\x0014oJ;°2!\¦zÎà-RùT\x001f ªja}fvÊ\x000b¡dFãÒ¬®=©	\x000c\x0016¤LtzØìÙà"$\x0019K\x001f6£Wx\x001cµì½ä³§.Ùf%¬&æÝíÑXtëÏJw\x001f`GÐ¿||ùýí£éUbZîèz=¥÷\x001d\x0008BóðC>aË%_?.»H]ª\x00157ÞISi$\x0016+Oayt)ø
Wxò\x001b²)È\x001cVe^Ì\x0014X>å\x0005[¾ðûïÊ?ùw{÷H£íi ÎÊæñ\x001eíä²\x0013\x0003\x001aùåø_aÐA¨-6út\x0019ÄMCí\x001d
È""ä9Ð_&Ã	+õúér\x0001ð\x0019ÅIÇ
,-ÎjúÂ\x0017ÅCäv$¤\x0008\x00037y\x0019lá\x0017ðfi¸(Ð\\x0017\x0006OÐ~I\x0000øLH-p
ea¶BöíÌyt¦·j,9	>s\x0016Á9\x0007ëÀÛÿ±DKÚòQ\x001bÕü%§\x0000às\x0004ÕK\x001d\x0016\x0018¢j%¶Öe{ßÛ4ÂRm8Ð\x0003T\x001bq\x0003HU$\x000e¥táäh´Î\x000f¾Sa,³¼Ö^6\#ÒÉC!)-}bÌ"xaB+K
Ð'ç@\x0015<L!\x000fj"+
c'èRA\x0002èä².\x0010¥ªOÏQÎN)Q\x0017Å¥1Ág\x0019#\x0014\x001a\x001d£\x000e¸CØÌ8R\x001e).³P|^á-P|Ê\x001cf>bj:,µÂzd.\x0013ÑKÔ9ágÔ\x0019bDyì¥k´ï¥¹V
íB²±\x0014«'<\x0014«}Ó%Øà¥vûçA5çF!Ã,\x001fÀOmª>\x0003\x0015@±ÔR)ßYÇãáâ<i·\x0012Ðçpn\x0015Ò \x0008÷[dÖÍ3d·Ò%wÏ¯\x001eê$'ïÓ}O[G?}9,¶ö	\x001bÓèÂÊ\x0011¹ìïðõÌ\x0002÷?}ªXÚGü·°ó«/'\x0001Ô¢Ö¡Ð½[_Çµ\x0019úÀv\x000e5ª 5(ÅaÕTÎì&Þj[N\x0001>ÃÛ\x0004\x001eBÿK;\x0004
0¹IÚlx\x001bÜíûWä0½¹}\x001c85ëÂ«Á\x001aN:åöYg9@\x0002%±C¬¿î¸%\x000e43-.Úc¤9·bú 6\x0008=S	V/\x0007´ö\x0012ZÝN±Th*àVWØþÇ«úGH$Ü<û·×G)ÖÂfµÉ\x001dûM\x000b5g§C\x000bÊó_Y&fO~v.}\\x0014Ï¥'[\x000c-2k±9µUÅýr¡KX²\x0008\x0013<Cãr©Ý6êÿÍ\àÂ\x000c½\x001b\x0014\x0001p(ã\x0005Ì0FßÀ©û¿ÅÎÌ¥çÜ0:ËSrE·\x001c½}Z,8ö¬ò¼\x0005ç?Bûö¥_ç\x0010\x000epg±tjÁ<¬:	)1-ACgÒ_¨\x0000&ø¤\x0002èâÄ\x0006'\x00118Ó:rn!ê\x0007t(±9A,d¤îÓ¹Æ&Î\x0018Úý@÷\x001eÎ.»gqMbàk.¼\x000f[Æ½\x0017 ÄÓ\x001cüæOM)n}}ûòû×ooÿý¬BT½cN*\x0001÷\x000b\x001edW\Ïë>ýä>±ÿs\x001bå²ºMÆQ#O\x000b¼*ñJ.Æ#%Ù¹¦ÎaÎHòC\x001eêTmm¡÷±h¹<qÊZýJ\x0019\x000cpd.w}ÒNß\x0013F¸å-\x0008ý³qt`n6\x000bf·\x0019ù\x0000ñ¢öÓ' Ðu©\x0003«­õÁuË¨­Ë³EÔ/µÔ}Þ¾\x001e\x0015mü ÑØ\x000c\x0013.­Vøõè2\x001c-èi_¯×Ó´1?aæ¯9xsÑR(^±¨aövæ>¸­
ù\x000c\x0003É\x0003­E»
óå>0¶,-d=W\\x0013ò	I	7¼jMMâ\x0006?ÆÃMH\x00074Îáââß\x0006]Õ\x0007´Üâû¤ù²\x0006é@Æñø=\x0006ÅéPÇGîgMÈ\x00070\x000eàDÛà9\x001f^çÇ*îe¹ÒÓ·\x0016»â\x000c%ÃR´\x001b|NýÏTÐ¢
2´³X¿í<zP®Cé ¼ïò	\x000bÚáÆO95wÑø¼Ýªt \x000e\x0006¶\x001bÂÖMvÃð\x0002AÆvå3%´8\x0015°¯¶È:d¾j« û\x0002¸ ò\x0006-ô\x0011Û^sP
ö¡ÐâmÏ¡-û®È\x000e'â#ð7ç¼à\x0006a¹\x000feíbÙ®>> ¡\x0013ê²äÚ2#ÚBò¹}ÎZ·]||@ã4¼G{«çH	¡øÔÝú/\x001eÚ\x0001
þ¬9Åö°ð$¯¨\x0006ãÒOË,ß\x000cª(5Àé\x0016dÙ½MòÁA~ða¸Ägª\x0008\x001be¢\x0011r¢© öÍ¸okÌ/´Õ\x00072h¢l4CgÕ÷Ô\x0002ÄþËfÝñ\x0001\x000c\x001d¶Ðü\x001bï|² ïÜé/µO\x0007t¡Ñã$ûTã=2íBOh/qÍ\x0001
½¶¢k'Þ;¥°¢js½ö±¬|º"{|\x0010q;Kó½\x000eG
HÍaîÏÖ\x0012\x0016\x001cÐ®\x001aØhõ\x0011 ò2Üö2u·ñL\x0011=:¤[_ý>7ÿ/}O\x0007²''Ñ\x0017ÂæÁWßÂËÞ9r¦\x001e]ÒÜ+\x0010×#Ë#Bæòa°c³Ö\x0016zÐBS ÛEú	¨:rÆ×Ôx\x000bÜYìè\x0003&þÉ«\x000fØýó³\x000f\x0018p\#â¨/Ié\x0013o-m\x0017ÝÉ$¾·\x0003\x001aÚ=\x001d5Úú\x0018XWd¾ï£ïcY¯Ð¥~â}ØüâõûS\x0017á\x001bùã'þ\x0003õ Ò?Ðä\x0015#¹T#.\x0017=©Ö°î,x{þ/xûÉ?aÍ\x0004\x0014 \x0004ü·Ï¾½}ö»w7³\x0014X~'bÌ2\¯¶7æù¯Ð\x0000\x0017¥9þ¤\x0001Ñiè&+U\x0019»óWjW
2?³Í\x0002\Ñû	HØ^3f\x001b1üR¤±\x000cxµ¹\x0017`\x000cC,n5¥°5oGæ¯e»3¸Æ\x000b2Æ
\x0006#K7µadÞ
Þ«V«a¼àfÂµ´½v]\x0008W]EÙGÔ\x0017`ô!"6\x001bK¯XU~\x000f½\x0012i4p­¶ë\É£\x0019:k<îÀ\x0013\x0007¼«û¸w\x0000cÜ\x001b\x0012n]µ6ã
6AVr\x0011ÂI|z\x0006Áà5·V¢u:t|ê8
ÊgQäVËï³\x000fûÈf\x0000cdãp¼&Z5m\x0010Ôc\x001eój\x0010áìÙvÏÄyEù¡oî7KóàµØ8ò\x0017èHÚ·\x0011AK§\x000e|ÑµÏÈo\x001cî\x000b4¨3¸«Kg"Ýt,,ÑµG¾\x001b¯ø\x0002
"Ýâó\x0018àªÕâËl\x0013Üu8ñ]\x00074ø®² \x000795@s\x0010Íh_&R.Ø\x0001æQ$\x0017\x0000Õ'ëx(>ðJëvõ¶).]\x0017è\x0018(7\x0002F)ñ\x0018ébìF{×\x001b¸\x0016¦|©xdßô2a\x0011º2±¤$¿FëÅ²å
^ñ3V \x000cRÙ"æ½&!ê3\x001d	þæTg¾¹\x0001ù°ÚÒrS H6gÏR\x0019;¾·\x000eÏÕö±K\x0015\x0012v½Éæ§úÒÄb÷$I<=}¤Ó³\x001c¦1\x0019\x0001Çç¢PºÌñÇ{\x001fGñU·
21!+Aº&\x0017mPWréæ\x001fïnÞþõÿ}÷úý³ßÞ¼úx{÷H}ÐO}³:K»íaÃ\x00074¾ÖÏ¤Õq±<íÞûVcÂ²;\x0008Ì\x00123.ìúHò¢ÄWd$ IÈ\x0006nÅ>ð\x0010\x001fçò%\x0004=CF.\x000b\x0007e\x001cé1Tl\x0013:=Ú{!g1hWd$(¸uÝÖÊ\x0013¥=ÃìzëÎò,]!´Í	»Ú\x001aÔÌ}àdM¶ë\x000c\x0019(Çuëí¿ÇÏtöÜ\x001cJÿ¡¼"ãj¤Ë(cº\x001cÊÏoÃ^¶L@ÏºH;!O+\x0004¶\x00029q®¦ÉßúWhdU2Qé\x000e\x0011s'pg¼<¥në\x001f^¡¡OÁ\x0014l½²Ù+èR\x0008:ÕAÎ&x\x00168Êl@5´6[¨Æ'å\x0011
´3Ñµd\Ám" Ì\x0008J\x0002g\x0002b±ù¡`k\x0015;»¤¾bOæ­Yõ\x000b4v'\x0004ÚT%;)\x0008Ùg¾ÜÙTW·ö\x000c\x001f1²¾\x0004Ex\x00033W¥lG²÷äB\Æ\x000b	ô\x001a87å\x000e´æ\x000btqË ý\x0015\x001aÇèS\x0005z&ÖÃ\x0014Ó2ØWÿx\x0001àÕfNËÎo\x0000·¢6ðAÏÐmè}o3II"áãN\x001aÜí`·¿àÉ\x001dAÙn·Â$/ûoò`dÊ/Î\x000fþz{0Ü=µ%9&5J\x0017b 3th<:C}\x00184¡÷\x0010¹o \x001b§ã uzSº¡¦3ôÕ÷·?¼~ûìÛÏ¾z÷ñîæ±F8cÑ-}øêÒ\x001bÖ~\x0005ì[y_¡»­¤ÝîÕÔøÄ\x001eP²&á¶ÃÎUot\x0013²\x000cù­r\x0001\x0006KSqË}{®îfUú\x0019TÖë[qÁ·¢\x0016\x001dÛÆÊ®D\x001a\x001cóëKq\x0001ý-\x0006É\x001bpUû[Æ\x0013\x001få\x0002\x000c>J¦q/\x001f÷ÃKâÛ§ì´\x001aÜ\x000bp\x0013Wz6é¾uê±\x001fo«2 ÑE)\x001e³Þ+J³?Q\x0016í]\x000b4¶¯QÎÆ» \6ÅÍQ|Ø÷n\¡Ý'ÞôÆC¹ Ôe¤Å¾©BænÄr¡9;?Q\x0003Ý2Ýrv	 ¥¾É\x001b¤\x0017§0\x000bk.½X\x0018WÚÛ½{-¦\x0008õîq¸Ê5=\x000e\x000f»m&á\x0010A~}Úk	¢b{\x000b;Å­T\x001ffÐ]ß×\x001f¤nòúígÿòîå÷ôô\x0018ÇY×\x001eÜç?Ä2Ì!ËóùkÌ\x0019à6ÓÙkÚ/ë\x0016Ê(®9ô\x0008Ý,ÊôÌãO·\x00177÷\x000cy\x0006ßÍxCÿmHÎq]Ì(\x0012ké]ÞVO²î¡\x0014.Ö9 "ëm9wk
³5')m»(³î¢\x000c¹`VÆr(¼6B\x001eüek2ë6ÊpYÝqEöJIÆ³¤7U.Û.Ê¬»(}2HÍ%\x001b¬àýX©\x001fBîÅð5u\x0017eßù\x000e´\x000f2à]\x0008oyÚ¶5¬»(¥b?NIÿb¨ÙÏÌÈ)t\x000efÝ9\x0018MA>\*§±* øKmæì¦¡W.Ì­Ë\x000b©,sZÒûA·xvÏÐ)×>6vÑd¡ÂÖv\x001dÜcåÏÚÙ²ngóâÿA\x001f¥+â\x0008´]ÑE»ñ®­U¬ûÙÄeþ¾*äý4I¥\x0019Ócß©³égËºÍË~S c7´B¸A+Ê¶vì};[Öíl"xÐ)QJ¦ÇvÓÜÕíMÞª²îf\x000bÒ\x0007­èBöG"­ÈmÃ(nÚÙ²ng\x000bÒï9?b®c÷&\x001eïùË}Y%¨µS`WQ®öÝ5h~à}ìÑë¦-ë~¶v\x000c¤Õ&MÇR­\x00141*ØÂ@-$ô×fãu\x0017ogOÛt´eÝÑ&cÎØFo\x000co^It>µ?©ÝeÝÑ&4¡ÀÐç$ñõñcYÙ¦¥-ë6!Â, |ÖrÔ$m\x0004=6ÿlÊY·´	) vbÀ!¤QLuí3î;Ú²îhk\x0016\x0004
Hªð/4ÃÜãMG[Ö\x001dm¡1</9pg©É<nåÍ¸3Uô8X 8\x0015rói*GaoÉ
zMO[Ö=mÍ³@Ó¤ß\x001aÙõ°Ýú3Uôn\x001a(õ²KE\x0012¢k>u§ÞôËeÝ/'½Æà#¤\èª­âr!\x000eÞ©3ä\x0002¶ØÞ7¹òÑ*ö\x0011\x000e¦¾Ë©l·\x0008\x0004íù:|gõ	g\x0018¦"ÆHþcºôôNèÈO¹sfËw@£\x0002\x000e\x000e%Iì\x0016æÌ¿\x001d¼õÖÄ¬[\x0013cÉ8_Ð\x0019ú\x0010¹ðLsâL\x0013\x0003xê:ÓS\x00162§§¨ì¨Vlz\x001e³îyÁBÜ\x0015ÅÏ!ölñ´".\x000bI\x000edÔDo¢ì§vK­\x000bÇ®À"8¨'\x000e-*ÒrViá¸3]	ðjU÷_û°uÖßùîO3e	èAf\x001cÅ8ü^\x001e=iÚÔçÊÎt\x00056ôÀ\x0005Yåè=ì¾\x0018ÝG{\x0007èÉG¤2ÁZ¨ñ÷\x0011üÿ3÷n;%Gvà¯$ø>	¿_\x001eÕìnJ
R¨f\x000fúµ\x0011¬f\x0005&IEe\x0012j\x0001\x0004ô\x001bú\x0001¿¢/\x00197÷½Ï^Ë¶í`*òLe\x0002\x0003
¤`YúñínnekQÌTÔ4NrK ü"Ç8ö$Â16Î¢¬[tfÃ}cæ\x001fÐ6®r\x001açÝ/Ê±`Ì(mÆ\x0013\x0019¯0½6<\x001fç]I\x0005©~\x0015\x0014/ÛgÞ\x0015\x0014Jâeó9Yýà.\x0012¤@	Rï\x0000\x0003\x0013Ð\x0017áMDÜ«3s\x0000ñ6ÙsgèÞDºÃ\x0019Äh\x00139z-oË¶à&ûÊ	n\x0005Ñ\x0008#4ÂpH1CçjÅHï,|p?ÃMþõéû\x001fß|÷ôîÇ{\x0011D`G©D7¹àëHÑ\x00029QFÜÝ¿F±käRUìê'¤ÉæË÷ziRÑý¢'zfãgÐOH\x0013WÀ(ÈëDÓnûqd³Yìê'¤É8>\x001ej¼I©¯Â5ØâíáÍ2
¸\x0004®]tM\x0015p½ð^-É\x0006!÷\x0013e\x001b|Ù-gÏ¸iö½µLz³WßìB\x0007z$Ù\x0019P7Y\x0005²9sC¤Vo×ºú	\x001cã	w\x001b²V\x000b,\x000c÷\x001bm|sWà,Õ\x000b<sÅ³ÒSV\x0008µf³ó´[\x0006pëôýDx¶YµCêBæ®°1¹G\x001føDe\x0007l2\x0003ëN÷eÚÓv\x0000v:,7:+\x0014ÁÕÌðf\x0019Àú=\x0003Ü[dÆy\x0013ÇÇu¡\x001e¯n b²[\x0001L)U¤ñÐn´8\x0011êÆ¼FÍÁíNÙ
ûf­Ô}7®® ¢½_¹è«[3Ã¢T8Z+1r¤¹b·ávÓ(×\x000bK\x001e·¿ \x001aÌ\x0013 ÍÍáÍ.\x000c\x0019ÈÆBçÐixÅÐ6¾­«[èY¨7é\x0012OòßÜ+ÏÜ(±.Ó\x0008¬oØ3ÈÂ@N\x001cuo\x0005UW×0 ¸=Q¿Å1ðñPm¶\x001aëf%z\x0001À;vGd\x0003ãÈEyÕ®±v`'î\x000c\x0006\x0007´6KðFu³Ìºö°Ñ)¨aSuð\x0016\x0001¡Q`Ý\x000c#<= \x001e\x0019.7Rg&¾\x000eQ\x0005ÝLÃ]8ÞDÌ]ÍF(j	î0 e$¹ÈÜêv\x0011rÿÞq[¶ø"èf\x001anKÀÑì,ê{D\x0019\x0014=YWÜ¨.Ë4ÖûªE\x001b5ÐÍ4\\x0016aE8ÎÝðxì¥GD,ÃÃw»\x0008ºÆ	³û\x0011e Ck±cj\x0017EÐÍòqYjï´ÓãîÐÁ\x000b4ß"èmo\x0017A7Ë8Íq\x0014ld jt¦ñ\x0013>b«b\x0017A7Ó\x0019\x0016í\x0010¨[ag<\x0001¶7Bl£\x0006ºYÆñz(\x0014ôT\x0004ã]ze\x001d£\x0004ºY>îa­x\x000f¥.çÑIG\x001eå!f@7Ëp\x000f\x0005Ëy¸¥"¿Z©r«/WjÔ@7Ó\x001d\x0016í\x0011XX\x0012È b\x0019ðHv\x0001tÙM8\x000b¶©û\x001a2S)EÏÓ\x001aõÏÍòq	kó\x0008T,EÉ&&hóq\x0006\x001dFùs³\x001cè¦À^d¦|U50¬zðÕyé¤*sÇy.]	DÆÌ
2ºØeÊÍtU{¤AÎ#î´jÏü\x00043êe8ÐF=kPªÈCf\x0002ÖMv¡r3ÝàØUd\x0014Ï]¥,±Ó5\x0014Ôb\x0017*7Óp¢E×\x000eØfsd
±\x0018©d\x0004óP\x001bÊe\x001a*µb11\x0017_Yñ(6>\x001fóé¤À|³\x000c: ÍØt%hÊf9Ì ýÄx³\x000cz\x0007 4,ÃP5\\x0005Ä5Îw^¾Å£
_n®³[\x001aq*3ï®ðÕË\x0002Ëu¼\x0010Kñ³/­êÉ\x0008v\¾>n¢H®ÃNKéJ?¡Ñ\x000câ\x0008¶çêIoùf\x001anb¦XjfzÇáèÑò)K¶|\x0012[¾®°ê\Xéh&#0Ls$\x0004³~\x0012Z¾«8"1 /ÅÑª"ñ-³ësb¾>®b©\x0015\x0017÷ºð«+x\x0012XÞM¼ò$J>Ä*+\4·çóÖo<\x0011Jß,\x001f\x0017¦liì¾hAVâ©\x000eü:A\x0016'2éå\x0008Û\x0008­I\x0017AÄ¥!Êº¤\x0012xÙo¦\x0013,Úá$°WQÙ14EÝædíIòøf\x001a.LAnÅ)ØÚyÕmÐ5È5?IÜL\x00178ÕTÆkD\x0019¸/¹ú¬\x000e^Ý\x0016Ð9.0ë×%þÇó\x001c\x0012wJck²	^\x001d:	.5â,pÓw¡pT\x001aç÷;±öß,\x001fþÄ]øýú\x0006×:,+ÿâØ\x0004o¦á<FÜr\x001dN_ÂYÃ;ÑåÞLÃ\x0015f¤¡®¯´\x001fiå\x0016'Jýi8Ð9a'\x0002<ì:ø¦Ô;ùÜ\x000cÃq«x²¯yÄ©Ô\x000fLU5òé9Ï}\x0012\x0004¾ã*f"*Méa>ðÉj\x0017'1àih\x0019\x0013f¨ñ/qÿ\¦\x001b\x001dÄøfºÑÑä¢Ì\U!$>zn:¼ó\x000cÚn\x001aü?u¼dÌVáMZgÓÃK1ýê*\x0002ðxJ\x0001Ð(½?uË\x001dMmf¡ã\x0011ÓWw\x0011Ô;¤\SÕcß\x001cm´~Ý«\x0008L\x0002Å÷8|BÒ\x0015~=­X8áå«{\x0008¿Å\x0005°,£3{Å6/ú<bùê\x001aÀØ\x000b'ª<ãùÆ!üÙ¹\x0006¨Ì\x001e"(~d\x0017T=öÄc6²±Ùõ?Ï'î\x0001¸Ñ\x0011¸1¿a Ã\x00048O8-_Ý\x0015É\x0012<âNsÔá3§ZÂðýgCqf·\x000c\x001a¹#z>ÌFÅÛè\x0012Éêà${³\x000bh¡ñd\x001dßo|.æ¸ó\x0010´9¯Çð$cs³\x000c`¡\x0011Ü9ø~òßéÄqA^¬\x001b'YÜi@\x000b@é(\x001eÿÏ©ý N§´''·îÕ¡\x0003ÍZñ£\x001dü¨ó4Tï9@\x001fþkÎÉ\¹\x000egn¤à¼f\x001aö6F²0õ®|Gß¿(þö5ÇÆÔëÃ÷«+iv´N\x0012\x001e7ÓpeB\x001fGg]i\x001f8Ïj¾òý@mR\x001cRf(CÂtW
«\x0010íMÉ»â\x001dë°RBÈê1äi¤ñäob;\x0017÷Åã\x0018Ì	À²cf:÷q"èÂÔ¸Iá\Ü\x001809NýÜÛ#î¹ÏîUèQ²ßdv®lÃù+	-eê:0X#¦²©»Sâ\x001d¢´¡uå©\x0003;Ò\x0017)õUÙCYüÓ¡&%\x0008\x0014Az¥®S}^âÝWÛ
}`©\x001a\x001cÕ«¾U üÞú5MqÕùô¾: Ë#\x000cN<¸ï\x0003ÀZWòªEé¡EY¤'y3-3!³ö{\x000c-,Eð«&&Tu4XE»³æÈYbÚÀ\x0017÷=¼ÄÕÇ é8$UÇ|¸ûv¸/Êc\x001eËcÍ'\x0018\x000f\x0014¬1Ó$©÷QÔ5×á¶÷Ûã.ÚÐ¦l.£ÒäûÄï À\x0015Z[À¯=º&àÈ.\x0001rGøW(k\x000cJÔÏëÓÂ\x0019¸¶Ç\x0000\+\x001b	ø\x001eìø®µ#´\x001cVcñzù¡*$\x000f]4i9ë\x0015à4ü\x000bid\x0010³,nRsîåZþ\x0017\x001cmLDÐxi
JÉoâôû\x000b_ ó\x0017¦\x0017>sî\x0005Ï(\x0015Ù~a"/ÿu\x0010\x0017þ\x0001Çÿ@\x000f\x0001ëh¢ñLRV\x001a#uE\x0000ù/ù\x000bHÑü1&¯.W¶£\x0012ºÏÆ¨¿ð/tþ\x0017rùØ\x0012º"°\x0018g#¾\x0014:L2²\x001dÅp¯ãÇÇçËZ÷¿É\x001f\x000fO¢òÂ*I-ÚÐ©§£N¿ºë :þ\x0007ªÇ@Â^.²ëNÆì\x0002¼ð\x0003faùZoÊo\x000but*+,wiÖò^ø	B\x001d/xQU%¡èOÙÈ~Á\x001dEåÃCM»­Æ\x0000È\x0001¯ú¬«kòÂígÞ¥ñ.&n>3\x0003¢çbêj>7÷ñ²lño\x001f©fv$
¹KaKf\\x0012	³nÜ\x000bÎÔñþø
S¤##W\x0008FM
9\x0002£\x0019Ó¿ð\x0005º\x00022¿²\x0018õÂ9­|N'î3qG<>ÃTÊÃ\x001dÅ\x0015§\<ã/ødÆp|f¤Â\x0005m§ÃÙù	Ê\x000bîº¨ó\x0013±âW\x001c
ÇGõ6Û\x0002ÏËaüMý\x000bØ>-¢NÁ÷¸®n\x0019\x0011÷\x0014;á\x0014U§b\x0016d°__k¬ 7¾À$¹ö\x0014ãÑ'O1"[\x0007~î8(;\x001cÖì\x000es2£¿p{>Óÿãd?\x0017~Aá_0®\x0016úªÜWZqy2\x000bç\x0017~AVÈ\x0017jë\x0008ï	õæx4Rf±ÓJ\x0006..'ÍêGEÎ-WEÔç^¸
I\x001dÔ×mÑ\x000bÂ;ÜµæN¬[¯þÝ\x0017úêæ.\x0003w^È{IpT\x0013mª]g\x001f"¿\x00105æ¨\x001eûDÄ#3p
sÂÄÑ#ç\x0017\x0002¢¬\x0002"*§#ÈvÔJiêtÎjh{!lo*lo
Bº±a#M \x001bU%7nãÌ/<õ*h\x0014b\x001bü\x0014yD3[cP×öý\x001fOcä\x0007$\x0001vqÀOïÞüëÃÓ»w\x000fï?
¿ÚÇOÏOóÓÜcøGU¢F×nD7#ìÄøË§9õ³Ïþø\x001e?oöG\x0004L`\x001eðUÚ\x001cÝêÀÐ4aZÿ³9¡£Éü³0\x0016ÃS¯²w<­aÊ\x0019\x001bMæ_³þfxø@~*½\x0002hôÍAe\x0018g\\x001dâ°bRbC^i©JnùgsÜEÓùe8ùÒÓ 0wÀ>Û\x0002y]Óùó\x0000t\x0016NGBÃ{Eè\x0017ÿêhÀLÊX\x0002Ö!S4rZånóµî¦ál\x0014ã..{Æ{EÀ"hª?Û\x0013\x001eÏ?³pÂT\x0014çUS\x0017>Ihõg{\x000ccÖCJ\x0010éç\x0011=0\x000c×+ÍÀ²\x0000ñÖ¸Ä2
_1¡tð5\x001c©§º,ýj\Bë\x0010dáõy(§d\x0019<µá9ùjZbYÆ\x0003B×%È\x0018\x001an3Aµ/\x0017Ü.e\x0018c\x0019edKE\x0006ÖÌÜ.ÕÏ+nAíµVÀ$P¡¨¦G<S\x0011´8g}\x0005\x0000|þ\x0000\x0000É¾!¬5¶ÊI±>´6£»bÁ\x0012Ät©è?:vQ54\x00149Cs3-\x0016.aÙîd\x001b"£6R2­e-Û\x0002\x000fLÓ\x0000\x001eHã
\x0000\x0017Çû\x000f!Ì3ÆkÕ\x000e!Á´U×j½©Ò\x000e\x001d5æI\x0019Oä&XÐ\x0015±Ý\x0000º\x0012\x001fEp!éQ*\x0007\x0013ãÕ¬Îö4
még\x0000á\x0000.©«Òí´õaºÕ	\x0014Û\x001d;\x001eçØ\x0005\x0006Ä:§\x0018ü[]\x001cvhI\x001cßhÇ	X6ÕAò"\x00077ô\x0019öh\x00012,Ã¥é DMT\x0003=	\x0018c\x001dC#yÙÎ!$/ãù\x0002 Ó8ªN6NÎ(ùÅyX¼\x0004!0G!ÜKd]
ð¬6Õ8s\x0017ÖÇ_ÐúØ\x000c\x001câ\x0019îq\x000bì
ktÇ·\x0007¿ëðäøÔ÷¦jXcµ²¸N^88N\x001dbAt\x0002øëVò8y\x0016§¥R\x0003oþùÓÓÇ=ÝKW"\x0015lËS\x000cm/¸R$ç¶I¶U¹ÏâôgP[eÁ\x001cb	\x0008+(u\x0018æB_
?Wah+AO#\x0000a>"t(6[ón\x0017Å
vÜÐ±®\x0014h\x0008#ûM^Ëe\x0019G¶\x0012¾ª®(îá\x0005"[nÑLQêIolX¸fGfy@IðfRu2ÅªÈ,G\x0018°e[Ç¬tÌ\x0004Ç§:)\x0015,\x0015ê·¹\x0011\x0006\x0007ÏIÇ,:ì';Í¦¨4;\x000c_ÈÕÙHGÐee¯äj\x001a.\x001e=\x0003±,ã¿¯oñËjÅJ§*7;ª'}4é\x001cÃ\x001e'UiOþ\'E½³LÃÕ¶7\x001cääÔ`áð0/°Å¼s^\x0013h)?ù¬\x0017Wùia&;U«'é5éÎcêªÀÇÃEði®áBÀ{3c`\x0003\x0015§Æ#Óä\x0005V\x00056)wz¯3óîäÅýd]6Ó0|Ò=mHòJ¸+d|FTgµeL{ä3Ò\x000b¼*\x0013¬\x00113ó¯Ö\x000b/\x0010`	Ý9s68öÒex[C1a¾'Û\x000bÿÝó?<¾øaª~¾ûßÿóíïé}^ùþë¤f¿¦\x0004\x000f%¦$ iÎüüâQ\x0013ñ·¥\x0013\àG¾\x0008ØÁ6j\x001c?Ý+üeruºÝ3ýfø ±2Õ\x0005e.£eæ^p\x001cç¬É°\x0019>4\x0019Æ°yD\x0013y\x0018æ!4\x0002¯j½ò»åtX\x001eiùQ\x0000I)2Lðt2ÇÝ0\x000b»åy_Òðc$T¤\x0000|Ðx\x0014Y\x0016õ,*³Y¾ù¯bãðp¥\x0011ØkN7«\x0014gÚýÍðA»\x001fÆI\x0000"háçÅ¢6\x0005\x0019v¶bénù\x0008RÍ;Ó:uÚGBF±¯0í¬%±Y>´$\x0002é$¦(ã èq{W\x0017¹Uû­ßLD\x0015O\x0010~\x0010ä·3/vìµÛåÓÝôq\x0005m\x0017ò¢÷1_ûÝòq\x0007}ÇIÓ\x0014G.ë1Ûì­Å¾
àÖfú¸"oåÁ´sÜÄê¬{\x0013»_2W×ð õ)¢¬
ô³ÂøD\x000fÄ¸Nx
ã""ºº á\x0003)µÔ8`F\x0012\x0019.3x=?È»iG\x0019p\x0003Ó\x0002È%Ó**±-ßó8ùf\x001aÆÉ{\x000c{$'ÜR`yü¿a\x0014\x0011ëéõgNeÚ'8y\x000e\x0011ÊÂÌqÕÈ¿YS=/Ðì\x0015`·
g¯uhä\x0003·\x0008;c}ÇÙ[æ\x0016`·
\x001fLè^ÐØfçJdìai\x0013y\x0001vÛ\x0005\x000e6ÑLOML\x0007Û±wòÑR·»räÞüê¯yÿ×¿<?¼(åW\x000fãå¿¼%Cè/\x0012\x001cnÇG¦ß÷öçPôøtr>HÉ«@ÂU,§#÷ijã\ÞVwÚ,£\x001câÎ*OiÕÌíÜ\x0010&iÝÙm\x000f\x00176\x000b\x0004ÀÛ<ÕÂ\x0005ÖÇø|ô7Ë á3\x0012(\x000bP\x0018Ó]\x0015yXØ*åW?\x0012aèM®aÊßªR\x0003\x000ek|èìÁ6Ë(_h$ÐCz+\x0007lR3#Í0xÝ}¶$Ð\x0010Òw,¤ë\x0017¤ñ\x001cHlA\x0005ÐÃxEs,êVw¹-üÐ9XQÊc¾¹I²Ç³"¯KºãìÍ7Ó@
Ø
¾Aãx¿-ôRT.ºûV/\x0002Í4ÜÁ±\x0003¨rÓÔ\:dVÐ\x000e$6ÓÀÏ)\x0013`°!%¨UgÆ\x001fûÔ.\x0002Í4\x0010töðÓ¥q\x0002âGækÇ\x0011] ç<Ð
i\x000eU¡ÙÄ\x0015áñ:D³\x0014±\x0005vÎJäøÒæ zA!ðæØÅ8xu\x0001¡\x00121¾\x000eÐ$&áþ¦\x0012Ø\x0008öyÑa5è¯® T"dî\x0019hæsREâ¹åà\x0017æÔÐ&ÝL\x0003?gÄÞÊ¡ðU\x0011}72½¤8¯.!Ô8zÆÒ|&2
ÙLPíÇ¬»ÙûvÓ@d;ò\x0004È!*O¥\x0015à\x0017Eô¹×½ã\x001c
S\x001e1&\x000bÌ:\x001eg\x0018)ÚÜ«£\x0007b#Â©_Ñ)\x0011¾¬hÊG\x0010zèºy\x000f¥é`dR*Ù	¬Ël^ªJç¶WmÿúðénUª\x0012Z©¢á«\x001b eQVæð\x0004Qç²W½\x001c\x0001\x001eO\x0008ôí(ª­ê.èÌ:Ïn\x0019Ð°é"SôT/¬>+ËÅÔ\x0008ß-Cx\x0016\x000bh	-\x0014\x000f×Tæ·/'éÜÍñª#@\x001eìÁ{¢ÞààÕ'÷×¹PíU7g\x0013 2r­)Å ä¥WDy®S{ÕÐ±â;6\x0005'ú¡ØÔÍ^utù
¾ö82Êe¤^¦`èn\x0016EÍQdí:PU¼r´sCÇ«N%i¨\x001f+Ý\x0011õ©%¯¤õ\ûöª¡3Ø=mÒÙV4·c7.z:^õtÖ÷Ã\x000e"gñãóuv>ñ·Ù«L¦ «c³\x001a9ì+>\ ï¼jéÌ£Î]i¼«Ó1¢dÆf»i¸é)\x000eûd@7ä¢Ì³Î´!`9¯Ò+XV\x0008¾¦^¯.¡Ç\x0014©\x0012d°¨ÎÊÓxIð\x001cv³È«fÑ\x0004²ÃX 3	¹QW\x001d`h»éF¦ñ&fÅT3L«¶x°\x0003©Ít\x000b£ \x0002#ú3êÖê\x0005\x000bòf\x0019Nu&Éqñ&÷C}Åºf®¯\x000eHÂ\x0003\x0012\x0003½æzõ
W9ÁØÜ]\x0013G:ÒßÂF¶"R)SÞõ%½5?°û\x0011\x001fxÝ¿p.QµÌÁÔ¯\x001f¾øôÓO\x000f?Ü-¢RXÃâ\x0011QÌ|#\x000cÀÍ\x001d\x001d3>wüÆYË:¢ÊPTQ#)gÜsN!6Ëxô£O4Ée§\x000cÏÚÑ9ÕÞ\x000c³;\x0007\x0014\x000fª!]\x0003÷Êìº2\x000cÎÜW\x0002ÞH<\x000cËBÅÂvÎ´7Ã"5À¬{¯øý\x0005Ì'l\x0016bÎ\x0019Ïf\x0019\¹£HÍk]¾ÒYMªÄI<sN¶7ËàÉGòäñóqQª´ÊáIÓ\x000cçT{3\x000c~ÜÑ`§.Qi:ÌîvÓl3\x000báóóé½­)Kã\¸¤|¡¿¾,c85,ÃØ´|=(Ì%þ¡Øµ®Í4ÔºÆ\x0011\x0003à­Ü\x0011
´KUáCêF:\x0019Á\x0003þó§§áAþððþ7ÿò\x001fïþô(\x001eã^õy%ÅUÄîGÁ Ã/ÉµègwK»ço§Q9Â)°\x0003A¢\x0017Å-R\x0015¨,PV\x0015ö\x001c\x0003Då\x0008å
­a9)iª&4Z³G¢ò³ÞÇ§8\x001eUÏ
\x0000]ZFå	'å\x0004Ü¥XdP dwuÏ1KTp\x0018î\x0018/ûäÙ_Éÿ,Åe~
ï\x0001°á;\x0006[>\x0015v\x0001¡ó>×{°\x0002}á4ðØeÞ\x0001v¥Ïð\x0005wweaûLTòÍ>\x0011}¼Âþ9\x001eJ\x0019\x0010\x000fýòñýÇç»5éjU\x001dñÐÚÍS£ø\x0016Ç©wßN(t\x001e:\x0011\x001e\x0017\2ù\x0002!g.\x0002WOþ/¶:9íÎ3'»ix\x0002¨\x0012%Q%âæ\x001fçÍ±õq¹sp1M{p\x0000 ºJq$¤\x0014EËà-}¯¼\x0000gZ±Ý44\x00035]EL#\x0013Ub\x001fWj¾|WËìEà" (BzKò«²NªÕ.ÚJDk·ÐHØ*
\x00134Gi]YlTgèÍvÁ\x001e\x0012Â\BS¨ïÊ°­ñ%\x0017`äLóº®\x0010r\x0019×çÅ{7
_í\x0007\x001el¡p#\x000c\x0003çûµ+\x000cÃÖ¹8Ø\x001e\x000föØj:"jH[tèøøõ\x0005F9\x0007^ËvÃ:VåÝÛÑ<òTYÏ:D\x0011\x001e%Umÿáñ§7¿}üÃ\x001f\x001f?ÞK.±)A<Ñ¥Û%JÔDïu±9}³\x0003\x0014I\x0017Ý?EåJù\x0001\x0004Âï\x000cÝI9LsdtÑ]XC|x\x0016¢\x0002ù\x0017\x0015s¹`æ»eÀuåzÐ+¤6YSquZ¬_çÈ(é¢»\x001f\x0007\x001c,=\x0004=90[ÈçÐ(é¢»÷	äd»Sâí-(Å×í!¤kî>\x0001q,s0'ÍOZ±{q.ö%]r÷Ã\x0015\x001eñVjU\x001565I)ÞÁ¬º']u÷±!<¤\x000f'C3·\x0008EÅ,º']t÷¾\x001cEÕ$z_\x00140·ÀÊã¥¶\x0011\x0011eÈ\x0012}Dê«$½Y>rjÄ{+\x001añ¤+ã^\x0005\x0012\x001dæF¯°*×¦¾HI¯N3b\x0014\x0003ÚÆa:2I\x00087cÒª¨\x001a%æ¤KÌ²ÏpÓg£ÒV¼¾:\x001a\x0004Q,´dS¦9nÈ\x0014b6êÊmùÃ±ê@3¶\x001b©%,Q-"\x0010(¶aée»Gr\x0015á ]â\x001dZ·j0®Yz3yØ]\x0007ÕkåCÌ3ÎB«W©l\x0007ðú_P½où\x0017`HÝéqÛÆs c7ÛÚøsò¶ïü¼M÷\x0007Á÷ø\x001f²{\x000bJ:º\x0013ù¬üÌMþn¼öwzìCRÿînô(ÂzdäÃ1%©ýì
vÑú·>ë*P\x0000¨]¨Å 8n\x001dF×Írðn\x0019ùï\x0013îLá'¦SâY°( Ï7+ë*H\x0011v²ãä\x0008£+uogõîP\x0016_Üeà¿\x0017Vz§È6(´Q¨­/}ÖE\x00101X±ÚØ)¥\x0008\x00197Á»eÐ ðX\x0001I¥ªÆ}\x0008¬?\x001dÒâæ»²\x000c¢*¢\x0001Ð¹¬HÙ\x0003Ýûx!U9x\x001cTÓ*r\x0000©\x00011®=Ãê<\x0017ç·>«ðX2Nh	\x0011\x000ccBd2üÛ2rV%á±è\x0008ÄQ2òÆÈÊ¸eä]\x0011Þ-Ã\x0005\x0014\x0007\x0002\x0000#\x0019ªèì|Ø÷\D\x0011a¸1AD,Ä\x0006Ä^ª\x00147}ò\x0017\x0003a	@6\SâC·y¼DÝ\x000eO6Ópÿ\x0004\x0006PÂÐxÂòz¿Æô¯î G!Øû4\x001e3\x001c¿\x0012Óô\x001c\x000b"Ò}6Óp	#
\x0006t:'!³;ò.U»»¾YK8â(8v2EÀ\x000e\x0015U\x0013~\x0011Um\x001bYíÈ9:\x001f\x000fôF«jPýl¦ñ\x001a\x0012|5v%kÈÓ\x0019}¶¨¾ý2
\x0000H\x0001¤ã~t¯8y³G[.ÚàúÙLÃ=ÌîXrªJ\x0014§4®Å¤9¹l\x0000\x00026»p
\x0013\x0001MÇÂÃ;¡ðépeÒæ\x0019$BéD¦a£SVEÆé´D¯4\x0000+\x001958x#º\x000f¼!OÞ*\x0001\<P\x0019\x0016ÓP]HÂHOVQ®^h\x0001/Ó \x0005\rÇT!æ%Ðt®]×¦þlêõná+\x0016ùi\x001c)\x0019ÑFX\x00149 6Uu7Ëð\x0011KÇG+nzµåÎõÅ¾öíf\x001afÄGp@ctJ\x001a-æÈå´8½©!Q»n´j\x001c6RµÐ#\x0017Îûdó2dóÆi|X®	ëRo-lZM¤µ\x0005 ¹ú ø*ZTîWzÎé\x0019G\x001c²\x000cYÖi»%\x0014\x0003Ð\x001e))±ÌÁ£¤ÓöÅf·\x0005\x0001¹ebó\x0013Áq¬;¨Ñ®¶é\x0010]<Ý¡,\x0013Íu\x0014)£\x0011áQ¯<¥\x0014&t°_¹ÔN.\x0015µ{*êSª0ö\x001aÑÕº\x0003R$zàÈ\x001fïW§Ö_p\ï\x001b¹8n\x0008;/Ó ì\<Èk%á¿L]0=÷³ÞàÃÅvÏ?à³\x000bñzõ
ä§£±Û\x000b°~\x0011JÎ?Ü¾¥È\x001e@\x0011ôÏÌ\x001b9V~Mµ\x0007ªL\x0013\x001d\x0010H8BÈÈõÛ\x0010ÕQXú-fËu\x000fÑcVÀÓðð\x00145Í\x0015x´3¹ù\x000fÔsÅaOheÊ\x0013G\x000cf é\x0011Zs\x000c¿¤q£I¼;[ÞÒhØÚé£Ó=G>Þ]bôöìY¦¶I×[²P\x0014Åµaû¢KFEf÷2È\x000fP
u\x0004n
b\x0018[âG®Ïb©Y²Ús`%
A\x001f7\x000fÿ@¹¯j\x001ck=H¡\x0019Ðö°\x0002é%þÁùüªb¸ëÕæÙyál*8PÉÂå®U;y\x0012Ã×\x0019«Ýå\x0003AtI¸ûI8ÐX©8qDîæÜÉÀ~;<¸üyZ\x0002¹LÖ
t\x000ck\x001aþvæ)&\x0005õ\x0015òùç,9wæFÒÉ^y\x0011\x0000\x0017nX('úCÞzÅ¥ô/dÅ¥6Hõæâh
5¿Rwo=Ó.2\x001d«Ó\x0006³¬ºg\x0003ê7 v×tq\³a]àáâR¾,Üîi¿ú\x000e\x001eGI}\x0013UÃ\Kôôãµ\x0017\x0005E0Èw²ÈÇÈçmrîå+/\x0017(eM¡'Ç»¥âyË®V?n\x0019¬¾ä·\x0011ltkLb\x001eGø3·æÊ\x0003­ù\x001d=
\x0001[å\x0002\x0014ùÅ2^p I	e ²L©f\x000f\x001eÈs´¶jþ#à»pAã/ø@6\x0016\x000cçÆ`þà¸¥\x00106HÂ\x000b/âa'\x0013RÖ¤´åBæ\x000eâÈ\x000cªEX~¡h\x0012ßýéá\x000fÏoþÓ»wïï\x0006\x0004Ï
@æ&Öcý6®-\x0006ün\x0015Å~þÑºöyÿZTå¿Õ\x0006\x0018e!¤ä
PNÊöpÁXTå¿eàIE\x001a
#GY¥B&Òn\x0018¨Úd\x0011ö¼5v=©3%îö¾\x0018DE\x0015þ[FÞÁa9r\x0001(«F «Ùï\x0003."ë0ø9I]mFÍ&\x0012|7\x000cT%ÓS¨\x001cT l7ù7»¶\x0002J\x001di|LÆ\x0006\x0006\x0005o\x001a\x001e\x0006û[QÿV:ºÇñzóåÏÑ\x001fnÑú\x0018\EUþ[AVJªCå½AÀ +ªðßÐ[i\x001cÕ\x0008ÇyÁÁ]ý7»pû§]öí-o²\x0002ÃMÙi)±¨²ÿX0d¯ã?dú±dÞ
wU÷ß,Ãí«\x0015çÚM9ÌÙÍj»\x0019uÿÍ4\¿êJª:uû¢Â«-67±¨²\x000c\x0017í¥j$Éæ¢¯.
ò$Ê,ä	\x0012N)Ð©t)¯>ÈÕMñxS
L L\x0000\x001f\x0005\x00129rM0z»6¿\x0019î_ºf±¨ÚüxÜ	\x0018(l)ìh2e|Ò©{iÔÐ7ÓH¼ë\x0010Îè\x0002W\x001d²£ÉÙVÏÉ4£Ö³,C­§u¬vI¥+0íÜêfh\x000bOÛ
\x001fØDÔ\x0001±hwç\VGofë¶ðf;Ð]ÄêÞ\x0014ôÛ½tÂ\x000f¶ÿí\x0007°^`¿¥ÁGµÌ¬[Þ\x001aÓs\x0000K?\x0019åò??|º\x0017>Ý«Juçy-$\x0014y\x000b	À¿\x0011ñ\x001a,"©×U(Õhz>3@}DlöÀÇn\x0019Fß\x0004D~Dµ-¥H\x0000¨s \x001e³Má¼[	µñ\x0016C\x000f·ÊÀ$
Õ1^ré|\x0018TuQC\x0004\x0013\x0004<IÑL-2GAHëÃ I
Ê\x0017\x001dy\x0001Ñ*Aq®qÄø5ö1'ó9ÞM/5}\x0016·ßLw\x00182¬\x0005ç\x0000WÌ
]u\x0005bX#\x0006\x0006!å\x0003\x0000Ôäø/\x0002T\x0002kä	¦VT#mê_\x001c\x000fÐÒÄ@)*<D	÷#\x0015KXoA\x0017´®¿ø\x001b×ý%O±
÷\x0017¦a`<ú\x0015·ß**É[sm/åsd·í¿Ü¶Aw¹l\x0003él*Ô\x0012\x0019\x000câÉU ,a¡¶/\\x000féËm_}Ê\x0000rÄiP& ¸[ÂÄ¶\x0002ïsÿy7Ý¾ØôÕµ9¤wJ\x001c!\x0010ÄÞ]?%\x0013?\x001eÎ^9·¶7ÓÑ}±é«ó\x0017ý\x0017¾ð~>/6}u²cüÒÏxnÉï¦Ó\x0017¾ðÙk\÷ËL_9Ö£ÛÿjÓWç:ö/5}n÷o¦ûBÓõê9¨È\x001e'íÃ¯¶­=t{Äò«Ò\x000f\x0015ÛùÊvFrÛ¨½\x001e;\x0017bEÐl·Ù$¶´0o\x000ea¯cf³§PéA\x0002+r®m>
ã÷*½·ÁÉÙæA+wìJÂ\x0003sÉJ3 d¶Øßhùûw¸S	¶y
¼êÇ`\x0000	dEQ\x0010û\x001aÁý\x001c\x0005ûÛ\x0005X¸\x0000[B@Î6aHîºRQ\x0011²3³\x0000»Y>Ü®Ð8áì\x0018¬:X.fæ©4u.\x0001m\x000f§+h\x001c\x0010ÓÌ\x0012ÜR¨¢®«_ó[ç
Ðf\x0019\x0006SMýX²\x0012{q`Ú\x001c·h-Î\x0005 Í0ì©\x0011PÄ\";j_7»0ð22ðHÖ	\x0010.g5ÎzAl¶Y\x0006\x0006ûT¨\x0016]IMÎERµèÉ¹u®þlg^®\x0008¼Ç¥)Ë9K]¹ 	[=\x000c6RMa\x000eÚ
µËq\x0011[_\x001d9$loJ( rÅª«1\x001a)hØUÇÍ4äÀµc¦\x001acVt¹*ÉI+ë»:tÈØ^)W\x0015Ä\x0016\x0013³\x0008ÞÈZ·ÁÆiH¯ÅUi¯	¦ª
xÁåµñ¾¼ªñ[yR¬ï\ÏÜ,Ã\x000c\x0017-¦Ð*Ã'+ËËÇº^ 7ÓªrÏ5ª\x0017­JÇù$lYF0\x0017!4	RÖxqð»ÙHãÍ.Ü\x0015O¤Ä1ÇI\x000c\x000cþeÂ0ÎÙÞn\x0019Ì\x0017ñ¥·T\x000c_ç\x0000¥\x0006Q·R¦®é4n\x000c Ã\óÕ¡LOø¨pÍ.êyròI±/¸¡ºFÂÅ µ^f¤ª¼j7Ûçi3\x001d\x0014rßP½&Ì¬|6d;ÎiÍn\x0018>áxR#\x00082ÃA Õ%Q\x0001ñ9÷ØM\x0003\x0015K\x000fØÝ\x000f2?È\x000cO\x001eã½¸(£o¦!\x001cæ.KZ\x00141&\x0015®Eµ9[qN=vËH¦ÜÐú-¦?,«KèçlÅYDb³ÿ\x0007ù'/aÜdºg¹½\x0012LøOï?~xÿôþÍß}úþÇû¸G°®¤\x0002Ò\x001cH\?Cª0ÐÆïnMÞþül\x0003I|Úß®q{¥ âå\x0018:\x000c'j\x0006ãÔF¦Z¥MýÝrúRËç\Û+Í×Z>W§¼\x0006x­ås\x0012ï6Àk-\x001b¬f^3ø¿ÖôÕéð_|:\x000c\x0006¯\x0019ü_kúêäA?ûâR¾x¡Íøo7]¾ØôÕÙ®ó+M\x001bõs¯ë_kúêðÁÁkM_\x001d>è;¿ÖôÕ	Ù­\x0011l`Z*J0»5\x000e_âàX6¨ìi8!Bøq¬º\x0001ëÀXrgxZs»Fá|³\x000bÇ#\x0003?ñðö\x001eÁWbSôWøpu:`n+Ê \x0008P\x0019<$W2ÍJ+ÒT4âÉR¤xþéáù§÷÷¢ý\x00191\x0013³Uã!\x0016X¯\x0007Ö¿äfàò­\x0012"ÝâzÔÄÏ#¡¦SM¿	JXGòÊ2Î@Vb\x0000õ\x0007d5ål´#g\x0017¾\x0019QdQd\x0006Õ\x0011,òzR\x000cÅÙJHe­\x000c\x0007lo\x0019æñé 
\\x0000»a\x0000¿g^2°ºdÚ¯\x000có\x00142²ä¦ÆDe!ÒtÛXòEç}³\x0013û8g\x0005\x001dB¡ÆNDUGÖl\x0015»÷e+T0)&÷AZ²)\x0006\x0011¢ÏÀû\x00057¿ýë_þøéwïþÛ§»	¨sã*O^¼\x001dðYP%Ü¯ßò³¥?KWulr\x0002Ä\x0003' ôÿ\x001f\x000c<\x0017\x0010Ö¾<©§@/!7fÎÏÎ½ÚÊª»e\x0000&Èkö<%?î\x0002\x001d\¦\x00141{ÒO¯¨3ÙíÉ523L.ÝÖOÏ'ýôÜ
1KÁa^I\x0014,Yc\x0012õ$¡.([0g£ê\x0012¾+ó\x001cf]:$Ô32(LËTyÌÎðdÙ\x0018p=i¨K\x001e¸í½ÒsÌ=çRÍw>¨Kµ4ÑmdU%Ú<.ò\x0015%ÈIE½²¨B,\x001ai«\x0004¸Ã\x0015%ÈIG]\x001a6¶Îsê'?h£óIG={\x0012z\x0011ÌÂ$²\Cö\x0017ú|ÒQ§ÑÖa:ðhkjUùLw\x0001\x000fÎµlÎ \x0010g´½U{!oÄ.W÷\x0010ñÁ\x001bå×ÍtäëªÒkH\x0017
íY+´Ë°BÇE;%HÞ\x0014q`ìW´ gvåX!\x0015ç9¬ÜR\««ÈcaGj¦V­\x000eÈ&zu\x0017\x0011{,\x0001e£­&-'é¡ñVû+^\x0010-þÞ·¶wÕoI¹\x0014s\¦¯.#¤µ\x0017\x0010|H"KJUÓ\x0014ÕÙõ\x0002ÖVÈXuDÐq«¹é9â\x001cÞ0\x0015NÀf:ÂªýäjÃG$KR±æU¯ýÕeÌµùS°½Ue:«{¾(\x0015-Ö\x0011§2×æ A>câ\x0013ÒÔ\x0004
\x0016ëSÉk\x001dÀs­^ò¤F9÷öföºìµöL±+¡×\x0014£²<³«\x0003\x0012Ã\x0017>1\x0016ëÈ²||ÄÚ
Â#%\x0005 Ísþ$_y\x000c\x001eDLC{«WG-Ã2;\x0010?7ºÔ»(8â\x0004¡MÑÑgÀD^ù©\x0005º¹\x001d\x0010ÊC^»ß×ÿ@äùÍ:\x001d`\x000b³®ãmïjÛc:%:çz8\x0012ï\x001e¿ÿQÒ_~øôôîÝÃ½:\x000e±QBUq«Ö¸´©,\x000eÑ¿ÐáÅ/ë\x001c§ëÓÿ»±]ò):\x0014ßì_ðâ¯H¶êb³-øBÛ^>ªeÜ¯¯½\x0019_i·="B\x0015kÇoQ\x000fûºõøò±p\x0018_\x0012¢\x001c±ÐÈqñø\x000bf¬ðÒËT­\x0019F4æ\x000cÌ\x001f3ú\x001dQ­\x000céÁ×,ò±õ0U1\x001f®­ÿpÅmþû/û¬\x0006`\x000eJ¿üññ\x000fOïåîþæÃ§÷¿¿lKWòv¢æzà
=à¬Z_ÒË?ûÝMÈï3@sªH¹T\x0004à±uUW&
ø·Ï¨Ú\x0000Í©"åk-\x001b=}U¥|­e\x0003Á¤ª¯µl\x0005Tòµ\x0005ão\x001a8F
ùP¥°À\x001d&-M>[óeUWûßüÝãóïïó\x0002
W\x000f\x0017¥Sm·\x0017°´0HéW|\x001dYÝ\x0017ÐüWUå«Ã}%\x000cÿê\x001cF¾ýøØ\x0019!:â;sö·|¼PÕ'jåÂj1rôçª)}´\x001b&'\x001bÊ¢ìN\vMU\x000fö¯ºÒß#¥tiã a§ÈÖ[±+ýá#\x0012\x0010Æc\x0000ôì¹ \x0012µ$A4+|»aàõK\x0005DgJJD>k<¼¶\x0004Üf¸áHYAWÊ\x0001±¨ðt
«\x0019C7UUøêxí\x00034\x000fGÊDÈÓX²\x001cm\x0019¸Ír]^Y3d_DÊ\x0014Ë)ý²+|i$ý
z´5ú\x001eÜñ\x000c"æiO¦\x0007\x000fØ\x0018|\x0014¢"ow\x0007îê¢@\x001d®F\x0008²Þ\x0014ê-fUTTÏf\x0019\x000et\x0018ç\x000erèæ	^\x0018\x0013³,äàYÐÚ-ÓÁ;\x0010¾B&IôOkÎ\x0006îváp(\x0010Æ4kTA\x0014©ë&zìæ5þ
|èð@öK¥¶CÑl*
éÚ%ý\x001b8%ûyñu\x0012ãn)ý\x001b´ {¢·]$éÊx\x0006¾Ð\x0018×2\x0018ÿ\x001e\x001eÈ\x000f@ftk\x001dµ[p®\x0013ÁÒaüw_x\x0002í©ÍE©FdFrkqRÃµdöA¡ÃÅ\x001b37ûâ^Ï/*ÓÛÎ\x0004\x0006\x0014ÇÐÕÛhÉ½ùz«ÿ§÷\x001fßüöÃ÷?Þ)øñUFM¶÷õ3òÆsóy¶È~ö\x0014B\x0006g?\x0003p8öK(ÂÛ\x0007E\x0018)¦\x0013¤Ôw%yPò\x0005?QT1Jª"lM\x000cìn|ã"clÉÖg¬j\l:22´
N\x000f]aÃs\x001aÌàG*HÉÁB\x001b¿\x001eXV8¤Þì>dU<\x0000sÉ@%=¾Î\x001dÇ?ó®\x001a\x001dQE)\x0017\x0007ðÅÃkö!«¢\x0018È¹"«±4¬é\T./¦\x0015I\x0018¬+QÅ(¹:jqõmFè³1·®Áº¢¨\x000bòx)pü¡ûÂZµ^Uã·¢¨EQ\x0014U3	öuÍ"8²8Êª6ªs7
W0uQRápÐG×ÓÓì6äf\x001aî P¸x6\x0003+\x0008lá|t\x0016£Ë°\x001d1m±¦ptÀ£S8µÎ\x0013C©­·Í$ÐÜ\x00073\x001f¸\x0018"{A\x0005zÚ®X9êbå÷gz¿ýs"½¼8Ð%\x000b\x001b|Rñ¬h±\x0013oT\x001fþîÝÃ÷\x000bh÷Ë\x000fïúôînúz¨¶\x001cS.(ÿ22Èøu\x0010ï%4ã\x0001:ÇZy¸xðuÙqÃ¹©öHkæÐ§ÓªÃ2\x0017\x0008é¦ºq7±9Õ\x0014îS
àQhÕa)öÀ¹\x0019\x0001[V#:;ÙrNÍÜ[Ë\x000eE5 B\x001dR)%×Æñ¹ðÉ·Ö\x001dKhÆÃZ\x0019BQÂÄªzN\x000b§iùÃíóÉ\\x0018à`¤JûÌCB\x00013.V\x001d\x001eÀu\x000f\x0019çXuÔ\x0013À\e\x0019«ÿtÛk*\x0017\x000eÎHóL´VU\x0015¥øuF^ø\x0007"ÿ\x0003\x0012\x0001á\x0007õLLU;7âe¾Ëp1äûnÜ¹ábþ÷ÿü_ÿðÓ\x001f\x001f~ÿþ~ºÆE%Âá\x0018-¯zÜµÊ$à7\x0012â=Fñ`7Ý«áé	ATY#8rée4OFW)½\x0013\x0000næ\x000fÌï«]$ß
)IÁsGºf\x0005Ä)Þòj\x0010ß<î&¥à«XC%Ò1\x0006ñÙF Váà¹æ¦pkÕ$÷Ü-\x0017r¹0«'z\x0014<WÿwgFÏ»eÔ\x001cÆ\x0001Ã<ÂTµ\x001bE\x0015R³·G4o:óDá"Õk÷ªªPL
ÏÝ0Ìq
c\x0018\x00138D½Z\x0012/yéÜ\x0018u8
µ+»ºU\x000f\x0015\x000e¢*1\x001c{¶ëp\x001a\x000f'£\x0014mIEGf÷³\x0002ó«cçñmë´Ñ_\x0008\x00159Oõ\x001c£\x0008§Qeë½\x0010L\x0015_mf
OuiYìÏ·E«×\x0001·5çÁ7	`G::?¤ùþì\x001bÎÿÂpÜð\x000f¯ËÚü4\x000bÝjÒ¶s+0òß<Ýíñ¥(\x0018TÅZ9\x0016´'øVÃÛ±[º¹\x000b¢tô\x0018ÉÈ\x001aùà§É°nôQÛ©\x0005äPsZ&zòX«¶lF»e¨l,1¢I§7,\x001bÑíÔR	d\x001a\x0008ã\x0014(Ç5ß4c,ºº\x001eõ-\x0018\x000eI1¢'Ïëª^}=Èúk¤)/á¤b|V8¹Ð²
µÝ,qû X\x0004\x0005Ãöü\x0003ÚP\x0017rvÚÄÄH\x0016¡²\x0001KÜC¿Md-\x0008Ð¦¶DyrïÏ ­ñPªAñz|x/ÈwOïïäTXÞ'\x000bcÕþ\x0013z\x0000®H\x0001uÏVäÏ?\x0012òg\x0005´Í+"ÓÇ¬n\x001e/<¥s¢°J?}Q$ãÙ¦§Ï§::*\x0007Ê%0FXQÌxv3|8+iDB<+'$b¡®¾0hálÓSíã\x0004\x0002xbìDågº¨É^¼9²[\x0006ô!æÒDQ^¥-Ö9mz^^X\x001c\x0000e\x00041¯³toö|Çn\x0018è!Fðå¸á\x001a%3\x001fU+í\x0013vYÂª}c^ºkvÈÙô°üë²1+ßô¬¼X>¸fgéê\x000bÅÃtº\x0008fï\x0000ÜOæð±É\x0007ºo6=ûn7éf\\x001d9\x001c¿hÈÏ5+«,cÀ£[¢nnó$í¦íD0.`:«IK¤%Ó)Øã\x0017»éö¥ûquSpúB´]+8»3Lê]øp)Æg\x000c÷7=Ü/J\x0014Çã;5^¨&idd<üË ¯Ý,£ä@'Ë!j)\x0011Ï¦W\x0003ß\x0018Àoz\x0000_Æ \*
wR3HÏÇã\x001cìQr ã5\x0014ÍZRôÌ®«ýX
RW\x001a\x0007$F$rPK×ú'`[#s_£\x0017W\x0007\x000fç#\x0002ÖuF<å\x0019·o2+>\x0011aW'/à\x000c\x001eÀN<B\x001b¤Î³å^7Ã0xñºËbPânº?\x0003;ú\x0014\x000e¥NIª?a^RWG:¢
RÃå*¿Æä§{èë¤3ªÇi8x\x00015E&\x0010²\x00025>3Þ´Ågr±jùÃ\x0011Í\x0014ì|%Õ;Ë\x0002ÉIXùæ{xñ"Î?\x001c·\x001c\x0015Årñª\x0008£æwÇýYò\x001fþâQ8; ¦\x001aÆ\x0015ë\x001a´\x001dÆ\x0017ëâU8n:ºLáP\x0017qEÙvÛ®Ø\x000ejþá¸6\x0015G¸D4R{å\x0007¬\x0019Ý:\x001f¡ñÛ\x000f>ÎbÆ?zº\x00177\x0002K¬ÙÔ
3ßF¾P 8göJFÄw:ëÈç´2Î5Ã0ÇkI$¾¬gL\x0018¸uÇ%ÊØ¥\x0017Y®nÇ.þ¡aÃj(ïö©¡\x001c±ð=\x000bÛäÓ%U¯g6ÄâöÁq\x001c 
{\x0003.aîMT{cµzºJÇéüõÃ¿??|ºSR\¢ãk\x0012o\x000cÂ¹\x0013©ã\x0005ËÏÏÖ-î´³çì:-n	åôFRÕôrSÓÍêÙmv\x0017e\x000f[\x0013"#4eNíÙiv\x0018pÞ\x0001m©Ö6¢Eµæ\x000b$w×q\x0013n_\x0007\x0002#Ëqy¨6»ëÌX\x0006\x0003\x0013îsaee©U\x0019û|èºÎ[=â¹<\x0002g\x0002ïd\x0016$Ï¢0kvy6³¢¸\x0014\x0002ãsË$gr\bÙ]®	ê.îÌ÷ÍÌå»Êå\x0005«\x0004¥,o+\x0019n\x001c½ÈÐ©Ë÷S.ÿº5\x001b±KWÙü$\x0002\x00050Ê\x0008ºXz®t>Ì«\x0003h\x0004.]eó\x0002¢À\x001en®g4é~\x0001\x0011ï*}K M\x0012 WÂ<¢¦Â¦Ó]\x0018QKWÌwÃ1xJ3µøce­z|T»VÐu­`¦(`Úe\x001aÔ!\x0015
A7U´«KÊü\x001dC\x0014n)ù©5rL>ÎÐwÐË\x001dF@Äø¿ópx*IYH7#íî*í\\x0008lGø@~´¦\x0016Õ¢çN[½´ýaáièWí·Ù
Ü\x001d*Ûo8\x00132\x000e¡g°[fÎ÷,ÀN#Àmá\x0017Zà_>|úáÃ§ç{aÑ¸1\x0011{p{]}Dü4H5¬}\x001d,<\x001b»U×\x0002Ç\x000fÅ»8\x0018"³\x0010µ@-ß8<[)`³\x000c´í\x00120Ð¾P)²1ì©M´\x0019\x0006jõñH"xgz\x0001&U}øv)\x000cNìðþöîDaý\x0000@B\x0018é.¤\x00029I¤¿Azá\x0014~LôX­³ß\x001c\x0018né£\x001aü%ç Ñá32þw¤%54\x0006Ù)Og0_Ä±é³\x0007IUçSÈÓd+Mäs\x0018±,<Q+¬B«PÎÈç\x0018Ê\x000c.W®s)ÚñæÎ@À¼ß\x001d=JÞÏ<Òfs¯Ã'¯6;_¼$Ç?@þ5ÿ1ñOþï\x001eÿã^bæÉ¤Òümâ·×Æ\x000cyÖf~þ\x0006jNEîé\x0014æ8wâuÊþtU;ùë\x0012C2&~\x0015îxZFvÈx6eì]gËs\x000eÎdT¸ãÜ\x0013p\x0015%g&uÆ\x0013\x0019vÍ\x0014Ù
c\x000b5coÈ7\x0015:\x0015ï»²lª}ï¡(ï\x001aÏ\x0017_\x0004»Å'}¢1ôu\x000bUÛp7<\x0007E/Ù\x0004¨ìv!SLí-.Ø½åf2ËSV7ý¬1ñuéq\x001b±\x001b\x001f¢4¹G¢dÃ\x00017Ëv\x0002B#Gþ\x001b;á¯t@ó)OÌ \x00181,{FÈ}êÒó\x0005Eúf\x001aî_ÎôùÆvðÁàBâØ
1ïuk¤ë³HÏPÕ¿\x0004Å®Ûg»ÉHæ6ÓpO\x0010M7\x001eóÀUÕSÙêE.·Y{"*å\x0019üicëòÅ)ÚÉÜf\x001a9ï±¾$\x001fò¥3«¬¹\kL9ëÆoá­.I7Â=Ç;mi#OÜLÃu\x0001àOcRÕF×µ\x001bW\x0005Ú¾\x0002CAWG¥2$·¹^K\x00105«ïl\x0008ÁV\x0008s\x0000\x0001g*óÄÉDdÉ¡.ËPQé¸Ã° PY¥1Õ%OHAç¾Y+Ø\x001f\x0013îH£UÞæÒl¾½Ý4TT<
æfÉ~¨Y36MçìFõf\x001a**.aôçcfÞÜÂ
GcÕÑõÙMñ-4:Õi¸n
ÞV\x001d¸ë«ÄfÆªm&¿Ýr£­Æ½\x000fMy¥ÓV×j7i\x0010Y
$2!1ÿEQAÒø3\x001d¾:{QUóÀ´`«\x0008Ãî\x0018¥¤YÍ³äJiòÆùa:ó<su\x00134=,MÑe\x001aâ±\x0006)O­ã\x0007\x001dÞöÖ\x0006sà~\x000b\x001c)3Á#\ÉÎ5¦ÌÃui?Äâ{ÀÄæ_·þó8å- F
Í­\\x000b´q§¯ªò\x000bË÷Ñì¾ò{SÊcD	êi\x000fÁªv .ÂÞ\x0002^\x0001¿zzþp'u\x0004\x000f:î¯xw\x0006¦Lý¤¸\x0010¿^°QÐR\x0003±8ú\x001b¹â[ê\x0004·Î¿}&÷Íè\x0003OË
úÀq<qh9&\x001c¯\x001c¦³WÛêW\x000fÁ¢¯í\x0013»|Ä\x001e\x0015U(òpÑ¹t®kç©>\x0016w¢ú¸-\x001b9ñ\x0004\x0004\x001dH	,¼pWÌG\x0013o=HJ¶ã?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-11.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-11.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=^ùì.V×\x0008\x0003uZ\x0005ÎU±Æl\«\x0018õå,:fØ\x0016\x001bÉ±P\x000cj0\x0016\x001eù1\x001aàU4 õX\x000b:\x00052\x0015±ÞG¯Älç\x0019^E\x0003È·ÏÂ¹ºµ×g,ygÚyaÆ,{À¸pB¬9-tõB\x001a
º.ÁÆ½S'\x001aµ¸]\x0006ÊÜ\x001dÔÑåmT©]ðóÖ¤\x0015:=zÕ{¢¶åñ\x0002%`2ÁÊó =u\x0016KD±¨\x001f0­aZN}<(PNÍ_ Â]³/H/o?\x0000åÔq!Ý~@ó`\x0012Q)³µ¡\x0000áþÙÿ$Ýy9\x001fÛa!TlÄm*\x0004§¸\%=1±âÜÉ\x00149êÒÄó)ÄÒ#\x0012óÒ#\x001eñ³ÝlÌÍ\x0006ÜÍßDºP4±\x001ag°°Ìb§\x0011!©÷~D\x0016Ñ)e}\x0000½8Ð\x001eËãúp«lW\x001e\x0004]ypæÇ"èÊ\x00037ÖÉ`L5zÞ|jgóh6d\x0011ø¢¿ß\x0003<Ç`c\x0005ªj
%íÒæY·5ÐLqHµWÒ®Ë\x0010âÙðaÆfÉ²½ñ1E\x0015ôÍ[æVø\x0000tåw®ç©=³\x001d\x0005{ë÷7kQìÃ¥jb£ÅødÜ[
y\x0011-µ}þµWÄ­-r%G6\x0017A hp\x001a^^Ú*&&AÒáAoäeµ<Â\x001a¢mVMèeÇ\x0010U°mÍêZ\x0015~sõ}Tk÷ºµuE\x00069+Üc:=ªäQÎI<âf±b9UaUºKM*àÑ/\x0013çZTIt²?ÒÉyws¸¾¿¾ÐQÏ\x0006«¿I!\x001d«øÈµ¢\x0019\x000có§VûÈAOp«U¥\x0004\x001dc\x0019´Öãøì6Sí&$ªJ	Ã¼ÂùµÆ\x00033FöÖãØ§æ\x0007=ªR	ÃUåQ&ð-tåggñ½[G÷N\x001cvU*aø
IZþdi";v¶;\x0019¤\x00158ö%ÇØ:H¶ê\x000eäÈVÍêÍe^\x0008\x001fU	iIR!eXàäFà¨¨&¡¯Óähe­·\x0006BÉÙ$¬ÁàÒ©+\x0017Uuá±
rD\x0001'\x0004åÉp*c\x001c\x001a)ö¤±,bÎk~
OÝß¹¸àv\x000f±/Ê\x0011\x0005've«*0kñÅ	KÈ
Ýï_à®\x0000á!F\x001c\x0013Íó\x0008!</]¾{\x0017°;I#\x0005Wã\x0002£\x0008«Æ\x0011ÚÅ\x001d\x0015ºßÀà¢àÅ¦ýn2\x000e«í3¡	Yû
dþ\x0011!\x000f¦+ÃÑSQ\x0001×jÚ¿½«Ò=fÓ/\x0005?Ç¦öÁeK5.\x001a¦\x0016ÛQØÒb3±Virú ö'qR\x0005\x0012wxÁ\x001fpPÅáÉ¢U~ZXV\x0000\x001bfVíö\x000bÂª5Ìà è²]Å>d\x0012\x0011Îy+aàI²5óöá}W~õ«Ëå\x00036SÆxÌàçUÔVûÔ\x0013Å}e1}Â¡Q8WQ\x000f`¸Zg\x0008ÑáZè&'µEC£p,²"Ù÷"Ô0x \ ä4Ïë¤±Q8B\x000brÅh\x000emjA®­ämRµ¤ûI[\x0018¾QÖz&\x00147§íJ¶káêíÍÍ<å\x0019
$¼Á*:_Í®÷&\x0004\x0017´Vnd%éã\x001f5 0%|â\x0007¬j÷\x0012ÇÄ\x0005äç\x0008\x0001ßf¦þ9"üt´\x0017ïðÙáÙ·?\x001d\x001eþ~¡Û´Ö\x000e[ç¤3\x001e¨}i\x0013ª¿Àr=¯bEmF¨L§µ\x0013Å>>1ú<ô¯":$Ú­7E¯&¦§ æøVb?	\x001b«\x000fg¸úW\x001b\x0011õKòh\x0013ÔjçÓ¡¼jÌh&¹È\x000c\x0001\x000eNÙ\x0004ô6MªõÄÜâ\x0015ß\x001cîï/G1¡¦Þ´^´^q(g¥Ç/¶ëÛè(WëËY§É=¯Øp\x0003\ä)ùyvÔè(¿rü\x0014s­@åhV\x0013äÃN=Ñ\x0001Q.&\x0011ù-ÃF6N*\x000b¦'&bcvô\x000f_.\x0011
\x0001\x0019½u[B\x001e9@¢½OÛ#ñÉ!® JHØ:^\x0018r\x0000«"½PH"µ\x0014#MbèªíPés÷*\x0010Ó³ÌWa!4¨\x0012\x0012~8\x00009úç°äY\x0017\x001fãN£ºS
7åe\x0014î\x0011Ø.uNbÉx\x0004Ú\x0019\x0004ÐUeJÃ\k\x0019<\x0002\x00100ã5°2ûõ\x0007Úç¦\x0015ÿüþðêRU#)£Þ\x0017-ÙÇHW^ÈÍ¾û\x0002\x000f¹ÕqÜVÌ(³\x0000Îa;\x001eÆÖé {ÈâñO¯\x0017¿U G\x0005<-òÔQÜVS×3dó:U3bÔ =2ì§u~\x0018íÅ7\ì#Ù]8^\x0011\x0010´fá[\x001d\x001dnfP28~+©*D~ìÌgq¿¿zùÓ³ß^,]\x0014U¬÷1wÓ(\x0003É_TÂ\x0017ØðF²ÒçÜ\x0002õ\x0000wöC6
¶ÙîæíÒ)êÓèìÁ(ï¬:ä!ö\x000bwÛÄ\x0003úÔ0¥£ èË8ò3yµälæI¤âÉ\x0000\x0004urËYÂ÷H¬J¾ú8©ðb'/IáÇ\x001fì\x0015}®;aÀ¤Â¶JÚ]ÚMU(\x0016ÑíçQCÍ[Ü³ã }ûþ\x0015Ú¢òMÈéÏSÿ÷tä×,²7d\x001f÷â\x0016GKµº%\x0014tZ\x0003®s\x001fw\x0008l>Sàû?`ô\x000f8Ù~¹O\x0017ðq·é\x001aM;Äm\x0012¿ÜýëoÿõÏU2\x0017ÕLIÒ<rµ1Ý\x000f5«a÷Ë¦:©Ëp¦¨©Ð§\x0008\x000bWrÀõ\x001c0*\x001bkæÈý¶\x000e¦BÒJúUÒ7\x0018³%LÛÀ]'ÒË¸:ë\x001b(ÈY¹ZÖL­Å#r×6\x001aiÞ²\x0013\x0007\x0018¹TLù:Mæ\x001c³@\x000e²KÏp\x0017Ä\1Õ|ëÄ\x0018â\x0011¹+EËK \x001f
¹áb±o\x001cÄ8U+´ÓSKK\x0019nçÚ·²4\x0001mº\x0012qÀ8B=ä"õl¤RÈÜÄ-\ø\x0018G}{D\x0016{XMk	?"3uO\x0000h\x001c8Í$xS{\x0016X 7Â{
u>Å©Ö_×^¶2ü\x0008ÝwÑY å¹§\x0019v1©îóÐfYÄÞ+´ öæ¤¨%×	³ü\x0005§¤\x0011tÊYQBÿííÃÝýJMõÍíÃábD=ÈJ;\x0019BezvÑ\x000cÉf¦çCCVUÎï­ýÄWÏIzF·sp'\x0014=CÛ\x001fwr\¦<fß\Ý½¾º»¾X\x001bzÆ2Ãl|g«­À2`ýÂ÷¤I¨\x0012?ilõ@Á-ôBñZoTÌ¯¨\x0017®îÍ\x0019è3L\x0005ÑÍ\x001a\x000625Ì>/æèäÔ\x000cü\x00195ÉWÙú\x0000c!',Ý0n×i Ï¨\x001e\x0015zB×*dUaaýÎì\x0018å\x0002Yæ(\x0017L\x000b<¦-`\x0008ÛSµû4î\x0013ó4o\x0001ÕKÎ\Åº-§Òzfæ\C«À1	Åýí\x000e\x000eJ/H1³.îá\x001fê\x0007äØXKæ:t3â\x0004ÅÔfÂMt\x0008mý3\x000fôrÜ_GóìÈÏÝ\x0018÷/p>T\x000e·m\x0013¾Àð\x0019S·£uÎTêBqöòP§æY\x0005«£gLø/k1V®
Øbz&ÛmÎtau+\x00141*a^\x001b©}Çq­qEgeåE\x001bÏ
cÙj(0fgÌ\x001e^OwP\x000eM
dÃ\x0000)²úTF.Ï² >5Rß^®Ê\x0017nYÞZÂHÃ¤&ác½]Lô/1{õSä-T\x0011ÚÜT(ÄÕ§KGdÑPOP^:ð´\x0012T»è·äTw²·\x0019\x000f\x000b!Ëú¶fìM¯êùÌyN¶²"\x000b^=ºé"8L\x000e£*µ(VI#N+
âDÕ^\x001dÛ\/t\x001akâkz7ö6N\x0014Zrþ%=±¡þC\x0002¼á:æ¢\x0014ÓÈT¦\x001ap\x0002*íþÜêòÊêr£Ã=(jÊª¨Ð×Q"s\x001d\x001föÆË&ì°­²T,ªãÒÎK¤Ì.FYn!|îÈ\x0011ß\x001eËéÉÉ\x000cp Y/~wûþÙ×oßß^¿å\x001eÚ;ò\x0007.Æl5-M[\x001e\x0000d`mß/Õôa\x0008Ó²äÂh 5Ña::\x0008;g3\x000ca:É&IFpÆ\x0013Ú¨dBÎ=\x0015YÄx\x000cØ\x0018Ìy\x0005~dVµ.jr&c&~÷òNÍåj\x0019á\x0003ÅóÊÜÈrþÄã'Î !éz\x0014Z¹\x0018ÅkÁ¨OðØ®Ï7e~`BFn°\x0016^\x0013©I,}Ãò4ÛXuçåÃ³ïIT×
%ù «ß8¹\\x001cL\x00170ç¨\x0008êPgdägwkvI\x0014{\x0006ün[æ¼`U\x0017\x001aµ\x0001àÂ¶	\x0015\x0015¾÷ªzÚÄyçeÕF9Cá7=Z
Ùá$<íÕu³Nºoú×ÿyux¸&°\x0011;5KìUÍbÌ¬a~õ'.iæéÑrdî¥-üä\x0017ÏRl~"üï\x001f®/5
I´±;ÄNFæ¢H¯q÷{âëúÉ#	Ô0\x00182ë«l\x000fâ¹~\x001ekì°´¤½,¢½ ÷	*\x000e\x0019\x0007Fý8M¹c§EßG`á=\x0005'gÁ!YÕc´S~'½¦h/Ú>JVÙui|\x0006P\x0018vN{qDF¿L\x0004ÚX£{¤×Äô	é®¥1ä9fý-mûÕû÷\x0017½¡ë5\x001b_ìQ¹WÈ\x00122MÈ\x0013{óªe¼\x001d\x001e¦éÚO~÷LË\x000b»@Ä
\x0005Iÿõ\x001fÿùõÝáõí«÷èÊ.LUkí ñÂøã\x0016'\x000cñÉÖSV\x0015xOrº\x0006M2ß½©àtÍ}¢m\x0016öG1\x000eèf«\x000f8³Ò:»jaRlöðì\x000f\lèGÁ\x000eÌ\x0013{b»Ê¦Û\x0014\x0017\x0017èK¼gAG)vÖ~ò»g%­vzÏþ|¸9¼º½9\x0014{jqáh;\x0013-tGÒgÙ'f'øÔ\x0001~Z×5NJi*å\x000ceÀ\x0003í~^ÓªKfLî¦\x000eKò²CNASÇýf)XØ\x0012õ¿\x0002E@6-e¸ê\x001d»pD¯_\x0010cl/ü\x0017\x0017ý{ARR{êÙ\x0015y\x0000®Àè_ÆB=Bq\x0018nÈ½l[E>ç
Ë\x001aÎj£ÊµD7\x000b\x001aoÈ(ÊË!å1b2·r9\x001eîT³§6à#²\x0015õø<I\&fSM s«7(\x0012G-ÿµÃÌ¾»}MJæ
\x001dg7mÎÓõë)\x001a0WàlÝÂ~\x001e¿>ÍD®\x000bxÚâ¼PÓ't£\x001e\x001ehFK÷"Ô²,ÝÁg£~åÏh
Yp.æÐ\x0008\x0010$²\x0005dt\x001fVdílÈþ«Óâ>¹S\x0013¿d\x0003\x0016\x0001i®Pv\x0000l!\x001epXÒ¬ý
9
ä¬!ÑÔØ8Â¥\x00167Ü$p ù[D\x0001+¨ÐWd­R6ä,«°ôa¬UÊÜU
³\x0014IÉ
\x0019ÃþAKy6uxC\x0016%nì·+i0Oý<ðC\x001c¡\x0005 +NôÈ-Ð\x0011 ól\x000b\x001aÈ
Z&ü \x0000Ðe&é\x001fb\x0016w°,\x0012Ðxîãè\x0008½w	­¼¶Õ\x000f
hh6¯ª²ÅÙùË°AGCïÝC\x001b\x001f
½w\x0015mz4ôÞ]´ùÑÐ{Q\x0010A\x000b½w\x001beÁéyÐnï6:óhè½Ûèì£¡÷n£sÞ»îÑ·ÑíÝF÷ÈÛ8ú\x000cNx¿½zxs}õìw÷ï/åG Ðá\[ç\x0004­GT»~@Ë'><\x000e/HJ\@$\x001fùêO~ùLúnþÿz¸ºü3òggú­8Î&/ÊNÈU1OÞ[º#ÿAÓü¹»×
M³³ú_®äïú\x0002ß<¼½~yýîpÃß¶mÈ_\x000e7o®_\x000fÃYö±\x0018\x0016G\x0017üØWM-½}Ê;Vä\oSì!Q\x000e£Ñûnù7Þ=Ð]óß²Û^à:>&r\x00141³{Vüê\x001füÍ\x001f%+þwûg¿¿¾º»\x001d\x0012:üã©s§OÏä [ùqËE0þdKJÒÂ'·ºþ©>m6øÑøÀQ:èUæGÜ¼1S³7rö }±ÚÎhÛ|éH ;ðí?mðÆnÁ\x001f¦\x0005´²\x000fKO2ºç=Ugù\x0007\x0013²\x0013÷»«gß\x001c"Û3w4Õnú·ãZò¶v®öî¢aÖ°fC	\x0010\x001fÛÐE0zCç«>õÁÄíáþú]\x0005ÿåúææðzÈ\x0017+u\x001báTq\x0007é¦`²éÌOô\x0001+ÿÙ\x0013ëÈ>\x001aÓ8JGÝÐK\x0004M
ë¼ícq	¾8û±Ð\x0000°½Àv½Ò°k;,°A)9\x001fÇr8\x000e\x001dÚnj\x0011´©²\x0004 EåEÃ&ð!þ\x0000Ø±cÔ\x0019ÓxÙYVë\x0010¶ï3uO*V\x0001;ul+¦ù\x0012v´²°£Å\x0003ìàÐ\x0003tí\x0017(\x001cô²Iîd\x000e\x0005E²0ÓZ­\x000f;¸\x0015úÜã\x0012ÙL
ÊRA!®Ón\x001fÜ	e+æÊêByyºu	\x0016n\x0016*Â}y[!ï,\x0006É.RT»L/t\x001e]M\x0000Ï\x001d{\x000eÅ\x0019\Ø\x0001ú^V¼9ÎøÑÕ\x0004èÒ¡Sì<`\x001dªVÑºMÅuÇ¥Ù{ÿ¤tw³2·\x0011'Å¥çxw\x001c\x001eï6ôÝín\x0004VgÂó"\x001dä3:&YÉ$Æ·	ØRUù^^O{\x0019Ëó
ÞdK'~ô	\x0001[¨*fÑ\x0015ÊÛÉLÎ¡i\x0018ÂÄ%\x0004äMSJ^ \x0011J³0°lgQ,-Án_U9¡ª²\x0013f
ù8Ïqá¶ÂÍ!¤&ý«ãÄÕñµU'm{\x0019eðÑó¸\x001e½ana\x001dáÁÂb"\x001d+nf©r\x0011ßr1C-\x0014y 6«©ËTð6NêBo~L¾àB¶\x001aö\x000c9¡]l\x000bÜ?¥EÇÿ£éÒE>úÁçSôâÔyL\x0001¶ÕÖÉ,Sì\x001e¬ïçì\x001f¬ïç\x001c\x001e¬/Ð\x001e¬_
¹<Z\x001aºÏP
Dö\x0019Ò\x000f^"Ê7a¨\x0016FJÅ\x0017":]UÌØV]M&¡ys\x0018)èÏ¾\x0019ß@ocW^¢>Ì®üD>Ð§9µ,\x001e}3çk>ù½Óû£ÈÏC\x001e6Ôéèµûg¸´3ïaá«\x0012¶fÌ\x0015a<ÇX¿¨=%	é=.ùä×Î¶ô\x0008ì\x001f\x0005<î¨~="Ëß°è\x0019½Ól"úy¦ÔnçZék#Û\x0005bO¹A÷c½ô;Gþ~¬ìlFðµ3yC{w4#\x001bÙþÃhpÊ\x0014\x0019óõ\x00029<\x0016y x\x0002Á7¥£\x0015%\x001e\x000b%)Gk`ª`ì¨\x000fäÃ%cf\x0019ß-ÛÆä­>¨sÏ|È/ásÃQ·!ÐaÉÁþÚ±©H\x0000»\x0013ÀbXÔ\Óó\x001dõù>\x000fX{B\x001bp|\x0014ðxøÒD\x001bþ×üçï^ß\ß_.Ð­±ÞöKjÁX*Õ¾¸-KhxßfK>ùµ\x0013KÑhKñp÷óÃÕû±"í\¡\x0002ûoJÞÒ\x001fÕw*¸eÿ)¤Þ\x0012\x001f7\x0014ÍpñMèÝÀ\x001c/Ë²u³\x0013êss\x0019ç"\x0008d÷XäÏ¿£Ç«
qWÁ(\x000bíeX¸¤Çi\x001a×ÿÿ\³wq±Z
\x0004O\x0004Õueî\x0015\x0011
5¹\x0011ÔA7Õ\x000e7u¾ä_;s\x0001\x0006\x0015yYó?æ â©ßTæ 1Ñ\x0002_ý?útÓ5üÞ¹\x00030útg \x001bZ'\x001bº3tõló_%îjÒü\x000eB\x0019õÌ®O}òê°¥ó5ü^%xó±:ÿ÷î_ÿüÇ5¯I98?+s8*Y\x001b\x0012ö<jY[,s[\x001eWG®VtYr[Hj·ª2\x0007³eÿa\x001dÿ½2\x0007éð£xwøÇ»ëü±¯\?r<iæÔIão\x000bIN\x000151ÖrÉ©ôp³ÍL1,OZ_ÊÅ³¶¹Vú aï(\x001bôí.úä\x0007ë£öÃ½ÿûíHsûpóÃÛÛ\x000b	ÝF\CÌ£­½¦Ö\x0016nåIdN\x0016þ¬£ß+¡/¢rÝÝUú`ÖØf\x0017Û÷Û\x0019ï9\x0015[|rx;ióÄ&µÞ< ¸\x000b\x001ec\x0007¯¥M;oA¶j'ÉhÕµeÞ¢>\x0002¹Ã]\x001fz@È6oÁ¦¶ê:s;\x001c$ß\x0017Iê"ñ½©S[èï5Þ#x@Ò\x001c\x0002Ï¥UüÛ}pûXy§°\x000f\x001eúAq¥GU-/ô\x001a&ò$	¹I~\x0008\x001fÜí»úòF¬\x001cçÍÕõÍÍÅn¨e0íÀ&\x001f\x001e½õ\x001cÜÒ¹ýÙ´â°«xô®ÎW}ê\x0007¹Çî}\x0010$\x0016ß±£ÿîðúííÐôzÜs¨	ÖA×fu ,«v*\x0002Ç\x001a­'\x0017|Ô_äÓôÀ&ø½UüâAò?¿þåç·ï¾bGrä^ù1«x<Oø¤6*ª$Û\x0015\x001bÉÊ,@ÈùéE¯Í" &úðÕGV}â{\x0007Á¿øÉ¦÷\x001f¾Õqßªay¨n>SÕÈ"Úf4#{ù\x0002o½ÍD#cf%\x0002|\x0002¹ûÙüI§Oü"\x001e¨9±¡Mç­}Ñ^Lµk\x001fl#<«ü\x0007ü¬¦]ð6ð\x001aJ\x001flgs)	Í»T"¼NÑy]1m~ð\x000föôÊ÷k\x001eÏµªaJ\x000c­«\x001df¦R'm%CO µO±§ôs¥Åi÷í(\x001cpàhÑÌ8Uû¢ \x0000l\x001f\\x0012\x001cb2²G²nÀîÆcaØÏ\x000bdNaÑ$\x0014¦³#«
`÷ãRíãhÙ\x001b\x0010Ýo
\x001b¨I	{!tÍûØ¹cÓºñ:\x0013v
(X\x0012Xa±¶\x0019Úz\x0014ØÂ1EZx<^\x0000LS_z=esI]\x001a»\x0018\x0001»öuÇeÞÄ&oÓ\x001eÛº»ËyÑ±.Qouì~¥^\x0007Ád_¥E\úA\x0015J+¯\x001aÜ\x000c\x0001ÞOJ\x000e±gä,\x00175öYËµó ´HÜjW@wW eß)Gø¨\x0018´{}È\x0016·³ÕnÙý³bûYIIð®Ò~zßJC;8Ì\x0014¢ý\x000cËTêýÃbûaIx9Ûa±\x0012<9«\x000e\x001fÊ$¸\x001bjÛØömCýs\x000bûéñ\x0002åÖãéö÷Óý$c¨
lßjC;¶K¨D}\x001eK\x0008\x0001º¿ýI
²X¶ée~
[)è&\x0015-OJlµ GlæwW'\x0005\x0016é°%\x0000à\x0018
¿ÑTQI½ãëÍÒ2¿\x000c<\x0015N-q#À
Fºì2,gÿ\x0018:q\x000càßcðÔÙ\x001c3\x001epå¶M[qûJËu¥bba:Q\x0003+wí:ýÇÍÇÛçÅ1$;ÑH§Î)'¿/öï\x0017÷çÑKp\x001eZâQxÈ}à÷ï÷ââª6xíéìåâ{%öºùý\x001bäÅ
J¹S¡0ORéeàËÂ-jòerß¿B>
©øÞKÏcOýó\x0004j%å÷s©\x0007Ù¿B>	pÓÉ\x0005\x0018\\x000c?^ÀñÈËvîß Ê\x0012\x0014pü\x0004÷EgYÔ¥ñ\x0015G\x001d×éà±ÇuE+ËV\x00149\x0019³¨µÂ2bqÿ Fq\x0010éXo½6lçpV**­\x001a\x0015Ü?Qp\Óà\x0006åcÅCÞ¬¸óc\x0015ç0Â\x0005òµEìÄ\x000bTðvÆF\x0018:DÒ:¸¤å"èçYÛ¦ÖÙ#ìZ¯µm¤í\x001fòÔ\x000f9ýëvª·G¿öL¹T£\x001eýÈJû<C\x001em£\x0008<®<,´ª}åÁâYIKnÿ'qÊyy\x0008h\x0007\x0013Qk¥e|øþ;
\Ï ®§\x000b½éx½x÷CëIû§%wÂÂÛlÙ\x000c§Åeo³k\x0003:\x0019ßÑ­\x0011¢LÖO\x0012ç<*³<(±ÐÃ± ï½CV:YeÕÂ¡(R)F¥\x0014É¡Xá÷\x0014í
ìgIÛäyády¥\x0013Ç`ÈÊ+Õ>ßþt¸9¼\x0018+\x0008Îô£E+;y×µ£\x0013!LòA+\x000cDú\x0015\x001dçVsºêq\x000e°ÄôâÈÌëü«gç%4«Uî,}æØ\x001b÷YáºV\x0012*Õû9iå\x0013ÀQ<A\x0011ü7càýA\x000eA­¯6ØM[qM0Çsû\x0015)\x001c
¬7$c'~øaÁòP\x0018t¬hÉI-¹L\x001cå
X¸ÉÎ
«Üd-b\x000ffZøÔ¬¾êGèváli\x000c\x001eø\x0006í\x001e
½wæº÷}6´¶67èðhè½\x0003ÝÝú³¡÷\x000eµ}ô¡\x001eú
º<\x0016zðÐîÑ²\x001efzI½$ÊùF\x001a\x00180á;\\x001c\x001bt¬p\x000cÑ®\x001aË÷ÈÒÏ|k|õ¨ÎJìQZ\x001eD$Ã\x001eµõ~¶<üä~:õ&ä(Æ\x001e.ÆI\x0001»*hÊ×ù£àÔ£`ÇÂÈÃâp·rzÝ39çNÇ9çb>¹E;JÖ¡mÎ±¬êá1Þ\x00101h¦\x000cG¸	Ï\x0001 ÜgS°\x0019u\x0000¨ aïZr\x0008\x0015nÐ2B\x0013û¼tvYÅ90ÂÛ¨À!w\x0004\x0016q¼Lë[\x0012<ÜJï£({ÝlÐpG\x001eýÖÿòÇÃõd,æ¹éõ\x000b)Ù~1oîÂæ¸Öøþ\x0004\x0017\x0014ãG\x000e\x0016\x0011
ÉéO~îP{,Ýc'ÊÄker\x001eòäòx­LÎC¼ÇH¢6òäVzed<^\x001e£gÆ\=[+ËÆÆ±s\x000bWBc\x00016\x0017i9©\x0001\x001c7'Í»P'Uûãù6Uo\x001eÚ\x0015{x'ùB*g¥c\x0004¥MÌ\x0002¹G7Ï©ùoSÕù>\x0013y<ß¦ªóÍ\x000c""§áì2]ì=>\x000e;Gfç{Eîç;r}nw'yâv5\x001b\x000càåÚÖ<zQ\x0006\x0019Vv\x000fÝ©ó:ß\x0017dù¾'ç\x0013e\å|èQ¯\x001a])y.ôÞîNT`N\x0012
pµ`¦Áx´JJY¦Ýïiûè3=1x\x000c\x0012ÂÐªC\x001fÐK.\x0015í\x001d"\w|(|0ç/zïTÛ~ª·½ËFUðÕ7±¶àëP?s\x0016Õ3Á
*`æMA@£\x0002\x001au!i\x001b\x0012®\x001bt?{,b\x0011xå?\x0019Õ%%
¡·êÛ(!'º!?ú|\x000cIË
:?\x000eZ?½ß ìV.ââÉOüþ~uw÷Ë¥b0\x000f\x001d,³=¾\x0005²]¶M]ýlåsú¬¼ ñè\x0000ãd½'?tbîøi§üIâ\x0017s\x0014rÁ÷ß\x001eÇ±ÍæZr{óÿ\Ë\x0004<Ðé\x0011ûèl¼E>£PdÚ^OU<S\x0002>ÃÑ9\x0004²t\x0014Bz³C@WDQÉÜ<\x0019à*ýc×<*\x0015
ÊKZ>5sÓ\x0010ä³Ã¨Ã8Øº\x0019óQÂûgßÿrwõöjìÀ;÷\x0018Æ¤Íÿíâç\x0014z¯ìâ:ä§¹û\DöIþjÔÇp¾ä;÷W£>ç!OüÕ¨á9ÈÃ\x0012¾ÒAGùT\ì¥p\x0018cM±\x001e>\x0015T\x0019K¾Û=Þ\x001fÉ¶\x0006½­µJ#\x000c* ª¿8«
Ýpýãp'î|Ð9£h@\x001br)t+cÒ\x0015\x0005Ó\x0000õôy#þîÕlÜÞ¹º%8¬V)ÇÐ\x001cñuXbZùÈ¤['.9gRêÝP²*ö-nç°\x000c\x000fÑyÈÕð\x0010%/Mr\x000bú°!FD®\x001e9ê}\x001b\x0016üÑîÕ\x000f×77#I÷zF {u\x0001\ó9\\x0014{\\x001d×cæÎ!¾øî²ÍÁóÄNwº{õ¸Çu¯Ò\x001aðéþ¯·¯ b|}ßþº\x001cÁ?òôåH0Ð	s3mâù[!H$_'\x00031ÿÎ§iW£K\x0006/GbjÊ­DÖì|k\x001dê\x000b\x0005Cü½e\x0008i x\x000fj¤F\x001ei@\x001cT9¦²\x0003ð¬Ø¢\x0019ùþM}xóÓW#Ä÷WlR
\x0006ÕyûÊ\x001a7Ë3ëýÖ\x0013\x0013)]yÓ­fJÓð$\x001b;w¦\x0006é/2RyùUüâAúoÿñêåýë.ýãàÉöðüåp3{vÎÜ\x0001e1iÊ¦q¬(;%cýg\x0014JüXüAT\x0001L|ò[\x0007Ùç«\x001fï\x000eBa{¸{yxýv$Ú:Sà>ËÂQ_È\x0003\x000bÇÕÓÓ\x0019ßÈï	aHF?­Ìù"&ó^\x001e±³ê_<=å¿¾þÇß vóíÍíÐ{wÐ¹¿\x000e\x0010ÛðÅ£\x001dî[\x0010|]~rµUÌ=ÐS«Q<\x0015´éÑa\x001aºEÈÍ6±Ï¾^¢\x0016¾××¬ò%
ZÔ±\x0019SÇ6-òó\x0003Ø\x00191/¼y\x0017\UWib±\x0011cð¬X"\x001a1-OàË>x\x000f\x0004ïìäÉSÀRÙ_y\x0010¾lH$ðhÛ+ÛÁLÊx¨3\x001cò\x000f?½¼û \x001aÚ¿½}ûêöÍMò\ÝRä 6_ltB·äTÁ&;¸Oi'é
]DU#LÌ 5\x000bO³
Pa\x0013(t\x0013Z\x0011~Ð/u\x0007\x000fý¥æÙë[\x0011~\x000c<\x000eÒbß\x0003`»¨8¶\x0019øE|ýòê
h­ß^}\x0018ãMç½PÉã«s¹½¶ãbôaAðÙ
ý:/A\x0007koÑ§¾w\x0010¹¿ÏýEü\x000f!Xsö#!'$úì£x$ëÃB£ç±~NcT{\x0002M*Ê\x0007ßYôÉ\x000f\x001eä}~ª?¾ýJpüáîpûp36ÆyÊMÀeZQÕÈí}[»a\x001d\x000cyz¹kÁ/âQu¿;«>ùÅàÿv÷òÍ_¯µà?\Îöçâ\x0002*®5I/Wº­\x0012´£_"PMðUÉ}\x000e\x0016!ì-úä\x0007\x000frÿ÷÷Î
rÿþ@Nïýý@:sæ3
iÉ\x0005,\x001bé\x000c½h¥SWsooiòÏfj\x0007`\x0011\x000eÖ«D\x0017S'ûáòS«ü*X£Á»¡=\x0011Á{{"Ý\x001eÓ{ÁÉ¡®\x001eÛÂC»{!u{¢\x0002ïî¢\x000f¦g\x00138¾çúÈ¡¶SÙ ­k\x0016[w_,^õ­\x0015{i±k3\x001au\x000e\x0016ö¦ UL\x0007\x000f]Åì\x001cSgl8é?¾¼	\x000fHñýíÃÛ÷×\x0003ËÏ\x0007\x001dWø\ö(Y\x0003­ÑåsÙ£^+E8mK«8éµuö\x001c\x0017í¢ÇP®nX8`Ã>xèàëÔÏK,bVöL#RÙ©\x000bã«ÿj~N¢¢þÏ\x001fiK/³¤0\x000bØÄ[µ.j¶õÞ\x001e½àÖhö\x0000\x0016±`:koÑ'>w\x0010÷/ïþìá«O`9ó
¹laÓC-qÄ]¬U\x0004»B\x0002Rì_OèÞ97£gÖ:w\x000eÖÖ\x00135UÜuâ°/Å\x0019\x000bª.UÕ:
\´êÄ(½ôXÑKÎV\x0004÷KmvG\x0005¸hÖ)9Àó2
¦Ç!\x0000×æ\x0001Ât0\x0004ß¦ínæÉ [\x0002\x0014x÷u--Õ×|Ý Á}Ê\x0001_èPu±\x0002ïýbv°vG:òS\x0004Ï¿q¨\x0014\x0017®	ýú\x000bìþú[É5\x0011\x001b­ ´ùú\x0018u¼¨èZ6\x0005ÞO¢¥ûoÆ'¨\x001bSðùZ
åöO¢\x0013QÑO\x0005)\x0017è~ö^­|¤÷PØ¹c¯-?Çíd&%ØÎ\x0010aálØh\x0006\x000e\x0005.òÉµß\x0016¢Sä\x0004\x000e¨xá6hO\x0004÷â%LÅÈ­Lx?\x0013\x0006.MÊßCvKÚO+\x000eKvØûlsöx?\x0017ý+äeÃeí\x000c¢ü:\x0017\x000c\x0017ÙäÆ×Y\x0011|(pÑrIB\x0016:1¦L\x0016¶V<¶1\x0008}ðÐcÅ5vvs¦!Q5ß\x0006óXÛL÷°=è1db\x0012±ii¥íÛÔ
²vxBWýý©³%Î}Gýn¤ý£¼©õ©b\x000cóê
½©, \x000cÿ\x0018k\x001fÉrW}*®V<é¶y\V+#´\x0015×¿ææ¦lÒ\x0008C¾CEé­:HB»\x0002O\x0003Xð3«a¸ÎÊqî}{¸XÐN
ú,.ô\x0018:¹pâ¦WôsÆ¢\x0006»âXÒ"¬éO}êDà^\Ï·\x0002º°U¢Íß\E\x001eÏàê
¶Uü|)%\x001e,!¼rçsgWà7\x0014_~4pCi\x0004sa¼A\x000bn\x0010	\x0011òú«|>-2¸Zð\x00112nÌBMª\x001fWûòöæbu\x0005¡ æO±³V1 ótýø\x0004û¹S±=Ñ¸Aõóð¨Z\x0011oI.\x0001
\x001e¯Rj­~E7dñ:/ÍçdìÈÅàFÓhÏ\ÿ\x0000cehÕ\x0019r\ÉG\µ\x000bøöç¯ ~Ü\x0005ÿáG\x0001ïe+\x0015\x0003í1Öf\x00135£\x000bM\x0007|\x001clöo·w¯.¥Ï}Â\x0018}÷ ¹\x000f]|)Í/ú|éñ$\x0006E¹·æß;Óê"HÔë¾;|8Ü\´¾Ègål9µÊ&t\x0012^Lz*µþ\x0015F,$¬/Ú[ó©Ï\x001ddÿÍb\x0013m\x0005¡Í~yóîðj$ø>÷1­èÿ\x0015Ó­]öÖ}W}ª\x000cÃ\êÚá}AÒÁ2î½%üÜEêënn_\x001eËp5ã\x0013&¶ª`f9ñºäáÙïé_èñqVåmO\x000füÉR³õ[Ú\/þÊ*óE¯æ±¥sF\x001fm$_ôÃË\x000eoÿÛ»r\x0014¾\x000eöoH\x00177\x001báO·77·^>S\x0014Á÷N
îøÉ.Ç£,\x0005ÔnóÐèsKd\x001eYÈÆ¢o\x001e^\x001f\x0016=yÿì\x000f·\x000f\x001d¯ìÒ0©Ûâ$
\x0013ã±,0'Ï\x001eé6ÂÑ ZãóHC¥F¿½»}øû³Wd=~}óì÷Ww¿ùÝýî
}gszÉ©HdÏ¥×1.\x0015ÔG$QôþööíÛ«\x000fW¿Y0ç	"dÓëVIkÔb9\½Ý\x0006\x0007r¨FÔæO)\x0007+/
9o\x000f7ÛüÁßüéöåO:\x0017¶s:óUq«Èãco}æ(XÄ:§GÈãgØÐ?##ë2º#R<ÉUk
w\x000eäñtâS\x0012\x0015]\x0014hI~R8q@¾#IüéêÅíÃÍý\x0005ïó¶ÈWÅ42÷&ì³\x0015\x0003<
sx\x0011Qôüêcí?ËèÞ\x001fþØqrÝ1@K÷fk¥knkî=\x001düÕôtZ©!laÞ.ÙûÓªÌ_®½?ÇEü÷\x001a\Î%àçþðó«×¿ØWð"ü'$N\x0002	g>Þvã7´tË56æjcM!Ïùñý£ÉOïòG¢B]2\x0010\x0017â\x0015^\x0000É+\x000er\x00128lNð±+Ë¾SÌ¯\x001d¾ý§\x000eo{_\x0011Ãç^]½À\x0007\x0014¥ÓÃì\x000f¯ê¿ßtòÄ¿Ür	öoÙ^²Ì#$	3¶éÿ·?Îù:\x001bu©# ]0*\x0006²»ì<\x0008ýÁ¿|øñ\x001d^£»«\x001f¼nó=/òJðØZ¡\x0019K.éXv#³\x001ccP¤\²·ØxòYoÒ"\x001c¼I¼â¾\W[<Q|jOö´O%¶Êª°\x0007\x001d¶\x001cCç-\x0013ß\x0011{\x0000w\x0015åè4\x001dýáGó÷Ûw8ºîû«ë»Ëí'¹)\x0004y°	Ý¬fk\x000f±<.:·:úÏrôv.¢QqgÁ'?v\x0010zºûPß¾B¿Fv×Å42 ¤V¤fýÂC£»óNJ\x0002«Ù>§À\x0017± ÀwÖ{êK\x0007qç»\x0017éND\x0011ÿíü\x001eÝÙ|¶°uÁË×*W»ê«bBñÏ»Ïaèô\x0004\x000f?\x0019YìApF	|\x0011\x000ck-\x0013GK&5RSomËÛç\x0014Á«)>µ¬Ó/¿@w\x001bz$\x001d»@jê\x000fMb¼A\x0003·Ç?8­\x0010\x0005x\x0000ðT¸cïi]Ñ\x0013î_Úpâ>zìèÎöô;¡\x0007·MðièÙâ9h\x0015[AMÙ\x0001ðÔ¥^C@àÜC\x000fà¾ÔsZ
+\x0014c\x0015 çûKÁè´§¥Jt«ÐC\x001a¯Ñ!þíï÷¢¡åÏW¯\x001f.öH\x0000×Ð\x0007\x001c\x001d­ÅØ\x0013	Æef\x001d|¼kx\x0019µ\x0008e°§\x000b>ù±¸ÿöïÙ¼üù«O¨Ø<Ó\x00035¾@7°Ù¸ÀfYÐf[°â3YAì²Y\x00189\x0015Î9ÇnàúÔIYê¤·¤ïYÈØòcRÂ\x0014%¹¥ôôä\x000e\x001fBê)m\x0016'©
xù£\x001d8È8l_&>wW÷/~yI«züT\x001f77À¦­\x0012ªEïëlmÈö£\Åxð.eOel_¯ä\x0018]?5à§N\x0006=
dÿÕ®$J'ò\x000b±\x0015Êé·bC\x001c«e4û\x0019\x0019,sB6erTvø|\x000eww×/\x000f¯.uV²Iê	\x001aH%y¸Rëô×_ù°\x0004ÓÚ1>~X\x0014\x000f­7§cÖÙX¯ò[\x001d~ªÍeà	\x0013À=`Q¸)Ù
`÷\*ô,jd\x0017àF
:\x001eBE\x0012DÀ¾\x0017Èµãí\x0019ÐVNê¨é\x0019T\x001cA¼u¶\x001dgqo\x000cÂè{Ó
A´±²!§¯ä¡(U\x001c%-\x000f\x0014ÞÐHaÊ\x001er\x0011Û\x00177òýU»"m­J·â\x0015­¿ÐV<\x000e\y(¤õº\x00046Ü¼\x0002Y\x001e
\x0003j$ÔNC°¹qÜy\x0007\x0017\x000e\x0000Ý\x001dü\x0006,BW\x0005G.Z\x0001-E½\x000cYÝ\x0004âZÕ\x0010uPÇ#'Ý" ¡\x0001h+¡ÞE_Ôã4þ) ¬¹¤$Áã\x0002±>)g£BäU\x0014£B&×1<'oãh·Ñ\x001e\x0008\x001eYowûæêíåôv
\x0016ÄX]¨Û\x0003ÄåêÝk®FQöýJzÛ¦ð	a2\x0016~ä]§Fåõ:ßiÕÛ·Âú<N#\x0010°ÛqaC{sªx7smÉza\x0001{ØÍ:!k\x0017À¡\x0003Ó\x00028&Åu¾\x0006ì\x0010¹¶5\x0013Ë!jËá\x000cA*{M}½v±·õÆ^ÝÖkQýUÓÆxhßrCÎZð¨VØÒ\x0017l²¥ÿÎ\x0019S\x000bnãr'/Á\x0002Ý_lj}îRejyXqEõDÇÏ\x0015Ú	è\x0008¯úÎ|× K\x0001õT­p©\x000bè~âÈáßZFÚ¶©	½jËÐÒ%¡\x0010ï
®\x000c½$ê;²©j\x0013Ãº^<\\x0002dg;\x0015ï\x0002\x001d\x0011¹Í=\x001d\x0002&\x001br·AxøY\x0011
cV`»'u\x0001Ãbéí\x001d=×_ÆJÙEsÇ4\x0015JT«©0{cN¾1g\ñ©Â5¥îú×?ß=¼¸¹þùáb®¤hvhJ2%×w¡@%X\x0008M¿þÚ¾dÊì¡|ü©Ú=¨g\x0014æeynacsÆ/mÖÔxÎ«ö\x000eZ\x0018S¨×\x0018\x001a\x0001¦8\x0018i!;7NÝªÝ\x0003F.BYyßÛ
Wd\sL#¨@>ª\x0007
\x001b]3\x0011:r©¸ï¹Vt³c~\x0014\x0008R|Ä\x0013\x0019Jo [¤m\x0015¾Ñ¶\x000c³°¥6nÇÃÍáúndº;3\x0010f7ºÙbr1
m@ÿi!\x0017ÿÕ-)?«ÿ\x001fbÎÚä¡+izQ\x0016²³2³ÎÏHLÓ¸\x0002÷h	¹\x001aâÙ¬)® ²ÃB\ÚóöûÓætE¸|î9¬8E\x00046s?uÅíFvc¸l[·Gh\x0002®kÖßøB¬ÀÝ8qäà\x0018×Sì\x00131\x0016QÀÑ®$ã6#.\x000eÅ\x0011\x000bxû\x000f½F0È\x0016±½Ã²*¡'Ó¤ÖtnFý×°\x0013Tç=)êX°eIÇ¹Ø{2qIØ[wxüºÃÞºÃ\x0005Ö÷°óã±gêûx#ÁJaÖ9'\x000e¹+\x00101¡Û\x0013
^\x001föÞ£Â\x001f0Q\x00047*OÝvIþ\x0003_þB\x0005IãØóÝíûëûû+ò¶ß?»¹zöííÍí\x0017×WwÊä\x0008_n|	úeïÐ?ÊÇ¦íçÂ\x001bóIwT\x0016Q[o.Jå<¡Ão\x0005k´Ì-¢hô3ÄeÏ\x001d|,ô7K@Üº\x0013/Ê Ê6z©{yk\x0001>B=\x0000=p~ú
­ÀÂ¥Oaã c`&È 	ÇÑ6\x0012¤ÑÒÚÒ²d\x0016§(\x000eºo\x0014\x0017\x001d9\x0014uÐó8ÄZ \x000b·6ßu]0ð3Ñ©[¿"w·í".çZ\x000e(Ö¬ìØ\·ññ*ÆK'#o\x001d§L§«p4pÉ©\x0019(u\x000f¸%ç\x000e¢\x0001;TÆW\rjÃè&!¨ÇlfKK×r\x0016¬\x0007\x000bt²ãÐ8\x0001-. Y%®\x001b?¦Vë+VÖYÇíÝA+MÁ$âô¼((q<\x0001B­:Cã\x0004´¸¤×¼\x0015«^fÄU'ÜÅeþî$Ð\x0011UÌã/x>R'#[V\x001dÕ\x0001iÄ\x001bvï"Zq\x0011c\x0006Û¸ºÎfßVÐ\x000f £5¡\x000f@§G¯zï*Zq\x0015Wor\x000eJE'\x0013Õqó$@TI¶jaÓ²×'\x0004û9L^¦Æí]\x0019'¯Û
àU}®Ã^\x0010åøhõÀêZ¤F*é{1\x0013PëXÐBjÉ5Ôp±ðõ*.¶Þ ÊúZÆôLcjùb¢ô86×ËhOÚ-úT,Å+)ïäËq\x0002/w\x0014v*\x0016$
\x0018\x0011+¦`F±øq°@Î\x00029µÉà\x001brÒÈ*¡SÚ;6>7+r\x0005ä("3YÐì,È\x0018©rÝ\x0013³\x0015b&Ë[Æê\x0006®*VoÜ\m¯È"\x0014j£\x0001ÜâÓ¦e÷Å\x000eªÐ¦i.ñ,>íUª²QSr\x0017"DM\x0005\x0003ö\x0012µu®¶Wè\x0008«®rÕA	Äb]Oµv®µWäôèEï\x001d<+\x000e^4p<jé\x0014lë¢1Ë`\x0017­½wò¬8yQªVZµ\x0001KGRÎâõ{'ÏY@Àb"û
¬ódÒ§@\x0016'^/âõQWÄØâH-B:\x0014fnÐâx$»uº7_£tn\x0006
å¹|]\x0006þ2@Î\án\x001d\x0002\x0019è>µÞ\äÌ¥û\x000cÉ\x0013WÍÚå8¼-'NoU©ZëST 3_ý¤\x0010}ÕoÐ¥Bv÷&\x000fzÕ\x0013'\x0005²\x0008Ò³K#/.ÛÏW®èë²M1\x000fÒW\x001d¤çú.+\x00186Ç\x0005\x000fµÕRZµâPp^syü²RÑ5'¬Ò¨;Ñ	ÎKþ9¯8\x0003n\x000czÅãHp\x0001,Tª÷ÏE\x0005O±àÎÐ\x0012rc\x0013\x001c/cÅà|\x0013~\x0010rªü\x0004y´Wä\x0002G®+RÐ?§#gÑ4f5.«X³ka±frP\x0005©µ5ÑM<Ò\x0005Y3U[¤éXJP0Ù«üøl¹\x00165t%o½yë¢±2È\x0007u\x0003ëN©TÅ1æ¼ê*óÁ¼j\x000f{*pvnÚT\x001ccÎ«\x000e- E«6e&ë½K(M\x001b®+ÆUG\x0014µ²Ç[6\x0015§ó¢mëú\x00165;­Ú\x0018e³"kÈU³\x0012yÑªbÑ¦ªEïø£\x0015ç£syWØ¸ëîÈJq-ÒÃEÇ¸\x0016ÅE´\x0016÷0©"½¤+3üd>º\x001671û­¥º-Ú+\x0015m3>¡µ¼§»@r7.®
òg,
MÊ\x001c3!ÍÍ±×¹ÚÍ<\x0017\x001a/\x0008ºÚ¥f\x0011\x0016ç|ï\x001eÊ2:6¡=ø\x0001±brJÐKñßÞ=\x0014\x001eJe\x001a02Äe§x¦ ÓÐß³AËjÈ"
=^µºâÊ<59ÏmÈãâ	ÌS¨áô¬Nµ¨U/æéÞM\x0014*|õd\x0004­\x001a2ø¤¨ÕMÜ«TY¡E
g1"vØ ±Ä×E½V\x0013àJh/k8!4ÁV$øúË\sð\x0014\x0007ZÆ\x001aÎ$îKuªFÛêÃ×\x001er¿wB¼8!É¹D&C\x0000h\x0013TýU#aö{ÛèeÑsØ~V
O¹*¢'ÕÔD½·^ì"]\x0011#v"8¡<\x0016\x0016Î^nÇÚOSyG`QkFÂ¦q3§{\x0019Þ_ÝíÿÀûOë\x0015á¦Ü\x0013]ùºnV6kDæ/õë·¯G¾Ôs\x000bfª±G7®Éª\x001b\x001d\x000b×÷\x0012÷§éù¸\x0014>­+Æ8í&Ñ\x0003»Äy.µ<è%@1F).\x0003Ñ\x0005°0ÑJ\x0012oN®÷±%*+Û-Ú{À²ÉÁ1'\x0007\x0004\x0003"I\x001ds×|ñÖ¯È\x0001\x000b¬Y×\x0002ª%Ï¤\x0015X8ItE¯7·ñ@eÿP|åzI+rO\x0017ÐVn\x001cÝÇ%3·®k\x001e­³\x0015YÖã\x0006YkBa¡§NFk(\x0019õÔ,¬3>c^ Ç\x0015kÖÈnê%­À=qGÃs¹}þy"Qõ\x001e\x0014gÊÜKZe©¯IÏ=HÙ	JÊnî$­È¢`=Øf×lú¢b0¡:<svIoì]@YCL.\x00127}\x0002\x0007â((\x000eÓê¬&>Ò
-\x001aÞBF0+¹NZA\x000eÜ°\x0000-ÊÉGÇ®Tu»k
dï\x0016¬\x001d¯Z\x0014ñóª¡M¯:½è8wVdq\x000bÉÌ+BÔY½¼$\x000f<\x001f¦uºO¤\x0015Z\Ã¤¹I«*h\x000câ\x0017\x001bv¼¤\x0015º\x001b\x001ee\x0010åaðûª w¼¤\x0015ZÜÄhD U¤½j×akxI\x000b´,2\x000fVzI9W´U«Síh«\x0019¼w\x0017¸d1¹\x00027\x0006*Y«òfÖ\x001b3qVhq\x00199\x0015#4\x0008\x0013
<p\x0013W×nï*:q\x0015É\x0014Ýy,\x000e\x0007åüÑª5¹´"È\x001cB3eõ\x001aVï³Z´{I+´¸ì
AgÓ§b.Fä¹´Âk\x0018ñ®0,¨¥\x001eô{´âÂ
q³ª®I=²¦MÁ¸G\x000b´\x0017§9WNH«Ú7oÅw\x0013ïhE\x0016'®\x0008³ (Þ^\£iÖüh2ªì"ª§\x0011¦Ì;õÔ.³^Ìþ\x000f8½
¤RE\x0008U*6×¸¨¾`INË\x0006o#þ­¢\x001c¢½4Ð0ËVõÒ´;yâ\x0013<þ\x0000¹¾Ñ:IxlÔÞZ3ëÐÈ*ëÃ}þä,\*åã ²«0*zñ¬¹Üâ$¿¶/ã¢ù$_&ë\x000fG£\Æû}\x000c\x0019å%²?©Õ)\x001f\x0018¹§\x0011I^u*4/CÌ:åÃ±I\x0011¹Í¡¨\x001eW
uyáÇTÃë\x000fÇ\x000fA\x001bFLÂ\x0012²z\x0019º3Yç|Z7±xsS}á	Î1íTÚë¤\x000fGCÀrhXf¯\x001fÊv)G;*\x000fY\x000cÁ¢luG¸
qåhæîLÖYÖ\x0003O­Y¹3ËG+*\x000fY\x001f:fÂ`M\erFid·ãÏdõi
¬bÍ1¢jÊnos·#ëÔ\x000c/ZZ:t ½ÅEOÎóÄ5È:}ÂMýA\x001c»`0>î0TA\x001báçö{ÖI²Ú6Gd_tü\x0013¾û½³¡ãE¬"[¯Ò®\x0016-\x0007ÖNs|ÖÙ\x0002¦]Òàt\x0008\x0014\x0015ôQ;Æj\x001e¢ú\x0004N2:}b\x001dêÑ¥ebTæ!ôNÐòH\x0017l¤\x001eWí§4±þò\x0010\x001fO`bÓ\x0003ÜÇÏ­ÐxòìHbH°óÉ\ÿëîÍÕááRonVî`\x0008y3¬Ý&ÿØ(%>AÃ½/FqîÏR½æEÂÃëî?]\x0017\x0017ã<¸"\x0000"¹ë"qÀI+\x0008\x0004\x0018TQ%Í;!3N\x0012c\+½¼Â\x001d¿PdTaHlaòÉáN:~H_6*\x0006¨
æI\x0008¸íi^÷¿âð¡÷ÍéßV¬­jU\x0002ÏÌÛùWdYdáZl[rRoªÃ,óªÿ\x0015W\x0014<ñø\x0002\x0011£]\x0000D%NÞÙy?ÿ5\x00162ãÈÏ*ëQk®;¯mR¯m%å,\x000frêhr\x0007\x0016ÕÙkÔk[]\x0000ip,\x0000\x0013ÿX³Fk.óðá
-®2ßk\x0002cVÉ°÷'õsÕ¼ÙãªUÐ:íÅ\x000fWhYçÀÌ«NàD\x0015´u'\x0014·B'\x0010àW*ÁbM#	Du¡/Í\x001b{GOV\x0015Hâ\x000bº}Z\x001d\x001dÚ\x0005\x0017òþ\x0006{¼\x0007ªsÖtsËüÁ½=ü|.há>\x001cjLcÒ\x001eÛ<é\x0005°C÷|\x0000^ó{\x001b(qÎµJ¶ªì\x0010ñ%ì´·2Í]\x0013h~>*¸h\x0015µðãW	-ÓÜ\x000c-3<þ#Ð®î\x0004rVhµ2­¡è¶IÔjÂN(ó4÷
-71«´Çê¬Gvå^\x0013 \x0007yÃ½r\x0011ºd¼Ïët[ÅÃ³o\x000f¯î.ÆÎ\x0003Z²ÌAÖ?\x0001y
¸
ì	8)j[ð	uCSqP(Î£\x0002P(¢ìw8ë¼¶Ä\x000cÔ³$Ð=*þÙ\x0018c&u^\x0007?xÄ 0lx	Þ\x001aEðµSîº\x0002Ë]dIòXoM§O5k4J	\x0019n0)ä°$)äænöªÒ.·%OÈð¼\x000e}ð\x0015\x0011KNÍÌ9qRãXÉêÎ\x0015OÈÚÀX«ðZq\x0007>V`\x000c|@µ²ÃrF\x001d÷¨­v´Ä¬îÑ%IÇñ¼²ñÊâO(å¼\x000e|\x00144\x001fSÖÐªè°LøIº²WüH&òo»\x0017<\x000bé2ºÉù\x0004Ó\x000bÈøN\x001b÷ªç~»n$ú\x000bOÀv\x001fKÄuw83h\x0014±ÞºÔ¹oßÊ],\x0018¬X8\x0000ö{Ù\x0005\x0004	\x0017		2Î*¢=ú\x0007óbü¬\x001bÄ\x001dÝmæè[ª°f\x000c\x0018ºyIÖýá.&y\x0004S±pÓ\x001d3ÿ#p;Ý\x0013?Q÷»êeÜ&Ñá¬aÎyt@³)ó2¬ûÃ]*¡Äo¡sÈíÍN_]Öýá_-¹ææuàà\x0015pËN=Ý\x001e~æ'¢î\x000f'í#½´\x0014×và¨BXkíùÄÔíá\x001fÚnû&î¢r 
|hÓ2|æ(êöp\x001eñ!êÒR\x000cPüà\ÆlnªiÏÓ=Ü;Ï¤#¼\x0003Ì\x001f¢\x0016\x001dv\x001aö²î³ö\x0001üÄ\x0014*v;ÕiÃ}\x0001óº¬¡=?â\x0016\x0006¬«pÞâCÀfø¨¡=¶wdÅ1Î\x001bäîcºñyYÅ,NÞú\mØ«ìSÐíÏPÝf½ó¢|æe\x0015+´8z¹È:\x0014<2\x0013x\x000e\x000c\x0017öîø·ÆõìUïjQXáé%©\x0016V
ç#¤¨wjÄWdqªùõK¸hGÄdâqÑ{GOT*ä\x0014$_8=\x001dPÙîQI®fÎ\x001c\\x000en\x0006_- ð	ªJ-=çÖ s\x000bý}#\x0012Q¤þ¥(ta®­ütæÛ\x001aôm3QûcÅ\x0001r¥ª$Fmé¢skÐ¹Í.\x0012Ö\x000cWWTyÃkP¯u³vN;e÷ýö§Ã»ËÍ\x0019«tÛÆ\x0003r\x000fp\x0014·_=OãdqûÊ²ô_©*\x001aÃÜ´ÜKMdÑ¹u@^Á¥&è8û¥n~\x000fY\x0014gE\x0003\x000c±Ük§Êà\x0014Y¸ßqp5o°	¹-rC60 U{¤Osâ`;\x0010\x0007Ñ!\x001a¬ùP@Ù@\x0015ó¾×\x00035'\x0019²;¥[Ç\x0013¯Ò)dß\x0002\x0014\x0013\x0017wà\x000e¦Ë-ò·m´\x0003¬y\x0019Î=\M\x001el\x0012öq{.Àf¼ç~§s\x0005\x0016õ©B\x0007E\x001fÀÖ¨ºÈ|Úã§\x001fX\x0013z¸lRÂÉª¢xDNlÈ\x0015Z\@®kÍ°ª I\x0005?¼ßer;ÞB¬òPhWll\x001e(YFü`Æit.ÊL¯~}ÿòúbÎ¹A»y{ß­Ö0ÉÂÆvÎ³µ|Ï`À\x001bU\x001aãÊ6}E\x0016Îy)²]]`o#s\x0015ß`gæuE\x0016Î97ci\x0007ï\x000e	xÍ;$¢E»ç\ê`Íò\x000cÒ±ð0/]\x0004\x0013»¯(ÍÊÞèhä5+çN\x0001ïÌÑX\x0000Ò»-\x0019hDÃ\x0010Q+Ö\x0015Yzç`!ð÷~ðu5O,Õ¢T+Oñ°d\x0007'#ù:9\x0019\x0013\x001f©hï\x001e,\x0011SnKFd«Oój] ¥{\x001e\x000cTÐ¢
xþ¥êã¼£ZWhéGð6¸\x0003\x0013¶0[}8v(ÖVhtÏSë]à@\x0017\x0015\x0015rKb{ï®f
\x001f,Èz­\x000b\x0014þ¹UÇ£Q¦Ì\ÿ¢]f$D¥\x0004deÞèE7cJ\x001aº*\x000f$
Í0
j<ÙÊÿo?0¼5¶©QLPýùýÅFs8²Ðu'rg\x0008
\x0001)=jc[øµóSåS\x0006Ø²`Ô+cI\x0017\x000e¹8£Gòhg¯Ì\x0011YÐ\x0013FèT«ä\x0018 -&ºÓ5,ùÑ=`INmó\x0006\x001dù±ªìÆO)BÀGût`Îè"õ(¾\x0004uáÖ\x001e^#°äñôN\Ü$
V\x0002®Ø \x001bÌt Ò\x0011X\x0010ü1i·qDn$Çl¼ÝÌZ7q 
_´²¥¬	\x000f\x000fÁW·º?3-·\x0003øä0I\x0017_y\x0018´\x00125ùF\x000eÝ\x001bZ\x0017¿»÷+\x001dÓ³KÒ1ETú­Kèµâùd'àûûTÏ½è&c>ájRJnªFý2½úG`Îò¼\x000fsR2ø2ç»\x001aEw\x0019·%#\x0003\x0000\x0016V©\x0014rµ­çgBp7t\x0019$\x0013\x0013üÿ"±EÄ\x0019\x000fÕÙy`ÑmÆ\t!bÚÌ'õâJ­ì8îE5\x0019·*9\x0004Ç\x001dbþ\x001fëDH\x0003»©}YT1¯\x0018aUqS°s^ý2t\x0018\x001b\x0018ÿÆõwª¾L#yqQ-ÆK1PSÎaS\\x000eÎb×q/ªÇ¸¨bõ\x0018"*
\x0018ÊNqQ=Æ¼h\x0001ëTÅu@O¶.ý£{WD2%Õ\x0008ãg¸Þ\x0015Ë\x0014IF3Þõ4ÖøüñöáæúB5>Î\x0017^\x0008f³¡\x000fq$½ôës5ì\x000cÕ\x001e÷1©
\x001c¼µá±ºfØ÷0¼¢ÄI¡Õ¯z4©
\x001cèÂ.ÒH;\x000b>Oh8¤\x0010æÚ.©J\x001cB\x000es3²­\x0013\x0000\x0019Óèi©\x0014\x001cµRR\x00053´wEöVÄTö\x001d_äã<uTaKCN\x0000\x000c\x001e¤/H\x000fDÀ;ÀI,tH\x001bn@\x001bÊWÌUù0k\x0007tèÖýÇþîíËÛK\x0011ðð\x0017´æú¨&îÂ\x0011)&\x001e^þ\x00143´?Íí é(Ó\x000cEA#Èdª\x0010sÎ\x0005ãD5ÍC[N¶Z»è bOÔ\x0015ÙN%\x000bwzc
@%òeÌ¥&cy*8"·Lýxc\x0013µ6'iÄ§¤x¯lñ
yú;\x0015&JmT©2ÆÌ,ÓURû;\x0015&J\/8\x0004W\x0016j£S6ê¤ú9Ë¿Sq¢Ä=	\x001f´½^°f,§sæó\x000b²ìsV\x0012LÒ<²)*rB\x001eµ5^t/.ú\x001fî\x000eo_Ñ-ÿÓå¦±\x0019M\x0012¶ÊWîcòüÒB%_Ju\x001fîxNÐÛÉÁ`èèQe3Åæùô\x0011?Ürá\x00020µ\x0002^ÄâÊ41ZN^E¯¹¶F\x0012Õ\x00145\ºxU=oê|¨\x001ft\x00073
`§È\x001aÕô8»3MÔ«Ð5-8J\x0002#îN¸bUiÒ¼²ÌkÄýn¢ù!\x0017¯\x0014´\x001a¥gí<tíµNª	&«rû3è¤â\x0014\x0015¼iìÖ£NòZ'±£"1JÂ>TU4o[\x0016sÔH^k¤F-DA\x0004­ÑÍ{MB^\x0005	\x0018b©\x000c\x000c½ÏÌ\x0019Èí OÂ´^iIU@;«C+Fõ\x0008ÚÎ+´Vh±¾9:
\x001a©\x0015"Aûy\x001dÕ
]åµ9R&
À*îöÏ(`OÖùÜ%àË8\x001a¯ êºo¾ò¤"i\x0016Z«ydCPÏwVYnãw¨ÏWh±Vai÷\x001b+üb\x00192í5p¯Ðb\x001b¹4\x0001(8Ìj¾jY¹6÷vÑ]4\x0005\x001aïÕÄ\x001bVfÉ\x0011ìí¢· <dy+ÿ?yï²cÙqdþJs\x0005üý¸3êVCR³UB
n£ADf!eF\x0019,ö'ôôóû\x0007üþkæûeË¶íÈì8'#\x0013]
´PU"WøñínneË¼IPf)\x000fâa<úQÚþ\x0004Ý^!)«\x0000Ó¸'kÔD¾bVZR
:r \x001aê8·)G_0V0þRp/D<w´bÅ\x0008ø1G0vù\x0010\x0002ÀÁªI4\x000e}tôýô\x0008Pû¢{\x001cÐô\x001ftôùR<\x0011Ù\x0014ÖYü\x0018\x0014Ö© \x0015ÈøÚQúgV]jb«íòÔÿtyw®Ê/XS.%¯Cã)!b	*ðGOO÷\x000fëaª\x0010À"Í\x001d¹Àôð*ª¸³G\x0005DÕÃÎ¥wyuJ\x000f \x001c¼ê°«ÑÙ\x0004°¨zÍ\x0007²¬Ì³¸:\x00007Åp¶VeTÍæÞl¸2wËÍ@gegmWO53[\x0000x¯\x0015õ\x0019iÍ8(Ù¾j7¯!Á\x000c§â°ß+x%b_Ä]¢j7gJµ\x0014*¬Î\x0000\x001f0#g­Ì£Ïö¹ ¨ºÂb.sn]÷\x0004Ð¨ÑE¡îA\x0004\x001aUë6S%\x0003y'8\x00087\x0018»a\x0014üg`9a×K§:Ó©ë°\x001d\x0005ë-eª\x0004\x0018ÛQ5n?\x001aúè#
B>^\x0016µþT½Åh\x0001zòÉ|º<Üo/O[¸!Z´Å~ûìË»w×o/oÎÖ£\x000b¦Z^z]ui\x0013Æ«¾zÛÓ Ân³Ã\x0014]Ò60I\x001cg\x000eLÒú¨,k;ÈìÍÈâòx¨DW(\x0013û¨\x0018-¹Ù1ÿ\x000c+\x0018kLJ±ySSjè<{öS0#'°«\x00129Gl8!»ª¶"ÛÄ²\x0019YZlÜdÕø»·Ø=Ú\x0015º\x0019¹Áó%Xv©ð`¢´>¨?è¡¥Y
RÆý'\±ü\x0010¶ôt6ªÁ²Ã\x0002A+¹Ô\x0018\x000efÍÐ	 E2¹¹ä\x0007Fç}ª8ÂíËñ@¶Ó#Î´­¤8ß\x0016Þd#0\x000bs5Ü\x0019EÖªÉ¢í:à?¿ùþòíÛÅmýÃíÝõåò<µK¬¥;Ïé¦¥Á@êìð\x0014®'éø'\x0017þF\U]\x000ftÑ	íè1V\x000c\x0006¨t§æ\x0001ûÿªë\x0014°?ýEI%{`ËðxdÓku=Ðy9 þE§d:È÷ò4ïd³`u=p\x000cZcÀ½ÐØ f§ \x001f­j&ác\x0017méÕ¨É¶ã¦©sá4h#¬f(yuóòòîÍÕÝõÙ"J§rÈ©¯\x0011%ÏMR\x0003ôâÅ\x001fQÆ2ÆH}@DYÕÍ¤\x000b\x0002ÃçB\x001d*ñ[fKö\x0007\x0015ªn&ùîëÍé#(]Ýí¢­D:#\x000b\x0007§ÆFØcô¨¼l±%3f\\x0011P2·@i\x0010A¿»RE\x0016lD}UG}\x001eæ5r^ÊÃ[¯'u%~Ò\x001c\x001eïË÷ÛË{zÎUNWìi\x000eÜy\x0015¢\x001d{/K¯HSB\x000ecö¡h\x0001ª\x0014û îSÇx¸ÖhË"4%PJ%*g^Èn«tÿÔ\x0015kÐâ,Â\x0010v \WÀä6¶-ñ%³qJ\x0016aTd)ka¾\x0019è:)ã\x0018Ä8% gñ±@zA	Ê§÷vãESº\x0008^ § ä¦ôµêo¡gÂæÆ)]Áº5{5ÏM5µÓ\x001f\x000f¸qJ\x0018a¤ú¥ÿ;08Õ¯\x000eG?\x0010FhJ\x0018a0i\x001aU{Äh©7\x0002\x0019\x0019edQ¥85-)c·öÑãbQïäÂ !:¹ÕzÒdÒ\x001fq\x001apwt\x000f=juY,ÜÇT¥±qY¬ñËJÍa\x000c±Ì\x0018§V¤Ôzõ\x0011Gf1ï³0Ë\x0015ß²0	ã\x00104UG.MÙàÁ\x0004ÎÏÁ7ì%\x000fCÜL¬\GØÑô¤DóÍëË\x0017/õ[2ægëM¤hBéÁù6Î
É²ºÆ	ý4GÃÛÙ)EfÖ®¦=\x0007%¡\x001fó\x0001SB+\x0011ôrAÕ\x0013»»
¹GjÃHdj!/Þc`£D¬¥6¯\x001bp4ZpçÌsYAz~ù,,bä¢µ,ÖÂQ\x0012,\x000cjÉ|\x000e9\x0018C4C£¯Ô©æ\x001e1Ø\x000e§eè»I{ÔéQV\x0002|óýõÍ«3\x001fQ§\ß:zÇÉAÓ ôOã¥\x0019\x000c4ÂÕ\x0006;=Ì }\x0011\x0003ºò5\x0005³siA\x0016\x001dó£¾\\x001bò¥dL\x0019¢\x001e%\x001aìTcÐ©ÆX`\x0018,sT Ù*zT­½Ût S±\x0004x\x0019Z\x0006'õÙN6agF\x0016­¦9É^&dH©{Ú\x000c=e%\x001d\x0010Îbª\x0013×\x001c9òiÕÒ\x0003\x0007cgh\x000f«îF\x0012v«V4pàÌÐ¢Õ4+\x001aG©èT\x00089Kcí\x0019ZöFPÒ'/\x0005J|Ñ%%t<ñ5HÁÐÿY¶1-\x00165¢âÛN<#\x0017;!W¸-bÒ\x001dË<ÈIw´h-,m\x0006ÓÜO¼\x0006iB\x000ex<ädT±N\x0011]Æ®ãù2\x0008L3´<\x001eýBL%jYõøE¯¥('ñ=±,\x001c2ÑQ&\x001arV»íUÎ§%Ë£[üî}õËÏ¯ÏæBbqÙ$gGÚHê{q¤ú\x0004Üzn¦ü E\x001eÕ×÷Ø\x0012¶¡£ÚïFMKJ\x0019ÎSUeå	wq\x0012³5sTû\x001dÏ¾£ã\x000b÷B1X)Gp_gðªý2@0§Qbí	ë93sôOÏ¢³ÀtNØf± ß\x0007Õ\x0010ÎÑC>9ç'»ìSAå\x0008¯:\x0002(\x00122F¯Gqúê\x0005\x0011W,UØk8¤Vl?1^ä>a1~¬\x0018{§ÖË½G\x0004,oL6cÑ\x00029l\x000c'.Ý+±ãB¿ÕêjSiÅß_¾»}öëÛsõèÐ\x0016*±¤´ZF5uu\x001eÚÅÇ\x0017ý`áê¢Åa}FY!N×É\x001fZ´üV·'\x0014­
ë°\x0017í\x0003\x0008Û¸~S²HÑ\x001a®Üg\x001f°\x0016,S\x0019j\x0012Ñ\	Þ¢\x0015\}É(ë\x0015PðÒ©ì\x000by\x000c¶
)ZÁÕç%fÝ__k\x0016\x000f4bVpõäö:ùù\x001cúNµËµXìbÑB«~/¾®¹(\x0005^í©N1ºá\x0004\x0017-ê»4mnhQµU°
TÑj¨¾«É\x0019\x0008dRõ'ô\x0007r¨EË¡\x0006×1\x001b\x0012`È@ð¡)\x001f¸[¦É\x0019\x0005½ÿõßÿç7/®¯nÎ*_â\x001dòCÈÑ\x0010¾N\x0014\x001c5ÎÑ·'¨µ§úsÒw\x0015½Öä»ÃYô\x0004$\x001bb ýH$Ëí*z½fSñWù¢î\x000fºfdtu\x001c@(\x0017
=\x001d|{²iZâi×wWçzÈØÃeÔõ\x0006þÉ\x0018ô\x0004LbÏÇô\x0003\x000eß½d\x0001\x0006%´%TrNO¶5*gdÉèlÊå!\x0014PWzY=d[æ|F\x0016öªx©<5DýaÍ\x0015Ô>ù5WÇ/àcÆç¯'¥\x0006¬òx^óÅ3Y\x001c´Õ"2±È5Â=¥\x0019\x000cÂW¯äÁy{ð¬Ú7¯³Pä|H­¬ôêê¸Î\x0007\x00143ðöHåVn\x0006\x0002øÚQì9\x001dTÝæÿzgU\x001egnëÅÝè\x0018Þõ\x0012\x000fªnóÈ¬¿8\x001a©cDÃ"D\x001eåM¦ç1ß\#ç³dÇ°VWVÃI;\x0005'öÓ>ÿÈ_°&B£PbR=ß%\x001dôÑÍÿ!µ\x0001àÂ­ )\x001cT£\x0000­ú@é|þ\x000fê\x0001\x000eHd\x001a\x000fÞk8HAÍÿ!ÅÈQd\x000bWÅ[&$XØý.\x0007\x0005ÕoöÉñy·êýËÄËõõwWo®oÆãõõí=Ùú×g\x0013KHð>gP\x0017ÞÒ\x0018p³n=ù8y\x0004:K¹-©Wfð\x00196\x00128ý\x00125*¦@Òþ{oËu&õÈêì&\x0001ß=Ë® é\x0000,	ý\x0003¶ÚNEÞ_É¤\x001eÑ¸(¹O\x0019ç\x0001ªÏî³Ý­2\x0003×\x0013
«U-ó\x0008\x0005ì5=ò'¢­\x000bFÚ».ùÛgº~ýúêþ\wk.ØqÁ<Û­\#'Ä0¾ïg"ÊC£s d«ä\x0011ö²!(ë^çLoA\x0016/Y ëÊêáh\x0005«ÚÄd^Ç\x0005YdW\x000bLgã5Ã\x001c$iÎÛ,®\x0005YÔ\x0007[Ç¯W0{\x0016\x0012\x0012ªÞ¼\x000b²x!Y	D\x0000;%ËÛ¢Úbú|\x000b°¨<6/ëõÛ[¡à\x001c~Àb\x0016¨Ó®gDÕÿ÷í÷t\x0004ÏT<ð-j
Õ\x001a+^\x001d\x0012èÊø\x001d0OR
<´\Èðso	ð/TËCíÁÖ²JI?b\x0019º9éÿ\x0012mÍcé`®$\x001boMÒoM)PVÏ\x0005]ZTÒÂ­ÚÜõ¤ªß\x0003YLAbd µ¨?»]üNªøM»\x000c
½»Aï-6Ån+\x0007%ê¤JÔS'´X3\x0005\x000bØÈ®D%ê¤¡P\x000e CÐÐÜZSTä¤ÈOÅ^+É¿\x001c<ì²n\x0019I	©h*e9:¦ÌHÇ+ÿÕå«Ë·g\x001b\x0013î\x0015©±¯\x00146#'\x0013°Å's,
¾«ËN·\x0010\x0012LÉ\x0000/-(\x001dñ~0ÿmF\x000eàòHÑ\x0014:èò(5\x0016Wl:ü\x000c,(5Ê©EµdÅÞôM\x0019¨\x0003êÙ,\x0018<\x001f
%1 ¹¦¨¼È,aD]¹¬­:8Ö¥)UU¬½Ú\x0003½gd¡ðe·\x0007ªua\x000cÏòË?ÿùêæòÕÙÒNÉÂ4\x001fV\x001egÉ=)64uçìtbÈîÃÎ;ßÒ\x0007Yøe\x0011\x0014;}Ôb2é é¬}Ë0çÛ\x0005á\x000f4\x000e}Ô2\x0013öH×½kÉÒ«Rv©¨ù Fººl7\x0008ì\ËÀå»\x0004\x001f\x000fR\x0019^íÅQ ·ó,GÅF\x0012¢NÀgu\x001díögéYFS|¾Ö.Tb_ÉqÛ¨çÝpaLÒá\x001b<\x0011Y\x0018SK> Ë9=ñÆ· çÛÖI\x0011U\.ÔR\x0007³\x001bÙ"=ñf\=I¡²ÎòÚªYî¼êôÄ\x001b_±ï§`BÑ´©a:Á\x001fpåxãë4ßW\\x0013)ªCÐ]\x001b|§Ì*OI\x001f[æÝYE\x000cd\x0003\U6?µ+\x001eÝAY¬0\x001cÊZµOv0a\x0005jìKÙW\x000b¿\x001f\x0016ÉÊSf§ä`ðp[>£\x001aÛü¤$vtöD¦Òg´I\x000cudWô¼¶IQÓl/9Ë?jévûölöâd(òYÁN· ÿ@²_¿+ü?\x0019ÚÁëïnäg§;\x0016A<í<\x001cí³WA{£ãS_Ä7íç§B·
J¢u\x0017ÝÂéUÁwê¡b\x001fp*\x0012í!H+Ñ?\x0010lÑz¯Z8®Ý¦ª@ÿbS\x001d6
HÔü\x000fØ¯W¥äÑQ·Ô¢9\x001f2¨n\=\x0015É«öÐ¡ (Û¶+rdYæ\x000f÷Ù&Ï¸²
C xA A+®jÅSiß\x0010´\x001c
Ñ\x0010Ô§QëÙèrh1·ýá\x0007}Ý72­Ð¢\x000fÚ\x001eæ\x0019ÐFaa¾Ff¯â½¼çÖçtÛÏÕ0áT?æ\x0010\x0017]\x001e \x0008=\x001f)?Åx?¬ÉhG\x0013c^Q\x0003Ç\x0012H<°T=\x0007:¯z¸'\x001b"{éx\x001c\x001a\x000c\x001dñØ¦G\x000f}\x001fãæ'r©ð\x0000¡ÊIþîª±cÈ¸£ q\x001f.<ðøV \x001a»-jG@ó*lªq]©RÍn¶Ñ\x0007¾# Ñõ

<K\x000cü¿èÕ.ÛíVz8O,ê*\x0001g8h}ÉlkOÇ\x001d±-b:å6ÄªRÎ³®ÕÉ¥G{Ö\x0011	A±÷]<\x0018Q\x0016w¹ØQ\x00038C\x001b5-ZMué f\x001fU§låB£\´Ç¹õN÷I8à
Ç\x001d\x001b/EÙQ+Î&wI±h]\x0008vlT}²u)æ®¹ª¬FT
§º%ª«y~<«HP9ÙâF¤\x000c\x001b-\x0018ÊÚ\x0004-n!½¶ 1pSÓ@È+¶ÿ\x001eõDu.7ÊUÏ5¦Cf6mHµ\x001dø¨çó/©|ËÄ"°£º\x001b¾ç!tst_ÄÜsT\x0019Â¡V\x001eygì\x000f\x001ai¢\x001e{îÙû:LyÒÚéI­÷èº\x0000;-õ¹I\x0016.yÆÙDu\x001axki\x000cë©çÌ\x0006y¡¢É¼Joöc±.Li¬\x0017ätDWÔV·ióÑ	H\x0016=\x001d¼!x\x0017«n\x001fºáèÂ\x0002\x001b"+3	µ¼!ªT0\x001d£\x000b\x0013Ä)\x001d»Ê\x0013Ú¦¦GêÚ\x0018\x0003\x001fõ\x0018x_
x\x0007)cªÌ¡z1½Å\x0003ùè&\x0006q\x0013¹/Söð+\x001e«M\x001d½áÑ\x0018\x0013æ£0ï+pï¸èãÁ~¨¾v»þ-ç<AË4Nptò\x00108ªÓ1$ñõQ¯ç5ËÔá~Í\x0018/k>ºQ&q²$ì\x000fa\x0018¸.M\x000b\x001c #\x001eÝÄ\x001eZ5LÎÙ¯ztm\x001d]Ä(."ù¡E:þE½\x0001\x001d³¿tòÆ~\x001c]Ä( \x0012\x0014_Y\x0015.¢/#j	\OÐâ"+Ó+IA{çt¹q@\x001fÝÄ(n"÷\x0019\x0008Ã3Ï¹Ñ\x0000·ºLØG÷%ûÒ³d#Vrü"Ò»U5:O¼ñ£û$Ù½Ã£\x0018ÕDhï0QûÒÑIíÞ@z¢
TÆÒó(u[ÒÜ\x0013´ì¼\x0008ð
Ä\x000eªWLXVçaè£\x001b$¾C@\x001b¼*ÄxõçQFOGW&ÉêCÜaL\x0018ÉQ¤§NÈP±OGW&	63\x0005¶RíÃ\x0017Õ7¨:©Ø§£+°qÐãmÄúWOÌDÇIGW&	iP+\x0016{íÕ¤N
PÕ	\x0019!L:z½àJû$\x001bø3BÙ$êý\x0018aW>ºYªâãå²ú	[ÉÆ¡G1{ï¾â¤bÆ ^ï|tc²ì²-P_ôú+fl#¯ÓÌÁ|t¬³èUâ´0!.(Õ7äe²\x0019ä[)Þ\x0013Õ¨\x0019ÁjÓ·ÅJcÒwÒ\x0019¼-ï÷ã\x0007ÿõòÝõË3Í\x001f¤û­äÓ'#o	©Û4\x0004ü£··ÄðA\G¯\x0004G\x000bOÍ\x0015½m¥L3R·ÜdD)êìAK\x000b² qÐ;Å<øR +\x0015iË\x0015sÚ,2×QÎ\x001f)\x0014\x001aD\x0000nªÃ¹m\x000b®dñÂ`ÃR"Ô|¸> öÂ\x0003´ Ëé4ð°ó^ \x0012^Ç\x000eäy/öÙ¡\x0019Zd\H²×¬ÄCºSBùmÊ´ìi^	NCÃpÕ8ÔÊEë\x000bîcô\x0019ZÄè\x0007×ä¡\x001bfFÒ\x000b²He\x0015n¡Ý^½þ ÿGRið¶ÖÅ\x001cÅN\x00032÷©ÃÄ¬î0F/sHzt¢e íìpÉ\x0014BµÓT\x0000íÆ³¾\x000f\x001c\x0017há®²ÊÊö@¦<D\x001e¥\x000e\x000fB´ïã\x0019ZÄ3®99ý\x0007BÕ«W|ÖKÊ¶ÿ¾@\x000bÿÝMÊ¶â+Â ÞõW´Þ\x00019WóöþÝ`ðþëõÍ«»Ë3\x0011úbQ4Î0ÆohÎ¸Ð#ãÊA|\x0002Fß\x0007*ÜÒîàSPÇ$\x000caIÈÕ
%â\§öq'ÕÌ½Ê'C(AÑÿQ¡¨Þìbëä/Àë½\x0019>È\x0015á\x0019_"\x0007\x0004ãYÔÚ²P
-T/Iy\Ä,ÄìA\x000f ¶8	¬;kzý-}! ¼=6Ó¶²{?©\x001eáÚé¥²Þ8ã¿½|ûî\Ò%A|ÏÅÉ²Êº\x000e¢ÝSL<¥0"U¯\\x0012ïÜ4ñºóM=ð\x0019Zn»;ÐP¥Â¦\x001cÇÇ²Ûh®*\x0016Cµ+Þ3®\x0018ïJO®¬þG\x001c6äÉ\x0004{@ÙÂ:#o,rÒ7¤3Ý\x0005lw\x001e[j?ªWyôHÊ`Û]Î\x0005LÖë?\x001aÃ:#\x0007±è&âÈîg	Y±h·LÿÀ¤svô\x0005F*'³ØéÒ/\t®¸æ2ÍS<úÂ:¸$\x000f^0þfÔ4F`¾·(\x0013üÝ©%e82 Mõ\x001f«´ì\x000bü\x001aº Ñ®ª©©\x0019ÐÐ?\x0010­é·ÝîÝüãÕóÛ³µ¡ùîÁâw\x001fÊ*9OîºàçuÏ\x0013\x0011ò§ÒâÚgdº×ñ\x0008ùWÛëÖ]Ç¢ÇièôßG{\x001azWüô\x0008\x001bÁ\x0014¹8\x0003þûq"÷Ù\x0019xËÆ,S%\x0016à\x0010Ñ­',8Þ×\x0003JhWV"\x0002\x0006îkÁ\x0001ÈÇ¥Ùeð\x0019Z\x000cÝ(R/ºs\x000f\x0006ôõTÔ~´	3]Y¬êz\x0011úxÓô rÝmJÛ3Õ}÷\x0019ZäF)ÐÙ÷=¤ %\x000e÷\x0005	ìjõ\x000c-eÏªü»âq\x000f(éö\x0010Ó~â\x000c-Z×}\x0015ù©\x001eW	M<ï¡~MÏB¼öÍýßÙõùÝå«Ë»g`AG\x0003_XÊ\x0016YeQì£S\x000fð¹Ìiz&¢[ÐÖËÙUIµ\x0004ü­!Ú­\x0007MÏD\x001cÅZqí}Uì
éÎ4yn5#ÇS×l¢ëi\PuâQ\x000bØ/ÆkV=Ûö´Å¦§->rÉÆl\x0002=mÑsBJ7Ò®z´%1ÙÍ\x0007M\x000f[dÆD\x0016ïAõXwÂÚ\x0010\x001b)ë}\x000fHûWWw¯x Ì¹÷æ\x0014Ý5ðÞ.é*YÈæ1POò¼Ûñ¶!é¬H£CtËvO³©°C\x0014]púAöD¦°\x001b¼ÁD\x000cItv ¼ÌÓÁÕ&ÚCØME_ðeUÓA­8Ø\x000feØMVNä¡ybP·N\x0018o°9ÑlÙiì\x000f-\x0001w\x001b+g¾\x0005EÑ\x000eæ!O{\x0012./½áÿ|uw¶±f
e.È©[D)þ«éÇ|\x001aOÖh³Þq[ìôçãY æD/g«;¥\x001d\x0005"z)¢U+\x0006È]Q\x0008úÔ\x000cm´Yï¨¢ÎK*O§\x001d\x0007Òvïè\x0014²\x0003uÐf­	ì\x0014&yÖ\x000bø@C\x001e\x0007¿üÔ8etÊkÚåÁÁxðPÙ\x0011rÒìH\x0007¼Ñãà\x0011:àåÏá@®;i
£k²qª³«_  ©\x0019÷ºNú)GQ\x000cuµË§Íõ³
zQ\x0003õú¤ßvô\x0019e
#wù\x0019ù¡\x0010àôHú\x00075­ª*1¾?\Ýÿx¶¹!\x0001ÓÓ½ÇM\¢8\x0010{jÓÈÑÏe<lõÊ}å µHÑ«\x0004-p\x001cµ*Ý«dô®»´ \x000f¦\x0012\x001bQ0A£ÚJx\x0013í1®U§\x0005é\x0004\x0008¾(\x0003C¡²)\x0019¾\x001em\x0017sÆ\x0015
6ö§{ð³ö´ªcu\x0011j\x0000¬Ú G{N©¡=\x0007³ªNÞu\x001e­\x0010\x001eÚf¥\x001d8m³5ÌÑkÓôÈU\x001fm¬\x0012tÀo.OÓ#ÙiF\x0016¾T¨:Ñãql\x0018¦	9\x0008­
ò|³<ÐUªjüA?\x001c@é±ºÊ³í\x0000\x0017\x000bï\x0005\x000b kö,
Y\x001d
ûõ\x0015Ëë»sÙ?6çrEmL:X\x000e
\x0018¹\x0017$=¸NnñÂw¯Çcs»¢lgå\x0000H%íFD[pÃëÙ2D6º\x0017õl¾Ûë;ºbAÀÚm<*Á Â
ì¤©0Éºª½\x001ahËÝGfÔjhá~sõîúÝÙ\x001biµ\x0014KÝlc¿\x0010±É<ª÷s9A=ÅÓ)\x001cØØÐ7n(cÖÉw²bØ=Å\x001c¥	ÿ'\x0010\x0013ë(-\x0006[¯pF\x0016´ä>8\s|\x0010yJz\x001bÑöîß#ËJ®\õA¼ö»Ûw×d\x001dßY\x001cÑåon___Ýkª\x001c+âºò6\x001eË\x0015!hCÿUx
1¢\x000fZµo8¤x\x001cR\x0017\x0002Î\x0016á\x001a=6;«\x0003©\x0004bÉ\x00126¤j\x0014\x0010yâòî\x000fdV\x0007ò±kÞ\x001fÈ¬\x000eäc÷gVçc÷Ö<kÇóÈûäfVU´Ç"ï=¸¬Ëh=uVÎj9x8ûÈ;Áé<ý\x001bÚ`CÆ\x0012³#L¿·,_wùýõ»³ùY­`§o]ç|.õrt_z9{\x001f&÷îw/\x001bù´ ûá\x0002^Vâc~\x001au,^¶ó\x0018Y"\x000c^	¥Îä­jæw\x000f[\x0007µpöc!/ÃÊ\x00076Íß½kLï=«yTîÄ»r°-öîwñkï ÚÅÚ\x0002°\x00178Ø\°õ¼&ÌPd\x0007\x0003i\x0019\x0019>_Pl°\x0015~½¶"´12û0\x001axaÅªU©w;¥î5\x0011Osä¹'N5v{¡ß\x0015ãÁ<íÚ}ÓMr½\x0006;éwÅx\x001e2%\x0003ðù<7 òÄÃ9º²\x0016ïUË1vôLçFè|Ðîw	\x0008²D\x001d¡D¥åØ\x001aa¥kñô?C\x000feI#ì\x0011«VÌñ¹\x0007ûè\x0016ÊÜ« YõTÛJGÌ~·s\x001b^å6\x0006´j:F=¦ÅOoc$7¼Jn³'ÒsUâ2
S\x0010µÙÁ\x001eÜÇòF¯ééúåçsEe¹ªQ~Íò uP\x0011\x0019bof\x0011;\x0005õÂ4³\x001d

:¤J!uLÁ3m'ä­Ù¶TÍ\x0010ÆÏg\x0010Äf² \x001eÔ\x000fzbgèíõâ>Qf)­b-$gÕe\x0015åâ8M\x0008\x0001H\x001cÈß]_Ý+«\x0014ÕÆPßùà'<3Ñ¦ºÏ\x0014â4)ÙòÓÒç@RRæ¥\x001eòNB\x001cO\x001d}åIu\x0007àx\x001bz@íÀÉiN+\x0001d\³ÇÉÖ¾ÆälÓáq\x0012Â%-Ð8BáÙ\x001e³j6=\x0010àq\x0012âP7"yL×÷sªk= n8MÜÐ{õ§¨FØ£GgÂz\x001aOÁK\x000f\x0005ÖZÊQMÑÈôz§Ì÷÷¯îß¾»zö/·÷/.yüÀ¹\x0012\x0019U\x0011TÆ\x000cù9â4¯¤ãä§\x0008@>t*\x0019mNeø I>!¢.`ÈÈ\x0016ö¾\x0001È\x0002,2\x0019)\x00027ªùÓ\x0001§\x001aðÐ\x0013³	Ãéñ«1FaBxóÕäªXÙ>[ù¯*\x0005=ø?¿¾þñ·ïLóëº\x001a¨7äfÚ#Áo÷¿Ïk]Ýi	Ó[#ô·\x001aëDA[uUú[©Û¶»î´\x000b¸oôº\x000cVÁöIWÈ\x0007\x0015º\x0013\x0013naô~¯kn(d\x001aTyË1Zaß¿÷Ï~}ýö\x001d»³ñ?CÁÆ»Ü6ÖGëlå°ÔFëùg´ïÚ°0UF4\x0002ö\x0007!áÈá\x000fêG¡kËB7^¨4$în\x0005\x0003PP»p{]PíÜe\x0007j*]+«\x0015ãði
&[W¹»ä$\x0005¾%A©\x001bû$pªÆ)ôNÁþåò¾í¯¾º¼{~¾y¨fÖú&ÉØAØ\x0002ã\x0011c}&æ6G\x001d@î1³â+ö,©¦¹g%¼ K\x00107²ò\x000brÖ\x0010eæ!ôÆr"Ó©\x001d¬\x0005o^rQK¶ÂX'\x001aQ¿y}ùâêÝ»Y)ÿæl*ùL¦WÁ¯þ\\x001f¡ë\x001aÈNmp\x001fû¤Ä`	õ\x001a¡î\x0017µûà/µC¦CG\x0000\x001bLmï©ÜÓå¿»»|÷ì%×énÈÅ=× ­UH]x %³\x0007 |ºY«ésù°]}ØR(t\x0006¾\x0004Sª|Âî\x000f\x0002°K^]5\x0002D>¨l+Qúy^)\x0003hNI"^ùæîöÍÕÍåËQ.ùõíwW÷w\6ùñò¯ï¹.­âµÑÓµ°"\x001b¸JT|\x0002>ûº£IG.´	ð\x001eÑ\x000fBÍO=u¡d{ú,âg!RÚx\x0010Ä¢Ê»ày©fô<Ãè¹FZeë\x000e½¨ù\x0013ü íOM1\x0018$¿¿zw¾ Å×\ð^$!ÁîÐ`dBïÐÕü\ÜÐ²«°§%;\x001ahbÉ\x000c±°½m)»\x0002sê¸Ø*a\x000bøQÜ\x0004k³;Ê®
æ"ìoJ¨úQQ¹þ2Æü\x001aså\x0007t\x0008
È\x0019·\x0002[\x0018ÙzJ°^£ß_¿¾¾ºã"ò9®ÏÅ\x001añä\x001c£ÌI
\x000b§®´
L²Bîû\x0013dÌ}0½ÆÙ%ÌÍÕ>øC­Ptz~ûì7/n_Ï±SR¸äÞ&iÂä\x001b\x0011ÝÈ¦.$î°K7W`ê¶\x0012ügôÀJ´ëëanEªµuÊRà:ø to®PGm±ª
¬H¶âì|sØçëüv\x0005Ëo=)o4w¦\x0013v-dcL² p\x0013Ë	!ð\x0005º¯\x0018\x0006ÝÈÒÛ4aZ2*\x001bÒñÁÌÍ~Ã®\x0003Ñ;I\x0014åT!£\x0015«´P\x001aÚJF _T ÏJ\x000eògª8ì²Ò°fñ%»
>AË*x\x000b2ïÁÛìÝZÑ4«³Ûá
Öª)PñÔÑBPÝî.¦Ñ9G§Nª³j¸(>CÅ'8¥\x0004JwÔ,ÍªÁo¿¾»½>[Ü\x0015o;nYZnù\x0012ªS,¯ñ\x0014½o\x001f\x001aó\x0004Kå G¨þòz½ì\x0007V¿Ón-	zt\x001aïB@TeØ;ª67S#Å½ïÀ%ö»Ûû®Î6\x001a:`¹4­\x001c¡\x0015YüMÀþ|ü¤\x0014
{ü;-½&=/ñþÙoimgº7Í©\x0010+~/.;
Ûí&áÇO²Ù©*\x0014\x001c-÷Áj¥Þ´\x0016(gÝÞ\Þ¼<cM)Ô¢24~#Rs\x0007ÈÐÔi2õ§	ÏÔ>ã\ÌÛz|ºOÈ&¤ßý>\x001e¤hRí\x001c;!\x0002)\x0007auÚE¬?æv01*¯«\x0004UÔL\x0015\x0010´C\x001díÆìÄ¨\x0007.\x001e§Mc^tê\x0012jÆ5ó\x0003ãÒÕªz}ùâú?\x0017	7)®aBt {þo¦qùuÝ't æÖÕ4ûÔ\x0012¢¡r­¦ÞÖè9ï<pZC((Í]R·bî¨yilÅïï}uys¶Áð´	YùakÒ\x001cB©TÛXÌà3J
F\x001a¤õv9³gø@ò§ª\x0001²±Ú»q\x001fÁÃ\x0000Y®SKéyÚCí&\x0007»N=#YÑÍIEVæÖar&\x0014ì­ç¾\x001a\x0004Æ?Üþý|©ÁÒ\x0014uÈ¯z(\x0014\x0013 µ«@èsÉ\x000cÖÝ!aj« Iqí\x0017òº\x0012û/á Á{wLJ\x0000î=Eð ¬\x0007¾LÑFã±¢¾Ðx­	g¶ÑÕ\x0010ôiªÑw\x001cðM+äÎÀÓ¤Êô¨¡Ú­ÜTMÖÃóÛ»ës©p¶\H/Bo'A\x0008q\x000e\x0016|Ôô\x0007º÷uß\x0006k.÷Áj©\x000eïµÉþõúÕýùè§ämb.¤µÍÉ÷AÕbN@øøùÀ\x000f½ó´7»jTô\x001c5. û×¢ÆàN|\x000cÍa\x000fæyPVGÔaqg¢C\x001f!GX³L@\x000c\x0014=]k\x0018É*nàUÞn W²FL\x0008\x0012°Zr°¼M/¼ÍÁ6Xºë/Ï¦+R\x0013ò\x001e8°Ù~\x0004\x000c· 8ydÅ>[ï»>'ör\x001fü©V÷îÞ#Ý»¿¿|wûì×·7·gã1*æS\x001f³£\x0016^`³Âú\æøØE\x001cÊuïêÂñÁz\x001fü­v÷®æ¼>\x0012ÙèÞUþácî]M§}$²Ñ½«ËèD6ºw·òXd£{W×è\x001fltï\x0006\x0015Û?\x0012yßx7#÷SÃ\x0004-J\x000e>ºþä[hT3fè¯¡Ñy7C|\x000fBÉ\x000c}òE4\x0004vgèo¢ÑÔ7C|\x0015
íÞ\x0019úä»hô\x000bÎÐ'_FcÒì\x000c}òm4&èpòm4FÍÎÐ§¿G·1|\x001bY³3ôÉ·Ñ5;C|\x001bY³3ôÉ·Ñ5;C|\x001bY³3ôÉ·Ñ\x00186;C|\x001bi³3ôÉ·Ñ6;AÇo£Ñ\x0000U\x0003ì£¡nc<ñ6êøãK'gÞlÐÕ³¯o_ß¾y~¶ü\x0003OkD6bé[èáä\x0008õ1Fã¥|vïÎ¥GÉÉæz\x001fü­Öî×Ýÿ\x0008¢M(\x000bH+ò«"}åBþ\x001872 Gï1m~Uq\x001fËÛÀ|0ÈE¢×QÉÛtg}­È²ohâ\x000biÇZ#Êú;»¹"Ë*¦õ\ÎëX\x001fU\x0014ö\x0018,Q\x0015Yh+¥(/ÆQ\x0004Aú fg¸ê¬èlE\x0016õÑDõe\x0012UjZ\x00071\x0006ÖëFt¶"j\x001aÏ^\x0014\x0014V¦É}\x000e{\x0017Ü¾jÜËª\x000b¯%\x0008\x001dîxF»äEº'³º¿_¹"\x001a5~wùì.ïî®_Ýþê\x000f·w/Ïs\x001bq:Dó¡Í%×æ²÷ræãA¬O /ùAi°ç´3)9\î\x0003?ÔØo9cd¼¾¾¼y{­Î5@çnOÁÅeõ;¾6Kæ7õlvÚMD~>M\HëDäÃ\x0005?øc
ï¢\x0001ñwÜvp}CÿùòêÙ¿\½º?ºW\x0012w=¶u\x001fda0\x001fÀ:åm´Ä~\x001ab~rÓþ¨zCña%°Òz\x0002ÙÞ\x0008½ê¬ùP
N»ðxÆN[x\È\x0006­\x000eïë =\x0015 ¥¶Ñ[ÔK:ùï¶ñX¿úû3Ù¬à¡µµ´UìBÎ:3\x001fKn/#¶Ë£<÷3UDnöz\x001fú©ÆG9'ôê\x0005çî¿ºuÉ÷è\x000fw¯nÏ4,Ô;\x0003\x0017)á%<oé¸\x000f\x0014A²Øþ\x0013ìü1:Ó\x0016éÄ£6×åÒ<\x001a\x000f·F¾\x0006×(æhêW\1âyûU\x0000\x0007\x00101ÊI\x0006°Õ#¼\x0002\x000b¡!^bØ68Lb`âãÈ\x0016Á\x001eBY½æ-|}ûâò5ï¼ÞD:´¦ù¯ÇÑ(EW^í³_ßÞ¿¡ó´g\x0008e¿?O\x0004ôðyê	ÚtúÐ,ÿÜyî"àJ?ÕÅ4ÌwW,ðöûD=jC¾ò\x0016ktÏ
0¯y\x0005;\x001aÂã¶"\x0016\x0010/àaM\x000bñµ'rnV2Y \x0010G]~º\x0003[õîòúîz\x0011¾{ywyÿ·óìHñ)D<Ïi\x0013û`\x0006Åíöæ\x0016G»È'Û\x0012»øæòí"Þõ\x001b2Z/¯\x000c Gn	í	\x0018\x000f_ÓrHÈ:ÄU\x000b¶$µ-òO½%Â\x000bøæõx\x0006)ÿ\¶\x001cå^¸¶õ%»RÛ:ö"¶i|ÔYöbûÛãôæþæúÅõ÷ËæÌ?{ý3ò\x0007ÿ×ù\x0017ÿ7ùW¼ÉôñôtaúríBÆ«'úï+^\x000cÏáû{ú?]h\x001b\x0003 \x0017ñ¾V}ÓàzÂ\x001füíîïåoGyº·\x0014-Qxzsy³ã\x0008<ò}È%	kÛ0m\x0012k\x001bnï,½çCöäoü~×ók\x000f9\x001cÛNËÁK.k'\x0017/¹A9ÿ\Ù;|\x0003Í\x0015RØA`×7ÅØ<§\x0013±\x0013b§î¼Â_È­Î\x0002;\x0007É\x0017\x001a	±éDªdÂN½Å3¡Ä&O\x00066º>i²ÂÎ\x001bvq«sÍ®s2mÄØ\x0015±éßQ	)]NÅ®ÇØõTìvÝNÃþ²\x0003?¤W7?X\x001e"Yzò_²xÀ^½Ô"\x001e\x0001
ç\x0017G ¡\x0019©LqDöñ­@îù=\x0001ü¶QÊ\x000c°©\x0012\x0011Bvò¼Wè
¢\x001fÛw\x001ca\x0005¼Ù6éa\x0006\x000e ÕS)\x0005#ý\x0014S½ÙBOjÙÎMêM&JiÝ>
`Y_Ã\x0006\x0008ì$Ö]V=Ì\x001dä¢kè\x0008\x001c,\x0003 7\x00030Ä@·Nd#<ìµ¡\x000fá÷}Ä
»
	kgÍ´è¡».>$¾Ò<ÓÊ0\x0000\x0002{3\x0000Ü×ß6	\x001a\x00056ýu\x000fØÞºÿ\x0002z»ÿ\x001c\x0017±×Ü\x001a\x000eß1àª'Ý~\x000cÝWè\x001e7åØ±ê0Ri\x000btvÑánû\x001di\x0008±WÚ\x0010}I¿É\x00040vId´ì¬<ãÜwÜ\x001e\x0005\x001eÄ1k\x0013Æ8&Q¶J\x0010¸Ê©ùTw:¤
|;Ü,\x001b»è®3xòRj|\x0004w\x0011­[©)£À·CXk¦$Ñw§»\x0012ÆÝé8¿AP1Á>*·\x001bóâ*ÜûL×
lwc>e~ðOdø\x0013\x00076üAû¿{îþzÿãßEÌñÿÜÞ\=ûòüSîhº\x001aîé7WïÈS%})ÓRá\\x0012\x0010¤°PX÷-r-#B}ßÃDqQ{O÷¶]ø~\x001c­ùÁßkØxNÃÖ\x001f9üpûæ§{(}E\x0001ö¹¢
èßì¾Öæ7·©®³ºèò8!hôþhsDÖúkVýdO\x001bÃ[^Ûn¯ùÁß»Ûòß¾~ù\x0016¶¢¼;ºIÆ»G¦5 {>}íKG9­H|lXb(|º}×oÕ´;cß×·êhÍ\x000fýÜÝ¶ÿÛO?½xu)¶ýc¤\A\x0017\x0002þ%TXZP¼,sìO²ñ¶ýªÚM\x001b4v~3`Ü>Ù£X´\x0013:É\x00089|\x000fÝp\x0012ª6`\x0002{3`ÜÀÖDN©×IúbÝÌà;b«\x0010|óÝOå§kyÞ>ûÝÕ«û½ÖÒãSêGvmö§·ºwa\x0010| ç\x0001¸MOýMµ\x000f?íÎØ÷Í\x000fÜÇºúO>V\x0015Ô ù*Ý³\x0019ãªý'\x0001¾úO{¬ê¶#\M\x0015G¬M
btÇMÿ»oú·\x001fn_¤\x001fE¶óÏìftLÝL!âü¬æ$R397á)²`¶}Ô{>m
\x0006NGK~ðçî6ý]}Q·mú¹¿\Ò\x000f÷o/_^>\x000bçò
b¨%u÷si(N6\x0015Ïg~ÕÓqì}Ùit\x0012í¸\x0005ò¬\x0019YÁ+P¿V\x0019TÀ"\x0003¶®Â\x0001ì\x000e\x0000\x001cÜ@\x0016LÊ2\x0006á\x001eK0\x0001\x0019«Ù[^©@\x0016ÙÇ\x0008a%wãwÈ>F<r42\x000f\x0002X¤\x001eyþD\x0015À\x0011ãÕ\x001c\x000bnx\x0014È\x0005Ë\x0003¡½ÖPÈ"í\x0018ÜªóÄÈm;±!û¡û\x0014²H:8&¬»\x0011äxkBÆÜ\x0011\x0005\x0003FÎA wD\x000eb7\x001cäºG\x001e]Êa\x0016)Ìã­ÅEÉMÊ¶2tEè°³R·~ý÷~óòç²RX+MÈ:ÿ´vøóÏ èº<ò-|¶HÛ(Ö\x0015g<\x000bø¨I}TÃD	\a¢bùÀ+Îw\x0007?é®¡Z!\x000b\x0013\x0015\x001aXU²X\x0019J$\x0001ïa \x0004®0Pö×{à»\x001b\x0016J \x000b\x000bå\x000bØ\x0011.\x001fãm\x0007Ó\x0019\x0015ÈÂBy'+Ñ,é»ì
"ï}ª\x0010þüo÷?AÔyö²Jûº^0µËc$¢¨`;UúL{³K¡K~àÇîö|N,ê1«¿ü¿ï®.w\x0004²Gî9Ô©êËOHu\x001bg?Í\x0014E|CEaã{(dËö(3ÈãÉâYóQ§Ð¯\x000eïP\x001dÏ6U+òf¨(0Yú¡òø`&è¡`KuÛ7 on\x001f<¾É\x0005^3>k©f­ý\x0000ÈY ÇUyð\x0013¬9B FÈ]V\x0006ärênh§gE®bÍèYÎO¾XsÃ5·¨U[\x0001¹ºfíô¬ÈË\x0013é¥Àz°PÁ¡ÿ§Ö<¤ÅvNÏ\x0002-\G.Ú\x001fÝ\x0015/î
3[=<dxW`LâxÉvR³\x0000-.K²ìÉ\x001bä\x001b*Ò*hC¢nÎ\x0006hq[êÔE l¯°ê\x001e=«VehN'ïõÑMôâ&¶04\x000fWg$*èêÕ^\x000f¹²]ÉiWÑIºF£ûS\x0002¬\x001a]³QOõG7ÑÈ?\x0004nR\x0017±t\x000ck1\x001c)Ô\x001e»Û\x000fü\x0001õ­<¼\x0005ø\x0007ðT·O\x000eÎ·\<À_q²÷Çûsy<>blèW0§Ù\\x001ahÍgá¾ÿñ\x001dÛ÷?¾\x000e§ÑK\x001c¿\x00122ÞúàÐÕÎ[D\x0015y³'!úUAtK\x0003FØ¾`­9hQ\x001dVät*òþÊÏÈ"KÒª¶6¨\x001f
é_~°#%õ#Ùï¼Ýx\x001eÉ#<Kî\x0001`\x0017pÉi4"îo¼C!K^rþ\x001eßÐKÖÄ\x000fßÌ·×áh4B\x000eP\x0015Ï	ôî	YQGé³\x0014û Å\x000b\x0019[çd34»|\x001d =n xÆì\x001bøàåµ\x0019Y\x001c;ç%ï0(gY\x0013´Úè<
?:vâ¥	LnØ¶#¦\x000cEä;.Úe·í
ÐâÜáKÊs\x0015DÞ;­\x000eÞÎg]I\x0001M¯zçÃ\x0015µ!qÈÞ£ó\x0011¶óáÙ\x0014\x0015¨Rá¶8,ý¹I§1\x001c\x0010Ä5ì\x0000Ì
Á¸\x001d\x0011ËOi96\x001f°ÅÂ\x0003öH{Z\x001eø\x0003\x0005þ¯mÕÃ\x001e$cäáÓd_þÊ%ñFþûË;N	Ls\x000býñöÅwçJ\x000e´\x001dÇzå\x001c¼
,\x001aVÜ]<\x0005³ã\x0003\x0013jÏi4áç:\x0008^ v®JRC±éE,\x0018<æbózr-@ù"äÛõ_\x0005ßÐw¹æâÊÈmÈ±§\x0019&Bm
Wd*É`Â\x000bÏÑ\x0004d­¸æ\x0016¬\x0008xEÎ\x0002¹É\x00168>áôgµßÝ	ß?Â+² \x001bN-?\x000bpO²·¹Sã\x000f\x0018j2¼Ë´OïüXß¾¾ÚÉ÷?òÚ\x0004\x0005\x0013ò2úf`¨µ\x0006\x000e½ã*«Y}Þ¿Iq2m£ì2â\x0017\x0019\x0012<X=ÉZð\x001dx7Á\x0011L\x0006kÞðtûhT\x0017æøzm²yöÕõ+Ú©Ëë»E2óW?Þ¾¾\x001fm!gÊàÙÛÙ^b \x000cÜr:´ \x0018ð-#ï×.çÖ®\x001cµÁlX{ÊAþÎ+»Hÿ¢´\x0004Ìpr@
\x0018n¦éµ62\x0012^çï"\x001d¹v\x0019\x0017)Çý,'\x0000\x0016ù\x0008 ¶\x0008¼¶åÛ\x0014°É#M\x0003è×é;:\x0016N´Ú6Uq¦#¥\x000frl^çØ¸OªóÖ¤ÈþÈe"p6ÓÞIO4FÎ]½»~wõìO·o_\îµo\x001ey{bÇ<\x0000\x0013Î×_Ã©Xamx¶ÖÜIyõý·'eu{BóÒ'¥\x0010\x0005_ÿ\x0010°]ÜûüwÊêþ0òFú\x0019¬ãä\x0011\x0019í£Ëz\x0016\x001a o÷'tì5 P±ËXO\x001f®y'¥\x000eÈâµ s-êÅäÏªÝáô®Ùõ\x0019yó+¢ß\x0002\x000cq&dU«óZa<CYÝLkà\x000bª±»Ú\x000c;±>#oÁ=+#	Ç0E/EÁ\x0008¹`Lq}égä&\x0003t\x0019ðè\x0014DV=\x001daÌJÙ'Ögä.¡àbS»Qâ¡GM°@´Aä|hÎMî\x0002ÖÜ\x0014pÎvZ}\x0006Þ®`A´Ö\x0005×\x0000\x0019? ëGé\x0019y»¬¹$ÜäÄ%yù4FíêÅiìÜÑ\x001d\x0014YõHñ·üä6\x000eÐUYIoö[¬ÐÛ%²G)\x0007x\x001bcP\x00194¦¨\x001by\x0019VÜ@ò×`ÅªÒ\x0017u÷Sªf\x0013Ç
-î`s«ÌûN\x00184Ðf)èvç¡ÅUit#ì3<é1«ªðL9º+^ÜVea&µêQÊ~f§P&hBd¡\x001b\x000e ­ÇRñç°Ó$\x0005hY
£&)\x0012aP%'Ûg:\x000fÞÈÏÌÐÂã³_ï\x0007_~­I
ÐÂåó	Ùâ1\x000c­c7XN;MR\x0016N\x001f×?eLæ/\x0012VU\x001ce
GW&"\x0014¼\x001e`Õ\x0010â$O¢UW­I
ÐÂ¡¬E¯\x001a^Zº×Êê
ï \x001c½[A¡RNþ\x0005NHèêø&)@Ëp\x0012\x001d0Ã4XuS\x001b2Ùpt\x001b`Á\x0010#ÜFpjRW¹Ò21nc\x0014,8z\x0014S8´©Yu«N\x0011R<ºQr¼&r¾¸`R³"OÐ]lZ\x0014 %\x00135ÉúgâB\x0003\x0010RU;=É2\x001eÝÅ(©¨
^T</µÑ©ý8:yQ²/;¸¼EÙsÅý¨G\x0015ÐÅÆün'ïFls¸ßA5PZ\x0010kÛ\x0002¥?^}ÿüõõ\x000fg+SæÉ¬¶U)éÝ9¤âÚÅh>äáG}@rm|é|'9«	ÉÆÔ=ÜôÝd\x0008@ÆC.Ü\x001cÆ»Ø0^]¶C$§S\x000c½¯c·æ5C-1Ú&¯¹ØµÄ\x0019¹ºfãö8\x0015o0ç0%«<tv\x0018r\x001d\x00148\x0015\x0014dßeò¢øá\x0006¹¦\x001dýïîïÎ\x000cÌ. 9{\x0006fÊ£Ë0jÁíÍ¦U\x0014(S®{VØ¡Mü\x000fãUwÊ\x0011ÎX´åñráÃÐn'Î\x000fÐRõ"È\x0018)Ôê0ã?Í?·¼U§¼UúO{¸\x0000\Ú\x001eêÔöpô\x0011KÉâ<Âlg\x001e
Gº«Â{\x001e\x000c2ËïsÊïËµÈ\x0015AgØÖ³Þ3iéú©Á>S­ìËw¿ü|®¤pÄ2O¬²)»A:ÆNLzÎÙ\x000f¶Ù%h]\x001dÜKò\1y\x001dï1&;«U2Ùä\x001c]\x0016Yt\x0000³»\x0013Ëà\ïOJ	ÚbWaûZ\x0019ô@á
c5;NÔ>:(8È×\x000b¤©ê§Ú¶\x0008TIx?'\x000cEpÀÚÐb'\x0012þ°Z\x0011îÄ\x0018¶aJP/\x000cGxN¾Ö\x0015Í0UÈæûRz_Ø=\x0005Ù\x001dé²é\x001b`U
NñáûQÇ#¸"wÌà¤\x001eB¬5ØY§³v\x0008:\x000cZyÈ»nÐ\x001e\x0005]É',öÛUpÖ\x000eCKIÂ!\x0019\x0010:á%iý ñTpÖ\x000eC1Òv]u&^V<b\x0017\x000eè\x0005gí04Ýl±èÚGÉa¶,ö)\x000fwtU$3Jÿ£&\x000fê\x0006iê×k.-\x0007ßýñöþÝ¤«øõíÝó1fù\=Â)dõp,ó\x0017§2\x0010¼gõâI¬u­|Þ'[±\x001bÇÞj\x0001ZIóLdJ.º
á "¦\x0002D6\x0008º;¢\x000bÒ°K\x000e\x001a¹Üè®N¾QkÛ\x0011\x0005\x0012d¸F*J@aÉ:\x0004§\x0005í\x0001Y¦/ªìê¡#£èýÝ)¹Ît1\x0008í]»Øt\x000fäÓ\x000bpsr)Ë~ØD\x0006>{Ýè\x000eËH©áã
ÏÞµóÎ\x001a\x000fÞªj<DÑ\x001aZu=à³k"àcW}t¤¥j9+\x001c5ÒÔ1ÁÞâk&à#/Å9×L@Û$=hÍì\x0004¹×D@\x001e7"\x0012E9O\x001dH[N¤GLEÄ´\x001bÚ\x0005Ð¢KV)n\x000bwéO¦xQi?²K\x0002Cz¼'\x001dòôb©ø<úiàìÑÁ\x00139lÖË\x0010ÉÏ"Òbîê\x0015\x001b\x0011\x0011ËÌÐâåuy\x001d;ìRD§Xñ\x000c¾\x0017;=COîÒ]gým0L1(\x0012 \x000eµÈaÇ
ÅbÖÇ\x0007·°¤\x001bÜ\x0010½3\x0012Í3´(2ÕD>\x0001\x0019\x0003i:æA\x0019êbgV'è(ñQº}{ÏáT;Ì+áå\x0018ÙÏ\x0019Y\x0014Ïë8Ækð\x0007EOò¡T^!î\x001bæçjörþùÍ÷oß.©Äs9)ß6$Ñ\x0011
é¡@ú\x0014<´>¨ò\x001fÐê û\x000c9é,\x0013\x0001¹ \x001c`VÝÅä¸Úl\x0008§»\x0001³Ïðô\x0016­Ùà\x0015rJ\x0007
	»n@äYä\x001a)ß\x0003ý}¬Ü¦,;ü§«»;>3oÏhJ\x0003KáàüFIGåé>0åã)}\x000c
Æûýâ¢[HËæEáÆ)ÎhSÓ<¼;èb)\x0016©UXÍ\x0001\x0014
Ñ»,q\x0015x{è¹)ÐmïO\x000c\x0011: :f-YNÒ\x000eÞuçhÌÝp\x0003§ìä´\ß»%l±ânîCeg³ÌÉ ¸á#ïÒÔü`×º[²¶*I\x0001^\x0007¸ñ-aÉ%\x001c.º¥±f\x000f:V\x001c¸Êç²aÕMéÊ£5LèÁ\x0015yàrÙ¯ð\x000c,£¥&i~ì¥@¶¨\x0004Ìé¸îwÃ\x001c\x0001Z\x001e-ÊÂiì])[wõ	{;x'hYß$[*ô\x0015Ò,\x0015$rÎª\x001cÕ4Ù°*râ7/Æ0¾g¿½½{u.»G.\x0011
x·°*\x001f2uKøÈÉ\x0008ORs£¸Å %\x001a­2<HÎ$¤½hÅÈòð*\x0007Ø\x000e2\x0002NSüR22[öB ûª÷Ñî²ÓL¼\x0014*L!ä\x0008©V§$ÖÛè¾14_5a»\x00089´\x001dòþ\x001cfÿn\x001eøæþúÝÛg¸ºÿóaT:ò¡oy©ØÉ­\x0017ãÈ\x0015/OÅ}Ð7o.#ä:ê5ËN\x00081`B
dôÑY%\x0007\x001c4y\x000b½\x000eÀJª¾\x0017	ÉôÚfdáµÑ?\x001f'N¸ä­ãÕq]\x000fZ\x0004d@çä³È<Ä èå^Í'pvöh\x0006\x0016¶÷¢5ÛÖ dm¸\x0013.\x001c\x0008\x0016L¸2ÃÍ'Là6ÌïP\x0018_Ï
/ÇxgdA´ò×À®¡ÎÐ"ª¤m^wk7ÝT½L	£}\x0016	Ð$\x0002qå\x0017ª\x0001¿_hÎìAJ\x0016ä÷cÐÙ²ÛH¡\x001b,:T*ðGJz¢\x000e\x0015noþ \x0002IÚY\x000c\x0005÷¬ÎáîÇ#}ÒÏd\x001ey´\x0005°¢7=
Íà\x0014¦]Õ0B]Ó\x0019©á\x000fª3²°N,u"ì^JªßÃc
:úf·¨ÌÈåÔ]6X
IÛ½$ó¥T¼ë \x001dc?`«'m÷è\x0011V¤&UöUs,j@\x0014Ôo^_¾Xîãoé°_^­ë\x0015¯Þ£°\x0002d£¹\x0013îóé\x0019;z@\x0001ªQtè×§¤<µI\x0010qâ®Ü^aWa©\x0001L\x001a#? ôª'3\x0003²,·7)ÍÄ\x001d°ÀI9é¹ÚÛ\N]óþâÄ]ÅýqÈ{8î*îA6µ\x0015²¯oïïÞíÊ¨òy\x0014:ieÒq&åÓÅcF>ºî°>Â¤uÁý¢£#o¤\x0018rEÕ\x000fXqà¬r£@Àfg7i\x0013MnA¦U
\x001bI	kY1UQ£¯OÖN²	Y¡\x001f/A}vËrÂÚ\x0012èo}ùâòÅõåÙ¯9l+\x0008Uðp}¸<Îú$
\x0008\x0007ÜF;íòÜÆz\x001fü¥v[{$À5|b1=rU´\x0000Øs}Ñ\x0017"»MÉ³\x0004¢\x0011zîOÿ\¬ytQÄ×¡\x001f°¬ØÐ/U2£¶üÓ\x000c,Õ>K¤ÅIYSÖD¾^³íÊ\x001cO\²árGeV¸
êfN-9bSkv£&l¸ÜQ\x001fpQxçCëØ.EçÉ¦©Ì°å$XÃÙÊgàS,ÚîY½¡d3>«9\x001cHJÍÈíTdÃÊ$²Õu: AÁú\x0011Ð{û\x0014â\x0017»Ç¼z}ýö|\x0019hìÚM¾o´Pe¾æ´ñ©jo{Û\x0014´mâfYQ\x0018"³'~\x001dl|JY{ã\x0014´qJdä^Ô¦´.½\x0012WÝ\x0016\x0008Ú8qBÄ\x0008¢xL*z%\x000c\x001bF÷ìÞ:\x0005møû	nduª\x0012¬\x0006å%\x001eïe\x0019§ \x0013.wÍadº%ë\x00127Ã\x001fè³\x0004m¸åRrJfÉ VTLd³7QA('Âö:\x000f 	KÅAmv¢?h\x0013õHä½
ÚD¬°à\x0005Õ®¼V%BÜAuBIÖÇ![MoË%Tªÿûø\x0006\x000bA×>È×þã\x00159ÞwïÎålÇ¬Ø×
\l:¯uêîü|"¾²+}8\x0010«c-\x0019loÊ¤l
:^\x0005EL©Ü¢\x001a½(ÆC²W°]¨¢åoEä¢ziaä\x000fâ²\x001fx\x0014ýtYÿ@W4µÔ\x001fè¦ä¨\x0007¯±\x001fë´_S¦]Õ\x0004S\x0011"O\x001c)H\x0001¢©«ù\x0013ã\x001bé\x0007­Rs°à\x0007¬å\x0005¹ÒóûA{¢ÅoTAÎ£³\x001fFûó	»Ã®/)\x0016©áÉ+\x000e°/êÇÚOÝ.çA\x0010qa4KTÌ\x001b\x0002¶ÒßI|Rcõ/?mÄaÒC«_§²\x000e.\x001d\x000ba?MÜ\x0007×¤t\x0006¼p'¢à#º	ÔêÐÊÔmk\x0004²:\x0005^é(*G$+	2O1´\x001dÈê\x0014x%\x001c¥P`Âo+ZSÄ\x001aÖ¼âÊQÍ\x0005´d³Êèu5ÊçÆ°¤\x000fùÁ¹xèHÙ\x0011gPî\ç¹b´#ó\x0014D¶ »O\x001d½gÉ¦êOÐ08
®ñ²æ0ÍÙÈeZ>#\x0018-«_M»°~á\x000e¨ï.ß|ÿ®åÍ«39\!{ô\x0013â*T\x0019\x001byÒºÔO÷¼U}\x0002ÓÞð×õ\x0004Ë}èg\x001aû\x001d3¼ml\x0005¿¾|ûîêõy6;ÆdöÞ×\x0002`bÂvdb¤S?ÝdÝ¢ïÏsÚ\x001cÞð²Þ£\x0015?øk­,¾¨\x001f­¬¾uìÎ9Ý¹XU³ùéãÂÉþéG\x001aDø]%É\ïñïv}^ÌëÛ\x0017¯ù7èå°v6ýëæ¿\x001a÷_]ÝÝý]æ¬/R\x001fþ",\x0006µU(LweD\x0017ü#YàS\x001c¯xJkt×/ÿþü\x0011\x001få±;w\x0014üg_ÝÞß½º}µç\x0007<v7ê÷\x001e»Ñ\x0016±íÌ
T\x001b'<R|×HÄ'Û
ñ2Þ¯î®Þ]oCZip<Òj/Gç·ªgL>´ÁÃúD\x001bâ¨E~ù#Ýç5.úç×ãüíÝø×Ï´1mËXóÆäÁG7¦¤­\x0008B\x001bÃRñÓmLÝ3Ýþp{÷æòæåéö¼\x0015	tÔÈX$£Çm\x0006g#lF\x0011a\x0015¦ È$Núi6ãË)µÄ×\x0014gûòåõ«{~oÑûì7wÏ_ï\x001bþ\x001f{P²2'm;'Üdã·[3·à|²­ïÝo®î¿}ÍNÃ¸ÍIïÝ¯¿»2fÉÿ¿3ù½;óïÞGý·ÿx[SÞ»5âÿéþõÀcSßomè\þG¼Rr¶Ä\x001f®_>£hðùÕÕnÄãö!;¡þJ\x001bA8uÎss3sØRcj}j`úT\x001b\x0011º>$\x0014 û«;îZ8ïBqm»áj¨Ë±àBQÙE­^\x0005éO»\x001b2þëÛ7ìÀ\x0000èïÎ\x0017\x0000Ú\x0003D9æÅ¬þ»jqÓ=iéâ\x0005_yåTå÷?]¿ýÕ¿Ü¿<ÓÑè±H·Ö×êzQX8gÙSÿ^íWÍ¼\x0013_]Óð«ß¼ÝM\x0016zìh[Óæ8\x0011ÞçíDMN\x0004ko²Xç+(ÑþîòÙW÷×oßÞÞÜ\Ò5¹z7\x001eº¼»;Ë¾dç \x00137§Ö°°t3ëHmÄë\x0018|\x000cª·âi÷¥\x00032Pþ§û××;rëã\x000eH¡è\x0017â?z?ç~.ã¯7%Ö0Õ!Ï±\x0011Û/ÜÒoîo®_\¿ìÌü¿"îï?xn9÷Õ¸næV\x0016¢\x0013¼¤®fÖ øþöû{ú¿ñÜ§ÿ+Í\x0010«x_\x000eW\x000b´ñ¼IøÁßÞ¼tå\x0008ì¿¢?øæêæÝGq*}íà9Õ\x0014×ÌO÷[C\x0007ÝÚ¡ÔOÿ¼ïKc§îÛ{\x000b¨Ë.A&ûpÉ\x000fþÜ\x001dC\x0006°Ã©Øñ\x0018;±Ó©Øù\x0018;]±Ë©Øõ\x0018»Ý±Û©Øý\x0018»ý\x000fe_~¸qßya_~Ï&åÕÝåÍ+
ÆX\x001f­aó/h½	\x0015­\x0018\x001dÏ=ù>£BQ70µQ¶\x0006JëE¦9¹#}´\x001bl?7GõsÓ^`\x0018°×ß}l¢\x000eÃ\x0013z¤\x0008KêµH°«ß7'\x0002v>uÝúr
ìr*¶¾\x0002»­/Àî§b«¶\x0000	¾6\x0006<\x001eüø\x0014úO¡×o\x0000\x000f'\x001fñUáñàúu\x0013àé4pm\x0011ÿR®þòÃO_ìYksày¦ ³¤möÊ\x0008:KYë½µ­S£N¯ô>]äásï·Ó\x0006)g«p±­ÇQ
¾\x0013·ûBµ"ª^
³( 7¨×¾ñYÉ\x0000:¯X{½uØIï÷\x0002z½ù,½ñ³ÝÃµaÇ\x000c7°CØ«¤\x0003vùâ=_ñÁ\x0013`E]\x0001{{9svA*\x000flLiD·g®\x0001öæWô\x001e65£8zõ<ìwÚÄ`\x0007öÄ)ÝY®
ÜsÂ\x0012Ç\x0002<49E[]\x0003ð<º>vÆE¯'Þõ¸)<ñÃd<µN:5ÇçdÞåáOntz,ÈtÚ£Ä.\x0005?¥¥&\x0003ÐU@ÇMÄ¡û¥Û°«Ú>üñ·\\x0015eø\Lzy\x000bxËê|·\x0008\x000bo®Ä½\x0016\x0004_Õè\x0008Ý·5j¦ zâ¬à5C&óÏ{)[ÀÞ>%'Ü]=(;%VçÙKßCñ{­;\x0000ß¾&yË\x001bËÀ«\x001bjø[BPÝ^ã4«D¿B+zØ^¡ÔJØ\x001aÐiÏkSÙXv yü C*ë6\x00074Y¢Ñ¯Þæ¸°ÙÊR~Í\x0016¦þëtC\x001fü\x0013^ÿ4ôYÖ_á¤\x0014ÿÔ±Ü¿¥þ/åu¹ÙÛg¿¿½}}¦\x0012Gê\x00113uÎÛp!S:í,T3%,¦Á74û7e©Èç\x0004·¼\x0002\x0019ûæË^Æ\x0001°Ãvä]ßÔw"Óä
nÁ\x000cÍÊW\x0008hqU» ªÓ²ù¤ÈóNa\x001e\x0010ûÖÀ\x00167Õmbväñ-CKW,\x001bN¡«­ì\x0004\x0001{3¼ö\x0001yðl\x0019O¨îbÙeã\x000bÇ\x0011©Ãôè0¡\x0018éüoàÛ\x0013Jëv8	JQ\x0001\x001bgúö\x000b*°£À[Wmd¶'Ú®\x001e;d«&¥\x001cLñ\x0006²é\x0012>f-\x0012¼y¤\x0017õCý6~÷×òîå\x0017!¸°á¾üI½w¯'Ùâº¤ë|.\x001aXuê¥wEìÊÖ\x0002Î\x001f;'\x001fÝÒÔØß«¸ìòÖ\x0003»]bÉ\x0015æ¿Òÿî3}÷ÍÓ\x001d\x00046ÔØYK_º¦<µ§áÙ÷VD`o¡\x0000ù\x0010ödÅ\x001abÇ)T#5*°Xw¾hbÙ\x0001J\x0000´%P?æòq7¬Þ¢a|+\x0010AªN±t<øtºö
ÉÝ\x0004v\x0016Ò(]t\x0005,­à¤¨õnê·»÷¾sPe8?\x0019\x000cWÖIfLÐ\x0008[(ç4ÓÐ\x001búèwüÞüþ»4mºK\x0007K~ðç\x001awI`S±õ]\x0012ØñTl}\x0004v:\x0015[_&OÅÖ!»À.§bkwC`×Ó°õEeeõíþææÅëÛ·Ïþxûöêõ®å±/]êà>\x0014'^º%/>\x00147Â~;9ÑýþÛÉ{£ß9Z¡0¼!w9R~lô\x000eýØÖ»¹"SõÍ\ã©È@Lðñ_¬àÉoßø\x000bÆ1Êo\x0003\x0001¿¾÷Z¯~ûã¿+×"ªûæL-;¹'ùÄFÃrôcÅÓ5\x0010¨®æ³\x0010qÞ{ô¢/\x001f\x0010ÎM;ïhÉ\x000fýZã\x0008èx\x0012ôî+Æ«»¿þøj\x0019xûì÷¬öâL}&ÿ\x001fò4ì»l$Ä&\x0012%©pNóI\x001eûß«¶ì
Ñ\x0003\x000b#U±d\x0018UÌ¢\x0008t½\x0017ë±\x0017Ø"Dç!\x001fÛÝ,äcÐØñèÝïÅÌ\x0001[Äu¼Ð"Ö]\x0006YG|&Èx\x0011ö\x0018Ð¡\x001f{\x0004v\x0017FkÅä©ÀÑ\x001b/½\x0000\x0016ñbï"\x0005JÏr$a\x0007\x0008FélÕý(\x0000À.ÝÅº\x001b&ç³zCÒ~)`oH\x0001ºpÉKoR@°3tXyÚü`¸û\x0002»mØ¾Ã!á;\x0013\x0001;vÜ\x0013­¶S¿-?õ\x001fó;qóoo^>ûæv°Å®.oÎ¢«\x0019B2Æð9\«L}Ó÷$õÿ8§
>Ó6©3y°ä\x0007îî\x0003üýå_ÞfÑó»ÿõßÿç/ÿãÅëû½ÆÉ#w]èPÍÝ«Õõ,¼-»=Ó\x001dý6][ÝiktbÔ^òC¿v·ç·ÿv×®äîÛû\x001f¯n._éC\B]9ÝZµÈ±K\x001f}ÃÉ
°ª¹ÚK6\x0006Ù\x000b9ñ¸hQ\x0017
Þ9\x00075ÀRÀ\x0014àÛçäA\x000f\x001bÝ~éËâ\x000eÚ¡@óðpwÕ\x0017\x0001¾½F<è5j1YE\x001a_rèðC¥²÷^¾¸|e'T®ùãí\x000f÷çº§%\x00048ºÉ-õÔypÂ\x0016l¹\x0018Æ(óOulÔÞO;´#\x0001K~è×\x001a\x000e'Bk. óIÐúÀüõ/oúý°.¿üüöúå\x0015í)½¦7ïÞþòó_nïÏÃGO±÷\x0019Ô\x001c×VD\x000eêV\x0002g\x0015Ìqü?ú©)åý\x0017mÒ	4{É\x000fþ\Ã§\x0016ØáTl}$\x0005v<\x0015[[1NÅÖç]`çÓ°õ¿ûñ]z)\x001a c|æ>Ð01ÂÖÐ(Ý]®W¡-åL\x0019©iôq·üàÏ5»À\x000e§bëã.°ã©Øú¸\x000bìt\x001a¶>/^?ïé{ððÞÆ¹?Þ¿}wMoö¹r\x001a±©ÆJïÖ~1$.*TÍµ34>öÑÖ¡ð´E (\x0007ãHÐ\x000eZH\x0013Ì±8ðõ|\x0018c¸¢v$7ðèN\x0006×WI\x000bG2FÙÆª­à¥&\x0015\x000b·¨E¢8ùê\x0019\x0013ÚÛ_ÞL-ÊgòôX¡\x000f\x0012
u­72\x001bKP_òÞññù%}À£Í;¤lXIy|Æeã½ZFâaëá¨Ö½"\x0007@99\x001f®ÒBÞ*+­¾\x0000oæ«´%ã=®rà\x0008\x0001;çñûÔý0.¼\x0019/:(
;ÜaÉ¾tDn\x0016?uEÎ\x0002¹lóà8¹\x0006òìÎ\x0003áö	°\x0015y+tñx"L5&É}	Ñ+àñýtök\x0005®bÉuL6%H}%C>V©{EnâdxÈ|õ´Ô\x0010à\x0003zúøÅàë¬È\x001d>`Ã<cÅ\x000fXB\x000eV\x001fÀ\x0002½ÅÑ½(»8z\x0016w0öMì y\x00165îtK\x0008=4ßwTíz+N^\x0010ùL{9ù\x000cÄõ§#\x001d\x0006\x0013mÏ/Ü®8°\x000bÙâìkîR¯·\x0005Ñ§w¼òw\x00029\lÁ\!ç\x00166%(è8Ï\\x001fØ;\x0012¦ÇK\x001eï\x0002ö	3.¬ÇKÿáxé?ø9½;^½w¸úÜäKÌ)o´Éá9wºØ\x001eØ¦\x000eL¼À´·ºG¡¢YÙ,ÏÛ]}-&Fô¯¸?úêfÌÚ½»¾º¿ûåçó<øÅ\x00154ûLe_êw,<²y±Ãóäv¦RÕLÏÃµÛ¶äìåØZþ¹	
&Þ,|	èp"´~ó\x0005ôV(õôhx±Ñ¬#Z%tÅ[K^ÀÞE|qû¦¾û·/¤àÀ×w·×goé6:pSó[Äåm<ó÷ÝY\x0008\x001fÉÒ[>m*5rd£\x0003ÿ\x001f±\x0015¨¦\x0006ït\x000c~\x0004öö,5r'¶.\x0013V_³¯éó4¯P»\x0000\x0002Zt½TÈxó\x001c)Àæã#±+ý\x0012«Çc\x0003=\x001e.\x0013>"lM")sé«Õâ!°EÕÆ\èOI\x0002 G\x0013\x0000ÞÈ\x001fµZ<6pÙâAªm\x0006Ã
ÃÊ;:\x0019-7oQ\x0016x £t2|\x001b\x001d%'þ\x0006°v\x001fpÓ]Ù3Ýëçå¿¹W¶ê¯oÏtO]
HehkÃ\x001eQÂX|1î*{¬«]S«n\x0017h-¢o[e²È^ôC¿w¿÷ädbô<1F__¿¸¼9\x001b$\x0017p}bék¾%RX·\x0019øLÊÅSDÎü·> r¦ÝQ¥L{½\x000fþT+p^ÃÀ»Ày\x0001'\x0002ïâæ\x00058\x0008¼\x000b_\x0016à|"ð.j^ËÀ»¨y\x0001®'\x0002ïæ\x0005¸\x0008¼\x0017à~"ð>dEéùÈGwÏz÷vMó+ò©o×³"zûv¥ò\x0015ùÔë·O\x001f,È§Þ¿]²zE>õ\x0002î|´\x0015ùÔ\x001bè® ?õ
î|¿\x0015ùÔ;\x0018î`8õ\x000eî\Ê\x0015ùä÷ïè\x000eSïà®\x001byE>õ\x000e£;\x0018N½»&ç\x0015ùÔ;\x0018î`8õ\x000e£;\x0018N½áè\x000eSï`8ºáÔ;¸«-ÈñÔ;¸+­È§ÞÁxt\x0007ãÉNèÑ\x001d§ÞÁxt\x0007ã©w0\x001eÝÁxê\x001dGw0z\x0007ãÑ\x001d§ÞÁxt\x0007ã©w0\x001eÝÁxê\x001dLGw0v\x0007u|}ýÛ\x0017@öýòÍíýÝÕË3Õ{ì²]×÷ÜWµ&f²Åèú\x0013ÑÁ\x000e\x0018Öû´Ð´;\x0016:XôC?w·ë×oÿü¦ÔÄÅGqú\x0011xrÏ ËWÒYDÆ\x001f¹çúþL\x001bÑÜÑ\x001fü¹û-¿º\x001bPìã·÷ÏyÑ`-B¦Üå¶
\x0014óðØQ\x001c\x0002ë6û§èMü°\x0006±io\x0014"z/\x0013p¾UèAÍ\x0003\x000fÚMRHÆ%ZÐ!·\x001a£}øEnd¯|KX2+~7·®~û×·¿\x0015¥!\x000fùýÕ»ë3iN· û
é*ûÅrÕ¶ä#Å#9ÿ¾æÎ\x0011¶\x0005]ÁÚ\x0013My¡÷&gòUþÐÔËA¢|Á\x001f³¶\x001a/rÚö#f0-¸\x0016a\x001fCß·@¼þ)_½\x0014]þ_ÞÿíÙ\x001fn¯ÏÕØÏ³hác¦R<m##½MN§Í¡ÿ5º®]<9m
FGk~ð÷î6ýÍ__½¼\x0016}'¿»|öÍÕ«3½C¹"$pãÉâ¼ðÙHe§lþà·Ú\x001a<éG«~ð\x0017ï6ýûW?ä~M?g×FM¨×F5`®\x0015'njr<m÷sÚôikÔ¦Û~ð÷îu3_ýðöEçÿ_éµ¸<×Yg\x0017r<b[\x0007Ó
rà°\x0006ÍSø¹\x001föúO[£9¡5®LG?(:G\x001f×s´\x0014y\x0005¶¤÷e©!P\zs¨\x000cÝA§¾¿ü³#è2b\x0012ÉÙE¢«CK{^ÌXwÝ
&Ôüôy~eÀe>D$zÚ%ü´Ýç(\x0014º¢+
¢\x0000
¿¶TKÇM@
:Ö8\x0017]M@dè\x0004ÐÕ[üX\x0001-ä§\x0000æ\x001eEXr\x0014\x0005\x0006\x001e\x0012E:¿"\x0000\x0017.x.\x0001µW F\x0013vë@À^s,t:ê±bsÒ\x0019;¨Xq°\x001fô-\x0012Øå÷¼\x0007O­Q=\x0013Ø}ÃÎÉ\x0012}@¶I'ï\x0003]\x0008ÝªmØ[\x0005­;\x0005<ÒËp!·»x\x000fÛMGÆ[\x00154½\x001dmú
"fLÝò°ppáòäñÙÞªh
<0\x001fQx§ªwm
O\x000bð(ÀÝEFì\x000eØÑ>>ßRvÎ±ç+*ùkt]CpÃO¼½ýîþRÊN/c°¾¹»zs}ÞQX½"3xëDh¥^\x0008JHñ\x0017õ	¼L\x0006ó\x0003ÑiÔ3Ú|\x0012LâJv«H¶YÐ¼É= V7\x000e\x0002\x001aD3*9IR4°=ZK°8\x0015\x0002{kGh\x0014ot3Z·G\x0006>w\x0019áºÖÿ®\x0005zÃ\x0016\x0002´A²KÇºG\x000e]1Ö­í­À\x0016\x000c<rSØÚà`º\x0019²ðëèÝÖöV`\x0017À\x0016B5\x0011O\x001fcç!R¢³Ú\x0002{ëKh¬U%ö\x001eÎ\x0000ûÝ:Þ-M\x000e½u&´\x001c`¿sEvuª]í·ñJ\x0008äØênÕ@
ÏNÀiÕû\x001eÿ\x0015\ô&´\x001aD§|bÚ­\x0000Ôv'Sç[kÙl·ae\x0007TÍàÕ~wy÷P\x0008pq1\x001b(ÎÖ4É+
\x001e(ª¶»\x001cL¾\x0000\x0017æ¾ÜÊz{ÈmÉ
Á'Ùö½:Á\x0006¾]Íî \x001d®Æ>:O6ð¤J\x001a²3;n\x0000\x0017óÁÉÞÜ\x0018Ö½\x001f~Ëî\x001dºüË_nâ_¾À¸s\x000fcÌ 1Ç\x0017yý
©\x0000)\x0002ò\x0014:_\x001fÖ¿>mzÆôHq`RD!áäìÒ`%ïNã\x0006.O#½\x0013EZ\x001aë¹\x0016<05¼\x0002\(\x001f¤:^Ëõ¨·\x000c_	¥2\\x001dkG§\x0011ØbB\x0001YAiÌk\x0004Ç'B¨go1j\x0004øfq;7°W5?$¶GU{Â>\x001bJvV\x000eLß>ûúöîùõ/ÿ~w¶y´®7ì1È}ñ·Æ¼M*6\x0016r{ZQæI\x0000\x001fÒùÙÕü£XKÝÜè\x0014\\x0001w+zHYä|ÐöÙÕ<µÈF<t!\x0006µ¢\x0000Éá°Òæì¾Ï®*\x0005o\x0013\x0010ÒÔ$¸Â¦u­\x001cì¦Ï®\x0006©ÅÊD\x001b*yRÂb;QLÍó\x00158õ\x0016	L\x001b\x001c\x0012¬\x0018\x0008÷¼Åºé
\Ä\x0016gÙ¦Jç\x0010|	Úb9Éyê`;B®bÉIvù~\x001b­\x0019õr\x001cÁì¾ç³«ñi±0ò¶fÇ\x00053y,\H°Íqò÷=]Í~¢Ý(\x0017åó³¢Ø\x000chsÙ7¿:#on\x0015­¹	£\x001a98*þÑE\x0018ûâ"ýSvËgWc"7{1B\x001f9	¶\x0003vó¶&uAÞî\x001f·\x0016Ç-ÂÙd2\x0016Ð1Û¡÷
½]ÀÒÂp \x0016èÚ!:æ©o\x001d¡éò¬ÐE¬ZÊFÐ?\x0014Á¢U7È[ó3d²6\x0017hqòj\x0013³Mb/ý"{X5VOYÜ$WÎÐÁÁle%º\x000bmLJ\x001b\x0002ïEÑæ@.Ðâ3¶&ÞE\x0014V\x001b\x0013îu\x001cé=	r`¢¥u\x0015J6Lh¡ó³gA.ÐI¬ºCë¨\x0015\x000e_®ð\x0019Ãèßs\x0015\x0017daóìçõÁ§Ù¤\x0014.ÐM\x0018)©»@ó¼\x001aù\x0015½\x0012\x000ci\x0008_î¹n3ôÆuK,w·ý(ä¥\x0005yöJD6\x0006íÉH[7ÏÓ\x0011}§Î\x0007ÅgTWpe\ót´è$äab\x0015jn.\x0002Ã\x001d|ïSÖ±\x001cA\x0017!Ý@¶z\x000b"3= Ç\x0013à±õüh×Ö'pYúnc\x0011ÖÑ¡åóE=¸SB#½ÑË]­Ët¼ó0Ó«)ñ iAÇ\x001b«kô]Fúø\x000f¸\x0002 ²Þ¨ÍÝó\x0005x9®{ôrÒ\x0010ëãmøóá\x0006}ûgp¡¢Ø¢ÐÕ\x0016aÐJ[TÛQïûâ<à\x000f¨E8\x001e\x001dâá%NS\x0002/\x001a³¶\x0003\x000f­ãö_ò:TùÁîx\x0011è\x000f,¿ãòç¹¥=\x0015á'\x0004£è{\x000fÿÇTKX<c<A\x0015?pÁN=v)²ú\x0003ü\x0003Þ]Ý\x001dÿ\x0000þ/·\x0013\x001aÁI\x0014A¢_$øÀ,;d\x0013Ç\x001db§¶K6ÈÇ\x0003ì0½\x001dû$ù+þ\õº½ùaèôk0cmÐmÎÇZÜ÷Î_l?£ûÉNôh-6Ø÷w\x001b\x0006ÑZö)
þjê=aû.Ý%È2jyY7¢7\x001di9NªW\x0002\x001edì!í\x001e¦Üáè=#iR±Hafv\x0017¡\x000f»§
çè=#'±f/\x00156Ø\x000eLS3*'%ª=Ï{\x0006ÎbÉAF)<4\x0004X²Ç%goÊô,È\x001bÏ\x000e±¬zÆ°\x000cºhtLª5BrE®ð\x0001\x0005]²çµÈ»\x000f_7·ëA:ü$ÈüÖ\x001ap£5ñz\x0005îðý\x00008ÇÅß\x000f²>!\x001cÄl3´è9t­	iÎj·À)\x0015Os²²G7Pô\x001czoË¿.àh8\x0017ÐW;d[Xs9°\x001eÐ×çâvÈ¶@;è\x001dì´¯(ÂUÍ&2ÛÒB\x000b´¸+s\x0011}n,Ã\x000eÐ
sÔ~â\x0002\x0018Í3ôvY\yè­`\EÑpE©¹â½Ý\x001d8C\x000bý\x00062\x001fÕ\x001aÒ/éLCÃûY\x000eùèºö@AÆ©¥  cD±Á\x0011g\x001aí3²\x0010hE\x001aÿÆªr U®!üTNóã³¢Ëg}\x001cÁ¶9n\x001c\x0003\x0005<\x0011ÿÀ4¹Ôòl×Ï \x0017ýî^oNmê­\x001e£½åz®_õä°\x001fÊSE&ùË\x001fé¾úhèJGÅÒãÒy0æ	?õQòSP¥Èh\x001f2§ªlr¢\x0017W
Üß~â¨áxîçóTPN×$rAö{ñÈ®+qL\x0003ÞÏç©*¡ø}Û\x0018G\x001c¾]\x000ekÆ¤SIÍªÜ¯È[qÐsE Ó{'ý\x0008ûQB²hMÍZ3 \x0017! Oq¿Ã\x001aúdO»X·2OàúÔ¶ÏäéÜÖ\}Çñs~¤AvqAÞj<lî6ryþCÔIA>\x0004%¥\x000c©\x0005Y\x0014¾ï0E0£r^¬.á©ëÙ$H­ÐbàTrczó\x0002Ý<Nú«\x0001ÖªoÉ|ï\x0017èíDq¥Jìþ@?GQ3\x001bçìïÑöräøbW	üáåäÅT\x0019X Xu,Wòx/\x0016[U\x0003\k³Å\x0000\x0016è­Ü\x001dK\x0007\x001dë¡4\x001a[Ã\x001aLmcåþQ^ ·³ÇßMÉJ\x00055bwX+©}Ò?<:|A´åt\x0018ÉÓr!ï(6IÐcìì>û»@\x000bA\x001f\x0007¬_z\x001dqe\x001eç\x0007»l§h\x0017h!Ð\³ÈÐäyÔÄ²ÇpLï~¸¿4²\x0010ëüvþïO=ãV2nû#2\x0019DÑ£T\x0011¥\x000bÕZ±:SÝð?ãñ¯pQæR\x0012Ç¯bF^ô(x\x001cSOZ.õ ²¾ð\x000bM,\x0014r\x0003»uðþx\x001cÑ[&§Ë=ø\x001dÎð\x0011Âåá«üí¥Ø>R\x0010Ëê;\x0012i{z§tk:B\x000fI ?îZ©Äõ
ÅT"\x0017ñM×®$<=¥¦qyß\x001doÍ;±5^fùØ\x0019jðaÁÎ\x0010[áøÀê#^Á¿àÐTVSsNø¢Nbnþ¿àñ/\x0004\x001cÔx\x000c6Ü®\x0016hJ7íÔW·Ýy.¶¾,:¹]\x001eòB´õÊ/Nù(	½z1¸vßåh7Z«\x001aè"Ú|
(P /ôØ½¾ºÿÛÇ\x0010¢w\x0018§uÆ\x0013O \x0013\x001a<I÷\x0004í09\x000f9Í÷\x0007\x0002¹¨De ¿1\x0005se\x001bFwÜ§°Ø\x001eÔ9#L%V1°[Ç¬\x001ff*Ï¦0Ú,fêU¿1st\x0015	N½-ð´9Ö<\x0015X$*c¢ôoBíù½jÉÝ\x001av³"\x000bE
\x000e½é-\x0018ß·\x001d¨X!%@\x0011w¶2\x000b²ÈTæ(=Ó+ ÑÔ\x0007ôÁâî®ÈBÂKv	­¹¨I})¨5GSQ|AnbÍE4ìÌ³ìjê¸Ï.ì\x0005Y(RÄ&\x0012h9P î`Í\x0015¥\x0015óäe\x0018ÁË\x0004-R¾:A\x001c£Ñ0­ö9\x0004´»"\x000bYÜå±cO	:/i°\x001d|iíØe\x0016iâI\x0006ß0µªOÇA®r\x0016Â0]\x0010±2Çùp:\x0014÷é(î\x0019¡Ë,®a¨«n\x0005m8'¶ºE;t¡ÅôIºQÜpÕO×\x000eeáÓ¨y\x001aË¼é\x0010T¥Ea-¢ÇðLìÄ>¸@o\x001dÁí\x001b\x0006r&$»~\x00132ºsê6#fF\x0016rc\tOb;r
Ö_©3Ó\x001b[·3M'KD¶tbÛEkÎÞ£ó ØÅ´Öìa£«Tï\x0005\x000f\x001e}ÂnRm\x0016èíHÓó'\x0002[ZtÌ\x0007÷öã|¼0íôÑ\x0016ccà³´\x001eÈ[¤OæðLû)ú<:ÓB\x0017\x001e%y\x0011§v+\x0001¸e$j÷:X3®ÐÁ
L ®A´~&c \QýÞËU-ÐB®*Ëa\x0015sY{Àég8\x001eÜ$ò\x000fKUj\x0016ªRdÅæ)ÞªGÐXÆdø\x000fKüi\x0016âO
<\x001aNÞx0y8(æXôñ\x0010\x0012M\x0014 üqæIäÒñ`ç	õµG\x001ah/¤4#K!%²ÒBH)Ä#\x001fé@àN÷ÑT>bÚ>bâÁ.\x0002:ÔÑXµA×®¼ä2
ÆG\x001f1%\x0001-ùñô\x0011}\x000bhòü\x0018\x000c>bÚ>b¢88\x000bO|<éðÒãS\x0011y(§£ÄG,^Ôª\x0002ã\x0011°«'»izü\x0001p\x00163Ayô­ØÔq¬qHXÎnl´ÙX\x0002\x0000¨ÅðR8~ä%@µ§¢þÀ\x0010ÄñVfcý\x0003"³Á+/:GØà¤vÌsúlÈ\x001c¡\x0016MñsÛÀý³?}÷ËÏw·g\x001aL9Ö\x0010è´,ýð±V9	ÃÍé\x001fó\x0007Õx¢j§¸yk»í-ÃåÜõ!(M;úª[Ãqg\x001beÈ¸
\x001dO"0¤¨ZÊ#Ïÿ\x0011-H¬Ýß
U`\x0012\x0000ÅLÉdf`ÁOÐOêÈºx`A\x00050'.N\x001aA{×,ªnòX9e'\x000eED6\x0007Q!wAÛ\x001c×»@\x000bÎùèÂÜÒ"ô¯â\x0017ôJKbq(>¡`×ÙgZ sÅz\x0017Ågp8ÒD\x0015ÙÓ\x000c\x0016hÑEa^\x0007ïI\x0005X·ØR\x001fv\x0016á!áØ\x0017ò\x0019l=ß\x0005zû-COB,ÈÂ£ç\x0018\x0017Ýs´\x001dì	YPÎ{bâr\x001aá\tTÉ3
`íaÏÐ^,\x001a:\x001a9¿\x000b£\x001bÉã¬¸êf»Á3òv<ZÅ¶T.¤¤V\x000cMu\x001b¹d«ã.ÐÛñh	Êp!w\x001a((Üûqà\x0003Ï¸åä}>:w8nì>D_Uí;\x0014¹ 	wÎ÷\x001a¶\x000bt\x0017ÐAf>éßÅf¦\x0018ðç< ëÑé¨Âzø ÊÃq\x0010\x0010ÁJ7,ÿqÇ\x000f'oG§n\x0010^L5Vcçþ)çó\x001eZ/É\°Ô¬&,\x000cþ\x0001zY¤ýóSÒH<a-§\x001b10ËßYÿäõÖ\x0000(~p\x0004á:v9Ñ3Ú\x001f\x001eØ£{ô¨°w©v#8ïýñ»ë3yS,;Z§¬ó8xyösï\x0017O¡\x001beÏWÚ_(=y\x000cÆD7×Ka4°+3=uðHô\x0018¬9\+²\x0008c\x0011nÜ:\x0013\x0001\x0019]µ\x000e\x00183zôf¦7@Ö÷\x0018FiªGSëbEÚÍ\x0005\x0016,ÝÌ\x00052\ð Ýî\x0007=w\x000el£¢\x0005;`7ÓRÒ\ÑÎeëé¨\x0019Õå´5\x000f\x0001\x0008×\x001dOª\x001bY½
×3,	\x0019ö\x0002\x0019pZ	¹`é³wã"ú,l_ÝÞ¿¾úñòî%_Çß_ß\Ýýx{}¶ÒUÇ¾õP|Y·?gÑZÅrYl¢Ï\x0015Ó\x000e¨9s\x000ey¯\x001a0
HþR0éêY±Áèø&a\x0011-P©±B OÖÞR¶Z%Q6Á£"h' \x0010Ð\x0007`ÏeÍ²Y0k;Þ´ä\x0005ZPÝ"N4Ù=5«vÝL~tØzE_\x000b\x000cA\x001d'os¿³b
¶È\x001f±Ú46\x001c8LzQ|x@þÎ
S¬ìÀ\x0001Y\x001akßqî[ÈÑ®¨,Ð¢¢¼Ll;Ö )ó\x001615\x0015;\x00189\x0015\x001b,§`Õ\x0014yHô{,\x00124M"=:Ó²¤P¡U'¤$Sp\x0005Ð\x0014´gX>Co6;,Ù`ÜvÐaÕ\x0011\x000fHT[®(Ö0ó`3­c¾!ðÊ\x0012OGCgfäí9HlÿE¯KÌjÍ\x0019å}¾£«(ê@ó![ªË\x0015ìÙK­a²ÜþdóÊghq\x0017;(m÷ûÁ5\x00064í¾Ø \x0019Z\x0014¸ä\x0016Ä¢\x0013$H¸â\x0006û\x0011ãD\x0007>º¢\x0010D_Q&u¸Ç¸Ã¢;VÜh%Ñ¬\x0004-Ð¢\x0012DYÜ CB\x000bmS\x0004ÙÑUJ´MôÑ:¼\x00019:ÌúQ4&ÏdEè£KE1ürÅ·\x0008Ø\x0011C=<3#o\x00171Ç$G^7¡<A\x001e7¶aÔ`×\x000b´(1ñQ\x0013;Í$\x0003Iè±âù\x0008ãI4fÏÌÐÛU$[-ÛÎZpôÈÓÄ\x0002ÏS\x000fçÑU\x0014Ãghë.Ícò±D«Ò\x001d´/¨Û-ÌY\x0016	SË\x000eªÓLA[èÓ¸+Æä	ZN1ü¯\x0007\x001d·sgf\\x0011».¤ú¸gÐA5ÅGõ\x001aæd\x0016ò\x0016d\x0011»,Ø'¬V
4{"ª\x001dq´X\x001bãafh\x0011btpY­Aöq]u
NG7EÌáø_\x0006\x0003\x001d\x0003®¬Ú\x0014`\x0008\x0017dQ]òRÎ\x001eÃ\x000e}\aW=xã54Æ¸ÌÐ¢¼DçWq\x0017òÄTßà\x0008ºa+\x0013²¨\x0011¦è\x0005\x001d.sÁ\x0013Í­`ê5¬fp\x00165B\x001eÝ. h\x0000\x000eõ¢ØÃ1K\x000b²(\x0011ráN<\x00149véâ\x0005ºü\x0019Í\x0012á\x0002->b©RÓ\x0011pLÉ£Ad³7Ã2^Æ³Ò§\x0016Íp$ÜfòG\x001fìÑÙÈÛÙ¨Í\x0001ý³\x0007\x0010j \x0018\x000bUdÚôªdk\x000cü\x000e%ÂZ«l\x0008ã¹%ÀQ*üÜ¢;T\x000bX/$ü\x0005Õk_\x0002ïXíQe\x0015Q$ôY(¡sFë÷·7oùùÕýÝâgæ×ÈePP\x0012¶Ó.µ©èm\x0018>÷GÏiõÂÞÙû»ÔsU9­D{¼eÓÂÊ\x0010\x0017\x001f{fÜ \x0019×¾ªÐ©\x0001"ÁÊÄv4
\x000bLe\x0017n8fU¥´8²\x0013-ßÜB\x0004|\x0006\x001eR¯Öìí°¿ª°¾\x0017ðÉt£}íØÕBk\x000eVVkA\x0016\x0011Rê3:ä§#ÁÙ¦\x0016ÃRUP WÙF®s\x00022Y'\³·\x0007ãÎÈ"B*\x000e÷9\x0001£»ZóQ®¢ª\E¢àBLcTûL®\x001aºÒ¦N-ÃÂVQH@Ñ¤íð\x0017ÈÀæ¡2·8\x001f\x001dh\x0011õ§\x001a¤ìÂ8\x001cð$$Ý¹V
\x001d
òö¿Ðíª,¥ñÕíý«Ëë\x001f¯_¿þåç³éi4§âc\x0017±
CÉ¤\x0000ed1>~Ãjáôýò9 ©"Ï2Kb/çþ ÃU°TF\x0011H3\x00155\x0016ä e­©-(i\x00190'7qÜ`~(2ÐKì+	¥rç@o¯Ú5#\x000b)ÛV\x001fA\x000b¨M¬\x001a2hÉÕ$`,È¡rl\ÅS\x0005o®\x0017\x0006
Ñ¶S\x000b°\x0010Èå²¯\r\x0000×Çf¨\x0015GËL-ÀB\x001f \x0007!29ö\x0002$`+:>óçÛ«ÍÀ"£êêÈâ$$(¦¢)(¶6Å4\x0016`!\x000e@Î¥HÕ2­C%½B$\x001eöZ\x0013´\x0014ÓðE²¬\T\x0012\x000f´fu0&Ñê£ë'Õ4l{ñ ­1Më\x0002-Òø\x001c\x0013\x0014±êr\x001a¥cÈÄ£\x000fÌê\x0002-ä4\x0008º´\x0005We!­\x000f¯§7ÍT^¡e\x0000\x0013ª¡\x000f5\x0003Q$Èqw£Â»O¨.ÐB©D\x0012gÚ£Ã
öQíàlè6ÎÐ²\x0000Ñà\x0007,V¥\x0013&¯]43ª\x000b²µá&`ñ\x0015¹ß\x0005\x000e\x0008\x0006§­Ã+°¸,j*\x000e5\x0013=ä7¬\x0005¢óf:uA\x0016²65#3Ý\x000cÄgZE^}hÁ\x001eã=CËtªÞÓH=%0¤È ¡O8\x000cÞ>º@Èû±Å¦½AhjM)æÔ)±ut\x0011lØr`>æ\x0002ý¶è®Öìlê,î!­Rd.ºl;\x0005ØªDP'rÎÑ5\x000céÐ.1ëEÙ%Lõá¦îÓ©\x000bôv
YhS¦.\x001a¦S\x0013!áN`ut
E:\x001bN½0\x001eNÍrh\x001eûBú5î¡H§2K_tÌû,_ÆP\x000eØJ\x000b´¨tÑ\x0017³Þ\x001c*WõÔÌ\6K­n9×\x0002ð
\x0002¥Þ3xÙ©uU©e?Ï@%Ox!µüòÿk\x0006m\x000e\x0005ã5
#Ö\x0012:×hªefõõ'a	Çôa¼\x0016Å\x0012æù­R>W¯\x001dbm¦*\x001d!\x0007@\x0016Ä\x0008
û 'ù9Â\x001doÁjQ\x0004dz¢¼p)èÃXÌÁÓË+¶I-j\ÖHVVX°C\(\x001a»fOËZE\x0002å^%rW5°Ü¡6Í³Úó\x001e½5\x0012\x0000B¾==\x0007J\x0004¦5spË
,ãPoç%gÌê;ìæÏ\x0019YÄÿY
ÙgVø\x0000`©lÍd*,¸²:\x001a¥vZ®\x0005YØ»ëºå\x0019\x000eeZk¸	!Ë\x0012õ.7¨°@ê¨srXC&ÿ¬A¼bÎÓEsª×,3\x0016QªUðÉðÀIê^·É÷=ºÂ­&÷FôA
2US×{ØÝ\x0008ÖO¯&zñ\x0016ØÒ\x0000\x0016P:Ý\x00013Ý+fº.Dg\x001eXh\x0018ÎE«®¶[½@\x0017øÀ\x0001óê²Ôª-R·Yï^±Þ¹uF9rK0
»ß\x001cè­´¾@7\x0001¥hY.N\x0010qP\x0008­z¼ç\x0006¡Þ+B}\x001e\x0002 ²Â\x0016`ð Ë$è\x0013ÒmF½WúQå\x0016©e6L²e5S--6£Þ+F=ØDk\x0018}Æ\x0016$\x0006\x0014Ëín\x001c>Rï\x0015¥¬ýd\x0000\x0005µØÕ¹nÆ\x001fo
èð>{}ùì·ä:ðÐ3å
\x001dVrzËhpZ§È¤¡¯ý\x0014ê\x0016t\x0010?H×e5Ì\x0014JK>)}Q<ÜÿÏÜÛåj\x001cW[IôswÂÿ\x001e¥ih\x0006¢Ð\x0008|mÜªJPwPÌTge\x0012ê\x0001\x0008h\x001bÚÁôS/B;ÑJÆÌ#âs,,.\x0013É[©\x0002Xdëÿ\x001d;g6þ¢[®ù\x0010Þ\x0013 \x0013WK¼\x0016Cä}9]?Ð\x0007r\x0006ä\x0004Åú6éF\x0011s\x000eGÿU·¾±ã\x0016À%ã»6\x000b~9M¤êZßØO;]\x0015\x0010¶k\x001b\x0017=ÑÃä$\Øä\x001c®õ\x001d¹\x0001r%×®9!\x0019Ì§Û\x0010vàvÀÅìÍ\x000bR´
FÌAËÃnucG>\x0005Ì*ÐuÊaXnò\x000eÛ\x0015s%ì°\x0013`)\x0004isZä\x0014\x0019¹ù\x001at;4hÐé
\x0003uWåF ;¤\x0004#±*¿6þÉ\x0017ù_à(ò¯Ç1^_Mî\x0018Ò\x001aÏ¾jjÞñ±¹I;hqpgr?ÀE»96bÓÉñØã¤É¥l\x001f\x0010pTÇ\x000czôÚ]Þ¯èrçæKÙç·O?z÷ZEé\x0012\x001b×ùæ¢sî¿`&P\x0017)ò(_T_×]¾¨Ô#c\x000fíD1à²
 EÓ\x0013/æJ\x001eÀç­Æß\x001b©z´âJOF~RÝ3{GÎtÏ\x0000²º'ñ¡m´Í+îzhïÀç¡ÝTÖ\x0012B\x0012Ù÷(Z¨ÚYfÈÍ?´wd8´\x000bY\x000f´8Û§g\x001e!×âk§ïÈèÞ±ÀÛb~;&Ù=¦_ÞáÔ®\x0001ñdQÈ"äÁ·~ ÂÑÚ*²ZÔ²ZT÷VöõNwhÐ;Õû
\x001eJêúB×LbJ¬äîw\x0007\x001fÐ°I:1×ÒÆM\x0012³9YË?\x000baÅÜÑ¶C \x001b×ÔäßãtYÛÄáïÐ°èú¤Ó4Hµï%\x0010Ý
ôwk\x0003\\x000f<Á ¬©Ä\x001e-çÎ=¼3Gÿ1s@O86( K^\x0005%\x001a+£ËßÏ\x0007Gi iØBå­\x001d§ÙÚ)ú
¼\x0007.øöd¢
¶\x0014¸X.H¼îòÒÙuHÆ;t¥\x0003\x0016\x0007»öè4=è»Oà\x0013V\x001eu1Ôh$\x001bKÕ¡ìîÈð\x0005[Ú:áó\¹ÍvÞðj7Ü\x000cß¯wlTmòÈ££#5³Û\x0015Õ\x0001
p\x0004¤\x0002Ë\x0013«¢©WÚÇwØ¯;4|ÂAkvª/²Ï\VÛ-x÷\x00053|Á1Â×krêf¢7ëÑ|÷	3|B5·ùh&\x000eK#Üª\x0003»¯Xà+NÊÎêG¥x#
¦ÁÍ±uWo®\x0003\x001a¾¢Þ×ô^n|þ3YmÎEa.w\x001f±T¸Z8âz\x0004{AÂî,w_±tH&U*\x001d¥\x0002m\x001f+Á~÷\x0015Ë$h¸kõ~$[4óõfÙ]ï¾b\x0004
^Àj÷^D^\x0006kõî#ÖLÈh¨\x001bíVì[$'ü"×Þ}ÅZ	\x001aèó]b\x001cNnSCm3\x0019¾¾D\x0017v¬ð\x0012õãþ\x0017ß\x000cº³p8î[z|i\x000ftÄkÆèôEóöÊÃ\x000b ?PÓªn?~zc"¶þr÷z<^\x0019üzüºF½H"?îIDÖ\x0012:'µùÚÞæ~_ì\x0017\x0006xræ ü\x0016ì^29ÖMÍ-Ç>B\x0013þ\x000b\x000f]-ï´:
»T~Á2-|á'\x0014ó}r[g`UÊæ*
\x001b\x0015ÔÓE~Ä±ü;9Äé
\x001aø\x0013b±­êKÚå?`¤õbÆ\x0004Dë¿âOà5Ú]ñâ\x0002ÄÐ=±û\x000f\x001fß½ÿáéï~z­ªuä¯UÛ|È\x0016«Âä)\x0000&\x000fáMéü×Â\é±Uë\x0018PA\x0002Zî\x001aÃÐÚ}:è\x0008\x0019^¯)~ÅØåßÊX]K\x0000Å\x0010B\x0017'> pg\x00157É\x0019²$8Q-/³Ì´ÈÕ G·n],\x001f´äé×$Ç¥ÑÊ3\x0016cõ:_+fÅ\x0010BWËQâ\x0005ÇÜ\x00006Z­=øæ%Åò6K©¸áÄÃE|îu]pãU¶Cc\x0019X\x0002e\s!ª1­-ÝÈô\x0016Ë\\x0015æsmÈÍ`ÊÀ%\x0019èpã\x0003R,QQÅ\x0003\x0013BWS¬­¬}V«ÜÒ×\x0003*4> ~ûñéùãóÓ+\x001dNu6jÁ\x001dIÉ¤\x001dØV\x0010ðk¡ªËÌ³I½*Aa2§Á¡y\x001fLÁª¾÷ã\x0001\x000cLÙY:5\x001cbS.#n½ÙÁ^Ï¦`\x0015ÕÕo¼Ð\x001c\x001a?Üzcñb­¦»gS°êa\x0010\x00132§d\x001cí*\x0007Ïr+u÷p
VR]9§«¤¬l
í\x0002ëmæ\x001bRM°ê¡7ÔêUyãgÇLÈZ}Ï¦`\x0015Õå5\x0003ú%L\x0019>Xà¡nüÛë±\x0017¬¢ºZðgSMÊ!laæ~Ý×R~°ê*Òaû\x0019Zú\x0006\x001aqòqc\x0007\x0015¬¢zØý:\x001fÐÙ¸?\x0016£z¶\x0017ÊÝ\x001e\x0004^Mè\x0015nñÕ	>ù\x000bòzNóæ¨\x000eVQ]{\x0017Påµ\x0015\x000e»13ÕPÄçÕ\x0004«¨.Ï
P\x0019³îx{Çá³Õ\x000fdØ	å\x00162%ª\x001a\x00175bðY5;r¥½R\x001aM4Y÷\x001a²éâ³jÕj\x000f\x0011Öp/CäÝ/þqàvæ_0Úi62Î7Ú\x001f\x0007òùä^llÔÄ\x000foÉ¢U³\x000b·\x001emQ\x0013¬\x0006¼jt¢Bt±ç¨qçU¥\x001eQ\x0013\x0008¼úeÐ'\x001c\x001b ]Øìn\x0017\x0002¡&¨þ\x0018\x000cºn¡È	Í5êõ\x0011\x001d\x0015ø`TàËT\x0005\x001b<ý\x0013UÜ\x0011¤8ôåïv!PuÖ«`:ªáI\x0018û;\x0019tòÙê\x00074vn%´H*\x0007ESm\¡ëV¬¾Û@Vÿ\x0006þHK@rvjvÅÞZyï¶\x000b¤åuQ£CL3UÓfzFêYsô/wè3\x001d¨ºL|ÞQ\x0006ÃøèÖM\x001càß!1¯¢Ä\x0015O¥¸Z`¢9=ÖuèæF\x001eËíK3°Xe;F#¸Åfc¬ºÓ\x000f
|®Ý³hï\x0007ýøñ\x0015ýò4²»¹Ö£i]S\x0014ð@Èªð5¾	©«Ì/±,92ü\x0001¿øc½\x0000û@>\x000f\x0015Õò;Åòóh/G`ÚT£«Äx 9dUo(ÇÝÍá9æÎ/éÜ\x001b`\x001fÈç¢ûñì\x0016!VÖrîFã1Nµ~ W\x0018swü\x0002\x000b\x000cÏÎt]Ëé±´®W\x0018'²vwBfmòR\^×\x0001Ü\x0001\x0018-Ð³*¨¡ü%Î¹î:VN\x001båuiÂâì`Í³\9Ù-÷+!~ OXÎh+(Èñ-\x0003\x001b©ØýÅ\x000cô\x0003ÆB\x000e\x0014_g#ë\x001fäÿÑÝøúÆ=ØÐñ2(®\x0011tdÉìÝñÒm\x0005:xWW]F í\x0015YÖ¼D\x00023ãuº´jùO¶\x0013èwï>þðáãk©iÌêe©äÂmËdç8UÏ=þz\x000eV\x001c¸XD~è\x001dë\x0014S©>÷ÒÕî[ÁíÀç©\x0005ìy^ÒEÔ
TcÜBL'©ZLâ¢ÎJ\x001dc\x0012¬a\x0005gé$ó÷©ný|>´\x0005tÙY¤NIgcÓÎu²ªÅ$.A\x0002É¾Y¡f6Ö!ådUI\hÉæ\x0019?_)TÐ\x0001»Y\x001dµ3*ÊRF.mvæ9^N²¶¬Ek
\x0008³\x0018¹ßÒÛcà%-ÊÏô¬Ü3¼
O<âè÷ØïÐ³P
9~<-Ñ,OwL9Üä,vèHÐØ_©ª1¡vØ*·ygêc\x000bRÌZ'Õótìø\x001cÇ©iÍNÈ.ªßüÕûOÏ?¼¹faBUlÚv»OÑ¨¨CåýÐ¾Åú\V\x001c{¤öÈÉëñ¶âÞQoYÎËùªá\x0007rÂÃ`\x0013uªtb¾\x000c?`á@í¤Ô¡~¦ÂPÁ?N÷u?NM¶HUg_\x0006ä\x000fàÉâ¶jíÍÀ¾hI²E*í;Ck\x00016êJ¹\x0019o¡^Ýî\x0003\x0019ÓXP_t\x000eãKäËEÞ\x001dnÀ\x000c\x0007_¡D[\x001b\x0001y5Ý^£ÉdåEW`Ì*éÅcfuÊ¶u68ád²õ¯VH^$«L6Ý[5}»IAßm\x0013<ú\x0012ù\x0010ªÑ\x001aéXÉ¨éÀ7¯= !ö¨\x0011r\x000cY\x0016\x000b«Ê±°mÛ£ë»\x0002ÙZ¥ÜÂN)1¯õ
×8¦J÷qÓµ\x00074Ä\x001e\x0019­$<\x001aÜãVØúG o\x0018¸\x00074\x0004\x001f\x0011ißòó\x0003Äî¯ØÆM\x0017ä\x0001
ÛEÛ\x0001:±}¹ü|Ö\x0002m-û]\x0007ô\x0019ôH&·j\x000fößê¡ÀÈ+2uäE\x0017QZ\x0014x«bÔ\ÕI ûÌnÊö>·bW_X Ó[zrñ\x0002i»ïè$«/ÒÕ[¹ÂÚë¼_ä4­¼@VÖÝÑ\x0017IV_¤×®ú\x0015\x0007.k¹wÌ\o\x0004ß»­\x0008\x0002#J÷\x0005¢»\x001cWuå\x0016¦v#Ö|à;±wl	]B~$~\x00198>m[½õn\x001fºÈâ\x00146:<\x0006Ms4J*7ê"ÉªèA?H\x000e8vÀAÍ\x0012V\x0012ën\x001fºÈ×ún\x001fºH\x001fdq(\x0005G¿-²d«ë)p\x0015k> AÂ4\x0006è\x0014S#1\x000e<jb7É¶½_\x001cádKT\x001dµÁm;\x000b%\x000ceÔG½]\x0015wè\x001cþÒQ_sØ\x00074lÄIBa¹WjÐÑKb0ô¦\x0007}·\x0011AµYí°Ü/Q5"«r\x0007ÏÇb\ië\x00072nÅö\x0016Êv*\x001bI7W\oaõ_õ \x000fhØyàTÈ\x001cuóÚÛt·ï6#êA·QMÄIÛ6p`SÇð-c\x000fdØ-cÅG\x0004\x0012\x001d¨Ü\x0016à*\x0007} Ã~é\x0001ÄÍ³vØó¡gfcYd]Õ w`PÖÉ\x0000¥ÅÜ.Èï­¥ÁËì\x001dËÃ(	Aªä)|\OÚtVc»°n\x001f!ÈÉºEPÑ9VÞ=&Hµ»¦¥Í;üû{ôïÿRô\x0014îg'\x0005«\x001dQôäæ0x7[iî\x0007ÿ	â³ÁAÔ%>ãéÏ®Í¬ýª®\x0014ã¿ûðÇwøþãki\x0010$cK,gî\x0004(M¥÷ê6	ú_\x0011«L)Xis\x0006´	õ4èM¦½+ÌòÏn\x000eà\x0000Vy÷CÇTWY1\x0002î¦¥?oÂþwÈÐ¸"·Í©^*CnÄ	H-\x001aàè«,w£±$CN°í9ps(³kuÄ.Wõ\x0000®¦61¨«{m*ë­[uígíFcIæb RÌ¯U³VßÐÚÈÒj¶pSM\x000c\x001byæÚhÓ\x0018ÒêÁm8\x001bÆn>\x0015¾%\x0012óÕvh¨*5´\x0017äÉ\x001cTç¢Ò\x000cû¤\x0005\x0008\x001eT»Õ´Ël\x0006ÝÝ$À\x000c\x001bE}F'í@ÒãÆ\x000c:Ý6u#¤·ÆL\x001e4É\x0014Â&óëx6u£$È\x0003äÈzâ7öQe·I®ÞíM\x00135ttÐÜwÁâÞ:èè&\x0001\x000ehlþ.Ôá%\x0007\x0007oCÃ¼ØO\x000e§Å·\x001b)$%"¡R\x0006±lüÕåITÜ$À<`Ð\x000e¥ÔL£Q\ÕÛÈM\x0002\x001cÐ°\x00113©NéÃ(?)ÚQ\x0017·µC\x0003o«)Õ=ÒÇÛ%±\x0004mØHNcr7JH«ç\x001bú´{dÃì8W+ÑFqs\x0000\x00072ìÄ<ó"\x001cLÄÌIÌùs©ÜuE\x001d×á¥+jÀÅ\x000b%ÜmW|ÊêøÂ\x001f0MQ3AuÍ:MúàÌíºf®U`}WµòÓóÿûjE\x0014«ùÍRÇÃ¦¢G\x0014M©Y)#ßD\x0011Äuz¼>õ^ÕóªC¹C[\x001a(ÕZù\x0006V{R·\x0012¬÷ê2\x001d\x00010u]aJ\x0012%º.\x0015\x0007,äUD\x001e~\x001a\x0017Õ(Ä´;dW£ò@Ô°<°=:g\x0005
\x000bÞè]>ý\x000caVpÂ"vªÖÀÈÅµ½<!1Ü\x000b1*g5uÑÌ<¯FÑk>*X[×Õô\x0008À»À$Úä§äÆPº¾®w`H\x000b«¡\x000eäuB¤³UL«E-®ÜÈ\x000c\x0005\x001aÕA\x001dù\x0015Æºé®8\x0005
\x001a\x000b4#¿´­É¢§0­Jâ×gvdØmrGD£Î\x0013Mí\x000f\x0003=ýúÌ\x000e
;P[O`>bd\x0006G
Û7¸/dr@Ã.ì2\x0019\x0016º\x000c¾{\x0005ú¦B³Csf\x0018\x0018qð\×Èy?}×û\x0015\x001d\x001aö¡ºÖÁÒLoÔÍÁº
Q@cfxRgR4é[íÝàQû±Ù\x000c\x001b¨C«ÍÇì\x0017Ó»Ðó\x0000ü\x000eáÂ\x000bd¾\x001d4èÌ\x000f;-\x0016ù\x0015\x001d\x001aöâ¨TÐ¨wê¾É´ßíE¬Ð$Jüi\x001d}p\x000bú/ø\x0015\x001d\x001a6ãÄ®éUI\x0004\x001d8z¯#ø\x00074$3w>éÚ£eÝL×E\x001b¾&Í\x0001iÇ@&çÀ9gÚÚ·Nf\x0007­¨­\x0010|PWæË¹ø5\x001d\x0019m\x0002©óPûí*'÷ÙôBÆ|£\x0000¿CÃN,èô¨R«Ì|/a6y¼Qß¡;ï\x0017\x0018´ÙÕ\/c[ww\x001b\x0011+45aéX\x0002[¶}¯ÆÔ n^Nf
¼åz¦A7S0«cµs8\x0015
\x001a+4òÝ¢Á\x0007J	ÅdÓû\x0015\x001d\x001a*4ÚÙ	\x001f1g³òê\x001fÒý
Í\x000e
\x001bQ^¤\x0014\x0019Î]í\¦ßC&§D³CgÚãTì`U\x0007ÝãæøHÅ¯£ìÐ°a»\x000c\x0013:Wä¸0Gõj¾¾J\x000b\x001dÐ°ªkF+\x001c»	\x0013\x00126\x0011§»µ'-\x0010ðÉÑ~ÅaÏÕßrU\x0016Ú¡\x000b,!í$;Æ\x0008
×i®®­\pU\x0016: á+¶å\x001fÃú×iØ\x001d¾²ÐéÆ­¤\x000f\x0016õÚUYèÆòq¶Ðt½4ãÙ©\x001bN\x0001Â8<þøïÿò¯ø
}çsd£Ð\x0016·iû\x0015J«\x0007që47vÎ/ÿ|\x001ezùÚç³8ëæT'r
nK*+iÇ\x000cýØMyÂËÉu\x0013÷é>\x0004\x0015ÉR{sàÇÐÇ
}æ>÷eÎ\x0006:\x0011[$¾\x0019\x0005xÙ­n\x0002¨\\x0013ÖcT2*ÉªÓÆÐéÆ|\x0006KòI\x0012£JÌ¡§®ÜLÔÚÒk»\x0011õÛ¡Ï\x001d\x000b)\x001cj\x0007\x0006±wÃ s;ôVý¾Ä\x0003\x001a¬UÓ\x0010\x0006ÝX\x0008>Ô1Í oä\x0002wä
\x001f1\x0000Ó@õx9]\x0011¨\x001aúv9ä;4xæÌ-Þ5°\x001fr\x0010£¸\x0011Ô\x000cZã>p/ÕÞzD6A=Ö\x001bGò\x001dy\x0000raÃUÓ®\x0010D\x000f+­àh\x001cîÐ°] D¥´\x000bR	-òf	îxo¸èIÎRkÐa2.{áâwh\x001e°°\x0007%T\x0000Ë\x0004åÖ22¿Í\x0005z#ÎÜíAô$/d\x001c®GTdhê
­õ\x001bUÆ\x001d\x001aö`¨xSá\x0017=9Z_É
Çî|=X&¨4V´ù\x0005-£^½Òàã\x000e
P\x0019:\x001agh\x000csZÛLÚï6!ð[$ôÀ
ôZß|²Le«ßùÝ.O·\x001dHç\x00188\x001a\x0013·µ\x0016o¬ÔwhØ#ÜÕlü8<U>ot*whp¡Ùóy0!\x0014MÆÊj±m;K\x001dö
\x001a9yâã\µ\x00018£
Ò<êu·8\x0012;4ÊiÁAªr¸¨cofÈùÆþ}Ç\x0005]#YÅ°_cÑD³¦\x000cyå\x001diÍ\x001d\x001a Ý(ìÅ\x0008îO®µü\x000e
Iq ùA3á\x0014\x0001Çn\x0016uY$6G¶sF+è¢+\x0015N&EÑMë@uLëwdPÔX-Ö\x0012	9õÁçiöö\x0003\x0018 µ+C6Ö%óo2ä­Åîn\x001f\x0016p \x0016D¬U\x000f-yè´ÞæÒè\x000e
ûP;Nä1­\x0019\x0014_ò	7S\x001bä
\x00064qÐ6Ô\x000e\x001fò¶	\x001cµ´øÆé\x000e
ÝBª=×`Ô¦¹Læ¡ó:<êÝN¬Ð.¤\x000c\x001eXÓêçE£,\x0003ÖÒ¢
9ú¨;4´\x000c¥á\x0016»hËãÓ·bW½Û\x0015´å\x0004Ö

EQæ ¯m*0ôê\x000e
mC¹¡V±®="þg;\x001fkéÕ»XÁ
J%!a\x0018aN¹éÍ ã¶@îöbÅ\\x0005ÛTªql2\x0016V-¬ox·\x0013+ìDU\x0004º\x0016îÌ-ðÊÛz1ëÝN¬d\x000f¼<Li Tü«K¹¦ÝmÅ\x0006[QIôð
i\x001b\x0010\x001f¶ßJ»Û/
ÛëlJ&^\x0010&>ÝÈHínQ7ìc¹FyçÒv1^õ=EíÃü÷ù×ÿýç\x001f~zúø\x000fï|µ<q[22G\x0010Efò¿­\x0003æ×å\x001aa~\x0019íÅÌL=Tá\x000cÖ\x000c5	-\x000e·¿ý@\x0017Gí\x001cæ\x000c\x001b`ÛX$ø<Ì`Û1³VG\x001b­pÚ\x0013ã²\x000cÛß~ Ã{C¥èZgmÏÐM$rã\x0006u\x0011
UæsÈ±&î@\x0018UìÓ%b\x0006Û©\x001dðÊ]4\x0019æ$i¹ßøAY\x001by\x0016$)±\x000clÔdcs;Ü\x000f`xiÈ=\x000b²õ*qG©¦Èub
\x0016ºËð\x000c¶ÑS%{a5Çb81)òóHÊô\x0019Á6zfµÄ[·2´ý&Â	¾ßå\x0001
\x000f
õ1(4ÑÄ~H\RÓö)ÁöyfelÀL×ÀÝó1Å\x0011V-×sÈ²ê
\x0017z¬¦ñ5±Na¨['Ãñ\x000c¶Ó3ÃdÈoç\x000eÒh¢:ª/ËwàÂ&l\x0013Uc1U/¹Ïø\x001bõán\x0017\x0002 \x0014Mà\x0014\x000b?C7yS'\x001clgPzÀÎì¸]MS\x0004å´âÝ>øâw/«î9?M\x001dlg\x0018\x0004Îþ¨ÏR\x001e4§ôäúò­.wè\x000fþÑo´}kÑ\x0004\x001a\x000fùyê`[1µ\x0007\x000ebö8"×Uõ Ëæ¢y·¤1¬\x000fQØâ=pZkÙ\x0004äºò
¶³Qö\x0019*dÄ:y#ÆF¥© ~f6ØöCÍT \x0002s5æÏ±q\x000e\\x001e=7\x0019Ô`{\x0004\x0005\x000f¹Ã©V\x0017»YÖê\x000c¶O{QÜ¹\x0014Ã:.\x000f\x0000'\x001f\x0019l»^	ïhDÅ'»¢hªÏO\x001a\x0006Û\x0014§>Ûp)Fõ8£-Ãë#\x000c¿'î\x0000Fkéï\x0001ÝÆg;1oæw\x001f\x0011o¥¡²¼YL×áùË6ß¼\x0010î>"&ÉzÂ.\x0010	b¸á.nNîPS\x0001A}\x0010üî<\x0003þðüôüjMY³±¢Aïó¡Ì¢/Æs¹èË}\x0005T¿×Ìy
hÀ{¾ÿU¨³\x0012\x0000P-ºçár\x000fd8[\x000c\x0008ÀsucCù; z.«ø\x0000Ç@l(( ¶«´Û\x0011yîÍ·\x0019<¹ø\x0000*\x00085u~\x000cÁ\x001a½VWDð@®0Í\x0013ä7ä/­Ur\x0002§dÔ¸q\x0010Èö1+ÌD`\x000e\x0016\x0003x¼Ã{\x0008\x001c¨g\x0008¢±n'Q56ÆÌÁjÆ½¯4ª#uíC ZH­æ!\x0017\x001aËF÷QÜÀ|\x0006 r<\x0000ß«vc©4+\x000b¾ôÙî´®²}\x0007ìº#0æLÐíû\x000e8 a÷Åþ\x0016f£q\B&vöí3ø­^\x00072TàG[\x001d\x001f\x000fèñ¶R\x001d-0Ù¼ÏTÜwÀ\x0001}î¿\x00140°¤xÔFôµÏMUün@¼\x001eµ»?ÃTGz
Ávo²ð\x001b®\x001fÈP&;\x0011DÖ«DgÔ	8\x001bÄ\x0011§Oú= a³\x0004\x0012_FÂæ#ò|ÔèË²\x001cÐçvI,X®æIdu0Å8î\x001a²\x000edØ.	õ$\x001aåþ i>a)>ãw\x0007h}YÀ¢L\x0010:;\x0002U`d¢Çv1>2±0âÄ{ÙàÓu7\x001aÚ;ì¹Uâ@£Od£t=\x000c¡säU(wD´q \Ë\x0003V]d¦\x001c¤Ì4ïe=¸\x001c\x0011í\x001dú¼«¢¶±ã<3³Z¶
³.G\\x001d0×÷Å\x0001Ý\x0000\x001aÛI4»V)eTf?÷Ù}îì<\x00009\x000cUÖ é\x0018µðy×7½¶»e\x0007¯\x000bÙ®PË¾ÎôÜé+3Ü×Å\x0001
ë£\x000e<¤cb³ÖQ¸é£E¼¿>.\x000edø}Øà4ÅGgõ¾eò®\x0003\x001aÎ»ÝSp.{Ñ\x001c¶!7äöÔüçÅ\x0001
RØ\x0014Tä
ÍÐ¤´2n××Å\x000c¯\x000bÕ\x000fGÁ/Uä'd~\x000b´¤Ï¸føíó\x000f*Ïðç\x001f_©\x001eP\x0003ËÿÅ»Ý\x000b=\x0013=¹ª¦+ò·àEªÂ\x0017\x0019\x001b]ÚCCÕ9-§\x0011S>\x0019Ó°:±\x001c£q£Ë°ô ØSw+î+\x0019\x001cîë\x001fÈØEQÉ}$7æÓU6ÉUÝy·\x001c0.CUÁ\x0007hsð#T¶$\x001d#òqõ\x0019\x000fdì¢(K7ü\x0018r*ä'Cæ\x0006/=fÝzÀ0Â\x000c«¯\x0010¦Y\x000f\x0015ªÄËU@\x001f°l¹cj\x0019R\x0019O)FÓ4x?î×\x0003v`è+ÔÞ9âÆ&æz\x0010ò,çÅ5wUàÃ&ú\x0005s1
S¯²Û¤|¿àËïÐØV(û\x001a\x001a\x0006ôV0fÑnª\x0001Ã\x0008>T5±\x0005k8\x000cYÊ6\x0005éAè\x0003Q|°\x001f\x0013¾*5]\x000e[K¬7\x000fÃ(>¨o"äNeÙE;Õf>òð{ÿ\x000ehèýäò\x0012kc:æeyªïzs@C^°ÁK²Ðï(Ñ3ªÜj\x0017¦ìüW?ýüôÃ«)ÿÉ
ô½\x001e7LiZ¦\x0003ñ\x00009³æ·(9×¥ñç\x001b×£QT 6a%Mûc(
\x001b~É
Ó½+æ@\x0006\x001dý0jEéYA6ÓXØæµ³$\x001aIõ5fÈ÷]r\x0019ÇÌâ\x000f#ûJ½Ñ\x0008o\x0012= W43\x001b/É}ËÚ\x000c3º7Á\x000cª#-bÍa\x0004ã÷¸¼\x0013ÕÃÛ»	\x000ed\x0010\x001dI$]ßõùLc6ÆaV_\x00038\x001añó²ZfAc£e£IÓX\x001aZ9jÞ]p #uND\x001e¡°\x0019P4mñ1,j¤Ób\x001eüùÒªÐ\x0019[z#J³u\x0010ß-hèï×Gãh22Ùa¯^ÛCw\TÑÁ A>à4.\x001bõ¦¹ÉÆÜ­gÑ§xQë	K£\x000ev=çNí\x001d\x001a\x00164&õÖ 19]Rêf=·\x001bÁÛ\x001d\x0019\x001a\x0019àVIdd¢&¯fAÏ\x001bUÚ
\x001a\x0005i2õMÈ\x0005ÀVê³ÄÐ7õÊ\x0003\x001aec
ÁuGZw¦)-,\x001b§}xGõð½(ÈæPÓNõ¼iòÝ¡á#Ê{1G\x000c\x0012ïÃp£ºCÃWç\x001b>J\x001cÝnq?¡°Cgø1"óM
«;+Ü\x0008ôMWë\x000eà`"sÞ\x0011)ZTó¡\x0017éÈQ\x0007Ý¡ÏÏXÇ\x0000]2bà\x0005\x0012ÍÝ\x0012C½ÑðÜ¡\x001b@\x0017:N£QÙGÖdè<à>\x001e'*k
ä\Õ«åÕÝX1ôy§ô\x0014ø\x000fôHÛÒ\»u¸Ûò\x001e>\x0019øÔ¸1Ô0ÔæLb\%òþä.=b¨Ë:Ü:5qºÈ¬Ë·]îYõ\x0005üÊøª\x0002ù$§\x000f\x0010ÆôNò\x0017¦()*wUä;YNôh\x000e°u¢ÿ÷ÏOÞ}¼¥ýÇ\x0010+Â\x000fé\KoÍJZ\x0014ùÂLMþ\x001d¡½mô3È÷.öf®¼MîîÅßÀ?`@ùF>õV\x0017Á\x001fÀwÈÖ@Ù^ø\x0001Í|½?zÿeZK©Ýà9Km,äã\x001dôáó§¥úÝÓ÷O\x001fü·ÿïD¼ô<älÛ²\x00148ÎR*ÎÅÖVðËw!¯fPû\x0016º\x001eþ-\x0017ê\x000e@WÍ-GÇPf[Í¸åe¯Gÿ\x000e\\x00008!zlÎË^(1GWøó\x0000>\x000f~ÕE\x0004í¾aªÌ%G>\x0015Ô]Ê}UìÈRÐïW{ÞN\x0007ff¥Ë\x001c|ó50ØÏÀ ÇJáLÍ\x001c9f#À­\x0019\÷U±#¡vç[_ÝÁÌ[Ë\x0001©&ß\x0008zWEWò\x0005\x0004Ú@A\x0013\x001dX\x00150v#/µCÃªÛ\x000eÈW£6#:ÍtÜx*\x001fÈ\x00108vê\x0003\x001aJ¥\x0018½1\x001bC6³/¢y@ãs¶acnDE}µvèùáÿ\x000e
£Þ\x0008`æ5Qlj\x001c&_r\x0007Æà_syçy\x0014t¢\x001beì@·¶('øß¡1llX\x000c\x000e#-ÁgNôË[«\x0013ýïÐ®³\x0004£\x001eF®T+O\x000c½ÉsÞ}Dþ\x0003i)\x0005Í\x001c\x0014æQ·z£Ä³Ccô(oj_Cqp¡2·u\x000b;Ñÿ\x0006Ñ¿Än%ÿf\x0006Í·cî+\x0010rÿ\x001d\x0019pòF)¡Æ8=v\x0016YÍ}ÞX\x0003ìÐð\x0015#iKÅÄ\x001d¬E+µ\x0004=¶\x001aèÝWÌø\x00151á¡üIÎÅÎû%oÙ0GÁ\x001e°¬'.kÙÅD9e]Í¨£_OÜ¡ÏzbQÅ\x000f¨ë\óTö¹\x001e.[ñÍ(\x000f-P¾KÏ<\x000fKîkí]ûn\x000fhxÃ±
\ÔDJVf$ÏõÜ
¬w±À\x001b®\x000et"×r\x0000\x001e¨2A¬.HòzX\x000fdün\x001cöb\x000c÷'¯Ót®ð\x0015+6mÕ\x0000jö@UâýêÑ¹û\x0015¾bÈÏª9×b¼\x0019ËÞiz÷\x0015ÏÍR&«¦©z::ðµØâÚ×ÆÊ\x0003\x0019lÕz\x001c4 TÊ\x000b­çäê\¸«\x001bôî+V°÷í\x0011\x000b~E;	qÌ×GÛ$õ®=;r¨b"ÀìP^L¡\x0018úÎ\x0012ÿ¿ö\x0011\x001eÈ0ÑJ¦<W¶|
öà©m[Ü{\x001d!5½Ä4¬lý5¬^X\x001dÝØ\x0011á¼ô\x0012S÷OZÞ)ñ@þûú\x0005/üÂ?¡¶WpÔNKÚ@,!!Û~ãûß \x0001Ã×+5Ýÿø'¤tÆ21sKèL:©I}á3Tþ\x000c2K È½LGð^V¯rc6·bÂ\x0017æ(ð\x001cõLkï}V½4^XH\x0017RëH<sß\x001dð\x0016ÓwÛú
/Ì\x0011goj¯h¦:\x0016ø\x0007¢!Âj[×ú\x00037ÙÇß0Ù\x001bU@{-Ù Æ%ÞX
öV\x001d\x001aP¶5Úw?¿ùÛç^+-1M6µò\x0010GS6rÃ÷E\Õ_:-!cÒ]òçI@Ù^ëD\x0012BàÜâlÆy,¯Å+\x0005![×kA¤¥^S5d2å/¥u>_ù\x0007Ùz^'ÕÜ9o\x0010MYav-Os])W\x0012P¶×I¢\x0002HRªo2=i'«¹©3usI@Ùz^'íûÄ1O7fçLß\x0014­çµvæ|.óý2dÚ¦W®N¶îÔº2Ðê¹¼¿ü)Úõ©.±\x0016R­ôÑÇýîÓk\vS\x000b7Älê¨«\x0011\x0007:?ç\x001cDO¡S~%õ@ÕQ'RBü_av_×Ìé
èètzó×\x001f>üýß¿%\x000e\Y$\x000emêu±
RoEµ\x0000õ~ûÅ\x000f¨ÖÒ4*éíÌ\x001c\x0007ê ªâ\x0016ÚvÉ¿Å\x0012òc}\x000eÉþRä+dGÎ)òµæ¾#5÷ÒÛº\x0013\x001fÈ9Ú!± `7±
\x00192c_5æëòF\x000eîwÿøî\x000fÏïuÿôôæ»\x001fÿùnà¹E\x000bTg¸EüxmÍßÂ#]¢/Zà+¯:¤'	æ\x001aU|¢²Ý7÷°4Ü"÷ ÆÎ©W<9òÔ^\x0019w}[\x001aî×"_³ìÇ¹bY¼ÜÇ4¥Nã\x001cë&cp7Ïh¯5\x0003Q"3wOÔ
oñÎ_+X¶eQ/ÚÆ:i´á& á8X¶eQµûd³Ý°\x001elè#±Åðù;m¹ \x0003|E¹\x0019,´!Sß´F\x0005Ë¶\`=B1±3=¯´àK\x0019\x001cÐPá	(©ªf¾f®Y4-*AÁí: añ)\x0016ÐUðK\x001a\x001cèöË\x0003ÃU-~22ª\x001b%2jæ'÷üòÀ°R]¶ÌÀ\x0003Ï\x0014¦
TÜ\|êÀ\x000cE%\x0011óë§¡'Ç\x0015¥9Å\x001d\x0019J\x0013ýùªês^	¦C \x000c_Éà>×ÇP*(X\x001aÅADßRXÊKE$n¨A\x001b4\x0014\x0007Tt¼à¨\x000b=sç¸~S\x001cØá\x001bªüP¡³x\x000br\x0016DJö{\x000eèó#\x000eMÙÃ±§NüÅ\x0010\x0000óÌ^Á¿ZÛS	[?~þçw?ýôj]\x000cÂ85Ç¬\x001dt\x001dÓ.¯ø-.õ6ãxÊìgõT_H\x0018°¼ÿ¨£|\x0004j®	cëúp¢VÛ\3k|Î·öª×Èv\x001aýõ|>¬% Cªj\x0012(	0Ø'\Æ\±­\x0003ù|:­Ü&9\x0018·wÖ\x001d%ÝDÃ¶·f\x0016búÖÂ5F\x000bÇ¦w\x0007Ü`*°3CÞv\x001aÒäó\x0011])­{½\x0019«m­ðîÕì)	¸Ê\x0002\x001dc,\x001b\x0018'z·5S³Õçxûä\x0011\x0003ºØý¬ÚÆÙ
\x0012Àë:#\x0010Ùèû^|'Õ\x001d\x001a²\x00003OLÚY8s°zaß°ïv\x001f4ÖÌ\x00160SkCóÌjG£m\x001ecw»\x000fÒ\x000b³\x0019®,e\x00164\x001b¨	2è-sq·ý ¯fjæ"Á\x00197Yþi°¹¶lìäËl\x001dÐ°ÿZ%YþÂ´5Yw,Ö7Ï\x0013'¬¶eg\x0016j\x0010¨¡±\x001bÓHt«®¹ßº@Ã&\x001c\x0001åä¢¢\x000e:Qïë¾uâÓj»f!©­2ä+£¼ªs¼{Gø´Î\x0019i®­\x0010Û0É¾\x0005Õw[\x0011Z÷gM¼_OÁÈféÝpWª	NeÈ\x0013ÉÃE}é\x0018eU\x0000AÞ8àw;1áNÌkf\x001fcN¬b>
ë2K Ôü¸·¸·\x0005\x0019tædÕ\x000fÿ¸XSY×\x000e
[qL_Ñ¢6íÑy+ê·ï\x001fÐå\x001cu¢& ¢\x0002ø\x0011%pàýV\x000b¤ã×µC×\x0013ú45ÙÀ`\x0006VèÜ·8@Û	*û\x001b×,\x0015ê¸5­Ù²S6Û»MxúLÈ\x0007ì¨)¥SAJ½u*nú\x0003ªy\x0004´ÐÒ[7:\x000bIÏ6ùûÅ/t¬ºvä	ßmY´\x0008Ïß\x0015\x001cÇRÈq^\x0017Õ¼.ZP\x0016<ÿ\x0003;9XL`·\x0008S×\x000e\x001dá#6T\x001cÓClY$²´/Áv@Ã.¤~]QÞ¨©b=_´ë6tlºvÜ\x000c_°ÀTTnÖÝ\x001cÏ» ìÝþ;C-\x0006Ò+¬ª<0pÈ)ðzîK­Û±ÿÚ¡aÿÉ¹	­V.«ÙÌºh«\x0014îp°vÜs\x000bÆH^!\x001a£k\x001e)¼Ovµ»-a\x000b6t¾©2hsÎmY	Ýµ#\x000f\x00184¥Ä\x0011-l ·\x0016.Ç±l¸4P\x0017²dVsg\x0005½±Â\x00027¶!¼1Uõ(ºÔl#^Î3.áWÇ
mG\x001d8#Jó©v\x0019F¤MuðÍòðM&\x000eè\x0004.Ød+'ÐÛÎn<è\x0008s·\x0007OµWð©Y\x001b\x001dÐ×½2\x0016ùÂáºíÐå/\x000b\x001c\x0003·\x001d\x001a¶a\x001fÀíW\x0005\x0013:$¬dQÈ\x0019Ö»Â¡ÑíÐ°\x0013\x0003¶%V£s-óQhOU@¹ò\x0013füO\x0017ï>þôüéÓkéçir~³\x001f\x0013K	ò*Hÿ-*U^Éé¸g4ñ©¾ßÐÿ¼\x0016VkÍ1r\x000e<F?< Aç¾ó¦r\x000bØ¬ qN¯n[Þ\x0011Ý¡Aç¾6"Í\x0014ãh)î§O\x000fh°X\x0018ä\x0006¹x\x000b¤Îß¹Û¯ÌáGN\x000748!ø«ãÅå\x00068;4H5)Myâ\x0004â±«\x0006-'9çô;+\x000fh»H
\x0005\x001c\x0017)\x0002'¤¤næÚçV\x001fÈ \x000c£DþH_4:á·ÊWìî½~@~¦aé\x0019{]\x001e`äy#\x0004»#ÌJ'ù8-dÐ{¿LcU\x001bÃ\x000bÓ\x0006
RMÆ¯\¡)J­ßªâÿ^ÿ9\x0003W÷Ø¿ý¯OþËß<}þôJDØÙ+b«ö\x0018A¶3Ï°¹ þZäd8¥\"ñ\x0008³ºÝ7X/Y®\x001f¨4¤rSÊ;r\x0002dLüæ6I\x0008J½Oè\x001bMô\x001a@ìÀgñr\x0019«í¨=\x0012iP;BèW\x00107¼£\x0016\x0018.Di¹çHµ£ÜXá,È¼¹,­\x0003ø,j$u>HeÄÌ
Ïuf\x001erZÇCÝO\x0016dtÏÚ
»F\x0007y®HÊi¥O.\x001ag\x0017Xîuþ]®ÍMwgq\x0013\x001e9¥\ÐQ:Ç¼[2ó\x0010²¥\x000c\x001dJxä¼¯ê @J!Ï\iÒ\x0003óçXoÒ³;ô¹o6õ\x0007CÝ¡ÏU§Âª\x0019F\x001c;s\x001eäâkwýn\x0013eù3=+g#óÈÔ*%ÏäÕ*å$:wèsy¨]\x0002èÂ©=YÍM¨óÜÝ ÏçnQ9@è;GÝ\x0003\x001bÈÿcÑ\x0005Å\x0005_ÿÃù!\x001b\x0010Ëe\x000cR\x0013\x000fÉòë9N'Ô\x000eÃïT¤ç­_ùo>?zó§W\x0012\x0007,ÍöÃfí÷Èóÿíy\x0018!oÖðMôÁcù\x0012^°L¹m&_^¥*Q\x0004°Ø5\x000b:Ï-:Õ·\x0011S`E«L±û¬»aôÁÖH¨¥´^À]£q3\x0017¼\x0003>·þìLXLMõ\x001fÂ\x001f6ó¸;äs\x000fMu1Þm¹0Ú.µq£ZL¾"Ô0òà\x0007}ÐÑPYéÌPM
÷Â\x0019F"\u|±4:\x0012We4nµC®î3Føâ[\x000fþ~Ô\x0010Ø\x0002«\x001eË\x0007ô\x0015¡Õ\x0008W®îl\x0018ÆMå³ÌÆÍ7­ÛÃh¯®\x001dlîHÙHE6¢ÓÝ\x000e\x0004¾ÚH»ÁF)'º\x0019E<o´¦Ñ\x0008U7H¨(\x0019NYíFâ&Õ"æ0\x001aájû@\x00127Z£BLc·Ì¨ïGÿ\x0002Þ¡a\x0017FìU¯XçT+KÄ\x001cîpF~\vK§sõ\x0006£ÍÂl5	áµ\x000f+?.?\x0000î\x001aD\x0011\x0013¬2\x001dÅw\x000b:a\x001fÖôüÑØÒGë\x0005¼>j¿£ØYõq9T±ð:öÂ4ì\x0017sxáË\x001fÐ\x0013Îè\x0001½JªëÎ½Juðs:¶Í¶ün+\x0002ÅnÎDÐI&E]çxBn²D\x00074lÞ0{;Zfåã¹]4nþ\x0010\x001eÇÎÈy¯\x001ae\x0014\x001a[OÈÚ3×a¾÷\x0001
w\x0000W}FO,"/Ï\x0019£ÐpS^\x001bFÎ»(=¦ r7ÈÝ,¶òOÑU<:\x000e>ê8Ó*z\x0019¯\x001a\x000b\x001b7\x000fÅ­©Åñ9.\x0003¯AË\x0013Ý\x0008\x001cÞLî!RGl'[®¤¸ß<¿÷ñ¯ÇMÍû
×÷L<n âe!}\x0004¼O¾\x0013'Ã!å²\x0001ÒÚ¹àRÛ
Ù\x0018vm¸¦ÿåÄÕNÕ\x0006\x0001®&\x001dÊ
½jðî\x001eÀàí\x001b·Jé¬Ý¨d{4Ò6÷k^±XJ|ZÜB9\x0019S½\x001c¹ÖÔzñ\x0005§%ÅUæ®åJ,UuÑaHXÇà5_Y,)Næq2äÝNVo9\x0019ûÝ]Û\x0003\x0019|}\x0013iëèRÎ> \x001baË6n\x0013[±¼8u\x00128XþCWYU§D\x001aóLnLy OX\x001a\x0003Ù\x000bòÜå*¤¼¼	¹o\x000b§=®Xb²Eá½¡îD¾ÍÙmË\x00169ÓÅ2ãÅ6,\x000e9¹'/h®ö´\x0011Nç]±Ô¸º·=ÖÝ°SÍù¢¾I\x0010:ÓÅRã\x001a\x0012a}Î|Ä\x0001IèòÓÕW,5N9£\x001d^[osÔ«=n2Fw\x001b\x0011M(ûÀ\x0008-ÏdLØ+;Eö\oL(¥Æ©\x000b
p\x0005s'\x0007åÈÜbùÑü\x000eÜA\x001aÇf6¹{OÍ\x000fÏvh,â	íÀy4^Ói\x00063\x0019«$áÔð!Õ\x0002o<¹T:Dö\|q¤\x0003\x0017,\x0000ñ²NÑÔ\x000c%n{}9Å»b\x0018UÚF@ª½\x0005Eà-X²/t@\x0001`ë[)µ«µÇçhé~ïÃ\x000e.ZvK\x0018ÆQ5ñÂØ+lw\x000fM\x001cå \x0000gÖ´Ð0\x0001Ê\x0012·tjwÅp}Û.ÄÖYÇ'A\x001bÆ¤\<\x0000&\x0011?¼ÿñÍo?<¿ÿ´rj:þùãz-õ÷Ìî\òmÓ#¨Þ\x0017g9eÌoã0X4\x001bòEÊ\x00026è÷ÅêL~ëBáo>|þik+ýï¾­ö\x0013M\x001f³MoÙm%©kGÃk{Ôÿ\x0007Q&®sßº	µc«\x0018ªéýõpyfòä/Õ¿ë^Ýq¡»^Y]p[ª\x0003	:d®AöØ}U\x001d\x0019ÍåÊ*\=(·ÝX\x0000±xv\x0018!º9Ö\x0003\x0019´\x0017ÂÖ\x0010w «m$ÙØ¦÷^ÜÚÛ\x0006p\x0008ÙVÆrF®ô¶´¯®Áå\x000c.m\x0011µ3JhäÇ^¦9lË]ü·\x0001£ñ »_Ü\x0003~¶#Ã\x0007Ì\x000eÛ\x0016\x001b^5\x0017|¸1óÞá\x0003Ê»\x0003ä1s	ìA0«yî§£\x000ehçºÙÆïÐi\x000c#DÁJ¡ÍöØI4<4%\x001aÔc\x000e\x001btY±ávY{æ¶Ó$\x001aþþÃç?¾{ÿôÃk¥\x0019\x0012û¶\x0019ó\x0019SÈËô$|º©ÿò6q8<«mÛ´É¬Ún "¤*rdæjÚ4Û\x0018.ñà@\x0006Ø)×ªrEÔ°\x0014Ø\x0013Z]\x0011\x0003\x0018Ì\%º\x00049º¢-~dG^\x0001înMå@07xÞh=é\ß{±m´dÇ\x001euÚWêÍÂxqQ¹OÉ\x0003\x001a9]ËÜ\x0019\x0003ç¶Û\ð×÷Þ\x0001ï½¶ÿÇ¨':ÜÊ\x001f&3rAÞ\x001e©w\x001f\x0011ßdJ4Edn´ÕcÄæ2»ñÄ\x001eKÎ\"ú\x001f«H\x001f[»vîäåç(tÄÔ«MºûÝ¿{úøý÷¯¦@3
÷ÞÕï¿S\x0012r$?ø¸½\x0004ñ`ªwÍÿÿù`ª[âUè
§~\x0001´ÔSu\x001bÑá\x001aNuK¼
ò"pJi\x0006Ä\x001d\x0012Üpª[æU¤û¬ÚEØ+k7:1;	ú\x000e\x0019ØWª]uÆ&+ `Â\x0011MFí¾DV¿¯ Á£\x000cßÆÃåG L±o×/Ì«No@ueÄSn/`-¸Ñ_¿0¯r\x0001%Ø´\x0003yh\x0000¬[[Æõ\x0019ß-ó*õ·h\x0017\ÏÌ3ûÁ·ÉÛÏò[JÔØ\x0016\x0007Sps£«¹ûð\x001d\x001aY]zn£Z8\x0013«Ëô!ÔxS	? Ï
d\x0003ÑP,ÊK¡»¤e¿\x0010Æ:ÚÂÉ7åDî$?B79Ë\x001dùÜJê\x0006\x0018ù¿Q.&ÌíÍêÌíç,û¦íª0ÕúQ+Ï\x0007\x000fz\x000c¿÷®0jªÑ(3\x0014Ûvä`çüpÙ}:îv"²ÜbÆúl÷ËH[,[\x0003«cî×-Ë­ô\x0016hÚò\x000f\x0002#oLj'!º#\x000f\x000cÌ\x0011=U\x0013}CÞ¥Ç\x000e\x000c&e\x0005^xòê\x001aÌ	¡²\x000fhí¦[BÅ±ÐM'\x0006ÖQ"'í\x0016å üÉëæ= Ï¨â×g÷{V^\x0014Mtl|æo\x001a1ºiÄW\x001dY\x0005É
2ênF½MÈÝN<»yµÎ
Ý\x0012Y\x001bHøI\x0002¥È£^TV'EÜMÇ*Í@7¯F
FÝHn0¨t½&î¦Çc}Fèr\x000bh/\x0013Â×ÞÄ~¸\x001eå\x0012\x000c´<Å\x0001w&®É_\x001a~¸\x0006\x0014sIpéÈär$L?IÜMZ\x0010ÑåJ¤xf²¿UPF?KÜMR,°ËMy¬Ø¦â×\x000c½±û\x000en:<¬65ªbC¥ÀV©a\x0017`vZ<ºiñ(\x00157K`^ù¢\x001cå¾\x0012|NG7ý\x001drf$QªR)éÛËô0axn´ý»o\x0008Òùjë
¤\x0010¹^d\x0018|æÍÕÕ{m'< A:?\x0004èÀ½Vº{xÔâUàþ\x0006³	ePí\x0006#G|0J|I]:r¤-ä«¾ý\x000cúö²!\x0018Ë#\x0016þJ\x0006"èýyÕ·? Ó_´:®jî;î©æ^ãIHTF"K¹×l3®t§'ÅýÓô#A\x0010tíGõîÁã£
>>$r_\x0011¤çsölXë[uaÎë\Ûâ\x0007-î`­q\x000b<+»G\x0004Ì?A¢`'c7¼õÂ\x0006eucdOûq\x0008²\x0014÷W|ÙôÂ'Hü	['áÓÃ¹uVÓâ\x000bßÇ\x001f\x001aòÊS5ñvÓ¼¥á+Iÿ8\x0006x\x0002$Ë;\x000b	¡6s\x0014,æúôµÊ\x001fO(«UT\x0011¢ÙÆÆ¸ê(ÂïÊ´þÌ\x000bkÕxòéÒ\x0001ævKR_\x0007ë\æý\x001fÑIZ?\x0008As2ö\x0003µ\x000e\x0005~E.óÅ9¢	ê\x0014d¨;}æ\x0015oæ¼ÎM7³~d7ÌüdTEHÅ^µ\x0017ó\x0003ÖJê/üÎ@\x001eÇÀ±p&\x0015\x000cö\x0019rM\x0011\x001f\x000fO>,ÀóW=jÌË» Ê¶=ãù\x0001ø(à¼!?gR\x001cEÜ\x0019¦~\x0011ò])\x001f91ÞÊ\x0012£cZ,Ø«&i\x0002ïCùóßü\x000f?øôüZÂ\x0013tqó¤ÙªHmJHnß"\x001bùrÁ2=¦´ä\x000e;¯°\x0019
z\x001a¯'\x0015sñk»¶nv/´c&&«¨¯QÜÆ\x0003\x0019J£Ü»Ðt\x000fÆ½8ÎU½Æ}ÍVdÒ@wå\x0014Gêc5 t\x0005%¿jlYivÂ\x0002J\x0001®®´à\x0001Ü\x0008\x0018.!³NdÕ*ÓÔ{v½Ú\x000fä³\x001c_;dÖI&ÁÄ×<²l¶ã .ÆvË²ÁXSUýµüB·eQ.®.Î\x0006\x000f¸3ìVw²Í\x0016§4\x0005>ê\x0003YiÄÍ,æ²5Þm@(¡kb\x000fOÞ¨$ç¨å\x0002º%9ÊÃ8éòv¤R]0Þò±U¿¿å>\x0017s6\x00164ß¡\x0002=x6Zô\x001bL\x000fhXtô°<¦õ\x0019º¡ê×Í»ònm@q^Éº¸\x0005«¡u\x000cô¦l|÷
AN+¹ \x0011£<\x0003Ïh=yÖÕè$Ë
HsfÆx4¥Ë¸QU¯ún\x00074|Å\x001e0E6ÒXýP't4'ÇQ½*±\x001dÈð\x0011{ÇRJ\x0006ÓþÉ|Äè]å²Î«ü¯þ(÷Úv÷ôOx~ÿJ·yÎFç ­½~H\x001eÚ\x0003\x00041[ÛºÑ~5m¶mðmU^\x0004jHrË C1\x0007îþ	m£\x0008;Ò\x000bï\yd\x0010w\x0017¤@\x0019\x00119Ñ9\x000bÜîDwwäÇ2Ì#%*\x001aÆmVã9\x001esv\x001b\x000c\x000eäv¹O¬\x0010hDI\x0011wlÅ<yVqÑi\x001f|5Þ­\x0017×w5\x001eÈ\x0003æ¹BÕ_ý¹){(ó¹V7§[«;\x001fÇ_ÖÎ0¸ÂäýÈU/ýQ<ærÓZºAWX^ÀL×\x000cå?\\x001c.¿®#À0¸¦¯:,>$ÕÀ\x001cN4ZÏmÐwZKwè\x000c\x000e\x0004m_Ü%qò¦mýÝ¶Ã0\x00055ùGØËJä§L)L\x0014ÞßÚNké\x000e]\x0001ºb¯m¢B®\x001a!eÝjÚ{¦¢\x0012Mtè\x0004Í\x000b:ÔÆÒ\x001d¹\x0003rÆ0R
I\x0012!W²ÜÓ°d¸Õ´\x0003z\x00004Eeý!É\x0008U¢4«ãF\x001cw>ëi!\x0007|	$µ\x001bFän\x000eÒâÓv`(§i« ò\x001dv.&Q"cNn\x0014r@\x0003±$Ñ»HO%
\x0016hæÊò\x0018n9í\x0006fªq<\x001b­<æ
é¨\x001bá\x001cÐ ê\x000bv®é¨1,\x0013èn\x0016õ\x0012Bq\x0014lwhØ,%c\x001aM\x0008"aVÞ&c{·¨\x0013,êJÍãIB©BÙ¢ÀÜ¶\x0005ß­¼\x0004+O®öK\x0004}9§WRÙ·¨Ü÷9'Zb¡Y\x0012)\x0001¨$snf¼o·=.\x0003ü\x000bY¥¶¦ª©N3\x001f
\x000fv/¯Ýÿ\x0001ÎÖ©5\x001e^8Rÿ³
GV\x000c0÷Û¿ýðñãÓók1×Ônâó°ìBöRP¦£@µ¾Ity£xmÁ\x0018_Ö\x0012±U*-\x0002;üMXÈ1a4áeY{\x0019¦"±µlâF1UD)nJgG\x00063s¥à×|ZÉß)Jq';&&pU\x0016þ|E2f\x000c¿-6¨õk\x0007|}e\x0013µ
rBà>\x0002{\x0012g]vÅwÇÚÑ\x0004­¥±jIßi\x001d0d¥P\x0004?ñ²A\x0003
ì+¡=GàÇz¦ºBË$HÞËà\x0002u2¯àP7ÅÎúÎãoúNãäCC\x001787¼ÉjÙÞñ^öüñ7Èµ÷köæõÍ=MÔýøùOÏ?~øøJçaoÎ\x001aáÁä­ªý\x001f¹èZÇ7²Ú5ó%-iav;\x000f²XâÙ\x001a ¶ÆH,=òGísd½C>çAû<Nn¶j¿á\x001c6´ìý¶¨\x0003÷L'\x0016Ñå1b[dùs\x001eZîYßgG>SçQ~;ëO\x001aÅ\x0004FïÃO\x0010ìÈ\x0015æ"@´¶d\x000cz{å»aàÛòìÈgî|I]Ã)Æ/#°=t\x001fÉÍo\x001f¸ x3ÑJBf9\x0011»Hæ"ó$\x001b}¨
\x0019òÐ1&4\x001dÔ-léÒ§MÕyjïÐçòâ\x0001äØ2l° ol»¥\x0001=\x0012ª4
vurâU YÔjÄ&\x0003\x001a¾`¤&f:¡®Æ¶üÀÝGÞu3ÄT\x0013\x000fþ2!G=ý'àð#F¸áeA'¾ûd\x000fÆá%Gmd}÷ó¿úéÃçw>½^\x000bk²:DãQèL*\x0001\x0007"h­¬\x000cø/ÞÇU»2Fþüa\x001dìa}3à\x0017¬{X\x0007{X%òõ¸\x000eö¸þJäë\x000cö¸þ*äë*LWÅ"mbÿ«Ïß|µnÂÂº\x0016Ë\x0008ûø\x0019­\x0014ÔøSÞ³¦Ö~-Ô2?f\x0015ê	uæhª\x001cÀì£é\x0010ú±Óoþ9A³<\x0014¼t4QHòß¦ÂÆMÌl¹½É\x0019\x000b\x0012îJ$ÙÍ-\x0019¼ª}×El¹]ÏØ^\x0005
©ãO_}\x0004ÜWÎ5dH¶Ú®\x001eÈ¦Ü 
·É\\x000c7`H¶Ø®¸vÃ8\x0007\x0014nJ©ùÝ?\x0007òY2\x0008\x001eRKaT<Téì«`&[koµcyyÉ¥V\x0002æ6ÂÔ\x0017ð¨J¶ÖÞ:Ê[«º>\x0017\x000b¨²moü­¶«\x00169Ô\x0013æhÜúX\x0016aê[UünÿAµ½é'+0èÈKCfGÝ½¦ÇmßÙÛ÷§\x001f^ëîmxó±´G\x000fuQEgèÂUEñ-\x001eJ_Z§)zeö\x0001}ñ2àM$éü±wº,J_þwG\\x0000'X9Ó(O0ã/Ñü7N1ºmh³\x00118ð¥Tzð\x001fJ;òyè©ãWÀ\x0011w\x0016\x0007v*ªÿNÚAuT¹\x0001\x0013<Öóù,ÏSFÞ¯ÇÞ\x000cª£a°Ûôf u¹ñ¦l]ß×coG>SRC¢êÓlEXYª\}¬ýsoG\x0006MI=4p6Qÿ-¼ÑKÏÅ=÷vä	cFbÍd æ\x0019yÙ3×oFùßÖÐÇ:%+ï\x001a«\x0019ôÍ¹·#Ã\x000eL\x0015ê{kÐôPªÀ¤Sï?\x001cwhP3-
}GTyeAÍDà÷<\x001eÈ¸	#~Cí½\x000cÍ<£ß·@Nª:@Ã.T	c\x0012eE\x001b\x0019u¹ñ\x0019Ý¡A'5 ýeÕF^\x0016´®|r;!Ý\x001d\x0019¼È%BBÃÌ9ÄjtåØíþtCªä\x0018	ºmu:\x0008*´QµýºáhÄyÒÁO=:2dv\x0016j¾\x001dÒ\x000c>ä£ÒÚPßÀFÈ'cS\x0010snwèó\x0003*
\x001cÎ{ã\x001cª\x0012ñª»ñßñû\x0015èw\x0014äD½?5\x0016\x001eò¦\x001bî=nÈÐ*§ÛûxÔ¾\x001aÖÑø Ó"38;4lï6i¢ÛàÄP3u7SÆ»o\x0008­rsl\x001e«C)-ù\x00028£3¯MºÎ19Ü¡ñÊÊxÆÉæ¶ªÑÎáUÝÄ\x0012W<6"%Ü¿f3:¿
äÏo~óü\x000f?¿V ¹\x001b\x0004!\x001b:?tÈT\x001d\x000f\x00063lE_^ó·~¡æ¯á·Õ,«\x000fh\x0019SÏ¨dU£·V\x0007\x0012®^Lm³ª¾(>írio6½C\x0006
g'%+5!2d\x001ci­º¥ÍbJ2ä¶\x0008\x001e\x0007pnl
\x001d&['ÈÕì³Õ)mÊ\x001b\x00118§qm¦\x0001bë¬tÄ*Mq³ªz0t\x001bd.?ÈYÎ_bØ\x001bÉ_SÛT\x001a!±¨'Ûho!Øg×·è@\x0006²zÍXÉ§ÉØl\?Gò×0òEB²çF=Cvîàiî[\x000câÈk²©n0$$Ï\x0014éY¤\x0015
~õÇ;Å_ÃõS\x0012¢:ËË'º
è-b÷\x0014
ÙO\x0006=û=å1\x0010h§°\x0002lnßFâ@\x0006ÁßD²ÍÊ±'oïØ
a½¯ÆiOð×pýäDÊÈ¢V;\x0013bk%÷Ê¦u·\x000bQð7çíPy\x0004ÚÜÐ\x001bw0Oð×ÐýdÔ\x001d\x001d\x0008fàf+-Q0ôÜ4ïv"0øK®¨¼¨}\x0007#ß0±­óÎ\x00136|¿õ\x0019ÏÜÍ» óGdÜ\x00159\x0001Åý4\x001fH­\x0012ê"A±Á¸´µ\x0011=bC÷[
ipFkh\x0019ù\x001bN^\x001eí®é \x0018ºß\x0012ì"ïaÄäí)½M'lè~\x0002\x001dÙE"\x000bfLu ù\x0006\x0015\x0007t¡Q\x0003íVm5BãQóÊ)tâ¦q)©ïíÓÇ\x001f_¹\x0015òTzx%,ê\x000f´5kL\x001c¿k\©ö?\x001f7
SürD	x\x0013ø¥²0¸·øFolÂZc#á4öÈ¯;ù\x0007L°Ï\x001bÜ\x001d2j¬\x000c¤#k·¯EîÜ}£a
_K\x0001ú¬\x00001\x0008»
j¾¡
CS(ZÙ\x0001{\x0014}6bêÆ2\x0012õâpc¦aX
ê\x0006§®µÉÀÅ¬ÓÜi\x0007\x0006>Xdõ®ÎÒk%NCSß´Î¯\x0007õ0\x0004\x000cªOrÙ¬¯\x0000!w?C¶##\x001fLå\x0008]f\x0002/åÔü4ÖäÆ	,\x0005A.T»ÇBûV\x00072R\x0010;
Î^\x001eç)¥òÍ=>\x000cÿA^ÈÔÕ\x001få ¦\x000cYÊÉ@ÇËv\x0018þCi\x001cBFÓz¡´aÞ7RÃÐ\x001fÔî	5°j£F~my1²\x001cÃSQoöá¬BÞï?½ùÝ»÷>|þç×ª=\x0017nV]¬=S\x001exKîüòµçò*Þöñ¬\x001cÄÉöI¼ïZMÔºlµ\x0003\x0018JÏ¹r}ÉUuÞL\x0016ÿ¦ÕÛ¾Êxaá<\x0018UÅTaÜK ÙsË\x0019N\x0011\x0015	áw¨&9;ÔÝÊs´ÝlµÕ¢ªqvîz/RIpE}£íf«ÊÞM\x000coyÈÅ¬ÔâÖ`¢mf[ä \x0016¬\x0017\x0017×q;\x001eXî5`ÙdÈÁ¦\x000eÉ¨dI]\x001fÐéåµOg.ðë-nVr29É;Âq³/g½\x0006&@×Æ­¼Å\x000cyË©xÞöå¬×@\x001c­\x0016æi~zÕ ñß·¶­*g¼\x0003´ÄØ\x0016×sì\x001eù·×k2ò»§Ï¿ÿôZí¶Åú\x001aËÃòA\x0000¡à\x0015¼BµoáIÑZú\x0012ñ\x000c\x001fs¢FNh¤Æ\x0012V\x001c2ÌÔ³[ÖÞ\x0019¨¡¼)í\x0018¤\x0000g^b1×ÚaÈ@ó\ï\x0002ûäWÏÉm´8¡®=$s\x0011¸àÚ;;\x001fM7\x0017yàV
U_$cÊ>X1mFÏ[o{âÚVÚûÿçÃç×z.\x000eöÒË#âQf\x0013
$ÖoãµâkÞ;,b½tòâN½b´?6ÏÍ®è\x000e\x0019¢l	~Ï'ãò&çµ²\x0017EÎ¾ô\x000cQ¶®¿\x0002cfÁà¦\x0019rsSË\x00070<T\x0001\x001evKä%ÌFsÍä\x000e`°ÁÙ6ÔÂ­i°hIí$¾áâ\x001bÉ_n/.U¿Ö¿CÃçSe\È#H\x0008ÉÏ¯ÞxÔ£úÔ\x0003\x001a¾\x00044\x0011¥#Yt¦NtANý"ô¸m
\x001b¹Y¿¨\x0016\x0016"·\x0014¢óà\x0017ï÷ßüöÕd(*÷¢Æ¼Ò\x0005Û	¨Ìº\x0008\x0001ZØØ_¿øCCé_òÐÆª©ªypÆ
zb§º"#yúÎÓ¸½WÍbx­&¥³A\x000e~Æi\x001a·÷ªN¹±Â#;\x0019
r3cö\x0015î§±{¯Ê­0\x001brä1rI6¤ô­9§±{\x0017äFOf
\x0004røzEî×ÇÆ4~ïU+~ÐÙ¤\x0001%=cº±8/wºiüÞ«?ÏÎé5\x001bô&èë¬2\x001b¾Ìý4~ï\x0012Êd\x0012Éú¸öa7ýÓëkcZ¿÷*ÈsÖÝ\x00005£ê?7¦1|AGìyÅnÎÕá²hï6!<7¦üþ\x000eÓ+1üë´Y68©²i\x000cße>:´¨Wu. óÅ>;Ït¸1|? Ïm8+?¿RÅ[ Ìº<ÇM¡n\x001a¿÷ºH³l¤T\x0005:3ò&¿x·
¡N§ìV 1ª\x0003	ùø\x0016Í ï÷~@7n´òB§Ø£JAµ\\x001bÉ/ÓMã÷¾.\x0015H\x0006)r'dN++²ß9u@ÃF\x0003/ã}UXEO®\x0007J4å>o*uÓø½Ë°·:$­\x000cö\x0003zÎ×h/7¢Óø½Ë{%\x0010\x0003²\x000eÛ\x0018¼\x0011%.~¡nG'²:{\x001f1ÉuþY\x001e,o\x0015Q§P7|S5\x0011è\x0007\x000c£p¡n¢hn[ÚÝN<u9ZØ5î\x001eÐ¯YùBÌò]ý\x001aà4&õjh\x000305ôN¯[\x0010æîåº¢HGÔl®'ôîJÿNk½ÐÝB/Þ¶£ ¿C·\x0013ºñg gÐgl|êå¾qôÒvä~"OXÒÊ'@ÔÉ<2UÓpé\x0007ì8ae\x001fBb/hÂ6Ë0ÐyKOÜíÃS¤¤ÅÁ*RH-YÜù¬òÞ.qÎ\x0001'\x0003Ã%] \x0003\x0013äs^eí|·\x0011ó¹\x0011£²|¡/Hîq"Rqhþ[]Ê1\x0014Ø¡\x0013LH{[aÔjÇQ\x0011:r_ Ë< \x000b:\x0002 êæ	\x0013¡³9óRôY\x0007tûËæúj'¸6	×bþ^^
??ÿ¤H¯_	õåN=dúTÙ\x001e
:0|.À\x001bÑÝ«Ù]jæ®Ô\x001e4¯\x0019Ä	T­6®­­Ùúêu·#+Â^O{ 7â1f¹÷AU¹ñºÛ¡ÁÙBb3`ÂiÕ*¤úê!h¿y\x0000¯\x0005Ëgj\x0013\x000f\x0015¢Õ©o¸s@\x000f&o£$çVch£«Þ¯'z@O.$è­ýóä?\x0011:³\x001fÆ\x00126»Æ";4HÕ×ó$F«ä\x000b=eT­¡Û
¯ÁÈ\x0001\x001dÿâQß-=È³Î&q\x001cQOû¨ø¬¡\x0003\x001aìDî\V»T\x001eõÒ¸^ë\x00074,>ÿðxñàq/à\x0003\x001a\x0016ßL¤\x0003ØMwu(iiíÅë-¹C£7ïÀ+[ÂÕ\x000cÍV0m×Ã¿û@ø¯!Ò
\x0018W\x0008;'·Rýì@F[\x0015¢ÈäÐ±V¥²«DX[\x0003ÄÝW\x0004k\x001cyua`ùlÑW4Z­-­Ï«5Î\x0001
Ö8{ëØ\x00019Ö\x0011hã1Ñ»ï³C;Nð\x001d\x0004ê\x001dÍ\x0013Ò'zVß\x001dç¯¸oì\x0003Z7\x0010M\x0008\x001bi¤'víïÿÛ\x000fïüøZ\x0012\x0013êÍ\x0001F¨b`OH*(½lJ\x001fÿA\x0002\x0013:mÀWÑ2X'½nó§j¥àÜÝ\x000cåÝ9H<Jþu¢ÔªÛ9Ïbv\x0013ÙöÉw9¢\x0007\x0002³øU­¥ÏÓ}7ËlûÙ{\x001e\x0003Éà®@mÄî<\x0019nA:Úå÷~5MÌ2\x0016ßkêdÕöö[\x0008ôÅ¿$ñ\x001e¬µ¬ÍI²_\x000eErsãÉµ1Ü\x0014¤µlN\ôÈ½&ÅØOÆ¸©\x0007;\x0005ic-«ý/(ý7\x001aFh,¾\x0019[:\x0015ic-»©°\x0006Uhºò
­;­bS6æ²ÚÿÂÈ´uây66ÈµoÍúËjÏ\x0007Þ\x0008C%ûHué\x0004yúeLë/«\x001d0HÖ\x001d9"ªÒn/weýeå~lÐøØ%cìÑÌ·¶åk«µõUå¨\x0013¶4ê£ÏÉôö|7`½eëbºÂ6é8>ò\x000f8÷\x001979\x0002§ÏÚzËVu8EQýÒë9\x0012{±ÜxË\x001eÐF
ª\x0018Ú:OD`\x00195ëõÏp£mÍeeÕ\x0012é xoTN\x0002¨lº\x0019?pah0
PBmRg\x0018Õ:r\x000cß(âå,O$¨ÏÀ"¶ÚiÁ±x,ô³µR]¥?h`Ñ

Ëu#\x0011"{Á	"t(\x001cî\x0005ÿþ/ÿú7ï~úùéµ'ÞXa.G»ã\x0002&ß&ñß7)\x001a«ÍÊ\x0014c7wWÓ\x0004\x000e8pùUþä·vrr\x0000\x0003;µ\x000fà\x001bw\x0015¾\x0002XUú @dï¾Ã=7M\x000f¤>®4\x0011"Ý\x0019\x001eó\x001c>ê\x0000\x0006vjhé#A¿¡ \x000enÞ\x0013s¸ñÞñÞ@±Se~R³Z5\x001ed³\x0017ßhG\x0006vêÖu\x0000kæyÐùé?çR\x0019º\x0006;0\x0004¥`cg«\x001eì9dNèkc£[.Þ
AGkØ7U<óñªo¾Ã§Nà\x0014çÂ\x001dÊ-ñîç×Ìø\x0006
×V\x000fôZluRl ÏÎL¸¾Þ¸N±x>7_\x001f\x001d3\x0015J¯¥\x0006InuÜôtîÀð(bÛòVÞY-\x0015ØoÔA\x000ehØûG{¬¹LÁ®ÖxÔ{çåÝ\x000eZq/Ô\x0017¯Äy¢DëéÊ.ß4uîÐ°\x0005\x000b½åtsókpX#kkúÅâ\x001dºÁG¬¼ôLçeKL)u=îvaÄç\Ã;±këCÅÀhÔ±ÜôìÐç>TÇ\x0013ÈdµÝn\x001c\x001e»ÏÏºñ\x0014îö"Üä=¢¨E ª
Õó¨çMµx¾N}¦@.\WH¤m^\x0015(+Ä§«\x001dÐ°eä"¬°cTcn»ìvc/¾#Ã²\x001e\x00195\x000eôb¤Â|3TÆ9·ºëÝÚK6#B«;$}EÎ³Ë²^7SÆÜ¡aH\x0010Yø:ä¯8{ÿÏ×ëÐ©5nÐ\x0019NÔB\x0015\x001eâÙ¡S\x0010Ü¡á+RÊ\x0019h#è'«ù\x0005Á\x001d\x001a>c
X<êÑ4o+³¡óÃø\x000e
Q­{`ÇÄLqµäÏ¶ÁæÜïþñÝ\x001fß/aÐ§7ß}øðOÿö??>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==Ã\ôà\x001b
wù(ék%IåP_b1I{\x0006þú\x0002ã'ïÕ	ÜèXãÇfpeé¥Z&ÉPÁ±Â"OåÒÎ"\x0016o
2n_ç¬{%£\x001e¹KR{\x0004|u_²ßàe\x001eãI-%j
^)¥øfáyù4§÷øð>ñfívJíá\x0017é¶¤ëò+V\x0012Ëõ(82È·EAQpÁß¿5L4ZÞ{}H\x0019e²\x0010ÒË+~,Ï+krôÌÏÓ>Ø¬üc%W+©n\x0002Û\x000cý\x001cRæêÞ\x001dàmÞa\x0002ÞI<\\x0005ìX0X\x001bé©ÇÊè\x0019{juÎ£Þ\x0016B$j\x0015D3µtzÜ\x0004+\x001c\x0006­#-QË,±ÙØ²ÆíØAS\x0004\x0006;à\x001bUÂ¶±ÝH÷ÂÙØRcâ\x0005^­·¿x\x001fw¥d\x001f¿,\x0013\x0019ñ0\x001b8ãÅGÉYyÚX\x000e>x9}4A!Ùó\x001b,\x0019ÊÖ\x000fÐ\x0017Ác¤wûR¾Ëé×èÃÆT,5\x0006O~Jcd\x0019½ªé÷e|WÐ[Å*òÑ\x000bÊØÁ\x001fÞ~¤Ãì:zSÓ\x001eôÏáðgN¥ÿãl\x0017ïFîýkèªÆ\x001e?¶Ó[íIÿ\x0014¶Ï<ð2PûlLv9&ß?\x0013=Ôè#êÏ+ÐáÛ\x0004¾qæ'7-\x0007õjG\x001eôZ_ÐãÇvzvÒ\x0015æyI\x001a{îSìMt}¦M,Rù~G\x0008u%=ì¤q{»Èú
p^dM&3U=¶^}í>}îï"5#À#A\x001fK®F\x0013!eðq\x0007~¯íÆ*xÍêÐÖD:´\x0003¾p,[\x0017»¬Z)kg>·ã«çÁ*\x001fÖ\x0003É9\x0000»\x001d¯b;ì±\x000b»Ï!^ ÷êàY\x001f\x0001v¬Ãçß%ìÊÖÓFíwkYÁ\x000e«U%`)ZLùãkÒÑV'3é·m\x00083}=èb£s Ñ³îê´ÉJ-ªãYúÜcÎkî\x0002¥=£+Ò"|3Ò\x001fl\x0015¾ª§V]¦\x000cn¦á¤\x0019dÆ\x000fÜe\x0001Kéºà\x001bç*|ãö\x001bu¬p0ó	ßhA£¯1PHøqDbw\x0015~45~ìrR\x00102k\x000exLË=¡äãè9hª&äÖfÒÛ¤Ým¤\x0005ÿJÚ±¤ÛûÏ/_d£íu4=m8o\x0014I¾?2Ô°Õù9z·§¯¯înÎn'ìðÉb
ÀùPî<Ò\?|{üiR¿/|¡\x0016«³êF\x0004ò<\x0008I¢\x001bNÉ|ãë³Ûó[L:¿Æê\x0003wÜd*J\x0001Á\x0006µS
Ø`\x0019ú4óT­kaaÐ
ýp^à\x0002\x0013r\x000eLñ¾90Õ\x0006Êke½J\x000b§¶@\x0005»\V/´\x0010à\x001fZÆ©ªæêòðìQY ¢'Âó6¢}\x001a·iøO¿,ÌÆÀs\x001a\x0005ã±$§Íi(\x001bC	jrLû\x0006unÓèÞÜ¾âßQv_9\x0003[þ\x0007øÕb\x001b´=a\x0013"\x0018¼pzh¾8Òqlß3øÕ,3tiîg\x00068 I=$5oÅ^x~6S#!ïuf¤°ÚÖ§¢ò3~,Z2/_¾è3³"$.\x0005¼Aâ+±\x000fC4ÓÉ¯\x000f='×-!û\x001aÙ7#ã+¢ ¹óÃ¶\x0012C\x0000vä¾²\x0008YûX"§Î\x0004MÈ\x0001\x000e<¹½^p0_\x0014½Å\x0007$A×\x0016![]!ãÇ6äeÀ¦8à)£Ñ\x0012ñhEÄ^Uó\x0002?6\x0011K©¸P/xïÙ+LªÈÈnär\x0011r0\x00152~lCVÙy#r°Ú.Zc¨8,ÉÌ\x0012d"Å\x0005rúÜÆ¬uÌwÖ(pÿÌo6°áç\x0013¶Y¼+±®v%Öo±üñåi¡¶\x0013\x0001±~0òn\x0019\x0013ïa1÷[,|¼»rÍ»*ëjWe}\x001d¶\x000ft<±QPrË»åÐÆHÝ"l½;ÚÚÖÍØ_\x001f;ï<ÿ q\x0003LÊF¶¦2uz§*Ð^O\x001eÅ\x0019V°ª\x0005Vb]oÅø\x001c*,(Umªbq.­+i]\x000b­ÅþÔ$-ð¶â°ïZ\x0016¸Å>=­¸¡Ä
M¸N`	bÆÕ4yQÖ12î¤¦÷,ÜB\x001b[ïjc/æåæå0sC¤Ø?>`
  
  
  
  
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
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=?î|C@=/§ÁÉtô8í\x00195äÿvïÈõÕõåÎïØ?|±|C¾¿½yþ\x001dôóóã§\x001d|à-q:Êr\x0003\x000e¾\x001aümýÐóñýéÉõßA5__¾ÞÂè7?È¸9{SñÀm2<zmSUfØçTýrù>ÝHF*ö\x0007¯ÅÍàµ©h\x0014FSàP\x0003;|Í-éJô\x0012lïWµ%md£f©Í\x0000W[6®øÔÉí9x®Äsx¦+9J]\x0006¹u\x0018ô\x0008÷^k»çÐíþ¬±d­¢³´4à*%öÄÆGÚ®\x0013la³U´û´9Á=\x0015Qåºná\x000c\x0019¦\x001cKÀs¸ðëª>¥j§\¬YöRê>¥n§4\x001f\x001ar£èøí
rÖQ\x0014¾ÿxxQå¼¿}7w¼\x0004WQsg_\x0000FO}Ú÷\x0011\x0006ãôß^Ãs»«É%ôÐ³W¾ßi	À7åö (iêçÄé\x0018·Ç\x0011¢%ðý\x000e#à}¿7è\x0005õ\x0006å¹«w7SC0\x000eÇ=¥´×òñ8½²V¢nyàé«g'½8Lú¨Ý¿vöÇ§ç\x000fêFðºL·Æ¥dC\x0019Äl\x0001ìîö»»nf­Ö¤h³OSêqCA>\x00042i<¿dg§?\\x0014lÇ¸yó²³£¶±²¾hú¡ð-@tp\x0003îÖ\x001fGÙ\Ø{ÛÍaómÊzÇhE²á&`+:²S@np	Î/_|Ý\x0002Pº\x0015PÑ°=\x00044X<Ð\x0001ÊÔ)ô -\x00004% ù\x000bJÐ¶\x0015PÇT>\x0008ðævñ\x0016\x0000¤G\x0000è¨ju\x0001 +\x0001Ý_HàA\x0015Ú8ýÚøûÛÕåúóÿÞuuì\x0016aàÏbq\x0008Ü\ø\x001b¸ts-Oßc¬ï/NOVÇoNÆ4^Á£J\x001eÕÀ#ÒPLPw¢³ô:$Ê\a*È¡Ã¤K&ÝÀ\x0014R\x000c\x0000\x0014Öµ%1¥Y
²kõÍdJ&ÓÀÔgwLÆ¦Å\x0010ÈJf$nÛ³\ÉäZÎRêÖ\x0002&ëÓÊî8ñ·3zþyò%ÎäMÅ¢\x000cêIe1ÉùH¡D</p><p>Mbâã\x0014üçO\x0012zÀäåüO\x0017K¦Ø &GP÷é¤"1ñ\x0011Ogç«lËfu?LE³\x0011éö¹´\x0014²Ó\x0008|ù|ûå\x0013Uì-ýP°`ø¼xøòe'\x0018\x0006Ü¼KÚ\x0013?iRUjÌ©,²`÷¼¸x7ZðZ\x0000\x0012Ð´\x0002Zj\x0011±I12 àsYï¥|¶ä³­|N§î+àóÝ`ë/(þ´ÎË=\x0003\x001eJAçJ:×JgäQ¤¯+.\x00136Û(<·Xx¾ÄóÍ\x001f7\x001c\x0005ú¸.¤¥ø÷t\x000cÈ£À\x0017\x0000\x00120´\x0002b¸\\x0013`÷XuÚòñsrß×Ý\x000b\x0018KÀØüÙ*ë$È\x0000ÃB>Ê<°~\x0011-`6ÆØÍåI÷zÅðWÃv\x0007 î!\x001c`\x0016µ\x0006lVF²µ+¢¡[¢³</p><p>\zI¤ª\x0000U+ î £CA\x001bR1BÒûï¼^LXéhÙ¬¤H$\x0012¡c@\x0001>"²RÒ²YKku\x0014²æ[bTþÄÞ,\x0005¬ô´lRÔxMBÀ)8\x001d!6ÈøtMÍß8,¾ÈªÍº\x001a\x0014\x0008Pñ'¦6cäs%XijÙ¤ªQÚgë\x000fcWþ	¿n\x0008£Zªªe¥ªe³®{,è\x0014ò\x001egOU-½ÇªRÖªYY«xäI2\x0015ÁÁ"¥êPZ-\x0005¬tµjÒÕ\x0008è³w\x0016pà`D/lþÈK\x0001u\x0005¨[\x0001qM\x0001I0¤9j(VÃ0RÖ\x0002ÀJU«&U
ÿø \x0005\x001büQjþÆ¸\x001fc\x0013Kï±ªTµjRÕ\x0000èÁÃµ\x0004h-\x0007ÂìÄÉ¥oªTµjUÕ^¦"=à\x0003º±cøN³çk\x0016kBUiBÕª	-¸$Ý\x00161§°ÛGu&\x0003\x0006µø5V"TMÐár\x0007r'\x000e÷#Ñ'\x000efÇKì?[ªªuuKtã-\x0001{%bm£ëFµÔú\x0003gP\x000c½Öbé=ÖÕ5Ñ×\x0004\x0008l\x0002\x0016¾¢ÎÆè¬I\x0015GÒ\x001bEõ¶\x000b\x0008+A7\x0019\x000cH(©\x0019\x0019\x0008qú¯N2åàð\x0000_¹º(ºñ¢x\x001coÕµt;#OS6ºL.ºÅ2¬nn¼)^FÅy\x0015j'&B'è+»\x0010:ÈR-òñª \x001e\x0000\x00196¢[÷ÈV¡Yls-¼Ð×\x0019!µU%»!(zE6\x000eåÒ/-Ý\x0016¨\x0001ê7ñ¸(Ó\x0004Ï\x001ff¶ÞQ¦\x0017/TEÛËóêÝÓúãî\x0018&\x0010x2_±Â!E0@lJ÷\x001e¾wuüj\x0002*±T\x0003\x0016ö&Ï	_fÜwe5\x00194Võ}»&,]bé\x0006,ëR¡<\x0016ZÄ#Á9 \x001c\x0017\x0014R-À2%¥\x0004ö ÆVÈ\x000e @ZÑÆq¬áH%3ÙÉ6</p><p>Ì¨täqJ\x0008$)\x000eÛÛØ'$åJ*× )eÓL7'îò/\x001dVT¤Û\x000cW\x0006ÎÃò%o9W3	å\x0007\x0014Ó>à^¬XbÅ\x0006,/R5\x0011`¡UL·0g8ìV¯\x0005KÖ:«EiÁ{DXZc{R¥9¶gM?(ÐUxÙrä¦l¿ôpÎ\x001ci\x0007íépYmpUK¶®\x0010S\x000f\x0017pÿÊkcY^2ú\x0005\Õé
ÇKIÍéFgºÁ6\x001dç$ÿUl¡RÕáR
K)Ú\x0010âÀ¨õøn'\x0015AgÞÈ8ç*</p><p>Ý+@W¡®k~ñøüõÏÿ</p><p>G\x000bÐÓOá&\x0001×2þpÄÒ$\x001biLP\x0015%XÜüâòú\x001f'ãÅÍ\x0005¥*)U;¥	"U{CÊLFjwÆ #\x0012Ñ´#ZééÍ\x0014.\x0004Ht¶r¸¶©
Ò®\x001dÒa_yúÚ\x000ennè áÚP&\x0008_+µÒ~Æt*\x0019DwÓ4i&@ÚC@\x00122Ì\x0010ePdQ</p><p>\x001b#\x0019ºJ\x0006rºU\x00078±3$é}*!\x0007IÕdHR\x001a\x0006ÈãbÊ"÷§·º&azáÓ¨H¥fL%ó\x0017vÉå	={ÓËó´Þ?Þ<ßÞí¼Þ<JÅ	ïã\x0011ÝnOZ\x0012\x000eÃ g¸:yqyr}:VË[À©\x0012NµÂÁ-qI÷x¬%'
Iã"\x0011Ï\x000fæ\x000c¦ãé\x0012O7â9Ö	\x000f§"¸tUD ­ãìpÚj:)ñL³ô$O:éEú¶ÑÙ,½x®Äs­xØ\x0006\x001céä\x0005²jÐE\x000c'\x0017âù\x0012Ï7âE\*KÊÚc\x001d	ÒYÁÂ³¡ïi´Ò.´</p><p>\x000fç§ñµí,NxeçÍ`\x0018~:],éb«ì|HÍ´Øÿ&ð\x0010vÂsõ·ªÉxj\x000eUYÆÄë4î¾àké³äFâÅ\x001d\x000c4Mç«ur£RV¸Ø)h²¹dJ7+4\x001aH|Î/Ä«´²lUËh­²b1\x00113÷ø°ÖÄç\x0016~ÞJ±ÈVÍ\x0012ðÙ ÏÅÚéóbÛ9ñÉá¢é|ÕÝ­7\x0018Awù\x0015Ò|:\x0018>~*îæ\x001b©\x000bý,x¨²àÓÎ\x0016ÓzÝÙÓßpÞ\x0008V|v8qÑpw«PqèÜ§É\x0010g5kz= Ø\x0006N§cËÅøÁ<ß~Léz\x001e(\x0016YN*]¯Înßß<>ýùïIÈY4\x0019 ª¬*æ¢\x0011Y\x001b¥Ç«³Ó\x0017'Wc1GFT%¢jG §E</p><p>Ä\x0004øÖÊ½u®ÌÕ½!Ä½Ô%¥þ«RÚÒÎ Ô\P¸ß\x0012¦Ýçö\x0013\x0004:Êå®¤t3(UH;!Ó¡\x0014Æp\x000b\x0012½8,}IéçÈÒSÒ¥Ôt%âôÍY¡¤\x000c3(Ñ¾ö½¢0\x0019\x0014WÇöÂfAÆ\x00122ÎÄ	; =CÆ|*!7ÖX§*Å\x000cJç8Â%¤+Ñ"Ë\x001f|9e­Ðghté\ÿæ\x0000â!o¬4º£ÒI¹SÍvdÌ\\x0012-\x000f ISQ9*]cgxêkÐG/á¯mÅ~U¹óe6sÔ9<:T¸m\x000c^óôæd9ö\x000b±ä(ªÉÞé\x0007|¿O?ÿºþòå&Cÿðp·»Ö	w×§\x0012\x000eøï¤ñ1{Åm!Ô§oÞ\x001e¿{ÇcÑ_^M4%¤\x0001	\x0017ÚPw,\x000eÌ`HÃÝ±±çlÍt%¤ûJ2a$i©)JÒb`$·:tõ\x000b!KÏ:éòfJ\x0017Ór3È¸\x0000Ï¤qK\x0000ÙëÉ\x0018`\x001c¹Ú±\x0017î±¬àxóð|w{¿\x000b\x000cÝdG\x001a\~\x0019R´UÔ\x0010äû%c)_õæâúìô|\x000f*T\x000bò,,
¯J*qÂÖq*qj8EKTã:öâõx	`Öf0\x001dÒÌR\x0000³i\x0002\x001e\x0008«j\x0004³%m\x0001sÕÖX\x000fÀ°\x0015À+\x0013¦\x0012,4IÌe\x0006£ÄÈ«ã\x0015\x0006k^&\x0015FV\x0014åê×	di¿&ÌRóº\x000f*Ì.!«odËôJÓdpã°¥rbCYZ\x001c5X81¬º²ébâ<W:f²ÖÉæ+\x0002[ö5MEfZd&\x0004õãÀ#ª\x0010Efwê±½`ÕÅ-7\x0013Ü3</p><p>è\x001btB"óx¥:2/EXBæ*2×$2C\x001dZ8g</p><p>W¦&yË2[tþ}\x0005æ[ÀtLûáüÃë$\x0015û+\x0016Y\tü+]&[\x0019nÌ¢Ò[S	uÊññß</p><p>¯µÅ,¶Á3Z\x0004HD\x0006gËsQp?õÑD¦*5«ZÔ¬W2Íµ\x0005\x0005\x001cÔD½\x0011O\x001e®ÅJV\x001b\x0019-ÊÌk\x001asj¶[\x0001ÑYÍ\x000fRKn¦ª¬\x000c5ÙÌè\x001aÈÉÍ2RDv³D L\x0002|ÌEú_U*C5©\x000c+y"Òmmç©8\x0007n¦Xr\x0001Tu5Õä«Ù\x0015kªD6\x0002»²©¯]\x0018®Û7jÞËÔ¯¼uåÕóêõãÃÕûnEÆ¨è±i\x0003</p><p>\x001cýÀ6mðO	½w`³¼àõåÅ»ÕóÑe\x0019\x0005¨.Aõ,PE8\x001acc©.xË\x001d\x0010&Ôº4\x0012ÔÌ\x0001µrÑ:à~O@=\x001bãÊ?\x0004¨-Am;hð<°\x000eÎ¦vAPí#wlH{OïJP7\x0007Tê£(<®Ê$P­ø\x0012õÛÄfú\x0012ÔÏ\x0000µ¸\x0011l*¦ÛÆ ¹û\x001dl*u\x0010ÎPr9hÉÓ³¬\x00025\x0006ÂE·»\x0007dµÆ\x00124¶úh¸rB«\x0010ùìÁÅM'ÔE#+ÇÚ8\x000bo­W;6Y¢Æ*¶
\x0005.|í¨Çx\x000fIÔ
×µ^¥2\x001b®\x0013þÐ~\x0000Àä7éÁØÎ'5Ò\x0001ðb\x0019¯R½JÃ¢¿Y?¿Ç)«ËõýÛ\x001dX²\x001c\x0003Ýzi\x0004×ã	Ô©)ª«©?þ7Ç×Ý\x001cÍÕåñùËÓ)x¦Ä3mxZrÁÔ¸H2Õy\x001bÁtºçr¶ÓÙÎ¶</p><p>Ïs½7.è¶,<N(Ó«ZhÇs%k\x0014\x001eö§!ÊÑ¤¡ÉS.¤ë=æíx¾Äó­ÒG§\x0017òÉ[\x0008\x0017J¸Ð\x0006g\x001dm÷u\x0012çÁPs\x001b\x0017T0\x0013e\zòb\x0017\x001b?­à2hn¡Dº\x0017|ðdXøe\x000e\x001b¡Ó§MÚJ\x000bx¨Uèäqf¥]ªTdumeã½Õ67'á\x0010a|,c5%Ó¥´Kùª!\x001boQ¦táÖ\x0015¤Ç¥xVÙJ¯Þº~(GÄáü»§§\x001d5ÜÎÀI½ÉI\x000036-ÔQG*Æóz¸V«vruµ³»Z½AªÐàÚ\x0003júÈ¦¼V\x001cÝ2Á\x000fÏ\x0005iAÔ%¢n\x0016"V!\x0007F</p><p>|\x0010\x0005;0²\x001fhJDÓ,Eë10\x0011Î!å\x0015àÑ#Dø0Ü$ÝhKDÛ.EEíÑ\x001aÛ4\x001dÅ Y ~\x0016#º\x0012Ñ5KÑðL;\x000bLÎ)ääGGÀ´ ú\x0012Ñ7#b'%¯?äëb²3\x001dF>¶ \x00121´":Aë§0ù ÒòG¼ç\x001c®sfù%alÿÎ \x0014\x001cE\x0008g÷Yö£cíE&ÚÖ+§</p><p>QS©[õ</p><p>ÒÏG1å:GÖoKóãb|ä²\x0003	\x0012UT·ÍÞýð\x0004\x0016ÄJ-Êf½\x0008ý:í\x00140D[?%¨E\x001c\x001eøÓX©EÙ®\x0017EL-ô\x0006'ÍRzS;Îë{ÌZ,E¬tlV:\x0016ÀÒëbp%
Â];Äh\x001b6\x0018+¥#Ûµ$FC%}hÇ_Z÷ãÊ3\x0010+­#Õ\x000e6Q"O¦:ÁQ°©ãM¿s¼QUwZµ\x001b!'¨òh`t3\x0007^.¶\x0018Um16\x000e|Ð sMVNºËNbX|\x001cUe2ªf\x0011\x001fAII+¥Ùf\x0004c\x0012}\ÌX)GÕ®\x001cÄÒ$ÇqÅÄHãW\x0002ºÖ\x0019+í¨µ#^ëÔ+k\x0014Xg\ÚïuÀ®±¥Õ¨ÍÆî[Óy\x000cðGþÔÄ\x0008>ôbÄJ«f
î0ÙLbLÝúI¼äcd\x0014U\x000ba¥\x001cU³rÄ:uêãjä´\x0007	9`\x001cÌò§ZWFn6Ê°Î2¥Ü\x000c.\x0004ë,\x0013cq±þÖþÖÍú\x001bÅHú[+sä
\x001b<,F?2t½±ÒßºY\x0003ÛQº.¸HÈ\x0011¢¦\x0014pPfdPV\x000bbíñ·«ïM
«-\x001d©ÆÈc\x0008q±ÚÑÚÑÍjGÛ@S¬Ô\x0012÷8 £t4578±ÜäÑÞÑíz'í Kfc³ÌrQUÔý</p><p>9¾`Õ×ùåì¶é.aL\x0002®-H)Ut	ÉkuZÌ¿Ûà÷\x0013à^VÅ	oÖ_Vß¯ïî\x001ev\x0007CAé¤\x001d1\x0014I\x000e¼PAû0<ãzõæøÝêûã³³]95¢T%¥A\x00194\x0007¼­µG\x0007Üþ¤:\x0004¥.)õ_U¦¤4UYÚÒþUeéJJ÷W¥/)ý\x000cJëH\x0011I\x001b\x000cu÷\x000bã8\x0013hFËZ(cI\x0019ç|qÇÃÆÈe\&g\x0004ÍhaG\x0003¥¬õå\x001c\x0019
&¢;Lå85hyí[\x001a³0U¥Ô\x000c]¤¢;¢=hVZ\x001eÝ¦\x00039Ý\x0016þÊ±²s¬É£G\x001fz#ÉÞÞ<~¸Ý=\x000e¨3~5W»+v$È$r\º\x001a\x0019Zôöäòåéîy@Ì©JN5\x0013#§\x0014Ä7à<Föjs$ÈNkÀÔ%¦þëÓö¯ËéJN7Sù
§¥¡ÚQÀA!ì\x0012_ÎéKN?\x0013cæäÀæä\x0003p\x000eë¤6ÎPr\x0019Æ[öÀMÃ1))¸/8ª!âðCÔÆ\x0019KÎ8G8?Ä\x0019óñ\x0014&ïÞ\x0007¸î²ºFrÆ=</p><p>8Ö%}w+d8ê¦Ò\x0007p(\x0013g°B,âtýöB'j\x000fãlý¯ÛÇ\x001d¯t\x0007m\x000b\x000b:4Õ2(¬ÏMu4à	\x000f#^¯Î¿¿8½Ü§K<Ý\x0007¦%Í+38q§$R\x001e*û±Ç|*-ñl#á\x0011Û\x0002ïöGYc\x001f3/§âù\x0012Ï7âa«&á9A;%­^FÇÑÒæ©t±¤t±s¹ÓÑ¨¼;<\x001eØl0µTx?®kñ­\x001bå\x0007ª\x00198Â\x0000©\x000f\x001cNcÕö{	EßB\x0013Æ­Ëß<Üü²zùóú×»ÝÍË\x00118yTþf\x0002½Ñc#è¹}ùóWïV/¿=~{r¶«ÍQUªf¡â\x001e\x0011BõþÈÓT»?¢\x000eBªKR=O¨6ï\x0011Ä1$Ó<î¡ïÜÎ%µ%©Gªéé\x0016</p><p>BÕ?¿ëÝ¢VTÑ_C Ò\x001aM}\x0007</p><p>|~Ü5ZT`­\x001cÍùÀÆAÑô\x0019·U\x001cÔ.Þö-þñúrWh°¿@¤Å\x0004í Ú³g\x0016q\x001aM\x001cò¼Ìõ;\x0013T z\x000e¨Êë8£´¤AÅfõ±°\x0007á\x000c%g%ÐÀ\x001e9¶Wñp$\x001eÐ\x000b×)MX\x0006ÚwwÅ»{ò´¾ÿ´\x0013RàpðîÊ[¬\x001b´ímôàíH\x00050\\x001d¿\x0000¨J@Õ</p><p>\x0008R\x0014]Çj°+¹óÐ-\x0014|\x001c±\x001a\x0000u	¨\x0001-\x001bàEn\x0006\x0010dJ\x0006¯íp|¨Ï|¦Ï`G'@é°Ò/ñÑjÓàÝHÃO\x0003 +\x0001]3`¤áËVãJD\x0012 \x0015ù\x0008êQ÷k"`Q¸´íÔL Ä	¸ôA5ró+åká\x0001r³ïÒýu7Zô.ñåÃý\x001f\x0013X+Ruv!TçÇ1\x0001Ì:]\x0017ç?ìqº\x0018Sj\x0006¦-HßHnåÜà\x001c¶tâ<LSb9¸Ñ*i\x001der(È	</p><p>\x0005\x0005/ôè@ð\x0006NWrº\x00198ÊÁv\x0013Ì`Ä³vôò\x0010Ý~<\x0005ÍØ´8?ÁxÒÁ1\x0001\x0017Çïx\x0003g,9ã\x000cN\x0010\x001d\x0016\x001awòÔ¹ 7:¢\x0007ß¯9Å¹©ín»\x0003\x001a,\x0015âÀ³è¸h6|@û\x000bvæÖj©Y/u\x0006¢àÅ\x0006\x0017KKyý\x0008/Sh\x0000­n¼l¾òÝm\x001ax-f|¦WÈ\x0013gPê\x0010\x0002µ\x0015§Ãii\x000f\x0015pæ.!x¡ÈÞ\x0008rü1À)|ß¨ôåPÝçÕËçÇõ¿]EI8©@\x0015\x001e#VJ\x0006\x0013\x0007azµv4ïzõòúäòxçdbß·(}9Ow\x001aò\Âf\x0001T\x0004äå8ÚkâR<]âéV<ÃÝÄ&Dª°\x00031r¡¢ÒÓ+§Ð	Ù\x0013\x001eöþrËÆa<xAl&b\x000bvògDÞ\x001aì\x0007[Föõ\x000b3.±ôt,	^µOms\x0011>-û­Zå¥[eJ,Ó&-Â</p><p>`LHËÒÊ\x0001ª¡â´©T¶¤²-ÂrtøeLí IXTÖ\x0007ÂêoÎjÂr%kÁ2´ø\x001e\x0003;©l^V,\x0008ËT¾Jr§¼ÄÙe8WíÕ"a\x0012+4¬<¯\az%úÞ¼ò­\x0017µ
+X±EZÚC£ñ\x001baÑf'ë·vÅµP\x0015=F@µé1r´$YòJ`\x00118i--xSw\x0018Ü3=KV\r¸°¤(ôÅå\x0006[\x0004§bU:^¶(ùèéíî¶r\x000b>\4®ß\x0006¥\x0017hSYé-Ù¢¸þ¯«Ò\x0010²EEn­F:]¼\x001a\x000e¸\x0014ßÅáí3ïbUïÙÝÇM½ç\x0014¡qi/èÕSë\x0012w¬W\x0007öÒõ\x0007¼4àu3º\x0019ÇÏ~º»Ý³Ù¬^q\x0012£°Îo\x001f4Äºù³¯ÏNwn;îÏ{\x0015iÞk+¢\x0015Tí\x0017qTb[CÍÊ
éLhJB3Pr\x001e,n!HBÌÑp­ÆæÆ3âH1ì§Ùe\x0019º\x0003åçO7{¼\x0015\x000cò¤,¼é\Ön>77\x0007\x00197²¦î\x000cÜo.®_ï©\x0005ý±¾²\x000cKMÄBÄÀûÁr\x0015"/\x0007\x001b.¦i\x0003Ô% n\x0007ô.ò\x00060Dw@@S\x0002f@v\x000f;Ú4d¨úçcâ¦¡å¶d´ín#DcÙBqÂ©|\x0014\x0007c;m®tíÑRµ)@\x001aV9§r\x0003¤<À×ö%¤oÄQ\x001bùR+\x001e\x0005â"½zÆá(n\x001bd(!C»$Ékë´ÍÊó½6z0ï1\x0011Ò»zÇª¨¼Þ­\x0015ýf¿9¸¯*=} Èl°rx\x0000éñ\x0004"U\x0012©©DØ¥\x001bh?}\x000cyIpö¢\x0010ÃÓ§ é\x0012IO\x0016RàÌ\x001fN{ãE\x001eÚS®ÀZÑwì\x001bLd&K	8\x0002/·y	¼å</p><p>	\x001bFæ\x0000OA²%¤'\x0013¥[\x0008ôæñ×ÖD7ÿ(¹ÈM&Â¹\x001dÉ®s:Ï\x001f³XDìï&«)xÝë,âi\x000f¾\x0019Ïò¸\x0008\x000e¹¡BOø|3¥l?gë\x000c\x001en2¹Z?ßî*i!KNÄl¬lÉ©l¬¤\x001epÉÕñõéÎ\x0016ÆÔ%¦\x0016wð Z²ÚyK\x0008n\x001c?7a\x0012ÓÌÁÔ)JÞEXÖÙ\x001cQ\x001aÉ:4QÚÒÎ T*\x0017\x0007aIªåä\x0008{µj$+ÖDéJJ·LvH\x0013D9ìd0a(	Ã\x001c9rWVLûVR\x0011æèÀÑ4\x0005Q^B\x0004~èÝõ/ëO7«o\x001f\x001enî¿ÜîÖ<\x0002+/È×uã\x0017uOpkj!b%ÐñëÕ·\x0017W'çïNwêFB´%¢mBÄ".\x0011gO2 yÜe\x0014cÌ¤[LèJB×L\x0018ô\x0011Ç®sß*Ü\x001b\x000eô«ÞWCèKBß.CÃ»\x0005#\\x001a\x001aüýË,Ã\x0003 Æ\x00121¶##Êè®\x0008>åy²ªW½!\x00133\x0008e}WÚ.KW0\x001byiÔ2h'ò\x0016\x000b.ïÇ5¼(ï3o\x001e»ùc§ÆVç"D­1íëËAøûÌÇN~ØU'ëûQ\x0003ß½Õ­?4fWRñaÆÓf>²\x001f\x0000Ùù\x001e¹R<î\x0012\x001cÇ\x001cþsÜWÙ¯\él±½a+FÓ%nEÃIã,;Ñlà¸©ì\x000fè¸\x001cõëg\x0015£ÌîÇd<í±"¥\x0016
6ú¦¾S½\x0002ýf<[âÙfémÒfð.\x001bªP°\x001fþX¥©tªuïuþ|{óü;VçÞ=<ï¼\x001b8d\x0018'tm\x0018±ÛN\x001c1\x00165×pÃ÷§'×ÇúÜ³ë8ôc¡.Ã;üæÏ?­o\x001fo÷X7¼ºÛHm)\x000c­¸é¼Û\2jÞ¼9¹:>½<@jJÒ¾Í=\x0014»Pi÷¦îþØnÖêî¤*åAÊú¾º võn}{ÿô\x001f¯\x001evgF$øÐfolCN{Lq6\x0010-Ï6ý\x001a
è»ãÓó«Õ«Ý)\x0012ÛÏ?XQ\x000e3úðü¯ÛO÷_w\x001b\x0004\x0016cFÅ©\x000cx£ó&uÀñ¼¸þþôõù?v|uÕ7lU¿|üõãúþ\x0013þûúùãíÃÎe'`ÉÒ
>ËëLy«²ýÕMEYÒëËãó×øïÇ×¯N/Í'ú\x001e4</p><p>¢æ)2/ànÌÙzõòñáö÷öÅÃíî!2iMÿ\x0008]ÿn\x000cê\x000cp\x000ejï\x001aÎãËËÓ¿w/.NßÑÓ1\x001fù×ÃÓ?5	°j\x000cyFýóùWüÃå\x0003~^+\x0012\x0001 þü÷Ýí}'3©´i\x0012zÐ88­óþ¤\x0013ZuRÀc\x001a¾99;=/ú\x0003®Qý¼y¸¼øÇß><|þü\x000cSú÷mBø»¨yÁ§"\x0016$\x000cØ\x001eÜK4±q)!\x001cc=PÂûÜy-puÓ\x0000LOLªg\x000c-\x00021óDè$:¤\x0008áàé>²7,ÂH>þRB¸^v\x00089
"\x0004i</p><p>DhR\x000b\x0008ÈÐÒÞ×Y\x001f~	Oï+!©@Ü tÿtó´\x000c_»Ö\x0005xöpæe:~J1åÞ\x000f"#õw½zsq~urµ(}Õ\x0016"CCÆ(­\x0012Ý\x001ey\x0006¢\x0005sàk\x0002Ò8§xº.ötAS&\x0006ì2	ÁÙ\x000cm@S R2%°:¥¦\x0012\x0013T©1\x0008k\x0019ÃOÃ{\x0011É¦\x001e'@\x001262	íH·?ÿ|{ÿ8ô\x0002`)ïíûÛ®=l</p><p>ã½]çUPÒuÓàu×¸Â\x0019Z^\x0018ÖþXÈ{úâôäòÝ~²æF\x0006G)
Ö\x000b</p><p>\x0017Út¦T²ß5\x0018qX§¶õ\x0014þD08âÀ¢M\x0005 3©:\x001fÈxÕN3Ù½}xï¹1Ôn\x0000pçñêWtÒðB%GÂgL±=Ðð¼Ð¤>^`¤\x0000ÜØñ**½9Ht»AÒ³-11DÞ'»\x0011|TÒ×k!2:­\\x0004·\x0000ã¥/\x0017tª	\x0007"|m\x0010U|\x0012¤T\x001e~5ËÆeÄÃ^æ\x0012Uª|\x0012v8K!É\x0008\Ò$"%Ù\x001aÄ½%@*öÑ\x001cÛVÒK¬O\x001fÍ*"ÒzHoN&ê©òIH.\x001c)BÂ\x0015vÉ</p><p>.¥©\x0001IREÛ\$ø«eÓAÒ RAP\x001e·évRòR*:H8px\x0011\x0012"Ùt\x0000É¥\x0011¸n8\x0011E&ÒË.\x001b.[UMß
g¼c\x0018
ÀÞ\x000c8d\x0000¼N[ç4¼ÐfÈ*\x0004WC5©m3`\Bg7EUpX5=¿BeDðW«&%©áÍHû8ÈXºo@d\x0019I,ºnØ\x0000ªÚÎv·¦¦{p±\x0006\x0018§làª\x0006aÓ A
'jÎIÒÿ¼×ÿú4h9uÖÜãÃó>=3):% \x0002h;¥óÍ}([V@gÐ\x0001ã\x000e¶¿­¹ýµ`;ÃBÛçÇO»h\x0008d0iøS¥</p><p>ÜAëHQF'+1aíõåëàLE\x001eÿi\x0014:\x0005ßp=¦Hë­ÂÄÈ\x0014µ\x001f×B\x001eüi\x0014¬\x000eA\x0016>
\x0007B</p><p>§Â¹\x0014éD\x0001\x0002è:¶"b{dGáe\x0016E\x0013ÃþçðÏ\x0011úôËõãÇ]+\x0018ó>
V	\x0016\x0017\x0002%7Í\x001bÖ­j¯Fb\x0000`·¾{w|ùjÌn-Àz\x0011©`4i</p><p>À\x0014U#Xê@0k\x0017%Ã£L§­\x0002ÁzÐDª¿46*Í${¼7â\x0019ùoïÖ÷\x001f~¾Ùft\x0014in)}Í.</p><p>\x0010<%óQh#úçÝêíÙñùËoOÆÐþø5þüÕ ½¼{øx»\x0013,¤}K\x0019hr©\x0004\x0005\x001aÌ\x0018×Ë³W§\x0013¨¶\x000fÙ\x0014*ª«ÑÑU¸¬»£¢	8èèÊy\\x001fÔ/<ø!§íûÛ\x001b,\x0019ùéáþãn\x001f@¦É\x0013\x0001-\x0010æø\x0010)4\x0017­\x001b~p¿?=Á\x0011%´\x001f­ç½ME3"-þ\x0000÷\x0004ë1ÉöVl¸hÂ\x0001Øz~ÜT6åR±7- \x0017Õ±ÈÚÕX\x0005Ml=n*©\x001f\x0015¿ä\x0010\x0001öí³æ\x0017Ã®o\x0013[µ6³áì\x000b~\x001a%}PëXhñ\x0000\x001f´çãM\x0003Ó`¬u\x000e`\x0001\x0007J [Ì^\x0004[f9\x001b8ChX¤Éª¡zC`\x0013"\x0007Ñ¡\x0008g\x001bÛ':Up\x001d-
&\x0007\x001aï\x001dÊÆ\x001eqkàP¹µk7Ý5&3\x0019>kê×F¸%ç8ì-íúMc Ö,9GÓY¿éhG\x0013\x001c\x0008_¶+83§4ÙóÚ\x001cÑu°"11å×a+Ò0Íc:¯#ã£\x001bùÎzÄ.W¾[1pRÚ´5&½ZÉ\x0011òÂò3\x00078q[Ñl¸SIÌ\x0016RTD)ïóºü®nùØ\x0013á@Õ¦9>xâhá¹ôÚi6EÆ"¶MpðEÕ¯ëL4½÷Î¦Ñ(`T3Ý!$çÿV-{\x0008g0h"\x000b C÷®F\x0011\x0015e~1\x001cîOÒíg\x000eCÿ©*\x0002à Ç+Æ£|¡±â\x0000p (uûû`qô£L\x001dÐ¤3\x0007ZÎQîÐI?\x0017nýåñöÃmaþ¦®Ö®8gõfýøt{¿Ó{Ç9¤Tv\x0000¾\x0016½\^æ*«ËZZS]ÎãË«ÓóýXÉºlÄÂÎFz²\x0002G6¼\x0008\x001c_ÑuÜi\x000eVJ\x001a4b9}B\x001d Ë8ÔágÃ×ù,ÀJfe+V8¢o}"É\x0010÷T\x000fXªfÎÀb«­Ëp</p><p>AÁ;\x001fè3ò4!Ú¥\d\x00135ryÅòÒ</p><p>_ª$¯M©M\ú\x0019ÙähäÂ=ô¦Æô!MÈUJnémds£\x0015,lÊ§l¯</p><p>`6º\>µøÁß@6ü(6Î¶­\x000fvó)õ,0÷ÁÞßÞ\x001c\­ïïóô°Q6g$©V)@oèdÛ\x001a®9Ã$äh0æêøü<\x000fÛ·\x001d½ûç»\x001emÀÓÊ¹\x001cÜ
CxÂÖ\x001e4àm±&â\x0019ª\x0001O¤ÑòÒiA\x0007¼*£%\x001b
t½J®ét8éµ»©"zÉ	\x0000\x000c×\x0010Õ\x0010^z£æ|[{d\x0008\x000ft°¶ôm%}Û`Æ#ºûð¾~}úú*CÏ	íøñ#Î\x0012ß	\x0016pèc÷"\x0008ðìÒn|\x0011H(/z¾èu:¾|CÄ'0Q­)Ú\x0006\x0007á|N`\x0004C>¨²±ç63Q\x000ck:\x0013x#âÞXõÓ]~R¥ÖO­Ä\x001c)ýr÷õñaàË¡ýº»\x001e(`\x001c\x0013)ÐMy·èsLÍ\x000f!¡ýÇh-PAD±Û\x0006"0uÈ\x0013æßp\x0003£f\x0011\x000eLÇñJd·\x0012ü¤À'òä¹©á½èùîËý¯qDÏÿðç¿\x001f\x001fv\x001e#ï
¦&ºê\x0008Î[w¢ÈÕ	£:êË	LÛÊ}?SP´ö=tV~z²}\x000c\mÍxNg\x0017Ö'ûå·_~Û:Ý«×ë»»õýÇNiîäÂ T6\x0011,.øJX\x0014_Ä¿b@\x000b¬^\x001f\x001d¿B¹«<ã¹"|8Aõ\x001c±³§1\x0005³º	ÌÈ×\x0006V*Íé\x0002³Â\x0001 1Mz3I.Ybõ\x0003FF0éÉàYS\x0005êb5\x001eÁ¥`¥Jþ)qg{$E¡}Ï\x0007f¾ê/ë\x000fCé9,òø¼~\?ßí¬>16Rx0g¨ÏMzcÓ¸\x0006-A»
Ç°Ì\x0003TØñõÙXGÁÖËÏMcÃ¼xJ\x001dz¶æ\x0003Vï©E1^á0l\x0013[/?7Unp\x0007\Ll\x0000c)^\x0017È?ÆáØz\x0013[/\x00076ÍÅ4ß\x0008¿)'½\x0015&Ë-\x001c
tÁ\x0016]j·Âo\x001f\x0001ËRv8x½l½þôËúqðb¤ný¸3\x0003~.ab3	¥[»\x0014~µÃqº7\x0018¦\x0003ók?U_^\x0013¨¢¤\x0006èOv\x001a\x0018ÔÕÏR¿\x0008Eõ-T½á$*Å¥ëÚxÃ¥þA¤µPØ"äS7©¶²qÓ°<GÐMô,,P²°ÔBYmeº&\x001d,ÜÏGPóSJÚk*ôÇ¸ðÂFl<Y\x001a\x000cT\x001c2å5¸xÜ\x000c©HE8ðbk|÷`}øY_í`ô\x0004lé»n\x001e\x001f×»ôU¼w3è\x0000ª"½\x0011\x000e\x0017õ0f$A}öÍÉååñhË­ß\x00191Í\x0008Åmf\x001e|Xü</p><p>ó\x0016¤#´#¾u\x000bZ?01\x0011
w@¦pÃ¡ØÄfÉï·*ùý{Ùü×î?Õ·7Ï«W·OÝ¸³Û/7ëçßwfh¼¦$¹rf<ãD\x0007®\x0001\x0002s±</p><p>é\¯^^ucâÎ.Nß\x001c_ÿ}´n°à£:Î¿\x0016ßÓcxr\x0007¯ÄÕÅãç=t ce²ÐÀm\x0017,
K»¸°\x0015×\x0006Ä..ßtlÃ_¶ Ûn\x0015Bæ8\x0006«|à\x0000È\x0014¥\x001fL°r\x001eÙW¿~¾}?èýNM\x000bâP	ê¸\x0004Ç7­\x0014Ç\x0011ãÞN\x001dü"Ù{ûõ·/v8Hü¼zñxóÜ­\x001fØ\x0011R	GT	¤cÚ.!sâ</p><p>v8:|½zqyr}z¶i«\x0017y\x0002S\x000e</p><p>ÃÓ¤Ó</p><p>\x0011</p><p>Tò`\x001ciûNµÕ<ERúHg(\x0016\x0014·9â\x0012×L[-Çû|´¹\x0004<æè¾Óã=ÚuO¥Új3HEÅØ\x001bJ*eg}?ãÖòãç\x0001\x0007óËêÅúÓýÃÝÍÓî`æ\x000e\x0010­à°SÜ×EÃ-`q¸æÝêÅñëó³«±°OAV»SÉ0B@9Jk°/E¤
ßC\x0011\x0007=ß&²ºÀr*Ui÷/I¬±O©yÍ¥Â
úoMdµ;2\x000c;3HÌw\x000f%Ø\x0016Tø	fcù1å\x001fw\x001f~ûÏ\x0008õ&_[z\x0002®m\x0008©É×Z¦½ë)Ýª\x0005Q\x001d¡ÞO\x0013ª(ú</p><p>¦kÄl\x0016\x0012ÙHyyí½\FTç:&È\x0008ç\x000f\x0008úp8xNÒü\x0001êa×Î]\x0003Q\x0019¯D¤À¬I½\x0007 ÅuZ)#m´\x0014
FãB·\x0013}ü*ÿùÛçþW{^½~xþºÓÖÂÉ´\x0001ÜGaÒIéb0äÕ</p><p>S«u\x001a[úúâú\x001f£¦sASÈg\x0012Mà\x00110?%Fsº"?I=#à´m\x001f é0E\x000cs</p><p>R¹pÎÆÅH=sVõÛø&ÐÜ¼ÿãéÞm]/\x001c¨qÿ£¥nvT-îþIí>J*¢>\x000c'È*\x0016ý´kÙs|~S¥N®®Æbª\x0005Z\x0015\x001ef°</p><p>2å:ÁqÐ\x0014\x0006¥Î\x0015ËøBïeËîD
÷O÷óûÏÿ9h\x0019§­Î·ë*Üâ+Ü	kSP5¢¢åÇÓë¸ÑùôxT\x0017h\x0003-,\x0013ÑÒÜ\x000fk+,Q¡çµ\íhw_?üñ¯»\x0011©Mq\x0011³T l°ÔÈ</p><p>ïp :\x0018-­«ÒA\x001cFûòûïïïÿ5ìêÜ­Wï>"½ÝuÜÀô3\x000fÇ8í7\x0005#l8\x000fìÝKÐ¦§cW¡ëÒ©pà\x0018æÖ\x0002Åñ/·±²¼\x0018ñ\x0011÷ÓýþüÓoëÏ#\x001eÏÃóÿü»\x001bÝAuo¢íÂa¤ñ\x0005å×\x0000r¤Çõ\x001a;\x0019áÄÍ&\x0003;KO\x000fvä¼½]ÿëv_DB;êb\x0001'Z\x001cqK</p><p>×	\x0011F\x0013¸o¿?\x001d?mîù?}ð[vÖêÝúùîÃþü·é¤¡w~J»éîR{w|}örG\x0002«\x0000ªÞi@ð±(@n"VÚ&M+¢P\x0019j \x001a \x0005ªz\x0001&BIAh{(;JóiÉº¡©©ÊNb2¸¥(E¡»¹ú×<<ÜØ°©JN<MØ½à\x0012T\x0008iO\x001e\x0008ÊSQ­3½^êP¿þtóåN\x000eÅfnVo\x001f><í£JLÝ­Ãêô¼àV´aL]½½xyµ\x0003+>®{ú2àáLP\x0006O
)Ê#©ÆÆ£h\x0006\x001d=oÏ\x001föái½}ùîxä\x001füë×=c0°9Î ¼¨\x001bÅsë\x000fr úe'ÿÁ¿þctP@ÁWù\x0016>kÑ\x001c\x0003¯9\x0017*<7}à<¶Ù|î÷`~þ×¶6tÌ°Ã*\x0014öW¤Ö\x0000#rg¬</p><p>C</p><p>uÏ1+ªO:
	\x001dI\x001fÓ±mhòx\x001c\x001fÄÐT}ÅiHÂç=GauØã´é\x001e$¯Ãô:âËê»5ü\x0017wZª{ °XDòÎh\x001cµãLß\x001d_A</p><p>®íü\x0014.\x001cfX|z\x0018L\x0019JQY;^þ¹Lüñá§µê\x000bP_ï\x001f\x001f?î¼8XÂZÂb	h</p><p>\x001e9j\x0007Æ±xü\x000bPa8;âÕèE,è¶è©t`g¥\x0005\x0013\x001aSaÕÎ¾26ÑûùÌ¯îÓO#öà\x000f?ßÞï.ëÝúñ\x0014\x000eHGÜû£\x0001~d)\x0019¼üöô|4 ¸\x0001Û.9\x0002&tÚu\x000bzTÄ#Â»ÀK!z°F\x001d£Ýdw¸TlØ¯YýcOù½ï@º\¨\x000bø:uå÷z¬</p><p>CåiXùÃh\x0005müùéÃÝÇ\x0001\x0017\x000fp°öÄCª\x0014Pj\x000e,yÒ\x0015</p><p>\x001cÜA\x0017\x0017pÆpÞÀsqÓ\x000f/°=\x0010s³ë\x0015a\x0002o§²PÑÓ¡R6û?®£Q¡î#\x0017Ñ0w·!ë#©\x0012I5"y._W Dqtcä¨\x0003ÌÔ:[°\x001bJþøñI~ùôPÄ»sn§ÛHPäßNáØ?þzsÿ(\x0006ü@Bq</p><p>7cu\x0013\x0007ð!¥éà§"ÚS8ÍoOÎ¯6Yá4æ&M2îþ`\x001e~s÷7å\x0008Ò"Q½zþj§¡F\x0010CuãÔw&m»ÆÑÚ´èJÎ\x0006ÎÀjF\x0015ôÓN¬ÔöWÀÒ?Þ¾¿{ÏõH¢Ëç§nBv ó£ÿöÝÍý\x001fë§\x0014>Âùy!s¤\x0011\x0011C
ÃØ.|ôÝÉù\x000fà¹Ã?ûòúª\x001c]¹ðÕ?Ä²÷\x000fÿÔ´\</p><p>4¦\x001a²èlj
.õ¡Nýçãº'2\x00046?ÔË¤^=><ÿñuÇàðµ@'XåR\x001ape$}\x0018]\x0002m¯¿º¼¸þal¨ù\x0006L\x0012L\x00062\x0015;2¯È	Áóñr\x0011«À\\x000b\x0018ö§3äN\x0001L\x001b&KÊz6¯È|\x000b\x0019Ï#±\x0019\x001cKf0lÙ·\x0015Xl\x00003^ðõ\x0007U@\x001d»¡ÛPÈ\WIÖN¦Cñ¤\x001fê"b°\x0003\x001eoo\x001eGï£ÀNÝ\x000eL`uJ</p><p>¢YÍëYép\x0004¶)p\x0003+à\x0012\ýd¡$\x000bMd2âsVq;q4Nåm_Ö.AÐdÔÎf±\x0019·hÉeh®Bs
h\x0006s©Ý4g'±^¢ \x0008[çÌ¢\x000fZ\\x0002DMh`­\x0018^íiÐîÜToi\x0012x\x0015r	Õ5MlÉÞñþ\x0003ðó\x0015-±i!ï|°ú~¶\x001cµ.Ü IhXäf(ªEµn\x0011®Èt\x001b?¢Õ±:f¡Y^±bÓ±ùh¦B3mh24l\x0010$6Ã\x0003</p><p>.¨²\x0015mb£¯é"×)FlSJ`&ÚeB«4jÓ\x001c8ª&\x001dv¡%6Ò\x001cVECUOjy\x000b@f>µ\x0006¥5ÅOy\x0011I3\x0018ç³UZM5i5,UiÕ\x0010ZòP\x0016e[£º9³Ù´(Ùªá/ûå&L\x001aBç°#\x0002Ïp9ÈÚ¶Æ/®4®nÒ¸ÁÊÔéè¤2Í¶</p><p>\x000bH:4\x001dý"«+«t..3£
\x000edJJ-Fþ¤nÖÕÖÕMZ\x0017§£¦ML¶@n\x0002¼¦ËÄVi]Ý¤uCØ6«iRjÄî\x000e\x0012Åÿ©\x000bØ*­«´.\x0013K5yö'5\x0017Ü1Ø*Å«\x0014oð	Ì\x0019EEL >x¨1zÚÕ¾\x0002óM`B¦$-\x0008M\x0007\x001a\x0001º½\x0003¬ã]ÄV=	ºéI\x0008à\x001eÐúg·yâ õ\x0001R[t\x000fL¥uMÖÅ`¦ñùE rÖç\x0017aÑ'5j3mªÍTQ\x0008l¢ÛnÚ±Yö\x000fìFsÌg«ôiÓ\x001fÆ§z¾ô"\x0018bÓaó$,c«î¨i»£î\x0001¶Û&Å&#ë\g\x0017é\x000eS]\x0003Ót
º\x000cé5e¨.JÜ3Øi\x000f[]\x0003Ût
¼ËK\x0003­ð\x001ckÄÙ5¦ÔLã£ë§\x001f8ÝðúöîýÍãÓêüö\x0013;ð2¦NiÁÕ\x0011lÜä¼8øëJ¹]¬^½8¹¼Z¾\x0006ÒýpªSmpQÐZU¥¡á\x0011ó\x0004ç+'a\x0006.át\x001b§]\x0000g=» 7XrÞÁæJ6×Æfc;ä\x0014¶!¦\x0015wàQQÁIå\x0017Âù\x0012Î7</p><p>ÎbH²\x0013ãùÁ\x0011ÞPþªÑéep¡\x000bGN§j\\x001c|àTû\x0014-oºÆeñq\x0019\,áâ_\x000bNJF:Çß\x0015^0~Q­#¿Ù©®'z	]¥Jd.\x0017öË*Ì=§\x001bá¨k\x0013W\x0018p¦3mp`Ãèpù­"EG­ûHW¹Î3è*e"Û´Ô2b¸4ÐÌRñ|\x000fÉM·L
ËêÂÊ¶\x001b¹è\x0005\x0003ÇêàhH\x0004V\x0017,Ô&ª~À\x001aO\x000f\x000cçáGÂyarºsîÕÜt°ù¡ló9{~úºjFÐp)p \x0004d·²5}Uc9\x0001Ù¿\x0011]àõÕ·]GÍ^0[Ù\x00160°,S<Du\x001bPB\x00023´M\f¹\x0012ÌµÁáOÖ¯</p><p>Rä)iºÃÕ;ÀRÖzÊT¾JIÚZ	Ty_ô9£\x000eçß.\x0011W(ÁB¸°ÑFæ\x000c7\x0005ìáó)>`n¸öÅ\x0012,¶H\x000cíñ¤mqÐ Åw=\x0012ã4¶þ¥l\x0002+\x001eQ\x0000ãGtÈeuG«\x0012`I)©LµÅ.ÆÖáJbR³sÝVª%§¬x=Ì´|M!(q`©\x0015=âþó\x000c¶D[ÈJ[È\x0016u¡¤e\x0007\x0001;4È\x001eò2j&[rüUuÊTË)SfD¸nôrÄ\x0000ç?²ÈêHÛt2¥z\x001e\x001f¼ªÚ_\x0005p_º¢ÿÛç»q[\x0012Ln\x001eëªgé
0ß\x0000_\x0006gÅõX\x0007÷®«û?½¸>;ÙÏªKV=Ur6\x0017ûPù;\x001bëÉ<BÍr\x0018XSÂ9°&zZçº½\x0015©/\x001aÉFº×æ@µ%¬'Y¯RbU\x001bi8²	b\x0012¬\x0017ºÔÓKX}Éêg±¢qÐµ6\x0000¬É¥çN:u*\x001c\x00066°q\x001e,Î°é¦¶Z²ÒtÒÂX¨s\x0018ÉJYÂâã5\x0016g\x0014\x0011­5Ô \x000fF4¥S<ªÒÃÐVgVÎ;´ ßÓ\x001ac u9°ì¢fZ\x001f\x000eD[Z9óØÚ\x0016ë85lô¬\x001bz</p><p>p\x0006ÿ`«S+ç\x001d[%Óº$Y²A¼r|j½?îþÇ÷Ý\x0006½RºøË¬«fRç9VÝ)j²«F1s¯¢¦\x0017FÜÈóÓ6?`\x0008øõãúþ#Ö ?\x0005Øaë*\x001d'Ü¤ õ</p><p>¼¶P\x0002¯/Ï_a\x0019ê.ñEîb-`Ô$\x0018Á£\x0004\x0003hÀ\x0019eßJ©0ºÑÓ$\x0003\x0006\x0012O\ÿ!it\x001b\x0008Æ\x00047Å,v\x001a\x000bx(ÉºP`_\x001c©ô®H#¹bR»q%\x0006£5\x0007ä\x001drÑW]Ðkñ%\x0006AF*¿M\x0019I³Æ\x0001Fº)0a\x001aµdWÁg²\#U.lÕ3\x0005\x0013K8%ÒÆE§lðl7a©!ÄªÚª\x0006Â³E-#&\x001e`ÅÑCL´¦y p
«²D´\x0005¦VyÓt^Àè*2­Ní\x0007Àä3£\x0007S©<9Mçy°\x0014È\x000fÃí@z¶*!ISé\x00199MÑouô\x000c®ü KÀ!hþ3\x000b¦ºÚrÚÝ\x000eX@æ( ®X4Jj\x000e9W	¬\x0016ênËi;h~\x000f\x000c\x001cHéxÅA\\x0016^Î©.·v»5Tr­¬\x0008¬ö¨\x0018\x001c\x0004£ç	FUw[M»Û\x0001Þ\x0003>\x0013x\x000c¹H±7)g^'UÝm5ñnã[N°ï¶2ÂzªªÛl¡©íi\x001b§ËSs23	`H=W6A£¦Y41hºÜÊ¹\\x000b/=}'°Læ\x0019\x0011Em2Â§&°\x0015\x0001J³ÓðTò}23¿SeÑ¨i&MÀsëówô´Ù|§4¦Q\x00135¡AñNéhs1¦K\x0007\x0006Å¼§[UªFMR5\x0018 g£\x0006\x000eP\x001d£U>\x0014hÓygXW÷[OºßV</p><p>Çf
î téM°Þñ!Vó4®®·x½Cà¬ÆD\x00155FÍ\x0015Mí¯LºÞVJfëâò9\x001c\¦)ã¥-4ÕýÖî·\x0015¦[â´Ç\x001dÈ1b¦êÓ]£'Ù5V\x001afÕ¢Ñ\x0010ÙÂ</p><p></p><p>>Ä3Ý\x0004]\x00196zaÓex\x00024É{rÂ\x0001~wÁu¥nô$uTÎ© h\x0001Xä\x00003,])\x001b=MÙHÆIß)z.Ð^q!ZY3Ý\x0000c*ÃÆL2làÐHæÂ¡\x0011\ðë\x0014¿Þ¢ªîj¡©4¨ùÐáç[²\x0001ê\x0002\x0017`tnâ,JõIª¯ËëC³\x0014=](ËæpZk<¦R}fêS©C§£±9X³l6ÆÊÆTªÏLS}Jld\x0003®¦ÔPiô<CËT¶dÛX8®T­é\x001eÏ\x00140å>Ã8÷\x0010WÏLÓ|ø\x0014hºRX\x0005KÑÛ`¨</p><p>6Z9¦Ò|fæ\x0003\x0003/\x0006\x0018J×x\x000e«Yøã<³ÏVWÊN»RÊ)Î®ã	r\Àý\x0005´	}\x0006Mu¥ì´+¥eGJ\x001aË¶
\x000e¡^è8ï~ÛêFÙ7Êû4\x001dÙáàXvw}tü¡´÷`Ú:\x0018;ÍÐp£|z0±fÂ|àSgOð3ís[Ýo;ñ~ënÉnGã=w_{£X6j¦[g«+e'^)*MÅA±äîzf±àóÔ°«o7íùî\x000c\x0008G4Y×\x0004Å½Â!úyGØUÏ·ö|k+Å\x0005v~§ç;DÁ³\x0005¤÷|»êv»·Û\x0006\[ØÑ¨È²"\x0013rÞ¡qÕõvÓ®7^(*\x0012¿¨`5_(;3hãª7ÊM{£4xuÆ\x0019¸ÜçEq	ëç¦Z\uÜ´ë¤1=GÁºV:5G+\x0004agFúdÝL\x00016üeJ\x001c	|p*Ô\x001aÜ^j£uìK9ÓúN~ÍQåüü\x000f}¸½\x001a­fÂ²if0NîÐ\Í¤ÝLî\x0018¨æ{yñæíÅéùÕ®r&Ó/\x00112ª¬°Ã"¡å®c£¹7/\x00187P4×fJ4Ó&\x0002\x0007Ø\x0012yh\x0001¸§tÖY&5[¢Ù&4\\x0013Gh>V`«5T/þ\x000c4W¢¹\x0016´@\x000eªHÓ8SW/\x0015éÈâ@Át\x0003W(¹B\x0013WÄ\x0011¸IoáÊD¦À=½Þ
\x0015g6Å,¶ÞNJ_\x000bL\ðDNËO_ÕmÜLVd$¬¬µ 4Ï%\x0007h3±\x001f«¸¬Èú¡ú÷\x00064Y¡É&©á^;ÒiÊòQÓì*ù\x0010¡U*M¶é4¡\x0008
\x0006îéÕR²â°~ÑYâM\x0003\x0017ºPo;Ö9òa\x0013/ÚoTidó\x0015oS\x001d¹\x0017:¦-G)`Ì\x0013(¼\x00143å¦y úæbôÕóêÍúëÍÓêãÿùoÿýäÃÃ®ê*øÒQÌw¬D¸¡\x001c«û.RêõêÍñ?N®V¯V'//vViT[`ê\x0019&}a¥)`iîB<Sâ\x0019x¸ÕÝ\x0014cäÀBÔ<×Oè¾òfLWbºyRäøNk\x0016@)\x0015Ælõhe,Û |RÍÍàIêMl¯[º¥ð¡\x000c\x001cM\x001bñÑÌY]\x001c9çæ\x0018'ØÁÃå`]\x000c'j\x0018öÃ«¨ßLNUÉSÍ'Üðd&(3'Mâô\U!\x0006¦¹4cÖzh8íf*\ò¤*\x00013rU\x0001Üôí~ùfÎê¦«9WÝ*Åª\x00164g_Á»oÑÀ°´ÉR\x001f«ÂNø\x0001\x000b;ßÞ­?Ü¬¾[øí\x0019ÞW7\x001fÖ÷O;ü5\ÚÃãVs $\x000ftãõ\x0012ÄøöìøåÉê»ãÿßõ	¾<>¿¨KDÝH\x0001</p><p>\x001d2÷µçl¡qJÏG4¾'EPz)ööáñi}{×\x0015ò~³s2Ë}§D\x0016ótT5`Y¼½¸¼:>=ëªx¿Ù5È1U©f`bg\x001bQzvê
Ümª:')uI©Û)Á¦àº7+Y¸\x001a\x0006æ9=Ø²ÕiJL3çëÍDÜÍ\x0014'ë£ÕPÿb3¦+1Ý\x000cÌ¨ø%wàÔÓ$½<£\x000b¤©ý\x00010C\x0019f|t`£0\x0003Ä\x0013ªZ.úäÁõ®9\x001cªºÙäûÛO÷7ãæ9¼düje-u^Àåç!\x000e·p}úúüdqÎ`ª\x0004SM`.R\x000f\x0016Æ/¡é®D]¾3ÈtI¦[ÈLt\x0014 Ô#w4Ë7\x0004î{«êíf ¹\x0012Í5	MZº\x0013Z\x001bMN*N\x001d·ä¹eßÓh¾IjÆsë\x00164í/xö\x000epWÉ\x0012°ÑÝÝ\x0000ÑD¦$wªhð\x000eRAp;
¢5ËØªK nvC4Ö\x001c¤Öûà²o\x001aÅ\6ß7³¼(
+Po»CH+Òèyài¡úÃXç</p><p>TÚ\x0004\x001cUâ¨é81í\x001dLö½á¹\\x001c\e\x000c\x001aLId¦\x0013\x0019.0Â3ÅuÜÞ²lúH¶D²`ë\x0003+Yh9ã&\x001bûSj\x001a\Iä&\x0013§3\x0018p|8«24Àa"/üt\x0019\x0019
}­lH@ûB¶e}Õ¦ß5Üúf)Üu\x0007PÅ%'SªbóF&]1é©L8V*\x001dÁ)eKV³Z\x0002&áÆûù\x0018¨:Û²ápÿß\x0013Ò&\x0000Ñ)%Ñ¢(ÅÉxªÐR<×3ÄÙGIUJI5h¥Àáu
AÔÐ\x0011r±³oªt®\x0004@SÒóàÊsÄêÑ4N$úo(Þ¶ÕÝÿùoÿýÛçÛ;ZÊ:^¯JO</p><p>.*¦Îç\x0010\\x0008[`«³Õ·×§gÝ.Ö½pªSpÖ\x001fQEY1ª¨á²[G«Mlº
L\x0003®ÙÔ?¨sKºØò\x001eàL	g\x001aáºAY\x001dìÙâJ\x000e\x0016ÜÒ\x0012Ml¶d³­\x001f\x0007³\x0002æ¤¹ãâ3\x0010á2¹¹Í5²)ÁªLáÐØT.MËZ±qû6±ùÍ·~SîäW8yÆð;á¶§\x001a5Á\x0012.´Á V¸\x00128«øü²\x0013\x0017K¸Ø*¹MÊFðjÙ¦Oþ¬[Á½\x0016¸Â)C\x0005,\x001aE\x00174\x0007N$æHt&+\x0012Õ\x001f4ÚHWi`Ù¨×ßW\x0019¦¦\x001c­i\x0013É®Rs²QÏ	«±Ü.\x0015H\x0006\x001e\x0012\x000fÐ\\x0000­úÃ\x0001\x001béªc'\x001bÏ\x001d¶WEöD\x0004»kVyóT\x0008½\x001f~¨Âa¸\x0013÷õúñã.É#IÛs¢¡=\x0011\x0014 ¯ÏñÁ\x001d\ûúøòU\x0001×Ò%nÊÃÁ÷\x0007,/¿pfpvÑ\x0004&[2Ù&&é\x0014îØÏíù¹â·ÔúáVû¡B	\x0015Ú\x0004\x0005&dÒh2®#!©[ÍRe·\x0005*P±QR\x0001ÅÓI*l,"ky¯·ó dõùdã÷Ã{ôý\WjNÃòÊ#«çQ¹ÊµQâ¢
\x0012(+Í¹Í§Ê\x000e}'PùÊ7ÊÊã\x0018Ç$+\x000bp©y-ËJ\x000fU÷S\x0015¹í\Ë\x0016*ðzº]msz¾uÞ¦ef\x0018í Æô³f{í²\x001ewë§õ®eÔc:\x001eË¤hå¥ñåØÕìR\x001egÇWÇ»#\x0004§J8Õ\x0008\x0017ÒsCÿàà¬°/ë\x0015æÀé\x0012N7ÂyÕÍ¥åíK»Ã­(µü\x001c8[ÂÙ68+=pï¦%d9'h±cv\x0016\x0008±WÆ\x0015b\x0019ù}}ûx3\x001e>°FÈ#¶\x0004÷iEË\x0001\x0004\F¹\x001d@x}zy²³¶ L	e&Cé`¨]b¤¬~¼\x0005\x00045`XOr%\x000ee5}B[{©Ê-ru1h³HËT&_2ùéLÆ\x000fLÝRÑTëï²µå\x0007RÍS¡B	\x0015\x001a $ï\x001aèP:âêu7\x0010ú\x000cUNUáî>*×:Æ4Áº£r4Ùº¡pâT(YAÉÉP</p><p>´(÷¨Üh\x0019\x0004ûh.nûhÓ©* §ë\x0004-e>éF±i\x0013\x000c9qûù|ªJ'ÈéJ¡ë¼LPAozÖ$\x000f\x000fÁNeªT®\x0013TÔH\x0007êIæFY©6EÍ\x0003aó©TÕýÓ/ ôÅVBðN\x001a[`½ÿíTuùÔôË×fç®\x0011·1ÅÜ52ÿò©úå~Ì±ßPr\x0012&W}»¼(\x0005zJUGJM?R\x0012÷¬Q@?8L^§X¡à\x0014Ñs\x000c=Ï\x001eÎSáÙ?¯^<Ü\x001dsóøññfý<jÇXlJ\x0005\x0012xÊ\x0002»xAâ ¼ëÕS0fN._]\x001c_ïÇT%¦é
O+^qÚ?D\x001c\x0018RÛÌ¨KFÝÎ\x0008²äé´Ò¹#G\x0015\x001dyM\x0000ò\x0003`\x0012ÓÌ\x0010%¨¸ôDiì\x0015NqÐÝ
\x0012¦\x001fð1miÛ1±J?¸ iLÁZ8\x0014\x001c¦4SºÒÍøæóãÝ¹äÒ''²0Õ@(£\x0019Ó~0á¥N©hÆÐ0</p><p>\x0014æ!Nf()Ã\x000bÄvfGiéþ\x0002CËê[)\x000b{\x00135¦)\x0015%ôt\x0017É¢\x0012¤<5\x001füÁ\x0003HSV÷\Î¸èZqþ\x000c8Aµt<O¯
Ò
DnÛÕfÕDÜ©ÎrBòtZ}\x00086«%\x001c¢Î´a Ð5V÷"9è×)ðOw·_vÍñ\x0013GFÞkF½2ØÃE«Û%Õ«³ÕÉë³Ów£3u/Pª	J\x0019i\x0005\x0016Åfù­âU[qÛ_ÜPí.Át\x001b<¢Zd©¸ùi3DTË¡TÕT,[bÙ&,0\x0011\x0005rç^zÅëµÀ§\x001cJRMår%kãb\x000f
äå7Ã\x0007yw\x000fÜ¡üÔT0_ù60ÃM\x0019.Í!H`¼"Gí¾Ý\x0006°P6°ÀÓO±ÅÁóO. Õz{CN\x0003X,Áb\x0013U<ÏÁW¥R0§\x001c\x000fìTÎUöÒ~\x0006y\x001f\x0018<V4ÀÙ<6Q¹Àc²íK)kÍÚ¦ZÝæVÚÍßÜ_a·\x001b\x0017\x001aÀ*í*ÛÔk4yÌ¹
|úµPYd)÷©d\x001em\x000c<\x000cJh;\x001cROÇßñ\x000cLíäVø¤¬R\x0018²McÄÈOÇêq\x000bnC1r°b*Yu1eÛÍÄü\x000b¥b\x0000Eq\x000c?JF÷¡N#ëj\x000b_\x0015°­Wß<Ü?½¿ææi¼ý­\x001bIubÒE\x000eýÚ¼=noÂÌÕ7\x0017çW/.ÎÏO®vµ¿ {æOhþ~þuýå\x000bsîN¯)x0
E\x0011q£\x001b\x000fã\x0001{¾zÔOß¼=~÷){ùµ1<Uâ©6<\\x000eCù÷¸éZw\x001cÉ°¾LþÍ¢3%i¥\x000b9µÂéU@_!g\x001bÌB<Wâ¹ÆokCNÐf¡Z;ïU®¨°ó¥×_L\x0012l7õÛõ/\x000fã»3µÈc¢±ÇÍsø2mnl¿òÛãï.v®õì/)	¶¿z7Â]%´r\x000e\x0017\x0018óp1Î\x0001\x001a·\x0008L`ºMby³rÀ­\x000bDÆù6g­X&3[¢Ù&ád-Oùð\\x0004\x001e$à&ôÃ¡h¾DóMhNp\x0011¿·#µÞóþ6c}Ð2Õe·*ïa3S\x0000\x001eLr\x001e\x000céxÖªÑÖÎbº_â¬7%ÎØ\x0002ÿ¸¾ÝµAÐr\x000fÂòDz\x00136F¸\x001b¡~µ°ñýòøtWz^÷õ¦xx?\x0012¶bq\x0013Mî£Ës7¶\x001céH±D¢<â1\x0006y$by¼ò¶\x000f5¨h¢ÑE\x0013Í\x0004¤À;´\x0012y´'Î¤~¬­</p><p>æéLÕ¿\x0006\x0003</p><p>\µ.2º\x0010.ô\x000b§3ùÉOf².G±yÉF\x0014yÆqØr4©:MròqÂj</p><p>z\x000fµÏûÕ£¦
Nbþ³Iþ3mìV©èËÇÛßWonïînv¬\x0007CÂ¸Âä\x001cª5Üêç\x001ev¦ÄËËÓ¿¯ÞìR§¦ÿp\x001b[õROFÒ¥©ác°QÖ5þu¤.è±BÄ¤*ö</p><p>\x000e¸Ì\x0013Fp^ÔÝúùãom0,J}ªR¸\x0014t'¤\x001c\x0018vó¢Î¯_íüÞª_f¤b1-j</p><p>\x001a\x000e¥c\x0018iF&\x000eåaçXâö%hºDÓmh>o\x0011.e\x0011ÍvëV¸-A3%iB³F)ÜeÚ)\x0014\x001c\x0011$ó\x0011¿=,¦\x0005Íh¶	
L³@Rëæ\x001eàH 7ø¸íqU-\±ä-\ð0\x001cñ:xf*I\x0015yÑ\x001c£Õ\x0000&ëËÙt;Á/b\x0007ÀàíLçL:u(Pµ­º\x0002²é\x000eà&±ôÚn¡WGf36Û¨</p><p>²\x0005aUgL6\x001d2Ê_³ËJ\x0001Xä
%JYWs
X®=Æ?Â×<{xº\x00057øóÍýÓê\x000eË5p¸íÕÛÇñêÎä\x000eÓ´$÷ÝxÏKÎM5Jöìâê\x0014Üá7'çW«3¬ÝÀq·ïVo/Ë2Ï>¦*1ÕLLÇÊzax 79\x0011ËöÕYºÄÔs1\x0015ÏLòBl0¹ÊXÇ²=s\x0016¦)1ÍLLÅ½\x0012Êa.0yÚ½Óea\x0016¥-)í\J§üøÍl¸ëj\x0007Ý,LWbºX(JË\x001e]±#'\x001b]éKL?W¹ãÏÙlJ{ÅÚHÛ2j8\x000b3aþÑä<\x000eXßMG?º\x0011KõQ,1ãünIÊeµ¹¹èjé\x0015Ê!¤ÝÅ|ÎÈ©üpÄúHæ\x0011Tz\x001e%ªõ½\x000fß\x0005¨çÇîu<¾»»Ý3Â"P\x0016Ó(4Â<{º"ñòâú²{\x001aÏÎNw
Åb*UR©\x0006*ëó\x001aÙOâ]\x0017@eÇ©F\x000c	Ñ\x001f©.ºêÌu\x000f^æYgÁÑ'T¡;5KÊX¦\x0001Ëå6S\x001bM.{p\h¥EUÂ4\x0019KöFt¡?T¡x?\x001eA4\x001et\x0008/u{0D`Hùå@ç;\x0003	°(p\x0006@9T\x0002¶Ð\x001aéÂD¨i¶b\x0008ÆdB³«\x0016u</p><p>aQÅ\x000bj¨âo\x0017¡ñÜ2³\x0014¹ZÖ[ÇVuÔó	Uot\x001dÂ\x0016ÞÈêåÏ8>ón|\x000e©\x0001ÅF3:´\x0000\x001e*\x000ck¨¼\x0003¶õêå·8;ólç\x0010Ò k\x0015\x0002?Ô!ï×Ïÿºy¼ßu;¼uÜ"nqý	í\V<Â\x000e\x0017f\x000f[¾?¾þþäò|ç\x0015a@S\x0002V@áyh¹ÿ_8ÁZE\x000fG®¦\x0001öâkr\x0006ËsÏ\x001e\x001fîw\x0015;ê$Ä¦F\x000elÛ<Éë­°\x001fÏ=»¼8ß9Íö?®-;Îö£aq¤^\x000e¬F .ãÜË¡¦\x001f5éL7áª(¶n,oÌ³{½\x001cjh@s%kB\x0003u\x0017hWô<µGE»ØOÑµ\x0015C­Z;&IðÑ©\x000bFHvØ°WÕCS¿&°Ø/C²7ó5<µ÷;£ß:R4(jÓóÈ&sÕ\x0007î(\x0018nðÚï\x000eGÙ{f£ìMÂÜOçræ5â¾Ñä÷DÉ*ØáÔÔex¦Ä3x!?`\x0011\x001cI¢Ó¼þ\x0019Ç¯,¤³%m¤×E|+\x0002õ®R£¡C«j!+ñ\\x001bé$d\x0007×ÆÀÓíÈhØ	pª_A¤ªa/ºÚ¡]1åpD»\x0010¬Ni\x000cÕ-\x0010¦\x0014ÕPsmª\x0019\x0000¥K(=\x001d</p><p>\x0007OÒ\x0006kãó¸`\x0003\x0007\x0007·äLÆ2%iÀ</p><p>g­\x0018ÑM1HWÕÊÒä\x0006,[bÙ\x0006,)y_¨	Ý¨ÌTã¢r$yÉ7\x000c%Uh Â¹j\x0014¬õÙ\x001f'Áâ^Þ\x0005X±ÄÓ±Ôf\x001dÝô¸{Ë]7Ê.é©XeB K¹Kç	Üè¾Ë\x001cèäyæ¨ÏUÝDÙp\x0015\x0015N(Ðx\x0007Ç\x000cu³¾KC¥\x0002ú#WT=r/ÈÞSÇ¯zárÉûv¡ô\x0014aEÝ71t1²ã9\x0005V/o?ß<Ýþù¿\x001ewÔÄÈÛ'pe-ú÷ð^\x0015n{8Æu</p><p>\x0010­^¾9¹\x0002`ç\x0016¾O¤j6)Í-³&/\x001bfR\x001bãö,\x0019 ¦\x00045³@1ðÀû«ÁP¢8&¯þ\x0005	÷vRø;ô,'*\x001fúÝúöþiõúæñó:yïÖàPï\x0018Æ	Æ¦Ký}Ö	nú\x0001:Ý\x001c/½\x0018ÈÖ®Þ\x001d_­^\¾9N\x001eâ»cp¯ù*õiMIkÐ:`JMp}¸MÑûî\x0006j\x0005Fa·¢Ä+ké.\x0011/Æ¤¨­W\x000bISj\x0005õõz¡ríÀ®\x0002vK$FMÂoñ¦Q»\x0015ÍðXYy\x0000`UIX-06ê§\x0012\x0017\x0003ZÂsÌqàøÊ\x0010ëX/!v;Ò
ª\x0004¬©Ü×à\x000fq¯ý3!\x0004MÜ\x0001ë[O%\x0017£rà
\x0015oÏ\x000b\x000f¯¡,
\x0018½ñH"h\x0015£7î jBÅ8.°¤\x0019µ ä\x0017mñ@	Ètb8S=!ø­\x0012õÛÏ¿®\x001f?î\x0008¹ÜöÓ÷i$¬ãk8ËcuÍXNùjWù°ïù\x0016×/ºÞWÌÆðð©@³ÑØ\x0001å\x0010\x0016âù\x0012¯_x½\x000f\x000f«Ô©A{îcu÷t\x001f´Tz±Ämx8\x0016*SáÉçÜ	:HÜÓÔá<\x001dOö\x001b¥©:sW/no~\x001a¿\x001bRpÑ3£Â¸\SÃq¨sãzõâôäýXªÄR
Xhl\x0012ë¼3I©ÜÓgÂ\x0002,]bé\x0006,n\x0019Ý,WgJhSN­Ì$M/¨	?°öx{{óøx³ººý}WÞ\x0001Û©È\x0015</p><p>r³åW:\x0013û£ÈÞ\x001d|y²º:ýûî¤éE4\x0011M7¡®*¡åD«¹g.ö\x0007çÖhcïý</p><p>^mûï÷?íÄò\x001c)Äì´¤ÕÐ\x000c1gÇHïÜ\x001eÅX¦Ä2Ó±,èh¬\x001bê°â®Lc¸[\x001a|¡ÑÛ\x0013±le[°¤ )ïRÒÆæ&%?Üô8
ÉH®\x0011\x0016\x0004ò¬5¹¥k{ôÞd¦²EÚnµHïÂ</p><p>0I\x0011^\x0017ç¡N\x000cêÈ%+.ÙÂe\x0014á4¦fÒô£h"Û\x0016Î\x000f·!ïáòýKè«´ß7\x000fÏ_Vþ\x000fL<?ÿ>\x001e#\x0004Uê)-5+ÔI\x0012|äùdf  úÍÅõå»Õ1æ¯ÿ¾QºQðÖF3Ì\x0002\x000c\?e½\x001eÚ¬ÓÈhJFÓÎ¨6S\x0016±JR¼ÜäÑsC!à²¿\x001bZöwC?<ß-~çð~}7Féq@%\x001dÅnEQWW¬Lnøªººy×éÅõ\x0019Øà§x"ÏÏö\x0012ÔÌ\x0001ïL>´¹H)\x001cSO~¤\x001cÞqÛ</p><p>êJP7\x0003Ôà6¿äîJÝm\x0000Ììkµ\x001d\x0001A\x0019JÊ02ämuCî</p><p>K;=Ç\x0011ôv¥{\x0003(|ñÞE\x0017½yÁÇ÷\x001fnoî»
ëï×OOë\x001d;Ö­pb\x0008ÊN¢$Íe\x0006®ÕV\x0011\x000b±Î_wÛÖ_\x001c_]\x001dïÞ·.úÓhDop\x0013²7l\x0003vÈÔ¤\x000f\x000cÿÚ\x0017\x001fªáí_V\x000f\x001fvÅfxH\x0013®*äÐÄ;</p><p>\x0003ìÈ¦ÇË}¿[ýøüÓïëÈzi»ÝÿåÃó\x001fXÕÍLPTÏ þöÝúîöÓý×ÿøòüø\x001f/n¾¼¼A6c±´\£\x0000\x0003°KµY6\x001a</p><p>\x0003´4ýûøìôõù?þãÝõå¼8y÷âò¤×Îþòâú\x0007¬Ô\x001a\x001d§PÃ7Ù\x0004Ð</p><p>¥Ò[cÃm\x0019)é
Ü^Ãs¦Ú\x001a\x0011ÐÊ­Tê>\x0000pÜã\x0008<Û\x0004pæ\x001d\x001e\x0016\x001cl	¿\x0014\x001cwak\x0002ïZN\x0011ÜJÅ'Å¥¢ÃÃÅ\x0008KÁµKár6çSÇâ\x0016HàÖ\x001dþ¨ \x0005ÿ·Pä.=\x001f@\x001e\x001c.\x0014éÈ\x0015\x001f\x0015ã\x000euTÄíO_¾òlÔºµ\x001bÃ²~þøp?Ù8@ó²cv¸¸\x000b-\x0008!\x001b\x0008:¨To·
½©\x000cì¦³\x001c_¿º8\x0002\x000cï^\x0000ìx±àÂt¼\x0006{\x0002¯I\x0005*\x000byã×ð!¼/\x0004ÓoÀÙÿyÚyÀ:ò®Ð\x001dÎ\x0003ÐìVuö#º:ç\x0004ß\x001c_\x0002ö\x0014Êô¶Ì£4\x0018)M§V%£\x00071SO$\x001eÛë62}û¿¤,oºù#üR|ñ³ÛçÕ«[l¸X½¸Y#íýÃíã\x0014Zu$]\x0005\x001a\x0018\x0010àñtS0>åKtÐZaÜ³ÓëÕ«SlÃX½89FìóÓ1\x0007Wý¸\x0006ÕU\x0004æÔÇ¨Ë\x0000ÿÛõgFkç;0»ÄÃ^p°piìgÀ]iI\x0013ö8{R\x0007J\x0011ðoß .ÚAß=<ºü¡@Ö%²lÐHOÈÞ¥^Kì\x0018t~\x0015
Ä>\x0008²-í	dW"»È\x000e§MuKTÅ}¢N&dÁ\x0017P*q8d_"ûÙR\x0006Ó-=Ç¸
0Íµ\x0003dÏ\x0016\x0010®®=\x0018r(Ãl)Gj\x001b\x0000YQ\x000b «´r\x0008\x001cyÝf Ç\x00129Î²piH>JY§\x001b [Iæ\x001a\x000e>\x00142E=YÉÙbFë´±XûÄlød\x00041b\x001bÏ`®\x0015ó|Í,u@¦£¡f4\x001b©;\x001a#ïô\x000cfU1«ùÇYãøNi`õMÌ:äi/¢\x0019±g0ÙÌ×\x001a\x0002k\x001a;fërfXRwÛA«çDÎ}O@Î\x001e-áîl\x0008Ò$g¾&Å×\x000e\='rî{â1\x000bÑ¥)ñ=\x0001O½çã,\x000f\='rþ{"4yÔ\x0016lÒa6\x0006Ü:\x0008rõÈ¹ï	HÙ\x001e\x0005BÆÒf\x0012²åçD\x001dPgTÏûnîJ&ÙÐ\x0008ôj+\x000fwÿTõ¨¹ïI'f,\x0010Ì`KÃð\x0005Tö`GCUïû84<
ÉÙ.$\x000fÈRjVsê`ªYU¾oé\x000bÉf3\x000eS\x000eô\x0004\x001a~N¤\x0018sUg0WªYÍ7õeÀ\x0008rbG´³Ì,Ç\x0002s´FÞR°Ñ\x001cøË\x0002\x0015íé&Ê|\x0013½Ïèc±æ\x0019Æ¨ÜB_@\x000eæ':UÉ5iã#x±\x001fD%íÁ\x000e·}ò8ÜÅ4\x0010!YÓ*[L&û,Á-¶Lá
·UÈ\x0000è5(~³þðóÃÝTj©ÍQÍà´£®àÝá+É¹0¦þäÉ7Ç/¿½8Ä­Kn½[¦ù-\x0008\x001ePwàTÖàfÄ</p><p>\x0007nKp»\x0004\x001c¬é²\x0012\x0016\x000c¾\x0014¦\x0011Â¨\x000c>\x0012¥ÇíJn·;¡\x001aRôÖºº\x000b»Id\wS\x000e\x0008îKp¿Dà`£j·?Ò.ÉÛ>qqÌÀ\x001dJì°\x0000\x001b\x001bLs9m¶²\x0005Ç¼Ns=\x000fÅ\x001dKî¸[WNâ1í8vBR\x001e\x001e¸ÅXäf\x0016w\x000e+$E(\x0008Ü(z3Aà`\x0014$pÏ/\x001fKºÍ\x0003¯5ø\x0012\x0015MK.%h­¢ÖL\x0010y´E¾/­Ò\x0004®*pµèwÃÖÄi¸\x0015H<p,ÇÓ*àCWºP.P^á|\x000bRâ_\x001fi8³ìíA/§¬t¡\¢\x000c¤µÐ\x0001Õ±£\x0017Ï£6^ §Qw\x0007"WÕ)WKN¹÷©F\x0014$\x001e\x0015«ñ`\x0005ë\x0015ªâ;\x0014xe¨¨%JW4ÁgÅ"\x0017ÚYºÃ2âFÌ#¯,\x0015µÄT	Ø\x0002I÷3Tº\x000fä^;&×<æª:æjÁ1÷Xªd~<U²ÅØèr·/5Þôz.\x0010äå¹\x0019F¢NÍ:h´È4z\x0005OM6ËÝA¬D#ê\x000c$þþ<¯Þ=­?N¬è
\x0017×Jãµ2	Ax5¢Vhú÷»«ãÑ\x001d\x001d\x0005§*9Õ\x001cN0]m:ÒQDÊE[+\x001dq*î6NSr9\x0018J#\x0005JûN\x00004ªº\x0012ÔÍ\x0001ý°CiU\x0002¥Ö7xÀ\x001cq\x000b¦JÑwx-÷"6Wú`Õãâ*\x001alÔQ8.®Ú	<¹ÌÁu	®;ËÙðIIàz{»:¼\x0017p\x001e¸)ÁÍ"\x0007ª\x001fô±3±Às5\x001d\x000b£Íã¶%·ý/$pW»%àèñRÅ¦HñaàVÒò	\x001f{üæqûÛ/âBÇµÞ©\x0016Àµæ*<ì; x(ÁÃ\x0012ðàÓêU\x0004\x0017T\x00171\x000cîÇ\x0012éóÀc	\x001e\x0017sÌÒaC¤¢#n<\x00171\x000fl\x0016xá­ºõiF5u8Ò6óYñReòCªqY¿?\x001e \x0018Ó\x0010\x001e$÷i%\x0011Ö2p¡H#\x0001©yàª\x0002WÿD^=@rÉ\x000bäqå)ir\x001c@FÅ½i0%¶\x0012U Î\x0003¯^ ¹ä	Â~\x0006Iá\x00027ª½·F2¹#~À<òê	KÞ ïs$¤¦di§1ðH>XG^=BrÉ+5ª\}{\x001aÙGð,sevÞÍäÕ+$<C>\x0018vnp® {±9-4Xdõ\x000cÉ%ïP\x0010>\x0010Òj\x0003\x001bi®-ëj\x0016U=CjÉ3\x0014¤JC«\x0011\¦ÆM\x0004§Z\x0018 \x001f+ÓG^=CjÉ3ôÿXäÕ3¤<CAkn{\x0008©H­\x0003×c
æ þª\x001c8µÄ\x000b*p</p><p>-</p><p>fý\x0002¹</p><p>\x001c}0»$ÍàÕû©¼ÁÐød\x0004×in [ªÞ\x0008Â\x0015]Î#¯\x001ePµä\x0001
FSÔ8JæÝ\x0003¸I\x001b3\x0011üÏ§ªOµäùÄº\x001e¡\x0008\¤2W\x001b¹µ\x000bT\x001dÒ£PÕó©<Ý¸\x000b\x0004Ê´Ù\x000cÁ-qwP[KU¯§ZòzÐÍÏKä>Õ\x0003yÌä^\x001dRäºzô¢G\x0008¼8IÁBmø\x0011òGÈõ$Ì#¯\x001e!½ä\x0011"¤y$\x0018=\x001cbñZ«\x001c=<(yõ</p><p>éE¯PôÜ\x0008öâx\x0010È<\x0015´Í#¯ÃK^¡(\x0003ûÑ¥`\x001cþÊ\x0002÷Ôäºzô7(ÂãÉ\x0011qt(RÅÓ¸f$\x001f+iG^½AzÉ\x001b\x0014q&#	Ü§æ\x0008NU±AÊ\x0006u¥Êõ\x0012U\x001eµËz\x0005GÆ%OÈ;>+ò </p><p>]¹\x0013z;´©yÁ\x000b\x001c</p><p>ÎJPù¾¦Råf*w`µQ¯;¦,`;%³\ö¬Ï#¯T¹Y Ê\x001d\x000eþ\x0011$sl\x0003Oà^°È½8äõ4&7\x000b4¹\x0013.¦</p><p>H/@¯Ø¤È£¡$wqgê²\x0019¼Räf"wà¢¥Ñg@n
wÿF¡<ÕrÌ#¯\x0013B\x000bt9îM\x0019!l#â\x0016[Á>üõ´ÊM¥ÉÍ\x0002Mõ&Ôà\x0000ÆUd\x0019|Or'\x0000ü\x001aÑTþYàO`W\x001f\x0019·\x001e7Î¤²j¶\x0003wär¬;q\x001eye\x0005f9Ö~§}\x0008xXr\x0011à\x001ew ÷\x0007=-Õ+d\x0016¼BNFK\x0011\x0016/µ "\x0014ûná9:äa±Õ#d<BÒÑþv\x0000ÇÁd$rÇþÒ\x0007=,¶zìGHjGÕ\x0008@Îu?èkñ1Wñ¯­^!»ä\x0015X`À±[4q%~Ðh­\x001e!»ä\x0011V¦É³\x0008.Ò\x001d§U¢>ì)¯\x001e!»ä\x0011R\x000bA<6Aè$sÜ&É×Ó\x001d2Îo+en(sÜ¶*b&w\x0004NÕ§\x0008~Èëé*Åâ(\x0016-h\x0012»vË£ÉËN³</p><p>%¯®§[r=q©¡Ã\x0012hx\x0017suÐb¬:|fºùÇ÷½óû\x0005y!\x0015¨ÇÑ\x0005«xsqÂ\x001d4å\x001cªjÈÕÂ_æÿ\x000fÝú9NÉYOEfÜ!Ý9©¶øÕB~ãx\x0002\x000exr©ç§.ÅñsqHMcD\x001f\Ò%üØL@\x0013\x001cy\x000e½\x0004\x001f²Sª\x000f¶?®+éÛ¿­äþ=õQ;\?"\x001c¦r,\x0000ëaÿ½k\x0017Ý\gÓÀ_XÔòÿ¬vÄA\x000b¢@ë¬{Zgàÿ\x001fÕ¹\x0018Û/
¶Õnº\x001fn\x001e\x001f>N+»¶p¢IQz°\x0019q]'nç9áv+Êw«\x001fN./^í¬¸¶õ\x0000¥\x000eWÏÃ
¼$Ùé>ÝËnØ2Ù^»C¢
¸¦Ä53qÁ\x0007õä=cÛz</p><p>':ýq·ßßkK\;\x000f7*Ú\x0010\x0010p.ÿ\x0011Ç5ä~lÌE3­+iÝLábV\x0014S\x0001ÓJQÂP³\x001d.ãîÚ\x0006\_âúY¸Ø©KÍK°f}zÑµ,]»[³5à\x00127Ì®±<\x0014N\x0004AgÁñxÈ äØ\x0004­fÚXÒÆÂ\x0005{lUÜ¦GÏu\x0014*«\x0003\x001dM='ÒJ1W´\x0002*\x0003©ÈÍñ°\x0002pÚÇÚyeÅ+g\x0017´§¸k\x0008<W6â¢f:
cÃBy«GMÎ|Õp®³t\x001ebêùÃô°æ\x0008Þíu5ðVÏùN`¥FdÇ\Rù:·áfØ]³Ñ@[é]9SñÂw§~~ µ\bc/7\x001eê4TLÎTeðñC!±*RnLfÍë\x000ft\x001aT¥\x001dÔ<í\x0000¾¥r/8½ôLø\x001cp×zé#\x000cïYÝ`\x000f\Ý¨züøñöîîöæq\x00121Z\x000e\x0014>uÆhê0ÂW2|ÝXýhÑ»w|ùêôììôär\x0002¹*ÉÕ\x0012r´] NrKór<
ÄË±êèºD×3\x001c	+½ÀÇà^rgÆNÊLtS¢ERCÂRÇv\x001d¤ÎãpÏAÉmIn\x0017	ÝÑúe\x0010ºæÀ\x0000¶éðpÑéu3Ñ]î ;[vàì¤Ù\x0003pI9ú\x000b÷XÀLt_¢ûERÇ6¤nÉþðÑþÿÔ½]¹qç»ÚÀ«@fâgø¯jv©Å	6É!§ùÇQ8\x0012_P¤l:ß_Þàux'^É \x000f2qÃ{î=À¹Ï#Û²*©¥Oå\x0001\x0012Dæ7UÏÓÖ+ä$zlÑã!t.ò\x0012ô\x001cE-jkÝ#E¿.\x0001>Zôt\x0008\x000bDpH\x00132:&]ëü§\x001b¢bëå@2Çö©\x0011\x0001ÒÅìEÝ>ÝÌ~½|½;àÐä0j\x0017¦¥Àý
\x000b;©4¿·[ÉÓIön£Â¡j¿/f§¼QÓ\x0001\x000b!¨<»»µÙ»</p><p>v*DÔå\x000eùh5ÅµëijyLÑ-É»}</p><p>6*xPQ|àô²Q­4\x001eå{\x0004ÜÔèØíS<²O)fKKã.\x0018­èáG$ß½\x000bzñPÔ\x000b:0/³\x0017õ
f§èÅÇ°èÆm\x0003°ö£\x0004a+ÍÑ8å°E\x000b/\x0012ç{8$`5\x000fÑÜØ¡£´ç\x0017\x0000XÝ8¸öæ4CûÛÝ?ý?ûFjxtVÃ\x0018b!"yÄ®Bn»\x000cYG`ýøêå»4þCq±ÅÅIÜªKé¡g O×²7]2[×¹QZ×Òº9Z[Æy²¨\x0007\x0010\x0013\x0016\x0017\x00187\x001b\x0019FY}Ëê'YsxBåþd.AÆÕ×\x0016»®\x001eÄ~ÝN.\îÃ-\x000b×%2§ÏäP\x0012ø´ô\x001båí\x0016.L®Ü(o-Ü\x001fÏ#\x000b/TÞ¸%!=Ìk;^;É\x0019®xy\x0001]ô²êemOP\x0018æí¶\x001aLîµä£\x0014(ºXêZË</p><p>2f6õ<y»í\x0006û-\x001b²°:>´Uº\x000eEH(\x0000Ä­zQÜÐáIÜ\x0014ªyÁ\x000e>¦æÀ\x0012p7â\x001doäµ Äò	\x0016E\x0000\x000bWµQ6\x0013£¼©ãMS¼!Ç\x001f|%\x9SÄ#Á©æq[IÕAÜ¦w\x0019J¸9eÞP½/;6/¸&èn\x000bæFË\x0001;ïsÞ!p­^ÑÂ\x000fP"-ÉuÛj¶Þ\x0004YW;S\x001cÚR;3eå \x0015Ù§{/ó(\x0000uQ-å¿ñ3ã;l;Í³3+Xª­øhÖ\x001b\x0014l</p><p>\x0016îÆÆÕä+þA\x0013\x0002¿¿{ñô·L÷õë®R\x001c­C-áüFGd´\x0001ÒlÏ\x0016b®6yÿÕ·o/T(4¶Ð8\x000fÍB¹\x0002Í½øÙÆª\x0019´Ùú8ÁL-3Í3Î,ËÓ\x0005±rÐ\x0010(¹­õ\x000c±mí<1×ÛÉð9À¢G¡ëbq³¤g\x0002Ú·ÐþÀzv|[TZ3?ÈÚ MFºâï c\x000b\x001dç¡y8}¹xP-©Hì</p><p>ióÝv9µÌéÀ\x001eÕÐAZ4xu\x0018ñÐÑn¶ÃC2º(#°¦-íª\x0014®/Ç</p><p>\x001bZo¦!Þp\x001fB·\x000fáÀFÄªÁÄéh(\x000f.\x0004N%YíyºÛpd'\x0006\x001d`­TUåhëSî¦\x0016Ð\x0004tè Ã<´\x0001\x001d1Ñó\x000bÝò \x0018¥@%8³)\x001e:AÝ¹\x000f8à?þ3MÝù\x000fw §þYI»Ø{y0Ï×?M\x0012Ñí\x0002\x000fì¢%\x000f2WY\x001f¬ÍY¶":-À!àí¨ûpé@¼cQ¡&%\x0003Ãqu<½¦Üº\x000bp>b</p><p>\x001e¤WÇ#Ô£\x001cIÕO-mê MPwÎ\x001a\x000f8kS\x0003\x0010\x0002#mè\x0011®kWÒÊCÔ³Æyg\x001d\x0012Ô\x001ch\x000eP¬ë å\x0008ns0Ö\x000cuç÷pÞïåhN\x0004s0 ²¬Ñ£z[îÅÎíá\x0001·ÇÍ \x000fUE[§\x0012§o%d7\x0005¡Æ©©ó{4ï÷|¨­ ¦\x0014ô.Ô¨ë#·³5u~æý^ó5áK
)$}U³·õ¨¿%Î;=\x001f\x001fL\x0016C\x001b[^¥25è\x0010\x0018´½\x001f\x0013ÔÓ£y§\x00178¥+$ôýOï·ä7Û)&¨;§GóNÏ'Òú¥	D¨U¿"oE¸á¢îBT\x000fQ½Ou¶CéÊ<ZVÙ\x0014ñ î\5Í»jªd)$ë\x001a5\x0004!ÜÔ</p><p>\x0019§¶ÝuÑÎ_\x0017}°Ú}h¼dº¢ÞS¨Í¦ì\x0004uçöì¼ÛóÞéØ\x0014Ñ)·\Ç$+ÄÇË)õ!êÎóÙ\x0003/_mu\x0004*Ùòìæ¢I"8ýöÖ\x0010À\x0019ê>G6ïù¼'}\x001dJ1êÝ\x001cT% m*SNP»ÚÍS» CR\x00161Ó¥m­7F\x0013¶ªOg¨;m\x000føk\x001e*\x000fÉ.òìçÅÖêön¨¶³¶\x0007µóRÐî\x00027¿£\x0018Zçú\x001a·Ù=AÝ9k{ÀY;ÇjNËòàE­Ð:¥z³j\x0006º\x000b¬í|`ÍÐbi\x001eâ\x0010\x0005Z_íóQv;h×\x001d0îÀ\x0001Op\x0014KgÌ"\x0014MÔÇåì´oçª]çôÜ\x0001§¯\x00002Æ<ä\x0005neUú$þv!é4\x0005ÊÃQó>7\x000bYê¾ ÀÒf]r!I\x0005\x0005à·Fë×ìy»\x001fgw\x00022Ë\x0012d¯Þ\x0014\x0019@ÏÑÍºÆ.ñ\x0003ãó¿þí)s.åü¼s\x001eó\x0010EP°è?rN5\x001c9?\x000býüç×\x000ft)\x000e||öêò41Æ\x0016\x001a§¡]Hüx[²S\x0019\x0002¡9Ø)d³Ø~\x0006Ú¶Ðv\x001e:z\x0015lÎgz¹¢§üwèK®Û]3Ãì[f?Ï¯`rIO`U¬9ÿª¥¾õÄ8Ã\x001c[æ8¿¢\x000bçFwQQ'ª\x0019¼¥×8\x0001ÝÌ}ámh\x000eP×«\x000cëÁ¢,iÒVa\x0013¶²©3ÔÝ>ùÈÏ¡:#ª\x001c­ÔqK?eº[Ô0¿ª=E\x001déÇó|\x0007k§ªúëF¤:ÃÜ-j8°ª3ÌMd
X\x0011{¡Tµvq«QºÕ©anÖ©66¨ÛË·õ$Æ\x000eUÊsKpo\x0004Û¬gÇ\x001bïaÏþòôëû§o»p­{\x0012Q\x001d~ë/Þ\x0003H_\x0018S¸¨\x0010øîîÙo\x001f~y|xw\x001d\x0016[Xå@OÔ£TØ\x001d0ê\x0000º\x0008Sî¥\x0016&-[\x001f\x0014¹W\x0004N³ÛndXÛ²Ú¿sÃº\x0016ÖMÃZê%SJ\x001e\x0017X]²
Â£°¾õ°(#\x0013#\\x0003S­\x001bL\x0001/I \x000c \x00165L¢Z\x001dj\x0012|T\x0015b@½Få8è\x0010þ\x0000llaãßµ]S¦íZ*ý2\x0005LÍªË\x0015oä\x0008>SßÌä\x001b5ü^¢^«¤3-U¯uyZínØþì<¼¸ðR<CÕÇÉ@ë\x0018/+Â
Ðv\x0017L^ÜX/â\×£N\x0016ê¼Ú\x001bí/èN/<¾þÓlÛ_0yeÛ¦
'ÛÖYÀ.ÞÆ!@wÁü	&½~!;\x0007RO«\x0005é²</p><p>Õ\x0000mwÁä\x0011Fîä¿¬êâ@­÷Ë÷·\x001b­Ûî\x0010ÙSÌóÂ%uÅ©ÿ27</p><p>d ;Ã`ò\x0010#_Ô8ó2\x0008*?\x0005à5ê\x001b\x00052Ðb0{Iñ5L[\x0007Ò®tm6øþ`¶ë\x0005^\x0002Ú*x:¾ÉT+\x0017ëÜJÐY¡\x001cÓ\x001e´nfXõ> i®a/>ûÛ¾\x001c°A¾\x0017	½ÈJó¥F«JèùËöÅ«w¯¯SbKs$,ÝëRnäd.\x000eHÜI-&cò\x0018{\x0012)çå\x0002\x001e±Î]¹P\x001a4éZL7IEP"@B®u+òÅ	®¸Ô}¡\x000c3(£±Bþ7ÂX¦$ýä\x0017'cí¥L-e£4Eë5ï\x0014TRT\x00129-w\x001c³©ùGÓF×\x0003\x001bH0¼k¸\x0002¶<õH Y¸8{q/gï&ÜQö:í";øZ|¤z*s^,¶³óG0å¼\x0011\x0007BuÍæ¬Û#ÝFîy\x0016\x0011Êg7êÝ\x0001tÊ©5\x0017Çìåìö:LlvWGk\x001c6ËKdX\x001a2Ë6¢-õ²}a}X¾QðçÏß>~ø´OàïOòæÁÓ´E\x000f5ÌËG»öâûó«w/¿¼dU`lq\x00128D\x0014%LÏ]æZí¤¤+]Û\x0003ÀÔ\x0002Ó,0«^y¬®uÄÂãËm\x000blg\x0019K-´RUÙVF\x001dÆu-®Å%S\x0007	\x0004S\x000bkÓÉ¾Wâv\x0003û\x0016ØO\x0003Û\x001aN³}eA\x0018{²ðµÚÃÝÀ¡\x0005\x000eÀÞ%í|à\x0015\x001cµìÐ»já[ñÆ7ÎòZàò{u\x0011A</p><p>\x000es,¨\x0006v7Ûq©\x0005NÀèD:\x0019\x0014+\x0007§\x0013±Àm\x0006°£°Ð-_\¿l?.,,×ÀÉ¢\x000cìS\x0012\x001dlæÍ+ìøzèÊl5ÑUÙ\x000c-\x000bð§ÃêÉa\x001cÔcSS{?·Y½'¢YÞ\x0013úòô)ãæHb×ÛAä\x001aE-&Îa£Ãzf'ýéÍÃËÌãëØ2â0c>ÀTÒÕÊE®\x001eR<Õ[Ý\x0000ZH\x001a7d\x000eÅôpÈ7\x001a)RBÔ°Õ=\x0002i[H;ñµA6çñ\x0015 FÐ¬´á\x0002F ]\x000béÆ!½Ñr/Ö©"±d¨Üº\x001a0úÑ3"FÃX\x001d¯uÔÝv	à\x0008dh!Ã!µ$_¬ôm\x0010£N*;Î\x0017[¾8ÎÃtÚ2¥<¡=
\x0007rÇØä\x0000Lya\x001b¥´é4></p><p>E3olwßµqg\x001d¡ìÝø\x001fÏÎ[\x001eØ¹»Ü\x0004\x00136ã~6^'F ;?\x000eã<Sê«Ddmv-î'SÞÀCç#aÂIfÏ¨E ü\x001a²o¬¾¤-±¹\x0011ÊÎIÂ¦Æö\x0014k	!7x\x0008åV[@Cùôåïÿ¶ØùHp\x0001uô:f$ùÜ\x000c&Ùü­þü\x0011CvN\x0012&¼d¾æë%\x0014k	\x0005U5.s²s0á+£½?|i= I§¯ã©cLã)Hê9C{)\x000fÅ J~ë=w\x0000\x0012;w\x0013î<6Oóë\x0016)B}Çõ[ÊO#]0ãÑ¤ÏöÓüä¹©­\x0014­j~r[ïKC[ç4-O6Ï\x001ffÌYk\x0011Eér1§¾\x001b½ÐÍTs2|þxVFÒ(F9j};\x0007ØÇo;kXaµ9xóPYõMÜ¥\x0013ë
\x000cÛ\x0014Ñ¢\x000e{\x001cöòA\x001eÄ#¿2«gR±n`SÈºZ\x00000µ\x0000ºXª\x0010O\x0011ñr¾Á®zZíªqþ§Ié;£¦\x0019£z.cÞ8ñJDÚëüÖã\x000eØ§ÌÙå\x0010\x001eø\x001bå°áÅç_¹çé¯ï?ýz÷ñý×»_þòíË^±qÏó%Q\x0013KÙ-Ä1Õé\x0011ÞW¿pëÓÏ/¹{ñøöîß¾{sQo¼òÛß\x001eåwzE\x000e\x0010U\x0001$é\x0005yi2º1¾oñýQü@r\x000fX^Òe\x0016er¦þ\x0002[½Qó¿@lxø\x0017ðr</¿@"H<×V\x0013[RêÓ¿@½Ç.¿\x0000ßc\x000fþ\x0006V<LÀ¼åú\Í¬nU</p><p>Îÿ\x0002Ý\x000eÃ[>¥f$5[@ª^óo°U5ÿ\x001bt{\x0018\x000eob«£2òo\x0000ÚÎ»]¢û\x001bÿ\x0006Ý6Ãûxò_Àjb¥O­ÚÙª9çïv1\x001cÜÆìòë\x0017±æ:\x000c[)¼a|C~õ Ugo>|úõýÝ³§_ÿòþËO{Sâ¦^­Í2)w\x000ekÓwº4*ùíÃó¿<Þ={øå·o¿¼\x0010)(7¶Üx;»xBìY	$åg¨Þc7\x0005Ù¦À©\x0005§CàpïbM</p><p>9\x0005¯ò»iSèg</p><p>Ü¶àö\x0010¸ãwIm\x0013ññhtFIÚÖ+\x0002w-¸;\x0004\x001ek\x0013ô5»4_{\x001cÜ·àþ\x00088¦{]âI¬\x0012²v,ñKEøãÜ¡å\x000eG¸!`z6¸¯éx´5;»9´b</p><p><¶àñ\x0008¸M2¤´¤täZïí)¥s¡ªl\x001c<µàéàJq²TH\x0005y©Ô\x0004é¦Öû\x000cøé)d9~Ì\x0011rTÌ/\x001a{o¼J¥äóç&þà<rrºÒ\x0003®IiÍ\x0001Ød¯%¥çÈ;\x0008\x001cb¾ôEí;×©\x001c)ÜÔ!BçXàgq®¾æ\x0011Å×l¿4¤yb·y
YêÚð_aµ\x001bøî\x00178Æ\x0017÷½_´R¾·j.9\jfÜOoÖ\x0002*f- r÷ñéN¸öµÚT}x.½7Ít^r["R§Æü»\x0017\x000fwòÃ«à¶\x0005·GÀyL</p><p>I·säg:\x00067±Np[é9pßû#à&i\x0008\x0010bí$5QÇ}&»õ@;\x0007\x001e[ðx\x0008ÜH;ç²Ý2\x001d#-2*\x0002¾0\x001d\x0004__äoÛåkè^bx Ûsü²,n_óæ#µÕ)_?÷ bS¨	µ 'ä\x001bs­¿ªÆu×:Év¢RJ³¨rºsK¼ðdÔÚSºUà4j[T;êXÅYø:|\x0015NÕªWÚ¶w¢º\x0016ÕÍ¡z_Sª\x0001¶©/»nSü}\x000cÕ·¨~\x000e5êQ­*WF8ÍÈ¹Ò>¸3´a' §Úü$¤@U¦OÛÅ¸c¨±Es¨Ve}xûÔãA:f·ùú©EMS¨Øl¯</p><p>UµLÂm\x0016¼\x000f¡¶²
]cÙ\x0010kÔ\x0002\x001e\x0016¡7ZBè5ºÙÈ\x001ccíÏª©ÃÇ¯k§¾	æ\x0019ÕÖ\x0015°9]h\x000cµsU0ç«\x0008«"J{#p¶¾F:¼¢°µó\x00010ç\x0004\x001ctç¢2BZZXÛ¯u\x0011ïeív\x0016Ìm-OZ(Îm;"±Ê·Àµ.ý+¬´JGe*]3Rúõço\x001f¾üißã\x0004ñù/½q\x0008%è
úFG[%°ÍDé×¯Þ½xxóã¥Ôþzø\x0018ác³Ø6/Z'Øù®\&	kv\x0007zmøÚ)èØBÇ\x0003ÐÙI7<CÛ2Y:ÿô½\x0011!Î`7y,\x0019å5Ëí\b\x000f¡ÍÒnÄi¸§K×Èqõû¹±ãÆynn0\x0001á&	¢Æ;¯v«¯\x001b;{ã\x0001{óº©
|I\x0004yÃbÂ¶rãCÜÖ·4ê\É·»\x001f>øºàÿüôå}{ÿëç=µ.×N\x0017\x0013¬Q/\x0018ÜV\ww?¼zþvùE~~xóßß=þòêRþ*Øþ*x_8)Wdç½\x0005</p><p>\x0000ïó?/¿Ç-)à¿</p><p>µ¿</p><p>Ýâ«\x0018~q)¡\x0014\x001fSå~\x0012ª4OØú\x000eþ&®ýMÜ-></p><p>ÅK-Uþ\x0016r)\x000cÆêà·ªþ\x000eþ*¡ýUÂ-~lÎÃ,¿JÀ"?ãc\x0012ülå7&\x0013XÇ\x000f\x0000mjæÇ§oûË]3xMUã'@Í;jqL`ñØ¡Î\x000fï^ÿöùÅÁÁ«]
ÐæfFXñZÏÌ¢õI\x001f¦«TÝvú ¬maí\x001c,\x0000·j·!Ø\x001aðnÕ±Âú\x0016ÖÏÁ©ég_Eèüò½w7llaã$,éS"\x000bAJA\x0008ZÝnyßÝÆ²­twõ\x001d[\x0007©®@ZÞ^»NÃf·Ò~X»Þ`¶\x0013øñó_ÿöáý}\x001f\x001b¹oR4¤ç¼mÑ-©</p><p>ôH×:ÿ|õóëço.Ý\x0014Zhæb\ÑÀüEpCÍµ±íCÌ¶e¶\x0007\x000cmd`tÈÛBulÈX5ôf|5\x0003íZhwÀÐV\x0003\x00115³Æâf[w\x00029´Èá\x0000r[¼Ñ98Tà\x0006ÌÕq\x0003Ð©NG 8Ý«À=it_\x001b\±\x001f¸õq¶\x0015=H]q)0\x0004)tÎ·a_K$¯</p><p>\x0018\x000cPCG
\x0007ì\x000c2@0ä;«\x001c|,&¥Ã]Ô8@Ý¹h8à£)rG©Öô;±µÕ9\x00106~&¨;\x0007\x0007\x001cuRÆ¯¯J"¹%²ïý<r\x0004©C	hA}\x0007U\x0019\x001cò7\Óë#¾£\x0016[ç§J-yMÇÝâ'û©±Ûxd'\x001a;\x0002ßqIU&5?\x0017úµÙ_\x0003Ô]ÜG\x0002\x000f#W`ÈIÇ<S«¯Þ.8 î\x000eq?Åg8ñz1JRöÐÚUxuÎÚ\x0000uwã¼¤>N ¯^O(hóÅs\x0002ºÛ8¿\x0019YÊ×4
(³^-©ß³°Y<\x0013N·ÕT%¤î}F\x0017w¨b41ÝkàT£êÍB\x0011t\\x000f\x000bÁ2,äáãÇ÷EèéË×÷o§½\x0013ÉÑèc¾vËÒvÖTá2³±!\x001f^¼x,zD\x000foÞ>æu\x00074¶Ð8\x000b¯TÅ"XH`a¦uÂ-	Æ\x0019fjiÞÐÁÖ¡_\x001eu\x0016Suh6ôÆ)3\x0003íZh7\x000fÍ"\x0017º:@ï\ü¨SE6.03Ð¡\x000eóÐ@rQ,Ú1êB\x0002Uè
o=\x0003\x001d[èxÀÒ¢¤á×Ébi\x001d´)o7ÁÜèÞÈdYhÌáReö²:\x001a}°\x001b2÷þnÞá±n¥êðHâêª [\x0003¦ü]Óï½x¼§YGÎÚpÆ6"\x000c\x0018Õ-Ô)cwíß¾öÔÏ®\x00134¥\x0010¼·çNkû\x0006ì&®_öâ)É¿\x0014>ûËÓ·¿îX¨êÉÔö\x000b¨mÈÆ]T#^</p><p>FýöáÝÏ;±\x0005ÆYà\x0010ë\x0000>\x0007ÚZ\x0004ÔS§Í$È00µÀ4maË</p><p>+\x0016×¼ÕÂþb=Ö\x0010°kÝ4°	â>aU³\x0000çt\x0007\x0006¼ô2\x0004\x001cZà0
´½/qÓ2bÕPKstS\x000bþi5jù³Ïþ\x0003þ}·Â¨·B`5¹ëu¢¼¥­áZWþìáç\x001cì_g¥æXsÄÊâhÔ\x0003cpRQhÍ{\x0018u-¬å\x0014À\x000b5I 3\x001f²OÛª}\x001bõ-¬÷|\x0006îy_eD\x0003Ùk3DwÂB¿dçÖ,wV\x0007E\x0019\x000cÈo(¨°îJÛÌ5Xtk]xgÚëéR+ð%ÿ-»;ñsìSç\x0015å£ØËAQßZyÊÊåèa)\x0012xóêåËËøN-:\x001dAG®\Ð]\x0000ÇãVªÀÇ§x-h\x001bDw-ºû/\x001eZôð_	\x001d:«Ã!³\x0003g\x001a\x0017t$G</p><p>×Ï\x0016rg¶j \x0006ÉÉ¬\x000bjM[\x0010óúó§_÷íM\x000c\x001c\x0008.eW8ãO}á+L^¿zùËuLl1q\x0002§KÊý#ÿQ£ylÄE/\x0017©ïÃ¤\x0016&0óQ"×iJÚJjt°s¦¼RT²Ò¶vN\x001d»ê¼VðUôvK)m\x0008Ó·~fiÆ*'Â~r!2uDÇµ\x0019gû0c\x0019'¿¹êÞF\x0019ÃÅ\x001f½b^)(ÛÙµ
*a?J#\x001c*­tkHTi/·&]¦\x0005»®Ó³[zýñéå>ñ\x001fÿò¯þøáëÞö¤¤½)y¥:m¤ªâ\x000fo¨¯_<<+7»Ç^<{é)Á®6?3Ó\x0011fP\x001axsÐ:¸:EpcwM0»Ù\x001d`æ\x0011'ÌVrÛÜ¯xu\x0000æ\x0004th¡Ãß94­\x000bV«ãéîÍû¿}ûÃÇ\x000fÿk¯úg8É
ÙÀ,·äÓ\x001e¤««úáîÍãëw?¼xþß/AÒºhµLÆá=Ö\x0012TÛE¡\x0016÷¥­n±YöÐ²ÿbO-|:hx£uð,$ÚÆpÒ6¹î</p><p>Ø\x001bY\x0016*­Gà]\x001d^Ìg¹¬­õ;Ë\x0006»)}·äáøGYó\x000eªé\x001d¦\x0004\u4côÝ¢«þ?~õ²Í£pN­9¼ÉÝûüõýßþ²+×Á³ÏÝBÎ\âÃ
\x0013\x0011d\x0002S¸õ´-m\x0006¾ÉÝ{õöñõo¯ccÇ°Ë\x00150\x0019mRejÉÔmÎ¦\x0016\x000e@'+u=g\x0005ç©\x0010£¶ÖfüË\x001dCcØ¶Å¶óØ¬^PlÍW\x0019\x0010ê\x0014ÔÖf+S0DmÖí'\x0006V/S?¼ÿòë§O;ß\x0002=ëê\x0004ob©ÓEU9S÷ÁÕ·\x001f\x001eßüòæáåeÑõs\x000f¬{\x0006±\x0013T©\x0008¥<&ñ¬Fã\x0017+ûG©mKmç©«\x000525AËÙãP¤XC^:W_\x0002\x0007°]í\x000e`s\x001dt¨°\Y#Ö{Í¦Íb¤\x0019ìÐb\x0003ØM÷\x0007(.\x0017L[\x0007¬Ä\x0018nZìt\x0000¬Ê\x000c|\x0013Á\x0016ÇbÛ£¾`\x001aÄÞ\x001cð$OôSn=	7\x0002,Üþ¢zË(7vÜ8ÍíY\x0014Y4,ø2\x0001ÁçÏ)o±ÁÃEÝQînSÂ]\x0019&¥r4Uf\x001cç¨«ÑmÎ¹Áî6%\x001cÙùt/Öö|¸,§9ªÀê·£îö$\x001cØ<
G\x0016·ÏÇ¤äS}\x001d\x0014i«y\x001b»M\x00076et¶.\x0012¾ª\x0015×í\x0014ÑçXðbær:nçÎûÏëIé,hB%jD\x0008x198ÊÝ%óqÉ"U^J½£¤\x00126ÑCå¾¥¹;_Bó¾Ä\x001bnë,ÔèîKX\x0012êY\x0005n¸¸©s%4ïJñ\x0014"mÄâQ¢\x0015±UZ mÍwKÚ¼wMjÞ{*ª²Ò*âyâ³×¨ª'hvÓ¸ª\x000cË~¬×\x0004ùáéãÿ|ú¶WïÆ [zé\x0004 ¥CK´A¸­\x001eÕF[ã\x0017¿yxwQ[C°]í\x000e`ç\x0008PÛ.r\\x0008®`«rcM½¦)ìÐbyìE¾Dj\x0007]äÄÕ}ª?N[1ì\x000c6tÖ\x0003æ¶Ü¾\dÊ¸®|Xz\x001d×µ\x001da§õe85á¯wþÓûúðþËû}/æÎÖ'è\x001cIU]·|rªµÓÅÐûí]Æùø»ço\x001ew`Û\x0016Û\x001eÀöò)Ú*ñ\x0018Õ¶ñºi{±)¬\x001fúÃJîæí¯OÚ\x0019 jåtâVìÑÔÆà­æ'Ù·¿<üx)\x0005\x0018Ö\x000fþa%i3KK[Á<ÑfÁ%pµùÓÛk[\;Ë\x0003Íe=ÔÇ|]\x000f[iaZ×Òº9Úà|mÆç\x001a²ë\x001ci1lvÍW|Ün\ßâúYÜ$o}!\x001f{ú\x0012£=qÉ°C;g'nhqÃ\x001c®÷(K7qZS,XíWÆ­ëí(n£\x0016z½´!Þt:¨C]¼V'F!\I´\x000f8®aq\x000eü©
ç\x0012ãeÇ\x001e|0zpÄë*DW¨a-	
¾Kü\x000e>Xó4EIéqM¤'5Fð`«àXÏëoìkahð]KÂ pv»Nµ\x00015qu\x0005^k¢Ø
L-0M\x0003G¨\x001aç9rÁd\\x0005Æ+)êÝÀ®\x0005vÓÀ&Vmó|±B\x0015M2*\x0014»9&}
|~Ü3¸ZÀ!þÃê-÷7?ýú´{\B¨CB"<Ãs«²ígk_\x0013óêå/\x000f\x0017\x0007\x000e(8µàô_\x0000ÜÕ#(/Þe<|úã÷ùÆz÷ìÛ¾Ædg9¢Pí~{\x001f¤d/:Õ\x0013·Æ<,Ëäáå³çùÒz÷ìÝ¥îdÅÇ\x0016\x001fâ{_\x001d\x001fwÑjÑ¯Pa\x000cÿübWvjÙé({\x0001YÂª@¾®\x001b¼Öæ4jzÛâÛÃ+ÇViß|»Ò×ÿ ¹ÈKÓYfà]\x000bï\x000eÛþ­±Ú½m\x000f</p><p>o.ÛÁ÷-¾?l{§]Ái³F7ºìapÙ_Å-~¼\x0005¾Zô)/ã«T¢¹|1ß\x000fëÎOXw~¹ú|ÏÕwjë5ÿXÅý`SYåÝ£\x000fëF´:MëÁæ9\x0017£4M\x0005Ì>G²Ø¢ñ\x0017Y\x0007õJòfW÷\XÏñ	©KLB§ #\x0019\x0002\x0019Ða¹T©a«\x0019{\x001aÖ¦bê×O_¿>ýynä
©"\x0005Jñ¨WÏB[O\x001dÜEõðÓH ÖÌÒ\x0003xÝä\x00155]V\x001d:¹
\x001b³n\x00084]CàÜ¾yp¸+s\x001fýiö9lå±×£|®¦à	×ÅhèNï÷Ù\x0013þæéãÇ÷ûêæ\x001dçH4ÿ\x0010¸x§¸\x0014ÔôÃÅØñÍcv¿á\x0016ÚyLÿø§Oúö']æ\x000cúâÃûow?~øUvä\x001fÄÆÞ,¬Ù\x001büöÿô5ÿ·ú|ÍE*RR\x00138°Æ¼+SÀ\x0010Ò2¬÷·¿ÿñí?¼xþøîîÇç¿È¶ûaÛ=Sv~æ	Rþè\x0014S´Âä¶CLù? \x000c1ñ«ær
\!q\x000fIò©TB\x001ebÊNL¾<í0g	\x0002UJ</p><p>\x0018jI</p><p>\x001câ\x0002\x0013\x0018[Q<Á*¯f\x0011Eeª|0A¡ò~I\x000f\x001e¢Ê¿Ö2)|</p><p>\x0007\x000c;\x0016(ÒïÇI£PÙë/Ã¿\x0007 Ø5ÐB\x0005e\x0006S±.¶P¡¥£TyIÁØ²²Æ²ÄBå\x0002¯°Êø\x0004\x000fñ¨­XÙ\x000cÇ6`\x0006(ÝÃÒ\x001ei</p><p>Kõ\x000bÙ\x0006¨²pÌVÈï7©¬+</p><p>\x000cÈT6zµUZ\x001aâÆ©x¼Âéð\x001f4?|þöåÏwâÑ§»ß>}ûõ< OÜ</p><p>·ø\x0008\x000fvù®\x000ch8ÅÑ\x0019_©ôiýðêÝî~¼{|y«íc§"Ú\x0016ÑN!.µ#\x0019ÑYÎÕ\x0017DPDpp\x0014Ñµn\x00181êm\x0011
ºËBÑ{`DHG\x0011}èÇ­ÈïüI\x0010\x0017\x001d½\x00051\x000b#z:\x0018ZÄ0nÅ\x0018J*×bâCbAôe\x0004öbÅ£±%ã!N\x00196¢ç¬ÁBèB%\x000cö(bj\x0011Ó8"³éwFÖþ\\x0010é´\x0014éèwnCÃøÎqQy!ÌüÖ]\x0018£ÌÏÉhüQÆnGÃÄFSnÙ/ª\x001dýÑÕ\x0008ÝjñåÃï{ùÔ~\x0019\x001d» bÑ+c3.ò"G\x0010Kå¢""#fÏêqh\x001b¯3í\x0018\x0001Ôüo7?å;c¾@¾ù¶q(çÿõe*E±,\x0002¸l\x0011«\x0007-µC\x000bÔOù./o¶Z\x0010lAp\x0007\x0008k¨\x0007+ ¨ñåáAL\x0001¡\x0016väø¶(\x0015èÊg\x0002]ì¶Ìj\x001c\x0006±-Ýc\x0011Òëæòi<ÈY¯G\x0000+xÌ¸\x0016Äí±H¬( Ø"!`ý4\x0016g@|\x000bâwZ$ªE"\x000b\x001e\x0015æL\x0006qS&´ aEPDJ</p><p>ú{_\x000c"õé#4ÃZ´ÃGªá ,Ã`\x0016\x0010éÍfà'@ÀtnÄìñ#QÄdÊ§I¤ñ</p><p>è§ñ3k\x0004z¶Ç£y\x001bô>ÛD¯dX/µfH:\x0006{\ZôêïMZúGJôª#3®\x0015ºm\x0003{ö
w2Ë·ÉG\x001cßÉXõñ\x001e¦¾Mì@â\x001e\x0010L¥ªI\x001cÏÁ]|k"[If<t\x001b\x0007öì\x001c\x001e=êÆ±%xuü¡ÝÆÁ]\x001bµa±$ ÄV¡~\x001cù8Ø\x001fÀ»+"XÃ$Ëà´B\x0015dÊ$Ý¹{\x000e>Öµ\x000bòqò\x001fÀNÃvëÃÌÁÝÆÁ]\x001bÇx
ÎM</p><p><Ür!ñ¤G°?E#$ÝÎÁ=;\x0006WÄ¥n%xLu¸eBÝ¥=\x000b'-£ÜL¹\x0017NHHR^ÄÏØº\x0005K{\x0016,\x00179èµ×üX?N \x0019nÁÒ\x0005Ëí^Ã\x0001}\x0018À /\x0003ÙL\x001d9Ô-XÚ³`9TÓä\x000bk\x0010	I\x0000u°ÁÎD&Ô-XÚµ`\x0001208~\x0004\H,hÐ\x0018Ò\x000cí\x0016¬Ýµ`My\x000c+ñX\x000cÔp`fØn¹Ú=ËÕçØ9ê·I¬·Wµ\x001a\x000fDÙÂ¶¿XìY¯\x0019å¾\µ\x0000A.\x0016è£Õ¨1Nù\x0012Û-W»g¹zÊ|@&÷ÞI¬$ÁL@o»åj÷,WÇÃÃ\x0005Äð¼¦\x0012\x000fxÝÁÑÅj°¾\x0006¦SþôôñÃÓÖ
Ç~\x0019¸dq¹à8[\x001dí²\x0018?=¼xþpZ</p><p>ÚAÁ½"r\x0000óÜ\x0008Á°z¿q\x0004a\x0002Ã·\x0018~\x000fF*ãuKúNÞì­	FJ\x0013\x0014±¥{>ÌjâÌRP1\x0013Tc`\x0018Á0m­³üà\x001fÚñFÏ>üü×?\x0014¡Ú3<9F\x0005Nªó3áºe©*á±Tq8}\x001c\x001dòìÕW?ÿ°©HÛa\x000b\x0003`dËÈ×|\x001a¥Î=så¨I\x001f'{Z.\x001aáI¸8bR±Ô d®ìwp+\x000cpe×¯ïa|?,WfÃ£×\x0004Ì5o9ã`MÖ×KÖw/\x0019ØJÆÞp±	\x0006ÕbñÞ\x0018\x0001C³ZúhTóøßÿ­\x0008,~yúÓ?o^Ob\x0019Ï#àÍ%áÞ)È²¦úFy}w÷úÍÃ¿¿N-\x0011î'2\x001aö@\x001aâ¨\x000f\x0013!Í\x0012QKDûÂ½\x0000e¯%<©ærñt\x001cå±-ÝÍ\x0003 w|ñ´(\x0018½S¢³³D®%r{¸ËËu;{)Òw\x0002\x0010oÎCÛg|Kä÷\x00139^Ì(ò¹[4\x001a£8m¢Ø\x0002Åÿó@§¼â²óÍÿA¢|'Y=ëáO9*ø²y§°È«y!òoæK,\x001fë=«Aª.òÅC\x000e\x000e¶</p><p>t[(ÛBÙÝP,"¬:È`j\x000cËõÓL®er\x0003L¨9Pt¬Ò&	jqIÎ\x001c¾»|Ëä÷3·\x0012¡·é¢¦Ài\x001c*¶Pq?\x0014{£RIÂ¢è´Ü@X(¡@Ù4ÿõ _æû×yþjüÑ\x0016*zUt)F¥ïCÝTÔQÑn*\x001e+ï­b^óPVº3^îôx`¡C·ÐaÿJ·ìiòÄm\x0008\x000ce	eUaó\7N\x0015:ª0@\x0005ò.ãXÒ½DåhQ\x000eHtà\x0003vk\x001dö/v\x0016£"+T§ö2\x0015ÕÚ\x0011¤t*uTiÿ²âD,«ì¬|IÛ\x0000ú\x0005áSo\x0006x½ÝTä}i-b[\x0019ÍAc¢ú\x0005O9a*ê\x001aÚ}Ö¸TØ#\x0014CA 2¯=ßÝ«Þn¤Î«Ón·¾HSª.:qëÀ\x0015+*Ú3×ÝTÝR§ÝK¿\x0014Ó\x0012\x001fÊÅTÎX-\x001a\x000fó\x001fÏvKÊî^R.À©G>,®</p><p>¬õB\x0008Í\x0013é8\x0015vT¸ÊóPl/åõÅt\x0017*£ß/$úþ>¼ª©ö/ôeNYU.GzeûAv ºÖ£§rÝ\x0017tû¿ GQ¿ç²+µD@(Od³-óT]´àvG\x000bÎç#°¤Ê\x001cp1QYì$r\x0018<¥\x0003T]´àvG\x000bÎq¶ J6#qäÇTè¥H"oÐ#TÝºrû×ç´"Õ$_ÐkZ*\x0018;ï\x0019\\x0017.¸ÝásàÅ[AþSÉ?\x0003È`\x001d®p9[Ü
ÕËn÷¹ì\x001cy/üýô]\x001aÐ\x0004Òïçç-å»\x001dè÷ï@n(&\x001c\x0008\x0006ò±¬ÅìÑÌ[Êw\x001bÐïß62ws^^Î!ûP«)Å#TýukÿÁÌÓ´#pïM¡2ùÃiÄ\x00184t\x001f0ìÿ\x0016i7¥ÍÅJ1Y¦Bí½	v"É»vÞ·®\x0018õì/Oý\x001b³½~ÿåO_>ü¿[o\x000e!ÜK*è­L>4±HëJÑg¿}øù5\x0013¾~|óãçÿ÷uBl	q0ÊüyNh6LªÉ\x0006ÂuIð8"µ4ji«_	\x0019\x0011Ì)G³îæ\x0018'ô-¡\x001f$ä:½JÈUk\x0005Ðë}Ã~×(1\x000e\x0018ZÀ0\x000cF\x001fñóÂ¯×\x000b¡Õl©Åè\x000e#¦\x00161
#ÚZ,ÄÏ\x00026\x0011kaLó,0\x0008ýn\x001eÝÎù;'ÝÎ.ÛBèµ\x0012\x0002i]á?NØ-D\x0018^Ë\x0014=)Ì+\x0001\x0012ÓÒkJßÕÎ\x0003v\x000b\x0011ÆW¢·ZÆµ>X^a!ÅS±Ïq#Æ12"¸ZÂ\x000eu)æð7h:\x001cöÐí\x0016\x0018ß.<¦\x0004ªËAYÉßÎç2\x001dËÉbÍh\x0016ð\x001aþÔ¥M´ÈB8h;D;H_dm¾µ7erjà^Ëã®ctÃfÌNäKçû~éÃË×}u;\x0014ò,cçvpØí\x0010ÕM</p><p>(\x0017Æìx\x0011\x000f#R·\x001aix5æu§!uÊÎ»ÜÓÈkãxÞßöp\x0018A],F£ÁXàtj¹v'ëäM¼«O\x0007x|ÇP·\x001aix5Ú\x001c$\x001aW\x0018óÂtÒé\x000eõ	\x000fñð\x0019CÝj¤áÕè¬v®.#JRU$ÅsUöaÆî\x001c¤ásÐ\x0019\x0003ÐUÅ\x0000\x001fõAmþéää\x0007ë'ÑßùøþËÍ;\x0015«3Ñ°-ë§ô\x000fy{ö÷óã\x0017o_ºëÅu9]ìk®£QÔ¶.ëò\x001fÉk\x0019\÷ÀMãíg³-\x001ddK\x0012ÜðTû(hÒ;\x0013LJgÓ±ûÙ|Ëæÿ®ì\x0006Ý`Ôpÿ?Áu3Îå\x0007'»¯wo?ûÛeVõùz(\x000fÌ\x001e©
\x000cèµrÑþÚôøöîí«w¯oÍ¢n|ä÷"ESË±YÔöT(RíØdìºdÐ~·-½ÿøq»ç³ö\x0015\x001b§\x0015Ñd¼Ó \x001eÓÙtÕ³Ç\x0017/.æ`ÖZ\x000bö»\x001dy\x0011Ë"ZÅ\x0001¨Æ-2\x0014k\x0004zþur'k±Ü\x0000±ÇNäôÑ4%mÃ$8_Kq
kíöÍÊíÿøùßo*)EMU{J	\}mK¡ï~|õû\x000b</p><p>M\x0015Z Ú
DU ¯sIKêrbS@=Èc[\x001e»ÇÊCg\x001f/k©Ö\x0008:¦*à\x0012ÿÇ÷ÿßÿüôG/&bÃüðáóÝë§/Ìÿå(éPÿ\x000fÜ=ç?-ÊZD¬\x0008Æ;Í\x0011÷»E\x0016³\x0014\©5Íß+¹eI?d7Ï÷ø\x000f?<u÷úáÍ³MOÆ'ÛPüÏÞß=ÿô§o_Í\x000e;/ã»Ìõ·+X,ï\x0017,JKE\x0015c%®È]°xdHõ?^½|¼{þòÇwoÉþ;¯ë»\x000cºp\x0016­Òåÿ\x000b!¯éfe\x001fôzoþýßÚ!\x001b,*·~ä1­uEtÞpÞ³·ÞIàðÚ@Ï\x0013[NâL÷o¥©PúR(`¸«?ÜZJ¡ô®ÔÎåã"oS\x0012ïÙv\x0019épÓµn3`y¶Èül3\x001a±g¾\x0004Â
8}Ëé§ìÊKbæDËi§bÏ ö,.ø fh1Ã9c©â¨ÍqyF1gTst\x000bÎÔr¦\x0019N\x001e8'|¤ÉfO)*Ç0¡÷ISN)I/5g\.Á\x000eJðd"{­\x001bvN	¦¼R2ùlÐhïËvw2^ÎpV\x0014oÀÙ¹%ñKÖH\x000e<\x001bÔÑ}ùî\x000eÕ-Y{ïn;L;eÎ°´3fJÊkå³Ó\x001a\x000bsvÞ\x0013fÜ''¥Ì\x0012rXx[b\x001f% )ÜÀ}Bç>aÆòw·ÅæXº\x0018â\x000f_:U3(Â
ÎMè\x001c(ÌxP\x000b±è°dRâµºZ\x0014:ô·\x0000\x001dh²h\x0010¿d5XrEDÏÔá\x0019??k\x0011ÌÖô¾\x001fck:ÙHNt~Êc\x0006ufê³ËÌpöK¡Lá¤ ¶Ì\x0010:</p><p>ÚH8s"åXÂÏüý#?8\x0014\x00065¨¿Å>Â>J9,\x000båËP</p><p>¾L´Yö\x001aÔ§\x001b¸PìN$:r8çe¦P@ÚÓ\x0002
ñ\x0016öìN$9ø»{98\x0013p^±g©\x00051µ±ý hw$áÔT4¥Ù¬I \x000eÔºänà°;pêHÊ\x001f~y\x0002-g'éVÒÐ®Ï<ÊÙ9zrôèîON
A\x001dHÈäà&;¾óõ8åëÉ®¿üám¬;Þ[9$	s:WOS®>/Ð¥ª*\x001bÔR³,PÝòxD\x0003u®¦\½ÅÒ
\x001a±\x0008µgÐ`åË{wh:_OS¾\x001e\>S^}óTOù\x001b,Qê"3¾Þåà®¸&k Ì\x0000³,t$\x0006\x0015I¯§)_OXRöùÃ=½&ExäÀ
@;\x0017JS.4où(+Tâ.[¾úú\x001b$¨s¡4åB-\x0014	¿ÌÉebº@¶¼\x0017mÕc ¶ÛIvj'9SÆ½dÐ\x001c59¹xæëÚòJy\x0010´[¢vjºx_8ÑX~TZ8SuMÁÞ³[¡vj²\x0015Ë</p><p>EVV¨(_>ÐM¾|·DíÔ\x0012Ë\x000542:8¢=\x001flº\x0001¨ëO7u|²òdùôd¨\x000c@ã\x0004¸îù rm\x0007A»½äfö\x0012w\x001aJ<ByÓû²Fó¡)é\x00169\x001c×m%7³òáx\x001fÅ yû[åL²D£q78æ]·DÝÌ\x0012uù2ïÄ \AAr|êÝ3(Î1Pß-Q?³DöBð9¿ôB, Q?}¾%ßÀ;ùnú©%J¶/¹%*Û¼¯nË¥nñ¤jO/JüG\x0010#Î"é±òøåê#ÈMÒN°ÆÍ&ãå²B+IÈúþ%+¬&uö¸ªï\x00074.\\x0016Û\x0016AÞ\x000fµ,ãíÓO¿Þ½þòáý×_/\x0010f¤ Èeò*ç½7!­¶Ôò|ýöáùË_î^¿yþøvû	»"º\x0016ÑÍ \x001aAôûd\x0004±\x0004÷\x001ep}\x000b@\x000c-b\x0018Et\x001eXæ\x0011óU^\x001c\x0013åPÏ</p><p>¢[G#ß#þñéOO_ý²ZÄ4nÅ$ï\x001e`\x0001Ëò\x0018Jù¨a=ýÃ\x001fºyïÊ'\x0001Ý<ýG\x0018)Êc\x0002Y@\x0019ã:\x00176ÁH\x001d#
3f¿³0ÍùªiäS'qA\x001e\x000e#vû\x0005Æ7\x000c"ì\x0011ã¢üÈÎXÙ0\êz\x0014Ñw~\x00141äËZyä\x0000mVR Ù¶FÜ\x000eu\x0019»=
Ã%ÆË\x0011ðÄ:(_Úi@#ãõÓÖ\x0004c·©a|WçS¥\x0004\x001aàøy¸ì\x0018~9\x0012Æ°~Ç\x001egl\x001e7ø1ÃßÚ\x00051À\x0007'\x0018n\x0016;RZ?
O0v\x0007Ç=\x000f¿
-Ïj~1ZìèJQs¶c\x0002{±?©jÖÇ*f\x000cùÆk\x0015¥.Ðxþøî|#ûÆX4xyJF½äBjÎ\x001f\x001aÖOX\x0013¶C´ãF,¾;À¢\x000eUlhe%~ÿj9\x0001ØyF\x001c÷<¼¬Ä^B\</p><p>Fik×·	ÄÎ1â°c\x000cÙ\x001b(\x001c²Ç.SS³\x0019A.à\x001c\x001cßÐ±cÃJß7\x000f¨Z\x001az\x00163×OíáøZì7\x000e;oñöbG\x001b«c´F÷KXß\x0012Ç\x0019©sÞ4ì¼Y\x001b¿\x0014EBð1h`k£=\x001cîPç»iØwó<m\x00103zÔÌsÊ¿1ÆÃ:ÏHÃGK,áCê|ê .Gs\x0003;va#
¡<î\x0015ÏãXr¸ÄdN¿µ]§&\x0018;×Cã®Õte9ò(rÄH_\x0014;p\x001b\x000f#v»Æwu\x0014ÝÁH$	ß|È$¹ ä;ÿáOm»]mÇwu(Òð\x000e	ä1¹ò¥yÌaÄnWÛñ]\x001d#÷æ\x0015\x0007ÊLqvàê¾Ãa÷m»xÌ\x000eÇc<\x000c	ßIh¹Ab±"ç \x0015ñø¶Ý¶Ã{:òU_Ádù´Y¬håí>;ÉÃûÅv[Ú\x000eoéH¨'u$+ï\x000eùè\x000br</p><p>rRú0c\x0017MØáh"ñëåS£q51DËø`×U¸\x0013ß±Ã~'.&Å.Ý\x0007±cB"ï¼?¼©]·©Ýð¦f0¹®²¤§\³¢ÑcÐÅãÇuGµ\x001b>ª£\x000f¥[#HU\x000ewÖ8uëí8£ï\x0018ý0#«´/ë±d[Ö#iJ4°ööQÆî¦åGoZ6É\x001aY¨±\x0013\x0016¥\x0017Ñä\x001bM8\x001cÝúÎ=úa÷´&:\x0004³)/vÔ6\x0000\x001fâñ\x0008ÜwûÚîkkxDH±c>	ïm9\x0008h¢\x0018\x001fg¿C·\x001cÃèrÌ\x0017\x0016³\x001a1_\x0012¤h\x00004xñDÇÃî1tf\x000cÃfD#ú¼\x001c>É¡ÖâåxÜ=ðOý;ÂÓÄCIg\x001e\x0012ô­cÇCÂ\x000eÊ?ô D¥tR\x0017Æ^)äéM«­V~pêçû!ÿðñý×ËÑíéõÕÛÌS<¸Õ:À\x0004ëd¶B?üðâq«\x0013ºA³-\x001dAãî^[Ðò\\x000f@í6KÜr\x0008ÍµhnÈjÜ°·åT£É\x0004­l´t¶þ|?YhÉÂ\x0010Yv/åFeyåyAóN¿g:[É½\x001f-¶hq\x000c×{ù¤OtôI`Î¶»íGK-Z\x001aZj`$åÀ¹.\x001e9Y8å¼\x0012Ã¹·çÝh`º
jÆÌZÂããâòE½íÐ÷Þu\x000cùdPka<EiÃàû²\x0017«ùxè¶v®é´Ûg5Sæ¬8Ë/\x0000(ÎCHÙjëj­ók0äØ8/a\x001bÐ°ÂóÂ&êDÍâ1¶Î±Ágãì²\x0013øÉV¾©¯ß4í\ØÏæ;6?f7½ýÚ@ËHºb7I°&pÇÎ*èÜ.ù]\x0016¬ÁêÜ¬ú]ðêÜÖÕA¶ÎïÂã
I{'\x0002\x000byÈ\x0011ÌcVëÜ.\x000cù]î~öÀ÷Gñm9îÔ]zè\x001cÅÎíâÛ
Úo;e¬40J\x0010Ö\x0001lsÃ1çæEV1³ÅÈÕ4%þ\x0010íælû~6êØhÌnV¢ùÍ&É'µÕñº³ûÙ:Çc7_¸äÀ</p><p>§G×HN¿©èéO³u\x0017Ç\x001c/?÷Ë\x001eõR\Èj\x0010v¶\x0008r?YçvqÌízÔºÇE34\x0003\x000e²ÚàlÉë~¶ÎíâÛõ¡èëó.
\lTÌfÕ³\x0015ãûÙ:·cn×EíUÌW{Ù\x0008¨\x001b\x00019±|\x0004­ó»8æw}í¦\x000b>ÕP\fàd³ÅuÄ\x0018\x001buÆ\x001c/Oº\x0010³á\x0004%§\x0018­ÚÍ\x001crnÔE¼4v[öúD\x001d\x0008\x000f\x0016Õ\x001c3[w&ÐØÀRåv\x0015m¼\x0017×\x0006êÚÐ-÷ÞÖ\x001d	4v$øz»â
\x00146´ºÚÒÙÎ£ýlÝ@cG\x00135ªl¶|:$µÞüð \x0003¡îH ±#!³I	4ÃËÂ\x0016
ÅÔ9^\x001as¼Vf]jÄT½Û:«>ÈÖy7\x001aón6hG^¤ õ,QJE2Z<f;\x0007bÇ\x001c\x0008÷ÚÙlÒZÎh~R\x0017\x000fó¶Û¦vl:/]b©ÑMZ¸ÈÙ¥\x0016Ö\x0019ÊÐ+É@í,CZ²ä~idIÚÇ°üç¶\x000bK[ý!\x0017\x0006S4h¶E³\x0003hÖ\x0000²\x0016âvêWËw5í\x0008a\x0000Óh¾EóCh,4"}J9"\x0017-\x000fcvÕàf·ç>´Ø¢Å!´|R\x0007b.ô­\x00137E¯ö¥\x0016,
åk\x0004ºÙËªlR\x0007\x0017ãvûá.´6\x000b\x0018,à>¶¤\x0007qmkéÉ\x000e\x0003íì-~?[¿AGvh¶\x0010I6<û\x0012\x0014åØV÷\x0000m\x001aí\x0003Ã\x000e\x000cÇÀ@û\x0017£I÷#\x0018¹T±Ñ¶zàö±QÇF#l<³!h\x0006EÜ\x0005S?h<öA;·\x0006C~
L8íÐÀ/Ó\x000bÊ[ÝûØ\ÇæØ\x0010x\x0014¬¾F+ËÍºÞÖe\x0011l¡c\x000bClÖiuc¤²YÑÍÕïGë|.\x000c9]àxòE£ê¼«^ÖCchØ¹\x000f\x001cr\x001f\x0010Ï¸°%TyA\x001d\x001cÆfs\x000exì<\x0008\x000ey¼æË\HÇó
ù:¿Ø­6¤o÷¦îCë6)mR+c\x0018³Ù\x0000D/ße\x001fóùÉýhÝ\x001eÅ¡=T\x0015\x001c¸«3\x000c¨ßµ\x0002ûØº¸\x0008\x0002#°Úh®ÝT,ÙâµÓüØÿÀ!ÿ<,@w×ÕF¨ªºùöp(hÃÎà\x0003a}\x001bq I^!³ÙB=\x0012ì±OÚm8\x0014·!+\ÀBfåÌÍ4j¶mõ²m£g¸QçÙhÈ³q¢Ck¹ö£äéó§U÷\x0011ÏçÂwu\x001b6(Ë"{'\x0016CéJá¦{ýÛB¾»¾&u6\x0001Â¦Å\x0015¬\x000fm³\x000f|\x001f[·Òhh¥eÏ¦B¼Òª{Õ¶©?·\x000bÍv\x0017\x0004;tAÀ¨F\Ü¨|-Åz\x001e2íö\x001dÚ\x0007Ö\x0005ñ\x001dÛ´Dx(9EÛÖÙÖ\x001dðvè'cXj Íq¡hÙ¢êQu(t\x001d\x001bb³¤qYm"Ñ\x0016k\äã¡MêºàÃ
\x0005\x001fÜ+­ech9ÛF\x0000\x001eðáìCÚ~´îwC\x0007¼MApÞ®¥\x0019Âz\x001bªL\x0007\Ü\x0008\x0017®ëNP7t:0Rù¹h°Y\x0011
òT6é<B;\x0006¥ü \x001bióÏ~ýúôA.5¤òßÅq.kyiG6ø|Â¹ÊÙ÷W/yûðv0´a0Å2ZÃå}ÐRJÏ£\x0006Ùw«n\x00062µi\x001cÒ\x0007É¢\x001a'\x001dæ^%LøÕè0`©É\x000c'áýToÐßÚ¤õ\x0018u\x001dæåy®d:J\x001a§Ì{×\x0008e¾òKq\x0003¬JöøÇn\x0012\x0011Lé)]ôz|\x0018Îç;Ñ[Qñ"Ö²9NÙí\x001b\x0018ß8.È\x001c¦ôúÈc*µ%7C\x001c¦ì6\x000eï\x001cJ/gJþÕ\x0007±È«~ñµüô\x0004%v»\x0007Çw3Q§
?|Ç%ª^ÜáÙféAÊn÷àøî±ÑHºß(¤!¸æ±@\x001a®/g\x0010Òvv\x001c2Ç7¨¾ú\x0010@¨2
Ñ¦µÞ\x000ce·Åq|óÆ(bã\x0017[òÅ°PÞÂÝÙãw>\x0006¥"xÈ·HSå»<]ØóÍ9\x001fÂq?ÄBEE¯a'Qr·ùßN:\x0000á;¯	Ê¦ö$sºø÷S\x001a
»3¥PÄPÅåÏª\x0016
BÆ\x000e2\x000eCòA	&\x0017Í\x0018¬\x00196\x000cg\x001bÆ\x0006!;Nã\x001e¸p²0r¿|©\x0011\x0000¯G8Ú³2,c¶ûÜvüsSM\x0008\x0012·ò3F¾ç\x0005Ó\x0006\x0019±cÄaFQr"¬n"Úxu¨\¤\x001b\x001c:¶;tìø¡Qmq¤î\x0015R_Û\x0010×Zò3Ý¡cÇ\x000f\x001dnº¾RJcqª.xV\x0016a²óçvÜ£ó|ÞèRÖhT5&\x0017N\x001bdì¼¹\x001d÷æ<5S¦q«@iôÆÄC´\x0017HH·ØÞ£´ã2JJ\x001d\x0015µJC\x0003¦ ­È\x0017çÃ§´ã\x00128R ­\x000e4ÁDZH\x0002á\x0006×\x0008×yJ7î)!Ê\x0013\x0000åÿÑ\x0019RóQ\x0010Ïj¼
Bvñ¹\x001bÏyA)þÊWÈÈ\x0017]¦I¥Áãñýí:WéÆ]%\x0011eDòe°öBi¥\x0005(\x0002­+¦nd6k¹-Ú¬W\x001e</p><p>ªÍ\x0003\x0017Óù¦×Ç³\x001dô{a±ÌÌ<}ø\x001c(4Eu?||ÿíý¯*×l>XôK\x0017$åGtñl\x0019ÖÛ»\x001f^<¾{üåRõ°aËCl9(Óº\L\x001dò\x0007º\x001e]Øh¨Ú
G-\x001c
\x001a\x000eµÅë*P\x001f\x001c¦ýÌZód\x0014Î¶pv\x000cË%kÁò1ò¢A§éI\x001bý¢»á\\x000bçÌ%\x0001.µ\x000b«§Z¿>¡GÙ|Ëæ\x0007Ù\x000c×"ªá²é°l¸óE¦»áB\x000b\x0017F
W¬æP«\x0012	xì\x000f®·ØÅ1² Ùå:K é\°Ñ¹-µliø .:Oª³k§A¸¦6Ý¯\x0019´ÜRÀVü¯6´òM¯:à>¾Ýtýá0x:Ø¨å\x0001Àâ\x001b ¶#Ýª~£i7]w<ÀØùDFKÛí´aß\x0004ºó\x0001\x0006\x000f*d\x0011Q«\x00149ÑPßmXè\x000e\x0008\x0018<!,ê7õ\x0018¡«×$\x000f\x001bmL»é:/\x000cn8Ó¬;»d:NçØàÙJ£\x0001ºÎÙÁ¨·«Ùö\x001c\x0012kA\x000fÕ©©6÷÷ÒaçQpÔ£\x0018-_ç[\x0007J\x0005\x0019hHÿcë\x000eûntÏ\x001aq'uødè£ºõ]m\x0014­Û\x00128¸%x\x000cjÕYÅ'è)¦AÏr¤èº-[¢>!ª:I¦3¶ºÙE\x0007ëÉöplÿíîÙçÿú\x000fï¿\>d¤+¹\x0019W/\x0011Içe\x0013xw÷ìÕW?ÿðüñÍu6lÙpMyx'2õ\x000c\x0017\x0014nÅ\x0018¦£Fé¼t',Bb:\x0012EðHñ0Ã\x0010méì O÷FgµÚ­Î@"nXÓ\x0010kéÜ(]¨ÃêC\x0014#~­ÓÀÏÜ\x000fè|Kç\x0007ér(\ä«X©çÄÛÕ'\x001b</p><p>ëQ\x0018Ãx¡Å\x000b£xÚcñ¼hvrÕUãk\x0019Â-^\x001cÃã\x0002P«Ö£êï­Ö;ìTR\x0006ñ\x0000%2¦\x0018Ã=È S·g3J×Ü*Ø\x001dQ¼ ïÃ\x0019\x000ft°»5©î3\x0007í\x0010^Z\x000c\x001e\x0017ÕzÉD­ÖÎ÷3}\x0018>×29×\x001d\x00180xbPÑÙ]¬j]\x000e§Ô)'wôëvG\x0006\x000c\x0019ZÍE,	,BVwn\x0015Î\x0002CxÝ\x0001\x0006±Ônñ,ù£C\x0013-j±YþÎÓæ3¸Urh\x0017ßÃ?½ÿTª	\x0017qÁÿë÷¿\©ÉçïºDÉh×`\x000fIêÍ\x0002p!IËøð»Ç¥ª°è\x000bþþÕËÕ¸</p><p>
xNð\x0014¨\x0011õ~´E ®Ê%7ä[\x0007Ü\x0002Ô¶ v</p><p>Tg \x000fM}Ô\x001a¤`×o ®\x0005u3 ±:\x001e9-±$Ãl\x0002øUMõ$¨oAý\x0014h©³ÈÊ\x001eF?½è(\x0005ëoòåcË\x0019§8¡r²6\x0018\x0014`Fs\x0013{¦3MqÊd\x001csfì\x0011Eá6@·X Ðû¦)çÄ\x000f×BÊhVIË=9 ¬Dd'I±#Å\x0019Ò\x0000"Y)\x001fJ*w\x000bÒJ\x0017\x001c®«¤\x001b)?ÃÝR«Þ¨D=NlJî&¤\x001f)Gêw¸Å¦6ÂºEÑà\x0008ßÕ\x0018Ov~\x0014¦\x001ci>l±(ö\x0013ºfÈÞõ&û)t a</p><p>T^ßÑ[s¯nT^'\x0002®A&9;?</p><p>SuëËÉ\x0012è$_Húå£½	hçHaÊ&'i\x0001\FÃÉf²¨)ÞÂ?açIq.ÌóêI}pz\x0007G«ë2ÙIÐÎ=á\\x0017¥³\x0000Yª\x0016d3Yy±
´ÎÇOv»\x001eçv}ÔÓ>Ô\x0002i&ÃëÄnAÚO8\x0015?QÚ}ÊÚ¯¬9Áû4ñ$i·ñqjãs×wI\x0002\x0002\x000fþ\x0014ù\x0003/ ÁÐ-öS+-Kyï8(_7IÁåèT´\x0010äy<°æÐ-@»À¦\x0002\x001342p ä­%\x0016µz¿ËÉ-¾=õ÷»¹ÀÄÈá\x0014)jÏ.¢tx\x0006î\x0000½\x0005h\x0017ÐT\\x0002^$}@Ñ\x0010Î&\ÈËô&¤¢)\x0017å­4 2Ëã&êdÚ`¿EdB¢)\x0017\x0005zu"x²Ñ;I79I©sQ4å¢¸:¬|}~rJªñs¾äÝäëwÁ	M\x0005'Îkp0Õ1!ºó9=q\x0003PÛ9S;åLJ8\x0013ºÚÕ</p><p>Ô¤x+íÂ(;\x0013FqÏh\x0019@\'N*/	¹âÇhnbÓÎïÛ)¿o±ºMã\x0014E2D{\x0018Úv~ßÎø}fãÅ¦¾V7\x0002H\x0019\Hpýd;\x001fe§|\x00147eJe¶,S5é-\x000eRÛy(;ç¡¢f§\x0004\{S<\D27Ùø®Ûøn."}U%NFZ
£$±·\x0014\x001f!õf%÷³äÏÿú·§¯_KÉÁ³§\x000f_.ZzÖô+\x0013óXCAFµ8b\x000caÕSúüç×\x000foß¢g\x000fÏß\Ô¶\x0014Bl	q0 J©\x000bxJèóùT\x0010×Ê\3Ô\x0012Ò°
mÀ>ÇIIÛ]\x001d\x0003){\x0018Ñ¶v\x0018W`Çê×V3\x0017dÛx´+©Ü\x0019Dß"úqÄ¨³òò9!¦:~~U\x0008>eÅ®â±$ÿ`ó
bLFï\x001a3®Þü§6Í\x0014'Hs°^:Îò=\x000eu\x001c¦×\x0010ÙÓÚY\x000e¦uÕN*U;Ú<ñ»\x000f\x001fßzºçâR'\x00061ËÃ\x0007Æ²`6Úe~÷üÅãËëd¶%³cdÜÀSæ±ò3v©eQa['éÙbË\x0016ÇØ²µJ;\x001f{¨³¹ÅYÜ
\x001e4\S¤*a?
¾Ìi\x0000Ê÷ÇR2ÁÝàuÛºJ|\x0014®[o0¶àlÁxjB\x001dùãF\x0019³\x000bñìpÁ\x0001ºnÍÁØ¢³ÜmR¶«
FØ¹ÙD= \x001dT¼\x000eh\x0015+\x0000µ=D?¿ÿúôéÏ\x0017}IþNïAËÝûMäÁß\x0015d}{÷óãÛ?]t%-\x001e\x000eâIrÊQ¡<KkÒ"£ÕS\x001cA£\x0016F-GZèB\x0015ðä\x001avUHØ\x0018^²\x001fÏ¶xvÔrFdô)ùS5j=\x001eÒt\x000cÏµxnÔz5{\x0012Ö:\x001dÔ6Z\x001eçp\x0010Ï·x~\x0014/\x000eOöwcéòq£Öé\x001aûýx¡Å\x000b£xÇFùEC$i>ÏÖ\x000e6ÒQ¼ØâÅQ¼Së$+Í\x0005±W§ò®Ö0^jñÒ \x001eªÀbAÕïìI</p><p>ê¼ý\x0000^[\x0001H]_Ñ^\x001cU\x0012(©À>\x0017ÇªÍAëAb\x001e\x0019XKúxÌ\x0003UIë gîÈÑ3¬NàÆ]é|âÊ@ý¼\x001bOûùºs\x0003F\x000f\x000eÓÝÁ57QJ\x0014«^_+>
óu\x0007\x0007\x001cT'_åXÂ)«Ê «ÂÑu\x0019F=3&\x001d\x000cj¢Ikës~\x001dÄïçóëÃS;â?þå_\x001fÍ¢=Ê_´LýY\x001añ]	ã!é±\x000b~­Y"zw¿d¼ëp¡\x000bcp¬C</p><p>%Øs1éàztúmál¯ç~¶Ø²ÅAÃEä¯²^ûùµJµ\x0001ìAÃ¥\x0016.
Â¥öF\x0005Ñ	AõRáì\x0004¬ÝlÍqá©\x001b±ÏrI\x0015I\x001cÇ*òUM¨_õå\x001aoì©E±Ït^_ò«ãrQ\x001fÈyvÒùÉ'{é¨££Á\x001d\x0001ª·H.ßº\Î4]\x0011¿«%\x001eÞ®}Âg¥ÎZ\x0014C\x0016\x0004.*Y\x0016\x001f\x000bhXù¾Ú¢\x0005[\x0002®2B\ß\x001f#ß\x001f_|úã{wýùéÃ\x000f\x00173â>{aÑ9p)Ò6FÝ\x001bÁ¬&þ½~ñðìQ4^~xþæù¥t¸ bÃ¡êUb¾ªÉ\x001b</p><p>\x0003\x0006rx\x0018ZD\x001aFô5háæ#)"Z\x0004\x0015</p><p>¢]Eô3¶E´Vt-¢\x001bG¬£H0ÕÑT1ø:¹¯Eß"ú¿K+\x00161ïhRÉfLNÛc<YÑÑaÄØ"Æ¿K+¦\x00161
#òT\x0017µb>ø</p><p>aº¡]<¼\x0014¡s0î\x0017sXS.r¬x ×ôTû#À*E4hÖÉIÓ%'øüíË×Ë¡¾áÐ¡\x001c|6^D ^4óMbCDèÕ»7o/Ïç[§&MÜ\x0005GÒ6wRfI#ÿ=\x001b"\x000c{ÙlËfÇØU50nrGÊÄ\x001asùµ¼ã(káÜ0tMóTóóJ³gç\x000cÀù\x0016Î\x000fÂÑ½Ò>ÉíÙ46G
\x0017Z¶0ÆV\x0004+\x00168²÷¨\x0013\x0004.¹MM­½p©KcpVëß;t¤UßÔ4Ì?×U;\x0000\x0007½#\x0019ô$4ÛìYñKFV*0tÔÑÑ \x001di¿´gm\x0012ûª[
a#á·®ó%0èLXªG\x0005/k¦Þ8LxNH`®s&0èM@\x0003ES:n\x000cÔËQ:;\x0010l®ó&0èN\x0008µLÐG¬¾N[Uã¦\x0016Î^¸ÎÀ ?ÉIiEöÉhYhþ©lÙ|Î\x001eó'm[
õJ=ûÜÌ\x0003ÖVªÓ²ÃMí¯½t·AwgT¥o©d\x0012Mïô}\x0008í¢ËN¸FF#\x00133¸êªàx`Áqù°Vç\áºÚ{®\x0006\x0003'8.:\x001d³iª\x0010¦-¾½tÝ¦À¡MAÉYyY[fËËw¥¤ò\x0001[¹ùÝpÝªÃ¡UÝÓ¸.\x0006[F#QÒ.ØHaãÕo/\x001cug,
±Ä
è%\x000f¤ùl:ÕLù.\x000f4L×­:\x001a\u9>\x0011I7â\x0005(ó´½</p><p>pv¸ënc@\x0012®\x0005\x0010úAß/>üáý_¯Ìnò:U+
m9ÿ½Õè$¦µxôâù\x000fo~¹¨3»®çÂ</p><p>Ó^@þQÞ
x$\x0016bxoN[Cv\x0003R\x000bH£\x0016äé®2ý*G¤¹P¾n2S¦v\x0003Ú\x0016Ð\x0002fOçe\x0018\x000f\\x0011¹\x0000	§õU{\x0002Ðµn\x0014ÐE\x001dÂiCb\x0017HË´:é\x0008	7\x001fï\x0006ô- \x001fþÄ¶\x000b^¯f\x001eô#ÁÙcc\x00080´a\x0014\x001ed8\x001c·O¯úisjînÀÔ\x0002¦Q@ðª\x001béêèÜì¬åhKî\Ù\x0010\x001fônpÔ\x000f.\x0013ÁañmÉÞÖyM)¸£K\x0010:7\x0008£~Ðæs
N\x0006ò+à
,Øy\x0019\x0018v3&éèUU¾Ç©æk:_6\x0004Øy\x0019\x0018u3\&º¯îÒãÿY\x0008Söb[\x0013¹w\x0013vn\x0006Fý\x000c¿¦JõCÞÈ;sõ55Å³ñ!ÂÎÏÀ¨£!"2aYEßJhp!u\x0017÷\x0004aì\x0008ã(¡Oªaî\6gùÈzýHi=io¯UYæz´oEòÃ©èU\x001fÛò*<¼O°\x000f¸F=
läèOe¹Q\x0000á¬\x0008ü\x0010`çipÔÓ°J]¹cæEhªP\x00188ÝÈçóßCÝFÆÑÌëej±(Oû|Æx!Ü\x001e+¾°Û&8ºM0Ô­<2Ô¿ÏÉøsò¦CÔm\x0014\x001aÝ(,q./Þ\x0005_!d¾ï\x0018çë¶	n\x00134^µU\x0018Ô`ç¨ú°³¦î\x001bÓè7lÁRÃn\x0003y°\x0007)sNpü¸s]I9Û\x0012ÅÜË# GJ4ê\x0010íF\x0019Ì\x001eN¿Öýó¸îhüùó·¯_?ºxwù</p><p>¥7ø|\x0002JÙipK
ëéímÛÓÏ¯Þ½}ûêåÅâ?\]3&N`\x0006ªå0\x001cá\x000f\x001e¬6T°±oI-&cú\x001c)Ê8\Ê\x0014%½\x0000Ô\x0017Z\x0007÷cÚ\x0016ÓÎX3Ê\x0013ðR\x0016\x0013|ôénñÍ]Ké&cm©&pª*\x001fõ0!Ø[`ú\x0016ÓÏì \x0002Xªcä\x0015,xÍ¼~W\x001d3\x0019ZÌ0aM»Ñ[¬y¾Ï\x001a­í\x0008)Þ\x00003¶qÂÉFôR%#=\x0004í"\x0008nU7ÙâR\x001a:¾Óm-B\x0011\x0011ð\x0010O\x0017zE÷CvN\x0013&¼¦\x0007-°å*\x0000\x0010ôNÝ\x0011Ü`iBç`Â\x001f-¯Ç²ÓMTÅ÷àív×ú~ÊnÃÄF÷§°B\x0019µR Î</p><p>~5ùz³ÛA0±r¤ËÉäâ7A±6íëÝØm Ù@\x0005\x0004Tn\x0011¨\x0017H¸;Â>îÙB¸«pFmY¾\x001eá\x0006î\x0008»\x001d3;(\x0018)ÅXÄÁ³6\x0006£Eg!Þ`§c·pf\x000fåËL°ãSHÊ\x001eb \x0019Öº9sÝ\x001eÂ=\x0014ë{nÌ"-ÖTÁó\x0010q[¦b\x0007gp«°8;vu~»{ýôå\x0017\x0008ù¦{\x0004í\x0017Ë¬PÇlI@¼»{ýðæÙu8jáh\x0010.ê®áÉ1¢òúìá7wÍ^6×²¹16Öíi{)é´ëÚ\x0006èÛ8mö²ùÍ\x000f±Q\x000c÷úM\x001d×¸PéIP»Å´q}ØË\x0016Z¶0ÆfÞ¹ËÒ¤ÈjfÍ¤ÕU6ÿ'u¯\x001co?ûòG\x0015\x0013zøôç«\x0019*\x0019_­ÈûåÖ\x001d$è	)CÉ·î·¯Þ½y¦BÜÖv\x001dÚ¶Ðv\x001aÃ³(å`êô±üÅ¥ÐÏ­Ç¢\x001eö-´?\x0000MZÿçrl¤¢u\x0018\x001f·Þ' c\x000b\x001dç¡sH$:ÝËØÈZ7ÛVrk\x001c\x001aú5}dQ;\x001d_b½ãº²¨uyÀ
G«VÏy¦NªåÀý}e<íï;7ïg:j:`j¯%è\ÿ :Ôõ¸îv"\x001cØ9HRuH§
uRõF/å\x0014uè¨Ã\x0001S[I\x0011+mY\x0019iTûMÌ-×Gê Ó¡õ\x0001â@ð4N°°,*t3jìV5Î¯jNî`eþÇ½Ì¶ÕÒñì ÁQhp«\x001c\'s=òv<ôU*T=?\x001a/¤\x001c\x000fÕÚÞFùëA7¬nprÎ{\x0001«ùx\x0011ö1ª\x0012æ´-ó(mÙì 
ÒÃO)Ç\x0010eúk^¢ZgÏkàù\x0016Ï\x000fâ\x001d&V¡U<®Ý,x¸Ñ\x0005²\x001f/´xa\x0010\x000f+ÀU´K\x001cÔHÆÒÙ7Ã\x0011¶Ø²ÅQ¶¨=*\¬Z</p><p>ñ2^ÕÍ9ëÜGèRKÆèbÒÙ´\x0002ÈlZûS:¿1±y7^+üâzá]|QÆ«g>F\x0010\x0007\x001e«¤ÔÙÊ\x0011>×ñ¹A¾\x001cJ¾ÎÔØ?ûAm¶°éÜ`¿!¾nßÂàÆåI"wR`Ö¯vóç_`CTj7_·qapçFÖä\x0012å\x001c4zb,yN\x0011öñ\x0007ù°[8ºþ,jW­á¾ÁXøæ·\x001dl\x000cªÝÏ×\x001d¸8vâÚh\x001aûEÉ:8SuÀ\x001e<Õ°?q\x0007ÜHª¶ÌÍ[)v,\x0007­|çû
ñu§.\x000e\x001e»#W\x0011\x001e"Mi:cOö;\x001a\x0015`ç^pÐ½`´ÌÜD¯ÂMy'«ýüèÚn¾Î½à {	Ñh/÷Êê\x0003£²\nK\x0019i7^ç]pÐ»pÂå¢oå1:¹\x000fF³1µ~?_wøâàéËÝ\x001c1÷ò>áôºÊ:5ñ6Z0</p><p>\x001bu\x0006=_ðN¦Z:X0%3åÁoKç£AÏç¹¢²ð~X/l\x000e~Vê¼\x001e
z½¿e,uvRg¢FËÞltþîçë¼\x001e
z½/\x001brhäH#çÏkHêélóÊ\x0008_çõhÐëyWßí,v&E«_w«©k?^çôhÔéY.Qo\x0019Z\x001a¼v®lî¦ë®\x001b4xß\x0008ùj´n h}C\x0002¨u\x0003G#>ê|\x001eú<©XËg¯\7lÔ:\x00016Ûù<;èóxXV-a\x0015\x0011M\x001c\x0004ÉËá¼Æ~¾Î±ØAÇÂMÉe\x0001K_ªLgLZU\x0015Í¹)çC|ÔñÑ\x0018ó:ùõÔ±Z½òæ8È×'Y\x0006\x001d\x001f¿\x000cËÖÈx ïÂzÚ±¨í¼\x001dôzÜ[!NÏU- ­ç1mhì§ë\x001dtz>_$¥u	e\x0014M¬>q=b¯s{vÐíù êÉ¬&Pk=n]Ö8=Æç:×âF]K^påÌ°<¦YJf<j¿h +¡ÞU¼Î³¸QÏâ<^³8{\x0012\x0014§Á^LG3·º¢ìrp²÷\x0016\x0018Bíº
Výsð±v<\x001eÝÂä¿ÃôÃ1/À ¥\x0000ªooPË\x0014®À[a½]gèmÿÖþúó×+Ýp\x0018tLSAò¸Ö9
\x000e6\x0006ø)áõ«·\x0017kÚ\x0005\x000e[8\x001c\x0003=Ý(ðé!Í:(:bØz\x0006ÛÉf[6;ÆæÊDnt\x0014¶¤5Z´® \x0018ó-\x001f u·\x0014î\x0006WeÊbãù<ÇÈbK\x0016È\x001c?\x0008	Y0:½Î[Õ\x0008g/jûÙ [n0¶Þóª"\x001aOÒV\x0001T_Âf×`¡»¸M¡[m0¸Ü|P\x0001Û^ÒzKÝr![wL\x000cÛ­[m0¶Ü|Ò:ÀåÍ Ô(Yßª¶ß«÷Ñµ)[»êe¼J·¤ÌH2ò\x001aäe·VâÏêZ
À¹\x000eÎ.\x0007 Q(ð~PeØúÌç7\x000bXvÒ.Î,Eû^F<Hý~\x0002}¿=¯/4\x0000:¸4\x0006t/ÏhÉ²»[ØxÎ½<dlvÞí£îX¥±s3*RrjLí¬L^k|l:;e::\x001aÜ\x0012b:o²R\x000fëóP¶ÄY¹²=pÞ¯\x000e}ïùÐö÷ýði~óôOO_þtY&E\x000eÊà»|Á¾¥81yéÑ÷Î¬æ<=ûíãÏÏ_.!Óo\x001e~÷ðæÇUÅ\x0005ZD\x001aFÌ\x0017Û\x0014\x0004±ÖÄ&ÌÛ´JªÌ Ú\x0016ÑÎX±Hæ\x0000v"È´u­x\x001cÑ·~\x0018Ñ¸f\x0008<á¦Èv' *#®ò3¡E\x000c£3@B¨¢49¨Òqïõ(al	ã°\x0011!ÕïôÅ¨"\x001eÿÎ©ELÃFÌWÈ\x0012Bá^!aåKùÚ\x00160¿Ô\x0014~e+á\x0015ÄZ»ÆY\x0011W-`3Oa§\x0018y^i½\x0018ÔãDt%¢;à\x0014_Ý$¯7ÉëÕäÙ3«t\x0013(r\x001bù¡òöö8×õ*÷õY\x0012|½@^g</p><p>\x0016êS\x001fD	JÉ{\x0015)ÉnûÌ	¼\x0017Z(Úo¨rû_\x000cå½º\x0013[oÃ¹Ù^&×2¹ýL\x000eT\x0010\x0007k}\x000e£4ÑèÓ¹\x0001Ú¸ñµë
¾p]'b]aª½	QFPÖ¡vç"§½6J-QÚOÄU= HN¦Yscv/Ã¹7PÐïºýÛn\x0016+ryµËT|Ðþ+Àí/wª[â°Ûr\x0008-TDòÆaU :«¾Û	©p¿©o~\x0002åtà\x0015\x0001XÝxx.äÝKÕ­*Ü¿¬ {yígÑ§Å\x001b`ª\x0000ÑL¹\x0003\x0008ë¬`è³×Uïm´ueQ\%\x0014A}ÂÖíåº,X§ÞBz»NçX«Fvcþ£\x0014mûPÓãÙ\x001a±\x0011<×â¹A<\x0016¨r®)×\x001båõÉl)ìÅó-\x001fÄ#/)ßl½*\x0008ã;Yï ]héÂ ]4uÈK>D\x000528M9ø¸Þ\x0017[¼8\x000fK\x000fÕx!tµ§oSås/]jéÒ¨ñ´±h1\x001e©ñ4awpåAïU\x0006Ý</p><p>Ë`¹§â\x001aAó«þ¼Lú\x0008\x001evx8\x0017ë! ç©:$9ú³¥»
ÞVþ7¬\x000eTf£A6@\x0015\x001fE4ÜµØ.ia¢G·-t>\x000f\x0006G¬R\x001fO\x0012Ôù2\x0015*ßÁ#\x0003:·\x0002~Ås5ç	Oò¬¨Ï5\x0019ozéõü-\x0013ÛNÇ?~þxYxkÂ\x000cq1IûEA_1Còë¹æò>øøìÕËªÐë¡V&¶(;Ð¸OXÚo3^\x000bY\x0008JvöÂ2@æZ27DküÒn\x0016õ%	-f¤¡Þæ[4?f4½-¥$sê-D\x000fbµ³W\x0001´Ø¢Å!´¢M½ ÙÚ¤\x0007É(Z>\x000f¡¥\x0016- !ú¶Wv\x0001Æ+½¼»Ñ\x001cQFkûNöÍi§X\x000e\x0001tÒ\x0002$M&³\x001d»ûÑ C1³\x0019ÖXÌfk0#uí`Ü\x0018Ô¼\x0017­sk0æ×xô±ö9×æ}Ô9¯lÁ\x00114êÐhÈj\x0014tZ)ìÊó=\x0019Ò\x0016[³1\x0000y/[çraÌçz\x0011Óá\x00078=ée\x001a¥=ü¬ â~´ÎçÂÓåä=\x001akã)èó=ÀFsÎ^´Ð¡!´¼/¥±É%Î\x001f-hú\x0004
tV'b?YçraÌç\x0006¯ó2rÄ¡ØÏ2è\x000f\x001dïÐù\\x0018sº>JQ?±\x0002¬ä|Å\x0016»ÙÒ¤lØy6\x001cól9\x001c÷Ò<ÌZçÒPîµ8\x0018¼;_Üµ­ó\x001f8æ?ø¹ª&qq:ÉN\x0008*\x0003áìMk?[ç?pÌ¤\x001aNr¹*¾Z_\x001bñ7ºHö²u\x000e\x0004\x001c\x0008\x0019«Q\x001b÷kxYoIÍýßÅ.jÃ¡°
êÅlhï½øÝP\x0003J¿ÑD²\x0017­sn8äÜ8})å?></p>
  
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

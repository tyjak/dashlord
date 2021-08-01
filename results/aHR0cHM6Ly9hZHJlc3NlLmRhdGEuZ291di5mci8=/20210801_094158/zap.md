
# ZAP Scanning Report

Generated on Sun, 1 Aug 2021 09:33:33


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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#pKhQL1`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#pKhQL1</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Üg'ú¾'ÁÙÚþ¼z1ðákjûó=ZåüöæúòâæE¼Á"¼Ö§kãi²å¹qO¬\x0005fNH7êtBtm§	xºs¥±6\è¬d(¯÷ù\x0007¦òÅ/v/Ú\x0007ß\x001a%]2ÄG°çÆ\x0007Cn9áAZ>\x0001Ï#\x001e\x001e\x0019Ä+\x00054)jI;r¹áç\x0002¾Ð
\x0008Ã«\x001aé¢ÑU%e\x0010W]òÈõ»Ó\x001a'òyßl?ï;·2DÛZ(\x001dÏE]·]$?\x001fZ¾ÐÉçÈN\x0001®óÑÜó!y-ýC½Ý]÷6o\}\\x0007t\x0002F¼*\x0002_¯J¼=PÇhv\x0003á£|÷{cú\x0002m\x0016YäÖhù¿¨fHbÙhsEÈ}&¿}ºût÷tÿñäõý¯OëÏ\x0007¬*í\x0014ìËã\x0015bé\x0003l\x0012OsG5í6C3ßÞ\|sqsy~òúòí»ÕÕËfÌhú\x0019M)öåq3<ÃòqÓ@èFF0CxL©­øLÆ
Ôw)dm;!­êÔµÛA,ÿU[3]&CB²%òQÇ\x000bã\x000fe\x0004ýê·;üï\?~}º;ùfýó\x0001+PgVG\x0002J¬\x0006¼Ydêi|D«\x001f.®\x0011òúÍ»\x001b4½V¯\x000fdÿ2^
y\x0014<²{{ð¼I<9JÛÈýIè¶©=íÈn¼¡ïnÆË}w{ð¨Å\x0017Ô¡\ÊÊols»álÍÝËpôµ\x000b.\x0013\x0001ÿc6ôó4)Nã\x000f~\x0019_+<Û-¼X\/\x001cq+#ÑäµÕ¤øÚ½g{÷\x001e%\x0012&>\x001b6¯3Ýx*Èò:X$>jó7Â£¯}xÑUßU<?L\x0012JðBm5ñèk\x000f^TAfÓæ÷\x0008°îS/6i&3øRËúøÈc/â£¡ÀºYæM´ËäWç-\x0014>
âuñQ\x00170\x0007¥ÄfTÞt»Bû3øbË\x0017;ù\x0000jêA´¼ýðþ\x001d2\x000f\x0016]\x001c¡\x001aü\x0005\x000cþ.<£ØÇfu¨óÞj_\x0015ãé¾à¡ÅëÓÍ'ãéQzN&úá¨\x0003ó~¾Ðò^>TÈ sÊ î¾êîÓËNo´
\x001f~íã¥\x0007RV~Q:¶ÛÚ&ÛXKøR»ýRïöC\x00129\x0017íbL)3¾ñ\x0000vóEÝhgúÚÇç\x001dG~³ö\x0003æ£©¬ýô¢ãK\x001beÄG_»ø±ÒÝG[+ëëk\x00133Jø_À7ê\x0014ùJ§°.@2^\x0018F§0`Þ½Æù%©VuT\x0014\x0003RJa\x0017`JR\x0011¡S	wå9y®Î%+¬½oî·ü½\x00070QB¼\À\x0014Ý/ñ\x0005§\x0005\x0010B\rÁé¡$\x0003¦>	&7\x001cßÀä\x0012ä\x0000­C?L;m«\x001bpã\x000eÑ½HÊ'Cr\x0014¹\x0006\x0006õX\x0019WæÕ¢%\x001eÂ\x0002Ø§eâ1¡ù\x0014;\x0019K"agxÉ%2jíÀ|±S
m,#íLSnÄF+ìëØZ\x0003Kna½qËéÞk.\x0003rí\x0015\x0001È©ò-ÚQ·g8Ï\x0011îÚì\x0012T»±PzN=ÀnÑùVµp¶ï\x000eNøK}¨ÀÓò´\x001fM\ôC»m\x0003Ðu\x0002R~\x0013\x001bY\x0000ÃuúyÙ\x001dTã\x001aÊßûøÄ´À¬¡}jY°C\x00086\x0000ûÞp¦±³ûEY~bê þ\x0017pË6`jý\x0007ù{\x001f\x001e
MÕ¹ÆéW5ï\x0014|'>|»\x0015'jõé\x0013\x0001yôk±ÏçõÉ7÷O\x0007KÿxPsßZ*ª\x0006÷¡W&e>W«oÞ\Þ¼È6×M~×Ý\x0003§Ë\x000c\x000fJo¢rR¨\x001dAÂû.¤sÓù|Ëç;ù¬«éWÞ¢X\x0017=W\x0007øÖsÕO7tÛËtM1ù\x0014:0HthûùÒÕ!&\x001evî)µn\x0011ß¼ùh-ºøèÜ´XÛRÊ\x0016P|\\x0016¦äÎ2Ø©x 6\x000eFïÉ@ÛÞ\x0015:#\x0005\.iö\ù|Ã-ÁÓôèk\x001f\x001e¾ÝÊ\x0014]CÓc¬æÕåì+ü÷Ò"<ÛJÏvJÞçä?#\x001dnôzôÎì®\x001fÎ\x0017[¾ÞÃ¬¬®3\x001c	vÉhYÝ¸èho¥ç;¥G\x001f\x0012']\x0005îpçÅEoÑÑ°ª\x0011\x001e}íÃ\x000bQèi¸qå>j³èÞ°­^¶½zºz°æ³xpþòl1ûØÖzôóÙæìZÛyvq{IÇ6ó'a·\x0001n>µèðÚ!36óyÝÉGù,?êqÏòsRÚ6îÌýJÓPÚ(\x000faTÚ¸>ùöñáëúþ`\x0016ÞgÒØC\x0005àÞh\x0006Sý~[±éB÷íëw«ËC5Z\x0002\x0018\x001bÀØ\x000bHy2\x0008V>á»J×GÞØ\x00018X}É³Õ×\x0005\x0008xl\x000b\x001f*ÂÒª=ê:)t×óN>ÝðéN>¯6nÑC\x0011® ¹ðR<ã:ø¥\x00024
 é\x0006T¹sGnlh¸#d\x0004+ý³u[pH½Ï¶\x0017\x0010ß\x001aÀý\x0003\x0013H¹%\x0018¨³~·G%÷\x0001ÚF¶_ u)\x0011ï\x0013\x0001´µ Z¸\x0005¹#Ïuó
ãV}âK\x0018· ®³º\x001b·Ë\x001cÀÔ\x0000¦^@\x001d3\x0002ÜV$\x0002Ht\x0006ßÀ»òd'\x0000\x001a3Èu=#ôÃ\x0019}\x001d¥aár\x0018\x0010\x0015²ÉiCF\x0001õ_²%;\x0007<\x0017
ú\\x001a¶+
\x000b/i|±å}|Ò\x0001¹¸§âE/eyfOAèDº!ôérè·Kz y\x000e	\x0004íØqE]ØDUnOÈÉ|±åë\x001e\x0015\x0015\x0005«kêêZy Qå\x0012¾¡\x00149óm"Oà£A¥¾ìÕ2ì"\x0016lD«=¹¼/á)\x000f%Õ¸Ú\x001eòlÁÆúrrþøóC=èb2I¦ÉYI+ÑÆpr\x001d>ßv>~ß¿yýê@\x001b:s-ë³JF\x0004ZoÙeeªyê\x0013ì2O§Âòc8úÚ\x0001#F<åÜD6) SÝ\x0006Úìr
uÐ5)¨L8îû3EÎ³ÓZDHÌÃÈ,\x001cÂN\x000bÿEHp%)qÈÀ\x001fÎü0Êùjý\x001b\x001a÷\x0007lûàe ±hæ'®­À÷¸t¦Ñ[}UnñÖø\x0001
û± Á\x001e,;ô£	ì¬B,W±vÌ^Hô*é\x000e*#CÛ\x000cåfK\x0017Wä¸­&CÓ©\x001aY¥\x001eYQG~î¢<¿5
3`¬´e:MÇ²
íÀ²±6Ä©C£ñ¿\x0017kEÑñï/Q%¥Ê\x000ciJJÑÅ·zøx÷ðo\x0002<×ë_\x001e?ÿó\x001f\x0007ºZÅêtQ\x0000'uøøèá\x000bßÆ6Rz}~yq}o\x0004<×«ïß\]¼ÙßØJX]\x001a³\x001bn\x0006kª\x001e  \x001eÇå~ÈMÝ\x0011µé\x00190\x0013u(çÉ¨¹g\Ñ<fw\x0006(]Î.Â\x001a\x000co]:
,´°0\x000f6\x0018Ù\x0004F°d
ð6µº©.
k[X;{\x0017Ô\x0000Ö\x000c\x0010EYÛÜTþ\x0008;vtåÉ®¥_f\x001d²\x001a\x0013\x0001W\x001f½f\x0017M7¹Ä&n\x0012£NK\x001cÊ6 büÇ¯ÁZ2µ\x001d¦{ªmf©ÏS;\x000càüóúû»§\x0003&\x0005M/eºÕøò+yÒ\x0011õ®d\x0001ì²fÑ ¸Z}yqsÀî\x0011>ßðùn>íjª\x0011\x0014\x001b\x0000´z6fWOì.D\x0013Æ&t#Z+ÉFh\x0014pP6ÈPí\x001b<\x0019q¨ù'Ä¦ä¢\x0014¤â\x000b;/¦ht\x001cÛ;[÷eÄd6}¦iÅN>\x0007z[}{÷p¨vîm\x0018ky.Ïô\x0000	{R{èmDr:ÐóêÛëË\x0019GîMSÜ(3îDeµuzA¨Íïì®ç_\x0017¤\x0019ª%	Òª%§RRþ \x000fùðJI \x0007]i¾sCöQ\x000eíc2å¨}ÌdJêöÍ qdoÄoæeväEH;ò4Mäy¦q\x0014{,.».wô\FélCk5z)i\x0010SÒØ²à\x000e\x0018Éq×\x0000×¦ô}PCCAêùpvvùó/ë/_øåºþùÇ§\x001b

Íf¼¶2¥\x000fm%A¤e@¼|ýýêí[~¼®^ÿæúeÂá*$Bº
;\x0011£T\x001ddDËï²P[oêF\x0003ÍAFÐ/E43®2ÂÒKó%\x000b<kÀRa"\x001a?ßÝ|¿~þ|rþÓýÓ¡\x0018×ÜUÚ£\x0017ï{PÒ,Sjló\]]\|¿º½:9ÿÃåÍ¡MÈpÖ7p¾ÎÅn9uè$>elWÝ7*#<ê0Õ\x0017Â©$´znl¤pûÕðc[VÒM\x0017\x001aá^áÅ:i
L¸(VÇjB´Hx£&\x0010\x0016¸	D\x0007_TT.ék½di\x001c¤@×I\x0003Ä§uË§{ù\\x001d\x001a\x001bó(ðIä\x0007°èlh\x001dZ¾¾ÝGÃ5d6£öÒ\x0017JA-	[\x0006\x0007-\x001côÂZM\x001dÉ¸¤\x0004¬¯'·}^wó
e2\x001f½û\x0016×U½¨ÎHTe()	økøhÔX\x0017\x001f
×ÃëÊ¸#äKÖ\x001eépÄV~±W~¸ã¸j'-Ë/úZ¨\R{xSïá¥zX>»¡x·\x00035\~p3Å\x0007 Ûö<øCnÏ3ÙÑ@c«9¢gÕ¢ø.¥Ú7K§ú\x00172\x00190?&Ëß§³ÅH.\x0005v¡¹Ï]6s»x\x0014lçëMg\x000b\x001bl¡-=_Ì=MýSKC!åM;	±\x000fÍ
©R\x0019Í
¹RÄKjj\x0012f`²´þ´ÉÏ'óC\x0006f&óC
æ$2±\x001f.\x001cÎËÎn~µygwä¯Ne\x001bSÍl¹æ¦Ã­©\x001c'_RczàAÎw\x0001¶\x0003xÓÉì\x0006í\x001a\x0002pb¯½RAK¯Y²Ag£%Õ.hR=\x000b@øà:\x000cê\x001f¸Ö\x0005iä@.­¹lx©4'4ï\x0010
ö\x0014Ê1ÐÜ .3\x000còØi¾}hÔPm\x001b¬MG£4²×¢@\x0002#RS!m\x0007b§¢¥QWmBKÃØ)÷\x0001þ\x001f.-Äû\x0000ß\x0011ÜúBË;B\x0007;ÍðóphO1ì¶öÃÝãó~2ó¯\x0000Î}*ÒK¥ø¦Òûº__¼¹}M7lº\x000f\x001a\x001asÉJBâh*TL]\x000e§Ã%3K¦\x000f.ØRdÈIá8±Ò^Å=Ý§±á_­YTc»à F\x0019Ûë#[GÊ}dl¥r{úbM¢3í£¯]t4\x0000Ç2â®]x~%<KE\x0005èLK×·°@¬ËÕÇ£Ü§HWø=C'ÂA+:è\x0013æ\x000eÚ4Jöd\x0000¸ÚÓü\x00052¾\x0014P×\x0018qÌ¹Úi\Ëðú \x0017,Y®;2!)v:\x0006vEX\ÛU ¯\x000fù¿ ªVÁÑ\x000fg0Î|½¾?8z\x0006­Ý:\x000f\x0002g8Ñ?J£Ç¶«í:ùzuyhòLE³c4ÛæÔs³Wgµ¸Û­q»\x0013w'²UÏf\x0011ëóP\x0007|@äf÷ôÖb
ÿ´kìÖd8£ÆpFõÁ\x0001HY\x0000INùxigÛm×@¡ÉpÕ§YVÕwÂ:¸F[I«\x001c['hÄÝ\x0019í\x0013áb³åbïVã\x00164\x0014 ;SúX¤=õ\x0000Óà¶¬\x0019.·eíÚtª¶`ÐRáK!ÜÚ@/ÍZWÔJÅ\x001aMG?\x000c³ÔO´>¹~üíîç\x000fªebî»\x0015j\x0013Ò?ú¶KÉû­<ìÛü¿ýæ×¯\x000eËT@ß\x0000ún@ÅyØ\x0019P³S$Õ6/~[£ô\x0001Öñ-\x0019Ðé^@=t)!a2 s²Àmù\x000cÀa<&\x0001F×	H}\x001bx½¼h\x0016ëí\x0010ß:¼Ó\x0000µr­O~(>õá|w÷ðiýôóáqj!q\x0011mîô¼\x001cÒÑÒ\x001aÂ¶\x0014Ë\x0008÷ëoV7¯\x000fÎT\x0013ÎZTQ8Ûªi1ðëßÒÛLzÈÖk°Õú´ÒÒ\x0019ÒT#µ\x0016u«\x001c\x001aU[û@Úc"LáT%Ù2\x000cï J¶\x000cãÐóÉùãÙG4ÐZÞj\x000eºÔ©H³[ØÙ ÿöäüÍ¤\x0001H\x00054¤\x00064¤9 Q®gC\x000e ]ªö\x000c\x001e¨Z2µ+#¿tðÿdÒhçRK\x001d®¬¡0³õüM\x000bdÏÓ
?\x0006rå\x0019­w'¯î¼ÿúõ\x0010(¾?Ä\x001cÓ4÷*sâûjðlcæ\x0019­\x0017'¯n.¿»|÷îEL\x001aÇ8Â¤¯ý4÷VBVTV(1)i¢Æä§ÝTRÐªdî×<oÒí,öï(x¿\x000fQSHØ(~\x001ck\x001azasÌÙ\x0018Ãa?\x0007v7\x0006Wû»\x001bÜïß¾TÛ:çSµÍ¸s>íKÜ_÷\x000bÐ"4a±ÄÆ©>ð0\x00134v-uÞ¸\x0015ß½Hç[:ßG\x0007ÞH¢\x0002÷u^úÈÅjÍN:MX#ºü½\x0007Oû'9R\x0017ªrN
BA²ðò$n<ÿz·üù¢ò\x0000]=ÿøüNÅçõÃ¯Ï÷\x0008D³(ó¿pööñË/wó~shð§U¥#Uï9wïcti\x0010C4%«êÍÛï/®òõ²ºýîö-«Õõ¿Þ^NÁBåg»±t½Q¸ð)¹T©LÊ\i1\x0017Ûur\x0019y\x0004 \x0017*d<Ë\x0007¡l	ÉïZ?}¼ûå\x0000\x0011þë¾ÈèE¡lK\x0011TÉÉ\x000fG:ôB¹Xâ³\x0004åXLÞ\x000buËð\x0010»7É³oòrãX6T1¤hC|²%\x001bÞlòn.ªX¦B\x0015QQ\x001ef/Ydyý\x0016ïtª¥Òº\x0013,\x0017õd®²\x000bå¨±Y¶×ÉÊÔ½ÚÊP¶bQ\x000b¸t§E+Ä2g`ù\x001aâÿîÕV¤\x0015|Ù\	P«³b°Z\x0015JØº\x001fìó_\x001fîÖÿñ¾\x000c{È#\x001eþù/÷î\x001e>â#âîËÉ«û»Ü\x0005ìË~:J¿Òey_^Jël`±Q~êîâíå7\x0017×çø¸x{òêòâ:÷\x0002Ûç\x0008m\x0010ùþ\x0018J\x001b!D@ÈÕãr\x001cDÔf&¢Í³Á3b8\x0015!\x001a/É\x001foË\x0019ÀS£\x0010o\x0002(§Ãñ(<Dä@ÞrD¾8ç êRÒKñ\x0014÷]FÄæ?ÒFä{t\x0006 \x0014@*'÷\x0002¨EñX2ä[u\x0006¢Ùo\x0011#Y¼\x0019+\x001cc-R]È×ì\x001cDvä""Þ\x001d¥¨J³ÆHA´#!âb¤YÔDÒEFL\x0014"%DäÚxÕbÄj\x0014Ìa,Óµ\x0011r6Ta\x000eÊã0}01¦â÷¡x\x0011óÅÊ¦ýã ¹0\x00071f ÞÊÜ¤\x000e\x0019A\x001dGuS\x0002w»PÂ`\x001esDzL\x0016FYi\x0008ÇQ;Õ¼hJ\x001bLDtAô\x000eZ_|G\x0007ºµ\x0011ï\x0016=ï~Q4rw£'ÿnA\x0004A´\x0000ÇAÄ
£çÝ04$°â¡AzP\x0018CòÂÄ×wÅ(ê\x0016V\x0010I ,ÆPw£óGBÄ[@Ï»bÈ\x001b®X7Î|`Dñ¸E'&<úôOn\x001cu®ûþîáîëÓú!{\x001b÷=8Q1\x0002èËÄ£üàüÞô\x0010ÆWà¨wÝ÷\x0017×\x0017ïnV×{]
\x001dþ%uú½ÒQÅäf+àß\x0011\x001dêA°¿[:T/à_téóÜç¯Ü	#÷¿ø×çõÓ×û»'ñÂ¿^xÖn8ü\x0019_Çù*¦ÑZüP6íÂ(ÅÙ\x0005î_oW7ï./nÄ\x0003ÿzµ?åßÃç?éÇ¿^Ê¯\x001e?ßý¶~úDÞÙïPrOëÏÙ\x0007¿~.q}y«å\x000eIÆóC/j±hb\x001c¿å_½¹½ºøauó
9j¿C	Þ¬®²;~u»?øÒÀ7ólXÏ³]\x0010Ö:òp\x0015Ï,wÉ\x001e¶<çÒZ|Rû&ä
óLDi'5~D/§-Oé¹´@ã1uu6éò¡ÁMânpLÚòª-[P|´P¶¦zÌµX¹IÃQiË\x0013{þ¾-
ó¾Í>âÉÓâ#^O¦Ýéi\x001c¡§ölÁRu oÚ\x0012VÊ5\x001f³ÉÀôMû\x0012jyrÏFu<Iö@jòbÿ&\x0015z¾Êë{6-¥Mó\x001e\x0008QÎWª¤Ç¾eWø\Vg\x001c9N3«KT»Ýá^MæzVi³qµ/}Ì\x00107\x0004È´&ÈéJÉ\x001c_C³i]u\x0017%\x001d)\x0017'ãT\x0015­¾\x0011&àòÃhö¾
\x0003.^\x0011ìÝJ\x0011ªî:Þ¶å\x0007Òÿ#Û\x001a,Ã\x0002ÓËy_z ñë\x000bn\x0012U\x001bmÇ\x001döh©ñ\x0001,°e\x001cå0²®UÞ¢ÄªU\x0018Áîh¬üR/RÎKê\x0000Ä¼ÓU\x001f\x001cÓ¦¥ª-XtÀtNÈ\x0003\x0006|À´9þ\x0001óï¿Þ=eõEÿÿìÍ\x0000®áõÑåM²q¾\x0019¦(ÜÜw¨éÿÿD;(W¨Ý"hJ4­\x0006G\x001eÉbE/Vn9NQi\x0005\x001at¨ñØYÖ\x0016ø\x0017\x0000ÃM$\x001dÔô\x000bùE\x001b²\x0010ÇebæÊ,\x0002ñ4°	¡,ÇGh`Ø2bé?Îùr\x001c}ÿyý1gEÿp÷üyû\x0003Á¦àj\x0004"ùÓbóz\x0005\x0012Èñc·ô÷W«ó\x0015ýÃåÅí¿¼FîË}E#D\x0018#B7"à\x00058\x001eªBóVUge)lXÄhÆ¦ÑzZå¢4ïPëD>\x001f\x001ba3\x0019íÑö3RÓeöùÊ!Â\x0007¹
"F½|©ý\x0018Ñ÷ïF<,\x001c?N¹ïd¢èý\x0011¤ø~ÝÊqÝ¿!cIä$Izò\x0017
	F$9NÑù¡ÅüÐéÅ\x0010 £m5cÊ\x0005\x0015ü8	i7æ\x000bº§6ð¬ú~è]t
&óªÓüñ¾âAlA¼ií<N4x[\x001dI\x0016ð¦ýzýù»§¯Ï\x0007Â%\x0016xÞBÊ\x0005®Å;\x0014¡\x001e}6ÕëÕÕ÷\x00177ïn÷\x0007K*%)7½(<[\x0003
Jç»]J¾Ù\x0017)\x000f\x000bÒ\x00117Mêß ÝrÓ)8Ò\x0004%é³!T5\x0014k¶R0),§ôcÊÍ÷ÿïE\V'GgÓ\x00074E\x001eUú ,«0µí^_åÄ]©SÃ¸éS´à£à¼§±YQÖ[ï}2u¬·\x001e\x0014zQC\x001fúà8Û\x0015"v8]oð½á\x000eN;VêåoÂSd¦\x001ap\x0019\x001fû\x001183W¢àÆ¿|^ÐêÃE^\x0004ºî\x0017¨NÜ¶EõN+#*¦iÍèãÝÏO\x001fÝ8ûË×þûïÿµúðaý×CÑ\x0013.Çéyòv¶Õ¨I+'M^©[;Y½zµú÷ýï²\x0011\x0010'rv\x0000¡eÆ¯]\x001f5õ9ÉD¦fÁúE<C1ÁTdÅàö!\x0017vf\x001e+nDïÆÝ\x000c¢!o"QP&:\x0010Q<åú\x0006ÔÂYè\x000c,[³ò25eI\x000fX(\x0005f,*\x0001\x000b\x0003ë\x0007{þóÇ?ÿõn\x0014ýæîËÇ;bÓÑ»{ú¼~øòxÀêÃª¦ ØÜ#\x001f½ú¦ÆÒúæâíù\x0005E±éà]Ü\­®ßîíÓ \x0018K/Zà¹p§åôQI¡$`j¿ªå`\x0006\x001cjÀ*\x000bjròr	øh_Û©Wï_ÿÕÔU5ãÏZ½[?\x001fØaÚ\x0005ï%wÒ\x0002O\x0011õm\x000bþü\x000f«w\x0017«}ÝK\x001a¢²¿#"Ilú¿ôã¯¿þfÿ6Z¶Trñôñäíó/T#ýü´+R.XÌ»ÝE"6çU»S64iM+¹¸9?y{û=Hßîýâßû?ßÿG\x0012K²ØwOO÷\x000fûïdol,\x00025*\x0003 ZèåâøNFË§±¾/nn.÷6ñïáçÀ«Ñ\x001dsþ´þy}¿Þÿç'ru¢ncåÏ· \x0011\x000b~tÀÎoV¯W«)~¹Qþ\x000fÿùîËÏöoÛ¨oÌéF'7\x001f:pÁ\x0006\x001e
Û\x0015õsâíÊ}\x0011)\x0015Ên 9ÑèäæÍù\x001fv+\x0011Ê`~LBñZü-¹©TdçZ-ÍPàf£\x000cåP¸5)S`»¬º*h8Á^	K4ASa8ÅÆÑ\x000bm2pl\x00039®./_~½7q\x001cæ½¢Né?Q«ýG6\x0001]D¼e©¹KÎ£¢ynra0ºÌ)\x0014µÚÍë\x0003\x0019¤RûôH«
´>¯OÎ\x001f\x001f>­.£\x0003÷"n²	V¬1£$¦äB\x0018Éfh¨uµ:9sýÍêõþñþýo_ï>ýõ·qÔúé\x0003þ\x0017r\x0005ón bàD\x0018ïõR|\x0007)q¡©×M\x0008cuóêÍõõÅ»³ëOë/_îê?ÈE´þÛoêÇq¦ãÕ\x001d®Ó?ÿ÷\x000bw\x0010\x001a¦Þ\x0018\x00135i)\x000fÝ ë»"\x0017ªÞ>û8\x000c¬ÿòø37VÊíòyüLÒ8 äAëÁä,	¼Õr¤\x001b?(òysE"y»\x0017å?ý:}ÂE±êòËgÀúåËz?.ò!rÔt½\x0014U\x0001uù+×Qã\x0004¥<võíÛÕ~ô§ÿ¤#ä\x001d\x0002ä\x000f<Å\x001f\x000f äQØ\]kâ\x000c\x000eãü6%¬oÎÏ\x000füé_ãÅsãò_¿|þÖåúÃÓÝ~£Ò*ÐRÏcáÇ:ý
Ø¨´qlñþ\x0016åêÕÍÅõ^Ï\x000f1Ï¿njàõðöwFãEãÔ¸)ÍÙ,æûì°FÐ\x000c + (µü¹E"YAQ(µdÛRCXÌ\x0010+fH\x0018[!\x001d\x001clÙü1\x0019\x0004_E¥¼\x0005O3d\x001c\x0010J\x0002NüD3i\x001c\x0016éa¡8EþÌBµ9²	*°=­6¬W\x0013Ú0n\x001cúÎBÕSÌâÌÀâÅÆy{E»\DÓ#\x0017}\x0019E.<Ä\x0002ÀIc(\x00175kpub^£Ø³a¬->WPÔ7#ß5&$ö\x001e%eì¬5ÂmF,ùsú)BÁ\x0014\x0014@M\x000blÍËqÖzÞ1Ò!\x001fçÐw S\x0014\x0014´(Kg\x0005\x0013\x000cçøRÛ]ùó/³ÐT³ò9]Ï¡¢Ï\x0018@=Ò¨Ku>ÓÍëJ'ÎIT2R>§Ã\x0004~r \x000cÕ>ë\x0002ã#K\x0006%\x0019È$ËçôSMÉÍ\x0005r\x0005mIÊW=C	%\x0019È\x0015våsú±F\x0015\x001e\x0001ÞZäcmKW\x001cÊFµ}ÁPZùÌO\x000eQ1Ô]Ëüá¤dfî_|Ò*åÏé1UßåbÅÔSÐÕÊÎ¹ì)víßàcéë0ÎÔU\x0002/0nÂ34*â¬|NI\x0016NË¡ZT.EuJî¤y×£É\x0013pÊçt\x0018K\x00054ÅäÊ|®ÒæcmaÖæµ¹|¡|vHÝ "\x001e$ÇâSM9Éc\x0016\x000cyáÊgÇI²ÅÅ²ªE	ÆsixòÍã°\x0003ÆÐ	,Óõ\x001d¾TsI+àqòRÕòR¥®³³,\x0007ë©\x0003Xù~\x0013$[\x0006³#\x000cî\x001eÞ2Ô>aÜ¬SMÍ±ßÄ
\x000cg\x001f;`Î}Øq¥j¼"åVÂSßµe~úkúÏÿð£Bo\x001f\x001eÖ÷_^p+&¼\x001bO=,}q\x0000ãÌÔoßÜÞ\¯.ß^ìøÃ¿¤_ÿlFx\x0002u³\?Ý¼}øø§ý ÚH\x0007s$µR\x0012¦ñ0Kì7ì\x0014\x0006õ²\Ý\¼½>ÿv\x0007Õo¿þå/NZ\x000fçÃ\x001b%ÿ²z8äe!J2¿·º²\x0015Å[ÃöPIâ
ßó ò\x0015¢U?\x0015Í\x00087Õ_hÊ&\x0006ã%z
z×.LEF°Ú.ß|\x001aì1\x0015Z|Ü,\x000eïò\x001aBµK¨²=¬ûeåj\x0016³7A4ÞßLevî«©Tõ?:©T,ÝJçöåe'Åx[ìIL¥"¨\x001b½8
L9£Ø¸HP;éáà_"+:*ù£²+åÝ®OM±8T\x0012\x001dåa¬è)ì]7\x0015
àsõ\x000cò}¯|]AØù6L¦|¿¬ÊPë\Þí$¶¢\x0011Gµ\x000f»Þ\x0016©ÈáC7\x0015\x001ag½²Vñ[\x0010/Ý!2¸Ó\x001cJ\x0015h·îÝ\x001eÈ/;¤
)\x0010j\x0000(.Ò¢\x0014\x0011È\x001fTC¨Á§<¦0Szã¤%P^IiÊY\x0016½ZËî³%GF\x0005ÖZºJlçè0Ü£ùùWýe\x00145\x001b\x001b\x000e?¬¿|]\>üéÿÈQÞýp<VFOéäÉ%\x0013"§V£
»\x001e&h?ü°zûnuryým	õ¾ÀXâ!³\x0019\x001bïsBÑ1£ñGa,Q¶¹`Kv²\öÊÌ0ãî[¼±\x0014ÏeÔ!O¢"FjÌkíø=L]\x0002w©¹nÈ\x0012Ñ	éâC
4*Ø\x0016H(S½pc*{\x0014Èms»G^jÿpµ5¡ä°æÈfô»\x0014s7bÉn\x0018l\x001erG&@E\x0004#'\x001bÌ®¶\x0017
\x0000æ¯6²Ø¢~µb\x000b9o°P&»ËJé¦ä<MI\x001dRaÈ=)ON »sO\Üõ\x0016ï¥¤¿ªÕ\x000bdÉtÚï\x0019%ÛìhÚÀ1VâBv¾¢4ø \x000cÜ3\x0018õQyï©6<ÙËÇ ä¸ó\Y:ÃM\x001fCÛ«¸F²t»ýÝ¨'í\x0002]IÝÅ\x000b$Ú?!\x0013÷z6Ù]Ïì^Hz\x00115¯¢NHz´É­£8\x0004\x0006\x0001´lËh±à´küüm\x001a{\x0005&JÃ+õ\x0008\x0010BÕèF\x001d&R¦%J]S\x0014>·zB£È\x0014¥N}I¸×\x0013ì|jvRê\£\x0016h"#MsC­Ø\x0019A\x001a\x000fGG¥	G ¤ÇÆñ^âÄ¸äÉpc\x0017ðn¸Äw:å{1i¶oþmY\x0002õô"L\x000b¹\x0015M^s«å\x001fC\x0013Q'®³ü1WÔÐ§¤EPÚ+fKü,»ãÿ¤3Î@Ï§$\x0005T\x001eú	Ï\x0012×\x0014\x0002%íñÎ<(³\x0017\x0011ôüç\x000f«Äi20ÇÆæÃó!7î\x0018²¤ô¡ü1\x0017SÇSW®H@=°^"\x0008;#Õ\x001e\x0013ùc¶**y\x0006(KodÁä_àÕs\x000c(WP%¦r¥À9\x0019êdZ(½d\x0001Ò#Ø4mõ,Ì==
¤ur\x000cõ\x001bj\x000bÓ¤vfmtbÒ\ú³ü1\x000fÓC­¸ItgI[°F¬uÇðixzOø\x0005
|Up\x001e\x0019Ú\x0005²æ.rÁFÄsté0ß.ò\x0014îSO¹\x0013aBä\x0015\x0011vGÛz1©é_þ)L\x001a3X"Ni¨V\x0000
²æ!\x001dá\x0019\x0019éìÄù\x0007È#O\x0019Hc¨\x0012WËª×ÕÎ¨X/$=Ec\x000fË\x00112òMnÒ¶b\x001eA±'ÒhùcöÆtâ9À\x000býD´1A0á'Ê=ÝòÇ\LÈµ\x001a\x0019úÇh5%¤ðùIGxWèÜ\x0014¸|Î<@n]ºB$*'æs®
w|\x0016Ôò\x0013¤s°ò9òÓcUî%U\x001d%ëÅêH;C5½6¿\x0016ÜèÔF\x0015\x0012U.<\x001dgLD\x0003Ëï ý\x0007åsö²GyöRFfI\x001e3Zl8cÂr¤ó,ûò9\x00133:-§Èj\x0016ÇÙ[8£;Âª;r\x0018Ï¹)Ê+\x0008ÿ\x001b%/ÄPÊX\x000b\x001c2_?¥õý®¾Êøöù\x0017f<f;\x0007\x0001hò`ä\x0013\x0017Å"\x000eæ ãPÜw\x0010q#¿¿\x000fQ2Á\x001dW[EñÅà?'YíÃNáiRy8\x001e¢(1ßêÉÙ\x0019]ïEäjÒyhóÊ;\x0012´Í¨µ¨ôÃ·<Cd&£MâÜ0)\x0016\x000f¦\x001bÎu2\x0007\x001f>\x0013\x0011yÈ\1J\x001f¢Ü^½T±¡\x0018%bâQ\x00187ËPú\x0018µ(.5Ø(	\x000c`¯oÅ<Cd\x001e£¡êföcÙê/°ä\x0012-Û±\x0019u2ÛæÎdôzh¥/ÝI\x0000Eê«\x001c \x001c¥r&cJò"3`©×O£\x0014\x0002£eq¬¹IîLFëÅÏfuäù;åhw&õ2òäLeÓ'\x0002O¡âêZÛ#0Ê´4HoBÛx\x0015FyÖîI§ïeä\x000eÃ3\x0019Ub¯P¾­\x0019!Tÿt:hêNdÜ\x001bgÆ\x0018xk~xd8 g\x0001¯5Õ$/gäîÇó\x0019K7Ódð\x0005ÆG\x0006´¼gýÎ´ü^Dnz<\x000fü¼N¼©\\x0019QÍ\x0013\x000e'¹LDäÊåxKx\x0019Ouâ\x0004C\x0004Eq\x000c1r3æ="'&ðÛ\x0010 ¸POõ1\x0018÷æ<LcTQ¢NGû\x0002k1\x001e\x000fé'2r³¹k­J}\x000fY\x0014g°âZC\x0012K3\x001aª°­Á\x0001MÆ²\x001d-Ú\x0016³\x001dÐ\x001dã@ÍÍl\x0005\x000eIs¦p²±\x0006t\x00156\x001c\x000e*Od\ç1Ñò·äç\x0002 â|Iu8\x001c)r¶\x0002'F>ÖÎ\x0018®/@FÖ<\x000eà\x0008¶#9Qv;R¦ê$6¸sJ\x00148îQIk9ÆS^fö3A{_ÃÝ¡Fì´³bòìLzîED½`fß1\x001aO2G>©'\x0018ÇºuÍo°ápPq"#E>gß1Ú\x0003''K]~Å(æM=f\x0013\x00197'õ1&8\x00151:ÉªÓÒ\x000bVú\x0018\x0007³¯\x0018jBlø\x001a´QÒ£i èïÃ)³Ó\x0018mîL2ûPkéÕ,ê\x001d]¶#h]\x001fÖãJ\x0013\x0019÷&'N£á^Mø1T;Wä(7µNG81TÍkç¿\x0011¢fØåªÜ{\x0006ãî\x0011ïï#(G+Açû'|õ\\x001fZ|( ÊÑ#XàdÅÛù¾(GÇrÄ\x0003nØ_&R<ÆqÙ:\x000fßýìÏsJÉq±¡jïè±Î{óO§ùÊÒi(G\x001cÍÅGoAqngß^Â½¹§¤èsÌU\x00089æî`\x001dC¸[ììûÅR3
^iHÜ°\x0013lpÓó\x0010'2âßÓÎ÷Bª¼\x001d¾ú\x0013?\x0010¼\0Îê#Ø;.w}ï)ÓÜ
\x0006%¥\x0004ÆÕdhª_Îï2AR+\x001cµeÒìqä\x001cÑc<\x0010(ñÎ-ðBE93îl\x0010od\x001f¦cxÀÉhróo\x0018
f\x0015\x001axXV=FRww÷·êEÄËÅÍ¾`ðÑÇ­ã\x0013¥J²Iæä;s\x000c)R5ØüG\x000cU½sj1>¹äP+1\x000e'pN"ÌGõ|(\x0018'Î\x0013:ß\y\x0003 1Vc[d¹Ã^ào\x000cÀM\x0013½\Kw\x0003À_%Ï\x001fÑäèàüWL4­0Ë\x0011Í	Î<TÃ\x0008ú\x0008&&QÏ¶\x001bm¢J]NBrl}ë¤kÕ\x001eÁ5±£k\ Ö¥jÊ]maf¡\x0011Ò\x0011Ìo3<æÛex\x0001H\\x000bß¾lõPÊ!\x001aEÍÔCæÖn³Í\x001eEtx\x0002\x001d\x001aàe¦NA\x001cQh±\x001caµ©æ6ÌõD\x0019\x001aAÌ¥7Å¿\x000c5}\x000f\x001f\x001b û\x000e\x0016Z©Ø¯\x001bÐ{Ñ=\x000efgYy'dvÔ/ðÔÓ\x0008\x0006VNÕh\x0002nÐ¡»\K\x001aòÒù®zºbR$þßêc iÄú\x0008a\x0019ú³ÏòÇüè?«rEã5@lq>ÝZ\x001f!¾eé:°ó]¸6!«'Êï±¨yT\x000fK«ax\x001fmõ\x0001ÐÆ ÞGqS\x001cÁ\x0000ò\x0014ñó#3\x000eÍ[\x000e)¨ j\x0012\x0005)FJñ\x0018@óó£Tõ?ÓRüeøH¡\x0019Ö6\x001bÒ\x0012äü-	2å0×\x0008p_¼È¬Ëpuç¿¨ï´§\x00148>7Ô²#q\x0003$\x001cj\x0003üî\x0002ÉN\x00156/l\x0012/©MÒEBÃ5UÓ é!?æ®vìLE¾©ÀÅðb\x0002¹í&{\x0019
1.xÅ&nªÐúå!h#?©aùuCSÎÂüH\x0017ùí¹Á¢5Ä\x000eg 3_¹Ë\x0015P Û ÌPÃqQ¦¬\x0002\x0018ñYØp\x0004ë"Ð\x001dæ_Ü:Ô
O\x0011\x0010¾n8Ñ¼\x000eË\x000fwôÔ\x000bÏÏ×FËcV9©«\x0001ë$\x001dWÅ#\x001cîÜy$î®÷Hªxz`ÒÎs¢=Þ7Ü;;ê#\x0018\x0017T;v\x0016ý\x0004HÃ#¢Ð*WtÎ3cm¾B4G¤2ªÝõIÓlÉÄÍ\x0006\x0013Ø(çÆ$UëækI
ÛåÎp\x0017Ë\h,¾ç\x0010j¹Âò;QçX{ùü=Sæ*}5;\x0008k\x0013*GÍNI\x0000\x001eºBÙâòÛÝÈ¶ò@YÒ4\x000f´«þÒO»¼\x0015\x0013\x001bAZ-wVé\x001c-ód\x0019)\x000bµ¹¥l>\x0012eÔP[qìlÛÜ\x000b+ÑæbÁA},nïºàú\x0008F¯Î¡Îò9óf¤)^¬Î4ÓÒN¢±:._î3T>g\x001e\x001dãÒCÇ\x0017#ub¬ùgK$§Qæ\x0003îþæÞ6»ÜÈóÞ
7`\x001e ð~êÓ\x0015Åª¢\x000fEª)R§=_|(.sF%Ú\x0014é¶ûÓlcVð\x001c?Û¨ÌJ\x0006@\x0002yïÍ@ÒÝü05"»^~\x0006\x0012\x0011@Ä?V\x001cpÓ,Z\x0001Ý»q.
?xº­r ì=àq-%
{\x000e*pW¬ô¹\x0003í%
ïåÐÅþÚG¹
\x000c¾t#¥
\Hü\x0012U5ÃGþCúk\x001f¥õùI\x0011{.lÊ£\x001a\x000e\x0017ð;¼%ÏsÛÜçéM\x0001uéh5Yª\x0017§ô¼!\x0002ânNor¹®EµÄômº¶0¯ã¸4Ã?jÛËi\x0004¶\x001f\x0006\x0004ZOà
D©^ ¼O+\x0008ìåÄBX®©Ò\x0016ËÀrùþ¨ÌK4\x0002a=M7¦
<gvHXÒ\x0003Yü#äsô\x0002~ ôýÑ¦S9õkLnbWã£ü
¿¿\x000f!yjlÝ  û»Í·§Ù¹u\x0000¹1Mª@zÜJkV\x000b \x000bc4Î­Ký6\x0017×g;edÿô/ßþ6Ãà??üeÂv÷»w·qíö£EOÍ÷Zå,õõ)-u~I®\x0006SÖh§Gï6qÝv­Úß?ÿåþ¥hw>\x001bxôöþéèëÝ÷£7÷wßþv÷íyfÊQ\x0017e$©ÐK\x000fÓ\x0006¹\x001aëÊ,ôyÜ½£·g×G8UîÍÙéÅÇÓÓ]\x0003\x0003
²ÔåÜA¦¨ë>y$lò á2[ÑÅ$Û¹À\x001dû´b(b+¹Qã\x000ca·\x0012,é\x0000w\x0001Í×tÂóPh£$«Ñû2	Õ\x0005ÄÛÁ¤¥[@¼«L\x0006Y'?\x0017ª.²$ùÛA\x0006¬Óí$·åÅ Jn#_ûõ'ßv2áèªìqV¢¯L\x0002Ï¬¨[ºÈ¸o\x0007\x0019ö`!åQ\x000cñÛ[ûý'Ißf0\x0011,OÝuXèD×\x0019KÚ;ÉR\x0008\x001d\ç 8méYw\x001c%ä\x001c\x0017]h$Ð¦x¦i´óXÙÐ\F\x000b+¿2V>è@<ÆÂYA½\x0019\x0011\x0007ôÆ-+ÑHñ \x001d-:s'ãì p1 yz\x0002wNÃÚU#¡\x000e´<Ä9~ÀC4Åhaíª¾A­X\x001cVÍQHô\x00022/ÚÚ\x0003Jª\x0006\x001dd~ÜOÇ3²
äù@Z®ÝO\x0008ÝîÓOÍd4m
+:k\x0018tÄgú·SóÀ\x0006L®0Yë¼û¿þÑ»\x0014|.îïþ±ö»÷|9Äp \x000c+HY\x001d¿ûæ|qvúÍ<ÇD¦ç\x0010GHs·0äÁ;\x000eâÍ\x0003CØ-=¼a2¿â\x0000C\x0010&nÁ\x0001\x0001¥L\x0018Æñ\x0014SìïáÀ×7ï8ì\x0007Kë\x00011XNËa
×\x0013`j\x000fÇ"¦y\x0010Ãà¤ô\x001f¿ôîy+ÅÓ»1ËÛµ3ÃÅ\«åßG\x0000%è\x0019 ò$¦K\x00044W«x¹sÚí!\x0012é²M_Õm\x001eB¡\x001c¤A(Áç	Eä1\x0012vç#Â!\x0014\x0010X8þº\x0018%^ñBqJéiÈ)>¼µk!¤a<\x0013"8 Ò
§xú\x001f,J\x0007\x001e\x0016E·,
ª\x0001Ñ@o,üM×è(¹éÜé.\x0012©óô×¥$\x0006x0güÇi¦X\x000cË¸VÍ}$ÿéþCÿòçÂÆS:å#üüÛ?¿Þ?ìw<\x001ekkH`\x0003\x001c\x000bZÌsê±T¨¦\ÊGäùùôüìrÓ)¡m\x0002Bli³âO@äUzÆ\x0016~\x0005PÊ\x00064\x0001¡ÕÕ$V I%ç×VÏ··\x000fÖìrÉ_Þßß>|ÛÏÆJL\x001aI\x001fOxz\x001dÐÜu\x001b¼\x000b»lÝÛ£÷gËy[>ÌÅCS#ÄXT%g$µ¦\x0001f\x000fvõÄ,øç\x00050DÝ"\x000cHê!¹Ô.Òø]Å\x000f34îÓÃÓßT±Mï¿Þ~¾;º~¼ÿöùöi §¤ç±`Î*\x001e7çã\x0016ïûóÍÉéÑõÕÙÅÉæz\x0007Å_¾»Ï·;\x0015\x0018c`yòðíËmüg\x0002KkãÅ%õ¢¾\x0014)\x001bª@©pçw¿(Å¸òäòâí&~Î;ãÊk*»¸Ë\x0019G\x001d~ØhA:Þ¸(\x0016÷rwOl\x0003ÙtJÙR2/éÑh\x0018\x0017ÃÃÓ¸HÎy±»p¼l:l)
¤õ\x0019)4në°f&ð·åvw'5M§}-%\x000br$\x000bøF4¬\x0019äÑî"®\x0006°é¯Å\x0019(þð8F0Åî:«tÇÛèn¥\x0006²éX¯¥dÑ:Xºbï\x001e}ÿÙNèÝÅ\x001c
`Óa^\x000bÁ¼p9W\x0014ÍjRÒÓ\x0017Lîî\x0018]Îµ­º\x0014LgÃ\x0017-Íb\x001d3EÒî¬h@ÛR?]S\x0016y\x0018¤æÑ§\x001eñoX¶%zº\x0018Íc!AÎ\x0014Ñ´_ÍæÌÝ¬
h[b§KÑxú9ú¦@º
\x001a$õÕFC¼[W²\x0001mKã´Ám\x0002
\x0010\x001aÐUp¼¡^¬tøöð\x001eæÁ Ð°£Á$G\x000cM=\x001b[¿û}û\x0010Ûÿºÿou¥\x001a?ÍÆ\x0008ìîéþéhó\x000b)ß\x001fá5æØSã'JR
{j¤ãc\x0000³ãÙ8Æa§×g×Gpjù®x,Ã¥QQÃ_á4Î\x0010a	eMMBFÈÜávÜ-Zà\x0018j¾ð¯­pø ÎXµ0ìªÁõânT½MhùÇOTÌù©}íÌðmQ÷¶¡¢X#ã¦¿Jl¬ïønÛù¤\x00174\x000e{ZÈkYcÆ6f
\x001eîm*K\x0011=t&2q_§	$ó3DømwUS4â}Jx\x001dU¯T1\x0003ÊÒðA\x0003ÜÐ)«ç¡åt¿ÄïãÑ\x0014ÁÈpzzº;ú\x0012m]üáûÓÃãýLZ|ÐÈæ{¾«|·\x001d.S××§Go£¥?|¸¾¼:Ûeè\x001eôW÷åWÄ\x001aZU°\x0002åá+ÕÅüþîvÿ: 
­S´¶\x001c@àI%VøRÊþäòÊa~ºÙµ>#\x0008j\àÿ[\x000c\x0002@Æ\x0002+\x0011è*\x0000_´­¬òj\x0007Aþç?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ýåë\x0003
\x001b?¡]k­°4¯ÇÅÁÝq	Øe~§¡È×7\x001f?e?âÃÕùû×ç\x001fN/¦Òp+\UãªAÜ<¼4ábG³ô$\x0008\x000e÷pÝöõ\x0018ÅÕ5®\x001eÃÕèòëm®$¸.[\x001d\x0011WïØÝ£¸¦Æ5c¸\x0006gæÝÞóaÀÓqa·ÅÂ(®­qíàî\x001a:¸AfíåÀ\¤ëp\éZ\x0007×Õ¬nÕÊCQÖ\x0008¹{\x0005Ö¶æV|qkw·QZ_ÓúÁ %ÓJ\x001cÇHh¥ÛfÚ(n¨qÃàæjêÔ\x00137WÑté¸¹TgbXo2¸d¿°Ì\x0015ÛkdNGÛkDî\x0019ïRÌ+v\x001a3ò¶:bPIXGí@âþZOÉ$JD¯)óªÝl·Q^hxap£Q_âþF\x0015Ï\x0003\x0004#MqåÎ\x0004QÞF©ÉA­¯/ÎoH3\x0015q%\x0018Þ_µ3]|·ÑjrP­àX\x000bGIç(bÐÑñùU«Ý·F­ÉA½ó?m>\x000fØç?ç}¨x
HWh±Úùmô\x001cTlVó\x000bRç0ñ¾éé\x001b÷\x0017\x001b×ám´\x001cT\x0017Ö¨\-òWS.\x0012qwß\x0011\x0007q¡\x0011¿0(~Qø¢ò\x0014Q1oØò6â\x000c\x0006ÅY´\x0018Y½)¬<ËÒÁQ¦ÖÒ\x0015Uåz±Ë¸â¯Û4ó¦H\x0008Aâ£\x0001¡\x0005I`iwúì\x000c\x001b¾ÛÔf\x001a½@æº£$\t.,;\x0017;y\x0008ÃÎÅ6´\x001eßêx:¼ÎÐÆåçBY\x0015è|HØlNPï)õF:Y¿Hä\x001fÔC~ºûÛÝç<èp\x0006m¼\|÷¼P9¾mò,©\x000eç\x000fî1¾þ|}öÍÙûé©\x00152ÔÈ0þ !Ç¿¢\x0011y*pÚ`·Ó­cX×Äz	±È\x0002\x0003\x001bHÃÄ7y§\x000fÚ8²­í8²ÊuÚ\x0016ëOlA¦sá¥;¤òf"Û:ÊPwàwûøÏ\x0014
\x0005\x001d5rNÌ\x001f¥²díBüá³üîôã>Ç©¡¦ajÀPU lIí!pògl¹V½\x0004[ÕØj	¶Êý\x001f1ÑMä40±a§MÞ\x0010¶2[gD\x0012\ã,¥962È\.´¡:'Àqv¡\x000f\x000fò*LUcª\x0001L[ecøO°\x000e-ù~ÐS:Ji·7Ó¾læ\x001f>ÏÔq½¥Ô,x#\x001dæÃ:îôíûË©Æ
\x0013jLèÇ4"7VØ^\x001eªDB·èpÔd&¥ª)ÕÀfz3z³w¬,ÙfZ±w¼óÄ0ikL;©Â	°\x0013o\x0019Ó¹âdÂÎ@¼.L-·¦U\x0007\x000fÏ÷_fª.¥³q\x0000ÎÓD`°ZÍ¨`gp\#n6\x001fnÎ¯\x000fé,-·Î¦U\x001eNaòÈ©èF¨j¢ã©ÜÁØù|T]£ê1Ô$ã®j |Ê*
Âa\x0003f6ª­Qí\x0008j\x0014\x0018°IÇ4Ü\x0002Ða\x0004/½Þ©)\x0019Cõ5ª\x001fCõ¹½\x0001JQM9\x0010kX.=ªfû¨\x001a>ªW	äÓlO\x000cû@%\x0019\x001f¦äp¹0áÐå¿J¿¿ôÄì·ßþË÷:@¢¯¿.îï7oî¿l^ßþüû\x001f?cj\x0012Ô6¤wÿðê\x000eí*±\x0008

Ù¹\x0011è5JÌkKÛ\x001a]\x0006µÓ\x0008÷ìýæÕ\x0019Z!\x0017çg77ç×\x001b\x001cu|þöýTV[Í\x0019øë÷Â¢ñ×(¯Ppâ2nôeR/-«"Ü°Óbs\x0000÷û§Çï4'<¢\x001aøðéö{<µßÝ=~Ù¼ºÿîöùË<^áCÈÍ¿"°÷¹TNb\x000b\x0002OÀ~'Å¥\x0000¸8}§÷ÕÙÕõæÕù«Ó)ãªA\x001b\x0000=
­È<RGbï,CÈvgzÑ\x0010r¸ý·\x001f¿\x0004\x0012¼(n¿º{ü\x0019½§Í×Qm>Þ}¡\x0017ø9ÔÂÑô(Ù\x001cEÍ¥
Æ$\x0019a±ÑäAþêìê\x001dú\x0004\x001f7_G¶r#=¹Ocahe-ä\x001f¼xO¯\x001eï²«;\x0003\Jîæ\x001c·;:`.\x001bås. 6¿Ý\x0014ðìÊ|Ü|uu6íêVÀP\x0003Ã 0&mé,2¼R\x0016<ÐyÖz;X:\x000ckkX;
ó\x001eó±ð:äh¡ÑÖj;-ÜfÓ\x001a¿u\x0016¯çøÝ>ÿøüK²rçâ u®¬\x0001§1èD,%ðÝÓròîq§ÆÓ·74v+d¨a\x001cjPË\x001as\x0012*¤ùqbU\x0013«ab£ó\x0003f<\x0013ZlEbë\x0008Yr¡qd]#ëadyl)
x¢MF\x0006(BÂ¯w.Ll­Ê\x000e\x0006î2å\x0008GdÏjD\x001dm\x001cÙÕÈn\x0018»àEdÌ'²\x00199ä1P\x0016û\x001f\x0017\x001dÈ¾FöÃÈQJ\x0004>ËY\x0018K­X\x0018\x0007½ÞA\x000e5o\x0018äX¡*ò©ÀwcÈÈñ\x000fB\x0006µÓTm\x0018Ò3X&%òu¹Ó\x0012Ê\x000bÞe¿S$<ÜªQ="AÛ<=.n36k¼Ííä=áqæF*ËQ±,\x0015g´Gf\x0015rcSiðodféwzA37bYËå¸¹Öyáòhh\x000e	Í\x0012Ãî´\x001cgnä²\x001c\x0015Ì\x00128ºQw.Isò>ïzÓãÌ¶a¶£Ìø¶Ó£[\x0016Ì\x0010$é\x0012åV\x001a.£ÊDª(JÌ©uM\x001a6X:\x001a\x0012vBAãÌ2£ÚD¦Ú\x0014Üd°r¬ei(\x0014 ÌNçÑqàFÈau¢¸:\x0016#ÄÔò\x0015Ï2kl\x0011vÞU¡Q'0ªNâY\x000e¹ï\x000c¦z¥v\x001aù0{²åÔN4s\x001c¹5ñGm|s\x0014u±>ðõSµa§Âe\x001c¹Ì0*ã\x001fªì2>¿WíX¬'ã q0,ã$Ð2Ø
*?¾I£\x0005\x001f\x000b\x0008a½Mnä\x0005\x000cË\x000bÉ-0ë^â"3pô\x0010vg\x000b\x000c3«æú©áë'Q¶ÑaV*§+â>\x001bÒ%;ÉtãÄÍíSÃ·\x000f$
²CÙbF2æÅf^oë§¯\x001f(z³Áü[[DDfêÅ\x0006èjÄÍYVÃg\x0019¼Í\x0019\x0005h\x0016|-X¶v\x001aq\x000c\x0013ëæ$ëá¬0.ë>,ÕÈÀOGz5âæ$ëá\x001c\x0015\x0005vUHÈZq¬\x0013M\x000bV×;ãÆÛÈËðIÖØ(o3ãAËX:Oå\x0015Ý?
4ée§o½) }vt4P¤J¤X/(eI^|ñZëy5ý\x0006\x001dEõL\x000e\x001cÑ\x0000¹æ¡¦ñF/ýÝè\x0019\x0011¹9\x001e\x0011K\x0004#u í\x0016Â
§ºÉDÊ?à8ó»Û\x001fî~~¸ç\x0017Õyq#ÍAü\x0010 è\x0016\x001fÒÄAy÷îôÍÙ»ËóÃÏª\x0005\x001ajh\x0018Bø\x0013¥(Ô,Y\x0011bÎ+AïÌ^À¬jf5¾Ñ^æÆïø¦Ø«\x0002a_Ó\x000e+>h]Cëñ\x0006zß	æÄeÕ
¶<	q¿\x000bmMlÇ\x001d5¯Æ\x0013àW\x0008¥\x0002\x001f
u8¦ß\x0007íkh?\x000c
Và­ô,7¢ÇïSjú¥µ\x001f:ÔÐa\x001c\x001aß\x001f¢¡Ô$)B§h¬w<d+îåÄÖNRQ\x001c0¹8QKåzEÙ!\x001bÙ!Äú/S	G·\x001dõév
´\x001bÖ«¤gá\P#£>Ñ¼ÕúpL¦º9ÕrüXèd\x0019: Z°[\x0018\x000cïµ6;¹¯ãÔÐ\x001ck\x0018?ÖF{úâ³D}Î\x000fGÞ^ûMÃlF\x0001[üò[&¶À69å(86=ôNúîóÑ§ù°y:tLLÎCÅÃ-OèlS¶,îø\x0017òÛï·®ä÷Ãw\x0012\x000bèNâk\x0016;1¹íNÿ\x0012¡½³çrÉ\x0003SxÒíöÜøPRÔ\x000e\x0007ÆzÏ\x000bÏ\x000e}9/<;tä¼ 0\x0017éN²Y\x0012l(7ôð\x000bíLö¦ËZþAÐñ)µ\x0015¼ýüãl3ÛäÉ2\x0018ü7|X@ñ;u4Ùàbsv}úþíqd]#ëqdtg2±6\x001cWâí¤2\x000fóÚ×óf\x001f7Ò\x0016µ\x000e\x001fàÜnû^ÞïÚ®0öÛWUW\x0018æýñS<Ês:1ô\x0002çMnü\x001d\x000fwIæ\x0010;CL÷ ¿½'ù83ÔÌ0Î\x001c©9:í\É@Q^ñVcCó¡u
­\x0017@cÀáC¦ð4'')§Ö¶5´]\x0000\x001dJ\x0016
Ö¾Q\x000cG·ñ;ÀN[øqhWC»\x0005ÐX\x0017Iï^\x0007\x0017%øí^ìôY\x0018ö5´_\x0000í,GP±\x0010Ü\x0012t<*üH{4åg6tÉyU·7\x0019¡è¬\x0005\x001d\x000ex ¤r\x0011ÕÎ\x0000íqèVâ-\x0010y2øÜ\x000c+'\x001d°Ë(ø\x0001_¹ZûqjÕP«\x0005[-U¡¶:wmB÷\x001f>ýÑXä|èF|È\x0005ò\x0003\x0002
í*ä\x0016\x0017èèòk²«j»­\x0012mUãõîöñö~vZqt\x0003D6@@ê\x0019NvG2Ho°üôô|:¯ø»¶
ha6¥èæ¼F\x0015/5ÆÉ(Eî\x001f¶#[	WÕ¸j\x0010\x0017d®þ¸ñ\x000e\x001aÅÉ®dlXï\x000eÛóqu«Gw×Rä@¥~¦\x0014JD²U;T£¸¦Æ5¸z¡õ©8CZ®7p°Ó\x000ei\x0014××¸~\x00107Zö@¸Òs¤Þ!\x0016'$¬µ»¡Æ
ÿÍ\x0005C­írîÝ]#ó\x0013²ÂáÙ\x0004åpÛ­W\x001dÅm¥î°Øâ\x0006~×\x0004íé¦9wä~>n#vå¨ÜÅÞÒ\x001ci\x0001On#­W»²»rLð¦Ê\x001c¬Pð\x0012%\x0002ÏÇÁÃNÛQÞFðÊ1É\x001b\x0003Í\x0010ûë©g1\x0007Çm-Ñ \x001bÁ+Ç$¯ÄÝ¶×\x0013*G¶\x000f\x0019^íL\x0007\x001aåµ
¯\x001dä-R
­JA²ÌzS#ñóy]Ãë\x0006yM N)¡ÙÄ?u4·ÑlrLµÉÔcö\x0017ã³\x0013nIµy}$\x000e4\x0017\x001ae\x0001cÊBbÝ\x001cOQØÀê¦¢uÃûkw:¥uóÔ¤Y¿¨âäÿñ¯\x001eîò®rá©sªBS{æì<õ°ÅªÐÉ`Ê«Ëóy¾Èja£l_E6ÕóTÇ»Í«»Ûç\x001f>÷\x0014àò\x000b«µ¥fØr|P»0mÿæIgñ/OoÞ]¾.¿-ØºÆÖ\x000b°­b'Îc\x0016\x000fakÉï~îÀÃp?¶­±í\x0002l\x0010yt&½g')§ÃKEkÓZ¤\x0003\x001b¶ów w÷´ñ%ÏA> à½:OèiiWzÄÿèÑrg¡·Ðã,Uñ¹¶*Íçîy]\x0015\x001f° l§*~R³ä\x0012ó\[Næ\x0013ÍÑ+t¨Ña\x0011ºWyÚÃvu<¿^\x001e­NêpLá±úx¬,¶Õ£\x001e¸°/'LÎ\x0017Ûñ¹5à\x0004°\x00115°\x0011ÃÄøC© ,E²´Ðt¾­÷nòbv"C\x000cãÈ`J\x0013xN\x0014ddIøóéLí9ÈæÛOÿû_þþ×ÔJ
[fâ¯«ûï£\x0008Éò{©ñÕÃSúûØK%\x0000¦d¤]
:è<ºÊÌi\x000eNI»\x0013[yuù1¶«s\x0014\x001bø»rf\x001bIÑÀE¿:ád\x0014\x0006Ù"ÂüÏÜ&
§²Qk^µÛ
a\x0004ÎÇ3¿zw\x000eà«¼s\x0006²ù\x001ew.Zi\x0004·[ÐµK·_È¢jZÈæ\x001fàuûxûùM4×æ@Z¡uÚ¶\x0008éÀÑ@ÉèW\x0018¿¯v'Ï!ß^¾³ÚqH¨!¡\x001f\x0012Û'#rL'Búì·%!;u\x0008; U
©º!
ã¼AbW\x0006L>DÞÉ¸©Ë!u
©û!qUTÑ\x0004ü¹\x0003ÕÌFÈÝ¹ß\x0003¦4ýÊ_æ\x0014Ø1\x0018wÒ\x0013#î¿\x0003¶f´ýÑ;È\x0016SZçÇ¸ÊÒ×\x0006Ø|2\x0000éjH7ðµ]Ö9¬á¥k\x0013ø[ÃNîÑ\x0000¡¯	}?¡\x0017åS{jÕ\x0016\x0011µ¦
f'Ïh\x00002Ô¡\x001fÒUét\x001eB?u:æ¤;©ïý\x0014e9.\x0006vÒçé+\x0006m³\
\x001f)å\x000c;¦Ä\x0000e«múÕ\x001f9+l§MÈõïø½i\x0016T»¥\x000f\x0003ºýú&\x001a\x0016üÁ£(â\x000fn©3¯T8}1d£nä¾ñ\x000e\x0007'J'²×\x001fÜ\x0011änß\x0000d£nä¾&c¶\x001eãÝ!\x001c·Å$&4-§lôìW8Æ\x0019ìÃî\x0011ÒQÃk©Ì¤Û\x0001Ù(\x001cÙ¯q¬àZ¸tu,©n§_®Î
b¨Ñ8²_åXÉý³á\x0014ôHéóK¤t;
.\x0006(\x001b.û%:ÎS"HE\x0019Å^§4ë\x000céw\x0002ýÐHtèèVxìS/¸;Ñ¶Ò2ånÀf²èÐ/Ñ-f\x0015å\x001bÉå·2\x000c©×Ðú\x000fý\x0002Ýg3\x0003O¥cH(rù\x0005F C¿@Çêòü|â\x000ckt*¹!¼Ô;9q\x0003@~n£Iitô\x001c\x0008,§­Ôj'5d²\x0011è0 Ð\x0015\x0017gD§Ëä¤ÈH©¨}ºÔ0\x0019\x0018è l$:\x000cHt«è9\x0012çmäçÓHi©¥²Ôf§³Ç\x0000e#Ña@¢cA0Ýè|ó^jÞJ½[\x000b\x001b\x0001ý~Å\x001e¤\x0019ÒºÛ}GH(±{ñrÈFëÀÖÁè|*­\x0008ù}\x0014ï\x000emäò\x0013©\x001a£úU\x0003®ÕsÑõÎ\x000fä^ã7¦}\þ©U\x001bf\x0019\x0010FS>³¾³\x0000Å
:Q5âG
\x001f9y\x001b­gR\x000b/\x0002\x001fÇ\x0015\x000cJÕ\lÕ±]10qÜ(úÖ!ý\x001a[Ò\x0017C\x0008Ò­ÀSp 	!áðûg>»²k\x0004\x0000Ã6k\x0018A5ÖP;d¬\x0001ÌÓ/£Ù\x0006V±¾JdhÕ±zz2É¡
B
nÈÆ_ùÅüT¿<p¿æMo ]+*ã\x000fF\x00026@BnOáôjÊ§àNÍz~&Iÿ»KJÏ\x0010£¤2p\x0011f&÷\x0003Q<÷ÉÐå,R\x0011¿ØVÔßÔ9É×\x000f£½ò\x001ff![®£0Bô0)"ì©÷à&=tÊÑ¸¾ºÄD
lyèÁÂÔY\x000f\x000eÐ£Òçà¡
\x001cßôRp\x000cVïtù[®jtµl×=õm»N3gq×Ù\x0007¿D°\x000cÝÔèf)z6btt¥R\x000fÙDÎQe|ßZ\x001cÄÖQ\x00071U6+\x0012esÅ_
4gÛK\x0005,c¥@ód¸l^Á@E\x000c5ñD=Ú¬ â\x000fö´¤H°]BF6ÇºU<QM2ÓÂ
\x0014\x000c\x0010:7\A_!pÈÂîý
#ë\x001ay¢n¦eAÈÊ©\x0017Ë¢ÜDí·³m<Qþ2Ë»\x0005ÊãWPÐÁÐBÒ×x\x0005'ß{}M<Q6ËTl³k¥KhGVK,X	¹~H\x0011Eh³Î²a_\x0008[
oDA^í(ËF`È\x0005\x0012ÃpYÓÖVÌeÕN\x0017çaææúÉ\x0005÷ÏjvÑ\x0014\x0012\x0004asY¯ÇÜÜ¿©ú³YÌå\x001aÇ¡9rä­á\x0007"#¦Â
ÝÌÍ
\x000b® ÔáÛ\x0019)ò$\x001c¨û\x0012\x0003kI
i[ç$íuÕâ­\x001f\x001bàFG5ä\x0006¸èNsLÙ5H=(-ÿ ènä}¼}þôýÃóãL+É¨Â¬rÓÓÃàXyÃáíÞ]Þ\¼¾¼¹:h"Ém½ò2l\x0000Z\x001bAÝ\x001dö¥Ó\x000cdËk¼\x000cHöCC{Hp·Ë\x0019\x0019Ùp AO.µ\x0004$³Ô²y§v&1\x000c7-õò\x000fjô6ZÒ÷÷³34Õ8;a7zÞ\x001cÓÝy\x0017Û§ú4ÑçWçuÓPa\x0018Ùò\x0000l5V²¨ç)êÄûãÈªFVÃÈÑ\x000cåWÓèó=äQâXI|LTÏGÖ5²\x001e?\x0018\x001aË:\x001dE\x0007§\x001fÐ5Ê\x001c¾]È¶F¶ãÈ³\x0008±O«¢!fäÆRãÈ¾FöÃÈª\x0004ãµy°\x0008
èÕ#vÆ­\x000e#W6)J\x000c1Ì\x001e!\x0019þ\x0010
³a[	ÂN¡Ç8s#2ä°ÌÀ 
;+â§	U)fÓì·%³oGs},hð2Ðóa½ól&©9Ñ[¸ïN¯&{/U¨P£Â\x0010j´èhc½*qf¥9ÓB\x001fl3IUMªH£ïøù\x001dJn\x001a\x0014{ùHq6ª©QÍ\x0010ª×%\x0011µ\x001d]±`´æãÉ\x0007¦>TÙ?é¸V&r\x000f±\x0016X
/X´ßò
/rl§è²\x0013&È¾\x001c\x0003LÈ}©\x0008|xþtÿyóëÿÙ|s7/Lçi\x001d¶è%_DÑ¨kiôÎË­\x0018â»Ëó÷ÓÍ7g\x0007äÂÄ®±ãx¤tí|tÎ(£
_i¿=LøÇØMÍn\x0016î»¡·]Kå\x0008Z\x0000§â¥¡Ã+Ë\x0006\.$\x001amzæfnØQ:~<wz§j\x0010ÞlÛøÆÔ\x000f,Ñ!Iý¾ï?Í½\x0016«v
½WGï\x0005üJ±§=òvÀ<º%©é÷ùtW¿
\x001djtXn,Ovu\x0018>àd>ÌÑÍèr2[w\x000c]Õèj\x0019º+	! Ùî·å¸\x0007ãýÝèºF×Ð=¡MW:Å¦xÎ°ò;íNÈ¿Ûým®nÊ?xûuN§Ï7OÏH_Mé!tÞ+¨*â=Dù_ã?Gé´JøÉÂÓÍ7¸RqJï¡û«Û¶úòÒçânHÌ\x0018§h<\x0017fÂå\x0008l*oÅÔ¿mEÌþBMý­ýgû÷Çg\x00122¬GqºÛä÷ûç\x001fîsWQ*"ÔDà»?DËûéá3Âb¹®ÇHº
\x001e0Úõ@'\x0018RÏ®mPV'S\x0015IQÉ¼|ÿ2Ó:âæ'üË7çgW\x0013Ç¤ÁÍ¢qµÍM¥<>© \x000eM¸Ê0nâ­\x001båZ+rÒAÄ
\x0012ÏsÂBë×¥Vÿ67þÛÌ8®jÊ)DkÉã3\x000bâj\x001bÙèo%Gv=Ü<0|xw}ÒÛ\x0012\x0002\x001bãî\x001c	è¾ÈUq£q¿£\x001b?_p\x0016\x0000òte\x000f\x0016Ám>\x000b\x0016ÏBú\x000f¬\x001b½â0£[DÞÜ \x001d\x001f]IpãßNis«áb´\x0008_5à³k]\x0004¯§Ó@=ÖãE¥¶@«áûp\x0015øè¹¦a©È~WÞ_[­Ç\x001bU\ Ö&9&-\x0016¤ÍÅ§´¼¹6¬\x000b\x001b\x0015\ Ôt*P;«Ó ´³:×\x0017ÄµvÝ\x001bõ\ Ó°®\x0016ksqsókÞÜüÚ\x0010°U¯Ê\x001b¥¢\ ÔPñ\x001a:¹Ø
6\x000b2l{÷\x0017äº\x000c\x001d\x0018¹@«)C¥Z\x001e°§MÈ6ö9Q5î¯u%Cü·É\x0005j-\x00083\x0015½r!ÚéÉÞÕ@\x0005pAG¼îþÆ\¢Ø|Òfiuò4\x0005xÞ_\x000f\x001d¼Ùÿ*M.Pk\x0001O@ºlQ#DI÷6ÐÞ¤^\x0015«í-ÃÁ\x0012­ætLøÜò÷6G=£\x0016Î	EëñF1\x000e\x000b´Úõö¢«¶D©Eù¥òö\x0006\x0011¥\x001am¯Ñ¤*âî®Ë\x001b\x00059,P\x0015\x0011(G{"/¤¾EÙ(Ë3¦B®O[7]X z£ïóî}j
¹³ÈK#J"/ÖË®É\x001b\x0005
,\x0010eøBòÚQÆJ¶Ñ)\x0019-\x0007aV¼X¹¤\x0016HTw¡²&ÆÂ\x0011²!!M,uäÁ\x001b\x000fZpÝðýÎ\x0011oÜ^0d9X¶Ì^õ8È{v/þyÜ@\x0013¹wq4Ð0ÁS&ØÏ3ÒV\x0012\x0019;Þê%ØÑ`Ý\x0011p¤Caù2{p°ª,\x001dí¶[ý_¬B¤'j¿ìX3CÐ\x0008J¹ÓfüüFZw³éÈgÄ¨<î\x0014}%ÉYY(Ç¾\x0012¬ºÛ
÷Çe\x0017\x0012ËiÖ\x0018\x0011\x0013c)ð\x0003#Â°;útÿÝÓwÿ\\x0005°óõÓæüÓÃ§#çn¢Ç"\x0013\x0008Ôð\x0007=f·ãÔåwêóËë©¶
Vüva	ÏQ\x0012\x001c©dòr9T\x000eðvAÅÏ\x0019\x0002A)\x000eÝHï\x0019Ë¹\x001d½\x001b+\x0007r{°¢1\x0013\x0017Qìã\x001cq¤\x00124Q\x0006¥¾ZNãµ]Tò|\x001a	bòE\x0013í(ün&I¥ÊÓù\x001dCÊÌßQ3\x001a`\x0018¿ãìß±Lg»éP¾:L\x0003¤²±$L \x0000aHûÒ\x001béTÿÞaÒ&}ÖhÊYú¬NÙ²wË¯@3\x0003[góXÜº"Ì°p\x0019ü°ßýïýáîy[Æb©Þ'|½¸ýòå1%
]ß>=Që\x0003¤
ï\x0016\x001e°+Bê@ãíÝ/à°Pï"'á]__¥t¡ëÓ\x001f\x000fô·nØóáBvl?UÄË!Å\x0001\x0001\x0013Ü2<5²[\x001d¾Ò"ãðN)zéÞH_!¼\x0015|»D\x0008¿ÉÎWÚf\x0001¼ÕäVKo9\x000c\x0000ÖðÓ\x000c¶Ðÿ-à+4\x000eoÈ­Üqç\x0003N\x0018Fx-96\x001fUþ1´\x0006|¥º\x0016ÜWM)\x0014\x001eÛ1
1Á\x0007\x0016{Âï¾í¯\x0001\x001f¾ý\x000e_Ç¾[~rhüc>9"ÐÉ\x0001('ç7Ù|²þõ(_°\x0006Ì¯ 5`a\x000c­!ÍkÌW×ïø\x0000Ãk¸3U¿ü´c½b¶õÛÛÇ»cgÝË<e8¢Fun3jt®$£ê	û\x0007³«ß^M¥	5`µ©8\x001b\x000cNÀÒ9v/`Aó9Þ}î\x0007«­Å¹`QxÚ1\x001a÷f0Î@"Í]\x0008_ÆûÀ\x0014F0¡èÕ\x000b*7ßL\x0019=`ù
¼sÇ\x0014Å,%Æ\x001f²K\x001cU/+2·ÂäÇîÎ\x001d\x0013¼cÎ\x0013I`ÀRìÉê'£gâ>2åÓ\x001f]5|\x001cLd%µAì>`öÑ+k\x001f\x0015'RÒ¥&d	Ì:>dzB<÷]Ë]d6'«?µÔ¢&ñ¹`Xlå;Gý~þ\x0018\x0006ø~C±öðzüÊò¯\x0006~¤XPüsdýôéîwâ¤¤ü@:\x0002çÐ[°¤¿À]ï¤\x001aôAñÏûââlÚU©³¹?
\x001c%ÃÛA7(	::Q\x0014\x0006WFì8{Ë³ª\x001d\x0006NÈI~àÅ«d\x001dkl8\x000fV»t\x0000÷Ç»}ú×»j¹9ÑÓææéöÇã»*iv\x0007ìßJµWBqòÚ®¦ãfD\x001f77\x001fOßÎË\x001eÇ'¸Qþí««tþó_°Õ
Ýó×?Ýþå.ge\x001ft?Å7ì~r\x0004\x0002\x001cV2çÀ7çï>`{\x001bºî¯¿>ýp6Ýpæ\x0003ùßÓ;óoµcF(½Ù|}ÿ\x0018?5¾ÑÊ¬¦1 ß/\x0002;\x0006Þ±#2ó¸¤Í×çWøÛý°°\x0013U¹FþAUø÷ÍÝã\x000fÏGÀ´\x0013\x001cbZj\x000eqçô\x0000vÚxþæìêÍÍûÉ
+xPãA'5Úa(v\x00137>,X¿û\Õ§j<Õ
\x000e$-\x0003Xév\x000f¬d-³\x0018O×xº\x0017ÏäV\x001d\x0011Oñî!&<9iIÌÅ35éÄ34\x000b\x0018ñÊ÷|örS%t¶¦³tXdLGÏ\x0018~àõ:·Ut
&Bý³ñ\ç:ñ°A6m\x0001N°ò xóÔ®½ÐGÛ,WD\x001fñRY%N°	Y°¸@Y4à¦\x001d¹|­Üë\x0014|8×ù\z\N|6w![Ê×\x0008>Ù)ùñ\x001c~Ôñ\x001a« è¨bä³báñä¢\x000f'þ¸\x001cÖÁPlW9ê?\x0018ùÜ\x001eÖÇ×>Ù)ûÎã_\x0010O\x0018:~\x0005IµKñ\x001aá";¥Aé(\x0013o2æèµ°æ|uÍ×H\x0017Ù)^¢qBo&FylâR\x0000¬ <Ý¥áù\x0006Ïwn\x0014¹ÃÇË\x0018gH|^óí
aáíFúA¯ôËU\x0012qó\x001c6\x0015Ê\x0019M¦lÞd\x0014k.\#ú Sôi'sÿÍÈgæü\x000ez¹\x0003\x000fKE3´6_§èCybOk\x0016-ÖÒ#; Ä^È×>è\x0014}\x001a\x0003H\x0019Ïj.=´E_l\x0018@#ù Sòi/
\x001cå\x0006[M\x0011Ô\x0008·ðÞBcñA§É#4í\x001dNqû©È*ðv©ÖF,C§XÖV±U`ò|Û´}ÅQó8Ps\x0019_#¡W,Ga3ÊdÜ).Æ3N±h±\x0013Ï2óù\x001a¹\x000cr9ªÝ\x0013ýpã\x0003%Êz¾\x0018f7³\x0013.4p¡\x0013.·þKW\x0012\x0001T4\x0014È¤ò8]f\x0011jêT\x001a¿ñæ©Fi¨N¥\x0011=\x001fÌ%Ng\x0004W{\x0019	´yAîvò5JCõ*

k`\x0005ÒÄ \x001dß\x000c·¯\x0014t*Ô¤;\kS\x000eYÊ\x0017\x000e@J7,\x0014¨Fi¨^¥ñÛo_£8T§âPÝIw7¦¶O;\x0012ÌAï\x0016\x001bvò5Cõ*\x000eÌÏrE¶Íg^lå²¥Q\x001cªSqà,Q\x001f0\x0010\Ô\x0012L|4ly	_£8T¯âNÑùÓÓ\x0004
¥\x001cC\x0010»57xêPªC\x0001M+ÂíSx\x0012ÓöE{·o¡pÖæÐ\x0003»ºSÆ	
\x0017G%@"ð×¥\x0016³nîU\x001eBçqqû@â0´}¢(©\ÞÙxîÐº#úfE¸¸4(\x0017z>}Ê.\x000cëFwèNÝ\x0001ÑY¸D'òÄfá¢´åôT³¯
3w*\x000f,¦5tyÑª§ý³?¯Yj\x001bèFyèNå\x00018{*oö\x001c\x000bRJr.X\x001aJÓîÐº\x0003\x0007\x001c\x0014Ù'eÝfùöÚLÃù|lÖ²Yãx\x001dÞÍwñíhd³îÍ \x0014[¦X*ÏWp\x0001Ãd
÷\<ÓÈfÓ+åê\x0000S*Í%[\x0006Á-
UF6NÙ\x001c}[~\x0001tX\x000bÆ¿iûò¼®%|p6½Â\x0019§<°îðE¸p 4øÝ²N¼F6NÙ,m\x001aõSÖU\x001bPRÖ¾±F6^Ù,rkð¸{JS²b«ÅOÕ\x001bÍfkßÿ:å²2±"\x001e¥©¨CøèYµÐ¬2`69:µy()*\x000eÉoDÊó\x001bV\x0008z¡Þ5Qo:zì´a(ëAù\x0013*\x000f\x0005ßí\x0016Ó×è
Ó©7¢ÓX$qT»\x0010\x001d9ê\x0016\x0014õ®?"ùöö}(pÖ0Z\x0003÷Î²w7\x001bTÄÍ[x7l£6l§Ú\x0000\x0007üþç°æ,;lÊøb´,Ôj¶Ê¶S*\x0015,VL(í÷¨\x001bIT¹)sé\x001a¡l;2\x00167î_úT	~|¿[úºf\x001bÁg;\x0005p
z\x001fmSIegÎ³Ò\x0008»ùJ|mêC¯à
\x001f>ç0Ï )µP²ÿa©;n\x001bÁg{\x0005r%OÜXN.àJÀ¾Ôb¶ä³O\x0006U\x0014Gtl*\x001a\x0005)Æ°ðÃ6ÂÏö	?\x0015+FIÍ\x00131].P£÷´\x000bÏkë\x0014~Ò\x0003ugFág\x0018à¢·hQ.ü¼®1]ÉóØßÅí\x0003Ú>Eþî\x001aÛ×\x0008g×)%N6åíã¢\x0000\x00058eöo¡Çá\x001aéìú¤³
¦ä\x001câö)·\x000f¸rT¦\x0012E|Éì:Mf©
ÎÓÌfi`MúrüJ]£<\òP\x0011Ç}´\x000c(ÿÞ{]ªw3\£<\§òKäS=\x0016[õÀÂå@}À\¾6q®Oy(i¼\x001b¤V´KS^]#]§pÆ"ez#\x001f\x0015;q¤\æ\x0017é²§ie\x001fo³ï\x0014ÎQ8Q¡TÞ\x0008d\yY¤ßÒûá\x001béì;\x0003\x001a¿¹Wä\x001báì;sô\x000b8)\x0017»·Ñõ\x0010Vãç\x0017\x001e?ßH?ß)ý\x0011\x001cíó8\x0004ÆRKR:'0-ákÄï\x0014/BÙºlÃ\x001d8\x0014¼Ô..T\x001e¾1ý|§é'@JA
¥\x00124Å´2\x000b]ÐÜÞÐw{UN9K?+é\x001d\x001fR»Kæ[øyCs=BßõHÆñeÿ\x0008¯tñÂeéö5·#ôÝ\x000e\x001c1Ä=*ìyDå\x001bBQ\x001eùÊp\x0017ÆªHovÐC/²ì)èÌÙ\x0006~©îì6¦³ÝÂR)\x001fM\x0019º,RRºí\x0017î¦VÛZucþöïorg7eÿnbõ4í¦\x0011\x001bA:\x00198eÜ-ÎëÔß~É¸J\x000eþ#þ¤/ý4%\x0014ç\x0014Å4:/§(rf»_ºò¯Ï·» ôÃÿV¬
¶?¼î\x000f¯1\x001cB¹;;(\x001a_òÝîüÞ0õ6¥qÝR¾¸Uà0Í2÷\x0019+Ï°ninª;)ûE§óùC°é1Ö\x0008N 
Ò,°#à¡_Àkl\x0006Ä\x00073bZÎóåDZµÔÊÕ;©û7\x0013¼¡&QÒÅCJÏO
Ç\x0004Ð\x000bÊÒ|_µ#àU¿WÙÉù3©4»Ôõ"£2\x000f1¤hÐ¾~xþòüx¼È5Õ´ÓEüþ\x0019¬æ\x0011L\x0011Å
×Ëë«5®\x0005V×°z\x0018\x0016¨|©äÚVõ÷f2i ÕÖ¬vUsò£¥\x0005mà\x001euà&ª;Y}ÍêÇXåt\x0002#_\x001a\x001b\x0018ÇM~ñÆ<VªrÂ-\x0015¼ýùùîÓæêáùééîöùïG\x00034S;÷ä¤¬Mæ¥'ç^Ø§ïnÎ.6W7\x001f?Þüé8,Ô°0\x0006ëSc\x0004k<äYZµ¿æ©\x001fVÕ°j\x000cV+"Ä-åw&_âÎîÏ7íÕ5¬\x001eu- ,	\x0003PÕ°®½\x0017¬\x001fÖÔ°f\x000c6Ú&wÖs2àKRòl\x001dX[ÃÚ1X¬ß"Öpâ
'xfÝ[ÔÏêjV7Æ*<ÕìAª@ã>³Ü
Ùý²ý°¾õ÷óá#,ö³=Skö§\x001duÃÖUÖ¶TYwomàÆÂÚEÓvVÝÿ\Û\x0001«ýNÐeÆô«çÇ\x001fnØüô|Ì\x001còÓ\x0018%Væ\x001bÜm ¯.o®ÞÞ¼Ù|}s~\x001c\x0012jHèT\x0002Ñ±/å
èq9
ÝfãýªT\x0003;\x0019h>\x0012øXJÝ®\x0005%¤k\x0019ö×CôAê\x001aR÷C-\x0013¬æQ\x0004Qr³ù°?Ç¦\x000fÒÕn\x0000Ò¼ÌÜaÈòµW8¡f\x000c\x0003_Û\x0013c\x001aÁCí\x00047\x0012Aîµ£º +I[\x000cP
\x001eâãéex[\x0014
aWÁ>ÈV\x0002 ]Î¤\x0002z>PØý)}}Íå#·[ò÷ö!p$\x000f\x0002=àk±¦4ým\x000f\x001fÕ9Õ`¡\x00181.?²¹Úràn\x000bIá;\x000cp\x0012\x001dVzÁí·û(Ë-ûo·\x000cGVbCB[Z¤ó¬¬ý¡.Hhî
ôß\x001bLi24» ú\x001eìÊYË}Ü'\x001aEuªî&Ô7ÇrºDº§àXt1¢ÅA
\ò\x0014ÅUPÃ··­P¿\x001dÑá!·Ð¤øè¥ºcÕ³Æ
ÚÞPéFv\x0014¨¡>ùÞpè)\x001eQî¯ö;ò3aåv#3Y72{ýðôó±fz*\x001dJ.+K"\x0013,¨Ò5ÓLeM¼¾üøî@'½\x00075\x001etâ\x0019à
8ìlËýå¤\x0018³\x0018OÕxªw÷\x001c
añ0ÒX ¸{¥ç¨LJ§k<Ý»{Sbpú¡Ì½d­Vü\x0000§'_çâ\x001aÏô\û/æøÛò+¦LÈKgk:ÛIç\x001d·YsXNGÏ¿$óN¾øÏÅs5ëÝ<Ëå[\x001e¶Ò§Ü&ØN¾
Í¥ó5ï¤Ã>H¼y¼\x0003°{t
lö2\x0017/Ôx¡\x0013ÏJÌe±û4ÅÝ+½ÏÍdaòL¼Ê+M\x0017¸ÛgqìUÞ>þ\x0012·Ïð×É÷¹|­ÒèÕ\x001aÁÓÍÅ«\x0001üuÙe\x0011 §^Nçâ5JCvj
\x001fíWJÁ/ÀÃt\x0003.m\(÷d£5d§ÚÀ3Gíh°Sg~7|¥û8LæÍåkÔìÔ\x001b(Pèù\x001eh(QÛIWöo¿ßÜÁ×è
Ù©8<¶\eéM¥\x0012\x001e\x0008Öºr²iÄ\¼FqÈNÍEy¥\x0006IROä3G>5Ed>_£9d§êB»Àa¦Ï\x000b'wçàvâ5ªCvê\x000e\x000fP*±î\x001c(sÙÄt\x001eþ\¾FwÈNåÆ?¯æT@§Ê`¤é>3ù Q\x001eÐ©<°û=õ\x0004qÚðl\x0003§Kv,\x0003Ë×(\x000fèT\x001e],Bá#£ÙbÉ*¹|­ËÑ«=T¤(¹\x0017ñ¸9qnZ2\x0017¯Q\x001eÐ«<4`¿é¼}<¨6ò\x0015å+Ú\x0006Ð(\x000fèU\x001e8L2ìt8\x000b%we©e
ò^å¡-Wù¤Qt}­á\x001cÏ0	=¯Ñ\x001eÐ«="\x0005o\x001fP\x001eyÄóÜ5",õ Q\x001eÐ«<°ª¶\x0014ÆS\x0011s¾ìÞbáÒ(\x000fèU\x001e'KÛ\x0003Ö½\¢fß.Ãkt\x0007ôêh®p£Åòóú%±k¡îPîP½ºÃZnéÆi\x0010 ´>Xê·©Fw¨^ÝI{ª|Þ@¶A\x0010¡|ÞÇ&¼4¾e\x00177Ó½4\å\x001d\x000cKè\x0011xBG"^\x001bò+§=|ýÓíã§»§Í»\x001f?Ýß\x001eLBàÈU\x001a7H)ä&L÷ýé\x001a¯¿>½º8û¸ywùöâüô8(Ô 0\x0002Þ¡Ü\x0018¥9c§|ñý\x001d©{AU
ªvT\x0014¹zçd\x0017­·×åìÅÔ5¦\x001eÂÔ8×­/*C¦Üð\x0017ð^P[Ú\x0011P)9Æ¡.Ê$Q¥\x0017\x0001Ã\Ó×~SÏ\x0011<Ð\x00158N¸Î\x000f5g\x0018át#ý\x000eû(ð\x000cf÷\x0012[ãÃËV4È&,õ\x000bÜZÉð\x0017VðÝk¡õ6W^Üù><Ð°PµÇ~´ÚÿÜÜi\x001aL3)5\x0007Ú±'Y~ØKg\x0002ízÙ7zK)\x0019]2_\x001fî\x001fèOG0MI×ÆÒE:p³R/÷ç|¼<»¹úH:©jL5©\x0015?\x000c\x0018£¸ÎÝ©RÜ\x0002°?!¯\x000fÓÔf\x0000\x0013ÛåÒ¨\x0004S\x001a9[z^ÃþÇNLWcº\x0001Ì Ù\x001d3XVwÓ\x001eñÄîÏ\x0018ìÃô5¦ïÇ&Û{ÙL*h2\\x0003äRÆÿ¼h¾9þõÐ~R1[t¨a­Ç.Ì\x0004º¿ôj.(¸­;\x0014ýGºC_?ßút÷å\x0008\x001fHÅ}é,Ææûæ±\x000b°W¯}s~qqv}\x001cM×hº\x000b
'P;X\x0003¬ÉGÛ\x00044æÌt\x0001þõQúpÂ²/mÅ~8\x001bÍÖh¶ï{jî)d5 ÄÉßÓ¶÷ÀÍFs5ëBÃ\x0006úª4àÄ§Qº\x000ba~ïl4_£ù.4-øe\x001eû^\x000bBeÈ~\x000fq6Y¨ÉB\x001fæè¶Å1ªªM>¶?ee.Zõ0\x001aÑøat&\x001bfdÍkQ\x0010[i'í]Ø«Òf³ÉMv±a±³,l$xÖ¥túól6hØ M½t©7Ü×Mià.õN.\x0012\x001f²Q\x0007²O\x001f8ÅOÝVè\x0013ª\x00117¶ í\x000fwÎFk®ìºÞñ'5AòÀ\x001få\x000c³ý®òl¶FêÊ.±­Á](\x0006	%?b²0ëùW¡\x0011»²KîbÓ|Ãu\x0001¿n*\x000båfpØ\x0010o	[#weàÅ¶¸ôzbÈ±ÔØx'oÚD»üÙ`Ø]rWa;f¼V*g´òeòÚþ¤¹lÐÈ6èm\x0011tp &³q_´Ð÷÷ÉÍÖÈ6èmJyî»\x0013Ïu\x0008Z\x0017´eæ\x00074¢
ºDÒ\x001eÓÆ\x0010-^L¼®yÛø­Äúel²
Uç#Ç±ê¹\x000bÍµuì×DonÄ¾YÊó\x0010
lÅ
pü÷ëÛ\x0008öåXÅ®t®$¡8Ïn6-9P\x00136Òi\x0004»>X¨\x000bÛq\x0000(>Ì<4[Æq9lBOæ8¥\x0018ê~½0L×dº,ZoÜ8@\x0004vú¥ó¥'þþ:ÌÔd¦\x000c[\x0016R\x001c_:\x000b+CyVwû£e³Ñlf»Ðç¶8$GPQ°cñ\x0016Ìþº³Ñ\æúv­xË.j.²Üd\x0000(ßsÙ®ù\x001aÍ÷íZ{[lmÇ»\x0006üA'Â³ÑB\x0016ún\x0001¿Q[Wü>éEK²¿Xi.lìj/>)vÆ! íË\x0014ÄýZ~.Z#ÔdT3Õ\x0015NI&³
»í±)n\x0016	\Ù5Ù'×9áX¦-¯\x0000¦X»Ë¶­k²S°21ª,»}E½Þß\x0006c6[#=d§ø0<ÖÊR\x001fäËTËýÚ}.ZsEe×\x001d\x0015® )ÍE<ÂqÓ-\x0013Ð\x0000¶\x001e#âêøÃ§Ûïï6?<oÞþúÏ¿þãñö\x0013>ç¿½}>Þ;DJU:wÀ3è¢ü£§È¨?vX?\¾>Û¼¹Ù¼={vuzûoOo\x000ew\x0010m	Í´\x0004ý%_Â{NE
÷»8ø|EtU£«eèâ¥ÀÁYªF³\x0018¥ÜÕ|KÈuM®ÇVÜF_p*\x00006ëÂëkw\x0000}bCæÆ~59v\x0013\À®×t-PtÔqL\x001b÷iÔ»\x0012£\x001f]l¿\x0017ò^\x0018¡_ýúÿ|ùåè,åÈ¨\x001atiÝ@ÑOØbs³yuzýçC®zë\x000eF6èc\x0003E­Bã=s\=+¹\x000fqüc~á\4U£©>4M\x000fÁ 4ð8>ì&ÑÀNdVÏEÓ5îü¢4l\x000cÐ°\x000cåÒQfÌh6©ÑLç\x0007
Ô\x00154\x001a\x001c»±áÌ»Ì<ú%l¶f³Û\x0006dOt{pI\x001e\Sw}RW³¹îÓÑx\x001bËS_Ô¡q¢ýÄ§¹l¾fóûF}Ö òðûËKSE5\x0004<\x0017-Ôh¡\x000fÍIªy*CP\x00025
4b3°LT/0(wE¿àÍÂ-52àóF­hhE3\x001b®\x0011¼²Sòâ4,:pÒ¼H^¶v4ìoH7­\x0011o²S¾á(ÔÜ\x0002,náþXz¿ã7­o²SÀáÜ|à¢¥Eö-\x0018ÅfìDõ\¶F¾ÉN\x0001§xF+¶ô>$K±Ö~Ùehäì\x0013p Ê7ÕBæ\x000eñ\x0013-ýçÂ5\x0002NvJ8m(t\x0004`Ý	»¥Ü^Ûq\x0008sÙ\x001a	'ûD\x001c\x000eOÔÔ
¸@\x0013 FµSÝÞgÂA#â SÄ9ï(!ê}\x0016¾\x0013\x0013æ56/ô\x0019½Ø\x0017\x0014\x0003Î¼ÜÎ\x0013\x000e­\x0018W<\x0017®oÐ)ßBÚ­´qÖs¯¥xòHÙ\x001b31¾d.\s\x0017 ï.`g\x0013Iç-zd$|q\x0019í\x001cLT­Ìþ¬ÍKLþ´¥j`®01¬¼OCö²0ánéÆíOt?Î(Ý»\x0015Å\¼}þeóÕÝã÷?Ý>ÿp,d3¹òùÃ>Ô<Yb15Ùè»qÙ9|{óçÍWgW¯¿>½ys\x001c\x0014jP\x0018\x0001ur
u»¨2[\x00149¬Á\x0019jÎ0Â\x0019år`+´x±ÂKÃ »
>\x0007@ëbõ1@Ê\x0016B\x0012Ý43!¢Õ·Û\x0005jÔÖ\x00117ãÕÃw¯\x001f¸\x0013WÄä|F=zôÄo¸ô?ý·èêòíÙÕæëË7gGcjëFV\x0018b\x0005LýJW>Þ"[º\x0011ò¸ø÷÷µûaU
«\x00067K×ÀãÄ\x0004É\x000fíþpS°~X]Ãê±þ&õù
A\x0006ê2°©þÞpB?¬©aÍØÎjòÆ)æ¥ÃQ\x0008ûÓ´{HÝvr±£äâ×?Ýý|ÿysõL!ÂO·ëÇÛ¿üånsû¼¹xxþËlccqlOÚg¡ Yµ\x0006$5Éªa71õõ×gï6W7\x0014)¼8Ý\_~øp¶9½Ù\\Þ|¨²_äÙÖ`ÅÃÙç\x001fï\x001e\x001fo?ÿËó¿?n©\x0018Î8ÃW\x0011ÊÔ\x0003í8pâUäìýÛ³««Ó÷or¥ÞÍëJ×lë2ÃRb\x00009\x001egÎ>·è\x000eQDa¯\x000f4\x0004¬j`5
\x000c/ó~\x000cVóP6¤åsÿ\x0010²¯ý(rCG$!k}¢\x00089hÎ¨û¹>d½]\x0016©C\x0015^þððùËæíãÃfî¤á%\,ãØ2^ó³#LÌÂ½Ù|¸|½y\x001b\x0005Èû\x0019<z»0R*ÜÜ*
¿à\x0000ºpÆpú©óûñ|T¹ýæ'¡TÅ>|~úÇàÃíó§ÍÛø»cÃªpô\x0013g\x001e\x00058Q¹\x0004ß2~¢IüëË÷\x001f¯ñ\x001c|8½¹Ø¼¿»<8ábûµO\x000c©\x0011hUfçÆm¦\x0007U°8·\x001aí?¾cÐªV\x000bv\x001aJ'h¨S«\x0017.B\x001b½?(6Æ¬kf½Ùq¢¦¶°¤Îköh*ï¯N\x001c65´\x0019æ¥¥¼°Pcòò#ôþDcÐ¶¶\x000bvZajîÒ\x0016H"ÇÓ¡K»ýïÇ }
í\x0017ì´çúj/\x001cÍ(;]fýECÐu9(¡ü!jÅm3¼ÐÜ\x0006ÔÙ³f\x001aè\x0018t#ñä\x0002\x0017¡½¦C\x001d¸\x0011)\x0013U£!ºW¯tRëíðvUÕOÿùïÿqyÿt4ÝE\x0008nj\x001eÖ³¤Kí4øa}ªñÇÅæòüãAû^l;Ï\x0000?}Êºúñîé»_¾Ü=\x001eupLßKû\x000fà\x0016À¥ùÛû,vqõÕÙÇW¾>»:\x0004+¶§ä4%çüç¿Ü>=Ým^Ý=þøùáXÃ¡r/\x0015â´çã`¬g\x001bóüÝÓ\x001fÏ6¯Î®Þ¾¿A¨jBÕM\x0018}9ÅÇTçÖ«¥Ú~7gh>¢Ùö©\x0012(®ïÓøc\x001f[{Jàxþ8TRÆ3bÌgê¹ìêæ<¾8t×·#:RÕòËYÿ0»4<pÍµÀb&*
ç\x0004@¹wÈP:g\x001f·ª[¿¿ýáöéK¼\x000cümhUC«qh­PÓî\x0016\x001a½âÐ¦6ãÐÖð´´TX\x0004\6^Ü\x00157ÚÕÌn9pÒ\x0012;Ç%äÅ=Þç	 7Q\x0014ÜfA%ÚcÔ| SC·Ì,JAùÞFP½Ð°Ýã\x001aRëÓ¿Ý}~æ\x0019jooéèV\x0002\x0017ùz\x001c¡
</IÝ~ª§ß½¿áùioO£N8JikJ;B)°]_¢ÄÒò@eÀzØ1\x0007\x0006(}Mé\x0007(åö\x0011^XJÊ\x0005¥xÒµ°»\x0015\x0003¡Æ\x000c\x0003Nca¥ÖæÔHMyÎBÙÓÃ´².\x0006Î]ûwSòÔz\x0017$wkT¥ùÎîÈ\x0001Jh(aR"ùhAawÎD©ùý\x0004[I¬À©\x001bNÝÏ\x001d¶¨óuæ_Gß¶4gØ3\¡s;(
¦~½Máºç\x001fîó\x0010â1sO
Æ\x0001ç7«í°¹\x0013»;JÆËÛ\x0014«»¸¼ys~vu\x001cÖÔ°f\x00086^\x001bò¾\x0001[r#\x0002àçg?Qîß\x000fkkX;¶³À½Ç\x0001Ãã¹Ã£ÂÉ¹´³°+FÇ`}
ë\x0007a\x0005?[Ìmõ\x0004ËÃ'½Lè
5l\x0018ÕÂÁ%ÑÑ¢\x001cWÃµ?Z¸ý-Íºak±jê\x000c¿®­U"¿9EU`é!§3x\x001cõµ
¬l`åØÖª4\x0000ÈÒ42ÊÄJiDù½o¢?O?m#»ä ðÊ
í<\x0000]\x0017¶\x0008Ì{;QiÕO«\x001aZ5¶·Ñ
&ï­Ñ\\x001eiµà½u»5$c´º¡Õc{k}
e\x0003!4XNßSåJA6Ai\x0006\x001còì(\x0003@(ö¶¬£D8
\x0013#è»a\x001bÅ \x00075Oõõ9·"pû\x0015Ã3ÿT°\x0013Ï»i]CëhÐ¤ÇÒ¸dri AÜ÷ÉzNÖFÉA5\x0016\ÙY
eg
¿) =¶
-4\x0001\x00065ã¸F\x001aaG³´¤þ\x001e:úõëì-´â °
ÜÅ\x0005\x0008@l\x000cy\x0008QMÌÚèm¤\x0017I/-J¶s´¶Y3\x0018+ÖìoëÒOÛ\x0008\x0004\x0018\x0013\x0008)w\x000c\x001ak9Àe<Ob\x0013û'÷Ã6w\x000cÆîöÎw,xË6#.\x0013cãºYUsÃÔØ
ÃôÞ¬Ä\x0000ÇeÿVñ K¹'­f¶¹ajìi\x000fe<±7\x0004\x0014X1¾&úaôÐn¿\x001a@z5hòTÀ½Åÿ¹ÂÖ¨Gó\x0012\x001cÒeo7z\x000cXF*BpxÖÉ]lÌ]:OÙK*âÞâÿ¤>©g×ÇW ê\x0015¨Å+ÀR¡\x001cWÐ§KFæ¸}\x000bìÞÀñ%èí,\x000b
Õ«Ã»ÛÇ_ÿñýOq\x0019oî>Ý~ÿ Æ\x001d®oîü|$ùFY«K\x0013å`¨-\x0002\x0018É\x0016±ÐaêÀ¿Kyd\x0017§××W)
q}úñãùÛ÷>¾\x0010¨\x0017\x0002ë,\x0004Cz\x0005×G'A)¸¬l\x0018_ª\x0017¢Vú"ç;K\x001cxûµ)\x0011«ÁÖ¡ëuèuÖáà&n\x0001ß`iVâ\x001a\x001d¹[½x\x001d¶^]é{DZ\x001a*\x0015
Z¾!/>£ðF×øBB½°Ö\x0007\x0007¢ôQqPüÛjö"äþ\x0017¦¡|\x0017½êo£§V¼öWØ=ýõ\x001f/¢ýp÷åþËÓæôùó±\x000eÑË
ô¯\x0014¶ù Â ¬jIJNÛÝH\x0013JÔ\x000fg×ç×\x001f7§7ïÏ¦\x001fj"§mDRä´(.n7\x001f\x001eoï\x001fïã\x000eÿç¿ÿÇ×÷OÇÒ"â\x000f\x001d7z&ÕY¡RÀó6;7÷âtóáêôüê<nëæëó+üÙ~V<\x0017ªAôÀÃót\x0010âñ¸{BÕ¥\x0012ò?Ýß=ÿ\x001d\x0011ezYL©-\x00060Ó4þOÈcqmÔ»ì}uq~vó§?^]Þ\§/þîôêìãT&`Å\x00065\x001bt²ÉH\x0017ÙBÌØ¨O~Ã´ÛEpªSÝ\x001bg3²ø}ó.,Ü7S£>´hB\x0005ú¦ºe&6§Xì#dÁÙ\x001aÎvÂ¹\\x001b:\x001fä*yã8£sÍÕl®-óT\x0005¢­q)BØ\x000cTà¦\x000c£l¡f\x000b}l@Ïk-Ò\x0018bS¹»s\x0013Ü9v\x0010N¶R¤SDß(UyD:\x0000´»\x0012¦ê[vâdsSeçUU2÷¯\x0001Ï\x001dÁå,âH§åèw\x0015~K\x0000\x000bß\x0008àW¿þãËO·ñz~<\x0018½ÈlSh'Eôáò×õ¾.à4¯ý¯Î®¿>}ÿúòæj\x0006§®9õ\x0000§Ñ¹WF\x0012{\dÉ¢£D.ùã0MiF¶ÓüÊµÕ\x0001½´!;\x0016Ääeéâ´5§\x001dÙN\x0015r+ÆÈiý¤\x0016¼¥>r\x0011§¯9ý\x0010'äÑ\x0010Ó{|ÛÏ17Iû)ÝrLz+ã[$F8!«dó\x0003h3uN>\x001dEÐPÂ\x0008¥,»9<@¶\x0003äR­\x0008jÃ]3\x000f´IøË?hÒëÛç\x001f>\x001fDLó\x0018ó÷©]]$´\x0011PÓ¹Ôvâ\¾>½ywù~\x0006\x001dÔtÐI\x00076±D\x000cïHOGS'½Ñ04\x0013×{6ªñT'
9E2î\x0016¤o,8Ö7ÁMÃÙtº¦Ótør(éÛjLOtÆ\x0019þ¶S§o6©ñL'§Ä\x0017T1õj	/X6ú½Ð³ñlg{ñ,û$N[ÆS\x0002x÷Ð³ñ\çzñ(\x0019\x0007\x0015Â7×gXïÁ±§O\æk4ßEà¼sñHÚ9\x0015BÑu\x0013JdöÎ½ô~(R/µ~è\x0012|*×Aá÷õÑ\x001f+\x0011åµKß6¥í§tçãDJê«\x0013¥\x0007vÛ­°·gPn´²5i_ÿtûBKÓúÍé\x0012S\x0008ù\x0004F×e³2S÷÷ëÓ÷S\x0015\x0015\x0019ÔdÐEfE(\x0011\x0005\\x0019îEöº½3áT
§ú¶-@.TÀm3¬t±ðw\x000e¦>êL8]Ãé¾Ã±=\x0014&"&£\x0005ÁBYNª´h¦F3}h`ùÊ&kN\x0017|ea*¤0\x0017ÎÖp¶\x000f\x000e[KóÆ¥7Zªè2¢~\x0014.Ôp¡\x000b\x000e\x0015¬¤\x0013g ØQFûá2\x0005æÁÉVô\x0011ç
Z'\x000e¥²$]ÆßÕ{³®¹¬²ï¶zyÚEc|%á+áÝ¤
:®¹\x0012²ïNÄÿú%:ì¿\x001c6«¡D¬\x0018¥ÓÛö»VõÝÃó§ûÏ\x0007?kP¹¬%ê®\x0006ø¥\x0010ÈF\x0001³%KèÉáòæâ|ª:°\x0002S5ê\x0001JÕ[\x0016*\x001bÆ¾¸ef[©öé\x001aL÷aö\x001c¿(ñu¶ñ'¢¿¨¸¨>áåb®záz}ÿóÝû_ÿoJU?\x0010\x0006§a9ñk4±!ÇÁ\x0005û:Ê}p¯Ïß]O\x0017(V|PóA/ðù	\x0006¥kj¢¾²ÅU\x001cÆÓÛÛW÷N~ýú¸|¼ýþ zp/î\x0004N¡ÏÚ¡\x0008`÷ß×7©cËÇÓ×ÇùTÍ§zù¢BõìîH|-LÖJvw¶c*3\x0001Õ·÷?ýýö\x000bG*^Êx6o?ýòý}~\x0006Ô.s)äºÿôé?|¼½ÿüå\x000f_=¢q$FP¬6o4 \x0012!DÞü\x001a\x001b7ÏßùÅÅ#ÐùûëÍWWh\x0002ç¢Þ·\x0017~}þ~rÖ{C\x001a\x001f\x000cêIMv\x001d#©ÊG\x0011\x0018Ë5QãwQã9± \x0003Ód\x0001\x001d\x0004ðl®U8£ìÒãùË\x001b\x00109_^Ó~FÓ­È\x0019å\x0019æV ªcDÅþm2£R7¢\x001a\x0016C« F\x0013Õ¢¦©µ!£\x001aµ ÎÇ²¼«EÒ*¨ñ\x000b¹á]u*M\x000bBTL\x0004\x0008yW³3\x0017Iíª¤Ñ1ôÃJï\x0011H£YóQõÆó*¡éUP£\x0018	ãGÕ'¨Þe«\x001bjÙU·æ­Â(©éßV÷ÂªÓ¤Ï´­Z½lë\x0012\x0015Ý\x00179®§lz9KÛªhO\x0015o)W\x0018¯\x0019³\x001cVRX¹khGSëÓ¼£¹\x0013\x0001îhXóëÇC/\x0017()¼×$T¡èS#C\x0011ªknkTRrXQáÔRKRÕR*K:(uEÒøïãªJ$\x000cIqz.Ëoø\x0004
óUX£\x000btç]µB±¬J3t3«÷+U|ããÊJé\x0014ÝCVåÊiå\x0003\x0010m?»"jÔTrX[á^^¦>RçmÍ!ÜÈ*ÄÛ¥/0¬\x0002¬tXöX!`»¤Ä\x001aç}\x0015UüwÁ¸\x0003 òàEdÕ®¸*ôî\x0013\x000fýW\x000bë^`e-_¬\x0018~`¯¤@(]ÊÆQáIüMý­v\x0000stëêöééy*~ýhí"%\x000eXËÚ3¥öÊ*\x0007»®N?~u5ä÷õ\x0003â'Ï|Ò#*\x0002\x001a\x0011H@E[zr\x001b;	Éê'ô2Õz¼öiÚqBt$Ð;]\x0007,ý~@[¾±P\x001e½\x0012 ôã\x0002&ox'"øÝ:ºÉ>Éö¨ç\x0003»wñëÍ\x000cN¯H¦}7¢\x0011y\x0012¸G£Yâ\x000ciDÄdê(Í´
ÚXLú~FT6:1¢$3ÙaØ512"o1#òýXÜdx¤uXUôÈ\x0013å°ëÑZlÆ÷#F[3ÇEâ\x001d\x0013Ò&×a\x0013`ÔÞs\x0010?ýàôµØ¾Ãçê¿=Ü?¥0v×VÚü
e\x0002H-Ü¤Ø>ÃÇëo.Ï?N\x0006¶\x001b@\x0012ÛÝÒ¤¹@\x0008\x0008>ÍÄDBÐ¤©U\x0010fÒ±ø÷ÿº·ÛÒë6®E_¥_ =ÂÿÈUj­Á¿Ý$5ìÜh´¨¶Õ{S¤Üd;v®ò\x001a¹Ý7'\x0019çö¼Þ$OrP\x000bUøZøÖ\x0002@ÇJljRö,, f¡P5ë¯7?jsû|8{z\x0013QÞoÃB¢\x000bD\x001dPÇhñÛ.þ3)H3Ê·ojoÎ^D×[0\x0016YÏ\x0018 ¼\x000e.\x0006j*\x0014N\x0006Û¼øì\x0001Yä;wTI¼\x0012AZéî\x0005¤NCE±Þ4c= dçNÇFÄ\x001dÉ;\x0010Å\x0018\x0003Ð¼?ì\x0001Yd:÷æÒ8½Ò\x0012HïÈõh\x0005«Þq/È"Ç¹\x0013$>¹$÷(\x0002ÕÜÂóJªy»Ènî\x0004éÓÜ\x0014\É\x0010RM\x0003ö.¦zEwpÄæ>^zºÒ\x001a\x001cÜnÓÁÖ\x000bAä´,R;W2H&l\x0011ï4:ÐJ¦õ¸'^]v¬\x0012{rQ¢M(
j:,(i&\x001d¢´Í+÷\x001eeÒm'J\x0011\x0016§Å	TÌ(\x0016cL¾~áÚ²LbíD\x0019é\x0010x[
Ê`Å\x000bZË\x0018\6¯Ù»ñ»O·÷Èø\x001f=»ÓPºÕÄàö\¤Í)h¦^üì¹±\x0013ªzø×lMâI!sÑ¡»¿Ks7Df¥»¼^T+\x0014C"KT}\x0001sÔ2\x0017]ºë«õ)Ð%àâ4u"Æ+Oº{c\x0018"u¼e$À&×ÂÎ\x0002|8X}EP(H¸ ¶ù¦+\x001dg3Âì\x0015>±NÀö\x0000ØèÔµ\x0014\x0001+ãOæ_ú\x0000Gûi¾aç\x0000µÈÿ-{/\x001e ½å-a\x001aÉÂ\x000eÀø\x0000\x0001C{øï\x00028µ²8ýà0.Áþæáþnë¾P²^Þå<§\x0008t5qëïò4À|ÁüÍë«
¡\x000c\x0003cPí	³ÇôwÂL\x0004\x001c1¯&<{@ç\x0012ð\x000c\x001cÐ\x001d³ @Ø\x0015Z.Ø]\x001a)Ø×bíÐÃÿùøãÏ+¤è¿¼û·m©	oc0&\x0017¤\x000e'¶.ÛÙ`÷D\x0002ªXu\x0018EKæÕ¿üú\x0014¿~®=\x0008\x001djÙ\x0010\x0016\x0005¨\x0005¢ö êÕ\x001bÌ\x001et\x000fì[Ã$\x0007\x0008¦,Y\Dº	:\x001dVo\x0006»\x0010.[4¢¬z\x0013ö-¥]\x0006T#P³ú\\x001aIÛR;µê¼N"õ\x0002îÂ\x000c
É÷<¾ÿp÷×³G·ïþrón\x001bÌ <¥Ëð+Ó#¢	|
¬$àóøúÅÕïÏ\x001e]>ýöâi\x001bj::ýP0á\x0002\x0015\x000fzZÑ isbËÏÚùÙ
5¡\x0001¨zQ\x0000G¨¨A«ÊkjÄ´5MGi\x0000¨¤Ü½Õ8hÃÑò{·\x0003¿vâwCM\x0001¨}ÿ\x0008U\x0005KyfÑLP^;ú»¡¦ôJ?T,ØOO(¤'\x0008ªãçn'V»wCMIó\x001fÄË\x0006ðøHBçX§V¯»¡¦TËÀª\x0002G\x001a[7hQù
ÇÅûâ,¤)ß2°U
?\x001f«tqLÇ\x000b\x001eãê®S{¡ò{Ó\x0010Vz\x0001UZ¤?<V±\x001a=k\x0003ðvÈ\x0005Èt®b¬DÙ,ôVt!°°0Ø\x001e \x0006°&\x0001¶\x0015ü2<í\x0001IleÅ¼=@Wï¡= k\x0005¼z3³òC½ña-Þ
É°Ry\x000e \x001c\x0007S« \x001a0võÚ½\x001b+e\x0008ØÕ&vxKq¼®ü¤;ñhQ%Ù\x0008Ô3\x001e1ÅQbxG\x0004ÊÈºúà9bø\x0014ÄXó÷«Õ\x0006»±R\x001dÙ\x0000VG¹X+­@íú\x0005«ðÀ9­Õ\x0017¡ÝX)94°\x0001\x0002óÄ±³ì¯4uh7\x000b*¼
\x0005\x0002TI&õÒñ"\x0001N»ÉY§\x0013X\x0003Ñ\x0015\x000e)Jß_%Õ*\x000c®ø\é°ÀÚ
jó\x0006 ªüýý¢|º`5.«yX#À\x0010_a;¶"eé\x0011\x0013±:öWjÚf¥:Â\x0001¬°4|"V\x0010©é~Áª\x0003ì¬8\x0000»h`¯\x0014pn<÷8\x001a"aåú÷È­³â\x0000|¯!ÂÂI\x001b	ª¨¬ zÞ®ë\x000f»¡Fº±;Î¡`\x0000ÊPF¬ì±¬\x0014Ó°Æ}\x000fC¬ì±ÉFt²¬&Æ²ë­:»¡Fa±]´\x0014KÈ7xÌø5-uòéj²"VKësè\x00033\x0001e\x0004¬±¨õo?|ÿýû2Íöááþ#äÞÜm¬{\x00168\x001f,9Ö\x0018Q£¤÷ò¤Eò×2ÞµÍ*Ì\x00178\x0008p\x0011Ç½¾¸zõ+\x0010ÿxûQ}ÿ¶È¯<½={üîÃ§Ûmk\x00184|YUR¥®\x0005ZA\x0017Ùtík?½<{üôÅëË_[·Óù×?ÿkI}uûþ\x0013¿Bü\x000egË§_>þñæçÛ­\x000fW1îTËi
P?æHW³*¯.¿æGßáÔùôËÇO.^âÖ¯\x0011Uý\x0018!\x0016m¥ø=ÿéç[@âNu´\x0005,·\x0015\x0002':&ÝØ\x0002Kñ{\x0004ûìåzé{\x0006ìKÀ¾\x00170Î(HÞ5à¨(S?ÍGÀë.k'`Òè#ÀKÚ¥\x00171µná\x0012ÓK7Bí²Ä«¡ÖVÄ\x0001Þ4m\x001eÍûòáO·Rû{Dvöòîöþ~ãcÒ*³¬\x0017q6¶áL\x0013ný
ëÍåÙË7__¾N­ñø\x001b/¯.¯WE\x0006
# 4\x0002
¸qÒ\x001bIi¤¸Å©ÇE×ªÜê4BF¨q#p¨o8\x0018!©H×lÄ|\x001bti`\x0003p`äQ\x001eªj´cºY\x0006l0¥
f
)Ó\x001bAµvùgè;4KS;°¥\x0011v\x0011a~^>D@¥åd\x0004½­D#¾Änr¥\x0011nÜ\x0008³-hæ\x001a-õz«L¿\x0011¾4ÂO0b©ÁNFxnH\x0002«óhv\x001fv\x001a\x0011J#Â¸\x0011Öp\x000c\x0012¯Ô?àÊÇzþ5ÓStKë\x0003o'vNAÊ¼¾\x0015\x0015ÕÉ	\ç\x001c\x0005Í^ë$\x0000F\x00186BØù|-+ª\x0013¸Î\x0003µoîIÑ`õ/t²eEvr\x0002Ûa/
û'`¦P4Ô\x0018¿ES±£Óîä\x0004¾\x000bx Ù\x0008º\x001e(PoCåcå\x0004'\x001b<«&yz6l\x0004ÇN¢Ù©ÑiEådå¸\x0001++*yl¯O\x000e
ç"S,ÞÖ*è³\x0002Di\x0005w®XaSÒÙ\x0003\x0017þÇ\x001buë9±þð8`BÅ\x00140Î\x0014`Â9=yH\x0007B\x000b\x0007ü\x0015âF&Ô7¢qP2pØsÏBò°:Ð«\x0013ö\x000bD±Pñ\x0004óD\x000c1ò^"	M³
½4ê "	\x0018'	\x0015ï¦ô¼\x0017l­©gÞóhw\x0015uZQ\x0004ÄÿH\x0000ªû\x0004_(þg¬¨h\x0002ÆiBKuN,!\x0004Õ¡X¦ä=ó`\x000bqu\x0012³NßÜÞ¼/òª\x0011æÖ\x0002o'ó\x0008<U'`Ë¾Ýäa¿¹¼x^äSãïn0\x0000J\x0003`Ô YÃÁåNA+\x001dß®ãÝ¥\x0015nt\x0019 J\x0003Ôð\x0017ÐüÞÂ¿ù\x000bpÂLxÛ¿»\x000c0¥\x0001f\x0001ìU¥MêûhÎ\x0006Èé[È\x0006ØQ\x0003âÝt©¼TQ}RO±k¥Êº\x000cp¥\x0001nø\x000b\x0018jGó\x0012Îy\x0003ÌjMí.ø¾ï×_â<á\x0014\x001fe	CÉï¢qýEËv\x0019\x0010J\x0003ÂðúÛEN|Ù@\x0013µ\x001ci»Õêé^\x0003\x000e¯%\x000b\x000b	 \x0000B\x0002|\x0002øâ)ÖË»
¨ilÇì2L{ù\x00044mù\x0004Ìc6Ìö¢²â19Ld^,³xo 9 BÍ|² OGgAEdrÉ\x000cW\x0010£\x0012{`?Ä_`:
\x0014Y$Ä¯ñ\x0007Ö§E%TúfQÀ¿~
*"ÃLæ\x00023\x0019*»s0d9­*Ú\x001a]\x0016TL&Ç©LÓ\x0011È²Ë1\x0014Rù\x0008L?Ä\x0015Éq*\x0013ç´RÎ°ãõ_­Gë6 b29LeÆóË'Î§ç[@¯Öö\x001a\x0000\x0015Á8å@g\x0008½Í)/ÕÃí_ñ\x0018ó¢þfç\x0004'ã¥|\x0002)à.\x0003êëØ8i.ÆrFñ\x001bÌ\x000fñ\x001fþ	*\x001aa\x001a3\x0007\x001a¿ähN\x001döÐôOPñ\x0018\x000có7¤ø²\x000c\x001aË^(05Äîz-¨n0~¥tü&^s¤9ì¡ÙD\x000c\x0015\x0011Ã0\x0011Ç{\x000cõÍ;eò)pù\x0014æì.\x000b*"q"\x000eÙÂaÖ\x001cG\x0012Mi£.ü\x0015\x0013Ã8\x0013{\x0016A\x0003\x0014yRq[P¨Ëa½àJ*\x001c\x001dï\x0003]'°\x0013¿ªX
3q9\x0018U¶8\x0003ü\x0005Äº e¯\x0005\x0015\x0019«a2÷0zõp*|\x001f^ù\x0014ËÎO\x0005\x0015\x001b«ñì(ð3¦Sâð
\x0002\x001fc±ZØÛmA\x001d\x001dfc_X ©Û¿\x000céÄôäªèX
ÓqpÙ\x0002Tâ"\x000b¼¡\x0006Ð°®ªÑk@ÅÆj±¶\x000f²Ìll]ÞDfúA®èXÒ±\x0014«CÌjþXOÀO'\x0003UÑ±\x001a¦c5Ò\x001cJ	hé\x000eÄjC·\x0005\x0015!«QBBq=ª\x0013þ Fûø
Öõoz-¨\x0008Y\x0013²Cuëô
\x000eQi\x0016I\x0008ÁÏ\x000eKuEÉz¥4,E\x0015ÿÍO5EãÑ°Ù\x0016T¬Ç)9°¤N\w\x000eæM4ÿ¹RW¬G\x0019YJ`WrKt×aWä]\x0016T¬G\x0019Y
Ê\x0000i\x00134\x0008\x001céé¼Ö%é{-¨\x0018Y2²\·¹\x0018@Õý2\x000fLÁöÉ\x0006T¬G\x0019Y
G\x0004oøA³'²ó=QÅÈz\x0001°µx±ÀÜ&Â\x00136æ|­.\x000b*FÖ£,¥äG?ë²\?<rÅØé\x0016T¬\x0019\x0019\x000c¿8á \x0016\x001aÆ\x0003pÄ\x0012f_\x000etÅÈz%8îRµúàL!;Sh\x0016àôX`*F6ÃÁ\x001c}\x0002M
ìÑ\x0000\x0016\x0006\x0008º©ÒÛe@EÈfe¼Q}¦7LÊ\x0002ÇK\x0016ÈÕ\x000eÁn\x000b*F6Ã\x001dk)cmå\x0001j x(iPëC#z-¨\x0018Ù\x000c32ÊRó¤*ÃeháObú
ÓÔ\x0015DÃ|¦<'ZâÅ83²æÞ V5'º-¨øÌ\x000cóY¼V\x001a\x001aj\x0015Ô!¬ãaG¡]ÎØ\x0017ÖUR¯)´[$5Ç²\x0015æ¼¸¥î²ç¹w_à¦Ýgv¸q;ðÐ[2\x000es5?H\x000e0Ö%B{ä±!rÂ÷°YîÎÇK§£'M_\x0004ýîê®Ôå~lPåÐñô\x0003,/½øËíûeÎÛÙã\x001fù¿no\x001eþéõX"»qfPÐf `I\x0017¹W§´PY§i-Nºøöòù2ò
;²__^¼9{ý\x0004d×'\x0008e+ ´\x0002Æ­°Þó\x0012¹u0p¸t1ß\x0008U\x001a¡&|
o8d(G\x0008éS`Yjµ\x0013uÀ
]Z¡'X\x0011¯\x000eö ¦DûIò´\x0000#WP
\x0018aJ#Ì¨\x0011½c\x001c{K°Tsêtf<mü\x0017ØP®´ÂM°Bg½@)\x0002UÝ9íUúõ8\x0016¡´"L°\x0002g=§³-pþÄb\x0001ÇBr`×<ì\x0011\x0015W$W?\x0018>\x001c1¥ò\x0017\x001c«\x0014\x001c±Ûj%ç·=6\x0006¦\x0018ãâ¢!¼*Þ\x0002Í0\x0001Þ^V¯æÊÖùUö»\x0011¶n®¸?X´¿ï²`Í«·÷·[ó½ÐR4Þ¹@%µz\x0011yGìµW/×¯²HÍ«7¯/[âù\x00198À¡\x001f¸\x000bAÒuÈ\x0007gIùI[Gé½ `5¯Ñ\x0005\ÀÕÈ\x001b~­õXÆOÀ¥G\x001eòö3ë\x0012¸\x001e\x0001.\x000c]ß\x0016Åx
iÅ\x00039 \x001f\x0019oU|¹\x0007¸)Ñ=îÓ§xB;Sð¨w6\x0013·-qÛ\x0011Ü\x0016è\x0011Á»`I:R;Gûq§¬&\x001f»»\x0012¸\x001b\x0001-Ñ\x0018Ô9Z+Ë;E¬ëóö\x0000÷%p?t6]\x0006.\x0005Í\x0018gÓYZñ¸ø3\x0012x\x0018\x0001\x000e\x0001ã®\x0010yÅ|EWÕ¤:pç®D?bhÅYÂÈû$\x0015a{¿ZÙ\x0005»fÍ!Úx[¤â\^oIW\x0014t)37¬hS\x000eðæB?@¾ÐRâD;Ö¡ÎpêF©XS\x000eÑ&f®hÅQ~hSÐä\x000f<\x0013xÅr6ñòAìÕY´U\x000cðVÁ÷ÿÈ+ÚC¼),IÁú 5uÓGÂ÷Ü­¶Êt!¯S1§¡vaôØç\x0018ßññ¬´*\x000eÜ¼bN9@\x000eg¦ÜÇ"\x0019fqhë={òø)f"¯¨S\x000eqg0T~å±
1\x0015mèèÔÙ³ÈÕKv\x0017ò;å\x0000yÆ5\x0007æ CE\x001c]%\x0008y\x0010«ô=À¡b!\x0018`!\x0017|ö\x0001G¶Ñ\x0001µô,\x0017ï@S7\x000bTÞ\x001c\x0006¼y\Ú\x001aÈ\x000bò\x0000y[ÉK®WS|]È+§\x0008\x0003NÑar2eXã¾\x0008Tq\x001eçÍbVÕ´z«Ê)ª\x0001§èp µ#×\x0012X\x0007\x000c+^óUÉË®à¶L\x001dQ\x00020·!±Ë\x0008<#ÂÊ£þ3ø~\x0008¿RÐÛÇ0Úó^E¼ãM¹Æ]©^Hâ\x0017æ¡Ì·\x001fÏ|¸ÿtûþãÝÍF©ÚHø\x0018n-é-ÇM"Ø\x001aBÙ-ß\x001e&|ùêìÉë×Ï_]]´äu	5¨¡\x001fµ3´[¬

Qc´È£,âymÎ\x0015ÞZ¨Õ\x0000êèR(/ªð^Ak
\}Úw\x0013aë\x0012¶\x001e­-	Â©HIP;~ÙÇ§ý¨MÚ\x000c kBT¤ÏtsBq¡¬õÍñ½°m	Û,v8\x000f*ïäGP>\x00032ìæÐù°]	Û
À\x0006à>\x001b\mGDsÊßúö÷°}	Ûø\x0011¾JXGR£Ú
H×TÏÜ\x000b;°ÃÈ&1\ÆN;ÿsy¬rM\x0007êB\x0013\x001d©F¬vÈSó,¤ºéè\x0013ó\ùí]3ä\x0000Eb÷§Ë¨ùDúìµÛÅÒ{aW\x0014)G8ÒjÖèUW8\x0011xªµ­¬½°+#$i\x00183Ökíò\E7sT\x000c)G(Ò)\x0003§¢\x001fê8óÐÂv\x0019ñ^Ð\x0015AÊ\x0011ÔC¿\x0008TÏ¶jL³7r/î!å\x0008E\x0006D*MeÛ8\x0005që\#+#\x001ci\x0015¬)} ÉÆ4\x001bÀöâ®8R\x000e$>dJÞÜÀDêìHÚUl{qW$)GX2:@Ç¸Õa½¹G$Ë¸¡¢I\x0018 I¢äý\x001d×;½S¹,Æë=ÑsCÅ0ÂÖ²äRc@)ò@T½úlÒ»¾K\x000e\x0010%Ê¥ô\x001b
j^oÏ±«iösíÅ]1%0¥Ê"×
t¹-ÉÚvÍø^Ü\x0015YÂ\x0000Yúx
fÜÊQ#l\ï\Ç¨ýÌõ®ø\x0012FøR	®\TØLëmò\x001dGOõ'\x0015_Â\x0000_zasp¢ÔÁ\Ád&æx âK\x0018áK\x0005<³D¤Ì}\oÅþ[5\x0015
÷â®ø\x0012øÒ{+ÆÒ+l\oÇ¸}{aWt	#tÚê\x0017ØÒp5¨0ùÓÔØ	[U¬£FX\x0007ÇoRM4÷¡V$/6¬&{`×©À!çÍ5\x001d\x0011·Íuþ"îDU>P
Ý\x0019\x0014çy hÂ¼IÚ\x0013öâ®|\x001añ%:ä]âIÔÏ	Çód-4çAì]I5r&ÍÁuG\x0017\x0018ïÃyZçÌl ®\x000e¥\x001e
\x0005ÕÁu+ÔÆN¡·É¡ISp/îêTêSéÄa½5oâ\x000cL9Í\x001b[qK-ëG\x001cl\x001cÀåþðÝ<|¿µ@ÙK»£\x0007L\x0010.ÝÅ¯{À\x0017oÒÓÓ³7Z5Ö\x000c\x0018JÀÐ	\x0018'Ð¦Ö	/N	¯R|
öv=ÜÞWxu/^¬HJ÷\x0003®ðKô¼Àf=o¹\x0017°-\x0001Û.À~\x0007[\x0019chÓÜuæõºÞÒ^¼¾Äë{ñâ\x001b\x001e-°
\x00176\x0007¼°Þ\x0002¾\x0013o¡X'Nt\x00026ù6\x001d\x0014Õª¹\x0018DSïó«3´wÃ5\x0015\Ó»¾Fps±\x001e×##^Ü\x0010³\x000e\!Ä]ïú¢6\x0006Ð\x0010\x001c\x001c\x0019O2Ô8£`õ¦µ\x0017q¨\x0010^Äñ¤\x001d¡Ù\x0003[ÃJ\x0018ÎOÛÀPQ\x0006ôq\x0006\x0008\x0010O¶\x001eÛ§\x0010±ãuÄ>2 ¦>Î\x0000/\x0018$¹£-Ps¶C%\x001eBÜÈUïE¬*Äªw\x000f\x0001¾Ö\¾å¢\x0017æM¡Ý4Ä\x0015ÍA\x001fÏÅ5v*#vZÐbY#çÖKAö\x0002®h\x000ezyN\x0005Ë\x001a\x0007¾%O\x001c,G.¬¿ÌíE\96èulJsè»8ÉµDïà¾À.®ü\x001aôú5|Ì§àR{	Ë\x0012k\x001a\x001bS\x0002fqª\êumZ\x001a,ÃNÜ¡8û\x0012H£®5}7àÊµ©^×¦Qñ?­0ó²'¼kÌ{b]vb/àÊO¨^?¡ã±£wC-\x0003%¼\x0014À\x0002Ö\x0005Î÷"®\x001cêu\x0014&Ò¥z1¿H\x0019,%\x000bcØ°:}7âÊQ¨^G¡\x0015`}Ø²!P\x0017Rçx\x0016ÞÊO¨>?.üÄÏ6^ÉO ¸.i§¬?ýl\x0006ìÜÑ¥9Rié%^}øé§Ûw7ï7ÞõuS\x000c¤4æV8\x0007kºj\x0001þä¹{õâÙ³Ë§\x0017Ï[W}B
%jèG­¢\x0017Nu¾ñÆÌ·çx/¥\x000c
îôÖØ\x0001[°U?l5!-¶ÉC)·VÛL]m]ÂÖ\x0003{$ÆA\x000c\x001b¸×Ñ¢\x0014ÁV§#\x001d°m	Û\x000eÀ\x000e"X\x000blÕ~<À>\x001dßý½¶:p`6g
\x001fr¿ý6Ì¸óü*ð¬B&\x000fs1\x00034Soo¸Éþ4^(ñB\x001f^\x001f@å\x0011Ãjqw&Ä»\x0014uÍüæ\x000e°ª\x0004«z\x0017\x0017\x0016õù\x00046Ë \x000bïó\x000cÛæ\§=xuW÷â>ª`ùÍ$±
>OÒnìÀkJ¼¦{}EÞ§\x001cÈÄõåéºR4§ÇíÁkK¼¶û°9ÎÏãú\x001a2%yR\x0014í\x0012\x001dx]×õâÀ%H¸¾4å^ØÃ~h?;íÀëK¼¾{}5ðàú\x0006rfg0Éõ¶ÐxsF39_Ñ\x000b8z\x0005ËSß\x000f#0µ@\x001aý{\x0000×lÑI\x0017>n	ìü\4â¢\x001dlÌ#Wu»\x0006z\x0007à.d'_`»\x001e7x
·"(É+l&\x001d9YQìä¸Â!Ï¿ñ±£\x0015>ÈNã8Yqì&
È\x0002ûË
;rÂT6s+Ò¬á½\x000fçô`­£K^È ×#âh+ÊÝ!Yh\x0005_¨6;ú`9®ý6º\x0003pÅ\x0019²4¼76\x000bz*Ô2G\x0002Ç ¾9Ài\x000fÞ3d7iàp\x0002^`.À±\x0002%yg¹´P\x0001\x000e½\x000b\x001cOY ÑZ\x001c*âÒ
+oýÍñ@;\x0000CÅrÐÉr\x001eûïÍ[ØÒ\x0002Ë\x001cE´»\x000bvà­¯\x0018Ýwè\x0015x,7Fl´#¸Ñ'\x0002\x000e¶0T.\x0018:]°\x000fF¨D\x0004lI,Í\x0004¯åtÀSN§µ\x0011\x0015VäÀ²Ý\x0000¶\x0003på$ ÓIDÀÀ\x001a¿\x0018Y&©k\x0013L8Dî\x0000«êÌ©î3\x0017ïÉ&ð=ù\Jº*;¯Ê®rª:tªûÐ\x001dêi<«"À*\x000fMõá=«C§º\x000fÈu÷\x001e\x0013\x001c¨iNå§­puèTï¡@9¹\x001d3\x0017À÷ps2ä\x001e¸ÕS½G.ò\x001c¿(-­\x0019>Ñ\`§\x0016Ýñ¤õÕÕÓ½G\x000e\x0001Ó»¨Kíý\x00048Ï²_\x0015\x0013Ý\x000b¸:rº÷ÈÅÿËý2°/\x0001Î\x001bÂÈIW
]§§zËJ^\x0018K4Óã~¼}\x0002\x0003n<\x001eì\x0004\\x001d9=räh4½ÊñÈ±¸}h÷Þî\x0000\\x001d:Ý}èäÎlk\x001c=4>®6\x0001VíæÄíMuèL÷¡Ó\x001e\x0007\x0003¦ÛFd\x0010:t»\x0012µ%*í\x0015Ê¹³Äû?pÚ]ªï>ÝÞ\x001f¥&ð'Ý¤ÇoPîÎY785iCKõÙr«îõFuLÆr `	wÞ×~ÖIècÜz`\x0018àR¼\x0006Ê\x000fòx\x0018v6'\x0000\x0014°]ø_\x001eI\x001fã\x000fø)éñÍÏwË°³¨Û\x001cÿãÝ·~Ø8»\x0000ÀñË4\x0016&ypìä§:,¯V¥Ú\x0011ùãWËÄ³(Ý\x001cÿãéÇÿëMk\x0010Ã\x0018òb
L1E\x0000»x§J	
l1"\x001fîÛ&ý¨Ò\x00125Å\x0012[rü­¬Ë\x001f¥9ß¼ß\x0014Sb¦\x0012ï¹¦¨U¥¯Ã<¹à¨u ûM±¥)v)2¿
YÁ
Ø«ny5\x001b3ûMq¥)n)6\x0006\x001aO½¿löjöâKSü\x000cS¤w\x0018Mp¿\x0004Í%R\x0006}SÇ£ßPZ\x0012fX¢ ²\x0004k\x00047Zc%$ºæ\x0018ånSªR4ñU\x0002_ºSSR\x001eºXZ®~[jBØ¢E·\x0019íYB\x001dKÙsGý"EV\x0014)§pd´&÷Ø}\x0018¬·¾-jÒo®lÑslñ\m¬áWdg#zó¾KåÄä\x0014/VÃ ¹$I¹Üäã\x0017Ðn[ :û0åì\x0003f\x0008i\x0019Gi\x0014þá0½Þ\x00014dK\x001dRÎ)Áq¶Ó\x0018ÉÓðX7;cûm©Î\x000bL9/¸Çh\x0014z¡T.w\x0016ª/Ã/Pb0'\x0016Óó\x001fFçy÷Ê[nj\x001fôÛR}sö±Ò"d c\x0015§#£)òl1U\x001d}5çè¢3ÍðÀ]-XÂ·\x0013ý¶TG_Í9úVåÀ2Im¤\x0018õc<4ë%úm©¾sôÈ·0àR
«AòÕ\x0005¾Ð\x001e«¾sôÓ$çdK.´ÐÇ²ù\x0018{~\x0011[ª£¯¦\x001c}T-°ö\x0010òK
-ù»Äÿ|\x0017]}=åì+\x0013rß\x0007\x000eV¹Í³9^µßêìë)g_[Ö´ÄæÄôB"­\x001cñï«Ù¤iqJrt\x0019ê¹ì3\x000bõuà\x000e\x001fïVåÏ\x0007¯cER¯dÔ\x001eüDIcjùFØÈ>æ\x001eh§¾Ì½_Êã$å¤d´ãG(å\x0004gý¼\x0010¬®á³ÞGöÝÑGûnÎGRJðÔkl£Buã\x0001\x0017¾Ì¾\x0013îø+¹I\x001f	8ê\x0014ëÂµæLG­æ\x0008\x0011ê¼?æâ½¼ÿðÓíû\x001fË£On7ö¾@ü¹\x0012ÿpgö>¬\x0006h/¯_<»|~ñUÒqyôæõëËö\x000c!\x00129ü«\x0012¹ú-!×%r=<zVÒj\x000bÆpÝ»r$zæ@¬jÉöA7%tó[ZtW"w¿!ä²:¢rìBà¹ÏË4!Í\x000fW÷Ëê³ó¯b_y
uæ¸ÕÕðkè\x0002éìúö§¿Ý<üõìY¶
»÷øz°Ð¯ÃpIPWT_lT³83ýýõå³?]¼ùýÙ³øófK£9î{5ü
:`\x0015$Õê\x0014\x0000I¯çÞR\x0008îmêõ J\x0013Ô¸	!á'HªjÑ_»ù@øõ0þx%M#\x001cêo(ªì1m»µ©Ï\x0004S`Æ?\x0001P7¤CÁ_¥i\x0017Q
3¦\x0019åô`K\x0013ìøWà\x0011NÇ{uz~_Aä¯àç\x001f\x0004WàM×éy_!R/\x0005Ég¡YÍÐg/-ðÃ\x0016H\x0016`\x001fÁÒË¬ñ$\x0004]\x001f×oB(M\x0008ã&ðã²CÑWEM2âÀ	ÍÊË.\x0013çX¤51n$}>§¥¢)ç\x0006uø3¬\x000eÊë·¡¦æqn\x0016pÎ;IP¶ß8¯ô;Î²¢f9ÎÍq+¥2i§\x0001Î
\x001f\x0006²\x0000Ýa}\x0016TÌ,©yÃ-³\x0005Ô½âp"	Û0ÚdÅÎr¦¾ØÅôÎ\x001awÕÙé&Tì,éÙ\x0005Iµ;ÑE¸g1!\x0006Üdjj#÷ÙPÑ³\x001cægfd\x0002+Å¯ d6az'+zÃüì<p §ññ>ÅÚ\x001a¬óOtEÐr¡]¤­\x0015Mà\x0011Hñ@ÓtÃø\x0019/)ûLÑÅq*Ëã¥íÉÍO·7\x000f¨âòè\x001eqnCÊñ)¶[Å'BB[®ã'\x0017Ï./Þ Ë£küíÓ¡D\x000cÝc4\x001aÜãùd-%\x0004GuYU	YõB\x0006íIõ B\x000eDY1T\x0007BlÄÚ=`?b]"ÖÝ\x001dPÜ¯\x0000/bic¸¦\x0018òêÕe?dSB6Ý8ì\x000b\x001e?¡§®[µ®>»\x001f±-\x0011ÛþmÁÅî\x00111§Ñ!¸¼WkG÷#v%b×Xø\x0004W@r\x0015:\x0018ÁpÕêxýp}	×wÃ\x0005%¹	±áa¹³h\x0011òê«ð~È¡\x001cz!ËÀÍJFRIò:@ö\x0015°ÚS·\x001br1q\x0011)Dôc^Ô\x0019\x0013fCcruP^2æUúë òA*\x0011	þà7À%P¾\x000e&äø^äqÍC¦\x0014¯\x0019¹Ë²yüzrø\x0000ûÏ\x000f7!§u\x0017²\x0001\x0011¼8©\x000fSxÃì¢·G\x001d+mÜçãÅa|5Ý~\x001d±m\x001f» «v\x0000\x0016W~ð$kfè\x0013ó1pèöëøí¡Û\x001aJÔ0:äEt Ô\x0010o8ÔÉã´Wí¢û`«\x0012¶\x001aLn\x00042è¤ÓoPèPC»Up'j]¢Ö\x0003¨½#-.\x0007y|C\l\x0000^ìf¶w/lSÂ6\x0003°¥¦\x0006\x0003'\x001dkE\x001bË¹\x000eµ''Â¶%l;¶Ú©x-®¶§¡¢¸Ú| }óÊµ\x0017¶/aû\x0001Ø.äMâè8\x001a\x0016ÂÈd\x001eæ"ýéE1O¹\x0003t¼#¦yÊ(¹Ï£ä¥\x0013óDw.uUq²,wn'í\x0001\x001f¹F\x0014û;m\x0014k8a8ycôf\x000c½äºÆÈ5æ\\x0012xÖÓTáÄ\x0008Úó\x0018¼\x001d\x0003ïí9\x001dÑ4ï(\x001dQ~xÑÍtùnò9Æ®Æ°k\x001e4ï ~\x0003CÏ5½.¾\x0003;VÕ©\x001cåë(åñý»¿=º}÷±UÀ>äTÕ+ã/=\x000e\x000ei\àÐâÓËþøúÅÕïÏ\x001e]>ýö¢\x0015Øªã¼òu¸Ò\x0003\x001fx: .`­ºÜóâl[ ²\x0003¾*á«Qø¹-\x000cUöéÕ:hÃÕæÄÌÑýðu	_\x000fÂW	êÄ|²&½\x0011\x0015¸ôX­O5èoJøf\x0014¾æé{(ÂJ<Y2RÁìÅ·%z;\x001e'LÒâGÒ¢÷Å`<\x0017KËéïJøntëkR{'d¥\x000cÍ¥ÑX\x00031\x0019¾/áûAø¨þB\x0007E\x0011M\x0008¹\x000cÚ´Å­:Ð\x0012}\x0018]üÃÌ`«\x000f~ç§ ã\x000b¿H\x001e)\x0014^ö9\x001eÍ³EÖ
R!Ï²ÝpÁÞ¿&ÝQÖ&ã\x0017:Ë\x0004«<K½-ÝÕ\x0001¿"]9Êº\x0012Îl;øÃæÀ»G¼\x001f~Eºruc&\x0012ëâ#
G\x0012ÂÆ·%;ðW¬+i×SÂÃ\x0002ÊÐ3í²ç7öÄÄïýø+ÚÃ¼ë°¤yÁ\x001fY 
Ü\x000cßÖCî@_Ñ®\x001cåÝ\x001c5`"[ÒæQ¬\x0016a ­ÖÚ\x0001¿¢]9Ê»XO6¿t\x00078\x000ezÌ	±Ù\x000eø\x0015íÊQÞ1LNèíÁõäipñÞr:E¹\x000f~Å»rx³ëØ×nx)bÖ~vÔ\x0003\x0015ñÂ(ñb®Ö_9\x0016\x000c;qbø6ùðBE¼0|Ý
¬ð$ ÷²µoëÔvà¯¯»ÃÌ\x001b8jNgü*°ë\x0017fòñzaøÂ\x000bt|Að£{Üþ,ë`Ôú\x0004ÕNø\x0015óÂ(óÆû:µ
Bü%G\x000e5\x0003\x000e³¿b^\x0018e^\x0012	@é\x0003\x0017ÃÙ\x001f*ÞQÞ\x0005ï\x001cµ9Ï#\x0014çGmP\x0011/\x000c_x=ë\x001a\x0000N¶ìz8j«e=½ø+æQæÅi\x001béÊ\x0012ãOÁÙgÐOg®yay¥\x0018r\¢\x0014´¢D§5³]ªW2/hÖ°Wö­Ò¬"c]Æ¼ú¸ûU/Ý¯¼ýéîý¢ÒùîÃ§ÛmÀ#7åù\x0011v \x0015\x0013xX[Õ-üäòÙÕóE¥óé×\x001b\x0010C\x0018º\x0011£PnºàUÅ\x0011b)y\[­ôÝ\x000fYU/d-sB\x00079ôr­Ô<¤Ã­¾\x0015î¬KÈº{qøÛaUÒàà©-nµ¤c?^Sâ5ÝK¬\x0014ÏmÁG°´6O\x000c~ÕïlKÈ¶\x001f²¡¶\x0008Ùà»f§2¸UE°ý]	ÙõB6q#§÷W\x001b4\x0017´YÇ\x0001:\x001a5
±/\x0011ûß·\x0008%äÐ½/¼bH4¢Ó¾pÒ2ä°Ú^µ\x001brøE\x0016\x0011¿e\x0015Èn"ÑA°ò[1G(a\x001d°óaSG¥k\x0018wÔ·ä\x001fo~¾}÷n«º£ÖY0^\x0000K\x000fö,¿\x0015#ÓqÆO6ß²j×\x00106\x000cÀöÙDÛ@³\x001ab¤*ø9É®®u\x000flUÂV\x0003°ãEÅÎâ¡$\x0015]0Eè\S\x0006|/l]ÂÖý°Qo¤YU`éòüæ.¶¤7c6%f3²ÔÉÐàW
<YÛúxy\x0008Û°íÀRc¯Pe1,»·tí
MMò½°]	Û
¬¶,ª¬í¹H°ÁeEBÕVæß	Û°ýÈjç
\x0011'hËnÄ¸¦`ß^Ø¡\x001dFV;pøoRMÆ²Ú\x001eXgPn)Ù
»|Ë=.\x0015Ü[	Çdêµ$\x001cÿAËù´-9Í¸k\x001c!I'óÈ\x0018°òrsÙ\x0017[^!6Ã®8R\x000e¤'#Ê`Y_O;*K·¦=\x0014`/î$å\x0000KBj{Nts\x0018f`x¢£
Í>ô½¸+Æ\x0003rÿRRÎ,°±ÚîÉmÆ]ùn9à¼Á»ì\x0005m\x001e»¬³¤¤ñ[ê\x00136ã®¼ \x001cp\x0010\x0004+`C~]¸\x001d»\x0013\x0007\x0013÷7Tî\x0004\x0006Ü	r<½ê`\x001fã6Ô\x0010ñÊDÖê\ÂÈ¹\x000cK÷ò[åèUç×@³©
j3îê\ÂÈ¹\x000c±þ \x001bÌA÷¶WÍ°«c	\x0003Ç\x0012\x0007UpÝ4ÙØ-'P\x001dK\x00188K\x0013ä	\x0012ØÔ§õ&Å\x000eÜª:jäXzÍn\x0010K%$MkQùÅéÄäî½³ªUq¹ Õ%é{Ñ\x0003ÍÁ\x0007\x000fC»E±T{?3HQÇèåqEýNø*?©èËIóS9ËoÛÔöß}\x0014\x001c~?\x0000,ÊJ¹\x0008g{	ÁÅvµM´\x000fúÛ#èo\x0007\x0002[u.Hä[Xv11\x001eàì\x000fzáÐ?\x001dAÿô\x000f¾ê7B×ù¶\x000b\x0014õF'sûñîÛ÷o\x0019ü×÷7ï>×¿ýò÷\x001bm°ÑÃÛôÆ­¥cfò.ky\
`._]}uùü1[òõõÅó¥íõÍ\x001f.¯7Ø\x0003¥=0Í\x001eÅ»³rÞyþ&°>TwÐ\x001eUÚ£&Ùc|~DÖ\x00189¤ÀØçä¨õ\x0011+öèÒ\x001e=Ë\x001eëÎ­ÌbÞt!ôà\x000fjÞ«\x0001Ü =¦´ÇÌ²GY~£ÓkDpP\x0014ï7½^#2h-í±³ìÁQ¶Ç°¨u&7Øèõ^ÊA{\iepÌD"A§Ô×\x0005þ\x0007­ñ¥5~5Ë¤ÔÔ\x0004âÎ\x001d[Ã	\x001bM\x0014æÒ0Ë\x001c°<|Á°æ¢uîÐÒò¥ÌÉùÄÄ¥b=ñÄ\x0000\x001b¤¨ç\x001buýùðõl× Aup0+:0\x0016Îe><Â³æ\x0017®Fì 9Ul g\x0005\x0007Æ\x000b\x001e`UXImn\x001dô_yd\x0015\x0019ÈY¡®ÍChÂOïóÈ\x0005øb\x0006U¡\x0015\x001bXÔ¥X\x0014Ç=y»Ázkj=K;|ý-\x0016}ñïn¢)\x0017ï¸ÿå¿Î\x001eßÜÿðáý6\x0013å<\x000fÎm§É8T«Ãý^>½ð#ìk\x001c\x001fqýÕç§aC	\x001bF`@Íäq½ó«TKæôjgg\x000fnUâVCË-P/9áÎgR{U¨´\x0007·.që\x0011Ü¨·\x001c«\x000f@ÍûVæ£u½½_½¦t¤\x0018¿4CkÍÍa¡¹¬Ë¬«ýw¬³-1ÛÁu¦n÷©LMëìóB¯\x0005³»`»ã\x0012
K4~\x0017\x001dá/ÿÏ»g_=üïün+rÏb\x000br\x0012ÝÒ²º|DÞÊ¥ý.:ÀÇ/®^}õæþj\x0003z]¢×£è\x0015$ \x001f¤é\x00181d?ØÊ¿v 7%z3\x001eG°ïr\x0008\x0018!\x0010zÛ\x001ckÚÞèí(úüÂíÏ;Ç±K\\x0014ì\x0004ïJðn\x0014¼Î¥Û""²<\x0012E6;F:Àû\x0012¼\x001f\x0005_EÁ³^³ÔMÍé\x000eô¡D\x001fÆö
V\x001bkö8Ë\x001d}³Ñn?ú¢¨Ã\x001d:úá[²\x0002ìêÌ?wíÒ\x000ew(í\x0018Y|z×D
å¥å¸±=Û¾\x0003=TèaÂÚÓÆ\x000f_ÑQ2YÉ¹d%+ª£\ÍQìï5çð¤ãÅGQ¥©è+ªÃ\ë¹C\x0010#\x0005\x0006¯L\x000e\x0014æºLYQ­\x001cæZÍoAk\x001eï3D¹0|6ükå(Ù\x0006Á¯WA¨sAçÖ\x001c`6GIuÀ¯ØVN [zß\x000f8Z\x001f­>f1p\x0007üoå0á\x0006nÐ_"SãùEØÞ;\x0017~E¸rq\x0015i-ÆÕ×\¥3÷ZÅ,ûáCÅ¸0Ê¸8®´ü^\x001eÝæéªNø\x0015åÂ(åâ-ï}\x001eZd%ÅÕo\x000e9é_q.\x000cr®\x0014ò\x0010®\x0019Î5c7\x0005¯þdÏ\x0003\x0015çÂðýVr¸\x0016â°\x00142p7\x001eÈæÓy\x0007úsasãÖ\x0007rûJó´[éãxmòí\x001c*ÒaÒ=ì\x001d\x0007\x0019¾åt\x001f´ÄwÀ¯H\x0017IWòxx9»àø¦\x0002bòM\x0005*ÒaÒ\x00154ºÂ\x0006ó:¼ñ¡9;½\x0003{Å¸0q\x0018×x~\x001e©ÍÁÕ\x001dè+ÂaÂ\x0015\\x001e<+\x0000ââs¸£\x000eûá«pÕð\x00157äl¦å¡¸ø¦\x001bî¨pÕð\x001dWäÞà\x0018ùä¤ âcÛ\x001egÕ\x0001¿"\5|Éõ$èÇXP\x0013Ge§9yõë|ò(á:)\x000bõ\x0011(^0\x0005-æ;ªb\5È¸R\x001a~ì\x000cÞòêäp\x0007Ôäüª\x0018WM`Üå]Ð	ë¨QëÐÉùpU\x0011®\x001aN)çV×à<7{áPLÞú/éª"\5L¸¤#\x0013\x0017ßç@ß²REüç\x0006kª¢\5r%\x001f\KÓ¸øì6v\x001dè+ÊU£ë\x0002i\x0006;!!o\x001d\x000b|nÍä[®(W\x000fS®Ë[\x0007\x000e¹µ¼ô±W|«ù£ü¸ô{ª$ê'ôvrVVW|«ù6PíQ\x0008¹½þ\x0010iêÉ\x0019q]±­p½\x0015´öÀc©qíyéW\x001f;Ñ×¯·Ã)eKEá.òà¹Ïù|gÙkõ0×
§\x001dÿ$\x001fÚür\x000em]\x000eô\x0015×êa®ý;¯}Eµzj¢\x0018?®=kÅ(3'Õ\sv\x0007ükõ0×:Å\x0012Ão©ÁèáONKélõ0ÙúsÞ:ëi¥åI2à'ßPLÅµfk\x0002\x001d\x0017{®±á7gtÀ¯èÖÒ­Ó4¹\x001c«\x001cï|.ýÐl~ë@_±­\x0019f[\x0013üÛ±9Êô×¾¢[3|¹Uç\x0004\x001e5WØéðí*¬Wù÷¯ØÖ^mµ ¦O'°÷äHjÀ)19\x0019kêZ©Q¶uf(	\x001cÃi\x0005Á\x0003 Ds&H\x0007úmÍ(Û¦Þ¸m\x000eïþ6ç\x0014&¿ jÍ(Õ¢&'9\x001c\x001bH3b§q&qå=å\x001dð+ª5£Të\ÞõÆçRi\x0013òâON%jÍ(ÕZá;÷½æËÍy ûáÛkí(×"f>¶:s­á\x0012GÕ\x001e¨Ñ\x0001¿âZ;üv+¨SÀaÑ\x001dçD¸ÓÜ)hÊtÀ¯ÈÖ­9JA\x000f¬°\x0015áOÎÅÚmí(Û\x001a÷>êç\x0001>ºJ¹u\x000b¶â[;z»ÞR\x0011|ïs¨£¹ÆTAsÊe\x0007üpí(áj\x001e¬ì$Ö{ÑÑ\x0005Òä«?9\x0019këêäQÆ'UDø6_Rxíu³Û¿\x0003|Å¹vs
êYÜù6g3|¥Ôdø\x0015çÚQÎ iH´2?C ·¡Õ|½µ\x0015çÚQÎU¬/â$H®\x0019\x0011!i\x000e\x001bÝ\x000fßUëF9Wsyx\}s#ï·ª­\x0007ß\x0001¿â\7Ê¹Rq¼)Q\x000e7yýø?ÂÇÀÜÍã*Îu£\x0019\x0011\x001aT# Èëg¯i&_p]ÅYn³à°õq\x001b¥½#<çÕ\x0014\x001eM_q\x001bå,ÉSGãâ_Û;M]£\x000eø\x0015g¹1Îò!º}ÂMÔ¡
4HÃsÁnôu÷Á¯{jFY\x000bd¦\¥¸P3n\x001e'Ç;®"-7FZHµçÜf0\£\x001cw\x0014ÏÇ¦Ä^\x0007ü´Ü(iáàHMo9É <\x000fjV6Ìï+Òòc¤BdißÀwtÁ\x0002GN«ÉÇÖWåG\x0019\x000bÔ²Ë÷Ü%,ß²ìäâv_\x0011\x001f#,\x001f´ÂÍ¾,¾\x0006
Mp|ÇÕvrÁWD?vIôX¥Ìû^ìtfïpý\x0018á.cçl\x000f É³±´\oä+ÂõcëòFº$Ú\§\x0019c &ÜÐ\x001cóÝ\x0001¿"\?J¸yrU\}.yhÉ«?¹\x0003×WëÇ\x00087®¾¤8$§0\x0008ð\x0014­i1ùëë6ÖQÆ\x0005Ke²øX´¦ãâ«¼ø\x001fÐ}E¸~pqÍÏ\x0015ÝS\*\x0010ë4u{`á~ø¡"Ü0J¸¯Yà\x000e£yèÓa²Û\x000f\x0015ç1Î¡r 2SÊ«ÌZÁñæi+¯vÀ¯H7®\x001cl¢t9ÐÌ3É©M\x0003+ÄCEºaté\x0005ñ¾ÅÓ\x0016½µ\x001c­­K·õa¯(+RU\x0006\x000c\x0018(Üá\x001b®}E\x000cË\x000f£.?Æ\x000biX\x001e\x0016óæck¸\x0019N»ÉÁP÷þ:MÉíXX`D­8£fðSo)RÔíóbÐíøèk6OðyF67 \x001bi&{\x001dñÝ§Ûû#¿?\x0019û\x0008@AÑ\x0008çu*­ \x000cPI('ÿÉ\x0012Ê#'!©§Ôs_(rvöØ
gÇ­ð.'kýáî_\x0018µk\x001a¾«Ä¼â\x000fÊI·\x001fÏ¾¾ÿå??n»óz	<\x0000Ìb5Ør\x0010R#ô"¢\x0016ÖÝ(O\x0000»|uöõõå«ÆºëcÕ4mò\x0000°3	·gâºÿi9!\x001bËw\x000c\x0005
àÎIO\x001a\x000eÙm\x0016®}õ&þo^]¾þõåõiàP\x0002\x0011à^å\x0007\x00158Ô`XÇYe«ã\x0008ö\x0002×%p=¸âJ_Ë\x001d 9ÆWª=Qk/p[\x0002·CÀ%um/¯Ü7|x:o¿~î\x0006îKà~\x00088Ð4Á\x0008«¤Ó÷º=
x'êr\x0002¢9Kê­s"\x0001%\x0016x½YaOi3\x0015yu4åÈÙÄT74Ñýq	>(\x0016ÂRíéÅ{WGSM©4*û¦8^Ð\x001d$\x0002÷97Í1
{
¹\x0019A5)¤\x000e=/®Í*Ìý;¥öÊ÷#\òK\x0015ã_.\x0005d%\x0011åÚS\x0008ö{\x0004þíØ²ÓF\x000fp.\x0015-<ð{}í¯aÿu9I	G\x001fP\x000fý|z÷ý/ÿuóén«8£>h^ðü°Ùâ\x0014ªfåh\x0012z}zõèòúâõUK¡C	\x001d +í³Ð³\x0005ö\x0006xh³M¥·ýØU]
.;["\x001c¤X/óè'Ù»Ú]ØõØºGÊ§^H%Ýa®äôjÃ°=ØMÝ\x000ca7qÓd
ÉYU\x0014¢§-£ÏûÛ\x0012¹\x001d[u\x0010<\x0008Y	Ë\x001a]ÚÓÎ¶ßÑöCw%t7¶èØsÖ\/\x001dyË¢\x001bÞ/ÚµãóÝÐ}	Ý\x000fúHII¬\x0002³\x0001$hh¤§YPV¹þ1ØÃØ² Ü\x0012à\x001cÍ·ÚØ©[ý\x0010í.$ÆVÝX\x0006\x000fñrGbF²µ¢)jµ\x001f|M¨c\x001a£rÝ\x0003\x0007Aªeþ@ö1j®\x0015¥ÊANÍý\x000c<5?\x0019n ²¦\x001dÅìÆ^Ñ\x001cä%OM06nt®ì3¬i¼ã+ç.\x0007½{Ð,Ë\x0002Æq\x000eÃ\x0004be\ó­u?øÊGÊ1'©ÁäE\x0002ïJÜñ`êiÊÕÀ«Ñ Ï=aWy×ÄÍÏC
M8=>lWHPæISXPÏË\x001bÇ²èn\x0019m\x0018ï»+?6\x0001M\x0000ðë¬*£=ÏÓ'wÒþÇ×'¯Oß|øxûógO?<üòÿn¼ñá~!ÅÚÈM,;I*Æ\x000e-_ùÍW/=}ñ¦uUeÈPB~È\x0013w\x0016ç|ú\x0002\x001e5\x001fÓ0«\x0012³êÇ5L	2JJÓ<KæÂ­DÌ>Èº¬\x0007 kL&ÌO¤¼5ls¾ù>Ì¦Älº1+çºøKÍSf)ùCóÖÙmÿ:ãXÙÙ\x0006ÍyhMµ¨\x00106\x000f²+!»þeyT^{*ª²!LÜ\x001a¾Äì\x00070+\x001eëâýçT{jÑE!¹Þ9C?f\x00054\x0003ÈAàÇ,#X¹f\x0004¹¸úÈÃÕ§\x0007sDJ×\x001e\x0017ïl@\x0011¬\x0000v\x001b¡ùÜ¹\x000ftMý,º±¬eÏY8½èlF\x001fû@W4(ûyPiC"Ö©\f\x001fTRÊY +\x001eýD¨¬8§ÝaôyH¯Fsv<þÓó0WD(û0b¦­\x0011x4oDÌ[£-³º\x000fqEr\x0007ãµ|\x001dNIM4h¸â@Ìót²"AÙÏÊ-M	²@¡·\x0004õãj62ï\x0003]Ñ \x001càAG:\x0017xä±ñ¬\x0002B³0W4(ûyPcôLÜí\x0014WÓ[ÁÂDBÃ_ø£?Ò8{ºÛ÷g×7oïÞo\x001bæç\x001d
$$¥àx§%ÄÆ)É\x0011n*\x000c|syñüìúâñÕóÆø>\x0006¬KÀº\x0013°ÅÇ\x0010ö­¥úC,`¼Í4È.¼¶Äk{ñ:Ë3û"}PÔl,?ãvoÎ.¼¾Äë»ñ\x0006Î3Y\x0015÷\x0006áùf\x0002Í\x001a=°(\x0002ÎaÑþ\x001day\¨\x0005W\x0018$/±hª¼ïB\9Ù{èb<Ì	`+r\x0015ªU<ýÜûfJi\x0013b\x0011«¿B13\x0013³0ÿýïÿñäÿïÓí;ü»o#Òó?Q\x0007B#¯x4I\x0003\x0000.«âqi\\x001fæcÎ¼x}ù\x0014ùmüS\x001bìÒ\x000ebGà\x0012~ëÉsÀ¼àÑ\x000cr5o0`*íPSìp\Î±|\x000f.06Û±ªL5`.íÐs¾GàHü\x001e,êó õa\x0013\x0003vÒ\x000e3ë{Ð3¯;2\x0007\x0012ÇqN7ÃfØ\x0019fHÁÍàÑ\x000eòùs|cîJ;ÜÏ!©E0Úá±J¤ÏòñX}±Z·cek8®F\x000cKVeÂÇù\x0011\x0002?Fr¹ LÞS«7»þoQ'µaç\x0004\x0006Úá¹úìàr×\x0001;j
Ãî`Õü %
·IX­\x001f0¤â@9\x0004%òÐ|"<2øÔìÝ}<"ó¸r)émèñû¥þñ7?ý¼± \x001e=\x000c¨óØÖ¹¼[¨,)Ze\x0018\x00114½\x0012=~ñæz©­üäâÙËVu=¢JSÔ\x000cSPh>	6Øz\x0011àE,}\x0012\x000f\x0008|À\x0014]¢çb)Çí&Tb\x0002X1H´.\x0003Ò\x00123ÅHåüQb%>0ÏIsôç)¶4ÅÎ1\x0005¨í9bK,ä\x0001²áËl/WZâæXbÏiÊò¹\x0002çòÉÐ(\x001c°Ãvøß´ó
¥)á·lJ\x0011¬DS(ð³%¸ã;»;To<»º¿Û\x0008Ýáx R§@Q^+nÚÊ\x000c\x0008öêúj\x0003T(¡B\x001fÔìPD"½wF¨À\x0005e'j;¶"U%RÕÔ\x001f^9Á-"è©i&Ô`1V»Lu+T]BÕÝßßçªÔôîß+fDS4y;TSB5]«
bx¶¨½\x0000Çbò¢úfÊ|;R["µ}Ê\x0016+ª<5mæÚ\x0018»~#Þ\x0007ÕP}\x0017Ô i\x0005Ï9:ìÑüýÖ¡wDW\x0014õî;V'¶á±ò´W°ùXµ\x000bì¶b­|ìrV\x001e¸Ô\x0008¬¡äx¨y*nÖv?æf¨\x0007].À£\x0004\x001eW»\x001ev«§IrÖÌYÔêXÉ®sÙ¾¤Û\x0017o9¬_ú¸Â²=
f;Öê\É®XyUK¬j.T¨Î\x0015ô+*=¬pj=\x0019h\x001d\x0000ô\x001d*ã9ÎZ°*Âjüd¬Õ©¾S7ZêÓ<Ú\x0001÷ÂY7åüCuª ïTé<ü\x0018ðXAä¸êT?Ð)¬ñUG«ñ\x0007\x001c­^ß¾ÿå¿Î®?üm\x001bVc\àònî\x0015öÓ,\x001d\x0011ÀO\x0018Â4\x000b\x0014®/Ç¿¼øÃi¬Pb>¬Bpu1´¢\x001a,§3Ôfd¡®ôoº£¬\x0012âT}8Ìõméï#\x0011pXS\kûz\x0012§éÂe\x0007Ôoåéªb#|ÃR\x0018Í¹Û±Ú\x0012«íÂªÍ¡þÎ\x0019VE·e
nVÿlÇêJ¬®\x000b«î¦\x001b+éyÓ	Gï7Öf\x001dév¬¾ÄêûÖ5~xª:wx\x0007¤^4q¨©j\x0015Il\x001aJ¨¡oYQ \x0015+H\x0013Y	ËO÷Ð¬Ù\x000cµ¨p9±{Yá¾\x000f¬û¢áN	ë¾Z·í`k
èã\x0000\x0017W
O°\x001d4ÐÂ\x001a¾]/ýq3ÀV\x001c ;I@B.ôÂtª§ÕÌ\x0002 ¦\x001c.Y\x0011ìc\x0002\x0007¹uLÇ+lÊ¢¯¢HÀùVÐ²\x001d«®°ê¾·\x0016R\x001bpXKý×Îåbáæ@Ñí`+æ}Ôm\x0010D\x0007Zò|\x001b\x001c K\x0017\x0017Â¦­¨KöqÁÚ\x0010ZYå¸\x0015Âç7äåQq\x0006Ø\x000fd\x001f!¸ÈX.ÕNQ­\x0013{zÀ6£,¨|,ôùX,B¤2Ud8|±|y	ÍÀæU:ríóZØ\x001eå¨îL;î:
!ö5\x000bå¶c­\x001c\x0001ô9è°=×!\x0002­Ü<'}+Ù¶\x001dlu¶ ïl9|Ý<tÍ\x0005ò°Få®¹æàøí`«³\x0005gKåÞy\x0013/[\x001b\x0014Vp`Øºß\x000cVUÇKõ\x001d/tUIØÊ\x001asà.Ë¹!¯Ã½·­Îê;_NI®³7\x0011·ã\x0010f Äà°õ´º\x0003luÀTç\x0001\x0003~<5©('\x0005\x0005$C\x001bï4Û<ìI¬ÕùRç\x000bëzÓ\x001dQ\x0007OáV\x000c_Ùs¹ §[ª:_ªó|IËùlí¹ê\x0001\x0007\x0015Kæ®9ñPUõ(à.ë½Ä\x0010\x0016^:)¹ôÒs=2fè\x0010\x000b\x0012Ï,¤(REË\x001bíÃÙãw\x001f>Ý~ÚVAî\x000c	È\x0012»à¸Á¶fø.ï²oÎ\x001e?}ñúòõiÈª¬º!\x000bÉ=p
ÞY®±'.¶C6%dÓ\x000b\x0019bÜå	qàf2ÍÚY\x000e5Â§!v%b×X+ÎÌ\x0005Ã\x001båsAHSf¢¼RàðÊz\x001fwoäeh\x0002ÕGeÚaZc7rKw\x000fàj\x0017ËþmBA©m=þkuà®HiZBM[\x0000K%Ê1p\x000b
8\x001eÎÝÜßlÍãL\x001f*{ýà§e|d^\x0015Ù]J6Þ=»¸¾hæÀ	®*áªN¸âPb&¸óÆÆèÁónXã¸½huVw¢USv\x0001\x000c=/X\x0011x<g\Üµ½»\x0017®)áÞÅ]^\x0013\Á\x0012"âÐ$áVë\÷Âµ%\Û»ºßï£#Îa\x0002\x000fEYp]	×õ4É­48\x0012ÂæÍàW[öÂõ%\ß	\x0017\x001bþyïF\x001fAË2¿Ò¯6¤ïD[dqÑ^¸&WÑ*\x0016\x0016ÞåzàÕÄèV¸(Tx&ÊÂ³'7,¶\x0016eb\x001e\x0003\x0007ËpAå¾\x0011×V	¿|uöä"RÅ\x0006¸ª«záZ¾Z\x0004¹°Kp\x0003¯®mJ*ìkJ¸¦\x0017n \x0002\x0014¥\x0010¸4<óoSêf\x000fXWu`õÒ7Ð\x001e\x000b`F3Mù=p}	×÷ÂU9ºñùe\x0017t`¿ gÁõAë>i>wh9Çmý s#¦jÎ	.ð¾½ùáæã§ûu¼ÕIÝGM\x001e:Ê\x001c«Ä\x0000ÁR¯Iób¼g}m×þÃïê´ÉÞã\x0016÷\x0003¥L=ªÃXÞ\x000fá÷[÷ÃI¼¡Â\x001bz×Wp¢\x0004k\x0000sK`¸'Ô7Ã-«©DUMµ\x000b®1ü&\x001fäÌò\x0015^ØfÊ\x001e¸w^ï \x0003gI|¼\Rõ:\x0018\x001ez!\[~\x0007ÞÊ;@¯wø»6¨\x0018zøï·òfÐëÍ¼<ÔX\x0018Ë8\x0014Y,	Þ·òfÐ\x001d<üÝÖ·
\x001e 3zÀn\x0011ôÃ\x0017\x0016ðÜ-W'ÅP9_èt¾`\x0002éX>èÅ?0\x0007¯ªÜêtg¨ØKäæb\x000cL\x0001GÇj÷uÕª´\x000fê¥û7\x0005äj\x0006ÒòS*Èæë®ò\x0018u*{Q\x001f\x0005$qU\x0005ÓâöcØ~\x0000u ].ïeî\x0006Ô<\x001b/þö¤è\x0007ìg;Äö£¡D\x0008ù\x001c¼°âwn<~ã{	ªJL=8ïÿùiúúþÃÃÙÅýû\x000f\x000fï6æ0Øþµ8_c©+öY7~]+¢<{}ýâÍÙÅõó\x0017o6\x001e\x0006¤<êCý¡Ãì²¯>¼ýtûpöÍC\ç³ç\x001fîî?lCï±î2UXaàÒÈbcY®\x001f;<ZËýæì«\x0017__¾¹>ûæ
óüÅÕõ
@i\x0008Ì0ÄÂ9±
>\x001d$Ñ#ã=«â«Ç\x0017°Cv¨\x0019v¨Àå¿øôHv\x0018®òðíî¿^3ti²¯²¦?\x00162¦á\x001bÆä®jÑîaêµÃv)\x0003rý\x001dhêo0Fçú;Ñz[í7ÄØ\x0019@Èá®1Ô¬\x0019
QY\x000có|\x0010WÚá¦ØËø1 dâ\u qO¯\x001d¡´#Ì°C\x001aÌø¤ë"Ý>\x0003\x0015·©\x0007]ã¶IïqzwóþÓÝû­LÂÌtÄ
V ð|\x001dK¿×ßd\x000e3;/¿~zñüõÕófÀ\x0017
\x0008\x001eÐÇ=Ã~ÖH{(ÿ\x000c^®z¨NôªB¯~ck¯+ôzlíql\x001dU/iAñÚsAPXTì\x0004o+ðv\x0008¼\x0015î\Q³÷¥ó¹åÕù-j÷÷\x0015xÿÛÚ7ªB¯~cèµ(Ñkñ\x001bC_ùK=æ/ÿþè+£Ç<v¯9F\x0018\x0016OÆÖ\x0004n¦Y-HÞ^ºã\x001d'\x000e] ?ÝÜo¼V
mø\x001dÖ\x0005~\x000c_6Å¶g\x0017×­¨@B	\x0012:@*ÇÂÈ¡"G1þD_å6ª©zÖRpêÔ\x0019G
ORpé¦výV¦Di:QR#­ÒX\x001eI0Yà[4CÛ­0]	ÓõÀy¶\x0005\x0016JkÉR:!4\x0007 n\x0019J¡\x0007fÈ\x0003\x000bðÄÓÖáØqd]sGýPs¼oQ©\x001eÖC\x001e\x0018\x0017ÕÐT}9VPÆë\x0010ý*ë&ÔÑ¥ÞÞßlm\x000eÒj¾RÆË¹L;\x0001åÆ	ÙJV\x0014zPO¢W½¼¾hë7	PðTâ~\x0013'âb÷*eýÁåF\x0015hev;MP¥	I$î6!z4oè+@.Ø¿Û¦ÊµÇ\x0004]ð4ân\x0013PåZ °Ü\x0001¦ïø+¨Fr¢Ó\x0004Sð&â~\x0013\x001c\x0017(\x001a;+kiÇø\x0015Z¯&ØÒÏ´\x0010w \x000cM&X×Må(¯ÐRºï4Á&|&¸ß\x0004Í²ÀF:G@\x0019n8­lv§	¾4á3ýÃÝ&äaôÑ#I³Aü\x0015Zï&ÒÏt\x000fw\x0010ï\x0007Få¯`è8Cñ\x0015¦Pê\x001dª_Ñ;Ümð89o±!Åe\x000b!\x0007~Oð­ §ÓÇé\x0019[°Ù«fáu\x0010Ü$æ×õãûm¨¼ª\x001cv«¨Ï[	;\x001fé3ø<~Qµ\x0006"õ2Cõ¹°\x0003ÅtC\x0004ÁS\x000cçb%íóhõmv\x001a"¿û¡\x000eø~\x0018\x000e\x0014©\x0018ñ	\x000etf¹ÖMªÛïk+¾\x001f³Âø)\x000cµ}K}nÓ\x001bBp¤cjØ¿©VÚç§ÃüTl5ºy÷»û\x000fØÃ%ó\x00162ô2®ù©6n¡fÁÒ³Ç\x0017O¿½¸ºn­ùñôTqÚ\x0001X°>$&],\x0015{d&\x0013í\x0012\x0002o{uU	VuU|_\Þ\x0003¨\x001cLçÀúÔÝ«kJÀf\x00000m\x0007\x001d,÷¨*ÍV.4µv\x0001¶%`Û	XÒ-\x0005æ¨\x001aE	­rM­Ð=h]Öu£ÕÔî©"¹\x0005ÄkXÊ¤­m»\x0007¯/ñú^¼ÆòvÀù¿,Èn\x0019°mÏÛ\x00058C/`ÅbT¼S{\x001fx¾n`\x0012l\x0012à"8,æv,1°ö\x0002Xëõ
·\x0013õä{\x0010×ÑK\x0019\x0011\x0013kI+¬+¡Má²B¯9UÝ³\x001dqE\x0019²3¤\x0011¬ÊÚ×'\x0014fÏò>Ä\x0015oÈ^â@Ä¥\x001d§mãe'diáiuX÷"Ö\x001eË\x0017ÄñÎ¯)\x00165Ì\x001cÆ4e9v!®¨Nör]ô],$\x0002¨D¹Ü,êÕ,ò\x0015yÈnöÐ«A-#·S¸o³0ê©rí+o,»Ý1ÞrÉ¹ ú ¬qåM¡\x0019÷ Ê¹A·sSÓÏ \x001cÏ¹ËMÕ´øç¨8yä\àº{3ü\x0016©DàB~é¸ò\x0004{R¦BÇÀ]?n¬Ì\x0005*|wñ\k¸òA7\x00054·áã\x000b\x0013\x001cMi\î{?ßn\x001eèÙ\x001dÞ­)ÌPÄ,¬¶M\x001c\x0006:-w½'f9\x001d_àh0ãnèÂ²~QE)\x001f'N\x000fjÛ\ÈÕ\x0008òøÿÕ«ãVÉÑ³_ÕÅè\ô:e\x000b?\x0018±`¹\x0003òÃ\x0010MâV r¹Ãi,PGªÑØ\x001fR\x0017æ}{÷§í¥UNb\x0017q\x001bÕIéz%hÏ\x0008k7\x0014:|{õu»DC\x001dÏ-S|t7hrcXwÎÔ\x0013·gÌbCIÕVÌªÄ¬ú1\x0007GI$cQg@[\x000eûÄz¾\x0003´.Aë\x0001Ð¦[\x001bkìð\x0002Ú°Z¯PëÒ	;@KõòKÖëÃÃ§å4>ºG[\x0013ñe\x0015\x0004ý±-©xCu\x0019ë\x0017o^/\x0007ñÑ5þîiÀª\x0004¬ú\x0000û\x0010xÀµ\x0002gø\x0001'~·äûÇ7IM	Øô\x0002¶üî§ðZK#Ï÷w=\x001bº\x0019¯·G;ÂÛÆÙW·÷÷w¿üç}ôÓ;»³\i±`*¥i±\x0003,áÙ\x001eA\x0013ÿu}}uy\x001d½õ'²\x0003J;`\x001d4?)©¦\x001aÎíjÐ\Ts"úî´Cv¨\x0019ß#Æ¶§¥+V¸÷IVÎ[\x001fh:b.íÐSìÞB¯\x0018öµ	¹´Å·\x0008ºí0¥\x001df\x001dZª,"¥Öi_áeí8Ñ4Üg-í°3ì\x00162Î³ lG»»«Ó\x000cWá¦áùx\x0018ÝUd]»·±Ï\x000c_ág¡\x000eµÀ©+}1Cü8Þ¾ÁvÚ\x0011J;Â\x000c;ÐÕRox(Eub\x0016Ó=1\x0015®Ë\x000eY³à\x000c\x001aD\x0019{~ê×Y|\x000e¥¥ø|ó!+ú3ø\x0003\x000b\x0015xg\x001døÃYoë'ºð»\x000cQÕ	Q3²ÚQ­´H%\x000b\x001c^[¥Tkf¬«\x0012±\x0019ß}º½?2\x00052Å\x001a*Ã@sH~Ïà\x0014"¶çKYººÕ/Ô~h+\x001f9.Âq?¿ñäÉq\x0006dvÃ'zÌ;éäØ\x001c7É\x001c­XiÃÄ8¾åáë\x001cO(Ìí4Ç\x001dçèÜ£»øËíû\x0007Î¶|}³1­èãb»Åw9e\x0014\x0015j\x001bï¹ ÞT×ðÅ·ÏßpªåëfbÑ\x001dç¸Üãê\x0004½ÈÓÊ\x0004Ú\x0003)BÄHÒ,ÎÕ%ï\x0000mJÐ¦\x001f4ÎçI ñM;=\x0011Ç{²\x00030
´+A»~ÐFP=¤Ór)éO·SVþÄ'i b\x001e{Q;G÷9§#Q\x0000V¿±j5
×º>ÝG1zqA=ÉN;yn\x0015ËR£]½Lw
4ôG1]q¶9K.,w÷D¿>oWËÊÈn\x0007\x0012¢×¦\x0007Â¸\x0017b¨@\x0019r\x0000RÂY×³í\x0000­+Ðº©SkJÚ\x001f:\x0006\x0007Ö\x0010ÀA:óPW^Ov»½¸«\x001dI8¸H+üÜ-\x001cEùÎ­j\x000eu¶\x0015hÛ\x000fZ;fE\x001dru\x0004ÁKí'újYùjÙí¬wz5VüÑ=D¤\x00166·\x001e'v ö\x0015jßÚ\x001e6Ht&Ö:k|8a&¢\x000e\x0015êÐÚðÈ\x0005µ¦Ä8ØÀ¨W+÷£\x0018¡\x00187ÕTAì°É\x001bÝ(_ëÜú°\x000eÐ\x0015/Â\x0000/ÚTË\x001cV=Ó«4<\x0000Øy +^~^Fs;£-¿Ö`¸èªç¹=¨h\x0011úiQ\x0004O
É\x0011µ§!ÝV\x0006Ð\x0018\x0003×yÑ\x001eT\x000c\x0003ý\x000c#
\x000fÚpq+çÎ©x\x0005#2ß\x0001z¥Ôï\Õ\x0015r¹wá\x000fz¯^Ö\x000bºzyKy¼x#Vo1«÷à\x001d«-åqG¼¬ÄÔ¿ùðþÏ\x0008p³\x0000UôÄ½\x000crO\x001døÝÕ¸æ´.|¿üæÅóÿ¿ÛlãÇ\x001dòR\x001c^z:@\ôÏFÍiÊ8XÙ.kÜZ¨Õ\x0000êàh&\x0016Ä[¤1S<"\x0011'µ_¥ö¡Ö%j=²Ö¹Ý\x001fbÀÇ#\x00085O%·¢9¾i/lSÂ6ý°\x0014ü\x0006\x0008¹RÉ	~:3¦9v/j[¢¶\x0003\x001d/òp\x001ai\x0013î\x001c®Í\x0014íÔà>Ø®í\x0006\x0016[\ )Ã9Ïüã÷V£Ûõ;Qû\x0012µ\x001fYì½±\x001có\x0005&BÎ¯)\x000b²\x0017v(aÅ¶y1\x0008Àé¥\[ªN*ï]\x000c\x0019âPíßåþ\x000c±Å?NÄÜ´%V\x0013q×\x00049ÀÎçNn7Þ4wQaÜÍQ{aW\x0014)\x000782ÞXh­ìx_Ì{ÄêSº¯{@W\x000c)\x0007(2º7î\x001bñtÊäµãåkÓÅImà=¸+\x0003$é$Ýi"µÛ|$UÞ"3)RV\x0014)\x00078Ò«\\x0007 cð:0%\x0007¨Cs(ú^Ü\x0015IÊ\x0001tp¨U&\x0018\x001e9Îä¤¦ñ\x001eÔ\x0015ÛÈ\x0001ºq\x0007E"\x0017_:m¹âÛh7ÑoCå·aÀo;«^@z*ÞÅù\x0019*³ûÄ\x0004ê;Â\x0003DA\x001djÌ@U.'\x001dã^/ÏìÁ]ù\x0012\x0018ñ%Nç6\x000cCd#Îä~jÍ\x001eÐÕ#é\x001dwAI\x001e\x001d\x00159\x001bòÍiñ=°«3	#g2^Éèöo\x0008o\x001bfÆÛª:jàLú\x0018øÑH]é\x0003ß%¥q&Ç$\x0013yRUgR
IÔµ#=\x0016é\x0015éÄ:ér\x000c(Û\x0002Ð;qWgR
IdJ*	ÎÓ[
2¥ÎqÉÌ}R\x001dK5p,=\x0016Ñz;ÉL	Âf?Qµ\x000fwu.ÕÀ¹ô\x0006¸YGâ\x0018\x0004[²8\x000eíöë}°uu,õÈ±´·UÔæ@AÆ=*¿\x0017º.\x0000\x00149À§ÿýïÿñäöþ§»O7BÅ¼¿n\x001d/½T^/´ä:J#VËZ=¹¼~võúâkÍ{óû\x0003æ¼Æâ¨¾%þóßÜÞ¼ÇYw·g>Ü¿¿{ûãÖ^.#xÄ& û£~¢À=.V¸\x0016K~syñ\x001c§V^]=zqýüêñVÂU\x001cu¢¡\x00010j59¥)-\x000fâ\x0002Íp\x0017zU¢W£èQ\x0018²T8\x001aÄ2äÛehö	t\x0019 K\x0003ôðþ	$Gê\x000e4ÚP,°þDÙßøÍ(þ\x0018\x001aÒl;Ì\Y\x0016Ñ¹¯ßO7À\x0006ØQ\x0003´Ìw
§¸ÈNywP³\x0007½Ë\x0000W\x001aà\x0006
Àö]MG@[\x001a×§$¿@æÕ¢\x000b¾/áûá\x0013õqL<ud(ïtë]U½øC?.?'\x0012ã$9d59ÓØ¾ÈæIÿòã\x0018kÚ=ÆåÉ]6ßòÜt\x0006\x0015Éa\x0002Ã@sç@\x0017'«Ì!wÞz^é2 b\x00009L\x0001Rsd\x000cXgC'@ëlÀüMT¹P9ìC¥8¸ } \x0001ÎÙfûK\x0001\x000fÃNHè,²¤\x0005W
)\x0008YÖ£%TÛe\x0001Tç\x0018FÏ±\x000cyz\x0005zTf\x0001îÜ1&Ìf1¨âh\x0018\x000e¤=ç0ÔS9°ÕÀ÷,ÛÔÙí3 £Gýñ\x001bGB
p;%e1ßy[÷Û.\x0003*?\x0004£~\x00089\x0014%ü 78CÈYaÓÌtYPù!\x0018õCÒºs~kÂAË$Öì²^§è¶ rD0êþ\x0007,P#RÃÈ\x001cèX@V§5=\x00114ëxº,¨\x000e²\x001a>È8Õ_Ys\x0017Qôªll>Æï²@Ø£r¤ø\x0003¾ÒÿîöþýÍû\x001fÎ^~¸ûøñÃûmà\I\x0010$?íØh\x0012Uêâ$µ\x0006øß]^?¿xþÕÙË\x0017W¯^½x~\x001a¸.ë\x0011àqÕI
,HÕ¸LÆÉõ&.à¶\x0004n\x0003?]\x0006á9ø\x0011Ái\x0006ÞÌ\x0010î\x0006îKà~\x00048\x0004>©8ë¶\x0008yú­m¦\x0008÷\x0002/zpì¡|£\x0013y\x000e×,,#xf¦tØ¼:rèxJçÄÍKêYàBziùÝÈ«ã)Î§t\x0007äI8ò\x0011yv#¯Î§\x001c: Rñk·G©3Ãkn\x0018ùÔ%¯Î§\x001c: ¨\x0004ÌCnËqÜ¸\x0014£Lô,µØÖBDÜÇÚÉE!»t7sÅý\x0017¹¨©«º\x001d¿9n\59±ùÓÝ»\x0018\x0000Ü¾ÿp·q§ó\x0019Ô;îd0Îf"RëÂD\x0011õå³«§ù/¿¸jí<\x001639¿\x001f2¾	2d/(æ>0ðÙÔÍ\x0012Ó}U	Yu¯rÐ|_ÅöÕ´7\x000c¶ä\x0010dß,¯Ú\x0007Yu÷*ËüÖDO
Í.xÞÎ¶©±\x000f²)!îU=H\x0000Ï\x001bÃrv/þ	Õ
Æ÷A¶%dÛ¿Ê¹¦4Ä_\x0006M«¹=îi]	Ùõ¯²£7³,\x0016Ùð¾\x0008«3\x0008÷#ö%bß½È\x0000¤e¶xæ¤Ún¼\x0008¼/Ö{'?¼®^a{¯Í!aÝ³1\x001c¿h\x0007ÉÝ|\x00113°sÍ\x000cÑ®e5ôsI¼É$\x0005\x0007ô\x000eçi­¡¤Sa\x001eÈJd7¸\x0018"\x0005­µáAÜÎñ^æ/dåe·[v¨Ó@û"®±"·lè\x0001ÌAûº¾\x000fsåãd·s8+u\x001ebj*@7ñoé\x001a DóÕk\x001fæÊeÈnÅÔáÓ{þ¬ÍY5FwaÊg@·Ïp"µâK0Tu\x0019O\x001f\x0011j¿ÍíÃ[Çqý\x000f'¥5Á1ÿKû¤\x0016Íy\x001fæêüAÿùKMÊÉÇ)æ\x0012kLvrzZ$\x0007Õùþó
Z\x0017ÌÆæ¸È\x0000EÊÏ;G×*ckU\x0007\x000bjoä\x0005]VÕÑ\®K5ìG.Ë\x0011äÂ\x001d6R\x001fÆy\x001e+×õ:¸å3äz\x0000ºsæ\x001chÑ] QÆiêaq\x0000a^è¡+±¯\x0004Å¾: £\x0014^@bðH3ûLô3\x0014é\x00195}¶ê#\x001bÆâ; ¤\x0003îb¶*ð!Å2µÐWº¯\x0001\x0012\x0007Ñu\x001aÝ}cÈ  GI¢jÜ9iB~\x0001YWøÈZÌÇSÈÖcl²\x0000J\x000b`Ü\x0002qnÈ\x0000Ï\x001eýÐg\x001bV³	«\x0006¬o\x001d2@\x0006¨a\x0003pë\x0010É#·Åa*^«í7A&èño`©EÛ\x0004\x001e4\x00127ÈBµ«Ï!ý\x0016Ò\x00023l\x0001v¦À\x001c¥nx\x001b\x0005.ªpaõ=¹ß\x0004[`MP9\x0003\x001b¯@¯D×+[úMp¥	nü+°\x0016]´èy*^;è+¸Õç©~\x0013|i\x001f6A\x0003÷t\x001b-©H\x0016+{\x000f²´ó¿B(M\x0008ã_ÁqÂE\x001bÉÊº"w?ÄëêtZÎ%ñ2h\x0003KêJq\x0010×yèã\x00178	ÕSXæî$E:cé,;®Rófµ\x0011yÄïk\x000b¾\x001f¶À£üVâfn£1Ø­\x001e6[!!Ôñ\x0011\x000ex¦dØ³\x001fnúp÷qÇè\x0015Á³³\x000b¤PäBQÛ\x0014}vñÕå³\x0017W¯ÚcW\x00182¡\x0017²ð¬ë\x001d!{þ\x001eïá!«V\x0002o\x001fdUBVÝ«\x001c)\x000b(j\x0006ÈCº\x0015g£Á6\x000bÂ7BÖÇ­4ÚÒ?Ïnÿt÷ñãÝíýÆn%\x0001PÄ\x0006Y\x0012¨ô@9<¥ý©¦Íg__½zuuyÝê²ÒÇ
4Úâ?ûa{¨ÄñîÀ\x0005\x0014t·R¦øßZ¨Õ\x0000jT6Ðt¯Òy±M¾V­
¯ö Ö%jÝ:ôÚz\x001d:\x0012\x001ay)\x0014¿q¶î\x0004mJÐf\x0004´¦7e©©ªUh«ò\x0015öTã÷\x001eØ¶m\x0007`;C½ÈNÐh	!óµ»9}7fWbv\x0003»Z9vÕèBXaß£\x0007±A9bÄøÏ2\x0006/#ßßmô×\x001a;Ø\x0016VT:U¡«et\x0004%ôtdMéË¯¯Z!9bF~*Ø\x0005]\x0005I·#¥Pkô8Ê\x0013¨`VÅÏú «\x0012úq`÷ª§\x0004A\uqXuéhÕÅj½|\x001ftSB?¾Zïîòª;\x0016Ô±8ùVÝo»Ðm\x001eJèÇ7¡}Ð¥£ç
¥Lµ"ð±«i÷.è²>¦cçT°¥RZó$'\x0013hEÜì«u	}Ø«Í.v;@ZZw\x0008,:l¬åu×§gÚíó1u"8ÐÇ\x0005,ÀeÏ\x0016ðê;¿)¡wÚ\x0002¡\x001c|<kÅÆùïÿ"º¿ÜmÈ=ª¤¥«³CÅ\x0006*h¡\x0006q\x0017÷Õ)Osvñ,þôÛ«ö¼I\x0002®Jàj\x0010¸ãa\x0008ø²'éÙCñí'îSI]ÐM	ÝAOÙº\x0004ÒÓCópÒ¿oî«É½ø,íøõýÍûevßÃßp\x000eÈ¶\x001doµäA¥(@Â\x0001xøñ~SöôëëçË$¿7¸ljçúãa*g"8\x0005©p"â8\x0005)¶8G¦4Ææ_y\x0004Læ|æú-_±È\x000eY´þqôÔ.*|öPuûþãC\x001a5³Í
o5&òF8¤m¢XOûmöøòù«7ËÓ\x0016@iÁg\x000fU»-p\x0007þà;~*\x0016t`HV:Zpz*î^\x000bTiÁg/U¿o K\x000b>{¨Úmä9\x001dVÆ¨Z²\x0012\x000bWi»*HÔm)-øì¡ê·ð
liÁgïT{-p.dµ\x001fÉ-äñ\x001eU\x000cL·À\x0016|öLõ[ø\x0006¾´à³WªÝß\x0000\x001c¸Ãú8°$\x0005IwV¯V+ô\x001aP<ðhñ+\x000f<{-°8»&dáy\x001a[\x0016*Y\x0000jÛí\x000e\x0013*>Ã\x0010}

Ï°Â)ªÔ±Áp\x0013¶«¢Ý&Tîô³i¿	8*1eaò\x00036\x0003%\x0013TØ\x0016øí1¡òFrØ\x001d\x0019l©Dü*§½¤Á^V97ý T'Y\x000e\x001fe#
ièâC\x0015m¢\Ql]Íë÷Z\x0000ÕQá£\x001c/:Üó\x0016ÿ\x001bùÆï¤â°ÞËßmB\x001dÚ
\x001feÇ\x001b\x001c½Nm{Ö³4Zoï6¡:Ê0|µÖTnb¨Ê}ª8ÊLP«­Ý&TG\x0019²\x0006M\x001d\x000c\x0006gßål#ë\x0003)X}Nì5AWgA\x000f\x0001)Äý&¨ãôR]Ô~w{ÿÓæ¼ \x000bÒ`y±1¤­ãý&ì¿»¼~¶\x0001¶*a\x001fßmvÀÖ\á\x0006¢)¹d±"êm\x000et#jS¢>¾
ìBí(Q· ¦\x0019V&¼Ø«\x001d\x0003=°]	û8Þ\x0003\x001bÔa\x0008góS\x0006lãÛ6êïóÕÎ~\x0014°(}Þ=ûðð.\x0002¿9{yóóÝR»¼cJ5¦>ºt}ó\YáÝzwÆÓË³g/Þ<À/Î^^¼\x0007ò4jU¢Vý¨­
4ËÅ\x001b¼sQpæ¨ÝGç¾¶³{`\x0012¶ùGCð¼¬_G?=þðpsÿÃæ±áû¤4ö)Rñ¢\x0017¤.ib,y2Ïöêìñ7\x0017×_5G\x001fËã\x0007FY?0î\x0006®\x0002ÝC4*TPðâ<X\x0002nüÉC¹\x0005¸4Ç3¸LJ\x000c~x¸?{vûñãß¶áRävl©XD\x000f\x0004O\x000cÃR×5¼/Þ\=»|õê\x000f§aB	\x0013öÃ\x0014\x0014Ó\x0006¡²´7YheUÚf\x000fFUbT=KÇ:6D"À3È#ÊÕ\x0016®=(uRw W3¥¢\x0018,ö¥²jY\x001dt½\x0007¦)aÅ<HHäûxCæ¸¸Î\x001e®é:`F
&í· ì¹K\x0014\x000cÎ\x000c¡D\x0019zP:®£\x000eñRæãL²\x000cS¬:¥-0ÝQ7
Nÿä¢À³ë\x000f\x0008+úÐQMüòÔ.fsW½ERjBm½ø7g×/ð·¢\x0003=
\x0019JÈÐ
9È4ÓZÑ\x0017;¬¸4·=0c\x0017bU"VÝ/¨\x0016´Hü\x0018ï¥´È\x0000ÍR» \x0012²é¬,«pXe¸\x000eÐ\x001a\x0012ÅÁ®ÈfIÝ.È®ìº!»¬ÐýTT\x0005óÆ¸jâ*\x0012rèlà6SÜËTÚå\x0014O¿òa\x001evCµÃèö\x0018\x0006{Õ¨YÇGÌ\x0014sYÉçÏ5µ÷a®Îì>i¤./\x0013ò2çá)~uÔó\x000eÄê¸V[-µÚ/ßÝ¼] ?»¹ûã/ÿuvóð×³oïÞop1Ì¡ùç8Ù¯ªá¼|zñxAÿìâ:F»g\x0017o~öíÕóV«\x000b·ÕR¸=lCÈQodpêÊ)¢\x000b·ZvÞo*mP\x0013l0ü\x0004¾4r$X\x0016Å¯>ÚôÛ`J\x001bÌ¸
ÀÕ]\x001cáðË¤åê-¯ßªW9\x001d	üÁ¨%ÑoJú\x001aJÓ2\x001cÄMî~U²­Ã\x0014}l?X\x0002®\x000f\x000f¡Ñ×7cC%Ý¹ É+ñÒMs(¼Ê\x0014«5ß/Þ¼^æE__`t¸ZÃ`¡\x0004\x000b`Q+4¿v\x000bÊÓ	\x0016»Öf}dÃN´ºD«;Ñz\x0017êô \x0006<$À8Éïa«qìN°¦\x0004kzÖñ;|¼²Sõ¿òä+ö^´¶DkûÐj!ÏÄ	Þ°Bbü5¯­Zï¯Ø	×p]çâÚ|Èò|\x00013FòÃ¢«7p}	×w®®2\x0014\x0004\x001aTÜ¢èx¼(:\x0001·Þ)´\x0013n(á>¸Fp1\x0018\x000e9·	®Ó¼ºÒ¬K\x001fï[Ìà@+:ñJK}X\x0006o¸^ñ33-¯\x0000±*ö³\x0013oÍ\x0010\x0014a¢® 2å4§Â\x000b\x000e[\x000c`gÁ­8BvDÜ³ô\x0013Ï\x0017SêØP¶ÐX±Z\x0012µ\x0017®ªàª>¸8\x0002\x001c(Õm\x001c>\x000b
 nHíÄ[ìd5§D\x0002+U\x001eÄªimÕz\x001fÇ\x0011ÖS±¬XBvÒD<SÔ}\x001fã\x0018MYD'\x001c\x0015 e\Õ ^ðG±\x0018ø*\x0016{ywûoÛ_k\x000c?\x001e\x0004~<À`w})Ã}y}uù/§áB	\x0017:ázõzéÆrô\x001e\x001cÅ¼FùÓ~l#\UÂU}pqÊúìWK	ùqzÖêê\x0012®î\Ý\x0018(\x0004^]I]"\x001dç\x0017°Õ
çhÿw!Ü
¼¸¿Ç]\x000cüòo_On¶\x000f<Ëó\x0004=êøó\x0004\x000bEw9±.ú¼$ñÝëÉEsêdFl*Ä¦\x001bqàùK>^¦×x`°\x0013ëÛw7`W\x0001v½]~\x0014ñ"w\x001f@ ²"TËZ}\x0015ÝXH/\x001cD©K\x00075þÁ=Ûðò1\x001eËÍPA±Z§\x0015üî¤At\x00168\ã_ø÷µ_d.ÍÐ\x0013ÌÐ\x001e)\x001aÍx@Ó[¤1<µ.²6¼ÕõQ%-\x0016S\x0016}µQkL \T\x001eeLü!¢WªûL±GDéíQÀåÛ\x000fï¶7~\x001b³ÌÉI¯Z,~\x001eO²ã$9­õõêìòñ§'\x001aÖ>~ÞÒô¼\x0015.íÄ¿Ù¶ä\x0011VÙü\x0016g¬=¨\x0019·ºìãÙ¥ªø7§!«\x0012²ê¬òó¡\x000cYÔ,ço\x001aâ¤;!»\x0012²ë¬\x0004\x0005ÕKrÄ-aÄ?ÑÍ²w«Ã¹¬4\x001fþ£"\x0017öxpMO\x0003÷\x001f~º}óCRbøÝÝ»\x000fwe\x0018d&SgsÕ®pü, Ô*ý¿¼~ñìòùÅWIáwWO_\5¥\x0018ìñ\x0008\x0005Þ\x0004ºÁc-\x001aÏ²Ç+"ðJ1xXu%àU	^7\x001fÌñn´ö$G]bµU·\x0013¹.ë1äv:N{\x0006Î!°8\x001aW«â.{Á\x001bw´á;&û\x000foüp·Y\x0001Eéã³`3J\x0000Ñ15°^ùQÏõÇO^\5Éçø¾æ<\x0015*$çòñìõÍû÷·ñ^±yÑ!¿\x001b\x0019\x0011ï=´èt
rÐÈ°yuöúâùóËx½Ø\x0002½vþ ünÐòh×Ä\x000bNÁü\x000fgßÞÝ>üõìñÝO·v\x0014¦K\x000c"IË-Þó=={\x001dêENòé³o¯.ßüþìñÕ³Ë×ueú¡\x0019úØMzóYãí×÷[ë\x00036·iz)w=ª\x001cËexVÕgö£Þç¥µ>g«ø\x0017GÀ\x000b
\x000fo>×ðØ\Æ\x0013j©Ç\x0010SX.Oè\x0014Ûé·"W\x0015òãrú}kÎ©Wr\x00064HÉñ\x0013^ÊÐÛT¸\x000bêwá¶
Ë]Ò«¢¦9\x0007VæQz£í)äÒ\x001f?.úåqñÉÍO·7\x000fK¶ðö§ê/Ñ±ßm^,m®ÀësHÐA\x0003+UÍ'\x0017Ï./Þ,IÃËgñ\x0007ßF×~õ¼Þ\x001d£wþê§o>~¼íÙéÆ ;IÒ»ò\\x0010xKuÓÖ­æg¯½¼xõêróº»£÷\x001cÏè\x0000t)©"&n\x001fêè· d\x001e¾¹Ú\x0007ü«Ðð÷\x001anUáV#¸E\gÒ_&\x0001\x001bdç\x0012¿É<à¦\x0002n[M
ñ\x0011­âVA©XË"zÅ5\x001aÚ
\~çÿöã~¼%\x0016Eî|Ôùå6\x0014!,\x0018%büãÛ\x001fù¿nßýÓÇûº¸ûøþ\x0016Qº\x0018\x0001úå-20ãÁD©4	©©T\x001bp®Ë¿{üäâõåÓ³Wo®Ï.®^=¿üçGÈß®Þäw¾¹»ý	
pOoÏ\x001e/0n\x001e6âÓA»¥w:À24\x0016ë&Î\x0002Ü¡p°/\x0012ùò³7[\x0010ÆMªú\x0010
wî!!\x000cK³ýPIË\x0008Y\x0012g\x0010"¾â¿{0ÊEô<,èlX êä¶´x«>
ñ×\x001fÀäwïÌÏÿ'â;_Ä=\x000cJ\x000c½{wû\x001e\x0015yw 6ñ\x0006ÔËªb\x001duÄ«lº¸Ä%5Üzõ9^Ì¿¦svñüñÕåó+\À{	fÀ×\x0001Á¯ËeVÕ²â&[àÍê¦\x0018² mãI\x0016ÄÛVÚÖÆ$\x000bLÞÖ«aÈè\x0013ý\x001c\x0003TÀÁ÷Ë\x00170Ø.¿àwiZ\x0004~\x0001î¼ÙcÀ¯Ì»(Ñó\x0011²þzÉ
.øËpZÿ¤ê\x001cñ\x0007~>\x0019Æÿ×\x001fþøoo\x0017ü86Í&7øèÃÃý65i#|-ÉK\x0007Ï\x000eÆ~ôâÍõ×+ÑP\x0001Oz\^/:ð¡Zð)Ô\x0010IþÄ8ZKänx?ßý\x0005î¾/Y.Æ	7÷[\x0019Xc:O«0\x0010·,b\x0013*½¡Ç¥S|Ûþ\x0015l18¸¸^#åwÿú1¸÷L¥\x001fßýñ±äã$\x0004{öìöýûÛEù-Æð\x001fï~¸}ÿööÌn\x0006ùÄ(J\x0003¾üGÔj3´¢R¯2JÒ={vùüùå"\x0003\x0017ÃùWW_]>|\x0019\x0001¤\x001dºü\x0017øÛw¼!+Þ.V¼mZ¡6[¡<\x000cêfútÆâÿ\x000e­=\x0000ßEöY¡~Íw?¿û+\x001cGjgßî\x0008Õp$wÔÄ"¡°I¡>jV­â\x0012ªa¬Ö\x0004Èc7°\x0018
«\x0004\x000c1.{AüÿÔ½M\x001dÉq¨¹Ü²ÝÌÿ\x000fG	 Yõð§\x0004À#õ'QHUå\x0013
 \x0013\x0000%r¤mhÖÃ®Q/¢v¢´[¸_÷HÄ½á\x001eQ|Eó¤R>ú®»ýÿÄ\x000fÑjX\x0016´Ç¸~øË7áÏüÙo¦Ï~sô³ÃêÏnÔÙ>û4\x00020v£å³Ç¡Ë\x000b_ù\x0015_þj´_ñvú\x0015oþ
\y-¡O¿&1øü\x0004£g\x0005G\x0004Ç±__ù\x0015\x001fÿýæö{ù\x0015wÓ¯¸;ú+âzA\x0002å	R
;ä_áü
CO0~åWüû|òä_ñnú\x0015ïþ
Óõ-øBa²´ùK0,Áê¾ß`¾ò\x001bþãíÿ¾ùáOü\x001b~~Ã\x000fG_ÿ%ìÔæC?"NÈ¿3c$ÒaÑd=ö+üW~EüéþOð7þ\x0015·Ó¯¸=ú+ìú/\x0007{Li*³ÍßB~Ã¢Ñzì'Ø¯ü{ÿÃÍß~âðãô\x0013~<ú\x0013BnUü\x0013´co-}\x0008Ë¿A-ËÓc?"|åGÌ&\x000b@,Àí\x001aÙ½üáýÝ§µÚÀ*w;\x0011>í@ÎÎ¦Ñü\x0018¨Âj;5Èl½üæéÕ«åÈÂl°\x0000Á\x0002[¸&;FL\x001aÈZÁ(¯XÅÅË3@nkr»ÜÛiBÞ¤	,UMä®\x0018cZ-Z\x0006\x0003ä¾&÷\x001bÏ<[_È}våð\x0013/Jÿ\x0001òXÇg®G\x00114\x0013<Ê+]õCû<7¾O_"jÚGª0Í·%ø¢q\x0017µÕ\x0000zóBaã\x0013
v\x001ax<¡OÕ¦\x0013:\x0017AÐuY\x000b
 7O\x00146¾QÎ4M7]Q©Þ\x001e>íj\x000c 7o\x00146>ÒXyIH²=£\x0010v\x0014éÐ<RØøJÉÙgtjÀ.~¿²~?96¯\x0014·½RHªS\x00000ÔÝDä\x0016\x0003[2\x0010ô¯\x0014W[_©ö´Nè ^µñ\x0012ûL×eÑ1\x0019QG¥þ¡¨¤ªátT"K\x0019{.òÑd×q\x0017|¬'\x000cå?\x001cV}eêÏ7Z\x000f
þ\x001cX!Ù©çzq\x0005+²\x0011U)	úõÅË\x0015ÌX3ã\x0016æP§53³£\x0006<år¬fÖ5³ÞÀjªénÇ4­>3ÇâvÛSn÷jfS3-Ì8µsòæð¬¨ËÞínØÙnavSÇ7\x001bXÆ2s(öÕöcÖaö\x0004u¨àÁ[\x001fÊf©å7èÉTÉ±\#÷\x0019Ýzÿó4·®¹õ\x0016îäï+~
Î½AY^ûå\x001cë\x0000µ©©Í\x0016j\x000f!¡VðÈa<ãEâ°>ttÛÕÜnÓ-	S	2¿ÆÈÇm°¸\x000ez½Û×Ü~\x000bwz:k\x0018L>\x001c\x0010µní¢ñ=\x001djì°é¸Äæü41°Í¯$Ù·>Ø{\x0012;E¨-Ü6w+N\x001e¦¶ë\x000c^<\x0006;^\x0013hà&)¨òì©ÚÀsjÈb(Å\x0006;\x0013À\x001b·p\x001b88\x000bQ4N\x0012X~ \x0000z\x001a¼Þ°E|»$ý¤\x0002%DÖ08ªR#³ë7\x0002\x001c6Ip"Q4ÚD\x0012;"§¹mÃm·\x001c¸wÓØ×©8Åsð\x0007# \x001c¸s;Bh4\x000flR=\x0018J\x0014B!µdrÚVd¸_vå\x0007À\x001bÕ\x0003[t\x000b%¬\x000fÆç tâuæ$Ï÷\x0003o\x000flÒ>49:ËÂ¼j/§·¬ÔEì¨{°Ñ=¸I÷(=\x0015]N5	£\x000fI+yeþË.à\x000cÇ-2ÜÅ<ØxÒ=FÚ¨ZÏà(Ä-¢Ð%\x0015Ï¡MLR/xp2Þó¦4\x0012\x0005·H\x0014\x0017pêKÓl4*Îº\x0007¥JÉí(P°y¸å]:7HO:S³óÔù]êJw\x0004×ÍÓÔ[&µåÚÉÇ´´ºExú{\x0016áé'ÄõÉæÓàÍ
×n¸ÖrS¨\x0016Ýò[dó*y*;*MÝ\q½é'¥	l^)E¶	Ü°W1\x001díBÝÜq½é§\x0007Yi*g©×u\x0002ç\x0019\x0017	¼ÌÞ\x0003Ü4wÜlºã>gC"WÙ\x0010Gïå¼qÏó6ÍE1[.UqÁ@OffMØÎsA\x000e#9Á\x000bÞÄ½ó%çÆ¿Ñ{ÄI~ IlÓ¼éºh\x0003rÏÍq óÃ6|Úªk°äQÂ*PrÉ»hP3\x0019\x00123|yþÕwºYÍl5Ü}\x0010ÑVì,k¾Ð×WÏ\x001f_½¼XC51\x000e\x0013Ó%¼Í¥N\x0014ýBßp\ß÷\x0000ë\x001aX\x000f\x0003'w \x0006ÏúR\x001b²&pGI\x000f°©Í00hñæ5\x0004)¼×>Ìßr\x0005M/±­í0±>\x0004|¢)3*#vGî\x001ebW\x0013»Ab\x0013£KAÛ±\x0014c<ìFìkb?~+D1(æ!S\x0006~¿w\x0017jà0~Ä\x00046MgåÜ ÔÔz¸\x0013q¬ãð\x0011«ÉïÊ\x000fOIöF|Ç\x0000G
Ô\x000eâ*Ll\x000eaâC\x000eî\J6´5ÖSÇS=À­¾\x001bWx4ÇÁqib/G|<RÙCÜè;\x0018UxTærn9df¦Zå\x0017õQTx¹¸®\x0017¹Ñx0ªò¦§ÇVEÂÚ4mAN9\x001e÷m{\x001b\x0007£J/rä0\x0019Uäk9d-¶\x001bî&Þ Ñy0ªô\x000c-¢BLQÓF\x0008hmÉ^ÈÒq­ç\x000e"ÙTCiUÊçÊêíÈÖQµî\x00052KZzËÈ(ñ%TÇ}\x001eäFïÁ¸â£Ì¿\x0014âR£T.»_¶#7\x000fF5_º\x0018V\x0012\x001dhÃÇ\x000c¦èêÝÄ26\x000fÇ5µ\x0012¡Ö~ZOY\x0015oo­ãôÕÈÛè=\x001cÕ{\x0019·t%°ù<êÒ[±\x001a÷ä\x0001·~Þ¸Þ£)ÚR¥\x0000
ESj³´ß
¹Ñ{8®÷4\x001e^§XÆì¼tàr\x0017j/r£÷pXï\x0005Ú\x0005 ÅØ®ô#°0x4fÔÜ(>\x001cW|hKý8uÏñ0\x0001\x001bÊ)\x001f¯ÌêAn\x0014\x001f\x000e+¾\x0010,±J!o²Nùx ´\x0007¹Q|8®ø`ZQ£Y@6s~~±XDa/-\x0016Áq-\x0002 \x0001~ç\x0013eäCÁÚË¼ÐXÖãb|é\x00122ÌÉ+jÿ,µAÇ\x000f{ÛhÖ°J
r±\x0011l)?ÝÍRÖÀÐÃ\x0002#\x0007¥K'WÒj\x001cy}j/\x0019§×§_\x001fM³CÁ¬Ê\x001e\x0014Ògv\x000b\x0005èÆìÔ£f§U´¤JF0D)\x00173¥\x001dünñ\x0016Ý\x0008\x000c=,0W¥ü
!\x001drñúh(Ø^Q¸&Û0Eâ$Ûð[\x000eÆ¡s'y\x0018|òM$zO%\x001câRºÜëã5§Íf¬'ßæ?\x001cJª§ù¥ïo?FQ®;.èp\x0007µô'ÃùD2p\x001a_úôòõëÅQ\x0015·®¹õ\x0016n¥J!JÓNF\x00181µ9Õ$ÐEmjj³ºÔ¦\x001b"Ù\x001d/!
}<>ÐIíjj7N=\x0005	¸A²hù£\x0019$¥2ùDâ²Û×Ü~\x000bw°Edç	q9¤Ê-9Q«Ô\x001djì°\x0005¶¾C\x001d¸\x000cûñ%iyjÜA\x0017w¬¹ã¦kfNÜRC¨§¼0sªïíáV\x0004n&ºÒè0KÜÎ\x0017î\x001d	4"\x00106È@C\x001a=\x0016i¢ýñÉ4êDJ¾\x000bÜ6àv\x000b8-á4¦émÅÒ{
\x0014h\x0004
l(_ðæiÂ¦·	^"É\x001dàyRäKB\x0016gYzeá\x001f?ßÞ·òþ0\x001fLrq¸ê4rÿTÞºÀï©Bc\x0012NðÂ\x0011x|Ìê3ý\x000eÎpM¥àªÕn\x001d>Ô\x000bJò\x001f}É?¾ÿøáöýÙû»\x000fWÓ#G»9\x0019~\x0001*\x001ef»êñ~söøÅÓ\x0017ÏÓÿ×ë«ç¯Oÿ\x0006]ÿ\x0006½ý7(ÏcÎ(Åf¥Í-\x000f\x001cþ	¶þ	vóOðt¿¡t?W_¦ofÿßàëßàwø
F\x001e1 9\x0005å%\x001c¤,\x000cÿXÿ¸ÃUÒâá%`Úùï\x0012\x001e¾Ã©Á$Ý¿\x0001Ú'½ÇÎc¶éG$ÿ;$AIc\x0010\x001eihêÿ\x0011JÏäÒ³Fü·÷·_þòñî¾Çb	\x0008E¥$\x0016r89ÔìéÙÅ£ëË7xqu}\x001a]×èz#:g*\x0018$k"[÷R¦
Á*Óîb·5»ÝÈNm{±\x000cÍð\x001cö2
;ÕPÖÅîkv¿\x001dJ¿;x	9ÒÒea\x000f§ª»ØCÍ\x001e¶±\x0008\¯­1Q»¼ÛJ!'g Ç\x001a=n<v
åÉç%ÍRJeVLÍX\x000e­Ù(eBFfåsC÷ú}Þ©Áx4(âñùÇ/¹í(ÑV\x001fÆð*ÚêÃc¥êD¹óó\x0017oþpy¢<\x001bg\x00121ÑêqZ6\x0007È²TAh\x00056\x001e=à\x000eØ6Æ\x0005gýÌ:\x001eú2Þ\x0017Í©×Ë¬¶fv\x001f¬©ÕåÍÙõíç_î?t\x000f\x0007iÅB\x0015$oh@*´U8ÙÑD\x000bÙ._¿xsý|\x00059Öä¸¼LjDôÜmÈ¥\x0008\x0005ÔÉy\x001f]äº&×ÈÑ×Dk\x0015"ÏTíopRSöÜl#\x000fC¤´>Ï)sÑõÉÁ0=ä¶&·È)WÄgnæÚi!7û¹«ÉÝ&r(i#\x001a0\x0010$áå¶ì­é"÷5¹ß@nb4\x001c\x0001íx2l:=Þ»\x000b;ÔØa\x001bvàºnpXÒtÖJ«äéÉ6]à±\x0006ÀC)Ë\x0003T%¥!6É\x0000:itWeô¤Ô6òXh\x0018S$¢)èz×;\x000e­þÜ¢@\x0013º*;r(íÈõÞZÚöôÉ!j=àú-ú3ëóÀ÷<¹?å¶Xé\x001eÇåØÝ\x0008z£?a\x0002rl\x001c*\x001fer­æíÈf\x001añ°#y£?a\x0002Mä(3wAé÷T#}Ø§º<»È\x001bý	[\x0014¨NÓxégâ\x0005'GîNO\x000bì!oô'lQ \x00139OhVÉñAA/·eEP¥\x0007½Q °Mº 1\x0015¥cÑE÷õ%t}:.ÑÞ(QØ¦EmÙú¢èÒ»ÉF.ýÃ®è\x001amzÔT_Ó D7k" pÜ\x0011\x001bEÛ\x0014©q²]CYU*e\x0000F³<?u\x0004½Q¤¸MÚÒÜ¬h\x0000ÇTtðï«I±uD·iRm©a?\x001bihEj¼eò½\x0004\x000cÌ½(Þÿ³ßß|yK{òfÐ»V\x0017\x001e\x0001Z)kE\x0013Ä±ZjD¸9~ßßýþâÍ´¨)ï\x0007½zv,\x0015É¿\x0002ë_;ü
\x0010³\x001d
ÒR§<³\x0019Ë\x0010\x0013£\x0006~®ÞáG$KÌÉ¯0ç.¿_k\x0004¢ñD¹ÉÐ¯0õ¯0{\(W2òþ\\x001b¹OÅãÆ±\x001faë\x001fa÷ø\x0014¡Ì.0ÓÒÖü)J\x0001Í©iVC¿ÂÕ¿Âíñ+´d·Q©ýÖhT«8ô+|ý+ü\x000e¿ÂuyÜÁô#¬ã\x00038^«<ö#Bý#ÂN\x0017¢õ|äU¨ð+<íXÿ¸ÃðeN'"\x00141\x001beÒ¹'¦Yü:Ô\x0000PÃ¦\x000b\x0005¥²fü3¬q%xü+üVqï¡¹} µ\x000cf\x0019\x001c´\x0012=Qê<ô3\x001aÍ
{¨îdu Ìß3Ò>aÄ
A°ý~F£»a\x000få\x001dJ\\x001f¡ì¥)¥ò5~_ÑènØCy;ä|2=w,kK_:ÑZ?ö+\x001aå
{hïh\x0013,çµJDÑÑô2Îký\x001a?£ÑÞ°ú¦	·%
N´Eð¿ÂjÔ7ì ¿Q\x0005<HSüøeè²\x000e\x0018½~E£¿a\x000f\x0005\x001eJ§>*\x001c²\x00158\x0018
>ô3\x001a
\x000e;¨p¤ª.NEY±âlIÌø\x0013_\x0006Ç\x001d48ªHEíùWÅHNæ+ÿ+¨\x000cl\x00148î Àuò\x000c/ú¶ö@Ð¯\x0008¥Xm ·ûÏh]ï=\x0014xt²¸ºR\x0012ÓöÇ§¼ýF{ã\x000eÚfCHVZä\x001f\x0011t¹QöÄf¡Ñ(>ÜAñÑ,* u2\x001a' Ô)}¢ cèg4\x000fwP|Ó<cÉzº\x0014W\x0016È»_ãW4\x001a\x0003wÐ\x0018H\x0010ÎÈ\x0006 >ý
/MfÊÈk\x000eýFcà\x000e\x001aCG]FîSz6ËÚ\x0010cÉåØ\x00150ò3t£2ô\x001e*C"l]Å»Ñ\VÅi÷î?£Ñ\x0019z\x0007TkAG©Oÿ\*Ôûë\x000cÝè\x000c½Î@[\x001aÐOgßÕ«âhØ_Á\x0005×Í\x0013×;<q\x0003eþ&@\x0019c\x0011Q\x0004:1Ê¼ïWùÆ`\x0013«ú¿÷\x001f¿üåæn}óQòØ2ÞÈ:5%Kwµ>ÕÛxöòúÅ?¤¿FÖ5²Þ\r\x0015Æ\x0007Êª(Æ\x0006Í\x0011ÝÙÖÌv\x0003³/­-ÁH*·SÓñ^Ì¾fö\x001b£xl&Ýóx\x0008%³´9¹[`=s¬ã8srl²@±ÉßTÒ¸Âi8º\x0019»]gh_à'd\x0006o\x0007´Éäñ\x0002-ª5<»34o\x00106<B\x001aÌ'HUD\x00134HôôÈ&ànææ
ÂG·¡NÌÖ)\x0006JZ<:ä\\x0005óz},õúïh	ã_nïøp÷}Ò4\x001dqeó1Å WA\x0012ZX$pvùËëo_=NJæX+\x0016³cÍÛØrToÙ£4ÏO{Iýx\x0019/»®ÙõÖsRØg%À*ÈjêìÞÝÔìfã¹çT_ÖV@\x0017Å~|
æ\x000c}iÚ\x000cÎdâ¶[ïKI'ýBó}¹ÕúTú»óÌCÍ\x001e6²\x001bÏqs«OÜÃªÃmS}äUF$ÚnÌ,NÀ2T\x0004D¡4*;\x001e{»}b\x0012¥~øµê"ic\x0001Ò\x0002-\x000b2OD\x0003×þ\x0000°3\x00194Ò¡vèñ7÷ï»\x0016gXåÊb\x001e\x001d¼¸\x000fé'È\x0018.Zûu\-¥¿_?=¹:\x0003æÓ V4Dnc\x0019Ó,DQjJÍ6Ú\x0013nh'¹«ÉÝ6r##£Æ\x001dÿFûÒ[vÊzéâ\x000e5wØÄ­UW\x001aKÙ³Q2?Ì\x001d\x001f2×	^\x0004^Õ÷\x001fö£dÛ²k¼ÌXØçÈõ¼ÉLª´ì/¿ü|öÝÇOëÑÃÇÜA¼ ëJÏ¤;>\x00084y÷ß¤ÿñÝWG·Ñëy6U\x0019V?¶
Aª@5í;æ§Y¨OLÖ\Imæ#E«c\x0011w"ÜÖ§æ`©\x0012jëC	Ï¬\x0000}yµBù\x0018\x0011ãêÄ\x0000·ÉÇà¢\x0018[Ö»Õ'C\x0012\x001dÜ¦æ6¸Ý!Ä\x001eesõâÅ)rån\x000f·­¹í\x0016îDWZùb©t¥YÈ\õÕÃíjn·é¼eÞ--=äì±õª¤4N6Äu`×KN\-½GÎ»l´\x0000\x0007´ÿk¥\x0004Ü\¸Û\x0003
8n\x0001×e "í­å0-[kO\x0014
öa7Ï\x00126½KS6\x0007öm±eÿkú\x000f8\x0019Çê\x0000oî7lºà\x0006Êy£\x00127ÂZ,ÍM'¼ý.pl.
nº(\x0018D+ïd~Õ(\x0005üþd[V×ÓlG\x000eLÏ³Ú¾7vÑYßÕ2ò&Ý\x0018Ñúä\x000c\x0015üoçÃz\x001eñ°§w·_ÎÜ}¦ÞGéßq{ö\x0007<ôyµ½â,JKQËí$ÑM²Ã¥CëÈÅ§WoÎ\½¦\x0016G/?¿<û\x0003Í\x001ez½l¹ßõïÀ\x001d~O\x0006:oM6Aå\x001aÙ¯ªK÷ÿ\x0015ºþ\x0015z_2ÙÄÒÀóü1è5äá,ïÿ\x0019É.»ÔÖÎ\x0006CÜýåîÿ÷¾k®¼¤[ÐH%çaUãùÕ\x001f®.¯Wp»ÛmâHq\x000b	ÚYn#*âsE:®\x0007<Ôàa\x0013¸.µ\x001aIJ¤\x0014KÞåäõ\x000elhî	l»(yÎ\\x000e{9Ib²D\x001dO¦\x0004zÈMCn¶\x0017ÓÝ:#Eº(û)Ì©¦à:ÎýÒØÎ\x000fyäÊÍ\x000fë;å<%ú9á\x001c¦Á3SNdÖæDL}\x0002$ÊÅ7G;åû¦4ÕÕOºI~4yÕÏ>~y÷aµ¥UX2¦Sf XH]´\x0010®½¼H4¹ÕÏ^¼yzõü47ÖÜ¸;y\x001aZúÉ¼¤\x0017yV¸õ¢IÖÃmçcü¬®Ææ;þËÏî>}¾ùðýú8WÒ¹¡¬A2\x0005½'Gsrgå««W¯/?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þç4ÑÒh.ÏjýÃúKªh	ÿÛ&F«ô_Ý¡Y8Â\x00167ýy\x000b®;$¥upÜ
¼»æ¿\x0019ã7æÃ§"O¸YðëâöñÇÇ¯-Á\x001dv\x001c\x0016\x0006CEeha|AÊX=ð\x001cuqvùcûÖ4ÔAH½)LÃ\x001f@¸,°ÙÔÌmû|\x000b2ªs¼ü\x001e{J^cM_çº\x0015õ6ÛjèJTW¢º&Ô\x0010ðÐK£Ã\x0004)¸o\x001c|¸{@å¬Dg\x0016VF¹$V©ÕúÌ: Å\x001aX;'7\x001e\x0001û¨#«M7Øp_S\x0006\x0012½U¬¢(PÄ\x001ftëN_ÝÞ}ÞÉÉux\x0001ïa\x000c<£HU~øVò)f9±þüõ\x0004FW2º\x0006FFyaTøÝ¥°\x0004)^÷ZÈâ¢²2 Ñ¥\x000f+RPÌ£i^w\x001b%³J-üAw%êáÕ\x000fëÝ9*Î¢ÍÌÒx\\x001fí ÷\x0010Ó\x001dA¥>uÝ6ËQ\x000fß\x001c½;\x001e­p+aE	++¬èKVØ¢\x001cïÕíãP!|z+)K\x0002\x000f¹\x000c¨áù½}à\x001d\x000ekó^]\x0017$'Ó¾ûÙ7s©·>§ÒÄ\x0003\x0019\x0010
\x0016¸À\x0012\x0006L\x000fHë\x0007z²\x0018qXõNLQbzLØ;iS4ÙOµÌá\x001d4N|\x001e¦,1e\x0003¦ci'\x000b$\x000c`Ó¡48©\x0001\x0002Õ\x0001÷¬\x001eÓ¾á£Ã rüèÎÁÆ²(MlF¼æ\x001eÉ»G³álþïH\x000e§©çT0u\x0012ÖÐ\x0016m*Òùµf h©ÀÄîÕÍÙ\x000cÛi\x0002õÝ!~èlå\x001ehøð\x001aK9¬\x0003)JT\x000bNR7
¾C,1º¢»ÄÕ%®nÄÕ^\x0003TybLöÜ;_Ëy\x000f\x0017\x0013zUý»T½§j&
\x001c@Õ\2 ÚI5þ%¦)1M\x0013&ÖÂ)$&`+oÉ\x0019\x0011î©Ù¬Æ´%¦mÁ41:JÒtT\x001b¦¹Å³Y¸ó ¬D\x000b'Wë:ä­Æhà\x0007Êûª9;âäMò\x00142ux¤À3å,C¬AnÍ\x0007ªk9\x0005/9ÅXoÌöü\x0006eÇâwÇ¨Sa\x0013wüîãaÇdNÙáM¢#Ø(ÝR©\x001e*{­Æìè$Ñ¤`ºÍ·]\x001bäÜói\<\x001dS\x00154øn£êÛÛû	\x00011OMØÀH¯ö\x001eè
ñ§ÞÈ&<z{vñn\x0002¤+!]5$LÊÀ:­ýÁ\x0002$z&×m\x000bá¦1\x0016&\x0008ÕCZÃaÃ³Ò$¯.ülükO\x0014\x001dHÑ\x0000i\x000f¸Ê

Ñt$\x0007Ò\x001fÕª\x0003©ê!K\x0013\x0001Rç©µ2\x0004)çÉÂñ\x0004JÓ@ir°Q9í+aÚÃ¡ì\\x001cÞpsL®¡\x0008\x001f\x0019&y%Kn2å@¸Rt®h¸:!ö¥òox\x0014ÆtôùîØq·h2eçXc	é#ºà\x000e\x0014R¤ä\x001bÊ=Òv m5$<\x0000f}\x001eHD£õÆÃ\x001cw&Sv¥h8¼ÐR
ã
ÿÁeçXÊcÉ\x001c¼ &³\x0013G%wQW\x001eË\x001fÕPv¥¬?°\x001cÅ\x0010%ñeéQ*C\x000eÔ»TCv¥¬WÌù´B\x0019²°Y\x000fÅÑÔà1_¥ËÎ±õÇ\x0012&Ébª\x0018æ°ã©4£\x001cx<\x000e©ÙûÔN°ù\x00014\x0016ä±'ëûÅÛ_ïÖ7ë\x0015ª°\x001aÚ0B\x0014q©\x0019+H\x0013Áð>hrt±xûó£Ó£±\x0011Y%­)iM#­Ýø,\x000en¸.·\x001aqýô\x001eUâb«{\x0011[è'i\x001a¨ä^]ÝL8\x0006&-\x0005\x001b\x0015»oÒ9Ø\©éNâ\x0003ºÇ§[£~Îû\x0001à»]¯®U²ib>h|\x0006SÀRVIrÒø[oÓ\x001bÇvIB-ãK\x001fãËzVéåA:\x0008\x0006âdAdôj\x0010ÛÚQ?\x0004\x000f¨R´/À\x0008¨Xqpuó°x½¾þuW÷E\x001c¸¤\x0013d\x0008\x00021Ø`\x0018a
ÞÀ\x001bÿñé»Åë£\x0017å~`"ÊÑè\x000c\x0007åÒà.V?­w=j0/Ã7Ný`:Ü\x001bj.\x0005ñÍ_²BÔÄw±¼üæèr¬\x000cÊ½ÿö§Õ\x0017M\x000f\x001bqÅÕÇïn\x001fon!c\x0008
\x0010Ð*"Ó|Íp¦"Üúá?bÏÿ§«õ#\x0000J	\x0003jpQ½±?UCéhÿãEÓîÑ»ÔÛÿòøèò«·Ç_]AÚ\x0010ú!ÎF¾s\x000745ý\x0005@S\x0017Ùs\x0005ýåúòåªøô\x001b	\x0002&¹¥±ráÿÃ.q\x0000ä*9JÌ8¿y
ì\x0000nþn\x0002XúÔÏ\x0010,õÝ>C°Ôû\x000cÁÒç\x0007F
øudJÑ\x001cC\x001e¢W£\x0013\x0019Ãá²&\x000e6ÞN6Ü§[QiX\x0015\x0019×Fø@å.\x000c\x0016âÖ;ZMÇ\x0019WóÁ°³±\x000eÌ\x001aL
ÏwJDAÕS"+\x000b\x001fÛÉ°ÃªyEÛ»¡C>NÈ\x000c2\x0013´Ã©Çl\x0002\x00196XÕ\x001d³\x0010Ùû4`\x000b:cl²\x0002Ü¤\x0002õð§u÷Øf2¨ÆµÕZ\x0016ü$3ÅtÜI\x0019>f\x000f	}óÁ¾°:C8W¨B·a\x001cêÉ­¦ÅAÆÍ;V3c_}\x0005¿êÈ?0é\x0002\x0008È%E0\x0003\x001d	Lùß «À`µ'neº>t¥¹AÍîAbá8¸ÚCÆ\x0015§¨Ù´\x0000\x0019ª\x000cã¯Ì¨¼½NeÀ~¤eÃáJ¬¹
gÏ¢Èhäa=Ùýö_\x000fëÂ-ÖÂ¯W\x000f÷\x0010u\x0001Ï$ÿQãX\x0016XAïàªFÿQÒ;¯ô°ÿ\x0008­_//ß]@ô\x0005ÿxÔ\x0016 4\x0012¥	\x0014Ç\x00028öÂx\x0004¥½\x0013!@\x001cþÆM 4.¥\x0005¾\x0002¨KCè\x0002¨ Å[¾x¡\x000f\x0003(Ú$êRµ\x0008\x0011l,\x0016 ¦\x0006g`XÑ4ÒÌ&Pô\x000e:xÕO ´\x000fÒ{6W¢?²ßn¾ý­8£/ot\x0010`F\x001fVÐ\x001f>V\x0019¥1A\x0015q\x0019ç3sïTJh\x0005ýfÅð9}yö\x0006ÒB\x001aøf	ýâSÓ\x0019xöÄ_\x001eÕÇo9\x0016 }\x0005¿Nþç¿þ{y÷y\x001d'îÄ\x0014©·6\x001e\x0003xnN\x00174¹=¸#\x0016ûd±<}t:ÖGPåÝµUdÜû´\x001b!9W>\x0018oÜ\x0018ü\x001d5r¦Ñ ç"³õÍ£üWL_Ð\x001eÑWw«ëI\x001e\x000e\x0013©×T@[ò\x0001O®ò¤xÔ°Oøê|yz8ÖâÞóëïì\x0014}³º¾}XßMÊ¤Ä5P¸¨Ç\x0007ÍÈ\x0013¡=ú]Á54ÃXo'gïÎÏÇÆ¸÷òf-îÒ0\x001cì»z»º[}+Uvr	ãÓÄ	Á¹ðB\x000fë]Pé\x0013\x001a­]·ËóåËã±¤£{ýá_>}\x001bOýfYr\x0000û8å`Á\x0019¼Øx®<KC\x0013Îàn8\x0014°åùá\x0014¨Íîä©PÚTó\x0005L§±´q9©&M6jz·SýøùêÛõ\x001d_kñööñi\x0019:GÖË\x0008VÆòØ\x0003\x0019:gÇ¡Î.ÿ>\x0001
^\x0006¥ª£vï¤óJ'À¦â¦g\x0017Ô\x0011Å0j³|2\x0015Ãü:¨«à9'K\x001f"\x000cMêJ7A±ûßnbúÚ\x000cOVóõ'Ü\x000b´+èò4á\x0001æoX\x0018\x0005\öt8iÜó¹\\x001f½v±õæ/UÑá:` óPKèHCHË5×\x0004:î~rëQuá\x001c¯óÛ\x001f\x001fõäZ\x0004ßBÀ\x0015P^ÂaÉIjÈÂµÃjâüì?/õ	ÞÄ.°RlÏ\x0004íÃ_¾ÿø±t'.n\x001fï\x0017×ëN\x000fÍn¯BrJí\x0003«IÚ,\Lº\x000cJ\x000c\x0013^]^,ÂØtÒì&?,üj#\x0015Xý"\x0018LþK×Ös£ðz°bîlR	ÐB*=7©ì\x0012\x0014L,¼WâqðöH#RÛH'\x0003«®æx©³
gkØlL'½Q>òô(\x001a.JzçÝãÕõ:uKî\x000e\x001c¸YùÀ\x0018ü£´¥\x000c\x0006Õ\x001b\x000cÌ\x001f3mËÅ»Ëã\x0013\x0018m6JwõíÝÝÃc'mPìáÞmJ \x001a\x001d\x0014fÓº>\x000e+çÈÀo×rî.Y\x001e«ZCÆXZ[\x0016nÅ½é`ä8j\x001e®ä¨é­@£Ì@
õÈU\x0018_ãÉQáj\x001f"ËÃ_\x0019WÎ]uÈTZ´\x001bÐ¼JKÖá9BÓv,{V\x0006/1¼ú[:hÑA¥,ãÆ0Ã}3>Þ©a\x000ba\x0003·ÕlRÃ[XbÓi­E`ãt7ã©Ùhá\x0016qW\x0016<(Î\x0011M¥Îà®[B\x001bIØÖ¡\x0003\x000b¿jÑlê\x0010\x00024VÜÆHÂ\x0010ÙÃi+\x0006±WÝ´\x0014î¨Jë\x0006!°áTÀÇ=÷
´p*D½¾å8Z\x001b¼\x0013{@ÀÉ·~\x001fhá~ú;ÊL\x001aU\x001c'ÇÑ\x0014xNlc£*¶p*D½n¨\x0002O\x001b\x000c'§{@h^Fø\x0015há2jõa­('úF^¦\x001d&Al*ÅÈÆ\x0019láêK
kz$6î¡3²IC\x0019·=Ø*¨WÕW4DÑuåßéZ^|Ñ0±-
Éë¥fÉ[ãïÑÆãì¥¨v÷pÚh\x0002S%rxC}Z{\x001bÀ°\x0007Á\x0010¸f\x000bdEVúAw?TÙO6A¸4ò'°¦.£¤é(

cu3yÉöÖ²\x0002YÈâ/¬Kdý¼¹ï\x001d\x000c\x001egH,¯¯ÿ7­ºû\x0014þwV¿Nó·XJÀ\x001aÇpi\x0008&ýðõZ¿¡}Tç/ÏNOÿØM-Jj1Ú;xËOoÓ,¿ûùü@¹WjYRË\x0019ÔVÐk5\x0008	\x001a;ãáUu$]ß\x0004­JhÕ\x000eíMN\x0007C1N\x0007Ä;ÔÎøáCÝD­Kj=ç\x0004ÏH\x000cê,Òù`ù\x001diä&6A\x0012Ú4C«àW¤þ jX!\x0012\x000f\x000fº\x0004©ÝXb§ÚÔv\x0006µSd à¨A<\x0017
«òØç±v%µq¬¡b/\x0010|£²æ
Ê96ò ÔDíKj?GÖJ]¢¬9Ê\x001aÝÛýÊ\x001a{ÉÆ°\x0019Âm4\x0012-¡ï,é\x0010\x000cfBT3R¸ÙÝ5í¶1HÛÐ\x0019ÒFaS\x000es¿ÂîFÞn\x001b\x0015TáS§ÐÎ\x00084~ ¶\x001ey¿kÂîØFÞn\x001c\x0015\x000f\x0012ÆÜ§\x0002'Ï
­\x0000vRíOeóáíFÁ(_¤V±ÿ<R;:"j$Ðæ=½ÿ\x0010\x000b\x0003
\x000f
~Ð|+9§4 hzñ ¢eÏGª¼Ú\x000eJ\x001f>\x001c\x0019ô
ÊùSô\x0005møÀ °c\x0019Ü°°Qò\x000fqÆt!yøA»#èSí'ÀcúÄrÉ÷x?Ùû=-þqÆY\x0017Ó\x0016ãÃS8ì4\x0012û³üCüC;9\x0017\x0014Ü`y¾\x000fÿ~Öä#\x0015¢möçÉIç³Núÿ¦\x0019bO®é¬[*s©;¼*\x000cÔ°\x0017J^Õ^®©ì\x0007Å²;XñÅõjRUv8Ã\x0007\x0006st\x0001Ðc\x0008¯q}5d«\x0007q7£á^,Ç{2©*IU\x0013)×àk§â!²Î@~\x0013ø°½¬EÕ%ªnB¶xÌø8Ì.¢úÜ\x0008\x001båöjJTÓj¤ïkd#*ívp\x0005÷êJT×
3°NËrª&×ÞâQ\x0015B\x000fëJÔ2\x000cH³t[X
M&VM\x000fµÚ\x000b*$\x0016#\x0001@õ½êª/¸[ð3kÄ\x0001\x0003­á%&ê\x0001AEpóý\x0000»>°k\x0005\x0016¼9\x0003{«P\x001fP\x000b\x000eXýè\x0003Ó'6­ÄÃÊÄt(\x0014d>R\x0002ÝS¥¨\x0018ñ?'\x0013«~®Ty\x001avöÍÕÇÛ»Å×§5S\x001b¼Â\x0001v&UT\x001aiA\x001fß\x001c\x001f¾;;_|}ùz¼:Ã\x0012V4Â²\x0003|1¥åÝæ
\x0017\x0002­a\x0015V*KTÙêÒC`õ\x0007§Ó¹\x0014G<×U³êU·±\x0006-ë¨4ÁÂàÐ\x0004Ï@1?e\x001e¬)aM\x001b¬²ÔÂ\x0013qb±\x0002=55ðT£Ú\x0012Õ6ËÕc]\x0005\x000c\x0013ô$Wªg\x001bi\x001e¬fu%«k\x0014«¡l¸æ\x0016\ÔÂåò£ß+S
ëKXß\x0006\x001bì\x0000G·\x000f\x000eðí\x0011vO\x0007¶p\x0011ÏS\x0010«E{`µ¸D\x0015KÔPw»\x001fØ®9h´\x0007 \x0000\x0010	X\x000eÊ\x001c=ÙæÈjÚ=à\x0006A*XZDË\x000f\x0008V\x0011¬\x001bÉT\x001fÚnè\x001b­-ü É0Ø\8l$U®;c\x00069\x0012²Og¼ç\x001d\x0004)tæ\x0013½\x000eîzñæj}=X2\x00022\x001e\x0002\x001bF\x0001\x0019Çµ:ÌBp«;\x0003çá¯oNvc\x0012[´c\x000b/ÒÙçªR8´¢&l¹Ã5¯Ã%¶
!\x000fN\Ð6cKG\x0003\x0017Øvß±ZÔj\x0006µÄéø°ýÀ\x0010uPmA\x001b+Ók£Ö%µA
É¾\x0004\x001d|_ôÓ9Ëc7ÆÆ\x000e´QÚ´Sóp9\x001elKåVÖ{EGDoO:ÔQÛÚÎ¡¶ù\[]÷:C\x0014\x0015µQ»ÚµS3bìñ\S{õJ\x001bØ\x001bßFÝµ2Qk\x0011hõñv\x001bøà5ck5àH9tã­ìÓëyôÒ\x001cÐ)G£Fñ4ÞúVý\x000c«]cy±ú°zÔ\x001c\x0012ä­Rl\x0002Ï±¦:Î1±d3^t¥m//ïF7j\x0015À¢\x0004\x0016mÀáVÊ4á\x001e^8F©°h\x001byÕHA\x0003¯,ye£}8\x0013V 
Í\x0016±\x0002ß;\x0017#Ý7
Àª\x0004V\x0002\x0016B¥m,0¦\x000bæ\x0011¢]äyL×Þ\x000e.yu«­K­\x0000AÀBC§SwG\x0004ñ½É×¼æùË×¼¶0.\x001cãø\x000ccQ4µÊ»½\x0001»\x0012Ø5\x0002sØf\x0003¸Á9sÖKA£v¼\x001bUðú×·\x001eä}&^-®áß\x0017;2¯¬·Ì
t\x000fênã©\x0019TÂ\x0013l­¤ÅN×y2qÇfðF£! eÌ¯\x000f³þ|Ò\x0011!®"\x001d!Gê\x001b;J7jÿUâÎ­ã×î85ÂË^\x0011×ë_V7îÓöx»'´ÏÈó¶q"Tê¢Ö\x001e.·$<'G_¾<\x000fnÛåq\é¼\x0013\àb\x000e8÷XT«ú\x0010\x001e¹1 
êcKJ¦[Ür\x0016·ÌI[chÎuêòåHÝJ#¸*ÁÕ,p«\x0011\\x001c$«\x0011\x001dÊi\x0000×%¸þ\x000bIÜàf\x0006xðà\x000eèj2è
L
ÅÞÎäÈ¤FnWr»9ÜNQé8¼MaÝÕ"÷Í§£ë¹Ë\x0000óýà\x0004Îc=Câæùí§¦\x001bÀ;ºÏQá\x0016Â30u\x001aR³Onæ3#I±FðNásõjÈ×8\x001233jö3#õÁä3Îç\x001còØ_"·yd²uúuõÈDóV=Þ­t`XLòüÕ¹p=\x0005Vïtw`ç\x0016Ót9}¹¡vôÔÅÇJ¢ÊuØ[\x0017[\x0014È²DÍÈÃVdB&óã7\x0003\x000eFæ\x0016¶ «\x0012YÍ² nR«ü®<6¬XÄº]È>MãN\x0015\x00068ù
\x001aÓsÁøm¬E6%²iGfÙóæÚÂÍß<î\x000fÙÈnÎ¹`4¢ÁK]×
\x0007coG¹0ë 0X;3|2æëd\x000332ó©\x0005YtÅóF\x0016}µ,ºUÊ·×OÐr|\x0003³)¯¦kKY'\x0018tp®s\x0016gW]íáÙÉâåâè\x0014¦T\x001eïF\x0017%º®,§¤$´p(³ÖÃC\x0011£\x001dy3½,éåLz(²ÔIö\x000cv$r¬¿Æfoc\x001dßþÜ_¯J|5Wø\x0006Æ\x0004 Î\x0015¹ç7
=âx7ã\x0012ßÌ=ö°h\x0018 7;E\x001f1Íô®¤wsé ÙïBX
3Ã}9¹WúR±^	w\x000b¾QTé"ÞÄâ'\x001aÒ»;y\ßQ;|®Þ1Î&W\x000bn.zxs)æ4ÖL¨m><Ý\x0007ë¨õ»%Ó-
ihK\x000bÆók>®q°w}¿Ê¿ÿ§\x0010óÿ\x0014Êá|H°\x0001\x000cÊÁ£
	B¨Fº>ëÿ\x0014Í×é\x0007õMÛÔRÚ4S,g­É££(ß"ÅH=8r§Õj©Nm7³(Å_YÌª9xº\x0010¿Å&\x0001èÃlE®\x0010\x0017j{­@\x001d´)¡Í_CÐ®dv3\x0005ÔÜFf#iS¥æN'ßjR+¡;
µ\x0011\x001c~ÐzH\x0014§P\x0014÷0¦\x0006³<sÜïót[v"{¡\x0007«Ù¡\x0003\x0002å®\x0005Msµ´\x001f\x0019eSÇÎûGMr~ûø\x0010ã¥ÃÕýÃúúfõøiu7y.ö(sMi!O\x0013^\x0003÷ÈÓÛùÙå»\x00184\x001d./Þ\x001d./_.Ï·6wö\x0015

¥\x0019]q\x0015»7RLí\x0010ÝsÇ'»I­è¦D7³ÐaÁ
M)Öø\x000cîEÐ(4¥Ø$o\x001bÑmng¡3zZáÀ\x0012Ç\x0015\x0017\x001eTÍ^É}IîgÃã
	]Ñ\\x001e¡T=?ëoC/'ÀÑùK±Ë\x000e»Ã\x000e\x001e!\x000e21&åd|P<yÂÃXN¦</Èil|³z\x000c\x0005uc6«GFlåècyëEí>VÀe\x0015íÒç¶U)ç\x000fK''\x0004J\x0013\x001b{­¨ý\x0013¨~bÝäÒÔ%\x00116\x0004B,ù
~@^¶³+«"vª\x0012T=cPSç\x0008*U/(
²r_üÉêñîêf=e#\x000c:ê\x000eBøKã\x001bÆf\x0016X­2l\x001eË½ñ'ËËóãÓÑ½ñ\x0005¶,±å\x001clO?J\x0008\x001cF\x0016°sÉa%Ý­KlýÁ¶%¶ýË`û\x0012Ûÿ5°;Ö\x0010\x000eI´­ä!ú¢Ñ^JrôA\¬áMä#Å±àºÿ¼¢E·EáÍêúnu¿øýÿYl\x0000'uO
\x001aÅ­?IjÌ;ÜÆ\x0006ðl\x000cß,OÎ\x0017eñ\x000fó£Ï/J~ñáÿÐLû\x0002'ÓÖ7ã\x0018ìÖ°pXá]#Éå	],\x0019Q¢\x001a\x0011,EDF))®85zòÎ²\x0002qlukøèý)ÊZã¤ÜuÃ\x0006GéL©aö¦Ö_+ò\x001aír§ío\x0004ÕÓ·ã²´ã×MË= ¬t^Øò4ÎØíÆüéÏñyÛ²ß.$c»Ð¼?fy!\x000cÀ¡=\x001b\x0006þªr\x0019\x0000Uþ\x0001ÔÜ?@ÐÖJáô.q\x0015\x0007
ïÒnïüºä×³ùMö^\x0005íÉrqÁ\x000fÌá ¬þ\x000fð\x0001ÊÅXzT@Ý\x0002*+ÈçÅêûÛÇ»O«?\x001aôJ*Ð\x0004L¨\x0005§l1¶;éÅòogç/\x0011y7©íÚ\x0016RÁÓT@
±:v\x0006ç\x0016Û±ÆÉÉ Q\x0017ªE	ÇC¥
\x0002/n¯î\x0017¯ïV7S*ïÝßIeÃb\x0018\x000bÆ©OÀ*=ºÐxñâìøbñú|yúr\x001b©í¼³¾Þ*¼³¶<\x000e«\x0003­ZjU¹Ukl¬Wç\x001dl\x0017ªî ê6T«]9\x0005\x0005
\x0018	1#v=Y9²]}*k\x001a9U°Â\x0008:\x0018Dü¸x¹¾¿íiÕ
³Úûä\x000eAoC¥¦\x0015§N-66Ïü\x0012\x001cÑ¸C­Û4;¿¢:RºhK8 áã}½úa½zÌÆ|ª\x001f'á&ê\x0005ç­Åu¯\x000eR2Ü@\x0002{üëå£H_ül\x0017t.Û]RÙn\x001bµ\x0008\x0006;×:Xy_k¤\x0016\x001d=ÒÊ×BOJ¤Ò,ëÜñË­ DPï·Ðl"n¢\x0016\x001djÑNÍp\x0019i¸AÖXM\x001f´ ¤]KMÔ²C-©B\x0017\x0015¨5ä,\x0017R\x000c\x000fh6\x001dQvQkáSù?	M\x001b·6¹ás¤'¼Út¨M3µ²&\x0015F§Î{¬&SÅàXK\x0013uGïvÅ\x00073ü¦ÛêÀ¸`¹ÔÈ\x0010Ù\x0016jÛÕÖíÔ4g4å@a\x0011bj¼äÈ|Ö\x0016hßÑ{¾]ïAC¢Gï\x0003ö\x000b,)\x0015ôÞpÈU\x000f]¤PY³\x0019êZÊ4\x000fNÂò]A\x0005]`çgRÛ÷îü2\x001cqÑ÷íÃUL~Xß<ÄèäuSn\x001fbBÌ$\\x000bïÃ¿óû¿ÿãÓúþ?\x000eoï>\ýþÿÞ­ï\x0001\x001aæoùTF\x0017\x0008M^pD \x0017_`Ëð«~u¾<¦$ØáÙù\x000bØÛzñÕÉÙ;øéàBÅ åu\x0008WÎÞeÇ:ô¸2u.=Ó\x001cÎ\x0012=&j
%\x0008o«áWw\x001f×_¶ãJÕÙr725
\x0007rÏÒø\x0011§a°N$\x000fîÕ\x001f"wÜº:^â.Ì\x001dñi\x001fZ85±v4
ÞÅ¢ï½ããrÖÙø^¤Á\x0003'\x0013É\x0002\x0005á+<óÁ*?\x001eW¸Î¦\x000f>ºAøA½D¯¢[gç \x000fWÉîEö&ÎñF:-Í\x0002Ñ\x001b½n¸³\x0013èHÜ>è\x001dö-B\x0012\x00187ö\x0004ü8;á«?>\&¿\x0007úp2`&sR>Më\x000eôVÖ7lïø_{P;qÊeä\x0017:Íc\x000c'ßx>7ì8<ìçû0¶Pg/\x0014Ê\x001f»\x0018üãÒïd¯â>Õ½ó\x0007mÆ÷anÿ\x001cÍ\x0003ù;¾\x0017û'\x001d\x001fÚ=ßgÐ(~Ë`Ù'\x001e\x001fæ³Ý2ÝÍD|/f÷O0º|/÷Oâ§\x001dæ³Õ\x000f0%,òkÏ§ äµÙ?\x0016Ï7¾òÀc¬\x0002[¼_rRÖþ!æ¶¡ÿEÏOÞ>ÿüø\x0003^¿Ó¤þµ\x0011¤¸ú#ä\x000fýb/æËóWHæ7æøÀ÷ÌQ)ýÿX\x0015	w\x0000þç\x001eþ\x0018¸0\x001e&\x000c»4o
þ\x0018äE\x0004gô1ÃïWÑ\x0010¯öá\x0008ál¤È\x0011²\x0002÷?$úm^ñC°=}\x0008éáa4'½7é\x0007³?wý|õùñs\x0019Ë¬\x0016oo¯®o§ó\x001a;á\x0014&\x001e\x001cÃ`ãoä
?Þrþ·gÇ'c³ÌíûÏ\x001f¿[ýüSzu·þm5]Þ
\x001cË´\x0005ñPX%PÊ\x00132÷êüèËqée87ÿUüK5\x001eÙhÄS\x0007Þ!\x0013gÆµ7â
WÜØ÷î\x0017y%Ë\x0014G®~µ~¼º¾^MÿÈÚÔÐ\x000e/:Íð\x0008\x001f9NÄ\x0008Ú{6~(sÕô«£Ëãå¨<\x000bàt\x001aÿ:ÀdÎ;ñOw·y;\x0000Ü§·«»õÍ§«ÛÇ\x001aÉ¦íFÌÀ~6¦Bb¶E;çÆ¯ÔÛåùÑéËã³±åFöýõÏ¿~÷ñg¸UÐé\x001eÿ²\¬>¬®§_+i\x0014ÅÌ[L\x001ao1¨	Ö9®\x001aF\x000cÿµååX%[\x00170Y/\x001fÌW=#TGD\x000e\x0013.¢ßcã\x001f:!J6n®\x0008qLßÝùMü\x00165\x0013¤Ià/ï¾[ßÝÞLÿÊNËÔ5É´a<í	\x0003e£òv[ùîë£ó³Óñ\x0007\x0007/ÿUÞóåO0Õ¤ÁðØta ò%=2\x0004Ã\x000e\x000bÛ4[~³È'¥æã_\x0011ïæ_}"ÿ\x0001nÉ8{å?\x001f¡6q}·8]?~;SJ¶ÙA\x0005L\x0003ìà¶¾Å=\x0019,ÿy	\x0015GçÓ£ËW\x0003´_þeÔê¦ÔAAËÖá0|z\x000cgòæsøÛÓym\x0008(Lò\x00049¤ö¢X\x0005CwVÊñ»\x001dÄºüæèôòèåeïéëð7g\x0003Èrõë5+xq´ÍãâÝú.¥Q©_nï\x001e*\x000eÑ© 1@\x001b\x0003÷@ÍIÈÒß¥8èær\x0001\x0005;K\x001cúöìüÝ\x0000w°£åbôX\x0008\x000cÕZð¨8\x0015Æ\x001e`Ô,UÚ®\x001c\x000e6\x00145\x001b?~,bÉÖ"pûuD*JRÑDªiq(¼k\x0018\x000c
ËñYZ;T¤²M¦Ö\x001e8|þ
^t²K\x001bÇÙ+
çàK]T%¤jô,­®x=ü\x0004é4©\x0003½Å]®\x0010§.Iu#©Þ:xÐ¨±¤"Q9n\x0002*PMjPUP¬\x001e¿|\x0008Btzøt,\x000buK\x000e§Ô¤ö9ß&Wº6reÊl\x001ab\x0015ðy~WH»!f£ú\x0012Õ·¡ÊøÍé¤²tR¤\x00184Ô)w\x0017*\x0016ÁÞgm¬Â\x001chªHY
'ÉguÜÏ¯`íÚ¨6#¥`§1æ\x0016!ÌOVÊsE¹-ËÆß\x0006*X;V·)\x0005ã1H®!r¤­´\x0019÷\x0001*X;v·\x0019*
Q?fªLK\79sk÷qµxÇ\ñ6{õ¿£°xÇ^ñ6¥µÈ\x001aKéÔ^\x0010Äê¤"±n)Á¨`í\x0018,Þh±\x000cîK\x0003íÊR?oµ¥Z\x0010\x0007îÃ\x000fà\x001dÅ\x001bmVp®\x0019s)Jqû8t\x0016Sû0¯¼c´x£ÕÒ>³\x00065 Ñ\x0014\x0018§²\x001aØÓÂ;V·­ é\x000f0Ók±
2>ÎRáÄ^4èX-ÑhµàØmÄ\x000eÍñÊ~Ä*:VK´Y-
ÛÂðEÆT\x001fä\x001d\x0017!ø>«èÆVÏ9¸\x0012\x001d£%\x001a\x000bN\x0016Ö	°|Z9ÙW!Ü>|,Ñ±Y¢Ñfñè¬$¿§YBAaIK®«1{aí\x0018-Ñh´\x001c½\x0007¹ê,×\ý"÷s\x0002:6K´Ù,-åÆ\x001d4ðêÜ\x0016O6Ëòñ¬j\x0005kÇfÖ8Ë¦VC¸X2+\x0001¡I	(¶#Ð±Y¢ÍfiÅÒÀK«%_ÀüpiÅ>\x0014ì\x0018\x0002Ùf\x00084LDÛäX\x0018²ZÏÀ\x0004a\x0005kG¹ÊFåªyjÐJ¬\x0018ÁnÜ4y~6jGcÉF¥Ñ`)¾á´\x0019TïÃ¸Ê\x000e: 8Þæ³ªLß\x0017Äö\x001eX;÷J6Þ«à´(\x0007|ÁJi\x0001·\x0017Ýª:÷J5Þ+Ì­ÈiÉ\x001eö>´êÜ*Õx« Ó
\x0014\\x0005¤bSï»(Kus­­ÁëÆmu<¿\x0011\Ìù>-ªs³TãÍrU½§B¨ÀjUly)ª`íÜ,Õx³ÒÄ¬ä´PÂÍ\x0004­M¬RïÃ\x0013Ð¥ÛnV¨À¯N.ÒÈªÈÁR³\x0005tçZé¶keÁ:DØlý@ëp\x001dÛH;×J·]+x\x0010Ö2³¦DK`Íß±½8­¹Ü(\x000b~ÒrbI=`·â\x0003gò]Y\x000e	¶©Öd³ûÈ¾XiZSR[+Ìd°ÍóË<!rRú\x0001<f¦·ãEÛã±\x000c\x0016jðbHï°ÚæÄ¦ÚRmÞ\x0017Çãô¢¤\x00173éá\x0019)©µð\x001bzãá\x0019)\¸ñCÒ/K|9\x0013ßHÿâ3A\x0015\x0011.§ù¸\x0005iÂW%¾+}ÃÉX;k)}ë,	oI7ÑÞÌ¥·ù
ÊYIuÌáFðc}à>ñ]ïæ`\x001a±éÕ1\x0013QF(*§uøcÕS_dPAïøü\x0016úGÂ?ÐÉ$ D±\x0002DØ}¿£éã'\x001fÌúSh«ó!
nÃ"@NÅä0ªtO
a{Ú\x001fÒ.¹\x0012çð»ßÿïÃzUQ\x0015¨¥ËuËÐ½A¬¡K\x0008¶Æý\x0017¬Á9üzùîh9^\x001a©EI-æP+\x001cà\x00085ã>§´þêÞe9#KØ|\x0015ìfÕ0¿_L«$\x0008QáÂÁEÖÝ\x001bY(@@\x0005\x0002ÄÕÿ\x001a³\x001bûWUûÙÍRo2O2çãé\x000c÷Hu¡~kVÕÏ¾èK\x000f÷s¿xÁé\x0002\a¸+j]RëYg­òAS#vÓ2·zµµÈ¦D6³]nîÆâL:h§sâH\x0002¡ÚÔv\x000eµ4Ù\x0004\x0001Cæ\x000c(W>ë8ÒSPKíJj7ZÑ¤IL,\x001cþ¶&°nÇk\x000ek¨}IíçP\x000bÏ\x0005ÐØGÌÅ\x0006Êë\x001cWØÝY:Ì:ë\x0006ñ¡w)pK:kÅI<=RÏUK\x001dKê8ë^ë´{\x0006ýwVsà½¦ê^ Ö;;ë¢jFù²Ú³Iî¥ÕnØ(o¸v\x0006D\x001f_ì´Úm7Ø}Í8K5J\x0002/Ý\x0011cæÙá\ÄÎ$¶ì©F9K7j8bÂÆú?zK\x001dq@k±{ºQÎR \x0014#Å¦¦ø$¨ôÈ\x001f7Rû_ÝÓrt
\x0017\x0000Ûg¡\x001dYÕ(¿;ñ'{
RÎÒ¸Qä\x001fêu®
q|IÆ\x001aj±{\x001aRÎR Í5¥\x000715Àµ\x0017%W»8írntú2Ârýy¯ãº~¸®is\x0004730Ês§¦ËÓB¤ÓÛ½üÞ_ný\x0001ªü\x0001jî\x000f\x0010.÷\x000fEiÓìZt\x001fV\x0015r{¥î\x0007èò\x0007è?ÀcuàrSÅ\x001d\x001dJfWÇ·ý\x0000Sþ\x00003÷\x000bHCóZ¤ã6Y\x00134gíÈÕo£·%½}Ý§l©ÒÜ~¦»ÝÀTA¿=NTÇïJ~7ûôCÜ§0Wty^ÎQ:mv}þ¾ä÷ÿ\x0002(? Ìþ\x0001ð~\x001d9ý2°=f\x0003ÛìÒdÚÚ~@,@ü÷û\x0002¥\x0011\x001f;#~Þ/ÐÒs×8Ö\x0013\x0014-uqÕ\x00063ðn|\x0004½x]÷\x0010ÊxÝ¿ËX;vïaþïÐÂä^\x001fP
ÔAá|ÌõjgßC¬çD("ß/\x001f>ÜÜí½}zw{S\x00139
`Ðé\x001c=°\H=Úíá÷ó×G§{o¯^\x001d\x001fENÅzæI"\x0006ÙÊïC¾HVe~Éñk\x0019FjÚ~.ý\x0003¢ÌU·Vc®5\x0004ä\x0004k\x0018#Õö\x0003Lù\x0003ÌÜ\x001fàÀKç¢Qk(&âÄ*~=@hâ\x000f½\x000f\x0010vð\x0005tNÿ¹UúO«\x001cËÞêÒLý\x0001Ú­=aíò\x0013¾Þ»ÅYû\x001foo>WU¿<	\x0007Wêäè\x001a©+ëè\x000f÷÷\x000eß\x001c\x001f]å¼µ[{»Úå·Û\x0008\x001eUv\x0006Rÿ):×i\x0008Õàº\x0004×³Á\x0015×\x001bÉkÒ%¦\x001aÉ\x0016W\x0012ÜÌ\x0002\x0007eDå²\x001e®à¾$ð\¬TÜáÛ\x0012ÜÎ<qû"LÕqo/5Ô¾¤öó[pb\x001b¶³uÅ>9Â=RI]Ü=ë¦;ònÙç\x001c~\x001b\x0003á\x00038Çõ_¹\x001ddd Òt~i×D"\x0006Ù\x0006&\x001b|N£
*l3ë%%FºÑ\tþY1­¹Õ2X
7¸HÓ
Æì3i×d¤´}3ëÑ\ãÖU;À²24\x0010Ìø)ºü)z7?ÅQ\x00194-Ë|#ãc\x0013pfü\x000eSþ\x000e³£O\x0012r)\x001fØÍÑ°XâÜD\x001c©ñSlùSìÞÙ÷.ÿ\x0014G&´`\x001fFtTÎø%®ü%n'¿\x0004En*ýó\x0002ûXXâò\x000cÑ;3~/ßÍ'	&çb¼ Fgloã\x0012ÕV£ºå§ò§Ý|\x0013ghÄ¸ÄÝPéru\x000bãÒ»µ¡ª~D,DÜÍ G·l'õñ\x0014£ÿ\x0002E"\x0010=(ÄÐ¼\x0016Á¥¨ ×ãn\x001dÇö\x0014«±\x001f#Ö=\x0007áÊ5ø\x0013\x0016w\x001fn®\x001fª\x001eHÈÓ[­¦ùèöìunü\x0015å\x0012ÙÅÉâô5üõ_ Ë_ çÿ\x0002¶hm Áû¨=rUÏ\x000fÑÈoK~»\x0003~#_¹ªü	a³þkü\x0005¾ü\x0005~ö/pbUÃf$µ\x000fºÈ	\x001d?\x0012y©ý	qÝÌ¥Û:"Mé<\x0002^Há\x0005\x0017HH½=tÑ¶õ\x0007¨ò\x0007¨¹?@ÅUïð4\x0004\x0015LÄQ\x0018Óö\x0003tù\x0003ôì\x001f \x0004åÃ]ðy*õÆÛÓj~Sòù\x001f@ò858ÿÔ<cËÅ×fd\x0007B\x001b¿-ùí\~\x0019\x0005Q¸à\x0002¿\x0000\x000e^K\x0011w}}\ïf\x001f¿÷Yá(®t}ÉufdäBÛ\x000f\x0008å\x000f\x0008ó@¾;Ý©\x000eØéÀH÷UÓ\x000f(2j(BÅì_\x0000h\Pþ\x00019+®GVà´ý\x0008óe¨ífu¤¼xà¼8&cù\x0017l¯$ªü\x0005=\x0019$g\x000b¡ný\x0016Âv
â¨´~¨Ø^0Wù\x000bzÏXÎ~ÇÒ¸Ü\x0000\x0005æ(u¢\x001bø\x000cÔ\x0010í®Aï\x001dËÙ\x000f\x0019<2©\x0013t.7Ý\x0002\x0011ô®\x0015ìE,;s(G,Û-"\x000cl«ü©Ñù\x001f×ÛbÜÓG(7Ü§¿(Lº·à¤VXÓ¢ëTÌ\x001dtTÅ¨ò6
µ½`þíâ|,÷\x0014Ê}ö«Zqe`±/*\¹5XJ*X]ÂêfX½ï¸;\x0011·?®\x0015mK5RkPkJ\Ó|\x0015\x0014'Ïûð¢¬Råö\x001aói¸¶Äµ3N§X£\x001dùpsMâ$Ö
\x0011\x001d\x0002u%¨k\x0006õ\½\x0014ÀjÔDj8ø,ÕvM?í\}ë[qÁ%¥K\x001b
ëÄè²a¥·\x000bäi´¡¤
­´Zr\x0019I<õ\x001c;\x000cvl\x0008
m,ic+­u¼ú-àr\x000bÇcøÖjµ«P\x0018«¨\x001cDó]\x0010ûÑå«Ë\x0003Y\.}TÛýüi¼=í Õe¯\x0012pélUî\x0005[\x0003ÓX{ÊA6k\x0007Ì~üÐ<%
dî]×#Ó«x{ÚA6«\x0007C&h)8\x0012\x000c\x00180äóÝ6S}K¡ù.\x0008·oé|CÈ\x0003$TvqÕöF¯-¼J­\x0019b¾jrXþôç?kîÊ\x00055`Ê+îpðy/Û¶´÷ÕÞÁâÛ±7ñªWÍáÍ\x0013&W\x0005|+Þ\x0019£U¸ºÄÕ³p)âa\x000cçº%ë\x0014t\x001d\x0019XÅkK^ÛÎkr\x0015\x0004®á*\àé'´ÎMâõ%¯oçõ¹Mi.z9"lG\x001aá«pc\x001bÛqã>Ý\x0006°#9 ³Ý`·&áuØª×LY\x001dÌ*ØÂÙÕuÐ#\x0013ó«ûÒ¬]¡ÇÃÇXiJe«WoÏ÷M\x0003î39C\x0005ì\x000cJúÂæ¬Ìj|¾²Û;Ì&\x0001÷\x0004lh`AòÃV\x0004¬uVÈ#Cô«M\x000fØ´_	7Ï!lx\x0010]Þ\x0000\x0014w$#bïÑÅöG\x0007ÇÊ5ê¨âò\x001dv»RqÂ¬Y\x0010èÊsõßç½ÅûåûõtØÉ°Oå\x001bÚó\x0008ª»4ÛZ{±·8X\x001c\x001clÑËÔª¤Vs¨­¥ \x0017b5^?¸ÜÝ.·D1k°MmfaSCª+æGÖBT3»ÙÍº Ì
°\x001f,Í\x0005\x0007=¢óÝmóSj°C\x001dæ`\x0007G¨\x0017FR\x0007\x0018¼Ä<!ÃÙÝa\x0017:\x001b/uÜ>7k³RÛ<®FÙm\x000et
wïAÊY/òÛ¯?ß¿··Ë÷©|x¹÷íýÝãòæ®f
\x0012Ü\x0015³Ú(àSÐÂçy\x0002£EÞ\x001e/\x000eR\x0005ñbïÛ³ÓËÅÑéüöëÐwðßî\x0007èò\x0007èÙ?ÀóÎw´ÊÅ<	q$âYù\x0003Âz}Kèê[Ê\x0012·÷\x000fðoç÷O\x001fkZìpæY´q\x000e¢\x001d±\x0007Ë*\x001d,T;?»z3Úf\x0017Ö\x000b]]/Xkü%8©Ë\x0005\(ÅzXzª\x000eì\x0019?Å?Åìæ£° 5ù\x001468¸jGª¸gü\x000cWþ\x000c·a$å\x0004º\x0018þ%¼ÿJ¥\x0004ÚI\x0019¹´ç±\x0012|nLÿ±»\`ò;\x0019\x0019®Ðò[ôú\x000b\x001dÙú<||¸¿y¬Î½&!Oò<É_©\x0011xÔsçgG£}2ë\x0003!td«³\x001e\x0017k²WF'Ç°,Wgk7n'O¦u%­k¥\x0005©©BþÄSU¶!¶äf&Ó64Ór?lGë9$ÄòÕ¶ÐTÜÂ¼Ô1
wAïÓájAõCå2"»¥}w;n²$Ëå©yâäwË§*V£)Vì¤üg^¨«ÌÈæ_$ýnq5SªÓå~'Kb®â\x00076î?OD5%ªiCU)ÝD8ÅÏ¼4Io©]jz§j\x001aÕ*J{vzÛZNÍé	{
«[÷#\/ú³k¦+\x0018#¦\x001c-¦£â<¯s)ßK¿I½ÙcÌ­{\x000f®\x0017G©Ç¶V\x0013¹h-5Ú\x0002væ\x001dFf¦Wcë\x0012[Ï:mãg\x0013¶Ç]\x0015\x001d6X¥Ü°-ÕQmJl3\x0007[ûíóH\x0014/cn$;¼$¶Ä¶s°¥ÉÃtb7ü=Mr)Úk·\x0007Û&c»\x0012ÛÍÁV*\x000fª\x000f\x001c<¶^dì1w¬\x001a;Øa\x0006¶\x0002«"Ê
DE²\x0007D+3!2ý´û#®ñÄWÍØMwEÒ¡wnJ 2ñýÆ¸%K6	>¬Û\x0019ÁÒûííòqyW5\x001c\x0007G»Ó]±n?pü!/Â\x000e#{Eûíñârq:îU­\x001b\x001eÁò»\x0001\x001cnãÈOÄò\x0014ùÑ9á°­-¥
ÜàfÞ\x0007jå\x0005Y\x0018¹\x000cËçÅ»=ïÞ-ïÎ¼¼å/þØå:¿Ë¥D«8\x00122Þ­f\x0011ì£«à\x0017ë±6a{ÙªO7··Uã¸ËYb@å6&Ë\x0012Fmõë\x0018g>zsut|<\x0005]èj\x0016ºôÇ\x000f\x0005C\x0005\x000f`èòJ\x001d±uj\x001d¹.Éõ¼C×û\x000f\x000c¼\x001b\x0016£\x001eîÌv±^Þ»ï\x001d~yßçÿ\x0002§ÿÝ\x001c~X\x001fG\x001aâz\x000bîÛ§º¡\x0007:·ýè}g¸öf¤§»\x0017-»:\x001am\x000eëa§\x0010`+ÉÊ=Jò\x0018Ø\x0018M®\x0019Ù÷ÒîJôõ°k%º]-AÄbqêr@á²µZ¼<äaæ¡ûJ\x0001\x000b«ÀD®o\x001ei+© bm3¢\x0014i3"%öÎïßÿ|ýP\x0003îh¿KçÔñ0ò\x0018Í\x0004§r@W{çg\x0007ß\x001doçV=nõoÃmzÜæÅs\x000b·n«»ÂVß;^¾[~¨ÚûÌ\x000b_½Ð!ï Ñ2§õ·í Á4á«ÅëÑàÐºî
+½\x001eÙE^ÿ,áÈ\x0015P%¼}
ÛDd]"ëvdÜQ"Û\x0012ìtjvCz$ûWIlJbÓN\x001cý¾44¼%æ¥RÒÛ&;fà
í=DëJZ7V¥ZR/ãj\x000e%ám\x001d(\x0013a}	ëaákïÓÉâÜ\x0000:ÙÜ¢·»
/C,ã¿\x0001±ìÉ\x0008Ù.$ÒûyrÌ÷7\x000fîÁÌû<äwëûÀ^Ñ>°\x0003HÈ÷NïßÝÜO76¢×Fc\x001a¬µÝMöFÓ`\x0012#ìÈQ\x001fÀ¿$ð½Ó³WGg¹±0´>TºÒ|\x0005fRUÊ\x000e³»\x001cÊd\x0005ây\x0007ï¶
XøW`#Ç§äú$!éJß±\x001eZû¼Ã®zÖ²<V~dó`5¶.±õ\x000cl§,-Ã\x0018w\x001e×æ9\x0002k¶î{ªÁ6%¶sÚ`
9Ê=:±OÊ/äyya[\x0013n
µ+©Ý\x001cjgÈÃõR*Þ­\x001d\½µ­ÚÔ~\x000e5è?*4\x0005\x0008¨B²Aõ¶Ò\x0005ô¦QknÍÃ\x0002â0çRSE\x0012g1E\x001e6J\x0016¨¶[2¾U\x0007\x001dKì8\x0007ÛI\x0016!ð_¨kÒt;\x0012{[§·l?h³^ÂeÊ©?ßÞÿQã8\x0019ö=ÛùÝHÑ¤\x000fõªXak»Í·gÿ5êõb-SÎÉ©\x0006îRL¹LÂ4.,L×Æ+Å[\x0002Q4ã]Üß^ßÜN\x00076a5KÜ\x000b£\x0001*=à·Ï
¼8;><:ÞlJdÓ\x0002Þ\x0000G(¨òÖÃí½ÛS]ìÚÁùÓ¼ò0÷W\x0004ÜNNöÖi+ÛA\x000e­HðpV]X'÷wO®ï\x001ekÔ¶¢äF\x000cTå¸ëFÙí{ÊNÎN¯N\x000eO/·c«\x0012[ÍÁ\x0016Ünì\x0011ÙæÚÞz3\x001dÚÐfÖY\x001blÜu´\'{r¶¯²íJl7\x0007\x001be2U\x0004<RØs¹¶RÛ\x001fâtêPR9Ô`\x0017\x0019\x0012yà{²Gm\x0016Òj[×Ð$l¹^[$sm\x0011ªíªÐQÀ!0é%*\x0012,¸¨H-UP¨±Ç<B©;ºGõ¾¸\x0019éàþvïÃÿ÷¿þ¯ÅíÞ«û§÷?Ow	ã¥\x0003\x001eo	YtÁòöq¤@öàìxïõÞâxïÕÙÕÑÁw«\x0015ãü\x001f2º_G÷~±¼¹{Ü\x0003Dø±7\x0015®,ö÷¦ö,sAR5§W|,ðiGÊã.\x0016G§{ðß;=8;ºØm\x000cùí.UÉÁÿ-üsÜÝ¿?á¥Ôh¿ùöþéáñþ	Á¬S-7åp~÷78t\x0007ÌÍd¹ÁSKõ gWçgWß\x001cw_ýÿ¼:Ü\x0008±\x0014ö)|F\x0008
"\x0000ÿ\x001c/÷^]?Üýù\x000f1,a©²CÀa%gÎô\x0018øI¾Xì½:<?=|½âÓ¯üòk7½\x00013)øç¸ü¿\x0001Âà\x0002Ên³
¸¢\x000f\x0019\x0010-¹\x000bJSa(cðLÿM\x0010÷w_ÿþá\x0017ÊctÙ\x000b87ð\x000füx¿\x0001þÁJýD\x0004âQ=\x001a¥¸\x0014\x001f"¨þY¼ÿøæl#Å¿¿ÿh¾vG\x0001\x0004(à\x0002Ü|\x0012\x0018Ã"[\x0008þq2uû\x001bm¥IG!¬Vf\x0002nçÍgñ}7_ºk\x0001ÿøç\x0018üïþüçÃÍ#M«ÝðQ@µR
¬Â«®$ÞXÏWhz\x0007\x0002/ç»Ãó#\x001c\¶ù©<Ý_ëë:\x001cqø\x0007ïÇw×\x000fn\x001e\x001bYÀa·üql\x0000}ÁvãM \x0019)BkÛ»¨Hrrt¹ÀÂðÏ4\x000e0F\ÂÀ²`0¤JÂD(¦&OÆ¸»~ôû{\x0001\x000f\x0016ÿ,ï><t\x000bQ7ÝS¯\x0010ÒgA\x0011bº{ªy+\x0006\x0008äB\x0011\x0003N\x0006>_\m$Çp\x0004aQ\x001dÁÃýãæ\x001bª­¥\x001a^­\x0005M7*Jê!R\x0006<äþùÙå:|?ü³í\x001e$¹7ðOi*\x0015üÓMÔôOw~ò?üÓgýú½»ðýñ\x000fíë÷ËÍo\x0014¦$²Ä\x0001æ²û\x0002¦³y»[\x0000
R÷E÷	¼ÅÑùægê~Yþí·wÂì\x0012 ,NînS¿Ý'*­ ®\x0015øáj_¦'*%
\x0000éåÖdÖÉÙÕ1öÑmâøåù\x0014n»3Ä?p&o\x000f×\x001fG¾1¸\x0018³s$Hª´VÃ\x0018Í]¹\x0002ÇÌöOäíâüðÍÈ·ùüõNþòkÇ\x0001¿\x0000ÿ Çug±lÒd8=]
\x00175\x0018iªJ­iÔ·\x001bm\x0011 øõ§\x000fRt\x0004ð¦ñ\x000f\x0012<}¼\x001e9\x0007¬ÿI9A7Ã&\x0004\x0010\x0010t;­sr
áêÍáÈ)|xzÿ;\x0017,}\x000eáÛÛå
ÁÖ©7H
Ðè6=ÀÛ÷vícüpt|¼\x0018Ñ!\x0005\x0006\l=
C+\x001e/Ep¸\x0015£{©¬>àx×\x0001jÌLÄH\x000bÕø±¼°ä¨Ã_\x0005ÙL\x0001ÚËN¥0\x0014{RHº\x0018 ¶¨¼Mø\x0002uM\x0018pn"g\x000e\x00186Ù7~\x0003m+å'B`\x000fí
BÐ'¡4\x001ePÐL\x0001¦wH¡\x0003ù\x0005@\x0011Så\x0018ª1¿Hh¾ØÊ¦}\x0012\nüÀ\x0007>	õ×ïÝ~?Ñ\x0016rêGñTÄ(%Ø®wüUbl¾\x001b?\x0013\x001eÜJâPù¡\x0004
A Dûg\x0001É%'J/\x0003æ]êª\x0002OÓàMA;\x001cÄ°$\x000eÙþ`±\x001bDN\x0014_FvmÚé<\x001c\x0019¾ºs4é<ûÚÄ\x0001¿@N\x0014`&\x000fÑ×âû\x001c´\x0000\x000c×Í\x001cðEåD	\x0006fn\x0016\x001eØF0$
ãPí\x0018 ¿äD\x0019fp¹Ì\x0018>\x0012!s´\x0016\x00102L=\x000eE\x0015=Ýg1ôU|Ì_E5cÀ\x000f\x0013©AÓK\x0011F·Î·ã°,K}hþ*
ä¨*Kc7®+\x001c]£û_ÉäpÍÂ\x0003ïjúÀ\x0019X²9NI¹N±¢5Þ´r`,ÌL\x0014êÆIJÔã\x001edûhá<¿Ù ?\x000bnå0-A¶eçÇ'1ÄÈ\x001c&4k|\x0003òËL6Âx-ü7\x0003Ét0Â\x000csD×Î\x0001ÃL50ÎÆ¦Æ<Rº\x001e
ô°î?Vpp4c\x0002\x0007\x0018²=ÎÄÄë!\x001dËRïd3\x0006\x0018ùßØ©þ
Ô\x0013\x000eæ`\x001aå\x000e·}XáiA\x0013\x0006ü\x0000;õÂÕ$<L\x0016]de©j}´isZú×I$\x0006ÄÏÒ´k>\x0007\x0012UHõÆ\x0013±\x001dNby41ÜT\x0017\x0003$zuSE¥+ù\x000eB'NSªÍþø
µ\x0004Æ4O®\x001f7\x000f7¤Øìe+÷}ãÄtR¾\x0012*Ru\x001a\x0007\x000e/\x0017GçG?ßìm¿\x0013!\x0014ÅØÈþ\x0019°]\?<\ï\x001d,ï\x001eSxC\x0004Âbª2æp&£Oá\x0018ËûÔåi]\x001c\x001fî\x001d,N/1\x000f<\x000cå~¼y·üÍ_w\x0019ÝMâ·¯à\x001f{sýØµÊ8ÚÓç(\x0011rý\x001f\x0007ËwË\x000fþ£K\x0018P]:z3ÁGJü*\x0007¶\x0003ø\x00188×ÐöØ\x000f\x0016¯\x0016ç¯\x000f/ºî+=:¼<Ü\x0014Ñu?þüä¥O¯
þ¯àãåÞÁý§w×SØ\x001cF°ðÕ\x0019PÎ>\x0015(Ü¤ä;6e]pl½³W.ûñóGûõé»¦\x0007\x000f÷O_»øÍ6.%°ñ?v\&W)¬H«¿Ô¼8²½ó³«ÿÞ\x0018Óq?þýÝS\x0014Jüf]o=0\x000f4Á§\x0003ÃvyäòàRh:/c7?Í\x001eØ@xe+Xp.É
\x0000ÃªíîÄ<8OL\x0016{ÅÚd\x0003!íd `t\x0002\x000b4âWa(q^Og#×@\x000cf;¤è­ÁXXý¤0ÕÁw¿?º\x000cu{`;Pù[jÚ
d]F=Ý2½3\x001b\x0008ÖL83\x001aE\x000c\x000e>3Ï·¬ß{ÖF6\x0018¿ô9½ÎÖYýÝç;<´ÁÎ\x00044Ê1\x0011-¦Ü& y\x000cÔÿ6\x0007Ã<\x0013Ð¨
Ñ,¿NÑ\x0005\x0012ÿ\x0008\x0006#.ÛÑ4 jsëÈ¢âGuÚ³Éb0ÛÉp\x0012iM\x0013\x0018
¼+Ç¯@íàª
e&\x0008[F%#Z×¤-ß4+wpÓ"5\x0013\x0014\x0014µ­"M©C$\x0019M\x000c\x001aUhCÁ	h\x0001;ÓU£ùÒ¨;\x001d\x000e¯vð\x0008\x0002:ÛÑB@C
4\x001f\x0013YIÍ·7ÐRÕB
WæJ"S\x0014ÁW^u{=:2½\x000b´¡°Ïv4¡³f\x00176M\x000cC\x000bEìí'kD+¡êZ)\x0018\x0003hXÛLßÓj>5µ\x000b4hª^ªap>¨4ûl@j\x0016jJÍ\äP+ocÊJ NÑo¬õ0lCö+\x000c\x001bÑ¨\x0002¢\x0016Í¤è	¢\x0014ÅAU\x0010Xª)·S+¡ê¥\x001aZA1£yÖRb6_\x0016å\x00015\x000fTÒdeãmðù\x0015D\x001d&Îÿ\x0018ÄÓõ¢CÙ\x0014;Nd!i)Õôl¾*ÈµW\x0002qQªÔ"\x0003h:¿\x0002¹\x0003S-\x0017/Ö¡YÚ4\x0010-¤ÞP@3\x0015¨/Ô\x001a2PíÛ|ÓÀëd©fÌ\x000e\x000e
n«®VíÑ)~6Æ|Õlö
¤ÿ>s\x0005fu0Á\x00115ip\x0017ê\x0002Ì(u¯ÀÅùfä`*e;,p»:nC
Tò\x0003
;°ps\x0011X%BÛ±CÿèÈì0O-ô#4¢
e~&¸\x00051\x0000ÆSi©\x0019\x001aßì±\x0018¿(\x000c¾$So\x0011ì\x0010îZL­Ã¨Ü=ë\x0002¿C\x001bJSMò¥¥ïiÓ¨ÃÎb²þ\x0018ÏF4*<­×í¯Ãz³¤ÛÙÂ5!ìà{\x000e%Õ&9ÇÅÆ¦æYMu:f.ÚPm;\x001a\x000e£«ézÞ\x0018\x0018Ííà®­z\x0010ªÐ\x0002\x0007;áï	\x0012%de6Xî\x0008¨EÊT\x0001n`ÉÙ\x00102"ý|%5®Ü\x001e\x0007WJ}«$ù+\x0002'ö\x0013Y¯\x0008ÐBvMNÒÖj/;õIO@{=ÿsb¥µkzì!TCWltxÑ*80¤\´h¥¿Xß\x0001r°üü~	¸÷O¿OÊOÉ}RüÜ!å§Tàë\x0017Ä eYÜ:X\\x001c,ýìê?74m!ªvkìº±ør}÷Ä\x001bXNnþv½¼»v;K}\x0002)\x001cíSf
gXæpôàÃYüpxÊGöN¾?\nÜ»Rp«[Íá\x0006«\x001fO%íðªºÌ\x0014Õ\x0019¾ºØ¦Ä6s°ÁV\x001cÊºZd³\x0010¬êAiÐÈmKn;;(J\x000ecÛBC¨°9ß£\x001eö7\x001b¹]Éífp\x0007i9©[F9mÃý}ßs±}íg]\x0013½J\x0012q«\x001b©Þä\x000ecÉ\x001cç\x001cµPè13E¿Í"Û\x001drÓV\x000cb\x000e8nÆ Y¢e*\x0014AH³Q£\x000b\x001aÁû¢{ì\x000eR¦jÛô(µç,ç_ñ&eOtË9²\x001b{ÓÊ\x0007®Ém7Áä\x0003\x001f\x000cÉ7ë\x001e¸uà&\!¸ÊWÜ|âaÐÓj\x0004ïi\x001d9GíD\x0019Ó \x00014§t\x001aâÌÈùp7ì"6÷Ô£wô+A(Ón;<qãòï»'¿å\x001c\x00017\8¼)\x000f\x0013>G\x001aõ°ãÛ\x0008Þ\x0013âr\x0014ÇØÊC\x001cRSÙ2ÃÑø6pÕ\x0013j0\x0004gÓ¶+²J\x000b\x001d^pÕ\x0013)jHá,\x001b\x001c6'èWG½CäÞT³Þd\x0010«²\x001c\x0010V­ÊDvø(UïQªY2ª\x0004\x000b&õec:×C\x0004·Cã[õ\x001e¥÷(EG
¬û\x0004-5)K'ëKZ=<|={;ø\x00173¬Â\x001dy^6ÉÆÜÉ-O=¸_\x0006â7ß\x001cü|ýéæ®Õ¥wtêj-Ð£×|ìÃ\x001eýÁw'G§\x0015\x000e=«\x0012\Í\x00027Ô¿\x0015B'¸A]ã(\x0007Ea+¹)ÉÍ\x001cò \x0004;\x001e	Á\x001e¢÷é\x001c´\x000b«ÉÍúe1gô¤\x00012'ËÇ»©u¾ß>b¶ÂÈlYaf\x001cÐæÆ,Î/N·ÓêV7Ò*ËAo¸Ë\x0008â·Ew\x0018.>¬§5%­yé´²'õºÛÀ+'ª¡uLm;\x0008-Ò2å\x0001\x0017bPpT@°\x001e¿\x000c¥¬{Ú{uÿùý\x0004V)À4d4	ÇF6"\x0017 ¹Á\x0003æ\x0007wµ÷êìâ`;©*IU\x000b©\x000cñ¹~¥¥D\x0018\x000eSÖêT7b^
3\x0014Ë\x0003£r]Æ ¶«Å4%¦iÁTi:Ww B²^¶\x0003¨Z\x000f\x0015µ¤¶$µM\x0007*%{$Ýéd$\x001b½*Â\x0019.øª%u%©k:Óà8®¡E`ýå,©/eÅ¨â
êKPßt¤\x0016íÈîDµãÚ\x0004\x00135ge78Kµ ¡\x0004
M'ê-¥\x001bµòi¶Bÿ>=5»\x0000%hl:Q°´¨ßÆàºACò³| k\x0007cq¤EÔ\x0013OW´ÝÒÍéb¿\x0019ÝRÎ.+ãF­¬©¨}õÔ¤þ§Nµ'õeØ×J`­8w©\x0014ðqùPåpëDíMí\x001b*ÞÇ¿¨æ\x00158\x00023¬
|\x001d\x0015EËhíLÕ_ÎÁLQl~\x0001/òÕò>m\x0005\x0010#1äY­\x0014p{u."\x0019T\x0000y3ÂÞ«ÅÙæÀ\x0005¬*aU#,Æ¡|VWt\x0011d.4q8åTO«KZÝHk\x000570Zas`X:¦U\x0002¶\x001eÖ°¦\x0011Ö8®¯¶FV!,«\x0003cÔ Þª§µ%­m¥\x0015i\x0014*¬í\x0016)Ø{ÑÑlô\x000cëh]Ië\x001aiÁ\x001e,h\x0003·1±M\x0000´s¯­Zw[TèK®³{\x001am÷²ôò¹Ò^dÇeCtE{Ò5{o§U%­j¤17Ç(;8qê
Ñntcë`u	«\x001baÉ~\ý,9 Á\x0001;7Ö´¦õ"ÄÜ­%|Ö
¨ÒÙ\x001dÔ»õ´¶¤µ´Vä\x00149N'`ik³ÒÝ
«+Y]+«æ0¢rQsÙØ\x0011«/Y}#ëª\x0018\x0008|Yº±:2\x001bBµÕ¬õ­õÝ\x0004Ùï\­Ë\x001a×äºðárÀzØ¾m\x0015´ÔohS_:Xnm5¸_f'¬=Á%[%\x0017X^\×\x000e¸ÜSª³á\x0015·èÛ©´=Q [eÁê\x001a\x0004h&¬\x0002E[ôíVZ©ÖS"ªØ\x000cqðóòñº <!á¨Xõ\x0002®BÜÃm§43ÿà»Ååáâj;¨*AÕ\x000b\x0006Õ%¨~ zýÓkµfjýùÏÇÉWÕY\x0019ÙOaàþæ\x000e÷­Wfël'Ö%±þw ¶%±}ÑÄrÝ%_­¦Àë{Ë+d'\x0015p\x001flÐ\x0016E"Anv\x001báþ\x001e­-HuIª_2©-Ií$Uë2A©râåi¢¢VûñãJÚUkøUp\x0008~8Ü´ü¬\x0000U%¨j\x0001
¹\x001cUd?Æ®ª:;Bj1MiÎS\U\x0008>!g6¸ÜT3«%µ%©m".ÍNÇÒ\x0002Ã¹MÕ­tO¥\x0005v'Þ¤®TzV°vìb½£Ï.ÁHx`:g(9C\x0013§û<1 pS¡Ò«æ |úÒqQãRAýøy\x0002Opi¡òZÈ< k¸×v2ªpë\x0001c·\x00160¾~øøç?&êÓhW\x0003ÐæÙTà^åÂÑá*"uxþæp\¡\x0012².u;²\x0007¹ÊÍ
.
t\x0004dgrÍè`¬ÖOYõ6ê\x001e/qbàÃD=àö©W\x0017XMsUrs\x001c\x000bÆ^\x0000.\x000c<\x001f½¼n]\x0011ô\x0016éV±ª»=á5­äòPCCígÐÊõíï*>|;QmÙ<\x000b\x0000þªWç·\x001eqd/ö\x000e\x000fÎÇ_Úº% zÞ\x0001nþzz\NªvñQæ\x0012\x001dnf2Üxlí\x001b\x0003\x0017voqu¹\x0018-tYw
DÏ)xq ¦\x00045/\x0018Ô ö%Êõd\x000ckw4o\x000b\x0010Ò¹À¸\÷+XsÙá\x0012ÔÌJ{Ä¶Âê\x0012V7Ã\x0016ÑL\x001e
%²I`»z¦ÓêõêG-Ê¡Ëin8Æ«\x001cÁ24'
\x0006°®°Èm´ÆM¯\x0017=jQxÓ!5-JÃ(¶À\x0015/IîG6\x0003ÄÈ·LiKJûÒR­W\x0018«®ÂøäþîñtÓãýÍDåÔfX^\x001evº<;\x001aWOf]ê2Êv\x0001¤wï'ÖûÛÜ\x0001÷vw°^ä9
aì\/óô`óK¢
«6hbõÈòÓ¯©\x0018ãfmÍ{ëÏÎÁ`í\x0003â¨èábÅÉÛT±qï$rêN>¹9±ë\x001f\x001c··Ë»ë\x001aRðH¨rÌ¨@\x0016'¹@[ÛáQ´o\x0017G§[@ÍO?ýúð¥[È	Q\x0015iõòáá:m;g<Ó
Ô¾Ã=%Å±3ôÅ\x0003
Ï.¹¢Ñ*\x0005Q´å=\x0017§]­x\x001e\x001aëÍÏÏ\x000fq¿ù&¸\x000fáÓýïïè%=[²µ\x000c>qHeÁ qp\x001a9E\x0017(O	Æ²Ù¶eA\x000fldìñF0øiH(yràjòéM\x0014y\x0019Ù\x000c²ÁÇ#d>m(C2Ê)Ì(>3¡w@6°j;YjïÈ\x001cÍ\x00012viBÔv>ÙÈàãÍd¦\x0013Ê¬FØq¿$Åùd£Ó7£)·Og\x001bçm"³ïÙ|¬¡ÅMÛ±¬MqWàÂ=\x0006ô-Cào\x0017|Í \x001b\x001b,<r`fßéD&#*tbÀò¶Û\x0019`csG\x001e¦MÝÄ\x0000¦D
U£ÈÉìü9:"wôÌ"¡áH|f|ha>ØØÜÑ3ëZ=ñ)ÝHg\x0016\x0018,o}hG\x001bÜ´\x001dM¸Th>\x0005ô\x0001M\x0005\x0019!Ì\x0019£Ã{7kÍhRÐ\x0011?§IQ<@ã¾	Þéùh¨Ïë\x0015:\x0016ûÜÀ\x000eoºi8.0¡9»\x000f:6¼w\x0004Í¦	(jm\x0016\x001cø¤Hqùïstxï\x0019dRU\x0011¢A\x0000;ÈÓ\x0008k´6ZïM»kVA[lÈwxûtó8ÅÄÕ¸i\x000e!J¸"\x0006ðTMVðnøµçðöêèr\Ñ\x0016~Cú~¨ûû?ÿßÇ×¤\x0019 TÐ·V4u\x0005HÕà®Æ?m\x0016°ºÕ°JbYNz34i\x0005-:âofÐ
\x000e«å«Ú§ô\x0017©²íÄßë»¼¹øh6ZT&Õswï\³E5üV£½û[pÑ\x0007\x001aA·¼³võ\x00179ø´w¼üró0MÓ´÷\x0008=
ªäEMãùõË8\x0008Lw÷xñÃÙÑ¦<2bùõWæ{¯¬;`p,ßO\x0014ð1å<½êXÀGíÕñ\x000b\x0001®eé¢¯dX\x0005bM\x0016Ü.\x001f\x0013¯uin\x0000¨bHçÜêD\x0007M1\x0006ÇËÅésHðË»â\x0001\x0015\x0008\x0012ürÓ
Ðþnùézùgyñç?\x001fn®§È,\x0015
uO[i\x001cï"\x0005_ªØ +¿[\x001c.®ð8/0w´Ù\x0003Î¼±Ç\x001b[yN¥»À+ºÙ×:M¼Ê
\x001ak¼Å%èxÓ%h>átY¥Áò]»~ÂjØPª ¶ë'lÓ	¿½½§§u¼|ú:åÖò³)YoÒ´e\x001c{\x000eØ±\x001eôlÞ\x001eÑÛ:^\ý÷&}«üãçøà¾"ë«¯å\x0003fæ®÷ÎÞ}~ÿô¸Ê'\{¿¾½\x0000ñ\x0000ÊI\x0016ÆþþTÀAÆT\x0012
\x000f«[§×IÐsxè«°8ÇÜáÞÙ««óMUÿøõÃgûðX\x0004n:á´w¾üãÓýÝ½o¯\x001f\x001eðïÿytt4Æ\x0019D
$k,ÆJÀ¨M`În e\x0006íäÒÞùâ¿NÎN_ï}{x~¾ïþ!S@»6/Åkä¥=[\x001a©a\x001aãÌi`\x001fðº®c\x000eïão\x001f¿Þ|\x0019¸\x0000E\x0016i\x0013r´j\x0008ð¼H­ý"¢(%¼´ÞûÙw\x001fÍ\x001bõÒ·®@Ò\x0012_\x0005}a:¢Áÿ qjÏ¿p=\x0012Nú¯;%O±9|\x001c!M¿ÂFª	ÃSê"`3Ò
·\x0017uJ)YsJà$
E§dÓT8¥fè¢ç3R°êd\x001aóH:\x0015Ëà)\x0019>¤8(Å\x0006k4ÞH$1®Ô\x0011©¼ÄAÁ\x001a&Cë5ð.Å¤OÉ¤2hdê2æ0%9*Wã<^
	-Ö®×%éËÎ\x001dA0Á"Á»«\x0015oo\x001fµ)dy\x001eøôyïàþsZ!:&ÌC:,-UªbCa\x001eH&Ø´\x000633åÙN`u]\nL\x0006ö°<¯ÂÂ"û¤²µöi¡)`yI:Æ\x001akfc%^åCJö\x0002\x0015\x0010ô\x0005µStµ,NSäz\x001dIE\x0012%\Ê\x001c ®	t±¬ôóO+Éöº»%RÜTk£V§E\x00152ÂÃÍÆJÙ©º»¥é\x0015ÂÿKI\x0003üÑðÕêª\x000bçQ%­SCFjHÊ\x0019<gVÎ*\x000b\x0007\x0017úÊ¹	+m
­;¬|\x0000¬.Å\x000fQ-j£ãF¬:-ë÷\x0013U×únl!»hÕ\*V5X\x0018ó&ËÝ\x0004FG¤
3\x000e÷qÎå¢TY\x0005Å\x0019²Þu\\x000e,¿®iI\x0004pÕè¼r³\x0005\x0004ç£j¸Qè6"$D\x0008Å|\x0008rö¥Ç:P)çqxJ-\x0018~,PÁyô\x001d»Å%3¹à¬B¥DÅäµñÄ¥Rv\x0000îWÐ,$Äüó\x0012!Y7¡?<ò¥È
è\\x0003ÝÿIÁFk=÷)ù\x000fpXòHgç2\h<ºÏ¿Yqýó3\x0011\x0007<~\x0019'ÂU÷d­¦	nÝ\x001bð£\x0010©\x001caÍZÅ`Ôæ^\x001eNRF/\x00057BOåÁ\x00145=E\x0015C\x001a2
<B³\x0019!Ã\x0003âú\x001bï*xÀªÑl@*Cû!ß é\x001bÎçé7÷á·OC¾ÅÞ·Ë»¿]/»é \x001bÕv)\x0015\x0007¾Ö,ÞÁã!1ª­\x001f6\x0000÷¾]~¸Ø8\x0008´\x0007¶fÆO\x0000s\x0002\x001cû$
d\x0007Ä¨\x0010Ìå\x001f[\x0015Ö½<	Ë»ÔM\&-\x0005\x0000®¬¦µÃæC\x0015ØÅ<	\x000c
éCÌTd\x0017Êñw´ó±ÖLæIX8	ÚÐyÙTË\x0005ç¥<ÝyíÅ°óZ\x0005¶f4O\x0002ÓÝtñeß\x000b¬Æ[]ü\x001d|È5³y\x0012Xô)å'æR¿"Ñ|`RÏæbIZ	fÓ:H<1Ï1ziDà«¿\x0003°u~
\x0018üwö\x0003]}ãSñ\x000f.L

Udë6ý$2¥8ýÊB7Ò³1¨½ûYõÈ´â¨.EúÁæk¦ÍÔídåÝgõ®PHyd5&¯.ï\x001e°V`,\x0006guZÉ:´ÀmË9+çz*)Ï§Æ¼ÕåÙÕ9\x0016\x0006L¡KZ©ÎÀ£$#GJL\x0001"¥µ\x0002@§uØ	]RNÕtArø\x000b«l( ÓM±Oxª\x001f:iÆKº \x0016ÏÈa0	!Yd.\x0006ûÊ°%©[ËæR\x0015hbÓ©5\x0008q\x000eá¸c\x0011Wý*ÐÜ\x0008ä\x001c¹ô0ÚgçHí\x0004]õñk©èæYÃ\x0012%8Ç².Øà´«Åó
T\x0016é{oÅ¬½än\x000f.lx\x0019¸\x0002.\x0015\x0011º:\x000e/8º}ZÝÜ>*¯­ÅÃ0PHÎ¯\x0000åßm¨\x0003kÜ	º}*
âÍÇ¬õ|\x0013p\x0002\x001b§-ñq`C\x0005avÂ\x0007ªG¹×k1Ö2ò.ë4sÍQLP\x001b¹Xd#\x001f7\x000bªáõjÊYPøT;\x0008\x0002/Æ,ýüNÔ\x001aÆHBh.6\x0015¡tÑ©\x001e¸.ìG¾½ÒÈgq,{÷/õï×pdMXªØð\x0001sÉn'\x000fXQtM¹Þhâ\x001a-\x0012¨ÐÆû4¼»\\x0019\x0012ûîE\x001dæ\x0017÷û\x000f²0ýï\x001f±ÏíÓõÝãÞíõç½åã08v\x0018Ð1:Ö"\x0001Ä_ÌÇØ\x0013ÓÇgØ\x000cwrxz¹f'Ë±P[\x0001Hmf/\x00170§/\x0018ºÎ^. ùñ\x001dÆSß½8Fùè~¹+\x0013ïe/;N²\x0018²ZÚ\x000fà\x0005\x000búö0eË\x000fX
\x0017(tc+6\x0002\x0005yûÇ¯÷®]¯¤{c¢\x0008ÎÂ\x0003XÓÑÍWÁI|Y²xá7\x001eÙÖ\x0012î\x001eâÀÅ{i)"õ¢\x0011©\x0001ò\x0005#¢E.×ôKc(_ämü|óéï~.ÏñõýÝòÓug@¸è}F*\x0015qxf²c¼à¼ªR};æõÙéâäðâr¤D¸\x0000¡NÍ9\x0008vPâ=\x0008|\x0016;õÓhCsÙQ+åà\x000eøýìÃ
m6lô\x001c2\x0013ðÏ\x0010$¤yx&\x0011{Îº3­]mu3	N9\x0008So	ö®S\x0002K\x0004¹O95Í9G-g\x001c	.Å?@ºÅYôq°!ÀSäMÓÇQk5\x0013HÂ\x0017'¬xf&|Þû~ùð!ÍlØûÄ	§\x0014ß\x0015û\x0014Þ9Tï\x0006êþ/ö¾_¿Æ)
\x001bÅÞ
(éà5Ð¯ú÷póµÐ¸ßß?á@Ñ\x0016ø:é\x0015®\x00016]2RJ(Õd|vÃ+¦0pZå_
a\x0001ÀN\x0006gµ!\x0004<\x0013l:G
\x001fRF\x0007(l?Ë)6]Ø\x0015\x0005ÎüK)4¶vÿ2éÐö\x0000ÀÀ1ôEÒ{EÍGÓ!¾üö\x0018Ä}Ù¾»BÐÈõ°ü4f×Á-;Êîë$äáfpúc­øñ\x001c{6ÑÆu¾8Ùx?n~úCßûûÏËÑü{à\x0016\x0012[ èÁ
ö|\x001a©²
\x0014]\.6þã\x001fïïe3K±Æôøæv9^éeH¼\x001bVyà\x0005å¸¨\x001b\x000eÛ^ì\x001d\x001f\x001d/FÊ&Âï_úy­½æÕè6ÍÀäOàCQ³ÙFûu)öj4`ò7ýîAøîÙÂÿ&þ ÍåíÍ\x001döxm1Á[úB\x0006ç/¥OÉJ@í[=8\x001f\x0016ÇG§Ø×µ±ï¬ W*¤ \x0002\x0017ìÂl\x0000\x0012ÁõIH^ôó;õHl£ü«\x000féÝÏï\x001enz\x0003n¦¦&#~R\x0014\x0003Bå\x0017Õ\x00131Ç«Ê±	\x001c<Îf
\x0008i"Æê\x001e.\x0014ÊS,\x001f7gTüvÿÉ,;ñv\x001fþy\x0003òvùîúv4\x0011¦j\x001a,L'\x0002ça(?\x001eíW¼\x0001»xux|¼ùÓ¬H\x0002\\x0014ü3ÄåÂ¥#1´NJ
-l&ñ êÝÍÝczHðaðÏ18Ë÷#*\x0008ã9)Ge
nÛèT\x0010\±ô~¤1ý\x0018ü1¸\x0000\x000fêöç_ÊXç¤È\x0017ª\x001f*pÂm/I\x001bGËEîZ¸~9(Ú5\x0001K@\x001cM\x000eJ\x0001uÜã\x0018r\x0008.ø\x0019 ©Ðr
\x0008(dF\x0014àÄ4À\x0005§ó»\x0005\x0003£\x001d\x0004þßx1õH°ë¿ââ3ø?ÂÊPg\x000fw"IêÛNÿ:%#¤\x0011\x000e(]Ö\x0010r!ê×AL`¹ûûï×iÂ\x0004zJø\x0007þ'÷£\x001dÎØ+áÙ®>\x001d\x0013\x001aÝ}õÑFâk\x001bü³«\x0011Ùþå÷\x000f¿Ýv2\x0015m\x001a\x000fóöúîÃòëM·k`\x0013ð
ó)(Bp¥b:\x0011\x001f#\x0012ÿz'²÷öðôõâ¿AÕl¤¹âuWæ\x000eK4`Jr;vS@íå"2J×Âã«"2¹\x0002f$\x0018*Ç°ý]>ÄÂõl;â¨Í\x000ftLÆÄ\x00189V\x001d{wäys#\x0004JBü3¥æ\x0004\x000cu|HçÒ$\x0004\x0011}n\x0017Õ±¯wk(àáãIgasâ

\x0011Ý`\x0017\x000c\x0015ÿöë\x000f*(\x0002|Kü3©þ¦Ë\x0018tgº©<(xöÃcl¦\x0000\x0005¦\x0014)¥=£)Ù,éÍF?ÍýRÂ­\x0014æ\x001d\x0012¿w¯\x0004î\x0004þ9Yþñ0Öèi0¡\x000e\x0002þ3&Tð±\x001a4zÉËêû\x0015'ÿ:_n\x0004èa/±úrûK\x001a¤¾QÅà0	ªxSFPÉ°_\x0011·\x000f_í\x001dl\x001e^ é\x0012IOE\x0002ãg_È|S¸\x0000Ûd\x0011²öjjt\x001fi2\x0013ø\x0012¹h1F<±T|Ûä@ã÷$¦<Æz³l¶ÌPIÍzÚô@Ï>Qm\x001e¬¨~üé\x0019×O?¡ã~\x000cÉ{°\x0000ÌæTá@ãþöÓÒdQ®þ¢·MìÏÿM[º6\x0007l-á®«´9¦ØòÃ\x0013Ï2¶-å*ÀL	fêÀ"ËF|¤'QÙ¹ÏfT¹ÌUVï!áâ0Ü±ÃgÖï\x0000¯%\x000b%Y¨"2ÍªLÁ*êÔU6é9\x001fS\x0012L:²6î\x0002\x0019Ö÷\x0013\x0019MB´0ø*§¢õ\x001e¬{\x0001feFãær\x0014ÉÌ"ë½\x0000Yõ\x0004XÅ·tÌcm|\x0016°v L_Ö{\x0002²ê
(á±I#)lCo>O\x001bg¡õÞ¬z\x0004hÛÕ0 Á§ÆnqzàP½W ª^rÁAY\x0005,C®¥·³Ðúj ê\x0015(¬Â¥W`ÓJ>\x00115MÑÄì÷\x001c®Þ\x001bPoÀä®A×)I_S±L\x000bbÐ\x0016Ö{\x0003ªò
h\x000e âÀ"Ço YP³Ðzo@Õ)\x0002PQdÒc}+µE(»:µ8G\x0013èÞ\x001bÐu\x0000\òÈJ=(\x0006ÍØ©\½\x0007 +
¡°\x001aÒ\x0015¹Kå~*\x0013å\x001cfzGfêÌæbyåbÚõÃ\x001bË\x0017mÐtÖ;5Swjà*q±ó¸"'¡e+-ÈYh}û±Î´*;°{'·¬\x001a?G¤Ü0uö£Í1]0\x001aót=Á­\x0019Æù9\x0016éÉ
S'7°ýp°8l¥:\x0007\x0006ÕM'³½7`+ßä`«ZõaòÚ\x0018D³Ðz\x0017ÍV^4\x001bä´Ã;GÏM¡9ZÀö.­»h®\x001b6È­&- s\x0017\x0019clEëm/LQDWpÉ\x001f£X}\x0001M¬tË\x0014ÇtCX¸´ä¿¶C¹\x0012ÊM*ú¥ð?²ÆÌ_Q\x000c]¯L¡d
Èc8Ñ³cÛg\x0015Êj\x0006T,¡ât(é8R'ev~CîËÓbH®Ncºw£ôt(ìbÚ5ùvæ«\x0012¬\\x0018rÉ'R\x001eNtVÖåYÚä¹zrÆYÙ\x001e­ <d\x000cGnò8/
`lÃ©_°ëéÅ<ôoÊ´Ù:\x0004«\^ÌGóµ\x0006½\x001ezÕeèu{þ&(c S©4X¨<P\x000eÝ.Îálå2%©ábe}92\x000c\x0003mÒêæ6\x000e\x0019\x0012¹lÉek¸]WHëoàÀr¿ñaÈÌ\x000cæJ0Wõ!³ð«Ï\«LÇ åK,_\x000504fÕ\x0018ÓùEÎú¡ä
UßQí¯¼È4A(\x0004ÅIeà\x001aÒ?¹bÉ\x0015k¸"\x000f³SÁÐè§\x0010h37ºjqÎ©\E\x0013\x0017*\x001a0\x001b¹G\x0005E\x0012\x001ftcÈds.=0Y\x0001\x00161D
28¿ë\x0007M\x001c´R'©\x001eªºû:«îÀù`¸û.Í:²lUÂ5\x001aî±VQÓ\x00083\x0000y^Õ`@`2YOÉ\x001a)\x0016Ív}t4);D®	²b0\x00178\x0019¬'.d¼øÁLÏ¶Hß³°-¦|Re:O­ªd¸&Ä
ÑvÙTZg²z\x0005èÔK\x0002N7i1úfÃGïSU\x0004QL\x00003_lêoØ\x000cp²8êí@_G%R¬BBjy0K(9ÄÑj\x001d\x0007Ôå\x0014¨B)ûM9G{ÒA©ìm<\x0017D+®ÿ2j ¼?J÷¨tõç\x0013d	Ï\x0001W?j=*Û²uPÎäÙ6.a®ö¨ò èÕ_¬~ûÇÃõÝÿÜÒcÕ$fßçê~#\x0000fh¿ý¯óÃÓÃÖ\x000bf,UéTR-¤¡íz8¢ÄÒ\x000c\x00060b9®m?a_\x0007©ÔºÄPi]Ç³%Ú[x\x000cûq\x0012ä\x001ag\x0007E»/ûÞåÛã	+³\x000b4]¢é\x0017fJ4ó¢Ðlf_\x0014+ÑÜBó%¯B\x0013.R¿Æi\x001a\x0014¸\*`ã\x0008Úæ\x001fB\x000b%ZxI§Vø)ù\x0015/úô[Zïó¯'ë¢WªÕ¦¤é6~ö¢&deý* ûl¸p¨­T.ë\x0012Ó_¬¯¨øóÿ°¢"é}ÑPEzs%Ööãþ½ÙÈc%áNtª®û´ä@<ÞÒgub.\,áb%ÈKÌ*¼
W1Ï\x000bÃÃ+§ÒÉþ­ü²båâ¸|.nÔ<\x001fØy=<Xv*^Ð%Þú\x0014øíV§­|øiu\x001aûÕ=\x000bÍ§×·Íëñl\x000fÏVâáö
\x001eR¯¸{Q\x0006.vtÝø\x0006¼w8Ü¦4L^uRêo^_Ón¸ÛrqìXy\x0010\x0014\x0014Gö­ªp}w÷úÂmÝ\x0017»"t²$D+ûÅ!ú\x001e¢¯GTyC\x0006ÙL^+Æ·\x0012¢ïä&DßCôµØòG%àEð1
-ø\x0018m_]\x0013cè1jFPq\B\x0004úz\x0013à	å]ýXætFõãÏnùëÓ-é¹¢ÿøbys÷\x0008lï\x001fï±µG»¦¾Áù-»\x0007Eþô¹Ã'\x0001iÔ"\x0012·À¦\x0000vFÒq\x00027|¥§ß\x001e]]änäÅÑé%0\x001e\mZýÚCLíz/\x0019ê\x0019#¸ßÝ;étj\x0017FFíÓ<alTa\x000eã¯ê×[Q|éW÷Oïî¶PYm÷}\x0007å¤MÁ0\x001f.A\x0005÷ìÜ^]ÁmÄø»u÷÷×\x0005\x0006\x0018{7wï¯ÇI\x000c!èÊã¥^§©@AêTp8£|\x0005½£ÅéÁ&\x001b´·tNÄiî"â8ú\V\x001e!®ëã\x000b3ýÅjÃåç½Ë\x0007øfË\x000f÷O]{Ã\x0008òi`D÷á\x0004²ù\x0010Tªí¯få3:\x001e,ry\x000eßoñúìjc³CÁ©KNÝÆI\x0015üð2Á¢RJá:@5´{.ª-Qm\x0013ª©Ð\x001aP}H!k\x001f|tü\x0016ôó\x000bØ\x001aKÔØ
ªÌ{:U\x0017Ã©\x001aOÕÉ] ßË\x0017U4±\x0002Q×Î\x000c¬8ê×Ñ
`Ù\x000c2h\x0016ë\x001föÃ§GU\x0008\x001cpóxýp·åÃ?7¤µf \x001d|û,úvÀ	ã]\x0007Ã9	Gç\x001b§õx¨é{*\x000f\x000eR2¶ãÁNLÂû5ACøøì\x0002Ö\x0001¥ÑêÓ¬MÁc\x0000R2í\x0017ð8ìäMqZ n/v\x0002ÿä_Q.ßlQ¢ØAª&¥×7A:\x0006	kp"É\x001aÑ	ü:Ù¼qý|\x000f)}´:$KD>ù\x001d'¢´Xj\x000eQjÙN\x0014BL\x0019héÁ\x001fÜ·1©.\x001aH.àïº¾¼9Hé"Õ\x001cÄª}DÂµºQwH6¦<ünâÙ[«CâÎù
&O±\x001bør¸3>!ùäàÃÿ½n\x000eÌf¤áp¦úñáú\x000f!>òè\x001aÛÝÇÛ-¯ÍjåS@Dbla_v@25\x0002pýóÇv\x0008íôÍÆù¦êGýôõî²4]nf58ùÍòaùñ	Üëm2ÜZ\x001c\x0005¬@¶\x000fN¤X
°©çZ|5@ùÍâ|ñæ
\x001ci\x001aõãWñAê÷Åu/¶¾?Ü§®ê1Bº;B\x001c\x001e¥\x0012!\x0015KñêÙ/¾m\x001eV¤~|ÿËÏ\x000f?ýÞû¤÷Þ.o[\x000eNx°"»ZWipÃu²)p<@ú¨
\x0014ás\x001di­ÅñârL?Û¸fHÂ+_\x001e\x000f¦î\x001dM\x0019=:° 4}\³HvO\x001a¾\x0002'\x0017õ³{×\x001b
\x000fâ´\x001b\x0008³V´ë³Ú'Òâ.FK\x001eÕi·\x0019¢plNÄç'Ú«KÜõÅ\x0010Sq\x0015oÇ#0d×áÊTp/g£×WkKÜõAîqUª£M\x000fiÙZ\x001fçÓh^wt\x0011uï\x001cêÿâP«àd*1A§¿A°´R\x0005}~óÌ\x0014 0ã$:ªT5\x00062\x0011\x001cÉ®\x0013Òcá}veHuIª_òÔ´z\x001cÄ*É\x0001ö©Ç\x001f¥éÊ\x0007öÏ®j\x0013ª-Qm\x0013jpûä\x0002\x0007j(4²b\x000fú¹bo"
%ihúü8S|5\x001cî\x000eg
á÷÷Ï¤U\x000bªì½)Ùö¨D·,¸cµ1%\x0006UjöånîªìÝUÙvYÑ³st\x0005tß\x0001W HfÕÏýõ&ÖÞem·ÕØÔk!Á5í\x0001§y¡M¬®ÇêÚ\x0004«NK¿P²\x001aìàO¢t Ywò²¤ï¡ú¦c\x0005ÍJá_WÒ²je»%
{Ï\x001a{¬±UÒ$V\x000c/Å´s\x0006#a¬°BN8UõUk\x0018@\x0003+³RíXg`åHØn«üñ±\x001bVØ,ø\x0017
w\x0016\\x0002î¬ÕÝ¨¡$c-½/¸¿f76×¬.n±ú¹ò%9Wiåd:c³\x0004òsÕfÀ¬#ëFbl#rdÇ`¬4Ýà¨
¿¶4hk\x0017Äk×B·^\x000bIç@ì"YÞ8ëÕsÿµ\x000eXsºÒ_¬R\x000fisÃÃÇ)Þ\x0017+ÝH[;ïKçpþÌCÚÜpþfÌ5Ð¼ ¨@TÕVd\x0013VSÅ+ê/6\x000c\x0007¨Õº$ÔÕ:kXuÃ¤
T`Ó5­¼hJDS½wt\x001b5Eìm4|c±|±äõ\x001fYç/nå#ÊJ&4Ïdh5a_âw¯\x0005ÿ¢ö[+\x0016\x0016üK\x0005eøÁ`ó|ÒRlv¤¹Yc:©r\x0018sd\x001bU\x001bV¤l÷i;ãLMX>8;!÷»,\x001fÞÿüç?·\x0005ªæXÅÎÚ¤¼ÉxnBQ_ÉÉâüà»	|ºäÓÕ|*­6è\x001eMZ1\x0007|:dÉ³á[Oç3%©æ\x000bh\x001f±d\x0014ÎÏeËcÃ\x0017ÎgK>[Ë\x0007:Äl\x0019Q\x001c\x0012ÇØn4*ñ\ç\x001a®¢ã\x0003 Ò}^Ç||Ïk\x0002*ù|ÉçkùpXÎÎ{ óYlûç\x0011J¾PòêÏë³bFYC|³>èæç+Ýx®WÊ»w\x0000\x001c÷O[¥ ó*ÕU¦"\x0000þÈVælµØä¦ ÄÿÿåÙÕ¨$$T]¢ê&Tx#K+d>O\x0003 i#Þ|T[¢Ú&T\\x0018ÎÁ:óG~\x0015¬S" U¨²\x0001n@W\x0011Åé\x0010ð{\x0004È\x001a;>OU6±önlº\x0002\x0006§îQP\x0001Ë,Òm5Þ²F\x000ca7·µoat«pÌjn\x0002èH\x0019²!\x0003ëH»¹\x001a¤Ø®[\x001a6ô3c+À"ËSïyxTp¸)?\x000cÎÙH¢iJ1\x0018ªT5bñ­L¤\x0012\x000c@ÊÉ\x0006ëFÒ6\x0015¨¦D5M¨&\x0019KïMÑEÔR\x0018Ì\x0006©wsª¶DµM¨Xj\x00160ë	¬lHó\x0010ç£ú\x0012Õ·]\x0000Zl¨\x001egr&TÉ¨Þ?óØPc\x001aPµI\x0003úñ\x0002xªrömã\x00050;A}\x0001Ð&\x0001'ñê1îe
±
ª6òîyH\x0013«î±ê\x0016Ö(iôZ+®C2èª§rtH%ëz\x0000Év\x0001¤ï®Oh\x0006¾]~Æ;¾úuÛÁ\x0006GA[\x001b\x0004ãr ïÍ³§õÝâäpqÖàÛÅ\x0005þÛñÙÕÛí¸ªÄU¸Îä{ \x001c	WÒ±p	vDªKRÝz°â\x001e·>±Ì²iÝ ÀÚçâµ\x000e÷Ðªw\x000f^u³@qÉÏõÓÞëG0\x0005>½KûÞ®\x001f\x001e¶\[ç#ËÐ{ê#vµ¬R\x0003EG{t	æÀÉ«´\x0001îð|ã6É\x0002YÈº\x0019YE\x000eà¶nm_Ð^\x0019:c\x0019Ý3?u\x0013òÖS¶%²mF^UG/R#  kÖ\x000frÀiFö%²oF6ÙP\x000c ÏTº\x0018Þ#f{®EF¶&$DäóÁòîñ~ïíõÃß·Xµ¸ªÜÁÁIå>JMù8PJíÁâôòlïíáùëó£ÿÜNiJJSM©¥bpZPæ)j+½|\x0018\x000c°Tbº\x0012ÓÕcâ,F\x0019ÉYÔT#Pr¦t¸`|*¦[\x000fõ¹Ðáÿpóñî~B­s|ÆÐ\x000bõ\x000b\x0004.³\x0005ÿáyVl\x00150ýáèÍéÙJ©u£Û~$"(ø¹¨Kzö¾£ö\\x001bÈ;\x0000u%¨k\x0001Å^ôåKs±ú(\x0007xýXX:¨/A}ÓFÜ@}¾\x0004 &^¼\x001dI2M\x0006-lXlØúK
\x001aÊø\\x0017k(ã=G3¼ÞÅ'amxÎTRly ¸÷i\x0008\x0018©Ð¹ÆXlè\x0014ª#í}|ù¿¾êI(Õ"¢B°Ü'ä¤4x\x0014RÙ\x001c\x001f\x001aI×N&Õ}YÚB\x001a-õéâ×w¬¤à:\x000e¥3I×#ÄÎõÓß\x000fËOµÜÖ\x0015£i¡\x0019ªQÎÔ{ãsÌíy5çôò|M\x0004öÌjJVÓÆÊ

®,Õ\x001e{+rMü|Y5©+I]\x001b©ñ¹PZÛä¿böGp8¨
mbÓaíú\x0015°ý+pqÿô°ÍÑÆÐû\Y"Yú¬ô7å ;Ì³«óñþÐrè\x0007!ª\x0006ÄU\x0011NÀ§\x000fï%\x001bzÝÒå-¼©\x000c©KHÝ\x0000é)`á¬	\x0019Òq?t\x0010zÄ|z¦4õ1¬ %{\x001d$ü78ç÷<°V\x000fiKHÛ\x0000Ic\x0018R^7r\x0003\x0007K$Ð¬#²s*¤+!]\x0003dVï\x0016÷\x000eRb-H6DÄµ<\x0015Ò¾\x001a\x0012+s"¤È)µ rý³#²}*d,!c=¤\x0011(vº¢W\x001caL:\x0017¿è1U9\x0011²ìüµEçïtJérÉ³4\J\x001eÍ­\x0004;xÞ²'d½\x0010ÂJWÎ¡\DMÀüÁÃ\x000e({ï[Ö?p/-7\x0010\x0008»:JÍ\x0007\x0003aèzÈÞÓ/ôíÈÞÛ
Gé,ÐEÑ¥¹HÂ=ï­¦T½k©\x001a®¥É©}ã<þGêgJ-G¡ÉVF¿ÚÖÒà¸\x0006c#pYLäjFï³!6õ÷Oc5ëFyÖèxq}ûe[/;z¿]\x000cn¤ E\x001e#mP\x0015\x000e¡Ó#\x0008zxüÃ\x0004NUr®·8Ná\x0014¸ß<5\x0001ã\x001eøä\x0006Yöc\x001cï\x0016ÜJ¹Þ6êÖÚF§W,ë\x0010\x0015õâ;\x0003Ê½ë\x0015\x000bBå!\x0014ðFò£SË¬×\x0003´n­st:°Á}ö©îÖ\x0006-)K*æ\x001ak9PÆ^
,Ö\x000caË\x0013~Ú{uýûÍÝ\x0016R\x0002 ]ÂÉßCy$'IÅæ£½Ú{uøG§Û\x0011U¨j\x0011uô¸Á\x001cL\x0019¦´XH\x0003øç!\x0012ÑÔ#
\x001c¦Õ"Ðv\x0001Ñ\x001a®àØ\x0011ÝNØ\x001bÏþ 7ËwËÛ\x000f7[\x0003	« 0DäZÜV1\gýfq~ôjqüúh;/ñüÃ%^|AxëctoL\x0013 >Ü||Ú>6\x0001
ÀØFû`Ïy¡
\x0015\x0017y~ôæjddBÆÔ%¦nÃ\x0014%ô¹ÝË:QÉ*0Mi\x001a0­CÛC\x00140\x0000{MqpSÛD\x0015¦-1m=¦\x001d]ùôÑMîQo\x001cÎ5\x0005Ó¯÷Ïû®þû½i\x0013ßÀH³\x0014hS\x001cÀø8*ø|`Í\x000fgG{[æ¾Áq­Û\x0016º³-Þ<,ï>ìÁ)n
Uº\^\x001dlZÑJ»j~vnoÎ\x0017§¯÷àô¶c©\x0012KU`nQuÂòiè5©\x0014\x0007Qõó\x0012Ë
,]béÓòÙ½¹Ô[ÏIRó¼©¼\x0002ËX¦\x0006+¦ÝÆåVåÓ9¨÷¼!·ÊT¶î°ò°<EéyÌÒp<Ô>W\x0015\x0015X®Äru¥Bn	æ~Üg\x0005"øÜe×µíi¯·7\x001f¯ïï¶1ç%\x0016[I\x0007fx,ä¦N\x0002\sôæðìttt
áõ¼Ï\x000eqå}N¦\x000c*·Òñ\x0018d|Ùß¬`·\x001a¹öyÌ·+Ìà\x001b¯º	p\x0015'£ãfPÏ\x0007¨u_¸«È\x001bõÃº_\x001c\x000c
ú\x0016¼ö½?ÿï½O[j-\x001c.+Míi\x0016\x001dugÅk)ÙÃY¥Ïªl\x000e÷¾\x0005¯}o#Ö¯Æ*-Ìº£az\x0006|åãå\x00178Ì?ÿñ°U¯ZÂ5ri4MË\x00141
æó$\x001d¿¹rø\x0002ã\x001fà\qlîèÝ\·ê­)ÚÀÞ.\x001f\x001fn¶¼\x0014«N\x001b21\x0010û\b\x001c\x000ea\x0001ÞùâõÑè\FµöÙ*\x001b]öÎo~]>}Ø\x0016d\x0000H;-çó¸\x0016\x0003öù¸\.Â¿Ú;?z»¸z½QªQE\x0013ØÜ3Î¥\x00020\x001f»)°\x0014\x0003{>³\x001eRº\x001e\x0012D8
·4ÑpXI*Orcy\x0005¤)!M=$X¤Ô\x000cß²§´f5hcÏÅtHWBºzHaöÝêN¦V\x0016px®\x0017ÜÉÝL\x0013 Ãzú?téÿ×÷7w×u\x0005ì~éæ\x0014[KEá\x0014øÀ9ÅÏ÷ë³ÅÑéáÔJkU%¬jíM1Vß¬
1~n÷Ô¢®wÛ&z>Ý¿|¸¿\x0001u~ýôëíÍõ¶i±\x0006\x001bâi(#6	TÆÎ	hxv\x000bNÎ®IÈ_\x001df?¼z{\x000c~TÐ¯{QV³töðÓõ	úHÐÒ*Ìºª\°\x0010y¦\x000fÃ\x0006ÎÎ¿=üa\x0016Z\x001f<f5W\x0001Ls1Ë%lEÖ\x0004\x0007n(ë çz}"YIÆÖåñÍírëÑa%ÚªÑ\x0007 ä¡xðî7mÇGÇ	xªÄSµx+<DLKæ.æ¸öóÈæT:¹Þò%C¦Ãu8KÚ3~ñ"O>3X5¥8gÉR
Û­ûæ\x000b@S\x0002Z@§\x001aãótjÌ&@¹a~D\x0005 -\x0001m5 âÁÏ\x0006\x000fùè\x0000Á/ÛÔ(=Ï|®á\x0000\x0003>aG\*~\x001ezC©Ä$¾u\x000bW2fx°ü²]¸U½	\x0018åC"¥ÚØhÛ]@g¾õô]K¼\x0005ïæ±[=:mâ¢¶\x0011÷ø¤ºG²À6\x001bÓh`ss¹q\x0007)2©u#\©bØ\x0010ÿ\x0019þ\x001dmó--Ü\x000e£ÂI\x0010\x0006öi¼XUîlÈ^uÿÅùEú§l®Õê-?$TÕj¼\x001al<wÚ¢ÙÄû9\x0005uë©ê\x0012U·*§P­Q<\x001bÆ\x000b\x00161\x000cG³kA]	êÎÔ\x001cò¹NÏiÉM\x0013/êPû±î¶\x0016Û|«Ö¯JÍø`s±Ì¦©;Óq×#WÊ\x0015å.»q\x000fÜpBÃØ<b-¬ÖÁÈçV$$/µ+ u	©\x001b qÀ&AzËU{d)ÿ<°\
iJHS\x000f35i"¿ªt¬*½~Þ­[\x0001)Ö?·(äèÁVoA9¯s«\\x0015\x0015Ú\èê\x000bzÖãþAX×CÁþâ´áßFÐ\x00176¸Â+Åw	R~ þÝ/\x001a\x0000¾i­\x0013ð¬?à{\x000eíÓÄ¡ó`
¥J®IP¤Ñ\x0008æ.EÕüóùÙE¼âéó0ßÉô\x001dßÃWð\x0017Ýþ¤é:DÊ6°mM¦\x0006ÜÈáy%a¯XcNþxûóòÓûrcÒâK÷2Nîï>ï-îÞß\Ã¿cÓâòñqy×}î \x0012§ì8oþüÇçÿøð,>t¨\x0016\x0019A\x000bÑÄ½,@j¬\x0008éIK¸¹Ýâ\x0008l¡×{«×\x0018Å·rrvz±\x0007¾öÑáéE×¾¸¸¼\n\x001c\x0001ßOæÃ²\x0014.Á\x0007º¯"ÆÉ4(j÷ôißÆ|ú¨RÚ5Ñ§£)©ìþ/@O
æ£{6_i,¦Á\x0013\x001d»¡]\x0000¯þO;<fÓ\x001bëh\x0013%ÐË4áÎXeÒ¨M _·Þ%=\x0018\n\x0017ô\x0002ï
ÃwA\x001c8z^ç¤Â.áá@ü\x000eà­´)7
ôNì'x-=±«lèî\x001dTVØÅÁã`DOì.Íok#M>ù\x001cïÝ%=<¤¸W!å\x001d5fÎRú\x001d^§\x0016@<{÷\x0017Hz,ÃÇ?ó\x000f\x001f\x0013*1_.Ø\x000eoÎWç/ G%»\x000b-^\x001dKkRl\x0013ÎÞ¤iG\x0008ÿW\x001c=mÏô §\x0014I\x001ckÓ:48ú\x0010X\ª\¸K|8\x0012¹\x000b5­Z/>\x0006UÒáÛ,sä_ sÐ\x000b»Ð´\x0018®êÒÝH/S1Ð+­ø\x000b\x000eö=È]¨Zë|Ú&ÏÖ§(à\x0007eæ_aæà\x0017»ÐµV¯§/Ò´~<}Ë\x0006¦²Å
\x000b¹\x0013m\x000b^º&|ÜAøQ°u/ÿ»\x0003XîBßZ'SÎ\x0005èuHsòÞk¦\x0017ñ¯À\x0007e+w¢pÁ¦W:ã{O\x001fÿJzðU¿Q»Ð·8JTòá,5£a¹óW\x001dìV;Ñ·Á¥)\x0002HïRBÌXl§`zÿ\x0017h\\x001c^ªv¡qqÎ¤§ÃW!µ\x0001 >½ñ/\x0010
ÔÚÊ©o	à¥KÕ\x0006\x0000O\x001dA@\x001fâ_qö Õ.4\x0016nQ|u4+\£=[;xvoå§xw\x001eR:ÛÃ5©N\x0013D&Â¢+s`¤úõ.\x001fÞ_ÿºþ\x0003îù=|¸-\x0005Ï1p=|J\x0019ÃmGmh\x0017V
KTèú´?\x001b(£\x001aÀ<Þ;;Çño\x001bRH=(¸hø§\x000eÊ¤\x0000%\\x001aÙPYå{1ðøj àúà*(ôôé¤À
É°u\x0018\x001fp2Ô¦ûW@Áÿ:þ©Â%Ò)«\x000fPZðK	nÀ/¨9)PÃø§\x0006
Û£§;åS\x0003\x000b@YË\x0006g\x001cR»[¡¢ÿ¨¿Þ\x0015Wdúîþáñz+ðÅºmZ\x000bð¼»cr"@ T\x0007/ÔwgçR\x0011= ÚÙürRñ\x0005\x0001¥ÈÛ\x000b\x0002J\x0011©\x0003ÄaCÄ¦`
VÉîÐ\x0002\Ínc\x001d\x0010Që\x001a\x0010<+phëÃÝÃ\x0017HÒwUËZK\x001c\x001a\x001b\x0013|HÑ
íÉH\x0018âÁ©A\x0012ô\x0016!*qvV\x0000ó\x0003¡û
&|Ê÷ïB*¿\x0002&\x0015HçÂá¥ê\x0017`zÀdÜÆd¾»\x000fïJ}ÿxóùóõ§ë»Ç½Û®aãnJ®CÊTæ\x00192¶Ì\x0018+rÆ¡oxvytqqxrxz¹×mG>ÚØ·Ñ\x0003M±FP\x001c=¹Jå\x0005\x0002µ-\x0017;h$4Öi"U¸¹mlÓ\x001cÓzè\x000e6:j#E\x001bØûbB\x0007öâÞá¦üV#)|}6ù\x00035\x0017\x001b\x0013iWIO\x001cð[ZII£¶zÚ$ðL5g°LªÃ@P­4%®\x001aIå*Q@ÎÊÐ\x0011\x001ftP\x001aIÉ(h#5´1|}ð\x000c¤\x001f	»{PÙXh#\x0005O/K)Æ{\x0002©ËoßÚ!YßJ9Ö'eSß1¢TôO#\x0019ÞÝ=~Î\x0018´¡Êhr^58S¸ª}13\x0014¨nE¥ðz+jÈ\x0001\x0016GGª\~ûbÈHkä¤Htë×7³3Tì\x001fßäØù MÒF£'¤~ßú,¦\x001cþ°\x0012Ss\x000fõ7û÷Ç\x000f\x000b[ª\x001b
tË§ÛÇ	¦	2òY<9\x0012ù!'M\x001cxIÝl Z\\x001d_N!KÆS-ÈIØiÐÌç\x000b¹êhA¥:2\x0005O:\x0010èÖôud`\x0017ÓWõCÈZ²d\x001cUÔùÌ0ZFFãûæåÀË¨\x0005K\x0016Fåès©\x0006ÙMõ`BÛÈG6\x0014öDöñú÷»/ï;\x0007\x0007³sø/¯\x001fï®\x001fn¶?Pgp|dJ\x0005E80|.c©à(\x001a=$_-Þ\x001e\x001fm*©\x0004ù¡¬ûô§UÌøçx¹÷êþáæ~Jð®«Ãvêèâ¾NaNÐÎ$Þ¬õC2c±÷êìüèl
\x0012ü"üSdº	W\x001d\x0012VI8¼*úz\x0018\x0004ÿëø§\x0002ÉQÅ3	¥WqWvþp3O	Ä\x001eþ©9%v<\x0001ébé81çÔ Q²
é³¿ùùËî~cî\x001fÿåø\x001a>¿ß~½\x0015xÈIºk°b©@Äa½=]ïh\x000e\x0001éâ`s­«ùô÷»¿õC
Øîs»üº2·U \x0008üv~àã\x0005Aþ°Cr
UáÁñâm×¹í`Ñ(
DÄò¬Ø}Àc\x001c²°\x001d\x000bw\x001b8BX
> \x000bd«ÃYÅá;uS\x00166"Åøóïúk¡¡O×\x0013d¦\x000c2ç;°\x000bì\x001cáØrôz@Í,.\x000f/§°$<E9ú\x0004Q\x0019GN\x001dÂ!s\x0004c5î®%iá©,88R\x001e(¦iqp.S.Þ\x000fYªYzÈbtà:g\x0001Gä°\x0006ãÎ\x0005dÂþÌ\äÉ÷Eáâ\x0010.ÄóïK®essX\x0013<E§^\x000f4DTA\x0003JözÅU9\x0015}Ç\x001a\x0016öÀ|ËÛÁpâÉ\x0019çÂ\x000eÂÔË»Y
ø^ÜAÃ÷eÐ¨Æ\x0002Ï\x00118Ò¿N~J+{\x0011\x00051\x0005'¼È\x0015\x0001a Q8óá\x000fóî\x000f];ÐVoo>Þu;}·Ö¶DÊ\x0011J\x0017h[Q£b\x0018ê\x001câüÓÍ\x0002¸ ¢HÎt"ø¯4ïBKìi!Ã\x0015\x0007Ä$$ð:â7Ó¸µ	»ð%R`Í¸H\x0017Z¡Ò½éL\x0012©ûO\x0007OÍV¯ö5\x0015Æpð\x0008kOf0w»\x0006Êz\x001cþÖAéÈ%\x0003ÚgCcÐÌØÂ´¼ûxó5\x001e÷òËÍííý\x001c8\x0016ª;NÌ\x001bNÌ£¯Æy; ºÎ\x0017?\x001c\x001d\x001f]m$Òâ§ßÌÓ³Sº¼~xXÞN©I±Ô3"q	]ÜuÁæ½\x001b~uççãT7áë­{ß3ï¯÷~Z~`5\x001aø{xV7?_\x0005/\x0017ÿTaY±b¤Âë}2ñs´ÄY9TXQ\x0003\x0005wâ\x001büS\x0005\x0015M\x001añ
TX\x0007Nö´ö,ÆõÐµªÃj°¼ \x0005xX´Õ`ÕwàÓ2Ã2¡\x0002\x000b~5µXn©"÷\x0018Y«lVÁ³©0]dk©\x0002	u0\x000c\x0002Î­IXÙ2pvöÕ\x0002Ó\x0002ÿÔa±F\x0006[\x001b>çzÕs>Q\x0015\x0016H\x0006[)\x001d¼ðäªÁiÕii\x000e«\x0005\x0001ÍX \x0019l­t\x0008«ÒE 5~\x0018»ù#\x000eÆ{k°°rËÉJ,¿2ópQAß¬â+ïgË\x0007T\x0011®Vl¹Hq|\x0011=\x000e 	©Z\x0015ë¨@b¹J©\x0005W'\x001dÅÃòiQ3Z|9º\x001bÚRê°à´]¥ÔêÝü\x0010\x0003\x001b¢>ßø¡âÝ
¬5ãa2\x0012àÑt\\x001a&äê)ÎÄ<mûÕñQ\x0015¡³Û/×\x0013ªVl\x0004º+p\x0000\x001cwÔèé\x0019ªÁ8øÙñÑ\x000fTPÛý+±Ü=Çw?\x0017&\x001fïSNã\x000f&×\x001cé´\x000ehÊ\x0017\x0016\x001di.¦CAp^©S\x0010RYÍ(_
¥4ñá´é®X\x00043"\x00050Q\ìcÌP\x0013h%_Jk´\x001fø=BS\x001dìöYÀñåº¶ÁPK%]
þ´ÑaÂ%}]\x000e\x001a×ÝQ¨Õ\x000eØÐpÉymsîê¸RÌÌ|ãÚ29Ô¥YÇÇÕ\x0007MJ	*çÑBr\x001eÒIïøøÄPq
 ýüåÓû¯eÑ9M<¾ºù¼×ò_?b5?Vòï½àUFÁï\x0004¯dd_7®zX\x0006\x001b\x0011º\x0001àÇ\x001d]¤bþÃK¬çÇZ~ø§>\x0007\x0017`4\x0017s9Ò_¬°.\x0013½\x0004\x0015­HÌ6{S~èñäé+Y4nJÂeVU²ªVVÐ»\x0014á\x0015Qì³¨¡~è\x0006V]²êVV,°×ÙÉa\x0003ÙkÅîÄÝÞ@ëJZ×|².Í?I´äê£iws¶¡¤
Í´vå@Ê\x001c\x0003°Å	u´´ _hÆ5û1ç\x0002<û$"ç\x0002ÌNÎVöÞld#\x00196¦Õ
èç
:=TÚ@kz´¦V§	©)ÄÁ^»á§[
Û{f²ýi\x001eÃ\x0002u~g&ò;Ó3ÔkªAêrrêÁýÃ»<	}kÞZäúTÝ\x0015*§¼5ß[/l<ñìüÕØ$ô\x0002V°ª\x00156æD¤V9É'\x001e¡h\x0003«.Yu#«ØàzÔu\x001a6qzyµYéVÁ\x0012Ö´\x001e,5Dt³\x0018\x000cÙ4>Û4jÈþj`µ%«meU¹ü3¨lùUEõ/Ü\x0000ëJX×\x0008K×èÆ:[Ãj¦ÑP<¡\x0001Ö°¾\x0015Öæú0\x0013)AaBÎº\x001d]ÙXÂÆFXìP\x0008T ÑMBI\x0001¤MñCÕ-õ°yRV4ÒzËåÕXÀJ¹(°eø­FAÏ£íëV¥\x0010\x0002÷é+ð\x001c\x0004^õ­\x000fb'OLölÔ
èÜp\x0017®\uáº\\x0012¼Zø>¶§\x0016d£^@Ë\x0003ÜbõZ^ÄG=\x0005¬¤í"y¥¬í"{mâ6ä\x0002
Ü\x0017M\x0011ÑÕ¨Ár­\x001a^]. IÑßDòýõ\x0013þÛÉòfJ>S\x001bÂk¸\x0018\x0014îÆáZ\x001c\x001czi«\x0005\x0010ß\x001f^á¿,6
n.UÉ¬ÚCäiZX®)V,wq8òÎu¬ÛeÒj\x001aî\x0004ðatÃkÖ\x0008lJ`Ó\x000eì\x0014@°Nç	îÔwCÚ¢ØÄ¶X\x0007ýb\x001d²£õ?8Íë¹wx]IìÚÏ\x0018ÛèCZ¼\x0007&N:d/vìKdß~ÈÖ°5çMÖ$ï­CVvs8¯9ÌaÆ1ë|ãªìGMHÞ\x0019q,cû)«<«NÛÀ\x0001Hp²IEG1Ô­ÛÆ\\x0018l¨HÄ,MBsP4*\x0015Ö$|ÃPD§¹¯üÚµÆ\x00052*Kfî<ü\x0003EóÎ {ÚOÎPpi§6¦ÊµÉj\x001aü|æúíúO\x001bÃ¥\x0011ø\x0008=Ï86>ËºÁ\x0011tMÐ=\x0015(gè@\x0011òA[ÍAJ\x00198\\x001dÅPáD#tO\x000bÊ\x0019jÐz®_P¶õ\x0002t.«\x0008&îLBË"í°Û\x0018Nqçö&4í\x001eU÷ðLÚ&æ&3T¡óÁï\x000eÚ\x0007î<µ;è¡>Fæ&íªPûúö¹\x001aV\x001a\x001e]\x001cÕ\x000e¡{ÊPÎÐQqÅr\x0006»nÓí`5(±3!­zÚPµkCí\x0004E×au;\x0014×F­vö\x000cUO\x001dª\x0019Î Ì
Ä\x0008%\x000ed®¸\x000frwvê;íêP\x001b¥4¶,w«©£;Óª§ZT»jAÃBFÚG\x000e\x0013á¡ù!îÎZR=)­fHiÔÜäayµê2æë\x0011åH.¿\x0016º'òÔ\x000c'VÐNò\x0008PáTVâCm\x001bmÐº'=ô\x000céë½\x0008ÚäÚHá³r\x0019*$mdî½C=ã\x001dªÀ1[üpdov¨\x001f¥¹÷\x000cõgèp\x0008;\x0017äq«uäò	¬$Þ\x0019tï\x0019ê\x0019Ï\x0010Ð¨W\x000bÃIÂäø×P\x000e²\x0011º÷\x000cõghó¸\x001c\x0015\x000c7EJÉ\x0003IÞ§ezÏÐÌQâ:mqEËÃó¸~©b¶<2¨Ð½whf¼CÐ'´"AáJÎéô íÎl<Ó6Îxàªx²ñ¬f)Ífi»s´Lï\x0019\x0019Ñ;)²ýo"»á#aa¨½U\x0017æ5r+}&ì6ãL\x000e\x0000E¶á	\x0005Q
o¡\x0018B\x001f§°µx?\x000eò*qþù¿\x001f§
gÅ5Ê<ºÊär\x000bÇM.\x000e\x0005ï&íä,0MiZ0ÁØ§~\x0014)W\x0005\x0001XÇJeð²Ö\x0015¶¤´-¸´ 
ùØ 6ø(ÃÐ¬ZHWBº\x0016H\\x000fÁ9Z»ª\x0000\x0018\x0002TéKLßta_Ó( )9\x0005\x0002ë×Ýû¯À\x000c%fh:MÇEreßÈy\x001cøè;¸±Ä-¸³0ÃVÆÔ\x0017Vm$óïf\x0011èFbÑôÎUnw¯."÷pa]\x0018òk9eS6pbÒÆ=
ÃQ\x001eää\x0002æ%?\x0015=á.¤;Ö¤p«ç±Vä~¹0ä¹×rê\x001e§n9N\x0010¼]\x0010\x000cnM¢ÓåÒÚ\x0003j8{ò]¶\x0008xä´\x0003[çFÕ`ö$¼l\x0012ñ!Æ¤<á\x0015ç¿1ç¦ae5=Ù)'NM¥.Ó\x0018yd.®ÅÌ£Ëæ_OÕJªI*U7,¨%ËÙH²C\x0006-gßkzî1Têº*\x0008Óäñ/~\x0007]õl9ÕbÌuµÞüÙ-ûOEõ´\x001fê[¯âì\x001b¡5·*7ª3BV5³ÇH\x000b\x000ftÎgwëEÓN\x0017;Ogoq»|¸Ù>Y«Û\x001eK3\x0000A»±Ãa,_P\x001bGÔæ	üíÞâxq~t°V´ªÖ\x0018TEÝ(ylçN[;&E«`u	«\x001ba­H6=°FÎPÀuÝøÀÚ\x0012Ö6ÂbjÏä{@zô<ù\x001el,J\x001bâÚ­{×ËL\x001bK0dTb_åÌ@\x000eoe\x00179
EÙ©JLÕiQ1ÑeÕXæ6Ô`J«9uÉ©S}RL\x0006Òy(¢\x001arª9MÉiÚ>»¤ØªôØ\x0006J_]Ð{ÒmöÕ¶ä´mç\x0019i\x001a&\x0003rã½æù&Ç'º\x0012Ô5j²IeP;§ãY¦F
uNUsúÓ·\x001e¨¢óä\x0005âpsxÇ`%f,1cÛqJjíÂ1Q<uÞ8\x001eÈj>¨ìËÏF\x0001*hg&<Üh\x000cWé\x001a=T¸]MÚ\x0013M²M6)ÏTª¼ÀË²\x000c5rh\x0003T5iïÑË¶W¯\x000cÅIà\x0012¤=Å\x0019-§\x0005\x0018Ï±M$í½&Ùö§Ñ}Ò¯vÚ\x001bëéÝë-u\x0013I{\x000fJ6¾(EÛ\x0011¤·£\x001aÇT»¡ØS-©ê½(Õö¢´Ígª<oî6ûù´\x001e¯ìHÚ{QªíEa§?JÇõ««°½VÃË\x0013+I{/Jµ½(8Sôh\x001auEGÊ\x001fKiÑTõÔËßt*ª¾¾	'\x0016dÈgOûY¼R¬9}RNßÅ5öÁLÁ\x001cáÿIÉÓVÛ'Ø8àjïâ\x0010{`¶Cª\x0012Rµ@lB7Â"ÊpBÄÈ]ÒÓ!u	©\x001b \x0005/\x0002ìþ'qÏ%Íà\x0012ÏJBS\x0012zBp1ÙQ
Êr\x000cÐØ\x0012U#þòTH[BÚ\x0016HÉ³-}¼IÔ ¡C'9T÷X	éKHß\x0000éy\x0007üOz®s\x0004¡îøBn;Me%cla´§¯­öi{Ô?öü\x001b¹ÊÓtÒG´<\x001a9Ød|xZz\x0002â'õ\x0002ïæxÓTÊ¾l\x0010\x0016\x0007Í}G§é3zÈ«ì\x001fÙ ¬\x000by¤/øÔ6¬\x0003§ht\x001cò7*){¯[¶<oÇ+x;/SÐYú½L?ÿ»\x001e¥k¡\x0014Ô3-hRö¼ÍÛ¸!\x001f³\x0012²'d\x0010¯¬I\x0008áiRÝ,'ýP{W%cO\x0006É\x0016!\x0014mvØpI\x001c¹Ù_\x000bC[Ý'B
\x0017ú&\x0010üE/îýt{sçu=ÝÜN\x0019G8îâàBÎwù¡\x0015L9êyu|tJC»®'ë\Ï#·Qåé]Îq8LÊ¼çjã&t[¢Û+tùããõCÿÎà_ü[ýÒIé~\x0001þÅ¿Ã/ÐvíÍ1oöþé±Gt¼üø°üüyÒNÇ½&à\x0005Rò\x000f÷¥%\x0001\x0018»ÿÓÏÏ®.Ó8¢ÅóÅÅÅ\x0004VU²ª&V,©5Tæá\x0004\x0017ÇIéó\x0018Á\x0004`=«.Yu\x0013«qËº\x0004`Ó¢&e¹\x001dÆ
\x000fv©gµ%«m;W#x|\x0016î¤Ü«¯­\x001bZ¾ÞÀêJV×v®Zå\x0019uÎrå¡vµSeè=cÝPÇI ¾\x0004õm ü§í\x0002ÁñeUy$¯õSG*Ac	\x001a@A]c¶¯\x00035v¶j8ÞÆ\x0002¯nÒÇ\x001få}IÕ&ª¬\¥Ôr\x0005"NIáÚPYý-½[*\x001b¯)Xl©Ï¢ÛÓFOJEd`4f'Oª¯Ä:5Ð)±\x0006M¨©¸Â\x0008EU5&FÁ\x000eÌ`õÏÔ\x0010×UV´lfV¬ÈÀÎ$¨T×!OòÙ`­ç-\x0019\x000f4®ë©h9ÊV\x0001\x0008êÆåÁÿã@ Ì\x0013èÂ¦°Ët@]\x0002êj@ ¢c
û\x0008ihAîÿ\x001f\x001c´P\x0007hJ@ó\x0002OÐ¶þ\x0004
:Ü©sCpFR	.A	¸Èj&¡+	Ý\x000b<B_\x0002úú#\x000cûE\x0011ßA.8\x000bêâ¦ó/¼À\x0003%`¬\x0006L	fnÅ§å)ësÞ4èr2`Q<Z¼¼#}UR¯K´á\x001dB*¼ØHr\x001bu0\x0006­MGì)\x0013ù\x0002µìi\x0013Y¯Ntà\x0015¹
+³hÔ\x0010\x0007Á(MØS'ò\x0005ê\x0013ÙÓ'²^¡\x0018ÏÕUT\x001cÄX\x001f_Ä¡\x0015[=ÄMÆ÷zq k#â§
àï*F,\x0015Þ:³ÏÃ<øsp¶CXï²ëÅ:®M¹ª\x000f\x00060ÃE\x0018nµázSð¾SºÓÓ®
8Î»ü¬Îq"?6p"çÿOÝ»-Çq$éº¯R/0°8\x001fWE\x0010¢Ð\x0006\x0002\8ÐfæFV$!\x0012Ý  ÆAÓÒÕ¼ÆÜ-Ûw½oöCèMæIvx{dDUfUFd\x0006\6Â4Ñ#­O\x0011î\x001e\x001eî¿«S5qJF]ù\yÈ\x0013EÎ~bø6Yí:ÇÔmËéÒg·
\x001bS¡0\x001c)Õ>0MiÚVÓá\x0010D\x0001SGIÚ¤ô\x001a\x00129¨å´9§m=E4*Öú4Ð[§ÑÂ£O\x0015.Çt­Ë½i BK=¨&M´Ý"B;Óç¾S¤XMó¤GmHùÄm\x0011HÌÚùõ!\x0005SAU ã	TS­M\x0012Ò\x001a}¯à,}Q3R8A7ÐSÃ\x0002vvë 7âmî(Ò@O×5|®ª}|ùÂÌó6;¯mÒ$\x001buUô+º\x000fÐÂÐó6K\x000fÈ$AÐ
nFD1û\x0016ÿ© \gIµ\x001d&æI,\x0001Fµ\x0013©¤l¥U£ÍJSI¦*Y4UU.ª¥.\x0015ÐÇædG]²£{pkyJ?¶Uz§¤ßÌµOæ4)õÚpÔfàêõ×pí²yâäì. ÁG
ô"\x0012zü1ãã8@{'¡È	E5!×0\x0003T\x0007¨F¥q4ãª\x0003	eN(ë×ÐRIFM³a
\x0011Ï\x0007T9 jZB|äf`	\x001f?á\x0013	MNhZ\x0008i~{?\x0014RQo\x0019ËSNçs9«ç\x000bNU³JõsZÇ§\x000cM#Ìâ"8È¬~\x0017ÊÔ\x001b\x000b,¼è3jH¦³\x000e°8Ç¼þ ÿ\x0003\x0016§7\x001c\x0013NÁxY,â©½Ôév[(×{ve1èè/«Ï7w±Éx5­ÇX\x0007ÿbPÎK¨êÏ4áÕË!±}gðåùãÓi\x001dÇr½W\x0016èã8HïIaB¦¤¦Wã³¥ÚèeN/çÒ;*ðè[± 'EûÁî9ô*§Wsée¸ô\x000cJí#½Hº£]ßô:§×óé1'%a¾«"zÚ÷l´j¯Þäôf.=K7\x0018kIQ2Józ±mjJ\x000b½ÍéíLú4t^JI\x001dY%½ß}[\x001c³»¹ì®d \x0013¬$±+ÏÇÃ6zÓû¹ô\x001c*ÑI\x000f\x001e|\x001a­bÄRgÐçr\T\x001b~pùhîA
K¬\x0019Iø!M¾9ô¥§éjïG\x001dù.\x0003\x0011\x0017*N¶D\x0006mô§ås]-6ÇµWZÓÂÖ¡Rq©¾FüÂYñÞJyOER	ê\x0010\x0012i}8¸[&Ïµà\x0017öÏ4øP^9@\x0018üMôÒÉ\x001c¬¯A_ØL>ÓhÂÎ×Â øØá;´÷¼õEavÄL³£¼H{;jÌ\x0015ÎöÃ-ö\x001b+2FyrÆi5Ñ\x001b¾v?	»\x0012æ»Õ·@7%?×\x000f:6\x0006Æ\x0019 ¤D\x001at<ö óîø|	22»	EN(ê	Å\x0001ÝA]?Ê4)mÎç9¬æÓb\x0014¦-ää£a·kFBé:\x0007ÔÕÖÂ5S®\x000e:
¥3blüã\x0004BiÖ/É\x00066áá×ëoØà°Z¬î>O\x0013/(ùê¦	  ½\x0016»\x0005¤\x0019z`?üñè\x001dv6,Ãÿ¾Ù/6ëb\x0003\x001bòeÓªVµÑ\x001a\x0018õ\x0011\x0013\x000f±~¢ÖEpm\x0003yí*X»-±y³ûéýÃç)é\x0011iJO&\x0004Y?D\x001d.§gçovã\x001cOÔâÉî
\x0012ß®\x0005½dÉÔoå`+CÆ7RJc×³\x001d6ooºv>½\x0004C5²Q¯¡5cu>×Nçxºaíè\x0019H\x0015\x000fKGxvÌJNÆ³9mÀ£¢\x0019oSB¦wªAÝ\x001a¾ìnfFìÜ'Ïp\x0019£ÖáÔ `Åè]r* /\x0000}-`p-ôÀï\x001cÙC&ª-\x0000øDaZDµm¡x8\x001cúPH1Íé¹ÛO\x0014WT^Ý\x000fGãI¼7\x000e\x0004hÔhª\x0000ã+ªÏ¯Ic£$Ô\x0007c»uZ@7V9¯8¿¢ú\x0000Cð\x0017N\x0003RY/­ß¢Ú:¯8\x001e¢úxXF|Ú§Ä¿KéÛÁ¹9Óø´]Ë\U	\x0013\x001fS\x0014ÈÝJl+ê»7H\x001bæ»l\x0011âsÊÙ-=0Â-½\x001ai/>Ü\x000fíbK©Õ©QKN¡ÜµÙ\x001c@Ý\x0005Í®Þð Á^.¨(@E\x0003¨°
\x0013Ùá\x0008R^ ü9½õ
E_ÕªàT/oA9³e(Ë¡Ø³×}xZMº\x00100­ZÜ(^«%uyHµMâr¹í.@2'µ ãî~'£u.	UN¨ê	]"Ô*ÂeJÒJÃ·È¹L#49¡©&t\x001e\x0004¹yô¤íA£¤dã*á\x0013	]Nèª	=§Ø(\x0019\x0017®|¤j ¸ÝhÁTÂ\\x0002É\x0016\x0012HS\x0011%ÞJ¹qfÀ*Nÿrppm\x001dbqyýiæÄ®@gSA ÕXÊ¡yÀuÅQáÕg\x0005ªýQÀÔöc
I;\x000fÍ«C´\x0005¢­_DUá8[!¤¼¹ÜvcíÉë¹\x0011çFÞ?ß<u9æÕóÃM§{²3÷$QT]0\x00182#I\x000c	°\x0019¶E³çýÕñea>Y^\x001f\x001foq~=iâó¤I\x000b·»Wç\x0019ÃGÐL
Ò­Ðãu«-Ü2çß\x000f·Ê¹Õ÷Ã­snýýpÛÛÎá\x0016\x0016_Þ@_*íèÍY©ÑV¶\x0016nsûYëm¡@2w*òpÚ\x0010ªâ[¦UsóÒ\x000eÎ2 ïPPOR³7|\x0008\x0012ÔÛ\x0012ßÔ/xYgÞ\x0019ñLÔéåîsÇÖücàÞß®>¥
ù³oÓÆ¤´tk¾?Y\x001ebüÙù»íÏnÝé¸ätÞ\x0007\x001a \x000e¸ËÛ¿?OZc-Ò\x000c\x001eB#JìR²ÕccÞ\x001f\x001f\x0001óbyò®v,ïºÙvÉl¿hbQ\x0010\x0019È*X;\x001au¦!
AõôÖR¡Zdisdi¿\x0007dW »\x0017,Öû?Ûx ýaõÇÿ÷éëõÓ\x001a3²?£\x0006[A\x0012ûÞ\x000e¥ewÇ\x001fÇáÏy_Í:­Êi×\x001fH_\x001c­Îiõ\x001cÚ\x0000\x0015nJxìQUN[Ü\x000f\x001e^\x000f¦âÆË:«ÉYÍ]Y¾^ÀM.E°Z\x001c>ÜßücÊ%ÕCº.ª	ÐÀ&UU\x0013ÛZüÃó³ãÝrºSæ²S1S\x0004óU°°TYAâ·NwfLàëñìâão¿Ú×âÛk\x0008p¦Ä
\x001eÊF
Nò5inED:\x0010+\x001c¿{\x000fR_\x001fN ®ÙøÜ\x001f\x0019ïìª%Wð\x001aF PêwçÅêæîiñnõðts7éiT<8¿aÙ¡L£eC[ýî¼X\x001e^.Þ-Ï/O_}Z}^=>=\§ÿ°íXíX;6\x0008áb\x001f\x0017ÊÒ ÝjüÐ\x0018¨Vl^`ó\x0019Øa'xê\x001c3Ðå\x0016Ó,iîÐKg+µ.¨õ\x001cjRr\x0016Ì¦áõJ¥¡ÔzH}µ\x0015Û\x0014ØfÎ\x001e\x00110&ªç¨\x000bNÐÖ6Ê\x000c\x0004­ØÅt3N¤Êy|ëQýCA2hF\x000cÕ\x000f·b»\x0002ÛÍ0$ªk´Bd\x001a(dÞãbûÚ·Sw\x0005·x 5\x0003éw¬\x0017¦²&>$\x001dÒí\x000bóçg¿p7ÆrÀ\x0016	Ûx*Ù\x0011C\x0012­Øùó3Ì\x0002GÎF¥q
ÜªU\x00086ö¸Ú¢À\x0016íØ\x0012ª¢Lß\x0019ØÆ÷Z1ÔÐ-\x000bl9\x0003ÛqèÅ­à\x0006¼Y9(o¥.áld?Ú\x0013$PÛ÷Å|²¹ÕØ¢«.ý\x0014üUøÓ«p)=ºût{ÿX;Ü&e~¨¥¤"\x0015Ñ±8êdqtzxrV\x0014½ïd¶\x0005³Á\x001cç©Åh$\x001b-ÒÔô¡wð&fW0»vf­%°Xi\x0018\x0006\x001c³<PCYÏ&f_0û\x0019ÌÂ "\x001aÇuè¤V\x0013þ\x0006îª-ÈªØÎjÎvö\x0012µ«És UÖ1KJ.î×MÌ¢`\x0016sY¦0U[ÒÐJ¨\x001c\x001fUÇ,Ë¾×á\x0017p;<Y=..\x001f®\x001f\x0017ïïî\x001fw³U¥[\x000e\x0010¯]Ê+\x0015Ígc¤N\x0017Ëóðç÷W§g\x0017¸\x00189¤lt\x0016ÔÀ©k\x001cí\x0003hac\x0003ê\x000eÇ:ãöµÌ¤v:Ì(µSM
J@è¡¡\x0018R Ä6T^ÅåôC\x0013q*PUwëÎPÕ+\x000b ×s\doÅB D\x0005\x0001étñÁz40Êb'³(Å\x001cfÚÂ\x0010rb³2´\x001bBÈ9d\x0011UÁ¬ÚalF3\x0016n®©\x0006ÈÂúì	Ú\x0014Ðf\x0006t8k^'±Mìa¤\x0006Ìa©ÍJd%×ÌÑµåæ¹§>:\x001eü\x0006)Áz\x0012\x000f³zè)ïd¹ß	,r`Ñ\x000e¬uÒµt\x000cØ»ë¢în«\[e\x000e,Û}7éj\x0012¯\x001e:{
¼*çU3\x0016ØÒ¹\x0013BSø HwÁº¡\x0016^óÚf^­Ð\x0018[N7\x000e©Ó­T\x000eÕ§·ÐºÖµÓJAòÜ87*¥M*·CÉÏ\x0016`\x0003û\x0019ËkúéM<5é>\x001cÊ²4\x0000sVX4ÖN\x001c®sÚÝ\x001cÍ"%Á¡i-Ä¥
n7ÂÐdXKÒîN¥\x001c\x0018x m\x0001.l0o7Â¹\x0003ÊN\x0018òr}\x0011¶CÍÍ-À
æíF\x0018Òà¨ÛåS$©ª\x0011ðPÅs\x000b°)M;0´ò$I	p­Û\x0018\x001a\x000cÚB\Ø	Þn( R\x0016;ýLã7¦)ÚvøÆQ
,
K,ÚM±ð,ÔÒ>,D?IÜi?K,c'Û\x000cVÑ Â/J;3CY*¸×ï\x0007W\x0017¸º\x001dqÚÃ\x0012d¾±óESç\x001b\x0012Aj\x0000VçPíC*M2w\x00020É¨,Ïñ¡dq\x0003±-vmß\x0011Ú+ª¨\x0016!Î$¥CNb§nª«~ ¦«~[É\x0014)\ÿ¡	×¼÷Ï~¨
`23ûéúëïæw1<DîïW\x000f«ßïo!\x0019!ñ!E¶ëÇ9\}\=|\x000e'!dÔ¤\x0011ZÀm®ë×\x0012JáBi¼É\x0002àóÅáòõòüÍÑÅ«÷Ëóå¿\\x0014(d\\x001c:óº\x001fUdð±»±Û,XXÙ	\x001b¥ò\x0003Ì\x001e\x0006ÁÒA6³ûQ·d\x0006S"\x0001\x000cní6.u¸Ìe´\x000c\x000eI÷£Ì/Ø	æÂI\x0019{Ú6F¯°fY)G+\x0004²ÚmfÆ±\x0019/\x0002\x000cï±LeÝv­d\x001aÈt%\x0019\x0008	¸¸fa{E¡f!­\x0017i
\x0006¥\x0012ÝÊ%ã±|\x0008n£>\x000e\x0019\x000bK&qÿ;©\x001fW}üý·Ï\x000f¿\x0002\x0018t¢v?^¯¦Ay)qÌ¼\x0016 XÓÕ \x000b
Â\x001de&\x0015S½^¥-s"Ðnï~L&\x0012]>'àÀ,'\x0019qX\x001b\x0003ÐÃ\x001b~"-\x0005?&ãÀ°ë®=)\x0004\\Ç^>¡¼ÅT\x0012æÓ\x000e\x001biD"õ¯º\x001fÓ\x0017\x0008&ÔÅ£\x0007"H&EøÅ%arí¨j¢è\x001bãÏ]dbQ\x0016ÐÔÐUu»ÈE$\x000e5ÕH_äÇ_îT·¯ÁáÀ××\x000fw«ÏÝ\x0004¦)Ö\x0013´èú+Ðx:\'îF>ÜÑùéòÍÙØ[LÁ\x0005þ\x0006~TqÁCb'è\x001b¸<@w\x0013þ\x0016äòc5\x001d\x000c\x0014»\x001fu`ÊÆ	§ag\x0005£®â)\x0013Å»ÃÎjö+í~TNÇ!Áä\x0005
j\x001c'+%ü\0¨wè~Ôí±\x0000{ÌZ\x0006"\x001au´êç³«È¾/¿óUç\x0007-øAÛ== òÔ.´\x0010¦Âëi·hÁ²ØX\x0019,\x0017D\x0019\x0002XïÆÐ.Ï;Ý©1¶¯â?Ø#T«r(îë~\x001c®îî¿<¬`@Ú4áL¬t=ëæªÃçeè\x000e\x001c;\^½=_Â´Q>ûËJ\ÿyû®þö~»îdÛ&1H\x0012¾i¸dstBÊànãÃ\x0001ôáÉÑ»£ÓËQ¨|ý«èJa¸ù+ï4÷·÷ß>ÆÇîo
)1à!`@o\x0014þ$1¸áù¤\x001cîähqxvröîõ¶Çê×ÏæAv\x0001>+üxw÷Ëíêæñf
_øïm\x001cæ«Añ\x000cº&à48¬!õÃxïÎNß,/Çáôí§ÕSöMÃâ}\x0008»mõeÊq\x0008\¹\x0003F'Õ\x001e \x001f×äÇ¹Ã×°r0oùvü8dh!SõháSrA5uÁ£³Xå
æ\x000f{:¶ð9u\x0003y±À\x0016§äF6E\x0011\x0019×ûX·ðïgêÙbÙx¼ëêX\x001d¾©ôt=²lØ-Ô±ãnëÙ¤k\x0008Ô\x0005 /õ6]Ã÷²Ýt
Å)'á*\ô¦Þ§a7_Ç\x0016Þ7,b°ÝäAt§ÞImùH\x0004R\x0006O\x0007¼Þà%\x0016SAëcæG(ë\x0005\x001d\x0005?bÝêà \x000eõpBF¹Q¨ÅU\x0007.¦W\x001cK±µÃ×Ë:8õªS¡¨\x000bÑ¤ÆÀ\x0012dô\x0010.}Ue/ul]TÏF5\x000fñÊ\x0019oÀªkÁ+çÈ
¸\x000e\x000en0
G5l9p\x000c$\x0015\x000e	pÞË}|T¸Å4\x001cUÉÛ`á\x0003³hFXJN¹}X_P\x001b¿ª¿*\x000e1\x0006\x001bÇ²HÄ\x0013{°¿\x0010Û³ª-¼ëÆ-×}à\x000eNÅ1°åÄ\x001e¬\x001c¤DËYås\x000caG\x0014µ	pÂ&ç0\x001c×±#%ê\x0011°#\x000e\x0003%æ)\x001f\x001aì\x0008-\x001cãûX¸\x0010úhEÕ±\x0008g(ì¤¢óàG\x0012\x000eupÁÂ\x0006+\x0007©PôùLF5jøª)Çí÷`ä C#ê\x001cS\x000cT¼bþÝ@s]dã¤Àø=U(±¬Á¯öé8È%ÀñØ\x0001\x000b7ÿ«\x000bÿ²ÁÊA\x0013n¹à)0Èt8"\x0007ÎÃ>Â%ÈÖÈpÉÅþNë¦ÂÅpÉ¥ÃºÏ
od
&¨#\x000eq¦'¯o=î9\x001b3\x001b³áù-&ØÄéñà\x001fL\x0014´\x0001K"é³}°l0Á!FbhÅ3p\x001eÈ¯Ê½°\x0005ë+\x001b,°ì¤ì"\x0011
Jpz\x001fÇ!X_Ù`Aíb`iû°ã,Áå­¬ípÁüÊ\x0006\x0013\x000csÎðMÁÉ8½¾»ÚÐq0v\x001f5Ä²:ÐtÞxZ¹ð	£îZÉÊ9µ@\x0013
/TµpÞ©Xo
÷.\x0003\x0019¦\x000eN\x001bº\x0014Ú}x}\x0015,¥ªö\x000fÎ{\x0014(ÏJLe¦`Î¸=Ü\x001fÀÇ¨jÿ\x0010àR=\x0000d½$î9ãé³j¿¬\x0017\x001c*Uí\x001f\x0002½pZ]Ôz\x00008G9\x0012¨\x000f\x0007éÂ\x0006ÿ\x0010N\x0001±é\x0003DKfd\x001f!0<ª\x0006ç\x0000ãú§I§\x0011-\x001d\x0006µ¬\x0017Ô¿ª\x0016\x0003¬âXUÈÈHN¡S\x0014f\x0002:¸`|U\x0001\x0006¥\x0016m'\x001e\x0010#¹8	\x0001àöau÷´ÛàW-¥Î!Ïª1\x0006\x0016Ö÷íaÏA\x001eY7ÄÀJ \x0019?H·\x001a»£Ø©\x000e,üËéø\x0017Â#ûÍAýnâ\x0004Ý\x0007ÇJ+êà «ßpR"ª\x001dª\x000f\x00048öÝGZ\x001f5tC\x001c\x0007
w¸ß=àLZ¹}À­¡\x001bÌáøn)`|\x0004ÝVáù(Âé½¬\0!ºÁhöfXü¤Ò¯W{±"Áóéú|!d½ð>Ø¥A+¢hÇÉ}<r`ÝLÇAÖÍSîÆ¤r¶}DqÐÚe\x001a,\0¿X\x0014\x0005pèU Ê1¯öª8ÓpVñèØeä\x001a,}U¾Ø\x001c\x0007L\x0013ö :|å-\x0015Üõ©\x0010äí
.\x001blàqô´tJe2Elû\x0008ãÀûHIÄQ
\x001an2ä\x001c¬øQÛ¿<²i¹ª:ª¸þu\x000bÞB#Ý[\x0016kÛbGRY,ßpÊÜ\x0018KEj\x000f\x0001	ñÛ\x0006;¢9\x00199\x00055»-T\x001c\x0003ÎûÏ\x000b[Ã6DKÁçÓÊ©ô^î4\x0019\x0012·ô\x0008Ô9Û\x0006+ç$\x0019\x0012Å±`Ï9æ	m\x001fÇ\x0001gmÃ]Ð\x0003§ÁÒ#\x0017§£0R\x0016W\x0007\x0016m0¾\x001aû\x0018Á¨Øµß¹{:
v\x001fO\x000ePEe["LIá¯òü`=Àt~\x001f1\x001cìÙ\x0000ÓRy(Ì\x0002§`È5x¶üp®^Ù\x0006ë\x001b.§\x0016Csæ3à8Û
	ÛÖ6DQ£\x0003÷J\x001aOo5ïaËx¤kp
á~àL:\x000f&=\x000b³Ï
ýâ®Þ5ð°\\x001a+©\x0018C\x000bçEêÍé2ò³Ùt
\x0001ÊY°oB¦Ü´ó\x001aó6n¬Õ¤\x000e.ü3\gÐ\x0007ÑEªà\x001a\x0014\x00199¨Ï\x0016v­kÉÆ)ÈrEß ©êÆ:I~Ë¸=¸\x0007è@r
\x0016	zq\x0008×8z\x0011àR02ÒÙTÇ\x0006õqÕF.Ü\x000bLo\x0010OÆ4¦É\x0002´êÔÁÅw
F®ke \x0003¥ðÁö\x0006x\x000f6\x000e\x0014"}²8ã:Õy1ú¨\x001e¦_Ï\x000böÍ7¿\§L)(«d½ñ)\x0001±0\x000eÔ\x001e}cÊ\x000c Ó\x000f³Já8¤ÌÍ>ÓPè\x001b\x001eC8Ã\x0018SK\x001dÅ¸E1)\x001d'÷Q\x0006:\x001c¾:þu^vQH\8M>ß¢þ\x0016,Ü>>j8R¾Ú\x0000;¯¨Z?¶oF42^j\x001f\x0005rðHæ«í¯ó¦h-è\x001c¤ð	n\x000f\x0006\x0018D\x0013|u\x0008ì¼Å\x000b\x0000gb';Ü"úº\x001d\x0017loð\x000eá6lZÐë\x001b*R\x0003Ú\x001e9tßu?ªÙ<µ®hí)È´ÓÓ{G8´+v?\x001a>+ÖµfE#§xzÛ\x000b\x001dTw³÷h#ó2:=­L÷®±\x0006Ý::(ïf
6X+ªmÑ&>ZÁRCÚ\x0007\x001dÔw³\x0006+¬,ðB(ÈÔõo]~¾\x0019î"îG5\x001d=\x0011âiíkí\x001eÊ8XÊîGµïêm0´$Å8Ó¤M8/ûø¦PzÎ\x001aììõ\x001a¼G½\x0006x%§ÂG6?ÉÁ\x0003v?ªC¢ØcLÒ\x0010~\x000f\x000f¿\x001cT¼º\x001fµpBQ£\x0008\x0014´b/F¸¨ÒÒ¹=Ýp\x0008\x0008»\x001fµtL0<U£M_4:?Hç]M}M 3qx	¬¥xÎ\x0018Þ¯Ý\x001eNl×ÇRßÈâ\x001cøWò\x0011|\x0011N'ÿº/\x000bv×Û9ëY_7ê£\x0016­\x0000¹xªâ\x0013{¡\x0003kÇë­\x000bûNÚÔI(âÕRP£Í\x001e®_¼k\x0002ªï\x0002rÖ8ªA·Ó\x001d\x0007²L¤`°m\x0007Ö®¾Õ&X;zf\x0016öÄô
{{Hºrháõ­6Á¥\x0013\x0006¸ècµO~b¤\x0003¾
\x000e»xýQJl\x001aC={
Î>\x001eØùW0\x000eùx^ÿvã@\x0005\x001f\x001dáñ\¡ÓT¾Ä÷Ð\x0007Ä!Æ2t.\x000e:LH%.Ù:¶·L\x000e\x00170^\x000bóÜ¥~G\x000bõ\x0011\x0006ûñÃZ\x000bY·Óu­q
I:ÛçÓa\x0018<=$\x0015®1I©	tÐ=õS¯¡\x001cÑ\x000f^{\\x001c~]Ý^?M\x0014æ\x0000£c\x0017bxçâ2\x001aj=\x0017Ü\x000c\x001f8Öì\x0002ëO.ÇUÃ\x0012­ÈiE#-4¤¡¢KÊDi¦ð\x0016nC#Ç¹Væ´²\x0016´ApmÃ\x0016Rl\x001aB µÃ)jZÓªÖ )´µUx \x000cuv\x0008¦{5­Îiu#-³\x0016:l¤$í³/V³6V\x0010U>í\x0003,t÷ÖÔXKe5­Íim+-'5<'\x0019UtyK
 T;TÓºÖ½ôµõ9­o¥eTÉ\x0007k«HLL¤¥ÝA@1jr
¬6ø\x0006\x001fSNÎàð©@«0©cÜµå¥'kte0à\x0006×V\x0016\x0013d\x0016Ô\x0000÷C[ì[Þºq¥JÎÁJj@ôhGÚK¦Ã\x001a»\x0016$W\x000cP«ÓÈ´®ï\x001föéòC¦ºææáp«\x001fµS`41Y´3\x001bGµ*\x0006{ìçéÎ4òÐ\x0002,s`Ù\x000e,uÊ¢zN{"¬2Ý\x0007\x001c\x001fÞ\x0015-Ì*gVÍÌ CEoå ã\x0015#]¨oM9Ì\x0011!¯\x0006f3ëvf/\x000fH6HB§ADî»Fôð]¿\x0005ÙæÈvÆ2+\x0014sëN°v3\¾iÍH"»ÙçÌ¾\x0019,R®\x000c³Û2õ"h9¢£VOÌK+×næ\x0002lz\x0003\x0002z\x0014ÜM\x000fTÐf·/æÂhðv«\x0001 (\x0002\x0000¥>¾ª	¶\x001aÑ«fbÍîhöÝ§ë»Åû»¿ÞßMKk¹\x0010±a^+lj\x001dy¬£\x001eQ{¥ÚåéáñQøW8;ýËÙénzÓË¹ô¥¼\x0017@xàGu+¼ÎáõlxM%þF[ÈóÄ\x0012'$Fô\x0017[émNoçÑûð\x000fHÏ(Ñmmê3v¸Z¦Þçô~6½ vJ)\x0010´ö®Y\x001d\x000eM\x001aéyyhgÚ®TÉË¤\x0000AJ\x0014g³±>®VúâÐò§6Ðë\x0003¯\x0010©]ß%¡\x00031"ÚJ_Z>óØvÅW\x0004WÅIDBÑÛ\x001d\x001fÑ~nÅ/-}n\x0005£¦§n\x001e=éÕdAù¶¼M=~qnùì+dS`Yycÿ$¾5ÙP/+f\x001f\aa\x0012\x000f=­¢\¦ã©ÄíwïâäÙ'÷OÃ7bý$à´¼½ýã×0\x0019\x0016+þñ\x0017\x001f&
;Ã-\x0006Ãë4/YjÕ\x0011#ñûòääè\x0008&ÄâÅåâ\x0003\x000cï×9¼	\x000f/,X*K¯£­\x00199·­ô6§·ßÙÒû\x001cÞ_ðùM*Æ
óè¡z§þ\x0008Ü8RQ©c#ÁB5>Së÷\x0013õ*Ò__/w\x001fÙ¹^ÞÃÚ¤Wm´Ä$A\x0008Q÷-ìóôp,­M$_¾9\x000f&çhqzvy~´[äÜb\x00167ëU'è\x0019'p³tí\x001e±mÜ2ç3¸¡ÄA(1§ô­1b6rjãV9·Ã
Oã¤\x000fh©ÀÀôB\x001a~ä¯ÛäÜfÎ>ñ2il8·W£Réáxk\x001b¶Ë±Ý,l\x0001QoÄ6ô:e\x0014	à{;RZ×Æísn?ëXjÊYIÚCF¦J\x000f3¢"Ù=ÿÀFg³¶·'cÞ\x001fÓè&o\x0018?¦yÝ¸O~úxóXî\x0015øÅß.zÝûèÎûß??Åwµ8¹þ¸\x0002ÈK÷\x0017Ý[w|p±éª4ÒJu~vu\x0019ãÝåâäìêõ\x0012þû	ì2g3Ù=Ý±Ã-/¾Í+Í¶f§q¾Gt£«YèÆºÔS¤MnHT³µ²ÛÝÎb\x000f±"déù\x0008b\x000c3»æØµ²»ÝÍc±>ÔUÞ7BØz¥Ff\x00124²g&RG\x00139\x0007>\GQ\x0013U+G]7F§705R)×
_ÚyÆ´Q¤{d¥I}\x001bl$ÚH.
r1\ë8\x001eö\x000c'¥ònÜ4½Ö$Ã\x001aáM\x0001oæÁ[ª+a\x001a ¦>2Êfè\x0011­Ú6x.l¹òóLT\x000e\x0010B\x0018C\x001dÒº­3#b\x0006Õô­Ý\x000c+K\x0002Þ\x0005Ä\x0011E8Â\x001e"\x001a\x0001»f²ÏAtÚöÏeïÂGãvË\Î!ç¥ýÎ]\x001cª
ò%I`\í\x001aÉUN®fãÓ5aXéâEê7\x0019>¥Ô:§ÖßÓzÜÌ"\x0007\x0001E.Ójøüôâ*rÛ9ä,\x0004ìØÂ¢$\x000fD­\x000fê#t£cáÚÀ]\x000eîf-¹ôÔÝ¢c/I,?sIÀu$\x0006h#çAä³,"ó>/ \x0003ãqÑ=õ÷#iD/,"e\x0012c)1\x001dnØ$ñgiÌõ#\x001aÒèIä³l"(Ç(Rcãi\K"{z$ôjD/ì"e\x0018N¢7ô§r4äO¼5\x0017fÏ²ÐªÞÒ0ª\x0016v²\x0019Öt;4¢\x0017vÏ3!ÂE¡M\x0019"\x0018» h»X1"Óî\x000bt?\x000b]\x0008ì^ã!VÄ®ÇÈ2\x0006\x000fµ«>©Î¼\x00149¤hbà73l;ó$ù+Ã\x001d\x001bUu=W´ãÁÞìãß@¸µ4R¸ÊÐ«ïóâðë\x001fÿÏÓõjÒ`ÚNá\x000eG2^\x0000Gó¢ßáº×Ò+(0¾<Z^í\x00159¬h
\x0006D\Â½\x0006¨\x001ev$ËX\x000b+sXÙº²N!¹S4#zdµ°*U­++ ò¶\x0001-,)DúÁ{µ¨:GÕ­¨¦¢i¥¨4'¸Á¤Á<2²­\x0016Öä°¦\x0015VRß\x001c¨ÀPÌ®\x0006ÊïçtÙÕ¶.¬\x0003á+*[Q:é7ÈLÔÂº\x001cÖ5Â*2öÂ$»EnÎm='\x0015¬>gõí6Võ³$\x001b^uÄÈ¨èJØ¼Çõí<
¦^üë¬Hý¼#rØµ´¥ûjö_D|¼|3xbEÿE%â+i\x000bÿÅ[\x001dr´kAjÜ¦\x0001§dgÙH
v-máÀx«\x0007ÓÚÐT¸ûád¶îÂ±]ß°¶ð`¼ÕI\x0007¢\x0002\x001d-Ly¦©^¤Õ;&F^\x000b[ø0ÞìÄÒè¶pù'xÈlÒ\x001fiK¯¥-\x0018oõbÐàÒªÁûRE\x001d©#A\x0007Ç^`\x000b/ÆÝ\x0018? Á|IUÓNqZu{ZÙÂ3ðV× RÅ\øöiÞ¦4´\x000fìÈ%­(­h5¶$õ\x0015
\x0004ï'Õ8;ö
T	[X/Ñj½T'¼\x00137­I\x0003\x0000K»vDõ¼úfS\$»Û
ü¢Õ,`\x0019¶ïM¯=cJí­\»3@¡@_q»Z¼¿¹»þ<Q[CJ¸ÖÀë\x000e\x000c\x0006D¥T/é\x0001_¡\x001eTi»\¼?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=}qþE»Ùò/XL½Jÿ\x0002JiÎÿ\x000bh\x000c'ÿ\x000bè²<\x0006\x0012\x001b«VÃÏ&ÿ\x0005çyâô/ q¤óÿ\x0002+ºÚ©Ú­OÆÿ\x0005¾u¯\x0006ÿ\x0005T\x000bÕ\x0016	ç\ÓÃ¹þú6Ù¸ßN?}úðRéwf4I£,7Pb\x0014I#¨ÑmQÿrñædß\x001e~zñô5%Ñ¿Ç\x0006K6èdsVæÏXÔR^bjÖ!V\x0014ª\x001bÎ.ál'\PR^biN\x000eÃy\x0019Ë\x0018°ÕêÃ%\x001cvÂ%\x0007+^m\x0019á´¾X4s+çp®\x000f.,æ>w-RÖÊ¨ÕHÓ3p~	ç;W.yÈ²çHGÇ\x0001ëgmýÐn¸°\x000b+çtñóÂ±Hõ<ªí7ìfK¶Ø¹pé¶)ï®6\x0018éÄ6UæThGÃõ¢Õ,G±qªsÝ,°Ô< Eò:óÂaUV¶¹®µÀ½&ØK\x001aPU¡C#Þz\x0008fÊ\x0004ëÆ\x0004ëN\x001b\x001c±VÑe­\x0002Þr²p&Ì}VÓ°Î£\x0004AÙs$Þ\x0013Êy0+ÒyûªÍõ ;ïHÚç¼p^\x001eÒmtbäPÍ­\s=èÎû!\x0006
+PPñKS\x0012zEí§\x000cn®\x0007Ý{?Ðø6>\x000fä\x001a\x0004\x0015êÒù©ûA7÷î¼ "ÂñÒÙðm°n\x0004;u?èæ~Ð}\x0017UänòNLT\x000c\x001dÒ3\¡ss\x001enn\x0008ÝyEDp2Ô8Åùâ2YUÑ¶±I/\x001d4\x0004ô]\x0012ií\x0002!å¾DÊ¥«f8ç9¸æÎ;"¦ Hn° ¤9]ý²íÐÌÑµ~zß%aÓñrW"é	SDbÚuÐÜ\x0012ÐwK¤ïjxø\x0008¤½&}\x0011hTÕ_»Ã ¹& ï°ÊX\x0011}"q\x0018åXÁF&õ$Ïgê\x0012æÞ{\x0002\x001d?ºd=àyÛ*\x001e\x0001sk×\\x0014Ð\x001dH\x0004.~\x0005\x001aCÉÖÎÚ*\x0012bÂçd\x001a{bzí	¥_øÃF²{ùÃÆ*i¡kN¬é=±^ó°Dg¥¬\x001arê¡Úv¦9\x0014¦óPhåH\x0003¤l»ê\x0011;\x000cbW3ºémgú¶Õéz}Ñµ^Èý`§¾¬Vgé@vÞv;\x0013ÖÉE¡¤*;ºú(jÎ½S?ÿc\x0005øîxý\x0000keøE¨áóRÔÏ_V|_:ùôù!5³\x0015\x0000szõuç\x0017¦®ùÀN¨ªÝÖÔt*1ã\Ú.\x0001~¹¹]!ÒßôeÈÎî\x001eõ8q\x0005¬ÿÓ¸É¹\x0010\x0008~~ûþó*¸¥¿é\x000bÓ@R*\x001e¹ÙÔÆ*ghÃÜQ6«\x000fmz?t\x000cü\x0006\x000eÔêÁíRà\x001c©Mq\x0005\x0018{m
Y@¹\x000c%Ùg¹qÎY\x001d\x0015è=*Ôn\x001ay\x0017F{Øb\x0015tn*L_VÆÆ\x001bi	 Õ3'\x0002««QdýÞój\x0005{÷`NÆÕç\x0001\x0012\x0012TJMKôa._\x000b+À^>°\ß\x00004ÞËÈ\x0016/\x001cü\\x0002MùÏ÷aëX¶æáIFÙÈØñàæ*´x¡û\x0004Éxç\x0011J¼ÿ\x0012gkÌÅ§<K[\x0007\x0013/éúäï\þ|sz÷¿þûÿ¸øíúöÎ\x000b2!Újä\x0001\x00060Rp¯[_ëÉ³\x0017¯^]\x001e.\x001e_\í>»g6íBËF¿÷Ñ¥hkÒ,¹4\¢\x0014A<VéÑN:¿¢ótô\x000cLçYó\x0018éÎö\ôÐ\x0001\x0015_-èòïtv´\x0005Ïý1\x0018Ô¹v\x001cÖ.¬JÇUÈ¥ãvqûËéë¯ïÞßÙD¦\x0002·|Bú\x000er$\x0014Úç#\UØb»¸úñôÃÅGOvK)\x0004\x000fxØ\x000ftI-SÒJÚ\x00035Ï3TÖâæ¡8w¾tyýÞv\x0012J¹8Pw»õ\x000buùÜ\x0018_KWåì*³/á~¼¾}ûéãÇ÷ÅÝU\x0000ÎÎkò\x0000¥çCKM]ùUKÄ\x001f/®~xñüùË«ïaÚ%¦\x001dÄT\åì½éºÖH%x\x000f¸ÄÄ\x0011L?
¦£"üI9\x0004ÁÜÝßÇ\x0004µ:Ò¹OjamrMÏ\x000fþþö®k.\x0005è\x000f´­g\x0013m$*RmnÊRÐóÃg?ìÞt\x0002\x0008K@è\x0007Ô§L\x001fBúÞ´\x0012?aÕ¾5Àg|fß\x0016Ò©GFjWeâ\x0003v	h»\x0001]ä®Æ´uÌ«a´³+\x0018ad\x000b²»\\x0003\x0019¢EI@Y3»\x0005uóuÿ7¦áa%\x001b\x0002\x0007ÀB\x000cÑUËÝ¾ÐlÂóÕR¶áÛÏÌþj:rg]C©\x0014¶&l»ßgÔÆ¯ûÎ|ci¾&{øñúÃ\x001dÉAo´½#ðJo
H\x0019DÛ>×d\x0008_<ý\x001e\x0019,É L
40Åì¥ê&±<\x0014\x0019lo¾dfIfúÈ¨#T×53fÏhq{×\x001dD³K4Ûæ\x001fÈH\x000eË2=è%å¶mÞA2\a'\x0016	X4¾
\x0014[\x0012¯8¶hV·Eô\x0017ímûùtùË×Û¯ï?Ü5\x0003±c\x001e\x001dAÂÞtÝ¾nÓ\x001açcúêtùã«Ë7Oîêþ
$,!a\x0000\x0012\x001f\x001a\x0012¤T`\x000cA\x0014J´Ýtô» Í\x0012Ò\x000c@\x0016\x0001ü\x000c\x0019´DJ±¨yD»D´\x0003<L'ûÇrt);A\x0007!.	q\x0010¸ÈÊèäÈ¢\x0012g¡\x0008óÛÑ-!]?¤%±·3¤eÁ\x001cq\x0001\x0013äîôKH?\x0000é­¨úh¤H½\x0004îÇ´õ~~%Ã\x00122\x000c@Ò 2X)Ja@YÈ°çLw0Æ%c\x001c`tg®\x0018M98^H/:øéÆÞq¶C»C³\x0019W\x0003)g©´ÿXþ
f0QÚéÏ­ÛËfà¶±ÉF"¯eòýméh\x000cVDÅSp²íwõP6\\x000fXrKÅ\x001e¼+I/¡ï`dW:³òêÙzñ(Æw7ýEÿÍè8¤OFÝIÓ`\x000cQ®oåv¼ìqÍjÆXÉÑæ-êtEd§;m[ó\x0017Ð\x0015ÇXbd<?-c\x0004Qe·!ï\x0001T±½,Ó_,/ËÇ×\x001f®?ÞÕöd\x001cjVâ\x0003\x001c8ÖTV¾\x0006W«Ùi÷øâéÅóý~'\x0001sK0×\x0005¬¸ä<]Í>\x0003.`Ûfè _ù¾\x0015«\x000f ´b¬ßMáT\x0001Cµí\x001d\x0005«¯ö¥kÑC>ª÷1V_\x0016q5¬à(ÚjEnÞk£äöéëÛ/wÅ/¨¤ê\x001dL`\x001dO
ú8\x0019¥²¶ãÄ÷âÍ\x000f¯¿\x0007\x0008K@è\x0007ÔR\x000f
\x00108\x001f\x0000EaÂÞ\x000b\x0002% é\x0006LçÏ*MYökpR\x001bà\x000clãv	hG\x0000¹>\x001fHqù¤qÖÁ\x0013v\x000f|ØÍ\x0017<¿RÐÜZË;ÅZÓòí\x0006ÐGñÜ\x0012Ïõã9I¸ÒòÉ÷ÒµâV³6\x0007\x0000ý\x0012Ðw\x0003Rq
ßtX\5Jò6Îêm\x001fá8`X\x0002^Àp.ý\x0005+!é\Ûz@öqGùâ/öóéÜ´ù\x0002\x0005\x0003O$.ñÃ'8º&å»3àßn®?~¸¹ýx÷+mò¡¸\x0015´¶òþ\x001eµÔV yB\x001b»¼x~úáòêù\x001dOµ\x0008KDèG¤Ú²Èì¦ÖFÇµÄì\x0008\x001f.ù°Ïh\x0012Ì*|ëÏ1\x001aU\x0011Ýæ1>èìêå)ýÅ:\x000fö·¯ïý^¢õ\x0016IzQ1çIg4¢g×#ýÛ'ÙõF\x0005Î,áL/\àÅKpNj\x0018"éA³Å~\x0016ñN¸ ViÎ ÂÊyvóõîwÏ\x0014®\x0019J¼H@T»§cEY-ÕÄ°g¡]¾¹ëÍSðÌ\x0012ÏtâY
\ðD¹:Zï¹ÄÂª÷¦Ãx¸ÄÃ^<@Ù\x001b\x000f\\x0017s«¬^ØË­n]\x0003\x0012Ú\x001a×_?ÐÁ½Ã4§/§DÏG]²ØlÁnÇ//Þ<¥S»k\x0005Î,áL'÷\¬}Á£Ô
$§ÂÌÁu°òÊA'\x001dé\x0006\x0017\x001c\x001f¤¹¨ÖñÈ
\x0012[ºEuJXU§üÿúiÓyo?múæÓÞ~úúî÷»ÔQK\x00002~LS?\x001ag\ËÂøÍhòåÕ7þº/á"h¥#¸fé\x000eÐE% Z\x0007d\x000bÕ\x0015Ø4vßA£ù×­\x0018\x0003\x001dÜE¬quýùë÷w<\x0019zÿâqFæðZ¾a+$ýúòâÉÞKé\x0006LwYy
¦®(w?òûaº{7¯¯£dg5rf»î#\x0004f\x000b4ì´<ÛøÊ¶íÚ\x001dfûeÅöK×Â±¥Ï¢ú¤?¿[Á½ë\x001a÷è\x0014xËÊÕ	Úè¶«²\x000eÃýºûµkå¢\x000c\x001eÓUi9}V]áÂfÐs\x0018î·\x0015Üo][ÎTÃµ¾ô§ºiC\x000eÃý¾û½\x0007\x000eÓa5ç=Ç¯o®î¸	4µ:ª'Õ\x0004ciÙ<\x0017md»ilÃ\x001bú\x000f÷ú÷?ÿýçÿürgù8Ò\x0010\x001e.j
U\x001aåº²àö"ì×½¼x½_Ü.tæ\x0005âkÊ\x000e\x0002³\x0014\x0019\x0010¹¦)\x0010¢èb÷ÓPße­EúoÞ^úøñæCòï
sHº¸(·\x0007¤·a³r1¤Ù}âýâùóË§É\x0019¾cèB¹úãr%ãÃØ\x0014^\x001dåD#jä48CS& °ÿdù]R\x0015òðî¥ßNãRÏËù>}øõ·ë¿.þ~ýîæëçÓ³OÿíúNWÞª=ÙJ§_\x000cs]ËV\x000bîzñô//?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þ}%,:Àm1Ð¸6ýQNEý\x0005&µô³Ûë«?Î¡ÌÚù·NÕño2«ßß:eV·¿IÊ»O¿>ýíËØ×\x0019âgÏ'×¿n\x001e\x001e¢5Ä
¢ËOhV9\x0005ìû\íj\x0002ß4ÿùØ\x000fÁ²Ûë³\x001fÎ.¯.öEaGðÅåé\x0006oxrTÅ$ð\x001c?\x000eûtÖløøç¡~AVþÝæ§!§oÕö l>'.P%I^l?L°\x0018¶Ús{wöjoBß1/ðo1ë¬ß6cÖX¿mÆ¬¯~ÛÙ¯úm3¦;Fü3R9\x0003ü6ÏýßìOO?í\hj¿y~ø2dÎ_>>ÿºZÃS°Û~f]OÑÆq'lz*ß{\x001bOêýýÙíåÍ=yuûn¿¯Ø^p;
!\x0013;\x0014^S².Ia\x0015¦èTg)¶\x0017ÞR¤\x000bg),÷t¤IÜ)Jé]7!òÁì+×¹ó­×.']&	<·ëMîÛ>_g\x0004_î7þ÷z3]Þ}÷òñùáûaü*lj\\x0013s\x001fY-¥´h\x0015H\x0003m·'è¼W·o.Î¯÷¾\x0003T¼é^\x001aúðª-¯ñ§fàM§UúÞÚ0¹Òsp?üú3|øÂ\x000f1ÛT\x0004Bþòüt·zg RìºÑ17ÝGª¼ËÔZyAú'fªÍ¹½¹½>ß÷v¤ÿ¤>Å\x001f\x001f*³MÉ\x0013¿¿¿ûóQ\´áw?}úûw\x000fÿø?IJé¥æCÐAq©EºnðPDc:Áë=«üþä÷\x0017ç{ºô~O?¹GÂ%\x0007þ÷î9ýS~÷]ËKM\x00128ÜGÈ»\x0011*#³2Á~×þÜÞ\\x001fxòM««MÝ7ÿ`7Uo]P\x0004ä×zîÃK.^bízï\x0005ã`zPljdÓ\x0001:{\x000eäÎ²Ñ\x0003rn!=fìÕÓ3]Íìz0GÎÒKÇpl8\x000fZ"ìµÇµ¯\x0001ò\x000fÆ\x001d~Ø<Ü}ùr\x0014=±ßý?\x001fïy3;\x000f.?lXZÐS\x001cl:eÌä­á­Çý6}(EO7Ïó\x0019ìX³c\x000fv\x0015xê\x0005½låk¤Ô\x0018Ïì.ì7åËØuÍ®»¬»§{~fç\x0019Â´îÜs?­;ì=\x000bÙmÍn{°cäî\x0005ÚF+&\x0012{A·¸ßÿXîjt×eË\x0000: ®¹gDB\x0017ëèïîktß\x0003Ê<\x0018ÝÝ\x000e\x001d×äËv;©±f]vÏé©FÇå.Þ´cr*pnBÛ\x0005\x001dÆ
²¤àÌ>Ô"\x000eûÅiÞ/¦\x00039îªG¬Ô#Õýß'?dM
ÑFÈ½Ûh\x0008Î£\x001bPGi\l¼{ßTsãÙWo÷Çt\x000b¿®ùuGþ«h\x0008\x0005ÏîC3è\x0006æ×{¡\x0016ñßôã÷oþ6Ù×|ÛÔÑInpÒ8Ní||Wã»~ø44ßlº\x000c
Ýh\x0013¿\x001c\x0000j7\x0019mYÌïk~ßê¸1oÿ¤\x001feýKh=}.Ë\x000f£Ó\x000býoZ`c;ðk\x000bJü\x0012®H7Ð.ë\x000f£í\x000fýö¿vCöI\x0016\x00009h¤\x000f¯ÐùGû\x001fú\x001d\x0000M\x000fö¼(C6o tæ\x0003`Ýþìy\x0002 ÛqíÑU®ýõÝý/ë\x001f\x0012¼ã¹= ø5Üx/Ê?ÂtF\x0018Ã__¼Ù\x001f *äXc'òä&ð¨CO÷mÉYéS,²[×Üº\x0013·S2ó¸³¹5>Èd\?¶ÜôÚ+âç$ÄH3Kò^A\x0001ßûº\x0000ÜÖà¶\x0013¸ÇSÃÜþ\x00143v\x000c¼ÅCÜ\3ÛÕÜ®\x0017·Î
\x0012\x0013xà\x0001fD.c×¨
F;¹¯É}'òÀ%óDîó8\x00034Ãoç5W\x001dÔJ¨ÉC\x001fr@ÕM9M\x0000ù\x0012eSòÔ\x000e\x0007½Éä±&Ö<çC\x000eäÉ¥d?8 \x0004\x0007ÐGÎ\x0015bT§EGG Ñ\x001cç\x000bÒ¢ËÝ `oªá|ô±ýìd@Ó\x0005;}¡	rZLÐ^Ðé>2 ÐÉbâµyÃ¤mM¸ÃÛ\x0005È,Êt¯m·D0²¡ÐÉRj§åÑÉig·%Ø²aô¡K÷Lò
NF\x0014\x001dõ¹\x001aÖ\ñì\x000e¤\x00079¶þwÝN>2¢ÐÉ"\x001a~7\x001arL9¤ÔÁüÃÈ\x0018A'kDI×2fòÇùF\x0008G\x0008ív\x0014F:\x001d:)õ´7r<MgÊ­Ü<-Þ.~ÏË×"r\x001c\x001dQìuD-®øç\x0011QÂ2xðZ4\x0013}´Ó±×N÷^&\x000bkÔüäa¢¶r¥vûK#æ£¶:öÚê4ËuzÎÏ«..£íêE\x000c©îeH¥vZôD\x001eÙ\x001a\x0019îc:\x0018½^J\x001aåz1¼©÷§4\x0000\x000e\x0001P\x001dp\x0016\x0000w~%öã{½<úþókdØ¹ÿ°¼\x000eèÀ{µA\x0007ÚS\x0019éÐh\x001e¬µ´2Ô~ºtifF|áÇqEÐ!~P<E6jznÌ¯yëhom\x0017\x0001t-Àâê C\x0002P;¢üMÑ¤ìÿ¢v \x001f\x0000ú\x0008`j\x0001\x0016\x0017
\x001d\x0014\x0000¸=D¤édù9ß!î!-¡·5ýâ¡CôÆFÞÿJnN¨K¥¡Ûÿæ·ßÕüK\x000e®þÐ¥(òÜß_Ò
Üþt¯%ü¾æ_\EtßÑ¢\x000fü\x001c \x0002ã\x0003¶Ô\x0011\x0015þPó®ü\x001b=D
Ü \x00040â\x0002t9¾±\x0016 v6\x0000\
ª"\x0005n²þ\x0007©\x000b]\x000e@\x0015; \x0003¶¸ ë \x0005ð¥UùS/\x0016À\x0017	º(P\x0018à®68-<K\x0000v»ÐJ/d½ÿ²D\x0011®VX!%\x0013\x000e\x00128S,&Ì.\x001f`d¡§
ÖÁqOzóÈQbÄ¨¥FWíÏ&["ÀÈ\x0004CO\x001bLWÅÀ]\x001e¥N$\x0001Hçu.-\x0005ÝE\x0019vx0¾ÙSQjè\x0011\x001d6¡\x001d\x001d\x000c2©7\x000b©Ô!ñÓ/`»\x00182\x001ci!ì©º\x0018°\x0000écäL[Q<i£üÞûã\x0012	FÇ\x0018{\x001ec\x0015"\x0010=æi\x000bQìS,C3
»\x0019¸0dà¾{Ø|<¢7û<¨lÕ]R%õÏ\x000fú\x001eÛ^ÐH\x000eygÃé\x0017wg/%§èÍÙÅþAe\x0014¦Ât\x0002MnãE\x000fËÉ½\x001e°Ñ¼+Og^®\x0011ÂÕB¸oTP\x000b\x0011ú
\x001187í'ÅÝ¼#N×B-\x0017¡rï\x0012	¹w\x001deÐa6U\x0012`qÀc\x0014Éïî%Åè`CßmØÇ#)¼¨¾)RLZè5bN6ô=Ú_QÑÙ¾ÛÛ­5§ùQÀ9yý8]i´FÑá¾§;¹­R¬F5\x001c,FP¥ÖËôÒQ8:àØ÷'Í$\x0007\x0002HY\x000c\x001bbù\x001a¯¨k¤\x0018[î®\x0007z\#gSÑ³$ç$ÉÜ;zçëµ§ptÀ±ë\x0001ÿb\x000e8v=à ÜéÖâW?/5MäGõ\x0012bt¾±ëùþjBèÑéÖ}OwÔ9ÀJRè<\x001e<))J\x0002\x0012)zY\x000cåÊdÑâ\x0011Ò\x000f¾-§p4ã,ÿ`èÉx>ùþñã»ç§ß?Ým\x001eÖ	\x0012b¤N¢lÇæþMtG9èUÝ|õòæüöúä÷×çgûú#WÒ`-
þ+¤a;¨Ón³"LqJ\x000eÚÁùÂ\x0000î|\x001aÀm2îçWOÜþxås¿æÖ\x0005ÊRª¢d*\x0018I²P¡ß¼º>Ûß'¼¢Ç\x001e»ÑÛp
\x000c_.®\x0011¤ÎQËè\x000eðº×ÝàéÑ\x001fK \x001c|ÊÅþøwèÑ>½©éM?zK¥\x000b^ò\x0003´\x000e)
ò-çÃÛ\x001aÞö×ThÇK.«¹úØÄP6¶\x0007r.çÓ»Þu£§\x0005^¬¥»#õg£Ã\x000cÀùô¾¦÷ýè\x0015u-\x0018è¢BªÜpAZv\x0004ÓgíCM\x001fºÑ'FöTÜÌªí¡5ÓZ)}¬éc7z\x000b5â¬¢=á¹-³9ðfµ½\x000eË`±Û\x000c¿ÍïrÆó\x0015ýZÒíL£ùôc;ÛÍÐjo$ÛÈ9ÈS\x0006ºÖHQîÑ°\x0014dh¡¥¥Ç*+YÇÉ\x0007Í
^]¶Nì±ïadj¡­5jk­üàñ\x0010>DõC)ÓóáG\x0016ºZ\x0003Ò©º×sw Ð ¦ÖuQ÷02µÐÍÖ\x001a-j.H*¬\x0005'71Ê\x0005èA?2µÐÍÖ\x001aí©6<o\x001cÇ%H	_vÁ»\x001eN\x001al-t3¶je¹\x0010)ðË¢¼Rª\x0005îA?²µÐÍØR¥©ã¤û\x0008\x0014;\x001dðóth¸dË	-t³¶é&Bùö¹ð.p E\x001då
áP¡þlz\x001c[ìfn;Lq¦Gn4eÎ/\x0015U2{çãì-v³·& í÷<\x0001+ZñQ.(1]w{à/¶Ýì­¥´¨XÊdMÖ;èÊû:T¶1\x001fdo±½µÎóÅÜ\x0007#;_\x001biª\x0016ýô#àRúÁÅn\x0006Z÷|piîw®p·É\x000csÃ2E
9:à,.v³¸6\x0018i0\x0010ÀsJ¾Õ^	¾:ÔÈg>þÈäb7k­¦ã»!BÎ²ZÚ#DÓgë\x000c.v3¸2òÒ§;J¾¢\x0018\x0005¼ð¸¿?ý\x0012ö¹ÅnæJ¤PÜKe¡Õ¥±Ftûsq\x0016àëÁÒÝ\x000c
CíÜÑ\x0014(?ÀwR/\x0016½ïqEÑ#¯ûiüh¤Â0@ #\x0003¾Ì-·²î?Òº«ÎäÚNÒ9!6éL\x0003Egöp\x0011þôaÇaøÐÑááx¬·6?³$\x0007äÅtÙýIÍ\x0000oD\x0000­w\x001bþéú!¢µM¨ÖùEï*lr®`\x0005\x0007¦¨|_÷	=5>vÄwÒ\x0017³\x0004æ´D§¼\x00080Ýät¹\x0000º\x0016@w\x0014ÀÎ,4¾TItoê\x0016\x000eÇeç\x000b`j\x0001LG\x0001¬ÏCW-Ð°RÞBSI-é.ÜË\x0005°µ\x0000¶ç\x0017\x0008¹*+	 ¤ªjå\x001dKà\x000fõ\x0002\"¯%ð=?*\x0012X'ý¸åÂçtw?l\x0005æK\x0010k	bÏo\x0010OMÌ\x0012\x0018àn9Ô)\x0005Pûõ,\x0012\x0000Æj´§\x001eµ;\x001b¦ßá¶\x0012\x0004V¥x :n¦\x0008v×\x0012Ø­%x>y½yþròÃÝñÆ»}
mð¥\x0015¦Åü4\x00041DiJ"öw\x0011O?¾9ùáüíÍqp¬Á±\x0003xÜ.é ÃË\x0010ËÐZo\x000f½È-"75¹é@îø¾BÅ·¹\x0006:­¸ó ]0\x000fDIWnÏ¾é°êp{íZ\x0017óûyZt¥¹\x0011fÚèzÿÏa\x0007»zaË8×»õÃ\x001béLrGÒ
3z¼Ä5§\x0003kÃàÆó\x001b\x000b1ÖÄØNLÙ.°M^U¬ÙMÒ%_r:wg	µ®©uu¦\x00121\x000eÁ¦KUngÒ¶ä5C\x001aÚ|+KmkjÛ:\x001e\x0016D9#Ä\x001a]ªH¦'e.¡v5µëB­4\x0015®ÔòÅe°A¡¦½Ô¾¦ö]¨Ë6­5÷\x000c³PR\x0002Q7¯u¬©c\x0017êm®\x0019¥æmm\x0002\x001eI\x001c_\x0000]§\x001eØ!õ :øP¢bhy¾§Ñ±lëé\x0004¹%ÔcûÒÁÀ¤µÖJºÊÑZó\x000e1NR="N¿ü-Á\x001e\x0019\x0019èbe\x001bô]Ö×¥qve\x000cL¿ø-Á\x001eY\x0019è`f\x0012vî9W\x001b¸1Pât1ò\x0012ì.&$O\x000e$É\x0019Ú\oPÍddh ¥	6P®§¼LæPcÚ$¥ÄLæÕ\x001eY\x001aèbj\x0002%Bp
M´4_fÀÖ%']M\x0017ë.Á\x001e\x001aèbk\x0002\x0006OÎ£ä9kúíü\x0008?\x001d^\x001dFØ¡\x000f¶>Õ¥\x001f(h¦.©\x0003Ó/xK G\x0006\x0012ºXHö%A/äµF/¯¾Á5o\x0011\x001cHìc"U)l4.Ói1\x0016ì=9>K°G6\x0012»ØHO)ys9¥\x001e\x000fË#u0Íj\x0004Ç÷°.&ÒG<åH9õÿ÷\x0008ÈbO·è]B=²ØÅBzBeå2óÁÞ|AO×°,¡\x001e\x0019Hìb i¦ +\x0011S\?²åó8ý ¸\x0004zdg°ñÔÑOcrýTvF Ê3nÐ¾ÕªãÈÎ`\x0017;ãÁJÒ\x0005õAæ[/ÈE,`³/#3]Ì\x000c9×È:$9¬\ë\x000e^J\x0002hµ824ØÅÐ8j\x001d¹rFç\x0007P²aºÍç\x0002l=24º¡I`R´k©äÛºÚê¾=Ã\x001a`\x000cîbhoÛQ\x0014Þm±åæ\x001b·¶\x001e\x0019\x001aÝÅÐPB\x0002F¨4ÌÈR¨\x0001ÍzD#~],MÇPj{¨7Ú þt\x0008Å\x0019ÑÓöK°G¦Fw15Ö\x0007éHNê/'ßèèK¢16»Ùzdlt\x0017cC\x0013¤GsVÃjÇ¢ÿ¦+ðfS:¨R¨þ¾K !d·Jz¨Ñ>¢Ú\x001b»Þm?ªÃvfæ5\x0013¿\x001cUò\AårÃEÉ¤Ë;;4.óÅ±q_»Í:uØ\x000eÌ\ÇKs½\yW¢\x0014\x0014âõVÞfÔþ\¬Ù¼®æuí¼yö¡¥Züç\x000cáÛóP°7Ô¼¡7\x0007É´ñg]P§\x001d\x001a³ ËqXØý\x0003Ãìww_î¿4½Ål§¤\x000fIÁÈshP|è§\x001b\x000e¾;¿¹¸9ª+vçþÀ0÷§\x000355Í\x0017 _\x000eÔ¦Úãt¨}	µ®©u\x0017j,WÛ\x0000¸m¨!ÙH
k¤65µé³ÖÀþ\x0000/ó!Òàüa*w#µ­©mµ¶òÆüO®öÚ¥´/v5´ë\x0002í<¥\x000eÐéeÒO¡¶Ó-¸PûÚw¡¶üâ \x001d\x000eÓ<(Il·Ó-K C
\x001dº@ÓhTÇ±ËµÏÏEX4"¢y©cM\x001dû,ué¹\x0015<r6u27ºl\x0010×º­ë×º<Ú§\x0003v\x001cZq\x000cØ!7,¶\x00044zèhÅ\x001eÆ>¶ÑY±ÃqÖ×QKö´kÞÙ0²ÐÅ8¦If\x0011EUú6É\x0016:¥­;\x001bF¶\x0011ú\x0018Çä4ñüÄ\x0010<\x0017\x0003SÇXöÈtÂ\x0005Ø#ã\x0008]¬#Rã|eÉ¦ó¼\x0010¸Ùkúé´º\x0004{d\x001d¡yÄtuápdLÒ°ú\x000b^2»Õt¨i	öÈ>B\x0017\x0003ÔQÓ¹qPC\x0010\x000c Ø{Z-À\x001e\x0019Hèc!ÒÓ¬ÿ¢I2\x0001\x0018\x001b?=¦r	öÈDB\x0017\x001b!\x0016E¢£DÈ¢â\x0017Ø\x0013Ø[=²ÐÅHb(j;\x001aOÕG\x0019[IÒ?NY##]$Æ ½(¢Aî¤A÷/ÉôÖ=#\x001b]l$)Xô\x0008Gl·E´H\x001c\x0019\x001bìbl4õIbõGãLs\x0019uºÑKN?NÏÊX=26ØÅØPo}ËçÑ°\x001a¡í,k=Ý\x0018}	ôÈÔ`\x0017Só5Özdj°©1àd<\x001aÏ
>\x000c\x0014ScµÈÈÔ`\x0017Sc ©:Èj\x000fuN¬Eötz^=25ØÅÔ|Õ\x001e\x001aìbjhµù
V\x001bÊjû²Ú­\x0016RLîbjLºürVpL\x000bï¹(\x0011ÁtsZõÈÖè.¶Æ8/×È\x0012i°\x0008r\x0004
\x00144bîcºË}ìk¬ö8XÙÅFÒ8¬PN$×~BÐÅÚ´\x001av=²º\x000cÀ¥nÃZsg tI`eÜÓ|\x0001öÈFê.6ÒËj\x001b¥x°NÙ¼zd"u\x001f\x0013\x0019Jb\x001c-¶42ÒÓB?mµìzd"u\x001f\x0013)³Ah±å-Ú¢¤Õn>#\x0013©»H«m¹û\x0002pvÕÊÚ\x0012×nm»\x0000{d"u\x0017\x0013¸äù ¢æY2\x0016] ZG´\x0000ÛlébkÒ~(^+â)°"¥kHnõ³\x0004{¤´M\x0017¥m½®õ\x001f\x001aî\x0016"q\x001d\x0015£hf¤ÿL\x0017ýG)D\x0010wÂQÖ8\x0008e´)@\x0018e,P\[õñ¤ìÐ=_nbq\x0000É¢g+©§ÛUàû\x0007¾»=ne>¸ÜC/ó\x000e&>rÁca²J6ñÅêL÷î\\x0014qÝeO\x0007©\x000f;Mó\x000ePà#\x0002*ôÓ\x0005fÑÝkãªä?lVR3\EÈãå\x0006Ûã|´e6Ø~\x000e·'8»>NmjjÓÚÚ\x001cä¦*À\x0019ð.lzÿD³¹Ô®¦v}Ö:Ê<cH×ÜEÝ\x0005å\x0002S»éyÔqwÄm3ûWwO¿lî?Ý¼»¿{zz\\Cí¦\x000cá!±ÈÈh\x001dºS\x0005NÔ®·ÊMì__¿9»x{~òîâüúúêP%5\x000baj!L7!Ò\x0001Ís\x0005´\x0003Ç\x000eÙF\x001cµ'ZµR\x0008W\x000báº	®ÜÕ;yµ.OS¤\x0014/'R®RÔ³Qc5<«Y\x0008Ü³:oQåä°¡\x000cç1z\x0007Ó_kÅ\x0018\x001d\x000bèx.b\x0011ÃHôàÿñ±Øc°\x0016K±ÛaÀØmO%\x001a\x001d2³V/y¹RôttsC¢\x0015ë¥éÔÜ
\x0006\x000c\x0002\x001dçÇ\x001fûñS:HM\x001e}~¨p1*±anº¦|1¿©ùM?þä³ñi@àR\x000cú;±fN\x001dhè³ßÕü®\x001b _g\x0004SÐqX®\x00132ó`ãìãü\x001fÔÎÜ\x0017*Ïy½ùånóüÝwß½Ù<?=þ}¥\x0000¨©góà4cH{I\x000fîÄPl2\x0008à\x0002ÆI¥úúìÍùÙ-ÉðæìöúêÇ%ÀZ\x0002ì'AÒ?|_ÁÒ\x00039ýîì{:ï§_Ï\x000b k\x0001tG\x0001¨{9²\x0000ç£\x0006\x0015¸ I0\x001d\x0003Y.©%0\x001d%:k¡$l\x000bÒÑàédÉ¦MçÊ-ÀÕ\x0012¸~\x0012%6&Kóà \x0015ß\x001dÓ­`º±Øl	¨yßnsÀ!møúñùË \x0004k©!ö\x001a¹jZ»ô\x001dr\x001bêä½°!vzz÷\_ÝÞ\x000c:HþÉqt¬Ñ±\x0007:
yd\x001fÂÜåG
a¾g¨Ý
t]£ë\x001eèÑqþ0õ^ º¼aÕK+.·§	ïrtS£\x001eèV&´èt\x0003ã$bÌ×vÙ§³ã³ÛÝv`\x000fÊp¼xpÝ +\x0015J¤!9ÏÓI+Ø]Íîz°£â¬ºä1\x000f\x001b`G,.ó´«¶\x001cÝ×è¾\x0003zÔÉ5\x0010gßq³\x0014Ê&ð\x0005}ºØröP³\x001eË^^*µÃrR1Ë¯ï evÛsi+Gß§KÖ?l>þåùxÇÂn>\x0017Iº]ç+oðÛæ9\x0003{;v¾O\x0017¬?½ü·ÛÃÝ\x0016wû]i+-;\x001bÙ\x0015¥`\x0012»ÁõÔ9OnÎîïS¾ÝÕì®\x0007{òåcÌìù@\x001c
#3{~Ý^Áîkvß=ÝÆ9ÖC
»gÄ.]j={:±Ç=ö`\x0007iñî%¹EpBWyâýJåèusQ[6±Ó\x000bln¥ò9®\x00031)\x0017Ö3éÐö\x001fé\x0019è¢h\x0014rKT\x001d¨}FÞ4>péO¶koÅÜBø¢.ÆSg§ \x0006ÚÏ I\x001dô»7\x00082\x000f>Ý?`÷\x001a\x000eÛk8§w6Ö\x0011"Ù¨aß\x0003õn\x001aÌ«×J\x001aÒFnY²½}¼;{uöö8>ÖøØ\x000b\x001fæ \x000f\x001f\x0000¼÷\x000cämÉª	f:Óc1¿®ùõ7·ü¦Æ7Ý\x001f=P³¬aù©oÖàÐ{O}÷òòÛi\x000fg1¿­ùm?~ÔßHmwNñs\x0000}$|0ß×ü¾ßö7À#Ð æ_\x000eÛßr\x0010ÖÆ0Ý'i1¬ùcG~Ï@Iúñ£àÇé\x0016\x0005Kñatz¡ÛñMû_ñøï´ÿeó;Í?]a°xñ¡z>gõO?ø6TÒ¸;$\x001beHöÃÃÝÉ\x000f÷?}z\	OmUéL\x0014¢¶º4¯Úó\x0018\x000cðååùÉ\x000f\x0017¯Þ^Í`Ç\x001d»±Ç245\x0004)º·Û¯qº¿íBvS³ìªH\x0007³âIì¥ß;n\x001e»ßÝ3~çííþóç»Çãí\x0019ölû¤\x0013°\x0014ÑZäØ·ñÆJÔ¶gÕûÉÅû÷çW\x0007;6°\x001cºC÷\x0003Ü©Ô\x0002\x00037Êóh$Ñ\x001e¹P
SKaºJ¡\x000c**²å¯á°Ô¼»i]ºJ\x000e[ËaûÊA\x0013lc©_Í`Æ9±	Êï\x000f,ÃÕr¸r°nÊbèÈ\x0013ÓñD¼=Osë¾Æ(9lø"ôoï£]\x0015jõÿçÿ~ýøëýÍÃêo\x000cµÎ\x0019ËÞ t´PæNéÞó"ÆÉë«w\x00177gÇeÀZ\x0006ì*C2\x0016<ÿÐÇÀ!QCÙâÒ²\x0005\x000fjÝù2èZ\x0006ÝU\x0006ë8Dþ\x0000\x001endPR\x0013¡ö÷#)ÝÍ<±CæÉåã\x0017:
¿Ü}úr,øËÇç_îïÖfÆ)í#IÓ\x00009\x000b\x001a\x0000åOaÃtns:\x0006t\x001aÞ§%SþòêöòÍÅù¡,9»bDÞâXÃ/\x00058Ð¯¸vO÷ÕÕòèZ\x001eÝ_\x001e]ê®it\x0013\x0017L¢\x0016O×É«ÝZqªÒq\x001b=wÇS?ðA\x001eJJÏ\x000bT\x0015Ï\x0002Ùé¶n«\x0005#â¿`Ã¡Ì\x001f×&sñ"7Í²{|àå\x0002iØÑ\x0007\x001aª\x0007ü¤ÑÎ~\ëÊÇÝH¿QÅ®¼\x001dÔ&wÀÜ3\x000b;¿R}Ð×°sø5T/ø­ì:PÓÜÑJÁ¨ÂÒO\x0017\x000e¾\x000eÎd75»éÆî\x00147L¢ÙZù=üõLî÷xXÀ]
îº{+öÏ:Í\x0015h.-Ýð~º{\x0019{¨ÙC7öät°+¶\x000cÏ!\x0004%3,ü9'sÑÕî9Uõ\x0014Îô»ï\x001eÆY=?\x000eôBT.:é\x001f=\x0004¹9d0]F%óãn®Þ¾=¿LÊæàkÚ=±ª\x001eÆÙA\f\x001b|*Î3å}ÖPyU'!L-é*\x0004¢Ì\x0004v´©<\x000báKôæÐ\x001di\x0014¶ÂöÂJ\x0008JêÛLð2\x0018*\x0004ÓM\x0008W\x000bá¾ÉO1êxKþ¾§ \Ù9
-¥L2Zp\x0014ûÉ¬Ù½Y*\x0016ûâîãÏw+\x0012Ò«
5¥ÕyN\x0003\x000c\x001c-ðé¢½ï\x0011b/Î_¾>?ovóØè#O¸>\x0003ÜÜhF\x0017Åì`'­ÊoÚêý\x000fÏég\x0007c\x0001¬kdÝ\x000119ç[tÐóÊ©6eo\x001cc&±©M\x0017b34«IÄ49 ¿ð(ê÷L¬ã®µµµýÃóýW<è+îPnÇ*\x000f%¤<\x0010öé©åª÷'¸½øýA-\x0012wÓµb='z\x001d3µÖÉi7ÔP6pÊ\x0010O&ö~Ï¬¹È\x0018w2n0Ò\x000bàËï~¹ÿDÅyï7Ï\x000f_\x0006üËÇç_W+¿¨LéAL¥\x0001Ù\x001f^`³þ³ÓZ<i7\x0017o©VïýÙíåÍ ÓåÕí»J
Ê/¶»}×$\x0019µ­\x0016ã(ÑùO\x000f÷\x001b¦\x0006(E\x0003ß\x0015?î\x0004¹¤u zo\x0013¿º¼x¾W\x000fé3Î\x000c¡k\x000fèqçáaóÓ ÊåãO&§§uþÝð\x001b¿{øÇÿùü]IxôÉ\x00010*'uÑäBÏí¦Ò¯(\x001dªwºåÒ+ÏååÙ«,ÍÕ«·<.
Ö¢`oQ\x0012t~dH¢8ä)_{P%ý9]v»J\x0014Sbº\x0015°y$AÒ«(Ô¨5_d4åv\x0013ÅÕ¢¸î¢\x0019fQ¬æp*d#²(~ÏpûU¢øZ\x0014ß]\x0014ëè¤µËPG-_ÅO×­\x0012%Ö¢Äî¢¤³î\q\>+Úqgdm}·\x0002c\x0005Ö_%o\x000båÄ·PKN×é¸ð\x001aQF
\x000cúk0Pyeº
$\x001b;Þ#\x0004/²¸²=t?÷@m\x000c\x0002Ò\x0010\x000cÔ\x0010åÜk;\x001d\x0006X%Ëè°@÷ÓTm§=æ5\x000fbD\x0019 í~\x000ekD)MG³TÝEqîmdrÈBÞaèx\j²zò\x0016:_\x0014 >,õ\x0003WþAqÝOÞmþúÿLÿHóm\x001bHÄ?ÿãÿûr÷p÷å»ÏÏOß]ß}y|~útP¨ú}ëH·~ÅÇÂ§³0(+\x001aT6Ü@/óËóïÞß^w}~su{ýö\z=¼;ûaß}£Æ\x001a\x001a×C§[P.Ê¡ç\x0002jJ\x001f\x000cíÔÕ>ÐºÖ
+\x001dÃ©
\x0019:-zN·M\x0016Ú
ónÕÙÔÌ¦y¨¦Ý\x0011x\x000eRvÈÐvx7ï\x0003mkhÛ²;¸a\x0016R\x000e\x001bw]öÇÐÞ÷ÛÒ®v
Ð9\x001b C&6ùêLÄÃÕ¹\x000f±¯}\x000b±É·\x001b¤±R\x0000ì-Ê¦\x001ft¨¡C\x000b´Í\x0003;)<ÈU\x0007\x0004¾\x0012t\x0018î} c
\x001d\x001b \x001fÚ\x0004ÒJ\x0007î\x0011í=_¾h¥u] ¹\x0018\x0016Õ²Ôñ¡©²¡m\x0014\x001d\x001d:@«èÆÖ0ý`\x0014ÈÚ<<<\x000e)Rs±5$âÛ#7=J^J`çu<n[(6tvyyu±/:T±cÍmìaèf1°\x001bÇÓM\x000eî¸Y®ktÝîOM&w^Éä`dÕñ¸Î^njtÓ*¿F'tmr,<]\x0002«A¯lßýbkrÛF\x000eÜÐ}ñ\x0014d\x00120¡ûã\x001a|	º«Ñ]\x001b:ò8à¬È\x0003/»q¢\x0013½ëËîkvßÈÎú%YÐÜ¼({ñNâpáé\x0007\x001ejðÐ¸_\x001cå\x0017g¿;jÙ0¹\x0015)¹¶ï¢Ç=¶±§³©Ä]>\x0019Ý\x001aQ8nù\x0017°o
é`TvL~¬Ï&XÅCk):#\x000e"ÆØ\x0015~lPÛ,*J<lxånEiåÅ,9o_"À,*´TC-4JÉËOîgx¥únM6£úÕW~d Ñ8i8u¼òT¥m\x0018^Éuª«aF\x0015O~úöâ\x000c¬)5¦¤y\x0012=áG\x0012\x001aUeÚ+rëO\x001f!¶)á\x0015Ð]ýH\x001ci\x001blôß\x0003äf34Ðð³y:°í«
]5%Î+6:ÁÞäÄ\x000e|;
ÚE'ì]w<+¶\x001dW°(QtWâzætûu±«_£ãmÇ&pºìØÄ¨OÝ ï\x0019êRÚwÃÿéË<]ozúIÓÞqù}ö\x000eòcsÚ÷\x001aËÞéìWâ£â[nVê\x001d;\x0012\x000c\x0019\x0016\x000cè¢4±ïþ]\x0011\x0010Ze\x0000\x001fK\x001cOéS%êÇ\x0015õÓ÷NEÏ\x001bc\x0019ÏÐú\x001d¾Û\x0010êÂ¯üßÚº¼½ÿøø°YD¯£Gý\x001d_â
L¯áè\x0017È
FÞ^¼¼º<Á5?6óG¹¨\x0004Ôüè\x001aÐbñ8ÝQ\x000b¶_×üº_ç<0Zÿ!M0¯¿\x0010«>~I\Èoj~ÓÈ\x000fé¢\x0008=þ@.èpÁÈ\x0005]áQïg!¿­ùmëúÇrÑ¥Ç±ß\x0012Ðç\x0019ôü®æw\x001dÖß²\x00065ÙÒú[ñ>ñx\x0014s!¿¯ù}+Rûï-^K\x0007½\x0016ýcá¨!^È\x001fjþÐÊ1\x000fn¡ó;ÔLä®ªåÆ«õÑÀýBþXóÇ\x000eüA\x0002lÒm2í\x0012JV·O\x0015é!ó¥Zù
ædÎü|ÉûGsc ²¾GïBþ±ùmµ¿ x\x0014MZÿäVç×ªåýd©öÜ<}¼ûu/ûÈôB«í\x0005JfåÈ,ðÆG+nOìmxadx¡Õò&Gù4»ÏCG5Ñ²ð&öÞø#»\x000b=\x000c/guD§É\x0003Í\x0002í\x001bPgÃ\x0005#Ã\x000b­whæ?hNª\x0001å'Ïô¯[\x0011 £±Â\x0002,/4Þä¯
ý\x0000ÊñìÓt\x000fölº¨co×yt\x0013\x001eÜg¹\x0008¯\x0017\x0003¶1Ûô\x001d \x0006\x0012\x000b\x000c¦·\x0005ÃÑ-l\x0010C.aß\x0018õ4üú-z6þòôÿ\"\x0002R[S\x0008yC%js/«ä.àg>v
3§Ò_®÷¶{¬Ðµ\x0010º]\x0008.ìRF@Îs1Ü«lÐ«Ç\x0013\x0019Ê`k\x0019l\x0007\x0019/Ï¥f\0´*%5\x0000Í¬î"!|-ï°ò°\x001c¥³|³÷ååtF>É\x0004û\¸ëUÇúát5>@.6"í
ãàSE»Î{=]ò
jß4^!WK¡°XirOs\x001e£1%ßa½X^\x000eÉÄmæ\x0003µ\x0010àC­µì%§g½ÏÌ"îâno «\x000féßz~ú²ÄBh<2\x0008Ai¼>{|Ö{þ\x0014&w\x00138"ÄÉåÉÕ÷\x0017o_¦\x001fî«%­0µ\x0010¦\x0010:J\x0006²£á9pm%÷16ãT,\x0014ÂÕB¸\x001eB\x0018ÃÎÐx\x0006¾ô8\x0005ò%úË\x0010j\x0019BÝ\x0014s7$CTòìgÈ\x0010Ìèû2!ê$P©§¦/¡skHêå7´ÍÉ_BÂ_Ô®¶»\x0018£
]¶u§ùP$ÝÊU\x0011Á<¦Q³·ÞBN6t9Ú®ì(ïÛ\x0004§=¬é¶at¶¡Ëá\x000e*wmIbøÀ5\x00124o <m\x001e¿.\x0016ct¼¡ËùZ²C©ã4¿.;ÏçÛÎI-EØMÌ
®*SyóøüpÿiÁviÿÈ«\x0002\x0005È¤Ý´·A­æ¤\x0013¿¹º½¼Ø×¦âÆ\x001b[¸)¡ì¤èQXB©Ç¯?ó¡u
­[ ­f¿"\x0018#©Ûnû\x0002¥Çð\x0016`\x001aÛ|#kmkhÛ\x0002Jì\x0015
1Ë3¤½S¾<WÎÊËíjn×Àm&ôüLc£xÐveÇ©\x0017pûÛ·¬wº9(ÏÃÜzÜF[6÷\ùÜ¡æ\x000e-ëíªgÕÈ~·ÛÜ[3«ªi.w¬¹cÓ>Añ\x0001h½eR`GÝuâ®ï»®._Y\x0001®$¹2dÓøP*#cÇ\x0005±¥l1¶G(+\x001ed°G©qÒ³ªÉæ¬\x000e´\x001dkË%*Xà®ªÞBÉé×3²çT8´èpKï¤¾k\x0001/OÖ=7ÊH\x0013B*´ô^$ª\x0010©8uØáÁ\x001dÞãdª{­ä\x001fÔ5Z×w¿üºyú²(|ã¦ô°l4\x0004¡Æ¢TfEo®Ïß¼;»¾9\x0010º\x0011x¬á±\x0011>FÊfÎð'w\x0004»MåïÌ®kvÝÈnÝ©OrÁg,»<èYñËùä¶&·mä®<\x001c<¶1×:y\x000fZ^"´õ\x00121\x001fÞÕð®qÙ=ä\x0013`xÐH\x0000qYü¬´Èùè¾F÷ëNùØÛzJ%
\x0006$Ê\x001b×>Ôô¡u¿ÇSÎ\x000b\x0006	`øPIé\x001fÌ
vÏ5|lONíÐzã*!ùä·³Ç\x0018`^VóløºvX\x001e\x001bÖ-½/!zª/ç\x0013\x001bC)Øê«'al \x001a-\x0001)C°4é»÷iÌó\x000c*W±5\x001f¤æ¡QÏ\x001b*Ù\x0016|ÏIH2\x0019NÄk	½\x0019ÑV³mMÔ\x000f¿vº\x0018¢äóÏèµ±\x0008d© ÑT}õÅ\x001f*h´UÎùÜ¾\x001e\x0008£øfÃ\x0000S~ Î\x0007wd® Ñ^}õÅ\x001f+h´W\x0014¹óp\x000cVÐ\x0014¤0#
¶\x0004\x001fÇq£kì´Ê=#¬Ò=cá\x0003åt\x001fi\x001dlÕ:à¸sU&VJÊ\x0017{;ç9v	þèÜbã¹¥ÑÏ6ÓGÍiïÞjÅN&½+÷¥\x001fm|lÜøÖ(I®\x0000T§<ÍQIõS\x0008\x001d5=òut£¯C
õÙ[\x0000géf¸ËE¦%ö¥\x001fZÝxjirÞ÷\x0010³\x0006½Ñòø\x001dÍ¼V\x000cóéG;G7î\x001cMFj\x0008¬Zê<ë
¼!*ÓùzeF[Ç4n\x001dM=@sÎ&=}ç¢9OVñCg¥iTëÈ"Ô\x0015g«¤\x0008!§.[
2Äcäà6*;¯xtÏ°+Dò\x001bZøj®8\x000e©¥\x001f\x001a½\x000fÓ|ÊêÓzõàx §Ñ\x0006¥èà¸ÓvrE£)gpcÍmÜÛb¡2Õ#qoûyÍhÏ0[×Üº;H3@Iz"îÒ
pÆÝ|6·­¹m37¿æ\x0004/ÑÄ]ÚîÌ°³³¹}Íí÷	o\x0013O\x001dàv·IGêXSÇ&j\x001ds«j
8I6±¼
Ç»\x0004ÆÚ¤MhW:Ö¡.I¢5!Ì¨#8Î
°£\x0005Ó\x000fª\x001cï6¿Þm\x0017`k£"wòrÖðæ\x000e.,>;#µõöäûë³wçg·ÇÁ±\x0006Ç6ð AV\x0007^
7\x000eáýM	Þ=ÉuM®ÈÁÄI\x0017¥^ÞS8Ó?õV®³ÉMMnÈ©¸³o½\x000cM\x000c\x001e$\x0011:É3'`6¹­Ém\x001b¹©Ògp(ÉªÇË»\x001aÜ5'/Ez¨RZë4÷"?\x001bÜ×à¾	<éC~i%pÞ*%w£3w¨¹C\x0013·µÒ\x000cÓ§[uà\x0005·Ò´Øª\x0019Í0\x0017Ç<¶m\x0015ÃÝG=Dö\x000bÓNì$þàÕË\x0007Ù ÕDî,µ\x0019Ë©¿[\x0007ï¤TÇâ¬DÙècóÙf?ict]Þ:Ù.8+·j6úÈB\x0005õZ.\x0012ôðd\x0019=(Éñ5ØS)ÂÈB	uxÊ«auî$xdÍ>i\x000bÈG\x0016\x0014ÚL(
Îc}NØøÇÒ³hFuà\x0002ò\x00056\x0013êKý÷¦l\x0017/»ÅÎ\x0019- \x001fPh³¡\x0011KÃÿì5\x0012yP~Û hNÕlô\x00116+\x001aB\x001e\x00151Ìí\x0014õnø\x0007\x0001¾ë\x0019\x001dÙQh3¤Ñî\è¥©L\x0000ÙénÆh\x0001ùÈB!fwÒ\x000c*v\x001a\x000e»^-pdI±ÉZPrH
âè\x0006]\x0015\x001a{:\x00018²¤ØdIBhé\x001fé¼,º5àb6ùø&ÚdHi\x000c nÉóM4lÛ\x001bw&\x001fÙQl²£\x0016Òsl«t\x000c¶,ºµ=5#\x000c)6\x0019R«Ã6,\x0017yzV\x0008^(ªëN\x001fYRl²¤Vk	\x0015Qh\x0003\x0000Á¹\x0012	ízÆ=Â&{d)õK¡s'õ\x0001=øíØ®\x001bf¤Õ±I«'ÏJ\x0017Q\x0003E`\x0008=b8«xc\x00069ìè`û{ò°9¹¹ût·\x0008ÜEñ\x0001hê%\x0017©Fp%\x0017rNêïÉåÙÉÍùÛCã0\x001ckrl"§ÉòT¡dÄ\x0001%3:ãz>¹®Éu\x0013yò»;âÅ¡ºv 7²YÜ¶óÁM
nÚÀuÝB:ÏI\x000b´ûE£w\x0005·5¸m\x0001w´µå9nè«;;#»|ÎÜ¥\x0005ä®&wMäÉü[)÷\x0019ú¦\x000cä¡Wár\x0005ä¾&÷mä IÁã)+àe9SóÁC
\x001eÀµÉ³YéZ$¯D¶#ßædÎ\x00075xl\x0003÷§ÁiÐ¯fðÒ©\x0015çµMI^\x0007é`Ôl`\x0005zâe'æJøL®ËMTV\x0008Æö³É:\x0007§¸½CLnä½ÅÁ:ùä#û	M\x0006ÔQù \x0007F¤W$¥\x0004£Ý<£ùè#\x0003
M\x0016Ôy§ÛæúÊdt§¶×ÿ®ûedB¡É:cå
Ú§ûbí\x0002%^4£­à\x0012ô\x00116+jÍ©	\x001c\x0019UüB7Ô-å\x001e\x001a3^\x0016\x0017l(´\x0019QSz,ùt³íR\x001a¡§ê¬Æ>sÑGF\x0014Ú¬hZhËÛE¢_PE;«èd>úÈB£\x001dµÒºÇ\x0004fsT¢Ñp¼qø\x0012ô!fKÊ\x001b\x001d4µpÌä2¦Óª\x0019Í1æãÈb!M.\x0007]\RêÀþb\x0019\x0013hüè\x0002ôñ}®íB\x0017Q\x001eG\x0007yxÛ×h7gLÊqt\x0015üN¶_ðÃ%úñùËÀþöîùÏ\x000f÷ÿ±\x0004\x001eûI«^¦wÚc½J¯no\x0006ü·ç·¿¿¼øgðë_7ò'ãyÊï/ÑË¤C%:6\x001c)¹^NokzÛL¯¸Ñª¡jàü®~U\x0014|\x0008\x000fìr~Wó»ÖÝ\x00135Y%'S.r~W\x000c(¶5Bo~_óûÖõ§N+l`}À@I\x000eèÍ\x001ejöÐ¼w°x5!òÓcÚ;rpýdÅøuO
ïMMüTãÃüÞæaÇi\x0017\x0019ñâ\x000c9ZÎ#~lÞ;ÈIÚû3¾)ëïz+N\x0018)NhÖÉV	üª\x0010ËúÃápÁr~3â7Íëï¥½		À¯ÀJ\x0002LÖ\x001dñóT?4ëþ`îq;\x0005PÛÜ#\x000f\x001eË\x0005\x0018é~hUþ1i ×ªáqx\x0010\x0000äYÕ#unË\x0005\x0018)hÖþÉqóÛ¶V\x0004Î>Ö\x001e	õ-\x0017`d\x0001 Ñ\x0004¤ß\x0017O\x001dt=çG\x0010Êò«mo÷¡/H\x0002ÄV\x0001ÀIvEÉ »¡ì #­F\x0017óãÈyÆFïY+c$ã
È\x0011\x0008¥=go\x001b#\x001b6@+oiÛç«n8Íëå¢G8ãT(6ªP
J²\x001e\x0004zU\x001bøÔEX8Riµ\\x0006ÂF
4Ì¨±\x000fìË\x001a%­tì±R±Å\x0002\x0013g\x001a8ÚI/QGíÆxµ\x0015
dì,²å\x0002¼\x0008ÓèEh¤9}\x0004T(« [rà»k 32\x0001¦Õ\x0004 åKrÝDrr0X%Ó^9¬²Â
\x001dÏ¸ðeÒ`)+C_¶ì
#-ÈþI}-ýÙý\x0008±\x0008\x001aJ?/ð2ðr\x00119¶¿Ð\x0016L\x0000Êì¤R¤o>z	zµyZä\x0006ëÀ Q\x0007êÙ14Ø)m¥<Ì©\x001c¦øÕ«³ëC¡7&Ç\x001cÈ=ì\x0015z8\x0004î%3~g¤.àÖ5·nâÞæÇG«øîå}ÁÊ\x001egd- 75¹i[ñmª+­\x0019\x0003Ù\x001b3:.!·5¹m"w¾#KÎ>:Þ+\x0012èôzNÿ±ùä®&wMä\x0001esÒ85hSæÎÌ<?\x001fÜ×à¾\x0005\x001e-7\x001eÓ2ØG>\x001fç¾Ï#\x000f5yh"G+Þ£w\x001c[ð!± &t]óXÇ¦Í\x0012Ëìä\x0018ej£O\x000e\x000cø¡æØýÈalì\x0010iwÜ³HI\x0015\x000f¥µ»÷ó\x0006OÌE\x001fÙ!h2D\x0001
Ï
·
\x000cÏêMû¥\x000c\x000e\x000fØuÕG¦\x0008lÑðêc\x0018=pYZu1þG"\x0008cð.\x000bÌ\x00104Ù¡a"©ôX\x001a\x0012\x0013\x0006Õ¢µ\x001eK={d É\x000c
C\x000bxøÖV\x0011d¶a Þä#e\x000emÚ<¹å2ÕBÇüVed\x000c]Ðº¯N¬'\x0002f½(\x0013\x0001¿\x0011s4n-C&iÛYæ°J»\x0002ÄV\x0001ró
Ñ5û×no\x001aanæÖ¼Ý¯þôa´ÿÕï>´ÐkSºpP©eöÚ£Ú:í\x0012v/w°s¹{N^lîå(¤áî
P·\édÍÌ\x000b\x0007Í{9yqv}}~0Éb÷¦\x0007;7½b\x0018\x001f%«È9%ý-|(Ñ¦¹IÄÐµ\x0018ºÇ×Ò j\x0010>£ÒncÖ^!©å0=>GÄ\x0012<³:\x001bäBLy\x00012³Fb.ÃÖrØ\x001eßªì,Ëò\x0016\x001aP,3Ãd¹\x001c®ÃuÃHæ\x001aÉaøã69o´ÓB9|-ï Óo¼\x00181F]b3ÍÄ"1B-Fè¢tKÒ \x0007×¹(êÊ\x001c\x001f$¾\:½Ýì¤·¯\x0015Äñ\F\x000b§Ñp2EÁáí\x001eÆªÌV\x0010©\x0002Âbh$ü¬\x0013d¤u¡ÚuéÊÆ£¢h_).Q)Jwn5Ó"1FÊ
zh+GSK±¡ycmÛlýK9>\x001b\x000b¥SK\x000es,©«+ÎÇ÷\x0008;) \x0011ê\x0019*?ÜÿõþîiñhnoE@3k¸ß¯öUQÍk¹ùÃÅ\x000f\x0017ç×\x0007ÛËÁNúgz\x000cÉ\x001avgiZÍÀî
\x0017y«%Þdº²ÛÝ¶±ûÀ=O,\x0004ÇØ[ëK·Ü\x0019­ °ûÝ·±GSÇ,ÄXzÑ@q^WýÙä±&Mä\x000e£´F
+­Å\x0003{ÞÑÏèb±½\x001el\x000b£Q\x0018kà½¢â¸\x0001^¸±xà·^Tó&nÏf\x001fívhÛîÆ\x0004Jg_äd1\x001aÅ s0ìR\x0005ðn\x0004ïÚàCàTÕ\x0004oxbª÷À¡¯\x0004?cBÖ\x001cxP;)þé\x0007U+Ëw¾\?þ}ó°Þ$õ¬i¶{Þ`,=Ñgµ{wõöæäúêgÇù±æÇF~eP\x001aÒãã\x0002È ,\x001fg¸	Ëðu¯[_\x0007ÚÙdJ¹±§j]^þ9CÊñß|sËok|Ûºü sU­¢Çk#Í¸eùç\_ñûß7òë\x0000æo¥ \x001eácye\x0001¤É/Æ±òiÕ>¶DÝåÖå±ô¼5Ìc\x0000£ã\x000b­çW§Ûâ
\x0004ÀI\x001eüö¬óñÑþÖ\x0003ðÕÏ/ö?´\x001e¯¯püîA\x0016¬¼{¬\x0002x\x001aUÊjB´ÐðàÚy\x0017íJvR\x00071¾ÚÇ\x0000µû\x0014¢ª§×þüp÷ü´ÈsÅ\x0014@:ÔNfÇÇ×\x0019ßàüäõÕÛß_ß^\x001fGÇ\x001a\x001dÑùÞ¢"r\x0010.¡K±H°³>óÙuÍ®ÛØ'o@Kó+³ë/\x0003Â¬´ùè¦F7mè^m\x000f;Æó	N\x0015ÁÏnkvÛÆ\x001e¯ÏìéÔrm¦GY\x0019â¬
óÙ]ÍîØ Ú\x0012´å9§Þ\x001a9¨qVªÁ|t_£ûFt\x0010w\x0001L®·RÒ\x001bÕ®êKØCÍ\x001eÚØ\x0014\x000fHê³;YqyÝý¬Làùì±fëî
{\x0012#RxïÊ²Ïêª6\x001b½~eQõ+Ë*ö8´
Èwmnª)IÛ9!äùðc£ÚfU©9y4|VA¦û aüp¬})üÈ4Am¢Ll\x0013Ë÷¼òJÒ%©iyWø6
\x001f\x0014Ô=\x0019Iì$-8èY¹4ÇÉÓ_vÞ\x001cBysx±¹xØ,²JÆ±U2Q\x0001_\x000e\x0016ÕH½;õâìâòòì80ÖÀ¸\x001eØp\x\x001ebjÊ¸ð\x0019MÕæòêW·,0WdE°¹ï.%ýJ!M<æ>\x0017ØÔÀf5°.}\x000c¢-Ã\x001cºRRp<>6ØÖÄv51\x0006\x000ei\x0018*BçÃcÇ\x001f@æ\x0012»Ø­'¶ür`¢ÓäëJ·Ô¤Ã»\x0011ûØ¯%¦åwE.©Þú¬iwJK\x001cjâ°z:\x000b¼+@¥±y\x000fGø\âX\x0013ÇÕkL\x0013þ84*RË\x0003±+ù¤îx:ÝLâºwÈö\x001dlÍ¶P%T$déùàgL,\x000b<ÒÆ°Z\x001d[¿\x0005våÝËâRãñ[Øl7®j*nµb;Ût\x0000}ij]\x0006HsÇý\x001eå;Ù®é\x0007UçÝÝÓï\x0016=Ô\x0005ï¶\x0019d~htXJ\x0019g\x0015y½;¿¾y}~ðq'ÁÈ±\x001c%u/8[\x001c­ÝvãDÏ\x0006×5¸þÜÔä¦\x001c¤ý\x0007µ\x0006[úYë9±Ùà¶\x0006·
àZ¥«®\x0007]Ã);Th,\x00115\x001fæ¸þ³É]Mî<r\x001eg\x0011)\x000bK0\©\x000e³z\x0014Ï&÷5¹o]s\x0003eÍÑÊâ¬âÙä¡&\x000fmk2\x0013"Ýw)\x00032wø¤`¯f\x0015.Ì&5yüÖ¼ÎÕ\x0019%Î®Zt\x001e¢7ÿHÁ\x0004VsfÏ'\x001f)EhÒ\x0011q¾ÙÃl @²dý¼\x0018àlôÑF~§rê\x000cÃiü`d§\x0019cÄX¢º@-[£ª@mAò\x001c\x001aæ+8\x0014S*Ó[ü¬°÷\x0002\x0001jq\x0010 ªïZ%Àv\8\x0002ÒÊÆÙØ	Þî:¶Nºûrÿs¼¹»ÒTÜ¦<ìïJ)K0³f½;¿¹¸á<¯ã2Z\x0006Ó,/3t­\x0002+ÁLoL©BÑ]|¾\x000cq×\x0005[\x0017øóÉÍÏÏß,:¾é¨Ò\x000b[nFå¤£¢ÒÌiN\x001eõû×·<;¸â®\x000b\x001cë<ä\x0015àéÜJ#<-\x000f	¼ÌÄ9]ÝçÜ4'5Ã³h(Ït­.ý[1ÎJBKnkrÛFnùAÜP\x000c_3¸ô
°³¦tÌ\x0007w5¸k\x0001×É¨íQ.aL\x0017½Bnº.¹¯É}\x00139´èöéÒ\x0007¼Y¬\x000c\x0017·\x000eºnóP&rT2[Z\x0006qåõe\x0004S8=<Öä±<ÈL\x0017\x001f\x0003ED\x0007rj'Á
¢¡'yí\x0002ÇQºú
tí$æìiZ\x0014w&E·ø#½¹\x0017¢Ã\x0008\x001d¾%ô
&#úµÐ\x0001vÜ0\x001aÀþýæÓýÝÃÉ÷wOO÷?.ra´µZ\x001a:)	!n\x001bÎ\x001aqööâü2	q}}ñý!\x000fFDÀZ\x0004l\x0017Á!MG®²<ÞMa\x0019 =ã-©\x0008º\x0016A_ÁÔ"oò+ØZ\x0004ûM~\x0005Wà:|(÷¨s\x001cp'èÒayFéÉR\x0019|-ÿ&?C¨E\x0008\x001dD\x0008R êI\x001ad\x0019J\íûË\x0010k\x0019b»\x000cÆV¹fx\x001adð#eõzÉ2ÔI^¶¸CßØ±îa£´¥\x001b\x000c\x001f /óÖÌ\x0018´T\x001e\x0016îëË02\x000fÐÃ>|=\x0019\x0012ÖNÔ-Ý*\x001fûüããóÃý²¢JÊ^C	\x0016rçboÃvìhçûóW·\x0017¼lfÇ\x001dØm,Wá<Ý'c'1r\x0015f<c-@×5ºnC§µt+ÍÃª½-=÷½YÙì¦f7[&§,¥¥5ù\x00102â4\x001c8±ÝÕì®]³&Òl6ÞîR\x0006çæTÎ,A÷5ºoÛ24{w{\x001c:.\x000f\x0005ÄÑK.W4?½N\x0016Ò£(Ä\x001ax\x001b%ÞF\x0013WdÝ·é3\x001eâæ¢[¥FèÃß7m\x001a(CZiÄ\x0013÷·(sq½îµgvßTBý¦ryÿøi\x0011u\x0018º+\x000eØFBÞ(NÏ\x0008qÞ\^\½=Î53~\x001bÌ¦f6«}Ú\x001d\x001c\x0003Oÿ\x0012§hù\x0012¼?6Ài	±«Ýzâd,eÑI)X²>Ag´\x000eË\x001cjæ°ªxøU\x0016F?\\x0014#~
\x001cÏëË\k¾íc
´3%·	"7|ôe²S¡Û:Ãè\x0004Âú#èCbf0èÂ<CU\x001fe;U¥é\x0007ã\x0006ï7¿Þ'|QkPAËÓ%Ý!?@é¯\x0019ÕÌNoïÏÞ]$üPwS\x0001k\x0019°]\x0006g¹\x0008Éøä\åêØ`Ê,J\x0013çv«[ ®eÐí2¤{\x0010;·ª¬ó(m'é\x0016ç¼g.ÁÔ2v\x0019\x000cF~òA%ýö,\x0016\x000b8³Éé\x0002\x0019l-mAK\x0012Ñ0\x0018ø;X)N²jî\x00052øZ\x0006ß.\x0003ØSå;ðg@I¦ ^:½EÑg\x000eß\x0001¶Í\x0018¹ 3	!»E5³Wà\x000c!@í½«A/½{Ø|\x0014)^o\x001e\x001e\x00165]¶ÁKØ²\x0017¥DA\x0004^ù_áÝåÙK\x0011áõÙåå\x000c|SãV|§¹\x001a8Ýúô¶Z^]<Ü¾e\x0011¿ÛyKßvkÚ^Üm?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==\x0018L\x001e¿ùåüÅÁÚî\x0006.%&òs<ö8 =\x0007Å*ÊÜ°I4Ú\x0006¿P
·\x0010æÇæ\x0002)Hc{Å*o.ïî\x0016×\x0017Ëi"ë$l\x0003D©ÊÇK\x001dY
G¥ÁÙÞ³³ÙÑË5ª­½¿0\x000cü~ñÉÉ4«\x0003ë½uG­÷·ËÅÕâvS\x0015°·°1rQ§ÁÃ\x001bé¥jCò·.j\x001aÌúÛÁìpv:P\x0004|¾ú£-&ä\B\x0019¡\x0003æö×²D¨¡{A8Ã+3\x0015 Å\x0000ÑR@Çsÿ2 ¦Û\x0016¶\x0012ªÔ\x0001YJ\x0018\x000cm\x0019g_Gª¦24$83	!
Hu\x0004F\x0011:ì7àÚ¬%\x0001l«!p\x0011öÕ¸F\x0011zl¹÷D(IÀÎXjÁ}\x0015Ø&\x0001Dáô(\x0002\x00047³\x001aÆXE\x0017\x0001`ÀØ£Ä¤\x0002:
¡\x0013I'@\x0014\x0012¢­aB\x001e\dp\x0017\x0001]÷É½ùøþ"¦V6l´\x0002¼åÞìjùýònïåÍçåíûa7\x0004~ÔDE\x0013²Â\x001aò\x0004Ooå ¾ãù|ov8ÿ¯³½Ç¯ç§¯Î×Yë\x0015 ÖÒ$­2BãXn[EMEppº	TðdÊØ4©Á)\x0014\x0013b\x0018\x0001¤Â\x0008XB®È²(p;\x0011`*Ò\x0014ÅXëHK\x00081?}\x0018#i85zX`´\x0010÷p,^B\x0019â35\x0016 PàÁ@FXÞ\x0015~ªÜ\x001aªT¨ø~L)G½ ¨ìi\x0019QNµ\x0012ÿMéQè0\x001d\x0010¥£n6XEÕ\x0017¨©6s\x001a'gJ!ºf8K¢ÍÚó§h\x001d\x001eDV¨Dv[¾Zó/	æ\x0004Î´fe£ÖH\x0005W ®JÊ\x0010á\x0003Ì#IT\Sï´òÔm\x0007;{ªoQ¹tO_ls¤hF}¨à\x001f
@'B\x001dÄd"éQº
Ú\x0008zÓæ\x0000,èT1
"&³Ó£t\x0011ÓªóÝ\x001d­"kák+\x001d&@Ä&æçéQHã\x000cñFD
 ´\x0011Sy¿Ö=C\x0019"NªØh]i.\x0017\x0008¤\x0014§@ÄHzEE©8\x0014"§&1øOl¹UØuC/Þ\Ü%	\x0001<¨(ZDb_,no×ß\x0017#£\x0016NÕ¿v2O´FQ÷µ;\x0019Â×\x0017³ÓÓu÷Ä+&sÔÅx&ox\x001e(2iò"ëèðSÜ©QÞ\x0019Éç¹ö=\x0005YÜ¬Lk7Âx&ÔÖã¢#Z`²¼94
SXëmG35s\x0002Æ35ó\x000b\x000céP \x0013ËqÍ\x000cÈ\x0012&LÁú0I	Å3b4x\x0005ÉBId\x0000l°»O\x00185\x0004SÀä\x001b\x0001td2\x00137«Û vßwhøBÁ:I\x0010\x0001$ÍcxV|ðqw$LeFWd)\x001dZ@¨q\x0002¿:¿»yê\x001e\x0019Æ@)KóÅáÌ\x001a¨\x001a\x0019<SÇ:·;Ôªh$¦\x0003V$\x0010gÜ
híÁ`\x000bÏ»·×\x000f¾Ó\x0019
8ûWËÏËëû½ýÅÛÅ56bmT)ÓC\x0008m9Ï\x0004pÍ$\x0002©×Z©ýÃy\x001aÆ²?{1;ÂRÏuYî\x0016§ÄÌ\x001aNeøx¥^M®D4rí*VpâAÈºªõLiÄé|sn^¶K#]§ãº«ZOÉÑ­ ×ÓðA\x000b\x0015\x0013r&\x0018]Ã	¶,\x000cÖ\x0010¦¶<OTÇµác\x0005&NZuÛH4³Pê¬³åC¡³am\x0000RÎ)E.ñª\x0001\x0015\x0007-\x001b©Y3iÔ­õµ\x0015{KÏSpÿ_\x0002»1Mðä×\x001bñ\x001aÐF·¯j=Ó`É1-g3ïvBJ%RóuÕr*\x0012\x0003Ìyû¼3µgÙ
P,VOªíN3¶Q,òçÉ3\x001d^sM\x0007'ô¨xïç¡Î\x000eeûd3>©NÅ©ðØ¡lýèÔi$½JWJ¹²ÊóLkçwÿD½ûøWÒîÄ8£¢t½{sù}c
#6\x0013\x0010u\
Ïk6z\x001a\x000e²&:JwÖû§Ç\x0007ÿµ\x0015\x000c£\x0003)ËÈ<Â§è°¶()¶1®õEd\x0018J­\x000cÍ·gLöSX-7{3?<îí\x001f¿~}~Ô\x0019 QHØI\x0010#\x0018<ÐÜO«©Q\x001ew<Îõé½"2Ì2²×\x0007¬9²hÅ­ñ^ìòVß..¢Mo\x0015]ZáÆ÷Wô\x0010ÒªÑ\x0014p\x0000i\x0006µ(Ó\x000cÝpr\x0001¶½ù«Ãµê\x0007-¶Þ\x00177M\x000b\x001a\D®©DPkÉëfÖ\x001b¼\x0012¶¥l;;á¯\x0004°96Æf}Ì]ÄdWÊ\x0006ß\x001b-\x001bW`ÞL6Ë¶ñs\x001bÖÎ+EÃL\x0019\x0011\x001cEM[3Îõ÷~%lMud\x0011[`­od£c©¶Í ^³>P-aC
\x0017\x0013\x000bÙâdcÚ¦¯Ñd³M×\x0006S%l|ãX6\x001bYø\x0003{
\x0015­óÍ|l±>éXÂU7¥ßmBeO}ìHÆ£©Õ4o\x0014ø]ñªyjËÂÉMäXÙãuÅ\x0004lôÚh§ày¬+¾Qö¤\x001c¹ût'ÿû÷ÎÞìý:ÛÿÇù¼Qº¿?]ïgÞç/¯.©iýb±¡Ö&
o¸=
¶sÊì:`µowþúàðzÖ_ÎÖÕÚ¬\x0008ÛU\x000e\x0005QqÂÃäÆDHÓxÐñ£îêÏÇç§{³½ÙÁÑN­VBJÃî\x0002¢aï\x0015¬\x000c\x0006')\x0000I3`^\x001f\x001d\x001c\x001fí¶\x0008ñ<=ÊPqÚn\x001d}3jl2\x001e~}f¦\x00103ÛéQH¨es+ä\x0004õ1B\À7\x000bN­/É(DTøñ¤G!"Æït!\x0003²¥ÐÅ°Kpr}IF1b£m]¸\x0006­¦Ì+MHÖºyÑë\x0013¯ÅØm'bù"ò(bX8¶V¸omdZ
fîp\x0019]	 ÍÛ\x0001@E¹\x0002m
oj±þ«\x00140¨ªü\x001d\x001bM=àZ"_.é&?d£\x000c\x0011\x0003Þô(D´+à´Ö\x001c@lF¯¯O\x0014"b2,=
\x0011ÄY\x0004ùÎÓX\x0002øO|GaÚñKÔï¿ù»Ô\x0014^ß·\x000f¾?ã\x000cËMý½°¦û:
\x0011n\x0008´,\Víý&\x000e:ý½Íñ·ù³mó\x001a£\x0010SEÎ÷«g	¹ØrKÞ`4\x001e:<eñ\x000cuªàÿ'M\x0011ø\x0008Ù\x0014ê
Wyex($¨U1ç\x0004v¦ 8ÖHÓh'Â3IL¢\x0014Ï­*G`!)©¯YïßI·1Pt\x0013e)×4¦\x0019¿¸UaK33~ªÅÃÃDÐÅtoDtë\x0013
øbqKâj,Lµâ²Üº\x0004.éÃ+0\x001a¥R%ë7<·ò]ûróîâÖÜîõârs!â¹83Ú4\x0019¢-p¯g\x0007ë¢Vh¨Æ-]\x0019[8NNo\x000eU04A¦@ku\x0000FSM6!\x0006\x000eñIº;%a6&¶ «&J4³lqÖQùuñîëÃæ
)ébØ\x0004M
ÍXÒ\x001c8×\x0003YCOÊ[áZ~l4\x001cH~(­i\x000eGM²c}±N\x0019]3Ö³Îp\x001d8vQµâÚ[¯Ö9
áZ	Óñpß+X<çøÖß«Z\x001fÍ\x0017Â\x0005,\x000b.ýèÔ³UH\x00157\V\x0006ñ1ÇÈ£áâN\x0013ã\x0005W}+É$ÉvO\x0002×ºu\x0019¿r¶ñ\x000eN4K'YÞçA:SÐa¡²/]:Ç5øb[!7"\x0001XH×êr\x001aO'ø\x0004l"p
5'§z±x\x0013nJ\x000eEn(¯ý%äöuã¿Ò0¿)èÚ9çÑtF,Xºlî_Ìê"r¢Ï\x000ecW\x0017Ké\x0002_ÎUQ¶«äDK×8GÃ9\x001e\x001f\x0015¯÷¢©ÄP\x0013­\x001c\x001eJb©\x000bs¦¹T£&8J¬
ZÖFëcè\x0016?|\x0006ç¹ê\x0004ëgØyz±±ç\x000fv)·«¹Èr6&ð@.kÄXý\x000cûN_®í'hèÚõ£é0^"8¾P°,º\x001f¬^¤(bë\x0015îÃFXñ|°Öq\x000eE­ß\x0013exøReéÕÂqDtgj­æ*l±><)Ã[	\x0014\x0015}x®iåäêSÖ 	&l¼\x001cODH¢,ß\x0016Ú\x000f}Sj\x001c¸fÊ¸-g°p
¿9Uúá)°qäd¥wÜ\x0006Ñ\x0000}xfSv\x0011\x001eî¯ô(Ãó|ÁI¨<üÚF¼ZoËN¥C»\x001eEt\x0010z\x001aê4ï\x0008\x000c\x000fÁ\x0004c¼­ªf4\x001efà/Åó4\x0006ÉI\Gj1iª	Ìú{ 2:Ì9)_º- 4¦F¡\x0014%\x0013]\x0003'¶å<ÇÒ­®ÐÅ\x000bÔÀ\x0017=©Wâ\x001csÉÍ¤f\x0007<ô'RRG>_ýÆóUK\x0013OÅP:ó)àû²¸¾y¸[þt±üiy{}sý\x001c'ã\¡¼áoÜ=Çái(¥õÜÀy<ºTü\x0000'³£ãó³ùO/ç?íÏO¸Ù"È¸¼~ws}ý°l~ÑGUmTõôPå\x001fW½XÐº>_}/n®\x0017Ó\x001bm3¤\x0004Èëÿó¿?Þ<\¥W\x000e§\x001e\x0014ÎÀ°ÔyÍ~hkÀè(ºQ\x0013OpGçó_Ï\x000fýâøhözv6j¥1
Î¯i\x001e§ó\x0016cå\x000ce%\x001dÑPÈï
îÂ¥
"KÝÀR	Y´T¤G
KÄCw£êd;G.ÉÇYX+\x0008D¦²xÝ×*×
çýRùÜT\x0006ó±Ê6o\x0010O\x0001»QunÅÆQiC&¤"If ÒT¹\x0012ÒzGª^íñ8,aóØDÀB[A{0R!Ð±n\x000bþýI.ÿúØ2\x000cû\x001fqùònïlyùþzùp»\x0005ÍFò\x0008ÎãÆJ8³RÍ°ØýÐaÛÿeþ\x001aÇÏÏöÎæ\x0007¯æç§£\x0008Qe»\x0010ûC"\x000cà¾Ò]´*Ðø\x000cÛ¦§ Ì{³P6k\x0018p³ªLH$0ÕT\x0013ê¸¼h½åC¼½~øüþ÷û-\x001f\x001e¼F:Y»è\x001cµãÅN\x0016$Sé©
vWÖç¯ç¯6|u-lø\x000eO¶ùO'óO'áO'û§Ã=Î¿G|ñ\x000f?
÷îöö?,>Ù\x0016Ã([p ØÃù\x0004ÙG6çZi7äjÎöö½>\x0019\x0005Õö\x000cT;Ú\x001b\x000f¥5AÉ,ý¨\x000cSÉÁh¯ª\x001dí¤ò*·?8ì&Èõè\x0010*X*ÞS)~\x0014;QIì<\x0014åår\x00107´ºy\x001cÁH3\x0018X`ulþÍX\x000f\x001f?/>ÇG.8eÿv¹¼}¿ÜÂ¥E.¨
g¹êü\x0016\x0005]ß¡\x0014§\x001dâÂ\x0013öo\x0007óÓWó1dc×X2¡\x000cgTIZ1î)\x0010&µÞïJÖ9{$³ò:x&yR')>Qà9lg²ì\x000bÉ¼Ì²Gøù\P	dÐZúá³N\x0011Y¿\x000ef\x001cÏ.
&ÑÈ\x0002ÿI+eW²Îép4Îy0\x001c\x0013kMjV`ÇâðYº¬_79,æªD|pFÌ`OÓx½3W¿qv\x0014Wp}°zõýÆKÚ)¾2\x001c±ú$É\x001e÷ô>\x001d4¼\*·gÿ#ïÓüñöò\x000em\x001aþ¯B@Ö#Cã{¸O\x0019¯Ý¡ßÿ¼¸ùøWûxsyw;Ý¯À·¿¹y¸½^ÞÝ\m¯Ñ¨å½\x001aQCYäøÚ°}S:I\x0001v\x0002ìc=Ï­îàçß\x001c\x001eÍÏ\x000f×ûú\x0016-×þChé4WKëÌ3ï2­vY)O¢T&Z+úõ´ÛwË/\x001bPé ÷\x001f²°t\x000cü\x000f¡ÍÎ¦6Ò\x0014\x000e E¡´\x000cKx`í\x0007Ðõ\x001f\x0001;ê?X\x0019EÝÛ«$6\x0011ðaÛj5\x0019+\x001dFþC¾\x0001®¹ýOÁÅ,»®ÿ	Ü\x000f×W_Þµ@xr»¸Xn;Zr\x000fH'\x0015uFÀáO\x0004·ôQõ¿S :9Á¹t\x000c
'9\x0006
Y§AÓ'ÃVäàP\x001cûTpØh=\x0011\x001c6JO\x0004:<þ­8w\x001f?½óß;òbïÍâvy\x0013Ý¶eHõ\x0003\x0017¨qD¹	\x001e7!µ½Ü\x0004Î,ÎpjÛówÅÝýí²ù\x0005!{yý¡m\x0017{§Ï7×\x0017[tT::\x0005\x001cðF.YÃø\x0008ètöúøè%ðä!=9u)¥h\x0015»äßhçë½ÁeººÚòê4Vnæ\x001bþ\x0018"ÍlN:ÒIS&Ä5ùñ_q±\x000e\x000f7¼ÂRµ)U\x0005%xÚÔKFÍ\x001c@)¨gM\x0019\x001f\x0006ë\x0010Ê(MÒTPjg¦\x0017«u%jûk^K·&^BiÛ¶2~\x0005PB,æK\x0000e×²¿7j(]ÒUP\x001aÎÁZ:,qJV4ßåäz	dhCÍãs+%B
,\L^ùæ³àÇ6e,§ÔNç^c \x0014:÷¤H§"¸+#Ó¡ERt\x000c¨Ä¤À\x001a>Qá\x0019\x0003ëØ¯d¨ÁìX"Yc¢ÉÍ½°NçÁsÉcüqj\x0002S¤þXtMæ¢\x001cÔªg^{tYÁ	wæóS.\x0000]\x0008c:þg0²{¬ÊéÀ\x000eÒL\x000b\x000e2ðÝ\x0010üª§4ºìõÇª\x0019lüåVjÕ¦V»PKj2\x0010Æ<ã\x0014¨µgê\x0014hNE­ÛÔz\x0007jt¡1SÏO@íhÈ\x0016Úé¨MÚü§¬µmSÛjj\x00085y^ª°\x0010Ädoë¥ [b-\x001e\x0005¢;@»6´ûOYjß¦ö;,5\x0018<¡óR«Ð,µ¨]?HÜ:´©Ã.k­¨íQ\x0018\x0017)k­\x001aç|LF\x001dÛÔqµn&Å
«c\x0016ÑµöÔ«ß\x0005+¤nbìdÄ\x000eØRS×Uþ°
íFµú°ûÇ°\x001d°»¾±Þ9\x001aTvà/\x001bum\x0012µÂ©£Ø|.¥îøÆ~\x001eºÌô)$\x0013ØÐf>ÂbKÍû±_Ý»\x000buÇ7Êzçh\x0004NÑ\x0014Æ9 @dÃ­D)vÇ9ö³èEØ:P§¨@¡|Aá¥n\x0016;õ:MÝñýlz\x0019¶CÇa\x001fY?©Ié
°ûGæ]°;þQÖ;Hp5:­ÀÕ\x0008:«ñlþð#é¸\x001aYïkÀjK\x0000`DÑj\x001b6¶ß¢°\x0003¶êXmµÕÆ¬¼Ú2iy\x0001uðüôk³vî\x000cv°~RH3#°\x0004Ãå
	\x001dä£è\x000eÔ\x001d·®êý:±\x0003ScËÉ¡ÈÍú¸\x001f§[lÝqzÓc\x00144^X Ê³Íð±\x000e[ÈT÷Ò9÷âoTÃC$biÍ±¾<#\x000cü¤îè«b\x001f\x001e>èQ5A7Iþbx<\x001e&Ç\x0015\x0006oÆqlw7×
¿Ñ©M¿ùú°¼º|ws¿%%"UäÜMÄ1c¹,*FNÐæé¿%»Çÿ8\x001f\x001eì\x001f¿Ù¼aNÕæT5ZæÙOÀ)\x0003ðºtèÈi\x0016ÎÎºÍ©Ë9U½7fè©\x0004:Ð¼KåýÚ
è\x0012LÓÆ4U¯Ä\x000c`9¥\x001d¼vÃ¯]uÕö%¶Íik8yÄ)rúgùÒ*\x0006Ëo]\x000f·\x0016bº6¦«ÜEt\x0019\x0013Çq@y9=%\x0016­µëZ*J8}ÓW-g ¢nøN=Öåõ¤"CeÍpQw!ghs\x001aNA"/\x000e-\x0011\x0017RGGÊºávÖBÎØæ\x0015ÂÛg´ÀÇê|É\x000bæv»MÓm·an´ð«KdáE
d4Ù$eJª|"\x0001¤àã\x001d\x0013/kl<¦\x0005*.ìME\x0013~Í5\\x0011hÇÆË
#±\x0013\x0010.ÐØ\x0006>\x0010+§ûå\x000bA;V^ÖyaXÝ\x000cå\x0014\x0005â¤¡7*éÃîÎÙ±ò²ÂÌ×44\x000f
þ\x001d
UÅ²×ôüæÓ(ÂÝ6RÇÈË\x001a+/\x0014Ébâ0Cºq·8k û1iÕbvl¼¬0ò)\x0004IJàX\x0010ÉÉ]^
KL\x0014v¼¬±ò\x0002§å¯SJ'2\x0000¨ÑäPl\x0002Ð\x0015f>­h\x001el%pR0õ&\x00060¨NM\x0010¨©WU¦^ðD:tLvHAsXµQw\x0006íFóU¦^¨¬W\x0001 xP¥½¤-¯¨µS¼zÝ:Ù±¹_ufðb\x001cs"¤ÑN×\x0006þTíº:"^÷×Uò@\x001a~8µ\x0007Ñ\x0013o¤ò3°\x0000ýLóx*C¿Î*ÚÅ
9-ls\x0004	8ë: 4]ÆKß\x000bKZ2
[
å\x001aFÕfTå(\x0018DÊsÑ\x001cª­\x0011c¿;­\x0002Ñ´\x0011M)¢\x0018)å\x0006\x0000c=\x001aì?¤2|©v_F×ftå`4E.
B}!í§g+\x0005oZîÌ\x0018Ú¡1`ûU^G\x001cÖ­3#¶åæÍØ@Ê\x0011[\x0005A!Çò¨l\x001b÷1r\x0004\x0002gK2ïBô/F+ ;[F\x0016ï\x0019\x0015p g>nÀ¯ùé¬äÔýF¶
HÝÔåppS9¤}àt4ÿ\x0014ø8¿3dggËâ­ý?a}V±{b´\x0015Û&<Ë]k\x001aÎ\x001a¹\x000ev
\x001dÙd\x000cýç
Fßaô\x0015ô¢\x0003bç!HgÖ\x000b\x0002mM×õJ$o8û¶¼ÎÒu§7\x000fËÛ÷\x000f[ê³!$ý;H(ÚÛÝ¡Q½ý6?Êzu§ÇçóÓWçëÅ¨Úª\x0006Ñæ
\x0007ôØ|\x000f\x000c3²_8¸u!MÒS\x0006\x001csMcu'\x0002TÙ?¦Õ@Ú6¤­\x000cIÉ3Q¢\x00004QF>\x001bíåî®MéÊ)#\x0001R9ìnÒ\x0005/«·uÜ\x001dÒ·!}\x0005¤¢¬\x0011\x0016uZªq\x0000Èð\x000bÇ´ÌÎ¡M\x0019*(QÒ<\x0014\x000bÍ5²xêÝ2¶)c\x0005¥TÜÓ\x001cLòDL4B;C®¢ d)E1%Öñ¥@PDòm\x001a4Lÿ[Ù5è\x0015\x0016\x001dëw\x0005õXMÊ\x0016>J¶¶/\x0014YCÙ±é²Ü¨k¡MNÂ ¥ \x0004¡h¾Ê°»±\\x0005kQW¬d£\x0004
6+Ò\x0003¦TiõîÖRv\x001c,÷<°Ãó`,\x001bõàW»ÇÝ1;®Gû\x001e-1*ç\x0016
OòN¸Àn-j0;¾G;\x001f,\x0018b?
YtC)5S¢&æÎ\x001dç#Ë½\x0016*àu_Æ´,¼\x001a¸Ì\x0002{\x001f&Àìx\x001fYî~´À¹\x0004+Lº4²éÐb\x0003u¼,w?é^E3¥ÇX3\x001fx\x0018²\x001f¦W@ª÷Q\x0015Þ\x00073w)R\x0018´¸q¯Ru\*w=°wDÓvçLCÞ<ÍÉÑù	²{¨ð=\x0012%$TóUÆ,\x001c 4_øÁ\x001bßý³T\x001d÷£ÊÝÆ¯àÕ4THc[yO\x0010««÷Q\x0015Þ\x0007ç>PÇq\x0008,âíÄ*X\x000fSl÷Q5ÞG¦\x0007Ës!Â2¾_xRCÙq>ªÂù¨U`
\x0010t¤!¬¬\x0014»ªã}T÷5,fd1æèb³v÷Cu¼ªð>
\x000e?:ÇQqGhä\x0013Ù/Ã®aìø\x001eUá{pü\x001c;r,»¦*	\x001f\x001eà¾>X\x0005¦îx\x001f]á}÷l2£Ã\x001aµ*æ»ìßíÖPvü®ð?\x0012oÊi\x0007¦\x00047\x0019\x001bÙïí¯Áìø\x001f]áÒ´&GIÓA°ïM¦ý2£\x001aÌÿÑ\x0015þGªe7xÛCÕelØû\x001a´5\x001dÿ£+ü\x000fÒò\x001cXXL­¹BSIÁ5pê¤k0;þG×ø\x001f³Jb\x0006ns\x0010¼ÚÆMîNÙ1ìºÆ°»FR	5(ri\x0013Æs6xýÓ±ºÆfz·RÊ S\x0013Í¥¸éoT@Å4\x0015\x0016SËÈ\x0001G\x0004,Oße\x0013½Y=ABØtL¦©1!òT\x0014ZÃ |ã\x0004¡\x0015}9µ\x001aÌÉ4\x0015&SëÈ½þX¤OþG9Å«i&8LÇd
C³<o\x000f\x0016RÚf1w\x000f9LÇ\x0014
S¤B\x001a8-fÌ³Ñý4¯\Ë	0;±°©5NÒä¢áH­Ï\x000ek¸¸ywÈÁ4\x0015\x0006SEÉá[4\x001a«µ²\x0006\x0005x­î\x0017\x0014Õ`v"aS\x0011	k\x001cJÆÈ)ºµä\x001dGöìÙ1ì¦Â°kîÔÂÕ\x000ct\x0006¾ÜpÝýî>Òv\x000c»­1ì®QíX9lH\x001d¥i	±ýæ\x001aÌa·\x0015\x001d§n\x0006Þ>JÝÀ^r"Ó	Î?¶cØma÷\x0012Ù\x0012&þ2ØÝÆ%÷r÷/Óv\x000c»­0ì`\x0012©U\x0007C¾G\x0003on¸3`øÍva[\x0011\x000cëÜµWÓS\x0002ÎAXÇß¦âÛìÞBWx °\x0007réR-­¦m^ºí\x000fsªÁìx [ãp\x0016\x0001ít8\x0000nO3\x0007[a)Ùî\x001d\x001fd+|Æz\x001d²^pÐ®gL·;dÇ\x0003Ù
\x000fd`\x0003ÑM\x00005gFmù0ÅÂ»Sv\x001c­q@¶©ÆÃý#É\x00015]n÷¥t\x001d\x0007ä*\x001cÑ&ßé{ü×±\x000e\x0003\x0013\¤¹\x0003r5\x000e\x0008#o\x001eÅ\x0007\x000b\x0015-[L/&XÌÿq\x0015þÇh|y1\x0003ÝýÀbr\x0019v÷óëø\x001fWã¼æ«è\x0018\x001c\x0007pXoÍ«Ùoð¬Áìø\x001fWápä½¡Æ\x001fÉcF±Fr+Õ\x0004ùk×ñ?®ÆÿøÀµ;1@äÉMJ>Mú¾ìV
f·\x000cªÂÿ\x0018,¡çÆ4\x0008:³ÿ1\x0005îÜ£Ù\x000c5\x001dÿãjü\x000f\x0004\x001dÜÔ\x001b9A\x0007°,sgÌ\x0007r5\x001e\x0008o*òbjA\x000eÈèf-å\x0004çI×q@®Æ\x0001á¸\x0010^Kõ¬b\x0019&¨tô\x001d\x0007ä+\x001cUÍ\x0005\x001e-Hx=røæ\x001e©ÖÕ`v\x001c¯q@±©¿MT\x0016³	9&Þ|Ç\x0001ù
\x0007dEÌe1ØÔéH±Ù\x0019Ï\x000eÈéþ\x0000\x001aÌ\x0003ò\x0015\x000eÈÀÑÜSg\x0010~Í±ðªçØï~ô\x001d\x0007ä+\x001c\x0010ªÒ(rçVQ-3\Ë\x0001\x0011ç\x0004ï¼ã|ÿ1F±R\x0007\x001avC\x0011\ä;\x000b0ì»ÇF¾ã|ÿ±:<S¹£\x0013«¢(m%)*7E!®ï\x0016âVø\x001fcÁ÷
»\x0014+Ã>Áþéx\x001f_á} Üm>L>²´²¢¬ÌwÜ¯p?¨4$i-áT©È\x0018\x0019Áñr»ïòÐq@¡Â\x0001á\öH\x0019yD;,¡ç\x000fÓOP\x001a\x0013:\x000e(T8 +[íå\x0005yL\x0013\x000c~³O
eÇ\x0001
\x0007äÐd&H)\x0015'ù6À\x0005½{Ì\x0011:þ'Tø\x001fÔ¶4äà,E¼À\x0016I9l¿\x0007­\x0006³cÙCe·Öbu^nØÔ«â¬üeº¾¬e
fÇ²
ËîÜª\x000fZy*¸w\x000e\x0016ú Å\x0004=t,{¨°ìpr`\x0005H\x0014ÞÌú6ÎºÆOú	2\x001d¡ÛcQaÛqúaå\x0003ýÌæØÈ³lòjVÐ1î¡Â¸;\x0008áè\x000bKâfÎ6/Ü#=
ÊØ±í±Â¶\x0007-ó	È\x000bâ@§Éà9½{ü\x0016;=V\x0018v'\x001añZ´´Q®Vr÷÷\x001d;&3VL8ø<S6¹¡Ö>3YxÝ7yìì±"dGý7\x0012ÝKQ\x000e9\x0019\x0013Ì\x0004\x0015p±cÙcewXPF«i!ï®¹öój
ÒØ±ì±Â²G<C&J-9\x0017\x0003\x000bË!{x$vYCÙ1ì±Â°£Å$Ñj,9d0y)Í\x0004YÂØmJ«°\x001eµÿr)Á\x0011Ñõç\x0004¶·»'°¥èu¥U\x0018LÌ®»ì}ÀcÒ¬x/\x001cOë\x0008q÷ö\x001fÙë3\x0016\x0015FÓ»F¨\âÅZ¶>4^Òíî%¥è6}
³é1nË9l\x0005[Hfo\x001eØÝ«xd·750\x0017;JÑ(Òx;8\x0002³Ôò·3g·SITìõäÐ3&péÀþ¼Px4j¾\x0006³Û\x0003$*v{@£·²\x000e=Râ\ \x0019ÔîSö»;+¶\x0011¬\óÚýÊ]rãWx$sQÙÝE\x0015½:jØâä\x001c	E§s ¹¡Ý\x000fè²×XÓ
ËØv*º¯_³´@»WÈ^·_M»\x001fÚx7\x0011Å)Í6>cÆ	<Q¯®¦\x000eµuþ4QËÆ'bQsÀ¢o¿­Uò\Iªª¸îÕ\x0006î
Áa\÷Ú(	®\x0000a\x0011û°¸®5¸ÿ\x0013K\x001bM6:X£ò06Å;u
Be\x0013LÐn\x001f­¬­bE1@n²sfÙ`,w9<\x0012â¯jeêÓ·®¡U8®´p&µ­Úp&ÐIxÄ*ëXQ¬2òÊº¦}ÃgãvO1ÉÇÖ\x0000C\x001aÚ`ib$ºÿÀi(¸À<¨Ý³#àï\x001fÛ\x0003Y·Å°ð¢h¸R6ºÈ[Ìî~hÆÕ½_ÞöW\x0017«xuFñÂë\x0019±)\x0011\x0008z
×ðÈ~U/å½oë
\x0005;kÊ¾aU\x0019X\x001fÖª/\x0001\x0002ýg«{Y*þ\x0003öê^v\x001bÏG6Á×Ù\x0004\x001blÐ
Í$Dëø\x0016Ù¹	ú\x0008á;è}¶¦ê£\x0018iÑw\x0000\x0004u«FýÃOP@í\x001e­¬«[Y\x0003ÖoîÒ+]5Ùæªv
ù)ÿhùº\x0000Á§U\Ø$T´f?6Íý·~D«ëVèæ¶\x001eÏÜ´ÅL£c>A \x001e}\x0007UÂ1\x0000ÔufD©Q\x001dúª¥jnñÑæu»+zÅ\x0005%ÊfPÕ|DÔ#D6¡Jùè\x0003²î\x000b\x0008àbIß\x0018O³25F¾-#ùö/`\x0010u\x0001\x0016 #ã7KêiÏ»3`\x001eö^Ü<ü}wwó°-#¤s+,ÆÚI
3¥0\x000cÇ0^õoO:\x0003`Î÷^\x001cÿóììø|íçÚðª6o6ÓX^Æ`
¶I
IÎexÛ\x000b©æÕmÞþLºÑëM |¡\x0012ør7X\x000eº¼èWGTó6o\x0018ÝèõÅBÕ\x0005]í\x0007v|,È^kÛ¸ý!t£Wë,×·j[)\x000c¡?g¼Öµiû³çÆo6ÁâìÒH®Â\x000få¬¼×·yûcYGóÚæ6\x0003kf\sÀáõõ}ÑjÞÐæí\x000fÉ\x001b¿ÙôªDÁrÅ{°Íõè\x001fÈjy[CMñÓèÇ\x001b
\x000c&ÁæR­çáîÀ>Ñ\x0002Ëõ}4\x0018tü~\x0013<¨Rxw\x000bÀ,6ã\x001eiU\x0003wÌÙ£á£|F²!p=olÏß8Æt\x0004/¬lOUW¢pWGù\x0017¨F(ÿjÏc¢ò4\x0014þ¥\x0015q:1üîfubÕSÕEDUèi-2\x001aÒ ±.pu´\x0014ý²ã
FÝfÔå¹!'1z:ÓÀÑ,%6|íhÚ¦\x001cQ»êDDÅg©\x0000\x0018û\x0017\x001d\x0015¶Íh\x0019áÃ{F¢¿Ø»÷5Í¸¨ÔìµqM m{ï\x0019~£=¾î·Ë«åýý6Áq,â¢9\x0008±\x000c´ù&óq×\x0010OøíàøpþæÍF¡lÛ×w¶Ùuc\x0019aå(¶Æ¦;Ëq,Fðè
¦\x0002Ñµ\x0011]9¢ñ,°\x0019£f]\x00078øpÃCÿf°\x00021´\x0011C9"D¤W1Ðð
\x0007û³U±¯CPÁØ=ö¥/²=Ìd$*J±)òÒÒ<\x0001L£p®=Æ­Ë¹f2é9¤6³ÚÖã#:ËsË¤U\¨\x0010Eh{ý\x0008÷õ\x0018WÈªM©Ê)=S\x000cç=ÅU\x0019MÑ\x0000åæÔmD]±Þq\x0005D¡~:Þëf^Yì7WÖ,¤iSt$5_7×ÏDÑ\x001cçú\x001d8Å\x000biÛ¶\x001c\x0011Kù\x0014Eh"ò3úf!E¿t¦f!]ÒÕ|\x0010FæN@	GNåøä}#û¶¼x!}\x001bÑW|.f\x0005ü\ø\x0005\x0016\x001d\x0018Çæ°fw}×¡\x0018*V16Ó¥´\\x000fÊOxÓ¬n1\x0016±5\x0012
¤¨XF\x0004Iyt\x001e\x001d\x0018\x000cË\x0001ºþ\x001dY1aÇ8Ê
ë\x0018p+Ê\x001dUùÕ´¬þMy1`ÇèÈ
«CAn\x000e\x000f]Mßì#	çñ±ïabò0'Ww)9ûóÍåíâòj6\x0016ÏÚ¹eÉ?\x000by\x0011¥iò\x001a*ôvóÉál?åf>>8\x001d\x001cnÁ3m<S\x0007Á"ßx9Û(êEÍxf\x001b<Â[o\x0010cß Æd\x0010\x000b	yFê!Ñpc§\x0004ÏÒô\x001co[¿õ\x0007~\x000c!Mg\x000c÷áåÕb[\x0018æm#	â,<*\x001b\x0015°~\x000ea\x0007³M«¾7¦\x0013ta[ÍºoiG(!Xx\x0005ßò.l¡Í\x0016Ø´°Y0\x0002¯Øb#X´\x001aj+ûû¶­5Ts	\x001coÒ
|ù§X­Æ©uqõÈESíð?píðÌ{
ú\x0019«\x0013IT­Éúx|ßgåÓh\x0006\3½0ö3K±YÚ»Zì.>ß\_\n»9Sk?P½DS\x0015Y(uÁÁ\x001có{§³×ÇG/\x000f6ÜI\x0012ëJÜ\x0018Y1J¯Miç\x001cÉ%aXð\x001f9$ÔRög\x0016\x0017Â~ÊNäÝÁç/»»üÎ_\-\x001fÛfWÂ¾Íièé\x0004§CEà"KðÆ=K}ðúdvvßýÃùù|ã¬Í~NLäX\x0005§mº²³*sö(\x0016s¶g.â®o³]²ÙmÎ×ßÜa\x0002w3¨\x0008scxªHrÝ4³B_\x0017¤
úúÇg¾Ý°¢¶ÿæmzóÍÔÒ\x000fÏ_îö~ÂõÍâvyýõaË×
gþ4\x0005\x001a½Ï\x0006\x0011\x0019A£T^?ÈöÙë³=üfßÌNçGÿ8öÝâbqw»l~ÑGWmtµ\x0013º<È
\x001bSxµ¶´Ñ°7dÝìú*tÛF·»­zt¨Áè\x0006Çç¬& /\x0018¢u~´
½u®°]×UÃn\x0004M¹÷hiÊ½Ùý:?[ÇÞùbän\x000c\x00187\x001a\x000eæ
Væ
çcb·}ÁÍ:v%{\x001bUÉþ­ÊÙòòýõòáöî§/ÞRM´ó\x000eÇxäÏF\x000b*}ÓÀÐÄÏÄ6?xu4??=+ü	Lû'0\x0013ü\x0004òÈ?AP\¼\x0007?\x0001\x0005ÂÉ¡Û~\x0002Ûþ	ìî?$§	?f){«L\x000cô\x0013è¾bQÕO Ý\x001f?ÜýÅÝÀgMrùy¸Ü;YÞ\x0011¥ÉÊzðöyø²¸3\x0010"\x0006\x0011mRø*1*ÞF\x0013\x0015^ÚÜDþËùÉì\x0014N6Ï\x000fç{'ó³Ä2èzå6\Ý¼¿ï²ü|s}ÿyñp»\x001eÅ\x0007<Á¤Ó>Î\x0019¢¹\x0019^\x001b{¡\p1\x0015p7(?\x001f\x001f½y=;?]¿*]ß±]hß°ÂûüùáóâbÃ2Iíri&,¤×ç¡9.^\x001a):lí»Ux?¿½\·báoßÂ;²\x0002+'½wõÿûÍntq½¸\x0007.\x001b"!9\¼»½¹üþÓÅííòGZ?)¬¥W\x0019p\x0000lR÷qÚPÁOn²öO\x000fþë§\x0017³ÓÓùïd´ö\x000e÷f§<;½\x0019	ß®Ã/.¥g\x00013
ð	©´-M\x0008µ\x00193\x0006ªk\x0000\x0013©]M\x0015RÄBçy©jÈ\x0011&\x000b\x0019O	?¯­]M¬\x0005Êp.K	\x0000I¼}\x0003ü\x0014QÂñßÕRb~\x0016Ó@cJ\x0011\x0010¥ EÛ	(á¼ä+)Ë`ôr\x0011>ÊôåíÀ\x0018© y\x0002F×Bõîq©9½ð\x0007z¤
Kzº¥/'Ö.¥v¼ÉPù\x0018\x0006«©5½qÉRc»cbº
SK\x0013£Ò¼RÒ@Cý²¦ ,§¥\x0004ä\x0004hÚ+m»\x0008*5\x0007§õ×îók¿Mÿ?wg]Émäù­ðm\x0007\x0008|\x001f=Ý¢h}XÅ:¬¢ÎØ/>WUDUYEÙòS¿Î\x0012z\x0007ÓëðNz%\x0000"@2ï½Ì[jy¦G´DËÒ/ñ\x0011\x0008\x0004"þ\x0001òX³§ãà9w\x000f'w%Ê¤oKIkS\x0006u¬ÁÄ#zá¤KÍGÒ9\x0019Ç<d¬-\x001dÖa
yÿW%ªã\x001c=±\x000f?Ý\x001eFCQ\x0017Oö\\x001a6\x0016OîÌfýÄáNÙÕË×ç³â·A\x0017Q§dp°·ËD<Hd'vr\x0017Qv&:D@"Q<WÈRc#+6S¶¥(û
\x001dDñ_ª\x0008\x0014¯*:/)k²üÃ\x0012\x0003µ\x0012)û\x0008ó¤Ë*<hÙ õ-J£d¥QÂ²¢uHÙ!èYÜ­öLÓRRr©ºòéß3J>5ZÆQÂD0K£D¾D»uDù\x0010íYÜ"Å\x0005\x0013Q±N\x0018\x0018$$¹Ò\x0000ðyÙ$]AÒ27Ë@Ä+Ëf#ÑÓ1oèìÊ¤³4Ôá71­Dû_vÙ\x000003QÈ\x0011ÆHdøÍÚQ\x0013/»l\x0000n8r\x0016¥÷§VÓó4sÑnMø´]Lñ/»v\x001c`^\x0016y2ñ\x001c6d*­¦qfõjÖ\x001fÿÏ¤¼§Û}À÷¤\x001f\x0010G\x0017Ôbí&@ö¸÷=)\x001b@\x0017¢\x0014\x001dÜÔÄ¸($=<q¤^¥´ùe\x0005ÖÚJL¨.O@å\x000c¥ÌäsJÅ\0_\x0016ÓÊs\x00173.¡kÓ)ëÒ»72á-(\x00177õËþAW^å7Ûû»ïSÊ~¯\\x0003¤dÍèðb\x001a¶Jf\x0000¬Ì"ÚÎig'n\x000fßl./^}½+å,\x0002¹\x001fÞÿ¿U@ñßùé\x0010LÊéIW\x0004o\x0004ÐèÄ-ÉÁ5ÒMXîø\x001f;ºp`ÀV\x0011túE¢=|{ûñóÃÓß\x000fß±\îªñU3)ý¦;V	LÅ?ßu/¸9ùöüÕÛ«ÿ}\x0018\x0012jHèD%Ìhá4{PÒ8\x001a=«§\x000e^DU#ª~DÛ4ã\x0014£2\x000fER¨$8Nñ¤×\x000b©kH½\x0000ÒåðÑ`ä4\x0006\x000c<Ù°+ÚÓÁhjFÓÏf6O¶±]A)\x0002í[Ã9ë« m
i»!Ëý\x0012¤Îå<ø®A>äGØ5®tý#Iå\x0008©eÖ /±F	Ü\x000békHß?*\x0017\x0012GRñÝ?º}§;ì
w@\x001a2,nº® $LhùkvGç\x0013JÑqÑ\x0018oàV¤\x0016tÍ\x0010Ø\x001bu\x0004Èö¬é?l\x001c*;Ð8
G\x001d!Ë\x0014GlÎ\x001aÙØàSWàmcÈC0W¤^¿kdsÚÈþãÆd\x001aó\x0014\x0014 =
ò{)ãFö76î\x001bG"ö\x000e ¡TÍ¤G\x0018ËæÀý'\x000eæk<Ñ ç¤¸©\x0005M¸\x000eá\x0008Í#û\x001c\x001b\x000fÃ\x001c\x000cO\x001b<I\x0010Å±$½¤´Áw=tvP6Gì?s,)ºâXZ\x000eQ %­KmÝ\x0011ÖesæÈþCÇb^\x0002­KTÄÎ\x0013î¯¦ô®w\x000eÈæÌýõ2IKàPblEæ¡$é8,C·\x0012s\x0007úÏ\x001d\x001bï3¬%F\óPjàUy\x0004\x0012ÚÛC¿E7¨JRæbÒ\x0008ªïtýº0÷R6Æ\x0012ú%fþ86C\x0002+KÒ9Ïó½û!©²1CÐo\x000cz¾|­v\x0014\x0016cÉ§£ö°Þ\x000cA³Á¡ 1 ÍÊÊ\x0016Ø³\x0013Ò\x001eÁ¤«fï¨\x0005{'^uLöÙt| ;dç\x001d>\x0015Ðí¥lvZà\x000f)ZÖ e4ùB\x0006ÞeH©õz®Ý£\x0016¸\x001aX	BÖ\x0012\x001b#«\x0001\K­¦"¬½ÍîQ\x000bîÀ\x000c-4Ë!ð3Ór½µTÍÞQ\x000bnd>m\x0018T.ä\x001cíxßqdTÐë7¸n¶îß:\x001e\x0014§}¡øm6JòE\x0002£ÆGpÒ¹l¤rÔKÝHÏÒ´ô(é±M"¯LÅ\x001eXs¡h2Þé\x0017)\x000cøðô9e	m¿{¼»Ç¾1\mØÃ\x000cÁqZU<4§\x0008L½ç^_Ý¼MI\x0002g\x0017×\x0017\x0007x\x0010\x0016jXX\x0006k4\x00077\x0005~¡çÒç\x0008\x000bW\x0005°ºÕË`­?U\x0004ë4§ÕyQÒêÔdòÅ\x0002XSÃE°\x0002\x001e(S\x0004\x000c]Ú45Â«ÁOÞ3\x0016°ÚÕ.\x001bØ`Øêc"m~î\x0007\x0000¿­OÚü\x0005¨®FuPÉU³	5Ða¯!PÎqdtI\x0016Àú\x001aÖ/Å#Tò¸Üe+\x000e¬3a§\x001e\x0007\x0017À\x000eq¯Rx±Ö¤V[~\x000eíºÍ-`mÌ\f·t4\x0005*ãø§´d£8)ÝË\x000cö.U# m<f-Ñ\x001aÇë@ÂT
Þ\x0002ÚÆ\x0018ÈeÖÀÈÀ×ú¹IÙsÁ®É¼\x0010&sÁ\x0017Ð6[L.ÛcØ\x0017\x0010hÕ*\x0012À¡5/\x0004\x001cã\x0005íi»lÙb{3E°¹ío:\x0014\x0004]ó±va\x001d,è\x001f\x0003º~Î|ó9*\x001cr¯Ë\x0002ÀÐ£ Ç\x0004Á!\x0013kÅn·ðÍÛ}Õ
\x0005PÕª\x0013Ð¢G¶«ñðªn)ä\x0008 òÚZÀP\x0003Þ\x0011Än\x00024\x001f\x0008¶<fêÑ|\x001e£\x0019¹äks{K\x0005Ä¿Ûþp1\x001eNi·ä¤#ÃñBÊÙà~*9ssyy~N%Ä¿Û|3\x0003\x0014jPX\x0002ª-Eð´"àÌ`\x0001\x0013¦SÕj\x0001§®£ä
+OÉï\x000fï&\x000fÐ~N]sê¥\x0013OÕ
ô·ÒÄsÊG\x0019P[Ú% ²$êa\x001a¡Ì/¯Þ*y#'\x000e¢~PWº%3/Ù\x001eE\x000f$p®Ó\x000c:\x0015½íÇô5¦_2"pZ/f÷QÁ§ö\x000b]ä±B\x0007g4&±d@\x0003;ÎÑ¨KÊ:RSÙ½ôò\x0018¤¦±MfqRÆS»
sIãV¢$25\x0019\x0013ï\x0007mYf~\x0005PüÔs\x000f¿YRÕÎ½úíN¾6!Å¿üÍÂØ)¡:tr®ï¾Û~¾½?H	¢$6`oCã)SÔ¼P»¦×\x0017/6oÏwh&ÕPCÂ"HÊbñRrÂo$çÓMUÙô2ªQõ3FóN²hÕKMæ·x7PÞ\x000b©kHÝ\x000fé/ÑYç\x001dõ}y¶Ú\x0013"
ijHÓ\x000fw¡<ñôT\S¥Ê@îyMÍèjF×Ï]áò8ÀÌVs:¢s;«O;\x0018CÍ\x0018º\x0019±	$å\x0011;üämÍá{\x0007{áçBÊÖþô\x001b ¥-ßÛL(¡{DK)²ë\x0019­-û÷¶r#\x001e!-\x0017gy|ùÕ{.\x0007)\x001b5-úEó\x0010òúáéÏ\x000f)µÊWKLÔ¦lhï\x001dùÃZL9%Îñúêæß¯f0ªQ-`Ìïr	\x0013\x0001ò\x000cZ3¦Ú\x0017::D	`Fg"ZDéúáÓíÁ÷\x0014%FÀ\x00069Ä(/kFì¬Þ}sr}õf®s\x00085"ô#¤*lVjñÊV*V\x0013ªPu\x0013:AyÆñâãùÆ\x001baB7\x0019ÛîCÔ5¢îFô\x0014	a)ÅÏ»Lã|:SÓnº`ËÍ\x0011aó},X.P;Ýù¶&´½hg,¢\x0001ôÔ\x0012)A
¿Sa6¢«\x0011]7¢\x0014©~·8¥I&\x0015<)Ú-·1Ð×¾PÓ\«©@P:¦ñeB½³f`>a¨	C7!hÊ\x000bJ\x0000\x0007ÐSâKFÉp\x0017bD\x0016[t3*MÏÑÂ°ú\x0016\ò
n§[;\x001f±=TºO\x0015#\x0015)¿¨xÏ\x0002Z\x001cù=Â\x0015\x0007	F/ô±jä7\x000fOØ\x001aî §Tf%TÁ{N¥°bêeºÖ:üæê\x0006{ÄÍà\x0017òÆkv`ÞÀi}\x001c\x0002vVN,ãU5¯ZÊKªZS\x001bë-¸Rµ6a4{yÍx=Z¦j\x001biÿ\x0011ÿ\x00173b\x0018^Ð\x0015"\x0000u`D¿W\x0004¶fç1\x0011o®þxõêÕ¾pËØ\x001bµ7ÔCªAQ*|ÀK.9m,?¨b\x001eP\x0007ªªQÕ"T%(y2\x0000fíSLØ³d\x0000pgÃµ¨ºFÕP#\x0010½[qåÍ¿\x0018Véw\x001fO]¨¦F5PIÚ¼iT\x0005æ}f¯Ý°î8\x000bÀÖ¨v	ª\x0011òR\x0003ÄeKá¬àM©©Ì¤èGu5ª[4ª6Pä-m+ªÄGãmµ³\p\x0016êVöìÚH!õ\x000c½ÅÖ¦ïïþù\x001fg\x0018Øxÿ=\x00159¢\x0010\x000fþ,{°¹\x000cÓ)¹º¹Ú96:ýúâüz-àP»×u\x0007.ó4d\x001f\x0001H\x000bÙaÉþTÅþbrUÛökÁ\x0019b\x001e\x000båHåÌ:4M¦³-'×5ù¸\x0001_\x001f9z;4äß¹ã}£ßåíËÁM
>n-Ú\x0007\x000e³±°îÖæÔvçíjÁbp[»vû$\x001bà\x00068å
LYå0eQ»|Üo´\\x0002{ÆØÅç\x0014çlN\x0007
û|Üy´<ÞÛ\x000cDes[H.åG\x001e;¥²<Ôäa%9
x)\x0003ØüZá¦ªÝ\x0016cKh>Æ­S»¸=Æx+ìLÐ\x001bVùQÑÛãsÕù\x0019\x0008^K²1WäóÇ¥ÂÎ­DÞBrÕ1ä±ñ+mP-øUFz6^c\x001c q}îWñ\x0017uùüÝÃý\x0000v.\x0016¡XBK\x0002À\x0005\x0004ÒûÂÎÀùÙÕå\x001cH¨!¡\x001bRzyjéÑ\x0006-wVîb£:­Ô5¤îÄ´tz{ÅWw4,\x0011éw¿tu@Ú\x001aÒ.$aF\x001foþüÐetàÙV»o}ó\x0019}Íèû\x0019±¼f\x001bã¥ôÐ.¹¾Øë#\x000cd9\x001fÚ`ß\ÊèÖKÚçÎ
ÒJ\x0014ü°éõ\x0011R¶»»{£,±¤E*\x001c¤{©K9Þ÷HCÏûïÔÍÞ\x000b6·H\x001dò¤\x0012h¥\x001d;yu½-½-û77v^´qb\x000b¤(ã¸±ÙÚ²o\x000blgIJ¼Å¼¹5\x0007ÊÐ\x0000íy
KÙlnÙ½»ãy#XD	³\x0016h$à\x0003Ç¹©´ÞNJhv7tïn\x000cß¦®wqw{º\x0019Í¹\x0015»+ó;(Ûc±{ëàÓð@©9]\x00124\x0017A¸½Äs)½\x0003Ý{\x0007+¹¬ÀÅã'¶.c©wGEç\x001f:²®6Í¾PÝ¤l¶;dË%%NÒÌÖeï<Ø\x0015ÖH}6}¶!òúqû~{0!dyö\x0013Ç\x000c¤#YÜxZC\x0004ÿäõõæëÍÞ\qP<{n\x000bP©%\x000b¢*âdY\x000eX$ßM©Ó.@U5ªZ
ØpðT»©$\x0014ýc=å\x000c÷ ªñ#*ùÿ~»ýxòbûS¼x|¾=y³}ÿð4#\x0005ÌÃ©çØQÀî¹$Ê¹$Ã\x000ekúïçW'/6¯ã½ãíùÉÍ×W73À¡\x00065àè>\x0015¿Äç\x0012\x000b%\x0018 we|.ãV5·ZÃ­}jÏÃ\x0007\x0003«vsI3;,î2n]së\x0015ÜØ©¼,Ë}Ø¢aó,ð`Â®2úeà¡\x0006\x000fkÀãmµ\x0002Ýpe)HÆíº .\x0002íÖ\³7£gKw-Ô\x000f$\x001fØ\òÁÀ-Æ&Ed²ùùöcN0$¦Ã¥L\x0003JpR\x0012¤á'0©µùöüUN1¤_\x001c\x0004\x001a\x0014\x0016j\x000c´x4Ø\x0014¼õÁ\x000e*õG\x0001U5¨Z2¢Òp\x0010\x000b½^Î}Õ²Ô×Oeþôê\x001aT/\x0019Q\x0010Ftè¼â]éµ£§túAm
j¨ör=xY¶Â\x0017Å\x0002?e\x000cúA]
ê\x0016bÃ\x0015R\x001fÃ·\x0006/é\f¹I\x0015~N_súERÈÕü\x0008ì\x0004\x0014U©c¸3Ôa	§v\x001c\x0001Ä\x0002jª¤·¦)íTòs7h\x0015\x0015RTÂÖO
§Té
'ÞjN]òobý ­¹_bïAéò\x0006æ5gN¢þ\x0007©¤~ÒÆÞË%\x0006\x001fã:>Q¬-ñÀ)MÄ~ÎÆÜË%ö\x001eDä¤H\x0016¶&ßPðE×)\x0015÷~ÒÆÞË%\x0006\x001f½o*¤\x000fBs¨(ºßü2dr2
Ú¢Ô,\x001aSÍêO¨\x0011NS/d\x0019Ò©è`?hs2É%G\x0013réU\x0011¨¤%ú¦¦»AI.9¤/u$^:¾2\x001aÏb\x0014.LcúI³I.9$v1&R\x001bÓ@\x0015weòaJ¦¬´9äãI¢,
PP³H§\x0018c8\x0013b²qR7)4Ç\x0013,9dÔ¡Þ%Ï~I6ÁÄâ#6ç\x0013,9$ppSr0fÀê©ï~Ðö:²äxØ\/ü\x001dJl0Øáb0S¡ý¤Í\x0001\x0005K\x000e(í\x001fH\x0001\x0002tQzrq:Êù\x0004Íù\x0004KÎ'lDÆaØè>S\x001e¥±¬DãÅ>÷|Ò¸¸Fq89JNÆæÃÛ»\x0019É8û$§E
Þ\x0001\x001d÷\x0000Õ°¯çëæ\x0004;\x0012o.ö&RÊq(VògÃªèóQUö¬½o(?Uù©°¾õK`ãx:RÒ\x000b(K\x0006\x00008dåµJ¢ìuãp¬kb'÷õöîþ~F>­æJ{,5Ëi\x001fZ\x000cÍKÝT¸Wlâ}½¹¸¼A\x000b5-,£µÑUåÞ Ø¹\x0005©Ja\x0004Y«j\µ\x0010\x0017$7%\x0010°\x001a áá\x001a\x0000ü³ãàê\x001aW/ÄõBi¨LA\x0012+\x0014[
öh¸¦Æ5\x000bqá\x0004{yW!®%e\x0003¯Ä¤JÄ\x0012\[ãÚe¸.XJQ\x000e*÷\x0005G\\x0015ÍA)´ÚsÞvá\x001a7,ÄÕü\x001c46\x0010ÊeaàI\x0011\x0018\x0005x×âÂ8´
Ãë\x000cg¯ÝÎË¡vÅ¡lÞ"Zéwª+ÏÊWqT\x0015NFq:¤ySÞ
XÇoÞaÊíçÔ5§^Â9Ô°µiÝåinOE\x0007¨©AÍ\x0012P°\x001cø¯²¸ÙÍWõSÚÒ.¢t¥0¡IÙæ|«Éí~PWº% 2´ûA}
êæBZNÈ¦LU%\x0008$ìÎÔÏ\x000eÐªfµzQë"Ål`3d\x0003³\y`ÝÇxçÞÝÊ|N.­Ñ\x001b\x001aÒ¯¾z}¿}®-gÛÇ÷w\x001f·÷'ßÞ>"ó§\x001fÏõÊñ\x0014aÉj§9$ Ý3â×ñ¯ÓýålsýõÅ«ÍåÉ·ç×\x0008\x0018\x001djtX\x000eÁã\x000bP~c\x0001îÜë$ç\x00067Õ*{\x0005ºªÑÕ*ô¸NÈWOn~gCAì®±\x0002]×èz\x0015z¼á<\x001fuë]é\x0006n&ß\x0015è¦F7«ÐmÑ7~\x0012Æl\x0012ºcõà¦ú­@·5º]®+\x000b\x00056ñe	%Ïïfê¹\x0002ÝÕèn\x0015º)ÇL\x0008ã\x000e¥h,L&I/'Íz«\x0016BQOYcàwq\x000e\x0005;¥C°}G~²\x001b\x0017H¸Qçìáäô.·?\x001fvä¶¥-M3°\x000bdNè0;f$'þìê¦Èê}»Çgn¨¹a
w4@£Ü)ä5®<\x0017ûÇ_î><\x0017p«[­ávòg\x000f,&¥¹ù\x0016;û~,Â65¶Y"Õy¼Q\x0019°â\x00060Îì\x0001YÂ-ÿ´m\x0017øvÍJ)%,Ø1\x0014\x001ffwîk\x000f9{®@î¹B\x0006%¿}Ü~À8á0!:Ù 1¡
®jyÜ»­I\x0002{½y±Â}¡B\x0018÷^Ü{e!´\x000b
ß³²`àº\x000cÁíãQád·ùîV5´Z1Ò\x0012CÆY\x000e8\x001bc\¬@7\x0015_
­kh½|¤­ç$,\x000b\x000f\x001ba¶ßT
äRfS3åÌñ¤\x0011,'ãùy^`2\x000e­0a²BÛ\x001aÚ.V)·?ïC8åæ\x0001ñdüTÌ³YúñÃ7c¡È÷q\x0008Nt.b71K=$Õá´ºýÖ\x001a8ýâÕÞt?~¸ñf,14\x001bÖ\x000bÎ-AM_îX[
¹Ô¤Øg\x0017.\x001fÅ ?åõpýðÝíãç¯oï?l\x000f×Q\x0000\x0008Ê+Ãd\x0008jçn¡\x0004kÔÔ£X^\x000c×W/Î¯±
öòåf\x0006-Ô´°6p\x0017Î¸£Yíµ<7NÕw-ÂU5®Z«QË0®!ù¦8º#µ\x0002ºpu«\x0017âj~kò\x001eËªs÷J\x000eÏTdy\x0011®©qÍBÜè.K
ÙR¯\x0012\x0017\x0003ãî<;a]
ëÂª¢À\x0011ÍáëJ½Û\x0019gêÄ
5nXk9OÆ\x001bÃÉüV\x000f\x0019=kiÅØÚá¡ößÿñ§x¢\x001d>ÐâÑK9§ØA8×Aðì\x000eOw\x0010\x001eN´ÍM<Ì\x000e£B
ËP£ÕÒÜìX`A:|%\x0017#k=¥ÙªjTµ\x000cÕ8ºÕé¡HU(Ï×:;õÞÐOªkR½ì\x0016&KØÊ\x001dýð\?ª©QÍ2Ôx[STk"\x0004V%T~\x0012uFì	7Ï@bìv	S%J¾»ýøñ6zwY±#¯Õ2é)KËë)©Dz
={qþêÕyô\x0014/fÀB
\x000b\x000ba½çºït#¦à	\x000cWâ©ëÃ"\]ãê¸Ñí¢ã@;ÏÍgA\x000e¹^\x001d\x000b×Ô¸f\x0019®9w*:À]²´\x001eÄ.JGÂµ5®]k-_%7\\x001c,\x001d÷öE=Ú#áº\x001a×-\\x000cJrü\x000c<'$	ÜäWûc­\x0005_Óúk4úZy-¸²\x0016lY\x000b~Ê-Á­ú\x0014	S\x0017ytò:îY¢PÂNÖ0®Ù¡Øàî^Ëú¨:«=<½¿}<ÜxP¢\x0004\x0011Õ^k>Â8öáÅä£\x0012µ\x000c8»ºùúüz_ÄqpuÏ¹BAy
°Õøù\x0003³»¯ÊlF]3ê~FYÔRQ	Då ®23gÕN!ù\x000eHSC\x00054\x001bVxleHÏoÎa§"M\x0007¤­!m/¤\x0008VaC·üö#O5eG\x0004ÃMF1Û¾fôÝ^\x001cºÇ\x0003-*
^zÊ\x0012u2VfN\x000cúC\x001dÚpoYL¦<(Y\>\x0017vjÒtPBC	ýVð+¥s_)¥µ³øí\x001a\x000b4\x000e°	oªÎN2¼Ü>~ÿiáàî>\x0012©ÄYH\x0000~ßýúqþMë7ùßt\x0010×Ö¸v!.*!Ó>
-;·r\x0014zJd®\x000b\x0016Æzî\x0000un4Ýû/·O·\x001f\x000f/ÍPÅ\x000fA¦\x0017 ê\x0000\x001drOÎ&]ý/77×ç¯öäßh NîDÆÞTT\x001fé\\x0011\x0003\x0011C\x001ej\x0001µ\x0010Y×Èz)2ú$4ÊN\x0002ßV¤UüÖ1)¸\x0010ÙÖÈv)²v«|´´íÀ°øËÝ½³Åx-\x000b1ÒÝÁ|ÞÇ\x0019-~¥\x0002\x0016Õ\x000c`Ì¼Àyþ~Ê¥ª$b0÷z'b1ª÷AZP\x000bq \x000f\x0000kñÔÚ\x0003[ÌÃÝá¦Úq¸Í¶ï1\x001eòËãÃÓáµ[\x0008e\x000bQÚ\x0012C)E×Â}=\x00140-ä\x000f×W7{¬¯\x001d\x001f\x0016¶}õ\x0014»IRø¤Ç9°SIf\x001d rü>.h\x0013W.·wo\x001fï\x000eÏ>Þ½#M\x000fÏ§5ÅÛÒ;[Ä¥©¿Ü\¼=¿¾Ø÷ 7~\x0017F´Ù*óa£\x001bCE_Á§Jê\x001cË\x0016|\x0002ë=÷:aU
«\x0016ÂZù\ç\x000fC\x00055\x0007\x0007½ßæ1\x001fV×°z\x0019¬tü¾\x0015Ï|ÌH°Ò\x0015!©ÊK`M
k\x0016Âz¾XÈÍIe¡\x000cóq`]
ë\x0016ÁÊJ\x0010r!½Ç¸f®ýTCí¦ò8Àú\x001aÖ/5\x0014\x0010
 )1Ép÷8®Ç1\x0005UxÅT7NÔè|®\x0019¦©³n©*Àî¼7tÒ¶VvÆsGSïJØè¢O<©\x001b·¶1³rWÒÈÖ²fÁðØî¼Ï\x001d»[ÔNYÿû?þóüû»O3l\x0017%¡;\x001ee¤OcKF\x0008
%õäüË73@M
jbÝ$Mª\x0008Jb*\x001e¸VUìÝ]³A]
êbª\x000bPËAW^
=w>ðR¬\x0003µã©·\x0013öËíÝ¼ÀRC5ïã\x0019KÎk<¶
üøGë¼¾Ü\ì_«vì¿ØQ\x001b°.`Í©ØÇ·¥â×xT^\x000b¬ÇOqz¬!\x001aÑ\x001e>}Q`Ùú\x0014CP;Êr¼»¼:t98»zóv_êx9\x0008ÛD±#ÌÝí\x000c;A(®1°¤-,gÄ\x0005»3ù:%Ç!=p9\x0018ÓÙºGø|P\x0010\x0012;£Å\x0012Ü?Ç
[,ÖÎ£ \x000bT× zÉ\x0006ö	0¥\x0000¸O:CG\x000055¨Y\x0000ià\x0005+ëæÃ5î¬£ì\x0002õ5¨_\x0002j²\x0000|Õ@%\x0019qóO	Uuñ\x0005Öäh'µ?þ\x0014YÂäyëäcÛ¸`\x0005Sº½ÙÇÜ\x0001ùM}\x0005ÉûÒpÌ8
Ãä
KX\x001d«\x0000Y¡¨<U\x0017¹"\x0013ÜÔuà9ët\x0000#\x001ecsZ[¨\x0008tøìÇO
 êÑU\x0004,
 {ÚÇßî;Æ¶ÞmýËøY3Ö¦öL½\x000fCÕt0®ÈÒMu±©LýËÍõÙÞ Å8º"GÑ\x000eTQté\	\x0003¡G>pê\x001fD\x001d\x0017ØHWç¼»ýñvv1\x0013ÖeÊ[ì"Ï¯n¼>ñµ3ù:nùëó\x0003EXáOæIþðùÏ´\x0014êóóÇÛ\x000fw\x001f\x0011õs$\x0004ºyÈùÃÓÝÃý-\x0012z4<©>\x000f{\x000e+x¯-õ\x0000²ñ\x001e\x0015²·ÿÍÍÅÕåy1G¿?yñ
ÁÞÎ¡£\x0007½T2ukÎT*ËE0\x0010ÀX0e\x0015X49º\x0017,Î"f×"Qy«ÄßQsÔ\x0008æý\x0011F,þ#L/t\x0010"#é.¯\x001di¶Ä¿AÐx\x0015X<¢l/I\x000f\x001a±<\.;Ç\x001a®øa®*è,vT¨\x001eG"3+R÷*®¸µ}/ð)Ð¸TÎÑ`×=_iWqÅ\x0003'ôrù|yI³\x0008Y´&
Êª2ë7$êÇîyd\x0010R-ù|­#f-/± Ö\x000f\x0019~d§ig¼I¢É\x0005Ô(@2\x0012TC\x001bv\x001dfPöZ×\x0010ON<\x0012ËÉ_q2!÷H¦×ïJÔ±ªsÈd</\x001d\x0019\x000b\x001drä8d>ðqøi\x0015YÜÚ²ÓðûtÓ2Ó*\x000b Ç1\x001b\x000c?7m]E\x0016«ì4°i\x0001\x0019>¤[ZfYþ
ÉÔ\x0011Æ,~ì4fq6m\x00193ÈÚ1ÕÛO w¡\x0016rÉOûûýÊå¹w\x0017O¿`ÈN \x0014¡\x0010\x0008Ó8R5¨7Â\x0019²bRÈ\x0006)Þ\x000cN^\ßüa@H\x0003=Ù02;¨à(8ÃÐ&Ä\x000bí\x001aø!j>\x000b*g @Ó±cD°\x0004#aÕ¸dGk.K0Ã$¹ì3{#.äå\x001aìÃÌ	¼E¼\x001a¥ç\	<.¢`>ÿåûÏÇ[oê¢~\ÞÝ>|}÷ùäêéþÇt
Ú\x0001d\x0014äFÆqÕhOå]^jRg¢\x000eYLtq~sòõÅÛ«Ëßï¼ø\x000cP*P\9ég\x0007\x0015æÀøLe}nxiò£AÎ,\x0002øëwáÑÕ\x0006³\x001bî>Þ¦ôÝ6Qazv£BÖB¨,{ÃZm\x000f&3\¼:ß|ÑàäÝ5\x001bÇåt¼äS*{Ä½8çëp\x000bÃ,àË%\x0006_|	Ç3Nô2\x0018]8C>\x0007\x0007[¡\x0008¾!|§Çs¢8pú/ÞE3¸»óhR¿{ötyé0xºa
NíJÎ[ÊÕñ^yÃñþÜ<ÌóËÝ§>7ÖÉ7wß\x0010ûÎt\x0015î`¨\x0005¼7À'¨R¢5?ç'ß\_üîw¨þ°û<¯hø¨IÅ®y\x0003\x0018º\x001b°\x0006G	½Ï¹4/I  '' 
Ùf\x000f^©~\x001ck¶\x001fþöC=Ul/·ï¶O\x001f÷, ¥K¥_Hbü)å¶÷Hi7i/7gµö
\x0014ÍØo\x0000ê½¶Û¿Ú'öÍíÇÏwÛ{OyÌà×P\x000b`ç>\x0000Ûg¥ÇÇü7ç¯Þ^lv×Ì78\x00034\x0003Çh5\x001d\x0017ñÞÍw
CÎíï¦\x0019< Y4¾ì±8\x000eYj']ýùðR*¬ÂÉaÙ8Î¦\x000e\x0005#Ëáå·¼ÓÏ}Õ\x001e\x001c\x000eBÌçQ©4)
?å»4(\x001e\x001d¿jéð\x0005>(O üÃÈ#=E¶\x001c,Ày°âéÃÈ\x000fÃýíý}¼\x0006mÿ±E&£,ßêøwb2\x001eð\x0018§?¿¼7Á³Í\x001f§\x001fh\x001a®!È<K#W6DZËS÷ä  \x000eîYLk5cÄ\x0006W±cÄä=¥ùÕ\]\x001c\x000f}n\x0016³bÄèwÇ¬®#&\x000co>IýãÙgã\x0011\x001b¢Ì\x001ddÞñò2'\x0003y\x001dÿnòøµV\x0007×Ø\x000c´!¤;\x001fÍHÇ_Ð4Of¤<\x0002Z\x001d<í`Ó£ó
Kí²ï
ì±¨\x0010]L\x0016 UAÊ\x000e4L Ï¸\x0012¼)
ÔÉ/²9wa«\x001dû3\x0002ÙÌf\x000cõVö*¥Äd\x0016ü3§¼s¢¢4Ý-Û$¹ç$håµRÝóÃvÆUaÊùhñW¼C
Þ\x0013B
+²iò°¹=4fqÐ¥ë\x0005³Yf2\x0019Jydc«¬æK\x0004\x001cÁ¨aç \x0019ºÑâi"#ic$c×«=¬BÃVAÐo9ðå ¯4lÅÃtÑr(²jÑ\x001cÁt :\x001fôP\x0002Ï \x0003-µx\x000082\x001d\x0010a:ð2§ºvÊï\x0014Qtò\x000e\x0003Ç\x000fiÒêµ\x0003\x000f:ÕmÒ÷\x001c÷Y\x001fA<zY0fñ¡º­
\x0006Ûü$·Ã\x000b~â\x0010AÓZ3
=¾ÌeûxÿÓÏâý8}"{Û·÷ÆÁ§b/IC¯	¤S9ñXýíó·³ªÌy@O%aENÜBÉ@\x00166\x0005dW\x0001
¾ì< ]Â°Â¹\¿\x0017HÏ'\x00029ñ,6\x0007èÖÿð×¿=Ï-\x0019ÀÒ§|@b%7¯Ê\x0001i¦Þ±gi*¨&¯dfäHðRÂ~ÊRäHrXMNÌ\/V¼1; ET"díî\x0014ÏÒlFÅÂÁúù/¿<¨þ$Lzg0íkÃæþ»}ÖÀZPå±!hòqTü;=½6h5\x001d?Ú\¾Øc\x0008þþýÇ\x000f\x001e¨¸2T^n|5ÕMìÞu_d\x001cv¥c3/·<×ÒlFõ"\x0006%.$üã\x000cå\x001f?üýÝ§G|¬ÂT°ô£¨w\x000f\x001f÷<\x000by¬L3\x0015LÙÿñï£ü²`ä®:»ºÞ¥Õ\x0012þ\x0014>|üpWì?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=~þ_[qF]
\x0004\x000fVw·¿üýß;Sß©\x0010PÔwä1ö`\x0015¯bë£»\x0007GçÏ<ÞK»xõúîÃ_ci+R¸]]½Ýº
S.s®Ô°\x001eÚ¨µv]\x0005¿	§N(<?zòÃ\x0014h5}ôMB«¹¥o\x0012Z½Sß$´úv }zý9»\x000fÃ¹ÕÕ÷äúýËÕÍë\x001d:Æ¶édÎCåi\x000eÞÐì/¸°cËz+­ïÉéã\x0007GgßïÓYãã±'1>mþÂb»3ç\x001d[Mp±·Ò\x000eKð!ïs²sä0ãRðEÇ\x0015 oy&Ë«4^/á+¾Aù\x00024¸ÝÁ\x00005u
\x0006Ç5d\x0010àb\x0010 V¢Ë\x0018 Òu\x0011@\x0017\x000ecµ\x000c^Q\x00077\x0004(vÜ÷\x0010\x0002D\x0003S>Ä\x0000CiL­\x0000í!	0Ñz?\x000c öq\x0003uÂU0is\x0007ó\x0014|.\x001fÒ\x000bQ
\x0019\x000b>Ï\x000cðÎmñ+'á{óçÇwoÑ\x0001÷¸©|\x000cFív·h;\x001bÉ5rÊ§ÃPÞ\x0006øÞ\K\x0003¯`\·ìnÖn"¢"HàeÓ!\x0008lU¥\x0011\x0000×»Q&öüï3\x0010iD¤%¡ÍÄÎhGmÆ÷S\x0003¢--\x001e\x0011YDd¨ÂèHE5'\x000b[ú'&#º_4þ""Þ]fMªÅ.cF\x0014\x0017Þ£\x0008Q`ª\x001eÓ:sÐ§nÔªn¬"$p\x0014àç$\x000c\x0006õØ¬NÈ×ã2ß\x0016L¤MI2ÏÉt!<®lAþ0ÕçÖæçüf\x0006¢ôûÕ_-àÏVW·ÿëèîíÝÇÛË«\x001di$ð%§J\x0019Ë[`À\x0012r\x001aÉwüÙÑ#\x0008ÑÎ8öüÑ)pª¿ÿÍÀ©>þ7\x0003§úõ_\x0017Î§üúÃ+¬0#Úwå£]æ\x0007\x000fW7ï·åfjÂ\x001a·/\x0000&ë¹ÉÚÄ-OìÙÁÃ£³Ç;Æß¾ÿÕÛ_»Än\x001b{YÅÛi>ïznÖ\x001aO
©\x001eI<­«K¹úz>Çà¥ßÅ^Ö3à¦íz|\x0003¤<´ø"ýã¯?ï^¿\x001f¦ë®ïÞ]ß½ÜÁÔ8òP£
é]]ó`y¹ÀêÊ\x001e?Ø¿\x001c ÆÔ¯\x0000ââóoîê\x0002\x001bð°¿|¬5ø\x0015âù\x0002arÙ×\x001e\x000bÏ®ºÀÈ@1\x0004(òqÓòâ\x0008¡í&L`tºPÔO)<åZ\x0014«À{©Ó\x000f6$²4¨LÆc\x0008\x0011ÀR	©2&#]'-kQ.Ñ\x001el8HÏAÛâ
O\x0001øæÆÄÏi8±ZwµÝ\x001d<¼þ½xw½cÖ©È«\x001bqÏ\x0004QM¤¤hÐ\x001bB±s\x0016¶\x001f<<ýgùÎÉé)çOïüê÷OxùðEÛÆ­[%¿¿»Y]mt3\x001e4EmÈC?\x0011p¤1ìÆð«.üþüìèÉöA·54ìï.\x001f2h\x0019ò\x0000\x001aøÌ\x0004Í[fÞx¨³ !ëù\x0010As)R÷\x0000.µ"K\x0005ï!5Îd3WjoïÞÿ±² ®c\x0010ûµ\x000e\ßlÇÊ¤ñêÛLb\x0003}¿^~gFóaØ6
\\x0007ONÏ¶Ã»ysùr5ô\x000e\x001f__Ý®Þî ªW%îª´Ü\x001e÷Nûo\x0001\x000f)Ü\x0010»ÏÇ§O\x001fý°þÝ×\x001f._öT^×³£àæ6­z¢V]¤]&VånÉZ6§à÷ì(¸\x000f m$¥¿\x0005H\x001bÉè¯\x0006éÃï¿ÅWù;ø©ß_|¸Þ~w\x001c\x0016_£©¸¸/¢\x0012\x001d§È¸ýJÀ\x0013$9zzºýîÜ^B Óm\x0017·×w7ðk»q±Ø³L\x000b7¡a\x000c\x0008E\x0003!ª®vüüôü\x000c~m\x0005a?Æë7¯{9<]}D _êõªýÀ\x001eWÄSg\x001a½½á\x001e'Ä3Ä²ãH\x0006Pª¶ùzPÌÛ··©6­`ª\x000e~ýtýérGÑËº)óï±rIt*\x0019*Íç~'òO§/\x001eí¨yùU~÷«+Uybý~uó\x0012ÞÊ\x000e\x000b¥"ß\x000cóÀ\x000cð\x001a]Õ\x001e¾?:{\x0000Od
\x0002ÿóK\søÝËÿ8ÕÝ¯e=x!'²¤:\x0006\\UÒ¤Öóì
ø\x0007~£9áËÉÑ_.â»ß>öì>¤¼¶¿Wð·r¤\x0015\x0016JÚ{b¢¼¨ÝèMÃ§*.x²µÿp\x001fÊzá×rsñöóí:Ø?¶î]{Á÷´4Lyp\x000bt:U*¼1ÝØé	ÕÜ?òl\x0002\x0018~´SÑ8j»Ç\x0004;m\x0015s1ð\x0006ÐyPR4è\x0019É²1\x00194I->sÜçlk6Ja	\x0018kpÓE1uynó\x0011W\x000e\x00102­$Dsõæ*þáÇ\x001bÐã\x0007b×°\x000eÎ¼ðf
iØ6HyxÒÃ\x001b\x00031ò3\x001cÐÙ\x0006áUúC¿ëf\x001f¯Þ­îvÄê\x0006©gt \x000c§¢ÍxÁy¦1MÈ²2p\x001dNÀÆ|\x0019FÝV>¾\x0008AyÏÑ\x001bøÓ¼åËð°v°]}ïK\x0008Þ?~[U&\x001c_\x0014<ª×³ë»O»×ê2#ñöjÛê .;ÀãF7ÜÙéùÒúµU\x0016o¯ß¸»a\x0017Ô\x0019fÎþþï\x00177®/o¶ß\x000cÍ\x0014aO\x001c
@Üâ.Þ~\x0006J
\x0013KpAÏ^>:Ûê·ßÞË¿z=["ìÕÍ|\x0017ü4¦@
éx*÷Hbæ\x0001p\x0013ÃX\x0002ë#ðÕ¶BQÎ~^\x0005¾1èKûéúãÅ_\x000eNV\x001fà=ïêÛ\x000b\x0000Ø,·:K©¥wê%
\x0016:}vüôÇ£§p;²O
¦\x0019Â4rà¾ñ¸}ÂÒ\x0005¥mu)ü>PÚ!J;C9±EÅþnZ?`\x0015·u+oF2=bn\x0008ÓÍ\x0011¦#:;\x0008¢4ñÝbWuã_¶#)=1L?égH3:lF1\x0005:s\x00135£ìWÜÎE\x0019(\x001c¥®OºôPãfªv}\x0005\\x0016¿\x000faÆ!Ì8C.sÇ<Xkf­1yþ÷\x00001
!¦9ç\x001dÆ\x0006Î[±(BYeÆÚ}Ä0ó\x0010f\x0001S+VE\x0011¢ê\x0001a\x0003(S\x0006;2-/©{Å>C³ûhøÄCLØ\x0011]pÚÜ(NÇ*çbf×3T»wó÷àºP\x000fK\x0002KI	lÆò÷bn×3;ò\x001c×ÉuxLÃ%ÐB,O=Ö\x000b$ÆÙ)w=C»{shëýôIã\x001fKñ4Rµ!ñQvº]ÏPîVEÂ6CÚ£\x0000ÏFxlcÄ\x000ebv×3Ô;¦qª©\x000cÆQ?LRÜÿò>¼Óízr7©©$\x001céÉ4|\x0011h)<ô°§Þ)x=CÃ;}\x001b\x0017ØÒÐeÎL½¢ÚÇåì4¼¡âM+Çbkm\x0013\x0003QfÂ\x0018½Þ\x0003F£\x0018\x0007s\x0011Óe	Ñ'U\x0015½o1³%\x0002*ðìöaÔMï¸ÏPïànÐ®\x000fo\x0014Y¡\x0012\x001f9þ\x001e¬¥é´¦¡5q¿r¤<»qÉP/\x001eè£}8\x001f¦ÓGf>û3p\x0005§6\x0014Ü<ÉI²H\x0015¾\x0007ÝS73º\x00014ô{lI«h¸*\x001fÚCÄf»gdg<#¬á(zíÞÒîÛ\x0010E":³ëi»Wdg¼"=´¤áuà]³A³!£[bßXÿ¼êó	+¹;\x0007ñP$/\x001e{\x000b*\x0019ea#/~¬Oj\x0006Òß{¤¿Ë©L\x001cox\x000etËßk·\x000f¤v8]\x0013\x000bø
qØÅFGa#·\x000eäÊÃ\x001a9uÌëm/×Û\x0019\x0001æ'U\x0016èRàÛê$\x001b÷¡¢Ü¦\AñÍ\x0011¬µù\x001dQøSMh¯÷VÄÑ\x0016y´\x0016B¥9h=NLè\x0016ÕÑb]íyb"Û±\x000eyîfHÂPó7øoóÒêxO¸qpË^2º\x000b7Ñb*"Ëï>»\x0001×ÏÓ\x0008\x001fké1"\x0018èòcû î=3=ïaï -ÎCúþHa>ï®ðyhµò}:\x001c¾ñ]¥¸¨{É\x001f^¼Þ]Ø
pöT©¶\x0006Ö¥\x0002i\x000cåñ|iÄÚà\x0019(í½ÇßïjÐkÐÌ\x0010Aã!\x0007ÿG=\x001e\x00100×¬O#ë $Ðì\x0010\x0015A\x0003åI³öÖ)$\x001d,åÀD\x001dzÎ»å\x0007\x0012hn\x0008ÍÉ Ñv\x0001\x0007w(B\x0000\x0019ûø!óCd^Ìd*PÐÂ!ÕsÑy×±GÈ!² B<\x00054GÊ¤\x0002Íq{OéCChQ\x0004MsÐY\x001fÑÅ,Ð</ñ÷ÙT$ÀÒ\x0010X\x0012\x00003ÈNMËiÁôtÏLÖ,2¿ì4ó\x0010Y&ö2J\x000b­qÀqm\x000flÄýE\x0011\x0002hk\x0016©¢mHjÁµÆ °^tÓÐ}a±E7M÷@b
LÆ\x0018TÏ¾æ,°ËWÍÌ;RGÝ}ëp\x0010þîu4xrñéïÿùýnW\x0018\x0014Ó½µ\ÂÕ6\x0017ÍH®üäøÅñ?ÏwÙzÂe¸¬\x0004\x0017è~¢é5Añã\x000czk,<Ë
q9	.¯¨X\x0016ºR+ ø\x001c¼@,M¸OÆå¸¼\x0004Im\x0011ø\x001dµæ\x0011}\x000e
W\"¯0Ä\x0015DçhyD\x0016´Ç!\x001f#/öe6¬8\x0015\x0005°TV¬ÈÊÄxËô\x001eµz\x0001¬4$Òâåc¹)0ßò\x001c^Õú'ÊCPY(+)\x0018:ìAX¥\x0017\­AY\x0012p
Ê\x0013ëJ,0Xü1\x000c¬Y£Q\x0002ôÉÀ:ª%JUåRu,Àn½Þ¦¦îH¬S^Z¢½4Óqo·ÂÈ*±h¹½kÉ\x0015ÓöÒ\x0012õ¥R»c\x000e	ã
\x0001SÌ°¥ÆÚq&\x0003ëÔ\x0016é/psj3\x0003·¢5\x0005r\x0014ûô\x0000ë\x0014\x0016i0P[¼DÐ\x0016DI¬tÇòX®q2°Ni\x000eóU«s}Ä`¹}\x0005îØ\x0012ujLôXÌÔh
\x000e«â\x001e\l\x0007 `z^*°Aý
]0%|ä\x001d:Ç,ñø*\x001dK,\x0014\x0008'\x0003ë\x0014¬\x0011)Ø\x0018h§-\x0000ËÄ\x0008\x0012ó¤Ç[¢ùMï´\x0014,Ø!\x0006\x0016\x001a[""\x0002æÕ£ìô\x0011é1Ås\x0001`}\x0014\x0013\x0014»f+C\x000b\x001c\x000bÓé1#Ñcð?0é\x0005&¥ù$\x001ba\x001ac½«ScF¤Æ@ÛSüá­æj®ó¼´.ê%\x000e¢éÔ¹b©òà\x0014\T\x001eóL\x0013\x0008¸Ü\x0002-f:-f\x0004ZÌdl\x001a"`1!8e\x0007HYD¤ê
ÌvZÌ´	Ì\x00183:mÄÁ³\x0016Ë#ÉãÉ¸:]aEºBsÝ\x0018\x0004\x0016,¶·,°\x00057ßv¾\x0015ùb:ò:&\x001f-·®´!nÀe\x0017øb¶S\x0015V *ày¨õ\x0010cs,bðK"I3(\x0008\ÅJð&£á\x0014Á9\x0005êõk.¡%æ(uuª/\x0006u):VSÇ\x0007Æj\²¶\x00124¤´äª©M|ð<eø\É&\x0006¢±å\x0013ãËcõéaÉ&¾¾®3EåæCÅ¾6o/>qT\x001eìXEgºUÿùå])±S\x0011»ï«aç\x0011ÿÌ²ËK\x000c»ÿùÕ\x0006¶W\x0007«8÷­\x001cìthn;À%ÒKTÜ½{'<×¯¦w;¬,×w;(-µwüÆ\x0002\x0018ø\x0006/y}wðüfõiu¹c.\x001d¹*8\x001fÅS\x001bsh¬`÷6\x000c~ðüìèÅÑ£\x001d|þ\x000cË\x000ca\x0019\x0001,PmhÄ6,BÅýMêÞ6H	*;De\x0005¨´§^ê",K³Ñü\x0004@V+U$¨Ü\x0010Êa@YnëÆÜ\x0014=¯\x0014\x001f¢ò\x0002TH¿C9ÿ¨På\x0016XÉ°\Ï¬.\x0015°\x0000\x0016Dr
V[3
v¥Á²+,$°â\x0010V¡ÅMÍ¬g*HÃ!ÚuÆs­¶\x0004V\x001aÂJ\x0002XÎb¯\x000eß-Êÿäl[$,Ñ\x000ey\x0008+\x000b`Å¶ù\x0011ë\x0010+\x000cîÖ\x0002Xº×¥\x0002eâ|&ÔP\¬¶BçIquÊT\x000b´©³a]OJÔ\x001bÛ¢m\x0017õ\x0002½¥;mª\x0005êÔÄû³°Ìå\x0008Wë(p¡ë]âêô©(Ôë­×FÕ\x0012ª2Ír¥£\x0011\x0019¯ÚõZ¢éu§»´Dy\x0019KÍÝ\x0005'y\x001a®\x0005ÖZwZB\x000bÔ\x0004VÁµI'v¹Râ\x0015hXËtjÂ\x0008ÔÅònmBF_noI\x000cgÕ\x0012­Ú¹ÒÕà\x001dJÓkà2¼ý6\x0000Ùuñy?átEÇ{²&¹`n]x´!\x001e%@Øo³);#Ý¿\x0017]ß0J¯Tt´pÛ(KeÖ\x001d"94/#Ø9G\x001bCìc\x0010\'ì\x0007\x0017W¼sàìúîæó\x000e¹eÕ\x0013é NL)\x001dTÇÅðìø	¯\x001b8;=?û×¡Ù!4+Ë¦¸\x0019iÂ&éÖ¯\x001a\x0001sC`N\x0006Ì²\x0013
¸®b\x0003`Ü)\x00082Ë ù!4/Ô/$3ðfù8#ó:\x0007×-\x0002C\x000bChA&59,Åi× qÂtäårhi\x0008-É¤æye\x0018x>´¡0éÀ\x001cXÑe\x0007Ú-×«o\x0014¿!\x0011^æíÉX§¶ôJ¹\\x0011L·{:@\x001dÌF\x001b48~CFz¤çýû®à÷\x0017\x00177·;z\x00075V\x0012\x0015ã5¯ ÄÊ0S \x0015\x0013K\x0013ÜÇOà·\x0017ÇgÏwµé\x0011R3Djæ E\x001a\x001e"Z3Þà\x001fKÓ¾%g\x000en#f\x0016!µC¤v\x000eRãØ´#
Äk©Å<Ð¨\x001fëÝãtCn®D«ÖÙ¨ß¯Dý\x0010©%ÑÌ\x000b¸<Ò:¦
#7ÁÛ±\x0012\x001ch\x0018\x0002
³Dª,\x0016UZ®ÍãJ×Æ(6º*F4\x000eÆY"E¸ÏL$J©è¹eÒÛÑH9Ò4Df 5Ù\x0004(ñZ\x0007JEËj\x001e©ÈF³Hæ!Ò<K¦&7BüÔXoic\x0004\x001bïãé\x000fú±Qí«¹oß\x000eÞ>ÍíÚ½¾|ÝÛ§Y\x0006J\x0001ÐL¬x9ÑæK\x0017#ë(=¾\x0018P´³Oz¶ªýHMÎû\x0015jg ô,\x000b¥+÷bZiª2\x000cÕõQÈ¡v6JÏ1R\x0010Q;Ìî\x00167xS+Ñ¦±\.ó\x0002íLc£\x000c.PtQCn\x0005zÛÔÔh÷²\x001cj§úõ,Ý«@Ù\x00026Zí\x001dUj§¿\x000f#eºjæ\TËôª9ÕàJÓ=Å-vüú÷¡ùMwMÍ¬k=g²ÁçÓ<»çP\x0005ÒéUSÅPmç¢ØY>ÆÝd¥p\x00101pU\x000eôÔ^Þï¿\x0017\x0004K¼¸e\x0013!Ä¶&cl~B\x000c5u75ÍS©8LªÉZC5ÍPÙ4º-J
µ÷§æ8T¸FJzöÇ?R3TËêØTÍ;íh¹:¿Æ`¿ m\x001be­\x001b_Á%Äº¡þgé«±\x0002¿¾\x0000ÜÅÏ}2{º\x0000Únÿ\x0011ª£XÀj)í
\x0011jlêøÂH)ÖÐc¥®TD4\x0002w ¬Ç6ÚmÝ\x0007Rß»Ô~O­@[\x0005¾­{ì¹i\x0016Õ\x001e¬ö½\x0003àçEA\x001fÿm@4f#ËÔïA5½Wmæ¹ÕØL$Ýè¶Rÿ^é \x001f`\x001f6ÀØÞ	°ó¼l©\x001f
ü\x0015G)fìGc\x001d ö\x0011ª"QbuN°
X¹)\x001e<\x0016Ë(]+÷á\x0005\x0018×©\x0000ürkí5\x001e)þ¹}_eºËêbtÎ»\x0002¡j\x000e«!0¥~0R\x001c\x0003¤±6p1ÔÐ¿«0ç]Ðx£\x0008@uLâg*þÑá\x0003)V«»»jõ¼»jËí¨©f\x0001lLµ§\x001eÕw~\x0000~9\x0007«²ÈU°K@º\x0015y	«ÝGbÍæ^®y\qÉ\x000eaU7Ô\x0019c½\x0002u¦s\x0004ã\x0008\x0004îªR<÷a¼M¦{Éª®»àk^u5Ç^a®b\x0016Ã«P0WÝ|Ö1>ëé`Á5ëk?è«!ïÁ§«ZÖN\x0007W\x0007:;¿\x001deLgµR4¨ÆÂh\x0005Y¥¯©\x000f^\x001c?©µmø»\x001eÕ¿û\x0008Í\x0010¡\x0011#ÌV$:$ùþ\x0010¤\x0012DsÇ)5\x000f¢\x001dB´RIibës	ûxH\x0001ö$*³\x0000º!@'\x0007\x0018¸q\x0006`1w\x000bÜ¬\ZÚBôC^\x000cQsãrò¶¦w\x0013hsÛ\x000ey9À0\x0004\x0018ä\x0000#yõ¸¥ \x0001"í^w9¦åÇ\x001c\x0010£\x0018".\x0007[\x001f3-wÝÙ.b\x001eBÌb)ð;®L¨9ä[­>»rm\x0016Äu]¤¨D%Çèx=*D\x0010Yßôó¾ó\x0010öJ[¬µ³VÜj\x00163WÁs\x0003h¶ÝðÁ<ÚÖb½þ\x000fÁË q°äS£ËåØém-VÜÙXÊ+\x0001FM¸ÝU·qËåØ©n-ÖÝXö¤A\x0018\x0015.ò¨\x0018ýÓn¹\x001c;Ý­ÅÊ\x001b÷:Sÿvr^pÒ12ÆÅ&ZwªQucv¡=j\ÐS¯chü\x0002Y«åG:i\x0006Æ
Ð'Þ.	_òVf¹fì·\x0016kï\x000cÀ¨\x001f\x001e<Yö\x0016\x0003/ÉJ/h:åmÄÊ;\x0007MK:]t\x0014y\x0003BpHÙ,6¦ÓÞF®½Óú*Ú¶ *ðF\x0011\x0007ög±'az§[®½×Ñ\x001a´\x0000#·û¥Ë±ÓFª\x0019q½\x0012ÖW\x0010chT|	Ë×Ñ.¾}ë_°ð\x001bÂ\x0010\x0006÷QRÕvñ8ÃY\x000b0\x0011ËÕ£¹\x0007ÔÌ@Ñ\x000bM	9ò+y\x0014lú\x001eÂÁõ¤o
\x0008_cÖÌâ´ù¦q(\x001dñn@n.ÈU\x000fr%\x000e[\x0015òõU_Ü\x0012m\x000c d¾°ºô\x000c¥Ï\x001bÃ«ð
ý\x001f\ß½»ø´ºy]öæ^Ümßç4¸\x0015%d
FgfjÎ²~Ø:4\x000fNÏO_\x001c}_vç\x001e}\x0019\x0019b32lwé\x0006¯\x001cê¡\x0002;h\x001dÌ\x000cpv\x0008ÎÀáêÒz°A!±q½~ÉS\x001c\x0018Tè¬\x0019àÜ\x0010K®¼ß\x0000Î+Qï ä\x0002IÎwÁË\x000cp~\x0008ÎË$»jB\x001c²¶ÔcÅKsaá\x000bCpA&¹ÊU$Ê&­"9K\x0014\x0002\x0001ÏCpQ&9\ª«ä´âÜ\x0003®$'É.Å4\x0003\\x001aKBÉqg^Àö{Ú\x0000SùUp¶Û(9\x0003[\x001ebËBÁ1\x000byGßvqZåXpzÙ{Xç\x001a
VBÉ9r`\x0002\x0018\x0006*g äXt:.»sº7\x00102\x000bQöÖbKá<®\x0016,\x0019\x0016^*ºÎBh¡KGw\x000e
å×Ê\x0016B©eNw\x0016B\x000bMD\x0000Ç´)2\x000e\x001bÕ\x00174õ*B1µ\x0008]g"´ÐFà°u\x0015¶äâeK\x0013c\x0001³_Ë°u\x0016B\x000bM\x00048TÎÑQç4H_çì\x0016¾ÎDh¡0òüHvSëÏIÇU\x001déñ\x000clÐB\x0013á\x001dyîà®{jK[9r_Æ®3\x0011Zh#¢Å \x0001\x001bM(A¸#\x001e¾i~Ý\x0019	-´\x0012\x000e\x0002Ú\x0008½çUIÑ¨"\Å´LÎJ\x0018¡Ðm\x00186¾\x0010óFb¦\x0019øæB\x0003k:+aV¶Ãg\x0017ié\x0002Ä¸¾	N¥eÐú(Bh#tÂ´s\x0011\JÍ±£®¾\x0008ÓÙ\x0008#´\x0011ào²¦sòT¶\x0008à\x0013^ö\x001eLg!ÐBè@[>\x0006]RgRÊ|áÂ2\x001dl:\x000ba\x0016Â:n®\x0003sß®\¢uöKÁu\x0006Â\x0008
D[z\x00134èc"\x0002Ê«ß½_®3\x0011Fh"ÀS¢®´l\x000c1}a¾º'²[húMg"ÌDiæ\x0001\x001cÍ¡©²#â*0üv¡&é\x000c\x0011\x001a\x0008Ü\x0001]»ú\x0013ÖÛ\x0008ç\x0016l\x0016~Û\x0019\x0008+3\x0010\x0018LÓÄI^fÇ\x0018ù\[ænÚÎ@X¡7\x0011HvHsË²ã^È¬\x0016¾	ÛÙ\x0008+³\x0011È\x001cèÈU·º\x0001'Q° >Yvïlj\x0012\x001a	¬¡VÇ$!\x0011KuL¢åQ²\x0004\x0000¡ëÌ\x0015	\x001b%@\x001dãÂ$nyµ°B3¡\x00141ÎùGHrT}öÈº\x000c]g'¬ÈNØ\x001c51\x0016ê\x001cøGÅQw\x000bE×	+4\x0013IÂ<îÉdÑ9.W$³Tt°"3a3ÄÖ4³F{V
S2:Ø\x0003±,-a;CaE\x0002\x001e¦ãÙÏ\x0008Ê¶ÞEÚÖèb\x00118×Ù	'²\x00136c¢,¬ò¸¬®MQeë\x0017¢ëì\x0013Ù	=ótÊÇÐª¢Ñp,æ\g'ÔNÃL·N±c\x0017]`3±ðÁºÎJ8\x0000É)\x000eý£\x000f4ýºóBt}EB\x0016L¨º\x0008´hâ\x000f
y¼\x0007Æg½ðÁºÎN8°HØî«&I«Áe\x0016ÝÂ¬¿ëÌ\x0013i\x000enã¶Í9ØÈbYè:;áDv¢´1P~8b[6\x001d¬æ\x0006÷ÌÂíì\x0013\x0013Jó¸X²<\x000f\x000e\x0000\x001b1ã2ppB3<ØG$ÝØðÀt,ïÌ\x0017	L2UÁ!=\x0016\x001d«e5ìó2ÓwFÂ\x000bDr<\\x0019MË¬GmäÔ²\x0010ÖwFÂÅ©@SâH\x0005\x0013f^öZ}g$¼ÐH¤6\x001e1/F	'My°¹a¡ä:#áe¡DÂa	Ò%`Í\x000c7ðÔ4<áèúºµÔH0O'ÈÎci§Ê®\x0019Ø`9N¾³\x0012^f%\x0012aD3U\x001c'ê³µ|í´](ºÎHx©0\x001cÁ]CÖZ\x0012\x001dKN/|\x0013ð²X\x0002L)ê·ê89â\x0014I\x0010ñsx­\x0016öøÎHx© \x0008\x001fUn1¢æ 1ú´ÌHÎH\x0004HYù}i³¬ºÎ·¬NÌË^Dè¬DZ	MüÈ :^\x0019\x0000áuæ÷ê\x0017\x0006:¡³\x0012Ah%b"äbÃèÖEÅN\ÚÝ\x0014:;\x0011¤vB\x001f:ånÈÎè\x0017®Cg&ÐL\x0000\x0006`Á¬rjÂ[Îtã´LÎL\x0004©Ð4©\x0006¢[ç\x0012Uâ7Ë«\x0017¡ëûfÒ(8jõ6ïKn\x0008R\x001b¡jC\x000f8NRã\x000clìbg`ëLD\x0010¦¢ã3
ÙqÍ$dfóÀõÚËÐu&"\x0008M\x0004öHè\¦Ý2\x00001*·LÑÅÎFDa A¢HÈíLíÂN¿Ø(5\x000f\x0011|@NAùõ.$»ìLcg\x001e¢Ð<\x0004E;M}©Í$%ÃæÁ.4\x000f±3\x000fQj\x001e\x0012\x0013[\x00060­Í\x0015&p\x0001\x0007ù\x0016ëÌC\x0014\x0016$ÚrS\x0000b¹û\x0015¢HtzaÅ?væ!JÍC`º%\x000fzÎðµ£·\x001a\x0016Ábg\x001c¢4Ó\x0014¨U\x0002$×xÄ\x0003÷JøE3ÐõÝ¯R\x0003áÈ\x0013ö CÓ\\x0012¾t\x000b¯±3\x0010Qh ¼ç\x001c]påúÕ;ÇÃÎ¤Eà:û\x0010g\x0010ÕCìÀã´uèùäèRg\x001f´\x001eÁu±K7\x001dÀÉW°cËd:+¤VÂrpèýÀM'W3,íÍMHR#a8»\x0019L«3áj&la?]êD\x0012\x001a	ÇWÞ+ÏK@±\x001eöý&\x0019è:+V"hÎæ\x0004íhK
ÈN³ì¢](»ÎJ$¡À"]Uv.·½rÁ³èÂÒíÌD\x0012	\~A\x0006Vi\x001a\x00027%°ù_ÎIHB3ÔúõÚ¹¸®o:FçÝÂê§$¤"\x0011Õ@B[\x0017j/øÍ©3\x0014Ih(¬eú\x0017Zµ$8Î]{\x001b©âÜ\x0019,4\x0014~í9Vv\x0014E\x000e_ÃÂ('wv"\x000bí\x0004ûT;á°H\x0017hn\x000f\x0016É¾¡ë\x000cE\x0016\x001a
_îZõ\x0000\x0006/o]\x0018¾æÎNd¡ÀÉÃê;ÁMk\x000eájW\x000b+¹³\x0013Y\x001aM\x0018\x001aô\x00039qn\x0008Ü\x0006\x0013ÌB#;3f\x0002»%«ät«5Ï	É5aë¬DZ	Å
DpÍ%\x000e¾¹N\x000bCÜY,´\x0012hóIt
\x000c\x0006ói0xJ\x000b_Dg$²ÐHçÄÎi&v\x0001ÏE§âÂ\x0017Ñ\x000fÓ	­¶Ô\x0017\x000e¢Ó´(\x0004©HøÚ¥eU:­:+_Jï]å2C6P\x001eã\x0008áù\x0016½X½1o­BköÁ\x0007åFØ -éb¤NY\x0006¯\x001f¨SBKáÊ¼p^\x0013g0Å2DÞ\x000bÑõ\x0013uJh*T ííà¤ö0xEóKo^?Q§¦\x0002=OÝ\x0002\x001e>ZlEäg\x000f û±küRvóJiy·.6'À°5váÑöCuJh.¬groÜ}Ì\x001d®=Û	º¼Æ/e7Ïp³õ¶1¡¨võì²þ5ÝÏ^ã2éi.Ä:ì*"sæ\x0014\x001fî².lÝO_ã2á)nþ·\x0010Ø&në\x0008,»eí:zcüZ6]©µÈEµ¦\b\x000cø	ocÄY6ã\Ücj&v~Ýêl8ìñ&.¶õÆ\x0018±l¸8RÔíà	{\x000e\x000cO/sBõÆ¬®lX\x0017®^æb\x0003ARçIÐªùÈ\x000b½XÙDl1hä¬ \x001bÊ¥;Å\x0003
à.3\x0019ýÌ©
ÚLÆÖ©²\x001e¬bãì¢KzÙÉÑá»ÀâzUy\x0016;©m'çæH-ë\x0014×ýð¤MO\x0002$ß\h¹\x001f+szÑùecÝO(jÙbé´Ë\x001c©È\x001c¡>ñ\x0010\x0000hEÉ\x0014Ý\x000f\x0001jÙ\x0014 Å\x0016qg\x0008F\x0002IêfãWëÍwê~ÒNËFí\x0000^äâ¬Å|\x001eµ=q½½P-@gúÊ±ÿÍ\x0001ÒaÈ2æ+\x0002~G8Înê,îò¡ûÄ\x001ccÁ,mUf¸)»È±lÊ\x0016)Xª\x0005Ì$;¦>aÚ\x0018·0W«ôÏ¯;)~÷ZÆàèáh3ÏggöùÂÂ7¢Ý<ædÇ\ê¢ÃIÝª,\x001b\x0004}ZÊÐâÖ<r¾² ¼±Qe\x001a$\x000fè×S\x0017Hâ"\x0015xKçRõ¦\x0014­>\x0016e\x001cÛ\x0012$ÖÔ>\x001bÚ\x0018c\J6¦þ½¿¿n¢çYÁ`=$VÕLÚ:lì¹\x0005ïU\x000fïÕ7öP6T
<\x0014®ù·\x0017Kµºw\x000f1s%}Î8\x0001Ov\x0019<\x0008\x000e357þ¸h\x0016e6Q\x001a±e\x0017RsðFÑÞ%¸\x0014©\x0007\x0016fìëo£ÝF\x0015smcÁ,.Os%gÄm)ûBXsVúÊ]±\x0012Oñr miQ.ø"uÃ\x0007íy*Þ;â(=c0+ª¨\x0001;3¹\x0012È}f)¥Kè
ÈPdT´²Ì"¨mÎ
Á7\x0017 ½Ú¡Wb\x0019Ì{U3Ù¦øCÊöÞ9[ñ[VÚc`W\x0007nmã´ðq=æ½e³?i©÷ðo~Ëé6Lb\x0011zÇ\x0013_ØËDóIQ\x00013(µ0íkî3FòÂËr¢Õ$\x0010Ì·ÎC\x0003ËÁ/¤¶t½Zt2­øï=h­î½g¬zI\x001f´óD¬+û&$øÜª\x000b}m\x00176ý\x001c\x0008¤~\x000eh\x001dÏ<0cª\x0013s©mWzã µð¤uå9/¾ljäMYÓpI°Á,«\x000c»{Ñ³FÏ\x0016¹¤Z2åÈzÑ;nKÌ&/ôqôFX%4+aÁætÈ\°M\x000b\x000ba\x0008ï¶w» ^!òæa¼²8°ïï ð
þ{ã\x0015ð>6àU\x0000´àÉ\x001c:.ÃþÿÔ½í²\x001dÇ-ø*ç\x0005.#D~Q2[¦/EjHÉ13\x001cG2Ã\x00112ÙMQ\x001d3óDíÿó\x0006~±IT\x0001¹\x000b»Î¡
YÛ\x001evDÍsZa-¢\x0012\x000bH$°üÇubRÇêÊIå¶Ë\x001d\x000e[Ö"\x001douÑ9¬([]RÅÙ\x0019¶ä+ÿîò\x000bÖ]ýëÛ»×\x001f~|ûñÓÝ\x001fßÞ¿ÿ\x001fß½{ûñãÛÇ\x0011Æ¢:A<Û\x0019Ö
nÈmK5¯xv÷úÕWÏ^÷ÇgO_Þ}÷üÙë×Ï~\x001b&na¢\x001fæò0± ìæ&ã¢ºý6Õè\x0006 ã\x0016d°eTQV*,Þ¹îZåTqÙ¬´è,LÚÂ¤	M\x001f-¨\V\x0017¶Xu¡F[X3oaæ	©=AÝûdH¥_\x0001Ì\x0016oaÍ²Yf`â\x0013Yt\x0016Pä\x0002:JÔon·AÏ¢¬[u\x0006%m\x001a\x0005Es¡¨&7éÝÂm²M Ìã÷t±r\x0003]êSÍê½Iú2Ã\x000cÌ ³Ë7\x0007a£y|óx\x0003Úg¸½\x0006\x001b¡\x001e\x0018¹h¶àDí\x0005²*Ñ³0
µÃ\x0004·s\x0008*²ø\x0013u\x001fVÿêc\x001fVI78`h\x0013fxs [Í	ò^Ùy3é¶f\x0004\x001agq\x001aÞ\x0019âlq¬ØÌY×h·¡\x0010¶´Çi(	&8J\x000fQ­U\x001eÏ9¨Kr\x0014°ÝÀÝû¥{sa\C&ÿÂJ¼PáýòõUÚjÉ·@k*äkNÇ¿ðóý8\x0003\x0005LQpX\x001a½ê
(+W\x0016-Í¡ý×d$õ\x001amBË=<AV\x000cf\x0015ó.ÚIÖcé©,/áUbß±Y¦üíý§Oo?|z÷8¼W32¼È
Õká\x0017FtJøÐÖÐo~ÿý³Wß?ÿm`¸\x0005\x001e`¼ÑkåÏØy^&\x0005CU\x000fJøÐZÁãÀâ\x0016Xô\x0000ë¹\x0006d\x00016ú\x0000 \x0001\x000cNY¶ÀÈe±&\x001d2\x001d\x0018é\Ð¬­ÿÏ=°(ò8®´Å\\x0006Ëº|1BÕ±
àëÍ
\x000cÌ\x001c´\x001bXÞ\x0002Ë.`ªÊÂýºþ\x001axúf\x0005\x0016\x001eÚF{\x001cXÙ\x0002+\x001e`¬±/_24W\x0000ç"^étÊbu\x000b¬ºE\x001e<a`X,\x0012\x0001ÐUÒT\x001fX`w\x001cVÛÂj.XYvpÇ ©V\x0005âý*pÆ\^]\x000cÛµÌ\x0007ñ(Öú!±\x0004\x001d\x0014¨Û(¯\x0016Â¹YÚwñ>5y½'l¤X²v¥Û\x000c\x001fØíx\x001cá}p\x0011&)u\x0012rQVèBÛêÒC+Õ#3Ä\x000f.æO´Ê$öÃ´
1f=ýt&"!~p1ÿåN¥§ ëm)¢\x000b0Ì\x000f.êÏ¤5.Ì£ê\x000f¤õÂ~Ë8Ã°`¨\x001f\ÜÏÏc+g \x000b#\x000b÷gi¡'ÂôÀËãÈ\x000c÷üûL22\x0004PÉ+¨ È BfÈ\x001f\ì_i\x001c3\x0018}*\x0007ý\x0019xq#3ü\x000f®\x0000Ðªl\x0008!\x000c\x0017\x0007¨YÏYhgl&\x0002 +\x00024\x0011¦~\x0011\x0018\x001a0=ë×\x000c\x000f-û=ÌD\x0000ôD\x0000AZÅ\x0006	j\x0019\x0011 É\x0018\x0004ñ\x001cñ\x0019d6ówENgk/5u©Du:\x0002¬â\x0019:C\x0013\x0000Ð\x0013\x0000òìÀ^0è=¿Î 3\x0011\x0000=\x0011?fY¢êÐöIÃf§	\x0001è	\x0001\x0019TxL«É@Þ´(t
\x0000è\x0000\x0019T~¶\x0003\x001b\x000b0\x00045YSÇÌD\x0000ôD²lOé¼UX7zAgÂCÛ¬#3\x0011\x0000=\x0011 SÒ\x0008\x0010ÚX8$Â\x0007\x001dÙCË¡#3\x0011\x0000=\x0011 ÷ôBn&¡TÚÀ,\x001bg\x0008Ût6\x0000\x0010=\x0001\x0005Ý¤n\x0019Ö?®ÀD3½§xæcF\x0013\x0000¢+\x0000ðV£"ÈP{
p&¬\x000fí#?Ì\x0004è	\x0000y4ú-+\x000ef\x0016\x000cúUêÌ)¶ôã
\x0000Ez(¤Äk?\x0016dUÏ?Ú6\x001172\x0013\x0000¢+\x0000´ \x001bÜ6\x0002É3pDsD8å\x0000&\x0000DW\x0000¨Q\x0006}yç¢6ÊaÕ*\x000bòPÀ	d&\x0002DO\x0004à\x0016µþ³\x0008ÊÅAÂ9Z
<72\x0013\x0001¢+\x00024í§éùaP¡¨ÍÒ©\x0014\x0008l\x0003äzCçß|)t´}{khçß8òî,bÕ\x0004a\x0008ó_nQñ\pÏ×\x0006Äì3`éNXÞEÁ=Ê jOÈÏÝ
ÚÎ|Íg¾\Ò
,\x001f\x001cÅi\x0006úÐN}ß¶³_óÙ\x0001\x0006aâu\x000c\x0019Æûxò^Uw\x0000«\x0013`A{uÌa
\x001aÄÚÜÃJ½~ñ©ëÏ¥ÏìÍ§ûß½ÿëÇû¿<WË¬ô!-óÜK;\x001c¯sZ\x001eSá±©7ß?}ñüå7¯þþ·\x0011â\x0016!º\x0011ö»ÖÚ°ÇùÜæ&	Ú#
\x0007\x001eq\x000b0ú\x0001â*&¬úÚB¥
\x0013>²	×0m\x0011&7Â Q$q\x001a%÷h**S\x0006ù\x0011\x0015U\x000fÄ²Xü\x0010£\x000e\x0005ê÷±\x0015aV
HÌÔz\x0010Ö-ÂêEØ\x0019E\x0007»9åõnUa°_·\x001fFð@l[ÍoÄ ÉÜ\x0005¡O¥4Ä·\x001eÙ£æxy\x0004©ò\x0008â5cäw¬õC£¾î\x001c\x001enmõ@´èæÄÒo´²´wú®Í­\x001dbV±<<3áÁhH\x0011Ü¬XÚX\x001bø\x001dZ\x001c&©\x00187<¶æÂÑð"¸±°L¨Ú\x0011´´N¬\x0013*v<í0·*o%N¬\x0006/\x000etW\x0008Ñ \x001dzD¹É\x0003Ñp7¸É¿´¬äpr¡ã§_Á(`z0f1ûÍ¨b\x0001\x0017éÄÕ²5<=:xéhâ\x000b¸\x0003La]5åEÒøß!ªÃØ×9&Â?Ä\Ãõ­\x0001\x001a"¶\x0010\x001f°ó`4!\x0006&bLÕt¶\x0015~m_S	UpþS£	1è\x000f1u\x0008\x0001òvl\x0019XdÎÄvy0\x0018þ\x0018ÃÅ&f$xãW µã#\x0013o\x001e6ñöÇÒ¤G½µ:<&&=\x0008§C\x000c\x0010þ\x0010Ã½ÊâÕyl·é\x0018å8v>@\x0013cÐ\x001fcÊè.j<"a\x0010²#<"ýèÁh\x000cúLwe©g¶~_¹-\x001a\x0013G¡<2­ìÁh\x000cú\x000cO ¸ÌØ'G¨rm\x0010\x001eYÝâÁh¢\x000cú£LÑ}÷Ô\x0008´.Ü1j\x0013u¹[(þ(Sd-_7ã\x00107î\x0010A]æô\x001d\x0001MAw)K'ª\x0012êÆåÏ\x0007h\x0008<ú	÷óW¤=\x0010\x0004ªz\x0012b=Ñ\x0010xô\x0013x"^I,&(ò\x0014TA°_ÀNßª£aÇ8ÁÿôÓhÚÍÃíDæ1 E§xTÖP3.×ðÈø·çþ\x000f×P¯un\x000e×ô`\x0014õ$(¢Þi£Æ\x001dÒ6ÔâEaIî'Ò\x000cY¸ÆÛàeô{\x00164\x0015zDùÚUã»¶hùöÝÏKo\x000f#¯,I¿}~Dì×gÐ\x001f¯\x000cúãDjÙ4EGUc¢8J,¶ëÎ\x00073Åt5\x000b\x0011\x0013WÆ¿þ_oÿöîýÝ_¸jÿøÌ\x00006\ÈÚúuÃ.j@¥¡Q`^w¿þÃ³o¿¼û=WíÿWÛñëkD¸E.DÜÌS\x0005\x0012|x¦Û¯\x001bÖæãâ\x0016Rü\x0012D[Dä3\x0012©tÍË\x0016¢ÕHª½ÙìäÃqHi\x000b)}	FÊ[DÙg¤ÄP+¤Ä½\x0002«´\x0002ÛÐ$WÇ!Õ-¤ê¤\x001d\x001dRY§	:"ÝñÒ¬ÜÁqDm¨ù\x0010!Ï\x0011¯Z/Iµ;$]ûÝl	á0¤Í\x0008\x0001sRðaªÂ­VªØ­êå,Å)L'}DÉ´¤8úúÊ´¤¢i\x001d:É0%8©²=UÁ¬Ó³>È\x0015\x000cZZi¦¨\x0012\x000cU+;3§*\x000b\x000cº¤ù«Û)N1\x0013\x0018²\x0004\x001f[­Åµ¬i-K«iÎJ+ÁGÝë ÓTõ«òôìiÚ¬Ûa"(.L-k2ÍûV"@\x001c\x001f®ò£àêûN8×`å
«^b'MÑ Ì0\x0001Z
ç\x001f= H×\x0012å@©VL*ËÍ:cy\x0006eLôQf¥$Íp³áuD³ªQAÈ\x0012-eF\x001fg²\x0004(LÁØy]"&©,iÆRÑ\x001e©è<R5«®\x0014t\x0014ëKXC&\x000eJq½\x0008Ùr¥*<ßO\x0017K­Ó\x000e.q¾\x0008Ír¥\x0006Ëç[¥µU¶|>©XtPuÊRd\x000e:ÿè²T\x0011UµÌmÿ2\\x001eIZ3XÃ /ü£\x0007TCÙ¯y°deTÍ\x0016Ã¡(¯Ç?º0\x0005I53ö?F9RI¢^\x0001fÂ\x001e5{ki>Cõ¤w\x001dÚÈK\x0008&"Ö\x001eç2rjÕbòÑy2¬Ý1E®|- @©3"Î|½d¯wü£\x0007TjëàeÇTTÛ)ê\x0002²)Ï\x0018\x001b\x0012¶ÈGR¨;\x000bxï¡*ÊåHÎ`L\x0010mù¢ÿË\x0017ßý|ÿÓÛEkâîÛ\x000f¿þüîýãå~¹ÓËj\x0017>¬Ow\x0018µ	¼$óTòÝ§_?[u&¾}õÃç/\x001f¯­(8ÜC\x001f8^ä½ö4gVè\x0012pMÇº)ùN`[lÑ
\x000b«,Ø0«<s÷D5\5ê\x0013àh\x000b¾,Ã¥-¶äÃ\x0006Zw¤A÷ï"ª]5ó@\x0013Ø6ª«?üèý®2KC\x0011q#þ®2±Zlëí¶ÕÛÕ~ü\x000b\x0017FÒ¡ÂõÞÚ1ê´K'tÖ÷Ö÷¾ãGLwR\x0019B,ØT!¦¤Hsø \x0016Ëxý\x0017ªJÙ\x0019øëÿuÿË§û¿¾ÿð\x0019p\ÕZ³2êI«n\x0008$¹9Rp­§×\x0019øë?<}óýÓo^¾:-m±%'¶ [Ú\x0008k\x001dØÂ\x0010Ë¸ÖTrB+[hÅ\x0007í2aúþÂ	N¿Çky*'¸¶\x0005×àÂ\x00183§¨»C¢vVSGWN\x0003{à'%
à2ù"CCcÐh'èD\x0017
ºè>sâ¬Hy´|ë\x001b`GÎ9\x0004\x0018\x0000§G°b£L
ASÁ\x001dU	&Ö;8\x0007Î¸\x00048}¢\x000e7Ä¨sj\x0014«~XÛp9Îø\x0004ø¢\x0002
UÑ\x000bÚTy\x0004w>hh<\x0002}\x001eÑã¶m,ê#òU[Sy\x0012.p\x0015 ºo]Àý|÷õÇ\x000fïþ¯ÿñúÃ¯ý\x0004[âu]k`aSú¡$Fô\x0000\x0013¿xz÷õëWÏÿ÷»×¯~øæ3
l\x0011·\x0018Ñ±þª Qt"µÎ[Ñ
2\x0007\x0018
cU7\x0004BS5Tð\x0001\x000fñb¤-Fò\x001b²È`]·£ÊY^¤p\x0012]nN L[ÉoE¡6´!¥xCy1OX±=\x0011e´~0\x000b!KU¸ä<Æ²ÅXüvÌ(û{î\x0007ÚÅ%ä/Þà8Ö-Èê7dÏü¤á7ræªÿ¢\x00072=DÝ^m\x000b²MX2ÉÚ@bUr\x0013YHE c8$/\x0015ýÅß<\x0014-ß;W&¢~TJ$¥z\x00036ÖøÍ¿Æ&ÚÀD¸iUÅO]¯ª\x0017£y§I=\x0001Ò09ø©¼\x0018q{,:Äàq»\.Ç+
Ý_¼ãüÑâüñËÄiVp®iÊæº2Ë½~3=\x001dtz:\x001a¹\x0003+^wáÚ)v\x0001ùo÷\x001fßý[Û\x001e\x0018¬ùâ^FÑ æ~@y\x001f®\x000fãû·§¯Ãmm¿\x000e·èÐ\x000e®Kn¤úv¥\x0016m]lå¡ò\x000f`Ü\x0002^Dr\x0017\\x00006\x0007\x001dNn¥>pkð\x0001¤-@ò\x0002\x000cE§²\x001aÿQösä¤\x0012Ô\x001eÜ\x000ei\x000b0y\x0001ÆªÛ³x¥=r{t<µD§-·\x0000³ÛYdl\x0013¯Ç.¸iôu\x0018Ñ)e\x000b°LX\x0004à\x0010Aí\x0016ÔIÕf3§\x0000Ö-Àú\x0005Z°m\x00016/@TUþ¥éJºêØÊÞ µà%oDés!ÄV´i¦ç\x000eÚ\x0016Vî
¨e·rÅÐ05x©\x001a\x001bJ\N\õÉç?\x0005á#7#\x0000ÓU\x0001\x000bE¦kåß>¼ÿôöý_ßýü994\x0019éf-Y\x0015¤Æ@ã\x0016S\x001eî]ù·W/¿öòÕ\x000fÏ_\x001c[èÙJ\x000bà:UR5èéèbH\x000f·oú`Æ-ÌèI\x0011U\x0015·åË¦V\x0015æ
0Ò\x0016#MwÉ\x0006÷àHpÑyPobÉ´EfP>?¶x	ÔÆÜ\x001dÜ\x0002fÞÂÌ\x00130YÏ}AÉ]Åz,«6\x0004h\x000f÷TøP-Ê2cLFcjØDé7Á$\x001d¿+\x000f÷Èø`Ö-Ì:\x0001\x0013:yMIÊ\x0000=&^Ö\x0014=ÜwáCÙ¶(Û\x000c\x0015¡,±í(QSÕ¬%ûÖ\x001e\x0019ÜpÁÜÄÆ\x0004W}åÇp¢ÈÌqÓ\x0016¬±±@ÓAÁXnÀE`£ÏDø¼+M	\x001a~ú\x0005F+}-×\x001b|8Møø\x0003ÝRU©¹­-¹~ôüÈø\x000f§?0\x0011gAdRe§¥´|yh\x000e&\x0004ÁD\x000c²´\x001b¬0Ûª9Qò\x0001m¶H5\x000bÓÄ \x0008BHE­îD)Y÷\x00024Û 1Ó\x0004!BÀû}ò0§ìMÊ£è×2Ý\x0002§	C0\x0011°\x0007\x001fyÃfI¦õý¿¨º´=¼ßÂÛM\x001c@\x0004¡h¼¬ýë¸zIUâñ\x0016nd"\x0011L¢þ¹3XÏg\x0012RÒ\x001d$-Ñ
H\x001eM$ÂHÄ2\x0011/ä¹\x001eÏDã³ßÄh\x0011N\x0004#¤×`\x0014¢îmÍ9k0J·\x0008FhïB\x0013Á%ÿäy¬ÂhXO\x0000¤öl7pw4Á\x0008'\x0011ÐÐ\x0007®t¾;²Õí\x0006\x0012h\x0013Ñ¨\x0012®ó.8c`}jÆIE7æ´\Ð#\x0008G\x0010ã%	IZæù\x0011Ý\x001fðá4á\x0008'ÂQ¨UW$r8
r>s\x0018çnñÝM8Âp\x0004\ûÐý­c`.Ý"-ÝâZ&\x001cáD8
¬ú!8!énîtùîv×Ô,N\x0013Ð\x001f°±Ì¢´3ª\x0014íÒ2|\x0003ç£ç±Q}RW{¦´Ô©ñr_nàíÑ°|ay~\x001c\x0019®E¥ÔÆWÏ7H£-yùY\x001e\x001b\x000c\x001d¾ÔO§\"©·\x0010op:£aù8ÃòlÏKR'Ñv\x0001¶GFM|0
ÉG?Éc]\x001f~jQOïD%\x00113[d Ñ0|ô3<¶1CËÂÍ"HS¸CV\x0013y¸A$á£á±¢\x000fã´\x000c5K·SNõ\x0016>d\x0018>ú\x0019\x001e[\x0019\x0019Háfw906üðX«\x000f§aø8Áð¼Gz}9%âÕ×+'aa»nã|\x0003_'sã ÿ\x0003[\x001duø\Ç\x001b§%\x0012¥vïN&\x0012ÑD$ZÊ«9ébÎ$Ï\x0005ã#ÓÌ>&\x0014?\x0014!Ëc\x0015\x0019¶IM/p\x0014õÂQã
¼L$¢HTyÃõjMÈr\x001bFÔI¯\x000c·d\x0008f\x0008\x0007\x001d×\x0007·¦ZÔ\x0005Ãh\x001blõ\x0006v2ÔI\x0013ÔYZ\x0019\x000f±­Û½
ðâ iÑ*7xÙ Ã4ÃÔt¤$åq'âÍånÃaN`NÎ­=\x0015-Vå²-0Å[¾aÎ4Á5\x000erP*\x001a0§¬\x0011\x0013oÓ0g`N¶§¶ñ¢ó¢öTsÖ\x001bPR2Ì&WI\x0004]_Yõª\x0001c\x0002oQ©I9Ó\x0004sr5\x0016ÕðÀjÍÑ5z\x0014>Ù7á	êäU\x0003º \x001d¦sP4K·1§áÎ4Ã=ýÐi\x0010F\x0017\x0019%\x0014±ÿ
p\x001aRJ3¤ÄûôtUt^Ì\x0002i\x000c\x0003Ø¥8³qö<ãì%è\x000eL^i-Í\x0000@Ecf(7\x0008íÙ¸QJ@HDÆº·Gmÿ@\x0018SphÃy`öÃeë^\x0013\x0005¥¥k\x0001S;YÞ\x001cT\x001b&\x0001Ô\x001bäÜØ|i\x0018^[\x0017ø\x0017n´ß¸#w]VZ\x001bâÁí&-Jq»Ykíÿá_¸Ñrê)ú·ÝKãJ)\x0003í-`m3övÊ¶ý¶YUü\x001fuD=
tA [4°Ôk´u
mìÉIRqY]ùPZÐÄ@§Þ9C¼ZÀÅÛA¥yüéû¿|üÇßïÞüãïÿùöý»·ËÄÂ²J8\x0014>\x000bë³¾ÁG\x000c×O_þþõ³»7Ïþôìåóg¯\x001b n\x0001¢\x001b \x000f\x000b>REXtz=B¹nìôâ[|Ñ\x0017À)À*·âeÇêÍ\x000cH[4c@yn\x000f²"Íþ<:.mÑ%7ººì½YÌ×¹(«b½Ö\x00109)=	0o\x0001f7@^^&\x001b\x0008KÑîK¿Ò\x0002°ø³ß·l\x0001\x0016/@Þº%\x0015mèÙ°jCWÝ\x0005\x001eËõ4\x0017_Ýâ«3çO\x0002bàm«ýrÓUµm7íÅ×¶øÛ~ýØ­1\x0005bù\x000f\x0018QûÑnþÃïÒ\x001c·0t1 \x0002þG\x0018\x0016Ô
9ôa°1Ä\x001dDø\x001d:\x0013S\x001d\x001bËfæ1íÔ\x001e¼\x0008M\x0010\x0001\x0014éÉ
èZbÔ\x0019ÝxÙ1
åz\x000cÉÐ°4øi:ÆÀSÄx0Ão|åîÿrÿË§#4~\x000c~GNE6\x0010.«Nõ\x001còX%p=kæ´!\x001aOA¿§ä¡P\x0015¸´&
)À|ò\x0018¢ÍeüÇ°Ví\x0019æçü,dco=ÂI²Fs\x000cÑ\x000cyÍ¤Ð!\\9\x000eWÆÝ´\x0017¡Çè\x000eÈÜD$ýYÐïZEEHô\x0014ÆÓ|m\x0016v7ëì¨Ë¡7ËB£¨\x0005¿îÌgé&ì@)A\x000bxu^Öô_}\x001a	ÏÆ°½©
Pþ\x0017è¸úñ2GMäE\x0005Þ0ÒÉs	øçOWAæHæ+x\x0008\x0003Ä¦w\x0015'¯*\x001dâOW\x0010r'\x0013ý'·:Drb\x0019Û ëÙûÀÎ{¦§Ã`\x0017PF\x000b3½SáÎ}pÊ}xoJ\x001eSiµ¢·gØé\x001c\x0005\x001añj6¼ÿB¯÷ß¼ýðñ¯o¹{óîo\x001fÞF3¯sOâ~àu°B{jÉ:\x0016ð+¿yöêõ7ÏÞÜ½yþí«\x0013ÍS|q/zñõÜ[vªÕLj¿\x0012v¹´]Äv\x0003¤-@r\x0003Lú\x0010Ö hVVbP\x0003î£\x001b`Þ\x0002Ì^ÜZ)\x0016ìÉì*+u\x0003!ìæëÝ\x0000ë\x0016`u\x0003¬5²Î°To\x000böÊþO\x0002¼\°\x0016\x001f	nY÷Xu8\x0005e3k\x0007®5\x0008Ý\x0000Ñ\x0000D\x001fÀØz¶­½uÔ´Fuù\x000eµºSIt#4^\x0002N7é\x0008/<ÃÑy\x0005XÇ\x0019ÿÆÆKÀé&±xi§þ~\x001cI{g÷"nÆKÀé&±e\x001cÃ&|W\x0015\x0013\x000ei½ÚvºÃ\x00081 
%ý\x0017Ûéë_ï~ÿ¿ÿû?þßOñ²¨º\x0007=s,Y¯{Þ\x000f²¸ûý³ï^}ÿÛÈp\x000c]È¸èº
Öq­FÕyjé,\x001e\x0011~¨Cå0´¸\x0016]Ðb¿Ò¯7\x000cDf²A÷tþåC\x000f¡Ñ\x0016\x001aù¾g·Ú:°³rÑÀ«j\x00041µÞÔ\x000eCK[hé²ZÞBË_\x0014´²V¾(hu\x000b­~IÐ6³ÇLkáÂf
|ÌöÏÆf
¾(j\x0003Cmàã¶\x0016¶@×\x000f®typýøË?þëý¢Sûë¾ûÇ}üì\x001cdQI8j.%W-e$ÜÕ^¿yörªýáOýÒø¹Gaº~s¥Ë«\x0003#BÑt$ö\x001b\x0012¦-Aá:áôC[q\x0006â¸{sO\x001dUÅ8º«vWo7FÚb¤/Òi\x000b1M@DÔq-î\x0015cZëªÓs\x000ecÙb,\x0013\x0018#é\x0013'ËÀ\x0006ÄFõ´ãtl[mÆ£Ç Vm)¼<gíEÝ©\x001aº1nÞGhó>â\x0001Aoã1/[/W\x0000\x001d"Ly§Bå·d½HD2Î*\x0012_ã~¯õ`\x0002 \x0007)
«BdT¤DCºÎÓPº¾¸%{q[½¾½ÿË÷¿¡\x0000³Ê¢'¾\x0005£h·5y\x0015ËÝ\x0012\x000f7M½xz÷íÓß¿zy\x0000 n\x0001¢\x0013`à\x0016\x0010\x0012Ý±¦ËÃR%PÝ±üp\x0003`Ü\x0002_ \x0005i\x000b¾@\x000b¦-Àô\x0005Z0o\x0001f'@ÈQæGRKUä±/9Y¿
?2Ûä\x0000X¶\x0000Ë\x0017hÁº\x0005XÝ\x0016,OT¶%ÙÀTrÓ
!ÂÃ]Ï\x000em\x000b°}y\x0016Ü,\x000b½º\x001eBØï:²¥·i:~Qt+}\x000eôÈ"j\x0007B\x001bJ¾ÀX\x0002&7@\x000bÒmùi¤,\x000cô\x0018>¢qç@h	|Ñ\x0004L4\x0001o8AZd\x001bÔE±¥\x000btÀG¦¿\x001c\x0008M8\x0001o<k\x0017Õ£-z÷Ë¼ t¥ëøÈ¶_\x0007B\x0013OÀ\x001bP°\x0008Òö#7F©jÌºú·Çç³\x0008
_°±jãòÂ6QÎ¡î\x0005ëlóÈTüqhø\x0010Ý|ÈSs"Í]ï\x0003´Jæâð³\x0000mâê%~1\x0015É Ôr}\x0012å#×¢°Y¼à$BãÊèueZkJ¬:¼\x000eÖ Ã(µ<2Þá\x0000hü\x0004½~B¥ñÔÉbÂ~kR¡FUNìyu 4~^?aiõ×\x0011ªÎV

U==²\x001e÷8B26$wò\x001aÂ:£*¿ÚcÐÇ¹~\x001eÏfÿÉøIr\x0007åØ¬\x0002ñ^tvÖ\x0011T\x001f78¯Üºyëeò@\x0000Öü$H8Á¤êá1üÄpu\x000fÞÌ\x000b\x0010dP+qd×ªiÐ\x0011>"úu\x0018!\x0016ëÈÅ}
Û&$n"]3¯rÉ¼NB6¯þÄ\x0006³áö\x001c&kå½di×Ê!½åÅf¬È?:!v>\\x001b\x0015ºÁNÞó;·æ
¸\x001dH6Ã&w\x0015¥7/\x0007hÒ\x0013Õ!\x0016M`ÓÙ¸LÉP6ÿè\x000cÌ¸J¼f\x000e:´ÃÚÌú¡áÁ~\x0005\x000fÄbr\x001bþÑ	\x0011zÞ*\x00087ZÜAóCxdm÷aÙRNvS\x000e±ðDòH\x001dhb\x000b\x000fK\x001cG
móÞÐ\x000cbÃÚª\x0008ÞöÜ´h\x0013\x001f\x0011'9°\x0018_á\x001fý\x0008s\x0013¨Óc\x001d¢&\x000fñ\x0011
Oép[È^Ëv\õPõ\x00068}]>6-8¼
PpÎ\x0017\x0010\x000b\=ö_Ø%G¯ßþû¯?þüî?~ý\x000cÀ#hOº	°ÇB9´oe]á½~öÝ\x000f_½xþ¿ýp\x0000"n!¢\x001bbO\x0014ÅÝ "ÐØ!Ê*×\x0018·\x0010£ß¨\x0017\x0016^é¢\x00085\x0011[¶\x0007EH[ä7b\x0014ñ\x0004^\x0003Æ\x0002¢\x000bÄ"ã\x001d\x001dâ#Ëõ<\x0010Ó\x0016bò\x001b±_í¥\x0019®gÞ GH!î;ü\x0010ó\x0016b±b\x0014oá9#Xv®[	ýøÊ\x0016_9AÚÏZyUL8¾rÝ½ù!Ö-Äê7aEÇ¬Ó¢ÛzSÑ»g?ç­Ø¶\x0010\x001fbt¶C\&0W+ê>X\x001fZPîx)i/´\x001dÜ\x0018KÕj'Ö8ü9+oóÌÌi6´øcK\x0007&\x001bÖ¸\x0019s¢TIb~x\x0007¢	-à-%D`BÞ):\x000fÉ§Y\x0011Lh\x0001laiM±b**T©!ÅtÓh\x000bø£KQÍßþ¥Ç´DÊ±/}Þ&º?¼º\x000e%ìÃHNÛ/§\x000bà\x0002þèRè\x001a\x0011e[]G¨z<Ñ.áhâ\x000bø\x0003L¿õÐN¬²»ýEjb¼\x0010ù4F\x0013`À\x001faä\x0005\x0003SÖ¡:ÎÞr\x0017Mxø\x0012ezõ\x0016M"`8Ëéï&¼àDxÑ~¦n¯*µÏFðBé4w£	/è\x000f/%j
\x001eaèWq)G0ÂNâÄÑ^]üñ%gÙ!\x0010\x000b¿ ®v\x0004ýÖx>\x0006¢	0è\x000f0øRÅ\x0018\x0003'"2!R6Ý¶á43¢/è/Y{R\x00173ã822<í /è/¬E¹¾w3&»ÎÏKÁpþ&À ?Àd\x001döNÜå«íØ\x0000\x0017!g\x001e\x0013aÐ\x001da
7\x001a¬ÌÃ\x001b$j\x00133Â°c<ïÕ&Â ?Â¤"«º\x001d£\x0008ev;\x0006õjØ
Íû1 î Ã\x0002PIí\x0008OÄ$
®	nP&ÈDá­ïBýÂßÄ«ã¸ðóm4A&ºL)ºü+Ò2R\x0019(1cÝÍõû!\x0018\x0013ý1&\x0005^æ¸T'EUï!&ðhëcî\x0018Ã\x001a£MÍ\x0008Z8!\x0015\x001eèvÜuû1 \x0013ýA¦':k£yâE 7\x0004,Ê<Î»	2Ñ\x001fdúE«­\x000c\x001ezL¬*#\x0013\x001d\x001fÙvìÁh¢LôG\x0019RñèNÚc¬ºC\x0013·ÆºÓëðc4Q&ú£LÑóAÄD+aU·.ítZ\x0016Mþ \x0013æ\x0013pa\x0004Qó²²Öòc4A&úLnZ÷\x000ei\x0010\x0010Ò°ãùk\x0002(Cþ(\x0013éIX¿5÷ÒjÁQæ¸ìs\x001a¡1ä19]¬\x00082X×½¨i¬>í.dB\x000cùCL\x000cZç\x0017­,Ô\x0018´¾ù<}	1ä\x000f1ý*-W­þ¿¥ÕFBíÉ\x001b\«É>ÂøC\x000cÊ¦\x0004)Ik «/+3f<ï.&Â?Â¤ª- ¬°¥Rj\x0010\x0019wjt~&Â?Â ®Bëv\x0004QW^Åé<}0ä0\x001d<¬²\x0002X,"Z5#íÆQý\x0018M!\x0001\x0012%å\x001eVt}\x0002¯?Ôv"À~&Ä?ÄP\x0018÷\x0018@Èà\x0002Ø1î40Ý\x0018	1É\x001fbB\x000eVÎ\x0008CãU\x0010ãùKB21&ùcL¼Ä ûÙº\x0019µX\x0006{ýA?F\x0013e?Ê\x0004\x0014Ñ¼Ämy"CN¹ª[ÇÓ^LIþ MV5ñò³¬òÚU\x000bx\x001c1É\x001dcxeOX
$»[º\x0015U¸\x0005q§»äÇh_úýA\x0006Q^XED,/k\x0005\x001cà|¨N&Æ$wá:Å\x0010 Jp\x001e¡0É\x001fa êZ»VÃ\x0013\x0014éÆ¤î\x0002!fïd"LrGRµ\x001boÑñ\x0013¦ðÀN¤Ú\x000fÑ\x0004ä\x000f0d¢Z!Ímc\x001a1Ï¿³	0Ù\x001d`JUénÇ8\x0012GÒJ\x0019òò³\x0018MÉþ\x0008\x0003 î­_\x000bQ¸Q`¸AÁ1\x0000Ý\x0001¦pïI\x001cµe\x0019¸\x0018ñ|¹1øýñ%\v²ä¨2Á¤Á¶[q§VíÇh\x0002Lö\x0007\x0005c·âÈl)ÆQZNçíh\x0002Lö\x0007\x0018^¸$1\x0015mHà\x0017\x0010±c=ÿîm/?Â\x0014=V©ÿ3<h.E¨aÇ²\x001f£1Ù\x001dcrÓh·cÐæ\x0013\x001ee\x0014;vÞ«MÉþ\x0018Ó\x001dE4×\x0002÷MÈÅ\x001f´n\x000be§XãÇhLv\x0007ÜY[V\x001a]n1¨Ç±ÄÓn]L)þ\x0018Ã{Ä­û§Ö¼1\x0014M'òù\x001bB11¦¸cLîIh·Xô\x00013"hÉç\x001fY	2Å\x001fd\x0012lëPAjËA\x001b\x001coQ*&Ì\x0014wÉµÈò\x0016ãPQ\x0007Í\x001cÃ~ó\x001f¢2Å\x001feè\x0012eâe?LÓ!\x0004°3Es\x0018M)î(«v÷SCeâÇòÄN3O1Q¦ø£\x000cAiKàÍ¸±zÞ^óÇÑv-û£L\x000fkyyQ&aÇ \x0018\x0003ÝÀ&Ê\x0014IÔ\x0013Oge­C\x001di´[1áÇh¢LñGLÒ;Aµ-åGÆµ(=Æóßº0Sýa¦\x0013>¨C\x0016\x0011\x0004Þà YÏNsÙ\x000fÑDê2Y\x0007\x0011º\x0019GU_;\x0002¿ÊT\x0013eª?ÊÄÀ*cZ\x0016\x0005Ý7.eÑÓ	n5Q¦ú£LªÃcü·x¾§ SýA\x0006v¨sUT×\x0017eu\x0018ÀÀ¶\x001f£	2Õ\x001fdR\x001bNÍÍ(Y¬¨½oa¿bÉÑ\x0004ê\x000f2\h¬£'fL1zÞé|¢\x0018Sý1¦\x001fF\x0014±w^-¸:\x000c¦N
ç«ËÕÆøcL¨ÂÔJåËázûÏ£\x0014uºZVM©þ\x0010C:G57å\x001dÌz	ç{n0Í\x001faBfw-èìÞ¡ñòv^3!¦ùCLÏÊÆ\x001c5+Ã\x000cÃç/Íæ\x000f1!è~¼ÆmÌrKiTôè<F\x0013b?ÄðëàZ¨'Ãú­qì®níü¥µ ÓÜA&·Ì\x0017þÕ #éý÷aÔôÂy;\x001a\x0002on\x0002çú\x0012x\x001aFKwºÔËÎ§eÍ°cs³c®\x0002Ò( @SåtA\x000f!\x001eþÑdT«ß«l<\x0019Z"¡¦o°£ÔüãÄµSÇªê\x0003\x0011t !äÝ>\x000c?H;M\x0016ü\x001e´wyùØR§ÇRãøØçAÚa­àw²L­ÿÈwÃõÒ:>w:ýü\x0006vÖt_eÔFûÍz\x0014ÌptÊtúÁ\x001a®FYý³¬¹G  Qw´`\x000bºkÎî«AQÿ¤h^©{\x0001Ù¯
«\x001di·9Í\x000fÑº
sIqõÞÚTÅ¨¢á|«\x000c\Í8ú\x001cs\x001ak&yà¿ÊåzL¿\x0005<Ý,\x0003W\x0013þ\x0011ÂLM÷òÍUzoQW\x0003óÝõ´%í\x001eøgôrRôFÃ2+FåH8=º\x000cx5]íw\x001a\x0002}>âi=a4^á\x0000Ïfg`GËÀ?[cáF5\x0015¯:·Ià2ñé§Â­<\x0017ª*º¯ÝZFÁù¹Gz­õ]w;ý&\x0013®q¶	ì2ò°É²[Mçþ\x000efóWm¬×Hûõn\x0002jD~þX'¹T\x001aßµu,ü\x0006Ú2®¡öO6óñ#oáÒ\x0007\x0011	å\x0004y\x0014òËù"\x000b^C­8\x0003\x0015³¸ÔRVËZVk4Êjç§¦êegkY\x0007,~r·¿¶Ñ)Ç#rÒÈÐô\x0012õüàT¾ý0KÊ:ç\x001cJ\x0013\x0001@^zé·8ßË°Ù-!0tÃ,ã\x0019>¡\x0006vÒÝ\x0012	Êyx\x00053úarïxÊc:ILÖØ°Æy§ë5AtY\x0013ô?~ûãg÷o!\x0013´øtSa"×öû/}õ¹]·t½\x0012.+~\x0013NOÊA\x0005£¾wñ¨õ\x0010º\x000e7GáÐ\x0016\x000e\x001d\x0013\x000c~Ä_p£#·\x0014vMGGá¤-t\x001cNV!(Ô>-®7©uv	âQ8y\x000b'\x001fdm\x0011qÓñxm/¡Ý\x0004ÿQ0e\x000b¦\x001c\x0004ô\x0015r&ª:Ö«$q?¸v\x0014NÝÂ©GmÒ&xåMÑam½º= Îv\x0014NÛÂi\x0007áP\x0019âRyÌ·'\x001cJ9×QÀütÿû_>}|\x0014Ìå\x0016Î`ô\x0012þÛß*=Q½0\x001cº
Q9IrÎ6\x0017í¨\x0005\x000e\x001c7L2g\x001a#XÕ8i×mv\x0014ad8JÉý$\x0007\x0019P¯UÔ\x001bù$\x000f­2Åc(\x0019r27p\x0008\x001e\x001aª<z©ª,»Á£x\x000c'ÃQRNA®ÉiÑå/b\x001fm»ÓQ8á()Ç(Üy§ÕaÙÓlH\x0019²2i3o¿\x0007êü`\x001d:?×%££h\x000c+ÃQZæÃ#ÊMQWÂs*7íf\x000fÂ1¬\x000cGi\x0019Ç¸&R\x001e¾\x00158\x001cÑ¬y\x000c-ÃQ^æ}}$\x00123¨û/yaÄÙA<h\x001923&y5êö\x0019u2¾O=Ìh¨\x0019R39<^"§
\x000eMG"ìêvGñ\x0018îÁ£ÜÃ»\x0000ã¸¹+Z$ÐlÒÆÙñ¨³Ã÷D\x0008òöCZé0\x001b)Ð8;\x001euöUfÕ\x0004\x0019ºTé¢	2éíh¼\x001dz;v%ÞÆ¤SÅU§ðcM4¢ñ®xÐ»xfÖú¤²¾wb{,\x000fûM<Æ»âQï0Ä\x001eZ\x0019çÑ²ôBÎá1O<ù°}dE\x000cÛ'EµÏ0Ïäñö.z4ñ	ùb\x001eM\x0017<a;¤Yv
ËGñ\x0018ò\x0007Éµ¾$ÓR/Z_mÔ\x0010&\x0013h\x0012x4ñ	Qu½5³ÄÛ\x000bèàl]Ñpa<È<õ§ÞÅ*5rz0b-eDÃñ(\x001b\x0006\x0010éO¨IÛ´7sÅÔ\x001c
\x0015ÆTÈ³| ÆAÇálG4 vÂ1yO<÷°§«ZÏ¦\x0008Ó¥\x0008:YX!ÃÌtË(#²ÔeM\x000b÷­·GÑ\x0018^¦¼\ZÒÚ+<'k×7ÖÝ\x000bÖQ<é(/_ªrÀÕ\x0003\x0019\x0004E½Ã²{â=ÇVå\x0012aÜtµà!íx¡8Äúö\x000b¤Â1DH\x0007ÕÚ¤¸ÂpTå<\x001eCt\x0008ûµOã\x0016w-I@}\x0008Á4{É!Ã=t{F§EÇ³´ìZ\x001cL³\x000cùÐQòIMÆ4\x0013p+¶¾iã<}GN|ÒQòá,ò8²´0Ô<ÓÔdØ'\x001deTXy`ÚÐA£Y\x000b#Íâ1ì²O*_£+´M\x0007§Ë=É$é`RXdo\x0017ôë¨\x000e+fÍÀp¶R\x000c\x000f¦£<¸Ê\x0010)\x001cZAï['ðØç£DJkB¿
\x000e!êÜ.âìsI2D\x0012!\x0015nÄ^ñûÖò¤x&\x0013ød2Ât0#,4\x0006? \x0014%ÂØz:îú¹â1Ä\x00123=A'¨ZÔð-Üõ\x0008\x001fÅc9\x001d%f
êé\x0001Ç°:\x0017Ì^³aå|ãè'Éj\x0017
\x0011Ù³
+ç£¬e«"¡ýÜC\x0004\x0008ÃNý÷(\x001eÃÊù(+÷H%°ÀS¨£`\x001aDÃné(\x001eÃù(\x0017öØ öiZöî¿Õ µ£=
ÇPa>Jõ\x0011'ð^hM\x001a#^ûîû£pìKíQ&ä:³´ñÔñÍ=°jÂÇQ<	óQ&\x000c\x0017	Ï´R\x0018©¶²Y8\x0008óQ"ì_\x000b´ÙecÒÅ\x0003°\x001f:9Ç\x0010a>JTÀ¨çªuÌ\x0012¦:é[ÅPa9J :\x0012fê¤1\x0015¿ßu\x0014áÂr\x000bÃÈ3zæÄ#MëlËð®2¡\x0016\x00139á¢W¢MHC\x00192Æ1\x0016[vº]Gñ\x0018.,G¹0ä¡\x0002Ùï^¤Þ¥uæî]9s1dX\x000eaæ[¢ª@<CgØólgF1\XraºÄ[Úð.5Î,\x0015\x0016Û·r
ófõ\x0000]TÔÒ\x001cäÙÛq1\X\x000eraæQZñæ'@3dD&3øb°\x001c$Â|Ù¸\x0019"ªX\x001cWõMVªaÂz	óe-\x0016/ôU¥,\x0018Sûñ£xL\x0016V\x000ffa¹Ê\ßý×q <ì³Ó{=güùÓòoÞæ\x001aü£\x0004¤j4eì²Fx¯/9Át`/¦\x001a­Â¿Ý\x0015.Û(QÇ
\x0013ÏùhûÜäu¹¤kcujô\x0018«êÊ\¥\x0017c)?¦ÌÞá[Øµ±R;l­Òý
.ê¢lÍ¯,2ÖÉ£\x0005ù\x001a\x0016äã\x001fi@ÞtSÒ\x0013?6¥\x001eÊá¶ºëOØ\x000eÁ\x001eNUB\x0016{6«»bql¸Ù«W\x001f¾º^ZåòúãÁ¯\x0007
×+iF[Féc?\x0004s\x001cÒý\x0015¤ûÿ/Ô®ÏS¤ãÇüõ¨ZÒ5ª£ê\x0006\x0012ÙXµæÉ3.J	m¶uG	Ç\x0019a¶ô@¨¹Âó\x0001_´\x000eQ/
I\x0017yÍÙS\x0005»\x0000\x0008Ç\x0003 \x000fyhKi\x001b>Úe\x0007éìYØªãª®ÚÚw;\x0016Hé©ï»-u\x0017ÿêa[-óër[¡8äp@«êÝÏU%¯Æºèeä±¥üõ\x001fßþòïïÞ~üøø¼\x0006¿\x0005É\x001daUÖ[OUÕ}`±µÝò×¯¾zöæ»çÏ^¿þÜDI¾\x001aÕ``è\x0001\x0006È÷¹\x0015Øx­(M\x0017\x001dØntÌ\x0005,nEÅPv\x0004-\x000f6ë\x0015»A\x0014×.Qwá¢-.r\x0019¬¬LºJMF±
:®r}æ]¸Ò\x0016WòàB\x0015XZÉÆJ8>ä®`é\x0002·À²\x0007ØHG[AèâõJAK	ò\x0004°²\x0005VÀääó\x0002 ª¸¢âÚ\x0015]¸ê\x0016Wuà
ÜwÔV`¥¨ôfÑW\x0014êäúNè\x0002Ö¶À\x0007XÓÆý¥cbÍlt÷Bµë@òÀÚè/äËäÇ1\d>»ç£léb°"\x0015\x0018
\x0018Î\x0018\x000c,ë{h\x0017¶àÆ\x001ba\x000bé ã/yÇ»\x0019Ö\x0007\x000fíó\x0016Àµ?ii+\x0013Q»RPÏXÜU]È\x000cí÷\x0003ïØÓ¹üqAVÃø»ýÑ.døÁÃü·\x001c£Ø,ë\x0015¨d5\x0019í\x0016Â¹\x0019\x0005\x000fÃµõU\x0000VSXASd»×\x000f\x00172Ã°à¡X.Ö¬ÉôÁ\x00169eÒýO!íi\x00170C±àâØ~­\x0006ÁUU«¥ä8í\x001e?]À\x000cÅcYÕO\x001c²®oìäQ\x0005YÙIy¡aYt±l
¢¹´L½Èé×ÍÀ|\x0008Ï\x001c´\x0019¬ËHuwW`rüu¾	Lh?º?ëã	cô<;Éù\x0017ÊØuÉúr²Í\x001cùýè	Mq\byÏÙªf?\\x0012?\x0005íÞB»÷$f0ò\x000cÖ
Ñ¨Yidf§Â¦)ïH\x0018Ð;ïAöÐ¸%\x0012({¤<"ÁÏá\x001a_÷S\x001f¾¥°Ò=b,\x001aï×(ý¸ûWc\x0000éú\x001aLæ\x001aüñÓÝ¿}øõãû·\x001f?¼ÿÌý|­³T
r\x0017ùj>h"UCTw:«îõ÷wÿöê×/½~õòñ9b[è\x0018×*J\x00195=\x0002Ý&O\x001fÌu}\x0010ã\x0016bt[\x0011²Ê\x0012cKÚ =ÝDí·­ø\x001f¶\x0010É
\x0011Aj\x000bË?êJ\x000bþÐ\x000f]I}\x0010Ó\x0016bòC\x000c\
eï©¢í¤µ"JáÁº\x000fbÞBÌ~º»»[±©,\x0002bÕ³Xw\x0012Y~e\x000b±ø!õ&M\x0011.2°(C§´\x0008\x0011EX·\x0008«\x001baÌª,d*ßyDbj;\x0019o?Ä¶Øü\x0010I5-cw\x001ciæÄ(£Í öÍ%ì%û FÒV\x0007â\x0017OùÐªìÜ­¸SSñC´ÁÅ\x001f]:DQÝU\x000b\x000buèx2ñ4F\x0013]À\x001d^r\x000eòÊN¬t";ï0«Þoz¸$æÃhÂ\x000bøã\x000b5~x\0r)v-\x000c/£\x001e+Æ}¯³\x001f£/à\x000f0¼,9\x000f\x0011fT6âéÓN
Û5ßÑ\x0008G>Ñ6	Ö¼©]ò¤~oÀ>`²Æ\x0005è6i<øè\x0004/ñCôuBFô¼÷\x0004¼F\x0013Hs(#EëwfÔ,²)Ò}ÏÞq¤\x0015¢MtyAJÿDOþù\x001f{÷ÝÏoß½¿{óágFó(B^½>ÇF¦Å{:/cS±D£2ÿôÅgÏî¾{ñìùË»7¯^ð¯~\x0013\x001fnñ¡\x0017\x001fË-­·\x0018bõvÁÒâ\x001cK2¹Ï\x000c¾¸Å\x0017½øx`tÅJIM\x0012\^­\x0014OÂ£-<r^UÜÔó²µµd\x0012j¿V\x001bÁ¶ø\x0017\x001fVYõÓñ)çT¤i¯Ög?oÞâËnûõÛÁâÀ1\x0005¡Ôî\x001eIÝ£÷\x0019|e¯xñÅÂW\x0016Å·\x000e\x001fTK\x0019ø¦Ï_NWôÞ£ÿôî§O\x001f>Þýá×¿~ø\\x0001\x0002\x0006µ\¶½\x0014ôÛîúqÿôüëï_½¾ûÃ\x000fß¼úm\¸Å\x000e\=ö®\x00037\x00153WUÂ\x0016\x0006ã= ®âÂ\x0015·¸¢Ç^5J§^§âÀ/\x001fkUU?%ìÊ½.\´ÅE\x001e{EB\x00126\x001a\x001f\x001aTXO`w7'\x0017°´\x0005<\x0006ãu£0ÈCËºª\x0018N°¼\x0005=\x0016\x000bUä¢w'J'SCy,ó	`e\x000b¬x,VTÇº+Ò|¤diüây¢Sg¿nU\x00070\x0016XÐX[ÕñÛª«ó"â.Kö\x0000»\)\x0017\x0012\x000b.dYÒw^î¦Ëª>tGÜ_\È\x000cÇX$¤\x0015YÏâ¤¶\x001f3É=`wÏu\x00013|\x0001\x001eÂ\x0000®Ú·\x0015X\x001c»\x001aûwS\x0006y§ûêBf\x0008\x0003<9jº´E­µ"Çìû¢\x000ba\x000cðP\x0006´eÄh±Y(ÚIÔ¤ï¸§;É8\x000f04A\x001c=Q\x001cù²µFñ%\x0017Ok¸\x0004)Jñ|Í\x0019öG\x0013.Ñ\x0013/\x0019Y¥\x0015Y
²4©\x0005íV#Ú-¨u\x00013ç\x001f]ç
¤\x000cK\x000bzÊj·¾ôîf\ÈÌùGÏùg=_ýIÞZÈòÔÍÝ÷§¾¥Kè	Lý\x0017Ú¶\x0000´t\x0016­È¤øÐ?ænÞ¬\x0019dÍ\x000cÈ®ðwµÜL\x0019î\x0006\x0015<È¢ñÌèñL¶Ùª \x0011\x0001TÖ±#">g\x0012Æh\x0013Yg¢>v\x0003Æ'Q9Cû\x000f	wÍ­.dÆ\x0001¢+\x0000TËð\x0014dUÏYØG¸\x0019\x000f\x001e\x000f`ýæuv:ò¨{Å+d\x000fÈ\»\x0019\x000f\x001e\x000f`d\x00124¹#«é×\x0014ÁE&8ã\x0001d<\\x001e\x0010XF\x001e_\x0010{f¦á<¶Sç\x0007Ç\x00035¤îÂO¨|&ÃÃËôì\x0019dÆ\x0003Èç\x0001¤í\x001eÜÒäú\x000bM²Æx*\x0003"ã\x0000äs$Óñ1`X\x0006¦Ç,î\È\x0003+\x0004@õcqY\x0000,Fx±çg>f2\x000e\\x000e06wd [¨[Ðµ\x001aìÍqär\x0000¨\x0003õôz\x0010m\x000ezÌzóÈlÑÀ\x0003ñkº3Ö\x0015V±í\x0006B\È\x0007$W\x0012(mu¸l¯\x0014:ËQ/Áe7|èBf< ù øDê\x0019üH0²3­gäSÙY6\x000e]\x000e4*-ýZÌSqÙþÿ>\x0015\x0001²qì\x0000U>f÷R\x0012ÒÈ \x001f;_O 3\x000e}Ê]~ã5¥3\x001aÇìL\x0008ÈÆ\x0001²/\x0004\x0014Éºk^òFTÒÀýÓ½\x000bqìË2¿­tEá ³3Èñâº¯éÅzÎªvï·*Oýít\x0018]È\x0007\x0014×-ß&² \x0003i@l)_\x001cà\x000ci\x0014ã\x0000Åã\x0000,û¥ØX\x0016Ú\x001b§\x0008RÒÛmv!³åY\x0003@«¢ÚÓ´¦Ê\x000fìZÒÛ)Ñ»\x0019\x0007(.\x0007`]_Fæ;ÔL_' îF«=Èªqêr\x0010å²¹VÎÖ¶\x0005Y\x001fÉ³\x0013¸ÐÖ\x001aÑWl,Qæúª®èô!\x0019Ê©û97}rãï>yÞæÚ\x0013}UGÕÚåwk}õ§3Ù\x0002\x0017ÿÔîÃåÐujwÓê<^ãrùê¢q'yà{\x000c»\x0006H>|ÌºQ"Uª*îÓYw¤j»¡)£î\x000cØ\x0000ybDjð¸lO^ 4È? Ùâ{}½\x0006N|F¹\x0003.\x001f¢\x0006Ôxê~ÀFÖ9~ô8G\x0019¯d9éÊè9e:¸L\x001d¬Ðî=Ð2\x0017ºWh#Ú$­O\x001dÚn\x001eô\x00106\x000cWêý\x0017ü¨þüoÿ~ÿË/oïþòëÝïßýòïoßÿrÿî3Mý(­\x001anÖ"8·#´*JATÌ=áù·ß=}óæÙÝï¸ûýó7ß={ùæéóÏuö+È¸\x0005\x0019'@¦ EÀN~Y\x001aD\x0003è$Ziæ:?¶(i\x0002e\x000e²2\x000b+\x0008L×m*Õ¼"ÌÂL[i\x0006f\x0016¹Y~	Ò·î\x0010¡\x000ek¶\x001bÀÌ[y\x0002f©Ò(Ó­*!\x0010Hqÿ\x001b\x0015ÚYu\x000b³NÀdÓuCr\x000e¾Þ\x0002SKMTy yy\x000egü\x001cîÆÙ\x0013U=tú©ßcô«\x0017¼Áá\x0004CG0ÃG-ñ·^q.{h\x0016Y'ÈJ¹\x0013Åm4\Yá÷¥&«h\x0019K\x0001ñ%\x001d_,ÕÜ½h{^a;º¸DRí¿¼ýåîéÏ?Þ|ûóÏoy\x0014b¿ý¨\x0015ÇÔ´\x001f®ï¸÷\x000brßÜ=}ñÕÓ×Ï^¼xöæ·Ñá\x0016\x001dzÑ\x0015\x0015¤%¢ÃÓeò´¤ò¢[tÑ®¶µW´ÛN\x000f:8\x0015&\x0016Ê=¶èÈ.ó<Ç"SµÄQÒØBûÀÒs\x001f¼´ü\x0007O´c\\x0014ÎWë©Ì:í/z^xy\x000b/{­\x0017d^p\x0011?ZÅÿ
Å±#­>ze\x000b¯xá)_sj-óYýãêv\x000c»\x001e>/¼ºWðJ\x0010é_LQ\x001aú\x000b¡ªÆÝ]Å\x000b®mÁ5/¸:ö!GWÆþiUnâNÌ	ï\x0012\x0017F\x000eN|I\x001f4x/\x0014ÊEð?¦Ý
(/>\x001b1¼!£hºÍe"\x001d1 ¼KÝqOz.\x0001Þ T]åöå.Ïÿ°.\x0014»)s/>\x00135À\x001b6RG¾5¨Éù\x000bª`F°[9æÅgâ\x0006x\x0003GD}ã\x0014k%f^¨"æÃ]Ë\x000bÏÄ
ð\x0006\x000e\x001a2çÜÉ°,v÷ ±z7ãÅg\x0002\x0007x#G¿5n5Ô"ªk%æ±9¶\x001cà
\x001d¬Å(Û?¹}ru¢ªúhÙözñ\x0019v\x0006/=Ç±t\x001c¹§YßEt÷hêýÐË~PU\x0006\x001cÐm©êzÐ½X±\x0017a\x0017ô²K¿f²_\x0015-\x0012ôøÅ$\x0017q_ôºï\x0010bHË\x001bÄÊ~ñXá®ÉßÏ¸\x0007zÝ£|Á§wdÍ\x0013çàý\x0008\x0011Íuí«þ\x000b¾®}ýá×\x001dÛ/Þ}V`2\x0007]h\x0015(¨Þ\x0018Ö¬jªÙTÐ¿~õÃë\x000eëÍ÷Ï?#19 á\x0016\x0012~\x0011â\x0016R<\x000c)H+¤mÌ³\x000cµ¹Ïú Ñ\x0016\x0012}\x0011VÊ[Hù¸T¼h\x0011¤\x0017es,\x001a¢À\x0008»\x001eB\x0014âµLK\eZþçÛþOÝýáíûïî¾ºÿøã¯¿üòIY¯¸ Þ"HË@U§ý¯¬õôOÏ^v\x0017üÃ³¯ßu\x0017üê7o>S1×B-q\x0015jñM2ôØà"ö\x0006H2WëIq\x000b2ºA²\x0008O«"êEú\Ù©¨Ý¿9	¶ ÉoIÃ<¼§+}d¹5½ÇNL[ÉoÉ\ô¦´rQk*u\x0017k;\x000f²lA\x0016?HQï¬=goÂ@xãX·øêcÉÖZA\x001f0ûW\x0017Ý\x0004°\x0002£ Û\x0016dó\x001b±\x000cQÃRQUP9f¬fD£2ñR\x001c"âµ$ß*Ä±³nå¢¡ëpÞ©Ár¸Äk\x0019\x000f®¥>\x0006÷ëÆPm53&Q\x001a\x0012\x0007?W¢qÄ8Õyh~tÞ«Áð#ø	
\x0001DmÖ¯TFf<\x001f\x000fÁ\x0010$L0dMÚ·\\x0012\x000eþ5ÇÖnñÁ³Ag(Rz;}Ý¼ HyÎó$\x0018\x001e	"¯òäÎZ\x001dÜp´R¥¾k:O`¸\x001cüd^³.\x0006\Ô¢Iv'÷~Ç¾\x0001Q\x001a2	6oYzÜxØ^µs\x0013é KËtþT¢¡sôÓyÍºr\x0011bÊ¬4\x0004ñ<
¡atô3:§¹"©j#cÊ:ÏÚxRä4JO0z\x000fßUåè\x00075îÚ2Ðùc&/GbÞ¢.þ\x0019L ÖTÕýoq/n\x0002\x000fN\x0004¢û¼Èºg\x0003ux¡µ\x001b|p\x0013wÐ\x001fw\x001a/*\A¦_ÊÉ\x000cª\x0018Qãùl\x0008MØÁ°Ó#H6ÄúQ²q&nHå\x0006¦4a\x0007ýa_%d,¥¬ê.\x0019uô¨b8h ¡tôSz\x001bÛ_b¢tA©mË\x0015n2\x001aJ\x0013^
RnªÒÔ¿¸h	w[Å¹(
§Ç	NïÑf-´ÇÄkÒVSÆÑzh3&A\x001aJ\x0013Þ´&æUûj1¥Î7¸Aú\x001bm¥eÑ{\x000e\x0014@gÊk&µd¥\x001b4\x001eýÞxc¨\x001dÚâ\x000e}q'ûyÑã\x0004£× 
\x0000TKó\x0010'*%ÏÙ¢¡ôè§ô\x0006 Wð¥ãTn\x0012\x001d¦Øò\x0016®c\x0018=N0:_ÊD­%õomíêÉ&O3¢¹IDÿM¢Á\x0010´Ë=ÇRt*¨\x0011¼ÜÀÁÉ\x0010:ù	ß$e¥Jâ7gÉØ\x001cÊJ7¨\x000b¡JòS%KSÉ\x0016Äsý±µ¤2Þ  A¶à;AC\x001dKÑ<£hH°R÷yÆ¿iÂ¿¹\x0005G¾7eåÊ\x000c:ìY\x0001Î\x0007p2¾C\x0013¾tÉ1·\x0004écW\x001e£ÿ¥µó\x001f<\x0019ßI\x0013¾STí¼3zÔÙ¤gÔÁèçA\x001aßI\x0013¾SX\x00015ÔÈCz¥d¼\x0001Hã:iÂuXìD@òíL\'©ï\x0014*7àJ3	$TÄ¿qûy\x0010UÆÇ%7 ¼7xØ;¬q
kmEuGòe¡¤&ëxd\x001dá\x001a)ÂU£¾¢,²è=ËHâÎ
ñÏ?\x0019£þî'mtÿ\x001e/\4.Û¡ê-²ûüeÊ¨ÿD	Ìff)hòoÜGUÛ{XrF\x0016Û§¡ÁÚè\x0006\x000fíÚ®ÐæÜê\x0015áÚ®\x00083vm!«ö(\x000b¼Þ3Û`\x0001<áXT¯#ú/tRãÅ_ßýr÷âþ§\x001f>}úëz¦
Që*Úv\x000bû¶å\x0017¯~xþæîÅÓ¯_¿úþû\x0003ðp\x000b\x000f]ðúo·ê¬ðâ\x0018²T]Á\x0004´STðÂ[xÑ	/j\x0001;±bÒØ£\x0017µ«µìE¼ðh\x000b¼Ö¢KX\x0005W·éi*`·àÕ.mÑ%':ÒÀe¼I¢èâ^1Ø\x000b/oáe¯ñ6Ìó&;ZËþ\x0005ekDý²\x001a/¼²WðÞËÒ²4@·¡ö£ïÕv¼ðê\x0016^uÂ\x0003ÏNá²:¾èo¨;18'¸K¿ÃBzÁ®s´³òftù´£\x0015Z½nÇôÂ3¤\x0007^ÖCY\x0017Ðé·r5u'¯µ	i7ªágX\x0005¼´µ\x0010Ý\x0019$lVÁJ35\x0016¸VFñâ3\x000b^Ï\x001dÃÆEeoN
Òp°íD¼øk×7bÎ¯¥\x0019X\x0017cªæMÇ·Û¥èÄÆ;Ðë\x001d=ªÉ|$º\x0008¼,*Û<s2l M	ÜÞQµ\x001b\x0017; ]ø«%çÄ÷³)ËE\x0017bMZ~tg-«ª\x0017·à^»Uª½¬\x001fáO\x0016áO¾´¯¡H\x0008-½º\x0019èÆWMÇÞRÁf¥,`Ã
éÿëíßÞ½ç)ç×ÿøû/o?þçw\x001fïþòöîçû»7÷?þüî\x001fÿõ¡gäF?I\x0004YÆ|\x0005Ü-*o²©ÙÝ_ÿáÙ·<ñüúÙg¯ÿôêùë»ß÷¿ÁÓ»7O¿zñüÙg\x0017C
|ÜÂÇ³ð©\x0014ÕR\x001eb!<
/¹N!³
ú<ü¸\x001fÏÂÏý¸Èx
w®ã\x000bAå\x0012gE7EO[ôôßÎøi\x000b?ý·;úy\x000b?ÿ·³~ÙÂ/ç­¼hbµ¾ê \x0016\x0018S
-\x000bòyøu\x000b¿ÚðÜ\x001ctl\x0015¼)öÃo{xÚ\x0016~;o}\x0010uÀný ýÝ\x001d~\x0001µ¾\x0019{<
³U£V8oþ$Oº\x001dÖÅdEw±nßFÝÓa÷_í¼`Â.»%EU4`î\x0014E\x0003ÈeØÿ¦Î\x000b&ìÂé¸û¯61·¼%èäCâ¾x\x0014÷çTm\x000bËYø\x0000ÍþÓô¹iÅ_ZG¼æ=Iôûúj·4?DË>ñ4ýðHÞú°Óñ7emMï\x0011ái\x001b4K>í4ûtóJ÷`*%KcnzOî\x0019Pº)þlñN}RÓFÒÔó\x0005¹©vü¨öOFÿñì_\x0000mÞ¼¼0ü\x000b\x000c-">þYì4÷©ù¦ôIÙ\x001c þñ4\x0006é°é7î²\x000b³P\x001c nI?:óg]É\x0002\x0002?Êêº?â¿)R®ö/p:ûdÙXÁ_£ô?äÒýs¼åùOÁð'ÿx\x0016?7ÕKü­Àú/Ë_@Gry\x0003é-\x0019´ ù\x000bðgÿ\x0002¡J\x0019¾p/à²x¶3h¹
F¸Óñ\x0014ùÍý/>¼¿{ýö¯ï~¹ûÓ»¿¾ÿl'BÓ®ö@zb8Ìê®´«K}óôÍ÷¯^vÌß<s÷§çß¼<\x0000\x0013·0q\x0006&H3¶6Fµ;+LØ½ûÍÀ[q\x0002&OL¶:Wp¤G
Æ\x000eS¼\x0005JÚ¢¤	iY|eq´Êä Ûyí
`¦-Ì4\x0001³¦ËÚ"\Úx\x0014C¹)ó\x0016c1%u\x0012Ü\x001b!çR;J#ìÞµfP-ÊâFÉ\x0003S¢]±(ÎI\x0001?gÒ}4aWÀY·0ë1H\x001d¬Æc9öùÀM¨¨mQ¶/ÔÇ7ÓåpymõÁT\x0005EBRNfÆ4üç\x0006Æ\x0004Ãëà'v
"o-kÆ[s\x001dë(öþ38
eÂ\x000cgV\x001cg³TíÊÎ±\x000c\x0017
×O°38
\x001fþUö4®\x000e~_ÿ\x0017áÆ¢ßþE8­nÿ#©n¿/Mª\óY";1Ð­KgbÜ­\x00102ªéÕ[
Ë¿ùBm\x000b×¶IÛ6	õ=S.²×³Ûvl5Ì»Wú9ã^¡íÆûÏ6nº~ûI×o?ßÝ¼ÿË»ÏH´DÀ`,ë(¡I¯&õ;Ôõ]éùK¾-}÷ôõÓß?ÿ\º~ÙI×/;¿
®íµçx%ïÚíU@û \x001bLOC\x0003\x000eèJã¾ ë./ê{¤"·Aw\x0019r`t\èj@VWZÑÝ\x0014¨Ò)Gæ\x0019t\x0019·è2:¿lfµÌ\x0005]\x000e²Ó¾Ù¨èj¹®ñøÐ`|"8¢na?w(=\x0005,`éèÂu\x0005Ðûe·ì-_ã\x0002ÙM80fñ\x0010oIß ¼n°ÆQÕøãÛû÷wzûñýÛOc½ª\x0013_ý§Ñé\x00052XÎ\x000b®o:|öôåÝ½~ùìûß\x0006[`è\x00022GSYÐPG!\x000c\×
h.Xq\x000b+º`®®¼·Z:\x001fù>(cé:J¸Ñ\x0016\x0018yÁXDTYôE:Fuð¨\x0003Ûµ\x0014º¥-°ä\x0002V\x0000ZÇ¨MÔôK&<õ)ó\x0016Xv\x0001\x001b'\x000cÂ\x0018ÈlEÅºh§WìÂU¶¸\x000bWW,¶/BÔÝ`ºd7OàU·°ª\x0007V(OÈÌåÕ^AaÙ·.7°¶\x0005Ö\ÀªßÔ°3®Àâø»µÆ\x001e`>n¼T\x0016 ¼(C\x0006J«ZùÈE]2îVZºYÒw°þ2S#òÜ»%,	PÝ\x0019\óÁAú¦ÏÅ`²6(!D\x0018wE\x0018\x00172CûààýÈ5\x000c\x001c\x0002MGPãPH¤S&3´\x000f\x000eÞïg\x000c	Ì¨\x000b-s\x001elA»ò\x000bá}p\x0010ÿRP\x0013e\x001d\x0016K\x0013QÉLYÿ¾ÖëBf\x001f\x001cÌ¿Ô¦TØ%käcV\x0005§r\x001e0Ì\x000f\x000eê¼Ç8¨_~OV¥¾°[\x001cìBfÈ\x001f\x001cìß?f\x001cÈú]J\x001d´å^¾ÜÌ°?8èyAµ\x0019È\x00134\x000b8
ñ³t\x0006\x0019\x001aúG\x0017ýg\x001aºe4Ùç±\x0006+°^×	dÿÑÅÿ=GÕÞÃ!Í\x0007Ï]­ÃÌfý®\x0008µ\x001f÷1Èn³ \x001e\x0000»%+.dhÑE´4òØÂk~\x0004\x0019¤Ag»mË.dÎÐEg²Ô»ÓÙPåÉ¡\x000eßÜU1]È\x000ck 5XRYV×LÔÊM>&l£J
ô£'mä¬h\x0010¨ª/\x001bó©à® %\x00074ÞP¦
½|Ô4Õe8\x0001\x0002·ÙÜ*v»÷Ø;¸n\x0005j¸\x0011	h·)Âi¹û+Ë\x001d\x0007×#;¨l0\x0013\x0016qÓ°\8u=Í®j±Ü'Oí jªVjz¢âã»yX§á~º2ÜOÌ[5/5çÖÒhØ?Ô9a}ºuÜd±_â 
,W^ "í\x0002ÝÝÎ¨CàRm¶nÆ\x001d,%øóÏÿøûÛ»ßÞ}ÇO\x0007¿~|ûóçÊ¶ \x001b·úÉØ\x000b4	LÍÓ\x0017/=»ë?}ÇÏ\x0006?¼~öâw?}øÛß~}ÿVÿû\x001a\x001dnÑ¡\x0013]iA[;Ùeeß\x00114\x0018Â\x0004vY\x001b]Ü¢^t=UkkAõ»¼SÆë\x001e¼Ú)t´EG^t)H	\x001a%Ï-\x0010uUY°ËýèÒ\x0016]ò¢c)±\x0015\x001cïÖjrÝ\x0011)äpîØå-¸ì\x0004¹#Z\x0002®\x0001\x000b\x0005Æ5õx?º²EWÜ\x001fvÝ\{Ê´.Ñík2».Î@«[hÕ\x000b
P\x0007Pm(%´ ÎyÄ¥µp]pÃÒPH¼æ \x000exê\x00121ú®`È\x000eÜl\x0007ItN\x000b4ë¦Ã\x0016½îÆåSá\x0013p\x0013
éµ
-ÃËÑCÝ÷Ò ÍÁëÎn\x0003Yÿ>\x0000}Å+¿þó]ÿÏdè1ê 88${\x0001HÇ®
þ\x0015ïûúÓóþ\x001føz
'náD\x001fvÑ\x000c©ºr\x0006t²¿ìªßGàÐ\x0016\x000e9àôiÕ]Â8$Ëqì´»2ÂI[8Éc"ÙPSTÉ «\x001eMÝõ¡\x001e·p²Ç:y,\x001cíÉ^ï°èÊ½\x001a¯\x0013Ú#pÊ\x0016NñX'É;5ëSpåeµ\x000eéÇjp+\x001eS·pªÇ:iì¡f1g\x0015å×Ù Ó¶pÇ:pÙ^\x001b$\x001dì©¡Nõë\x001fÍfáo¾¼\x001c³ö§§\x0018Æ\x000bDB\x001d<mWé<ÇÒ \x0007e92"Ï´¬\x0007å,\x0013àÄ×Ú,ôÍ§cö	Ã>=1Ð>i5\x000f¿LÀ1´\x000c.^.º|wGÅ'E÷nc9>ÁEÌ,ñâL-\x0013&Ô¹AÚWà1L\x0008N*DÝ­=^a:K«wán;ê¡@±ím[¶¶\x001dûjw
Js¼P'«e&|ÕkTÕê¶ÄHåº\x0005¦\x000chBzñîÇ·\x001f?£5Ó/ò{ü9;ce!í]\x001bË\x0017{v¹_
ÌcG/õìõgÅpÊu\x001bL\x0019m0\x0007ÁñC¨Ã¨kÛ»çI¥\x0012ó\x0003k³]àâ\x0016\tZ\x000eE>ri[Pí\x0006íHÜW´Ðh\x000bv»|Ô\x001eð@>j\x0011FïØà²àÒ\x0016\rË2E¶Ô¡e×=\x0014}GJ×¯¶Npy\x000b.ûÀÕªE7î`h*	¡w);²w+[pÅi¹¨
»­sÚ\x0000§·\x0018w\x0013\Ý«Np [\x001ca,¹æå¤¾»\x001c'¸¶\x0005×ÜËb¸K\x001b§°.Ôýg\x000f´ML¹ä\ö
^¡¾:^ä\x0011w/¥Np6:xÃ\x0003¨F.¿/ ©Ä\x000b*º´ßlïBgÂ\x00038ãC?hòªÐr\x0019ò?©¨·ÂIo\x0005\x0013\x001fÀ\x0017 ©üõm²\x0015\x001aò8¹*\x000bïº\x0012àL\x0000gè¦SËÑ:tÇ$|Á08Y¸÷æ'è\x0016tTtE°Ýr0Î°0xi¸_JÄtÚmÚ?k\x001e.\ç»NpèÀËtuÐpºP]Çnº]ã\x000f\x001d\x001a:A\x001f°éÔ%ø® ¶]í\x0004\x0015Ï\x001dÚlÓG'\x0015ôÓÇËêâõQKç8 ästNÐI'\x001dÝèÜÒ\x0012JÖgû´kCr¢3|N>¦+Lû\x001d§
¸\Ç³=ÌÔÍÍkMOôæå¡<e`*h¤ÕPv6µË×\x0010³\x001bbÏSFn¬û|X\x0011K1ÒI3BÞ´\x0018¬Ä|ï\x0002Èí\x0019J/YjE\x0005ø¸±+Îxyó¿róO.\x001fîW±*©^lã°%
\x001du'«î\x0006øé
à'w\x0002Ir¬\x001b;\x0005\x000c\x001fyÓ³~â\x001f}x)Lè'Öô\x0013LªÊ\x0015Àâ\x0003XU½|ùÂ(>Ò4%ÝOþ»áýÇ\x0015¼ÿø¢Ò\x0003¸¦\x0019\x0000?ÏüsSÓ\x0010¯1F/DgXoâKy¥ª°j¼ÔW&\x001d¹\\x000f\x0015¼ª±Ï»_>Ý¿ÿé³ÇD4a)²èm¼%\x001cESè×ÏÞ<óýÓ_\x001fÀ[èÇMÔ[Y$6\x001du\x0018ñá\x000fíÁ\x0018·\x0018ã\x0004Æ ]\x0013\x001dd]qñá´Æ\x0003¶\x0010É\x000f1vÛ\x0015	ËMTûÍ¼hXn\x000f§­\x001ei1M±\x0010ñjFO}9\x000fÓ\x0007bÞBÌ~ýB2ÌX¥¾`l#»i\x000f»´\x0007cÙb,~\x0014´±­\x0012Í²Q\x001fv;Æ|þS×-ÆêÇ¸j\x0005¯\x0018Ë5\x0000¢>u»I!?Ä¶Ø&Ì\x0008¢"´\x000c6É
\x001eqTÜè4Ä\x001a0^\x0017Ý`¡%nZk[$\x0005üD#×ÆÝôÐ\x000eãO÷¹ÿåÓÇÇ1Ú\x00183\x0011d¨	FmÚ^]¦\x000eæy¤té1¤	20\x0011eZÐi'n\x0006\x0015¶ Å¤¸ëÙö4Q\x0006&ÂLê_[\x000c	{(+?ÒîÛÑP8Lpø:\¡\x0005~q\x001a]1Üí¸ÛLáÇh8\x001cü$ÎM¡Z`jM	2&\x001dlÀ\x001b\x001cHÃáà'ñ\x0006£Ü_,r\x0008:\x0014°Óóc4\x001c\x000e~\x0012çeâØHlÑÕ#½Íç³G0$\x000e~\x0016ç¹\x001f)ÃæªåõG Ù5\x001a¸!¢!qt8¶D2Î»È&Èm0\x0016\x001d\x001bdßÓ 
£Å#Ä´ÚqY\x000c+?^:ùñ±\x0007£½)øIÕ	¦áC¨#mL»öC?HCâè&ñ\x0008¤«âiÙ\¶&â9èÝ?ÓNæ®þËBãmáê5I/®\x0014FGEx¤\x0002ï\x0001i"
º#M7ä¢ßº\x0018²\x00166/\x0019ôÖ\x0015a7Ôí\x0007iB
N\x001aDà½[rø6ó¥Zr'äê\x0007ix\x001cÝ<¾¨¢ÔW[÷I, I_4Úùd\x001c
ã\x000cñÖ\x0013´U¸·ûöh¹ç<\x001a&\x0013LÞ²¨¸ðÜ¦º£ób7ÉéÇhH2Nd+2p½Ì\x0002JC\x0012éÚÉþG
g\x001e¢b¿§ËÎðåÎ ¾MQÅ\x0007:Èó_ÛøvtûväÕk­rE\x0016·©p¹ÄÆh\;N¸v<v§í\x0005R	OáR	/§C"\x0019·¡[lÏ-FQd6»PÁ4¾öyÆoÈí7SÜ¨Wí¤#*êh#y¤ÉÅ\x0003Ò\x0016ù&ü¦g@ãsÇ\x0011¸ujÃÍé3IÆohÂoX\x0002Gå~\x0012)éRÚm÷ôc4~Cs~Óô	¤qÎê7e\x0018²ÛÉøMð:º\x0002?ö¯á÷S\x000bØéi2~&ü¦&Õwb)iÙ¢
/ ¯F&ã7iÆoð		\x0003u\x0017=BÔ\x0006ÈºÛë\x0006ÍçÎ\x0013»§i\\x0014äy´5KS1/Qeóµó\x000cKêF~[ ½oSV5/l»+?HóµóÄ×î7ñµv\x0000PÕ\x0017Ûùì"Û	Ì¤ºtIsI\x0010ÆûüE1\x001bÌ~\x0004¬ã2FÏLj »ÆXÛ	·Y÷¯ã\x0001m°$ªR ²>ÙYÆoßoúg%¾­ÓÈ%w2H~Æoßo\x0000.,Ù]¨\x0008È¢ªXÒi*/Æoßo\x0000\x0012V®G²r=h\x0005y¡òG+\x001c «±d7YnÜý"Ó/]hÂ\x001bã#]z®\x0017º?ÿÇ¯÷\x001bíÛõ¡N~ç~yÈÜ\x000e¿\x001eOÒrt¿à§ÙHãD©÷ÏWh;	¬\±
4J.Âîý'ÍÜÒùWdÚö¬\x000fò¶7äà{wÏ~ÕªY\x0015
p0|ºÁ;-^#Å)¤³,®ÇÐKO<þèö«óï¡\x0007¾ýÕ1¥SÊbºú\x0000Îß>jëM\x0019\x001fÿüãI¹þøÜ§6ñõû
¨É­^É5mW»\x0005]]a½n=ü«\x0007 ¡\x0008b_Æ\x001e\x001b}ò\x0000Qçl\x001adqoä\×\x001d\x0010q'¯9óý¯\x0019µL1*7ã\º£<ô¶¼#î4¦f¼ÿ§+ïÿÉ×Ñz\x000cC\x0005O4zd¸ÌG¨W6Å)÷áB¨üB¹v:Ñn¼AS[»>¨m.He\x001eÐÖ¤ë ´qPÛéx
;¨0\x000bs:sFÕ8ÔñQO@Íéªå2§KËå/w¯?üíþã»÷[#PË:_2ïúUC&Ñj)üNyîÍÝëWß>}ýüåg¶\x0008(2Ü"C\x000f2>ëHwNæÔt\x000b%îTd|Èâ\x0016YôÙ,è´yæ¾\x001cíyn´\x0007÷<Ðh\x000b\F\x000bÚQÙ­¦Ë
Æ Ð°ìO\x0007ZÞBË.«e\x0010\x0005Êy\x000em\x000cO½´;±S\x001f´ºV}\x001fTXl4ùu\x0018ì\x0014ªM7\x001d»fpÁ*À*&+®*\x00172¨*HQ"íùØ\x0003Íø&¸³d[wO	³¶Ù@QÚ \x0007\x0004\x0004<Ð\x0007Ë\x0005J2Ïµî\x000fÖ9x\x001aØ\x001eè\ñ`3.\x0000.\x001fèÿ'uÅ=90ÃÅ=÷¹ \x0007[1Ø\x000b[Ò)½\x0005JO6Ý[ßaîk\x0014\x001elÆ?Áå ¬ï\x0001Â\x001d\x001d(\x0000b\x0019fû¢©'£&|ö_ün³ûíÝ·÷?ßÿú¹]ÃTÅx©\x0011.á½ÿ¤ê°
MmY÷ð<»ûöé§?|n»°Ã-8t[ô3ÖÜ3\x0003­\x0004q¼³Vû^4-n±Eábá½\x001aá¸z³Ú-k¶6Ã»\x0013Øh\Ø2«µÑ\x000eµÖ@rOä´\x001dÊJëMK[pÉg¸þQãzâr%Y$cÔA·Ê¥Ï3àÀ8ð\x001d¹~Ì:åÊµÇiåÌQÈ\x000fíÎr 3g\x000e|.D\x001c\x00125éÉ¨DB%ö9Ð\x000f\x000b¾/\x001bX\x0004sEG¼.6®èö3f+\x0011;®\x0018tÅwî:\x0007UoZAî±zá.!>´*Ð®\x0019tÍ;V¯ Þ°z\x0005
Â;\x000eM@g`õÕõËÆnÕêÌKSÁ.YÅ	tÆ+Ðç\x0015\x0018Æ¾»´8Ýã¬rq:Ë(h¼\x0002}^\x0011£v+vÛzîSíàòÉ\x000fk\x0002}N\x0011ADf¸¯áÉº!=÷\x0014S¾+YÉé	pÆ'Ðç\x00131ú\x0004òk-åÄa©Ð96üû\x000e\x001d!ÊÜ\x0008Æ&º£ì³wè	pæÌEßëVâ2\x0001èÒ¨\x0012Æ;wLp\x00129tÑwè¸R#Ç\x0010@'d6KÆÎ\x0005±h\x000e]ô\x001d:\x0002íÉ\x0012äbØs'Õú \x0007Wg\x001eÇFÉGÃ¬è¬y]kâ®ýÌ¥¨ñd\x0008#c9òY.w\x001fÕÞñ¢µujºÎ­UgÐÁFL\x0003l¨_Tfho:èK<\x0013+jË^_sÕM\x0018±Ð©ûDÕÓxaY#µ ãçÀ5Päªs\x0001ü´v\x0006Þø×ÊÉ\x000bÁ\x0017)\x0012ÉÃ\x000f²Á\x0002\x000fa°1Ê\x0000ìm|÷±\x001ak#
fUÙÏ©jr×ï<§>.+#náñ·p%\x0001A6¾wxMÔerÊZ\x0003 F§<²µ^vZÛW^Á²<î/ðRSÇmõT¼HÅ8.ÿèÊ>\x0011Tï!òb5¿ëyÄÚÏÝzRÉ\x0016ïãöìX¨ÈÛç%u\x0007þßå\x0014º\x001cñøG×Å¢^·Xó\x0013±ÝX\x0003
h%\x001aÛñ.t\x0001õA±ß·E4Ç1
Õ¡¢bi¥8i%ð1Ê\x0011ä]>ó\x0008Þ\x0019Ã)Z)Õ|[þÑW\x000eH|ÛY/Ü(£\x001c\x0019Ë¨\x0006nt5\x001aãñ.tÝWÓzòRL£¢¶+ñ\x000c§ÀvµÈ«/ -
l+ºÜ9\x000f¤H¦^ÍpÆkaÓÜ½ÂK>ãqñSr©\x0012FÄYwwTÞ4|\x0006_±%mþÙ/ê¨Sâ\x0016cáYS©\x0014pÕÙkNVIm£òDñµZrÏçî?h4Ò¥dÁ¿ñ\x0004Ý\´ô\x001e±qWÕQÎa%«w2SñÙ^Æ}\x0013TòEÐÉ\x000cqC\x0003û²Â­\x0019Æ¯>Þÿõþç\x000fyó!ê Iè°(Fó¶\x0018¿zýô§/^}îÕG±á\x0016\x001bú°å¡\x000fµèpj²Oûý°Nlq-ú°5xÖ%mL3$ýE¦\x001d\x0012æÝZ\x000e'8Ú#7¸ub¶\x001bt\x000bZ*c¡
×
OK[pÉ\x0005[É¥¯	P»´Hp¤~G{¨yÂ\x0001.oÁe'¸ ïeÝráÌ§µª_õ¡6"\x0017¶²ÅV|ØpY··`Ã¬C§=ÆJ§\x0002ö+Æ9pu\x000b®:Á5Ñäë<2´Ú2Ê´;\x0013ÉIh[pÍ\x0007<æuËÁ\x0000Gºx\x000féQ|\x000f¸Í:\x001dfààCªnòâ +óí9UEWN\x001e:°ñÁ\x0017  VYÌ¸\x000c*\x000bÐø\x0006µÃ\x0007]àL\x0000_Òtù\x000fÀ\x0018Ì\x0014\x001d= ûáBgB\x0004øb\x0004DÔÎ¢Pu÷N÷a;ØíKq¢31\x0002|A\x0002ZéÌN_iK	¢×ÔÑ=00ìBg\x00048£\x0004½<¡'y\x0011ìd'uô\x000fu9Ð(\x0001Î0Q{¡WÛ\x0005cæ
=b»fë]èL\x0000g ¢½Y!^\x0002EÐs\x0007»
ÙNp&N3Pt-bºÎv ¦\x0001¨\x001evÏ\x000510q\x0002\x0002ë\x0013qØ\x001e'¢FØ¢ØN&hÂ\x0004:ÃD"Jx\x0004O=¢D	\x0013P\x001eÐ.s¡3a\x0002÷\x0008^Ü'KYÉjMxPU,w2©C{p\x001eaÅr\x0018x#È\x001a`i{`ÄÛ\x0005ÎD	tF@ÚÛÖª¶AuÓ%=tøÀÜ´\x000b\x0012è\x0012\x0018ôTô\x0008\x000bÚº^ÆæÊ\x0007µ0]èL@g \x0014¦#\x001e\x0000á´Ì\x001bmÅv\x000fvÈ^Ð=*©è\x000c\x000f£{àÕ¶­\x0011_e\x0017t9©ÇÆÙ	\x001a®C'×Õ<\x0016ywçm\x000cl'SâhØ$:N^/·:,\x000b?¤&Y¿m \x0000goþ>íiÛ S$`C¬¸×\x0007;Æ\x001dèKDK DÙyx.?Ã¢VM`¿ÛÕÎ¸Dô¹D¿.ÈÎ£\x0014
hÂ^H×\x0004C«ç®Ñ¸Dô¹\x0004öKìHë¢Ê¬\x0016}êiÝ\x0003JÙ\x001etd|NÑï
ü¤½ÞÄÆ¾¨Â âpîËÚùÆµx\x0019Å:\x0006ôH+I
dí°%E\x001cõÄ\x0007È=áâ\x001a#&/HèIñêÀÄ²m"\x00021é!\x000f¨é\x001e\x0002Ùÿ¶vÇ\x0008úùêÃ¯?¿ýÏû¹ûãÛû÷w¼ÿõã?þë3\x00083Ï0®#ËþOD­k·bÜä«W?¼xö§§¯÷ÇgO_Þý«Æ\x0007P¦-Ê4²çÈòDÀúí²·¹\x001fÓ¤(o\x00002oAæ	!jSh?{ÒP[»'+Èl.(Ë\x0016eùàMÛ~yÓºÈ´ð¦¯-ÙÓL¢¬[Õ2µ1e[û	\x0005µ¥îlÉÈEN¢l[mÆYJË\x0017_ûÏº-UÂ´ñó¶Ü,M\x000c«~»Û=Ù·«ÂRÔ«1A'¨Q>oÌÍúÄ°J¸û­Ib×L\x001d¬oví$L40qÆ¤¹6ï(Z©\x0008ª¶Í·ØÎsÑfbXUÜýÆ\x001cº¼e½¯TT'Of1à$H\x0013{`"ø¤u\x0004oS\x0002±¥öQv1Á\x0004\x001f><»24Ù\x0001Ùý]e©ÕL4Á\x0007&¢O*(Ko©ôl|Un«u¾|On¢\x000fÌ~Ë1±\x001aHÖó\x0010\x001aó\x0006i¢\x000fÌ~sIAn6Ý*¨\[¼Á¹4Ñ\x0007&ÂOwbUÙ]\x0016U\x0004É8x\x001dÎr4á\x0007gÂÏÚµN\x0006ê"ëºÂdÀí<H\x0013|p"ø¤ª5Ïî>4>ù1Cº\x0001L\x0013|p&øt×.Y\x0005ÛÕtk_wªó\x0007\x0013MðÁàJ»w÷\x001fÔ\x0010YtÝpåÝ_§Qè3Ñl\x0011¡<UÚ\x0017U\x0011n\x0000ÓD\x001f>{|Å}°ÈE·[sôU3	7	ÓÄ\x001f?<--³ÉýÀä\x000b®\x000c'ß\x0000¥	?8\x0011~8Jêx7OP+³«ÆÜ-¸ÈD\x001f>,\x001dº~ñú"Ù¯AºÌ¨4¼ð3á§§lÒè]nÂè¶z0y×ÍYÑ8\x0013~bf\x0016âDN(\x0013U¿¸tþV\x0011Mü3ñû\x000bW¼\x0017S(S/5ó<è\x0013g¢O¬Z;àÜô`êò¼+u¡I&üÄðÃËwåWx"LtÇrµºþ(Mø3á'ª®	¥¢Ûn*\x0000I¹¨P9¯&üÄð³ÎÁ.ÆÌ$ËEº5õV^ÑH]NÂ4á'Î\x001fV\x0010S%\x0000Ý[VaLN\x0014H7ð \x0013âLüIU¥«sO?&pUØ¨;Ó
>º@q&\x0002õ°#ºÐ)¡\x0016¶@5x\x000bÞ \x0019&\x0000Å\x0000²î´Ê¬>Ò4\x001bÖ`\x001eà<\x001d	@4\x0013\x0010\x0008ibT?\x000fÚÊs\x001fçéL\x0000¢\x0000¢¦\x0019ãådjïx©7¨k	A4\x00130pù±&ðÄùjÌ¬C4ýnq\x001e¥@4\x0013R\x0018.¡H[t½ì\x0006/vzu\x0012¦}û	A<\x000b¿:P
AÆD»5£\x001eÍRÏ&\x0010D3!W)®(+é\x0005D-_\x0014Ï_-ÈD @uÜ»ßpeR¾\x001bS·{æ[<¬@4\x0013úåL©=WyìaG÷®x¬L\x0004¢\x0008Ä"\x0019e)Zè\x0008Ce5Û¡I&\x0002ÑL\x0004¢ ;ìÉñbQð\x0006þL\x0000J3\x0001\x0008.cEuÿ»1õÉ"'8\x0005J&\x0002¥\x0008\x0014efÏà¢\x0004Ô¡ð7¨ $\x0013ÒL\x0000\x0002Ý=»\x000c®«Íº1µÎé\x0006µád"P@q¨¥¨\x0013Mýv¡k*\x000bÀù@L\x0004J3\x0011(d}\x000e ~O\x001aB(ZÉHçý<\x0019ÒL3¤ÉÊ;rWëß¿ÈÙ\x0004\x001dQÌõ\x0006ÏÑÉf!Í\x0010U\x000eøÍJ­©\x001aê©ÝÀ\x000ci¦\x0019ÒÄ6\x0019ÂH\x001eÍu?Ù°faÍPd¦b\x0019Å´}Qð\x0015ªó 
gæ\x0019Îäk¯&\x001dé°¹\x001e%aò\x00064\g¸\x0008£¦TÆõG]'áù´(\x001b"ÊSDTµfÄâ)Ò¼ÓHu!¨\x000fåÙ¤Ây&\x0015î\x0019»j\x0008ô;F\x001a\x0019»\x00183Æó<ÛF¨T8Í3<n5¦¾÷HonX=Ï°:\\x000fv»j(×­\x000ct¾´
_æ\x0019¾Eõx±fÃÁêU¨Þ ÊQ\x000c\x0013\x0019&QÙý^\x0011P¯?\x000b§ty6CòÂGü/b»\x001aÛ\x001cÔRÆÃZ\x001cmQP´c¢\x001bdr±þùÓUÑð\x001bi7¥nÅâÎ\x001e©Á.K*Ú·¸\x000eÑµ]\x0013ÍÙ5$Ý£L1ðFSKRù\x0016\x0015ã\x0004;´06êè.¥±\x0008oGãª\x0019Ïs\x0015Ök´XçÐRÕ¥S|fõm#&-s\x001bxXÈ¾7Tð»û¹¶µ\x001bÒð­:\x001aÐn×Ó	h	òØß2rº"\x000f[ú\x0019ã
ÊòõÏÿqÅ\x0004ÿág4ÚwSj×\x0000ã\x0005nðh\x0014vL0I\x0004uñ§å\x0010°f¾\x001e\x0002\x0015óm·è.ïfýñÊ¬?úÍó(7eh­a"\x0017ºE(Ø5NÚõ_òÀY/+Ä®?M=wÉUë&$HC\x001agßîôúÝå\x0017ªóôo?~üðî·w_÷ÿúî?=±ðAÙ\x0016áI\Oi¿Ê·\x000c×jO¿ýêõ«çoÝ}Ýÿëÿ|úýoCÄ-DtCli}èµf\x0019U_\x0014\x001e\x0005!î6Þú\x0011Æ-ÂèGHº»ö\x001bª­ÐÏ\x0001Ì[Ù\x000b°säX\x0000Ï*lëý¢>cC¦ëAN?Ä²XÜ\x0010c\x000f=Y8
 Ýã°âõ`\x001fbÝB¬n\ðÎï¼\x0016?Y½[!îFÿý\x0010Û\x0016bsC$\x001a«ùxX±Öñ¡áz*Ö
q£\x0015³.»ób, +\x0019Ý¬+-öË\x0010xhp=~êÇhYÑM\x001d\x000cRö»q\x0017\x0018ÎÛÄ)þÒ`X\x0011Ü´XKv>VlUfQ11cÙ-·óc4¼\x0008nb¬yYö¾\x0011dâ§?Ú\x0011N;õFC\x0006ÃÐñ`,ì'\x000bFH¢\x000fÔ1ª`õÒøq\x0016c2\x0018ÓËüÌ½]]Çï;\x001aAE\x0002ÈÏè§\x0012U-ÑA<ERqû¼(JTYf\x0004EÚüp>O=~½O×ãðLz$7±\x0016{å^ÅâFæ¶-÷¥Ýúç\\x0000\x0012	ü±vÎVÆ¨×4Ö.RÆ:±³ß`7à9Ik\x0010\x0015îî]­chövøìq\x0004³u,.ø7Ë@êM§¦)ãnÆª\x0011;ëfëX I*¶®hÑ$çAÄ\x001apÞcg\x001dÑl\x001dqmP¤\Z%ñq×\x0004ogìF³y,TxèÑêe²è~ä(z.ÕÉà´ÁÎ:¢Õ:zè)ò©Ã\x0012ý0b½\x0015È2º<ÿ¥;ãfãÈ¡\x0012vE§\x0011Oýù\x000fÝÙF´ÚFïx
]jáÄ:Z-'¯/j.çãfx;c\x0017~£9þ.¬w$1;m4Zà\x000c°ímGìÌ7ZÍ÷?g\x0019»ø\x001bÍ\x0001x©n0käX8Íº,£×\x000e z¨ç\x0019;\x001fV\x001fãY;È*SR=îs\x0018\x001eê|\x000cÙ}LÝ\x0011áYõ¤rl¥ìõXO\x0013Ôù\x0018²ú\x0018_cDÑõ]"4)(Ë¨ÅÂ®ìÆLÛ\x0019ûk¿Ù\x0003¶oÍa¤øj4®çÚÏûjê,8Ù-xÁvfx^á\x001aÅ¤Ýn>,£ÎÙ\x0003zPÃ	\x0012ó}\x000bx¦}\x000cuö¬ö»þ
Òy¸Ü°×1T3(í®u¬«cgì\x000c8
8oF¹kå\x0018õê½Ö³.ÕÌ³\x0001'«\x0001¯¿æf\x001c½\x000eÝÍ±´e\x001b©³ßd¶ß,é,\x0019\x0014^FiLa\x0011Ï¶Ó\x0007ÆwöÛ[í·¯w^y\x0014çAAú"ZÜât6ÏwæÛÛÍ·\x000f"g±,£D<9¶pâ\x001cËØ]\x0011¼õP±É²"`ÚÃr]Çéíè;\x0017ãí.&j\x0003ùL[uý\x0017¶pbÚUûÎÅx«©¡#Ê
~ëAs5tÔg/eGì\·»\x001a9¢FeNbr9,£gì·;\x0019nu¦\x0016ñ¬#ê2ªf+ó\x0019pß\x0019po6à¬ í6\x0011øzd¸È¥­ã\x0019eBÚ0S4KÎ,kóz¨ùQ8äõæeò1j\x001e!eYr}!\x0015Üð¤ãA«
8Ã\x0003Ò1i\x001c M9\x0016\x0019\x0015çô¥¸®x¾\x0004Zýüî>\x001c}~þÅÖõ¬Î¸¦\x000bòÖ´®6hCeðîxQ«/7¯ªgÐÒÜPV7\x0014\x0017¿í\x0014
\x001c)Îëµ\x001cA,ªf}óéó)\x0002»%Å%å©08s×\x0013\x001eâõÝTWícÒ\x0001PÊ\x0000Ri½$ùÅJy¯M4à&¢öèJ\x0004ê\x000f\"põ×»úW]<¿ýüöâÉí»_ïþúæÝC7H7N\x0014[5SR"@ÑwÕLW?^?­Ï¯^=¹xrõô»ë\x001f\x001f?ý:"n\x0011Ñ\x0014\x0006U£¹ìÑ5¡±."%ìÌÒ\x0018!m	ÉL\x0005\x0012\x0016§J\x000cõO×³C!Ã<¢ß"zû"æ¶HÚ\x0012~çäºN©1Ä°E\x000cfÄ¤\x0013'.ê\x0003ND_d\x0015ç×0n\x0001£}
£ÔÒñ\x0015¨e(eè\x0003Åþi{0m	}	ã:P°\x0002¤t¤\x00077õÍä¼%Ì#Y>²ç>.yt\x0008¢ÊJüð9X¶Å¾áÒ­þõå%\x000c*oKÁùiÄCÅbµÝâ Æ¿<~ÞM$¯f»Z9Ø;\x0016»g©[·Æ\x0013À£+½<d±Û¾tï\x0018cçYÀîZªW^¥'äfIY\x0011¨á.4}¤¡ó-`w.üÐ°¦þ £^ ¢ò\x0013KÓL#v¾\x0005ìÎUø¿ s·ë)ÍÿuzIcs\x0001»w	íÉÒK®%ÚFhþÈtþ\x0005ì\x000eÀ¼jß^dudi=Õ]>h±ó0`w1!ñ4e\x001dë\x001fÌKÔª\x001fòqÞ\x000bBçcÀîdbËOb5®E\x0012²\x001dûÈ1ÄÎÇÝÉð3ì\x0008ôdtÍ:ú4½\x001d±s2hw2ÕKÑ\x000f¬%\x000cQ¥»§!N3v^\x0006í^&´ç%¾Àz­\x0004ù4ä)Ì3ö÷\x0017»	E\x000c\x0012hór\x0016V\x0003ÛüU\x0013þÅQ0ÊØy\x0019´{ wj\x0000:\x0014Ô\x0008¡Gv2Ø9\x0019´;\x0019¼¾\x0012r+öÛ\x001dìN¶;Øù\x0018\x001cð1(
ÁÄ¹T\x0012WíDç¡Fg0¿A»ñÚsIüü \x0007¦
8­ëæ\x0019;\x001f\x0003>\x0006õÎÕxÂé·Fn½;Ã¡î|\x000cÚ}\x000c\x000b\x000c\x0001¯Úé:ÊÃH5<Ó!\x000fv>\x0006\x0007|j¸ËIfwÕe$9_Æ¦s;Ôù\x0018²û\x0018."ùÔI
O(íX»4}¬©ó14äcä&Sÿ\x001aÑNÍü\x00181\x001dQçbÈîbê2J
\x0003@àêöu\x0019AO5Î_d¨O
¸¬uÎå½e\x0019Elß\x0014g\x0011;\x001fC\x0003>Æ³Vÿú¥³Ê\x001fÊ¼\x0001§ÎÉÐ@¬HÕæò¦¨Ù	)KZ¦óL#v>\x0006|L\x0014õöºMú&¨F\x001c÷\x0003Í\x001bÎÇÝÇ$¯9[ç]xP\x000fuÎQg¾Én¾ë\x000e\x000câ\x0005)^Ê&áNgÈúÎxû\x000bÎâ¨¨¥*\x0011².¢/ÓÑwÆÛÛwÖÒÊ\x0008Í	%UÆù\x0007\x000eßYo?ÊÜ>³0"©FrýÔ^\x0019Ýt¼ã;ëíÇÒPë
Áq§¶^b47AiÞîøþcàÃÉ\x0015a\x0019«é\x0013%¤<}¦}g¼½Õx×_fx¸\N³'©YoÓNÐwÖÛ[­wý5Ê\x001aùuPê\x0000bLº\x001b!ÎêÎz{«õö\x000e¢ «ëíÚjtÓñïn\x0008ÞzC¨:Û­®£k)\x0014\x0011æô¾ó1Þêc.õº2fí=Ú!Îs§Ouè¼L°zµ¢¬94/I\x0019ç_.CçdÕÉÔe,ò¾~jI8Í§\x001bCçdÕÉTF\x0015,@ö7R6\x0011.c%Þ¡s2Áêd¼+$}]X|Òûô­\x001fÓ\x0019Ö±s2Áêd|ë8³³0ÆöØÄ<§cèßÑÍN\x0006|æ¥cÂ\x001cJQÓ, È0\x001dNÎÉ\x0004»I$i(¬×\x0002UHAïý\x0018§?tì\x000eu4\x001fjHE²Pê¾'§¢Ëó\x0007&v\x0007&\x000f\x000cä"#¦Ô²P¹h¦\x000cÜ|\x0004\x001e»í\x0018íÛ±è qä1Yòä_D\x0007\ñó]8\x0011Íá\x0004Öpd\x0019¡¨øCÑ²êaæóß\x000e\x000e"Ik©Ö_ÌµZY\x001e®Õ\x0012\x0015C`\x0016}:C
Ï¶ðm­ãá\x001fì\x0005QY\x001eàêÅ°'¤VÊ3o%ã4\x000e zt«2O_í¦Í©ïGGÕeÇ¤4²¦\x0019X ~}\x001c.¢Z\x0011up\x0005Ew¼}9\x0006Å2B\x001auäO=Ü¨-\x0003õ\x0008µ.Mý^vNRø\x0003¨,©"\x000f6|\x001fê+,|ýeîëÞü 6%þüµÙ\x0013äª0{×Z\x0011¨p>¿ ¸[P\x001cYÐPTp£ë¤Óß:¿þ¼´CMC¨M\x0006ÆE;B^´"ÄÅé0©\x001aýO½Ñÿd¾ÖÖT³z©\x001d­^î\x000cå¹»£4tr+\x0016`N¯mÇ\x000eÎ\x0006
î\x0018\x0014Üs*âì«\x001b*p\x0011=éúrCÿóÑ¡ÿÙzè#Hs\x0018fZ}ô\x0013ù\x0007ïà\x000frr\x001bºµîOn@\x0005TçBßA1!ëFÛ®\x0011É_ò/Ö\x001bpÔ'[¦Ñ5±xMly__QÿòùvO+?ZÏ¾×Ò¿jZ^X%mß£Î`¡~î-u£ÖøFdf¹L[Ûb
­¤÷,ËztôýP\x000cõOHb»Ýf\x001dØ«K\x0004­}\x0019Ðºq"iFdÉõùOÛzóá¯ö3´fx½7Õ//>AÏ4ø#Sêí;´zú$)\x001bÆDí\x0018òlwNáè\x001cDé0Î
o·xÿæ÷Ù§QóDAgªç*
.è{K<C	L]Õ×G«j
]+xÂ\x0013\x000f¸Y?¾&ì×wþ$½îOïöÒ\x0013ZßFÔþ¡äÎÐYÍR\x001e1Kõ\x0012*V©Æ{z\x0007UÄ4Ú?\x001dvsÄÌã#$³ÜÉ!ÛRÎz\x0018gôtÔrWØ´ÜýáýÛ7ï?]<úüáÍÝÐ(òáT}z\x0001\x0012Q\x001bÁ\x0003{\Ð\x001f=yüìåÅ£W7¯¿Î[>4óùµÈW£ÞÜ\x0005\x001dt\x0010ð¾Âd\x001b\x001fmùÈÊN\x000c u\x0016á\x0002¨\x0004Ëj'ùüÏù¼´\x000fÕ\x000f|hà\x000eµ¸·_Ñ\x0006\x0018¶Á
È"V²~¤÷
G\x0005é\x0005[¾hæCy`©\x000b\x0008ÚÓæ\x0013\x0005È÷¸\x0015\x001b_Úò¥õï\x000b¾MÆkrË\x0001îË\x0015Ûøò/[ù¢\x0017Å
4ýæP{Îë	¹'(³\x0001-`1\x0003:mëßT¡ÌAP@w_»	ðÐ_·hg%\x000cª´¼\x00115Ò.·=xC¶\x0011öNÄìE|>Êú·#Ð®j¥¹Ïg\x0012°ó"`v#^+4ê\x0012:qÃ©9ºî¾[¡°ó#`v$C\x0014ük¼Íl+¡ô\x001b×\x0015.÷Û6ÂÎÙPÒ(ä4Cj\x0014Û¾ò´¯ÎTÙVcÒÑÊÄ2j´\x0012&ß¾ò´3ÎXÙZö&zÌY´¥\x0012½~d7ë¡³Ö`6×üà(»0IYFå£\x0006§\x0001;k
fs
 ÝºAÄ\x001aS	ú}¾ïo"ÄÎ\£Ù\Ë\x000ceÌõ\x0018\x000b^Æóez\x000bbg«Ñj«)\x0010¿z/Ü
¶\x0012æ¤ºJ>N\x001fcìC~«±æûûyðÜ0¹¶\x000f¤öFï}Ó±F«±®ÿÊ º Ï\x000b)\x0007Ò5\x000c÷½+Ù\x0008;cVcM,Ö'_9Ö¸z\x0005Tu\x0008Ïcæg\x0001»°\x001f­q?\x0007Ó2º\x0010½\x0000'VPÒ%¼¯*ßFØy\x0013´z\x0013v!(Æ\x0007I'¦\x000c:[¾\x0012NäÎ Õ,|dr7I<#Y\x0008ý}}\x00036ÂÎ Õ`p:ÝUTÄ#'¯Ó-<ÍåÎ Õ`½ÈlJ Å)Å¨G\x0019ïë§2\x0011RçOÈêOÑe\x001fB\x0016­HÐê?tÖ\x001cRçRÈêRÐ\x000e"Äê}\x0011B\x001dCz¿°s)du)HNÆ\x0008TBº\x0014@Tk÷ÕÛøú,Õ¡ðáPW/P«ONÐÂ.³a\x0017uþ¬þ\x0004\x000el\x0005º-ªA7½;!«;Áj¬×æ\x001f¿è»¬ul\x0013Öa%ìÜ	YÝ	6è\x001a2\
 ª 1,Ì\x0002vÞ¬Þ\x00048S³òqNiýÄ±9dº¯vÓÆ×ù\x0012²ú\x0012Öî»\x0013ÄtYV;\x0018Ú°c¾ÂSçJÈêJ 8½~²¨\M¢J´ÓtÈå;Gâ­\x0004xðÕpm\x0001©\x000b¨§ßQf	;3í­f\x001aªíáà,ç²Vj¦ òBÒ}5¥Æ °\x001b\x000e¹\x0006·û\x0013ÍMR=çêÛÝ§\x001a`û\x0016yÍÆDÇ DvP.Í]ÛUªÕqÝ¬w)õ,,\x0003;_?\x0006\x001dXPÏ\x000fxAä)húÒ²°ó!\x0004ì8a\x0004\x0014ñê\x0004\x0011\x0012K,x¯)¦Ù\x001dJ;N\x001aàdw#1Yçnð|î¦+-
ºyÄ=5°\x0000¿¹4ßÑT\x0005\x001aúÜ×\x001ebô»\x0005M\x0003\x000búvwû3\x000fìONà\x001d2xr[è2xó©	õ\x0003	½¾b\x0008j¬§J?<;ÎÙünE\x0007L(ç½ÓaE¬hÖ#ïË}]Æàw·CÃÀ\x000eå\x0016!0QÆ\x000b¦\x0018r³õã\x0011\x0012Ð\x0017\x001bÔ\x001f¸Øàño¾ýøñîâÛ\x000f\x000f'Ü>'\x0002é9èû\x0010z"ªw²N
ôñ\x000fÏ¯^¼¸¾øáêæ©Ä[$<\x0019):-\x0016+Ù«ÃÁ \x0002 |ÍÃH´E¢X2lù|\x000eÏAhD½
ÈoüÉD\x0014E²"5	)Ä\\x0014©»ÚÂ\x0016)\x0004:Ò³Ê\x0003Ê\x0008ù"ÕIlKÂ0RÜ"ÅÓ¿[ÁÖÞ±QKòátl4ú<þáò\x0016)\x001aNq]LC­ÇL\x000f\x001c\x001b\x0005+\x0012Ò#Õ\x001fz·oÿþ·»_î>^üáöãûw\x000fÍwEª\x0001BI¤\x0001~)2§<ÖOÐÙÒ'O®¯/¾½~qñ«\x0017Ï~íðÒÎlËKûép´9.pÕ~Jd¥{1:è%¬l7\x0007f[Þ\x001c,lIÊ\x0003÷t\x0007e\x0013´#E<3ZêÐ\x0011¤.¼¢öäbT¸4ÃvÈü1Ûù3ì·Ue¼µùJÎ¥ `±L¬\x0018W
äÖMx8§¼Ug£4\x0005ç»àm'Á£ãÍ
:\x0019Ö\x0004Â96ß±yã'-å°p2­¯|j\x000b7eB|w\x0016¼ý,Ä
Æ×ÍÏ\x0010ß^o´½\x0010ÅMU8ÔaèÕâz)#\x0012º\x001d\x0017;\x000eTdqY9§\x0015DN§©-wÐÔXàÀèµHb
dÀKµ¾òd^áú÷Óáè(ª®?pTýèOw¿½y·°}÷ö¯oî\x001e ÃBªÓ\x001c\x0015IÖ·Þj>Vç\x0010jô±]ºGß_ÿðøé÷ýõ\x001f\x001f_\x0002[@´\x0002:Ia\x0005¬Q7\x0008 ×òàc'a?\x0004H[@ú\x001d® ß\x0002z#`NZeÌv2\x00142º<b\x00120l\x0001Ãïp\x0005ó\x00160[W0ÀZç\x001eø%k\x001d,0I\x0019ï"Ç5É·	=ù\x0010;+ s,÷P/\x000eÒn0Òê:BÝ\x00030KØíA0oÂj¢ýrc\x000e,*\x0015¨\x0002Ü\x0001±Ì~cè6!Xwaâ)«¡á:Z¿²ÞÃ\x0002ôÚ\x001eC±\x0003f@-6\x0008Ü¬ N?r/©?D:Âd%t*o\x0015\RÕºäÊpútç\x0018¬\x00079f/ODÁå¨Æ\x001d\x0010;\x0019ø!ÂÒ\x0011\x0016ë\x0012¢\x001a\x0017[Ù\x0010¨\x0007ãYo]¼Ö!bdåÉ°z\x0013X.áQ3(\x0001Âì1ÆÎ\x001b£Õ\x001dGïd8F`QÙuäMZJ\x0018VÀ\x001cg?1v§\x0004­§dã°fZ\x0013Ë¯+\x0018HR\x0005¾PþÆÝ&Dë&Ä\x0014ôù§Þ?ÖçÈÝÏ\x0002\x0018Ëì\x0012RçïÈêï4ö\x001f3U\x0000è2ÕCxÝ\x0019!ë\x0019©DË3\x0019¿. T\x000cU÷â¦×¯\x000fY­UX¤\x001ab\x0019¹nAîÖ/Lq°\x0017È\x001a/x~X·`A!äÛ°Ä\.ÅY_B]¼@Öx¥ò%Kg=#&¤ Íq%Ìbêâ\x0005²Æ\x000bHfupg\x0008bÖ¸ZÏëåµ\x0008;KHVKè8\x0019¹ä\x0014ÔÎ\x0013õ\x0012_hú\x001cwá\x0002YÃ\x0005
ôðu
%ÍVÏ	è&ì\x001b4\x0008;KMVK½â¨¥Ò \x0017yþ ,aYBßÙBo´PSo\x0017Ó\x0012a3! \x000ecåÞðYÂ.Áà­\x0019\x0006Ì(
o>S§³\x0018|Òsâ¦¯w¾¿À[!²È©\x0010(*P¢Ö\x001a\x0013Î\x001e\x0014ß\x001ao55K\x0016}`p.èGÜ®"Q¡õx¡\x00185b CçOI\x000bß%Ì"ãW\x00030{C\x000eÝ6\x000cÖmøO06¡ÛÁ¼
]la
\x000f8Y\x001d\x000f2=$,ÿs±ûÊÑúÁ¥\x0016¸Æ"\x0013%bu\x001a×ø4»\x000fc÷£õ+/*\x00125ð}^\^\x000b­ý´ÏÝGÖÌ×ÎU«Ë³ÄéúD\x001e1i\x0015e!?k
ÛÖ~Éqæ_1,ÊEÏgGl\x001f×\x00186iüÒl:$vµJ²üËïí`ûxPì\x0011\x0003þ³\x0011TûÌóXD\Ïv\x0004ý®*¶>îH¯G¾¼ühûøÙÉ ÏÉWåº¤2sÐ<KÛ+3ÊEßüíyØ ÌEïªA%åj`^¦7)î6)þ.7)cP\x0008vÐ|Ü1'9;gàWÒ,YÌÝù¥H-K1kGë\x0016=:Mu\x0012ú¬\x0007Õ\x0013I\x0001RôE[zó¬Ç¬Æéõqzý»3N´óI4àþ	\x001f=ìvg\x0018ØÈ}Ü²¢5`äEPõÀ\x001aÊ¥á\x0004PqÐ¿K×\x001fø]úæóÝÅ³·o*ÙJyñâîÃ»\x0007ÞÍC½I«yª÷õNAª|Á.»yu}ñìÉãvS1/^\ßÜ\À[F´3RÔFé$Ã3 ên\x0014ê\x0014\x000f\x0006!i\x000bIvH~R,KöÀ\x000cîÀgXH¿eô\x0003I9^H\x0011ú\x0001PwÞ«\x000e2-c°3ºÖÅ¢\x0016]e§\x0005Ò\x0005Jg[Æhg\x0004>TÚ$8W\x000eßº{e\x001ddL[Ædfô^¼Mñ:^fÉ2·9ÃfÌ[Àl\x0007Ì@íº^ç«» ýYÅû3ê²,vHÌ"}\x0016SjDY5\x001aò9¾ô¡*a1án`%ÔÖË¤4þ²@ f'ûYB½±;\x001a®	öé\x001a÷´¦¤½$¬T?OÙy\x001a°»zÏ\x0011wÏÃ\x001d\x0019R»Ià¼ùÎÕÝ×p%¤7býàA\x001bÜD3ßs\x0015ù<eçlÀîmê9¬%è¬\x0004'j¯Ügì
Ø½¯ÞFBÉHIzæKh²ì¼
ØÝgÑyÉf­"	ëB¶ä~_¹5HÙù\x001b°;\x001c.(-Ö\x0004n\x0017íñºp\x0003Þ9\x001d\x0018ð:¡¨\x0008Ajj'ÙaTÏÎ±-;¯\x0003v·C¿\ND9Ý­1®\x0002i\x000c\x0011;§\x0003N'ÈÑ ³\x001bê×Ñ\x001dhþ[cçrÐîr¸ÌQú£­&\x0018åi¶^xâü·Æþr3àr<ë"/KÉ­õÚ\x0001!cz|çøÚÇA»Ç!q^µPHº
êR z
ÕÏ\x0010QbgÍÑnÍ)5ùÀãâ¤Í\x0005dW¦~ÜÕ dgÍqÀCVÈ -eRßMgXÈÎã-çÇ»õ\x0013¢Î¨w\x001díø®QÛ\x00196egËqÀ×0H\x00148§¦:1¨-ÇtóÝÙr\x001c°å\x0011´:ø\x0016øæ"n1!Ìpê¬9
Xs¶\x0012P¶È\x0012R[É3\!¨³ç4`ÏÓZ Î¶\x0004EÌÚ7¨³çd·çõJÈYe-YÒVÖ\x001bL×µìÓ¨}¶jÀ ûp)\x001e<ð·WI½}Ç|Ä\x001fuW\x0008²_!8\x000eU$\x001e¯¡67çslËÎëÐ×!­ÇöõR#\x0003ãSæ\x0011!ëR¦3xpêÜ\x000eÙÝ\x000e_¬7q)\x001a/¨|æ!;¿Cv¿kcÊ¢ÜÂÕ8¢Ù£¶²:õy\x0007NÛ!»Û©¾Oª9{î¤\x0010´ .\x0005\x00063Ô¹\x001d²»\x001däâS\x0011Z>ä\x0008êZ
e\x00084Oé;¿ãí~\x0003
\x0010çP[\x0005j ¡w\x001dßÕ­
RvÇÛ\x001d\x000fòðT&÷Ô¶erªàïÏÜ÷ãñ\x0003'zÕ\x0016	ü .áÓô>·óÍSvÇÛ\x001d\x000fòs²\x000ekÈ2ï±ÞÄÚ°\x0001ÌgØýCÉã©\x000bä¾ã³öCæ¢	ô~>´ôçñvÏÃÊ*÷^cáõa,%ßÎ8øùPÃwÇ\x000fx\x001eJm_ú¤ÂþYgëRÎ;qßy\x001e?àyÐëó\x001dV¤æ\x0012j2¥t¥ì\\x001fp=¾é\x001dó#¸
2%éïó±Ð|â×w®Ç\x000f¸\x001eHj.¹2GôÂtà½çËÚ4dè<O\x0018ð<¾)\x0007pZáÂs(u)çweè\x001cO°;\x001e[ËªÚëTO3fT]a<I\x000fã	\x0003¢d°QU²1hø{Ð¹`w;¼RmÆ
¯¤oró¡eèÜN\x0018p;\x0010õñÛ×«\x000f©à®d8Ã×îßçíN\x0007rl{Òå&¡\x001a^8!\x0018
Ó	\x0003N\x0007\x0001ËJÆ%w¹®¤æ¢?Cn(t^'Ø½Î"û¨kI"g\x0014£&,=¤ùè7tN'\x000c8\x001dt:\x0006À\x0007§WG\x000ee)é\x000c®1vö<Úí9\x0016¯©\x001aCjGj\x0006Ñ#3Pv¦2ÚM%\x0016×(=ªkÌ.´µtó'vf(\x000e!Wx\x0001\x0017JDypL<VZ(á\x000c¯à±/Â\x00198âÎ«I÷,\x0018/º¹rßî\x000c÷ðØ8pzÓ_N²(ine(gH¼¤îô¤±Ó#¹¥å,³Ó²ÏpxRwxÒÀáII\x001f¡8\x0007³ª#%NZ
eÌó><u'Ù\x000f\x000fªgùT/\x0017z­Õûm8ÃRvg'ÙÏ\x000eÏsI:\x00133H­o½â´iþ\x001eº£ìG\x0007«ä\x0010­-G+d\x001b\x0015vâ«Ü<pr(´aW%µMÉòkB9ÈÝÉÉ\x0003'\x0007[¶eÑ½\x000e¯ÐÉ\x0006>aSæîääSí£¼×ó¸\x0012Ö¶2\x001fÎPT»í'\x0007x:´lM\x0005=El1wóö\x001cÂ¡_*^ÛôêGª\x001f8O$:Awò9C¡kû#ÿb¾Bz­\x0015ãqÂ\x0002U\x0007ÁÁÿ\x001c³¦!ÖÅÀ³\x000c^ÎRÐJÆ\x0010Îp\x0001ª;àÓÑ\x000eø4RëDòæ³­uRWÎQGqÛÒ!SüËH±<Q+ÖÑÜuÿþä¿?ù±ï\x001fD)ÛÇ5À¹\x0004-®>r;Ø!ÖP£Oíî8NYËY1¡r0üô£­ú\x0017óVMNßP#d\x0011.Ë´*f1\x0005ó}(Çk:tþ\x0003ÒZ#¼ ]=\x0019HïÃ%á>Ìm|Gú³ýü;Í&E<TØ\x0003¶BBO/ô\x001bäÝwäTU$ja<¢§d\x0008üuCud«ü©úg\x001c*G»e\x001d;ÿ¥uü$ºÊaUE­¨þ\x000c; îPãP\x000cPÃ)Ò\x000eÀ¸Ä\x0000!i\x00011¹yØ\x001a\x0004\x001cm\x001a\x0004\x000cì\x0001ní×õ\x001aº8½å\x0005\x0001Îá\x0002Â.¶\x001aYVÎÉ¬	Ëÿô½KÍ\Á\x00195ïö@\x001eÚ\x00035&Õýº\x0019õ\x0018Û¤wå\x000cizØ-,\x000cÁò}Oß\x0014*ås÷¤¾)À\x0019º\x0007ÂO¿\x001e9_í[\x0000Z!4h\x0019UvÔ\x0011d¿¤&·\x000b¯Ý#¨\x0017T¥I¹âDR½z}9Ã\x0006ØíÖ0h±P\x001f}$¾\x0014È#CÑG	G\x0010«gí\x001a|ë\x000fGÂÓÏß<$Í&j\x001d3\x0014øI\x001bu\x0000\x0013\x0011Ibùÿ{»?~¨óXÁp\x000b\x00160"\x0008|Ï\x0007½@IÉ{ S`´\x0005#\x0003X=(:&åªVÐ J\x0010ç/É3\x0006æ·`Þ\x0002\x0016µá+pZr\x0015,|I\x0013è4°°\x0005\x000b\x0016°¤\x000fX\x0001Kz-(\x0001F /J\x0006\x0016·`Ñ\x0002ÆBVµkäë¤¶Èm\x000eüö6\x0003¶`É\x0004Fªr]\x0011cÐJë¨\x000bö%ÕÏÓ¸ò+\x001b¸¼\x000bmEà{ÃÚ ãh\x0002Åø\x0005\x001dÃÓÀÊ\x0016¬À²(û\x0007.rrÚ/!WÃà\x0001¾ Er\x0012\x0018ôöÕb`=jd\x0015\x000eùiÙ__á&¨:\x001b\x0006\x0016#æ³¿\x0014%
m¢JêÔÀ©ô\x0019°ÎTÅVÄuè/uB\x0014Õï+f?LZ×.ª[åbÇWÜRÒ\x0012°ú9Ê»g×¾èÄ:\x001eÄûY¶~ü\x001b®¨ã±loï.~ù|ñÃûÏoß¼û"U½^¨è\x001fE\x0002ËV\Ô(åÜïë\x001f|ûêâg¯<~z:Á-\x000cþah\x000bCÿb\x0018¿ñÿb°	ÿb¸ÿb´Iÿ\x001a\x0018
õ!:ç«7\x0013\x0017_Ü¾y÷éâêó¯?~zB\x000czëu¨\x00156\x0019Ô2zôak³u\x0014Ü«ÇO_^\½úîÕ[¼c\x0003©¸ÅÄ\x0001Ìâ%n§Âe!¢q¼`Bè^iF1iI#(÷äzQ1µH\x0016b\x00170bú-¦\x001fÀ¬[Ù<EWS5*!vÞp2l)\x001b§IfpòT/Ò\x0006,è%gG)ã2¬¥\x0002QñM§MwDç L[Ê4B	¢=P)$
3\x0004M\x001cC?:}\x00143o1ó\x0000&W\x0008\x0008eik\x0019TÇ¡^:ÏaÊ²PFé} \x0012¼ÜÕ+¦Ï\x001cî\x001b\x000ekÄ<hó,¦Ýpzy-®Yçê×Ò*è\x001faG9{\x00174âZ¿\x0018R§V9µ\x001bÊ9Î\x0010t>\x0008FP,bÜcÔT&xÁÄ\x0003ÊÏ`Ü¡óA0â*Zw~ÛôêÒuR°3øJè\x0010x¡HòðZ9\x0003ûÍõ135Îs|õÎ\x000bÁ\x001b
q\x0019t´b\x0016î7Wrìò9N{ç`Ä\x0011Õ#e{fjÆ´÷\x0005ûÊÙQÎÎ\x0013Á+
ñ\x0012Ä*e­bÊ\x0015.*g<Çwï\\x0011ø¢@3 R\x0014Ru\x0010Ý\x0019B$è<\x0011¸¢ÒÅÙ;\x001dw
¨%tÍ+Â\x0011W\x0014\;ë¥\x001c>º¶<!¦3¬'v®\x0008G\Q]OÉØ¬9.¶Sëºà\x000cýehÄ\x0011ñ\x000b°L9w©y¢¦tÐ\x0018;O#(è=ÃóLY¯NÚùT7ç9¾zçpè>¤ÏUõÞ«½ÿ\x001cÃëzn¢ñ(gçpÈ\x0015ö`VÑîm­T	=c=;W#®¨F m=A\x0013Á ÕÓèÏaá±óD8âRÔ"EÇ\x0002Ô\x0012èØ\x0015î =\x0007gçpÄ\x0013\x0001¨êCýç]âY\x001bØx\x0016ÌÎ\x0017á/ªô ¶s\x0019Ã¸Vüh&ð\x000cWLê\\x0011¸"l­\x001cÎiAzv\x0005ÕµS<\x0007gçhÄ\x0015qu¿ìNPE±\x000c®¹vø:gD#Î_½pf}[\x0001Ð"\x001fôçpFÔ§æ\x0011^
&\x00127wg×ðØã\x0014QçhèVääÍ±r¦fH3Øxrv¾F|Q½\x000bIac\x0005Ô\x001e£èÎq:_DCù9ÐânGÃ¦Õ·«/p\x000eÌÎ\x0017ÑP´²ß*9ULjg±/¢\x0011_\x001eÛ¦;Uÿ\x0017ã9r5Ô9#\x001aqF9ª\x0006óp©_=µÝy\x000e£ä;gäGQn³9ÇË¬Ë©²SØ[rvÎÈ8£âÚ½È{}ÕPO\x0014Ï\x0011ÏùÎ\x0013ù¡G"\x00101ç\x0003àÈ\x001bQ;Bé\x001c#òCD¤U±<À\x0018Å\x00135ý;S(G×¿\x000cÖ\x001føeðê¯wõ¯ºøñöÍÛ··\x0015ôÑûÏ>x³T$ßO>6gW7ESÑ'õÚW?^?}u}ñãÕã'O®*ë£g¯^¾ºy|}óuXÜÂâ\x0008,ñ
S&FACÖ<]òÚWJ¾ë9`¥-+-¬_Æ]G?.\x000b\x001bT=à\\x000bë·°~p\x0017D\x00199\x0001õö±Vy§¢Yõÿ~&Ô¸Ec¨1·\x001b4GQÑ\x0004(±ÒöYHÓ4
¶\x0003W}\x0000É\x000eÈÚuFÐõæOÀæ-l\x001e
¤º+\x001dXK-)áÁ\x000eél-l\x0019<[ÇÅéÙJZÕ'×\x00159£\x001eç\x0016ûêÆX9{'û59Uh Ð~NrtÞ\x001b¹\x001c\x000fÉQOë4ç­ñ\x0004{ýú	ØÎ\x001bÀ;Àü¥Ì¡á1rëµ4aÒfi,x¦¥íü\x00019\x0004ú+åü¼´¢\ï¤ØÖ6¶s\x00080æ\x00112«µ U
¡8
`²ÃóÀ\x000e6ÁúÜÐõ& jkKêYöL\x0016:\x0007\x0006c\x001eç\x0011¹Ôîi5µõB ±vê:ü&h;'\x0006c^,³(`ik\x0011CT/)im;/\x0006cn§ÌÅx¸c¯ù\x0010\h;á<°\x001717±
~w\x0014T\x0006\x0014]{\x001dOtCkÀA×P#nÒ,×\x00169X\x0016Z<Ï¶ÅÎÚâ µêv©Ñ®9¡jÀJ3	]²e¶3`8fÀRiÊ|ZÏ\x0012$jk\x000bgZÛÎ$àIH¹
Äuj\x0012 ¶;e8vÊR«Þ[ÖV&\x0007AH-¦Áó2êN\x0019²Åù\x0003-¨\x0001;²ó[êï¸c§,%h©ÂJ+Ù\x0003ð.ùQwÊhð¢zl\x0013`ís\x0003\x000cÍñÒy.\x000eÔ2\x001a<e¾
\x000fs\x0004ê\x0002ëb=ÓUºCFc,ºC³^!Ö\x0010Ëá\x0003çñ»¾;c~ìuhå
«r@qý)´þ<gÌwgÌ± O0|{\g¤ç&]TïºgZØîù±\x0003æ\x0013¶Èç8­\x0013YrTh	ÏCÛKm¬y/þa(õÕº#X|\x000b4ù\x0005ÊÎtÑé\x001aØ%¡À¿\x00047Üq\x000fm\x0003\x000b3¶¤-kSÀ1³Qf~\x0006AE.&¶lë¡ÓB!ê[\x001ag²a?Ýöù°Û¡}Á\x0003\x001b³ä\x001d§pÖü­¾Í\x0013'Æq»5\x001e^b®\x0000o)g\x001d(åf,è<Ù^>j=~£Ì\x0005u\x0014\x0002¸¦ÌÃ*ÚºÌaÒÍÅrôXRÐQæ¿|¾¸¹ûóûÚJ£ÌøRq»>2b\x0016¡ç\x0000{yo_]Ü\?öPKi9z\x0011a"<+\x0003£ EÕ]Ã\x0014Û|úÅéH´E¢Ó\x0017	tÌ{©ñ«T÷cÖvep;}­Óü\x0016ÉäFO\x0007\x0002¯í¨2jÁí$gO'
[¢púwËª\x0019Î/\x0003N\x0017IôòÛiÏN\x0014·Dñd"Î¬qPñ(i³\-µlnv³3NGJ[¤tú"¡4ÕErí³©tl]¤þåéHyO_%hH\x0014D:0£WM\x0005\x0017óð*\x001d^\x0018\x0016£äNfBÒ\x001b8¿/Èðc¤Æäw
Q§3õòtK\x0019¼¼àþ3T»¤_.Åq¤ÎRÂé¦²ÞJdÐmæyð«D\x001dªJÃqã
¥ÓMeµKR\x0019PHç\x001b°]"]&w¬y:SgàtËäu<#op)êÄ¨\x000eejwf\x0000N·\x0003Þiú® ëáe\x0012á\x0017×7ÚJTN·\x0003A\x0007
\x0015wØL\x0001ôÌÑNjýd&ìÎ\x001c~æ¨jÏ%ðèjrcc¨ÓºÝ§ï&,¬KÞ\x000eL\x000e§nØ\x0010`÷íðôoÇ\x0002ëå\x001f
¥Bpc/a7ÙÈ°Å;eu«Ü×)0éÛU \x00131x]®0áñü1·±\x0012éú!KuË"í±\x0005,ûaÂ_'K%\x001c\x001a¥téíÛ»\x0005êÅÝ?¿{÷éË\,\x0005µ¶Hå&B*%Tú¹ÛWO\/`/®o?{rýòël¸eC\x001b[ªXÅ÷\x0005yvhµ¨ÑAÆ98¿óF8\x001aBa7¤pRãQã$\ÜÂE\x001b\x001c§·V¨\x0002^g\x0006dNæPêÏÁå-\6®j]\x0007Î½\x000c\x0003\x0001µ\x001fåèz:\x001cÂÑí´þÐn§w\x0017oÿç¿þûú×·o>Þ=\x0014x\x0015MgV»!cÛêµÂ5Åà¼\x000bs®/\\÷äñë¯£Ñ\x0016lhI{\x0017}%gµ \x0015íö/!\x000c¡e:.¤eÕ¾yÿùíÝ_o?ürñòöÃ÷>=ÀæëùÔj½Àj¿k-é\x0015më§¾yöêÉõW7ß^¼¼ºyüìåË\x0013ðpF<®\x0012Iu÷I·\x000bmhJì\x0012FðhGF¼Dì\x0011V¼ÄZ	\x000b^ëa¨¦\x000e'ñü\x0016Ï[ñ\x0008ôy\x0016\x00116:GúÔ\x0013b$\x0019Á\x000b[¼`Ä *¼xkn1Wß\x0010ÚâÑ$]ÜÒE#GmKâI8*»XBÃ³xi¬xY^Yj<²k]S¡Wà\x0019ÁË[¼lÄ«6X\x0002:ª»0¨¢ µÕë®S#xeWxÜÉÓÌJ\x0014!ÆuìMìz\x0006è6U´æ4LxÕ÷®^ÔR®\x0012´Ü(Ä2×û\x000c«Ó¨\x001fWOÓ\x001aúm\x000ffeÒ(Cç3Àê4\x001c±PäÊD\x000e&\x0015¯­;!¹É½\x0007Ó\x0000«×¨7\x001c*Í,K½@mÔuß³3Â×y
0º
âö\x0012Ý}Y«/
©AH0»~Û\x0000«ßp-=J©e\x0016ïÛé\x0008³Ç£s\x001c`ô\x001clð~ßÂ\x0019\x000fTj.$=\x001fç\x0000£ë \x001aT\x0015jM\x001aHÊÁ4ÇÉ¨\x0000:Ï\x0001F×A!µã]9µ¥-°\x0018Þ\x001c_ç:Àè;ø6ãìµ½@hA_ÃÃÎw Ñwð «G:¯<\x0007×\x000eï4^ç;Ðè;(¸¶z\°¼\x001e¬\x0003(x.Þ$^gÑh7Xù;\x0007¶ùf}\x001bv¶\x000f¶Usåý\x000fGj\x00039uýÒ¤ëÀþ%~ýÂüEÞ%8õ¤ó³\x0016\x001b\x0006ï&
ôÑÛ;iNÏ|ý8AIÑVãÕÜp\x0018]Ëzóè\x000f2_E¶rB¬|õúöõÛT¦#®A*å\x0012ÌD«}\x0003º·\x001bÕ¯\x001e]=z|õâß^¿ÿí·Ïïîôßñ°ÃC+^ éì"~~ÓáwEëÀß«/aàó\x001d\x001fàKaåCßÂ\x0018­oûD©\x0001/vxq\x0000ÏÙáT<]¾ïÓâ1ðå/[ùê5%Ú¬AkêuýÂàú\x0005<ô­?l%}¸ýðúîíÅ£?ÝþöþÝC\x001dÆõWÔ×¨XÚÐät	O\x000eºñ«G×O.\x001e}õÃ³§]ñ\x0017HqK\x0003¤\x0018\x00045	*t\x0010R/«£»OqËLJ[R\x001aZSh½Ðü$*
f	t_fçîÛfR¿%õckÚfÆ\x00124½Tþ1ûpü£\x00194lAÃØ¢v\x000fÅê\x0019WKTTÛ0²»WnÍL\x001a·¤qlIÛ\x0013a¬W{I\x0007ÇÒæ!eMÓ4
æ B¿«	Ö]Zÿ«íR¸O\x000fÐ\x000c· y\x00084\x000c¼ñ5 hKªõE´ÅF-i\x0019"
Q\x000bØxI¥\x0012ªîX\x001dºéîUä±Bo÷G\x000cÿ*WØ\x0008'­¨*ó\x0012Ý'\x0010gFíÌ)ØÓEéWÊ\x0017í(ß_'ý¢Üp\x0006ÔÎÂA=ÔÅ6¢¾®ªÞly\x0018ë9P;
#&uYUé\x0015\x000b	å\x001eÄ«ªãÖè,Æ\x001f:C\x0005ck-ÖU]t"WÒ¨§ªoeú"èÃ±\x0014tv
Æ\x000cUuMR\x001eë%]*\x001d"ßÕäøß«öm^ÒÎPÁ¥â«ùº¢üJ¾¾\x001cÅ¤¢µ\Ô2¿¦ÛÛ\x0012õ¹±5ÍZ¦Ì\x0015A kÚz²Sç0þØT\x001c3©Ü!¸nS_jò,kYÔxRò5í#é±P:´v»ÈÙ\x0010µRÚ«b8G4íÇ1Û£è\x0007x\x0016j\x0015Õ!\x0019\x0011ÊIôW´úp,ìN\x001et\x0002%\x0015(¯Ë(Wåäè\x001cÆ\x0014;#cF*dí\x0008!~\x0004Ç(A­é½·z+*uûÆöiô*&\x0013Ði\x001a´i­^\x0000Îq¢ÎïÓßõ·ÆÒÁ%©:â\x0010U\x001eTbçøþÔíT\x001aÛ©<\x000cq-\x001a¨Aª1Æ&\x001fXwÂ9\x000e?u[Æ¶jj½SP¦ýU/¥	èÎê;7åÇÜTF\x0015eô.òueEÕ\x00185äóDS]nY¢þeÌ\x000eHMUäÚÝ²Ú!Þ?Çÿ;`\x001a\x0005®&V\x001e\x0005y*QÔk ª×
÷ªÜÚ
×1q5^£Ä¤ÍCl¿Z­Û7ß«i~20âqÍ\x001f¶¿ëßÞ¼½»xôþ·\x001f\x0018
ì\x001dÀ¬\x0019ÊP/R@Hv-·ü\x001d×3_ÿÀãÆ\x001e=ûáÆ\x0002+\x001anÑÐF(a\x0014WAø\x0004\x0012¡RJxÜM`C£-\x001aÐêÕy
ã\x0019À2Q;×[h\x0014´\x0002Çé64¿Eó&4LÒº¹B&ô|ÐìvUà6´¸E¶\x000fºNF	~ÉÚKþ.(W[²¼åÊÖ¯Yäk²®ªdÀ½ÔV´x\nB;Ô1-ÇÓØ¢&QàñQÂ¦½"a­7\x001d6Ûb5UiiMÚ¸´N±u¶\x0003lÆËç-\x000fY\x0007(b<îg±±u'\x0014lG4k;\x0004EpÚ¹Õ\x0006S
\x001a¦\x000cÛ!7´°\x0005\x000b\x001b¸z\x0000V4îXÑê\x0001PëQ`Ê\x001d@g=Àf>JÐÇ¾È*Íâª¼åV6?·ÝRÇLËÆ
7ë1\Iº\x001eÓ¢kO\x0005òÜ1í¬\x001b\x0018Í[à\x000e.e·i×iE\x000bs»­thÅ´lH¬fº åV9Ïm\x0012ÂF»¾a\x0013\x001bv\x0017M\x0017Ð¯÷yJÎ©S`k"h~Î_agxÑdxÁ/\x0003³\x00176.#\x0015¶\x0008r\x0012ê8î\x0000·±õAÉðw\x001a\x001a%rêç³e¬7::nKµ±uQ\x001bÂ¶ºÓuJ\x0017+8­uS¹\x0006GÊV&×­s
hr
P#$Ë.³¬~Ð<\x0017´agvÑdv±dÑXØËfPÿ®8ev±3»h3»!K\x000f4-âl²l­a©þ#çìGgvÑdv§eaf@jaWÃ9µnÔÙ6²Ù¶D¬ªÿEÚõ_VO×èiÊÍSµ²\x001dÒÜ*¶ØÌ­d ó\#ÃtÐôývkã'39¦%é4·'óú|î ¦îðîLß5ªcÈXt"]qÔ¾+N9-ýêÕ¯bY=ºûÀ\x0003\x0008×ã¤C(Iß·\x001b9²Ú¦|ê©-ò(^¯VÔ"¬ãzOs~è­^'UÚª£î/>rn\x000fþr´\x00071íA
º\x0007ÛÐ\´¬À\x0005?wè\x0014ÛäöÅ¿XÝiáëÃzËñz\x0001«Á±^\Öw\x001f\x0019¬\x001f5úH_)ëd§\x0014å$óâN*nwT¬'å\x001f5©Ûðç£mø³ÉR\x0007©¯$¨¯Æm |5QËO¯è^è2¯Øjf@$T8mÿr~.\x0010M?ýñî¦#\øê¿\x0007íáêFrsÂn\x0010\x000fâqzlùê·\x001fo/^~xóþyp²ë\x0002Ö¨J\x0007R\x0013\x0007¢¼ÿ®O^\]¼¼yüµöùx¯®hhBK2Q(\x0010\x0005ñ½Ô\x0011¥\x0019ßWÓØÉhKF&2Wï=«\\x0003·j®OS)TPp]Â.\x0019fBó[4oBãgSYµ\x0010TµOtA| ]ønâ
[®`âbYß%Táñ*²bQêxBÀý³,nÉ¢mÅ@<\x0003¿ÎH.¥¢ª8>ùû7¡¥-Z2¡ù&ná

×# dÁï´ldyK-d\x0015M$çyâ6+ó Á¤Ù([´bZ´ j~qÕi\x001eI7ZÜé.À6o\x000fljmÑ"ÏXÈ8e
ÚfÖØâ.\x00166±õnÀæ\x0007ª2²¬,Õ6!ä2u>¡3¶`³¶ÙËxj&J\x0013ÇÁ(\x0012/q¯Ïhcë¬\x001aÌ\x001a9/S-ø8jÛo®î\x0010	æÐ:Û\x0001&ãQÿ_s
ò\x0016\x0017á¯\x0005-ªg}¯­;¢`:£Äµ'²l|ÅeËR\x001abØ_\x0018Læ£+êX¢\x0016D\x0008õfõ£$Z®)\x0016ÉÒU{cvÜQAýAC¶ïn?~zÿîâåíÏ·\x001f~¹{û7Íma¤Ë\x0015.v`ÙÅß]½xùìéÅË«o®n¾½~òu>Üò¡¯Zÿ6¬ª ä8S\x000cm\x001e ¤ãÕ3\x0003Ò\x0016Ì\x000b\x0018%[F>\x0014HÒ¬ÄÑÄ!>¿åóÖ\x0005,©
qÏI.~u\x0001w
ofÀ°\x0005\x000cF@r*õæ\x001d\x0006õ²1óa/nù¢õ\x0003óC°øóü<,çW<º]¶Ø\x000c·Ù¼\x0003\x001dÏ¹2)OËÒvÔÁq¬n\x0005<Ä*qVB~
ñ,\x0001¥¥\x0012jò\x0013óN\x0010ÕLØY\x0019°\x0019ä6\x001bùÈÜø+¡»kv0ï+ÌÝ1\x0006ë9FÖ#\x0015mýz\x001d[§D¤5·Xcã¸ÊLØ\x0013°\x001e\x0014(NÛUyT(GÄ¨\x001dì»\x0001\x000eJçW§ÞØ°¥
é+$¹îz u|õØÃ>/æc!úÜ|òÍÝ»¿ÿíâ»\x000f·ï~y(I²Ä¤Ö3 Z¬\x001e7âÍõÓJxsõôÛ¯sÑ,\E«\x0010\x001cÐ,\\x0004ÚáøýbÃõúöúu>|+l¹\x000bK^\x001fg+VaG¼:\x000fÍU?||*,Ë¶XÉuèß\D\x0007¤é%¿»<Z¸Ê«¸HÏhÈØ>£\x0016éî
'\x000cPÐïyË¦GÎúËj±ÕÕÒ
ý\x0014v²Ë\x0016°nÓe×c
9ÅµrY³Äî\x0019T+*Å¦°å3NºwÙùjÍNÃcu7é\x0016ñªtr+º¦¡MVÿ±G÷
l©àç·ß^|÷æC5±_Æª¿h\x0017\x000bU\x0003ë×G\x001c
¥ôì>çó«WO.¾{|SÍë×Áp\x000b\x00160\x000cr]dûÖÑÒ\ÃÜ´¡ð8\x000e1Ñ\x0016,`Ô¹Snú	\éÔD`\x0013ßy\x000bX5û*tÈÞë&Çì\x0002\x0016`jÅÂ\x0016,\x0018ÀbÉz­ayMyD"ºÇBÚcq\x000b\x0016-`üÈ*º;D6ÏÕîª|Ûþ>c\x0002K[°d\x0001m\x0008\x0016QÑNmL^?%í&%\x0006\x0016Ó\x0010¡<ßß½ûðæâ÷ÿùÀx 
uÒ7Ös C%ê­Jn\x0007\x001ewÃn¾¿~zóøâgÿñÐP \x0005Ã-\x0018ZÀ&&nªí×&zTC1\x0013\x0017m¹ÈÂÅ-AI\x0016Lg\x001cÖ+rá®\x0012ØÄå·\ÞÂ\x0005¨*0ü!E¯ÆµÙT\x001ewï\x001f&°°\x0005\x000b\x0006°z\x0005Ö¡(Oö©huKý»$¡	,nÁ¢\x0005¬´&J¾J«·\x000bªO]q§ÀÒ\x0016,YÀ\x0014W¨óp9²`»Ù3&®¼åÊ\x0016®\x001a\x001eJ¤Ð¬«ÓÁ\x0013¼÷§ÎdÙ\x0015Ó\x0005ÕÁÀj]åC:
­½ß],\üK8ä_N\x0004¼áW0\x000b%«\x001cA³bC2ÒÕ\x001f\x0016²çoo_×øõýÏw\x001fÿüæîÃ/kÔyARRQ¶Ö¦â]\x0013þäêQ
a}sýâùãë\x0007$ê\x000e::0Òeù[êTÄþ§A\x000bUÊ \x001d\x001eKÛ#í\x0006\x0002|üóßÿV£ÿ×\x000f\x0001Öàl}oFîfÌÚ×*5¶tOÂeUÞñüº^\x0001\x001e@[B´\x0012R):\x000f
¹_<i\x001f«6`N³´%$;a5(ká#ò|4)<ço.1\x001d[`+¡ß\x0012zûWFXÕ@°\x0010hÿJÌ2;0ìfI\x0019ùÂ/\x000c­àÚ³¾¬ \x0014=ò¶\x0015ÜÍ\x00022\x0012Æ-a\x001c ÄvNÂF¦$ê7Îx\x001c`Z	Ó0Ù	ñ\x001eËG\x00069'èJûÈ³yKíõÓBY	!jwÈÚW~×«d%,[Âb&Ì)¶-æº%Eð4è_ª!éä>ÜTlÐfa\x0011ù\x0000Ëg®¶;®9$%¤Ý /#`ïPÌ\x001ee\x001dò¹ÚëÄË)ë´\x0000ýì\x001av\x001e\x0005\x0006\
ÈFt¤¡i\x00082É®.â®RÝØ¹\x0014\x0018ð)^ËLêYqÒ1\x0014r\x0003Ü½\x0017Z\x0001;\x0002fB\x0005@j\ë\x001a:UÄ	í,ï3\x0001VÂÎ§ÀSA¹zc.¨û0DÕ>@þÈO\x0001§Âõ:E\x0010

p\x0015§"æã[¸\x0015±s*0àUêÕmÍ\x0013ÔH°yæ )²úïÊÀ­S\x0001»W©Áª¤\x0017ë"fiõÅ5èf×°s*`÷*ÿxÏWA»WIÁË#\x0005Vw¬×\x0000\x0016\x0000ïÃ¤_ÁÎ¯ Ý¯ðÔÃ\x0010d'zM¼\x0007_Ô¯2\x0019=`S±û\x0014TneYEÞ¢ØVqr/bçWÐîWxüg\x0016Äz7M²¨ÏnöCw\x0005íÛ¼,¢&Ú¸3[MÎ¾ÂJØy\x0016´{Ìºø©-¢èVùz\x0019ÀÝ\x0015±³Ûh·Û+\x0006×H[\x0019Qgvë}\x0005üô}6=2Ë½ùµýj_Dó¡^ªè ø¤â\x00055f½Ú÷¥´-ö0Yð"ÉßjÁ=ñõö\x0007\x001aÅÙS\x0003y\x0007GHy&\x001bÉéá±í:\x0017b3AÓÙM\x0003áòÝ±']kJÇ5mâ()k¾LO.§+?ýåóí¶p¹\x000fÊofÏ£	cÎ©îgð¹yÙP×í>¾\x001bÚ¦ ,\x0003¨8q\x0008¤g>ï\x001aì»ôhMë.\x001dXÑè@d¬¸(NW\x0014¼
\x0010ì;ÔÍ6þ´À\x0001Ò\x001c\x000f.½8Màú\x0002¹Ý"¦ÓÏýqúÙnFÓ¢kö,_ª'eL»\x0017 sðv¼AqÌBÖÃºC³¾\x001fs_¤ÉÕÄ°\x0003
# 9$i©\x001e¾-õ)\x001dÂ¤Ñ3Ï¶©KÜsÖJÂá«·?ß}øtñèö·Ï_nàÄt°eµA­0Ìk¥G\x0008i7-÷êÉ7×7//\x001e]ýðê\x0006NEÃ-\x001aÐêuÑµÂë£_biÖr¼\x0015mh´E#\x0013\x001a\x0014\x0001ºv \x0004iÊM\x0014ej/w%6´°E\x000b6´Ö¿\x0016×>\x0015´q§ì\x001e½mhilhª&Ë3\x0017uÆ+EÑ¼\x000eGjÂv´²E+V´uz\x000cYkþ+ôÄ$Úf\x0013\x0019ô\x0007ÔvBW\x0001¸z\x0010CûR(\x0010QåS+¶5qëª©û\x001dÐÑ1\x001dYé¸^¾«ksqëa¾Dö¾SpL\x0008¿õËéè=·þ náÇú\x0017ß½ûtñòýç×z¨O,µ±³)%U¾ Y^Ë¾xæÇÇÕY=}yñòÙ«Gß?Ô)¦|¸åC+\x001fÎuMèô±¼ª(ç´»\x0001i\x000bHæ\x0005\x0004­¹NÜí5ù E+eßÝi\x0006ô[@o^Á u±É\x0011Ç(ë
J`Rã]/\x00190l\x0001y\x0005\x000e\x0005OèuFF=\x001f:\x001f)í\x0004ÅÌq\x000b\x0018Q¯zZ\x0002Æ¢5õõ4½|iKÌËçåYe\x001d0#«§ý/õ^wü2óå-_6ï¿ÔF ðT\x0019Ù~:\ .åôú-_\x0019X?N\x001a¹9¡- Z\x0018Ê³ÁåéðkZÁ CdÃf\x0013|]w°w"v/R÷ Ì·«×_©(Ü¬!îî\x0017fÂÎÝhU-\x0007¥Awa\x001bjèvõÑfÀÎÝx)\x0017©}ÞºúÝ´ÎÕÄ\x0004"\x0015ÀckT	
KûÄ;IJ3`çFÀîG \x0019\x001aª&GÌò)ïÚ\x0019Ì\x001f\x0001«#áMØ:t\x001cñ.Ô£écÜy\x00120»\x0012P=>\x001e¤¡jÏÕVk_[Ú\x0015à	;_\x0002fg¨\x001fµÉçÐ|´«©6\x0013vÞ\x0004ìî$¨±\x000eü¸Lzu4Ù®:Ò
7A³7aù"\x0001äÎwÐ_La
"fm5vÞ\x0004ÍÞ\x001cW)­\x001fy\x0011\x0016BÝ´k50\x0013vÆ\x001aÍÆ|ÛÁë¤\x0014z÷½#fÀÎX£9è÷®
\x001eËËÈ\x00050µ\x001còôGî¬5­5¶
¹\x0004Vz¼bâ\x0006»d°³Öh¶Öu
e9\x000b1å k\x0018u
wmfÂÎ^£Ù^³´bbÖÐºZq=ÉÓ¡5væ\x001aÍæº.a%d!U%ÔôB¤é]ØYk4[k\x000f^\x0008 \x0013oë¯º¹Ìº\x0013ê¬5­u]A¹~z,Í$\x001d#\x0017a'c&ì¬5­µ'í\x000bã±<A\x0002×¤M(Ü¹<KØÅþdý¹"I;)Eí\x0007¨úÐ\x001c9{N¨3×d5×ÙF-ÄÓø\x0010v=ÕfÂÎ\x0018Õ\x0018ò£«©Ô\x000b»¾Ãù6xmyß$ì!Ùó ¤'\x0005jâò¼ØøúGÓg¹³dµKy¬a½LËk/Ã¾Þ«fÃkêÌ!YÍ!_Þ×2e¦VbëAYJª\x001e\x0006ü¢æ\x0000úÎ\x001cz«9Ì¾5Ç\x0002ig?·® ìÙ­+è;kè­Ö0\x0006¬D]\x0008RE¥\x0017ùiç;kèÍÖß¥×µÔ<CÖÐíÄKÌ}ÂÚl
¹Àc®¡Ê
WG¢Û°\x001c×Ê\x0001;cèÍÆÐµ)~\x0010^Px"¥\x0000¦]Õ¦°35Þ\x001cx¤9u\x0016¾¤¿o7\x0014ÚÏÊ³\x0012Æî#Gû
%ª´\x000f\x0004lYÿ¤â\x0013\x0014wïþfÂ>ëoÿ¹æÌ7B\x0019Hj¨÷Ñé%ì>r´~äÈ\x00026rNx,D¯N¥\x0002êYB\x000f?ýzd\x000fµBTlÖUôº\x0013±`ûÎ»æ\x001e{ºaû>+)\x0007} 5lÈpI*Û;@\x0006M\x001fÒtØÏ\x0001,¬\x001dC±tÈsj¦ÚüóÙ<'8w\x0018;²>Y8;ò;r3Lùë1¥qwþ3!\x001cÊõä\x0008ýl<BÕKª\x0004¸ZOUg4(ÛµüØo/Çû\x0006öeÔT{êZÊEßT%Ê®Zj`)_\x001f-åkëRz\x0011î­KY´¯h1{C3\x000fy{\x0004yku<:)jí¢§iÖ0|:CI¶@þb]Ih\x0011\x0006O¶\x0012sÙ´æ(îê\x001díWÖÝ¶#Û2ª\x001aË	Jwj.ÛÍæµgäw\x000eÈ
Øuji\x0000E\x0005vx¶¥¦óæA©ßõnlÝÕãÈ3eÈm\x000f¤©o?½7¡ì¼d\x0019qçQ_\x0003CNz\x0011cÍ\x000f}lÛ¾²_¶·\x0015ãráÖqÃ£\x001bJkq½1¶
gB};§]ñ=»ÛydAf/|H*Ã/rË~ã§Ý§/\x001f#*(P
±I'éç£j>ïÌ§1<âØ]T«ør!iR\x000e·3|õ£ÝÙ¾;ã:+iùê.ªQ¢\x0017ÉPvOìÏ4;Ð8pêö\x0014Q+Ï£4
­ª>ÑïT\x0016íiãíéÂ$?¸[S\x001bN¿ûüMÝ<Ú´îÍÈ3Ö½I·Ø.¾\x001c¹wá\x0007GîÆøãs¿øÓ1å~oì.\x000fx¡Øî\x0018ì.¥_Ñ;Í¬Vw9}|à§OG\x001bóÓïÍUº\x0007\x001a	=°U\x0007Ô%le4¡\x0015ùéÐ\x0018w¦\x0008G2	u\x0011%é«?±¯\x001a!ÅPÃ@bæØ²ÃÈÖt,t±&f\x0008\x000egVùÒÄÌt±Åî¢\x0003\x0017
ö@r#òë8¿u5õ¢\x001ew3üì%\x0017Gá{0ï«8ìZ¸\x0002ÚøG1è1Çö½Zøx1GMjbÎªÎÊBz¦\x001fz\:Þido\x0011I\x001c)ÉåÒ%å\x000c³u¥ìþxì\x000eýáhwi£ÏÎ\x001a\x0004$\x0005¨\x0019mßSXÞ©W/dôé±Þ{õ/DáX×Aã£0|Ð ïé©?\x001c4\x001a?.Òì¿Þ}úôÀ´N\x001e$_;$¤ÄÕ	íî}{ýbQgÿîúåË¦u*\x001cnáÐ\x0008\x0007*T\x001dØûÈÀ1ÒaÅ!»ÝT/+\x001emñÈºvE
êÚ\x0015\x0011Þá\x0016A¯«wO¹
Ïoñ¼\x0011\x000f³ÔÙÄEs¥^)°ìñ$^Øâ\x0005#\x0007mÄKõæ½N\x0006ðN;?³»G­ÏF\x0017·tÑJWÃ2¡ó*ÉQÿb\x001f\x0014ï\x001eU\x0006\x001b^Úâ%#^½j­¯y«Ò@ð ¶ÕÞzy­«:/Qb+½®\x001eh\x001b£ÛÕ[ñÊ\x0016¯\x0018ñê_íöqIt\x0018yõ&íÊF
m²û½-\x001fô>Ãê4j SG¹ OÆ(yð\\x0005:·\x0001V¿¡f'y­\x001a\x0001^«þCÎµ\x0015®s\x001a`õ\x001aÉKÂdéÆ¡Å¾õ\x001fÝ
Å×9
°zp@\x0000Ï\x0000«ÓàtC\x000b¢ Z?®¤êÇõ³;¯ó\x001a`u\x001b1µñ­ÅKð\½oQ©tª¯s\x001b`õ\x001bEÌ\x001e7eÉÎÍi íõQlpÓ\x0000«×HñR\x001448á-\x0007×;\x0015÷»6\x0004+^ç4Àæ5ÈA\x001d¹Ú_ø²\x0018\x0004÷(Ïø°ó\x001ahõ\x001aÿàÏÀßÙE\x0003ûÕcü£é:¿3ÍC«ÍûGÓuF\x0005­Få\x001f}ÁíÀk0zPú\x00173\x0006\x0017ú[.Ï\x0011xåÛ·\x000f\x000eæ\x00127ytLÜª!Oâ^[ñw\x000f¸?\=yp\x0018´Âø-?\x0011&ËB»,yÑJ\x0002\x001eÌ;\x0013¶8áD\x001c.Îªº\x0012.5y{Häíj)O¥[xêâDöûÅÉÓ¶8éÔ\x0013E%\x000b¨¢n\x001c­â\x001eÑ³=jëîÑ£öu(§Ê+Ë¥¾^ä¶F»¯Q!ù>ýVàôÛÕÛ·ÿ[=ü/þýöÍÇ×w·/^|~`ê\x0019~ÙLèÒpM¢Ëy¶ç©ª\x0005xuñïW_<º¾zuñâÕ\x0003³Ï\x0012·h§Ì\x0011Îõ°Öd«¨qTg¤-#\x0019ë\x0005¹UDß
\x0013$\x001dpê ¥ßRú±ï-¥[A·bP\x0011;ÏWç)Ã2\x000c|ïÔ\x0006.pªJJ:ÒuFe2n)ã\x0000e]@Ò\x000bWýU\x0011J}¢
}Ï eÚR¦\x0001Êê½¤}êÙ\x0011á¬m¥ô]\x001e{2o)ó\x0000e¢ÅÇE£Z\x0004\x0017t²\x0006w^á-e\x0019±C¤ÎÎ»¬ûÒçÖYÎ°/·cTü¾3czº\uÜø\x0002ÛÚZóY½á\x0001³w=\x0003¾§\x001aM\x001d°Tliansp»+÷ eçz`Ä÷`\x0011]Wïckÿñ¹u^÷ªK÷\x0001»û©Nd\x0017LÅLÔdöóû\x0001ÿÃ«éÔhnÖÕ<`ÁKBç`Ä\x0001ý3>ºÛ\x0014I¬òv êhF±Æo¤Q¡ìè\x001cv³W\x001eörÍ´Û¥p)33j3bpÚU\x001cb<CìYó\x0018klUÙ\x0014@5\x0002j]G <±°p<ã\x0016\x000e3n+â£?ýýÿýT\x0011¿\x0017Òr»a<~-\x0014¯\x000eIzXKû¹|¯.\x001e}õ²²}+l¹+¬[¡¨÷ÊÊµ\x001fYcà[®háª÷.\x0019q[Ú«[\x0006Ñ\x0004«XûÔ½\x0001+m±i¹\x0006\x0014Ë\x0014>Áé\x0001`§@lÁ*[¬bÁíyÜVÔ\x0004*¶\x001a í
\\x0000\x00076ÓZOüNÙR\x000f¨ÎÎ^¿ã®áÚÂ\x0005\x001d\x0017X¸ê*­¿jÎN]\x0003\x0015\x000càw=Â\x00160ìÀÐ´`I\x0015ªøùJ¦þ©{¨\x001bl?\x001eÓÀÕ/°Ø/PCTø÷«ýr¬S¾áÔu\x0007\x0012L'2h\x0005Zeðª¥\x0004\x0011\x0004\x000cijëç\x000e,[Àx(ÝºÃÈ©4+R\x0019\x0017 ì¤5
\Ø\x001dI4\x001dI.,\_Î\x0000tF\x0019Äu½ü\x000cW·óÑ²ó}µ§ 6ûAdFw\x0004]0Úg¶
`¾\x0003ó\x0006°¥^p\x0005è´t\x0010\x000bÓ~Þ«Û`hÙ`±¨S pd#RïÝÌ®ó]ìk{ª8í`¢\x0008`\x0005ç¼1\x0004\x000c\x0001±ÌD\x0016é/Yñ\x0012×¢¨\x0007ðâÉ9\x000fàâ1^´áEHÜLyZ\x0006\x0008®3îT[OÁ\x000bú\x0004oýaà}~ûùíÅÕ_ß¿ûò\x0005\x0006	¤²¿~A½i\x001aÆ«½°³_½zrqõã³§_'ó[2o!9\x000fµ|ÑÔE#l¨·¬\x0019°¸\x0005&0\x000e\x001aW\x0017U
·Þù
i\x0007Ð=yG\x0003YÙ\x0015\x0013Ïr\x0008<ÏÒºd¹H?Iõ\ÝÐ3+\x0019tÛ\x000clûçâÕ¥\x0006-EËy±×ê1 ã\x0013\x0010´ÔxÁúîó·oï>üöþÝ_0ñÑË%y:^ºíÀí\x001a\x0016¶ï^=® 7?<{úÐ\x000bV9~-í!ötDGÈpÖº@ArnW c'ô[Bo'\\x0016ÂêX¥æØ¡
ÚÖðä¸ºÍ\x0018¶Á¥l\x0011\x0008[­]rA¿ó®¿Á\x0018·ÑX\x001dYU¬Aúú\x001aK9V\x001eh÷¾lGL[ÄdGÔ\x0001Ë&AÌâ3êÞ½òÚ\x0011Ë\x0016±\x001115DÒr·XN\x0003qe'ÉjF<ÜW\x0019Qï«\x0006Fò,]¿´jèÅ\x0012õÍ\x0005¸ d±3:`·:n\x0019t°0òxWYG4Ü>Ø\x001di0éúwIÜLÅ(µÄ\x0002ZsP¯ØÇI\x001c;cw`À|bx`ZF\x0014u[~ª\x0014B¤ãØÔNØ\x00170\x001f@A\x001aª&°U\x0007\x001bÔt\x0015i~\x0015±;0h>0¢ ½|ézCZû©x¨«Zï¸Ë¦Ø\x0019»\x0003æ\x0003ã¹ò7­ë¥+¦Öò\x0005~§ênGì\x000e\x000c\x000f¯\x0017Me\1+ ×ïÝq!ëÀ\x001an\x001b&e\x001dµcÒÀAj%\x0016û¸¶óVëØõ^Gd\x0004u[V´¢êÍÎ°3A«°Gy®×;NÃèWß
\x001cpÇ¤e\x00004rãUjÑÅÆ¥É½Ã~,Â@vL\x001aFHW5Ê4xñ<©FÑúõ÷
®\x0003Fó ¸&fóg³Ý\x0014£É#½ÖÃ©¹ý\x0008×Ó¾Û¡#Ëé\x0013Éý«~ø$ý1Ehaå.\x00011`ßw¨0r|
{ÅÊg
ø®-¤û6þE=¶PaÀBQÑ^¨eQW%Èú¯Ô,Ôî=ddÞ\x001eíÑ[ë®zðÍo'l¾}âv\x000bñ¨×gLÕ ðño¾ýøñîâú÷o?ürñèO·ÿ÷Áñ½ moÞ±¦YÒBÈ\x0015\x0011;1äÇ?<¿zñâúâúÛg¯®n¾å<Ùÿ~`,®"ú-¢·#ÖXxÿE¥DÍá¨2\x0018\x0008Ýô dÜBF3$Gé«¶\x0004×\x0000«øVÐ\x0010	9fÌ[Æ<ÀHz\x000b/a\x0019fµ26[4ÿ­7oqíÁ´2f\x0005lúëlzÔ\x0004u¯ûVDwÔº_Ø¶î?ºýøéý\x00078-Ó!\x0000Ñ5¼°»8rÓÀ£«\x0017/Ý<Ð1 `¸\x0005C\x000bÏºn¨=ûõÆÓLwØEl&0ÚiÅ4ýNK÷´®XsÔi2ù-·\x0005!Põ\x000f³ïGÔy\x000e\0Á\x0015¶\Áô%£z¶£Îê¨ÑB³#S\x001f2n¹¢+ôÔõk;VVÞs{1q¥-W²p¥%§½®Ñõfª2}È½¥\x0013`y\x000bM\x000bæD¯\x001eÉ¤\x000fý|KàÜÛ`t2XÙ\x0015ÓiõiÝlA\x0006ê,äDî\x000b\x000c\Ð\x001bWu­`$G\x0012\x001aÿØ&Çß?ÕYÈ:#\x0006&+Ü¥^2½>\ÇvsÇ{[POæêl\x0005E=%7°,`¨[\x0001wYBuí\x001e_\x0017\x000b»í²;á\x000cÈ\x0001 ÁFÔûj2vÁïIpèè¨\x0003¨º§ºÏ\x001eýéî·7ï.¾½ûø×ÛÏÿçËAy=xRéyrõË¢¤ç2b(zôýõ\x000f2ÙW¯þ¯Sá

Tõûé\x0014)r©ômï­T´¥"ËZåK©§çÑÞkvE\x001fD"áÌJù-?	9\x0008\x0013I<2k7ú\x0014Ú\x0007ìbD+VØb\x0005Ë\x0007,kepùÒ	\x0015éb%pi*n©¢a±À«2¯\x0001õÚ\x0011\x0011+b2ØUuY±Ò\x0016+\x0019°<èDg_×m½¾ûÜ¦3ºnp*o©²ªµ\x0012h\x0018c©~r_+bÅ*[¬bÀ^[×|Î\ÍX\x00014T½À¯\x0011kÓuÃvÔ\x0019¸R\x001b²\x000c¾[3[\x0001\x000f\x0017q\x0002«3¤`°¤ä@í{µôkCU\x000cÑ)Vt\x0013V\x000b:K
\x0006SZ5W¬èI\\x0017+¦v\x000e»\x000bª3Z`°Z\x0001#'úV·CRWÌz~º·ªc\x001càr%öÞ°þ \x0017ÚG·¿qêìâÑÛÛÏ¿Ü½ýrô\x0000	Z]^õ>qþ¨K¦yû×»GW?pæìâÑ«Wß^?ù:`Ø\x0002\x0006#`]lyÏ©¤=%ô@q'`o\x0006[Àh\x0004ty©\x0017\V°\x001eÖµ7*$z§,&:
¶É
X¢Ö6'\x0019B\x000eRÇ]Ï³y\x000b­AGgÖí\x0016T´L\x0007ù»Ùf¾²å+æ/ìT\x0014Z4N¤à(û8\x0011~2`\x0000ì\x0003m.9\x0005#øð¦â}®ÿûóÁ\x0013oE[²ê2%ØX\x001aÇÝÿ7+Ù«ú¿ÿíõûß~ûüîNÿý
·Th¡ª×L\x0000Q<"©N\x0019ªEÚ\x0016«-×\x0017¸hËE\x0016.\x0008mµªUvbM¼S.÷Ëo¹¼+8-Tå\x001e¸be¹/H;ÑC\x000bVØb\x0005Ór\x0011¯ÑÅ-ÉëgL¤eª¡ì¿Y¸â+Z¸êíMd\x0004\x000f\x0011eÓK!B¨>áøÚkáJ[®dàâª^/Û§í¢:+)Q
9Îpå-W6n{\x0017ÅHdëwTq¹\x0008;Y{\x0003×!º]³Uïeµ1.@=»Ì¢\x0005¬³_`1`Paìë\x000c¬Hº~IUÀ
y÷øiùý[òbò\x000fz/§¬\x001bwaË\x0007õiÍ\x0014§T\x0018\x001fÞ£aôU«ïbì}\x0011¿ /úæý\x001fÿóâÿù¯ÿ¾z÷ëÛÛ/'¤¼Íö×ë69¥¢}\x0018vMNß<{üâÅ\|{qõô»'W\x000fä¥\x0014\x0011·hG¤C\x000c\x0015}H:¾) ße\x001bÍ´E$3"\x0000h\x0000ÔøCJÊsÈ¨<åød\x0011ý\x0016ÑÛW[K[EÑSO\x0019õCû]-\x00191n\x0011£\x001d1ù¶5:ÖÉ\x000crQ­»\x001a\x00163bÞ"f;"YHO`\x0002¤2{ìåëã$âÁ@/'ÚÙ7#¥v^ª¿W\t\x0011wÕfÂî@ýD\x0003·¬¯ö\x001a\x001cpåñÚ¶\x0012Ñ¥é\x0013Ý5ÿ¯\x001f[¶å{~\x0005îh÷D*1û\x00113'\x0006ép¸Mð\x0004\x0002}ì¸x{{ñüöÍ3\x0015´9-åÄvÁá®ôýÛë'W\x0017Ï¯\x001e?¨P*ÜR¡{Ê¤ÙÚÈµ ïÛÜ:AE[*2Py'3Ø7Q©Ö\x0001êüþqûtª°¥
\x0016*`¹þ\x0005+Î\x0019\x000e\x001cßI\x000fûî>hÁJ[¬dÁª,+Uh£ÌëhªÞ°g>aÞRe\x0003\x0015\x0002OOZ¿aáðYÃupû¶g\x0003VÙb\x0015Ë~oSËo£:ë"5=½ûÉT`=mô\x0011NZ­¢:y, ASÝfú\x0011ËÎQY¸ze1Z\x001cÁÉrñ$')¸\x0002½ÓW;±:>«³\x000f`2\x0010¨:s¥Ú|ÐMOÚ\x0015ë÷ò\x0008\x0006.ßqùÓ¹ê5A
&+WÔ:&ß.Ïî¾\x0012Ó¹:Ë\x0005\x0016Ó\x0005\x0007\x0015\x0015ÇH"2UTuv3U-\é\x0002írIrµô"£â£Fâõ?òWì®g<¼ÿ²û4wV¤ã¶ê¦W\x0011\x000eº§ÈêëtDGDý¡ÀóæÃûw¿¼y÷@aB
Eï
Gk÷ÍUöïãgO¿}üôAyâ#ÇÍhdDó"L\x001a\x001cO©\x0013¡0\x0017¢Ê=GÓ\x0004\x0017¶pÁ\x0008ç4åXQZÃI\x0005öøÞ;?æt¸´K68VGsMÁä\x000bÞ[Òg`+[¶bdÓ;\x0000«\x0011¶©n\x0005táp×\x0016iþ4\x0018Ceéc¥xÖ§YéZp½o 6ÒaG6:ÒöæE+J"4J¹³÷(8®;®`<¯õÒ)£àYÐ\x0007eªm¡¦4tO f¢ëÎ+\x0018\x000fl:H\x001cWr2Þ[sÕA4I×\x001dX0Øz#\x0015ç\x0000ÉdÖ+¾-¸8{*º#\x000b¶3\x001b\x000bÉ(¯\x001axi2á7s½¯øIÝEÛÉkh³l:ÞÉ+\x001aÞ?nçt´îH íHÄ\x0014%PÑ\x000eæÄép¸Wú±ÑùÎÛ7^a¨¨õ^cÌ}ÎÇ-F:ÔÑ¥^\x001eP\x001c\x0005¥¦o¸S!0®\x001d\x001eZïÕCi½û½\x0000Bêg;,V¥\x001bîp\x0002$\x0014\x0015çÖ\x0008ÙAC/LÊ2PÖ°5ºµEQp\x0019|E+Ò»\x0016~î»×Nå+Ç¡qYBãGo>ýýo\x000bÞ\x001fn?<\x0008çë\x001eiÀè\x0008Õ\x001a³¯Çàuå_®t¸º9
·lhdÓn_ \x0003øK\x0012EaÝ5ßÎF[6²±q	,Ng«Ë&]³uÙú\x0002/3ß¢ùß×²-[0²eyþ­.+ËÍº²¡n7×cÙâ-ÚØ|Ú²á¦\x0015­»ÙÑÒ\x0016-V²\x0004\x0012ÖÕU²=,Øåìhymhü ¿\x001a¯Ë~q^êBØü±qó¥Ýû¼ÿüæãÅÍÝw·\x000f\x001b5õ:\x0011mÌÚíºkÉyòìÕã\x0017\x00177×^=$kìm/í\x0019áD´j)´ø\x0018J\x001bP$A§²6p´#\x001b\äè¥\x00143£\x0003ïqWffó[8oCÒ\x000eföJ r>,D3\x0007\x0017¶pÁ\x0006\x0007±
öÆ¢yüÊ©sfhwÅ1ÂÅ-\4®\\x000b±r®³sýÂ
nråÒ\x0016.\x0019\x000f\x0004´-Þ\x00176mìó´{\x001e7²å-[6\x001fV§lZùËUápw­6Â-\±ÁñÜi\x0010#çDÇ¡\x001ac\x001a©tÇC\x001bÜáf±ÀÎF\x0017
3/\x0012B\x0017¤>\x000fÄñõËH×û\x0007<ÕK\x000c]PÅ\x0006\x000eéØ]¬t\x0000£\x0008å\x001eÈÚE\x001e÷\x0005\x0000£à\x0002óõÒ×]ÌÚ\x000eâ\x0013ÌÙ\x0012è\\x0004\x0018}DLÀÃ0 L*âèÃ¤wÎGÑIäÂ\x000bÝA\x0014wÍ»"\x0016#\ç#Àè$Rnæ$i\x0013`ý°jMâìÊu>\x0002N"j×\x001dÕ¸Äëgm¨v5F¶ÎGÍI$W.eË±îFôa[¸¼Óm>
îgð}1ä7õö\x0000öù\x0002
\x0017j~¬ÿ\x001eñËa:zà%ç/cÛ²Sä\x0011\x000c÷LàöÕÍõýU@Ü\x0002¢\x00190i!5p\x0017ãº~ùPÚµ\x0017»4\x0003ú- ·\x0002bQ$Á%VYW°	%û¹mq\x000b\x0018Í¨%ò.ä\x001cÛÃIÚPfÀ¼\x0005ÌVÀú]¥Êù¦\x001dCÖ\x0015Ü·bX\x0001[¬²\x001e\x0012g%äd±\x0010Ö`9È&\x000cZ¤	~W\x0011g&ìN	óí#;§o(¹½¡\x0000ìKr¬Ý1\x0001ë9á&¯,&fÑ	ÍÚ+OÎ÷H°\x001b¿ò&g¬_z£\x0013êv\x000cM_\x001cÚH×º\x001dµÜìy\x0001¿\x0003õvÐeE©­hL»\x0015\x001d]P\x0017+â¡¸âù»\x000f\x001f¸ ôÝ»¦¾\x0012Ë_i4ã¥a¨\x0000j¨Uv\x000f¢Ï\x001f_ßÜp-éÓ§\x000fÍ~U6Ü²¡Í\x0005)ºö<ëa×I\x00195ÔªÇe§Èf£-\x001cÙàBKdÓìTÊY/\x001fõ»îTílp~\x000bçMp½TÔW¸(¯ð)\x0015Í\x0015Ý-lÙmáj¨\x0010\x000fë¶î¸\x001cå=e\x001e-mÑ
õ°éÀ¶v\x0011ñÃhcÛ	9ÛàÊ\x0016®Øàx8~S}JÚ ×ÉÞØÌH½:ªF\x0004·ôgé,Ð6Üîºk¤ë*ØÎ*FÒ¢\x0014¬Öx-èI©)Pú²W ´Ñuç\x0001l\x0007s\x0017\x0000íî\x0011¥©.D½{]/©î07i±ÁÎFç\x0013Ç)+]úzñh3oÝ.U`¢c¤
\x001dÿÍGhÌçÙ]ÈÀ\x0007N )Þ~VíÈv-v«mj­§Z<U»^.¾QL^Hz8v)>«=FD3b5.ù&\x001eá%Ú ë¹ o1Ä#=\x001e\x0001v\x0010½àÒÔÿù¯ÿ~ööÍ_ßüýÿûðåVE\x0016ùãÏ»èg¬c[
¨Ôq_XÖÄ/.\<{òøÇ
»é¦<[¸8\x0000Õs¬ÍW5 \x0002½ ¨Ò®W=µÑå-]\x001e¡óÚ¶»T\x000fÊå·[£ý½â/§ÀmÚ\x0000DBÔN\x0017²nQªa^7H'\x00012kQ\x000eÙMç.ãá\x0008^B\x0019\x0017´$°äÍ\x001b%Î£eÂ(]·ï`dã-\x0006eó<\x000bVÞ³¼XQ"¼W\x0005é$ºnßÁÈÆ£å-h¡#`5ÖN\x0012¹\x001bþ²Øm<\x001cÙxÄ\x000fCë¥zh½|Ú\x0002òic\x0008ÃÝÆÃÇe\x0003"ÇÊE!^VOx¬1úmýFÓ¿n½Ø\x000e\x001e
Ü\x001f
?q4\x0010s§­?üÛ:·ýn-ÚºþøÏo>¼û@Ñ\x0016¿AJ»nòd\x0006F
ø¤ä",ñÁLæ"_¿¸¸~ñ¿^=¾yöä!IC\x0001Ä- \x001a\x0001ë½^¤\x0016À B\x001d(\x0012\x0015°û¶C´\x0005$ó
Fa\x001b¸T¿\x0005¥ZWï¹÷Ì\x0016·\x0001ú- 7¯`1'!q·iPÅ\x0007©ªÍÐ
K\x001e\x0002\x000c[À`\x0006$n\x0008Y\x00009¤"ÕðÂÁºÓ{0n\x0001£\x00150§¶T4´°12½yË­|)Ë\x0003jH\x0008,Ë|±hÂyµ\x0004,[Àb^@/BÞ!ú,êu)9/V&A×`3\x0002¸\x0011üc3è¬1KÝy½M\x0006yÖJQs¤)Âì
Bo§ÍõÿÖì\x0018©å
0(!Á¬ÎPÙRse|äêî\x0008ÛEm¢­ß4ag©Álªë½wMÙ\x0007~&\x0011\x000bjÝö)øýÐH#agªÁl«=J¹\< w%*Î³¸½IÀÎ\x0012Õ\x0014¢K¬F¾\x0000bi¢.¡|äXºôÕ\x0010ag\x000bÁj\x000cy2hA±5^$Öñ'æÃ>±\x001e\x0013ä&eÙú¼XyLOI\x001avvuéú×RÒWoÿü§÷ï>Þ]|ËÚ{\x000f$8J\x0010ñy-Ì:ê\x0010á8\x0007sõäù÷Ï¾¨,½÷@CùhËGV¾z.t\x0000K/H\x0019Xw\x0018H»§K3ßòy#_XdP\x0017<\x0008º|\x0000¥	äï²f¾°å\x000bÖõ«'XÔÕËRÊ±ð\x0015§\x0013"ü®KØÌ\x0017·|Ñº~@mì+b\ø\\x0002]¿ýw3_Úò%+_ednnA}¤\x0008:hv##Ì|yË­|<ÍWÖ/£\x00166¹ÚtÈéï[¶|ÅÌ9±»ðñ\x0010± |mæÆ´}ÞþY
 /©MFNÀ¾d\x0001lââP·à,!vh&$¹r\x0012ë#Hqómpå¼ÎFÕH/)6]CÏ\x0010°ÍnÞÉk	;+
V3íS0a$yhmZnÚUE	;;
VCÍÊÕíÍ¾H7L*Q\x000f+Ó\x001f¹3Ô`µÔ5R¹Äfh¢|â¢sMö:Öf¾ÎPÕR{n\x0010KSÃ}¹\x0016× ¡Í©ã
3agªÁj«Y_¦«qK1È\x001ars¬áNèÄJxÈþ2¡>iN\x0018JûÆú W\x000117Àã\x0017W3`g\x000bÑl\x000bk\x000cH2Å&/®å#g×Ü]9~3\x0013v\x0006Í\êX#\x0006yS?¼xAÿò0DØ\x001dd4\x001fäµ]w%*·]kÃ<w"ºfÂî  ù p¤ªYËt?\x0010N\x001bCê\x000e
\x000f\x00032êP\x0015Õ\x000b5@¿k2\x0003v\x001f¬\x001fKvtÜd
Ò.xîÜëÜNÞÔLØ}d²~äúCCX\x0016¹ µBA4ùéxv
}÷½õ#ãª¬\x0010©¢$\x000f°)vª ]BßYCoµ<EhíR]\x0000\x0003ékIQÀ0|CÁ£ÇÎ\x001a?m\x001f;?_<¿ýôÀ+\x0018æµÖé|]É5²N< f¥c}ÿý+Ø«çW/o¾¬¿beÚbe2béè%VjK\x0015t@Nq®Ò-W1-\x0017\x0005\x001d\x00150É\x0010ÀTÃ*\x000e\x0012Ü;]å$.pýgt60/÷\x000f\x001fxÃ\x001cÔtïäÓ¸Èw\ä-\\m¿~È\x0010\x0014Þ'ô[óÉßûÆ\x0012\x0018B·Á\x0010L;¬Æï¢\x0015ÑK½}Â Ã½²£á\x0015Ãþß\x0002\x0016`R\x0014\x0016yfNR0P°ûÆbÇ¢+,\x0002;Ìøác½û ÆÅ9
//ÝrñZ,çûâ\x0002g	Ö¯}\x0013.ÄûÆ¡\x0008z°d\x0002C.iYÁd¥Rk+®`yøC¸qýçñ\x001aÀ «\x000c-xIö°ÅW®èÇ¹¨û¸ÑtÕûñÒs\x0010T-)ãð\x000c±Ûøü§\x000f@nyZuµæ«^yÙÆ;ÓÊjäR¥?Í*V0í¹¢îÙÄµ©k
KFÆ¸@uÒkø©µÞõD¶f°8\x0001=\x00186X"ôà¼×)Aªù
\x0019wXìw~´í|\x001e®\x0005Ì¶wÝù*²\x0006ü\x00145
\x0016z°`\x0003#\x001e§ºöõ¹f+\[±\x0012­~émX±Ù°MÃ!:Ö¸Z÷X[±è\x001e\x000f[@}D\x0006tôZWø·ë÷?ürûá?¿\x001cïg\x0008Rù±èúI2Ý{iuà¹Û÷Û×o½ºùöêæ?¾\x001cî+\x001enñÐT`\x0012E\x0015V
(=\O;G[<2â»Y¾1;mô*
Æáû\x0003ìÓñü\x0016Ï\x001bñ:uJ\x0010¥béi\x0011¼îw\x0006§ã-^°î=\x0014%ê@Å\x0007XFðú\x001e \x0011¼¸Å6¼²~Üä|û¸Z)}ï\x0000H\x000b[Ú²%ë,©º.\x001d5awUE¢ÂÖx\x000e/oñ²qé"ñ¥nµ*x)-þz(|ºßÚÎV¶lÅºë¢f\x0002+Ó¥n:åQlºß­Lw($[ì±3.]Ó»¢È·QÑ¼ðZ\¾p¡:\x001d¯w\x0017Fª\x0000ñ\x0017\x0016[\x000fR=A\x0005g-\x001etþ\x0002\x000e\x0015.åÉ&RR¥|Ò8¿\x0007\x0003:\x0001FÁQ:nLMÚ×i\x0017Aîðu\x001e\x0003./ñ9¬|®HyVFÕ¦çÇØY¾ÎeÑgpÙÝª\x0011ÊSd/Ut%èçÍ³f\x0019:\x0001F\x00112êÃzÈ v\x0019¼äÈ9\x0000=\x001eÛ\x0000£ßAç\x0013K^hÂy\x0008rº·\x000fÃÂ×ù
0:P\x001dGõ¨Ö\x000f°}ß^\x0005k¯ó\x001d`t\x001e,ø|ß¨K@æäñ4Ü9:ì|\x0007\x001a}\x0007«q®AA¨AÁÚ\x0003ÁEq¼\x0019¿p÷?\x001d¯ó\x001dhô\x001d!¦K/xI\x00162CÅ+q\x0001öW
£ëXfñÊòÜ\vÏMóu®\x0003®#ð ­\x0015\x000f´%\x001fZ¨ªg´ÌØy\x000e4zÀ
k\x0003ZN:ÍÍ\x0005½©--àsxã@£ã\x0008Õ\-OQ\x0014.*\x0014"P\x000eè±ó\x001chô\x001c\µ¶\x0005Näa³#yC¢äi¯ó\x001chô\x001c>ë[ÒR\x0000Zî$qAYÓÒù
4ú
\x001f6ðqÕ¼Mµ9\x0013ÊdØß@£ßðÙi[°GR¿V¤|_È\x0000ÌGç £ç¨S\x000fW5*ÐqI\x001cNÒÿéÓÝ£ÀùAnû\x0005ù]A\x001dd°CÆ¢=ô\x0011¡I\x0003s\x001aR0§£ü²Ã,fÌ\x0010tføâüdÂ
ð\x0015³×â\x001b¦wÉ¾M<i©í\x001a7H¹\x0005ý8\x0019vÇ'\x000c\x001c¬eÉ4´4>¤¶5gCüÿ©{»å¸åLûVú\x0006\x0006Q?õ\x0013:j\x0010\x0005\x0005\x0008Ð À°ædGÄÞÂ\x0004DÈ ¡ðöoÃ§s4{¿;ÐøJ¾ÊU««º\x001bUµÚV=Þ"\x00102ýL®ªÌ¬ªÌ7·iÚ4§PiN®YH'0¦9³©·¾¹nÆô4ÎÏ¡)àð7§á8rÏÐ}1
zSÏ]\x000fRcïîWn\x0017?Ý®¾,Þ®>ýñ=p(³ñwAf¥ñ\x001d\x0012¦¸SÂ½;_¾:]ütº¼X¼MzÌd¦F·1\x0013aC² ªð£\x0019Ì`¶	\x000c¼\x000c5¢"\x0010+\x0013Üø=\x0017bí\x0011É $&2\x001dù\x001a\x001a¨0ça[§ÊºYd®$smdçgÀP£/ãd¬¼×\x0018Íd¡$\x000bMdj\x0014\x000e\x000eÎ#ï\x0000¤Ìn\x0019ûÉ
¡o¾[Ð¼\x0018Ñ8b\x000e½T*\x000b­ª\x0015kF«ö¦nÚúVx>\x0015\x0018\x0019sm
'Ñ	ÍÎùºÚ\x0003ºi\x0013ÐÛ$\x000bËSí\x000cX\x0014\x0011\x0007Òí²sÐªM v\x001b{û!\x0018äÏjÑÕ\x0004ÔÉ`:ÖZÆô\x000b
\x0002g¿þ¶úúuÐÄ|÷ðeO!'ÍÍF8HÃd.§Y	\x000bAW%Ùgoß-ß¿\x001f\x00041ß]^ì)â\x00140S\x00160%úWhuñqæ6g°z
U3-Ál\x000b\x0018Ý'k¶\x0018ÊÓ3kUwÍ`PA\x0013ãÄ-YÌÈÅ32e\x0017õ)±\x0004Ã\x0016°\x0004eõx¤©\x0013\x0003(æª\x001cY3+©\\x000bUÊ~ØZ¤½Ï\û9*;çpùË7YKF:¥Ï\x0018Å½:\x0011§\x0005\x0015æØKWë^7-üðø\\x0002ei\x0008@N\x0017\x001d¸\x0006\x0003V-/Ý´¾@¦tÕh1äëöô)í,WQ\x001f\x0004\x0006\x0007K¿ÌG½.¬ùAÂ<î\x0004£\x0011ÃUÙìd¼°9Ð)Äâ\x0000ðááþÛênO¹ÑpÐÃõ|éÈg\x0013\x0015¥Ü\x0008väe\x001f.Ï¯gW{BRØ\x001cæ\x0014býOÁÒ'v,
òð)³t\x0001¶óéP¶²-P§8¤¤Ðïp(£\x0016¼ÕÛG¥éXPbA\x0003ó'ëyÒ"¡\x0010Å·jjºé§Â
Û¨XØ_\x0005UÝ^ÓJåJ*×B¥yZSÂ
r³oÂ8±ÁÚíÜp:/±|\x000bTJ\x000c\x0003ùBß\x0004©¨ÖµdQ+V(±B\x001bVa-+TãÊa«õ¹(Äò\4*ÅlÏÕÔÑÉmÙN£'py½áI½.³è\x000féáöË·ÅõÃÓ§_öµEy\x0013å¨écr­uZ:iÐí\x001fÎ.^^\/®/o^ý¸§5jEãgKÐ%½e&Ðóow	ôW\x001c\x0002o÷\x000b\x0005\x0006)\x0000k4*£å¥AU
@ç×gô-QîÒ
|\x000eÔ ¦\x0017/úRªÈêä\x0004*Á\x001e\x0002Ô v¦E-M2÷\x000c*%;ÎU]T½ PB\x0017h\úOóõø\x001cåÛ5ëlõøÐ\x000b%(önyN8©àèT9\x001c
Ó®\x00173t\x001eF\x0010X\x001et
\x001bÐ$>s\x0000P_ú.P-\x0003\x0012H\x001e_\x0017£rF>¼
ØJ¡\x0004
} @\x000b\x0003¨v¬pN£lùÓc¬\x001eá{Ac	\x001a»@
È\x0003\x0019ÉØ£\x0006f±<º}õóAÇxÝ½ê%e\x0005\x0008\x0013R\x0012©ãg\x001dtñ\x0000ß^×©+2Ñ`\x0011\x0016L1AÏãÐUÄ¤î\x00106­"î\x000bMQ¤\x0012\x0007:\x0014G:~ýª\x0008·´
Mº/6%C®²Bi\x0019ÎL\x001a\x000e±óu\x0015tgpRãÖ§q\x0010R\x0010\x001få\x000f`ÓêHÏI\x0014ý¢'ê{)g\x0002Eê²+õ\x001aý¬JG¿yÃå\x0007IÙßo¿<×\x000eôÏ«_þøÿ¾ìLy6y{Jæ
¸q2\x0015mã°Tr\x001fN/nÆ\x000b\x0008úçÕ\x0017\x0013HcI\x001a{H5È´D¤º|¹\x001aê*ö\x0016¥÷	tÐpí°©ÈÇ!Í1*ÐÐn±i%KÔª+TÝÂ)Û4¹©¬è\x001a¼~7ë«RÝ¤¶"µ]¤Yõx@õ ß\x0014Õ \x0000\x0008T¬Pñ÷®v¿îÚþ\x001aE	i¹*j¶ªj\x0002ê&õ\x0015©ï2*"\x000e¨T\x0005Ìß?*ùþXðêF
\x0015jè2jT\è¯N#Êu UÅQ7gåPuG¥¼wÿ(¤KsP¼¸Ôl)S¹TÓåRI@u4ë-"ìlÂa¾¾ýËjÃU­zÖªÑÜ\x00024§/\x000b\x0005\x000f£[
0Ë­¢Æú\x001e=ý¢|A}»züv·º_¼¾ýûãí\x001e\x001d`GóµXCÅÈÐk+½\x0008à+\x0019Q¹z»¼º>[/^þ|uºG	X m	i; ÊÂí\x0002¿8~ãDéÅEÜõFÒ	%&t`úÈ·¢	3³á#\x0017ÇÈ®¦VL,1±\x0007ÓñÅIÂ´R\x0006a"w·%kº]o­®Ät\x001dN\x0004ë\x0006Ý¡ V5Õ®ôVÌPb\x000eL0RïB·Ü²`FV¯Ô®\x0017ÙFÌblSÂ¤´ÓXn§\x0007O\x001646£Ð¨ßýÐÞ©+LÝÇ_fL{Â\x0005\x0001F
;9«ªÃ^ÎÊmê\x000e¿I\x0017ørÌi\x000c÷p93Ús×]~+gå9uëÄÓó¼Xrð<JLûh\x000ejÏÊuê\x000eßIplNÐÒ¤Ï®á ¨|«ÏÁ¨|«¼H$¢Y\x0012\x000bÉH¢¥\x0013É\x001c£ª\x0008ul'ÝñüÕê×»ûûôÏ{Rá»Rå¢Å\\x0011ùíÐ#X©\x0015qjû9ìÕòíÙyúÕ«sÒá;\x0019\x0012JHh$eW®Î\x0000qÊÝ¥l$n¿%6Cº\x0012ÒµCÂ\x001a\x0012G]«äîÄí7ëfÈPB\x000eÈQ¸&\x0005¥ü\x001eâQK!ÃíâVÄu\x0014"ÄõÓl\x0003#PÓ×À\x0018´I£\x0019ËªÿµuµotÇÆ¡ñv]c5RlipÆç¶éQ='\x000f«ÃÓð7·_þø¿ß÷>&QIQ&õ	\x0005V(
r´ðõ\x0019&¾_¼9½8½ÞãuË\¦ËL¤cÃ\x001f×\x0019í\x0019XPbA\x0013T\x000c¹à8P{;NÍÂ0ÇX®¤r-Ti·æ¸Ê1Y1Ì;±Ve­Pr£áZ_Y\x000c>69.f¢
s`iAzAË\.lJÊNáBµQ%~!ñüéÓí·o·\x000b¾æÞ_\x0004­øm\x001fé2\x0000 ½\x0015Æmiøß¼:½¾>kþùLÉg\x001aù<ÝðñÍwYÍ/rÂ\x0017¶æ\x00197óÙÏ¶ÚO\x0019Þ¡ÊXL>(ÛokÚw3\x001f|ÐÌ\x0017ø	?\x0001j)6\x0007?\x001aÐÙ\x0006Ä\x0012\x0010[?pDîTIFê\x000füN,¸9\x0004¡\x0019Ð®Ù¸¶ ðhÔdAVEHI´ÚÇo\x0006\x000c%`h\x0006T\x0012»h\x0006\x001fÈ\x001aò?ã·æýL\x0006´Í\x000e¶nvx½úòíáË>÷"£ÐèAs`JnèõîïåÅõåÅËXPbA\x0003\x0016=\x0015G~â°Òì\x0006^¦ÄÑ\x0004ð~¬õñ`-Õb.%Á¤£¤¬µ yÝuHå*c¹Fk\x0019¾g\x0007\x001e=\x0019H
¡jÍöfcçZ6Xy°ý¾e:\x0018mD×´8º¾}øò-Q-VOW¿üñ¿¿Ý®öE0±Ú*\x0016N!lÜ 7CìÛËë·XÞ,^ý¸¼>]Þ¼ÌiJNÓÅ\x0019é>5s\x0006.O§gkÁ\x000cÉÓ\x000eÌO«Ï«¯$\x0005ú\x001c&Ðô:Íò¾4\x0016D\x0004üZ\x000fy9_äÄ\x0013{ÌIºàlM+-Kô`-æ¬¦B÷bº\x0012Óuaz¹hÑ yê\x0006MÏ¾=l¯guúÓwqZV¯Iö\«\x0002F°bÏ­±\x000c=ö\x000c%gèáÔã aÚíVê¤Íz·of\x000b=ö%gìá´Qn\h}J\x0017n\x0018\x0013×Iëó%N]{Ï.÷I#\x001c\x0004\x0014h
dP\x0018
\x0007pºrºÇ:\x000cÒÖ©=p}WX_m°5V³\x0007ÔV ¶Ë¢;ý³kâ­äãÚ5mæ= \x0007Õ].Ô õn
 éÀÿ^²!c·¦ÙôV¾Iw9'\x001bYf\x0018µ\x001a[íúÓ\x001bs5ZmzÝµë©­?½F\x0012ÐeJ\x001d©ÒñNPSízÓµëµ\x0008ß¤OoGý\x0002ÔRbÝ!@«Ídz6\x0013Ý\x0016\x001aþô´
¸«OÒH\x0007\x0000M,äoøóÓo:\x000c«y\I\x0002ãvR¬\x0018\x0017?ÈJ­Þª2.ýæÈpÓq»ÎñÓ/$Çÿ~õôùnß±Ã\x0019éI7Vz#\x0002\6Z»8}¿¼y}¶çÈ!8¦Ä1Sq KK"MÇf\x0015{\x0004éµ³vë\x001ej*-iìD\x001aR\x001cdB£e\x0006\x0007õ;uÒ@I\x0003\x0013i¨·\x000eÆS5ïQÑwdÍ7\x0015Ç8n*åç÷Á:ü^£nÀ\x000cërßåÕ#ÛnÒ\x0002â±Æ¢\@®ÙFaswõîzxú¼ïPOÝî9ô\x0003¸È»ËG94Ã­Ñ¨ß_Þ¼Þw \x0017\x001cSâ81r\x001f~Â	2v-\x001d>dìÚöûÐT\x001c[âØ©Ö±'<mÍ{V\x0005ðQË\x0000mç¶\x0017ÐD\x001a(i`\x001a
hË\x0017\x001c\x000bùè´\x0018ÇÛ^ã`\x0013C3L¹MóñqüTÁnyÂ4®¤qÓ#Þ\x001f\x0007: ëÂÖ`Ð©8¾ÄñS\x0017²áGl )ñ<\x0010Ù®çôÞm\x0015J0Ñ8Êñcu®æãÉ³ãt¾ZÖ¥ yö\x001c/4±¤Sm\x0003Ê\x0001Òåcãp\x0016\x000f~{ðDã\x0014µ\x0007!·O]:VªÞ¬Lp[ÂaC2µ§vÉS}r´|A\x0008¥}df¡^Ê'ëN\x0019ÒaFñFÇq\x0000Yô~ü^;KW^POuFñ;\x0011 ×ãbo¤JqûFe*Oåxtç	Y
Ô@Ü²LZõ¸uÖ{g³üCÕå\x001fË_W_>ßÝ>îy
±Ò\x0007"\x0015v
TT4%\x0010;èo\x0017¯ÏN¯ö\x00151-Ùl\x0013IÃeQn>\x001d;ÒqÊ\x0016£*¯ypPÂA\x001b\\x0014áHþ¹ Î$\x001d³ÍkÅF4,Ñ°
Í[>
Aú!+j¤Hü\x0014Ù\hl®dsßÔËxNë#\x000f£oÊ\x0011\x000f£ÝUCÓ\x0000çK8ß\x0006ç¬\x0014\x000cD]~Ys¨eò:BØ\x000cÇp¡\x000b_\x0015¥qV\x001co\x0006#3×ÓÇV\x0004Eò"ª
\x000e
÷þM¾?_
:ÜûC\x001ex³¬¡ÎTt¦J\x0005æÖæE\x0007\x0012(ÑmÝZLK²>ÃÐLâ9þjõõéq_y Ý¦ç¦ÞÓd¾VË`ÚÀ®^«åû«}e\x0005%\x0016´`%·\x0011Ëê\x0005Ø\x0007\x000e»\x0004þ&a	
`$»¦s1\x0012cî7u¦"î*\x000cæJ0×b1­sÍ¹
isÊ3QôZïl0Ì\x0015J®ÐÂ\Ùk¤¼Pêµ¬f3H®m½Ö>¸ÊV	_ÒøBpëÇ\x0004%éVvWçÐd²jKê=é¢!!\x0005\x0004®Y÷4éÝêÉª]©[¶e¢\x0010¢à×«?È´y­í®^ÉdÕê×-Ëß¥Ã×äõo,?\x0007Ó:ó5+/ÒòÞ,kR&l\x0003\x0011O \x0012^ÖÖ8ÒÍsg°I\x0007t&pO\x0000ÞK'i\x0014H\x001cÐ}ÞÃåJ£õ.¥î2ê½¿ÿã\x001f·w\x000f_»}\¼½}¼ûõvÏ¼X\x0012KÈ#
\x0007Ù\x000c\x0003¨u\x0017©J~by~~zºxwuùþÝéÕâíéÕÙÛÓ¢ý´¦3º¢3º\x0003O¥%RÁX-I¥\x0011!\x0017º\x0006¥ÏÔ|¦/¬Pø\x0002§n\x0006ù¾\x001b¨Á«\x001bÏÖx¶\x000bÏè|\x0006$\x00010\x000føq/ñn¼Pã\x001e<Ð'l¼0¦tþâÅ§«ã6¼XãÅ.<+rÛt&ÌCÎ\x0011y\x0006ê26í|\x00066nÇÓ/ävüÛÇÏw_RÖ»øþéîë×}\x000e4	>GEz'üÒâe
\x0011Imd¾?^½>»Hïâû³÷ï÷]?\x0008£-\x0019m;£Q¢\x0012G:¬Ùù!òI.\x000fÀ\x0008%#43\x0006çeL¡6QÆ\x0014BD\x0004»yÜï`Ä\x0011Ûí¨ÇQ)ýaá­@sÙÅ[¥N\x001d®tíLç¯|IhbXWÔ:~×¢&¾Í[¹\x000eH_Bú\x000eK¼kLFæÒ °ÇIvÜzìê`\x000c%ch7d\x000c<ô$ÇAäV$öÒ\x001f\x000e\x0000\x0019KÈØ\x000e\x0019\x0018Ò{>w\x000f\x0019ò±·\x001eÆÚ\x0019×ù\x00031Ê½E\x000bäxwr|Cr\x0006¹`Ùð4n« ¸RWºÒ¯7\x0003©ÀAÅoøÖ­\x000eÊ*Üèöx\x0013è=)IUûFI=\x0003\x0007¬ân\x000f8ÁE~æ2±\x0018ó\x001e­ÒoÝÄwPV\x0011Gw<â=RÉ`f:ã)·Z­:(«£Û\x000eöm©lq\x00082_ÎÀV?S\x0007e\x0015ttGÔIhfÈÑ\x000c\x001d°¤'ÁÈÜ6£·Ú\;(«¨£;Âò¢ò8ÔWJÑ\x0010ëUÐ Éù»G¿|¬#ÏÇã\x000c=Õ?'\x001bR;ÓäÜ£ÌÐU£Ê#Íìá½n\x00017ß:XMY\x000e3u©\x0006lJÖå-.eënüþ,«B²+óÝf]f
ò\èX\x0005Nªè\x0012Ôüm¯`Ó¬ÐeV®p\x0002c\x0006â·Þ7»ê\x0006§ëá¤Ô8rìzì\x001bô"ëmõÖu×öÿToÿOí\x0008P\x0001Øx^ão/S³Á\x000fpÌ0ËÔô,Ó(iF9ü¢l}7\x0007ÔovS{U\x000c\x001fù|»¸_-®n{úx÷/O{\x0006
P<â~
ÒôlM\x001feúTmÎ,\x0010ñútq¾\\¾»ùþüìnöh»ùÍ¦e¯¹\x001f-ý(\x0015Fåµ~\x001ceq{è_;¦+1]\x000f¦>ÑÀ c\x0011ÐË|\x001e»c];e()C\x0007¥\x000f,¨è=¡\x001e/0;\x0006(6S®ÏED¹\x0016XiÁt<0d&$ÆtR6\x000c»c¶sV;H÷l!\x0012p]O|^Ê\x001a\x0004\x001d¶Ç\x000bµsV[H÷ì!<\x0013<qª\x00131§ÔÚì\x00187Ô¾4Í:»Ë\x000eéc\x000f&»#G{!eæ\x001c\x001cà§À¾ªýÑªÒrI;¹Mùä\x0016G¯¹-þÓcÍUmÍ\x001eN'
Ã,3ÙìÒn\x000cõ0³VRËOk\x0005 Ò)ZÏZ¿]ü´zür·úô<!ÝZçã0µoÒ\x001f©0ÍG'o×¡ºÿÉÁ§W\x0017gËW/ÃÙ\x0012Î6ÁYå¨\x0019rÓG¥ó¹Ì¹ÑXù \x000e8(á \x0011\x000eå \x0014Udeæ\x0004'õB\x001açZ\x000eK8lÓRÀá¹°Ä\x0007#ÅÚÎ%ó%o[pAz]¹Êfó£4¨Z§\x001dN×»¡m;X7>G|=ÈDvU@ô,´j/èÆÍà½ìÔ`eî¦\x000fRs¨êCW\x0007\µÜtÛz3ãìA\x001b	\x001do\x0006Z)yÉÅê¸®ZrºmÍì\x0006­YÞË¸´Þæ~ÔXÅ62ë¸ýw\x0010\x0007
c2¿\x001f¦cë®ùòÓéLµ\x001bLÛn\x0000\x0012!`¸HÙ`\x0013ËáL´j7¶Ý\x0000$ÈlÚãWÕó¾*ÊùÆÝ 2Ã´\ä­ªä«jçæíU¯*\x0007¬\x001a\x00032º\x0005Çrà2ëÀ5ïÃúÊv¾ÍvD§9æ§\x001da\x0004Nª zéè«B¾où».\x0012\x001cè(	|X	ç*8×\x0008\x0017$²Fe¹N'ÁYIå\x0000gÒ.4WÏ\x0011Bi.¯¦\x000f+\x0011\x0002ì¼=\x0011ª\x000f\x001b\x001a?,m\x0004öÃÑñóy¢ïjgy\x0013­«ýJ?6ÁÙuy©§í¹\x0002±\x000e:WÓ5.;Ò\x0004a:\x0003D\x0000?%YßôK:hü°¨ÇzNª>`gçáyÆÃúÓbã§MÇìü65àñ²óFáèf\x001dptíPt«GIËMè¬âû\x0000J9%!®ßJÛñbýmcã·z\x0003DQSZ$Þ·ôL½1LãÆH\x001bkÃ²°'·èÁ:·³â¬±5mÄ³ ë@ZùÒÑ\x0018G<7ëãÒ½}\x0007m;\x0003l /ñüh=?æíèfm\ÕÚ£\x001fÛòOÇ­ÄùTÁmßÑkOÍ³\x001e\x001a¯-Ú\x0002½ËáxÊ~Ã±W¹y\x001f7-¾Z)pHàé7MA\x0017å-nP½Y'¢j^Â¢õ&¤ÖÍB®\x001c»§\x0000¢Æs·\x0007I³\x0004ê+²mFärµä
=\x0015BçÄEÆ2h\x000c3¯È1F\x0019ouTß8ñ}«ù¾\x001d\x001bß¿Ô|ÿr\x001c|h7\x0015¡íXdüvõ¯ï\x001fî\x001e÷v ;Ãñ\x0003Ù\x0015>*¹ÿôé¿6^Xß.ÿyñýåÙÕ^©O»)´lÇÝ)Xt\x0013ÅÂ\x0001æûò~\x0018G'­\x0016*WR¹\x0006*¯x\x001f8c¸dÂû íßÑnVL´P*4P¹ NIãN¢Ãvú[:Ó±QCv]9kPMÊÝûAb¿÷vìßª\oáªnY[k\x0011\x0008M\x0007Æk\x001c\x001fæõ¶>g\x0003Wµ¸tËêJG\x0007\x0011}¡1=\x0019\x000bE\Àù­z\x0016¬juéåÀr¦\x00008Þ\x001fJÕ\x00008p3¶¢®êøK*lSè¬e©â,Yy¿ñV^¾Ò!lKÎ¬	¯T]Ëx£êÚ\x0014<ãø\x000ePR±÷Fð\ËPvS5Â\x000eª\x0011Ò®64U?þíö~µglV[ª\x0007!¸<[Ë£Ú1)\x0015)ÐFgj«¾zsz¾Ü×ñm7\x0010iäKÉ·¼µkk$hRQ\x0008\x0003R	ØL@[\x0002Úf\x0003\x001a\x0019\x000c£¢u2 (*ý¯MP\x0002B«\x0005I\x000e?°ØN}òýì/%\x001f¶ò\x0005)Kù\x0013%§Ñ|jç\x0018Ç&<Wâ¹fó9¬£¢å®\x0002OEåûê]½ºM¡\x0004\x000cÍ;DË$\x000f\x001a¥¤\x001c`d4Þcî\x0002,$%¬­ÚÃ'\x0012\x0008óQ'?Æ"÷a£¸«k·	°ò1ºÙÉ¤u\x0017Øî
f4`xÉÏêfù©ðÑé\x0017µ\x001eêOþøÇ×»¯ßV_>í)@I_{w(e\x0002+ýÚëÝ¹\x0004åýÙûëåÅ«}Å2ÌjJVÓÃjHÈÆñ]½¶õÆh¬®óúYmÉjûX]ä¢ù5#Û:\x0005ÇgªÝË³Õ¬®ÕxyÅMg#ÏÓ´ìhÖ:
ëG
%jèCUç	äÒX±¥ÌX¹âw;öVÖêb(o¯²i¿i\x0005QK¡\x0012þÜ¡Ö¬\x000cÔõ\x0019ª\x0003Ùmz\x0003\x0017×:_«§Ç¿?çC8QùÈB¢\x001b[ d,b:.lËA-®.o®~~ÈDv2Q\x001cº®\x0006¢t¸ã\x00110^§e[Ëh*/|\x000b\x0012O\x0008v\x0014
ÙH£ÖXP[jñÓb\x0014§#YVû ý\x0002\x0011\x0007\x0002à\x0014\x0016bN$]/¥µäH-_­xé1\x0006\x000bãuÁ\x000eÝ³©LÕbÒÓWS\x0000\x0016ú§)U2w¤Ïik Ôt¦j5ééË*¼yT®Ð2ã\x001d\x0001À¶\x0018ÖK@qsº\T£zïûo«»Ç=.æï)ùAF![,M¢î\x001bD\x001f.Ï¯gW{¼RÜìj¼=@äX(zM=¹½Ïgj«7c:-ìd ºþÊ\x0007\x001eêjã®P\x000bc:g¶¦\x001bLG\x0012	Z\x001c'ÀypWF²¢Î\x0008jó\x0012l:\x0012H8\x0015É\x0005¹gJHu\x000f\x00075F²[«Ó\ä&#Å(G}eìdY!YÉõ¸P"éH\x0003\Bòs\x000f·t´¥p>\x0019i}¨j}§:	¨Wk`²¬
9¤±>©Á\x0003÷pÙ\x000bÈ5Ü\x0014×äNdÛ4Ã¤U4z¦­¡ª-`EÁä\x0002n\x0002\x0018xÉR"	oÉ(&¨¶&p5ø¨M2Û@FËKÍxR`ÐV·¯ö ]\x001d\¨ì©(\x0014}Z¼ÿ¶ú<\x0004¾·{Ä\x0006é-+\x000báZ \x00174\x000f§#}¦]ç7\x0003¿\x001eâàÛý'wA5%ª9jT[¢Ú£F\x0012\x0015\x001a\x0015KT<jT_¢ú£F
%j8^T­ª\x0015ýÜAK\x0003\x001bLNC\x0015*Ö2pÞk>\x001c¸³îs:­V¾v­é\x0017¥F÷«Ûû§=Ô^Ïs@¨§9bE\x0015\x001cÔ7\x000f\x0013ï\x0017¯NÏ/o&`Ù\x0012Ë6`9ÍvTÿ"Ï\x0017 ì4÷q¦îT,,±°\x0005+Èä/PVF§\x001c~ÄÚ©}=\x0015ËX¾\x0001´¹C57\x0006ä;XéVÜ:ì´@Å\x0012*6@²¯@¡ÔÅ\x0002Èý:Ä­ù\x0001
Xº^ð-+\x001ev\x0018Kñ9Ì\x0003Jî<\x000c+îÇª\x0016¼nYñÔßÄký~p¬\\x0010¶F µpU+^O_ò\x0004Kä®â #=
2\x0011®êS¹ª%¯§¯ùÄ%*1k¼Ë\x0007Q¸Ô.Áò¸6CsNáýÍw¸ñ´t}ûøH?ìÁóÀ=øÔB*~4Ö4ûýz]ùvs}zuE?L`4\x0015£igL\x0011IeiI\x001au.©¾w\x0002é}Cl \x0012:(­\x000cÚÐa.f4'P\x0007ê|JWQºvJ§è\x0005(ÍØÉFO7|)\x0007Z?÷Ø@\x0019*ÊÐgË\x0011RdÄ¥Ø\x001e´yîQ{:£«vëØ9(úØÃ÷æ÷\x0004;Îy±áÙÚ\x0006Êjï¸½\x0003¬ø<l\x001d'5¥~Ìz3\x0003ÒâÆ0òô\x000bIê~¼ýòx·xýôeõåÛ#¼\x000fr¹Ò\x0013Rö,Î[;Ð¬Ú;þxzquRÏåÅõËh¦D3-h>­<¾ã'')bÔÒÇ;ô~Ì!³%m2ñ,HÒv#rå\x0017ë.¨v2(É ÌQé\x0000æ\x001bI]Èhlû\x001c2W¹&2\x0000ñÎéT3*³;1ÙV2Õ\x0006V×\x000f»@î±¦ZN\x0004ÚRj0Jó(Åõq[\x0010v"¡ßx0I¿(\x001eMïÿóßÿãÇo·÷ôÃ»ûû½÷ðÇô¦/É-Zt
/#îqkJ\x001b½í.~¼¼>=§?~8;?ß§áá7\x001eRÔtÒ]¸uLã^Ë-¨ îxìmG\x0012\x0015úª¥u\x000bHøÐUnmæ>Ò¿üµfýk\x001f,H¥(uýÆqþ1'ÙÊÆÍ&Z\x0015ÃFÍc:jQ|È·Ó6Z=Þ&Ì}Uéü+òÑSÒK\x0011\ðÌI\x0019nÁÅÈ´;í¥åÕiúy_Õ\x0014SBI	=2M\x0014S.KÉÄ@éYé\x0010©^¶;)]Ié:(SÃ\x0007>J&ò\x0011Á'O/j[\x0016¿\x00192¡\x0003ÄñùH¥ü\x0003$ò°/ô±Ês\x001a)Íæ\x0013¯Y?ñ¾¾ýò×ÛÇ}yD
ÑÈOÁs©ü /%fÓ³¿>½øáôjS7ï©fýú2\x0010
À[Ã]Ô	H6±Qnû\x001ef"\x0010@8\x0019Å5Ê©¹äD;±m2\x0011Ç8n2rÆèÇ\x0012\x0018-sÍX÷8é¿ñ®¤°,c\~ùüx»xûûí»á\x0005ñÙ#Ñ4R8[\x000e2Ç5Ë×W§÷§\x001fN/ÎN¯^Æ4%¦éÀ\x0004%ÃeµæÒV9\x0019Y»«|±\x0015Ó¶\x0003$\x0004øîC¹±°HE¹VÐqW9`+&ÐcM/S]TÔ"ëgÇ«y«vV-¶bb\x001dA¼
isKjÎïið\x0010kÓ®Ïg+?VIY/yvrË»îZ1}é;0c\x0011ÄÚXW\x0006å\x0007i\x0007\x0003P2ô\x0018SûA­Ï{4Ó\x0019ì®VÌXbÆvLjêW|Scâº¨\x0011G´sîU#æº eðîªÇ½+i^SSfÁyñ&å×\x0007à¬£PG\x0018
ÚÉ $mhõ\x000e³^³=\x0001\x000f°:u\x0015tO\x001c¢\x00169\x000e
¯\x0003lN\x0019+²ë\x0003!]ùwÝãàÑr	 !°Bq½môÎ\x0016¨FNS-OÓ³<#rIzr(0»N}ÝnTyÂ¬eEúôð,`âfdyErTcx7ðôf\x000b·\x0016\x0006\x0005HIí½oÇÔn×EmóbÝ¤ÕÐûß²fõqu§u\x0013.Ë÷Dzã\x0015ëJ\x0004Ø\x0018|Ñ\x001d\x0001¶p;.\x0002)ªeë,]ë¥§Æ¨x\x0008ÏUÕ+²ué7]7B<q[k\x0001\x000eA«¶hU7-wÖÐX«ñÉÓ	­\x000c@ÐõQ/ýB®[Ï\x001fî\x0012èÛ»O¿ì\x001b©éªÚsñ\x0006ð}\x000bÈÝ\x0015Ä­	Gç7gñíÙ«\x001f÷ÍÁ\x00146S²666»ÈôÒ«\x0012¨\x000cìl¶d³ml8\x0002	À\x0018¾¨b\x0017¨·JB\x001bá F8à31&_/¥/Nr&j²ß¼VhÃ\x0012\x000eÛàHý"\x001bÎ(çt\x001d\x001bÎl\x001515²¹Íµ±yÅWÎhIÐ\x0004ù*W6ÃÖõx#Z(ÑB\x001bZÔcM\x001a¥¬ê ø\x0005¤ì7o®&Â\x0019·±SÓ/§\x001f\x001eWØ\x0003F\x0015²i±É0
kX1LÇ]íI?\-¾\x0000\x0005%\x0014L
8*FK­x\x0003ÔØíV7OcZ©²Â¥Êeç\x000fßîRPøõöË·ÅûÕ]úÏ!<<O\x0017£´Ñ[o½ôáHÝ@G5¥ÉÎ/¯ÏRXx{zq½x¿<Kÿ9\x0004AM	jÚA;`2¨,ºàI|9úpÚÓöp¦!÷\x0005{ã¹\x00041xÃ\x000f[³º\x001bè\x0006\x0012\x0014z@Qêÿ(ÛÑH\x001eø®%9ªI¥\x001b\x0014KPì\x0001¥Ý9qI«Ì!ñN\x000f\x0000©qT`Ë;	¿ûØ\x0001ª4'	Ã
Í÷-NfáÅX	uµ²ªô7mÜ¦§h -é_&ÎÏÿùïÿqöåóÖÄ\x0014CNøZ¡tp å\x000ec»"àÃÙÅ+|½8»x½§EQøLÉgùhÀ8ó\x0019~\x001bL|^ªÉô¦X+\x001f|ÐÌ\x00179g\x0000­ýØ&¨yü\x00150I'	\x001b\x0015\x000b4.¿ïÕãÝÇÕýç»}\x0017Ñ@2#\x0014
µæIWuàÎ Êa7ÈÞ,¯Î¾_¿>{\x0019ÊPf:\x0014ðæ,Æ(/³t\x0001e­OtPXBál©\x0014 êÏGÅ³å-ãýo¿<|Ix½zú|»ç\x001d\x000eR`dx\x0007J{¼\x0002\x0014e	;/pÎßýxyAElË×§{^å\x00044 ¡\x0003\x0014Ó\x0006Õ¬Lh´¼)\x000c\x0003\x000bX®c§ðÁdPí6{'Ü`Qy$Z¼zxúúíöþþái_St&r<ÎoSÈuzÇö×7W7ï¯OÏSæú2¡)	M3!µ\x0017ò\x0004t\x001deH¥\x0001V¶Cè\x0002Ä\x0012\x0010ÛM\x0018EfÄ.x\x0016­·8Îü«Tï»\x0008}Iè	\x0019gg\x0016ÉL:\x0011\x0008auÑÕD\x000b\x0017×ÝFo\x001fîïöª\x0019Z2Z>hÎ`¼Ç(7Èªê-_w\x0019½½¼9?Û'5\x001bGf|,ÑèÇépÉ«[\x0018@¹t\x001e5éµ·KÇ
Ð\x0013à¬©÷múE¡|z÷ëíâÝ\x001fÿømá\x0012\x001d\x001b\x000e\x001c%*,»;:?ïaó\÷vùÏgoO\x0017ïNßMa
ÚØ´ák_@RdÅbëD\x0002ãæP\x001b+Ù\\x001b\x0002yÖG7Ë\x000flFîx=\x001dÊ\x0013Ø7u´H¿(;í`ñ!ex{%ÛÔIÌi\x0001RÌ\x0010A4.¥rv\x000b
©Ò_»=ETÂeJ.ÓÂ¥[\x0017È:¢9Jâë\x0016·U"Û\x0004fK0Û\x0000¦5J3H",Ã\x0015Ùvé¶«7q2\x0018`Ðb1#WÝHÉãÞ£(`\x0018v¶\x0001N\x0006Ã\x0012\x000cÌ\x0013
pjGkoÎÚQÛ\x0000æJ0×\x0002&íPTç%£YÐð\x0011;q¹Y_Ò\¾eÙ MT)îÆG\x0001þ)\x0014ìên\x000c\x0016J°Ðb0ïµÓj\x001aõ\x001d´Ý9·¥ÍÒ\x0004\x0016K°x4_r]ì1xWu<`µÛoòûÿµ`ß×Mÿ¿vSbùj=ônLÜ^\x0014H«\x000cùi\x0007äi'ìîk~/äûöu«.uÖJ«î§¿\x0013×çÇÕó9Æpä\x0013tr \é\x00122¾DJ9íæ%ÒëõÕrOÁdÆdÆ´Y\x001cå
i\x0018\x001fõ\x000cÊL\x0013ØÊ\x001aÈÔzÄÀ¦¾ûØb6Ç\x0012Aé¬l¸ 9-8\x0019a38µY­ª\x0012È\x00057\x000fÆ\x001bë0j!Ð1T>ë¶¬Ò$ÀÀo¼]»áâíVßîn\x001f\x0017ç·¿ßîòkhÙ\ÁfI«oØ	ÆJ}rJ'ËðO7Ë«ë³Ó«ÅùéÓ½ã}\x0007²Rëb £\x001bà¨~¥Ö,©Q\x0001¢¤Z\x0011m¥ôÛNg7èìQÐiw3c'$Ý*¤ÃÊ·»?þÏ¾Ç14NÔA\x0002É\x001df?¢µH\x000bF·uQHw
é°B\x0013ØlÉfØªõóE~ðQª¸åòhRºØ\x000eMlP²A\x001b[\x0002ÊÇÏh]\x001eF\x0010s\x0011m?¿õ<ÜF%\x0019¶\x0005Ïi\x001b\x0004Òc6\x0019i¯H\x0015u\x000e/Ñ|£Ñ EíhâP6ÛØc¶=òb\x001a\x001b"Ô\x0005é\x0017ãÐ\x000bôo\x001f\x001eï\x001eö\x0004z\x001bÇ®²hÍ8\x00056ôÅ01l;Ð¿½¼:»,âü&O¬xâÆ\x0013ÂÆ53	\x0016èñÛ}¸û}õ¸º{:'èÒ6_ØG	\x001aÒ¢Y¬ýUõáìÃòjy¶/\x0011
\x001b"=\x0004fÀý\x0017	\x001dd1vÐn\x000b\x0018`Ð\x00046yÅ¬f°à\x000ec1,Á°	\x000c¹ÅÜFcù¼ÀD½JÃ.\x00071\x001dÌ`®	L\x001a#\x0012P\x0014\x001fåÆq\x0016/Á|\x0013£ï7ÁØ`\ª¨_»mµÛ\x0016°PFñðÅhÇB0¶9ém½\x0016®XrÅ&.if³\x0011=jó\x00145özn@+XÑAnL5¥Ôm4ædNz\x00084Ò(Õµ@Ídµmó°¼'½3SPòD¡£Ýr÷-X{ÕmþUqÅ*x)·\x0010­\x000c³3\x0007NV¹1ÝæÇÔØîECãPÈ¤èÌà¬OY\x0004d«­Ú¼?È\x0012ô¨¹§·\x0005»§°\x0019¿Ñm~Q«¾Y=>Þíôhe(O\x000cëy­2¡Ú)R1ÜõÞôfyuu¶gÒ \x0012Í4¡YQ9vfíñ8O\x0016ðvÊî\x001cò8Ìd¶ÍhÈ\x0015É>N¦hEy\x0005péT¸[Bq*\x001ahÐf\x000e\x0003\x001aÀà7º¨å{â3SÑ°DÃ6«)î%Kh(ï®Q++hUØlGs%k³\x001apYÇ&ÓÆ#Ï³Hh8Ìd¾m\x0013Xì\x0016¼·Ã¨Æï¹û5x"®\x0016n[i£Ì\x000e\x000eE&|$Ñ(630k\x0013ês¶ï	\x0015\x0002\x001dµ\x0003Õ\x0012«Y;Ënë)ÏÃ\x0006U­l\x0018Øy\x0004¹ý)Ø`ç|ñélÝ ÑnÈ%\x001cµ¥*Ù¢~í=vMïÎ\x0016+¶Øº\x0013x#hà²:Ú\x0008²Üêkäf4W}R×öI-PxÊ\x0014¹\x0008?±csób¨«"k\x000bUÆPú¿¨¡v!ð(\x001còl³v«n£×u´ÄÄlk6"7A'»Ù¾Õ¦6°T\x0016Âúþáéþ6¥j\x0017éO÷
¢\x00040"V\x0007V&,Ð¤ó¯¹ºdøûËóÓ«½^¤?½Þ;rSøJeá«\x00062/ÏDfh"e¾\x0004å×\x0014§Ã,0[Ù&°\x0014¸U\x001c¬ã2k\x001f´µ:S½@µ£A\x0006MhÎÊ,¡ë)7É¨qtún\x0016\x001ahØ¦,6\x0002è<8ÇGQÑs&Ì[g®\x0004sm3\x0002¤D<p+'PWk|´ùÌ·¶.kÄ\x0002à:û\x0016ÍPg«Ñ>íh¡D\x000bMF£ò 6\x001a}ÑYYh¶êiG%Zl²3rg´(£uC¾hg«ÙÍhÅäK´´l\x0002%#¹ÉlÚó.X[m\x0016Y\x001d\x0006â@ú¢"Ã\x00048¿\x000cVs2JÒÇV\x0005\x0002Ý\x0014	,©¨\x001af\x000bu\x0004/W1\x000e`Þ\x0016µe\x001bv\x0007ôí ¶\x000fa\x0001ñèÔèwq^´Z÷0±çýØäGF\x001dN]\\x0016Í\x0018äuµ#ê7Ù~ô\x0006û\x0019µöÁAFÕG\x0017Æ:ó\x000bÃ&!´\x0012R=Ç/ëEcZéõ\x0017çñ/ê\x000fü©å\x0003SÏ?\x0007tÀçyÉQ\x0006\x0007}_Ø7!n¶-U³jß¬¾~{ø²xwKÍ{ºrÐ9Q÷Mk-ß\x0006
£ôS\x000c»@Þ,ß__^,ÞfóÞ¡¸ÙÇTM©LIýì,E\x0017¯\x0008¶¢£Eý\x0007À´%¦íÁt"Xª\x0003ð\x0013¼¶\x0012zm<\x0008%ÐA©Æ´J;/*ÝÊÍ~§ÞG+&ØIZâÜè#ýq°¦\x00195jÂNÁ¼VLWbº\x000eL\x001bG%:«dêÖ26ù§]:E­¾Äô\x001dé\x0010.ÆÔòÂª¢8I\x001bÌ.\x0005æo^:óüÝKEéû7Qrí(»htIn§´ßTT\x001bý¼é\x0017Õh _VOýëÃÓ#éºìyN1\x0010XôÙzíù*¤Ã´ðãÎrW?.o~øáòæ]öM\x0002Á¶^Â4\x001d(+"ú1¥Ý\»í	»í¶¤´í:Èe©õcF/\x0006ÒÄ\x001dvÖu·bB	\x001dÆL\x0019\x0010wF¹hDj4zéwv«Mº\x0007\x0013KLì°&úQcnzùT\x0014VH6é\x0010®Ät\x001dÖÔßqmJ'åá;"\x0008¦U;gè4b\x00123t`*àK%ë\x0011}(õ¯6ÂÖÚ\x000eÌõÙuðGªg\x000fI&7,Î({E©9wv¹lp~Z}NNúñyÎÊ!é\x000eD\x0012;Í\x0019xö[\x0008ÑÈ\x001eB;kqn¶óëu;ÿëUB»_,ïïï>îÓd\x0006mÂ	\x0017²\x001bGå,\x0003"È\x0005§rÛOåËÄu¾X}¿WYovöëug\x0003\x001fP³m.Év"\x0010¤ï\x0016\x0014ê-\x001b¶\x0002Ú\x0012Ð6\x0003r¶rIÇÏæo,\x0019¯ï ºø äV>\x001d¥|*¨±;=ÐD\x0006\x000c[ñ¦\x0015\x0010K@l6 °M\x0016\x0004^ã6Yp«Æ¥\x0015Ð®Ù@÷ë\x0003 w£\x0005\%÷°þ´\x0002ú\x0012Ðw,AÇÁ\x0014kùêûö.¾Pò=Ì½ó)ãånaÚÃ\x0002è¶uñ[\x0001c	\x0018¿°\x0013ÑM2Ç|ï¾0çdékþ\x001e©S²'Þ\x0006NËwñi%F\x001aÝ9EÇ8ý½[5Í+qÓ÷pzsð\x001eÆ\x0005iÆ\x000f®·Ë§r:»1J:ý¢Þ»ûÕ§ÛÅ»\x0014I¬òüºzüüü±khü\x001fª)¨Z/ÒÀq\x0014A½;_¾:]¼Káxª|»¼z=\x0001°¼ÏÍôFN-Î\x0011©xo °rG\x0002­Æxumz\x0003(ýâh@W)\x0002T|~±©EwÒ²>}Ú3×qµzJú	iT«Ãsdç)/ûùæÕ«=xGLSb£Å´%¦=ZL(1áh1±ÄÄ£Åt%¦;ZL_búcÃL¢¡áÔ®;¯o¢<}æêé~q¾úò·Ûß÷	¤s5+[Euó¥\x0000\x0006¾NMÿB%=È.sys¾8_^¼9ý°WGEo
Ó/äløvõøévõ¼Ö\x0011Ý¤dGN\x001a,F¯

ne»É{¿:]î\x00138Ò\x001b'A¢1SiPL MÌâ¤\x0007¤5\x0001ÅÍ»É@¶\x0004²ÓÍ\x0005\x000e\x0013K[PJ"ÛºËÌ\x0003%\x000fL6\x0017YkAzè\%@n[g"\x0010@Ø` ÖÔ éh\x0010\x000béÑB°yf\x000cäJ 7ÙBq\Bn
¤ÇäÄoå£|	ä'\x0003\x0001¿& È\x0015³ÉB|«¶z&\x0003\x0012(L\x0005J\x000eÓ	Pà·Q0Ñ\x0008ÏüødXòÄ©<NjT.ÑXK\x001e´\x001b¿Xï
Zß>\x000e.QM6¡Ù\x000c$þ4£C¾XØê\x0011J\x0004ÕÉÚk~(N\x001aE3¯\x0018ð\x001cÑ³7#Qy$`*9\x0005þW=:5ÜB»®P ¦\x0019ýÝ§ï¿ß¦îd\x001f)5øLooO{mFª°ã±ç\x0006F\x0019]
òië\x001fN/\x0012ã«\x001fW\x001c¼¦\x0007¸½Ó6×´\x001fkÚÇM»ªiWÇHëÌFf~1hi<Rj¸xw{÷iÆ¶8\äÂ\x0005éGëänÞ\x0017ÿtE)áâÝéùÙ«Râc\x0013Ç8æOÇ±%ýÓq Ä?\x001d\x0007K\x001cüÓqb\x0013ÿlBËä\x0000ù'ñ¤4²ÞZt.)*ª®\x001eè\x0016rñÓíêËÿÈ×TÏ»%jÒÙ-yÜ«íC!!À®J«Kº\ütº¼àËªç\x001dàB\x000b¸TèkX¼ÒRÝ\x001f"Ku@p;kXzp±ÄÅN\oYm\x0001¼\x001eGDíÙé\x0007¿³¥\x0007×¸®\x0013×*Z\x0001Ùº¢\x0019îU\x001a\x0004õ\x000fCëKZôÆ
%nèÝiFÙ¹ C÷b\Ø)ÙÝC\x001bKÚxìÆ]»UÂ-§X¶ú1Ö\x0001K«TúDÇÒôë\x0003­Ýu\x001dÿÀ«Ö¾Îm\x0014fÑkbÑµòÖwOû+5¬²"è
\x0014Å²fµHX­¶)Íq)e}wuóB\x0006\x0003\x001a,\x0001
¶\x0012Ò0
ÇeJJ©ÐV*n«B.ÂX\x0011Æ\x000eB
ª=Hÿ\x0001\x000fù6â®VÛ\x0016B««¬{lÈõé\x0010¯\x0010Ê(åèwuµ6\x0010j¬¾2ýØº\x0010\x001dK¤¤\x00033²Î|Ú\x0012ùIAl&¢W\x0015¢W­h$²$L\x0011Qä\x0013b\x0018ªïL?¶#r£ÕÛ6\x0013"\x0017\x0001\x001a³«\x000fw\x001a¢\x0007Ðª\x001d_L¿xú¶¯]"åËÜüG£Ë¤\x0008»¼8?~ys½¯_B\x0000M	h:\x0000õÿ\x0012àXy¢fâÎÉP2B\x0007£á¦¢Ñ\x0005±c8$¤+!]\x0007¤ã\x0018 \x0003O\x0001$C2¤U;'Ð¶~íê\x0015øâe=úTV@VhM¬U§\x0003\x001a¹º;';ODEØ\x001c\x0000£Pý\x000füãó\x001fÿx¼û´x{÷õÛãêùwÃá\x0012sÅ\x0018®' EÅçL;h\x0001Ô\x0017?\¾>½:{µx{öþúj¹g\x0018@\x00122´C\x001a2j\x0016©ØkT\x0003! ³· ÍÅ]6¬Å²(â\x0016Z\x000b$z8PÆA³)Í\x0001(«ÛäL*·ÉM°^\x001e\x0005,\x0004ËºNqÍ
[Ó\x0000¦³ú\ó»\x001eæM#ÍFþõ·ýé.(\x0012Ýa¡F­e¾ððïåÂ'xöhùþÅ¼	MEhÐW¾\x0010¥\x0008=\x0018 \x0019P¤\x001bU­ÂÓD¨âÆ\x0008ôª#fþóY43LËÊÜ%;²Ü5|¸E\x001c³Y×F\x0005ÝËô/CÙ\x0012ÊNJ¹¶å	\x0006t±Z«­L0PagÑþ4(,¡p:\x0014\x000731"tÂ\x0011¨­Á
P¾òÓ¡ Êeg´$®F43\x0012Ôv±ût¨XBÅ\x0006(Ç¦Ã\x0013\x0016v2>P°³a?Ë\x001d½¾p¢¾ók\x0005U
îîï÷M_£¡:?y*ôR\x0015kÈ,ëúìÎ2zô7ß^?ÿÌ8ÒÕ\x0003\x0002\x0006ÂqBÀTÈ@· \x0003¤\x000b|Á0´V1dx\x0001òY\x0013¦T¨ö\x0015TË8\x0016þôðõö·_\x0016×¿Ü}ÜO9\x001dYê\x000c"=ió4L\x0019\x0018JÕ½B®ñùéòýé»\x001f\x0017×?}¿/\x0012@[\x0002Ú#\x0002LÛiÃÛª°¶àò×\x000f4
úUúÇ¿­ö\x0013p\x0017p\x000fHÚ-\x0001¼6Éahý&ãòí÷W4\x0012úUúÇÿ\îùÐ~sì©ÏcO%j}¦Àõô¸gdg
N"Ó¢¸Ö&\x001f7ÓN
;BÖkZ7W{&vê<8À®Ëïúþ.z¡.¤ß÷k~§ü\x000eÙå9ÔrÕ2e.tvà«\x0003\x0012=ÉPûÑZð{Ü·°ùö
ÃÛ+?\x0013§-ûîf¾<³:}¾ñ:{c¼	r\x0011CÓN·\x001eÓ¾}wIcN'LÔözC2ÀëZ2à×/ûÜòÐôÁýÁ±ïÈø5á®ååÛË½Y;ØèÚJþtÜ\x0014£ûíÞ±\x0001¤no`Ò9&\x000cæSRÞ\x0018£ÙÞ´Ó´ÜÓ~ßÌÆçõtx|ü¼Ú·\x0011\
\x0019È]£tïâ\x0018L\x001aóB¨.)i¹¥CãÕëeÚ\x0004c´?l"\x0012ÉLE"\x0003Eîí \x001dL.µ\x0012Ù3ãÝHP"Ád$½î×ÑHuW\x0003\x0012°RÎµ[IÛ¸ÑÌfc­³úê?þ÷·½;"ËwÌ\x0011´ÎkX\x0010t¹æ×
qÉe\WuEÏÁù\x0012Î7Ây)âK'U3ÎÊ<IëpE[jú»µj¤\x000bêÄH\x001cu2æ^\x0007®{¡6ytº¢Ót\x0018D=Tinn£ñ@ïsW-;Ý¸îR\x001c¨¥>3\x001dEù>T¹xÕÂÓ­+\x000f\x001dHQ[w\x0012Åxc=Ú-8.Tt¡.\x001dãùÓ¦ã_`Ûx"UàîÃJ·¾p :cZ÷gQªd;;jD¹ yÛÂ@\x0005\x0007mp4WÕpQgr}Ó±¦Óïz¯\x0000g6\x0013_£63Êûÿü÷ÿ¨Ó¦ç1iP\x0004W\x000b8{gx\x0002\x0002ÒKÑîôò|QçN/#\x0012Ùô#ðN>Ù½s¹¬Srþ\x0007µ³\x000c \x000bÙÈv¯Bd½\x001d²=ÑÞ)iÔ\x000c%2Ì@¾U¤¼².¢\x0010«]Wy]ÀX\x0002c?pòPYü\x0004I6rÀµ(ËXï|\x0007éâõ%¯Á\x001bø¶4\x00198Ê]¤\x0003ê vÞ¶!ot7Ò/ÊCU&>}z|ømÏ øÀ"ùàCä¥(2\x0004Ñ]'*â<½¹º|wú2-ùl;"\x0001Ì§¥ã\x0016\x0001øÞ9í>7\x0013\x0010K@l\x0006L'e\x001e\x001bí³\x0004Û\x0000heÜvTÕ%C\x000f /\x0001}; aJ÷	§g@\x0011	\x000bÕÝs\x000f_,ùbû\x0017F	N³Ô|á(x3¿¯®7Hû\x000eq~s®ú\x001b¥)<1 Ú¹Õ\x0016Ñí{ÄyÚ% #rç\x000eÕ3 ®öîØ$ÿåÕ&Ñ\x001d»Dñd@g­hu¤L?2	\x0017Ï\x00034Õ24\x001dËÐåîA [\x001c>û§¼¯n¼Ó3·±©V¡éðÔã¼Lt ¯ë4'S.3ãÌ}bªolÚ¿q"\x0005@\x0013GOÜ\x001c\x0006.Îõ5¶úÈ¶ù#Çä`DJ6}oÏ_\x001eL2!ìhi\x0002¬£qóGZ±¬Ò uË±$¸Q«\x0015gîc[y\x001aÛìih¢ÉÑÎúÈú¢NFc¤9w\x001fÛj\x0011ÚÖE\x0008ÉSñ[0És+ôZ©±\x001aJÔ\x0001\x0008Õ'ÖO\x000cÔ,Í2üF\x00174\x001e\x001fÁÀ\x0000Î\P}chýÆÔÍÉÅÌ6F\x0018ÅÇF%r£çúB¨>24d\x0012kÌÂ4gÖ°\x0008¢12\x0018\x000eg.B¨R.hÍ¹ÀÐo¶ \x001a«9¢O \î\x0000ÄÊ\x0011b«#ÌÒ¡2(\x001dD\x0002/}í±\x0003ç\x0012VÛ\x0004·¡´Pf~Ë+7
º\x0011­"3\x0017!Ö\x0007æmbè¶;ëDx\x0012\x001cpPÎÍiïÌä«\x0016!6/B«Q,è\x001cò"é_\x0017>­g\x0006\x0013W­B×¼
iàg½Èä
#ãÀ)%1·^BÌ\x001dÓããAúÅ0¢è!ôáË·Û/\x000fC\x0019Ã³&$?ÃÒýºD\x001eLbé,\x001f>uõL/Bô
zyq}zq9\x00142¼H\x0015!¶\x0012F	ï\x0017P\x001cîo9çª6r\x001báæ££XÉZGù%!e¯øÁ6yía.H¾¥×cÄV×ùZG9\x000b)¿\x0008hJ@Ó
¢7\x0008»Ëãå	$ì¾Y©Ò\x000chK@Û\x000c\x0018d^\x000f|×V\x0012\x0006\x001bâ¦JF3 Ð
HÊ,à\x000e¢<ýÀKébÊ\x0013góaÉ­|àIv4`\x0006Ôãà#»-FÜ\x000cèJ@×
X\x000b¸\x0003Ï\x0016(\x0005Ü7ë\x0017\x0001}	è[\x0001+évÏ_¸nß,ÐÌg­©
HÂ¬ÉËûû?þ+õÞ<fÓ·oûÊõ"Í¥ÉÏm.¡"÷çhË\x000f\x001b®R\&¿ëõÞ\fÓõõéû\x0011C\x0018:\x0010½Ä92\x0016	äd^Wµ}±díÞ²*-:
xÒÍ&oªÞÙë\x0007}b¤\x0007ý#4äúVsÔ\x001d4ÜÌ<@Jç¢õRi«ë{ë.HSAã´¤­ m%ª§óÖv|5GÝ²µc\x0015 û ¡vH§O|¶$ÆdÔÜÙFã¶\x0019ÒÏgÄ\x0011Û\x0019)Í>\x0012S*\x000f}\x001eP\x001e]=Ö¢\x000f²òãºÃ§\x000c"\x0017ì$CJ:\x0018n§EZ³\x0019+G®;<9ÉM³\x001d£è\x0014¤DÑ\x001dCÍX9rÝìÉ©yÓÚ¡'\x0002\x0018R®\x0012ÓÖ®æLwAÊ\x000eO\x001e\x0007ýlIËÊ$Ú@ÅõÛO\x0017dåÉM³'·Ê\x0014\±ò"¿¬¤Ó
Î^¦rã¦Ã§õ(É\x000fuØ²\x0004	5\x0006g'?¦r¦ÃAáíQ\x0018yÆ']\x0018\x000bäü/]ù\x001eÓì{l:¨Ä1ùQ¼\x001a½¨çoÊ÷fßc©NP:xÒ¾\x000eü­#?Ò¾îwâ`7z+Ò/äÄÏ\x000bç«\x0017\x001aÅ¬s[ÃÝ"?¥\x0019g¤Í»Í\x0013?7./¹QìE@[\x0002ÚF@:ÃD¾\x0005Í/öÞÈµëúÚ©\x000b\x0010K@l\x0005LfËÉ	ÐÐèÍÁãDi¬ÐaK\x0017³\x0019Ð®\x00150FéV`e3§\x001cG\x0007ÂVÀuF6¬Ah$Dê)ã¡SFËPAÅõ6­9Ó\x0001óÅ]\x0001j\x0000¤»óÕÓýêo_öµFÑ\x0010¬<'\x001du4²?¬2¢ä\x001bÃæ¥âùòæ|ùæâtO¹\x0012ºM-_7ÜñìåýÝïÉdt±ø,·ÇÃ õRõK%K\q£
ßkCL6Ý¾½<?£î\x0014º]|OöÛãe\x0004Õ¨¶\x000bÕ¤%Ð
ÇõÓ¢\x001e\x0016í®w\x000eR(I¡ÔÓ\x0014¬4*º²ÍW<v4ê®ç\x000eT,Q±\x0007\x0015Ìî\x0002OÂÎ|Ûãäu-*ØñnÐêKTßOÞJàÒa!\x0007Ã0¼ÑríÐ®·Ô\x000eÔP¢>«\x001a)ð\x0011Øeô÷I% Àa\x0016@,Qc\x0017ª	Ôp8XÕ{\x0016Æð)Wj¢\x001d2í HËz}K\x001b®HmêDñ&Ò
ê!Puª»Pu\x0014é\x001bçàGÜ{Ë¨Á¸*]ùÝ\x0015\x0000 h\x0018<\x000cïã]v,¹¬T\x000eûY«\x0000 »"\x0000hC½YÓ
p2\[ª¢ÙU«ÐÁZ\x0000Ý\x0015\x0003Òn\x00128§\x000fvµ¢\x0011\x0017ýaVk\x0015\x0002tg\x000cpR¤â´'\x0013%§5ð>\x001ef	¸ÕõÕFOçsy°RËr½ VáJwÅ+\x001byD\x0001¸âçº\x0014
ÄªAéÃ¸Ö*\é¾xÚCrÙ°Æ¹tÆ6R7| \x0015PÅ+Ý\x0015°hÄydõE\x0003"+\x0016å8\x0005Ü]u\x0004í¬¦
Y¦/d!PÿmV^D©ML\x0002·a­béYé"µ÷N9QçFÔ\x0017½w;
­:XëCK_ÐJ© c\x0019yäñÒcïup\x0007Z\x0003UÐ2]AË¦\x0000\x001b4\x0017\x001b§åÀfú:¿³øª\x0003µ
\x0004¦+\x0010X\x000füB\x0004è-tõQËa®Ç\x000eÂZ\x0005\x0002Ó\x0017\x0008t
iG«bI
üaÎ\x0002¦\x0003¦/\x000eø±Ì\x00178×t.R\x000eoýa\x0016k\x0015\x0008L_ Ð_¶R µ¤ZÁ\x0019l,*â?\x0004k\x0015\x0008L_ pZ®\x0008rÈòa4«Ñ\x0007Y¬¶\x0003¶/\x000e(ÇO\x001f)qEn¼ò\x0011Çåj\x000esv±U\x001c°}q\x0000Óru\Ø/£üz©WjG­c\x0007k\x0015\x0007lW\x001c°1r+#8pü~\x0018AÊ¿ÃÎÒÛ\x000eÔúòª/\x000c\x0000²^âP»Ç÷ÐÁËÛÙÕÁZ]l×ÙR,¾¿¢\x0006\x001eï%Å\x001a3×Ã¬Ö*dÙ¾eår\x001aÒJê\x0005¢Í\x0014\x001b\x000eâ\m\x0015²lWÈ2t\x0015\x0010Ù¹ºÜNá½cÌ:ÈáÕV!Ëv,C'BV\x0017ö[g\x0012iàD 9®Ã,Ö*dÙ®U¨c0ò\x0017õè¯¨ûñ\x0010¬UÈ²]!Ëø1\x0017´èÄ·úQ9\x001eÑ\x001e\x0015ª\x0005]1Ò\x0016ãÆdPGI[ì\x000c\x001e\x0004µ
YÐ\x0015²H`+k\x0000i3ÈrõRÕ`\x000er
UÈ¾\x0000·ÍÑ@<¾n\x0015ýÔ\x000cÂAü\x0015T!\x000bºBA/Jíns\x0018ðNIÿ9Ìb­\x001f\ú"\x0016\x0006)<Gêv\pìè4q\x0002P,è
YÔÃ%Þ$\x0018Á¬\x001eF' wuáw°V\x0000ú\x0002\x0001QT"á_¾qõÚsÖ\x0002Þ\x001ffgU\x0000º\x0002É#\x00015`Ãáy³ÑÈ\x001aÐ»ó;X«@\x0000}ºòz5\x0018¸]'9,	°tú:\x0004+V\x0000û\x0002\x0001\x000cýN]µbåÇ¹ê±Ó÷0é VÞ\x0015û¼«u\õ\x0008i?ñÈJOº\x000e¬W¬|\x0016öù,íÄ\x000f\x0000%Ü\x0019U\x0003\x001e\x000f\x0012\x0007°~"îrX$õÎ F\x0005aôCác^¬æ0á\x0015«\x001c\x001b»rl«\x0014	Ð#¬f«jauÎ\x001dÆ®sÅ.çªééÍjY\x000f.U¦PÿÊAP+ß}I¶Q¬)	éøJ3pòb$Û\x001dè\x000eËUþÊuù+\x0013AN¯§¤ä% d	Øxåê*åºü¡ÁèÌ
Fâ@P8ÚuàM\x0007kå¯\¿Ré¨Q©H]«aùBpú0\x000fÅ®ò\x0002®Ó\x000b@n\x0019O\x0008øí5¡J\x000f;Q«åú6\x001aoÛKB\x001e§EÌ\x0005ãa
0|µ±|÷Æây>)¶"çØjÌ[Ãaö¯öïÛW)\x0017Ìssî\x0007xÈ\x0014]·0ÄaÞ}µ¯|×¾2Y=8\x001f³@
º=J	-Íj>\x0008kµ±|ß\x0015\x0016Ý²òP#ÏL÷^\x001aQû\x001d
g\x001d¨ÕÎò}ÇäO
_
ÐI>\x000e;,µ«g¿5T;+ôí,\x0012¶à\x000c+3Ñ¼åÆÄz\x0014;T[+ôm-T%Q&Ìy-÷B\x0010\x000e³\CµµBßÖRN³\x000c=\x0019gïê¢¬×tP<Ë
ÕÖ
][KÃ¶\x0018*ûç,[\\x0011­Y¬éo®Á\x001d¦·NÕa\x000côØÂ¥ÌéøÊÚ|Qqû 1»*^T^\x0014ªXRÅ#¡*Æ0ÛP-¾\x0005*X>4£¡i?"]ÏDtP¥+¬-ñÿ=X\x001ar\x000e&\x000c­%ÇúÈ\x00144ïæXËVX¶\x0001Ë\x0006ÃgüØE6ªp¹RXS¹°âÂ\x0006.\x0018Çï 7 !å\x0011£½v\x001dÑ&sU;QOß [ôÑ(\x001cÇi\x000em4Ìn\ÎT,_aù\x0006s!ò
\x001c\x001açY$'ø(X\x0018vI5MÅ
\x0015Vh°V:d\x0005nÁp\x001c\S®*\x001fÑD=ç#VKO÷\B
\x001bK\x001bÑ[h¼|D·ÃßOÅ2ç2
Æ#²Ð5u¬x6\x0017ÍãÎæÚYbù2óu\x001f\x0008ÍW(\x0006lM\x001b\x000fì8§Ç(óØÁGÉ+ß%3ÆY¢Ïy½1ú+ý¢\x001eÚpõÇ?¾Þ>þþp÷ø,qÁÉ\x0014Ì`Æò¹qñâ\x000f!ìO1ûôêÃåÙÕ\x001eÂMm\x001eµy^Ý}ûã\x001f÷«»/ß\x0016Ë§¿=}ýv·gÊPZR'Ü\x0008g
¿=0\x000cSqXÞ«³ëR,Ï.®\x0017Ë77ï¯Ï.^\x00064% 9B@[\x0002Ú#\x0004\x0012\x0010\x0010\x0010K@<B@W\x0002º#\x0004ô% ?BÀP\x0002#\x0004%`<>Àõ±apÔê\x0008	ëPr±DW±D\x001fa0ÑU0ÑG\x0018Mt\x0015Mô\x0011\x0013]\x0013}ñDWñD\x001fa@ÑU@ÑG\x0018Qt\x0015Qô\x0011\x0014]\x0014}1ÅT1Å\x001caL1UL1G\x0018SL}>9Âbªb0¦*¦#)¦)æ\x0008c©b9Âbªb0¦*¦#)¦)æ\x0008c­b=Âb«b0¦Ø*¦Ø#)¶¾ô:Âb«b0¦Ø*¦Ø#)¶)ö\x0008c­b=Âb«b0¦Ø*¦Ø#)PÅ\x00148Â\x0002UL#)PÅ\x00148Â\x0002ULc)ÁÙú¬~1õdüè§¿/>Ü~ùü¸z\x001e\x0010Çç*'\x001bh¾\x000fW$\x0018\x0019\x0003,Ì\x001c}sóóâÃéÅë«åó\x001fU¿(­äÿî_¾O¿ønøù»óU²àÇû»ÛÇÛÅé×=U/Ê3\\x001d©Z²h$\x0004Qª­{ÎÉ|ß^.Nß?ÿJØ°zJlHÏP%Øû§ÏÏ\x0019ë5U²»a\x0004»L\x0011OÿÅC]\x000f5+ÁÞß¼~\x001eLëz@ë÷4*mÝsz:¾ýûãÃÓ×ô§Ë§Û}V3:RjÝÍDïyÙAm5z>>ýùêòæ}úÓåÍ^Ë	 )\x0001M+ 
'ZFI¡È/¤u\x0007\x0002XØv\x0001Ú\x0012Ð6\x0002RE@~å\x001e¦K³Zs2ÚQcÕnÝ\x0005\x0008% ´\x0002R\x000b0Òx=¶ JÅFmA,\x0001±\x0015DöX07\x0019K=\x001dH¶x|\x0017 +\x0001]3 íÓ\x000c\x0018´	päð2 	³?±/\x0001}3 ã\x0019²Ã(ÔÈx\x0014ÖÒzö&\x000e%_è0 Ê8¤0ç¹è\x0014DýSÓq&`,\x0001có&Ö$l\x0001µª¸´\x0006\x0005PÏä\x001b\x001f@³VÍnçÇ¦\x000f\x001ce.	ý÷øçn\x0011]Çö@¢¨«$ï\x0011ÚrJ({$~Â¸\x0019é"Eº\x001f\x001eW¸ß\x001b}S|@àH\è\x0002kI\x0016Ø`ªvÝ\x001f®?_¿\x0010x­Û\x0008\x001bélÂÆO\x000f¿ß­>íÍR@ad\x0019T§<rùur*¬\x001cíT%ùÓå³å«½ùÉ¿&³TÆùgú#}½oûÕâ\x0006¨Qòü§Îð0D\x0013!ÊTX§Y+À\x001a_\x0007K\x0012d^\Óô4ÊR^F3%iB£ªNÇhF¤81²
ÕN4»iµ!yzuÿðuq» îKóòÎróoÊG}wUås¯Î/ß/Ò\x000fôÏyLÉcþ|\x001e[òØ?\x0007J\x001eøóy°äÁ?Ç<îÏçñ%ÿóyBÉ\x0013þ|XòÄ?\x00076×3Ðz~¢ÿo·\x001fOîO~=!§-gÞ=\x0007ñ\x0014×¢Yò2\x001e\x0008\x001d\x001fw«t\x0008ß¤\x0014àÝéâÇÅùâí¢8û¾ªcJõ	í¬&¦d»\x0019R²"Ó´T({¨ÂK7ëX©0°R¥Âñ².Yé.°g
M8\x0008ç¦H´,¡AWyN?¬©`ÍqÃÚ
Ö\x001e7,T°pÜ°ÛN¿õß\x0005ë*XwÜ°¾õ°J&¾x"\x0006dÌ"MR=\x0004l¨`Ãq[¶_Ð\x0015¿þÛ`±
`Ø\x0015Àþû`«\x0008Ç\x001dÁ°`xÜ\x0011\x000c«\x0008Ç\x001dÁ°`xÜ\x0011\x000cëÄû¸#\x0018V\x0011\x000c;a\x0015Á°7ý7ÁV\x0011\x000c;a\x0015Áð¸#«";î\x0008æª\x0008æ;¹*¹ã`®`î¸#«";î\x0008æª\x0008æ;¹*¹ã`®`î\x0018#ûÿõù_øMEfæ~¾]Üÿç¿ÿÇòñóÃÝWÓ\_í¾{ÿð÷/_
0¸<p
\x0005£³8]\x0000K<\x0002Í"´÷?_^¼g\x0015Äµ¼z}yöþô»»/\x001e¾|yº\x001dÿ°M|i#
q¸Ã$"k²¨W ³NBòúÔ\x000c¤äyl\x001bµ'é,3 é@¥Nl\x001eDV¢¿s\x000eRò/ÐD:ó­\x0004¹ì`\x0018\x001aÄJvû\x000c¤äE°q)
³Þ3Í3%h)eÙ°\x0001i\x001eQZ®\x0008<)Åg¢ KIîÃhÐ	²ÄÐd\x001c	®\x0013\x0011ªñ³Y%û-ÄyF¢ê\x0006ú&$3\x001côøÝ\x000cÊê·¨YZ7º\x0000ãOh44\x0011\x0001\x0017d´|·@}¥ÍLÿúWå\x001fËb`)Â$Éë§Ç/·_\x001fî¿>ËE\x0003Ôbþziåägì9\x001f\x00069gÆ*L}¹¾¼¹º8}yþ~
\úKèZáhn¼ÏpÎæb8¢SBç\x0007½£¹tt\x0001\x001d¦K\x000c4'o08Ö\x0016Û
ZséHJÔwÐÑÜ\x0016¶]
?¼à\x000c*é\x0002\x0015ð\x001e.ý%ÞtØÎXÍ¶\x001b¥2\x001déÐ\x001f\x0002.-9ß±ì¬\x001e$c\x0007Óé¬Dúã²Ø\x0013$d\x0019:¾«ÁaÆÍ°'R.ÁßÕqOøØM÷ðôûþ-Ñ.äéw÷«»/{\\x001bßH@Ö\`Ï¦Üð\x001c<+Â3PJþÞ/Ï.wi¿}ú·»ªH!\x0016ï\x001fî\x001e\x0003pZ
ÙB"0.dx\x0010\x0008ÈÉUð4\x0015¸4ÈâýåÙåw«ÇO·¿åÿäÿÃÔè_Tñä_Pî¹¼¿¿½]ßýúðôu¨¹ßm\x0007g\x0015»R\x0013Õè\x000fÀ±!bÎ\x001c\x0005dy~~<üÙÛË÷g\x0017ÏZc2%irC!\x001dAi AÔ\x0003\x0014OJNPZa?-¡ìt¨td\x00081CÑäÖ8@¡R\x0002àuBA	\x0005Ó¡\ä\o(\x000es\x000c¥\x001do,'\x001evBa	¡<Õ«óçCVÛ\x001fX9Æ(03,åJ(7\x001d*Çæý\x0016£Ï#vm(
fÆò%\x000e¥\x0015ý#¿¨\x001bÂ¼ûÒ¯9Þi£¡\x001f*PaúJÃÒ\©<D?ù|1¸~¨XBÅéP\x001eO\x0002=n¼¡I\x000eåëþ²ëÅwªÝ7(Hg*aÑîC>i©*¬µRÕ\x001e½Á¥'\x0010rv¶°I¶Q¾_¿G×G×-.ÝP\x0019Ô\x0000EïßâÒ5Ç\x0019­UÿJ×K×
>Ý\x001aöTiÿ\x0001
6ËTFö\x000e¶ªòéºÅ©;S©|¾§\x001a\x0013¯ f,«Ê©ëé^ÝÅaÐ\x0003A%
ÅP(7TÚà\x001dX9uÝàÕíP¬CÊÒÅÃ¤ê1Ôô?]9uÝàÕ­]\x0007e\x001aæ2X*ú1&Ï4ºrêzºW÷z\x00182Ó\x0017ç4\x000c¿\x0016K\x0019®¼ºnpëÜ96Pé\x0013\x00178ÖàTAÿª2_7-~=©lTÁéõ3U^Ý4xu\x0008Î-A\x0019C§©ÁU(ºîJ?MÙ91Þ\?-Þ­\x001eWï=×¹´q\x0007=ó\x0004\x0015¼T!¦Ãh>ÆDê\x001eª/n\x0016ïWË×gÏç\x0004ªðT\x0004©Òé@z\x0000Åß\x000f\x0015ß6½o^\7@ù
ÊO7U\x000cÙ}\x000eLùÀ
\x000b¨Í+ÐéPÅBOPF5@E>'ªÀH'Hw\x0007ÝH±BÓ\x001aÒ1\x0010ØP6·¡¡fP¡)©ÐL§J\x001eÁ1\x0015\x0003Ê°÷¤ËÙþÏPQÁt*RVçî4ç8(Vd*´¯FÓ©bµ¨bÃ¢2ãJ§>=ö	<\x0017|î6VµOP\x0002\x000e	ú\x001a/ï¢áã{Â27þÓ±le+úq:ã'­äAé©¢@u¯u£k§ \x001b;¡@óQøå\x000fôÚ1`?\x0016ÖX
_Ð\x000fcQó\x0017ôygÂA°\¿g0õj7Ó;\x0006à\x0011æÖÁ\x0000g',SÞ µaY_Y~~ª\x0018<|Á£Ð\x000c¡Û7©°9Ê­åùÑÃz\x0013°ü8éÆm¸õð6\x001d\x000bj,hÀ
(·CæZÊ3nð\x001cT·Ó"ù\x0012+4,y=\x000c\x0018r> ÚaÅË­yò;Ý\x000bÞÕÔµxÒüôo=\x0002=:\x000cTÀð]L¿­­±lÃ'L\x000eÞÉQ\x0010é\x0006køÑÛñ(Øo-¬Ü\x0003ý8ÙZÊ\x000f£G\x0007kE¹ËNBN8Aw/x¯*,úqº{X_\x001c{\x001eÝIî!È%\x0011ög\x000ehþòqø?]fZô©	Dr\x000c&É\x0016jN¶\\x001c­\x001e6³yÒ1rÒYÞ¼}ü¶xµúõéyÑ\x0001Úå»Z\x001b´8T\x000c á&nlyþýéÕõâÕòíÍ\x00040S\x00160£\x0006q\x0013\x0002ó<5\x0016\x0012\x0014q\x000e-Ál\x0003óæd1Èh
·æK[\x001f?\x0007\x000cJ0h±\x001a®µ\x0007°èóÐÒáÞF*-`³h§
\x000cK0l²?\x000b³Ád0¾£±1ú9\®är-\iÁ£g¡ÜÒp\x001d11sÀ|	æ[À\Ê"<é­¼\x000b°Ó·^Íú¡\x0004\x000bM`zÐl\x001aÖ~d\x0015u\x001c×¾³sÀb	\x0016ÀãÑ0¹\x0015Ø[\x0018öû\x00167£d\x0013®Ýk¥Wð\x001c¿­!-\x001f^c:Èâ·\x0008sÈ*7¦Ûü\x001d\x0004K,¡ð{C«Ü,°Êé\x0016?FOÒ9PRktn3'I¦EsÈ*?¦\x001c\x0019¢<÷\x0018zXa2ª¼\x0019ÈLô³YåÉt+\x0003$õªü1ãx\x001aïQ­åÊtå1tËH\x001eßò×¤/~"^¾æ¬Õ_§dÃ\x000elòö¼=é²=e\x0017\x0000ê\x001e@­BeÐüø÷îáîË×ÛoßîVÏfß:Ñ\x0019äIúã`³¨S±õTöîòìâýéõõÙòe*,©°
5\x001f\x0010#Ê!\x0006'`y_/ØúÂi0j K4×u';)N\x0017Ó5\x000cfüÖCl\x0003\x0018V`x<`®\x0002s-`4-Þó"CËU\x001a|\x001fÈ0Î!óÕ"óM«L\x0001×&ïNJ\x0019Ìä1ñ\x0004f·¯§ézõ\x000f­ÉRÈ×øèH45£\x0001Èò\x0007Øz­j ÓÕÇÔºåk\x0012w¼3õ,__ÐÎÄ­ú\x0016´ÚhºÉh)iÌ6Cj¾ÈÎ\x000c¼\x0019Éæ|Îäª­\x0019f¡\x0010Ð§Úýjòÿn¡\x0000Ï!à@\x0011ÀþeU£­Èj\x001fk´-VÓ|1XÍÕFo;\x000bÍ©2Ý`K¿Î¶\x0011Óé\x0013È¦¹Äüßª¡Â'JÆëcJÚ\x0006tJyxú6´E'g¡tPtÄ¤\x001c(RßA6¦û¨!\x0007Õ\x0007½º¼¹Î\x001d\x0011éÇ\qILËKâIPtXÊu©ts&\x0006i\x000f¦JÞ¬êÓjò¶ò¶\x0001JîÓÜ?¿-[¾#NPàúÒZª§B¥x®¶¿f(E\x001ecú\ì¤ÒXS
zÖ\x0013©¢#§E+]þy^TÖçë;ªÖ«l¨Ü\x0006Leå\x001b\x001fTÉlm\x0015¬cªúi¹ÊoPù\x0006[E®7I¶Ò'Ö²­</«¨cè¤2\x001bëÊL_Wé É½²Ô\x0013à¸­5ûy¥t§[Ð¶ÞÃÏSm\n"sË\x001fÐ(ÍP4Ïº\x000f
u
z2\x0014èÈ]\x000fiýDZa_·S\x001c£lïbG³AeÚ>àà×\x0011æ­ô\x0001#\x0007Cc¡Ê\x0015O4Då7i¶¢#d^ì@
\x0011¹d6Q9Óë®Ý ²
Tov\x00100ð\x0007²ÖM°ÑFl\x0003\x0014Noè0-Fj!\x001b²\x0019\x0016×iÛÌ Â
ªÅ.ï\x001fHgÛüþ\x0016»æÔ®yz©6<»îÙÁ9¾fJ¶
²¬ÙÚê:³*n|Á8ý\x000bÒ\x0003|vWi\x000f\x0016~ÎGóëm¢Ân*¯j[y5ÝVÞ¯©\x0006ÀJT)ãê¥2µ­¼iXíV\x0015HÏ\x000cl+\x001a\x0011©|wvå7¨îDÉ])¶\x0015¹vöV P¡7\x0006zØ`éLÁx^ët/ h\x0003öæ\x000baÃR¡ÅRÈ5_ÉP0ºP`(ØûùÂFº\x0010¦§\x000bh\x0014\x0017Í¢óq\ê^ÑuQG\x0013Ô¯
Ó}\x0015æJg¢¦²Èß\x000fØ½ù¯7\x001fý<\x0015)X>Ù\x000ceâ¼ù|rël(\x0017{£2µ®VTa:\x0015\x001aÉ`\:O°ûôZLE5ÙÝT\x001bozbVÄ1\x0012J\x0018zäC\x001eZZ:©â\x0006Ul âúTô)ïS¡¢@\x0019Õë©Ò©o}[4\x0003W\x000f7\x000fò¨R<\x001eOù\x001c\x0018bo
2Õë\x001co÷i	²N(Ùf:%59e°1ð\x0015CôÝéUræ[läà§³AÚì¸g§zh¾É\x001a£¡ó=?n}Ï¯\x001bì	ß6¤/ëø¬Ì¥ëárfCþ\x0005Ý_½[}ýºúÛP]uuûëo«ÇoÏb)G7Cßyò\x0014Y%-8©\x000b
ª¬®¢Füå¡Âêêôí»åÕõËl¦d3GÅf b&8­Tò%\x0017çP[qBW^Ôì ËÝû[h&»øÂË&'0È\x000f¼úåö×»/´Î~zøòé?þÏãóz\x0006Ö"-1\x00124ü¦ÉvK\x0007ÙìÕ§oÏ.h­ýty~¸*d
j¨P\x001c\x0013\x0013\x0014ýø§BÅ¡¼°ÝzP\x0019Y3Ý¯\x0016ç«§Û§û`N±ÞJR0d\yÎXS/Óÿ»ùÏ+@0v\x0015\x001dýØ§»øüÊnÆbr=çØ gáÅ\x001a/6â©Hë>\x0017¤?²jÜ[´³Wö,DîYh óTÌÅ`6J9k®l\x0015B;ðÐUx¼´àyfKÞ-Ó9îõ\x0000z\x001eÖq\x0013\x001dG«¡^\x000bà\x0013ÙòLÙNgMõiéÇ&:\x0008TD4(Q¥OËµ1)/±¢D¥æá\x0007§g±
ÏTºRòiQË-ÃV\x000f¯á|\x0013\x000b(õÁ7ÎmËõút7\x000b¯vÈ¶Ñ#0\x0007²\x0014SR)é\x000c²gqS±ÞÔx¦q_\x0004ºÑ\x001f¬g<Ý»\x000cx^6\x0006bi½zåùÆg\x001dØd=sÂ.OKÓ\x0003ªò¿.Ôt¡.Ò\x0005£cI;ÃÆãG\x0008ú¶zÞ·­Ãm\x000cgÞ¸qÛRI?ã)\x0014ëé²è®\x001d\x000fTG?6áiÂ Q®Dº~¬
¢zè°¦kû¶\x000e5×]XºRæN.TQÜr³¼\x001eÔn\x0005\x001aÝ
UCÎ¤ø\x001a"WíZ^zèfâ\x001a/4âa^zt³<SÆ\x0000ú0ïãÖ\x001b\x0017\x001a7®(r´Hz \x001fWvFu\x001dØõÇÅÖRwvÊ.1RY­áåö\¬¬G?¶à!U³¡1$¡Ix)uçÜ"ÎÁó5oÄ\x0003já`<ï¥Ï\x001aj\x0016]¨rhtÊ`\x0002KºØ°fM?p\x001cÐï<76¸½úÆ)»>úUË
~Ôk&Å\x0002Ñ8n\x0005ÔóR>£6!)enô)óóÌ\x0018DÛÏ\x0005%©±Ý\x001fz¨*/@Ìwf,($UÈóÛO¿Üî«4"ñ7,ÇüYç38ë·ÊÏH
òü4Qî«vÏ\PqA\x0013WÊñ¹ÍX&@GÖGMdz«:´ÌUd®»r2ÐI2\x00074í5ë*8\x001d¶
\x001d[È|EæÈPÄ1Ú»ó^Ð.ÍÚ*öm!\x0015Yl!\x0003Ã~\x0006©EQ5V\x0005ç¶eã&\x0005Ø¸MÑZ\x0017nîëâÇÕÓ·ô\x001f\x001eoÿþùnÉïwM;\x001aps­4P!ÃP~Ââ"C±ô®hö~ñãòæ:ýã«Ó_2ýËÄÅ\x0005\x000b\x0011«nä\x0014¹ïÂç\x0008\x0016å2\x0010\x00047\x0015ù¹[QØØÉ!OµëãEÒ$É\x0004>mëÀ¯!p-
ú§¸\x001e\x0013cÝÈéÜ+5-t±¥´CÈëgðB\x000e\x0015rèG¶R`Iù!kl"zäê.°+kì@Ö¶BÖ¶Y9v«ùvë\x0016,òÊpÃ00ûÙw3\x000fmÞlg£Ã\x00180Â]ÙG\x0007³©ílúíluäO\x0015lRæJcÌ¬Õ®´®\x0019ÐÖNÃ\x001e¿c.\x000f»Äìû=³\x000e|!NtQ\x0001	Yr\x001bÕ¡ÖFy\x0002&æÐÍlb\x0018;¿´ç\x0004\x0002mh\x0002&\x001eÊÎ±f³xRfÆ¬\x001f\x001byç)ª¹,·¥¢û÷ \x001d­¸LÒy\x0011ÖHÖ]×h\x001d(¤Å¸Älþ_`®}\x001dÎðuNjÎDÿ\x000cÁKëÊ°¬\x000f\x0003\x000cÕb¦\x001f»ú\x0014­IÓ8;
'urQ\x001dÊÈuFý)5ñ×\x0005zÚ\x0003²\x0014fz8P4AW\x001bÙý?à±&8#\x0018QMÇ´çÆa¸eF[w ä(1\x0016¥S\x000c½kðj¶EAh5K3º]×úmÔ>l§|ÈÒá¿ß~yÊÓ\x001f\x001e\x0007ÌÅÛ/ßþöpÿ×»ÛÇgõØCbH¹Mgf\x0015ÕZ®­lxûpzqª	6.Þ^^\¿¹<ÿ!a¿\x0008m*h3\x0007ZDÑTt<\x0012\x0001UÈ
¤?Yê\x0017Î¶\x0015´\x0001M"}¬n|\x001dwë¨ Ì®ÒAÅ\x000c\x00153Ì`N\x0014Öù\x000c(5§Ê\x0005Y\x001c\x001e\x000eÆ\x00153Îa¶Ã´=À*	\x001aA$õ*\x0019åYÐÅµ\x001a{ã\x000ch\x001e2 zþUÖD«óCE\x001cæ\x0010Ã\x0011]h'½Kj=ÀEkw(èXAÇ9Ðß\x000e\x0007t\x001f¤nTØ®zðç@kSAk3ÏÔ,MLí¿At¥åQ,%7ñPÔPSC?µ\x000fWéÈ\x0002r¸JÙ®\x0008¿;{¨\x0005¢}\x001d\x000e}¿÷Pô0ßGÓºã·\x000bTµpTp\x0007[ ¾6µaê\x0010¤ÜAi;tè\x001c'§èC¹<\x001djS9¦\x000eëy/ÅÝÈÔ"3\x001aáP©GY~HÔq\x001eµãÑ\x001df\x001d\x0013í8B©Ùºö{zãS$$\x0003GD±+­\x0010ÝÔªCmÔF7ÃÖVK-òÒó\x0002ÑãÓX¶LÌ£ÞHNgd§Ê¦vê$pFme\x000c®Ô'çA×É©Ò²æ·ùt&\x0003WZÖ2'Ç\x001cnÔé©©\x0005"¥ñ u^\x001aâ¡6£©#£\x0013\x0019
&\x00154Ë+§È8R\x000fWm¡®\x0015d"ë[:ÊDç2KW=ó¨ë cæ\x0004 ¸A-Qû1·qÒR°\x0007[×µ»6sÜu¦H«íØV§\x001094\x001a¥\x000eñÙÚñÙ9:\x0007ònÔ\x0008ãº\x0006\x0019f´?»¶õº¶3ÖµÎÍxCoÖbkM\x001a|Üá\x000fåCÊÊÇá`>çL£\x0004'àxÊõ«M=,o\x0016µ­©í\x000cj-}µ)\x0008ª1å\x000bA:%*-ëyÔõ\x0000f	Òá\\x0006Û¥íx"Ð0J×\x001e,È@§Â<®nx\x001a»¥µÂ\x0007 Æ\x0019s¨\x000cÔ\x000fæ\x001cÐ\x0016\x0017þ.ùòfÔbk°Íu3òTMÚ\x001fÜ\x0000\x0004À¥T´*ÔUÉÄLj¬©çØÚRv©­\Wk%\x0001Ý\x000e
ó¡®ï«qÎµv¢ðkQºJ¨úÏ_6\x001eìz¯|\x0000\x001d¨çØ\x001aEÁÍ§\x0004\x00199ëÚ
X\x0007tsÏ2&Ù\x0018yv_²µÜñÁáÒ\x0010¬¯ËpÎuÉD\x001dx \x0007¦ÿ¿x±õô£Ì3Eb\x0019¹>}á·´\x0015ÙDMq=¯QæÞÄ­:ã`n¢$©Ö[\x00114ÐcÏ(è\x001dt±>|áÃ¶EP¬MùªDq69Øµ5ÝÊVÐq\x0006´h\x000e£6Xk AËFÔ\x0007³tQÄDÐäf@GYÕãEHÚÒeÂÁ<5Ö¦Æ9¦\x0006×6tË:¡\x000eÒ\x0016híÁ|^ý|sÞ,MQ$ùÅñÅ(\x0010êx¨l\x000f]mk7ÇÖGûR5$¿j3îE8\(¯Ï8ç¼h½äáä\x000c<øØuë\x000f¶@ê{\x0010q\x000fB	\x0008§M\x000e¼(ÉÌêÁÃ­ kh=ÃÔúû²©(Ó¤\x0003ûHm\x000fG]/9/£6Êpo0F¦c¦\x000f0R\x001f¬:Á\x0015£uè\x0001Ñ»©E3iètçë==No\x0007o\x000eµ¬]}\x001ap³ÊWü¸¬Ñ²@ÖÒð\x0006\x0001\x000f\x0015Í]½\x0017Ý½£3\x001a'ú\x001aä\x0011Q\x001dêàåê£¹s4O'\x0000~\x0019%j~;×æàÔ¡¾\x0006	s®A¼{2Ï\x001aÚ¡½
ZÓ±^ÓqÎöe\x0016-XÓB-²\x000eÞÀ¡N\x0003±>ÂÄ9GD\x001d:u~ÖÞ­íál]/8gy c­Ûdk¤·¤¼¨å5×\x001fìÙKoT
?÷\x001b\x001båé<ðÍÞ ¹\x001bU5\x001eÈÒZoÔ\x0019êYËÚK0)ÒÀØ\x0017HÔñ@þ£RE\x001f°qÛ\x000bA´\x001a¢	\x0012ÍÍX\x0011\x0012µ>X\x000e¢êæ[¾\x001cæ\x0017ô×Âñ	,%}À÷7>È:w°ëv\x0013q\x001eÀf°\x000fo`ÙskÐã\x000bÜ\x0018u\x001b³'Z\x0014ýú)¥ÑsñÓêé~õ¬Ô\x001eÒ¼,ÁlÑó\x0018(\x001bO0ÿ+ ¹ÏsñÓòæ|¹Om±Le\x001a°ÐÈÌñd=~³ZbÆònGcìd,[bÙéXÆ\x000cdc¥oEY,\x000bõ&(\x0008;zb_Ò&Ö0ý¢l}Z|¸û}ï:sµÅH-\x001b= F¾.LnuW¿ãÍâÃÙ½kÁAÿ?uï²\×Üï¾
\x0000Q·¬Kh\x0004R\x0010\x001b\x0011àÅ ©8í\x0002\x0012a5ÛlR\x0006¾ü\x001a¡ûLÎäÿ\x0006z\x0013?É©¬Ê¬½rcík¡-°ÝM åÖ§\UYU¿D0£ ³1h½ÃQP$Kh\x001d\x000f9y§Å`N9\x0015\x0018¦5½´ÏãÛ\x0005«¨D±\x0005Ì\x000b0¯\x0001Qsèë\x001f#_îq5{plþ¶°°WPÙ\x000b/Ï©¹ß\x0018\x001e\x0015d\x001dÛ\x000bg\x0012l0X\x0014dQGæ)W­'I\x000e¼ÃåMéæô$ \x0003
¥**çràk¸ºWIu x?ÓK±\x0018¬\x0008°¢\x0002\x000by,þêgÍ¸¬\x0007^csbKÉ¬ÜVµ/M	Ü\x0017á¢ãnsã¹ô½z~ÆÅhY¢eÕB3®Ý+áÇF\x0013¸e#ÔÝ°\x001emRsØÊj9Ñ;\x0006nONÇc«ù\x00126,µI^wg*4,÷îkÍÙ4
{Mæ³)ùv³åh Ñ4ÛÀ$G7/ÎÕ3.\x0014±;Ðâºßb4¹Öj­\x0019ßC2[?l\x001f \x0014
øg\x001f6aIeÅ PO[ýeB1]#²M§ËE¢\x0015
Z]ÓÙh±K©¥Aæ¶ø
Wä·,ªo\x0019<ªn2Úø$4h\x001bb
W¤ÑÊh½®Ðá\x0000G8­s9á¥\\x001eÉðG\x0005\x0017JÞÓ:³nÍñT¢°Ñå
\x001fÓËéu\x001b\x00135Ü»ÑLÉTTc2ª¤Ê.n	µ½\g^·Î0.\x001d-íÜ\x0006´Î8ºm\x000b\x001aH4ßè"ª\x000eKY©\x0002Þòq\x0016ýJZª`öBZÁ \x0014KEqÎàÌÄþ-sÉLæ·d'JÉ¦0XCë¥oÎt¹CBãeææä5\x0017£É\x0003=h\x000et¨Y%
qèÙú´óXfvN*z1t\x001bAã6*Zë³nh5¿£Ñé9q*àÌ¶áb4é7Æo@Ìa\x0010îSÒ5ÄQÈ\x001d­¢\x001b6'Èm\x0000ºmP\x0001\x0012IÍÇD9zÀèÐÀnXk ·\x0001è¶\x0001Îf)\x001d-%ÐB\x000e\x0003-Îii.Fs\x0012Í©Ð*@/W¨V³\x001c
eOO¤Ù\x0006ØpzÜ\x0006 Û\x0006.©l	Àâ·u_òRónÃ.\x0000ª&Wâx\x001c¸-~çq-µd;«\x001a¼\x001cM~OM²^Ñ
=þX´_¿à¨h|uszËKÑ¢Ü QµA3ó÷\x000f3¿k"YÍä-ZL\x0012-©Ðb¡·Iq8xß\x0005	Â;ÚìÐ¥hInÐ¤Ú \x0019oÜ»ïH©y\x0010Ü\x0014JÓ9Y&7hRmÐýÐ\x0002=ÙXúxJD\x0013N[&­\x0006*«Õµßsâà¹S\x0008$|ÊdqNQ~)Y¶,[\x0015iÓ)\x001bát(OHd6n8@³\iYµÒR)\x0014vØX¸Z\x0006%ýØhf\x0013¼âÈ+\x000e¨A?{µZÙ,e6\x001aÌ¦XL&÷@Ví\x0001o\x0016Ýs\x0018(<M¦&.d´ë­7ò{¶\x0015l(#Ãlîàôp¼ÏëÌfÂÞ5<\x00167¢Õ~ý?_úóâ«ÊuD§FD\x0014rÎ$þù*aÏq¼|Óß\x0013_Uª£<\x001dÌ\x0000³ $\x000b$¹o%Q·\x0016ò-`E\x0015\x001dXH\.+¶gÍ
¸ÝÝul\x001eöíêÖ¬ÿMWw7'Ïn>Ýþ|sòúúã»\86ì¼$jµ¹£yeú>põöüäÙùË«gç'¯Ï^|û0b9\x00057£PÛ¶1Ê
\x000bläþ%1ÎRå§X^eOy|\x0012ÏC\x000c­\x0003zÁ¦"Ojª0¥
o\x0018éµÎã\x000cÂ>U=4ßÅ-jy\x0003\x0016L±@e
Òy\x001c¥×÷¢\x001fE§>ÀO\x0018§Tq9UÍAN#µó¹Óîð]\x0019Ý|q©Ò\x0014*) \x0002«{ò#¥w\x0017¸AÈ§6`)VÑ`ÅÑ°éÇ-\x001bÈ^ÑbM^ôÑg\x0019Í6Ì£O\x0010G\x000eÑ>ä\x0019pÁú
Ö²Òª|iÀX\x001byhÈUÝ£QcZP¦æ\x0012¾Ôj)ªÂÐl°Ôº2ºgÑàbÜÀ%©UxS\x001c)¹o\x001f\x000cq.ý(ð¶\x001b6£\x0015îÔ*ü)rqëJM-i2ã©BX,¸\x0001K¸S«ð§5¦[ÿÖEhi°\x0006Ï¯¬Ë>lÙÂ¡ZG\x0005-êZÇxºs®;#¦Ëj¹Oµ\x001a§\x0002Ý\x0011×ÐÆÓh-G\x0008íU\x0005VV`\x0015 ëÄv\x0002õfÐà
·sÕ#h÷\x0012¾Þ*=Ä\x0011EÔï8¸J\x001eíë©põNáêq¤§ÖÙØ*£ûâ
ÜÛ$2n5ðõNãëKÓï\x000b°À\x0012¹Ð\cu¹5\Æî\x0005¨5²ßµ\x000e¾üÐrF¬\x0011|}4ßhÍ3½øÝUÚQ%l¸æ­øt¿ ûåeË\x001d±\ðõ9Ý\x000b\x000e+(¬\x0002å©Ù\x000eg»r;\x0004_ÆâðÅÇàSÎ¸³&J\x000cê[X\x0014ºzEfÎhhéA'AQ\x0005+H­c±QìÑ%Ð\x00148=wp¿\x001bP\x000fê\x0004¨[\x0007:\x001eØ3Ë\x001af\x0015]ì\x001a\x001eÓ\x000bL¿
³æ1dÏzÖA-ô@[Lº_ü­\x0007
\x00024¬\x0002uyìy\x0003CdøtFªd\x0005i\x0010¤a\x0015)ßØWR;4-\x000b?ÇcóÅ#°)¬²iÝBÝ¤©Û\URfÐn>=h\x0014 q\x001d¨gÿr¢(¬\x0016&\x0015[A*\x001dé*Oê\x0001»};©\x001d\x001dÆòÇ\x0017³W&aÓ´Î¦ë@S\x0002z¨¤mÂcØ4\x000bæU6
ª|Sô£Á\x0017=S\x0007ÓÕ\x0016aÒ²Ê¤ÁR£K\x0000,;S],B|\x0004RköÑu¨æ.7Tn/5%
ÔG8¡ìÞ¿îÈÇ\x0010¯Q	_\x001cYlrL\x001fÁZyæÛu>Þ)Ñ\x0002¨çUàþh:£²3ÊÊcß®;÷\x0003wÍ»S¸):òRu3ºzTyðÛu'(§dÓzðg¶é8¥ì®T\x001e§vÝy#AûÉ\x001fK`9µÑ\x001e_}¿}0ÚJço×yÿt\x001a³£\x000co'\x0005/ªaÔ,Ió:RÖ\x001cp1&zÆÄ¾\x0018Z©)=Fê¤Suëjõ¤Ô\x0015«'àíïH,-'È°ÿ\ªnåRõèô\x001bª1\x0013%\x0007òÿiNs\x0005j¨ëBªÄÕÝ#w¸QDÌcdÑN©n]
,\x000c_QÃ°ªãöÅdfÔ®ô¨É	ÔäV¡\x0016\x001aøSSfCõ¯\x0015\x000bÿb1±VS¨y
jS2j,XqÔH}à9©yF4@O¥Qó*£Ö¨
\x001eIP-|UL3\x001amzT\x0019ªºu±j4\x001cþCärÙúýùX¨xéVý:·\x001a[µC·*_*c+/ô\x0018	\x0001 _\x0017\x0000ÆÈ·>à\x001d5ÉL×*ÌhÍèQ÷.~ÖE1s³\x001dØÂó#kVHÁJ\x000cbU\x0019\x0001úu\x0011 Ö@:BÝ	yzAÆÜp\x0002xy®úuçj\x0000\x001aëB<ÅÈÃÃÅûÚzÔ,Q×¹UÏ-¡¸¡öåÆdì9­
=j\x0014~\x0015\ºë#\x000c9ðEë9±¢1t5j\x0012mQ­BíÁJÀ6\x000eZª\x0003ëø(^UÆÕ~]\\x0002Þ»Pc\x0001\x0016Ö\x000b<²\x001dòc|þ \x000f°î\x0000ÀÇNúüà\x0000Op,U\x001fã\x0006 È\x0003 ¬;\x0000Æ»¬\x000bF\x0003U«\x0016VÕx\x0003 È\x0005\x0010V.\x00008u´\x0000â«iÃ\x0010\x0000\x001b­s\x001fõ\x001e\x0002?¡M\x0005_ú3ÚDîEw\x0007hÇ\x0019×UüNá\x001f#]©.\x001f\x0017OÀñ\x0014úeòX\x0007£+ÿ\x0018ÇÉq7Ç¸ø\x0002È¬öÔg~±â«+ìÞ\x0000lÙ\x0013Ñ©QëTDçÃõÉåõÝßo\x000e\x0011ÖÔ9sÕ$\x000eèJ±¡éu­\x001fçæ¤a.Ïêÿ¾ý×óÑÜ\x0014Í©Ð,pu\x0001¦UÔ¢a¸4\x0017ïX6ù)WÝ<\x0016¬0\x0018-\x001a\x0003MHéÑÂ\x0014-èÐ\x0012IêxôD*çGIh'_A\x0006S2Ð¹þ,æñ\x001a¨S±J¿BÙW\x0015§XQ5DÆ*\x0017\x0017\x0006N¾eÜö)Ó,éÖ\x001ch2`\x0017f#cER]à6£å)ZV¡Ìý÷iç1`Ç(S¬¢Ä¢BÆ]R§QÁ<¶¡­"«9Ñ~Å|äùww'ß}º»=ùõÿ>yúë»¿\x001e<\x000bRM\z¸\x0005uÝã3QeB%FWl2{Õ?ß¾=ùîåÛ«³§¿;{û=ç¦xN\x0017ÈÛB±²ÁghrÌ>nãVWÆQ]©\x0000Ì4G\x000fpoo®½¬«\x0002É\x001b\x0001A\x0000\x001aÐÐêæSp\x0012
ÝSWÀ`ÊFÀ(\x0000£\x001aÐQ	\x0005dlÇ¡\x0015Hj;\x0015ÐoÄK\x0002/©ñì°\x001fNµl¿Dxnó\x0007Î\x00020¯\x0000Ì¡\x0003zOõ\\x0008HÓÜã½"r5`\x0011eÅ\x0007ö´EÆ¸Øæçu@³_a¨\x0005VeÆQ©[Ý\x0007b 2V -@(û-:j>á¢ÞG;jp\x0005¬Ý\x0019|ì£ëo7:A'´ÚK£`\x0016-Á\x001a¸$Z6[¶àæ/ì\x0005 _\x0001ï/AÛ£ö¶\x00047z\x0019'\x0011§>F*` /ãíÄìe¬Ýè¥8Fú\x0018Á\x0011eç\x0006\x0007`\x0019np+ 8Fú\x0018A@:E\x001cµÿU¾ÂÇß\x001aÈ8á\x0005Ú\x000bâdÒBØÒxôX#ñ±£Ý\x0006è\x0017ôj/#57W@O·\x0002Õ13`Zí\x0006]/\x0010t\x0011Û>Jo>¼¹ùüùÓÇ÷7ÇOXiU\x0019Cýï {ÌP×\x001eå¥Ìµ9¿>ysþúõË\x0017\x0017çÇ/Z\Æ\x0012Þè1³³ÔÖ\x0015¬5ô0¹HZ±\x000b}¦ï_9m\x0017·R\x0011l)f(§0±À.\x000cR¯´,xÇ´\x001d3KÌ¼\x00023ù~»\x0016ð\x0015¾2t(Ø>£r¢£\x000cV|ó`W|ó1sä,¯fË0ÁÌt¹/Çt{µÕXpdZ\x001aúë?zçö÷5%½ûpì{Ç1\x001c\x0019Çd\x0000/Kà¶rq±Jh%¼¨|{¹\x0000Ï
<«ÄKÀ\x0003G\x000c6}PÌRX5ÿK°	/\x000bëe¥õ0ÓëWè¾:Å!3éa¢2Ç+ðÀ+Z¼lh^·+\x0018\x0007\x000fRÅÿ-tÓBÔJ×\x000bQUÖóCÏ`ÜgE\x0016Ý©KÏmZzB%×QE§\x0006/î¶\x0006\x0018¾=ª?ò´soVÏÄ=9òúéeøç§7·ï?WçrøÂÞÔ¯OkìÀÊª%+·Ù÷ôüêâuu,\x000bèüÎ+é\ávNçÈM\x0019ý.ÍÝ;«ðÂ\x0014/(ñbBý©\x0007­×­YÏó8gogîUt0¥\x0003%]<ÜáÀ\x0000AæEó»V\x0001\x0017§pQkº<LW\x000f\x000cëØt|\x000bçaTxi´xÊê¶p¨ðØð\x001cÏ\x0006v`g-¨ðò\x0014/+ñ2·xG/CðãGÕÛ¶xy5XñÍ^Ðrùëÿôc±4v-Pë\x0012~g
¥=÷UÆ8\x001f¯\×\x001f\x001efsÍ)Ù,`Zï¥,\x0004\x0002,2\x000bÄùÈt!Ü.vF¸½Ðù!8ì{TöSOZzÌrÙ²\x0003\x0001)Á\x001d\x0018!KdA\x0005\x0015\x0019 ø\x0000PgíI¹Ð7Jm\x001e\x001dY\x0014\x001f4*?¨\x0019\x0003Hr04dµ\x0002ÞXý¹åÆ$à\x0012ÎòÌ\x0003Ý#\x001dE\x0000Ï\x0005\x0007aN²S\x0001W\x0004\QÁÅR¸Ï û!Ú\x0012\x001d\
1§C¼\x001c.­t[!H¯\x001fí³Z²\\x0018ÍÙaN\x001cs9\\x0016k.ëÖ\Ì\x0005o1¸ßd&ÕB²|ZÐÃ\x0015a¹¢´\x001cN¢
aëÑ\x001a	.ñguvFOq1Ü$\oGÑÒ\x0005nÃÂ\x0007rª¿\x0000ÏóI§§óÎ+é°ØúÙê\x0019K:\x001dàX\x0018¥'6ÑÉcÕk]¢×JWX\x0018|\x0018¶qÓ
.hé2wØ`íãM\x0001Ü\x000b\x000eÜù,¤'«U\x001e­1z1¬tù>¬áêò&ÓÁ^¼¤7\x001déa'H¬\x0004~ôz\x001f¸{\\x0008'ÏW«<`±³¦\¤àXx\x000b\x001ck\x0019fØ°.Ëïßµ\èL¤¾¾0PQ\x001c~fhÃb:gd°i¶«K:¹êakiÃ*r|¢\x001eÎã\x001fÔÁµæ²F<×ÛÔ$ûÌßòat'NëN`TëÆè¨µ4Ìµ)o£bÙ¹¨\vÎpÙs,\x000bBàC¶~Ù-ÎÎÉ-ë´[Ö[\x001eÿ\x0012ÓO0­å/k7m\x0012\x0005\x001d¾\x0011kèl\x001a\x000eÅp{[\x0008,ÃC\x0013¶|Y/\x0003\x0014¯
P<`ÌÔ\x000f
Ç÷Õ¡X>)\x000e¼°,¥\x000bNEkèÞÄá¡Ñ\x0007öVÓÂ¤M¶óYÐay±&K¬Á\x001d{\x0014l\¤]a¸É6¹A\x001dËé¢¤:ºX1\x001a	!':Ç­JY\x0014;èéd¾ã	\x000fÄÀ·ì)Ù!Ø8áÉyKJ1
ÓàÎ¡ $M`Á-KÞ>ðÉmÚ\x0014AFíA\x0019µ£¸«¥Þn,nï9hOuSlKÂtø£
n²cMâÇ\x001dT8&:¿)h\x000f2W\x000cÊd\x0011júJè{\x0017*íñI1§;¾\x0018\x000e¤+\x0006¥+\x000eÙóªÃó\x000e
Xÿ*9ûåtVÒY-]ä\\x0011?,I:&NwO[ÎXÑ\x0013(£§@êAØI3Öpü	·MhÒÑÒÑ¡\!·aöa¥ÍpX¶­9¹]A¹]QfÖ\µ9\x0017X8*)ÄLÌm£N\x0017:PF·-dN(ÆõDÜv=\x0011ø°1(?¬á1ªà\x001cWSØÄ¡I["(÷CÔî\x0007ch4KÝ\x0012Àg¿alxôþúák'1®ðWÊ;
ÝÒ.Ó6,K\x001c«\x0006Òî)àãû\x000eÖ~ºû²dv5\x0014©\x0010WWÇ%pX2Î0!÷ûòíeC¾\x001bÖDÝ©a5ë`)djË8æÞÖ-\x000fë*yºæ´\^ry
	TWë°z'ÐÍ:çýE´o*¹¦W\x0012\x0016úÄR®è2¯°\Ýp×¬É\x001bOs¢\x0018T	\x0016$XÐ¡\x0010>Ýö{\x001e\x0018<k30=Lµ\I|Hüq1\x0017ÌÝíÕÏrh\x0019\x0016O=«ÖIoÁ¼U\x0018¬æ©ã}Äzö\x0015>qËo69	æ4`XQB\x0017­uOF\x0016ç\x0003´i4®\x0005KÌk\x00188 *Ô¦TÈ\x0016ó,£[ÝØzgáå\x001aóª5¯4\x000cÖôË\x001bØNï«õÒïÆÎ60\x001c;»\x0018\x000cç«±º9\x001døóåõ+,È³\x0008T|È<N#\x001c³F*Üã	)Û
K?L
\x001aW\x001c¨+ÕÍå\x001d©ï\x0012x­h±äÂ\x000fmù¥ïÆ \x001a\x0007ñ-´hyÖ\x0015	V4`ÁRa«)üÎ\x001d¹ÅU\x000c+@\x0013VÔ\e
#»\x0018¸¦ nS¿\x0001\x000c$Æb.Ñ\x0008Pwç\x0011IÎ\x000c.·~M\x0013'äJ*®0n`lâ¡8¦3õ´áKf	5`ÿÌÈ5ÉH,i"1\x001fÝPøH¯¬\x001d\x001a_ín-\x000c]&tõÁP¸\x000b8X°\x001f&Ç!=S6XÌKyÕ§4,Ý]½2ÍJ²¥%\x0000`ýÚOÒ½&{õ¾æ$+ã\x000b¾l4%~<³¬\x0005òKFÍìÒö]D*\x0018@²>ÞI2ÞIx§þÌ%x\x0001¯§\x000b8Íd7¬0y\x001e%Íyäë
c)«zP\x001a\x001au\x0018xé×%¶þKf\x0019SgMLÔHe\x000f§\x0013Å~\x001boxy»>âÉ Á@\x0003V³\x0010:(½OtûùÎ'²ú ´Óº@LÀñçÅdÖ\x0004,A
=¬E²9H\x000cBçB\x001fíÿp½\x001fï_«r7à¡\x000ekÛ&¹\x000f\x001bvf\x001f~Üß\x0002?.ß\x0003ÐßÚ\x0017
C\x001fS\x0012/5\x0003ë7'ÚíÇ}»-g\x00033\x0006
ÔÊ\)»÷»-\x0019¯¸À£¬\x0017µ<ñ-C³¿°Àhýª,UL^\x001f\x0003áWýiÿ«þ´ü«fÃ²8¸Êw­ç±\x0017¡øM÷+û¶Ã;\x0016ípæ-¥À\x0019'3µl»¼j³¼wí\x0019ò1iÍw··×?×?½»;¹úÃ§V°\x0014\x001a\x0002|u]¦.1æ/íÏë
xWWg¯_×?}ûöäêw/_\x001cS!X7uë`Ç60Óµ¨)\x000c+æ\lõSX¿\x000e¶F¿<\x001aÍ\x001b^\x0011"·©äý	wkaÃ\x00146¬´læ\x001aoß_¢1,ï÷ª¯SØ¸\x0012¶IÜµ\x001e<"yîóþ´ÃJÔ4EM+·W¦ûònWÚ^àÒ°ë¾ÂJØ2-ë`3wiÔ#"seZLÔ¥Q<væ>\x0006ìä\x0006\x0003\x001dY¹
â)·Ð\x0015\x001e ÉÀ{â\x000f+Q¥]éd±\x0003
81y×OwOÈ`%­p²v¥u&|·æÄÀ^Ö\x00166x
fµ+Ýlá©ß\x000e\x0007éÒ\x0006Ë½y¬5+¼¬]éfQ	\x0016aUù\x0000ÖÅG:m'WqH\x000b+ýA¡\x0017j[¿ë@æ1÷f{®\x0015g]y(ØÀ£5±uû/2OwFiìÇ¡\x0015Ç]{.\x0004ÜXÝ#x\x0012iÃ°k¸Z÷HËV\x000bvåÁÐ»¨ºG0#î²\x0002ó¾ÌÉ:X'­[élk\x001e`È´u»qDk"\x000bgnºÀîÅ³5HxÚ³oß#ÌAÑhúÓ>ÔôäÔô\x0016×#«îÀ\øröìê\x0002~ÊO©ürªÜ+ \x0018~=&\x000e¹±4\x0013¤,F
S¤ @BÑ$ÒO*:Z£ÉeP}6
\x0016L±@U¿_$ñ½¨õ\x0011÷\x0002ïÅ²ÅZq\x0015\x0015X)S¿\x0008*ãóSÃòC\x00130¦\x0019ÿ·\x0018+M±\x0002«°4}Å
½`\x0004§ë0Ô\à³\x0018*O¡²\x0006ª°'òõ-ÚèX:,Îø³ÅTeJUt_Ô¤*ÐÂ¢ÑöjgÄÜ`EÌýð\x0007
Z\x001aW¿¤Euµ±²`ÃG\x0004ØÈe5þ!SÚ\x0016ë\x000ccqmð\x000fVøw«pð()iÓØdËÒk.ç[Ì%<¼Õ¸x\x0013I§}ÇBþ4ÝfÜ°¾ð\x0010Ná"RLôÙõ`»ÚH)0NÄiSK8	§ð\x0012Mí¹\x001cQ\x0014QÔ¹ÂL¶\x0018Kx	§p\x0013	
½cB
j©
\x001a\x0003\x0008Æ*>c\Çv²¾Ð&ËØv\x000cµ«XÍIïDö1¢j¶w{f{÷-î-êÌq\x001dÞ¬ï\x0002+×H[pØ§\x0003\x001dÝ?7\x0018\x000bûtAG'#XVºF°Û¶ê{kîÇ¯cÍU²=²¯ìzìú·&á\x00071`³þ¢\x000fØ\x001c\x0015ö(ÿäæöçÛúÿy0ó
9²F\x001aYm3ø¸&\x0008õ\x001ev£Ì\x001euó_=;¿zùâhâÛA£\x0004+@Sò\UåMbÐ\x001aèò\x001bvÞÎé%§_ÅéG\x0015\x0000V*tßç½å¶0ßE¦\x0004-\x0012´¬\x0000}êW\x0007õTàá\x001dpëQHsM :Î WhX³Bqìëà4\x0014²{gX'Äò\x0008  Aa
¨MØ^Ö@±\x001d¹WYà\x0016gÐ9á
%gi\x0005g=WvD\x0018½õf\x0018tÓ·fO±þ\x0002\x001fw¯n?ýùæãO\x0007	kN
ôö,\x001cÝ{¾0æ7û««ß¿xº\x0000ÎMá\x000e.³ [ý Ð\x0005ÝPv&\x0011(P×³MÔ\x000e\x001aP;xÎ\x001bèe×¡¢Ð,V<¸Nrý¶KéÄ@·Ò\x0007ºiè,ëXb
\x000fsõf\x0000TÜ\ÿïr¼"\x0017Òxé1\x0013G¡R\x0014\x0004 ;MSrÝÂKñ\x0000Ê\x0014\x000fTáeO%â`s"%\x000b¨+BÃV¯¿\x0005/J¼¨Åkoi
¯DN2\x0003ÍyB¼Ù®ýåxòãòãb\x0015c×\x0014\x0000g3Ïæ\x0003k\x0019/¦Mk¯\x0018±5Ñm
È9\x0008Gð`-\x0010}\ý¦[°^	:ëEÃóØ \x0014\x0015x´CÝÙ\rÉ\x0012/+ñP¨¤Ñã<¡EÆ\x0013í+àäÊ+ÊW±xt\x000cxÃcA³\x001bta\x0013\x000eÀ³Ö8%\x001fNXî|=¤Ý¯Ô¯KéºY-å|qOy¦E@|52 ©º¹X^{¨	º/\x0019Ét[7¡âA÷,(úBÒÇÕ£ð÷\x0015sYVðå=¾¬ä³. 8\x0005«|\x0010/ÏI ,æ³V\x001bíg\x001dçÁ;MÚ¢\x0010\x001fÏµ	nÛþ°2hi?«ø\àÛSì\x0019¦ ªx¾\x0006\x000cVÙZ¥gNÎðX¥Xqøn×%\x001a\x0019\x0013BØöua\x000f´|
\x0001 Cn=ËÖ;pÃ°oÏ»X¥wÁ¯Û7oM)¬ãW¶ÄómÀKZ¼D\x0012\P\x001dÍp.>|ßÄ·ç\¬Ö¹øB>M\x001c±ë«ÔØÌÓ»hHyÓætø7>©:¸¯ËI\x0002ú\x0019é+\x001fÏÛ1³ò´Ëù¬´³JûØý!LÑõ¼õÀx³2\x0017^Î3îq½\x0010ãX\x0010ÚããG÷ÐÎ$º\x0006Àf=vÕi¥Ý\x001bb\x0017\x0007Ý¹»~w{óåË9Ë(\x0000Or&\x0019Å\x0011iò@àÞ\x0002aæµá_Þ}{uþæÍÑq0vo1Â9\x001d\x001c
\x0000qu/¦»!+YÀÍ¼7OØ\x000e\x0002·{S\x0011Ì+­\x0016Yx0×}ÛKÍwò*%Í\x0015Ãj\x0016¦lAýE-`Lk@e,
\x001cLá@¿Ü,ë¬\x0010\x00197^4Wó®!KS²¤$ó¬[L\x0018\x0003Çýh¥-pÖÀå)\Ö¯·Þ\x0011ÁïÖ\x001bâ!s}\x0018\x001a¸2+J87¦úÔC¢+"UËñàìM`\x0003\x0002}Q\x0015\x0016Í/Æsìnðr¿éÌc¥Nz^­ëµ,¼R¥.4´\x001bC2s\x0005d\x001a:áE¬ÖD:µ\x001cV=\x0018\x001a\\x0012xXuý235[\x001a:áF¬Ò$úâêÚßíVn1níº«R©81LÌBºúôÓ1¹¼<NPãu\x0015XºCÜ\x0006ìæ©\½|ºÉMÜr&j*Çú\x001a` 2ôÊíì|eD~Jä\x0013\x0005Ë}«8Õå:¸Á1g;;ik\x0019S2åLvbÀ`*Ämá7Òì¶|:Bb9ùÓ\x0018\x0006\x0014ÉYÙ2t¿Ý4ÁÒBÅ)TT¬'3 l¢Ëàº¤\x0012ëùø
+*M)s_*Jæ\x0004\x001a+c¡Àl*S¨²\x001c
ÌN'Ø² ÛYHSiÅP1íy¨ê	ÇÑÓÞ1oo~þt÷ápJb°\x0008\x0004l8ås\x0011\x0008ï½yáý\x0005óêüÙË·G\x001fZÓ§ªlNÉf©j².ùrøÜaI¦x¯6Q\x0016¦hA
\x000bà° DvsyÀp0\x0003\x001d\x001c6á°8¡jæz$\x000eËûU°:¸4K:8ðÃ¹¢\x0000Xw®e\x0008Éfî¥rËà¬ß;¯ë/Æn¸;yróáÏ¿þãÝ¯ÿ}{¸¥þOÿðø'Oú»P(Ò\x000133ùÉùå÷çß_- sS2§"kï1½!\x000cÿ8Ô²iXVAµÃ-h~æuFó<ÌÃ\x0007,3 2ïØjö^J¢B\x000bS´ ´¥ÅæQ¢5ÜÜèõjS³6 Á\x0014
Th¾XB_\x000f2ôÀ2É\x0013\x0014ð÷ÚÐThq\x0016uV«¹\x001b¶
XCZx@Ù\x0008¸{*²4%K:£%®£¯dÀ»ÀF\x001b\x0007Ú¦¥§hY·\x000b2\x000bíúêjIÕ\x0015jØ¬dß«©ÀÊ\x0014¬èl\x0006Nø
\x0016P ¬ÙÌg^h!í×NjÐ&i¹4·,4Zý½Ö¡z²Â#O\x001cª[\x0011Ù²Ô¬<
tg\x0001ªÖPç8*\x0018vã!»î¢*6q\x0018XÝiP\x001d\x0018=z\x0014T£áÓ\x000e/\x001bé º×z­b\x0013§Õ\x001d\x0007õKR\x000fNõ\x0018@/\x0005Á:ÿ\x000bb\x0004M\x001c\x0007Vw\x001e\x0004G§{\x0001nS®\x0001;\x000f7ÃÀ*O\x0003T¸í.\x0017PËÞÓb\x001b6Û¶GÅa`u§A=.OS¤ï9×88òÈyk³â8°Êó\x0000ÒØ£\x0015(¬\x001fk-ûý«)\x00158\x000f¬ò@\x0008Ô\x0011*\x0005Ö27³añVC«gÖ¦O*N\x0004«<\x0012
P\\x0004Çn3ä\x0003\x000b6 9q"8ÝàcS;à@ýî`áNØâÙ8\x00112;°alR\x001fYcÍYVçt¯KTÅ&¼®S\x0006á.r8	±`ùe¿HcÅhÂ~Bª\x000bÚÄó§\x0017\x001d`K÷j¤ò\x0019êÁ|«æG,nÝªó´îR$ªmÖfñºýüúç7_\x000eeËÒÞÚÂQeÍëé`°\x0007
={qþæA²,È²,å&¬ÖÈj*Ã\x0012+1\x0001ùÙbËedÖ
2kUho@<\x0016ù\x0006Ñà7\x000b're5Ú¤\x0000Ñd#ÁCh8oôH|¡Êü\x001a'ñ u¡å­'F\x0003ÑPÔ\x0016øµ\x0018;	X)ÅÎ\x000e[Yæä\x001epªMÐ¦%ôPÜ\x0014ÃBIØæ@K-ÎW/.Dâ{îµ.=\x00162ÉMÕ%:Æq\x0016RÎÆí97²i)YF+*£¡No"£%\x0016\x0015
\x000fy+rhÑüT7>?~-ßÓO´\x0003\x0010ÍZ\x0005\x001a\x000eÀ°lµÀ#éç«\x000ffç«.E®Ã«\\x0007dÇ\x0002\¶FFtU³\x0017FËf\x0013\x001aH4ÍZÃp¨K\x001cûúpÐæ³ã³\x0000æËw\x0017¢É
êU\x001b´ú5>ÚM
-\x000bÍ£+$WÛ`¶®i!ZhE\x0006»m\x0002=^\x0007ª^¶iJßáU¾£¤ñí
\x0004\x001e»Y3\x001a6/\x0006[\x0016&
-\x0018\x000f¬A³ãB4\x001aYî\x001d\x0015\x000ea©ó³=Xñ=U}Ïjµ^àñ%'®\x000c¯æçî\x0016y\x0019DzÕ÷t\þïë¡2¾ç(~©g×l\x0005ìB´$Ñ
­&.t\x0005X#y¾.BAª(óÅ\x000bÑ²üYõ=Í\x0018
Pr\x001a®Ã\x0004.}I³ó\x0018\x0017¢pA\x0015áâôÔÀhá´3\x001d&Á\x0006£ÁDË®%\x0015Yá!'e\x0014\x001dÖ\x001fAhn¶Xx)ZhEåoÇÛcÁz\x000e\x001e9;Ð¶l\x0002G;èöÑ\x001eá7¬Äï-=Ù\x00163ß3¹LÚ\x000cT6«©]\x0004"Û}ÎqcjÜ|í÷B´(Ñ¢
ÍZî\x001a/nÜKÖ¿?§/_å&ÈM\x000f\x0006¤Æ_p¶\x000e9\x000e¸fnÃÁ^32	¦±Y@½L`0b8Çk\x0002«É¢\x00117þ¨ ÃÖR\x001aðVã4\x001a©ãò(£\x0016úEj4h BÃ[oÖ\x0007\x0007¹P¸"8ú
\x000b
\x0005¦hQ\x0016¹ ¨\x0015ÆÓÕ\x001a\x001clKÈª\x000bS²¢"«Î6ôò+\x001cqÈ¥N%\x0008
Ìw2/E\x000b\x0012-hÐB9å2eà\x0008Òy\x0016q(qKÎä±TÇ:\x000eÔ¡c=ÛqqÅ±\x0010nøÉ°»ÃÉjÂÄ\x0003+k\x0000És¥áæçû\x000b\x0017yqv¶ùM¯HÀËe\x001fÆ¸7¿«:ß\x0012p¤ \x0016\x001aþ¨@Ã¹MTî\x0017\x0013_öÙ\x0004cÀí-dhT¡mMT¹æ\x001co$iVÄeXqK\x0000e\x0016UY¯\x0001$Ï­tÀåo`P¯hÃ÷Ìr{fÕöÄ±"\\x001fæ\x0002Æý\x0001h\x0014¯-w	bbRî\x0013\x0014V\x0003º\x001cj%¸>¨\x0003®,õfÕ`ï@\x0006üáb¶TX3ëÄslDA\x001aMn¬Û\x0006\x0015*¼ã¨&²&z¿ÙáçÉ$Ó¸\x000e
B\x0019\x0001j\x000bÄ1em7úpCÌQ0Zq\x001a£¡D§¡5î¦4ª¦(äÕ\x0012ÌËX,DgAQ\x0005¾´ÒÜx;6\²d\x001b6A\x0019^Qex\x001eïhb¤³¤Ã\x001cê\x0018h[R¼"÷gÑíÏéFÍEìâýiÆ0KØ\x0010\x000f\x0015ùÄXToÁº±\x000bPÐe\x0014"òR; 7³\x0010M^Þ\x0016Õå­OÇ ÆêpyÂTL¶%¼­\x001c1Õ1dKï,<û¼ºþDó#ù¨j\x0012^ó¦Íú{Þ
¶~sÛÍ"'\x00075#à·©b7lT¤ûiî'
]¦ê\x0018|r§ó
øT¨paÝVÍø/fâEj\x0000!Èç\x000fGÚÉªÓÇKÈÖHoÇ]©¹þµ$ò1ïB^\\\x001em%#,\x0010X ÀÊÀ\x0002Ò8È¤Ë+DD\x0019í÷ë±¢°VÔX«FÜ¤P\x0002§,ÑZ\x0012-\x0000?\x001bF.ÄJ\x0002+©°ì)\x0019\x000bj\x000cNzÃ¦°VÝK±ÄGLèá4»a­Hªé5(`¶c!V\x0016ÖÊ
k¡ªuêâª8\x0003zëK¶¼äÁÍåË¸¬\x0011\Öh>£
c/§Vh¥Æp¦öz0'Á\x0006¬æ$Ñ}\x001c>¯_]Ö¤Ò,/ãXú,\x0001÷$U0\x001eCQÍµá;NDæ\x001bXR,°\x0012Æº\x0007CAÑ8\x0016Nª\x0016[ï&¬÷\x0002Ì{\x0005X\x001eDØ\x0011K\x0012ÖÆºÂ\x0016²\x0017M\x0005u\x001a\x0014Ôùmö¤uþ\x0007Ù"U\x000f\x0015Ñ0øæÓÝíA*Ã»é\x001a\x0008ËKz_å ¶Ì´©cëÖo¯\x001efrS&§`*cÌg
ú{K\x001aj
6Ív0.òS(¿\x001c
¸Â¥Ím%åÕ>$²%½e\x000b\x0014L¡@\x0001\x00159=Âñb>ßP\x0000Æk¼õPi
\x0014P<\x001a B9®àn\x000f\x0011\x0004u\x001a×r¨2*5eñý¾ß)\x001a
\x0001/*ùæîþ$«ÅPVn>Åî\x000bb´ûDÛoRJ\x001emé3cÖSn\x0015K½þ½
ßr:Ò¢­TÀ7O÷jÉ\x0015Pb¥[ÅRÇÚ\x001aêõ¯^Ù}âM]Y¿ª¬XêV±ÖGÝ¶~µ\x0019ùa°äqµéÝ\x000fXSl¤r»°úÏæ8kß}¸ùrü´!eÍù\x000fÏ5q]Ä0\x000e>{yþæØIØØ\0Í¨àêIS\x001a\¬þE³Ê\x001eRLóñÖB8p ³DÀkØ`îj¤4«çº\x0014Îï:P\x0010\x000eTÀÅ\x0002Ø¶Öàj¤ &}Vì\\x0007\x0017÷:ê/¾±2¼yÒg\x0006~w{ó·wï±1à g²9Sà\x001ak\ÙoQ"ö\x000b\x0010f,óáá>7ð»«óß{q~u4$ëÄE\x0010µÄuÃp\x0015\x001a@,CV±Á\x001c´ÕÄÖK\x001bûõÈÅñ@Ø¥${¬[(ÂÇÙGbÎ9¯fÎÕK\x0016Öä\x0004ª>©§óP\x000c
³E\x0001+'ìÈ\x001cö²A\x00053¶¤P¢5Ì\x000c\x0001He×\x001c(\x0017XÃ,WsX½I\x0006û49÷:\x000c´³O¼Xô\x0007\x001cyZ'UeÊÎÁZ^\x001bÎ;\x0012.©Y\x0011-
3_¨½\x00069Jä¸\x00019³«C¹Ï~ÌgÏ&>£\x0003¹4àÿ\x000fK#GÁãjfïLçÍã
xlV
\x001dæ
V!\x0017¼vi$©«#dàû]°ÍÌä4G Yj\x0017OIRt£ÙòK\x001cf\x001bÀÖ0K§QV;d¥ÁØF¿ð\x0001Ë\x0012í%Î<ë§bòí\x00104nõ)Xù°d»ueû\x001eldÏÂÔ&>\x0016sÜc^½\x0005kÐ\x001ex@(2\x001b
\x001b:Ù*5ÐÉHè´úèÆ;@\x001eÚøéÒ-Ñ\x001e\x000cóúîkó\x001es^ÏìX|§\x001a:\x000cÑwÇsîðùûq 'òô
ZÊÓë ýPª\x0007Ô3¥Ä$Ðü\x001al/y,h\x0019×Ùýk~
t,<>\x0001{ë\x0012'Éü\x0004\x0017ì+Y=tûPJÙ+t\x0019\x0011tM\x000b\x000fReUq|Íz\x001cfØcõÌÚ=kthxÀL	¨ø2[*±9í1§õÌ©\x000cí4x\x0018GàÒâ-¢X\x0001íä\x0001¾'ä®F¥\x0016zÆ
y<i¼d=Öê¨»wh»z\x001bb¡3éäãÚ¦G®\x001cØÐ\x00107\x001f,õ\x000cÙ{%1I^ûp}òêÃõûÃÓáàpO·1vCÌþ,é\x0005À·\x00121\x001dîÕåÙÅñÉpIÞ[!»7jï!@ç)\x0019±ÕKpcdq©_¦ç{\x0001\x0016\x0003z#\x0000ý½¡\x000f\x0001Z¾¯IFÂ+À\x0006h©\x001c:eï\x0012^\x000eè% ×\x0001âE\x001aÍr²±.JjYH98\x0002]ËùÂtdCÝrbÃ\x0002¾léÙ\x0015~¹á)s=yJ\x001b?p(Â~áÞôÌøªûé5-(ï\x0017Ðo¬À4_M»\x000f¼°\x001fx­ý°þ§ãÙD&dThhx5;Û\x00170_tJóåÂï\x0016%·<-?\x0018ëÉ\x001f·y$\x0001\x00160®Óú;\x0016/\x0001êW¯Áöì½½OzÀ¤ôPÿ÷/¦ß¬`éå¸\x001e³I÷rÀ\x0005à^Ùô
â¨¯n\x0010ÓÛë\x0002,÷ÇüD¢Å|Ezè¢ôÐÿ|>¹\x0000v\x0001þ³ùªÇCaº\x0013\x0015¤K0=Ö¨uLËWý´¯
^Ài\x0000\x0005ö§±9.YsõéîK{´|óéîÃõÝ»#n&¶öiba¥³,;\x0011§ªñW/ß¾iÏo^¾½<{ûíhì\x001dÑ0y_Vp\x000eÉ\x0014äÀßwtµKÙY%³ÂfÎªlÇY\x001a¥·$òNEdÉ¦¯©H\x00164&Ëc\x0016oSd-Ìój\x000b¢@&¿¦S}Í\Hã'¦¼Ìý+ÅÁôYË5	E«¢
®.Gç\x000cO««ß0\x0002Ô\VrÙ¯çSNãæuh\x001cyú
Ç¢\x000e[³]1\x001bv¦ëßëÖ?¦e]tÅU\x0016ÏdÐ¼Ùb³\x0000Lå3²£wC_\x0017;Û,
+/ô½µdQÚ,êléâË»\x0018©Æ¡Ú\x0002áâÝ\x0013Àgi´¬3\x001aPIw8µR\x0008C
ÐÅJo5ZhEwnºÓ.$å
zCÇA»Ó·çÚµdA: r\x001c8Y\x001d¹<&Øä5ößt\x0007\ ârTM¼\x000f\T\x00112½ÛU41Õ\&Ï¦ 4\ ñsÞ&ÞÑ\x001cÉ\x000e&åµ\x001a­xòê¯ù\x0018ðøØIh¥wa\x000b\x001aH4]\x0018Ô¶dCC¡oGa\x0010«Wbb¸\x0005-I´¤±åi¯\x001e_åù\\x001f:RaKì\x0008rwnwÖÚ¶³¬6\x001atD\x0016·\x001c \x000f\x0002P\x001d\x0004¥fñD\x0016Û¨fº¯\x0019¢ãn³ÒhQg4Ç\x0015dM|ßÓç¤\x000f\x001bVZ\x0011GÔE\x001cÕ`<x\x001eì\x001aÚå`G\x001b"dÄöÄ\x001f\x0015d¾ð\x001ePÆýe\x00183\x000bÒT	C&\x0013¨¤K ,wòz¨Nô	êÇP.\x001b6Ar\x0012Í©ÐL\x0019K-'VDJÛ*£1Ö¡Y#wAûYÁ\x0016\x0012û£¯-²\x000eã^±Í%y?/g`ú»ÏaÄ\x001d`y~Mup\x001bÐö\x0012<«Ëð"*÷54<L\x0003uñ\x0016j.ÅÀ\x0016çaÍ\x000f×ûíZ~²"i\x001byRäíP\x0001×y]\x0013ä#\x0017\x0006ÍvgµÏ'OoýL^z\x0002óÀ`ÌXzë¥!\x0014(4\x0013¯½>yzu~|îb'$ l.A\x000b<nÍ[G%3>\x0019<0Eñ\x001fÑ@\x000b*4¼«ï%H\x001eQ?Úé{b»\x001eÍ\x0006ù=îb(Ô;Lj\x001eÐ\x0015\x000f=×hwæ
f9`^e4è±Òg\x0014°\x000c$:ÁAQvfÃR³E|OüQc´h¨KÕá;Q¿ºò	óõn6!~«es\x0002ðÊÖ´\x0015l0¤ËçiÁ>9ïË [¾lS¯Û¶¨ÎnÐ%\x000fë^¤Ô q×P{SsÉýéu\x001bÔàlÔF\x0006	ÐdÔä\x0018!Ï\x0006Ñ@¢\x001aô0 °\x0000Qe£\x0017Ó\x001cßÀ\x0016¬XjÁ*\x001a§È.ÚBçTeËC±&mØ\x0006Ó<\x0014Ù
XÅ2Ö34Ñ6ð|Re\x001b7¸\x000fß\x0014tß\x0014ËhónLp/°Æ@E¥bØÀä\x0016Mº-
\x000cú}GÇaõÀ§ÛÇ¹KÉÅlN²9\x0015³pJÒ9Ðë·o5Ç\x001dMTL«ÑdðtÑ\x0007*DÙÌÜ±æ³Í,~Xü\x00166éÝÎ»Õ(5\x0006\x0013\x000f5ó%\x0006ò %oÙ	S¹<DËÊ/\x001a k=·l¡OÊqx=ÌÖ\x0007mvïP°ÊSÁ%V:i\x0013×JOã«?\x001fÓkæ\x001e¨ÂEi¸ö³\x0006®D~;¨ÉÞP\x000b,mr\.Ø©Ò Âe«\x000bxk|Ô
WÏ\x0000:Þttzèç.\x0001\x0017³¹=6\x0013ñ.gðÍ6²x$ÏÑËÙlØ©5 \x0012
S\x0014#µ¹Iª³«¿¿×H)RNñçH)­³_n\x001dS\x001dÛDv.þô\x000bVc|¸9yvóño³æ,Ðe\x00031Ï)$~{4Uõ¸xþ
\x000b0O.ÏO¿øýC\vr±±B\x001e4`,ëçq(']\x0006âÄ"\x0002^Ðh¹¬°\x0017þ¸\x000b»dxN®ãª\x0000tÉìB¦Ç\x0016,H° úg*`@O\x0008!ZÚ¢X¹°\x001aÌ\x0015\x0001?*À\x001c{ÅG´HK\x000c\x0002mO\x000f°~yù)½êSÖ\x0013*OðÝn"¿¹ø°îK=u\x0016\x000c´&ú\x0010ÿóÿuþó÷ML/\x0018Ýv1<+ðâîÍÞ¬\'çÏ./^\x001f+#2{\x0012-\x0008æt`*ìéµÄ\x0015\x0012K\x001bË -Wr\x0005\x001dW`]Ælù¶\x001aÅ\x000fÝd°8\x0005:0\x00181¤É¤TÁ\x001cë¡\x001bñâ¨\x0005ËS°¬\x0003KÔpäRý£M\x00046D,¸îÐ)XÑál0Öæ<
L,¹\x0013ý%6
ünÊñ20c0^ì\x0016³\x0014\x0001A\x001b~@\x0016ÛÀ%}ÊY`vgÒÐ\x0003\x0002úÑsVó/y}ûÓÍ/\x0007±§°*Wa¥\x0015ËÒ1æâ\x000fÍ¢ÌbyAæud\x0011«3Y«¥¦"\x000cÙ-Rx1«rc8«¿dÄ\x000efÉ`ËÚ\x0007\x0001\x0006:0®ñ¯	§\x0013l¬ýto.º,	²¤s\x0017r¦¦\x001béc\x000eµýÙÓz2á`­ÊÃZh¨ £!Ýf|iÅä>5ð°Véb#\x0005M\x0017ÉÒN\x0017kË1îu:\x001f[cþ@_\x0013eÎÈûÇÂë\x000cîÍöÖ	/ët^¶\x0015ÉÛFM\x001aî\x000cç\x0001¬'!ÎÑZÏN#d\x0016*©\x0019kdÁ\x0016?ëu:?[3KÖÉ4\x000e¦Ì×\x00196¸Y'Ü¬Ó¹Ù¦NÔ¸ÌÎKd³eñ\x000b'ëtNÖ\x0019¼ºh\5cÊ\x0014]\x000f\x0005ïlïMh× Ö©¢Xë8c,<Õ§ZÌò¶4[E'Ü¿SºÖy®k,àrë«¿°¸!¾vÂý;ûw,Ææb=ÌI:²ð|TÂöàb0áýÎû{CµÓmù³÷/=)GÙÑxÑ\x000b×ïu®\x001f\x0005þèq'Â8È\x000b?[§\x00147¬1/\¿×¹~oy\x0016^¬y¦wD\x0006l/{äK\x001e·pû^çö}üÕ¨°?#\x001fH²ïRm/á÷½Òïÿ3÷¤\x0017ßë\x001c¿O§<($ód¹Ì<×`h\x000bpý^çú¡i¦vg\x0011Xh¶\x001e\x0008½;r(\x001d_cÂï{ß\x000f®{b{oêæâ'ô´Åyáô½ÎéûÀ\x0007eLZzÑU°µrØp{áô½ÎéÝë9NU!eöa>n0Y\x0010>,(}\x0018kDTo\x0001|Ýcç*1n\x0008_ð\x0016Aç-B¢\x0007àXI\x0016\x0019Þ×Q½ATFuGÿ áQ®ÞNN^¼ÿÓ\x0011qzðsËsA­Ò.Y\x00108p­Ï\­ÞçÇå(Z¹{\x0014T!*¨ÀS	¡Å{*p,:Å²«\x001aYH$URP\x0019ü`ª#kT\x001e\x0006sums\x000b\x001dëØ÷\x000bY2e\x0005Ï\x0014{5ÕÜ_B
\x000cK<×ç±ÈT`\x0004\x0016¯bYEù\x0001ãò\x000f\x0008%^J`ñjÇrO\x000cu\x0012¥æ\x001eR¤åTX#ÕU%PdF\x0015âSÂòa®t|\x0011V*\x0002+\x0015\x0005\x0016®v\x0012\x000bñCl Å¦],$µß°þtXfùÒ,û\x0010ù%+>\x0001\x0001cÁÙv°eX\x0019$V^n®2\x001d;6\x0018/!JhR\x000c³}·¸=ÿ¾\x000b%û0;[ÏÃÓ¾¸\x000b¢Ê ¤ò{§_þ\x0011\x0001E»»µLkf!\x0007êfJ\x001efÛÓqÁ\x001e\x0017,çÞSjf\x001dmsÁQV
i®üt±â\x000bÝML+\x001eô_nælÝ< +Roõ\x0014ó½Ý\x000fÑù\x001eÙì¬µi·å'7\x001f>Üüùî°\x001e\x0004\x0016ÌPG_õ\x000f¼ö-_4ÕhÕÍ<Ç?9¿¼<ÿþí1Ñ
"\x0003A\x0006*2K\x0013M}ÊC\x0012Ç¥wïl¦G¶\x000cÍ@g³Ä<8m&2Y\x0019dy¦èc1Y\x0012dIEVèYÒã$\x0010Ú¶p£a¶n¦T`9øIõ1ãö¯³d²Â]ú\x0015wÝÇ4 «\x0018°x§þ3U¶+_½¿¹½½ùòå\x0008K§\\x001dî¸\x0012ëÙ"ÔOkbÏ*QÛ¯.Î¯®Îß¼y\x0018nª\x000c\x0005-åVÑe\x001eY\x0012\x000c\x0017ü#\x001d] ¸
XA\x0005]VÒa\x001f|\x0019=\x001c$\x000ba}¢
\x0012¡N¨.AW]ú:>­ÝwoVº·ww'Wï?}8<0BpôR\x000f\x0011Å®[J\x000c+\x001a8m@ç\x001dñíÛ«Ç¦\x0012\x0012Ú$Ca;£Bó<Ñ\x0004bonB¶ºæXÉ3Ca9[\x0012fK:³yðÛÄ/i|\x0008\x000biáh\x0019G²\x001c-\x000b´¬C«{¦\x001e\x0000
2\x0014BÛ'O#6=[\x0011lEÉ\x0016ù"ÏÄfò`Ûfw/pÖºR5;ÁP]\x0014\x0000;Ór+,ûîk¨»
N\x0004o\x0004¿Ò0RMYCì®"²\x001e¯\x0017}W*Ä(K~°´Ûv7÷ë?zÕîkôsÇ&ÄS\x0012 \x000f<\x0015¦n\x0013v$9[{ßÉ½>yNîXlId È@E\x0016
\x0013·~xÅyz!>l@sÂhNg4ðC\x0003¿OJjh¬ûóÌ©º\x0018\x000c\x0004\x0018¨Àp@\x0017`os]D9\x0002\x0018Ï6³[l\x0016\x0005ZüªÐÄJº\x0006¦oÏºÐ¸a¢.´ÄS}\x0012ÌÄ!É +_Ñ\x001e°{Cé9l\x001a³P´Ð\x0010ØjÓ2\x00165\x0019ì9\x000eÕ°"µ\x001f¥¬ò8Ó\x0004\x0006ZÞÀ&Õ­5\x001d
ò¬\x0001H$Ñ\x0018£/ZÌT\x0007JÍ&\x0017Õ¯6w«-ðj{Åæ&\x0013*Ãõ_\x0011\x001aH4Ý\x0017M®q££¹O¾Ñ"°a¥9y|:ÝùiR¡×ó­tW¡²it÷Ø\x000e¼[t0'Ání&Ñ¹1Q=\x0006_ÍÂ*ké<j2NÓù\x000f×'O?Ý¾»¹}ì­Î\x000c\x0011`x\x000cAýkYÄ"ú¹¬ïòìäéË«oÏ¯.=%\x0012 \x0002:5`¤s´	\x0008E\x0006L¬\x001f´ÎOé¼Ýâ¹$ÚzÃÁÑ­a
\x0018V|_êä¸¦Äz;ôzÜÜ\x000ePôÒ5Hü³&
¡+áÝt¿\x0006[O\x000cñ\x00118ÿãîúËÍ­D¥ß}uVõûVõ+¬ú¿°»Ã\x000f÷LúuÙÓØ=7Yÿ8*-><½þøîýc#¿QÂ.îêlÅ)4\x0006\x0013§ÃÞ/{}}òôìÅ·\x0017ÇÇ\x0013¢9\x0015Zb¥t£{j\x001dÁµù^Ý
ÍOÑ¼
-¶P´£\x0019ºø\x0007cS\x001aV»W9£B\x000bS´ CËôäÛ¬fy\zÜYí^a¢

¦h C3\x0014Ë»ävft²øûµÌ*´8E*4ì%Þ}ÐÀS®G\x001f¿_Î©BKS´¤³\x001f\x0003ÔñÇ\x0017ºZÏÎßkÌXÖ\x0006ÎLFRk\x001aáË°êÚ>^¿¿=þ2ºÕ\x0000ëaéÖß\x000e=\x001d1/Ãª[{qvquÔ­u²"È\x000c2Nã2­
Æ¥1ÂÌÃÜb°iÿCjý\x000f
0Ï}fà\x0013w=[|@ ¥-&\x0016ô§VÐ¯ ³Üò\x000f]x¶q	8N\x0004ÜB\x0016\x0005YÔamb\x0019d$RmâXf¢\x001aPM6\x0011#À\x001eFCf8DndÝÙ\x0006\x0013\x001dd[l¬ ³*2Ãí\àHT-ñ\x001e\x0017Ålu5X\x0016Ë,kËeæhFch#§,®'³F|LüQ\x0005ì5\x0012­3_
¿\x0012Æ4÷6²\x001c
$Êjq4'¡Õ,£í¾çÌÒb2'æTF\x0003·S\x001d'Mc?ãìÍb2/É¼¬é>\x000eWk,îÐ¦=Ðj´ Ñ
Í²®OCs$:äÇ¹Yf|yIæUFK¬CWÿóþ)Ç©æ-c\x0005\x00154X>îNÍDö\x0002¶\x001aLîÌ ÚÖb|\x0011I¹WãâÝ\x001a\x0005ëÑ@®2Ð¬2[,éÔMÊ
+>Âþ,¯ò´5$¡\x0006Î%\x0011[!ýË?\x001fsHºlÁ÷Tj\x001d\x001f\x0012oÖ\x001d\x0018>tòòûÉ¦\x0013âÜ7{\x0003â\x001e Ã®F*\x0001-\x0006¸À¿QÕóñ\ÇÉj\x0010/ßPë/ø
õfAÙ\x0014 h«¥+¤BZ!ð0zhÞ{¡y¸f 

¨º\x0015\x0019*àôÔVÿ9¤bºw¹i²ì£ÿfWíó0S\x0004,
oLØÍÕ¡\x0002ç\x0015êþ[Öbª(¨¢Ê\x0016.®lÝoT)Kµ[%fïia)Ý[SE\x0015J )º¨Æ¤\x0004oY].
ñ\x0012%XN<M\x000fö8³·V\x0006Y«¸.ö{\x001d±ä'´o\x0018Bæ!>¸²ú7tÀjwQ;+©²¤Ê:ª\x001e~ùz<Sw8bñ7,q53\x0002\x000b\\x0015I¯Ç·¦uGX«Ýý»ÅXNb9
VâÉ=x\x0003\x0015\x00187b
>¬Æò\x0012Ë+°jàL³p²º¡µ\x0015Fíu¸_O±\x0018+H¬ Á²è\x0014\x001a
<\x000b\x0017¥ô	ËÃj_êäw%_cÁþh\x0016#«UcñQXü\x0006(PË,Râ#ÞQÐ\x0013\x0001
õdZåÀòF\x0015\x001c\x000fÃÁðÕun\x001c÷«\x0017cÉÇ+N\x001e\x001f,){Ð@'eMÂ\x001aÎß«T[L%\x000f\x001e¯8xðÒ©Po¬÷ÙÔt`8-³úàñr½{ÍzÇuZZ&PòScz\x0006XÏîÕÇtÞ!(¼C+ù¦ó\x0010gR÷cÚ&ÏK+¸Õ+>ìÅ¤ \x0014¯äh¦#¾8º,ä·D>¦ÄJÒZIa­dè2¢z
WÂVá¶ÖûR0{Ñ²\x0002\x000bY(0-'\x0013Z +¯ìzk\[ Y[5IyÓ¼iä))l°Ö^n¡H.\x0010Ã\x0007ÏR<5ÖÖú\x0019äÚ\x0002ÍÚBåA7°Rä\x0006)7°ÖìD
oÓ·åú7¯nùÕëZ¡ô«»÷_\x000e?[¡j
ã±5.sáÇ>7\x0015ê}uyö´I¿z{ñæØ\x0015A¹)S@e\x0012é­Pý)CMizÁ¥e
S¦°É¦¡ïgwJ¬R:ÍWµH0E\x0002\x0005Rd\x0001¥ÔïC:\x0012ìÌ\x0014ÖCÅ)TTA\x0001I9ØAE\x0016¶qÓ^æÅP)í­ò¾<´|÷éãÛOwøD{pÿÕ¬ß
"¾n\x0014j\x001bö<¢äÛÉï^¾xsõò->Ò>7´\x0010\x000ft|¹\x0006\x0010d¹lFËi2¬yPL\x00114ÖðM2²Ê7}?XÆ\x0017Y\x000e7ÕcæìÄñr\x001fÛø¼°WÛÏäy\x0018y\x001câXsã\x001a:\x0010t ¤Ke¼ÖcqX/Ò\x0005{PÓðEÁ\x0017µ|uKxÞ·W_a½`¶Ùoú\x0012ö^b\x0016\x0001bç3Kyyªa
5c¥<×,»\x000c0æ=ïR¿
¡\x0015îúçæô^ÿòþÈyU(gu2~±ÆÞôÓ"×Ù³æô½º8B\x0015Ú¿LÛ`ò\¦7øOÞüáæöh\x001f{È}ÀB((ÿÝcâ{\x001fo1Y\{ò×'o~w~u´½Ó\x0015tø£®ú^ÖY
%gÚ\x0014XÖ\x0016\x0008/NûzVà9çÆCA\x0007×ñ|¤\x0006A$-ç¦ä
<ùmA÷m£±ÚA\x0002\x000eUg1dC}xõßí¦\x001båÇÚçEìxèñ¸úú.pVÍÜ\x001bÍr¼,ñ²ví\x0005B¶üìV×^p×îè×àÕÂö`³{ßÂä©2Æ÷×\x001fn>þtøy«ÝãQËáT\x0001çnÙ1c'ß]¿xzìá­\x0015\x0001VT`>Ó»MË\x001cHLº`Í\x0011u(KÉ¦âZ.ík=ÚÀÄ6Âº\x0008¹\x0005©Ø83g1\x001a\x0004õr´êzûÑ\x0015\x001dJýôî(\x0013ziJHs\x0012,Ñ@¢
ÍÑÑ\x0015qØX¯ó©{\x0003¸9ÊÏÉ<Hf î¨õÕÊOw·?\x001dÓ­Àe¨ÑÙ¦®Óo¯\x001eõ\x001dDæ¦dNG\x001cm\x0002\x0017±à¡G">\x00070yS±ù)W²\x0001O`ÀÉµ}¸ieË\x001c%\x00017+ØÂ-(Ù
O\x0010\x0006øÑ×\x00177\x000cçZ\x0001\x0014l0e\x0003\x0015[4+·¢\x0019Õñ¾Ø\Ùf·8eJ6µG­@$':H+\x001bK8'\x001bïÝþ©ØÒ-)Ù\x001b\x0013\x0000\x001c]Õ Ý2\x0017¯ùv¼¥lyÊuë­\x0001B\x001al\x0006xZg6ó-KÙÊ­èØòðnèNh½ùÂ³\x000f¹\x0019¨a
¿/Pð ëM§¤\x001bk¹££z^à}\x001aì|£ñR6y*h\x0005Ã#1±Újy=sÁMÁÁ*O\x0010Ép
§¨\x001e\x000c;\x0011kçû?²Á*O\x0006¿««Þú½g¹õda¥÷u{NXsFÝM¯ÞÿrD¤Ã¤ÃÞÛ\x0007Ì\x0004[\x0008îøò¹¸ýa\x0016¯.^\x001dSç`\x00147EqËP<¹\x001e\x0005«¸À\x0013CÍþð$~JâD®ÔÍcdtEÉb}^\x0012¦(a\x0019Êpî8(ð÷á¦³bÂ*\x0012À"\x0012Ô¯æ¹?"è¬±;ÞÞ®BS¸Ô(ÔLÐ\x0006ýd6Ê@që\x0016m¢¤eVq<\x00145L¨ÀÁ;~ }ýår@Ú8ò#/3I\x001ewõëðØ/oÆÍëþ\x0018&)S²Ì$­\x0005º$q\x0017~|{\x0013È\x0016dr¢k3Kmè
«þÑÜ³IÚo\f\x0013+Ýì2?£²èíªz\x0017O.ÅûÉ´/½EøY»ÐÑf~ÁWèÙ.Ü''Di\x0014,Â½Ùþ­ìf
äÓÈ^ÅaJûÓ\x000e\x0016²\x0008\x0007g\x0017z8ËÂ(8Êsm<¿þäèWí!+<]æâ\x001b¹\x0019(nc·?ka!p-voÁû/v·\x0005híÆ±^Öy[+\]è["\x000f\x0011\x000c<Ä¾~¡Ý\x0018)·ê\x000b9±£ÝÂ\x001d\x001dÇy\x0018Ì¨÷Ü\x0003UÓu,"^qË\x0002b8`IÞYQÁVæýù\x0004\x000bYÄ.rËvQ\x0019\x0011%
|sÇ\x0002· fog\x0017î\x0001ïo÷K+¬\x0011XMXàöÓÝßªZf¼.¢Â0r{àX}6ÂL¾Òt\x0005®^¾ý×ã²D8y×­BXm!"¾§Q\x0016Ù\x0003ñwåø53Ý
é\x0005¤×C\x0016\x0014å "(;ª0©â\x0002»ûEPJH+-iW²\x0004 üÔã\x0018\x0011V¾Ï4­£Ä\x000eé],¦¦´kl\x0019X~ UçÒ[yæ·òJé6S\x0006I\x0019VPÖ\ßÅQéI¹~Æ!W½bÊÌÊÕ.¤L°·wj2ád\x0017Ò¢½ãlÂN¶7ö©Hþ¤\x0013I\x00019mMÐÛe%x{°xóð5öEÌ7Li0­Ä´+Y·£ÚÞèy@\x0003`ÌÍAB\x0015%öæKß\x001eú\x0007¯\x001b«\x001eÝT\x001b`%%HJXñÅM¡©\x001e\x0007fEu16OI¯ÃÎoÇÝSV`ZÏÝiÙÁdR\x0008k »0÷Æ®Â\x0016WL¿×\x0005¹\x0008\x0013Ç(öÙÞÚi\x001e@¤QG\x0005£ÍIb¦\x0015>tA
lmå[lÔìÅÎ\x0016,¨(A\x001a\x0013Ö\x0018sô÷\x0004L{H¼ÐÅRÁäÍÆÖV fY	t\x001bð­\x0006\x001a\x0014\x000bLY`Ë\x00062å\x0007Q$ÐT\x0002'ûç\x000e	?#ìóÛ\x000f×\x001fß\x001d\x000ez-Ï\x0010\x000f®°Îk(¹Ï\x0012¬f
eÆoò5\x0002??¿º<{ñíC¬S÷^Y{WÀVSö<\x0017gP4\x000c]½Áb\x0003ávX?©«°øã\x001aXÏªÃØ¦}ÊÒVêB;ô¬Y\x0018¶5¬`\x0005>:±zkêc\x0019Vhê®
{+våMüSä¨\x0016\x0017L
T\x001b\x0004~®.M
;m"¨°\x0000ë`}äýU#\x0011zÖÁËgª\x0014¨ïñ\x0018° a×,Ùz\x0002X*èÀAItS^cf6,^mg-^°â+X±.ÆR}\x001dª´÷´3QCe1rÊô\x001aØhöîã¢ôóã³Ùë?ýøéîpX
D(>ÉBMí¨v\x0007°IoæÙìÉÙó'/ß\x001e{6ëlÓNg3iV_Â\x0016\x0012÷I@V¾ÛØHÔ¢²8+%¿-\x000b¶¬cÃø#\x0011\x001bÇuuM³6À,é\x00026ëZ±îd&Ëm&\x0005Þ\x000e}_ÿê_NÞýÏþ×ÅÇw;â-ÇäõFkECãd½ðß_¼xzþâÍÉ·'\x0017/¾ýýxÓ\x001a»ÜkìTx¨Cx8²îè6¸´[ÇM|Â|Em>»ÖïBkPyJ\x0011\x0007÷\x0014´?XVG7UI¯tÖªÍ\x0007T8\x001c\x001fÉo¨%{
X»
\x0010$ Ú~cGSr]vÝ\x0016\x0004÷V÷\x0000\x000fhEw:/Íçõæû'm\x000eýÞ{ZõùVøß]ß}©ÿöÝíÍßÞ½¿9"j\x001d½á7aH\x0016(\x000f@Óg«)í¼ÚöïÎÞ¾©ÿöÝÕùï¿½8?®oÝy³àÍkyûÜÆëRk\x0008I3,ÀÙ!\x0016jÞ©¨G\x0016¢\x001e:à`\x001c5ZW`®\x0002p<V\x0008ü|m\x001eØË\x0005á×Z8\x0014¬kiÀ=±
[ØÀìy¨_\x0011Ö\x0008iä¾§ÚÈºQ¨2\x0007\x0012y\x0013v
|ß,ÑR¸÷Qâ®Iôyu&'¯o~¾{ÿñ #ª{zä)\x0017¯µáf\x001a ]==y}þìíÅc¥Mí<\x0004êÕ\x0014£Ù÷s3åÙP~õæöØB³yÛÑXy?ò~*÷4\x0001^7#=G\x0005Öó«£ÅW{'&\x0012\x0016Ð\x0012Ö`¼×Hà\x0000U\x0012\x000f\x0007Ø¤|OÒD	8Ýõ\x0015p·ë\x0017\x0013VÿÔeb[ÞÛÇÅG\x001f9ÒMùÞÄ\x0007-¢^*d}ð\x0003^zD2"I?TÄ¸\x00191hz%\x0006~¥j\x0003£{¾?t¹§·°\x0018Ñú"·qý\x0005nã]æõüîóõíä\x0010Æ,ØGe'ö{÷]\£êÙëùÛ×gWGò,\x0006sS0§\x0001³q(ÍÌwê5?\x001cS¬ËlÚº\x0014ÌOÁ¼\x0006,gRQ³oTiÖp®d¦Kh9X¯Èbq
\x0016¿\x0002°úoû/\x000e~ïÅáóÉÓOw÷&Ôæ³\x0004\x001b
\x0017Ò\x0003º{´ÞÎ÷ó=}ùö¨ë 4h A«iJ×aðx;ÞËB]øæÞÏÝá.EóVXÍ[ÕÀQÅVÀÑul5Ï·õvþ¶~)ZhQVè\x0002\x0004ç4³n\x0012\x0004Ký£6û¹§¸¥hY¢e\x0015Z\x000cüÆÑÄZ\x0003¡Ñ\x0004BãL{\x0017^6ÕI¤%£@K$\x0015|ý¶>(¿kxãçÛF$\x0003\x0015Y²|íSáR\x0019n/½KsO.KÑäR\x0003ÝRû§nPK
KÇNU´*%\x0019mî~z1tkûMÊ¿¥Õ¢tkQçÖ\x0012_a\x0010¹(\x0016Ï\x0008êFåú
hr­EåZ\x0003RÚ\x0008`â)í\x0002ÈÜJ²\x0005æ]Ehs\x0014e9ÿóÿuþËûø4z8_Í-\x0010Â|5\x0014ÏÃUC¡ ¼þå³U9'ç¯.^à»èÓ3>¶ËS-a¤\x0011«
xOHÀ\x0003jmi®ZF\x0018÷'ÅÉÄ³'7×w'¯ß\x001fySÆÃ´\x0017e \x000cu¯\x000c`-ÝB¸_
øäüìíÉë£ÉqÌY9[Bé²¾b\x00056O<â,ÌIê-ÆòS,¯Àª.fGµÖkCÚ-NÇòvFt1Vb\x0005
\x0016?»´HµT`¨Ç\x0000?â*k¥\x0016yO\x0004Æêa&WaXµðìú°x¬\x001b>c\x0003\x0006míÂ¡³¹G,XxvvTäÜ½\x000b\x0006gú\x0005Ã$+¸>ìÏr´ÔýfôZ
GByþIòùÙÑ¦3Dr`£"9ù¾{\x000c	I{oh\x0008;¸\<E^´!¨ ¼ò\x001a¨ÐCÀ\x0019
£(F¥\x001büÀj&kó^jnóNíõ§_ÿßO×\x001dã,b2§Ö³æ\x0019·\x000cæé$¨~é÷úåÅËcÏ'á\x0007QÚ]ñ¼~SÆ/7·7Ç¦-At\x0007±6^¹Crä\x0019¹¯jÙ´;ê	ùæüêüøÈ%¢\x0004A	+(±¼×¯ZÜ\x000f\x001ax¼K©Ût¶VE9\x0010¯!f\x0005¥§«ÝêN.ZðÔYj\x00023ûR»Òä}ß÷|ÇÍÉ³\x0007\x001f£jæw²kÓ!ÀMU¹9yvþâèKTÃJ\x0012+)°\x0002Tõ©®@\x00120ñÄ­\x000e[åÀÂ\x001fcñ0V@\x000b\x000b\x00187ÊÏÃ\ì¸\x000ckâØò·}\x0008Ë¡Ù2O<êÍK-?^åÀòNsqièc\x001ewUa7òsýÒ
*(¨êG¤÷ MÛTx\x0018\x000c?\x000e×-1[R¾\x0004\x000bXZøãR¬à?êÆ~»Âif80sc\x0011Ü Ø>;jâóXPØW\x0016jýt(3_»\x0004*\x0006ñ	cXþ	1¼
}.ô\x0012læ\x0017ô |ª\x0012+I¬´\x001c\x000b;±\x001aS/¿kL!ñ÷sóÕõK\VI±¬ðõ³k]yÔ\x001bgIv?Õ|cÂÂ=(iû>Ä_ý¦[ÑZØ;¹±gMWwï?®È!²6½G@à\x001cË\x0004Ä@JÕÅÖÿöÙrÏ«·\x0017¯_×dä!º<\x000eßd\x000b\x001a<gAµEÿ]:¯\x0002ü\x000c\x0016ý|5êb¼ ñ\x0016/²\x001fä\x001aóô;íÇÕi1øÙg¥xúHÄÛ«|\x0018/pù\x0017\x0014Ãã'qÖ=¶Ä\x0014g\x000b\x0005\zE·öj\x000c\x0011IS\x001eP\x00171Ô\x001a/½$Ê,ÔtvÒtíg\x0015åûíÖAÆrk£\x000c$Ùù7»Å|~Ï+ù\x000cPjåk\x0015°/\x0004~ÅvqæÕBÁöøÒWÅ{wêyÿNÝò\x0002J,Åv´GÀÒGöTA^!ço\x0015\x0014[äëýMr­2£7\ÖÓÓ
í\x0014yX³Ò53Ý»)ªÉ©\x000c\x0003>\·äïðUCpä]25ì2\x0000Ë\x0011Ûp¨¹\x0005ó¾Ø&Èf\x00014p­cºÛa\x0008w¥!,FÆ+Ølo,G\x0002w"sÆ|÷áý/Gjµð>¾Ï­\x0000#è\x000cð'\x0005fKøÞ¼½¼xu<ß\x0008\x001cìçò\x000f\x00057§rH\x001fÈ)×ïi«õìl\x0019Ùl¦ë\x001c\x0019xTî=h|9Âf1\x001aèVC¡§^\x0005õL£Ë^Þ<H6uÇH&ÝñÃh5}ð}flêw\\x000e\x0002\x0007*9\x001ez<[Æ&"Pæ\x0013!èoe\x000b?ü8\x0005ÄÂ\x001f\x0015t~|Ûâ"·òØRØ\x0011[{è
þ8]Þ\x0015Ë0ü×ÕXB=-
í\x0014X¢;¥Hg\x001aÄ03j\]\x001cºßRAÈìk3]\x001fÖ|¸°rJ\x000ba:\x0015j\x001b³\x0017Ì~5s»ò¤áÈ"
(.?áÑ`\x000e\x001bì\x000c§T5udeÇEÃ.=ÚÊ\x0000A\x000c\x001b
©Õ\x0001J®\x0014²rv0ÏsV2[¿'.,z	j\x0000tyóçë\x0007¥X ÙBØÖqïd\x0000G7 )d¿×QCËóïÏ^\x001cQ!¤"Êr¤è©\x0002ßÚúÍ#]%g\x0012+M!¨g2^ú©ú]mõ«ú!ooN¾½ûÓõßo>\x001cü ¦æÈ=\x001ak¹Uá\x000b\x0016Bô÷¦¼ªï
	ýëùåÃ|~Êçµ|4X#£Ø\x0010ëûd\x000b÷^ÂÕ¿_ÛÉ\x0012\x0013Ë³mYØòé§_®?\x001cSr÷\x0007Ô#1²\x0000\x0011\x0018 ðÂ\x0001Ìj÷>}ùêìò¸Ð|Ç4Y.N_\x0017p\x001a\ïû\x00086F 6
KA£\x000b÷gÝªð¢ÀJ<_\x0002é´\x0001]r£Z
ÕlMö6â\x001bµ\x001f\x0017\x0005ëÈzgBÈqàmû¶I\x0018/i\x0017¹éºÍ»$\x0005Ó¨µÒÅÙ@ñmwY(}ÝkÝês@2 °ðjÀ0\x0008g_÷\x0016\x0010æ\x0016>N¹jð(E_ÝÝÜ¾ÿÓ7·%»\x0002Þw\x0005,O')³h¹É¾\x0013³CÆ½=¿ºxþäüêXCÌA\x0011\x00151gP"1­\x001a°n¸ë8ª'Â®øµÖîM¶ª¿¹¯?½?ò@ïLÇP\x001eç\x000buä$ÑïÏ1À\x0003Ïó\x0004ã§0~)\x000crô|tc
Nr,S¦-.: \x0002ÁR SfÒ±\x0006®ÓÁ2a!;31h\x0019P\x0002¥Å\x000b( o_ÕéX´¯~15ÔÉÉUPú&ï\x0015ÝýtýÓûÃu'8Âf?EH·átu`p\x001cûl
wöôìéÅÑ7Ù·7©å7Ä\x000bûÕ|Á±t5]Ý½ÿx,õ5©\x0019ºXO©ÈÒc Õ¾ú.2]½½xq|¶Í~)_p,a½\x0008	x\Äq\x000bÌÄ¦)ç´\x001aÊÉM\x0001bo~\\x000c3²hú^1ê©ìÀ¦	KÁ¬ëÚJ\x001dÓ\x0006ÇQBðúËõ»#õrÞÐ;Ë\x000b§+\x0013oÈ÷ûØk>ðúÍÙ·G\x000b÷¯-"È\x001e­'·7?\x001fi ©Ö1¥`­\x0004y	¼ÿìYJÍSfo¶\?{ fÏX\x0018üx\x0005O?}úåæöúËû?\x001f¶\x001bª·tOoK\x001e]¥°È²sÁM\x0018éåËWçWgo.¾?Z\x0008iö£n³k	ÕpæD½xÎÔO\x001dèD²|D:s>í
NaOXcO;tÖ
vÒ£/µt\x000epZÓØv-\x0006õ\x0017ß$Ñb@yà15¬\x0010YçÐy\x0017¸:\x0011Ë:dïµ¡T\x0010µ°~º~wýùËí\x0011@ñ,Dòµ~\x0019'©DÎ\x0013\x0006çqÌ#Ñd;û§j\x0000©©\x0001ì.qZyúÅá)ýéÔ\x000fÉ\x0016:ËLÙÝÒç1­8ýâØ\x0008Cë÷F\x0018â\x00009Yãéß~¹ýõ\x001f;W­·<tÌ$'#\x000eXìdÕ\x0017Îç¿õÀ5Ò~\x0001ªÏ{\x0003\x001e$ÃyÔÝ\x001d\x0013\x000f©B!.B;0ºb)Z¢E\x001da!æ6\x0018 \x0005®?ÌVSõ\x0010)XÜ9\x0015þ,aFøóò×ÿóñðb\x0003\x001fùá\x0000{)\x0000º©ñ³iKõ+/_\x001c\x0015xí"\x0008»Fê°6ùÙíõÇ
V\x000fß#\x0001Jk!lo{iÔ¨× U´Óôìxvuö¢\x0012Õ£wç=ø\x000f;öp\x0011wÞØRäÝêå¯ÿýÓ\x001f\x0014Á\x00129yÁÚë>K18\x0004b2\x0007.T/Ï«á^\x001f¦«YÑ~~\x0017ÄlÑC'¼\x001c$íXÚ\x0008­~;8Æ<i×û/º\x000b\x001esS8§Cá|ÊúãËAÃI_6Ó\x0016
\x0005ÛµiÂÎpg¸O«á.?}Á÷?¡Í\x0007Ü¡5}ÿ|¬%\x001f
ÎêÅx8ãÎX\x0011uEúÁ'«/ßàóûs³¹ÄZSø×­-ÿ\x0010éÕj\x0018\x000f\x0003gÍOpH\x0003þøÍåþ­þ¯ÿ}\ÑÆö«.\x0014e¦ÑÙ¾Î\x0015S\x0002/g/óç\x0019á\x001fÿòïÿnÉhÅ¶Sÿ|7¾Üæ
ß\^ã\x0014¡ºOêß&\x0015L\x0017v÷Å»L#	ª¯õ½÷=úz  o«îâõË·u\x0017ôÝúýÙ¡û^QWû
0ê/¿\x0015F¸Mö/_ÈÍwç^ÿWï¼9ÂÑ¤ÿq\x0010}å¨>¯7EÕ\x0000äöq
µ¦\x001dGýÓÕÅCî|\x00111Ænÿ²\x0004\x0003gãæå\x001a¾c@\x0000Â°íre9ÆËô\x001fï'KôûºÍ¯:ÂÐî\x000b»)\x001c\x0016*¡PIMFíÑáÖ\x0016\x000cß×­}öt	B_¿%\x0002¾øàÿýï3x÷ïøå§É¸lj¹?¾\x001eBje\x0000(<\l«u\x0016\x001aC(Öï/§W/\x000f¶Z
þ1~kúÿé#÷1½ûånòEþåîúöK=ôZùëz¶ÜöCLàJ\x001f[\x000b ±!\x0010TñAî×y{võ¦*-ÍüÝY=c®\x000e_|\x0008Äþ¹¾>Ä¿þÇû÷¿ÏYûþðþó1ÄPó´¦[[\x0011kZÞË¿,?¦­V£kGìýÅÏ./^/\x0002Ü³áW\x0002ø\x001fïþrÊì:¬Qÿõõ\x001b¿ÿtì\x0014`}\x0001S_MèÏQÎ¸ìé\x001bCÅûÆ5
8{R?ñÅËÃGê\x0004p\x0015~\x001dýóßýø\x0005qkÜ^¿?Ê\x0004ãÈw8q uÞ8S&b¥%\x0000;&Ü\x000cWg\x00170º~\x001bÛ£ùÛ\x001f'Ö8{ÿóÝÍõ/9ºÈéH\x0008S¿/³9E=ê/bÞ\x000eäìâÙÛó'/_\x001cLjëÊùÛÏé¯ibïÞÿ\×Í±0Ps\x0008@\x001eof\x0011#eÒÆ\x0010¨å×;ï.Õr\x0010áæý»¿þñs{®K\x000cÿ¯þ
¿½ùüåÓÝíÑ`\x000cVû$|çåðU2çìºâÄ©9\x0018VË\x001eÈv<\x001cü¶<ïnë
ûKÞüúOw\x001fÁÔC#µç£
\x000f6íIÄ¦(n7}d½`ysþòíÁÛ¶\x001a¤ýíÇ`~sÏn>¾»¾ýÓqã@8m§÷Évÿb¡¸\x0019£µyÿòìüÅ·gWÏ\x000fcýÿò¡üåw~}ý¾&Ìîú
ë\x00018\x001bpøiî[+ÆS¬²¨\x0016s¾×Ö­U?èþ^]`ÖüòíÅ¡-\x0001yßC-7wÿöñßæ,yyýãë
r{ô\x0013ã3%>áà)Â\x0015¾ÂÅYrPýep6yryVsP\x0001~?ÿõo£ö|óôúC¬úeÍ¯ÿøüþóë_\x00190dÔ\x0006Ê\x0018r³5w0~d\x000c\x0012ðéÙe¬ú½Íùë×oÎ^¼9l¾»òî§ôÇI~]ÿöï«×x j¶´/\ É5h.¼©÷÷éåEõ\x0018MõÇ¿þÑú?N\x001dØóO\x001f¿ÜÜ,\x000f§rê7Ïh¨zäAÿ¦UÔ\x000f<i¿|ñf¨É\x001c\x000f¦PgRÔñìÕÁË£eqKÝ	­\x001f\x0010ãXúóLõ+¶+GTÄµ{3?\x001câ5ÒÐx-\x0015ë\x0011¯wËÛ#Rß#àr¯Ú«À©_êW`ï\x001e	\x0018-¬´°·­·\x0003[lPiÀ\x001182t\x001f	XZ\x0018¾z\x000bGiá¸ÖÂÿ\x000bÀ½Áî±âC\x0005A¢OwÇ@Su\x000b¡gY±:±o¶ä\x000bÅ7ÕíGÂcv\x0005þâå¡æ®	!\x0008BÐ\x0012æ¦²Ð\x0008ÃbñF\x0008L"\x001b	³ ÌjÂzrÛíC6½Ì¡\x0012ÒË\x0019:,èc/&,°¨	\x001d~ÚF"/ÇäÂêgýFÂb§Åj	\x001d´âX$\x0004w\x001aºK)±
±Ìs\x0013¡_Ùª?3U!õ|ÚsÒ\x0018mOoÝ*ÎÍìv77¡\x0014º­\x000bX1ØÒÚ\x0013_×Å´0HÂ &Äª¾CÞ\x001fP\x0011k FiãVqY\x0012f5aý¶XÚ\x0015¶=ëbyeÂ\x0000\x001b\x0011=\x0008Ä=Y­\x0005=T}³ø\x001c»È««bò`¬ÛJ\x0018$aP\x001365ÅNH³Ñ+!ðÅq=_¶\x001a1I#&µ\x0011½kãÛ\x00101Ú.iU\x0011=¥¯Î§²ÑãT³2 %ewøÂÏ]<\x0019³é\x0008öÏ\x001d-ïÕÛö\x001a¿]VÑ
¿®>Ý}iuo®?^ßþ|w4·`°$£]`\x000bv»>*Þ[rÞ{÷W/ß¾i\x00055÷:»zööHbÁ|Ið¥¯¯\x0008¾¢åK¡É0bn¥óE¾ê.½¥s\x000ba´SBÜ|:B¼OÐô9ø\x001a D·\x0012zAèµØHÈ©{Jm\x001am(vIÔî¶¶ºa"l2½°À°a¿¶Pìøµí\x0013k\x0005û°)	{@\x00074|\x001b\x0015²c\x000bî\x001dÍ+\x0008$Ô0a»'B®­(¡¤±\x000c!nE,\x0012Qëm\x0010\x0005]a\x0013>!FÈÃÛÀFD'¼
þ¨EôdÅØ:©\x0010qâ\x0010ÝVD/\x0011µþ¦õÞï>tÁ¥âøÐ\x001bý
+M\x000eDõn)¶
"Dß­\x0008¦GCôF b·½r»\x0014NLKq\ð\x0001&òv´\x00151IÄ¤EÌÖ·\DÄ'ºNÈOc®Ûº[²$ÌjBçXr#\x000c½ïµ"Q5\x0003f«[Ìr·díniôC\x001f\x0002Ù\x0008\x0011óV¯åfÉÚÍÒF¶³Ë!\x0019å\x0008#Â´ñt¶u\x0015	Ä¬F,m|IûÎ®«Õ#âX!oýÎ%\x0008DÌt>rÍAÉãD FEDÜ{/R#NîH\x0010±Ýè\x0010[5/Õæä±\x0016S\x001c~ãvV"Z5"x¾/	è9\x001e÷\x0008-Ánô9ÎID§FÄ&Ú.Éõ3|w+¼]üÖ\x001díäñçÔÇ\x001fÊ!\x0006F$±![XÜ\x000f­\x0018¶~h/\x0011½\x001a1\x0007g+bì%:\x0015ÑñMNýÐ\x001bÓªÉ]C\x000cê\x000f7\x000eý:\x000c¥&3a¹2JÙ¶f-.H+\x0006µ\x0015kÃé3v®Ð\x001eè%­NG^8õ
I®Is$+&#\x0004\x001a")<ÊvòCGíÆ\x0011g@k\x0011ïÃ\x001cÕÛ
¿è¶.E?;u\x0002]PãhÆ\x00136\x0014¶!l]I\x0012¦¯PÆN\x001d+âÛN£Â·s\x001c\x001e§+bnBFTGb¥Æ*\x0015bêïÿ\x00151ígýfÄ$\x0011µY~Ý\x000b­Á¢ïaNÌv|h»õC\x0017ù¡úCûüÑwýM\x0012	ÇgÞVñÀÁ§þÊ¾pF\x0010=ç,±@Ñ\x000eÑË@Ñ«\x0003Ås\x0011¸´(`(Ñ\x0011w[ec´íÚk\x0012\x0014W¶¼S\´Õñ\x0004Î]Úè³½\x000ce½:­\x001ft\x001dÕ?fG\x001d\x001d£>«+\x0018oB\x0004¨^õã&ÞÌæÔ[B\x001cþÆÅ­\x001fZÞ*zõ­"\x001eÈÎ*7ÊüãrâÂÆ«YïDæ?j\x0011Ó)\x00191\x0007ä
\x0007Ûvk°íå]Wß5a'eÄÈçJýëy?[¿ÕåÈ|À«ó\x0012?ìÖ¼~,ÅàÆR´\x001bý¶ùWç\x0003\x0005+\È+\x00068MD8¢u[\x0008\x0010ôqd,°çT	|\x001a[÷
8IèÔ\x0001+\
i³
gD¹\x0012µ	\x000b`	\x0001»Bî&Ç»Ùê\x0011e¶âõÙJiCn¿¡¯\x001cËøÊ[\x001f1|\x001e1*="\x0018\x00139\x0002\x000bå\x000e¾4.ß-lLJñ
z
Ë°\x0002æq6]·evv n]2]ñÚt\x0005óM÷Â\x0007BÌfw¬¤¹¶×\x0006Ú`p\x000e \x000eSè8
«QÔc+¢üÐEý¡k$ËF\x001c5üÙ¹aÄ²0ÈX;hcíJ\x0008èfF¬\x0008±¥¸5\x001d\x0008\x0006$¢Ú#\x0006ÇFcíì`\x001cÍiã~\x000e2Ö\x000eÚX\x001bLµ\x001cì¢\x0007ºðÌÃiÉ@vÐFÚ\x00150b¦×m\x0008\£w#éÛè´¼×\x000eÚ{m08Cg\x000c\x0018ZÑqômÀ¼×\x000eÚ{mTi\x0003/è~.òXÞnÝÍ2Ò\x000eÚH\x001b¥;\%å¥±_2å4rû¸õ3Ë@;h\x0003m@Ý7ÇsÁ\x000e§þÇöV@\x0019f\x0007m
(øF}WmÂ\x00130SÅùT×îA{í^\x0011ÍØ*És\x0008\x001bO@[o;±Òv\x0008Ê\x000bfEö5µr¬ÈþÆoö7²ò/hKÿ\x0000ÅGø½Ôá»d\x0003,v÷FµPFÚA\x001bic¹È¨ÅI¦×É"¢ásÅoM,N\x000cÚêD°Æ&ÀÜ\x0007'"á8ùBÜñ\x0005ùt\x0011´O\x00170\x000c\x0015ÛÝÅ¯+"mAo\x0017Aûv\x0001(z\x000cHUÆ\x0015ÑÆ]uÁÆP;Èl ¨³\x001aS7Szº÷\x0010Ãxº7\x0011¥\x0015µ\x0017\x00151\x0010\x0007­è¨_Ö\x0017Ý­Ù@\x0017Aûx\x0001¶æTüHkÑ\x0012"·ÚÔµ¸Õ2§
êÊbûÜx\x0016/\x0008óîµtc(\x000b2a\x0001uÂbq¬ù\x0010x¡2Ï6á\x0008·8 \x001f\x0007@û8P	\x0003ë§ìOpÔC­WÆ 3*PgT\x0016>>üÆÅ{M]\x001e­Ì\x0005dJ\x0005ê
\x0011\x0003{\x001cË1\x000eV®=Ö[$È\x0005Ô\x0019\x0005;.dc»Ðiq\x0017mt8 Ó\x0001P§\x0003\x0016ï\x0010óHûèõ\x0002e½FeÁÆ
d>\x0000ê|À¦>\x0003Bn;:T¿õÒ\x0018dF\x0000êÀÒøþrßùç­â¶>8¬\x0005m, 
\x001f+¨\x001aÖ\x000fK9[»ñ\x0004tIë\x0012Ù½GRrñ#³·e3\ê\x0010ÌÉòxþaÄQÈd·` C0P`Î¶\x0016ìþ}\x0017,BDn1-fk \x000b²²\x0000´\x0005à\k8\x0014×Ú(ÙS\x0015·îåHzÁ?*\x0011½\x001dOÎÞt}Ô8º`s\x001f:Ú,\x0011ÅÆ8Òr\x0014Õ¹Ø#\x001cD\x0003q«ÇòäêÏù2J¶í5$\x0015Ë¡q\x000cÉVBÙñ¥¾ªsàF}g]Ômr\x0019¢+°1òpêÃ\x0019\x0015j¸´ f¾3ê\x0011¢Ù¸¡£<ù¢úäC+rI;+²ÏÉiësdoÎQûæ\\x0011\x0013ë8\x0015ì\x001f'+À»%m½|ò\x001e'ªïq\ô¤dæpöª!Y\x001dÃ²:9n½%I2!HêÀÑ
ÔÄ¦HQ,¤øÿ1÷6Ùu\x001dÇ¾çT0\x0002¬üþXl\x0014,A\x000b$eÔ²oG\x000b\x0012q-TA¤\x001eHøYn½iT·Zuû5\x0003Ï¤FR\x0011\x0011yvlìs°3÷ñ}lWlëwcgFFFFüCoL5E¹£c÷¶»[UJe\x000eLAä³%ù­6%vo\x0016\x000bûºLSÌØ´[T\x001f´ar[kÂ¢L\x001cÇîÄ±SÞî±º<0åNØsë³séºØ®³¡ùmpÑ§U½ÀàøT"Üx_²Q7övêzÖG"ö\x0010°	
·_$¿5Æ²\x0015(ö¶\x0002yÔ} [_
¹É:VÅI6mF¹;RtµÉ\x0011u=XL«ÑHvkÏWÌA"öF¶vQ=µb>\x0015Dì\x00142\x001cA¤ ø`1«Òæ¾ñ$³u©;[gÁU{ò8!°\x001e³	Mv«ËI2\x0003º3\x0010\x000e"XK\x001f\x001aå]êÀªh¶v$yÃOÝ7|\x0017\x00027'Ô
«ÛÅrº.¦´q·$}OÝÙw\x00175wHbÇi¨*R6ÐD\x0001imYÆ8¹;Æq©µ\x000e$I4Õ&N(Æd7f!² rw\x0004áU:¥ê? 9­\x0011Sü\x0016ýÖj¡,\x0003Ü\x001d@xð8ôÈ\x0012éè\x0003'Ä©q³\x0005e$w'Iþý\x0016\x001b%wo\x0014_Gü\x0016Â\x00109u5 ¢s[(\x000fçÜ}8{,Ë¯!NtíJ\x0005>­h68ZÉuX~îdë\x000b"lfSýMË4¼ñ¾¢±C"öF\x001e\x0013ÌhXÀÚ\x0005ÎD³±ÅT+ùÚW~îc\x000cÆ³ºPpÛnç¼g\x0008\x001b«ÿ´\x0011Dù¹\x0011vLfFS\x000br\x000c¦¤YrëõYk=cì~­
®éº¶©À¸%\x0004»-£ç$Ý¢$\x001e¾%×¾T² EEQñµ l\x0015È\x0001¦4cìh\x0003Ö)j²c¨#ÔPGÑffÜÍÑsánå\x0014©\x0003kÇYî ø\x0016\x001d¶\x001e2ZÙ·î¾FØ=¨jÕ\x000b0º6fÁol
Ò:Î\x0018»ß\"\x0016ÁWÿ\x0008[Åõõqc9¥ÖyÆØ}\x0014FÚ	¶±¡8ªfÿ¸µ4G\x001bYÚ[~îdt_]\x0002vÑUÿ\x0018U;\x000bÝÆ'
=Ó	ÐÝB\x0001>¢\x0006}kß$\x001f#\x000f\x001c3ÁÆßÚÎìh»íP;öòüÀ\x000cGf>»þÑÎ\x0014l÷E\x0010sbºÆß>P\x00130FÎ>y¿±®RÏ¤u4;¼g<4Õð1[n¥óvcW§vòÑ üÜËÅ\x0005ÑdÖÎ-·UY
fVìn\x0003Ã\x001eèÀ:æºn\x0000¢kÇzcLÏêSuj¶ú¬¼¦6mDä\x0007,¯7öLêYõ§î/ÿÌ[ÁP
bì¸zÃrvÚÏ¾´ïýÒ\x001084Y$çë\x0008DÕlè6\x001fÔ~vIðÝ\x0004,b£`ÂùPGµ\x0003£â\x0000\x001cî®[8;¨»K\x000fÀak¾ø;k)\x0015ªUjJ½v£ü\x000e27Q~îcÔJï¤3ÕÁhÝ.­v.\x0012ÞÍ8ËËëîÄ|0Ê ;,`Çú©Q¥\x0012Î\x0015¸»	Ó\-®7ïâÜdlb¢ò\x0008m¹³\x0000k\x0017·!æÙm0÷Þ\x0006Q®Oi\x0003z\x001bÔøBM1oÛ0û2û\x0018a±q\x001e
\x001c5o\x00188Uè{Ã¶\x0016æÝ$co>\x0014çárw\x000bv¨Úµ\x000cïÛ\x0018õL\x0001K÷F¶ÁC´C\x001a÷K	ÈÀ7\x0018Fôj+âL\x0001Kw\x001f0ÞúfF8\x0004CEÌÜ
þ{Û1³» é¾\x000b¢Ö\x0015OxÀR¼Â¡-ÌhÆÕHÅÑÚj÷|\x0000¿x1\x0019Aq£E\x001f?¾ùp{hàÇyûF¹æH2B»¯Úå\x0011\x000fç8WôýõõÙ7çûÇ]1¥\x0011f\x0004SE¢\x0010°T®¬>pgv\x001câ´Ó\x000ep\x0000-rÒkB°-efÌòdÉH@øEÕ	ÜòÈî\x001e?\x001c\x0004\x0000\x0007'6k\x0001¯¶\x0011Åd©¨ß>Ñ$ÚÑò\x000cïoßspv\x0001!G\x001cGñ®X5Å-Öë\x001cÚ°ñ´o½v\x0013gIGQØ\x0012q$9Á¨=ÆbmÅ³´q\x001eµ±G\x0001jMÄä²cJ;\x001b#\x0019yÒEÈ¥~\x000cÙ¶\x0019ô8LW#gn§·&ì÷Óì§CÓÌ\x000b?¶Ò\x001c´!µ-kb$ÉÓ¤L[\x0018vÏ\º~ä ¬\\x0006\x001dY9YjÑ1§]¬-!\x0005Ù¢Ôq£D_32ÜÈäY\x000c¿\x0010gñg\x001aòxèè\x0008*s\h±BµNy¸V°¿C7ÐköxàÜ`Â8%ýü®V\x0008ëá\x0006¤Qy3b"æ~ÄHSx\x0000Ñò=
®Þ\x0011Ýf+j=EÔº1ñ8OïêQ@\x000cÆ4Ä=¡L\x0007¢\x0015¶\x0017\x0011; SCÔt§\x000f®}h·ùCk±[t÷vÑp§
±¦é\x000012á©Z\x001d\x0014\x0013.EÕMèÒ)ûwwZmh¨\x000e\x000e)³á+\x0007õ\x0013\x000et\EÕ\x000b=ixX;0Øaþ\x000bÍ!t%õr\x001dÛØ	¿Ü_¼nZ0:	ê\x0006@]Ì­W;ðdsì\x0001k\x001duËï] Bi]	¥õõ 6µ>Y|?¯}ï*4½8³ÜâÙ\x0007ê%¨\x001f\x0001U¾©ÆÙ*ú¢LÓ\x0003Q	Ú.HÑE©D\x0017åjH}ùT#¨Ü)Í³·|Ë]¶\x0000íáÔV	Îòs/(\¥\x000cw|FÌÉÓUJ³a\\x001ehÕ\x0007ªg z\x0008ÔaÙo\x0001µ(3CnßDZôÂ«\x0017zÚ\x000c¿\x0012P¸\x001c\x0001(Ok8ï³jõdËUF f\x0006j\x0006@q»\x0006Zr<@ê¸¯-ºåW·.Òä\x000fiàÃ+¸.S\x0001\ÈÔ
ª#J¸\x0011©^®æé!5*IÇ¤RÿÇÇD2«Û£Më\x0010öã½ä6|£¥s*?÷âSa¢MIÝ+Îd\x0002]~Îì#u3R7Bª27x÷$©"×ýC¸´ùT2¢Â\x0007IÃ\x0000iÈ¥ª°:¼\x0011\x0015Ò6ê3úåÁ{}¤qvÐÇe
æãV¬(­Mþ@ÊbK1,·´vÎl\x001a\x0007mêÃMÝ1mf¤\x0003NÊèÛ1jyTMHm<VôÇØûyöõóÈ×±P\x0016\x0013ráa\x000cË\x0003.ºHç\x0001éHDZóú¼NcmKÂ^\x001e#\x0011÷Ìmë#µ3R;@êskZÁ}uDÿd«Å_ÖÈï$õ3ÒuêÚTçX\x0003þBy¤RÜ3Þ«t¶£ÌÈÂ\x0004çºwOâË\x0001\x000ciÚ×ßnS+c>c\x0007b>ã±Û\x0008Pâ¥Ú\x0014SÞQq¹®ÔHZ3bS¯[\x0002«Îë\x0008!q±l\x000cË\x0005k}¤nfÓk³ñ¦M\x001bX\¿~p¡í¨eÅNR3#í\x000f¤ÿ{HÃlï½oðMnPGu·oë4ÍR\x000cÑ%i\x001e ÕIsbLüô\x0014öÜ^®K
ºHãì#gömÐ_Ì-ÖKiÁ¸Ç 53Òu
ÆãöÔ\]I#}H{&ôZ-¯¦åç^RMàIø¢W"\x0014\x001f}ë£ÝÎéä~²n`?i\x000fÔfSpK×ö6òì¤¥åúHÝtà\x0016¥],ß\x00161AA¤ÓQ@ºyç['s{Ö
$÷4&÷<z\x001aÊ\x000c.ë%`ç\x001fÁ¦~fS?bÓdÚÍ\x0014¿~5iÛ÷j{tbg\x0019);ÂrìÓDg~b]<o27\x001dÃCÙ }iù¹Ôb/¶\x0016½R\x00045p<\x0001â¨Í'©
vF:\x0010ïkk\x00147ËÀ?Æ£ªÜbÓeaÎ.Ò(³¦åçnR;\x001aXâ¤*²hôË\x0013ÐºHMËÏÝ¤\x001a\x000cIãî4ïÒ.uêà£R\x000edz4¾àÑ0\x000e¬B«Ñ	\x000e«=â\x001dÊ¦4#\x001d¸Ci\x0005w(ÞûÚVAh¬jIå\x001eÃ\x001ePgdRÂ¤Ø"')\x001c
2\x0007'ðÏ·fù^âòÀ{	¶_±Ø\x001a\x001bÕô	ø;¾@û¸)4U¥i\Mju¤¬xÂ=ÿøáöËo¸8ÆÞ\x001c9·íøí)/í}d>óÍù»w\x0007kù*â¤6§Hõ#â\AÝ(UÕ\x001aõ±IDÏ'PFaÈ8`H\x0017Y.¬\x000c\x0013á1Ùm~É¾\x000fPN2åªö'uc¢f\x001d\x000b«ëD*Ç!ð`¼òb½UÊK5ë¢Æ"öùýÿ÷¿þ¯³\x000f\x000f·|9@	áQh8
¾¾%Õ0Ê=Zm\x000bÏO.OÎ¾¹:ÿë»ç '!\x0013BÊi%¤§\x00017Vã´bORkHìr\x0003g\x0007ãÎµ\x0017FáÙ×1:§ñ,Ôµ¥ÏZ.
Ó~Yªp=a\x00080\x0001Â¹\x0016SçxÊV$q£\x0015C\x0014_:Äþ/
G!\x0015=[\x0012÷ÁÚÔJ×ÌòÔ\x000eÈ$!S?¤í\u\x0001Òqw¤3+Ì²Ø\x0007d_;÷mý´iR8%ý\x000f\x001f¹4Ì,\x000b¬grEÆ\x0015\x0019T Æ9ø¥¼eCb#â6È$7v\x001aØØ\x0011ýx­\x0007ÖÆ×\x0004lq']$«Â¾ÂZÈ,d\x001eXpê\x0012#|wê4õ\x0014®­Ú\x0017þ®DÔ\x00021DÔ²Bìë`´Z|ëYMË*Æ\x0000ÿMÒ×°¨\x001a^Ä4ÜüxkÛe}\x000eÊ<£ìßÛAaâê\x0001±ï«R\x0002f+ðÕÛ¼¤¶\x0006J\x0019¿BJ7ûânäC\x0008¸@UÕç7¤­Ìw_rs-¥7Ò~JLjs12®ËZ\x0001j)÷Hðu@z¹Á½ïÞàAgÕÜ9æ4¹96ð£öU¬¦m\x001e?°yÀçÌ\x001d\x001c\x0006	\x000beö\x001cñª}Y÷µa¶,ÃÀ²Ds\x0017[ +å$¢Ô\x001bFÜÒ?ý\oÖbãï¾º°_n\x001fÀâï¾\x001eØ²¥óËú_Â/^ÀÅþ²!çë?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=`\x001d.xéà¿»b;GÙPî
¿»A#c\x0012¨\x001aEHEýy}:~BI\x0015u{\x001bC )º*\x001b¢óc7\x0008³\x000bKf:,åå\x001eãyÑ\x001fô ±¸~YíÎój7§HM·Ú`µ\x0007ìº¡¨£gé°0yç(oâvLÛMN+ØÙ±OÖ&:\x0016\x0019þêÁ³v£zÚôýmnA	ónz8=Þ&A\x001dÎ"WbrT¶\x001cäG¡DÙgïjfÊ§Ç_¦¿>\x0016ßYêRd5\x0010Å½*ÊëÑ"\tÉàF\' ýý®DZÜr-?Ìßp±¹Wy«â\x0007jôÈñ¼R\x0016Â\x000eC$CûûÀÚæIVØ×ù\x0015\x0016\x001cÔÿ(úí¦\x0008.3Vb7Õ0\x000e«\x0006Ñ¸¢fYp=\x001eJ¡Ü?$¶\x0000ÍËk¬]÷¡ËLG.|Tô\x0004*¹<\x0003¼Ot,cé°ìVt\[A²¶~§H`öâ\x0011\x0006®ße÷úqX[?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÙZºè°dÝ\x0017ÌW%\x000b3Ø¯\x0004K¾ÖÁ	°è'\x0014:Èk£ ÌIT0½\x0014i¿ÿeùå·Ëkó{\x0011\x000c3¬_\x001c=½¿{øóêóçí\x0011[ð<ì}\x000eT6ù\x0004Ðjð|¿xó·×¯O¶Pòw0ò¯\x0010ôl\x0018Üå²ÖºêÐÃqü\x0006²W\x001e\x001aË<åÇ<$KHÄr$íZ\x0007ó\x001c\x000bd '\x0017p%Û<,Sn\x0019\x000bo~ÊXt_*\x0015ÄrY°\ÎK$÷ª¬s®y´Óíý\x0010ñö",ÅÃ
j¶\\x000e~[~þý\x001fÎmôxá«áyvqûöÃöÀ>V\x0013ÉGBk¾³\x001fF\x000cé\x0019£érqÏ?ýË,\x0004Y©¹Y\x0008²ËY	q1³íß *"7È\x0008bX\x0000#½Y\x0008ò­Ô\x0004 RQ$D"±\x000cÞ*¿ìû\x0019vw\x0006sâÚkì\x001c(\x0008\x0002Íð\x0006\ë¼\x000cAv;ã,\x0004Þ>\x0004À°ã\x001b|à#°\x0016\x0001°¥ë>_Eü_3p8 G(àÖ\x000eU\x001d¡ü·©Ý\x0005'\x0000òËÛ|2ï©O\x0001»\x0013o~Áæ»l\x001a®ç¨\x0012Fj\x0008¢Sô\x001eÌæ$Ï^â2ó]Öló}\x000cÿæ}\x001fJ½\x001f¿Ì)ÑÆ'aü ÷¸\x001fÀÇx÷	¨Ý´4>½{¸}w÷°õûÖ&Ê\x0004\x0007ì6U\x001fhø.j³	¾xóü»\x0017Û\x0006µ»Ïç'ö~~\x0010ù\x001bÇ\x000bPMdñûA²Kðõ\x000c\x0019ÿìÿå\x0015?ìg%úxh·O\x000f\x0012Nó¿ûËðÏÞ¯{_º*Êç\x00136ãç-Ö·éóqÉ/+.Ò_\x001eGIôÖ`\x001e¾|\x001e%k)=ÒBàÕ»qø®l¿-\x0002à9\x001b0-ÕÉóË³\x0010\¦?ÞGÂ/³÷O/îïn¶\x0007 ÖqaT\x001bàæ\x0008lz§o«3ûôøüÅ¶]W/ërëËµÿÿ4^ùrçw~:k\x0016N4â¾5Ê.«fz\\x001aÿ¹ßÆíòcÏ·£%UW¾Mù]+´èÛ\x0003³·ûÛÆþ×»Ú>¾B,UÐOÙØ<Ü_½¿½Û®mqÙ¢\x0002K| Õ]0\x0015ÒÀ÷8~
Îó\x001f¿Ø®r\x0007PÐúÆÙP\x0014\x001b¡8Îy&f\x000c¥Ïs1,ÈfC±¶rçI*\x000fF®@<\x0007Ê;ûéÏ_ä
g\x0017¿]ï,Î*Ó.¦Jä\x0015æHö\x0004Ë6\x0018F½RÛ¾^^Rù±÷û¦\x0010	pBõÉ\x0017óÿ¦ëT©ßóÛWHWh¯\x0010+-¨ì(\x0002á\x0015÷
øaFr\x000f;syqñ\x0006¸plëäöýÕýÇ­_wqc|+Ó;×ÔñÐ1>yþÃÉù³ã\x0019_Ç)-ü³÷ó8mc[^Ç× ^f_Ð%Ç\x001b g|>ûT}Â°D×°ÀéfÍ \x001f*ø<|S\x0006²öÿöJáÅ\x0013&Ùó\x0010üåaÉ×³2Ç?{¿\x000e@T¨\x0018\x001cs2Ø\x0006Ýb²I\x0012|\x001e
ñy³q\x0004rD@µ^\x001b¹\x0006ã^rôì	íû¼ÏÞ¢x\x000c×°V{ì9¯Åt.â_¾8BØÎ¾÷÷o\x001bè0\x001f@ýµàkwoàKN¿ 0s\x0010dkt;\x0001*\x001a\x0000À|\x0019Ü~øíýÇÅ\x000eå»\x0017kÖÙÃGL/Þo×~.\x001aZ{äq3p )8"
:ö½zgoavñ|»\x001d\x0018\x0000Éè£	\x0004÷èÄY*ªÉy`{XÚ÷&Ì\x0008I45i4C(ÁZÊX×6\x000bÅrE^w
Cs°ü©~ºÖ\x001fqDwUÑà«O¿>\ïÊ\x0018$*\x0017\x0005léK7ÊRq\x0004e»¼ÑËWÿëÍé,\x0014ØÈ¦Â<\x0014Ø0D(òõõdåk\x001a·ËP\x0014+¥Õ<\x0014:a"rÌ\x001c\x0014gò¡\x0004Å»ÛZ.\x001dliÁ??Ü=üùÇöòDÂïqv+ROeÖÜ3Â\x000f/Þüí?ç|\x001a³WaÆ§[\x0003\x001dD.[ÅÖ\x0014$ÿl¾½øgßgCS
ÙQÓíËÜ\x0018åÂOg{ö\x000b[éöK»Ç¿3¿\x001có=Ã?û¿ì]û²â*alMz§?óÓ¥á»üØómciõ¨Ïz¯.ÇÃ¾ivÇ³ä\x0017üÚ¼Ï¿øå\x001c\x001búz`e³©bÒ|É×/Ê×/ö~=\x0011áhþ:-ëÄ¯³öw³¯¹3|¸ù8_<¼½¹øsGß] vq\x0002´\x0000\x0000hE°~Ð)ûüøÍÓ³ã¿m×+Ï×tèÞÏãö0Ïß·X"/!ú 0=(Q´ïo3¿ïsJl?\x0000`
DbªO°xå¸!%D»L\x0000xøØý¸\x001fO´±2CpÜ\x0013£¬å©0¸|\x0012\x0008¥¦ç@P\x0001ÆØç\x0000\x0012ù\x001a0\x0002çÒ|\x0004Éýüùæsy\x0001ù
ÄÖ´¿#\x000eETq÷§®Ô~9\x0014r­ùÓöwÄ¡ïo¼Á}ß§®¤Ú/NßWÍÿ2~<41óûCßk\x000f\x0004§\x0005ËÉ*| M\x0001ç\x0006v`¸úõòÃ/±x;¨\x0015M/]\¿ý°Ëù\x0003\x001f3:\x0007þé	µGyNÖ¤ûÆýãÓ§Ùåúý\x0004öm(µK\x0004ï¯®oßo-Ybkb<Ð\x0000£\x000e\x0014õñùÉéó\x001ff|Ký»?_+|^¥È¿éA6.r\x0010ØóñÛ®Õ¯ep\x0003;{ðÏñÍÛ]ÙÊìL¥Bòo\x0010?W>î\x0013Ðù[c6²?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ùã²\x0010P
\x0001;\x0008\x0001Ü\x0015 åÐp¿1°æ#l\x0014BB¨~!¢+\x000fli%M³D!tÖcÌ\x001dBèR\x0008Ý/\x0004d\x0002b-s]\x0011·ñìoè\x0010ÂB\x001d®¥I¹áK$Û\x001bÈéÀ°Jn\x0014ÂBØ~!"rIoBivÜâøÊºI\x0016Ù\x000e!\)Ûá:A&ÄîS"	ñSÙNr\x0005v\x0008áK!ü\x000e_ÂòÖâÈÒèyn\x0016pÌó\x001d2R°\x000cÍ\x0004.ÃáÛ4ºÒ»0F1¥\x0013ý2ÄØMµËýîBg7CNV¬;¤¨íõ\x000e\x0006Û\x001a^¿¬.ù]ç®U¬9vHQ\x0019ì§MÓ·0ø\x0014\x0007
ÉKêÀìïvÈÊØ=q¤\x0008ìw\x0018$O\x0007"S\x0006êÉ^Ü\x000e)*k÷4ÜiºQúÈ«Ü+O¡Cq£ÌdK_\x0014Â=í,vEg1®jøæþýÛµîwt´Dª_["R®ß³÷êâ¢oÎ_>÷õÃ»_&áB	\x0017Úá\x0006æ¾µQ££ê£­&¼\x000b\x001d\x001b«áª\x0012®j\x000b\x001aL¨éÐ\x0006FëçK)«áê\x0012®þâáú\x0012®o«,§xb/ã¨ÅûJUwé¹Éêeû\x0011«Üþk­\x00181\x0013ï\x0005>¸ù¶»-«cíçC¾ôè0Z'\x001dt~y\x0003r3f¨õD»¢À\x001eYO
åÞ2ëwaùfÌJTÊBô(7²éÖ\x0008ZB\x001eßß¨wC\Ý\x000cÕ~3¤â¹Íh\x0006\x0016ÏkÇ§l\x0017ö:nÀ<\x000eÉ\x000e:Îô¼ÀÀ7CãcL/\x0010ò\x000b\èwÚÙVm3fáóÈ¦Îa×"ój³·\x0004ÙT~iw,ËÇ\x001cO!+f©÷f2¯·\x001ds¥4L»Ò\x0010
;\x0006\x0012æÜ\x0010ê\x0015³<z3·Ø¹ò0L»\x000bÃéj(I\\x0006\x0011³Ë'÷2lÇ\©
Ó¬6prÇB¾\x001b\x001fò
·Þc¹\x0019s¨0ös¼\x0014Üã¡Ìíèõd"e3d[]gÛ|U0\zDê\x0008ÍÇm YèMÝ¹º\x001a¶ãj\x0008^3ÃéÔtÏy½¿¹º\x001a¶ùjà(£ »ÃQä\x001f\x00013Çy­vó\u7\ûÝðFw-(^Céó¢;¯w³¾Bì;\x0010\x000b.rY9>À\x0006Öp7ÿÈWvÛ7ÛmÜcÇþ\x0011ò¯ÑG\x0008¬èÔ<È\x0016Ì¡òB³\x001dÈ\x001cU	 f.Àõ°\x0019vÄ\iÐ®5l`N0+\x000cóÜ9Ïä¤^ÍSZlÀ\ðù\x000cQh¿\x001c\x00162¡E\x0008Lè\x0018òÒJô
e
Y¶CÆ
-Ñ+¡kì\x0004;\x001b0½T{3è:zm\x000f_Q¼Ô\x0004I¼ÎzVurad{\x0003æ:\x0012í¡ ÒÙt\x001b¯òxáY\x001a+Ù\x0000ZWè°k·\x0015´äÜq\§ ¹­/ê½Ý^¡©´ÝÀWÛ\x0008Zin£46Oô;\x0017 ýTGÑ/ Ç~ùÍ !SÜ\x0019­è\x0019\x0002°.F{aöõAûöÆÝktÐj3âöfçöS\x001d>ÔÛ=;	GtÌj|\x0012¸ÙÓNv\x0014lÆ\x001cjÕ\x0011ÚUÐ´`ÜèLïDÆì\x0016\x0018\x001e¶`®Ut»ýhÿhq±A¶8Ú\x001exÚÙõç\x0005Ð ªG\x0008¢ù\x0011"hÅ\x0014I9\x001bAóIÝ²2Åvî\x0001´l¾\x001d\x0010\x0004÷/1¾ÇËuC;O¯»	´©A7«\x000e\x0008×A¨E6Æz\x000blûp·\x000e5èfÝ\x0001Ý©¨|àf§÷

¡v; Ýí®\¶àØrÍs|&×cwK5èæL#xà¹\x0019#Fåá-¸^ Ø\x0002º¾\x001dªývàs*ß{êÅG\x001aÌS¶\x0005:q\x000eísÀ5CÔf\x001a_d`î\x001duvj·z\x001bèú uÇA\x000bìH %\x000fäYcs»ÇäìÀfÐµS
íNiÄÇ\x001d\x00058eBk¬áÕ\x000fnxy\x000bh[¿CÛþ\x000e­dÆTì ¦ \x001c»\x0001\x0019ô<=í&ÐõõhÏÝ\x0001\x0016\x0007Ç&Ê*Yåòò\x0005\x0012
 ]}=\ûõ0sþ8Û\x00104Î¾ônÁ!¦#*Ìí.\x001e¨ö\x0012fCÛrÁBîÜ÷°\x0019³¯o´o¿ÑÚåÆC¶óÌ··Ô´·\x001dríúv§T+&\x0000ÖVqÝÛÈ£Rû9¥¡>çÐqÎb<gÞe¥Íc\x0017X@ÖcVuÛ\x0012íc@H1¿D×y`ìIÝ\x000eY×{O\x0000Æ1]ÃK*
ò?'&;7º
JM\x0011ÜÁûy\x0006Ì9³k\x00178Ï7av5æöG\x0008Ñ&£¢\x0007ªùtÐ!\x000f\x0015ïæ()U\x0019\x0015üµ\x0019´<¢\x0005_Z\x0003GÐÜQ\x001aÃ­ý@Û\x001atsB\x001aÄH«\x000cÓYl~·ÀPÕ½\x001cª½CÜ¶U@\x001bn\x0017µn¾o\x0003hSë\x000eÓ¬;d\x0010¼à&Þ\x0014¦­4fØ
rÝÔÞe ½Í®\x001cêC\x0003d/ÝïB×]ÕÙ^\x001e\x0011¥Z\x0008Ys(.VX\x001dvÃ\»IªÝMBÎ\x0013¦d5D\x0003\x001d1ëÌ)»Ë¡êÌ®jÏìÊ\x0018Ë:f ä\x0015 `çøíäÑÍk7Iµ»Ix¡
sË¸YgÎI³[\x001f¦
µý\x000eÍö[ºÜÐÔP4gY\x0002c¨µ\x001fèÚ\x0016¶×À£ëÉ)%å5±DÐÌ~oÝËSÒuÂQ·'\x001c%®ðb\x0012.EE!#ó9/m\×t{MHb\x001d¨xqCVRÑÚ°Gjö\x000b±t}9tÇå\x0010k³ÑGä\x001b½°\x0004Úï1µwgÚ½»ß\x0013t}Òæ«8iéÃ\x000foV
ß6
=¶T¥\x001aÜØ&\x00019Q:¿g[pXQxxÝ\x001cÒê<{l}Î\x001d÷9ìV
\x0007i~x÷´:ô®£\x0010ÇÇ
¬øÊ:Ün\x0005üxI®^ÖÓV s/¹P\x000b\x001c$âòºýZ5n,k5ã!àÓ64í\x0016;gLMØ-c*ÍSÜ¦ýv]¸ ØSÈ3Ý2VwÄýö)îfe"4n\x0003Lçíy*Ëå-çnj|S÷\x000foo\x001f+ííáß´6Æ:Î±>7Æ²y÷f,\x0019(óC5\x000f\x0019ÿ"ÏC~:¼þùþÓ:´ÑÆpFO\x0008eQÑÊôó`ß\x001c^wþf\x0019'8¡\x0005§Î#¸ÂC\x0011O ÍDjiCî: ª\x0004ª\x000e4pÇ\x000fvÏÓ~ Ì­sý×\x0002Õ%PÝt¢Ø\x0019H\x0000-7÷ÛiþÂM@M	Ô´\x0000\x001dëó8\x0012dó/äôÀ¼\x000e[\x000bÔ@m\x000bP¬d®\x0003È\x000bÄ$å&®\x0004éZ@ú¡%;fÈôf#\x0001?.\x0015Þ\x0001¨/ú\x0016 Áã\x0002Êt 6+¥2Ç¤çÙ\x00044@C\x0003Ð¨Ú9Ø×¸~M\x0011qYÞm3Ù\sl\x001aT½h\x0001*\x0014ö>¥\x0013µ¼JUià$æ»sÖ"­RUòJe%\x001aÔ\x0010R/C>Ó=´½¬Ìl±KøñÝH}?¾ÊI]¬Ô½lÑ÷^»\$HÄ\x0013Û\x0019é.÷´Ò÷²EáãZv&!Â+k\x001d-+|µ´¬n\x001dÒJáË\x0016ïM®j¨¡·)\x0001Íõi^ÔM@+¥/[´¾·giq\x0008*
¦"ÑßÈo½ËÇ¯©lÒ¦6÷ÓãðSjgÊu¢ùjí\x0002Îkx²¡ð\x0018ÒÂ³û·7ïo>|<ÜÝ<\x001e.n>ýrw{ó°a\x0008\x0000fÅ]m¼\x0013\x000e×¨Éa³ó×§WW'/O^½>\\x001d.NÞ\\N»þY\x0004(E~\x0011dîFÆ6=*Ð9É½*FM¦:P¥\x0010ª_èÑH !xYx\x000cÓCþ\x0012MB\x001dBèR\x0008½\x00103bØÀ%¼\x0018³S¨c`Y§C\x0008S
aºÀã§n-CR\x0017f\x0006`3íkt\x0008aK!l¿\x0010Ñ\x0010±\x000ccÒG1\x0005\x0011ã]»R\x0006×/\x0003®{JÆ4Þ!
óâ½òü!¦\x0003ç\x000e!|)ï\x0017ÂäUéàÍ\x0011PÃ"ð\x001al3ÉkÒ!C(e\x0008;ÈÇ5±yÛñmâ%\x0019FORp´\x000b£dèÄ\x000eïZdåä}Þ\x0005«y¸×h·ÿ§µ¹î·×ØÔMÁ:YðÉ+¸\x000cìoìde±e¿ÉÆoAÜö¸ÛñøKØÏ de°e¿ÅÆW¡(&\x0005 öìø*²\x0014ÎûTYlÙo²q¿­§ì$\x0018"&DýÄoÛË)÷ºCÊdË\x001dl6ÎßR\x001fôL\x0012dsj\x0008÷¢²Ùr\x0007£­\x001c\x0013v*)Ð-¯TÌ¿v\x0008Q\x0019m¹ÕÌ}\x0004^Óø¶	z´wA?UF[î`µÓ~L\x000e)$uÁøÑ\x001b\x001cpì¢2Ûr\x0007»\x001d\x0003#âuz)7\x0010{f
1Ø\x0019¿·\x0014PÙmØÁn#M;Å\x0014\x001fEü\x0014ìÊÊ°¿±ÊlÃ\x000ef[\x00035ád'5+9-\x0018\x001dòýß6Ôö\x000efÛ\x001c¤j\x0007YS\x001cFL&;¤¨\x000c7ì`¸cG)Zìü¦=¸ºMRèÉ­\x0017\x001dBTv\x001bv°ÛÎ2\x0015/½6ø+\x000b1\x0016ë¢²Û°ÝFG¥@Ø4\x000bÊ&OÉJ^\x0014Ý\x001dì6v'o\x0016cVª[ÏR1Äø\x000cß¢2ÜÐo¸\x0007"\x0002s\x0006<ñ\x0015
\x0015µ¿\x0010á~Ã]ìy\x0007ã2IàOa&k\x001dBTv\x001búí6Òè÷Hë¢ÒR9¶c`!ÊOí\x000b~êÇÃÉ»û»-
$TTp©´\x001aHx\x001bFPëùx\x0017åÉó³ÙÎ\x0017ÿÚ\x0017üÔÛàj\x0001G!3\x0017]oîwQ<k\x001cÈëÖÃU%\Õ\x0008\x0017$c|@kÀ[®\x0004½¸és-\]ÂÕ­p
7p9Ì£\x0012q«å-pñ-.­V]\x000b×pM#\Yá2é9pE,,E¬kK¸¶\x0011®òä\x0015;­Ø\x0013ó^åÃ]è[Öh]#Zwý8\x001d4íúáò}Ïv¯EëK´¾õ*\x0004N<;e3É~\x001e¼WaiÍýZ¸¡\x001b\x001aá\x001a`¯ÜE|DN\x0011\x0004³¼\x0005cvº\x000bP.´\x001eo"(C@hÓñr²&aÕxU¥ÇT«"AoX!£f°ù­í¤Èt¥\x0019t³jP\FÅ\x000bÌm|V¼;¯\x0011â\x0015­Âó89öJjæ~ç¾C\x000c+wÂ[Ý_Ózgþ°cr4ÃÙkLH¬+ÿ¡¢}G®.äß~ñóÍûÛ\x000fØpq\x001f}ËW7Vî<Á5qt½æíX00
GÐ\x0012\x0017\x0003N\x0005½/¾;yyú
\x001b\x0014.Î£[ùêäÍÜÎÜ\x0012yü­\x001d¹¢U\x0006\x001e7ÓÓ´#.ÂV4\x0014M°u\x0005[÷Àö\x0015±%Ìs/uR\x001a|/´\x0001¹ÔÕUÁ_; Ë¡N9\p\x001f¨}\x0011b<Å~æôW\x000bôpxÃÍÐ1@\x0005#'fKã\x0012_pã¸
È¡Xa\x0017\x000f½
íÈ-\x0013L9ã2Pæ[	nruo\x000br¨.:þÚÜ\x000c±HÎÝØ`uví$v\x000btUCW]Ð8\x000cÎ\x000cHÀ\x001earwã&àB>°å\x0010a¿`où9~wýîözí
Vd~HörØøì¸Å4\x0014Sªüe\x0004{LÐñã\x0017§Çs&S>
´å\x0010h7£®\x0013=M¯@i¾©äR\x000bfUbV\x001d!nNÄÌ
}À¨NöD­KÔº\x00075\x001cùd4ã¤ð\x0005;&³.R%-¨MÚt v!{VãÈÚÚðày°ùÇ\x0016Ø¶m;`ã{È-£ö9k0\x0019Ù¶ v%j×\x001aI\x000cÝ\x0018SS-v,0ì=ï/aû\x001eØb<l\x001cUÆs`>õh\x001dJØ¡\x001dvÀ±y=¦R§½\x00119 SM`
°\x000bîY\x001a§Úq[(¤H\x001apKËORLvU´à®íc\x000cc\x000b"¤ä\x0018âf\x0005\x0008ÅÖ\x0016Ü\x001d&2`!Ö"Äð&2äxýw´ì²²²ÇL\x0006ËdCÎpÇlÔ&&+A¿£ê=2jAâ)¶èt+ÆÍë>¬Þ\x0013we)e©\x000cÊs\x000f CªâtÞ&÷\x0006Ü\x000b³\x001fîÊTÊ\x001e[9Î\x0017cæD±t<o\x0016åÚÑêÈÊXÊ\x000ek\x0019"XÆ-4/\x001dÚI\x000fNö4µà®¬¥ì0ñ\x001e0¯S\x0008\x000eý×=QWÆRöXKì£ÅAAò\x0004ÉûþÂdv¸\x00016TF\x0007ºNfj·ÖfØBç­;Þm¨t7tèî 3Ï+.8å7\x0019\x000cÛ\x001c;YëhÁ]é@è	\x00170 ãtÌãÞvÂ­'©\x0004\x001bp«Ê§R=>\x0018&¬ÓyK\x001aV:I[¼\×Ô»ºÞªçzGÜDk\x0011\x000fm\x000eÎd37Ä$ÅV\x000bîÊ§R=ii[â\x001fÅÖÑåó,·à®3\x000f=>\x000f#\x0017§o1Ôá\x0002¯×ô\x0016-¸+JõøT>'\x001f¬VÔ¼a<ë\x0013³ëyW¾êñM\&\x0016Gî\x0013M¾`&ëÞ°·\x0005¶TO\XÜ9Uo§þöúáfeMGðN@gcàÀË|uNóe2¶o/O\x0016áj(ájh\x0004ò7=\x0000^M\x0000þÈF¼ã\x001bÄ[¯¹Ù7ÞdN6D#ÉZEÎ\x000eO·amÃ+ÇÌðp\x001djë-ó}\x0010!¯\x001f£uXA´
¯¬Î÷Éª·
xã£û Çv½`Öµ 'ç±6âÍ
z	/V¼6¸á\x001e9\x001d²Ik\x0015àQ­
k¾å-Çå¬Ap\x001f\x000b¼\x001f9\x0015û°Ö\x0001v5`×
Xcý(%@ØÉ}>áNÕõ\x0013
Ü¨\x0015òîö¹gÖñH\x0010+¸¾Öá­n}rÑPxò½¢\x000c\x00138uÌ0m\x0004l*!M«Ñ°{õ­\x0017Ä BÙ,ÉÁVÀõ\x00156ÍWXrñÜFýFÝ!ñÍq\x0018\x0018Vì÷^\x0005ØÖJÂ¶*	«¸cÚFì´øÝyàÕËt¿ëàÖJØ¶*á\x0018[Ó}À9õ&ø¼hÓ¯XÄ´
ï¸ýeÀ[oÙ7/q°ñ¤ivÚyn¦À¼\x000fÞú|]óùªl3b|ÊÍ\x001f>ß_¿bmó*À^T½h\x0004l|¶\x0019*f\x0000ì¸Û¯Ù8±
p¨\x0001VÀT\x0006sD;*ãÿ\x0011\ç\x0006Û\x0000WÕpUë\x0018óZ\x0006¸»Ô¹¼\x0013{\x0005'ä:¼µkvÛâ!ZkdÞjër\x0016n\x001fýP6ÿ(ÚàÊ¼r<"Ô¼îx9\x001d´\x0011oí´C³Ó®î¤\x0014'\x0007^Àår£·rû\x0000P\x0003fÀúZ\x0008­\x0002^7a½çc[WUêáÉVÇ
xE\x001e06¾7òx2\x0017uØ)+\x0016:&¼­QgåÍÏçksÑÒ¬Xç¸\x000e0Ô[]Jìá&Õa¾\x0010ÌÛàÍ»«\x0000ëúuó	Ë\x0002§
9\x0015¸Ó	×Q\x00064G\x0019c}Òâ(\x001bé\x0008\x001dr.m²o`#`S¿9ó¥¿9£k¼­açï·6r¦ÕÈ)Ë©?+
o#Âåq|!&»[7\x0002¶õ°­\x0017B\x0019æ§±2olt:\x0017óÔN/ÎUQ'¸æ¨\x0013rjÊË¼Á \4Ý+\x000b~¤xg?íº
3²º\x0013Qºw¸)'yÂ
ìß|kÌx\x001b1ãÃsôð\x000c\x0016Äèáñ\x0012\x0000<ñTñ\x0013Ìºù\x0005O
xK8!9¨ýNO\x000foÆÛ§7ãmcd²Ë&\x0014ñ½Â°®b¤	eÌ UÝ\x001dÿâYe/ï\x001fopf{%fëòÌ \x000eÒ§\x0016\x00183ÕÊôàù\x0008ùòüê\x0004§µWà\x00127ôàö·\x0000\x000fd\x000c©Î(\x0003d¦\x0015ñÝ\x0006àª\x0004®º\x000eÜòÔ£B7ÎÑóüâÁ\x0006Øº­{`\x0007A\x0004OÞb<lö]tÛÚ¨M×aKæV¸ÙÒaçÍ>aE-l\x0003p[\x0002·]×Ûe¶ÄÄNÌ°MuGà®\x0004îºN\x001c8ñ\x001cò4/\x0011O	×,\x0006Þ\x0000ÜÀ}×k&¦Aàî¸÷yÀ²îÞ;¸C\x000fn\x001b¸í\x000c\x000bëõÈ»\x001aVÓ×\x0003/HñÑò®\x0013\x0017\x0019÷\x000cÆ\x0013çE°z\x001b+ðÚdvÙL;.\x001cq¢ç#'Ü+\©
°+)»L¦Ë­9Z2?K<ov\x0002­l\x001bÞ\<\x001bQû(\x0017÷\x001f×6ÄÌåP¢IZÏä!>¬X&}q~õz\x0005`(\x0001C+`íx="4¦ñ!'\x001aÃu°+\x0001«\x0012°j>á±=À
tiì~,UÊå\x000b½\x0012°.\x0001ëæ\x0013Î\x001eõ@× \x0007+òJ+\x0001\x0012°i>aÓ\x0008ñùíxÀ»áµ%^Û|À\x001a\ð|\x001d¯ÏÕ\x0015¥ëp]	×5\x001f¯b'o8^\x001aYwÚäó]6$+\x0001û\x0012°o>_ÅÛ6ðYEÅà0ÉÒ¹\x00150Ô:­Y©)3£1Ú\x0012Øeî\x000819¹±\x0019qõä ùÍAÞ\x0013byO\x00088ån½®\x0004Tw\x0018/1¢#XÍÔ\x001c2ì\x000eWÕ6£ÙhD\x0007ËÎ¼\x001c¼Û\x0015©ò%Ä ø\x00111¸~Äéû_®\x001f\x001f\x0019ôÕÍíÝÝÍÇµÀ\x0007bZ\x001a¦4w:Ác\x001aÆ»)à§//¯®\x0018üÕÉéÙÙÉë5\x0002@)\x0000t
\x0000s¤\x0000ËtðÛgíÐ¹¯\x0000ª\x0014@õ~\x0001!½Ni)#²d&¹.ñë\x0012¿îý\x0000aØ¢>\x0000d\x000eø<<\x000bÙ_Ú'\x0013¦ñ/Êõ^/¯úpw{½òÍºÌ¿àbèZó!ä5XA{³o\x000e/¿}u~vz¼X\x0012±
­ª>éE/\x000c§Ú\x0004¦\x0010ór
bPO£\x0015%þ¹ÿôðnKîÉ\x001c\x0002QF Îd«Á\x001brþæòÅÜõVOã\x0016%þ~Ù\x0002}¤\x0018öBæä¤O\x0013±+õÊJÔªDý[¥²\x0005u\x0010\Ê÷:ÏÊ\x0000-RÂ\x0003¼&mÐu	ý·úd\x0013tÇ+A}Ãh¬
p/AllmnJè¦ï\x0007.ïãR6ú§®k2NhnKè¶\x0007º¹×*ºäo)Ð¡É$e\x001btWBw}\x0017FqðKû\x0018º´ÌÏe&]Å6è¾î»N\x001d\x0013\x0010µ\x0013HZ:@7ÉþHd_[éz­\x001eJè¡÷Ôù®[ÞÓ\x0011OÝ\x0005>õÉ:u\x0013ôrõhâÂè8v$ûKÐ$@À9VÉ6äµ\x001dí2¤H\x0012 øÂ(æ1\x0002£ì\x0017iÃ^\x0019RÙeI0"f¤k`íè\x0019\x0000ýdv»
{eNe=Efìi\x0000c\x0003vëIÇLÒpnC.\x000cÔ\x0017na(\x0018¼_ü|ýáãÍÃÍÝjËqµ:n?É÷Åñf#Xh²¿:¼øîøÕëË³yZNB\x000e%rèAnpy\x001fq§Gc*Ó+\x0015DüïÜ§Û «\x0012ºên1¦J¼¹Æ*ó~2¹PVØ
]ÐõW\x0005ÝÐM×U×Ìµ\x001f£	¦\x00017VNR\x0000¶\x0001·%pÛuæÀ«\x0011\x0005e_âóq/oCíJÔ®ï¸5çÁej&°¡ÃÂ<ÌVè¾î»\x000e\x001c\x0007\x000bK®Ì=ñï\x000b=ÐC×©{£s©ÉÒTÄÎ«=\x0014ìª\x0015\x000b
24E¢ëØãý6´$:ê@ÇnÔ¨[v½ì²6£}vÔç\x0002¸¤Ø\x0006:w®X\x0019»Ðj¾\x0015{eHe%ÅØNñu·Dëª g\x0017\x0017[WÆHvY#\x0007<\x0007\x000f6dùh\\x0018ÓÞ
½2F²Ï\x001a\x0005Í­\x0005j`\x0019\x001fî\x000bd;jw¾ë9]ö\x00085»\x001d]\x0005ÒìÕã$	\\x001böÊ(É.«äqóeîLCÆJY\x001e\x001a3J/\x0011üo^\x0019%Ùe<¯	©	<©|ÛarV\x001böÊ*É.³ä5p\x0017|`\x001b5®öSûZT¨Ì\x0012t%\x0017ÄÉÇN\x001e¯ÊÚqçSÊ(AQò^ wE:uË7F+^ÒdÔ¾!\x0012ÔÑ]QòR2ë\x0017 {\x0008\x001d{,^~Ü\x0006½î +¼\x001bø©?\Pµ+:ïvÕ\x000bé­È+{
]öÔëLÛ>;ÕaT¦\x00114°Ð\x0019¹\x0015{e Ë*y\x0017\x000fá.5¢SÁeg`aÈd+öJµCj÷\x0018e°EuìùjÉØ¸¼cGèªÒªK;z§Ì\x001bY\x00053cæÞ	\x0001Ué\x0018Õ§c°YeGYßÇ§*\x0017&·b¯ªê{ªQ¡SM}X\x0014¯Ål\»ëSUÕSU}OÕÛ¼\x0015gØ\x000cc\x000f'ë¨ª§ªújÄNS\x0008Wë¼\x000b~zOM\x0013v]½UÝ÷Vã}§\x0018U\x0000±Z)ì]dË´¸=l\x001bôê©êÎ§ªò¬\x0014KCÈ
ìªÛu0í{¨Q+JFnó¶\x0003ÈÐ\x0017Zo·B¯Þ©î{§Fñ¸b:M\x0015Y \x0014Û
¼z¤ºïêLµ¹^ö\x00052ù1vWïÑTÔô=Rb"TBqé1\x0002çøTO.dj´¦?¼½}|bQñoú\x0014$äp	XÉlSÝNîïÓ.$¡ÆOç·7+W\x0003aC	Ï ZîÔÅþ\x0000æÏf¼9<?=Û	ô´åH¨qTb\x000bN\ÌÀý¹H\x0005ÓtÜòêÔl¶k-PU\x0002U-@¥\x001aÜ\x0002±X(Pc÷þü éZ º\x0004ªN4p_%\x000e(9\x0006?ý.\x001fÞ0M\x000bLì\x0002ÉlÔa\x0006k@AÎW®Öâ´%NÛ3'y"ÑSËöyg>¹¶\x0016¨+º\x0016 Èù@[\x0015ÈßÝæ­!\x000bÙ¨µ@}	Ô7\x0001µySÌLó1DdZ¤>ß\x00044@C\x000bP­yQ¦Îy\x0003pãZÏ=4SQk¢\x0016\x00069Âqaª§Ôµ7y£çBwì: µMj1JÎÄÆã¸j\x0002\x001aò¦ß=Þ¼¬l²JVçÄVp\x001b\x0012:ï\x0004l®ß´Rö²IÛ»ü9\x0003R§¹qT\x0001ï?\x0008nÂu-ÒJßË&\x001f\x0003zÞ¡\x001dãcÊK(éÆå»i¥ñeÊ\x001f;û]ÐÈÛÃ(\x001bäç9GÖ"­T¾lÒùhèLSóóTñ(/®¿Ø\x0003i¥Je.õÂ3¯¾9¬¬æ\x001e¾é]\«Ê§£°Faï?}LNÿÉÇë\x000f?­]L²Ì\x0000¦xB"SûÌÌÒ¿y\x001cþ×Ç¯¾ãÒ:Z*i´´\x00151Á\x0005\x001cîHx\x0005OaéiÒÞ­xeWv\x0000\x0016XV*Þ¢\x001e$q¼N±nÅ<ÎæIÍkÃl\x001dË'b\x001fÁë£«Êç<MÎ¹\x0015²ª/rûMitÆ`qÞ0d~RClÅldue;fÃ\x0015¾¨×<Oûðë\x0013ûÝæÐ\x000e!ëvÈ#U½Ì¼ÎA¸L¸6mÜ¶b.³q¸Û6c6\ÑC\x0012>bv\x000eÙõ±_y7ÈÕ\x0003´\x001d\x000fÐò±¨+âÕP\x000cÙO\x001a­CuCÇev|3ò¼6$B&W\x0012'}wÂ,kë7ìQn\x0005M\x000c\x000ePÓÝÈ
wÎLÓ\x000em\x0005-«\x001eúÛA+\x0002-=/ä\x0008¼¶\x0018%í¥éä\x0013#Øa\x0005#fÍ5S\x0016§Y¶b.6\x001a\x0008ÞhÐY³IÑD
\x0011\x0015\x001d3\x0008Êéxc#â¢Z0Euó)ÓØL\x0019\x0010j\x001aÕµÓIÆ ¬,í&\x0005G\x0017r}P;»ínOPÕþêp¼çfWÌô[\x001aÔUc]h:Âß
ZUo\x0010m\x0006õ\x0006\x0004½g{ºõôtñVÐ\x0005¿+\x001eø]\x001bA«²]Qs[¢Áìå$é1üCÐzÿÚ@\x0007Ëç eÖvÛ°õu/Ð¾º\x001eøk#h#äM×Cê\x0018nÓIç~
-Õ^\x001aO\x001atè\x0002M½7\x0011^ö:4{\x001dZLn!Ý
ÚÔ\x000fÑ´?D#\x000c_\x000f«%HMkæÃQvz¸b+èú¤MÇIÇLK¯\x0005&¶)&4¬òÔL«ÐFÐÖU&\x001cm\x0006
á²Áøl\x0010
óøÀäB÷Í½¯0cõ©\x0015sÔx	²\x0006"ÛÃs¦|\x0001¨iîÑíZº /&=}Ý¬¨§!\x0006\D4\x0013áæ¦~¯\x0014¤ý¡Z¡uÞ´B0\x001f\x0006|ã\x000f?>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=Üg'ú¾'ÁÙÚþ¼z1ðákjûó=ZåüöæúòâæE¼Á"¼Ö§kãi²å¹qO¬\x0005fNH7êtBtm§	xºs¥±6\è¬d(¯÷ù\x0007¦òÅ/v/Ú\x0007ß\x001a%]2ÄG°çÆ\x0007Cn9áAZ>\x0001Ï#\x001e\x001e\x0019Ä+\x00054)jI;r¹áç\x0002¾Ð
\x0008Ã«\x001aé¢ÑU%e\x0010W]òÈõ»Ó\x001a'òyßl?ï;·2DÛZ(\x001dÏE]·]$?\x001fZ¾ÐÉçÈN\x0001®óÑÜó!y-ýC½Ý]÷6o\}\\x0007t\x0002F¼*\x0002_¯J¼=PÇhv\x0003á£|÷{cú\x0002m\x0016YäÖhù¿¨fHbÙhsEÈ}&¿}ºût÷tÿñäõý¯OëÏ\x0007¬*í\x0014ìËã\x0015bé\x0003l\x0012OsG5í6C3ßÞ\|sqsy~òúòí»ÕÕËfÌhú\x0019M)öåq3<ÃòqÓ@èFF0CxL©­øLÆ
Ôw)dm;!­êÔµÛA,ÿU[3]&CB²%òQÇ\x000bã\x000fe\x0004ýê·;üï\?~}º;ùfýó\x0001+PgVG\x0002J¬\x0006¼Ydêi|D«\x001f.®\x0011òúÍ»\x001b4½V¯\x000fdÿ2^
y\x0014<²{{ð¼I<9JÛÈýIè¶©=íÈn¼¡ïnÆË}w{ð¨Å\x0017Ô¡\ÊÊols»álÍÝËpôµ\x000b.\x0013\x0001ÿc6ôó4)Nã\x000f~\x0019_+<Û-¼X\/\x001cq+#ÑäµÕ¤øÚ½g{÷\x001e%\x0012&>\x001b6¯3Ýx*Èò:X$>jó7Â£¯}xÑUßU<?L\x0012JðBm5ñèk\x000f^TAfÓæ÷\x0008°îS/6i&3øRËúøÈc/â£¡ÀºYæM´ËäWç-\x0014></p><p>âuñQ\x00170\x0007¥ÄfTÞt»Bû3øbË\x0017;ù\x0000jêA´¼ýðþ\x001d2\x000f\x0016]\x001c¡\x001aü\x0005\x000cþ.<£ØÇfu¨óÞj_\x0015ãé¾à¡ÅëÓÍ'ãéQzN&úá¨\x0003ó~¾Ðò^>TÈ sÊ î¾êîÓËNo´
\x001f~íã¥\x0007RV~Q:¶ÛÚ&ÛXKøR»ýRïöC\x00129\x0017íbL)3¾ñ\x0000vóEÝhgúÚÇç\x001dG~³ö\x0003æ£©¬ýô¢ãK\x001beÄG_»ø±ÒÝG[+ëëk\x00133Jø_À7ê\x0014ùJ§°.@2^\x0018F§0`Þ½Æù%©VuT\x0014\x0003RJa\x0017`JR\x0011¡S	wå9y®Î%+¬½oî·ü½\x00070QB¼\À\x0014Ý/ñ\x0005§\x0005\x0010B\rÁé¡$\x0003¦>	&7\x001cßÀä\x0012ä\x0000­C?L;m«\x001bpã\x000eÑ½HÊ'Cr\x0014¹\x0006\x0006õX\x0019WæÕ¢%\x001eÂ\x0002Ø§eâ1¡ù\x0014;\x0019K"agxÉ%2jíÀ|±S</p><p>m,#íLSnÄF+ìëØZ\x0003Kna½qËéÞk.\x0003rí\x0015\x0001È©ò-ÚQ·g8Ï\x0011îÚì\x0012T»±PzN=ÀnÑùVµp¶ï\x000eNøK}¨ÀÓò´\x001fM\ôC»m\x0003Ðu\x0002R~\x0013\x001bY\x0000ÃuúyÙ\x001dTã\x001aÊßûøÄ´À¬¡}jY°C\x00086\x0000ûÞp¦±³ûEY~bê þ\x0017pË6`jý\x0007ù{\x001f\x001e
MÕ¹ÆéW5ï\x0014|'>|»\x0015'jõé\x0013\x0001yôk±ÏçõÉ7÷O\x0007KÿxPsßZ*ª\x0006÷¡W&e>W«oÞ\Þ¼È6×M~×Ý\x0003§Ë\x000c\x000fJo¢rR¨\x001dAÂû.¤sÓù|Ëç;ù¬«éWÞ¢X\x0017=W\x0007øÖsÕO7tÛËtM1ù\x0014:0HthûùÒÕ!&\x001evî)µn\x0011ß¼ùh-ºøèÜ´XÛRÊ\x0016P|\\x0016¦äÎ2Ø©x 6\x000eFïÉ@ÛÞ\x0015:#\x0005\.iö\ù|Ã-ÁÓôèk\x001f\x001e¾ÝÊ\x0014]CÓc¬æÕåì+ü÷Ò"<ÛJÏvJÞçä?#\x001dnôzôÎì®\x001fÎ\x0017[¾ÞÃ¬¬®3\x001c	vÉhYÝ¸èho¥ç;¥G\x001f\x0012']\x0005îpçÅEoÑÑ°ª\x0011\x001e}íÃ\x000bQèi¸qå>j³èÞ°­^¶½zºz°æ³xpþòl1ûØÖzôóÙæìZÛyvq{IÇ6ó'a·\x0001n>µèðÚ!36óyÝÉGù,?êqÏòsRÚ6îÌýJÓPÚ(\x000faTÚ¸>ùöñáëúþ`\x0016ÞgÒØC\x0005àÞh\x0006Sý~[±éB÷íëw«ËC5Z\x0002\x0018\x001bÀØ\x000bHy2\x0008V>á»J×GÞØ\x00018X}É³Õ×\x0005\x0008xl\x000b\x001f*ÂÒª=ê:)t×óN>ÝðéN>¯6nÑC\x0011® ¹ðR<ã:ø¥\x00024
 é\x0006T¹sGnlh¸#d\x0004+ý³u[pH½Ï¶\x0017\x0010ß\x001aÀý\x0003\x0013H¹%\x0018¨³~·G%÷\x0001ÚF¶_ u)\x0011ï\x0013\x0001´µ Z¸\x0005¹#Ïuó
ãV}âK\x0018· ®³º\x001b·Ë\x001cÀÔ\x0000¦^@\x001d3\x0002ÜV$\x0002Ht\x0006ßÀ»òd'\x0000\x001a3Èu=#ôÃ\x0019}\x001d¥aár\x0018\x0010\x0015²ÉiCF\x0001õ_²%;\x0007<\x0017
ú\\x001a¶+
\x000b/i|±å}|Ò\x0001¹¸§âE/eyfOAèDº!ôérè·Kz y\x000e	\x0004íØqE]ØDUnOÈÉ|±åë\x001e\x0015\x0015\x0005«kêêZy Qå\x0012¾¡\x00149óm"Oà£A¥¾ìÕ2ì"\x0016lD«=¹¼/á)\x000f%Õ¸Ú\x001eòlÁÆúrrþøóC=èb2I¦ÉYI+ÑÆpr\x001d>ßv>~ß¿yýê@\x001b:s-ë³JF\x0004ZoÙeeªyê\x0013ì2O§Âòc8úÚ\x0001#F<åÜD6) SÝ\x0006Úìr</p><p>uÐ5)¨L8îû3EÎ³ÓZDHÌÃÈ,\x001cÂN\x000bÿEHp%)qÈÀ\x001fÎü0Êùjý\x001b\x001a÷\x0007lûàe ±hæ'®­À÷¸t¦Ñ[}UnñÖø\x0001
û± Á\x001e,;ô£	ì¬B,W±vÌ^Hô*é\x000e*#CÛ\x000cåfK\x0017Wä¸­&CÓ©\x001aY¥\x001eYQG~î¢<¿5
3`¬´e:MÇ²
íÀ²±6Ä©C£ñ¿\x0017kEÑñï/Q%¥Ê\x000ciJJÑÅ·zøx÷ðo\x0002<×ë_\x001e?ÿó\x001f\x0007ºZÅêtQ\x0000'uøøèá\x000bßÆ6Rz}~yq}o\x0004<×«ïß\]¼ÙßØJX]\x001a³\x001bn\x0006kª\x001e  \x001eÇå~ÈMÝ\x0011µé\x00190\x0013u(çÉ¨¹g\Ñ<fw\x0006(]Î.Â\x001a\x000co]:</p><p>,´°0\x000f6\x0018Ù\x0004F°d
ð6µº©.
k[X;{\x0017Ô\x0000Ö\x000c\x0010EYÛÜTþ\x0008;vtåÉ®¥_f\x001d²\x001a\x0013\x0001W\x001f½f\x0017M7¹Ä&n\x0012£NK\x001cÊ6 büÇ¯ÁZ2µ\x001d¦{ªmf©ÏS;\x000càüóúû»§\x0003&\x0005M/eºÕøò+yÒ\x0011õ®d\x0001ì²fÑ ¸Z}yqsÀî\x0011>ßðùn>íjª\x0011\x0014\x001b\x0000´z6fWOì.D\x0013Æ&t#Z+ÉFh\x0014pP6ÈPí\x001b<\x0019q¨ù'Ä¦ä¢\x0014¤â\x000b;/¦ht\x001cÛ;[÷eÄd6}¦iÅN>\x0007z[}{÷p¨vîm\x0018ky.Ïô\x0000	{R{èmDr:ÐóêÛëË\x0019GîMSÜ(3îDeµuzA¨Íïì®ç_\x0017¤\x0019ª%	Òª%§RRþ \x000fùðJI \x0007]i¾sCöQ\x000eíc2å¨}ÌdJêöÍ qdoÄoæeväEH;ò4Mäy¦q\x0014{,.».wô\FélCk5z)i\x0010SÒØ²à\x000e\x0018Éq×\x0000×¦ô}PCCAêùpvvùó/ë/_øåºþùÇ§\x001b

Íf¼¶2¥\x000fm%A¤e@¼|ýýêí[~¼®^ÿæúeÂá*$Bº</p><p>;\x0011£T\x001ddDËï²P[oêF\x0003ÍAFÐ/E43®2ÂÒKó%\x000b<kÀRa"\x001a?ßÝ|¿~þ|rþÓýÓ¡\x0018×ÜUÚ£\x0017ï{PÒ,Sjló\]]\|¿º½:9ÿÃåÍ¡MÈpÖ7p¾ÎÅn9uè$>elWÝ7*#<ê0Õ\x0017Â©$´znl¤pûÕðc[VÒM\x0017\x001aá^áÅ:i</p><p>L¸(VÇjB´Hx£&\x0010\x0016¸	D\x0007_TT.ék½di\x001c¤@×I\x0003Ä§uË§{ù\\x001d\x001a\x001bó(ðIä\x0007°èlh\x001dZ¾¾ÝGÃ5d6£öÒ\x0017JA-	[\x0006\x0007-\x001côÂZM\x001dÉ¸¤\x0004¬¯'·}^wó
e2\x001f½û\x0016×U½¨ÎHTe()	økøhÔX\x0017\x001f
×ÃëÊ¸#äKÖ\x001eépÄV~±W~¸ã¸j'-Ë/úZ¨\R{xSïá¥zX>»¡x·\x00035\~p3Å\x0007 Ûö<øCnÏ3ÙÑ@c«9¢gÕ¢ø.¥Ú7K§ú\x00172\x00190?&Ëß§³ÅH.\x0005v¡¹Ï]6s»x\x0014lçëMg\x000b\x001bl¡-=_Ì=MýSKC!åM;	±\x000fÍ
©R\x0019Í
¹RÄKjj\x0012f`²´þ´ÉÏ'óC\x0006f&óC</p><p>æ$2±\x001f.\x001cÎËÎn~µygwä¯Ne\x001bSÍl¹æ¦Ã­©\x001c'_RczàAÎw\x0001¶\x0003xÓÉì\x0006í\x001a\x0002pb¯½RAK¯Y²Ag£%Õ.hR=\x000b@øà:\x000cê\x001f¸Ö\x0005iä@.­¹lx©4'4ï\x0010
ö\x0014Ê1ÐÜ .3\x000còØi¾}hÔPm\x001b¬MG£4²×¢@\x0002#RS!m\x0007b§¢¥QWmBKÃØ)÷\x0001þ\x001f.-Äû\x0000ß\x0011ÜúBË;B\x0007;ÍðóphO1ì¶öÃÝãó~2ó¯\x0000Î}*ÒK¥ø¦Òûº__¼¹}M7lº\x000f\x001a\x001asÉJBâh*TL]\x000e§Ã%3K¦\x000f.ØRdÈIá8±Ò^Å=Ý§±á_­YTc»à F\x0019Ûë#[GÊ}dl¥r{úbM¢3í£¯]t4\x0000Ç2â®]x~%<KE\x0005èLK×·°@¬ËÕÇ£Ü§HWø=C'ÂA+:è\x0013æ\x000eÚ4Jöd\x0000¸ÚÓü\x00052¾\x0014P×\x0018qÌ¹Úi\Ëðú \x0017,Y®;2!)v:\x0006vEX\ÛU ¯\x000fù¿ ªVÁÑ\x000fg0Î|½¾?8z\x0006­Ý:\x000f\x0002g8Ñ?J£Ç¶«í:ùzuyhòLE³c4ÛæÔs³Wgµ¸Û­q»\x0013w'²UÏf\x0011ëóP\x0007|@äf÷ôÖb
ÿ´kìÖd8£ÆpFõÁ\x0001HY\x0000INùxigÛm×@¡ÉpÕ§YVÕwÂ:¸F[I«\x001c['hÄÝ\x0019í\x0013áb³åbïVã\x00164\x0014 ;SúX¤=õ\x0000Óà¶¬\x0019.·eíÚtª¶`ÐRáK!ÜÚ@/ÍZWÔJÅ\x001aMG?\x000c³ÔO´>¹~üíîç\x000fªebî»\x0015j\x0013Ò?ú¶KÉû­<ìÛü¿ýæ×¯\x000eËT@ß\x0000ún@ÅyØ\x0019P³S$Õ6/~[£ô\x0001Öñ-\x0019Ðé^@=t)!a2 s²Àmù\x000cÀa<&\x0001F×	H}\x001bx½¼h\x0016ëí\x0010ß:¼Ó\x0000µr­O~(>õá|w÷ðiýôóáqj!q\x0011mîô¼\x001cÒÑÒ\x001aÂ¶\x0014Ë\x0008÷ëoV7¯\x000fÎT\x0013ÎZTQ8Ûªi1ðëßÒÛLzÈÖk°Õú´ÒÒ\x0019ÒT#µ\x0016u«\x001c\x001aU[û@Úc"LáT%Ù2\x000cï J¶\x000cãÐóÉùãÙG4ÐZÞj\x000eºÔ©H³[ØÙ ÿöäüÍ¤\x0001H\x00054¤\x00064¤9 Q®gC\x000e ]ªö\x000c\x001e¨Z2µ+#¿tðÿdÒhçRK\x001d®¬¡0³õüM\x000bdÏÓ
?\x0006rå\x0019­w'¯î¼ÿúõ\x0010(¾?Ä\x001cÓ4÷*sâûjðlcæ\x0019­\x0017'¯n.¿»|÷îEL\x001aÇ8Â¤¯ý4÷VBVTV(1)i¢Æä§ÝTRÐªdî×<oÒí,öï(x¿\x000fQSHØ(~\x001ck\x001azasÌÙ\x0018Ãa?\x0007v7\x0006Wû»\x001bÜïß¾TÛ:çSµÍ¸s>íKÜ_÷\x000bÐ"4a±ÄÆ©>ð0\x00134v-uÞ¸\x0015ß½Hç[:ßG\x0007ÞH¢\x0002÷u^úÈÅjÍN:MX#ºü½\x0007Oû'9R\x0017ªrN
BA²ðò$n<ÿz·üù¢ò\x0000]=ÿøüNÅçõÃ¯Ï÷\x0008D³(ó¿pööñË/wó~shð§U¥#Uï9wïcti\x0010C4%«êÍÛï/®òõ²ºýîö-«Õõ¿Þ^NÁBåg»±t½Q¸ð)¹T©LÊ\i1\x0017Ûur\x0019y\x0004 \x0017*d<Ë\x0007¡l	ÉïZ?}¼ûå\x0000\x0011þë¾ÈèE¡lK\x0011TÉÉ\x000fG:ôB¹Xâ³\x0004åXLÞ\x000buËð\x0010»7É³oòrãX6T1¤hC|²%\x001bÞlòn.ªX¦B\x0015QQ\x001ef/Ydyý\x0016ïtª¥Òº\x0013,\x0017õd®²\x000bå¨±Y¶×ÉÊÔ½ÚÊP¶bQ\x000b¸t§E+Ä2g`ù\x001aâÿîÕV¤\x0015|Ù\	P«³b°Z\x0015JØº\x001fìó_\x001fîÖÿñ¾\x000c{È#\x001eþù/÷î\x001e>â#âîËÉ«û»Ü\x0005ìË~:J¿Òey_^Jël`±Q~êîâíå7\x0017×çø¸x{òêòâ:÷\x0002Ûç\x0008m\x0010ùþ\x0018J\x001b!D@ÈÕãr\x001cDÔf&¢Í³Á3b8\x0015!\x001a/É\x001foË\x0019ÀS£\x0010o\x0002(§Ãñ(<Dä@ÞrD¾8ç êRÒKñ\x0014÷]FÄæ?ÒFä{t\x0006 \x0014@*'÷\x0002¨EñX2ä[u\x0006¢Ùo\x0011#Y¼\x0019+\x001cc-R]È×ì\x001cDvä""Þ\x001d¥¨J³ÆHA´#!âb¤YÔDÒEFL\x0014"%DäÚxÕbÄj\x0014Ìa,Óµ\x0011r6Ta\x000eÊã0}01¦â÷¡x\x0011óÅÊ¦ýã ¹0\x00071f ÞÊÜ¤\x000e\x0019A\x001dGuS\x0002w»PÂ`\x001esDzL\x0016FYi\x0008ÇQ;Õ¼hJ\x001bLDtAô\x000eZ_|G\x0007ºµ\x0011ï\x0016=ï~Q4rw£'ÿnA\x0004A´\x0000ÇAÄ
£çÝ04$°â¡AzP\x0018CòÂÄ×wÅ(ê\x0016V\x0010I ,ÆPw£óGBÄ[@Ï»bÈ\x001b®X7Î|`Dñ¸E'&<úôOn\x001cu®ûþîáîëÓú!{\x001b÷=8Q1\x0002èËÄ£üàüÞô\x0010ÆWà¨wÝ÷\x0017×\x0017ïnV×{]
\x001dþ%uú½ÒQÅäf+àß\x0011\x001dêA°¿[:T/à_téóÜç¯Ü	#÷¿ø×çõÓ×û»'ñÂ¿^xÖn8ü\x0019_Çù*¦ÑZüP6íÂ(ÅÙ\x0005î_oW7ï./nÄ\x0003ÿzµ?åßÃç?éÇ¿^Ê¯\x001e?ßý¶~úDÞÙïPrOëÏÙ\x0007¿~.q}y«å\x000eIÆóC/j±hb\x001c¿å_½¹½ºøauó
9j¿C	Þ¬®²;~u»?øÒÀ7ólXÏ³]\x0010Ö:òp\x0015Ï,wÉ\x001e¶<çÒZ|Rû&ä</p><p>óLDi'5~D/§-Oé¹´@ã1uu6éò¡ÁMânpLÚòª-[P|´P¶¦zÌµX¹IÃQiË\x0013{þ¾-
ó¾Í>âÉÓâ#^O¦Ýéi\x001c¡§ölÁRu oÚ\x0012VÊ5\x001f³ÉÀôMû\x0012jyrÏFu<Iö@jòbÿ&\x0015z¾Êë{6-¥Mó\x001e\x0008QÎWª¤Ç¾eWø\Vg\x001c9N3«KT»Ýá^MæzVi³qµ/}Ì\x00107\x0004È´&ÈéJÉ\x001c_C³i]u\x0017%\x001d)\x0017'ãT\x0015­¾\x0011&àòÃhö¾
\x0003.^\x0011ìÝJ\x0011ªî:Þ¶å\x0007Òÿ#Û\x001a,Ã\x0002ÓËy_z ñë\x000bn\x0012U\x001bmÇ\x001döh©ñ\x0001,°e\x001cå0²®UÞ¢ÄªU\x0018Áîh¬üR/RÎKê\x0000Ä¼ÓU\x001f\x001cÓ¦¥ª-XtÀtNÈ\x0003\x0006|À´9þ\x0001óï¿Þ=eõEÿÿìÍ\x0000®áõÑåM²q¾\x0019¦(ÜÜw¨éÿÿD;(W¨Ý"hJ4­\x0006G\x001eÉbE/Vn9NQi\x0005\x001at¨ñØYÖ\x0016ø\x0017\x0000ÃM$\x001dÔô\x000bùE\x001b²\x0010ÇebæÊ,\x0002ñ4°	¡,ÇGh`Ø2bé?Îùr\x001c}ÿyý1gEÿp÷üyû\x0003Á¦àj\x0004"ùÓbóz\x0005\x0012Èñc·ô÷W«ó\x0015ýÃåÅí¿¼FîË}E#D\x0018#B7"à\x00058\x001eªBóVUge)lXÄhÆ¦ÑzZå¢4ïPëD>\x001f\x001ba3\x0019íÑö3RÓeöùÊ!Â\x0007¹</p><p>"F½|©ý\x0018Ñ÷ïF<,\x001c?N¹ïd¢èý\x0011¤ø~ÝÊqÝ¿!cIä$Izò\x0017
	F$9NÑù¡ÅüÐéÅ\x0010 £m5cÊ\x0005\x0015ü8	i7æ\x000bº§6ð¬ú~è]t</p><p>&óªÓüñ¾âAlA¼ií<N4x[\x001dI\x0016ð¦ýzýù»§¯Ï\x0007Â%\x0016xÞBÊ\x0005®Å;\x0014¡\x001e}6ÕëÕÕ÷\x00177ïn÷\x0007K*%)7½(<[\x0003
Jç»]J¾Ù\x0017)\x000f\x000bÒ\x00117Mêß ÝrÓ)8Ò\x0004%é³!T5\x0014k¶R0),§ôcÊÍ÷ÿïE\V'GgÓ\x00074E\x001eUú ,«0µí^_åÄ]©SÃ¸éS´à£à¼§±YQÖ[ï}2u¬·\x001e\x0014zQC\x001fúà8Û\x0015"v8]oð½á\x000eN;VêåoÂSd¦\x001ap\x0019\x001fû\x001183W¢àÆ¿|^ÐêÃE^\x0004ºî\x0017¨NÜ¶EõN+#*¦iÍèãÝÏO\x001fÝ8ûË×þûïÿµúðaý×CÑ\x0013.Çéyòv¶Õ¨I+'M^©[;Y½zµú÷ýï²\x0011\x0010'rv\x0000¡eÆ¯]\x001f5õ9ÉD¦fÁúE<C1ÁTdÅàö!\x0017vf\x001e+nDïÆÝ\x000c¢!o"QP&:\x0010Q<åú\x0006ÔÂYè\x000c,[³ò25eI\x000fX(\x0005f,*\x0001\x000b\x0003ë\x0007{þóÇ?ÿõn\x0014ýæîËÇ;bÓÑ»{ú¼~øòxÀêÃª¦ ØÜ#\x001f½ú¦ÆÒúæâíù\x0005E±éà]Ü\­®ßîíÓ \x0018K/Zà¹p§åôQI¡$`j¿ªå`\x0006\x001cjÀ*\x000bjròr	øh_Û©Wï_ÿÕÔU5ãÏZ½[?\x001fØaÚ\x0005ï%wÒ\x0002O\x0011õm\x000bþü\x000f«w\x0017«}ÝK\x001a¢²¿#"Ilú¿ôã¯¿þfÿ6Z¶Trñôñäíó/T#ýü´+R.XÌ»ÝE"6çU»S64iM+¹¸9?y{û=Hßîýâßû?ßÿG\x0012K²ØwOO÷\x000fûïdol,\x00025*\x0003 ZèåâøNFË§±¾/nn.÷6ñïáçÀ«Ñ\x001dsþ´þy}¿Þÿç'ru¢ncåÏ· \x0011\x000b~tÀÎoV¯W«)~¹Qþ\x000fÿùîËÏöoÛ¨oÌéF'7\x001f:pÁ\x0006\x001e
Û\x0015õsâíÊ}\x0011)\x0015Ên 9ÑèäæÍù\x001fv+\x0011Ê`~LBñZü-¹©TdçZ-ÍPàf£\x000cåP¸5)S`»¬º*h8Á^	K4ASa8ÅÆÑ\x000bm2pl\x00039®./_~½7q\x001cæ½¢Né?Q«ýG6\x0001]D¼e©¹KÎ£¢ynra0ºÌ)\x0014µÚÍë\x0003\x0019¤RûôH«
´>¯OÎ\x001f\x001f>­.£\x0003÷"n²	V¬1£$¦äB\x0018Éfh¨uµ:9sýÍêõþñþýo_ï>ýõ·qÔúé\x0003þ\x0017r\x0005ón bàD\x0018ïõR|\x0007)q¡©×M\x0008cuóêÍõõÅ»³ëOë/_îê?ÈE´þÛoêÇq¦ãÕ\x001d®Ó?ÿ÷\x000bw\x0010\x001a¦Þ\x0018\x00135i)\x000fÝ ë»"\x0017ªÞ>û8\x000c¬ÿòø37VÊíòyüLÒ8 äAëÁä,	¼Õr¤\x001b?(òysE"y»\x0017å?ý:}ÂE±êòËgÀúåËz?.ò!rÔt½\x0014U\x0001uù+×Qã\x0004¥<võíÛÕ~ô§ÿ¤#ä\x001d\x0002ä\x000f<Å\x001f\x000f äQØ\]kâ\x000c\x000eãü6%¬oÎÏ\x000füé_ãÅsãò_¿|þÖåúÃÓÝ~£Ò*ÐRÏcáÇ:ý
Ø¨´qlñþ\x0016åêÕÍÅõ^Ï\x000f1Ï¿njàõðöwFãEãÔ¸)ÍÙ,æûì°FÐ\x000c + (µü¹E"YAQ(µdÛRCXÌ\x0010+fH\x0018[!\x001d\x001clÙü1\x0019\x0004_E¥¼\x0005O3d\x001c\x0010J\x0002NüD3i\x001c\x0016éa¡8EþÌBµ9²	*°=­6¬W\x0013Ú0n\x001cúÎBÕSÌâÌÀâÅÆy{E»\DÓ#\x0017}\x0019E.<Ä\x0002ÀIc(\x00175kpub^£Ø³a¬->WPÔ7#ß5&$ö\x001e%eì¬5ÂmF,ùsú)BÁ\x0014\x0014@M\x000blÍËqÖzÞ1Ò!\x001fçÐw S\x0014\x0014´(Kg\x0005\x0013\x000cçøRÛ]ùó/³ÐT³ò9]Ï¡¢Ï\x0018@=Ò¨Ku>ÓÍëJ'ÎIT2R>§Ã\x0004~r \x000cÕ>ë\x0002ã#K\x0006%\x0019È$ËçôSMÉÍ\x0005r\x0005mIÊW=C	%\x0019È\x0015våsú±F\x0015\x001e\x0001ÞZäcmKW\x001cÊFµ}ÁPZùÌO\x000eQ1Ô]Ëüá¤dfî_|Ò*åÏé1UßåbÅÔSÐÕÊÎ¹ì)víßàcéë0ÎÔU\x0002/0nÂ34*â¬|NI\x0016NË¡ZT.EuJî¤y×£É\x0013pÊçt\x0018K\x00054ÅäÊ|®ÒæcmaÖæµ¹|¡|vHÝ "\x001e$ÇâSM9Éc\x0016\x000cyáÊgÇI²ÅÅ²ªE	ÆsixòÍã°\x0003ÆÐ	,Óõ\x001d¾TsI+àqòRÕòR¥®³³,\x0007ë©\x0003Xù~\x0013$[\x0006³#\x000cî\x001eÞ2Ô>aÜ¬SMÍ±ßÄ
\x000cg\x001f;`Î}Øq¥j¼"åVÂSßµe~úkúÏÿð£Bo\x001f\x001eÖ÷_^p+&¼\x001bO=,}q\x0000ãÌÔoßÜÞ\¯.ß^ìøÃ¿¤_ÿlFx\x0002u³\?Ý¼}øø§ý ÚH\x0007s$µR\x0012¦ñ0Kì7ì\x0014\x0006õ²\Ý\¼½>ÿv\x0007Õo¿þå/NZ\x000fçÃ\x001b%ÿ²z8äe!J2¿·º²\x0015Å[ÃöPIâ</p><p>ßó ò\x0015¢U?\x0015Í\x00087Õ_hÊ&\x0006ã%z</p><p>z×.LEF°Ú.ß|\x001aì1\x0015Z|Ü,\x000eïò\x001aBµK¨²=¬ûeåj\x0016³7A4ÞßLevî«©Tõ?:©T,ÝJçöåe'Åx[ìIL¥"¨\x001b½8</p><p>L9£Ø¸HP;éáà_"+:*ù£²+åÝ®OM±8T\x0012\x001dåa¬è)ì]7\x0015
àsõ\x000cò}¯|]AØù6L¦|¿¬ÊPë\Þí$¶¢\x0011Gµ\x000f»Þ\x0016©ÈáC7\x0015\x001ag½²Vñ[\x0010/Ý!2¸Ó\x001cJ\x0015h·îÝ\x001eÈ/;¤
)\x0010j\x0000(.Ò¢\x0014\x0011È\x001fTC¨Á§<¦0Szã¤%P^IiÊY\x0016½ZËî³%GF\x0005ÖZºJlçè0Ü£ùùWýe\x00145\x001b\x001b\x000e?¬¿|]\>üéÿÈQÞýp<VFOéäÉ%\x0013"§V£
»\x001e&h?ü°zûnuryým	õ¾ÀXâ!³\x0019\x001bïsBÑ1£ñGa,Q¶¹`Kv²\öÊÌ0ãî[¼±\x0014ÏeÔ!O¢"FjÌkíø=L]\x0002w©¹nÈ\x0012Ñ	éâC</p><p>4*Ø\x0016H(S½pc*{\x0014Èms»G^jÿpµ5¡ä°æÈfô»\x0014s7bÉn\x0018l\x001erG&@E\x0004#'\x001bÌ®¶\x0017</p><p>\x0000æ¯6²Ø¢~µb\x000b9o°P&»ËJé¦ä<MI\x001dRaÈ=)ON »sO\Üõ\x0016ï¥¤¿ªÕ\x000bdÉtÚï\x0019%ÛìhÚÀ1VâBv¾¢4ø \x000cÜ3\x0018õQyï©6<ÙËÇ ä¸ó\Y:ÃM\x001fCÛ«¸F²t»ýÝ¨'í\x0002]IÝÅ\x000b$Ú?!\x0013÷z6Ù]Ïì^Hz\x00115¯¢NHz´É­£8\x0004\x0006\x0001´lËh±à´küüm\x001a{\x0005&JÃ+õ\x0008\x0010BÕèF\x001d&R¦%J]S\x0014>·zB£È\x0014¥N}I¸×\x0013ì|jvRê\£\x0016h"#MsC­Ø\x0019A\x001a\x000fGG¥	G ¤ÇÆñ^âÄ¸äÉpc\x0017ðn¸Äw:å{1i¶oþmY\x0002õô"L\x000b¹\x0015M^s«å\x001fC\x0013Q'®³ü1WÔÐ§¤EPÚ+fKü,»ãÿ¤3Î@Ï§$\x0005T\x001eú	Ï\x0012×\x0014\x0002%íñÎ<(³\x0017\x0011ôüç\x000f«Äi20ÇÆæÃó!7î\x0018²¤ô¡ü1\x0017SÇSW®H@=°^"\x0008;#Õ\x001e\x0013ùc¶**y\x0006(KodÁä_àÕs\x000c(WP%¦r¥À9\x0019êdZ(½d\x0001Ò#Ø4mõ,Ì==</p><p>¤ur\x000cõ\x001bj\x000bÓ¤vfmtbÒ\ú³ü1\x000fÓC­¸ItgI[°F¬uÇðixzOø\x0005</p><p>|Up\x001e\x0019Ú\x0005²æ.rÁFÄsté0ß.ò\x0014îSO¹\x0013aBä\x0015\x0011vGÛz1©é_þ)L\x001a3X"Ni¨V\x0000
²æ!\x001dá\x0019\x0019éìÄù\x0007È#O\x0019Hc¨\x0012WËª×ÕÎ¨X/$=Ec\x000fË\x00112òMnÒ¶b\x001eA±'ÒhùcöÆtâ9À\x000býD´1A0á'Ê=ÝòÇ\LÈµ\x001a\x0019úÇh5%¤ðùIGxWèÜ\x0014¸|Î<@n]ºB$*'æs®
w|\x0016Ôò\x0013¤s°ò9òÓcUî%U\x001d%ëÅêH;C5½6¿\x0016ÜèÔF\x0015\x0012U.<\x001dgLD\x0003Ëï ý\x0007åsö²GyöRFfI\x001e3Zl8cÂr¤ó,ûò9\x00133:-§Èj\x0016ÇÙ[8£;Âª;r\x0018Ï¹)Ê+\x0008ÿ\x001b%/ÄPÊX\x000b\x001c2_?¥õý®¾Êøöù\x0017f<f;\x0007\x0001hò`ä\x0013\x0017Å"\x000eæ ãPÜw\x0010q#¿¿\x000fQ2Á\x001dW[EñÅà?'YíÃNáiRy8\x001e¢(1ßêÉÙ\x0019]ïEäjÒyhóÊ;\x0012´Í¨µ¨ôÃ·<Cd&£MâÜ0)\x0016\x000f¦\x001bÎu2\x0007\x001f>\x0013\x0011yÈ\1J\x001f¢Ü^½T±¡\x0018%bâQ\x00187ËPú\x0018µ(.5Ø(	\x000c`¯oÅ<Cd\x001e£¡êföcÙê/°ä\x0012-Û±\x0019u2ÛæÎdôzh¥/ÝI\x0000Eê«\x001c \x001c¥r&cJò"3`©×O£\x0014\x0002£eq¬¹IîLFëÅÏfuäù;åhw&õ2òäLeÓ'\x0002O¡âêZÛ#0Ê´4HoBÛx\x0015FyÖîI§ïeä\x000eÃ3\x0019Ub¯P¾­\x0019!Tÿt:hêNdÜ\x001bgÆ\x0018xk~xd8 g\x0001¯5Õ$/gäîÇó\x0019K7Ódð\x0005ÆG\x0006´¼gýÎ´ü^Dnz<\x000fü¼N¼©\\x0019QÍ\x0013\x000e'¹LDäÊåxKx\x0019Ouâ\x0004C\x0004Eq\x000c1r3æ="'&ðÛ\x0010 ¸POõ1\x0018÷æ<LcTQ¢NGû\x0002k1\x001e\x000fé'2r³¹k­J}\x000fY\x0014g°âZC\x0012K3\x001aª°­Á\x0001MÆ²\x001d-Ú\x0016³\x001dÐ\x001dã@ÍÍl\x0005\x000eIs¦p²±\x0006t\x00156\x001c\x000e*Od\ç1Ñò·äç\x0002 â|Iu8\x001c)r¶\x0002'F>ÖÎ\x0018®/@FÖ<\x000eà\x0008¶#9Qv;R¦ê$6¸sJ\x00148îQIk9ÆS^fö3A{_ÃÝ¡Fì´³bòìLzîED½`fß1\x001aO2G>©'\x0018ÇºuÍo°ápPq"#E>gß1Ú\x0003''K]~Å(æM=f\x0013\x00197'õ1&8\x00151:ÉªÓÒ\x000bVú\x0018\x0007³¯\x0018jBlø\x001a´QÒ£i èïÃ)³Ó\x0018mîL2ûPkéÕ,ê\x001d]¶#h]\x001fÖãJ\x0013\x0019÷&'N£á^Mø1T;Wä(7µNG81TÍkç¿\x0011¢fØåªÜ{\x0006ãî\x0011ïï#(G+Açû'|õ\\x001fZ|( ÊÑ#XàdÅÛù¾(GÇrÄ\x0003nØ_&R<ÆqÙ:\x000fßýìÏsJÉq±¡jïè±Î{óO§ùÊÒi(G\x001cÍÅGoAqngß^Â½¹§¤èsÌU\x00089æî`\x001dC¸[ììûÅR3
^iHÜ°\x0013lpÓó\x0010'2âßÓÎ÷Bª¼\x001d¾ú\x0013?\x0010¼\0Îê#Ø;.w}ï)ÓÜ</p><p>\x0006%¥\x0004ÆÕdhª_Îï2AR+\x001cµeÒìqä\x001cÑc<\x0010(ñÎ-ðBE93îl\x0010od\x001f¦cxÀÉhróo\x0018</p><p>f\x0015\x001axXV=FRww÷·êEÄËÅÍ¾`ðÑÇ­ã\x0013¥J²Iæä;s\x000c)R5ØüG\x000cU½sj1>¹äP+1\x000e'pN"ÌGõ|(\x0018'Î\x0013:ß\y\x0003 1Vc[d¹Ã^ào\x000cÀM\x0013½\Kw\x0003À_%Ï\x001fÑäèàüWL4­0Ë\x0011Í	Î<TÃ\x0008ú\x0008&&QÏ¶\x001bm¢J]NBrl}ë¤kÕ\x001eÁ5±£k\ Ö¥jÊ]maf¡\x0011Ò\x0011Ìo3<æÛex\x0001H\\x000bß¾lõPÊ!\x001aEÍÔCæÖn³Í\x001eEtx\x0002\x001d\x001aàe¦NA\x001cQh±\x001caµ©æ6ÌõD\x0019\x001aAÌ¥7Å¿\x000c5}\x000f\x001f\x001b û\x000e\x0016Z©Ø¯\x001bÐ{Ñ=\x000efgYy'dvÔ/ðÔÓ\x0008\x0006VNÕh\x0002nÐ¡»\K\x001aòÒù®zºbR$þßêc iÄú\x0008a\x0019ú³ÏòÇüè?«rEã5@lq>ÝZ\x001f!¾eé:°ó]¸6!«'Êï±¨yT\x000fK«ax\x001fmõ\x0001ÐÆ ÞGqS\x001cÁ\x0000ò\x0014ñó#3\x000eÍ[\x000e)¨ j\x0012\x0005)FJñ\x0018@óó£Tõ?ÓRüeøH¡\x0019Ö6\x001bÒ\x0012äü-	2å0×\x0008p_¼È¬Ëpuç¿¨ï´§\x00148>7Ô²#q\x0003$\x001cj\x0003üî\x0002ÉN\x00156/l\x0012/©MÒEBÃ5UÓ é!?æ®vìLE¾©ÀÅðb\x0002¹í&{\x0019
1.xÅ&nªÐúå!h#?©aùuCSÎÂüH\x0017ùí¹Á¢5Ä\x000eg 3_¹Ë\x0015P Û ÌPÃqQ¦¬\x0002\x0018ñYØp\x0004ë"Ð\x001dæ_Ü:Ô</p><p>O\x0011\x0010¾n8Ñ¼\x000eË\x000fwôÔ\x000bÏÏ×FËcV9©«\x0001ë$\x001dWÅ#\x001cîÜy$î®÷Hªxz`ÒÎs¢=Þ7Ü;;ê#\x0018\x0017T;v\x0016ý\x0004HÃ#¢Ð*WtÎ3cm¾B4G¤2ªÝõIÓlÉÄÍ\x0006\x0013Ø(çÆ$UëækI</p><p>ÛåÎp\x0017Ë\h,¾ç\x0010j¹Âò;QçX{ùü=Sæ*}5;\x0008k\x0013*GÍNI\x0000\x001eºBÙâòÛÝÈ¶ò@YÒ4\x000f´«þÒO»¼\x0015\x0013\x001bAZ-wVé\x001c-ód\x0019)\x000bµ¹¥l>\x0012eÔP[qìlÛÜ\x000b+ÑæbÁA},nïºàú\x0008F¯Î¡Îò9óf¤)^¬Î4ÓÒN¢±:._î3T>g\x001e\x001dãÒCÇ\x0017#ub¬ùgK$§Qæ\x0003îþæÞ6»ÜÈóÞ</p><p>7`\x001e ð~êÓ\x0015Åª¢\x000fEª)R§=_|(.sF%Ú\x0014é¶ûÓlcVð\x001c?Û¨ÌJ\x0006@\x0002yïÍ@ÒÝü05"»^~\x0006\x0012\x0011@Ä?V\x001cpÓ,Z\x0001Ý»q.</p><p>?xº­r ì=àq-%
{\x000e*pW¬ô¹\x0003í%</p><p>ïåÐÅþÚG¹</p><p>\x000c¾t#¥
\Hü\x0012U5ÃGþCúk\x001f¥õùI\x0011{.lÊ£\x001a\x000e\x0017ð;¼%ÏsÛÜçéM\x0001uéh5Yª\x0017§ô¼!\x0002ânNor¹®EµÄômº¶0¯ã¸4Ã?jÛËi\x0004¶\x001f\x0006\x0004ZOà</p><p>D©^ ¼O+\x0008ìåÄBX®©Ò\x0016ËÀrùþ¨ÌK4\x0002a=M7¦</p><p><gvHXÒ\x0003Yü#äsô\x0002~ ôýÑ¦S9õkLnbWã£ü</p><p>¿¿\x000f!yjlÝ  û»Í·§Ù¹u\x0000¹1Mª@zÜJkV\x000b \x000bc4Î­Ký6\x0017×g;edÿô/ßþ6Ãà??üeÂv÷»w·qíö£EOÍ÷Zå,õõ)-u~I®\x0006SÖh§Gï6qÝv­Úß?ÿåþ¥hw>\x001bxôöþéèëÝ÷£7÷wßþv÷íyfÊQ\x0017e$©ÐK\x000fÓ\x0006¹\x001aëÊ,ôyÜ½£·g×G8UîÍÙéÅÇÓÓ]\x0003\x0003</p><p>²ÔåÜA¦¨ë>y$lò á2[ÑÅ$Û¹À\x001dû´b(b+¹Qã\x000ca·\x0012,é\x0000w\x0001Í×tÂóPh£$«Ñû2	Õ\x0005ÄÛÁ¤¥[@¼«L\x0006Y'?\x0017ª.²$ùÛA\x0006¬Óí$·åÅ Jn#_ûõ'ßv2áèªìqV¢¯L\x0002Ï¬¨[ºÈ¸o\x0007\x0019ö`!åQ\x000cñÛ[ûý'Ißf0\x0011,OÝuXèD×\x0019KÚ;ÉR\x0008\x001d\ç 8méYw\x001c%ä\x001c\x0017]h$Ð¦x¦i´óXÙÐ\F\x000b+¿2V>è@<ÆÂYA½\x0019\x0011\x0007ôÆ-+ÑHñ \x001d-:s'ãì p1 yz\x0002wNÃÚU#¡\x000e´<Ä9~ÀC4Åhaíª¾A­X\x001cVÍQHô\x00022/ÚÚ\x0003Jª\x0006\x001dd~ÜOÇ3²
äù@Z®ÝO\x0008ÝîÓOÍd4m</p><p>+:k\x0018tÄgú·SóÀ\x0006L®0Yë¼û¿þÑ»\x0014|.îïþ±ö»÷|9Äp \x000c+HY\x001d¿ûæ|qvúÍ<ÇD¦ç\x0010GHs·0äÁ;\x000eâÍ\x0003CØ-=¼a2¿â\x0000C\x0010&nÁ\x0001\x0001¥L\x0018Æñ\x0014SìïáÀ×7ï8ì\x0007Kë\x00011XNËa
×\x0013`j\x000fÇ"¦y\x0010Ãà¤ô\x001f¿ôîy+ÅÓ»1ËÛµ3ÃÅ\«åßG\x0000%è\x0019 ò$¦K\x00044W«x¹sÚí!\x0012é²M_Õm\x001eB¡\x001c¤A(Áç	Eä1\x0012vç#Â!\x0014\x0010X8þº\x0018%^ñBqJéiÈ)>¼µk!¤a<\x0013"8 Ò
§xú\x001f,J\x0007\x001e\x0016E·,</p><p>ª\x0001Ñ@o,üM×è(¹éÜé.\x0012©óô×¥$\x0006x0güÇi¦X\x000cË¸VÍ}$ÿéþCÿòçÂÆS:å#üüÛ?¿Þ?ìw<\x001ekkH`\x0003\x001c\x000bZÌsê±T¨¦\ÊGäùùôüìrÓ)¡m\x0002Bli³âO@äUzÆ\x0016~\x0005PÊ\x00064\x0001¡ÕÕ$V I%ç×VÏ··\x000fÖìrÉ_Þßß>|ÛÏÆJL\x001aI\x001fOxz\x001dÐÜu\x001b¼\x000b»lÝÛ£÷gËy[>ÌÅCS#ÄXT%g$µ¦\x0001f\x000fvõÄ,øç\x00050DÝ"\x000cHê!¹Ô.Òø]Å\x000f34îÓÃÓßT±Mï¿Þ~¾;º~¼ÿöùöi §¤ç±`Î*\x001e7çã\x0016ïûóÍÉéÑõÕÙÅÉæz\x0007Å_¾»Ï·;\x0015\x0018c`yòðíËmüg\x0002KkãÅ%õ¢¾\x0014)\x001bª@©pçw¿(Å¸òäòâí&~Î;ãÊk*»¸Ë\x0019G\x001d~ØhA:Þ¸(\x0016÷rwOl\x0003ÙtJÙR2/éÑh\x0018\x0017ÃÃÓ¸HÎy±»p¼l:l)</p><p>¤õ\x0019)4në°f&ð·åvw'5M§}-%\x000br$\x000bøF4¬\x0019äÑî"®\x0006°é¯Å\x0019(þð8F0Åî:«tÇÛèn¥\x0006²éX¯¥dÑ:Xºbï\x001e}ÿÙNèÝÅ\x001c
`Óa^\x000bÁ¼p9W\x0014ÍjRÒÓ\x0017Lîî\x0018]Îµ­º\x0014LgÃ\x0017-Íb\x001d3EÒî¬h@ÛR?]S\x0016y\x0018¤æÑ§\x001eñoX¶%zº\x0018Íc!AÎ\x0014Ñ´_ÍæÌÝ¬
h[b§KÑxú9ú¦@º
\x001a$õÕFC¼[W²\x0001mKã´Ám\x0002
\x0010\x001aÐUp¼¡^¬tøöð\x001eæÁ Ð°£Á$G\x000cM=\x001b[¿û}û\x0010Ûÿºÿou¥\x001a?ÍÆ\x0008ìîéþéhó\x000b)ß\x001fá5æØSã'JR
{j¤ãc\x0000³ãÙ8Æa§×g×Gpjù®x,Ã¥QQÃ_á4Î\x0010a	eMMBFÈÜávÜ-Zà\x0018j¾ð¯­pø ÎXµ0ìªÁõânT½MhùÇOTÌù©}íÌðmQ÷¶¡¢X#ã¦¿Jl¬ïønÛù¤\x00174\x000e{ZÈkYcÆ6f
\x001eîm*K\x0011=t&2q_§	$ó3DømwUS4â}Jx\x001dU¯T1\x0003ÊÒðA\x0003ÜÐ)«ç¡åt¿ÄïãÑ\x0014ÁÈpzzº;ú\x0012m]üáûÓÃãýLZ|ÐÈæ{¾«|·\x001d.S××§Go£¥?|¸¾¼:Ûeè\x001eôW÷åWÄ\x001aZU°\x0002åá+ÕÅüþîvÿ: 
­S´¶\x001c@àI%VøRÊþäòÊa~ºÙµ>#\x0008j\àÿ[\x000c\x0002@Æ\x0002+\x0011è*\x0000_´­¬òj\x0007Aþç?></p>
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `2cd4d8-kYyVm4N+k2y7MfUr5lDAUfFyjUo`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
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

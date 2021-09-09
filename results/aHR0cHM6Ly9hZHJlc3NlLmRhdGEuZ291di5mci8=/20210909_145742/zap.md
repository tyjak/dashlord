
# ZAP Scanning Report

Generated on Thu, 9 Sep 2021 14:48:50


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#rHIW`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#rHIW</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=/qöMê{}¥J¢p¯OÒ\x000f¶uïø~¤æ&¡0\x000b\x001d
«¦À/v_ìê­Ïìéeßö[pm»íA-ÅM\x001bQ$7%¹â\x0014²\x0002µ\x0012®Ûs¾\x0017×Õ¸Û\x001eÕR\+1ñ\x0003>5	ZdÂ¾i··ï^\_ãn{Xq
\x0007´ ÆÆ´ÅC\x0015kMPÃNX\x0017°¦\x0011òkòªÏ´ltÜ9õÒÆvÛ;\J\x000bÍiâ¦)\x0010­ô<\x0013_ip)pwÜÅ¼`ã,.Äï<Ù8«yxwâw½¼jÂ»í>.æÕ¨ÁÁX
\x001b*=ñUs.î"^¼\x0015ñ±ãí.\x0005ÚGb\x001cÛIN½ÝùstáT5ç®W¾0xº\x001b²Ü\x001b±ì¢Ô5¥î ìhv\x001atÛÚþ{"]¶æÜ
T4GD\x0003V\x0011Ñm®\x000bÔÕ »!e\x0001B:@ÈÔK\x000eê\x001223\x0001A}
º\x001b¼X\x0016RUæ*\x0007ËvCª] ¡\x0006Ý6«C®ò+Ç\x0017wC®] ±\x0006Ý·,\x000bÉò§÷9\x0012I!ÙMlxOO¼×.Ò:d»\x001b¯]c<åÔ$uÙ¤æxn\x001b¨´[¶SÚmÛyzÿáÃÃÇëCé-\x0016ê
ñòWÒ\x0007ë^.ÕÌR:}ñìÙÕó}-\x001akPUª\x001eP«è»g]C\x000eTOçrfD\x001aÔôú%½(\x001ed(`\¹8\x000b\x000e.\x0007µ5¨í\x0001\x0005õ_LÌ: b\x001açL¹Rîæ4¯Íõí_®»ÿýx{óéÓÍ_oßþ3Ø.®?ý9a=f buyÿ\x001bÌ
»ùîÙ54Lùtû%·\x0003Pâk*-)èÿ\x000bm\x000b%Ç¬ez|´NçòÅÿ\x0001ÆWpêÞ'ç¯Îüx~vyyöóÓ?æ¶Ë¿ìíêa_¿ùtóþÝ?\x0001\x001f¤+ô¤¤íÅ§»ï?b à-Â?$ú/\x0019×)	¶Y$8mKéøóÀsÛa\x001e'êìïeÚ«û*!r¥ÏË?¾x^\x0015{Ñ kÏ\x000e4á\x0003®zë¡\x00043ïN	Íbo>
4ÁA\x001a±w=p\x0012Ó¸Á\x0014Õ\x0008§Ñ,ÖìÏÀm\x0016w\x000c\x001d}RÚÙ0lX\x0008½ØòÓ\x0010\x0019¯ò£cÜ\x000cöÉJ1ö8TqHt"ít
4}ò£\x000eóB¦<\x001fCSNa5é 4:å45ài§KCCCÎ(<C&ÛoÑ£\x0004­j;:çr\x0001h~´]:AÐ´ÉºäÄÂDçñH\x0006÷£\x001f6\x001f\x001fíÛ\x0018ñLCÎa\x0006§ÔöäP\x001e\x001eºÛ0Ôv=É.À\x001c2\x0006@Åtüa\x001d0uó£\x001d\x000etÏpô@âÁá²Ôs:mvN\x001dÞR\x000e\x0003\x0006\x0000\x000c}þ\x0018§åNOÀGÃ§°Á\x0018´ð'ølç\x0006\x0012ïó,¹Ë¤âµ´%«8>~2w\x001cÀgûâ\x000eEÒ¶ì4:®iA\x0007EæL\x0004sxõ\x001e$Ì:Xøì0i\x0002û£ÁñDcE\x00105vUÎ\x0000\x001aÚÛà³c\x0003´¨\x0014	\x001b Á$oÕ´Ó\x0006xØ:\x0008hÀßÅg;`ò¢<ú,Òê9ìÐx0M4ª-ö\x0011¾Õ¿Eùj«êª£§î?Ï¢¥ê¨<ÉF\x0010YLû<i*bþuò¥ÅÞùwvôôòÅË\x0005\[>ò2.H¸òÈ\x0015%¸yË Ê\x0010Ô¾»\x000b4}¬nâJ\x000e±D%J¨³Ä¸áÀ¸¢ÖÑìu?ëQS»	ß6XÞ)ÃPy\x0013	\x0019Ê\x0005I\x001fÑï5c\x000bÒ\x0014¨Væ²\x000f¨\x0014^\x0011@.£\x0010gþRÒ@¥#ïðÄ\x0002G8´}À\x0000\x0016¡pe©§Ì%6\fßv¶K\x0014g~4}DHº2\x0019\x000cLÕø\x0011qô\x0011Ã\x0001®ù(Á½ÏÑ­5Òh%S/q´\x0012¬¡ÑÎ@c£Û2åGËhN´A0	* +Mâ²{ý¢¥X\x001aÒ9ò£	Kfû±Ò\x0002\x0010¸
JMK\Zî;Ç,\x0006ÀùÑ\x0002\x0016¬C77\x0005\x0003ð0»¢7\x000c\x0016Ü}ë ©ËÀ\x0014n\2FÚ$\Ôå3Æ½¾År*\x0005TÓ+(y\AÜ/	UÀF'Ñ¦[¿£¤nq\x0000æAë&)Çß1áï\x0008\x001bM~´¥Ó\x0013º.Ú\x0015Ä\x0017\x0000,8AÛbt¿·Põ\x001fM`Ú`©N\x00023¹_j\x0006Sä¿j¿Á\x0010X\x0016HvÕ	oñ¯iÄÒÞ\x001aÉj;Ç`X\x00108\x0004\x0006ku',DÐ\x0003Ab\x0002rHÒùa×ËÁåk~4q\x0005ª\x0000Y\x000fK¦Û9­xÅ½ÇÍ¥`\x001e.[ó£	ÌRÏ[è &Á¿ÏNa´äSx=<Å<ø9¾ÑÙÉr²É\x0000Æ\x000cæ)¬¦½Ý\x001b}Y
\x0016 ±5?ÚÀÜqÄEiD.ò@0Á#6ºW\x0004µæGwOx	Ëc¥Ø»§SGÐbßAm1\x0018\x0008}äG\x001b.ã\x0005{!0OÛ~0n\x0014,Â\x00194úÆ\x000fi ï3ây(­\x0002äÊzex\x001cÎqIP}Ï&°tæ¦5i!\x0011ìðD=ºÁ\x0012¹FKf\x0011ö»K¶Qæ$ ÓxÀÜè\x0001$KL<ÁgÓ)w\x0007\x0010\x0017\x0002mûTÑªÓ*Ý\x001bã^Szó³i¼ Æ¨\x000bÃÝU;[ÈFC\x0014\x0012ïUdëöªAË¾dPL1SaLÚ<>[Ã:|Êõp\x0011Ja\x001d\x001a³tn\x0013\x0007Î!³§I	ÎÀ\x0013|¶\x000cú\x0018Ç\x000bý
n¯ZôjÜÛÎñºþûÍo¿zK­Ùr\x00132®?¹}wóÝéõ/ïn\x000eë0öD>6{p³ô,¶\x0002ÞîÇì¯ÎÓ/OO~üþlïíÊ\x0006\x0019Ä´\x001dC\x001eo÷}\x0016R\x0000Yr\x000b"»óJ\x00072¨x3\x000c1O\x0008ïA\x0015Íó3(G·ùê ÷àÄ`¹åÄOé`N\x0007¬°}\x001eñ­h¥Ù{ÕÖK
Ã\x001f\x0003Ô\x001eê3\x001au0Z:M\x0007
)f\x000e\x001a]ØpoûDÉ±	"¹ËZ:(\x0019
	ò\x0018AÄ½Â\x001aÕ\x0006=?£³c§\x0007§´¢eR&÷QRÌSK\x001f\x0010ò\s\x0015j°¤zbNÛEY
\x000bMÁ8\x001cÊ¢:ÿgÝ¹áÀs\x0013w®ZÓæa¡³ß"³°z¿qëböpsæU\x0018c\x00123vT\x0014¥OgG\x000eð
\x001b×Æ°×c»GÚùÈn\x0010Q[rWk\©­3øØ´Ö*b\x0000/12¤BlÏq2\x0011Ö#\x0001®¸\x001e³ãÊ:J\x000eÛ¬\x0000¶	<G¤qû#	Ø\x0011°Ç<&e±v\x0001¨
¼\x0000R{60Vì\x000fÌôQI\x000cvQÁÍ6Q;\x001f2+\x0012òÚ¦<Ày3?\x0006:Pº\x0000ÜÂP¤)4ûyÒ¯=«¡ð(?F¨1$\x0007\x0004¸ñò!Q\x0007\x001fQ®ldò_\x0018åè`KTiHØ.gkflïh1ªÕ©Aè;?¨-\x001e\x00135q°ÙµV3AÒNj\x000bÔ\x001bv\x0018©\x0004jI7o,o!J®m\x001c#ØÅ8h\x001c%¥\x001d,¨Íã\x0014á`Òrü«\x000f\x001b¤ùòc\x0004Ûc"1Ðé+QóæÜíu7?µöBy}J:¬Á·ÐòºÑ|\x0003\x001a+sÃbÄç\x0008·\x0003\x0017rûÜI\x0008¹9 ^`]«.³î5>G¸ãÙ\x001d¡¸©\x0016
\x0000Õº³;D!\x0010'üØÆ
U@
­d²\x0001\x0014ûM/´Y\x0019û±k36ìvtàÍ\x0005¶\x0001bÓ\x001cèI\x001eh>>J	aS|\x000eµÀRë4ÖÁ³Ìõà¨µ®|4"Ú\x001dâ&@êØ%ÑÑX\x000e®|¬ Tù\x0004S[FÊ{1|@Ð1jN|Ù[dÐÉ­A@\x0007C[·.ÜFÐ-¼7JqÞ\x0002Ê§¬É
\x0010ø\x001cÚº©Ü\x0004Ò\x001aBq]µ¡D\x0010È1^;Ç\x0010ñ9Ä]ö\x0012e
¢\x000cüÕ+oà©=ÁçÐô\x000eåSJ(ÛÆ[ðõÚ\x0016>8(ZÉÏAK\x0019ñ¶1·S·lqèfC<¹.nLSÓ\x001bô¥(`)J¸A\x0019¤´y¯{XP¹\x0000GÕe8]Øp\x0007ØÉ%¤ÑN&bÃFµ±\x0003\x0004´ós\x0004;
r§?\x0006f3sS\x0003h¨XÉ\x0013éãO|p[\x001a\x0005\x001bSi¼E`n9s7ÜÂýÆøwá=\0Aþ&üszÐ/ï\x001f~¿½¿_T\x0002Ð°\x0012À\x0005¡Põ\x0001² È\x0019\x0011öÔ¥Ó\x0017ÈùòÅÕ_Î/ö\|\x0016°M[\x0013\x0014Æp\x0002DÜ¹lQªXê \x000e\x001d\x001c´M[#\x001btÎ¦\x0012(%°¼-P~\x001c\x000e\x0002ÆOò£íF\x0015èÌ¼´fðBg\x001f*á\x0011»!¯f¸\x0008\x0017ºùÑ:ß²K\x0000p\x0002»XotÍ.|ØõjZá$d*>Ág#\x001d\x001c;=­ÜÅ+Ó)ìÓ\x0007«!\x000e×ô;KL;Âî|.}c^«\x0016D:Oìl*ít\x0001n}ó³ÎA!\x0011\x001d49ÏpÖñÐ9µoÕ\x000e\x0007!-|6Â%;b-ý¾«5Ú1Ün9Q3ÎiWùÙ\x0008g©Õu¹m2Âi®Fun÷f¿\x0003Îe¸öÏê<\x001b\x0008h(,\x0015³VQ©ób\x0005:O\x001eðl§Ãï\x001a±è>ñrpØØv,å\óbu.R,p>7ÒñóÐÆuÎ\\x0003ØjÀ\x0012] ÚvWÚ\x001fÔ_ÕÝ{÷vºòtZòWµê?,µT\x0003¸¸ã¬6Ã\x0019èþÏF8)Ñ%\x0005º\x0008g/ 3Að»÷\x001dt>Óùf:Hâd:Í;ñXèÄ¸\x0005\x000bPùÏ6:iKí®r¤ì\x0016Ç((Q>Yÿþ%ûö7ñOù·\=º'OÎ?ürýù3à}\x0006\x000577\x0007í"È\x0008ÓõqÏ\x0019¡ÏP¦SÑíL»óg?¼|	|/AÂåéÙ"¾,\ÐÃ§Ó^\ð0E1\x001aâ¢À·\x0007Û\x0005\x0018²6@\x0017 K\x0003D\x0003âg\x0008è4\x0003b§Îa@8þ=ÉvÂ4\x0003ÑÃtføeFØ\x0011M«àw£¯]àíäG;¢q\x001c\x001fÖæ`À\x0016óÏìsºøà\x001fí|iÜ(½E+G7xÉ\x0018FÔ»%\x0012=¹!P~´#B};"*¸\x0017ÀA4T¢
-¢v¢\x0006]àëåGÇ :òå£ò\»\x0006¢ÒÊÝÛÛ.D8¢åGÇRÁ½F% ,7Ië$ÒGön÷Â³\x000fêVò£c\x0008\x0005§¦Ã\x0014ev¤!ä\x00114»9Ç]päËvB\x0019dBa)í.¹4\x0011\x001f\x0011ÓèAÔg\x001f\x001d\x001fY8T\x0004e\x0012O[v¼TÞ9\x0019u!aÏQT$é\x0012k\x0005'¥<2Yv»eÞ
\x000f÷ïíßäDtá¡
ú}¾ýxóéöæ@<Hré\x000cHiTO\x0006i2Úµ¥ä^UÁ¾çÏÏ.Ï÷	\x0014ÖE£¬RxK\x001b·O\x0006\x000fInK±\x0010Øn,µ\x000f²hu@:\x000cTÃHzÔL\x0005Ñ-Ãú3ñ"¤>È\Dø§\x000bR0¤wEîM[Ö-\x000b»¥e]®Z\x001f¤"%t\x0014À8 PjVW³+
¥Ôùø®ú0îÞ\x0019S»"³&=¯ÝNH# }i\x0000)litrli,ãªyä\x0012¹\x000fs#X×)°¶\x0010$ë,M!\x0019'¦xD×¤\x000b³R_ëÀLç,Ò,6Oúk®¶Et\x0018´`j/o?Â\x000föy>ýùúËÍõÃ¡;U-09×YèWªÚ{
,AÖÔ£xWG§<yuvrµ\x0000lbm\x0016\x0019E\x0011¨ÐT$ñ\x00139j\x0003×ã`ÉÓÉ©"m`Ã\x000e6\x0008R$\x000b\x001e²G±f2\x0008syÑLfiI¤íë¦\x0013YùB?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=A'*\x0006uØ,Í)MÈ\x0003*»N¨·þk&c\x0000nDä#+8â½TØEößlÿv\x001bÿ®ÍÇ§Í\x000fÿüÇÃ?ÿñ¸¿ß\Ü~¸¿}üp\x001a~\x001b$«!\x00053¿`!k§\x0013¶»tª7Û?ì.£w|u³ùaw\x0019M¸Ø\ì^^ì®_>o\x0007ävÀ\x0008;¬	¼\x000cºÙ\x000eE£mA.wëw¡r3ÔÏ!\x0002çb&\x0002g
DÓ\x0018?\ÚP\x001dvÜ\x000e3Âx'¢ca´!ÎÆxµ&nRÔHÿ
Ãåf¸!fà\x0006²\x0003p|²ÃÀv|Ã\x0011r3Â\x00103\x000c³\x0005\x000e3³\x0005j¢\x000bH-<Ü\x000eY:«!Þ*^¹iÕ lÆÌ¡mKC.ÝU:ì(¾\x001còA,=ÎI\x0006êÌ5³è­<\x001b²\Ín7\x0004\x000f\x0002C>Õ\x001aYÁgCf.ãÕúa£!ë?ÈþñÃí_\x0016(|.\x000cqº\x0006©fd2bÎU\x0015¸Ã×XlOêø\x001aÓ!^\x0017\x000f÷¬È\x0012t0Ô\x001fÿõ£à²Ôs!Û!~×(Á¯=\x001a§
HÃÓð]4d±)¥Ãâ ÃnëÊ!¬îB"^Áb%«Ý\x0010U\x001ct5ä £8µ\x0005kd\x0011\x000fº*m­Åû\!e5ä°k\x000c\x000caQX%xjy ¸Ãâ¨«!G\x001d©\x001ch_yIBn\x0010+\x0010\x001b[¿\x001dÅIWCNú\x001dÅAWC\x000e:N\x000bÓk¶zuæûßlXìÍm7D\x0017\x0007]\x000f9è8\x001d\x000cqL\x0012â½â`(¾B®¨®\x001cô9\x001dônÍó­¨¹¾Èâ8Z!ÅQ×C:ØÌ\x0010D\x0007L,r´u\x0018Ru=ä¬#,ï¬ôÔ2\x001c\x000bÅW8ë¦8"fÈ\x0011Ár²kZó5\x0004´\"\VÑlÌzMq>Ìó!Uò¼:0å\x000cK,ÎÆv|bO!{J\x0004A\âÑ\x000c}63ì@Ä826þl"~!ñ\x0003§	ùk\x0000vAñ\x0019²ã+T\x001alq6ì³!\x000eÌ£ñogÑ\x000bÃí ÑE}ç\x000eCãa\x001c\x000f\x0011Ñk6D1û\x001evÅeða\x000fä«V¼Óp4\x0004Æ×\x001alqÔí£n&fUº(E² ­äÇ°eÕ\x000eC³nGuL«T«ÖxÑ%CX\x0019'Çg&®8ìnÄa7AK\x0012r
\x001a\x001cî²éÙ&dÈ"]o!Åaw#\x000e»Ák:?!{üÜáã4\x0007FÆ{-W\x001cv7â°OÃ<äµ\x0011i|J:>#ò+\Ó]Yx\x001fqØ5v¶q7dD>\x0007Ävû}¿BÒëÃîF\x001cv-äÂ	Ä\x001fcø?\x0017!\x0016{°z\x000eû¾\x001c\x001d÷/#I¼RY:&\x0001HC&)ß ôWp\2äÂTÇß¨^\x001b®\x001aa)4*¥ùÝY.0÷Dc{ì {L´\x0018ù\x0002Jèr\x0014s\x0016·ØBÜóz\x000b\x0018Ï/ø\x0011¡>¸Ý¨TgæR\x0004È¯àåþzttþ:âè\x0018Í4\x0016
)zI³ÖzÎWø4òWGgÐÉA	["pÑñ+QÞyR³æñ@csâÆ\x001ec\x0007z´g\x00167\x0015ÓäT\äué:9Gö2ç¿¢ª\x001a\x000fÎG\x0007çÇ\x0011\x0007\x0007Ù\x001a,¥fi=¼\x000fÜÕ¤\x0017'ºlùpdË\x0011¶8ÇDSè\x0004h \x00139»\x0013\x0018èÐ@\x001e\x0011\x0003LÄÀ»?í\x001f?nÞÞ}Þ?ÜÉÄ{0×!¥\x0013Üp+´Ld\x0008W{ì¢Ü½úa{ýjóöüÝöòüyÔ£\x000eÔÑñÒã.ÎåS\x000f¼0ÜíÍâ7 V9jÕÚjb¼Îb\x000bè\x0004û\x0003¼·Õ!ñ u\x000eZwv;²qÔ\x0003\x0008µ\x0007Í¨«£@+Q\x001cµé@í#Jâ?PÄñaGn\x0010£¶=QÒ,MÆï\x0011#0o:)ã cü+=ÈÔµ0Þ>ýôôùËíæÅÓÿyªû\x0013µ¶£ÿc&`wÐWÐÕÁ¥íÍ\x000f7ïÞï6/n^þ·ç1C\x0019Ú1kÁ²]Ã<ôÁ£\x0001^YåU;f3jÎ\x0013ñ¥Oä/ÖTÉ_ÖaÖ9fÝ9F\x0014âF5XÞ¼$ãÆí\x000c#6í¦AS\x001f¬c¶\x0000äÂJ4âµùumÙ6c¶"°|)fð|O3J¶>ó¸\x000e³Ë1»vÌÀ û¢«\x001c?\x001cj±p\x001dfcöíeÍrTÀ!ò¿àxDÓ:;no\x001cshÇ¬8ÜcHÔ´7¼?è;Õ¢÷*ÌÙ¹\x000f®\x001d´UÔ­cSH¯7ø\x001d\x001a¶9d\x0019\x0006Ûã 5Iÿ8(8£
Í]¬1KZ|Y¹\x0008²=\x000eZkY7(¾ §ÎÂ¹J^½\x000es\x0011\x0006e{\x001cDÌ\x0005*3\x00021s\x001cUÝàu 8(Û\x0003¡>N\x0011è/ÍC<\x0002eÉqC\x0016P¶Â!ó)\x001aÿ	´d\x0015u+\x0016g¦Ö.B¡ì'F"èÄú|ðw&T§\x0019×.b¡ì\x0008JÎÃi\x001eG¦H*&X¦o1aàB\x0017±Pv\x0004CÇ½WÌ\x0017@6õ)ôu `(Û£¡A\x0019¶´á§pØÒÃò~(¢!´GÃ¸ÔDGÐÔ£+cà6iG\x000f[h(!t\
c0¤Í\x0011&ÿ$ºfÆ¼Xª\¹¼\x0013v\
NÊH\x001dBu<sØ\x001c¦F³\x000et\x0011
¡çV\x0018è±kõ¢Ü\x001fSþ\x0014Yù\x000e(¢!ô]\x000b9UÂñVz?HIq!\x001cp\x0008\x001d7CP<©fÃÚwTë`ë@\x0017á\x0010z®>%x¨îéjÈôÙñ\x001a6Îy\x0014á\x0010:Â¡\x000cén\x0008ë¤A'%F\x0018þC\x0011\x000f¡çr¨NfÒ{3T8HnÚÂâSàzÐE<Û¡¥\x001cdÐbÒìxQä\x000b@Vk\x0015hUÄCÕq;\x0004V:H¦Z
&i-û*ð:ÐEpQ\x001d7­o	ºðÓªÃOÇ;!\x0017ìôãä§ÁóµÅ+\x001e¨Âå©vg¢Ës¤ðf\x0014yçz4÷\x0018Y3Î{¨Â{¨vïÓW@ÁRiçdª Wß*V!ÖÅ)Ôí§P#\x001d6#\x0016ÿ;Í\x0012VËa©´.N¡n>zª&Í§0n\x0014¾\x001dÀ\x0016)È(Ðe
½ý\x0014âJ\x000b4.ðJóöPUJ¤U CYvì,ßÐßiÈ;.hàoZwÉ,Ï5ï\x0012AÔYÂz®·×yå1tÙÜR8\x0007"'-ø-ßêqEu-þô×§}Ö#Fþ~ù\x001dl\x001ba×Þv­}ð¤TãñÉÜrA5\x000e¬«²\x0007¯Ý6G+/Ó±ê\x0006úã¾1Ô%\x0012W]¥[ùBð+Ü¢\x000bø·\s¼]|Ïv±1\x0014	Ö\x000cøæ8UWu*cE¡Ó¡+uôÔ¯Tzêÿáéï\x0017\x001eîþ¼ÿp¢ò¹Ab5ï\x0013%á@\¦\x0008³¨/÷\x000f7Ü¼¸º<ÿíöeEù1C\x0019:0+ª)ÉÝ+ 4Ë\x0004\x0008[½á¬¬rÈª\x001d²e~8\x001cÍ4¬«I0îZud\x001ddCÖíñitÎ\x0006!h\x001e~Qæª¼0Õ"å:Ì&ÇlÚ1ûÔ\x0004\x00028oHË\x000c×Ù\x000cÜÍ6ÇlÛ1c\x0013¢­ax ]yCYw¼Û\x001b.ÇìZ1ã3\x0011ÍJx¤}kP\x0010£ç#X\x0015Í[Ùç}û:;É·\x001b0Lu\x0005Z
ötPÕà\9äCû:äúµJRy ð&zçjUu\x0015æÃSÿ\x0014QDÇ!Ôôô5)ÑÐ:\x0003?×ªFë:Èe\x0010lV g\x0018EAåè¹\x000e`\x001ec\x0011 v\\x0007º²9\x000cÆC(hêÂ\x0003°\\x000ehM-\x0015.ªÄé:ÐE\x001cÍ\x0010ß.¸þ¤t ú\x0013ÄtN¡\x0014Uu H(C¡ßì÷¡¥B[j<Å\x001eæíd\x0011	es(´Â[d1\x0016\x001aeçu¶"¡UÕøuH(Catw©¥\x0002EO,-4cÆ4a\x0014ä"\x0010ÊöH(à*²á¶³·t¹PUPZ¹\x0008²9\x0012Fog¸!\x0012ðQw^f#ùÙ\x000bß8."¡ì\x0008ødnÉqHÔU\x001d\x0007°®>®Â\x000cE$æH8qEÐ:{à¤?^ÍSÖ¿HÙº\x001es\x0011
¡#\x0014ªè,<¥\x001c1Ï-B:5½z=u\x001dèòBØ\x0011
±Ön)ïOD/x!ç¼q¾}=è"\x0014BG(	%ç$Úâ¼î\x001cVx
c¢:\x001b\x0005º\x0008+ÐsÃ¦îç=mHµ'fwÜ,ôÀsX8iè¸®Ð2Ç[\x0015É!Æ\x001cõ>á_¸ðvÐáí´àR\x0012ºh&5\x0011	ô°à­
Ç¡:\x001cGYâ°C+ÇgP\x000bßª,ËtA\x001f\x00165AC£r`ä°b«\x000f1§¶ê\x0014ÜâÃùùíþóÛ§Ç\x0013á"\x0011"Oö¡¸\x001a±TJ^ã\x0018\x001ak\x0011åíöÝûÝÍõóH!G
-H-&Ì°Â8\x0013\x0019KÃí@ØE6\x0002¨Êª¦%u.©ÑûIà}B*ømÙëEJûUHuT7!
XF0s HÅâFñ¶]\x000b\x0017'\x000359PÓ¶¤Ù
¤gþ¸¸¤Õ"\x001a²¤6GjÛÎ¥d'HÔ m
<²âµ\x001ar\Ôµ­©¤6×IüÙ\x0013Ñ®à·\x0005l°\x001bÔçH}\x001bÒK\x0003iF\x001fÅGßj=ód¤!G\x001aZË,)\x0010\x0013°ùä©G|úCUmrú¢
g\x0012Ý\x0000p¤#@é\x001eá±\x0015~\x0000Ô2>µ\x0005(«(=\x000c¨§)!\x0008à5]$jY\x0005µðû²Íñ\x001bîÏä½SFøjó"GÎ*¨?m\x000eUz4©\x001c\x001f©Iàf\x001aÜ½Z¸)Ùæ§°IVÕò7^o$5Ö»SOZ~Ùvü\x0015°\x001cf¼ÔhÚª:É¦ª!§
S\x0005m§*îOAß?8\x001aP\x0005/ªZz2Ô2íkÊûðû3V¨¿?\x000f\x0008\x0007U­ï\x000cµp\x0000Ðæ\x0000d&§§©s\x000cO\x00153Ùê,óÉPÌ\x000fÚR?¥ü6\x000e_\x0010TÃÃfAZø*hôU¯(J	6\x0010ÀÅÅà\x0017qVA-?hËþ@%2Aiiø7n\x0000nJ\x000f¶úºv2ÔÂ­B[UØOÂúr<}£bbôåÆx"ý¶ü/¦RD\x0006¦Pë²\x0015iÆT\x000cñ«eÝ|£æÞõ÷*¢bø\x000eÈ\x0017+\x001e¨ð8:"µ>\x0006ì[\x0001ÇpÅ<(\\x001bRiXÖjöôÛÕ1\Û\x000cW\x001dnØüÔô\x0000E¬0¤\x0016`óF´\x00190÷¡­\x0005,Y\x0012Qbw1/°N+<&ýj¡ycVèf½%|U%Ñ\x000faDv8é2ó¯©ÍÅ±¦5íXoûðåÓÝÃíæ¿ï¿|¹Ý?úpf|A<iX/ÀÊ
Idzù\x0015ù¶ï¯Î/wÿ¾}ÿ~·½©µû\x001dµÄ¬f×kAb=DÕ½%ZÀÛ\x0004=Ú\x0002[ ú-\x0000jäV©%Æ2'\x0003~Ñ\x0006èÜ\x0000=Â\x0000O\x0006\x0018FâL\x0018¾LÞt£Gz	Åèù}Ðº¤`*\x0016\x001dc³\x00056·À°À±\x0006«%Ù½ø	\x0012¯4,j4[àr\x000b\¿\x0005"\x001dbç+~dÀ¢BD³\x0001>7Àw\x001b\x0010ý='±Yw¢\x0001"ñªá(ä\x0016~\x000b\x0004f³\x0005.ùQs [\x001c}sV¹(×k>3DçJeVóA^|\x0013m¶ \x000cÆýÑ\x0018é*È\x0002áÎh\x0013iÖ\x00181O\x000bÍ\x0006\x0014Lö2ªyh\x0000ûRÃ¼°ÑÑ\x0007Yªrz`2\x0003Ói	$Ì!UJtÒ³°¿ë-ú(µÃ¹ùÖ\x0012ËÛ_ö\x000f\x001fïn\x001fOV¶6&Í<\x001aÃ\x0013\x0010Z¤9Íjñ\x000f\x0015·o¶¯â_ªh,3hÈAC\x0007hmÓÄI°LÆ­xè±9¯¬rÈª\x000f2\x001c¨Ö4¶û4?h\x00175O\x001aPë\x001cµnGí5·pa½\x0005N\x0012½]Î\x001b@\x001c´éÙÒöà¼¥t\x0006S­ji`%dC¶}!ÂÃ)LÇÐ-Ò±7 v9j×Z\x0001
y[Í-/*Ñ»ÚE¢ò\x0006Ð>\x0007í;¶4H,ÇÏ¾Ã³T\x001a@\x001aÏôÕY¤¨C:ô¸Ã LÆ§B\x001aT³)×zÔ²\x000c.=Ñ%¦YbÌÕIÄÆ³@GÌyÇ9=Y¸jÙå«¹äOs'Ê«t\x001a\x0017\x0005'\x001b`\x0017nOvø=\x001f\x0013YÞ#Þs\x0001ixµ}µ³ùDØÎ\x001dÕâ/0\x0001yùóí/w\x000fHáþþöñq?ÞnÞýåÓãS\x000bæ6Ýë¤
|3
ËÀËÅn´¯woÎ/Áýýîúz?î6ïÞ^]¿Þ\x000eÛ¡FØ¡\júQISrzEí\x0010äµ=vèÜ\x000e=À\x000e-ûÁL8\x0013ß/ø±\x001d\x0016_°{Ì0¹\x0019f\x0019\x0010oÛÀÛJR»?¶ò×ÐK.¨Ç\x000cá\x0001étèÄÆêRÏ\x001b,²\x0013ö\x0011r3Â\x00083pVº!\x0005uCó©N¯\x0016§j;Ì¥¯\x001aá¬pª\x001et\x000eU4¼
ò\x0003É"Áe\x001dÅá#N\x000cÅf°ù?\x0008pGUE	\x001eCã!G\x000fl±ã÷v+ÛÕ©C\x0013Ëâkk×ÆÊë	´¹ð7ýûKxÏÂIAêrvù â½q)÷÷_Û3Æ©qG¥so)\x001cÌÅæâ®Ø~l\x001ac\x000eµIpLñªªÅÒUß×ÉKç¯¿èÿ:`Yý\x0013C½ÔÜ¬¤R¨\x001fyÅè[fñ\x0017A¾ûëÓþñvóÛÇ}ü\x0007î>ã`ÀýÝíE8ãUÊ~c¦Î\x0003E XMBªEþ®w¿¿ÙÆ?ÿíõöòåÕù;\x000f¸8ßUpl\x0001ä\x0016@¿\x0005g)\x0015Ý9\x0000\x0004PêÅ!ìfø*¯ºáÇ]d\x0008~*s\x0017I¼~ðD¶ÔS;Í\x0016èÜ\x0002ÝoÁ4\x00043[`©\x0011
\x001bá¤^ln6Àä\x0006n\x0003PÃ\x001e\x000e\x0006Ìe¤ô6\x0016-X,26[`s\x000bl¿\x0005Q£\x0005n\x001d\x0010ýOú\x0006
^Í\x0016¸Ü\x0002×mA\ø¹óÓã³\x0006\x0011¶có\x000cY`\x0016ïMÍ\x0016øÜ\x0002ßm·|\x000c°3^÷4v©èÛl@È
\x0008½\x0006 ±äO\x0010Ò'à\x0012°\&Ìl5àð<9Å2ÑmÔÌÖÝô¾q \05Êf\x000bÊhÜ\x001dcÚYl'ñÉå7±f\x0013p,»ãqà;Þl\x0001U·MâcX\x0016k¶ È²;$ã6R|Q¼TòE£½©,B²ìÉ\x00135¹JÎHñQN\x0016,>Ô7[PÄdÙ\x001få)[-tÚG2¥\x0015Ë¬\Í&\x0014AYöGeïHÇ/ ¸c%F\x0004>ÌËÝ\x0006Í&\x0014QYöeË7Ð\;ÐsjdØ¥ªÅÞ³f\x0013°,ûã²IGA9Ç·NÀpL&,\x0016ÏM(\x0002³ìÌÞÈô\x0015äÉ~0L\x0015)ÁNP¡\x0008ÍÐ\x001d½6L§ Mg\x0001I]¦gQbªÙ"6Ã«r\x0012ÄÑ\x0004E&\x0000ËUHáP^ûïÊ\x0011(ßU¢à\x0003Í\x0005X\x0011\x0016\x001b¾× ø;AØï§'\x0014\x0018}³¸=±Üb°\x0018¦\x0012À2½®KãºëÕ
Ê¾Ù^îj%\x0016yDß¡\x00032Þ©B\x0014\x0014Í³J\x001ble®Ju®D­rÔª\x0007µC®Ñ¹J\x001fè%.¢f\x0006"oªZ+Që\x001cµî@-ÃLÆ\x0017¸£íaÂ5TV"69bÓXÃ¸\x0008P#­Iã"¶*>»\x0012µËQ»vÔSï-Ïçkò\x00115\x0013þû:îJÔ!G\x001dzv\x00071éNÓÚs\x0000öð,P\x0015)[Y\x000e¯ÇãÅË¥=­&NÏ	µåÒ`\x0010U"°\x000b÷!;üBvhzÁò,ëdu­÷\x0008;æ\x000b¥¯Æ\x0004#6/Þc+êÔ\x0011òòçOO·_¾Ü®id!¢Z¯\x0015þ87²P4z1ç\x001aBn6/_o±\x001duê
yùúêf÷þý®Ò\x001bÂ¦¨Ü\x00145Æ\x0010¡$S«ñßñm\x0013ªÝ\x0016Û¢ÇØâ-\x00179\x0003Ò\x0011ç±N-hu³v[Ln\x0019aËÄ+ÌR\x0015iñ|]¬Ý\x0016Ûb\x0007í±D¤\x0017S\x0003®YiÃ\ÔÆVç4Ûmq¹-nÌwé1ÉÛÔ0Êo(IüULñ¹)~ÌgÁ©= /\x0016¸\x001e­%ß{M5cn7%ä¦á_%ÂTÛ-ÌòÌC-ú´Æð\x0007E\x0017K.Û$¹6zJ_Å\x0018Y\x0018#}ÃÆXîÚÓ¹ºêÔùí¶\x0014Q_\x000e
ûR°\x000eW:ÕÞ\x0015s\x001b]%th7¦ûrPà·eQp\x001aÁòégr*£\x0017£ú)\x0002¿\x001c\x0013ùcä)\x000fþÌ\x0010HÂÈê+\x0019SD~9$ôÇó\x000fÉ/ã6\x0003Î.Sz)¿1EècbDË¢dÞ3.\x000f+\x0016R6Uõ·v[x)Ç\x0004Lï'Íí9'\x0013g©Zo9%«2d¶ÛR\x0004L9$b <wx0iÔKñILÎªó<­Æ@\x0011d`L\x001e,m2¬òÐS`é\x001e\x0003×>c
Ç\x000cc\x001c³ÙRÄÄwF:2Î²c*gd»1/1¾\x000c¿1Ï?°1_ÅAùÃÔß ÿb¿\x000c©ý\x0001ËÓ¨ú¤a³-Åñ1Ç\x001f\x0013KÞd:p2h\x0012æEº.cTqüÕ ã¯%¾TÌw²üÑO\x0013_e©²\x001e3èøTñ\x000exø\x000f\þnðÅ?ÆýãÉgËÏ0Û·ëO?Þ\ÝÓA\x0019$»[¬-+z"ó\x001d\x0017%ë*¯â¯®¯^W«{\x001arÔÐÚ§ú¯g]]¡x"\x0017IxÆV9hõ½,µÎQëïd©M\x000eÚ|/KmsÔöß}©Á\x001f9\x0010$Ï+Åu¯?}¼{8Ñ\x0003BLH¯ÇDg8q¥Nw\x0006%ªCÛ,\x001ey}õêüòyÔ£\x000eÔNqBmf\x0003&Ô§DãN9EiôDÔ*G­:P\x001bÅ4\x0015Æ1gÔ2¬*g­D­sÔºg¤A\x001dYº]\x001b¦ëR°ÈôÓÚä¨M\x0007j}Ø×a¢ÚP+b®ôõ\x001b×JÐ6\x0007mû@Ï3,ñ^"¨õ\x001dASÍ+¢\x001fÚå¨]\x000fjPÏ-¿3jncQ¦ª2º\x0012µÏQû\x000eÔXír-P´­ÓÐ òU5ª¨C:ô V$	gUHg\x0011 mÛ:§«ò©ÞÞ\x001a\x00045\x000by\x001b\x001d \x001d\x0019´\x0018º=¡\x0011\x000c\x000b\x001dZãÒ¾NE[\x0015ªr8+a\x0017¡QvÄF\x0019ÒK
£ri±aäj\x0017±Qö\x0004GaÒytf¤ò·Èâ0r\x0003ê"6ÊàD­3OB¼?j\x000e3ÊòÄ6Ur°à(;¢#vð¨»|~ÂÊ°þ®3»¯]\x0004\x001aÙ\x0011id\x0000|Ô`\x001bV
«ÍoB1\x0001\x001c¸µ\x000b-;6Î§Ú\x0019ÔL@\x0015a3ï\x0011Õwìu°¡ðÐáÿ¤w\èw3Käð ýtU\x001f7¦êCcêïî±¨ót÷ùdÐ.¨ôlè\x0004±jÇû\x0018·¥ÄÄ»v\x000bûÝÍ\x0005\x0016rnÎß\x0019rÌÐ\x0019£\x000b?¨	VÔ!°²|<5ß·\x000e³Ê1«öu6I\x001b+4ã(Á\x001dÚ²j\x001ed\x001dfcÖíë<»ºyC\x001b[Áh®ÅºõMÙ´¯3ZÈôrD¯àÂk®¶ªÅYõm\x000eÙ¶/³\x0004n©pÞ\x0013í\x000c×.¬åÂìrÌ®\x001ds¼#¦§Ä%LZÕ.ëu}Ù·c\x0016×ÎKNô\x0002p7¡\x000eUuuC9´c¶.5B\x0008M:- $ÏÎjµi\x0015äÃõe(¢\x0019³¡á\x001cð¨Då\x0013Zd\x001fÅ\x0013YÆÀö h\x000f}\x0000ñÿ¨Q43\x0010ó¼q  (Û£ RòÌPI/ífc\x0014\x0017lªMáë \x00171P¶\x0007A,i\x0006fÁ¥Ý¼Ì¶\x001et\x0011\x0004e{\x0014a3$g¹\x0017IzËò3Ú
ÜÑ{\x001dþYRm}ruT÷\x0008GJt°ÃÂ \x0014§\x0010ÚO¡ñ6í\x000el3 Ý!x6Cûê{ü:ÐÅö-\x001d\x0013\x0014TEfÔiwx\x001e\x0017Ð,:ë1\x0017\x0003Ú7ÑñREy
3Ñô»\x001e«5ÓuQ° //*¬õÒÛYK¼e¨Ã}\x0001RëÔ¯Uí=]÷ÿéKùiOIã\x001d:æ\x0012)\x0008&eþã<uDýç\x0012õQ#Y>e¥X_{°¤dÂíºÞîÚmQvÍÛ\x0005vZcÃ¦\x000bMG\x0012ppÛà«d¿k\x0017üc¹à\x001faÇë7pædI\x001c(îî\x0014gÆ\x0019aÊÍm:6·JïF8a\x000cT?`!ÑxW\x001cwETú±\ë\x001fÛ=H\x001dF X\x0000ë|M¬6å¬¬z\x001cïnèÚÝàHaØ#ÉD`wÂy	U®µ+~[®ømÏóî¶\x0001Õhæ\x0015×É\x000c\x0011õ\x0012õöªã§:¬\x00109T*Õ\x001eµòÇòP¶oïoz(÷åbïÛ\x0017Û0\x0019²âÛpã¶)Q\x000eÔµ2\x001b/¥t©W¹Ê\x001b^Àþ×Ânö¸\x0007Î\x001ezà®î#ªÛÇüñöññÔF>\x001d\x0004`zj¾ÑÝN5'g:êÑæêbú-þòÝîúºÖÁg{áì¡\x0017®\x0015½wL(<	ê\x0019¼QI»´ºä
àU\x000e^u÷<\x000e\x0016`Aë>0k­s^çèu/zÆ£\x0013W\x0008L.\x0015êÝ¬
àm\x000eÞv\x000fPÜõ\x0001¹v'ð\x000e\x0018½©¶æ4 ÷9zß^§ú+Ò®w6\x000bWG"×?\x0014\x0004'#:=N¢%\x000b ¹A]¤Ñ¢>cá\x0017\x001eGvºo\x000f¿8µ²óØè'µ%ø©¶"\x0004Slú*)@\x0003úâØÊÎsûÍÑ\x0017ÇVvÛo>º2Q@ß@Â»»_>= ÄÈæÅíþéoîNÔ¬j¶tV1¿1sëh°\x0002\x000b_\x001d_zwþæêrúÝÝöæ\x000fWç\x0015Á]Æ\x000f9~èÆ/H§m"\x0012ü©3ªê5[à«\x001c¾úþ_çøu/~\x001cÞ)&õ]O%f\x0011õëj\x000b~ã7½ø}à#ÒÁ\x0018`U ±L\x000fÝ
ßæðm7|Mï\x0000
«ó¸^\x000cZW¿Ú×\x0002ßåð]/üxé=\x0018Hø\x0015×Äði0~ã÷Ýø%\x0016|§õOz\x0011\x0007QgPk\x001frø¡\x001b>p·\x001e¨DÌ-ø¡ ~ìÁ¾órN¡KtâwB²ÂÞ$¥3ßÍ¶\x0014yãÿÞàõeìí\x000e¾AÐ\x001b/\x001c\x0004k¢\x0017±©gk0þ"öÊîà\x001b\x0002S\x0000L4õó\x0007Pl@¨\x000b·\x0018PD_Ù\x001d~½çìAÎav 4Ìá­>¤¶\x0018P_Ù\x001b\x0010,Æ\x0017×zåâO\x0014\x0001\Äµì³Å"þÊþ\x0000\x000cÌ¤,­ÃëûÜ\x0001C¯9.,\x000bg·\x001aPD`Ù\x001dc\x000c ÝZi%`Þ?ªZ@nA_\x0004`Ù\x001dQTp\x0006\x0013æþã\x0003\x000c£ó\x001fY\x0004`Ù\x001b\x0004lÙ\x000cú@pµÍùP!k1 \x0008Á²?\x0006\x0007®åËt{\x0007jVhÀà/\x0000E\x0010î \x000cé\x0000\x000b\x0017dE\x0010M¨ó¶ÚnÐ\x0002¿\x0008ÁÐ\x001bHTD\x0012\x001d(0Ï\x0006øÑ\x000e\x0014\x0010\x0006½!ÌÉ4#c2\x0015aeà/\x0000C\x0018\x0014!\x000cºCØ¡k,\x0006\x0017\x001a^\x0005\x0011¨EÝE³\x0006ûP(B\x0018ô0\x001c\x0019±ô\x0005föpá\x000c\x001b «ýê-\x0006\x0014!\x000czC\x0018~¹\x0005\x000eysYRBÐËs¾:#Ð¿\x0008bÐ\x001bÄ\x001cø3Þ@À\x001cúÑ\x0019\x0019Þ@U&Ú\x0016üE\x000cÞ\x0018øçk0j²3OpÄ æðÁ·àBDoº	sÏBG$ó,\x0004ÞrGQd|\x001b6Õ\x0007Þ\x00163äáI}®þøÝUãl¡ÿ7¸®«¨E\x000eIE*5g¥ô4ýï\x000c.*\x001eo(=`C4&µÅÙ-ÉàBX\x0014ëißPûrCí¿»
%\x000f\x001dk³	\x001f¿;\x0013àx3ÁÍ4éDó3æQ§$-QePi;\x0011G\x0007[\x000f8Øÿ\x0015'âC¹>|wÛÉ\x001f	ßÿ%Pto\x0006«RáZó¸yF\x0007£Ca\x0007\x001cCK¾Bm7¾þ3u©ð+kÍ°âH 6þ\x001f/ªìÍ?ÿñyÿðÓÉTe\x0016Enæ\x0007{!\x001c&À´NÔy×vï6ovï¶?TßÅ&,\x001eÐ
Ö\x0011t vå\x0008\x0007¶¨¯\x0002­rÐª\x0003´N\x001a1qOO|ÞÐ&q²Î=¸
´ÎAëDa\x001fA\x0007"²Äía\x0018tõ]r\x001dh6=+Í\Ah\x0006)ksÕ1ÑumØöBÞ\x001b\x001aÒ\x0008q\x001a~pËòeëA»\x001c´ë\x0000\x001dC$×aP`*$§«Ùñ:Ì>Çì{¶\x0006·¡"Ù[üL:åtu²n\x001dæc\x000e=ë¬Q²{Âì\x0014É{à8 {»eÅÓÕ ³f6+¢g¥\x0005	©M¨çk,æX*¡\x001e¶Ô²=á\x0010ÜÜð+<vÏÎY\x0015oéê´ö:ÈE,=ÁP©ä¢È¶\x0007/tµðº\x000et\x0011\x000beO0\x0004Á.Zâ?
1\x001a`'\x001dªEu¨`({¢aÛ¤ÞP¼e~\x001bW'÷Zº²'\x001cÊt\x0012¥40ªX´ÚË:çù*ÔED=!Q\x001aTfQ\x001bÔªgs\x0010\x0018µa¡.B¢ì80@û\x001a©L(Cà&FU\x001d_º\x0008²'*¢z0íkÃ
,qèºÎ$½
u\x0011\x0016eG\4ÁÑRÛ@\x000fq©F\x001dö¯\x000c\x0002
EX°h§w² ñ\Hê6ubøU ¨\x0008\x001dQÑ\x0004I¼^!rÉl1Þ\x000cKô ¼"vEã\x00035e\x00054S´Ð9
cN=,k".BG\D*TöÕ\x00115Q\x0005f( û÷4cÍV1QcÿòýçÏ·wûû¿í?~zÜ¼ÚßßÛM\x0004SSó¶M´A0eEô%Keó7o·ïÞí6ï¶\x0017Ø¾ººÞ¼Ú^?\x001erôÐÞ\x000b¢é\x0007Ñ§[\x0001f\x000e3z¹HyÓ^åèU/zÃ§\x0013LÞ[ø4®³479xÓ\x000b\x001eXÑ5tK\x0010L\x001aµ¥V×æ\x0010Î$B¸7ûÇ¿Gü/ö¿ÜÝ\x0006|\x0016÷óÔ/\x00008q¤'Q,n:ôÕôäÍöú\x0011ûí»÷ç»çAC\x000e\x001az@kªÞ¸S,\x000by\x00015yWÍNVV9hÕ\x000cÚà[.µ§
«¼¥J¨uµ¹p%j£Ö\x001d¨`²$DMÏ¸ZXP×âÏJÔ&Gm:P[&Ä\x0011æ X)`jµàm\x000eÙv@Ö2õ½Ô¶ ¬ãÖµº¦ËJÔ.GízP\x0003/´6\x0019hÇ «ò¹+Aû\x001c´ï\x0000-Ù\x0019¥\x0010Ip
<wøjr%ê£\x000e\x001d¨ñÖN'Q\x000bnåé\x0002çaàAÌØáÌ\x001d®	µH
rR9özX¢Ý}\x000fC]\x0006Åö¨\x0018×Z%_­-[\x0003_$ã¶®R*¬D]DEÙ\x001e\x0016
2\x0010I´Ä§%BÍÒ.¨ªZßJØE\=Qrâç§Â0ë¿¥Åº0ßJØE=1FxªìÄ,Dók©\x0002vð®z\	»pØ²Çc\x000bÉ\Rzæ;#µHWû+WÂ.ìð~Ó8<5æÆHÉ'Çj\x001dÞèÁÂ@#W]ÞÛ2^(-	µ\x0005n\x0006
º:´\x0012vq$¡ãHzT5!O\x0012¯òó\x0004+ØkWÛcVÆÇ\x000eÌät`\x0003.4.üúB3dÃñ5\x000còâÃ\x001b$w¹ßüîÓÓÏû·û§\x0013\x0017^ÇhÃíó¨»1\x0017N,\x000b{ÆÌuì/Ñ»Íï®n^o/_í¶7Ï[\x0001¹\x00150À
p<\x0008)GöÁÉ
w»¾Ã
[¡FX¡\x000f	W\x0013±6°\x0015ËÂ\x001c\x001dVèÜ
=À,L)àçm«=\x0007X¼áwXar+Ì\x0008+ô\x0019m¨èýµ'#ÒN-Ö;°¹\x0011¶ß\x0008\x0015c\x0018g(
=¿ªØ4^èa1­ì°ÂåV¸\x0011VÈ3 tM9b¸Vèô-\x0016§´\x001b¬°òåÂJh\x0014ÛÜÿßÿýâÿ]=ÞNj/>ÝX¢¶
,
Û:ç¹ä\x0003÷ºi_éÞm.6W×»\x001dª\¾¸:¯²\x001cñ\ \x00050Ä\x0002ÔU\MDFûLkÂj\x0013Tn\x001aaÒü\x0011<M!\x0008~fÔõi«\x0006\x000btn\x001eaT<oåÒC\x0018x/	Õ\©Á\x0004`F ¹9n¢Öó È«sç
&ØÜ\x0004;Â\x0004+Ïø$Lµ\x0005Ú¦mT÷]mË
pC\x000cHÔ\x0017È.fw\x001açtxæ\x0011xµ\x0005>·À°ÀYV>~óî`¹éH*çg	!7!|\x001f¡lÃ\x0002_}¾\x0017§¤û¸uêã~»ÿòx÷ánÞ~z8\x0015¸ÄsÌãÿ¬·
Öf×åZT~»}}þò¿mÞ^]\x0019rÌÐÙ§ó¸¢7^vs¡ú@¿\x000e²Ê!«vÈ1÷¡ª\x0004ÒDPÙ>n@fYpP;«ë0ë\x001c³îXfÝSsI" ËÅ¼5¸¶iªîe\x001ddC6ÍEjñ¨\x0016FÀÆ\x000bÊ(µ×umÙ¶/³\x0011gFYd\x001aþµÇ¯«ÖÙÖav9f×¾ÎØ9`i%Ë\x0013a\x0013,¯suâz\x001dfcöíë_ibZbÁ\x000e°,¿ëêìëð\x001coh_cãøÖ'I{\x00194»\x000c\x0008ÃÖ8ëÞÖîíEVÑg\x0010!ç·§xSå±,YÕSZ¹í!\x0010\x001fI\x000eQj]ÜÓBK^Ìj¯
ë0\x0017\x0011Pv@àçvô\x0019¼Ì·ÊU:ÖA.¢ì\x0008'R°\x000c\x001b\x0008ÁoeØ8ÀTOãâ,|³lwÎÂ{ä´\x001dgz\x001bc­M\x0001eÜJ\x0017N¶{:\x0011"Ò\x0002NÑÀ\x0018\x0018e\x0012¥\x001ev
¡ð\x001cÐî9\x0004v=3\x0013RàÊ9ðP©jÑ:Ðe"Ú~\x000c\x00053gáì\x00159hÞlÆù:(\x000e!´\x001fB\x001ckË?\x0012X \x000c0§È~ÌZë£\x001a­IÓýãþÿßo\x001fOE$kfîmM#ËJ4|\x0015ª¢Ssëöz{þòõîú\x0004Üã.ÜJ\x0013¹i\x0010Ø\x001e/gàuïªR\x0003­\x0005®ràªoÁ}ê\x0016@¤LJËÀ+^×u_\x000b\çÀõw´â6\x0007nû\x000b\x0010:<}©è¨y³z?\;ä¸CßNqL¾-"Ðù&\x0010w
k\x0005\x000fÅ-KÒçS¾åËâhÊ¾³ùM\x000b{Tf¿ÈøÛÇw§`N%*Ï°¦\x0012«Z¸:Í0b~±»~u^:\x000c\x0018rÀÐ\x000cX1+]À7\Ë
?Ü^î z)XXåUû\x0012K²O\x00078Ä|ªVU"ÆUuX·#¶¬·!Lz\x0005\x0011é\x0011Á©ê-f\x0015b#6Íã]Kó@µäë­p×ø"ï
À6\x0007lÛ\x0001\x0007"\x000bÂ¦Ö3#\x0006\x0004øÙ©±\x0011»\x001c±kF,\x000ed\x0017Þ1¢cOa«è«\x0000û\x001c°o_b '\x0008X%îA±·Ï<å­\x0000\x001crÀ¡}\x000fóõØ¾J+ÌbÎU9Ó×\x0000>T¦à!Ú\x0011sVDÞ(âNÓÓÕæàUËx×\x001cð&bqJ AñÛ\¼.ò`l¼\D<Ù\x001cò\x0008×Ó¬¦4)H\x001bõt¡Ú\x0014¼
r\x0011òdsÌ³1Å§ä\x0013G½?_0«X¼ ²y²9èÙÀ£é\x0012=ó¼ÄiJSVÛÅWá-"l\x000eyV39lÀÚ®%\x0008à\x0000xnÀûdÄEÈÍ1Ï:^(ÈÁ)Á\x0002ªÎ« \x0017!D6Ç\x0010k\x0001qÎ'Z­y\x001f\x0004ùY\x0016S!Cá¡Ù'#)ä}q\x0010\x0013÷Ü
\x0015Þs\x0015g!«ã;:ÜA^ß><Þm^ì\x001f|úüùÔNe\x000f\x0001å§¡Ñ|Îr£Êp\x0007\x001ayV0¿Þ]^o^l¯_Ü¼{WéTVÇ7\x0011u¸´Á\x000bÌ²z¸=æúI»#T\x001f5`ØÜþò¸\x000c[å°U\x000flÉ*ày~@!å\x001dOv\l£Ö]
|½\x0006£¨â\x001f÷\x0008'\x001bAT¹|Öâ69nÓµÚúg¹\x0005f¤ój¤^XóÓkQÛ\x001cµí:z\x000c\x0002r\x0016ë\x0019µã:c¨»®írØ®\x0007¶`Âî ¤gØÆòÖ¶Õ\x0010³\x0016¶Ïaû®ÕId1xuP(±Ë¤Êý¹\x0016wÈq®åN´Ø;çyq½Yç)¸jÞ´\x0012÷áÚ¢²kKã¡ä\x0011ãèíxn>Jà\x0005¯÷v¬\x0005^\x0006Ê®H)\x0014\x0013[¨è\x0010W\\x001e×2ëµÀP)»b¥0$ß\x001e4i[×å<Ö\x0002/Âì;ÇþÃÔ\x0015Iq
!zGS\x0016\x000e\öxp\x001749*\x000f)^*\x0012	\x0002ªÝxk\x0017.\öøp\x0017ãô	¸¤-Î³!\x0008¼V\x0008Y\x000b¼pâ²Ç»D\x001aTlDp\x0016W.8A¨jcÐZà\x0017=nÜyÅÁ^ù@óôqÅ©o3\x0002\x0017\x0003CáÆ¡Çã¨\x0004\x0011åhi©E/\x0002§ú \x001e¸U pãÐãÆ§Þ|ZñàË*\x0002§C\ñ*ÅÅZàå§Ç;§ptwZqÅtxÑ¡\x0003\x001fN7t«\x0014w\x001eè¹ôÄ«1¾½LÀ\x0016pÓÐt\x0010º:\x0018±\x0016wq{ës,å\x0018·¸?óä
y0\x0008IoG\x0002/Ü8t¹që8§ÕàSÅ5À ìÀ¸	3.gDv¸'\x000e\x0006¥\x0003ûBW-]®Ä­
¢º\	L¯©µ£\x001afÄ­y£ø*ÓÜZàe5¢ëdb\x0013íì\x000bµ¡GsO\x0013WA*mÎZÔÅ¹T]ç2&±ìOâNç×~¯hHQ}:_\x000b¼8ªë\j{F¸±ú3û\x0013í¨/$HY\»8ªë\"ýô;¨ÔkfIX"H¨öN®Ä­s©»Î%ªªÌþÄÄË£\x0005·D\x0010\x001aäòÀvËÝ¾àë²<HÕxS\x000e\x001c "Å¥	&e
0r¿\x0008w\x000cßõÂ\x0007\x001aâ(*+V©TY\x0019¸mÊ1¶¹¼Ü\x0007?æX.\x00155\x0017	ü¶ÐÕõ¬cô¾\x0013}Ä\x000cÊC^|â¿þ­êh\x001fÁÇ!ý¿ü
»óG,ñ\x0017ø\x0016±ýÛí\x0003= üáîöááTÂV\x001b}8Ï\x0000[áI?\x0005\x0002\x0018ªi)µX\x001fßþawIo(ñ¯\^Ö8[\x00197ä¸¡\x0007wÌ[ìÜ\n<7üA\x000c©ô\x001a¡ä¢\x0012B\x000bnãÖ\x001d¸µP<\x001afÂ$4áæwL\x0005°´Å[`Û\x001c¶ím\x000e°=\x0011+ª©\x0010B¸ÕÒÞnÁísÜ¾\x000b·#½{zuqs\x0003Ý2[\x0003ìLÖÞÏäy\x001d¸\x0003Ó\x0001Y!HÒ>âæîJµ\x001cÿ[\x0017ÇRöKÔñ6L×\x0015HÅU)¤åâE¨\x0005xq.e×ÁÄC­ô¬TiÁ\x0017)ä[p\x0017\x0007SvLi)áò\x0013y¿'à¬3 F:\x0014Y\x001cLÙs2
^#æ\x0019\x0010\x0013ßó\x000e\x0007ÉÏÉ\x0010\x0016éZ\x0002xè\x0001î\x001cïi+Pêt\x0002®$\x0001aQ7¨\x00018\x0014>\x0005z|1\Ì!Óáàì\x0004\°úG´`àÑ"E\x001cÅ8Aµ\x0015\x001fÿv1R¦\x0015GáÃqÀË\x001c¥Ç\x0019Æ{\x0003s(ë\x0018ì©|\x0008,\x0000Ëê-¸U[uM>Zj~L\x0001I38\x0008<rÁ\x000b'\x000e=NÜÄ\x0003é%M\x0016M[Ü\x0013p\x0010\ò-ÀM\x0001Ütíly\x0008\yuæi+Þ*\x0012\x0016_h[\x0017á\x0007zÂ1zÆ¼FÞBZp\x0000vz$nWàv=¸½aò\x000eÃ©´à{ ¥\\x001c\x0003n\x0001^ÄMèF0\x001fªFqÀyÇu¦L\z\x0018¹Å¸	]q3Þ\x001bÔ<Ã¬LL\x0012çJs¼hÒí^E)Æ\x0006àªª+n"¼\x00198ò[ÎùqÅSø±e\x0016àEÜT=q\x0013/ôp\x0010;\x0016t8H²®\x0003/?ª\x0008ª+lÆ\x0003M$±T\x0016\x0015ä¥\x0019\x00197U\x00117UOÜD}5ºmÆ\x000c_!X\x001656#)ªª+nâ£\x0004E\x001fÃ@ \x0004/8,\x000ec´à.¢ê>Öü²B2&Cy
WÜ¤\x001cyKV\x0013W]NÜñ¸ªÇ\x0002 \x0005\x0007¾üE\x001e\x0006ÜºpºË\x0015zËW\x0008ìÇò\x00144ù\x0006!<\x000cöºð(ºË£|«cR4:Å·÷÷3ÛÛýãÍþé?7Wwoã\x001fO}T\x001e½÷TYÖfbV<¸:é\x0019/À¿¸éÜÞn¯_n¶7ÿcsuþn\x0017ÿø¼\x0015[\x0001\x0003¬\x0000Æ-q<%£¸`\x001b¦ÿÁá6¨Ü\x00065âK\x0008¢\x000e*^0¨!Qáþ¸e-Ê\x000e+tn\x001eñ%\x0004=*ç¸_«ÀFÀ"Ù^\x0011&7Â\x000c0"FXIÍÏÈ;I\x0013ÿ©\x0001`Y±­Ã\x0008\x001baGì'ÉzÎØD'·àÐý§ÅbÙ±Ý
[áú­°\x0010\x0003Q©iT\x0005Ç\x001bÊ¨¯`Ï­ð#6\x0014ðDª\x0006HßBºÔÂ³H^ßaEÈ­\x0008\x0003¾\x0005J°\x0015üÀ¤tjµ[.¿7ÛÑ¶ÁÜ©Þoaþ\x0014¢\x001flãnÞe%¯\x000e3Ê°= nÛyàhîõ\x0011\x001c-÷|.¹Æ;Ì(â¶\x001c\x0010¸ñxsS\x001e*\x0005>ÞÜ$¶Ì\x0013Ý`¶ÇBÖ
\x001bOw\x001fn77_\x001eïîï?fC¼à8þ\x00148(¨g}
Ï\x0015Íx§|ÿæúüånsóþúüââêy\x0003 7\x0000º
ÀKñAx\x0017È\x0000Ã\x0003a~¼\x0001*7@u\x001bÓ¥,®ÎæÞ7 <>¿8?ØlÎ-Ðý{{\x000eâ\x001e²DG\x0015÷\x0010¤M´X\x0008j¶Àæ\x0016Ø~\x000b$\x0007jä¨Ud	LÄá\x00179Ñ\x00000²<Æñ\x0017<5»ûå}ü[ï7¯oïâO\x000f'ú!\x0014Â\x0003Äù¹»ÉIîUñvñ\x001a
6»7o¶ñ*w±y½;?]>\x001drìÐÝ&Ýì\x0018\x0015¤"ì:©}WgÇÖcW9vÕ=^õi&\x0008±Ïª>Ê\x0001×ã"öZ×êzì:Ç®;±\x000b\x001eÄBix\x000b´î<ÚÄ¥C±\x001c»éÄNJÚÑõÏÊ7qÑ]b<Z'âzà6\x0007n;K¾%K¬Wð'?9vÉ]Üõ.9wg\x001f¨1âª{æÑY~ÜoÃîsì¾\x000b;Ò
Ð1×
.\x001b/hÙmuVr=ôC\x000fÞÑ0ó\x0004 !(möÔ}ã««¡Ë2(õF¥o]Ø?ýXÔ\x001f»Ð£$.g\x0004çVl`*1[íwnA¿/Ñï{£*1iÈ¸å=¯=$Ðêà~Ãq-áû>øßúÄúrëøÎ­ó­\x0016_\x001b]ÖøL$ü§§ÛÇ»/·WOûycÃîø\x0005\x001cÅPg-3\x0016øC&À
ò7Ûë\x001fnv×çïñf{½­ñn\x0012r#wß\x0013ò#\x000fÈ
Ó\x0000Î)ÌÀ%\x0013kûçTs×!Ï¬õo2%ë&è2$Ý\x0014`]y\x0019\x000eTæá\x0019]ÔØe]~G\x001b&\x0017µÖ¹¨uÛ²'\x001d\x0010jqÙ57\x0013ûÅêx\x001bxUWë.ÏXÎA Å]$"y\x0018\x000b]\x0017Ðuçº$Eá<¶\x0002ÎëN£ý.êôÙzðg½®]Pí8^\x000cM´H\x001c\x0008%ð¢ª-¸\x001e¼-ÀÛÎW<#©Bh\-ÖøÚ\x0017aIöÆ%Í{F8Kí]\x0012	\x0011gðÞ.¾\x0001µ÷\x0005xß¹ìÀ\x001dÆÈàHZ¹\x0005c\x001cÖ\x000e/Âªì«R²¢0:mx¬.««e±Õà¡¬Ð\x001bYèO¼Dy\x0005\x0006¯\x0018¼¯\x0012ø­\x0007_Vè\x000c­Ò%]_e)\x0003à\x0003ëX@5\x0003^\x000f¾\x0008®Ð\x001b\'Öv>°<ðÊÛji=ø"¸Bgp\x00122!'Ý÷	<¯{ma=ô"¸BgpUw¼P!åcÚ²2TÕ{×/+t\x0006WT-À£V\x0019èbó19Ê\x0018]Çn"¸BgpM¢Ã"ÑnÊ`#ÔòóM\x001bö"¼BgxUÆ¼ð?¤(\x0012Áó
ÄMj ®Ð\x0019]¡î;\x0017¬:£³êhæuÒä\x001azgU2\x0007¢WTæø.îO\x0011ü\x0012üï
üÇ\x0012üÇï
ü¾\x0004¿ÿ®Àßào¿\x0003ðñà\x001fõËJ·z||i>
Û{|YEØ1g©X¡HBÑGWÿ\Ä«IææÕó¨!G
\x001d¨¦&vÜ÷¤¢YºÈ,?ô5V9hÕ\x000e\x001aå\x000c+Më¹û\x0012aa\x0001\x001d\x0016+3
 u\x000eZ÷¬´åù\x000cç\x0004ÊÎKÍ¯\x001dÚ/
}7 69jÓ±Ôñ~7s£²\x000b/u"°Ön±\x0018Ó\x0000Úæ m\x000fh`Â\x0008g\x0005y\x0010\x0010iöH;»ÔLÙÚå¨]\x0007jd&&-{mÓ\x0012\x0007V·4\x0017
¨C:tn\x0010:Ê\x0010É\x0005î\x0010Fmô¿n@-KízIKí$ð\x0007îD©\x001d\x0002¿Ü:¼\x0002»>¦ð×\x0007
î¤ºþô´<\x0019µWXâP{Mé8\x000eHS;ñÏäãs\x0017ÕõÕÍöú\x0004Üã\x000eÜH¨\x001cæ
\x001e¤a\x000f(\x0003©©{»Ü\x0007Ù[å¸UÏzO\x001dþ3lEÍ013áù\x001d+«¬bkaë\x001c¶îZnÏóèñlÍN\x0010fØ~qÐ¢\x0005¶Éa®ÕÖÄdý¬ù-½âwiµH¸ÐÛæ¸m×r\x0007Ò\Amä×ÛðîöUöêµ¸]Ûu­w s\x001f,?Y \x0015
¥vyò \x0005·Ïqû®õ¶g$º©*q¹Y\x000f+ûq¨³÷Ü\x000eÿß\x001fváºeïþ°\x000b\x0017(û|à7]lmù½ìí\x0007R\x0017<Í\x000eE\x001f\x000cÄ\x0011\x0001©×ÂÛ:Íì©è%\x001c]ß%×÷ÛÍË÷\x000f_n\x001foï~z8FÑr«±\x000bÜLMEÜjü|:\x0018ñz{ù>þÅó\x001f.+<\x000c\x001frøÐ
ß&9Q\x0019\x000cO)\x001a½\x0019¬-P¹\x0005ªß4$\x0010S\x0015¼YL\x0016\x0018Úì\x0017©\x0015-Ð¹\x0005ºÛ\x0002\x0008I`\x0006;Óf\x0003x4Ô{·xx
0¹\x0001¦ß\x0000¾=\x0007P\x0001Çf&\x000b\x0004\x000b¦¢ÔÌh\x000blní¶ ÞÿI¹\x0005ðE¨\x0019\x0002\x0013\x001a¡¦Òh\x000b\në·ÀQî\x001e ~\x000e\x001ajÀ­à8:0Ú\x0002[àûwaå3¡pG¤3gÍp\x0003Bn@è6\x0000¥\x001eI¨2^I<Yp\x0018ø1"h­\x0016\x001cÒÌ)n\x0013\x001fç~&~àÉ\x0004f!ô"#Y³	e<î\x000fÈVRU=¦
YVULX¦±k\x0007yB4Ç¢ÈÔ¸ô\x0019$§
\x0014×@ªñN\x0015ÌQÁ)þ\x0002S£?ßþr÷øïÿïÿþ?»/ûNLé@)¤#d¼§\x0012Ô¿0~	ýË×»7çøç\x0017Ýûíå\x000fÏã\x001c7ôáfAx¤ôäk-¹ \x0016G \x001b`«\x001c¶êÓ?ó\x001c´âæ\x0018ìo Ôrqä¹\x0001¶Îaë.ØÎ»ñ`ñ\x000e°ækÐr©pÓ\x0000Ûä°M\x0017l!ÏÜ\p\x0002\x001cØ£åN{D,vf4À¶9lÛ\x0005ÛHj(\x0001ã¸kð¥	µX¶iírØ®\x0007¶@ibzÜ
gzÖÌ\x0005a¸Í\x0014y;Áö9lßµÚ øÉ\x0011´¦i\x0019	VñrËÅ.ü\x0006Ü!Ç\x001dº\x001bõi¨Ý\x0010µ§\x0008\x001b'fòa°\x000féË\x0014pD\x0017n?µ4ÎC\x000f,&\x0011cqòbñµt=pS¸nÓã»µw\x001f9¬å)w\x0011\x0014ÐêÅªû¯qÿk\x0019\x0014Þó4e\x000eñøh\x0019¯«Üxá\x0002éìÄXÉº\x0017
;\þ)æO%xüEÇ\x0001µ±Ñ\x001fH»\x0002ÎP\x001c°_;Ê¬â/ò¢ÓËý/w÷÷ñ÷û§·÷§®{\ìÙ%â¥in\x001cÚkº*©EòwÎ\x000c_nß_\Ä?^lo^í.Ç\x000f9~èÆ\x001f,ù&\x0003¤:ósÃ\x000ezz2À<Û±Ú\x0002[ FXà\x001fô¿°à¹;Æéøåñ\x000eé1x{ÿãíã\x00174áéTnA\x0001I\x0019Fêt0X¯\x0015ÕJñöâÅîú=¿©4J1dÈ!C;d$#:á¸ù\x0015Ø(fm^¼I¬G¬rÄª\x001d1\x0006|\x0002\x001c¨\x0004\x0006RQµJ±\x000e±Î\x0011ëvÄ.)¦I==ºO­ä\x0012¬5J¯lrÈ¦\x001d2J2Ð@¯eÞ]0Ücì\x00179·Ö#¶9bÛ\x0018	¶è¹ æâ3qm=:±{T§GÖav9f×qø,Î+ÌE-ýh\x0013fÍaÒÛª¦è:Ì>Çì;6³¡õ¸3Tr\x0018Ör-TUç£Öa\x000e9æÐá2\x001csÈá¸±f*onÔx5æCÚ=ÿØu\x0004\x0015-4¶\x0018Ñæ06±|Ue¬×.¢ì	'ºæ\x0002àÐ+¹:}àeªG¯\x0003]¸gÙáM\x0012:\x0007ìú£Vòáþè\x0006-ÕQÜ¿(\x0018?Ç4éöóý©LÆÆhz\x001cS¯L£¹^¥ÆÛe\x001e©C\x0011ó]Lvï.jTÆÜæÈm\x0017r|\x0018¥\x00145º\x0013AÜcý^äÿ]\x0005\x001c[ýàÐê·û2±Fo^}º¿ýr"l
9Ô\x0003@J\ÒiæF·Ë=å\x0013ËÅû4zóêêb÷þyÔ*G­zP\x0007n	
H¡O Iâ\x001cï\x0008ã0\x001c³éÀ<
O=a\x0012Î@\x001b¾ûE}\x0006Ð.\x0007íz@\x0007$ãFPC+møÍÅk\x0003ê£\x000e\x001d¨cl¡z«woê»@MÕõ­Ã,ËØq\x0012cèfþ\x0010§<©)Ihè´YdÍo]DÙq\x0014¿
l{ìöìÁí½Ý?Ý£³~<\x0015³ÕÑAspû^ï¥`²Ñ\x0000U\x001a´·Û\x000bôÔ×§ \x001c14#öt\x0007#6Íæ\x0012¤fÄÕs¸
±Ê\x0011«VÄF\x0008*ÙÄ5viÓ= ¨êüõ*Ä:G¬Û\x0011;zÄåü\x001c/
ÓUú¸û*Ä&Gl\x0011ÇÍK*ñ\x0010ø\x0012®@ñlUÐO¾«\x0011Û\x001c±mF\x000c©}\x000cb<$áOÉU° Æmc\x0003v­-²\x0011½°,­¡$¿Y¤õ]Øç}ó\x0012+f·Kì«ðL\x001bT/c\x0015â#\x000eÍk\x001cq°t¼Érã\x0002·³\x0005»¨øµ\x0016oÆä5Y·,±ãÆ\x001d\bË"eiS¨ê5v\x0015ä2â5<ë-÷\x000cÆ¿Ý±
ìÝâõd5â"âÉæg¦Î\x0000Þ1-;h®0:-ï*ÈEÈÍ1Ï9Ãµreb¶LRÓ°W\x0008UîU'Û^\x001bC\x0008ßÿ\x0014XÇ[Y/vÑ­\\x0010Ù\x001cC¬b¥½è\x0015s\x001e+H\x001ey{CÍ\x001eÙ&½Ñèà\x0004RêÌ=Ó7»Øa¶\x00162\x0014\x001e\x000e=\x001cJ;xR3Â\x0007·Y~Fy®\x0006;ÌÃA±- y[ÄK)\x0011þ\x0004¥E\x0012Õ\x0008Ü\x001c\x0014ü¸¤^çoËsÒ¿h<RséÇ¥=¤aTÚ)Å¾\x001cEÀ/­ m@mèÙ;kf\x0006æ.!°Jîº\x0012õþ\x0008õ¾\x0015µ94{ ÇÌøHÞÖ:r\x001e\x0007\x0016r\x001f?v¬5@ZkÎòuJè\x0016õ\x001a6v>ý<mlÔé¾PÍ½åjT8\x0014æ\x0018¸é\x0000d\x0004\x001c.=u÷§9ù`ª´Ñ+·Éþh´nn+ãÝÞ)OrÜÁóåÊTêW\x001eÉ\x001fdóæÖ\x0013SÅ¼I\x0002Ï!ÈÀC­\x0013\x001dj'jg ¬\x001eÅ_\x001cµ+ï7¿ºÄ\x0017ñç··÷÷'¶]ÇüH¤þqeéÁShÃª¨\x001e\x0016\x000b`Y_ÐvóûÝ$Ä?¿Ý]\TÚ¯Ù\x001eÈíQöèDø.Í¤Tö\x0018¡Ò3ùb¡º×\x001eÛ£FÙc uhIýýÂHH»÷á^{tn\x001edõ\x0001Q9cÎ&
©»e9òöÚcr{Ì({¤á¼MF\x00034}@?¡´É\x001eÛã}\x001fHß\x0007ùlf{¬÷I
Ç~­ýæs{üw¾ßL4¨Øoøç\ós;d\x0016GÐ>Í]-¾=cÑýÇýç/ÿÇì¡Å\x0003CËãÛ\x00185o\x001f?îO\x0015'ÇDåie¬ge	ð\x000cÙË]»ëWÛª2Á1?ÉøY\x001aP{V©¨-\x0013o$Ò$	Ïñ®\x0001­rÐª\x0003´±Üö«,5F¤|gò9æç5¨uZ÷l\x0010ÍÏÊr)
\x0012«sy
 M\x000eÚt\x0006@ãTÁ<Øo-ÙËçøð×¶9hÛ\x0001Z'\x0012\x001c\x0015S
^iÃOsRT+h+Q»\x001cµë@-5\x0016û&ÔJqk¡MÜ=Â/jå5 ö9jßZ	\x001fP\x001að6o\x0010fÓ\x0012a±}=ê\bãðZÐ\x0004;^gé]¯d¼\x0013Ï.Ä\x0004î<\x0015î\x0019~§U]Lmè4µÑ\x000c>\x00003¡3µÍ:É·x©«5\x0013Á\x000by$:©&PûÛÃÇÇ)äÓÝé-\x0008}À\x0004\x001b
âÉU\x000fåöòÕõL\x0014ru^mÚ;BEÐÐ\x0001:no*\x0014\x000b\x001fRSµÐÚÙzOç:Ô*G­:Pc\x000e5ßàãR0YI\x000c6TiÀV¢Ö9jÝ\x001a4>ñOI ÐX8AÔ:ØVh­8µ\x0012µÉQ\x000eÔFqwµ\x0000I\x00042`¡ËÃ\x001ea¨mÚ6£6!¸3KW\x0008;;¿xíãFeµHÙ\x0000Ùå]ÇBkÃ­\x0015B\x000b\x001b \x000cÞ\x001eq«CísÔ¾c¡cÍÍ÷Ø14ûj­Cê¯^\x001cGo@\x001drÔ¡ÇíY~Ð\x0013aÓ¦|ÃtºZ\x0002\:ïe7)ª7-6Þ"H(®û<5 U\x001apÕÀ¸\x0012v\x0019\x0018{"#X|øæÁ\x0001_Üby¢\x0001u\x0011cdO|îG\x0018A{ÅÏÜ#»=þ:\x0016GÅ-pXW`;¦ç\x0016\x0007ÿ\x001a`\x0017ÎO¶{¿è°}\x001aú\x0017±Yª)úl.aÁb¤\x0001uáFd»\x001fÞ/pË¡´öÎ£I#iªÚº\x000e5\x0014ç\x0011ÚÏcD-\x0013£ZôÙ´CR\x0003~tÙã¼\x0008\x0014ç\x0011ÚÏct~X»'±rAQ\x001d\x0002¿\x00128=2ÁÎ¯4sÍWÖ,jîY\x000eF
ðp\x000c;\x0013¨ÞÇN\x0004ïôQÍÏéTóÃù·w\x000f§®¶\x0003¦£Ç¶Y\x0007\x0011A$ÆýÚ$N¼=¿<\x0001+äX¡
«P©\x000f\x0003U]<3^ó\x001b{¨æ §cU9VÕUIî\x0007P\x0002Õs&"ÉÄp\x0012ì ¨:ªÛ JFHµ:ÓD8ï)³\x000bS{Õ\x0008¨&j\x001aW5pºý
3¯\x0019HÉ/¢AWyOÇjs¬¶\x0011«å\x0000­PÞ\x0011V¥y]«]C§cu9V×5bzÉÄ!@<Ê`ù¥¼ÚFv:TCõ\x000eËsË
:,Å'+5oÖÇ\x000fOÆzÈæ'ç*÷\x0000{WaùR-e\x001aU°ÕZèé`\x000bï*\x001bÝ«Fp©-n\x001d\x0012\x000e½)U²ÓÁ\x0016>K6:­\x0018hýaleîm\x0003\x0016Íôäj\x000fVeªñ\x0017\x001cb_ß><Þm~xÜütj^ QÒcÿãüúÞ(:Bµ¥íõîòú|óÃõöÕÕ	!G\x000cíù\x0010\x0003G\x0005oy4Yê\x0002¯¬rÈª\x00192ÄÔ|v
ÞZ Z1ðø¹¼òP;më0ë\x001c³nÇ\x001c¯ú4äfNë¬·Yj±p\x001dfc6íµãwKT×£	pçC"ý©¶ü¯ÃlsÌ¶\x001d³a^«ô:ì\x0005?¤)_½	­\x0003ìsÀ¾\x001d0RçÎMRdp©¸«¹uC\x000e9´C:qA©\x0004Y3§ÒÕ`·
ò!:O~Y´c\x0016\x0007ö$#=	J®ÙUÛÑ×.I{4Ù9\x0015Q¦¶ôpêCWº'²=  Ã£\x001d­¹â/o\x0011ü8ÌE@\x001d\x0011%^Ýè\x00129p©\x0016\x0011ïv\x001cQLUùt\x001dè"¢È"XòÇj\x001eQ\x000bÍ
<ª>`±2rçå9zsùäß3KÒò¨aWË©a÷íýþÃíæw·û¹ÓøÝþ\x0011»­N½A\x0007\x0012"Ù2õ±\x001dæ\\x0010°ä«ß^l_î6¿Ûm/ç~ãwÛë÷×þ5\x000f9|è¯<öyÍø= ×tQ¸\x0015¾Êá«^ø\x001ah,ÕK¥Ò½\x0005Ó\x0019¾\L¡Zñë\x001c¿îÅ\x000f\x001bf°#\x0005ÿ(9qA-\x0004´Â·9|Û½{,óTK\x0003Te\x0016IòT-ækÑ:&¨QEÕs÷¸ÿñtV\x001dÔç²tÛÅ)áÙµ+Æ\x0013eÕMâ
rw½}Q§Ô9f1\x0002UÔ>×"ÖÔë\x0013ð¦C]\x0005à;/T{8V!V9bÕ\x00189\x0012y`\ò r>
EUÖV!Ö9bÝ¾Æ@,Q¸qiÒ%î4Í\x001cóòQMØ´¯±bÞöqâ=ÐÕ§©Um\x000eØ¶\x0003¶,p\x0012ÿFb+K®ª·
±Ë\x0011»vÄÛpdUKZâÄ#àª«\x0010û\x001c±oFERÚÆJñ¹i`µÊH¹
pÈ\x0001fÀ¨ÄJd\x0018ØIµ? \x001eµÄ\x0019Ó·*\x000b»ë ÇÏ>'}ÓP0e\x001d*±$PåtY¸\x001f²9xO¬ûqù\x0002¦\x0004OP\x001d=<	°¡\x000cÑØË^ê¨ 7öÕãí¤wûâôU|ð£Û£CByÄ MËý¬N/2d_]ïv¨zû¢úºÊF@n\x0004\x000c1Â\x0008ª°#¹1ÇÃéue6bç»Ã\x000c¡\x0001©ü:­föAðÜYN¸;ìÐ¹\x001dzÌç
Û\x001dÑéP\x001d3¤Çz£\x0016ùa:ì0¹\x001dfÌ÷p$¹âc@¥GQ|·%3à\x0014Ù¹µfØÜ\x000cûý~\x000eÛá¿?;@\x001cß('_ÞßýõiêÔ4j{\x001ea3ÈÄ01Í8Àô°Ø\x0007|\x0018a{yqþûm,P\x001cßÄ\Ò:Ô6\x0018ä£Â\x0003¶à0	av×\x0013¤BN\x0006­sÐºc©cjæHâL¹Þ¥gÌÎ0\x000e}2h¶\x001d ã½YSgØ\x0013<¡\x000e^2êÅ\x001bR\x0003j£öí¨1¿$\x001enqGµIUÑEîð\x0006Ô!G\x001d:P{M¤ÖÈ\x001fBÌ¿ñúÌ£&°X[Y\x000fZ\x000e¤Ý¸i@âñô¤©à\x000bÑáy\x0019a»\x0002¶ë9Äo\x0002ªjÍrCqc3õ¯sòùÙÝÓ}Ècö"û\x000emyæ\x00184õ¸Gíy\x0000ÕÐá.{øpÏZìå)ð'Â|IX¥Z\x0001]LÿÏRL³T_~~zÜüñÓÓÉ"I\x0001ÛåT*jÍ¤íÑ'\x0016ÄåX3µx^¿}s½ùãÕMU¬0ë\x001c³þ>0\x001c³éÀl8\x0011Aúý\x0004«úÙÔ\x001bÜWa¶9fû}¬³Ë1»ïcC9|\x0017³ù\x0018ùSÐöxÚÕÎÓ®ó\x0013Ï»\x000f?ßÞo.nï\x001eOîÇWÁ³ 'v´Ï<í6\x0015\Ôã\x001fxÞG_}±¹Ø_×ïcGíkvxí\x0000îý\x0019ªE¤³ô´Àé5¾Ð\x0004®ràª\x000b¸ÓLÁ\x0001Èa5KUXÁ½?b\x0017¢	¹Îë.äV0©? º\x0017iyËãèÏ<\x0006®\x0004nrà¦\x000b¸ÑDVêA²N4jc\x0002¾TalBnsä¶\x000fùÄ\x000c6!ÇK¤£%ü\x0000\x001b=ÏHä.Gîú¶¹¢¿Ç.,Ò5±BñÃ÷r»æJäÇ|ùòWZ2oþþéó§/'xâ\x0013\x001a\x0014Õ\x001a´IOnæ\x0004yøw7¼zwõþ\x0014à:\x0007®;\x001b\x001e	Si¢>bç1Þ`à\x0014\x0015Ó±Û\x001c»íÄî\x0012Ã»\x0005êüWÚ¦W-¹ØÅÙÝçØ}\x001fvmúnêR&
Y\x001e=áYÉÓ°Ç{öQßz\x0010GýMÛOOw÷?ìÒù}ÙKÃ½Ñ¿Ð\x001b¾\x000bÈ\x0010ðlÇöòêæüâõó¸!Ç
]¸å$¶ÁiÆ­\x00087,f[-¸U[õàvÌ¬ÐAN¸CÂ-ÔÈõÖ9nÝ;0YÞpÇCMp>,z\x0016Ü&Çmzp\x0007\x001e*ë-Y\x0017Ì\x0002Q¶EÜKNe
l8n;¹í]ÊîãOûÇÍ«Ûö§FOÌ¯hààÎ\ÑZ²\x0014¶£pìQv¯~Ø^Ç_ÿ°­½/\x001cw\x001cÂÜqØ<5aï\x0018\x0000!ç>qý¬fð*à*\x0007®º#1\x0014=2hÇ®P+&vÑË\x0015Â&ä:G®û\x001b¢ÿ¤H<þÜ>ûb{\x0012råÝQôÇ(®Éöþþ6Îý¿>á×ãíßn\x001fO²ZñT\x0000Âê=XzNs^.>l/.vñn_þþ\x0006\x0007¾®wØ]W
\x001erôÐÞ\x001b¾\x0011\x0003[ü¢ì\x0016õâ-´\x0011½ÊÑ«NôÖyß\x0008%Ù©\x0007*g9\x000f£Áàu\x000e^÷\x0017Ì	)tò3Ó|è^-¾7¢79zÓ>\x0000
8Fô
¿Â´qäµ_V¹jDosô¶wÛ\x0007j@Û^Ò­4n{ËQU-Þ§\x001bÑ»\x001c½ëCï$wÆµg¢j\x0010d5\x001cN_E\x001frô¡\x0013=¾ÐjZûÀºê"Ò©«<·¡Ï±ÐÝNø[\x0001½W%âÇ\x0012^ñÆ7eFøe´ê\x000cW\x000ewäuì¤5M#hÉ^Ç\x000cö²\x0008W²3^9ÇD^xAY U:¸V:¸Ç+J¤vþ\x001fö¿|zØ¼ØcUiÿøñT¯\x0003Lxã\x0011T!A)Z{·üò\x0015öÚ¼¿ºÜ¼ØbYi{ýêyìc>ìÆà%uÂ\x001e¯Ü\x0014iQj{n\x0017sË6è*®:¡s .»æ¼88"uÂü³öêµ\x001e»Î±ë.ìNpN\x001f= ^Ääm8¹Da¡ÐM\x000eÝtB\x000fÔM\x001a¡Ë4¶eþ\x0010\x001b~Çn\x0019c·}[\x00069\x0004%a7¤\x0002ø\x001f^÷ª4ßzì.Çîú°Ç}\x0012è¤bELSRÌ'Õ,>µA÷9tß·e¢w÷´Û?Ç0k\x0006ÝF«
þ¬Ç\x001erì¡\x000f;eÒq¤ær ªZÄGBÏ\x001aq\x0018\x0013hÅ\x001e<±ðN¢g \x001dµÅe¯R#®\x0007_\x0006Õ¾¨ê$Ó=Ä\x0017g\x000ccÅö{U§t=ö"¨Ê¾¨úÍ\x0017¾\x0008«²/®b&\x001cBJ	h\@xH\x000e¾:ð·\x001e|\x0011dgt2@´S`¥[ÿ\x0018W=ÔMÊÂÃË>\x0017ïÄ´Co&rÄ3~r,øÂOÊNGé\x0008\x0014ã\x000cSZHÅ÷¿\x0018\x0004Æ\x001cX)2x)§\x000cþÅ§§ûÛ¿EÀû_îâedón÷ðeó\x001fñ·'3<éx	'V©RµÕòÑõmè/®n.vÈ7/·oÎã¥dón{~ù~\x0013ÿ°«Q>Éãwb9¿\x00132G2\x0003»ÔñH}4N&æSûµ\x000cR¹AjAáL&þYOÇ'{äâ¥×\x001eÛ£Ùc<Mé´?SÜÿë±Zþu\x000c2¹AfA±U©2&i\x0003Ó¿.
¢÷cssì0säaräà%0Ý-éû¥Ë}¯A.7È
3H;æÊüt2$y¿Eu^|n\x001fe\x001eÛP7·\x0007v	^øÄ\x0011¿Xôí5(ä\x0006a\x0006	E¢0qË	Ò1I\x0002eÃõ\x0006\x001dn\x001fSL\x0015Ã,RL\x0017P}EÐ'Ò½¶u£?Öþ²&&~Ù\x00032*Çl^þ¼ÿiª\x0015>°+K^v\x0004\x001c\x001bxDñÍË×Û\x001f¶\x0017\x0017Ïc×9vÝ]óÐWL¸Ï¨V&¼²\x0013E6è6n;¡p®S\x0007\x0012]\x0013vekÀZÝçØ}\x001fvw æÖ@ä)Ò{ÇÄÜ
Æ`\x0017Ç,5âÀR³}úééóÛÍõíÃ§»ÇËM:µ\x0019ÅÊé\x0016&ß¾¦Ö6~óÃÍ»÷»ÍõîòêüúyÜã\x001eÜZ
A+zù!©³àÄÏ@Ü*Ç­zpOÜ\x00083lÖ?Äb6sÖÈÅ¼©\x0005¶Îaë\x001eØú0zbü<L*w\x0019¹Ú&mºv	$¶d²;ÆIËíÀãpÛ\x001c·í:	K°¡ç%Ë\x00055\x0014·Ëq»\x001eÜÂ'QìD\x001d)\x0013Ý¿_¸kr&ºÂäPºBÛÙTDõ\x0016\x000f'KzËÀN<È*)êÉèå\x0015N.üÅíýlOÅ\x001b7·O*\x0000Vp½\x001d_&À1\x0003µ¢õÝÅf{
RÈB\x0013Rí¡Æpl¸ß}]`j\x0010\x0016Û|W!U9RÕ¶¦ÀWÊ\x0019¦õ,V\x0000U\x0001aê\x001c¦n[PCUóÃ%$¬á<
ñÄÄu1G]ÔäHM\x0013Ò\x0012çY¼\x0007°â/r2\x0011Ò:ØÉHmÔ¶}úØÙåj¾s\x0013,& «º\x001c©k[ÓÄ åÔ\x00018¯©f¤¶Z=\x0019©Ïú¶5ÕìRU\x0010âÖ\x0001(U}Þ9\x0019iÈ&¤Â2ÿ¡Æ\x0011æ&Õ \õ­þT¤><ü­ýüS£ê|¤\x0002k9«YûÃ,ÖªVA-ü¾lsüR±ôÇ\x000bèû\x001bÇ§¿Jcö,RcBIH~wÿy¿yÿx÷éþöÔö$3«ªÏÓ¨âLÍé¢OóKË\x0003vwñn»y}~u±«Q\x001dÀ1?#$ÏÚ\x00029^Ú§9=©\x0012DÈ¬A\x0018®¥\ë0Û\x001c³mÇì\x0004îi("p\x0003¤ô6
ý¸*qç:Ì.Çì:Öo\x0012þ a#½fÅ
¡ªJ
ë0û\x001c³ÿ>Ö9äC;fM÷c\x000f^\x0011ùô9]\x0017\x001fIV\x0003Î\x001aáàÿÍW9ãjKþw\x0005­áè¦£!Ýt~÷tûyóÃÓíç'RAÇ»¥¢\x000f\x000ec2C±q¬ÊceõRü»Ý»Í\x000f7»w¯j$ÖptçAÌÐÙ&öpì\x0019¥\x0001
£YR,Æì{^ÙäM3æø×ÏìÜîFE4ÄÌôJ¡Ú\x0008µ\x000e°Ë\x0001»\x000eÀ^¼÷u°¬`²íôl\x0014æc\x000eí£óDãç\x0000Ù\x0001&Ì\x0005+â¶\x001eY\x0007°ý\x0004JD:·o{\x001b\x0012è\x0000	t5AZ\x0007Z\x0015 Uû\x0011þ\x0008ð=º:\x0012§\x000fü®`Bµ¬s\x001ah\x0005Ç^`ò	Ì\x001fn\x001fñqíãíæòöñoû\x0013ß\x0015,ë~S\ä3E\¨_ÙQ\x0014çw\x001fv×øª\x0016¹»þÃ¶ò¶À6@n\x0003\x000c°A¶·\x000fHIH;mìò¨t
îø;¸â;ðØÂöéãÝ·_îN\x001aÕ³hN\x001d$2¹Íí\x001bU ÄâíàÑíÍ«ó\x0017»ë÷çÏ[\x0001¹\x00150Â
¡~²B±xK´_Âr\x0004í°BåV¨\x0001VxG'Ñ
Í·4\x001c\x0014`+\x0016».;¬Ð¹\x0015z\x0015Á0³Ä;\x001c5XÇ0\x0002\x0011\x001dFÜ\x0008Óo\x0011\x0014S£\x0011Ê;Òyvù\x001aÛÉæ6Ø160%e½9´ÐÏ¹§\x0006#\n\x001b`D<ÎdCôTÍKÍ'by¨­Ã\x0006ÛàGØF±e<âN\x0015%iQÔ¸Ã\x001b\x0011\x0006\x0018a<uUGàÔ\x001c¤7ÉÅZ\x0018ï²i\x00027ëÕõ!I\x001fPF?¥ª\x001diB\x0018ïd\x0011îäxgIÒS!uXygÒÇx\x000c¢Á"ÞÉ\x0001\x0001\x000f;chf5î$j¹Çâp0\x00169X\x001bÌãFe\x0007Y¡§Í«O\x001f¾Ü>=n®?=ýçø%N\x001cÎ\x0019¸èaç­_³ÁÕµ!n6¯®^¾ßÝ\o®¯nþÇóÈMÜô!\x0007j{ægØÌ¨\x0018/>UE¤a\x001fg{0g{ó ío?=Þ~þrw{ªbä\x0005J·
WI¦þoJ·\x0017Õ\x001bç\x0011Ûß^]ïÞ½Ç¿ò<dCÖÿÖõñ
MC\¾ßGÌ\x000f_öw\x000f'"Ö1Ì2ÂD\x001c6\x001dIá-Úy]|¿ÿíÕåûíùå	U\x000eXµ\x0002FÂ\x0007w0\x0006¥ã\x0011°çþæÅ4g5b#6­'*ùÚ.,É\x001e
¡k;Tß×\x0000VºXbÝ¼Æ>iOaCï</l`ê!¯«"¤k »Cv¡\x0015r\N¢`	 IC\x0018¦y\x0014pNC¼üpû
×\x0008!-Þº+b\x0000Çc}ÄLì¥Â'\x0019y\x0003Õ¾¿\x001cñýÇýgT"\\x0004ý§?ÿ
ö[\x001d\x0006v\x0012Ónæñ\x000fá57æ"ûSïÖPá¸j\x0010Êª\x0001Ò½Ä ¸:ùª-\x0013q)¶¨óU[0Wì²þbÊ<Áì%\x0006ÂíÍóØU]õa\x000f:½$\x0001éEÇû5û\x000f¡\x0017£w\x001btC×Ð}¢èu=½t\x0008½¨ÚÝäØM\x0017v#\x0003×£&\x0001>éS\x000bºXVðhÃnsì¶\x0013»&\x000eíéõBzä5ïmØ]Ýõa\x0007ËQ	J\x0000 xÙí_\x0007ÝçÐý÷µì!Ç\x001eú°ë¤ð®DH÷}ZFÜâ{Y\x0013öìª\x001f®úÿþ\x000b\x0011\x0007Y¢¾\x0007¼Õ\ÌVÒÐÛD%u^ùE\x0019Ê6ðE\}õ¯|\x0011Xe_d5%àãßw&yÖ\x0003«¾ê{\x0012ô\x0018\x001a¥Eñ³½ùWÌÃ\x001e\x001fâ]óÔ×ÀT\x000bø#µN9ý¬Jâö"æa1\x001f»¹¾Ãóø!Ç\x000f½ø­gíU\x0011ïqÜP¤à4iô¬XåZü*Ç¯zñ»Y£\x0002ÙË$uppã"ò>W[\x000bÞäàM/x$oK"æe´w¼K2_Ïúúµð]\x000eßuÃ·T\x000bñoeé@\x00134k9ùá{?äøC'~\x0004MÍÄ\x0013	´¦>\x000f.º8ÿìKòJü²ô=½ÎG"é\x00048\x0006n"\x0004+
	ºg]çZ\x0003Ã+{O¯ÄÀs´ÿ-°2+Ò²\x000cïßñKÕº×·\x000fwØðþÓÓý§§hËÅþ)Þã?¬¸Ô*f.0)öZÃÔ\x001frQÓ\x0002ïâ¯w×çø«÷W7\x0017W7ïðv~óþz÷òyk ·\x0006ÆXc&mGKúl$ûãàøZÆ¨Ü\x00185êÓ¸TAÃ{¤æ/\x000fEmNktn\x001eõi<7¿£ëòt'\x0013É]-êNcLn\x0019d\x0014gäºl ¶¨hzþìw\x001acscì(c,^\x0018,	v:²FJ¶Z¿ï°ÆåÖ¸QÖ\x0004jØ&ç
½\x000fJvhNÙZM´Ã\x001a[ã\x0007Y\x0003.%Y:ðd·grçhMfµÝÃÕÚÑ+ú\x0010s\x0014°@U2GqC­\x0003W«üvSD\x001b9*Ü(\x0016â\x0008Ñ1sÛ×\w²Ú\x0002ÚaNá¡å(\x0017­IÝÔàéULúTß¶A}\x001d¯&\x000b¯&G¹5\x001cR­ñ:
O$ÁSë«c
ÖÀñ,3Ì³ÌG2ç»Ï¹}Ü?|8ñ±Ä8iøÙ=ÈÀSq©ø³,2\x0014\x001aç»wow×ÛËµìã\x0019gÐGò]m\x0016 \x000e\x0019\x001f9d@xViIóójR§Y õñÃ¶6¥Dûýãþï§¾Å#ÿ¬ée[Ï¢¹Ê\x0010\x0001­ÿöçµ¬ßl¯·<\x00013ä¡\x0019³S\x0007é\x0014Ü1Ç'\x000b<¯t~*b#ÖÿÆ\x0014G³/Ä<\x001bÉ\x000fËýON\x0017Òñ\x001aÁs,\x0013\x0005½ß/
óñ\x0019±¨pÎ\x000fËí\x000fWi¡¸õ®|Öæ¾d&¤úÝ§\x001f6oo\x001f?z\x0012\x0006ôë\x0013å<(*\x001aÄt§bô/¨~wõúr\x0013Oã»Ê.a\x001b ·\x0001úm0Ì\x001bm°Øx2\x0007Ý¤"%{Ê\oÊMP\x0003L\x0008Øø5 ó4Æ&j²õâY=©ÓMPîH\x000e\x000bÉI³ôúÓÃ§Çþ\x0003\x000fíýýÿÚ\x0018^-¾#pGÌß¸|ã1\x001f\x000fÁó\x000cU¯¯.¯æß¿Ø^ü?ÛJhe# 7\x0002\x0006\x0018aõ;|\x0012Q\x0005/Ó\x000cZ$
i7BåF¨\x0001Fh\x0006gÆ2áv
÷Ü¡^oÎÐ\x0003\x0000Ç1ÀKÏ$?&\x0000\x0019±Ø|Ó`?\x001eñÿr0æÅãí©=\x0001YÚËJP5_9Ö"ÁáÁS»Î_\ïjC=þ¸±ÅÿËq5Ø$]¾ $Ú³\x0007«Âr«V\x001bvcÿ\x0017=Á«°\x001b\x000cc3vM×}åÒ\x0013P0pjWs\x001d{¼à\x001d=ÀIÈæ\x001e¾|Â$b&Z\x0019ÐÛýã/·\x000f_N¯%Û¸ç)Ñá39Å¢;å÷Û:§Øåû+Ì*fÚ¥\x0012½Ý^¿Ù]¾¯WÅå\x0006\x001bZ\x0004ßµE ¾\x0011¨â°~\x001b=ÔÇþãñîCtR_~þtÿñÔösi5Ê Yñ>Ì³oJq\x001dSCmT)ñbýöz÷jw}þ2ºªë÷¯¯.^\x001f:ðøc« ·
ÆZ¥\x0015qèx'\x000c.)Ác\x001au}¾U*·JµÊhzaòÖzÐJ&\x0011IQ{âë²JçVé±VÅ+´¡+ij\x0000GÓ(¨8öµ>É2Ã7àLÚ\x001bÂªÂ:×d
O\x001d½FÙÜ(;Ö(©I5hÒ¥	HM9Ú.4÷Zår«ÜX«°\x001bèTI.I³/^\x0000¾Öþ\x000b¹Qa°Q\x001e\x0007»&£a·\x000eÓ\x0008-j9tU²\x000cV£\x0012|¿qb<¿öì×k÷.³
¿.\x0007;vi¹\x0013ÛEoè%\x001d,¡ÒÕµË¬Â\x0007ÊÁNPLÃ3³k<Ë\x0004)ìÚ¿Ö\x001e,Ü\x001cì/D\x001a\x0002¦èc\x0014m­Q¥É,u\W\x0007VÑ×·w¿ì\x001f\x001eN½^Äk)½ZCL<Ì×\x000bÉ­~\x0019üüpþf{yù<RÈB\x001bRËü§ÒK"H¹ÈîuLùd¤*Gª*N6'¤|eÃÄÖßODªs¤º
©H:\x0018ÆÓØD\Ó@\x0007ÒÃb\x0002¹
©É6¤¬w\x001308Ï\x000bÊô9S=k\x0000LÃ´m0ãÎ¤O¯Y0"åÛ\x0017Õ9¶º\x001c©k\P~xHÔ"	)s¯¹ðL\x001bÁsHÃQq\x001cõ-Z«e6	èR£IÜødd"ä[|h}ò\x0016äg!«\x001c²j\x001c,íO]ßÛ\x0004·¬Å¹õuYw`ö48:Í"QîëÒåKèE*õMÙ4c6Ø¦¨i\x0006I%\x001bVGáêZ`XÙå];f<r\x0006I$Qd\x001fØ/P­ºÊ\x0014·
sÈ1vÌÚ2ý\x0012I²#ckt\x001aC«1ç³#ö@bÖ87BRR¦Þ/6´«³Å­\x0002]8\x000eÙî9pä&\x0002UÜÜ
xèwt·ßø1&úE\x0006ùbÊüã¿õvóòé~zÝøôtòöÑ×Íi¤·Æ!x|1!D¥Kó\x0002äøÃÍÅô¨qu\x000f}\x0015Èá\x0018r!Þ¼º{ÿýòç»å4
2Q«\x0016ò\x0016ÏÅ³øO\x0012É\x0017ÒÇ-B~·yu~\x0019ÿûåësÔ+Z¬à\x0008²Þ&#ªß?Ý>Í
'ûÍÛÛûûg¸¥¥²sLÙ,)\x0006\x000bm\x000fÒr-Àñw¿¿ÙÝÌÍ&ÛÍÛÝÅEm¹Uù$9a>ì&`åa\x001e÷§ùóCb¼,w|:véÿô¿þß_þóöËÔ\x0005/~ó\x001büÿ?ìþútû0s@ Æÿ­ë»\x001eþþ\x001f÷ûÿ¸üôðpû\x0014·{Ä\x00197ò\x00137QÌå}Ì\x0002Î,v#Oi±vbÜ¾>ÿáò\x0008æòêòrw\x0013·î\x001f¶7\x0011äå"ÿGö³þóß\x001e(Ûä\x001cóãÓÔ¿y¹¿¿ûqâÑx\x0006¢F*í©H\x0015S_Jó\x001a!Z%ççD-å4QökÄU=ùÛó\x0017K,\x001a\x0011ëãºÛ¦3´¥Úî/ñ¬}ùrûù\x0004ÚEg`çÑ\x0003&Bû¹½(^¦\x0016µ_£Ä\x0013¶{\x001bØû÷»ìxUðMâ \x0011ÿØ\x0004SÍ8U\x00088â9á\x000c3¯¶AMÄ­Ï\x0001]ZHÌ)\x000f~~1Ý×?=}¹ïîïÿ~\x0002ThjþñÃã=&éøáã÷²J-b\x000eäÿõ¿ºyOÇç\x0017\x0017|\x001e,ä`¡	¬§<º£\x0008VÚ Q\x0007Á¢ì\x000cVÙ\x0011~\x0000XÕm`ÝÔl`£\x0017Å4x\x0002«çÞ]-Pvu\x000cXµ`ÅTz`ÝÌc7´µÐÊ1X}Õ·a
ÜiÜ±\x0013\x001dÆÕÎ×w-l\x0010cÀJQ/ÑvÀ¤Æ¶Zdþ\x0004s&a\x0006\x001b\x000cí\x0002\x0014\x001f\x0003¶8_²í\x0005\x0005Szhîv\x000e\x0003ñO\x000c{\x0003=æÉâÉ¶\x00131,kO¾kR)Ñò®õ
\x0006¡5\x0005ZÓ¶mQ­·-àÌÅ´\x0013IÛ\x0016\x0006íÂ\x001fÈ6ðíÖÖ\x0015h]£K0S\x0001×6\x0008N_¥Ä@8Fr\x0006 -üls`\x0001\x001foçd\x000bü4C8­í¶êhü×iÌZ°Pø/hô_X·\x001d\x0018\x0012JK\x0002ë\x001cÅÜà\x000690(²\x0019hLgâu\x0006ììÀb\x001c\x0013´\x0011Ò>5ä\x0006U\x0005XÕ{¥ÔË8N½TJ½ÆlZ(-4:[/± hµ\x0010g\x0012Å0¢µ9Ó ´³6g\x001bb¬\x0015ó®\x00059¥6óÚr¦è\x001a¶p¶Ðèl£\x0017óZ@I®@g\x0008=âÚJ¿pýZ¶p¶Ðæl¿Ù\x0001
g\x000bÎÖ\x0007\x000ed(Í¥g\x0000Ô*£±Æ0È\x0002mø÷^[UÄ\x0006Õ\x0018\x001bÂÌ©k\x0014ÖÖ±OÐ\x0016Æ -[ÕÜ\x0006Ï>!âÂó\x0016µ~g´c¢®*Bê\x0008
ßd\x001f\x0014\x001eA5z\x0004Ô>ÕÐ¨3©(YÔ,0æ©Â#¨&\x0010â?;±àà>@îXÞ\x0007Ëé&9\x0002­.În:cß\x0010méÆüËNßs¶èÎf I &~PØÕCÐM\x000e!\x0008\x0007³CÀw\x001dº5\x0000©j)ç^ø\x0001h\x000b \x001b]µ|ÈTÌÅ4%	é\x0013¼\x001bãÀtYüjJ\x0017\x0003^qÐÆô«_Ø\x0007@k\x001bÆD\x0006]dº1[W\x0005iii)UD5"ZW?h\x0017\x0014©¢nJ\x0015¿Ýº\x0016qA7Æ\x0005;ÑcLë\x0002®\x0014\x0017%.í¬Ü<\x0000m\x0011\x0017tc\øFKk°`\x001aÃ\x00022ÌÖÆ\x001b:ùÁ\x0006¨®\x0018\x001f\x0013rM\x0011\x0016LcX\x0010\x0005oi²\x0008|wT¶\x0008\x000b¦1,|«}PD\x0005Ó\x0018\x0015æè¦k¹:\x0003J\x0014·¼´n\x0010ÚÂ!FàRz\x0010·(¾ØNh½L\x0017ÝAõ\x0019S8\x0004Óè\x0010Pj\x000e\x000b1Êâ\x0010õtÆ¥\x0000\x000eÆ$á¦¸:Æ«£1ô\x0003JS-É(º/üÿÔ½Û²eÇm-ø+û\x0007Î\x0004×àSª#WDä)]¢Û/¢X¶Ê&¥"©Vû¿Ã?Ö@®µk.îTË\x000fÈ2e\x0001 \x0016\x0015@³q\x0007Ùå\x000e¶ÀKx!ÕÌm\x0013\x0012xI&\x0006eQ\x00054\x001bþàïu\x000c²q\x0008Ùé\x0010Rà\x0002Òv\x000ch[´8CðUÄMäWjZU$\x0016W\x0015bH3¨ÍªËÙ>ú¯\x000er\x001cïhye\x001b·¤*BÄEÏ¤Å\x0008Å\x0017"ðàØ¶^HÞ²8Úc\x0016 5ç¶¸Îm\x000b@ü ¿ùX¸P³ù\x0004Ñ¢ZR1éMñ¥7\x001d\x0012Y÷\x000fú\x0013C\x0014\x0010ó¢jR1·¬¸nYëÇ÷Wm¶Å¦A\x0002b~\x0014À°¨o¢n3WëÖAãzÉÙ\x001e\x0019¶\x001e*$y.\x0015mÊØÆ|6T¨\x001bÆ«ÆZµ¥|\x0008|ùþÝgöOu\x000b«\x0006=0Ojà N·´C¿¿Wm/_½|s§yj¢M×h\x000bíV	ê"Ômì|Ô4å­°W¦9\x000c7_ÃÍ~ãfyÔ«Û×°î|Ì	{m?Ï\x001b®:+å\x000ft\x0002ê\x001e~ýáíwß<|ù<¸Èº
rÛú!^Ø0j/Ýß\x001dÍt¿~óâó_=|ù\x001c¸t
þááæk¸Ù	\x0017¶\x0002ó\x0006çÿ\x0006Ü\x0014ô9§µý³p\x000cm½F[ÿÑÑ¶k´í\x001fý(½hÿð7íº_	§ä?ìi\x0000sÓÀ{Õ\x00184\x0005mJjPSZe^s×À{Ù:ª*ie\x0001Þï1ðÂÍ;1ÙQ¸×p\x0011p{2YgZ)­*=â%M+Ã"ë^wTàè¨pÀVõµ¤Á¦z´]¶Z¼¸Ê¼æô¢÷ô&ÚÄf·"Ã\x000cz¦\x0000eïáÿ0^szÑ{zSã¸Áu7eÐÓ[òNnù|¸t5¤#p-öyøºµm\x000eç\x00145cKI_ÿ©í\x001c\x0008¡<\x0004\x001a¯A£\x001f4ïm©\x0013tD1s?ne\x0017fºÆL'0\x0017-H×\x001a¸t`Ö<âÇ3c\x0017æx9²s¦içifvþxq\x000cs»mo4ãÊw\x000fxûÓ·?½ÿáíw?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=|ZÓ,f.Ëiü¤àGcI\x0015ÎCq]ÞüpwuñêúÝÝíÕÍ92ÛÙïÌ·dþ{"-YüÈrK¿#2Ýïé\x0008èî\x0008èïé\x000cèî\x000cèïá\x0010À\x001e_rsq*¶\x0016nxëÊB\x0011»g§k¼³FS5¶1ò*[¿ì\x0003àr·&+T©LKeDT9¢°pS \x0007}º ÖrP6e[,+Â
º\x001dN¾"Ek©u\x0007°Ürè3åZ,'ÁÊÚP³;|DÌc¼Ê\x001dm®q*ßRyÙ7ÔÔ\x0000Tª~Ã@\x0012°Xaûb\x0016+\x0016\x000bû#è\x001bâP
*&ÐÄPÙ-\x0007c#T©¥J"*ï)
T<Ý8\x0008Ê/ÜwG±rEX\x0010¹:2\x000f8\x0000°|¥\x0017«Ê\x0003\x0015¥DXp5Ò¶Ö4Â¬¤ËbÝñýÛ«·¥"c«è\x000e|E\x0016D\x0002+/Ç­Cf«Éàé2xã\x00072ºÇtäoYR	\x000e¤ÝNççt^J-VÎojéñ\x0008L¾\x000eLåßÔÌ\x0013¦I,~½xyÿùËãÓºÛÚ$J
xíM­TÐ4ëDØ\x0017n!Ôûoß]ß®:m3O)&¥8\x0002e'ÁÕ	Êù*­£©|B\x0007;ß
e[(+
4ãÐë\x0014yz°3¤G¤£:vÃP®r\x0012(G\x000f^\x0007ÍâÎ°RgHjûJ\x0016*H "gÂtt,èçÏÍQ\x001dJ-T\x0012@9Å9j\x0012Ké9C
~>9\x0014O­§\x000f'Ç6iÃ\x000f¾<?H\x001aæ\x0014ëÇ+æjRîá³·~yuóîîj5_hçùBk»|þy¦lh²µ0\x00083(¼¥ÒR:Ê¶TVD¥©³,V`¬j¨\x0016rLÃX¹ÅÊãXÓ\x00040ÞV8¯\x0014\x0018\x001eä	Xzûjé~_	6V
®iµ\x000cÉLADwPußP\x000b>bCKóÈ&oSêHÁ\x0005Ñô;\­ãyËw\^Äéu²l®b±L6uså#/(àj#\x0007b;\x000e#{?f\x001aI\x0002x\x0001_\x0001'<Ë"é!-dðÏã¹¹ñrÕx½|xþtÿüÛÅÛûÇÏ\x001f¾\x0008j°c²a6Z®5& Æ\x001d½ý½¼º»¹¼ûáâíåõÛ·WïÎÑÎHé´£á\x000b6b\x0005=¥7 º£Ã)¤³-\x0015¯]¢\x001aN/ÇkÈ\x0014\x0010*\x0012(Upë_kx®Ås\x001b>­'ºúbo25\x0002ÝÑY\x0015ÒùÎKé`·) ù&õ\x0015'PàÏ§\x0010/´xA¼xä³,N\x0013·gx\E<Jð\x000bñRÄx±NªHÜ\x0016n=:\x00186\x001cÝ/x¹ÅËâké\x0001\x000eA*Ö<IÃ}'ãp7Úpr+|>S8,¯ÃHÔ¾¯«{£,¶ÊxW¡õÃB+âã/TÈ'=|YÖb»l}]?\x001d^Ä|Çd\x0017^gµØ0Ã\x0005Z0<Q\x0008kfÙ0«05|aÖbË\x000c7ðò)®ÉqiÖíÓbãg3)xX¹ÞÀXC\x0005$
\x0002¾|ñÓbëW*Ð&>T\x0018a>ºâ(\x0013â¾ãa:óbÄæÅ+>\x001e\x001e.Ðý³\x001a\x0015ïïãëÌ\x0011È\x001d8Öc\x0002Ö/DæÈy\x001f_\x001fõÍKà!y\x0016«"?oxÿY»Ï}Î¾\x0018±}I¢ú"½IA@Åcrõ<\x0017âu\x0011VÉSýEiMÞ~ç3\x001a½/v|QÊ\x0013ÚdäsÙ¾Èõ5ÇÑf»óxtæÅÍK­\x0003>Ï%¹\x0001Ïíón¦­8¸Ê\x001e§YÃ|:¸9Mé\x0018ö\x000eÛY?+¶~)°uvÁVëÂ\x0003À9ù}ëg;ëg¥Ö/#;ñyÇá\x000fï|èÅØ¯¶\x001frôw/\x000f¯\x000cÇùY\x00168T8Pwçå£KiL\x0017\x0010Îh\x000cSÆ²x\x0013e4ü|Ê©kegsVÇ!]Îáz9ÿxÿé×¿¨ÌíÇµ\x0019ÎqÉ©:ÆÉ\x001fgù_¾¾¼yõÓj¹\x0018Óä&\x000fÒ$£xn_ö+þ%14íòÑË÷\x0018Îá8õqÇÓr\x0004ê©\x0013Éòjw';cú5ü¡Ë |øúðåDêÎVïÖ¬ÌµÒAenÉ&åÜØë«÷WïVsceZ,#À2X7Ú4´FCíg;~ë\x001b¦²-,\x0016ºó@úa¥	\x00037ìq1Ì0k±\x0008^\x001c\x0002Î&Ù0^)»ðÒ=ä[$/ÜV$§z\x0011¼«¸µS-T&\x000fC\x0016* tÝT~êÕ¨¸0\x0019®U\x000b/ÈÃX±ÅB¬Dý®ê2\x001d`¶GÙ\x0010\x0001Vj±\x0008+Ñ+2XT{J5kt£uÝuH M\x0006K¸<¥\x0006\x0003ªAÌBÐ®ÊlùÅÇ1®ÎbiÉÂ	ÅòPuC\x001d6MÞn\x001ctg\x001c´È:À\x001532T81sâ²«|Ü¾ëuw\x0018µè4*¾eN\Ä\x0018ª\ÇU
ã\Ý¶×}oPlWªSÙ|Ðü\x001d·\x001fFÓíz#ÙõÆg\x001a\x0004\x0008«\x0015^,©cé6¿cÏÞKÜ4^0bUõ¢èÁ;z_¬\x000e\x001dæêö¼ìy\x0013\x000c\x0015\x0004uV4}È±zÖG\x0019H\x0001W·çdÏ\x001b,2!\x001bS7õ8R^¨\x000f\x001dæêö¼\x0011íylÈÖ[*ãCÙÖ\x001a\x0005í»Þv»Þv½Ml#ËË°FDrz»í²Ý¾·¢}ò\x0014\x0008êÌÃó¼åÍ¤Ý\x0016®4{QÆ1ê|µxúúñ§ON]½àJAúC
ô¦WRÜ[¹u8ºøß¾ýòöæfý~fÏÈe²û0\x0012\K.Â+(ÕT
{Ëu0£ëà(kÜ8\x0012|/^%²m
æùßÇ/;£@¡\x0005
ã@(~RxR¤æ/2/\x0011xo%J-Q\x0012m$¬©ª¶\x0011n¤À\x001béÈ\x001a"5q_j\x001e\x000eG¦1;ISå¬â% \x001d_äGº½­\x0005\x001b<^I.øIìÉ×UR[·îö¶\x0016lîPË©TâÙ\x0003`\x000c2\x0017âlGêv·\x0016lo¶BD,­¡rä©ö°½R\x001e£HÝöÖý\x001d=\x0016UÉQVHåTÎÔQãÁ(éö·\x0011ìïdpS\x0017&CÑ0\x000eµ¨LöèÍt©7Þ
X\x0014\x0015h&;2ÅÊd\x001e
Fº\x001dn\x0004;<×É8WÆÂNò´d¾ßÎÎ1ùyq¥·]ßÏýÅËgìG}~<\x0001æªÒWÎQMò¹úpôlåé\x0017/ï°'õîú,kñ\x0014Ï\x001e,#	åyÊ9Ð-\¶Dt¾¥óRºÈ3]¼B])ÎSØÑËx\x000b)\x0010\x0011^jñøÛÖBÊiÒ5&1^ê\x001b§;xE¤k[]\x0006W/ñ´2\x0005|É¨ ùÛz·ÔÞ%À3\x001dâ'¢atX(Jæ6Ø\x0003ßQ\x0010(äëNÆÿÇÜÛíèq#}·RWP ßxÊVÙÖ@_¬Ù9YíB·\x0000Y2d\x001b»3Gs\x001bs{s%ËHF0Éd>õ02ë\x0005Üh4ä²dÿIF\x0004\x0011ÿÐâ£ø\x0002½×*Ï£83ßØ\x0004 Ü|ísOÙmïË\x001c¥O»)\x001fÙÓÛò4\x00123ån«Õ\x0004¥WkWõÚñýÃï\x000fß\x001e~{²\x0015?Ú ÃL\x0013iºiV·ÕÑ\x000cÁâ÷w¯ïÞß½¸
\x0004-\x0010Ì\x0002%¥9,3ÀwlIØD\x0018\x001e\x0018gL\x000bdæ\x001c5£9l(¤ysÚx\x00062j\x001b\x0002Í\x0002Ù\x0016ÈÎ\x0003\x0019ÒÁpKó,«'8\x0012ã`Îfy\ËãæyÒºtUs°tÎ_,m
Ø,oü4\x0006\x001c\x000eS¶P}6ÔÙÅ3ÐÑ\x001d\x0014Z0Ïã© ./Z\x0017jq\x000eòÄ'ÎóD\x000e&p}hÊvõ
Í×³<©åIÓ< ¹/\x0002Û=é].ûåº>ñà	[=ób\x0014Õ<EÝBä0x(D©î Á'Ï\x0012õfzÚN#Ñj\x0015YËÅ«zÆ½Y ÎLëy;ÃñhS#\x001bm"o×%Ú\x0005³DÖóºTE-\x000b¤xÒê6î¡ÎJëy3m\x000e\x001b^éªvL4È\x0015Í\x0012ufQÏÛE\x0013Ös\x000f<t[\x0007_äQ§Mð\x0003\x001dk_bfúãØ#r¡¬Ëg«2ö\x001b~G\x0004â#\x0012½»F\x0003-
LÓ<V_³p;\x0013\x000bøá0ÅÒlf\\x00193\x000bêüv\x0003¢ÀKc*ÏPäw'lÃÄÐ5k~ÿðåë=Ñ\x0015³íâþr\x001cWC\x001a\x0006»U\x001dßß½yûæÇËX\x000c\x0006-\x0018ÈÀ\x0014%<­\x000b+6\x001d£Æ´÷¼6\x000bfZ0#\x0002+3ô\x00160W\x001b9¡¹ 9\x0004\x0018JI%`¶\x0005³²\x0015³tg²8/§\x000c\x0011Xº\x0012	l¨°pùË¸@Q\x001a-s\x0019z|Áä/iH@\x0000\x0006ý\x0016í1µä5,ï&;Ç$V\x0001\x0003½ÛR:½÷Û\x001bfÙÿmäÜÙL¼p§¢Yå\x000f:Ú	¾°½[õn¹Ø°?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ª$QÓ\x0013L3Éâ\x001cX1ü\x0008RÁmªA±e\Ë\x0014HQ¹\x0019ë}\x0002[<\x001d~\x0002
Û\x00059=\x000eEòåLxw¶\x001e0»\x001eÕVã_B\x001cnB_\x0002\x0006(f¦^	Pz¡ø\x001aÌø×\x0000*#¸\x00024
$ÍW6²VpÜ÷\x000cº|\x0006½¼ã¹WGgI}¾þ}ØÒºf£_Âf¯sð£<yuµysqßÙþ¯Í´\x0016b\x001f;\x0006YÖG¨¨½¿:>xvøúusû\x0017âË9¾\x001cÆ7\x0017Û$"ªY«W¾¢eÖù\x0000vþ\x0000vø\x0001&¹ð\x0000ìo2ÿvÇ \x0017ü|ü\x0001r©k8Æ¡ý4}\x0003Y¿¤¢\x0014Ô÷\x0000³öGXAjø\x0001Ü¾Â%$$Eï6R\x001dþ5;{x\x0013;ÿ\x0006àöêaC\x0000ÿßÿù_ï®.ïãwË\x0005Å
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
G\x0003*P+¾Aú×ìWnZCÈ3¿©ÿïÿü¯û»»ÖÀ)\x001c£Òì\x00101MHÕÆP\x0015­
½Ê[ãÞÁùëó³³jð$\x001e9\x0005°Å\x00073ÿíö\x001e]ëëö\x0016\x0017¸wJ\x001bºa¹¸@ä¬ÖôøßN_£\x000bóòåá7·»ûà@Ñ_<\x0006Vs`Õ\x000b¬ræ\x000b&%ªT\x0012\\x0017<´ª\x0014®\x0004Ös`Ý\x000b\x001cr*°44ÄDÔ§í+#\x0017JÞôÂý\x0005Ö¦\x0013gZ\x000eáûäWS¹ðÓÙý\x001er6\x001fú0ð\x001eo|@^\x0015%<\x001diøÈÚ#L^:ævá¯Ï^ïáß·ýKà\Å¤ô¬[=áés9»ßÜ_ÞÄ^Ý·÷]ë\x0017\x0003
Û ñ.\x0015\x00168²lx¬Â?{}ðúè$þôê$¼ÉÏ·¯­MðÂ·÷\x0000²	Pú{qwùöâ:|cÏÞo®.îïf!ÉÕ\x0016|mrs`NBfµ\x0007'!Õê\x0014îáÙÑw/Ã÷õìãÃ×g³ ¥öÂä\x0012ó\x0012;}(\x000eÞ3Ó\x001fJÕ[\x0017\x001eê«oU~"9"ùoò5©ùC©2ó2ÿ&\x000feç\x000feÿM\x001eÊÍ\x001fÊý<?ÿ÷x¨çN\x0014û7yªòèý79{yqöòÝ\x001e¾ÿÿ=Uqþò\x0003\x0017\x00070ÿ79¹.Jÿk?ÕÏÌñÂQ
ýza³8¾Øûñòê*\x0004\x001a}Ñå\x000có\x001aZ\x0019j´·\x0014K)QI \x001e\x001fîýxt|\x001câÆ \x001eÂùCÀ¡ñ§PX¹*5¾ThËi8®¨\x0014Ún}¯ºâø\x000c_\x0004ßÅW!4ÐS\x000f>ÕÚY©rNx×O!Ë§;x\x0010CL\x001e¿\x000b'©\x0006¦\x0011âw±³¯\x0002\x0004Á7=*óÇz\x0002+_oh\x0010Á!áÊJC(r¸R\x000bä¿\¦M!]ü|Dî
ò¿è ­%×\x0006e¤Ìó\x001e%³TNÈ[Õ\x0016ÁKµåær
¹U¤Þ(¦\x0011z2W\x0002	_©-\.x\x000e?\x000e.\x0017iVÍM.70V«\x0008\x001f®$O\x0001ù_Ô§Ö3µÆÚå²7¡\N]V2ÚëÐåll{@CðÆÐ\x0019ß4,w*WSå4ñ®¬\x000e£©çèv\x0010]8½\x0007ÈÐ£Õ\x0005]¸\x001aWI\x001e­E·%úcé¬Õè
K±´ÑTQ+\x00045Â\x001a¸Ð\x001d$ÿ)H\x001fË¬ð\x0014jïáÇ'\x0001é÷½§Wëæ+\x0010h¶@5
\x0015¶\x0015\x0012ugQÒí\x0007ÑÁù{O\x000f^>_,±ÌÃ\x0003ûô+zbñãas{yq;«× -e¶w\x0017·ÿëéíE¼¾\x001cT\x0002aÛ`ÜHuê\x001c|\x0000 ³0üuì}~xú¿\x0006×\x0011.bþv~púúèðt¡\£@
û¾ø\x0017A
ß´ü\x0017A
ËGý \x0006ÏBË¨\x001fÿøíwÿnöZ½ØÄèìùíæúÝÅÍu\x0013©5\x0006ßwÁ!Ðu\x0016o·Nn#}q\x0010#±ç§\x0007/\x001f¼l\x0001M/Õ·
ª/ß\x0011¿\x0001høÀ\x0017P}ñ­\x0019WC¡\x00168
 c!S	.ó&\x001d¶Æ3½\x001d\x0016J³\x000f\x001f¸7\x001f><ÿ4þïc^\x000ee\x001eñc\x0004'	\x001aè\x0014ÐX\x000fÇ°i)\x0010bæãÄ\x001aõ\x0010±q©«\x0018%hýDbz\x0000¹ÐÉ\x0018F\x0019§ñc\x0000ÙTä\x001cGCS=ì\x000b1Y¡*1\x000cAFü\x0018@\x000e/J+\x0019:=RõR°ròÖó^ír)\x000b(¦\x001f\x0003ÈB§æ\x0014@öy)§ÊN Þå²\x0010Ò\x0000°\x0019\x0002NaP\x0002Ö´[ð¤\x000c\x000bÀEyÕ0±\x0002\x0013«A\x00133èÍÄ¥y`ÁÂ¸·~\x0007»c\\x000f_s\x001c\x0003Ëë·°¹¨é)!µ¥Þ:K±m°ù0\x000e¿\x0008àßm?g¬<Çu¬°
C±``µ^¢þ(óJâZPÌl[\x000b]°¼
\x0015ZG\x0003¬
1¥AÃjo\x001aÓ¸@\x001fì\x001dç´Ê4hÐN§7\x000f÷Xâuý6D7m¼ÒYC'\x0006¨îÅÚ¹¸XMÚ~\x001f±ó¿Å]/¿\x000b\x0001Î¶\x0015»¹½³\x001f¿ºb¯.ö^8,Öé.*Ð\x001còq×\x00150~7¶hp\x0018§\x001a,\x0008µm\x0013\x001cÈÃ½W!\x001aÛZ¢[à>\x000ew¾EÜû?åûMáñþyùsìkX¬ÌÚÔ\x0006ª>\x001as}ÁspøÝj­¥ÿø£§[å
.rp¿	®?\x001e®Ô¯jf¯ãÕ»<ßg	[\x001c0\x0014Î%|BgÕVoe¶·7Ð%«}«t)f]Mgâ<ärí\x0019\x0002\x000biÈ;Ý\x001a\x00024à½ÿCþ~¡¿¶Ñ­ñ÷?\x001bãTk,¨ñÄ
\;ÔI
¯°ÂÓY·øÞñÇÃlG½dêÏë_¶¤¾ßü|{ùé¡
×Â´Xê\x001abÀ\x0010£¤JL\x0019Â\x0015lê qr9¬þþàééÑßÎÿ\x0006ú6\x001fÜõ·?UÅc>ñLE7mÄs\x001c¡\x0019ör\x0013ëþS4B\x0013¼<³mMà!**O¶3V\x0011YE?«#\x0015\x0012ªFTiyFÝö­GU\x0011Uu£B«@V\x0003\x0003\x0015#«2Õn[\x0008¬·ï¿\}~óµ\x0017íìâööâãEðë®Û\x000e%Ãi\x000c\x000e\x000cºöûR¥\x0004÷\x000eàÌ.n\x000cg§§¯\x000eo÷rû\x00195~ôª}ÃÐò³þøùSy°¾¸iÜtÃ»\x001f`ÓõQÞBò´jÓÛ|Pè<©ì´3¬|¢~\x0003X÷âVßÎ¬õôö¡õ\x0014ÕéR\x001fÞ\x001a\x000fñ\x0014å§Ð-ü,¦Ì±W\x000eÐ\x0019T²Õ·\x0004¥\x0019lßés
åé\x001a>pY·/Sv»\x0014\x0007.Ë¶m1u®\x000bwýËÛßfßàóÛË\x000f·m¯%Ì¹\x0013*\x001eÖ1ôÏÉð²ÓvNõüôèÅÁùw-\é\x000eä\x001báúôÙ{½Å\x0008qÕeã7j\x0004èØÇ/K*Ë ñ¾ÐàXÚÅø\x001adJÃß°ýÛµ×?zøX¼\x0017Ø5ÕààÀ\\x0003¼p\x000f\x0003S\x0011µÀfpÂ·¿\x000b6©^ÑoË¼ûyXuzùæýæ¶mÕÙ°T÷Oá\x001eÌNßitªR¼ÇÅÖ\x001cÄÑ³\x001f\x000eN·/»\x0019X2Ø·\x0002ö^þvsùÇü¼¾åûûÆü\x0016ZNvÍqNr88¥ú½Ý\x001aLA«òÉë×Ûó
\x000f¿û?Ä×³6w{Ï¢µyø£
U[æ@\x0001\x0001ÑÍG1àñmõg³½g'/^¿<8ÿ­Ôþº¹úx5mñ¿á»æÆ':¸´Øé(¹\x0011¸±0¹õ»N\x0017ü
PøÎ~\x0003P×\x001f\x001fþ¸/7¸5YN'@\x000b\x001c#\x0018	Ç*KíÆz½íÈ©Í¯\x0017w\x0016`)\x000f»\x000eÌ(\x001e
\x0006ymIxÎmª\x0000\x0003ÁA[Ùâêdì·ßØ§Ïó=îæá÷þßæ¼7q«9ö\x0012#S\x0015q|{ÔKé­d\Ì%pÒ/b;Õé<¬K]:¾ïS\x000c\x0019k\x0017SæÒ\x0018Ì\Â§-¤TsNyË¯e\x0008Ls"\x00108Îè#\x0016:º*\x0011\x001bnÂ×¢Þí\x0017ákEI,º
KòÉ`c\x000c-\x00021\x000e\x0010ÄÛRu+}idßodA×\x0001\x00195×:Ä\x0001Y©\x001d­\x000b_ZÙ÷[¤Þ\x0008È\x0006tË£ãTFÞvô¬C\x0016ìÑ»×oeî÷9¾|FÈy²r^É|7KY<Ú-ú·\x000b!8¡\x0008È´\x0008²ºóm{îJbU\x0012«\x0001b\x0004#Â¿ë\x0015\x0001d/u~\x00149D$?MóÅÓ/\x001eÏ\x0017ö\x001e¤;îîÿù~o<Þl\x000e³¡\x0012E×C\x0015?®Ô5ø\x001awì\x0018yñêðìõáSÖì1µ(©Å\x0018µc\x001c\x0006Gj\x0018\x0003Ò3MÔj¿°
[ÆVÆvLÛÊ \x001a°Ñû\x000fØ[«&Ö`Ó\x0004"Ä\x0013°ÃÉÂRÕ\x0012¿äÉ\x0007
\x001b­
þÐ\x000e°5+¬­ÙµMx\x00151\x0019\x000cêB8\x0007
ï®LpAvm
kÇw\x0008\x001bÚ¸ÐÚ£È9·\x0016±;y%
/°
\x001fÄæ Èm\x0010[¡ä\x0015w\x0002/¹;º\x0013êò4o¤áFí+4vØþ0ËèPÝ\x0018­öí&ìrÑ5\x0012\x0008)	ng"µu­¶\x0005që¨mImG©\x001dÝÖBín\x001aÀÇËKÄìâ}\x000c>oAí\x0007m\x001d</ÚF¸²)ÇÅw6?¶íK[ûA[\x000b(\x0015Â­9íÙq¢Ku\x000bµc­áÇ1ê\x0010'&W°Ä¼\x0015Q'.aÅ\x0018¦	[\x0017»Ó»±³ia\x000b)ñ\\x0017L9²¶ÛÅ&â\il7hl	\x0003³\x0013%ÂcSöQjÃ9¹õ6j\x001d¶-±\x0007W6\x0008éâA\x0003#Û1]o¹%j·\x0014Î´Pûò ñ£\x0007
Ì\x0018ÄrÙ\x0010fÐ\x0012áÜ£±­ßÉ6â(±Ç\x001cm\x0003
dliBH°\x00053´²·fZ×a«\x0012[bk®¤\x0017R µE~\x001få\x000e¶\x0011>KÅðÑE\x0012ÜÔ8M\x0017\x001aË\x00146Â¼°­eàë¸Å#îÑUâ=-n\x0008\x0010ð+O\x0001\x0002ã;ØI8èú\x0017ÜnÐÞ*&tó§1ö\x0015ÜÐ2I;ÀVæQ\x0014i\x0006±u 
[(_6\x0014Ø\x0008	\x0002è[\x001a1\x0018ý
ÄU3G
f #ËrÖ]\x00132ªvbÞz¬z\x00087z#áußêä²\x001cúÅ¶ìHDÖ¬@Ö¬\x0017Ùø°¤}z\x0015=LÂ{kÔ#\x000cÈåÌ±\x0001d]"ë~dÍÒÄ©¸Òîá\x000cu\x0017)¾µP|-²-m7rp¨Cd6\x0002²Àº\Å¶è­È\Fyçi-_<ñº6ºê*\x0003:t±
[¡ÞªñaÏ *lÆ·!Ï.d'#3\x00053üØ
-$®f¡µÜ7xá5Vax8\x001aw\x0003]\x001a\x000fXZ8Ó8B[,\x001d\x000b
/©ok#ÁJh!
h!\x0006 ¥EÏ#@\x000b*ÒW®ºÂ¦·ÍaZ\x000b­Kh=\x0000Í<\x0006æB\x001b\x000e\x0014¸ÔÀ¦ØÕµ\x001bf[2Û~æ\x0010OÌ6õð\x0004f1+õ\x001c~\x000fä?M\x0002·é\x0017OÊý¹½nÌ\x0008ôíw\x0002%±á"ÙSÝ\¬øM\x0005d\x000b°v\x000ek;aµ§M\x000e`EJzpcsÜ¶"VÁÊÂ²²×´á3\x0006iMªP\x000e´2Õ@»Õ[E«ËuÐKË=ö!\x0006Z\x000b×â§ü.ÐúÅzê\x0016ZWÐºNZå(A
Ó£èÊáÐ@ëv²lyùqÖ\x000b
!\x001eq\x0005\x000c|¸©Õ\x0002hu£Ù@kKÚÎ×LiCE\x0006P'I:&mÆ]èk£å¥my¯mµÀÆ¾¸\x0014Y M¹r Ý+_+J\Ñ«t\x0011*\x0010>¯\x0006\x000f~\x0019·ÜÃxï&\x0016{XdÆµËË¸»xÑ/pïÄ\x0015VA'SÀ!RD±ó\x0010\x0013­oqÜ\x0017ie¹\x0016dïZ¡I¶\x0005\x000f\x0015ñRÞæ}Áïd_Â¸û\x0008Ejº\x000b¸*1­1ô¦ùàs\x0019×Ö5½Ö\x0019C2hiÔ#³2/Ü]°ÚÕv²r¯¨JÊ;\x001aéÌ2t\x001báôÝg#Ë×Lö¾fÜúlZköMê[5\x0014N\x0004\³\x000b×FGê="à:Õ\x0011.\x001a\x0005\¬\x0014\x0000\±Å \x0004/p\x0005ïÄÕ8c
péüe0§&÷rìÂ\x0015Så.¦zw1\x000e	\x001e<CÈ&\x00041£\x0019­]³WM©\x0012WõâJ\x001d]Ã1	Ï\x000cõ8\x0006Ü­\x001b«pËAuï\x000cLÀÄÔ<\x001dÀYL«·¶:¯ÁÕ¢É^O7ì¯T#ç\x0015Ê,\x0004\-(P;q\x001euéÞè^÷\x0001#ZW\x001a,´`ç\x0013X]¸7~k\x000f¸ðc\x000f®2ÒãÝ¨yE)
\x0005ÑËa\x0018Æ
OýÈ×í|×\x0014È\x0008&Í#\x0011ôä1°§QÆ¸\x001b<ÖRÏËìÆK¨X\x0010>MÉ[©kbì)Uü\x000b\x0005gY\x001f×Z=s8),pë[\x000fpkï@t\x000cú\x0001Âí\S£YÎï5S«ÂÚjÈÚ<1Km\x000c±È"åHPò&po­¬èà.¬­F¬mÂÂV\x0006¹-\x001ci(Üvk©ÓznSp!î`dÄV4~\x000bÌÍ\x0011ÛëÅj3¶-\x001dZ&BD\x0008¸¥öÈ­Rä\x0001Ü[¯\x0016WpséJnèêµÄ\x0014No~¾¸½o--³Ô`ÂBXSð¸sXÇ\x0007\x0012\x0000-z
§'O\x000fO_/q»Û
q;\x001c·	Ü²ÂÎk¼\x0000s~GÜ±;þÜOnÝG ¹Á\x0019ä\x0008UT5ÁR­ð^nÕÐZA\x0003g>\x0013\x000c$.|¦ïo®ï¾Ú¼yÑ(\x001c
w\x0003(¤ÄáºFÅxU2­ð¢ÔØeÇôû¯\x001e\x001f<ûáðt\x0001^Ì*ö\x0003|Ý\x001b\x0017Ìí§ÊW\x000e%r\x000c\x001bø<\x0016\x0012ù­\x001d·=è¶°»°cv,LR¿\x000cvw©wÆJ¡¼%»o­\x0011î®°»tv÷\x0014+\x0006\x0017%
\x0003¼$QÉJÉm\x0007»á\x0005;ü8jx\3LJLz\x0004ÃLrËïj\x0013¼\x0007x5\x000b\x0019`Pf\x00112\x001eíMc¯ÁõF;PÉI¥°Áãeª°b1>\x0007AÚóÿX@\x0015\x0002²fÝÈô²8\x0008áÙ\x0014ç8GÂ>Â-Ç9È¥u¿Â¾ìö1k%â­\x001dmkmIl»5µ:Bõ8¥\x001cf\x001c\x0003ñÖFõµÄ¾$öýÄ\x0002ûþ\x0003±Þ¥D¬iYø­\x0015r+
/
ïG¦¿ì)õ\x0008µ¼µÇj-²,e?²Ao*¸P\x0012\x000föðò1MÈ»Y\x0018[\x001cçý{æ8Y8Ä¨ÐÊa©ñÚvõV=¥Ìú\x0011sÿ¡ãAE.RÃ~-5hÚåJ³&f­Jf­ú½\x0006U
ø
årªw{\x0005T3²{\x0014\x001dÀ<õÇÑÁ
y{ïAì5*5\x0004Ï¤wOÃ1§±ì_Guû*0ç\x00050çÝÄÐ\x0004+Qq¸ÙÄ\x0006ë0 £E}­\x0001YÈª\x001fY;¬oIõ¨b-\x0018j@ÆokZd%²)M?²#Uh®\x001d
j\x0011ÁÝ¼\Ñ<« \x0001ä¢d\x0015²d2Å\x0001dÚÕ\x000436\x001by76\x0016¼\x0000\x0016¼\x001f8'lÌPäNpM&Þû&ÍÃ\x0006dU"«~dcb\x000fãÒ©!B4\x0019YìÆÊó;ù\ÞÉ¯BÞþ\x0014h[bBd(xG6Vå«§ú_=Ù±@\x001cüml=aÞÀíh{Óå:ÖýëX\x0007\x001e}8\x0005iÈ´(\x0014g¸(iÒÃl@.wdÝ¿#Cz\x001d\x0004*;Ù8ÄVrj¹:®¸\\x0015ºU\x0018n)\x0013¦¸Do(¼É$xîTS\x000e¯\x0005¹\\x0017¦{]\x0018îP®"\x0018Yb¹\x0008ÁÌVÞ\x0011²-m?²ÌI;\x0005\x0006Ohz\x0003òÖÞ¨uÈ¦ôL¿?ds.À£,±Æ\x0014)G
\x000fcLw,\x000b+\x001bÙoe\x0018¸\x0003B\x00042.B+·J¯´"#é§²¹AGes«äµ`4\x001f!¬kô:A\x0005»¡Y¶rÖÃª"ÏÄ¥\x0000¹H\x0012­S\x0004\x0017f?\x0011ëàä§BJ\x0018kHÄl9ÛD,XadÁºlµ¥'¬4V\x001b\x0008m=¶ÊñåâÄ6b^\x0012ó~âJ»P\x001fîQuÝPß>\x0017»@VÅ²\x0010ªYÀ\x0005'\x001238\x0004#1]Ñºp/zpmÄ¶4²í÷@ª/\x00113·B3MÍ/W¶\x0011ûØ÷\x0013;\x0019\x000b%P4/¥ñÊÂ\x0008ÁÇ_Ìj5!KQ,\x000bø±\x0017Ùúí\x0004dË1\x0011\x0007å=4YÇ/§.ÚK+Ë\x0001+û8c#Í¬áyä\x0001CaXÇÄÖ&ýµÈ¶D¶#È,	PJoP\x00183 ó¼£·O²êß
Ô#1Ã\x0002÷°\x001dê\x001bµÔü4\x0012ÛxÀÈ,f\x00009x\x001a\x001c8¯3òrÌ×\¾}jäíÃb\x001f§2¯Õôêñ­5JÍ¼üQ'\x0014l/¼¡ã\x000f?·
\x000c\x001bo\x0018v=pë\x0003ç<é\x0013 bÙç<yñ\x0014«Äóc/\x0010ÇÞ\x001adËæÎ\x001c">¼ÐÖ(ô\x000ey¨åÄE\x000b±ò\x00051üØI\x001cu\x0003ÒmQÔZ"\x0015È:¡îVA´uÈF\x0014ËÂÞua5St/\x0019B]ì©s®E7Tk4\x0011ËÂÈFv\x001bY³ØnFé¡T>,µu\x0018Vûíã]×!;S ;Ól \x0011"­\x000bi\x0019ÕfØ¸\x0003¥ñ©[«§Ö"ë\x0012¹{]@¡+ÃÑ9\x0016§"\x0005n%\x00117ÔM5\x0011ÛÒÈ¶ßÈ\x0010ï¡MìÈBeä\x0010µ\x0005Ù{²ïÞ­	\x0001E·%sxû\x000bcu1ª¶bë,UÈE\x0017çK¼Ö1;\x000eP±Þ%Ri³xÅ\x0007âÍ[U\x0008W"ËGÈý;\x0006 +¥Q\x0006\x0013q\x00040Â^½×óGÌ|\x0019æë¦]\x000e4ñ\x0004ÚÙ\x001aLkimwÅ¬\x001f1÷/g\x001f\x000b["33´3;.pmhµ\?×Æ¬\x001fÙY\x000fØï§Õ\x001c¶"l\x0011+\x0006ÅÖ!\x001fë+Í,Ü=-à\x0004a)ÑÌÌJíè\x0015Tv
Õ¿kX¸\x0016IÂ[ÎçWÐ9&
{èV)Vff£ \x000bê\Â\x0014\x0002àWW7)áùßÿù_ÿüß]]Þ5÷¸\x001b,\x000b#Ã^V\x001e%¡#´[³á¯\x000f%è½ÃçÇGg_ÑRB\1Ç\x0015C¸ÚÂdÂÕ ¢âÐCÚæÚðlÇs\9f]ò<å:\x000f U¬»5}Ñ«ç¸z\x0008×X\x001a\x0013mÃææià¹£	-bk=N;®ãÚ1Üàr"­¥¦5ï0g\x0008´ÛÞ·vZ?§õC´Á¢n2®Á¡á$Ì\x0007³·ÅzÍ¸¼Ü\x0018Æv\x0006Ð\x0019××áb`ÊgÞaóòâUãCï\x001aÜÙxy\x0000Ú	ÄÖÝ·\x001d·xÕøÐ»&¤CÑ¼ëhOÀÝæH´ó\x0016ï\x001a\x001fzÙ@ÄûÌºLB06¶Þ:Ç¤·xÛøÐë\x00065!¶^ëd
§å»ýfºW\x0014¯\x0018zÝ$LÊM¸çòÍ|®mo­k§-^61ö²Õ{\x0003	ÁÁâ¥¢za¶ô¶ã\x0016/\x0018{Ù|\x0016h\x0007^ÖõÙË1[ãævÞâe\x0013c'[8ÏP4Ò*	åXé¬:ónËÿ´ó\x0016/\x0018;Û85+Dûã h\x0008qà\x001dØ\x001c¼³rX÷ÄÎÓ>w{Ï\x001f.¯ßm®ß6Î{Ó&\x0017\x0012SÌb\x0007\x0017\x001c\x001bÈ¹×KáÅÙÞóó£Ï\x000f^¿Ü^È\x001bÉ}IîÇÈCÚok,kâÂ<
çKAF;¹\x0004r7/\x0007é!pMÚà9Þ£r\x0012µÁÅôü
tY¢Ë1t\x0010(RYp\x0000¾Ñ¤§´Xvº\äj\8l\x000b\x0010^³=ÓIX¼ÂYÁ­Kn=È-Ð=
Ü4\x0014²q¤Â·Xñ´Üäf<\x0004z¤\x0003c¦e.%\x0019}Qzk\x0005¹-Éí\x00189$¤\x0000º¿hrWYTYAîMÑ¹¡MQ;õÎ\x000c¥\x0005ÂNhiWÔ[CÁ5èáü-Ã\x00008yAþêæúþòêêæºÜ@\x00121	½2'8IYoñ¤Ë7g{¯N^¾>:>>y¹D.\x000br9LîÐ\x0007ô\x001aåñâ­e]±\x0015äº ×äy8µz_
$WDn\x0017o×VÜ\x000c£f´5Y?3S`·NRXO>ë<ë
¡³àf!¹dMàÖ©	3Ëoh3¹(ÉÅ ¹kî\x0014IJ\x001aÝcsõ­\x0010ý+ÐU®ÆÐaêP# Æã;jI\x001aB,Ö\x0001® \x0018\x0000¹gCä\x000b\x000c¡M>Ü*Zè\ÛÝÙ\\x000b]\x000c.tç046RâÍE09Ã¬$_./_A^.t1ºÐ\x0005]`@]\x001aª\x001bÐ)ãr±\x000cl
º-Ñíè;ë<¼¢\x001aw\x0017kÈèr±²q\x0005¹)\x0016º0c\x000b=¸."\x001dFÚr¬íçÖ Zá\x0000;Cú\x00030v\x001aRl ¬*V\x000enÇ\x0013º]¬nA\x000f'ÇO¥ \x0014f*\x0005\x001f6\x000fUbR;¼)\x0017 ÒòðS7ºjè\x0015{~zôâà|û-]\x0002÷\x001cÛ':×\x0000;ÖvàuÔÀ\x001dvï\x0006àåÖ«&à¹ÒL\x0000.fV\x0011CóN>~\x0015ln\x0013Ø"­ìrqf\x0013±ÐÅ\x0010º{QhÍÓ¦-\x0018d_Ss´&ØV=ýÀ¾\x0004öýÀÎP	ãT\x001dv~HÑ-ÝrKP\x0013²äÅª¼{U\x0018F·\x0001YaRS(CVp÷±\x0013dS"~dEÃ8hºz,òç`rûîuÈó>MØÝL÷Â\x0008/\x001a\x0007æ\x000e$!ÒÂ0Ø\x0010Ü(\x001f¼\x0003d[n\x0017¶»piX\x0008 ClV\x000e\x0004ª°p±Ó\BæÒ>ÜmÜ\x001f¨QìÕÍ]£þ\x000e\x001b\x0018Í*\x000b\x0011:\x000c\x001eJ×úùîo\x001exzN}b¯NÎjªeöqìhSìØÇké®Ñ\x001a8^={OÞ´Ý.g²×\x0015¼®×cÏ<HæÒôâx]ÞÿöÁu¼¶àµ\x0003¼\x0006q%(m ®!Üí ¸qR wO¨'Å\x0008ÌuÍV,+\x001d*ã©Tsa©«-OH]ìEÈÓ
\x0002cë\x0006cµ]bºl©EÅ-}k#VÕ%L'NÀÆGjMÃÙvm©µÈº0²\x001e0rp~\êQQ9ë.t
È ûcGÌåZ\x001e0³2 ^ì\x001c¼8\\x0019ÆÒbv
\x0013ÚÛMag3`gÍâ!\x001díÌq`8\x000cÍ¢Õ¼]+~5sag3`gPþC;\x0010
\x001d\x000bm³[&ý¶1»Ù
0Ï¥Æ6\x0015\¹é
ÿ¥+»«?ÚèFv:*æ\x0001:¸C©K3\x001c,Ø
Ë¶®e\x0016c´Ùq\x0016u Yx& r´ uÃ\x0014Ô\x0005h¦D¼Ã<å\x0010ÆËRñ\x0017\x0006Þ\7Û
Zò0\x0015 S\x0011DßÑQ¶Û+¹gr¿0JôäeEÄ5AÏ¤ Â°\x0018ý¶\x001e\x00040
±\x001d\x0006~ÖnÍ/v`Û\x0002Û\x000eaÓ4e\x0001\x001a\x0016éê\x0002¶Tþ¬Ûªg¹Û\x0015kÄ¬\x0011ð;pð&TÚ\x0012V#î­¾èjn.
n.À¹Ç´\x0011\x000c¯J=½ $}z\x000etwÆ-Jn1Â-X^ßZc.\x0017:H\x0014Åyíàª\x0004WàJ#¸#ùÓ\x0000NÊ[£Ø\x000enSrAîT8\x000b*8(¶\x0007CiÉàbyªk3¸*W¸\x001aZá"àá«Iý{$÷Ü:¨q=·.¹õ\x0010·\x00144¨\x000fÚ/pKá»ºíe9ëÁm	nÀ¥ª9Íp.¤g\x001c­p½5±Û\x0001.Kp9dq\x001bã\x0008n ·/óÿºwY®#Gò¼_»Y5
;L+JÉÊRnÆL¥Õô&XYO%õPRMu­ú5z;«®çÈ7é'ùà;NøaÅ	D #Íh¬¼ü\x001cÃáþw\x0008Üï¸6åY\x000fC}À\x0012U\x001eñú\x0001\x0015KÚã¼ÀÏ\x0006ð ÁG{¼I*I\x0005C!\x001cä\x0001/70î\x0005¼"¸ÖC#\x001e\x000e=®óñ\x0013kê-xKS%©ÙØÞ\x001aðt\PjAÁÁÿ&íª\x001f»ÛWp,UÒ©[H0t×IÎ.ß\x001bH¿êÅf8Ü\x0008r3FÝXOäÚQMe^Ôx#¦Ðqyè&wÜ
»\x0014(Ø®ðª¦©#µ|ÖWÙ@î\x0005¹\x001f#³·°û&%@±taKó½m7'AÆÈ}¢ü
,\x0006äiÞåJÍÖ^àp´@ÇV¨s-¿"oì¨¸SâÄ1Q"Ù«Ä*tPG÷ä6ÉþïÿøÏÿô±smæS'q@M*ÐFq\x001e®_H¬8{ù¯/_,¡jª7¢V\x0001ÊZÚïUÔ_/Ã¬^\x000c«ß:¬Ö·pÞp¯!\x001d|wÃ½.V1®~ë¸¢\x0002	³jz=ÊN_C]êÐj\x0005ªÝjH¦ ¶\x0012\x0003g\x001aëÂ{m\x0007ëT4<ÿåT4|\x001dl\x0015Ý®)î±jÿ!É»\x0000K\x0012ç=¤r\x000f­@@
öÑîë¨bý-.iKô°ZÉj·²B<§Aõ\x0016US\x000b«oMcÝReO\x000f«¬n+«±¦¦¤âÀÄÖ>\x00185\x0006`­ùYª¯ç+½T__\x0019ÃÃN\x001eupu>9dª49õy§XTeXvé\x000bô¤<\x0000¡ÄZhËw?Ôb\x0007')j(­PÞn\x001fh­ÅHk=0Ò\x0013½µÑ­ûO>()ZêÓ²Hq/´Ð\x0003#ç\x0004C[ÕB¥ÚS\\x0003w· ½ö#Ð\x0001ð
$\x001a\x00147\x000fÅWÅÜNæ$Ó\x0008³afl~êh\x001djÅ1é\x001e$}ÐÆ\x0008hcFÖa¢¾\x0002ÚæÙAÁ#Ô½£Úk¤­\x0015ëÐÚ\x001d/qÍ¢³ÛN+ ÆÈ*Íß6ÖB;	íF ¹©U>íR\x000bD· QÙjÜµÐIB§\x0011h¡gÆ:4t)ªÈÍ7Hµ¨\x0005ÕÇ<í0eÌy\x001eWñ\x001cíu@!ÇÚmÛÔä¿ØiÃsrv¸¡ÙQ
´\x000b´ç¶/è+R-«ZîîÜÇì`öj¹õ$ÑXSr<Ê@Ó\x001d$OÄáe\x0008pü&\x000eV\x000e}={~ý÷÷on¾ô9w6EjÔ÷càD, ¦$ÁÅ\x000cÝ×gÏ/þõéãË\x001fO#©"}d&^þJdá,"Ö¤Ù%rL<\x0016¶ØJb»8Zêl¥Âáô\x000e3\x001bu\x0015JX\x001c$rØï¨!´êÃ¯¤\x0002\x001dÞl\x0016®þÝÈZ"ëÍÈùè\x0003.lÒE\x0001\x000cëB¥¥\x0010@7²Èv;²ÆJ=F&õ"¼¢´êÔ]~\x001cö)ß>/44%¶XÚ\x000cuxI
±\x001bYKäíó\x0002\Ó\x000bËÈµA¹òA·y±Ôs°\x0017Ynqvû\x0016\x000716¥\x0012\x0014ùpábk5ûÒ½×I^·W¥&*§\x0008)í8
m[8­;½\x0016Ä^o'\x0006NP2X\x001b#(\x000bM-¤}æ±÷\x0012ÙoE¶)(îD\x001e°â£\x000e26õk\x0005á»\x0010\x0007é\ÍÎMõkò4N¨«âv\f©$yØ$ùr\x000e¢¸³¾º}ÿ×ë^ì\x001eã=Ê¤1Zw\x0006ÏÈÀ\x0015V¯®þtq¢À\x0011y§ºÅÈk¶\x0002cpZ"`|àÇ\x0004Ò¦ {qu\x0000Àà·\x0013[\x0016fÏ&VÓ\x0005 /\x001f]\x000e
t\x0010ëIr\x001d\x00127\x0012+Ey0
ESè	Ò±\x0018ØåH\x000fðTI\x0017¥îªY\x001c\x001d\x0017¼ú¨ñQ¤>\x0006>¢ÕÒ\x000bS\x0017±v\x0002Âkl\x0005´ØÚL¬êeO\x0007Êfð)$îñéç3vV\x0012#â°Ø \x001b_£ªº(lÎÉQÞ/·8M\x000fÒE\x0007¦¹ÚiÎÈÿÇ^~ür{óöÏ×½½<]uêI|©Õ\x0011O$Ç·¬³Ë\x0017?^]ækêìLäA1rã-ë$:ké=\x001dûÌ3yÓëÉ'y¹\äån!÷Ñ_ËÏ-µuÈä,\x001f®ÒrFñ29øR¸;i\x001båh\x001bõõì§÷7_ÿv6áìé(`L"Î\x0006ê¤©\x0001<ò).Þª~zzùúgåo9+Ëi3L\x0014f¸\x0019>EjN¨°f(\x0001ÅX\x0004\x0000fK¶[\x0011¤\x0015a\x000f+\x0012i_)¬ÈI\x001cè5Í\x000c³\x0018ûXkÆD0\x0005ÍHj\x00073²3HûPÞIë2\x001b°t®6À0ÀÂ\x001e\x0006¤D\x0011ùP±TeoîóÔ\x000eÖaÄ¢°fµMF«kc\x0001¨2V¦CK\x000c[ð\x0014Öáå×ð;|
L
§,1T|Ml\x0006×|%·Ôod\x0019Z¡÷0\x0003XcÅD`¥pük2Ã.yA\x001bÌ°Ò\x000c»\x0019tMÍ÷%òðñ¯\x0013±µÞ 'UØeRnÌÕ\x000cM-@ñkh6cI¬g\x0019rïs|GÖ\x001b7Þµ×nË\x0015ÉÉØÝ×<1ì\x001e'\x0006.qCÊQ\x00072´?^z³ß`ü\x0018iaÔ¹ªû­±ö\x001e\x000f-·\x0003LËq½F8%>S{||hÐ±Tfñ}wÛù­
fh#sÙò/D.ÛÍç³ç¾t*pÚ\x0014]Û7÷&\x0013)8A0Ë
\Ï_þxB|\x0004vÛó\x0007Sìðyì$B\x0011´DG[1K\x000e_'°#ì70¦ßÖÛ\x0002vt\x0014£T\x001c-1
ºx§bx÷H\x000co
oö?icÁÔ	EÀº©¥\x000e	ß\x001e`#\x0006XÍ\x0003¬©MR¾Â;êY;®]ÕÌ:x§Íq3¯h»7z.±É\x001b¦TG¥û×\x0015Ç`\x000f`'fÄhÜ\x001a`£±o½$~_xHÝ\x0015ñX\x0007ì%°ß\x000c¬\x0003å;bN\x0011õ®ÃÊ4Â»ÀF9\x001dâæé\x0000ºÁ\x0006x\x0005Ö±z£ÒKqÀInÚ:º!\x0001%f*ìíLñ\x000fÐo¬í²ºx§/´è¤©­\x0003\x001c°_}$ÞÄñ&0)ñz[ì#Ú\x0007,7\x0008»y\x0008QazA\x0001N-ã.\x001f\x000c¼x_è\x0004;°Ý¼\x0003Ú;Ú åJdP¬´½®]ÎäI`\x0001¶½¡¤5Dã&3ùdã\x0011^î8Ü\x0007,·`»y\x000b.ÝO(ÌbËàöÜX\x0016cÀ»\x0000K¯ÇnözBÝhë\x0008'êOWº©\x0011ð|\x0001l'°rð³^pP¥\x0017ÚûÅë³ï>õya²Z]vù4¦\x0004\x001fÈ^\x001b=Äyµô\x0000^ª¼¾{yªÆ«@Oò¨\x0010ÚØ\x0001èÚe±¼\x001e\x001e¶J1s}=tËz½ÐZBëÍÐ\x0014;,\x0015¡eèÅ#¯\x0013zÒ¸\x001e¡eãúÐÚSËï|8\x0007ÎÎM#Á,Îè^h#¡Í\x0000´r,<\x000f¶}XSLÐzYU²\x000fÚKh?\x0000mÀóËDÞI)'\x001f\x0014.óv±ÉÏ"3;	/å+\x000bGÌ¯>dÄNèä\x0003GÇ°ø\x001aBx­8	Óvô«gùoXÀ\x000eÖL±ñÇ­ØEõòª²\x0011à\x0011£Å¥\x0010Ì
l'±·vÆN¬\x0019³¯¨¡BkAlÌb·NlpÓ4\x0004ó\x0008d\x000e÷JnT®®ù?à;uæ=å\x0015Y
\x0015õs{'¹ýÀxçsBØà%\x001f°á/qw$r÷rÇ£ñCãm1DT¸m+,óþ²ÓôIÚ|áyó«¹©X\x001eü¡\x001e6zMBe-í
GØ0m\x0001%C
7½\x0012qs­\x0010î1{qË½»ü¼Û\x0005ª\x0007Tÿ¬\x000fM\x0010c$n°Ë\x0005!ÜÁÊñ\x000eÇÎß*î\x0004ÔV\x0019Bk]
É\x0000ä¿Ük;	á;\x000cpkÌ «Z×Ø/¬R[C³;»T=\x0007|\x000fuÔ:\x001eß\x000fVQCkn\x001eQ~·®Êä#¶vËÅ½ÜG³$Ì\x0012­
=£BL\x0006óÊ
wÂÓq±L7·?âö#Ü¦\x001d:	\x0014	ÏCâr8,jß\x000b;\x001da§!lÎ\x000fÊË/ð&\x0012ñF/\x0017.wr'%7Át|¿Y7M\x001cu
\x0006Ô5 \x0012|L:$n³:ÛË}4MÒÐ4±®Æÿó®\x0012¹=Á¡NÜ,\x0006§;©ó¿SP·S»¦!­+\x0012a\x0003\x001f9\x0016Ëj{¹ÜÇw³uÜÜOZãÝ!\x0004æ&l·×¢Ôö\x0008ûÎ=x
6Ö\x0018Í\x001e\x0015	ÝBäE\x0019â.»È OÂªùp>Rº]}ÂsA\x0008\x000eè)#ï+<»Áõ¨Ýv;AîFÈ5¶
!pO5Fyc\x0001v©æc<\x001bÀ­\x0000·càÀz3¹¦	nQìT¹Yç{\x000by\x0010äa<Q\x000c¢LÄä¾ùlâ\x0006r'ÆÜ¹T\x0006XÉCà!´Y>[\x0017³\x0001<
ð8\x0006ð´>[\x0007"£óÅ¡G\x0012´\x0017<	ð4\x00065ä¡]yªBBÞÇS»ò¨}æJI\x001aÞéÕ£p|¥þ©S°Üå{\x0007:«d¹#WcôqI~©0?yBc½\x0010Ç©g¥\x001eÅcÇj\x00051ÊEUâÐ\x001eÏÑI$bßåt\x0010[1Æwn\x000ck#×àªCi\x0001w¶Þ,>?v\x0012G9Æq`\x0013ËàÿÁÔ×JLI6Ñ-Öàv"'\x0010È	¶#S¼Ø¤¢ç4\x001b(^\x001cÝ|ÈZÌt|\x0003^ÁxGÈ	+ª
rðd¯zåÄH\x0003\x0013\x0003t	 2æ5\x00112tctnIg \x000f\x0019Äi¨\x001e72«|3Ð©2\x001bBË\x000bS;]Ö®éb\x0006#áØÁîf¶Ù;*!\x0006dÆVJÆ\x00023®\x0000Z\x0007³=b>~EXÁ\x001d
¨ý:\x0012jî×$\x0000\x0003¼Ï¹Å\x001aíNf'wæòóFfl5Z§sÌ\x000e\x001e\x0015Ùás{E¶a¾ÁV'²*LkÕ2O\x0010y\x000bOÊ?qýõo}Ì
IË[
¶\x001b©' V©=1-Êýpöäåóç¯_\¼þãiî\x000c\x000cr\x001fu^\x000b§@àtêó&ÈµÚfq°û¹ä6#ÜØÖ];â\x0006ÜKÈ\x0015Õ\x000c¾x´ôO\x0004¼TÜ\x0000\x001e\x000c×éF\x0008|À\x0000p;`³¼ó­\x0000#îF<Dó\x0015på±jMö\x001c©søzÁ£\x0004Cày\x000fL¤ \x000ecÑQ.ÑoíýàIN44U¬¥{Wã,ÿ\x0017bhs¹çu'ø$µ\x001aÁR«×kwÎ\x0003\x000e-/Êq¾½\Ú^n\x0010\x0003®ahÀ±IÓ\x0014w$<^Bxï¶6uàq\x0004\x001cu+h¦\x0004îÚáSòm7Y}ýÕà\x0013I/\x00047f\x0008\x001c÷nâùRS%\x0000\x0012¨¶4\x0017½í~n9àfhÀóÍÚ»Ü\x0012?ËNJ<ÅýbnF\x00078èÒûz\x0011\x001aúðÍÙ«ëÛ/\x0019¯ÏëÎ\x0013õ\x0014SI\x0019º\x0001jý\x0012uêP:¹¸ú1ÿ/§µDÖÛqt©æ6å\x000bòæÙNëÑåW¦.ÞÀei4ê6óæ)ËÉ\x0018*X?l\x0006eÝ:»$îÕì¦©îáò7+}Þ38J\x0006¨ÿVN}Ôä»zX¾#t"\x0007\x001c¶#G~~Ä´\x0006 D´Èû×\x0005G½ÈI"§ÍÈùZP\x0015Õ³¯§Hê9#³è_\x000eêu\x0011{+æ·Ûç\x0005*&Ô·RÈJ¢ü3KwÇäíl^d\x0015ÓÄ÷éÑ/6²èÞ­s[\x001c?ï*NáÒ³/`2àm,\x0016 'IÙ\x0011¥\x0006¨1\x0011¨µç¤ì¢&@g³ò\x0008«© v#ÔÖ×G\x0001T1\x0007\x001aêdH\x0014Wy×Ñ
¯\x000fÚ\x000bh?\x0004\x001dÐ­«Ig"Õ\x0001\x001dN:\x000bûQYíG§ujÔ¨\x0003kÛ+lt»\x0013u\x0010c\x001dÆÚRÚ>&®2'ì\x0010^ÀfË9ÖC¡\x000e#CmD[3t<Ê\x000eÁÎ`ãÈµôv2ÎXz+2Í2Ñ_>}|×[\x001e¡«âºÉ\x000fCÁT\x001eÁIû!%ÍË³üç/_|·\x0000=Õã×Çzüë ±<óî\x0017ë\x001b\x0017U«å[úrÆj'±\x001cf=2ÌÆp\x001du©4É\x0004ò\x001b\x0017f'îÃl@0\x001b\x0018`Fzycúæ¬¼¡2\x0003å½Nè ¦	Û§\x00066ÑòÔc:\x0000{J¥Ä¹Ê\x001bÂb¹~'ô¤Q\x001dW3®öØæÐÚ¥!':Úk\x0011Z9Òv`¤ñö\x001dêôpZÓ*ÌÐ¬v\x0002.-&:õA\x0007# \x0019Î7,W·à=gzB\x0000zÒ0aI\x0011µ\x001f:Hè0\x0000mÐAÓì\x0008èL\Ò*êa.2vÓÍ#<*{Ç×\x000f\x001f¹ õ £°\x0015k§|Çªm^t>bøò­çk __>{ÆÐå7§µ`Ö\x0003ÌøÙ£Ôoa¶\x0007ä­ ¶\x0003Ä\x0018®\x0001°ä\x001dçì%VFÅõ³K°\x0019´\x001d6ÁÝ:1
0\\x001c_\x0014zH¢U¹ÙTë´X©[µ@Ö\x0003È_]\x0010\x0014UtjëóÝ¡Ö2G1Ìq`â\x0012A\x000cL\x0007­áêb=¯o¶\x0016y\x001aJÒG9W+uU¸Ç]Þ<&Ñ\x001c\x0016Õ~v\x0005®f\x000e9\x000c0¦ºJ^2EÌ3Ä:\x0000NÛ:çÕ\x0017YÀ\x001c~1»\x000b2(1ñÇíÜ²pý±\x0004æÚ~=_[·\x001a\x001a$4\x000c\x000c´¥¦
_´|}ª5ö°\x0002;dû µX \x0007 f~\x0013´Òm×p­Ç|õåZh#¡Í\x0000´k
]ù\x000c§RWlðÅÍ\x001aÌì=e-´sÚÌi(©b\x0005Ú³ç4ú5âB[%ïÝ\x0008,ïÝWïßþùúö]_x#YßZ6dç¹\x00166\x001cduÇ}ðêéß_\}·@\x001c%qÜN\x001c,¦-ÕQNÃ\x001b\x0013ka"ò.ÈF\x000e²Ù<ÈÅsæS\x0010\x001cU,j¬gäÅ×ØNäÉ³\x0015"g«uÈæÐ&ÓÇJÌé°	Òò{J\x0017ñT?\x0008óôvâÄ\x0005uËõÄ\x000624È\x001ayÈFÌ\x000bY¡³
9ß¬ñä«ÈñjÏZí´ú¦\x0002\x0019Ù©í£=¬ª\x0010!¶H¬À:°pâ|aÎJ`#Ív`Të¢¾
Ù;Ò4-Z\x000bvl³¼\x000f²Èv;²·(vT[M°Ú£Áì-BEq¿%de¼Ü.ò/ävñ\x0019»Þ½ïË~p\x0006T©ë3)Æ<AH^6XÚKïò?`Ï»§ó)\x001b\x0004ì$°Û
L;2\x0002'Í
êxÏfà<\x000eà ÃvàDÁæ|Ò%î¢Jë.ø¥\x000e:´IÎ´y>hÎóØü¢ùÓ\x0002>í\x0003,7m\x001e^Ìß&`ÓD·#M^$_\x0016së\x0000J3a¾¸Ú\x000clÒD\x0005.\x0005puy\x0002{³VÒ	\x001c$pØ\x000cl0ñ¯\x0000£®\x001bMà\x0000´Ex»xÖu\x0001{+æ°·ç0*ÕÂ\x000fðæ¼Þõ¢4Àq¹0¼\x0017\x00163¢ü¼\x00118ÖZÐ4æu\x0015bO	ÿû\x0010#â­s\x0002\x001bÑxzA3'1V1±íÈgí!NGÄi3±ÆËh%æº{|\x0005æ§Õ4\x001bké%¶\x0011ÿö\x000cÏ£q,coßßt¾a[¯L\x0005cQï v¤
oÓ(ÿ¾äP<»@î«§'\x001e²\x000bz<8dôx,­³\x000e\x001dËòHìEããN-þ°å¡èÑ2êB\x0007\x0002½ü¼ÝDïP/\x0005ÙMU¦\x0010ÐE5v	¾,ë(#sù\x0017Ç¹/\x0010yÐ­$boÏ\x001a\x0013H,Ä4s\x001e\x0016_M¢½\x0014j;BMíH£3ÔT§\x0008Ì¬g3ÓÖ3;Éì\x00061OÊ4l~ê±dçjä>j'©Ý\x0008µW,|\x001bmI'¨×\x0013Ý\x0006{¶cû
ìãxâxÆ?ßüåýÇ3jËýæúkßFbeÄ\x0002ä>¹&7\x0019ê'¿¿|þôÅ\x0019µå~|ñú4t4\x0002\x001aÜ
ÿ]t\x0013X7Â\x0012\x0016h"FFÏêzwCç\x0019b\x001a!p(ó2¾úôöÏ7oºÅ,=*÷RòCÔ
\x001fð\x001dò\x0008²ß;·÷\x001d¸¯^æ¿~|R³ Ow~¼à¶ýþ¯ø\x0016ÛwÄ{ÌË¥Û·\x000f¬V¹Ätû\x0017M9_Oþï±KðNÂßIU[\x0007¯"iºeGØS¥Mç\x0012\x0004Õ\x0018¸\x0004ÌÑ;}2åþ0g0Ëîöúã/7hKß´ÉëÞ5øD¨t(ÓÝi?G6mwuñâûK´æ4¿vß\x001a`ó½·*VëÒ¯)Ókë>Àlø#½ôzëâ2½%Yål\x0000çÂ¢¨á¾\x0006Xi\x001d5ÀäùÈ\x0000®\x0002Ð%ý \x001a ayÛé3Àb©zééQ\x0011\x001bìô¾Þ¾é^º6¸H-Õ\x0001'?µ&Ö\x0004Þ»ÙÔd¯ùúêñ©\x000bF\x001f½\x001få=¹¼\x001f\x001dÀ_½ÿØÙÚ9ï1î\x0015iªöuID W`V\x001cðÀüêéS×+Á?nãõØù¢ÁFQV\x001eòr#|Þ\x0005xª?¡kòÀ¦ä>R,¸5ëöx\x000bzV©x\x001d¯¼n;¯;§\x001e\x0003(Ói\x0008ÛdÌ9ë`½
~ólÈ`\x0011å¥lè¨Ï³¡55
\x001dnÊi`8~c\x0006-
ö°úgüÿ®nþ½óýÓ%\x0011\x0010µ¥#^'º\x0011£ÆÀr+·ç\x0017?àÿwuù?O\x001b/ÀñÇÍà-OÊ\x0002åZ\x0005<(\x0016ÿ[z#XÁ=I`BnÑµm=w¢
\x0000\x0015|Þ\x00107ëÍZ=Û.y
¸£d±|±w\Ù«Oonn¿ôÀ\x0007:@(úne{VÊT´z¼Á«/¯~?T]\x000bv=Èî[E_ðÔüCCøåNÏkÐ@¿ã¯CÏ\x0013&2:à»BEW­²¯#!«]ÃÑÍMC½¹\x001dæú§¯\x001fp[üzöýÍõû¾;DÌÌªJñ8(YÊTdËIàv©\x0018#Ï÷¯áöøú,ûQO\x0017\x000c0Ò\x00003l@Ò\x001cVvÙ¥%ÝvtlYì½ª×\x0018à§ÉZy£ÐnÌ<?JSb@H\ðÀÊÙ4[v´Â\x0000~þú¿Ò7_®e¥øïÙõÙ\x001f¾~þòþ-ÎõP§KÿË¿¼û\x001f\x0017·ï~ý¯·¾AX\x001d±ùQyråð/)ù\x000eíª~IÞ'ÍÄéþÃë\x001f~üïþÇÅÕwù\x0004}ç8þæéËGï?¾ýôñã×ö\x0017Ç%¦Yþøv\x0019Ë
RÛã¨Ñ]*|Ãøò\þøv\x0019
&Ì?¾]ÆÒå¼üñ
3â~_þØÀ\x0018ña¶"tRF´µ\x000c\x0016\x0011M\x0007áÛëw×¿Ü D üñíbé1Qþøö\x0018ÿÝÄëkÜÁqÓ\x0001ÚyWÑÖ\x000e@½
Kå\x0011
`C*¼\x0004{c¡F5ÂÜå{J­spöö/àþþs	\x0007<zäë4¼}ÿËÇÒ\x0007¹køð9\x0001%kòðaÛÛRøî±Âf!æDÍã]=ýþÅåÕ,ßûïþT\x0006ozB?þõ\x001f¿|}×û}C\x0008ºÖºráòyQ]ØÒçu'\x0006ïñå÷¯¿\x001f¾W4Ðà[æÓÈ§¿Y>¼¢?¾)¾_>9ïþÓ\x000fË&òÿ}~½ÙëÏh	Å§\x0012íÐ6v£>¬
\x001fgwèçÙ½ø¡\x0003
ý\x0004üß [iàZþø\x0006áðUèQùã\x001b\x000b¸\x0015?¾E8\x000c±?¾E8ôIË\x001fß \B®ômÂ\x0001&?ª~t%Û¹þùíÐù_ÿôÿùÉ\x0001ñêÃõÛ&ñ{ýþö}·\x001b\x001a²k\x0017Ê9\x00160VJ\x0002=\x0018ï¡zy&N\x001d0_=»xÒ~/^=?Ò&ÄÙ\x001bÐCÄ¿ÈÄ®¾&eb*\x0015Eb\x000bû\x0012çïd\x001eÖ\x0018Û|þ=¬1ÎëË=¬1öù\x0018\x0000cþ÷ÿú?ï>Oö
tu?}ýpÝíê¢Ú~iíI±J¦t÷\x0000Ñ\x0012©
éÔÿñË×Ï.N¸»\x0013Âº7|»Q\x001d ÐÎ7Ê(Âxß\x0016£þ?ïàö¯>}}wûþ×ÿºíÌ®BíZà<\x0006QJÅ¯WÎÓÍË¼z½zùú»Ú»\x0008YÒÂÊ\x001fß6&þÊ\x001fß"æßnýÿþ\x0005ä'Ç\x000c£wÿò\x0007J1ê\x000b÷(]ý1\x0018å\x0003OL\x0017]¤Í\x0012{VÌsbnÑwg(ÉEs¤ßýéïæM!
Ù\x0005éßÝüåÓûÏWÔëÿEGùÿlªØG±¡DÄ\x0010Ã\x001cñ´0ý»Ëç/þÙEóþà\x0001\x001dÅHÀíÂ®5Åþ\x000c\x001e¬\x0015^óp£¨éîðøw¬¹°\x0005>ï\¥$\x0007á¡vbÉð\x001eØ\x0015\x0000µ\x001b¼?}üÓíÏ¥ú9O\x001a PÒÍíÇ÷ý³;YìçUC­¨R
y­CM2
[ô\x000c']½xZòæ8¨ÎÁgù·þ­LíÿñÉõþM"ÄX\x001fw]þ«XÓä|Þ\x001a=ñA8Å÷äâñÕ<\x001c^ìi8üâÑD/äw>~¹þø¾æôuá\x001aLc ÝK¼½SgJ³¼<\x0003~÷òÅ\x0017/bVßÜÇgò ¦äSI§
èª´Etìæ	]GBÏ¿õc7 'ÆÐ±°>Utç)Ù\x001fõEiÝi7?K¶ ;îÐ¹\x0011RFÇ¦¡¢'g\x0018]ÍúâëÑAQ\x0017uC\x001bØ±ñ|Ý«µô\x0012¢òu\x0016§¶û²kÉ®ÇØ\x0003Ö­Wö¸=\x0018f7{.T\x00009î06î¾ªÜ9£«`»Ï\x000bªÖ¶à¸Åcf\x0005»\x0013Ó]Ô\x0012m`ÇM<Ð¸SµÌn¢ksfÖíÛÀîå¸û±qy¢xbwçÆ\x0011»gv3ÉÚ]»\x001f\x001awº±[_Ùù×Ó~ãèA¢1tPU]\x0000ÑM-\x001bö¨È[¤±{N(Ùã »AÉ¢Â®IÇ\x0001ÙcbvµÏ¡jÜÏMH~a­\x000f\x001f~ýÇÍÙ\x0007,{þpýþöæË5¾¸Bý0\x000fNQWì'Úg|ï\x0017\x0019÷òì\x0019??»xzuùã'|YÆ·\x0002ßîÁO\x001e
tqL!\x0004\x001a|?-&Þ²Ûd~ÜlÆøóuÂU|\x00084w tU|\x001ffC"ÛðÅðûáá÷±J@¸ç{-ÏA~G\x000e¥·0{Lmâ\x000f?ó\x0007Þw°,\x0003xúpTäõîÀ\x000fZL\x001füqÐ\x0000ë«R2\x001a k\x0006~6ÀòüÑ~6Qe\x0013¿üfß´õëóRNô\x0001°\x0008
ØßJ~;Ì¯\x0001«ê
?x¥Ê\x000f®M ·ï\x0004rÒ\x0000·\x0001ß\x0019zGÌüb1\x001eÔ¾\x0013Hî0¾æÛ8=tx\x001bèro>}½Úù\x0003\x0004i@Øã\x0003Äêé\x00171¥:}èVë\x0012Ì^¯6ÑGI\x001f÷\x0018~òõ±¯õ<ü4\\x000fn2 I\x0003Òøðk¾àzåyöÓ
1\x001f\x000f»\x001e_T¤Éô¥HspûW¥©Ð«ZîæQLÎ²\x0001z×å«åþ¯Ç÷ÿ<ièMÈ%]¥?qÿW¼\x0000½´l2@îz|ÿÄÑÄïÿ\x001aØÄ?Èº_:pzÜs¾ö¨\x000b= \x0017y	D·¯\x0001rÿÔãû§×Ø ¢\x0018\x00003Æ/ì.¸}°Üôø\x0006äMóà®UqÈ\x001fL;\x0002öå\x0013(O P+?Tý,äWß\x0015lä\x0005\x0018\x001c5\x0000¦Sqá\x001cEÑsìÂí{\x0006\x001b\x00103¨ôþ\x0019A¥\x0010|8ºÁ°÷ö]½Fýüöø\x0004xûÀlÃÍ±
7\x000fÏëc\x001b®G}ÀW\x0019´Á/j]j6ì»\x0013e\x001b~9¶á÷\x001dþ|lÃ\x001f
:¶áO\x000fÏwÇ6¼{x6¼9¶áÍ±¡TÝ»I|ÅBUÌf\x001d¯55çìûO_»\x000b±bÈ÷Z\x0008\x0013LâðÓõviÐó\x000fÖ¬çñ\x0012t¾ùz¾(\x000b«ud\x0000Vî@éùTREôÙ»àq\x0007­N\x0005¨\x001d\òÀ'NqI0ûqõºfäÿb&>1äl¦Èf\x00009ïÿ@Èæ¼N\x0015­ZJQÒ³C½\x001aÙNífd\x000fE\x0014·f¹úÚ½%ÿN·L¢8ÿz±ÙMÝvfåð\x0019½\x000e³«J\x0000\x0019\x000eãlgäjæ0e\x000e\x0003ãì\x001b°¶4ÈÁ5àÙ\x0008Ûjà8\x0005Ûu@\x0008\x00185(¨-\x001cæÅ~c¦Èi\x0000Ù\x0007\x001ae[;qgd\x0013-²Ùmù\x001d. eS\x000faAnÌÛwflÓÒaýÕ½v`îa Å>\x0007\x0003\x001b±T\
\x0010è§t´£»' 6:\x0018Øé¬Aaj\x001eiO#íá°qÌ^NWC\x000e\x0006¶:\x0012ð%hZÁµÙ1_7±Yì\x001c0°u8ÍN¸wD\x001dA·#e^5a-´\x0016{\x001eØ;~»ÖbïÐ\x0003{EHgtõêtâ²<Ð³ÁÆµÐF\x000c´y\x0010\x0003mÄÖa\x0006¶ßp ­\x0018hû \x0006Ú	f÷ `\x000e\x000f9
æø ;\x0006ëUåúAÜUÜ!úQ±ß|Ë7Y\x0015\x0017ä_`¼àHíø×ÿú{"!v
¯À·Ye\x0003\x0005óm
:\x0012;¾ü×I\x0015]OÑï*M¯BÏû5¥Í:]ªü*:ËùØ´/º¢aôZIG=¢x,¡Ç6ê³Oè[Ðí\x0014ý®<ö:tÜIê ·à²íí¹\x0014ïGî¦än<\x001bzkT[ø!:/QÔlàf\x000bº¢ûaô`Ú¨\x0003¯RÎ\x0019ÉS}ö*¶\x0005=LÑÃð|IºúaÂ\x0000£Ã\x0013\x0006ÄÁ\x0019ãRé\x0011[Ý`\x0018(Ì\x000b'öù\x000cñ
ì<MÜ\x001cïv\x0011XÅnKMD7®ª
gtàZ\x000e§Ü;\x0011èf\x0014=òÕÒa«ìêçááü.­÷2V°ÛAö<ØÎÑ¸Gê\x0005%\x0005Æ}>7g\x0003»\x0013ìÿ¤ñÄ*v
¥/9±'**³*N<ìoa{ûàR\x0005Ïù\x0008Î´R½\x0014[F/ûÞÀ\x001eÄ¸ÁqWk]uTwå¹ÀÁÛ¨ÕKµVo\x0000ÞDÃû3\x0014$TÉp-G^«³æ
ìGÛûàþ\x0005oHê£ø·JÐØçë86°kÉ®\x0007Ù3ppmÔ4ðÊò¤ÑóÎ
ðrÁ\x001d\x001e;ôðÏ®MM\x0000TÙéåÕjÜâ\x0013ë
x¹Zap¹b\x00016±ÇHÏÛØx-´çí\x001dg¼VGNÁ\x0018»Në^räÑä#+×³ë
ðG\x001eÍ K£ii£\x0016È/PQ±WfGFË³õuuZ\x0005\x0008Æ`Îk.æ¶mi^\x001dwÓäuÐ¤34ëuég\§½¥\x0017Y\x0015'IÇ°ãà\x0003æ¥¼ÿ|¼çà¯FlÈ¤¼ßcá\x000cM ÄoÎÌ¿hmýÇ6à
\x0018´á·]\x00048®çÑõCGà£vÈ<Î¿(
}µºPøîEO¹ÁÃ£Cà7s«}ßådYil\x0000+l(Îà \x0011ÉèÚ\x0003Hõ
\x001d5Qø^;_À±Ñ M\x0008;àci/[L\x0008XÍ6$m8¦;á5ßáç/Ç_âË°\x001dÚvF4JËü-|8ØÑç®²ãí±\x001doíp¥\x0017Sµ#xDv7Âa]ìý=î¯<±îì¯\x000fen½9þ&o\x001eÞÜÊûíñ7I»|£m·ªaÊm·Ïqí0¥ö:>³`¯ãI\x000bïÇ¾Þþò/öâã»_ÿñéC÷ëVL\x001cc)¯[¤ê	=ÏDÜÎûñË×Wß¿çìâÅw/-Ûâ¦¶¸l	McÈjÅuÈ¨©ÈÆÌ|\x00183©e)MÊw²&Y\x000c¬\x0017k\x000cpMÑíMæD\x0004iÄ\x001a-¬Ñ»YÓB\x001bÖxî&at\x000b]Ã¼HÂ5FXcö²&zºr[\x001b¸à×\x0000\x0007&ñõé>l\x0011Æì¸j(Ë\x0004¬¼h8\x0015Ðb!ð=\x0018cÅ±;~\x0018fÙW¾\x000c»Ygïe?³âÓØÝ>ks>o\x0014m\x0001Jwøö#Ö8¹;ïgM5Å³\x0008*Âïúæ~v3/Lñ;~\x0018\x001b\x000f§?)K+NÍ²6Î§²\x000cX\x00135a/kLdéW"?ç·\x0000"±vÀ(¶¸Û\x0016X\x000e\x0000­±|nrÆ­Ewó>¬\x0011ß&î6Ó<kàY\x0014\x0017âuãÚîåÜLÂ´£5Òèª-D5ìÓøù<\x0001k@º¥\x0013Æ>SM¨%ÀsÆ\x0001~°ÉGÐ}8päpîæqâ]ÞÎ\x0000¸
²rÂý|\x001déqÂ~.§¢T	Wm1-ÍãDòì-r¦éÝ\x0016Nà(+ªE%Þ\x0006ÚÍ9Íkt#ÝgØË\x000e`Pç­\x0013\x0014jÏ\x0014s\x000eoVf>è:btl`?Ï&²|Eö/Ñ\x0001­_'ñó!ÜÏ>à4'ìµ\x000f\x0018\x000e¹ÝN2\x0007\û:'jV\x0006Ìñr²ùýö\x0001ÖçsÙvíêÉê.Erts4'ìf\x000e°·]©¢È È]5ÇÎKm\x000e£¥9z¿À@`Åü¡ÈØ_æ¥ä¬±Ò\x001a»5¤£âòw²üqZ";Qó<bÜØv»\x0019d\x0007Gñ>mXÙ);8ír^XnÄ\x001céKÃnÎ´nBÞøVS­&×¹8m0dÜ§ãNû´Ë×DÂÙ_£\x0001\x001a×Nû\x0008Ý¼\x001bÀnØä\x0002<*zrPU\x0018Õ|BÂ5Ó\x0012ïÜm6\x001c»ñ\x001a¸û°ÑÍ'\x0008ñ>¶éi\x0008ãv3Ç±F2
DÆ°1¬îa>tÄ\x001cé\x0013èý|\x0002OY>¡\x001c2¬æÍ|êý52â¡w\x000by¤ýq«\x0000´Âjôj\x000eë¿yîÅ\x001c¹\x0011èÝ6|rÖP!\x001e§|9Ð©é)ßÇL32F`ö\x0011D.µ\x000fj\x0012Ü5ln|\x001fæÈ\x0018ÙïU*4­tmXlÓ¦5\x001eîeå\x0018\x0019#0ûÅ\x0008\x0002ßÜ1-¼fø^íïg6\x001a¤9;¾æRG¬`ÍáªÃBy2Þc´æ½\x0002Ó­'Y°î\x0010\x000eÀÂü÷rÕ12cv\x000bâc\x0007'ØÀSÚ¸Ögà^\x001eÛ\x000eÒ½Â\x0004ù¨¡`n°\x001f¨54Ùò\x0013ÕHCæ$iNÚoí´É6];î~×ÎÑ\x000bõnOÔùr@ÚhNäæ§¬¾åO©¥#·\x0002³×V\x0010S;FóåÀ\x0018þ:á~·£7÷Ý\x001eÝ1ï½F=\x0002&b7\x001f'[
÷b|§6»=T\x001fÂ\x001eÙ¡æ
9cX,¨ùzÐ\x0011säë®Ùíy7; ôqêCoµ\x0006è\x0014
\x0010îãu×È¡Ù+`\x0018\x0014ð\x0013b¶½Rµ®qù¿\x0017\x000fTÆ¤Ìn1©<×(\x00192à*J<×h'\x0008÷sw³r®ÙýæZàG·\x0018\x0001Kë×¡\x0013a>÷yÄ\x001a\x0019a³»EØRâö¤L{	±æ\x0015Í|/\x0001sÜQ>á^7¼MÓÒI65ë¹g¨oá6b\x000bH[`7[|k\x001a}K&r,OÔ½$\x001399ÓÜ^3-\x0000'®Fe\x0015ß
LÐ´I'gïcáx9Óün3
,¦C\x0014s0Ìá(Aº, /:a¯NpDï"$ÇA\x0002Ëï N©e\x000eÅ>'Ef\x0014ý|³[øâ.´$IÃÙ\x0004Ønä~¢\x0013Eg¾ÛÍ ~;\x0010\x0011Pw¯\x0011P\x0013üDè\x0016ìõà<R\x0017¼\x0010ñ\x0014"¯}P¸5ßèOÇßèO÷\x0010¤6önú>Î\x001f\E×Ç«èz·vò\x000eP®1\x001d"¯æ;µ
~¢·ÇèíC^FøÞ\x001e£½,úöÞ\x001c£ýöîÿ'ß(\x001dFi/²`émÑ¹C
\x0008Wíø\x0013Ý×\x0007¿ÑÍñ7ºyÈß\x0008£ëããh¯½î·>l-ß9¸t\x0016çÜ¡«ï»¯g¯ÞìäOØq;Ö§\x0004ÐëKm@á\x0001ôÏù¹£ïw¯Ï^=}±\x001c\x0004rØ¯\x0004´,Tj}øR`äüËY/m%òäY\x001aë\x0000Ôfä¼|)J\x000b&RÐY+\x0014ª£\"û á·O\x000c×´ÃÁ\x001aÔ|©ÈÐç\x001f4W"\x0007\x001cæ2U\x0005A`1¦<ù\x001d	|ÜmbzS\x001aiüÍ·;Ø \x0005ñu\x0015Ä§®+Ï®oßÿòñ¦·_I^\x0003tÚ\x0019~\x0017J>Òhk3_AýV.®~ÿâòT§\x0012},Ä­«\x0010÷Ff\x0008F´oÁÔrDµß­×2;Áì¶³NÔ\x0017¦´º¯N@J­¯õ|ö×Jd+Ù\x000e\x000cs\x0002\x0016_ÔN©ÉZz\x0001Íóz¯©aÅ0ÛaD\x00018±é1 \x0005nî
i>C`%²\x0013ÃìF9*4ÌªuTOöÀ<¯}°Y\x000c³\x001b\x0019fÃ¹/±4}"\x0016âümw%³\x0017ãìÇv:cÙqGä=Mç|Ø,õ]îdäÕÝy\x0004ºõÚ\x0004{Øê<\x000b?Á¼
÷Jf\x0010s£ãmf\x000eLÇ 5xLëEò¶±Ó\x0006¹oÀÀÆÇônð,ï,§\x0016Á	\x0015ÅÌrã#ZÎÆ\x0007mH¡\x0003R{ÈÝ\x000e©\x0004\x000fBV/¨á>	Ép¾à©hóJæ(\x0007:\x000c´c)_)u´u\x0018c\x0019z¾x%t\x0003F\x0006ºTnWh-çéøn#=>9LøY¶ Ëk<Ä«\x000f×oó\x000céìùõ
õþ\x0000ü¼j°qWk¢Á\x0002'j¾-Ì«g\x0017OûÿÍòýD­§Ôzºõt3Ê34'é\x0013Uë¡Í\x0014Ú@\x0007
W#³âøæÎÇ¤úñ?ËQãkÅ¨ÐóyrûéýßÎ\x001e¸þt½JpÊðT	(ÙKZ¶õ@óÓ[Hú<¹zùôg]¼ÀÿiÁ¨-ñ æ&[BT\x0014OÃ\x001føð±Î×û\x000cdÏdWS@ý,U}òý;ß|Í&Ü|ý\x001bÅÓ>¬!n\x001d²\x001fE¼ÅpB\x001e\x001e«³\x0011´×e>=¹º|ýG
¤=[æ×_\x000f\x001b\x0000-{ xwNòÕ!&æ7§[­æ¤\x0012fþÖ.i;¿&©)Ößf \x0016z¬7@|\x00003ü\x0001t>Y}Aä6yÊ3hç/`Å\x0017°Ã_ æã\x0007 z5Å­
×²Þ\x001fÄøáñÇ·rhãOy\x0000Êp5do*¿?
þ8Ì\x001fõa\x0001\x001bî)§|â\x000f\x0000'^`7\x0019ÄüIÃó'¨Ói¦Ô0Â±8kA»òOµÜ3¹¦\x0019S1¾\x0000gý\x0006µÐBxµ\x0001ò\x0008á3Àå3@ñ\x0012°¬C\x0001M)(O¡Óm	W[ ÷P\x0018ÞD±fÞÐ"\x0008	C\x0007ÅV\x0011ôBcÅÕ\x0016ÈM\x0014wQl\x0000n&Û(7\x00007-;yçc`r!/\x0016¸a\x000bP\\x0001¬õ+\x0016xnaîÃÇÄjÁÛëw×¿ÜÎZ\x0010¥\x0005qØ\x0002\x000f¬°\x001fòå&\x0001í1tßLË}H\x000fïC\x0005j]Râ(pæçÈî|i\x0016À°\x0005Ñb
QÉ3¶êfPj\x0006\x0013úkÛ\x000cÎ4ì±\x000fÑu *\x001e\x001dïC¼Ú\x0013%\x0013,8º\x000e\x0005ø\x000ciÚ' K\x0019Ø¶
Â	Õ¸M\x0016$iA\x001aµÀCà\x001bAt³Tµm\x000eõR³ëµ\x0016\x0018¹\x000cÌð2ð*ðYoöM\x0002B·YtJãj\x0005ZZ -Ðê|Áa.mÛy|ªdu\x0005G×Êá{%vL'Ù4´4µ3¦Y°¯Ga¤Ga=
TL¤:Û|KnëÀ\x0007ÝvÓ¿A\x0016a\x000b¼æÆ+¸\x0017QF³N¾­\x0003¿op\x0005DZ)yE×£\x001bjleg®\x0002k#æÇ¾k\x0019D9ÙðæÁØ`@æLä_Üíê÷äúM¿
ºÊ~))n»¼±RiY>Y\x0000ÑÏ\x0007}eñâñI\x0005ô\x000e\x0012ý}W±\x001bË\x001a®¥¹¢;ßÚ&Íg^m@(Ï!úîr«Ñ)+\x0008w"*·\x000cM°ÕÅù\x0002Å
ìI²ßiZ²=ïøÔ\x0018\x000f\x001bÓ\x0001\x001c<\x000b~y­[Ï>½\x0008Ù>4e\x0000ßû)IÕð% :¾Ëûî¨z\x0017ºèwú=­\x001bvï0\x0013.(ó&¤&ÛÑÙg«\x000f=Iô4NÂÁs*ÂË\x0017¦0\x001fÂZ\x000fnåt±ÓE\x0003öÁ+\x0015wÚÒ+^\x000c\x001cvÈþç3Ý\x0005±JÝ6ëÐó*­~ÞËýy ^ÅoaÉÍþ×³{+Ýßéyº½jlDPÀe	"©ùPÃ\x0006ð Áïtò[	H['
ì	ISÆ\x0008¶ÞñHòA¶\x0003#þ;½Q¾a\x0013òv~l\x0002îð&MÞ¥»ü\x0013ÈÉA¼r\x0007-È×²xÃÎ7\x0014rÒ&ïÔS%#lÆvÝÍ\x0016Çû¥1\x001e3\x0018kÁ5\x001fR¥Àe©d\x0002;±]tPO[Als²\x0016;ß8ÅÄ@+\x000eÜ\x001eÚôÈEôbO¢ûùß*äHÖbÀ)ÏØ»*n8;Í\x0013wðµÐIu\x001a\x0019ë\x00086=[)t\x000fRÏØ'DWbOeÖqbÃ\x0010wä\ÀC5Ê\x000f¨ý°Ä6\x0003Ø\x0018¡Xñmj;àxéétÓÉ­%·\x001eáÎ\x0007\x000eëc3ë:Üeç®Ø±CT¸\x0013ÛX\x0016¶/É\x0004*b1_ÁN\x0003ÄÑr\x00147_rµ\x0016Û{íý\x0000¶ÉSfµ¬] uÞ¯[uHMur\x0007'¸\x001bà¶/k¹ë¤6Üp"ô²\x0016;Jì8bk\x001a×$asèÑêÝ\x000e(\x000f8pÚ`í\x0001CZHÔS\x001bÝúÿè\x0013ñÆµÜr°ãÈ`;ËÐú±k\x0013¹éT¿ÂÕÐIB§!èëÁ]/AÚ$}àÞcÿêÈý
Ý?J.~÷õì÷×¹¹þ
ø|öÃ§¯·ooºsI
E\x0015MP$¬¢çÐ9Ñó¦æ\x0019÷úì÷\x0017Ï//^gC~8ûáåë«'§²JÉ\x0012=µDïd	$ø&À¹'c\x001c\x0007xÍ	\x0015¡!cÌÔ\x0018³ÛgáeòÄrüaØAwó\x0012C¶Ø©-v/[\x0014÷\x001cF[jr\x0017~\x0018×Y(ìÚh\x001aãöû0U>(\x001b\x0013Z'qÏf~Á\x000fÙâ§¶øý>ñdK<\x0007þ.±²PÎ±Ñ0µ%ì÷]\x0002Ý
½§	UZá1n¡àq£1qjLÜïÃ\x0004hÆXÞÊ¼¾gcÒÔ´ß¡RTã\x001d5¹Á/Ó\x000eù=#ÆL.x\ªý>MâÍÌ;Ï¦Í³¥ª¾ÖÈÃ¯Óß¨Ã1c0U¿MÛ\x0001Ìý\x0018#ÎØË\x0001Ð)Õ\x0018ÑúiÚ<Ó÷rþ8ÿa/\x0007 \x0019s\x0008\x0008\x0004>gb;gà^VM\x0012«&íµj\x0014°úÑÞQóµKNEî¬\x0011.@ÚÉ\x0007ÈWÀæi* ¦¤*$Û
°îcw¦|G%*Ç¬ÉÛ\x0018%NçÏh±&¶Â½yÅ½\x0011kÀÉ
m¯o·1Ê\x001fÕÑQãËl
ßÈ4Úu\x000fæhiÞË\x001cWz%Ô©æ1=¼Ã[Ú|Jû-FÚbö²Å°hÐØO­\x001eØÐ>MH³Q·\x0011s¬\7v¯uc\x00147^=kº~6'X^7÷qÜL3Þ£\x0012%ècÖä¥OJ\x0016xjÚ\x0005´¶Cß5^N5¿×TS\x0013\x001fu\x0004º>\x0007Å¹§ùw÷òmü6a§o/\x0019$$aZ2°òS3oÔ3dü8a·£9\x001f,ïÆÔ#\x001døëÌ¿\x0013¥9q7sÚù©1>Ï­©0¥ù²\x0011s¤§\x0006{¹j¸tBó\x0006T³Æ4oà^w\x0013MÚ
Þî·\x0017ø¶\x0017x¸»\x0019,)l=v,²j/äÉC·6qòÜ7*\x0017Ò"½Û7rá=1©êå°Ü\x000eóR¨èÝñ'z÷0?Q>ld²\x0005>"ÙâÕ§\x000c[/?ÿÛíû/½¶\x0014¡Zº ä¿TÜ9Ö±k\x0010æµÄÚ#Ç«/~$}ÍË\x001f^]=ýqÙ\x0014'Lq{\x0012ps£g*é±U+´ÅÕ;Þ}×[bÄG1;}\x0014\x001a+Å|Ïim×\x0003ïÓ~>D8bø(f§Òºuì\x000f\x0004ßfù\x0006ã;Dì×b)v'SbK¬Â\x00075Ê«jaÛõ81½ÜNÓ+bêr5Äb´£N¯Ô"'êÏ¶â)~·B%½Æ%
¦OWíè²Á\x00141½üNÓ+µ0×­\x0015åDç|\x0011¸E\x001f)a\x001fS@·Ø\x001ezÅÛ¶\x0013ë\¾Õ¦LÕý\x0002Ë&ìrªPÅ/J_YV f±MsJ¾eÀ\x0016'mÙé»X¾9gWÿÛ
± %ªéÝ) ?\x000bìôY\x000eÏ \x000fçâ\x0014FÕÑÖa½-Òo\x001c\x0017\x0014í´-äÌ]¡-¿\x0008b©Ò=Øâ¤-n'[\x0002\x000bjø.N±-®£MÚz[äÙ\x0002û\x001c.Øòü|e´~5\x0010øæbïápqò»¸¾\x000bj±\x0015[|tü¬\x0001Ùû*ë%\x001fý±£Íè\x001a[¢iMù\x0017¬ö¯g?|¹~·"ÇÐr¥0ÄRéY\x000cÕA"v\x0001þõÙ\x000f?^|w"\x000fõ\x0014Xo\x00056Ù/¡©\x0003x\x0017ÑÌ©XqüD8|%ñÄCÌÿÅ¸\x00169¸sÖ,åÞ\x0011\x001aÖ¬Y:ÿ\¼xz à¤íÈ¾½×«\x0018(õ\x0014\x001cgCª¸xMêE\x000c\x0003£\å
2Ö\x000bXbæø¨raºdvÛgFÂÌÊliOÏSDÕuÌBÓ²üÔöqÎ\x000bîÊ8N:ÔÆÙÄ¶\x000cmÄ8k³y1í*CÖ4:ÿC,\x000ckÝÒ\x001eÝËl%³ÝÎl\x0012·)PÀRÇZ[¾ßãN7Ê¬¢/¹\x0018\x0010¿\x0004Ó>\x00167Ï]½}Ó¯³ê´å2G#Á¦\x0018`Qn»µ¸üáìÙÅë«§'ÅV+ý¤R*Ók5J_*Ò
=\x001e¤\x0004\x0005\x0011}Çå\x0016«ðÅàëÑÁ7\x0015\x000fl
\x0007-±V4àç³,6á\x001boFñ-·s\x0000,\x001c\x0000fÚ\x0008{ÓOD?*ÿõ\x00031À»£ÔcÌ¥;÷~={|ýùìw7ï9	ã	eæ`£¢zWÖ\x0010Ê¤ù\x001eÙ\ùúìñÅ\x000fg¿»ü×EîI1Uæ6j\x0004\x001csXëænMÀ\x000cÐ:å¹JÆ/jMôc[mÇ°ý¡ºÏ~Ü'y£Ñów\x001bÀ\x0000w#à ZñóMu´½«[c\x0016+ûÁ£\x0000#à6\x0004ö\x0010\x001dLÔF9YÃF·XwÜ
\x000erªÀÐ\ATâX;S\x001fËó\x001dãK\x000ev\x001còi>\x0006!rÔ\x000cªàù4¥zØ¢µN*6Ë¥ÞýàIÌ\x0015!\x0004³\x001e\x001cÇ¹º_ÙMÄFF¼Õhº\x0013×ÕäZnzh?´Ö±¨®Go,X}'Ìß7×;IîÈµaÏÑS!RJ%`ô²2F?vØi\x0008\x001b<Ýï}¾+W\x0015oZYìw¸
ÜNrLq\x00135\x0015jbÃNÊùL¶uR=ñÂ³\x0001<Hð0\x0002\x001a³4Ã\x0013Õß\x0004NLñvY\x0000c\x0005vØi\x0000[co?j\x001c-L\x0015Uârâ¡s5ùT×\x0011=,=6Ã5¿ 'NGScÏ~ÏmÜh-ÉõÐÉé®\x0014xn\x0017¬<Ç7½/	Ü@n%ù?®»²ÁT/Ó~½ßq\x001bí$øÐ¶JIo\x0001×3ûgy\x0017B|r\x0003¹ä~d²äë\x0003ez\x000bMÍ\x001dÛ\x0006Ur,õÚ<Hò\x001dÑZÍÙ(\x0016È\x000cs(PYMnåÖb¶\x0016\x0013\x0002\x000boÇ|cæÙb"-ÐàæKC×oçÊM\x00042qCÏ7ô7\x000fdØ\x0011þú\x0018þú¡À\x000byUò\x0014GàË¥/¡B\x0005«^D§"Xëùiz\x0013Ùù"!2\x0015|îÈ¯.,
þÈ´ÿm\x0006_Cy;<ja[a½¬ºùøåÓ×¿u?ÖjÇuèyçá´	Ü¹,X³»Í¤_ñO/~|ùúèZ ë1tkX|'fÿ7Ö«´I,L\x001aPæ`?t#ÐÍ\x0018:¾Ç&j^\x0013Áª¦+?´´ü\x0010ê*m¨ÝØ [Ò\x000bÌäê{ò ³äÛ)1ó
è^\x000cº\x001f\x001côDÉáÑEv|óå§KÇ+L?x\x0010c\x001eÆÆ\x001c÷h¢HIà{G\x0015cèýèQy\x001c\x001bsì"EÊñXÔB\x0013]óÛWÔó2¶[ÐÅ¨ÇÁ\x001e(P\x0017¦ö\x001bVq.^Ôóå¬\x001bÀ\x0018ó4<æÔÿ'æ4\x0012ºæ\x001eR'êT¶!OC\x001eÏ
éïªÖëÁ¶®¼Í/?5v£O8ë9:8êø\x001aMó¥Ý«m+|z¾Rc\x000b»ì\x001bâLºéOò4fþÝeÓÎxp½ho|34g\x0012¥³\x001d\x001cÜµåÕ¢Úq¶ç9rpÚyÒ\\x000f|<<\x0017ýA8Æ\x0013Å¿ÛþúhèàË¡Ï^ÌôÊA\x000cþfÐ	Í1ö3³£/sçÍñÜ\x0019ù¿õÜyw4wÞ=¹\x0013&\x0015\x0004ÿöÁÀ§£='
n9(ÐCÞA<oÎgç ìâ)ådR.&ÉO¥¦+áóëÛ/ï?vG£Æ²Áª\x0012«¸\x0007;D7±Coº&\x0015?¿¸úñée~=å×Ãüí	\x0015[
S.LdQaæçÍF|3Å7Ãøµqø¹±d+é\x001dÈëðí\x0014ß\x000eã\x001bî£\x000f	\x0016¹é©}XÇï¦ün¿6óäá§ª-`Ûø/×Ò­âHáêU;|\x0000£Ã\x000f Ú\x0007Hí\x0003,\x0017l¬3@,_\x0018^¿!°¯JÜÚ\x0004\x0002w\x00176ñDSÏMüZ|\x0000=ü\x0001Bä\x0000w>¬Î\x0013°\x0001Mf{þío\x0001F\x0018`
À\x0006D±}\x0001[o*à\x0008þÎÛ¿\x0011\x000bØ\x000c¯`\x000e*ç\x000e\x0013
þAô/.fä¯4Àñ·Ããï\x0012»\x0016XM\x000e
àáïP_Åï\x0004¿\x001bçW¤êo³Þ\x0001¬k\x001bÐraÒ*ü ðÃ0¾I\x0013,qe\x0015´*±|sÙù\x0004Â8l\x00008.;À\x000f¨+/gM4o¸?	þ4Êéû¤ne5`¬ª>R±\x000bdw>À¦Z}å\x0004\x001e7 ÉAbn\x0019õÿ+måÉy	¨m\x0016È#\x000cÏ0ÌYåwBÍÕ6 \x001cß\x0001,>çíj<Ã`ø\x0010³Þò&¤\x0013gÄ«ÖZÄªw!§\x0018\x000c\x001fc¸_òø+KøÐ_xyÁð\x0011fó\x0011@[Ö\x0000UÅå\x001dùOtßÄ/\x0000\x0018>\x0003,8îªmCQÇ\x001e\x0012Z²9ì¼ÜCa|\x0013ÅÐ>­à| yJ³ôÐ:Kì¼ê#7zx\x000fB)\x0013:M¤0J\x0015óÙ¼ï'Ðr\x000bÒÃ[\x0010
hm\x0016\x0000eè9X°ï\x001e¤å2ÖÃËØàÌqm\x0019\x001a[m\x0012èú¶Í\x0002'vQíFwQct¦èH
VT\x000cÞm;\x00142V\x0019\x0010¥\x0001qÔ\x0000\x001cßuÛb{ðÊçØ¾\x0006\x0018\x00190Ãñ\x0008í`Õ|)|4m_`ßul®ÃÃëXGßîÃµÓGù\x0006`Û\x001cêPYg\x0001H\x000bFCº(\x000e\x0013ãÁ!¥\x0016\x00056µY4\x001fÞfÜÌðN¤uË\x001a´V59â¦Úcõ|_m\x0016x\x0019ðÃ\x000b\x0019åºùVï\x000f½qjÕü\x0003ð6\x000b´ \x000c[/cí^éÛJn]\x0006³\x0005û\x0006VÜQ`b82¡ ¶î\x0016)òJ¶¡	&Å} wÓ0º3Ãò=Od\x0003ÉÞ\x0005Ò­\x000b£n]ùjÀ½_"p»\x0014í¹Æx\x000fÞf\\x0007at\x001d|·<Èí9v­µ×Mbsçu\x0010äå ^\x000eò\x0008\x001fz³zÅM ØO4ßÚd@´â\x0013D;ú	ðU\x001cScÛf
\x000eLàÎ(JÇ4:¦\x0001_·YèÐ\x001aJfÆ8\x0003ëö2bk\x0015aA\x0018¶À4ùÌ|$§êZ\x0001óZ³ï\x001cå\x001cGä-I 1_tª\x001c\x0002Ý¤L{´&W\x0019 ×q\x001c_ÇFñ%ßX ]FìÖqÜ9Ðbekq
\x0016á¯\x001eF¼H«£~Ñù\x0017åÉIô\x0015ÿéúíý¯þÆº\x0010-Ëø¼*¨PÑ'm¸2a^ÏìÉ´µøO\x0017ùÇSÝ%ÿà\x0018!ÿ´úy\x001bhâJ>\x0003Sw\x000c\x001fu«¬}ÝÝ{ù½à÷Ãü¾ÊW~\x0017Âï-×\x0014«´Xn¹?\x0008þ0Ì\x0005óTYì=W£yÕÊEZ¬_Ç¯\x0005¿\x001eäWùhþä¥P&c=1oçõ7áG±|ãðò5\x0006=éo<eD+¯cþó/®[ø'\x001dÈ\x000fftþ¨ìÏ5\x0003\x0012\x0015é(¬ñb\x0003ÕhÖ\x0019à¤\x0001Ã_@\x001d$\x0018ÀÖªcå\x0012¿ºhöý\x0000VòÛQþ|\x000b&OÂëÄ7cçøfìÒ¼Tý&~¹Âð\x0006gH+ÊÌ>E}oR_7\x0003\x0016eGV\x0019¤\x0001iØ\x0000m¹\x0004\x0006
 øm'°¿\x0016oã\x0013(
O í¹ÌÎ%Í\x0002*¿q\\x0015;\x001dØbÀä©\x0000
Ðvø\x0003@¹	WÉ\x001dÇ\x001dù\x001aÆ\x0006¸¸ë\x0012Ðò\x0008Ö£gpHyç¯.sÛ6ÀZÎÌë\x001coâ?\x000eóaíTç
i\x001eaçIþ\x0000v>ñr\x0001Z\x001a0èD¤"çÝ \x0001ä\x0004å+\x000co¢'Þj¶\x0019`¥\x0001vØVAèP¡\x000c07çÌ¼àÿ&\x0003ä&¤Ç7!å9÷Õ\x0016°­Ã¼ù¢¶-\x0006\x0018%¯ajÐRK½t ©Ï
ª¬rÖGZ\x0016Ye\x0000H\x0003`Ü\x0000ÏÇSE,×ÛyÛMøZâëqü\x0016pÊq\x0003Lk9\x001eaã|±ø&\x0003¤#mF\x001déB\x000b¢V\x001f9r\x0016%/h\x0002¹}¿¼ÈÑ|H\x0016Î=M ì\x0012ñ)\x0010¹\x00148Ïª]oòFz¢fÔ\x0013ÍÇpäì]-¢i\x0013Ð\x000cÐ»\x001ecÆ[iÀð)\x0000á`æ\x0003ãøµØ©}ï2F:Bf\x0007GÈ±/ó&´0_ò¶Í\x0000¹\x000bá]È\x000b@Ý"IÊ*«ZÆÁ
M\x0006HWÎ»ry\x0011³²Í\x0013Ê'4Kîº­<íø1\x001cÚ)R­ô:c5XZ»ï1le8Â#ò\x0007Ð¼bÞS-3Ï\x001f5¬Þ÷6fe<ÂÆ#²\x0001¶\x0015\x0001M6¡xÈ_\Öü[a\x0000X÷yüyÐèÏ\	­'ÔêåÏÝ\x0018S\x0014Ï5®8\x0015[Ú\x001cY·\x0014­\x0019p<<\x000cì»Á¨c+0º8lJ\x0017÷f)\x0017m\x000bP/vöÙ¡ ö\x00068¼å\x0003èH}éÉ§¯oÿ|ý±»Wv¯Æ(9f©©là¦rÎÏ?ÏLÊq¼|ýä÷\x0017/N4É!x'àÝ ¼=\£Áº
ß\x001c"7ï\x0010mw\x0002Þ
Â¶]jí=?±:Ó%ðÒ
ïÅÈûÁÏ+À]Ðü>¿\x0002p@bÞÛ\x0002\x001fÄÈÁ×­¹¥Ëî\x0004=¡?Áwùy½-ðIÀ§AøI$Åz\x000eD\x0004hÑP¯\x0001]\x0005ÿ?\x0002JüOH\x0019ìç7·\x001f®ñ\x001fë=¹<6E¦Gy\x0007Ü\x001f\x0019¯ô(ï:¤__^=»xñäå§lb·Ý²\x0003k\x0003ac#R9ÆìJÎ\x000cò\x001dªÒýðNÀ»Aø¼ÃÊ\x001eÞ
¹æ\x0006*&,G\x000f×{AîÇÉ5çcqÃ@o	Y¦C\x0013s\x0005¼\x0013ðn\x000c\x001e*©Û¡M({lÏ]Êw\x0000ÎÅróy@\x001bàM5
\x000e½:¼|ÕÖ\x0018Þ\x001dD%{äÈ»é=Èy\x0003cô6´,²\x0008
ó>\x0002?<8Ü\x00024é\x0007g½ÅÍÄ¼<õúÍðÓ\x0006â¼jÝ\x0016ø(áã |>Të¤OVÕH§Ës3ã"ÿ
ðQnqp§Ä"\x0000[ö¨|ÀÔBÏG\x0014`d{Gú$Ï¨4xHZÊ\x0010ASÑgt×Ód\x0019ýZÕka[¯\x0017(³ËõÙÍÙ«/ï¿½xÿ¶û\x0002eð\x0016N­GjuH­M O°zvyöêòÇ§?½xúdþâÔxµàÕ\x001by­ñTv¤1¡J×\x0012¿bm\x001f^-ÆWo\x001eßÌK-wóPrÄ&\x0006cy|ílÈi\x001d°\x0011Àf3°5\x001c&Ö	Î©¦(ê6\x001fâ¬£µ×	^·y#¿ïëØ«\x001cÒÓi^xq\x001d¯\x0015ãk·¯å;?òrá\ä0¼Nó±+Å\x0000ÛÍ\x0003±ÈyÕ3pbtìEÁ|
Ñ:^'\x0006Øm\x001fàÀqì%ñSY>÷XfBÍ?\x0013¬\x0003ö\x0002Øo\x0006v{r\x0018cù:\x001fSÓÑóë£\x0011qóp\x0001Å_êE2P+NT»Ùùª½UÀ §0lÃ\x0016\x0002wIÆ²ÀeóÍüõq\x001dqÄa3±)BòXØK>è\x001að>\x000eäÍs\x0002ûQ
\x001eÖ,°?\x0000ß\x0014õ|Mù:â$Ófbg[GñÞÙÏ7¼êö\x0001ÖJ\x0000ã[õÇÊFÌ\x001dØxFÀüÓÏ:Þ#Ïg³ë"Et\x0007D×»$Ø\ùÄrõö\x0011Öm'Î·VMXµmb>Sm\x001d°ô}ôfç\x0007½aZu:\x0019´Bwøà­í³O\x001cô\x000f*±\x001b!¦ëFÔü\x0004\x0012ÇÝuû¸kÚK`¿\x0019¸®µB\x001c\x0014§n%Lü®Ä>ì4)\wa³?\x0011\x001d¿\x0019Å=U2'1î\x0000åË\ñ'\x000e
ãr\x0008­?»þåæöãõnfç\x0015\x0017j`È¤µ pÕaTº´Ï.¾¿¼zqñc\x0007¶b»\x0011lloLm\x0002Ð\x0002ôã®dù6ºø\x001eÐÏ=Vèz\x0003\x0019\x001aoº5ÅÖãÝ\x001a\x001cÌw_\x000fî\x0004¸\x001b\x0005§:óý±H\x0003ÒØ3s?î ¸Ã\x0010wòÜ×+aqdåÖÀq\x0016GÝ\x0011\\x000bp=\x0000îfÕâ7«:S´æ÷º\x0018Ì3%\x001d%l)´¢S\x0000n´«5Çâ[özê(æI\x001cß\x000bN1~,´òÂô;ÎÀ \x001e\x0018ëÉó5²Û\x0012öf¢-Üsä(.w5ê\x0007\x0007	\x000eCàXeg\x001a8o)-=>/¾H÷\x001bInÈ³ÍsÅ\x0013·æâ´\x0018ô#.\x000f\x001f\x0018;}´â\x0010MÂt\x0000nQ¯Úf8/ßµÜKr¿ÓCkS\x0007Àþv<\x0011ùX\x000f.\x001f\x0018;kC\x000e¾©·¶¯Øåvi=ä¡¸²åW½¯>}ürö$ñë?zé£fñv°U0÷-¨õ\x0013¨a4¯lrx\yõòÅgOÐE\x0003\x000e¼ÅèF
p%S\x000cðµ­W¡\x001a\x0000q_\x0003&íÑ£vÇ[\x000c0|·	Ó\x001eé\x000bÔ<»ÌoçÃìøä7ÃüASÚÅ^Ì\x001f\x001fæµ7ñ[ÉoÇù9ÑÑb[/K]à¨\x0012\x0019
èy^\a\x0006øa\x0003\x0012 ×[\x000c\x0008ÅÛ
´AÁ¾+ H\x0003Â¸\x0001y\x0005Ô%\x001c=éóU/Ð\x0012îrXÃoàÇ\x001f\x0007ùÑ·¡-\x0008UM¨m
\x000fX._YµHøåc@6ý¦O<\x001f\x0013~£Lø-\x0019ËOþ|ýo7\x001f>tçc§84IÊÇ§¹É®£qSIY~òûWÏ-\x0010	aÜ<ð{i6	ßüyÙaVóé6\x0013&
ïêWp£6DíX\x0015÷Ó@jo¶]\x0010Í|¦ÉF\x001b´Izü;ÄöÒ\x0019" NEUKc-ñ`vÿ\x000eZK\x001bô\x001e6 {\x001cAC\x001b¸	/-ÝhßÁìò\x001dèÎ\x001e|Ø@9\x0008AÏTl´ÁI\x001bÜ\x000e6´<<ä5ó
màæ\x001eA-G`WÚ¤
i\x0007\x001bÚ¾\x0014ÀQ¡üßáB}\x001fö^\x000fZ\x000ezã!Z~ò	(mÐ,YÔ\x0011'\i6Ø\x001dlÐ­\x001fºW\ë\x000b÷Öù·ö\x0016xißÁ\x0002Àþ<U·Ks½8D\x000e	ùù^[ÛLp \x000e¸â\x0003\x001eÒ©µvá\ñ!íÚJGôµÃ¡U!\x001f\x000f×;¬i*¥Áû\x0012'qc+ýÍxslÆ\x001du´5qó<Ü\x0002¹N-Ì¿Þ¯5\x0003>zÃ\G®¾"ýç³?\ß¾{ÿñs\x001c=RÇH\x0003Ê¼ðá»\x000e©ù²«×HýÃÙ\x001fò/¾øa\x0011y\x00126ÊÈEx+³ãäy£\x00147º9x¨:h·\x0012ú UÐ{°\x0019Ú´T\\x000f$\x0002ÝD®\x0006Ô»\x000f4\x001côÀPçÛ0ßgtíT_\x0003p]êùV\x000c+©µ¤Ö\x0003ÔFsIN^Ü¯\x001bàG<\x001d^Km$µ\x0019 Ðr\x0011&YUPØ÷k¿±V!\x001e\x0015ýåSOj\x001f|{ýñyqóõ¯½;`\x0002ßºßéÀú\x0019ë ´ë\x0011\x0000ùþêâÅ÷g/._ÿtj#/&L\x0007e\x0013@Jm±A\x0007\x0011bá\X­ø)TÃ|Ï&\x0004iB\x00187!\x0005VôÔ:o÷\x0018RÒ0¯ö¿Í\x0006­
Z
Û½SÈGÖ\x0018\x000e*÷­\x000cÎb8\x001a\x0013]w¶AK\x001bô°
ùB¹qÚáí±|ÄµºGRl\x0005Z~\x0005=þ\x0015òno(½\x0016Âj°¾}\x001e5U\x00068±!üA\x00030N\x0006(V\x0003ÑÐJ\x0007ð0Ø×\x0004/¿\x001fÿ\x0006¡µ,&T\x000b\x0002\x0007O²\x0005;O##¿\x0019ÿ
Ök¾§\x0014Mr.h|\x0011#\x001b¼é\x0010§[a\x0003\x00176À7R\x0014Ë§À)wFû\x0011¯S
=:ÉkÐN\x000cÚ
N&ÌxØq¡\x0018o5EÉü1È\x0008×£l²Æ\x0008o¤\x0011Þ\x000c\x001bQ®ëõÎ³\x0012ÛLpèQª[e?²atUc¬ÍLQMn/\x0006ëDÈ\x0006ß#³òt\x0010òùtBHyoû°Z\x0014Áá/\x001eÝÝ{rûéýßÎ~zó¾ÿîw"Oë"`8éùvw·ºSEüÉÕË§<ûééåÓÓa\x00082Å	S¶\x0012ZQ9ö<\x000b¬GÏ\x0007íxEÞ`\x0015_å¤ïÆ¯\x0012(,aó\x001c³ôM8ñÖùê\x0001C0ä(âFC\x00147ÒË\x0015HëC­o11`H\x0012ÜQ¹ÞdHöÀ¹³-&»¤nÐÂ¼°ËvK\x0000Ä2;J§\x001b×k:/µ\x0005Bù*/«6Î)\x000cØ¢ÅW\x0001½ÏüÂøFjâ¹{hðRqªS¼u¥-ò»ÜpÝf6S\x0015Qê'àÁ°`V§â:Sä¡r·+ÂÆÏR«Æ\x0004ÔúYøTqp\x000f;ñ¤¿@1åß6S²·H!@ç8Úª¼cQ¿ü©îc\x0005iË\x001dyÎm¶xÇBC.*\x001a'¤gy*{\x000fçVÂ\x0014}Gèró\x000cÓô=J6å X\x001bÅ{6Ø"71½Ó&Vµ\x0013ª-e\x0014ò=õÚ:ûX¬2eÚj\x0013]0¿Ógíl1­Ï o\x0017^wâanÈ\x0014\x001e~u)ïè/îáUF}×«ìÓïµHòÀ5iFk\x001eåóøÕë·õî¿ÿã?/ùðþs±\x0008\x0018|"­ÕÀ«µæbôüëÕ³'õuîìòûgOOæ\x0011¹ë1r¥[ÛJË°JÏÕ~f¾GÐ\x0006r3%7Cä.éÖôÔ\x0018N¨îÁ|ÝÅ\x0006r;%·äß2N\
)¶ZìùZ
änJî\x0006É¡IÑiº6epÛÄ<æ\x0003\x001bÀý\x0014Ü\x000f+öb
°ô4fm·gèy|\x0003yÁ\x0005ª8ÌlZV\x0012>Vð4Wó\x001d¢7Ç)y\x001cÞZ\x0012+\x000es\x0006om(aþå\x000bøÏo%úÛ1ööÎe´j\x001b:ØVÊ?\x000b¶	þ3\x0006ïÛ®\x0000u\x001950ß\x0007w\x0013üµ¿~Pðï$ü»\x0000ïk¾ËagÏ\x0013ôNèâw×½ùÒ_â7Ã¶ÑDÃ)Í\x001e[¼Òhgpïw\x0017?]þxªÊð'a=ÿOÂzkñ} )ì§T=Èd:û|v¢k9òzxè±ø¿Â\x0003ö\x000e§\x000b0w}ÔÙ§±\x0017?¿Û£k-~¾À\x001bOope^½õ\x0014"è÷æ\x0017\x0011²áÎmdÌ\x0010îÑ×\x001d¡\x0016Ý1\x0003þÉ¥jõds°w'Û{2\x0001(\x0019ÔÆ<°;Amd\¡>â_Õ½KZ¸c\x0016\x001b=Ày×¹ñ;-BRðõD38ãë;ôüÖEz±ò\x0018ÌJ5\x0012ñCgËÞ^þ$_ßÅ¯å÷\x001cóØ/P±\x0010WÍ,Éüº³ÑR'ÿ¤Ã\x0006òßm°±ß8GÅ\x0014Þ¦ÐÔðB\x0015·×©;jÕË\x001fÅü±wö®ä×^Wø*Vù\x0013Ã£ì÷ðÑ\x0008øxçp%¼Ê\x0017[KüÅ*Ë#ïö]¹I\x0008Òì¿³}nX\x0000µçðÑ\x0002ð{/\x0000e\x0012±|èxòçë¿¼ùõ\x001f·ÿÞIÿ&.-âMºN\x0015¸G\x0001Ó\x0011\x001d|òûç/¯þç"ûÄ3Ç.Üjvg\x000f°´©biS|å¬ë¦nv/Øý(»æÚ!í\x0002ó\x0003FùìýÀ\x0000\x000f£àþÜÚ¦\x00140ÕrÆOT1n\x0001\x00173=Ít-LëÚ\x001b«òM\x001eÐ÷4ãêg\x000f=\x000c²G¾&j×
cÁe\x0013Û\x0013=	ô4¶Á8Ý2r¬c_\x001f,k¯äÙßqDu³'1×Óè\oÑK­-ÏußFýD½ë\x0016t1ÛÓà¾}´	ÝjnT\x0005­÷_F;®ÔiV¹\x0015±aÜÍy$xeZç\x0018ß\x0012¹ô|Td\x0003¼<`øTÒü\x000cªUë¯¶ÁwÜ§úáåÈÛÁiã}«®Ñ\x001b\x000eAkõ¤Í'Ó´¬\x0018áÝ\x000egª¦ûx¾ø£4/¹\x0005^Kx=>m\x0002ÝÂ\x0015«h\x001e6\x001b@Õ\x001dá­·cð\x001c\x0006I$mà2­ie*=½»É¥\x001b\x0006Ã~X«Ü\x00038ÙRµüü-v=ZÕäÕ¡:co\x001f7\x0006GÑ'Úçåõé\x001bßêqüß\x001cÿ\x00072þÈþîýÝ\x0003b¿>b¿~0ìwæ}ØaÚÿ¦\x0011¯MðÇÁ\x001bì9½¡Kì>&h#ÃÅ7lùøæöãûÏÝ/oÉd÷ZFGµ­XÔGO@ÎtfÞeú\x0017OO+;\x0015\x000b&\x0012sh¹Ö¹Ö\x0002l)M©ÞXJÖ:²TA6¬/±«×\x0002'-pã\x0016 \x00144À¤@M'´1¾	ÙÌ-l³`rÇB\x000bÒqürõ,R\x001aÎ>*îV\x0013»¯\x0015\x0016x%,ðwR7×Ï"ËwÜXu^\ÜyNÍ\x0017xoÃ\x000f\x0012ÿN\x0012íZ|lCÀè]´|_	½-î»
Ò;áûÕ3\x0008²ßOz×ÚÄ«\x0006`½ÿåöy«ø\x0016üáNüêùãáÜÐ
°ºhþWþú1»-_ \x000c\x0001§\x0014£²dÍ´q@7¯d;/z-r
Çá5ü[@Xîä3¬µ\x0000Ó§\x00125bÄ\x001e°U&ÀFÎ%I®ç\x000e¹î\x001b\x0008¾ÃÇ õGÇðlý\x0014t_µ±|¤%;}·uG=6ÄßñO7V°w7Ö¾Ü\x000e;à8½\x001aJzõO_o?£lçãë÷\x001f>ôú¥Ùý	\x0012^®\x0006Ø@Rª\ËÜ<Õ÷åë«\x001fP°óñÅÓgÏN9¥pX
%±z+3ØÖ÷8ªÄÐjÙßÙÀBI\x0002»øðá×þä¿»}ÿË§¯\x001fnz\x001b'«ë\Â'ÞP¬F\x0007Â'nþõüâÙ³ËÒüwWO¿ùúÙå©æê}RëÙ±Ôc\x001d,K\x0010ã\x001eßZ7Ux°ó\x001aY[ØÅ¸ëÁqÏ®\x0002õ¯Á\0$Éû\x000ckI¸y\x0001
ìF»\x0019\x001cw
\T\x0007N+fçJ4°ó¦·°q7ãnZw&ÌþÒ4gXñ\x0011æú7[1êvtÔ\x0013¿Ã¥&ÓHÎà»Î\x0017+ÆÜ\x000ey&T©Íªe§µcÙÙç\x0013ìn=°w\x000fè\x000eTÝ\x001dí5gjùö
ì^°ûQvG\x001e@¦ä\x0000IþgxÑó¯)\x001bÐ@\x000f£èË«@{¾hÇ×rùØÔ\x0006ö(Øãè\x0016\x0013±_Ca\x0007OBµ\x0004QmGö$ØÓ(»Ã9^Ø³G\x001f\x0012o<gÔ¼Ú×zö©J7º2j\x0014^{ðùBeè\²&Jóñ´
ðG~Ø¨#\x000fU
D)Lc¤í]³&´Jóy\\x001bà¥#\x0006Ãææ³yvãG¨^$÷Á\x00045_Ð½\x0005^ü¨+\x0006Ðæ\x000cÝ¼\x000fj¥*ù=É¥\x001f\x0006£²¤	\x0007ù\x0003(Ú$\x0015_ñàDað\x0016v9ê£\x0018{aÊPNQ&·G}>gz\x0003¹ôÃ`Ð\x00113\x0018é&×=ß@\x001cS<ìï;« ]1\x0018ôÅÌ¡\x0016°Ùy"xVÂ	¥
ðîè®:\x0008UJ¾m3\x0005øôr³Áâ5ðÙ3úYª\x000bë ;y|={~ýù¬ ýáæúco\x00002Ñ6µ\x0008jgí%X-bÞ\x0015n²Î¯Ï_üpVþ³?\^¼X6Ä	CÜ\x000e J²\x00012ÄS\x000f<\x0015¹\x0019¶³óá¾ívXaÝÃ\x000e\"±»«àwb)ù÷í81³Ü.3\x000b\x0005ÃI%ÂYlyZ\x000c\x0001\x0003lÈ=|\x0010'>Ûå`O\x0006Z!ÖP×¡lgá\x000eðË}VV\x001bâ!~\x001fC4ªåVÙ\x000eK×¯lf5\x0015ÕÑäcµ!AÌ¬°ËÌBIAú"&¡le1
ðÜÇÔ
â]¾Hh0¥'U
©6µÔrÇÑ\x0015(\x000fÇáZxt·OÃïnnÿ²âu"ò;Þé±ÑhvWó½¸³ÑÄï.¯_>z{ýîúóÛYø àÃ ¼7¬¨\x0012°\x001a6ÊÁ×\x0017{;LTøÓ#\x000fÓ~18òÿ¤aÌj|ê$ø\x001chºhj¾Nq==ÎIÆU9Ç½1ÖáG{N\x001d³\x0013y\x000eÞy9c);ô³ÎÓ\x0016þpÄ\x001fFùæ®»y¢´Û½g=<´w\x001eÿ7GãÜÔã\x001b\x001dãLÂç¸ÚCàìÕÍ÷_P·éëß¯û[Mäk\x0003µÇÐú¼Ö;i\x0002êø¾;Ç^û\x0008½ºüñé(Øôú_/N5\x0013(ðfr×ÌðøãÂ\x0016l¥ÚJò!áG\x001f\x001f\x0016¾Õ\x0002ßê\x0007oÅÜÇ\x001f\x001f\x0014~øñaá;%&\x000fþø ðåÆé\x001eØÆ$~z8øÖÉ\x0011Æ*d\x0017óè\x0011å^SË©"pk]î6ñº\x001b\\x000bp=\x0004\x0002ge\x0018Ï	TàBÓº³f1£¶\x001f|*zîèùjðT{z\x0014ðÄ¥sà\x0012'çÏ°ÌÜ
\x000eGSeh®$ç¨×zt¤Z\x0007\x0005\x0018³Ü¢§\x001fÜ\x0011\x000774ä)MÕ³êu\x0016bí\x0002µ\\x0007Ò
®ãf`Äó\x0000\x000e£ëÖ\x0004Bâ÷i=\x001f¤Z\x000f.G\xR\x0018ï¤r­XZ!xÔÜåQûå~ò <\x000c
yL¨EÞ¼.ÏXzWòåB¿\x0015äZë¡1\x000f\¢¨5÷rÄ1çÉ\x0002Ë9îýäQy\x001c\x0019s@½aj\x0017\x0014¸¹,äc+C;²z»É{¹\x001aç`¡©\x0016\x0004®Æ\x00189úªíh_ßK~t
\x001cC©ÙV[% )Îb(Mew#+Ô\x000c­PÀ\x0007ÐÈk=\x0013ú\x0001&_Lî'óÜÍs×ö\x0016TÛ6ÔkPµ,¯°Ü^­ÜJgËx[	\x001b\x001cPk;Ð¥z¾9wá\x0006½Ü\x0015 \x001fÜiníÐ4Ïà¬\x0008H\x0011\x0002OD²×GI\x001eÈÁî¤ªMz\x000b¸åÝ\Å\x001d÷Äéu4ÿÊut\x0000Üp¥ÀÈÑòÉ÷;¼t·ü»å$9|Â&\x000bän\x0005K2i).\x000bEõ[InÈ\x001dPks¼áÆÂÁ×7\x000flô¶¬
ÑM\x001eå\x0002C\x000b4{úçU\x00160`IRå¦È:8ÿV¶;\x00193åÆ\x001fGî\x0014±ë±/©'¿æJ¶f¿%É?
üyÏ£ÖåÞcÉ\x000eÍÒ\x0002«wèpô²bÌËÏ\x0003÷\x0013U;ÐåQç\x0005êñ2Aèû\x001cý\x0011Â,\x0011dbÎÍç³ç×··ùzsÛoBà\x001aZÔð¬tùãrý]ÏËÌ\x000fgÏ/®®^¾xñôòªÃ\x0004'Lpã&ÄÄêÎ\x0004\x0012M­u;QºÕ\x0006'>Ûá3ÄØlQÓ©F¸ÖâH/§Lt\x001b¡üÑ3YöA\x000eÏd\x001f®Ï^}úÜ/ÂëRë\x0000fl ý\x0012\x0012'Û\x001b3¾K¡Æg\x0017g¯^þpREÝ\x0014Ù
 \x001bö×1l¤cë\x0004\x0002KáÑnf\x0010Ì0\x0002­\x001b´sTÀ¡9\x000c`ì|\x0018`5t\x0012Ði\x0008CùªA\x001aÁùÔ¹»
ôär'o_k½\x0002¾\x0013a\x001cdQµâTEcçf¯\x0016³CÌ\x00163>p$4\x000f4Ï\x000e·ß6b¤ÍÈH;¾
\x0019¼}Rñ(´ÚQ
U¬f\x0016\x0003mÆ\x0006ÚðóD 4½<ÐMßÏß×B[\x0001m\x0007 c&å*]^-H\x001eæ\x000b¢×\x0012;15Üö©áP&¦Fâö;Zi\x000eÏKo®FÊÈ ÇÖ1(Ó·S+\x0015MØ\x0011ZÊ"Õ±Æßl\x001eî@\x0005\x0015&:jhðò2ë¬@·Ç~4#ÃÊóÛn\x0011'\x000cÅ¶uØt¨ÀèC7¯ù£ú`áùÕI\x0001'"ÖSb½8$Î\x00024Öð\x0001jGüX\x0015\x001aít\x0013)±ÙLì\x001d\x0016WbM¹îÙ\x0015zb;%¶Û\x000fò\x0018\x001b bÛ\x001e\x0004çs\x0015×\x0012»)±ÛLì\x000eí|ë¢ CóEí|eöZb?%ömäüîìÛWOCÓ·¼¹Î:üÝÀáXX#\x0014a
mÖßý÷üç\x001f®W¨(¬ª¥w@WjRJ¬ÁpÅ¶óÌFÄvëßýáâ´DH8Û\x0008Enc\x000fK\x000c4¹^\x000fT\x0014\x0004Á6ç\x0013~ê%fjÙÇìqðIþ;ùä\x000c í|)â!vjÝÉ\x0010KAÏüIB\x000bdjÚÕóá\x0001KÜÔ;©ê[,	vIN9ï©Ìâ£m\x000f ó²\x000b\x0003ø©%~\x001fK|bmeO`z>÷>´­õ©%a\x001fKòQA×%Mñtïø¥N;w\x001f«=NÍû¡[°\x000b31è5\x0006S¼øÌ'§
X¦¤,I|vç\x000fÂâG8¹øø°ÝZK&A`<\x0015ïÔvl4Å\x001d\x0012\x001e\x000c?îåë\x000bïÁ\x001dÅg\x001b,T\x001aT[+
6\x001bC\x0015\x0013Òt¿Æ\\x001f\x0019s\öñpQFÜ/ËI¿xx½£#ÒÁ££G'7½ùøñ¦;Zïð9¹&ªXß®ä¯[ÓSËõÃÙË._¼¸<\x0015§wÇ\x000f&îîÉjöÚv¼°»È³	 6|ÛõÒÐ¯\x0005¾\x001eÅ7\x001b£°'|Ã\x00123ÖÌ^H7Ñ\x001bAoFémë(ô\x001c¤5\x001c
·'òU7á[oGñ]n³u\x0000fúùôZ\x001fEôµ>ÊÍ~üéöÝM¿ByÍ¦²fq\x001beÏ<\x000fx\x0019zÌ:¿ö\x001dÞi\x001f¿Ì¿:-ÿPÑ£@CèIEz\x001dÇN\x0003øR\x0013â)#!FßWÞ\x0004z\x001a\x001bõd0·¹z1n2ê»K9Ñ\x0002?U\x0013ÝÆ_\x0005ÿøõ=ðÇ;üq\x001f§N¢\x001fM°ïÔ\x0001\x0015\x0016ªV.\x0003wÔÿðéýÇëwýí]cø\x0000¨¼Ñäùø^ø?¼|úââ»Sm\x0016+¿üv_y~\x0010\x0008¶õSr­Í´ïêò·ßKþ»
^×ñ«\x00189ü\x001b²¯@\x0014¥¹eUÒE©ï\x001dù?fpþäÝ¹®¾N\x0004öuÕö]ÒvåóÇ\x000cÎpÖù\x001fñÎ\5sLòÌ\x001f:%Ö;ù-\x0008~{G\x001b{%\x000cõ\x0000£\x0007t\x001d
ëä\x0016Oè\x0001nâ×ÿBüZ~Çù®Ù; Âø7áw$ê®ÂÓÇNh|\x001b~f®Ó_{MË\x0017;¡ìÉïåò½Ûàa%¿OÕvSöÞ¨\x0011 ¬P\x0014Ý|h\x0013¿þ~túûh¸ú%åÃ\x0017¨SNàbô®¯¿@/¿þ~tú{\x001fYX)å©¤©UQ+Ä±³CH/¿ÿ~tþ{ôx?¹ZHÝÝX<ÞöÆ}üQ\x001c\x001d\x0007üR\x0015ó·­\x001dB\v\x0019¸Ä!%¿ëøG'ùÝ0¿ªð1ðàG>®mÖ÷Ý|DlÚî¶È\x001eÚ\¼»\x0007í»ê»fè\x001dÌø­r6ãËÍí±\x0019ø«aF¾eü|¤\x0002e
Ô«\x000f$p@qZrhh²n>èùêYúÍ\x001be¢\x0008\x0017>Æìã|Ó¿ü[r®\x0012[ºJþ81a~÷¦\x0004=µÌÜ\x0002=ù8us\x0015sB?é¾®ýy>º¹\x001aZ\x000côqêæ*èVÉ¹ìµ\x0013T\x0006Î
óU²k¡\x0018éãÔÍUÐ_ºQ3ÀñHûT8;¡×2[1ÐÇY«]ËLcºuÙÍÌ;B·× Æ¾\x001eáæ ·Rç\x0016\x0013Ç¢½là~sÄýæ[æÎ[§=J<uöNIÆO_n®¿þ­\x0018ñßÿñ\x0019ó\x0006){ã8º)àó©q\x001cßD¾\x001d\x0016*õ\x0004¾_þxyñúÅ®3þ\x001b\x000cóÂ0¿¯a\x0010¸tÃåc)Õ\x001bçl\x00157/B1lV\x0010f}ÍÊ-R5
&PÜ*ºÖpß\x001b×\x0016Ã¢0,îjÂÆ¥¤ãYS\x000fj@\x0017C­é{2lªÛ
ãâ³AË0\x000b-3m;YXÍ÷Ó\x001c¶ÌHËÌ¾\x001dô\x0018ðÕD*ïFÍ²pßl@_íúÁ6ÐGäù\x0017"üÙõ_?½¿í>¦\x000c´´ªì\x0016P>«eß\Çù´ýÏúìâ§O¯õ\x0014YoG\x0006ßjÁ\x0014p\x0006\x0002v\x0016"æ4?î«ÍÙlgÎ\x0013Ä¸ÆìÉ\x001b0æ>AÜ¢ËôÀ_lE·en×\x0019â¸=6£gãÑ>vdtudd3Ä_ÿñË×þ\x001bsÐ\x0011TäÅ\x0013ûc\x001c¤{{»ü~ÿúä¹Ð¤a|¯(üâSP,¶\x000fÖ²ä\x0004Ìg¡nÂ×\x0012_áãÎâ*½"÷Ê¥\x0014YJ 9ÛÛ$º~Ú":Óßm\x0011½>Ø´'ÇéåýÀV÷\x0010\x0015\x001cÂø\x0016ÄÜ±0:wpÂXÒqà·ïüëµZçÏ0ßðcÛÔÿùíñä;fTURýëó\x001f@äÉ"±ÑwÇ\x0006¼{`ËWfPÔ%|·¡ì7½Ý4)>Ã±Ïà\x000cÝÃ}B-¹êáL¥çÓ×Y\x0010u>mÃ$(êGåç)v3~è7ù×¾\x0012U¤ód¢6RXú^1Ï>[\x0002ÇîñSðòófð|·6t¹v*.5ôo¢Î\x000eÄ(÷Z
j4\x0017\x001b<.ÅÍùÇGÏnÎÜÞTÇþ1ö\x001aêõu¬w\\x001f\x0015Æ\x00074ôueÁG=\x001b´yvyöäê²úñ±ÕÐ	GÍXl1M6{þë?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=>ìD\x0012(ØÎÈ\x0014sµ=e¼Ð>#yW\x0008	\x000f\x001e0Ï.ðèææìúêò|'¶£#\þp\x001f\x0010+ÕÝ\x0005\x0015'Biéóµ?PÜ\x0010PåÒ¤#ª\x000fÈs¹>D\x0013Æ4áX Ä\x0019ÒhwÒF)î#Ä:£1þ/_\øÍþNá#=ÜÓûççÍóýêãûÄC¡YÆ¿¹}z}~Þ¼¼lþt±ùcóg9t\x0018|£wZx|H×¹Ê?Ü6\x001ftÚìn¯î®Á\x001eÜýéâì§³ËÁXÀ\x0001ò\x001a&Øzõñb}\x0004,&áKÝAÎ(hc\x0016ß\x001d\x001b³[2m:­,E\x000b-Çÿë 5'ÔµX)CgXª)°aÁ¾Å×!å;i
áofË3!&iepQzÿMú£k.Ä\x000b§Ô|/¸pÝ¸¿ËÇ_ÿÏo¤Øñ&ÅOýÇÿû²¹öõ¯ú	\x000fLäsÓ\x0011è:q¸pØ³`BÆ(ÔØ£Ì9³ìió{¿¾=[ß]Ýý\x0019ök0\x0019t:ØÉîn\x0007lF^R;\x0002/GM:\x0008©\x001dîÒ\x000e\x0005;¹²Ëµ#¦\x0014Ô\x000e¥Ø\x0008Â^¡¹\x001djçJíj\x0007¾\x0015:¹X;PB/7"§\x001e¨KmH'ÃB\x001bÀè8¿\\x001bàÌ%¶cá©\x001d:oi,Â?¥\x001dXhÐ/Ù¬wÚ!¢	Jeé¡\x0019»ÍSW3pO	Ë-ñ¨jHjùln»ÉÍPb÷¦ÐÓôVT<\x0018õ¶\x0003Î@ÚáØ\x001fô&f]\x0000Q\x0015ÿHTA{ÿ\¦%Æ@F7b¤j6ºéú6·ÄYµäæñp{ùC\x0019péí+ÔÇ×Í\x0003é\x0012¸ÿüôxÔPx+¨ÀP8mr¬\x0003
2zj\x0016»\x001b\x001f¨>ÞXñõ\x000fW\x0007ÙÓCfú£Ý¥êsÀî`NIKëA;¹sÇkdO%)Ò\x001fìX\x0015]\x0012{Ô'y\x0005È@{µ1né^O\x0005*uùnÙFîM>aÂ\x001eü¥ìê§Gn\Üçêµ {Mt¢£\x0000ê`§Ã%å-*|à	¡K¢\x00074dé^tÓ4pz{BäÚÅD±£¥ÑÁ\x0004¼It¢\x001bØqÉÚ;\x001e\x0019=EÓdvev:Cì\x0011­K\ÀÄÀ\x00196]Ü%ó\x0018È\x0001rx\x0012göÝ\x000eP+;.ýèd?»µù\x0003Øá/­Íìüh­ã?ÁÆä[4´3ø\x0017½\x0006>Ð=$G4\x001bI°¾´7Yãî|ï¹\x00058ñ\x0017hÁ l,]\x0016Ns_\x0005ûf÷a¦®	\x001bkþÏßPyÀ
<Çà§_¾®~Ú<ÿ\x0006þÌQý\x001dÕài³ê°¨
ì`ÚyÚ«ÕOg×\x001fÀwÙÕÃÏ¿~Æ;u©09ÿyþøééññõ\x0018?Ëá¡0M\x0005*t¥]\x0007¶\x001c\x0017#ó\x001eüùåéÕååÝ\x000e¨ äßÿÈ¹\x0017°/âÿ}|øßY¯7??=|½9\x0006.\x0002IÝfB\x0016#D8\x0013rL»·ÁÈÙ}åãùM~f½>{{u~³¾Ý\x0019\x001f^þíùg\x001cZLÌæ\x001a\x0014_W§O¿ý|ÿòrÿøòuuö¸Zÿõùáoø·^WOéNýð¥#¸}!\x000fºÆ¸Ü|çèùS1¾aÇkÑÓ«\x000fo×··ëËÛÕúÏ×çÿU+îVWxã~ %ù°íä¢-Á§¼Ø´Öùî\x001b{\x000có³·­)_î¿/OÒ0óÒ\x001f7ÇÍ3×\x0006yzþåW<êDi0ùº/8zIð&§7\x0015Ôav\x0010nÎ.oÏÏ®¹TÈÕõ»÷ø·\x000f\x0013£\x0003t\x0011çr6	Y£ômF\x000eSÑ¼¥=F×¤?Ú
ü­¤Ñ\x000bÌ2]õçkJºY\x0002ßUÍ\x001a:d|KþËP/~Èõ"sÆÙúçÿñ«Ó/÷Ï?¦£¥vdú*LÌÛ¸É.k\x0008b~\x0003¡ô³õÛ·0¹/Ö×ÿz6p0­S=´t®\x0011oï\x001cLÈ¼~v*×ò0æ
¡7b Iâ&\x0007¦cïzZzxu½\x0004oÎñbÞhy1zxÉ!'Ø¿+çO_¸2?B2®\x0014¾×ÒìÅÒGxs¢>ö¯^b>PÀÉ\x0000¬d×\x0004ì1h&fà0{Òª\x0005Î±\x0010\x0003°ÑÍÀVb!J\x0004N5p³ib\x000baÍ\x0012\x0016BúÂBàg+0Î¼MK,Ú{ØÊaJ8µD\x000f+!ÆÀøÙ\x0008¬¤?É&
«xâ5ä\x0015àSZm?¯,y§pâ¡\x000eVm°U§°KÌ\x0008Ö\x0018U{\x0007\x001b\x0002_Ó³YP\x0013½\x0019Ä¼w_\x000bl\x000b«­ÀZó\x0013¤1¹Ì
\x0000owå0W\x000b\®9Õ¾æ\x001e¶
é$½';TàÍÀ»Üüj`S\x0002f`kNTÞ7$J\x0003õpä\x0017å¨æß:ê÷
\x000eÀ\x001dï\x001døS£q£ÜÁ´ö\NÁ\x0007k,å`,æ\x000f!
Ü/IC°àÆÚ¸EtIÜ\x0011¹5¿ôa%MÇ3zÖ¯ßD¾énºhi×~pß\x0002ÕÀè¹»Õ|XG½{<åv]Ø"GÚ%/9äº¥h¡íà%ÇÙ­ã±]ºÖ\x0010ÛåÆXp¨>öSz\x0000#²cæÝp\x000e\x001f9G\x0008ó]hçIãv76\x001c¨Oá}+5ç¿µ_ê1¿Ôý
I~\x000b\x001b\x0000gA\x000f\x001aKpä\x0006$\x0013»d\x0003bÑØß\x0000ôn±\x0001vx®Ã7\x0019j@Ò-Z°\x0001ª\x0018\x0001µÀ\x0008(ÞPñ;(n@ä\x0006øÙ»²æ\x0006è0n\x000eý
HV=5 hºU5`9\ÈÎ?"µ7 Bz)D&\x0013\x000e5t\x0011à\x0007<8Oìó]ê\x001b`laì\x0012
°d0ÕN}Ó½GÊú\x0006Øb\x0004ì\x0002#%\x0015±\x0001QÓ\x0018\x0005\x000cy
¸ùæ\x0006¸b\x001bp\x000bì\x00036Å£\x0006DÞ\x0007û'5Àûq\x0003¼ïn\x0000\x001eZ\x0003V\x0004~è}cåÂÞ[µê\x0006ä:æ£¬\x0011¦ò"°v¸1Öã6Òõî
°åNlû7\x0002Ì×Ì\x0000!Y´&¤­\x0018Î®b9ºM-pý-hþs\x000bd^Á!0\x001cÅdæ\x0003.[àËIäû'\x0014'´
¢É¡\x0001r\x0008Ãrr\x0017ZßX6 v7ÀÃ©ÅRT´\x001cw¬(\x0002\x001dÎóÁK­
ÀWË±7ddw\x0003`\x0003óÞè\x0005Ý| \x001a\x0000Ç\x0017È}WKõ
°ÅNÝ
°\x001c\x000fÜä\x000eáfÀ\x0001\x0012{Ï»õ-pÅf½-p)®#·@Ò¯ÇCä\x0010²è*À·ÿq\x000bBÿ$rý	\x0017DÎ.ÃÂÏcøv¼kµ¶@b;Ö¢{?ö1&U8\x000cÌ#ù´ð´\x0019h¿¬)ÕªlêoA\x0018Þ½<X¢|¢Ç:ê¼\x000e¼\t\x001dh]¬düìÝ\x000cÄ\x0010ë
½²y\x000c\x0002¯\x0003§\x0017=\x001bSñ«¡\x0005®C6b\x0008ÖÛÃ±e¯NÛù°âÖ\x0016\x0018S´\x0000?;[\x0000Çß¤9l§ÛC¢A9ÜlÑYdbyA\x0014»gQÄ'ö!æ,äe`\x0002_°h¹ìB¶å
\x0017~ö6ÀG\½9ZÑ  s"Q¼\x001d¨\x0018v«ErFwÍ6ÕðMST2\x0010-álýo\x00145
É¢
£¡ÀjãÃ@¦Lé
\x0006¢}~}<\x000e][ç£7¥,EÕ£}ÚgNSÒô\x0019F¤ýpwyÚË1µ\x001dØA\x0013­36pæÄRð$$½
9ï÷Ù:ì¢³}_o{Ú|\x0001;\x000e\x0013Årj¤ÛûÒRE\x001dÄ:®Î¶d*a*Ú:v6M\x0011g÷Þ#VQG?¦¾ÚaÑLm±bc¦æø
ð@÷-Ê\x001al)ô\x0018\x001b?;¸¥\x001aV$ü%]Û÷ÍsÄì½ù¯ãv%·ëêoêlØXÕ0E<Ï\x0011±\x0019ºÖ}Ðâ\x0018=&§\x0006:XÏs;Ù-Âí¹=D$Yoä¶ò\x000fRÂ\x000eRIî°caHZ`×dl\x0015¶ÝÍñ\x001dXÈx!n¥
³}Ü&Ûí_°±ðÄBØºènüìZlJ|Ä\x0008Ød\x0002­Þë`Uq²»M_wû§\x001f;%\x001có\x0001.âbÜ¶ìoÛ×ßnh¼ß&[¸Smµ¸uÉÝ·åäJî{{·çDdî½¤UÜ£hRä\x001e¶pËT\x0006\x0006¹µÁÄâ6&°7D³[[¥îÜ*#%x¼Á\x0018Ìâ t¿÷\x0016©r\x0014g\x001e+£3O\x001b~4ÔíÂ¤qs<z4\x000bàë\x0014
¢·&lôztybÒO\x001e?Ý¯>ÿ×¿ÿÇÕóqwGúü\x0014g,ßÃ+I\x001cÅ@ö\x001dÔRTúéÕåézõÃêêú\x0000»\x000bcv\x0017:ÙÑ1\x000ctU\x0014@îv)\x0007¡åØ£\x001c³GÙËÁCÌn)©È« \x0006ôåØÇÞ¸v7Þ\x0008×+4i´\x001c\x0002)\x0004u\x001d÷ýVÒXÐØI\x001fQ¡$\x001bI\x001bÌ Vâ#Oýç:ú02@\x001fFf²Þ\x0008ð[òÙÓáý\x0004PX+òiÈã=×rôÖ\x0016ôÖvÒËìä&z3-ie{,\x001aµ½	®ì{×Û÷\x0018]ÄÔÃ#rY\x0016 ·óÉv-ôRJUÌ{üîÃWà\x0012È4ñ\x0007\x0007'\x0007,ÂKñ¡0äÞ[ö*üñq\x0003ñÇçFü\x0008Î{¢wjø°Ee£ãOTk£×®¤×½sG£J\x0004áÃ¾EV\x0007\x000eÙðí^²\x0012ß\x0012ßtîµ\x001fè}Ã9¡³>.àÇ\í\x0003ð³ør|\x0004Iô£3H#½ÔôÔí,ê\x0001&ø\x0000¾7Ã\x0005'¾Ð»~zOÏ\x0002\x000ec%"Ñ\x000f=/3:Ê©	|¯ÑÑ2bxJw÷\x0008\x001esd|µÅ\x0007ÜÑq½FG+'$|E±þâ@/\x0016óÓv²j{=d©È9¹\x0005èõ@¯\x001cÛL½÷ü]\x001f'øZÂ\x001f:?à
HÆ÷CïïÍ~ªÄ÷uë»×-øøY-õ>u¾zèü½OÂôrBßyB®\x0015\x0014å\x0016.w¾¶¼aíOªÅL}ß=õ<á/Ø[\x0008Ú±É×{oÌ*éÃÄjn«9¤\x0006;<£\x0004OøÃºÝÿ]I?1¡Ûh\x001aÅg\x0014¤7´ciR\x001eAüÅÎ(r|ñû§§&À÷¤J~oh%}LØ=uLH%m\x0013=Ë\x0006y\x0016\x0004Aá\x0005M~ô}ìî{ëéæ5M\x001dAëÖ::ûPªèµ(éñ»Þé\x0013÷>æRá(À®ÙUSf¹£U¹_iÕ½_yM¢Ê¯0Y)ás@¨7r^U¹\x0011_Nð»7,/­|\x001d\x0018B\x0018ð;`éÉéVwn5Ö$\x0003½dzÁëV.:wü\x0004¿ó\x001e\x0019%y»ÅbÅ´lã`3åþ0Ð:z=ùº{æ\x0007«5ãë\x0001?Pr¡7bRI%þdîèî¹\x0013Yå\x000eðå	MèØÑ\ð¨'§[Ý}º5\x0018ÞA\x0016ßZ¾YJ±¯#\x0016<bi_Þëàw'¾©v]Â\x001f|h(»Ýë¸7\x000b¸\x0012?Lfè5°eQV*àG\x001bV±ÑÜ¯ñS=y·7@ãÃ¶V À>~;¼3Çá¤%¹cÈE2Fyµ©Zä8êóÝ?þóñ\x001fÿù|ÿ\x0005\x001bòîþõH)_á\x0002\x0015_\x0008©\x0010,ÝS6\x000fìÀó*ÛpÉwgg×k¬¶ºz·¾Û-âËm\x0008~Üàh²ô\x001a\x0017¤'\x001aa\x0002Ë\x0003¥Ë\x0005\x001bªìãÐzVHêÈ\x0016\x0001]WÙ­fÞM[ß
£V\x0018µD+`=PV\x0006üSÛ@b\x0016aÙ«+ÕÐ\x0006[.	»È\x0010ÓP0-;£V\x0006Ëº,ó\x0002ÍÐªNZ-0t´þ\x0015ö#Ñt\x000bq¯òIK\x001blÙ\x0006»D\x001bLägWÿ\x0018\x0000g\x0004nÅ²ëzì¦F,`°\x0014\x0005ki¹ãF¡\x0011{Ãº[Z\x0011ËV,°&R\x0003¥}âg\x0011~\x000eqÿ}n}+t9¡ô2\x0013Ê·\x001d4\x0006,ñªPe?÷¿C6´¢Qz\x0019eY\x0015[KÖb+$7bÿX}#liì"öI\x000fÉo\x001aõÅHHÓ\x000e²¥óU:\x001aáÊF¸EFBcHdÖ^Ü\x0008G\x0011\x0011Q\x001cT©nD¹´Øî`$ü0tRèÉCAÇ (\x000e¦_Õ¶Â\x0017ö\x000b8\x001e:b^znMRý9lÁMõ/\x0016mDiü"öI¹\2\x000eZ\x0001Û\x0006\x0008Á"Ô¹\x00154>j\x001b\x0011ËE\x0011\x0017Y\x0014+¤\x0005íü°ái^\x0014öP^ne#ÌHò\x0010\x001aaF\x001dÎh?ø±XÇZá\x000e%ÙW·"­XdiKÇ¡Ü
7$&*zDVì\x000f\x001bªo.&ÑL(ðÇé
g=0R²
vá\x0019UîÚf];DÏÒ\x001fàSí\x0013#H³-Â_,{ª@	ßq#¬\¢\x0011!bq\x001a
i\x0006\x001d¨\x0018x(¢;éZÝrB-²màX*ÔÈÀoX pÄ¡|ÝÚVør,ü2cá\x0007A%\x00111ÄZÁÎl\ØÐ;S\¢å;¨2g·õÈ­\x0003æÄäk(É9¶\x0015
ý!5ú=cÚ\x0014Ü7hÆ\x0000M>døÀ×ÊÆ\x000ckÄ-½\x0001jÿMcÀd-ÒÿþI\x0016¾iLX¦-\x0006FEì°r'å`YgùrJ,|Å¶õJs[Fr¥=\x000bFó$°ÉS|UÊ~#Iôåî<uV#\x001b½_À­°Ãïï__þôñþïÇ¤è\x001b,¸¥g\x001c÷w éâ\x001fo¬ö£¿_ßÝ®>®ÿuwn~BãBýF:ÕÌlÁ\x001dÌÒÇ.ù´¹Ø`Õ+¯\x000e^1\x001fÉ¬Æ\x0019\x0013ú\x0012º\x0019Îu\x0014F¥µ"Åñ (#ËËh\x000ex°Ç"Ã\x0001t¡]ì0;<!Kª\x000f\x0017°d<!û½É\x0015È¡D\x000e=ÈCÈ\x000eª7kOÌ\x001c,÷?\x0000\x001dlt1ñ³\x0007B¼¤\x00032]Hºº%K ÛÑE$ Ûò"²ÒfxQÀ\x0002\x001bdº#\x0007ç¸h\x000e	n\x001dË<RkCæR­­Ùa¥ðäÓX¼=Í*g(þ\x000fÂ.\x001czZ;\x0012\x0019u|GÈøÙ<3à`£vmðÒL`³¤7(,\x0001·L7{Qî&¢};Áx§\åÖ\x0006ð"s/Ã®\x0018\x0008yå
dYÌf/Ûg³WX\x0015§TMâÜAÅ©cG"À\x0008\ª\x0000Wö±¦È>\x0019§¹a.¡©ìw\x0014\x0004¬få1fÆÏfæ )<Â&m2GÌûYûe,sÐÅ\x001dtÇ
Çë¬\x000e:!ä@¥KJ\x0015\x000b cÈ\x0011rª\x0019Ù<\x000516\x0014û\x00160y7!Û¥\x000csT%²êAöô¾k1¾\ôHí¬ZÈdD]¨{LafÌòÜÍ:
g\x0018»\x0010³)ûÙtô³â'hðYo\x0018ú®Y õ2V#ÚÂjDÛn5Ö<­\x0017ô\x0018\x0015p,1evm)F¢¤x8\x0011¥*i\x001d4mæ:VXªPÀç)w0çHb\x0019Ù¾[}¾D\x0004ßá\x0019\x0005q\x0015p'`-Ý"óBkx"][G,\x0003ïÙFr/@[r´³l'\x0000\x0019'Ð\x001dÝ,\x000c½'YÍU«\x0012\x0014æð)`\x0019f«KfÛ¾\x0007:0É¹\x0006Õàkxr#ï(XÌw\x0019h?\x001d¾Ãl`\x00102u4g:RI¡\x0006èCÏEÇÏ2fHyAVÙá\ß\x0004Ø=©³AÓ#\x0011°\x001fz^9þÔ=eÇw\x0007ºÕ\x001c½\x0008o}¢$\x001d¾9ÝG\x001e|º>Þù¢ûoî¾«ÝSêõ ,Fþe_ÏÒ4÷úPåèÂ»oÐ]\x000f9Lv\x0014I÷w¨H»,!ª^Æ±}|J[{ÏTÇËÜéÖñóUJ®9\x0013÷ª\x0014\x001dn°ÓÇ×xæÍÖ\x001aþøôuóû¯«·÷\x000f_6GY\x0016ù\x001cäüÀSjä\x0004§ö"ÿxusöñýêíúüâlW¥åÙM\x000fs \x0012^=\x00151Sö,0ïU
©bcæØÁ\x001c,=øc\x0004\x0015÷³\x0013¬¨önï5Ècu
óf¤­ÑÀ,¨|\x0019ôóHÓËÎÂAg1èb>Ë	\x001d\x001cyØirPºÃj'ÔÓ{·Ê*èbrÈÎÙ\x0011ÝÐÓ\x0014\x0003Ð8åÞwï\x001ah]@ë\x001eè\x0008g@U§ÿ\x0005ISîÕ-©6¢0\x001d¢Çvh¬,×a¤W\x000bÓ\x001c\x0006ïögVA»\x0002Úõ@Ã©Ë\x0012´&\x000fË¤0¥ÃRëÐ\x0016ëÐö¬Ã\x0018ÉÏöX\x0018§ô Àf¡«\x0017\x001eÉ­¢oÆw[ªe\x000eþ\x00069T!è½a~5ÐãÓ\x0019Kd×CK;¬Ct@\x0008ZG^nïy·
º\x001e¾czH8
H2Ó(	 	÷Þ× ¢CO?\x000by\x0012\x0007b*å\x0000¾\x001d2w¡°Ñ¡ÃFK0\x0017$h\x0017´D!õ\x000cmY§tÿÁñ8h«\x0010Zm\x0003ÀUWÛ×÷¯_Plóõåùas\x0016Ü Ñá\x0003ÌnÇ)W\x0003öþrz\x001f×w\x0017(´vs{}~¶;í-\x0002ÜtK^v\x00084\x001a\x0012cìþ"nuà£Wf\x0000\x001f=27k9kÇ9nÜáao\x0001Æ*n9ÊG\x0002n9ÊGj\x0001]t>S\x0019Lºa\x0019&\x0014ÈÞ·,ëÈuÑãR÷u¹0¬i\x000bób8zaqMîó}v»Üä¦\±à~*\x000fCËS\x00086~ïN\x001dù¨¾8ê7;zöA\x0019>\x001dXÁyFÖí­#\x001f©4"ùH¥±\\x000e®\x000c\QËDÏ[æÞ\x0007JðXÇÞiîÈ²ÈÁy\x0015¬ek÷¦lÖqrª©¢c\x000c|ÄJZdÊM¤Â\x0001Eõ:ðV\x000e¤rZÀ½À;\x0011Ö§B¢ÆzãûëßU+Uãg\x000f¹µ¤Åòìb%9±L¾¿t%¹.É{v! ì° 9ÕÀ6ZÅ|©iîÆéá¾:Î\x000foÚù=]rÃ<\x0017\x001cOl­âé¢öª¹ÕvzqåJ\x001d?ºrmé{gø¤éa\x0018ÌPßú\x001elä\x0012}¯SÙ\x001a5:ÔÇ7¨õöéõËæûçÏ«üçÓãêæþõûãÔÕ-««\x0007½½_ÓNpð³¿_{{u\x0007µ¾þauqvu¹ºYßý´Þ£®¸ÇÁ:1Uìîàv\x0012e^9yi(ø.ä¥yUø\x0016îQ±	\x0014\x001e1}ÜI÷ s«\x0013.ó®l¥yñ¶\x0016ì±Ðk|2¯=Ø¢£RÂâºÊCî¡÷¶¸î¶ÝM	NoËqs\x001d_aç\x000fMÐÅÜ¶s;\x00058äDÏpÂ}ÍêÀXÎî@-Ø®èk×Ù×kok«8P;®V*Ì|¥Ì&î¢»]gwsØC@]KÊ«iÎý­Õbý\x001d5\x0019úÖ¤å"ÏÚ°úÞ¦ÈùMÔ² ]Ô\x0018gI9Úp}\x0000Íû/Õ­
lÕmÜ°ß N\x0004w·äîÖó\x000f
MÜÅ¢\x000c}\x0012¦`
\x00028à3·ÚæïÏ^ª4q\x0017~IèôK\x000c¶Â4\x0011\Is¥H'óï«MÜ1	}Æ\x0004èÈRâ\x0001½ÖCNõr;N,LIì3%°\x0012-aç4ÅÍZÐ1U^»X±oUjMÇÌ²¸t	¤ù­\x0004¸çu\x001d¸U\x0019ûV%,Eá\x0007nG«RZÝzþF¢»¨OCÕ"{¬wÒÌº,CIQíyzK¹TKYÌoüìâ¶¬Ä§]\x001cTqÌR\x0013\Ê²Ãeg;t\³(\x0011øCó»kóùMà±\x0004½3ÄoT\x000c,×«çµ\x0018çãÖZÀU±4S:ZÂÚ\x001eB²\©öT\x0006ÀíR;½\x001c)%pÛ\x0007\x001ePî)÷¸Dpêq\x0006OýmáÖåÚÔkãþ
´óxÉÒa;^»¨}Iíû¨#O\x0000j·Ë\x0019\x0015\x0019£>n\x00017ÿ=à!)ö'p1¹¹Ãýü[U\x0013w(¹û<+°¹¨\x001bpK6 \x0003wørÖ-à®4á®Ï\x0007\x001be\x0002·f8:\x0004Bv1WVçbÙy0\x001e´0­D]ÜãJ1ørk³<«ÉÎÃ÷c\x001d\x0014ï27\x000bùíÈlàV»ØÎËX')6HT¡!ðá\x0005<,·õ¨rmªÎµi5
\x0006$p¯¹ Öü0\x0018æå\x000eZ¸Ë6ÕyÓf¹°un\x0008ÔÔm
¬ÅÀË«6Õy×*ù\x0000!m\x001c\x0014Å¯TÁÅåÀc	Þç\x0016ÂñÒ\x0011¸\x001aDké\x0006åÙù4Û\x0016p_N\x0015ßy°¬['Á¦Ðv?\x0012\x001dö-Ü¥-T¶\x0010:£¢¼fèp~
v^J³	¼)¡o¦\x0000-Ë,ó±GIß\x000bðXlö)× §»\x0007=_pñ?éî\x001dUµ\x001aÀ±ÎÏø=Mô¹xBóDÆ\x0001\PÆbÀ¡¥ÀKVwú³@K'd»'Á[\x0015\x0005Ûp|á]
<à}\x0013\:àMB+SqQð;b×\x001bÀ(L
~vûèI)\x0008úVò²rÁýb·WF\x0012¼Ë{,8m8\x0018+¾.Tï$¼]ì\x0016ÈÈÂ1ÄÏ.p3ô¸\x001a\x0002\x000cá\x0012î)$h!ðòìcúÎ>\x001eSÐ(åÈ\x000f\x001e­T0+x9_7¨	¼ìq××ã.E*38)x))¶àKmV\x0014·)øÙ\x0003®=½fú¨\x001d_-K?$¦ùÅ®Ä­ð%x×S;\x0002÷\ÿY\x0006JFð¥6 «Ê×zÕgUð]-\x0007åGe8*R:ævu¸E'eÛ\x001enLÏaâ\x0015B¥
CèïRÔå½ë»wók%cÞ\x0013c\x0018{A/	Ô\x0002^ú)®ÏO\x0001_nS°@/KüJ'4ÅÞØ±%x×½2¸ÝCt;ê²h\x0002WC"Ä|Þh\x000b¸-{Üv÷¸ç©"éÈ&Yº\x001e¸\x0017»ws¶â¶Ó\x0012J\x000chËÑ7MéÐöå\x000c/\x001cZüìáÄí\x0015\x0007ýJ\\x001cºM)ÏÈ®ïÁÝ .ír7/\x0000ÛÂ\x001dË\x000e\x001d.9ë\x000e£N)Ú@ZÎ3¶b1[èE\x0001½à&\x001bA±KÒn£eã6s]\x0013ÅP4GÁ5à/¯Oná.ï9}ß=§W4Í½\x0007\x0013NÐp´Ù!ìÓÂíËþöÿ?so³l×m¬	¾Êy{\x0002¿	 4:¢i\x0015¤¨&)Gôè\x0006íËºV,º)ª#zVÓ~ö¨ý\x001c~zÎ\x00042±\x0017öÙ{-,\x0000ª¨Áµ¹$K÷KìD"¿<o+mÕ\x00105\x0014àÌ\x0016\x00174l
pÐ­\x0017¿Ç;ÂÅXk´l\x001ch¥£æÎ\x001a\x0011äm¨¿§[ÚG^zSøáJR[VYq­ÚV|îO¡¿4WµrÜ¢b§ÊàÂM®µ*ë+Vr®*ÏâO²LËÄÈ<ÌÔb¤"¾,è¯(â9úÃ÷\x0016\x001bbà®kHÞË¾Å;l.c\x001d×ø#Ì\x001e¿·\x001b=Må\x000c°²i\x0011Õÿöâ3ðÿ¢ù÷Ì¾·ÿ-þÅoè¯e\x0001^|üû?\x001eÞ}þÏ_>w¡Î-69]<íLÍ\x001e\x000cFÌÅeÄ\x0004v\x0013õ§7?<¼{ûÝ÷oï\x001fµ*D#\x0002U²6/þöéï?ýB\x0004Eß~üò.ª}ë\x0014\x0012)\x001aC»B\x0008fÔ¥Û\x0003£x{ íÅ^¾yõ=\x0013}ûôîÛû4î\x0005êF\x0013¡\x0012æ\x0008TÊ3ÒÈ4J\x0010U\x0019x@¤é6¯Ü9¤\x0011
DJ#\x001aCH\x0015gî\x0013Õ3KV\x0013¡ä BÖ·YÐÏAæPaðPñUô\x0005)¤G[\x0006&\x0011¡ÃÕ7MÃ9¤©A\x0006êÈM\x001bè:±bÔóÀP½»iOAÕ´<]*JË`UÒM\x0012¾Ø%å\x0007\x0018ñ­rÄ4uÓ\x001dHX)ý9t®¾bÕÜþ\x000fÜ|Düì·Î!µ-R;Th\x0014\x0012å#EY£±rª·Ó\x0007ç°¶\x0016@\x0000ÄZR)ïë³Õ¶Þ	¨ÎaMºÁJ§CÚj¹q.á[Å»ÓP[ËxSDx;:\x0015Z¬0ÕÐ\x001c­)X©
À:@	ãõÎhÐ)¬fCJGï\x00155\x0012`
ýv¼îøâ\x000bÀHÝívÄsHuû²ê1ÛjÀÒ, Ö¢	d\x000f\x001dÐ/4õvPw\x000eªk.\x0016}\x000eAõº\x0004üÖS\x0010ã_ªEWo7_C\x001aG ·{ ¥\x0011j(H½´2AÞÍ¡º]¿?ÕÚæTés\x0008+y,\x0005«&2çò`aÀ
\x0000î6Ø9¬¡QVú\x001cÂªmaëÐd¬y²\x001b \x0000{W\x0010o3g\x001d&ag \x0007\x0002#^¶&ÊÒba#7A4Fî¾=\x001axÖÂ>`\x0018²åD&¯X\x001e¨Å3ôþv[ØÙÀà\x001a²	ã
éX­øU
\x000fnÖrºáæÿØLî Ëd·êûâã¯_?ýüóÇ.v\x0005ôºf]yx\x001bzBº½sõöÅÓû\x000f/_¿~ºÏLÀã\x0016q\x001cGLSti\x001dåÒ!â -év\x000eg\x0000qÚ"N\x0013\x001d«C&¢db6<o\x0001|ið<àÍX\x0014\x0002Öj\x0002±§\x0019ØT.¹Zo÷G*Ü¸Qc=¡ÇôÄ1OpR±&Ã&ãnÈ¡\x001cÆ!{YHý\K­D°«XØè-b£'\x0010ÛJ{\x00175/Z\x0008R\x0001u»µk\x0000°k\x0000»	ÀïÍ7OH>Ô\x0008|ºÝÿ7\x0000¹Ñ
3¡\x0015.	Ý
-4R\x001c`H;ËÖ@¶µ°\x0013Ö\x0002\åÊÀ.[\x0008ª2ôÜn@\x001b@Ü(²QäÈÌ6ÔýÈ\x001cÌ)H[ÎÚè\x0000âæ	±\x0013oGlª±ðrõ*/°º=2y\x001e²kÔÂM¨E0BeÕ¢´É\x0005m«I¾=\x0010<\x0000¹q-Üo\x0011/&\x0019w·\x0007c¥K¬ó\x0012È¾9e?qÊÑ\x00123@æV0PyÃ"Åð¦l& ûUV4ÕT Wêº£¨©\x0017ñf3 å\x0015ýK<°ß\x0011D
µ\x0001~Ï	Í;\x0002\x0013ïHp<ÕNmîÔÂRn_m=T·÷ìèE\x001b9eÝh#§êq¡^\x000e^\x001em\x0003ªÎç2ý¸F:2\x001c\x0015n¥ ·Y©ä/þ¢3ð\x000cùu´zR[¬¬Ù ç\x0005XY\UÛÜ$gkÿï-\x000f\x000cÞûØ¤^_üüñóo=´Ñ6\x0010ª:ÖÁ\x0006D'/ó(êö\x0004Ð\x0006îë§·?ÞgÎX·Ô\x0001øÿB_ù¡ý`ã\x001bôQµãúÒ\x0019\x0014ï\x0010cEë[´~\x0014­\x0017r\x001dÚú =´N\x001aõ¢ºÍú{\x0012mjÏ6
-X/Ó¼öj\x0017+òxNæöTì9´f³|\x0018ÑÒç\x0018Z])i\x0007^5êa8ä\x000bwfaO¢Ýø\x0016öÊ¹èFëñç÷ÖJv3U/\x0019ÍÂgÑ\x0016Z´&Á\x0017¯X\x0006·	)
Ïö½¦õh¡ÑÛ<©;Vñ\x0008	\x0015à
Õ#Æ\x001fÒ¨\x001eâQY¾\x000blj\x0015!*»LÑÑÄ¨tí\Fº\x0016Ü1»\x0019\x0018A°Tj\x0008,\x0006²e\x0016*È±\x001aa9¡­·óH·394Ïä\x000c!\x0005i\x0014e\x0005\x001a$é¤\x0019êö"òÓ¶q\x0015ØÚ^ù
ý&\x000cPqË$(­ã*¡¾JÂO\x001eÍQ)±\x0017ó×L®Û`¦¿4ÙEæ]S¸ø\x0019T÷7Ü!¿9ýF\3½\x0013£çì)¿Æ#åVSè_¯PÈD§i«\x001bôuþU·ù×O\x000f?|xñùgÖ\x0017"º"ÊûGã8DRj·GX\x0004ðË×O\x000f/Þ¾¦¿w\x0000zÏÔm>ó<hU\x0007\x001cp	\x0017\x001döº\x000exA\x0016N
è4\x0003Úr?\x001f¾\x0017Nh\x0012P7êÛã\x0003 m£\x001evJ=d\x001dyÔ(Ø\x001aAûý4Å	Ð®Q\x000f7¥\x001e®n§1ZxÊªe\x0010¿_,=\x0001:5êfÔ\x0003cæ\x000f¢qO%ÉXáqÁ.:h½áìÎÆ#Ît¨%²Ë´JP\x0012Ñùp{ëí\x0000jß¨\x0007}\x000e£¶¼1Àóè[Âkc÷SB'\x0010orBx\x0014:¯\x001cQ§4,Ée² Ë.\x001cÀîóÝ
:alA»\x0019ãáY2vQ\x0002\x0011ê\x0004a×Þ\x001c´ö¡Öù\x001an\x0011ýMÛ\x0019û¶ZY|ø¹|©7ÄÚËzlóv¿}½·Ð*cÝw"ÖÜ·1\x0004\x0006N¹#ÄX¦\x0006\x0004ðPÁ\x001e9\x001a\x001d`Í¦ñ\x0016Á¶ó¶\x001flÞ_Å=w7\x0012Ð\x001aÞ =wé\x000e°¶=Y;z²Ê\x0006^ÈÁ/é@Å\x000f=}w]h7u<B{UÈëGzà¸MEbôÏhµ\x0015´á6\x001dÃI´\x001bâ%B\x001bâ Z­K\x0005Ð
W\x0014¢
ZÐÞË<Öéæl\x001e<[M¶Ñ¦Ä4xÅbmj;¬+õ µ¾Aký\x0010ZCÜ\x0010{0£â(ZøÃ\x0010¬=j\x0019ï\x0002\x001b\\x00036¸A°T\x0018-GKRÉ©õ>J\x000fÞmÞhc6¡µ\x001aCQ£\x0005.$çeót¶¤>ÐÆ¢Å,\Å¢ýG¬=Eú\x0019´Ud$\x0008´Iµ'7ù\x0005
¦à\x0019hüÿ:\x0008Új
eþ@[\x001e²\x0004ï³¸â]Cp
ÄðI£2gº[RæÚ§m¥ý\x001dÿù\x0015£{9>Ë\x0008õcFÛD¥\x0013§ðK¦a`\x0003¡®ZJw6ª\x001c\x0006_²Ú0%\x0017hyCöy@Fâ¼º½F¥\x001b³\\x0019Ýô1AÞVÓýü÷¿t®2y¼0±§Õ£ #|¥\x001b}¿x/~ûúío÷öG\x0015ÈÛ9\ÌOAFýuÀya'\x0004fÏ¤äaÍèB¼Yãõ\x000b}\x0002±á=F\x0018ÐÌñè\x0001Óó!dß¡\x0014=õ¶Y\x000c¾ÑæÚ\x0019îÇ¬\x0013o\x0017Et)¯Õ+\x0006¿ÕZEüúõ`6®Q\x000cú\x001cÆLD	¢\x0019	Ëð
4\x0016y,Ræ¶J\x000e7êû§GS*b9øäÑ\x0004/OJ:ûë\x0000Ývö\x000f£¥íQÿáó_¿~úíËÃÓ¯Ãÿzóñ·/}ÃË\x001axö\x001aÍ\x001f¯ávj\x001a\x000ec§?¼}ñáåï\x001eÞ}ø\x0013þ×§\x001fßíLa\x0017I|ÚJâÓ
Q\x001cÞ GN½$\x0015h$Dñºv¢ÚÛ¼¥S¢\x0010ÑèF\x0014ú\ñ³`}é÷ô0±nÃ\x0004s{qê,Þ7²x¿FÅÐQtL§­\x0010ã¡^I¢;ê\x0010\x001eeÃ*B²\x0004µæwI^(¹6	¶²þg1ªùYès(¡r/%ËJ¶@ËÏbá 4>"Ë+d\x0001»F\x0016-\x000b!J\x000b:s/\x0006á\x0017\x0005sÔL3"Ëv\\x000ceiÇÅe	)R³´4º\}i^\x0001ý;ü.´\w#KÞµ»B\x0016ê¾áJ\x001ah!:4Jê \x00067dñ­,kîK\x0000 t~EUÖ`j¯õQJaD\x0016ÛÊb\x0017Éâ\x001d7Hè$\x0007\x0019tª\x000f°\x0007dÙrQRW¡^t_¬¦ºr)|ÚÊ!¯½÷«µc²ØV\x0016»J\x0016SGiÐ¤Y! ¬)ð;¸0h[¸ØåÖ#\x001e7ÍµE<\x0019^»k¢P\x00139jj:'És!=Ô¶nú?þÛÿ×ÿó×Ï?Â¯_\x001fÞ|þíç~ùµ«à\x00049èÀ£ÛÊ"¯ê\x000bÎì\x000fL¿|xýð*NøÇ÷\x000foÞþøú\x0015þÝ}A6ÕT\x0014äª:.lË\x0000ÃdHânsÍH²	\x0015iÂÜ/Ä$¶dCÝÒö\ýMì¾%\x001b$6ÄEÐ2íÒ\x0010¿õP´®M~}ö\x0001I¶\x000c-æ¡eJ\x0014àf\x0003@#/|p\x0011¢ü&~¿¡u@\x0012»aÄ {²eÄÄ\x0004]\x0000\x001f\x0014qe0\x001eE	û\x000eÌ(¾\x0015e~\x0019|èË´
\x0010y°4X¶Ã\x0001Ô>Ö$Î4?3~\x0014JÉ\x0015Þ\x0012ÈkH¥E$ý"ß$^ÁV\x0012ú\#	1\x0017@$Iê2í\x001b>ì4;-Ê¦oD¹ê\x001b\x0019\x0016&ØuA\x000f¼N\x0001\x000b/ú]QgEMB<À-\x0019Ö(Q±~\x0005ªys\x0017\x0000oÐD×ì¨Wê¬$aÓ<L=Ûæá)I\¤\x001eIB\x000eÝ\x0003ZÌ%IË\x001d\x0016|C\x001ag­39e}b5|Zä_"TÇ\x0005V:.\x0010ÿ½#¥ñ\x000bb¼üå¡Bí\x0010À»\x0018ùw\x0000RêMÚ^àÁëÝ\x0007åáå÷\x000fõo\x001e\x0000ßÌP ðí\x0008Å\x0010ðDq¢\x0000/íVI[NK ðýNÞSÀC\x0003<L\x0001÷øDX\x0006×¡ÄIKG\x0007»Ï¨p\x0006ø¦êÀ·U§\x0011àÞñ^\x000e\x0004n¹­	}ô$ÀáÞ. FÜzÛñ=\x0002<EÎ,:¨<xúp\x0018¸Þ\x001fý?Ü7'Þ°á
 \x0007ã\x001fM\x0001æ\x0013ç\x0016jä"Àm6ÝêÛlÛÕGpGsQÈÃÉB¬ª²Û¤u\x0006¸kî&}Î\x0000\x000f*pHªb¸½,Ù\x0014¢\x001cù~3\\x001fr/§¾\x001c¹!%ß>±üø÷ÿÇç®r_æn*\x000e -{ýØ$­ö¹^>üñéÍÓy{¿ÚWà\x001a»kì(\£¹[=:úcAKÖö¨··\x000fí¦CX¹ü(ZtÊ\x001aãº¶J®kµ?®×v³v\x0010ÑÆ4\x0016õ³ô\x0006*\x0004î
\x0008ÆÚPá\x001eL·tÁÕªÕ\5ªºôg¼PçbPÌkZVµ\x0000¯u
^ëFÏ\x0017\x0015¶G*ë¼³T'-çk\x0017á\x0016/âE%×±5\x000bèjDÁ«èÃ6)\x0018¯G,Ná\x0015r¾ÙÒù®¸n:¶ú\x0010Gõ\x0001hGØ2à-Í\x0008²ªïþô['\£\x001bë`ô¨y\x0000#S®rV\x0006´·F¬ÃQ\x001cÙ\x0007wSÈ\x000fE\x0018KíolÍaFø ä¥ æú\x0015p}{º~øtUfWÍ´ûI	+ÂèñÆÛË0Ïâñ¥Ï1¼^\x001b\x000e ">Ê´Ò¸!GÙ\x0011÷Ç;ñnÇ\x0014\x0010o3¦p\x000e/j\x001cT¢þä2kjªç°ß]ØW\x0006¯6£x­¤\x0006ðqSônÁi'pÓ
ã°-g¸£¶Ü¼ø\x000e3ËD6&xõ·ÂºÆ1³nÔ3óô\x0016³ú&Ç]<ªæa.½\x0017¯oÕÁ\x000f«\x0003:8¥\x001b\x000cñZ.B@²®â½½ÁèüÛÖæ»ÊûÖæ»ÎX5\x000c#»hÄ)eØES¢\x0016pFíµ\x0012×°­²ã°1¦¿\x0004Eê\x000cÅXèú4¯1\x0015Ï@k3\x0001Ú©ê^¢vó$V\x0002/î¥^e2ÃP\x0011\x0017\x0014oÈÎ{n\x0012\x0018åáÃØn\x0005ìë>Ù\x0012Ö
£\x000e\x000eê(\x000cú¥\x000f@öú&uD\x0004p\x0004Úªoé+ñíÔÛ\x001f¿|þÏ>}yxõËý×?¿üôé·>à)Ô5çàxÎ%\x0018Ò¢ÑÞ#ú?¾{ûÝ«ï\x001e^}ÿÇï^½üñHÍ0\x001c
ÐÎÂ
Ê@SE,CôBva,\x001e2\x0015aS"G\x0011¢_ Bàv\x0012!ÔØ\x000b_V:bI:-CjdH+dðÌ¾\x0017u
ZÊÍí=I\x001dMò!­\x000cÉ¬ÁqK\x001fÊ\x0010rÔÛ2\x001cÍCa;Ñ2\M4\x000f
Aû$Dì6f!LÝ¦È&Ï
±I1\x0010mø \x00106ò<y4\x0018irÓ«\x0016j«d\x00062ÏÊà\x001aÛªÝ
ãJIß\x0008àár^Löhèã¬\x000c¾¹\x0010Ú¯¸\x0011T,/ÑQZt\x0010&¬tÄÁ{VÖ¸ê\x0015Ö\x0015Ý\x0007&C2*
MF\x000fID8èÑ;+BjïtZp§!HO[Ìä\x0005E\x0004c½pÔ\x0006zZÔÊ°à\x0000tí\x0000XLÝ^ª­Ü\x0007sDWwR\x0008³IÕ¢\x0010Æº\x0005BPV°c hÊ£\x0008q¸«å¬\x0010Ð\\x0008\x0003+.v\x000cË¼\x001d^§Ú\x001duá\x0015bg"!¢\x0017ÂÓÛV|&ãUý%,\x0013Hp´Æã´\x0010­:Å\x0015êDØYÊT¡Ç\x0014º¥\x0004GS®ghYa<m\x0004´URËÇ_Âü^BXÕ\x0004\x00119?-DBO*ô¨øNh_÷Ì\x001eñU\x0015B7wÂê\x0015w"Úz'M
Jº*hYîÚwÂ¶&Ö®0±Þ\x0003\x001d\x0016"EÞÄ\x0002)H
:\x0007`Kp­:¹\x0015êT\x0008\x0018rF\x0016;
¨ª{s\x0017G¥Ö·êäW¨\x0013ÚU´ª¯À\x001elÂðeí;AT \x0010+¬\x0013ÍÍ°\x000cQøQ½Ì>¢j8+Bk`í\x0012\x0003k\x000co0Ce
²w1Y¨;È\x0017¥vÃ]\x0008\x000b@
J¼\x0002\x001e»À%"-õîL³VöZ§\x0015×ZÛGþ!¬\x000cd\x0010Û.W=\x0017aÛe28³À¾º$á\x0010-´\x000f,â^æ¤üâÎ¹æFÐç¼\x000cÑHsõMJ8I}\x0014Æ®O\x000b\x0001­\x0010\x000br\x001c.ä±,\x0004PßD¡'HjñØ²8£\x000cW,Î2Xs©åY\x0006é¥±ÅBèæ Ïy!J«[\x0011BS\x00060\x000b!)u\x0007¬¡õü
¯Éi/ìÉ\x0016ýW®ÀÓúZ_ë5ùÖáð+\x001c\x000eæ{`,1°×5ór#àï¬\x0010Ðþ\x0012°âPIRÖyÎûAHIü×	±óB´Ñµ_\x0011]Ûdê0JÚCà¤\x0019¾tkÝ&PM\x0003Ô4\x0007ÝZLW\x000bÁCª>øZÛ\x0004®qÀ-p0¤*«`1\x001a¢G·Ù+aL8\òxV\x0006ßxMô9/\x0003ú\x0019#:Z7æfªÚ×åÚ\x0014k
aÁµ¶&V!¨TZptþ$ßt´@ï´\x000c­2%Ê\x0014äµ6 õ¨LB'\x000e·7\x0016"µB,È#[\x001e=çóAq£/þcVtñ§æ¬\x0010©µMimò±\x0016é\x0016:¾`j2\x001c]ÿ¥B\x0004Õü\x0012ô9/¾$þ\x000eo®¿µ\x00066´\x001d\x0010aE\x000b¥]U¾fô¹W
@èu\x0012,6NÁÚV\x0005ñ\x0010\x000e*ÞAwÕI~VX\x0016¢U'»@LLò^\x001bôf/¶\x0013º¶tÄAsV\x0006he\x00152ÚGÅFÅ4Æ69µ¸`zµ\x000b¿-ÁÉ`q\x0002jÝ\x0014\x0002ï@
Z;n¬IKÎ\x0017N®¹ZÆkQÌ­­5`\x001a\x0006äû¡\x0016í¬»êKdÉ<År¼ÈWÅZ?d7:_|&É3NÉÑêå	îÒ\\x0010¯«_vñWW,Ñ¥n(hvk\x0013\x001aq¿Êl4{ÄÙíòÑ3Q0`[!Ëÿô*\x0012\x0006J×²Pì´B\x0016Ô Ù?hcÞLb¸\x0015\x0015[°E7ý(a(?±=vúQ³óî¢ø½°¸\x0002=kYÈYY"¥RLéw4<¶\x000e´hEÑGðçúg¢@Z"
½ø\x0012(Ç7^|¹-yáÃ"Y
Uî&\x0003îÒ-§åýoÿ8#\x00021æÙÓÂÄñ)Ô¦ýa®\x0008ïü¡K\x0004Ýp;{R\x0006âU¶Õy,k~ðFDQ)×\x001bÚvË\x0010\x001a\x0019nçge0Ìô2X	E|¬m9½-\x0008½"øF\x0004¿B\x0004|\x0007uíy\x0004À×\x0017Ý÷ÖeºE\x00087³U'E\x0000-¥{CË¸9 TIÒJw^è^\x0019@7\x0017úfúö¬&)Y\x0012ÛÔp¼2_'\x000cp×Ê°íÛÔwâÏÉ¾¿¸TD%Åå1oj3¶[|¡cs\x001bâÛ R\x0000µbs)Àã_®oÃê!52ÜhÏÿ\x000c\·×)Öý-¦ª]¬Jº}ß´Zñ:DE;ÓKÐdhÕO¾ÓVª\x0019jñï Uû8¨%¯E\x0012G6*ÅZWZ.kÛ5ï³?D"âRWªÏ4¸(\x001d\x0014î4ù¬\x0010¾¹\x0011Ú/¸\x0012\x0006¯µæ
\x0005Ù\x001b÷ºVøöÇ/Ï\x000b\x0011l#D¸2<+\x0004H_×\x0017\x0019\	èmê!¶Ú\x0014\x0017hE[ÆÎiE,g\x000c¡^°OÆtZ\x0008³F!¾YX:{%2\x0011ºÌú[+W¢¶Pô\x0002z0Í[MóBH=\x0007"á¼§MuBÝu&\x000b»­\x0010+<?êburñ¢NZ6\x0017¿t´-{+½9°sR\x0006[»»R%bÀG\x0002*±ÁZ\x0019¶®V·®Ã2ÐzC`Ûä¥Âç}ý\x001dBï|B¯\x0010íKgW¼t:Ô µ¦>×B©ÄâçÚBûKÜ\x00149)VLp>\x0007d38Sy\x0006ôâ ÚÆæVÓç¼\x000cN\x0013{UéÕRq ÄP½ÿN\x0011i\?gVÄ\x0011\x0006d`Ç*}Y\x0002ë¤\x0001ØµOk3\x0003nEj@Å(5Jj>àx|!DÞqÈN\x0019üf)¥\x0006ôÍbñI\x0019\x0002"½ô\x001exÞV\x0018dP;¥ýîç0MnÀ\x0005É\x0001tì\x001fyæÈY¯°µÞ\x001d\x0017;¯M£ ¾×(xR\x0004e)¹TF,\x0007\x0003\x0006\x0017µ+ª7Ü+Dëû\x0005\x001e¸IÉñr\gá$
zRu¼b\x0004õ´\x0010 ¯\x0012Mó¿\x0004F\x0011±ZW¥Äg2®2?ÙÞ¾¨^!\óÌæð\x001e°ÚKi\x0005_<	|/wA¯\x0010í\x0005wÂ$çy«9z¯Jzâ
yÆì5\x001dí<-Dl¬Q\x001c-æY\x0013Y©\x0011ÝÚMT'[!â¼\x000f¿Dì«\x0005#ËÊÀ\x000eØºNË\x0010Ú.,\x0008èLRF¨Um`:BÐ¡\x0012¤e¢Î2ØÆÀÞé:)\x0003óï\x0010\x00195­Çf!ìÚ\x001b\x0011 q\x0002Ì»M¨LK¥\x0014Ð1!1kÒfñ#A\x001b¥¶)d3\x001f\x000b\x0014.Ä_ÊÉÆrjP«Ü¡k\x0003ºh\x001bÓ\x0014í8BaT\x001aÔ\x000eh\x0001tñhë\x001dNè\x0015Â7W"Þ<k_-õi
o§¨KÅÕ®µ¯14ö>ç	Z\x0008.2Z*sîbû\x001aC[Ü
\x000b"kå7Öd2hÇ;Ä}¥Wv½cx½B¤Vn\x000f¦\x0014\x0002´CÎÔ\x0012
¦
\x0011Ö¾\x0012©Í¿¦\x0015ùW¼g\x001a\x0016ª:9ZQû\x0004óç\x0008¥Ïù\x000c\x0001\x001a§P:ôU\x001fmqþ\x000cª\x0008aö	7ÏËÐ&jÒD
±ód\x0013\x0011\r(A\x000b·Xîù>!´RM /HÀZ~¯1\x0006âæ9JÀ6u3&õ
¡ÛÚÒ+.v´âÁzð|'/¶qzi\x0000z×Jq]åäc\x0017µ®ñ\x0007`\x0016e\x000cëÄÿC¿déÍÖ¦íÈßÓRDj0ã×®R\x0015ãó k\x0003üÚ\x0004¦¶®½\x0015ö6\x0017ÚY\x000fPödcPí\x0007ªü\x0014Â°k]o\§\x0014.´\x0015xw{~êäO\x0011ëÄvÐ5íQ\x0011\x0007vx+Öþ\x0016^]U¯oíW¨Rù¥\x001d\x0004\x0015
,;ãb¥B¤önÓ÷´\x0010¨22\x0017l_X)Rô\x000e¼t\x000bá¯Xpµ\x0003\x001a(`\x0019\x0014ÓMòr)Ð£]ýKÀ\x0010\x000b»@®becYW¥\x0010òÒäÍÚ?½ÝO»Gí«Mô¥ewY&\x0010\x001bk¢
±øÁ»Jé%Ù³q6÷axGmÉE(RØ^6^)Úè./BIWGA
vJVKøÐ;ßÙ+ÄÕÕ¾3ày^\x0008\x000e¢¯½¼Ê	×¹wûësNK\x0011ÚB|þÒ\x0005ån'\x0015x%!(áÎL¾{&¯W«Îð° 7\x001c¥H~Â B2ãèæò³
ÝL+½R\¹Pa\x000b\x0015 \x0012,£9b®@Ò(\x000eñºù\x000e;º½ÛQ¯¸ÛÚqZ9a´Åù}¢¬¹YÛØ¡7¾a­ckÔsÉckøBa±:Å¶\x0008¿ç¥ \x0017|µcd¾nü%d\x0013ÀÚÂ\x001dE×í\x000c\x000eGÜ·pÎ6H\x0004\x001a[É^02æåÀJê {Vµ?Ò{&\x000cE{\x000b1É*\x0019\x0003qâj¤\x0007Ð(XûË \x0015&\x000c9éK¡Ö}¶ZøG	ü´f«åãâw\x0010/Ç3aèÂ¬\x0010Ö¤ûâ_%­¸\x000fÇÇ k¤ðe\=7Ö\\x000bC]+®\x000c1ÿ^òÏÑÊ¬Q-\x0004,î:õúÙõ§\x0015¢(t°Ì5
E­\x0007 yÛßÐ2Òp-
µ!¬Ð0rÛÆË\x001a\x0012\x0012G9· îï\x000c\x001dz¹%ÞWý_wøE­¢\x0017¯\x000bßyÓî\x0019ÿøðÝÇ¿|éYÜj2ü4\x0006h\x0019ß\x0018Fîã~»ÝË×O\x000fß=}ûîþÖÖ\x0002xSóFÀÖ\x000e\x0003¦e\x0015:^áG^ «:ià\x0012¸¾ëÇá*G;«2Ü\x0010¹.hÍ­±´_ò`\x000fT'à ·Q\x0008ÃçK/2\x001f°\x000eÜöç\x000eúº\x0001oòÇ\x00088úQÀh%¸&\x0010vY~©\x0000ý^ ^ÀÛí­úÙöÖS£å@©U]t\x0002\x0001\x000e£]¾[#¡Ç­\x0004ªÅ\x0001í\x0015ÄÂÌæý\x001a-ÖÆ´Í0b´
%p	¨ÇÜ\x001b\x0014±4\x0015ÄfÀ¸\x001b±kÏØ±IÜ]\x0018O²\x0018)·;3â}:nÄ)1BÜ.î<ØR­	FHêâN9b½_­é\x0006¼Ù£EC\x001c\x0005ì©»«<v\x0003åa\x0004L·\x001eý\x0001A/bÓª±\x0019Wc\x001f\x0015oi
¡4\x0016\x0015Zò
8\x001d,kì\x0005ZÀÃ:A!iqê\x0010oä^º$\x0005èÝ~ç{7à
ë!\x0001Þ²\x001e\x0004lA8\x0005N
@ÒIØïNö\x0003nO80Ì\x00028\x0013p1·x\x0012ÀGërû\x0000ÛÍ¦«ì°Á(`Ú\x0019øÖEW¹­p=x¿Ï\x0017ÔØ5:A£ÁqK@FÌ$!Ñ¤úÜ\x001d-9ìD\x000cÍãA£½f6aD\·¤FÚO&Øb»!\x000e Ä1\x000c#ÆÇÃ¦j(x(ªOb)ö3?½·3JD§`&\x0010\x001bNïdÄ\x0011G½½Û_MÐØ7ïóÃï\x001dÑ(
£¨\x0014u'\x0018Å´\x0012>-:chnágAsùB9væ!\x0010õIF\x000cjè¨\x0017±o£\x000f?\x001e~\x0010oJ(zðÈÃÀÊ\x0008`X\x0013?n\x0002ô°R\x0018/!Ù:
ïë;Ú­¼\x0004±mâ%ú\x001cEl\x00135\x0016Ä=cðÀMb8Ü9ÛØ5J\x0001n\)¨¬\¼D-@uª7\x0008â£\x001dñ}sñès\x0014±ÜîC½\x0018Ò,í­\x0013ÄzÍ#
¡q+ \x000c»\x0015¦ôtgÄ *gæñï\x0018YsÆ±½yqøæé\x0018y\x0003\x001a"\x000e¼\x000e\\x0012V»`ö\x0013ÝS«ÇiXuÔ\\x0004 R_\x001dÆ­TÁ\x001em1ïC\x001côUöjØVhð<î<È~\x000btA+â}ænÄm\x0017ÆC<Mé	¶Ç\x0018âÜ
"¥Î!O¯@ì[ÄãZáò\x00191*\x0008³9\x0010æ³àöçtº\x0011·/H\x0018A´WÜ2-ïãDûn+âý\x0019Ú~Äí\x0019Ûñ3v Ù \x0014t@8'ñØãà¸>G\x0011[[ý
Ô
^ãjþ*8·$\x000e±½yqøæ)Ú{]2Ç)Y¡³ÄëÆa^^±\x0000qTM1!ªájB¦\x00041õSfÀ ÔÎ\x0008xÉ\x0011Ç6fã1òy}D\x0001ìdDÀ^Ü
¿&\x0015ÛzM\x001c/Ø(ãhzJyJ«G\x001e\x001aKR¯	ä'Ï\x0003\x0006Ýþù{¸"V\x001b\x00103Tä\x0012\x00105¸LT³$\x000fÛO9\x0017»­Í\x0015\x0006\x001eE\x000f!\x0019)\x0000'Ê?XÏv"Yx
\x0012\x0013À¼Ô2pEÕ§\x000cÜd\x0002¼]r\x000fÕ\x0015+q)ãÆÈu;@]%\x0017´\x0015\x0007Ô}æª\x0013\x0019kÜÅ\x0018\x0007îðýæjN¢mM\x0013r²×|WwÝíÀQà8pbìxx[ékî3\x001cLQpù\x0001O3Àuåý£¾%6^I\x00195i\x001bíÒ5nrA&p[àe3è,ó¢ÅÍâÄ5^4ÏG3\x0003\¡1\x0015¸å!ÙTÃY·¿¯\x0007x¢ÿØº¨é\x001bÝº¨ß}üùç~ùéSç"\x0000/g
è?éòð\x0018/5VwôT~÷ôúõ«ï_½ÜivÉ·;Bn\x001f÷Sñ7bÂã\x000c¹,	FK»óû­`ý7\x001bY	sãT|Ì1òk\x0001­dqß_ÑÙ\x0018zn61-þñyHûùËþðu v*j©\Æ:?î\x001eHîÙí\x000f$\x0016}~ûî»?Ñß=\x0002\x001e\x001aàÏÜÕSÀç^®\x0010U$ºÊ\x000c\¸g\x0011xÏãÞ	<¨-ððÌ\x0007<\x0005ÜEéÜ	ÁTàÞ;¥Í2àz*Eàúyªô,rééJÓLÁ\x000bSnt®§!¦\x00139´Èa\x000e¹Æ¿\x0010&ºß\{±'nõ\x0014ò
«\x0001!OÏbSÈ¤:PÝ¢´ô¸x9óý¼sÈ¡Eþ,é{\x00029>°A\x0019iíq¸ÚÃ²\x000f¹Ù#dø,\x0005u
y´\x0004·¹§lIF\x000eµ·î\x0011ú\x001cò+c>cÍm\x0002à9µünò\x001cçÄ\x0001wn8ê\x001crÛ"ÑóÜÕ×³,ä$äõöDÇ½ÈÛwhê!²Ä\x000ffcE\x000e|C\x0016é©Z<µÈ¥\x0001Ï!\x000fLÚÙè\x000br¨¶eá
µm1ÏûTN!·æ»-]NñÐCt¡§
Ö\x000b<¶ÀÕN\x0001÷A\x001a@ t\x000f:{¹ =qO'r×\x001aE7g\x0014}- i)sêÔ¼§·\x0013¹o¢3V¸ï²ÛbøÌë¦=´1ëLoâó\x0004ç)äÎIæ.(0pÉJ8×Ó\x0002Ð	<¶Àã\x001cp¤3\x0012ã\x001d¿ *Ô>'ÛQ,ëCnc£æ6Î©¹	µ½7¤j\x00133åpiï]<¶ÈçLÕ<£gêÛ¯uíÛç ;Üù& ¢Ï)ä yZ"\x0002)¤8Á\x0019A\x000e]\x001dÊÈCó\x000e¹ç
ç'\x001d&Òn.¦!r»`÷G	O í\x0000-]¹1'p\x000eºâÅÛ\x0018?_\E%KßUk=\x000eeQî{:\x000bðï~û¿?gø?|üû?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=>|ú¿Fúu@\x00032\x0011\x0016a³#§ÿ´ ²ÝÙ£wrsöÕ»ë«7'SBÙZ(»¦Pí
IÚkÐ¬<nÿç\x000b%e-+Jeæ®x\x0019-õòË2¦ÌD9dPÍk~*£\x0012ÁNÞã(("UJRi
÷8®.T\x0014\x0014ìm~6Äþv÷PTÂ«Ûû±ÍÂÂóÉ¦N\x0004É\x0013×\x001aü7^o+v·¢|{~UÔÂ«³Ã«\x001d\x0008ª\x0016A-\x0017ÁHê\x0010>&ë$õ<Á\x001cwW/\x0015A×"èå"àÌ_AyÚ\x000bª\x001d±æ\x001a\x000fïem	L-Y.\x0001ó«á\x000e³H\x001bð \x001cç¾bï'úf`k\x0011ì
\x001fÁÓ\x0008Ú£¼Õ\M\x0014÷gàj\x0011Ür\x0011x¬ÜÁï\x0017\x000bñT¼l;N Í\x0010Á×"ø\x0015¾É}f`÷dÑGÜ!güTÝk\x0004¡ ,Àû²­]\x001a\x000eãæ\x0010'\Ã\x0019\x0012ÄZ¸Â7P§ô\x0010¼ vn\\x0004É\x0012Lmà\x001e\x0016@Æª\x0015¾$	pjÙSB3\x0012ñª	\x0013{qfHÐÚå\x0015\x000c³âú/|\x0004ÏÔDN\x000b6Ìnb\x0011È\x000c\x0019\x001aÃ,W°Ì.äUî\x000e½[Ú\x0010¥\x001dù~&ÈÉÂ\x0019"4Y®`!&%\x001a¼+iæê+¬mÖdcÖä
v
ý:6Í÷´ãb«I\x0002+ËÐØ5¹aÓ\x001a\x0015XÌä\x0015\x0003M0«Û5ÙØ5¹aÓ*ó*ãg°Üìå«4G!CcÙä
¦-jª_ S\x0007æ´:%kL°fm\x0017I6¶M®`Ü´§$HòTÉÁ°Ä~\x000ea¢\x0018>.jlZÁ6\x0018EM6"@LÍªe/ÏOôÏ\x0010¡Ù\x0006'%9ÛR ¥¹¡}8àå­\x001e/¨&äQËc\x001e°ÀÜë\x0004Z(Ep0eXÝUUmP+Ø\x0006«^ÅDZ©¢zvV'ø=gÈÐØ\x0006µÜ6 E\x001f¹Û[pË\x000fÛ\x0006·¶iPZUËÕ*Òõå¯ ÒH$G
\x0003,B 3!C£VÕ
j\x0015¾$_Ï\x0018âÍÖÎQÅ\x0015¤Ö~Ðº\x001aôò¨Á\x0019A\x0015ô\x001d<÷ò\x0019Ö~\x000cº1
z\x0005Óà,\x0015&Ò@\x000bM%ºP®hí!Cc\x001bô
¶ÁÌY£Bî´<è,\x0001h¤µÓyºMç­\x00105¸xª³Æù\x001cQ\x0002\x001fr2 !CcÝô
ÖÍ)A
Ãä\x0019\x001ab6
\x001bâTi\x000cyÓ+· í B\x0010­\x0002åbBñWÕÚUÝÄ
z¸\x0001ëþ¬<gV½.¶a p\x0008}Ó+Ø7öÈ$\x0011ÄÎ_j¸ ç\x0010UX]±6öM/·oNº¼ì\x001d=OÖÚ[Ë)¥©Iõq\x0019LcßÌ
ö
âNE22ô\x001dx\x000cÌD½zfÏ4ªÕ,W­Î¼rÙ¡Ï¶.«%¦jì!B£Ìr­ä<=gç9'\x0016p\x0014¾ÁD\x001bÏ\x000c\x0001\x001ad«$\x0017¸@
ï8½\x001axS»GdPÛEC%ZR¿¹ì1Ñ\x0005â¬\x0017¸ä/oF	æõ1Sì1C¼1E\x0010S\x000bbV\x0011Ä3k¶0`´sWR4\x0004gtèe¹ê#lÐî\x000føòéþáýû\x001f\x001fn?Ï¬¯ã:\x0001A«U¼"§¬5Lu)'Bë\x0017.òË«\x0017ß\¼¼:{ÛQd×ÛEv-ZêÎ\x0017\x001fþù¾»}\x001eF\x0015n^çh ¾&Ø	þ4¸õòüìÝ\x0014~UãWËñ[\x000c«ójuC¸(ºmé¤yîÆ¯küz)~ORN]CpO1óh\x0018Ù\x0019Ænjìf1v©OM!Ø6D¼W­©\x0001¯aø¶oÂ\x000fRdÃ¦_fÏOyÁ{jÃ\x00143Ô0~WãwË¯frÌûI%Ý\x001eá\x0019çÚînü¾Æï\x0017¿){\x0003Núäã·¼\x0013,Ñ\x001a}X|úÁðö» ¹d¢8¥\x0004¿Ï\x0004WÝ(üª\x000c­E³öiæéÃ»|ú>2U\x0011Ü~Þ\x001dì{ÉÌ»\x0005h\x0014¿\¬ùÌVê!~Î|Ep\x0002\x000bà'Z«\x0005h´§\¬>õ¼&Â»{¢UánÔ~ª{XFÊÅ
4âr<â\x0014N\x001cu
4ðÚ[ç:÷tão^°\ø%Ø\x0013É\x001fÀ\x0016f=
®/Ý \x001b×ó\x001dô¶ï¦w\x0016v¼øp\x000bî5x¥rÈ-
Zñv{¯Ty\x000eH¢o\x001aXò£}Rþî\x0011¯To{uz×|d\x001e3\x0003ôÐ
wj ¦¥6]øaÿ¦âqÉl-Ù6åÿRÉ<%eÉ 	W8¬sïÔ<Éb-Ùövi Y^§¥\x001cg65nöùóÄª
¥ÞZ¼X.\x0014\x0012DH\x001e8y®,\x0013üá\x0014øÀ*aÑZý±®\x0002ñèjl¢Ô6D\x0011Ë@òW\x001bÚ¦1,iDÛ^³ð«É²	ES´Ëú6ÿlÉ\x001a\x0005²³4d¡d1ò\\x0006ÞGCÜç¼\x000fÝMõÔÎÌnÂvk±ÂÏfÛ²¨rWM«Q²cTª;è[w/~qyýîÍH¾\x0016É¯'RÄ\x0001C
väp!¸M°Ü»¦c\¦XË\x0014W	ü'N½xôÅ3\x0015<¯\x000b\x0008¦sßHv;aÅÎ®­¯\x001f\x001f>\x0003ò»¹	>/PEä\x0001.DSVY&\îÝ9oêëë«·ðOwä÷ìvÀ6IUD³\x001fÆÕn¤/¤àÍç¾weû ln;/ëÂøòùîùáöy¶p\x0006|\x000e{Â
æ¨6¯e(5²½|wþîêìÝpº\x0016N¯,WHÉkg´â]Çrª3p©p®\x0016nûV.þr1ÕQ8¡Ê
\x000f-x[¹è\x0019\*¯Û^\x0017·øËyGk\x0008¥d¡`\x000b-CçÖaÙüv¹À­M¹}ÿøýý\x0003èÿ÷\x001fn?¦Èd\x0013þÄ9!x\x0010]õê7'9{qýå\x0005H\x0003.Èe®LÉ¥j¹ÔÊrÑÂT"à^«^ÞeéZ0½²`§ðep<ýSX²û\x0017åÌ\x0010ËÔbuÅÂÍ'FÇ=\x000fY.K\x0017lÿ>õ\x0011ÉÂöM\x000c[ÕßË[\x0010hn1
'\x001b²gÌÇÓÉíYw	øò\x000cóS\x001d:#l«°å]-HG\x0014Ùm$rÅù?K [\x000bd×\x0013(\x0018Þ\x001c(</¬I]²@Fô{S½\x0002©mÔ¶@¸`d®­B®-*m\x000bjISl\x000b\Æ^ÍGKFú\x0005rµ@n=$MyDFsØ¥\x0015?"\x0015;k|ã\x0012ùZ"¿DÁ³ZÀöÌî¡äª¥îÕâÃ\x0002Z °@Næ^N¤päF(\x001dxÝ4\x0004ÆD±(®&ÃÆ`&ËàI$e©$rý>ßDUî\x0013$jsËDRkµ¸EªÆÞ-JóEj4\O5\x0000vNJ"IÏÊÛDÇì\x001fn ê\x0018\x0013©yIr½§ä°é6Ù\x001aæ+R¶ÔtU-!RÔ[.\x0003NÐÖ¹W·O\x001fÿù¿\x001f\x001ff{wØ
ç¥+ }}nJd\x0006Èà'ö\x0001mªt¯În.Ï¯¯z|;\x0012ËÕb¹UÅ\x0002s$3¡
¡°\x0000â\x0018G\x0012k²×rX¡\x0016+¬*böd­µgN5ï)Q\x0001oj_tXRlW±À´³füÿûéqJa"çb5K£\àñl÷×ç7×G©X\x0008U\x000b±##\x00166gW@\x0008Ðy!GÃ½\x0018B#©ØÎÏÎú\x0012Þ	el\x000fÏ³Cà\x001bð0 ¼#«¥ØNzÍ\x0002)\x001d#Í\x0003Âû'\x001a<\x0019lêìY\x0019"ÔR\x0015¤·@;«ð×T)ÄgÇ
ä@¾nR
»ý¶íîÛ¾¿{z\x0002ãy÷\x001brh\x0011Ü±J<Ó`'¦ä-Î³\x0013\x001aTo
!tq~s\x0003¿:ÿ¶TÓ¦ÄSµx;¯~¹xrØ©é¹W\x000bòAOÐ¾,ÎÔÒí¨ÅÒEW\x001a	îÌEÁU(?1´T6_Ë¶<^A6Ë\x0005^\x0010	7Ï'ñBùt½mzsÅµxÛM"Å\x000bY¦$,Ç\x001c¬\x001a»\x000fþDéd«UVW+ALõ\x000câ!×O &K^\x0004\x000fþøz97½\x0007I¾íÞåòIWn§q4¦\x00029-9Ö\x0010,\x000etVÈ'·­´í0ÄëçßIÊ»ûÁÉÌW ¥¡}ÅD"§é\·\x000bûúÝ¿l7ç\x0017WmÜVÒ¶AÔ\x0012iÀçÈëìÐ;/L\x0010Gp¢½Æ 8¶\x0016Ç®%óøò\x0000¶§©ÜèB#ØÝ]ïâ¸Z\x001c·86Ð\x001cá\x0015\x0007\x0018\x000eCZ¸ë\x001e&\x001aF¶/gµ§£--À\x0012;wÜÌ\x0014y|w[ü <ªG­%§äQ§8\x001bxÐ<ô¹Ãâ4ª@®¦\x000b¤9ÕÙsGBk¢"\x000eF+:;vÅ	8a%q@\x0015Ó&\x001el/eÚy\x001b|YV÷g}ØÈ\x0013WG\x001bx=Y\x001b`\x0013\x0012\x0011d\x0018A9!\x0004P<ªÑ\x0006j-m áÉdÂ\x000fé}`J.\x001clÈòX?±¶v¶<6Pki\x0003\x0005\x0006­\x0006C4ÒÖÚÐ2{0MòÏñ\x000cnäÑk}\x001fÞóó	Rs
\x0012Þ$qÄÄÊÙâ4ZË5ÀÍ>{:È
*(Ñ\x0005\x001fä±åËay|#_K\x001egh«\x0006îL.×MÐ\x0002\x0013ëí\x00045Åly\x001au­ÖR×ÊxìÇM¿è\x0012w«ò¼[4hÑ;04(O£®ÕZêZYfëØ@3]v×ùÐ\x001e\x001eG7êZ¯¥®±²óz
é+T`}\x0010Ä\x0004áÚly\x001au­WS×Jï\x0013hM©VÆ±8Vÿ9¾¨n7½ó&¢\x0013lM1¼­À\x0018^F"}gUyX&ðÑëD>8\x0011óX\x0017®Y\x0017§ÊRI÷Ë)ÂÙò4ÚZ¯¦­Á·6ùó\x0008ïyÝÒ¼74?ÉÙÑvÓëh7l4D*\x000426 >\x0013Ç×MtæUGÅ1r3ë(7\x0010ÇJþ<à°ñ´<®0ËòÐ=­:\x001ai÷ýý§­h\x001b²RÀ\x001ds¯	\x0004¨Bbô\x0003TË\x0001·ë.#÷¥¶Ú\x001eå6é
Èñ/Ïw>ßÏ/#ÛÈ+\x001b4®æâ\x0016\ML¸\x000elÒ@¡ì_Þ¿y{ÑWJ6[mÓð­¶é·÷\x001fo\x001f¶nâ\x001c	qî\x0005\x001f'g9¥è{¿Òù\x0013\x0010äòìêÐêÍ"®\x0005ÐK\x0005ÀM2D+ÁöäÏ!\x001d5X!lgcÉ4~½]\x0010Ó© vñó/·>1/ÔÍóÝèÖE°²ºZò\x001aQ\x0011\x0002TNÔ,/^½>{óy¡nÞ\x001f«Yêí|®NùÜÅ2(\x000b]È«\x000b[º¼ü Ll\x0001\x0019\x0010â\x0016>Aó\x0012ÎðÀK¸|ü|\x000fBü|÷ð9ýþËÓÝÐeò`C\x000cu^é¨hÕ¨q~úãòúí\x0005ñêüêm\x001eû·×7çnT\x0011DÕ¨U\x0004Qvn "Íoë\x0010=?k1Ñ9O\x0010]\x000b¢W\x0011DH¢)\x000eZSß\x000eÎí2\x0013ò<9L-YG\x000e}\x001aHÏ\x001aÅ)óL ®ÅñAl-]E\x0010¹!7i\x00186	\x0012\x000c·»LÎ\x0013ÄÕ¸uaV~d¨\x0008\x00083µz51{=*ÝVZv[i}¼;yýøpûðy,·dË.2URÍZYV½r@Ëó××WgWo§ÄPµ\x0018j
1¼¤\x0012h,ÇµM-<«Þ8Q\x000c%®ÅÐkád$ÁµjyÕ\x00157OÉm³Ä0µ\x0018f\x00151,ïÑñÞ±ýP(\x0017À\x0010NP\x0000Ï\x0012ÃÖbØU.åKDFÎro\x001eIá&\x0006fIáj)Ü*/»Ú@
Ç¶\x0003/\x00151`\x0004»Åðµ\x0018~\x000514ÖõèJI¦º×Æðr\x0013\x0005ØYRZ°\x0014\x001e\x0007ï\x0018\x0001<\x0012G\x0001\x0013³\x0001;?Q\x0017%F¬Å«¡ËîDü.$á¨ÃÅ±í9b!lüÄ\x001ao\x0003ÂqOfC\x0006êBÃ\x0006oö«äDæ~D\x000e`ktY¦\x0018üõÇä=¼¿¿{\x0000gäñçïo?\x0006Q>üð_ÿñg}\x0018	O©-\x0006l;¯,·¼
/Úd÷ëËä]½¸8ÇyÑëW_½}\x000bb½9ùêäìë«)ét-^[:\x0003;\x001a1\x00047bÈýÒqéa©x¦\x0016Ï¬.\x0016E¼ÍV+êËxXKÅ³µxv}ñ\x000cÝM	\x0006Z¶¢àBP\x0013Ë>fK§¶ÙÜTA¸y|þ|Wh \x001fn»?¬
1s^L¤p¬¦Ì§\x001aº³r\x0011úæúÝÛóB\x0008}uöíy×°¶Ú\x001eèQ©¥EÉ0gisy3
{Ê»\x0010ÕYìMþÓ\x0004«&ÿTf=[S² h\x0004KE\x001d<Æ¼öÎÉQ¹e¢F´°®hÊÑ\x000eE-à©Ñú\x0007ghýóS­ñDSÍWS+5És?Z`\x00179m=R¤Ew\x0013KýÖêu\x0008:B1·}yW,&x;	f\x001aÁÌºi\x000eB4N<Ñ"F«h-)ø,\x0013tì3E\x0013rËã_Ê"\x0019\x0018°óïîï?\x000eÉâ<gÜ½\x0017¼\x0014l\x001a;¿n¢Sd99ÿòæüÝÅå\x0014x[·KÁ\x001b}j)BØ¬ò¬\x0016¼¸ÝNÒ\x000ew5x·\x0014¼´Ó&y\x0012´¨\x001a"ÎòèRô x_÷KÁk7l	$EÍ´ÂÚ"\x000b@\x0006o&ª\x0003àC
>,\x0004¯!XÍ\x000c;\x0002÷DP d,7Û#¡áà+«\x000fV,E4ÔùÞ@9^kºmXõÞÈVÝ,Ö7C\x001eáÁÿ¢£/
qwMðª\x0001¯\x0016p[¨Bl\ ðJð ±\x0013Í0àM\x0003Þ,\x0005¯T\x001es\x0002ð2p¶FB¼Ièí\x0004áï úFÓËeª^ÄHv ®"#¥#B_«xÖÞèy¹TÑC¤·8\x0001î8.rI¸eÆe\x0016ë¡WºQËÔ
N¥:&öðK\x001eÝôL7¬#k¢oÔZ¦nâÚ1#cKOD<N*Í³}}îu/úFß¨eú\x0006í	¸·¸B\x0014Õºgß(\x001cµLá §¢ÎåQ«tFðê(&:£\x0007Ñ7¯V-{µ\x00027
æu´\x0016¢ivòàÀ\x000c\x000cî\x0004ø úÆ=SËü3ìÛ4|ö©{ú69q\\x001f«ÞÆ?SË\x001c48{%ò:c\x001b±¤kU\x0012\x0000ÓgaÙzèucªôRS¥Îá!Ü\x001cd6\x0019}ä\x0001ÚÉãYÝAôÍÍÑKo\x000e\\x0012Þ5¦9Õ:£÷ÏÞ¹UÑÇ\x0006}\^ZÏôÂ rLR÷28jZÏ\x0011Ö¼ö¦1Vf©±B« L\x0013\x0007\x000cøW[¿N4k¶õ¥9 /g2\¡êTvêTóTg\x0007ÁÙVCæ\x001a+\x0012h$gFò4.
iÈóï¨zÜæÀã+\x0011Î-Ñ;T*yeìDâ\ªGc\x000e<¹"I&Piõ|z\x0004R[\x000e7(½\x000e÷üÝ3\x000e\x0003µ]ç[Ís¾{ÈûI(Ù\x0008uà+Í\x0013ªõÉµÞõÉ\x0007o^·Pª\x0011j{>[¨]õ\x0001¡L#Ô>¯}®PÉ'¡ps¸g\x000f¾0£L4xÌ\x0017Ê7B\x001dÐ{³J®qØã\x001a»y®qP[]Úº´KMâåíÃÃíP³EDy4¿)mRß\x0013Cè¥\x0004ñòìêêìpÇV[¶ ¶ì\x0005ÈM´Y§a×àÆr\®ÅÈ'6\x000eB×5t½ìÐµGjË²\x000f´tD;+\x0019úÄtÒ rS#7Ë£§C·ë¢
ÎMP\x0000
"\x000f5ò°øÌóìpÑpÚÒñ\x0006RLÖwõNè²¹érÙU·vÝØ
q\x000c7òZkVÅÞ\\x0018¹ðÆnä2\x0003\x000e\x001e0\x000f·½ZÜô´"öæÊÈw&Fa\x0017 ×AÅsD>O°\x0017zl ÇEÐÑ:ÅêÖ`réØ½å>Ý´¼v=ìªÑj¡z\x000czkP\x0005®!i9U\x001c&¨ö\x0007±7×]-¼î!|î
\x0014¤$\x0002.éøÜA\x0011­Ý5ØÝ²;£
ç
\x001c.;`:_\x001a/Õ.ôvkM`\x000fÛ\x000b¢BhËûÛ§\x001fF G­òzläZå\x0011\x001a\x0003§Î\x0013ª³±çòâêìæ«)äºF®!7hp
x\x0018ô	è»wEè¦n\x0016Bg\x001c®\x000bô@\x0001\x0018@ï\x000bÀz¡»\x001aº[\x0006Ý2\é\x0014Õ\x0014àqÒ6`>1\x001a3\x0008=ÔÐÃ2èa3Û\x001e»ÍÐµà«n'ØùÇ ×[\x0006BÛk8]ÂËÁ8=³-
Êè\x0019ÅóëÁõú\x0002}Ðe\x0003].\x000cwY±K,Äf6gc\x0004_ö«¼WÄÞ(G¹H;¢f§ \x000fÛ>\x0012p­y(/ö6\x0006öánô\¤`à®GdáËlæ\x0007öa¢Ø<\x0008½Ñ/rRS¢\x0017¯"z*cTT
Ø}Ý/Ã\x000eÊy\x001d!òÈe3c¬`\x0002\x0000¹.öF9ÊEÚ1;Ï
à|°ãsçc_Ó"U\x001e;"Ë{î\x0012H\x0007És\x0000¦¯6Ð]5z]-ÓëÒç3\x000c&4áÝæV¨ÞH©\x000f{£ØÕ2Å\x000e\x001eù©Ê·\x001d(µ BXJU&+B_\x000bb/öÖë]¦Ø¥s4p
/Õ;ãçÆu½q{Õ"¿WÊÈS½2é}>v^\x0003jÞ\x001fÄÞØ%µÌ.ÉHó: CÞÊ1ð;5«¾SÛ\x0000·Ëî:\x000e\x0018ùÂ¡Jg\x001ecd
ÕU7öT-³§xGrË$î¨#ú=cu¹é¡¯g²\x0017{cOÕ2{ªÀcWÚ\x0011Y\x0011	»T·bj¹ã öÆªeöT\x0005Yn\x000c\x0006Ö\x0004Ýñ±¯ë=ªÆ ªe\x0006\x0015£0X3qì\x000bÀXó1]7\x0006U/3¨àçU	¨d\x001cé\x001a\x0017\x001c\x001b%ÓéÃÞ\x0018T½Ì j§NÉó<\x0006m¼|eº\x0007vú ·¹eFI\x0007G±5¸4Ö\x0013\x001aouÅìëûéÅÞ\x0018%½Ì(\x0019Ð|0\x0015iÅøè8â\x0008kÚSÝ%½Ì,Q\x001fyvcØ,ùhøÔ§Ø\x0007\x0007¡7vI/³Kà óz$Ì\x0010|ê¡LQD?±pk\x0010{cô2»d.\x0011
y²Î\x0004»\x0019«ö«ÞÆ,éefÉx\x0007W	¾ä\x0005ÂÄ¸û\x0018pÓ(v³L±[å9¥\x00013`¥?Æ	.Aèr4Ë#\x0002)v\\x0001
´D%ØØß3½Ñ0fq6\x0012§EÂlEZ?\x0007zóJÍ²WêÀ\x0003\x0013\x0014ox£~	;NõMêísèÂnøÔ.OÐ4+\x00123y'\x000e¸:±³a\x0010{£bì2\x0015\x0013­$ÊbÌ\x0011ú¤Ù­	9CüªwÆ6®¯]æú"é¥äsDöoe*\x001að\x0005Ö¼3®ÑnHE±\x000b¤õËoÕªBf"Vudd¬\x0019{)?Y\x001f\x0008ïps$ze9\x0017Ù{_·D£Ô¶\x0008J-\x0015\x0001Saì	ëXÒ3i;c\Ç9\x0000»ÝVT¥i*ªNÞ>Ý}úôøy0'òRÓI\x0008Ì¨\x0018Å¦ÙgÀÑ¿9y{sþæÍõÛ#\x0014¼[ÅI\x0014À-\x0017@\x0012SpÎ¢þo)o¬ïk}\x001f\x0010À×\x0002øÅ\x0002`w»¡¥ÀÝÑ³æ·vbÝÈ¸\x0000¡\x0016 ,\x0016Àå\x000e\x0014§5/¯ÆQyØ\x001aÝXíG\x001fkôq1úþ|Æ\x001fÉvé\x0018¹«\x0013ÌØÊ÷¿ZÉeÚzå<\x0001,|\x0012NæÈ\x0004~gòí\x0004Sâ8úFýÈÅú'X<¿s$÷åüW~¾Õ\x000e1ÓÖ]gJ Uy¿"PH.4SòYÕÙÚÑ/m\x0004°Ë/\x0010§º\x0013\x000bUØOÀCöV÷Í
HÐ\x0000¹Ø\x0006\x0004kxÐ\x001eÙ¦(\x0007K×I\x0002ÑÙÂ×/Ac\x0003äb#üÒÜ·í\x0013nQù\x0006Ê¯¬Fe£Fåb=\x001a,í<Åg ¨ó\x0016¾áÎ[¹¶!ØÔeQº.;S>N·\x0008<	%¼µ\x0015\x000bÌ}aL¿\x0004²@.À\x001bÞ\x0006Ýy$Æàn\x0005~\x0007}#1\x0003\x00124æ@-7\x00078sÍ±õÂ1ì7ô
â\x0004Åß¸\x00049PÍ\x0001\x0006ÔÖj
\x000c\x0019ÜÛC\x0012¸µ\x001djÕØ\x0003µØ\x001eD\x0011yr!½|$ïû3ÞAc\x000fÔb{í^²æ
dFv(3µâj\Æ\x001e¨Åö *ÅÃF8Òàè\x0016Yn]4S+"Ç%h\x0002µ4*ÀÝ(´"\x0016$\x0000Ç.7\(¯ø\x0016ùN\x0006Án	tc\x000fôR{\x0000½áÎW\x000b\x0003å&¤ü;»ú%hì^l\x000f"X4REà!)êåØÀtÝõã7Í\x00170K¿ÂÞzb¥\x0008ÈÚ\x0003g45z!-ñÊºÔ4_À,ý\x0002 \x0001M\x0004y\x0018á\x00137Bâ±\x001fßÄfil©\x0012\x00194ÁGË\x00050´n
7¬ü\x0002LãO¥þÂ
.ÞÐ<m \x0012»ÛFlFZWÆ0Ký	 ä	HÝ¦¯3öºëÐ;i2-\x0000`ÿnkfÖ43³ßÞ¿ÿuDý k§á=@»zv±wÂçÛ\x0017ÿ2\x0005[Õ°Õ\x0012ØQ\x0010A,À\x000eÄj m\x0014Ìê.úØdú`ë\x001a¶^\x0002[\x0014\x001b¤¢\x000cm\x0002s,úÞ«Þ\x0005ÛÔ°Í\x0012Ø¥ã\x001eÿÀ	D\\x0018\x00196&BWmkØv\x0001lø'óh8ìÈC\x0010ðj(ÙÛÙZ6-¶ Ö\x000eYA\x001eÞÌez»¾{`»\x0006¶[\x0002Ûz*¨àÔiNsjé\x0004¯K2½Uº£¸õö´ÎÓvÏ¼îÅãÃçÛ\x0007wQ\x001a¡x
V¨iÚ0/³±a*ÁÿWÓ½¸¾z{öêÈ\x0016J\x0016A×"èå"hA\x0015^Lè`ÉgKÅ	8.­E°ËE0!Pä,'\x001b#mCÉrN¨Çq\x0011\-[á+¤­Y\x0004K¹rø
A\x0017\x0011&Âq\x0011|-_.WÌçj&º0m\x001d¯\x0006Ä
\x0015k\x0010j\x0011Â
"¸SÊþ´^J­}ª©BMSËð[a8(Äu\x000cÄP6~ÉÆÍq\x0011\x001a*kT«%¯A\x0002'éà)ü®qªÑg\\x0006ÓÈ`Vø\x000c®1´uÇöþ\x0013®Q£äredr½ ff/Mafv«F\x0017ÉåÊ\x00085\x0010yÌ&ê¼Ê[co3½\x0004¹¾\x0008¦é?É7)õ,Ä	n0\x0016=¼t\x0002sÍ@ ¾a0nËI ºzÒH\x0017õþñáñçû_dðFz6ÐMC¼LËN\x000e\x0010'ç Äõ«y7)©0k\x0008¡Ò2Ï\\x0005ãuê:DÉål9±\x0011z\x0010®\x0016Â­!ð,õº1[U
aSåÔq!|-_A\x0008\x0007fãc,«b5\x0015\x001b55Ó2.D¨\x0008k\x0008\x0011%\x0017UÁSåu\x001bí\x0004øÝ}¶º_ÊÝ\x0000\x0019jwc¾\x0010\x00101xRNú´´\x0011Sµíq)\x001aí$×POà]°z2Xñâ\x00103\x0011\x001aÀÚ­WmíæU:ùúñùiþ1\x0019/HcÇ(sî8*í\x001b®z>Å¯¯ßÝtmÐ±vëy[»yÞ¥Q\x0014ÒiD¤ôU,­Dq>LÜÍ&ÔÒµ¤ÑZa5ØsN\x0013x\x001f-IÓ¥¯©\x001e¼µÕ_*
\x0004¨\x0016dØ³4ä8?97*ØÞÑ't¼yyû4öâ!<¢\Yt§<\\³sNajÕQqª^Ý\x001c~ï[×¸õ\x0012ÜèÖÚ¬o±¯\x0015ùµSì\x0008C¸MÛ,Âí\x0012V>pUXf©ô~ª
m\x0008·­qÛe÷Äp\x0003 Vh\x0004)UfA\x0003êº\x0019\x0002îjàn\x0011p]Øã"n='£Æõm?YZ\x001aÂíkÜ~\x0011np(¨½#­\x0018¡À­ðú8µf\x0008x¨E7\x001cY\x0012é¦\x0008frÂ/3Lm±\x001bÂ\x001dkÜqÑ{[×@¯Sµ#l´Dw¾¥\x0003x½½Koe¼i6¸*²\x0014A
®M²Ü\x000c\x0001
p¹\x0008x0\x001caáÆ\x001aá»\x0002±ýÚP6Z\.Rã\x0018³H:rÅÍW\x0018³0abý\x0018BÞèq¹H{¤AÊÀ±\x001d-ÇÝAêÞ,J\x000fðFËe\x001cüÀz\x0007\x001fáÈ\x0003_ó0Õ©4¼Ñär*\x000f>oÍAbÄÈ\x0004¦Á¸Âé¸ê\x0003mT¹\¤Ë=6cÐmPð\x001cÕ9Zó7Ê\.Òæ\x001e3	d>}¤q©ÈÄ\x0004É#°U£\x0011Õ"Ófz¡N'äåyú)^!ä?®\x00169ä\x001e´In(B¯\x0011fF\x001e§\x001aj7º\-Òå\x001e\x001bIÈ
i_ó%/«rj¸e\x0008y£\x0012Õ"èÁô\x0004_9XBÔ\x001be¾â=×Ë¢\x0017¹,ÞÌh,Siã\x001f&è]3\x000cj\x0007bSÈÜÖ#5ºÔ\Ã°9P4d¹\x0016á')©ûð\x0007»\x0015î\x0007[û·¿<Ý\x000eÎ\x0001:ÖNÊòH7³\x0013jj\x0012q¿¾9;ÜcG°u
[/ûj¨Õ=X6ý%\x0014ÂéãõPÛ\x001aµ]\x001a«¶ÔÞî$Úèh"\x0016=õ`»\x001a¶[\x0002Û{îäÁé\x0014]æÌ¦§SF`û\x001a¶_tÚ«\x0016	KéjÒß«Ä{PÇ\x001au\Ú2S¦°F\x0014ÔºÌpL\x001b\x000c ®©ë$è\x001cØÆZªØ\x0008\x000e£dÿÊØ)Ì\x0011Ø²-\x0017Â¦\x000e/x¥ Ü|Ü\d#¸\x001b­-\x0017©m]R\x0013VºrÞðsÂ­;k]¸MÛ,Á-M)OH\x0003>:\x0004¦U7rÍón\x0014·\¤¹uäaa	\x0015®Òs' \Îdg\x000fîF\x0005Ê%:0¤ÞùÜ \x0011®.qøP]ÏàÈF\x0007ÊeJÐóD'\x00048\x001bì\x001c:`«F	ª%JÐÁ«äb©´4v¡½ç&3mz[kzp7ZP-Ó3ËxÜyO\x0003Üî Êy¯w»Uã\x0004ª%^ 1/øË
qà,
zVëÁnZ¢LR{\x0003)Ap\x0003©ÏÄnÚV¼Ü*QKT\x0003×\x001c\x00138Yb\x001bÐAón\x0006í¦öcàntZ¢K°#;öp;¸ç,>¥!°u5ÜºyzÉ£tÑó£Äå¶Üi¸ÞÔmX¶(.C^¥¬¸á>pæ$
Îk15À;»yzÑôãI
JÂà ØíÖZ­\x0017PêæQêEÒ	\x000eÍ@Ûq/\x0008X}¶8*®xOG©\x0017=Jð»#=J¡O©"\x0018E9îUÝ©ïn·\x001cªÛ%Q¥ÄAl+\x0005)ïh$÷¦uõÞôFð-m\x001bFñUj[Å\x001c\x0013ëõQ{6ò±«	j\x0002º\x0014)¡¶¦\x001f|Ájðùäõío÷\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=B^âÝõOÐC1\x000b\x0015m²­J{(ìf§\x000e?\x001cÎÐc$üõ÷««÷ x·~\x0003M\x00163ðSÔõ/b´YüQø×Âgÿd¿|ÉL(x?N7\x001fà!áúiµJ\x001f§±Ñ[Ë):Gå(ùk\x001b¹\x0016®âCÂúý¨Á¸ýÇ?7\x001f\x001eãý\x000bÒðãtóc|&ãµAõ>i(Á1<b×6(Å\x001aI=®¾OÆû©ÀkÃ\x0016*PjO]¢&*zc\x0010Ï8]£óÐÊ6¬¿úùï·\x0007,ØñÇéæ'¸©ÞßÍJ<À\x00082\x0019KzÏáF\x001dÀ<Ã|9L\x0014\x001aÞu§«7pO=?\x001b#»¹ùíçMÌ;hØb:n±ÏîgÒ	
	Ã\x0015ü\x0005%j\x0004ÆÎ,÷£}Åõ\x0016^ôÆ¯Ê\x0003o£R ÷òZá&\x0007e	ex´\x000f«¥øØ¶\x0005oñGÓbÝÚ ÂbEMö\x0018\x0011j%iµF\x001a÷`©ë»
Ñ;Ò1wôxôvs÷éaó´?M\x0013ì\x0004\x0007qÛh'\x000c3qB|%Â1-ÌdNá0~übõ~,Oóñ\x0017ùë_"\x001c¬\x0019üx{÷iFü\x0005æKÌB¸ïÄ0?/N× ð_7\x001cUèùõh\x0000v->þ\x0018ßÓ P&þëuÿ|{ûüp=gÁ¼a6¾á||ÚÆàMg¡°¡%;¿:=½ºX­\x0019\x00017¢6B°eÚaÿ\x0002¼âmÍ:oqí´`#6c\x0006á­þ}yW\x0010H\x000bÂ3\x00185çf$@Ë¦ã)¼£ \x0010\x0012Ó»|$t\x0006\x0003³Æ.E\x000fø?¾l8±Å«Ã#i*\x0008~ÒDiÊ\x0001¡\x001f±c{\x001cx\x0001¢¿o\x000c*Åtmñ|O\x0019FPf^pC?jäñg>S
ÔÚ\x0018Y­Îa\x001cQ\x0012×jØÜÏJÏ>ßØ×K9Êo\x000b
\x0012\x0007ð¯\x0006*æ¬´[Ê.o38ÜQê<÷Ì¦\x0002"Ú\x001fs^a¯½ÒPÖ^\x0007|Qc3ºó©À!¶?¨\x0002ÂÖj\x0015%Ml²êNæÄ \x001c\x000eçSAÚv\x0002g\x0016»ÓC4càÝ:®\x0015¶Eµâ~Ø\x001bÎ¤*\x001daÓj\x0005k	K\x001b[PSN^bxªä\x000bÜuûÏ_~c*³~óp;Ë/s-\x0019NLS0Ç¥,ªøèêÂ¥l8¦y·>¹8?\x001dwÉ\x0004%\x000cDµa)¥)fæ6V¤ÆYâ'tÞË±í>õüÓ?þþS\x000c¶ h-þxws7/ÿ&ØßªU¸0\x001a\x0019]\à\x0013\x001dÛª½ìB'à¶HP\x00154 qÚø\x001a< Á\x000bgÒ\x0010R°§íH?Þ<ÛÆU\x000b\x000füïb\x0003\x000fs¾_¸ÑPå\x0019K.-×NRé\x0019\x001b^*øãÅ
\x001e4Ç>á\x0016\x000e¤~ãF8\x0011.d\x001c3¼Î\x0000'\x0016ùqlìº¿\x0017îÓ\x001f?þ¶¥ð\x001cü×@¥ÿÅÍ\x001b\x001c
¸ÿ%Øqz¥6^a±å\x0006§\x0004¯>\x001cÕ¬ êÿâäõèÕ¿àý\x000f?Úù$ÌOx Ê¾Ð(Q\x0011"êËÆ\x000c¾\x001f¿<ýú\x001bV±§ÚõûçÏ»ëÛyC\x0008Åò[õx\x0015òà\x0015èYÈ\x000e\x001b´ó«py\\x001b\x0002\x000e|¥ípÜÓëPt\x0001ÑÚzjnà/G<S\x0013\x001c¸L¡Zá8è¤`áu\x0019
páæ!\x001d{éoËeÚ+Ç¡[\x001fkkc	r}¨øLå	àÝ`¥Ko\6\x0007mØ\x0000\x0003C¢qÙ\x0018Ão\x001a>nï7ýÍ|`\x000f?Åk\x000cÂËçßçÕ;Oq¬Ê`¶Â2äÕS]^ýÛÕèÅv\x0004\x001eñÇ|$Øó©OMÃüDãR
¼ÜXþdH|röÓ\x001f±\x001e\x0019àÇûûç»\x0019I0í½à¤ì©¢á&í(Ö\x0007	! à:ÏF\x0013`\x001f\x001eÿ\x0012`ðÕtL¯\x001eý°	«ôp3+O\x000e\x0005íx\x0014FÂî\x0002*\x001a£\x001fNÍ\x001dý°
kuq2ê\x00002\x001cÔ¤Ä\x001fpÑ¾R\x0002Ä^ÒiFfÝo÷ÃÝ]ÿý\x001f®¬=E¥àf¥¥Á\x001b9ÊÏi* tã× \x001f3Rv\x0016\x0005ßÌ\x0000KI60(R¸ËB\x000c©
ÕÒù\x0002¡\x0016°©h\x0004\x000b+/ï:*\x0003§:=*6á#e\x001d
X w\x0002ÿjãÒ0ÇYa\x001d´Gït+\x0011>g\x0006-E\x0003\x0019t	Èæ=¦AÙ\x000b7Äge£ébÉØXu6\x0016´xhÑü!ÃI´\x001ep\x001eäLâ}É`mf)XØ?ÚÈÞ>QZoEN:CU½-Ýd\x001c¬tüÑ&U©êg\x001d´¡ÇíÏ8å<\x001fËIÏGÖl1%e5¥µÅ\x0002Ú­!jñç\x0004\x001dø£qÍ¬ÌEÚVaK
8n<R½I6 Á©æ5\x0003
Jæßü9AÆ)¡¯-d
ÈÍ,èv*ÜhÁµc6Cç"5,E0#þhDó<£\x0005Kk¦
ñ\x000e£Ùd\x001aÈ}ôR\x0008Úå5m¨ÌW\x001a¾ø\x0010@qRüÑêÏcÜÐ8=jzË\x0002¡¾¥d0?ZÉ,õéhK/ó¬­T£\x000f³Ñ, ÙvË\x0011¶\x0017¢\x0019Noð:OÇÓ¥«&àú&Xûª	\x000bæ"ÆAãK§À0º`r·4>«ßNMk0\x000f{M6h²\x001d"ÛÑîÛi´û§O\x001fcë4\x001fÄ\x001fá&ð×ûçy¥ näáÿHÕ)KòaùFvÚêè¯çW\x0017£¥<KC`\x00104qq\x0018!ª$ái7b1+\x0004þAO\x0017×\x0010bÇ=$\x000c8(f¨ðÇ±\x000f1ÎÞÛÇP\x0016!ècÍ¹×\x000c¯vPc0ì
bëáÉÅ8\\x001cð(Ì\x0016N¿îõ¶\x001eÉ(3õ©Ú\x0001nè6÷V@o\x001coª32\x0013ÚÐ¶\x0012\x001aoP­O³\x0010¿¥GC\x001b\x0002]"4#\x0015§s	áõ\x001aò&Dí=(Í¦êSe@\x0012%.bð[\x0014+1Òw=\x0007ÑÅ=è¶î%üñå«ûç_î^mf5B	!°õ\x0001æ¿¤K¼c\x000eeÃ½^4î¾:¿úËùÕÑ«ÕXÎ* Æbp\x001c\x001a\x0018\x0011ýKø#!B¥ã¬·\x0010*¥çah¡!\x0003Ã©ÀßkóðIFF¨kÜ\x0003éU\x0005\x0019þØ\x000c	Âç:A²xiØå	Ãáê~F¡eÙt`¢.-ü1w@?\x001f\x001dß|¾~¸ç\x0002æÔc½DÒnOM\x0000T-ªGÞ©\x0001úêèøäíúýDþ\x001eÂBu+ýEÝ´}»I³*\x0004\x0002%¾N*«k\x001d7¹Àõª:a±¥p\x001f°*U/0·\x0012'´+i\x0004µ	/rFe¤}g6ð\x0010\x001b\x0016ÂM°uC\x001c"ÌüxôýóOÏ×w÷3êíÂ&öTG$L»Wi\x0013[áÐ\x001a_¦¾<úþêÍÕúì|´ò.ìd_hÙ¤¿(µ\x0007cAÙÍÝ¬,\x001c\x000eVyêÜZF\x0004\x001b¹¹ow2Ôí%¬üÆaU	«¾UX-v\x000cD¸ûî\x001a÷!Ú;úôÿã?×w_fd¥¡$YzìÓ\rjSõùe
$\x0001ö\x001f¼÷!\x0000<z}´>ûa4G\x0001[þ\x0002vñ/\x0000r(¨EÄ¬¡j®eî¤ñ{Î`ã/ \õ\x0005Ü\x0001>\x00061³ôº\x0003"pé\x0013\x0018·(7RÍÕû\x000bÈj\x000bÉCì¡ÿÞ_@ò\x0017Þ¿Î/ w,\x000e³Òâ$øð{\x0004þïïç]Ý3ÅÞI°Þ\x0007A)Ô¬v÷WH¿ÿà|ü.\x0001Sþ\x0002fù/`hÜ«r\x0012;ôÂ/ 5ý\x0002~äá®û\x0017på/àÿ\x0002\x001aóÎ ²
^\x0008*34|oØö\x000b\x0010Pú\x00058[þ\x001bp\x001aÇ©\x001c\x0008wàs¼§¤¾Q#GÝ¿AµøòMäÂÑÅ×_¯9öî{\x0010ÀßÀï9Æ­¿¨¾Xþ
ÂÕ\x000cÇ\x000c\x0007S¹\x001eb¬|©\x001b_Tøb9~pÅØç\x0011.óX\x0014\x0010nwôübåH\x0012µû7¨ì¨XnH\x0014eÒQ'ÏàK8\x0019ÒðÛ\x000c?ºµþ\x0006\x001fâ8B\x000fn#0æ\x001a*Ô×wG.\E.?ÍÉ\x0000^ï!\x0017^ï\x001d¼lr¼JûQå£ðñï^ïÃ45¦iÇ `'\x0013¦eX0\x000bY'Y	1*?2\x001fÓÖ¶\x001dSÁ¨¸\x0005
ÿ\x000c\x00010\x001d=í¬ù\x0002È\x001cL\x001b¶)\x001e\x0017.ùÊ'ÌëÀù
:[gu{Io°0ªpÊÔíåHl\x001d:Õ& ®/.Â_¾fÖñTÂÕ¬ÂÕ¬\x000f7|b4nð\x0016\x0005£\x0000×Â\x0008TþèGR¤m¸U¸uâ"MòèZxz"5×TJäõHð|ÚTÅÉr/á\x0005-$ÓfÒ:RÑÐGÖ´àÔeGê#·´QÛOkkZûMÒÂ\x001dm'e\x0002¶¨p\x0007\x00174\x0016`ÿóV$\x0006¤áåÒb1}î³\x0019)\x0004,\x0006\x0003LóO´ó\x0019Ò\x0006wê±\x0003_ÖO:¼eª\x0004T\x001d\x001e\x001b744Ü\x0013_\x0016ó#ÚÅ³ùtÉ§;>°ÇöõØª°úG	\x0001GT8æ\x0002Ú\x0012Ð¶\x0003ÂË%Vh6\x0013Ê$\x0015´(-Í\x0006t% ë\x0000$£®4ÎE@kéqzLf6 /\x0001}\x0007 ¢L¸6:7[N5\x0007#EsùxuyÇ!¶¤Ç¬´cIÅ\x0007>±ÊÏÔËÎ\x0008¯Î\x0008ï8$Æ¾À¦0kI\x0012&\x0018\x000c¸p\x0001MÅgÚù\x0014Gµ\x0007·'\x0000jï³#¯é³ñª\x0013Ì;p°1"!\x0010 "\x001b=Rã>\x001b¯:\x001e¼ã|hIý\x0001:\x0004øRdd®.1\x000b	K289ÖN(³H`°ÑXþbX> #wÊÙ|U :¢\x0004åIæ\x0014JHQKÆÐË4#&³\x0001ë(¡ÃÂ\x0008ÍÞ«l\x0001a4\x0008.àHÕÕlÀ*J\x0010\x001daà/P);\x0014qÚS4(ýHÁÚlÀÊÄ\x000e\x0013Ã=\x001d\x0012#X\x0016d\x0000\x0012\x0008·Ì&¬Ü°èðÃ\eµQ!sµS\x0008Gê\x0012æ\x0012Êê\x0018Ëc\x001c\x0002}]¼"l¦
;Ê±K?¢Ó:°:È²ã 35<q\x001f2¬é´Lµg\x000b	«,;N2Ë×\x0006æFÓ\x001a­Qcuô³	eE(;\x0008©\x00053\x0014OÒÊÖç2* 7°26²ÝØÈÁ³h"$õK6Òy?\x001b°·d{¼\x0005i\x001dÒç\x000cGY¡\x001aÉ~L\x001ap.ae\x000ee»9µÏèQ h\x0010Ë²q|9¬áÒ£\\x0005]²=è*	aø'Â¼
G\x0014Óf\x0013V\x0006[¶\x001bì\x0010¶SÆbK\x0018+Ý8[xLª¸P¶Ç±×dsMNYçÀÚHÏ%TCQí\x000eE:ª\x0002a	E½WYC/¼\x001b«Ê¡¨v\x0002²}äP`\x000c	¶¯Qf>	@³	+¢Ú\x001dJøp(rXCG±«ôè§øÂ¬*¢Ú\x001d¾\x000f\BM0aÆÐ\x0012¼lï\x0005äÕøÈô\x0017¥0é»ÍóíÑÛû»Y\x0015\x0004Ìzñ"\x0016\x0017< D\x0012NÏ¿ZÙi=Éw««Ó£·çgã¥\x0003Ä+J^ÑË\x000bøà\x000eÃ\x0012ÓºZG·>=6À«W¼²W`&1\x0004ØÓbáIÖw¤{ªW¼j\x0001o^\ÔÑ	´<¯î¡v.iu7­\x0010Y$ XU¬
w:\x000f¼\x0012#\x0015ÃíÀ¦\x00046ÝÀÜæík\x0015
\x001d\x0008c\x0006\x001e¹µ\x0003Û\x0012Øv\x0003c\x0016×Bù0î\x0007I\x0005Ú$i;­+i]7m\x001a}\x0010µÂ¬.ÈSy\x0018S§n\x0007ö%°ï\x0006Æ\x0004 Ì§J%©Øós\x0010ÚmÑMt\x0016ì@ë+í×ë{(âÚ½uû·°Yqs ¦\x000c\x0008\x0014×dâÇÛvâÊÁñ~\x000f\x0007ÿ\x0014\x001eÚ\x0010|q\x0005\x001d:åF\x0006g´\x0013W.÷û\x000cªC3!$\x00195Oé\x0007ð%\x0007\x0002®0ï·Â6ðp\x0013ÈQl«dÂY\x0011Q\x0017aó\x0013\x000c ÂÁû\x0015Bê³Ct\x001b'/Gy#ì¢ú\x0018QFX½IäïÓ\x0008á1L\x00039¿ó
îØÑ\x0005eÌóçëY ÜXÕØq(f¬?r¹\x0010UÄòüj3ÍR[Î`à/ßnn¿\?þqt{=«\x0013
µ\x000cO\x0011\x000eq\x0002ÞmQ\x000eµÃÇ\x001f\x000eÌß®NX_þõ\x0008¦N4C!©¬Ie\x0017i¸¥\x00176í¤¢§Æ:\x0014ôëãrTg+ÔðÇVTP\x0008³:\x000fÔ\x0004ûÚ\x0008sTÒ£G\x0006jÎEeRrÛ\x0005\x0017~søc:«\x000b\x000b½¶w¬Ù5\x001a\x0012|©GLF)X'[Í\x0010Ö×°¾\x000bÖ3Mm\x000eÐDíâ\x0005"\x001c5KÅGcÝm°9©`!«Ñ³²åJ)Èë[Ü°FfØáp¼\x0011×°¼\x000f\x0016Ú]\x0013«ÔLHvÓÂº\x0007öFVQ³.Vc9õ\x0018c0;\x001dX\x001dÂJ>RÞ9\x001b6VIñmw¤'E\x001e\x001b°Aa~O6\ÌR[Ìò40±5«±<fê%ÂÎ=íÙ	Úú
\x001aÊÕ;¡ÃF@M\x001d©9{FÛ\x0008M\x0012¤JH¶0k³S\x0016o,G{wýéúöóf^½'\x00081¬ÿ\x0000F$\x0015³b\x0008êHvéÝúõúôíjºØÓ¤¹S[\x0017fØKøc`|xøcfA*ÒÎ$ÿ Ôhf­"YcG\x0005]/.þ:OÕ|ªO3Î¿tÊ½@ºð7&N1\x0003/öÊ­E~p\x0019õpÿx¸m	zu³f6\x0008hÔLs ½§7\x0015éRéÏ®ÿzqþ\x001ev$\x0008×éÖ!ª0¾D?v¡\x0006\x001b¨FlÇK­X5\x001bU;\x0003\x000b/h;µÁaøñíæãõÑÛÍÃõÝO÷s@£A"µhKÃ¿]~\x0013#¶ôÝéêx}ôvu±>{s¾Rª\x0012´LQ
G'cd]À¤Ú±T\\x0013¥))M\x0017%§QnZç×\x0016»}\x001c\x001fQ\x0013j¢t%¥ë¡4\x00000\x0012å^,½KªÊø\x0016È¢­	^zY\x000f¥Î¸Pñ§ñ\x001bÒÀj$¹ÒÄY\x001d\x001fÞu~´Ê:M05aj\x000b\x0013GÚ60«óÃ»\x000eÒY\x0014\x001e*<Se¥+=ùiâ¬N\x0010ï:Bb{Ð]®±"×
}jâ¬Î\x0010ï:Dÿ\x001d¢:F¢ë\x0018q\x0007~ÊÚ\x001crnõÆfLÌÀüÀl=ì6~³!ö
qóaswt¶y~¥IÎ¬·ôN- \x0013\x001cS©01b27b.N^­ÎÎVW\x0017£¢äPÌ±ë+õË$­ýt
^=¬çoÏ×ó\x0014\x0002¸\x00154}YjKS;D\x0016àác*¾\x00170Ä\x0000üzXÔ»ZOé\x0019èúÉ
på7kJ\Ó\x000bI=I\x0002"qdk\x000cèÉ-D+Ã|3­-ií7¿¸®Äu¸ WÌhLÆäiI
zR#­©Í¸¾Äõ½¸áíðR*êù½Ë¯¸±Ê0 \x0008z\x00070÷0"m\x0007Gµ²ä;ìb[ymµy½íàe6Ä+\x0012Gàë©MF\x0017¦5Ñ\x001dW¼o\x0002vÕöýV}ÖAç\x0005\x0005ï$Ni\x0002\x001a©Äi\x0004å%Ø^¦zw\x0004\x000b¡\x0001n\x0008)k'EÞ\x0010j¤.§·PC¼YÇ¿\x0003XGÁ¶tæd\x001a\\x00027lÜè¨Æ#÷·\x000f7»Ç\x000eþªs=ÍnPÇ®4\x0012eÈÂ:Èµûä¿mj¯¼éÜÉÂ¡\x0000]ô\x001cxëV$Ñ©\x0018Ð¸3þöé«½ñ©\x0013Ú\x0018ZeèYÄ+&,/F^5\x001aw\x001b>eløÜÒÞ<\ÿzóû\x001cZ%5U\x0008\x0003­¥¹£2Ë½¨\x000eoqO.ÖïÎOþ}\x001f®(qE/®Ê¢\x0011JS0àfå)5ÄlÆ%®ìÅ\x0015ö\x0005Ê\x0003Ç\x0004v£äÅ~¡I«JZÕ½\x0017dÞ¹a©ûSû #·µf\]âê\x0005K~NùÜ/ÊÈ1ÕÝwÒfâ\x0012×tãjJ{Á¸y\x000b\x0000j¯$S8">ÖkK\Û«hNF°¾4ö\x0001rà´º#½\x0003Í¸®Äu½¸ÄLô6ëº;juà~ä¶\x0019×¸¾{uÙ\x000bî³f%j¯l\x0005ôFÒL­°eÑÅ\x000cc\x001fm\x0008Ð0û
JÓ\x0012UÖ-´àcÓ\ykÖíÔ¸Í^"\x0018	¬,Ñ´yÄØlÇfÞÊKðn7\x0001¯ôxÖ`ø\x0017ò:KÓ`Çªûy+ÃË»-/Çr'¨»,þx\x00183Æ+3Æ»í\x0018s(¿\x0011µ*\x0005ÑrZ[¶7XÉ[\x0019\x0006Þm\x0019Bé ÀK]yæcíP­°¢:h¢÷ Aû\x0016ªß¥ñ\x000bnBcâ&Í¼ÕÆ\x0015Ý\x001b÷¿+Â\x0011Õf\x0010Ýá¿\x0017JÞ+ÞþÝ+·76FÖbä\x0005¿=&+ï\x0010mz=± )p\x001bÔYå]¶½KÍæ;×5\x0010Ì/Ö÷ýýóíýóã¼\x000e!É¡+¶\x0008Á¼\x0018¼\x0010S*U
xÎ´ïÏ¯NÏ¯.'ÄæøÎm-Ð^ZíI³Ç¸AÓH\x001bÚ
£Õ1Í¸²Ä¸Â1(¸Îcbì
K´zÏY\x000b«JXõÍ¯­.qu\x001f.s G\x00030\x0019*[XÏH;ÇÐÔApMkºWWæÆiíPnÎi¶Î°/W6\x0017×¸®Û,¸Ü\x001eký]ðÔ¤,\x000f´\x0019\x000b\x0005X1ÖÍk0/b \x001aÀ!®¥¾t©ß[q+3Æ»íÜvßZF>bÛÚ*ía,\x0003¯,\x0003ï6
 \x001díÌÂsixÕÀp3ouÖxïaá"\x0012û^=§Æ\EsFáÝ2Ë[\x001d6Þ{Ú`î\x001e¶\x00071\x0012÷\x000c~ÞY^Q\x001d6Ñ{ØàµBaçJ¸h¢*tÙS4·7ãÖ1Cïa\x0013ð)±ÑFÓî&wAT\x00017ãV1è\x000c\x001aþû\x001c¨è5\x000eg\x001dEKÅ"1ÁfÖÊ0^ÃÀ=
RV)ÊãHN¦4\x001bé%mæ­\x000cè5\x000cÜqÊ;ÅVG\x000eY³Ã8
YY\x0006Ùk\x0019x\x0008\x001c×8l\x0014qÂäÎø}9Óy¸ÂÛjy½ívl´³¬Ã\x0016<§L\x001eñ®ö¥¤g_'Ëe¼Plú=\x0005f¥gP©®â2½¯d/1\x0013;·K¸ºõ}¾#~V\x001f7\x001fofõcÿLi\x0008Ê°.CPÝ8¼¬îÕ:\x000e÷Y\x001d¯OFû±2©,Ie\x0017)ó"kÕê,kÄ\x001d¥Ï¥°#i§6T]¢ê>Tå¨ûYÛ`yÅ©Â´ªnÄ=´¡Ú\x0012Õv¢2õÚ	T(úücïÀm¾äô}\¸öT\x001cÃÕ,±\x001eK6nÔªø"nÖXzÑA\x001cÖÓ¢j¢ÎÊ¹UyTóX\x000ez.±Ù5\x0002&\x001b8îïq^í\x0002¨'âE\x0007f¿¡½2º\x0019s`\x0000\x001a'þ]N\x0014. ¦(1E\x0007¦ô\x001aUZaü\x001f\x0016X\x0018\x0012\x0014\x0010c"M²]k©h-¬¥Á\x0004÷æk©KLÝÉ³,tüäôV¦2åÄ¹KiKJÛE©¨\x001c(IÍQ$(´\x001f\x0004[0}é{0¡Òp×ÊÚÖæÚ4Ì,J.wN9,ÃÖ¾z¾y|¼¿»»5Ïè\x001a/.ÊÀèìÄ*\x0004ËÑÔHO\x0006\x0019¥WW'çggëq~,Jd±\x0000ÙQ{ñê\x0005\x0012sêo\x0002ãz(bY\x0012Ënb¦³%(\x000ecP\x0015lC\x000cw\x0007[dU"«~d£InÈ\x0008NoN\geÐ1×\x001dÄ¦$6ýÄ:1ê\x001aÃ¶ ,FdÅ;]ìú-	eÛKÞ\x0016Y¨]^\x0014-O³³º÷Íö\x0002J\x001cî\x000bUwGd¨:k\x0013×oã`ø3	âÃ/ÑwîÛÔc\x0005xíÌãýF\x000eL\x0006­sp'X¾Í³Ô£´{"ñ\x0006æÊdð\x00056\x0003ô\x0014qafùC²ÛfìÛÊ,|u\x0002áýfCÓåÜ2MÙ\x000fîi\x0006\x0019¼«-Ö»>[>ûøçÍíL\ir-@\x001c±\x000fÁéàþh_Ìß%ÜãïW§3PUªúP5î_Î¨ÝGóìòÜXz¼Ó¦Seõa0\x000fTnÃòôóÏ&Ý½ïðò¾\x0013@®7Ïs@µÍ÷2Í·m¾.÷Ï´c\\x00198ß¯WWû8eÉ)»8µ¤lÚÚ[ú
^Ø±\x\x0013§.9u\x001f§É\x0005\x0014r5îfndq\x001b¨-Am\x0017¨\x0011ùÃ³\x0010(\x0018\x0004uyªÐXyÊ<P½« U±C_ß|º~~8úáæÓævÖýÇ{*^3ÑÂ8Oíèvìå1á¾>?~¿\x000eûÃÉëÕé>hUB«\x0005Ðpô1\x0018c.êÆj1Ç`5B\x0012Ú,f
\x0016º\x0014rY8}"\x0007ÖÆÌ«æ\x000bVZBU
BÛ<cLkA"z\x0013\x000el.³Ø½$ê¼þx;cn[ì]RÁ©ÕÄP\x00159Í4&sLÞa}|~:5¶m÷j,ª«q\x000bhÖÓñE8Ên{b´¾\x0016Ï\x0003U%¨ê\x0001U f+j-I\x001bGB¶ÂU´\x0012Ôt}jmN0Z\x001aôEO!Âìy_\x0007êJP×\x0007*)\x0011ê\x0004£MT\x000e8"\x0005ÛDYÜ\x001fE}lùð¦V)[âÛ&\x0019Çº¶H«\x001dÊû¶h0«\x0002\x000305U\x001eIï5\x001b³Ú¼o»Á\x000fïy\x0013¥rÃ]¶A¹ß½µx2¢ëÏ7·×GÇ÷Ï\x000f3\x001d\x0015Èmã\x0003\x0018ôæN\x0017:K~¬?= ®ß®Ï¯.&,>Â\x0012VtÂ*\x0012à\x000f\x0000êë5"K¤¹±\x0016­FVY²ÊNVni
\x0012Ìs¤)Hùú
ä\x000f\x0002«KXÝ\x000b«èòª9@Cþ>ÃN$[`m	k{a9)@hnò8\x0010'ò¨ÑÇ\x0016XWÂºÞóås9\
©E©<Ös"ÃÜ\x0002ëKXß	Ë\x000c$\x0004\x0006!£<Ñ¶¿E²	Õ\x0000[&=}vZ=¦\x000bÛ²4/L\x0017)H6V\x001fÓH[ÛÙ^CËr~(\x0004Ôy¼Íy\x00176¦SÑH[\x0019ZÞkiÃ^Eã\x0015âlæ«\x001d%^ØÈ,ÚVÖÊÐòNK\x000b­MxAÔRÓûVÔå$ùÈhßVÚÊÒòNS\x000b´ä\x0017\x0002-Ã·\ÇÁ\x000fã\x0016xeiy§©\x0005J\YhwÓ$}01Q\x001dÓ\x0002[\x0019/Þi½@®\x0006\x001bÎ5È#-ÏU\x001c#s¬\x001aaE\x001dÉt\x001e0éÙ\x000b)y5¢´&+Çæp´ÒVGLô\x001e±ðõ)Ï¥sif:Ï~HÅ¶ÐªVõ\x001e1\x000eÉ´¶\x0006¥tÃ\x0011£VN½ó·ÐV\x0006Aô\x001a\x0004EºÊ
ÔñA)ÜÉ²ø"\x001b¿Ö´ÐÖtÒ\x000b"=ÙiÃZé²Ið¡­/Ñ\x0019}I+ò@k-H8PË,ezC&«xFvÆ3Òè<\x0001^Û\"ò @9Q?ÑB[\x00190ÙkÀ\x000cÏ\x0017G\x0013\x0007x%kë³¹=È\x0019E½\x0016A«¼´a\x0015uãÑ!ÁÃ,muÆdï\x0019\x0003_2§ÆçWc\x00045¢wÙ¼¶U	eZ_ª¡ìv\x0004ÕÈÐ\x0007Ú½êoO×\x000f;Ðð7}Ð\x0006óhË`îXÎãÕÒP»ùnE©ï\x001e6w\x001fïo\x001e7ÿË¬a\x0014áÀ«J#9@ìB&Öø»ÕÙñùÉåÑñêí\x0007\x0016%°è\x0006¶2·	:w %MÂMÜ~Ûe	,ûWØÃ¼(ájÝ¶f¬×­\x0019XÀª=¥\x001aãÌ\x000b\x001c8\x0016ÿ;\x0013ð¡v.yu7/LJ¥¾hEr.W5òê6^Sò~^OZ®&\*\x0018N÷\x000bÿ\x0004|(^[òÚ~^\x0001]\x000c×Ðs,7kò	ßÑ\x0006ìJ`×\x000bì¥ÒXBVÖIºZ(9ÖÿØ\x000cìK`ß½ÂSÚ)Îp¡ùª&7sfo\x0006.ßvTNu,±Y¢\x001c¡¸-gèÈh#®ý\¿£óY§ÄXEF\x001c§[\x0013ñZ\x001bqåèx·§\x000b\x0017¶\äªhR:K£ÞMv¨%®\x001c\x001dïöt0uF»;ÙÓ`=2ð¨Tc3qåéx·«sáR¤iþ2ËÛ8KÁH?2;­¸òu¼ÛÙ9&)Écr\x0001\x001b\x0008Â©P&xåíx·»sáÂm,ÁØ.´#Ó?Ú+Ç»\x001d2ïà?4c64YÉ\x001ce\x001bqåðx¿Çs¦l:0Ø¾í9Ô\x0013É´6âÊãñnçÞê8C\x000cÆMd1éÍÄ¢ry¢ßå5F\x0018\x001dþ\x0011g¥%[¡'jYÚ+'º]\x0013,WÁ®ÀÀMçÚ«1y£fàúj×íñ<t\x0019PN8ÖñÇ%Þ&\x0002\x000f\x0015·Êã~§\x000b\x0017­hôµg9\x000cb\x0013ý6âÊãnçÎ9\x0015é^xl¥e2|¢8£¸òx¢ßã©8\x00190Y(ù,ÝÊ^\x001d¸òx¢Ûãù°°F)
ç½Ï9\x0015è_;\x000cqåñD¿Ç\x00037G\x0015ü°!\x0012ñ6OlÇTæ+'º=×Û7Oæq0§c¹\x000eÎÙñ\x0007Ú6àÊá~\x0017.vØ(
y+²m<»\x000f7QbÒD,+÷!ûÝËÅ\x0010ÐDó¯e\x000eÛ\x000e[§Ùúm±÷YwÁáÀ1ë5Ëj\x0006\x0013\x0005\x0006mÀaÝÍo\x0015¡uÚ\x001cx[\x001as¨»¬¬ì¶\x0012`×ÐJ@;pd×(µ-Æ¦\x00105\x0013WNv\x001f:¯8	\\x0004{£\x000eÒ°Å\x0004|¨=¡ª3§ºÏ\x000f±0f·µä¤4Æä¶\j¢\x0004½¸:vªûØyË¨ÒW<ë)|Aºz°^6âêÜ©þsg|V\x0013ááê¡8ë¿úC%UuðTÿÁ39\x0003«%ÆB¯àróÒD\x001fE\x001bquðTÿÁÓ^Áw46ÄÝT£h':\x0014\x001a«\x0011?ðÀXÿ\x0005ÏFa!òwéù9xh*±v¢Tq.³Ý}»³e¯ÊëÙÂ\x0008LPg\x001ak¸wãÞ×
ðf=ÙÅ ¢\x0004\x0015] ÒSã\x001d\x0008b¡v\x000fì\x000bp\x0018`Ø\x0004ªJPÕ\x0005
8\x0018\x0003{ºß\x0007PJúè=²Mó8MÉiú8-
©¼ FÌèt'À<PWº>ÐÜ\x001ah¹%©x¡ó«ð¾óA}	êû@sá\x0015N	J)72D¹³|y±UWÍ·\x0006ZyÞyès\x00065\x0018M\x0018\x0018å²>ÅMZ\x001dzÞwêÃu\x0017W4Ä8+B°üdá÷´ÕÌ\x0001õ©?v­)§\x0011t \x0002ÕBn\x0005÷ôÒÍB­·©ìÜ§ è¾ÉP\x0008þ3.ÿúó´Ï\x0006 Mz£ªÒ¢XP³±¹<M¨¢Fí;S ,ÒÁ§â 4aDÞª{´\x000bæ¡Ê\x001aUv¡\x001a\x0003\x001e´\x0001P¸"Ä|98Ù#\x000e2\x000fUÕ¨}ç\x001fÞq\x0003\x0008O=¿b«$ä&2_sPý®Û÷äö¿ß<?Í\x0016#çxU\x000e6A,çÍC\x0011Ã5vñûÕÕûq-Q±Ûé#r§Ï|<¡iÞ\x000e\x0014É£b²4KNiUÌÀe\x0014
µ°âÛ\x0001|'L¼\x000cÿ²yøts7O\x0004\x001ekh\x0010}íñ#,¤ &+°\x0011ÿ²ºx}r61ì;¡Ê\x0012Uv¡
c³'bÄX\x0015¹\x0004o¢-¢\x0001U¨ªoUÃE\x000e¿¼õTAªôVMO«AÍ$Õ%©îüþ\x000eCñ3öK\x0006£D5ûrnÜLTS¢¾ï\x001f®GtcM¶GÛ¨LÊ+TÞÉ\x001aöªÆ\x0014èìô´W³6Ñ\x001eÍÃ¬®bu}¬aØ\x0004u¨Ú¯8=Í)¶G\x0006l\x001ejñ\x001e.y~\x000foFUx® 4	U õ/Å÷\êg¢ÖvµÏ°
\x001fKÒû¡$=f%}Ö
ô\x000bYws:2çtÞn?\C	Ù^»mD¹Sëz$P4|»ºzµ>Þ\x0007(J@Ñ\x000e(@\x0016#\x0001æ¬©Y9k¢ju\x001e,ùd3Èª¶[JXár3ìDcÎ<@U\x0002ªoo\x0001uÉ§{\x0016\x0014ýx\x001e½`·S¬ýØpÝÙ¦\x00044Í0lÃe@Ôn³Lå¼ý\x0007hK@Û¾²\x001e:ÄE(Ù&¶}ù\x0013nóø\Éçù$_\x0008G\x0004û«7[M¹_¸È\x001eÈmk>!¼\x0015xR¸ðY6ÆS-ÿäcÒ<ÂÚL·Ûi8\x001a¸LÐ¬\x001aË²PsãWÛy\x001däíÇ9$_\x0013\x0011V·[\x001aF\x001bê§SeA&ZSçÑU·b`¥õ£²°\x0007³$_êHÊ¹±6×P¶\x0012'M
ãy\x0016ØQ\x000bc\x0005Q\x0012Ñ|JT¸!p²4hfÍd¢¥l\x001e^uDDó\x0011\x0001\x0005HL¥\x000e©þ8¹Õ¦Yh\x0008EuDDó\x0011\x0001=2]\x001d&Ðuù\x000bO¨\x0018Ï\x0003¬Nh>% >FmÐÜÑ³¿±Ygy*q:°:%¢ý@\x001b[\x0016Áû´19é3£\x0019ÍT­®1¢¡N×a+÷\x0019þÑpò!²\x0007S±°_±BéóíýóíÌ\x0011\x0007Ðëïâ<ö'¬|5q\x0013ýù¯¯Þ_NÌ8@LUbª\x001eÌ\x0010T´¯çÐÁd\x0004a)µä¹ºÄÔ\x001dQI\x0002÷%ÔÊä(v¢n6¦)1MÏj/Í¶½×<Ëwe		\x0005¹E¸\x00180ó[SÛW÷4ÌY{\x0001+¾ºÌ_}¢Öv6guxÏ!r;ÊkJB+aïhªY!Þs@ä%yVë\x0012$x#\x000e±7Ee7£QÊSÚìÎ³A\x000b²¤Ý\x000f¼Tt\x000b[J\x0003DXR\x0006hµ4þApº\?fVu\x0008\x001bº»²ªseÿÜCÅùNÂsJ½Û<ß\x001e½ºÿ4SC»·ÎÎ\x0013ëâl®Zgã»õÝêêôèÕùëý²Ä}F\x0019i\x0011Å\x0012fãa\x0013i>¨.Au\x001f(Ëý7\x0001í \x00186ñ\x0018:\x001fÔ ¶\x000bû<\x000ePrìÐ\x000bQ¦
Ê'j f
¶³C!i^¾¾ù|ýü0/
ÕT§§\x0015ÃÎ\x0010ò,Ê5¡(\x0018I_¼]_]ìC%ªìC5ö\x0005ÝÌU~*ÙáN¶_5 ª\x0012Uu®ê6Ç¡\x0005é\x001a<ÃLN5s7 ê\x0012Uw¯ªyU1±oôVðnGjJRÓ¹¨"+×\x0004ÃªaFgñË©\x0006T[¢Ú>T-hbNìDÀ\x000c\x0014[]«=j\x001eª+Q]ç÷×Yä\x000eô²óc£­Û8}Ééû8SeIBõäKM\x000e¦äDùÁ|Ò²¼l\x001bñ7}±4\x000cËÀò2£ò}TM<>6 ÖÖ¿Óü+\x0013aRu"¿êOdê\x001aPE*:Qm¶©á²B\x0011êVlë Zù)Þé¨äö¦oô\x000bt©!z!Òê²\x0006ÔÊOñNG\x0015\x0016P¡Q\x0006mª0ÛaÀ0ÿ¼rT¼ÓSI^±Ò(XwÀA\x0015¯\\x0015ïôUJäs\x0015b\x0001\x000c\x0000
Ï\x0001(n`­\x001c\x0000ïô\x0000Ò@X³Ò©áB@=1u¬µr\x0002¼Ó\x000bðm\x000cè\x0018jÎJs^×þ³ù¬¢r\x0003¢Ó
K@.Còt¶´g\x0014\x0004	)\x0006ÖÊ\x000fN?À\x0005ØÔ Ö¬Y`>Ä+0¯¢r\x0004¢Ó\x00110EÐ½É©?ks3øD¥B\x0003kå
D+Þ½P*g*\x0014JD<ÉÉLw5°V¾@tú\x0002&³Í©Y¨\x001ckó~µ\x0013]|
¬/\x0010}¾@z©½Éê¦a\x0013\x001cv\x000fT¾@ôù\x0002`Å¾=`%Ùëb»\x001e´ºµ¾kt&g,\x0019ä\x0013i®n°û²\x0016óP+G ú\x001c\x000cÖ\x001fõ\x0015\x000cSÙ\x0008äñö\x0010·\x0001YVÙgZÃªe`¹rj=ç\x001c?{i¦UzªÖ6·\x0018n²\x001b(\x0011j`­³A¦5\x0000Zìgh²\x0006í+ªò>HÅª¤uº\x0015RÖº9*ôÙs\x0019\x000f])ÚÎâ6ê0\x0019,¹,»ÿÒfØt\x0013C>\x000b=®¶E>¶hFi".\x001f^"1=¼4\x0013G#J\x0016a\x001fj\x0008\x0011rjcbFé\x001cbµ;;Kù²©ûâþñ\x0006`æÔ*+\x0018IÃzjÌNæÛÁÁM7\_À÷ \x0012Uô¡
	Å[©
YÐ´pG¤&?3-l@%ªìDÍuõÖS»T*ë í\x0019c>T¤ªçÁÆ	\x001aí$¥Üª;N×ªÏDÕ%ªîCe\x001czPS\x000b£~%)8mU¾göLTS¢.T¾U\x0006
:û%ÏM¾S\x000f\x001b
¨¶Dµ}¨ÁºâV
7q\x0014¬\x0011.WU¹	Õ¥\x0006RWº>R+èQÓÀ´\x0019$¥¨+\"§{fúÔ÷*ø8E¥jBÞödNc>jYÌâ«\x0006ÿ¦ïÏ¨!ü+k&Ø'ðrºam&kå\x0000x\x0007\x0008ÿY\x000efCxPö u5\x0013ïïsX¥Ùñ« (P/77wOGo7O?ß\Ï\x001a«­@iÊ\x0001å\x000b|09Îª³»\½?z»zÿýÉz|°¶Ü\x001dý\x001ehE/-¼k ¬Éó©U¾Ò°V&ZYÒÊ^Z¥¶e\x0003òñyl²ä\x0013\x0017&Z]Òê^Úp\x0007Eí¦;X®\x001dè1hÂ5%®éÞ¸"7HB¹åS'Èr6áÚ\x0012×v¯îvø«Ü\x0006ÛÌæÍ0kÂõ%®ïÅãEÁÃ.N¸9''&÷[pËÎ\x0018½CÇòn[Â©£÷ÄíuQ\x001dfuymt»­®à¹¤@I\x001aW½-Ó\x0010Ùº¼2º¼Ûêó·¯Xª{Á?\x0013\x0013Ã p+«Ë»Í.\x0003V\x0019\x0017ûá´ÛÊ1NÜkx+»Ë»
o¸&â\x0011îá9Ð6WÂÈfü&ÞÊðònË\x001bâ\x0004·ôÁæ! \x0013×Æ&ÜÊðònËË¶\x0004æ0ô¼Ëw&ä¾x]ÅëºWl\x000bN$¤pÓòê,xp¨õ­<\x0005ïu\x0015Òü<®=¥ê´¹æh¢¯®WT®Bt»
fIx\x000f@Òô4»}Î\x00179n¢ò\x0015¢×WH¿\x001d±iby\x0017¾ãdÞ\x0003áÖ\x0011z·³`l[Ù³_j¶¸¹P\x0014O«ºWWRCÙV]&ìã\2XlÂ­l¯èµ½Òm§+ZW4¦Ã¦\x000fµ¼1\x0013½Æ\x000cºz¨7\x001dT<¨«'¿M©O7ñVÆLtÇ½Üeùtp\x0016j'rN|"{×Â++c&{´\x0012£Ú	éÚÞ¨Lj¢­lìµ
Òæt céI2K=ê¤&ÞÊ8Ènã\x0000o:6grh&wPh\x000e\x0013¦ËÊ6ÈnÛ`\x0014¤DÒ{?Ë³L·ù\x00063Ñ_Üv¯;<MñjÖ$qyD\x000f\x0014	ª¯¥EæË ?+6<åÛ+¸sÃ\x001f_&ÖÕÝ§9ri \x0002A9Â0)ù\x000bÇ´¡\x0017¾p!\x001aöÄ	suöúbL0-C\x001aR4C
-Hb\x0010\x001aêbôè`VHnï\x001déOl´5¤m_I¯¿ ¨#£Ñ$(
£\x0015û\x0019}dd[Fÿ\x0012þßý×ÿ¹½ù}ÖJìu4­"Ê^'JO\x00166\x0016S~·>=ù÷qJ\x0007Æl)ÝË(º(¿þpýð4çøÀl¹è¯Âö¤ø\x0005v"Bz=òN ¿¿zµ¾x?JéàÉY-¥â¹Ly¹yþ2ï­Y\x0008áa8|àÔK
}¿ã'á\x0014¼5$ÎËÕÕ\x000fã/Í\x0001TÇåt[Pý\x0012þøòòúá\x0001\x0012øGï®ÿx¸zÿ|÷Ç¼ç1C$\x0002>:+lútag
?:^®/. ôný×ó÷ðOïÏ¯Îþº\x0007ß²
ß²eø\x0002ZVcè\x0015n4Ú@Cørì!²\x0013ß
ßøÞÑÃ+J±?òÒLïyñ\x0005y­pf\x0002èÃÑ§ÿû\x001fÿ¹¾ûr3KN3Ðá$\x001bÍÂÖ1é(J\x001a´âÆr\x0001ïâèõÑúìq³º¤Ô=^	x0T#ÄpªÑø:626ª\x0001³°¾ cÃº8¥ÅV&\x001dü\x0001ª+\x0004NÑ;Ï2Nï\x0013þØ\x0001ê\x0007ãôÙ\x0005¦\x001b£Þp'FÞMæJnªÝ	©»fPÁd{uR¤ø%ÎBÄÐ@ûè»\x0001Ô
\x0014F\x0003t|zÐñI	\ç²³êA\x001c\x0011\x001f\x0003ÊYtj.÷ð\x0017/á/ÿ×ê\x0008&Úo\x001e>Ýßmæp\x001aãérk 3<\x0005ÜÎç9´Ãß=üïaö«×çg«iL§xDLøc;¦
\x001bÔàwç\x0006Æèà«)~öa«ÔB¹\x0008#%DÍpÁÒ$ã-IÆÛzê²T~¤~n?(ûÛ?¥»åOøj\x000eoåÇ7O×G·£wÇ§°?¯\x0003ÒKÐ¼O ?ýÕó§ëð¿ÖÂ`5¦gËpº\x0015\x0008\x0004Jn\x0005ê_tjñ½_\x001f­®^¯_\x001e¼_\x001f®Þ­.as®ÃöòæîãýÝÝóuþ¯!Ã±\x0011} k\x0002a?:\x0008%V|ýXê9/#\x000cçEv\x0012\x0014\x0004,¥àÝ6B*M¦Lo/\x000cö\õAB\x001f-Bj\x0007·¾\x0008©QÉY1[eaÓèNH7¤å L\x0011!
¾\x001b)VIø.\x000cöÖôA\x001a!~t´¾L°.\x000c¿­íDyÅ\x0000é\x001dñFHåómÉðËºNF\x000f%0:³IIUPxx(È`h}çÔé\x0007Eð±Ã7\x001b|[Q¼ê]\x0004	Q%ü«k)mJ¢\x0003¥LK)4QÊCíIÈ\x0008ñN\x0003©])\x0005\x001eo§L¦<Ô\x0007íÍ;\x001dóù§\x0011lÒ;¢ä\x0007ûàÁßð>c\x0018®#Ó\x0010	\x0001¡ã\x0013¡;ÔéfhÞçq\x000cg©\x00183Q\x0006\x0019)óäeÈ»\x000c2x\x001bÞçq`I\x0002\x0014 \x0015ÔDHi¶\x000c¿-ïó8P\x001fyÃJä\x001d)\x000evºÃ¯Ëû\\x000e(sÅ\x001b êëi)i%«\x0001ÙË ÃoËû|\x000eÔZÇ;88o\x0006ÍÚ	2A^\x001f*ä\x00053Áû\x000eìJ\x001f<XöL/\x0008!\x000e:9¢\x0003Ñçt\x000cói<\x001dP:x\x0006K\x0007Ì\x0010sêPk	¥\x0006¢Ïé\x0004KQF¤4¥ÉÚl\x0010NÇ£r\x0000\x001c\x001e\x0010ÍGG\x001dÊ/Bî\t^s,j\x0011\x0003"!Ðyã¨¯\x0000©\x000fåt k%:¯9\x0006%á\x0006Á@'\x0005Bùþp(Ä°³Eç%Ç°|lÂMahNÓ½à&¦\x000eE\x0019üè¼åh\x001e1\x0003%£ó\x0018÷Z¢Ô\x0007óÐb-z¯9:¥X ?`A\x001d*­eÎ`¨]\x0018ÁÅÎ\x000e½»\x0001¥Ì×Z³\x0018êp2Ø2ÑétÌQ\x0006st\x001dsÜ¡<Xp\x000eµ!²ó¢\x0003v\x0012w¥c¾·2æðÛÊ^Ã¨&P²íJR¼Æ4[æ¾>º¯ËäßÏ×oîà5ê»ûç»Çç§ðïwO·çØZ;\x001bÌ\x0010}xî-^xD8àÉýHé\x0007>ü÷ë·'gð\x0014õÝùÕÙåÕûðïgïOWW\x0017'ë9Ü\x000f\Â\x001d"vJÄ\x0008\x001bu¿\x00137nX	Q\x0007Ç4á²\x0005wIq9,¸´`\x001a\x00128ÖÆ&Ðscæp\x00197\x0007=¸àáJB\x001bE¡R´T¼¬;>\x00148f\x0013\x0017í\x0014.^¤
Î 'Ï\x00137
\ Å}xnL0.ZðÔ\x0019\x001c7"Í\x0011\*:
Ä\KÁ1é¸hÁ¢èiWÜaJ\ÁøRpÌD.[qìt\x000c+Ú±Ò\x0016ç¸U¤fMÁìä¢\x0015W,Î@ÆG\x0017	Ø\x001c\x001b\x0002¤8¼\x0001ÏÉÊe\x0016ÜCAj:
Sé\x0019×¥p?9¹lµ9Æð\x0006Ò\x0008>¯7soþ%§æ2S£<\x0006*°\x0006ma*[
KnÝ@NÎEäFá\x0015Ùx\x0008ûeZsèuIk^ÍD?\x00149å?­¹§ø¥a\x000bÉ\x001a2ò?Â\x000cÄKÉ))ºlÍÉ\x001c\x001a/\x001c¾~\x0008hàÀ5Wn »2¥\x000c¹æxQ"W²>Þã\jXò?aSòtÙsÌý\x0019çcXZr+Îr\x0018\x000bÁs\x0012pYth²A\x0014î\x0010´Q\x0006óªK±)ß¶Ô\x0007Å\x001a·@.õ\x000bA.¬ÊÁMù­e!VFÆmâ\x0013·ÇqB°O\x000emS8cÑé³ån_BOh\x000c²\x0018Ï>È=Lý\x0019Ña,ñ\x000f\x0011"üÛb~Ñ­ãH\x0012Æÿ\x0013â-¦\x0013¾^oCD.Ñ6*\x0003]\x0015\x0011aÕ¿\x0014úOØóÌÿm\x0003QîfáÒk\x000f\x0012É®\x001bÚö<ÜàÈ®»?Ý¦µ·\x0007Ø: àpí\x0019´\x000c¤c«)RWþO¸B+X{µtí­eI~1\ÿÇ"\x0003\x0011\x0007ÞF\x001czv^\x001c¥µçê\x0000ÏQî\x0016n¥f\x0007ð\x0014\x0014¡w¥ÏañùâÏ<ÕoqÍà\x000c$ãr*àOÄ`Ì\x0010l\x000fÿy#\x000eì|9;ºY+B\x001céÐÍj:¯ªR\x0013:Xê(íys\x0000[ïlR\x0011	Û&Äò\x0018À3E®Êü\x0019©Æ4ö\x000b}-49î\x0005Y\x001co·ÁâxK\x0016GµnÍÃÇë_wÙï>¨ûÅ´§÷O7×¯ïN7\x001fî?n\x001enöäý9Üs!^Ot\x0006\x0012Õ\x000bÉ\x0000\m7{zþþäòrýv}öþètõêüêx\x0015@G¹@M)ô^Tý"E0 î'R
l²Ò\x001f4åÌ{I-\x0005[\x0002.Ï\x001cQ)\x0007\x001aNà×Ï¥ý¨)MÞÊ\x000c½û@DúøØ,\x0003\x001dKäLYñÞ%EH%òzòl«6¤Å)\x000bÞÉ)\x0018~i±d\x00192TVtà}§4¥½{I\x001dÖ_Â§K»$\x0005å:P\x001cÑ\x0012Ý¨ÒP\x0005Tàù\x0011Uáct@\x001dxBíGM©íNÔ¤â\x0006uoa}\x0005n¿¾ãv£RF»w\x0007hªê\x0000iWUÊl¦\x0006^<úY1ÝË*±23ZÿT?\x001aX¹ÉÖÿ¦¿½¬\x0008xeÈ§
ìù\x000cG\x001dõ³bº·×®:zæPjF^UÑº\x001auHÓê£nv8^ðoý'Li<aÐ¶\x0007LÒ\x00013\x0005q¡qá\x0002`
­ô»Äbù\x0012ß|Ø|xú{\x0011
®¾\ß¥ÁªÇ÷?oî>mùú§û\x001fÜ\x0017ÀJv¥£f@\x0018òÐÊ¢_8jþëí»úa}Æ«\x001e¿}»:{½\x0002ðõóï¾\x0003âÂEÐ,ÉÍ%[æSò\\XÁÔÁ¡SÜµ\x0004TªÁPx*\x0005#Y\x001e½¿¶¿\x000bSl³YxN%ÓÜr°ÉYR&N\x001a÷µ!^\x0008b%Ð'ÑôDnp¡¹£Öüë»Ã2hrÍK¨Ãúb-
s¶\m¶r B[HïµK¨Ã­¨!ÄLE·ÒæûûaVúGÿû?äciñî>Þ\ßÝ]\x001f]Ü??E½ïn¯\x001fþØo£yäå\x000cÚh¢y6¹|\x000f¤ÆWgÇ'ë³³õÑÅùÕû(tðÝéúêâ¯spÓÍò_\x00067ÝÚþUpá\x0019@ó¼¿}b\x001býóHòæûÍóST;?Þ<ßAíæãÞâMëBV,¥ÎI\x000fÊÖ±xS0?}?ú~uõ>\x001f¯®Î ór\x000eú×É\x000et(\x0017S	]zpá	]bu¬\x0003#ËÑ¿Îîô #7säF\x0019pyÓ÷>î¯S==»E'!a@ª\x001eç$ô?cÅ¿NþtÃ+\x00026\x0011\x001a\x0003ç4\x0016)cr%\­\x0007Ê½;ÉW~þø©8¡'Ý\x0004ò\x0008üæúaswóüy\x000f0\x000fwÞüàÃRËcQ
%Åì×ääí»U\x0000oÖ\x0017«³«·³8Óqìã´2IAÃ¦'JÍ
Uû»ÎnÐtø:\x0017Ô'a5Ð-pp\x000f\x000bJCê\x00066º9ÓaëâdZ°­\x0007Ý\x0002PÚÌÄÀ\x0015ª3\x001d­>NÇé\x000ejÕtzÛ
%L\x0001yÏ\x000e\x0008&á<²ÎuÅa9Ð¦ ÑÓ6\x001c\x001d(=ÐVÚÊ{sï\x001c<QG·ÿ÷?þsõüáú×»\x0019J%d¬¬r¹7Å
ªý3z \x0012Þ¢\x001e¿yµ~wr6~ë/Pw÷ê7® ÿ\x0012¨éâùí¢>ýóÃ5ûG\x0019GÃôvssûóýí>oj\x001c¤\x001c"_U|zPcNa\x0015Yp	\x0003.üãÛÕÉé÷ç§ã'(SèéËøãÛâÒðp\x00124p\x00052%`:Ø\x0014ò1g¨|[7 ²P}Ü|Ú<>=|\x0005ænÿò©\x0012Fº½Ë7(ömn÷:Eè³Hw\x0016\x001876Ñ¢\ \x001dp6Ç§çpá\x0006}¾Õéè\x0015dØýÔFF\x0005\x0016&¶b/2Tð§õ@æ³\x000cÛÚÈBdf	´BdÆðpj3TÝ\x001dLMh!Î¥'yé\x0019½%\x001fG­?zàñx&üýò»ò&\x0011öÿ«î6{·_\x0019à)\x0010=\x0017$}ÛÌ(9ðª\x0011þñÕÉ³U¹ûé\x001f\x0010ù'þY»þ
Ì%%ë°»Â¢¥òzî\x0005#AY£\x001cûÏ\x0000ÂM?\x001b('n³\x0012Ã)\x000e]é6;ÔÚ\x0002{}.\x0004¾N@!$5xMU2\x0003n¨]¥\x0005\x0008wøüË'O¢	îÍÙ\x000c4P\x000c¹\x0017èÉ~¿øhÚ\x0015v@º¾ãv·×¬çç\x000ec \x0004\x0016É¬cºRx®\x0006öÐú\x0014\x000eÚÙ\x001c\x001eÎáÇ\\x001eî¨ÛÅ\x0018/S\x001b\x0000sNâ-\x0017\x0014
\x0007Î\x0003\x0001 Ó\x0002¤Óp:i<+¨j[\x000cîãq÷îó?\x0007ÞBãÓÍÑóÓõÓÓ¾ØÊàNR\x0000ÝÕ:!y\x001a\x0018vÖPAÀêèM@z³~ÿ~=ÊõÓ¯\x001foøãí\x0006Z¨÷ml.\x001d\x0015+¨PNæQà4| {ãí
º¦çÀ8qsa@ùÖ¥k²ÔöEz\x000cã*µÔ_/Ïl\x0016Ï\x0002\x000büÉ\x0012B\x0012Dù¶)ÁÇ"\x0016=PH¹åWÿù×ÐX¸X\x0001³9z{¿Û8+
¥\x000ffø\x0002 ¥WBðÿ\x0003ûæíùÔÙâPwÇl\x001e\x001f\x0000¥ðXÁ¬u\x0014 ñP·\x0001\x0007\x0015?fãÄ¹bq\x000bkz¨fÖPL\x0004*Ðí87ÏòAYW¹ïooög{·ºXü,\x0005>õ+©ráùØMàüêôdÜY\x0014DXê5\x0008ú\x000f9\x0012xÊP¨·LØ¡ò®ýDüá§ç\x001fÿ\x001e\x000f:øSÙåæÃíýó>ê@fT'Ó\x0003\x0001HªÍÊ©YøÇËÕ«Óó«YX\x0006°L\x000bçBS\x0015¤\x0011\x001eÉ 
*ÚrCu\x000eÕ\x0006ªuS´þb\x0015çÖÉe
¹Þ<]o÷±*è`KßÕ\x0005ÃÚ{¢ò"o\x0007^µËÔ2\x0005àÇß¯Þ¯WWûáE	/ÁKO\x0017\x0006è°â)\x000c6Î	(\x001c\x0016^ðr\x0019|p
¨~\x0004&IX\x001bC\x0005sÞ\x0003Ã«\x0012^-×\x0006S\x0015áò¯ql Â/7ýÒÌ®Kv½xáyºÏ95a
i:I? ×¶Ýìf\x0019;LtN¦Å¦!;Ýæ´µÐÓ/AÍð¶·ËàCÄ*0çÎ9(Gø\x001cPó|à]ãJx·\x0008^\x0007,,î\x001aAJ£ÆS3Ì\x0012;\x0008üÝçO?êçâ}ãò·çÍÃõÑ_®7wG	çýïýñ¶Ø1\x0010þ[°TI(Oõ3\x000f¼Ñ^þÛÕêb}ôõêìè/\x0010^bÿEüIK\ÿø÷\x0012ñ]óq~ÅÈiâ°\x00010=½9|H|ðBLý"ñMó²(9ÅÆ4V·¹´3+[
^cA¾öt%tS\x001dF³ooøg\x0013©V-¥T\x0014¨é\ïé:\x0006c¾BiV{>ü+\x0005³Í\ÞÇ`awrC\x000f.÷ó}\x001dcïçúõç_~\x0012EÊ
\x000b¸.o>ßß]\x001fýp}³ïælX1oÀád§ªefiâ©bb ï['oÏÏÖG?¬ON§áªÉ\x00168\x0013µþ£Ù	w[p}ù@\x000e¢­*lasôw\x001cÔ\x0019&6\x0018÷pC¯ü­pU	dÓÂ	èA#¸"
\x000bÇ·p£u±sávJ\x001dö¦Sê\x0002¨Bº`Sòóóâ¥Û)ilZ;G·s§)4
kçÈ×9þµin¥Ãêý\x000e:É¨¦Õ{»çËØ^Y\x0006î¢­t(kÒA'rÃ¾.ÁIMKg\x0006"ãV8TîY:;C\x0004áTa`NßR8TRîó|»ë\x001cÖ\x000c1ÇI§	\x0004nÒxJÏwUÔ5\x0006Z>¬ò9þ\x001b­IMÊÉ\x001dtÚ¿Ø^Ç(fr`í\x0016{	Êðu°È\x0019_i¡1¹DÇE¦\x0013w\x001dI%÷¬|Ápé@I\x0015S>\x001f¡²×F8i3>·*Úpyâ¸t,/d_ç³[é0WÚ±tÊG\x0002á\x000c©\x001fùÛ\+\x001bj"w°ñ,û\x0012ìpÞtº5<\x001f\x0010Jm¥C-äã¨q	FÏ¢-Ñ,\x0018ßoC	ä\x001eK#ú\x0002Ãß¥£c\x0003^ZáPù¸Ï¡Ú>\\x00185´x1p½i¤#Éãój-\x0016uÛø\x0000\¡W\x0016§\x0007$@[áPê¸gé$Uø[\x0018îGBå]Ç\x0007:I[éÂï'»¼2á\x0014X\x0018FKÝÐz+\x001cÜ\ûpt\x000b\x0003a\x001dK'=¥ÝØN+]øýdÐ\x000c\Cz\x0006¡Ökf\x0014e\x0012Ë×.XaÙe¡ð\x0001Ý¿q.\x0013ÆÐeÂI±88Qð2ÛwbM\x001c<Þj¨N$l;\x001fk{1hfT}B±\x0017I©/Ð\x0019ÐCt:R\x001d\x001foîM\x0007©¾}\x0007¶\x0018é´ÀÛ\x0011t`ÕZÙÂÚ«®ØÄ$¥×È\x0006Ý¸ë\x001cé_¹!iÆV:x\x001bì;\x0013:W8¦\x0018t\x001aEY|;¤qÝ
\x0007U\x001c]Á	´É¤J¥°éòíßÐ¨·ØjµÎC)EßõdÚ\x001eXC·D;$^9î\x0003sTþâ\x0015d²xâ>Ý|ÙÜ}Ú_íåÃy°\x000504ºH\x0008ERTÿºw[ÒäÆñ<_%^`Â\x0008iu\x0015¥Î²Ì6u°Ý+Y¨*»:ÍTRw\x001eÚvïæ5æn/gö5êMæIø\x001c_Ð¿pÂ}dj³²T¨Zú\x0005\x0004@\x0010ø£Ô\x0000õV¢øõÃ\x000f\x000foÿt£MG`m\x000bku°Ø¸j¥\x0017Ôp°\x000cëF/
Ö·°^\x0007\x001b¥\x0011¢\x0004ôý­ü¶ÂqçÀ\x00166(`±©Òss~Î\x0014\x0005¬\x000b<Î*U°±ºM\x0005\x0015fxeI~Ì&V­+;=\x00056µ°I·²K%®¬,?s|öÊæ\x00166ë`Ï°*x\x0019¾Å§\x001bÊé3¨¥E-:T\Ì¼öoQã\x001eXÊ4jàÒÀ2\x0004YY££\x0005\x001eÿP+-\x000b\x0002á°\x001e
mï\x00134N\x0001«º\x0002GsÅ°T\x0007uq\x000f½%¥;CÛ9\x0005Ðx\x0005´] '\x000c7-.._,éÞÿ\x000c¬ë`\x000e\x0016g¶íJFCb
*×tÑ\x0000K
mçÂ@ãÃðÉT1\ZntÀD!¯í
¥Ç\x0019ÚÎÎ]Ä,ø½%Këa\iã
aÇ\x0019ÚÎ/Î1@tÜß/kKà\x0015pÞ\x001d9±[RÛ3°_\x0000cà¨N#;Ã¾H%ÒI{¶ó\x000b s\x000cÖ°\x0008eÆ fñ\x000b!È\x0001K\x001cÃ<ìE°¼ó\x000bFç\x0019PÓr"8\x000c!\x0012/+<zãoÎhx·Z×\x0017®x¾Áe~Ô¼\x0014ÃÐVHâ\x001bò-½æÝ¼èÉ~|¼òe:g\x0016yNF\x000e¥	«3ã
\x0007Mª
\x0001?þë%þW­ÿµ+òR\x0004_%³\x0007\º=ü\x0004Ù(×Ô^ö\x0003\x001c%&O£¨ªpìR!ÕdWµRûÃ]¸Ï\`éè\x0001¡»A^­â±8ç\x0011;ê¯
¡Ýu!ôÏï©Ä¯ÿðáï¿<\x0001ÊÎKW]J\x001ca5\x0019È´L§W÷ªüêßþáÕWo÷ü
¶ý\x0015ìá_\x0001ÖÆÀX8|7öò8\x0014ôô_Áµ¿;þ\x0015\x0002©\x0006f\x0014iH<®	\x0012A¸qôWðí¯à\x000fÿ
Xe,±T\x0004²DÏè*~Ðþ
áð¯\x0010i$O\x0006$Ðg\x0001\x001d.¿\x0001¤ó?BlxÆG¸ü
\x0016Xá\x0003'ý
vÔDsðWHí¯\x001f\x0005`(<Í4ªÄõ0¿rû\x001bäÃ¿A\x0015mi&LW­¿Í3ªÀ_¡´¿B9c\x001f±P\x0015±`\x000cÓe\x001fÿ\x001b4Î~k\x0019Ößù/\x0002ùÊAã}©ÿ\x0014ß|yÿ×{\x000e\x001aßçH¦Ý×8Þ.]YªÄC\x0019\[êo¾ùâ_\x0007µ-¨ÕÀUÄ~qÂD\x0017\x0017\x0012\N\x0001u-¨S­¨c\x001dS\x000fí¯+ÊUB\x001eDg
Pßúß\x001f(&ç»=zy
m\x0014÷õ\x0004àkyF¦¯W{G_>A¿\x001f+>«(¶Å´\x001aLÃ3\x0001\x0015\x0011¶§T¸w¡Þ$¶õk÷cº\x0016ÓÍcFã¹J%\x0014 ê^ÈÀÏ{7Ô÷Cú\x0016Ò+?ùdªçÚ@ÚOî\x0007
6ó¡Å\x000cµ\x0004Ë\x0002Üõ°°Ìr¶Q0·Ë\x0007'0c\x00195«i±\x0019ì\x000c\x0005	
\x0017t';x,ÇL-fR¬¦µ\³\x001fRa¡ìXÝ>¹AïÝ<fn1³æ£ûR¾9rwÊ\x0001*-dÑ¬¥tn\x0007É×CJôdoiïÆ7¦Å´\x001bÍb{Æ\x000cëbÍ\x001c¨ÚÌSö\x000eHá"ª;Ð9\x0011ë.!Èjn\x00171Mpv\x001e\x0008\x0014.(\x0002\x000bÕå\x0004ê\x001aÎ,\x0012çü\x0004G	\x0007\x0002\x000bJÕl.97_j7 x\x001ed\x0015G#\x0017ç1;\x001f\x0004
'\x0014q2H¦¯ÎOµõ\x000cQº
G\x0006q:'\x0004
/õÄËE<ùlè«£obù¬pÆWï\x0010(¼P¬×\x000b*@
Ñ­ËÉYËdÍ\x0019\x0017\x0002\x001bJëÀ\x0007\x0001g\Ö3\x0014YÏÞÎ<gç@ãÜêÕë%M|à\x0019[	¶\x001bð&8;O\x0004
W°TKä\x0016í\x0017ÔOãÓ\x000e\x000cû4¦í<Õx"\x001cFºpIÙ(\x0007®gLÉ:ó'²
O]$«[C`Ú	rØGÓç9û»Æ\x0013¹ByòºdëròÝ2Á l³sEVã°vÄµ¬ÈþÖ\x000f8ý1(pçì|Õø"oñç²(]º,gdedÎðì¶sEVãrÝ´8J|YMÇ\x001d\x0010aTá6Ù¹"«qE^T>B\x0005ãx.\x0019YÎØó<ggâ­ÆÄcN.Kû1çE&>3\íL¼UxÔ×¡j\\x0017\x001c%\x0011­á.\x0011Å»ÎÂ;¯f2\x000154i5³c\x0015²rFRÁu6Þ)l|0)<vÝ§§!ÃÍ¦Án\x0017¯O`v&ÞiL<*[EZÎK½Õ²Üb\x001fo´ØOpöù.Çw}ª¸tõ\x0010Ñ3\x0015\x0004\x0016½\x001dÉ'Îcv\x0016Þi,|½XRl°E½s±ìÙó¶JÆ\x0004ggâÂÄcA\x001dMarõØ{zqbÑEØn6 ì,¼ÓXxÔ\x0014¦øÃr{J]Í\x0014x5·{¢'8»ËS\6r\x0016\x001fWïGÆ÷/Ù®Fóg¬gçÆ\x0013¥(wað2MÇäü¨Fq³óDNãêEÔ!\x001c$\x001e\x0008ÒHèGÏYÓ¾óE^ãj DÌú1isYOàæ®ºO¸oøÎ\x0017y/BUe2ÀBà¹ÚÓFcÏcv¾Èk|Ñ:Ù=\x0018·.gfÜx÷/ò\x001a_\x0003·X¬¨¦'âÈ"M7t$&0û×\x0017/*KÓ/rõ,\x001bb\x0018T\x0015Ìsv¾ÈkÞ_P±35ã´'Ä8\x00180ÏÙy#¯ñFEnÃ¾°^\x001c\x0014	<OyÀô3ò
gTc{K»3\x0006.´'LÁ¬¦yÌÎ\x0017y/Jõ;úêøêF	:9ð\x000cg$\x0012}ç¼Â\x0017\x0015WXoÇúÈõ Ï/¥¼1CçÂ\x0015¡\x001a§ôqÊ÷ó\x\x001eý\x0019\x0019¥Ðy¢ ðD5\x0004á0¾: ¬´C{3Ðçì\QP¸"ÌÆSÿ¬¯!½t<]ßâ1¥û1;O\x0014¦=\x0011ÖÜ&¾n\x0000æhv´ã\x0006Z\x001cw}\x0002gçÂ\x0015UÎÙc¼\x0015c/ï\x001beOÜ¹ô"o1öU\x0000Ónh©{_¶f,\x0010IhÓ;Î!ÛéXÊÎ\x000b\x0005\x0017JÑð]Ã×Mºd½¬1Yr\x0003aÞyÎÎ¾\x0007}¯¾5_ô­\x0001î|\x00089°5cg8£ÆpÖØºN=ÚPN\x001dsåÜ)WÌØ\x0019¤¨1HEÕ\
?©³è2®cáÛzC\x0013ÝI^\x001c/§K®ì¶Æ\x000b¼{ª?nôØ\x0017Ò(\x0010ÿS»H=.\x001c!Ä2ýÁ¤Ý\x0011#4éÕ8F*a-0M{ÆóKêPR\x001c¡ìE\x001cÎUdq\x001a1s:É\x0010|¤î\x000c%Å\x0019ÊÁñ3³À9Dk%K3ÇìPR\x001c¡ßh9»í\x0014Û³4ÙÀ³-\x0014\x0016\x0019ó~ ó<Í»í\x0015Û³`ðAk%-ÿ"NlÛ?ÎÙmÏ¬Ø\x0005Ç«,\x001dLÙÅ¹*\x0014Ì¥3ÞÝr·?³b¹
Ûéõ>º;Å\x000fåÎÆçi\x001b¿t×Ñõ\x0012BÆF»¥»Îó ö0q4ÏÙ!j\x000eQ\x0007\x0003Àú\x000fúèâvaÐB4ÍYºCT¦\x000f\x0011v:\x001aÀ*\x0003ÊÏ\x0013§;#­PºCT¦\x000fÑoõÝKwÊô!ú­8}Û¯ÊinüÉï3G\x0017ì5n½»ÿ~qËÕ-ÕK93²V'Bj87ÇPäxBÍß¼r¥øy/å8x¶FF¬ãd\x0002Îàñæ,mÖmÜâ\x000c'Áí2.ì\x000b\Üï°³ãV'çLE\x001bVoåþê×\x000c\x0000Éo¶O\x001c³ðä\x0005Õ¾\x0005ãI\x0003ï2¡¾EïS&\x0003õ\x0008Åó×µ\x0005Õâæ\x001c¹\x001e_ÁHf¬0 Ï`'ÄÕ\x0015÷ê Õæ åtºtÁ5\x0013=àùêó`¥¢Òözuë¿S³º8ok\x001a¡Ì.´fL\x0007}hDù­«³\x000bé¢b¾äwa\x0010ùr\x001eÍ\x0015íìÔOÕîüØ6Íý±þ ÓH¼ûóãO~ýt÷ç÷\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=»<9¼(}°oÁÊ`ÐàË¡S&À*TîÍ`Eà\x0002Ø·\x0008ûv!¬\x000e8`¦#2Ml6\x0014ÝôR(B
[ÛÃ¼Âß\x0017Î«ü¤2\x0013&Pâá`½\x0013dÔi¦\x000c6\x001c°báï\x000bWl0Þ5æ8\x001aÍ-fCÍeØÁ,ý2Xñã\x001bóîçN¤+cøØ¯× Û^è\x0005½IÒ¬+"uÎd\x001dÌíÎ¤ 6öú\x00084Û§iS\x001aÌbZI\x0001\x0010s(Rç¥Ðxû:6ý\\x0012a*&çR\x0012iÑ`ÙÍ¥$j(Áz\x0011nJ©]E±z\x000e\x0015c(Ü=`ÃìjZCÜ_²\x001c×9\x000eæ\x0017Eh%§Â`§\x0007³a\x0016á¦¤å¸aÁò´ÓH"aí\x0012îp¦Q9îã[ÿéçm4È`íê¼z{xJ±pÈV×Qñ\x001b,G©vÆØøZèôßBæ¶ñ³\x0010)F
¨\x001e\x0015ÉñS\x000b¦Âå¨PøDí\x001fsQ
8»sõVê3ëY.`â´A
Z{ñ³\x0014ÒMñî²ù3\x0011P*'ÕP \x0013?\x000bI=Ée±øZ\x001d\x0008Ô\x0004ÑÎ@ðL'F3{¥\x0006c@â¦âY\x0019Ë
Aõì²ÕRzùßÊ\x001c¤óÐØÍâöw !'\x000e«IÔ·2?Ë/MÇÕëÍÍÍÝmá
k|.\x0003\x0013\x0016£ÞjÚ\x001d\x001bÌÃCõrõz}||z2	géî<Ë)5\x0006çÂ;yçbmÊ¿°\x0004J9\x0005$ÔÅÏ"P)S\x0007Ô\x0000*Æ\x0016\x0008X\x0018JØóvÊ\x001bS
\x001akÎãg\x0019hÀÑé'\x001fj¡ÒFÎ~\x000b`ÂX)\x0006\x0005¥ÍøY\x0006ª9)ÌA\x001d¾&-1\x0019\x000f~2Û¥\x0014T\x0000Qü,\x0004U\x0007hý	C¥Å\x0013o|'\x00075\x0006grBs¹'ñ³pz²ûXø%ýäµ£[TO%;\x0014Æ¸Q'l4\x0013\x0014z\x0011PÄ §\x00179×ÅÚ)÷[9(\x0004:îây Ð=8ùGÍõ
%\m0!¿IwfÎ'h5bÂ+Çfn^ì ¤ÃsÂtªÅÓit®á\x0006\x001bX!B\x0013:\\x001e:\x0017TCLC³¥\x0013Ê\x000cN.¼Æ¨dOì\x0014Ppf\x0017Æ@Q'N4÷'Ï1³\x0001ÒE½¡|®Ý7\x0013O§RÎ¨ªlõÒP¾ç\x0014×D¸ÿ³ÄNÝ\x0019zõé_þø©k5¡ÂùáýÇ;àÙ\x0016êÊpÄ$L\¬Î\x0008vS\x00164\x001c\x0004EÕóÃóW§ð\x000fÎ´\x0017;¬èöYÊÊ|l¦\x0013ÅV²N à\x0004Dí°ïo\x0001,:}\x0016Â
pª£2L¸PQd9ÚSÚÛÁÓt\x0001,º|\x0016Ï,\x000f¦8³Y!\x0010ÚÜÓÌ\x000egc.EÏÒuÆÝÉx`dÍÁ\x001a%°èîY
k$I9ez¹&ÿvzðh\x000fK/iÁôCÑP¥©dSz\x000bèÝ6EEÅ°J\x001ch§\x0016YËË`Pg	,\x0008oUì0!(\x0019'À\x001a\x00128ÍÓ:\æPú ß»\x001fþâFÈ x(7Å\x0005/Ú0´©Ý\x0010X`*èUzV»Ö;à\\x000fWºtH»÷Á\x0012R1ø¨Ð¤	¶ãV\x001f´¯\x0016Àvï\x0005°2¹%âÌrzþÅþ'8³Ã1\x0005°Ýû`\x0001,\x0008\x0019æUà¨r7Ë¯êA¤%¬©\x0018v1+·¹²0L,ÆõY3iØC½\x0000¶{wÍU\x0010i%Å\x0018Gi#J,å0XÀ½\x0004¶{w-X+¾_D®6W"'b\x000c+y,íß]Kh\x0019ÚÜáµåHJ	êêaeý:Ðü§òsçÝõ{z\½Ül·wÐ_¨W¥ÊRt_h²9UÒÎ]§ËÕËõÙÙ)´\x001d&Nm
±vÝö·bY\x0011O
&
ÌAÞ~Þ|Ün&\x0019nÝb§°\x0015ÜÀk-	 )N×®u>Ì\x001e/\¼C\x000f±\x000elº\x001f\x0016ÃzÊò\x0001c\x0002$H|ÐäºÁL½bØ·¿ÿ¤s¬ýÅ\x0010\x001eºo®o7¥ý28Çë,æ¿1Rå¢ª~hB[\x001b^»ONÖCFM\x00078]h\x0015ÀLàÉ\x001b5fÄC÷	*óî×R`ëøéá\x000fâ÷(
êSð9¿£bãÔ2-üY|\x0001ÍÈþH¹Ât\x0018h\x0010æE\x0010ÚãM\x0005\x001b¹Úé\x000bh2öïOÎOS-ñ×zOY÷Ãòöýýæ+}Q\x001eWÇw·ï¯#C& @þ0k·Wÿrsuÿ/§Û÷W±#\x0010\x0016\x0001äÜÇ¯\x000f,$Ýx\x0000dJá­u±:¼\x0008óv\x0002m/ÏW§g/.\x000fÏ;:§Ç§'/\x000e¿îÒ\x0008Èoþøéñ\x0017ñõ¾3ëÇ7þó#µ(ÅÖ à\x0000kT2\x0005ó«#¶åâ\x0006\x0002ÇÌ$5ô\x0002¼|zø*öÈ\x001dÉÈéP®|:\x0002\x0002:4v\x000eï/@ºÐD.ê]9úÔXZ\x0003ò\x0002	ä©\x0013I"7H®Þl;r\x0008ï\x0016s\x000eÅ'
§ÜCÒt\x0004×\¦Û­!y¬Ik2ç\x000csîá AtI¼xíÐá­¢tI\x0017<æÅ\x0001ºày¹8×¹I'ÑýØ\x001d¸\x0001ºMúF	=\>	ÝùÞxCÃ4u\x0012\x0001°`äÀ\x0016ºo<åÐÊ¶9ÑERfLÜaÍGpÁvè§ÜévM¦Ü)ÇÓ%\x001f<æQ%rÑøt¢9×d\x001blì\x0018®Q\x0010Í#tOm'Ã³2~êÙA|
gÃã%nQ¿C÷mgÇW,gMö¨Àë(êé¥Igtº\x000cµ#\x0007{=~\x001a\¤
ÍE\x0006EnRGg:O-¤Û±k`×mØS1 X7©%±1¹a±ã[\x0013r¼5\x0012*;ÁµÐ
®uþðì*J@4Z1\x001e\x0017»Õ\x0012ÝjbgÓ\x000fyì°bL\x0015\x0013^ÂÒ!{ùEv£
±óÆÇ#¤µÄO\x0003\x0013&/Fv\x0007ULÉ!ÃÑ:ÑÖpä \x0016\x0015?
ö$\x000cË=JG¥£Ýeô7é,t\x0010\x0006èáÄ=ºþ\x0012;D0#;vÂlÆ.`	&ï;m\x0019M»ã \x0016ï%ð\x0004ÓÙÞöF\x0015Q)[ðFè\x0002§ÝJH\x001fAv²\x001el{B
Èò\x0006F\x0018\x0010ÁÅÄ¡#ÚtÊxÑöf\x0012 Î\x001a?
Øe}Â)\x0013\x0003ÌÑén\x001b¿¬\x0005xúã§\x0015&B\x001d°\x000bh\x0018ì0å½É[éÎ]ýîß\x0006ôh\x0011?»¾µ¯6ÛëÍ\x001c4<ÕÍJá%×Ð\x0005¢`ÁìM3.¬p\x0005«eõj}v´\x001eò×edp\x0003>q=GÆ\x0002d+Ñ\x0003
È`ASn\x000eY¬HÌ\x000bn¢BâX\x001f?5ÄZªTÈ#@÷\x0003ÝÎÅªj@VØÔ£\x00052gÑÄe=\x001bw\x00013$JDc\x0001\x001eoH÷i\x0016P¬\x001e©_U\x001bæhÜ²u»\x0019:éÄìbCc`\x000e$\x0019¶Â0Ölip\x0015µÂâ·Yñ`¨Ä¬=²)`6 ?\x0014Ã\x0016\x0018Ì±ûaúÖ0°MZÏV:X&ÀlÉË/\x0019\x0014/W2ÿôéÇ«Í¶\x00138úðqsO\x0011ßíÕ5\x0016Ò\x0015Ç&NÔá ã '\x000b0Lpº\x0017Ã=¯\x0017ÇÑËW\x0010àÁØïÅÙáÑ@E]ôzëÑ-OñT@×èäw ÓDìrØW¾\x001dÉ4`·©¤\x0015Ø\x0005\ï]ÉÌÎ\x000f¿eì\x0010ÿ¿êÙ¡?Hì Cì\x000eÑ\x001a¾Ó\x0017¢k°G KpÀ¥i·èZq\x000c\x0015XíVÌùxÿswµïN@~¾Ùn¯¯\x001e\x001eæ°sïEzõ\x0008ïE£ÄxÖ·P%¾\x0015@?_\x001d\x001d^|½7D\x000f\x001e*þi\x0002ïRÝ6ÀCi\x0014Â;­¾Äi>\x001e4¥h3õ©U\x0010Ðäb²Àc6S¢÷%Þçô±·	=TÊ%xe ä\x0012§Â\x0015áYWrÎbßï©\Á®MLL\x0004øpS¥·k¤·%ñÐyôð$±mf^³q\x001fèÃï5Ò£é%+±\x0016\x000bàï?»«\x000fÝV9tR¾ïöî~Þ«Í@÷åävÊQÈÂ	ç$núß³ÓóÁGÛ\x000ezÿjZH­xª¹\x0004êØQ8R+<c\x0002õHÔ\x00015dÇÂ_ÔB,NI
±\x0004=C¦ÐÔH¼\x0012Úyr8CßÞäMñ±õW\x0016\x0005÷h94©î¼~8Lq\x000cÔÐÕ7a;«\x001aÚ\x0016Í¡\x001eHgÙa;,~*±=6Iáh³ØÍÂl¸tâ§Úú¤\x0017¨Ã/ÑÓé\x001cÆ\x000e\x0015³Ã¯¡%­à±\x000cZlZ¥ÉÆ4\x0016çÏ³=|Õ\x0017Ï6ÿÝÿ|ÛMÌ[ßÜ`¿¸ïþüçÍõíõûY­\x0003ýÇD\x001dÌ«\x0014wsá\x0015MK{Ä²\x000eflÌÍûîðøèéÙÑÃ¡ÉÞQ\x000bè\x0006Áê±=Wyc¡\x001bOzJpîð`Òºa³ð+àS³M\x0017Í76ÝPêf`§Gí nÂÎÔÃçÈ¹F4¾\x00054tjÃ\x001d©<ú\x001c\x000ff-b«\x0000á|n\x000eNø©m\x0011+ð\x0004t´J0^\x0012\x0012?kLÃ>~êgÜa\x0010ßú8È-È$	ç°Oh\x0001wWscg\x0019\x0000wQ/.v	^9fØÞ\x000f. ÿ5~ªÁÃºÆL[«å\x000e<\x001fÊ´Ü\x0002zsÆOý\x0012\x0010ÓI'
F\x001dÂJñ´Rn¹5þ\x0016\x0013îuæfÜo\SÒ÷#â\x0005à&\x0015?Õ\x0017&cè®eÆr|\x000f;h÷àØÀ¸\x0011¸\x0004-ø©\x0007ÇÖ¶\x0001\+r\x001aòðúAp=b|/\x0000\x0007q±ø©\x0006,5³\x000bà*öÜà±
x\x0004W²åi\x0018«¬dSÜCÃ\x0019§ä½\x0000îòóáGÚ\x0012ppXé\x0006\x0013À1y\x001f¤Â9.\x0015ïiÆµmyÇ&)ñS
.P?pÿ ·@_7føé°Û\x0005\x0003<~ê÷¦¢|\x001axkÒ\x0012Ï[Ó5µS\x0014¼-ã§~¾)ÅÓrÞµðxðôTãMÏB¨Íz\x0012?õ\x000b\\x001ch´hÃ±	<VZ&î¬Úbîíç÷ï®X§\x000c°Ëñróþvs;ç],uÊVJ7½ÀÈgÐ¸-A3Uòrýâd}2ô.ÞAÛp¨ZYMíYRéëR¡ÇÇ\x0007ËÍå3pøÖO
uÈOâ§v²M
mÀÓ&Û!ËlQ\x0015\x0010a\x000f9OÔOâç¯iI¼¼~{÷¶#ÐP\x001c_ó>93Ã\x0012æ\x0018\x0002wÌcDsnó$ÕðòèÙé³\x0011±\x001e8EIªÁ-JM\x0007rXÞé²dY$g~ø_Fn¡MU\x000br\x000b/ùH.ì4H.2¹\x001a^âÈ¡]á
ÈµMú^;\x0008ó`ü\x001eW\x000bó#þúEäµåZK\x0016J ç\x0007\x0018\x0000g.*À!«È·X,Ô9K_P%*Æî5szø\x0014_B\x001eK\x0015â§\x001e\x001dX<[¦LBÈ¯!ôÆgKÔjtÒá6(ªÍËÌY:Ðc\x001b­ø©fg>å\x0015ÂRgT\x0004ì-\x0016ÒhÐäj<íPJ\x000bú\x0015#Ñ¹\x001cÐ=X¸Xv·éH\x0014s\x0011:ç¼É¡\x001eNríð"¥Yw±´\x001b/RÛöÆ;Oâ§þlL
\x0011Ýa±;4\x0014ð\x001e¢[¢)~ªÑ\x0015JË\x0003ºÄ\x0005ã\x00189>5´~lþûÃûc"-æ9¯éqõâfs{=ç5\x0001Æ`Ò\x001c$]SZ¾'§F5Ïñ¦ËÕãõÉÑ`("\x0013Çòø©c\x0016,3C9g²ËµSDzÓÔ\x0013Ó¼«¨6&5V\x0002\x0019p*º*ñ\x0018W
»\x00037âÓø©\x000eO	\x000eA\x001e¬\x0016²R¡ T#kz>4\x0004|â§\x0012ÓÉÍAA]aú¯t\x0004Ý`yð_\x001f¹ÿÐÙÇ×W«ç×\x000f«\x0017×\x000fá\x0014ä\x0005è¥ÌÓ\x0012Ð&µ
Ð\x0019®ý¤ß\x0005ùÊ81\x001e\x000eËÕó£Õ£ð§p¼\x0000ñÎO¿ør\x0010)ñ§Í ßCu\x0015\x0015µin\x0015ãGÊ|ªF\x0014ÚÀiZöÊIè\x0012\x0012\x0007a)½¤\x0006W!óÛÁ\x001b\x0002á ndñ\x0007áñe§¨ÍEûA$E¹&ÐÌ$Ùöè²\x000f¡\x0010[SÊíHâgÕ Ò\A*\x0008&ÉK\x000ejMI7!ÿ$ôH«j\x0010I®Í ¤ÅR,®1Õ*¬nV£ªU#Hu
mF Dì\x0004\x0007#°Ê­´ü_4\x0008ÒÖk4
É\;°0
LiUÐ(è¯\x0019\x0005¦¢ã£@WeQhò9Ü.VA[K)£Nè¿h\x0014ð>ouÙ+º\x0000
Bi\x0014TÄãþ]AúKßÞ\x0018ØO®î>~í\x0001v\x0015\x001e77W\x001f¯¶\x000f×³|öáº'A|Òh®5g\x0004Õè\x0017{§´ä%T¼:<»¸<\x001az>îèyTah¯9ªÔðØ{S >Vc*
>ÂÖü`ÅÃ_M¦_¥¦\x0016ÁX
&SÈO)ëFød\x0017òs¨Iâ{IK\x0007 9K\x0004Â\x0000²\x001c\x00164eÃ\x001bÚHQTVU0\x0000õøîêó§®àÞ«ÍÛ}ÙØÕÙÝí»µ\x0006³j8F£ëGp<MµòÃkèÕñúÙ¾ìêìôäë½qû£ÀmÐj\x0014\x0012\x0013Ã(\x000c\x00153nÉ71r%T\x000c"Y­\x0006¡¢:2\x000cBè\x0003òdá\x0008ÌHMAÅ\x0010bW?Ñl\x0008Z#Q
K$£ê{\x001aÅÈZ1
ÈCÒ
G!ò¹
é
äÉÕF1¤P3Ø"¨Ý(\x0018jõq\x0010Dàô³àöÄHôö(~d?}|×õÌ\x0004âûÍãÃ}¬ÌÞÞýzuûv\x001e?h#bö°Ðë*\x0002$þ\x0014¤#©9ðËï×\x0017ç±<ûìôõáÉ³ÃAÛ¢\x0003\x001ezx.%f¸£×'\x0005#¼\x00183Â£3¦\x0005<&¡%Y³Ä.)·Hk.fÇ§5{xo¸¦MS"¼ö$ÄæG\x0014p\x0017Ã'õÞzxxÚ \x001e+H±!¼¥,:çÄ\x000bl)<¾ö«áA÷\x000e*Ã8\x0014¦c0ERCvä\x0006[
_ùÕôÎg
_-¡v+Y\x0010PçÌHvñbzzÝ×ÒiN}a\x0002½²P¿Ò2Hn(\x0018ÕíÏÊüª¯¦ç<kù¦zÐ\x0014kÏZ¾zÌiº^óÕôBâ#i©ñ¸t±a.Ò\x000fgb.Ç7@=<4\x0015CµPÐoA#ÁZZözDck1=*rÔÓµ9w\x001aÂ¨8õ.«nåÔ\x001e_.
è\x0015¥×kf±F4Ðç\x0003Sü\x0015+\x0007r\x0006ZÜU\x000eºdãÊá\x0002?ù¼rÄ3q)}RlAo8Õçî´AÈo'ðÛ\x001e\x001eõæ\x001b,\x001c~7\x00062ètÚ;G§=\x001fI¶_JOe
¦ÞÆ.kQCåª\x0012ÊJN\x0005fÒ*aÓ\x001e*\x001bI\x0001Ý>a¢GvÕ~ÙØ\x0003tAZ\x000bpQQî=³´æÛïW\x0012\x0001jÀNÉ'\x000cä	­¡ýJ"ÅÐ4¦9=Jé48+\x001d\x0006Áb³\x0002*\x0006\x001bü_@\x000fbmNú\^\x000fÚâ2Äµúë\x000cXíØä \|4\x0011\x001c;dß¨ü\x001cü\x000bJ
²Ô:6w/ñØù;åÓª\x000e_Íé%(µxR\x001bé\x0000] BIO¾öØ\x001cª\x001e¼\x0004\x0015õ¸0aþiÒ9Ê¼\x0005ö¿\x0000\x001ee¯\x001a¸?\x0014¹n\x0004¥»Y[Ñx9¢à±\x0018\x001eÜNMüNR¡Î²\x0002NrÝp*ü#ÒKá¡t³Åíj\x00019àèñS&»+GT\x0019\x0017Ók¨ßlâòó»&kþzµ;iÚû\x000f(zÒ`Ñ[*÷ÕNå^]êÿ+V=Ö\x00025ð	Ì`f!Ã0å=\x0017+\x0007³þ/X8P#Þâ~µÞ&¥Zðy\x0012\x0008¦\x0013£ÿ\x00157T¸[e«û¼\x001f\x0012mÃýÊ³Uù\x00178 w¤Ü¯L6±Ã=\x001b.]M\x000bÇ\x0014Ï£?þþé\x0018£úJ\x0017ÛÍíûY#\x0012¼ô\x0018ù\x000f+å \x0007ðç\x0018aSÍ/^­O^\x001c\x000eÅÌwÔ¯èM5ux5a.0Ü\x0019-L]$¦OÔ\x0003û\x0019ÃDó\x0016³í()CS@mO©Ù¾LÑ½p¶!ÿäIüTbC/Ã\x0014ÔgÖã{5c#6\x001fÑÛ\x001dÃr¯·Ë\x0012láü¥dÞ{8öacð/\x001a±~±7·~Ó½ví.ÞÝz¼zCÁ\x001b®¡\x001bMÊÄ¡²ª Îåêééùß/\x000f/\x0016v\x0019¯o\x0019r©Ô·ÅÌ¡\x00187~¾%hÇo	\x001aÝñóMA;ÝW¯inQ@\x0000ª\x001f\Ö$¡¢lA«\x001dóÄi'àÈ\x0017]qîo`¡{üøù ¥>	Q	\x001d`±\x000f\x0016³ãi©²%xñò0\x000b`xíÙÁà\x001dæ±\x0012Éa\x0005ÅI½Õ²OÅÌ\x0016"¬VÔ.i\x000e\x0005ë¸:¤¦¤5-rs¶åÌ¦f»Ý1{¾c\x000e/l8\x001cÒ4\\x001b\x0016þeñS·\x000b¤µ¡Sð\x0008mÑÏ\x0013¶á´:M93Äd¬«>9D|Ü¦CP¤Ù°\\x000bU \x0003TÌì@+~êAÕJ!³£^ã¬ÊÇÝ´\x0006~1´wÐ\x001eÉÕ.èÿÞ#ÚÃÂðÕ«#Åø`á:?kÕ:lò×Òþyûñý¯\x001b¸WX/ìè§W7«õõv\x00161hâê\x001cBý0»9<÷ÄO\x000fWë£³)\
¤º\x000eW##%vCÛ	\x0010ø¸\x0016£FøÈho>É_¼é¤ªÂó«ÛëûÕÅfûîúêq_Ée
\x000e-D\x001c¶6w\Ôø99:_]¬Ï\x001f\x001d^N"Sì£9Ü~(¾¡å.©@ç\x00067jä+e~øÙß~ú¹S2Ü)!yzµ×ÖÆXµ#ÌyuàS¨ÆyÔÜEQñÎÓÃ³Á6;`J©"úì¸áEC\x001fÙ¨\x001dÉ\x0015MLAÔ*âð\x001eÁÔ<ç\x0018æA=cèXÛ\x0018¾\x0019VKì)µÇAëN\x0004&^]Öë¨7l:#j×Dî{
)\x001aØãÝyr-r56;4ÕëöÆ.^,v§Á}ç¨\x00086yíÖ\x0004<\x0019ÄO
²MEø´(\x001c%äçeÜp\x0015ïº¹×\x0012kZ\x0016ü W?¼*:Ô\x0011­¢o>±Ø -Ì±CùFë\x0015µ¾àcõWÈWìöÇßR\x0011"äï¾«ùéæ\x001dÐÏò5\x0007k\x001bEí\x0004ótö¥ÆL@-Æª÷:¾æ§ëç0!gs\x0006\x0017pñ	Ö\x0000<¼Hbw.)¸¶T(&©eG¸Ãe4i)¸´`uZÖ`Æu!\x0012¸£6K¿Eà²¬)q)¸b1\Ø\x0000\yì\x0004-$\x001b§è.ÔÒª¢àU)¸UâZ,\x0015×¸\x0008¸NÆ¾\x0002ó(+^Ö9¼\x0018\x001cB@ÎÔsfA û\¡²²ª\x001aÓ\x000fÎ¡ÊòIúV`ö§¸¸P¨cg$)ej^Ò/·\x001c[Ä.@ñ[\x001dþ\x0007\x001c-­¡4KªeÐaæ\x0002oÅà±yÇ~ÏíEàºE	\x0019l\x000e0éÈ[âÁ\\x0019×¦~Æ¦'Pç¦Û\x0012+øµ¶#}^ÊÉ?òëÿ¸ëÖ\x001cu®úxµ:~=¡ìN¯qJ\x001a\x0007$)ztßî\øçë£ð\x000f/
]û;zjÁÔ\x001e´ê±m
Ó?\x0014éÃ? ú\x0011ÅÆ¥ô1ôÒÃ7fÓ=	WXC\x0003l¤¼z!;øT\x001bveHÜ2\|V{Mê|¤Ds\x0000~ÀÏ·£\x00079HãÐa\x0013]¢6¤)ÅFtâfMý'ñËÆuåZHèóÙÿx·§3ãÀZ¼QA	èødÓÜ¸a4>\x001d>?\x001bÎ¹ÙáRMf
oYQÐB\x0014k\x0015\x0004'ùÝ±î­{¸SKëº\x0016Ú.a@Ãú»\x0015$.=æÓÉ
e\x0002ºvf\x001dI\x0004z°®pf±\x0012A\x0007Û§ÕÌîz\x0013VájêvîÃ-¨×\x0012Vøi.GZåÍäµ`À§×\x0010åæ¼ÍBéÇÕHðy¼"*-tºðå Pü\x0017ì¦dð	Ýñ4×#wøLÞ¬G[³\x001e8ÇdÙÀ+PºÌqÉ²·\x0019.8öâ§\x0006×0X\x0003Ñ»\x0000.(êÿä	×»S¼ðjåÀ\x001dÊÍåÀË\x0017¢kÂ¤gÎÄÍÍÁ¾kMêEüÔÌ¯æ`1ÄùU6Âae\x0016¬Ù\x0004K°¢â§W
a¼:w\x0013\x001eàb$õd&®\x0006÷®»-¼¢jÁ¬¤ÒR¨GB\èBÙ\x0017Ò ¤©5ËvÓË\x0014tqLë\x0017mÉp<ÄgòÚäj+
\x001d{8\x001e\x0004%ª1GvY0ñÂÎ®Ò0ó*¯p1NeÞd=ø.1¼ ÿ\x001d?UëÁ\x001f¨äa\x000cûÎ³Îí6f>\x0017\x0007_w<p!^EÎ`µã]¥5yóé×ß?ë\x0018\x0007\x0002Ù\x0005ÖÏÒÞn>l~ÜÜÎó·\x0008p9ÇL~n(ùÈ\x00194ÐÔr:ÿrõôlýrýÝúd\x0012\x001bn¸ø©ÄVjã¼Í-£¦:Qâ	-Ç\x0016,úYX5v°ÙQâÂ[E\x000e\Ú
ä[RGï¨¦Ö©9j¢fÎ\x0003^]Â\x001eéþ²\x0000\x001b*±â§r²½£¸,¼=\x0008S\x0000.¬¦³ûÒVÎ64¾L¥ýÞxìVç<e\x0003·SQj]15\x0014õêsDgmÀ0Ùxé\x001dZÊJ\x0014Ä°Ê¡%D%¯_ØZS)¿7Z½x1Ã0×#¯ÿ\x0005Ø0	r//w	¶Sh53¯©¥¸gº½\x0008ÖtHpëKS?Ûa]\x0018Äæ\x0012\x000b;=c$.ÌÍHblqãÍï*>ä\x0004¨_>»Û¾»ÚÎjD" Û\x000e»_)hô\x001eZri)3Ò´8$@÷òÙéÙóÃ³Á^$;tpâ8Ó\x0000]\x0006³\x001fuGÃihÑ9+IÙÜ(^\x0010¢Îa.â§Ç&\x000bqÚÃ
Z\x001aY¥©ÓQ#rà\x0005¤½ÄO5<×\x001c³?\x0002¼H\x001e[+´çmÌkõxY`XubÌ\x0017 ¾¾½¿¾XÊ%ùÂË[b\x0019­\x000b\x0007aJ,Ul:±ô\x0002T×ÏÎ\x000erKwÌÐ))~êQ\x0015³K½Æ°¸Â\x0010´äÓÏ\x001chhW=ÑÜ&Gn\x0016Ùî\x0014·WO9t\x000c)wãÊ cÒAÌú\x0017^F1\x0010©1ãC87]\x0012Ò\x001ep1í¨!»FtRlQ{²¿aª¥"M?ÁÑ« å~ëìþ"\x0019}!3÷I·50\x0004S&Â¹"\x0008²À þäß°ÛØÄ\x0001\x0008L/ëÿlóë] ö/d0W±!j8©¯¨Ô°Ë²é\x000e\x0017|À>
2÷¿£ÅÖJ.¢V\x001cJª#µµpÑÇkÆSQ¸\x001dñøÏæQìjjîð\x0010[[ñ´\x0015\x0015É\x001dXîK©A\x0007)~*©ExÐàTsêe\x0015ø©\x000eD¯¾B=ä£ÎØ\x0010\Jl&¨ÚI9\x000c¿Z
VÈ\x0012gCñdë¨fZ½\x001dcé\x0010Õ\x001cR¡¤¤\x0006\x001a°mÉ3¡\x0018\x001b¬÷ø©Äö\x0002\x00139ÃëKP"N\x00111\x0012ÄX
K»ê5\x0002ª#¸´¥æZ±Ü\x0008I\x0016äBÎ\x0006ï³ÕÐR¢56SI)HîÚ²äü, ö\x0010\x0001÷¬Z3°LciNx#¤üÍ°°Í®(®äÙ^
fª\x0017õ+$÷ÄÕ"\x0016\x0017¥5« FTJ©ßmýý'ÝWÝA¿º~ûÓfV?\x001a\x000e{.ÙN vrÚÕ¤gÄÄt]\~uôìûõ`'\x001dóÊ#\x000bAþÊ§÷\x0000øÒÒ¹g,ÃÊ-á]Ñ^Êü¥í´9¬Xm\x0006ólÐÅ`Gßd\x0005Fê\x000cæ\x0000ôÄºZfoEáA.E\x0017q¤®ÇLÑ6,eÞ÷,cV*EìÂ<{
ªÁÙb²½\x001c\x0015,enûn»ÉTWõ[sÝlV¯6\x001f¯\x001ef:\x0014$g¤/Í\x0015äg&_¥R2·¶\x001aÝu\x0012í×«WëW\x0017#N\x001d?ømÃ/\x0018ÕF~Ð·\x0017øJ'©+#Gb¥KùÁ[\x00015á·¹¥/W \x001d\x0006\x000c5Ä#®´ÅüP¬¯ÛðÔ\x0018öå*ö£ìÒÎb³øáGê\x001b­\x001f-©\x001e7üÇ±!±Ó,Oÿ°-»\x001eúøFô*ÓcXXs\x001deásàyLe¼
=\x0014\x0010½¥úmm(º3êF7ì§¿½é½ûÕëë÷·ÇYay\x0016¬\x0000x*V¢á\x0015~­©ÚQ\x0016xc¡¦à|õúèÅÉúrèäßÑÓÊo@¯í\x0001æWC;·d5r.qîY53\x000fþË×þrz\x001e^\x0012°a\x0015aë'á\x001cÅÁjo\x000fÍ$ã§Áä;z20w°\x001a+Z:Ìdt,Ä\x0007\x000bï\x001d.Å\x000fï\x000clJa¹$ßVø5¤Èòïeø\x0002jçâ§\x0001>x0Rº	?.a\x0019YÅ
$xZãC\x0017µøi\x000f9w)o´ÁZZË#Ír7"ü½\x000c_Æ\x0017l2ûBåx­ó,ô­TjÄÝíBzxÈîÃ¤æàÔ¶
\\x001bl/\x0002',PÎ¯c'Û6\x0007O0\x000eÐ3\x0013\x001e>zRsK\x0001Dn¯\x001d\x0003:¦+*W/-IPû	­e{Àr1Ò
g\x0019½\x0005WUü´¸rýò8ù
\x0005ûÃÆeTºoGêÉ\x0016â¡ËUcïxR\x0007n\\x0002í\x001dß\x0011Kh\x000fq\x0018ë÷\x000bW\x0017_Z8ùéúJw!\x0001\x0010YZä\L\x000fUJO\×ÃW±òÄX\x0001sÎ\x001dpç\x000eÛ\x001d­'ßCÑKü48ôµ \\x0017¨6GI\x001e\x0019\x0016?æºXÇ\x001eþ@ææ'õ»¹®\x001d¨ï®ÕËÍöfs{7'Á(¼Rlª\x0013Þ(ª&Æ£7\x001bN¢ë³ãõÉùéÉ$6W±g^5·\x0008ÿ*POHN)yô÷Xz+SqÈ\x000cò®\x000cþEi)¸\x0012ñi\x0012æ\x001b
Ó\x0015\x001bÖ\x00089åÌ\x0012n\x0010\ç=ÕõÜ\x0012\x0017ypP\x0002Ä#F`Ò³ð®ä,\x0007\x0017PÇ\x0011?µàF¤\x0012ó\x0000Î\x0014\x0005PÁçHX'¶À\x0001\x000eá<a\=¸u©h@\x000c¶¤Ñô\x0004Gn9R\x0006¸\x001b\x0012ùoÃm=f¼(
³3
e"\\x001a-&üÇ\x000fÂønmóÝãÃÎes{õæúÏlg% A*\x00146»\x000eèTj\x0007ÚÊ9·u¤6åôòbç±99|ztx6XUÞO½®«á¡"\x0016RpácRIÌ²º¾K>R¨òUøçð\x0010\x0006ôÊ\x001c`IE0¿°\x0002Z\x001aI]\x0006ÜÈËc\x0019|>\x0018[À+ª0æ,ÁIÈ£é.ÍXÍØ\x0012ú\x0018rorÕCräøi0ùÆÊ\x0019d1Ì
´YüÎ\x0015p.|\x0005\x000f±øi±t8Ìx¤>8	^Q
îÕðY¹\x000c\x001er	â§ÁÊñT8¼6TY\x001fn&G\x0015\x000c²1½è|ü´ ÷\x0010\x0012InVM\x000bGä$6¡Çt\x0001\x0016ÑK±mæþ¿×j\x0017ÅÏ·\x000fi\x0017ñóâÃÒWÍ¾MÁ)HYOÕ0N²übå#Á©eK\x001fr¹âç\x001b|\x0003øm¬\x0005fÓÓ\x0015&_aÙWø5õjd¦ýÊ¯õõçhb¯Wñ_ÿñëÛ÷þóæúÓã¼²\x001e­èº|¬¿bµ§>sºÄÃº:^AS¥ã£¿_\x0016À\x001bÄµÇtÃØy\x0019ý«Qû_S¢\x0019Ùc\x001fX5;xj6Þ^	Y\x0001Í\x0003y­%ÂÔèêÍzjæÚ^òÜ\x001d+hà$¯(®ãTAÇøØ °	~J¿IøÂáZçfïª$ª6\x000b\x001fÎJ¥\x001bá\x0007fAkGQTMknò¾-ðPÎÂªl-[áKêªÏ%yd%CÈ6³Ïµÿåí}Äó~ç5«¿]Í¬Þ\x000e\x0016K	£²qªÅ^{?é2\x001ao«¿\x001d\x000eÖnfd\x0008\x0014=*f%\x0005%
\x001bç0½\x0019Ä
Ð\x0010~5\x0019\x0003\x0001
ëNtb¯Ë ¥\x000fZ#´§\x0013dÏ8;Ý\x0013²\x001cúäÐáÉµÆsðÝ$¡T©	zäõT
}ûñöÃoü]SN¸ãèÝÝãÍ,µ\x000e.\x0014+	ç\x0014G5\x0014Ã\x0004ö°\x0001Å×"Åè£ç§áLA+:l\x0019ÞwQ _8È~ÇlL`¦E)\x0011Ðñ"ÖõÐÂÙÔ@ÀÝz\x001d\x0006¤	{¤\x001dô\x0002l\x0008nh­«±¡\x0000%FfJ{\"\x001aÕ"õ4k
Eöû*ºK°d-Q7Ç0AkDØ"Eñqê\x000f7VþÐi\x0005Ò)¸ºx|¿y|7Ï¤5ø\x0008??uò¹ç¾ÏÓ7\x000cÔG\x001c_\¾X_>Äþ²@b\x0019¶ù\x0019\x0011F ²;¥s# ¯q\x000f·îÀárÔõà6&ÀGpEb|Ö\x0008E\x0013>¦\x0016·`ÂaFÄÏ·6ãñ
Î»¹%\x000bÉ­\x000cÆ_\x0004\x0007\x001bJb¿\x001by%Òt¼\x00193\x000eÂSOj0ã1Ü<¿s ×\x0016´V-!à(M\x0013Å0|$K\x0013ªÞ\x0003ßÉ¤cCÐ8~ª\x000fBªó ^@ë[ããØ@\x000eXCì(\x0005¯|ÙþoÞ1\x0012\x0015?ß\x001a¹\x0005hÛ\0tÚç²SAàÊ\x0017U3Ö\x0008¯cõ¦Ðº<\x0005³ç\x0000$\x0004æ7PA~à\x000cn\x000fSí[¬\x0014Ë\x000e$Êv\x0018ïÃÖÄl|)UAv×,pÐ8`ê[â<&\x0003¤oíZ1è§\x0015\x001e2ê\x000cÖ±K¬|\x000bFnÖ_és\x0016Û³~¿ðä*$m¸ïGgèÎnG.ãË\x0006sÎ­¥\x001aZ¨:1ÅÈ<üóë+H¨Mßol¡\x000bÁ¢wÃ%\ö&\x0015[\x0007Ó\x0004æ?\x001e.\x000cjDtÑÖOú;öéîÇ`ÊùÃæáú.ú5\x001fç¯t\x0014\x0015fÛiï1ÛÕqÜ\x0011\x001cRHWøùÅúâè4¹3/\x0007c?\x0019woY\x0003Ì\x0005\x0001{h¼é&9} a\x000fûOæ\x0002¡\x0016?U3l	Ø*
½qÒ\x000c'¥\x0017\x000eÒÿ
Ié j\x00196\x0016 @f!°\x001cù	,¡Z!~j!Ï9ñzMg\Ó°Í\x00160tm~\x0012?´Æ#.'	Yè³L¼#áÀ±Å­ªÞqö\x0000y\x0019?p¨l\x0004!\x0007\x0017[;^hå\x0019?U\x0013,\x0017ú$\x000b¼nÄý>w×
ºW;\x00019\x00118\Õ\x001e{*@'\x0004lF¤#f\x0002[`µÀ êû
zN¡\x00089\x0017È+ÇZÒñþòáÇÛ_£ cìù+ö¤\x001fÿ×Î\x001cdÞSä+<­PÒKNr3>ö½-Ð-½ü÷á\x0016ì\x0019Ù@:ñ¬
Y1h>JúÒJ¼\x0011Ôd¸gæY¶ Äk÷åxg#C?\x001bì)\x0019zk¼¡ÜG
)\x000fµÈïåÍûONªòúææÏ^\x0001ð³»û\x0014üú\x0017WÛ\x000fá\x0017sÖ´\x0012k%9P\x0018v\x0002ð¤µ%ùH±äúøøð\x0010Ø\x001dc\x0018ìÅáÙËðÝr¡_|1\x0012îþ/\x0018
èqÃ_ÿ\x000bBÊ#ÿ\x000bBÕYßìP~ùíñÍCJÀ\x0002E^tíåÿßöúj;«F.\x00021PerâaTh\x0006YI|íååÙÑáÙ`}Ü\x000e\x001bÒ¨çvnðXKO`30t¤x^ ~Ôá\x001e¸\x001626\bUck°xUÆÆDcP\x0007:`\x0015¢\x0017b\x0019¦ZÊÍÝ;«\x0017\x0018lö\x0010°yöB)6Ä`â§\x0016\x001b$ 1,h\x0015tÕØ^SXÐe\x0018r¡Ñ¹;Øf\x001a\x0013«,V\x001fXË\x0019ÏØM§;¶êÕ
¦[K\x0012§ÑÖcK)kÌÓ]T.\\x001d\x001bõ\x0006Òð\x0003ìpªèäª*iq³\x0002]Àrì]o¿ZìðXbØ'6¼FQV\x0001R:òYÒ\x001bf!~*¹
×\x0014ç1Ð¢0e
:Fq\x0007ßbº·ïnîï÷dØáÿ^mîï7ï¯Vfµ¾}·½»"Àa.ÊðºãØMÑzÉJJÅ
ªQë\x0017éÖ'ÏÏNO\x0006SQvàQ]¹	¹I¢K\x0001Ü`~²÷\x0019¦\x001d©dÁýñýÕo:e¤Õµ~Ü^oÞþ4çÊ$fX)\x001c*,\x001d#¥"W"2¶\x000eëcýìûA÷7=¾\x001dÞ0XÁ\x000búá(=ª·Bz\x0015¥eJ=¼\x0005çóãí[_È·ûxÓ\x0001WÃ\x001b.Î!¯8Àª#jµ\x0019ÃfÃ|ÜT8RË0Ù+._¬êõ\x0004;-½I¬S'\x0019%§Õ°c\x0014Y59Üg\x0010.Ä¹¼T\x0018RÃk
Tà$ÞÜ4X	AÓ\x001b³k\x001añ&|\x001d¯cÊo¤Æ6\x001e
uäíÖ\x0003´\x00045óë
¼úh«	¾¥¶yaùNKòîK®.º*<vù\x000bó\x001b\x0006*ÝRýéÕúñóö]ç¢HM+¡ïe½{x\x0017òPÔ\x000bEJoÎ¢_@)?¦ÚVB\x0011ßËÀ{zqq8èéP§ã÷ þtõûæãûèiáÜ\x000f4úi³Ý^]oa±ÌÉÑvÝÎ£4cNò=fH3Æ\x0016Qß¯ÏÎ\x000eÎ`Ý\x000c¬<\x0006\x000e¡øi3\x0008)°á43á¿\x0013e4õ]òÅí¹f\x000c\x0000Ê`ÄO\x00018¯°B¾}*¶1\x001e¸\x0017ÓÅ6\x000b\x0006\x0001\x0011k!u³Apjc¨µ=ài\x0010Î»ìú\x0018¹\x0016\x000f"ê]KÞl\x0010R¦Ì:ÐkdXÆm ÕäÊj*g\x0001Ú°É/»Õ-\x001d\x0003sTÛ§¬b\x0006\x0018¥~2üEµ}s\x0007\x0001éÒúN\x000b\x0007aÃmmS¶y\x0010VQukT\x0006n=\x0008\x001d~àOâ§Í  U\x00063Ö\x0005CÌX\x0002BÒøNís\x0007ñó\x001fúãçT\x0001mÖ:ÆÙñÝ#\x0008ñ=\Ïª¦\x0013aÕ£vi8ª\x0005º`\x001dÈ\x001b \x0005!Ý&d@\x001c^\x0008ßÅÑ`9Ý\x000eâ\x000bØÖc\x00007Ä\x0000be\x0017RÜhK°u\2õØD#7vV`T\x000fÝ\x001b\x0012TléfÐ(Ìx*r¡6°E/æin÷nóÀÞ|ÅI\x0005¾ÌõÍí»ÎL)¥Ç&\ªø\x0014Å¢d\x001fë±
èüùjýr}ò|Ä¹#\^ø«\x001e\x001dt\x0017Hìm,'qR5\x0012ù[Î!÷{(,eOýÝ£²W8Ø1ÑÍ2R&^ôP÷³ïo¿R§û¸zõç?ÞlÃ\x0018 |þúf^^¯­Ä¥\x0004åR\x001bIeÑ\x0015\x00189«WOÏÂ(Vë£ã!·K\x0007¿\x001f.®Á7ÌPÏæ³c\x0002ñÃO¤$··?5ùÔ¼¥\x0005¾VÙ:\x0003-pq\x0013¡HÕ¶(h\x0006=\x0007¹\x0008®t£Å£ånö9\x001eÖpÒÁçc9gËø¿hBPÅÏX¡\x0004~-n­V¦¿,3|ÿÑm´¢\x0011ð\x0003¿^ÝlÞ^=<¤sçÙæúþ~nìÊË	Å\x001c!ü\x001aú9¡Ð \x000còHüþÕñúÙáÅE:x­ÎÏG\x000e\x001d=Dñà¯\x0016ô\x001cuá8óâ©)$é!ZïFbAsè½øøÇ=\x0019\x0008Ð\x0001É=[øow·\x001eç*4q'\x001c\SPT <@k)~Wýíôäï}©=OIg\x0000°øm4\x0000OªÎÜ{,E\x00118\x001aAA\x0011ÍÜ\x0011ÄÖeñÓ`\x00046ÊÕ@§\x0013ëÇ\x0004zì\x0015¬Ý\x000fàÛ\x0007~}ÛÇ<½ÚÞÌò©AF.K9+ðÅäò|Ì3?|Ì<=<;\x000e/¤Í»`ÉnÇÐÒ¥:\x001bÍ\x0000\x001avDÐÉ.ÜBx\x0006ªºR8\x001e±\x0017ÐAÓAæI8Æ8§Ç\x000fw#>êD7ýS¥èöl:\x000f==úéHaÜ	Få\~,xY:w\x0002D®Ù\x0012:æwn\x0013uOCK¯T¨íGÚ-Òþ\x000cüõ?é'ûùFÝß|è:\x000eâ}Mx\x0012¾}Éê85êâV\x001d`§1&éªUb¤T2^VxÖ'á³Ëã!Çíoæíî*>?^­^Ý=^m\x001f®\x0001þ»íæöyI¡\x0016\x0012ÖÉïðae}~Ì*¯Ç½ù¯N/\x000fÏ.ÿ»³õÉÿ}4ô}Ø~ðo pOÉ\x0003ßã«ÕË»Ç|Î¿¾¾5ñ2âxË:pìkù \x0016\x001d>¼\x000fW/O/óAÿúèxpêÙ§;þésç5~\x000cÖäÍ»Y\x001dÝã\x0016\x0012oaºÁ{Ý\x000c9eËifÙð[ðxµ~º~~4¼ë:i},\x0004ßW2½¼0¹ôc\x000f\x001cÍÙúÎ\x001cÈôJ]\x0006	½)mÁsU\x000báêÄ\x0006¹:<VG~ð3\x0018Ó¾Ñ2¬!äpÖb
\x0016¨^"ä\x0005>\x00072Õ.\x0014\x0016\x000bwãÄ7÷(Ö\x0016äHÂ\x001cÈd,4á2ÀP?\\x0006(à"1æ¨S½~=#8§ùâÍm96[\x0008 âq&Ñæ×|¬/Ç\x001cJ%.ÞÝV:ÊHñ.?¬\x0018Ê8j®G\x000eü9±hxùÎ1ØÍ{­ >)ùX\x0005\x001dAb$\x0015e\x000e%Ú\x000b\x000fJf1«5üÀ9¶\x0005q1ªö#o9h.=)£Û.ýÀ-¦ 1	t\x001a\x0003M áí¹ü\x0014\x0002kÏ¤Â9LäaÚÓ\x001ckº6\x0003,å¥äý`\x000cæ\x0006\x0015\x000e4d\x000b7¡\x0004óhù!d|H¯±\x000b;Ì¥GÊ6g\x0010¸-t\x000eÃÿ\x000b¾°&Ñ^Öag5ÙÞ f#\x0016\x0018.ÜÙ©\x0004ä\x001dQñ1loI9ÒBu\x000e$fî-ÁBã\x0008©\x000eÐVS2\x001d Õ°ë`\x000e$(->ñ¡>ÁÃ/0¢\x001ai¤4#¡§9 \x0004»ø\x000cr\x0010=M?o®b¨,yaè¤ñ¹Ø\x0012£\x0017BNåK¹\x0013"Ès9ö.A\x0019xÈÅ%¸\ª*f.ÛçÜ
**ncTR\x0016éBHK¢$\x0002îa@;2}isïÀ¿E.?ÂÙãSMy0ÎH8ØEyY¶¹w¢¦ÇòsÈ\x001a|ÙB÷.hÞ(±ZPË1Yÿ9 å±ü rÔèGpV*Jaa6¡vÀ\x000f"ÏE¦ª@A±\x000f*Éw#ÓçP¢on!¥$
¼°.
Êñ;a¥u9âÜC\x001aü\x000b)ÃsÑà\¬75úÀ¤k-\x001b=ÊHjé\Rñ'ü\x001aR¨p.ñ½£Ä¾Ý\x001cÊ0Vµx÷xEÅ\x000cBr	ÖÂÑÍ£o3\x0016Ôd* \x0013!\á(	Ñ¶y7B\x001dªØ9\x001e3Â\x0016°<\x0013%*\x0000ëðài2:ÊÜ,?$êBÇäÔ"GaA²cmÔ)\x0001Yô]È	Î÷äÐ\x0008o\x0008MÉ©k´7#I\x0006s(VÐáäs±µñßÃ©\x0019\x001b-O	Ïô¢àJ9:\x0014%ü\x0018SsEþöËý­ÄS¥ã	'æ\x0015uLþ<g:eê¡\x0012ãC\x00013Õ+e(/IíôCêü¯Ãõ\x0007üÍm¼ Y9üõü\x000e$70§áÏ¼ÛÎ«muáçOÖ&4È ` ÝÁf\x001e¾ÕÔ\x0006&4\x001c>?;<\x001f\x0004çúáÃû_º\x0013\x0010&z±ÝÜÎÓÌ62IQBdHq\x001c\x0018SÊÝð\x0004CdèÅÙúäùn!Ð/(õñ#ûuÃ\x00001SdfßlPÚ=àØû0`¡lg2¼\x001dÙT1;$µúÆÄHÀ"L-\x001d;x«XAe²èFÄÂJ0ßÜ|üEwÝì\x00013üÈ·DABSÊ\x0010S ¦Pºr1°4\x0019~æ¯\x000f1ùß?Ë«½Cj³:Þü>ë¹\x0019UR5£Àµñ\x0014¸æbDMàx½:^ÿÛá ãÝ§ÇÏbÛg|y÷¸}¸ºÞ&áµ2+|á\x000cVV:\x0008¸ZWi\x0016·\x0013#·^^]\x001c\x001e%ùµ2¼\x0010øÆÿtÕ
]-ÔÐ&y;Ã\x001c;Yå\x0016ÊpG4k\x000f»b¨\x0003¤à1ÆËî\x000fbô%§=¦åûûv^ãèè\x001dI\x0003\x001e\x000e0lÈÉ)ãB©Ñ¾~Qâ(.â;ë¶¢ßgÖ=fý-0Þ<obÃË¢Ëlþg33AÝ\x001fÄpCn÷ølûx=ëÚ6è)\x0010\x001fñ8\x000e\x0018bZ$èä>ÏÎ.Î\x0007qéâ\x001aS\x000bþÈÅÆ¡ú²1,]ÆáùUÐF9ñR\x001aÆ\x001enøYupAÆ¤\x0002W»\x0003r_MFmÊônzÇR_JhEgÏÁZè5«\x001b,2J2Z@Zx¼õrpmKº~óÊ>¯¬âu²\x001f$ø-\x0013®É\x0001ÕáúþôúªéF\x0010ârõv­ÔÐÅmW÷yu\x001d/Ðr\x0005	;\x001ayIäÇÈÔ§"^Ù_¾²nùJw[°Ê©¡Í	ÝF\x0012ñÊ>¯¬ã\x0015&)m\x0005\K!J+2­\x001b¶ÊhmÖVÑ*¡aÉÆÍ\x0006e¼éppÊ`\x001ea#E¼Z÷.6øm\x0005¯VÔËC¯\x001d\x0014£ô\x0014z	W,h>ÂË÷.âøû
`ÈÃ»Âk\x0010~\x000e¼^Yº*ÜÞ~\x0019nÿ"¿¯ÁµÑÃx-ªÁ{MÒ(:6e©áÕ{Ó««¦W)FÎF®\x0019O-º\x001cH\x001cKò:¼7¦­ÀÄÍÝ\x001f<ékÃ=ûéÏÿwT\x0019^yÉý\x0004ý#R}"^i½-j¬\x0018~yr8(EJè®îªÙrNÇ \x001b§E°$HÏÉé¶¡\x001dúÙ\x0004ÏmÞmýÌ\x0003Nk¬ú|\x001eþX)?âóKï|ÞùzzO® hFîm£\x0005é|ZSÖÛ²>J]zo«é\x0015\x0005P¡*\x0005
âº7XO)­m7÷Bë.½Øë+º\x001eÒ
SÅ\x000cÆ?Â{jñfåHåö\xÓzaê§><©P¹&,qÔ¢4JXê\x0006¨\x000bÚ\x0001\x0016Óû>}ý²g\x0002Íkè\x0000Hò\x0016
"^IiNÐ\x001bóCRgÚýAÖiz\\x001dßÝ¾¿ç4\x0008ö?6!¡xÌ¶$	!ÝÞ\x001cú\x000cOO^\x001cv}v_\x000e[¨\x0003-D\x00155¨g&s;\x000eGëAìÀ=¼M÷±G§Z².5$\x000cUPC\x00025:h¬'÷3è\x001e#ôM8\x000bÚö m\x001d´ÆL§\x0000Íñ<\x0007S¦z¬ög\x0016u8l»«ÚUQ3E
Ü88WRF=É`©±DYÔZv©µ¬¥\x0016¸¬Ãs]Q\x001d¥\x0015"Æ\ s¨;Öxø¥15Ô nâ1ø£©x!+,)1&£7ï\x0008éZ\x0001Ùò*êðÌQXÓ¦=«mx\x0006QM\x001b7VíÍµ­ë`\x001bâ;C
AêÌ<âcÃÜñC\x0006æè\Î\x000c\x0001wi=ç½%6Ðõ\x000e\x0010øm
µñ\x0007nÆ¬Wï(@\x0004²&°E\x001f[Tc§rf\x000e[±àÑy¬	\x0017ãòÜ,lÕ»Ïá·UØ
b83\x0018@7®lifØ!£ØºwÀo«¬'\x000e¡CÀfP7º!¹^©\x001b]3¼ÍðÊ{Æ\x001d­RÂ1"#Ec9ó¨uZ×#\x0002ÕV8äð0±¿#\x001b­\x0010Ó3ùbW
hÐùÀ\x0003[2PÀÐ*"c^ì9Ôý\x0013×\x001eÙâæd¸¬°/ù?p\x0006¶à½Ë\x0011~[uh*£dI©/bSzdÀ\x001e\x0011Ø­{\x00166ü¶
Û\x0006<\x000bg66þqNá\x00059Rê;\x000bÚöðÛ
híÌÑ\x0008m ó/æÒP\x0012#e³¨]ÚUQ\x001b)H¬AI\x0004êe)R]\x0010·¹\x001eE?Êýhb©[Â¦JÌ°B(\#ìHnÝ\x001clÉzû\x0011~[­mr.Åä\x0003Ûæ\x001dI\x000bE­{¶HT^­ \x0006¡\x0008ï\x0019þWë´Ï©L(©}\x001f»nè\x0000grª õr1äÊ\x0011#Õ]³¨m²mÝdsu5)Á\x0011o\x001aN\x001c!&\x0004:±}ï\x001c}\x0014jÖ\x0008Çv¹Áîc¨u\x001fÎ\x0011ç(áQ´Y#Jô¬\x0011%ª­\x0011ì
å¼À0u\x00123óá_ÑdÄ´Â®[$¦\x0019ÖØ#\x001aÕ0xX/,?OföXã=ìÁPQÑ	ÕY%p'$ê(Ür{õøëÌKIéáÈÈR\x0004ÖïÀã$*¶\x001c^¾ÞÉ¶ìãú\x001e®¯ÃÕèéX$XKô\x0001wDÎ£\x000c·k6©­Â\x0004\x0006\x000c\x0001E,kÇ¼¡\x0018°x2Nã\x001aÑÅ5¢\x000e×\x0012dY&5\yv'Öð4®í-\x0006[·\x0018bÐrÇ4¶×fdIk3¢+ZFëdÖÉ:ZM­G ¯E\x0010nN·0#½1
qu\x000fWWá\x0006(kA¨¬LÆ±\x00002àä¡\x0017áòN6@ÀßVò*O\x0006%ºn»p2T®\x0006ÎD·n¯A=Ë{M\x0011¯Ùíµq\x0007G\x0001¯éó:^GRáñlÈùù¢\x0018\x0011Z)ã\x0015½{
~[Ã\x000b¦&ñ\x001a\x000cv:øu¾ØÆ
ûi^Ý_\x000fºn=XIÄNÚ$k
(Íªy}¿ùºý¦\x0005IÛÂ~S¸\x001còÅ6PH«û´u§\x0019$ãiÆY.Wy³M\x0004%
pm\x001f·În°äß\x0000×¡¤æyz'\x0002£¼)\x0015«³x\x0005	\x0019Æ
µy22áõI}.Á»LnZzõë©q,Q\x001büCØN±G¥b\x0005´a\x0019$9\x0019.\x001cÃÔ\x0019\x0010Þ"ý}!Æm\x0011­ïM­_>·jA\x0000$[à¤¸oÇ\x0012ò¦iu\x000c£ñÝ+HCDzSÝ¯Î6o®\x001eæõ\x000eu¹¡Ò;b0¤\x0014B;¢×\x001aS¯ÎÖO\x000f/¾B¸²+«p\x0003#:5ÃÖÊ¸Ú\x0014¼=Ú/k;\x0010×õp]Ýìrè\x0008fWQ	\x001bË\x0019°fD¾lr;7p ¥\x000bx!­UX\x001cÌ¡ÆÇ${×¸	{w\x001aW.®\x0014U¸&ÊlF\Ã©<	jbÜTÀi\x0012·\x0013iÇ®Â
PX¢É¸dýgÅkw\x0000×÷®¯[ºZIrÕ\x0001\x00152+¤µbÊ92EËEÿ\\x0010\x0007\x0003£w»*+¸qº']Ù¸ÔDÀ5¶víbOì[OÚÇ\x0002/
;¦G5Å+åW\x0004\x0012Ãm'Ñü»»ÛÄ5ËÂñ,÷4J|4È4&	6¶Ý(Ùü»ÓôO°;\x000føíd=¶FùØ\x0005\x001fmFS+\x0012ihÕVÕÐ\x000eë&\x0018èàQ\x0011\x00166uÐp#Â6_¡þòªKØ¾7×þÿçî]ã8lÑ_©Ù\x0019	\x0016ïqp¬\x0000Ö¦Ð\x0017\x0004pðu	­D(h\x0000\x0005\x0002ÜFý\x001b=;vGÝwpBÒ_rÃ#Ü£2@Tä#wj3e#)mby¤?7¯µä¬Ïè1Y\x0000ÌíèLpQr9tµ¹-`Ãë\x001c¸q``H\x0007(hêâlHÓ]\x001flÓ¹B\x0016­\x001fÓ`\x001b\x0007Q\x0008\x0013§rZ$!Î
òLÅxM;nY\x0018\x0012#-wTFÉ·Xßâ1XÕìkIÞÁ°M±'áµ\x0019¶¦ì±ZI¡6
a9líÔ\x0005Ü6Öµà,\x001cßæ)pâ>\x0014\x0018f^ÖÓa\x001b^À6¼\x0019¶$\x0007i§(´- Z1öPØ0°k¹om\x0018Ù\x0012-²\x0000	u	Õ2¦qëòÄÑ­Ú\x001dqk\nFùé\x001boVÒÁ\x001d«\x001d·-	¼¶â¶\x001e£Èq)\x0011DYM½5¾2Æt0n¯
=Um¸Ò5]
Ã®SïS\x0010±«fH+g\x000fl\x000esºGeÓÔÛJÒ2\x0001íÉ¡S>#pS«¾\x0018»ÛI\x0003¸c+M\x001bn\x0011î3©ò\x0016
\x0008)ì¥­ÃCGU¦\x0005
Æ-ya\x0005ã{+n(9K}{á2\x0003ÅQ\x0011·Á!RZâPàêÑ«\x0019\x0016\x001c\x0017täÂñÐº\x0014\{,\x000fW\x0019\x000cJ¸=\x0015^U|o^q\x0011oámðNÐ Ä4uâð±róý4n+\x001e9±¢yg\x0006rÁ\x0001¸±à'î\x0008%¹\x0005¸Ò%p¥\x0007¤IZá\x0018/Ë©­Ë!|-½°m¹3­mÞÐ"fÕÙ°òZ\x00115\x0003Â®\x0011½
FíMÚv;¨ý\x000e×\x0007'ê­±o\x0002F©Í`\x0008.ÛévChq^¹ð\x001aFÄ¤õÖ\x000e\x001d+¸
µ_\x001b`Â]\x0017x|o=1a@LÄ
iyLÃ*\x0011vaÕ\x000c×\x0006(æ,qfMá\x0011\x0019\x000fûR¡¢Ñ³\x0012z\x000eÜJ\x0015v0¾·*J¸\x000bÇ@«p0Q\x0006Ç\x001e+Á¼6Eá©]¶C
f\x001e1#'\x0011TÊãå+Kÿ\x000c9SPi\x001cëtú"àÎz4Ä.ºØÅ·]v±Ëo\x000b»êbWß\x0016vÝÅ®¿-ì¦ÝÌ\x001dGV\x0015Ø\x0007q
\x000cÄn»Øm#vÈ*Lë(K­Áû¤<ImÞxì®Ý}[ëî»Øý7½S!ÀS@Ò\x0000ßªÅlU$\x0003JC\x0014\x0003ÖWHÞÆc/ÏÕÖõÿ_ìÅ¹Ê[\x000fV­%M\x0019\x000cÎ\x0016µ1XC	Ç+ÝÂãÁ\x0017\x0007+o=Y5Pa§ô<ôòcÛÍÝEN\x000ec^\x0019\x0006^\x0014»U4o×\x0000\x001eI5Î§\x000fWiGµ\x0005r\x0010ñ
Q;ï¨çIØu¡ñºÙtbÏ¢©Ü2b·4\x0003U*zFC/\x0014^7{@DÈyv
\x001c\x0015ýYViZ\x001c\x000bÝ\x0014ên\x001dIg¨ôK\x0001\x000b8­:iåâ±Ø]Ý5oU&ö\x0004Ï<r\x000e·*#\x0006s++ã#±óÒ×V\x0013kî´nKÂÔ|[\x0015ÊIÃ©ÕÎh®h^\x0016\x001cÇ\x0001\x0005ðÊl\x001dã\x0006×ÁËòdÍG«Ø\x0016Ü`c \x0015¹Þ¦\x001b\x000b\\x0017n$¼¶ú\x0004x!´2XE\x00186+b\x00053Û^å¦ô	L³S\x0000ºdh´É½Á£¡¯tMÄ.Ê»G¬ÞhÃ.=ÕÀiM1Sk\x0015õ®{0\x001bøRÝE»º+K%ÞP³å\x0010¼adh¼\x001aãÐô/W^6¯|Py+\x001f'F®$5Ø
]ÎXì¦\xÓ¼ð¨+¹az\x0014\x001e)ü»S	µÅnH\x0001¼6bw\x000e{L ¬#4µHr+Èc±»âd×Öu§aA\x0001<#\x001e\x001aë¨¾ÈÉ\x0019\x0015Þ\x000e¼k>Y­§1Ó±­\x001a) `:×¢®±à}áÁk#x¯\x0001ÈÀ¬\x0016KìgÝÌ§ñ²cÃk\x001bvÃ%të$ì<Ó¥(Ã3øY\x0016Þ=\x000e\x0006»n0xê´\x000báë\x000bÆh-ó\x0014\x001eSµD\x0002ß\x001dxñeòÀ=\x000e¹n`l*n)ÅCÒp\x0013\x001bRq§#pw3®\x0008ÎL\x0006þD¸äqÑä)]ñô\x0014ð'¦¢¸ÇÑ
WD7&#w4ö{Os;834êKUJ¸Ç,¹.ë\x0019[b
%§¾PF\x001eaÉÇéÊÎ%·\x0005rÛ\	Hçácû­ÈË=ÇjBÁÅ\x000c
®dGÁ	3-u-÷;f©»3\ùÓ\x000c;¹qo Sÿ\x0007üß\x001cë­õV3¬·ÖÔ\x0005\x000fÛ\x0012ËF95V\x0004CØ/\x001d[\x0015¸Õ\x000c¸³³Å½¦Ñ\x0019\R\x000cFÕh=F\x0000×Å¦Ô3lJ«IS\x0004ÃÐ«­I¥+~\x0004n[à¶3à~\x0016:ê±Ã"ONPºR~9\x001c5ç¦</Û7¦\x000f×\x0008%¶\x001e
öXp=\x0014=ÇÆìvg\x0001rÑ~`Â d­¼AIzD.¥ÍkÞ\x0007\x001d¼Óc\x0018Oz1\x0003r¾Uq\x0004G\x000eæ±d¯°ÿ\x00167\x0000¹.µEÏ -\x0010F·\x0014à\x000cÏVe\x000em\x0011¥?\x000b¯È%p\x0016¦æ\x0016Î%"\x001e¹µµ²ÀAÈ\x0015äÑÓ\x0007<ÚýÛëÍçõÝ;Àn\x0016ÿò\x0010¤à>\x001aü\x0011÷\x0008As¦\x0001xy2ët\x0015:ýË£Õ\x000fË³ @\x0000p\x0019D\x0000vÐi,
"@_Ñ,"{\x001cÇT\x0018È(%)N\x0004Ë\x0015\x001f-+$psI ó*\x0018N^g\x00080¥­PH ct\x0004`sfEnüDQ¦É\x000b\x000bg8©­$ÄFÀ\x001fïÙ¶'\x00020\x001e\x000e,zä\x001cSêJ3ãX\x0019JEâ³iil\x0011gÎíá;æ($U¥ôt¬\x0008ª\x0014AÍ&\x0002Í áÌ
Ì
\x0007\x0019,±ÝÉÊ(±2R\x00063\x000cÒP\x0010m\x0007B3J±J^á\x0002\x0019)`¢4ªsíh¯'\x000c!dTñZ%YåZ5B8ö³+}Q¸A\x0017·7ï\x001eF\x001dÇÎ£\x000b\x0004;\x0017Gº8ÅÈ\x0012ñA\x001eÐÅÉñËËpe\x0017®lk
E
Âáô4ÊE8ÓhêÁ«l\x0017¯²M¹aB\x0013×Ö³À+¾Â0¬\x0017kËyÛê\x0013,
@ÓÜD«c¸¯ô¡uX·!\x0016\x001cND\x0008Ëñ&u-³jë\x001aGÛµm8 \x0014KcÇ"°P\x0013\x0002ÿ\x0018^d5â£aU×L\x0007
6®	±«QÒ
è?B~<ÏÉD@/f3b_"ö\x0005º¸ÌZG\x001d\x000e\x001e&
$Ä5N´}¡Ç±Ë°\x0005±¶¤Ç@Ðù	ïdÖ
çÜ0Ä¶ÔcÛ¨ÇçÉ}6OÜõØó«Íþ\x0003\x0001¦Â6
+i°L\x0000ì¨\x0000\x0000\x0007§\x0008°\x0019\x0012«"¶ÅÆÓÿZ\x0010{8¸\x0017ÉµóÂR¨w¢U)+6sm\x001bÏ\x0015Î-
Bä mL\x001d4\x0002îP'\x0002`ÏÛ\x0000s±Æ\x001bì	õqÜWZa\x0018Ô\x0004wëüáÀc¬É¡\x0008ÓÔFèóK\x000e×Ä7/ÃjÌY'^\x0015!\x0001«Ñ!RÂð\x0000NñÈ\x0003V
"Ø¨ç
C¬K\x001f3¾· \x0016á^H3¨,°*\x0002`')'U½\x0017\x000eClt©\x0016F·ù\x001er\x000b8\x0015$ÜÆ\x0013Í×HV'Úxäñ.óJlTÛ"sKõÌÁÖÁ8ô¸Êá*EÀÖSÛG«lÛV9¸O\x0014C\x0008Lé\x0005í\x0007e¡v@ÖowÚ¾(ôþØ¬\x001f~\x001bs+
G\x0005+e0ÍèÐ³\x000eUp\x000fËf¢#ûß«åå¿îÂË\x000b¼¼\x0011°S[.fIMú\x0010\x0010#À=3@úñvééÂúÊF¼ØôÛØá½\x001fì\x000fâí\x001bHÑ\x000fX\x0016\x000b,\x001b\x0017Øsâ]\x0005ÆQólKn¬*\x0003\x0002¶\x0005`Û\x0008X\x0013\x001bs;üÅy+\x00150\x0003\x0001+Ö\x0005¬X#`G#Pa=ªáf¾=×É®\x0003`Þ\x0004\x0018ÑÄ/Ï|\x001e`è¶¤U\x000f{ÿ\x0000À®\x0000ì\x001a\x0001\x0007O^"¡¸\x0014`>Ç¬´±Í®3ÿ%\x0000öª\x0011p®\x0001ÌAKF*º`Ù\x000cWr»Ã\x0000\x000b^5Þf×\x0013[%ö{F'&·y\x0000«\x0012pã\x0012;ç{\x0000)>\x0002ös\x001d\x001ba_\x0017pEU\x000b÷\x0016*}áâa©NÁÒ\x0004]£\x0019\x0019X>:èÚ4Â\x0007¯á\x0002K½D;Za3¡¹
¸Ã@\x0003n[bK=gRhÊísMiN]%´\x001a\x0006¸´j¢Õ¬Aç\x000b¢ñG
ìÈ°B\x0007]3`_\x0002öm=g4õoù\x0007\x0019\x0017³ÌÂ»Î·í:\x001fn\x001cr;)\x0001'©\x0008æ³wYÉ\x001e\x000cC,Y¡Äqø[\x000bb¡¨þ\x0017Æ\x0016a\Pp'æCÌKÄ¼\x0011±ÌÖ\x0018éD\x001e\x0005Ô®\x0014þ%oT
\x000b¯\x00000V/)åæ[áG\x001e|£\x000bïµ¦F1ð&0Iäâ\x0001­jÌÃ\x0010¦X6b\x0018ôîiøÄÞN\x0018¾Ýw­\x001e¦4i¦Ñ´Yý\x001f\x0008\x0011¢VäÞ$­\x0001ÛR)l£Røm\x0011\x001e(4r\x001d{ûN¹J\x0019ÀPÄ¦DlZ\x0010K&òpz\x0011®LiJ©\x0010ëH²Ø¸\x0013Ý\x0006ÄÎ7®q.ù¦
K×ØvvM%É?\x000c1°\x0011vov®É¶IÆDv)\x0004wÀÛ0\x001fàòVm'´d0cg»ÄØï"Ù\x000eA\x001c2Y£X³ÂRhÖd)\x0002bKí"ØQ=£²3"Ö%â&k\x001c6Þ\x0013[ÛÀJåJßhô~Àå	­ÛNèÈ\x0018-¶³\x001b-Q/w\x0010·zÆZ\x0014! -b@\x0001±Ë%æèøÑÆ=ó\x0006 ¥\x001aËF5T\x0007\x0004G4Â\x0015j¾\x0005.o£ºí6\x001al®ÉmP	ÜuåUß\x0018ô*b\x0017\x0003Å\x001d%v/èÂ\x001f-\x000e®×Ww£¢:çg¤ÜNwe4eCÛJ.\x0017\x0000/\x000f/\x0016\x0007GËÃ³]¥é\x0002¦
°a´\x000b\x001dÕ©0íZß\x0014Ý\x0001;\x001c\x0001°+ìóÅ#hã\x0004¬\x0013u·x\x0000à\x000e£\x000fþ¼
p@Is2ÄÓÙú<ÖÓU\x0018Û\x0006âí(\x0007¼µáµÛÔ\x0001PÌ¡
\x000boò\x0002×â!E\x0001X4ª°Ú\x0018 Ð<7Ï
"vÐ®­\x001b\x0008Ø\x0017\x001aá[5Bf«\x0016´9ÝìFä=ç{&{\x000e\x0001\ì9ßºçX\x000el\x001b\x0001Ú¬ÚæCëf¸\x001fp·ÕJc«UN8ê~\x0008wÄÜý eE{Ýª\x0013\\x0014:\x0001¯mõ\x001e\x000e 4\x0006\x0006}b
\x0006ù±é¿C\x0000K,\x001aØnO°Ú\x0010çùm¬'>1\x0000±Ô\x0005b©\x0002Yá¤U4\x0010	J\x001fÚx£]	Ø5.±¤&*iÝ\x001eöL\x0007?÷Ü\x0007 Vû\x0003¯m\x0005VÔHGéíX4Ã{FB\x000fÀkK°*Î°b2RDq\x0008\x0014ÔÍp}	×7û\x0012i
F@ÌòÜ¹\x001c7²gÄã\x0000Ä¾p&àµm\x001dÎoãÒó<ØOzÚs¢Ù\x0010¬@\x000c¯M#&@	wT@¥\x0013Fôd\x0019\x0007 æ\x0010¼ÑLx=6/³]3yÛ	Ùzv\x0008Q"\x0016mà4\x0007\x0016Æ0Ðñì©`ÉHñ\x0000Ä¥)\x0016­¦ØåÒmÅÒV{\x0006í\x000e@¬\x000bÓ&t«i\x000b\x0017%ä\x0011	 zM­cl(âòî¬\x001b\x000f\x000fÇò0cæ)°­
3²ùø\x0010âF@lTãÎsXÏ\x001f\x0010\x001b¯55Û5nµÇÁæñFÄÎ\x0013²Ü(\x001a·</Z5»Â\x001bÏ¶\x001a7KQAÅ\x0019½g&\x0003®yß¹òüpmçG\x0000G] Åt~Xm\x0003jD\êkÓ	\x0017\x0014&13U@Ì¼Ä\x0006¶aä³Û&'+±S.éD\x001em\x00027}ÒâÚlªau¡\x0014ðÚ¦\x0014.óÇXûÂã¦kS!6%bÓK¸¦5öTÌÆr©ðÂ\x000c\x0004\Fdc\x0018È\x0005Mp¸ïäÖ\x000bÊ\x001dÒÁ(·"Vå_µ^ù\x001d§\x0004\x0018*\x0013¿ 8MO)Ð\x0010Ä¾DÜxÿ\x0008×f¬IP\x0010-F5T`L³o¬t\x0019-Ö¡+é\x000c\x0015ÐY*Ó%kÜ\x001c\x001bT¦pisÂm.wå°ÉÔõ¶';\x0000±-Ø¶-±vbuFL£Ô\x0002âÚ¨×a]a*àµ
qô.\x0013bÏ\x000fª¶2µ»¡U	¸õ6¶\x000b\x001bò`ÌS\x001e¬¯\x0012z\x0000`_\x001a
ßf(K±á9´b³1v=éò~Ä\x0015áÌH4ÙxÞ)Bl¶?t÷p\x0015Eá\x0004Ák«clqÛYNc¸¡Â\x001aã+Äù\x0003\x0011«B)´jT°Ä\x0010{ ±,OhÛ\x001eã6e,È4ÆätÖÂì=â¬´ªÙN\x0018¦K¼m:\x0001D7ñót_Î(¢iueLÑ@Ä²ðlódy¡9^Ó\x0012g.ÿ
³ù@Ä¦8<àµ	1ÌÅ5¶"wyP°ÍVçâ\x000e\x0003lË%¶­Kì:Hû8%<\x0001&¨õå\x000e\x0004ìÓÎøÆÓN[g\x001a\x001c¬Íó\x0001's¶¼ÛÙÖ»\x001dO*l ü\x0003¹V5Õ\x000b\x0002OI+âÒc³\x001eu6#6­M³L³°Ö\x001bOg\x0013gÃGÄib|jüÑ´Æ¶åxâMÉb'Å#\x0016»×w\x0001Óâ`ýé~Ì4S¡¬ÍÅ	Á8{\x001c\x001c·m\x0013´Ch»\x000e¾_Á¿8X_<55âïH\x0016/,\x0007?ðØPõÅsk\x0014©ör±\x0002ÈB\x00009\x0000zÛ1\x0006T·4©RosC\x0010	 \x000b\x0001ô<\x0002À²o\x0003 8tÅäþù8Õl&\x0001:eÉA\x0000¨JE\x0000N©\x0013Ë&5
\x0013j¾Òx:N\x0000Y
 gÀ(C	«9
Kr6±¯Q®\x0000>fGømg ,w¶øÖ;\x0004h>]%ü8N\x0000Ý)Oæ6¨OA\x0000èTMfÔJc \x001dwDìEeòÐH\x0001:$U \x0000¸\x001bs\x0008`
\x0005Ù­Ê\x000c|áÛØËJ°o¤\x0004¶ü\x0004v®O`©òÒêL£É)íUeêÖH\x0001\)I\x0000/Å!VÖ\x0018ì\x000b¤(7Éâã$0\x001dz\x000f\x0018UVòO6HàhÞ\pÛ)§+räÊ;=×il\q\x001aÃë<Û@Qu\x0005\x0003¨_\x0017Ü·$APl\x0004V\x000eÇ#r :(PpÝÆî¤E:¢C8@Hà:µ8p\x001e{6\x0016aÖ\x001a®"-r$Á\Jä¼)\x0005k#3.:£\x0002ÑW2ãÐûr\x0013û¹61\x0014f xE5\x0003ÜiKø+­³£\x0004ë~Wø>\x0004I\x000cGCm0ÅJÄÜ V¼\x0012z\x001c,\x0002N\x000cÆ<lÛI\x000eÖW>]mîFM·rÁ\x0001E6k\x0003ä_x
käÚSNô¼x\x000fÏÏ\x000fWgçOÌsI E\x0001Z4£\x000e\x001a"N\x0006ZÛÑàÐ\x000cì°û;(·w¬sçö\x000b]+äà¯IÂ¬÷ò\x001cÆéï¶îÜé5
·Õh"dO\x0017-lú¦`!ûÛ£zAw8}+8}¦ö¦Z\x001a¾µ&ªM\x0002þ~~Ð¾\x0000í\x001bA{Æ©%Æ@[\x0017QJH1Ç+cs\x0007îDù@ýXóJ[:t\x000cÜÃi¥\x001dmC>,§\x001ft¡\x001eºU=<Óy\x0012!°ä£>¯´îo ë\x0007]lDÝº\x0011=³Ôm§±	"C\x001eÐiÛ\x000bÙ\x0014M3äH)\x0010k`­JmÆ<é06­&\x001a0Ó\x0008h¸W fRg6û \x0017²-\x000cm6\x001cÁá¦lQ0|ÄEí\x0006\x001bÀ%Ð7o>½½2ÙáÀ\x0016\x000eA<®ª¯[q\x0010bW(s\x000ch¶!¶2Fp¨àá\x001d,`>T\x0006p\x0014õ¢öå:ûæuª@t9\x0006»±évïj<£CA\x000b^\x001c*ðÚºÔ6Ô¶æÆ	Oc(£¦\x001dµ(\x0014Df\x0005q¹\x0006ÆQ'm\x0007£\x0008u%\x000e1\x00005×Ñõï\x000cé\x000bËÑ\x0019l»¸^ÃXªðÓßnoî\x0003Øq÷\x0017á°-\x0012Xãýq{ËÒ\x0001½£%Ì§:\x000e?ýíäøbyx¼½Äàÿ,ï
äç\x0013(¦ÇÒü	Ë%\x000ew\x001cèë@¬#¨\x000b´~\x0017nw»$ê4²\x0004¸Q$-:ù°1$)RVU¨J²á\x001béBéôZç¡ä¥NÄTA\x0015µ\x000f M"-$²3#HRs×v>j\x000cL~\x0005\¡unN­ËÉ¶8'´.#îÙÔT¨Ó_\x000eÏi\x001axêÈdàV£gºµ\x000c¼F\x0018Õ",\x0004s
DÕ!\x000câP4Wäé5_ã\x0003ñÒtÃë»c¨$(¶&\x0017çÒÃXåð\x0015Dâ¥×\x0019·Ær
\x0016)PQëÏ"Ù
éEHåWâs~%åð¶Ä1T3¹}¹ªà6HÔ)ªË¢Í\x0012\x0005/\x0008ÕN
â\x0017dÇPWÒò
\x0012ÙÒe°3ZohnS¨vÒå&MáI$1`ñxDU*\x0004¯ód=ÆBÂYjÈi`tKç\x0015þà\x0006J'HÌê\x0005Á@!\x0002É<ÈÐPÓK¤Ëþ
">Õi\x0010\x001a{Ü¡¡ø÷`^\x0012zßC\x0006ø\x0017IB¤HV0Ú\x0019«å=rB\x0001c\x0011M©ro\x0013Uy(äQbÆO$EM\x0013\x000c¹£¦Ì|ãS\x0015\x001a\x0006|)Q$\x001bÎX_ÉYÌâZOÅôðé¾D\x0015\x0007\x0012¼Îê\x0008¥^-f¼¤¼4)\x0007\x0015\x0007\x0008}
?H9]Häô\x00129eWÌÜ}\x0006(°_ã@R¾8àu>¬BÊÜ Ú£êw%\x001a0;rDZ\x0014]Ò;ùGÖ»Û{a-\x001eîÆ\x0000÷\x0006H$ÊÃQÅP­ueîÓÙÉåÅ*pyöDÒ:¢UÝVÜ°\x001fc+îT´\x001cÜ´¸+anpáéemÚZöËtuëx\x0001×ñg
Wuk«Òê\x0006¼À\x0011uAA$æ<µ[Ú:KF]\x00178Yê/Å^È®+õi±¼ºÛËB2E¹1\x001d\x000b£f}ºX/\x0007ÜCÎ\x0017ËÃ³U§~á\x000b3Â\x001e%É\x0002t#Û [§zB[¹G#(S\x001dþõ#x òî%½(î\x0018S\x001b\x0005}>yÑÑÁÄ0h½\x001a`ôAçÝË\x0004{ÁËÄ\x0014ì"W¼èp\x0015·H?é\x0018U¼\x000cq·\x0007B%tÙ
¹\x001bñ\x0001+ú¡gè\x0015Î/°ï<1#ôRÕy«®\x001bkX^Ã¥4µ}xº\x0011\x0004Ý\x0019¡ëuä®°/ðÚÜ\x0018t+Ã¢\x001b\x001cEa}Î°\x000eqý\x0007\x0001\x0017¬\x0000\x000e¯mÀS1]\x0002.SÊ:Gþ®V9\x0012zg\x0018\x001e@ç¢\x0011z¸@b{·\x000e\x0017ÈÄ\x000e\x0012ì¡ËÐ+©ËÐ;Ùm.t+t\x000f`\x0019\x0013!]@N\x0011\x0017à¦\x000b¹2\x0005reÚ`gN\x0013\x0013c\x001drÞ #,z
·ê¶$\x0007Üñ½mÉe¦Ô3ÌØ­Ê5|À=)cßà3òM9¦2ØÄbôéæþê~qñóïãÇÜ§±ÌF
o\x0015Ãù
ÆCÊ ^!¸\x0019¸\{±¸øþßº\x0019ä\x001dBØ®\x0010v\x0016!¸O\x000cvA\x0008'ÞUóX	ý×ýgÓ(!:)¢ D9\x0010yª\x0014À#\x0010Òb\x001d^8º´¢/1 ó0F\x0008Þ\x0019Á\x0018×\x0019¤ UlL\x0001òÈXm¬²¤P¶Rä¶C\x000eÊaK9fÑ©\x001c¾\x000698Æ?tÊ\x000c <F\x000eå È¡õ,r\x0018fe\x001cöe"\x0001\x0006jZuæ@\x000cïf\x0011Cò8U%H¡Mâ²\x0005F&B¸
\x000fÏ\x0014!\x0004+¾\x0005¼Î 	þ±yoøô-\x000cÑå\x000f\x001b\x0017=BÎm\x0017è^w[P)+\x000f$¦\x0013\x0010¾¯L³$Fgd\x0001¡ä,bXúÏàÌ°ÈbÇGbÔf\x0015N\x0011Cv\x0018¿\x0018ð:\x0018áZæñÔ\x0010
céFSû\x00101ïù-;åç ò³¡ãp\x0003\x0010ÃH3¦@fp¹û¯hc¤P²0Rð:\x0014\x001a®\x000e(µ8Õ×(FÛ\x000fÈ\x0002Bbgh3ËÎ¥¤`Gn
Soiø\x0018aE#Å1@Ô¹ÁI¶\x001dgþ°8º}ø8Æ\x001b÷@ÒTÆÂ\x00103Ð\x0008\x0012t_«Ëåâèäòô\x0016®\x0008T¨.P¡zbrà¹ëO\x000b\x001a`{¸Ã{vÔ;@"ºåI@ù\x001eÍ\x0015à4Dh\x001aR\x0004UÈ
0;½
\x0001PîU\x00003\x001c§HI"Ý~x1tO1z\x000fPS\x00005MëÉÄxä_\x0005ÝNïè)®\x0003í$;\x0002$¢\x001dmÔP\x001bg@ÃÍ¹§ì¼\x0007h±çMÛ§ÑÁèrQª¨a}C{p\x0016*jZTÔåiTPGB_\x0006r\x001aÖW¦Ý\x0003´Øò¦eË3ª'w¾|^Ñ¾Ùôu ¶øò¶íËÓ\\x0019§·F4s]rÞ¤¢¶øô¶åÓë=I@mlª2ëMß¨·\x001eq²-Æ\x0011Í0Ì`y+ö¶Ôúâøô
Ç§tÔ\x001d*½'\x0006gÑ\x0019dÑ7|¾
wbTà0;\x001di¸[x$éå2÷ü\x0001s<òyW8§\x0006 åÅÆ
´Ékºåñ\x000e
\x001a\x0018,33Pß\x0000>¤¦DÚ ¦Pâ\x0004¬<O\x0013¢ÃßôõEqrÑpJªäJÐ\x0008\x001e¡hÆ£Q"!@]	´Áæ\x0007'T -\x0014ÏèÀ\x0016Õ´Å\x001fí&#%&#§"5ø,-)#ê\x001eAC¢MÏ´¶\x001e68ÀÛàÆãtÎìÑ¾×Û ó\x0004\x0004\x001dmYP!\x000b B¶\x0000\x0004\x0014²XCdów=\x0003\x0007zªâËÃëd ^bv\x000bX-Ö|;6]Â]¡\x0000ª§û%\x000e&\x0015á®·"÷\x00169K§¯\x0014
÷#¬°ùð:y31NÙ+-8\x000eàtZY)\x0002\x0019³¼ÈËH8ï)/i(P¹/Sù\x0016×YÚ\x0012¨m¹5qbÐ0E \x00015Ä©¬+
Ký8Ã±ÜÅ	¯-=#¦_C\x000b
ÃÚè·e=.ÖSéõ\x0014\x000e«\x0003¹\x0006r\x001bê1'3ÚKðÛ´TQÕ¢¢ÁÇ§z*å1ÁuÎ*j+\x0005\x000fU ìqê\x0015©ßÍâú¿ÿý??®ß]k»5ûËB}\x000c®¬#\x0015ð¦2Í¹S;ºXî/_\x001eVzS\x0011¿éâ7Íø%Ó®;\x0019\x0017ùãÂõ">vHí]\x0007ÿ\x0008%Âw]øn\x000eø>G\x0003$\x0002i;¢"Ðn@u(|Þ\x0019«\x001dàÃk»\x0000Âì\x0019ô\x0018£ãXjb\x00061¦2Ôu´\x0000\x0014\x0010\x0008 ä\x001c\x0002í\x0001\x001baÕ©êÄ¸!u\x0005ð¥\x0000~\x000e\x0001øvæ¥Ûz\x0010@\x000cp3F\x000b K\x0001ô,\x0002¨ìÊ»¨MIm~6ð¢Ü¾ðÚ\x000e^f®'
¯Hpa\x000c¡ç\x0003RÒ\x0005à¥ùçí\x0007@\x0010Àï1,è\x0014\x001f,
`©\x0016ÕÊÊÈàñ\x0002èR\x0000=\x0000FW\x000bGá?IE\x0001A
qÕx\x0001l)À\x001c&TJâbÖÊP.@\x001a\x0007DÌx\x0006tÇF\x0001æØ\x0003áàeHZ\x0014´	)\x0007¤ãÙ/¯\x0004·F\x000bÐu\x0001\x0002H>Ç\x0017ày\x000fXªìªPÉ~´\x0000¦ðâÒö/ ·ó/<yqnáÇA]ZÃðÛr\x000bØY¶\x0000£¸\x0013f[4ByZ®õÃZ\x0001\x0007	 Maàu\x0016\x0001°pÕ\x0004/Â\x0006eÊ?3ã1 mq\x0008Ãë,ç\x0018â÷âå¤úUW¤Æï
7\x000e^ç9Æ°\x0000×+\x0001í\x0000êu¾2Çh¼\x0000®\x0014`\x0002¦©$E>{'=íaç*£\x0012Ç
 J#ªf1¢Â"9\x0010\x0012$Fç°&\x0016i>ã1¦T±áµý*ì©Æ\x0001ús>(L\x0002üù.2ª¼\x0007¨\x0019î\x0001j
\x000cP1\x0012ÉÉ«\x000eD\x0018+fÅúk6Çú\x0003\x000f0F"\x0014v¸C$\x0002\x0011l¾#ÀÈ2\x000e!g8%\x000cgMð¥ÂP\x0015Ty2ç%Ìèí\x001cèed?\x001dtNêo,ùp~Î@ëT¤B\x001cEª\x0019\x0004P\x001dõ÷t\x0011329P¯\x0018¼¶\x000bà\x0005\x000c¦N_@d\x0001|åà*9­\x0002ðBAµKÀ9 N\x0012Ø\%\x0006tÇ©©±Ä'%X\x0007óù¦ËD¸\x001f\x0006\x001dÝÞ_}ú´ù°¹¹_ì¯ÃO÷ãr j	\x0002`Z~Á±GZCVp'ø£ÃóóÕëÕñÅb\x0019~ºØ\x0016ùÓ\x000fù\x0003X\x0004Á¶'°`/:ÂË·÷?_½]o\x0012Tt\x0014#\x00172\x000cÄA\x0017\x0014Æ8ÔCÏÐtzrñýáAÙBõ\x0008yç\x0006	ÈÝ\x000cÐa|Aè,wff"'¡1\x000bôN\x00004@\x0017v\x000eè\x0006°\x0008\x001d§sGèÌ`":\x001cºý\¡C KÑ.Å\x000cÐ=£Q×B\x0011{V¸iQÝT0ó¬z\x0013\x001e Ë\x0019 »<{Wh½ç\x001d*Ï«^¹ð®T\x0017ºRs¬º£!lSº.©
LùèC¡b\x0019¶©eTË  Ôú3½\x0019yeHÆ\x0018ä¶Pu;ªÛàÒ YP\x0014#\x000fÐj(¨ú<»´3m\x000e ë9 K\x001aö'Â\x0015¡ÑT<T\x000c3\x001czøkX\x0017z|AcØÞÖÂXÜ¦ãã-Ìô#\x0012\x0001Þ
£^ð}äo·wo××¿>\mF·\x00042ñCÄ\x001aÀ%Äëbÿ­VA\x0012\x000bÉßNÎ\x000eGÿëòpu¶Ó#K"8_\x0000=Í"HN}8ù$)À\x0019E\x0008ÿ¢â\x0012\x0016¡ÛÚ\x0014D­M­"ð°]ñ+ðpEI·ZË½Ç¯ U%¿;^\x0004ÕO\x0015vX\x001cöÐ*Bp'S\x001dÎ\x0013\x000cn\x0015¶f)9|g\x0004²@Î!\x000136J \x0019r8Z®pbT¼6®x´\x0008Ú\x0015"h7\x0008\x000cê\x001cRo¸çDôlÃ,c°Psî\x0004Ã
5Íw\x0012p¸ 0ì*Þ×Ôå ¾!õc¹Ê¶	"ðÂ\x001eÁk³\x0008Vx
3xyjBöD½ÆjqO°³:ÉÐ-á
2\x00086\x000c§©ð\x0019@.\x0016c©\x0008
.Áóxügè\x0016÷\x0008n\x0006\x0011÷Ì\x0015jÃáãÆQ{\x001cÐlÏi,\x000eg#Û\x000fg\x000e,çØï
­¯\x001c©\x001e\x0018FË!%YqèF`ËÍ`çØ\x000cáH_A\x0007\x001f/UÎýÌEÍ'BPËÂ$Å÷omCB¸\x0019v´\x0011±]\x000c\x0010@UX\x00054G&1Q­\x0018ÿ!¼,?\x0004¼7Ë Â]^$«Ä·\x0002&jÃ´ä\x0019·´`åwïÍ2«Nâvpæ?\x0011
0ê&DÐ)\x0000·5¬½È×c â<]_ý6öæñ\x0013®÷\x0016i_µ¦"DÕWð»\x0002öÍÓåá¿~y;Kh9ï¢å¼
®¦f$á\x0015rm\x0006¸Tò¦cJ¼
®.àê6¸^Q\x00045gVzeûÚæúÑ\x0016ªÀÛt9\x001a\x0015\x0014î\^Ñ8`-ûJ{áv®Y\x0001®0mË©y2¦hq)k¨y_Çô\x0016î\x0013Ü 	o±¼¢yy5â
îÑ´¼\x0018RÐ¢Ywe±ÕdÛV\x000bp)Æjl8ÀÍåÉ¼Â"7\x0004n\x0011·ÑeÜfêf£å¥	?°×H\x001dD_EM\x001d$dÊÂß_²×\x001f7××ãH·¥Ê*¬}ÆL\x0013ºVBº|ðýòtut´;oàu\x0001^·7{\x000eÁÃ\x0015¨@©ÝR³¾ÞÀQèmÞ6£\x000f\x00185Åá\x001dñ;\x001bv^ûÞ¹#ÐBqÄ\x000c£iz(än,±°æüÇ ]Ïàw»®	½*Ð«fô\x00012ß®=\x000e¡`[Å©Ì{\x001e½ô²\x0000/g\x0000ï ÍÁ#e2ñ
\x0002ú\x0019Às4èYë9\x0018ôÇÃ¶^?Ü­¯\x0002þÅñæáóÈ§àjÇ'¡ÜsX5çiì¹Þþ\x0001	ïåâõåÙò0H²8^]þÐ'Ïv&\x0003ÈóÅHÉòK\x001c¥t:\x0016%\x0013DÂÎ\x0012ÉG\x0016ò<KÕð}<¾\x000f£éJ`Ú'|\x001fö5äÙ\x000e/\x0000y¾]Ðð}G:]!Ãî×Ø)!\x0018Íxë¯ )äy<]¢Eß5\x00158ßá\x001cLúfHÁ#©ÆÉSØ\x00037= \x001e("\½Fâi¨¡Ñ~q:³qA\x001c.fÓ·ØZæk\x0005y\x0004
B\x000eç=\x0006\x0006Î©\x001b%Ï¶U<Ê£\x001e\x000fÊhÑ7"
\x0008ÿ\x0013·æI4\x0007J}íÃmù}ìö\x0000bniÿ\x0008/iP$\x0016\x0004­ù

'D±s\x0003ÅyèQ #,\x0007
BJvkéýÀn£\x0004*\x000fT1óÛ\x0005T6\x0011q\x001a]N´t_ãD¶\x0010\x0008^ç\x0013Ã%\x0005\x0004
L.êú$¨$Ò¦\x000bTl9§ÍVù\x000câP6UÇ\x0018\Ò³ý\x001aòøRÇC\x0011[>\x00106r\x0008Î<V\x0001:l'yÂ¶ú
ò(Sºpf6\x001f.hÇÎ Y[Ò,8µ\x001cÖ2V\x001eUÊóxØ^<\x001aË|EP¸-"Ó4îTÀý-M\x001cíT
^6OeaBq±§ÐÇÖt\x0007\x001aBgü¤<;\x0004Êò_å¿p!Ý¿»}÷û¯aLn]\x0014J§Ýo'¦³Þº°ý³ÿöed\x000e!ú.D?\x0019bî°¤ÔW\x0003\x0018s\x0011U\x000f½]\x0015cgÌ\x0014Â©É E¢Q\x0006ªÔ2r=¡:ÆâSóéß:7\x0019
K#\x0012\x0011\x0018¤2\x001dd'(\x001f@RP~<HÛ\x0018\x0004P+à×¶4ÒÚ\x0006L<S¹x\x0002H¿6÷\x0014´túeUL¾\x0017¤*¶jÙ7ô¹¥âCGÌÞJÕ\x001azAêB'õt4Ä>!ØvßPÏÒDý\x0018mÑNÆHãn9÷\x0006ga\x0007DÐ t\x000fÙ\x000eÂ?JÃ
\x000fiØýÛëÍçõÝ;<®~üó¿îÖ÷W·7cPÃL[CÖ=#\x001eÃØ;\x0015Q\x000bSqìöO.V?,Ï^âÑtt¸¿:[^\x001c\x001cï\x0010Cv\x0012âA\x000cxK\x0010#|Ü\x0010®¬cw=D\x0015h2\x000cöM\x0010/\x000bAàu.A$ãê\x0008[\¤µU\x000cY±dpºçù \<:Ø1â¤Øÿû¬n~\x001aW>\x0008\x000e{\x0000"£2ß\x001epÒô§i\x0016«ã¿uÊ\x0012¶y¼¸\x0011ÄÖìiÿB\x0014|úç»Q\x0013\x0014N0\x0008GÇÊ_esM\x000bÃaÒÈ\x0001×ËÅùêìÉþqÔ¿¼\x0011pÒàØã\x0000E\x0013SÏ	­\x0010C¦\x0017ÔÐv¹\\x0003ÚÈåÚ\x0000×HK³¹S)d´ÁÖ\x0019©m$u\x0018àîè\x0011ÐrôÈxÀáîV88h{"\x0015\x0019i°\x0008YóJÚ| `!\x000bÀB6\x0001¶\x0012£áÛ\x0011c®1\x001aY	¥ò\x0003ú9{\x0010ÛBáµ	±ò@B\x001b«¤«©p"§=§t0{\x0018béË=çÛ\x0010;£6$øØ"õ,\x001b§h\x0016\x0015_s(`Y\x0002nS
'%ÔP¤BtVÆÑd
%\x0007p¬\x0003\x0006Öð\x000e`xm\x0002¬
Em\x0008X ;\x000fAþf\x001d±Qe3ªÍ²A|\x0002\x0007E9¸$-\x000e¾}\x0002\x001c® Cæáì\x0000ìRåÝö\x0016\x0012ü¤pn^¯ßn\x0016?\m®&TOH¼-q\x0017Cé\x0007ÝjÑ®Ó£åÁjñÃáê°ÿFÈª\x000bY5AÖD\x0001ñ\x001fNÕ*ÄsPM\x0012ì»}\x0013dk®Ø¶Ëæ(IÍ°Ü©\x000cr©Èq:fas(YúÙl¹rû\x001bÙ\x0015]\x0013fJï\x0006Õ Uf\x0019pe`Þ\x0018À¢XdÑ¶ÈáC¼tàY¯·»¯\x0012\x0006\x0018\x0005¹Ø}¢iû	fD¦íG£
³³-³ÖñòÝ9øti0C;åÉÝÍúa\]w{\x001a\x000bfX&\x0012g9,T\x001bm`¿ðzµ¼ü×Ý¥J\x0011;/±ófðs_\x001ccøîâXí\x0013V}\x000cú]\x000boô£
\x0019|Z*æ½¸\x000b÷ÖÍÕâäaÜ\x0018,a´&f¯p\x000bDf¯Î\x0008c]¹ÀÅïâ,ÜVWËî\x0000¬GEY´cæ9>\x0007.\x001e\x0005\x0011L÷D\x0007aî\ÿ\x0002f*mÀ,è-R\x00168a¶ÛBÈ\x0019\x0016º;ëT¿ \x0016úé ¡*\x0008
\x0016ä\x0004Ð,±ÕÃwÃ0\x0002³iÆÌ0Ç\x001e0\x000b\x000c
Xgø±¢\x001eÊ\x0018\x0004Ú\x0014\x000bmÚ\x0017:|Æ\x0006~A\x001a\x0019Bz¨Ê.VÚ´¯4Ï­û\x0014¡¦à®ï)r\x001c¹C\x00100\x0013YÂtÌÒÑ\x00045!9Q±8íè écZ\x001f\x0006Z\x0017 u3h×B.z\x000e\x0017ZS½²3(-Ã6+ðÙF\x0003K\x0002N;W\x001bAWî\x0001ÃAû\x0002´o^èm*À:èyJ\x000bmr\x0018T×ó¥C@sY¨4Í:­d¸Âf¶\x0018GxæhÖ¬2ÜüKÔ_ö5°\x0018q6¼Uð0»-¢ûëq±rÅ\x001d´\x000eQ\x001a0UFZíÈÜ¹ÚH\x000eêÛ_\x001e?\x0015\x001f\x0007´\vîZ\x0001m|\x0007b_2g\x0004M¬¯M\x0011\_Z>\x000c°\x0010%`!\x0000;\x000eÇu\x0002Ìð~h4£PR¸(\x000eè¦ß\x0001XÚ\x0008²Ó*b_"~{zõ~\x0013h$ð8
\x0006a'a%Q½ëëLd=|µ:9>>|*\x0015w»;í\x000bÇf@.4Yh¨\NS\x000f­E	¹¯tÍn\x000bè¶\x001d:äª\x000cê\x000c~u*ò·Æå\x001e¹ {ÑîÅ\x000cÐaúp²"0wL&÷Ô\x0018\x001a>e\x0006
ð­\x0001wRmáWðíð×ÁZ¿kú.w.ÏÉ­öÛ;¬¾¤)*¯½~	õ¢5ç1rU W3 çÛöDC3­·t@jQ3+cû\x0002¹\x0001¹'òÆN\x001cO~_µe\x000cpQ,¹aÉ!ÒÝÌAß±<Á[[\x0016û\x0007
Cî
än\x0006äOÍê=ø\x0019»¥yÿXÀAÀe±är%W¹õÌrÌ×\x0006ä¤+U
1Àu\x0001\·\x0003×[%7\x000câð1\x0010Åù°ëúcÜ;ì¡+\x0014ÅÍ (\x0014cà\x0006©ÆC(Ó?:tÐjûBMü\x000cjÂ,Í\x0005äd\x000cóÝôÏ¸\x001e\x0002wçÆ\x0007[Ø\x0019\x001c?\x001d¹¡¹haMk\x0000N%7J÷Ñ\x0005\x000eE^Zñ9Ì8äÊ1ÔêLî'4hV©
\x000bø\x0018è¢.æÎhsÆ
CÌt#eÿ3@ïÐg\x0003ti¡\x0003*>ðð#rï\x0002/\x000b­zÿ<Ò\x001eè\>ºcrÙ½cþ÷¿ÿÇÉÍûëQôÜ\x0006¯<%Éfr½áêÙig*É^¼\x0004-N_?ÝX\x0002±\x0010ß\x0000ä\x000e_-@ò\x001blJÈæÙCî´\x0000äØ2ò¼!sÙaõ\x000bãû³ÇÜ	DÌ°É3Ä¬ä£\x0014µèáôöáúêÝÈâYËèò\x000eÉ\x000e¥ËÂ\x000eµî.°Ë§'G/OwBÝ¶\x000e\x0002T%!Ô5c1\x0016Ëná\x000f ì¦K½^¼º[ßDö®ûtdSS\x000eÿA±\x0008?90	<\x0013xe<ÿh¹xu¶<D^Ç\x0017ËÃãN\x001fÐ#"ý,íeç\x0014ËASz
\x0012Z¨!O½gÌ\x001f\x0018þtØL)b¹®XnV±4Çiºák9¬Ûph\x001e\x0014i[båXQ\x0014\x000bbE3Êå,&	
^»ÃÑà
©½¯°Ô¶Å\x000b±ø¼b9,rc0m\x0000£qE5ÞVF¬¶ÊUØ\x000c>«ÑpaKaõ)\x0014,h4\x001a
¯*Òë
M«\Ñà³Z
¯\x0014¦\x00184J%nR$"H®Ê@ÊV¹
«Ág5\x001b0}=õJ\x0006=ÔüsYÚ_¶R}Û*/äò³Ê\x0005m¸¸¿Â½ÓãÙE\x000cãÞU\x001cF±Da6Ä¬fÃKEWÌ2l\x0003ç\x0018é5j«VJ7c^?CQó4þ\x0000t
\x001c«\x0015cþ+Bµí rÅ÷9!\x000cLJ\x0019N%[.Ö¦\x000f&*sdá\x001f¯>=2ð's:\\x000e\x0018ö¦ªqé¨Ð öH·{Ð\x0012:RÆ\
#ç©1u½¿¾ú4:ªIõS"\x001c[y\x000c
Õ@Ø
]0\x00153B3Ø«£Ãó\x0001ð]\x0017¾ûÖàËbõå7·üªX~õ
­¿J\x001c\x0004«´ÊcÆ\x001e\x0016gëõÕÈK\x000e+&bºÊcP\Úä½å³ÕÑòð|§AÊ ]\x0017´k\x0002­\x0016)6yz\x000e·ÛêÝ\x001e¢Á\x000cºo¥y¹Ò­Ks±27/l«%De\x001eõHÔ¦@mP\x001b`\x000b\·X£éE.å¶7~?\x00105ã\x0013\x000b5\x001bþ 	»â[=ÉØÅlzò#³Ý0Ì>ÜB ÊãöÃÑ \üüû¸Ê6\x0016Ç]lÖÙ¨ÞZ"}\x0000Ì¢®ôÃ¼Þ¶äâû+ÊÚ¾Xsî\x001fñ\x000c\x0007G%ñ\x000co»\x0002¦Oâ{\x000eSÉÁa4\x000eÍRÛ«x\x0006ÛÖrÀ\x0015­#
[¸\x0015dÜ· Ä¶Êf\x000cJ(l\x0011\x0000:"J\iCÅoÎTº\x000bï&üñ¶Ü¦#\x0008ýðH îí\|y;oÈQ>é°\x001dÒ4Xk$ËJW\x001bÈ8Q"Y8kË8÷K\x000e6ïÆj\x0018eÄÉ¶Þ#ÁWØ\x001bH5<\x0017þø`õ²P°]R¸®\x0014/á¤0Îr@À{n³\x0018Ã¿È@1º±:ùe¬nÚ×`\x0006aq/YÎO[t4¯ñ]O£ø\x001c_\x0004E&jOýôáÐ{\x000e#Ã
k\x001bt\x0010nàum\x0018¾\x0010ãq\x000cd\x0018\x000eávX<åÃ¡RZ°Jâz¢\x001cBuå\x0010j\x000e9\ªr(O¬jãT¦p|\x0001\x0011r\x0014j%fQ+\x0007g MlwÆS§\x001c×[zÅ¹¥¢+|â\x000c \x0005ô\x0006$!¤ÆÖ\x0006Ç=²HÃH÷¹(TJÎ£Ra'._îhN«ãÖÐ\x0018\x0018\x0014\x001c.*P³\x0008\x00016Vr$T5\x0012ËÈ\x0010[\x001b0UÂN©YìT¸\x001fï1,öp,³@\x000eL\x0015\x000c\x0012Ã<ö\x0016ÍSÞâ÷ëûOà·ÞÝ~ÞÜ¼\x001d\x0017ïã~£%s!¢Æ)ÀÒ¹J¿D\x0010(¾~¿¼¼8\x0007\x000fþôìäÕñÁª_&Ñé½þ-Ê$»2É¿L¦+Ó\x0013nð·(íÊô8ãöÊä»2=aé¾Aº^¿yÒëÿ\x0016*ù_ÃóÂ?uýÿ\x0016*Ì9ÿkØs®
¡pí¾E¡t!þk\x0008U¼ü¯qôòâèý¢Úå\x001b\x0015Ê\x0015B=qýþ\x0016*\x001c§b<ß P¢¼uü5Î)QSâ¯qNâz*4÷-
USâ¯qNâ\x0012sJ\x0014çøkS¢8§
\x0013B\x0015çøkS²¸ùÊ¿ÆÍW\x00167_ù×¸ùÊÂ£x*iñ-
U\x00062ÿ\x001a\x001e,<§23ß¢PG!ÿ\x001a\x001e,<
ù×ð(dáQÈ¿G!\x000bBþ5<
Yx\x0014ò¯áQ¨Â£Pß¼Ga\x001f'=ìSI×\x000fwÿÔ³×gÕb³\x001fã×\x0011&W4î§;T·þðqýþf³x}ûp?j\x000e\x001e\x0017<çÚ½Üó©çF3ýªÌùË×§ËWáÏ^\^\ìþ\x0006	º\x0012º\x001eß[ ³\x00000Ñ
\x0018\x0004a\x0013»´T>lTªËc°)T§\x0000\x00161×\x0017¯×w×ëO·7ãÛ»wc\x0014Á4\x001e\x001f+`ieÔ.<«Ôí¾^\x001d-ÏO\x0017Ç'g/+¸\x0013£w.\x0008Ø¬Ø/^Þ­\x0017û\x000fAóïÇ Âá7¦\x000c
¶JÒ\x0005Ç*E>§gËÅþePö\x001dpÍûØú7\x000cQ¥ÀÔzñ·»õÛA%4*½I07ß\x001dÜÝ^ýöÝ»ï~ØÜAÇzÀ¨¥Õ,qj\x0001'®Mµ{\s\x0018'\x000c\Ú+\x0019Ë©Ç\x0017«ÅÁÙÉá¿B\x0005ô\x000f«3h@?Z.þv¶<ø~Wwyc\x001en¼ú\x0015Ï²t\x0005ë»Á\x0008·|OPª4å}+\x000eõw\x0000Ð MínË³]jÞ¼ûåAÝ=à7¥\x001f\x0013fý~Ä\x0012rÈÂ\x0012Jµ'x\BfaâN\Bnj\x0008\x0013\x0011ÌòÕn`;Èô\x0007ñ{Ó «I]ùüÙmþì&ö
f\x001as¿þÓÈõÞù\x000f·ÿÀ\x0018~Ü\x001f¬¯×ïbéþÑúóí\x0015\x001crÌCë\x0012ñÿç»£õÃ\x001f\x001b\x0000ÌÃÿÁ\x0008b#¹62
ï5a]mÔ\x0002\x001flCª^x¿x¿[~w´¼üß«`µ/cÝþÑòÃ³'Yåõ÷úöÏ¿b\x000e/fî\x0008k\àóÛ»xf\x000fk\ê4
pAeÂk¤C¼61B×ðÆ\x0005>?¹<;xz\x0002A\x00172\x0004pE#d<©\x00012,¶AÈ`­\x0012dgf\x001c\x0014,\x000e\x0014oYåà\x0015i,¡2AÖ¤\x0015÷jÅ\x0018ÈpSVY@xìYj\x0019\x0007È>C¶3@þà»^ßAÿ\x0006ÌL\x000fb\x0018ýïÿåÇû¡pÃ	¸¹VÊ3+ÂUq*À5VîV
$\x0016],O/v-íß­¾º¥µÁ­±ÝIÅ\x0016ûëûõÝÕÍ§¡X\x0015\x000c\x0013H{\x000eFï¨U0à;X=÷»÷\x001c'>_ì//gÇçýÃ*æ­Ofµ\x0001bØ\x0015\x0001±GÀ"æe6£ÛÏ@\x0008;\x001btðñ¼nn}¦\x001e°k³'LÂ®\x0015\x000b/Ó¨  s`\x0010\x0006ÌZkPáÙ:´ÊÁ\x000f¦Íç»&¬÷ÇÍýÕýâÕÕ·7¿Ï&@|4H`ÚóIpäíñ$ND	xìHoÕ
Æã£\x0001s0ji8\x00027A="ë\x0011É~ð°%ÁmJá»Ûßã<\x001fr\x0001È¶'g0\x0017!\x001e&Ü»\x0012­¥\x00116\x000eÐ\x0000ôÒè\x0019-
ç0<#=[Û4×\x001bÍM\x001a``âTRòø\x0011Òÿí*¸áþØ¼ê?m~²>¶kBÁ¿+UüåúáÃz ú°\x0003H¬\Cï±èévxàh\x0019¹3 áí\x001a¨	ú±¿\^¾^îB~-n×?®±t!\x0016,däÑ«¾}ØÜ\x000c>,¹t\x000e\x0006Ü\x0011\x0007\x0013ÏvaÉésÀ.ÀÑ«>¹\\x001dï:3·éFÕ\x0002Y[ #NîÛ"AÖtfb4`.Ä ÚzO@Ìyêª\x000fÐ¹¦E\x000e\x0017\x0016G§<ï·½Ýç_nù\x001f\x0001²xK|tT:À¹»½¹\x001alG4KW¬\x0019f&$«
,ó\x0002:2¾þó¿Þ÷\x001f7á\x000fÎN\x000fw)4\x0001ç\x001c\x0002«éÙ\x001cf5\+\x0013Ù<Ô1Z\x0004À-CÁ«&=[0"9v\x0005ÐF\x0008\x0002\x0006yÍ\x0004Z@=dz6\x0001{&©µ\x000eGÁö\x0013è4oe6Ð6¶ óí@\x0007EÁöB\x0011æ~s×\x000bù\x001fï¹ºÚ¼1ÉpÇÇÖzDlÙ¬o\x0006»&Ø´ÎÁA\x001f\x000b¨-nE/ú×y\x0011ÿõâ_VËã>Ô\x000e\VWø­PÛ= U"ä\x0000Ð0Cùàþæz±¼º[lî»¿ U¿ÿôËû>Ãò[X~«º³*.Ïàn³~\x0018*\x0007Ì?2)#ÀMÁãÆuN÷ø\x000bþü¿ïÃßºPáæî\x000eqU9.\x0017\x0017@qp¶Z^î\x0010Ã?¼}øQ!¸\x0003Èq\x0014nÃg\x000f/ï\x0012È1Þ`éÎÃ½b\x0014"1N$çd\x0019Ù\x0011\x0004\x001dY\x0016g»îî[¨À­\x001f\x001f\x0013 \x000fz\x0012¡»O\x0017÷HÜ ªX´Y®¯®¯ÿü¯V¬\x0006Â§ð5õU§ØÅk0÷Nx
îq¿kO\x000eF( º\x0010\x001fS>|p\x0014E\x001fÍ^39o-\x0001Ü\x001d\x0005\x0019\x000cPBÿd|L\x0000(\x001cËa¥pÇr<!qB¨ÅÎ°ÒpÀ1\x0012\x001fS\x0010B-zá¬ðiëÛ¼:¶êüÕÛÛë\x001d»}8N\x0007+é&®¤\x0014#0á«Ë´Ç!kC@u»2*\x0011ô0>¦ \x0004o2\x0001¤Æñ\x0000o\x0010Ì
;Ìh+Vh¸	XÃ&¡1\x000c}±`ð½¡Õô;\x001dÈ\x0011\x0008% \x0013\x0011ª4i+}o1äÈ\x0010Ú\x0019\x0010ó\x0016\x001fS\x0010¯lq
a\x0013	r\x000búà3à³ÏNÃg9¤À\x0013>dÈ\x0000|Û­mvºTÃ\x0011ÙQ\x0013mO¸ï\x0019Lm\x0004ç\x001a­£ÑY	SLaqp²XPÁ	)PÃa-ÐÅ08ø-@ÎíHº\x001eìd¤£7èÿqxó9\ ¯néBþúEüë[eñ`¨ü4C\x0015.)ÿ
²¨ÄY\x0015ã!¤\x0018ðÙ\x0008\x0006\x0010Nóx0ö\x0002Íp1ðhòÆÁ°¯×WwW­:\x0001YÙ\x0017ñ1\x0005%L"°ûä\w½ÎVPu\x0013\x001fS\x00002\x001d¸p8ñô¡5¤²\x0012BädiC\x0008ÙøËÄh\x001cnªáHbÐc$Y*\x0013N!ò\x001f¶ÎúîÃæõMëg7.X¾øYÄb\x0002È½yA.¼ "^¯cÓ"B#êOYßý\x0002î|óÕc{k;x²dm_L\x0011:åÈÒVNÖ×ß\x0004¿¿\x000fî<LÄxùf\|ü¸y·I\x0015Q¢ÍáH#âò|ó\x0010ÒgÇ~w\x0008ãhµ8]ÃÓÓÕËU¬z\x0012óÕ­¾ºyÛ©1A.½Ñ%\x0010\x0010«%°ôÁ(Kvï>g?¯§\x0004â^üxÃq|
QÏ<?ä!1\x0002/~X__¯\x0007ja¢£yÓ)¼6Áí\x001b7\x001d4)ÄrÅòúêíÝ£D.\x0013\x001fðâåÑÑrWÜ6KÀ!¯Ä;\x0003}¦ Ã¹¥1þ\x0019Ö\x001coÑP![ÐÇ\x0008Úúã&ì:»¼¼z·3Y;E\x0016¡ ë&=Q¡««`î\x0008Å\x0004\:H×Ö\x0006%ü\x001dÃ$\x0001Ò°YU«BÝñFÅ¼OÜaß:\x0002(Í1¨\x0011\x0013¸\x0007wW¿>lîç\x0013DB3Þôl\x0012$ØÈt\x0003>lr;ÂU&9d¼­ãèìêÐD\x0001\\x0014À5	\x0010\x0016ßÄÒ\x0004\x0012H*c6Ýë\x0004
¦~
	<$¸Ó³I\x0002»ÍÒ7\x0008÷TiQ©øÂ9ïíNk:
8\x0010¬¤g\x001bp¡\x0012*\x00007pÒFà:EÝ\x0001øîÝ\x0018à?¼{01¶\x0007ii³Å½	ßþüç&f¯¦\x00078Ï%Xªúj\x0011e\x000brÒ\x0007?ÿùÿÜ@Öûz}óv\x001brÿ\x0000Åá«O\x0002\x0001\x0012&	 p\x001a%\x0008\x0017rbð,rÝÅJ\x0006ÉÄW\x0014AAä2>¦\x0010ÎÞ½(\x0001xXà'ÂH\x0007\x0017qr;H°
·àÛWsa\x0001©ø\x001dÆ\x0017¹èÀÃ]8ÍF5\x0002\x0006\x0018%ðÊëdú÷7wo\x000f<\x001bt\x0007Ð]\x001bt\x0005Qº\x0008Ý+¼{\x0004\x001fÓ¡òk\x0016ûÊÖìG¬\x001f~#-I\x000eÏõ">\x001aäP>Õ\x000c\x0007?ë=§Ó'àxçáÐ²é\x0013ÜmÞ¶á\x0016\x000fì÷÷¿Ç@)}îâ¾Ú\x000c-	ç\x0014\x0018R\x001e\x0007<iÃH\x000e\x001c÷À	\x001c/~¿ßýùïê'\x0015j¯vVÁ\x0010hnÁ\x000fOÏi¨úK¸¢ùÁÿW6®q/ÍTjý\x0002ß5(\x0002\x001cF& \x0005\x0012Ì£IG\x0011\õ0
ö>hÅúÓ§97À5\x0011´\x000eB¾\x0012.RÆ'ÔÚs\x001dY¼ç\x001d´é9
vpÐÖ\x0013`+­RòT{ï<y,Ð\x0013ñ"UÓÀ_¾¿¾»[ßî\x0008ÿÂ®8,HzN\rKuFR\x0019·Ç#tËST3@r¶\x0005·¿ýúñ&q\x001f+º$¶\x0003m\x0006Æ\x0007E\x000e\x001d®V%\x000ek\x0008½Qæ=\=vF0;M\x0012y<O\x001fà°¾yÚü4Àa?bÌH;6:\x0000fÛ+÷ÎlÆ\x0004ÀT\x0010ß\x0002ØfÀ0O\x0019\x0007ÌgÀ;³m\x0013ðB_¦jÔ.
f\x0013\´ÀrÕlw¨s\x0002`(HZ\x0000[ò¼
i1j$\x0004%?¸ÞY
5\x00010\x001czF5\x0001V¹$Q;Kb\x0013'0ñÄ\x000eÞûÍÎÈü\x0014è\x0016\½6èáj³&R6ÁnP=ÿéúÓ¯\x000f»cDC¡oþ\x0010Ï ãê\x000b\x0007º#ànñçÿÒÁ\x0015F¨U"³0#a÷9«lw\x0017\x0010àT¿\-ÓðìªÚÜ³[déÜ\x0017\x0001êÍ\x001aº»#\x0006Cy\x00025%êÊ[«vÞ/\x0002Ôã%4\x0011Ót¥^ÀPä§\x001b\x0001oã·\x0016ì0\x000bI%~awÚºñ©%´\x0005°\x0011©U;5±Q=³6\x0014p¶lgt|\x0018`õæïV|`ï»\x001dGÐ¡tóîî6ÍÃÆzÍ¶ûÛ?ÿß{\x0000è\x000b7Á8*C\x0004G36ÈïY¡Oø\x0013&:
\x0011éwû«ãÃ\x0017GåñË³\x001d»«ü1ÈÂY&\x0010ä±Q\x0006 YL9åä³ 3/\x0012#Ø\x0018d:µ\x0007\x00002\x0017Ûç\x0000\x0013Å¤J;4lï\x001b\x0005ïá)\x001e5/®¬ácþ(ýíD\x001c¨Ã£¹HY­*¨pÙ®ÅÐÊcõEX/(Øky~¾ÚÏêâ"8\x0002H\x0016;©C\Ì\x0013.Vù#pA¡°\x001d\x000bFïÄ0\x0001lJ\x0003F\x0019\x0002\x0016\x000fÚv`P³!Æ,ó6õ!\x00010\x0019ëù"0I{E*v`ØI2\x0002Jv\x0016Å[F\x0002N{\x0000¦æ\x0001GÂ\x0008`:E®\x0000¾\x0004ç\x0015\x001cíÀðÞ3\x001cXðV4nJîó¦´è#\x0006`¬b,F\x0000Ä\x001fµb2õ\x001e\x00000úê\x0001\x0018ïp6U\x000cÿp`A£tÌ¹-0\x0016«5"0Á	eWÆR¼Q:æbCL\x0004Æbµ\x0000\x0002ÃóÈ\x0000ÃÇ\x001cÀ \x0002O\x0002¦SÕ
\x0000sqdoô.°Õ2¬\x0018ô"Ì\x0000\x000c"z\x001402\x0011àêø\x0018\x0015+FæÂ¸XÚÝ\x000c\x000c4U2°ÖíÑA®<ÂÒÖËÍc^¡fLÓ0¬èç³_a\x0014\x0001³ó\x00003\x0012:NÇ\x000031÷\x0016,µ=\x00020eòéYp*æ\x0018\x000eLaÔ\x001c\x0005»\x0000qã²\x0015ëî'ÿá×Î­µÃ¦\x0000WX\x0000Þ\x00070Fdÿmð1l\x0004¨|¶ÿZUV®Ã£°X\x001d\x001cõ#}\x0011d0T©S#\x0006@õ0Î/­eöÓ´©ìÖ	P¡íÏOª ñ,B
\x001bÅ¢)f >
\x00143r¢\x0002\x000b\x0002­jbàJ«JÆÆ\x001a(\x0014\x000f*\x0008®§®*#Ø1	MCiU5ÝR­«ø*C¡¾»ÕWf\x001d\x000bãb­~Ôdû*Q.ÕB·o
P\x0014L¹KH­ÅÏ\x001fþêä»\x001e-\x001f¡ì6Ö¾K}(ãÍÕL@	]ÖR$\x0001IæÜIL§j\x001f;ø`þüéáýæó4	2½Ü|z»¹I5\x001b§·w÷ë«ëXp¸út¿¹\x001bp±
×
Nl«9Ù*üüWéËÕùÁê8Õl],\x000f\x0016/\x0017«óÕÙÎ»î\x0016=9ü­ða´\x001cn¶`ÍE
ærHÈ M\x0004"Yi\x0015AóÔ>\x0013Záp_¦£VUìÅ\x0014\x0011Þ3þz÷&b{AÍ\x0000CÝ(\x0017{d\x000bþ 3¬j\x0006£^A[àÜÂ(\\x000c'\x0013.àñHþ\x001dÆ[­ÝlF 
ªäÇ 2.+§µÁ*ÂâÙ\x0015ý5\x001c\x0017Ômq6j¹Ä\x0016¤\x0011\x0018ywVÏ³`P\x0004ÎÍ¨\x0015\x000bhðÆå\x00049OZgýÒ®²\x0017\x0003&ÛÜh;\x0008Þ\x0002B\x0019\x0004¦ò§4µ«à\x0008`èw\x0000¦ö¸ËÞD`R©\x000cl\x0015£ôäO)SI\x0000ú\x0016¨ü¶¤­ù}¸nþý÷ßû²n=ù>ßßÞo®S\x001dÀõ\x0000'Èn\x00036\x001a&×£M\x0014u²r¦éïÁ\x0007úþäbuJ\x0000v:C\x001däÉö6!Çü)|\x000eÎ\x0019Fî\x001bÐ»|
ä)NÝ\åë¥21d\x0010÷¹ÍÈuEk\x001bC¤¥\x00119Îª\x0006ä,ÚdÓI[\x0004«Î\x0006äéDlA\x000e\x001d¹:g\x000b\x0018!gdÂxÅ5\x0000Onj\x0013pxKàë\x000cüë(K\x0001´ \x000fÆYá©\x0001Ü¥d·Ê"¿ÎCT#r3%SúRªl\x0013kAì\x0006àÉÃjR\x0016%XsAq+yÅå\x001a\x000b\Ü}R¿Ë/¡\x0004ëôjs×{eL©2-!]Á©û\x000fT¤rI\x0013SÊéáêlçµ±´{ìA
ycÒ\x0008\x0015/ã)\x0005ê\\x0016§\x0000í2£:u×F¾"\x000cB\x0013Re*AÕ)H»§Ê8¤.Ñ3Çu·ÀÔ¨|Aèµ\x000f\x0003úOr­ºj
EÅ\x0000\x0016	Úë@¤¢2·º=n T\x0001È¹ïå"¢ÜÕX`K9\x0006R1÷9@×>UU4r\x0014´¤ã !®m\x001d\x0003·Ûüw­Ä¢\x0017Øýûë\x0007v\x0015½rh0ß\x0016\x001bÇzÛû>tV\x001c§âYï$\x0011h\x001fûkÏ\x000e÷V=Bu®åññÉÓí9\x001d|->F\x0002\x0004&\x001b\x0000Wû\x0000PpÌî\x0006À<\x0003@¸ÒÄÇXÜ'²Ó\x0000P(h+\x0007ÜsZA?Ï
ÊØÅÇ\x0003\x0004Vÿ\x001fWÎ°ts\x000f(	Ò3ál/\x0017£ñiè~Ðø\x001d\x0019iA/
::\x000f>¸és5\x0001CoYy`ÎON'3\x0006½eÆÙ,\x001a(!>\x0012\x001f£\x0001DZ\x0014\x0000\x001aN9`f-Î0\x0019{Zg\x0000\x0008M|ü\x001eV0
¶Hrr\x0000 £\x0012¸T¸8\x0003@¨Ñ\x0000Å\x001eâ¹¦+¦$\x0011_lãhÇ\x0017¹P'\x0018A%L"\x0008[8ø^L§=¬\x0010 öVÍ±Gx$8OÏq\x0008mp	R¿'$
\x001dÔC\x0007Ìyr\x000e\x0004\x0001?%&6\x000eNN^6\x0001\x0015\x0011èhk\x0013<\x0017X@²i\x0000\x0000\x001e\x0003Ú\x000bHBÏ\x0006ÔCÖ>=Ç\x00015Nzè÷\x0005 ÚñT=dÙÆ\p
á:Ð
Ô¾WæÝÃ\x001b&b[\zææý»õÃo}\x000b*Có
û$:±aA*>â´L\x0000kÉÁ÷Ë×ûg'OB\-öÏÿº\x0003£ücóîb%Hl»­I×ëÅ\x0001´#®o®ú\x0013ÚQâX\x001a\x001fyL!qH\x001e¶´)n{\x001eSrç;p\x0006ì`yº
ÿÅá.,Ã\x000c®ñ1
o¸\x0012 ¿\x001d.TäXØ¼¥¤pjfÀ\x0010ëI\x0005\x0013%'\ÚäVîAx@\x0010`\x001bY¡æ\x0004\x000cÊÀ'k\x00044Né\x00141\x0017@Y.²dõ![»#E;	¬X`n2ØD¨\x0017°ÆQRU\x0010ZUs¡\x0005jøÖYÊ+q§#\x000bCëë¤s\x001eÌ©\x000b0AãE|LS^&©^
:
D²\x000e^Ré!w©®`FÀÀ+\x0013\x001fÓ\x0000sN\x0011Eæ[ê\x0015Å6¸q»*\x000c¦Á8||L+RÈ\x0000à\x0006\x001f\x0014ÂPz+çg^_íÄÇD\x0010Xg\x0012k"Z¬V\x000b¬Ükq]dÉj\x001bD¸x¤\x000b,8bh\x001c¼¦µ¸ó¡5P»b>ý1h%ð/*¼\x000eð½¨	ábkÉ5rµu?\)ý\x0006Ü\x000f°»Þ\x0015n÷êæþnó¹Ï½á\x0010¸ð\x0002}ïpUfïÕ\x0016JØR\x0008\x0007ÚwNO\x0002È«ï^]®þíå\x000eÔÕñÅÙêÝ~\x000e!I\x001bäTÄFX,Í\x0000â\x0003\x000c:k*Òì\x0006ç\x000cºqf\x000cìé9	2Ç©H\x0002&\x000bEnIïæ1	«=×*óÏîïzÓåuuz)\x0017§×\x000fi\x0018jo|Ïxõ\x0019*¦R¯ÎÚÈ\x0019¼\x000cîïÿÚ­ÎÔE\x0019´þ2MAÝ¥Ø\x001d\x0001R&°U\x0000IÑ|Ï\x0014\x0016D\x000bÊ\x0004ôú+¡\x0007¦íf\x001a|¨ÇG7Ùk\x0015çÙÁú\x001bì	5>ªÎ×ÃÈ¡øhý\x0002Úbðß°°w±îK2¤A7)\x0004ö5D\x0010\x0003F\x0011´Õ\x0018â1Ì\x001a¼V\x000bÁ°|=Ü°ý:"\x0000
âøh\x0015!\¸uú
\x0002\x001a#ÓWà\x0016
}Æ¡Ëzp\x0004æeN!\x001d)íÖÈB#`²ý2\\x0018Dº4J\á¶Îí×\x0013\x0002²_Rµ\x000b\x0001sh
\x0006\x0006Ø®c1ªÂ¬å*ÝÌæ\x0014Â>¼¿ùG·sd3"H}\x000f\x001bN]¾`F­Â=ÌÉÆLcMÿÉóí\x0001(@ÕEWß\x0007"´ZâõÜ°pÛM\x0000À<æúÞE\x001d1B]\x0012\x0018\x001d·\x0018ô2Ì\x0019Ä«Ð\x0015ý[p(F\x0008ÌÈntf(FCm\x001dÁ±N»-U©S®
\x0004©\x001c\x0014Û96\x001a$\x0014Ëd\x0007ÊåÆ>B\x0012.\x001e|i\x0018H/¡ç	Ï=i1î.\x0005ÃK\x0007òø\x00189<%\x001fº÷[°òèô¥çh°"îjøìÊ3þÐñÀÆ\x0000ÁþòøàûÕáÙÉ®kìP¬À*#±r\x0018	\x0017\x0000Ou¡Sga^î¼PEÇN<~(ThÄÆ¸@¸Táõ*¬5uVj\x0001\x0011ðí;R\x001bC1j\x001fÙ1¼\x001e1ÎEO;^·\x0019!J½â\x0001mjÍo9ckz
TaÒÁÂ8\x0014ä0\x0008(b
~è\x000f\x001a×Qº«÷?ëÔ²s\x0014óqÐüÏÞY\x0007é´ta3aÊÒØÜ¬áSÄ"§óÕ®pÐùÅ\x0002þh±+»¡*<ÇÇ\x0004¬BQ\x0017\x000f×T\\x0019\x001aU\x0019v4ôàäøåò50á´¡¹H°ñ\x0015\x0000×³pÚt@\x0000\x001eOÐ{M$\x001c4àüäòü»TÐÖ\x000c6ZT5em=Ì.Åº\x001d\x0003û°KQnÝ\x00088¦æ\x0004«#X=
¬\x0017\x001b\x0000«M\x000c¸\x0001Xm	l\x001c&<\x001fX\x001d³\x001bºHo\x0000Ë¨;V\x0005Ç\x000f\x001b;lî\x0006PZ\x000f\x0008À\x000fÇêbêÈMSYúµà\x000cà>\x0012\x0000VG¡lÍå¼XeÄ:Mc
¥âµ¢F¬8QÚh\x0005ïJàâ©å&i,\x0017ÄU£ßæ·\x0004aÐ\x00150'V\x001b±ÚiXe¢\x0013
»\x000b<lì¤1Æawù\x00176î.7iw\x0007ªÒ +:±qe>FGR\x0019Áú¸½ü¤íÅ½&»¥:î ôh·R\x0003R/±Æ¼SzNØ^Ì¢ÆJI.Âxê\x0006J÷æ\x0006\x0006\x0003µ@P\x0013¼\x0002«aÃÑJä.Æ}ñD\x000c^A­*g\x0014X\x0017ÁNq·OÀ(W\x0008Éc\x000cm\x000b¡ä±\x0015k´\x0003v\x001d`2mþG[\x001bý\x0017EPUo.k0P\x0017y£âs\x0002Pè¹J8£§µÖ4¦vç\x0002\x001aCÍ®5r\x0005,!\x0015qØ\x0015 åäÀ
\x0011É*gûü\x001eüìô¢ª\x0014¥\x0002ö	bõ00\x0005óÄX²?Ç²ú8~:>§*¥Ó &ßÕ8Jüpéæ³U>7ðf\x0002\x0000\x00157¥y»_Züþ±fÆÏ\x001fç\x0018ø"µ3\x001cª¥ZV
3\x000f±\x000c\x0003<@ÔU\x000eD³3õñ¦í§XxE]*\x001e\x0001\x0002\x0007\x0019Î±\x000fæ\x0014Èf.\x001a¡H\x000e\x0013 ¦Ô\x001e 
\x0007À>\x0004b÷àiFÕ\«*b7Bzê\x001c#>7æxfM\x0011¹AØ9Í3ËÓs\x0002XàÞÆÒah6JAuí\x0011+ÕPM:i]­Kî
\x0013©®\x0010Ò\x0013\x00013\x0002ÅB3\x0002u\x0011è¤àõb/E\x0004£/4W17¯®Æ1O³¬V3*Ìö.Ý_`Y5°[{*ÛG!\x0015\x0011é$Ã
dg
O+ä®\x0004­'." _o\x0004zýü=Òªrèô<Cè|ýys½\x0019ÐL£Ðý\x0007~\x0011Lÿ\x0005úT.\x0005-*Y´ËÅùòÕÑª\x0017£\x0014îä\x0001\x0006cT
Çq\x0002Ï¡h\x0005\x0013ä¡Xâ\x0002<x(¡Äé	(µ";É(æÏ°Ô»ù@Z\x0000i§,¥ÀÏ
-"x*EVÞt1õéZ\x00120þÐÑ\x0001×T|ÅÈFÞS\x0003\x0015ä2xn<RÓ[\x0018»V\x00124â´sÂZ2Ïb©WL¦qd´åÐ\x001aBù]-æÄé\x0001§°Ì`W\x0007g\x001fïw0Kö¸G:ypÂ¹æ:±Á8%wA\x0015@ä\x001aãèÜÑ\x0019\x001aöù\;ÈÁtìø\x0018½Êì9*ZÑ{V¦Õtê=÷ó­¦\x0007v¹ø\x0018\x0013\x000eLý´	'òS[ÎÝr\x000e<\x0012þ¦çè]\x0004±´2lüå
ÚÙ\x0013hmçó\x0001\x0015\x0016Iðñ\x001fÞzî±ÞÄ(HP% Q´`fBé"J7\x0001¥ÆÚÂ`Ë=V!p¥¯Ã*\x0005é< c\x001aJ¨ñ\x0007º
>P.üR>]¹í¶\x0010{L\x000bHÏÍf\x0003\x0003Îâ.?w\x001c,{÷®×\x001ayK%Qá\x0006,¬<vgÓ\x0006ê·F±Éüìe\x001fJÈ\x000f¼ÐBN@É$*8¸Ë\x001dØ\x000eJ¬õÕ\x001cÓó\x00001>Æâ\x000c	'\x0003¼T¬Å¢ÕÔÆwx!\x0002\x0016á¾Êbq\x0004\x0000ÔsZP\x0017vy>0Êl-ï\x000e\x0008ô³bï~YwH!ÒlO8êïjs×_\x0013%-\x0005m-,(RðÌÁ.Mç Í9_\x001c|\x000f5ýá\x0006²«ô`\x0006\x0011LªR>@5&|	ª\x0017\x000eF©B5\x0005*ÒòN\x001a¬§D>2ê¹"ÔÌ\x001e¡jD+S "Kß\x0014¨"Óx\x0019é¾\x000f\x0000¡ÖÛ'@"\x00061qU\x001d¥Ã¬qÄ(¡%Bl$D\x0013*Î?\x0000Õ0ìÑa«ç\x0001-g¨5Í	P
qÊª*< 4ôUÓ\x0014\x0006çVhSa\x00025\x000e*f\x0001tfp´
zt.9³z\x0016\x0005¸¹»ºÿ¼ùbÄ_|Õ\x001f\x0004å
wlË\d\x001c-§­ñ\x0001uf]õën¤à¬	Ï\x0018\x0001±ÓP£oÐÕ>»T\x0005÷ðûGáÞv[tò°³×ë«»Þ\x000e³°o\x000c\x0015\x0015BôÃ\x0013õWkT\x0008²lözyx¶³¿¬\x00032q¬\x0007É3?ðÄO&}\x001eqÄ*\v£A~9fr(Jy~y¢
0m\x001eûÂ+\x0014Zãaâ¼)_\x0006 \x0005ØÞò(+Æ{-å\x0018Åé3\x0006¦Ý£ù&*§6ÉWjã£Æ£ÄÁ0£QZ·\x000fO\x0014ö\x0005÷®ñ5\x001eêÑ0¡ýHê)0%vÄÃè\x0013½o©ïu9{AÞ}p¿©§-Ñéí§!ä_<\x000f+\x000eÉ1_¼°æ\x0007íS¨íÇøØ\x0010
Äh"'oä\x001d\x0014©7\x001eÙw\x0017rR\x000eÃH\x000cÕ£Aæ©-JSöB\x000bµe\x0013cá\x0006À¨i2\pÜi0`ù\x000eT\x001bÅ3\x0016ãr\x0018FiòÈ?Ícè0MÏÈ kÜ¯£Aâ±Ñ\x000b)0\x001a\x0008&5Ý&·4Ì\x0015"Ìa\x0018!k7Þí\x001fôÑëÅÅ\x0010_\x0008¦&ÐZ\x001aY¥|fÝv\x0010±ërq±Û!ÊhE\x0017­g¢\x0000XY,\x000e\x000f·\x0008ºQÊÚ>\x001aVvÑÊ)he*XEj;\x0005R\x000fãã\x001eVuÑª)à¶\x0005GyAÍ2\x0007·ª\x001dîÐÊ7úïæÃ?~ÙIàÉm\x0002(\x0011 Ì´üó¿¾»Þ|únyýqó	:\x001eðQ÷E@\x0001	Ø®k$êA|0²rõÝÑêü»åÑéê¼ ¥¼ºy{{só°É?|ò)*Ï¡(s\x0019\x0000S©Ð:Ìñ1\x000fÆ§8=\x001bÆD,û¼1&:ç1q?omüycL®æóÆ(Ä7FýæÇ«O°oàÿ=C¨ê½ýlY×o>-Îo\x001f~}ØÜ\x001a\x000cR\x0008ÝHÊ\x0001Ç«(µ¤;a¾râ¬Î\x0017ç'ÿëruq¾\x0013'ûûø?º\x0007cÀ¹|ûv}¿\x0019\x000e\x0013®kèxp0ÆÚ\x0004Í%Õ{Å|\x0015åòà`	Ýo×ïÖîï6ù\x0007\x0004i~þíýýU\x0001rqpûðþf=b)¥ÇÈ 
ÎÚK\x001f\\x000b\x001a{È#ÓÑNËWÇËA\x0018é?gxv?kxv?kxv?kxv?kxv?kxv??>È?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=]}ó\x0005FáäX¶3ÿÁ`Ñí¿ÿÏÝê|¢«¢àhÃÌÀ´\x0006°æ\x0016qP´ùd\x000cÕ50ÜááÖ¾:ßë«09½ \x0012¹4]èØû\f»\x0011SL(¡GGûOz_]\x0010
èÔ³ÐwZ8ÎEGý
ÚyF¦MèÎòÎñ 8\x0003Ý\x0017è¾\x000b]beuçÊVB·4éJ/\x001f)MäAx½\x0008Ñ\x000eçµÍ\x0006Û¡|º#\x001di­+WÙmìóÍìÊ÷±Ã2¡i÷!=`&vv'5²Ç½oÉ8*Avrî]æ\x0002L`7~ÁÕ.IrÙ½êb\x0007#ãhÍøÜP\x000cØ1gç]}Ù\x0015md/ç½s«¡Ë³ÃW²®\x001d/wkD'U<F\x000f²\x0007\x001dßÅÐ´¤­*Sv\x0015²V:²/i eÐ%{×ì(~JìV1»\x001dØ¿ì\x00176²ÛÝö±ë£ÈìaXîÊ\x000f&Ò-iÞI_`w½ËÝ0{L)8i½gé!d_Ò\x001f¡4ï¡Ë¼(è*áHi«iÚ
[wï\2T¥Îè1tM»±ì\x0001®NUµKæì>~ÿÃ®ü¡s·Æa³Èu°ïqÉs\x0015èovéo:éü\x000c\x0004üvñê:]#ã[À4û.ðíÃ/\x0007Éñ¯vñ¯º,NÈÙ\x001bx\x0003Ã¶5Òð
$,iq\x0000³¿ùþ]ú\x000f]kÇå¼D\;9\x001d.­¬¿°göý»ø?vMs$óiec§\x0018+Å\x0008Â\x001bÁ<üw»øï:\x000f,öéE\x0016*A|jË¥³qáûÏ]üöÌ>ö`¥£\x0007rZ<ÛØÓ\x000b=\x0010ÿb\x0017ÿ¢\x0013èÃ\x0010y\x0014$}þÂGîû]ú÷½úá	á\x0011"Eùwâ\x0008øGíCÀ\x001alA¯;Îcíx
FR,ÒÛ¨tá\x0007ø¸û\x0003|üznW¹Ù³úµßnÞ0,\x001føØuYüu9üwñ^nù«ÏWÿÂkç_»ôÿZêØÍ¡îtìÁeóËl^YxBo£
ð;k9Î@GòÕë\x000b¬q~\x00163bóÚZzêÖÆe'
Ósàªò\x0016ÑW¯O°Àùí7\x0007ám\x0018ÃÛÐ\x0007/)¬\x0000ðN§`Wt½uR\x001e¸Ïwj\x000cïT\x001f<ÜÍSÃ*7G4ñ(òFì~¿·0=1{\x0014]ì!Äí§°±Ö1kãÎ¢\x0013/E\x001cÃã×.zîøkÞ¥ªK¤÷RòÔË%§^ªbÃâ×.zárá\x0005ÐË{^\x0005Mô°a÷TséUIß·êC*xÉû5{ÈNq\x0011'X\x0012]èª\x0013Ý©&Ó{CïZ'z]I_i¤w® w®\x001e3ÉVúH+-½à¹×~ÿÝp\x001e½\x0016¦8¥é¢Ç\x0007\x001eCÆ\x0012uYJ)ÁYòÂ_rL¯:ém¶6\x0006Å\x0004ò²\x0001;ÏþP@g\x0016ºDÃÒVö°ëÔhÊå=\x001bDÎÓ?Â>ð-é,ÏbÔ\x0014{ðÊ9goSC\x0011ÀÁ)Æ¯äuµá;Yâã÷\x001e|'L^÷à-Ø}O1eÎSávÁ/ïEá%¤ï=øÖ\x000bì°sU\x0003åªÂU\Ñì»¿ÿZ2\x0013_g\x0015~ïÂ×.\x0017¦DLz¤l6ðæéÙÊE} 6\x0013?¸\x0012?ô|ÀW´u\x0001_«tv!¾)\x001cÍXìlËSD\x0015ØúÃ
-;\x0018}Íìï`uPÞÀÊX:·ì¨ÔÔ1XiG"2ù\x000fPD\x00063=ü)O/6\x000f\x001f7wwëIIÄÊR}V
nVtd\x0005çiöá:QÏ4|ööï÷ôbýöõúÍõË=Ä\x000c\x001eÆà¡\x0007ÜK>kq\x000cN\x001cØàcÊàÜ[Ü¬Ö\x0006î8m;*äÜ[Oä²{Ú\x0000î
p×5ã:Ë"¸NòíiÊ\x0003»ôR×{ço­$£ì |¼ªÔæ\x00139]\x001døK;=&Ç³£ÊÁ£\x0014\x0012¾£0~ÉÕâÕâºVKpc\x001d5Fo²a"ð\x0006
¶OÙ@\x001e\x000bòØ5ç.¿m\x0002¹|
my5=¸\J[.k\x000eîKzÜÉ?Ñ£dOFÊeÑ}î{ÐMn\x001f
÷Ü>:Mºe\x000fX\x0006ýe\x001fìËä9\x0005·­ý_;°#½GáOPµ\x0008Ì¸\x001f\x0005KnP©BÞubW<5Üµ
-\x00165d<Ë/9ÚÈ½(È½è ×Âåê\x0014×ódZ4å:9\x0014/X<ä¡\x001cþ	]I^æ\x000b;\õñ¸\x0011=è=fQS!
¢k\x0002\x0019}\x0008ÍÀ-u9t¥
+kÐ·ÏzRsÊÆE\x001eÑz±#©Lù6p]Ìyj%ß\x000e®|:9\x0011ÜEìÛÈÝ°ÒãÞ9+\x00070ºéZéF±uÁn\x0011Ð\x0003\x0015Ù8U»T·¡ûr¹ø®å\x0002è&;]&òÕ\x0002.x´ÐRKÇâ4ÊRôÍäÖPý*\«5ÿeM\x0001Ý\x0005×Þ\x0016$\x0017]\x000etC¯LÆYÊ¼5É\x0018Ò\x000e­Ä\x0000Ú¸U±ÎñkÇ{J\x0007)ÇJ§\óbqzÉ\x00197ÅbÁ¯=ä*kF\x0003ùvÒñÞÉÃç?öû\x0018\x001eÏ\x0005, ß-lt\x0014o4Âñå_J°º
½Ü¡ºo¢nTFwR\x001c)t§éB§Õ×SÆ[ðkÇ\x000eÍ\x0012	\x001dþÞÄ\x001d(ù\x0001¸ã;ÔÈbâ×\x001eî\x001cQOSÓV\x0011=aÊ\x0017¼\x0013\x0019]ë.r-²Z\x001ak*«S?»\ÚÈ\x0005±9Ç¯\x001dèpçÏG¨£®.H®"½\x0008h[É³j#//\x0017¦ëríÛxZl;¢\x000f~®®%¹5¢Û\x0012½çúo×e\x0017=ÉGBç\x0007½häÂÄr½Ä¾ãß\x001c\x0005"×ÙC7pI\x001cÀíVÑÊ"´_ÛÁ­Ê\x0013ä£EF¡9$t±(º.Ñ{Î"\x0013ì`Ð#':\x0018\x0019,\x001bÆX)ÌnC/½.ÛåuYêEô2p4h\x0016"¹]\\x0017ôÓ>é(-£\x001bu~î2Jp*\x0011\x001cÈ6tS.uÓµÔe¤=ê%ßèÒ"0y%»¡Ü+Ýö¬tø'p&W&=ö¦MÊÑÈJe_#z(Ñ{¼.«|nðèrfâØ\x0005þ
\x000b»Â¤ã×\x000er­rH$÷$\x000f\x0002äü´µÑ\x000b¢a:Û\x0015¦³Zc7®-U$¢\x0005oÒE½]Ì>\x001f£Ç.ûâ=ûAm}\x0000~¤³bÉx´®$ïy1²ªaÒMH\x000cpÒÝ`_Ì\x001e\x0005ÙèN\x0014ë\x0005¿ö {N[óNpÜÊä±bAëâ*Á»Lº¡vl\x0012á´Es&7ôÞFrS÷X\x0017ç,':§sb²1Ã»¶\x0015}¹6òòÎu=ÒY£9\x001aíÁcÌoº0çFórYòáôÎkt×9jÃ\x0011¥Æz*EAô`Ø¤\x0007µ ]t¦8Gé:G·ù">\x000e~\x0016] \x0017<`u\x0016è®kÁÀ*ÑdÒ¥¥\x0002\x0002@\x0017\x0014î2qIïÅ\x0012=ô §\x0012ÃlÓ\x000f¤Te´áÚ\x0007kôv}éíú.o×)K!&¹d\x0004÷,£õK¦\x0004QlÒ z6©S¯u\x0011k~h¥\x0007¾\x001cÙ¸G<n>z\x0019ª\x000b]¡:¸Cpò:vvå\x001e¹ÜÄ.ºÒC\x0008\x0010º\x0012\x0001\x001e¢é\x0011S\x0019<Í:G¼°^cAôò©.t=ÕáQêóQýF}ö^Ö´Ö]Ê_\x000c½\x000c\x001b®°$*\x001a1)\x001d/l\x001fIènãlôXú±ËgÄ\x000eP$%&¤£Ì\x0011c8näüÏé±L`]\x0019\x0018,"i%!s4#Oz`ôX\x001bº*:~íô£u\x0011»ÓÅ:M:?z¹P©iC×E\x0014~í@ÇÊå\}*â@\x000bàbXð(¶HcÀ¯\x001dè&gF!:\OMöx­æâ\x0012¯tÖ£+gÝuÍº\x0016)Õ\x0005Ñ£l]c\x0015¿ïz¹¤³\x001e}¹Ö}ÏZ\x000fÊ²P\x0005ü}ì{Á5C³m\Ðá¡°ê1ôXuìy¢izK¥Æ\x001a>K½Z0Ò(Qy¾w°£rX®%üa£¤Mº ç%E\x0019!Mß;¸\x001d½\x00028¦×e£}`2¸5ËY\x0017@µ;è]`ø$¿`ó¼\b¥`³=ì°w]\x0002^hÚ­$=
ã04JìzÉ¥\x001eEÉ\x001e{< $;_péà%ãXÿÙÁØ\x0016w\x001d¿w°k{O$e\x0014[\x0018ÇúU.Ô¤«ÛÐc^\x001bÚÑQý)/wåòQêM £\x000b\x0003Wª\x0004Çï\x001dàaè	¡¥àu8aB5=ç,Ýã-ÕÎbQ]%*Á\x0006FÅp\x0014s0À¡@pÁ¨Teè(}ï@×\x0015c´RTßeàj£h\x0016Lf;É²/1hÇ\x0002\x001aSëÈ¾x.ÄnO7\x0006öy]ó\x000eÀEÏs\x0016\x000fÎ»tÌn\x0016ty¥\x0016årÇï\x001dìà
DEóÎ]&L0ÎÓXÓAmb7eì+}ofW\x0002\x0015æóyù6ûëQsp\x001d\x001cÓ\x0005ç\x001dü£ÝvÜ54\x001bÕ!ë ©\x0006ßr¯x\x001dp\x0017<OÍ/`z|\x0001%µf]Ü\x0016"©\x000b
k&.9ï¶|\x0003Kß;ØÌ5°À¯\x001a¤\x0006é)Ô§òÏåØËiúÞÁ]ó^5àJZZ3üv/LÊv§tÊöL¢rÄîÈ\x001f@90îÃ!\x0017;\x0002«Ùaï¸æ)\x0015°ÔC\x0004c`¤K	ë>·\x001fZ\x000cÝU¼ø½\x0007Ý²4Êy\x0007vz:\x0005v·`HCy¹\x0015?µT±é)Î0ùÅ\x0019ª3¢âº\x0012µdf©sv+¿É/yïzò<'\x0006©¨æÎ¨8äÄÄ%s¨	ßßï>¡Þw\´í6ÍAsM¯1RòC¤ªÈ\x001c´\x001a,pÃ§Æ\x0002ÀO©VJ\x000e¢bÄVO­\x0017MkzÌî\x00080E¦k\x0004\x001635)c\x0003îßtsÕ\x001f&ME\x0015¬y\x0001½Û]@=Ëß\x001b\x0010\x0008Bs
¡\x0016óªÂ/\x0007hzÞí\x000ezm"\x0017\x0012X\x0011öÈaIXýKFT*éñÙAïáú/\x0002*ó\x001d\x0016Ì>?\x001fE³NÀnnvífÕ·Îp¶\x000fv\x001d£« \/-ÛMµ ½7ª¤ÇL\x000eúÔï² #ÇÞÀIËÏÚnÉM\x000bçÃîÂùÐ÷fF\x0002=øf\x0016\x000c¿
+gÉª\x0002û÷»sÿ¾çq[°\x0003¶j\x001eÎ,Ë+G-YB\x000bV­Ü´ÊÑc0cd\x0019QæÒP\x000c¿9QéÀÓL¿Ù¥ïY÷p)\x0014\x0013¡¹*æDø~ÉÓVîÐcuD\x0007½A=\x0007E5\x0006s#åPØ\x0011Ï½"ÇN>ulÔ\x0018ÊM
Pð\x0006\x000e-MªNÜüÈ¡Ä²\x0006çb×à\ô¼t\x000b²6ör\x000b"ÇoÜ<\x001d	þMalÐ¿é06©DÀâ\x0011e\x000fìÆ/y±Âåþnw¹w\x001a¬Òç2I§j ¾è%\x001f\x0016°¹x\x000cÐuL<vÃµyÁÛ\x0010hæq\x000bÌKÅ#êÝî\x0011Õ1óN\x0006V\x0004\x000bAó»\x0008·ûrÖl<¶ó\x0014ca
õd,ó{q\x0007à·º9\x000bpziÂúMiãÉÄ(ÎÁ\x000e*/Ög{:9\x000f¼¦à5M¼\x0012þAtñ\x000eJXÖ75~À­øfãëÕ\x0013-\x001aquê@
´\x0012\x001f²ìUÒ\x0012.*/kÙ5­³+#]J7\x0008\x0002`Ú36wY7\x0014¼áO¯+¦×µN¯\x0015T×\x000bmX¼Öh\x0000n¶}\x0013¦ñbõÖÕë²²\x0001òb"ãZrZ­\x0008\x0007Äx§ãú\x0002×·N/=¨\x0003®æÞyÀ«\x00087\x001eî3
7ª1nT|vÇÅ]ë\x001aq± ,¯\x001e¬l\x001bâB¦WÊbzñk#0kt\x0005e\x0004µ'\x0006`*ç²\x0012\x000b/\x00006^\x0017ÆÌëV`KU90Ã.\x0000ìÂ°\x0001)\x001d;>yß=úU1ö43óûÇÏ|±Ë|ñø?ì2xüÌ]æÍceöÙ*o\x0006üÁ\x0013´\x0019ëO\x0017×©ãýÝêüÇÛ§\x0011K¥8ÂÕä\x001f§Ò,0\x001f\x0015'hýÝÉËÔóþÍêüÛ³\x0017\x0013·ÉÁÈ¹ÁÌÚ¥ÔÄìXÕqG\x0017`_væ3Ëí3½O+C4C\x001bÏjU`ó©CEò±ÙÌ¾\x0019ït2G2¤\x0014û¢/\G¿\x001cï\x000f¬¶Bæ\x0008_['Ù\x000f©Â\x0006d«ÈC\x000eº\x0012\x0000h`ÅbÆ¯|u9Éºy\x00149á\x0017Kån8ËÄ\x00050øbÐ¾öíÐ5\x0011Á \x001fÙì\x001d\x0005AíF1Îøå¨\\x0003´U\x00054^z\x001b¡QºA
3-òL\x0007)®<5¶@ËÃ¶ïA¬SÎq,ì£sï´7ÔÞÏbÂÆTè/'÷\x0012qy¨öó\x0004\x0015Ë\x001fHë¨m\x000e²c±nc2ñ¡iÞæ'hL¡lö´\x000bQ\x0014Ö\x00134¥Ú¨*éó¡µ,\x00164~m6Ëï¥7[}oÉ3­\x0017;\x0005µ´%t»½3CS\x000f9\x0004fÇÐ5¡é\x0006hU¬éÔË©\x0011Ún×tà\x001aj\x001d8\x0013\x0013 +-´Z }	Ýn¤ñÌ¦å\x0011ù}\x001f 
¯i[\x0011®mÖÅFÄ¯­ÐN²c§°d\x001a\x0005PW	\x001bÝb§¡Þ&\x0000&fVfO2û
\\x000eIÈÓ\x001f]å5¼¹\\x001c¦}q`Ç\x0014¶)U7A\x000f+º¦ÅÐäõ3¶ØóÇ?juþ\x0003½\x0008b}º¶äüS= 8ÿ¶ßìa£d|(\x0019.Ø&3s?ü¿ÿú_ëÛwÿþïÛ)ï:\x001e­G\x000e5\x0018x`âV\x0002\x0013¼\x0012]ÄÇ¨oVë³ã³Ã¨¡@
¨:õÄ(¾à²?-)lkÔx7©)&Õ4N*\x0000åÕ àÚê³7bê÷\x0014>MFµbjE#ªI9µé÷wéôK¨bÕúCêtRSFRI\x0002ó@*9\x0011\x00183<yR@Ýì\x00115ª6T©É1\x000eÂiþý\x0005î¸Gêa*é(ú¤R¶¡¢ \x0006m*"l9sDøa©=#ÓYuÉÚ¸­¢ó\x0017X5I:i\x0011HüÃD½'µk2ki«d£±B5!\x001f\x00150\}\x0005\x0015\x0003U·'k2ª.n[\x0002p#\x001eV«5ÔOPEíy	ôÛ*¹
IdRÛ6©àk2VÊ³	\x0010<0\x0013Õ\x0002äÉ¬¦°«Ò´\x0019VçÙ	pC¡YÕ;¿\x0018ì©ÖÏº-{M¬\õ:Õ©T¬°ÇòµG(e\x001bpeê	Q}9­¾qZ
Ç\x001c| ¾µÄ®\x000c*§/ÀZN«oVpXòÃ­ÇvôF\x0000?\x001a\x001d\x0003!T\x001eg±Æâp±ítuÅþ\x000bV*ÕFÔ\x0005vV,Mkl4­à\x0008\x0018Z\x0002A
V@°Ë\x0012ö)ûMeUåñªZWm\x0007V/HîAEÖ\x00071p©é_®j{-O¬Ê7/\x0001MKÀÙí¼jBu{ô&£êbg)Ý¸³°Ù
M«öïª"Wpbírÿ¡¥ôÎ\x0005«Íkq*ßê£á\x0006íà	HÃ¬{ª«§³ºÕ5Ï« %\x00006'pã¼²\x0019¨ef±Úò6h\x001bÍÔè1U¦ÕI;,zmÚdTW\x0018Wå\x001a«È@DÍÝ¦\x0015¶A&P]		Ì\x0003µ%h£\x0012F@ÙÃI\x0015l®´¬+0Lfõå¤úÖI)ØXMz\x000cDVC±|`Ý£t15\x0014^
m^\x000b\x0016ñ±
@\x0011\x001dbÕYk!üY¬±´­±Í¶Ú\x0000Ç«É¬RSÇ"ø\x0005¶­j#KÂ\x0006hÑ\x0018\x00122)ë>E\x0004?çH3Ü\x0007Â\x001e5ÈÉ¨²0­Z¶V¬h³l\x0003\x0014Vl­0,×~gPÇ«n<^­Wô¤ÌK@pP0¨=MÎ¦³ÚµÍdYÔF$W\x0000Ö\x0000±\x0006çØdÉ\x0005V«)§Õ4N+úØ´³ÀxeY!\x0015¸,\x0010PM¿×¢}¹\}ãrÅ\x000cï|\x0012¼¯\x0014¸Õtdù}ÒAcaZul4­ÂçÔn\x000f\x000e*Å¯UTrf|X ÖfDq\x00190¢í2`ð¥+XÁá÷\x0017Y½ïÿý*¦\x0015¿6±\x0006®Qñ\x0001£Ùy^Ñ%V·G¸`:«-YÛL\x0000²*Z«p\x001bÌªy^mXUóª\x001bç\x0015ÃB~`ÍÒ\x0014üð[Ö~oÐO\x0003¦ñm\x0000ÛyZ¯Å·ì
z³Ä¼öÊ4Ú+\x0003i³mEÍ|÷W%\x000f¬{Lf
åëPh»\x0011b¯¼Hó*\x0005uVV^3ª¶\x000bLkùa\x001a_2Pë&§Ùù LZ
Ê¡\x0016-:Q­(V«\x0015­/Y¾/hK_Ð6ú\x0006Oÿì_y|ÊÊ×,ÇÉÃÆ«=BHYË×\x0001Ûø:
Y´\x0002à¥b\x0019ØVæÕË\x0005\x0002®V/ºíJ¨Ã°±<V·f¿ÅYgu°×tÖr
4Z<¶j »\x000f$4­¥´¼^÷É5Of-³mã{¶ùe\x0010çÕFêK
ë¥aíÑ³Ì\x001a
'\x001b¿¶\x001d\x0004t
\x0008}Ä\x0000Ú¼\x0016ý6ø³-Ú
³Æ\x0000Ê¥ç[¶\x0013ì_íSJêJ·Õ5º­Z+*\x0014÷pFñ
Ë\x00067 îÑ\x0003ÎjJÖÆ wW\x0016PõÆó«\x001f^\x0008\x0017p±,V\x0000~mcUG³6?ÀªhWE¹@DÀÏÙ®õ9\x001b3#)z\x0011\x0003¿\x0010Ê!.\x0018+9³PM¹\x0004Lã! =óyl¸8\x0015\x0001t\x0008¸Tw×ËêË­å\x001b¨O"N«åÔ^\x0015Ã0¯\x000b­®tZ]£Óª­£¾·ÞéÀN«ãÌ6cégõååÕ7^^1é&'\x001f\x001f`8ùBéÀ>ZÀÃ\x001bpÁêÚü\x0000e$?e¡Ì\x0007qüìfÍ\x0002Ö5â¢_Û\x0002X\x0014r|9¿;ÅÚØg	r{ÅÂ¯-¬Ò(jräSS²ì\x000bhMU½p·­\x0014'Ìbu%«kcUpaÉen(ìNr

Æ@¬Æ.à·Äò>\x0010\x001bï\x0003
S/³7­\x0003­WÁ>¶ImûzYwÒð\x001ao¯8¯¦Õ$U°ªxVû½VTÂ\x0018¦ïMË5äDgd0ÃùJ¨} % kõa³`Ë8vúÞ\x0004ibU»@/¯Zsf\x0013¾½ö¢ZñYP 1*\x0000KOXeòë«\x0016^³Éôòöåê¤!àº-*æë¦-Þ¦(½Í\x0007Å}Ù7Tè»>,\x0010\x001fÞÖô3î»&\D¦H¦HÁ7¤\x001d\x001eà½]à\x0001\x001eNq~>gd²¢êìçí@\x000f0))&8\x000eÁ×è\x0016H!ÖÒí"ãa#²Å5A/qÃÅ!ð£¡ªÔ«ÍãûÛÝ9Æ?jÍx¢¸FàbØdCî³¯lÏ´º-\x000b´¼¬±\x001eb\`Ð\x0002Å7x!×ô?fÞÅ¿ÿåa³3Ïx%§?m9Þ\x0006©K\x000fsMÍí\x0014F÷\x0002¡¹ ·:\x000f\x001cùÐjÎ\x001d¸GzR\x0002S<D¼ô\x0002\x0006\x0003çygeà$·.\x000cã\x0001\x001b1ÒÂà¬H\x0017\x0016&à\x0004¿Ûà&üL°\x001a+¤s®Q\x001b.ÜÎÅÖ¶	ÉQq[ \x0002ªÆÂÄÛt:;)(IÚ§þ@Dëõ"¦XÙ¬
:xX=ªT|X=½ý÷ÿ½OÐ'	Àà¨;ÒõÁòr0A¸á\x0016\Ñ>çZ´·«§g'ç\x0000²~{\n;£ 9~í`ø6J¹¨\x000eË\x000e´6¬>PÄ?]o¼\x001d¿~5óî¶I_È_{æ\x001d¿(íC[V4\x0004®já-ààÁñk\x00178jjfp\x0015ÕÌÒÃ,ºRmTÐD¾M\Jäc}\x0006r0Ë\Ñ À£&1<°©÷Ñ^¨\x000e§}úä·¯`©;eKePøR\x0019tuvñþößÿçÃÍ\x001fS¦<å¹#&©÷%½TòËÂA¼iuv\x0002àß¼úÇAèík!Bk×\x0001mÒ«6B+Ï®¬§¼L/u%)¯\x0001Ú\x0017Ð¾\x0007Úçì<¶bè2\x001a(
ç¥­´jÞZq.´,gB;Ét-JíYÔ0\x0007ÿ¥ ·%1\x0008\x001dC\x0017´ÏÍl`\x001dmøÂ«#Ø\x0003¡¥,ñk+tp6\x0007ê#Þ\x001b\x0013²WôVçU­B®\x0001yÛS<!+Õ,;fy\x001b¸\x0002u¥D¢Z\x0017\x0006\x000f¿¶¯\x000eº*Æ\x001c\x0004áåAúBo\x0017£Þ
Ö%êBår&µQ9g\x001a¨}HYéÉäÑ©m¡¿ìs7Prö\x0015â\x001dÝkp\x0008À\Ç0¬ë¥ c	\x001d; MzÕM3mn1ÚÌÂLÿêÞn×\x001bÇó}|³¡oQðU¶;»Ê@íã/àÌMag:«l ÛîvÙ>ó8sÕu^Ã/vHT­µ"\x0018rÁ53èöÚS\x001f?)(¢È?óª-Ï\x0001~ê¡K+°,µ4X¬:\x0017±<I¨VPkÑ]Z,ØSðjÞç:õ~lÞOâç
ê­wu¥&\x000b>\x0013´~BHÈ¡\x0010<\x00149y9{ûH5ù05ú¼Ï\x0014.XH1rS¬)1ä9Ó.ûuÇ¢OÿA?õÔ½!+õÄå\x0006\x0001ô°V¡Y¶íù25ýÔCgéL	Éq@H-Ã:ÿ4ØÁ@½` è+14
0´ç\x000b\x000cî\x001fË¬:mµ9\x0004M?õûá«5eï òT§0\x0011WSPá4¯z«Zjz\x0019¨kÑZWø-òFØEÅgd7Ìuv\x0017æÚsÞ\x000bRs7»J-^j¶(åyê\x0012Ý~ê\x0017£oýÓõP8g/¤Ì
\x001a2\x001d=«¨ã0×ôSKåÛ¢
\x000e8Ï2`ø</!­Z%å:åKgL-î$êÌqlkîi`k¨k¿Ù½ÃG¿ÕØèçÅ¶PcU1Èê\x0014@¹°wÁávczìD]ºê=×RDAö>Éð\x0004\x0013'¹]ç±\x001d,»þVc»¦¨@ØÙHÈ©éPÓÉ\x0016aoÊ£
2\x001cØh
rÒ¤à¸!°i]wÐàívÿp'\x0017^ú½P}sXSàP6Ð¿¾y~a""¨ºÑloLr§y¾âhç\x00162£ä\x0014ä°ÈL5F\x0007þæ\x0016ü:2âdC19·1Ð\x0002ÞñÇ±\x000eüí-ø[ý\x0006ÞZæ\x0013\x00187'0
xp\x0014Lïr\x0000ÄÊéOZ+·í2Æ·I6 3Þo\x0010¼\x000e~Ìa\x0010~þëÊQ@2\x001cã~±TóuwÑ×\x0007Ý«ÿ@\x0012÷zñá÷ßýØÄ>?}÷Ã¿û·¿}ûýw\x001a£% â#¼öä(Yü=Gà^^ô/>üäã/îç§¯>ûÓGþÑ'\x001fßÑþaÀ~\x0018°b\x0018¬[s.O,XØ+=S¹÷¸­\x001dÄìMè¹ÞWFó\x0013×ÕeàjEoú«1\x000eãN²v\x0018~\x0018_2\x000c1Ó8rOZt¬Úã¸Wn¡\x001e\x001dÆa\x0017#¥
_ÇÑºMÖqH`*\x0013=íKã\x0008Ã÷\x0008+¾\x0007-ìÐí*[îõo÷rÚÔã\x0018ÖxX±Èéa\x0013Æð¦Â58\x000e)>\x000f³âÒ8ò¸å.Øs©P\x0007äÚøRqWgsO¬N;2\x000c£¬8:\ªåª¢¶%z ÙÜir®\x001fG\x0019ÆQ\x00162£`û\x001e\x001aez\x0002åo°íZ;lWµ²÷²]$	Ø9ä®{ãJ¯t¼'­\x001e\x001f\x0007â\x0017\x000c$\x0007É\x000cÍÓx\1®\x001fá·\x0018G\x0018Ç\x0011V#IV\x000fPÎ]º\x0011"ÊÁ¬?@¬ã@â\x001dËJy\x0007HO(®»dö»I¿ÔKãØ
~ê8zÁÏ¥\x000f\x0012ëñW?Hâ\x0010?Èr<á^\x001bH\x001e\x0007²â\x0008IÀyõ`³T\x0008Â:íïÕ_kÇ\x0011Ç\x001eW¬ôd6=ÄÙc\x000e ¯\x0018~½7+$®X!¸áF®2O­!ç ãà^ñv i´¬´Â²bRi rù""&¹e×Æ\x0001ã8\x0016816×ªæöÉ­\x001cÇÑ\x0005 Êo°õÂhX°Ä°ø\x0000³u\x001c%·äÖ½êZí(Êp\x0003±eÁ\x0015$Rz\x0017ÃrÊ¼øá×ø
.èÎ\x000c®"ý\ð5\_\x001dí*%ÄA\x0006ïåê\x0007²-Ë`zQÈñøð\x0014ºü\fI7é%Mòs¿r\x0013\x00137e_Jtiå[T¤r¨ÈòYÊÑ}ü
¼\x0015\x001cÕÍ7¢!-ùF´}ù\x001eNñQ6ÐïY¿\x0017i9\x001e»f<Ô³o)¬\x0013\x0019Áî
ëoñ·ÃÁüÑ8QnÃ/Ò50?ÝÓ\x001cÖ\x0007n\x0013ÌáÐ3YëÖWµ'¸°\x0014ñôÍR\x00079[_Sv\x001dðü\x0007ôs\x0017ÿüâ«oßÕ¢Ìþ\x001fx>\x0010÷Å\x0014/Íð¨¬Ýê­Çø8í^°Eå_¿|ñÕG¯ê?½xõÅg/ïçÛ@rÊûäñU^9\x0010¸Ma£P¡g\x0013µ¶.ò­\x001eý±\x000eÀ@ôûÔ,³ë\x0003ÁJky\x001brá'düw±\x000eSrð¨åôùqP×Ý8j¿×ëã ~(íD¼Õ7­FÒ<i+>yû09åì@ì.J\x0003©¿\x0017\x0004D(¹,¾>\x0015b´HdÊnÒâÂH¨Eé~$µeéoÒZåR\x0012YÒxë2ê\x0013É'­\x001eH	ã@ÆäCí@¶&%xNC¤*ØÄ\x0003)ùÑ{èéø\x001bãòkËá\x0005,´OBorEö-^&)LT"/$d7~_\x001fgy3ê½ìJMé§o"U@)çI ûÂHR\x0018ÎÄúûúHH¹³å0âá\x0016Þ6Ò³r\x001dI
¼¬\x001eI¼\x0019I\2\x0012ç8C°jÏD×FâX#+áù¿ú4Aò|3\x0015ç{0¾©R\x0015¼è2\x0019~\x0013VõHÅO*(/d`ZGraª\x001d	ú¿¾eÐXÒ×jp\x000cOøâ&Íø®$Ü$,\x0019IÊ{~|m0J\x0003)OJ\ä4\x001e'ô{Á@Jl,\x0012ëË[VäÁ³äQbÐùaÜ\x001cïyÉñ\x001e²\x0014\x001bç\x001dKyã\x0007É²Úq«G\x0002v<KÀ®8K"%µB\x001dG7\x0016ÑÃ½àL%Äß~/\x0018áì\x0008\x001cI\x0006Öÿ´Ò\x0002;2yÛº2Æä\x0015þ|ôM3\x0007\x0007BZ±×¨\x0014e¼>JµTäæä%Û2ÐHcC¥c_6iò\x0000|e$[Ýr\x001bÉX¹¬\x001c	½É[^&¸öÛC¥ô\x0015¶.xy~$Å#)+n½ôÂÅ\x0004oïMØ\x0001?IáäL3Óº0âÇÐï\x0005\x0003A'>·4Ó\x0018û9tÕ\x0001;Ñ4ÑÄ8îõ÷\x0002ã
Av.ÒOh\x001a¸+\x0006\x0019IY~wfqÕßG\x0002\x0011EaMýg>Á§Iô¿ÁHÊÍ7)K¾I
O¦­\x0013iåM\x0018T¡¸YO\x000b#±øe\x001d	ý^0\x0012\æG\x001ermÅ\x0003\x0004©U÷\x000fË\x001fÏd¼cÕß\x000bFN¼|\x0013(â\x0006ãÍJ¾IÈÒ\\x00183£uÑïë#ÉÎ<qI»³rYÄõ#%íåa1Åù\x0004?\x000e$¬Ø©\x0001ÖRvj\x0013$ÁË\x0016§FeïÖ\x001bO\x0002K>	Xù$h[Üª\x0011-Y\x00062Ó\x000c¾0\x0010\x001f+Vý}} Hä8ý\x00145Úó\x0001'u#0\x0011l¿4x3\x0015ë½ª0r-ë\x000f¸öåÀÃB\x0012ÅHÒÍHV¸ôàc/B
w.<©¢|²Ü¥w7QT·&¡\x0002@¢\x0017­öZj¶¢¤IËøK\x0003)7\x0003Yq,R´´} ©\x0006ø\x0014¿Çò¸£óÑÃ+.&y\x0018ÎÕ^=8\x000c\x001b²Hä´ÜÝÚé2´a¤\x0015Ã µ\x0003W¸JÏ>µW^Ó+ÒDyõÊ8nN\x0011¿ä\x0014ûæ\x000b^r=¬VT\x001bß\x0013«ÿ6¤¬XèUKË\x000f!vÛòQ¤\x001c\x001eëO\x001eI¸¹%/ï@OX/%VÆ[/\x000ep(ëÝÆ]\x0013¶:ÚíúH h\x000c
ªeßÙÄo\x000c\x0019ÿK/÷xsÄ%§\x0008à\x0004
Ü?Iä6£øI&\x0015YWFnFV¤PG?V<±VNÙ\x0014O&	Ã\x0017FÜðîS/¸]ùôÄ¶®pkøgkÛ÷f\nù\x0017\x00013\x001eìôûê8\x0002åVñQBÒÂÖ,
%­­\x001eH±ãj§ß\x000b\x0006\Ëë ÎUERBÂ¤êD?\x0010oÆH]ý}} \x0016éè§Tvµ\¬Iæcõ8Òx$Öß×ÇA®¢oÊ$©¹ÞKñ%Ø¸ü<¤×a\x0018yÁ)B­e\x000coY\x0016=ÄºVp$èm±äK\x000f\x0005VÎd¼êÖß\x000bFØ:i\x001b¶ìg;{<ÔÓ8;àüpA¬¿/Ä\x001a\\x0018©Äá¿¬ªðáH²ãÚEðP0ðüèÃoD\°äNòdù(	+p¡;\x001f`]!³¤ßî\x0007c\x0007\x0001\x000be<\x001bL|J57\x0018çßs¦
. ¥ÄdÖ_°L\x001a2·{t~n¹\x0010 \x000fÐ\x0003ôí§\x0000½ï\x0001úå\x0017ßð+\x0003
\x0006¶Öõc\x0001\x000fþÄ>qðÝÿZ\x001e#ª¶ö<ÚÚó?§­¡WôOCÒOã¼cSÐ«íiô<\x0013zÐkù­Þlú3Ê\x0001Qµfn·d@r%ðÚ%ª®ðP«Xù|; Ê~^2\x001eG=ýlËöFRÒñøä,\x00167ë~qí¼\x0019×ÎÊµC>åí©~æO®&Þ%=\x000b\x0015ÃB«ÞI\x0010\x001fÜÚnh
\x0001¶ë\x0018Ä\x000fhß|ùþý»w2ïzþñÇç#ôTÍ
\x0001,\x0019g_+\x0012ØI.ÎË×¯_½\x0012øO¾|ùÅ\x0017/\x001fRûÚ_ ¶¢Ùl£ãlAï¥@#äti wî0B3¬voí\x0015:04Gé\x0008zÒcD\x0001\x0006èt\x0001Úû'ß6RK
ULXä)á>úë~»:Û=5¹Ñê©.²ýÛl91Öû(9@\x0010&Ú\x000fÔþÂ\V!JI°ebq®Ìuì$:ê\x0013Þ¸ßjÁs\x0001É[°¤ÈÓm%¡/Ï²bàonÀß¨g<DqI-´¢/\x0002Ï, N@O»hoU¦ì¦2U?üþßßlGÏ¡\x00164¤ÙÍ\x001c¦ËNà¼VÛUî\x000f?ùÓ¿È¡s¿NÅOqâeühX\x0017\x0014ÿÅ<¼R\x001a\x0001æ^3UÍ\x0008òð\x0001òõ\x000f\x0010LÝ\x0010ëÙé¹Ñ2\x001e gg\ü
öíºlmôrq\x0004¸ãpNEä\x0004<\x0002/#p;¦~\x0004Ã7ëßÀ¹a\x0004Í\x0015@+õ\x0011¬þ\x0006~\x0018¿>\x0002ßÏ*ÜØ,ä>;%Ú\x0001X3\x000c~^\x001d\x0001î>ÜÂÒ¢o`Ä\x001d½¤ªà½~^\x001c\x0002z\x0004}3Ê3T=:ô2xOËR3-6Y@¡É_Á¸'>
Rá,Ho\x0015;
°ø#Äñ#Äë\x001f!\x0005¬RûmU\x001bä\x001b¤I\x0010B=<~|ù\x001b$yññ.È»°\x0003\x000eá\¢j\x00080\x000e\x0001.\x000f!\x0004	;:¼Ù¦æUX+·\x0014¸'~£\x0019\x0001\x001f\x0001®z1£í­\x000f²\x0012ò=Q>Å\x0010Ü^Z×~@?¯\x000eÁ\x0005^ËÎz.ÆðFR5\x0013ÌêöÕ#°\x0019ÑÏ«# ®Ë®Ì\x0013ë\x0002ëÑ&JÝ\;ñHp\x000b\x0004¼ÉH\x0012:\x0019G`û7¸'×£\x0019A\x001a­(]¶¢HIØ<\x0002\x001fk>6
!Yöî½§/¢\x001aÂhFé²\x0019QåHârJ®PªºÆYpOR328Gôóê\x0008bk:WË(#çøzôÂÔ\x001f®ÝO)ô5àò~J\x0002\RA=×!á\x0008|H¹v\x0008~¯¾7å®¾¥\x001f\x00028iLçB\x0000ñE
¥Ýâ\x0011Øá#ÐÏ«#\x0008 >6¥Ê\x0000ë,#=\x000b\x001fÆpE¸|U.ö\x0000·#´Ï^w¿Ø½óyØP}¾¼¡\x0006°õé*òl`%S	·Åþ5õØá×\x0016\x0012×ð=á71
OâêMo*C\x0002â0	Óiâ°¦xy7uÔ\x0003§\x0015\x0012æT\x0013Jp\x0004)K${W\x0015W52àòVäð`ÛG\x00088\x0018\x0001L[-d¼§D®\x0019B\x001a?Bºþ\x0011ç\\x001e\x001cB½(yèCXmG)C¸¼ºl¸ª \x001a+\x0012\x0016@\x001bBäPê\x0000ã\x0010.»F.&Ì ¶Çíe\x0006¿v¼~ñ5'±»t=xçô\x000fÃ¯`¸¸\x000e í\x001em¨¨PÆ¯P®¸\x0016­\x001a°\x0019IMM÷Ä\x0015\x0003È~\x0000g9\x0004ìz{.\x0013½\x00113Úú#Û2ÉT×\x000fa\x000cÃ_\x0008¡'>+\x0005À%>\tR5k&½óÔ#\x00007\x0000Üå\x0011ðI Íâ\x001dÅzêÅç\x001aA`¸\x001e\x0004¶©?^*WeF¾kâ\x0008\x0016»Ø0,àzÈÂ¢m¤ú:òc \x000bÅö®ìaí\x0000!\x000cC\x0008áò\x0010\/Ö F\x0008íIÐ{\x0001ù=ýZÕ\x0010Ò8Ë'3=erçsêÀõ~j\x001ax\x0008L'õ\x0010â°¥ÒÏËC\x0008r& Íe!@?':|ú\x0011äq\x0004o
Ö§m)XnÃäHÁ]ÂâÈ\x0011À8\x0004¸<\x0004\x0012qåÛ&éìfþ
N\x0012\x0000ã$s^=2Q¹lFU½£\x0002Ü³\x0008GÐÏµ8I½Ñ\x000f!C¸\x001cCEKÂw\x0014\x0010æôrR\x000få!äÕ¹vT.Ú/{VÿH$\×ÐEïbq,¾¸a\x0008ôóòW\x0008U7¿jXxÏÅëA¯\x0000]õ\x0010Âà]ÐÏ«C¨\x0012Ò,^ÑÚ>Ò\x0010zcxo\x0017Ç Ë¸\x0016Êµ\x0010Ê\x000e
!;É±öI³w÷ú\x001f5vp/êï«cðYü\x000bªGj9x"ç.óà\x000bÖ1¼úûê.V2F2Þ?MQ«àV`Ö&íX{ó\x0019ìÕÏC¢1I-+û$!¤àÖ¾) r¾\x0019Âõ¯\x0010Ë\x0013m1¸î¨RkÚµCðe\x001c¿\x0018ÉÃ!x/<ê(Þ\x0012ØÔiü\x000cvéÍ9\x001a3¸\x0018õ÷å£!qOñÚÏ#ó\x0006)2rf¢5\x001dÃó\x000foßýÇ<7ö\x001eh±¼Þ|àBXØÊ´Ûmº¹1D¶«üñÄÜ²På\x0006ýæ²×íû\x0015ÞðÕ'\x001c\x0010ÙÖòQ¼½\x001dÅÛË£È­T\x0002\x0001s¯q\x0014ÐG±ØÛ Q<ßâù²ó
õh¨\x0016åY-\x000boY\x0018\x0016\x0016Gd|°\x001e\x001aÛ´7·ÞÕFÿìæAd\x001cØ'ËMS@ÒªJËoÇïA\x000f¸W¿G¤®Æ\x0008`ø:çòîÒâû\x001cZÕ×·Võõå\x0010íV\x0015Aú\x0006àj×êµû\x0014YÕÍKVu}ÇÞÊ*w\x001081Ã$) .Î\x0013#«zskUWwÜè\x0012+¬:Hò
Ô\x0002ÒDGîü\x0010ð@­\x0005u=nø`\x001aÿÛ÷ßý\õç§ï¿;@o\x0011µ	ÙC!ü%¤÷P¹Õ}üûäã/ðOõç§¯_~üx\x0000q?xy\x0000Þ4ï\x0003\x0007Eï\x0012Gàd\x0004ÓÏO\x000faÓÿ !Xsý#¤V\x0004@cö\x0002D¶å#<²¡ó#(Ã\x0008Êõ\x0011´àR\x001d²£$\x0012¥Ì¬\x001e\x000bÃJ\x0008×Çà¤c£× Äcà\x0002æDÙcËÇ1äëcà\x0018\x001cCjÁh\x000c\x001eC²ò«°iÈÐ\x0010¼¿:\x0004CÖ6ô"w'S]÷\x000b#\x0008!ëdø9
\x0001oÙÇBÿ
\x000f#\x001cgÆ\x0010o\x0017CÜ-¿µ\x0011|÷îÇ\x001fß\x001dêÀ\x0006¸
ÚJ\x0006Óºf¶z$îÀVÂ½F²¯>oä\x001f¿úâWw\x001a¯1t\x001c ã\x0005hÏo\x0008íT £Sdúþ5ú\x001cu²{êdõÔAì\x0004\x0013¥:Oé\x0017L}?·ö\x001c5¸=õöÜ¬ëØ\x001aÆ@.E4©æ®YwxÝzWgDÔ»:#ÅdKg+ÄÎ"¹ã\x00127U!ì{Îÿ9l7b»+ØâÞä\x001bzbìÈ9\x0001â½\x001e©'±Ã`#ôSo$á©Y±¥R\x001bn\x001c\x000cw/Z'¡Ã\x0008}eëK\x0002í[
NÝú@ ýÝÃó\x001cu4\x0003õö`¬ ö­1\x0002a{I\x000ewÒN\x0000±'-]4Ø[\x0012]ÅÞèÎcÛ&éNØv+\x001bu¬ö[÷Ýèí9ì\x001c\x0007ì\x001c/Ìvl\x0010Â¶'³--ÁNÔE\x0015ØÎ\x000e'
ýÔÏ¶\x0015#Tz(G>\x00025_G=º"V¿ s1U³ªöíö\x0012°©}w\x001avº\x001bÌ<½UÁUì­
î<6Îpë0LHRý\x0016At»O+ç¨a8i\x001cèO\x001cYH\x0013±­yJ+'­`ß¿ÂÃ.Ãöç~ûËt*rKt\x0017zÍj(ÒÚ¯;k\\x0019M»\0m\x00160$l\x00138¢ê­ÎçvÒ\x001eXA¦·§¦jj<\x0017KÛýr\x001c{ôè¦FÁ^çg{7,Hú©ÆvÐ[.å×41ms·îâ\x001cv\x00186í]Íb¶c«e¦fØð\x0002Ï¶í4®Â\x001e\x001d\x0012Á!É\x0016ý@zxs)¿)¦cßÍ?=Úv¼`Û¤$\x0006
z~I±&+"ûe×'©GÓ\x0017Lb
B]jN­Ï,\x0002½ÌÂ\x0005¸\x00065¹=\x0003(ìÛ6}sZ;Yã²ä¶´,;(Ñ2~A\x001fã%z\x0013¹{5zOh:\Òù\x001d&$¸'{ÖÝÃÄ}¾rÏ1ìÃâÙãYôÇçmÖ¸ürÚÍµio²|ÞÁgÙÊýºe>à-<¹Wà3k1kè»:E,±»\x000bÎÏèS=úÖHZÕ7=z>þéí7ß\x001ffÖ®Àe°·æ)Éq\x001e/Þã\x001e*aüåüäN\x000cË\x0008\À\x0008Ôs|â&\x0003¢¥ÿg	oÚn\x000cÄÆ\x001e'&Uß\x000båUFÎ:áË\x00020\x0015¥¥ì\x001dmMfÑÑÜ3¸þøùÓ@ñöP\x0013õ\x0011®s¾\x0006å·
\x001fÊ·ÞukùéÅßüü~|wPÒ&CÕ\x0007p²Þ\x0013õ"u\x0008¹ûå\x000fÿøòûOË7
¼IÏ Þ\x0006\x0014<ØÅÎ¬V\x0010MT")ýìÕÈ±µ+ d´\x000e~8³ü|\x0019íÌMU\x0010Ã@\x000czâü\x0004-òîç¢A$æTàhí&\x0005íN\x0000í¾çÅIf<µ3\x001bFN"èbe\x001f6<h=rÙ\x000fa½Þ2lbÉap¥½®Ö\x001b\x000cËuÇzò­aã<Gý<\x001b³\x0007@?Koè²È\x000bÐæ\x0007=Ï\x000e3ï5o?Úyv­á\x001c2\x0007èQ»bÕQ[Ãìy¦êy\x000eMð\x00133î\x001aVæÙ3ó£SÇw\x0005f®ªÑë]«@fz¦æ}Ãp¡ktqÙ<§qz\x0013=Ò5Û\x0008T 
|\x001dg}ÆXß0ûqýy.öÉ·yFúxç¸\x0012½®çyæ<ÛôóÂ¾Ñ^êÙËk.eÆ0s|ÐÕî03ï}#§çÄ­¨\x0001\x0012Úw"ø×®1øEÛsH#rÒ#P¤çiÎ\ÅÇ`Ì2Í«¶¸åT\x00103ý¼`Î±s
VBKÎ±Èk\x000c¸/böD?Ìµ½F3çDòS¼\x0004¹³a\x000c0Q5>ÜLÿ¹Jd×²¶\x0008\x0019/~\x001cÖ\x0010ýÍ\x0018Y´ÑÅ<ZFV[\x00068Ód\x0007\x0008Y\x001b\x0019¼0/³æî/1Q3çh:P\x0013h#Êù"¦1	:`N`ê%°;Hø\x000fèýéå½ûb/?½øüùýÏÿó_ï\x000e\x0010ÛÈ\x0015ä"q³å`$Õã¯Jtõêc¼|ùâó¯_}õê!p´{`º\êmîþ\x001c²·² üs
â7O\x001e,Î\x0002Û­\x001cé§8$\p|;)«úÐVäÚj)Ë~
q\x001c£ÊÞøn\x0002¦Ï±ñr\x0007t¢ÜÓÄ[6P%¦7kå\x001cÖmÌ¸ðm*ÂY5xkµkÌxR£Ö*|¤+ º\x0011îüPs8yã¯ûDçíH¬]yÁC{»¯¡\x0016#Ñ6ÑDú<°\x001b\x0016ØFq;\x001d²7 V'ÑüóÄe$.ê)vâÜoz8ÇNbr:
\ÆuWÔë\x000ewãö\x000e\x001ey2©\x0001;Yw&MäÎ\x0012;?¬;ú©]w¾^¨[ÐS`©¡°\x0010O¢ÊçóH¬=¢½d}\x0005÷$¼ÜÙ¼ 5FìÒ°OÐO%/U\x001c3p2\öãK\x0004,Ûäþiâ2,;ú©$Abh¼R\x001aP$s-ÖÒ¢\x0015Ä~»\x00121ýT\x0012;'\x0011"ë%\x0015\x001dDø#pïià0¸\x0014õ¥L	\x000câRXSj\x0012D%Ì¯'Þüiâ­7S%®ÍTÄÆÕÔK"Æ­Ó qC)$$}&aáÕTZ\x0015±+I ½g!J*cDîÏ\x0003»\x0011X{@;¼\x0012@wXr¦À\x0017â8\x0004;K\x001cÌpÞÑO%qÆ;\x0012D×§ØÉ+uqNà½-8íÞæR%\x001b*Uæ9îRÅÚ5~f\x0018· Þ*\l	/µö#Kç¢ÜÂLJ?N\x0003çÑ(²Ú(|ªg\x0006\x0001T½z\x0002ÎA²Ff²-çÃH¬ÝÛÈóa·Í\x0018èS\x001c¼NÌBX\x000bÞ>OD.yô'¿\x0019sK` \x0007y»KËTGS&\x0001ãàÙÆ±ü\x0010ÿPË\x000f_¾ÿóß[nË\x0017ß¾ÿî§÷G\x0012[\x0010Y*X!¼ræ«)GfúVÒ\x0002íó\x0017_|ÿøåë;Y-¼Õ¨\x00102möZäe\x0005&+\x001e\x001cÅj\x0005ÚN24Ð~özhJ	åH²*¦ÚpE 'ºg ]jÁ·M½*á:7}Ï?üáÝO;¸ud)¬%£´À,\x0004éÿh\x001e½´:ùÏ^}ùù\x001dfê<Pç\x000bÔ\x00168Ñ¬ø&^H¹N,\x0015A¹¹«íNè\x001fé§\x0019§·ö\x000eBæäÄc6Ò:ÈI¸EC½K\x0012 ê}ÀIjjÔÔ¢H
Ò5÷6)³4P
õ\x0016'ªÔÑê©Mä:eO)Q\-¥í\x001aê][\x0017¢NYO\x001d%\x0004jú\\x0007®ÞLuÓ^½]]+v)zlßäkïj¹
fëÄ°gyÎ
jgÂ~ê©\x0003çr\x0010¤{f+\x001d,<Èå:½KTl\x0007\x0017,;³7]B6O\x0010YD@ZG9s ïùAê8\x0017LÄÔ\x0006K\x0004\x001d¬x{)DÍ\x000fRÎPg3PgsÚò»	µÀ©¥\x0015ßYq®Ë£lÕ\x0013ØvÄÖo~\x0006oáíE»Ð«Df	y·Dì \x0006\x001bÝ~ª±©÷P;i\x0002s4¨\x001b$ç\x001f<\x0011ÀövÀ®ý+µØÉs¦PÎ\x0003oÚÉq§äÂ$\x0000­Á\x000e72$ñÅ¦~Cí¤\x0010àÉÈ\x001d´ÝºÝoW\x0007T©£Þï3u\x0000ÚÔJmd²ÓäM³¦ÆñÔØ¦5ËClüGÎ1|A[ybrº¸º8=5:ÙM3Ób½"Uft¾P0ïcõ6côîª1ß¯Y´ÙÑâÊ½l5îS½\x0008Û©W£©ª\x0017M¢)R}[\x000bNÇÀQäÍ¤»\x0006;³Ô³\x0007çËB\x0005ÞD¢YÞ®; Ã¸\x001c~9"vâoÄÎ"&\x0011I\x0018¸aÏUØ0b«]?S(,Ù.½ÉHu\x0007#Ù¶½\x0014ø*°£\x0019Ü\x0011ú©Æv+\x0010J¢Ô\x0019Æ¢ æÃÃ²\x0013Ø0b_mgY\x0003\x0003­ÜÈ\x001d2\x00042ø:¿î~ðçw·7wj·5e~é*Õrê÷:'ËÜAÒ]\x0012úÚ\x0007\x000cüºÎT\x0010­¨$(§5sþævÎßèçÜö9§,\x0015¾ºËË\x0017NÿJ'püäY§?ig\x001dï¿|®t_°w>tibýó\x000f\x000fþ[\x001dQCCgMÀ\x0004¢.	\x0012$N³g\x001a¥±<ß\x001aË³ÚX¨ïccé\x0019ô9G×ç{eèa'\x0001Íäoõ\x0011*ËuÕt¸KPe¹ìÀ½\x001cWPµî§Pªôà¥|H/^ÿÓ\x001cv\x0016 éë\x0014\x0013ÈtEz4m¢¼x©x\x0004ý)þ~ñú/?}\x0008mã\x001eÚF=55wným§éHÜLí\x001fÞÐSo¹MuªÚô¹ud[Ñ[6nÙ<ï2Më<\x001býDÓ.byPJdË Ã3sÜ¡Ì\x0007«°Ë]ôØ\x0013
)cr\x000b§èn»0Ò`oo\x0015Ûe=6ø¶ v\x0012E´Ø5óHXwÝlû0`ûpa¶½´ØÁu£p¶åVÒ$QD\x001dF#	\x0017\x00047ÀØÁT\x000f°3§\x0012\x001e>:\x001dÇÎãlç\x000b³]´Kô^^¬£Kâ{\x0017\x001e]ÐcÃ
zl×\x001b1\x0012¸r\x0019=*	>\x0014÷ðaò8v±\x0003v±zlçÚc;b÷ªöèMÄO\x000f\x0015Ø;Ù<Â®²yZl\x001fÚ½f¹£wvkù¾l#qn°\x0011ç.Ø\x0008Þ\x000e\;Ö½\x000eK\x001dÅFìÃÛð	ì8bë\x000fI¿õÎôs£\x0017ùM¤eÛ\x001fiÝì©}º0Ù½á£~Dl#V\x0018@~èh\x001fÇ\x000e£e\x000bB+ï#\x001b	2Ù±÷-xøä~\x001c:\x001d/\x0018vÎ½G1Ü4zLP&e\\x001aê<Nu¾0Õ\x0010d9Ròªej\x00082×3=4
6\x000c^¶\x0003½M5\x0004±Q£?ÙB¼]C¤Tª¨ÇÉ\x0006ýd\x0007ã¤Q
pp'\x001e±P/;\x001dÝö
R¡ÇWsÐÎÊTçÀ§LD\x0012\x001c)ýxuô\x0017îø[¤fÚ´Æ!\x0008ÝÍ\x0003Ö¹OÞ¦Z¿[\x0007Ü­c»ÕÈN[!ÈE\x000c(@²
Û\x000fVM?ÕØ¡ÔÊ®j!ÝÇ\x000eI^R!/mïFì\x000bv\x001dù¹f[ÚFÅ \x0012y	Òº#Ý\x00171á"\x0016Bli;- 8Ûn;Ò×Ív\x001aÃ"I¿al¥ëµî	Ø¶øØ1º\x000c;K2_XxÎ8Æ\x000e3`"\x0005G\x0018{ÝõÑÃ\x0018î\x0003}À/R"ë6Ù©}êÔ\x0013\x0001_
v\x0019wí¢ßµ£þGÝz\x0012v\x0012¿\x000fÂº\x0015\x0019\x000cì±ÃøPv\x0012»\x0010¶OO<ÙQ®\x0006\x0010ÖÝÃB\x0018öú¬¥\x000e©[¶nÙE®à'
4ØiXÀÊYl/ç]\x001bç\x001dZÔ/õ[/¸\x0007â;g°Ç\x0010C¸\x0010b¹¥WìT+?*6k&àl¯2vÑv¢ú\6\x0012Óo\x0007Ib`\x001fªk\x001e¦£C\x0012/8$ò¹\§æ³&\x001bï;öÂÉ\x001eºZOÀçèï_ç8Á6AßC
Ë¼@¢ß=¥
ýøzÞ@w\x0006ÑxØÎ7§Êu»
ÂÿçOÏ¿2ûüWµÑ\x001e4\x0001[»²Ó\x0018z1ÞyÖ¹áàe\x000ctö_\x001bC´ÍÇâ«fK¸ÃCI²× ¬\x000büÐ\x0018n\x0006pÁ"~\x0001éZ\x0019YÈ.R\x0017Wÿ¾Ì)öÜ4q¶7ÖL´Mêü«ïßÿøüí\x000fK\x000f}«#Iü&\x0018AÕ¬\x0014îôØüê×_¼üè³{¥pLYöEAI\x001d\x001dZo\x000emÚ\x0013­\x0018îôÒ<iÝ\x001eÓ:Íl\x0016ÑÈ\x0001¶ÙL"9\x0015ït\x001d;Î\x0007Î¬ûê?:ðw+éÅé\ðÑÝ`NcèØq\x0015!ÉÙG)¹\x0012\x0005=¼\x0011Ì\x0015½sÂÀ	\x001aNûd3re.¢¶Ó9×M?Î9,"§YE\x0016D16ã)
kÁØÕÑÝéhps£\x0013§´è8ËÉ½û2\x0015\x0017sÛYÈ2öN³ÐãÃ|\x0006Õ|nôt(y@¹ÏçäQù\x0014g\x001cV{Ô¬vã9_	9%¡Eý\x0011r\x0012¹8\x0005­3)¶N[b°´Ét\x0007+ç2Å\x00013j0»ê\x0016ìr)@"°\x0014gwS[
\x0014qf£à\x0004#Ê\x0018$*	\x001e:çF\x00149a°MPØ¦$")ÙØ^Æ\x0017Dr4ÚIAÜ)Îö%)8Ñ\x0003\x0001\x0016fÌ8\\x0002\x0007²ÖÃÆG1wIQYä÷ÎÏgK"N\Qì)í¾»h\x0005\x0002õ£\x0007â5\x001f>\x0019Yï4¡­é\x0013º`_²aøðõmþ4¨3¢\x0018HJº&gÑñ\x0014ÒâLÃ§ç9©\x0008Oh4àS°2¡µÆeÐÑDU[¨-OÌ\x0019rÍ\x0013ªóÙÕoÓ$â\x0014'\x000c^]Mo8ËY\x0015øÃûÞ-"Yb\x000bî\x001cèê\x000c^ÕpÆÌL\x0011·.fNêÅ»Ñ¶A·ò
\x0002\x0014ÏuQ\x001e]Â+RÊV\x0005õ÷Ú\x0004\x001f\x0005õapE|Pø"¤èFï¹-\x000fE6Qî´ô<\x000c::v^áÙR,+jâê1q¨wpÕ\x0019ÎFG9÷M¡þMrÓ¢Óäü½î1óðÝéçyÌ\x0010å"¶ÈÑy;¨´zðz¸S 0l¡ôS3<©×yÙèÝ½FWG)wXõÚaÎoL¦x+ÂE5W¸ùL=Í\x0005}æI
ü)P;Ü7£=áDÐ$\x00179\x001f8õAzXâ\x0015iÁÆ\x0014ÇHTDD*hkÿ Q¼ú O\x0003\x0008:©ß8\x0005\x001a\x0007g$ÆóÎ)\x0016W\x0012lSZH\x000bÝ\x001fÚ@í­>ÆñÓGÍ§§ç
^L^ÒÞ¼Þ­\x0008\x0016Äbt#¨foúÌ(\x000c§<ý<\x000f×âÌ=Þ<3\x001c|]Â,ÃD?Oc\x0002U\x0015±Rr²\x0012´ÛV½ é&.¢\x0008\x0018ô¤%\x0000¥\x0015pK\x0000Wº¢3\7Ð\x0004ÃJ¢
ÎÄý\x0017Á¹\[\x00197Î®¬·àË'H#èù\x000b\x0001tæ\x0013\x000b8».ÓäÐÇ\x0017Ð\x00057Ï\x0004e\x0004Õ(\x001dK<£fÑ$7%ï4²>
íàd«pGÀö\x0019µ\x0014\x001cá\x001e,¾Ë\x001fÇ;]Ox$[Á¯ø$o\x0014>­¼úxA¶Tº,>Þ@#.ô­ \Vþ»óóMÍla±Jn!äñß"{Ô¤\x0018ü,ë×·¬_g¥2<ÖÊN®õÔ³YgïþgYoY¿¬ooYßþ~YßÜ²_[ ùG_¯ÐUº\x0004QÉ>ðöv\x001f8?¯ÿ°}à¯·óú×ßï¼~};¯ç÷È¼\x0012ëó-ëù}à\x001ff\x0003ßÜÚÀ7*\x001b\x0010÷*ööÖÞ@oP\x0003KüÕ?ÿåõ/
Ö"^b¨\x0012|õØê½tÜ¥¤\x0012\x0017rM*ÙÔèAnè¸õþç¿ÿïw?\x001es]RS$+\x0006§R)¾ç\x001açô@\x0002éË\x0017\x001f¾~õ¿^}ñ×=¯3Z`cÛãx¡Ï%êÞJ\x0001bhïiàíÒJÀÑ)©Itd^é>â`Ã5pó0¿Y;¿9µDQâõNZ§º9Ó?;¿Æ víÁ\x0008¸¶\x0007Ó\x0011G#9ÅÆöÖ|AjÄ³l\x000c§w=\x001b	ø¦gã	`'í\x000fK¡¢½¶?8$Æ\x0015·hwÄ\x0004\x001c­\x0016ØË[%\x0002\x0007iµìºbu*[Ó\x001e$N#±v[ËÆ?eâ\x001cEèÅ¨K¤ü¸¡õAâ2\x0012\x00175q\x0014\x0005¦ÇG+ú@b\x0011ÕI«6bÆ9Nê9¶VôÜ
z\x000f\x0012`KàLç\x0004\x000fG\x000e\x0013Ã¸Sz§@«0L³ÈoZ)àÄÃnÍ\x0014;ssÖiq·}jÒs%äA¼AÅR|Üuô\x0018°\x001f¬ø¶óö	ààëË;\x0011Û,O\x001eÖH\x0002yz$Mx8\x000eñPù}Ø&¾[Pë@¹[ k!;Å¬½ËiâqÝ9õº£nÊ­+_\x0001(UùCß)Ìã¿ÇËh\x0015Ek\x0015±·ÜFbÃå3\x001eÝ\x000bãX\x0016ù\x0014~t2½ÚË\x001fl\x000bd/\x0007±+g-RÏóÂÈ\x000bZÞÞ"\x001aÛ±×\x001fòáß×x~t)¼Ú¥ÉHß\x000eH\x0012F`\x000eíQzÑ"â4NqRO±+\x0014§]y\x0006,zf)¦\x0007ÂabPOq0\x001d8ÚeHÄ)M¤Eñ^³öª\x0014ZHa©DwxÈ6A\x0012"+Ã¸M\x0004õ6A%ÿ¬B\x000eÎs\x0012C¿»\x0018&9gçãH\x001cµÄà9·¼\x0000{õDÜgøAõùqÞ<òf-o1}c£úâÂ¼¢ª\x001fWÝC\x001aØ'9:¬t\x0006C\x0000±\x0008w¿xñ0/\x0016\x0001j°3\x0000
*ÚUÉåÒÍ¢³#îDP»\x0013$iÒrKFóhÀ`ú6a\x0017\x0001£\x001b¼SMe¿øYé´á\x000eÌ}\x000bZe­(\x0011$ÿ@×øÄei¦ë\x0016\x001a/û¬NwÒÀÞ|Þ®¤Ë.x;-cf~£e\x0006\x0016Õ-è¹\x0005&`\x0010^¨ÖL3ÙÆ[ÛÐ"G¨êÄ{²eh×/MþLÅcèènjÒð\x000fµ&­xþíÅÞý`ÇnyI\¶R?Wy[»vÛ¼Wâùù?½ú\x0012ÿþ8\x000fÄYM,úÖ@2HBl¥í¡
ä\x0012\x000e\x0013ïtÔ\«ÿÒ\x0011û¸¥\x0011\x0019N#2¦§½<¨¡=»Óÿ@¤Aþã\x001c®¯g\x001dáº¾U\x0018#5kvu\x001aØî?\x001c\x0015Ú$¼·}G®Ý9¡ìÁI}\x001c9
s\\x0006tÈ¦\x0017ú\x00129ßÙ\x000clÅ.>\x0008`\x001dG.a@.A\x001cShì\x0000$}\x001b±8ÈÑ?êÎxb£\x0018ªØÛf1\x0014±3g)\x0010¦\x0017<N3Fö7÷H&ü1¶kØ[®)1ÅA¡éÃo~þ?ßýü÷C.Q4ò:Zõ4¯3GîPF«\x001fif|øÇ\x001fß{ud^;ðZ-oØZ\x0014# a§3di\x0003\x001dò#c¼»®+È46]9ÃLEkí\x0013CÌ»lM\x0003lRÃ\x0016)Aß×\ÆfÜ4É?»¥ø\x0011\x0012\x0014-.«ÎÕ®ëR	¼\>\x001eJkxËÀ[Ô¼Ä
Ásdårw§Îû y×Á\x001cj!¨\x000e\x0018XÔ\x001eK»þ×\x000bSàðPë\x0018ð¦îWGu¿\x0013ÀÔå.hÁµ\x0006G®ø¾;,±\x0007çùuN;¿Ñç§f\x000fÔá=@îÙé¡¦Õ1Þñ¬pêÃ´Ã¼íyµ­;µC#¼Zx\x0010\x0018<
\x0007{ Jàè·eÃq ÑmÊ\x0001$)|\x0008ØÛ\x0001~*)ÓsÖ)-\"VýÃ\x000c\x0007a\x0004\x0006-0õbm¼àz4Þõâ8)\x00068Ë\x001bÆ	\x000eê	Î\x001bhãí(±Â>î\x0010IR¬òÃNKÇó8ÁY=Á`^\x001f\x0002,Q¶â%ÑÙ5rÁA\x000b õÐbì¹×Áþz`$ùÞ5k\x000eË\x0001¸dõ®F[s\x0001/\x001dY6	¤\x0018t	o\x001c\Ô/9ÚÔ\x001anL\][b`ûP¹û\x0018o\x001c\ê%G\x0012DmÉE
ló1\x0007ìEDÿ(\x001ax\x00148Ç\x00018G-°Ë"YAmªZ¶ë§Ô
Å-Ã
#\x0016í\x0015\x001aÂ¶¤Ñ\x0018D`ÃÑ\3nY³\x0005Ç2ÚoQÛ¯óõ*DÀYÄÑíÉlÀáqóÌCÀ)\x000f;ZÊê\x001dÍ\x0015	Q%Ã»\x00032Y\x0008\x000fÛ!\x001e¢Ín ¥z'Í±ªA;r!D&â±FþAà4\x0002«½à÷
1\x001c(nS­zØÏî\x0018°\x001f½\x001e8rÓZ <+'±)/Ò;f\x000fã\x0008\x001cÕÀÉË	ð$G-"NdÖÎò¦ÑÞÈ}ñÞºE\x0004á}Ø\x0002î p\x001cÕ'FâdMxMÜv/ÅÐ¸	/ñ!r\x001e|\x001eú©\x0005]½Ò\x0016®Þ&¯²ËW5&Ë\x0008¬\x0010pW9Ío\x0017785wå\»2ýÔ\x0002\x0017îØÀ¦ÜC7°Ä"À\x000c&\x000cFmÂ9vÃì¹Ñ+1&_Y\x0013X0L0ýÔ\x0002;nÉ	Ù\x0017Î\x0018uEpÓÃ~çÇpÇ80¨\x0003Át\x0013\x0003¦ÅÇ9U¢8³ÆGÃKË\x0018YõjÚ$´à"kb¹98¦nìIà2z=EïõÌ"À
¯ð¦É¡U´%ÛYñ#®×ã¦§¶9PyÐr"
iN/¡á´ :ÚDÍMÛì\x0016cêª«¯Z7ßü°1×\x0003Þ$-?Øþð\x0001þgþáçï\x0010õ³Éuæ \x001c\x000bWLA\x0012Ê~ß\x001f>{ù1\x0012~öå\x0001>¿çó§ù(º\x0000Ï3`4rè¦Iyß\x0019Ä´GL§\x0011¡?\x0007æè9Ë\x000fç°k\x001b'M-N nº	õ+Çó¡û.Éò\x000cò
ã¬ô\x0019F\x0018\x0018á<c·\x0016\x0004ó´Ê<^6Æ-Á\x0010)Áåü4X0Þ\x000f¸,S¦qsÑ\x000fþ4£§ÆiíâéülT\x0010ÉyÒ\ï\x0004ãæ\x0010#¹#g\x0019\®hUó§.¦\x000bÆÉ£È\x0019ÆaÉÓKÆS«\x001aùÖ¥nBÄè\ÿÖ\x001cô\x0013qøÖñü·fAuv@ù)ADÏb\x0008Ú`ÌÃîOo\x001e}\x000bÎ_Ëè~¶þ\x001eÝ¢>×¿5\x000có\x0008çç1º§ÀöT0\x0016yàùú²ÞÞï+b9÷{Þ\x001d3H9]É"Ï\x0012'­°O á¨.§Ïjz'B\x0002¢¼\x0018qÏ¼È¸{õ®\x000c½z\x000cT\x0018\x00182sÊ8þ±_*`%u\x00022'a8}\x0014`¸h\x0019À¸Vþ\x0012¶Ýq\x0012g8A\x0018Çiç§?³_FÙq\x0018{0dR´u1§WuðF>5Àµ{TçÙïTß\x0013iÈ¤ÈÒ5Þñ>ÖtjC\x0015sã¼ºõìz­WFÚ(N.ìe{\x00046Ëö(Á[J¾
	Ã1C?ÏNd4"î\x000eÖ´û!©®ÈþX.¯\x001a7ÞeèçiÆ®\x000cÎðº¶FÄàÒLQó\x000c#ç÷\x001e¼q\x0005Þ{læóÉåcÏDÝO@Úq"íùÌF"oàÚ\x0016n\x001cÉNrØÎ\x0010Óxþ6\x0013r\x0017\x001aÀ½²½ØÑ}\x001b\x0004ò×ïÿ'\x0018ý8þü,RÄ?µT\x001fÚØïInÒ_â\x0004d\x00186Húy\x0016²è\x001cOd
ÒFÓ'ròv\x00022
A\x0014úy\x001a2I"Àa
×¢ä&¡ö3ãL?j(/Ø\x0010]KU
¶?z§Z`|q<jÜù£\x001eºKfÆÌÏXôºÝ!'\x000f' a\7pzÝDªãmäCØ$%\x0012\x0019/¤\x001có\x0008ççÑ;I $RS\x0001¬$ÁèIôü\x000cä¸GÂé=2úÐwñ$MÞ\x00112uÈIÚÈ	È2®r~ÕàÎÈ¡3Àûk»x\x0005gE\x0001=ÅI®Ó\x0019È8B\x000eVPº\x0005'm\x0002Ý\x000e\x0013Ï¤éÚè3ãç.ç?w°õá¿Bt\gRøÿqÕEóf¸fÓÏÓ;KØ\x0007@\x0008eóI\x0013£cáÏ;\x00161ôGR(¦\x0015]\x0006ç¤CLJÃ{Þ\x000fá=úy1Y¹¿Bwä\x001d¼#\Þ"½·#äé3.9ñ½\x0015o´ñû×¤CÝ	Èñ\x000eëÏßa)
Ãñ\x000cäDÀÚ"!ËåCÛä´U×rïÍé`iaå\x001a\x0018@¤\x000fÛûÂå\x0008\x001ab¾»Á|w\x001a3K'a¶â\x000cÄtý5É^\x0006³¯ãø8ýå$ªÍ½ß_²ýÎmÅ:W<|á>ßÌèóïóÃÿõ\x0006ó¯§\x0003å¦wÍ¤î <Të-\x000f7\x000b(ÿrCùÓ	,\x0001P)åYÄûm2¯_uÜ­yÒMâ¼}F[@.\x0013\x001bãm¢ûn~¢)tj÷¼e¥\x001dTÁ
ï ­á6í ôØ\x001eâÍe\x000bEÿü\x0017.»\x0002\x0014/¸üvGBM­X\x0008/\x0016Ò2\x0015Ï´·¬hTýÉô"ÿ\x00175n>\D)ý\x000bVÔ×7+êëÓ+*qw}¯å\x0017	ßßB\x0017<{#åÛ\x001bÊ·§)cÛI®¦Ô§ÆþBv9VDßÜP~sz\x000fµÛhà|!Ì´=~ë7Qt»j*Æ.û\x0006>\x0018U¾yþñÝûç\x001f¾>Â
½ÉR¡2×I\x0018a\x0011Õ\x0008³+;?¾üâÕëýëCèà÷ÐÁë©cä·BòÅ©½¸ÍðXkð8t\x0018 \x001e\x001a}*VH4x\x0010´êò\x0010\x001c\x0004@ó³z_!ö\x0001zêâkÙ\x0007Q;q¯\x0002ÞKØs<ih¨Ë` Eo U´ù¯\x0005¢Ü s\x000cÎü(gú\x0004µÝ×*À\x0007Ö%=¶\x0005VéÂÉxJm®³\x0015\x0005<kn©¡\x000eÔ·Wõd[Iö)Ð\x000fã\x001cºø\x0007Ug°÷Õ»\x001e\x001b/Ü®ù\x0010Uà¨EPeN\x000b
d§\x0014LÌ7JÁ§c×Z)x´pÔ\x0017ÏBvÏ³{,<w\x0014ÛÁ®¹`×åÐ¨ç\x0012ttHe\x0012@ÐPûÚ_ ¦®âÝ@*3ô¦~	\x001e¤¬aNÃZtI½\x0016¡ÞY\x001cã§\x0016Âîµ\x0017)>V0=qo\x0006>ÑßétûTxïCË.|¤k\x0007öAIÃIî¯o¸¿¾ÂÝJ¨\x000bÉxÏÜ\x0002J¨O¿½\x0001«\x0007çÊÎÊÍOÉÉ½\x0004ì\x0003ùÜÏ7ÜÏjîÀª\x000buÚà÷DRÛÌ\x001d\x001fÊÿá~sÃýæ
7tn#ÜRê	5·è*w\x000cíêÚ\x000f\x001cüÃ\x0007[~úüþýOX«ðø×ì\x001e¨.ï\x0004ç\x0007ê\x0014óéË×¯¿|L¸u­ B\x0017~y Ìç	]Íö"B:þ8´¸M\x0004?Ñ·9ÁèïìÏgÕà+	ºÉ±mºâù1L7O0´g\x000cé<cæøY1ÅõÀ>Hr\x001aäÃ\x0019F\x0018\x0018á4c¦]¬È"\x0006W¤¤\x0014â$Ïæ\x0004b{Ä\x0018ÏOca¾Ì%¤8r\x001dYxç\x0004`\x001a¾s:ý±üÆ ¶è¤hCºniXÓéü. ¶h©²Õ2£b\x0004vN æacÌ§7Æd]Mà$DçäVã{Î\x0017äp\x0011O
ç?µ|óBÆÄJZº#	ãäiö\x000cãð©áô§NÖËöm}äUdîãU¤á"c\x0019¶ïrzûNN²1ðcMð^rH´ã"£Ýó+!ýÑO@ú ­Llbíã@B¦±P\x0003º~Ø\x001béçéØ7³Aªð[gÙ\x001eË¤¬á\x000cc\x001e\x0019Ï\x001b¤|\x000b,Ý íÌ¹Sûã WÚöHúb+w¼¾=\x001eÑV.nÅäÉãÔ'¿%¥Ï®@ýÍ¿<Mêï~¸TúËÙIurA¦M3ð÷7Ð7Íëß¿ÛY-F3©.>\x0001AÁÔRº/Lô\x000fAM\x001eK(©Ù\x0014=ö¾ü¯wø/{ñ§ç\x001fÞ¾{ÿâåw?~óýwß~ÿ¿\x000f½×D¨÷1ÚÓT\x0016øä8
~mþò«W\x001f#ó^~öá«×/^~üÅ\x001f?ùø£Oþ×CúÝjr\x0015<¿BÎÑVÛé¡k\x0008M.òZz\x001föôøëjîwn*Òz>àF'Z2!ô\x001a)i\x0018ÃL\x0011]K\x0007ú|>I^W
"\x0019\x001bjÚ/ÓOäµô;\x000céÉ'»DßËXRtâüÔ	¦»+é­qÃCYEWðáxêÊ¤â+:e³Zx-ý.T@ô\x0014+¸B\x001f¼HxP\x000fÂå\x000fq¢R¥Åá×\x0016Wð³8÷\x000f,î\x001c¬Z²&J¨J|·É\x0012Ô\x001dt	.àÇ\x0000Ò}>A~â\x001cæÞ6"À$Ü ¥\x000fÃiK?/Ñ''uÎ)C\x000fèPbjÃ¯RY\x000bñóp`ÕZ+øÈÌ©xÆ>\x0019Î+AlgV\x0017«Å/éÓÏ+øt¯åñT¼Wø\x0000\x001f&ïJz?î;þâ¾¼ô0ÏÖIðßoIfí®¹\x0013Ú­ôùå§Rø*\x000c\x0019ýbÞ5i7\x0015é¹I(S\x001füpdÑÏ+øÙIXâ¤&ò-%C,LÞpµì0\x0018\x000eý¼Ä\x001e}\x0017.(Nê>¾Ü¯Ýñ\x0003\x0011ÿÚ¦CÙn\x000b©L$RQ]IHOÉ\x001eí0õôó\x001a{y*«Émm½§Åâ:ÉÑº\x0011ÿ¢Õç´UæzÕ"|+(%`%¾\x001bñÝuü\x001c{Á%WD+O<ÉNJÇ´ø~8®èç%|È¢e¸üJ\x001d}è·kÙóÈ~íB\x000fRµç8©6ÄÎ×õ¥78Þ\x000eãÅë!à	ëEÌÀÔtkÂO\x0012\x001bKaÒ\x001cP?::ñ¢£\x0003\x0006zA	t\x0014{d¡J6¯£Onp\x0015èç%z*ïÜ#'®Bà^&*µZüÛ¸ÈÅÉ÷[5V2òÂ#\x0004nÒ ^Ëó~^câ¥\x0015*¶åÌ\x0018#©HÙM2¿´ø0Z\x000e\´\x001coëðKîSä¸Íqí®ÍO?ÿy<|»OóhQk{~Ýu8
Z\x0012Í~\x000e\x0012úöK\x0003#Ö\x001fùáZ4øcOdpB/Ça"¥¤·v\x000cëÐïkÎNaQØ\x0012×^\x0014&iE/å\x001f#ùõ÷?ÍìSTjK'¸ÔÛK±\x0011\x0007-\x0005\x0001ÿãj¥÷3És>¢¼%èqLùÍ¥ç\x0008\x000epPÙ²È= ¿¾Àóí\x0017x¾ö\x0005\x0014½StÊË\x0017p=:5É¢¹ð\x0005o¾À¥\x0001ø\x0012¤²¯v§/ ¥=a&vá\x0013¼¹ý\x0004l¨*Øþ	²|-@è\x0016mBÙÇ±¬jq\x0002gh|ýîÅûç\x0017_üôíûoþ\x001f\x000eJ'\x001aVÝÊxU\x0017ÞbÙé\x000cy¦tM/·ÿúêÅë/¾øò£×\x001f½úìN\x0001\x001bCo)ï\x0004@\x000f\x001c[<B\x001b\x000e/P©z\x0010èIÆûyh»éá\x0013tÍ\ÑRgÏiZ¹ØM\x0002\x0012m©Ë¤]£ÚÚ\x0006=5HÝ].{xâÉqÀËú<¥õ,ô8ÕöÊT\x0017.\x001aÅ©ö\["W´ãLßI:	½Å>*´Ojè`¤W_..J¯ß\x0002
\x0019ÀLÒÅ\x0015Ôãþa¯l $ÏöAÂY=\x00008A2xï
ê­\x0010¬R[­k
35nØE$:ÅB NÚ°+¨·FxâýZjª2f\x000b¡\x001aòþÍýtÑY\µW»-,FÐNr×4Ð­;\x0005\x001eø/cÝPÛS5èÙÛ\x0002z\x000b
TèlôÐÐ\x001a÷\x00115½Ú{VÌdÂ@=BQS/L5à\x001c·6~{¢/Aæº¬2jaÖ\x001fæÑô¼\x0002\x0013¬\x0018µu^º\x0018\x0003~z×V¨k[U-µôµ¦êLv÷\x0010»;ù­'Ý`ÒôSMìÛ\x001b\x0018Aç 
ÉI+ãYdZ\x0001\x001dGèx\x0001:&Q\x0013´t<æQô#à?¬2i\x000f#5\ N^º^ÔÚ\x000bÎ\x0017à\x0001½§eS=\x001e.þÂáBºd¥­C*tð"8èÙ=Å\x0013ç×oa\x001aêq\x001dÂuX ÷@§ª!®Ã!qÄF\x001d&E¤\x001aê0Rëj¢.l x\x0001\x000b¢»#ñfºá-¢\x000ev0ë`/5\x0014)4F\x000fïI\x0014\x0000ÅªËDCÁìÓ~jSwª©Jï·8Ó"5uÕé\x0012Â`ÕôSMm¡>ø\x00135:zü"u(Ul{\x0011s\x001aôÎ\x0007¥Õ§æ2Yò¸>z
6j?é·¡ .ãL\x000b3\x0017\x0001YuÖõ\x0014ûÞ,ÔÄ;µS§çz\x000b;Él¿ÑO·ï·]é\x0016½tãî\x0014+¾ïk\x0004är.E\x0002ª Bæj0¼êzn\x0007çKÚ®ºËÎ\x001aõçÛYÖÏz\x0014I?\x000b]ÖÂevWMÝ«àè\x001eá2ò\x0017ö\x0002\x0011ï^|öî¿~z0ª ÍK
¾2Ö~\x0019,vùQç½Ï^}õåëÇ¼0ð×g#Ex	OI~
4M#\x0005ó@èé(/58ßñÒO\x001d0)¼µÊÆìvr+Àî\x001aÄaà]£3\x0002¶Q	\x000c·µ+\x00197\x0011NòÀ+dàYÓÀn\x0004vZàhx«£ÎHÒñErjR-Æ]ÂëG^¯å
EÐõ
ç_¥0Ëa:
¼\x0005Ä*ð^\x0019éì\x0004\x000bpÎ¢Ù^õ¢\x001apä»\x001d\x0007\x000e­Úl \x000eTiÖ_N\x0011÷\x000fï¾ûùþë`ãC+ý#²o\x001d´H`1tÅÒp¿\x0006\x0007yÿðêãW_=æÝ\x001e«w÷T}\x0012\Oî\x0008ä3?zð±7ïøF§·x\x0001\x0001;£\x0006½	÷õ½\x0002p]ô÷\x0013bN\x0000\x00018¨M\x0002¯Ü<Ã¸©É\x000c\x0007yÅöþ\x001bâqà-2JÀ»|ÁÀÙ÷V\x0002À\x001d\x001d·&Qö~ïqàíZBÀÁ©g8=±þ®"\x000f
AJ£ÈCç\x0017Ô\x0013¼=s NpoRoî\x0017I\x001e\x0007	Gµ	Óû t©·\x001b°d\x001dYµ÷yàa\x0017êm\x0018i\x000b¯¹$\x001a(xyºxp\x001c8
k.©×\±½~\x0010Ù¡];(Þ%Ïô÷+O\x0003ça\x001bÎêm8Kf\¢Ð>ïÂ)öÜû¹MÇyaXs ^sPDJ<¥ÀR\x000f[`\x000e,b
­W[\x0004n½³èöR\x0002n/L»2|\x0018Ø\x0001~êÑÙåû\­cL\Lqº_PtØÚtÄ\x0005¯ô½æØséùIi§7÷=&\x000eØB/vÀWf_l¯V\x000c+óiâ4\x0012'5±/\x0012Å¥ô,\x001eßÍØÞ¯·9AGbíVì}ïö\x0017InX\x0004³¥ßM0\x000e;ªuÙ\x0013z©\x000fnÛcü$ìK\x0014w4UÄã\x001czËÉ\x001cKí¡/AÎç`&I\x000e§ËH\ôÄðÔv\x0008Ë\x0011¸ô)^³S8?lmôSÉ>&·ÔèãY:ÐølïVZ\x001d'\x001ex§÷â)C´];¨\x0005,G^Ñ¢y§À{Ô¢9\x000e~$V\x001fx\x0014Ýnn15É\x0002Î@\x0003~á>MÞÊÎ\x0013ß\EõwÑ Ï¿!;IO\x0004/IÝÞÜOÈ=AFbm|\x0002}ÊêûÐ\x001cÛvZÓ\x001c\x0017¹=ãù²æÄsãåÎ©owõ\x0005÷6ÛÂmX<Mÿ@Dæ8q\x001c#*QëË£W)¯§Ê8Q®ô
ì8»[TïnÐ\x0015õ£·ýÞãýjÀ\x0013Äãî\x0016µ»\x001b\x0011\x0007±
éjÄY¦ø~.ÿ	à<\x0002«\x000f<¼X1-T,\x0017R´â5~KÃ~jYÒxgÄªß\x0017ñæqgËÚj9/§L°lln+¿kZA{Ü¡S&\x0007t4Yz#£\x0005B<Ñ9>O<nÅêK?½0ò\x0001\x001dÐÍ4ò\x0000\x0016Úc¯ öfØØè§ØYi[\x001apW¶ß\x0018»i\x0017ã½\x001d\x001dýT\x0012{ÏovT\x0011&É\x0015&\x0006qÛÊ¢[¿wUx§¶
J7l;[ \x001e}üî\x001c¥¶ûüÇý8Ç^=Ç!Jð#Ïq\x0012	C\x0007®K~t¼Ú	
\x001dÉvì³$¯\x0018Ý\x0018ùE+/+/©W^Ú¸\x0014¸¤~ýX\x0004\x000c#0¨Áð«GpåÉpþ©®..
qûq7öúÝ8\x001biq\x0013\¬\x00028uå\x0006«5nf°ã;U\x0013\x0017Ñõ'^à9vò8êü}m³ÃÄqôÚ¢Úk£DHß½\x000f"v*;UæÍ#oÖòR\x0014{èyÓ»5áÁ3lý$	ò4ñ\x0018\x0008ê@PÂÍÁ6\x001emø¼óV\x001eïìýzÊÃÀÉ/KV
\x001c´ü¤\x0010\x0018ô<B;éNz\x001ax|àOê\x0017þD-4c7Dñä}Ï50ì=Mì}~j§¸\x0015\x0000Tâ.\x000cä{Û\x001dSÖll)\x000e\x0011cú©b/=Ý]¶"Mà{\x001e¯5nüiÜØzcK\x001bíP\x000fHÉnôÉI
oYtÚ¥ñ\x0005:© 3^ï</;\x0012ç\x000e\x0012Å
ñ\x0003·ÃÄy|ªÉê§\x001c\x0003÷_\x0001K¯¥,ª'ï\x001eÆ5]\x001e/¤Y}!Í%ËñLµ
®¤UÏû÷k»\(\x0010ýÔ\x0012{qäñ«¢DU}.HÑ\x0010ÜW\x001b=L\x000cvcú©$ÎQÞlîs\x001c@:Ïá¿yÍf\x000c0Ä¸\x0001´1nðÐ«åô¥PÛÜrÝÍ¤.ü,qñÃW¼öÀ\x0003Üy« \x0006²-¥4ÄWÍ1\x0015§í£öÀÒÅäõ´&b\x0014¡.ºB2ÎqÑÎqñ^4+ÑÖø\x001daë\x001c\x001b M*#O\x0012Û´Áú[é\x0013g:\x001aé/
½­¼_%fw\x001aú\x0000¢%.>IA5©¹s×D\Rº¾æåÃº0¾êÒo\x0015±³6¶4¦L¢\x001c¥Ö^,Çà\x0016 ÖÚ}¡¤­Ð A\x000bqÕ=ñÉj\x0013&Å§Ëÿ-7\x0005\x0000ÔÜ\x0001Ý¸Ü!-õªZ£\x0016Vb\x0000\x000fúC\x001c\x0000w¡Ö|ìz£S3\x0014}øí?ÿýÐ,(G	I\x0019~DX?I\x000fÚ*j>üèÇ¤[r\x0010ú¨Bu\x0019j'µúüa¹c©-\x0007ÄO\x0014&OÂBÙÃÒEL\x0003\x001bÒ\x0016åN\x001c	ò`¥U\x0014Þ¦\x001fU\x001dµn¥*Z+}Ö ¤,IWè\x0018I¼¸L?NÒn©\x001fÖ[\x001d­1¬:GU\x0007ÜËÁçh{t{\x001f6ú6z\x0015­%cñÇÙüÄ\vR/q¶\x000ck~ªhCäöó@íJ84õ¤\x001a÷Xæä\x0008­3\x0003­3ZZIÑÅÛ,ú\x0004ý#N\x001e¿NÂÚa£¥*XôÚù\ÀM×ñÌ&V Â}¨u\x0008vÜ\x0011rG°xtvúRÉaZ/ñ\x001eg&îïIÚ8ÒÆß7-\x000c;B}\x000cVÑ\x001a¹ZàùúäÖIÂ¨3\x0013ì$m\x0019iö\x001f2·>\x000fÌgÝ"3yz´w[¼Ã³÷eãäë\x001cm°ÃIF?U´FêmÁeÑï$Ù®Üß\x0006VXB,Ã*£¿c»ÅvïËÙ;V¼\x001fw\x0016\Ø\x000e4iãÖÕäÂ"_áÏÿùÓó®ï `ó_äâæ §[\x0006ÓâIÌä<ú¯p+¡-Êð)WeñÍTÍ¸¼ÆFJü[UãÐ©)BÖg[[Í\x000c»ô£ùól\x001ek\x0017é¥k\x0013uûÛðâÓoßýðÃ»¿\x001d@@ËØPÐ/\x0017Q\x0015p¬3<l4ÜÏé¿í£W}öêóÄÁîÕ\x0012'àÀT)rb`\x00008MôéÏ\x0013§azÉ¯dbð2Ç\x0019øñ(¹<Q\x0015?M¼/ÓGâZ¦¯Cv\x001c*®ô-0#ÒpUÄ¡\x000cÄ¡(ñÌã*B¥I\x0008¨Ð²cøxo«8¼sà	yçÀE¦ÊìÌÈ]ë?%åiâ³\x0002¹ÈêYNI¶\x000bz\x0012å6ÆÃh2<\x0016\x0011»a· ¿{b?\x0012ûß=±-þË­]üE	×ÑÀ¶¾gàçÀùkÉß0:7Íì½Lô[å.\x0017#»÷¥
¢µ\x0004«\ø=4¹Üºúë[ê¯÷Ôh ½5¿j
¤p9\x001a¯5\x0010N{E\x0003<ï«æúÝí\¿ûÝÏµ³¤lyo~÷Ôh!ßÜZÈ7J\x000b	u?ê\x0016ÂiL)¤Ø·U'8Îõóí\?ÿ3Ìõ··sý­v®
·¾n«Q¶ë\x0018\x0016®ÆR[\x0005lúõø\x000f¨°öåû÷?ÿ\x001d¡zñ9Þg¨\x0017¬×Ï?ýí\x0019AÀSgVªYH©]e\x0014\x000bôÿ'®ÞË×¯_!þ/>ÿ¿¿|ù\x0019_·¾üü%þ«\x001e\x000eÃ
Ãp\x000bñrØNLWæ¯\x0006y$I¦¸õØ:Ò jCÑ«ð n·ÇË:·\x000c%³&5N\x0008a¤\x0015ß¢ð\x0003[ñ9I¶Cmø5fÕ[\x0017\x0011\x0006
+VF\x001c]EªZíµCmt2Yë¶\x000b£MÅ\x00156e\x0012Wâ((úÈu8\x000c?yó¾0-oQÓf®~\x000cHÜ\x000e
A­\£Q¸Â[¬Y\x000bCý(vB\x001fu³­B\x001fÿT»mÎmiôûj¦[ù«oß¿þáë\x0003à¦ØÒÁéJÒ÷Ô·¦û¸¯>zýúågÿú\x0010u{×%ÔÝ³î)TÃM\x000bÑ´¥G\x000fß÷õ\x0013ñ³¬0°Õ'ÖM­[%k[áêL}Zïê¸\x001fdµ[\x0000Xí\x0016\x00008\x0003\x000b9³:w	èç\x0016¯÷ ·\x000egï?7\x001dM#lRÁÌb5ä¡Õâ*YRm3î¿6\x001dÝÒ0+¬7ZX\x0013\x001alsd\x001ak\x0014Ör÷eÿ0ë8±^5±\x001eÆ·Kåò0f,¯8Ñ²:	åej}ÑÄ²Å\x0006xbT\x0003ZüÀæÑ\x0006²Ò\x0006\x000bÔ
uYa\x001d\x0004ÊMÇûý>ÂÂ°ÅZPí±·³Ä\x0006\x000b]\x00073\x0018Ó_:îg§\x001duf­úîµ"ìKÙiNÌ@}]4w\x001f¾ÂÚÁ\x000cU\x0001-/ÛY-O¬\x0014xáM²¬Ø¶Ü®ãKeuZV'\x0013ë$#	aåº\x001eï·>8\x000c\x001bFØ Þ·<Ãzê6XynÅQël\x001aa§\x0017´s\x0000I
¦Í ÉúZ²ÉîÂì\x0015Ö)×W\x0010iòHºpQ¶YÙt¿iØaX\x0018au\x001eWp¢é\x001cM`\x001d	ôÅØì§û£°[^mÝ%Öò¸,\x0017¨\x0016<U¹ðÌû\äLÈª¨°a\`A¹À,+÷\x0016êãÅ1(ò2[&ÙÕgaË\x0008«ºÏ@IòÄ\x0012c%*4ÂMãÌ&åÌ\x00069\x0013b~ÊE.4ý\x0001yÉÆåÑd³ÎdqçÊ<±9È\x0017ES8\x0018jî7Æ<\x000c;n\x0006Y·\x0019àÄ&b\x001fD¢%ÕÂê\x0005°eÙ¢Ùb¤n%ömÖÉz·dõfpcè§
6³òfI\x0006º\x001f#ïS~Éå:ç\x000c¨Ê\x000b
pî\x001cÎëv" ¡Ê¼Þou\x0014Ö\x000eFà­Ò\x0008BíJój³4C
.\x0011û-\Â!`à*`@3k\x00196úbYgÖõ%÷Z\x001fÜ\x0008«sfmT(\x00153\x0008^R\x0005ÒýzaÃ\x0008«;\x0011ðÛïg7®\x0010zÀ
'ÆÇ5ªY\x0003wÚ;"«¼Dæ´Äbóh±Yg±Ö?ÉK­ÅÒ\x0015Õ
ÌjºÏ²æ5ëX%5\x0012a\x00137&ÄÕ%Ñ
_ò\x0012#(£\x0011\x0014¥\x0011ÜÁ\x0013¾o,­TÌ{m0ÃÌÒOUt#píkÉF:\x0001á&öÖEKâF»Lõ
kÕl{\x0019ÉÁ²Ö\x0015ZAÞê¬ÄñZ\x001bt×ZtTe+ÈÎ<É®\x0015u&õy5\x000f\x0016K?Ï\x0008Â
 \x0012øôæÄ°ånBáqØÑbµ{t\x000f°EZN nAt÷\x000b0ÂÂ\x0008\x000b:Xôa¼ÌlÖè¤±#3W,¯hÇÇ$«{M2H\x000bö¤ÐvY~\x0006ö.'Yýøäu×\x0019\x0017Y®¸@ìá$\x001e\x0017ãDàã$l\x001cn\x00081ên\x0008x"p\x0008\x0019|÷âã ÞÏÖ=N:öA\x0011X\x000f§5
t\x0010mð\x0014gê
'aÓ\x0008t°.t\x001b ÎDl¯I®´q\x001b\x001bÇ`AÔ\x0005\x000bÐ·$ÌÏúrã\x0019\x0016\x001c\x0008qta¢ÒñIîß\x0000FD\x0003pm3þÝ®ØcÓ\x0018íNÊh7åÀ7®âr \x0014ñ·Öl²edÕå\x0016\x0018QbÖ"PHxFXÜ\x0010H®k\x000fët\x0017"ñÍ.6²¾ø0ÉÞo|\x0014ÖVàuV\x0010\x0003÷ú*´/\x0014Ë%Ý
V<Ï¤1Ôt¡î\x0012¸\x0004HyNY\x001cçt"aw\x0012t\x0013$e BSj²Ø®(Ò§)y·dVÇ0wR¦íÄ()\x001b%\x0004	ÃÉ=\x0006ïÞ+â/dF{Ô¤×dû\x0015B/\x000f¶rAØ\x0015\x0007W\x001a\x000f®¤<¸b\x0012»¤Þ¦'ZË^!º\+®³)§\x0011Vwë¢ÂÒaä´½\x0013/Â.Y^ep\x000bé§
ÖI\x0018Ê)ù>\x001b]Ùrá9Ø<f\x0016d]f\x0001ézq\x0011n[ýM\x0019¼À>\x0010\x00109
;Fc³6\x001akÛ1[¨²¸Fç[­l&-nÎÂ\x0011VùäUjÍ$³r .J\x0005T®2a×Yã°sÑOe¸\x0014°	ÖKR§\x000fNª\x0016²[\x0004[FXÝÃ'\x001aÛ&XYÍÝS«vµKv®~ª\x001e\x0013[q\x0013Ã\x0016\x0014ø
v³óh\x0006Yg\x0006ÉÉP\x0013¿Õ\x0017I;­Æu\x0019\x0015ÌJ?U¨¶5K$ÖÞ(Ú¾\x0015<Pç9
;¦2½\x0004ï]b\x0004Ôý'V$5ñP\âqÃèqÎãz\x001c\x0010)H`âÅL\x0004`Ìã\x0004]\x001eg-2u
¤Ä³À\x0016]b\x0004c0\x0016tÁX°MÄ\x0018a-	nðÌú \x001bÁLòó´
ìµ+Ä\x000evÚ\x0015g\x0003«á5X)õèÅ
sZ²ÓÚ\x0004[
oæTÙ·ªÍ6s÷x¼ãú-KnaÎÜUV8ñ\x000e~;Çô\x0016®cÊ0¢­P*þ\x001aCÙéknã·ÌIm\x0017ÿKyr¿ Æÿ`-q¯!¢]¹¹Eº»åègìøÍ­\x001d¿QÚ1g \x001d»"v,©]fMæ?ò>ßò>ky9I\x001d/?I*\x0015Jì¼â¿°\x0008«·a#YÅnu#÷\x001e»$ñ7&LQq%òo\x001d\x0018·PÅÒ¶f\øÖëÃoÞýû·ßÕÂâùáû\x000eU\x0015ã>Ù\x000ee<>ðÎnËÕ±²thûð¯þôÑÇµ®ø_>ûäË{EÅ8o	_DL?uÄ.\x0018qÔs­`\x0012÷\x0006NÈN\x0010Ã8Ç cK±¼ê³[c$'\x0012ÁÛñô÷<v°é(a¼SZ\x0006²æ\x000c¡\x0013Ì\x00158\x000e}ö¶ú²£Ö\\x0017©C©íäwm`ù`§®yªè\x0011OæÌN\x000fh\x0000\x0014¼Xr¬ò°wU¼\x001e\x0015:2í®ã\x0019Òú¢£µI¶ct{\x001dÒAm´ybÆgiw
Tv÷z\x0016w5Î³46÷^*«âýéaÖ<°f-kf)ãë;\x0016ÓeUóò<æã´\x001dd¥\x001dVºN´¡uØ©VË{CÄ«÷¹anA9·!p{Ìb-H>t\x001e\x001865°e-¿kX»k-@»×îFÿ;¤Ýt\x0011íN¤ëd¹\x0011ï×Rgå¦!á¥·}ñnÉ\x001asúE¥õNIË\x001d\x0010ÍåIX¥/q©»\x0017ÀqjvjATi¹µx_TîK´<FÜ¤ÄÍV
Þ\x001c¹cÜQÉ8ÁM÷\x001f*ãÂ\x000bJÜÜ¢è'\x0019wÃèáXîW7\x001c¦ÝÞÿ*íîýï\x001cm×Jç#Ëò\x0007jÊ´ù~ÑÀaÜ2â\x0016%nïÌX¨«]s\x0019Cp}[û)wÇqG[(J[(IÞÕ\èÝ©qÏí¸÷éGq÷\x000bwNVáö\x0002HG:Ü,\x0015ã9Å=Y¸³¸n]ït³çr2ê!iD,©k¸5û÷ÃåÁ{Ýí\x0001¯3R\x0017ï­\x0013<d\x0010m§p?¨~\x00187¸I+JÜÅS¤7\x0006\x0011Ô}ðny\x001cv´\x0004å}úRoÊ\x0013Omô;ãï*Ó\x001e¦
npÈÓyä9¹n	1×+%õVëOèI/±0zäAéí\x0018©yÙæ.àfÐ\x0005¤&Á¸\x0011M~ªpqÏ\x001c6¥¼¦f¸Ù$Qøuu:ü¼\x00127ö¤\x0018rí\x0012H¢{1IitXc»Éû\x0011×ëpñ
¸²Èx\x0011Æ«E\x001aÞû)nÇqã«ó\x0017jÕs¶ï9ÊÃ;:\x0014KÜ4\x0011IyFàÿãVY%PÝVso²Ô\x001cãÎ±äüM0ìc	tûXI©&¹\x0012mÚó¥\x0015yÂÁ"Óûö\x0001b\x000f»ö\x0001çLÂ?É«ã(RX\x0014èYÐñüz»i× Ënl×pjñyÓý³\x0017
¼D¾?Ë(¬	éá^öË	·ê	w±¯A<î¸¯s\x000e]\x001b,Ý×S83ã¿2ÝÚ¹Æ«&\x0007ùðþÎù{¸@\x0017VX\x0013.¡¹þ5;±Wìâ|¢`!M«pî¢\x0010éQ»Ã\x000eÆöt(.ÆóïÙÇ ­dß·ÝKÜïótñ¿¤öZêßþ\x0008ÏÖVuÜ-ÅËÚ\x000fè2Ö^|ñí\x000fÿ×¾ýáÐ3\x0011µ*o­S\x000b,}ïð³µ]/\x000eb&zñÅG½øÓG=$\x000efO\x001c8pÓJ\x001cù\x00167ç,ÀpaÀ\x0005-®\x000fá)¶VÔåÚ\x000b-z\x001bÒO;N\x0012jÏ\x0013¸h]âÚ9¹)U»\x0018CïN=\x0011=MlwØHL?µì¸;5.º\x0016sÅ9æ`E(vò
sx{=¬Äô|¨#vß\x000b2%·\x000b¡¬»Y\x000cà<ò¸î¬zá9ã8\x000e\x0000ôÖÕ\x000e>\x0017<\x001f|hÉ|ÐóÈqå¨eê®Î³#K÷ )³ú\x0001^VáÁÓýaä<rÖ²#k°
9µªbB\x0016xDdÍGqA;Ë.\x0005òÎ%°!\x001bàµ\x0007jâÓ¸Î\x000f3L?¸^º\x001edò[\x001b<\x0017Lpd~'ÞU\x0011\x00111EÏ+ÏókY|;¤ËbÆn\x0012uQ \x0011Ym\x00136¶vVz.\x0005à½o¯!Ã¤è4±ß"ED\\x001b.ªmüÅ\x000c9²\x0003ZY\x0016»0\x000còóÈã^áÕ{¥¼Fì\x001dëû8Ïµ\x0004!§¾Ïy`\x0018A\x000blJâ\x0007±\x000cVä\x0003q-òL\x0016ø4r\x0018Ý· ößL4-
rÎ©©.;'eq!ÏªNO\x0010\x0007
ßâFµþü]ÿú÷Ï/þðÃówøO\x001f~óüïÿñü×c·\x0011\x000fÜÊÑ%\x0011¥ äÜöàäâ$´5²ýòÅ\x001f>{ù1þÓ|ù§O_þáîu¹Ý~\x0018ôsÁ8Ðço=/ÀgÇÒ×Åzé\x0001:Ã¿6<#¯\x0018Gã(Õ®h åeq 3eÿKCÙDèëPèüúPHXJÉ:~gA{ãäH©ß`(y\x001cJ^2.0\x00014*®v+R¬\x001dm\x0014]\x001cJ\x0019²dÁ»ÒÛ''#¥\x000eÅ²¦"~ÉýøÚPvoaU.Ü¬\x0018
\x000bïÒPBà5\x000fÀã8é«re\x001cÎý8èçõq Û÷ÄÛ°·@<\x0004Viv¢Ø~m$~\x001c_2\x0012<
¹Ù5\x0004©\x0007\x0004eÅûI$ãâHò8\x0015û°ÃC¤i+á÷.\x001f¥Éx\x0004½®$#IKF\x0012¼4¦¬\x0012ÖÁÛ.'ÁXû[lÃ~+\x000fUSÕ¯\x00183\x001cð\x0005ÊrÜz:I\x000e%Õqý\x0016C	ãP¬\x0014\x001bZÆ"Ð÷aáÍ\x001c¡dq}m$v°/ú¹`$[¦³ÃÙ=OÔdó[Ã_Ä-ù"¦iÎWãJçD\x0012öIÙõ7\x0018JIÃPJZ0\x0014îV»¨â\x001dÊV<êv=ÆOòÞ.
%¸Áó¢\x000bâ$°\x0001º6\x001d$\x0015»ô\x000c~¡a÷¢\x000bâ
\x0017\x0002ý#w¼éÏ¡I¨ñÚPÒøUÒ¯b<g*µIüád$\x0012R ÿ\x0006k%ì2ªl¤]1\x0014[X\x0013p\x000b\x0010	ä@R&Ù`\x0012Íà\x000fÓÏëC¡òðÜ¾
â·\&ª4âZIÜçkC	ÃW¡\x000b-÷B\x0005¢ôÉÉPÂä½æâP`\x001cÊµBü­\x001e\x001e\x001da¼\x0006³lRLý±l\x0012\x001fº68~¸ä«DÏõ})¢H~´Õ½8ñ£,M(býÕ¾X¡;»}ý\x0006{1ÞÿüßÃ=øÿ¾>à"+ BÈo]ÁH\x0017ïèÊD âêýq|Â7Èç\x0015\x0017/Ño\x0003o²haA¯²q"}y4onGófÅh\x00027fÄ«½(U/\x0012¤k¯ö9×ê:³ÓJ1\x001fìRþúÝÿ{ÌéFÏ¢ü\î³4çCêûY±_}ôÿ{-póÁ \x0005~\x0013ib3ý\x000csS|\x0012yRÜ+\x001eiJ\x001cáÜw½4\x001f\x000cM/\x000fÏ'´þ@JÕ|0g+qvZ¹\x000b0aÀ\x0004\x0005&)y1g\x000c\x0012JY\x0002Q1=¦=Â¹×ù4\x001f\x000c2?»s(§ -\x000b\x0012H%x|Dz3\x000fYóÙ³Ä+²sÜÞgäÑOnÇç8ËÀYtæ¹ãä[¸Ü¡s>:9Â	Ã2\x0002Í22á)î8-ß ú¶ä\x001fµ\x000f>ÂYm©(¶%<A¸K\x0005®#ÑÜ@ï5;±Ïp}û´û\x0006K¸}\x000e
¢rn_ö3©Ú_\x0016R<\x0003#¨fÅÿ#¾¼Ý\x000bû"è ì{tF·¸1U\x001frX,%»`)Ù<lõ6+öz³\x001dñ)´·»âÝgò~r
t\KV·pFÛ§§¶çýþ\x0014\x00054?\x0012	:\x0000:4257Ln/ki\x000b F/J\x000f!>j¤s\x0004Ô\x000f¾ó
ïÎ¸¦A ¤\x001c&Ú¸\ó\x0014Ã£\x00068GoÄkLÔzÖ DÿÈkÉ&ùò\x000fê
Nè(\x000eÕ&u\x0010:<¯,àJó·ë±Ib\x0000ægÚq¿M,nù}^zñÅ»ÿ÷Çn¶75§øpk¨\x0016LkIqñN\x0019÷/¾xõ§O_ß»4Ò]\x0012\x0013ö4§Hq\x000fÍ¬õ\x0002ÀDuèü¾@y+×IÝ./ÚP¹¹Q ÒÃº\x0017YÖ\x001c\x001eÖc×\x001d¸³\x001e\x0005õn\x0000¥
P\x0013¹\x0002ô\x001c¸A]qÜ$»
³IÃh¦Ac§é*Sê­\x001c¦Å^¿Ï:FÔ¤BÍ½\x0004ÚQ\x0015a[ûP´Ü\x0013}Lê¡\x001e§[O\x000füÃ\x0007VzzüÛ÷ßý(\x0007¿~¤	ð]\x000b¹\x0018!¥þºSÒûäã/ðÇcÐd\x0006Ðd\x0014 H×öÈ¦ªruª\x0015º1aÄ\x0004
&Ýñ\x0018\x0013d9yÝ§t§·òQP·y¦\x0004êÄ3=\x0005Z
¿Ó;\x0017/âÂ®~;ª39·\x0004Ê)â\x0007g8\x0005ñ÷p#åÇË`¸¥\x0013^íË|Ç?Ì¹9ÐS\x001cèSh9Mb\x001dü§X(Üéw\x0018t´P§±ÐàxúÔj\x000bÎL¿ä%º\\x0007\x001dg\x001443\x001a¸\x0005!r\x0016)B4EnÍ©ÜéâtÓa%y£XI!&n÷\x0016
\x001c.¡ç7\x0011Ë3wç\x001e\x0006µÃ§çA3Ë]\x00031Ô\x0000\x0002Æ¹1[¸¾î\x001a\x00127Ð¨Ñ,	\x000bÔ\x001e«\x001dJ8£"ÚTC¥AÝ8£N5£î	\x0012Ï¨­EpuF\x0005sÁ¡ä]\x001e15{höµ\x000b\x001aaFÑ9§\ÞD³»s\x0015=\x000cêÇùôªùôÜ\x0013\x000f¨}WË@'Ð>£+Ö|\x0018A\x0006\x0014GyÍ£±\x0002¯ù ©S\x001dÝs v\x0004µ\x001aPÓ¥ä96\x001ev6z§;ËaÎ8hÔ(\x0000wï¤&®w\x0011lì&z§ÐaÎÑ
õ\x001a7n W<Þ3É1g\x0008ç@Ã\x0008ªpì£\x0011=x(xUÎ|UÎ¾ËãÞ¹*\x001f\x0007\x001d¿¼ÊÁ+IJ\x001c
Ø¾¼åYµÆ)Ð<.¥¬YJè1ËG×]f\x0012D\x0014Ð;²ã ã§ÏOÎA¥,ëÑÇ\x001cï<\x001d§,#eÑ¸w]9t{c\x0012ÿN¼YÎë\x0000úüÃÛwÿ1£\x001cP¯qB£õ\(^¨\x001dàlvqá\x0015'|\x0019·¥¢Ø"ÝX°Ù\x0018\³¬×w/c]Q8v\x0011/\x001c&1fêþRéÆý<s\x0014\x0014/]{Púy\x001eÔ»>6É*"¾ïu`;Ì¹u®ÒIú,gÜâK"·Îv¾Üé¸tÂ£ßÄÅ«ø©5O-\x0007x¯'v§qñïÊ\x0002Þ\~Á\x001b7Ø½§²Å¥0.,» ì4¶ÐP¢yìE\x0001¥GK0OO÷\x001eî\x001fã&~qèx©ÆG.	þÿãõOïß\x0013Ó\x0019Îå!$Sk6É»Èé#\x001dÏ_|ú\x0019þ×_¾~MÄ¾uî&vÒO½ÂÞ+}..|M­U8Ón²iéó@/Ò{Lç\x0000¾\x001f\x0019ÜãÍD¯U\x000b¿®\x0008\x001eÌExËÇ2¹¬mA
0ý¬]²\x0012Þn¾\x0004ooZ¦ßb[MUOR^\½\x00045µø[¡OÅ·ù\x001a>IJ´Ù6°V\x0003]áøjQûD¬ÄwéÐÏkø5>!:)D¦»»\x0015|X;ûn}wmöq\x0002Ógq­#ÔGòP'éã°ÝÓÏkôV2­c0Ýv\x0011Û·æÓøÙÝfºUÚ³xÿöâ«ï¿ýáûà¡ÿ¤D\x0011d»¬jÔMÖÁM\x0004\x0008{êîç/¾úä£Ï>9ìâ\x001eÊ1uÈ¤\x0002Y\x0005Æ\x0017.Î%®\x0003¸GUêÇwI®%\x001d*çC)\x0017Ü$yø,\x001dz\x0003Gz\x0007Çw\x001d\x0011+\x0004ý4»\x000eÌÉ3ÙE'À\x001b¢\x00028
vôv\x0011<\x0017\x0006etkåÍ7öyÈ\x001fT\x0008\x001cg\x0006·g\x0006w¹³2c9db¦\x001f\x0015\x001cg.Ã<\x0017ý<Ç$j;\x0000ÜêÇWÅ+F^6Ë%\x000fÄYM\x001cg|#²:+0®OòBÑÃÈÖ\x000c«Ï\x001aýòKþ3¤,
Q»îqÈ³<;
t\x001c¡õ¦A\x0006!Ð½ø\x0013¤\x0015¡Í*s¶Û»LöF\x000f-=\x0013p«ØªWº²Ñ¬ey.DÌCåÝ9æ"O_\x0019ú\x0019\x0008xp3³\x0004r\x0014ÌãVgõ{wÀ	\x0019ðB\x000f¢d\x0012\x0004\x001aÿ»Aû\x0011Ú«¡éF\x001a45ÈûtÝ«GEæÇ¡Ç
Úêwh\x001f\x000cßd2õæ\x001c](Eá¬9ñyhòp÷^QûH\x001e\x0015àMÄ\x00168eËM§Y_\x0018\x0005ôè=;½ûìiÃM\x0015­°ûìåhCH0PkadVï\x001dÿ@f?2ûKÌmÎP¸O\x001b1;a\x000e\x000fÊ%3ç9ëI=±íw\x0019OpvúK\x0010iÛ&úÁç¡w­êEÅXõ}Ð&.Ê9ÔD\x0016Ið
iÙD{7\x001c,Þ©\x000fà£è®f¼¬ð°á7öP5¦×0Ñ½\x000bz÷.P¶ESïLÇyuV|Òh'yuç¡c\x0019¶hú©¦Þ´¶í\x001c\x0011LU,©Qm©'\x000f°ì\Iqiú©èüóU6\x0019\x001eS6§"3=I	=\x000fNï\x001e~j¡¡\x000b6\x0012{jS\x0011q^ÒYY·áýù?o·¼ÿT{\x001eòî\x0013äÚE¯z\x001e²}ÄòHqàüùí­¼U\x001bIj]ÞÐF\x0002KnQ{\x000e1\x0011³ìHÄÙþÛílÿMíænÚx,²è\x0019¥hËlOR4U¦ýç¯oûkí>\x0012$7&GÒ\x0008jÛ\x0008ìI\x0008fÕ!CFòõ­h±c\ý©§<Ä<Ò89e&onÍäÖL ÷3ZÈJÿ¤YÎûë[ní|\x0007ÓÔõ«/â9
À,jDª.æã^BWsí^â²\x0017¿\x000fðhO\$#¾j6ä\x0005Ýlÿx;Û?ª7\x0013é G£ôóñ¤= É¤\x000eQ·*oWå³zUú§Ô\x0017¥ã£\x000c¹/ÊU'%íon÷@í¢L!Ëf\x0012]·^\x0007ÜÖ'\x0004?É\x0019Ñq?ßrk§Zf[æöö\x0013\x001b3qï¶«\x000ex¼.\x000e5«|¤?i/ è\x0019\x001c7mô¥k§¼ìæ7[vº,èÙ\x0003$irèÅ¬°ÕÌ<§Uì´:ßÜ®N­Gr\x0008ùÌt±{ßS¹\x0002ÚþJ3{kæÚM<ÂR\x000c¸<£4UvÐ\x001dp¿ì~FÜïn¹ß©§¤fzGwm¾]ï§\x0013ü²ç\x0019:4ßÜ\x001eZ;¡ÊR\x000b=d)êÐB§æ¤7ûù[»\x001dºÍ·\x0002R(cî­ù]vüÐi?Ø7öZûÆmïC&Ñõ²Óä{g\x0001vM§«Ç¦ð\x000f\x001fPdêýûÿ^+?}þá-ýï\x000f¿ùùÿ;Ú1ÑK,Å^\x00117H´óq²._¿~U?}ùÙô¿?üã«{Y\x0002÷ðù"¼\x000fµb¾JWfÖw	1&é\x0016Âd\x0013×Áoi\x0004Oáó+ô\x0019\x0008UàùÆu!xZÔ u!½Ý*îªÝPÅÝ%üT¸,\x0018gY
&à¡Ï\x000e\x0017Ì¢:ú<Òç«ô"g\x000bDi\x0014J¯\x000c\x001ff®~Ëj¬ôµÁ%zû9¤tïÅg¹Â¬Î]_`À§\x001c¦+øh#½Õ¢)âÄø­UVHèðÝ¸c:sqÏLÐp¨ó2IbñÓ¬q\x000eß\x000e³ß^ª®à£K#¿N\x0004·\x0012å"%óø~X¹ôó"~ïÉHýg3Ó'Y¹yé¾ã¶4öF.Ò#¤\x001cY>ñuÏ\x0006îùi©å§aß¡×èÝ6÷¦æ&3å¼<i.©¤/a §hà%z³e
\x0002=\x0004'Rý¸iÎ\x001eÄUô~Üuüå]\x0007O,~
(à%¦î¢4¨0»ùéðí0ùôó\x0012>bs2{¦XË\x0017©-ÍÔO\x0014OønÄw\x000bð\x0013;\x000cñÿ§î]ëH4Ý­`\x0005\x00103S{
F\x0008\x0006\x0012ðÑ A©ªI
È@F¢IFDJVr\x001b5»ÃÊ;¾;ÔJ®ªª»Û!Ü¹w\x0016£Eº;\x000eòõ\x001d=öPUSý5qÎðeãÎ½ÃôÑCM\x000f[é©.AV¾âhÐ\x001a\x0008fpwö¤w5½ÛL\x001f¤%Q/
¯|«1sÏI}ø±Þ¸qëÆ5Zª%I¦Â3~ÐCíïÜ+o'~mý¸õÔä\x0002ë/uDÖÈ\x001b5ú\x0010»®üqxl¡O[¯8ÈÊÅí¥ð\x001a¯dßê¹á?]øv\x0014!|ú¸
äxãª W\x0016þ£`ÏÕvÒ»~««\x0006ñ4ð¿Ö<\x0013ü4WVÙ\\x0008åÜÈ_7æ\x0017âiâ124ñ¹ø;\x000e½ É/ì\x001bãF5&\x0000%N|¿qóÊ\x0008å<Á\ö®\x001b(ÏM\éþ\x0002·_àv[¤«Ex\x000eo./ÏQâ\x0018¨ïãrúTjý83£ ëÇÛ7\x001f\x001f>¬¡VÞþ8kl·ÒJÉcTZÐ})òýo^Ý\?[Á\x001b*ÞÐË«9\x000b\x0018\x001c¡:sJØÊ>váô¦¦ÒÚÅ¾0{\x0004N
õÊI\x0018E9ÀxmÅk;yõà9ô\x0006tûÃ¯!öõ33vyÇëxcêãõÉÈÁmÑuL¥ìHÉlIk(|¯æÕªÚoZun8\x001f£ôý`\x0018$ùw°\x0012}Ö¯6Õz }¼ÞK4d½\x001d\x0016º.r\v\x0002v5°ë=!ÔZÜq\·¯DáÄé¸k\x0006\x001e{:2°\x0016v¥ÂIs­\x000cØN|XX\x0010lâõµ}§ý0õ!ôbQ­5)\x0015Þ}pSzqñZc¿$BK¹\x0005Wj·Hdy\x0017`£ªõ`TïzÀÏ\x0015\x0001¼æ+Î$od=ìO30T\x00166Ðmaà\x0012}ðÒ~nR\x0010\x0017\x0002y÷YÀA¸·ÓðÖÈ\x0002\x0006#ZÆh`ñÔL\\x001e¯²\x0002Ø\x0005{ð\x0000\x0017ò8\x0011äõÇÛO«Þ\x001e\x0005¢SV\x001a¢7f'ª|in"\x0019¾¾:y\x0014\x0012*Hè $IK¦´qT|w¯æÚ»Z(£RF×L©½Ì&\x000c+X\x0011Èk`Êò¥&H_Aú\x000eÈ4
Á¥[<1#Ì¤­\x001b 'sUò¢ÌUYMé¤«6Q\x0015\x0004wÕ¢kî\x0005sAc{-æ8î)cNæ=­Æ42Y#ä¤\x0012Ô{e\x0017Ä7×bÚj]ÒÇfLí²ÆnÆ\x0004Î=z@Ä\v¹×a¦\x001a3µcR\x000bH\x00180y\x000fnÀ\Y^éª
µ91!?Ó"&Ð\x0018Bé£ì \x001d c½2cûÊÌ2\x001a\x001bz¦¡¬²2ýòÌ5fìX"LúØ©¨à è+'pN¦\x00129éðZÍ¼\x0001¶`êê82ºý8R<Ë-ÿä>W`çi½<R~óÍ?údNÁ4\x001dÅ\x00103æ»(cr·§\ÁvÌúG×Í?z\x001eîÅ¿¹Nybx\x0019ðdr»Ë1éÂ-íÛ\d-§\x0010L-;hI\x0007x-¦­<#cÛ]#Eu_lLÇÍúNä'panv9hÍÑµß?ø/r\x0001&Ò³b\x001c!m?|½.}Ïa$#mñ02ÒËâ\x0019\x000e£¦Ú\x0006L\x001ae4õUóÂü`¢Ë>­1g·}2Òiµçneú|Êz4¢&Áq\x0018_,ÎH[é¸ÿ¡"Å\x0013¥SÓ\x000ccö=0Ä,Oòè»{ñ=$¡Ö~=\x0000ýÚã\x0019\x001b\x0006µnjX4Âgù®í{iòvÁ»éö{¼ÛÉ¤\x001f\x000eLú¡Ù¤vØÍ!\x0011ÿö4#
»=\x0006FÐ÷\x0007 ïAC\x001c\x001cä\x0000Cé\x0007P³ÝÇ;èpçÓµÔ±õU\x0019?/yîør>Æ=.y°åsT\x0003¶ê\x000cÿû\x0010íCÉÖü÷ßþóâ÷_Ö\x0015U ]Ì¤P<&õ½hìÎ8!å³°9¹x~uùfI¸Ö\x001eÔ|\x0013rØ\x001c¸\x001b
\x001c\x0007!UïD«^«§\x000eä4ENÝÈÔÝ¥DÉ8²\x001e%\x001fEgvd]-\x000c½ae\x0014\x0001Ù\x000e#\x0001Ì8Te7âÊÈºßÊ.\\x0008\x001d§Êx¶ g\x0006¦·3Ï)ÄL¯)ÝÌna"IHd¹EAÏd{ÚÇTd>2t?sRY.3q¢Êi\x0006=]2øNÈÕ\x0001\x001bÎTÍx°Iyh³â9¸Ya¯\x000eäj5ÃÕÌ\x00133²Qf&yFíº9V+#ö¯<¹T[%Q2\x0001P²2ÔL¡R;sªFê_\x001ac]^LÚp¾ÕbÜ+2èqF¬¹¾N6Ü'4yW¦²ùÜ\x0003½Ìaq§n"\x0006Ogý;Ø\x0013	åÌl¶0Û\x000cí¤/µ·w»¶cåzò6¤¿ô®\x0010KÎNR`'ÔÂ\x0010|\x00065ÓhÛáL¾\x000b°â\x001b3U|¦§Ã\x001fn\x001f\x0008ð84ix©R¡ÙxÙÚ\x0018õI~9Ù.ÛAî\x000f8¿¦ù(÷¨èã2»2¾pSãª\x0015îâñ\x0007z"Ø{¬4ÐÙsèç\x0006t>²ÃÜ	¸$zâ½pïio_­\x0013¿iÄ,jNØ\x000e¨%Þ
öÖ\x000eµÃ\x0016kSÃ\x0000¯nc¡µYûÙ§8ÓùÐ]\x0019;l1¶f]p²¶ÏåUyqÃ°HfòX}Ü±â\x001bÌ×
\x001f&0t)i'Å\x0001#s\x0007Z¸r'½ÛT4·O96Ï«Ç«ã2¹sz°µ¯ÌM\x001fû¹-Ü,Új@xyÓlo\x0007;®ï¤ÿðÇ\x0003ÿq\x0003zÈÓ¥Èæ\x0000\tE~«ØÜÍTµuÞ;øß\x00077ÏÿÞ°;Ë\x0012Ý<\x001b\x0007HÙê^ò÷\x0007äïûÉÊ\x0010Z/Ô ÉeoÚ\x0019»w­|8X+\x001f~\x001f\x0006Gò\x000fÈþÎÉ\x0015O¥\x0018î\x001fE\x001aµbãùÇ_ïVÎ{\x0012­\x0008<C5·ÛÉ¨:s\®ñüêõÅ\x0006ã\x0002Lq\x0001:q\x001dH(	TÅÁÉ\x001còØ
.i"íÂ;ú®Ä{0b=/{e\ûKC]\x001cpÃ¬Ãuy]¯yIj¢Ä4VÛ×DY
sQÍ¼ÞLy½éä%'~éaÞ³Á8Xx'YÉë*^×¿\x001c\x0012óÒ²×\x000c5n&iæ\x001dgX\x0012oR}¼^\x0005Éª[3é¨ä\x0013Í\x0019;3©wRÕG¼¹ª¯\x000f8å\x0014B\x0006N, ¦f\x001d4ðL?P3°I\x0015°IÀz¶kqói_Ë^aëJ®\x0003¶5°í\x0005 ÏYYàWK2¹AÛ­¼f|ÌÊ÷
¼¤²8N\x0017c\x0003ÓìEæ\z;pª{
\x001cl\x0011ÌÔ!Æ¸AæµGÅ,×áêêÆÈ÷|\x0017nRÜ7\x0018\x001d7ëCy§ôj¼\x000f­«î\x000búØE\x001bB:uå| U?NE;Íå-Îîåï\x0018W/_×¹|©¡Íðò
\x000bÅ,)
°k®ãµãwoàT\x0003§ï\x001dõ¦\x001e°ÑÀVÊE#]\x001eNäÀX'\x0014åö9Ð V>\x000f}ì\x0003¦âõâTú\x0000ÙØdaà\x001bÎÎ	ñ4â¢	j½3"BO%¿bÐè½3Í
sÐ-iÂï\x0002ì*ûÒÇ>`°2ö6ààè$XÝ\n¼\x0019xÌee`\x001f;q«jtËó2rÒ©ãs
Öñê\x000cÎO\x001b}+BnäN;;Á^É	áôññOëxcå\x0004ÛØé\x0004Gtyø þx~RóFÚ®\\x0016õÛ\x0001Ø©êHsªóHÃ«íTñ Ù-e\x0005{Í½MÎ\x001d½°·öy\¯Ï\x0013©¯±ø<4 '±}ùQ\x0007Ý |vç«\x0005L\x001f»xéÕ]ó\x0018r¥¸t\x001fÃ
\x0010à¹jóVà\x0010+\x0003Øi`:xµa¯GÄiI¡[üÊã#\x0004×zic¾Uü´÷ß7r4ÓwlqÖ\x000e\x0004º×/e\x001ddi \x0007!g1FG¼õð\x001eÙ'B¦¾=4õíwjj[F¤	ø³©Iáç·\x000f«
\x0005pûq\x000e\x0014ÿyÖI°N\x001cø#\x001då_/$vL\x0008gZßkÏJ´"\x0000xÀ\x0013:QV=6Aw=q¬c/±W\x0012âÌî\x0001©Ä°0ó.ÖN\x000cÕÞ%alê¢¬6Ès\x000e\x0012\x001fsîå´8¨)qPßù"\x000eC·Á Î¥¡\x000b,*'A>&&¿\x001e¸ZÃ¡w
kXþ>¢5e×\x0005Åïu\x000e¹\x0014«Sµ Rï0xqv@:\x001ad(*FÓ²éæ[õè\x0004\x0011°® &\x0013#\x0017¿\x001dt
+Þ{9×à¹\x0016x¢µÊ+n[\x0013Q±üZ0$~:Åky¡¾8 ûæø\x0007\x0011¸\x0002þðõîápQÐú°½?¼5°
\x0004hèÀ\x001e²ÝB>ñÝ¼òÝ¾7r¯]vFq\x0018íÎ¤eüñäõÃýÝãÃo_÷Z7MY\x000b\x001e¤Ô\x000b&ÝÅÍÉëëË5¨iúP£4%/9+\x0013$i\x0015üRÑzÖh\x0014²\x000eQí°En9t\x001f|\x0003ë`A\x0010f=ì8¸`AuÃ\x001anzIfPÈÀî²\x0008FmÖ¼^m\x001f+Æù%ùNy\x0003«çå03k¤uÁVã¢Êþ\x001aZâÚIy;ñº
^*ÀaÈU\x0005»ÏR0î\x0010\x0019×n'35È\x0019.µiXä\x0007+»¥VÎ\x0015Ì\x000eèðM\x0013m\x0001\»IOJ:\x001eO^|þôõäÅã/ÿ¾\x0002Yy\x0012JÎÄF
³\x0015+l;\|Ëé\x0017¯^¾=yqóæÍ¿\x001eÅ\x001a\x001b¶`;-ø\x0018,så#.\x000eË'°
sc\ºÀ}
î7Û$^Ä[²dY\x0001÷Gæ÷6ãí©§àùs7y$}\x0014&7A®h3|®\x0000¼<¤<¤
ä4\x0015§W ÍKG%\x0018kYx.\x0005µön!×ãóc&×Ó÷ÇfòÄ3×1àEÊ\x0019À\x0004\x0019´d8ÎmÜpÀ
ýÜ$<,'®\x0003\x0007\#\x0003ù\x0016r£ëµ+ÑºÉ­ã¡s\x0014c	¤(k\x0005æ&>ô[U[µ\x001c/\x001fÎvÑ\x0015_|R\x0012\x0014òcC¶È¯ÉCÿ¨ñ\x00122AÄõì v´Úõd©\x001a÷åt.ÍÛ\x0014¢4\x0013«(Å{\x0018}Ê´ägJÛ¾!×sA9\x0005\x001czp\x0008ÿùñávUÖ\x0019­³Ã\x0013$H·¶\x0003>W<þG\x0017´1nNþùæúü(å(\x001aJÉ}§¾¢ô]eíÒ&&¨\x0008£?¹ ²\x000er¢lG£²ÝzJ\x001aM^\x0004¯p-¨¾eC\x001a5óÊÐÀ8»"ÆQîªQ:ò\x0013¥\x0000|yÚC/-iÌíJÌXÒÄ\x000eS\x001a(ùØD2âëÄtf\x001933Zº\x0012LE	¦ÒY
H\x000e]\x001e+åÄ"*cÒV\x000bcÞ>|¸ûu\x0011ªC\x001f\x0019½È-'ê_wA*\YK\x0008ÔLÓz)}mJßnJë¼\x0008áÿ¾\x0002ª£aL?SvÙiµ¯ÏôvkÒtâP"|OU\x001eå Ò\x0006í°}ÆGfÙ@ïÛwæ\_¢I\x0007\x001c%S1\x0007¯M7_m$ýpHúá{$Å+¨¶iò\x001d&M1K\åSI!c9;\x0011P½$c¹z+ÏÞ²n7=p\x0005RòÊsÜn1\x0014ãî9)Ql».kNº09ó¼IÏ\x0016õrÎKÛ0\x001at¦ qÞ\x001e®ÑvÐÐ\x001a½=X£í ÿ5j\x000e\x000e(º;wsJ\x0003éb²¢\x0019eä^ZÎ<®\x0005½=\x0004mßL^ÂìDÚ@NzDÄùÌcvØöï\x000f·}»IuÈõ§´ïñ\x001fE\x001bÃØÔÌ\x00146¬"õ&æìóø\x0004Ãa÷ýõçÇU¢ôÉ¸¢XèMüTs0*ý½~Mçýõ«¥ÌsÁ\x001dï|ÂÕm÷«yiFY,¼\x0018÷k±W}Ð33¡;SEº-\x001c³\x000bÈ\x0006\åKÉø \x0008jMó÷*à±l)?Ù\x0007lECBùá¹Ý)\x0011½\x000cvæm\x0007\x001eÇ\x0012p:Ô\x0019Y
ìX©/¢¢x8j)¬o\x0006Öª²pNÔt\x0012ÒOHú(kfb%6\x000e3\x001a4íÈºFÖÝÈÞØ\x0005þÛDÕÞ È;m;mT\x0005\x001f;\x0012é\x0002M5/,Õ<dTÂÜuÑ\x000cÕ:¦½È¥\x0018 #{yrÈ\x0010Yïµ¡>Ü ût\x000bZ¤[4Íî\x0004FV\x001cIÚk\x001fdW]xô±\x00179¾\x000bD¶ÀUë¹}õÌàvd¯ëKïPüd5r´¥¢\x0008\x001dÈ¸<çø31y\x0007p¬\x000fUOÖ\x0003\x0017mßlc»#àxlÈ*âP\x0013£³XÓ z(æ-'Eq>Ú\x0019ýävÞT¯âÔ½+ýÈë\x0013çHa\x001d¡8W·Õ<\x0019@ÈyTB§¹¡ ó\x0010E\x0017e\x0012\x0001"¯ÐÙXjäÎãM+£D\x0019\x0004ãb)=T]\x0018f¢¸vâÉ\M"¦\x0002°Nbq7
^ÓÏè([Øë¢´öfb×O¬ËÓ\x0007.\x000b£ÌÑà°.úâvb_ÝÓy\x001a@\x001f±5rO\x001b\x0010Á\x0018\x000cë\x00189Íd\x001f;ëì»\x00172M¦fd\x000cùøÒó\x0006d%ÇÞ²väT¯Ô½.Ü¨yèA¼!o¹]Ä§½î\x0010bMÜ}8-g²qeX5n<:o+dÕÖ\x0000ª\x00162}ì]ÈÜ3KJSz
cµ Ç5Jpë}Ü\x0000@dU\x0006\x0012r9ÞÊqâÌ$ÞvdSyo¹ñ»\x0013Ù\x0017ÅQZÈå
\x0011Ù\x000e\x000by¯\x0005\x0018¨a\x0003²\x0016iCÛÀ32ÏÅöi7b[9\x0017ô±8W+¿Rgb¹ª\x0013é\x0004î\x001c«ã";-gr¼\x0005M°\x000fD\x001bUÏhbõNUÙ'Oô§î8Ur\x0001xðÈ	ê×\x0008jûm}©±\x001d\x001645çò4ì¾»ÍÈÏï?ýBP+3.<r&%ÈïòÜ\x0011Ë\x001e>E}³)Ù¾8ÏÐÏ/_>§¿\x001d\x001es.\x0004­C?5\x001e\x0017Z¨\x000clsR\x0013Ô~>åÝL*êÔOîQ®úL¤î G´MCæÅ,¾m¥¼ÌÓ\x0002ñl]\x0014Ú\x0013\x0015¸;'¶NbëÎ¨\x001eêIU\x0013¹\x0007º:Æ<Î!S\Ì\x0003my\x0008ÇÐuþ©ÚVÔ¶\x001a#A:¢\x0014C®ÕÏÁ«dñ}°ûÙÚW¶öÝ¶Ö¸CJ[A"«hF]·æVêP!¡û\x000cAêxêõ°®ÙÔâDû°P(ÑÊ\x001c+KÇ
vÒ OkÇ´\x001d×ÇÂt3uuÅÄî;FS9çä\x0000ddé|UØ\x0007Zëj+j½a/Òd3¶5\á`ÖÉ´@\Ö»Q×µî?­µB\x000bk~¥ÒZö¢OJÎ½dæë%[±]}»þÍè¨T¼xNÖ\x000c#5ã>^ìnÛq2°I¬\x001dØ¸!Ú,|Ã-\x0013$æ
\x000bÓå¡]
í6@\x000fY\x001aeÔ)Ú¶¸!3
\x0005]Ø©ÆîöÐéÒìCï¯±\x0008	B0$
KÀ­ÔPSÃ\x0006jSz\x0002ó\x001bl1Ä¸a?hW/k·aY³@\x00141¸À=÷îû¡ ,LÎk¥®½\x0010³Á
Ñ\x000flz%TC÷°\x001f\x001e÷õú\x001bÖE; #O  \x0015ºaN.µ\x001aê@\x0006ú#<[±\x0004èèÚÉãfT2/;¤Vª\x001ej[]2ô±\x001aOú2¶Âó¡]uåMv?\x000fBµ®éc7¶öürE5Xûc\x0018ï\x0010Í~\x0011ºÕÏG\x001f»©a\x0008
4è:I\x00065Î
Bê¡®ý\x0010»Á\x000fÁó§4	Ò\x000bã:\x0019#Ø1íæõîÐ\x0014Ûo06^±ãX&IÚ)þÝ\x000eh§«uM\x001f»¡éQ\x001f\x0011é¥¶lÇ$Ã\x0017}ÒûØ®N=¹þÜ¦ùæü`\x0014
oGK%bìý8ÎU'6}ì¦\x0006(\x001d<±µLB¦ßc7ì:rt\x001bBG³\x0002
Öït§ë0ge¿H¨°)Ñ9`äpEÅµ03»å'ãXP²\x000bª\x001fÛ\x0015\x0019\x0000¤Æ
\x0019Y
]³pAPq¡¼ÚÕÔýñ\x000céKñË\x0017\x001eý<¶	/u+Ã½vLD¨
\x001bí½Dê6ÄÁÚ ä#íçúE¨­
\x001b¬íl~ØÏØé\x0014¸õÞM\x0018;ì¶#£­­m·X»ha³µµÈüs_4b/è´´b»ÚÚnµi´\x0017¯í(ÕL´H\x0018²T»aÇ\x001a;nÀNº¨D$ÒÔ\x001dú#ùÅ?h½ ÒJjêÔOíU,í	D=ÎÜ\Ê;;Ø¼:ÕÔý7»§\x000bmaoà¶^%SÔ4µWì­\x000f3~[R~Ñ&ÉçXj×,ââpÛìµH4)/WÜ©ß%Ij\x0012hp\x000b^æfØ»¥üô¤ô-CçÚ·^h\x000cÓyPï7{­!9\x0019f\x0006!uq\x0003îþE¨	Ë3·)#ßlaê[Zh¬oÅ>HÂ
Yx´«T¶X\x000c\x0012J]2rGqIânÇ¶6îÛmàÆ8Òé»\x001cÑ
Ô3Z]Ôéºÿ\x0004$jÅT,Ú[\x0019\x001bdN]RûmJ`m¿ÁÚ1È0]\x001b\x000cëüÚ\x0018ä\x0000\x000c3õö\x001dØ *O*îÄ6JY©rÁÿ.	%©ï¹}Úmq
\x0007ÜÝg	r;®Y&k\x0007ÁÖf0÷n«\x001b\x000e!¡ÿ\x001dÒ(ã0m	ol¹rUâwËµj0õ¦Ì\x0012²½Ø \x0017=¯óåCØà$\x0004¦z®½¸ëð&îæ¶VZÐ,	=Þô$]sÈ½[¢D=X&ý¥#È]æï\x0011÷8s\x0002/"ËrÎk'î:¹­7d·
=³Ëá¡%§J\x0012)÷1÷n±\x0002=\x0006\x001dpw\x001fÞF\x0005%%Âdo`{Çqxñ^I\x0007ÊäÖØýÞ«Qèý)YÞï\x001cÑ\x0006ÏÄýNÁt°¼SÿòÖÚ\x000cI\x001eë8Êq
øÝîVAùÅ>oàfc\x0017Ø\x000c\x001d\x0005ÚÍê÷e/ÇÉ¿¿ü¹×5Á¯<\x0004ðÆJÞAËk{ÀÿènÉ©0\x001dZ"äï»3Æ\x001e$câüèQ5;\x0002ÍÃÚ±Ú¨Ò¿æ#Ñí*ðr¬\x001dHúXKtºú°ßcÓús6Ð£WÇIå\x0017\x001d'lx\x0007yÑé8ï{\x001bùÞ¥Mô\x0016r:3WÊóû\x0008p\x0001OvÇÊ:ÿáý&»F¥×Ü6\x001f¤`Ã[\x0018Úæ\x0017ÈÛïþoÖ<Ýÿýøè\x0002ø!£.Nì\x0002\x000cgû~.\x0000½p\x001fâÓæÚ`|cÄÌFiQYIDM¢éÞì<*ÿxxTþ±;K«íàÂ,
\x0015nôà
ìæ¡óùíY\x00136íV\x0013K)l\x0019NÏ\x001aRXà
\x000b{>\x000cþáîÐêwÝW+îP±ºÖ\x0012>174×íÛIþáüC·É\x001d\x0002\x0007"'¨¢$\x0011uP»\x001dïtµþÇÛé\\x000c¾]ù¯ÝU½çS'\x0012\x000f`MbïìP¬ö+ðÀ³æà\x000bÐY³ÞX#ò\x0001TÌTÔPñ¬qÒÜî÷p\x000f;f8fõßûÏóÿóx÷óãUk\x001e½÷,"\x0010öZÆOä+âv)+*,Hã^\ÿ¯\x001fo\x001då!Eîj
i+7­ø¢¦¨IÎ\x0018Ö:Os/\x0014\x001dÔ\x0013y\x0017¢Îò.ýæ\x000e¬ØèE}ª%S·ånÜcýfæöz\x000b7*ÜÞ`¼\x001dD6Å\x0007Ë\x0014{qjä	¢ýÜ4i¹\x0013ä\x0002²,\x000eÊ\x000bÅSGî^àÓ9òîp|3xÔ§¡ìKÐ2øÁj¬ötÎï\x0006®+çªÅ~ð²§EàÖæÒS¢âÌ1Þ\x0003>j
dp6\x0004fcxjYV\x0010Ýv\x0006O3Éó\x001eðqhL9ÁíFpnM\x0003\x000cRev\x00022\x0015M©\\x000f\x000eªZ*ôq\x00038uE\x0011×Ö(\x001b¦tgnt$wÛ «½I\x001f7p»ÀS )4{ôÔöØÜî\x0006ðúÎM¦\x000b^\,kí)û·²N´wG'ÿ5\õS\x0007¯ûÁi­ã^I\x000f\x000fÎ¥4\x001d~¡Ýl®êæs?Ö\x000eï]³Æ
ÂsdôÇÆ"¯¡'ÑRêy\x001d:Ú©|Þ\x000f?Þß=¬þ

}ã\x001dMQËëÅ\x0019\x001bø]NûôÐ4ÿæäâÙ««Ëë\x0005©G¥¢N¾\x001a´Êo\x0015D\x001d\x000cW89 ¡µÚ\x001d\x0013W\O=Q!êZ9¦
Û¢CËOÎ\x0018é\x0014ÏÐ9ÃéÅ`À\x001f\x0011(XO
ãôw¢¦½Ô\x000e}o®\x0002	x\x0014\x0015âåê	&\x001cÓÒ[Om¡¢¦ÝÔd`ÍÔRà¼ì?ÞÇ»a\x0007]a\x0007ÝMÃëù½9`	9è¼cb=-Ð¦î_×\x0011/\x001a[*4M»(OùÜÏÔÇ§Va\x0007µ7ô\x001fþz6þéLýµÖ\x000bùéîáÏwypÌýqx c¦c\x0000Ço0\x0011~\x0014îO\x0017×/.òðËñ\x001b\x0008¹eÜópÍã\x001fÎ ÒØ{ýùþËí§\x0015ÆÆ#ñà]\x00129'ü
óm1?¦óúÕåóó\x0016ÞPñN^\Ñ9±¼vèÎÃ¯\x000boñ¤y]ÅëzyA4YWòM
Aì\x001bg\x001aty'óÕ7¤N^ÍÓ\x0003q9(\x001ee3 ¸Gõ½Öáê±péc\x001f/5ÇaýªT­¬Þ`½\x001d××¸¾\x000f×¥Èb7ÁÓ°Xp\x0001pÇ\x0005VòêW÷òÆÈ\x0013]Wó\x00082ôÿù\x0015\x0010yg\x001a\x001b}½\x001e|çzp:.þ\x0018È½(\x0012Y&R,\x0003{73¦\x001d8ÔÀ\x0007\x0004eß\x001d\x000fA6\ôÑË;ªB¶w¬óÉ¼Awò0o8tåTYÁÑÉèE7Óè×ÊkÆÂ
â¥}¼ÞòÜG?\x00038Êñ\x000bGU,×âú\x001a·sÃÙäNù:¦1 6$#×:jæ­÷éÝo)óó}\x000cåð!ÀÎë\x0017\x0017@5å×D­ïÖrN¨ìeCÛ\é@ËBæû9?SÔ½\x001e;èT\x001cÌ³ñ\x000fgãh¿·\x001f\x001fèÿ¿º]\x000eôzQ&*Z\x0000V²_H1Ä^\x001c¶ñöÕÍ5ýÿWç\x000bÉ\x000cL¤\x00150}îc&ÅÒ\x0015\x0017#ýc\x0011Èv6pá\x0011EØû@\x001bo*èü¹\x0013ZæT\x001d\x001e\x0018Q¦ï¤À\x0017\x0008\x0006ØËÓw\x001a¨S¬ÖFþÜ¹<÷y¾\x001eR\x0003ð\Y\x001b,Ogu4m\x001fè\x001c1}¨ô^h\x0013rc\x0016­\x000f
<çº4¯\x000f=^ì£~_S¿ÿ}PßÖÔ·ß3µ)1õø8d(¢æúí¯÷w\x0008vòãoÿõáî?ÖìEïÜÐè®5\x001fÒ.\x0012ó;ñâíå\x0005þ\x0015\x000fê××\x0017ÿv\x0014ÙUÈn\x0003²wË¢\x0013¾ ÛcõíÌA-ÙÌÒMÑ\x0003\x001dÊÐ,9a¹ÖÏ"A1,´\x001d¶RÇ:öS§âßç\x001a?)D@÷\x001fb/Ó\x0001í\x000eVô%mEt\x0018p©xËKzÐnp\x000bBmÔ +SÓÇ^ê\x0010átlo/J*.I¦Y¹fÚFf[-êA!¨õ	s\x0007°åâa\x0017ê°ÐoØFíêEí6,jtï¤õÃ£\x0007©$?´\x0008é\x0018w£\x001e;(2µ4P´S
üKPê´Ì\x0016ñ 8
Æêù:¸6jÜõSjúØkkêìääx4¬|åµãJÛ\x0000zæ)¢\x0007\x001ajhè\x0006'%ª´ÂË¸\x000e1"çôÁ¤½n *ê 6PûPo&\x0015É£0\x000cQ¨aA\x001f¨ºv?Â\x0006ÿ#Ñ\x000b[9B¢öÜúëuW\x001fp\x000b\x0005­Ô±¦î?B0
rg9gç5§<H®p¯e\x001dÆ\x001eÃ\x000c--Ð|D\x0010\x0005\x0001\x001e\x0016_Ð:m¤\x001eH2µ(tQ\x000fË\x0011\x001dìâíyXò\x000f\x0017ÈBýo+u½¬íeTkÚ\x0002·sbÈÌ%n\x0001\x0016ÚÆ\x001a¡}mj¿ÁÔèíqÓXá´6Ã#=íÞ:Ô¦\x000eÝ¦F¿Ws,Kãhä¨\x000buímÈQU·b®ëE\x0006'3\x0005£\x0003µyI7 Ù×Ì\x001bü\x000f*6åÅáT.$f)Ã° ÑÕ\x0008­+\x00075ên\x0007\x0015M¬\x0005\x0019½çLn«¬´ ?²\x0016Ú\x0005ß\x0006Ç\:ú	´½Ï?~üíïwüÆýúþËûO«æy Û\jebôAó{¥\x0016ñG°3ïAçWW\x0017\x0017üºýúòÍ³Ë\x000bs1zôô\x001c½njàj¤¶2cÂZ/ù1kg¤çÚ°µÏIñ%.\x0003ê\x0017¿ýýãý*hjéÉÚÎ\x0011©\x0013ûLV§ÞÍh\x0005L_\\]®\x0000\x000eSà°\x0001\x0018$G\x001d}\x0010¥\x0014-\x0011¹ó3G\x0007q\x0012Ç~bÅq\x000b\x0012Så\x0017\x0017{\x0007®&@#Ï\x0015{7#ëÊÈºßÊ\x0016#ÄYæõáÍÀ<W¼»\x0019ÿ7roã(Ås¾ûròO_×¶HQq90HÜÏH£\x0011§ÓaIô*yþéæír{NA¨8#ª87¢úr4\x0010ª\x000bªe¸¶ôõ¨z¬"TúØÃ\x001a=OrR2Àí\x0015ì/Ó»æÂãÊzXÐ\x0015,è>XËE0Ô@É­7ÚH%.¤¥'\x0006ÖX³Æ.Ö\x0014Kc\x001c²¦$rw¹@»\\x0015jAÊ¬\x0001Öú
Öú\x001eX§Ò)_ÆÚr3Õ÷1*Õîêªc`È~¶¢ææ¥:Þ
'®#«Ýu"¯A¬hid5IÖ\x0000UA
\x001d)Q`çHZaë\x0005º\x0016¬\x001b_v<\x001e°ÜÌ1´ÏàùjöX°f¢:ÿsFD§\x001aaÁ\x0016
`rÄdz¤ÕÉÊî²\x000bÚu-°¦í:cé¾\x0002^³Nóì:ÒÒ²\x000cf¼µ°¡4\x000fZþÚ×»ëäÝÝ»Ow]\x0013\x001eëÈùyo¸\x0011\x0016½1\x0018t\x0016òTè\x0010¼»xsñòâ_õÔ!·òô&\x001e7@RR¥gÊi¥\x001e¨o`\x000fÔqø\x0018¡ZÝÔðêaYg\x0011Q\x0007±]8}Åé{8
¥ÜEXÖqôKoþòó/\x001dV«IÇQÈDêLE%ä%P# £ºs\x000fy[P]êúPí(i²¯ý(BqAQ¡u×L¬Þö.\x0000\x0011TJá·¿\x001b%\x0013ç\x0013¾-¤U}U½cUrò\x0007¸ÓZ2»R¡â\x000c¿¾\x001e\x0004§¨=¡&-AjAy¨µ:úCßÑO%"\x001al9?¿h\x0006«\x0017å\x0006ÔX\x001dþ±ëð'QAJó\x001cD\x0007¼\x0012v`MÕé:Oÿ«E\x0015ÌpS99ÿñ¿a%0)Ï·¿ê4ì\x0000E§$WÝ\x0011¬\x001fÍL3X#¬®\x000c«u·e9/áõL-öð\x0001´©aM\x0017,­Ò\x001cèr´U¯Øq,
¨\x0000\x0015*@\x001fª\x0019û\x0018\x0015w\x0019Ó"`I{©\x0001ÖUWv}w\x0006\x0019·G­¢ï×0\x0008´ûwì\x0016XWÃv^\x0007áT\x000f¬E\x0016\x001c,ÑÀ_Ezûðáî×ùKkZÝÌ\x0017H*µÞ±E¥?ß\x0007+ÞV\ì>\x000ea¨\x001a¶\x0019Y\x0004qÚ¯0Ï\x0001¯\x0008\x0010\x0003\x000f2ÄiaÂo³uheo;­Lç\x00155sÍuÂ´&Ä=\ª§\CÌ³Á´q É§)ìïîï\x001e~Y5N&\x0016\x0016­P\x001b\x0015¢\x0019ÜZõ%¾»¼¸~¾7fè±ù ëÞ£6jÐÃµ¦)\x000eXy)Ï¤\x000bz¨Mej³ÁÖ`\x0007[\x001b7PöM(²î{Q§:õSë SUrÏLY!ú?ù@96z¨Çº\x0000¢®OÚ¨½\x0008;/#9Iå^®<?s6÷@O\x0002,¿Ö\x000fí¬H9gx\x001c±dØä}\x000fõ8À+ðèç^êà)ÝúJôi¸\x0005öR­¦ô[æ#Dm8Câ\x0010\x001cÓ(\x001b\x0011æw²¬ãLms\x001fuu¿0yÝ£Ô\x0008¯OÓ`r«\x0019ÞÇÁäÛÏ¿[äÎ'$xÎñ\x000fgTÒ{uwòìãç/-mJ1pw`\x0002<Dxe#«©LêIà«gW¯Þ\x001ck1\x0018X¡b>Vû5°\x0012õÑ\x000c²S3Ë¹\x0011\x0015*³BYÑ?Ò,E¥\x0000<òEzM»VFN£ÆìËg£zpàù*ÁÓh#««¬êú¬JRoe°ì.ï-Kíª0S×ÞÊZÙÕuÙ\x0015½L~FO@'\x0001¯\x0000-³§µQld
]Ãwm×PÙ5ôÙÕH\x001fh\x0002Ê£§¾\x0000Ò°£UzÚ/nd]c]³_É¨ õ@Á±´\x0008¢]Ì\x001a+³ÆN³\x0006.¸J\x0016\x0003%Qe¹KÜk½Ë1 UeVúøý®W­ í³¬-3¨²e\x0008lQJÎÌ\x000cHj­½\x0001Ýé\x000eü,[»\x0003ºÏ\x001fH)\x0008\ÆÓÈ)OÝá{°\x000e:8;X#\x000b  \x0016c)ÒÇ\x001a`\x000fçe,©aØØ\x0005Kc¬#[6\x000eA¼[fF0¸ÕÕu}M|jâæ<\x001aQ\x0007bÕ}«­ê¾g«úÚªþ»^®¾6¬ÿ\x001e
«|Ê\x0005¡£d\x0001þáÌ\x001c¦@ÞÞ~ZU\x000fÇä\x0015E¬D!Ê\x0019f¡y\x000fnEøöüåRAha¶5³Ý\x0000íèFôj\x001c«Èx	\x0013Ü`A;45Ñÿq­Ïþøû þ¹¦þù÷AýKMýËïúO5õ~\x0007ÔFMM||kZNMÒE()%\x0017¸4ÏàÂ÷nEþwµÁ?Ô\x0006ÿð;08RßÕÔw¿\x000fê÷5õûß\x0007õmM}û=Sã%3=¢îxæjIâËûu£Y0¸Ea
H7'oYW\x001c\x0010kÒLËÄDÿôòúr±H¶ÐÆ6vÑ\x001aU\x0011Ù\x000e4h\x0005DSâOø/ÏTH4ÒNC6¿a÷\x0018<Ñb[ëxº\x0003$\x0013Ä¶s\x0013åVÓúX@jIüÃÙØãAK÷Íu>é%\x001cÑNút­³üàâò¬7f\¶o-îµÂjaÊj¡5åðÆf():À%ë¸\x0017!/ß=XcÅ\x001aûX\x001cµ\x000eÄs\.íÉü7²Ê®á»¶ë(¦N¬É÷°FmJ]\x0017²$½¡nèDHtængÅ\x0000¬Þ[ß5,¤
\x0016R\x0017,¤a\x0008\x0010F§^Ôÿ¸zÄ±\x0017ëcÖÂºÚ²®Ï²4½YñÔ*±>F¡ó{©hd\x001dëQ3ë¤ µÆ\x0016§×P
\x0012pÒÈËÑuGa]É©ûá:À?ùZ\x001cýÅíÃíªÛK%åEMÚÄW\x0000ZÔb­±íäúzq~}¾t¹\x0007L\x001c;i YÖEbü·q+\x0015^¸¢Ç«Â±¨b5qrSâäzml|1\x0013¨\x001f´4ª¡\x0013cÅÄz¦ì·\x0019\x0018\\x0002Ã\x0003ö=Ú8Beã\x0008Fþ \x0007;õX­ª©ÑrzL¼»Çúï¿ýç«»u12²ÚÌ71\x00118×f£^ìdåb\x001fO^]_,U\x0014r¦ä6m!ÏÓÁ\x000c+¹mBäÞ|ü»\x0004ÚÈ'E·H>©¹í"\x0007>¢\x0003\x0003zDæº4\x001bíJ3ùxP\x0013¹7È\x0017±w\ò¥À¤ôd±8sì"l\x0000Oa
Â&pÒP)Ü^³ª\x0011ú\x001dÃ*\x000fG/Åõàú`nÛ 4O>²ÉÃ¨A\x0013£Çå^¨6tëê£eÛ:§>Þ¢H¢Ë\x0012\x000fnd\x0012\x0007½Fìîtîô\x0016t:Íõ°^¢hëeæu§¼6ú¶Ã\x0012,©¨=+mY¸Ð ëÏù\x0000
ö;\x0016Ç\x0017JFß´I!ðà¨Là\x000e5\x0017eáõ\x0004Gã¦åR\x00156òTÎ÷|\x0001?îUDßK+°K^\x001d\x0007ûá7ÀÃ}Û\x0017 VÄwª\x000frØ \x000f eÝ/he­ÿ\x0002àr>ª[ÐH?zÿáóãÇ»¿Ü>ü\F,ýzÿéîë×»UþÀÃpÑ\x001dHYÁ?O\x001fl¯f:ÆxusuñîüúÇ2féõåË·o/æ,\x0015ú±Íè©\x000fi\x000b½Ò
ToXG¯å\x000fqF9«\x001bÞWð~\x0013¼¢áåÔ\x0001ãctþ¹¦×¢çûôªé¥nJOíõLï9\x001fôj¹-s\x0013©AëGkMáéã6Û{IVGð,¶·²r`&ìèÄ7¾Ú´¹r \x001f_eáF\x001en£¥ö\x000bCR®®¶\x001ef\N|L¢£3&ÑmÁwã¬&ôp\x\x000eu
¬\x00199ßK\x000fÕC\x001f7ÑãuÅ§½a0¾òb|532¤\x0017?ÔÆ\x000f\x001bOH<YÆ\x0002w\x0008£3NÙuåÛ1üpe6Ñª£/ôÆ\x0003CÓX\x0019ôñëÓ.f'¾¯W¾ß¸òCä\x0016}J*É\x001cFÐ§¸Ï'zñkgÁoó\x0016(\x00193àXô%@\x001b¶=D½ëÂ÷±ö\x0015â¶}\x001b@Ë¢\6]¼\x00055Ü·àf\:ñ®¼\x0005ú¸	_»Ò+øÁrp\x0005èO	þÎg>ÞSGYn]úÓ\x0016·ÆuÃ3¢¯Ïc\x001b]1¸-v=~¨Ó÷¶ZEöìvÓ\x00170S"1EÙÀ\x001e¸AÙ¢\x0017½«Óf)\9<@ßo:AçH\x0017}4à\x000e0ÑÉÄ«¹î
ßàöð\x001blù	\x0014Àü\x0005D5\x0002¿\x0019¾ÀL¡Aû\x0017\x0008\x0007*Bt÷æ1ê\x001f?ÞÝ¼A¤¯'\x0017}üõîáß×¬\x001dO]ø<ô\x0007G&3äÓúX\x0014;ßà?¿=¹ø×\x0017×ÿzzò,FÔùY¬\x0013;\x0018Sæ«Ð(Å$
Á c?ì\km\x00075y°\x0013júØmlbc7
¯-UZ\x000eLñsóU¨-â]c>ÇªÃ¹éïî\x001e~ù´6\x001a·EK FE\x00037-Gã\x0017\x0008zÈGzTß¼»¸~þriU3óDoÊ\x0016½©Nf[\x0019\x00198ù\x0001ÄÆ
óØH\x000f³¯ýï9VÌ±\x0019Ã\x000eÍi>Å\x001d4à#\x000fþ³x\x001b\x001d\x001d-È3\x0002$w\x0014Î$Þ\x0004Ý¼ÔnmÙÆÅ\x000fHÐ\x000e6>:t|¥õXNÌÚ¨nèdEMWP^jhj
#\x001fmÇ_\x000c³ÐO\x001f2\x0015­\x0000#óh\x0004b&Õ\x001c93vc\x000e5s÷9g\â\x001b\x0005×g3G\x0015å)eêAN5rêG"]«ßM!Jà7mY\x001aUGUÐÝ·\x0015\x0012²"	­ éäÝvvåKµÈ°DHÚ#Ö+äüáöÓ¿¯ôñ@ñ\x0003;üà\x0015\x0002FIsy_ _¿ü×ãÈ\x0013Ý5B®\x000772»2oºÆ¤p\x001e¡4\x000cÅã[q5´©¡M745è\x0016fçYP
¸iÈ(8º\x0017×2ÛÙö3kàaäªÊl4\x0000Å×·7æØpäõÐ^WÐ^÷B\x0007\x000c\x0017KÜ×âÇt
[¸\x001c\x000ewéQc-t¨tè^Ò!Ùa\x001bRÊ¼IÀCÆ¼±39\x000eèXCÇþ}±UÉ1ÐÉÆÊí eþÐ°\x000b?Üþ|ûåëÃ,rJ\x0015rJÝvvIz\x0013HßJ\x00160Ï6¶[NÐ	2}ìEöGFäÀ³BÁXY\x0019~¦ý¼YWf¦ÝfVY\x001afdÀÿ\x001c\x001cþxÂZh¨¡¡\x001fZ#ZöÉr=\x0008\x000cºî~M­çZh[vô±\x0013Ú[%§\x001dºüÜD\x000fJÊÌ¼Ýï´3cT¡\x000fÂÂ\x0016K££Ä\x0007\x0007éòe8ÌCóxXï\x0007\x001dkèØ\x000fm¤4)
\x001c@ãò>\x001ag­®ï\x0015³á^(:F\x001e/ó2a\x0005¡¹YÈÓ\x000bì~Ðc+ª`ÿÒ½\x0017µÔß\x0007«Yú\x000c÷¢f\x0017Ïú
§®K|lüküç^n\x001a\x0010Ä\x0007vYèìíDÅä¡¯»ÙûîÐÞwÝö¶\#²èn9Ftð²#ÓBp×]Ûìn{]p*G¶t\x0013@C×·Ln\x000fÉm¯çÄã³ÉÜ>\x000e\x0007 lJ53(¹ëJ\x001f5äRß½¸5÷Ib8àäAÞF;\x00033oÂ}Öþã¡µÿØí\+i´v\x0018{Ó7Ì7s}ûöpq÷®\x0012O´Eh\x0002;Î¬Ö\ÏìanJ|ß:¹=\'½ÜÁIé{"­ÀÑzÀö\x001a4¬÷ë¤w}G=z­qð´A\x00193Üðû¹R\x0007æÆ=Ômn;tWz<L¸GÉ\x0018~oÇ¥ãw\x001dG\x001d\x0001\x001e?ü+nÊ\x000f7e/5f\x0018¶v\x001aÚ¯1>çEBRl;.î\x000f»ÛÚèF±P¨'	_ÍmVrxCR»ùÜÒlØÁÊ3zò¸Ð=_:f<\x0004¿Ç4ØûîÐÞ½\x001eUä*_âVp:%âÀ~9Êxx\x0006Æ
æ\x001e]&uÇéwãä)çzhú¸o\x000f¹»\x000fÁ\x001c7Ýñõò
>.ê\¼-­\x0004: ë$¹íë$\x00124Ìàr¿&â_ß}úíï'ïî¾}øºØ(/U
É\x001b/Å\x0015	4g\x001cÐAï"¸¾xyqòîòÇóë·Çp'0	wÙÌ\x001b
w>&\x001a*Wê0-Åð²\x0013\x0017ú6\x001ax½©x½éäuÔçXæ\x001ch¢³sè¯\x0016^túv±o¬yc7/B*áµ¬\x0008ï\x0015­dÒýØ×CÅë¡\x0017\x0017/Ãp´³2\x0012É%	Ñ_\x0010£háµ}c¯}¹hÚ\x0007VPÁ8F¼Ò\x0010\x0017Æ"5ð¦éTD<\x001ed,b+¯×ìý}
ÏïñÁ\x000cæÝe5àaVO\x0016É\x0007´\x00175\x00116°\x0012©ÇÝW\x001c´\x001a\x0002Ä~º¶#bt0ä¸ë"¶ÖW\x0001²rYÖ\x0001;ý!­v¶eÜÅ¤äÃeÕÄIÿÖÝÃÏ÷k¦·c~?¤bB3TÕ$},ÖÎÈ>OZ·.®ß¼º\àR]\x0012»ØI\x0017Z\x0011\x000e&þr\x0014- ;ëç·\x0003Oîe;ÞËíÀ\x001e²]8\x000eO\x0001IX\x001fï"^G<j\x0015gâ¬UÜl-÷±ôC)x(
À\x0016#×£
ëõ2î]\x0015VÙ2ò\x000bÁ\x0012l£'ÄU@ôâ²\x0013r¨L\x001f;ñ³ÀõøZ\x0004¬q"\x0018f\x0016ç\x00157 ûÉ\x0018@jHº\x0013\x0006\x0001[V
#¹3\x001e`\x000eRzl|8Úà|\x00149åB±ß
ÿpÿ­¯?Þ~¸;y}÷ðó×»?ÿºªðê^bBL!5\x0004^\x0014.Ø+úõÕù³×\x0017×?¾½xñzÉ/°£È\x0019ÁRj\x0007-^
\x001c*!­át¨u&ðtø0ç\x0010·Ò2gDKû¢ÆÖ\x0015X¤cI6¼ýÄ´s<­°YC©\x000c1í2­¼³Ns1´Ãëz\x001fÚT6u\x001aCJ½Z2\x001f\x0007­²\x0010|\x0019
ÝHkê=F\x001f»pÁdopánFk¥1|Ì]Ö-=óOqõw¿\x0016Æ4
¯Ûï\x001døÃ\x0001ðï\x001døý\x0001ðû.`ÇC#\x0005\x001a<\x0019Ë&VpÁÌ\x0019\x001d¼?\x001fðþü}\x001aØ¸"\x00195\x001cgø3]	7>ûíÿûZd"Î\x001fÞÿö_\x000f«"â>\x001aô}ø\x001dGù mÏá¨[ùìÕ[Ò8¿þáâzA)ñÇAoÂf|Oã§J÷[ ?n¡DG¿?ªdÔö
ÆöUú\x0006\x0010·\x0003o¥	\x0014\x0004OAié\x001föi¦y»÷\x001bÍcô
j¾o\x0010ás7Öð`¢d\x001e½õn¦\x0003±÷\x001bê7\x0008;ü\x0006!Ê*¢äA\x0005Ò>;Æ¬÷\x001beô
RÚa\x001f$¶ÐãgÍPÜ\x0007	o°ë>ÛÎ\x0007Ö;Dqü
§E\x0000þÙËWÐ».#­]ý\x0015¶ï\x0004z£\x0010%\x0003§åÉ
­¹Å/\x001e\x0015kû
cä¿B\x001dùö}\x0005R`à_Aü¥ÂJâÑÜHÓW0c³C¾\x0012Úþ\x0015L\x0014\x0005¡<V$iÎÄÅ)ÓÍ_¡^HfdÑm\x001f[¢ËÓ\x0006þ
"§âôLEïW°Õdìö\x0013	ONúÐBRÀ¯\x001d ÁK»+\x001cÍLÔ_áé\x001eAæwµcá¶{\x0016ìÎ\x001b\x0001
Ï~NÔVÝL=hï/ªK-÷]oü\x0006ÆÛñ>0¢¼F¤=ü²Aÿ"\x001aã+YF·Û×âAmÁ¡ª×hUÚ\x0004»÷ßâýïè[¨21u<\x0014)ø\x001eCzö§Û?ÿzûË§uJïÁp¾<jü\x001e,Em\x0003»¨.Ïg]|zÏüÿtþâõùó+Ø}Å~8`¹Ýc\x0014\x0011Y\x001eá\x0011ÞKä9í
ì©b?\x001czÞÆ\x0011MIãP\x001b~q¬\x0005; \x001f)xh#·Õí6«\x000c^àÞÔpj8\x0003¥äðO~&¨édO\x0015{ÚÆ·U96ssjq\x001f,D'íË«F ¯f×cu\x0001±ç,m?<UÚ\x0019Ñkpì¾Q]:k!î\x0003O5Iô(08 T4¸_N
Ó÷NÞHLç\x000c7ôEjÌ«Ý-'ãòé(¨Ú\x001eP\x00179¿N½qà¬æ¤ªóú½«9Ó3u\x0019\x0014XI¢\x0010\x001102\x0001A\x0017
\x000bÖEG\x0004
º\x0014Ã%'?½\x0017G=DN?áO?Ó\x0003ÒFê*R×CJ*\x000c\x000c\x001a½4\x0007ñ\x0015â\ô;üò0'\x0011u\x000b§+¶TCB/ÈH\£3
\x0013¨®Fu\x001d¨*j\x0004*)^\\x0007<KÊë$k\x0018\x0004mGõõ¾§Í¨Ùyã,-¡\x00119Ð±\x0014\x0013¯CE/JUëT¡pË
 \x0005-ÇK5\x000e+@ªÅ\x001dÁ¬`}:Øò¦QÃJÅ?iyô!N{òîîÓ×Õç©ásÊy\x0011.Ã\x0003×*mÿ9±âÿÚÅË·K#¯ÌÁ-EÀ¦\x0017Ø'ÑèA{æã
fâ©ogÛ¸\x0005\x0018¦ÀÐ\x000b\x000cJ|_:NWÉ3 \x001ax7^ý¿Ökâ¯ßï¢0Vç\x000blL\x0019X}\x0006aÜlè~ÝÂo»îéÇ\x000fÊ1tÝªR4â\\x000es}£²ßÐñº|ùöz©*Çê'\x0002N®\x0013êí\x0015\x0003\x001b\x00190&³¥^|/iÂ\x0015nìµoJ§Àw¯	Ü\x0001h\x00053\x0010/EÎ
Äz<×>v"[#ÑO\x000bg1ä4\x00076£O×lò\x001dÍ©µ\x0013ýé·ÿw"16
¤¼3¬éa·`ÌL¶nR]ÿ¸(ÈÃÈ®BvýÈ´ÛJù¬ÇÀ¡\x00089cùÉ\x0003­}|PÏ:d­+dúØËLW²ÎÌzèJIµAçW¨\x0008­d\x001eÅK2óxI\x00033hSª \x00125mg`ÐÜ2÷`8Úuq\x000cXÇóÍéc\x001d\x0007ÿðø\x001fw\x001f?®\x0001½´R#È**\x0016¨ x®ù3\x0001U\x0010üÃÍ¿]\]-À©.$n£6q<8#Vo)\x0008×ZZSÔ3Ê]Øãõ±+é´FlEý8e(/<ZQÍ\x0003\x001fkÍi\x0002O5øa­\x0005
>-[\x0016nÕÊJ¿3åÝö\x0003·¦\x0002¯Ô¦ZÁé\x001c\x0001^àók¸êE6&ÂLqm\x001f¸­Áí\x0006pHE´®,\x0012òëg¥²b÷zðiëÀ3¼ßB\x0011Ì%~	Ñ
x:	ò\x001fë[ÅïM¨«X©lZ\x001f.ëû_]\x00154)éò"\x000bDÞsîÔø\x0010OÇúµ	úúòõëãÈ^M½êFÆ­	åLÁËb¼¦!\x001e*÷bLEæo²Ç«cPå$iÞkóâö¸NÊ9H\x0019+ÎÁ#Ì\x000e§Ö¤2µ&»ª'Ïo?Þ}%òç·\x000f¿Ü~úúx»*îJQ\x001eiÄãì¦\x0011\x0012\x0010õB6ææäùùÕÅ[ú\x0002ÏÏ¯¿|{s~ü\x001b¸ê\x001b¸ß\x0000TàÈ1XDæöç\x00082?\x001b\x0016]ß`pè\x001b\x000c\x0011Nï7Ðè»á¹¥N<Èì ëf¤Àº¿VÕO@\x001f7®"ôZXá\x001a?àqÈ	]v\x0004ìEÿ7\x0018\x001f­ò7°~ë7ÀÐ­\x0016\x0004Kí¥vÃ\x0017X
6û¾A¬¿ÁÖUDÿÒÁ"ßôú#\x00031ÞRºðë]¬7ocDy\x0013@8\x0014¿L_]nÁéù\x0006\x0013ÿ¾ÁØðÔ½g%±à"æ½TP^½Öõ\x0015Æ.³ü\x0015.³þ(åw#ú
ÞR¶7«	AÍd\x000eû¿¯\x0005¿ùW0C\x0005\x0015¸a\x001aKÒ~fæ^Ï{¿Â4O_a¿ï¿áÔÛ¡\x001f­xùx\x0013\x000f{aæ-wþ+<Öwá@Ë\x001eÿµìÇ¢×÷w\x000f\x000fw'¿ý?'Ïî\x001e>¬ñi&Xd5©H*A¼¥/ÔYm\x0015Õ¾¾¼¸¾¾89?yvqýlÉ_æo0ª\x0001Ò7\x0008jó7 0«¤J©\x000cu¥¬¨¦9«6\x00046~\x0005=&ôè+ÐÇ­ß¡Ì÷¥¯@MæåéÒJy¹xt\x0012dëW\x0018RóW¨R»¾ñOuÞÊ¥l\x0015K;H\x000f°Mß!ÀÁ\x0011þAê\x001aÞ>ÜþåîáËªB¨£à µágÀ±ójF#ß^SWæqÌ2\x0005aê\x000eN£¥Ó&\x001aUÞ\x0010ï[çæTUÚ0mi{ÌiYý*òÃ1qú ¯\x0000qáe5§­8m\x000f'=®øáùÕóÏÎ\x001dÄÎùti\x0013ædÎ0¨¡£ÍÙ\x00083)ÞQhÎá)Ó/´\x000b¬æ\x001cs\x0001ÄéU9mE¹8ûñ ×l·p\x0000¯ç¬ìé{ì©ô\x0011giCBÎ8rîð»ÇÊ±Ã$ùÎÛ(ØÔËcÚð=£mÖÄ9é¹ÒsÛnOÇ$\x0015À9¼\x0002ÃòÌqLo\x000fêð\x000fgõñëÏ4ýk]Ä\x0012r¤KÕ!¾´-æÔ¼ö¥9íÿñvº~uC¿\x0011ë±µ²ÈYn¦ \x001b\x001dòój²8WâRÓ<\x001cÌÈÚw#KS\x0007
>¨
}{~gOñè\x000cúµÈc7~F¶ÐL¡,[Yiñ\x001e½$é\x001d©í\/\x000cÛ½0æs\x000cã0ÓÉ\x000fÈa±z¨\x0001Ù4E¦}È*xQY3^Kï\x001e«|~XÜ\x0007ÙU\x000b>ö"§ÓÈVÆ°"01çZ½2i§uaÆQ·ØnâÀ³ÐÈJÚ\x000bý µ¦æ&;c\x001c{1ädÑTÁ3w¿x)ü÷ÊÎÌtê±òôI,-\x0012[]+Úñòpc\x0002i²¢\x0017.éä®ô¿U.ëM\x000c	×W©ké\òTjâ(i
Ü£\x0010yZ\x0003X*u¹9yýjIY+SæLÍ2@\\x0003gôå\x00149-ÕîøÁÓÙ9uyÅ#!W¶L8qå\x0011åù_î>¡ïÇÛ_Öy?4{ÅsL¦Yï×zãý\x0010=íQ ãór\x000cy¯Î/\x0006ëÙTÌ¦\x0019ÝÉ0\x0006hí«Äc3J\x0002=È®BvÝÈAóÐwD\x001edRüÐx\x0010g väÉ8@BÎã\x0000{ãÑ+|yaÖIâõ0óðß\x0001íl\x0005M\x001b¤\x0013:ª¡¨Ö3o¾¡\x000eUÍè^ö0ûÙ÷3s\x0011µS\x0012&yçÄÊûÙ8Ö¼q\x0003ïPë.}\x0019CÈRr¨f4\x0018:}½}ÿb¦¤6vÒ\x0004Ã\x0012æy\x0011ìDè¨¹\x0007ÚÔÐý\x0007]rÜ\x0017Ùg\x0001Ú\x000c--\x0016NÍLLna.\x0015´cv\x000fÿ³{eò0\x0011ÿ÷ßþóÕ¯¿Þÿüøç\x0015ÐfÊr\x001aTàf\x000bü <\x0017=ÙÃ\x0004}òêõëË\x001fo^\x001c¥\x000eaJMåÚÝÔ\x0006Xl4$\x0007\x0019"4É\x0015h4úÌnH(\x0013tPþ\x001dPOnB¢îû¦6Yû
âÇ?åúøºáñ~e°a\x0014_+FÁiqðæª&§üâ½gKnr!v\x0013¹\x0016\x0012JMßtõ®#V$Ì\x00072e6IkUZ¦<Ï)*7 û2¶|Ô)ò4¶<\x000b\x0015}~üF\þ|Â$ä±tE6\x0001Ä<ÖæTkO9¼2´ë\uó6¯2¹üùÄdv\k¯{¡©v£4
$ q¾¥>r\x0018á ÓÌ!ÝÎLºù\x0013fúØÉ\x000cZD¨IJ\x000béµõ`F\x000ft\x0015±2xXûØÉµ=á¸43C¦E¹º\x0006tü_Ém;Â78£-.GÞ\x001eîVN vÉäa¤YEó'KjôI{5³ªå¼{sòÓõrY{áÜ,Ä[Ý,MÀ\x001eØñ\x000fävpW:]|tx3\x0014h\x000765°ùî-lFÙ\x0011A¾íd!ifD\x001eojI\x0004Õ>FÆU\3ã:îD\x0006³.$S\x0013uÎ7Óº\x0012vëâ?º\x001aÙAÈÅÔ£_\x0007á>N.Á_ï?Ü}\s	æ³"æ*Y\³ìõÀSCHÇf^¼¼y{ùìâê(±¯}/±Aï9'òØÈ 	\x0013.Ë"D=Óúß\x000cã\x000b\x000f!C5\x000c·ÍÈëÔµN¢hg²nf±rQoAö¹zÚ!,ZØLÚ_\x001eO^ß=þ|·FÈZYosqK
t`\x0011AÃú>%µ\VsòúâæÇëi­ÒZÕI\x000b Õé\x0000áaùõ<äVÍ}h+ÛÚ^ÛjþÈ¶¥Ø©él´îr]újÞPñ^^S\x0014×\x00047\x0014^`ï-¹\x0019\x0001\x0006\ãëþ
üCî¯à´òÏèûüðñöÓugpÌÕm9\x0018XÜ)\x0007ÝRë³\´úâ\x0015ú>?\¿|vxF"bðß?ñ$ÃÄ.ö\x0012\x001b5(ì2Æ/û?ó\x001a\x0016\x001f\x001a\x001a£\x0012GÛKìÝÝJpZZ'qi\x000f]Àqé\x0019§¸²qì¶1\x0006ÔJôX\x0002§Ö8©ØÄo´X¹¼\x0018cjç\x0001t"ûáÁ\x0004yü±54CHZ­\x0017Ë|\x001bÇª«ì\/2ºï¢p\x0000<øØÂPñÞbÇ\x001aâ ói\x000cc½&gâ kñöóã¾&HYý¦Dw\x000e/¾Ò~E	0\®Ò\x0016o_Ý,õ5\x0015æé,3dÎáR'4Í'â)ä\x001b;ã0ÃñX×òzàT\x0019>v\x0002SU@tìUäá#ø%äÎY¢}iÎØtaØCuÀµÌ1ú(#ãhZX©\x0017¡6q9éÖÈ\x001dvQ³ÆÈ\x00102áÎ4ELÂ§àO_sètùq­âb5\x0004Ú±V¯Ó6È+ûLqäñéMøåÛ\x001c@]^-O\x0003þû\x001aÿýï\x0002?h_ëá\x001fòôÛ/_nÉðïîï\x001eÿ§àãÇûOkN@¨T\x0005j\x000c`dåy-ÎÉû¿ysþ<Ó¿»¼¸ù\x0017<\x000co®._\x001eÔ\x001f#<¹6\x001béÔÎZNl\x0010½Ôø&õ´é{éÇN}¢'7g\x0003=\x0016¯ÈÕ²z\x001aËDúxrÇÏ2é¤·jJO\x0001×\x0016zmÄö´¶KiL¢ËýÖ°¶\x001eÿ[óÊ\x0019ü\x0014üÃ\x0019M)I\x001fînùîq#8º®\x0008\x001dÊk2).0óbæîs$½¸9:q©\x00085»Tß\x001f«?¬döJf:ÿ®?AÜu3ÑèÂ,-^xÑò1ü;g¾¬]å»~õ\x0006yå\Î\Á¦>Xk¸
'øèÙO¢ÈªÇA#¬\x001eu	>vV\x000fÉ[GÉ/V:w*§fÒ1­´cpi]ì£\x0005ÃmZ¦RJ\x0005v¶c§·\x001a\x0017|nø\x001e%\x001a©XSëJRçâëí§_VÝÝ$Ò»/\x0012/N\x0006×\x0008zÇôáDTçâíùËçKyæBì*b×K\x001ch\x001f\x0013+É áÊ`=_\x001fÕqy¨uÄz¬¾Î6¶ÐâlTYÂ\x000eC\x0019/B\x001dé¨:Ô:bp\x00151}ì#xö²8¡ª#[ä#$Íì£©j@ÖcY;j\x0002Æ²\x000b*¸ûxrþçû5{.áFÓE«\x0008È+ù\x0018t)ä@gÂ\x0015Ús?\\¿¸\ð5\x001cÊ
â²¬àøHòâöá\x0001ÿS÷w\x000f+gJA!¦RõÂðpÃP©~Ôñ¥äÅùõ5þ\x0017×\x000b&¶E\x001cbÊN=¯Ä>\x0006YW?ýòøÛýeå@\x000bÅä*\x0008¸\x000fX±ÃW^<\x001a~¿zùüæâÝR\x0005ßPã*êÇ\x0017îVÛB¢¤¢åâk\x0008ò\x0004³Ê\x001e	foN^Ü¼¼X(¹\x0005O\x000b\x0019&ò\x0003ò¡u$ûßûÏ¯\x000f·ÿ±*ü)\x00177 2ú¬xk°²¤Dã±'\x0008*¹x{}þo£Z¦üC
\x001dÆw)\x000eõ»T\x00134.Yn7$aoÎØiãe¤¸N3z\x0015ÍÐqzÊù³è`\x0003´ É>õÙÌYYÇ2ÓÇnf\x0018Âí\\x0010S\x0012JYb°$:ôñ=¸
ZOÞ|\x0008:î¦FJJRYÒè.y8oÝ(k©)}9¥¦ÏÝÔt\x000f\x0016hk¥v\x0007dv÷Ç.îµÌvlTÏÌô¹r0uÁ@*I«A¹ãÅhë¨½­¼ü¹Ú*C\x0011\x0012¦+12©Ä\x0011q/jw@í6PÓ\x0006äî\x0014K\x0015Äa,¯'\x0019Å½¨Ã\x0001uÿQm\x0019¼;¤Î)~4Æ`¦S¦:X]QÓçnj\x0016é#j¼\x0015§)G=¼Å\x001eÒ\Iíë\x0013>wS'Wz¿\x0012\x0015Èºö'\x0012â	2Æh¦Æ³¢¦Ï½Ô4\x0018ÈÆâR»Ä\x001dk:(ÞAÍ½euPÇ\x0003êþ;Æ¹Pj8Êq\x001d4×þ\x0005uä±~=ô4*ÐQuCÓ\x000bKt\a`óÍNÐA.Æ´B!v\x001duÊoÊ»MM³)Ë²Æp&?¼\x00105Wâ\x0006zÛ\x0005ÚTi\x0003?wÚ¡.\x0008í´$Ñ[â)d!?#îC\x000e¨Ó\x0006joò+¢.ê\x0018ÔÇ\x001bÑãzëé\x0017"ç_°\x0017\x0019WGÉw8/I0\x001dE«\x0008]½ãï+¡ë»<îN!·Ð\x0010u*¢\x0004\x0014(*îÒ
ÆÏ´:6S\x001bU¯\x000eúÜKMã­
4F+$Ç-¹\x000fÌN\x001bÑX¨¡mÿé\x0011HA¡8{Þ\x000fÁ)
*°0SóÓN\x001d\x000fL\x001d7:°ü?R'\x0019\x000f¿]b\x001dX)Ii\x0006[ù\x001fùs/t4ÅÎ\x0001<oD£\x0002WÑ\x0004Ø+` \x000e\x0005ÌáC~\x00137r#5:zílåø#%#tÑ#ö\x0007ÄýîR\x0004©ÊU¤eãXÆ¼â·Ø)\x000c@Êt@ÝJãÒ8#µgê¨Í@½çaÀ©ÚõûK\x0011$½¦îây\x0018M	é²:Âñ)+©ý\x0001µß@T)\x0001"êÄ\x0003\x0014ö2Ô"ç;,êã\x000e6\x001cw\x0011c\x0000\x0019\x0010\x00112hüÏñ!má¸þJC§XS§þ\x0018\x0000ÃA)Þ\x000e1qsÑr#ô\x001ev¶u²7î·s\x0019­\x0014Y¼<Ç\x001a
ZÛ'\x00187NÕë>wCG-XÆ=ÄõìæZjÚ©¡¾\x000cés/u2E}Üã\x000e\x0015cô@M
ÙûP×©Óü¹:9èH­Uîø&jÃo´\x0001£µ+diM;ì7 cxÅSO¨v\x0003\x0018F\x0001E½¢\x0018o¡I&JM»#\x0000prvÄbe\x001d-ëU\x0007gfd\x001d£ªïpúÜl©¨)\x000b
S?\x0010)Ä~
TäDö¡Æ¥WQÓçnj\x001aÝl\x000b5\x0015\x001eCÊhÚÎ¨¨¶Rªs\x001eùs/µF'©tÚP?)×9"?ÏW\x000biÅPuÔ¾¾\x0010óç^j¼òÊs\x0011I\x0002\x001a\x0019c\x0007©q{\x001emr[I\x001dêû%î¦6\x0013Ú\x001fK	2\x0018©l\x0006V' \x0017Î<\x0008u¤?÷"S1-#7HöÄ0²cwÆ\x0008ïsàO\x0015ºäÏÔZÉ\x001a\x001c\x000eïFmsíRégCSÿéfê\x0000uk\x0008þá,V\x001dY?}¼{üúðyEå%F\x0018|Ûr¹P\x000f@ÔÔsÊ9®ñAÿ§«·×¯^Î#Û2LÒ
'5þáÌÂÏï>­,ÀsY±ê5nc\x001a}\x0018DZU¯_¼¤j#¤á\x0007D:\x000e?hB\x0005H\kNiâº\x0014 WÂÿE\x0001Ãu¬ X!ê\x001eV§R~oË2jÕÄñÏ,IïKîÌúôéà\x000e\x001e9\x001ez4É·ö\x0005\x0011ËÊÓ6\x0008O¥èX$?é¶YöåÜ÷;¶æ³©öTOw\x0011Åº$CPu±¢~n
?	=»{Ú \x0017r^77\
\x001fxB.ì0ÈuÏT;¯6õ{ô}ªö\x001fÈ\x0019Ê®çí=yw÷ðóó~ÿ2.çDLÖ\x000eSÝ\x0003PFôé\x0003øüÅëw\x0017×?.\x001c½9¸\x0019³8õ\x0008J\x0004ËJ\x0008Iz£ÍüÕ¶S\x000fáiá,Ñi\x001bh,¿7qº ÂAúg\x0002ÀÜ}¶
3é¬nÀÄ_&Ã]Ý}9yþpûég\x001aÁÀ«*\x0017­/	YÊ\x001eú2\x0016ÂMñN_¿üp"÷\x0019bý?\x000fî³~`þÞ<>üt÷å\x0013]\x000cÀ^¦>{öø\x001fÔJ\*h\x001a\x000c[ÐÛx>"
qÇ+\x0016Î,)¤ù>Ïnþ\x001a\x0002ÞÜ\ütñæå\\x0005¢þÃÝmøøë\x001d\x0015@ÑOùßÜ=üzÿñãí×9hBÊñ#\x0001	C\x001c¤Þq	gí\x0008ÄÅõëË««ó·³fPxÃå±\x001cçå\x000fg¤"8èâd|µ	¥G©Þ\x0000bÊjà\x0008+\x000cOL\x0014SeÐ¿É¶+*\x001d¹<L¹Hk5æ1ÕÈ\x0015sÛiæò#
ý\<x¹òàÕ\EwÌ¥éÉ5c9\x0012~`sù~¬Xý±ágÌ^c\x001a~ÆÄ\°+Ç>.­ª>®\x0007\hF¿cîÜÏ`ÆD1X\x0016²í\x0004cßKÀ´i\x0000£qYø\x000eÔ\x000cF\x001d(l1ßÿKj¨\x0016\x0018}\\x000fç*`\x001cªÌe³?¹t\x0016ìär5káÂ³[¸´¦\x000c\x0016\x0006éØ¿#©\x001cu
\x0016[æ\x0019x\x0004fiµe0P|¨i¡}\¦^ú¦eéclQ7éT¤Q¹H|
¶aO\x001e½e=úµ`$¼d³\x0015Ê/	Þ¨yOn\x0000¡\x0002£E±\x001aÌªá\x0014ÃÕÛ3å\x0019Ì\x0003t©Àèãz0Êzða¡òW\x0006S²Ä¢ÙpX\x0000Ô`Ð\x0004æ²ìW\x0006s$½]À4\x0008XN7öÙú´-÷$®¦òbBð¹=ÀtîÀ"°TÿOi99 `Q·¹,\x0017J`6ë\x00170Í?äL{7X¨Á\x001a~Jj\x0004¤ZÁ¨Ë§Ô¾ZÎ«
`±\x0001,\x001cy ËE\x0017+\x0017L\x0016ùþ\x000bÉ¥Ë¥\x0006.ã]é§%)6Ï³`Ø`ý{ÒkWy®4ül5\x0017M«)X ¨n)c¹È÷$z\x001eý\x001eTÓ\x000bmá2¶Ì I{Î`yðÏ\x000e`±\x0006kù!ñt³\x0002â©\x0002¦UØá¬
ßrT çpjÆ\x001fR&K³½Rÿ5IÿÙ)Wjp]5-f.*\x000bÈXÎÊÉ\x001abÿ~ÄuZc5¬/jÉ\x0008£½bÙÑ\x001a9YÃ-:d3
w\x0011\x001eUÃú¢V9\x0006Ë\x0012F|²Æ
`©\x0006kpÄðÏ%wJ\x0016ËU\x0007\x0019,wÐ\x00160Ó¿#­\×#Y
¦Ë°5\x0006+\è«ÿ\x000c¾ZbÁ7,1.5»ú\x0001L¡ri 
ëë %Ðâë¨hK¾7dY_Á4¸\x0014=ë\x000b\IÕ\x000fæÂ?ÁÔZoï\x001e\x001ePÆÓÙ&ål\x0019²`0ìÐ\x0014½ÑÕò´L\x0002³Î=e±·\x0017××*Æ\x0001Q4S¢hZHJ \x0011\x0010\x0014¥\x0006)ÿ¥cS¢ïV \x0014¦@)4\x0000iÖÍÍ@ï\x001eôñaàyÊ>\x0002¤MõÑÇ\x0006"ãäP\x0000ßV2Q®ÊHêÉèì\x00081i1\x0012i(xÑ¤\ÒEDJÝKÖ2w"6\x0013qR\()Þ@4\x001c\x0004R\x0014\x0005	<¡!Y]!YÝdøÅ´\x001c2R\x000cì÷å³È×D¾\x0008n\x0005lÖ|!g!	N6?åV\x001d\x0003
5Ph\x0003r¥,\x0017ç!X!zÊs9J\x00045\x00114\x0011ùòüCDc\x0008Zïò£©Ô³B¬b\x0013\x0012\x0014!\x0010D²ÓF$©\(FH0úOù\x001a©ü§£HÔ ã3N¹t=#Q}F2.tüp` Fjúá¨Ñ³\x0018I\x001cI¹g¨\x0010\x0005ÝqnC}$AÛä­Ûê"x)\x001cIÆu¬$Õ±
±éØNJ¼8í<§¸3ñekô\x0001Ì\x0011¤\x0014«\x0013 Å\x0013ÀÓé|ÿÓë\x001cIÁs\x0003=©V$ËÄ4"¹³8ºà'ïn?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=}¶?0_\x0000ã%À\x0017¹\x00043^ù"àÆKp_ä\x0012Âx	á\x000b[\x0002î\x001eç¡ì\x0010¾:º|kµÒ=ÝåTªÁ\x0006 \x000c!°¿ç¼Óû¯C úôèr_ÓÛ\x0011ª6\x0015ªéaõ\x0006sÊ#Õ[KëäPåtìàâ\x0010MYÎ
X¡K®4äqh'åM >'Y®h]È¬Ö9\\x0015ÕuÔ´³\x0006Ì\x0015½ÞP{æ\x000e\x0006åêòëûrÖP±.VêýÅ\x001a,¿\x0002\x0003êÜ\x0005>ÕÚ\x0003Aÿù¨ÛA\x000eÛÓE?è8`û6¦ós\x000e!jË^¡÷ËöÁ\x0007I1´\x000cûÒóòîêþ>9&Cyîí\x000f7w³\x0015YÔ[0û¨ÊÎ5tü²»¹ÃÁ4qò³/G2\x0014å^¼8½_\x0015p?\x0006÷KÀiï\x000c\x001e|gB._JØj%ìP«ÞçÜÄ;Ý\x0017ÞÝß=\x0005y{wÿËÝüC°éæàsjC\x0012Ç1÷DàÌ\x0006ÌS ÷^\x001cÞ%ÿ¬ÇÛ×¯^\x001fºB|¨úv\x000b;|Yì8fÇ/ÝÙÍÅnÇìö`§yO;nU£üÍ¦û½¥6µ>ÈÅÉÌçjÿdzbØï}pÝ\x0013wü\x0002\x000cc`è\x0005Ö>Ï@JÀÞRÏ¬\x0001Ìp6ëxà\x0005¡\x0011ØÍ\x0017\x0000ìÆÀîó\x0005þ ÁíØ\x001bploÞÜ_¥+ÊÃýwså\x001c=%Ï1I\x0003Ç6gÑiqG\x0002ÄÃ1ªËÓt3yùõ¾
À11áK 6cbó\x0019\x0013S·ù\x001dEav&pdÀ«Oæ_¯Cí5q(\x0019¥ë6\x001c¢ýàÛ\x001blþû§ïÞ\x001d:\x0006wÔÙ\x0019VñyãûÝh\x001fGÓÞmîûu¶\x000eIZ\x000bùFã\x001c¥£\x000f:\x0004ótdVrC«ØïN.ÿ²§ac\ìÃUÞ\x001c;¾¹aÂ	áj×@¸\x0007.`3qµ­.\x0006CN5kâE:?\ß6í\x000eKc\x0007I ´awFÞ\x001dJï¿mwÇt0_]<±=ò\x0002\x0000Ç\x000b\x0000\¸\x00026\x001fUQåz) ¯/h°5Í\x000bÀj\x0001¸t\x0001Ör\x000fêÜ\x0016]¾»\x0007mxë\x0004'wúÌ\x0015$\x000e»Vs¨B§êÁÜ¾övîwN\x0019ì\x0005K\x0013º²>Gk$ó\\x001dxØ¡:AêU{±Ã\x0017X35}°^k¾\x0004»XæDPÏÆ\x0007óXÅÅ°ZUU´Îðk³§¡#6\x0007M­XÊpàL¶°Ö» s\x001bx\x0005yv8Iv(ý\x001b$k\x0001D²¸ßÿAKÃ¯vô)zïÍ}ú§¯ÿ¾¹ýjJÅ®À»6\x001ay55Ô8ïZw`#\x000c5/Ï.^½9Ù×Hj\x000ca\x000c¡Ù;E\x001dA9ÐH¼ye79£¨Éàbf¯v­¡\x0012køöúù~×âyDKgtÕ\x0003NJÛÃêìíÙ«.\x001esÚ1§ýì8?(W;CÏÓ\x000føòÍPèµy8zy÷ãæþÓ\C\x0011Áã>R³vÌZ­p\x001cÏÙîó7CQØÉû£¯¿>¹Ü3\x0010và6º:nÏÓ\x000fè¸%n2n®o¾ÙüÊmg¹\x0018kjóó\x0004ûÚÅò:qÌÚ»³ó£oNþLslØü¸ùøéþªübÀößßýíï¿^ÿû(ñã\x0015W\x001e<ÛZûªÚî_ÿïWù\x001fxö,$)*ÌõIm%\x0017y\x0008ô\x0007#-h"ÁnÑæW'_½\x001aª\x000c^\x001d¨5ðßÿóoðáA¨¶Õ¯î\x001e~\x001böê\x000c@\x001e\x001e÷Æ(Ðù1*XùÛÛ AÁ\x001e¾mùß«×ïÿ²w¿úí¹ÊÖ6ÿ`ð§ë¿~là\x001dz©'`ãò¤
\x0002vÌ»;¶àÊ\x000bþÞ}³/Ø<b
cÖÐÉª!×«'Vo³A\x0008Öq¾\x0004ë÷
·]\x0003¦\x001d÷ÍiÁ¥\x0001÷Ã8µK	Ä.ãb\x001eK¸Á®\x000b\x0015.tâ\x001a\x000bXÓqRá8Ó&éêL\x000bj·«o/mµmuç¾\x0005~÷¦Ô4qmnâN¸»]¬;q¡Ú\x000bÐ¹\x0017´w¹å?é*kÍ5É_`\´~\x001dÜJºÐ)]|\x0017Ç¸ÎçHqÂÕ9Àpín3Ã.Ü!OmóÖ>ÏÍ«Æ>Bþ\x0004LNî?m®?¦KåÕÑw×ÿ¸\x001eººÌ¶ }\x000cÒ´drgÈÊbîÄNývG°UÔÉ789{n§Gß}w¶¯Ë\x001eÆô°Þ\x0004ÍÓË\x000c:ÀÜ\x0006<8¬©Ë¡-Ò\x0001oÆðf\x0019<\x0005Sh\x0016\x0003ÁSO\x000c\x000f>÷Iôé2¿.½\x001bÓ»ô*æIòÿäÞ'Áé¨Xöé\x001fÙç\x0005uÒ1}XFomFOî\.
I×;Nµ>ÝÖßKÑã\x0018=.\x0014<
fç=\x001fbÎyLÛFåä$øÃþR;½®õÍ2clð9U*íè©\x001b!á'!Â×»}6âÛ
ß.Ä§Á	È{Ç¯\x001aãm\x001f­^W_êêÐê§ÖP§{;àGÍÉ_!}\îkÒ{ï.ø¾Â÷\x000b¥\x000fê\x0018Xúé¦À.Lä\x001c+þn[×ø#Ï¬Z(}4ÇYïD§rNP\x0012¾\x000eì+·®ì¡:¸°ðàÒ(ö!¬dOs6yë\x0004ÍæF\x0011¬_{
\x000b]äDfÉSßS¾\x0012GdO]ùÝ6KÙ±bÇ¥¢Wäè=K^¹"ùuu\x000eT*\x0013\x0016ªLCÃ~2=õ÷\x000eo@+»P©LX¨2:zÇ|V:S):¡\x0018_ç|Ù\x0015ñ+	\x000bU&
T¬t>V|l ÌîÈëøXi\x001d\ªuÈ­)'×dïýèä®ëí`urqáÉMN\x0002
\x001cð©Ñ¯Îø\x0012*TI}®K_\\xrÑ¹ü\x000cè#\x0016áCNkOøqw´ò"|=¾·P®âÝþBr\x0012\v6\x00038\x001aÑ2ø\x000b.÷%OMñÛ\x001d~»ß·ÉÎ²³y$tr\x0003«N\x001f9\x0014²iY@\x001c'ùå\x001fpl!a\x001d½¹¦|âOs÷
DòÍ²Æ·ÇYêÎ8xÚÒ½9£Tâ}Ï\x000e#\\x0018ãÂgc\ìÅ5S(\x0013.\x0006¾y[\x00175\x0016~`WÏç­¶s\x001cEÆ:­£$\x0017Ñâ1Øk%zÐïNoGV¸³\x0015\x001b\x0013üòáæ×Ù¸"²ÉWy<dÂU%ÈO·²\x0003¡¼£WÏÏ÷½QXqÌ¬ÚÓô¸U\x0004¡
òz¢q\x0015V3f5}¬ Í~\x0013«ãh¹\x001cÏÕnwâo\x001f¨\x001dÚNPz+Ñüfåì4
+ØUXÝÕ}ÆBõcPß	C=w~æ+JÀ\x001a	èksÐÍ\x001aÇ¬±W¨Æ­\x000c¬#ùZ|Nm\x000fZÝ¹ ºVUºJGÌ£`éóÛÜø?X\x0013Êùw\x001f¡æÂB\x0005\x000bï^ÕVÕj7\x0000MØÍ{ÀØ¢\x0001¼=ti
[i\x0000Ý­\x0002t.Ï{o\x0019V\x001b]öÀ\x001a6@WZ@wª\x0001*µqûLc1ÉógH2³+À
6ôn\x0003%oz*\x001d4÷¬áthÝÅsa+¥;VF\x001eû5èÜ\x00113I\x001bq'ÉêU¬Ö8&Û×èfØûm\x0013l<Vù¡\x0017É\x0002ì°î­ô\x0016tê-\x001at¡ù-òAyÏÚ\x0002»;Õ­\x000f¶R]Ð§º0Òì³¬ºÈ8ä\x0007"+õ4	6ì¶\x0001ï­\x001c-èó´0xÌ	\x0004+7\î\x001eQ`Wa­Ô,tªY\x0010Ä^ar\x0001¨Ø{Ø\x0005 Dsí\x000e>ébÅêxaçñR4ÂYÏ£ \x000c(O¨~w¼t\x001fkuº°÷t)	3¥= ÅÖ\x0002ZQ\x0005A­¡·°ºÂ`ß\x001d\x0006£õyü14pÅdÁj\x0017ØÖâÐ\x000cu9lµc±oÇb¤9¬a\x0003Ý\x0001V\x0017Ö5\x000e\x0017V\x0016û,-R\x0007öcI®!k-\x0015l\x0010V<\x0014«\x000bkªÓeúN\x0017\x0006çÅx%½*@¢bãÁäÙ°Õñ2}Çë­c8N£juf9fÇ;]\x0018sB¥¬Zö¸(»g	mØ\x001c\x00065ªùûÓÃ?6s&(!\x0004ép\x0019àw--y¶úð\x0015Lwò4©\x0019.Rütt­%{;Ò DgáA\x0005;ÔI]\x000f©uAÞ
CÐ,S7Üø©swð[\x001fi\x0018.Ò(7!\x0011Dåì-%µþð½à)N­ÇWù\x0007uF8ýêê~þ¥Ë\x0017w äY#rM®Ë^\x0007v\x0013N¿:½<p¶\x001aÆÔ°:\x001c\x0007¾*¦\x0018G$«Ýk¿: q\x000c\x000b õ0\x0003)ß\x0015 \x000f¥MI³Ý\x001f;l Vq72Úq?Ãï6?ü|57sUÉ´dB6¹Z$ð\x001c<\x0002>\x000e7Ìy>IÀ2Wãnúd´Õ´ð&Z²g%ëÚåMÃÃ\x001c?86ÙëÆ¸®\x001b×\x001bNR¾È¸Z.8
\x000eú5Oã~HÎbõrý¼G\x001cÏ)-æE\x0014\x0003\x0007é\x0010Òn\x0008&;pZo´ß\x0017P,S5\x000e¶ÿ	ß¸ùéæÃÇ!ð±\x001d\x0002òfC0UAV¨(7\x000fÿüêOwÿúÿ?%Ñ?{æCt
ò0£á!:Ç;Ò\x001dÌg÷6
3ÄßÿÛW¢þºo&\x0001'ôÓ½e.\x0015hZ³NPã]MÓIì1½>'P_¡c÷ãð\7gúì\x001a»9ÞÈ3§ËµÅ3ävk\x0004ú8µ´\x001b4\x001dm:Am\x0004ª»\x001a@uÌ99éËs1q\x0002¥¢µ@y¶Eß\x0016MÆ æ-Î\x0010]\x001c\x0007ÐO\x0002ëoºAÓµ[\x0000:äµ&Pcm\x0018Tä¹;\x0018|\x0001f²ÙÚ	òLfD/àÈ§[\x0006ýÑy\x001b;`ú\x0000¹\x000e\x0012N\ïÄË\x0010>yFßcr\x000eò°^0\x0014\x001fÈ \x0001\x001e\x0007´ºAA\x0006Ýýácn¯Ié¼!§ÉÒ\x0007>JêD×\x0002å±1] èMÎz¡Öò6_`K²õÔîqü½3í!è5J$'¹éã\x000c6_V²ÑÒëñÀéò8à¨½\x000bë}ø´dèµI¨B\x000e
\x0012è\x0010\x0018 P°¹Þv\x0000]ïÌ'-\x0007½6	b\x0014wÄ¦\x001bË:\x0014\x0012PûøÝ
,\x0012ôZ%4ü<D[Ú¥OOñ;Þ¢ëé&tÔ'ÐtØzB\x00089\x0012\x0004ª\x0014oQ\x0013\x001f'6t¦Í\x000e½V@ÙzÕÇh²î,Pãôj[Tf3}þ É$a¯YâÇµa¤Pó]IEdCïðq°²ÿ®ôýá¶ô¡Ó'Q1_@³/:Ûz®IMKñ\x000b\x0006\x0016°n\x0006ÖÍgïç"ÔäAu¢ÚôÝ}\x0016«×@`\x0010k°Ì\x001a<<ºØ÷ßîÎÏtÃ£?÷ñ"\x0007Òh\x001b\ì\x0005\x0014!\x0016_½;\x001e4k7îï¯
ìõ½ÿ\x00108ì7ôÜÐÈ\x000cÂ©\x001b=A\x001a\x001d²/
ÔuH \x0006je]TÔþqÀoDzB£2è§û{U¬Û5=¬ï'04þfÔüØH\x000fÚ«VPNÜ	N¿ÏBM»?GØ\x0013©õy·¢ÂÇaß\x0005¬e ^\x001f«¦\x001b\x0014ÎÔ;Ì2k\x001e\x0001@~×ãV\x0005\x000bXyr'+©ª\x0001ÕÊÏÂ	5qgTXiµ¢æù_Ý¨:?	Q\x0017\x0018Ã
ÚÛ\x0002³ÚwÔVV\x001e÷üE°Ú¬_mV¯Èàó¼ç¨l\x0001
ðNH\x0017°GôVbsÿáß?\x000e±ª#Y¼o®?~¼º¹kaMÖ ð¥Ud\x000cò¶Eo\x000bìÄk\x0005ûæìíÛÓó×\x0004;ÝÄj\x0004«Õ\x0010EWÝ´AÛcpy38®
\x0007´â\x001cBQ Y´ÿq÷Ïÿõÿ Ñqñù
ó]âÙüÔ@jh:AøG®\x0006\x0004TN´6OØXúÙÉËýEû5'dæ\x001f<³ùÀï)ïîáf>7Òtª\x0001\+ªÂ\x001c|¯´eù´é\x0007\x000c\x0019÷¸ÎO+ïèï¾?ß»e\x0005NWàÔâ\x0015P\x001dÄv\x0005C«\x0015\x0010s- -Á\x001c¸÷-AWKÐËÀÕty	.¯ PVpÀ¡ì[\x0001T+Å+HoÈ@¤\x0015(\x000e.\x00025}-ûhõÕ\x0012pé\x0012¨á\x0010f®äyúÿç\x0006\x001ai	Þ¯¾\x0004S-Á,^B:Ì÷\x0011*H(GÁ?.dYº\x0004[-Á.^æF\x001ai	Ê³}\x0002Om§ó\x0012ì!oµo	®Z[º\x0004-ed\x000b\NÍ\x0007pF^õDaûÒ%øj	~ñ\x0012èíuª·ôA%hYBÚI«/!TK\x0008à\N\x001dIQH³¶%ð\x0008p\x0000sÈ=ï[AeÝbÓ¬\x0002æ3ªêSÇY\x001fYgø0'§mõ@Ú8o\x001a\x0006tyø\x0018[gÈþÖÅ0\x001còàzWñag\x0015\x001f®ÂT^a/I®û´µvÓ\x0007åN«FÎÃsEÁì¦ÛÉOÉ9½ºýtßà¢\x0003~ùÓ\x0018Ó¥5û\x0017ûpG0ñq]å¦\x000bÊËä¢^¼ÛÛ$¶k­Çàô\x000bÈÓmÅçÝC\x001d\x0013òÕv\x000f{F\x000eÃáÈ`\x001b9Ôä°\x001c¨-EV?ôÚ\x001aØ§sÜç8Y4uøé¥\x001ckr\"ótëfÅié-ýi\x001f9\x0006óT\x0006K\x001b¸©ÁÍ"[\x001c85Ôg;Vù.>NÔ_@nkr»Dä6æÞóéRDÎäÑi	{C\x0017frW»%2\x000fÇ$\x0007Cu\x0012Ì­b#åÝ\x0013¡û6r_ûE»³\x001f)Î\x0014s¿<Ú-
\x000fvÍÝ\x0012jò%ê\x001c¨É\x0019GÈ´\x001d\x001aÈ\x001dksø	ª
;ÖØq^ñy\x000fÅrlî¶E·\ÏÜé\x0014\x001c\x000e4ªÈ9½§<Ýh}¶4ñÉ±\x0015BÑåOÄÌZÉkû	ì§Ü¤B\lÈC§»\x0015O'Ôæ\x0013OÊ£4ü\x0012¤¸/\x001e`´¼\x0004¡;\x0010ÐF^OXb>\x001d$Ò\x000cnx\x000c ¢-OXK\x0006\x0017×æ\x0013OîªÙ|BÌ\x001dÙ\x0001Ó}Ûñ;_óxÖÖ\x0013XO«
Í\x0012\x0018À«Å±WÍ\x001b)«hÕ]^[OXb=ÿX×Æ\x0013\x0018OºÕå\x0017{Mý×B¨±ãã¶Iýä¡ÞåaÉ.w+JèYåÂÓt>\x001dÊùè¼¶Ä~9Ó#\x001bÊ/ù·¯8ÌL¤Í\x0002Os)é®¯Ð×lþ\x0013YÚ\x0010¹$1`Ä\x000bý\x0000£å\x001cã½? ö|s¾<K?zØÔÄæó'¶5±ýü]Mì>b_\x0013ûÏ8ÔÄáó'5qì%¶C\x0018é-)\x0003;ÎW!à\x0003¶¥\x0005Øª
8ýåç\x000e\x000c50t\x0002£×Ç8T²\x000eÅÌ0ô¸ÈÄÑÀ\x0001Ç£¸¶\x001f¶×~ 5\x0013ÃLlµ¤\x001bÃïëéÏ{\x001dw\x0012×öÃöÚ\x000fH7ü5t:æ¤{Í®Õ$\[\x000fÛk=¨¥nNµ0\x0000_­h OæU¨\x000fÄ+kãa{\x0007%áçg6Cå\x0017\Ï".¨\x0005\x001dÖÚ\x0011µí°½¶#}üÜ\x00103\x0018Ä¡c®\x0017±Ùs³é(®¤mm;l¯íøãD\\x000eÛk:(¨§3/Ó5|è8\x000b!\x001dºC/¯-À®6\x001d®×tüa\x0012vµ"výØäÆÕI\x0011GÈ]\x001d:é{VÄ1®´]­]¯"6JBICïÄ\x000b\x000cC1v\x0013\x001d§:kUìzU±	ß´=ß®õ[âP-i\x0013q­]¯.þ\x0003keìzñ\x001fH\+c×«ÿ8b_+7ß«Ü0)·\Ïg('ÆrÅ)BM´"\x0015MÀº\x0006ÖÝ"6J88ò\3c=\x0018\x0011ñZ^¯=yßíÉçG·ìÉ;ªJ\x0019DNüb£VRÇ¾6 ¾×\x0000Ç¼©ãÚ\x0019ÙÄnµM\\x000fßm>ÎÃ)	Øp\x0002K\x0002örvkù\x0014¾6\x001f¾Û|Øaz\x0019\x0011à)!0W©È\x0018\x000e\x0015z7\x0011×æÃwÄ5LKL¿Á¡&w
xb^i'qm>|·ùP\x001f31Á\x001dó\x0005ÚÊ¦°6®%âÚzø^ë¶Bî³\x0015Ð\x0019nG«ÿU"ö-Ä¡¶\x001e¡ÛzxÏ®1:Di¥b¸j=mµnK¡¶\x001e¡×z.F\x00161MÝå\x0018\x0005\x000f4JÄþq¢NâÚznë<xÇ"Zn¤\x0006YQXs¨½	¸6\x001e¡ûöá´\x001c»tÖr\x0007a i#¬(\x0012ûZ»¸Vm¡Wµ(Ø2ÜdùÜ%àµd\«¶Ð\x001d¦°C5[&VÒ¼
tÆJÄ\x0016Jºi	hnzÏ\x001eäjÌt+uáH7êÀÑ+µt_(eò+³MÙ§N²ÿæ>ýã×ßÜ4fe\ø\x001eAó^tê¸dH=ßûæòìâÅÙóýïx]\ú\x0001Û«%ØÜÒ?èÄMe+\x0019Ûóû#ýz=l]aëeØyWk
 sVcr¹®`ª÷x?6TØ°\x0004[åé	|9N=2R\x001aúPÒT\x001b¶VaM¹\x0013\x0004\x0006\x0015é]nx<³;ÖÜñ\x000báÖÕ¡¤¿ü¼¹?(?ôsT£\x000c5WFY]}<º¸{\x0018ºOÎmý¡"\x0015\x001c\x00124Ý\x00001rß\x0007°O S\x000bÊ×ï÷v Ü\x0012.*éÞõ"\x0007²3ÜP'Zªú\x001dÄìK¹äÁFf_1ûnf£
ôÍõHÉ¶ç"ÚÁaÈÐxè}²\x0011:TÐ¡\x001f\x001aJ?½\x0018\x001c²¡(u#ëI:VÐ±\x001fÚp!¸J'rÒr\x0011°ÔV«±ñ6æÑ-+1\x0007ÕÍlf&Ñð\x0010ÜdV=¦>UÚ2\x001fºR\x001c¡[sÐ¼\x0008ê\x00049@ãP"2@{I;Wá)'¤\x0001\x001a*hè¦¢& ¢\x000bütrÎ[Z?Y¨<\x001f\x001a+hì¦Òdö6\x000f*\x0005D%¹Ï¬\x0005m*h³\x0000çv\x0010tÈsö´hix<È©ÙVÌ¶ÙÓ]ËsÉeàÞRé.\x0006â êC\x000fðÐ9\x000cýæÐâv$§ßÖÐx#Uêñ\x0000ðnèÊ\x001e~{Hí°r¾°¦g	í¡#Û¡\x000fV85BWö0ôÛÃà£vë\x00108ÐÎK&?ªÇâ»¡+{\x0018úí!õr\x0001ñJun\x000fèµl\x000fÇC\x0013z¡ce\x0010c¿A$bsµGj\x001e¦DÅ¶âãÑðæÕ +\x0018û]i[\x0019\x0018\x001aç²+Í£µ\x0012t<T\x0016Ô\x0008]\x0019ÄØm\x0010ÿ\x000fìz$oNóC\x0005M	ºT\ÏõAÝ\x00061jë9l£)ÎæPr(\x0005ÉqZ\x000fº2±Û &I{~M]à./4:%mí-	æCW\x00161v[Ä¨¼â.úü=`hRªÖÓÓ±²±ß"Fz.ô\\x0010é¥p)\x0000HAäÓý+æCW\x00161ö[Drüó\x001b§vÑÈ
ÑîE®0«]këájK?é¾Ýêâ ¦"_\x0005Ê\x0005¾(\x001e*èhµ1¥³X\x000fÝ»ÌLÞ(\x0010¤{4Ò\x0013hìCo­ÊoWæI\x0001öËúñÒE17\x0014ðSnd6"5\x00148ÔW¸õÎ¸ËìÜýbÓ\x0001ånØÑÚ\x001cÁAj0'\x0011C}Q[
åÎvþí¢©>,Ç¯qèÚEÎiwÔp~½]>~ÉØ/b«ïÜ9?v[[iC4¼åÇçaF\x0004ËûP#ÊfîÍ\x000ew¯¼Côü\x000e6´ÉÏ\x0005é·*q\x0003ÝzQ³ðHE<P9\x001e¿Ð¸ÈU\x0014NR*¨ëÇbB#)§ÒmÓªd:ôpk¿{ø±÷Çí5 ÀñÊä¡\x0000wIÊQÒ\x0015¼ì>ýiXÀð\x0016ùöÉÇH^«×á¾¸uTÓZó\x000fò´Ö¼\x000cÐxûëü=¤Gîrx^YÒGIß¼ÿ5ê¤?:¹Ø7ßl\x00152ö#ÛÀ#©\x00048p*i\x001eJ5\x0001ó-Ä¦"6ýÄ\x000e©\x0007ÂL}\x001c#s|¨)O\x0013²­m72µ)É×ãd1£ S½xF¶ê` ¢\x0005ÙUÈ®\x001bê|sÅò¨¸â	áä®ÝéÊ¿ÖÆð\x0015²ïG¦hZ2µDvÑ@ý\x0014\x0006äp¨ÍT\x0013q¨C7qº·³Wi3p®\x000b*	Ð\±§µÝAä\x000fI¹
Õ÷Û@`Òo'e$\x001dýë«{êLöüîºå\x001dü\Æ\x000e\x000cÎ\x000fJú;Øsx\x0018÷ÝÙé%õ%{þúìµgþXóÇeü`\x001cO}\x0000LOä&6rkC´\x0004ßÁªâç¹\x001aÝüÚ"¿å$?\x000bé\x0002:èÀÀFÉE¢\x0001B3¿®ùõB~ê×{f¸´¸i®\x0003~"A§èWÜÌ\x000f5?,â§¦\x001cY¤v8²L\x0001Ïì¦Ë»²ü±æÇ¥üÈ\x000f'ÔOúåb\x0006\x001a;Vå75¿YÈï
7Ë\x0005zËÌ3%h¼a~}(\x0001ºßÖüvÙþW4jåî\x001dù£\x0013ùÃ¡ÛF\x000f¿«ùÝBýiþ\x001c¼ôa+û3<9=<mM|_ãûæK\x0019ó*ÈT  æ×Ot1kæ¯Í/.4¿&Ù\x001cFJ¬×Ür\x0008Xý\x001b\x0006¾¿6¿¸ÐüRu,×ap2\x0005@SËËÌ\x001f\x0018«ÙÊojók\x0016_\x001b\x0003¿\x000eyàÙÓDzâç\x001ceûÄ,ÃfþÚüæ÷ç¯Í¯Yf~ÿxþPë°PÿP×\x000bc£Ì\x0000'=\x0014Ó¢\x000eå\x000fuí*XÆ{\x001bA}	ÁËð\x0012ï³Ã\x0018\x001cì;ºéï\x0001\¤}R©aCä \x000f\x0003æ ßÑy5æãÉ%Äj	ñË[\x0002
T\x0019-a¯òå­A×kÐ_â\x001a ^\x0003,_*k0ª»1ç\x0010]}
X¯\x0001®Á\x001a_'×Tq\x001e`Á?9P¦y	¦^Y¼<ÍwH<p^`¼¸8{èrÙ·\x0006[¯Á.]C/k Æ"¼·'¹õøäkJë\x0012\½\x0004·t	Z 'b¹cn)5]@&oí%øz	~ñ\x0012­A[î\x001cLW6~mF|:Yhö\x001arlÔn\x0015k:Ì6;ªÏo6·?\x001c½º{¸¹?8ÒÓ4³<Haº$ó-3]9h\x001elþüüäâÅÑ«×ïÏÏ.¶­ör^A3ùf	ºP4úä$	:OÔO
h®Ð÷£q\x00188a¶Ï\x0014¨\x0019>»çWw·G__ÿ<»qÚè\x0013ÛéaHËÅX&ø<ñÊ~úúâèë³¯S÷4¶«°Ý\x0012ì´S@°#ûL\x0007çJ]ÌSYOMà¾\x0002÷\x000bÀ©a\x0014rõ\x0003
ôä@Ýf¬)ðPq/Gà±\x0002K\x0004N¥ü\@À}\x0008À;g¥rãRi\x0005/\x001d\x001e\x0007p«\x0016«´S²À)Q»×[/yC
ÍÜPqÃ\x0012îDË³êÆ\x000fÉüû\x0002~(Òß\x000c\x00158~9à¦\x00027KÀ]¤Ös\x0019ÜÉÛE©óIàO\x0018ý&ðÊøØ%ÆFfqAº\x000eÇ<óKæ®>lÛ\x0004]\x001e»ÄôèXGà´!ðZ¨ÃSõÑMØá±\x000c"k;¨òAKÎêºÂ®Ì]dv´ã9XC5\x0018?;ÓGÊ*»"¸%¡O\x000cÏ\x000b6
½õ\x0006÷\×\x0001Éc¹þÖ¹\x0001ÀV
jûî)on6?äÄÿçþtsý±©ºÛHÏ÷¤<¨ü\x0017Ñæ:¾9?y/\x0012G§/ÏÏÞ\x001e*Lg|Sá¥øQ<Þ[Ö)¾:\x001cÊ¹íÀ·\x0015¾]o´9|Ê\x0018\x001e
Ìö
6}ôGSø²ü7KW\x00108[$­\x0000J<Øò\x0001\x000e
ákY\x001d\x000eî¨!Cò¹â6+ñèíõO·¿\x001eÝ\\x001d½¹útýiö
"M6Íóe\x0015õ4ËÑ=Sæï)<Ø½³\x0012Þ½¼øs:ÈGoNß½{r\x0019£þ\x000ci\x0019C{ë <n®=T\x0014ìó9´ä\x0015wÞÖÑCuZ½\x000bÑÕBôúAFy_i\x001d£¼¯/í`u@p\x0013B}ÑyÀØphJ\x0017\x0012õ¡ØqçBLuDÌ\x001aGÄ8K	\x0001ÃBÔÐ\x0017pXHàØè\x000f\x000e\x000cí]GuBÌ
'$\x0018ïäÂ<Ü\x0005µÒ²±¼ú\x001d6j\x001d°Â:Gn1ª|ÑÞè¬d(ÇCsòº×Õ:ðË=éaôð+jk¨Xº\x001e«\x0014§`¥ï2x(9>Î)i=¿Ç9ÁÝå\x0018\g9´ÍøóÐ6ã9%ÎbÙe«n33$\x000fëQ£®ðLJßn>Ü\ÿëß·\x0014
¡+Aç6\x001bÛD4JR¶Ý¡ÇRÂòöäùyºc¤ì\x000boéGbæß,[@î©8,×\x0001/³ú
S\x0007º]Àþ·
3ÄüGÀi\x001b
O\x0015\x001ftúùÑÉýß¯n?ÍFÊ"HFVrH¨«%¥Å)É=Çdþ\x000e¦B¼åÿßË7§\x0017ïö»ïüð\x001fÎyf/­¯\x001eonió_Ü=üvw; >£8aFwÏ\x0012÷_ÙÜ^ß$\x0004*FH\x001b|¨sÑ'çISn¿§Â¾A¥RQå`«\x0013é7¯N.ÎÎeôó\x000bÚä\x0017¯ßÿåõÅ°9 I
`'("×d\x0011(äò½\x0004Êê	48½\x001ehZ³íhP¹éQÛû%ÐÜ<%h\x0003Ó°\x0012gòl}¯@Ë\x0003­i£\x001c·÷T\x0003Ä_Þà0Jt%Ð´ãc/¨×¹2"RlÞ¢`rÓ°\x0004jõRÞüæãßþ¶{®^^}¼ùõ\x0000[:\x001cNv%º[0ø¢.gCöè\x000eÛéÑËÓ·çû*5*d\x0007 \x0001Çp#OÂ¹d.áP«PÆYF3:¿³hl.#\x001a\x0007\x0013M\x0010!øÜOc=3
4èò\x00038ÑØ<eÙG¶ÈÆNì÷\x0006Î\x0003Gð$\x001cê?\x0015øìePP3Nìê\x0006d\x001e]tt~}$é@~¥N8\EBÒÁe\x001f+É64àhG\x00031\x0007\x001c¹®§ïqr «\x001b<8ÝpÎ·¹-<Mn¹ÈÆSG:Ï<Ö.\x0012\x000f\x0004ÝrÐ%=Ë
MwE>0a¶\x001bxÒÁÒ-Kù²åc\x0015xv?KúÒºe++\x001e\x0004O86G×\x0013ñò­|ð\x0014\x001axÒ>Ö
{9	 ¨AÒÏ¬x\x000c{\x0004gÑV¦yâ ZpÌ±HGeÇÚS9¾ÀLYý\x0006\x001a2X
\x001bY[\%\x001côyb²Cçfæ2î
<iëAÃFVÞ?\x0010s|ÚS²|,7Ôºöó¤o

YY\x001bÓâ	bµtÀ°âQn¸E'S±í0Çxå\x0012i(\x001d.ÆB-\x0013ÉPéÃµP)çr\x0018};îº¢\x0014mì8iöövó¿þcä\x001bÒÍðíÝýë«ûûqP¥]Gø¸¡\x0015Ó`RöNÎ½\x001bj\x001fF8tõ{ûúòyº±î¿öÅ\x001fþùA]p^ü|õËõíàV\x000fùi/6É¡¾{8äQSÉ\x001cíq?d\x0005Ø¼Ç5
o 0Ê/­\x0015äoO_]\x000c>õöâ$yÓ¯ßï÷ûõ/¿l>î¸ÓßÝ]ß\x000fys{¿_:õÇlGhpL\x001cn$Ñã+^:·Õw¯Ï.÷&ÆU([Wz\x0006
òPâÌ1fµd¸ä=¡\x0004x¬@÷w?ª7ÒæèÕæúãÝmþr?\x001f¸\x0005¡VÖP$ÇÜO2\x000eò,\x0004Êô0õG;?9zurööõEþhßî¿ýlXBÛ\x001f¬N~ùpwýñêèEúÓoO\x0007Õ\x000254`eî}\x000eü'76OLBSö±á=yõüòõÙÛÓ£\x0017éO9Ù\x0017(\x001bQ1¥é¡t\x0014r\x0015Ê!úJÚ\x0017ÌÇÛ¬\x001dÓ1]\x000f¦Ê-	\x001dÕ\x0010\x001fc>
É(á±æoÇôcLßiu\x000eºaòEÌþ\x0004j'C\x0013üÅa\x0019:0i\`ºÜvJó\x001b\x0008aâcÛÐ\x0019Ç±GÃ=9câ1õ\x0017ÌÒ\x0014Ê	o¨\x001fRzý·aü0æ¨¾Z¼$\x0004v\x0000\x0012gxìE¶sêSwp¢-_2?Üù\x0013&Ôx;g¥7uâ4:\x0016gNÞ]<\A\x001fi¬ ±\x0003R\x0019rb\x0006\x0008Z\x0010p7ZÊçp+($]©wÝ£ß)±\x0018)ÈÃN¾Ès"ÐÓÎi+NÛÎIÉúÙÁÀcvÁ|9èa\x0015ÆÊ\x0006é\x001e#dtîÖêáµ \x0001ÅòÍ!<3´sVÚ]÷¨wj½/&7Q \x001eå£Z³Rïº]¿§\x0000HÍDn6ãÓ%Øòw×C;¥P)xèQðÚP¡V>ëÂ\x00179þV\q\x0013Wpå RðÐ®àCJ<Nn\x0018~èC´1µÅ\x0015\x000f¨T'´«Î\x0010é:U\x0005%.ç£9q"ØÛÎY©NèPé>ÈWV\x0011\x001fò)\x001a\x0013ä\x0018ùP^;g¥:¡]uRyªDE¬á)4
oúé»O<»´sVê\x0013:Ô§ò1÷6¢\x001b-èâuz³Êv'\x0006ä\x0014º$OJ¤ ar\x0002\x001dµÀtk\x0008³ÒñÐ¡ãU²\x0016ÉäÛ¥^¹0\x0011kç¬t<tèø\x001bÈ\x000fÂLÙO
ÁË{¥zÙiæÄJÇc§\x0004h\x000eu\x001aoóýRs\x0005Ô[ÃÃÊ7Ævß8ÄÈãÈd\¸tg3¤õD8¿³ÒñØ¡ã½\x0007Ù6J`}hO9A\x0015\x0011V:\x001eÛu|rAìq¶ìVé<éÄ©ø³'Î50+\x0015\x001d*Þ'/>æ\x0018³£¶v9ÂË\x000b\x0006½ÂaÇJÃc»\x000fT{ÂMr+³RR¾X"Ï·sV\x001a\x001e;4<uÁÌ\x000eÓwÓ\x000f\x00053]1×øêÇv\x001d\x001f¢+±9«U\x001e¿Äé8!3®!ÎJÇc÷ÊJÔËÑC¾Îò¤jÉ,Ï5ÜxS©xÓ®â8Ó=¥94S\x001e¤i%6§é·,Ç¬¼xÓáÅ;r\x001cÚ<_Û\x0007ÇL4Í\x001a»ÓT¦Èô"
y¬6Ý6xròBôåº±Âî4u»GÅFÒ^âÆéß*
\x001e×\x0008oJÁ\x000e\x0005ïhJ\x0017+xlúèÊÉG_Ã®JÃ\x001e
oP^\x0015-\x000cI2<±3®qÔ+\x0005o:\x0014¼\x0003nþkMî²â\x0012E¤b+pV\x001aÞôhx,oD6Ý9¢¤%Òf\x0010·©4¼éÐðNé<\x0004/ý7iÑ¡/d§¼Þjðkm¥âmG#Ù\x0016lñç´D¾¨çÎ
·\x001d:ÞÒ«ÈÓå\x001aú$O#\x000f00õ¸ÛÎYéxÛ£ã©r[äY®Ù,Ï5Ô§­®\x001b¶ãºaib\x0019÷¨Øñ\x000c\x0006$¤Ã+óbÎÊ\x0016Ù\x001e[¤¢#ò&L\x0010§Ènç¬Ìí0GÆùÜ\x0006þ\x001bÅCF/×aTqÐ­Ìí1G\x001a%2K>H>F1«¤í\x001aE¶2G¶Ã\x001c\x0019\x001b$òåéá »J(Z\x001eµ^!ðe+kd{¬\x000ey\x0011I\x0013Äó±Ä¾ì\x001a\x0001O[Y#Ûa\x000cjáôJ2®\x0002\x0002ç4&y®q/rw\x001dZ\x001eMI²ödòö\x0004-Ñ\x0005Ä5R@\¥å]<8¾»Î\x0014Gy80acä*-ï:´<%\x001bs`ÖCà ½X#Ä°Âþtw=Z\x001e¤qÚd@óqÃNç\x001a1dWiy×¡å!\x0004¹·ûdÀr¹\x0013KÓ¬á¸Jyº\x000eå	ÖsÎ'.#é\x0017å¹Êë«§ëQé£{Ü~t#\x001fÝ®úÑ+åé:'`	tûäÊç¤|Z)\x001dsk\á|åÊû\x000eW>D_Â\x000bÔ\x001b#\x001föôWÅ\x0018Mä¯¶sVJÞw(y8=\x001f"ïÙ\x0005\x0019|0®Ä3k`V:Þwèøôò\x000eÌ\x0012Û¢hå½Hç	tK9+\x001dï;t¼\x000e(º39ðì!ûä!ËökDä}¥ã}§VErÜ­ÎÝ\x0010èÑUnÄÚ­\x0011°ñ÷\x001d:RýX{FK\x001dÄi­\x000bª5¾rä}#\x001f\x001cïÍä)ß	\x0012üÒ~Ç"_'wvX¢$-©]	Ê3'©±J2z§¯Lï0E%ù>ºÎ{¢^òø¶8C¥áC÷^\x001fó«R\x000e\x0010|x|ô²²R¡CqúÜ,;c\x001a	Õx)\x000c\x0006í×À¬\x000ePè8@\x001e>r ¹Ø5ø£\x000fS\x0005ÌíuæqÇÞt¡<\x0011ºm²óA8í\x001aO±úì±ã³;]ÎºsïDÁz["t+èwéT/9tª\x0003B5Qb\x000b³\x0003&ã)a¿ÜÓuAéåÞ\x0004ªuqÀP\x0006Ø\x0000ªXvÄ5$Zgyª£2±®EÃ°ÇáZÄÍÁébä\x001f%]'ñÓ_vÜßPT7Ûû0@,W£\x0015$º ß!®pÀ/¯ÃÃó\x0015NråX³>K\x001dç\x0001hÖ$\x0007l¼æ

]i«Ë½ÞIêîÈê¦G¹ÄÅ;7&OÛ«£²BdIïdLw¤LÓ©Èg#?\x0012'\x001b¯ÄeRk¤Î¢*Ý¶)`R,Ù\x0005¦c\x001e?ç¢	
Ô,A<QµF\x001aÅ]\=¸Á¤oÏé\x0008å\x0018ôì!J­áè\x0019¿Kk|\x0017-½Äb\x0001È§Ë¡¤{uk<~À#áB\x0017îP±*o5ZÊed\x0006í\x0010\x0015]#j¯¿ÿ»åÞ\x0013é'ÍO`¬¸+ÅïtÁ\x00044ÓjÖ\x0008>í6)Æ\x001eÑÒÌ
®ðñÉ¹r¢g\x0004M¼[Á©ön\x0017×»¾ðdºxû\x0008×váj\x001aüÉæ6i|ÎÎ5%²F­d\x0008»¸!ô©dË\x0018×\x0019»³%µ`¥\x0015¬ñÄ¬õ.­Ö]\x0016"¹©bÐ0úc.\x0005PjèÖx!{\x0004k»`u>V\x000bÞ\x001a¬6è\x0018`\x0005ë«\x001f©\x0005Ý§\x0016¢³ÇÁl\ÅÉENüY
jÆÍÝùÔ6äK½ùJ÷ÍÑ·eÐþïO±\x0015®§+ùìÔÑIÚ*Äé^3ç'Gß\x001e\x00144\x00021 ´\x0002ºÈ\x0001?,±´Y¢blzÕc<lÅóÃ*óñ88ª77ÒR$\x000f\x0006X\x0004hÆ¦Y~@\x001aÞq³%Sj£¥ÇH0=FZ\x0000í\x0018Ð6KÐIå)\x0001r7\x0006´å\x0003O÷¬iásc>×ÊGÉ\x000eÜR§ôÁQ\x0003¤É~C-x~çÅÇòyUù¼Æ\x0015ñM·Øiá\x000bc¾Ð,>#|É\x001aÔ¼ÇÒhº^\x000b_\x001cóÅ\x000eý"\x0006ÐøÒUÏ¨mC©Év7
£\x0003ihÕ,Aµ%DIg@]Tî\x0012ÔBXÛf#B9BhÈæe\x001dÃ\Ô\x0004k²IX\x000baeDt³\x00151
\x0018KÕxÙ\x0013C#`eFt³\x001d±¥®\x000c\x0011¤=\x000ej+n²»Q\x000b`¥¥u³F/¾\x0017õ_òÜZ,\x0016E3Ý`±\x0005°ÒºY\x0011\x0006+z:mG'Ì¶YçtSÁ\x0016ESû±·5jaõ\x001fÓÚ\x001dÐZr\x0008óLaÍÿ¸ºÿë¾VÉñ'Gù\x0014âòqÇØå\x001dÃÄÿqzùÍþÆV
ÆlÐÈ¦G½ö47ßF¢ªw²¶ÛñpmxäJs²vº´n\x001dÒPÇtfLgZ§·\x001a0),<¢¢ÝN±r;\x001dÓÙVÙ¸*½\x0002ð§ÅmËËÝ7Þv<7Æs­§ÂKó2\x0004'79¥Ë£Ýq\x0012ÚñÂ\x0018/´âYI\x0017'ÝÌ¹Z\x0018ôìN·\x0019oäÂNQ­|X.I:JÚ=\x0006'JÏâÂ«+½¢[\x0015R¥©¨và\x0001J\x001fÆtÕÁÕ'WG¤>§Y%{±¼èA¾®¥|ÕÙÐ#ùòÇÒÄ291LWùîäµÃU'C7\x001e
\x001d¡t0S®(\x0016_Z~´f>¨\x00064\x001e
\x001dbi\x000e¥¸ó\x001fù\x0003^¶\x001e.Ô{P[ÜÆ¡Ë3É\x0008O¯RÜ\x0001»PëAu0 õ`øâ\x000f¤¿à¼ \x001cÏ¼[÷ÜÎW\x001d\x000ch=\x0018¦gæ©ãd¾Y\x0016w\x0005\¨\x0006´\x001e
E|>rQ!]à¤Ñ«ö\x000b.VG\x0003[\x001fÚ¼f>3â\x0013Í¢q¡7ÕÙÀÖ³ ð\x0001Î\x0013^q÷º,X\x000el>\x001d¥Ë)8ª"!Ñ,*,å«N\x00076ç=\x0011ã\x000e%h(ÝFíxÕéÀæÓ\x0011ÏRó\x000fV.Ï,\x0014©Ni>\x001dQâºàL¹Hò¸¬oáéàFÍµ¦´+.i\x001a¸VVÅ¢£û1ÕîRÉóÂ®6·GÚ<ä±D{é¨[¨T
¥ÓÌígEîÃãèéNO.þtò~ÿä¡\x0011\x001cá°\x0011.äÁÔFlÅ5p¶¤\x0011»Ðn\x0013\x0019Ã68\x001a>-Mº\\x001c\x001e]\x0013ÉMlvÌf\x001b\x0005â´X
ÙËW-}F&B,MlnÌæ\x001aåæKÅ¬AiÏí@·÷7Á&¸8mp^\x0006-45È3\)ª0\x0013õ§-pãk¤*ð¹tV\x001dk~NMpÈt6JººÆßu\x0014\x0005ñ¥-te¶\x0000õ
ÊêØ)+{NO$Y6ÁUjN7ê¹ß]tÓBËÜ{Ö+\x0019`}(½ß\x0016ÂUzN7*ºß]t¦Óªî÷\x0016]¥êt£®£ÑGÒ¬&q\x0019\x0016\x001d~O\x0013oãMt¾¢óèB\x0005\x0017\x001aEgKV\x00064Àx\x001aôãgÓ&ºÊLèF;ñ;\x000e*E\x000c\x0018oÝ&'â%°Î\x0014&\x001aÁ7ÕÎf£\x00166Pú\x0011¨¡¡Oþ¨R¼F\x001eÝ2ºJ\x000bC£\x0016\x0006_ºA»tóÎ^¥:JÝ2¶J	C£\x0012Æ(ì²ÔDrRÛ­iV×"ºJ	C£\x0012 \x0005\x0016ÆØä£ªü&²J\x0003C£\x0006Æ í­L4d}\x0014
¬&¸è*
\x000c\x001a\x0018\x001c¾ÎÊ£|ºê0ò\x0013ùÓMp\x0006F
t\x001c\x0007f©w\x0000\x0011\x001d\x0014Ñ-Ür\x0006F
¬KÃ%îVce\x000cZÝDÚ^\x000b\x001dV:6zêéÃ\x0002\x0014ûÀm«¬\x0006*L\x001d4ÑU\x0006\x0002\x001b
D2¨\fdl\x0019f¥;r\x0013éÄMpÀF\x001bA\x0003\x0008ùÃ¦+¶bÃo·\x0016l¢©t\x0013]\x001dh´\x0011*ÊkÙÞ¬-JGt&\x001d
¬¬\x00046Zí\x0013÷ÐCZ\x000e´P~¢ÅB\x0013]e%°ÑJ¨2ÀÚ¯s$Ì"Ê\x0000%g\x0017\x001eÙÊR`£¥PÛfæn8½üeefÅÂë+V\x0002\x001b
òÒVÐÀ\x0015\x0014¢(Gv©>©,\x00056Z
52cF$Y.Ëuqe)°ÍR@ôUcJ/$\x000bR;¯Z&:S\x0019
Óf(ÊùuÑ'<ÔÏêrê:ÑDW\x0019
Óf(Ò§Y3\x0006Kj¨ÕÒÝnjX\x0013\e(L¡Hÿ-Ng:\x0013\Îà t¡0m\x00028UÐ \x0016\x001b¦¼\x001cW;Q\x0019ÝV\x0007®Û¬\x00042¸ÚP#\x001e>\x0011j«L\x0016^­Me%L N©ØÔÃá\x0018rÜB9\x0011è9Å¦²\x0012¦ÍJßÞ'ÐÉ\x0004³tµ\x0010º©Ç&ºÊL63A¯°â²'WÓ¤\x0019%ÙeØTfÂ´!\x0013S)¼-,\x001eNM\x0014:4ÑUfÂ4	¯¹¼I\x0000	CÎ&n°°mVâw­¬m´\x0012T Ä\x001eû6Ç\x0004iÚîÈ\x000beW	Ûh&¬&$	'³ÄMéD·LÛÙÊLØF3d[Ù© ²û\x0004L¤½7ÑUÂ6Z
»dÇn§!\x001d'²[HWébÛ¨©E\x0006OÌÑ(	½ÆB9²ná©¨t±mÔÅ.q¿JÉ]Ìðá]Mt.¶mº\x0018èéÕ\x0017ugÙÊ2Ì\x0016a!]¥m£.¦¹Í\ë\x000bàËx6h[Û\x0002ç*eì\x001a]v
¯ètQ(¨EtS\x0003\x0018è*uç\x001aÕ\x001d8ÅF3A9+ÆÞÊn!]¥P\£B\x0001(ÃMãK¶Ñe\x0000ìÂK¶«<O×èyÒ0z®Ãô%þo$ÛS\x000fy\x000fèê´6m§ã¶|ÁKÏ\x0002Jv+ù\x0000®Òv®QÛ¥{?g9ªz
k\x0017'lè*mç\x001aµ]2\x000fkz\x0002UÌsÝÔ¡O\x000e\x001en¢«´kÔvÉÊZ[¶¨b\x0015ÃDýe\x000b¯´ou=ùðyÛ9Éñô®VÌW§oô<)\x0008¥ögám±_ø*æ+UìÛT±Nú\x001b¹è¤ò·4rS\x000b­¯\x001cOßèxB(£¸c	í\x00180ò~\x0002\x0013/è*;áÛìÎ¢ì¤æÜ«ígá­\x000co4\x0014FQ.G®$3T8=(%\x0015SÃhè*uâ\x001bÕ	+\x0005¢._\x0016}¡[èÚêÈÆ#®\x001c
(9\x0006Q¬]è\x0002êTÆSA3'¤Ì
¸7èÖ·Kt\x000b\x0003(¡Úw¡qßar¸Î\x0008%
`ÀèÌÂÈX¨<Ðè\x0001@,µ©Ê\x001f[\x0016ô.T·®:\x0014¡ñP@,Þ
lÆ\x000c`)(oÕg"éb~òDex\x0018dBR¥\x0004já5;V».6î:ðåF¡JÝ»\x0001e
Ý2×NÕ
Þ\x001cv©*·\x000bd$r¦¸Ä¢¤è$=Æv\x0002ù¾Îx&G2	ðîáÓPôþòêãß\x001fn?nî\x000ftBJr\x000b»\x001bH.H)\x0019\x000b¬X¬ßU{¯ß¿\x001bêÞ_¾}óþâíÉåÁFH\x00192!C3d\x0012\x0012\x0007TÉãC+_j2Í­|}4\x000c®\x00072!c;¤É©	2æÃBÝ{9\x001dUY³\x001bmì\x001c7,19M»ÒS@j \x000c1'\x0008R{.Ä]¾\x0007\x0012*HhôÔïEéunØ\x001d´Eé«¬Þ\x001d¿ÒD©áûº:%!JÛ£\x0017?o>]m\x001e\x000ej\x000e
mB^öd¼/e~"yëë÷G/¾=ywzòþi4\x001c£a\x0013wò¨l­t:ð^4!Ø-dfLfZÉäJ-Ü.ZxïnA³c4Ûæ D\x0013\x001a~øRÏÐ&Z4 ù1oB³Cf{NØ\x0002n\x0014\x001c={0ÚT¡\x0006´0F\x000bMh	£ÜI)Ûì\x001cxÄÒÁVOô§O¦«C ÛN\x0001\x000eÏÇÍÉÌz¯tTU\x0013f·­Úkºm³\x0019O¯x¾È/+\x001eä\x001aOÅËZ¾híµ\x000cº­ôÂyR£LF1ÎH¥÷å
î'\x001a½Ï"tn Üú¤ÎI_Ä7®\x001eî\x000f:|ÉvIÈ'Xîë¸Ò>öß¼}wúþòi&3f2ó\x0012\x0008_}¨Òs=\x0014H-j\x000cE5Él\x0003S(M=¥\{U^ÇÔD6ûl(7ró¡(L,ÁÄ bVv\x000fq"Én6\x001fCù\x0006¨(©:Ý·\x001c,ú7wCÅ1T
EYkj\x000b%)õ S\x0001ºt}îæ\x001f<ºü²É%{S.1´Éû bùL+ÌwS\x001bÉ]Ì®´÷HxMU<=ÿè¡örßÃ¤:cìï¢\x000f&fÍÌ¦ªöèmA:ÄiWÊn±£§\x0006ðÍ¦ªÎø(2Îm\x0006òäx[ÉLUê¸ª:|ºáô9%Æz:rjS¶î'Þ)çRAu\x0002¡á\x0004\x001d\x0016Y)y(rZË\x0011t\x0013o1³©ªÝ\x000e
»=l©@C÷(ÒMUí+hØW£!=T'åê|]\x0002~\x00135ó5Cå]eí îÕ\x001c8
3Ú2¥Ëã¶im\x000fÚí/¨ì¸áôÿçÜÿxu{{°\x0001"y¦Õ\x0004
ñc¾¤­èÑÖÔ\x0000ñèäòëÓCý\x000fÕnAeÇý¦çòY¹\x000bÑ#½e¼\x001eª':\x001b´ñá\x000fù,Îü2äËèåÁÔ-£3c:óùIÏùl»ô\x001cm9q{æ®*^ÆD¶^\x001b \x001b\x0003ºf@\x0008¢W\x0002yÔõJo_&§û\x0011Ï\x0007ôc@ß\x000cèJ¹\x00035³àTQ¿í+\x0014'\x001evÛ\x0000Ã\x001804\x0003RÑ#ÛàÄ;òºìAµ§£ó|À8\x0006­Ã,6nv\x0019\x0003õö#@ÊÝ8\x0013&Àñ+[uî\x0012¡\x001eÇ"îR;°6"ÍVÄÙ »p¸^c\x001e¨è^\`X
XY\x0011ÝaF4\x0016f\x0011ë×±¤ìé»?°²#ºÙxC¸@9AÃc*;P/=Ãº2#ºÏls¾Ø\x0011s âÑ\x0006XÙ\x0011ÝlH¼\x000fbHº\x0003\x0016 g·¨\x0010§BàM\x001dÑíÒ½9¾\x000622yð2JáÄ\x000c¥6ÂJ
êf=\x0018ÐÊ5ò"B\x0016!ÈÝ:¸Y\x0013 Tj\x0010Õ sFúÂ\x000e
&}V2¥Åny>¯RÐ¬\x0004éñ¨©}\x001f¢tµ\x000fnb^b\x0005øÃæÇt¸ß\x000fX»ÒÍJÐ++	¯\x0014.\x001cLq $\x0015ÑÒzÏèù"¬ 4+Á\x00089\x000cFYW!\x0013¢u"CXx¡RÐ¬\x0008$?ð<ñz¤¨ÕÁ\x0005óù*=\x0008Íz0j#³\x001f¨7Õ\x000b\x001foGLª05O¸
°ÒÐ¬\x0007=Uqæ\x0010HW§\x0005\x0008
0,>ÆC
Í\x001euD'UõÚ«cÌ¾\x000cFiß\x001d¦²LÛ\x0008+\x001a]ê K\x000bj0<1É\x0010¥cpq)aeK ÙD\x0007R7©iÌQÖFJÄ\x000f\x0013i:MX\x0019\x0013l6&\x0001tÃ¢L¶¡)F¡áÊNê±ð(ceN°ÙD\x001aMÁ2Äaüö C'ºÐûîIm=Áf{~&±£!=\x0006+f]z/Á:8ÓnOÒànò¼\x000fCÙÎ,<)X\x0019\x0014l6(w±\x0008
MÞÊNxÖÁN4\x0018i\x0003¬\x001466+ì\v¬uÌi\x0012	Ð[q\x000b\x0017:þXéBl×Ö1\x001f\x001aY~A\x0006Z\x0005³4Âe*EcÚ\x0015Còâ\x0015ÒéfÀ©Ï6Àê\x0014öSL³\x001b\x0019\x0010rv2qZ\x0004Ñ,T¦a¶\x001f\x0011*ÂçO¬íÄ­{"Î'¬Îi?#AË2ÕYä	JùBòZ'ÒÈÛ\x0000«SbÚOIr¦¹\x0007/8\x0010¿\x001a]!(°h"´Õ1±íÇ$Éä¸\x0002\x0013\x001a ÑPòÕ9±Íçî&Z\kºéñÕDÜB=1½½
°:'¶ùÐ a.£¥nóÀ\x0017Ðâ0s½°:'¶ù¤Ó!Õ äZs\x0006}q\x0018ÔRkg«b\x000fJr\x0006¥æ\x0006\x001dk&\x000cº8ÿ°p\x001bºê ¸æ\x0012·N\x0017
\x0013
¬¯£Aèýi!auP\ûA1J\x001akjëóx¦ôe¨C¿;z«°:)®ý¤\x0012-¤I6ËÐhçÃTª`\x0013aýìÔ~Rh}\x000646\x0003 Éóa¢\x0003H\x001b`uP\ûA±%/¦9r,ÉLÊña¢Â¦ÐW\x0007Å·\x001f\x0014ç¤6ªlC\x0014ÏËû¸6Âê øö\x001c\x001b4 ÉÓ\x0012a\x0019já½ZxP|uP|ãAÁô´TR'\x001a*[&Bk­ÈPï·Û\x0010tý~³\x0013vÝ4ûQt6¹Øì9H\x000fò°\x0017\x001eæÝñîv<Þ½!~í\x0003= çÚ%Eñ!üº­­\x0006»4l@wù¡Ù-Êt\x001d\x0010\x0013Pí¥\x000fe*îJ3ö\x0008\x0013J¾+½ÚrKîèËVXü\¡¿ÿaG?4;µNòÊh,\x001b«qI\x0001vKZÚÍ\x001eíLÛ!Ì$8)H\x0004§s¤)]§å\x001a¦r¿çq:\x001c¾ù(\x0007\x000eGIJ\x0017¿ßÝ\x001e(\x000bÊe²	%p;Ç ¤õº¶\x0017'o^_\x001c*\x0008b0\x0018A\x000bµRÚbéuS\x0006TBØéKé\.\x001csaÀÔ1·ªwY\x0019RªYRã§o)s±Ì\x0018Ë´`%\x000bËg\x0014¸(-~´hBØÀeÇ\¶+9üò\x0019Ó­ÎJÃðÒË<LG\x0008ç¹1k\x0012\x0018Êk§uFÊYl\x0005í&ÚI41XhÚ`]SK³a¥\x00137\x0016Mß?ærÅ1Wlà\x0002[.F.\x0018
wä9ÁÀO¿Ì\x0004Óµ
kÑa\x0000ZZ4x¥Mö\x0016Ü@\x0002öLKVé0Ý¤Ä\x0008'k\x000bÄÜ\x001b\x0014¥\x001fL¥Í6UZL·¨1zþå~jôîï¹×\x000bÕ\x000bf²ez_WL·h2ê\x001bÃT\x0019!]hã±DóëJcè\x0016A\x001dr9ÊG23RD"=£m_ô5}Eæ\x001bÈ\x0014\x000bÌSç¬bÁp\J'\x0015¼DéJé\x0016UF¢Ø¹H>ù¶·\x001b+L?Ïåª4nQeÊFérìµ\x0014½RFEÇrCNj\x0018ZÉðÊHý1(Ç2NºçUJ\x0016Z¬2¥Ã£.=ËÇu²ZDVû-:Vç£8Y%Û\x001f$£(al «t,´èØ´EùíÑ'\x000fÖfE¦KÛEÄé¤¹¹`\x0016\x0015«&d>m¸ÀÓ4A\x001a",Úd³\x0008
ÞbH7:qÊ|:£\Ï®%{E£~GKVé~hÑý*§.Ëöç4ë¤à@>æ"Ý\x000fî\x0006Ý\x001f"
É\x000e£÷(*C9éwÎ.Y¥f¡AÍäÊJj\x001f¼}¥µ²\x0001À©y£óÉ°R³Ø¢f\x0015¹<ì1¦{\x0000\x00186\x0000^\x000c\x0000N\x0014:6Uj\x0016\x001bÔl\x0008ô¾FPÇµt\x001aØËÆ=Ï\x000fsÉ*=-z6yNëá·WLm´ÈÌì6i#«Ô\x00196¨³\x0010)\x000cÄdÎ\x00162½Õ\x001aKÔ\x0019Vê\x000c[ÔYú\x001bâ0F%3l³ôS9\x0000&Ntgk «Ô\x00196¨³@¯\ìfËdQÉ@[\x000cÓy'sÁ*\x0011\x001b\Æ@ù&\Ò\x001ePªÇ\x0003]ñXd°Hd¦Ò\x0019¦Ag\x0004ÂÉ]b¬@Î«tJ00\x001d\x0007KVLÓp2§\x001e\x000e\x0019£KË·4Sâ\x001a¸êTË¹ü·¿QuÙèð=GÁÙ\x0019TY1P
§3`¡"\x0006\x0017Ý4\x0001vù\x0000øH¹JÜØÓk\x001bO×Å´\x0013#E[î)\x0000Û\x0004øûÝÙÒ¦o22^\x0002ï·?\SäýèÕæúþú`\x0000ZQK\x0001zúÐr­Ò¥À&ìáæ¹ì9\x0006ñâðG¯NÎ.Ï\x000e¾\x0019Xi¶K ¹n8©Dé(\x000fPZ1ìÔ\x0012,!öcb¿XÒÛÐÚ2¤T\x001dOt	s\x001c3Ç%Ì&1eæ`Ó\x0019Ò¬/!o\x000b ÇefqvS«0n#­ø\x0006\x0017m\x0011u\m{èê\x0014ê%Çð¤®¡^r\x000eÿHêê(ê%g1Q»	h³>´Úy%%­G?èW|HºCÚÐ\x0018\x000e\x001bêÒû6ìÜ\x001b»ØÍÀ:z95¥oÖ·O	©u0¿\x0007'í\x000c\x0016M\x0007\x0013Tß¼7\x0003\x0008Æ@Ð\x0002Ä%+>yÐÒËXÒ³¢@8\x0006ÂÙ@Ûå`Ë%$5jÓß\x000bdÆ@¦\x0001/\x0016TYÆ	
# ~\x001e;æ±syLC@éb["½2\x001azÜ\x0018ÈÍ\x0006BÚ7Y@¦L;y\x001d	h¢÷àL ?\x0006òs¬§cðC+?8ª"¡n\x00011O-  ÝÌ\x001ah\x0019£S:óLõr\x00074nAëJ\x0007\x0019DQÒÇ(\x00084åéÆ©âl­H#|ãöñ\x0004)_ô¶ÞÎ$ª´¢­\x0016méº8\x000c.7ërÈ¦&Ï$ª\x000e}Ê"æô+Î:H7ti'¢&zÎÏ\x0004ª6µ½«½.zÈÙblC±\x001cjâ>\x0008ª]
³w538ßÐaîTLD¾È¨w_Cm[gï"
^Ë.ÒÒ]Ô*É#
q¢ÅÊL¢ÊÁlcg´ç*ß(ºÚj%o\x0013¹+3ªm
s·5êRÅ\x0007+å\x0016}ÒÔ>Äîm½\x0013¤È\x001bI\x00143>ÚjH]Æ(ÄÒ·lªµËS`.ìx.«×W÷÷WG__ÝüòTèD)¤,åÚ)å.É\x001dhJyvzyIîù«'â;aÇLÐLH÷\x001eqá¼´IÆÒ¡\x0012&
×Z	qLíÇxvI±8\x0008jªU^#¡\x0019\x0013.B¹(\8 nÝà\x000e­vhÛ7bi«Ü>~¤Ãh\x00131Õ<¯Ð	}»\x0010}IM&Æm[ôVÄ0F\x000c­Êti\x001dË@\x0014\x001d¤d0SS\x001b\x0011ã\x00181¶"j\x001a\x001eÍàAFèeàC\x0013þb#âÈ%¨\x0019OÄï²4y»%b¹¤\x0005?1!µ±ÖÛÍäÈsRI\x0019½\x000f\x0007¼VÆêHëæ3­ÀÙ}Ô\x0005×¥]ÓDFX+bu¦uó¡ÖÁËÛ\x000bíÛFqÍÃTk##T\x001aÚ?5õLt¥e\x0013?o )Ý\x0003üT×ÓFÆÊ\x0004B³
Ô\x0014îa×\x000bæI'F\A?ÕIº±úÖÐþ­ÓÍY.à¤ù=*R~çb+\x0008vvõø\x00070bµ\x001f±}?þ\x0011µKÖ¼\x001fÇ$éHÓ!§pIà®)ý°ë6Bxô.xúÓÍõÇÃ·tÃä[AºzKdÉa\x0019\x0011\x001av²,G\x0001æÓçgo\x000fÝ\x000e`×oÁolE\x000cÛñ)\ã0\x0001%noð~.\x001dóí¾Ìá3r}1É'ÓÜ¦ÚÆÆ\x0007Þúæ"º1¢ë@Ç¿2E¦\x0018ÑnãàbD?FÜ}­ì4ûd4Êg%8[\x001eíví@\x000ccÄÐHóÌ9WÚX(ÓÖ$I(\x0017\x0016ïÅ8FÜ}Ë#Å@¿ü¡Ä\x001d]É$³\x0010qä4Bxür;1Jö¡7-\x0011#ÊyñÆ-e¬Tn×9F!?\x0019\x001a3<gÄ -4w§uv VGZ·iBä´\x0008c@®N¦Ö%Æ\x001d¬q\x0014µLÿO\x0014µleÔZ¬4µ·æäRç\x001cwï\x001dP1B\x0017#
£ç\x0003çåÀ\x0018»T
G¥ÒþÐ|d¨ý\x00063n\x0010\x001dõTgå\x0018\x0016+G\x001cUÇ\x000fv_\x0002å:|î2Û\x0002¼P¸7µèIJçw£d~'Jö|sC£§þyøc<\mV}:3PtÏÞ«Öós?õoOCÚ1¤ýL!ý\x0018ÒºúÜºã{'í\x001dÅÖ Dz¼%=10g6¥W;áo¯U\x0006q`o\x000e\x001e\x001aÔE¥yº§j©ÜßM\x000cÝ\x0004z~èÈ0\x001dé zþ\x001b\x001eù£©	%ág·i`;\x001eñ°Qxª4Pèr×$<UYa¯}gÆx¦Qz6H_\x0018¤üZÀph÷ùbsáì\x0018Î¶ÊÎ¶¤±T>QÏÒÖb)\x001fãùFÙ%;ÇÃ Ä2cÑû\x0011î¼8Æx>\x0014é\x0005'i´£÷}¿Ï Ï¤ÓÕ¹Ð\x0007æÆÊÁ\x0008Ûéfû¦\x0006û|ì¹|ÕÞÓÏX_\x001eÔ¨W
ëe¸Q«}©¦3ù RÊÐ¨
¹¨@Ó¡Yï¹ÕC}È2¾êûBë÷\x0012¶¡wxæ£þ
\x0012Öv\x000b÷\x001fTß\x0017Z¿oR.F^åQ^\x0006Ê\x001dOý®à|&î\x0018Ýt\x001c\x000f¾ùû§ë®^Ü\ýrõDWPÚæ@þeÝ\x0014\x001dó88O~òæÝÙÛw§G/ÎO_\x001eÓ1®\x0019ãN\Q.ÊÐö2[¤\x001cë®N`?\x0006ö½À ¤¡*)\x0017À ù+vb¦Q'o\x0018ón^Wf\x001c\x0019S»EyBH*`5à8\x0006½À4ì#óêH®.{á²§ºjôñ\x0013óbyÐìÛ\x0011,aô¹	ð°#ØÇïÄµèÕ\x0011tÓ1"c[t­I\x0007\x0014\x000c\\x0018*bX°)ø"R1vx'nµ]<rS\x0018{U\x0010{Z\x001fóeÒKÒ\x0014­h-àJ\x0011ë^ML\x0011õ°m
çÄp ü÷m\x0005l»%lJé\x0006	;HðZö\x0004N¤u\x0012W¦C÷Ú\x000e\x0013C°\x001c;é\x0007V±üÔYØq%ÒI\x00165ñpsõñè«ûû_\x000fAÒÃaK%g\x0014·SûÌDBÎÞ¾=úæôòòÏOÃÁ\x0018\x000eà@;I,p2ªG¤hr¢2£	
ÇhØ&7\x0003%V\x0008e:/ÊÛ¨Vvb8K\x0013\x0019Ãf8y.£i\x0013òQKô©àìÍ6²y©35hxÎ&j,Qÿ\&67fsml0<Üåý¦Å¨¤/ÚT§Ì\x00168]ÔÆ£JÃÅå\x0011\x0014¥ÿ\x001e\x0012ê\x000f\x0013éÝMtÕyÐm\x0007b(Êá\x0006QéØ*.[*-r@Oô!h¢«6nÛuwùËZ\x0018ò¹4Õºw´Àù
Î7ª¹r$.¡èä2H§¨FêMp±m».:­ãhz;ïºà¤õ\x0017LÔ·ÐAu& ñL¸R\x0015âoë$­+è¦J¯èª3\x0001­FÂWè4òÓ\òÁ±\x001cÇÁû&¸ÊF@ :C6®6RÖ'þZÇ©«W\x000b]u`¡ÑLÀ0\x0001&\x000e¶ªXº\x0011h¿ð»Vf\x0002ÚìÄé\x0018.\x0014]'¾^x^GÝÈ/Qml±LÀ%6vì-X|"°rè°Ñ££'¢-\x001d§8ZT¦ÐõZ	Üu7\x0011¶]3Zú
×W÷\x001f\x000f\x0002Ò½({í:h\x0019 l¥\x000e
¨j$ñ^_\^¾}\x001aÒ!m3$&óï$'xà\x001d®\x0016Ê¤à©&©nÌè:\x0018MÉ[ö¥\Â©(q©LÿfH?ô\x001dPÆ|Ú ¹\x0013Êj°\x0004ÇfÆ8f\x001dÛ¡ÛÖÉ
Í©]½\x001cG±±ô¯ÝÝ\x000fitÇ\x0005Êõàs\x001dK¶ÿ1i¦Ô\x0015¥î \x000c¥ú/©p©µ±¨G3%VØAi%n@JÿoîµÚ\x0008i*HÓ\x000e®q«xyH³
2N¶wl¤¬ô¤îP¶¤O\x0000ùb)¥ð-É^ê¦Ô\x001dªâË¶<í(¥\?¬¡Ïu¥*u®4ÛúËÜrn ôe\x001c­h»ÐL\x0019*ÊÐA©K\Ó$÷\x0015wåáÎ­°/+®;tº6ÇRb\x0016ò4\x001bòDYÉ\x0006¼mP)KèPé¶\x0017e¥{k$\x0008\x001f&G°4BÖÞZ»»ôÎ-¥GP¥¾	!¨åG\x0007*5\x0004\x001djè\x0010e¥ C\x000b¡*=1(0ÇZÈºÇ\x0015Ì\x000eTJ\x0008:Ð\x001f!ÉJ\x0007A\x000eJwWÑçP\x0012ÄívØ¯l¯ÚHYé èÑA¿¿(±:ßØq¾AKÜFCpyÝÄ9X~¾±òØ°ÝcÓÛ¡ÊÇRÌåd®ÇhE3eå²aË¦-­È\x001f\x001céÛg«St¥l®ÛFiªi¿IPu¦ÝÎòVÀÝ\x0012¥0Îïv\x000cë¢¬ö¥é\x0008\x0013èí\x000cV\x0018R­\x0006Ê\x0012&ð~ùá1Õ\x00077í\x001f\\x0007'Þoºn~\x0000V|!oü
Þo=£,ûCÛÎ£ów§*Ó«è8ié?êËlº¼ù°v·-m4~|8zu÷ps}{\x0008\x000byb¬á\x0016ËÞÉÛ²\x0013o¹_¿?zõúýùÙÅÓT8¦Â\x0016ª\4P)/ijÞX©ÛÍ\x001fn\x0004³c0Û$.¬pô¶9é±¯¦^ë\x001bÀü\x0018ÌF`a\x000c\x0016\x001aÀÒ\x0016|á!Ó?J*¸<(»©©ÎóÁâ\x0018,¶H,T\\x00142\x0007Mè\x001d£¼&OÙ`£ÐÝöø\x001cD6~¬ÝvI&XLº:`0¤
\x001a½\x0000¬Ò\x0017ºEaX´Tà+oÈü\x000e\x001a¬.õS\x0011Ïùd¦"3-dÞJàÝ*\x0014»\x000cãjÉ×@æ*2×B¶­ìµIep\x000ehN&ZÃÔtÜùdÊÐ-:Ãi%o=\x0016½ÄØ£å\D­ÍD\x0013\x0006²Jgè\x0016¥a)hÍ' (z¬\x0018ö4~£jè%	*¥\x0001-J^\x00139£×bÉ8Û)fj\x001aå|²Ji@Ò\x0008¥%UZüó\x00082üê\x000fU6\x0013fôÔÕ%(½||\x000c%Ùijòc¢­\È¬l\x000bù\x0015ÐçZÃQ-6
¥½»þéöîæêÓa7Ü)x@1\x0016në K`eÚ
wöòâõùé»C~­ß-+õþ\x0019v\x0000rJ3\x0001r&\x0000bi8=	µ	Ð\x0001M+ I: ¢d>·%T19Á¸	Ð\x0001m³\x0004Aö\x001fusá/\x000cRM~ãâ/ìÆ|®O\x001b¹TCR-\x001c&\x0005\x001båêoö\ª\x001b\x0000ý\x0018Ð·\x0002R?
\x0006¤¼\x0000Î\x00121\x001caÙÄ\x0017Æ|¡YR%bÏ\x0011\x001e°Vò\x0001\x0000u­dµ±ÔÎ4K\x0010dª\x0019R\ÏÈä\x0004í&B¨\x0008¡0¹ëüdHMÍä\x0014\x001b)Ø\x000cf"e¶°R3ºUÏ¨dF¼¼Ë¤\x000f\x0001Ñîs\x0000+5£õLrß¥ìPY\x0019¨
2é8}dX¼
«s¬\x000f2 ae\x0011fð%ÆLÕ7\x0012Æ0¶~dçd$\x0001e\x000fòãeûTBc«\x000c+&Ëq\x001c\x0013¹\x001bK¼V'\x001f/ÞE¸Øªhó\x0008Ôt&ÇMu°Òm\x0006 ho(0\x000b\x001av[\x0014\x0004%\x001eØw×?|º»?úöá§»Åä\x0011j©\x0004Á³äuI­óc¼ïÎ^¼{}yôíû¯1\x001c4Âéò\x0019J9uÛ*ö®²Mp8ÃfÉYiy[Úw'Ém«Ä\x001f+Ä&833mp¦\x000c¬ÂôÏpÊ\x0014×L\âÀÜ\x0018ÌµQÏ	\x001eC¤Ê;SÛÊ	oµ	Îá|£Ô|IÔJ&/æ6ÈÛ$
"èS»w%UÝo®o?\x001e]l\x001e~øùê :¡Qá|$²´È\x0004Ê\x0015ë'\x0006 :y~rvñöèâäýoO\x000f©\x0014\x00061(tZêPÆePÆ\x0015P¦H\x00187í/4â\x0018\x0014{$\x001aJµ=Òà%j·eÌ\x0013ç¸\x0003ÔAMD"?<ÿ0&×V6§è\x0019ÜÁéÆ®G é\x0016*ºÇxñr¢\x0007ß=~b#¦\x001fcú\x000eL\x000fÀS«Qñþ\x000cJ\x001e£:¤tr1gè:ñ Íy)K\x0003x)FuÃ%çsj»³=)ÄQâ_/~¾º½\x001a)htaI%ôÙP\x0007ÀJ8ý\x0006Ð.NGÊC=!Ð	m3!\x0012h²Fú0m\x001c'L¥!4"º1¢ëA\x001c\x0004to¥\x0018K¤d¢v¢\x0015Ñ\x0011}3â(¥\x000c·O$¦Ü\x0002ÝÔ@ÝFÄ0F\x000cíR¥>5|\x000f-BtÓ/rMqL\x0018	½fÍCI\x0008\¬\x001dJ5ØÅ\x001bqôn\x0000Gï³?ó6éV{É7H×SùÌ4\x000f~)#TÐÌh¬\U°ç×ºàJ@bñV\x001c=&\x0012#¶2R¡,øÑyr\x0002¿§°Í¦²ÅæÖíªÛ:rêU/ÇmQÏDl¬±ÒÝºYyS;wÕIyse,iOÑ-ßîÖíÊ.6\x0012@J³ÎbE\x0013³\x0008Z\x0019+å­µ·K\x0006+ztúê\x001cd¤>\x0011"Ç©Ì¬¹f÷cFW¡Ëè·w7×C@Db\x0001#È\x00182Ç.\x0016p¢ÉÿÐbôÛ×çg'OÂ\x001bøQùÉ<:í\"«Òq\x0001±"X\Fg+:ÛHg\x0014»`\x0014ç#B·\x0006-N>\x0003ÍS»-¹´äº¹\x0019vßóÍí0Fûîá·»C/\x0014ê\x0012# \x0000m\x0000-uæ8ùq~>ìÀç'\x0017Ã<í×ïÿòúâÙ\x000f\x001f7\x001f?¥½.¿ØeÅ1+ö±&$î\x0001è­'\x000f<Ã\x001a~¤G÷øc÷ÁÚ1¬í\x0014¬þ\x0002Þ;¶\x0001ï\x001a'üï>X?õ}°yNï\x0000KýC)ÈaíccÖØ¹\x000bGC:ý¹aÚ\x0005<aF\x001b÷8\x0002Ù\x0000k¿ÿô7üûoçË¨ëÃÑ»ë\x0004ûpóÏ2eºë	:áQUçLÛt´p8PVI\x0013Rï4èÎÞ&\x000cîÄ÷þèÝYÂ|¾çØW\ÉúV®d¯
cÙ\\x0002nUà>&Ä5JLïæJÿ
÷\x0019r'«?$*\x0001sL`¹\x000bY\x0002\x001bÕeus¥nþÁ\Û4\x0011WÎ;&®QC60÷Ë\x000fpsÃìÉwô\x000f|Ê}£ö\x0012%ËkhØÊÐ&mù¡jÑj9FëMp£$½\x0001é»ó\x0017¯/Þío\x0016e¿¿	¿l\x001eþ6¹¼{ø4Þ\x00177üz\x0010(ýsú\x0000\x000eÙ v\x0000JZLg\x0019ã]\x0003Ïåë÷ï\x0006Óûâüä»}Eû¿7.ÚÏ?Øbë¶íû¿ óÓC²ç¥ÉóÄÖ*~ÁÁ®í[>¾k2ß¶<z6 H
-Òn°]V9'òÓ\x0016ú	ý®\x0004ý(±ýÍýÕÑÉýíÝÃÍ\x0007	÷IHå\x0001Ù+µZ*§ â\x0004áû£7§G'É\x0002ý4¤\x001bCºvH*4Îó\x0007¬1·µJ~Jmã/íÇQÙ \x0011ì\x0004éùìÒK\x0015ÈÑä\x000eJ;rTó\x000fÆo,¯6ãZ\x0003:/±\x0000nÉéNJÏP\x001aúÜ§o^<Um1Â4cLÓé8W3\x001933ç\x0012fnÂK¶lôVÕOéÇ¾Ò;.L§{h7?PÃm]2)c\x0007%\x0015\x001a\x000b¥Ém$,õ©\x0016ûkÂÔÆlÄÔõÎìØÉ#8Öéò\x001dÏÒ©ø{V¹\x00150«©;¶f ®Õ°\x0015'ë¢ ºÈø]Øé*L÷¹b
3t`ZÇUû	\x0013ó«4qêP8õ"N½«6õ3=
-mh\x0010ÇÑdÍ7\x000fMy0¤Ô\x0007Rj¯I=¿ü%RðSû\x0002L'4ãèë£ô¿O£Â\x0018\x0015úP\x001dpÝ\x0002RÝÎ'ÞCA\x001dw ]cTìDE4¤
QQtè¸\x0005Þ\x0002T;Fµ}¨VêS1íPQP~{Á\x00025µUQÝ\x0018Õõ¡¦
ªmAÕy¯:Îú\x001dP×ª®öªîÛ¬6l5@ÜO&±ê z?¸5Î®vîÜ\x0002\x0000Å{R\ªJî|±Q\x001aÖØ\x0002P©+èÔWµ?¨ÜD/¢/\x000eRÿÍ P¡O¨6j~£\x0019\x000c¿æ
\x0000FLÅ)g¯ÕW¬¾s³Â±øøj»Wµòv
T¬¾?ö}ÊQ
¬Ycd\x0007À\x00069V VQ¬h*Tóª+·{+qã[ÉÍ<\?á§ÄíE>ýÒå@2åF\x0012õäEþíÑÿùþì âv-\x001b¡Ì\x0012\x0006	%l¤¸¡\x0007©Ð)ñ5°ù1o\x0016åÓ\x001d=ßÝ\x0013\x0011«\x0019÷]åæÂÅ1\lJÙ**Ñe8'\x0012(×-¹°ëx\x0006r<_ü|õËõmæ»¿ûåêöêá	\x000fÙúr\x0015¦ñ²më[ºÉíØÇ\x0017ß¾:»È¯_¦¿uØG6»¨fä#oþqw}ø\x001b#ë ó¬èt]Á\x0005=\x001d@:?ùîõÙå^®\x000fÊ×"|~0Ì¨»ÿ×ÿÇ\x0011ÃÑÔæàå6\x0012³?J:oW\8~
Þ\x001c}swûis}{82è\x0011dëÙPLI\x0000]ìd\x001c¦\x000c}óúâÝÉÙÅ¾Ø ~¿©Eß°èÎï>]ü8Ì/ OûÝõÕÃ?¾»ºÿé>0òC\x0011>»ØÜ~ºz¸¾ùêãÃýW'×\x001fÓZ=£ÞÏ¡(V¨ó»!uV\x0018¶b\x0012­5CÀãäâÝéû³ó¯Þ¾¿ü*Á'Òó×ïÎÞ¾\x001d\x001aÐ§ÿîìôý¿\x001d}wzùòtß\x0006\x0018­\x0002Æ«å«ð2Æ¸É×#ZEn-Aiîë/\x0003ÇËÀ\x0015>\x0006Õëü1b ë4,#fåá¢ù\x001daÆË0kì)ÎÛ eè<jèå"
Z\x0006®ø5-êhÐ\x000fèh¼¼ßÜ¦ãNñ\x001cjCó\x001b!S\x001bä2wLVÍa¦ÖÜôþ1õËËtÓq~\x001a\x0012ÆÐ\x000e\x0019¹\x000byT!ß\x0002PY\x0017x£SBýrH\x001cCb3$u	\x0018ì\x0007IÒç\x0014õ$I»'IÝ³[ Í\x0018Ò4C"E|\L¦d¸û£Ò!°æÓ9¶¿Ñ\x0019m» Ï\x0016\x0002~!'\x0001£BW¶$æÇÃen\x000cé!©W£É_ÛjÇ¥ß\x0015\x000cCÂð$¿\x0014Ò!}û×¶R\x0005\x0007IzÌ¹Ê¨\x0000óÝ)IÒÆ=*©\x00052!C»$UV?\x0016y4\x0018Á3!h³ÂÉcÂØ.F4Ç¬"},RTQÎ[á`ó³èqÕ!FÌOî$I¯\x0000HøH\x0012+r][vsC£P\x0001Xÿ8Ê3\x001bô\x000f'\x0006$Yr·Óe¹Ñíö&9­bÊ-<\x0003Õ0J#Ë\x0012V8Üº²7ºÝà@\x001eú=P*ÈCWcät\x0007·ütëÊàèvC\x0015Ê1ë z\x0018\x0019ú\x000cBÁ\x0004å>'µ²29ºÝæ\x0000² éöÌJÈ[`AF³ÜàèÊàèv.|4¤k ´Û#$A\x001a-\x0012ÍrÛ­+£ÛM\x000e\x0015õË¦¤îtÕ\x0010\x0016»\x0012QV&G7Û\x001c¹l~ðÕ\x0015çáBôÜª+Q\x0006·²¬Ìn·;ÚÛÜe0ùs[\x0011è}wÔ\x0006D¨¬\x000e4[\x001d\x000cÎäOIFQë	¢L¿´vË7%TV\x0007Ú­ö\x0006:dAb\x000e=\x000e²¢t\x000ew/£¬/9ÍV'ye&w\x001c#Y\x001c¥*Àj\x0008a£\x0003Õv«£ÓÏ·õÇYèeWróÉeÍf\x000199ÕUnôOT²+Á­ ÉÊæ@³ÍÁ\x0008\x001f\x000c\x0013enéFÎ8%w[FY\x001dh6;XÒÁH>{èÔ\x001e2²BG\x0015dY\x001dh6;\x0018|2y[:à1\x0019TVQ/
VØÙv³\x0013\x0006Y\x000f9gå Ò¨å\x0006Tf\x0007Í\x000e
ÆË	"$KnE\x0007e"\x0001ÉÒ-×XY\x001el·<>]h=Sz6 f¥"Ê°üð`ex°Ùð$\x001eJL²\x0014Y\x0006Çå÷\x0008¬ì\x000e¶Û\x001dJ\x001f]é!Ïâ¢ñÊE[\x001a¿üì`\x001d]k¶;I\x000fñX3²\x0002D(µX\x001e\x0004½üì`ey°Ýò¸`å\x0016î¨:<ïJÔA\x0017h9dex°ÝðPÀÝóëòú\x0011µìJXãìT*\x001dÛUº{¿\x0013e®C\x0003êG"\ãº®Äv]ùG@ý~³ãjl>K_Cé\x001aT7s\x001ajhË[3]%ó#
*C£¸òUgîõr<ó\x000fèÍääææJrä?~øõÓÕý\_\x0018(Y:;Ãñ\x0018Ù\x0019f\x001döZóóóSIûüÏïN÷ì q\x000cýÐÔ=NAñàCVQÉS*.ü>\x00117bÛ]l;Ê­|swÿéw\x001fIYÂëË}¯à#L;Æ´íécç²c2O1wA\x001bÞ\x0003DïÇ={¡Ò)]\x0007%ÍifD§
ËM[\x0002<ón!¦\x001fcúvL\x001a.fmq$²\x0019<l+¿çÎÑ\x0019þ\x000fuo\×¤N\x0013h\x00062ñ\x001f~¢U´­\x000eý]Jö¹Õ/\x000eJfÛ¼-nJr·ûé¼Þ!\x0019Üy\äB&6°÷ææZ\x0000ìVEGU[¬*ñ[	ä/2¿¬a\x000ei¦¤Cs<rDÅl'\x00171>\x0010(¯éö­Ûk½Y¬ëÇ³ïîÞ/ôD+üõ;å	\x001eE5b³\x001eÊæªfÅÔ¾¦ô\x00079*øXÃÇQøJR\x0013KfÝX(\x00167<p}·¢òÅFã¾¦\x0004²/,ÄP+\x000b¢waCsçA4®<ÁÁCÖûd¾>Ù!ªö/Ú#t¸|÷þóÇ/].ÊNÖ¶.O]N\x001aó)½[¦ý<ûþÁi¿
¯®ñê^¼Ô
\x0010\x0003;\x0007é\x001duJÛø2|è:o\x0006ljÀæË\x0017°­ñÚn\x0001\x001b(\x000e\x0006¥óBÛ\x0012ãÃ5û÷wiÚã\x0001è¥\x000fíùõíýíJm#jk¾\x00109¤IvÅ¼Å\x0007æ<\x0012½ô¥=¿xzõô$f¿ï}m\x001bnÖÛ\x0006'æÌ$3¡-\x001bèÅ8øS\x000e$\x0019K2\x000eÇi\x000b($×õ°eþA38}uûëÝÏ\x000bX°\x0019,~õüóý§Û\x000fÿtóé¾NÿÙ\x001fÔåÂnæ-ñÊXë\x0018\x0014 gN\x0010LßHFìù÷Wo¾ø§Ë7ÿôõËo_ü}7C}õôyúÁC\x0012­b
\x0014ûÚ\qIH/lBÊÃ-\x00011elS ê\x001aªîªó[x*
c\x0004y§PçAÁq¨®êº ¦C_\x0013Ô¤Và2TdR\x001dÔj¶\x0013 ú\x001aªïj3;W4Þ\x0016\x0018i«êg³q¤±F\x001a»:(H©fÍçÏï=	jXòÇa¨Ðªþ{%jµ¼ 1V\x000b\x0005ë2º>é`v\x0016 I\x0018k?P\x0013\x0015F«|X^3yb%¹
Ïvu\x001fíÎ\x0007&-¨à\x001a®é\x001bd3\x001f½\x0010x«£ÀÕÇì@\x0007ZW£u½h£ËO-	-¨¼~(¡µüx£YØ\x000e¸¡\x001b:á¦ËKQ÷\x0002WÞ~\x0013\ÏÔîàÝ$¸ÜÁÅp©«\x000f/\x0016:õ@ä\x0001|\x0019ãíNþ¸\x0001ëÀÛ¨\x001atëZÔÂ·\x0016hWÈx+òõÇb\x000e¼®A·²ýex\x001bm~uCYM\x0010t8_6w\x0012^¦#¼sl\x00194ê\x0006½úF¶7\x001a¾¿¾è\x00061fÞÍ/6ú½úFòe&ZR½Xî\x00033y;É>`ëÚú}Ú9\x000b),\x001bß¦\x0017öÅ	x\x001b}Ãn}ó.gÉ\x0017G{.®\x0018Íc<\x00169vÀmÔ
»ÕÍ/YyË«\x0012	¯ëvºa£nØ­n\x001er¿]\x000eu4__°"_s\x001bt£mº[Û\\x0010ª>zÀ\x0007«x\x000f±W³n/½0;£t_bæd¥Ñ1Ñ9N*ÎÑK¡÷Ã_\x001d\x0004øõÝý¯wk"u¢÷à-¤\x00181¯µ3uÈO\x000fé¯_^=y:¥¨¹;\x0019§îÂÀ\x0019æi\x0015*Ô3¨ HOg\x0014C5u{DþÁÒ\x001e!\x0005èÏgoî>ßsi¹\x0016+.\x0002üBä¨À£Ú[!\x001cu\x0001Ý\x0004)?öæå÷W\fZ®ÇãøMßâ·Ìô\x0014=íÑ\x0010ülÝ?fGÐ»\x0006½\x001bDO«\x00152øäª9­K\x00163\x000fÙ^gÂ\x000f
ü0\x0008D0~°L`EY>öÎNoT
?ýi\x0010¾§7®\x000c\x001fx:_\x0013»À7Çê\x0015#ø\x001bÝ5£º\%ï\x001a&üñpÚ&üÇ,Î\x0008þFwÍ¨î\x0006Åì\x0012(e­x!Þ!ðÇcu\x0011üöQíMÑE}%ó"º)QßcÁ\x0008þF}Í¨ú¦x00~«iò:g
RI NïÙòo|\x0006ô±cðß[\x0007¦M	$Îc\x0005®ÏPõ\x000bvþAõþÀä*ïo>­@­AVK{jRd¿\x0015%,SµR&XyvùÐk{\x0015k¬Ø\x0015#E\x0006\x0012ä:q²®\x001fÕ±Ò\x0001V×`u\x0017Xçì­õü:o%\x001c×G=j\x0007RS#5}b([ìé\x000eóÅõ²}5¥fúÄ#Ä\x0016°¶\x0006kûÄj8¥¦MúiIÓÃ'³-`]
ÖõIViÙ(ï£0kj¢\ú\x001a©ï\x0013«Ñ²¦Ï*«ÓR\x000c3v\x0019\x00085ÖÐ5jI\x001a\x0017êR6\x0003ÊÇÙÊ\x0015k°±\x000f¬V²õøK¹lçÊ\x0015°0G°uÜezâ[\x0010Ä\x0013'hT._ÀV5;8ñÈ·\x0005më¹ú\¥Ãg´:\x0001]\x001eOµõÎ¬àv m|\x0017ô9/\x0004ªCA\x0019­Sxº>Þ¶q	Ðç\x0013þ:´O>§@ëxw\ \x0017õ\\´XÜmÀI7¡q
Ðç\x0015â1\x0001ªäës\x0006\x001bJ%Ô\x001fMW;À6¶\x0016ú­7<â­\x000bçÈ¥\x0001,uÅI`më\x0014\x001f,ë¦{"/¡õô¦\x001a\x000c\x0007_±øSM\x0015ë0ï÷ÿÔdë3$´¿Ñ¾ÇÑFçr]1\x0005\x000bé6,­Ã)áW22 ÂÑ´aÇöà¾¢µ+ÃÅ\x001a.vÁäÁs\x000b@ë-\x001b\x0006\x0003LÅHï\x000fîhy±\x0003®®áêNé&PË«$I×ä.wk÷Ò¶\x0004Gsû\x001e¸¦k:áRí>£uT[dËK:\x0011µ9js·`5aïâÐ4®ýëà¬È\x001a¼Ô}fI\,\x0003sàPÕDì]û\x001f\x0017W´äý¡\x0015 \x0015X¬Áb\x0017Xâ?Ã\x000c¢G	\x0019Ë&#§ãÉ¢øz°¾\x0006ëûÀª²	ú×|ä¸F¼±ñ7[\x0005\x0016ÍdÑ|ÕT\x0001\x000eò³'ïï>®©ÿ\x0005
¾\x0016á\x0006%iyº¯×¡;]øX:ÇÏ<{ùPßøò\x001e¢ön®VÍÍÍÐV\x001800¢b)\x001eÏ\x001ba\x000c8®!${ O6åÿàqXãÄ\x001eÉÐ:ö\x000b4*.vV\x000bÎÓ`-N]ãÔ]ò\x0004:ò,PÌ\x0001B§ôB8ú\x000e½\x0019§©qí8UTiÁìe\x001a\x0010'
ÀZ¾é{`z7Çût\x0001l¦\x0005 \x001f øI4ãþu5PµoTU8Ü"ð\x0018NµD®¹´á
Ñe.æ?9I¹%87¼ÌÃ45Ì\x0003òè\x00150ÉÓìcñk(ZÌyLéáÁpe\x0003LWÃ< äüÔUr¦ùùÐ\x0013¡\^²)§\x0012L{üÑv#ÌPÃ\x000c\x001d0q\x0007Óy\x000eþÐcP\x0008æ4
ìÙx\x0003õ`Öç³77÷÷·+RàkÔ­l¸LhP\x0016a£öêØ}U¿¼ºzº\x0006l¨Á.°@ËÄ³©'Â±ü\x0000htÁjÃ(VÜ\x0017,Âþ0Óo·ëú£ôÖëdòF#bLã\x0010Õ\x000cQÏ._=<tUáÄ\x001a'vá´fáá§@ÚgªKêV×ó*ñF¦Æiúä©r¬GéPP\x001bdXJ§ö(o\x0005\x001ak ±\x0007(Ð\x0018vóqyn_î(d\x000bN	íýìº ¤K\x0002Óä"ât\x0012Î]ïßO
G»³gÕ×bNcÉJÐl-\x0006<®M­¯?Ë?=\x0001Úï)¿öí°ÒÝçßïï\x001eÅ«>Ù¼ÃÓÑBVûü\x0010N\x0015³/ÏÒ?üpõr\x0005T¬¡b\x000fÔhR"b2Ôd
\x0016>LNy\x001a©3n\x0008ªÑûÉ©nS¨7)z÷K¦Æ4vò\x0002G·6[Uí1p%;y«GS\x0006õä»ÙòsÓÍ~ÍJ7×`å¥õÉ\x0003°³¢TJË37r·J|¤\x0015î±ÛªjV\x0006©¿@¸/MlÆ+×ÁLa½ËU\Nc×\x000fs}*§j\\x0012kØ2sêâiä9D(^ÿÞoEij¦\x0003eÊDMA©%³7¡ <9àñ¨\x0019ÝïcÐíØýzãDÍ>çNDÎ\x000bÔ¨qJ\x001eàº?fÌ¿ÞÝF{Ï\x0017t¯Ãû³ï®?/\ü\ßZ³,¡xû_Â
r<:öt	¡p\x001a\x0018î¢Ô\x0019dÕ³§ÿÒÒí?»<ûîâûvÿD]§A7w"µH¯ë\x0019jÈs	ªÎÑÉåÏ\x0003¬î\x0007
¹Oêä&ïû% \x000e\x0019¨.ëUg@ÍÛË;¡:\x0007"ÈÃ[ár5Ù2%¤924]xÛTe*Å¦h\x0019©¡Ú`&BÍ«×{¡¼³>Au®@u\x0002\x0014ãD þ+*Aõ\x0002¹üH2rQ]ö\x0004ÕÏ¼¨)q\x000eÝPSâ$Ê\x001ftÙsâ¼\x001c¿\x000b3¡¦\x0013ÝPC\\\x0014Ò<\x0017JÏÇ¯ó\x000cý$ Ô\x0003BÿêDª\x001cQJ=ÕÌM,Ô\x0018&ª?9\x0012è÷S6ä
!¸l41¢ÿ¹û\x0008¾£5\x0011t{ª@ÃO|WM\x001eòE¢©\x0010\x000bàÕD\x000b@É.tûª@=â«øQ<v\x0013Í*U\x000e¡ÛYùYìª\x0016\x0016KmÀ\x0016Ë:SµÒu!w\x0015\x0019«/¬ÙÆ*	Vr¿ù,¬éïn\x0015?õ%\Ñr\x0005B	W\x00085ý]Ðí±Õ¹S%aUé\x001fù
ð\x0014H²\x0002s-VrWÐí²Bº£å6·[\x0012©\x00153\x0000~¦ÅJ&\x0005º}\x0016mà¶l\x0006TÌ\x000bPH®b]Ò\x0013±Ò¼1v{­`MÞ?@X-5¶g¬r\x0007âÄûJùØïµþR3@æ\x000fû½ñ¹\x0002\x0017!äLÿ'Kº#\x0013¡&/ý@»Ìº :ÄKH½dXÉiÍ¼\x0002é»±ßºÒÇ
,¬,W/^KÛ\x0010&bM\x0017ö,z©È\x000b1q:¨Qyõjb4@Ðºß\x000cÀ\x000bëÊâCmB+à&\x0006\x00034úªû+\x0017j\x0017»&§ ÖÕK­\x001dÌ\x0014kú»tE\x0000Ý¹råºFk<ö»NÄÔJ÷'Ú\x001aò\x0003\x0000ÉU\x00190ÊOT­ß?þñùçºxuóñl¡\x000f>ÌPÉÏgª=·­Óò8`\x0003\x0005\x0001[zùúla\x0008~\x0018Èüöîúßl]ï»>ûáöç-o\x001f\x00061ª/]Èé7ÇÅ\x0013åµìÖ\x0015­_k`\ýðôaª©\x0006\x0004Kã¿\x0017\x0004éþ\x001b@üñù·ßo¼ö&¡xÿþúçS8 ðVA

Ãyæö¶1rU¸º\x0017	Æ³g\x0017ß>DTh~DÔw·¿×÷âæ\x0011½I_kó\x0004é
okN\x0019}´
{\x0018\x0016
¹¾wó[þ÷Ã_-ºñè¯&\x0006\x0016à CçÔØðÝÍ¿¯Àã¿Yy	\x001bÛ³r\x000bR?ÀÍ¿\x000b¯ÿf\x001aW`º[nk=Àjó¯æJêc¿ZG\x001f3eqúÕèsë\x0001m9_ÛO+£ÿêX*\x000béfåö\x000cZP~õö£æZçã¿Ú¹L~µ6YÙ«ª¶ÖÛ\x0005ÎµËÇÏ:Æ<cGí\x001dLeN»\x0002X½ÑoþÍ\\qÔX>Úù²ÓE~õ~\x001dgÅ¯.ÅÅ\x0015ºå(¿ÌÅ=Ý¯Y)À­øÝ1¯#'/F>ÿnÉ²÷\x001díß-UªÇ7Ú¼Ã*R%^¶Zê§&nþÝRÉYaUb\x001eE§§\x001bÌl@´µ©\x0014îVþîtv¦zÏ?¨F1^ÝÜÿëõ\x0013X¢¼É\x0003Mò£¹2§óqñ®1´6{q^]^½JNöâ¡VÖ
­ÁÙà<=m,à¼\x0011×\x001ft&&uà|
Îo\x0003\x0017r+\x0013R?@^\x0001°\x0019\x0007Òß\x0008cØb-nÄ\x0016©Â¶&²\x0017pÖ	8°f\x0008\x001c÷1¸ª\x0017l-:Íà¸©b\x0001'ØÌØ¡B£\x000e°Q\x001fbyXCêg}ðJÐa[¢Ú®Ñ\x0007Ø¤\x00106E.\ïET² 7ørç´ÇÁc-c~»£]æü¶HÐå®\x000429\x0017¹Ó+çýç[7uå\x001fHÿé7÷7?ÝÜß¾;{uýéT\x0014O\x001bl.>ðJRkA6)Î\x001chÆ7W»¼zúäìÕÅÓ\x0002O×ðôFx\x0016a%Ã¼H+	C\x0019^n6\x001egjxf#<Ïû\x0012¼\x0014{¾4±ái7
ÏÖðìFxÁfby¤æÜ\x0001I693Óq\x0014«á¹­ð\\x001eÊ é)Ùú\x001eL^¿àá0<_ÃóàYe¼¨¢%\x0002ÙôE¹3<¥Ã ¼PÃ\x000b\x001báñdXB</\x001f­<Î«\x0008úÀªl\x0004\x0017kpq#8òÑ\x0012¿yÈG[b:\x0015â(<f`x\x000bÄ¦³5¢\x0019Éª»ìs#·°\x0012>7höê@`-> f/Æ\x0017 Qccd|Î\x001cDS\x001bñ5^\x0003¶¹t¾¼ -á#\x0016¼²":Ñ\x0010`P7 q\x001b°ÍoØ$ßP\x00102}¶¦¥\x0000\x000cÏ¶}k\x001dð\x001a·\x0001ÛüF:^¹@èxU.£Óñz\x0010|vT=\x001a¿\x0001Û\x001c¥ã\x000b<\x001d£ÉoÓ¦?D;Æy\x000c^ã7`ãH§ë3«\x0012.µ0\x001bätÙ¯\x0005£Gñ5\x00196f ØÈò³¹?á\x000bZði\x001cÔ^l¬\x001fn´~à\x001d¿çkÊÚ4ðùFQ\x000fAõÀÆúáFëéúYÆG\x00032KP
hL.®*ïí¨üÚy£õC`úW\6©eët+TÊG?hý°±~¸ÑúaRZ¹\x0008¹c;ÉÏ+ÁçÌèù6æ\x000f7?Ô¼\x001e7áKAVö¾\x0000¼2ÓÐ&AïùÃæOçdrÁ§,G/ å¬Ã8h±±¸Ñþ\x0011Srdù©\x000bt¾Üí¨¼ÅQ|Mà\x001b#gâ.YCT¼\x0011\x0011´èÅë¶\x0001£\x0003_cq£}Öô\x0010\x0019\x001fäF\x0006M[¸½às£úÑ\x0004Ï¸1zÖ¶Ø\x0017ê\x0014´ñY~
&úé1xºq\x001fz£ûÐNqW¸\x000e>Ó \x0013º¢½¼®l\x0000^ã=ôFïa@\x001a¬&;­³áYªoy~\x0019Â×x\x000f½Ñ{ÐÌ\x001c+sÅÒ\x0010>\\x0017\x000f+j\x001bá5ÆYo4ÎF\x0007®Æ/ÍIÅçÄø¹0\x001aêÆøéÆÏ¸\x0019¨\x0008¼U\x0001\x0004ß¨ê¶5¿E}¥æ·ú©R\x001fpJ,Ç³t\x0004õ\x0001L½\x0019&íuô\x000c3Ùl\x000e\x0014çæ\x000eE¤ü£åµ}f+ÊälM©²AÌÃÜT\x0004tR\x0004L»QÖ<=ù\x0007;ªgÏ®¿þðÓíÍýÉ\x001eh-ÏI`ú§Èµ\x0018P<yÄxàîh\x0005í³\x001f.^üíéåÕ^\x0010k¸\x0011¡M	ômQð\x0005\x000c1r7\x0017\x0001Ô5@½Y:²V\x001b¤Æ2®CÈ¾)f\x001dhjf3D¢äaÆ\x0007®ãK\x0019?Ó\\x0001´5@»\x0019 ês~hðË<y.åK\x000fYú\x001cD5\x0011º\x001a¡Ûz"k
ä^zêf2åÌ¸\x0010}
Ño¨4Ç®I1S±hâ\x0018\x000f+[!\x001abØ\x000cv^3Ä\x00149~Cé
Iñë7¹\x0010c
1n\x0018½ïbð$_\x0013q@\x0014)\x001eö·B¬+ÀªT7ÑT&'ócº\x000eáôÃw\x0011Z¿²Ù±Ð0\x0003Q+	#+cmÄs2±ñ,°Õµ$Ë-ï\x0010T¶ql·A`éEb\x0014ac·a»áÎTb\x0018\x0003«tÉpªÇ
clL7l¶Ý>\x0005<\x0015ªµ\x0017³cÓTð0ÆÆxÃvë
F0"\x0011å\x0016\x000foMQêc-\x001e\x001b16Ö\x001b6oÚNÃ½zÚ '¥2\x000c4\x0008:\x000c±±Þ°Ù|G'1¥\x001cÎz\x0014J\x000cûihÌ7l¶ß>ù\x0015¯Y¥'%å\x000bÑâ°ÁÆ~ãfû\x001d\72¢Häµé.jÁ\x0008ãrÄÆãf\x0003îS\x0006Í\x0001¶6/\x001b¢Y4iwx¤ïh#Ä63Øl¿a¦É\x0004¥²«vNZ\x001e\x0001\x000fu16É\x0001nÎ\x000e\x001c­ofÉ«qG\x0001þ°Ïb3ÆÆËàf/\x00130P¥nÁ&÷Ë&9j	¿AëaëÁÍ^fÝÍrdËR	'híÞ(ÄÆÉàf'\x0013â\x0008U^ïÄ\x0008A0R\x0015y\x0014cãdp³q¨8Ñ¢:\x000f\x001b\x001eme¾\x0010ÂxüÁÍN¶Tq4 c;¼wfñÃ\x0008\x001b\x0017]¥h\x000f:hnqH«\x0012}jØ|ëÆÅèÍ.vÅõ^jÞ9(Sb\x001a­\x001b\x0016£n<Þìa¬¥ ;KÑILN\x0010Çn\x001cÞì`h'f):[ËÉ\x0007ÊUtÇ:H7Bll·Þl»=*¦¹Ð4,Åâ\x0013ø0.ÅÆ.êÍvÑ+_ ú<è z(6g<ÐÍÑm\x000eÑÖC,\x0018¹aÎÈÃ\x0010ÙÅa1F£Íf¦é9±:>H.h\x000c\x0014\x0017xØXµ\x0019c£0f³Â\x0010}	Ï eäb­\x000eÅx\x001fAØ±­nÖ\x0018§¡DdDü!Zc2ÞÃA£i4ÆlÖ¿\x0000¢mn£Ý~\x001bÿ\x0002Íe´/£
A':Å\x0014*+µç¶q¼0oËh7_F
%X)·\x000e\x0012I\x000c&áHÂ6Ñn¾4ÈæDFê\x0012èe\x0018\x001dâaKÉfý¶í·µJh^4\x001boäm\x0006p¡\x0011\x001a\x0003è\x001auqÕÅêé§\x0017òÐF
Ðñ°ïe3ÆF_Üv}Ñ¦Æè\x0018£I:¤dx\x0014c£/n»¾`1Aä¾{DÉ¦Q
'Ó®}'Ú®.) ,0R#-\x0010Ç3U×¨Û®.àò\x001eÂÈû]\x0013F\x0015F\x000f'\x0007¾Q\x0018¿]a\x0014
Õ¤¦F¬\x000c±Ä:Ñ\x000f«oÔÅoV\x0017\x0013¼¤ÒÉ\x0001r\x0012\x0008.º¿\x0017È|Û°dü»!®Õ¾Z9ê#ÏcÌ´}É\x0011ê]Ö?^¡÷j\x001fj:óíP
Í8²P#·÷*\x0008;xØÞ¶½êx Tì@d&Ãq\x001aè¹ó^®(\x000e\x0015\x0001ê½wù\x0007ÔÜñô×ß®?~\vüíæþCÂHK³?|º}\x0018¨E¢Â4<Pà¸?\x0001ÐY--ç±\x0001úôù«×¯E"»¼zÒì\x0017o>\x000e\x0017k¸Ø	×ñ0îÂ*
ÀXÆoTÛ~4V×hu?ÚÌâ±ô£»\x00027H?º%\SÃ5½w\x0001Èiæö~8Ï
rhKw?¶íH\x0003hmÖv¢¥16n\x0016¦Q'n\x0016VÒ¬\x001eö\x0008ñ\x0006àº\x001a®ëKïÜg;h\x0008ïB`N<\x0015l\x001bôÀõûvÁïöaÖû\x001e¦~1Ôu	Xtñû¥À"Âc\x001b*`X\x0003;¶íêaÎÀõKÇWN\x0017ê\x000c\x000c	å\x0006`º\x0006¦¿ Ù\x001aÝ\x0004,\x0016N;ÚkÄ\x0012Cy\x0012Ñ\x001a$æj`ÇVm=H¯¤\x0014,u1\x0003Ó¯\x0008¡9Ò@³\x0001¯qù-¸\x0000ù	^A¼ØY/,ûêH5w\x0003®Xã[péP\x0008L\x0000ra\x000fiC°¨¡¬ÈX¨\x0012c\x0012uK\x001de|÷mQJ¤,º\x0001YkÆ¶Ø1\x0008Z:\x0011\&ÐÎ\x001c^®°Ý\x001c	i7 kì\x0018l1d@>/s \x001cÆðië\x001f´ìl@Ö\x00182ØbÉ\x0010ô\x0007\x0012¿¬Éc¡d¦)\x0019:MÓ ;¶CðáÓÄB%\x001a½Ðsz+\x001a ÃáTÚ\x0016d-FviGu¬Qø·Â\x0015w\x001bf\x0003²ÆÈÂ\x0016+K&u3ùNË,v±æ±Rû\x0006d-vVC±ÿL[¶gQÇ4xØ¿\x0005Yh\x001dÛ®ø ÌL	2h÷¯Éº\x0019\x000cOOn\x001eæl\x001b5.\x0000¶ø\x0000­ÔÞ\\x0002,3']§FãÕÀÆ\x0007à\x0016\x001f@§ÉÏñTPgâ¼¨¥çKûÃÇ-È\x001a\x001f[|¶WÌ¬Ø³\x0018
mþXÈm,»Å\x0007hÌz-öî_á\x001b:ÍÆ\x0007à\x0016\x001f@\x0003pFÚ ¿\x0017'dYÖÀv¤
È\x001a\x001f[|6îÜpM\x000b[²=RNÑÖ\x000f]³Æ\x0005à\x0016\x0017@#ÌqL\x0013ñÈ\x0012\x0013\x0002.}¬\x0005w\x0003°ÆÎâ¦xöÏT['[ò¹R&[ÒéÒÑÆ0Í	J\x0014|Ð)8³\x0003\x001bÉß¯ ]]J`Y5-±ädÚU#¡?,Ï\x000boß£°«!Ñ\x0003\x001bËÉB`(fL;}à.W#Ò5"½\x001e\x0011\x0016
rât\x0016ZÃ\x001d§óa÷ÐjH¦dVC2e¸ÅRÃ9+Ìøþp`5$[C²ë¯\x0012JY 1oi÷K\x000e,ÖjD®FäV#òºÐQ&p&[\x0004§´PªÃ|m5$_Còë!²2\x000cQ\x0002\x001b§ªÝvýú\x0016jHaýUªâÓ(«Á¬\x0014Ä ö r^
)ÖâjHôôÊi\x0001fd¶V^
\x001e>±¯ET§ÿ¦¤ÿk ¡ôÑ»¤{¼Ì ®GÌ÷jL­í^o¼ÿÄË\x0004ñõÖ\x001bËK"SX-Ý\x0007)Që?»ÆVÂzc	V\x001aºiC\x000fËÉð3\x001eöÅ¯ÔX&Xo¬5b\x0008æ¢ 
;`ÝÉîÃ­­×­_}{}j>;¤\x0010Åó{HºäÜkìAÈÔ|86tsöìâìÛ«SÃÙv¿\x001cnm½_ýq`)Õ*4[$iyKp\x000c~[\x001aÙ\x0004Ì\x0015jÁ\x0014¦cd` ì}êX\x000bÆz`¶\x0006f7\x001d¥£\x0005$×-òëJ>Ø\x000b¯Û1®ÒÕ¸\Ëm\x0012\x000f)ÅáNl¯
U¤#Í\x0016ë\x001aXøÅ\x001aXÜt9	Ò]¢>|åÕÏ\x001ckZ\x000bZc±ÍZD\x000e\x001ct¤¾=¹b^¨
!(eUÚµ¶f;~\x001cYÀ\x000bc¨¼Ì¯æ)e\x0003¡-òCv¬*\x0006Úª\x0018¸\x0002E\x0005¼ñaYº¹°eqCÙñù\x0015 \Ø³ú)\x0017¯¦\x000f^ÿvwÿé$¥D°\x0003RÉ[¸oãäî\x0008\x001cµn¼~õòêÍÉ®°gõ\x00130Ü\x0002
\x000c¾´j\x0008·g,ìGØ±¶\x0000Ó50½\x0001\x0018Q\x0004#·9X!\x001d\x0005Ùø§|tG»}×â25.³é$ì\x001dH÷AlE,Í"úB®Çek\v¼Ð\x0017Â\x0014W\x0000Ó(\x001aîcJq=Úa·\x0016«¹-\x0002K=	+st	°\}8ä'Ü\x0002Ì×Àü\x0016¥\x0007\x0018â\x0002x2\x0015²õfµ®~¨MW\x001f©óÄ1ã\x001fä®\x000eUH¯R8t±\x0006\x0016·\x0000KÞc×àPØ¸©IEÍQ\x0011\x001a\x0015·ß¦¨Ø"j1cþÈkÞ\x0006`­Ýßbø!ÏeÒ(%üjÔe_H£öl®EÖ\x0018~ØbùÆ[·\x0011u®Ü$9qIþ\x001bl\x000b°ÆðÃ&Ëï5± ."\x0003/Àhµ\x0003Ì\x001fo
_¬1ý°ÅöÓÆ	\x00060\,LG[Á×âj,,l1±´C$0IË\x000fP\x0018$\x000f)ü¶àjì\x0018l2d^Váê -\x0013Û¤\x0014Â4\x001aÒê\x0007¹ÀMæÂ$<ÀÒT9Å\8?\x0014¹¶ÝüeÝí»Âeâ¼Îiä2Ç4}±ß'\x001fó|ìýã»ôµ\x001cù¤ÿFà\x0008#yl0¼ùHç±}z\x0002ª~ÈÞqp¬@¥¬0¦\x0007Yj\x0017yÖSÓ«Ùan\x0005*Ø«ÓuÙ½Ç>¿ûüþö\x0003§#Oè\x000f\x001f?¦\x000e´ÜaìM8Kô\x000fÆ\x001baaL\x0017îÈ»Ôóß?{ú\x0013'ô×¯W`65fÓ\x00194W7´\x0007[¨7å-MYd_L7hWvý \x000b3ö)ÏbßA¡\x001eKZ\x001fÙ]Ô
:Ô C7èen5KÚQë'3\x0000\x0007¡l´ÇxxzA×Åy¨{ó6£vRN*hxU\x000fh§8|¶úH1g;jû7VõÖg·ïß\½A~è¤-\x0007<`\x0016Av\x0007DwäE8A{úìÙ
PXÂõ R¸Åõûeo ïPª¬rñÇÖD­\x0004ejPf¤Lú")X\x0006¡²¤ lç9ÆË¹\x0016«A¹
 ,Ïñ/\¦rx²SÆ\x001cKi×B
5¤°\x001e\x0001i %KÎm\x0014ôª×
ªÎ°ÊV òõhjùô´\x000cÔAÛª¹ç°á¢[ÃeU°Z\x0016ÉEé}SÑ\x001f\x001b\x0002[\x000bª¹ç°á¢\x0013\x000b$ïyrF\x0006¾È1ª`ûµ\x000f\x000e\x001bnº\x000be½\x0013½ìçrjt²Å!E4GBÒGQùýÕI~YTfM6\x0010\x0017jé/\x0003êýäG\x0018/³)Mh\x001ck4Y=æ÷7\x0015ù¼©¨\x0003+Jøl \x0008£>qâ
õÞÞäs7Vl°b\x001fV^G:wyusºl©ÇÏ¶b5
Vó\x0005c¥¿¥Âºü¥=\x0017ÖB¡2¹¡¸6¥ëJáà}
ûÉTPÍH_~ª¸¿ù£¢j_\x0000ÇD04\x001a"!«\x000b\x000fÜÖåÝâêò\x0007BzêAÅïEPé\x000c7¨ï>'ÀN²/³ÑY].\x000fÉ\x0016î\x0007`¿û>a}sUña\x000f·âKWSN;ÉS\x0018#@ð\x001d{]Ù\x0006O×ðôFx¦føUòè\x000f²&\x0000Òa\x001fõ9[\x0000\x001a Ù
0:1ï\x0018°ÀqC\x001d+ n\x0003èjn³\x0004
³0`5¥]»Ô±× mð|
ÏogðB\x0012\x0011v\x001bU°cµ\x000fõ\x0002¬\x0007\x0018ja+@ï¤\x000b\x0004¨ò;\x001feÆE£\x0000+×M\x0016FmEèÊä×¯ .\x0004\x000cÇ$«\x0011Â¾
jõë»Ûg?ýÿù¿.î¾ùðé\x0004Èô\x001f0-EDNx+eW^Ê'
\x0000|ýòéë³¿]\}{ùâÍã0±\x001d0=\x0015ÅLIæ\x0017Ò\x001a/ÑäoÛaê\x001a¦î¦u²»\x001e`CdBsÚ#fq3L[Ã´=0S<éYÉÏ0Jô\x0005å±:ØF®\x0006é:@&t\Ò¦(áA3ÆJ^zlsòf¾é{nfÉ»ÅA\x0017È MfTÏ\x001dG\x0019k±K<9é\x0005¦Ò\x°F\x001eù£>Üê³\x0019em.BÜ\x0006)Æå¦Kz3f-W¥\x0014¡¼\x0013lÙÚÌ\x001e£é<èÑ\x0001ï8-ÑÄÃý>Ûq6F\x0013º¬&\x0002=êe&Ý3³¥)\x001b D¹q6æ\x0008zì\x0011\x0011<óºVzÏö¨\x0014
\x001eEx}ÿîæ·\x0007á5\x0008º,QðTÃ^ðQ¬Æ¬:\x0014Kt8]²]¡Á\x0019:p\x0012S\x0016ZJ\x001a($5\x0011<nÙ"è±E4VÁ§b8dÚC¡H£ÝÕã\x0012\x001b[=¶è¯&6¶\x0008{l¥_ÉP\x000f14\x0016Ôco«q¶\x0001\-úKÄi\x001aæKÙXLì±ÖÉê6z=/ôÙB\x0010N=\x001e©ß³1IØcRöPv5\x0007Ë}	IÙËíD\x0018Ç©\x001be×]ÊnÄGªæm´å±\x0008ÇµH·ùEOa¬*üHA"wØM\x000eàlM7Z¤{´^­m(\x0001\x0012rêk¤'Òÿd\x0018g£FºG÷\x001c\x0015¼ç$\x001f\x000fE&Àl\x0002\x0010Ý\x0013$ç"Mà6­\x0014nc1J\x0013]7îI¨ÁÂrÆæ\x0005+'íQÉ\x0015{vÝ\x0018%ÝcR¦FÕ\x0018Q¢À}?E×ñÈZ­õ0Ý~uÚùÊÌÍÇ³«»­mDXxEs?¯c-\x0002°A\x001a\x001aí\x0011R^\x0001zùúìêåëG9\x0012÷KÕÎ\x001fÔgÖ\x0014\x0019[iXDEË\x0014Ø,¬ºÆºoCW
Ö\x0003ú/M5)áàÖrÔr¸S^i\x0013XSÝ·¤+ÁRû¯läsn\x001eÌÝ\x001dc¬ïjk¨ûÆt=TÍËy­åÕÐ\x0010D±¼:Ú«ÔÕÕX÷-êJ¬&pEQ§?qy\x0008Ge°ÆÎº\x0003¾\x0006»oW×µLìAK}h¥8Hä7
5Ø}ãºö\x0016\x0004i*\x000eË&øå\x0016ýà'²»\x001aé\x0003I=Ã5Ìý$t=LÙcn\x001cïñÉ¤ûÜÈ~¤A¡G¦ÐºN_\x0010#¯]ö^3Zô¶´\x001eÏ¹\x0000ÐWè´¯-XnZlÀÎÑ-hÖAíi\x001dZ­cê¤\ +ÅÑK\x0014è¼c¶ ±\x0004Ði
läLEÓ'îbE(óGiÞ:À6*vPèY	ô±u´\x0012=ûY\x0014ÉÒdñ\x000c°Ø¨ØA\x001de%XÚjÉ­¶\x001a¥o\x0001­Ù6ÎBÛè\x0018öê\x0018È\x0007Ã/b)ÜåíÖO²\x0008ØèØAµb¥¡É\x0004P:i\x0013Å\x0008Kk­r"Zs"\x001fÜf\x0010ÚIÅ(TK[­\x0018û\x0007T¼5\x0005S¦vÓ÷\x0005\x0008û}7ä\x0014'h(q\x0017¶çÝÊUï\x001b1ï?<;hoÝ¾½¹¿þt{÷ád
i\x0000ÓÕ`¦\x0001,lÊ\x001c¡*[ÞÆ=ýúòêâÍÓ/\x001e\x00075HÜ\x000eÒ\x0018Z{ L£¼@\x0002õëÔ5HÝ!I#}\x00104ÍÈC,h)R\x001d{&Ý\x000cÒÔ M$\x0015w»\x001ecbýgú¡1ö- m
ÒvHÒc¢5\x001d8±tY\x001ea¶Ü\x000cÒÕ ]$@,%+âÕ¶Õ\x001a¶ô5Hß!I[J È²\x000c\x0014Îã£
\x00061\x001acè\x0010d\x0010æ1H*äe/]ÓG¼ýVuû;ìu\x0010­>ní$ù¥\x0019Á"Éq;	(¡CZvZëHËQØP¢\x0014\x0002N±æ?~º¹o-:ý`³DK¥_«t\x0005XËMY<ø@cà6¬K÷ñËÁêö]¹\x0013WþÏ7×\x001fÎ.ÞÞ_ÿrýëÙ«»Ï¿]ßl(ò)@bË	Òþ(uôxø\x0006ùÏ\x0017/Î.¾¾ºøîâùÙ«ß¿º¸:YUuû\x001eÝGß\x001avx.X#-3ÐÈ\x0018\x000f'¨úÀê\x001a¬î\x0003²=#
òXî¼0§.m"SÀ\x001a¬é\x0003KMFÇ\x0014tÙ\x001ddYà²£n
X[µÕÂNÔéü¨â\Ð\x0002ÖL\x0002ëj°®\x0013¬¥!Ûìõw
æQÀÂ¡!è\x0003ëk°¾\x000f,qä\x000bØÒàU\x0000Ôá\x0018e\x001fÖPc
}Xw¨4\x0005ÄËÙ]8u8$Ø\x00076Ö`c\x001fX0<\x000blPi\x001ePMÎEH7ú]`ë°Å°e³hAfå¨\x001c(\x0015\x0002E$Á}`[ÿÕéÀ°$ÑTÏ
`´\x0013¬}h\x001b\x000f\x0006.L\x0003½ZÊ(\x0010oÂt:p8\x001cÙ¶qaÐçÃ¨C\x0016x\x0014\x0003tæØ¦\x0016YY²ÒªIh\x001b\x001f\x0006N,oNÊ²µ\BI²-\x001eHô¦ m\x0018ôy1Âmf+F\x0008Ò\x0007dËÎ\x0003uØØ\x0007¶qbÐéÅÀz
Md[¶_;°8IÉ\x001a/\x0006}nÌ;%Ý\x000c^z­*sh÷mÜ\x0018tú1ÚæË=p¬c±^úpÃD\x001fÚÆA#ó	\x0013àL\x0019÷%[\x0014¾_uäíµ\x000b-6\x000cû\x001c÷eG\x0006¡åZ¥µÂâ¬¬#[l<\x0019öy²\x0014\x0013\x0016OfÒL\x0008â\x001bÜ,Ù¶¹X'óZSyhAk\x000bª\x0004W\x001d>Á\x001eÅúÐc±Ûnqå¹e3PEïWY¬*oÓ\x0005¦=¤äéiãÁ°Ï¥T¶LÆYb+QÂPç`mü\x0017vú/(KÇMY·h\x000eDnë!wA\x001fÚÆa\x0003ó¼Æ.+w5ÒlM¹­sâolü\x0017öù/GD¨6iY\x0006kQ<T9ÀÆaÿò)èæ:\x0007Ú -yÆÉê\x001aå\x000fQúÐ6þ\x000bûü\x0017Í«D~Î°>o\x001b¤\x0010[ÌÖa£S\x0017ZÝø/Ýç¿\Ô²MVíj\x001e¯±e÷HóP\x001fÚÆé>ÿå\x001c°ËÙb\x0011Læ«pØÝ¶ñ_ºÏ-K¬d»b¢Ñ%o\x000c-¯}hÛbb\x0013sÚË4ô&oÓJ{	
\x000eÛû°6^L÷y1ç\x000c]a
ÀD² T\x0008s,nüîóc´Ji¹h\é°µE±_ÊHºqcºÏ9\x000bòôE`®HS\x0005ì\x001c7¦\x001b7¦ûÜ
Q¸o¨åï´\x0018¯\x0014!Lº\x0006\x001bÓ}nÌ\x0011g5+X>ÍthÜAL¡s\x0002EÝ¸1ÝçÆl°ÅéÆ¢bz\x0007öpi\x0017XÓx1ÓéÅÐ\x0016/F<×¢aü^ÐN
¾LãÅL\x0017³\x0014ÄD~¹\x0003)u \x0000ì\x0014}h\x001b/f:½*Ob\x0018Tè4ÊN 2Æ>'F3;­\x0017í;Ä2ª(.\x0017ì!3I\x001fÚöI¬ÏY\x001fÄ"$ï%\x000fx\x0018¥ó\x0005àpÁf\x001fÚÆ3>Ï`÷R3ÚÈ5/ô²ûZ7çm­é3¶Ôe":FK¶=ë\x0018È­\x0014(ÚÆ|Ù>óµlq7\x000cVKî4Ln-ñ-NAÛ\x0018\x0004Ûg\x0010¬Ñ2f¨Á\x0015ó%Tcp7 \x000flsimß¥5É\x001d(,\x0006¡pQÅb\x000fÆkH¶¹°¶ïÂ\x001a`¶õe¬åé8y´\x00018»ÙY¢mO2­tl®%-m'Rö¼<lÌ\x001eNHvFáû µí\x0005M\¥Û08~8eP»Àæp\x0016­³\x0004¶\x000f\x001a»A{åÝÉ*bAÉ\x0015A¸InM¹\x001f¯kÈî«ëîþ	é;E\x0019OY[áÏù\x0012ù|÷m\x001f^SXR#ï=¤\x0016RÃÃmp\x0011Ùþ¥0Ø{)Ü!S)&ìÈ,7¹°\x0000®ðCü(û+ l³\x0002ê¯ïºýp2¤\x0014\x0007xá\x0006u¥0#¥pÄ¥ÿÉ¡ùË×gÿ|qõ·§/Nî$Ü_\x0002e%PCs1Ðø¢\x0014?eÄ\x0017ïCXL×Èô&¡9+÷Ö-qÛQ5PÁ\x001c\x0019ÚÌÖÈì&dÚ\x0005¢å<¾ítñ%
:º¥g-4h Á&lU
FË9±6¦t\x0014Ãá\x001bÜ:lj\[í& ¿æ:^\x001aßd\x0019Zf\x001dÏ*#GØ .Íô£\x001f\x0016¾ã\x00074TíOg«="Ñ5Ø,óÆ\x0018äÍÙ(3¹æ°Ø³\x0007îQÙ\x001aùòð¹\x001aÛOË\x0002\x0006ÚãÄÏAÙã\x001fh¸_\x000f0Ô\x0000C\x0000£H°\x0014uÌÝ\x001b÷ÀÐÂjxU7Ú§Á\\x0005\x0018Áf%
\x001cÅ`\x0014àÞzåÛnëÿfVï{Z]{ÚËwwïOR?{ã\x000bÛn
¹±Ö¢XË\x001dß\x0006vùäå³Ã\\x000cL×Àô\x0016`\x000e\x0008"m6Ë¶à:¾Öí\x0011XoSRÑÈëëô\x0003×³³o\x0013²××·\x001f>-ÔÃÈ¬¡4¡ç\x000c\x0016\x000f\x0014^ÆÆÏ>»<û6Á{}ñôÅ%z\x001c\x001eÖðp+</Ä3ÎìÐÉ\x0014o-\x001fc\x0007:]£ÓÛÐ%g*h¸.L\x0001rá´l¾\x000et¦Fg6¢ÃÒE§¼\x0018RÂ¾hGáÙ\x001aÝ*<\x0006Ú	,ð@"¼ýýM\x001dð\
ÏmgÌnÝ\x0007ÊX«rÂÌdÝ¨^ø\x001aßª\x00172Àj Y:_\x0014Ñµa{\x0007¸P\x000b\x001bEòÈ#c\x00189\x001bKIXá´8*»XÃ\x001báydötñ$*ÝéÞjm	\x0004²AVÛà¡ÒD\x0014kB\x0010T±.
-´þb£ÃX\x0002¬\x0016^è`@Å8®q\x0017°Ñ_`²y\\x0008 |\x0016x#¢/\x0013V{o¶\x001dø\x001a\x0001\x001b=\x0006*/KÖÉá\x0016¦YÓæ\x001dø\x001a\x0001\x001b}\x0006&«ÇFyÙEÈl	J\x001cG\x001c×¸\x000cØè30åÛLç\x0008Ê\x0016Ý\x0005/DÔ;zý\x001a\x0001\x001b\x00065q/YÊÝ\x000bû\x000c8\x0008Bh \x000e|×n\x0003³Ê
\x0011.²Iµã\x001b\x001dø\x001aË\x000c\x001bM3õ´	\x0011355±üÊfæ0j±±}¸ÑöýiðR$eöS\x001fsÈG)Ú7w\x001f>%¬'7cÒò4~Kõ@£\x0004ËfL\x001bå-õHkØÝrµo^¾xPÌÕÌ~éÑ\x001c2â­\x0005E®:Yí¥-\x00016²c*ù\x00132Û\x0000ë\x001að\x0001¥ÌZÀÖÈ¨\x000e­!õ,á \x0017à\x000f[Bz\x0001\x001að\x0001ÓØJÀ´e,g*Æð4¯f\x0001ã
®xkv{sÈnÿ\x0005\x0002n®ð\x0001üJÀ:Ð\x000bZ\x0006L4y°\x0000ÖGûA«#×NÀ¦\x0001|À¸\x00160\x0015c\x0019pÌ¼HÔn!/úÈ\o/àæ
\x001fP¶¯\x0005ìR¢ÃÏDæ²ô\x000ebL\x001eG\x0010[´g\x0013bl.ñ\x0001-úZÄ>8:³Èo\x0018QÉ8Iëµ	°n\x0000\x001fP;¯\x00161hÚî¶\x0000v:ï+Æ2"î¾HÆî\x0004×ßFÏÑ\x0014#\x0017ïqÈæ´ÒZ\x0010í\x0010û¤||gòO_gÁ\x0006µ\x000f;¸^Ü:êÒa\x0002oïÄÒR\x0001\x001e\x0014Í{ÍÜ\x0001ð~'k\x0017¹.gèÅÉ²µ.ä\x000bÇ\x0005îRÄfÚÝl\x0017¿Zþ¼@Þ\x0005lg__ÿöéöã#[ÄPú3\x001d!J­ÜûR^\x000fMÇ.l;ûúâÕ§¯Oìz«Ô~)V-¥Ø'¿Üü~söÃÝ\x001f§6\x0001ÒÖü
«5mÍüQñ"@Ôm­éÉw?\]ýðòï_½»þéúã§ûò\x000f\x000b"øñWüíÝü\x001bc"$Ï¯o?Þ}øxvqÿÓÍ\x000fé\x000fKÁ\x001aÙ]ÃWÏï>ÿW&YÙý!\x0018b÷ÉûÆ/ôyþ+{®<rhæê\x0011	ÛóßÿËË\x0017_=¿xúúå×g\x0017W»|ñ"ýáÁòu0ý
Ø0¹¥PG\x0003HÂ[\x0010æ\x0019\x0013\x0002¸düc\x0000ÓeÖý\x0000õ2z^\x0000B\x0006Þ0\x000c#LQ\x0019@\x00182£WB¨,RF\x0018Xy\x0014n\x000c`:\x0004Û\x000fFõ
¾¤È\x000b>°¡àsÃ\x0000ÓßàÆ\x0000BFhÂ0'þ	an¤\x0018C\x000eÁ÷#T17Ø\x000c#lB\x0008´\x0011ÚñCN÷8ô#\x0004î®&\x0019.ÝÀ\x000cUîìrÔU;~Êñ+*\x0017w"ô1äð\x0010.O\x000c\x000e\x0005á(@Jè_Ý\x0008S&!´Jy\x0019!È)ëè`\x000c"9~BA±\x0015ËnÊ\x0005¢ó¢*zé¢\x001fÜ	ô»\x00148æwä\x00041å¡É¸fNì¡aBcèw*Þû\¨%ú\x001cù mÞûNR\¨äÆ ¦¿\x0001ú½éÏ\x0004Ñ/oTY(wÑ#LÇ\x0000ýnåÏ\x0013âõÍ/þ©Â¯\x000fïn\x0013´³«»Ïèßÿ¸^Ú,\x001eÁh\x0015Ñ¯;V\x0017\¦R	#nSðPûæ\x0017O&lgW/¿Cÿþ÷\x0007\x001b.\x001a9\x0002ë\x0006i5ñP§Ã2\x001aA;Pe\x0012#GÄv3Pæ0¬_ÖdHe\x0003m4'Q&·#¡bp\x0013@æH¬\x001b¤Q:¿NÒ.WKa\x0019VF3Hma\x0002Ê\x001cõö\x000f²¥È±\x0012u\x0014Qj;\x0001eÉ¾ôkã²~Yz\x001f|IË&EÚH\x0015\x0000' Ì±Yÿ½ô:?\x001d%Y\x0012Kñ¢<¨5\x0019%ÔE7Ê\x001cõË22ýH¥ò\x0014¬-²ä<ß\x0011ãÀ{)AZ7LRB¾ªK\x0011´.\x00173\x0013Âä@­\x001b¦663ú¤3øHQÂ]åp\x0006JÕúé ³¿\x001aZôDÂ03\x0011S!ê	J.áZ¿,S 	ì|pyz]déb±3.&Glý²ô Ñ	jì,sçNeîÉ\x001aEÉQ[¿,\x0011[äiNÎ¶cD'õ\x00005\x0003fºÜ0ä~¨Ñ('´49¬Cv?\%MZîÍ\x0004WN=\x00000âZT;GÁËÂ¯%â@±ì3BLzö\x0011\x0007D\x00162CÛ2\x0017\x0005
DÙÆwSÍp@Ô±\x0000#\x001eÈPO\x000c\åCW¦Y\x0019GI/R8â¼b>×äÖóÈÈ"L9s
?&9qÄ´§\ö\x000c-00c6íFçGÊ\x0004Óâ3'þ0\x001c±\x001emf5I01\x0001]`È¾T£Ça&[#ö¶õ¸l6ij=\x0017)±\\x0002LÂM0Ôª#özVJn\x0001¬A>òB\x0019áÜ\x000ci¦OÅ\x0011{´H3ßM¤:\x0002\x001f:\x0013m85!Ít¿qÄ\x001e-¾«ª´\(¯\x0002B\x0008\x00134\x0004ôH¨iÒªóËä_N{µ\x001cº`6\x000eJ\x0004qF+	\x001c¸³«´åjê	\x00011eÎz$<2ÖI!ÝÙ¬{A\x0019J¨~BBI\x000eB\x000fÅ\x001d.\x000frVK¬IÄe\x0002\x0013gÜÌ¤<zÈ¡\x0007¦Ü£Ä7Åð\x0019¥V\x0004Á\x000caR hFôÇb\x001e\x000fL µ'²\x0005å®L¨ÜIL4fDhÕÂIC\x0005e¯è\x0012\x0011s\x000b\x000f\x0015dÂØÝÍ\x0002YgåIÙ\x0017¼=ÁaÙ©ôdFôÇF/\x000f)6"¿\x0005\x000c¥àÌàþ\x000e3¢?.Åp:\x0007GDòÃÂ¤iia4©(jG\x0014h)Éd
²)\x000bÊï£TdM;=\x0001fú;ì\x00069S®¦µÈ× w9eæÇ\x0019Iåá\x0011
rÙ)\x0013L£iø\x0002Ó:Qt\x0008\x0013î&½XÛ\x0011\x0015r6r_Õc£ õRM°ÄÈj4
Ä|5aÑù\QF*\3ªÔcä4ÈLÝD¼åbã\x0005fTR<ò3|PJ`¾rCåÂ`¥\x0010äyÎÂ3ß`ý\x0004sD¶Âè9=Pñ31^#×3&åQnDÍ	%w\x0019áôÈÌO\x0008ÛS2ð\x001bQs¯x-x.\x001dÀÕ\x000e+7sla&\x001dw#z¾T;rt¤SÐ\x0019XÒ¥¼cÛFP²ïôÿûõF;Åazêp[\x0014	ÅÂ9nýÇëÅ±_á@A\x0011Ð\x0004e\x0004¨Ì\x0013DNÓ3N£¢¸v5!ÓL\x0002Aí¡ãÿKêÎTî\x000fHÕ\x001buÎT-á\x0016¥ò\x0012×Qûí\x0006
\x0002#8µ7rM_º	sÙ+ï~¦
\x0008Ì\x0000ê\x0016\x00005´×¡¤í6vWéPÚ®'\SÇVÊ
Z)\x000f<pK\x001e*B·\x0011íO\x0011þÇåøaèüÿ×"\ì\x0014\x000eÙ©Êê ±75 n*ÎH#\x0001MçAM
/¢>\x0016itÇOõY\x000e©\x0014< 8§i\x0015`~ó¢S\x001açôí"Ò·cÙ¼)É¼\ÞÎÌåU !þÝ*îç{\x0008²Ý=óí|<ûîîþç\x000fkº\x000e-*`Î=ÚA\x0014(MNWSÑè\x0007?\x001c@}ØÏ._}÷òêÛ\x0017'º
+D¹o\x001b"ðÄÁÎO\x0019ÄU¸dn1¼d8ìÆ[ö¶Jb|zhÑ,!.`'	ù~D¹?o£\x0002(é«F\x0017é\x0015mñÈÔQÄFD¹\x0017o³JTyùõ"##ÉË\x001b9û\x0010å¾»­2ÒR¦e/Eä\x001d»\x0005§M¿rÝV\x0011i+ïÙ|\x0016\x0011Y_D\x0014ú¯Qn§Û*"g¤¡jQ}³ R\x0008"#¨67"Ê­s[ed`wlæ"#gªîk$mr[\x0014Ë,
¢Éuíe'2\x0007BNén!I³ÙFHFßrÄC«9C6HÔZ!Ù¨¡\x001b\x0012wm>¸ê*Y¹JèbRì\x0012·m]ÂVn:-W$H`¤CÇ:ßíØ¤gl³,áÈw)f\x0011yµ»HýwÃ6ÈçÕ$"$þ,"\x000f""Ý/"n\x0004Û,"$\x0002,"<g#)³.y7f/"îùÚ*¤ Ï³¯\x0005¿làYd\x0014´\#«»Í¶´wmö$^^Ôimh\x0010O²Óÿ~ß&½\[­¤rlZéól·Ër~\x0000\x0011·mm=6Hø"E\x000e\x0000Ï\x000fÅ¹ÑÎø^HÜ¢µYÝ´TÔ0\x0018ê\x000cÏê&B²¶\x001f\x0011wcmEäB\x001dH|ÀqjÝ\x0006@Z6«[ \x0007º\x001c¸-$\x0004\x000b$y\x0010q&²\x000b\x0011\x0011QèÍw\x001b\x0015Íª²kÓ¤x¶!HÔ\x000cêlDîµÞ|·\x0001ØÅÿàÏ9Ø¶ò´ec¿Ù¦½ozóÕ^<\x0015³\x001dò`þâÜ\qnýÇÄ«7ßí$¤W\x001dä´
Øß:´ãÑ-ÉWo¾Û	£t6Û$-\x0006\x0000Kb\x000b\x001bed»½¾ÿ÷*÷gögÎ|xvñá§û³¯ïîº¹¿¹þ¼ªR¡LÞCL7\x000b¤=B(nIýêG\x001f&ÒxöæìÉgg\x0017/þvuyöõË«¿]^]^|¿\x0006u®\x000f£NQ°\x0012\x0010\x0003·Ô\x0000\x001dÖ©Õ0ê\E ëÒ\x0000KZ_¨},o¿\x001eæ¡Î	²F)a\x0013j@éóq\x001aâDÔ¹\x001a1å^«Xn/÷ºÜ sÁb¨Ì\x0018\x0010¨ç·
(Fµ\x0019¾\x001cF«\x001a\x0013D­Î]	à=?\x001c*·ÓS-H.|L\x0000\x001dJH\¿¢û!Ï\x001dÎ¨\x0016$\x0017GQë\x001895¡Òñ,ji\x0018JÙ\x0007Zê'\x0013dm¥Ó\x00165æB\x0018ÉZºIq\x0013e-5)÷_ÄÐ ?ßÐÅ\x0016×hëÚÔ0l®ÃL¸#Zb0\x001f½LY8\x0013gÞ\x0011.ÕL@m¥ÿ\x0011M Ð2\x000b»$ou'Ï0j®æL@­Î­JÈDrI®Ö\x0013asÑç\x001fLØ\\x0017\x001aG\x0012EÆ"}t<vIãéGÒéaØ\ªù\x0007MÂ8#1ø¥Ü\x0016Ô\x0002Øn©/óK\x0007r$¥T)½\x000cÇ$Êþt¯#\x0001Ý½º¿¾þã8D
\x0003.~}ûþö×»\x000f¾
´ëMÎbBi-æ
ß)DÕm¥áìÕÕÅÅß\x001fDô«ýõÃ¯Ôï°wn?~¼ùõæÃ§³÷)s}óËÍ¯w·k2W\x0015¢?\x000fûP2,\x0017E>4ÉôË7O_¿¾|~ùâÍ\x0019å±o¾»|þòé	
\x001dR~\x000fý\x0007@Ê¯ÿ\x0000HùqðËGZèþ\x0001 ÊÓÝ?\x0000Ty?ëÞ\x0012×£]Ó`òÔ÷¹ºo#Ä\x00158,Ë\x001foô¿ÃþÛ^\x0001+ýÚ÷·\x001fÎ]ÿ~ûóu<+ÝKh.Ó{,«{XÈ¾§|öôÅÙ³\x001f~û íkoWªú2ñíÊ;_\x0010¾wÖÚÿúÏê|¿¹¹ÿUÖ»=¹Iüöÿ÷\x000f`<ðÔêë!)îðïZ\x001dø\x0005U/\x0005¿\x0002óË«ç²ííÉeòâO\x0003_4ô?\x0002Ò\üG@
\x001cÏ-áÜ\x0017\x000bøÿùpó\x0019|SìX:ý\x0008êÿùÿëòÝ/7\x001fn>}Z¡S&¹\x000c\x00164Íõ,9Ó(4»^Õì¹Ó`]>ùîòÅå\x0007éw(ëHóKÄùÇO·¸?Zåè¿¾þãíÍû5&ô
«äÑ\x001bé¾³2W
èêÖþrÞ__üýëËg\x000fbû¯þë\x000fªÅö/w\x001fnÎ~øéóÇO÷·7ïßß}sþg·\x001fÏ^ßýúëÍý\x001aSJÃº°ÈÓQ\x0017ðv\x0008&ûJoëëù/OÏ¾¹ºxñÈ_¿|þüòêAÄÚÿñóÝï)ýßÿï»÷?.Â,X\x001e=mC{!rÌAm3ÖyË)\x0006«çJ/<ûþõ"NþÁCàüïðÓ/õCÔ³ë³\x001fn^w\x0007ô½ç·úÖ	×®
ÒÄo}Ý\x0016T9yWï·oÕO-linÖ\x001b\x001a\x0010ÂÐ\x0018ÐsÆkµaÂPM\x001d 
¨}y\x0006½Å\x0019Y\x0007,ÔÜC´ÀÊõu«¥`ù~XÜ Û\x0001+*n#öPfi\x0019c%w\x0005p\x001baý¢ßÿ\x001a°ÕÑ
fCk\x0012\x000eÝ©ôYDá²Ø
i\x0001¬V¶\x0016\x000f!Qè\x0014_¦Ý\x000fª÷Öo®?¿½û|ÿs^\x0003psöm2¿¿ßÞü¾Ê\x0000{Ú\x0004-F:\!IN\x0000WV4Àa9üï¿~ùýÕ·y/ÀåÙ·É\x0016ÿðôòU¢|\x0003Ößs¾aY¾8eJ\x0011øù$ÅÒHf:¬\x000f|®¿AOú\x0006£9ÇI)X2Õ_1«;\x000b/\x0003_`ê/0¾xóM4hÄ§@ý)ù\x001b¼ú
¶þ\x0006;ë\x001b4ÐÓ)¨ÜHß \x000fµÚ©©ßàêop¾F*ò7,9~®§\x0003?%ê¹àë\x000fð>¨<\x0000ðrú\x0010å\x0013ôagÂÀ7ú\x001bÂ$³\x001a#-S]¾Áï6\x000cXé¶ÑF\x001f¾j\x000c|C¬¿!ÎºHÉJ\\x0008®0\x0007ÁÕ&Ì4«\x0002Ýt\x0010!]
4TÈ\x0007!CùZ»0ó\x001bZ\x0017=ËG§ËùÀ\
JÅ²&`ÝÌmDã£aöAÑÄiþ\x0008/¯â¤µÆ©·©qÒ0ÉK{ÀâÐ1·Ð¥hIèøVSoSã¦aöÖò@\x000bVbe¯\x0004Oi©·©ñÓ0ÉQ{d \x001eÔ|¨w8\x00048õ$\x001a?\x0007\x001cþ\¾A&rÓ7(oðS5¢ñs0ËÑ)Ç\x0005±¤\x0011üÅò\x0011Xl:|Û\x001cøÆÏÁ$Gç"òË§£½;\N¹\x0019o`ãçpsaiÑËßàxÈ×¥Ô(È7
£ÃIÎQ\x0007h\x0004ÐäØibNrtõI4\x000e'9ºä£y=HúÀe\x0001\x0017£Ñò\x00118õ$\x001aû³ì+\x0008\x0015±ó)öËqSÊ)¬\';5ÃÆÀâ$\x0003K¬¥Ý5¶b>	kå:\x0011¯å¼ÐuÒ³¬\x0015*ýô\x0011@\x0011ËG\x0018F¤érà#\x001aë¤'Y'¢ÍÈ½nYÖåòu²\¥ÒçL?¡\x001bë¤gY§\x0014ÁæQYçã²Îr9	-®Îï¿µ}C[*d¬÷ÌZç¨|/S0 ¶IO­\x000fè&
×¢pG-Vl"Ï\x0007©e%+\x001dm\x0003\x001fÑDázR\x0014NÏM\x000ft>ÝG i`uS.Óêe.­y\x000c9â]
.+'áfæCºquz«³ÖçwTG\x000b-M\x0013hq\x0012
}ôø74NÏòtå6%SßáRHh$§sS5¢I%ô¤T6\x0018q^êµÉó£é T±¯05ø3·6³¼uJØ4¥X6¥°Iê~h§æC¦qÖf³¦P>\x0007àwÊ¤ß%\x0008©\x0001i|µä«m%°ÎgK\x001dLÚ£9Òõ<ð\x0011³6³µ¶<¸âÕ ù6ùPk\x0019¾öek³¶É¦\x0002\x000e\ä \x0016XÌëÔhüäçè£W\x001a7ãÞ\x000b~OÆù
3³Ü\J\x001eÄW«b^¥ò\x0011SÏ¡qsf3ÎÉeJÿÊ,CÄ\x0007!í\x0010ÌÔhüäçh\x0011\x0004?I8ßÉá«\x0007)C°3ß·lãçì$?gÆ\x0014ïÑÅZNÂ\x000bm\x0018\x001cÛ\x001eøÆÏÙI~Îøeçò
!³vQ.ÓÜêmüäç.sR\x0017t&RtÎJã\x0000ø¹w©qsv#­ö¬\x0010Ápç@úGé£fÙæøG4~ÎNòs&ù¹Ììá¨y32\x0007~ª³m\x000bÇ¤¤4\x0005E´2iù\x0008ï8~ù\x0008'ôàâÔhµå¬S¨Ä(®<[S#|ù\x0008;3¡³§³<®Ø&Ú½?Â\x0006Ù 	VÏ,\x000f¸ÆI¸INB\x0007/Edg\x0018Xë¥þ
vjsk¼å%¨\x0007­\x0013UÌø#¢\x0010\x000cñ3?×¸	7ÉMèPÞ|i¥
§C´ø#¦æ¥®ñ\x0013nÐqé"_>¢ì²H:!ë\x0017ÀÎÎ5~ÂMò\x0013
°ì'¬¢L'!ã¸`¦Ì\ã'Ü$?AË\x0000\x0015ë\x000414±^Ë"\x00190GæÎ\x0007¾¡ÉÜ¤|H\x001bävºçN¹¤à(^â\x0008ÏÀ'4NÂÍr\x0012¶tÊÑÎ\x0007ÇZ­}ÕG("\x0006>¢IÜ¤tH£¹\x000b\x00077Q%Õ\x0019\x0010Ü¼ð§ó<\x001díÏÌ×é#I÷jÄò\x0011ff.á\x001bOç'y:­\x001cQÆ/\x001f¡\x0002S--.ü
0S«}ãèü$GGq!\x00076	j´7¬\x0012*º!o\x001cäèÐ\x000b+Zú\x0008#¯¥\x0006lZ«ñ£ó\x001c\x001d¦0<oJ.Zq\x001b¯ÓFèU\x0008S?¢qt~£K\x0014ÍRì-µdVÄ\x0011ê h\x0012"?)!\x0002ÚêÈ\x001faTþ´Ð)S\x0011pæ7´}í¼5
\x0005e\x0002FÊ\x001fä¥19@#·é\x0008\x000f\ÿGÆKI^\x0002\x001c0\x0003_rÒ'"\x00175ÈG©Ït¡ñ\x0012a é}1D ³å#d+0\x0015ëfúëÐ¸0ÉMá)\x001bÒLdÂ@ôPzêÌPh¼Dä%À#\x0019¤|\x0010g\x000c\x001cza%VS³¡Ð80ÉI\x0000:\x0019|²*2½C%5ØôË¦^¦ÆIIN\x0002¬¼ùZ\x0011ºt¬úL\x0017\x001a\x001f\x0011&ù\x0008\x0015\x001cïbrª6Ë7·÷Å¬OüÆGI>\x0002â\x000f0y\x001bÎ²à\x0005ä\x000b¦zêÐN>MJè\x0014õ\x000cèÝGð1\x0018éºÌûç}DÐI	²&ïusôHÄí\x0003À6Æ¹ot±ñÔq§VÉ+pÈd´ç\x0002ÇB6¿¡Y¯0þ
£\x001cµ²%ìÓf)\x0014äÀü
!Ìt\x000f±qÓqVÔ1¿À+ª8-Ç\x0010r×h:\x0006¥gzØ¸é8ÉM+K<\x0012ù#tú1(Ãú\x0010üÔçØøé8ÉOÓGp\x0011\x001c\x0017êZþ\x0006Ö §\x000cÅÆMÇInZ¹ Ô´Ä\x001f·\x0000óz²ô\x00118õ16~:ÎòÓ^ø\x0010\x001db\x0014\x001a\x0010@Ë\x001fá½ªÖ£\x001c5¹¹ÌeâÙÖ°eÒN¨VæNH\x0004ÚþÚÆ\x001b×¾]\x0004¬±^L}ÓÜ¦ \x0015\x0017"¦ú4jÍá±w'ÓÊ\x0017Ã{ðq7­<µð·ÿ%\x001e§}
Úx.3/³7:Ê°\x0004m¶\x001a@íJw*´v\x0007f
1\p\x0010\x0012ÀJ\x00102µ?%ª\x000b¦æ}K²UüM$âÜ\x001dAw¿ÚÐfCì¨,nG±àÊ0¶/$\x0011SÝ³]ví\x0002-{\x0015Ræ­Å\x001b"2\x000eª©rp"aÞ(ê|²6¹svì¦\x0014\x0011éØAï
èiâ© Âó´\x001aø¡Þ++#´Z]3ª½^FMº^èÈÃn¼Åp3¿°ò N-:'\x0017ÿvÏÅ¿\x0014o)fÏNÙ,s\x000b¥H\x00058y¬ío÷´}Îg@Ù;ë\x0016¾/.,\x0004_ê;qê;ÆÞµò³®\x0015=\x0016s½Ð¡©¨&-öSoÒ·{Ú1ç8lðRC÷>JìXÚÑnù£ü¼å\x0013\x000e-3/Ø¢×$¦Ãð^ÖÜ¸ ûÕpS±êèg|v?¨=&Êg×g¯nîßýr»áÎ\x0013=f&\x001eÕ\x0008dá. ï8L¹SM=òìâìÕåÕï>Ìo÷ù~g>×äÇÂóïw\x001fÞýûºtZgö
\x000c%)fì8sh&S2kçß_¾xò±\x0017\x001aaø[s°Gìæ#q8~Hÿ/ðÕÝ\x0003,ö5$Ä¦ù¹Ö[zC_Ø/mYÈ\x000eûæáòõÙÂ üNõêåßO«Öõó.ð«¾§³Àèõ%\x001e*ÛÐUkÁúD\x0017É¢ft_º2ë9èªõ_]²KÉ6dhò¼¼\x001fV.àBÜ/\x0017l\x0003Wmùê\x0012\x001dqbj\x0006gx¸=XY¤\x0016\x000eá¶¡«Öyu.¹J7ð(
ÁÊPe8Y_NYÜc¤L?Øi.1+¿º»Ïöäk²Ìw+©À©ÅSóº[¢~ãuA^ùÓEÜ÷*\x000b¹ò«lc\x0016»üò\x0014)xÁ5v\x001cÇnÀÚdì².u³`ë\x001a¶!r/63Á¦¬0ÜËj\x001584½ØMÝL\x00109FYö¦Ó¿°P\x001c2t¿gtC·5t;Aìéz{¹-R>¬5Á\x0001§[7vWcw\x0013Ä®-1g¹k^4\x0015)\x000b/\x000fv0vC÷5t?CìV C²²lªLrRís\x0016öPc\x000f\x0013Än9ijóHZSv\x0013O³1±F\x001egH=rç~zd²\x000b\x001f£.:Kè;\x0012ÉÅ#©\x0019RßÙ\x0018Ïæ1ÐrCúA1¶\x001b{ëM'¸Óe\x0019¦.rweEc(r?zÁ7î\x0014føSj\x000cµº_B
£Ë2àÈ¥\x0017{ãSaS5\x0010U{¹5Àº*{
¦ÞÆ©Â\x000c¯\x0012\x0015³Ûgl\x0019ün\x0007ó~Ñ«\x001bzãTaW5ü<JÄÓÜaä^Ö¿â\x00015P7øÆ«Â\x000c·ê¶"\x0012ÎD]¶\x0004ûY~\x0015\x001a¿
\x0013\x001c«A_À+!<N±4_MÔÖÆ;Á\x0004÷dRÂ«8!þG\x000eg Èýà\x0011´\x0017;6&\x001egxí¥ª@ÊêØ?²:\x0018Ã¬°\x0000\x001b33Ì¤©¶y[\x001e	´OGÀ\x001fÍtol
Î°5\x0016vËêg=\x0010	\x0002×0ëÊc£®8C]\x0007Ùþ\x001e¡$Ö\\x00060éÝ
¾ÑW¡¯Îð¬½G\x0004\x0005HàmY]o¦åN¸«ç:ÁÛ\x0019NC2N\x001eÊêÌ«püø®Åþn\x0002vËO{KDéÙÜhUò§ý\x0002\x0003ð¯[ø×\x0013à+Ë &\x0017ËÂ×¾Ô:f\x0019K°õ\x0005Ç7åÍbð\x0004°øY\x00009â¬\x000e:S7Bò\x001emuØ|v
O®»ýt}ûá¦lüúøéîöýºL\x001e\x0007²«µ!Å÷¹ñ¦¢¹Îìüaë×WOß\<}qÉ»¿^¿yùôÙ
üXãÇ)ø18©¦&\x0013ÉÁ>H\x0012\x000eËÀÊ,üºÆ¯çÈjø\x0011"Ó¼6ËÿÈ\x0008R/~Sã7sä\x001f5°\x0017ù£\x0013èàX!ïßÖøí$ùÇsÌ¬­Âù\x001e-Êý·G\x0006
{ñ»\x001a¿\x001fKÜ@£©|ÿ£¸!º·~ü¾ÆïçàwBä/\x0004b¨}EþG\x0018Æ{ñ\x001aº¯\x0019~ ií\x0005>Ú\x0002¢ù5ü8IüA2-²]¶þNøb£UÓnÿ®\x0012¸x/5I}¡<0;ÇiÉ|²ó¥7¶iø[ï;ÉýzäÙ\x0005¿r{ïkÔÌ<í\x0003\x001a÷\x000bsü¯vJì?QÞrkY,\x0019#±zLûÆÿÂ$\x0007ì=§\x0013Ý	\x0014\x0007l\x000ejáý\x001fÐ8`ãµ	\x0004O£³\x0018ä½PNà\x0018¡gï\x00074\x001e\x0018&¹`ýe\x001bTX©|,K)\x0018÷\x0001\x000bI>8ÒoÜ±¼ØFaßÇh_z? ñÁ0É	§\x000fà²µFÐ\x000b;BÞÞ\x000b¾ñ`0ÉEä¦Po\x0013`ä\x0017Äè%ÓGøÀ:?\x0000\x001b\x001f|@\x0014ò¦ô\x00012\x0019\x0016vuVà#\x0003ü½\x001fÐPcB\x0002^9>@\x0012Ê.\x0006Åy÷\x001f\x001b\x000bs,Q®D\x00114\x001fÁ'P¨Qõãö\x0006q°+¢ä,þzÊ\x001dRÈa¨#ÊÈ¬\x0003Áó3\x000b$Ï3/Öí\x0017èY_P¨£òöÃ!0mJ$\x000f\x001e[6Â[eÛBÄ×é\x0007ËâågOn?ÝlYíþ+Rô´¹lN­\x000b%òiV\x001c_¾>{òôÍå£½\x000bFSc4\x0018]é® 6=v­ÖH}-BÝF¸\x001d£«1ºNT\x0001áVB%ýpÉ
ÇiT5CÔv¡Æ\x0018zÏÚðÔT\x0002fÏC¾)c*r¬÷jlÆXR£\x0005#¥F}\x000c¥§U\x0001)\x000f~±\x001eÜ\x000e±Q\x0019èÕ\x0019Z°Ç÷Q)©6î\x0008HCÔ#g
Î@¯ÒDVrz[\x0006\x0017CÓÞº\x001dd£4Ð«5ÄTîKÞ\x0015Eòä\x0012M=w¼\x001dd£5Ð«6Þ¸RûsÖl+½]\x0011ý ±Ñ\x001aìÕ?\x0017cëi:Õ\x0006§*\x001f¢\x0017ÏÛda7t!±Ñ\x001aìÔ\x001a@ÏÄ\x0010fØÕ8B^pvÄþ`£5Ø«5®ÏÆFk°Sk\x0000<ó zj¹ÊÔ?ÞAé®·nä¸u£6úT\x001bÝ¨îU\x001beËÊ\x001bã©Cv\x0001\x0019EmÌÈYúñ§=¯ýSg%{Ê=;9FÛÅ\x0016=¡2fo" ýÞ\x000c/~¿Iÿ­³ôûßß~8{výûíÊwNHÇì¹\x000e,eM±º4HúZ^üpù"ÅèéOÏ¾8{v±L0<\x0016k´86IUíz·x1´s2{äêªF'X]ÕC¢Õç5\x0005n½\x0011é\x001acµõ(Y'XS5Ý`MDL&%ë Z¥CÜ=yèa´¶Fk\x0007Ð\x0006bGÌÙ\x0005mm÷ùÖ¢çáN\x0000Wï\x0014éDëk´~D¶)çn\x000eÚ2À:¦±$Á¶ÞÉÞ6Öhãlô¿§È}\x0000\x0006%¢Õã×\x0016ZóÕo¿òMàÜÃ{§|é"DFÛ<\x0015u¢m,\x0002ôv×\x0017@\x0003c#Ö#ï@L×V£m\x000c´,Ò\x0019m(6\x0001m\x001bÜ¸é]÷T6¸ï¾p³ KÀêw\x0011\x001aØs¾§­>Ïx)bÈF×Oñg?þÒâýåKÇû¯-ÞýÒñ^·x¯\x0007B\x0006j¶á¶3\x001dxJ>%	²TÇÙñAÿøs÷ç/]¾7-Þ/\x0012ï[4Ðæ_§\x001fPhþloøv
P/[\x0004·\x0017%ÓÄ¾d\x000f¸>Ô³ÄO\x001f\x00075Hì\x0005éC©ñ¦¼[ñ0»Þ½Ú!º\x0006©;A\x0006¥ÎM©ñf6kK+Fq\x000c¤©A^IXú¥ÐÊ 5Ö\x0015n\x0008¥­QÚ^Q¢8x \x001cßÊ ì\x0005Á\x000fÊÒÕ(]÷\x0003írÈ(£\x00188yø\x000eÍÊÄ\x001eÕ©:Y}è\x0007\x001adKñ\x001c°\x000eÈ+7*ì\x0001®¥Ýï-¶Moñë÷k"*\x000f®0BD/õ?Uð\x0011ûáóÝgCÃ\x001a\x001av@Ó^:\x0004Õ¼àÓ§DUzTõÑ\x001eÉUØLÍô`\x00039Wg\x000cmJY°\x0005W°\x001d}{^ÍÕØ\\x00076´2ðÜ\x001dó\x001eút\x0015\x0005\x001b\x001e}U^-ÔØBÏu3ò²é¸é8å¹ûhËÓ\x001a`u¢m»\x0014×"SçÓ­gRB¯\x000c¿\x001eÁr.Ø\x001aE\x000eMpÑ	%\x0006))ðjaìQm\x0016\x001cÐ\x001aôªÐ(\x0000ïï~[\x0015yÑªy1jð¼lb\x0005ÆèA\x001fÖòóÿ÷W/_"àb¤X#Å\x0001¤ºø\x000fÔeZÎX#Ó+F
"Õ5R=4;[@]öUQ¢x\x0018ÎnBjj¤fäô£¼kjUæ¬!sß0·ô µ5RÛ4`y¦¡&pd¤QâEº½cH]Ô 
çÎðé/sðÌ$É\x000cj¯ú\x0001¤)Íü¡^S+\©SÂàõ:Ò&¤¡F\x001a\x0006æYÁ\x001fF¡¡pe^ÓpX©Ýtç\x0016{ªú¡Fôb¦ð>ï¥I¡¸°ú\¶\x0007jkú\x0007lÊ\x000bd74?t\x0007'A¤·0¦üÐ~\x0018°ý1]OÍvÊó.à­\x0010¨øfl«\x0007icúaÀöG-­\x000bãÓ\x001bïü ÒÆôÃí4\x0001\x0001\x000cÕ0[ \x000f¦ cf
\x001aÓ\x000f\x0003¶?Nù¤îûLZ\x0014\x00163ÊHÍéÆ ÂEÔ(kTà­aÇ
ê­\x001b\x0014jl Æ\x0001¡\x0016V\O¬Pu*HÕ1;IÅ~
Ê©GÃÅ¬\x0010ed0\x0005°c¦\x001f\x001b{\x0003ö4¥DñEêhÐ1TÈ\x0006½ÏH ¶±t¿A\x0005 Æk\x0016)D\x000eûS:"|Û¾Ù±Ù\x0003µ±¨ØoQ!9w©
\x001b\x0010RÄ\x0010uÑ©8æ¥°±¨ØoQ\x0001QVF­¸©:)´é\x0004¥Ç?6&\x0015ûM*¤Ü\x0016¨(«¶B²	\x0005*\x000cj\x0013Nc<Rx}®\x000ck¿\x0011>¦ íxþØcç&¤õÇ~ëOËu¥oÙ \x0013ç\x001fË\x001aätþWµ±þØoý\x0013R#OÈÄ"\x0007i\x0017\x001d3Uº±ªºßª\x0002-¡µ¬TvÎ,Jed\x001bp\x0000\x001cDÚ¦ý\x0003(\x0015Ù¦êdþuFªÄP±Ã×òë\x0001åGêÖâÃ§
ê,Ò(cÔ\x0001ÌX}B7*¥\x0007T²=ÏÊ"ë<ð\x001auáû\x0008jôô\x001bÒ\x0003*EÛÌ\x001b§Sh9pi"]\x000c\x001e¬úF¥ÌJýéR5N\x0001rÉû+©¦\x0000ïÛÞ)é,áiÔÊ\x000c¨ÕòðÁét
TÜ\x0012¨Ä`J@°c
êE29§ºî\x000fVAâ\x0017*°{Bòn0ûÇvÇJ\x0002é'Ý\x0000µÄ\x0002\x0007\x0002vÙ-@(U0h¶\x0010\x000f\x0010ã\x0010b\x0008PºôQöÑª\x0012\x0010¨±Ë»·$i)\\x000e\x0000N´D*«¬Z"\x0018§d\x001dÇÁ`\x000bÌ>àôW\x000f]
ed\x000cÒX&C\x000bZæñS\x001a;\x0018\x001e\x001e\x0018d\x000cdÆ\x001c;_Å¥ÌòÌ/t\x0008d\x0004o÷¶l\x000boÕ_®ïßÓ\x0013øÍÙ·×ß¯e{ÒÒGPKlÉ\x0008K´1ÍóÕï.®è1<Áýöâûg'Ç[÷fC\x0015Ï\x000eEa\x0004\x0003¼h4àÛºý
R\x001dhuV uQÆ\x0010h'Gµ>Å²Zd»Ï×ÖÔhÍ\x0008Z+kìÒEPB\x001bä#zA»?-ÜÖÖhí\x0008Zc¹³\x0008 PË/v 5V\x000fu5X7\x00046HG\x0002]\x0004Ëh\x0003:\x0011­Åa´¾FëÐÂd\x000e(\x000b*¼9\x000fköùÇ:Ð\x001am\x0018A\x000bW4%´ S))Ü\x0001A»¿­\x0003m¬ÑÆ/\¶U¿Ý±BõÁUN\x001c/M~ñH¬Gy?°z
³\x0003nëÊ|Ù_!ÝÆÁ7#rÔ ÒU2¦¶4c°t÷×ëvÀmü\x00038\x0008Z3eæ<URO°\x0018ý0ØÆâÂÉ\x0005z\x000bV²_ï¢Ô>-î/2íÛ\\x0018²¹¤]ÈpÕ93\x0006\x0011ÝµÀ\x001dvgÐ\\x0018±¹)a)P¢qà\x000bÎÉ8¿àá66\x0017.â¹¨¥BÃ"[#Ip2bÃh±±¹8bsÁR8ÍVs'sBoa<ÆÅÆæâÍ\x0005/S\x0013 @¨\x001d¼\x000e¾\x0018±q¸m\x00021ds­¦R¦Ur\x0019`kE\x0007Ü&À¡\x0014\x0002Ê[³,Z®tïX\x001cÎ °Éq((ÿó­\x001866\x0017Gl.{XÐ\x0006+î·ÈVa¸\x0015Ã\x0011+¶l.cáÀc)É\x0001K\x000e1\x001eÚèÆ*è\x0011«\x001c\x0000ï\x0011_<\x0004³Ò¸òú`Á\x000fÛ\Ý&ê#j\x0006T\x0006¶
c\x001b'å%«â°	Óé\x0011-#ïë,\x0005!%rNØlúé0ÜFÍôYO\x0018\x0017¸	90G¬\x000cW\x000f[\x0005Ý¨\x001eR3+½]\x0016²9\x0013vhcrÓè\x0019Ò3\x000bòÊ§£Æ\x000cW\x001aw¾¦Q33¤fFI¬ hZY\x00194·+\x0013÷©;à6f\x0014M\x0007záËp\x0015¿õ,mÖ\x000f
¦Ñ33¤g:E_,Ü¤rVÆW-ÈÄý5Ï\x001dp\x001b=3Cz¶*f¸NæÛ\x001d0/CúUû0ÛáÚFÑì¢a\x0019!v=Çä'*\x0014¸ãq£m4Í\x000eiZ\x001bùæ\x0012·iizÌÁäX÷­LØ\x0003Ëò/Ô	Û\x0003Ìv\x00143DáÄI\x0011Ø¹c_¬d
×ìó,÷\x0014EöA\x001b\x0004\x001d´Tú©6â$8\x0012øÚñÀ·¦4ÍYÐõH\x001aÒ\x001cJ,}QÒ é\x000fµ\x0007ëËzRø}9§4~üB]\x0004äF\sÈ}\x0003j\x001f\û\x0010~Ð®§þáîó§\x000bGìEhl;XSö5Ù=ÕËûv~xùý\x0015\x0008±F}\x0008!ý¢D9Þ4¿ÿÚ³	 ®\x0001ê>!E¥\x001b\x000c%¤\x0007£º[\x0000\x001a é\x0003¨D\x0007üi¸[ë÷Ë·\x0010º\x001a¡ëCHÓ)ü¤çQ\x001erhÕ5#û\x0015ÛM\x0008C0t\x001erÐ\x0010"7©¦SVeu\x0007>­ ÕcjÐJÑ«÷×ï\x0004á7wïßÞÜß®âá!ò\x001däégdN&\x0008ÜJ\x0005
ë÷üWÏ.\x0008Îo^~õõåÕÓ\x0015X±Æ\x0003XC²ëL½à\!SF¥dêØÖDÅhuV\x000fI¶t\x001f¤\x000cKhñ¡ð])]ó
v¢55Z3"[åisE&>Óâå!ò~Þ$ÛºÍ§\x0013­­ÑÚ\x0011Ù\x0006/cjàeû\x0004éE¶uöÒÖÕhÝlZÓ²l¼¦T\x000bD¶õ\U'Z_£õC²-ìËDÖÀ`­\x0017°T«\x001f\x0005\x001bj°aHÉ¼/\x001fd}\x0014°Í
øN°±\x0006\x001bGÀÒá³ý¢U=|k-\x000f,2Ã*¶{Í_\x001c\x001a´_,Ú\x0001äéjòµ\x0002¶¡\x0013îDÛº±!?æA^pSÄ3¸À5(T\x0019
\x001dw'ÜÆÁ+#\x0003Æ Kÿ\x0008bÀln=j×	·q\x000e0â\x001dÈ&\x0008-æ\x000c\x0011¬\x0017ïàqØAcoaÄà\x0012WOdn\x0000r\x0007U¥hÞ\x000eÛ0hl\x0018\x000c\x00191¯dûeTº»²<ÄÇaUÃÆ0àapF^k¼Bnaö À
]w!\x0019Ú\x001f©æ[â[ùAEôæþîóqd¦/~}ûþö×»\x000f\x0008¥Ò:/Z¦Ç[aSbÅÏu\x0018>dysõòûÇ±a
»°ÑôjÈàÐ°\x0004\x001d*\x001e\x000bÀûö«Áé\x001aî\x0003\x0017ø6F\x0007IU\x001f-Cµû­\x0005gjp¦\x000bµl7\x00138d&
"¹#»âÖa³56Û-¥¤æ!¦ì³\x0008Ns\x0008>C&©uà\
Îõ3rålr8:28¦­Kàö{\x0003Vó58ß\x0005Î\x001bfÇICîÏM\x0011QÀí¿Q®\x0006\x0017jp¡\x000f,GZ\x0010ù¤\x001cZ#\x000bû¥æÕàb
.v\x000b\x0012öDë</ÎJàxt\x0000©qi=¸Å?XµÇ[~ &øÕÝû³OgÏoßýróÊ¿þvóán©®ê±Ã]/
G¿®ÐÓ\x0004j\x000bõÕËggoÎ?}òÝå3ªv>uùâåÓ×cÇ\x001a;NÀîÔrÌ>HáÞ*3
»®±ë\x0019r÷¥)(óçú½+
\x0000:ÌÂnjìfÎQòJ)»ÝÜ«WJ=\x000b»«±»\x0019ØìS#ZÞM`\x000fvÜ}ÝOÀ\x001e]{\x0002Ò=ä\x000böýêe7vhíÌ\x0004CC5uiÚÓ¾\x0007\x0019±[H'o\x0015&h+5Åq·ÂÒ¢A\x0015d\x0006ï&Ýøôoª\x0006¿üyÂÅA\x001e´¡®\x0002Ç×\x0006KÇö£àÓßÜº§ô=¶Ãë³W×·ÿ¹\x0002. ¥2\x0004L\x000cÞ\x000füR¤Á\x001c\x001fx½8{uñôÿ~\x001c$Ö ±\x000f¤D\x0019'ýÓ1oy ®#[|Ïq®£µ u
R÷tªtÐ'¡j\x001d.½E¦Ì;P\x001a¥éE©´,M\x0002,Ll.áöc}ãd-J[£´Ý\x0007îeÈ2|ÜN\
Sî3vâ®Fé¾TYú\x001a¥ïD\x0019A\x0012YÆ|)/t`\x000fÖ®\x0018j¡\x0017¢/Ëåh\x000fQÎ~BÒ2dÇ;Ö(c/Jã\x0017ºò¤ç\x00009í\x0007ªWÜ\x0015®\x0017{®ºQ:iý\x0000\x001a£\x0004YÆRã\x0019Öítú\x001d\x0015¬=)D¡Ú	öÄOQ\x001dhü\x000eô:\x0000K¡ w\x00018¡×µ¾¹óCê\x0003ç^×\x001c\x000e\x0011k-í\x0014 \x0004Â@(\x000fíÇ)¶Ö¢l<\x000fôº\x001eZ\x0016ÀôZ\x001e(\x0016àMaÖ|\x000bh-ÊÆó@¯ëqVÐÊTwÐFrE÷\x0010YáZç^×CïéÜÓÎ	óoR\x001aiAòG3mÙ¸\x001eèõ=\x000e\x0008ÓGQ\x001f,Ü.\x001cÙ%¶\x0005eã} ×ý$=§
´c"Õü\x001aÀJmÃ\x001fYËµ\x0005eã} ×ýÐ][8r¬ cÛ\x001e\x001f`'Z	\x0012\x001bï½ÞÇÄ²ÔG@\x0007$ýñM#m\x0007ÊÆù`¿óQ»À
=o×Kmµ;N³\x0016fõôz\x001fZ´Ëëâ\x000ch¡Î\x0004å
#Õ ÌÆû`¯÷ùÓ¥Ù¸\x001fìv?´Sèéa?+y(tÉa(ÆÄÆý`¯ûùÓÙø\x001fìõ?&OL\x0008«g¦D"ÓÎ7\x0013q\x000ceã~°×ýè\x0014³ñªe¢IËõÇX|yT\x000fð¹®EÙ¸\x001fìu?Äà\x0008L<"öìÊ-\x000béu\x001cÊ+°q?Øë~hÁì\x0008Ö(D\x0016abYþ3VÝÐÿÑÝþÆÙd.\x0019Æ"K#\x000c¾ÁØ¡\x0018S7þG©þG7þGwû?÷bê¶ìö¥º\x001fÝ¸\x001fÝë~þla6îG÷º\x001fËsÁ¢åN1\x0005²\x000f\x0003öxºZt}ÿîæ·\x0007\x00116G÷z\x001eâæ,Òy 8nÌGó\x0000ááZA6®G÷º\x001eôZºSÆ(½ÏA¨j¢9i-O\x000b²q;º×í\x0010Û9/ÑöÆSÍ(ÂÊ2b\x00184ÛÑ½n\x0007Ôl:íÈ÷QÖÆÄ\x0007\x0008×Ñ4\x001eÇôz\x001c ä1^ª\x001aÞì\x0001\x0003\x001c«\x0010Æã^Cdu²»^ÃµPx\x0000£;Ym;-ÇÆÙ^gC\x001c
"ÆôOùáÌ\x0006i\x0007#ËN·±ñ5¦××`R\x00141>ôLÉ\x0014\x0018Âã\x0013ÃÀul\x000c¸é5àÄî\x0007E©`sFZ=äfLcÄM¯\x0011OÒs%pVxvQ66ÜôÚðd^*h}à©`\x0001©N&§O»±á¦×+ó\x001dâpù>\x001aéÊIr\x001cÊiMcÃM¯
'Õfâ\x0018Oì®Èº]îd·\x0018mcÃm
71&Ùi\x0011£çO)\x0000nV)­£m¸í5âés;,Ë1Ç¶Z\x000eûí\x0014«\x0004Ù\x0018qÛgÄ m\x0014¶ï \x001c\x0017 \x0015G¹\x0000þ4ÆG\x0005ÙqÛkÆ±noQ\x001añ,ZñÙ\x00037²É\x0016l_¶\x0004¤Ç/¢é¿Ì»¿µæý\x000eé¤Ç*\x0017¶}¥ïu6)*±\x000f\x0005\x0018,G\x0010§KÒ§åØ8\x001aÛçh\x001c\x0001W:@äe~^\x001b-\x001dÌØ}l\x001cís4	e°Rè¥åÜ(g\x0016AÚ\x0007\x0018Æ×Âl¼íó6&\x0006Zi¼¤4(\x000b\x0012Ölãml·IÂLác1æFHÕ\x000cD\x0011æ\x0003Û;W¢tËq½.ÇG%¤òv9\x0001\x000fqË\x0003 \x001e{trËq}.\x00067\x0004jørx\x0006.þÄ~ã\x001aãz]Î.ÈÆå¸>`&Ãý¤Q\x0001/õ\x0000Ò¼Ö9\x0010R½é,
²)JM»[å /xnPí®\x0003î'ØÛ\x001c°\x0001­ÂsàgðX\x0016àbÙs NÇZ¤\x0003°¶\x001bìî\x0014üø®ëWïúZBé
|á\x001cQ#ä%xZËcxCòØò_[ÿÚÒ1Ù\x000bJ1ñ\x001c­ëñ\x0005çXg\x001büxÓ\x0002½ùbþÔ\x0002ýéË\x0004þq_õ¡_õ\x0003Õ¥g0r	!X/U{:_!Õ·­Tß~aRõÁî\x0013\x001aÙ\x001d¡ÑÇ³\x001fnþp³ªe6\x0008f¾\x0003cÑ	ïRTyNÃ¦¿àÎèõÙ\x000fO¿}qy¢K]àa
\x000f{àiâ]Ð\x0019Ú!Ïô7ÈÙ\x0000a\x0004q\x000b<]ÃÓ}ðt6ëÆ*{\x000e¹v\x0010B`tqúl\x0007îxx$ÈLÌ|1³Õ|²ü`7\x001cwÿiÑoî¯?¼[Å\x0011¤0HÅÊ¥Àòz§\x000e¦=®Þ,\x001aòÍÕÅ''æ¾m5­\b?Ò2\x0015ìAi^cì­²»þßQ¤ºFªûBG<E®,SgÊê\x0001c\x0007\x001a©\x0019)
©%ªwß@m
Ô\x000e´P\x0019ÑÀ)pnwüÌûÄº\x001a©ëGª¬W£§).\x0012 \Öì³toFêk¤~@¦JvC.\x0013Æ"S(I©8C3\x000cHÔHÙ\x0015òìs\x0012§+âÜç1Ý\x000c3Ö0c?L%/?4LÎzÉ)\x001d\x0013£ç¾\x001bPXL¾\x001a\x0010hi\x0012¥\x0005\x0013ÌTcÊRÐô×\x001fÌnÚz§\x0001÷,½e½÷ÀÓå´ V>ìSAlÚ¸'\x0018ðO4Â³

âû\x0002µÉÜ» 6þ	\x0006\x001cT
½\x000c/Ïç\x000bÔÒ½nÕþê´ÍP\x001b\x0007\x0005\x0003\x001e
\¹\x0000ÑóúòäKËÜ»Þgcß\x000cµqQÐë£è\x0015+ï¨ÍyBßèâ¢Ôþî©ÍH\x001b\x0017\x0005\x0003>
§i\x0011*×\x0019Wèiõá@þF¨íÿº·I®+Gò|·Â
$
îø¶\x001cQ
i\x0014\x0019M²Ê¤Q\x0011ì\x000c1¤lJ¬®ìQMß\x0012jZ£ó·ØI­äÁ\x000fÜqs®Ès\x001beÊ2ë¶[¥pà\x001f\x0000Üÿ>àüÁÑ=Ñâ¢±A´\x001b
Ã\x001eTlÜ*\x000e¸Õ\x0014îä(\x001bPý.ésn\x0010´qªØëTé0H)©¢	°ù"ÌË\x0004\x001cúu´Mù\x0007|ª*ÃëU°eIMçz0íÃÆQá£J>GÏQÊøäSw\x0019ê MacþØkþä¨\Ù+ï¸GÞè]LËio&m¬\x001f{­HqGZ\x001e
ìobË6TÝX¿îµþü\x0018dVÄ.ÿ\x0003¿k\x001ftTº±*ÝkU\x0019ÕAAåºÓ\x0019Üªº±*ÝkU\x0019UëÊcñ\x000c¸¢²¿½ÙÚX\x001e°ªjÛ¥¡´z«ù5ÞfÔÆ¬ôYy[\x0002Ey³3J)\x0000sÍ¦­¨¦1+3`VÉì½+:0ªêXÔHâèªÆ¬ÌYÑ\x0001#ñÇI}YÔÑ°jÚ[\x0001«r¶Ìµ1å¨¢L#6aÔWÆªÌUQ®"R:NJ3´èë&TÕë\x0000hBsJ©`5à¿þý?N><Þ=ýë§ûÇ5\x0019!\x0007 /"\x0015U©]°<Ì\x000fôÌptòêêôæýåÙÕË¤Xâ\x0000©N»»
n\x001f3¢O´\x001c\x001aµT×¤ú[^SS\x0001ÒdS.{?¼r¤ÂÅCÄ6PWº\x0001Pj±;ßÈÃP1|íFm+i¨IÃÈÇ·"Q¢(È\x001fG:\x001fÛº´®Ú ÒþT\x001fl9ý\x0001ùÔÜ \x000ePÆÆ9\x001cÜ©ÍómöU2î¥\x000b\x0018hk\x0013È¿Aa¹¨Vó³ÕfwUÔ\x001cÖm?,U\x0008óÈ\x0017c¸/*­nÕív\x0012¾L¹Z\x0002ò\x0003G\x0007yl~ýéé+{T\x0015g¬Ñi\x0019ç pÕ:\x0006ml=?÷æ×7+@±\x0006Å\x0001P\x0004þþ	\x0014¹ºÞgE\x0003$Ñ!P]ênÐ\x0010½æ¼*\x00052¨\x0008ÿ`¿ýl\x000555¨\x0019\x0000M~?+=E§"\x0007+§K
\x0016ÒÀ[9]Íéú9CJTAÄª6º¢ý<°AÙ©\x0016ÌâTûVÔ\x0005!;-¬\x0019L\x0013 dE}çF;³ú7h¶\x000eq\x0016¦U¦D=hÓ}j´¨EM\x001b,×@¯»?\x001a°Cüï/Bê\x001aR£¦4ß(¤­!m'd\x0008±8$ÒaÈêx6oF»m%t5¡û\x0016	}Mè{	}\x0019f\x001d
X\x0016 ³A Ð\x00193\x0002\x0019jÈÐ½fzq SNçÙQ¢xJç\x001aUð­±ßæJj<¤ê¦ÔçwD\x001db>\x001eYïùv\x001cS\x001cÒ#vÍ©qeÛSjü-\x0018Ïÿ¦¿é¬X0å[|×p}ÿx÷åöþãªg\x0006Q\x001a\x0002\î\x000béäÉwÌ1Î\x000f\]^]<7pÑ°FÃ\x001e´d"[\x001em'¸¤K¯8ên8]ÃéojÝLfzÐl\x0014P§\x001dßÆMJ¬¨@Q¡ÎÖt¶Î;9&Ò0®<½=X-Mfj1ls\x0003«éÜ·¶v¾¦óßÚÚ.|kk\x0017kºø­Ý®jrÃê\x001b[<h£DWø=W¯\x0014Ð\x0013*\x0002Ø\x001d^\x0011¦´ÁÊôDØ×Ä
è	\x0016aWÀë\Ì/9
d¼\x0014ØM×\x000bè\x0017¿ëâ5ñ\x0002z\x0002Æï¹xG\x001e\x001câ*M\x001a2Êá¨\x0004nQM´\x0001®qyÐãó\x0008N\x0006_úp\x001cYâZ´l\x000fåZOOÁ\x001e\x0012tR<\x0017\x000c_\x0018\x0006'!@\x0019\x0008ÝxÑbÑÒû\x0010ãEEï[\x0019ÏË3¾Û,°1\x000bì2\x000b­åÍÝQ7c¼2\x001eÒbÿÇmì\x0002»ìBï$8\x0014µSQæ0ÏGÅ¬ \x00037{`rµ~túñËãÝ\x0011¨G:=Ü\ÑRCoì§{8:cp9\x00082´rþÆ~zq}uzD3ê\x000eiçg\x0017ÏôÖ½³B¹bï\x0003Î\x000b\dOsyJ:"ùÖóÙ]]Äº&ÖcKì\x001cuQå5\x000e2ÑÖ@Ybw%65°\x0019\â Â²ÎØc©f\x0017Y\x0016N\x001f\x0000ØÖÀvlmØMÛD\x001eúâ*mý\x0001x]ÍëÆ\x0016\x0018õ±\x0011	í¦\x000c8Æy­@\x0017®¯qýØò\x001aOÕ×yyå\x0019Æë ÖÏ]Y\x0017p¨ÃØúj9]N{inÚÍy`\x0017p¬ãØ
kË=µ)XÊ¸×¾.Â¼(«\x0018Ú¸1\x00188Pð=LÕVT*h\x0004Ê\x00001\x0006Ó\x0006ôC5õÇÇßþÁ_×¿<Ý?¬\x001eÛîxp¼\x0011x67ßÉßÝ\x001cýx%/`×?Ü??W¸MÍmÆ¹ÊßJ&ËË°¨PÑ¨ÞÃp»Û\x001ds¨\x0005\x001aËéùä°^èPCqh\x0015¤Ff7HÄX¹ða^ÌÕ\x0007¾»5!p¹5\x0019"!ÄÉÀ±â1Î¡\x0016ÒÇ<\x0008yc0n¤Rç°8@ÍÃÓC9G.
({É\x001bËqÓô±tüú´q\x000c\x000f&÷ºûÃø\x0014hl\x0013Æ\x0006Ös}µ'%\x0017\x0019Xï$®ÇyÃj/yc 0n¡æÎr¸\x0004+ª¥`c!_\x0014/õcc¡8n¡Þ\x001bÁó¤àÏ»ÅH.µ¼	ÛÏµ\x000cüNËà]:¹~ùÃùíÓãÝÇ/ôwøÓÓãíºóK\x0019\x000eo@\x001dóñ\x0012øé­'À|pè»t½NÄ7W)æÓßáO7W'/Cc
ÃÐÅ,u\x0011ÏUñxPóFNj]SëQjSªs5Ý\x0008å£v2Ò#j{\x0010hSCQh«åDNÐ\x001cuÒ?j¡WêvRÛÚRkMRz\x0013µ/¹`I`S÷ìtR»Ú
o\x0010¥¬¦/,\x0005öl0¿óêö5´\x001fF%ZÝÚc6E-(4ø Ð¡\x000eÃÐñX¥¥O[%Bl.\x001cf¡cÍ\x001cGw\x000f\x0019Ú"·!¤V²ÒIÃ}ÔÕs_%0¶?xW\x001b#\x001aßuäÒÁ}AuR·Qq8,¦dSVMócx[-²(ÏèÄnâ"\x000c\x0007F*\x0008äÅN[óUiTófÞ¨¶\x0011ÚÎo|m[Týttu÷ñç»ÿ{ôþÓÓ:Í§P¤\x0015Ðy.Ñ%:?kX*Vo\x0012îw§ÿóèýåÍsÚOóË2[.Ë:iÉ¿±Ú¤w\_ë£¹\x0004.¸qÚXÓÆ\x0011Z/:i\x001eC,kë´3³K-´ÚÌäÜÒ\x000fµÛ\x000f·O_>\x001f½½\;<etÜ\x000fB\x0000xøUZPÁ\x0005³è±zwôÃÉÍõ»£·gWÏN \x0017V¬Y±\x0015Á\x001d>¼Ü|x'/¶t²\x001a%Õ5©\x001eYÕÈ\x0005áÓªBöb.îVuqK³ÕÔ¬f`U}IÙ¨Z'å\x0004£ÌùÜãngµ5«\x001d`U>x«¤!8"m??4mGu5ª\x001b@M\x001eV.\x001dzQ\TÏ
Ë×¬~Ä°\x0014µ­M¬¾\x0008­x«eÈQÃë\x001ajÖ0ÀåÿòºzÑZ\x0008Nnã\x0000Ýv[YcÍ\x001a\x0007XÛ±ZIfÇôÄ:ê\x0006vIã\x0014\x0008T?¬&	\x001bÙ\x0004\x000b\x0013|¡Ö?\x0001om£Ö@ØB#o}TB&óÇ\x0004t®°¸\x001d´	Y0\x0010³4î®\x0003ÓÎÍA+¦¨Ë¬tv;k\x0013´` j¡2%Ê<\x001au²\x001b·3¿tÝ\x000cÛD-\x0018\x0008[Ú\x001aÉ¸*\x000bå9\x0001\x001du¯ÐD-\x0018	[4\x0014SXÔÔ°zÔgA\x0013·` pé\x0011\x0006\x0005'JµÑIå\x0017×©Y¸\x0005#$yþ	=öÊ -[\x0006\x000fÌk½¶Ã6\x000b\x0006"6A*¿HÚÈY)\x0004?¿GØ\x000eÛD.\x0018
]AÄ\x0017iee\x0010\Ð\x0013w\x00016\x000bG"\x0017©	«ÃwÝ\x0018°èiß
ÛD.\x001c\¿ûÂ¶ç­àEb»9 ÐøTÃa6Ê´=ÜÓ{¿\x0015¶^8\x0014½x\x0000	p5¯/ïàç5Û9À#K\x0015=Û@åï\x00195Qó.\x0004ø¶³6\x000bG\x0002WÚ¬|6\x000côÌªåÊËÂÒ<ÕAØ&\x0018àH0 	¿XR-Ï»UA|\x000bèí°Å\x0011ÿj¤'Øò&\x0015D+\x001d¹o\x0008tã³ôÏJ¹\\x0012ùRÏ\x001a \x000cÕÃ+«Û«\x0001? UI\x000cie­(íï\x000e³Ã)·n\x000cL\x000f\x0018Fäs\x000cUX\R:\x0005nþ³µ±/=`_\x0014
ø^"\x0017ßk\x0006)½\x0010×µ1/=`^ZqÓ\x0010²Èa6y¡\x001a\x000e³¦1/3b^Ñy\x0005\x0007R	\x001a¼ä/\x0008ÃaÖ4æeFÂl(·üì\x0018\x001cW\x0000Pø\x001aÍµLc]f$|E*¬PCÑ\x000bNßP\x000f\x000eLc]f$z¥\x0013wà\x001d\x001bp(Åª8/RØÎÚX\x0019	^¿;k;ÿï
v2R}'E~-Oé\Ç¦<A¢7-­g¶nÖ5~¨\x0015ún®~ûÇß><Üÿï§u\x0015Æ®MR¾Í°)Á-M8}K¥LW§?Þ¼:?û\x001f7Ï	\x001fºY§:±ê\x0011Ví¥$ÈóbVm¤:ÒEXØ
kkXûÃú\x001aÖÀ¢"54prPv\x0001.j 7ÃÆ\x001a6~Û°ÐÚ×ýþû\x0000\x001a\x000b\x0011\x0013óY÷n¬ð.ésy£rD¿(@ÞLÛ\x0018\x000cÙXPrÍ5©Yä¥¶<Óö/­÷óBÌiäÚ\x001f_ÿr÷ëýGÂ½þí\x001f_niòÕ`éÁ\x001bZ¬Üt¦ÿÚ®é­"}ýÃéÛ³\x000b½¦Â7Ï÷;Î«\x0018ýTÅØËiµ\x000c\x0005u^ñDÝX¡uÝ%ß\x0003jkPÛ\x000fê$ß¢Ö\x001c¶\x0002qÔ$8ÆékN?ðá\x001c¾Ö¢)2£\x000b&\x0011û!ÐXÆo\x0017\x0014ZS\x001a±¥ßôCÚ5Ñ¿¢¡ß\x0004zÿ%§¯o~\7é.ý»Ô\x0011Q;
f\x000bª¯ýèë³ë\x0004¾>ùîêQw\x00050Ô¡\x000b0Ë2¥:Áø!^AÊ¡îbÜL\x0018kÂØ·\x001eåFØJ\x0017uò:uËÔV¾ò?±ê[BeËÙÄ*¹²A<éàï\x0007¾1´°s\x0017Z/Ó2ãÙ\x001añL³\x0018ú	±!Ä¾5$\x0011\x0000,_+^eÐ8°\x000bKb	uß\x001aF/"ö!:9:%@hâÈ"\x0006Ñt!"©Üùr]ÆuÉ;Êut\x001cYDÛ\x0010ÚNw8µp\x0010a¤G	ÃþPFM£­gÁmFt
¢û\x0006\x0017Ñ7¾o\x0011YM=*#Ót¬÷1;dÊM@¾ü\x001d·6.
Û·rS\x0003±îÇØLØ\x0004\x0014è(\x0016iÜñ´Pæ;¦|BLÙ×\x0012U[\x0011±)Ø\x0017S¦]¸g\x0013ê\x0003lBlB
v\x0014\x0003r)\x001b©\x0001.gm¹íö#MHÁÞ\x0002,¬é£6râN!E¢^À¯ÜÄ\x0014ì)\x0000J\x001f3b(ô\x0010ó\x0003MLÁ¾\x0002ÆJ!\x0011uÒ\x0004^Eñ×>|æ&¤`gHæ8'\x000eÑ\x0018¹eµ1C\x0003é!6\x0001\x0005û\x0002ÊïºM<ÁÞxâ¤<Z\x0000y@-	¬V0b(ÇÆNý;~dÝ¸CÝé\x000eÏ]èË¸\x0008ùÌ·ß\x001a#ø¿|¥6\x001fº\x0018ÑÉ£ILÎ\x00152¦af\x00192ýoF²êG2\x0008ú¥k5ËÉ>*G÷y9½\x0017;rê}rèýäT "Ë©X\x0011Ñ[]ÞN\x001dnLÆ&!iP³Ñ éêùéÇûßþñÕ>úå(Ü\x0017'åA\x001ee 2ð¸¹ôãÙW\x001bè\x001bB¬	±0ªt8Í¯å$àD{_
T¦1t\x0013êP÷\x0012ÒH\x0000\x0004\x0012-W§;Hÿ]!Üs_¿ÐÔ¦\x0010,çi±b®AsàA¿¹ìê\x0006@[\x0003ÚÞmèáwaP,\2)PÈ.7
o\x0000t5 ë\x0005´plø\x001b;Ë­Hl\x0003\x0013.«øV\x0003ú\x001aÐ÷\x0002j\x0019\x0000ñ8;eezÛ36i-`¨\x0001C'` +\x001cÞ	)Y\ú<¬µ\x001fìQdk	cM\x0018{	+3H±oZBK½¾L~ï%þø·V½4nV\x0016Q\x001d#\x000f\x0001ðJ>³ë-l@l\x0003JoDIÀwÚ1¥¸\x0017ÒÆ2ø!\x001d©»½!4\x0011\x0005:CJ\x0008\x0004"3¦Õ/mÔQYÏe×6 6!\x0005:c
/²IZ9Ï5b6¢-c°æ³Ð7 61\x0005:
0s\x0019~BdE\x001b\x001bD\x001b&\x001dðmY«	 \x0002½QÅâ\x0014ßÐgÄâ³ãÙwk	¨\x0002½aÅ;)\x000bÉÑigÂ \x0008ó9¢\x001b\x0010¸\x0002½Å\x001bä>ÁhÅå¤´[ü¶Ú3ër-b\x0013Y 7´x\x0008ârlÔÜ\x001bf½uârÔ\ku\x0003b\x0013Z 7¶Pbèw\x0011Ñê²Ýñ\x0019Ø½±ò
åCþµ¬bøÃ&¶`olq)\x000bãðGæG[çv×t÷^Äö´Ò\x001b[qr\x0018 DN"õe, î\x000eØÄ\x0016ì-\x000ezì¸I².{îif-{îåÐÊµMhÁÞÐ>i~Jnà­5N¾3ªÎèW\x000f\x0002\x000e,JõÚK\x000cP¦\x0000úX}ÔçÏ\x0016¿éÐB÷
)\x001dVC#ýPI¶¾þå·ÿürwû´æú\x0001©CRFÿJôó>mÐ\Ff\x0017'£×?\Ü¼Ìgj>ÓÇGªÍùæS¥èÌ3´½×2\x0016\x0017W\x000f\x001b\x0000m
hû\x0000ÙÉ*È$Þ=\x0002à
®\x0006tF\x001eYÒþ\x0014!³ ø¡JYX\x001c©6\x0000ú\x001aÐ÷\x0001z#Û\x000eWÒõ$úv>(s\x0013`¨\x0001C'`©¼V^ICqr/òÕ\x001eyÝÕ±\x0006QdtÓ¾+Mnh\x0004\x0010ôR´x-àNL\x0000Aõ\x0011ÒØüZJO»».\x000cßÏ)Úý\x001f>G¨Sã*+¥\x0008§|ëi_d
\x001b\x0008uC¨û\x0008µ¡ÆµÐ\x00149± fqÚñÝ>þt÷·¯Â5n\x001aúü´\x0006Ë%`éÔCa97°	\x001b;`!ÐxièsÓ&I±ä­>í\x0010.y\x001b\x0008\x001b'\x0003}^Fkñ2.ÆÀSL¨\x0006G\x0008÷
[\x0002I3}
&¥sf£)Sy\x001aû\x001aÃí½\x0017\x0015«äkæ36^Àä¹óIæqz®øñáö')9{{¿á2ÛÅrM§ú|ÓÆÉÕH°UbóãùÉk©9{röl(¨X£â\x0008jÊF{÷¼5\x001dºr£\x0018êFÚ\x001eT]£ê\x0001TJ\x0011_YXlmZÊòÈ2¸¦¦\x00065C ¶ÜÄ¬Ìa´¶|þÁ5µ5ª\x001dùü¤\x0000Ä\x0007-2¨ütBzy\«_}W¢Nfnª7@ù¡mA{ûéË/«*¹fÂ\x0007=Ft là\x0003k
>Ëÿ	ñòú\x0015X\x0013b\x0017¡¢FÍñ\x001b¨ç\x0008CÉ0ö\@­\x0007Ô5 î\BM÷b\x0002Èy¸M)\x0000î¹h\OhjBÓ·Ú:]J
ø\x0012ÏPR »LÙ@hkBÛ¹H-æ\x0013!ÆR{àEµbÒ\x0000¡«	]ç\x001aNº
y
'Q¼JÖp\x0011\x001d·\x0000ú\x001aÐ÷\x0001ÒÄ.Sãn\x0002+²øé#ï¹À[O\x0018jÂÐGF:°R²!)+\x0012Cqó\x0019[\x0008wÇ\x0019Ó¾±ms6î\x0018Ä\x001c\x0016};ô{Ê
Ö#6¶\x000cÆ¬\x0014¿¤\x0015Ó1"?LO3\x00031C5+§Ë¦\x000b<n½¡\x000b\x0013Þ\x0003-C1\x0018£/éüüåæÄÐ­w?acÌÐiÍFñLÁd6â\x000fSN!Æ¼ç¡w5 6y\x0003ö%\x000eJi\x000f¦tQi6\x0006@,eÄ±ËØ\x0013é+;I-\x0005DÓh(\x0007ë¥(ë\x0006ÄÆR°ÇR\x0008Qí\x0010t°A\x0011@7a)s¼\x0016/»w¹¾ìÞêqtq8\x0019
âpF\x0002-åv?Üv1F>ºâ$\x0018«hcÍû%\x0014Öf\x000f-¡ë$Ly
OªM\x0016(Ô@/;k ö,@ORHû§»Û\x001f\x0013éýû<þ´*\x0011³S©"Qt4\x0008Àû¼\x0001 ÚSÑâNO..\x0012ìÑÉÕë1±ÆÄ\x0001L\x0010¡U\x001d¥·3}e§£Æ(uM©\x0016/Giê6\x0008Ö®¥Õ÷\x0018lã45§\x0019àôÒ\x0001hht"tçËr.z!¶qÚÓ\x000epFi7éTÈý¨ÎÅ²:êm®ætý$áS4L]ôà92eÛì6J_Sú~J\x001a\x0006À»\x0013uYÍòÑqQ¼
3Ôa\x0000ÓB­ÁÀE24iY\x000b§\x001f3öXsÆ!Nåô"éhê(sºy{à&Îê¹ÆÃ®_º\x0003¦í±\x0015é ñÜ\x0013\x001f¯ÝÐþ6\x0014
Ä"¢PN7Ò±ê\x0002ÏvOÿñE\x0007ÿ6Ð&\x0018Á@4¢R\x001c\x000cò[;rI
\x0006ç\x0013Û@x\x0004\x0003\x0001)Èíi\x00025ì¼Ë¾`Æâ\x00114ñ\x0008ú\x0003\x0012õ±\x0002sÚâ|\x0019wEU_C M@D¥\x000bì¨¬MÉ\x0014N;äC¡	HÐ\x001fRÈ)\x0011>\x0005Q¥aä~-X3ï3Û\x0006ÚÄ$\x0018\x0008JTd\x0018Ë\x000fM	dæ`SÝ\x0001Úx{èw÷¨Z2­(\x000foö¸[Ð!ÇÆb¿\x0013EUÆb§\x0013\x0006gÊ^;1ùE«Ô6ÌÆ3a¿g"GÇNfMz\x001dä»;54éætJëK÷YO&jÊªÊ\x0011'g¹\x0014ô7ïÒ\\x0006óî.È/;\x0012çÕ§¿ß>¬.EÔHj­rRo\x001dF.PK?×çÍË\x0004yuùçóçè`ÞÚ\x0005ùY§\x0003Ï¤3p~ÈCtÜôc\x0010Ó4çnÃÓ5îÃ\x0003ºgí¡\x0014rR(ð±\x0017ÏÔx¦\x000f/ÍsÜ:h.\x000c²6òe?ºdö½x¶Æ³}xéÔ½xÔ)òp\x0005'If<k\x001böMx¾ÆóÝ«¥PÒê!K¥ÕóÜGCý½x¡Æ\x000b]x6Ê¸¾h´Ê¯ñT+[¯i\x001cÝF\x0017kºØGçEM1\x001aë©93×\x000f;Y<zVìÃ«Ú¤p:ø\x001cÈÇ5i!¹½Çj\x001e¿N¾×±@ëûü²¥6ë\!nå8kMî#ï\x001bßMx[>¿l\x0001ù,\x0013m(
\x001fÆciUÐ½»\x000f\x001a¿\x000c}Ù¦¼+rý\x000fjÍM\x0000Æâp
ýëÇ9B½S1U\x000f¦+ýSmÍDYZR )ùz	rÊY\x0015}¤\x001f¹äGßÝ}\'l\x0002\x00049&Î|É\x001b 6§è1ëRÈ\x0013L¿;½xN\x0019ÙÍç:×\x000e!ßB¨D`\x0016á\x0003`"´B¨\x001b Ô5¡î$ôRwHÀ\x0001\x0006\x0000\x0019û©æu¯\x0000m
hû\x0000I\x000e=%ô\x0001c!\x001cúÈ¾&ôZ\x0014\x0012ÀOÝ\x0013¡\ìÙ8o\x0015Ý\x0004\x0018kÀØ	èøá\x000b¨iñ¼\x0014_/\x001aû·ðAkÇ\x001cTØWÜ\x0011\x0010¥tØ\x0006?Ø	ôÙI:+É\x0016 ±\x001b¶d­­ Î\x001fa7!6\x0002}b©¢	ëô\x0012aN\x0014?/Ù´\x000f¡>xf-\x0005º].£ÓqÙËá3IrÛÐ\x0003¢×ì\x00051Ìª	Ó!ù·¬!¤\x0012B.ãò*PT.ü`©\x0014aÓXèNÈ/\x0003b
}àY'a\x0002\x0012¤2)Då\x0008õº\x0006Ô+¨¹\x0008\x0016ÐHå\x000cwøSÞ+þ½ÏÔ|¦s\x0001£´m9ºNRÂ²~{&VóÙÏv¯\x001f«§ûd#"§tY¿½=ëø\ÍçúøÒÉ/ó¥À,\x0012\x0014uTô\x0003ú\x001aÐ\x001fÂ¹\x0000 1á½E3ë\x0000C
\x0018:WÐÈÛsEP×D\x0014\x001dw³è*[\x000fX=²y\x0011á\x0006Â(yË\x001df0\x001e{W\x00136^\x0010:Ý`ñ2éÿâo²\x0012ùÆn9üw=`ãe ÓÍÐë\x0014I¹Ceò·òj¯±bè4cc¹æ¼Ë°!¢TK\x0003\x001bú	\x001b+N31\x001a\x0017½¼£X,êü~ \x0012cc%Øi%¶< ²\x0017?Z-\x001a¡ê+¥¶ë\x0008Û\¡ÓJ\x001cJ_^J¯ù&É[ãK0ý\x001f\x0019\x001b3ÁN3ù]	\x001bCÁNCù]	\x001bCÁNCqæÊO¨ÅÕX+Ãa¢\x001dÈh°yuÒÖÝ\«Ý=U*E}	*z½í:NsB7'`«6";`AF\x0006P÷ò&ÌÜU\x001dQäúò_ÿþ\x001f§}¸ÿ¼ºLK¯Dô\x0011Ø;ºt&åKÄèÍ\x0008}túæüìÝ
L¬1q\x0000Þí2f *ðLi9Å\x0018ö©¯¦Ô5¥\x001e LYXnë4B<é8\x001døL±é\x001eÜijL3é§)Ü\x0019\x0013¸)!a²\x0001%LØsô[ikL;\x0019D\x00118Ò¤û,î\x000cUòG#®ÆtýHMoüÑµâ®<g4\x0017
k¥öeá«1}é\x000707bQ?\x001a³Ç=¤¼Å¸/O[\x0019jÌ0é\x001d/fäY«ÎD\x00043²±\x0003>ðrrEÂÑ\x0016±Øè÷u\x0011®ÅÜ½ýÍO^[9u:ÜpáOgÅüºë\x001cZ± }JVë9Û\x00184\x0010¦9Ë-ÝpÓµ-±þ³\x0019³ñî0àÞÑ+icö!ò{¯³(«é¶ú£)Ç°óKG»èWþz÷xôêÓÏ'¢\x0015Åm¾4írÖñz§Ô£fg«Ë7§WG¯.¿{~x\x0011kFìe\x001a²ÔL{\x001f/§=b=Û\x0018uÍ¨;\x0019Q6az!"A]Ôfæ~h\x001b£©\x0019Mï:¢´\x0000´ëè\x000f³¶f´ýû±¨öøcí(Ê[0·m®Ft½e'ÍøÒ¥,°(\x001fÍ\x0007;ocô5£ïÝÈOè1PóuÞv§o5\x0018jÄÐX\x0006§\x0005£¨Ã\x0016#®qÞ¾·1Ö±Q+©¢WÎ³PO'\ÑuQó¼w\x0013ãîÆÔVq{ûBº¢\x0006GU12¹H¸RT\x001fqáÐÞ8£Ë\x0004-ºÖà±\x0003Þ)é_sÉ¿mMÞ@¶Òk\x0008zx+Ý\x001d&Ì[·A6\x0006z#öe%Óçæ¹,;qBªË\x001bl¼8ôºq½F±®ìI']\x001dé¬6â ñÐë$(ÓOå¯¼W;ý!ën<\x0010t» p,\x001a3Z\x0014\vÕÒfñÀ¾17Ú\x001c\x000e ¥(/åºïï\x001f\x001eî(}üûË4Õ\x001a2¦\x000bXT\x000bÊ \x0007qQ7RÝ÷gçç§o//®¯þü2)Ö¤ØO\x001a)4N\x0019s¹aPµÜ²Q\x0003â¢u+«®YõÀª\x0006Ã÷üÉr"Õ|\x0013+¯¸,(ÜÊjjV3°®éHÇ:*\x000f\x0008Ùäµ0\x0004fÕÖ¬v`]©V%ï\x0001O¯\x0015µÈ¡\x0019ß¯®fu\x0003ëêM^Ôä­XéU\x0007I@\x0000í¢\x0018|+¨¯AýÈ¢:\x0002Ì*\x0005U\x001eMñ\x0001Ú
²5\x000c,j\x001e\x0014G£\x0016DÄDÉ\x0012À,
±·²Æ5\x000e°\x001a%\x001a$Ç¢5Úìôë ë.\x0011Â\x001aú+J=7¥´\x0013\x001bu®Ð\x0004\x0002è\x0004¤ÍQ¼\x0000µ¬°8\x001a8ËF­¬M H\x0002,õÉeG`EEËØ®´*aÔ»B\x0013	 ;\x0014äB|ÑàH\x000f_ñÊ\x001aéâÕÁtÁ6¡\x0000\x0006bA,wtÎ¥|\x001aÅÅJe Ð|ÕAØ&\x0016@w0øïYÙ&\x001e@w@ÈÏ®34)KE\x0018²Ð8Yèö²ÿ-+M²ÝÙ6	êEVq6E z8Üð©´^ôqlb­å¦TK©î@Õ*O¬.åUôÞkºôt[oSÌ1ÜÙDÙ\x000b»öí otÉ)xÉ\x0010\x0015ý+Òù\x001c>ÑÌq\x0000ò/ÂvÞF177¦ô7ÒÆµÈzÞ@£ÝLø¿þý?~øíÿûr÷PÈWni¼\x0002·1hs¬£èiÈÕ¾Ã½´G?\^\x0017üÁ±\x0006Ç\x0003ÓÍ`¾;H9¸Ìyë¥{Àpë[\x001fbÁ£\x0008b\x001e£\\x000c§CñAÀM
n\x000e\x0000(#%@Û2óÂø²Sô^åÍà®\x0006w\x0007\x0000/Ã¾<Ðº\x0005÷Ù)¾æöÿD;¥qÙ<éq\x000bu¢Æ\x0006\x0010¸\x0018$öË\x0013HSëÜÁo?ÃÚI=î»_ï?N\x0013o¯>ýz{ÿqE
©SZ.±q´cµb~ù²Ñ»º¤óõ\x000f§oÏ.¦¡·WoOÎ.zs]\x0004|÷ÇÛiA¯Vr[+c{|òÛ¹¼Ý!\x0001M±®üzsur\x0016ñêæ¹æQk"àä·£9(\x001aìïô\x001cjSÊ\x0016êÇ-dº&Ó]dOï1Ùÿ1¯Iz±9\x0010o!35é!óÀ\x0017¡é «¸á´-\x0004­y\x000eÞfk4Û\x0016åd\x001eÓ\x0019Zæ'4ï¥\¦9ínAs5ë@\x0003(C:½.Êôé¿#¥'XOõØæk4ß¦D0ú¬±2¡)\x0019q\x001aM]·¾\x0005-Ôh¡\x0007
½ÌLI\x0012\x001fXF\x0019S\x001cÝ\x0006\x0003­2³\x0007\x000cµ^*>\x001f½º{üëÝãýºyãhv"ïº¼§íVæÜ,KÝÞ\x001d½:½zC3Éë\x000f4³Ç\x000b¢Ä^J¤!Ñ\x000fE¼z^v°Q×ºÑHÖ@Êù³ ²$G7DikJÛKé4OC^Õ¸<¢ .kÜ6!\x001a1ô"ÒªE2ÛFækE) %\x001d ¬ºµ©j\x00067bjj\x0014ä,\x0011A&ß¤£¨TH,'0mÃlí»×ÀwÌÆÀ¡ÛÂ]¤3pÎY1yÈ	¢àfÍrÃ&LÓ`nÌ2\x0010TØMÏ\x0003)$Ó{³1rè¶òÒ%\x0005¤áïÌÑRLF7#®ÁtÝ.Ó\x001fóÖT¶è5Æ2§N/û)6QúÒw[á\x0008\x00163JÙIp2Ë.\x0015¸·ùõ¦fòí».ÍûSíd÷®¸ì6-©-áÜ-©Ã\x001b¡õÔøáxÚ(¡TÃ2õ¨Ñ/hÍ\x0000­T%i}\x0019jVîaôrbô*Z³+FÕ\x0015ã$÷ð÷÷?}ùô¸Î¨lÎ\ÿ\x0018äJ±¾¾Íÿ,øðþìõõåÕËXcb?fiiWQ\x001fKJçÊ W³¸cÙ©kL=²1Õr®¨BYÎÅ8®m¦æ4Ý4q]Js¦Cä<^®|Ô(¦«1]7fPªJx|Ií¬ÅUæÆ¯¾º¿ûm÷º2'7å&ª\x001c´ÖÁÜB
ÊµÖ~(Ç·§£×\x001e>}Ì\x0017~¯Ó\x0011òîãÊj9\x000e6ûRB>G©è\x001dÛ}\Î\x0004¹9z}y~y¯ü^_^\^<[9'äXã8¹)#©"\x0005\\x0007iöUÅ^r]ë¦575¹\x0019'Oæ¾`¢æ\x001e­<ýÇC/¸­Áí?ÓûÜÿ3Ç<\x001eÀ@M?¢C1P#ÍîÍ\x0000\x0011rhâ\x0001¼¢.ÇJGwH9\x001bè¥±\x001c÷M"îBo|\x000b\x001cÀ¹Ð|g6QëèI>£¬:.&¶õ¢76
\x00070REçûÁ""9\x0007ò-ÐX(\x001cÀDÑÈ0Dç¬(Ü¤\O\x0014dôB\¤\x0017½1Q8¢âª
ï¼RÉ¨@[Ì¼í`3:Î_ý0¿úíä\x001e¾OÄ)ÍZõHi,ò#¥14=*çWÑå\x0013\x001bÀìWÐø>¦<ëûqáÄ\x0013{9u²½Ü¬e\x000c½zäCÎÂ-I\x0012îUÄYijLÓI%0\x0012­èo\x0005c"c¢Ý+²\x001eÓÕ®\x001b3Ï 4æÃóE\x000f²s!Â­¡f\x000cÝ;f\x0014ò\x0017§L\x0019CYJØ+#µ\x001aswÿ<\x0019êæL\x001fZéÌi@î#"æº=Ús\x0019Ï­ \x0005A·	dBÚ\x0015PÞÔf_@Ç><46\x0004ÝFdåÞ-CsYrAl V\x0003ñIº\x00134ÅØÙ\x001dØE\x0015ÙÉ\x000f·_î¿ª\x0016Ý²ª¢2K$Ü\x001fcËP3\x0013aÊÉ«W'×gÏjF\x000b,Ö°óÊ±M°ô\x0008Òk¨íhS\x001a,·= ö0m Õ5í¼^lÛÒ\x0006WZø[åÐd­dê¶.î55ì¼FlÛÒ-°!9.\x0016O¥³=\x000cï\x0003[ÃÚ±áöie\x001d\x001d*òÊj¡Uû+Â6Àú\x001av^\x000c¶
ÖûÝBXköÂò®j+l¬aã\x0018,P¾·\x0001J-¿Õ.}°¸¯ÚH\x000b­ó\x001aó^.PqK\x001bÕ2ëÙââºr+mã\x000f`Ì!8du2\x0015íq\x0011E×f Ü6XÐ³«ÿôÃ..üp÷ññþè»Û§µ©ªaá/c|´ s[¥ñ\x0001º¿\x001fN/®Î¾;¹y.z	%ÖØK\x0019eÌ¥1É\x001d\x0018~\x000cùEË²ÐMº¦ÔßêZÒ¬%îÖÒËZÂÖÒÕî[£ô~v~à\x0013éÃC~á»þåî×O+Ò(U%ãÙÌSò'M\x0004q®\x0011s~_ø®8}{ùTº`Æ\x001a3~«Ð®f÷rZãË}'ò,ôß2rÝ\x0019U\x001fç-=òÔÇ¨\x00132yÉ¦)ßÿtWùu\x001bä-9ñ"w+:,±î{Æ±¥Dÿ;zÌ}\x0019\x000e\x001b8ì3üK\x0019(i-s¢´X¼Ì4d¦L{I9­qrð´"h\x0012u]·Î5t®\x000edÔOJ,T¸¥ÐÍE\x0005É\x000bÍ§ìmø¬ùyöaîÙv %Y)AÓîÛn>]q= *ïb\x0016·=Fäð­6R3fe\x0008`"´ýûOýå§\x0019áO\x001dNqA(\x0019®b}`íåÂéþåÃì\x001bè±^+\x0006g\x0001éSzÀ·¨Ù&T]rZ	#¥\Õâa`d\x0013~\x0001ö¬ õÒÅÎ\x0005ôZÉG(ßX÷»\x0019	vAjË\x001fÙ\x001c\x0005]\x001c¡Ïî~0\x000b/Î{V\x0014ÎEO~úeuùy2e\x001eéÍä4/\x0013¥2~Y;MG×?¬Ä\x001a\x0012\x0007 #Åä³ÉõLO	r¯ÞêJH]Cê~H\x001f¸M:zÒ
ÍÑK£Vû7W2Ñô3FÇ¥ÓÑ§Ü0Ow\x0006e\x000c_l'Èm´5¤íÄÀJ[\x0010fåtgdd/Fj\x0016ïFt5¢ëG\x0004½ë÷ÒÇU\x0011Õ°\x0010Û\x0002ékH?°ÅA#M°¬ÿ«KSZ\x000bËm\x000c5dèÔÏ~4&¸3Çx\x0019\x001aö
®YË\x0018kÆøM2NüÎ«~HGE\x0013#
ØÉréVäe0(ßï"¡
6ýÑzÃyªK\$©gNÿ}²¿+)h\x0003\x0003áF[Òìç'§\x0012\x0017dq\x001b%§\x0016Ð\FÐ?Ê\x0004ö§ÇO+LtQQÃ]n\x000e2àÄÁüørrsuyµ\x000ck2ÜN\x0006A*"I>Îü"JAsóv-®Éôv²¬%ÉDË°\x0014m8ßej,³\x001d\x0012.Æ
NN)\x0001,u½ÒÖdv;wôRÉ@\x001aê\x0001\x0019\x0018gëþMd¾&óÛÉLQAv>\x00162\x0005R°eëQ{ÈBM\x00166éd|\x001e¡
\x001b­ù\x0016ÓÈ5Iê&²XÅ®}¦Ì>b\x0001M×\x001a²HÍß«m\x001f~ûÿºÒ¡y©L¢±ÁÈ
	(\x001d¦\x000e\x0017-)SeÒùé\x0015º\x0006Ô]`L
£¡$¬¯á¬GÉh÷N­\x0003lgäL«X:P6rFIS<Ä(µ¾Ì\x000e^äÍ[qN©»)­\x0017qkâ#¯f×²è:V3¹YMñu7ñéßî\x001f>=ýÛ\x001aÀ@Ý&rj÷¬î\x0011R¬5rñá\x0017\x0007¹wG§?_ÞüËËº&Ô}À\x0007$OErùZ!Ø jAëE^¿\x0001ÐÔ¦\x000b0eP»'\x0008Ç;1¤Èo\x0010!îë\MhkBÛGhà\x0018ø#«©Lj"´ÒZ\x0018ü²6j\x0003¡«	]ßG\x000e½§¯\x001cQ0§hÌWÁ
\x0011úÐ÷­¡UÒúd\x0012lÖe	)ÄÈ\x001aºE!ï\x0016ÂX\x0013Æ>Ât&\x0012Cq¬s\x0013RåÅPöÈ\x0002¬å«ªô\x0012_Ý%¾å#§ã$'¦)àS[pZ\x0012ì¡@ã
¡Ó\x001d&gÃÊïÆ!ë%nÑV\x0008fä+Cãm ÏÝ¤ìO\x001a\x000c½èä§Dk¥k,,«ò6\x00106¶\x000c}ÆLÇH1fª\x0018c
»E\¤\x0010[\x0010\x001bc>kþ]ÊnöèD\x0018:\x0017\x0011¨a9#z\x001eÑK\x000fÞb,zyy°\x001e\x0011\x001b{Æ>{NIµ-\x0019-fÁjyú\x000c{fnm@\x0006\x0011:ã¡\x001c;{mÅY)È`Å¶\x001b\x0010ô\x0006ûò¼"+¥\x0018#·D)"´wÀ\x0011ÆÆå`ËñÁÊ1ÔyzéCK¯÷^¡ÕËÁN\x0013=Û³\x000e¾ìD+Ïw4»c°ñ8Øéq²\x0000Dü\x0006\x001a\x001cH±g,\x0003ñY7Æ¢;\x0005 |æÄÃ³õòÄ\x0018cé7\x00006i¬îËc	óX\x001dPr0ëbÏ¬z>³q³
ïô\x001c§N\x001e>Ü=~9º|x¸ÿ×»//CL»Û¤i\x000e|¾Ó¶Ô¢ùÝôÉù«Ó«ë£tê;{zý2§®9u7§B \x001aÙË\x001a´Ïmq>;o+§©9M7§¶4Ø:×ö+q­MØ5
c¶æ´ßîzºÓõs*)g¡\x0002t\x0019\x0011e\x0004÷mô5¤ïLG¿ÜÀ¼ktâ,=Ì\x00070mÅ\x000c5føæ0S<kMhQ]IoO#(úåîãÝ/+_zBÔpËè\x0012pyÙS"\x0017.}9ÎN_ÿpzqzýÜ\x0010l\x0001¶5°\x001d\x0004\x000eÑäJóhhÔdQ6F¾cFçÌ¨××¼~\x0017E%#R¯a`¦µ{ç\x0007l¢
5m\x0018¥Õoz\x0013mà\x0017s\x001bí`íèòî®
\x0008\x0018Ô ±O\x0007¡<}Z§£\x0007\x0003\x0007Å³5ÑAã¼ö\x0001ÿtûóíç/_\x0001näîiÿ*5Li¼IÕËef¹NO¾¢iEÝÄ¬ç³Uu=*ýóÑn\x001f^¥:L÷Ô¶\x000caDéõ#\x0000\¨1¤ÄêO'Wß}Mq¸\x0001Ô5 î\x0003L6rG\x000f@sRçmìóúj>SóN>K«õ.AÔÛãºÙ®&´5¡ýöVÐÕ|®O©´lÝ$ö \x0013î=Û\x001b\x0000}
è¿½\x0005\x000c5_øö\x0016pçÉu3Z|#!H.%ËN\x0016e\x0005Í>ÃÕ\x001bN?Ø\x0010²ÊHC¸çÒm5aãg ×Ñ \x000cQ!\x001ek#/òõ¾cújÄÆ¡Ó½ô\x001c¤9HóE%NÏÓâM©@§­ü>>øY\x000bV:^ñeÌûÛ£DùöÓýÇu\x0012Ú!òsIr=|cdä¨òÙ~r~t0ß^]<«°\x0018fÏÇDÝÆÈTvV5\x0017\x000c¤ÌÇJq¿+DlåÔ5§îæ¤Á
ü\x0008jpZÜÓCÔ\x0003ijHÓ\x000b\x0019HºÂo.ï \x0010¤CÏK·rÚÓö/f¤ê¼ÓT§|#\x000c¥\x001da~¯¾ÓÕ®{=¡<QÐæ´üXæw'1qúÓ÷÷)\x001efÎsà°Ta\x00187¸¡Æ\x000cß,f¬1c7¦7¥YÆy2\x0010¦ë\x0002þê6\x000eqVçÚ°{\x000eï\x00012=ÊzéÎ\x000b¦\x000cðâ\x0018g\x001bº#Q²ÒE\x0018,]sNe¤k´ór«­ M,î`\x0014\©·"ÐìªÄ9¸ ~?O:ZEý\x0010y\x001aÑwÞw®§U³·ôC¥Júã§_^Ýß®iZ¦§\x000c/'t\x0015©"½+òD·¬²ûñòâúèÕÙÉsÍÕBijJÓKiQ*seàt\x0014ÁT\<¬mt5¤ë\x000c<\x0015;Aºc\x001eYj\x001b]\x000eÆP3^Fg¤ôÓiÜ
CrÑú±rç5²!·cÆ¢E8e"©\x00088ÙØ\x000et\x001b·< (aùò\x0006µÔ!«EµÓ6ÌÆx ÛzR\x0008âÎW¸Ãä< \x0016÷VÛ(\x001bënóIÎ¼(ôI\x0013FË'W{T4·P6ö\x0003Ý\x0006\x0014\x0015ß\x001e8°eèµPªô¿\x001fZKlì\x0007ûìî´HâSóTä	·ÖKv\x0014\x0017ÅOë0uÉ§\x001fª2ùpôööþ\x0008¢±k(ovb=ùÙ7(Ð¶8£%eú#NÎò\x001fñ"%ÖØMiåãT\x0005!}ùâó8¾\x0011R×º\x0017rW Lâ¼/Ú7·A\x001aÒtC:\x0011ÅKH\6\x0011H2,®Þ¶QÚÒöRb\x0019@~È1¥q\x0008Çy¹ÒÕ®²ì´Ñ\x001cÇ®+IýbÈ6F_3ú^FªVæð¨\x001cgmAR_\x000cjìs\x001a2ôBÒu{DY#Ð¨F>N\x000cw¬!c/¤×Årò¸ò\x0000 ä"ÆïIÑ7 BëÌ»½¹B	K\x000f¢)}¡TËüw\x000beã'¡ÛQ2Ç\x0006ÇÝ:\x0001PêËâ¾®¢-\x000fn'\x0014µt¸Ù]Q+hy¥Ö
Ù\x000e4\x0006\x000eÝ\x0016\x001ePö%]\x0016ñý5 ÃøBÓz\x001bfc=Ðo>eø%=6à½iËG_HY¬ÃTóYéÊ©ºkðßþóËÝí\x0013U\x0016|{ÿð°j\x001e=µvä-j,ÉcF/¼qÏAòõ\x000f'×§'7TWðýÉÙùù3óÝÕ|Lºrª\x001ejÒÅlA\x0004ð
Ý¼f/ßÆm@³çÑ\x0001­kh=ºÐ¡H\x001e¨\x0012\x001bY:u±L\x001fÂQ	ÛMÍlþI\x0016ÚÖÐv\x0014:?´NÐTuÌÐ:²ô=êyÝd\x001f´¯¡ý0´?f+$4ÐËæÐqÏíÌ±f£Ì¹ÈkvÀ*zÞew,:Ä6Aû¹¿ó¿#µÄÛ\x001fï\x001e×M\x0019\x000c¥M\x001aL©¬Ln®\x000cß×Sy}rqqzsõÜ5îÜ¿y×LmbtRëÑF\x00114VÞÀRlÞSò³Q×ºÑ¤}Ê*\x0015R~\x0016¦¦Ìh\x0016Ãj61Ñt2¦8Æ'ý·²4æÔv\x0011µÝSs±\x001eÑÕ®\x0013QK\x0015_:;E\x000bªÜ×[Xd\Û¶c5§mÚ·VÃ
ñÚtteFÛ7»z\x000bãñC\x001fcÊÿe\x0000/ëù\x0018ØÙ×ç»a?¶\x000biz\x00172&Óf³¡`¼±¶ÙW\x001eò2fÚê­L?T)a\x0002x¸ÿHÿtõiKO'(éØÑé¨\ÆrV.@OKOÿv~vAÿtuù;\x0017V¬YqÕþN.u9ÔGÚâ2üldÕ5«\x001ea-ã8µU¥\x001cV!
kX^>nd55«\x0019`U\x0012µ-ÒÜ6Ê½w{\x000e\x001bQmjûQU,ÏÝÓ\x001e\x0016*
¥Ð/fÞlfu5«\x001ba5dO5r
\x0001\x001dd\x000b«\x001bÞ\x0002¾fõ\x0003¬AK&¢4âzë¤ËÕ=*#\x001bYCÍ\x001a\x0006X½Ì:\x0004qYÖÊvÝ÷ø°\x00115Ö¨q\x0000Õ\x0015½\x0002Ze§\x0016lµçr\x001bëîIt\x0004j\x0004Vv[îÑ-\x0003\x0015­.ò\x000fj\x0011Y7Ã6¡\x0000\x0006bJA\x0005\x0002Ð\x001d;~Í+UY\x0001÷PÜÈÚ¸W\x0018ð¯ÊZÙ\x0005$6\x001fE|¼ôgÏ%æ;`\x001b§\x0005#^SrK>\x0004`i8\x000b¯ì"	Ü\x000cÛx\x0002\x0018q\x0005èKç;ÐKTÞ\x0006An\x0003âò¡b\x001b,6ö#ö\x0005åÆµ\x0001¿º {\x0016ö\x000c,]	kÍ¼hÇÌfôýøéó×Zf|S´ì0Và+ìa³.Þ§yrôãå»çú¹°ªà0óamë\x0011c\x0011\x0002L\x001f[e\x0002Ú¸CÜ;Rn%b³Ð·4b4ÏæVß+´´C9mö9|\x0010çíP¸kúþ!M\x0008óüï«N(¸#$ù3+íEÈÁ\\x001eäûót6@ÿüÌ	\x0005ç-Q¸kÚÎ\x0018Eò\x0000wÞðE£m>³u\x001d£_âÝ%ÎÅÝÓ¿æóÞ\x0015i¯,q¥ùM+.zZQ3·tÄ{Ï{W$_¾ÓÔf3`\x0017«
7[\x00083\x000eÜêjT7\x001aËP\x0014Ý¤\x0019Þ )¨\x0010FYCÍ\x001aF5Ï\x000f,{A\x0001IZAÜ¼\x0008w3êî¥På¥ª\x0015¤²Yé ¾QòBiÂ<¾¯uóvR\x0017ª¹Vïnï?~ùÃù§§uEFH\x001dhÜH\x0015¤rÔci3õ\x0005y\x001erôîäìâúèüòæ¹\x001a#7÷¡.Tc­¶BÒ(K6 f¡*OA½ìÒÅ,³M¦¦4Ýäóþ,\x0003CKñ¨2vÒÕ®Ò³OÉ·\x001cR6'~ÔÖ2\x001d\x001d¾¦ôÝ^y²\x001fQm¶e-Ivi2Ô¡R[¹{Pàåªêdd-ÝØ\x00175eì¦trI¦vu×¾¨_þî×2¬ÙÎéþí)°È[Ä&K¶íÕ³¢GÄv\x000eøÛ5ÂÅ&RÍµ2¹'11é<\x000b"bi!WûäâOÞ<§],|Xóa\x000f\x001fÉúå\x001b\x0017\x0012\x000b\x0007%Å\x001aÝÞ¬øy>zXh«$T^¿¬º0Ùy¼ûéÓÓã*I\x0016\x0008OÀÎ©Èm~¤bÏ>\x001d`©qrtrs}uúúòæê\x0019I\x0016\x0001Õ5¨\x001e\x0000õ¼\x0013(î\x001b.àÏ
\x0018j\x0016HmMj\x0007Hæ4ÎÏ¤N®m¡}8î õ5©\x001f 5\x0015nKÐ>Ï2@#i'83øõ[\x0001ëi«NÒÐÝÀã$`K\x0012v\x000c,ÚV _ØÛÇîþ¶`Ùì\x0005ú¡\x001a¯=)XúõÃýÝãº[\x001a-ö¾~®ÏðéH'Oñ¾.ã¯õåÛWg§W__SÍ;8u7'è"µÀX'ÌXî^¡çøå`ÚM¶æ´ýJúBÀ¹c%å÷en´Ôx\x001b§¯9}?gàw%\x00121÷|ØteìwðLi\x001bf¬1c7¦òr(\x0004:øD$W56±Ý	­\x0015u\x0011&øH\x001dó¹¥Ü)¥ÿ\x001bÛs÷ö7èmïj%¹\x0012}zÞ \x0001Cùò} )xÌ\x000e¦ÜÛätîÕÝãÇÛÇ×@êäß\x0003ß)ºô9øþk~+³¹W§W\x0017'Wß½\x000cijHÓ\x000b¹\x001b¦@Ó\x001extd,Â©\x000eç¯]\x001b)]Méz)M,tYÃL(¦îæý!\x001b!C
\x0019º!K\x0013\x000bòÔXêÇÝb$Þ6ÄÝ½6!Ê½övÆt\x000câ2!ÔE>&Jgæý\x0002+1¡\x001a(?Ô¥ÄO\x000fS)`Ê:Ö-%\x001cóå¶\x0005\x001a¢)¥à*%y{fgÜO5)íx\x0019\x0013kLìÇ,\x0013ÐZ^ÊÛR2yçÂÂÐ-ºæÔý«n\x0013§aH1\x001d·§J`\x0013#üåËäµ«ÏN?t¢ê2â\x0019ÓêF¶t²¤ûÆ¦lÃ­òã[NÙ\x000b\x0012Ò)«\x0017}T²¸ûÚo^¢Í#Óü|¬¨ìéõ/w¿Ò«`~-º{üé¯Í>Ý£M(7³Q\x001bäÓ±M;þÒ?ÖC¤~8}K\x000fùÙèôêõ\x000fÏNAõó\x0001£~²«\x0011\ãèÑ(ã*¾¼±>Èl:ÛÌbèÀe-Åµ\x0014Gå9ÛQçFe\x001bµ2h&­%6*:×:®ô\x0003;®<ëp¿¿}úüùîèÇOë\x001e\x0011I\x0012m-e('dY9z5s³yä;ñ~róîÝéÑWÏ>'2´©¡Í7\x000e
Aµ:\x0010doH¡æoÿÏO\x000fO×éhhº\x001bÏY *5¯!\x000c«Z\x0008½Là¯ÏoÞ=÷\x0012¢LÝI0:üáÃoÿ ´úóDõòºzÅãª\x000cugryÎ$\x0010\x001bw4ì\x001d«ùêÕ)¥ÖïÒ/âbc¸Ôo2¨\x0007§yí¸Á\x0001\x0016¢^Ûqu«Çp#pqFú2Cæ)\x0008îRûp+®­qí\x0010®V\x000b_¨\x0015C4\x0017¼ã6\x001d°ó\x0017Ç´PÙ×´u+ûê\_äTÌ<.4¯¯-»wÑeºXã¼\x001f\x001fKñË§û\x000fV-iôòà\x000c^\x001f;'\x0015Ûå\x001e`.øææìÕåÍË\¦æ2Û¹àx7ÿ\x0017.\x0006©Îµq^B¸\x0016ËÖXv+\x0016õ°ê\x0007MòæI
é/»K\x0017·rÍ`w3§¿üôëÝã§¿~\73/e}Ræ MÒ\x0005oKEÆ¼läêòíéÕågßAæ*¡ÕØÜ	\x0003ä-IKÉõN
+ÅÎ°\x001dÐ[=kMJÑùþtwûñèõÃíS²ßw_>=|ù¿k®B(õ7@\x0013\²M Ì\x001et`g:=¹8z}~r¬÷Ýõåùõÿ|\x0019×Ô¸æÇu5®\x001bÂò*pµ\èaTÉÁÜ÷ðÆ7ðÆdç,D\x0017¥(ÅCfßEi'îî²p\x0001xS¾ox;^'ÅÝ5ä\ºq\x0003ð\x0007\x0004lòÐWH\x0015S<¿=Ú¥Ð×w_nïWú\x0005\x0017d\x0000Ë\x0017AäSB\x0011"SµIÊwéóõéõÉÙóÞÁÏÞtH!®yf¾Nê|e\x0016üÙ\x001adjm\x0006®4ðÒÒgy¤>}oº×éxÍW:%çö29ÖäøÏ@îÔìÖ-ýÀkwÇúÊ-\x001aükXÙÕQ\x001dç\x0002\x0004\x0010-\x0011³\x001e¼5Vm©yEË¬í@r\x00192¹\x000bÅú×Nz´Ì¼"{-¤W³#
iÐÔWÿG\x0017÷?}z¸]·4ÎTr=/BçÊSÊ¼ë-ï³¬ 45¥é¥Ä Y\x0002¤Cµã(ëK|§X\x001b)]Méº)µD\x0005T(¯ÞîjtÑwQb\x0019Oú¡î\x0006ÿáÓÓOëÔºCFI­=«ó­\x001aXV¿;úáòæÕùåsrÝJÍÏù*ìjON>þt÷ñãÝQþ×«O¿}Xw\x000eø¬ê©ì\x000bö|ÑQl'VMÏú'\x0017¯ÏN/.Nò¿^]þùä¼\x001aý!ÿ0'Ç\x001cÉ-IiÌaqù(cxch\x0014 GÈuM®Ç×Üh¹*öÜ¡Mõð×<Äx rSñ5÷(Í{ÉqñÔ=,uÑã¡ÜÖàv|É­\x0015µ¤äáD3ÈÊ\x0005·(^é\x0004w5¸\x001b_ñäND¼<(\x001f\x0001CQßµúP{Å×ä~|ÉIÞ=\x000bX[ëVeã¡<K¨ÉÃ0yJÈvJ×Z®1\x0010\x0005íþ\x0003Ç<¯yJ1¼å5Gn\x000f\x0008{k.\x000e\x0003¾{Â\x001a_ó\x0014\x001c«µÛ)ÌO]L("*\x0011\x000fEÞ\x0006Ðñ\x0008JM÷>ï\x0016¯D\x000cÒG©ê\x0001åü¢6²\x0013½ 0\x001eB'\x001fÎs^S\x0006ÈÒ@\x0018D#?\x001dQ\x0016cà:Ñ\x0010
ã1T»"²Î%,yå£dÿ@}\x0007Bob(\x0007Qçt§È)"nzÅ1­º;{&Âx\x0018ÕôÔ¯
¼.B\x00031rÙ7Àrl`'y\x0013Fa<:»Ûê\x0010ùÎ=èRS\x001fT86q\x0014Æ\x0003é¤ÛËé¢Cêî¿/\x0000ðPÞÄQ8@ (áÈ \x000cA\x000c¦TáVV|\x0004½	¤0\x001eIÍ®ÝÊ{9\x0017\x0005%Sº\x0001´9Ð~Á&âx(õélë´é\x0006RÒ\x0017ª(l4Çä\x0011ôöH7\x001e|:È±S$¹;ºSoõ¡\x0016½qê8îÔé ÇÕJZË3iÊ¼¤\x0000Ìëe/G'zã\x001aqÜ5zª\Ê®Q\x0017õ`¬\x0017\x0013å\x000eµ_\x001a×ã®²\x0000Ç×Ø)4Å(Yä^ö`VÚøF\x001c÷t&²<Ù\x000bzÚëZ¼?Ôi|#ûF\x001dÄJ\x001d)øÈóµS\x0006Ý\x0007\x001c\7¹º\x001eÏÕI¾·º#%\x0002ÖÆC/Y£³\x0007¥º½3\x001aOxQRï"?\x0005åÊ=][ø<BÞ$z<i4$8Én¥ð)¨¨ËÐCù\x0017Ýø\x0017}ÔË\x0003\x000bë&t#¹ -ì	]\x001fj¿4Fª\x000fÀ\x0004/¾:4YÑZ4hÏ6i¬Ô[iò0eÌ16-×\x0018°¥ÞÞX©\x0019·Rº»U×FruD½_q ¯n\x001a35ãfjTÙ¦S:F¾õ2e\x0014CTÚ0q3%~\x0019\x0012eä\x001b\x0006Éx£óBoÌÔé4RÑ\x0003°¼XÐEÒ%Úe\x0017h\x001fºmÌÔ)mp\x0019¦ê¤¼Z£Ñ§<á@èÚq3u&9G\x001e`\x0014²fR\x0019\x000eþ@!É¶\x000f\x0019ãfêlÛ£ÜÊ4SíLuC7VjÇ­ÔQ%\x000fout¬\x001d´/³Ô²5»\x0013½±R{\x0000+õfBLèjw{\x0014èêCmu×X©;Òô[\x0016®¶¬zZªà\x000fõLêÛ\x0000wÛ\x0014x¢!ßÈ×\x0001F:ÎCÛ\x00014Þ8\x00187î`<x¹1Ö1FÜz8Ô«ºkü\x001b÷/é´Or\x001e\x0013¹eÑq§wi\x000eä`\ã`Ü¸ñjª\x000e;^¹)U4]â@èqã\x000eÆCîì ð~Árg\x0007Ã\x001bf>ï]íæ½SÕãGÖxüi
°¢9w<0'\x0001s\x001f®\x0005Ñôó\x0007Tðx1IB\½~\x0019R×º\x001bÒ\x0015Ik½\x0008éXS Í¼åf\x001b¥­)m/%u\x0003!çQ JãÒå\x0018Õ¼\h\x001b¢¯\x0011}7"\x0006YH\x0013
oO\x001aÐg%þÍ\x0007×QÂ¼5\x001cL5÷ê-¿»ûõþèüiMQ«I'ró6 \x000bökIê¬^(KOUß¾=;:¿¹xÆvt\x0015_Ñ(öª@ìííýçO\x001f?\x001f<þÌ?ýË:¼°KCé:ËîPÒP*¾Z½=9{wyñ.-ìwÉúÓ¿¾{\x0019\x001ckp\x001c\x0007OI3WHx,ÃÑ²a\x0001
9=\x0010¹®Éõ8¹.ÃZèÊWPËÕB\x0017jw\x001aÜ\x001c`¯¤d\x0008ùéU"¦$ñ\x001f
ÜÖàv\x001cFg\x0002ÎBú\x0008P\x0010øy$]ä®&w\x0007 ÷ÔM8§Õ½R.s\x0000\x000e¥Ü×ä~\x001c@d\x0018\x000b¸Q\x0001\x0016ò=óUºÈCM\x001e\x000e@n$ç÷;e$TVÖ\x001cÍAE]ä±&ãäJ\x0015gnD*:åuN\x000c\x0014\x0017£k;ÉwÅWS\x0018RÃè>éP>\x001dÒ³\x0014\x0019¡;7s\x0005Ünô6P\x001fhK{*\x0008Î/`£ìôns7z\x0013Ca<ú7;)102\x000b¼\x0013t³oPS\x0017z\x0013Da<¦ØYêÜ$Ó1¡\x001byG\x0003³\x0018kßÞQ\x0018£S5\x0007#o%u\x0001Q
Hè
GÐ\x0004R\x0018¤´êÀ«Nst¬z(\x001bfOkÁ&tcM/R3úN½ã»»¿\x001dEgÖÞ;qÁ\x00155è\x0007#Wf»°W\x0002ãÇéÿþ|¶æ³=|°¹`ôEøyÌri¯ÃÌV:WÓ¹®ÕKÇ\x0001\x0015\x000e¸Õ%`,5\x0019º~½ÛÈ\x0007Í×®Ïkí(\x001eãã¼ï,ú¯Éù~>Ýðé\x001e>FîhÌ\x00165\x001e\x0019Ù±ÿûVóZÏt­-¹%Íä\x0001\x00082SÜ7âè[\x0001\x001bó.ûÐP¦³\x0010«gu\x0010å4½»\x0001}\x0003è»\x0000¦Züü\x0014D® ¤35`"¡\x0001\x000c]Ø¨jpæÉ×ÅC3q+_løb\x000f\x001fæøjæ5/ QÑFÛ
X
³¡\x0008¢ú\t¤êè|\x0015½«¾0ªÌÜ1±\x001f\x0010\x001a@èZÁ`äµßxÌ3CÌn\x0004ûÁÆ	b\x0013D§ä\x000bS\x001c\x000b\x0004(/n\x0011\x0007¾pcÃØeÃ4 u	\x001bîC\x001bl©'÷\x0003_¸±\x0011ì²\x0011eC9\x0019\x0019d7McÕÊA\x001aû½ n¶ îÚÊRpËÇ\x001fãÕR \x0004¨ún¶ îÚ*×\x001ee@±á\x0004¨Êy¾ßIë&Ìé®0§Lé"õÔ# E(§vÓó³Àî´KO\x000eÐH üx{ÿok\x0000*
 ,Ú¢rfq.\x0016Ä:r'gÿòu@\x001f¡½Ð¦ßV5ìô¯\x000fé`_	¶Ý*ù»\x00084\x001d \x000böy\x001a®EØµææÆî\x0013ä:}s\x000e'ôdðöÕùÙÛËëù±æÇñ§MËþbPxÌøå\x001a0Åô×^~]óëñ»©¶uâ\x0007ÇõPN\x0007îÓÅ\x0018÷J`õü\x0005lý\x0017°\x0007û\x000bP_Tà\x000f\x0002kþ\x0002F´?Ó\x0017X^Ówþ\x0005|ý\x0017ðú\x000b ÝÖó\x0017HÇ\x000f\x0007&0äô\x0017Ðj9Û°÷/\x0010ê¿@8Ü_ÀeEõ\x0018td5Sg¢àÙ3Þ£\x000b?Öøñ`ø$ dÙ\x0003E¶`«Cq@Èü»»ØÉªCý\x0005HB:÷7F²y¾
Iò_`ï|®¿@\x001b\x0002\x000e\x0016\x0003HøÄkþ\x0002j@c\x0001é\x0013,¯Ã;ÿ\x0006\x0013yQ\x001a	ü	¼=$\x0013ì0ÚåmÛæ¿@GáJÓ#WLèÛé3æ_\x0010=\x0018ÃwúÖi6á©®wVP+H¶¡c\x0007BGÅIwèXÐÓÒ¥\x0012£ÛeÇc\x000f»­Ùí¡ØóÝ¨A´\x001d­\x0003Ü)ÿ.ÊízØ}Íî\x000fÄBm¾3: ÷à[ËÃ\x0005ÑA\Ý÷ \x001a=\x001c\x0006æ´æÇ·h´â4>­5ß6crvð\x001eöX³Ç\x0003±g]¨nÚxÙÅÕ»fxI7:´Næ@^Æ¦=î³¸MçOMf3døt¬_T\x000böÀ7n\x0006\x000eäg,åö\x000c\x001bÛ'xËõ¥¤°¨/í×
¼>\x000cü$\x001dw
Ùm¾½³F(z@7âàoyTÙ6'Ó\x0000©´\x001eçwÍ@êÿµê¶	Ï{OGC\x0016k \x0011°\\x000ck«uNo«QÔß?h\x001a]Ä\x0013*ºÉºÿóìèûÇÛ?}ºÿ|ôîÓ¯¿®\x001b&C/\x0005¹¬¼\x001dJ'¨|ÛcS\x001aPßyÓqurñúòìÝÑ»Ë·oO¯¾ú\x0001µI8Ò}ðÖóúñé\x000bË¡½½}ür¿Fç^çYc>Ùã<Í!ìò\x000b¦8\x0016õúêæ\x0005ÑÞ\]]<GÛ^¿¢\x0017º\x0004ûpô@\x000fî?®\x0013é\x000bÉ°ä9Lu\x001cÚ®5§ié~r~tNog\x0017Ï=Sâ¼n\x0010¹nðËø\x0015¿8·Ô\x000fð9m2\x001d~ä¨#Þõâñ¿åqfÓÿ?§
5Uè¡J	3_ZëxÜ^@y9MÓáJªÝA\x0005elÌV,ÊË\x0002/\x0016biø)RTµq<5\x0011é*÷Í?Pîû&m¢J)<!Ù¤â1Qüñ\x0001cL\x001biÒ
\x0002íI7}¬c\x001f¼Î{*ý§\x000cw¼Jöd£$%è_\x0011×«`°Á0!_ &tÒDÉ/ZÐc\x001f®aô:ûL\x0012Lò	T¨vLs2@`´lè­0¦1ë`èÜ\x001aù3!·O0&w*Ñg;­0¶±ë`\x0000óa.Á¸@Ò\x001e\x0013\x000cf\x001dûôF¹\x0011Ø
ãj\x0018·\x000eæÀùò|fá)ÞôlçÂøÅ¯dÁ<P\x0016Æ\x001cóha$8o	5LX\x0005\x0013Ë×f\x0004ãÈÈ	ÆÆbÙ¥/o+L¬aâJ\x0018 Æ	Æ\x001aò|\x0013LÈ

é?]Ô±6Â°\x0015§ÖÑh¶ët®ÇLB\x0003Ù2}\x001b\x0006Zï»Îý\x0006çs&Á\x0004J<&\x001agdY¤Xp+Lã}aûõ\x0014µ3\x000bjñ1FgIXò!è3kh¼/¬s¿ÁÚcùJÓÑbZ\x0018®£Ïä:W¦ñ¾°ÎýRµXäÏaòÒð¦¡¥é¤iÜ/¬ó¿)}Èµk´6hH^\x001bY\x0019ÓÉÒx_Xç~½Ç²0fµM\x000b\x0003\x000c£bvÝ¸_Xç\x0003eR\x000c\x0013ËQ»
l;W¦q¿°ÎÿÒ§AþJ0õN\x0011\x000e\x0001eilÿÆÿÂJ\x0007L­¶\x001c
pz>8`*_èûPØ8`\ç½VùBÖÆµñy'­é\x000bØ8a\ç}4¹\x001d$ob°qXhB_\x000em\x000e¼Ò\x000bÓ#5\x0014(	Ú ø\x001aÒ«í¢iÜ0®sÃô/)
L}\x001bÓÚ¤³¦Ð¨Îµiü0®óÃ)ûÎ9¢\x0001D.\x0017×\x0013
öY86~\x0018×ùáÉãñ¾QiúR®ø\x001bßyBÀÆ\x0013ã:Oì\x0001Naº\x0018Ö\x000b&ê;<aãq+öäo8~§¬\x0018
ïâ¬áFk£ûÒ,l|1®óÅÓµ0rI<1û\x001bpFhb/Mãq/&¹,É@Õ4=rZ\x001b
ò¥<ö%ZºñÅz/¶Ô\x001a%·19·\x0001t%2¸¾]¬\x001b_¬×ùb\x0017"'µÑFC(kÓçnt{\x0003°Îùºl\x0005#&\x0015+öºÏ¤tãnô:wC_
IAvÅèµ)î¦s\x0013»2¼uçrè5PJeerò:rüèJþ×yÈD\0áj¦d_\x0017
½,Ö%
Ü¿óÅÚ×\x000e½0çµ8Q|ÕG7\x0014ÓéV Üèýáük8q~Õ\x0017¥ØìúöÃÓãó\x0018	\x0010	Iq£1Ce[ô\x0008}òêæêÙo\x0015çW}Q*Ç^±¹\x001e\x0016%Ð]v	r\x000c7ÊôÁè\x001aF¯qN¾P ­ÔÌ¿\x0010õìõ±Å¬\\x0018%V\x001ehÈ©¯$Ç;__®m±5]	ãó,\x001bÐ1ýé>ç[Æ8¾Ðh:a\
ãVÂ8¾\x0008.å7¼c$/¦>ÜNP³,1?w& è­6Ãp²\x0005@ß«\x0007¦¾Ï¥\x0006ê%àø®$&g³I©\x0016\x001b6øNÃÆfËàÊ=ãL~\x0006¢«¾@I`¶¦r9¼åYwÍvÁû%í\x0012¹3wA6xZãÌï®\x0006ñ
_	ÂÊäëb9_\e\x001efÓâÊ]ëvW\x0012q\x001aþA$\x0000Ø\x000e\x0010ÝlX½rÃºX\x001ezÒÎò©R+¹(ï³åò(,NN©<ÉµHÆà|9åR[\x0016ï\x0015Ø\x001c\x0001Ü<N;Ó\x0017wOÿúÜ%VÉÇ£T\x000c§[,È8µ7,\x0017§7ïW `«PHÆ2;9å©p/§å\x0005ÁÍ½ÿJ\x0012Su$:\x00171ST4r7m|0Ï\x0016V¸Ä­"ásdH[\x0018³§µV|
 ê[Psu\x001cZ'§\x001e¹ /IK\x0019¾
¥\x000e@®\x0004 \x0017XDO%mÙYòå¢-ï¶\x0010t\x0017J³caÝ5%}:ÒE\x001a£èâ¶±\x00192¨]]iJýßß>ýÛ×""\x0003ÚYG\x0012ÓÍ\x0007Ý¤SeQÊÿßÜüËËHX#áz$d£v8©éMDéHÀDÊên"]\x0013éÕDôÍòöqzª\x001aÊ$k\x0004õEùF"[\x0013ÙõDÀ	\x0015Õ \x0006^#9õ«úzf#¯yüz ÛhêÏå{O)©U²ûÐdæ;Ûìí[úº±¥\x0013?È\x00133J0<ÜKÏÞ»geÝ/é\x001al_)ú×Áty<LÙ(¿J%/-á\x0002=vqÍËl`*³áN9AûÛýÇ»/_»6\x000erý\x0017ÂÔ\x0007\x001f?<\x0014Ï½+]rÄ÷ãÙÅéõõW\x0008§t¬vVüC;-øêîKB$àtvõÉE¾ýôñË\x001f¦¹?\ÝýúwÂ¤ötÈO4í"ubµÏ~)è°îÑÂ]¾ýsÕ5wuJ3w¿6Ü¸ÆÅ\x001a\x0017;qcÈÊ	.}lÆåáË¢^ã¸ºÆÕ¸*Ò\x00116¯.ßQ\x0019\x001a\x0014\x0012\x0018×>\x0010®©qM'nÚ\x0001ÓuMÂ%\x000fÈ¸1·ñ\x0011n<\x0014®­qm\x001f.²Y^\w\x001c3,ævim\x000fµs]
ë:aÍ$\x0018×ÖÒðeÂ¥;º²¶Â
5nèÄ\x0005Èo·kHzÂE<øV\x0010\x000evcª×Qûg^ï#LÀÀÉé!y\x001b?\x0006Ì¡Íív×çõEeÄïÊë8oãÈ ÓÑm»8aòÙ9í,g:\x0019\x001b\x001e\x0008·qdÐéÉh4ÙYÎÎ\x0001°l\x0007yB\x001eçm<\x0019tº2\x0017 _äåu·/\x001c~}\x001bg\x0006ÞÆ\x001a»²¼\x001c×\x000b§åµ\x0007Âm\x0019tz31\x000béçÀyyIÄLxÍ\x0017¤\x000c;³2ÎúJ¶%!ýi}M,Û$ÇyÛ¬¬Ó\x0019_y_Ï¼>F]Ì_Çy\x001boÞÌj.'Îy\x0019æh¡äð\x0017?\x0014nãÍ°Ó\x0019\x000bù`HË\x001bòEjZ^·\x000b\x0016\x0007ãm¼\x0019vz3\x000bÑeyÉËkÃny\x000fä}±ñfØéÍ\x000cõ´°;Óæ?N¼PÜ\x000fr\x000f¾áõ½ë«ó\x001boæUìÎx4+ñò\x0000åqÞØðÆÎõp¬\x000b®ãí\x0000åÐæ\x000f´\x001btã|uóuQ¹¬]åóshrpçè\x0008ÈJ\x0002ã¼í\x0019³Ïýwò6ÞAwz\x0007í].}D\x0012)¦<â¥^jÞ\x000eq,¸ù¿¨§ðËÏ|GB7#ç·GonóËP®dMÁØ~½»x¸ýø%ýq>Z\x0015\v[\x001e\x001dò£¼\x0006Ïn6e`6}{zv~~rqýÇóæäkOD-Jr!¸\x001aúÙlFq'\x0014/$Î\x0001\x0014ÌZ\x0012°$\x0006B Æ¶Ã\x0004\x0012h£a+ÉÇÛÿõåÿüÊ×\x0000tøO$¯\x001eïÿ÷\x0013]¨=Þ¿@äÒ	,çö6ýñ1ß¶k­0·qz5X"½º:û\x001f7t±vuö¹\x0005´HÉT·?ù\x0007¹ýyóÛ?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=/qöMê{}¥J¢p¯OÒ\x000f¶uïø~¤æ&¡0\x000b\x001d
«¦À/v_ìê­Ïìéeßö[pm»íA-ÅM\x001bQ$7%¹â\x0014²\x0002µ\x0012®Ûs¾\x0017×Õ¸Û\x001eÕR\+1ñ\x0003>5	ZdÂ¾i··ï^\_ãn{Xq
\x0007´ ÆÆ´ÅC\x0015kMPÃNX\x0017°¦\x0011òkòªÏ´ltÜ9õÒÆvÛ;\J\x000bÍiâ¦)\x0010­ô<\x0013_ip)pwÜÅ¼`ã,.Äï<Ù8«yxwâw½¼jÂ»í>.æÕ¨ÁÁX</p><p>\x001b*=ñUs.î"^¼\x0015ñ±ãí.\x0005ÚGb\x001cÛIN½ÝùstáT5ç®W¾0xº\x001b²Ü\x001b±ì¢Ô5¥î ìhv\x001atÛÚþ{"]¶æÜ
T4GD\x0003V\x0011Ñm®\x000bÔÕ »!e\x0001B:@ÈÔK\x000eê\x001223\x0001A}
º\x001b¼X\x0016RUæ*\x0007ËvCª] ¡\x0006Ý6«C®ò+Ç\x0017wC®] ±\x0006Ý·,\x000bÉò§÷9\x0012I!ÙMlxOO¼×.Ò:d»\x001b¯]c<åÔ$uÙ¤æxn\x001b¨´[¶SÚmÛyzÿáÃÃÇëCé-\x0016ê</p><p>ñòWÒ\x0007ë^.ÕÌR:}ñìÙÕó}-\x001akPUª\x001eP«è»g]C\x000eTOçrfD\x001aÔôú%½(\x001ed(`\¹8\x000b\x000e.\x0007µ5¨í\x0001\x0005õ_LÌ: b\x001açL¹Rîæ4¯Íõí_®»ÿýx{óéÓÍ_oßþ3Ø.®?ý9a=f buyÿ\x001bÌ</p><p>»ùîÙ54Lùtû%·\x0003Pâk*-)èÿ\x000bm\x000b%Ç¬ez|´NçòÅÿ\x0001ÆWpêÞ'ç¯Îüx~vyyöóÓ?æ¶Ë¿ìíêa_¿ùtóþÝ?\x0001\x001f¤+ô¤¤íÅ§»ï?b à-Â?$ú/\x0019×)	¶Y$8mKéøóÀsÛa\x001e'êìïeÚ«û*!r¥ÏË?¾x^\x0015{Ñ kÏ\x000e4á\x0003®zë¡\x00043ïN	Íbo></p><p>4ÁA\x001a±w=p\x0012Ó¸Á\x0014Õ\x0008§Ñ,ÖìÏÀm\x0016w\x000c\x001d}RÚÙ0lX\x0008½ØòÓ\x0010\x0019¯ò£cÜ\x000cöÉJ1ö8TqHt"ít</p><p>4}ò£\x000eóB¦<\x001fCSNa5é 4:å45ài§KCCCÎ(<C&ÛoÑ£\x0004­j;:çr\x0001h~´]:AÐ´ÉºäÄÂDçñH\x0006÷£\x001f6\x001f\x001fíÛ\x0018ñLCÎa\x0006§ÔöäP\x001e\x001eºÛ0Ôv=É.À\x001c2\x0006@Åtüa\x001d0uó£\x001d\x000etÏpô@âÁá²Ôs:mvN\x001dÞR\x000e\x0003\x0006\x0000\x000c}þ\x0018§åNOÀGÃ§°Á\x0018´ð'ølç\x0006\x0012ïó,¹Ë¤âµ´%«8>~2w\x001cÀgûâ\x000eEÒ¶ì4:®iA\x0007EæL\x0004sxõ\x001e$Ì:Xøì0i\x0002û£ÁñDcE\x00105vUÎ\x0000\x001aÚÛà³c\x0003´¨\x0014	\x001b Á$oÕ´Ó\x0006xØ:\x0008hÀßÅg;`ò¢<ú,Òê9ìÐx0M4ª-ö\x0011¾Õ¿Eùj«êª£§î?Ï¢¥ê¨<ÉF\x0010YLû<i*bþuò¥ÅÞùwvôôòÅË\x0005\[>ò2.H¸òÈ\x0015%¸yË Ê\x0010Ô¾»\x000b4}¬nâJ\x000e±D%J¨³Ä¸áÀ¸¢ÖÑìu?ëQS»	ß6XÞ)ÃPy\x0013	\x0019Ê\x0005I\x001fÑï5c\x000bÒ\x0014¨Væ²\x000f¨\x0014^\x0011@.£\x0010gþRÒ@¥#ïðÄ\x0002G8´}À\x0000\x0016¡pe©§Ì%6\fßv¶K\x0014g~4}DHº2\x0019\x000cLÕø\x0011qô\x0011Ã\x0001®ù(Á½ÏÑ­5Òh%S/q´\x0012¬¡ÑÎ@c£Û2åGËhN´A0	* +Mâ²{ý¢¥X\x001aÒ9ò£	Kfû±Ò\x0002\x0010¸</p><p>JMK\Zî;Ç,\x0006ÀùÑ\x0002\x0016¬C77\x0005\x0003ð0»¢7\x000c\x0016Ü}ë ©ËÀ\x0014n\2FÚ$\Ôå3Æ½¾År*\x0005TÓ+(y\AÜ/	UÀF'Ñ¦[¿£¤nq\x0000æAë&)Çß1áï\x0008\x001bM~´¥Ó\x0013º.Ú\x0015Ä\x0017\x0000,8AÛbt¿·Põ\x001fM`Ú`©N\x00023¹_j\x0006Sä¿j¿Á\x0010X\x0016HvÕ	oñ¯iÄÒÞ\x001aÉj;Ç`X\x00108\x0004\x0006ku',DÐ\x0003Ab\x0002rHÒùa×ËÁåk~4q\x0005ª\x0000Y\x000fK¦Û9­xÅ½ÇÍ¥`\x001e.[ó£	ÌRÏ[è &Á¿ÏNa´äSx=<Å<ø9¾ÑÙÉr²É\x0000Æ\x000cæ)¬¦½Ý\x001b}Y</p><p>\x0016 ±5?ÚÀÜqÄEiD.ò@0Á#6ºW\x0004µæGwOx	Ëc¥Ø»§SGÐbßAm1\x0018\x0008}äG\x001b.ã\x0005{!0OÛ~0n\x0014,Â\x00194úÆ\x000fi ï3ây(­\x0002äÊzex\x001cÎqIP}Ï&°tæ¦5i!\x0011ìðD=ºÁ\x0012¹FKf\x0011ö»K¶Qæ$ ÓxÀÜè\x0001$KL<ÁgÓ)w\x0007\x0010\x0017\x0002mûTÑªÓ*Ý\x001bã^Szó³i¼ Æ¨\x000bÃÝU;[ÈFC\x0014\x0012ïUdëöªAË¾dPL1SaLÚ<>[Ã:|Êõp\x0011Ja\x001d\x001a³tn\x0013\x0007Î!³§I	ÎÀ\x0013|¶\x000cú\x0018Ç\x000bý
n¯ZôjÜÛÎñºþûÍo¿zK­Ùr\x00132®?¹}wóÝéõ/ïn\x000eë0öD>6{p³ô,¶\x0002ÞîÇì¯ÎÓ/OO~üþlïíÊ\x0006\x0019Ä´\x001dC\x001eo÷}\x0016R\x0000Yr\x000b"»óJ\x00072¨x3\x000c1O\x0008ïA\x0015Íó3(G·ùê ÷àÄ`¹åÄOé`N\x0007¬°}\x001eñ­h¥Ù{ÕÖK
Ã\x001f\x0003Ô\x001eê3\x001au0Z:M\x0007
)f\x000e\x001a]ØpoûDÉ±	"¹ËZ:(\x0019
	ò\x0018AÄ½Â\x001aÕ\x0006=?£³c§\x0007§´¢eR&÷QRÌSK\x001f\x0010ò\s\x0015j°¤zbNÛEY
\x000bMÁ8\x001cÊ¢:ÿgÝ¹áÀs\x0013w®ZÓæa¡³ß"³°z¿qëböpsæU\x0018c\x00123vT\x0014¥OgG\x000eð</p><p>\x001b×Æ°×c»GÚùÈn\x0010Q[rWk\©­3øØ´Ö*b\x0000/12¤BlÏq2\x0011Ö#\x0001®¸\x001e³ãÊ:J\x000eÛ¬\x0000¶	<G¤qû#	Ø\x0011°Ç<&e±v\x0001¨
¼\x0000R{60Vì\x000fÌôQI\x000cvQÁÍ6Q;\x001f2+\x0012òÚ¦<Ày3?\x0006:Pº\x0000ÜÂP¤)4ûyÒ¯=«¡ð(?F¨1$\x0007\x0004¸ñò!Q\x0007\x001fQ®ldò_\x0018åè`KTiHØ.gkflïh1ªÕ©Aè;?¨-\x001e\x00135q°ÙµV3AÒNj\x000bÔ\x001bv\x0018©\x0004jI7o,o!J®m\x001c#ØÅ8h\x001c%¥\x001d,¨Íã\x0014á`Òrü«\x000f\x001b¤ùòc\x0004Ûc"1Ðé+QóæÜíu7?µöBy}J:¬Á·ÐòºÑ|\x0003\x001a+sÃbÄç\x0008·\x0003\x0017rûÜI\x0008¹9 ^`]«.³î5>G¸ãÙ\x001d¡¸©\x0016</p><p>\x0000Õº³;D!\x0010'üØÆ
U@</p><p>­d²\x0001\x0014ûM/´Y\x0019û±k36ìvtàÍ\x0005¶\x0001bÓ\x001cèI\x001eh>>J	aS|\x000eµÀRë4ÖÁ³Ìõà¨µ®|4"Ú\x001dâ&@êØ%ÑÑX\x000e®|¬ Tù\x0004S[FÊ{1|@Ð1jN|Ù[dÐÉ­A@\x0007C[·.ÜFÐ-¼7JqÞ\x0002Ê§¬É
\x0010ø\x001cÚº©Ü\x0004Ò\x001aBq]µ¡D\x0010È1^;Ç\x0010ñ9Ä]ö\x0012e
¢\x000cüÕ+oà©=ÁçÐô\x000eåSJ(ÛÆ[ðõÚ\x0016>8(ZÉÏAK\x0019ñ¶1·S·lqèfC<¹.nLSÓ\x001bô¥(`)J¸A\x0019¤´y¯{XP¹\x0000GÕe8]Øp\x0007ØÉ%¤ÑN&bÃFµ±\x0003\x0004´ós\x0004;
r§?\x0006f3sS\x0003h¨XÉ\x0013éãO|p[\x001a\x0005\x001bSi¼E`n9s7ÜÂýÆøwá=\0Aþ&üszÐ/ï\x001f~¿½¿_T\x0002Ð°\x0012À\x0005¡Põ\x0001² È\x0019\x0011öÔ¥Ó\x0017ÈùòÅÕ_Î/ö\|\x0016°M[\x0013\x0014Æp\x0002DÜ¹lQªXê \x000e\x001d\x001c´M[#\x001btÎ¦\x0012(%°¼-P~\x001c\x000e\x0002ÆOò£íF\x0015èÌ¼´fðBg\x001f*á\x0011»!¯f¸\x0008\x0017ºùÑ:ß²K\x0000p\x0002»XotÍ.|ØõjZá$d*>Ág#\x001d\x001c;=­ÜÅ+Ó)ìÓ\x0007«!\x000e×ô;KL;Âî|.}c^«\x0016D:Oìl*ít\x0001n}ó³ÎA!\x0011\x001d49ÏpÖñÐ9µoÕ\x000e\x0007!-|6Â%;b-ý¾«5Ú1Ün9Q3ÎiWùÙ\x0008g©Õu¹m2Âi®Fun÷f¿\x0003Îe¸öÏê<\x001b\x0008h(,\x0015³VQ©ób\x0005:O\x001eðl§Ãï\x001a±è>ñrpØØv,å\óbu.R,p>7ÒñóÐÆuÎ\\x0003ØjÀ\x0012] ÚvWÚ\x001fÔ_ÕÝ{÷vºòtZòWµê?,µT\x0003¸¸ã¬6Ã\x0019èþÏF8)Ñ%\x0005º\x0008g/ 3Að»÷\x001dt>Óùf:Hâd:Í;ñXèÄ¸\x0005\x000bPùÏ6:iKí®r¤ì\x0016Ç((Q>Yÿþ%ûö7ñOù·\=º'OÎ?ürýù3à}\x0006\x000577\x0007í"È\x0008ÓõqÏ\x0019¡ÏP¦SÑíL»óg?¼|	|/AÂåéÙ"¾,\ÐÃ§Ó^\ð0E1\x001aâ¢À·\x0007Û\x0005\x0018²6@\x0017 K\x0003D\x0003âg\x0008è4\x0003b§Îa@8þ=ÉvÂ4\x0003ÑÃtføeFØ\x0011M«àw£¯]àíäG;¢q\x001c\x001fÖæ`À\x0016óÏìsºøà\x001fí|iÜ(½E+G7xÉ\x0018FÔ»%\x0012=¹!P~´#B};"*¸\x0017ÀA4T¢
-¢v¢\x0006]àëåGÇ :òå£ò\»\x0006¢ÒÊÝÛÛ.D8¢åGÇRÁ½F% ,7Ië$ÒGön÷Â³\x000fêVò£c\x0008\x0005§¦Ã\x0014ev¤!ä\x00114»9Ç]päËvB\x0019dBa)í.¹4\x0011\x001f\x0011ÓèAÔg\x001f\x001d\x001fY8T\x0004e\x0012O[v¼TÞ9\x0019u!aÏQT$é\x0012k\x0005'¥<2Yv»eÞ
\x000f÷ïíßäDtá¡</p><p>ú}¾ýxóéöæ@<Hré\x000cHiTO\x0006i2Úµ¥ä^UÁ¾çÏÏ.Ï÷	\x0014ÖE£¬RxK\x001b·O\x0006\x000fInK±\x0010Øn,µ\x000f²hu@:\x000cTÃHzÔL\x0005Ñ-Ãú3ñ"¤>È\Dø§\x000bR0¤wEîM[Ö-\x000b»¥e]®Z\x001f¤"%t\x0014À8 PjVW³+
¥Ôùø®ú0îÞ\x0019S»"³&=¯ÝNH# }i\x0000)litrli,ãªyä\x0012¹\x000fs#X×)°¶\x0010$ë,M!\x0019'¦xD×¤\x000b³R_ëÀLç,Ò,6Oúk®¶Et\x0018´`j/o?Â\x000föy>ýùúËÍõÃ¡;U-09×YèWªÚ{</p><p>,AÖÔ£xWG§<yuvrµ\x0000lbm\x0016\x0019E\x0011¨ÐT$ñ\x00139j\x0003×ã`ÉÓÉ©"m`Ã\x000e6\x0008R$\x000b\x001e²G±f2\x0008syÑLfiI¤íë¦\x0013YùB?></p>
  
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

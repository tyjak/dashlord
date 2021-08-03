
# ZAP Scanning Report

Generated on Tue, 3 Aug 2021 12:20:33


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ltF8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-02.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-02.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#gfyx`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#ltF8</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-10.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-10.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?='2¸ÑáS\x001a²EdkØ
T)Ì]Ðt¶è«ÑvÖÙn<Ì\x001cxÓµ\x0004ä\x0012ØÈÕÒ1\x001e¬[\x001cî\x0010È¡
]sv	?Nh\x000c?ÌI°hÐ\x0019+ \x001a~¸ÀÐi\x0017"Èù\x00137Í8ßôØ\x0017ñ2À\x0011¯lm	ûy»²<\x0005\x001bÏ$¢xzxÿýRr)O!g¾ÑBz¾Áo/þ¸ÿ\x0002\x000fAh=;#çær\x001f-8!P®HÃiNcØµ÷\x000eG$¢\x0013Ûëxa,óA\x0004¹dÚÞÆn8l<\x000e,xä1(#Ó\x0014>v&×3r:±\x001d^E¹èîÓò\x0002'_º\x0017»zônIÉÉ½áÆ5âÅ8ì\x0019Uôí:\x0008
!)ËYOÔ
'\x000f{¢4ã5»>t\x0015Ü\x0006Ó\x0001Î²çZÚbI·MÊ¹%)wL¨\¤\x001f¬QYY{\x0000y¼\x0004ÑgtVSÐ\x0000'}ÕC\x0012{M\x0007¸%)\x0017(Ú\x000bÞ\Ì\x0014þÆ}ZÎÍi¹hFÓ®"ëô\x001c4³<åd\x000coºÌÀÕI'&hÓt&_¾`2»¿)ì3\nÎpin\x001døLSî,F\x000e\x000b|ì²\x000bWû\x000eÞ\x0018MZdå\x0018©ö.Ð©6¼]ÀqÛ ôÈèÌÍ\x0008G&U,kN/=W³\x000c²ÄSÃA\x001c,Ûf1Èým¦¿ ¶5
Ð¶þÉ«?,ç\x0003Þ*=\x0018ák¥ÂAV\x0006ûeÌçv1_KIÁÆq¥ýÇñ	h­|\x0002_fÆL\x0011\x0004¥¬ö=¾çøNñXr:kk\x001d}Æ«K\x0002Èµ\x0011þ3<Ã.ßT²ìvÂ1eÔ\x0011Å·\x0016\x0015NDÔÀ¿u\x001b4Èâð\x0019ao,Nß\x0015d;=ðÛØ\x001aE¾ýñá§_|³QúHwJÙp	ÉÔÓÒ±Äp©\x0016eùZßq
~'ý#]®Ek\x0017M¿kR8¡$1PK¿>\Bó\x0014<`îN%\x0008È;Ñ"[7¨¹ß,Ñ¿ÿåÝÛ??¼YjôÎìjôÇ/\x0017§B\x001ag´J\x0008\x00161§T6\x0014>²\x001c]£t<¬Ñ{oF~,ã_©&ïLáüêí\x000béO¨ïþîÃÓ7ÿá\x001fç-ìÌn\x000b»ç·°DÀ.Ñ¯K5øet:B>
\x00135WÑíÞ¿¥ÀØ
]¯qðÒ¸\ò³¿vÞh¯Þ}xûOÿ?sï²cÙqd\x000bþJã®¿\x001fÃ¢ªUÕ\x0017Ô-µTÐ4\x0011IÈP¥2¥|°(\x0001\x0017¸¿Ñ³FO\x001aêqÿ\x0001ÿ¤¿¤Ý|³}-s÷T2\x0018I \x001e`©¸Âo3s{.»ùý\x0017xü×wÂLøì«?üáîýû¹eò®_6/\x0006\x0012®>Àvü\x0016i\x0003KçoÉüúe\x0015Û""sêú[B+²=ò½¿vo\x0008:üHè´N?
Z\x000bÍ»ïo_~ÿ__L«\x0018ÚóúvÁ×ñiâÒBÓG©}Àûø\x0015¶æ\x0006»ýjÜS\x0008K{pÒCÃõvÐu\x0010Ãëüx\x0015ªøØçÝ\x000c¯÷ücsûè	\x001bº³g3¢`KË>A\x0019h·8oÙ%äaal\x001dÛí:rÄ\x0011TùDVaûya\x0016a\x000f\x0019w-4e|BG3ÛÂ\x0007'ãus\x0014OØq[úG\x0000[ÜçN±\x0010¶Ñ~±{q{{óÝÕÌâ\x000foÿúHoÍ¸mBrS®\/aÚx¥eUW¿Ïõ\x0018Y«?èq7R)²ãnN}ï/ný÷oÿøç?\x0019¼õG7+\x0005g'Ì¦Ëm\x001bÙd\x000bò\ÿÇ\x0017p\ÖÑõïý½³EýÇê¾U×þöÍûo£Qtñ¾°oM9½/+Î\x0005{~I\x0016~6÷é\x0017$\x0012ïO3³;õ½¿xºúï¾ýö/7LÏ¾Ù;ù\x0002_ü¤zz\x00032ùÏî@}
·×û>ßõÀ\x001fw£\x0004Þ·÷
b\x001cmÿÇñ{qL¥ýÜXç2 Aw#\x0018wflì\x0016ù$Ù\x0012ÍÐ~1EÐéGBç=t\x0006èNßpÆtåy"äô¿pD\x0017ç\x000eD\x000eÃkiîà(_Kb°\x00171EC3\x0003.eßÇ\x0011rÝç
´A·%7/Æ¡+(/WÒ;kÙ\x0017³ó\Pv\x0005¶tò"\x00049Z5/¡3x¹ÿqóºÉðcif\x000eL³ä\x000cO÷ÈW4ëí2:#ÀO¯±3W>ää^þ\x0007¹¸1\x0004râLÙHÉ- åXûµ5Ö{"íh´ºH
*O®A\x0005-a^K\x0007È\x001eÎGswíõy ZhÈ´5¥ÙÙ\x000eÁ½\x0005\x001dþ^\x000eÌÏ²LØ/ÌÔ\x001cá6Ò¹ü\x0012÷s©@ßÎlVFê\x0004\x001e&Ê\x0005\x0002N²àc¡\x0018Eræ\x000b\x001bu"\x000f\x000b%´8a<3ñ2\7¢Î`I4RZL\x0002rùâ\x00015¹WÅ¦\x001a\x0015 \x000fó$5Ö\x0002¢qØo\x0008\x0013]F{dë\¤\x001aÈvØ&\x0019S,¸áiº\x0006m
ßF\x000boW¶i.oÖ
|b\x0012\x0002ç9ãïèÓ(Ö,ïDy\x0012¿á£­QÖ)ÊXx¥KG}Ò¥@¿¶ôúÝÂ:\x0019eb£CD\x0013`Cæ§&:W\x0005\x0000yX§õ\x0011Q\x001b[\x001b2­¡jÈ1¯Âï\x0013\x0019b5\x0013Æ$\x0008w$\x001fJöØG%Ýó4; Ç/0
LpÏ´\x0015RÚÊ:²ÇZ\x0000xX§è\x0006Ël\x0017¹L'
§S\x001c\x0000r\x001f"^\x0018'£Ç%åæ\x0012ÇLÀì:êÂ8\x0019e¤ \x0017F\x001a"ÈVéÀG&ä\x0018Í<Õ\x0002È\x0015ÎìG3fí\x001dõ+ËY°¾\x000cd0NÑF|·dt;R\x0014OTN´9¦á6Ï¯ný²iýÍÝëÛg7\x001f¾oÿð¡Á=Z<ÙÀ×t&<Âãóó§p¡>2×½Û\x0003ß÷S\x0017ïB×\x0019ýÝÝ7¯Ûÿúáÿ|öêÿûÿÇ¿¯èÂ>íö[\x000cÌY:Ï >75~Mç\x0014~\x0012\x00176uÒ½úrSlÊm)£ÃTÒLL_ûÎéÎEË\x0012\x0000\x0007\x00006çº\9üsím­ËÈòDN\x00039ÖÑÒkÂùùL®q\x0016e_\x001a¯\x000bp\x0019Àó³Æ³;ïØ\x00104ä´±1\x0007ô°1Ò6fò\x0004º ß^\x0013ªR\x0018ú2¶û£À¹¹{åuC\x0003èñ
[d\x001eDuÔ¾Ú £ü¦qa±h\x0004 ÇGla°Uô¼Î>nwÑÏm\x0003¡sß\x001dsæ¨*Íò
t]¬\x0003\x0019Ðn|Æ\x0014"Æ\x000b5zìikÐ\x0014ádi	ç£\x0000y|ÅÔ"<\x000b²×¼úâ\x0010xû\x001btê1Û}E7¾böf\x0010\x0014°½9ùRUÎn&«ï¸Mä\x0017#ûå«f¾WÌ}¢\x001bî«¡\x00077»z>pÙÂÔ¥äg\x000e©ÞÂüQ^¸¡]äíÀ"#\x0014Tçè¶dÛiænS\x0000\x001e/gµc·w\x000f-Il£à`¦äµCkhËyCF{¸cÆ$oLÆqZÃl\x001cOCûÈ\x0005¹ùó\x0006¾!¦æ
\x0012XC¶Õ.ÝÃ\x000bòp\x000f7rq¯LÍ}\x0003Ú/Ø\x0014\x0002ídL*^´ÏÉò¡}û \x0001z|Ã$X\x0001¾aæ\x0006O¬w\x0012\x0017ç¹
\x0012Ç7L²d\x000e\x000e]\x001c=Ñ\x0007õ	ÛXîÌ[¢\x00013qtf«^¹.\x0008Ï\x0001:\x0003tJ}\x00146FBvF]´Yð\x0003òK°#\x00148´CzÁ$*i\x0012\x0016ç\x0000=$¯I-å6äaÃC\x0012ùÐi÷Úd~m\l>SÁGj\x001cÙÜÂzXÌ±f'ÓÎÂM'6UÜ;® dg\x0017ü5\x0000í\x0000:2tÀ©9vJ\x0013W¾\x0000
í?b<!Xð	Û\x001b´jåhÖ6Ì£¾\x0000úÑJíß§ôÊæ\x001dÍ
;¡vï\x0003D/ÒÈ}¿j%zfÁM\x000eÐ z\T\x0011ÝØB[VÒ¡ýN@<\x0008=\x000f3£¡^FfPæûÍ\x000fïoý÷ÞU· ¡ùÔ\x0016+\x001b8«ìGq»§\x001d!./æSäìBLáãÂ1¢\x00072\x0019\x000c7Øo¤¿ô2¦ÅBI@\x001eù¯ì3>½¡\x0006r¸c°ì87³»\x00010d©JÄ¼4tdg¹Ï'\x001fVj¡9ºÊ'F\x001b Ñ\x0013y\x0018m®{J7ò:Ò#ÖÅ¦:$\x0001ª|^åý]]çÐ/È¦í>ô g<²-ê=?f\x0017A²T\x0005³©\x0005s×¹÷%­ü¨ü\x001b\x0019M\x0001Â+Dg\x000etælû\x0016Uh\x001a94uÑX<)?RjÔX¾æ\x000bgÌâ)ÊsMÁ¨6\x0017Í\x0011²ªvAoä ×É\x000bd]\x000f¸®I*Àª¾\x0012W³)\x0000
b\x001bQ ¨\x000f­dn±\x0006p¡Ò\x000c\x00062ð\x000bzb\x00163/\x0000
©b.Yj^¶¡¬«JêúDÊÊ%Ê%\x0013f¬\x0010àÅulL6|ÏîN	Á%\x000bøý\x001c7KD£º%dcÃÆ!Ê!\x0001 ¨!\x0013\x0015Ðµ\x0011\x001a\x000e~\x0014Ýb½
@cßA$\x0007µ\x0019þ\x0014è6W\x001dúêC\x0016C&Iø\x000c\x0017ÛËN\x0018Ë\x00082ßºqÈ¢rÈB6\x001dë<5I]¬Ê\x001bK-£\x000b:(´Mp\x001b9!s£4ød¾°\x0000ìt\x0010\x001c=\x0019|\x0005 ñ¼èºÔçÃÜN
\x001d4\x001aDîX\x0004Ðr\x0004!'WÅ\x001e»Qwj\x0008N¤\x001akëíßÏO­ÜÓN1àvzè\x001ez©2A!\x001e¹öRáV¿¾ÓCðO\x001fK\x001dº]Jûhö\¥Nq³SD\x000fõäjð1Ì²Àzºî-ª\x001b¿7*¿7\6|*NtMòjf×\x0007mýN
=\x000e¢8\x00036ô¬\x0002ô\x001a$nZKiÁø\x0003Ð ÍYÇ0 p{D-Ê*õ-S~§\x001e;ý¹K@Î
n\x0013mg¶½:RLS+á\x001cIÃ!!Þ)àèÌI\x001fºs.ø\x001aú¡ÂzëÆ'l¡<wË%âÞj>Z¸ýN
=tu\x0008ÿ%SJ¥¦àêÔ½÷ÂïÔÐ\x000f5\x0014vZhKÌ{Ã0¨C~\x001f;-ôÐÖ!»±¸ÄèÐN94G%&ìô0@ÏY¤þ\\x0002÷ø§`øÔÕ/Ø\x0000z(¢p¬C:\x0015ËïÚ©mÔ¥Á¾Èv§ah¢
4Ka\x001dO*ùQjïú	;M\x000cÐ©\x0019sÏS{\x001e6©F\x0005\x0016õàÚéb\x0018ºh¹´Þ¾\x0012r·S\x001b¶¦5ua§!ÂÃe±¶.[\x0018µRÀf§\x0001±ùép!Y\x000bkÙÓÇ§îtÆa§\x00011pD$Tèx!í³ñ#`N¶2\x0006PF3vzõSWVÙV×c\x0019ÑN\x0019\x0003öXyêÞ*ZWK©Í0½¢\x0016wº\x0018.ê\x0006/`mF>P)ÄÈM9ÕöZÜéb\x0004]t@Gv86ä#q¿ÈÅ±;]C\x0017_\x001f±\x0018vlBô4BÑNÝÈ¸ÓÅ\x0008ºh¨æ*ÉCzpKPïëe¸ÓÅ8tÑ¤^Bg\x0012\x0018ü S\x001fMq§\x0011z\x001d×9«{ó]\x0002½ÓÅ8t±Ý;ÍMØÌv¯9d<Ûäzù2ît1\x000e]lá5\x000cffïØ\x001fËªkº^;UC\x0015
XæÖñ{\x001b8R>¥¸ÓÃ8ô°ý4Ê*·\x0014fò5\x001fk\x001dÓN\x0011\x0013(b·à\x000b
QÃ\x00102<ßÉ>ÒN\x0011\x00134\x001cËîEpm\x00021å\x000f©¼ØØÒN\x0011Ó(@×0ä\x0012æ*OWmÕP]ìoÚ)bcaÊ\x0005\x0016»Mso}ê\x0012{¶-í\x00141ÚvM\x000eC®öØ\x0001iÖ£¨S÷Ýñ;EL &ã«\x0017²áúYé¡KÚ)a\x001a\x000fÕS¹¨SÈÓCä\x0013§nK;%LC	e.
ßÚD+Ìe\x0002=r¬}N;uI8¹@3´©à^	ñNyðº\x001c=Çy'ÒÙ\x000b\x0019Ï=ÝñõÝí\x001bÐÊr\x001c9óNì2´\x0005`\x0010äÄ\x0012\åC\x001epåld¶t\x000e%Îi¬Ay^>bÞ}Ä\x000c\x001fÑPC\»HN}Ä¬~Ç¦i\x0000å®à!\x0004æª¥4aó\x0010Ô«eºÍ+»¯X,<-¹ëôùÓ\x0012TyZ
[T«ì>cñ`<\x0011Éwòòª¯Ö\x001eÌÝG,c­f
õ;¡\x001eibUcþh\x0019ØEäÖãÄÅ\x0018TÈ
ÉP×À}Ì2ÏÝó5	\x0007S6	çâ¥ÀÞ
%TúT\x001aº\x0008îÿBÎô\x0017¬5ä\x0014f[hÈù½Rû"4[n6ø¶\ICzFËc\x0017ä2¥Ù=Oq\x001dÉ!wà.#x0Ø¸&	qNMª\x001cN¿|?Ñ\x0010a²/¿r·l\£Zµ©\x000bÿW÷¤v§xzÙ_\x0000¥:!½à\x0011Èéü\x0012{Ìîù´I}ÚL}l9ÓºnÏÙ2£Yfÿ\x0007:·\x0017Ø2øéÎú\x001aÇ"Ù-8\x0017ÌQ±S-gÿvóá}\x001f~ÿh\x0003ÒÑ&UêÅkw¤2E>X.Ô\x000brIò?pîÃ:WU7T)aÞe\x0002À>*æì<Çòí«ªÜhìÔ®\x000bsy c/Û v­Íe3Ý4³L-\x0012í\x0005+ö\x0013\x0018Ó¹\x000c\x0016II\x0014\x001bò¶b?ù5u\x0007ñ^\(jÇ¶\x0011\x00145J"	Ó[;ld\x000fC\x0018åWb®W\x000bßöõ~ûêö\x0011©hlQQ×5æÌç\x0012ÂË\x001bû$"¾îZ_¸U"¾>ð½¿u-âVxû¦Øö".4ûýÞ±;ã¼®\x0007Á#°R*I\x001d9ñØeMë¹&C{{)$` +^L%?\x001b©Û]t\x0007iá\x001f\x001dÈ\x0015´\x0011\x000bá2)@ÓÊ%rÜ\x001cµ²ÖJ«´ÒJ³\x0001ÂÏO	ÜåRc÷\x0016\x0017Þó9ÁOgµ´±¡ç\x0004Õp@]\x0010.\x000fhhhOÖs;\x001eZTtU-%ÁûÕÏVÍ\x000c\x00074ÈÐv¤\x0018©Ü"&;¯»3´|¯ülø\x001c»ÂÒMóìQTwbÞó\x0007ø½÷\x0006ÖYTaádÿ_åj8ÆïÁW\x000e×%/xJLDâJ\x0018\x0015æ¥¡­¡ý	8×bç¾Ç÷Õ<7Åp-Æ\x001di§'"­\x001fij«2µÙîMX§Hyy§t;Ö;Q­m~\x0007µÇDy²ö	=#ç¼i¯ÊÖnnùÞ/´¶¶UY[É|\x0014xñ¥ï\x0008KB2Ú±ÝXÛª¬mi÷gö´Ö§Ù«\x0019÷Á|am«²¶%\x001a©\x0015dj\x0005Ìó±$uam«²¶Âô\x0018\x0018Ûùu uyª8+9Ó=B\x0014?1\x0016åiæ]·[Uf¼T éÐ0²Ï<w\x0007¥£§zi©êÂÔæ\x0018¢°¨©\x00108Çj&`¼\x0015Â¹:$(;AnªHqæ2GWò9Ú¡UÇ²Pl<9y¬ô~a}éHÜ}®\x0018k1\x0001¯ûtm¶T®î9åCk$Ûû¦Ëjª\x001f}(qT¨\x000f,Àpâh3Õc5Ó
qª§ÑzIr¹ÔÚu®Õ}º²ÄTTs_¨à\x0011³QtL~3ô­ºim\x0005\x0007¼ø-á9úEÁðäMómõÖ®G¸§7¡7iÿê¿w÷ÍëG"·\x000b9ªAÙ¾vÔ?ÀûÝ+îi(§ÜG\x000e­Ñ\x0016^û ¾¾\x001dr\~¬f±\x001d\x00010±
Ti\x0004ÖZnèÈ1ñÄçj­( cÉ\x0014Mz1ÍEÉ\2%ZÍl\x000eæÅÓ\x0019ÔÓÙâ	|,Êô\x0003*W*Ð,\x0012eÚ\x00172¶d}ú¥¬\x001dçioIÿ\x0003\x0005ÜÕ\x0004¯o¯b\x001c­3UÞ4`ÿå»wÏ~uóûG¨/´PÆ	KR\x0019ßÖÃð]\x000bßÜg¥ÉÓÒøò:EÒ¸<ñ½¿ve´\x0014\x000f×ï?<û\x001fþþîöíûG
S\äV\x0013¡6;'/¡\x001d¬\x0000>\x001d­?½Á
Ñ?¸¿ù¸\x001ce°d©\x000btÖË²\x0011¥pÊ3¦²b=aB³9ü`\x0001|5Ô<-Ó\x0004ìúÀêÂh9%&Q\x0019îXÍ\x0018evêµÑr:ç	]bR¨ öf\x001b¹+ú\x001c×33\x0007,öëÓì®\1w{s´\x0016{ÏÜj²å\x0008ò¡«>$|äå\x001fMÈð¼`,=7\x0011¿ßÞñïì-Ç{ðC6Äd¡o^,%Ú\x0012PòªÊa!ýûÛÛ×ïïnßþ4)àÌÉ/\x0019>:]p'üÞ	ùØ?½­}åÈGÐ[M9àPpKvµR>.«óh\x001c[¸à:Së¤.\x000eÉeijÅ7S¶¢ð£oW^gÏï©âU¿wÏ~ý¶YòGú¨5p\Êþ|<eÝ54ºJ)Ë>ã¹æ_|T¯>ª\x0017r
È6ÅÌáj#\x0013Å¸ùª^çßÅ\x0000	C`\x0006\x001a¾G·\x000e¬¼²äÁflÊ\x0012¢*ÊMVnPHiÞ~Ñ\¬\x0000¹É»ýðöýmsãnýòöÑÚOÍÇ%AÛÌ5TT1½¯êó\x0011pë üe»¡®­P\ùÞß»PT¯Y\x0005¢þöæÃ+á7iîÖcÑª¨»\x0019¹NCÐ\x000cm*O\x0000ÙÜþ\x0008õNosâû~ìtõÿLÏ2÷äU;õgpn#Î]\x0008!ÇÓ¸º\x001f·ãf.QZ(|æPU\x000boåx®$·²'ì"b­ã\x000bi'i´ÅVÂPÉëéC3¿¦_\x001eÍù@Õþ´DÇ©Ó:
7±ÅÑ\x001eKýµgÏ>}\x0003ÑpéOøâ#ßûsÕÍÛ/\x001e\ËôV<VÙfÍ_a¿é|ì«D§äp bCû¤÷¸S¸ãZ&gO=ÕÇø\x0007W3µà_ýâÏß|ûê{d¨¿i>ÛÍÝÛ»|íý¢&¼$Ô;\x0017mçs>®EFÅ-\x0019é=FIúdË\x0001Ø\/¨{C§	©Uf[2\x001d¼\x0014üÑ´²ÿèc'ñÎâ?	­*t\x000b¿ÿ'/äohsûâ?ÿòí\x0013ÏÛù×o^ÿáæ¯\x001fiI\x001eú¼bÅ¨Í ¥z}p5°Ø¶\x0016ixÎî©¾¯,&^y[E]ÿqCÝß:3\x0000íä©'V¯'/\x0005ó¬Yºa¨MA^ý^«{ô3×_d\x0012¨\x0004¸à
ÆöóäÛªV~\x0004\x001fÍü-B\x000b}ªù
\x001e#÷~\x001bBo±Ò$6øîUýæõ\x0017¼·â!±	®rªÃç|å²©Òï[ Ù\x000e¾'\x0011\x001b/sÏ\x000f%C¯÷Ãï_a\x000fi#iýV³óÆÑûïlofU´\x0017\x0008>/ªL4Å\x0000à\x0005×êf_-Óä7S\x001fæj\x0004\x0007sæ²Ãù\x0001ÙÆ
+íkÑ·
Ùùy  ë®\x0016öW\x0004c\x00108p%ä£\x0019,o¡ÇTd\x0013\x0003³àÒe·Ý\x000c\x0000½ª!ö¶j5_ÐcÂ°Ê"5XA&Ø0*dE\x001aüÕÛ_É\x0018ÈªÒ\x001f\x0007Ü\x001a¾Ý	DþíäË-ÏóÔ\x0014¹©\x0006î+ÑÇ\x001c\x0007\x0002Î|\x0001>Õy0°áà.a/¢\x000cx²ðÄ¯¹%j;°óiq«DYPóhÚÚ+Fvk]yÜöäÖáÉ-ºæ^þNÎÓÛ>ô)F«¦\x0011}Ì+WßÎ\x000eWcùè.ªïÙë6l\x001d\x0003ËUöæÂÉÝ²\x00075O.Ûc\x0005}{ëvLÿÖ¾"#kZ±ñ1\x0007ábô0ìo=îGjôÖ<g·Ç*¼9øz÷:jAGe\x00103\x000c\x001du}Mãf\x000c÷6ªß{Üê\x001dÀ
½b¥_örTFç\x0005Í'ì÷®&	Ý
ôb1\x0007Ý\x0002\x0018õU] \x0012;¦ÌlÜs\x001b=\x001dÌ¹|\x0012øì
}*öØV¥uu÷õ··¯Þ|dUîa\x0017 òØNH¡ Ô\x0003[¨,·Ù\x0005ÐRÓëÏÒm÷n	s\x0011W¬d&-kÆ3LÍ
²Òü\x0008 eõÑàLÌ\x0016=Î\x000br\x0000\x0019å$bkoQt`\x0019çYÇc\x0016AÄ\x00138xS\x0003Ï´Î¡\x0001{.È
1óc\x0001äH¢í\x0002<AU]e¥÷Ç²\x0019íbÈ	\x000c-ñ\x000eù\x001aÉ)o;µÛU¦¦!@Îp\x001b4á+qWÊm0íP0e^\x0003È\x0005\x001e\x001eÈAÚL-¿<\\x000b½\x0004ª÷nÁ^ûv$l£Û`\x0012Åp¡Z×û
m
½¸¤9\x0015 \x0013·:E×5Åî\x0014\x0010Ò,
\x001cåNHÌ\x0012?ÜYÚt°Õ\x0016\x000c|ó«2.À\x0012îGv Ø·\x0017RÂ\x0016ZÿÅ\x0003¶î^;ù?&\x0016>$ÓÐÑ\x001cdj®ZQ½Ë3³S\x0017G¸÷£°ïCsÙ´ F\x0006äÌÆ]0á9Ë4oS\x0008åàáÛ	µ­LgµL S ÚN²àvçØíëI´Ân7O_%ÛyTlÞ`Û\x000cR]¨«9·\x0007©¢]nZ¦Ò\x000fuÁ>òÛnUáB\x001co{À\x0011\x0010i\x001bïÙø§yÛ}|°\x0004Ü~Ú\x0006á8Æã\x000fV¼AÍÙg\x0003\x0000\x0019wé\x0008ëð\x0019û¿å*¹ÝR¬Öòy/jÃp 5\x0014ïÂ5[x\x0014Æ\x001d[±f»RÔ\x001e¨L;ûäÌdWô¾-1ZË·²¨}M\x00072Þ\x0006ÍxudÒ£öÂ-Èí\x00074>\x000e\x0006kqìíX5äí:7ØÂ_á¢\x0003\x0011\x000e·°\x0006ù=\x0005×ÉI	jmÁ/ÐpÓVØ\x001c_ ùÌ¦[¬½ ÃM»s\x0007¶E\x0015U¯=¨ÒlÞÜÍx\x001f\x0016ïÃY¢\x0014iØIÝt{.\x0016&«.ªÕÇ\x0012¼GJ^`xÆ±ÉéµM \x0006ë!\x0005»ÕJ?33Uµ
²\x001b\x0002"?é|wô¹¸ém§JÍTÕf*\x0000,ÄíßS	±Ê7é]\x001fS¥j+\x0015lÁ¿\x0012hc¾:\x0004«£\x001e;G!U\x0015î\x001b²A\x000e}'
7ÎÌy\x0019w´4ÏZYµý\x000b²J\x0019âë(rdv~$»´\x000cBªÚ×.fz\x001b=?î³kãµjÃ\x001aÇ\x0005®Ù\x0010OY©ï3s\x0010RÕ"¼~f\x0018nsMP¢ç33°'£\x0000¸Â-Ü²Ì¡ék·ÌVõèÏ_ UíÁ«Â"¶¯É\ád#Ç§-\x0010^%HôÎËr ÇÊ\x0004ñt)`Ì\x0000_SøßüSÙ¦Úûj\x001f6NzKg5MO\x0006Gz{\x0003\x001cR¬J	I\x0015`wiôÎj==Û\x001eÍ¢b\x001cÍé\x001a\x0000yX'#!Ã@6Í=\x0001¾vf5ðÓüÒ:é-Õ¶	Þ\x0017«\x0013Æ3\x000b01-­ÞÒY­É¸¿Õ\x0008ÝYÄ3\x0017î,´ÞÎC"àÌì«62\x0014:3oõv¥¬ÍÞÓÙ¾ AJGº
«Ò­¦\x0013öÍæIïé¬B\x0000\x0003½!\x0012\x0003Rº¡yLt\x001b~µ	+ÙAºÏÉ ¸'¡ãhÒe·Ø0Á>µ\x001fÓ¦NH9És·ì_ûtqá\x0005[í\x0005Ûö/\x0014¬'8öUM`2"	ÜwZ\x0008)\x0012ñ(s SSnÎFEöÎ,¶G\x0001ôPCñNa½@SUËD\x0016v!=±ÓC\x000b¹ÊìÐYñ{*8Pty±
Áw·´¦^=\x0005Þ©û¨ëäË\x0005\x0019s+óïË±
ì\x0014\x0015´P.ómÐSV÷|$vzh¡ÔT¸ÀghÜSÒ\x0018¼f§]NYçu.Ð×É\x001ejÌ©#ëï,w±{ßùÝN\x0011\x001dä*×ï2]t GÁðåÝ±Xz§\x000e³:D\x0007+§¦oèÕ{îÝíÔÐA¦2\x0017Õ\x0010±CïÔÇéÌ}î{§\x000eSJ\x0011âR\x0002M{\x001fú©wjèÀYoÆ\x0014ò«¾¹«\x0019¡ãT¶÷Çê\x001e=\x0008µ³»à©#îÒÜ\x001cÏ{ßÙ]ÜN\x0011\x001døëBKuåÊÏV\x0008IÕ\x000fè&:èn\x0008ÄÙ7Ýµ·ìyøífªÐàX#\x0007U;47N\x0004ÃIòv\x001bD'Ó\x001eÂOo0[á½C24ùÌÐã{ZhêQ9!J\x0014Ö|@\x001f[áÝ%äÞGâwÒ1èùk,ô	ÐûâçdEHý­õ»Oèá\x0013zªË't$x\x0007ZÚ'ìÖ4o´\þÑÑ\x0010Øêú´jiZÞU1Î
Ce¨ýð\x0013Oïo¶^õà\x0013«Bá
\x000fzs\x001cS7Sb\x0007Ç\x001cÛ\x0005ì\x0016Û"vûWFÛdµ´\x0000Qæ\x001a©×#
çÆªúÍTe¯^õÁÔ_¼zóXÉ§&Ãª÷É§aÃ=|4õ<Qò©Sº~Dý[Í©ÕæÿS¹)XÜì a5¯ª\x0012~èu
\M\x0002Ôv$Lå\x0004é÷¦wXß¥Y'Éõ0@Ê&¥Ë~)ÇÙ\x000bÎ4õÏë"¸¢+«2
¹\x0010Ês>2\x0013Ch75p5gÐ\x001fxpJbsJ"½\x000cj\x0002Øy\x0016á53ÊÉR.¬ôýVÍzâ*k'ÆLN44²i\x0002÷.¶\x0013ûu\x0001ÜªàNZ\x0016 M¯i!3ª²Ã:÷t\x0001±Ä\PíÈh]½êºj'v\x001aµ"WkïzÆ¨ \x001aÇEH	]\x0018ÚÚM%Y«uo\x0015ç?îÙÒ\x0012s¡X¤µ,¦µ~ñííî^÷ÔûoÞÜ½ûØ	±È¼ó2\x000cc\x001eî£]ès,»eû$ÌÆÏNÙ­ \x001a/*.7ãÈn·ííhñ»"\x000fã'+\x001cG?´èógÑxzÐjOÝN&êÌ\x0019r`jt)!ãÙ*C¾ à\x0001äa£R\x000c\x001b\x0011\x0013jó9Y\x0010íå\x0014p1A\x001e0jr¶v\x001b·ÌÇÐ'SrE.l°<pj¶?\x0004óØæ6lÛ¨\x0005IÔÅÎRÞ,Wn?í½E³Kââ¬Í%ùöÿëýíÍÇ*ÝGÚ%\x0013ë`\x0008®B±ââDwð\x0017|ÖÉ,º8¹%\x0001¤<UãÕCLt]±&³N;;EUÍe¿àÐ®ÔÈí+Çí}ñ¯\x001a\x0019¿øáÿ}\x000c~u÷ÍëÛ¥l|èó6§ÃFçÌÙ!bè\x00079I±ÃOcxÿ8¯3hÃk\x000b´_SnÐplSZ~ß 
¯i\x000fh\x0014ý-aÜ¥\x001a+\x0014\x000e¥×\x0019tYAæb\x0004äDm\x000e¾ª%íÂ#»ô:6é&\x001b\x000cgmñT{o2©Rô¶o ÝÎ Mº CÒQ¶¸9:³çÜ ³½\x00142ûa*+xGUO£úPÛ\x0007TÝDfæk\x0003äáxÓ'6UäÄnGVü\x0016îh@ýÃ sÿ}â\x000fì¥Ã[!/Øw\x000748\x0012¾ÂM\x0012Ò-~eFH×<¹96¾^\x0007ÆÆÉc\x000b»X:7w¹¶oÑ+e«¬ÁUª)k`JÆ¾y+«Ê\x001cÙ\x001fUÁ>5ØEh½\x0019
í
®R°í+`¯¤/UÉ x\x0010ì/e0býooþôçwby\x001f}>R¬(¨·k_~M±B,t~é\x0012-/~æçtÊ¿l·%îÌÈ\x0017\x001b^ë¹%Í\x0017ñ7\x0007Ã¿9£ÍÖè<ÀÇG.ízÆú\x0002\x001f\x0012ºM\x0013¾N\x0014ÈâùE\x0018óáÙïn^=ûòöíû»×ä/ÕôöÅ®-¦¾æãZ\x001edû<îH=yÿè úª+\x00028(ÿ·?ýùæÝ»£uëÒ\x001dñîÙïÄ¡y$ýò÷²ÆREö\x000eAª¥\x000cÂ\x000b¡aíqÓÓ¸3\x001fÃ\x000btÜrgÁ)ÒT.Ó\x001fã\x0007Ò\x001fkH.Àß¶Ô\x001aÀö§"ë¹\x0008Ù%F>	\x0017ÙyExÙ.\x001a÷pÈúÉ \x001aÈâÈ(#Ïë.ÀîLi^5ºØYøóñ1Ì<B\x0016\x000f3+\x001d G¸\x001e\x0006\\x000cMx·Ë\x001cT{³j\x0001Ê\ø·7w¯ßÿÓ»ùú/\x001f\x001e-Wâ\x0003\x000f\x0000ø$\x000eÀ5OEËÔ¥.â?óý,Y\x0007N>\x001bÊdÃs\x001aÍCWóAvíþ^!é2\x0012Ðú¤¦x¼.\x001f8;©\x0017äá¤úMJ}yð\x001dë\x0016Î,^¥æD¡É.ÿõÃ\x000f¬´ç¹ÁàÇX}ðþ9,ú\x000bBøúT5\x001d\x001bÃ|íSZÍ[\{(ë®h´ý*N%\x0005¿n¼ÏsG+­´a¡Ì-­\jÀëè.O-­âd[ºiN%e«k_iY
_,\x0012\x0003¿}óáñz\x000c}ä0¥Ä\x000f%M8y,\x0005z^àðf\x0003²}p%ÔqGJ^dÖ\x0010¾ªyéÀ¿X
Ûm²=&h£Uy¨1\x0012\x000b£äT_Eê\x0003¼½z>Ñ*¸­P$±PI p6 Éüúù4AÃöäg6<U¯J¸9-ó»\x0013\x0011u·³Ð\x0010\x001cGÖbÇu¡&¢®Â;½MRì¢\x000e\x000fÚøÒE\x0011*è"TSCxtBRIXOYtá\x0001[× ®AIÄ\x000b= E7\x0013gNvK\x0008¼\x0019ìÐ8*)Leðùdr+}<È\x001dL*yÆ\x0003\x001a¤¹xÜ Ú[BÈú%æàzyrÑQw\x0006¡[\x001b{Îfêð\x0006á\x00084´\x0012ù÷Î«f\x0003z÷\x0019¡?MÚ`P¢sU\x0013¯E\x0019\x000eÙ\x00148¥\x0016,fs5§7\x001fýÇ·ýÓãlËÇ²\x0006ëò\x0013ú^±\x000b2%É\x001c=3¸ãÓÒ\x0011¿
ª¹3\x000b¹¥\x001f®¸@\x0012m5Ô\x001aóAWj§F\x0001=	²&\x001a\x0016AP>Ô\x0016ÎÇ\Ý*¨Mì¶õn¸øýæÕÝ»G{-÷ô­qWÑO¸±ïèz²ÚKécª¢íôs\x001crß·y>@\x000eÄÈ\x000fVæ±en6`I»oÍ¿Æ´¿oRÃï&\x0002Ø\x000c$%í½5\x0012h2åÉd;P£ æJ\x0000±	7FE#=|ä´ Ò¢
x\x0019æ}ûÃÿóhì\x001cN=àÕ¡k>\x0019W\x0014ªS\x000c?H"é2 lRæÕ nÔ¼êÕcZêºNt8+-äð(µW&Ø¤ÄÂWYçE"\x0000¼\JUG¶U}$M(ÚaÇåX
#vëõ7í+=\x0016Ë£SÍl¹\É\¼ôqbI ´|º4÷:\x0013º\x0010\x0017&sÙúÞ_¼ÈB;x8F6ô'\x0008ä\x0014ÓGoÔ\x001fþXAÇ7=Ù°ØÇj«\x0014\x0000t\x001cg©{.Z.ÚkæØ;Í'º\x0002yÏ\x0005ª\x000bë^Ù½lCñW`\x0008a²Ì\x001d¹í%á|B.+óîæ\x0004Q/O=ûòÍ·/ß<VÙ¢É¯\x001a/;7$Ô([® \x0002ù¤öýc]Ibb¤îSÂ'
\x000e~¶ó¢\À<Q$~\x0016i\x000câ9Tµ\x0001Í\x001ds<³Cà´C\x0010#\x000f÷\x0017Ã	±ê	×îÃ¹TzR©ó\x0007¬ôfê`Iµ3Iè".èK8óÕ³\x0016²ÿgËi·Jeb\x001c\x001b²Ûhc¸´¼´ÃrdÝ°Ìòþ½þÉ«ÈújH»ï¶+hm½Nèøã \x0017Å?Øå\x0004½£?Mí/[ê¿5\x001dô¥
$«MüSÑ7|t«UËlE\x0003Êg)þe*wYU:\x0016.N\x0017ÿ¤é:Â}\x0014î8Ê¦ª»\|ß/\x000f¦Ña\x000fþåöÝ»\x000fï®uõGMt¸ úò5gçD/.wrR½\x000bÙ¥L:Éô²Ý|4x¥7ç¾÷7¯¾\x0002,©ûêæØÒú{÷§öã\x001eÉ©8`¢3.]Ýc\x0019Ð\x001b9ë$­rùÉôkó\x0005¦\x0001×ö\x0005dg=\x0007\·ç¾÷7/¾@G\x000e¢ÈÀUÃ\x0015y?ÈÕkÊ@Jóc¬K~ó\x0001¦g¦]®º¯O}ï/^\ñ¤\x0000ýäÍ;yóX[\x000b¤ÃÉTFa¬f\x001aFj?éÉÚd7îqvErõ\x0015ý¡úoÉ\\x0019\x0013\x000e3Î\x001cSãfJá\x001eØ*O}Õ©É¡8ö©öØb=ùS\x0017lb^¤ÕÛí_UãÝyÂî­Ó¬ô\x0015\x001bf¥m\x001e8\x000c\x0010\x0005KíÂ1ÃÅåUÊßR7á³_¿mÿ}óöæ÷w6,\x0013¼bm\x001aL0Âù	7/Ì\x0008O\x0017«íz\x0008gÓ\x001em~@¡$;aºTö\x001dÓätT¿Ù×õwÓ+{ÅQ\x000eO\x001b\x001e±=cKjvþ®ÇÇº®l:Øfà¿zóú\x000f2\x000eus÷h\x001d>2þÄ%tæý£DßÃeÈÆ=aQgóÐæ©I´ýpù\x0008yÔ.7ç¾÷7¯>?dÏþãÃÝ«ÛGÛR\x0013Ä¬ài1gãL{¥ºü\~IlÅgÿ\x0002sHçú8 \x0005þÍ¹ïýÍ«/àÈ¼\x001d\x000c|Ï~óæÃc-\x0003&Ñ¬zt.â_ÝA¦xõ×êAfôY/",hìK
AësßûÕåqÀýJª?½üáï_¿ù v%ËÅ{¿ÚIuUPKsc®#\x000c\x0012\x0014­rQúÁJÆàzm\x001d÷RÅÓëòí¥²!¨ÅTæÅìüGtóý±]Àkù\x0013áõ~%yæ~ÉkÞ¥Å¦\x0016nÙ«áµ9ÖÁS[dyuÔ~üâG\x0017=·$¡gÁ»^\x0012e¸åàåÌ÷ËÁSè»PÇvXòn?Ú-ö\x0012v<±¥-ÂRZ¸M4íÊ2rÇYÒ	;sK\x00027s\x001dQu*Ûô:ÚÑàç\x000eÛ\x001ezû¥XARM|)S{yñáûã\x001f9#º^ôòXM S¸`.\x0011·-Æå3[ÜWTùîº><Úº$Ðòx\\x0010Ëc\x0011Ö¸!2=\x000enI>«÷vÁ°ØvÈ£°{$7>k¥Yìm^ôYC?ë¥\x000fhª©yÓ>î_½º}öËvQ_?Ê7NFØé\x001b§zµ9¥'òøÆ¾vM~"ã{¸sÚò¸-J[¶cû1-Çþ\x0000Ø¿h\x001d;J«Ý<û\x000eÈn Á`ßÞá#Õ.3²¾ø8\x0013;\x0002°\x0007àHG\x0016z¥LÀ¡²&\x001eµ\x001dòiiJðé\x001c7wÕEF\x000e\x0014\x000b7L3ï\x0007\x0000²^|g\x0003£\x0000ËwÀÖ\x0019Â­Ó\x000evu ê¼Éo><ýZû\x000c÷ú\x001bO#ÛÞôý+\x000fË¶S²³	'_Gw\x0003(Pñ\x001bÏ\x000f\x001b\x0000Ø\x0017)\x000fZ2\x0001­`ë<]¥)vî\x001a\x0001àñþgát\x001c÷,l\x001a\x001ecá7æ¿Y°\x0012ì%W¶Ö#ud\x0003N\x0016ÚY²ìÜì\x001ej¹¹\x0013Yxª	ùX·vÈi QÖêa·_fý\x001d#§Åh1 \x000fo¥±Ü²kcå37¹¡çè­;àúÅñËç~â\x0001.s©<@{ÚÒn6É=\x001f«FvjbÇ\x0013`Gh\x0019\x0011-(\x001cÕ\x0018¶Ô¥süØ¢Ø¡(R\x0005sa:No\x000b7íøA5}\x0013´Ý©\x001d¯\x0011¦`xoee³ÃS+Ás¥.xE\x0001:ÀgôW\x0006.\x001e\x0019»Âå+²à9{Ðüì´eø<\x0005i'äÐ)bï};tbù¨ÖÜîdú,ØîSÒ;\x001eøµ5täö/«\x0001¸\x000c7-³\x001aÛ_[3í-`1X÷×¶»öv§.'ù§íCÔ%\x000eèâ1=ÜÎLK]b¸¬°s;uqC]j\x0019
}.æ2Ú©\x0003{®²!k&é\x0004èá×´_p6#
t°8"Ô iø¨A÷ÅMn'Ò\x000e\x001c\x001b\x0013;ð¶G³¹b!±·íúÈÛI´\x001bLÛ\x0017»r4'®\x001cL{SÊLÑ	ÐñÇ\x001eÚiZ\x0002¼k %h÷]òIÚuÆ 4Q\x001eªÐ\x0000îÿ±ø\x0007ú\x0002¤àÇã(c+(áÑ:~\x001c\x000fú gîù	
çÖà.2\x0006ÛÈ\x0014õ.d¯+øF¸\x000f0'¥³7Òø«»wsoÙ'zío \âõdZÆB\x001cnWô¢Ø¼d÷lÁËö\x000b-ØûÞß¼ð¾=ïT¼°JþÛÍ÷Ï¸ó±\x001cñZÉû¥§Y\x000b	}"'ûÙ?Á¤\x0003÷ n}ïO^Èbùïyì~þGJâ$\x0013%[\x0012c<cÃæóaöC³¨æÉr«×^ôËvEìEï}ß/æïîí¹ì¦
Øíiì°Hc_Ýeq,)?\x001b×Ä7¦\x001díÝ,Èj`¬_æ4vIÆ¾â\x001fÌ`§\x001aù\x0007¿à\x0005F÷Úa!eí\x0007Þ+e.Ëbú]ÁùóN¤Ú\x0000wR\x0001+\x0014³þ+\x001f=Ê\x0016À\x0007¢ìËÍ`-'nïå¹Á#{&\x001cþXSÞ¦}ô<í-B`7\x000bPïIy<¡è6d¢2BäYuÈ\x001eaPµ!çN\x0019ãì|°\x001dr\x0000äÊÈ\x0001V9sRÈ~"½@ä\x0008ÈvÐ.géôî9d83¦K\x001b²±\x0013w,"§\íàÍÒmì`rf\\x000eÞÄµöý¼CÎtæg¶¸V·Ùóû\x0017,;ä\x0002göçÜlÖN¸,K4Ìð³u:G`°IMá'dÃ×<Eð|à÷}¯U"x\x0006\x0015,q¬ïUà	ûçå\x000bbÙ¨AG?/OEhG§.\x0005NmÐ9SG>µ/óöT\x001eZhZt\u\x0011Zt»ÝÖ&4'¹N\x0011<B\x000f5´Æ6\x0012Ù^^±=¿A\x0007\x001c1l§vfcFè¡-=ÏèhÜ`àS9Gè¡.²IÇÃ©[H_èB)¿A§ÞBlwúb¾H^ßS·§µ×^Nhaê#h7oð@ä¡06Ñ\x0017ÛsEïÚI\x0012/¤G;±v\x0016 Ë\x0018ûõr\x0005Wx4h\x001bÉ?F÷)ÔFh½42uý>Ru\x001dÐ\x000ey\x001bä>Å#;Cí"\5Lþ	´AjQÙ&Ë\x001fÑ\x001dájPÑ$	ö&»påE"Û\x0005Ë¡]¶ÙBÙê´K÷bÁfsþúÍ«Çòsb¬ü}Òe&ZìJ°c¸[dÝ<ã|)\x000f\x0012.£\x001c\x000fûÖå¸\x0019é\x001cä§Zþª9L\6\x000c\x0006V¡+ \x0017¶'1\x0005<íGdðr\x0002\x0010¡7A-\x00132yf¡D¿\x001ag9¹·m÷\x0013ÅçDb[l½ü \x0003\x0010	Wû]z
õ§\x0011ÎPö\x0011.qÔÒRÜ ²jßÔg¤A\x0014'"ò{lÌ4\x000bÈ§´\x0004IMÃsÜn
\x0013yN¸\x0005Xå¬+\x0011ù N0ø¹(\x001f"h»\x0015çâ\x0013"qææÇ\x00070z:åÌ_G\x001cÙ#n~¨\x0019mY\x001aCXsÚµòKÂD\x0018Èi8Y:qs\x0002+"{õðQ^{Ä=â .0¾	WG¹N\x000bÃ/Z8Ð\x0011¸#7\x0003\x0015áó5\x0007(á%Kñ\z«Æâì\x0011^-#ÛÒ{ÑÇe\x0010Ç]¿¹ò\x0004ÐÃo
BÝàòm_.svâÅûËW¯Þ¼¿»mÖá±âv\x001bX B°Cå}oÕ:Ý '1P.¦Õ.7¤-Tµc)È!QâõØÚ.\x0004q¶#azud¿:Ú\x0011£B3ãÙBMÌ\x0007Û\x000cä\x0017zú×ñ¨Oý	7u´À3/)aÉÉõ¥ß¥Ó ÿô\x001f³¹D\x000fñ\x001d\®F}ÌÍïýµ\x000b5v¥F¿øöæÏò\x001féæ\x0003®\x0011kG±\x0017Î×þ\x0002Uðkk,OõÊôQJ\x0014­V"ëÑTµ9XÎùª®Në<ù":\x0010pô\x0018'\x000e×dzd©Ñêg¾fTüæ\x000f#\x0015D+*2î~ìüÊG«^ù*L ë\x0011~/GGÆ2|ù°\x000eá_ÊÅ}\x0012µ|å£åW>¶@ÿ¡Ökúä*­]òiâ«CdÈ{eØ¿Ö\x0014RÖlSÒv¹7äØ÷ô¹­d\Ù\x0001.nOøOV=!x\x00133:ß\x0003î´\x0005O\x0003<\x001a\x0007+ÝS ªÄhs7\x0017¤L\x000fò»g¿¼y{÷úöýûyòæ\x0013-I¶/ËùL¢Kâ\x0000òIdþ),IèËÇ\x001f¶$E?Ç+!,ä·fí\x0008­-IÑá¥M°«T\¬ÈÞ[v/±®
IÑï¼eXC\x000cS¡µâQTþ<É­ã¢sè6Ö±\x0007C¹ Ð¾;ûI\x000fZ\x001fáð"nÝr¾}jcRµQÇ\x0011û\x0007JêEcY?¡\x0018·ÎC¨È²ÙÍ/CIÓx1\x0015FvGsÒ*!v=6%Ädù
b­é\À°ü\x0007ÂB`,n¸xÇÀÔcÙ+¯ÞlëêÐÒò\x001cn(\x001eÝ:?\x001bi±¾hÕâØsúöHB\x001aÌ/\û±Çú±\x0006²\x0004ïÿ\x0001$«\x0007rÈ\x001c?dÞ<Ö³\x0008Àß¶Ð/þ\x0006àìBåW\x0018\x000b\x001av\x0015³U¿p\x0007FçöëÛG\x000b9½*TÎàYæy@hì±Zò§\x0017XÍCû\x0011.w¤Mqh\x0013G\x0006Xñ·2ß¼IËGÎêJq¾Û\x000cÈ¶rmÔ§\x0014Õ-æí²ºR,å=¬\x0013`°#[¼Ú¤2y½6:½rVW%\x001bu6fô3ûçú Q\x00139²[¦¬.ºö¤s\ñ6qºMÈ\x0012\x0017\x0001øÂûõíû»÷²tçÍã¹qZ\x000fO.ôM`äQÏº¦·Ò\þ$!áÇÚÅ¨EÜ%éo'¾¸Óã×rÎ]|eæ÷<\x001c9o,T Ú]¨ülµTwl÷ß+òxeYLÀ[.\Û(Õ)ä²z?×\x0002©\x0010ôíLw¯^ÝÝ.¦??Mj¤/óSé4Í-ÃJ¾$s>	\x001c]/ØøÞ_»Jàl	+\x001f;ãTdì=-f°ØÑ\x001e©ð$±×Ç:¾ZeûÁé\x000bq"ÿXyý4%ÀÄ	\x0014¨×¬<
ió%`·©ìiý¤#Ï
» «üêæ»7wo\x001f+ÉZ'Õ}k«\x0003JI)ÇÖº)B_\x001eøÞß:]ùÆüå··ïE?ywûêq®¼@"¶pÿZqOÍ¥À\x0007DZ@êgÌk{ù{ÙnG.Ý¿Ýïý¹«È\x000e\x0004ý×¯n¾¾ZÅ_ÝÜ-hH>UÚê\x0000¨e$\x0003Z0
õD©Õôs\x0012w?7u.O|ï¯U7¿x°o¸ýºïîô³$÷-l$sçð¹\x0010äöºº,EÒ©¦Ìí1ÀÝÍá\x00116\x000e[sJ|°w¸´ûã_ýâo/ó»ôý\x0017\x001fÁ4°ä\i¿ò\x0001vEo0ñÙ~\¾2
¸bj\x0019¤U(¤?õñ\x0019¥²öâ¼\x001d|ÏäÔ²ù§ÏÙB#äÿu.«_|4z\x0005³\x0005\x000f°òÒ\x0011'(Ù!d\x0003wÞ£\x0011)ÒØWô¤=ø¹Õ¤8\x0003»X¬a\x00164·\x0017\x001dKo65éÙ
»\x0005RTz/O"\x0012\x00115\x0013ïÀSoëLû;OãÎ­5Ýi¸JÌ$Ñµ8Cà"u\x0002¾¿4®Å:K×"\x000cµî\}Ð4U$~ÐÕ9%wóööëoo^=ûêöëW·o'fOÔ©öT6\x0018×¹'ù\x000cqÐÉ\x001fÆ\x001fÎL§¼\x000bé!ZËE¡ýîl\x000bqì)É¹H{Ì·Íµ²¦orj\x0001xÑJë<\x0018\x0018þÃW®©\x0004M\x0016Q"0Ú1#'ò(û®,Ù\x0000OjêÁ2-<¨e¾ûìljÈÅÒæaçh_>ì:U&\x00019\x0002r\x001e÷ì\x000c¶bf^ÄÑªt"
­A'p\x0002à4ºÐå2Ês»ÇõÞ¸)7\x0004¸\x0019,
(e\x000bÍ p(:\x0019vÜhææ#\x0005nÜäè\x001e\x0002\x0015Â\x001brL¤î~\x001e¨GàúÅ\x0003ªw¯ÚÎíø\x0003z,è:ÎLGöÌ'vqnj\x0002`P½àG2²\x0008\x001d	í±t^	éõj»Ó= '·Ö\x000fV8y&©µFL¶'äf>¦¹tD\x001el³C\x0015\x0011®\x001cQÏXZôË\x00034<\x0005&½_²²÷~7K\x0014H¯ÛÍÛ¹_\x001e Á\x000b´N\x001d\x0013¦}å>@7\x0005æÇ\x0001\x001a÷dû=¿!5ù7äP\x0008ÙÖ#U½û\x000e>¢Pqøñ¨W×ûöÆU[\x001c]iÐyõ0ª\Û¿Þ¼{ÿæµÌ¡þå±\x001eÄè³s
U:	íH\x0018JF³¨pæ§s2ÛG~°Â~\z\x0010Å¢Vx\x0010/E\x001efJôAÓ²\x000bïa¶£7¹\x0008\x001f){:ã±×\x001d§÷P-\x0010*R5\x0005½iî\x0018¿àNyáØµPvêíÜ!æù¸	\x001f\x0000:[É¦t}@`­.\x001eÆ·oî¾¿ÖÚÿýí\x001e+æ	Þ&¶mõôÏl
ÏÁ*f£ãþtîY3¸\x000fæ\x001c»Òî·£[Ü3*+5û\x0012-\x0019\x0001ã´ê\x0014Ñ¼¤ÎÞr}×|F\x0006ÁvÎ@®½3Å¹u\x001c8;:p|`~/sß9{gsK\x000e\GM"Ö\x00141r`ÖÌ\x0016íN¤[\x001cÉÇáï8©
f:sPw¼tÎ,\x0013\x0013íäí^Q]zgy$«á;%ãé[«`Ò\x0017Ã'N½\x0005cáíX¦\x000f)5Xó.¡¤c·=Dö®/dJ\x000b¯Ä2ÇO¥{a@7÷\x0002É3?h®H\x0017neº\x001c¹iX\x0014(N§ÅÝN¶sÚÛ¢\x0016nÉ\x0005\x001a\x0002÷ö/äqhg±H]$Â\x001c+b\x0019×^e&\x001e9tFÿO¶L\x000f¼çpÃåîØÙ\x001d¶L#Ù\x0006\x0002"³ªº\x0005Äï=Wnwj7NÝ^À®w×\x000biÏ%DKnN[w¥vvpèzÿì+D7èÊ÷Ñ¢¨¾îqgFý0£Í\x0016\x000eÎ\x0006m-ö,µ¯È±¨éèwænP\x0000\x000bQÂ\x0018L(Q\x0006jqGró+3=¾¦\x001cÍP;öC¦]µ¨¥\x001aìÍ¼®g£z«Âî\x0013úñ	½xí#]$íÈn£°a2±\x000fjä­e\x001a;©´û\x0005°¥Ö\x0019º&ÓÊ4-ÝÖüÎçüëÌªð.B4`|9Ó¢M\x0012Æ
v5³öOä±Ö\x0007¢]îFù\x0008Â}APZFv5z¾r\x0013ç¥\x000c\x0016[ftË@\x000e#³\x0007hRÛe\x0000\x0019ôÆÃZ´Ü\x000242«\x0013-Ô¶¡#p\x0000#Çð|\x0003nß³@«]\x001brðÓÒrDNlø@Õ@MHe¢n\x0016mÅ\x000eÔ[edþèÑòßçÞ53ÒÄ\x0006"ìöà¸'\x0012nÙ=ö1Âí½\x0012nÉOÖBg&+(Toü{rrÁ\_cÁ¤H2m\x0019)Î6øºNÉ]!%¡?¶\x0008g+\x0011dÅ\x0008!Û}³g\x0017dÈ\x0002J#»*?Y8lþg]ûf\x00074fÎ\x0005Li\x000cW9­ü¼)\x001eÁmo^_\x0004h\x0019Õ§\x0016Ãp¤¹v7\x0019#\x000fY°\x001c\x000eøhX\x0011e9\x0010\x0000\x0017³î¹Dö\x001c¿¼í%®+E×SRÒ&Üÿö#ww}D}/9òj]:\x0017ZtBî\x0002ÁdìÓèz»ù
v½Õº\x001eò\x0018<Aä\x0010ûTøâÓbf\x00191*-\x0018á	ùgaaÛ-;âW©yËòí³_¼º¹{ûÝÍï\x001f+á¸ä\x0015"d0$\x001b\x0005)\x0019!F©?/\x000bn'\x000bn#\x0015B¦\x0015%Î{\x0018Â1ã¾p¾ýôU=¾gM\x001chñ¼ÄíäÇ\x0006\x001b×	\x0001Þ ñµ\x0003*O/u	Ç:ØëÍû\x000frpÊ\x00074Y%u
?\x000e-ÜNÈÝ«È}#\x001b÷ÊÕ&r×¯CdÌûà¦@ÂÉÂÐå\x0008\x0017Y\x001dý<8;Æ_\x001a²ì­¦ûHtÑq\x001f·ëÇÁùá5È67JË\x001fóWëÝ*uiÖ£AÿüòííUÿÛ§j¼áÓZÆGmA ¼¶óÁ?¾KgÚ\x0003\x001c;ÒÅzÔÎIàll´çIY[q£3ÝVØÔ\x0007°18¡&×¨ÂÖÖÎ !â\x000e\ 7ßo¹ê¨?ÐÊµ×ðÇÇ¯n>zòÃ¢bsåÒ]²ît[Lâ^
ÓMÍS\x0008K{¹\x0017Ã,,Üúº?ó½¿wuó«Ä²Ñcî\x001aû\x0011îVf÷ÚøÆv=àÔ\x0000ÂSßýü0G½xsæ{ït÷¼.Xö"\x001eõ_¶\x001fÕÄÿîÞÆRÑI6¸ë*ûÜ|ÿç§­\x000fÅ?]Êfíéz-÷%Á\x0007-óõÌP6\x0016~\x0010KùösK¯¿8\x001bÐ#\x0005×ÀÁN¶óAí³Sd\x0014­×KDúwµ\x0011uêæO\x0008æ¿Ý¼ýýc\x0019³æø%\x0012°Ú»N\x000eáFRpÁÚÿ¥[èÏhÌ´\x000bö²Ýj\x0006Ø\x001cúÞ\x001f¼¸yµïË¾}ûË7\x001f$QôX/¯ì\x000eúGøÿ¬/^Nù¯£öÆ\x001cìÝ#jß\x001cúÞ\x001f¼¸|\x000cÛ¿ú	ëÔEåÃu
c6LJòóÏÚ5¡]³\x0000;Á*%iÿÀMy>'ò üQuúºB;Ho·o \x0003(Á\x0007W8Êk»3\x0010Íúz@{(vL~_\x0008P\x000bD7.9¤cõÔîÔPqòB\x0001Ð¦ª¤|É]J§MAùâÁ¾øon^ÿð+ \x0002hÚç®"<ëcAºµ\x0019W"ÀaýØEBu[üéÝÐ1þÁ®xa+çßüâO_ßüõö{ÒÁ>\x0000£õÎ.§/Ê\x0003ÄíÎXHkjhNGÂ´rn%PÎ*b¡ëï||«çËYÈsèr½.igð²;õ½¿XKÚøß¿
·ôì´7ÿõ#]{Ì×ÐJ¿æE\x0016SEÓQSÈþ¹KOrëB)öPÔr½\x001a[Ú¡Ê\x0003GíÐRí÷"õHû½Çf(¿ö?\x0012:Õ-v\x001a{§¬À\x000b\x0003»!\x0004X+ÔtEìfn'Iùó\x001f¾ýÛwpë2õýN£OÓ»¦­&zl	qÑp*¸ç,HÕd¸ø³i«U\x001fà¸(¹¶¾÷\x0007Oào¯Þü¥®RÑ¿»ùðõ·s°\x001a¡þTÝõJyó@©\x000b«9[jÒè?£îêopÜ\x0014vf\x000f\x00063Åæ_\x0000Í(\x0018®ñi¿·\x0005S½°Á.\x0008+ïxYcöØi,wÝ²ÂqðßÜsð3²ë\x0001ÃhÚûvñ\x0016ø¢>Õ×
\x000b\x0001F¯A¿½{ÝÝÉ»ýD½
¦ÒÏôÙ_÷Vi
>ûk&Óø$z+>è4½Çõ(­õ©\x000e²³²«ÏQiKT\x001fµ¦yò\x001bÝ\x0000ör\x0002§|´\x0018\x000cdìÁlÀa*\x0005àó\x0011\x0011f$ÐË\x0016ê\x00003V2)1n:æÁ´»qâqàö8Õ!)"ýX2¹8~B{0\x00018\x0003;#%È)dºcYu?Õã\x00019
ä<6@´'/\x001a¤mG¶YjoÞ±Ñ2ïó°åH±,û+\x0013Vdê¢-OÇ·²C.ãÈ-\x0010©ã}5¼+­ý\x001féSõ3G/ ×qæ&pn ËÝ@aD:½,Ù¾fú\x0016s2\x0003z,¬Nê\x0002|Aß;ãÆ¡½ãëvÑ\x0000ÐCMdY\x001dßÐ{%kÐãæØ¸y·\x0004@\x000fEéë\x0010\x0007´l®.¨*í!ñh/rK[\x0000\x001dà­w£1_î:b~UÞúBÞV¬nnw\x0005ä¡,2¼\x001bÆUÛZ°w;\x0019j:lÀÇî\x0018»S\x0016;ÅÊ&ãqäH¬íÈÏÝ¢Û\x0015¶Èö
1g"îµvæPé6BQç~
\x001eêbmÁ\x0017E´¶1KÕN½¤;}\x0019'wÕ½\x000fÝ<94 Ç¶¹*d¼\x0005Ní\x000b6×¥¾äN}ÔkÝN_ÆæÉÚwo7}Áð^Öº0rOk¸ºÍU¦²ÆK\x0018k
è;É}\x0014¾\x000fÛ-Û©\x0003u1\x0011ã@D%u	ÔÝÔN\x001dz³¡Ûé\x0003}\x0015°rêf
BûÊ\x001e®k\x0017$Ð;q	T1Ñ©­Ãþ4QÅPØ~\x001cýÐ;q 1°ÉW¸ÒwQ\x000e}´C»Â¸¡0²n	<`[¨EMÖ{¶L¶w!¸Â8P\x0018Ù%1\x0004¤xK'\x000e¤í\x0005-sªnàzÐG±ªÊùsz·¨­XÆHó¢7\x001c-Ø£p\x0014\x0019TNth\x000e\x0007ìºô;=ô\x000elÅC·SÝ³¯g«eÑx\x000eÐïy\x0008Gæ\x0005ÁýÔô	­ïÓSJé\x001e(ã¢f\x0018¦¾æ\x0019\x000fÍ7\x001d\x000e¾9¿SC\x000fj(Í/ã¦,«léui^\¿\x001azPÃæÖUh:\x001fÜ¶GH=¦ó;eñ ,Òª\x000c\x001f±ÙVºèÂ¾X8ÈÃN¦\x0001d3:üÛãBv|æcí|Ø	^\x0000Á\x000bvltg+ô\x001aHG¢·EB#ÞIG\x0008¤.nÜ´®èJÐCò©?[a÷\x0011C"pjÙ¦QØàñãúF¤°û¡-\x001dÎ©¬*Ç«¼[/Ä\x001f¤ã»»p×MÖÇ%à^. S_vuÇÝ]Ç@ñlD­R\x0003Çn1¹\x0010V\x0018\x0017º\x000b\x0019ww\x001d\x0013CSRÙ[oÐ¡ûàrÜÝuÄ»6c\x001b@{ÖÅ\x0016Î(èÞv\x0017\x0002é¢×¥\x0005\x0014úÂjnKZp\x00004\\x0004\x0015ã®eI\x000c=ä¾\x0018N®7ï.$¡\x0005ÉÏý°{}ÑeE'	±®\x000f	å	É>ã°{ò
"¡@³6¶ÈA+óN®3Ú4Fµ®6z:µ9\ß¼û\x0019>£,e\x001cì%§:TôdËNÌ&zF{{´?É[Ód=° IÜ²b¶ÌdÙ\x001aeáÓ\x0018\x0014KîÔ\x0008ýOaM%/(ÁfÁ1I%µ¤§Ë\x000c¸³ªà\x0004\x000eôV³=\x0000\x000cbcÜ\x0018Gª©¿D¤ýÁó=Ê\x0016 Uè\x000cÊo<55LÈ¤üÂ¶¼Lå\\x000b#ÃÃÓ"jGf%¨ç2?:ëþ\x0001
	O:´ò/MT\x0003IRÉùÅÍë×VÄñÊN8SPºÇå$lÌ|\x0002ánqÉ
Í¤´Ë{uâû~ë"a{â¢?_Çàa\x0003ÎL¢§ÙW'\x0019UÆö\x0004>¦ÔË¾\x000bpLsÈ´e>.»EÊöD\x0003¹\x001a\x000c-\x001cÝxËfMÿzFÿ5\x000e\x0002ð*é\x001a®ùÊq9f{V+rÁ\x00073q¤\x0006Ýü\x001eËqá/ú>ÏàtfzÔgªÁ©\x001b9xÁFâþ\x001cóx£éÌú\x0016X%¿jr-\x001c ¯\x001e¹*\x001fb"\x000b!8¯¥¦"¯QjjÁG\x001fV\x0002ÝôXÿáÇ\x0006U|\x0013Æ¾á±¤\x0010"Fòâwq.7yY7\x0000\x0001Ü"\x0011Èäú±\x0005©Ý£)|.®Ênç¿ß~øîÑ|\x0008Êö:Æa\x0001\x001c|É\x0018e\x0016þgT'8xv'¾ï·®\x0008ºñww+
sÏ~3\x000fò}g\x0015ö>[eîÃÆ$kêSu´Ä\x001eì\x0005?îo¼»V\x0011Nl°çD\HvK¨)Ö\x0015Nnð¿<\x0012Ã\x0019¤7Û[W\x0013ßcÝ8
¿
ÙC©Bè`\x000cZUn
Á¬ÝLkôù7Ç­Ü*eÃ{\x0007ïÝ£5Æ\x0018O¿Î%çÏà§\x0005nD²Ò?gÈ Å¯½A_Ä
N5vC	6òÏ½ä`wÈàW¦à7ù3\x0014kF~ï]Êó¶9@\x001eÙL+E\x0005ÈûHå[y¸\x0016îÒ|\x0011¡°|\x0019d<=Î\x001fKcÏUéäü	\x000cÕßæ\x000b\x0016Hu×\x000b\x001c\x001a0­n\x0012ä©'õ\x0005\x0013z]ÃâÿýÃíë÷w¯\x001fÝCQ
¥Óé]za
\x000c%6»×ôÔ>òq½G\x0013W;r>Ú½®\x000eJÍcj¿ÖqZ¶ø>\x000b¿0³E¹>UvvCcF0){d\x000f¥¤cÈ2£r\x0001ÇJû\x0003xÕ\x001e*\x0002\x0002\x001e"¥8\x00072ó²ëè'\x0010\x001bÕ²f\x0013ÈÍ±þùì¯<X©~N¯säÆckEÈTïjoü\¿\x001b«ÉÒI\x0000­4RCh®V]d^\x0005´'2´±¶Ð\x0018D='L¸7_<ó\x0003V¬÷\x0002p\x0018GözX¥xÒØg\x0016u©.ÞçyoðzÛ§¶ÀY®\x000bù4²\x001e±\x000eî\x0011)¡^ùÿl\x001eùToOGTÕùÍïû¹«\x0008\x0008'd7]«Üx®J¬¥³CæU\x0010þ\x0018nÏ\x0016â."#£-
àtH\x000b\x0015æü¤wm´kCà~@LÂ³2&må\x001e9k[êdãÓ\x0017\x000fïq¸{÷Oï>¼ý'¹°/ôÐJ^îr¸®ámKgTXÕ`rÅ¶È\x0001½và ¥\x0010Zõ\x0014¸ÍOóÍ®øàåßÿâ]ù¯?ß]ùçïÚç½\x0015wïfÃcé~¶ºÆÚ¯×V%\x0004áÖ°pCEÓà/~l©n\x000eïÃ\x0014!×KB¹î'\x001f=Ùíäí¿°%?\x001aÛ?¥ò»\x0008@	Û
ì\x0006ØÂ\x0005\x0013\x0010;aS[Ãvy^mKØ\x001eÎ\x001dO
\x0012Á¶\x0006\x001bxûÇrm\x0016Ï\x001ca\x00078·?}ºM=
;bL°{~5î±#{Ôh\x001a¶T;!\x0012hØ´l/ú87Û\x0012rS\x0007º\x0011c]nÛ$FIO	:Aâ
.\x0006	"åÐ¡\x0017ý¶\x0004]èÔ\x0011®# µ\x001c\x001aÝ \ºÔ=tS³ÏO°eë"}Æt
;ö%ª\x0002à×\x001aP?w<\x0004\Ê\x0006\x000eî\x001c_I\x001f´{¥´¨õ,.\x000bxpêVj ¥lQG;z	ÜÑÉ¯­ïýä\x001e}Ú~rÒÊØÞ¾¹§À=\x00130íÍG²mQËÈâíãÏÀ\x0003Ù\x0000bÊsúÉó§m¯=\x0016´Ç»Ó¹\x0015ìq~¤gÃ\x0018ÊÜKØ >Ñ>\x001fæ$Kw
Ëaâ\x000b·ÅÍ
¸úsî%¾H#s";ØE\x0007.a\x0002EwÙ
¸p&Ñ¹3KS\x0017äýí\x000c;Ã¥xZ:Ð\x000fÎâ»ýv{ýq ?qÌ\x0000ËsÜ,«O!l!%\x001b|	\x001bÔÇ'p{,\x0005AlUlZôø\x00128¨O\x000cgû\x001cü²Ê\x0005N^Ù\x0007) Öí\x001e\x0007OOÌ`j` o_óâøá	\x0007ù^P\%äÉA,¡\x0019;ô\x000b÷ûéñc\x00164Iz÷\x0012³1\x000c\x0007¡ßM_3?¯\x001eÀ­zÙr²\x000cÞ;ßüþkzü\x0015ßdùNX3«>QB\x000e$\x001e^\x001fñP2\x000b!?\x0010¶ÓFú½øHÇÆ\x000b·\x000e;'úÉùÂ_´t\x00128Ø+yË\x0006xl6<B\x000cêÑû£1w/\x001eÄ0x]\x000cRÐÊÁ\x000b¡¯½%<ìÅ0X\x0002\x0007\x0019o¾\x0002?\x0010
<óÁ
hû×'Àë\x0013Æªi\x0001,"y\x0013¶æ¼õ¦ÀýÉ#¼ \x001b\x001eã÷'XúÞõæ¸\x0017ñ\x0008"HÄC)|ð`Y.[zâ^\x0010#\x0008b»cxïC
l
\x0003
ØK\x0014Ô\x001f·¸¿òÈ;pðMv=îIêà~nÃ$ìBØ.ÁÁËsvRås÷´8!_<\x000fGE¦öKdpÏà\x0007îÞ\x001c&GJ\x001b}è\x0010ý|ú®ôùªÙìtöõjÈsä|Ví|ö»öÞ¿`Õ_\x0008çJ\x001e½Uþ
¥*q×ÓûþDHÓHþ^u
\x000buuáåþ5
/^3
AbûoTùé(YÒWûÃÿøÍH\×ª¾{öo·oßLåÐOÍÄÈav4áü\x0015íæí¸¥&=ÅýDIf¯ã©¾ë5é¤k\x0017>ô·HdMT,\x0000°a¸\x0000lO\x000f \x001dâ)5FN.Ì7Zâ¼ë°#y3.Ã\x001bÇ\x0013· rÂ%ä°¦\x0001\x001b\x001eW!\x0011-öÕóÔU¸; 1Ü54¶a³Ió6+ì¸H\x0001|Üw{äÏ)~'	\x0007ç\x001a¸ó%Ø/v²\x0011x\x0004ð\x001f³de/]`[s{OQ#`gÂ§µ-öf¼ãÄ\Gö³\x0015Ã[!+ö©7sßlñX¥ÖïGe}	ÿDÒ\x00149éEøÛëúÝAýâöÝÝïo__¬ÙHÑWeÐÚkÈO÷åúk©'Ájû5BnëÐ \x0015ë\x001edQ¸Þ2hV^\x00108yIìIµ0=)\x0017fæ
Âvm\x0003t®ìÐ·Øl¥³ef&hOÐ\x00106\x0008J²5löuV\x001dí\x001d\x0008ÛÂ¹ÅV&Âf£ãúªMm\x0015\x0000zX\x0005çì9Ó¡\x0003ø4èÌ7búT´öZ\x0001:ýHhmo\x0000:ÃøçÃ¯l!#'dÓ*ü\x000e$/@\x000fØB8éÃ±2y\x0000{\x000e\x0011l)sW
\x0001GI¸\x0006
cGºÀ\x0011_Ãö«\x0014ï\x0000\x0014o\x001f)ö\x0004Nùc£Ê\x0017¶ô\x0012ýôæ\x0001¸\x0005ð±ªgºîlëêä{\x0014¯HkÔÆ-à|ð®5Ós
ÐþG
àß\x0005ìðc±÷:	/µLùG÷BÁæB\x001b¬áçÔåªëèéÅûò¯ï¾Ú\x0017~Ý¬ô³\x000fR?ûòÍ#\x001bgÍ©òìòõ%òåBtu"¥"î%
)>¸1éz[ü\x0012yq\x0001 \x0019QCÅ=¶¶Ù\x0002O\x001f9û¥k
Ø~`§«Ú\x0000,aä\x0018ÛÏ-\x001d\x0007v°¨¯õ²Bx|­\x001cøkùþ^hË\x000bØy`·p/VÀæÊÉ)IèýóÚB\x0002výâ\x0001I¹WÊVFl[øÒ¢;â$Y\x001cç\x0008<è§°ª>\x0000ø8y\x0016\x001f\x0000w\x001eh)7ï¥CJkìÝïííï§9«±\x0007õW·oo¦OTØ\È>¹ì/\x000cÍü\x0018{ÚØ~fõý\x0019\x0004ÂÇM)¿QÆ~k\x0018'o0l\x000bkªjÉ)pùB±Ç\x001e\x000ct9¸H»²­ GÂ\x000e=K¦-\x0001`\x000fKPe-¥'lúp\Y°ãª;\x0000°Ã=·¶2\x001dáÜ\x0007n÷\x001d\x0014IøÂ+sór,ÂN?öÜÚÁ\x0003ì\x0002Àö\x000e®\x000bv»^r3iHNRJ½¨\x0008>ü°O\x0006wÛk±\x000e®Å{Èë\x001f"IÄ)
¾¸õÛ³[o~\x001cúdÄBù¯oÞ\x0011\x001aàÆ~ö¯7¯^-\x001c>Õõ°ÜôÓ=ôËÇ0\x0011¢æ'õTÍS2çÍG8\x001eÇ})Ç#W±d~>¢PUq(,C`Àvðb«W\x0011=Õ¥[\x0013¶ÑÎ;Æ	\x001b\x001aáu\x0014y"¿Ãq\x0010rÙ8<Y\x0001
>­'\x0015`\x000cí¹1¡\x0008=4^ÜüáÃ×ßÂ`\x0002ÐÒ\x001e;\x000b\x001eK(Û	IUª½°¡5·Æ¹LÖðtbéÝ{×®\x0017¥\x001fØ\x001c0ä\x0011ê\x0007¬µJ28ó^¬\x0010%l~`ó\x0010\x001dÓ¼3l¿k_3WÆ\x000eó\x0012QÂ\x001ea Ðþ\x0000çæÒ\Ó\x0008J\x0007Ë¹\x0017ï+@Ãû\x001aÆ\x0010Næ¡([aè\x0005Ù\x0000a±EF,'!Òu\x0007uì45Û¾øczÿºW9
¼¬êèÎå¯ïnß¾&\x001e?Mð¥iÃõhóå\x0007E\x0006/Ìö ©}"Áo"ä\x0016k\x000b´ä\x001f\x0017Æ¿;ù½¿zþ\x0014yù>üerïÿãÍ_g\x0012OL\x0008oH:\x0012Â>¤½Ì{t\x0006=U×oèÛ¢\x001f¼ü~EÊì4AÇL¶týråÎãQÑV\x0007 ÕñB½6Â6i¤sXUp\:\x0013\x000eÄÑ\x0001hO§\x001e½âhÖªZÕ ÜÌ¨@Ø°í°\x000c²\x0017Kºìdúd:	¢¶:àJLoª^7ÊõñúXéuó«Ö\À*QI'\x0017nïúMÜ£g¹&\x001eÝ\x0000Ú©\x0007èBÇNð%Çá{9vâOy,éÐÁ=`Ä­¿°<Ç&Æ\x0000©=¹Êçî´qSÀ0À!q«\x000fnçs»òÑ¢7å<\x0000ÜÒcÿ_s+Is\x000c÷ÇÒYé¦ä*`£ÉÖÞg\x001d;M\x001dsï¬sXe@\x0001<\x00128dÞr>ªó\x0008NØyA0KÐ(\x0001|Ô<n_\x0012duß\x0007}Ü\x0006\x0002ìJØ\x001e;\*!Èç\x000e½C|êB\x001dàÐÚ\x001c\ì0jA1Î²ñçyó©òª\x000b\x0015À-Ü\x0018
?å«.n¿lC\x0005pG'§>ºL-".³mgÉ«.TÀF1ô\x0018Îd$æýÜÜSìs'mÕÞ\x001d`\x00078w:i	zÌaè¸\x001f\x001bÆòQÚ¸tpèÊûä\x001bçrst½»pJ\x0014\x0000x¢Csl/ ¦|ÇE\x0015PÆ»½\x0002¹L\x0007>Ü^\x001fnã6^Y¬¼ %p°ãBQ
ÝJÆñÈË¬AÞ¥\x0005é,£zZ´µ©:m²¸e,Ô.,Söd{C'\x000054Ók-<Ð+Ñ\x001ce_1£z\x001alÒk\x0006QW5ïUü~ÀÝ\x0017÷{÷:«¶bÀ\x0006õ\x0012;4§ÀcU§B\x001fØZ\x0001:\x001244>¥æ¼%fOE
Aÿc"%pV h\\x0014ª\x0013Ö\x001fvøÝ¥ò³W éà\x0006îD¨séÉ¯ì«dÒªg\x0019ÀAdîdøo¾\x0014\)ÖÀ\x001d;YÎUÏ2`þÈà\x0010tå\x0007¢Éè\x0007'â²:ìõ'þHÍ\x0004
ªº¦ï\x001c\x0015aíX5D\x0003¸¥C¯hò´öZNÎ\x0013\x001cáH¨½þ\x0004ÇÏÄ\x0010DÙ©\x001dØfQ²ºEÝ¬½\x0002\x0005T \x0019&
Üçjà;·Ýi\x000eû\x0007.@_7ÑqÕ)÷5ò,õ\x0007\x0019Ö^?C¤;W_ßªçóûe\x000f:`£zÞÑ~Áî\x000bÓùÊ¹§½_x¯\x0001Ù\x001c>û-zR\x001d;åÂÑn\x0013öú\x0019
|ÜµFég¦hVXo\x0013Ú+h¨$,	Zó¥
nUH²n\x0012sîõ3\x001a:8X-!X \x000e<¸ÜSM\x000c«¶\x0000·|pp\x0010#\x000fÈ¶³£Uz?ÏÔö\x000fØ¬APUQ?ÌªÛç°lû\x0007ðHà\x000eÀC}®°9Qú¸\ÜËaÌ|pö¸ê csãvêo~ÜKJdIH%êqç\x0006®8JO!ì¿f¢¯	µÊé\x001aIÝ²ï)7ö2á§L8\x0017MÑ/''>|'\x001bNû/"aÓä	-½éØ|n×+wiÿ)Sfpèè©\x001b\x000f¤n¯Ûb_\x001fW\x0002\x0007\x0001ñ\x0010õ¸1t×¼ÿÙ\x0012´\x0005h\x001aÎ\x0006U¾\x0014ÓÃÂ¼ÿ¿&äUB\x000bÅcepno=Ffòþsf\x000c¯,W²½"²frþ­=èòâçýçÌ\x001d!lQuÜéôìÉ1%÷3câèäË°\x0002Îoé#meç\x0005ÃeÈ~Ä*;Ô­ÐëSduÏ4­ñß~_`Zã«Ûg¿}óú÷TBh®5ý>k/ë\x001cs!ÆçeÜ»P@~Þ\x0012ÂÔ}ßïs¶»ßû«§y÷¿~ÿW¼ùwÏ~wûöÅ\x001aÇO,\û¤±¢\gdZØU\x0010¡é-OU¸´¶®h´órÜ\x0011çÎÚ3'å®\x001c]øþ<þìX¸µ!÷\x000eÖ)\x0003àPö\x0018ã¶{IýKCE{>rìsSZa{<yè¼~Wpë{kß8ybÍÍ?ä¦\x0005\x0014À©t®âßo~øû?¼|u÷óôSkP!ªrÌ(}7Ç
#%i\x0019HéÉËRù"\ÖTª8O[bä:Q\x000béxv&t§]G'2ÆG·×¡OTä|\x0017ç/«YµÈyxZÎ\x001c83j:óL\x0016\x000eÈ\x0016\x0011£Ò¼°Ê\x0000º^èlt`w"CXç3± Ô¢n#pÃmì^»N`ÌsD?²á	Z§\x000b
µ\x0007/S	ç
\x0005\x0016{,Æ9ä°³\x0012\x001c²lVÍñ'4´ÆW\x0003c¿¥\x0005Ð\x0011½\x000c[\x000cÏ<\x001d\x0019Å©ýDOh\x000cM±\x0019Å\x001ady@î\x0018	ÈINàôc¼û@\x001eâÂ\x000fú\x0012çlææòÍÝiÂäÊ\x0015øßÞÜ½~ÿì«7\x001f\x001e«!-\x0018Ï3ê1kGZûýêZi÷×T\2M?Ã!;\x000eþMåÂÁN4[©¨­¬Ò\x0017A.\x0004·`4µJÊk+\x0015µ]±H\x001dT\x0014é¡¥7rä²\x001a:Gh!\x0004¹\x0019Kei!¦ö)Kó\x0017µùsæÍ\x0001'¶\x0016SØÄW¥÷\x0013\x0018Æ¥¨\x000f\x000el¹Ýl\x000e[¿äÖv5j»*cGX}4+OÁð¤A<Vé8èD®pd\[íÈdUºLÖ\x0006;jíbÃâ¡IPù°×;-r»nCxù\x0016nñcÌb¹-@Ãàbµ|èÀåö¯¨S÷"ÍTÊ?¡ap1\x001a,Ñ43Êm¿µT¥=Ý9\x0015òOhÐ\x0014á\x001e\x000bÛ¸«èçm*äÐ Ò2¿\x0001}*1sw\ÍÜÆ\x001a\x0004ÖTÇ?¡Aô¤Q\x0018\x0013U	}M\x0016¬9åóCãzh¿ýë·Öö|¸ÕÔ»Ï$G\x0019é;ª×«éøG´Ê
éWÆ\x0011mMd*Ù)\x0010J¡Kâ¤>Wdð¤¢%¾ÁTÙ·\x0019TÚ«33\x0018\x00032<`:UJPõ6Õ}]MoÈðÉò=8râô¯UU\x0008Il¯Þ¯+0\x0017Êv"¼æÈ-GÍ\x0002ª#÷×|zÀ®Èi÷æfÃõ\x0007d\x001exì°Û!ºWw2Ïö3;9L(|\x0014d§'ìOXB¾Há¡àYâÂ©Ù\x0014»ÐMvä\x000cv¤\x0010³[	lãÇêÖ®é
»@Ã\x001bf+ñ"JpÇ0òÂºkìG+\x0003Üàoè\x0014ç?\ø\x0016â#&£ü\x0000\x001d=5Hg<Ä\x0010òò\x0011»Bã#\x0006\x0017íÕ¸D­<}Üb;;ÀB4c³d¼GË8Ï_0ôÜúü4^ùi\x00042·â-1f´§Y´ë\x0018ì
àÐ>ªÀ\x0018«Í¨]¿ºWh|u\x00136B\x0017W·½ºøN\x0007ÝÚ\x001cß]¡aî¾¹xÈð!4\õÎ5CZ\x000fú\x0015\x001a\x0014Ñ\x001aºk§²ÕkÊ°êÊ»"CO^÷,R¾\x000fUeH¾\x0007\x0019SOÞ	
zh<Öºd)\x000bµc\x0007 9\x0004uÕwB\x001e6\x0012\x0012ç\x0014kUQúQö\x001aòNhµ¨L£ììsrølVVGûÖN\x0015\x001dö*°]
Ø\x000fàS\x001d:.6¿\x0003ôÐÅö,aw\x001aEºjUj¡7\x000fO­x'4è¢h\x0008
å\x0011òz\x0003:ØÔwB\x000f]4ÒZ\x0005Rm3\x0012úR\x0015]=r;U&<k]CF\x0013u\x0004&gn/[õàÈC\x0013´ÊAµø1çª4ñ`°Üi"´ßµÿ\x0000N\x001cÉv4]áRyêµ¾©õî§±J\x0006Ü,\x001d8râ0¼l¼;¡aä©2ßP:ø\x00050¹Û\x001dÍq;-®;5Td·\x0018Mj\x0005eK/;Ôwj\x0008lFX\x0013ñ­õD*kY ]Yl~\x0007hPCÏ$R&Sk¶/Ú_2]
§¾\x0013\x001ag©\x0012vÝÈ»EjX¸ìÕNÝé:¦~¾\x0013\x001aÔÐ%¦2ä?úâÔxé}NS7ß	]@[(2'¼¢¸õ³Ëf¾\x0013\x001a\x0014±y½(|²%N­'Hì²ï\x000c}|2mºóJÅ£½ãµúøNè1\x0016[ìaJ¯RæF&>uÖz±J\x0014\x001d)LÀVÚ²\x00180Ú÷NX\x0018í/\x0016#-) Ò\x001b5c|=Fûwz\x0008­{MÈ=°U\x0019&§èól\¶îÐ0Ø/Ù]H­TßEe:p³q¬}\x0004hêÜ;¡A\x000fm&÷@M.É\x0000±ZöíÐ¤}l¾kKÌ±>ëÒ[õìÀ/@\x0013¢1m£e±Sá²ís\x0017SÇÞ	=hCjLÏ±Üe¨åH(HÔE¯ûõ®È£[OXÃ¹àUÙ*em:Ì±Ðw§\x0011´Ðg,,æ¢Æ³*,Ær@ï:\x0006ø_ÈI½\x001cÔ;nú¢©Uï\x0006¡¶º9OÄ²ÔØOéCÀ\x0013=ïàÐ¯:°&f8ªí[	§\x0016À\x0013\x0019¸v¤\x0013\x000b\x0002Lí)n*a¤~èPG\x0010ê)7a\x001cÏDgåö­Ská	\x000c\x001c>M
Q:s\x0019ltº§v\x0012@¢£#'ÝX¬º´\x0003«s÷\x001c§~Å\x0013\x0018¤ÿ\x001e\x000exò< .Ù,9OäAµ ¤NàGKÑ¤¹ïÃ3wÉZ!Od Z\x0008413(\x0015\x000b½\x0014£ãî\x00140\x0002\x0006"ÈµRL
\x0003÷\x0008|j¯<q±EZ\x0006rRÁld\x001eè:×kÚi_\x0002í»°àO@>Rªª¶ÕÙü§®Í\x0013\x0019´ÏQ{bNÚ*¥­GUsëØi_*dÈ±¬}Í\x0018)ÃßóJS;è	
úç\x0003Is¦±c©)iîÙ»¼SÀ\x000cÔ654g\x0019Â§;\x0005¯|c0x§\x00194Ðy¤·
\x0014]´\x001aë±JÞé_\x0006ªbiüUFT\x0003ÙOÕ\SºØMÝ«'42X"mÖ×èÕ(s:nw*\x0003\x0018ÐL\x0003ØÅq\x0014\x000eèbOä¡Ò\x0004\x0007i°\x001c2N\x0003ûÀ<:1öäkÞé`N`A32¶NokÔDé¥3AM½¶'ôPBiÂ*§9,¡SRµ¸N9w:\x0006Ê\x0017z¨mÈj´\x000eæºìá=¡
®9_TQµô\x0006ª:\x000fbÏÜ\x000e\x0016ÐA_ûÐ/Ô®3Y!>#Uv:X\x000e¦rt]\x001d#O\x000f·ï\x0005²²ÓÂ\x0002Zè\x0002ÆÞ9{NÎDÕùÚ¼²êg>¡\x0016öqBhçËÈk5ô=\x0007VvÊR²¤À^®-úoÈjÉëÖ¿ìÔ¥ºB­
_¬èÔcxL\x0000¶¡-É;ª·Kz
ïÃ\x0015}èãªwêR
("Í¡TÉâY«¾bXÊN]ÊP¤ÖY% .sÒ8ºÞWwúR¡{¶\x001aªË`\x0011)¹Ñ§înÝ)L\x0005i/\x0000°
eÃÝ:ÞEÕ\x0012uLZÖÆT\x0007öÃc
E8
*Ù\x000få,õe<u§/\x0015ô\x0005¤\x0019G7½\x000bÊD»îÖÝUÇ%ýOè3FöøCJª\x001dîøz;\x001d¬C\x0007£´°Ì\x0019G<þÞYå\x0019Øð©;\x001d¬C\x0007û\x0016"ÜZÇ{Î¼xÂê5ìDÏ;M©\x0005Ä¹R_ûG9W£t)d<[3ä9Jë-ÜU7bþ½\x0008bÍFê,\x0010ÃZñ©5Ü/ç­ò;\x000e&+k6\x0012bG'\x000f$ñ\x0005:\x0015åI\x001bÝËb\x000eâëÍe[ slÆÍ4Ó§\x0008[bQèþ¿Ý\x0015Ù­ýñ½ØÎ2ª´´rà\x0013+µ5ÜlÕòÅÍñx\x000cÛJ\x001eNP}L©'S²Ûg\x0007à¥T`[mnª"lK^Ý\x0013©Ó.y4x7xú\x0006¹ý\x000bí\x001fè/yÁ¡ÍÊ[Í\x001dÒï^ïÅ»ù#O_\x0016+1ÛCO¸I²³ühzËÕ£ËNÂzpÖÄ¡½BØ\x001f\x000c×¶åá¡¿ òæë\x0012¾Ðìs9-\x0016´_q\x001d7ñ5H¯ºt¤WªÙ:v·åáfë\x0012¸
.Êî0Hi¸À1|Ìç+Ì1
=·z^ý@¶	\x0003\x00138GÞ>(S}Èe.»­/Èa \x001bZÚá.9Ñ\x0015p^6«]ÇÜ\4\x0011'g]&
«X,gçì1\x000c97^O_¹=\x0004ÄÕÔ|	rðcT\x001c9¦Ú²uù\\x0007òe­ÈydOE\x000e\x0019\x0007ã%\x0012¦Äuïò\x0001=$ÞEfwyÙ®D
º'K\x0016\x001dÆ\x0017h7N\x001d\x001c¶ø·ßÅµ\x0018¢Bö\x0007çÖN6F\x0013U»·LKW\x0002ú±½áäÝÛÜÂôt\x0003·ÓþöæÏw¯¿:ÕS«&km\x0014\x0001ª\x0007ðªHwû¹ñ¢Ë5±1ñ²´\x0000ú¤[HÌ!a6Ü8¹$O<q1·í®¥r%/sr´\x0013~i£.ÀP3mÿÿ*öV% äTð\x0002\x001bè¼È\x0013\x0012Mà7d®x·ge=µqA\x000ctS\x001c\x0008_;\x0001\x000f%ì*³ì5g7-MÔ\x0005\x0019JJébW(Ñ\x0014ßNsIW»ÌOdH@\x0007Ê7§;\x001a2í¼Úâp"CI³;pÍ¦M\x0008IíLµ¦.ÙÕ¯ÐàKª\x001f\x0012I.Gµ2CíÏqy3¸qA\x0006%\x0011îúL/n¡C«)L+=\x001c:\x001a
ÈF½{öåÛwïn?<Övý9ãzø\x0008'z\x001b0Hb-ýyª¾S?ZZ®IõýKZ\x0017Ê!Â¶E³êßu®§b'+uE\x001e}\x001dÙ\x0013Q¬"¦îü¬8\x0013ÝÑÛ1©+òh±ÊbO`m*õ·GaC\x000f'3u
p`bÕE\x000fÌ\lGËøäG]GsdÂUB8Mi\x001c®¨¬sqµèëDNpä³¤MMy4)«ýÎG\x001el2WàÑYU¸Y$\x0018OÑ¾dß»&ëw\x0005.ðí
Ñ9_ø@Þx,É9·Z»"¶ª^}Ã#[¦Õ©Êõk¼vý.ÐÐò/¥¼6<\x001b]lQ\x001f°7Ìæï
=ôoc7îµ9K¯ò

X
\x0012Q
\x001d\x001dÆ\x0005Aw":ÛÛ\x0005çÿ+ôÐÀ"Óáð¢WvàC­zO`gõ
=´PÚeh\x0005¡(goÚ©×}ÿWè¡òÔT<5õ°E£6e6e	Ë¶ÿ+r\x0002ÙóÏ+©!ÝtUÔ.·±ÓChú¯1PdÐî\x001dÓw±=eU\x000e»lú¿B\x000fM\x0017¨¸¯V\x001dZ1p\x001fgÞ)"´ü×epÙ\x001ev?Z«6gº^­[þ/ÈÐò/bþiIÌ\x000e×ÄõðØT0·ü_¡Gào¤ïÚÑm`Ò(ZÕlÜÄ..[þ¯Ð\x000eÄ.<çC£ëÔÄN#w\x000e´¹/ÿ\x001c@:\x000c\x001b\x000fC£á±E I\x001dzÙ;E\x001e\x0002][¤\x0008·Q¸\x001d8J\x000e®üØA{T7¹DÒï(õ\x0010î\x0005ë¹\x000fý\x0002=úÐ£¹¬A:¡à`@'.f9Ó³ÿsW÷\x0015\x001a\\x001cHòÓ\x001e\x001ablfzóE
¦ÊFÀÛgÿòæí\x000f,\x000e\x0018=(E ë¯p²6\x0004¸þÜa§*Î½÷ááÔ¢SÛýb\x0011Cø})\x0018«\x0007G,6\x0017å õ-\x0016IÖ\x0014\x0011+±&=ÑÊç»"\x0003\x0007Zs&\x0003#ÓJZç¶Æ÷ÊÜ\=+ógÆG,Jc:Íj©q\x001fêÒç»"\x0003³tæ\x0017:2-`ujêIÈW®Ù\x0015\x0019hÕd¸\x0018·A©÷Ñ)ÿIÚ®Ù\x0005¯ZbÛ\x0016R\x0004¼Ä|¾Þ¯×\x0016È@<d1-gÆVÛö\x0012°?,zþ°P¸B ¹Á*ðØÃÅ`Ñ3¢õô\x0005±l z\x0014\x0015òòM¿\x0002Ã\x0002Ýµå¸×ê,_Þ\x000b4\x000cÛ¹ã]Mæñ&qÇ»÷}t1\x0010Wô@@/È¢H\x001e\x0002æ\x0011öÖÌ6ÛzM&ðáÙ¿þð÷×?üýíÍ«g¿½yûöæîÕc%Az ¢\x001d\x000bÕ$
²ìîéVWõ\x0019Ç°ÝVówµsWdRUØ2ÐÁÛ¦.\x000b*Vluà[É¸kª\x0001³¬\x0017·Úù}\x0002C\x0017`¦¤¢\x001cª«\x0007é]nü>#\x0018iNý´Ó-JZæ*¯¸q\x001dÙ\x0013Ê3Ëx*\x0003\x001f­i;äBW¯Ì	\x0017º\x000b¥%®vrÈÏ\x000cö$ðclà1Ý=½\x0008VõÍÁh]m%§¸®±©:ÂÞ,[eM&f\x001c95\x001b\x0010Ë2X·o¬ß´ohæ)4
jíà2T¿\x0002³@\x0004ÙY\x0001SÀ_ZbvbIQÀ¸&.Q«^YÙ\x0017¼S\x0013ËjW!\x0004i4za9AÞÜ½õx¾Õ\x0014iý¡\x0014r\x000eÍqÌ@ÍOï\x0015:ïî9\x0008m!K´òDÁ9R·~Mf
±Þ\x0013²\x001a
KÀØ¬Ùv®À¤\x00035ñD_â½þØS=Gé\x0017T
ýÙÍ s{W2\6v¡®]+²]W¨>\x0013\x001f,Õ.×ä¸N\x000c,Î\x0012î\x001a6\x0019A§\x000e.È\x0015µ\x000f&TCàe\x0016rh~ñs\x001fØÿ+t CÕïûÔTð=Û°ÜsB£\x0006\x0016å\x0016cx~P§K²ûËÄÂ\x0015:±pÀ©Ó§V!zZnÇ9Y\x0001!³\x001c¬ç*cRí
.\x001e_q§'n­'>1\x000c÷3®)a°¸àzÖ\x0014¨ªyYrÏFHì1£:\x000fÏ_¡QU\x0012&p¢W-bÇ×l-½ø²S\x0016ïè}Å,ªì±à!	NàØÏwÎ²\¡Q[2.	B¿e¹Sâè×³óWhÒ\x0016¨kOf'Ø©î9§ªøH÷uââµ³ÈÅÜ\x0019c¿"'ºg\x0008½5<ÌTÿ´=\x001bç¹ù+t¦CÃ\x0004ºtg\x0005¾\x000fvÊ­ë¹ù+t¡SÿÿÍ½kfÉ,¶\x0004\x0017P÷ã'\x001f\x001a^
nS-\x000eÁ¿B²$S(VQÙ]Ä\x000b\x0010Ð6´\x0003q\x001dÜV¢ð\x0013ß1ó]¨ú&É\x0019\x0000\x001fm\x0019_xx¸¤+Võz\x001aUö=Û¹öÍOhÜ\x0011]®E_\x001c\x0017°4É½>·öÍ\x001fÈÁÐ\x0005\x000bå\x000c\x000f::¢Ú,6îÛæ'²¥1Ã\x0013ÔVÖØ`ÉYCVwíÐ£\x0002\x0018tÈÊî¼\x0016^z¦;2¬½ó\x0013\x001a÷!\x0015m®jQ³©N\x001bÕ¾u~"c\x0015É\x00088¯\x000eÓX¹!ÅÔ!~pµ_\x0002ìD\x0002Æ]¦ZÙªê¼oCÐ aªm1ªRé½´¹\x001c¥ÅÎ{{® 7\x0013û+ºøÎòtë\x001cä\x0018÷\x0015x(\x0008ÈFR"%ó¬0óx
m¨ª··=QUû3ü\x001c}
ÿ@rÜ½\x0014FçjHÃO4ü/.'uhj`ª|ÝäÝûÙÇ9o\x001f_¾»OÚF>júµ3å\x001eEk\x000cÜ¤ÕMÒo¦:\x001c>ÇxY&Ó6íi\x001b!mª¥Wc\x0014ù\x000cúªãá¿¶:\x001cÀ'×Qü¢°eÅ8rìJ\x0014jÜËA\x001eÈ\x001eC¯ÙÝÆ\x0007ëCZímêk\x000fÅ\x0001\x001c\x0000¸P¼È_E\x001e²juëÌ¸5\x0013| G@vÔgYZQº\x0008InöÌh2@\x0019AD|#ÝbØrw'ðÉÝµÕpWßO«áF³W<ËL\x001a\x0011F-¸ §Çé½¦®\x000fØ\x0012,2`Ì9,"UómñûâÃ\x0006J°u$ÖeÙ`QØáª-;_(A\x001eÈ°ý,1NDF60´j\x001fÍs\x001b%È\x0003\x001a6`t,æ©GªïeN®\x0017`7J\x00074ìÀ6\x0003ØL^Yù¤=¸TëE\x0019÷äÕN±&\x0014×
=dBÒGÏqn&\x00074¬hOuéóå\x0015íx«Hh±/\x001cÐö7¤²J¬íÊp\x0004-\x0016¹k	Â,zÆß?üüãËïÞ?ßÍ~&ØXÕùnÚùN^9pÉKrë
\x000fÎï\x001cì×\x0018Ù\x0018ÅAl)i_À^¢K\x001fé¼Õ5D6ºr\x001c\x001aTÄË[Øä÷x6GØs\x000cþ\x0010¥\x0008Q\x0005^ÉIòë8¡&P\;Õ 82³EÂð_ßf©\x001cËÿ\x001e\\x001bkb\x001a¢Ó\x001a#CÒl¼*@t×\x001alÇ5,^"\x0005z5\x0019\x001e·¾&ÍRöÔ¿.³Á¾^YØÖþ2Û	ÌR9n×\x0002\x0005"^Ùð)Óú\x0006íöÙ|£²ùâ©MÆ¢\x000f{Xûî\x001eÈWÒ\x0001\x0005ô\x0005l&lá®Â\x0006m÷©q³T¥\x000bõ+\x00084QúTf<Ô½ní\x0004Õa,\x00059mu8
\x0015ãÅ±É¥Þ\x001dI=?¬êÝú\x000bîUk\x000f`t7TÜèá/-;ãô´O¥~èÍÜfY1Nlàfð0R~ü¸Qùñ¾êÔ.ä\x000fXuö5ú	
\x001aî±bDFM\x0006¾¢É F÷	r£\x0012ä¡wVÐ 
/hÝù<\x0006}µW@´V\x001c!\x0002®\x000e­µ\x001e¼Úæ"?nT~\\\x0000û9t\x001b5·	\x0006÷S}µ[y'äª	zG½]z"{ 7*AÞ\x001dCà,\x0015i\x0014ÖVgGéV$\x0014¹Q)òv\x000cW¾g+oqSøémâ>AnT¼ËiC¢2eÏÍ2U¿CËÐ\x000e½Ú. .+"ÿ9óuÈ6',K\x001aM¯ænÒØF¥±ÅÄ	\x00039J±n\x001eÚGá××\x00087ùf£òÍ]æ?{Ú,Æ\x001fôN\x001c©Ê«\x0008º¤ý]S5l«Ù\x000e\x0004\x0005=®æ\x001aÔCå5S)0u¤ñ\­F¾HU\x001aªlkÚÐyÚ®\x0000¶=0V§±îSF¥*Û =&\x0014úíBB¾Õ©H¬?û7©J£Rí'ñI\x0016¢\x0012J-ÜòÙn®^`Ûåûf8Mº	ÒÇìðXea/\x0005Õ
<Ò×Áñ_øÂÛÆïÚëoË\i?´OË!Ö ]zÿ
õßPù/4\x001eü£à\x0002§\x000b·¹´\x0013qÛy»uLûõ?þþçÿ¼\x0013å¬*òÀà¥Î\x001f\x0011¨µÝ§oÙÓ&­íÕw»Ð\x001dªJÖ6÷,\x001d\x0003Ý\x0019íÙãw¹Ë	\x000c4ªg@V\x0012ê5p\x001d Ç°åMä@È©"Dâý,\x000eC?k6\x001d².ÜÏoØÎ¨\x001f\x00016{_³¬ß|=÷u^\x0017ÕFv\x001b\x0013ÏfÏ9ÀF\x000c3\x00113×\x0013jàr{öu®;Ñ¹År§´g³×Ñ½iàÏ½Õ\x0003\x000c:ø\x0005¶{viÏßÐ@buh(U¹:ÄÄZÓC*o£
\x0015}k\x000c\x001aöWbIë \x0007\x0019êjÕ¡
Vôª4X²íê\x001bó±¬\x001fV\x0014ËÀÇ6U2s\x0016u]xñÐF
Y®êÊò\x0015\x000bz0H®ã¥\x0007w´\x0004é¹fè4_}\x0013ÙÒ|@ÎU<HÏ´F5\x001dnûèÀ¼¦¡T[­"´µ!«\x001dÞI\x0002ëËlBãÊKHÑ³CM4WDÖzû~Ð áÎª¦¨V \x000cê_4qá±½J;¦åVN%1wµðÈô#ÁKµeqðt\x000cÑ¹õ]6á]æ2\x0019$\x0008ùO\x000fë?Ì(®V4~XvP\x0000Ú\x0001¥ôîõa6-\x0019\x0017´	*ÌkHfØ2_-iïhÌhÝÕÎRµ8\x\x001edô«cÚ{\x001a5Ü\x0000]²%\x0015´\x001eT®«Ýây· «HéªQ³u\x001e\x0006\x001a«ÂOVì¥>jÔËS= ë¨KÝÛ~Lèt9×meÔ\úÈ}»¬ô¥	iÔh\x0002[k¥ÄÚ +{i"ãFdéþô½¥\x0016HJvË^ÐõrÐ»«Ö©Î½Ïe%\x0019\x001dÐ\x0001wLÅ\x001e(Ñ1 áé\x0016ãkÕC»}^OhG\x0013~ãÒd¡Ö2»«{Ñö4j\x000f\x0014ðòê¨\x001fÅÕÁ§;	ûEu!rô\x0018l­æ\x001c\x00136ÒQ:\V8§Nã[X3\x0002\x0013\x001aw\x000b\x001bJ¢NS}æu.ïêÍ13
ö\x0012\x00051?1º='jâ\x0016\x001e1z\x0002p\x0013\x000cY\x0017dûd\m&°\x0004BÍ2då\x0018o;ÝâêÒ\x0006MâïQ/gN¬=3·ZsLhK\x000eS Ú{\x001b´Jì÷\x0007Q¼Ú\x00116¡c\x0007ðôVç]oë[M?&r`d\x0014â.ê$Õv3í¬ýÛÎôcBÃfñr~ò\x0004 éà*f\x0008Ý¼k5ýÈ\x0006\x0012ßY_ZZ¤7Û½ëÇÎ4hLì[Ë~"Jô)\x000c[°Õôc"ÃvqÔCUgtPÃuµýÐì\x000cV{ï¼4\x001f:×d{¾l5þ8 ¡Q\x0003\x00079%\x0016SÒä=Ê[?&2n\x0017O½pU¯×ïYÄÕùc"ãnqäNí:¢:¥C·Y­?&4\YÀäFÕÀk3«ÒIõ·õÇÄ
<d\x0018ñò²`nKô}\x0017®\x0016\x001d\x00139\x00112\x001e\x001drH)h>ÿ}¿XV	{%@ÍGD(Ùº\wr\x000cóåÕ¢c"\x0017Úày_¤åkà­âº\x001câêÐ1+yÑ|5\x001bú·EÇ\x0001
Í4\x001a\x00069£²f\x001aÅ«GÇæøTî\x001auä½bjýjÓ1¡q³R>\x001eu8j^zÎu¡â«Í=ßâ,j©FÍqñÂ¦c"\x0007\x001a´Ç\x0002AÖ)\x000fU_³=
»ÚiLèDÐ\x0005èúBTäFÓ{\x000cVÏ:`á¿×Àø(Õ¡^}]=/&4ÇKÈV]©m:XM5ùn\x000fpµ¨¡A#
"En_Ó+/ä×\M/&4ÇKK·UY*^zì§ôêL1ùa\x0001)oÛ\x0006­\x001a¾jëÕèrµò
®<Ê\x0010¦õ¤fÉó\x0010úI½^Lhz\C\x001bîÚGÅØþ8\\x001d/&.®hJ%\x0011#â\x0015Íùôà{Îcµ¼Ðø´(x.K0GKå\x000cÌÈÔ¬\x0017\x0013ºÐ>Äö:\x001c\x0017ñ\x001bòÂ\x001bR>«åÅ®4j¨\x0002È'åÂ?¿ñ]\x001däÕòâ®ê\x000e ©¶=àÀ4ô\x0000a5¼À\x0013sg\x001cfMU[<Ðnq5wÇÉÕðbBã
\x0000½òÑëêPå&÷¬Õêw1q=­;\x0008¥M{j©Z\x0019Ië¸\x0016>õ!_íÂÊç\x0002¡\x0012»-.w¡\x0019B5W»°FÚàÐìÙ\x000e,ýª¥Ê¼«Ý¾Ú^LèDß\x0010ÞZ-¾g¶\x0011U×¥¯W\x001b±rM\x0004nqqzæ\x0007s°¼¤}/·¬\x001a\x0013ºÐnÁæ$ÉMóñ\x0011xÔÞ\x001e^\x0000{lk\x000c\x001fÔ !\x0010³z\x0003DÕ\x001c]ÊÐ«½X~\x0016ø¹\x0016Õ{bm\x001b\x0013yäLçWÓÆPc\x0002\x0007Z×©iX}F%>¨NÖ\,>\x000bü\©|!d,Êaª::©]Ny@_,>e`VÙ\x0015¡dÇë:«\x0010r|ÅÅg±\x0010l¡Ú\x001esjíYJ]¹|¨L®\x000e#\x0013º\]·-rÑg\x0008Ë5HóÂß¶\x000e#\x00076\x0016\x001dl¥QUg6	Ú\x000f\x0013Õb1Xn\x0014@\x0016=~U8ã¹¶a0¯VU	\x001bèÜøÖ5ë|X®\M¶å+\x0017ïÅ\x00166\x0005^"ü
5G
ûªüi±üé\x000cÜ\x0004\x001bÆ«çÃ)Ù¡pz5Õ	\x0019\x0010&\x0018gGe3Wª\x001fÀWó\x0015J©\x001b\x00168?
ôØ?´­¡ArU¢´.}í7¼*$Z,$
=\x001cNÕ7ä¶\x0019½=WßÐ¯\x001cv²gË-\x0019tz¶ô90²¢·,Ô¢\x0003¥\x00107¤Ë¶´²Û:aJuç+)VmÄ\qWÒHØ¥Mõ\x001cþ#
\x001fåÑZ$\¹\x0002Ã£O=#\x0019V?[-\x0003ç¦E
\x0006\x000b\x001aØjr
ryØ\x000fE\·³ã¹íM\x001bg±æÚÓä´nXØÕbváò/\x0018\x0017ÔìQÉ¿}Ä\x001f^®?°üøO	Wé$'ÂfûÂôXu%öp"æë\x001f\x0011³bõ9jdpYç´9=<2Ù_­¡ìi
\x0019È§ùÇp\x0019\x001eÚ¡n\x0010¾»^BßñÞ³&«} ål_ûÐz>\x001bèÿíéÃËóÃ/>}xüðÃø9s¥Ëu\x000b»þ+¼HÇ<HðÅùf> ©lºÐV&q,Lîkã¦È?´P¼Äsæªr\x0008¶ì¾\x000cþ\x0017H\x0018DtÂ*ÁÚ·ÔÚ°sÀ!1&§
\x001dgí\x001b±\x0002× #®ôä\x0003\x0019Ì/*ñ /Ì
ÈovCm&r1±8êy²/)\÷\x0015/À¿mû¹\x00064ôs\x0019ÉmÃ;%+ÊY.Ü³#~}[âà\x0006+jðâhG²rI¬´dËU«Ø\x0001íaÔ\x0006Cþ\x0010¥\x0018ë n80oß\x000eè3:2Êdþ(}Ð5°¹\x0013l7]h\x0007rüÉlñW-qpB£K-Z@DÚ.TÆ\x0011[Oµ]/î·/í\x001f¼S'®OÙê\x000bÝß~%=\x0012zPóVì¶üüçP²¢d·ag"¶ßE+&)Ù<\x0004\x000e×'nñmÈ\x0006y5Õ;¥ÝÆ\x0004<ì\x0002Ö\x000cîð\x0010Ø -&bÊ¬#¼5\x001aÈp\x001f\x0005=p\x0014IHòKóÙ¸­êôDíÃ\x0004uá7Ð!(Í\x0014tÏ×^Z\x001f-ÆèF\x001c8ÏÝSMâ\x0008QºhÍÖÎZó\x0007ºyøKÇ¼¾tóp\x001f3ôáVÃ^àÒ\x0001ÇC¶[I	\¿vÈ´Q\x001cõ\x0006í±jVjÐcÖ¼Êº½Å&2\x001a-\x0019HN¨Ó©ð[ra_g¾ÄDj\x000fX¦%+s(}
E¸
û]÷;·AÈ¡\x001cw,¾W
\x000e}ï«]h\x0003}Dä\x0016%ú%ÅP\x001eõ\x0015ýÝ(ú{Ó®dý\x0011YË$¥tAQ×\x001dÏ^ÞM8ÕQ\x0015USæNº\x0014ÍÞ¶cBW:\x0008ZÛ&~#Öúý®û¨!#VÓ£v
:íÍ5&´£S\x0016â>¦ÌÒ)}kòÆµàA£â\x0002ÉäÓ&qß?<ávüËCR¢Ø\x0019½1^ñßuÿ°¤[±­µ\x0008k_Ù©)zO"o\x0008ðF\x0011àÇ¨Ñ·[Ñ2Ú¨¤Ð¾3y"\x0017\x000e Ì\\Ö\x001f¹\x0002É
)Ó«Uí*
\x001aå¦¼Q
Ö£>\x0010ö\x000cxÝÜ§ÚC'
LCHl	ì°a¼:@¬²J*\x0016gº(éG¥+\x0014{élÃÊÖM¾\x001d\x0019\x0013\x0001,FX(\x0016Ç\x0015Pw\x0019y'b\x0006f\1 ÔÖ5\x000b\x0017£6ã ¹í\x001203¶!±¹/¼xw}ç/¸Ã\x001fØÉåÝ`þ\x0003¢fímQéßF>U²¯Wý¹·XXý\x0001T=¨*°Ô½s,ïaûñÂùùþüüááW\x001fÛàá\x0017òÝGl(;U
/§¢\x0008·\x0001J,ëÿ\x0005í^Û4ñ\x001b'H\x001b7*Êd¥(­æÊl_"\x0013\x0018ÌLÅz·ü[ìVÎª\x0011ëè¸^í\x000eàó\x001d²!óÇ¢t{ZP¤4ÀËÖät"\x0016Ñà\x001eD\x0015ùYÖCÜÅÞ\x0013ùÌó¤v+CP\x001fÒHyv}ÛÆÞ\x00074Úüé!l~\x0013á\x0019ò"c4\x000câVÑµ\x0003ÚÁ|\x0016ó1I>a[+l=gÌ}Ê@þ¿/[\x001cë}?óW"ïÂÛ^¡lz'±m%¥!}þ\x0001¥Ê\x001c¤wq9®\Ø$d¾y|yþp?m4i\x0011W]¶Y;\x000eÜnVÊH3½ÕqUCù.ù6M:%iÊK³ÒÉêüFÝ¥d&2Ää¼ù¥ç\x001cÝ!}Vl¶\x0016Inýº&²§1\x0003=G\x000eUgH\x001aì%$È\x0010\x0017Ê\x0016ÍÊDBÚæè'2\Ùc\x000bU
ìÿ×ÖW7¾ÙÊ®Md\x0008È\x000bi\x0005\x0015IªE\x001e³jÎr[Ùµ\hÌÐÜ#­á¬:ÃÃÖ¢z\x0002W\x001a²§÷ükãõiïO}àbÚ$\x0013oW²TÝ]FlË^sBÃ>)¨WäHiôÄÚFÉ»}kÿDÕ\x000c­\x0015¥Î?\x001e·OÙ¼ïë°ðzh-öUUjÍº3«\x000cÏÐ«µLnµÒÊëùi¸_-8ÌkØ=¤µ".,cÎ=Ï³&\x001f\x000ehL>dæø"	é¬Z ÒPÀ^\x001fÛ\x0013\x001a§Cµgf-,óaûØÍ\x001dy\x0013æ¿t^®ÿ\x0002þûo/\x001aY5®ý¨Ò£à²«üßâ=~B\æ·C\x001bôÁåØÆþTÑMñ¯\x001dÛ1o:¶·DS\x000cñðþñáÏ/\x001f?üþNO\x0018¢R0vóÅ\x0013xh¦R\x0018Ñò\x0010y'¯ºq7\x001cBtð)CÒ¶Õ}¶·ü\x0005\x0019aY"ðQ-§ªãÒðØuJ7î\x0003ß;QÔÓ \x0010ßå\x0010Hé·¨öÚiö\x001b\x001bÈátúrKz`ùê\x0010TÏRêÜ­Aäð!e\x0004æªeûà \x0015ð\x0006E{ã\x0002\x00129|®ýï!ätÓ\x001c2³+cÌÛ×ßD.0\x001b\x001aÒs¡|^
=nïªíëo"ÊN»NàdéÁ\x001aÛQ¾IAî\ã"\x0007\x0010m2\x0002ã;}?å³\x001d£¿`\x000f\x001cÈ\x0016\ ~hç)\x0005±m"t»P\x001dÈ\x000e\x001då6Û?O\x001f0ê¥áã^É{B[P$[¡[Õ³W»\x0013¸Ï%º}Õe\x0002[Pô>±-¸(wñøæ,I¸òÌ\x001d\x0010\x0016753bx¡Öºqe\x001f÷Lè\x0004\x000b:Ê %#QÙÝÍÊW¬\x0003\x00196aÎ\x000fÜ\x0017y\x000bDËõ6?q\x001bSMhØÆãþNò0E;lQeèñ\x0015¯¶!è»B¾\x0005IyQ«öav·óxÏ¢¼\x000b¿¤¨èQª¬À\x0019[äN\x0014·\x0019\x0014ÏÌÊ\x001f<¨üN¸\x0012=aé	·\x0014ÅDYJ+¶WP«z£óîú±ÏaÈüÝËó\x001fþp¯ Ä(×öXÔPYk»m¾5ßÌ\x001dÜìèukºAþ\x0005Ó
A<b )\x0010ÛÑMRì5²=Ï\x0002²¾¤\x000eä3?*Å#På\x0013ûS2x0µ.E"m\x00148O\x000ex
¤\\x001d\x0015á¶}'.\x0003øÑ½&\x0005\x000eä\x000cc®\x001fMl2\x001bMPùÑÜõóÖ7Ú|æt/ÖÇ«kk\x00158Ïn\x0016/_ùtG¶ÕÎ¾ªyÒ=!¥[[(
ùP<½\x000fÄOC~\x00178 -\x000cÊ¡íì \x00066h®ûìË>1p@{NØÑÖ\x0002Ç|&k>y'Û¬ä\x0000\x001dðÁÔ.\x0001ª?5h&\x001cú£¥æjå2_ôÐ\x0016põ\x0015ù-æG\x0017ÚzßLhX ¡¢`n4\Åma\x001fs;mÚ¸@µK×_=þåãûü½Ü§¨UÕ]Ým¡3Ê't\x0018Á÷ûó­ÎÖØéu?~¶\x0016§ÏVo0á\x0013k`yöj¸÷@<Õ·©Ü\x0003ù\ã%\x001aòR>'²g&p¸ ×MäóÔ."\x0005K¼-KF6\x001c÷HÍu$>ÏÍSÚnAäöf@ÊP;{éq,ûûà@N0æ©ÜØ~\x0002÷s\x0019.ìÍ&lÏ±-Ör$t\¹$éG;Ðz\x0017\x001cÀ\x0005Æë0JC©\x0016¥\x0006ÞëÎl_x\x0013¹òáX 6ñ&ã1;\x001b÷'ö\x0013»´ø\x000f¸ç
\x0013\x001b2¿ñ¼!.§ÈH-Â)òÓçïxn¡ÚÏ^Û¼WÅ©V\x00151Ê\x000bzÒ¯-«2¸þÐy+\x0012°Ù%Ë¾<#ïKÛ>%ÇÈÜÌé´IÀÞ×f\x0002ÛRú¡3­ý\x001fWJæ
K\x0018\x0019Æe[Näs[hÈEu.*\x001fäPfÇ\x00150tXÄ!Jq\x001br`Vu÷¢\væD>w¦´¬£ùLV\x001c¢Ôs$|ÞíÌ\x001d\x0016\x001cbyg(Û­¤fÃP0\Ã´\x0003\x001aÂ4\x0013AgU#+¥¨Wðè=]6ýò\x0008\x000fÀâ;ÁsfVÈG'ç\x0015´Q[rLÈJs\x001dô6þÀXæ$CÖb6"	e%»%¥ômþeBCëF$ÅO±½ jHIVíÂ°w\x0010ÐPBJ"bBÅYÎ42;WÛ\x0010ä¤M,\x000fJÕÅ;=è½7ÑFR#i
&¡b\x0012ë5++Ñº¹æ_&4ìDOFÙB¡ÕáÔv\x0019e§«Ý\x0002ÝÔ²\x0011q¢\x000f{JÜêX2{§	ýHäW/?d*SçR\x001e WÐP\x0014ëYö¬%SP7^ßãk\x001dnBc\x001d®0´c&f\x001c@µËtOMÐ\	/LË#\x0007µÇó^?ù\x0000Föh;ò1\x0016«êÓÆGyÐG¯>"8´Ú\x0005<zåÈ£nOáß«zÏLÐÈLµïð`=¼\x0004dNf\x000b¯ÏÇ¦Zx\x0012®\x0016\x0006Ã±²ZÎFYÅ\x000c±c»ãÞ(þ\x000bô\x0001S`\x0002´ð0Ùõ\x001f0Ü%lD9\x0001÷=~ÖZåuCjÔôÛç§ç÷ïn³\x0016¾ÝËôÑe&ÌÔ$pü\x000e\x001fá[gwãÞ,\x001dØË?Z×\x0014|°P|ÊbME]\x000eÛ\x0005°í4ÖÔëY{Êb\x000f\x0014 ÷\x0012\x0001Û\x001e\x000c.\x0017gÔÜ£ \x001a2\x0001fZ\x0014Ï-
ß\x0002-Î*»03jPCÎ°ÖÛÒ³$c\x0011Dª«Ý¦ì¢&òtä\x001cØã;ÏÀ/*qQSyÚ²WZ[v
"âRÉ\x000bv_ÇÓsÀ\x0011g
Å\x001eÍòGWÎÕÊ@ÐGlÃ\x0016\x000c2)sY9§´
×¢æò4dT
oçt¢\x0017HVK£A/fÔ\\x0006]üÛæ£ªù(V­²góDÍæ	>Y"rw&¤eWèªo\x000fÚÑÏqµ:Ð?\x001cu³ËA\x0019\x0016ZxÁ¸¡GµÚÍßf\x00044\x0018|»qºÛwEµ«N\x0012\x0012Ò(\x001f/\x001a\x0018nÛ½­Ú>	0|çÈ¿Ó%¾\x001dj\x000e»\x0014D\(¯|xúðá~e"Uß5n:Úêó;\x0003µa\x0011ezCW(1Àý{¡Íº\x0017Ú{ÈZAÙß\x0006«\x000c	¼w»a"ux/\x0014*HåÊ¬¤´MZè_wIÒ\x000c.ÃÅÀréíøx
Á«<oö¨3\x001b"_ì~\x0018h!¶hSµuªû\x001a0G\x0010±À\x001c·T\x0014r\x000f¯ÖüCÔWN´1D!m}¥aÜ(¬±xTWüoí\x0010GO]9í¼¯\x0011M`(fñÈ¹ÕÉÏY\x0017N*^vyçLèóÎL\x001f(uã
\x001c­R\x0005²vÏKÐP'Ï\cJêÕ9ä0t¬\x0017é¨ï³/\x001dõ~*ý\x0010jâN?«¸AF³ÆHÇÕ^2&zo\x000b\x001f
Ó\x000f¡EÊê`Ov8ìàE¥\x0010
mÖ9ÓýÉí\x000cÍK>ª|8Än´±Ä>ÃÉó\x0014úÇJ£Èçò\x0010ýiL!µ$\x0011í¨XU¹\x0019>²WË\x0003d×R\x0008ð¼\x0014®\x001bVêÁô®ÒÏ¡1OF{'\x0002ÍUäæ°³â\x0008\x000cêò&C\x0010U =#	gÛ¯Ç³%)\x000ftõê!ß\x000b\x0016hÏãÙ'TÊ7<\x001f¾ïµ\x0011tB\x0003\x0001Á=¥\x000cQ\x001bH¾í¬öÕCg"´#\x0013h\x001fJ\x001b\x001cîèÖî·ÕGö\x000epNÉ\x0014³\x000c4¤×C=h5ºÐpÛy(öçÄ,LêQ{
Éï¨Ü·9ÁÐOÉtÔØ\x001ej!¨y1\x0014iýõ_°ÿÂÝ6[\x0015·ÛÞ¤¿àÅÖ\x0014­&¢Ø1{ô®ú´i ¾­HpS½2â\x000b¾E\x0000ÊW»ïÿ­óëù\x00070þ¾\x0008^_
|ûg~å'\x0014ü	Â¤ÓÑr\x0012CT\x001fA\x0004iÖ\x0004Ð*3ôðÿùt·ÄO©tþ»îÈx<R¤£
DDí)½]\x001f;OäÇ3?Zd(øQL«ÈÁ'±·ü¢MCåv}àk¡6#dîÛ»Ðó«SS¥Ã¶·w"{\x00183»ÙÊOeoUG\x001dÒWÈ:h\x0017\x0011¤!³Ð ø}ÏU¨¦Û|V\x0019\x001acf'D471+·ª­ÈÐ\x0004N4Í¨Nà)¢Dç$\x000eÙfÁ´ÂP\x001f/jÈ´
Ïª¨¾³[9»\hÀHÎoôJ6Â\x000bÍ|_Ó\x0012CmÌ¶WWo¡P$»6f§B¡Á\x000b^S(ZbH\x0006
÷þ:buñÇ}¥uââö#µæ\
=)ÛÓTy	Æ}÷ôDí¸³>tF=fª¸\x0008\x0013÷D»	ìiÈ`b,m\x001bgY
yû\x0016¸p\x001dÆÌÌo¸\tnwÛ§í´¶PÖqÐ­
ÚpFP\x0007*aOàÐ¸O\x0002µm$EòÊ+(]h\x000bMäz\x001c2ñ£Åò]y2
Kî«ÕL	ÁÔÕ\x0018o÷@½&2\x001fê5ÒG½¾Î&´¥Q\x0003
3\x0007ÿ
\x0015}ñ\x001a¹ZÐÎÑ ÁJ*±;¼Y%úòX\x001fg\x0013\x0019VôA=¿H5\x000cDºOQ³Mè@\x0006è¨\x0004$Í­xÖc¦¯öÃýâ±\x0018]R· {II×Ä¶4<q»Dò\x0010õ~\x001a3;ºùaØ²Ê#LdÜ-ä\x0011,|É\x0001ÍG¿íùõE9\x000b(pê\x0019ì\x0014'Á»¡Æ|µ\x0011\x001d_+`øÚ\x000b;ò!Í"ïaÔWÖvÔrHmÔ\x0001*å¡°ßG\x001b´z@fu\x0004È°\x000fs&:L»ÎIòÃ)+©áAº>°'²£1`QHsÂW´«Chéj\x001fzÜÔ\-w\x001b3W\x000bÃh\x0008\M{'t$h4!Ëthè¸M
Ld¾[àÀkG¥>Kù\x001b:?ÂÜ«Ý\x0002½2h|\x0016E£<eÙ2z:×|ÃDæÝÎ»V\x001e\x0001w\x000b·þ;×\x0019í«gï®4hôì
^|5Ñ&öØüjI\x0007ËÈìI!©SýS¡³\x001cÖDÆDv4\x001dèô!R¼\x000f9p´±\x001bo®½\x0013ÚÓ>Älåa6\x0000VîW¶ì\x001d{'t \x0008ï¼Ä<0ÔÂ£\x000bÑ\x001e^ÀW»%D\x001atâ\x0014«ç¨8®\x0017×WÓÞ	ÍÛ\x0005\x001aÚ\x0001¯¯qN¢µÛ£§£®¶KÀí\x0012gc\x0002I8´AóK6\x000cSÕ·w"\x0017\x000e=ÀæÃ\x001aî\x0012%\x0018vu¦«oï®4ÕØ¶R\x0000«LÓòßvÆ½\x0007t¤(ïk|d²¹£óÎUö¦½\x0013o\x0016Øà\x0016æK«ª¦Ò\x001b¼âÕf¸Y\x0012ºÔJ\x000fOäS³ä£\x0019fuÖÈ±¤,Èª¿¡GK«ÿíÎ\x0004
o*â]0ñÕÚ1¿ê³¾\x000fyEÏÖ«,Ac/­êÖªª+#tïjø:¡ù#bc\x0010/\x0019c\x001a?¯>bâ¨b<u\x001fª7\x0017÷Æ¬\x0013?"<¶B
*N/îðvh\x0011\}ÅD_\x0011"¼¬9EÅÁêpzàfü\x001eIÚ¡½<\x001dç~ø}(³ó·
éöt\x0016öÔ\x000f)i0\x0005=\\x0012®¾aÆWy\x0007Nóm\x001a¹¡¤M\x0008-vÊ­¯¾aæp	 å­áÔÊc£Úq\x0001¬n¡\x0013ºÒ¨¡MÏ îÚÂE63¼æWçÍ\x0003º`:\x0005}\x0001¢­J9\x00174fôÒÏbb2/\x0017\x0003&&rsAJ{~*b\x0018G\x001f¶öçg®ÉÎmNÀdç\x000bg%ïh¡·ÏÉÔLÊ¼^X<9\x0016b[NýN7+sé69_;9ùÿúô¸)m¿àøï1½ÏÌiêh±Æßpõ
ÚoøÝWà«	j\x001f\x0018&¨Xvvt*8á\x000fÜÂÂ~\x0001åáí\x0000S\x001fX4\x0014½dõ+ÍË8W?\x0000Ï>uºKlÏ7¿\x0012Ïh±ý8Ë^ù
qY¤\x0010ÂùZt¯]½ÝFÈÀGÐSúöéç\x001f\x001eþ+xjBæUz>Þ~J¬¤_ûúVüåöê.##\x001b¨Rð)2mÜ>²ç\x00070ÙvU¬|>
]ûpË¶OÉ1­J½Ôm3ïD¿sÌ|Ï DÄß\x001aZL`¤Fo?â«\x000b`W\x0014ÈpÃ&ªVt)I\x000b¼B¶[ÚDæg\x0010\x0002'n`uµªÉ°Û\x0002Ë\x0001L\x0005\x0016dìvdl\x000b\x000b»yEm{c`Ó=zçÞ|ÿø]Û\x001e~óôÒÖñ}v¥ô'³ïóY[nr(u&\ÿô>øÕ<£zÞÊÆ\x0014¤3}DP~r\x001e\x0002¾WÈg³4÷A\x0013¡\x0015Ê\x00036¼xÃ\x00140ÌvSNä³0[\x000fëÐ\x0019Ã¦^Éõ´-,OÜ³\x0007HÒ``\x0014a\x0013ÿxý»r¯9#\x000c¸RjBâil]\x0015çT\x0002=ºXeï\x000fä³AL1ºk¡\x0005¹×øÀ¯-³P¸g÷ \x0018é\x0001÷ËfÃ=ÍBà&\¶b+\x0013ùì;KµÒ²P"\x0006ò¨ç\x0001÷2ÎÆaf Tª\x0014*Ðç5r\x0010!ëÇììNLÃ®\x0004÷\x000fß<¾o\x0001Ëó½N\x0012«ÄU]§¥ß\x0011CBÉ=\x001fMÿ\x0014ouH¯ÌçHjXÅ%t<^iÁTVí5OO\x0017ûý¾
_XÅøfÌ&ýCÀÊ
Ë\x000c\x000fÕUFÂ*\x0002\x0017	
h(lSß(³ \x001dY½UDÂ*öDûdf#Auôõ÷]Ùë	YEð·Ò\0ªkÓ&®r¹Ðe¢·²¬sÔÔC(²9Ð¯.Ô>RM\x0015Ò8\x0007âaCòò	öÐ7Ïïe\x0013µ+ùùû¾Êî³ªá«¬§\x0019P\x001aAÞ H\x0008\x0014þå:9Ú,é\x0008¹=Îµ!&Ü\x0014¥éE\x000fz\x001b!§çe3\x0019"Ä¨úå,'ü\	[)±\x000c\x0005\x000e1Lä0È0*´ª)\x0019¯m4\x001bË\x001dY\x001c\x0014ÏË\x0016å-0.Ë­9\x0013 G¬ÙÉ©:j3?7ÝPeXï¤\x0019Y"/È"¾o\x001c«ì]î\x0012Õ«ñDÒ,Ç\x0002ãAô3!«­?D\x000f×°>iF;ÔncV$«D Ýáz¹\x001aO$ÍÈr\x0019×\æ÷^;K©Yò^ðfâ\x001bEzú\x0000YX7\x0008l3o<4Ñ¯ö	\x0010²\\x000b @WHV\x0006%S¬Ú%\x0017þ\x0013\x0018\x0016³¼\x0001U\x0005Ú(Ó­ö¹÷J\x0013ú\sm\x001f°\x001fj%wP	Õa^ÉM\x0013ø\\x00186Q®VúÌè%)I\x0016\x000e{íò\x0003\x001a\x001e¶\x0007ô«gûÛ4Ï¥aÅÎ²YÚ°\x0005®J¬ÍØ½ÐÃ\x0006\x0010p£HC\x0018¹\x0015¥\x0016FóçÕê\x00005äÎ\x0014\x000eÿsÐN
z\x0018ñnÌNfóâ1;\x001b2(-U{üæ=çfBnN4Õ5p4RTwÕ~õ\x0015\x0019cH@\x0003\x0007{mÕ¹-ueq°\x0011\x0000xâKù¾Wé	Ò\x0011\x0005_w±\x0018ªâ
\x0001\x0017âÍP¥¸Z\x0017Ài[8Ö©gXðB*Ï[JÌFÃ´H\x0015bùxÊÉ6¶w\x0004¯	ö\x001d¸¹ÆÂDIÉurÉÊÀ Yâ\x001c®åd<ëaI\x0012yLôÕRö`ßxkû¤<cøÚöi´ö\-ºÀn»\x0010\x0011Äªì0ªÆóÜËt»Î[ Ãí¶(
\x0006\x0006ð	Îx¾csÝ¼yMZß¼?ÿÓcC¹[Wg{ë\x001aâÏnûçl²­C¸è­¢õvùäÏé»^¢õ6o(ov}ª\x0014n\x001a\x000eUWÈ\x0010­\x001bj\x0013»_®¿\x001aÞAiõ­-IweÈá¢\x0011O'âØÄ9»"ãÚá¸y\x0007DòQvìÛÆÌl.TðÖwä¸Ð\x001b©ª,eî~\x0019uµWpy\x0007ÈÛ\x0005Zº«ðÒùBÏãþZÅ·6Ï\x0000t\x0013ùT1k\x0015/a*½6!.Ï\x0000o¨c JÕ\x0006í³<D÷×&ôõ\x0015P\x001cÙ»À¥\x000eY?-|Ñ¾¼\x0002¼©4\x001bKáÇðs+çpÑ¾>\x0004Ç[¬\x0006Å¾±{\x000f³»x
å)Ðb,Hgµs/1EÆò{+\x0017sÑts\x000c\x001a,ãa\x000eÍ\ 927]è\x0007r 1ôI\x000bm\x0015\x0019ÉªØû6Mèëû¥¶-}¥å1ÎWo[x~Ûø1¡a\x0017:Ò¯\x0011]#2kt7K=O®ö¡åç8È\x0004µÿ\x0012q2Õì\x001bzáë4a\x001fî/­W/¼í³kBCíÔh¸äô[£½ÀKKoHß¯J`FU\x001cké±ä¦\x0007}y¾´ç\x0019ô¡e)®3qÛÓC -.¦¼>_&4W3AHÊ<Ï"³\x0016¥ºm3ÂD/HÆ(íJ±¢ã¶ï¢\x000c\x001f\x0004\x001bÚNÐL\x0012\x001fmÌ\x0013~ub/B\x0000Ïìø\x0003ÒÃH\x0004âöµ5Q¥æÎ*w\x000emeàk¼ß$M×n¯Q>¿ZsÔ6VY\x0002\x001b®\x0019iÐ²¾æ&4òß0Y{B\x0006xÐ½\x001a½\x0002Ôï¹6æñ¬cöyaLÑç3¹w¯ï¹	äÈúQ!(bª¶öï¹	íB3\x001d«
\x000c*u¶Ô)4ë{nBgiØÞ ¤	Y¦z\x0004\x001bM\x0005ý¢ëüHÞ\x0010ÃýQÄÜh#¿ÒMèJ£v°ª5ñ­\x0005¬Eúo[µãIg\x0008ùdXdiÌ\x0008ü\x0015I/Xçöí\x0013\x0013\x001a\x0010\x0006ÈÕ9duÍz\x001byªGGïF\x0008"-ý\x00139Ñ²®/Ú"KÑ¶¾q'´§¯\x0007^°ïP\x001bRÞ3§ºßàkÿÄ\x000e4!\x0006ÏNõ¶Ç/o°í¸KÚèv±À×JîYÓµyb"ÃF,X\x0006m§©j\x0008òfí4µûæ	­úXáø¨ë\x0016
VG»\x0001ü¶{bBÃF¼`ÓÔP.O®xµÇ»öÍÚ=1¡+Ý.>Áä.j×\x000b_©LkÃ\x0001\x001dùâ²\x0011 VÇGê	ûµÍaB+ýsMw<­\x0010Ç+ÄõfmsÈ¸ô,äëÛ £î\x0019vjô¯¸¶9Lèüµ¾úØæðEÈv5»¼=-Âê¤\x0001/¢ùü°¥MEö¸ß¸Wè\x001eÑåÒ­°×£Uý¬E­ì\x001e÷F¿P{o\x0004©½PÉ^çÄ\x0012··mÉ.¾\x0017òÕÐC¦¡;\x001aº¯ú¦ñ|üÈl+\x001b³M\x001e:ñCÃJk6@ur&2{59ÁÒä êM^*¸Ðáp\x0002WØ¢wüµk&ú«o\x0015'~$Æn5uQA¼wÔgíY[9v\x001fi^uÃ\x0001wR\x0013Ó­à½\4Æî¡"ßÐý;¾#\x001f/£M2_~ÑL#w]\x0013í¶ Ë² yä©Çóa«&5/!NgÙEd/7ÍtÒ,	\x0001ÃY.\x0010|y{ís¾üß\x001e?<üûã§ü¿wÊ·7$3÷¢+ÞâëÑëy¬ýìLÏ<¿UÆÜ\x0015Â\x001f·Õ­*c.\x0016\x001d°zÐ"\x001d!>îüó6a>A\x0018Þàgm\x0013RÞ¡e¯o7(k\x0016\x000cÅÕÖ³ê´¶©äÏ±°\x0015FµÜß\x001dñ»´öDR*m¡\x0017ö`á¶Ãu5õ¬:­mªëçÉ
9³OzµjiÅºÕ@ÈèÁN7bùJv\x0004¥\x0016\x0005\ö9â\x0003\x0019R\x0012ÑBsdµöÆâ\x001cqC³æjÕAØ´+Üd3Wàt\x0005<Æþ	7FµUçMò(\x0018%RTägR5H<|{WOÏªÄ&elÉÂ= :8s\b\x0018\x0002«WKZ9¥d^x\x0017ú´ÒÏòû,ñ5\x001dë»\x0002+¯]ø¡¹Ê\x001e\x000fÓõ«EV)!±fMæªr	Jy(îÄ\x0013\x0019-\x0002Rsr`U\x0012±,bä0ô®ö\x000b:¥´\x0013Îã 
Qs|QÂm1ìÄ\x0013\x0019¸\x0017\x0012Å:BÎ´ò3H\x000c\x0017Ü\x0003ÚôÕÂ|xEëÈªÊ\x001eG}bã[59Gæ\x0003ê÷l aø¼k\x000bzÙ°pü³\x000eZöÜ\x0002ç³r0Ý°rã¬{ Ã.4JÙÕ¹Eÿ¬Í,:v[6Ñ\x0006Ú¼\x001cp-_Y)Gù¼\x0017\x001dÈ°\x000b
\x000bä¹¢\x0006]º
ÃÞfB\x0003k$VTõ\x0013\x0015&l[j¡§W\x001dÎÜk¦B\x0003k¤\x001aJÜU\x0001R\x0008ÙÛTÿ\x0006ÞH;ñvªÿ";«VôØ,WûÐ\x0001qD\x0012vpâ9OYÆö\x0015µUyïY³ò\x0007´\x0007¯@ª\x0013ÒA×xVgë©À5+?a¿H£\x000bÆä	ïób¯\x001eö6:\x0013\x0019\x0016µ¯¼ô\x0014±/kñ¨\x0003újU{páÚ\x0007½¯\x0006ÌÛÜùUí#Ý»àÓ²Ë»üî;Ðù+CÞ5u>\x000cåéÚj^`\x0002S§ô6q>Ï%]D\x0013\x0014Ömÿ8±¬LÕcvÛÜè\x0001}æFÛ%MåúìØgÔÇìÔ {\x001aiÍ2NèsÔòÑà8M¾ò­\x0015,?\x0001Bì3½f\x0019\x000fè\x0008=r!ÒèXñ¤-áª\x000f=»Í2NhhesÏSeÄ\x0018îïé5Í8¡¡é,Tº\x0014]ê4±\x0013:pDÌ\x0002úlê·9¡f/\x001aüÚp\x0017òÙ÷\x000fß|z¹\x0017õ¬-!¥Kln£-Â¥\x001e+æ[uZàÛg¼£Û\x0004ñ;zðÃqªêí¶²\x0011°Uw\x000fé\x000cæ\x000b´ÿD-êµ-ÈVÈiË<ÈO·´\x001ceÌ¬f¦¼1¯Ýaya	\x0014B\x0015³Þ\x001bM°\x000cÛ\x0017ú\x0004D½'½Xê;gòÊaÓÄmÛæD>\x001f3ûu÷êÝ\x0011Ï&0\x0014\x0000Ú-:GmÈÌ\x001côn7ËkO[ÖOÿP©3LTÞI~­½/\x0014_Øog\x0013¹ÒÑ|ºÙ©1+þtÏä®Y\x0003\x001a²
ÑPãm¦·´4ý\x0018ôÆo>ë§î\x0017zmZÏq=üþãñ/Ï\x001f¾øÙû§O÷Ê&J;\x0010Æ:­Ç1.þ@ãwi)¼Ù)Øòã­ëYéIxqK\x0013Å«+\x0014~ÚE6îOÁ\x000c­ëÒ ÍR\x0014ÔË;ÓP¢¼B>ïû\x00143Ê#Ë\x0017E)Þ²Ôõ£î|\x000cÍë) ,7íÛrd¶}x\x00139Â\x0013öá4N%dV0´\x0017½ë\x0007.ô®K\x000f{MU²¨½Xô%lÙ·\x00138ÓQÓÀUîã×²èf+>q¡u]|#\x0003|¼Dúc
W-8ïöéÏ\x0003\x001az×E6\x0014ç"¨Þé¶\x000cþÐÈ¬^-fëhÔþ\x0014g6Jxî\x000f3íØtôö7\x001eSß<¾|÷ôþýóo\x001fÿÏ?Üç\x0012¯\x001en¡ª·c*Æ\x0010PZº\x000e·:¥\WLÿñ^\x001føjÃ>Eécâü_,ºîS¯\x000e¯m%\x0007¬\x0007X\x000eÔJ \x001b¤6ªcl4ô®=G\x0007òi(\x0014%§)ªG\x0006j¬ª¥$Ú®\x001d¼ö\x0005\x001dÈ\x0019Æ\x000ca·\x0019hñ ÷4H[ê¦S¥s\x001dþô¯í[tl8Oï\x001f~ñòüøáNÑí\x0006È[w>®Ò;ôB1½àòf
æ9|ÚK,]+TeI!*Sp¯\x001eÉÉlð|^?âïà²<ñ-(\x000ch~~wÎëÊ§:Ïk"WGZÅ^ºÑ¨`9öäÌÊ9!7ã
Z`·k´Sbd\x001e~ØÊ\x0013÷¼'²DÝ¬l)\x0015¡ÄSÂ0(YY8\x00072¤f,õä\x0001Ï°Gbe4\x000e\Nia	Së´]Câ­0t%6\x001d\x001a\x00074$Oj!WjÇÜÀöù@öp¸_\x0019Z\x00072äN²#©i\x001bÙQ[[=\x0006¿7§Èçbnÿ =\x001b<»5ù îÌpõVò×\x0001
Y\x0019\x0011\x0016\x0004hk¹bØ\x0016\x0019¿HüÞ?c"Ã>ië7\x0017hF¶I-çÑ¡qµQ,¨\x0001µâñíGTy/¬	>ºóE¯Ã\x000cY;qBË=\x0015\x0003J-¡ã¶u C\x0015K\x001c\x0000¥fe¤¤ºr}_\x001e\x001bsÃ\x0003\x001a\x001e\x001e¢|faYI\x0018)Í¬àÌÞ?cBC°<\x001d£&R2£EñÚé¬ì
4&4<=D=-ÎÁçå¾ã·ð°*¹Ú/PÊèÕÓGdA.e\x0013nþ«íâàí\x001c\x0006#òÊöüª:ë°oÐðJ\x0008E½#WP\x0015OJ0\x0017Î\x00074<\x0014Ä}
³h4Q|\x000bïUÚ!]ô\x001cÐç¸	-yëYï\x0013º°Ôa0°·é\x0002\x0019ÐPoï\x0006\x000f(,w\x001e5ó\x0002Â¡`vÜ®¹\x001f)aò(Úß\x0016JQ_3p\x000bRðÇ¯Ü´9ç'7íKg}KMw:ç»³!Åýv*Ò\x0004ìÔ\x0005\û-¹ê¸Þ\x000eÂÖ\x000e
.4Çäç° mO~~om\x0014çe©Æ1QjU+\x0014«îË|Õ~Ò\x0018¿dl\x0001N¨½ÿ88Â«ñ9=¿ûÚéqåjòÛÚ9'¿=ñ\x0004kW)F\x0012.ë\x0010ÓlÄa\x0007\x0011\x001bsyz\x0017ýÓ\x001e$¡
|» ÝHGZ¢M&+ú}o÷:®¡|Ö$fUÉ°Â'8G]<\x0013Êje2\x0013ÜV}r\x0002\x000c+G
\x0018*×\x0016î±ä¢\x000f\x0017ÖåY\x00152l&"¶OÈh3¡'ï7&ÁY\x00152lÛ?$Õ]Ø\x0019¼\x0019UGpV\x000e\x000csÁèÆ±Ep{¹×íÓìÀM?ÁE\x0007DÃv÷2\x0007[\x000fØm¦`\x0002¤Ý0âd¹ÀeX£EPnû4;ËO^ß&¯î°íËì\x0000\x0006­¤£ê6\x0015í\x0007çhÂ\x000c\x0011{VE\x000c\x000b±¦=î8\x001c1{dwñ2;p-
\x0019C¬SÝD"ÔË1Z¯v\x001fð"Û10ÕëQSMÎ
ù{æG6\x00016su²?_êI¯{æ't} Â,+ÎRµÜUï®üÛ³ª\x0014µ!£×\x0011\x0003­øÚ¨ÃèB¿Ú@´±@NÔ(+\x0016_YñTlj.:ç\x000fäL_\x0010®[\x000f2-më¿à`cmÞ|\x0007t¥©=(ôKRh¥ð¨{÷ÃÎv>óËL$åðu-ÝD|.gÚ\x0016÷«u\x0007D@{(\x0002!2M5wÏ·A
×a\x001cÊªÜ÷Óï\x001e¿{~¼W¥Ï\x0015ÊM´ãAÔóñp[±Vÿ	ôh>K ºM®òyÖ\x000bö.EÑT\x0007kÜ\x0008f©òyC\x0017y»\x000b2½\x0017ÈúØµ	Û\x0016ù&°g`Ð6£\x001aÑ¸à3;nÅ6'2<´]ddCV\x001b^ôÝ\x0018¹'¦ÖCÊ,E>H
\x0018Ñ.§HacÚÖø&,Ôø\@\x001d9ûèIàç©\x0018´íõ2KÏsµ0Ï_	ÙÛùÔsRk`*#7P\x0013Y"ÉK\x0019Ó^bÇ(ý|)î`rÇøB£ävxÌ¶¤}`ú¡Ë\x000cÞñºÈ<æ£ÕîjÿYÜ\x0011¯öhä\x0015ÇÞ¨]\x0011}\x0013!¥*)ÙöL¸Ô!2AtÕ!sµý,n¿õ{õxÜ\x0008\x0007n Ïwf/:´UçEUÐ\x0017Yá\x0003\x001av_\x0018;nBgK
:«#\x001aºe\x001f"\x001cÐ°\x0003Û+üäúvhÊe»ÌQ^\x0019}5W;Ðb\x0002
óï±ó%Ouàù8t®ö =Ø^\x0012ç¡\x001fkà\x0016i±cä!\x0018uµ\x0007!áB\x0000ªo¬.1\x0015Ü\x0015kÊØd\x00074f\x0003Þ'Qø¹T\x0002\x0013,{Ãæ	
°\x001b'\x0005#Z¨Ú+¢®4!¹öètq> a#â7l\x0018£Ú\x0010ä³1tÜL\x00072ìCq=:§ºd¶ú\x0012O9Ú9õãnp> \x0003}Å³Å5\x0016Q]¦1óq7\x0004ZÖþ	»¥d«©#N
y\x0012>aE
W,-æ\x001c¹çø1Ç\x0012×ø1zÅýíÓ§¿>=üâÓ_Zpöðëç?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=fb>ÛóY)Ñ­'\x001a®þ\x0000°­=ÌæÀ$¾\x0007ôbÀH'yþ	ø\x00124

ÇNûÕ*NKâPjôÇÇ_f\x0010!\x0005ªÈÃØ¬g	\\x0007üìsÈ\x001f/¯Þ\x001eÍnÆi©Q\x001cÞó`±µÛ`i I
\x001añ}u6¾\x0014Ìô`F\x0004Æ\x0005é\x0006Â@MÛ9&3¤\¶ç²".ÇÕ\x00038iÇ1\x0017´¢1µ	Ìõ`N\x0004¦¹\x001d\x000bC\x001cJ_Ú^¨\x0001fþ~)ïÁ¼Ôbt\x0007Ô\x0005²Å¸n,ØMK,ô`A\x0004¦X*ËG\x001aak#-ýù¥\±ç\x0012®\x0010)µ\x0016µ,1s±è°Ô¾+õ\IÄå¹<\x0005ì\x0018O`<²9ÍTÃ.çêjâXk´\x0000,ÔX¹ÜÝÁHÅ\x0000/ï³¯KÁF¯/rû¡=\x001cá\x0004\x0003^úÊ7ga6
n\x001fD~\x001fó\x001dd³\x001c\x0013·|G+NI¾åàÅ@äÆB{!qJu&coáæ$)
Þ\x0002Dî"\x000c\x0016_Ñ"k¯\x0012ÉÅMrØ Ý&´ÒDÛ¦rª%Î<N,'ÓÃò×ÒåÏål¡êUm)½eé!¶Ð¢à"ß[=Mjúõ£óêw³ÁöR°aõkÑê7-
=ZäÊPJk\x0013Ã&ßï»WðrßHË&9à4÷SÔR\x0008[v2}/u
\x0017ñ\x0017\x0018ÛîZk\x001d\x0016Ð×\x0018gÀ¥9Mçñ@»Éí\x000e®å~ýÚä6\x001eoî¹=¹zxúåès£^±bh\x0013oÉ(~!Kû;ââ¢Io\¾{vruyýöHã\x000bãÚ\x001e×®ÃÕU/\x0007ìY"+råh|úÞ!ÅUqb]\x0015Ýxùöí
¸ÄA^©Ýµ¯\x001dþö÷ûøñøªtÓ\x000b\x001b/0ÏåÒrÉlàÚöö\x000cl\x0002ó=\x0017YP¯vu©üþØÌô¡(n\x0019î=+s\x001aÌ6±%¯ðl2mÂs~ù\x0019¶iFÙ©âÊ¯Ø­v¬Ù\x001cõ¸©Ë$~Ý6gxÙèÂ!7\x0017Ø¬v$¤¦\x0019\x001ae§+\x000b\x0000!rý)\x0007o\x0015\x0019â\x000c\x0019«&Öàù\x001eÏñ,·v\x0018|'`>hâ¶0ÿ\x0014(\x0000=`\x0014\x0003ê&©ã-\x00159æ\x000fÜsôAÍ¥Ý\x001dÇÖ;\x00100Mª·8âü±Öî\x0017\x000fiÖ<O8MR^õêÿç¿ÿ³ïùÔ8¶}QuÖ\x001fðë¸
üb\x0015û»÷äâäìS>)'Ó=åOK¡¶µ/p\x0019H´q\x0013éÉ,\x0007|Ô%zÝ@EÐ$,â\\x0012b9íÑ¬\x000cM[n«3©uðäÛ>O?¯4·\x0014Í÷h^Hß\x001f[=¸Q&ÇQÜ;Ûñ·\x001c-öhQøA\x0013{\x0011\x0006l5ìæp´â\x0006´Ô£%\x0019Zbe
lYç
MH¶åzguñ\x0016u¾Í«A°o	å÷m
9Ô±\x000e¨Iùñ°Éjý½Ç÷÷ßÔ4:\x0000Ã\x0001hBÿa®óõy:v0ÙHî\x0016Nóû¶\x0015\x0004¶Û[\x0013]-&î\x000ejûðJ\×^DâÊ¼Ö¹&Or«x§G\x001aø¾¼úâæo\x000fwÇ[Nç'\x0008T\x0001®Çmà¢ ¼gò×ï§ËócÏÓó\x000c|_eý,\x0016æÓ\x001d¿%qÓIZ7¬ÜÝr,Óc\x0019µrÌ	tÀÙá\x0010<ûä4ë\e{,+°\x0016¸\x0015ÐÃöhCþq\x0003ë±ÀZ¥-ê§Ö·`Û-(^Jå{*¿*Æ\x001c'ñ¦Ì!p­àÉÓ7©·¦ÝåX¡Ç
Ë±R4Ü~\x0015'ôzc°\x0019k¶w)Vê±\x0000\x000bëÔYrÎ¸\x0005ªäö~I=¥í´øÒ\x0016·õáëÍÛ7w÷ßOþôôõîöþØe&\x0013°¶\x0005&!~D[]ft®\x001f.Nß|<=ÿéäO×\x0017çgï§Ó=Ò¦m¯\x0005-X\x0019KÅÖ\x0000\x001eÐ\x0001#÷;¢6\x0010ÝÛ l\x0005´= \x0015\x0003ÊRsk\x0000]\x000fè¤'d£øYÓ\x0005ÛRaó\x001aô= \x0017[\x0010¸\x000eßìö(\x0013Ôöz+`ì\x0001£\x0014P¦nèý+úÂ¡ùb
[`×UAé\x0008!`\x001b5Õ\x0015\x001cö\x001c\x000ccþ\x001aÀÁËØÍ D\x0017´sÃzNµscë\x0017a\x0013x\x0017k1\x0013n\x00122¡WíÉ"lþÆÃ&\x0001ñ.\x0001Û"\x0002­¨&Ñ$¸ªjó'\x001eö\x00087J|ÎeªöÆÈGptc"`\x0005 \x001e6\x0016o\x000c¨\x0018Ðriic·\x0010¦ei\x0010»H!0ïn\x001ek°¡ÞNâèãP«iÙ±ÌªÒå æÝéÕQý5\x0016¦AìÂEh\x0016Z«$v,ÓÊÛ
®rffo\x0008ÐLfDhÉÓhNÌìpÏò­/èðEf{4+³Zh£PK%Íx?d³m"s=av}\x001d>m7	\x0019ö$>Îl\x0004\x0001ïÑ¼ÈhÎ xpÍ\'*cÏ±Jë¤¶f&\x0012 \x001e-ÈnóG²ó,	ÔÊÃ\x0003\x0016Å,Ê\x00169\x0007ó\x001d9§\x000e±#¦m®#õhIæÕl{	Ë?²ôÔîsMÛs\x00176AìÃ¦Ehu´\x001c?Òñ<\x0019Ït>(gì0\x0008±	
àôIÔ|ØGû\x000cÞ
ÇÔëüÒ«usò\x0013ªã\x001eO\x0015&ÅMïÙ¸)\x000b×~ÒWtzò\x0013
ã\x001eË\x000e6*ÝSéåTùïÓ¬N\x000cÓ
Rðó94\x001bLÏd$L
9\x0013ª/	Jt|ö&°\x0001ËöXVð\x0001!¶\x000f¸ÓOZ®¼ÌQ¹ÊI\x0015¨.Ù)ã*x
0¼¨l
±|å\x0005Ær°tù?%"¢{70\x0019\x0002+Ã
=VXµzÜ¶îp$\x001el&nõòØð³\x0001+öXQb-ômS+Æô)aé\x000cÔZ]÷Q±×Ír¡d\x001e\x0019Ìñ>\ÿl°I½ÔEdf1\x0019z\x0006CCE³ý,?Ô\x0007K*kÞ¨ÉPÑ\x0005dé/ÿyÿ\x001f\x000fßú¹\x0017·'\x001fò\x0008tJ\x0008òýöæ)ÿ§\x0007\x0005Pd!\x001fr¬jÿ¯lù\x001f«\x000b=¤6!èÓÙéõ\x001fòßÿ\x000fÿ×ïÿþýæ¦ÿûýàó×7ù\x001f¾-bÅ³89ZÁé|å{%_.\x0019\x0007§ã/àÌÜ\x001e§{þúôêòýû³jÅ\x0003ÝdÈøRºú¥
^(á
âyà
9
/78¾\x0018cl½ù+xÒ}Ùzþe¬7\x0019>¾\x0018/ïÀòq½Êç6\x0010\x001dåúi½1kè¾þõïÿ1¬üo'W\x000fßîn\x001f\x000f"Ùâ\x001fbIaÓ$êCâòWææùÔÂÑòÿxruùñüìj\x0011\x0008-²e ê<\x001cê¡jM |à`ùz\x0010ZNË@\x000c¢( X,\x0016	$2ë9hÝ,ã\x0008¤)çòùA[MçuCÁ]²Ü}½\x0006&Õ/\x0003
Ä*ì*\x0008EsÉ©°Ó/ã`1ÇÌN²bÐ\x0010êÌá7|\x0018\x001aH¿Cóð$çQ?TÀ}òzÃJ¥!ô@òQ\x0018ÄÑY¡UÔl\x0011Ï-mk@hòü"üçRh ´RÛq¸Õ\x001cmØü"ü=tãÈ\x001fAóNÛ\x000cÒæË/û4ºaòZ5¯<}@\x0019¼XÍúÅÚfÊ/#\x0001*\x0018v(4ÈÁ³6·GT!É¿«¿ÝÿÛ¯s1Î»ûï\x000f_ïî\x000fâ\x0005óJÕ¨\x000fòº\x001c(\x0013D
7\x000e§(Í\x001cï.ßº¼8?\x001e&Í\x0002¦0¥L¸·Ë~Æi¿ÔéhÛ\x0010ËõLpf\x0001\x0013&51Ñ¶\x0005Êb)meÄ0Ï3åX\x000b R­.L[B­q~+\x0014K\x0012¨VNòw4)ªË¡^Ç\x0014Ãßb8\x0014*¿ùõæñçû#±^þ5¥L]¶\x0010\x0012 È7\x0007\x001dà` üæÇÓ«\x001f.ß\x001fÙ;¶@ôy6lÒ¦X+af·ø\x0004ipzvuIáèp\x0017Â©"(Ud(]î\x0008\x0017wpÉ¼\x0008\x001c\x001d´2¸|
P]­/\x0001kYnÙ*¾`D½þ³þÝÝÛ½;þÿþ?N\x001fÎ×êï]}Êû³Vq;SÏ¾üOr¸è£õb\x0017'*ß«O\x000f	±
\Ó­°K{|8«\Ù~ÕiC#[¼ó×\x001e\x0011ÙôÂ¸,FäN\x001c¾¦y_£@ê1¾Mò\x0013©ðkú|;'\x001f¾>\x001cd1!ß¢_Aõø\x001eÊüy
a\x000cÕyæKQ&"..?ýáËÍÏ7ß¾?\x001e\x0005(-\x0019¢\x0008ìüÿÄqÈ\x0010¿üòî~Ù»~ùõöHÐã4Ê ;GÁ\x0004MeÈ«g?|zóãÁî«\x0001£¿\x000b\x001eÇ\x0008*R`à ¯a]#ýÄS\x001d¼f?v*\x00187_nÿ:eøò\x001fÎOnè'\x001fnþ×èÃÁ\x0003\x000ec#ÖÚs\x0011¥"JNC\x0001>äcd<t1?y²Ë÷\x0004Qþ÷>\x0001_Í\x0010ä¨ºö\x0010¢>V¤\x0015\x0002 \x0003hÖ\x0010ð]x	AP\x00145º\x0002&,
A \x001bF\x0000\x0005z
Ânk.Bº\x0016\x0012\x0014!§à91\x0007°às>ãº·¨ô×ù\x0017¸ 0qzóË-=¾IuSmÝ£.¡r2îQËí\x001d¾ÌmÞÑ ÈéÛ³çöjãÒ=\x0016p¡,`}^ÇÚúú¡lö§º\x00066\x001eÌH\x000c\x0006¸´<pP-ã\x001c«ÅÞ\x0004f{0+\x0000Ã¹ÛõK\x0006_*íËi~þÉîÏmáò=\x0018Ì'¾\x0004UªKÁP=¹iH[ÀB\x000f\x0016\x0004`£|Kk_¿r>9>³ÝÄ\x0015{®(1QmRjZ÷¤á\x0015¶íÉÔ%Á\x0003N[}EöR}EÓÖZÅEe\x0008ìÃÄbÊP\x0010NX­X12V°°\x0006\x0017\x0006\x0012\x001f\x0006&SX\x001c¢\7$NÓ%.7Døb®ÁÄ)¯i\rÑX\x0004d\x0001%2å7
.\x000c$>\x000cônKbg\x001aq!}Þ[V>Éø0\x000cë2ié×)\x000c\x00087\x0004	¤à¶xW\x0018¼+HÜ+¦ºÂ¼)#^xÉXË?ïÊ¤·
î\x0015\x0004þ\x0015¤ô\x001ejQa(U2\x001e\x000eávãH×
þ\x0015$\x000eVyGú6Ç¡ø]×äU\x0006~ÉôàÈ´Ä)ci,£Å01V_\x0006>XÞ[V\x001e£1+Ã×½@`¶T\x00160Míyå-\x001fSÙ&Ó"\x001füÅòà\x0007øjæ5`TV
ç,¥=xØÄ\x0017¦|AÆ\x0007.bv¬86\x0015°É±\x001c\x0006+	«¾¬rvÿQ
«än¿ß}¿=ÁÖ¯×_oîk¡ÜË)è@õ\x0013\x001e³RØ×\x001cÑ|¬÷Ð³OçÎN°ûëõÅéûÃ¥r\x001dîñ´\x000cOç³ÓQþÓBÝ­¥®"\x0012V[ñlgÖC\x0011\x000b®\x0014H\x0002Í·*Ï\x000ccÞx
ïñ¼\x0010/RcfÞ¢
íXè\x0002µ\x001a\x0006í¼ÙH\x0017{º(¤ó\x0006u¸L=V3S¢\x001d3z+ðvQeÙ\x0019JÈÃõhkäm«èãjà¡ìF¼agpk\x0000«tºtÞWJnØ\x000c:ù;\x0003\x0001Â­¡ò«m9³¨\x0014Vø¸)>»Å°qñÁ°5@¸70\x000e¨u\x0000\x001fOS·H0Qo]}Ãæ\x0000áîPÆPRÙC¾9\x0007CÏò´ú\x000f+=KS¨æc£(TwRg_\x001e¾\x001eËgb.µUrxLg}á9JÎõh,luöæòâHju¢<öÇÃÂ>\G\x00157Jq¥K¾rqý\x0000\x000cEeR,Óc¥X&{¶Àu\x001eùKç»¦³#á¡ZÊd{&+0byqçó¥ËWÏk\x0014gep®Ó\x0006,×c9©ÀÑøc\x0017ªÙµl-í9?\x001bÇ')ï±¼`½\x0007G	\x0006çQF¢,ö]uLØ²ªBÏ\x0014*ZûÒÈ9¸TÕR_ ço¶\x0018*öPQ`(¯ª²Áj©A\x000eß4\x0017xÅ!Ó'dj'yuVê÷\x00015¬(X¼¤òJÏª\x0003c>\]èª\x0014³[°\x001bÜ\x0002\x000cß\x000f\x0016À¼ªðE¢m\x001d±¡§,+ÖÅ×	»ËL\x000f\x001cÓk×¼yøí·ÛÇ/GÎÂüñ¸2\x000c»C½\x0005\x0004O¬Ç
º)×õÉËwïÎ®Þ\x001c;	ÍôÈ1½zÍ\x0002°6Á*»Oµ\x000b£ñwXM²·\x000f%\¦ç2\x0012.Óª>µ-ÚD\x0005Ls^È¥=ÿ.ár=\x0013p\x0015³j/ã±P¿p9È`yCnú¾\x0007ó\x0012iÝV÷\x001cm\x0005\x0000\x0006\x0003p[ÀB\x000f\x0016D\x0016³ÔcçP&<s±Y,m\x0002=Xá$\x0004ME\x000f­×{~<ôFï\x001d\x0012°Ô%\x0001Á\x0003\x0015¬La®Áãl;\x001c\x0005`ÝIdé\x000bLòMD\x001dm5Bun>À~,!!\x001bý«ÄÁb§p­Ê6\x000bøbWmÆ±s0jÏñwd³u

kð® q¯Vy®:5I×hò¼+v>åà_Aâ`I\x0014\x0014É,?\x001ff2®fðm<ì:0;YÉT\x0015öÇÊ¶Ä\x001c?P\x0007£·x~\x0018<?H\¿Á¹ñu¡h³â%FCp<ÖQm!\x001b\?H|¿Á±A@deäF!3ü"\x0016¬Ùô1\x0007ß\x000f\x0012ço¨¥\x0013e$M]bÖ+Þ>nÂ\x001a<?H\?zXE\x0006ÓÏ<\x0013\x000fëô&²ÁõÈ÷ÛvZZ\x000fµQ1Y\x000c{ñ¾L\x000f¾_K|¿Á±mµúÉ¢28ù\x000bÓ>fÚâúõàúµÄõë\x0014yõ\x001b5ò±<ÑÈã;Ê\x0016²1¶xwj\x0006Ñ¡&\x0013m\x0000§\x001cËýl\x0004lpþZâüu Ñ Î9ËO&&q\x000f\x0019\x000c»\x0001lpþZâü£µjÜcSb7ÂØZ\x000f\x000eV\x001c¬kÁ5\x0019«×J\x0012àd0Ð[\¿\x001e<\x0016y2\x001b¹mÞ¦¸ó\x0017É4l9.Íà/È_hK3\x001c\x000e\x001a£Ef\x001dWtE»Å_aW\x001aÉ®Ä`¿h9¼ýRö×òüÉ¼úí©b÷ØJ69eÑMNyÚ\x001aåoª£õå\x0019¼6ð¸U½]Êo\x0004h`iÊ(¾\x0011ÖwôLÙj¨\B 45\x001d$í&Ç§ó{Çç*kü$ÿc\x0006íâßo~>êm¡µ\x0005ê2³¾¸Û\x0018¸ÖÌÝç>~:ýa\x0001îôr¤HkÌ£d\x0016\x001f\x0000öIsîl!íìb äySz\x001bkïF5ôÙ¦V\x0019ëÜb¢ü©¨$/&LÕ{ª
`õz$ß#ùÅH8\x001dÊ¿m^HÕH. !_Ïg\ê3Dzú6èÛV\x0011ñw7wwÇv]^C±Û|\x0006±\x0018\x0002Û}4MJEE:üÝéùÕù\x0002:ÓÓ\x0019!ÑJÄA\x0014Ux~*j|\Açz:'µáÞ
\x001b\x0014ÕÓkkU\x000bz\x0006©5x¡Ç\x000bR¼|XíZ5¾\x0019opøkèROdt\x0018ú×Q\x0000\x000eg(hZyº¹ûä6~[\x0018÷pcä£\x0011\x0005²êÇMÅ6ÑòÕDY³oX{ \|\x001aKíiçÆf?\x0013i\WkÍÆÏ\x000bÃâ\x0003áêC)@z¸t éT0\x001f¿Pêv#Þ°ú@ºü£ê$\x0007\x0011Ðê)Ê{£)V­w{}<T]\x001fþBæý<U\x0016ïWtv5±¹¿K\x0010«\x000bG\x000fóYèb\wzPµ,VO­þ9ìBÞ
xó{\x0001TÓÃWÕ¸òáé{àþ^'£\Þ}C¨\x0003 ù¼ÅË|Y9s­Á×OKCÇ"ÀÐttuyý©ðÈ?Â\x0019)ç\x001fñÿö,±îõjâ 
=§ùPk`\x0014P¤nÝÌ î²	ÙöÈv5²Q7à+\x001b\x0015x\x0000¯Ä\x0012±¾\x0010¯ïyýj^íÆ\x0005\x000bÃÐ/ð\x0012¬_lUt\x001b­¬uÔ8\x001dÁq9\x0018àâ6å¨ó\x0015¿9êÏ#õç-Ë¹\x0016zì\x0010­oy9S¬\x0019³+	/Gýe¤þ²:µ\x0002'ZmÄZfxéÙ
­¦\x0005\x0014ª\x0016P¼ùõö·»{¼ú¼~¸ûvòÃÝí1÷éZð¨µ«=Ù½%.È´c=ë\x001fÏÞ¿Ç+ÐëwòÃùÙõá.q5-¤PµB\x0004\x00185MXv)\x0007¦õé
¢
\|2\x0014ÉÏá=k?ÛãY)\x0002\x0008ñÊÀ\x0014ùBHMwM­®\x0007tB@­Ây9\x0018««R\x0014\x0006<u·\x0002ú\x001eÐ\x000b\x0001C°­× ZÊ@°kZ\x0007Wº/ö|QÊ]e\x000c\x0001[40ªû¡4»Õ¸ù\x0003§/	ùòU&.{þ4MP¬´~àè¶\x0002îª\x001b\x0014U7\x0008óiC¹:\x0007g%\x0004g\x0002\x0013ª!W·ptR/CXÞÅX\x0014ªòJ -àÇtÆ*ÀÁ	Ô\x000b:ù1dÂø;¹q.[0m¶àà\x0006Aê\x00071³ÈÊ\x001eQ$\x001d	ç¶:i\x0018\\x000cH}\x000c8Ï!±Ñ¥uRk;p>nþÀa \x000c2Â2\x0000¬V9{\x000cE*\x0000WöûQÿj\x0015áà\x0006Aê\x0007±\x001f÷¨\üL²¼\x0006ÃfB=ø\x0019-õ3*o\x0012MÐaD\x0001tme½«\x0000\x00077£n&Æ|¾U\x000bZ_t/\x0011Ð%nm
Êl]zµ¤n&ß\x0005Ú*´E\x0011³ý K[÷±\x001e¼z¼B¨²Öç\Uð,âG!×U§ÑBO\x0013QnÚÑ6¶U¨!\x0003\x001am_l\x001ba\x0018á&Éh\x001aùé±¨&Øw¤ë\x001f|ð	Eh0GV9L­\x001fÙâ\x0008Õ*ÈÏ=¶a\x001aR.«\x0008ehË0f§GÞ½­ÙÞB¨¸K,¨ÍA¿\x0019¡.Ãè\x0003½Ùz\x001b\x0003uÈªrÌUB­¶ne3\x001c'FxÄ\x0008\x001dòÚ3õQ9\x0014¤#9¸ÍÎÐ\x000eëÐJ×aðüîí3LmÇ@dZÉ«­\x001bÅWOé2Ì'Û+â3\x000fdH¼
Kx³5jíå\x0014¹âodÁkäëfUw§Ú\x0012\x0006eU÷'øË÷ÛÇ1\x000b¿\x0010B\x0002wVb,[÷4Xz,\x000f6ÕÚM3Òn:\x0004ûÝÍÝ·û6RúÀ\x0007·ªòRLÔÝ¯ßÐ!ýU¾\x001b(ýîôüãåû£Ó¤;NÝsê\x00159´æ±\x0007y	q$ï(Üì\x001eÔ¬1¨áÑuErAUëÔC)ùjPÛÚ5 ù\x0002ÓiÖ:i,rkÚ .¼\x0004¨ëAÝ\x001aPÅ¯ÇE9¢4eaµ!)há§\x0011Pßú5 ºä+(µfÐÄi\x0013{	ÐÐ\x0015 \x001aå×9ÃH56:ï\x001fÓÃcãjÐØÆ\x0015 Æ\x001aÛÊ´¡jÑ\x0018
gB_s*^T­²¨"e\x0018¯êë^µ(°E}O\x000f\x001f5\x0014p,A}«O´)mÊç>;|ïÒK|{\x0018ÞÄËé¿oª û\x0003ÊÓ\x0001eSh\x0007Ô&Ëæ¯?yòáÉ£¾ÍÞ¹»½ßM7?$`\x0014=Ý,\x0001Éâ´$6÷Í\x001dùø4súþÍùÙûãsÎ;\Ýãêµ¸9\x001c
¤h]\x0002érj®9(·ôM´fj\\x0003÷¤\x000f_oò¿fä³£O_9'Ý\x0008ÕÉ³;eM×üßd6úpqÿõäè£\x0017C\x001eÒ¬Ô\åc;~WJª²q;¤ë!Ý\x001aÈ¦ó\x001eP\x0017\x001e\x0011
K=tÍ01¬b¬\x0015¦3Z\x0019º1:Ù_Bÿà$lÖcØütòÇ§Çÿú(®þô÷CV¡r,Iq;¸ÕÀ·\x0016Ë8Jõ5·t}òÇËë«SW¿þóó¤º'ÕkH±¡ÑµÎ\x0003ïq­,&o÷ÙèI
j{P»Ê¤ÆRG¡«o'\x00054µ>\x0004;{ÖK9}Ïé×p:ÓDMPjªñò\x0011ÏÕx>Í^E\x0016¦é"MS§¹Hþ9QUtà«§Àïcà\x000fù"~\x0016O÷xZgùÑE,\x001b!ujF·ÏÇ-Ç3=\x0011â%;º8É¼{jÓ­Ò\x0015¹T:tÜ,Æ³=\x0015âáÃ\x000e	+nsR4k¬Xç{</ý¸MÆ&`@½Xe¥?åÂÖ\x001b{¼(Ãó\x001f$
óé8ó+-\x000f<|.ÀV§h3Év|Ë1ÙÓã±\x0011H(ä\x00149ØAµtOqkÔ|Ï |ÌñØõÕÑYH
Ñôf
"µ\x0000b¨SdDÇ\x001bÄù+y8ßË¯§\x00154ÚLÒ\x001bør`ËS¤°6¹VXäc¬5oXÐõNLh\x0015_k0\x000e3,ØÅ\x000e:\x001fOó×Å\x0016ô=\x0017óåëKb)*>ã\x0014Î\x001c&\x0003Î_\x0012%\x0006\x000c=`\x001bÐ¼\x0002úÄ\x0015^ yîÚMix_aÀØóEù\x0012tXÅ]-È=\x0005<\x0006#û ð,Ý!\x0003~VÞ\x000c\x0001ÂëüÉìÖ\x000f·'zøúõöØ8\x0019üÆZ\x0018-½è"2MZ4ãdÀÝt \x000fWg'º¼¸8;¦\x001aKºÇÔ+0u KµÓH\çxÅ¶½\x0019®©k1Miä8øF\x0017kÇ6
Üt9f¨×bÚ\x001eÓ®ÀÄ7d²¦×ÔoAqS¹Wãd®ÇtrL¯¹\x001c\x001a;ñ«Í\x0001bbcÎ\x000fÞ\x0013RúÒ¯ \x000f\x0015ÊZ¥du\x0013¨p1½Ä7\x000f=fXÙ"
m¡êB#&Ï"±H1AMüQþE?\x001eæÍÃÓ÷ûÃºÕùÂ³(\x0004)ÅÛX§IÙÓ0HC°nõËëO§ï\x0017é\x001eL\x000bÀ"ð(!¯\x0002÷ ç»?§t\x0003³\x0005Ìö`Vb±¼Ú(1\x000eJñc¼å,\x000e¦E·p¹Ë	¸òñKç(6N9°\x001cË\x0018î\x0007áÜ\x0013ù\x001eÌKÀ|à[\x001cT\_å\x000c\x000f£\x0008ø´½+ô\AÀ\x0010\x001d
´Î\x0017u^úz~JÀb°ØEÁl¢\x0000Õ«¤Ú\x001d8*þ~vàÉb°Ô%ÅpO·µØiP,¦øö«¨³\x0014¬\x001f\x0010c\x00011ÏÌp-B
ÐsÑ\x001ebs\x0016[¸\x0006'\x0006\x0012/æ\x0005½ÊÁ<=IçÁÌ\x0016g\x0001\x0013\x0003\x0017ÃNª=â±\x000cj\x0003I­%\x0018\x0005sÓ
\x0016s
N\x000c$^\x000ckÄ<Ï°sì]óí5\x0005p\x0017l \x001b¼\x0018HÜ\x0018¶\x000eæ`ªÑ{±óm\x0014jÜD6¸\x000bø\x000bâ*X¨ D#÷%\x000f´
[°ô°'µdOZT'²¼
¨¼S¹4;\x0007O\x000c6F\x0016Mi±&:äCË/,¿sÀ¨P*&\x001bv¥ìÊ"Hmù]Ç#åû,O´\x0005kÖ\x001cIxzO^ZóqÞ=¾`0oä¯Ô\x0011ýX=|¬£®°o\x000b\x0010cMÙWoçÒ=på?\x001f[Ñ\}aØºÒèør}V\x0001&×ü\x0000å³DØ?ßãé°\x0003:v\x001d¿ÛA®ââtáÀ\x0001BÒ=^\x0014C¤¼\©âª='1¤Vr4\x0014
K©LOe\x0004mæ<&\x000eéu¹MëÔv\x0010ÉRÙÊ.§Âe\x001bZ(
cÕ<Û¨6`¹\x001eË	R·t\x0002ùRSåùJª#\x001b°|å\x0005ÖòÊMÍQ:0qi­±vµB\x0015\x0004\x000b\x001e\x0002UTk9ÏPV|[Xq\x0003Sê)Gö¤bëÏ\x0016ø\x000búq(¸\x000c\x000bFw%ðWX`xLOl\ÞíJQÍ\x0006®aÁ`Å'\x001b[µÛõ]\x0007\x001e¢^´¦Ös
K\x000b\x0016¯-®Ë\x0015¶TÉ\x0010eÛ`
û\x0010Å\x0005W\x0017»Ñ¤\x0008\x0010H\x000b\x00064\x0007\x000fù3¯8xòa1Uö\x0014nàÐ_2Û÷ç^
ÚäOääT½åòï\x001ago3ã§ã/\x001bLizJ³2FÞ¡\x0001ÃéH¯/\x001fFYýµ®Çt+0£éÉ.`ùX"L®ÉV£dÅZÌÐcuj÷Xi4cúöX9_:.ÃL=fZ\x0019<ç5p¸ ix\x000eÆÜbMT¢Dßz¨süV¢Ü#Î×
Ã5tó<O<æ%9[Ùø±\x0004¹\x000b¸LÏesY¼q\x0017iÒÒ\x001bZ\x0005Ëz:j¶Çp9ëÑ\x0008ÍÒÜsT  \g\x001eMFÃ³[ÈBO\x0016$d>fÇ\x0018í¹Í'ßY6q¥+É¸sU!º61
X\x001b!GTsÅ#\x000bÐÂ´Î7LªªÞüzóxó\x001b\x0000ç\x0004Òá#Ï«n-£@ë3v\x0007CÞüxzõþô_3=ÁPÉåÁÁÖPÚ=\x0007t\x0007Z\x0016¹ÌÈ ß©êëÅa?4¡×D¯OyÝm\x000b=\Á\x0019ÕàðóÖ
èÄã\x0015Ý*63Xîµh¯\x001e¾ÝÝ\x001e,ÍÆÌåÊmÝ¢\x001aX9©!"\x0011Ñ«Ëù\x0014x\x001eÊ÷P~1Tvò¬+ìðì§Q8²¦BÍ¨ñ/E=R\¤}+Ægg*ßÌ4'_½i×\x0017R¾Z\x0008QÏòÆ®\x000e©QÖ_inÔR*=PéåTX´Å¦\x0002JíÊÊb¾­²\x0003]\x000c\x0015Û­óðrgìîqâzïR¨aÃÒu·v×»Qºô¸+SÙõ\x000f\x000eK:f^4g^pî$î\x0007ÏuÇ	üú\x000f¨µ®¯uliæ¡8BlÅo%9$S+ÖºÖ@«4*.¾~xúò_ÿû°_pÑñbÇó'Ò`²l#*y8 \x0000øúòúÂ¸\x0016?«4ê*>Çew#
TþQl<P\x0012Û[³yÇ¹n°ßª·×)þ¹ïwù\x0012òÛí})\x0016yÖªîÔqíªdvKlèñ¿¸ütï ïÎÞZg>jÔ=¤^\x0001©ybWg»)Ój\x0013ÇéV+!M\x000fiV@Z¬Ü-`w­\x0000P\x000f²"+!m\x000fiW@\x0006\\x0005\x0012\x000f\x0002gØÏ°¤ë!Ý
ÈÄmUå\x001d\x0008Òs-¯}\x0001CúÑË\x0019Q\x0010Ûç|ùkÕ\x000b01È\x0019­ãÁ@Þy\x001e
¡RÛÛÞ½ÀÇ=düB¦\x001e2ý>![ðY]¹úR\x0007Î\x0013Ç&\x001cÿái ¦\x001cbìÌÝ0Hk%åpâÀ#'£A¬e\x0019Ò\x0006¹ÞùKOsÛ\x0013ué7w÷??\x001eI¹ç[*	®:p\x001aFPgË;Ç:î\x0016S¼9ÿÃÕ±¤ûTD\x001a&"ÒÏaiåÂkZ½åÌf£ÝÄez.#á
m	¨zéÇÙ¢t4ÛÉ¼;)í±¬\x0004Ëk~\x0000ªoYìÕÆWÙ`V©ª¯ªúþtwûô÷ÿöîáéëÝÁÎ)\x001cCÐ.6;\x0017G\x0016g>\x0003º¯?]ÿùäÝåõÅùî)3í2Smß©Íñ±.ò³\x0005¤\x001eâ¼ÈÒôf\x0005e\x000e\x0014¨ðÓ:K¯ÚXÛ¦Î\x001dèÄ\x0016aÂøÍÅ\x001f\x001d_e\x000b¨pÈ\x0008å2òí>ºwv9õt>öS "ýÿõ&o#òÿ&|\x0017 ù1	¯1µ§ÔX..ùò \x0000pq÷Ðñ)\x0000~Ú:ç§\x0012AKQm»36½ïá\x0010ÚÖ;ß<.Fu=ª[\x001aÜBAutÈ¡\x0005\x0017i\x001dî1ëQC\x001aV¡&î"(ukTk=\x000b%ù\x0007´¥¨*N\x0012qrPÿzó·Ç/¿Þ\x001eyàðVñíUbï\x0014½åQî£\x0006ÜÎÉÿxúÓÕeÞ^Ç\x001aÃTåu³pîþëµ1\x001aon\x001e\x001fóÿÿðAdÇ®b*\x001es,
\x0005N³ªÿ8ÚîÃùY¤ñæô
×Îv
îüÃ®>ÑNElß,òîáþûÃ1Ï?£¡\x000e&\x000bÊ½Ú\x000eæ(btÙs%ï.ßºDWô,îÉ´,$\x001a\x0012§PÍ°Ä.ÝÙñ¹ONfz2#"Ë{#&"\x000b4àºh@3ÚF£Ù\x001eÍJÐ\x001cx*iÎ\x000b/P\x0002\x0011ËßØjÆÍ§/Gs=¡±7f__J\x0016éDÉAÐloÆ3dá/¿|yúöù¯´\x000bÆ!n(òË×»oesÚ
\x0015\x0010êóÍ=21ÁQì,ÎëÌLQëÓÍîÎÓ|}ú¾\x001br5\x0002ç\x001f\x000f9·)/,ó{cÊÍýÞòª\x000c¿\x000b¦Ï*ô
x\x0001¶ö\x001bïn®ª[µy\x000ePgúÊÀ$Ò@ô­à\x0003T\x000fÅ]Éï\x0008>Áó³\x001fªèÖÁæ\x000eT÷ Óà% &²\n\x000cÞ×Íà\x0001¨²"ÅÀ5êÛ@M\x000f:m
^\x0002ê
§DäBi-}o¥¹ír\x001b¤í!§-Á¬\x000fyúìE±Ã\x0016NÅp	+^\x0002Ôõ Ó¦à% Î²¾Z6§¯5Ñà¡RÌ"kwl\x0003õ=è´/xÑFÂX´ît|®p´BUXÌ>Ú\x0017ùô¡\x0007v\x0006/\x0001
QÑé\x001b±½¢Ô¾÷ÂQÔâz\x0014{Ðø;¶hêAÓ\x001a6¹|#1õr/tF}cøð\x0012 \x001ffg¯ÖúøÊCýöÚb#{ùötµË_¹·§ÒcÉ\x0007SÓ¯1`ÿ[ªn4Q\)Øõ0J°æX
8HñýÔ×oï\x0014\x001fKù`z	ÒÁãÃ\x001aïX¿S]¾áooæUê^Æ¦Ëu>^°_áU¨6Íÿ0\x0006ý\x0012\x000e
\x0006\x000fk|¾G·TÒ£Ñ§ôª$8\x001c,Ú²ð\x001b\x000fQ\x001aÞ×Ñ\x00156
JIbÊw\x001c[YM¨\|sõ[:)×\x000f­\¿ÔÜ|z|¸ÿ¥
VÌÇÉ8\x0001µÉª¶\x0010ä0Y·0ÙÆni³OWïß\x001e\x0014©èt¤#YGuf)/¹ÿºwÉ®ëHÒ5§	\x0004¿\x001f-BPÌ\x0005\x0002¼ ¨\x001d-HD\x0004\x0002
)ZÕ­!T·ZýAÌ¤FRfîf~|\x001fýpßû®«÷æ\x000e%3CñÉ»ÛÃÍ~Kz$\x0012Ë\x0007
1éÚ1neÒ5^Îä\x0004e<ÉåÑç2
­)PýL¦f2u²5ýs¬«Ür&TÇPÄ$³\x001a0¹\Ä0e?¯¡|Ã\x0017©ï=ê\x0010)üó8\x001e¡é
5ThX)\x001am\x000eL\x001a\x001b\x0013-;Jù\x0015L±f
\x000båéª\x0007(ÿ\x000c\x0005£ÒB\x0019É\x000b%ú¯¨âÙå[S,§RÊs£ö"WÊ\x0000\x0015\x0015Z\x0003UQî¡\x001aÞå
9\x0016í\x0004¢²Y\x000f@Ï;]Æ\x0015k5¸ÎeÃ}.5¥¸#^\x000f9\x0000k%ø\x0017\x0014,\x0011ØC5¸<eÃí)\x0002uTEm©´
¨TÖQ0¢§ËÁÝ)_*r[Rÿ\x001dz&$á)%cuú©\x0006·§\~}*p°\x001cÝ
à\x001fò.ùú;uÅZ
®O¹üþx´l*áx«³j\x0019PÙ.Ü/\x0005°7êåËÕÑ_ïî?'\x001eÑÒx$\x00010p©¬âÝîêå\x001a¾ýõübT?¿ÂS5Þ\x0007Ü\x0019<­³\x0002Ð 2Ð\x0005gNùtº¦{òf;GgIñÈ}É\x0017øZõA­Ä³5ÞwÚ\x0019<å)y\x0007«\x00179©ìCY¼°vñ|M÷äiv~ñr~)-^qñLY<Ù·WóìKÍóË/wßþãúêöèÅÕ/\x000f7ß\x001e®^Ü|:¶Ù)DÆRÞ\x0005ÇÖ\x0007ºL³ÓúòôüÝÑ\x001c\x001d½8~{ùúÝåÉÑ×ßMà½ºg_êAÐT
\x001b\x001d
Àå"7\x000cZ/f?¨®Au\x000f¨\x000cÇ*Ã\&½\x0012B8çÚ\x0002ÔÔ ¦\x0007TEÒg¨s+²Ë¤\x000c\x000cZ»\x0001ý ¶\x0006µ= ÚÑÓ2ìQÒ(\x0001P\x001ajÇ6YQWº®^=
 \x000eSô¡nr|
ê»N=bF§©-\x0011\x000f\x0013§\x0019ÜàÑ£\x001f4Ô ¡gE!*Ë©:XQ%*ø\x0015Õa\x000bÐXÆ.Ð4­>zÅ¡\x001a¾.1hÜ\x0002´ÄG¥2º\x0014.¥À÷åTY~Lp^Ù-H¦©Ç6¡F¯tAÑ|> umS0\x000elì2N^RîP\x0017('4·l|ô[\x000elì2NØ!M¤¤±4\x0008&-Ã`×\x000eì²N(LE\x0007
\x0002zCf4D&
8&r`dyI$>f±á\x001c%òz!·¸LåÀ<É.ûïÆ\x0004*³¢/ò]\x001aí\x0016fT\x000e¬ì1OZH^¨g\x001càò¹÷ÒlòÓ\x000f¬ì2O\x001d
º¬¨,É6ç~`dyÒu¯¢àMQnÅ\x0012'ÜU[\x001c{5°NªÇ:an*·\x001fÃOoÙàïrS8½g\x000bÒuR=ÖIã{'mR\x0008C9·Gº\x0013@ª·!\x001dFN=Ö	s£ü]ÆVGÏ¿þ& \x0003ë¤z¬Öj\x000e£Ç·\x0014Îw\x0017P»E@¢\x0006ÆIõ\x0018'
Þ½Én)Ê^ÈO=¼KÜâà«qR=ÆI;K\x0005Ã8Û"ÏKÂ÷\x001fÞ¤ÛNj`TmÂL´äß¦"(g5½ÝÄ-U\x0003ë¤z¬Á\x000e\x000b"u³ÂÆh&õbó40OªÇ<á\x001f¥Ô±x¶©Ñ\x001fón\x0013ÏD
ìê±OFKlÁN¤^QOMr´¦['=°OºÇ>\x0019¸õ\x0015Ù'Ü±¯%`\R·Æîf°?ßýAU=ðòóÕÃõ	:MrÑ\x0008\x001b,¤çE4Æ<}®xùýñåÉé<ªÔb :°Ûa÷ü~\x0019>Ê-\x0005Ò5^\x000cÑç\x0015ß\x000eo©þ0F>}\x0010_dj$³\x0018	5\x001d=\x0012\x0006þÑ¬4eÔÓ§¥H¶F²\x000c\x000f\x001e:jÎ\x000fÈ\x000f_p×=}!\äj$·\x0018	¢,MoqË³½-\x000f©¢kû\x001aÈ/ÿÙô3§v\x0005\x0003~6Å¥:º6­H¡F
K¬vÏè
ðJ¸ãÙ}ÒeX|\x0007Q¬ââE¨@´÷Ym\x000f\x0016:(qoË§51\x000bäð\|IZ¡K© ·¾lniº7·\x001cÜJrñµô?ip\x0007ÈÅ\x0000üJÏ\x0014UÄX$øEwPÐ¹IîÛ·'#Ç¯^Üã\x001b\x001b5<\x001ed£±ré\x001aG\x001f,ß\x0006«=¬\x0010µ\x0015Þ
ï>>zq¯lã½\x0015£­\x0019m;£õü\x0010îÈYAÏ\x0001ÆE½Ñì¯£\x0019ø	÷×ß¾]Ý~ÊÝCëð1<ásÈvpü´\x001bÅ÷âäÝ»ã³W'\x0007\x0007\x0008V\ªæRM\NòQÀÛlO)äAqú)¬Ù\x0015Ó5n"\x0003ï
/à\x0002Ë\x0012)7Áh:¬C35i[´rÏ 0q\x0017Í\x0004^5·\x000eÍÕh®	ÍgÙ»1àJ8\x000e-©C®D\x0003Y¨ÉB\x0013\x0019ÎÙË.\x0005m4æ	Í°qJÂW íÙÒá\x0014-l¨\x000fÄf,n»þ&²AW\x0007ÙàxÊ¦ó©¬â Òâ\x0010E~?â§
aÝª
Nl:\x0006øöNÞ½½{%\x001cý¢î \x0019]Â\x0016ö¯ÛðÔl½M\x0016áúËq 4
¤
GÓ\x001bzrçÚIp*ÍMHÅ!\x0017'§§SF!ì_qa Ï±R
C*"QÉTaÂ²åWªvÌý
y1¨\x0001¿3éÖ\x0004¹^1\x0017lV3m¿y\x001aÁ½ßx\²¶bR5ZÎ$\x0014?\x0004\x0018£ùþx n¼ÅPºÒË¡tDÑ
¶¤£8cQX±R¦2¡,ÊÓ\x0011ÓÊA
M2ÂK÷W¹\x0018ÊÖPv9\x0014lxJ?ÁenÖ\x0007ÞSæ@¡õ,Ü÷u¥¬÷ù»«Û£·w÷\x001f®r'þH,î1\x001fÜp­Kz@ð;.b9\x0015Û»ã×gGoÏß_¼<\x001e ©\x0010U¨Z\x00111G`9©b¸ ßèR\x0012n\x000e\x0014_·"ê\x001aQ7¯"F	ùF\x000b*÷'y«<ß»Ú>=	­¦\x00064ÍBð«±ÕËrV¹$¦\x000e¸ã­®FtJÄP#vÄ\x0012Ô`k	\x0019XceIÊ§S#bÕ£ \x0007nÝRFþEù>ç©ý\x0010\x0018KM­<8Úc,ò\x001ac\x0003-O4Ö«Ò-­Ë\x0012Âµé\x0000ÿ}õ\x0003#ÛO3\x0014X(HgÚñ\x0016ñi\x0017Q+âàÀÈö\x0013ã5oG)\x0015¿\x0011[Íý\x001f2¨Õ'F\x000eNl>2\x0018^d\x0005Å(P-PGÒvú@jµQ
j>2\x0016+òv\x0004{Ç>+¯.RÚ§iÄVÆ¡
l>2Î²X\x001cæ{JJÊ&}-VïG582ªùÈàÜÔ¼Á\x0005À\x0018\x0014lÔÜ§kÃ\x0017¢æ\x001büÇÃ;ücóå£°\x001a9_>iQóåÃ­xÚ\x001fè0k¾Äüiï\x001aÿ©ù\x001e¥\x0011¢uîp»{ü@¯nûb^
\x0017óª\x0012|FîkÄÈ¤4ð5\x0019åj\x0008?
)×R;,ÎN®ã×¤ÌENî&\x001bóÃòC3eDûÁUd\x0007H\x000f©»7æÕÞÆlþÉ±:"\x0006©¹È3åÄ3¦;Ðô»\x0014\x0013âë½àÝ\x0011\x001d¯Ìû·7×÷÷\x0013ÂPX¡Byh\x0008\x0008éé£\x0014'_T­é\x0013a(æ~}r1*\x0003[QÛú°ªÖRjUB\x001e¥²âfÊRì~­!±\x0016Û×Ø·bk.©Æ¡`ÛÒ$·Xí¸¿GâpþÏ¨:\x0003¶Æü4}\x001c\x000c½Wìw>
Äq Æ\x001c\x0003³èEÿ¯e15YÆª9\x000c\x001eÃ\x0004£bÉ\x001c>ñÒf`ÒÛ~'½ýÈÝmï®~º{|âÂ,µã]'z`á{äpK\x001cÈ \x001eÃ6zq~9ýÀ5\x0014àö;\x0001î\x0006<
>·àÊ
[Êô\x0014ç1MÏÒgj<Óñ´*xt\x0010È\x001bKxkWÏÕx®õÇõü\x0004¡qÂ0Wà\x0017<Ùýã\x000e\x0007Òå?Øí½oIòßÿ=èÇ\x001c0ÅÐ`×H\x0011\x000b|/Î·Zý4)ö.©SL¦ùý~\x0016ØWn	ñüDèá'åw|Q
­x
Tº¦ÒM«¥¸ëÃZÇop¦ÔÕÚ 8\x0004
\¦æ2
\©Ï\x001f(øyTñ	:o0¹ÓW^e~üz%><Z:S¬YI\x0004};zy÷k­Pl_~¾û5\x0012\x0019M\x0013\x0002ør4O³\x0012±ò6K|ÿúüìì¤V\x0007zwôòüð«xú&\x001eûã/\x000f?Ýÿ\x001ci»\x000f¥çßÜ=~û\x001c9C¥öùåÝýÃõ¿®n¾Á\x0003Ãú-xïG-ÀåK\x001e~J\x00118:×^æ×¶óËÿ:~ý®\x0012!sþþÝ;Ì\x0015Ý}ýú\x0008ÿô¯õñ÷« ¿VX¬äüíèíõýÏW\x000fß&¸$îîÔ7\x001c\x000c©T\x001bË U Âb0A\x000f¸XÌùÝÑÛ\x000b¬\x0012y7\x000f\x0006'O5)Ì\x000f¤ÒlX;
ü\x0010ÌL"\x0016®å·«U`Y&¶\x0015:\x0004\x0011LaÇP\x0002$ ÉùU`°\x0017L+\x0018¾*¤\x0004PL|Øà¸Å\x0004·Û /ëWe\x0011ÛF0kÒ\x0008ª6UÞúÂP©fêZYÍ\x0005\x0017kåJ|éÚÂé¢èD#±y¬1<\x000bu\x0015XVØm\x0003\x0003w+ë«Ãá¸JÀ¤ Z\x000b#E·
\x000c,Xh\x0005óÜ\x0018µ\x0011\x0003'\x0004³$ú\x000f+\x0016r¯Ì*00a±yÅ°$E'0+#ï1¥²p\x001d¬\x0013«o\x000b¬L­\x0017¬BUÊ\x000cGjÊ¼dÎjÚdÖuÞ¯Füãã/·\x0007.~0ßná/ ¤<þò%Ï\x0004\x001aÁ\x000b\x0011§\x0002¥¢\x0008F:ÒýoÁyÍ·UA\x001e^80ïÎà/OOq4Ð,äÐ\x00084BÒ D3\x001bCTôÖs\x000e/b3äÐ ´A*§å!$Û\x0005ë"½MâÐ Ã×\3äÐ8´@\x0018={\x0013ð1\x0019]Õôfµ\x001erh( q*íI\x0008¨°ô\x0001!
å6,+¸­g\x001c\x001a¶³¬ò:êÚNë¨¨Ößj=bk\x0019ö£\x0011{ïR\x0008b+
Ë?¶Ö¼#­\x0010\x001bA\x000emIÛBÂ\x0005\x0014òBâD\x0019ZH\x0012°°Ú¸
âÐª´­£"EyXGfP¤u\x0014Ô´`­t=¾VH|NïÐ]\x000bç§t\x001a\x000f\x0010RZO¶ÙjR\x0000ZO¹g\x0007(]\x0010¹I\x0006çI
\x0004FJEñ¾µFo´pÉN{§;¯#ºÑÙ"Â±áuj£u\x0004K#;­MÀÔTé\x0014­(Äg(\x0005µ\x0004Z'G\ÄfJ¸ke¯¹	Yí2Ýä\x0002õ¯ÓRJP²FÈmì6¾èËÞ«<XÊõ\x0000$\x00016/¥¡ç?k °Ú\x0006\x0012®HÙ{M¢MLOV\x0000	÷¤ôl\x0013y)ÍF\x0017%'[únJ8Ý(£â¥Lm2Èm,\x000ez)ª÷x{EM'x[6ÞZ²a·qÐKQ½'\x0007NÒk\x001a0\x0006\x0008hò5©(]d­\x000bCÓeÿ\x0010¿Zù¹\x001dNÆY¨¼(sG¹§È\x0014\x00139\x0000Ü»\x001bOë8æp¦o@å4$a¯\x0016¡Ðhj}12ÛÝ89\x001cXÓûDÆq8\x0010*z\x0006nhÂ1>¬ÂÉÿâÕ\x0001»`è·\x0012´ÍaulÉ"½ôF+Nvâ$
dOé)åT)
$(Óez\x0015NöâûÁ?\x0016NdñùÇR\x0004\x0013\x000cë\x0016'»Äÿk·Î?½ò\x001fê\x0014ìÞ@ÂÛë©\x0016ç¥\x001fLx4}á\x000er\x0011\x001c Öw~/|ØFøúìdäú©¸ònäÂ\x0019®\x0004æ$¥\x0003\Ô$)\x0005`F®\x0006Ë»\x0011\x000c\ðÔ\x0004`8Ü)q½ÑÄ\x0015]Í÷U\x001bW6¿\x0000\x0002W4ùè\x0001¡hUÂîë\x0004ût\x001d¾ýQ?\x000cÁ^Ü=þq;TÆáBÈb1Q¢à°Ê¿fÐäÙ(é&Í\x0017çïÿvm*³À"@Øü9á/q,o\x000eÿ\x001c,¤#@+·\x0001ÌÖ¦\x0003Ðè<¯\x0000\x0000±Á\x0000Y¶NqUåjÀCu\x0011 ö¹«\x0006\x0000CjFNÔÍ¥¤\x0011Ûð\x001d:³Ë\x00160â\x0003SâS\x0002}\x0013_Èd\x0012aê¢[Îwèì.ãsô\x0016\x0006|8ë;ÿ¾tß)\x0011M?¸~üüé`\x001a\x0019gL^ÿ|uûáóâ\x001c¨q2G;Ñz\x001a_yÄH,'Oþzq|öòûYïµBÞK*w ÃáÈmp9\x000fis0\x0010$-.Ôq$ÛØ¼bîZåõyÉÌXïIa	\x0007ñn
¼nîYcås!0êg{,aHkÌ¢ªàæØÃÏF½È{Éç®máé¥Ë8¸½dÎ\x0006Å¬tcòNä½\tç*Ë¼-tÏ\x0002/²¡E6c!c'ñ^Ò·g#\x0007ÏgO¡;Nï:/qwoIü$½Ú\x001cðÕ${+ÊæìwÓÊùMOß<f\x0007³U*w¯@Lè\x001cçØ¥.t­hRÖfÌû)Ã\x000ef¬ÄO\x0005<\x0018å[òña\x0007G*ÿ\x0000gz$ßÕÂl~ûíú÷Ç\x00035=É4¿ººÿ8\x0013â\x0013\ÄHã\x0010åøíÔÉ!ã ÃúÕñÅwcFùúáÆýýîQ~óxõ0\x0011I
vùÇ\x0006>\x000cG\x0000
§H*O	c/SoÞ_\x001c_Î\x0003íÜ\x0019 ¸°Ø>¿æ9'¯%+xH\x0004¶gÏ<Íò Î\x000eÚ~=¥ÉGa9n½|\x0007§ÓçÈ\x001f«póc§CG9ÿ^qô%q!ÏÞ5=»àhQ\x000eWEÍÁ¢×ôn´Óräf
è×_ï¯?C;úÅãï7ÿþî¯¿¥²>\x000ce'2%¹·J\x0001ÌENX¯\x0010Ùù#WÙ÷ÿ	÷ÀÉ»Tâ\x0011íX]EEºçªµ:\x0012\x0017\x0005T°Çü4¾v­\x0016ad!{X÷\VVO}¢X\x0017`1\x0015\x001dwÁ^rì\x0011¤uïM»5Ø\
\x000e¬8Üý_Þ\x0002zÌ3ëAÝ{6nD2å\x0005ÓåxYÃ®LÀ]6\x001d¬OÞe[aU¤\x0015à"\x0002»ýG®\x0016ÐcÍbÔ{ýõËÏö`²\x0008ëy\x001fï\x001f&³¤!`WxR¿\x0012\x0015[órâËbF\x0004ÓgqÄ.\x0012Æ²Þ÷\x0017ãåT\x0015Ü~¢h\x0019\x001c´6ÃÙ&&y,QZsa\x000b¸ý$Ñ28è \x001c\x0007§¡l·²q,\x00018Ëvýõ_\x001fÿþápíÍõ·\x000fÓ©
*WùU\x0000þ\x00068ï/\x0000Å[\x0019O½¼9y÷r4­QQ=ÉZÍSI£s?\x000c\x0016nsNÒ\x0006G
a(	×õÞýl¿ì²·7_îæ~H§UîNNàh|ùÉàò\x000fé
qô|ûúô|â|\x000cßÀý=d£/¯ïoÓU2á8H|d¢,_È"Ð´Pó\x001esÎØ»Ë3¼Bæ¹öÏE\\x001aÎÙ3ñ	ËqKªÒ!\lË±ö|ÐEXÊ[ÎÚZ!s¸\x000e?o¤ëB\x001bµzµö|e«\x0015UíÒ\x0019OÙîà#Ù\x0003Ó¥Gr5Ë¹ö\ä%\"ÐÎ=&Á+âò®<®øý»¿kÏ/Y¸»bq»\x000b'PÓö¢7hØ^a$±kÏ_¶^`Í³\x0004ë\x0015¨Â;GRH(²9\x000eázpÿ|øûï\x0007û:^%º½ùpõ0íhhÚO¥
VG~Wäúl\x001cû%ßa.\x001bØ^\x001e_ú\x0018\x0015Ý~\x000fÅB:¸@¹ÚÏºHx¨¹/Ø\{²n¿aa\x0019]ð&ÉãÐ'A¹_\x0015iö\x000búHc\x0001MtûÍ\x0001\x000bé3T¹ë,\x001c[£\x0012X$¼8R\x0003Ý·È[Ì\x0017]ÌÝÞÈgPi3íZÆó[ü¶û9»åxp÷¦FR8Z^\x0013¥\x0014.j3Ö,0Ï\x0017¿üóFÑ\x0010Ç\x001fÂûÓ®£îÅÍ«Ç7×Sw
¾#¤zÏÈn÷LÎ\x001a*\x000bîUpp[Ý×§Çï¿KÊX­ºsægw0AÙæ.<¡uVôÃ`\x0002Û^(jsEIïaEwxé*¶=\x0007d\x0011\x001bøp§dã¥À\x000fBo\x0004Ø¨èØjéåXpÕÀ¶®X¸n*wÇc7¢À¶£´lÞfpûXÚ¶ç -]6Øe:\x0007¥¬ÄyliÙx`¤\x0016ÒØ°\x0016¶=od![\x0000-\x0004lùÈyElà'mÁ¶gùþ¤°ÿs(*¢Sda½0\x0014'K,\x001c]Íöä5e1Î³Ô\x0001\x000e\x000b13\x001b§\x0019dJ¬fÛ5YÌ&©â)JI\x000f%\x001eÿïMùr-lû¯#Ï©¥W_õ\x0000à$=%)ÉN8óû×_oêrÐÒi}uôêñæËO\x0000H\x001a\x0003£°ÄÊ¢\nèeJù£#l5µr\x0018­ãaão!ï_¾\x0000Æ	µ\x0001%ÕeþÉ)©\³\x0012_Có\x0019Ñ\x001e'@äàÐr'¯v{^Þ\x001aÊ\x001c$v­¥\x000fT£¬Rbàý\x0010v
&\x0015þ)1ïÿ¡ÄÏÃ\x0002æäò}3\x000c©G\x001cjÅÜv\x0000Ný~)urò^-¡àBáy
ÔkP9C
ñNî\x000eèà¾ÐA[k\x0001°Iü#·¡]\x001b*'ÊU\x0010ûÅÁË1¸NyÁjÀ\x001d+
õPY~)\x000fZr¾Þùýòå\x0018\<\x0001qÌÓñå(O\x0006q\x0000å:à¶ÚK?¶`paò\x001f\x0005|\x0007¥è­ÍSYõ&òÓmìÇ`ïaÙæðÏ\x0004õ(\x0007ÛáCsûo4ª<E\x001côØ°îÊqôèÙ\x0002Ã&õÝ½eÛ#òÃb*G¡IV¨´ZîE:-\x001cÔIµ\x0003Nj GC\x0014Å `»²µ¶û5ëË1¨Wj\x0019å»#hn2s\x0015­C÷-Ê3\x000b0B¹ÏM¿ÌgÖ8ÊZCÒÔË1>Øë;÷¯CÅ)ß.1¡p}õøûÇ(wý¿Ò+z(H¢N»ïEòwGN89~ÿc\x001eãíoöÛ§CÑ:N&¸~¸Á\x0001|÷Ì8µ`z\x0003»c\x000eµÛ©Gß\x000cÒn$hÇ\x0019\x0005'¯q\x0012ßÅû¿Mø¶;Ò½Ø½\x0014U´r7N¢,,&¡#OàÄ´øH¾¾t/\n#ÕY\x0006IázËÑ\x001f\x000f´0ÐÛ­é^ðÜúës(\x0008¿~.
Â\x001f^Lá;öäÜ\x0001º\x0017I·Ê#ÑÖÀ®·H­Bq¬|u)çýç¿ùº\x001f¯<\x000b>ât¯¯¿°Fä¿ÿÏ«Ûk\x0008l\x0014¸0É\x0011Î\x001a\x000eaQ.Gv¿¦²¼\x000f¾Ç_oÞLäåñÙ«\x0011X{÷øõÏ#gy\x001cæ¹\x001bÌãXcCq\x0018eëLj<¶¦\x0003§|\x0016òé±_\x000c©"ËÝx)è\x0002
\x0006l
C5Ý6CîåîZbEt\x0004é¨"
ë8XÔcÕÍO¯¥Å+\x001aï\x001cv+ªr\x000bT/Q 6Æ§\x0017RKÐ­iKB(i!Yw\x0004 åHö§\x0019òée´\x0018R[ª\x0016ôÂSd"\x0014b\x001c-þ_Æø{üí\x001f¿èÝÜÞÝN×ÀàC¶ÉbG:Ib
L\x001aOÅÔ\]pöúìülìõâ³V¿ýëcuÉ\x0019ÊRÊ\x0017w_¯¦ô÷P8ÎÐÓ\x0006Ç»Ì81"î]7ä\x000beÜó7Ç£\x0002|\x0015Y>\x001fdÆÒÖ\x0008_\x0012Mõ¨¼f:ÆÐIöíã£ýòuäÇ|qõå\x000b\x000eáº\x0007\x0014JåÑC\x0011õ\x001cQä\x0011÷[©·²\x0013õV/OOq\x001a×ÅØOZá=­YW\x0012Ýø¼ÃÅ
Gx+ëÆÊtÚøöK\x0016ò\x0008\x0014Jbtd\x0003¢$=u+gìxµÎ,à??ý®Õõ\x0001C\x000cG\x0015®I28\x00118(µ=iIeâA\x001a
cðgp,@Ú/\x000eEòZÑb\x0019+-\x001922}dÇÔø\x0016\x0012í«=Î\x0012Áÿ£çb\x000c#±.-åäð#ú%ök\x0014æð4Ò-â\bê°Ç00*×¹h_àqHbò2Z#x#Aç_ÍÄEö+%f×\x0008ã³\ý8¼F«\x0010`F0\x0017"í:Î"¡.4Åd(fm²¢#Ï3ÄÛíëðåÛÕ\x000b\x001eë}¿»¾½ù×¤½Î\x0019\x0002R\x001d0,l\x0005N$;áÊÜXéûÝÉÙëÿ\x001a7Ø\x0015Ûðv_Ê¦¼¤UíJ×\x0012~3\\x0018©Ym\x001bÖÓ.Ó`m<	aj\x000e_0#ÉÊ#ûÒ¡}pC»³\x0018\x000e,µ§Si¶Ic}\x001b;Ü°¾\x0000îãÇ\x000föï?
²ûKµR¬\x0012-1Ë¾«§^ÊÆ=\x0019µÓ¡\x0011\x001cË}û»Òä<ÙãÑ«û«Û¹úæzºé\x0005~DêJZ)ÂfºéµÂú¯C¹²÷G¯.Ï¾Ëõ7'cÝ/\x0015âÀ{mAÄ
\x0008ª!Á2VªoÑ|\x001dø·*H/AüÕÃUýá bJ,A\x00146æ\x001958Û Ù©ôDm5ÕkXï\x000e7Ä½Ïi¹Uüç·/_þ\x0018Õr¸¸ûðùúáa2|r¥¢D[\x0014\x001eÌªÒè\x0015Õ1\x000c#¨s ¾¼\x001c®~ºÿIý>âÑ¾ü|u{7ÓåÒåÉÅ\x0006z«"?1ì\x0015¨
êô¿?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-11.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-11.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x0011OE¿YZ´ÕÇLÊ[\x0019\x0004\ç;<h\x0002mÂ\x0016¾ÑË\x0019Le\x00071uræx¾Ã#\x0014~Û\x0018\x0004ºù\x001a\x000fC\x0015_;|:ßã	ö¸?ÃÊåþ¢´á'?÷÷'oñÄ©à\x0004\x000bÏ	i¦$)È.\îP:~KÜS\x0018d#N(ËÂ«ß:UèùùI\x001e\x0012)qc#ßâ±ªòb?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-05.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-05.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=.=éèL,\x0013Íåëª<\x000f?^k\x0015b
wæímEb6\x0014}7ÙP¸ZË¡ÎÙæÈÚÁDÔqÚW¸VîoÜ\x0000÷àDÁÕjàe\x000c.kà\x0012Ù*m\x0017w^Ô\x0000G/ªÚCêD¿Éè¥\x000b¸%AûÝXfñtéú§¿ñÕ?zbZà|\x0018=\x000f/­ba¢£\x0013±Ou&ZÓ\=G¯^ÜA4SôjGïYC/TeJN\x001eåîÕ7ÿV÷ç­\x0007 ÿ¦NíPwð\x001føníø<GÀiâ\x0007\x0015®Sß£Ä[ñÈþ1ñ±I®ÜÓ\x0015ÜÇ\x001a³\x001fÐ7ý¨½æÑÃ«£Ó§íK¡,¾rj×3a\x001fouÌ9\x001cB,\x001dCÒÜÅÍ{
Ø#M¥\x001eÜ¬ØéÝ)ø¹ø\x0010¿üÚ}óùjwÊ~óöÃóÚñyG+Y+Ñ=\x001cÎr-z­üzmÇØL4þ	D\x0019}+§(Cç9\x0016üuqYÚÆXçygÂZy ìãéPñõ#õ\x001ctô\x001bÈ\x00187ì4íºÝd2¼-æwïvOü¿´\x0002Ä¯å\x0018¬cÊ>óOL°PêÆ¥\x000f'z×\x0010çi¼ßQ\x000fþ¾±FK:,ç`¾¬}Kf+?Ïæ#çÞÞ8fj´­qÄökÃÔûâ\x0001Ì\x0000Ïõ(\x0015èÞIðaðÁQ\x0016<·Qxi>f\x0000î\x0006x
\x0018\x0012\x0018k\x001bók;ö$å5Ó#ÏWÇÊx©fØ0ü\x0010ylàÔ¼Ähåðsì
»R,Æ\x001b×á³\x0003\x0012¬Éù¦h¶æ(\x000fpÈQz¯-à\x000cN~ÎôaôV³¶§+·\x0016WF~W6\x0005d5ûÐAr±·D'QÞ	S\x0000\x001dä»ÚÊKåK\x001aÅãÍÆïÂ×æÏ ~>]¾{ñ\x000f\x0012\x0018üp#§DN*%KbiÃAú\x0003huøÂpoSôw÷tè¨È¿\x001d\x0019ôÝdó\x001e%²>zlõ×ù'Lv&&Jù}ùÑÙÖ(>@ýp\x001dÄÍ°Ó:u°\x0013`Gxä«!pÁæ\x000fÚ¸s¸\x000cÐ\x0005 }kî¹BËÅ° =c»e ¼¥ùOïþ°;º*áöÝ÷O¯\x001e_ßÈñQ;OF&Åpd×Ô7\x0000«Ý\x001a\x0018Vðßõøº`û\x0012\x001eö\x001dåððì×}tgoõÕþðï_}ä[½¹áÇ\x0012óÎÔZÇúÏÑ"y.ðsjc¶ÝÓÇÚÛåÅé{JÕuùZÑ\x001eBúó$NÁ\x0002­©Ä(ÀZU4\x0011Ü\x0003øExö
®o¥EðLL\x0015òö=;Ðá=\x0000ª\x001cl=E/Ó¡´4ÁÝø]§+·°r%_\x0015\x0015;ûÁÖk¹?ÇáþÏrÃï~ø>îßÊÆï%plÀ\x00187A\x001cZ{rðï§EY}3\x0008Þ\x001db\x0004í×\x0001õ\x0012ÁsÝ\x001b\x001eçg\x0018°\x001d`ÇC\x001f@#\x0000c)G+ØD§Nas\x0002¾zóûGãö'àxýúñý­Î	Ä6SU#ãÄ?\x001a9¯Ý½\x0015s>1Óws:\x0002.\x0006Ì\x0017d(ÐÖ¡Rzò)1=8N[³\x0002`WÌ\x0016
6OrW7Â\x001eI\x001c\x0015~1]\x0012ÖÝ¡bx×4ýûð§÷ß\x001d¯ç¯ÞÜêx\x0015ÒRI9ætÜ\¨ÞàÊËUFã'``úfÎ\x0006&\x0019ãíÇùÁòkûR8ÀÎÑíªÅ=NW)\x001eÓxÙ!tÑ¸QÆ1¶Äk<ö\x0007÷ÕãóÖQÒÏo_Ý¬`,+"Å\x0010ù­æÅÅ\x0019WÅéÀô;c¥eqf ï(»Iâ¢ÚcÒü¼dAÛA·Æ§È[\x001at)J\x000cðQ>#r\x0018\x000cÕÌ$x¹y§nN×­: }=Æ\x000c4tG¥n§ÉÂ	½Ov8G\x001fé§(çÿÐ\x000f¾¬Ý!º¥.\x000f\x0001Ïmé\x000b¡f\x0017Xº5H\x0006ÓWOS\x0004®c_ªÜ)º\x000fÚüÞÕ¦\x001dk\x0011)rH-s6|!ºCôzè0èÚUª\x0011?ª+tµ³Y(úù¶;ØvusFúÃ©\x0012\x0003\x001f\x0019çù0º\x001aøKåÄ9ý\x001foÞ=¾Ò\x001br#\x000f5S\x0017\ªÔy­	LZ\x000b×\x0001-÷ÿ=y@f/²ïèäEælÑÿÖ9ñ<T\x0012ÍCÖh\x0015s.\x0007 G.'+?\x0001 «\x0019S.\x000ejàMßTú¿yóá\x000fÅïÁo^}+^Ä\x000e,YqÙ\£ì¤£\x0018#ïÕÜ;Ëè}Ú÷½\x0008±º~°=¼x{C°P7Æñ4	ÕðÛñ\x0000Ú
èà Ûâµ\x0007ÝH-?DÂ.Ñm\x000e\x0018`­Ê\x000bøQ"Õ\x0019åÒ­ÖÞÕÎ|ýíoÂÛ­rms}ýøôæÅ¿¼ÿõúFÙ·âeZ%·ö. QÓ*©ªÜ½Ùfßæ\x001clßØ\x000fuòã>º1Ë'û½«9>Oö«ÛÛ\x0002GóÁm­ýýÔiÕcXLï´óÓH¸M\x001f¨oãl
¬\x0005Â\x000fâä¤\x001bI&®SµËX\x0000ö°\x0005:
k<\x0008ÞË}Å\x0007Á;V;/¶Oåm\x0001`\x0007ÀF¢¬HÞWg°ãF°ÓÀNþh Vl\x0015ßªm×X¬Ùd÷ë\x001f¾õoáÐ\x000eQÑ¥T\x0001*
±\x001eyý¦-7\x0012-©ºF\x0018¼£\x001bÄ"ÔõäúÕwóK­«\x0000SÞ\x0003¨ï2Ô¨tk´-¶&wm|\x000e\x0001¼\x0018Ìãè N|È¬3ÑSÓfô\x000b3k \x000ffV{÷\x0012êG5c)»±[\x000b/½Ý¼øã\x0007x\x001eþøÙwÿèQô%\x000e\x001aè\x0005Ð534ÙQT
YjS{»\x001b\x000bu\x000f\x000fð\x0002ñ¡spõ\x000er\x000cÈ\x0016ÍF:	z\x001btU0h C\x0018dü´t7$ã\x001a:\x0013¬´C¶Mj	çè\x0001Ð#m{V\x001a\x000c$Ý8¡·jy9ÿ¨\x0005,£e¬
èh´ÅOß45år~\x001cK^$¥!B\x000f\x000e,Å)q:54þïùÆTØ\x0018õÛ< cë{+ ÌEÞ¼É-Æïþìx»³§?{ûæÍÍ\x0012×6E\x0012>§ÄÕ~ôuþß¨\x001f©w#èÝA°`\x0013\x0015,×£ï&ÉÁÅù4~ÖÞð3¹¥´Ø\x000bæK\x001bÕÀ\x001emTâO%ìvÓzVÆó\x001b\x001dMãÈ±õ[\x0012V\x0003<!xh\x0016î
^<\x001b¼è<g.2§à@°	Ys\x0013|ô)%\x0017S¥Cü¥>mh)\x001a\x000et(\x001af¹Ö\x000e\x0013	\x001b:+\x0004½S·ð®\x000ft7x×g\x0007ö£]Ñ'r Ã\x0013YÄ\x001aH\x00152\x0004Ø\x001a:\x0013É©7$øó}÷¸ïòleHæ:´ÚÎäÄkO¶\x000e<ßwû
æ¬t2æÛ¬ü\x0013¼öÒÆùó\x0003é\x0013î\x000cå
åªP*Ý&Ç£b\x0012ÀÓù¾\x0007Ü÷ËÐù+z
\\x000cÎ\x001c\x0007ç\x001c]Kâsô2Ð+$
¼2^ÈHs9²\x0018^p\x0003ºë \x0003¥aá1\x000e½ÉÎ£Âe[Rë\x00028]wó¢\x0002+nX=wQåJ£ÒrnìÀx¾ò+×R\x001b|PgÛ­·óÖ½¸\x001f×\x0017Àaå%\x001cÓô¤ë_Ü\x0016	æ®g1ÏßS#%°0)Ín	5\x0001¨ýMÆ/ÿôþ)ýn\x001d6©Bvò½yzûáFxIÜmn]¹ö¦äÒ¡Ï#¿Äj*óÎ_ùxñ\x0013J};¨¤ó¸ ELP¡càÅm/¼5ÑO§èPyI-ç\x0000=\x0012}ÀgÎÄ´qÒÛgl \x000fs*è\x0001Í©\x0013í\x0013£ógÕ\x001e]]g 'X{.¼vÜhUtÂO+ì,Ôß\x0001]¢¯	\x001d3	eòL\x0004¼k\x0003oL)\x000eï¶\x0018Ä>¥'ÞvúèëSt\x0007ÛLßcÛ\x0013Ôâ¹ò¢\x0012+í}?Ý\x0018\x0007\x001b4	ù@ÒÎdö\x001e¬í3¤\x0017:Ð+ WÓZQ¯èÉ\x0013õÓ×À&ÕÚfSýRO;Ðý¨§%-û{K¶Âà$j±\¥°u\x001d\x0000zlºD¸­¬\x0008g=az¨fõ¶±ÃçVÀ\x0015È\x0012EB;x»IÞÞ{Fo1jXB±\x0003=P,5m¼ÀÎ[¤¢»`\x001dç6£:_Ó\x0000×´¤\x000c
ªZo\x000fò\x0000OÓÒuRÑüÒØôüoïvcÏu_þ?¼6ÄÐsÉ¥\x001cçÓ¢ÑñbªÛO¯M4aóÚX³¾©:·jl¬Ã÷&H¡GðÌÌ±\x0006×_Sx\x000b\x0007YçËW\x0013ôs;
\x000b¼éÒ\x0016§é
ï úwÃ|hµ±Ð\x0005Ô
"qV{qä\x0002­¾ýé¸&\x001d\x0002Ú/å+=hA+àtrlKæÈÏ:]}°¼úÑmëª~
^}å\x0000¡6oÕÅóÕGX}R#âhõà\x0003±heõ¹eõãâR\x000eø\x0002\x001a<Æó>W¾ä¹´~X¥¨A'°ÛÉTmÄgçÇ8×yÛÛs\x000cÇ@wðÔ\x0017L\x000enè
¾L\x0001H±ýÐ¤Å\x0000\x000exôSBÄ\x0010DEÄ\x0003m
»\x0016;éÅ;\x0003Ï\x0006]¬äËÚ\x00013ïL\x001f]âò©1h\x001aNÅg§j\x000b\x001fµ\x0012§ÅÇö\x001aKu\x000eO®Dm9¿+|­ôîøêXDO+|9?5\x0005OM­¬\x0017[mø»ÖJÔ\x0003·íØ¬yã\x0001\x000fÇ&[\x0003¹W¯Ij\x000f\x0018>ÞÒ:Ìe\x0017Oáká3o\x0001>ZÊÒøY	J7«åQN\x000f7xp¢9u\x0015ÞGJ½yÙHZ}5\x0017GëÔytýr#FÅßä@){_Ù7KÑ\x0016ïN÷¦ýiX2\x0007v¸M{óôe÷.Ö¡·\x0003¬>è@G\x001fT¢\x0014\x0006:yékgsS»\x001e§÷§f¸ýiçÆêN¹I\x001cZôq)\x0012\x0001n|òàªúr\x0019è*}O\x000f¬%-;MQ´\x0004Y>5òíOÇûíPVAà\x0013=°òU7Á¯l\x000bóôª~÷Íðæ~ûô 
3¼Q§\
\x001aÇ}+]mNy9,Z°~7ùà\x001eëöóÙêÈ\x000cÐví°z\x000cälËÙ¢YÎ}»w3+`{\x000b·.\x001dCtï\¦Ö9_©ïS<«+X-`½Ø~~ÑmJú\x0000´ 	3\x0005Á\x0008nw:ùôqÙ\x0010ÕÙÉÿm'®ø_ÿñÿðôÍ­Ú¼\â²DJG¥)j\x000e¤äÚ·¤Ý=\x001dÞÒ¦ÿ-ÒîåÄaWA à°ËóÇ=1q8AëÐ\x0006@\x001eäFÙ@èTµIå\x001b\x0002÷+k\x001bÃpr \x000fn£ÖÐ2,üi¸>*ÿS×¹q\x0000`É¹eù®È¡¢Ë(ÀH\x0003æ&Õ\x0003x´¨f%?Ã.G\x0018ÇÞKàFº\x001av7!ÍMP\x000eË·\x001fþýFF<VÏæÄ×\x0019\x000c¶Óhr¥}Ò{º\x0008'V|±W²;¬Å´ÂêG\x000cëµû\x0019\x001d¿\x001cH(?»ÒÄÙVÇìnª×C¸à³a¯Oe\x0006hÓmÈ[e¡+6ÄÞMæa¬;\&·\x000f¸$êc1_¼í\x000b6PÕ\x0005/&¦S§§³ÂùRvÇ¶×\x0016\x0003ÞZu_üòñùùáÍ"eþR"¡p¯®ê°]~wtx­Ê]\x000fñàû8¼'V|9\x0004²£Ê\x0002@3Ní¢»Õ¡$ÇacÙjz]¡GêÈ;%¤\x0001]('q"+-[\x0002+ò\x0008'¼,\x000bÉý\x001aÉÁ­¿N\x001dÀ®ç\x0017V¹\x000b6e8ü\x0001\x0012"9bNGV]&µÔ±\x0000ý\x001d\x0000ÛF\x0012¥ Ö\x001d&ØË@2ì4®Ea©_\x000bóðx3¥%1f/ª9$vbÐñGÃ½TI\x001ag÷bßb±¤tKY\x0003'\x0006g0â!5$9Û¬çê]Øªú^¡¡\x0005)h3ÖÈ\x001a:\x0015Ä!h\x0016®÷b£´u©6¬ÆQ>úã=¾¾+{E>\x001fÁÜ\x0004d9ëU¯ÿ§Àz_ü[ÙÍ¹GsÿÓ>º-'lwWÀû?éëõøâßÝêC¹R¼Åk$­AýkmæjnÅ=}¨v¨õ²Æv£\x001c¬TÝ{Äò\x0011
(XGú\x00124JÊJ¥¹`\x0003&û\P¶Ú§Ú8A\x00076×'\.»v2ÿ\x001fT\x000cíõÓ­4OÅK¡H@ôõë»*áÉH-jóêïéãkÛç§äPAñ:if´\x0010\x0012|Ëc}qAI&µÒü"Øq\x001er\x001dNg\x000cV²Ñ±W\x0011Ïà\x0018ºq\x0006×\x0004Ê\x0015:ÒªG²Ø¨â\x0004)ÎJ jÞº]\x0017h\x0014RÍ\x0006ºD\x0005º¢.²
Áy^µo¥¥\x0002pÎ\x0008Ié^Çûá^[\x001e¦Sö\x000c\x000b¶Eì¡¶`(H
h6±rWu¸í.Ø@µë,²qþø]	dáì	ñÑ³](:omùe´ÒÏt^ÇBéTØé.tå\x0017E6m¹§{ºÌûÆÕ5
e×(QÀº8\x0012äòòÕYÒ;7Mï²&.È£I¦Ö+:ôhYØy*`Ýz\x0006ÎG\x000fS´\x0001\x0014G{Ã,ÑòÚL®+_ÂÄ\x0008ODó
´ñF.\å$ÊÁ_éxz\x0007cÖoîË3\x0008¹OÉQÊ\x0016Î>\x001bs[þµ \x0015^Ûåék1w¢¼\x0002'ÑÃä2«øÈßiÃU}~#àq {B.\x001chP"³ÌYÙõÚ\x001d¸\x0001p\x0013\x0014µuìæKÍ¡l)ªÕ=ºàFÂ\x001d\x000f¬·«õ\x0001pádmÙ©ð\x001fÀ#¥ª¯í¨\x0001è<dVà),M¤\u"' g@¶\x000f´\x0011aJ¨ödÝª½Â\x0016-­´vÀ\x001a\x0012\x000ese\x0012¨kª\x0015³öþ[\x00017s
Øs
¸Ly\x0014íÈÿË2\x0004m@\EÕ>ÑaºÄ.\x00105ÐU&\x001eãÜ¥6Î®«§RgãÒò@¥U'\x0013j_kÏ.u°ê\x0008C¥£Q©Zy2¼jÛ]íÙí³pûRÀá\x000cIþ#\x001dæÌhYlÂ_Ém<î_5îJéÓY\x0014\·®n\x000c70Ç¸\x001büfº©\x0012§¨®l`£3èÆ&ªp7jàÂWv­ÆgÏ® +X\x0012:1Iõ+\x0010Ùx®\x001du\x0002=»vÜÂ*¦\x0018tµ90Ñ¢#ÍÀÒÄMûg\x0017ÑÂE¬M¦þX³6Úv\x000eðÙ=ÆJ­u:ÕZA\å*°ºVK;»\x000eîa
deã)¥CÁxÕ-¿ëÎî¡{(oSÎà9\x0004ÌñK°&§Ãõ§3d¸NÚcÑdÑy:ytxv\x000f\x001dªO\x0014´¦JÀäit o£×apWh\x0018Jhì1±Ý\x0017KdC'A\x001doµë¤·3äÑÊnuêðxZí]OcÑ÷£¸~>În¢Ë°è\x0000òº²hO­B²è§KÞ8QgÈ-\x001eÌâVò¸ð}q½7ëìP\x000fbFè¬s×\x0003AOÂrý#ú³£ç=Ø\x000f\x0013\x0016NKïV
¬9/Ê¥gçÃÃùØ{Ú\x001fõÒ\x001bÓç\x000c\x001a¾¢÷ À,ÐÊb@\x0002ïuhá?û\x001e>#;xÙ¹é\x0015HìàiµS]Ò³Ï\x0018à3\x0004)V\x001dnÇf/³¾­U&}Æ\x0000Q¬3ø\x0008ÚZ\x000c\x0012¯¬QÎÍÍ[º`\x000fhøÚÂ³¸
zÒ^>\x000b#fÂÙW\x000cð\x0015Å)p¬UUÕÓ¢3§\x0005z±7}Åp|Å¤Ó\x001c*|Å4Y\x0010\x0013Ù\x001dË¥\x0005,ñì+ÆÁ2\x000cýÃ=\x001a&g>{µÑ*ãÙW~@{ÐW°ù"À?+KîçÚø\x001aìÄ\x001c\x0001¹bdX\x001c3¡8
k\x000b«¢Í¥d zÝèqßß®\x0008£	1®Å×pd´I\x0006´þB¶íòßQ\x0004R^ý\x0017o'ÿ%å\x000b+áøq\x001aiü<W1tÙúõ½¾Bc\x0007j¬S\x0005[¦\x0016ÖHÔfmæØÏcõý°c;¨b5÷-qÏ/©nOî\x0005\x001aN®<8Ø%\x001f²g¾¨ªmóª\x001bélÑPE\x0011ËM[}i\x001dÈÞò¢wy,ïòæJ´êôûÇ×ÙóÒb·$ÕTÇqÂHÒ9wF\x0019ý4Õ7ÝÌ)£%>$F
:
\x0001í¸º'S2À­ç\x0001\x0019^L±\x0019w­°êæ\x0014S\x001b³\x001b,uàÂs\x0019
±ù\x0012Ë8y©9A¤ZkzÔ¥}÷â\x001e¾z|-ûx£c%Þ?ýÎhV²\x0018´Òtüà»(Ã\x001d\x001d«O^ª9\x001d+¹î ëa£ÉÔ´¬I&zÃ%ÞðÛLé\x0005y\x0004*Ö?\h-»ÓÎ\x0007:¯±4O}
ä.À#¡âÇ$B\x001bJ¦¸Ê>%Ï@³$Û|æ\x0005v\x001c×¦\x0011_\x0006+©pnà\x0003bÍ#zE\x001eÙ\x00141/Aø]Üj^r*¼äÞÍºº\x0017àá6\x0006Ã\x001a¯Ur%9ÿÞ\x0015r£CnïØL¹ \x0017Ø\x000cG!_Ï~d/Bi¹Mæ±#£ò±ü|øJE$¯gá·\x0014b{Æ6éÁ\x000b´íðÐ\x0008n}ô,¯¾l\x001cÑMÉ¾ì\x000cNøæýÍÄ¯å\x00103ÇÒ\x000c\x0004<j\x000cÎÚzoC\x0012÷Ùåî¦2Ý]½\x00102¨²\x000f7\x001ffîç\x0015ç1ìß\x001d\x0019ÚUc¢ÆCÕEÄïsá~
\x001bw|S îÐ(0\x0010É\x00135{\x001a9ÊÉ¦«­æÅø^¡MÃy(ù8¥êà c_bdhm{[\x000flÝ;^_<?¾ûê÷?þß·â\x0004ªÜ\x0010+\x0000\x0017}#\x000e\x001d@«NÅµ[¢Ì¦î'?¡\x0002,\x0002[]d
§Rk¶Ûrâ\x0015y÷.Jv\x0018&«N#CµzÂ§Ö4þÒâÕ]= G\x001cÄ£Ù-ú¸(U÷\x0014WÜ1Ø»è\x0004WX±çd¸Mó	u[ôÎf«\x0011ýâ7_¿½
/JÞ(Ã®arñMSÅ\x001a£&ûòÑ\x0017?1R#\x0005\x001dÄÇÉµ\h_x¢`f7câ@H!gP±Úcï)·f§<¦÷[çë\x000c±\x0004\x001d0b1Éá%í\x001c\x0015ÈäbEÜ´
l\x0005èÿ\x0017ªBÇÌ\x0015ãX¯ox\x0010§\x000eÍ¡8Í5¹£\x0003v6¿b}¶&rEðr[Fç9Nc¸\x000cµÅê¤º5³º½ \x0007FÄ¡E¡ Ax\x001b5oÙ\x0015Wäa\x000eÅõÃÂA\x0014+¢/\x0012ìy^s2»!fÍ\x000f.\x0007\x0018åaÕyÃÞ2³Ö»mÝ]+òPþrÉcÈ\x001f=k\x000fÉù3\x001c@÷VË%p¸"ç\x001c2P[\x0005ÙRÍLÌ
_·aÃ\x0015·\x000c\ÕÍS\x000c=g¦XÃÔÔÝK\x001aû\\x0001Úá¢\x000eL¡\x0015[ÇÈÎnÒ¶¡a tÍ½ýø´2
\x000b­ÇýÊK2ÀuXÐ·`èÌÂ\x0019!wþD²3çJÕ3Æ¡jtE¢Á0g6öá|U¸\x0002\x0003çÊÆ¦×pÄüz,\x000b\x000fë\x0014`SwW÷
\x000cÔ(MJ\x0000°\x001eW\x0000Î\x0007\x0012GÛ\x0006/\x0011ÿ\x0015\x0018(LûÏüÑ#²»aWdà\x001añ:mVáù\x001f\x001d\x000bÅmd~È¼èT	\x0018\x0003_ÃDÜ¡\x000b\x0016ºèô\x001a_ñû5Öù\x0015W9´\x0017£òwO;¦\x0001ñæþúÃóÃÓë×·º½^¾Å\x0014Î¥+^\x0007!¢$\x0006éÎ¼ÆzË\x001aåöì	6nÊ\x0018¡BËáèÜ%ÏiªZÛýÝÐé;4\x0014Ezw\x0016 \x0013HM}Oò/méâ\x00027\x000c*³:\x001a¥½R¨	ºÏ^\x0019É\x0017dd$\x0004n´Ø4`}r,ñdBoÀ]Û\x0001;6´\x0003
v$UÁÙEOÌ"Õ<È¦¹$Ö:îÄ\x0017¯\x001f^]K¿~xz~ºY\x0017\x0018'Ír¶ÊA®\x0018\x0002JÜ¼³ûði£t+§GG?rEsX¨¹FHrØ\x0013r/È8g©Ð®ùÄÈrçômÚË\x00126öã·ÿâáýÓ·O7ë\x0003Ém*\x001d5ØZ\x000ei\x001c)ØV~»§ïÿ*\x0017)Í\x0011	5Ð­×Z"ÛÜ\x001cmæ²2o-£T\x0006ªb~rê{þ{
q.ÈH`B\x0011-ù\x001a×ªZÅô%·¼+2DçÁê¤¬9ýÖÆ#Þ.p¼\x0006"i®`\x0014ùç¡/:9G*8â3Ð¶úõþTÏ.öÄÞ*\x0014&¢L\x001a\x0014¨Ùß]Âþ\x0013I²ó5¨ÄæÎò(ÜúLzJu[v¾"\x0003ÅÇ0QË³Ú¨7q¢ §Æ\k]kuÈÇÏ\x0017\x001c¬¯XyWaº\x0010Ø¬búóo\x001f¾zûþ½¬¸ÇÙXª¸¡?\x000cNÛ´¦ô¹Fwt°
\x0015îø=+?À´Þ]ðWô\x0002·FÙ\x001a¨U\x001f\x000c_Å·ºè::á
\x0013Ê¥\x0000¡.²º¨õ\hR±´\x0016®¦\x000bö¨4\x0005\x0015×\x0002è¨uB<5¾\x0011\x0012\x0016·$èÚ®Ø¡#L\x0006ð,Sd\x0012ÍÑ^\x0018:·ÆíUê¯ÈG\x000cÖfÛ{æ2*mÑiQ(¼@'HSù\x001cÁ\x0005·\x0006ÄÕÊQ*½j¾¡iu`\x0007À:s\x0004s"\x000baäÙaì4gV.ç\x0005\x001bæxí\x001a6BK|h×\x0004äS\x001fWÓ(Yµ>/Ø\x00197D
\x000ed\x0004ÅÐ\x0005Âöü\x001dm/V¥Ï+ö\x001c«6ÛZêr0¥N¹W×òùlO2î	X2KDD Á
-Û¸!udhåT\x0016\x000bs%F¸\t&\x0019Åz\x001a¼Çnø\x001bFò#æµA¯!ñ\x0005zÄrþ2ND5\x0012ÝVÎ6§qtÊo\x0007ßï¶ÓíU\\x0012Z°äÀî.\x0001Ï|%íóÙÊ3¬<!1ßm-ÑÒ)¸9tìÅ½b»=æù$î}"ß×-ß¶a\x001c\x0014\x000b\x0007EÅ\x0002_:X·Ã\x001e
Á6%òº[.]«{ì
{â´¨4zØU\x001a\x0001LÖ^99mKìà'öµýa;\x0018#WÅb¸¨âA$Ò*¶DÌÉIq@WõV\x001b(@©Éõ\x0003[|dVjê;®5Þ=¸M Gpï».\Ã\x001eü¥w@´WxÓÚ\x0001\x001fÌ	\x0001/Ðe#pË½e\x000b.\x001f¥OOXõ9.à\x0005V\x001e1õcT
Ä$Zù¤\x0011kop:Û\x00167¶Ev0\x0000WÀ+\x0006SMðN¢I}Zø*{\x0005\x001f©¥&,=\x0018]^Ô\x0014¦¨Ç¤ö\x001a;âú´?\x001cà® ®W1¦
&\x001fà[d®\x001fÔ<?í\x000f\x0007¸ªèÃ[J\x0012
¸aÃ¢®v÷ÙÎÀA¿¢hk¤\x0007ðÈd&Ç	¼k¶¯C®àøAM\x0006\x0012ÉJâ¡=7¬ZiºC¸ªÙ_±Çåw%ÓåÏrv<b\x001bÖ²Oj\x001fþ²\x0015¿Ô¼¶D\x000ewÓG\x001bÁæ\x0011\x0008rÆ\x001bt>Ûð\x000c\x001b\x001e3ê\x001bÖ`ê\x0018\x0019º»ØéQ¥m ôúíû\x0017¿xøãdnROy
½µ×@©hébø\x0000m¿¯²Ú§VÛýR\x0005\x0010ÿvÚ§gÀãK¡\x0013"oÙMû>Ý@N¤t]%ÊV\x0004(\x000b\x001dëÊ(3Q¥
_àXØ\x0018¢µÓÝ¶bwE>r§g\x001fú£dËVs\¥\x001a\x0007¾ÓöaÌËi\x0007\x001cº>Äë\x000c95Ë;5xðNs\ØÆßr\x001c:\x001fgÉù9{V.\x0006Ó\x0001G2¥Ä´WÜZÖ\x001aã\x0015ö¨1ÊN\x0014Z°¸6?IÕrKRÐW{5\x000bag\x0016´Aêí«ooÕ\x001d\x0015©»±¸xP¼´f\x0002Uc¯\i-¹ÜMh\x0012®Û$É$d¦\x001c=lÞ©_G	´-&o\x0015¯È\x000e-xÞ\x0007\x000e/\x0003gû&·&!L&!W\x0008\x0015qù\x001a*^AÂëÀ_2ïMBLB\x0016\x0013
5^»3pÚwÐÆvB\x000efKJ»"\x000f\x0001¸æ½ÂluA\x0015h3"#\x0017³å\x0007\ÓØ
\x001f_ÂÑLhNHNElÑÞ\x001eÉ\x001eÈ?G°\x001a\x0003¢\x0018^äè©¨ÌÙÖ"É"d+\x0006Ý\x0019\x0011²@2aAã\x001fBNi«qrE®lãäU \x000bõÞ#k¸É\x0016÷ xunÂÔh
6´\x0003gi-%xdÉÍS]ù\x000cWd¸$Å@~YN\x001c·bÉ>É*µ\x000f¸\¡\x0003\x001c9õ\x0011äþÑô0ÙÊÐ!l5=®ÐãÌ\x00189¢ò®(&Ð\)
É»Æ×\x0017«þáÅ/\x001e¾{xóþF%G\x001dëÅy¦AÜUò\x000fñÀjûQ÷dÕs\x001b=û	ÞÜâUU\x000ftLbA\x001c§ÖGñnöÞ,¬K"zM@à©Ý^.{Ooî\x001d\x000cÎcý.\x0014¿g\x0007-\x0018ïÝ¼Y®?§ÊÊÈÚ\x0014ê}ñí¾)1ÍM:\x000f\x000bÂ)AöÓ\x001eqÞ»yó$BÓ=ÖìéQv9L3\x0006zh¼qóòT$Õiµ£ñ×ê¨'\²øc\#õ­\x0004·qô\x0019\x0003ÉÐe\x0007ÃÑ6ûZ&ä­U¿\x0000\x000fé© lh\x001a´pÃãTÖ­{åª\x000b4°Ô²\x0006©°æR¹[5û©\x0016Ý§7®ÊUWhè\x000c ³Ñ
æXu`iNÍmî\x000b4\@íÔ\x0003Â­R\x0018óa§cç\x001bOiU®ºBã\x0015L¨\¥ücn¨³3ñä5º@ÃÔ\x000cMíÂ^'OÒqjIêCè69\x000b0ôZÚ6þØ@?m
f¦ø\x0001ûWî<naÔ·\x0019,vCþ½4}Ã²?» ]ås\x0002½Y«É@«ÑOF©}Ã³\x0008ÚU1ZR³©\x001br¦jTSÒXµ«®Ðã*z1K`ISd-\x001eÍc\x0011²ëIÒ³\x0008ÚUQ\x0005·*m5v¨³ÂknÖc#ýpA\x001e\x0017Q\*.Îõ¼àX´å\]r¦'_Ï ÇEX\x00073[_Â\x0005Ö®£×³£gÐã"zñE\x0012æÄã$þ³-Óª/ãvÏ.âÐ®:ü\x0019ïK¦é{²Ó~z´úØÃ³\x0008ÒU\x001eºÏÔÂ¡Îò|3mLm+>»C¸J«ûH
Ó3Aû<ÕWC\x001f3yv\x000fA¸Ê]tfòª#AW9\x001c÷½,ìÎî¡¶ç½wùQÏô/;Q¬+ô¸b/^k@\x0013m f.\x0011Ms<6#\x001dzÐk\x0013\x0006\x0015P5ÓD(ôÒ[êr}«ÞÖ\x0015\x001a:\x001fA|ÌUÂ42\x0017¹m;îÙ5ô \x000eP3Ýp­ÝÐ
ÏYê¼]vW<È\x0003x¢±k´¥ìRÅîB\x0019gÚC#¿8b°Ñ¡V#)7§=é\x0010'>;y¾À=¤þ$u¤££«ÈMä#7ºéÙñ\x00185\x001b\x001c\x001f¸!±½³õj£k/K8ûa|Cø
Ô0Í\x0015Y>Ñ|\x000fÅ(Ù³zªc=5Ø\!\x00106×!GU?ñZm^Ø LÓü¥F~oÞ~¸Q\x0012RÇs±lg¹e*õ9_sgÔÀí\x000c¿ÑCk²A~ðEN~ÛG·eóÜ&þðâÏ?þ?on$û^\x000b%Â]:æø Ý(\x0019~C§\x0005ÝÑ\x0007
rÕÃ&°
¸)å\x0013Tïx\x0000µ%$$\x000e8ËCªSí5OkV¶\x0006m¡2×Ã´á	#t±èÜ\x001b[rí»õ\]°ÇÝÏr÷ÁG+\x0017-=ÕJéÊ_AL
Û\x0001*{K­ü\x0007wKtÀò#µu9Å³eGXvt$jX+·(Z[yv¥ØÒ¶Ý~3DÁÛ\x001f®ç´ä¼¯3\x0005Æg*OI<\x001d:\x0007d5¶
ÜÁ<8±Ë\x0011SÔ9ÃI'Ês¢üØ½8îV~V\x0007w\x0006IT\x0006zU»¡Üq\x000bf	\ü»\x0006¾@îà\x0016W\x001e@´SCR¦\x000cL4>\x0001o!·\x0019ew\x0001'úÃÞ"JÉIÑì\x000fa÷\¬ªã`{ÀVJýè.rÅ£Ú²¿æ1ª-×àÎ\x000eÃÃ¢­iÊÝá´±Êrn®ßÍ\x001d×á
gåÄ`~ÔØ¶XäìsFø\x0012Ç ¸6Ø\x0019\ø$VUTì/Ûáô\x0017p\x0018Mï½ãV1\x0015,AÂ]ª4\x0008B¸Û÷ÜðI/àã-ôòAqâ®É\x0013_HN^dðËàûÍ£\x000e\x000e¬8¯U9è;TuÄ\x0014XÊCÛ£´q|Î°îRðê\x001b\x001d
Ð9N\x001bÞNa:;	O¡¸´¬}é[\x001a²´Ùv×\x001ds¥c\x0003sE¼\x0010\x00033hqffiHµ­øí6$Ä\x000b8\x0010+8¶\x0002\x001eø[Ä\x000bïb/åìö\x0014´´%¡ò¤nJ$cH\UùýÔ3RÁ¤´\\x0017\x001cÁ¨â¥úª\x000cîz\¼ñÇ/à°ð\x0014=h(CÕx·\x000cÞç^'¢ýá\x0000O\x000eE3Fôm'¥\x0012jÃÞè½vì¡)WÇ·òú*çHz¯*¶Ëm±nA)úøBûß>¿º(\×È®:^3\x001eå?åãµ¯}OªN7þ¤Y^fî=WÉtÈ+Y:Ì\x0012g\x001ajÓ"ß´\x001ew`È¨6=ä0ªI\x001cWOF_{ëñÚfÔ¡\x0007£0êqjÅ\x000cK~rÉ:ÿ´­ºÂª\x0007\&O¡µË;$ÔîO°-\x0016PBF³ìÜK*\x00046nú\x0010µ$öÉ\x0000!7¦\Ëa
Ë\x0011j+\x000c_µ>á\x000cº\x0002ô¥Ëæ°e\x001a³ÍMîÖÕmïÐÎðgt\x0010Åº8Í\x0006\x000fi²lÝ\x0013;Ûk{­44¾L sµQ	\x001cþ/ÛAË\x0017lÇgdL{Ó±ÅÔ¯/gd¶È½Z¼éªïØ0\x0003U)_ðXo(Jjµé)éoà\x0019vAl\x0003¼,¸xnPb½\x001c¹Àý[®³¾®ØÌÈîT%ëÕÀ>G\x0017Ú?;'\x001eÏjÖGÀ®$7°íì>¶N\x0013¿ú½\x0017l¨EõE!1UXã|\x0006/Ô«gzÁ\x0006Õúä
ê:¨Ã^1i&O©´*ßL×ëÐ\x0019 m\x001eµ%Í¬r7Öé53M1"¬.A\x000e\x0006N0×@Oót+§\x0010&67}È\x0000\x001fRÙ\x0004@{uÅÂ
,\x0014©MÈ
½ÑuèÐjMÚ\x0005±nu,\x001a\x0010yØ¸D^\x001dúlÕ\x0001\x0008ñS]vÔæ$®\x0003µRÈ4i¬°\x001f¸bØ\x0015\x001d=çµ#¿dâ´+\x00196â\x001d;C0#=Oå]¹\x001c\x0012Aû®â\x001eÏ¬k\x0004ëª\x0015¶Q5ÕV\x0002¶$ÑRYLB°®\x0005|v##ÞHciø«öPÉ-N\x0005ßç¦mIÄ-±\x0016ó¦\x001aQM6$r}jMÛ±\x0013î	É\x0016¸F\x000e\x0008ÍwÒ×>mu¥/Ø\x0011ªö\x0011ÉiºLV5òÜ{C\x001bÎ\x001c\x0004\x000e\x0018ÌX¨¼\x0017
o
}Q2Ng¾C\x0002ßA5ÆÌx\x0017jaî¼êÔ§¢½ÁÐf\x0017å\x0012¡Ç\x0013Ý4\x0019ÊWÏØ¥MºÙD¡\x0017lC\x001e\x0003\x0012íP¥¡Br\x0007ÉpGÛØùÌSË\x0005·$\x0003ÓÅ)£ÈsuãÐFü/g;RpGb\x0002G^Ìt"¯¬Æ¯hëýNÝ$®Eÿúÿü?$ÖR9Û\x001buÞ\x0007ãIÓJ¼ê1ZC_!Í\x0015mÈrWÑV\x001c7G[ë×\x0013¯YNÝ¸E\x000f\x001aê#ÈcËÍñiË\x0017º\x0000[\x0018±¥BçP\x0014\x0008\x0011c\x000bÏý\x0008©´ràFÛ9ÎÚÎr qÐLÑ¡X(ò$Æ\x0007­^\x000cæÙÓX²X\x0016\x0014MQu[Nk
±å566­CWXµâµÁGvÆ\x0005ÉßÓI\x000c× !KÚÊ
U\x000c\x001dªGóæ\x0005Þx^
\x001bòõâx9ìK®äeæFíc\x0005w¾hÃÆ¡Ò»1Ï\x0013y\x0004ÛÄ½§)¸¢\x001d9\x0003rEîæ×ée\x000b8\x0018/Ý\x0017Ýø\x0002
\x001b:ð\x0004	4dÞ§¶A\x0007vÜ#-µ\x001aú\x00196¢Ñ\x001a\x0003DqW£ÝÎyíØ«\x001aç\x0005»\x0000vÁÏ¨5Í'Î³*Å÷)['§$¤²ß,$2
GC>W\x001e£$ßÒ¸\x001d\x001bôÖ.ZáX}ñuªÑýe«¯ÑA_Cu>Ð15ç%¸Z\lú¤òcÏ°Ç -íÓKðb\x0018öFun\x0013gVR£\x0007¦u^ZÇN\x0001f!y\x0019iÇiu"-	´º\x0001<ÙUüýK÷±GRÝ3SÁh3¹Y\x001c1ä<\x0005SÂ¶i\x0019é|f\x00023ÀâPÁÛétG©\x0017¬e·ÎtîÚF\x0008ã
[Rä4CuÁÖBD|õa&fC#	Z{r\x0006Û\x001f®}\x0018Îäæ$\x001e\x001eºk"'\x0007x2íö¾·¼¸ÞÀ]\x0004ðd°ó2è´Uà:Ë³/}®ï¦'þ\x0002\x0000<ÐØ,qÚ)»\x0012\x0012\x000f£Ì¡1´nã¥wð
àâ;@
$Zæ*l9Å\x0017lOyîr7
\x001cr7:ê\x0015ÇN¨"\x000bñ©Ê%Ï^ÃÞ\x0005æ
\x001b\x0002sÁ\x000eéïþf¡ý¬DÀÆ>y\x001dÚ\x001f®ØÍFÚ<5Uï9\x0006\x0008Í;Ñ	{ð<µ¬,ã\x0004\x001d¯rÊaO4x&O=õö_ù\x000c'Ø\x00156%SG¼Ó\x00046ljÐºsÍ\x001bjPn½1SÑåÝß<¼ùæÃÓ­ô^³õiùå3\x0001ë®N»ïLÄ}ßBºQÜ·LÁO*\x000eO6\x000bâ¹\x0015¯÷E\x0015Ô·Äð\x000b4*ÉÚJ¼°\x0012È|zÕV`óÙ&¯®Á\x0005:#4j)ã\x001d_Õ«#èÜ\x0003î³
A\x000fR¼\x000e¸kNð8Zµjs]IèlG,ìÈÉAúè!l\x0006èdÝ\x0016}êè!Ñ
\x000eÕ|
Ö×ÞóíØèùê,¸!£¦\x0016¾9fÃïðtôµ)Ym<ß\x000b¶C_\x000c\x0007ÆÈSÅï ¯\x0008¦M\x001e\x000bë3xÁMÎXEö|õ½°Ûº×WðÀ_Ò¹Éøp¿±¯¬@ 7´õÒ#èÍ\x000fãcz\x0007zNþÃÑä\x000c\x0017\x0002úÔ4o¾:Gÿj kÍ\x0013ö4e#¥Ùs¯³¾:G5ÐK×<Önh`~A_þ\x000fªFÿí³Ø¼ooú\x0011ç\x001fÎ&6Ùy|âÉqm:O®%ïÊè§º±ú\x001bu ÜH \x000e$6B\x0004\x001eT¦
ç
É-äQÚ£\x001fÖÂ^\x000e£°'\x0011\\x0006c§~sdÑèZZièïÈè?ù"\x001fû¼&Y/È L×Dr!\x0011ª=L¬\x0013É4¼h¼Î£Ô±£$v9CÓ
µ\x0012£Ð}\x0008\x000fZ×ÈªcW\x0003ØÉ¢¢ºæ´1Ío]lj{PêÆ0wl]\x000cª³\x0008\x0006NÓXÄcÍÌ{\x0014§³óÍN\x000eKpHE^±åõð·âDÒ~×Üú>\Þ¼à·\x0005êÚ-?Ú3¼Ée"à2\x0001ªè7Qóæ7Gã\x0011y2Ó\x0011Ýã¤x¯ñ	Ê\x000cFÖJ*²o½ce­\x001bvp¨\x001bú6u´ý{\x001dJ\x000c¨èÉ?P±s;[yÀ'\x0007©\x001a1\x0006\x0016Ù½\x0002&éÒ­~X\x0017ð
àÖÑÊM%¡U\x0013(Å$»Ò\x001aµýPÝ±P­ÍVÐ`(a0\x0007³f\x0011CÐêõAñ\x0007åE³Ý/ÔßºÅÍ}¥µ°^K 	\x0007ììïNê¹µ|£e~lÑü9ÈÇÊóH
×w¾\x001fù±%Z3Wõ\x0015¬QÈÌ-±J[¡ô+òhÔT1?è[MÓ8\x0019ÊIi6w+Z¹´² §Áz&à4Ie¼\x0015-ÈËhÚ¢\x0019g\x0000fî¥¬+s÷f\x0006¼L¦-J,Ã±kK£%sÇ»ø[a÷¼¦-h)GnðÄÛlÍvÆT^FÓjõ\x0007Û«gÚ]É|\x0013þjÁ\x0015y´hªT"°ît( Õås%f;-í·Éeê­ÊN t4­ ¥sé\x0019¨³\x001b\x0008ª\x00059átlØ\x0013\x0010GG¦I@Ò3~gÈ Z,
\x0012T.!OÇ®O\x001c_5\x000b®Èã\x0006êÀy¤d ù½K97ÂçZ¼Bt­84-_Z!ðÉUH×z¥7Ñð\x0005\x001a´C| ÁrmÚ'¹\x000cîþÌ¥#ÝCT-¨È-³ªðJ\>Õ}¦GhqöªZp\x0006ñ\x0010k°
µhk»4sé\x001aÆg7\x0011U\x000bÄëã]«#añâT\x0003êÐgW\x0011T\x000bäE),Æ¿\x0012·E½Ô;ÉNÍsÔ¼[.T­\pëS«lÁ\x0015yÜÄd\x000b\x000e\x0015-Ú=ÈÙñ{²vU-¸"Ãdk%hÁ¢Åù$ËäëDb÷½'áì*jÎXÌ@\x0006\x0008Ì\x0007ÖN?Ztî\x0014g7\x0011D\x000bÀoXµc\x0010uê ­ùÂO=» ZpâP}Ì\x0017ûËN¶à<.¢£¶,m\x0015§Ý°&MÞ¶ä³k\x0008¢\x0005^ÉÐ¸\x0019zé\x0004\y¼4![hkä\x0006Â\x0003eÄMæ5ýØ®<íV\x0003mX³ø\x001dØ¬¢\x0005åilW[ôª+p\x001eWÅ(ß\x001fh\x0017r6¸w|\x001açX}«S­Ò\x0002WhhKO\x0008Sà«~ èbfA\x0002Ï Ç]Qu6pvöNaC\\x000f6ÓÞîU\x000b®Ðã²®u<\x0000®	ïÀ~Lm©ÉìE\x000b®È£	XÃ?¤¡\x0014C5$«9\x001e{»¢¶"¿=^ùÕýæf-0³Þ¸<ÏÇ¼1¥­ùa«¬ki¡;£NF¯·xÖ\ªJKÝå4\x001av­
¿yÒü*©\x0003\x0000ÆRyDwNy©kMï\x0002ßè
n12QiúA_1Ùf\x0012ÛÐF<R\x0016SÝz>ì&9×À-0 ­N\x0003\x001ebã­úÉÊÈ\x001f#îª8\x0014zÜÇççÇÿþ?<?|øú6'7ÂE\x0005ñé¯Dv\x000cV·U£=Ü×¤´}%qÓAÛl^è \x0011!@!Ù;\x001d$	~ ¸EÄ\x000b.*÷¡Æk/lØ~ä\x000bK\x001b8
jr\x001f%ÿ\x0000³õÅ\x0007?aëwlÈº\x0015í\x00167½ÛfaZsÚ:£~S$êÐ£H$>c@b°\x000e>@2Pf°çlZKcÜä~\x001bv\x001c¹ß¢cZ \x0006ZÔ7ÆíVá\x0000ZvMhy²nH¹\x0015ÕøBeØ\x0010¶\x000b¼ÝÝiÛÐÞ/Ø\x0019Ö©´\x001aËÚÝÖp´DrmOÎIc"\x000e0\x0016ü
K¨¸°gèVÛLNº@WØ\x0012\x001d÷\x0004W7rã\{n«Í)õ©L«Õ¿`]"2ôjð4<Y\x001aÅR7ÊØÙ)Iwd\x0018O§4NÔPKSÅ9ûö!Ó¦Ô¡=Üwù7@qY¹\x000c]YøEîh\x001b&uv'\x0013ÜÉ¨ºªÎ\x000bfÂÊ
Ñºå¬6_ì\x0002Øü\x000f]yü¿þã?ÿáßÞ~øþáFJòìí©üñËÏ1Í%uE;²÷'®ÊâPÈVN)ß$\x000e6ÌV+¹L­Y&M²2-µ·¸îWdhßSÉ<$¦O\x0002Ó¡UQmÊ÷<<÷°ï¾É§dBFr.½8îWdÐÈT)Oà¦Gæ!jk*#\x0017³9°ªÞ\x001f\x000e©üo\x001f[ËÃÎl±<Í·Sq.éO\x0017 åI\x001cÅ>?ôÎì'\x000fÑpKÂ;W'½\x00177ÉÍ5)UóÑ-¥\x0004Õuõ°gì¢OÁ:Å¦7Î\x0001C1Áã,\x001c\x00016<4ÝsFìOå\x0019.\x0012t\x0019\x0008ïÉ¿]¸À\x00199½~WK¸"C-Á'ÌCD\x001dqMyyæ*jË¶Ýeü¯Èñ÷\x0019{øcFæÊ^±àcíRî«6óò:4ª\x0002´ìé`xnI¥\x0015\x00136¿nÎ\x0017qÓ\x000c|Áä¦1ÏuRe´;Ã\x0010¬Ý¾dÿøÍë§w7²
VÌÝÔo\x000e6LU\x0015\x0017l¬-UWV!)ïþoZ\x0005ÙJ¶
¡xj×5:DÌªå\x0004W­t\x0006||ûP]lnË5#ÿ=ÎQ1~z"sØÖ¹"îZñsÖ\x0014ºer¹ËÀúº\x001dK~E\x000ecÍDwu¶\x000cz^6UËùZ³vqE\x000cD»(Ö#?vIZ\x000fàìuÎ;ËpE.°æ½\x000b:/\x0012r©F^s(qk\x0019.ÐÀ9R¥\x0010²ÍPÀa'W[N·á
=N\x000e\x0007\x001c\x0015L9vH¬VÕpùØ5uµúuÆDÞBç\3ÝøÍYw/þñÝûWßþp+þ!®ÕÅS1¼5M.â§é:Ù
	::\x0013æ­UOÄhk¸t\x001dËy\x0006<ÌB(4hQb.¢Ê \x000b¯ÿí\¬0;\x000cáÚ.} \x001bdK¨®%àØ[xÎHPÑAö'6\x001c«eÖ:Ï'$º
[4µ"*\x001eÕ\x000f/~ýöÃë[M\x0013yÒlÊ;\x0017^\x0005ëßF
Þ\x001bSô&LÉ.Îþ²Ø\x0011h0ÍªS\x0015¶â¦\x0002}õÛ¡sWdpB¥ò65\x000b´\x001e®G¼\x001d1uE\x0006_|ÿ9>ú)wOã\x0015\x0019ñ`ÐSUÌN3gçsÏw\x0001£ÏLj¤9\x0016\x001eÀ!î)sYúXîµ÷ó\hÉXÖØ¦è9,íJsÎ»\x000e>³©þ±\x0012R²VW±3´IÛñ
>³%S?é÷\x0014Ö<Ø»SNÎ¾!òB*J1Yuü)RË\B\x0017èË\x000cê3hø*×\x0003\x0015¶d¦øÄ0S­äî}F Xè!\x0006~½<4­¦ð\x001dñIÜ\x0006qAFù¨\x0018­Ö\x001aß±,Âx:ûn\x001av\x0002)Ì\x001dä.{&ÊêÝÆ´°D>_¼~|zóâ_ÞÊÿz}+GÄð ß\ò\x0011ûèdû
¶Êô¡Î÷dàårm,ü¦³/I¾.(=#\x0002NÜ4ñrfù\x001a³\x0018·]Z\x0017èé\x000fNIW0þ'äÆä\x001cÐ3Ú$£\x0014½³U.¼j\x0013ZMÊDNp\x0008>ôzãÉªAT!8ÕóC*+õ/\x0018U~ èx)e¬ÚZXµØHïB:Mfa\x000cí'î\x001d¿'È@ÖWi\x000cX³°è#ý×¬ÚF¿¢CWC\x0007\x0004d¸\x001b96$O_1§}¶lú\x000e')¤i\x001e~F^wïãÛhBwl\x001düKx¬%C¾)3·°^ô¦O¶\x00044÷´\x0007¤Ý*aß\x0001o\x0014N:pÄ\x001bSñáS\x000f\x0003kzÚ¼Î
'®\x001b?»ènºèHãÔ.îDß±òóäÚóäÎnºîUÂ\x0003,¤|V\x001c·d$@çu÷i\»¦í
MÛr\x001f\x0013Ñ-µ±ÎvâYâ\x001b5NÌF¾¢c{Cg\x0004ø§â\x000c\x0014ö)C¼Ó8éÐ\x0001í#ºG*foh»Ý¤ÍÎÄB\x001a4´LÊn{\x001cO3·ÊnO\x000cÃ\x0016\x000eg'0À	lêiN¥/Ít\x0002[Ë¦\x001a~Á\x0013èCK³á\x000eZÒ´îFAÙt]°¡¡H«Êø%+õüZë´ìf\x00007Åð\x000eþ¾&ä¿)Ñ\x001aC\x0015«
Éìè¶\x0003¸Ó®ëØðØO\x000cÄÎFè`xG=®»@CÄ®M£v&MNc(­\x0018¾\x00118ìØ0>Aö\x0004'Âå\x0010ÈNY9ÝÓvw^ÃÙÅ\x0001Û·2T¬µ;ûÎLâ·Øg{oD7:6¶©
!Þ\x001cà¬õnÂö{~À\x0005\x001a2íí\x0006\x0017=\x0017~\x0016¬6ð}o2À4´lJëhayÚ\x0012>;%	NITª\x0016\x001cî8l¹\x0013T,w»8éìLðLª\x0018\x0013T¿õ -ÑF¼éN¶eÀ\x0004&0êäd8ÜJ¤Â,µ3SQþÒ\x000bsv\x0000A	G¶$Pµ¤gª*.\x001cæ×¦\x0004¼ð¿`C£©\x000e\x0006i4m% ÝvÓ²[[w:3®)áù³öP\x0001He\x000ep\x001aöq¥nÍQ[Å´±»O®äÔ\x0001Òòé\x0000Wèx¶!ªdéF:ÃþD>»6\x0019s*Ùrviä&Ù»LåLò±cãÙ¶øÞ$\x001e¡;³wÙ\x001b¦VZÍ\x0005\x0019Z³\x0000
oçKjvw»ÛíM/ò\x0005\x001b_÷RÙßö/iÕé\x000f9·þ|vþ2¿ ö\x000fãÈÈ\x0002ûÖø)$k2wùìøe|Û#V3lÊr\x0014¦Îi·Ú6äìø\x0002¦¸
CTOÍzVý~\x000e$uÕåìi/ð´ë\x0000:\x0013´q\y\x001e@Ú¦röø\x0016x|½-T\x001e'7Êqv,·\x0018¡¾\x0002¦OÛ\x0013*ÕìýM>Cö»VÛb¶,}ûáùÍ½\x0015%³<n*\x0007?\C\x0000\x001eJÜUºÆRv³¼¼ìäÜæ\x0017
ôj\x0019äÙÇ°¶³`Op\x0003äEe\x0012:¹ó@ìÌ.á½¢Î\x0005\x001aäÁs­hÐÉÜ(ÿ\x0006û\x0001¾Uíju:¶á\x000bÕ\x001bè(j(ÏUSa.û®²\³\x000eíAµNà¯.êbF&uÔRölæ\x000bt\x0001hñÅa6¥D°TTöò¯Mâ°jè]¤köúu«{ýüÛ\x001fÿçûÇ\x001bM5\x0014GGLø\x0017Uz\x0003Dý¥\x001aÝ°{ºgÉ¨ò	D±8Uh«w\x0010uü4îP®\x0002Ï\x000b	ÍåÞPÅâT¢­.Ñm¨<gBöS%5´ÚÆÓ\x0015§\x0012m\x0015W\x001eåqs¢$ 27æé)iSõ¯pªþõùá²in$\x001být3æle^Ør0g_±é¸ó.îépuõRþ¯Óá5M9\x0016Ï\x0013³k­s\x001dq[U½";@®HëkV\x001cÅ´TrrKÃYP§c+\x0016éïV{ÂQÕÉÕÌAÍ´RU.Àãá©QN-\x0000çÀÝÃµföfúÌ²P§û ÄBx\x001bZ@niÅÈ/¦Ì$0\x000eÁw\x001fÞ<½£ÿZOÖq?.ÇðáÕ\x001f>Èñy|óßûðú\x001b9êß=<s;Þ\x0008uþ/¼&Ç®789PÇÓn}\x001bI9ND¨4¡J¾Þõïß~ÿAþ_Oú\x000fÙp\x0010òþÖÂ>ÿNð\x001dPzç-ûòR$¾ìÐÏ¿}üîéÍA¼úæõâÿuwq¶\x001eáãÖC\x000c;åÂ%\x0008æ2n7¨õ\x001bl\x0015\x001bµ\x0017Ô¯Öc¿;ÿÿY\x0010YñîyZPûR\x000bªþ@\x0018ò¦?¸tF\x001c¡esú¨\x0013èc
HP}ÑA¦Shd\x0004Y1\x0005
-Næ_CàvàÝP\x001eûÂ\x001eû¼#àµø\x0006K\x0011çî\x0012\x00034:ÝA±²­9Ê¯1À½\x001e\x0000·|%ÇíÍm8Ðhçµ­³\x000c\x0014Üdk*jáëÖ´ 8\x0013èT\x000ehñuGc@«©·\x0008M3O²*\x0013ÏÂ-®\\x000fÀ/¾Ú51|æ×\x0017
Éqú/×ßàu|=~æT6Sòþîßß\x001b]Õ:Óyµ\x0000¥G>\x00058û\x001fÝõ+Ù\x0013[ýðâïÞ¿ýp+k\x00029úz|<|8®Ëê°fîícå´ë:Yîªµ,a%þ»\x000e\x0011ç¦ªÉÁñÖô¾ÅV_\x000fU\x0017u\x0019üKØ¸@Âê²é¼WäóW\x0000¹\x00022ØO¯®\x0014Ì=Rdd+rKBNè\x0003ùhDÿ\x001c7gsl1ôåc+_ÿÅo\x001e^ßêè\x0006}mÑÞ%®Q]!ü\x0018g×ø÷ï~lSt»î´|©\x001eP\x001e*(Á\x0014LéZokÅy`:ÌÒCZ¶Ø!û¬,¼ácè¾!\x0003Z·\x001c[\x0001tËûD\x0013ä0ÌbcÊËæ\x001c\x001a\x0005ìË\x001c\x0004+nÜ{/ÿüîÕëU{ö3\x001dØè\x00029R¾Ín?Ã«\	\x0013&\x000fÅ]ú/j\x0012ãd\x0012}\x0015§ÂÁï»4½¡	ßY\x0015TV.- §\x001cã \x0016\x000b²jh:BÆ w
_\x001c£\x000b´/\x0003ZlÕA\x0004°M$È\x0013´ätûÐ¿¦ôë\x001e±_{óN!Î×UdËÀefJ
ª;}Ëýã_ß=¼ùæVoy¤¬j.bÅëñÖE!²¾>îûÞ\x000eîÞ(Nâ}OõK\x001dâÊ\x0018Î+«3°Î/Ã¹í#hë\x0019r\x0005ä\x00043û\x0004Ù\x0013¡Z\x000bAtÛ]g\x001e.ÏyÇ¶ðKùí¨¦­ØSÙÁ¼=ag÷Ã_?~x³\x0019~ýn½¥¡s9«UôµñÂGÐSC×âý\x001c®Å\x000cÈv¶Ãu5\x0003ò\x0003å3\x001dÔ\x0003ù&!÷E}~Ç\x0001oi³\x0015§Ã>j\x000e\x0002ajî\x001dÛE¯]õ´íö2]}1\x001dÛ\x001f]\x0006bÌÓ8ZÚÖç0\x0012^Ü Ææhzt¿~ûôîÝÛ¥çs\x001f]ùÑu¹\x000e#¶>\x001d}fø½\x001d¯}Ò`ýL\x0002\x0001¾_f(@ë£[×^\x0019Ç{ã6ês\x0003Ú\x0001´÷/Ù])lüäêø¹Kaýæ\x0001;käúÌ·ËÎ¥\x0018ºz­9\x0004\x0015\x001d;$TåMÓ\x000e«>ó~~\x0017çØ5
8ýÃñ\x0003=ÈOÉ/\x0003\x000e½l\x000e\x000e­ØËö\x0017¦¬¯WÇ.ãõØ\x0012ò\x0011^g\x0011¢bó»XÂîÉ;+ðN6ìáéùéV··\x0005I¬9¥k3ÁõFe%\x0012ÏM\x0008éÞ\x000eÁþ±u½ª96Îý0ÖE+kã\x0007Ê\x001bJC[â!{cò³ëóÕ ç+ø\x000eöc¯Í¶N¹?v\x0000-\x0006ÆÃwq¤¯b4>À£bvs¾ÊÖùâùÇ¿¾ø\x001f\x000fï?<?.ýDùÎètÂ)	Wc©Âã\x0007Ë_¬¥);-¿û\x0019;14f5\x0006M¾É\x001e¥7ýá%<¤&"«J6'§)ºksIí¸@¤Wå\x0012(í8Kãe\x0004»NXõ ô\x000eËAøíÓë×\x000fß<ÞÊÛÐ~XrÙ]kÔë\x00063Á<~GPÍ;,QygôhÎ ,!lh\x000biGÈ\x0011k\x001aHòØ¤é±ÉqJN~\x0008Ìr\x0008:¶\x001dA¾øªqä=éµL]AntT»&T/ÀPM\x000e½dù*\x001e5öµ¡>ó¢Ko,s\x0007~Á>(£g\x001fü£gE¡ýS½@ûSMÞ\x000c>¾UÁ4²¼ÊÈå½öÖÓ5WwÅ½Ö\x0016YØ\x0012e\áº%*åmk6Ù[\x0003:
!%ý%ÐeFdÏßQBÞ»¼rWè\x0002Ðñe°jêSê#\x0015±\x0004»u\x0011lÜ¨\x000b6¸Q*~`--;\x0016Â¦Ò`÷éål·\x000bìv	CgG×Í\x0011`"¦¿B÷Îçr¶%\x0005¶¤ä![¬ÐÔlgTÓ{Úîe&{+\x0018Ã\x0013úÏß}ÿðnÐþA¬Ó7oßßè	
Ô««väGUÈë8ð±Í\x0016¼ÃÜû>?º)ÂGRÅ\x0008:xèÊï«S¡rªÑÕ6;q­îÚ%\x0008t0![w®Óo\x0000\x0019)BÜ»P7¤\x0006}sÐ\x00120i]NI]}iín«QWä
Èe°S\x00059\x0017º\x0015KT¯ò\x0011£\x001bÌîè¾{ñ³×\x000f¯¾múz·Êí'ùìz?È)J2\x001fîu¡õ®ÜÛÙ=	1×Hv8Ê}\x0013ûgmÂùÊÜä¢9×!×sÐ]\x001dÈâ9ãÎY¤·é®;>\x0006]Í4­9Ãu´B\x001aÐÚ½g7Ñ)qâ6u#v'ìû¹	øà¸úÚ&l\2½òöûíë¥]öÞN×ù°ºQ&ñàÓ\x001føÑÍÙ|©º}ÆÞ½øÇW\x001fni\x0008>Ñ±ÉÉäk\x0018(&+Ö'ñæ.Ö?/µr:\x0001Ó
ÒÉ\x000füèæìjý[«}-öË.ÝPäræìzºòÉ|-úNÌ|\x0011£Þa^h\x001f³o*ò\6õU³GÏþ¾òÖmê^ö¦µ;¬$\x000bU-\x001fÐM<\x0000´Gq\x0000-jäÊÐ~w\x000còîÂ~xñ«?¾}ºQíI\x0007*p\x0019¬MºÄ³à\x001cMÕ\x001c¼ÇêÀÞå\1.\x001dtÒ;øX¾ê|c<R\x0008¼7¥\x0007zku»CÛ\x0000Ðeô/[¯c^°< ±\x001aG\x001eâ96Íõpuh7\x0002öè@\x001dB¿'@õT#ÑÞ¿<4\x0017è8\x001e¨t*¤¥ÙiÕW­cb7ç¶<4¿zÒ~\x001b9\x00043»®U¡¯¥ßÚ\x0012
ð^;¬Èï-×æ\x0008ù\x0008Ù!0Øæ«µí:mN\x001f}´²:ô Y»¹`2Å\x001d*Ì97GÀÅÓ\x0017ì\x001fÿ*[ [«'¬`WØÒ|?*vø2\x0003ï(.Û\x000e¸·p\x0012w¬%îÈ*Îò9\x0018\x0014Û«ç©êü*,·êÖJÏq\x0013=G·Î6aE\x0014{Uè pÄÏîÐ1ÑëxHËëX\x001dÃh¯#;%ÙÎ-·[÷G¬U6äýæí«ooEÿI6s	5Ù#©\x001d*hà);Æî\x0006\x001eüÝÏØÞ§]9`²­Ì\x0001;û\x001fÝMùÁd"þÏ\x000f\x000f²ä\x0017¿}|óþf©Ä­ ¾\x001e!Hm@F7\x0000qoëÂº¦j
5Ty\x0000\x0017W~ {i(\x0015\x001dW¢j\x001fó¸&¯
O\x001fTh\x0003¶u¶3@¾^d©N±¹GÅí\x0000ÚZ\x001c\x0007#Ð±Rþ$M)Ýo]\x001f^üëÛçg9]·r<R\x001e@ç«\x0012
Ðiä÷Û&"òÓ8\Ë£à\x0003ÏfÐß\x0017Árû\x001aýËB[3¹>-Eþ\x000c\x0014yÕ[	Ð1#sb
\x000c\x001dzÄ\x001a] =8K²Jt
iò\x00084Í.\x0014è´k\x001béBgÓáR}=3:\x0002\x001e/Ê^1\x0005FAXÙÙÚÞãÆÑZS¨>DN¡\x001a#ÏÌZÏ\x0004èÉæXOTÚX¦kRæ\x000cI\x0019£\x001f3l\x001d	/Ë¿À:Îh\x001fè_ ÇÙ2:¼rðËg\x0001\ý¢ZJÙq4,\x001a®/^?¼z|ñOýÛÝèA\°¬Þ`]©¶>Sõ\x000ec¥½û²\x0006â³É:ùy\x001fÝ¯i\x000ftaj6Ö­8ZÑ°·n®\x0004\x001a
Ã*¤b\±¹e÷ö>5¤uÇ\x0004÷\x001f!(0½fCANKÕxcå\x0000vèè	zP\x0005\Q"chNôÙ´7\x000cògÄi}~ÿôøüâ\x0017\x000f|úZü§\x001b1h¼·#ö¾\x001ctpå/\x001a8\x00061·øöÞÁþ\x0015Xë©§9èïà\x0002>UÂÉÙªc©/ÍwÝÉµ\x0006y&³±"\x001bgPAÊtN45øÖU\x0003} [H#G\x0007=\x000cNåÄ±ºì}ò\x0013~÷\x0004ø´;]ÊÏz|Þ\x0018þÌ£\x0015\x0002·¯ùVâ»<e6\x0001W¢åJÊ\x001d>\x0004²¿»	$«\x001bx,UÐâ'd{¦ÿ3ò)7Óæ4zÌ\x001a\x0017]# ×ß¿"[C½}<µ0¸´w].?X³õÀ/pâ\x0010¢$"ç©FÑH\x0011`.MÁ\ÿÞ\x0012<!òYávúÜú]7^Q2³Wä"2õ(%r¸\x0007§Çp«§°\x001b_ÜH7\x001f¾Ò[q+¯;TÜÃ$ï¸\x0014Zo/£Fäkÿ²÷v)ö\x0015\x0010»6ÉÖÆ`&6T\x000e¸Ñ^\x0007óàÛ\x0018[*sa_m\x0004\x001b:ô8¼Ö#ëÃ]G¾\x000eì\x0014&¾MÐqé\x0004[ÿ0\x001cïBË\x000e³ßMö\ÝÆøÕ\x0013éÐÞÁéõvèÃÚÖ\x0016\x001e-Ý9Òª<JÓ\x001dÓûáÅÏ\x001e:ûúñç1nãTüw£3Ñ¯ñ:c·®£·ÿÞWÜ¯²\x0011Z\x0019òÆw\x0013\x0006òA\x0012\x0004CfRn\x0001\x0014"^ì"±Ø	)Ñø(Ç`ÈBê(¹ðª s\x001dÌöDÇJ»iÈÎB¦cûQ>ò5\x001bðê;]=\x0001WD\x000e/'à<!Í`\x0001>MK-®
])ñã¸ì:#Ö­üã+6¤gTÃ
 óqíÛV³ó\x0011à|D\x0015\x0005\x001eï¥Ûtp­aF¬oZ§¡®¼¬]ëíaª
r\x0000­Ô\x0004]ÒsÞ\x0018 \x0006¡ºClm°\x0017hí\x0014G2YªÜ\x0012YBjê\x0019y¥M_°6£\x001d»-ÐB!®¡7yÖÞ\x001b<?Ì?ÿVSbÏ\x000fo¾¾]+!V&|\x0016[¨^¯'ð.³»GÊÃ½i%°kÐ*[ÚH YªÍ«\x0016:z\x001aû\x000bõÛÑîÄ\x0016\x000fÛ´¾ù\x001dûä\x0016l\x001c¥©Ø®s	~Ò»J®m:[wu×\x0000É6ù2\x0006Eõ«Úé«n×;wÁ\x0006N¬ºìÀ²,LOÐÓJ¢\x0001êÔ¶¡PëÅhØîP(Tì<´\x0015;]\x0016lÎÖHÂg&®c[ 6[\x000f¢£Ù\x0002]&U®Üî6÷¹C{X¶«Ð\x001f.Ð\x0018î%TêÞ\x0010ì\x001e lÞÀ]@W¢àó*ïGrgyiøêz°ëÒ°}áRÒh(NL3.;%2UbVJ:;%¾\x0000cVGÎCg.õaÍ¤Vß&ÃÙ\x0011	\x0006	³yr\x000b°\x001c\x0011æâ6cÀî\x0012èaCÆíØ@Æµ\x0016ªèCWo;°s r»ö6ì\x0018cfu:?65ùs)\x001bç=|N#û;fî¨N7\x0007wfÏ:ÊWLÏ&\x0016Û\x0011
*U-£\x001cps2\x0013#í\x0005«\x0002Õ\x0005º\x000eè\x0018[ïÕ\x0001íÑ§P»=!o\x001egk·QóÃ_>½ní7S0Öp\x0006l*àÒIT×÷v\x0004ö%ºÖ\x0014zoF=üÊß÷Ñ­Ù|¨møË·\x001fnìÓÉeÉX 6àbÂê.ûþ}hC/\x0017bçzzd\x0018ÇM2A¥Ç\x000fÌ,è\x0018\x0012§{Kk³Ë+õ®#gÈ\x000e0&§+rÄi§\rµ¦b.ÐÑÆôi³üËFÌM~½-ºÀ¢Å°`¥mG¦4br}%Ø,?Û,\x0013\x0013xâN{­\x0016ªçý\x0008OÕVÅ¬\x000e]!Ç£ñ<~DñäÒ¶¹Á\x0017è\x0000Ð	«ém\x0002|!è8mïº'm
l¶ªìKä]ËÔiGbg\x0015¯J\x001d;"¹Å´ª\x000f\x0014\x0017úÈÁ[¼-:-:E[MÙÂ¢u\x0007í5ýj'B]E\x000bWÑºÕ7E¦í,\x001bp`¯Ì\x0005;AòR'ðZ>|xÙr½¨öÌ{89}úÈZ×\x0006½òÎ/Ð#õîÄhX(µ8GÂ!>Õ¹`Z¬\x0011Ö®\x000bv"l(\x0014k-\x0002¥7\x0015·¤ù¿~Í\uh\x000f\x000c
'Ï\x001eôKÔLâ>OÇÏ§òðgçÚÃ¹ö&Py®pó§/&ð	qW¦ß%&Þ½øâñÃ÷¯ôõ¸Q­Nc«^é¸ö%ü\Ú\x0000Î;{V]m=+Ýx¹\x0014®Gà¡DbÝ¸p:B\x0005#posâ*}\x000eÝPl\x0018Ç=ãz'	´7Ý4¸Ûx\x001d1E\x001bß®¶a\x0017ÀÖL ÔÑ"åF½<6½\x0015«ðG\x000f7Ü¨|sd¡þ«±>³Ì[{¤¼]·\x0017è\x0002Ðe\x000cÎP 6³1°\x001e)½pa£é×ãÍ\x0008Õ¿j¡EÂÉm¡þ°~zKBØq°Ózá>¼øB\x0005iþíã\x001fo&²cñàâhSJ\x0011:Çzçñ\x000eCÎxc=\x0007©Ç\x001b}ò\x0003?º9»´ívFÕÏ¿}øþñfÒÁrp\x0002\x001f\x001cg¨Cv àÝtKïÐ>¨\x0000m²Z\x000b\x0011 dú¡L^ÔôvÈÇÌÛ®¯\x000b´c¦!B'GÁAôÄamOÓÔÍ\x0011ÐìÐ«·7\x001bR\x0011*3ê\6×Ní¦a1*\x001bÑªé¼ÃrúÉ\x0003¹¦ñê¤\x0003Ð\x0018Ñ\x001e²ß©èh.NÓ¼ÆMyï\x0002
R\x0013r<\x0014\x0004Ä&
T´ÎÁï¥&ê$|ÞD~Q\x0008 uÍ_@fíÜÆ¸®D\x000b²GM\x0008t.A¶Ôb[\x0002÷©)tË-:À¢m\x001d.\x0005:fNNBðâø7EMé¥2_P¡-D\x0015\x0002ípµ@gË\x001fñ¤{wknõðáÏ·ºj1ãH®¦Ð0*dÕAgX´zóî/	ç}«Ñ/LÁMón?[Cp­¦Ü2
G¡ÉOÕàù+>Z{F.:^p\x0013©Õé-Æ*©@§éF´ÙîÐï\x0002
«Î
D$Åã¢sØ\x0018Ú·\x001b±ju_ AæF»@#]¶È\x001b2Wõúô5ÍZ\x0007má{\x001chÕq¾lµ
¨^Ãì\x000e\x001d\x001dBÃM\x000b$ ¸¤ÿ¬7M%Ñ×,}Mp¡Ra4ó+
cm\x0003|Ï6#Áfè\x0008¬ÒühNPlã»Ö*Ð\x0005:ÃÁ+\x00112Qg\x001c±Oan\x0019|¶ê«ÎÈW
z¦Þ-\x0017Z-o¥y]\x000b~ÁLJE®¼¤íwÚ·³±ÉÒå)K'6Ì\x0017Ïù\jQñ\x001bE^³$\x0017d(mV\x0014\x001e\x0017äÈýf1'Þ\x000ey¨[þïdÕ\x0016;\x000ej\x0005ê*\x000c·\x0004éÀ.ÓóáâêUï´ôØ\x001aÅ¡iIfò\x0002Ä@ìZgãô4© èã»¯~x»aEí`P¹Ê\x001fÊ\x0012Féá4\x000c×[Lïìu:kgX{fy*¡þ>¬ø«¤dst½	\x0013=Ù²\x001f÷qÆq\x001fâF\T:\x0002ÝAÐq\x0013\x0008x·8'ï^üËÃWoß¿S?å·?þõÍ[)5$@\x0013·ìùáBí7ú Ö«zoÇ@nô^»\x0010¡/\x00123Àõ×~T0\x001a¹-\x0013'¯N]¾7µ­ôm7Ñ·](¡¥H\x000fbD«)ÌÈ35o]\x000br\x0000äq\x0006ÖF
A;ÊÅ\x0016ÛÜÒcG\x0006Ret\x0001H\x001f-\x001aDEã"7bÚ¦Ã·¾\x0014\x0017ä
L?ùù\x0019Y|\x001fÕDI|\x0008O]Éì\x0017h[ß\x0018>S?uJ!1cÓÖ\x0016x­\x0004Åm h\x0002\x0014\x0002tª\x0000õ<¦ÄTã";¡\x001a_Nìë·¯®ó9'ÇZÂ\x001a9\x0000×ÿz¾üYï»Üùxõ¶%<¼~ýaUN»îÓÇozCHTÁ\x001cÒ_%ë;¾müªåªÿüùÇ¿~ÿôæwûs÷ª\x0005Þ½úÕã=¼ëJÉ\x001bÚöçm\x0004\x0015DV3®}ë¶Y)èm>&&Ë?iZEñ^7ËÃÁúù·\x000fß}ßÖë\x0007YÅm6ËùÂ¹ÉU§Z]7KE^\x000e#kÔûÞ¤ïh³ê¼Y¿y»rf?oBð$\x001b¬»¶WP±Üú\x000bEâ^÷)YØ§·òê¾øú¿þã?ÿYßEÊá3OU )TJ¾ÞÀ¬^û¸QÙÍ4²;Ú¬BæêçÏoßµíúÇ\x001f¾ÙV>?sÃl	´a­û¬ßB-N¥ã\x0016\x0006ÙÊÖ©v·\x001bV7\x001böø¢-óÅu·1ô\x00193ó©P\x000e;/\x0001ì`] þo¸ãG1Ã£øÇwïÄ!n¯â¬¼ü{TtP'\­WJd8&Èg\x001dºïØÊ£\x0004^ÓìÔqa/\x001eßkýÃU\x0005ï³v,Ö\x001c]j×²h	ê5\x001cÉwÉí¼Û\x001dKx#ß5¥ÓwGÇ§ü÷Üæ%Í\x0001,¹l®¬V\x001fa\x001cR®½.r§;Ö9gÃéáTgXì¨\x0005]Wã%|;FÚñä7\x0015ûÙ­\x0008»õÅóÃýöíw7»J5Ã}
í?÷{è5\x0001xìü-Ý³ßeqù¿<>?·ÂÕÏ?Üê9Òã6ú|Ýªä\x001f\x001d\x0016¦ød7cîh«,]Àën½{ñ¿½ýúí×·òºbAOªÖ¦tø©Êã\x0019~j¶vÓnqG;æ6;¦ÿµ7Ú*íË¢­ºÊYì#\x0014De§ä\x001a®­üw´Sà@ü«lÓkÒðO\x000fïneà5\x001b97cSõWKÕË\x000fÆNÔécpîuÇ*x§¿}úæÍãÙPôÏ4\¶D6>\x001d6>\x0019ç[Vðÿ¥î]ì:,Ñ_i|+-ÞTKÝ×$\x0019*ÓàµÁ\x000e\x0012I ÁDf"\x0013ÌzZÐÓ\x001a\x0015ï \x0002Ò_Òî\x001eçìX\x001e±w¢CÕ <àBl\x0008\x000f.ßëx\x001b×æýsDÕeÐ\x0003Ù¯\x001f®/Ï/o\x000f²;hsµ
\x0014Ê¿í¥ò?P,\x000bè^7\x00074'#ÓèAÁE²ôïâêlþ;n\x001f®Úý/Ù-)i-??v?Ra\x0004_´XwîÙ³«.ÿïÎÆoïÞ^Þï®wWd`^<ùÃ\x0003\x001f»×ÇsúJÍèõE·xÊ±@«Æå_ÄnúÑRv¥¦,Çs\x000cc/Òl§Ïó#_õ@tZ \x001f®_^ß¿\x0017Bª\x0013ïv¯wG¼ÆF\x0007©i¡éðFD&=Î]ãÕ`W&ÔÎÖøaküTÝØæ7=*!aè~fùýåtþm6\x0014Kè5åÉ[âÖ½Ê¯8\x001f\x0015u)kqP¯N6®ähj%Ò;©eò4¼Èßß}\x0007)««Ï?4«wxþÓséîGr¨÷Q©±j\x000f~¾¯6§Þ¨\x0012bqCÒgv/_ðÈ&ç\x0002î Ã§\x0004Îù ±ý\x0017%\x001e|\x0006YS¦ÞP\x0019å\x001aK(\x0011Ü\x00028\x0013uôãFÏ¼j\x001dÜæ ÁÛDèº	¾\x000ckâüWì®åMSÚ.\x001a=Ï¾Ö!¾½òÐWnk\x0001p!ñ¤t¼(¡¨¦R}«à)\x0002¸êR:EAQ¹«\x0016¤¡c\x0012Ásçv\?¡\x001eî¹ªIawK-Z\x001f¨x(ïàAÆW:\x000bs;&bÃ\x0000yfÿrÍ{DÕT5
P)ÓÜ%÷tWncl««¯¯¸\x0016ô'òRÿ¨ÈVuWêá;<éÔNÛ\x001c2³ÔNÏÚ/¯"ZkÀãe\x0015\x0007ù©Â
\x001e[o ø\x000e§lM\x0017Ñ\x001a¦æß\x0004·ýAò\x0001§k³\x001a¤ÉS%µ¤Kdð¡;\x000fÁC§ôÑ\x0000;EÈ.+Sô8\x000bzø¥l5·¸Ç~9Å\x0007#@3ý]ØÌÝX\x001a¼U=Æ²
Þ»|ÎJæL\x0010Ü)\x001emZ¹\x001f[ÜÓ\x000f¯?^§ëù6pÀ÷îóÿýSÇýèu`\x0006&\µ0\x0013}6½P¬[	Èýò×¡f³Ve4ª&Á§Ôñè®¾y\+Ö¹\x0018uP\x001a\x0015?î{Çö}ß]\x000cxbS\x001eÞ¨g\x0011¶Üµ8Þµ\x000e\x001eû]s	Ò\x0004^tÑ²\x00037\x000e·õñ£¶
\x0000+Sû¢«ç_Å×Â½³sy±Â\x0006;4P²pÕªê wq\x0018øÝxwò¶Ä3H¼`\x0005iÈV¶»dí°ð*ÅºÛà\x0005Àk\x000cN+6t\x0007=\c»Rù
à½ön\x0016\x0019@	t\x0004!à¬\x0010G¶VQÄ2Ö¾"º\x0007­o±Õ´~Uóº\Ro}µF\x000c ;éÎ\x000eºsU)<ªO¤ût\x001b¼\x0000xÄÆ0²ú4K\x0002½W¹Û_¹j´\x0016tþ©kf\x000bcB	Nxf6jK	HÚÎìæ:\x000b{Z\x0012°bê®ÛPI2Â\x0016æÂ6:Ì\x0019
ÎÕ
rÏbAwtUrÀèµ1ÜgGÝò\x000c<'½\x001föóõ¬4¶&¥2;:\x0018ÍãÚÉÅ&\x0003Z»*Å­¶4ðMÎ?-àôô\x000e]ÚÔªXf\±^Üàé¹½L®^_­>·úüÃÕçÿüt´\x0007¬cå!\x0014!:<O8&¹\x0019Ò_üÁ
v­ª·¨PB»&rÞ÷ò ~\x0013ê\x0001!\x0017Uß	v\x0013eÖú&ºÍ ç\x0001¢± 	jPrºg4[!¹\x0003h³¯g\x0011Û¨Ú@\\x001a:Ê0K:7¾,\x001dÛÈ¡Ø\x0014bú`å¯pkYÅäro¢G\x0014JRQ\x0001M©ôCT ¡O·­£ÃmsÕ(tTÑ3½öCÌ!´	Î\x0003ÜÑÁ\x0001ö®µ\x0010\x001eÎ}öTµfêegfm ·qZ\x0007s!ôª\x0005q¯­²Ït\x001f\x0006¹×¢ãü\x0014/éà\x0010/ñ«üë¢ýë¤¹"K©¥1-onªw°©ÆH÷Â¢\x0018âà
Y]\MW\x001bd8Ú\x001dÝ£q\x0019`\x001aoô\x0008W%\x0019ÅHKoS\x0012Ã¨ü;xÊ¸ \x0018ßæååª¤ÎCÉ\x0018<¯b\x0007OýU\WêZiÉÝ^yÇ¢nõÄd5z\x0010óÒ×í¥WXº³Z.F1R:î/ÖÉQÐGS\x0007Ð!Âæcçý\x000ea|q£\x001eNïoÎL·y^ëçÅÖ\x0004#B4E5þºP¼\x000eEïÃwnó&\x0005G\x000f\x000b·ÃQ4\x0003´o\\x001eaSóÐ5/7¿Æ\x0002èãÂã°¡\x0012®ØT.!A\x000c/M\x0000h¯Íà5´\x0017\x000e÷0\x0019P\x0000\x000eQGò%áÅ\x0008ôZ½îA¹´ñ£ÓÁÁÑ±Ácd0Ç.^&µNÈYºl\x001eÄP î\x0018\x001dÆ\x0006C¶\\x001e\x0013W¬ºº-
ñ¦u\x0010zTTp®uÍ\x0002¸ðÜF³ùÔE{m]îf\x000bò81þp\x0014¤"N\x000e\x0008\x001eãe¾¡(\x0017¯[¹,]Ö¾}C£ûrEMü*¾¾¾ì×//^sqÅ2[âó\x000f?y¦ÓYÅäH©\x00101gÅ\x000fa(¦ÞÂ\x000evÓ¦é}é0T¨y¦ÆÊ¢IQò\x001f²È)\x000b{\x000b:³ìÅÒp½\x0006Û(ÂÆÕÁ\x0002\x0004\x0012\x0017\x001dT ©0Ù©ûL¦h\x001a\HÒ¨,:x*\x001d\\x0019ÀÛ<Ê\x0005Ü\x0016EcHæ_ã\ß\x0016Kîbñ¤\x0012¬¬nÎq¯ç\x0004/\x000c\x001be|o;x§¶¢' \x0007L(¤\x001cá0\x0004bÓu[iFì
"'\x0013\x001e mUq(Z·*r\x001cbì6vO¯Þ¾}öì|åºÝ?ùêæòXÞ'\x0019-JÝ[¦@Þ\x0006nCY)þå/³eÅÿrM~C.ÐTÌ"øDÿ¨R¤*4P¬G¹lC\x0017P®ÊÐYL.é¤Çeî\x0007Âñ&,àmºá\x001edß{x°³PV,àvðUx\çt¢nín_¿]=Q_¿üü\x001fow/®:Ýß\x00076b»æ7%ws´H\x000b+TÛi\x001eÛ\x0017H¾ç´2$Ë¦G\x0013¤j,f,¨O"\x001dnUBÕªQ¼N±ØïãûÝÁÁ#³\x0005}dr&Âöº\x0003´®ø5£"\x0004ìîx0]¶k¾ïÇLð0§Z\x0008Fk¯cGp;\x001e\x0015f` ø)É3Ð\x0016¶³\x00125ÒÌ\x001d\x001cÒÌ½\x0004¼Vf&\x000bM7\ga+.Û\x0012/à\x0003÷0\x0015O{\x0013V\x0002X¶\x001ebS£k´'ÅZô#\x0012\x000fjÌ\x0017\x000fF\x001eº¥»Ýº1fÒÑa $\x000f®\x00062ôbâ!óÚ\x000f"\x0017\x0007ÛN±*@,H\x0006h7º¨QëOÒy³\x0016zÿq÷þíÕ\x0016\x0012R=nX<þ!+W;Am¸â\x000c¢Å\x001aöÑJ\x0010òK+"]ßÓ»6Æü4ó\x0012Ý
×
\x000eéã\x001a¢QÑÉÚÀéÉ\x0004hàÍ(	3~OÕÅ\tü0ùhgÆ\x0004\x0005\x001eóØ><º2\x0017b\x001b¹óþå\x0018\x0003¼íªü)æå¬\x001aÜ¦ÕIÃÀ\x0001ç â\x001eë\x0014QFoIA¢oy[Þ¹Ë»`{\x0010{z	1hG0\x0005\x0019¾GÃ\x0014À;Ëq	\x0016sÒ>8Uh\x0015b\x001cW.VJÝ^y³	`?óAàÊÑàýT \x001dµýÎ?-èÌÞYÔiAâº\x0010K\x0019äRÖÜ\x0014\x000cÿ´ oá`íì3átd­F/!¬jM@/\x001d=â|{Z"ÿØ×U
RÉûä±ß\x0007ÉðDÊ\x000e\x001eª/	Ñi\x0013üç©PõéùÝÕM¼_ÓÊ­üë»çÇÐÌñ¬ò32\x0018yÍ\x0014\x0002$È.gScï/®]\x0011æÂ¹xÜü&EÙåÉÜø¤Ç1Wÿ¼zý®®^vO~¿{8ZÜ%æ X\Õµ?g63­\x0018Ðé\x001aye¾ô³¹î\x000eN1÷&BMcÙ.	¾Èª$z$?Ë\x000fÒX×X\x000b:h,ËÖ.º3LÚ\x0014\x0010=jå
9ttl\x000bØ\x0019¼
ZyR<23Æ^Ér|ó1¿Õ\x0003³m\x001eÉ
ôNOÏ5¥À¿¢wxNc¹\x0013¨ÁÞ0~C\x0013\x0006ÈôÜã>2¡bcwz®G-í\x001dÏk\x0007\x001cQ18"ÉU@d­ê¤sb\x001bLA+\x0000O\x0000îz/\x0016;}\\x0019\1²×òt¤]¾áÙ¦úÓÍýýÃùq\x000eUrQ\x0011ÏèÍ¾\x0019%8ö!%ÍråË\x001fª7$ñT5	JîaáÅÛú¦Gå1íÍ»ï.\x001eÜnã\x0015ùæòó\x001fËõ2±äÝawÈ°ñ0/\ $_úÊ{W×øtG»·P\x0002(Ýî¥«\x0003,¯ÁÇÊ\x0013¦\x0014Öâ°Òw1Õbvp\x0018Ø\x001cxÔ(½Öª²CU£-v\x0019|;\x0005P:6\x000cN¢¥\x0002×qàj\x000båÚñ\
½\x001d°2¾P\x0000n\x0001<Uê½Q\x0011Ë`\ÕØa¥\x0007àSÉW÷fãÄþåæáîX'\x001b5T\x0001\x0017²ÑCv&É,ÎC8ß\x000büiØÉzh"|tëôEÞAºÉ\x0017iéÂÈä¶½¬u\x0001\x0000¶ëØ\x000e\x000b_"Ó6`-=7\\x000c\x0015y£âøFuð¨sY½29\x001azlu¢ÌiþY²¶¥4y\x001b<\x0001ø¾Áæ\x0000î¼\x0004> '©ªGø[gSýÍÃåÛ÷qåÈÞ?ùëÅÝõ±\x00127>\x0005MWZóSªÍ¦ïdÙ>æ¼2HðT^@;mN\x0013!\x001b¼©;è\x001bßô¨<fëäµyu	9µÿþú/KS\x0011÷4\x001f)óA6´$¯+7Îu¶q¢9	×ä°ù\x0012ÌM:Á\\x0013¡\x00062_\¿Õ\x0005µæA\x001cÆ®uQ\x0000x\x000f8'®²]Ô\x0014ê¤\x0004³Æö+\x000b7wïÞÝ®nû\x001fV\x0008Z~æ4UM:.®\x001cX¸¸E%!ù°á>\x0001ßy}×ÇÈm\x0013tõ$F6\x0001ªaÚé¤¤¡ËÕ\Iv­Ù´Cñd6hø2ZTä¨kZÚ2vÅ\x0013òy¸vu×¿½¼yxòÝÃÝÑº\x0008£Þ|Î\x001d[ìè&¯\x001e¼/_Æ½Q°2\x0006×\x0014eó!Ç\x00143ÄM¼0d0W	¬\Mü\x0018[ïØ\x001e2è\x0003tÖ´Án`Q¦½oMÛë\x000e¸îçÊÇ¢\x0013r^/ÜÁ;Ù&\x001d<B¢³2ð\x0000>Äa],ªn(éÈÚ¦:8´M1¥Sï­ôÉªÎZ3\x001eÓÒ%\x000b3UÍ\x00028v\x001f\x0005©«>3)Êë%U\x001dÊè³á³û>¿÷²_·?Ñ¹m=\x0013\x0012¤¼yxñù;>lGºqVgwsòÆ-å\x0012\¾|
Y²Î_üÂ­÷íN½µ"È¡·\x000bYd¯/J#:¯Mö[/øÜ8± cã\x0004iT5êé\x0008È ^»¢ÃJdÎ.¯Sÿë\x0002^û\x000bn¬Á\x0005<Mu*YÎÜ¨Á-\x0002~jÝ= ;ßß!c0à­\x000bº\x0001a¨µ¢µK2=LEb\x000bzèEb%sð\x0002NÎ¸ºÒ¶d\x0015ÁÍ\x0015Ýx1ò»ÛOWwýb|sµ;?\?í.\x0016»wUÏ\x001e,\x001cP=)\x0016¬º'_§uÊè\x0018¶¦Iphe<\x0018H'U¥¾U\x0017\x001fñÌM>TÛÈý®Ål`ÓÉý×5+\£ ÔÊj\x001c =@;èPå"DÅäïªSÎq«ã¢ÓºÝµx,~ÄÆ©t<t­ÝW\x0010oc÷[Ø \x000bJØª\x000f³¦¤KmxâÐÌè\x0010Î_½/Â=¡Ï?ì\x001e>\x001cé\x001et,'Ä¬ô(\x000cõ,ûµnÍ\x000e,Àá\x001eX¶.!$ÆF\x0003§è×H\x001auí&\x00006¼:\x0001û#"×¨\x001b\x001dT\x000b{õY:Ç«\x0000Ø@ËÂ­½]ôD/ÚEÝÚëS©+W\x0001°¡¤-\x0005Uò\ªDpÜ\x001a®±ÃÊM\x0000h$|QÈx»f\x000c0j'[Jµg\x0005\x001b:\x000cô,²ê´y:ç\x001e³9Êýþµñý\x001dæ9ósó\x0015\x0019`ÇJâÓc¨í\x001a\x000fA~vÒ=4ùû`êI0Edç×nÙx\\x0004µKs0	TJèWÅaõLáZ¤Å©qø]BÆÄ©¶\x001e`ö\x001cAÍmªßÊg\x0013­q\x000b,èÀ-°µ\x0019n¤D{G\x0015ÑÑ{g	­\x001dO¼/åÌE\x0004z¾*\x0008\x0015»tSè6{XzT~&Y½nXºrLJMÒ\x0000°^\x0000Ý\x0013\x0005ñ<®\x0010*3Ê8ª¾Jù5vôc\x000fè¶O\x0007%úÞFEKwJìeh\x0016¤7T
ÌÔ\x001aÑÑ{kD2ôØC4´þ\x001e38=\x0003Úhm\x0017\x0004±µ©òÓÎ\x0001~Øã^Uwx§\¡?ßÈ.6Ï»Åón¹{\x0015ÓØUwöªbG\x0007tzîÅùû7éÃ¤ç8ûühaTµImúÌú@\x001fÑ«;è¬\x0006ð~¢:nÜö&½ÁÉä\£2sct;}º\x0012þ6aFp¨K\x000e\x000eZÐ|Ê\x00039\x001dy$Iï¹t[NN`Ç\x0006'4\x0018¤Ç¹äj «Ðë6U÷Òx;vêñ¨}~ìöÜ\¸uH<e@{ÆZcI­4\x000bi\x001aíT\ÛÁ¡ÓÚç
UÝ\x001a¬t)U]R¥>Þ¦ÍýäzD*¡n8úØÑ³ Õ~im¹Ûç0`°£Xl¥á¼¶¬\x000eý\x001cg§\x001cÐ¡Ø\x0019Åû2ð²¤ûsiLbaÒm\x001d½bßo\x0011ÃànÊ\x0019Ê{7t(ÍÌ\x0011Wç!íÌlÂÝ\x000b­+÷Y~<Z×ë)ù0Mù\x0011\x000c°/øà['ÁÖpëuòqê(\x0014!J¶ïN ë=cömàb+C½IÂV\x0014§¬E\x0007÷\x0000^f|,V]\x0007w~ÌUI­ÆoYÀ	)\x0006$\x001fðL©Z6Vñm\x0010íx\x0001\x001ctsA\x001fÒóx\x001dÅÜ57iÆ=0°,è\x001eéÄÖÏÑ£gPÒ\x0005ñ\x0015ù$ÈV~\x001d(¢¢÷:3\x0013Dù¼oA\x000f@ÞçÈ¼ímüÞG0÷±\x0006m¶\x0006¦0Eõ;:¡q\x0002¬ÜmÅ)\x0016Ñ÷¦¡ãDoµ G ·r	i8=³©]bÍ\x0000zjÙ¡£#-\x0003×÷À(Z6A5;©\x0006oÜYqJÔtpHÔ8&i9°É©a­Üð¦ttv­)mzº::<]ÒñÖï\x000bN7`\x0005«ÃºìÛII®_}¿fr/åÅîáH~¶·:{N\x0007ìP?KF\x0014\x000ez¦;WN\x001fjË\x0004\x001d·¦	PLP°*¬Ãñ¬LX\x0014QIÑ=$¦¦\x0016Î\x001fÕÿ\x001ezÇ ý·\x0006\x0008]}4Vó	YÝy[Ï·+yt´\x000fèòS/ô/bÓâãn<O¸V;~T÷\x0018\x001dêðË\x0014X'<ÕÊe\x0016^Á\x000f½;¶Ñ;»:ù«\x000b|\x00055û¤lhÒ\x0016QÁû±¹	§NE\x001d¾3\x0016¥\\x0003P¬zfaàlW´¥}\x000bN»:Õ tx\x000fÂ1\x0016ï¦»\x0007Àðô©\x001a>ç&©ª»Ã÷ªîÄ{	²IQøë:º+v@\x0014Vh®:z§¹J\\x001d\x001d".%µö8h\x0000ÓÖ>1=\x0003zßØTó×K&( |ÖM\x000ed\Ï\x0002W\x001en¯\x0005\x0015yXâýíîîüâêX^·ImVÍÉäC\x001d1m¢ä>FJnlôæÄs«\x0013Ï'~r\x0011ã\x0018\x0008O0\x0003çÞ§ÁÄÈF\x0007ðe"õÄNÞ¡±'=CNd^î¤ØÉË@ýAÒÔë&8\x0018\x0000¼ìnKá1\x0010¢à^2p)Ý±Áæ÷ßARÎ¬êI'CDGÙÉe~êJ_Ð\x0013t¥óTRH\x000fÐ\x001fÔá¢\x0013©5\x0007©1)Û½ \x0017p»£ÁíÈÝÔ)>M,R|cá7\x0013¯Ô\x0001]~Z2q	Ã\x0015\x0013¦dèýÌê´ÔÇýäf,ð\x001eÜÊµ;uI¤=F[Ý\x0007§øì+\x0017nKDbn`9ÀÞpµu{\x001f½ù\x0012\x001e\x0005>¹^sÎç¤\x0017WFz_uLRoL-F0º¢OÐg)èý¢Fzî±\x0014Ð­Õ²i!Ý4Ù¼\x001d\x001e:ytnKÄÈ\x000f¦Z|
\x001a¾E±,ýµð©Ël\x001b)êXVo±GÜg\x001d1¦Å»\x0006>ºI\x0000Þ\x001b\¥s\x000eö_-ø¬Êãèñk§2MÌ{\x001d>÷6qr\x001a1\x000fÉ§\x0012Ù®ÉâÔ*3\x0001
~[ò\x0019$Ïä <¬>ë\x000eZ·­¸fj	;ÀgÛ[8¸â¥§"ÏÈ
>©¸\x0000Þ·\x001cÉÄ\x0004ÜáC¿SÎ §
\x001b£+£	ÃÎæ¾¥+å'\|7	=«4-/¾\x000e§RÔYÚ\x000e_zY7YNJ6´³Xlán­\cÓà7w6¾³\x000e"hzÒ\x0015²<\x0002­o¸p¡Áo\x000b§tá£«OäHbl\x0014ë p|K!å-·Ã×~eÉÂ8hä,Uði¸T©åNíúî\x0001ÝCË{ä	 Ø¡Ãè\x001a>µvý2Åû\x0017øâ@ôdÅ\x0016¸³$*£w6ª\x001c|\x000e¦\x0015Møj\x0000¾¨ÕTG¯\x001a,ÑF\x000búÄÆ×Ñ-\x001cËµwÈRïKÑÏ`*\x0012\x0010#íÅ[\¼Á\x001eâ\x001eãç¨áÍ\pyî/?ÝA]Y³Éÿ¼»½¹úüÃÍ1ªÚ%\x0017rzÛ%\x0017ª÷C\x001c%FIë}éøÃú@\x00087±!5\x0001J=a¯ø\x000b)¨jEï\x0014©\x0010}².'l©\x0007?Ño,à~¡ß #\x000cðüy¦ñt\x0008î"ÐÉ\x001cR\x0010ôh £\x0017@WUÙtÙõÒé\x001dSÑT.ÏO±\x000e±\x0013I¾`²¦¥':kôæaéÂ-èÁd¼ªOäMXhé}Ô©"8Õ7/à±×7\x0017Ë1á\x001e9qÃ\x0004\x0016k5¡qÎ>4&þÍµ;X;39cXXb:»!ëT`éìð\x0010÷q\x0015\x0015©·\x0005Ä\x000cãR¢WáÉªØçK\x001cZÌIí÷¿èê\x0010A7ôñ\x0004t¨\x0008\x0006ÛD\x000b
Qàêä`ôÆ>>Õçvø^»¥\x001eÕ^|äçâ\x0003¼Çâ\x001621£\x0018Ö\x0002\x001f\P\x0019\x001d'9\x0017\x001f¦û\x0005=ôûXÙ"ïì\x0013¤¢»wÎè~ n¡'úoÂ¼u_å§\x0003z"t`ãárÐ\x0002¢aïG\x000fhUp\x001fÚá\x0013À[86IãlDô<LY¨RB\x0010[û*?õÅ\x00078ó2y+eµxÍ Éü\x0002¿©)å§\x000eoÄ\x0004?ÀçÔÉÙÛêõL0\x000e\x000cÏt¯>Ý¿
íþ|óðîbeêæÏeÏzH7¡³g¸j­îMé/ýü®O0\)lj\x0002ÔM\x001cgÆVªÊüÀñäÃ~ÈÎTÖ\x0004ØÀÍQ+Ðv\x0019UU¨\x001f^°âsóÃÌìè,Y=²\x001dhz«k¤=ín#Ù\¼Z\ÒóJ0<ñ)*x]4åÛ\x001c\x0007k§(qy\x001béÑ(u.vâ
<ÀóOKG\x001fÙ&ÐyUÉ\Ç\$\x001b+V¯^£¬R/\x001d¾§^**\x0001éaeª\x001dt6LUóxk÷\x0004[ð\x001eê9
¯ØjàM\x001a$VÊr½xÿÌÇQ[ü\x0013ß²HuåEap\x0018\x0005¦LÃ#Íô_Za¬w¡:3ñ\x00136\x0019	 Æ{ÒÃ\x0006tõ|Çr3qû	Q£uÔÑ+¤½zEY;©A\x001bAWBògéãyxÄ»}ï¿½8¸Ú\x001d©NbÔ\x0011÷´\x0012â\x0010¶¢¤n\x0005\x001f_zë7zP'Û$ø'.
7\x0007Ò)ÀLYST\<0EWù·9ReÊ.è¥çC	ÝãdW2ãÓ0p£T\x001fÌz \x0007Xúên<ºRÌ3j«\x000eÞ!S¸?"Ìæ	WîêÀu"ª¶Näµ\x000bxµ°r®ÌLÖ³ä¸\x001er |oÖLïÄ\x0001^~êiÌFUÖFÓÒ×Íõso^ßÝæëù¾q\x000bÄ¿Þ]^_¾ýüÃÂ#EÓïcêÝâ\x00172Y÷Ûl<a¦£È²	QÓÿ&=§}¥%·%®¨Ê!äÜ"zÓL\x000eÝg$\x001eÆ\x0007\pÖzUëO^t\x001e$ÝæwMÇvAw\x0016ÐKP\x000b7`Þ\x0008z
:ÀP74R\x0017ôP¡9$Á\x000cD²\x0007B\x000fuJ]Ïä ÑtfKzi.n×Þ¿îÎ_\x001e=è9"L_µ4Òë	FZÑ	ØuVö±IPê²\x000e £jo&B\x001dYÐªî³älb\x0003\x0017¶õ\x0019üwÉ®ëî8_ôx
Óâmcp \x0003©µE¥îí0)M\x001d\x0005þ·\x0015Nö\x000cÙoæ¬Poà[ýdGÖ$5XX¾½ê\x000c«ö\x0016Ì¥ÈýjNAðNÄÉLµé½ïàj¸O²½Èmý
f·:RëÆWsAçz9Gj)Ù\=&~ÒrÇSn·C=£åÒ°¤d®z£\x0019Æ¤XI«û)Á¸ {5x»`µ\x0004¹\x001a}êMryÙ}~}ûÝ«I\x0001=<ùëåÕÕîîùqô\x000fÙËªí)Cz 3UÛ·)?_º²SkMãmò\x0013îß¸&×\x0010Ù\x000eÙ\x0014CÆ|\x001fcUµWAÞ´452,àÉö\x0004\x001e\x000fi\x0005~Y\x0016\x0018Ö\x0017¬\x001bÕ÷üéi²Ä\x0000½\x0000º¦
ß\x0017B\x0003úÀß'4niÊ*wpÈ*s§\x0011\x0018×Ì \x001d\x001evÖ¬Q\x0012úiª\x001eêè\x0011\x0008\x0019\x0007BªÀÃFp|/IqØFé¥iÐKG/ v~ì<j2o£g¥\x0006§9£\x000bx6ÀHö4Çf2\x001cH\x0017LÕ1á$a§XG÷=ï\x0018÷Ñý\x0005]ñö\x0004²ôê°tá­z+:xìå1aéAO$&Å¤YÑhOÅ©Ù>ì\x0005\x000eûºrxL­×1µa\x001dÀmÝÂ|þ\x0015¯)çZ¤®ÙU«o SFG\x0002
f¡.¥a\x0014Óã\x0019bÎmñwÉªa\x0004Éa¬ÜÕ \x0006j7¨»ßR\x001b©k¦æ\x000eü£dg\x001d¾,>©µGõ,ÒÚC\x0013Í¿éè¥¦ÀlGGºRO:°z²\x0004a7Wr*e\x0003ì\x0008Ø\x0001Ê±\x001b)ýã cèí¸lÝ%ùiOàÝ\x0005V9jÖAÑ\x000ceÉ¤Æ\x001c>\x0011òtð\x000có<ªR\x0003¼vdÁ
i8ït"[Ïö4|ï£É\x0003G\x000b÷Ü¹ªô@¬z¼MäÓÑ^xýÖºï±ÿöaa\x0019¸¸{qq\x001cZ\x001biò®V?ËÀæxE60»[R+É;M¦ËéJ4\x0011>Usé¶>éQqLsÿÊOß\x000fÃ­)»OÇb¹\x000c!;}\x0006{u¯5
¶qoO"5µNì\x001eÇ}iÒ\x0013·	´xÄ\p\x000e%õHx !?»ÝøQ/èÖ\x0012¯þ\x000c\x001e §ÙMC(zvlâ\x001cµéà8~'÷\x0001:Yv8jMÈ#¡Æ#õòõw»oæ#uC0\x0017WOþßÝù\x0007hß\x001c-Á¼©ú¤e6¡¶<­Y2¸_úm*Mj¢\x001cx|¸ð\x0008z0sz\x0016qÖÕ~Åfi¬§\x000e\x000e=Ïý\x0010 ÿ*FL\x0006\x0000×Ï¸-2»v­\x00018tß\x0007x¹û\x0018PÈC~Ìö\x0016Ï,Ckj\x0018V>LiÏiè^)©UâmC#@\x0002£R\x000e"®Íe T+µ\x001c7±aD{à

\µ\x0017ÝÛÉ§Û­õ^\x00008ì'\x001d«ÁU\x0003Î\x001f0v«íØÄ	\x0016l\x0008ÃïÈöP-xÅ\x000f\x001ce\x0017e"Éìà@\x0019U;gU\x0001çJÐlÍóëöî¹¿¾M\x000fîE:¿9JíE£ô\x0019¦*ºº0\x001cq\x0005	´úq³ÜUl^Ls\x0006D|ê+q;a/"+¤Bøç!êã\x001a[À6¸\x0005p20¡¿Ík¶jëÐ>\x0017DAL5Z\x001dÛ!v\x0002ïywÎªSàÚTfª¿­\x0010Ævð\x001e·\x0013p¤Ù	´¤a;ÝrIN°t£nc÷\
\x001f\x001a çàÈ¤ÀóÐÏéõir
\x0001\x001cþxæp¿g\Wïª:Û^ëd#¹8vXÀ£U+KÌ\x001dA<\x000f­¢FZ¦ìe\x0007.ÚX-R
FÎç+¢­Pô~Úæì×¯½Lë\x001aâÅÕåÑHh³õØlÊ¢F¡Ð^@ñß¾´~X§ÛÜ\x0012\x0011Þ@©\x0017\x0002©8\x001cAkÔÀ)ãðä¤Æ3:8dixf\x0012ÓEé\x001fæ­²fA\x00008X\x00101ª÷,)g·p°«¤öw{ÝÎüæ±=~ìl0ðhR\x00010T$^p\x0002sv£½fEç\x0015âÙðéÍÛ÷ú\x0012ÜÓÞ?¹ºxò{:\x0016Ç¹\x0003\7ªKâM=T\x0014¦yJÀÎËãdËNÂhÁ4\x0001fíê|3\x0018Åm¼.°Åéjoòç%O´	n\x0001<\x0015Õ `²?³(ê;¶®Ê¤cw*\x0013\x000e\x0015ã{Ãd.°9èù^±¶O\x0015»\x001d\x001djìS±P¸á¥0»ª¥\x000féû 1Tç'²ß\x0003:ÿt@gF\x001aè\x000epz~¦Mz\x0010É5òÍ¥»>U­D.\x0004Ú\x0000&ÎÅö8P$¿2Ö8ù·éÅÇÉ=þýÇ££I»ÃÆ-îpJ¦ c\x00163\x0011ÄHãUVÛÑi¢Ó®Y±¨Ñ8Ü[¤a4qk\\x001f\x000fS\x0006*\x001a%T\x0011KµR1	È%¯6Å\x000360V\x001bÁ°)Â\x000eÃÔMìúô*\x0000xT¦\x0011t;ÄX{aW\x0003×\x0011mSä\x0006Oýz\x0000ÞM]¦¦F¶8r\x0000\x0012¸Ó¶®É\x0016m[,\x0001Ä\x0012±ïÀkï"Ýï¦\x0016KN«ã\x000b:xÂiÄ\x001eèl¯ÑiÑ/1A5úÔÍ¥[;ªº{¢µrxúÒukR1¡Õ]oo)\x0010\x0000n]ÜG/½X>£}ÒÑ%\x001bR¡,: "NQLÙÌë%å/S®rAw\x0006Ü\x0000r* \x0008\x0011éU>\x0010Ò°w/nÝè×utôë²Å#\x0013\x0012\x0004~\x0004=hbÿJ\ºª6åîz\x0001fÊÆásÅ6bPèEvæQhMUÛèPËÆùÄ\x0008g\x0011bÅÓi`Åe\x0016.Ý¾»yóì7+	?Üí®_\ð0ãpÞ\x001a\x001d^öî0NÓ×l\x001d°á×}.ó¿,2§x%6ìN¡<-0¯*)ÓB\x000e\x0001Öt{N¡4\\x0007`*\x0000pWE\x000e\x001a\x0019\x000bbl8çvPÝ]L´æ\x000b6(±å5¶j`1I«"\x001e9#v\x001b¼KEØ^A(Qå\x0008¼)uÀ¹µn|Ì\x0001»ÇYS¨å¸%)ð!ìZ«ù4~³{\x000f\x0012OP\x0006î\x000b÷G*p¯\x0011]ÜÉ<^¤Ãà\x0003\x001e?g¥¨Z.¥Èzû¬\x0014h±r«Z«y'¬ÕCyÂÇßVHÅ;8\x00102]\x0018hçj²fV°Ú_gª±Öì´\x0005nZp])<ªOÄ	&\x001a,à¡GÎ3ONêH:À¬÷Y£W1s¦¾È\x0005\x001dú"+9ËX\x0003Ã#$ZÈÛ:t"I¨ae\x001aM\x0007Jè]µ\x0004CvNQB×$gÁ®x\x0012åîÙýÇ0éý?înïvGÒ÷iH=Ôà\x000f¹Bk0T[l#uúÒê~£h}DÛdÇç	&Ñ
@\x001eÌ\x0012²V\x0010ÜC ®k­mu*¾\Ðk/1Ñ`\x000e©º\x001e®\x0014p§¯\x0002¹Ùy½²ó\x0000î:&$Ê\x0017Î:(^h\t \x00073\x00150\x001fÐù§\x0003ºSlL\x000cãÛe¨\x0007#¡ÎÖwîÕ+¯Oë\x001fo\x001e.ï/¬øâãÝ±\x0014~Õ6ùÚ\x0000¬kãòV\x0011Ó.\x001d²ÿ\x001fãk\x0002\x001c8á"wêÁÎðÔgÌe\x000b¦\x0019ºÛÐ@Oæ+ï\x000b´ÊÀ\x0015]ÖAØë\x0001Ñ\x0005\x001c\x0002¢<)ÀE8QNç\x000e«>®ô,øµD\x000f`ÃX¦äõc¼"rô|àe­\x001fÀ\x000b,<a¸ØØ½¼¶ðAG4¢ éÉéà^KÅ{%r£Á·Ø\x00111\x000c;x*Y	À¹q\x0017±J1çÄMüÇ
ÍØ±z¥9}ÕAz½¾R6õ
\x00008,¼f}i\x001dV\x0016\x0012¶N
Ò3»¯Ü\x0002·Ø±kÛL\x0005¼ª¡#K'
Òø1÷
tt4Ä¹ü\x0014LÎht±\x0019j	½ÕjlE#o×µÙcp5NÛÁ\x0013¶2\x0007¤Ë.^­[òé°´AÓfF¿JñÏ\x0014u\x0003<Úá(îc\x0019Û\x000bÇ\x0016ïR@¶\x0004E«È¡r½t/\x0011A;\x0011Ì\x00018ù5\x00009\x001e{Ýýn±+\x0007ÝNt\x0013\x000e\x001bªù¦ù\x001a%%\\x0006\x0003¤6¦­mÁôÁÊ¡\x000cTè~ l$Ï-
b\x0017ëf\x001b¼\x0002¸U	âÓhékSÒ¹$Ü´\x0001² ;\x0003\x000eóúÄ\x0004ÅOJ\x000eÐh¹UC¿£¡Ov\x001e*Fï!ÂaxDeìÑ\x0000pðQ¢âµ\x0011VÑpF-6òÚM\x00158\x001d\x001c*p8ÿYáºª*éHBu[æz½÷/î^ß\x0014mýéæáêòúXýæ\Ö©S\fÐó´\x0011ðdbð7É62£ÏÛd'S/ÑÞ\x0002KsàqQè\x0006ÎB)idÉOS\x0007wÐ<A¯_¦dTL*pþLZ|ÞéAéà¾Ûùl`+\x000fmM\x000e\x0008>Ìê>Pwm¯<àÊ\x0003\x001cV\x0002½þFÀ5ÏPIEb;S µ§^ÃÏ6B¶ì\x0015Ë_pahiº)~½[èµá¡\x001164\x0018´íhè))3µÃ¹z(7kAÚ?ó¡=Nêã'ª=Ðxè2y{-âzÉ\x0013µ·Nê1\x001b)MÚHoþDïuZ\x001eªEþ²´Úi\x000eè\x0011Ð#°É\x0014s×Ý{tÕ.I\x000eÐ\x001c¥y{þñábÒ<<ùfw·{~y¬fíââh_÷ùcÕáàãâ\x001béÃÞ÷\x0012ÄQ4ñÞ#çõÑØ0zêGÑdq¥UØOámÀ\x0006oÃ¨ù9%Ö35±ª8\x0004æW\x001bÁ\x0001»1¡Z\x001c\x0011VXU¹ë£\x000f\x0016¤q"¤ìà²F²À,wV3ÐÉ©vÍyìàà<Òscå\x000bVfîk}GÝ­Õúvp¨õå"åÁI
Üf¯pÿM\^\x001d\x001c¸¼¸\\x001e£þÎiZ\x0013N³q'Ü/ÛØ\x0005±Ó\x0019l§uCaW\x001dl^ëæâ+cÞ¿¹õ\x0003Ý»Æüsyþrw÷üHÂrÞ	3ÑÄC%b)ôo`t)\x001dÝhÆYéNT\x0000M
 ¤æhÓV¶½­EõU8Ä-8\x0000<wð`1vÀ<q^\x000fãXé²-V§i\x001c\x001d¼vpïQÇ\x0019ãGMÒÊ\x001b¹jÒ,èÝ¤az<LmºÊM³H\x0001[NkG\x000eÀM5k\x0008×óÓöíç\x001fÞ}þáîâúùo>ÿçÝÅÿFçvwþòã±â»¶XIÃ\x001e<h'*({h-´_:ÀkB^e.\x001b¶ª	t|ì¬i\x0002òIJË »m´«õ£\x0000\x000eA^ëAqë\x001a2Îó¡\x0012QfsLÉ\À®]Á|\x0012pý 
ÀQÈ§\x0006õÝÉhùðC·1a{u;È\x0002pn\x0000Okn\x0010C×¡¥Ì\SÂ
\x000fàÞ\x000e\x0012Dñ¶T<Hù\x0013³^¹\x0012yÊ£XâZ5\x0007\x000f\x0000îë(\x00165·ªäa²T:©o¿ÃLÄ¸\x000fGÁA\x001c\x0012\x0002PÖRÐ\x001d\x0019RÐ<c¢ Àaò\x0004a½×%Ò±MûJí\x0016t\x000b=P¾V\x0010c	©ù¡í,6¾ÍÉ¾èè`_¤ä±Ö.3\x000f ªùá·¶9f×ÑË@(	\x001bêÓ\x0010³Óv?ý		\x001fM±;\x0003#bª\x0001&\x001b\x0002¯jÒÉÚ¯eBK\x0001ßÔ,Î`¤tU\x0013?ªÅ¥\x0006qóþ»>	«æÐfÖP£óº¸Ø$¥|~{í\x001eÖÎ­l\x0010BæN\x0000ù/\x0003¸(û©\x000b²C\x0017$ç£À å¥W:Í\x0014ÇK\x0017É\x000bèèà\x0005°}Í\x00061ëQ\x0010Îç:_S?y\x0001\x001d\x001c¼\x00001ûQ½\x0004]ãÂÃ\x000eRWä'¾©\x000e|Se?\x0007uAXÉ»Tgô©¼:¾¹½x?Û$7\x000fOþ²{¸;ÞÄï¬J¸B7\x001f¾<\x0003db÷L\x0004óå­y\x0015ÒD8X!>¨ªßàÞ¹¤+Vx6ëz¡u\x0007ïAr\x0016\x0010\x000cå#ÛSeø×ó§KiNE\x001d\x001d»\x0000v)ÈWÌ´^ë©v\x0012¾ãkªù]À+´×\x001a5ÁñE¤u\x000e\x000bo&õ¼[PÏ£\x0005ý\x0010Õª[{HÃ)&B®t\u\x0000\x0000\x001cºéQ4°F\x000f¼a*°4 7ÒÑêèPÜè!V@~±XS°ð¬\x0017îÄð\x001dÚ#ôêÝzô^Êk¾¹¡üSßÐé}ò=ÕL6ÚPµtæpÇ|{éPÆ\x0017LÁcîmV\x0004<®üEzwæÅûûË÷×\x000f¿YiÖÚ=ùöæüåªh¬Ñ-«Òsð\x001e®\x000frÃ<u·@(y½kq¢Ql\x0012|ªh\x0014éMg0~Þ\x001e´â¬uÊàªµØY^­
i=*éµðV\x0007ïægaîM w\£ØI=÷ô?qU¦¡X\x001d»Oû.B­Ú#<ëHµj¨¬O®,±³È¤÷ø\x00063«Íï²W
Ì\5¬<Î\x0011{õÉéËð×ÝÕÅõÛËcÌ5âKéµ_Ãë8¤TªµH\x0007æy&ñ	°
mÕ¼\x000f»Òd÷Tð5ÀQàÁª*EG¯©F]/úêà`CX®\x0002Í\x001d5S©Ïºó¯8Ö¢ß\x001d\x001bì^nÆ\x0002H&ÛC¢@ç£nZ$oF¬êñ\x0006\x00038°rý#¼9\\x00181dÒäÚø1Â\x00106=h\x0000ì°8ÝE\x001c\x0015mða\x0018ÛSÅ=\x0012d\x001d\x001cªx\x000e\x0016Äâ¬¦\¡{\x0017\x0007Í¯¹í\x001d\x001cÜv@\x000b\x000c9Ò:¡9\iw¥¸iª\x0005l\x0007Ø\x000eÛÈ=3\x0013)©ØR\x0007¥)àÛRb\x0015R.ØØ!÷\x0016±Í¨yXÙO³z\x0000º\x001f\x0015CfZØFÐ^\x000f¤õFÇsKþ×í£R\x000b;tØ\x0019\x001c×í4\x0005ÿoÕÚ\°ÑÚ4ÜÖ\x0007\x000f	(pZ\x001cÃlê\x0012OX§ê9óI\¿¤uçAvæúÅ\x001aYÃ©g/Þ\x001e%.©º='ÿv\x001dÖü\x0010±'#)¬åH¦	M"Áá\x001aÅXJ*­"r\x0011GHºÑÁZ)Æµ\x0013\x0007Èn#¼(zò\x0016WrY¥;KÔáëàåÔn¯Ý¢
ZßG·RÜÒi¬×\x0001Ý\x0001_²e\x001a^@OþL/} /)Æ¯Vup¨\x000c³û	\x0008¦X¥D3½1-=Mk[ÐS\x000fñ¨U^ûëÎj6\x000bg¤PÑmÝ¡Ø½E-WØkR¯m\x001a\x0012¶ÆM·ùÕÃwwéºÍWWr¡¿~¹»¼ºº9\x0012ÿ '·WWÁ¥%]éa÷Ü\x0012VO P³îÈûÞ\x0004(\x0006\x001c\x0004Fé¡ôB©Úù&=«);Ý>N3n{\x0007\x0007\x0003.\x001bd4æ®}UµÏàº\x000f-É$º©l\x001fÀ!ÎeÞP¿Õeóf ÙrvJs\x00016\x0004t]ë\¤\x0012\x0014s§»8´þµ<×¶È\x001dÜF¨ãÜªÒp<CbJoÃËOñÕ{¿v\x001bèy£\x000bq{¤Yqvidà9Lv\x0010Æ&¸Ø)¶©¦_úB¬\x0000L,u"Ã§\x0003_Ù>Ryø"nÌÄ¦§§^KïÒÿ3Q\x001d\x0001tç\x0013HÎ![\x0019)pïPÌuÈ¤ÖÖ¾í\x0000Û*s,ñDIEáÇ8¾$8§L^\x0007ï¼t â:ûÔC\x001fbLÍú9\x0010u~õr÷\x001cêÿõn÷6¦Í"ùËîÅ5[dG*[ñteµ\x0015k<Ü¿\x001aqè»\x000f¾È\x0011þÒgv½°q\x001e)b\x0014·
\x001bf\x000c\x0019Ptg«\x001fHrö\x0011ñÉûéààý6dÙ\x0012´\x001e\x0012PÁ*-KXaufªû¾÷ß\íÎ\x000fÊêËûóËëcÙâ1×!õÛÇÐxz*¦^%M÷¥÷};x®ÊIe½0y70\x0002d>Çh\x0010Æ4\J'Öæ\x00160ý°FÙtTS¬\x0003IXjõ\x000c[È=\îÉVKvª\x0002ÊÅ¡GgVLVGéÛëÏ?p\x001bÂÝÅÑÚ\x0010\Nz*¨õ±WÉFÏDvñ\x0014
~"O0Kp8LÁ\x0005Å*K®9D[¥eá$83¦=2\x0014=ºu¦#\x001cx`®°N
ÓæÓ´GäÏz\x000fªj®"SÕhWÑË4£Qé-È0;uNU\x00139_Ã9»5\x0018îÓØ+6æaÞ\x0004!±ÌAFl!CU¬\x001aÖ#3¥ª.MA×~\x0004)Ï+\x0017÷ÈHtX°Í,\x0007UÞàr*8ª¿\x000bù­¢É\x0008IÊ*§Xî\x001adÞ\x0003~µ¶98¬´d?D\x0017ñFMòeéÏ¬è:ë\x001bºSoüéâãÅ1è×ZæT\x001fï;\x0019¹&\x0013b¯$\x0000\x001bðº»9+:)\x0019£:ç²\x000fª_Èe;&\x0006¡½L\x000c³æ£¤Òº¯v ¦ðeýÅªá%ÃÅY(½ä´ÚIáÐ¬cê¤c'cÑAQóó¹Ðg´
uL\x001du\x000c¹g	î+ÇôUB½ÖA\x001af6×÷æ+.è]ò¦¥¤#\x000cÆ¦N\x001a\x0014Kcy÷rc\x000c(ëXR\x0012ÕÇ
m|Ñ£ÒXÙ8ïÍÃ¾\x000bóXQ°Áø1@uì?Ù\x0008\x0005fE\Â1¿Ñ\x001d%5`g<OýVïEÑ\x0013¦8\x0005¿FÆt@.X\x001b\UÀg$êÖ£8\x0004ËÓjÙÌ\x001e\x001afb²\x0005)+&\x00023\x0002·ÒÑ¡< \x0017(ô´ªð$íy \x0002v  6a½Òs­ê<CDoEÕDu;8\x0017FZðüT-½ÇöP+ÍQkàÃHÌ5¦§×lIèMü4¨å\x001d¡a=\x0005d I\x0004Ô ù¨£v¦Õû­ãçáøq_¶us¥´Öm´&JÒÕOô¼\x000b4tÂ\x0007ÕúÆfYE2½úcöµ©SÜá
QÌÊ\x000b\x0012AI@ouMX1¹AÏïù\x001e\x001a:Õé\x0004B\x00006¥ªëy¶ó\x0000ÝÒó[;zÀb°­É*ª\x001b±\x0005zk#\x0013rÝe\x000c-%E:@j!\x000c¸mlëÖ6&ØF\x0013ÑX\x0010\x000eKµæ\x00125KÃ²èX\x000eØ\x0019£ô\x0006­2GR72×q\x001båÖL\x0005G\x000b6\x0006éË\x0019:éêbZ¦×Ð­ÊbbîX ¡Ô½F´rR
°ôÉÎ­¤{"Y°q¤"g!OaÎj'ÓÀÄò\x0013kÇ\x0002
\x001d¤£ú¸'­ªª\x0016oâÀ\x0012,ü ~Km{TÛLò­®ºÞÇ6µeäýÔ»¸@Ã>æ,¥Û]Õù\x0003r«gÙÚFÕ± O_´ª®Ë\x001bÍ\x001eÎ³ZgÎÖ6\x0016¸Vu¡2æi\x0019t_j\x0002ÙÚF¤X4aN:ý4è¾$3~Ê\x001e°+öYx,Yå¤V$Y{3¦\x0015Êø:»`{ìî\x0015\x0017±Í×É{ï|\x001a°Û[3Uá,ØN\x001dmTÚL·¨Z8$ý³lå\x0014^°Ai¯«½uL \x0006'\x0007·^5ÕÃ\ü
Ú\x000b\x0011sXé\x0014è\x0000\x001eo¡ã\x000cÐÑè¶\x0013rÅ\x0006\x0006i)f\x0008[·=Àm¯F@`\x000eoôò¼×/{®UÖ8Üì±£Ç|EêÈLx)½ÚHz\x001f$ú5QY.ÈÝücJOH\x0018Fn®BÿÇ]hh)^úöÐ	JúhÕhE\x0005ºi <«Ì%\x000flÄ]\x000cp1êÖÄ@zE­:è\x001bÉä\x0012\x0003Ë\x001bF+ÿÐe\x001dT	%ÉÚ)Ä:Ü9!kM\x001bÇX°Sê³D=÷d`P{\x0004trv«uãh[\x000cæTæÍÂâ²ªI\x001e\x001bê\x0010	hÍº@ë·\x000f/\x001eîÉéûæâêêòþþòxq¶u41Ç%%\x0018ÈJVChª8%_:ÐÆ\x0005\x0014+¶\x000b\x001cÙíÄÁ7Îc»\x0006GÚôt;?x´!Øµ\ó\x0001\x001a8êøðCKÿ¹ªøÍnÊ\x0005µ6Ý\x000324é\x0006Î;\x00014½Mªàs\x001d\x001el£¦ªú\x00034òQp.BGÝèýp87Méñ\x0003tDQ\x0017Õ\x0012ª$dm=\x00132_ß5³!¤½Ó­¿Y×då04¢&	®¹n\x0002
®\x001bC\x0003rÒL<	·ìå,À`9308W9\x000fIIZ³ÞÃ"ÇcÍrnÐ.ðí4ø\x0019mÖä\x000enÐ/p\x000eã?\x001cGH*_àLD\x0011ý¾Â)Ñ +$||F\x0011KhUò$\x000eÔêÆøÕ"Ü=4àrÆ\x0007[fkÐõÔypS,yì[£â^°A"dª\x0014¬ØsÃ±\x001eÒ\x0016\\x0016#«­u£rº\x0019¿VÝ\x0007*{Ó(4§vÙ\x0005\x001a¤\x001d\x0013ªÂséUzM7:ÓzN[\x0007h(Û
äs#²îøqd©ä\x0001ºnÅÛâ\x0010oc\x0002\x000cÄ0&éDf\x00196Òå¼VaaôSú
=wLÎwýüæXí-äùé3\x0015Â\x0012\x0016&×á\x000c³;N>ê?¢a-X¿R\x0006±SB\x001e\x0000£è½çÔOl\x0006ö\x00162R£zL9F§_g;Ô°4ÊÑùÉhÈ¶?\x0019úQIàb(ÕÐ¡Sn\x0003ê-}Ñt\x000e>ª\x0000¨\x001b¦\x0008´Êc|\x0000\x0006gÃ¡\x000eM±\x0006VÀ+Í,kô\x0019\x000bt×b{ç@¯Û0dÂâÀà¤\x0001}\x001a'pa\x0002>\x0016\x000c¬2©2VR\x0018$-ÃVRD{d(!õ\x0004.t\x000c³F\x001e3BÍ¾uî\x0002$\x0006O\x0018ÓâNÌ¸qZ§\x000c\x0004xÖ{à®\x001b=³5@$¸\x0016Ýðü0rÔÊk±b\x00045h0|Ê\eh\x001aJztÝ\x0016f%ìÆ¬\x000fÙ|¶a?Ï\x0011 -LÒ\x000c°\x0012vßCC×qpª\x0013uêô\x001eÂî{Ò\x0015Ó­AéæCÕ¤
­ñ	ÇøI­ÿkëCÔÝ'å2iFR«*JåBG?áÑ÷<\x000f\x0003OuÖ}ØqLJ;¿ãöúýêæ|wÅ\x000fÆ¥ÓE^þzóô«Áß?_íîyüø\x0000Z¿ö\x0000Ç\x001f@RtSº{B´È½0Kk\x001e3ÇÅæUê\x0017ðó¿¿½¼¸¾¾ø«ùãîáþoáÏ\x0016øà_Ý\ÞKI.ìË©îgÊ-zäÑ\x000e%Çâ\x000fr£#»\x0014\x00181E>ßñÉr8A¹Y0¸¾~¹{}ûä·\x000f\\x001ft¬£¦xcB-ÁÈÂÞþÜ\x001f56!òÔJ|"³]däSöòâúâ\x001d\x0019ª\x0017÷ûVëë\x0017Ç\x0011`d¢ß.ÀH\x0016ù¡1/ZS<9Ï	ú«8sµ\x000bð÷7$¶·\óÕÅîáõTó3ÏÇLvà b]]¶"O(~\x0013ø\x0004æ¡\x000bô+Z¥Ô2ýù\'¿Û\x001dKp¤â<H.ÚR\x000e\x001c?L²<Û<6¢\x0004)±8}ÑÁyûøíq8ÞÓj0bQ\x001d"³ÑVn©\ÄæcH+Í\x001a'(¶`F±ýÙ¤eÄYâhB\x0008\x0015Â£?órI¹ZóìX\x0017E÷Ï_?\__Þ\x001eDxÍúrPJÿ¶\x0017Óÿ@9-èívÕÔY~xRµ8è|Z<Ê«X¶doon\x001fèß]òr]m/êç\x0007)\x0013ãJ\x000eZPO¿{\x0019^Û\x0017hP\¼¾¼f=õo\x001e.\x0019õH\x0017ì+þÓ%+-fÈP[\x0012Û<fuâó?ñøühñe-f-£]É8UîÉzûD_ú8Ë¤\x0005\x001e\x0005S`Éµ¥EÌ\x0016ºC\Z\x0002\x0019,:úG¨\x0015&td¥¤¿|?\x000e.
¤g\x001d]~êk¯KÛ=£sNUkÇü&Á§q¨yú}|s{9ðß<xrÐëO®þÏÿü_¿½|1×öþL5eÔàèÈQÒ²%-°<CÅÖ\x0006/xÎ¸Xp­fÜ«&R	Ã-{ÅÍ1Kþ?£\x0001\x0015åRUr©¥
æÙ\x0006/\x001dÜ¤3§°ÂÎ^CKTr:Á\x001dº`Úºät\x0019Û\x0015L\x0018\x0013vÄ²»(iÉ¡o\x0017\x0000'\x001d\x001d\x0017ÍâéJ¤[­£]ËWâ6xìà1/	>\x0001XHà¦jó<Õñz¼Î¯¾û>®©à½rD%8©¦¬\x001e_Ý²Å9-c£Øê±-Pw:Ã5ú\x00107ìTçSdêi\x0017ß¤nd5VÏXUÇ Ü2bã9XÐ­p9: \x001b\x001cqÄ·£\x0014\x001e\x001a5pÝD_(ª	ÙÓ
 W,±£=U=\x001bn­ '¿|GaI\x000b0z
\x0018~ã\x0010aÒq´·eSî¶t¹3\x001d[3Ålý	Ñ¾~Ñ\x001bÉÕíµWX{.èNGVYö¬%\x0013¤ÏÅQå-è.vÇ¼b¦ï*O±t¸v§j;\x0008½U¹²¹«®ô]õ)-ÁZFgf\x0015\».¥'ôìÇô\x001bi¥ïÍÅwoôÓúÕÅõÍçÿýVÚSÏhý;\x0015ôòt\x000fS\x001e¡oáZò_ÒEÿ	Ü\x000cy­¨ezWEÃ»ê]g\x0010ã£ë¨î³ÊÄâé\x000bR»
î\x0001^ÒØ¡CVð	qÞ+Ë6Å\x0014ó&xÌ\x001d<F°
éj©¸¼¥V`R\x0006^
ß6ÁAqøÞ	ÂØIÕÔ1vP7NÝÊ¨NÄÎ\x0006.]r\x0002\x0002±ò\Î¢Õà±®\x00140\x0000z/a<ü\x000cDÖI®æ\x0001»¬>\x0005\x001d\x0001»,¥{pWÓQ\x0005}ä6OÃî®~¸í×ú\x000fw»k²\x0007èv\x001f+fÔ]v¦,Á\x000f\x0013So&ß\x0019/=Ú§s«M+]\x001eÕn"«Ý¥è\x001d´\x0014Uò×Ù¬;rh\x0012LmÔã~|í\x0016pþi\x0001·iÉü28\x0013d8\x0004÷H¢J¹\x0015\x0012Õ±ÍH¡ÃÒ­AOÏù¬}îÂ.7>n¯=ÂÚ\x0005ï!r\x001a	2ínÐ]ë4\x001a\x0015\x0011/¬«>¬BÀ=òö\x0011¸\x001a1Kà^xÆN\x0012DïÚÂ0S=%\x001b\x0015tôªJÐ\x0014áú<Þh@îÀÈ'tìbp\x0013\x0006p\x0011L\x0019Õ\x0007/Ý¿9Jûù\x0002q\x000c4¡\x0017«÷4´Êø2Z0^~£®rQèJì<\x0013}@o\x0003×Ç\x0007`A\x000fK2Û;\x001e\x0012®êù\x0008]Íßet	=$¿¹©É÷MÕO@ôÎ(Û/}\x001e«tWçÉ¶[Ðs·í¬,\x0006\x000bÇ-pÈ\x0019¡ë×K\x0014$»n\x0013½8@/q\x0019EÏèäÑ\x0016îÕ¦öìmÁ\x0014\x0014\x000cYè.\x0003¸6G¢\x0004Ëè¦¡§mô\x0004èv\x0019ÍÀèVñî0ºWjì~íÛñ(\x0018q>&~UJÆ*6VFJü\x0012¶ÑF\x000f°vSÎ\x0002·zOtÇm\x0015V@ó©Än\x000cö°X±\x0010]*ñ7ïQÉ\x001eN:\x001c&VTdi\x001d8R¤Çè# ÷è#0õ\x001a]\x001f1*+\x001b¥n>I¥ö'
*\x0007³Ó\x0012OX¬FàY|Çê7\x0015oõ]ñr}¼W\x001d]w¨WÞÆ¥!\x001dÝöÒM3çQ\x0013Ià'§½Ãw§\x0014{YJYÅÎ¨ÈùÉ]eíÈÐ¨­\x0007;l\x0019ù	\x001f¥`Á\x0016\x0008ÈbÂðJ\x0007Øi0yz{»»{\x0007Fæ}»»¿osý\x001e>>ùúâîÝJ\x001fÄÏ48³Ó1¼\ó¤¬&.%<g½\x0004`Á¹Ï´M$iã\x0003ß\x0004*^Rà7>îQÁL[õìáíó0~ñOô¥àù\x001fo^?»y¸»>ÚV%W¬rg­4Ðí½\x001b:Õð5¦\x0015\x000eÓËÓØñÊ6\x000f\x0011\x001càNÑÇùÁ/ÌI»â±¬°"¸\x0003Ô0FH¸mL\x00177¯²"¸\x0007ð\x0012ÏÁÎ¢¶´\x000eàvä^1OíÛÝíÅê!\x0003þ\x0015IÄÿNÜ±"ÒÁâ Pk9(\x0006\x001bj'«a\x001aczlìé\x0007¤íhg5ÁÊa[ì,6£\x0016Z)j©XÙoYåD%,þqìà=ãÈµÊ2>y\x0011ÁÆi\x0002\x000fQ\x0017Û\x0014á_4Z\x0007ï\x001aÌË¼Ð\1¸k=\x001bPÈ£#\x001cæÐ\2^Â\x0005½·D¶£Î*¬<é\x001cV\x0008nXylcyÆW³û\x001e²P'Yt\x0003\x0008AgLe²ÄÅ¡°~4\x000f\x0001:\x0003tg\x0010\x0017ô¤ã>!\x0007}Ì\x001b\x000fã\x0005ïè±_pvµ*¢\x0017ì0!ô\x001cV×ØÏ\x0015º\x0005ô¸\x0010$
zT¦\x0010¡4ÅY}ÞÈì»!Å\x0013ÍîV&ýÜäî &YÐnïM\x001c²q{rñQ\x0017\x001bÓä95I>Å\x0001\x001cä)Õ¸ô\x0019óÇ1\x0017\x0007\x0006¡É\x001bW·ÎùV%=y}\x000bºí^evý\x0002!Ñ¢*Ç%5< Bó>\x001b«\x001d=@&x9®\x000bº×9X\x001e\¤ÑÃê\x00087\x001fýfds}ÇèHeýÂ\x0017ßMZU"§»ÿ¥?÷tMN¢Èñ)\x000e¦a\x0003¢b%õ22\x001ckuÐº
?HØÆ\x000eMÊ
±ÉWË\bTåÉá_ s¿\x0014ÁôÑF\x000cm\x001c\x0004\x0017x(lReÓÁº¹3>
MlÍæùÝÃH÷8.PI:\x0019é °Ú\x0004e\x001dÚ¹\x000füäÌñ5ob|ü]	\x0013ãì¦ª\x0000dÑ5aLò%!Âñ`uðÔ\x000f\x0016OT%k1bD¦¸¨\x0005ÞbIãØ±!.[é¶CaG±gè¼¡ª£e'\x0003gAv(\x0012r\x0008-l5\x0019µAÄz}×J£9\x000bëv¡?å\þ\x0015\x0012\ä!TÕÏ\x00113ÄMñäÞãÉÖð Ö\x000eôF)C¡oÔ6Ûñ(\x0018æä¥ÆYØÑkÕe]¡ñ¨Mñ\x000eE\x0014ìªb\x0019S	ÅX]ÐK§}4Eñ\x001f=\x0003\x0013gá@<n³\x000fój¡¹UJì\x001d\x0018lÔt·g\x0000_² ûg\x0016°§«Iò)2óîµ9¡%êJ\x0014Õ½ÆVh¯=Å\x0017p\x001b\x0000|]p
}µ¦£C.éé{|ùC\x0008ù!*\x001a¼i2\x001ag\x000b¸+Ý8ãAp\x0015eLNGÝ±³¯Ð	zyCXzJ=Ý`µ?gÕP:.øt+ÁÄï^~¸¾\x001aLüêâêÝç\x001fs\x0015Û^R\x0016 F~Kñ½xOÐ°t<¸\x0015R/i¦\x0015¿Æ\x0017:9\x0001M Ú	0Ì×í\x001d®ÄÑÖ$¢L\x000cÒr\x0012²\x000ec¸}\x0001·¡Û~.wÁù¤Bùü´(s)Õx
î¾ÿæâú7c¥/Úàô#FÇÙõÓ\x001cÑ$4_=%'ùáÖØuÆýo¢à\x00088LåÕkõ¸³Ú &`ã\x0018\x0005ã[%*\x0000:z\x001aIÒ3=!\x0003\x0007U\x0011£î32>	sc|d\x0001w®ÇG¤±¿î,¤JekT> ·mpÒ¨!;x\x0004÷Ìçç&3³¨Û!Æîj\x0010ðÉÉèààd¸Ô­5Ç\x0019\x001c6\x0005K\x001b6eÏ:rÂÎì ùï\x001d\x000f|Tw4_Ý
\x0007!`{|4¸C»([M\x0017­EÇåÑar\x000fÑ¡k¿*Z\x001eíc.ÏÊ\x001aÜÅ\x0015^<\x0005\x000eKç¾þ~Êm\x000cª&"¹0ØjVê
æª\x0005\x001dª\x0016x8Ú°ÁcG8×ÛérW'õ¨a*þ\x0002l(þâñ\x0007à6p¬\x0012º×
TÎø¾yj¾à ûÐ\x000e£8_\x0007Û^æC°y\x0018ù§ne´ 1ø%Eå\x0010Ô\x0008zRºR\\x0014¦BÝ\x000e\x000eºÞ'\x0015\x0001"­\Ô]ÉF¡\x0019uó
\x0016\x000f*zµ\x001f\x001dÝóºZ°ÕÿÄ©ZpAX-¸þ¢<ö\x00181ø\x0016êàNCÏá[«ÁU±a2ºM±óO\x001dÝè*¬ÇLD\x0003zYakDtÌ:J/Ý§2<A\¯Ýèµ[1©ãöyp\x001e\x001d\x0013KaÕmÔÊ1;½t#c:bÚ<11¡Íë ùïéÝÔñtæQR9"\x00141o*°\x0012{÷d\x001dÇ\x0012TCS\x0014Õ+dS·ß£\x0008ï7\x0005\x000c¡\x0017\x001d	¶C²oÏø¶O{2zSû»ájNÊÇ§µguLU¶\x000fdÂ\x0003i\x0013Ä\x0002]Õ4"´öªrÐQÐ7Õor ~m4(\x001d ¬¾®CÌÍ.èrO®¨]í½cTù%IF\x0017ñS/"°\x001d\x001d#°Þ,\x001cJ\x001e\x0007'Ïê:pækë\x0004âííG°¿{\x000eæ\x001b2go&:®[ÌQ³ÒÖÂovhMPWÇ¼ªâºù½²\x000cä&Im \x001a2¾bL\x0017\x001f±z-\x000fÑÌÜâ_vªbíèPÅÊ¢3Ý2áá^ªÕ2Wm\x000fæ6þÉMùæ\x0005Ýõ|³©%Á¾®VõÅé×tÆÚ`\x0004÷\x0010-Í\x0005Ëõ2ëx©ÓKoÔånRÖ\x001d½+kB\x0007ó«`\x0015´®V)¦y%y{á\x0019\x0016Îý¬\x0005Ð.\x0002cFg.E`nê=ìè\x0005v4[ÜQfïS\x0005²ô/Ô=âYa>aí÷ù\ôqóöýÇ9ùñþçÿú¯/®.ïÕK\x000b×]ú\x0010\x000fÉ§\x0004égzä§£3BaàGë¿,j	z2T×¬\x001b¬\x000c'ìu*8XkF`I@\x001e°cÆöºvzM,eµçpAÇC&@«`ôÒÑÕ½o)è§4Ë^©ÃXÐ¡\x000eô¢jï¡£ëå§´Hñ8n\x001dÑ+Z9É2-V¯Q>»Ë£I½o9\x001c\x0011\x0015P¬\x0012LôH­Ê\x0007]\x000bÆ:'úÈ/Ìî\x000cøÕ|\x0015À¤v°\x001cë°òõ\x0017 cCÅ¯¡Ã\x0004]Àèß\x000cæºis±·WîúÊ	\x0018ß1Á\x000e\x0011pkGtÑue\x0007è\x0011Ð#Ô{rµäuE=wdÍUoíûË;àºÀ×»Ï?_^<|xòÝÑ 
\x0012iI¹²ï¯±P[äjSj±Ú¨xuSeu\x0013©\x001c4xöV?î1±Ì=ñ×Ï®o¿
Ù6»W¸´I.\x001b\x001d2=)p!\x0014°$#jêÔ·©L½Ó"MÉp÷
ò{T0sÚçÅ\x000f·÷SÀÿ¯r¾~¹»¼º:ZZã:BÜ¹ü80î!\x0000¬<´'³S´"³bBØQµ6yJ©(ÆåË\x0019DÎëÐ(®gÕ\BËºï|Çî=$8\x0015Üry\x0008Up·\x0002÷mVÈøâtð\x0000<-\x0003\x000edWª~æ	\¯¼qÓ¤Ñþéà©Û?þn[K»¢Jè\x000fÞ7¥·%Aâ¾Í\x0017XÀýÂ.Þê(éÜÉèØ`@Aq-çZÝh\x0007O\x0003{M5³£ÿÖ^ßùO+OÙÅ¯éª]ÜsÖõêhÔMÖ¨\x0018§c¾ä¥¿\x0003zÄE'!ÇÓ¹zë\x0015	£l\x0012}sX¹w*@»\x0003}[RÉ\x0002nì\x001b:\x001c%\x00089_À~2·GÀÈuÏØC÷¤o
Bó\x0013|\x0000·Ø<1Q,\x001c\x001f\x001a\x001cGÇ0¸TÝMú\x0008À\x001d{¨»¬lKNWsh·$Çx;:6¶ðÁ$\x0007Æf!4\x001eL\x001e°]ÓÐù\x0003i!¿f=|syýüîb÷p¬{áQk«7K$Lú\x0005¡ïå't-6ê\x0010¦îÙ&Ë§H4Ý¾­8ø¶¬\x001c+ÍZ.WH£­ßÁS\x0004ð\x0008ÑsNc
í^½w¶Ò£5+ÈçñSX©F?6d®:CÊûp\x0002èF\x0017Lïò4ÅyöélWU¤ùÔÈO?òyf6 ?¾ÿî\x001c
ÈÃÈç¿î®î îXO\x0018é
]_àêâ¯¤^ä\x0014EYÎ>­_U[ÇÄB\x0013¦\x0004,zÿoÍ^±ª\x000e®V
e,ë0-Ä9\x0015
\x001dÐ]g@3S.ÚÁª¡lÍ`Ìä9\x0006yq\x001b?½ºXS×âì}þ·wG¬\x001eÓ}½ä÷äCñ)Õa\x0010#æÖ}2'aÆh´	DµM`¹å°×ùy\x0013Ð©AgT¹ëg°§\x0003aÏ!ù{\x0000/\x0003ÓD)Êà0lK	Øè¥,è¶seÑÊ3®bP£QéE}Ìb\x001bD;®\x0016t\x0008]Ñ\x0019öÀÏÉó¼uüØ¢ÄM­x\x0000\x000e×G\x000e\x0000\x0001\x001a¹ÙV]?M«bbm\x0019ÉèèÝàyg}åäcª`dL^'<oE>S[Ø\x0002î{[)\x001eÛÂ<s´*O{V\x0015z±³÷ò}yk×m1º@ßÜÜ\x001f)>@ªE\x0013¦¥¥*ÔV[\x0010ä³NæVoè÷Þ¡R.^Ï\x001bW<\x0003r¾|VRÑ½U1\x001bÁm\x001bðòS\x0017GÞD&MÈ\x001a^W4ÑåÀ«O/vo_oè÷?íè?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ø(·%Êç©ÉýîO÷\x001f?ü´¿]XNVc
0Ñèa\x0011N\x001c6­@\x0019\x001fïþtyqòÝñÙ¡ýX\x0008_ðÅ |¡°µ\x0012ã1Ïë\x0005/ëÐË\x0012½\x001cD\x001fÂ;ï3|ù¦/À_=[\x0003_ðÕ\x0018|\x001d\x000cV4%cÈ¥\x0002íÛDò¡ëÚ{áë\x0012¾\x001e+@÷!°áßP?VÛÁ· xd10\x0017¼­Xr^Ýüôxó¥ÄR8Gu\x0005`­v1OÀ¥\x0017´-he|uyñæõé»ÓÃ¼Ä\x0011¾b¬\x000f?àC
Íæv
c\x0013|ÎunÇïþ_\x0004_ÄeâÁ(~3ýÅ7ðsÚ2øîöînÿðøà¯ýáÛûß/wa.oÔP,Ï[B±0gÑf÷?¾;;??¾~\x001d½µo/_½88õ\x0002¢p>mL\x0004QâïaY¤Q
[\x001bÓ\x0012ß\x0003w&Ö¸mö©ÈRô÷FY ÃwX\x0016+=Òà\x0019\x000f\x001cI\x0016*§\x0008©­.\x0003¸g_ÅmñU,¤6ÓWñRâD\x0015÷\x001c8À\x0008Ð#JøÞ±w§pÄ7ðó×ëúâð\x0006à\4¹\x0001\x001eÙê5V\x0000\x0018Ý`ÆNÝw×õÅ!\x000eøwfÄÒbÀÏQ1¸ñÄ\x000fi-£Íl.OyÝLht\x0011¿ðµñ{ì?\x0011TR·Î¦h!è3JÇäùg\x0010äýsAÞ\x000b"qàÓ:`|U(	
,rÀJò>èôØ\x0016O^ìð\x0017ßÀz×\x0012K`:N=.²wa\x000e\x0006\x0007`B·ìÇÒÕX²
1üüâ!g
\x0004\x00198(¾TÈáÏè¡\x0016!ô\x0000BËã»»4\x001côòî\x000f·\x001fz§Ò\x0010\x000f°86>ÇnÓ¦cq|~~æ^ÿùäìâ_@k_}\x0010Ý m¦o\x0005E.5ËË=\s:b=jgKÔÞëF=íP=:¡Î½]º9ï¶\x0006µOýøSøëY"(I.ÂÓî*¸Ð»ðëÇ¥¸¡e;q? \x0004.Î¢\x0004};ã°½Ý]\x0005\x0007z\x0017~½G®x\ñ!äy	ª ¥²\x0000æLX[¥\x0003¸©Ü\x000c\x001d9ôàÛ\x000cÜÓ:\x0012»&­C\x0007r[\x001d¹\x001d:r§(9\x0008Þ='Vw{L5/y\x0017rW!w\x0003ÈaÄk®i\x0005\x0018Ýi-}\x0011½\x0003y1õ\x0000ÈÓÔC7t®h¨s¨4B¼\x000bÃmè=ÐuuÑSÇ}7ô\x0010
¢rñ°Ë\x0003\x0013C~d;è¢`òÐ-Í\x0006 [Î©ê's/À\x000b\x0013ÄØä
!`Ä}âÿñ÷\x0014ö½¾yøÇ~!ñ
\x000c\x0014âlg$\x0018À\x0010IÑp¤=ÀzI±ÞëÓëwÇâ;¯ãXþdñ=,(#£ÝÕÍÃÇi\x001cÍÄ¨×!@Â|ÏSÇe¸ê\x000b¨\x0010®N¯/\x000eæ"h£U\x0005\x001a~wf¦hCtàtr®\x001csé¤Ãÿü,ÃÍBÐádØÎzß{ØàT%Ü\x001aH§ùqHö\x000bz¥YZ\x000e8ù(é)XËQ%+O\x001eîo9ßÂj\Ã\x0014ô¸FöÈð¿s/Nù&{õ\x0004ùäúòìïËiAeÝ\x0015îo1ßK|d\x000cT"²{°&MçjÈ¾ì{!+­Á\x001dÑ	²TH¥¢Ú{Ò\x0016C\x0016ÜÕý0:û³¶ø.nÿu{óð»?|{óxó°°f D\x0017lTÊÁ{r`÷ì¤üàßÜ]ý×Ùéõî<úå§×8J¢D²Hn(\x0011u%\x001aíó:\x0008N]ÝáÙ6;^ÇD\x0012v
CãGßÈ¤áÓ$þ\x0004¥Ì\x0011\x0019X,2\x001a¯Û\x000cr½2q\x001bã=UTOÀÝ®ª\x000f·?ÞÜÝ,øTZ%\x0018ª¸óDî\x0018\x0014õÒÉÙËÓóÓÃ1_B>¥ë\x0001¹v#ÈBsk\x001cp:êqán­]\x001a
×%êø»\x001b·ô^à®\x0008ÃÃR®P\x0014o¾uØ¥®GÃ_¤Ñß)Ëøòaÿñ5%~\x0018¸KIßà
S\x000e^r\x0008*9çª¹lÊ0¾¼>¾øv¶Äà\x0017í,\x0000ß¨1ø!ë£çÌAÉ6Â·ÈÙ\x0012B\x001c; ]\x0003ßù
¾ócðCÐ\x000e\x000b£k{¾\x001a\x0007vä
ÑÅ^ÂN >Þ\x0010ßFO\x001bHSã¾©/W¢gâÙ.xàÒ®×aí^ÜÜío\x001f*I¼²'"/r³£k:nEyüÅéùîøìz\x0016öÄ\x000c°\x001bí8u%\x0004\x001bEg^\x0012G]°Ìy9îU\x000ep+1Û«Ü0§hÓ­\x0000ÆÞ{~óØbÜSÊ\x0017pkß[\x0001åxO\x001c
&{MK»¬kF­kps\x0007%\x0001á\x000bÎaó
ü,é*/ïnÿ±Ø(ZÒ\x001c\x001búa\x0017P¦Â\x0019ÍªõÓ×»Ëó³wsÔ²\x0008½¬â%ðû~ô@\x001bZ\x000f\úPX«1ûkXseT'ú÷ÏÑ¿ïG¯`Ç³7tö9m\x0010Î¾9Kµ
=S1
/¨L\x0014ø\x0003¼â±:ùiÿ¿ì?.Ì/qHH¦\x001bïÂuI\x0011
\x0004¼4Í\x0016ý"Øúîø<¾8_JØå´¿&bßýØ5\x0004Ê\x0011»T©!?x\â¹K;î°ëÈ\x001ef¦<¼%Sì=¹ÿûÓÍÝíûO)û=tÈ¥Ô»Å\x0001,Ï0Ànú\x0001¤gN.ÿãíéùÙÉåC7&!÷\x0015r?\	ê\x0019pFÒ²\x0012#%¥ÞÍì>Û\x0015Èa\x001b@\x001c~\x000e@7ä:\x0006oQ\x0011oÑ\x000e\x000fÇüøfÐu
]A\x0017G\x0006\x0013Ø0\x0004íªc\x001c\x0008½6îjèn\x0008:±Y\x0006ßöY:À¡¼
8·Ï²Ø¸\x0012Â\x0000ÁêÖùý¿AfÖP{\x0000Å¤Ï¥ÏmÄó+ßî^\x001dÿ×,Ü¢
	©!Þ	×\x0007äì\x0016Â3%úM9O¿¹\x0010­«Ðº^´¹OX\x0000{/ÁÍMÚBo·H±C¦Võáå°Å\x0008û-M°*IMkÀ+¿Õm(§\x0010â}Øw\x001e±¤Â®°H:È»ÿ¤m\x0006,¬M¢$ó¤RÑíãÍ/\x000bÏXg>#Çä\x00112Þrªq±9êl(\x0014½>ýó,^_áõÝx\x0005§\x0019Më\x001d´ãÄ\x0003Æî\x0000¸¹n%b1M\x0018\x0000bøÙ\x00079(uj°\x000e\x001eæMNS±¿Y\x0002]\x000c¥Æö¢\x000e\x0000}ùþ\x0019Ëäû?ìïî\x0013æ¨p'ðÇ§ìUL\x0015*IÖ7[,*¢É\x0017×\x0017ß\x001e×9
)¦=\x0014,6ßKÁi\x0013½gµ:í©Ûî\x0013é\x0017bê¹\x0000!,ß@\x0008Mä\x0004lFÕâ´Ëôe½Ë¤\x0008ü÷õr¯ kEU)\x001cÖ7«f¼¥$\x0016Da.yx
ÅbÍyÄI\x0004Èb½<OÂEüø-\x001bÄ\x000f;ARÔ\x0003hìâÐ7\x0016ñ3«æóýðï«KÃ_DæÒz,twõpÿãâµ\x001a\x0016z\x001d
\x0000éüsN\x0010¬ÙÐ^Ïî®®/_\x001eÚ«ñó
ÿ¯æ§×â÷áÊ'ü°×\x000e³ V u5¼9ëÑ_Tø51½\x0012¿W4*$Bã%C\x0000GüL¢É\x0016´\x0012?\x0001\x0008!&ÖgP\x00185mû»¿,4b'¢"¤	Ð««ÈuU½dÉÆéõ\x001f\x000f\x001aÞ\x0008Ú(^ Ã¿×£Å©Äàá}wnAfn!h_öý ajÚán¤á¸\x0007QsÐðhzé+A\x0007_Ê ãïNÔáßÆ«m`d\x001b×8ËpZ5\x001b×\x001euøQn2I×zß}¯\x0015\x0004\x0016é^\x001blÒ\x0008÷ÚÑÚ%Lò¯HÛ+Þ\x001bö®áê\x0018	ËÌ\x0014Þ\x0012C·¤=\x0017¿\x001c7F\x0005ñM\x001d*ÿñþéa÷bÿq·´¬bp=5*¯¿\x000e'13d¤ç\x0003¤?^¾½Þ½8¾8>\x0005_¢ÀF¤ÆÐ[Mé	\x0003©~AÅ,jñ^ÀS·
=+\x0003Óxøû±ÓÏk¼M°¥D×£¤#üócÚ\x000bñKèñ®Xjæ¾ÕZ°§¥¦SxÆ\x0010¹Î¤Ô½Ë¬§ulÁ5[²\x0011ìíá]fª&}½`üÙÆ?í\x001f~¸ý¸´>\x00119¦\\x0002phLJ\x001d""²\x000bXö^ïþt|ýíÙÅ<p©KàR\x0000\x0017ö\x000ejeiGlø\x0010ÏWã\x0003/:\x00034-Fsj²\x0008À\x001df=¤M»ík[\x0001·#À
·:_\x0015)ó7§Ö!·¬Î\x001f¿¨J*)@}µÿtóðñæîné`Í3;6ø\x0012\x0007\x000cqÍx5'Oñé«ã7§×\x0017§çç\x0007[Òf\x0004_Ê\x0000?GJ?ÊàÅqêçòÊÌïZ*\x0003\x001büxÁ´\x000b{ÍXµNîÅ]f8^$äÞnýQàÙ¤1_!\x0004m\x000bÜ°\x0017çàx\x0016¾ªá«Qø\x001e§Õ\x0002|FóÖBHMðçEè¹ARQäÕ{
?Ëêýß\x0016f\x0006`¥}Lk\x0000¡gz¹0´½ëJ6_nÑN}ü\x001fÿ?wï]ç¤N\x00130\x0017.ÛÒ\x0013%Ó¶¼(ÒII^'ûÅk[fÚª#KnJr¬§F¿õcÏ£gÒ#9\x0008 \x0002\x001b Íÿ\x0002Yvwwfy³*«¿À\x000fÄ=¾x½ÌÚçí R8î	þlóJ\x00177o~ÙNÆ\x001fjÎî\x0019/,M¬ÅøÃQ²kÉ|Ý/ÎãÏål£QL\x000c´ÑèÇ§\x001f>¿}÷îÿ¯­>>.U\x0015ã½¸\x0010o\x000b"ß\x0016·ÐZTù\x0004O¯^?\x000f\x0015\x001d7\x000e\x001f?ÅÓãhñ[ÑàÇcø¥t\x0012Vp8)1%P\x0011]à\x0018òLøá¸,\x0014á\x0007íÇà#ÅR¾öà`4¹òÒ¸ÌX$¢\x0015Xaß_Z	5þô{H\x0000\x001c	©|\x0007&%Ì\x001cRÌê\x0007Ù^ûðW]\x000c	¿\x0015ø§&Þh}\x0005ã&áWëÚr\x001b~ù*¥\x001dÿp'¥ýý
aß\x001aH9\x000eDÐ³§]í¼Ù\x001b\x0016X}¯\x0002\x000fª\x0006\x001eÔ\x0000p\ï\x000b¹ÙKhæÍn£zxõù~àZ4Àµ\x0018BnÅ©Í^Ø±æÙ
g\x001aûÀ§\x0001?Îá%àZ\x000c\x0001zôÊXÞÖi<v¿¾H|3r¯¡F?\x0007ã\/\x000e\x00029\x0006:ú\x001dÔááÁaÝÈ¥WÍeI¿û¡+%¨9
;Fqä7u8I½êîÁaÙÝÈUÕlÈÓï\x0001äQÜèûÍí
\x0003\x000föîG^oUDäwÖ*îD.1»dò8!jpÚ@CyáA"õ\x001d¸\x000fQµ6)½³ø\x0007Lé}ùá×\x0008+­Ï~9¼q\x0013M\x001bc×x×¸\x000f\x0006WgÝ¢­.%\x000fN|yõ"þ5®Ï¾9»q\x0013M\x000f\x001b£"®%ÐÃ\x00126À
\x00039ß¡\x0001I³îÁ¼A¿\x0008¡\x0016!\x000cà\x001dÍÆ¸\x0018³2
 \x0000''cpû?Ð-Âí9Ý#1.?éY¦F\x0006\x0008ü\x0019ôäaý2@#\x0003_%G¤aNE·,sÕÇ«Ä+Â|0°_\x0006y\x0012dy
Øh#ó:\x0004Äþîðþ§\x000f\x001béSµ´ÌL¯½:.3áêª~ÐZ]\½B¼\x0017g_^]>9Ü¾¹ù-ÿû]¦iú`b¿=Ýsè\x0013LÅ\x0002Æ=¨á·â,m\x000f	§.*\x0000\x0017\x000b4fÄh.Àv»è\x0014tá\x001fìo?ÿã×ß(W2Ôß\x001e~ÿpûþCjS#ç\x000b\x0008Úõá×\x001fon?}qóþ§¾ù'¢ó>hH\x000b@à\x001aÁÔh	Ñ\x0007ÄØ\x0013k\x001cÍ\x0016Óë³\x0017OÏ¯_}q~ùÅÓ×_ÿýÉ·gß_]_^=Ô¥\x0006?üÛ/áÓ¿¥AûröûÍû²¸ëëÃOoËÖ®Mh\x0015g\x0017£³\x001d`>Á\x0015X
E¸ \{öýùeYßõõÙÏ/\x0017_\x001aðÑäªaðÆBh\x0013MîZ¨Óè¨!ÿ=^.ý=øøä`üàáÇ­A*\x001f¼Ýè+p"ö¨ÖÌ\x0004ìD\x00012íj
\x0019¼Âx-×\x0002>:°v\x001c<W§\x0001«95àËÉËj-ÈDðñ©\x0000
1çìGð)àñÁ>\x0006øh\ý\x0004ð*õü\x0003n¤Î6\x0007±ã\}:xQµLOÄ\x001eu@\x0018Ç®i\x000b\x001cvù
d<Bð:\x0004\x0002\x001fÿÏc\yôZñ_è!È¼\x0018\x0019ó\x0011*wHEô+\x0012z%\x001eCS²\x00030ÞË¼V
kVÔ\x000eUkæDôÑºÊ	\x0016\x0016l¾6HþáéÎ#ÅT:xWåA'BwQ\x001bXl@ò\x000e^dÚQÐ¸×\x000f^?ªÄ0G[XíBæ¸ÁKosÛ\x0017`\x0015²\z÷\x0018O\x0016ÇÔ'Ô»té]ñÌb\x0018Df
$<¦ÇÄ\x001a¿ô8l\x000cìÊwâÍA\x000eÁl¦Üãxf?üøö#zgø_&89¤3£O£ÙÉ\x0011j\x000cêã»ÿímå\x001a\x001f7	ux\x0017ÿG÷@wÞ©ÌÉ\x0007È\x000cIwGAÀL\x0005\x0006P\x001fâAèÇmÂ_]<»Ú\x000c<»cÀ=MU\x0001ï#9\x001f\x00027ìT\x0004¾ ováöú¿¿·U\x0010HÑ§\x001f°ú\x0011Ç\x0010.zü_\x001425\x0000(äÍu=ä}\x000f2eG^aÿôCÍ
Ø|;þÌ`Qÿ|\x000bÊk|ys{û¶\x000e7Þ\x0003Oo/z@.ÎÇ{ §{`,þËóëëçç\x000fwÓEïÿaÿ\x0007\x001apÃCú·gØ®H»»?üúëáýO7·o·Þ\ÜCa°à+E%.:N!5Âå'\x0017
±ø\x0019v-Ò\x0006ï«\x0017/Î.¿<¿~pÙ\x0006üðÿø·Õå½À\x0012íÍíÏñ¿\x0008wÄ[´Qa ±UD® 2içsº\x0018Æ,(\x000c$Ýù\x001a¹÷³\x000cg\x0017\x000f3\x0018Á\x000fÿñ\x000fëÿýw\x001f\x0003Æ'ø¯ÿóÿãÛ_ß~:ü¼ýÌu Í{ £#Bñ¿ñÊfÜ\x0008p°úäóë\x0017Ï_}ýPI"j·¼ùwµ+û·ÏÃ¯ÛO;Î7\x0008®oÄºLþ7àòÃk¨ëî\x0001ýÛë³x¨/Î®_á¡ÞO¸	åêºIþÃ²þãÉ\x0015êæÇ\x0017o\x0003qtF°ÚäF\ÐN³çáXÓ²\x0016~yr\x0007ûð\x000b, u
Z\x000föìì!\x0012¥$pW&^º\x000b{AC
\x001aúAãÌ
]\x000b \x0005r\x0011´!5\x0017A/eßv¦r\x0008_\x000fÑÚG\x001cr(æî\x0013\x0014y
\x000bÑ^ÔÍýý\x0017Ä\x000bW(DÔyBF-)sâaÉöíEí\x001aÔ®\x001f5\x000eVÒµ¶&ÏçFÔiEFmW=¹í¨}Ú÷£F\x0012³ãY\x0007:kìêâ³§AhNQ\x0001ÔpJj/Æ^:(G ÍRd'hÕ<F5ð\x0018µ-×ÚQ\x0013? Ío\x0001=ï-ªÆÀ¨~\x000bãµ@êç\x000c(W\x0010tÑ \x0006æ)kj=aÔª\x001f5R©Z\x0012jÜæD¨²Þ{Q7zO
è½xA4_kÇÖÜ§ý\x0019µx­\x001bÃ¨ú-£{ð2j Ô
Ê
±\x000by³½¨MÚ\x000cuÈü¾:P\x0010\x0010od7Ïø¯Ñ6¨m?jÌÕ\x0010h\x001b­ñ¨\x001d»{ÆM\x0004Ý\x0018F5`\x0018óÚËãQÛò\x0018ÃÄkÝ\x0018F5`\x0018­âL6N*9÷P\x0010«&^ëÆ0ª\x0001Ã\x0008¶óZ:º!Ò\x0015Ôónn,£\x001e°Ö\x001a\x0002m¹äáÓwÞÂ¼£Öm\x00143 ­Ê\x000bË3jké¨+Ôólnô\x001eÐ{æxÔ!·ØEÐÚð[´v»§\x001b
¢\x00074H|LL(Ý\x0003\x001eTy~5Ù¸\x001du£At¿\x0006	"qcdm­9\x000få¬k®aÔ\x0006Ñ\x0003\x001aÄ\x001eCÆ\x0018óR1\x0003\x0017#\x0010j71¥\x0000
\x0003nª#RCÊÚÞ3ÀzÏ©y\x0011\x001a\x0015\x0002\x0003*$úK\x001c¾à9©àmqB&&B Ñ 0 A¢
§J£\x0013"·÷!hÇq.r¾NCÝ¨\x0010\x0018P!XVZ\x000bâtAmçµi®µ\x0019¸Öñ\x0005º#jvøü\x0011ô¼£6Í­6\x0003·:ú¨-ië \x0006±\x000båÐ½¨\x001b×Úô»ÖA\x0005ÎPÛ X[\x0007åKÞwÚ3Í­6ý·:HqÊOQeî9í"Ò]4\x0003vQCIá\x001eìî\x0005]\wº±¦ß*\x0006YBs<iÈ¹ Õ#<DÛ¸Õ¶ß­\x000eÀµe4å\x00191Söóômôí×wA:*ÍI§h1\x001e³æ\x000b\x001d&æml£ðl¿ÂCZ\Ê¤eot9T¹Ñ~bÝ6vÜ\x000eØqWZµÐ©6\x0014ã;Ü\x0001)U¹P7\x001aÏ\x000eh<å¸×ÆáQº!ªx\x001f>L¼×ú°\x0003ê\x0003Bf\x0010Cõá¸2F\x0002\x0005õÄÜ¯k^£\x001bx òæB<kÇiö\x0000µÞ¼´kÞ¢\x001bxmxÈlV\x0011°-%\x0018·Þ²ã!\x0012§Òñ)\x001eú½SqjÉ$â?²O]"E?/\x0001âdê¼j¯\x0008þ¥ÛK\x000e\x0018Vy54sMy fêìp\x0017||\x0003à½±lplÐ§\x001a(\x001fR×nâÃ´î\x001ex7tòÊq¹ÓÓ"ñ¯O~\x0002öèL¶\x001d\x000bè]V:åé»ÃûÄ\x0015²\x001d·ÈCÌ©eÈdÂ\x0001§á©åÍ-%Ç§\x0017g.d\x0003vUcWcØ#Äl5\x0004îWNY`ðbÃmß\x0003^×àõ xO1ÀÝ!cODè	»ÚÚ\x001djì0Ýè\x001cê\x0008ÍÂ°K£FAz°\x001a»\x0019Ä®(z\x00102ð(H\x0004ï4-µ=àm
Þþµ\x000eÞÕØÝ\x0018ö\x0018Ô»\x000c^	.â ª¡ñDczú{Àû\x001a¼\x001f\x0003ïò¦9|¬æÔ´\x000f^n©\x0006ïÁ\x001ejìa\x000c»°°0\x001e<ÆtùÖXÇmÍ¦f\x0001þØ2ì\x0018C¿tå]¹5Ê¬ñÊ/M#ôoô¤\x001cT:¯k\x0001\\x0000NÁh4P
õ­«¯½|ík§æO­r½ãÜ8[u_Þ|þÇVÐA\x0001°\x000f\x001f¤È\x0014çD-®\x000bº:¶/Ï_µ\x000eWÕpU\x001f\e\x0012Cp¹u\x0014çB%Á5K6i\x0017\]ÃÕp1}Ýø\x000b|\x0012\ë\x0019®v\x000b×z\x0017\SÃ5pH+\x0007E>^a:\ oêM\x0011C`+µ7Wt^]å9Kið\x000cWÇ\x001bMp\x0017ãæ]x¡Á\x000b]x}7@å»ë³\x0007\x001e5äxs)\x0001´ïÞ6-Ý]üCÏ	 ¸}\x0018Ù93\x0001ò¨\x001c¤\x0019½¾RC«Ëp\x0014\x0007':ß½»),ÏÛ/0\x00127):bLò	°\x0017`i¤êââ¼p<¯CÖ5dÝ\x000b\x0019;÷©îäDNÁ\x0004YpWhpÓâû \x001a²é¬3ôQñR}\x000fá\x0016àðNÈ¶l»!{wJ96\x000fþcôüÜÒ°ã>È®ì:!û\x0010d©*\x0004Àé¬1\x0014k\x000c³dwBö5dÿW8e©\x001a¡úßÉ\ßøþë\x001bß\x001f \x0007¿4´\x001334¡\x001b³\x000eÌK:CÐ´ã\x0001Åiõ}\x001b!»Uz-	@9e\x001b\x0002ß¥Ñ\x001b!ûu\x0006N¤ó)óÄ\x000fp4&óÔl\x001e ì}ÑÇp¨\x0013f¡qKmÂ,8%X³àgìÃ¬Û¬{o³æ"³FE\x0017½NGuÏÅ1$1wkïîtåî»ÖÂåMÀx­\x0005\x0016ËòµÖl¼Ã\x0012áÈN\x0015ýÃÿî­¦¦¿uÞp,7\x0002¢)itÑ×KÃ?»Oþ\x000eøxòýÐq=¦.ÈÙÑ3\x000eæ\x001d¼2þÎÔc\x000cå¸ðùäÅÏïÞ¾ß
Ø¡÷ü<\x001dUæc\\x000bG\x0013°R¬¥±_¼¸z}ñür\x001d²ª!«~ÈðzÎÈXM#V\x0011ïj½c;^]ãÕýxq\x0016!;f%°Ú#^b\x0013Ù	\x0019jÈÐ
ÙéÜ
ó\x0011XE\x001d ÈÒ½.Ý\x000eÙÔM?d×\x0014dÈ éË(·\mZÝ\x000eÙÖm7dës-B\x000646	²ô\x0005²v1d«.úõ\x0005\x0004dwDÌØ»
ÄTA
Í\x001a5Ç4ÈÍ]ý\x0019»iÈ\x001f,\x0012¸¥c6/³qÌBßQqQ{ûæío¿}x÷ÏO7'\x00177ÿüõ°^\x0001Sÿ¤ëðARÞßJÂ
Ki\x000eÄýÍóï¾»ºøû«óó¿¿8[¢V(\x0002@-\x0000\x000b ü©&\x0011<u
+\x001bÊÙÃZQ\x000c¦ÁË i(/
\x0011]<¢,6±f!ÖjG=2ØZ\x0006;A\x0006¹Ãé":ã$³.üÊÃí\x0011ÂÕB¸	Iº\/~ãm¢fh­
}º\x0010¾\x0016ÂOø\x0012.ÇxòÃñ6\x0001»\x0003v)®è\x0015"ÔBq!Ò¶ô!ÈKS±\x0014¬Y\x0006¿Qé¡"r2pUrè:\x0001µü¤ëä4]'(·i¾~­ì0
!'|	
2r\x001b\x0019Ü?\x0005°\x0014~­c¬GÆÌÉ	v\x000e\x0014E¬¨¾ó\x0016g\dkÙN8=_ÇV\x001c\x001b(ò*,ÑxÅ»¥=?\x000b\x000eNÂ\x001aB\x0014Å\x0013L¶¶T{EB\x000f"MKó}Zóðzdh,¶`²Áq\x0010ð\x0005ug\x0000\x0006p¶yº\x0014Í\x00136Rö½úØ\x001fgØÞyñ\x0008ß¢1ÚrÕÆÖ>ºOQY	ÒP¸	^ÅÚd^\x0014Á\x0013,±å[ð\x001a<ì£°ü-ÂÚ¤^\x0014ª1yjÉsòT\x0015!D81åS¬\x0001õ\x0008Ñ<5ÁäY Úd"Ð³\x0000êðÆOñ\x0008R´Ý\x0004k5,\x0019\x000bÇ9\x0016ç\1\x0016jþãVÉS\x0013Luy3z~Ülòpåq¯4\x0005öHÑ<5Áä\x0005íêù[\x0004"æQ.ã»x\x0004)\x001as¡ÆÍ\x0005¦ý£o\x0001ìû´Ú*K1ßæ©ÆZ¨	Ö\x0002k-|¡\x001cUñ³Ü\x0013\x000eâ\x0011¼rÕÄxj<ÈKìäÏ\x001aîøPè \x0014r­e³C
ÝX\x000b=n-¤¢4pæÓ¥\x0004W4³¤A­åT{¤hÌ`.¼9~\x000bA¼¨hiwÆM\x0014ó¥hÌ\x001e7\x0017RÑÞ\x000c!Â}LùS°[\x0004ßóh¬`-¨\x0019\x001d[K¦"HöÉå#DGº,ôxd-\x0003>\x001coû2p\x0013ßÄ|³­\x001bS¡'
|\x0008äGÛi¤çá>
fo§GÆVèq[!¥â\x0004á%\x0017/£òeºdX\x001bÚê¢±\x0015z­ð´Ö1uQáLQ"\x0014Ör·ÆuÙ#E\x0013\x001féñøHJWÞ\x0005z¶ä|0K`ü\x0016kô	\x001dR@cñ`ÅÆD äM² "6]
a\x001b©GÆàÁ¸ÁÊÈ"(¢!¶"Ç=_ÆRÀ¸¥± }	ä\x0015§§­\x0014_§ÕÉ\x001e)Úâ×x\Æu \x000c_HºOÀ_Â(3ßõÆäÁ\x0004Ë\x0013I
	Ôq\x0016EQP«a=R4&\x000fÆM^¼:y5z\x001bÌ\x0003¾ªÌ³k£×æÂ{¤h\x0005\x001b\x000b\x0015\x0003;2ÜQ+qA58¢"ÑÆ¯q\x0012vHa\x001a5kÆÕ¬Ò\x0006Pb¸mhÌ=JÁy(»º¨£GFÏ	z6DF¯ÁaÎ<I!Y
xÄ¦i\x0002\x000b3\x001eXà5ÊÌzÑß·4\x000c¤§
_zÄ°GÆ\qs¡ n/!-\x000b¥Øû0«Ý?=R´}\x0006ãV)·¨Æg[)I
Ëîq50WnÆ½r\ÐGµ<e
1\x0012D=Ë÷éQJ/M\x0003-\x0015xpr°.élI\x000coî-Zaiï`÷ë¸+Ñ3QÂÐúÊèhÎ\x000f\x0006]µVÏ=²Hi:ÝØR<±Ç&®/?¼ùtóùöäÕÍ¯¿}¸=¼Û,\x0005ö\x0011\x0011O~nîÊ>²Õ»U"×'_^={uþúúäÕùï®®Ï.Ö¥°\x0014v\x0014Ñ\x0005a61\x001e,NK/ju¤»G\x000cßá'áÙÁ_G3S¤OTLr\x0012 C\x000c'j1ñ5Ü©¶DÎ¤¨\x0016x=Xµö.9T#\x001a#`\x001bW$\x0007ïxEOÅX\x000b7ºÄÐ\x0018zÂç\x0000\x0014
¹\x000eÈ%Aº=¦pZ-ðuÉÑ¨*7®ªâç\x0000
9\x0012¿¢çQ×Ù\x0019{Ä0\x0018fÂç0ÇWðLÎ\x001dl!\x0012ôò\x0011kt®\x001b×¹!ªWª!\x0005[þ\x0016Gr*¿J÷ß#kp3Þ/üH\x0016Æìw<a}¾\x0018ápã#~\x000bÏ\x0004\x000f¸\x0006@y\x001bñÂC#Fð5p±\x0001¿ðÂ\x001cÛV»ïzäð\x0001ôã\x00060ÍN[zâJ\x0012,Ä`-GX%*ïC6rÈ\x0019ßCÒ"Í(G \x0008
¿\x0007o}ÁÅÕóåh\x000c¹aÈ?Z@CéÏø=Êö°º\x000f¡GÆ\x0002ú\x0019\x0016PGÿð(£{e\x000b\x0011ôãÈÑ\x000e?ÃtDFÈ]^âGº
kíó]r4j×ÏP»\x0010Nm\x0011ýC_üªUÚ\x000e)B£­Â\x000cm½x$3)\x000fÅ\x0004®²\x0006öHÑÜ©0ãNy«ÅÙYÏ#\x0019 -\x001e~¯Ñx$aGâCaÎÄa\x0000\x001aH\x0017w·Ç\x0008\x0002CcËÃ\x000c[\x001en®ÒEçÊò=0S2[\x000e)×?'\,Geqéó< 50wÄêB¿\x001e9d+Ç\x000cc\x001e? ãýÜ?\x0008)Ý WWWö\x0008¢[AÆãÙ¨\x0002³;¤Ü¦¥Ë\x0003\x001f\x0006J\x0001­\x00183yp¼ÇÅ(\x0004Ha\x0001/\x0002\x000c«T]Vñ6~#M| Ó$ÌÅ\x001d¶\x000cÞî\x0017Äµ«Þ\x0018Ei^¼î.PÞJûâ¶ûù¦P
ß
2Á/ÿKeÃAYcäJÉ G\x000cÙj^9Aób\x0013\x000cQÆ³g"\x001dgJÂêÂ¸\x001e9ZÍ+Ç5o
?4ÉayGX\x000c?
ûZëêî\x0012DµL£RC\x0015É¡h¿;òæ°\x0018\x001bÈ"öÑ\x001a\x00109ÃD1Ø \x001c),ShúÄZ÷g ­	\x0013LQ¤´5å\x0007¡ËÅz\x0004%[\x0013"g\x0010¥xY\x0010ê+Ç\x001fMáj-­KÖÈ\x0019\x0016Dq#hü yþbÈ\x001fä1|^Ù\x001a\x00109Ã`~tMr\x000c¢\x0004èbÑ;\x001eÈXH\x000eÕZ\x00105ÃhS\x0016Â9 Öø@
S^#}èù ªÕ¼jæp
é³rÃ:(Y^ú#Ü+Õj^5CóF°Ä=ÐpÆ¤h^µº¾GVóª\x00197FPÄùë¼`r>%\x000b©\x0016G0éªÕ¼jæ51ºå(Är\x0014"ÂÑW|
T¶\x0015dBþGâÎ[òy½Î}2ñ\x0014Í\x000bP:ª5!j	±e]¨3&c*¶<ÇðzUkCÔ\x000c\x001b\x0012\x001f¸£ì¨çåëp
au«e\x001cºµ!z
±ÀN¯\x000fäU³&°ºÿ¨G6\x0008Ñ3\x0010w¬I\x0019ÍÁ­<zïò\x0011²ÕR·¦PÏ0èX1e®¤1~PPîÕcätk\x000bõ\x000c[èe)æäUO°.Ñí#\x0014	¥nm¡a\x000bq4Ý,\x001c\x0000fgA\x001e¡MFêÖè\x0019\x0016ÄùÓ#\x00153ùÊ\x0000tó\x0018P·\x0016DÏ° \x0017DaºRÅ7yö+©[\x000b¢gX\x0010xÉ\x0017¢\,Ïm}Á¬ñ"u	\x0012ZAÆk!\x0001gfA/Bª÷¸\x000eô#$ä µ!0Ã\x0004ÁõNÜ\x0015Er(/ä1Â[hM\x0008L0!Jhî\x0007@\x0002å<38åb­
Lt	Òª^ zð¼rÔ\x000bÃ_D\x0005^\x001aìc\x0014§ 
C`B\x0018\x0019ëpL(Ë\x001cË%P_ã¢ë\x0012¤5"0Á(\x001c¯ceKê$òEV÷©õ\x0008Òê, ³0×+9ub)[v ³Lëf	n\x0016¦l(q!¥\x001cd(~/èGp³LûDÌ'¢\x0005û>¾\x0016MO$(\x0016\x0004©Lç\x000bÒú'fÉÅP¬"å+J\x001dÚ<FkÚ\x0017bf¼\x0010Ì\x0001Ù#
?)_Y²¤¢|mûDì'b-ÌÇ÷mXù*\x001dXù:ù\x0008æÐ¶OÄÎx"^pI\x001d¿\x0008õÎ(c}ù"`ElûDì'â\x00037^ú¼®0	bË\x0017±ÐÌ$mûFì7Ë\x0007èHQÌ!¶¸?¢Òr­ëë&¸¾JYvá£
,+ôdq\x0019Ý\x0006\x000e÷ý´}Â4H\x0014ä¸J:¢\x0018\x0003-Byë>±ÍF\x000eØË*Æ¡BtähM\x001c·Ä*{´&ÐÕ$¼¿+÷SÄÁ,\x001d'·pY&gé\)M¯Ñ\x0019÷=ü\x001f>Ý}ú&|\x001a(G¢\x00123¬Ä¤+JìQDùñ®(?N	\x0018=/CÓÄ<\x0011ÕXù,Ö?Ja÷Þ«s®Y¢½gárÚÂV@õ\x0018eÑûJ@MR\x0002FÜ6æW(u'=ß4xº/ôuRi4^G&Êê=ý\x0018©úørÞÜ}9o&(\x0001¦\x000eÆ}èÔd%À_ÆOÍ´ha~h¶ùÄ?¤E¿ß¼GAnN^\x001e~ÿ°}È\x001b[¨\x0011\x0002·ez2Ðñå³µ\ZVpöýù%Jp~òòìû«¥ñnÆ­kÜz\x0004·Ñü"<²\x0004çð]RE\ÒWûq\x001a·\x0019ÂÍ|iQ\x001fÁfµäÂÔÓ¶5j;Ú*n3AçÒpú¸!Ì-õìï\x0007îjàn\x00108n<Ú\x0001Ú®kYÑ,/ìÛÛ×¸ý\x0010nÏoxàü.]ÙÚçZ\w\x0003?ö¶&}"F\x001fK\x0001^ynuÓ¡Å7ÁîFÞjÂ\x0011U¨(\x000bap2_òD÷IeiÍõ~äÍë#ÏSÇÈ³ä\x0000¼\x0001¯2BKÝSû7·\\s\x001dU7'f¬@;3Á¸ISAó«æ«k\x001eM$ÛM[XÀzÞÚ-*Eû«\x0006¸\x001a\x0002\x001eÛÑ\x0015\x000f3\x0000MFàKí\x001eûC\x0003\x001cF\x001bWlcÆíÉ\x00056ñfjDÕX|5bòµ!Ô¸W&¯_5bi\x0006f?êF§¨!b-÷{ÏÛæ\x0000-&÷Ôãn,¾\x001a1ù\x0008Ë\x0008t»\x0010¬PôÒÚý°\x001bU¨T¡·§¤	'f\x001c£\x000cöb»å~Ü¡Á\x001d\x0006%é \x0014wù\x0000·è\x001ba¨Ôv#×½×#ö\x001epÇY ä­¦1Uá\x0012\x0003í~àmè3\x0012û@tTh6HÃã\x001d\x0006\x000c\x001b\x001f³Ä\x0006µ\x001fy£
õ*¹\x00197¨Òkh°|ä3_§n\x001eQ*\x0010c5jZEÎ\x0008}Cã%\x001fù"±Û~äÍûÔ#ïÓ\x0000\x001f×ÇQ\x0000ä4¹Fª¥IÝÀ¡ñ°`ÄÃ2xµéyÆ ¦`-îÍ¡#_JäïGÞ(\x0016\x0018Q,6zµÄr¼mÔrî©FÊ%\x0002ÜýÈ\x001b\x001f\x000bF|,'Ë(8\x0012\x0007Q\x0011(Þm6CÎÎÔ,Ðh\x0016\x0018Ñ,\x0016\x001c\x0011ä\x0005G$ÈG¸SwùDÜb\x0011Å\x001d\x0002î¶xøHß"â\x0013_,îFn÷iFÞ§sGÁ\x0002®w4\x0019¹rÅ
MÍ­&\x00042#!\x000bá4\x0014%óÅ\x0016l÷Í\x0012!È~à.7#º\x001c·)+öÉ5¶#rÞïfÒHì<à¶¹å¶ÿ\x0007\x000c,%´ÕèPÜr±T%ß¼9rÛäHÅpLg\x0005Î3\x001b\x001c â3_¢ÇßÜ7VÈ÷[¡è\x001bOô­Ñ
Iª\x0019\x0019ç\x001dó°4²\x001fy£Ë}¿.Ç
pbéÉVY ¢6\x0011|Ï\x0017\x001b¨öksu¬¨&}®ü8b<¶ÖgOÑ\x0012Ëw4EE-.î\x0006Û\x000e^É; ø\x0007¬\x0004ýíóáíÉÅç7ooÞ|u{xÿf+r\ÎÆSüVó°µv¶\x0010óÈ%þ·×gÏO.^?{~~yòÕõÙå³uèª®Æ óÜ¾F4wÜEä¬Q-iô\x000eäºF®c<#Ç®A\x0007ÃÄmj©\x001d¢\x00039ÔÈa\x00089Qp\x001b±fä>Æ\x0013|)uÛÜÔÈÍ\x0010r:É3òp*óE÷«B^-á: Û\x001aº\x001dî\x0013Û"C\x0007n¡Ï=sW\x0003wcÀ-[#\x0004N<¤Þñ`´×¨¯¡û!èA²r1\x0012¡\x00119÷WGä\x000be¡\x000eä¡F\x001eÆ;æû±yWî¹
&Bª]dk¬Q@ÅH7Ýp\x0010KNËY
é:°7ÖH\x000e£ \x0003g\x0016ã¿ðÞ'ì:}ªVCj=z(L­d
EÒÈ\x0017\n»{e\x001aµ.ôzbsåënis´\x000eGöÐÉØE»x!¹\x0002ø\x0007«\x0005Ïm¡´ÜP.ýÒ6Ó\x001e]sW0(A ,©5­Sà\x0005{\x0008Î\x0007B´\x001e$\x0012!\x001eçæ}~óË÷1»#U¼·T[gøÞ
ì#Ï^?ûæêr\x001d²®!ënÈ*pë©U)ï-G\x0019ÑWWëm´[!C
\x0019ú!;Úë\x001etAÅZÃE®m?ÚØÔM?bS\x0002"HK\x00173d~j)\x0019º\x0013±­\x0011Û~ÄÀµO\x000bö\x0008GÄ²hÀ
¼F[!»\x001a²ë¬J\[\x0013qÄ4Ä¾Fì»\x0011Ç8úgÂ\x0007\x000b¼§!,v"ì\x001cjÈ¡\x001brô \x0014½½àib^;Q¼o·GmóUnÚÓu®wëfyÊ^`	Õ¬ãñ\x001a\x000f\x001b¦RÖ\x000b/[­i8Ò\x001aÏÞ\x001d>ÿtsòâæö×O@R¤^Ã<´Qàâ\x0005ç¶Z³ÔJ°]½þòüäÅùõóWO\x000e·on~{\x0010·«q»\x0011Ü"\x0004¦´ÁÙ\x0019%5Çæ½µ=C-îÕ#\x000f5ô0\x0006]â"\x000fcH"\x0000^­\x0010VW$í~\x0017\x0010:OöbÒ¿§K?¼\x0004Wú÷ôÊXßNìºÁ®°»ãf`\x000b\x00032²\õ©Ð¡\x000eCÐ½ÄÅÃù¶\x0007fIZ±Ð5ÚÒØ\x001b\x0005#4°¡°\x0007Þ\x000cR\x0016Ê
\x0013æ^÷FÉÈ1-£¹þæ|á\x0016î¨\x001c²\x0012\x001dÐ\x001b%#Ç´L4¤§ñÌ©\x0005b+3ê8;\x0011»5v%Ç®8e^êè¡
ÁÐõ\x001aýÏNèQ#JÆcM?#QrNd\x0005Ü\x0014@.×Ú¯}Ø,kIÖ:=«\x0016\x001eà¤)A©Z~©S»n4¤\x001eÑXäÇ÷É¬%²AGú\x0015m¦^wÑìåÌn\x0018ûr&¶\x001eÜ|ñ½~÷îð&9¾_\x001d>ÿøáóíÏÛHÜLË3ò\x001f¬Ò¶Ìd.\x0015p¿»8{¼ß¯Î^?½z}ýõ:tUCWcÐ\x001d['$\Dq$RrK
\x001dÐu
]A7´\x001a8\x000fhÑ$¬.£~it´\x0003:ÔÐa\x000cºf&\x0018L$j^¨N\x000eu 75r3üè¼k}ä ,Ã|K\<\x001dÈmÜ\x000e!æ\x0004zí\x000bO®âTXrÃ:»\x001a¹\x001bBøBAî\x0019~AÇTä¡F\x001eÆ\x001f)¨ &¨²
7,î¥Ú\x000f½Úü:]aÇÔ'Ï#ï«xù\x0011c\x0015\x001dÐ[s4fâ-¡5(Þ@a+\x0014À-bî+=c\x0006IËSMçn\x0014÷úËPZæÅR.·\x0003{cäERº\\x0019\x0014Ð¨Ì\x001c¯ÌTä=c\x0006):÷+JÏLX2ý&Kô{ «pÇ÷22\x0017\x001f>¿ý\x0018¡¿{wøýíÍíVì\x000eÃ»Ô²\x0018ÝÝè©¼Ê]\x0007j×zoûâêõó\x0011ýÅÅÙ÷ÏÏ¯×áë\x001a¾\x001ec¸É¢âÿfJ)E/nÆî¨Éð¡\x000f£§¯3FeN\x000ed<}CèWc¦ÝèMÞ\x000c¢w@\x0015\x0002¤®.¥y­¨Ö«ë\x001fwÃ·5|;zø¢¾\x0014Ïä§)h¼8³±»\x001a»\x001bÄã­2cx³\x000f¬xm³Æ8v2z_£÷cèãÑ+K­é
³©|qÖ²zá\x000b\x001bÚx\x0015»¦)¿ôôömDþéß\x000f·o7\x0017kÎLUiÄi00Þ\x001d\x0008\x0004_¬qÉ?½~\x001e¿Âî×³ëçK5\x001b{Gå#|5\x0008ßÇ·J*_2SÔ4ä\x0015á¯%&wÃ×5|=\x0006ßEÒLï¤°\x0002ÞÂ¥Y\x001a;ê\x000f5|\x0018<}LJ\x0006oðC¤Ó7Ô½£]Û¾µ\x001b¾©áÑËcò O¼<Ñàæ\x0012+^\x001eEðýZªl7|[Ã·ð\x0006m'Ì¨7©'V+XÛ°¾\x001b¾«á»ÑÓ\x0017§ùð±Ñ4÷MEK³\x000eZ¹5FøÝè}Þ£÷ÙÛÁÄ¢»ã¨£@+µ¶)s7üPÃ\x000f£ðm.\x0001"|G%Àxõ)Û\x0017áÉ/÷\x0018'«%FÍVÈ\R\x0011¿åér÷åÚÖñÝø[«;hv\x0013\x0015,)~e(¸U $kNégcvå Ýõ:7XGøQ\x0012\x001f/hÊh¹\x0018&vÁoÌ®\x001cµ»6ä\x001fx¿¸Â\x001a:~½Æ¾\x001bcwå áý×\x001fcwå áý/8þÆðÊAËû¯?þÆðÊAËû_püíÆë__5ÆK
\x001a/\x000bwIùG\x001f.§©Àyö|`­e7ü6ä\x001aÕýÿrøîT£ºó_\x000e¿ÑjXwjÜáàç¦xó%»=«M¡»Á7S*Î\x0018%\x001aÖM\x0001ï½ÐC|}ÁzÓ\x0002vnNè\x0001ó\x000c¢FÀ\x001eÝ$ìùûé1»½+\x001dÂY\x0007¶ñ\x0015\x0018jÁ#'\x001e`\x0008{»\x0010ÚÞÉZi[uYÜ|<9{S+\x001fO}øõÇÃ§O÷>nÃ#/U¸L\x001e\x0013ÜµàÔÒô
Õ+Î_]â\x000cËËgW/½zuvùêåºDªHMÈs:T\x001alàááE¦ÉufC©´W$¨Eÿ+D2µHfHGv)#\x0001¹½R{¾\x000f|ñä\x001a_¯H¶\x0016ÉN\x0013	,ÏX\x001b¤üw4\x001en©cÏÙ%ÌA\-&°Øß/¢ýD©F÷niºpP"_Käç}$W$zIÈ\x001eõ\x001bZ¢0K"ê°Ì\x0012¥åé\x001b\x0019íY¤\x0005§`L"ÙÚ¤iF	wuÒæ8\x0005
(óÀ¹¥äT§H
î43Æ?pq\x0008åyqxûñCçòæóï7ÛEÁahG\x0007ðTS×_]ä-LÃ<Q\x0017gÏ_^EA.Ï_¾A\x0006UË Æe\x0000Ë>\x0002%&@m\x000c÷ªÙE5Ð+®Ð\x0013\x0010LÚ	P´³\x0001ÖÎÖ¬.ñë\x0010\x0002j!`\\x0008
§@20ñ¨6£\x000cbm ´C\x0006SË`Æe@ËO2"âÞp\x000b~m°C\x0006[Ë`'È x\x001e2*¦SãI\x0008\x001e:µ°Ö1Ð#«pãBÈÀ+I Þ+¢\x00102òø%V·(v\x0008ák!ü\x0004!ì©§g
À\x0000ÇB,±\x0008÷
\x0011j!Â\x0004!FBYê¨BPZ"Æ«kö\x000bq,(%K'&H¡X9)Ét7FxËB¬5w\x0008Ñë	öZr$/ëÒÈ¿FR¬\x0016öz¤h\x000c¶`±cºd6ôh$g)Ì#HÑXl9ÁdÂË\x0012_1KO$Åêþà\x000e!\x001ak'ÇÍ	?\x000eÖi`C±¾«CÆÚÉqsg¥­¡\x0006oY\x0008\x0011æëXÙX;9nîLÄ
­½!"Ñ(\x0004Ï\x0002Z4MÓh¬\x001c7w&Àñ6yöÀó ©«l\x0017\x001dR4æNÛ;ã=¯ÞÓ1dõ$c6:³H-Þ)jì\x001a·w&^#¢ñÐN2s\x00118\x001e¿RÎíTcðÔ¸Á3^±ÁÓ\x000e¨×^e³mÂ#Ä\x0014ª1\x0015jÜT\x0018'\x0014ìav\x0012ãæ¿	ÕØ	5ÁNXÏLñ\x000eQ\x0017¯F&r\x0012Â®Ywì\x000c+íÂ\ò×²Ü\x0002îÊ\x0002SDgÆ\x0000×ñ°CÈßÅÎôÜÝ$ã$Ô\x000fï?ý\x0003'7×¨B4ÖÜ\x000cÄV®,'\x0006µ^dGè/®._}CÀë¡F\x000cýe\x001ezÇk~\x0004ÊÆCåZ¦i\x0007dSC6Ýy\x0019f\x000cêTh¬¹}ikÝNÄ¶Fl;\x0011{\x001c¡Òe \x0019\x001fk\x0005\x000fÉ`§Õ,¼®ÆëF.\x0005%\x0019AL\x0008x)\x0008ñ*\x0011Â\x000eÄ¾FìGN\x0018øKw¨å5;ñ×6>ï\x001cjÈaä¥CöD£Ì\x0017ù;÷A®3\x000f®d\x001ez0ãã¬,xÀ1²ç'Ö&¦v@V
dÕ}3d8µ4ä¥y«¨²¾\f¹F{´\x0003s£àä³yö8bvö¹¡+ckáß\x000eÌ½:.^
{Ô\x0019Ìâ\x0011ï)×y­;~\x0007æFÍÉ~=ç\x0003\x0012¸&ÌA\x0013~<gnËÓ\x0016¦©fÙ(:Ù«éâ9;ôîòÈhÚßJoGç`õb'æFÓÉ\x0001Ug3\x0017ÝxìBÈ]\x0019U\ËÉlÇ¬\x001aU§\x0006TÊq?\x000eÚ£/§ø\x0017;@vbn¼O5à~Â)
öé¨6,?ARu æY\x0014Õ¨gÕ«u8_
|@l¾\x00113OÃ­ùú;\x0010ë\x0006±îG,ðhóð§82w4°ó.sãä«\x0001/ßÒ\x001a\x0005|ÕcÇ\x0007ÈFp*g'æÆ\x0008ª~#\x0018ÏÙ\x0013fÍ,\x0016xÎÏy-£¾\x0003sc\x0004Õ£OìiÿPtô\x0015ße·Öd¿\x0003pc\x0001U¿\x00054ò¸¢øY\x0015ª¨µâË\x000eÌ\x0005T\x0003¾¾,Y*$#ÊçÌ i\x001cr\x0016æÆ\x0002ª~\x000bè=TÄ(X2SB¨@.í¤Ü\x0007Y7\x0006P÷\x001a@ìH¥ |h2Ú¶d\x0006ü\x001aö\x000eÌ\x0001Ôý\x0006Ðs¯Y<fW¬	8êtÅE;17\x0016P\x000f\x0004(>zÐw¡rzO¬-Ç<í\x0005êÆ\x0004ê~\x0013è\x0008paèQV\x00131R<ãip\x001bë§{­_<ay$<ÐDå¤¬+.sXZ®²\x0013scýt¿õsªP«8]n²¢n]üÔÓ07ÖO\x000fX?{jïùyÌ zùó\x001e_cÿt¿ýsÌò\x0015©¿ãef&\x000fKÔùÓ\x0003æOe\x0002	<fwjIa\x0014Ê °Æ`°\x0003rcýt¿õs.\x0017£_äÚ6\x001f2>ÃêØÿvÈÐX?\x0018°~ú°Ñ¢ðÏjÎÚyj\x0019\x001aK\x0002\x0003±+Î\\x0015ÿÙ¢\x0017yßvbnL	ô\x0012/±:aÆf
ÂÌê\x001aÌ<\x0007\x0014ÚÉ=¡ëlEÉ5;Ú£Kg\x001aäÆÀ@FQòÕÉß "C^lYß	¹±&0`M $l¢=!sÂ§¼Foµ\x0003rcM`ÀxbÆÿDñå4§ôÁÏ+õ@cN` H´ ù60[\x0015yi÷ìNÌ=\x0001{\x00024Ê\x0014ÿ\x0013¹4¬æü8® Ù4\x0006Å\x000cä\x0013¡\x0018\x0014\x0014Q
ý¹y>¨iìéLb mÉÓî¨f\x001bX 6ÕÍÂÜØ\x0013ÓoO,ÐZ_!c í=ùÍÐ0b^\x0012Æ4öÄôÛ\x0013¡2µ
úG\x001a\x001eâ9{¾\x001b æankðý\x0006E\x001b¢\x0016ÈNìsvÀxNÜ\x001a9Ï
5E1C\x0016YÓ\x0012(4(l\x0004a"äÆ¢ü\\x001a:OÇl\x000b_ÜQbÔZ¯Ø\x000eÌv6ýÚ\x0019xãXÈ\x0016Å\x0004\x001a\x0010À	 i)\x0002Ûhg; ]¦\x0002M!
'nËÅWê±n¶\x0003¾¾Ïemtèl\x0004å¢§m£çì@\x0015"pF\x001fyÁ\x0005Ç'3bÞe¶mçNYÛ\x0006\x001c6J}ba§læË<\x000f³ôm?]*\x0013sC]_iÍ\x0016ÿ\x0019Øá°P\x001cèy>¿¹\x001cÌ\x0008rï8+#q®.·¡Îq
vñd\x0006¹\x000b=jC÷«\x0005ãYIÍ½ø.\x0019ºØæîBwC\x001e\x000297p@©\x0011å×t\x0002÷Ã\x0018tË\x000e\x0014.Å+ý2¡Üµ	Ç
Ðów84¯×Á\x001e~{û)b¼9ùöóï÷;¶\x000f\x001a£yä_
s\x0002A2/Æ°å~××'ÏÎ¾{þ*þO|ûúû³ËÅE$\x0007ÔrÀ\x00149,Ï§ÕÔ¯Â£³²aâ~Al-!\x0008\x0012Ûæ\x0006d©\x0000»rc8P\x0003²^+ð÷Éáj9Ü\x000f\x0002¼èYâ¤ õ+ª ã@ùµ§û\x0005ñµ ~ Z³#ÑsÏÉX¶¡q(lï|\x000cAB-HôD²;\x001f¿\x0008P3">\x0011Å_dÍ°u	R±FDAÊÌæ$\x001e#¨,¡Ö9F%YKÏõI¢\x001bIô\x000cI¬ Q;)ysZ\x0014¤¨_»DÓ/i\x00041S\x0004QØ\x000e%	<H\x000b¸\x000e$Ys=ú$iô¢¸,ð&a©$±®aº©(àÕ9ù.I÷.§<øèyÓÒÕcF8\x0017oIU6\x001eITóàÕ\x0007oýñ\x0018ê£$Á\x0017£ø\x0018·K5\x000f^ÍyðáhÞyÿ\x0001&ÙXµý\x0001}4þâpaÅZ\x0015A\x00149\7ßÄ[ö\x0018:X5ªKMQ]èqñåòøäq±ëø\x0018~j\x0014¢¸¦lZÒk\x0007\x001eÛÖN>ÊÕjô£·<ïV.\x0017
§àkâË? ºQ[zÚÂ	[[<®ÜGSGquóDô'-5ä\x0003c94»À^±!kEç.A ù"0åH\x001aß\x0018ÇãÏñi°q\x0017kµè}(©Ú¸=þ\x0001ãö¿}>¼=¹8üz¸ý\x0014ÅØ\x000c\x001fÇ¶h\x0006ÝZÉ\x001b
\x0005¯\x0005ôzÁ
þíõÙó³\x0017g×¯"ôuÈº¬\x0007 \x0017g­>uyCDb\x001b1/õXì\x0005
5hè\x0005\x001dâ2c÷Ý\x0010hE³fàîû^Ì¦Ælú1ãb\x0007O\x001dy\x0016 ÀðåX,äí\x0005mkÐ¶\x001f´V9ï ¹Ï\x0017å\x0005õ~i\x0006j/f_cöýÁ2u¬Õ!ª(Ï\x0008\x0008ö\x000e5èÐ\x000fÚè¼ý\x0006A\x0013bïË)/Õv"®8"bô9z!Ç[\x001cènxEU4@|Îf©dº\x0017u£¡e·\x000e\x0002í3è ¨u\x000f¤fòDo*î\x0005ÝèhÙ­¤#hîiGÍm \x0015èÄ£^"éÞºQx²_ãI¥x3qômyÕ¬tüDï\x0006{Q»\x0006µëG­ãµ¦óQ\x0000È;¬eàõÛHB1\x000fu£ód¿Ò\x00004÷\x0012QÛÓ¬§ ê)ø &jFçÉ~¥'Mñöæ\x0006\x0006P
xëöâfÙ¨«ÙOôñD?j\x000b\x001c:\x0010ÔEtÜð\x0018QO4ªõLûõ\x0012:\x0006ã\x0002JG=9Ø'I7$¨¥å¨¡õóú\x001d½ícÔ?\x001cî(ìC·ÆÆE@vÆ\x0012u
R1²î³K\x001c[Kyg&òEzöûÍûÄ³sòîÿüçÿ8ÿ|ûá·í\x0011\x0001\x0012G
Jzg­Ù¨³\x000f´×\x000b¯òìûóËD³srqrþúúê»
ðU
_ÂWá¸\x0016æ\x0008ÒhÉÄÂz6z¨ÑÃ(z\x001c\x0000dªHI\x0017^ó6Xµ¤Ç{ÐÛ\x001a½pö\x00192}\x0019\x000f¿°ú©%\x001eø®ï\x0006á ¨µ$\x0015I'ËR¢]jÑîïkø~øî\x0008\i¾\x0004§³±Lù*\x0018¦:à\x001fcÞ\x0011ÃÇ/¨©_jE«âé;º<K$=à[¥9ª5ÿåwG6ZSªMäã¬\x000f´¾ãÊìÓ×
zý;ýFëËaµ/
\x001d¾Ö<j\x0018m.u\x0012ÆÓ_ª÷àoô¾\x001cVü8v_á§¢l(äÓñ7S\x000e«N¡Øì"~U\x0018\x0012Ã#áWêT£ªÓFïÞ#~Ò\x0001Ôcáo}¶a§M@»ªxñ/øù=ø\x001bý£Fõ\x000fØÀ\x0003<!³[i-¸¯ÌÒØ{\x0007xÝ.=jº4xlÈCðÞDß?ã`HùHµÔxÔ¿9|=zøÊ{
XWFøãñ[ºü\x0012%Sñ7Ê_*#
|å¢AÞ¿t,'¬µXZÜÞß4øÍ(þøx)á#Ü´òH\x001bÞå¢õÒ \x001eüñÒ£Æ+\x0002<¿`æheU9ÿ%\x0016À\x001eüMÔ¢GÃ\x0016U\x001a	ç\x000cæKÒýO©\x0017Ä/ì\x0012çM\x000fþÆøêQã\x001bÃBØqØ
èø\x000f¬>Ãäë\x0013\x001aøaøø
]ÿ|üÙ§\x001f?4¾\x0003ú\x000e\x0000Y÷c£<W+\x000b
&ë\x001ehÓ%£ºS[Ëº?8Á½(ÒñÛUzi\\x000fþæîÃèÝ×ÈÅß®wáLoÉVI39d7ÍÝ1£wGÙ=ãñÇ\x0010Öi£ëàÈ\x001b{ð7¦Ë.i%1£ø¯SÇ>}à9¨`:	zð7ªßª~©yiÀ­ \x0004¿\x000c\x0007±ÔSÐ\x0001ß6¯×¾^åà.¿çîèíÛ¿#ïAß&;Gý\x0006sä7{ÉAo4/\x001fï\x0012	a\x000fþæòØÑË\x0013½ýÓ<Hg´ Q¹@\x001d¢:\x0019©ð\x001bÕiGU§BþÒ74\x0008\x0015Xõ,n®ëï\x001aÕéU'fkéòãE"ü2pÔ\x0002Ktt=øÝì
\x0014\x0013@xã¹\x000f__Oö\x001c\£{Ü°î·D½eAZÊÉ\x0013þ¥Uu=ø\x001bíãFµDºõü|ã?ÓD
L\x001aé¥\x001eüÍóuÃÏ\x0017K\x0014¾à§íÁhõHø}ó~ýðû\x0015ç\x0013~ ü<2\x001fó~ýðû±9^\x001fKðÍñúÌÕþ¾y¾~øù
]Ã\x000f\x0004Ôóá7¯×\x000fû\x000e3ÇÛ£\x0008?÷FÍÆ\x001fCë¶V7zý¥×´'*6ÏÔPA\x0005
\x001c\x0005r	L\x0015 ­wÑû\x001f
-»þ\x000eÆfü:PÒV(?Õùm\x0000þ\x001cÄoélM¢äÐEòùÏu\x001fdÛ)?GC¯Â.íâ[&vMò=CXêxíAßÖÄ¨õP8ó°ìN[\x000b¼#ï!Æ\x0000KÓ<\x001d\x0002Ü©µ\x000f\x0017Û¥æü\x0018Ô\x0015¢l_¸(\x0002,Q»u\x0008 Û÷«KFL,Te8{o\x0000;M¤úáÍûA\x0001bìÎ5SÐDíöJ^VN\x001ee»\x0010þifõÂ»ûÕé_â§;_â§ñ/¡yÙ,\x000bAêéR£ò\x001e\x00110ø)*¶{aH¦»'ôß|¸}÷áç=
©·-:Çõ\x000bPÑ\x0004Pk§^,Dìß\]_\}½xþwHNâ\x001fää<ÂyÿöæäâpûÓÛíó^"j~¢\x0003SÊ1õhá|rk+vÎã?]>èÏ®¿|¾0çÅÐu
]A·\x0002\x0017¾&èÆ²\x0003í¶Ø5\x0002¥½ÐM
Ý\x000cAVÓ¸¶PÚÓò]\x0015Rân4~©`Ú\x0003ÞÖàí_êÊø\x001aº\x001f\x001e
_\x0018Öìdvú\x001a/ÍRÊ¤\x0003|í4ø²Ú­÷Öh\x000c\x0018	=X^aâ¡°ùµÙø½èe^=¸SGàá4X)Çs?\x0008~òÑ7ZR©I\x0019ÁS¦Yi\x001eÎdÖÄÅI\x001eôÐ AuS>>X®±à\x000cÞ®±xï\x0005ßh\x001b9¦n$î "])5ûÉA1oº1kÔ\x0016»ueë¦¡¾dö³?¹Ê\x0014îÎ8BüÃ\x0013\x001e0|öËáöÝÍÇ§7·Ï?½½¹ÝîY.°cOÒ©¢¾æ2GfMX\x001b¸yöÍÙõÅùËøß:{ýåóóëu!T- §p=/.&wßsºÖÚ¥&^!t-\x001e\x0017ÂÑî×(\x0005Ê9D!,	û\x0018_\x0002j!`\x0010Çë{ÊiHë\x0016¼(½"Z\x00043.\x0017´´FLîb\x0002'¬_ê8ì\x0015ÂÖBØ	B\x0000r\x001ee!ÜiîZ²¯_b6ì\x0015ÁÕ"¸	"8ªIÈv"Ëàyâ"Gx\x000f¡\x0016"\x000b\x0011$¶û£\x0010F\x0008þ\x000eøòã\x0013kjûe8:¦ÉD	BìcD\x0019\x001cÏ¬YÉ¥x'V§\x001b;híÜ\x0004C\x0017ã¼\x0008N\x001a	\´Ña%)\x0018zhì\x001c7tÌÕÙÐ\x0019¥¸%ÈÂ[d%ï¢1trÜÒ9ÉÙii -ÁHRp\x001a^"¢é¢±trÜÔ9ÉÝÒàÂl'¬áÌ¥Ea½R4ÆN[;üµ¤ ¬$\x001a]ÈªÁ¥á¤^)\x001ak'ÇÍÃ\x0005hºpÖðãÖü.<ùß¢Íùfÿ	ÿð\x0017t¡ô]Iô\x001cI4³ò\x0000n^!OÊóyôx\x001fá«»²D½;A\x0018¼b»âxÅ ¨Þ¥Xu¯0Z¸Ö=O[\x001eìÃÉË7¿\x001c~Ûw¾Ð\x0001ò£çá´a·6,µäp"ûìäeâ»¥4<A?z!\x0008ÓcØ]<Éñ]`BMÑ\x001a'Þ>äªA®\x0003ðì$Kò\qbåRÿý~ìÇ}Ê÷)wbÔ\x0003(µ\x0001fPµØ9G5´µ,üFèJÊ6³\x0011ÿðD6U³\x001f¼9ùöÃÇß~9yõáóíû=/W²7\EÝJÅp/Á\x000fÇW×¨\x0008±söôéùÉ·W/Ï¿ûæäÕÕëëËÅ\x0007ÌB©Z(5Q¨ÂJÌl\x0014\x001d)¯¹;ÙªUêÎ~¡t-(TtÌ
Éäé±(Ï³6Q¦5òá~ \x0016	&\x0014õ\x0015}¦ÀQò¼þÝj±á
udjÌÌ«ç¸¹SÇ§Å\x0015.í5\x000bµÊ¥Þ/­²3¿å¥:>-Ã\x001f\x0013évV½_(W\x000bå&
\x0005\x0005B)JeaieZê\x001e\x0018É×2ù2aÂn_æW{³¢m\x0015÷¡B-Tyû\x001c1	
ªh>w\x0014jiÒjL¨££ì®(\x0015¦OéM\x0019E3\x001c*\x0008ÞÊiý*/~¿T­71Ó\x0017¿Uô\x0014\x0017ø\x0003ëôEÔA©\x001awBÎô'¼#¾|¡màåòA\x001b¸ºvy@ªÆ3\x001d
g1Rc©¨_.BMw\x000eÑ(6îìYü\x0003º³\x0017\x001f>½ýøñæ×÷N0\x0004}us{\x001bÿËOO^|øün{Å1\x0006C\x000bÖ:Ä\x001fHíR).9.Æ¡\x0017W¯¿|yþâüòÕ	¢¯Î¯¯ãùòõÉ«×\x0017\x000bõÇ"ªÅRSÅr¹\x0018\x001cÅò\x001b8¢NÚ"úî\x000b:p\0]\x000b¦ÿ/\x0012ÌÔEG)­¢Áè[!þG/7q!¸\x001d\x0017ÌÕ¹©iLdÁ\x0004\x0015Å
Ô¿\x001e\x0005\x0013\x000bzc\0_\x000bæ§
FôÍQ0ll¤\x000fFìz
 [®(j#|$­#|\x001dUûÉÓ·o~Ùµ\x0003IZ8¨\x0018x\x0007\x0012õØ\x0001øµ¾ë¨ÍO>öÍ\x0012=ÃÖ5l=\x0000[º²Ê:&¢ÒÌ#\x000bk¨w65h3\x0000ZÇh/cöLmª±Ñ@«5og\x000fê:õ¦ÓwÖY1\x0004§­
®lm\x0008+Ï.Ô¶Am\x0007Pã\x001fÚþ\x0011ß'%:µgJX]Ñ°	·\x0002{'ã\x0006\x0016ßãwï\x000eoò\x001aÈÃÛ÷ðßj \x0002±\x0017|¯äP\x0007«\x0016îÈw\x0017gÏò\x001eÈ³ç_/2É\x0012jU£V#¨\x0005gôÚH\x0002ÁVÌÚëÆ\x001cvÃÖ5l=\x0002Ûå$YD-O3÷­.¤\x0016Á\x0005\x0015¾\x001b4Ô a\x0004tà\x0015i>^\x0016:jÍ}\x0010Ñ\x001a-\x0004íQK­Û{\x001dÿ@væÝ;NÀïØâv\x001eäÞ\\x0011U	mOvQq¯ãr\x0014qqÁ¹ð¯\x000c[DPµ\x0008jX`BMÄH<WÜ\x0015omÐ°\x0001ï@×\x0012èa	,/pÄ%¶Ä¿ª\x001c°K\x0006rÉ%ë\x0014\x0001j\x0011`Xè#ç­ È\x0017p*H\x0004[öBë%BN\x0011l-\x001d\x0016Ás£¥\x0010y1rLgs\x001d\x001eü®ÆïÆñs\x0011\x0017	K8uíe\x0011\x0016Ú;Eðµ\x0008~ü!8r\x0011¢\x0008\x0018½b\x0008)Ë-ZÉö\x0010j\x0011ÂøC\x0008kÂ­²Þg	\x0016õôIP
k I\x0010ã\x0017Éq¹\x0000unÒ\x0017êºñ+øåm\x000c­Y\x001b·kAÑ(\x0003³¹G£\x0000ü\x0018¶µtÐ59Å®±Uð\x0001Î\x0017« WÊë=24M[¶Ò"\x001aßYb*Î2h¾J°ìò÷Ð\x001869nÙBaÊ\x0012VRZÁ1Á/\x0006æóm³l&9G\x001c#à¦(wô2î\x000c2ÁÊ¬g\x001cRB»\x0003ÿ0ê²\x001aêaGV4æ¯qª\x0008¢Vv+ïäî¢\x000c&S0J¸I;\x000b¿úðy{Î\x001e­\x001ac¥\x0012ë\x000ce1\x001a^ê\x001aÃ(á<m*üêêõBéA«\x001a´ê\x0007m\x000c\x000f¬¢Á§kCZH»¥\x001eÊ½uX\x000f\x001d³¤cV@\x001d<fj¶ÐaiNu/hS6ý ÑN©¿\x000cÁÓ¿\x0008Ú2hk\x0017ü·½ m
Ú\x000eÜ
_@G·Ü\x001dÍn¿6K}Â{1»\x001a³ûÜP\x000evÐÁÜQwÁÔíj¯ooÞß|ú´cO¨±§\x0016\x001aÅ\x0008Åä1`óÆD­v___¿zuþäpûææ·'w\x0011«\x001a±\x001aC\x001c£'ÅKB\x0015wÃ\x0006\x0007e\x001bë¶¾Æ¸\x001c÷]Ðº\x0006­ÿÜ TÊþ (|PO1~?¹@À÷\x0011ú³ÛÃFÈAXìEÊ\x0010\x001c±gX©¨,oDXJ¿'¬g\x0011õ³ë³?8beî(g¬t=yòì_£·ÊMä\x001cÞáöíÍíæÓN¸Bâ\x0006Î9®6ÊlòA}sþ"z\x001d©ØDÈÙÅ³«K¬½?ysøéðñS\x0004ÃÿPD\x0002qgJ\x0019DÊÈgöª Àó^q¯4/\x0014<_
Á/¥¶³\x0010E¥<úGZ×Cumpø\x000coM®ïüïÿyòÝá·í\x000f!1\x0006gîf%âÅÉK[,0p#qõÏ.ÄÞÉÙÉwgßa³CÖ'wak×+Æ?`ãåÍí-^'/?ÿ´ý¾à\x0010¯¡8(0é\x0019\x0004ÃIÊ%ÂÚç××x3^¼|ýåÃ\x0007
4\x0006Îºû)à\x0010û'© ÚQOÅÝ¬i\x0013\x000e>Æ\x000bä«¦\yª§ÂÒPYªVåÓFi\x0017¨ªªú¡:¶\x001f$/DxnðÁX°.%ï¶AÕ5T=\x0000U¥£LPm¢\x0002ËejîEZ\y°
ª©¡\x0001¨ZroG\x0010¥ÅMK*j\x0015µà(VWcu\x0003X%í\x0011ÂË\x001aN5]VÏÝP
ößmÃêk¬~ä¶BvåtÒ°ùªrôªäR\x0015t\x0001¨JZ¶:Ôü\x0007<Ôç¿þvøø1A}öîCê­xõËÏø?EU\x0006|óÅÕ»·¿ß L\4Ék½4Ü
N©Ì\x0015\x0017[ó/®.þäùïÎ^¾L\x0008]\¥þWß\½~Àá<B¦Å(\x0004\x0019ûA;1;À	³³ÈU0{\\x0007ãÑÛY¬1Ç_Ýçr¬	st1]Î!ËãHþ(äÐ@\x000eý [¼\x0003©(!£\x0001NAN;æ\x0010\x001aÌ¡\x001f3:È±
0'
0\x001fiG\x0007!K2\x0016\x0004\x0019\x000e`\x0016º`æ«á5\x0014Ìf\x0016hÚíÃ T¤\x0013t\x0010§|Î©E\x001f1+|xÙÌº\x001bÒ6\x000evbêxÒA£[ -\x0012ùeÐz®¯¤\x0001íúAãÎ-zØw@ =òð'ÐÆL»Ò­æýª\x0003Aç85ªpj\x0019³cÍ1AÙySÕcò\x001fr=æÃçO\x0018`<yöKÄ\x0015øE°\x0006¶Ð\x0016i
5*Ýe\x001dLà»|\²Âh¯¯^¿ÂXúåÉ³oâ£×¾
\x0014L
\x0014_ô~ Æ®°Í0-©8¶\x000fôÃ²?{\x000e\x0017·§y8kè@ùÊÚcú»\x001f)n\x000e\x0014=êýH¥¢|s1Ø÷ùL}ð2#Õ\x0015Ë7TiA6¿÷cÅÂ\x0014þõRc\x0005\x001dpQ¢ÿXãÜ{T{ ÊÌ=\x001a&{\x0014	8ñ@)«Ãû:xúáí2dtz$-|v\x0000\x0012s)É²¥\x0001\<^\x0001úîâ\x0003å©Î.¿NJáéÕóUðJ«\x001a<þü\x000b÷¡\x0001£Éýà\x00071sñºá\x001dGð8o/\x000bæO1\x0000\x001eéN*ðýdàä%Ûi§Òºö=\x0005OÝß7x#Ð½k Ç#Ð"[â\x0005 §yÅ\x0004Ý{úd\x0000;ÞÅ
{Z	3\x001dAÆ\x001e]RIa\x0015Z®\x000c>L½ð¸\x0005¬\x0006]\x0003àÉF\x001c¥H;bé{
xAùÙ£JÇüìQ¡ãÀ\x0017æ\x0003ÞÞ|þÿÖ¼$\x0005Ô\x0013comÉM\x0002k8öv\x000f©ô3x~þúÿYEjLÔ?-RI#ùLqsän¨\x0001Ã_Ä	ÂcT8ñ:gA<h$wà\x0004hp"?f\x0007ÎÒ\x001bÝâ¥wjQA$¨ÞÜÎíP
5TüÙñõ­÷FÃaÉÚÐÓ
\x0018 R\x0003pO/ìGJk+\x0019)î­ì@ê¸»Ócç\x0005P$-éó\x001bsd
\x001c@ê[¤=×4"
¹\x0007>i\x000c\x000f3Ru<Óq¤^º\x001a)þìA\x001aÒÆö\x0004UyL¼åP¢£xÒ\x000fyó;êæâÏ.¤zc]£NaèëGWhüE\x0005Õ¨SüÙT±{æ#¶À/\KÀmZÃHCó¢ðg×Û7§^ç\x0008	\x0017+NNq$Ã°FÚVóÛ¾S×3§J\ZÎ®Wà\x000ck¼d\x000fÅÇÛB«OÓï\x001e x;ó¡Æ`\x0013£ì&R~\x0004ÄßËíÀJUñ£UñÊE¹9ùþí»wÛ\x0015
}?Ö¦\x0000ÅÁÕdLõaüÉ÷Ï/.Î®_Réâ\x0001GÏ$íÍn2pÁÕHÛ\x0010ZG\x0013ÓA¬â\x0008Ñýg\x0018qYBè=\x0007\x0011"q	#¼'½påCKÑ~hÑñ¥q9r¸{ÁJY>õ8Ì£{`VîÝV©íÜ»\x0018\x0018¬7£Z'[c|Cß»rí\x0012ÆÊµÛQy"8õ\x0010ß\x000f}q[\å üØT¦ùÜøs/Æø,òt8bT§9á\x0019YñÅCægó×ÆE«5Ê ÷£ÌéîRs^V:Y`>hÏ7ÃÔ²¹øs/L#dÑ\\x0018Ò º£ª\x000f°®'W`iî%þÜ\x000b3Ù\x001c
7â\x000bO ApöØ0\x000cÒ\x0008Õès¡ö´\x0018ä½Æ­9ùôxP;
Ã¤Ö*¦wÂD¾º¬4æº}\x0019?¹¶÷²k»aúÖ:úýæÑElTsÖÚPBG\x001bÇyx¯îçDöÂtBÔ0ñç^Ñ¹ ]^\x0005yês¹À\x0006
\x001f~åU\x0018@ªÝvÜ»¨ËóÚ\x0011kÌ)¸À\x001c3÷k»Ôz\x0015\x0000'°û ½µ@ñ\x0017*ñK$_Ý\x0002=rcï÷EìÄè[»µeÚÖ\x0001\x0014÷\x0006®\x001bKËuc³Å\x001fZXÅ¼\x0008±y·j._Å7mRÈ:h#õ¶M\x0018«\x0018\x00121Ö1äfñ=gE\x0019\x0003HÅ^2Br\x0004©×_Í"ÆÐ\Ç:zÜQ\x0017»\x0018[l\x0018±}3\x00078w;QV5ÕìøÂÞ6J\x0008îRÑzç4\x001cò¡ÓÇ¶ÃvQFsÐ\x0006b~¯/dVÆº¼DbÑ2ÆÞ¤#­ó\x0013`;0÷jI½4\x0017ë£{)ãT£Lst9Oüpéw+Nd\x0007«q&¶°½8\x0011¤|v x\x0007)UH[³î£¯À¬r\x001a9Ü±û_¹ÕV7Fã8,\x0018æ<·CHêÐø{ïY\x001a%±«<¥R\x0017\x0012·²-Õ~3üÍ¡5àMÞåÏrÑµ!\x000fþÞy1v\x0007\L86î#F£DI`ëÑÀL)Õ¸¿é÷~¹Ð,d)4Ã|¸mb\x001d§Ð9õrL³kó\x0004\x001fy©\x000e~<yúáó»Ãj%UÉQÇö9Ð,®¢O¼W\x0015|yòôêõÅùÙbZ0cu¡ÆêB\x001fÖ@\x0003Ñ
\x0016\x0014Ç\x0008;\x0017ýýÖÅ\x000e¨RË\x001a*þìÀj¢.©¿Ë:î>{é¤q¬R\x0016k×¹\x001acK/\x001a6\x000e«ûf¢Cbï)û\x001e°Î6`í\x0003kÚ+oIIE°áÞÞ=
Ð\x0003Ö·`}\x001fX)¹©Çvüù°¥A8Ì9ÙÐ^Ðw
$s×ÄEB¸\x0015¿=?¯û\x0003¶cUU?¢F\x001b º°
I\x001bx£ÚÿH\x0019%(ZëAí
-Tè\x001aÁbÇ2kXÎ~qÈéx¸Ïh\x000fVÛbíº¯UJ¬»©*ºâRM\x000båÏ«~RxCéY\x0017ÝS\@Ì«7\sSv¡#õÅëå>¿\x000cÒB\x0003ÒÂnY|ïI\x0012H(­B>è«l\x0004©«ÜR\x0004©ëÜÒFÑç£® g\x0004¥\x001b¢Ãêé«?èÇÚ\x000b2ø\x0006dð;AÆP»X­×\x00182#H\x001dô\x0019¤x8\x0006Ý\x0008\x0012dó¹ÓPßN\x0011Y&âw¤%\x000fW3f1Z|0q³\x0011¤\x0011ÍÃÁ{Ae&Ì\x0019øgÇ ÿàï\x0004i«üR\x0004iëüÒF8ÄFUj#©5Ó\x0008\x0008¥P­FAº\x0016¤ë\x0000)\x000c9MN#ij\x000eD&Ç9´Yè6ß\x0006²Õn· -IÕ\x0002k\x0019$÷üÉ\x0007Ëè[A\x0006Ó$þÜ	2\x0018ü¹£çû@1<ö\+\x0010¨=Ç@F-\x0017jé÷^ÊaW_êý\x0014Ù/¡¤N8¯\x001e,¬n\x0004\x0003¥5Hü½\x0013¤EVOÍµ\x0002)§ ­åþÔ¥±M\x0018MûµÓï\x0018µnf~8Ò±ÅA&Y:Èû\x001eñ^î\x000eF×ÃwÝ¹ý\x0004³toøkÿp¸÷½\x000f»?¸¦lHüàiã[þà4\x0019_|àÔ\x001e[e¢¡ÚØâüÓáýÏ«Í\x0013ñíP\x0002\x000c´É¥U\Ñà¹)a1²8uvùõ:L
5L
\x001d0E ¦#\x000f8\x001e¨GR!üA'×~¶Ái;pÊèi¸\x001c¯ë`r ¦<XÏåôûsNûa\x0006[Ã\x000c¶\x0003&VÑ¹ \x000eHöp¦-¹W\x001f'T62âL´»@)

)/ø<íý.®\x001d0E&ÐPÇVC\x0017\x001f¨æ\x0006qÀép{\x001bÿS+Ï\x001d\x0012!VÎ'8_¥´÷<®ï\x00179ÊØ Î8]__]^.Îc¹<Q\x001aj¸i\x0016¿\x0007¯·jÂÎDHx\x001d6øä\x0002\x001a\x0007\x000c¦URXãR
Þ¼cæý·7\x0011òÉù\x000fïnÖÒ\x000bÑ££Z¶ÆOÙ»Ò±²0¶É\>{~\x001eq?»ºxVï\x0008\x001eT
\x001eÿw÷Ü\x0003,\x0000zä\x0016\x0011+î\x0005Ç#è-Ôè-\x000c¢ÇÇHÊÍz¾âZËÒsß\x001b\x001cAï\x001aôn\x0018½".§^³WJ3ú©GTÒ\x0008\x001eô_èè1«¯}0ã÷z]q\x0015Yî}ÄG\x001bÊ£]P6;àG+^íÑB¦î«ªHt}óîæ÷ÃûOk\x0007ù
3G\x0016W½çîÜ@Cx°uüüäúüâüû³ËW«8MÓtàÄ'GhÞ\x0000§\x0005wÙeÿÝ;)¶¢TÕ Äüeè)\x0003×²,úEüLêÚT÷É8vÀ\x0014:mK¨\x000b.ö¾[d½yóù÷\x001aÏÍá·N8ãÉR½ÄiÈåâúùåùëïÞWÂ*«áUÞkôùS­x7\x0010¬¾Û\x000b°\x0005l¢r#¢\x00100:\x0005å¹Xì%_®\x000eoÄ
íÁÂú`hÀ»mJ\x001bÁ¦\x0015YI\x0003Ä§EcZ@`Ýsc{À*\x00035Xu¯÷Ï\x0004¶\x001aÏ\x0015Èûn3Ã6°¾pk XrÔDÇX\x001böW±º\{­\x001cz¬½¶Qü³_\x000e·¿"âÕ©yË[¹ÒÊíoPB+É±¿§d«`éÙ7g×/\x0010ôb\x0004{ø]
\x0018v\x0001Æ\x0016yê=GÀÙ!8°IA.\x0005ËÛ\x0001ëc×\x0008\x0002Æ]µ*½¾2\x0017dSO ò<Hl\x0017kpÛ\x0001cû}\x0005\x0018v\x0001>3°Ãb\x0012\x00026BN±¹òýÝ\x0018Úß¡?#ÞO7\x0015Ú Uiw\x0001	ÅÕB±\x0018Ä2Ô7g¯ÎÏ\x00169wîò¸ùû<nÛJ&:ö:\x0004\x000eDYûÉÜ\x001e¤¶Aj;Ïú\x0006°kÐJ>S7ýý£\x000e¤BHëA\x001aC2Oa½\x0007nÇ\x0010®D\x0008ÎÎ8Ó*®ñX\x0011éA)>#
öß¦É\x001e\x0001%¼_ñìA\x001a\x001a¤¡\x000b)`\x0013NF
Èkrm6\x0006<gÛÖ\rþ\x000f¸ä¶AÅ%L(\x0010Ã-K'\x0014bÔ0\x0006ÕÔtÖù\x000fOt9ÛÜc¹Y+ADlZ9N{y?e^'ÎJ+Æ\x001f·c\x0012Òãh\x0017"Ån\x000e¨8S¿¿ÂÖ¬Ü2\x0012­*·âûÃ]tíX«\x000c¹áÛ\x000eV{Ûò$k#÷áý®Ì.¬UBÏÜMèmÇ
ÇÆ{ÜB\x0008\x0019\x0010\x001cÜ/÷¡m®\x0001t^\x0003PâÏ÷ ÍÊf´Lßiî»-]`]s
Üô\x001aØ»\x000c´61Ðð\x0000qârÅu¤8\x0003¤!Pù\x0012\x0018É\x000e·7\x000bÉ\x0017\x0004Û\x0014×¡ÚÊ\x0019Pñçn°FÄèÊÏi\x001a,\x0017#¤\x0019i\x0015CÛþ¶aÍjëh_mT[wìëáöv9æ2"¨Ò\x0005£GÕ°ä[ýÁüqm\x0006Î®¯â-ÓYºÆ?w\x0012\x000c÷n(\x001cúÌMO\x001a\x000c3e©e\x0002Ñ\x0015&5oøJQE\x0007À7ìg¿x»Vã1B{Iµò\x0000yÍ\x0015¤ÁÄLMy\x000fV Ï¾¿z¾\Þ	wk\x000cÁÜ->ûðë¯×Q xZÚEûÉmÎ"0§DZfµ\x0010¨\½xñz\x0011«iÝ­Ú\x000fâ÷Ë+1v}÷îðþÍ/´Ñb¹×½Ìùâ ÿ±/_q-ú>ët\x0004KT]ß]]Æ_Ç5!éßïàt¶ÆIÝØ»q"Ml#¿¤H¡0`Ø?¬ñîYw\x000fê'ÁwÁ4ARØWZµãÖ¼ð\x0007üÁûPJ\x00015JüÙ\x0005Ó8bTÄÔ\x0005Owk]\x001dç\x001f¥Wv\x00015-PÓ\x0007\x0014;\x001c)Ñª²V\x0011¨)×Óè½4\x0001\x0005Ý\x00074\x0006§e\x0005ÖÈ'GÚÛÒ{r¿*°\x0017¨ovÞÐ\x0018ïó:aj\x0006Z;ÌýV½@M£¤éÓL\x0006Õ¤¢êx¦Ïóþ\x0004õN¶ÑKø³\x0007&¶²3\x0013ó\x000fÎ#\x0002Ü*\x0011\x0012_À\x0010Ð£ÏR\x0002m7Ð²Ñ*\x0002rC%·Ç·Ö­éE®\x0000ª£ÇÚZÁ\x0019MüûooÖ|¤\x0016\x0019\x001cD#¤-gÔ\x0011í\x001fb&þòëëóß[\x0000¨\x001bº\x0003 åe­Ø\x0015GiSåÕ±z
e\x000fÂÑ\x0010½Ð\x0010Ñ,a ï¬\ ^\x0018\x0015}Æ?\x001a\ÚÐ4\x0008M\x000fBÍ\x0005tSxZ"BÇº2\x001eè\x0008ÂãÃFÇw½\x0003¡(å\x0007ë/Þ\x00084ßÃA®\x0001è:\x0000JÍ4QFx^\x0016âX9û¼\x0008{ðU|u\x0011\x001f\x0012\x000eìÅ'¢±\x000eÐ1U¡Ô\x0017\x000fð\x000f'§¶#
BÙÐ\x0012{\x000crm7\x0003ä\x001e\x0010þ°À´\x0002PüðãáÓáðÛ\x000fy\x0013!î\x001fúùMÅ$|û9­­NM%2¬/.ßþÇÛÛ/ÞÝ|\x0011#à7¿|ñohMT\x0006ù\x0016Æ\x00012/lñsgÂG°30~qùü¿=?¿þââü\x0018á>ûæ*Æ·Qg?K1\x001aþýúùå\x0003\x0011E
\x001a3=ø¯¿\x0016jô\x0001Ý_
5Úò'éßþb°Í¼`\x0004¶¡}~\x0011v´Q`2ì \x0002Ã®öùMíäÖ¿\x0002ìÃ/Þ¹÷XûGå\x000b¤ûÙ/¨ËN^ÜÜ¦Vµà5®ìJûå0}\x0012pü\x0012¨\x0014\x00123"x\x001dÿïâU9rt?ûæ,*Å\x0017ç×\x000fv¯\x001f½=üt &92Oon?|þi\x0007dïâNõ\x0001O>"\x000e^æ2Z\x000c
Ä±à÷G__½þòa7ÿöï?þ\x0013=lÀ\x000eôoß\x001e>~<¼ÿ¸ãN8lÎ/\x0010Wî\x0015ÙS\x0000\x0003²Z·ú\x0007\x0018¿={ùòìòå\x0003k\x0006Å\x000fÿöþóá}êüöH³3Cì/\x000eo¾Ýq¢.z\x00069Í\x001b,nUp¸cNzÏ'ê[<Q´DÏþâìy´`\x0001c`¹¹³\x0017ÿð\x0004Vwø«Ã??D#ýi;ôl;Ñ­µhñ-vMS%ÍU
d>Ò~-_ß¯Îþ~\x0015­÷C=xE\x0002E¹\x0016@	\x0018@)HÓÄ(¼3V	+rì3^nñ®t@Å,\x0016¡\x0019ªé\x0012Aè4ºbS«\x000f^üô\x0015\x0018EX~\x001d"\x0010\x001b\x001b\x0000bT\x0004]Yø\x001aÀç¯ E\x0000³¨Ä;D \x0002A\x0016ÁQ\x0011))I«-¬Ê\x0012`\x0001<K\x0010Ô´ \ÍUÿp«äòÃ?on÷(ÍÔqÔSÎç%ÕXµq:kM£\x0001Ì¢\x0004/O.¯þ~þ M%o\x0005ð£\x0002dÒøß§¶¤?w{EüZMÆO$®?è1ü\x0002Éÿ\x0002	¶Òd¿Ñó\x0007Ø¦¶Ã7-|3\x0008ß»Ì\x001a÷'Íì§óyn\x0006ïÏ¶'¼\x0015¿:\x001a3Ä¯À\x000eâg!<~\x001a5\x001d¿âë£¶yb\x001bàç¥p|¾\x0001I\x0007Ú\x0001ÃÉõÛß(¸Q\x0002@¤4R\x0010õi1J\x00105§$¿'\x0008X4Çõ@ÄÙÉõóïÚ%è\x000fÈáB-\x000b\x0013ä\x0010¹`\x0013Å\x0008\L0"ç)¢\x0018R/¾>1Bó9ÂÏd.áÄ¡M\x0014#Z\x0002Ïb\x001cú\x0013Åp\x0018n\x0018ÈÑnèV¥'äÐyÌ\x0018oÕ²Ô%Í­ÂQAm\x0004Qv !;|x³ph.\x0016¿r\x0015Ì|1L+ \x0006>sPô@ÒìF~çÎ\x001a\x00059Öä'\x0008\x0012Ãµ\x001f«Áó\x001fÔ&\x0019í·ß½½ÙP\x0011»ÎvÃD^vC\x00056\x001caÅó+]0éâäÛ×\x0017ÏÏ\x001fÎB°\x0018ª\x0011CMC\x0006Zu\x001e?·¸\x001c8Éá¾r~Ñ\x0002öÉ¡\x001b9ô\x000c9¼Ê¬FQ\x000egÙUÆñûpâ\x0011¾	Íµ
\x0013ä°4Ê\x001bå°\x001ak­I\x000e\x001dX\x000e\x0013\x0016\x001dª>9,ÔrÔÄWÝr ç\x0007Ëa1ÝäPÍ¹v°S\x000e×Èá&ÈáhÃ(Þ+}ù^iÅr,Ûó>9¬åprÆ½ryÈ\x0004¿G"ÇÎ÷ã¤º8>M\x000e©m-\x0007þ\x001c\x0017$\x0006¬Í gA¤+\x001fDEw·O\x0010×<\x0010ü9,\x0008ÓÖ\x0006¤áM¥ÀÏW{Ùç	\x0012D#HCaÞ-GZ±$1È\x0005\x0001RYÞêù&DµªWMÑ½Âä\x0011(ò8-s	\x0005Ñ~1Ð'H«³Ô\x0014¥õ_"k\x00137Ãª\x000bËÙ©Ä³ H\x0010IÎ{t!çk_í\x001b­æ\x001b\x0005Á\x001d¸ùI+e D\x000e\x001cÿä\x001fáÖ]4süEìõÍ\x00083ñbÑV¬(ÖóíÑúÅã\x000e|ü"6\x001bDÓ\x000b$H0tµLE~;M\x0010kUã X5.\x0016ÀW\x000b`\x0002\£¥
´Z\x000cp{\x00046¶U¿BNÐ¿@L­*ÑÉ5i7I"ó\x0008TÙÕ|_KIÝXÄô{Ê71Ékf\x001cÐ:&I äº\x0000(c\x001eApG\x0019Æ]\x000b	\x0006ã*»Î#	\x0000ÒÚù(Ñ
¢Ä\x0014A\x001c\x0005V&:VT\x001dÆOB\x0005Wù\x0008_$ÈFo¥ß\x0013\x001cà\x0019Á\x0002i0·\x000b\x0006ò\x0002´0S\x0012eUHÊ'xâ\x001a6³\x0017\x001fÞº=¼ùå»\x0012(´	\x0007\x0007\x001f\x0014Îºå\x0000\x0002\x0012~ðÖ¼Ü«ËW×gÏ¾ùûª\x0014^ÕRx5,\x0004GÙE+\1\x0018X\x0014ÚmMËmBV5øÿ¡¼SDè\x0012C\x0012q\x0014CqR\x000e½/R¼Á/&\x001dz¤Ð¢"mÇ\x0018\x0002\x0002î\x000cÏæ\x0003\x0002§Þ]¤XnKè\x0012BF\x0008\x001dÆ0wÀ¦áçõ´\x0007\x0019àrIªK\x000chÅ\x0019b\x0000«Û\x0000ìF\x0014¼\x0012\x0014ckw»\x0018¦½RfÂÒ\Þ4øÚe1\^bbÄ *½ïÊmÇ÷]»íÏ>ß¾y{ØÑ¢`p
\x0005äÌhP©\x000b\x001dß6ÈLñ\x000f6
îo±\x0017Ï^_?{~¶Ð¡á+ékøªY\x001fº\x001f¾Ö¢À÷+:Á7\x001d\x0005×`ú¹ðjà7s±\x001dðó¹^X}ã>`ðJÁ¶hi#x­\x001aðøs\x0008¼	d\x0016¼~`,\x000c­4èírÎnôu\x001a:¢oòÐ}è­Íè¥8UÀð=Ãß`Û
ß\x0006¾\x0013cðÑgø¸e>_|#N_WÄý3àoàãÏ!øXlÍw\x0007û¼ÈßÑ(©\x001díë®{á\x001bÙ\\x001e#\x0007/·y0ÂWÓÌ1¬æÓ·fêå1Ð¾ÑÓÿWÃoO\x001fþZ§\x001fdsúøs\x0004¾\x0011Øyà[(Å/'ò\x0012\x0006°n¥±q?|ÛÂ·cð%ä\x0016´VfÅã"£å¬Ú\x0019Û>ú\x001fÍÝI¿àÛ<O\x0014¼³¥#Ð\x0005jø°87\x0013¾\x0014ÍÝI¿àã¾aõ\x001eyäºç:ëýrgø\x001eü2õFTþ|Òxk\x001fnýð\x001f;°[-O¹6§Ùdy\x0010ÜÛQ­qY~uýâê¿­!çu¢¼Ý&º\x001b»F:\x0001­X,ÅG,â*ßxm6a\x0007\x001djìÐðÊþÉ±Û:Ñ\x0018M|gÜ\x001dËÑÊ\Ðµ¸­ÀÛV\x001aÙ\x0006>æÒàÏ~ð1@\x0014H&
TÒa\x001f&\x000f¥ÒæÙ¨+·ª¥9ùô{\x0004½/µt]õÐ\x000b.æ\x0004·ÑNmCïMÞÿÎ^yhÐ§ßýè½6ÄM\x0013,\x0013ùôd6ÜÐ'ûÖ÷÷wÀ\x000f\x001d½Çª'ð`(í\x001941Fð[ÃÚ-àµrÍ­O¿\x0007Àã\x001cy¾õXuå·û\x0015rq\x0006xeRÇÅÑµ@÷àNRêÝÍÇ;=\x0004Ã½\x001ew£*òp!\x0007Í®8hMRêâüåËE/Ä¨:ZQ;\x001d­}b\x0000ÍpÆOâO¥#1H\x0008c¶ç9·
¡[!ô\x0004!\x000b+
á\x0005¹^°\x0014~ÑWë\x0012\x0002|#DËÞ×)\x0004Qi \x0010Wv9ù>­x]RöY\x0019Ïâ_~MHY»yó¾O=9oc!Ê§pÂÏÚÕH\x0010Jqg+G\x0014Áå½ò\x0018\x0000KdLRPôîVÚö	!u¶\x000bÇùJ-4í\x0008Ï~¹ùýð.\x0002Ýå\x001a\x0019\x001eç`Omö-À~\x001d»ÑH|sþýÙEüo¯
  \x0016@Á¨\x0000¶fG\x0001<Í^u\x0005°°ÑµÛ.k\x0004p£\x0002¸tý³\x0000*H\x0016IÜX\x0002·Ñ½Û,Á1D	Úp²ë\x0013Ø"ÑÅAT4\x0016\x001fs\x0004¡ \x000cK\x0010qò%\x0016
\x001dJà\x0003\x000fkXi6:z[%¨Ûé\x001d\x001c\x0015\x0001¹\x0014sýHã´Î"Ø2_é7¶Gm\x0017Á6\x000fAÚá E^ù\x0018Eîu$\x0002u\x0013E\x0011f¿eéZmêÕ©ywnHkióXCtÅ-`'K Dó\x0012\x0018~
ÂqO­Vzjã-â\x0001\x0013³BÚÑ!\x0002¨Ö"¨A\x0011«Fuã?\x0001I Y¡\x001a±Ü ±_\x0002-t-\x0001þ\x001c\x0000\x0013\x0016Y\x001f)Üë@\x0019ç\x001fs¯#,7Gì\x0017\x0001¬­EÀ"fÇBx\x0015>\x0014!\x001a\x0008R©Z.\x000c\x001d"\x0004ß\x0010ü¨\x0008Òe>È(\x0002ùd	$Oêª0û1;ÑH?Ç$pL¾à¬QÁ+J|)¹5\x0007°Uà\x001b»?\x0007E\x0010!³¯\x0007ô§±';@[cp RoìØ,Bhì\x001aþ\x001c\x0013AD\x000fÏæ\x0016@'¸»?¾qC-ñæ Ek\x0015ÒïÑÏà(\x0017\x0013?E\x001b?qü\x0019äÜÇ ïF:b8Ö\x0011Èç©JÓk\x0010T¶ß!L{
B'\x0016j2A'²Þáûùäé!Ñúßþ¼]\x0006\x0008Rs*\x001bKFâz¸2Mµ\x0006äõÉÓ³D÷ýõª\x000c642Ø0*CüT=Ã\x001d\x0000¹Ó	·\x0016qñl±Ó#A5è\x0012x;.Aà©h¡,P¦p\x0013\x0005ñT!tµ\x0010øsT\x0008¤m¥QbÖÕ'!âÐËg\x0010Ê7B(?,)¼,Nñ¼'x­¹\x0014«Ç${°Í£Æ£BhÅÜ8.Êû(`Ì!âÅð³GªÖB81.áÐ'JoY\x0008S&ìëûH°J\x001cßDôÅðg½ÛãýûÃ(Ä|ÖõR¦\x000cOÐiÐÑ~o\x000b\x001d^]^=2¬PY\x0008\x0014¡]ë\x0013\x0001òï`\x0019HÌb\x000e\x001a
çJ ­%À\x0012\x0008V®Fxîo7´\x001c(J\x0000\x001b\x001a¶Kpä¬K\x0012¨0*\x0004ª3\x0018dcô\x00114°\x0008zc/ïv\x0011B+B\x0018\x0015AÅðÍÓGÀåW¹T¢2bÚÈe\x001eý"\x0018×¼\x0004ãF_ðÌ8\x0016#~<iH\x0003?3µ[$\x0000HáhÝ\x0000àÏJ½\¤!ºÀô­63P\x0006zÇÅmèW(I	;\x0016ð*ì©×Ý2hcB8Yð\x0005í(\x0000öf[§ÎFøuÝ?ÂoËþûá{%Ni\x00180hlïÅÊyP<
!\x0002LE\x001f´ªÑãÏ\x0011ôÎKJ½\x0018çFkwD	õæÝ)ðM\x000bß\x000cÂw\T:\x0000\x0019X\x0013z[8xíäÃwÍÕ	nìê¸Ì®ÐkÍ]\x0017Þñ½ÛàÇ°¸9üô{\x0008¿\x0015l»¬×§Rgü@'Zýì[ñW+áoM×~üHÍµ>\x0016Éø5E5:¨©_J§\x001büø{\x0008?\x0000±\x0018ãdy¼´4\x0005´\x000f\x001bÃ·â÷®ÅïÝ\x0018~Eô&z\x000b¹Fr-o6v´o¯ª±v¯±ö\x000eøvÓEüsD\x0001)j2|½±×n\x0015~´\x0008¿\x001aåsH gê|éåáý¾¦jì8 Á+£i\x0008ÎKpÔ\x0014®a£ûyv¹ÜTÍøÝ\x001dün\x0010¿çI,ºñS)Ù¦9öøq½{\x001f\x000fáÇÝL¹MJG÷-ÓÌydg'üaêñkë[øË¹\x001f> æ|ü\x001aG:~\x001a$\x0003\x0005Ûz5·¢÷¦Eßxm\x001dè£êÉªÓk¯ZÕãn\x001aÂa"~\x0010íåÁßCø ª\x0016¯\x0003WýpªÌ1þ¹·\x0007ª6Á¿á-ëÀï(¯\x001báK*6yeiÆÂV
¹­ðA·ðAÁ·\x0008Ó^z\x0008\x0019içâÍÅïÚë\x000fnìú\x001b\x0015X÷)_¢ãC=u¸Ä~&~£[å¿ð#;\¾? ,¥rñ*IÂ\x001fì¶ÄÏVüÇQÄ¿EìÀ¹|\x0012~á\x00177É±út\x001bS&\x001bñ#qH?\x0011à\x000f:?<^¥µ\x0008W¬ñ\x001b³V[ñöüñ÷\x0018þpJÝâÑóÌ=\1n!Çßnî\x001eÚ\x0008ßöù:1ö|08\x0010þ ÊñCéN\x0006=\x0017¿mµ¿³cÚß*ÁÏ\x0017g³t¶^\x00117Y/·\x0003`+~w\x0007¿\x001bÄ/m^ý\x001fD7ä¡xnNlä\x0012Ü\x0008?Øööãï\x0011øé!íï\x0014ÏâFQ\x0002\x000f³n[¶¢\x000fwÐ1ô^ºLil Äí\x0016åàI\x000f\x0017¹ýwÂ×Ív\x0005ñ$ý\x001eï\x0013H&\x0014ñ\x0007ü9_ÈA¯SajÔ¢u«9Óï!ø
â9ë\x001cµ¨¼ê=á×[G7â·íÝO¿Gð\x0007í\x0014\x001bGäRÆP	¥(nA¶ÖIèE^ÍqD/L»\x001fèóÉÅçø\x000f·{vdyae\x001a°Hµ­)ã)\x0002'ÆË¿\ñ:VN/^Ç8{~½wÈ2øV\x0006?,TÉú¢\x0008yÙ*Ê ]`\x0019V\x0008ÂöÉàM;ÐÝ`ÅùüîæÓÛO'/\x000enßþü~ß=²
{9Ò=jÞ2ÔL\x001d7\x001b< ïÎ_=uòâìÕõó¯/\x0017¯S\x0012C\x001eGQ\x000cyl\x001eí\x0016$ G\x001b½¨Xe^×¤á\x0007¡¶PªìÃF\x000e\x001fÆåÚRD\x001cb|\x0016'AÀ9ú Æ? ¨ö*Aðç\x0004A\x0014®¾Ë¸ÜX¨"Èäm\x001e\x0008Øñ'\x0012»\x0014L6\x0015Öæü(n\x0002£¦Xùéé8Ù\-''\-vÊUQ5y\mDó\x001dþîÞvÇ®\x001bÇ\x001a¾\x0015ßÀ\x0014DRÈ¯ãq»áÀv\x0002ôü	*IMÇ/Üv?¶Ó@?Wÿ[¤ÎÖ©ÎÙÚ[:Óãg0q\x0015kK")\KËTÇx«\x0016 'Þª\x0001 1rÂ´\x0000T:3\x0005ÙtELÏµs7\x0010×\x0002q3Vä\x0004Ä¦ÒrÀ+"Tz¬ÛÖqÿß
¤ÝZ8ak1-N\x0014 &Ý³^gêò=¨gä}\x001f\x000e\x0013uôâ}áÄ\x001d}\x001c\x0008Y/-]9\x0017)¤n¿<ø\x0014/Ï\x001e\x0003\x0012Î\x0019@X±\R\x000eTD$\x0014íáòÞcE\x0013¿àXñÄàð\x001cÍ\x000b\x000e_F[\x0018h e$=D\x0016ýHVAC§7ü¡hýÂóâþïïÞ¿ßWf¥ !hë*}°:\x0018ÒKÆñâÉ÷Ï?ï°uÛÈö7w\x0003ö{pÚ6ËmE¥=-Z#\x000fü\x000emçLE¯ý°*4qûrSg:²\x0000Ñ«\x0014\x0012xÒJ\x0001R\x0010\x0000ä/\x000b\x0008\x001f\x0000\x0010Z\x0000£;(G<\x000c\x0002\x0000\x001b¥\x0000w\x001e×9\x0010Òm>@c>À ùi¡^Ì¯3\x0011­pçÛFç\x0013y7ÓÈõ\x0002 ¹þ*N@ë`Ô\x00051	*h[#Ü\x0011½2£5}µ¾~\x0000±\x0005\x0010¿¶\x0015°­\x000f²>ÈÁÒ¹¬\x0000¾õà)\x0008Ðl\x0000©=Äið\x00103ó)+ â-Ëc\x000f(q\x0002N*²^\x0000xê3Â¥a\x0006\x0001èkI0\x001e¥¿7RT}\x0013ôld½öS\x001bÅh41\x0005\x000c~ÝÉ\x000e²ZôËG sÞ½\x001bÀê¦À\x0000.ñ#\x0000¢\x0002g|½¼÷(\x001f\x001cRçT`7\x0000×ì þq\x000c@Þ7¡a¾\x001dH\x001ea=È\x0011@æ\x0003\x0000\x0016Mds*{\x0003GÍFýýÝ£§î>ü5C¹{÷×}åW4òð³¹)G9ôLYxì)].BO_ß¾|!Ý>{z©)B\x0003(L\x0003\x0014Ê\x001cÄ¤bçùOAÎ\x0006Ë/¹Ç\x0011áÖb­Y¼²»ûh>®§¨s^9ÉïÓ??\x0000ÉµÜ,HtvÙv\x0011E<'&«\x001df×o\x0000R
¤\x0010gAÊNY\x000eR\x0015I´ë?¥t%DÍIâ\x001f'! 2\x0015KédÅ9è\x001cF²R\x0006 ­\x0018\x0019\x0018÷ÓÜ\x001d
ÙgAÆ2BÌþNÆ\x0003¹|\x001a\x0014£´<	MäFèóYâ\x0016Æ\x0005VªlÚN\x001f\x0014[HÓ\x0012÷Q¬R`Ù²JÊ\x0019`.\x0007×\x0001D©]¤4Ïßyé/Ê\x0013f¸¬\x0016HÑ_~\x00039\x000eÉ´.\x0018ÒR$äï²ß.\x000eÏyªÞ\x0001¥ëÂæH|%ï\x0010c\x0013hùÇ)?ü¦Ðm@r2>\x0013\x0007áy°6\Öe>É¶VøÇI\x00104Î3e"6\x0006/LG*f#2EVþTw1,+Ïu\x0006ÑbçÝ§_³Ù;\x0000å¿7Æá:k'{\x0017D<"Ûhùííëïò_Ú\x0004D§®\x0001\x0006Dñ<Ê\x001e\x0003d
x)Ïsû@yæ\x0005Ê9x\x0006k.?4\x001c\x0006d¡\x0001Ä?Î\x0001DAãQþÂ#±4»à¹,
u\x0000\x000fÚeVe\x001a\x0017h]¦ùüèÅÇw?ç*üyÇvK\x0018å¢ÊrW¼P\x000cÆ\x0005\x0015yö²jÞóÞ<zñêÙ7¯^¾ÌãÍ\x0006\x0014Î	CY~\x001eÇ¯r7¦\x0008Vr\y| á·Ð©ø°\x0013	!¡)HÒÒ¨µÌ¹9\x0010º\x0005B+\x0017"kRÒîN,«Î³\x0005Ëºól\x0000ö9çm¸1 X¬b}ýsû°¬_è\x0018K£ä<°ÃPÙ\x000b\x001c\x0007\x001eÁ¢OtÄ\x0011ó±Xl±XÅÌ³IÉ\x0008TÛ\x0016
úùP|{\¬r\Ø#±Jò't\x0017,^*æ\x00147Ènañ§Áî\x0005_Ov\x001fÆârÐ/W\x0003Þq\x0014c1Úº¯U}sN;±öèû0ãè»\x001cïeØ±¤Å!cÒàBüR0\x0013KNjÎ¨Sö¼p»¬_\x0003þ|÷ùóÝ\x001d \xCE\x001d5([.¡>\x0006ä|¶¯þçÛ7on_nïN\6ß5Ü\x0003æó¤¨\x000b¹ñ¦XïEÅÉÁÂ55Ïz"aë}C\x0018sÀzfh\x0010v=îé*\\x0006D`×Ð©ÔÞi~:%Ál>ÿ8`>Ë1è\x0015Ò\x0003(Õ'YOzÑï\x001cZì3\x001fpE«ø1¸¡ÕÛo?X\x0010	3f4äÎTÏiî·Qß3F¯ý+¶ØÅþ.öýL*YH\x0001¿Ø;Þý±å³×þvû,?}Ï$
Å~#\x0017vo½}x~Òh¿]]ÓÙ~þyÄ~ô:µÈ,7³ý\x001eelU>fúN8sý0èû³ýVf\x000f8_â0°Ø\x000f^íg
Ý)öcZ´½O*rù\x0017ß4\x001arùÂúúÝßï¿|ÙsW\x0004ª©Å:lÞ+ùÌÍeÝ·ò]õõ³ï¼}{éº`Uæ1@3øz\x0008DàF\x001a!Ð³ÒRcAåóì¤;0¬4Ö\x0019CÄa\x000c*¥¬È\x0018|¬üy.õ\x001d=\x0018Úu\x0013ÖA»
8'Jº\x000eÊ\x0012°³+b\x000f\x0006ßbðÃ\x0018X\\x000cóm4:Y\x0008å}N½ýYý ø=~\x0005\x001c\x0005Ár¢¡2¢õÎ*¥$LßM¸ª
0f(í\x0018¼R2ÿÑ%\x0001\x0001V·S'!Â\x001e\x0010¶\x00051ì_}ª¼\ç\x0010ßäQ{µRï`é\x000e\x0010í¹ÆñsÍÕ&é[{>¼\x0007%¼ÉÏ\x0006AØ \x001c\x0007Á\±Q¸Û·\x0018\x0004ëÕ*wr'ÿó\x000e\x0010§g\x0005DC~\x000c\x0004Xm\x001bòÙQA¡Yu ²¯.úNZÃ= ¨\x0005A£ XûÕÈà§Àr&ô%e>g;'Í¹¶8|®ó¾©Z¤¤h%>\x0004£ÉG\x0015 Xçã°5 Ù÷)_?myzIBuè\x000cv¶Ñõ \x0000þå}zè39bó
?íe\x0004¯ßa:·ü°\x001cÀ¸"ÉÍÍQÂ\x0004\x0003Õ§ù-/\x001bþúmOL\x001b°Ì[\x001f¶ØªÌ\x0010S>çâl±Üõý\x0007Ì±ØáÚbþ\x0010ÿÛ¿ñJM([ÌáäÅ9ÜÊtCä¾ÐÂúºëÈ7¾ÜUµÃâÔìãtt\x001fÚÌ\x001dÑ*[0äëdýÆ\x0017óÍ~ÁØæäå\x001f\x000fÌÔ´PM.þÛñµ·<ÉâUµ-æbÕA9=ôèEÙ\x0016>¡nË:;L&×ÌGúÉ¬ï@§³'\x0014Ì:§ãÍtî\x000e\x00034&óSÈÁ­lu´%\x0012>·\x0003t_à¬\x001cÚ}\x0011\x000eïè¥|\x0013b¾b²/Ð[ýÈ&^ý&£i\2ÿxÐä\x0018±läYÎ¡sµ`\x0003¾2Ø|ÔÅaÎ2¤U<\x001aãÏ&3l¹\x0003¥Ë\x001d+;LÆ&T/ÙË1I§³ÉZ\x0005pD U1Å\x001d&·\x000e\x0003\x000f;\x000c´Kù®ìDrË­U°ty¤}É¾5Ù\x000f|e\x0010
\x0014årÌ_Yå;.×vX|"mY,fÒÿí[Ù¦Öä£>\x000ekq4\x001abÒå\x001b»ZXLû.wXìÛì\x000fd§ý¼y[äüB,Ö'=¦£dqj-N-N:\x001dBtÂ>ç¬ñº/s_ö[LmfOS{Ö§\x0011¼\x0010Pª!n¥Ã´Ñ\x000cµÃdßldþñ ÉL0*b?,\x0010ZÒ\x000bgTìGÁ&\x001cL<j²\x00122ÀmÜE!Úi;\x0010÷¡n;4Ëu¤²ÑÞæ_|Ã¦ûÏï~½ÿðËýÂét÷ïv)Dº9ù9/9Au\x001a_T¼yöÝ,N·?¾zöÇò\x0019\x0015\x0000®\x0001à8\x0000ËCi%O²ÒÅ\x0008RÍ.\x0017h@ 5\x0004±\x0006NS½Td\x0012hÁÀøËÅ¾#\x0010ì\x001a\x001d7 S9¢¤¬Ë\x0005o6\x0000·\x0006àÆ\x0001\x0018\x0015çZ$®JºM1è6ZÒâÉ\x0010ü\x001a\x001fPfb\x0016\x0008ÖTE¥x*ÌG\x0010Ö\x0008Â8¥0R\x0010\x0004yXÌ\x0008^ÓèòÍò\x0010¸\x0010Ç!Èl\Î\x000fèF (;j8óýiZ\x0003HÃ\x0000|Ð\x0014'ºÈM?\x0005BuF\x0016æo#÷ÓÏï>·ç1z¤A\x0004¢¹\x0016ää\x0014c-¬lH\x0013ï\x0000ÂïÜ±gN\x0006Aõ ÁçGßÞ½ûüù~OÛI"eÛuÞbÉÕ\x000cyaè\x00190xóèÛÛgoÞ<¹Ô6\x0003Cä(\x0003·-e\x0000Ïþö÷»lvAðû'nýÜ!²lÑWöÙbiaî~¯­3Ë½øþ6Û^`üð;?/\x0002I¥¦±êãFZ|ìo?$fsþ²&%6µé2wêiÖ££i\x0001\x0000Ð\x0000\x0000\x0018\x0004\x0010ÃMð\x0002 j\x001er7\x0002è\x001c&ê¶Zûit\x0001Äxz·å\x00145¾sp¨×øLÚb|´cÆ[+Ws)\x0004«sVtÞ­ß\x0008k;ìGWÞÞN/_\x0000Öæ¿øøþþóç]Ô»Îæ¤N\x0004gÈÁÜÈt>³Ôx'wÂWÏ¼ys~·@X5^e\x0008\x0011!äûz\x0012ÑìJ\x0007¥óªlH'³À\x000e\x0008¾à¿B\x0008+>\x000c!Á8\x0004Ëñ\x000bl³\x0008Nú \x001a¸KkÙd\x000c«¶\x001c\x0006\x001c>
<ñSØQsbá4E
 ¯LÖ]\x0001DjA¤a\x00109


Z-²\x0004QÈ\x0010:§´û!ØØ@°q\x0018\x0002WÂEÉÔw¨à4UµÔ\x001b\x0017úA¬\x001aÇÜ¢&2\x000edÌ7pZ¿\x0008Öë ^^\x000e\x0010`\x0017BS\x000cS|5\x0003Ë\x001f=þø·¿ýþaOÇ|æÆâT;\x00129ëTÌ¤ÎIØ7\x001e¿zñâ\x0017\x0013<Áà\x001b\x000cþ«Ä\x0010\x001b\x000cñkÄpRæc\x000cd¾F\x000c'©wXüú0\x0006ï´\x00051a
ÔÎ\x0008\x000f¸\x0007sY\x0017÷\x0000Õë²Â0\x0008Çs\x001aA\x0016\x0002õ	,8Ô^x¹é\x0000\x0008¢Ôl&J£ <T\x0002¿\x0004I½k¤ZQêÓ\Ø!¶\x0018â8¤éF¾){iÞsÌÑ.»i£Éû\x0008SÞ·h\x0012¿c òÕßÉn²Aha¸5)Ëm.\x0007@Ø\x0013(à\x001fGAxÐÎ¾äÐ¹¨
0\x001e.7D\x001dÁ\x0010\x001a÷jÃ°
X;\x001eR>áâRp4ÁF¡û\x0000\x0008·"æÉ \CÌs\x0008D\x0004\x0012¾®ò¢PßåÃ¬MS`/¿jî\x0002T®B+fË|\x0015rëÊØ\x0001bÅ\x0008\x0000RR
\x0010@ÚDqJmIîòý©.ÖÅ
¹d¯>­1ð LZBôBóíé&\x0016\x000c$b9·½|%ÝÁøá¤Äìaû\x0006Ã·ù\x001f¹ûåãï{
ÅÄ÷¹e%l¢¼±¤jOòàÌ<Á\x0017Ãõ
Å·¯^¾¼}üêK¥â\x0002c%eÏ0¢\x001bÁCéË¡°1\x001by<\x0011\x000c´1¾\x0013ClßNø\x0017ßÄ¶KýÛ_~ÛG¨ã)h+Sº,öT,õTsu »×þÛWoÿ´Á
T0J}\x000b\x0006;\x000e"Ð
Z)VÚ"9\x0002>F¥{Iw  \x0015ÃQ6\x001cá¢©Ð\x0005 ³2\x00153ÂÖâzõ¶úa3Íb,?\x000fâ\x0008Lfä
%H\x0000£ämÞÄ\x001aGÝs~Ý8NÌ
\x0005£q\x001cùN\x0001B\x0004TQóÅ(éSPç\x0000þ\x000e\x0018ñÔ²¸Àç\x0003\x0007`°p^QMq,C-ÌsÂ\x0002\x0012ûØYz1;v:aÈ÷¢U6þ;ó~ýz¿§XCµ8Z42 Çu(IÅµ]\x0017»\x001fïë»'],ì qmý"ü=`>eÚ%6ßù s\x001eÂ"]m\x001f7c·ùÁ4æ\x00073h¾×âqNÅµ\x0014ÑWó/w÷ï5?û¸µùüãùÖ
	N6¿6\x000f"I`Èæ_~Yßk~ôvm>ÿ8`¾Í¹^iñ!)1?ÊÖérXë·\x001eÑ´ÓXù\x0017ß4ªÇGTÿ2\x0002³HIµ\x0008ÐTV¸\x0010ñrMæÄcÞ¡¨S\x0010¸\x0006\x001bG\x0010UË,æ\x0015° \x0008þ6ð$Ô\\x0004pªÇ0\x0002þq\x000cBâ9ÄÀbD\x0014\x0014ÅÂÐ9KÙ\x000f`5"æúà\x0010\x0000\x001bäªrðUõ2$qA!@\x001f·`?\x0004j×Æ× »!+þ\x0006\x0005j\x0014n>ÿ^\x0004Ö7À?\x000e"Èw2\x0001Öd¡¶f%X^ËWÑNU^\x0008nõ ÎG¹É¯ÿ/Igo
\ÉÀóDâÓ_wD²ü©åá-D_ë`\x0004µFomW1o\x0005¯nÚ~ê`Ûíy\x0016ñ¿ÚöÔØlìöAÆ\x001bmd\x0011Û%¨
\x0000&Û\x001aÛÏsç}ßðçï\x000eµÁ¶§ÚËcK;mÚ'¿ØÎ?\x000e\x0019_§(¢KÒÃÆÆkw°í#Óï6ZãiÔxÙ4.Ô>Hºá»\x001eÉ»Mw­énÔt\x001dóvN ³íõ»_V\x0006î6>{³ ÿbá,XQ_ÞÿuWã£ÇääíÉ\x0013&îZÊYJ\x001daýñ+ÒË'O/ö<õ§ë
[ïü õQüdþ£ª§eë£2æ\x001eì~ëa%äoïÝùÜ Up9¯çzÜR3¢¾}M\x001fUXµþ»_ï>ùô\x0007Öç=i\x001aëùç¯èëó»nk\x0018üüV\x0012}Ç\x000feE7-~Ïáõr×ö³%»6ùùëøü&,TN§÷Öüop­[÷9{ÍÏß×tò¦/ÅÛì-Ëe\x001dyHì\x000f®\x0003éMöoÞüÐ¬_#à\x001f\x0007\x0011\x0004§\x001d×Ü"%êöà¬ÑÃÆLÔn\x0004ö¤ÞÈ\x0008,Åá5 Ê¸\x0013¬U¤­±´=öÖ´U±[ÓÎ¿}÷þý\x001eóË\x0004Niº¶ 46±\x0012äY\x001f|ïk÷·Ï?¿øLl\x0016SÖÃi\x0003®³e\x0005þï\x000eë="çì¿ÿb|\x001d'×ß¼òí«ÿÚ¶Üµ»!Ës¼\x0012Þo\x0000­\x0013-*âiº¦cûÑqè£çÛxyÏ¦Û\x001bµ\FÐÇæYî¨ùèüãqË¹PjkÎ\x001avØèQnV\x0014|oÃÖEË\x0011ÎÞ$ò/7	\x000eVw¸tÏYÍ{Ül'Yî£ÅÙ$o¤ BÃ)9\Ý¾æ&Ò\x0011wÁ°ïX0\x0000
ð¨äýüÆUpò	P\x0011¶`}êÝ>\x001d0aÐjRÙ(O\x001fï>Ýø°G*
O®T¹¿cI\x001cR°ZØYêå=\x001fo_?yùòÂóØïÏì÷cöç+¼\x0010¥	Ra-'y3³çôÕ7»í÷göû¯Ëþ\x0013@±?Ø¯Ê~w¶ÜØþI\x0010µDXà	M)PåhhnÿÔI[Ùm>\x000fcæÀ\x0012½ÅþXÔzÙ~ªöÏýüþD³¾Øï\x001bõÿÕö/1xõ¾Â¼å}e\x0015\x0005Þ~úøáßv^\x001cõeÑÛHzq¬ßÄË\À«\x0018ðöõ«ùÇ'1¬%¨ü7k\x0005ªßy¢ãîÓ¯;^I\x0001T¬<K?/EÒ9ËÔÇ>û\x0003OsÜ¾þnÓxÆx!ã-·ð©í¢\x0004ÄS[Õö¦¯\x0011ÙtL\x000f\x0007\x0016ÛI\x0016*wê/\x00136í5~õ°ÈÆ¯\x001e\x0016\x0018pC²$T
)¡\x001e¥\x000fÍ4\x001e¡1\x001eaÈx~P\x0011Y?\x0017,\x0013:-Æ{\x0015ËyPÏï4\x001e\x000c¶_Þàõ)\x0006á(öK\x0012½\x000c\x0008ä\x000f®#ö.\x0019ïµÞYoG¬wÆx-óQå*µéÁ\x0015C\x0019+~ý»ö½¸{÷éÝ.
WVWö/vUCå)n\x0008ü ­`/n½~vUYÇÆx\x001c3Þ$®ª)	_Tëm¥ì¹¼kö\x001aïÜÚxî¼\x001c1>_´HÙª\x000cÏ,Æ;§,fîòEk·õ¡±>\x000cZo"õÜ£ZÞL Ý8æòCânëS³qÒàÆAÐù@^ÅØ b\x0007´¡Ø°ÛzßXï\x0007­'©Meë¡î\x001c[ùÂh£g§õ\x0000ÍÎYækFÌÏ_\\x0008¹\x00178÷sã£²:Âå÷óýæÇÖü8h>J\x0003á²óÄøÆÄå¹óÝæÇÖßÇAïQÙrJÉí/ù)(¾ßè_ë6\x001fLXF"O#Â&|Ã?6\x0005ý\x001dõA~OT1f ¥Q\x000cÆÕz²ëkêß¬l¥åË¬
§ö-qá9>ð\x0003¦NYöLp\,ÛË=³»\x000c·Ð|qþñë0ÜÆúÙpçìWb¸_ñ\x001cqI\x0003G£\x000f\x000f@AÚ«\x000e|\x00103pN°
å×i\x0013S(®«NÞ~z÷læT\x001e<'b¥Ã(È-*ÿÖi£ëÔ\x001bYþÆ£·¯ýÿÊ&Ó¼/#i\x0006\x0012\x001e\x001a×¶\x0017º¡"ÖvøÍ·+ \x0013Ý3#á\x001fÇ¡DD9E&\x0002[ÚÆ1)#^ì\x0015ß	Å¹\x0006sS @eÆADlm<u°kì/ÛB±S ä£,½ü,¤Qz m¾éÊ¢`èS\x0015ßÄcsæùÇq$6\x0008cFÀÄó\x000b\x0014+üÆLçZ'\x0014 ®{p\x001a-ÏmþqE\x0003£Ç\x001fßüÛÏ;g£Ó\x0011\x0005Ï
þE =xU)àpÒUûä\x0014éñ«ç¯^|{yBª`+YeÁÅºP\x001a°òEG¾\x0016,:±øNZ^0Kik5Á#©Ïï\x001f=~ÿñóq*\x000f/[ÿ)¾Bë¡¿,óüÉ£ÇÏ_½é/ Ò\x001aDúº@ü\x000c&-MÛ\x001aM¾¥M6£¸{ôôÓGpfí¿îá ô\x00111_ï"ÙZ£ x¹ÿ6ï¡§¯_ñ|33m?ýãm¤Æ×|p1ÓÁ¯ÈøÚ\x0008´\x0018Ï}@_ñÎÆøåç\x0011óC8\x0005m\x0016@_¬\x000fèTªÆ].Ô=0ÿ\x000fû@]²A{¹³9Z7ô`ßÞâ¡»\x001dÏÁ,êédè7ÊU¾üË¹%&Èïs¢ß>yÍSw\x0017zÈÄüÐ\x001fÆÌ÷Ýy&.,OÙ<Ä \x0013Ë-X½ÆÛUë9\x001bßta\x001d°ÞU#ÇMÿ¥ZïF2ëo·5Ý\x0000¨\x0005@\x0000xd¼»\LI*¥¹j\x0005@J¼£\x0000 \x000c[@a\x000b=qZ\x001c=¿<'(\x0013\x0000Ùr\x001e\x0015/÷\x0007u?@e×¢Ï	)U9Kûv\x000e\x000eá¡Ên(À@Eqù\x0016t\x000cÅ;(£\x0008f\x000eÂ"\x001cOü|#0Ê]\x001e<c\x0015\x0012Êj,!a\x0018	Ï\x0007\x0008©\x0016Ó.Ê83(¹YºL§°\x0017H\x0019ÐÀS¦½t©óÍíû÷÷¥Vóø7nûòeWbg\x0002Võ\x000e\x0014Z^P\x0007åRºül|ûüùR±yü'n{ûöb·ÄâNº\x000bü\x000bÖ]¨éËÿ¼ÿ´Çzdb³\x0002KwDeËw(
\x001b|Z¾|õ'¯·M_UãcQ$\x001d±´®\x0001H7>íÂ\x0001ë._ ÷Z~ò«l9oÍ\x0011ËÍ§j¹0±-ü@òÕ7ZlvÚ¾Ò\x000bç
cl·UD\x0013['ß)U´\x0002^\x001efÛiûAm_\x0008\x0014\x0006l÷ÊYÆ¶×ÁSéPáÝ>gÏ@©¶¬¼&W[ÌùäéÒqðaOJ=\x0011m¦\x0004Ô!¯@Ypyªª\x0019Ç{[\x001a\x000f^^J+h¾ÆSÓDþÅ7ücõÿ?Þúåþ;\x0010X§Uî\x0018\x001dò\x0019æ\x0016¹(Cy>.
äÛÿÇ'¯\x001f?ùË%Ë±í´a¢	lÛûv\x001e1üâísê),ø	­0÷9²}#%¶\x0013ÙµíüãíE½äñ/&)A$gQ\x001fÿ:û\x0012»L_±&.ü\x001eÁ|-¦Ãº£2\x000e-eÅ~Û\x0013ÀÏ;"¾á°\x0002ËwÖÓIÌp±\x001e°>ßµ8>-ÅÝ ¤²ã=Ôt3uÊoY\x000fç¡
$TÒLÎ/y¬áË»\x000f{>?\x0014Å,¤j:IÚ=ÜÆî9å`ò\ÃÛg/7qø\x0006X¹\x0004ÕAlË|\x0005Gg¶ÜÂàY·ÁÒmöäóßï\x0018\x0010$Æð9ÿ;`@Nõ½
LqbÉ}}Â¹ÜðäÍ÷·E\x000fÿû·¯ßÿþ\x001fg\x0011\x000bÕ#®\x001a<«OiY|øòéîßv¥Å,\x0010äl®<\x000f&É¼\x001c0»)ã_¾}}ûøO\x0017FÁ@+-l$Y\x001cÀ`@ÒÐüO SC, ¬ö¼I] [^mâiÊ6ÿgøÇvbì\x001d+\x001cýò~\x000f-Vâf:áµ@f+-÷9Q
JÚG
±¼?c£ÇÏ/r{-PÒéU¡ðãPxx£\x000cÁ\x0005\x0002`UEbs8»q»ß\x000b\x0005ª\x0017­4{ó\x001fùÇFsêñÇ¿ý¼çRL\x0015!E\x0014EE vS_&\x0019\ËM=~õâÛËÃælð6Èàm#u`tØ\x0013·\x00062\x0010Da\x0004ù1H»Ù7\x001el\x001aÍ¬íùáR8½:qOu\x000eÜß¿Wok\x001fýù÷¼µ -åí~7µò¶îKéWK®æbªýýsu¶ù?ÿCÞXË¾\x0016àõ\x000fg(NíáüGNæaäH!\x0004Ñ&a¾c9Ú\x001a4.·Ë\x001eÃ\x0011\x001a\x001ca\x0006\x000eg+\x0003O\x001b#Ý©*ÊoÔ\x001fÂ\x0001§9QÆÁ?\x0003	IñBäRêFÊÂó¸}{X<ÙÁåegÍ×¼ÿi\x0007P
-®Õ;K¾í\ÎEÖÍRÿC\x0004PxØV*ØÌÃ\x001a!¤Ç¿Ý}ørÿ·ûOïw  \x001eV/-©62§¥-¾d\x0002(^&ú8EñÇº}ùöÉ'¯_\x0000Eëb=¿âÎnÕ\x0007f("ß\x0016\x0014o$\x000fQuÂg§OLleâLÿÙq{Ð\x0007¶o¹Ê?òãþ·w÷r#Ù\x0008:4ÄÍÌå]3¶Ãå"Þó¼knß\x0008+Ò]¾ý½ü_¶6Äð×þýÿüòSféºÕÏñøÓÏKZ\x0011K)D1ôÅÝïÞýrÿ\x001f¿ÞÿÇÓåWÖÈ[òà¡´\x001f gyÔBý\x0011ðp}Þ3ÜÙv
É/nxýìñÿøîÉ<ÍÖ}Çrwu¯ÿCòëoÿ(§h
Ï\x0001\x0012G
\x000fT<&\x001bî¥å\x0007\x001a¾¢\x0005fx>04jxòeodÃYqM¨;òñ\ìv+\x0001õifgoeÍN¥¨Îß[é¾81uú½oxö\x001enÐðhèfa{Éû ¼ÐLi\x0000bx\é¿O3<ÿ+ýðÑtå&Éçô@\x000c·Ü_\x000c_I¨M3<;½ðõ\x001cÍÿÏþ5}ø}åSî¸ÿúøáþÑ³\x000f¿þý»û÷KôìEáC¢2µs¼\x0012¥<g£:ÆHæò×oºäþëÕË'½üî7o_?{òüù\x001fÔÕ3¢÷¿ýÿñ/\x0010­F\x0010»WÂdcÈ\x0002,º¸@Z@ä\Àu¸<ÍþÇÿýõÓ»¿¯ÍóûCözÝ9½b.öûür¬Ïvæ $v~ñÍ»*»ûôI*;m\x000fÌ\x0007_::Ð§d~éè°y\x000f±ñ\x0008h/o5>?ú¾þã¦Ê5\x0010\\x0003Á)@\x0002¿±^z%*X\x0004\x0001ââey\x0010\x0008­Ð\x000c Nä%2\x0010æ+(%jK|E(@6bíA v
ÄNZ\x0011#@\x001cÊh\x001f¿)¸á\x000e\x0002qk n\x0006\x0010k
o\x0019\x0003Ñk.z/@ÖïÛ\x0013ø5\x0010?\x0003\x0008·¨P\x0001ÂOPA\x0000Á%Î\x0007\x0012Ö@Â\x000c (j]\x0019H\x0002yµO\x001cv\x0004\x0015 q
$NY\x0011¨[+zQ»²Æâ¸Ê	Ik\x0018i\x0002\x000cPJ\x000fù6³r@)\x000bx \x0002¦fÆzD,¯k9\x001cæû\x0013â£t0×8éÐõ\x0019q/
±8_æø.ÝD/FB&^Îf\x000f"iÂ!Ìù\x000cHFHvÐ\x0005\x0010 °b¤\x0008¤	0#\x001ers%q\x0019N%q^R-\x000c\x001b\x0017Hx\x00083\x0002"Ú îw!aÍeÄkW9îM<)\x00011ßù¬\x00001Â\x0018O;%Ý[îr\x0019é &\x001eÂÈËàKdç\x001e_`zÜ¹ÊÞj\x0002"Ì\x0018fæåÄ$K²TÛrWÁÑDD\x0012\x0012Ñþ¼"9¨ ¬AÒU"	6!\x0011gDÌ7Ä\x0014ä6
G¤§\x001dü5\x001c061\x0011gÄD¨wÝ6ææ|\x001c\x000b\x0010×Ø[Ø^u§ÜuÁèÍ
!1¦eIX¬¬ ¡kø_lb;Îí ,³\x0019GH2ÃHc{kø_lb;NíÙéê!A££I\x0004Z} ²k@\x00074±\x001d§ÄvÂ\x0017\x001d1ðPå|KÊ h!]®\x001fDÒ\x0004w\x0011Ü1ßÕQN	kÉ%¥wË¬[ê'"i¢;Nî&Èc@ ÄÓhbqã1à &ºãèN¡È]ò\x0007­@°:AYh®rLðSÂ;¿ÏÈ1¡eü¡´Në¬uæ\x0001¡&¼Óð\x0006IPLÂ°\x00165\x0002Ä\¥\x0004AMt§)Ñ½\x000c$\x0015I7º Vý\x0016wW_\x0001H\x0013ÝiFtÏa¯ô(g \x0006@2/uº$á\x001aÚJöðïëº$Ü®åeMP7
WÙ\M|§)ñ]{kxMH$\x0014\x0012êÞb]³+àh¢û¹Tò±\x0015ÉW*+8<QBªH<]eo5Ñ¦DwðÌ\x000c[ò\x0014Ëê\x000b\x0012Ö\x0010x
\x001cMl§\x0019±\x001d"\x0015Y#p6¼ÀXè\x0004\x0016\x0018Á^Åm5¡¦öì«bIæ)¦$´Û\x001aI»Ê4±fÄv\x0008T2tºº\x0003é!IW)¦Ø&¸Û\x0019Á\x001dB,Ã:ÄKK|F*«\x0014Om\x0013Ýíèî*\x0012Ë3¦eMò]D\x0012.Öä¹\x0006&¼Û\x0019á\x001dãþ\x0005±\x001cUÊ8Ebà\x001a.Ø6áÝN	ï´\x000cavY u`×Yö¥zFx\x0018Y¡§ì®TÃ;YP$ö*H\x0000o§\x0004ø|8$Q±\v,»\x000b4¼¡\x000bW©
Ù&ÀÛ\x0019\x0001\x001e¼Ã¼&AÄí\x00136×u4\x0011ÞÎð&\x0004­h[´3Å$ÍÝuê\x0010¶	ñvF\x0007²Õ	¤±öA¸p\x000eÛDx;#Â\x001bg´YeÝ¤5Åx- ëÜz]\x0013áÝ\x0008Ó`yøav!'%TkeI\x0012]£Zç°è¦ENâË°òQ Zw)^\x0005IsJÜSb¼ÈWd$)òÛõ²¹"H÷!]£6äÍågl®üu
³A>&' gdéE¾\x0002fkù\x0019[¶b9#!{0¡90>
hð\x001a\x001du¾ÉSü<Å¸pSø2	'K"$ÀU^°Èÿôó»Ïg7xþÍK<Õ\x0002\x0011KHè%¾\x0016è*¹°Ás@8\x0007Ï¿§}èÁúÐ\x001c<\Àsÿ¢~g¯Z¿³p'gßsðø\x0005ÅÀä \x0013åîµ¨H»W¸ÊÍ~ú²p\x0010¯ï_ü)OÚId\x00037 \x0017|\x0013ê\x0005ÿ*\x000e!<ØpaÖ\x0002ý;ðØ\x0007\x0007ÈÎ:@ÿ\x0016<h\x001fø7;ÉÁYÔ,³ämÂ¢«oª=\x0002ÙÚ¹Ï6tÒÿùñÓG¾ûðq×°GË=ì¨¹tQ\x0006~cvg2³á-\N	Ns2ÿùêõÛG¾}ùêç}*\x000c\ÃÀq\x0018.§3T¦}(TMjqëQÙy h
&\x0008©Èvåµ¨
FÑ¼I\x0007º|HÁ°k\x0018v\x0002\x000cãÄ\x0002.A\x0016CzëÁùpùþr\x000c[£p\x0013Päë°î(çå\x001f¢ Øz8Â¯Qøq\x00146\x0019ÝRü:\x000fEi\x001eÓÅ`Îàù0Â\x001aF\x0000Ã\x000bï\x0008ÏR*Ý._$n¤+Ç`¤54\x0001a (v,\x0015<\x0001/Ä`¬¦\x00038f	8¸U¢Ì%¢Óz77@*h¯ào¡}\x0013\x001f\x0013\x0016 8pîò)*¡èc8à\x0007\x0013¢Å(/)\x001eõl'Àn4I\x001cÃÐÄ>\x0010ü,ßã¿EÒ¸\x001d\x0011ëZl5n\x001fÃÑ\x0004?\x0010ý,³\x0005³\x0001<ÈäË\x0010l\x00037ZéáhÂ\x001fL¼§¢¸\nµ;ßUn£Ùù\x0018&þÁ\x0000øïY&\x0000Â\x0008/\x0019\x0001\x0005\x0007	S&3(~Ác0b\x0003#Ã æ\x0017*\x001e\x001fMä\x0005ï&ÙV\x0014é\x001aËÑ\x0004r\x0011ÉÁh$çå(]\x0011b¨ëÑË.°\x0003\x00066\x001c'\x0004rr #ÖÌ/Ãq\x0011@Þ\x0016y9®\x0000£½üM\x0014LaCË0ÿ¹  ¥\x001dp\x001bSÉÇP4\x0003'D\x000er\x000b½ÉÂ\x000c\x0001äÅðº\x0018v£ë\x0018&ràÈAn\x0014\x0015"Ð\x0008hu9¶úOÁh"\x0007N\x001c<L¥mò£t\x0008Æúz\x0005´Á¬t\x000cF\x00138pBà 
zu2ya
ec!æ@°ñzu\x000cG\x00139pFä¨\x0004FÆ\x0006isÆ\x000b\x001b\x0004¹ÊMÖ5\x0005Ä¥´À¿\x0018®.\x0000\x0016\x0001R#R\ÀZ°ò~ê\x0019\x0001<+\x001eæ\x001d\x0001knÕ´j\x0005~ÿîþÓ®r(\x0018\x001fê{ñ¥\x0000óç
ò@bh£`Í_ÿìÍI5ðûgO^_.ôâYA1ÿp*4î\x001eò\x0002Mf³2\x001e¯^C\x001b]+£Ðh
fB\x0003¢÷¡\x0011\x0016G4\x0016¼:\x001aG}ñÿ(4»f§B£ EÈ;Wh¤M¸Ù\x0017öZBskhn.´T,¶\x000cÍ¨Ð6^ñG¡ù54?\x0015K\x0002%'W\x0019Wf\x0000\x0013:okG¡5´0\x0017Zv#\x0005YÎ&|\x0014\x0002è(\x000f®fi\x0014X\\x0003S\x0005W¨­\x0019,Ò!fX×Ýi
+MeA\x001c\x0008³ì>k>eëÈb/÷Ú!hkN\x0017lª¶ãØ\x0010-_½\x000b×\x0019·ììòQ\x0019ºêf6\x000f@ªibÊÛ\x0015
\x001a\x0007Acò}%Ý£ØD\x0004¦f"¤d¯)Ù"¬ÆË&e÷¼n\x001b£ØL\x0004¦¦"Ì:R9Ò,ì\x0016lè\x0014ßh\x001aÅÖ¤"05\x0017A§\x0001Ç749fÝJ-x]lM.\x0002S\x0011Þ2GïàåZ¶ìIÅÖOQy\x000c[ÀÔl\x0019X¤gÅ ôFäì
j\x0017\x001bm°2bk²\x0011 óòôÅ½9¥×÷¤öK/\x000e×ÄÖDn\x001aºÑ\x001a©\x0007¾¼\x0019ñA(\x0011¢í+\x0015\x001cÄM|Ã©ñ
CmÜËÞ^å+<(+\x0005øëÆ\x0000l/Úsã[H:8i¸-IÎ\x001bÖ=I×½ØÀY·Ø\x0012\x0007ÖÕ	\x0010c\x0012Ã|w7¡\x0002®\x0001ý\x000f]Ká\x0001ÄÉ\x0008cÚÃµÊVÍ\x0014¥o\x0006\x0013íº\x0017sq2ÀeTï;®päAÒù¥B|Ý]ÚôÐ.»óÿÎA<«º.\x0005ÉaÊå¡e\x0011QÇÿs\x0006s]Wc\x001eC3ÛÕ\x0010HFí\x0013jZ¦· »ÁÊ2¾g{ÔMÞ¢ÿ67\x0013ÏKé\x0011Û>Ü÷w\x0002çÑ·ïï>üòÛ\x001eÖú@9\x0017Úu(\x001dIÎ)5\x001b0ðÎç·\x0002æÑ·Ïo_æßoÂ5¨s6þã 0{L,å\x0006\x001eÅ-CÎ:á2`;Þ!P´\x0006EóVÊxIÄòJyv6Ê,\x00150Gëõ@Ù5(;o¥r@ê³\x000bÛ\x0002*¨´A'=\x0004Ê­A¹Û¯¼\x0003X@é\x001cuÖZyT÷Ñôö1\x001d@ä×ü<D L¬»Y¢\x0017KjSS\x0008\x001bôåC Â\x001aT\x0007*û;Y¨äUÃÛæ´C0õ7\x001dÀ\x0014×â<L´ý_|E\x0017T~òBu÷	\x001d\x0000Ö ÒÔÝW&­½3\x0012{y÷©°Mè¼Þ\x000fjU\x0016xÖÌ<\x0015:¥OÂ\x0015\x0018GdêRu7
\x001e@Õ¦\x0013óò	æóPOa´Á+£J\x001az}º^>\x0001M>\x0001ó\x0012
à\x0019Ì\x0002\x0018JèÅºT©óEþ\x0010¨&y	\x0005pWú
eVË¨¼.Uè¬Z\x001dBÕ$\x00140/£\x0000\x001e\x0015(i+,\x0005`/M05ù\x0004ÌK(\x0005}ñ´1@cå\x001aª®çÕ¡É)`^R\x0001àô¾È³O­Áå;]«îöÃ\x0003¨¤\x0002æe\x0015&\x0011\x0017·KZáTÐt­\x0006ÒôªRõG¨´\x0002æå\x0015`¶%ÿ¯½C¥Ã§y©º{úö/\x00156\x0011\x0018çE`\x000c\x000bØ\x0014P*Ûê*Û\Fu½¤\x0016\x0000ó\x00020\x000b5Ëþ[@©¯@õêqÍe\x0008U{¡\x0017Y4ÉI¬B\x0015¦sÌÍª¨®V`\x0013q^\x0004Î^H
\x0016T\x0012!ÃÒ¼â×*l"0ÎÀ¼°nål	4\x0002C½\x0001-f¤!TM\x000cÆi1GBvz©)¥Êÿ9
Výs­\x0007@5!\x0018ç`ÞQ\x0015\x0011X.KFUÚ\x0010ý\x0018BÕ`\x0016\x0016#õë$-9,ò^\x0013[I¿\x001aª&\x0004ã¼\x0010£»6:\x001f5ZÑÑÝ#ÉûQQ\x0013iZ\x000cö\x001f·d\x0007F'\x0014\x0004Î\x0004\x0010\x0017\x0018í\x0015¯VÔ\x0004a\x0016}K§\x001d\x0018e^Ù\x0019#m¥ù_´A\x00175ª-@O\x000bW>\x0019ÕlZµ%\Ù\x0014D4$ÿ6xGP¹\x0006\x00189aÒÔÂ³üíé×àæY.>è\x0000\x0018ÍÛÉ^Ø·\x0017Öåj¢à®XdBw\x000e\x000eÏY\x0006}\x0007K	-\x00119 PJ¹|Æ4x1[ÖõjçØÒÌuCã8Ï3»Iñä\x0001jÅóén|°lqê²1\x0013¾ÜPÕ@f¢HBÞ×«Ñ\x0011Ð-Ï3×Í#\x0003ÒÛv¨>*t\x0013<\x001c)ê>p&0Õä´C\x0013{0¥\x001d8ïJ¨Ïª¡ºéÈùÁÂM\x0005÷ï
\x0003ô`åhn\x0018M0{J*M`°¨µ\x00086J×[8\x0008\x000f°©\x000b³ýê\x0012â@ç4ßPí\x001e{<\x00077\x0015\x001bK\x0004¡\x0016\x0013Ó
É¿	õÖ®\x001dÃyË	4÷ÏÿùñÃÞ\x0019C!&vèF¨ë¼Ñ!«´Q¼9Q×ýåÕËm»qm7Ø³\ÈææÉ$*¥ \x00141h~a¢á´6F\x000cgR\x0002ùàè¤­"Qð:%åç\x001an×ÛAÃu>ÔÝ_PÅaÓ-¶Öeµ[[í\x0006¬F&kÕaäTUy«Í}ÝÚ>]ûµá~ÈðxcÄpP«uà¬1·Ëæ°¶9Ø\x001c¢2ºÄX%QµÏl/WyÕqmu\x001c±Ú{R	,OU\x0015J©Iå-Ò­
Þc8´¾{ÄyO7®<¨Æì\x000fH\x0015tâ\x0012R·*eáó\x0011ïÍjn\x0012u¢sê½1$ufã\x0012µÓòÆ	Âq/ÈõK¯\x001cRÞÅÒ\x000e?¸ózCÚh_ÜixãN`Äð\x0016D²\,/²Bñ\x000cùÞ7Ó£@ãQ`Ä¥°n¸Àê\x001a%îð\x0010§Xn¡W'¤ËòÆ«À[YÞeË'g¯¢\x0002'Ú·Ôæ&\x001a\x001aÃÓÈ'wgO]£*\x00036ËTÃ×OÈÐsï6ÜÖFþ sõÙpôê\x000eiêáÄÆã#ÏÑ^\x001f{\x0002g³òÉL¼²VÑLOm\x001a>âÉsÌ\x0017ÅA\x001f\x001cª'7¦n~	².Ë<\x001cG\x0012ñ\x001c¦&\x0010*\x001b`Õ³pØhy\x0013p$\x0013Ïÿ2\x0016L*Ã\x0018îµå÷ÍLÃ\\x001c'ã9xr3oñ\x0001*¯gÒÛ&lÕqv\x001aÞ\x0004O<\x001e<Ùp¸!1\x001cá&\x0014þ¯ä¬Fý´ñÄ¼Óò&~âñø-\x000fAtw|N»ÄÇDr\x0018º\x0005(»,oâ'\x001elyÒWýªG±<:Ý,sãP\x0013@ñx\x0000Íû¼·åÕ£å¢UË7º×÷\x0019NM\x0000¥ã\x0001
Ï7dq,få/+ë`zÉ§&~ÒñøÉ\x000c\x0018^ßdrèìM´\x0005$º
¾7ñÇÏb¹ôÄú\x0018\x0006<VRöèçZÞÖ±ÇO¾	\x0019½ÃåÿQÊhõ/Ú©÷}jâ'
ÝáÕW.>(ÛÜÔm3ö7\x0001\x0002¨êYrä/	1ê\x0013\x001638Î4¼	 4\x0014@t³p\x0018*¾_?®âXðI#á3æ3iäºÏ¢%ðGÐë~HÝZ5]7áÂ'7Êg\x001f¹%
:®7áÂ§Yæ8\x0016Ë³w\x000câ\x0012­Ñ¾#Ü)Úg¹mâ§\x001d9h&\x0014ËIyI#if\x001e±[Ô´Ëò&\x000cÙ0?¯¾Jxfñq²Ïõ\x00192n]Ã.ËÛW\x0011g¨ååmîE<¤Ú6^¾wZÞ8s;âÌ«\x0012?É7Ënñ6Öùî
µ7ÞÜxóÈ\x0004]e·8Öüonê\x000c÷ÔjmÜ¹\x001dqç!_@¶ÉòQû¤_|c\x0002i§Ý3·#Î<p[³|pÒ%w~\x001dÝj¸k<¢\x001bñõªµÛÏs1ÜÕ\x001bé\x0010]ã\x0010ÝC\x000c¬ó$_J>1\x0011\x001a>u»öÁsÈ­0¡#Ôþ4\x0010ËMm\x0005ÚbtÜiys:ÝÈédÍ3'þ0±\x0000L<S\x001d\x001b­0;
o§\x001b:9îK3Ë®±ôD\x0017¼n\x0016³Ñ6·Óò&×r#¹³QÕ\x0012
7"l\x0016¢öÄÙ©aß7Å8\x0016\x001fBe\x0008\x001a\m	óSÓrßT*üH¥Âgåµ\x0012:ÞàÈ×)Ø~Ýû.Ë\x001bèG<¢ç[³/ÙâòÉk\x0018Ì\x0006såNËJ\x001f©T¸|<ENÊ\x0005(\x0013\x0010*GÁÔ½Ò¤¶~$µõÜãtjê,}Ñ&}\x0015
`¦Î&\x0006ù\x0018de±z\x001d\x001d!Q(Ê7!íØYtömÓÍHfËté\x001dF	@¡¶+Ú©»	~$pZî!1z{Ã5UÏÔ£ÙDN?\x00129=T\x000eD\x0007Q'l}Ë
ÙÃL´<4\x0001(\x000c\x0005 \x0013y(\x0001Éfqõpb·ì|å#\x000f#Ü±HÕi²Ð´,nsÂÏä¡9aät:4ÚÂï¹rc&Kuö¢[h¹ï\x0001ñ§Ï\x0010\x001eyCÔì6'²*®\x000f¦>
¥áï½Oüm÷óòÌß¨]\x001fy/\x0017NÀª\x0013ò\nêsùïÞNá\x0007ö¿4\x000cMB¿Ô6\x000cO}£þÏïwkâÃòÞ"¿\x001c(ë¦(®\x001e±\x0018Î¥Ç¹YX>\x0002¿\x001d_ÆL)ò\x0019°ðð\x000cL}\x0007 ó=D4²JQ\x001d >\x0007Ó?uÿ4·!>8\x0004q\x0010@û¨.vÍ£úT\x000f\x001e\x0000H£\x0000ª0^vIÒ)Åý\x000cú4µ;ï Gxðü\x0006mñùI^Â\}ï5\x001b#1{\x001f\x001e\x001cÑ\x001dô?Ó\x0000\x000bÆüÔ\x000cºä_<àV}-Ûa{ p*ÁL±å­ÀÙ¤/KÖ\x001d#oóo·\x0001à\x001aÀ9ëÊ^\x0000Q\x001b¾![,p\x0014ªÔ¨íVÛ\x0001Ö\x0000Îg»w\x0003ðõb\x00089
£Pp¢\x0016'­Ý¸c\x001d\x0000`×\x0000Î¹Tv\x0003HAIôeÂ\x000bá¡õ"n\x0001t7í\x0000àÖ\x0000ÎiSö\x0002\x0008\x00023Êø2h©ÒÂYÊ>ûýÚþsý;\x0008´Õ\x0007jÃ)sª\x0018u¿Æy7°\x0006pN²{\x0001|ÔÁA@«\x00000é×¢¾â\x001aÀ9ïÉþ\x001dä¹àªgØ\x0008;&Ö\x0013°Â¥Ïþ´¶ÿ½t·ýùÒ+³Ò¼\x0000¶\x001catJ¼Ð+æÕoÿ¨tbç\x0014-»\x0000Ê±ó\x0002\x000833ÕÖ\x000e;}\x0003A\x001bGã0°,¨®@T"4TW`ÏÐs\x001f&\x000e?à\x001fÝ\x0000
w¤% édvH±\x0006ânaãn\x0004M\x001c{@Ë¹
LU_·¨¹\x0010ê}\x0011ÌÄÐ\x0004\x0007t{\x0011\x0010EÚ'gÒ^ùñ!*ó¡
{|:\x001dé:.ÎôÁLùîHæ$+u \x0004z§½´Q-?âPÏqü\x000býg\x0002o¤|n\Òä\x0014I'âÉwÊííZÕý¬¬ÇZ[â`TÔ×Cö\x0015wÝÁüw\x0019I©½åä_4ãüÅÔ?ßß}`;_¾ûøy´47\x0010r3\x0006û\x0002\x001fñ:pá6X\x000cëmmù+þüäv\x0001öòÙ«74¦\x0005\x0016®aáDX1i
¨0YgXµ\x0014\oÏ×!Xv
ËN\x0015¨Öö,Ë\x0011\x000b\x0002ê¬F\x0008\x001bJ-c°Ü\x001a\x0008ËÇ:ìkU4;ÃRøä7\x0012®1X~
ËÏ\x0005\Å/½ØKQvE¦
/ô¾ä\x001fÛMagÙM]gçHÒV©N0£Ú¸Å\x0000}\x0010
g\x000e1oùì\x0010_|üðåþ^\x001cúÓOw\x001fò\x001eü²O¥%\x0006=^KòSò~\x0017ÏÒÆ\ÎW/ß>y"ýéëÛùO_½½D×"pp
\x0007çÀ±\x0006o¤\x0014\x0004(PçjdØ
-ã`h
&­
ÁHî\x0010QÆ`\x001c+:ÉÚl	©\x001dc×pì$8!§\x0010ò2ÅqÁXÝj\x001b\x0017ãpÜ\x001a\x0004ç¤\x0011ÍI·Ví^8iû8°\x0013&Á1õ\x0001É«K'³\x0001*\x001cwùòv\x001cN\Ãàå¨rv¬Þ¦\x001dæÝq£¦z\x001cNZÃIsà`Æ ïÌÉt¥Âju¹+XéÉpÔ1³v[e¯3Ù-\x0004ÝmVñÄqíãxÚ(:)"N3m\x0015ªA¯Ó­DáJ¾
0
â(&Ôô×d¿¹\x0008W_&Â¤P
.jÜ0¯AY\x001fTN ²×¤ÐDR\x0014JYNh\x001a\x000bÒéë,b­*ÀbÏ|ñøIx¸ëWà\x0018B,´IÚÆÈmÌã\x001fÓR\x0014KMrZÊ5ÙnÙmU¤pã5à8&Â¤`Ê"Y2\x001bl)IÞÇPË¢d7änãi)Ì¦>Æ$8.eGWÞ+m"\x001dÀ!¸;À&â¤h
E\x000baY\x001fÊâ\x000e4ú¸«Ý{ZÊì%»æ_LK°©&Ød\x001f&ØW;Eç¨ N\x0005ê­¼c©¾Û^ËÙ¿.wY¨0\x0006\x001dá0Á(¹¹u:þx½ü\x0007\x001e¬\x0015Ì[«ä´79ä\x0016AÚZK´¡cv\x0000U</~Ç¥øýýÝçÏw½geè×wÿýß»û\x0003Bíñ1^úr¾ )<°v	Ç÷·oÞÜ>}ÂjÐ¯oÿó?/ïãy;.uîA\x0004±2\x000bs*JÕÎrk6Æ>@°k\x0008v|\x0011*¥&ÕçQ\x001au,l<Í\x001dpÆBÎ{1_\x0016u;Ù\x001bQ¢¥ ýJL|0
H:ëyË¿xÐóöúÝ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-04.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-04.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¼Üi\Õ\x0002)ÿ\x0016ãô\x000c¾\x0003Ébs{Ùám9w9Å¯QFÍ4Íµ^ó\x0016G\x000fU\x0012d­äuÄ\x0018úR¿`"\x001féTß;ôÀ6m	§NÕj¤âÖÝu>²Å¸à\x001e\?\x0003F\x0002+¿cuÉëWa1.x\x0000Csx:\x001eX\x0012dÏKkGY£CT¡à(È\x0008P4g×Þ¬\x0018o¦TÃàÛÜR§bcßÞ7JÔÅ\x0003«é=euÆî¼qîiÉÁ[ÉëÞ\x001dú8\x001aAÉÍ\x000fähd1å¡KöxÙOëøÇ´RC\x001bóX6qö×Î\x001cõqÙÏ	\x000cÀ¿\x0003ðJÖb\x0019y+ó¯ég\\x0005«Õ<:UëåáÝoÄn¿üôû<7õ§GU+7µ\x0014()JøÖz	Uþ5\x001e­ÚÇ¦êû\x001e~§hËX­´/,\x000f/Çk\x001d®VC¦|+@ÔZT)\x0016|¥ §hÛ:\­æ\x0019´mâ\x0008±©
\x000br¦V*oµ¯¬ö!ë\x001bvÁ\x0014%}.\x0018]³çS²±nåaÍ	<OÑ#\x0005©d]3\x0015ö\x0015yB«æ´9\x0005\x0006¶ôtBrN#ïsÛ&¶În¸\x001a\x001a°¤\x001d5¬Óþ¼Ïw#åõÄ@5ï¤<±ÅKô\x000eÏ\x0002]³±Æ¼V ÈýXs\x0010¯\x0016¥Ý´æFóÅµÅ|\x0011¯Vó¬OzEÃVÙtàêÖí0N[ÏØ\x0015z°Âä\x0016­ø]\x001aú\x0006-Ò\x001cm\x001d\x0008W.HÊ¡u}\x0017/ãÈº\x0003u\x0014VìÒúVª_,é\x001d}ä|\x0006t§OÈ­L\x0002í×:á\x0013:\x0003ô6ì;¡5È'5úuK½§Å\x0008íÍÄqv¸&h,Ð{
\x001eÃÌ\x000b\x001bc;·\x0008ö*òôááN)\x0014¯ø¥Yú\x000c³«¦¡N\x0017´oêÍÝI9êøùQj3\x001dÝ'dj\x000f	nô\x0001Ç$\x0001®-©7&2ð¶R\x0006´>XdNö$°_Ý\x001c6Ñ¡À0\x000f¦âåØX ÀL¼UGÈº0\x0006èh½\x0012©oêÄµ/¶ÂÔG\x001báÄâÞ°y®c:\x0007n±;\x0011:oqXR<NÜ#\x0017ÑX|L\x001d2öAÈ»\x0019\x001eJ¹Üß¡!c \x0002\x0017°ä\\x000c/®§Îkùz\x001bé®<®Øã\x000fnØ:C´×\x0018¥ÍäÂ\x000e|4êèg)ç0{î4ÐÖªb\x0004\x001c}\x0007öÚU^øè:)ÿrý/\x0007v!:í¡w¸+\x0012ÿðÂ·}ùr
þå+;ò\x0014«\x001d_9Êf
Ô¿ùôòôùñÝ?|þñnXú8Vâ<%n¼!U·\x00139t Þ6îÚYcf\x000bÕÕwhRÐl$spHlxgòÚn"£\x000e|(­Ë?IT\x0000ÑV qÅ­Ù\x0012x-\x0001âìñEX»¾N´\x000b\x001bUùÙ\x000f7[\x0004/ÍÁ Ã@¦)Gß=#×°Î87[\x0004\x0017[\x0000Av#´Ruá\x0013¸Ñ=q³EðÒ3$Rø)cð½½­ùì-U_ü¯ZÍÚ\x00177Ó¤×¹w&"¤»v\x0017m7Í4éµªóE°ÓÑ(×ÌFûuúvGIÕêA0it\x0003¦ztXè\x0018Ði¿Ý¡aTUIù\x0000Ù62Dó
Ëb\x0006Úo\x001b\x000cò·\x000f\x001f¾ÿôñãÃ{¹I\x0012J¿¯ÃMÆc¼}ÿ
oËM¶\x0014^èÐ4n²èKðÈöX|Ðò| èWC7dp±%\x000c±(æ0£²º×¼!\x0003Q<í«}(Í\x0019gÆ¸Ëð
\x0017d\x0006W6$\x000eiú¹'\x0006Þ$üÎ"\x001fþä#ÇÄm¯ÜXbãrK©\x001b,Ø3'3S\x00151ê/çS½ÊpÜ+øÇ\x0002þ@\x000b§?õÿ\x0019àU¿ã
\x0019<o 	s%\x0019¡|pÀ\üó5¯\x0012\x001c7àþ«±Ò¯ZøÊ¥Ohté\x0005\x001aÓZ\x000fÉ¸Ý]^òÏ´ÌoÜ!FI\x0011]Ø/}@\x0012\x0015Õí(\x0017"\x001fÞ^\x0016*\x0000\x001bíÌìzªw:Åeâý\x0006
zrú=8=Rüãóv[\\x0019
jå·K¼\x001f9{¶ì¶\x001cl¼\x0001ÔTÅ\x0006Þ¦º¤3[Ê&ëØÝBD±;µDª\x0006\x000e\x001c½G\x0006\x0008:ß<ouÙ\x0004mÝY}c½C}CîfªÍ(Wã»Ùñn×Évþûo<Û\x000bÝéCpå²\x0011\x0005Üi2G0¤ÈÞÆé>17\x001en\x0016Þ¡ú£¬-ÌÚÑK3{>z\x0006VZ0\x0007:ÐÉ)ÅF;FÇ\x0016Èµ&^»r£/âfãçï\x001e?¼ûÝÃ\x000f\x001f?}¸Wìâ ¤å_\x00116«FÃ[kE¾ Æ_ø8Ãö&\x0007\x000c{Õ6Z³û\x000c,ÜòRÝþ\x000c\x0001±kchv"7ó¨ÑáNF\x001eY\x000fÖË\x001eàGÂ\í©aé\x000cÎ=§~\x001bé¤£õòüôÝã»|øÓÝ(
cjíæRuVü`G\x0011ã}ÿæ:\x001a^UþÓ½´]îªV|ÜÚèÃû1%Ú\x0016e\x001d]\x0006Å;p@`@u\x001c£¤"Ã®ïvTÐÿuXi*^O¯¬D\x0002=
Wj7dÿu\x0011j¼:iÁº´É<g]\x001b­\x0001ç«~G«Þw\x0018\x001ck&v³ÔYóGä\x000cw½^{*Y·¾\x0005ûuP¼Ã\x000c·üö\x0006È%\x0013ñIdU\x000bµA©r\x000ewd\x0010ÿM¨£+kÎªÊÔ',k®uEË|CîOÛÔH%Õ{\x0013÷¬\x0013\x001d\x0013\x001a¢âåM'Ã±z³ï×¼Uý®l\x0004C×\x001ce`	oG\x0008ædø%)Ç
\x001a¥å+Ù
Ò\x0006s:ú¦!wuê0ÂL
\x001fÒ
Í±«gWªr¦«\x0011Ê\x001b4D«nÓÙG~\x0005¿¤ÛÐ\x0001¿bÁ^\x0014\x001doHãØ5¦U~¦ú_YöÊß>üïÇ;¥g¼¹\x00100ÔCÆ/(Ú\x001fz \x0012·iØÛºêøB?\x001fâTÏ÷Å T\x0000¹\x000c%´%ê\x001by[P¥!oLç;cG\x0006êqß¹®Sýõî\x001b\x0005¥ÌÜÞ|àF;ÔÞå±#\x0003íMnXþô:»CT¹\x0014k)j8³³íîÈ×|4jG\x0016ÑÞe°\x000cÎ&ïz¾4väJk\x0006d¯j¯ÖÌ¬Ô¥u&eGn´æÃÿ*å\x0018ó\x000bi\x001f.­ÙÇõ¥±#\x0003çÍÚ¢¾jëÇ\x0006\x001cQÍ\x001d»\h#\x0012³ï9«\x001cNòËv\x001cõ£\x000bê@fB\\x0007?ü"\x001b±##ÁKAI W9Ê\x0007Ïòþô¾:\x0017À¤4	NIW¹hªÊùñç\x0005eÑ
\x001aXu\x0016æèò¥ÛÂÅÎÅÉFàÄ,4¡YH&\x0003z#o,°\x001aQè<Z[Oü?7h$Âë¨ç®íö:Eã6ò§ç\x0006	,¥Ñ¸²úPþò?ßq¡Ø\x001aÄãów\x000fßßí­%î¬PkA\x001a[½9W\x001c7P
ñôz[\®¯)ÕêFÙ ¼Í\x001f'\x0017ÑmbÑ`9	K©ñ	²MÐË¡LT¦÷#äùµ\x001aU¾á\x0006Y«`\x0007¥§hT\x0002uÊÛfùÜÀG»L.ØH¯\x001ad\x0005¾éjYòªL{C>úerF\x001dP9Aj_*_\x0017©e\x0015b"\x0017@N0r$È\x00145\x000bO*§M¶ûä"'n½ðØ0#?*S*Í+Þ§«s"|Uá\x0010E|1Í¢ÉoÈ<\x000eÆÉ÷Näc,Hs9¸æÀO\x0017±q\x0016»k©n6¡QÝLÙÀ+ÅU¬i÷\x0014x]Ð`â k#ßË«ö,²37^\x0019
¨­êxy\x0003dßØ\x0002K¯ìózZ¼.¬çÝ:ÝûÓ<ý÷O/wÊwu*üË\x0013ÍëëykÛ!äøþ[Z\x000fã{¼)\x001f\d½¯®Ö-5#<òÔÃv)\x0015r§	\x0010C®¾ìv¿Á\x001eÄBÚÁ¬í§ÉhãEÎËú`ùo\x0016$_èr´ºY±YòÚ	;ëõÇ!½I÷Û:iÎk.K'ì¬\x0013\x0016äHþ²\x001bØð&È<ù¡}(Ë\x0017uÂ*+¡jwd\x001a\x000b\x0014*oçú\x0005cÝpWÀûìE.7³\x001byÕsCn°æ\x000eIvíVFØ\x00196ôõóÅúà>~=mrKÌV4¿ÎyY\x001fÜº3`ôw¸\x0013c+F^#®ßEÖ\x0003«À\x0002HßÉ\x001d×á\x001asv
pZ'Ó©\x0003wåg\x0004æs¬ÕÈÈ¡.ÉsoÐ`röÈgÎÓndcÛ#-µÈÓ\x0015Ó$«¦'¨öäRëWk,«\x0017ÂR¥û\x000c&(7tóô	ñµ\x0018:¼,Úùu\x0006°\x001as\x000f
»&j£\x0011HÍ½òÃÅ[qÇ\x0005\x000b¬4,®-Õ4PØj5Ð\x001bIÔ	\x00029N¸ÃtëE5:7²ê\x0004bX?Cwh0ÃFD3zðH]M3þ¼ê-ª¿2Ã#i)«nH°$[Ë\x0005÷îy:OÙ\x0005Ö/Ü\x001d\x001a\x000cQââDçº¡´ÒbÎÝh\x001a½2Ä;W\x0007Ày«=çÕqò¢ÓÅÛy\x0006CÜYKÇ\x0003­7c-#\x0015t¢Ï½A\x001f\x0018CGïßtB¶:\x0005VGÙÄ\x0016Ïò\x001d:ÃWì(ì7zÁ\x000b}E³j?¸·Oô¹7èÃ\x0012u:?ãª3\x0013Á\x0019æM\x001dÙ\x001d)+c<èsu\x000e\x0018#Z={Ô*©Ó=E¾2p\x0018LLXj\x001b\x0007\x0008Ûz1>o;Õ'öÜ	\x001dÁ`t&\x000b\x0016];÷»öÚØ\x0016ÝâÁD\x000f«î8ÑTDöÃèý¸1\x000bw¢æ½!Á¨V\x0005jÙ¢E·ÆVî6¦±+\x0011ö#î¶hÇÃßÝ8T7è¦O¤¿7d°ZßJ/EÕG3TîûhHWÖ\x0012ÁZJ\x001c\x0014Ð·%×Ak
»A´\x0010z¤ÇýµD°Áçé\x0008\x0015ÑkõÓ¢Ç\x001d\x0010¯®\x0008×¬\x0012ÎÆÿOÝ»íj\x001c×¯RÐ½
y>\²9Æ\x0002i\x0011¤ \x00183\x0018\x0010»«·ØÛ®®ê©\x0003G2 @·~\x0004Ý
æÊ¼7è7ñLD~\+3¿Ý\x001bU¿5?aÃ0µÅUùÇ\x0019\x0019\x0019±b²á\x0007¹ñãÂ\x001cájG\x0007ØÑ*uÕ5\x0012Éì\x0006ýÙ­ýgÁÎØû¶\x000b¨\x000b ýÎ\x0014y\x0004Ã­®¼Mä¸Ú\x001b¡ï`ÏÞ\x001aTðr\x0011è2@·äÀÔ±Þ\x001f\x0016Ø±\x001e=¿ßÜ\x0010A\x000e¼òÈY\x0011F_?½ùþñí«_¼ûÃ:R¬¡d^*¦\x001el%-A\x001d<ZÈ]½°_(¡\x001c²V6\x0016üºV\x0018CÍ\x001ffý¤ìÌÅ\x001b{l\x000b4ZÕ?/P3÷vXCÄ\x0004ù\x000fÊÍÂOmmÉ \x0015o\x001cÕ\x0008­x\x0011{#>z%Êx"\x0007@.8«GìômAi{³pfcûÕ1÷\x0015¬l9,w\x0017!çmÌÄÂ
|\x0017»ó¹}ñ¬\x001cû÷l°P$6QÏ° gR/K%\P)Ò¨ø£È}x\x0008Ò\x0002Ì\x0012ô±.\x0015Ndø{×û±5,\x000fÆ°J¹$hyÿ\¼£FÉ\x001f£
\x000eös¥O(\x0017\x001b©	É~.Ë¬áÈ½|z÷ôæíÃ­R¡0m?·GÇÁò
ØÇ\x0015µ>pwåI«\x001d\x0007¶Æ¼½¡F\x0017ù%\x0013r&Ë¤ºìR;AªµâÄÄf7O<¶Â­\x001djóuæ­\x000cl³R±µ½­ëP/,k^u©È;[©6uRF.DÊ["kñÔ\x0018\x0006ø62NÀ5\x0017ÎCj\x0018Ù,ûßNäBÈ\x0006¾`¢ÏW-olïfYsñß#åçñã«_¿úøñý»\x001b5ú\x0014\x0002sP\=²ñÊí@Uß³½»¡÷Ê\x000bI¬P,Ç
òë\x000cª,k\x0016\x001dS>&\x0005noÏ®ý|#P\x001b!;7\x0010RÌl×ùø2òTÝ\x0014
øm|\x001bhI$>#¯uåò\x0000`Õ:\x0017¸:et6Ì`ÕuP§"îWko5Bu/ÕLÁ!ÔÈ ¨½påîÈÒ¶ºÅy·Ö±°\x0006\x001cbuº6
ý
vkU¹üån­c\x000fa£'Böº\x001aî¦
e@¶­¹xÞ®uì!T6oDäJÄ,Y3)èjõo\x001dÚÖ±P­Ñ/±¢R½©\x00122O\x0000ñ~\x001bb^Í§%xû?\x0001<OÖB~x\x000eÞ ¢\x001fÊQøø¨Ûðó\x0007PñôøîÕ¯\x001f>Ü¬´\x001aôëÒ°çc\x0012\x0012 kC\x0011îët¼P·Z\x000c;TV=\x0011-µxH9vµ'\x001b&-\x001f~'2fÈ
ÈJP]9È«Ù)§µ\x001fÆÊkOcÉ÷ ½/]2×VSõká[?%ÿA\x0004² gJSÈ9¥Ã8\x0017×Ä\x000c	2
\x0016;pdjf\x000byÀµÍëé¡~\x001eºY¹·\x0005\x0015\x0012!cX\x0012ë­ò~iK\x001e{äú{
¡b\x0017Î£,0äSµçxÁ¿\x001e¹ipýôþíÛ§[Ýre\x001c
\x001fÓ¿i%yP\x0011ªª{w1ÙúÙ³ ?N\x000c	ùT9á¯£ôçdtKÚ\x0001\x000b\x0005ZoQ·ºAÕ¡¸¡¾¾M§]P*'D\x0008T_×v#*uú¡
Âö'2g=/Uýîda®};\x0010\x000b\x001eöÄbø²\x0015/2!yªÓtª\x0014'V8
Ã\x0017\x001eôñ¶\x0008"ÿùýÇ÷nuÀ¬õÄü\x0008=\x001fa¤R¼à*±nÆû:`køÅ'\x001a1³¨B\x0012¥G©;}ïeÌúi2
cÊS1\x0000mCNfl:z_#¹?g[m~q\x0010\x0006aÌl£\x000f¹òj-O4p6^ô:\x000cºb\x000bV£\x000exÈd\x000b:	b|Ñë0èbÊ\x001e²pÆb2ÂSÙD´÷bºèu\x0018t1³õ8Z:Ö<d^+KLªÄºÕaÅ\x0014+\x0017Õee\x0016·Þ2r(+áã\x0013¹Ò÷,¦\x000e\x0010KìÜ`zA¼\x00195&õ@V^ÌÁ¬sks\x0019Ìa.7£Æd¶Õà®Ó\x0019bX¶6\x0012U\x001eÄõx³C÷
ít¢9\x001cÄ\x0017ëxú­-ï°j¦\x0018Ô+õ´Âõ\x0019u¾\x0013¦Ä\x001eiøñ¢áÁ1Ó¤Iéá0\x0014ãÚiïÈu8+r\x0001Ì¾Ý6DðíÿñéÍOúñû÷\x001fôÿûøãÛ\x0014Àlµ¦åìÏ¬Ø»Ëo\x001a\x001dywÞýeâjMöîQÇáv',o\x001cCeªá!Ý9-%âOà>½ge³g½rí\x0007lè°1\x0000D2Å¿%\x001d)NËÍ.-\x001b\x000fàó èý\x0008óJ\x001ef`/©.
\x0011rqv\x0019>\x001dÈ}*²Ï#ØÂ¿\x0018UmáÙ\x0014qÉÄ?p3àVÔ5uKtàÌ2¼y\x001b\x0019=yö\x0003¹O\x001bÒ³ÚdÒzcFS\x0018;\x0000¯\x001dû\x0001\;pÉÀ¶J'[M\x0014±ÊöF\x001e«u;41úBkÌwÆ\x0001í¾\x001aúj;ÛðuÐ³ô\x0003?à?¾\x0017?ñÿü\x000fÿÍãÛ··R®\x0014§Íi\x0011Sv¨ª\x0013cz@P¼ßè²÷å)×=¿ÓCSL:>4%Øl«u ìVE­±ø%Sà@F2p@\x0008WËÀ_feeAn=$³\x0013öã\x000e±f[üH3óU\x00199-Cì\x0003\x0019ÞÕ\x0001´èä¤JÄ'[\x0012#·\x0010mvÄ~\x001aÔQq<wñÖ°\x0018@u<ÏEÿ\x001bKGì\x0007\x0012x\x0017\x0012ßòc×R\x0018¹Mj]±\x001fG(2HÞx;|Á\x001a\x001cÛ¹öü\x000c\­ì ~S¼¼½È\x0017$¥mßoöÄ~-â½T¢we¤Ú\x0019Nømêw\x000bGì\x0007ÚDÕéN \x0013¡©4Ê~\x000eÔÔtÑ\x000fu\x0000CÆæÛ6ª"²çÞä¼]{x?\x00102\x001a»,ÃÎ×.\«gÌ\x0003\x0019R¶5¼\x0003¨ý Ì[Ëü\x0001]KP-®\x000e?P=â\x000bEâ\x0013ËÖ\x0004Sl°wëGÁ\x0001\x001d\x0001:BÒVçS\x0015ZtIü	}Ó©\x000b\x0015¯sã¡WËcã\x000e\x0019É|<?@²¼ôÂP+Ñ¬Ïß½}R¥[e}áÎ\x001fyß\x001fósrDÒÏªw·]ZhxÍg-\x000cÕ\x0011ùq\x0011;&¨¹)vá¼ÙÕ¯ûû;yêHÁq\x0006¥p\x0004XM\'}\x000eä@È¡y® \x0013?©â­´\x0007rÏÍ(\x0014¨E$Ý½3PuuBn-\x0013³sß{\x0006%\x0015Xoäm)ìÛMrKåù\x0003\x0017k©: ø¦è¨´eUªm|8»ux-´÷¥X¸\x0013º2¿L\x0016½\x001e)wB«¥\x0011ÖòÐãEg^tòk¡\x0003\x0019Íì\x0019S\x001ar\x001câ(y7oùÊÐ\x000e\x000cMÃoå?\x000e´%ÊÈ¡.\x001bS\x000eh8(q´Û\x0019óv%X>(eS\x0017ºú\x000eNJððÎªÛ\x001bh?\x000fÅ$¹IÒ²Åãè=¼gts¶±ØÄ\x0006ÙÜÕWtð\x0015×þöY_½lÄØ¡=|Fgp>Ê3ò1<´ÌnUÊ¹]âÏ(ë1\x0013®v×\x0010nl]øsGÃ\x000b\x0004úRìV©ðBÐ,RµÇ½-yuI\x001f«ÆKºùS¨ÉZÑ »$²½KX\x0010Òl\ÌCû\x001fÿúo÷á§?mWöøøæí­Ø>ZÌ%õ\x0001¹ NIª*¡ÞJlß_"ïej\x001dbÖVC=ÜtbEËð\x001e.Ú±¼²ãP\x0000JUô\x001cEHÂ5#\x0017Ufd¿¬\x0000\x001dÈ¦<¢îãöU&J1½N³\x0013±@\x001c
@²ä\x0002ñ|RÚA¡\x0015'^±ÉKÖÛ\x0001ÜYoòn¹+bÈ¶ -r]q^ª#\x001eÀ	>\x0005:Eét¥p¶¼´N\x0013Æ±þct\x0016|¾È-(¦²¤¹ÐG<\x000b|=ÖKYìê)³Y«Y«\x0018îÐ=i003/¸MÔ\x0001 )\x0018\x0010k§^\x001c
@â\x0005¶©b'4÷¡ëä\x0018Ú-ç5Ð°ëj8C\x000câ\x001eZI([¡·\x0019ÁWÛ\x0003É÷&ÒIñµ¹²\x000eê`ë0¶\x0011Üi\x0006æ\x0007óðôO·©¢äâ(hpÇ\x001dt² âZ½½/f	;Ì½
¶IÖpí8I=ÃëbÞF/wÃ\x0018êºÏ!¹e·\x001dÇ!ðb»\x000e)¼ î\x0016ºPÄ·a_B\x0015ÃÀÎ¬Àñ+W¼peCí\x000bçlØ87<\x0004íí	\x001dXB\x0003Ps\x0017[$.Ò+\x001bÒaAg½C-;ÛÂ#\x001es&"Q\x000e>¯eû\x000ehØr²Ìæ°H\x001a\x0017è@ï\x001aY~Qò\x0018g¥MÏ\x0000EY"R\x0005¹ô²Æí:!\x0016XÛuè\x0005ÄIB¿n;ÇÐÑ^ùß!#&Np!5èÌûÃóþ\x0008Û»÷jK[ÜÒH¢Èâ~¡)^ùÒ\x00081­G Øqº|CÔk{ÚãÖ+CEsßÔ³BÅ\x0001\x0001Úbk\.çÃ\x0016\x0012¨Ug]Ö/ê\x001d¹\x0000rìÙc}ðlQyåñ³_Ë$\x001eÈ\x000c
¤ ¢+diËµÇh[GÐâ±¾A÷Çz\x0010ðÆõ8Vh6¡m£fiÕÅ®\x0015\x0018\x000fh8ú&¶7¦g\x000eyléE\x001a`Gî\x0007QéV\x000eNbmJ_4ßûa\x000b\x000bgy\x0003ùkïE~aGîç0ª\x0010Cù\x0012\x001eñÂMñâm\x001bV§8 ¿öjYd.vd<¾±%ÏE×v,aãF,z{?]\x0016§Å`#iñ4¼²\x001dqò\x001e1lTó«ãâà¸H\x0010ÕÓ\x0000±¨\x0015ùi\x001dC]SìÈ\x001eO¶xÙÒý´aKoíËW§ÅÃi)8M\x0016]ø ÊíÂû#tË\x000e
Ç%zÜ\x001fÅeÌOZÕØà¯è[RuV§8 =|E\x0007Wb\x0005ÓËú\x0011ùI\x0012÷\x0000ïê¼x</\x0006REdêLÏÕ¼¬Îú\x0014\x0007tE£.J\x0014ï0¸SÇÈ©=þüÕåâár±o\x0010{W"\x0005zË
\mj_É\x001eÁÑ¢ibzÉ?â&^YËÅ}ÛþÐã1\x0014Îlé\x0005ß\5c-cký*ov\x000474®ù\x000bãõküa\x001cô\x0017\x0006Á\Å\x0019\x0005w¹ É\x0001 tæ¼%Î!8cJg(MY`Yùëð¸xý\x0007\x0008c¿\x0011½,\x001e±ªý£¼`ß½ùðp#. <a\x001dåÖKj\x001bn{ä{\x001dY\x0005ÒáyKxßÕ+V\x0002/ªûå±ÃUr@ÇÐÐél=65ëºß¤ï\x000b¼\x0010à@l19\x000b'ùvRÌW	\x001e(9X\x0013©\x0006c¹=²æ´\x001c7d'Í|_\x000c¨ÙX²$`Gú\x000fE\x000eÚk8Iæë»\x001cuÓ¹Þ>,YävRÌ÷ûD¤\x0003y\x0018Y¢Kf[µÞ¤\x0014ó\x0004\x0000\x0005á¦ºyÍ\x0003ð:8	æûJâå\x0012e±»\x000bÃ´éÔ\x001amækd\x0012ÌoMm½a÷¡+°äÄßo\x000b\x0016ú]ÌÝ=ÛëÌLÐ~8'¹Mb\<ê'-~/Ï\x00080\x0014R\x001d1\x001f@\x0012ÅõðÁ\x0003Ï \x0008
Û9y-«æ3X&Ââé½CãQ±XsÆSIQ¡Y3ÀlÃö®\x000e\x000bÈý7\x0013Ãy\x0014ªÑJ\x0014A\x0007»{B'Z5H?©ZÊ¸ê¡ë>­%\x001c\x000fhØÖ9a/¶Çc3DXï7\x0019½«Íç\x000cAã]b
])¯z5¨Ì÷¿yøðÝãÇoÕ\x0018ý çj{c±ü\x001cÒlÓdî®³ø¥¸¹ï¾$<Árø¹
/ZJC©øÞ²uÐÎÝñÕ$\x001cO\x0000Q!!îI4\x0017Ë:NÂÕY½\x000eÅQ\x0004F\x001eE\x000e2ãìë8\x0000¶V\x001aÖ¡ÈÔ\x0000\x001c\x001d\x0013\x0002Ø°öuTçÿDv.\x00113«º\x0003YùÁmýE²\x001aº:â\x0014Ä-J\x0019º?£gÆsMôqáÎê¨t«SlpÕ\x0012aÑµ\x0018F±éMDw¾£ë¨H«\x0006@\x0019QÙ\x001eu\x0015\x0002ïMÛu«£l¬ü\x0002\x0014P¬NO$ß¥²Ða:«£´«J\x0019´G\x001e¶^\x001cÚV·Yh³üÞ¹«a\x001ci%ÝXÝ|ObLÃ¶vWÏcgÓ8ÒJ,è&ÿH\x0003)ãØ%¬\x0012¯\x000b_ìg&£øã\x001f\x001fÞßÊ\x001fËÝÄ3\x000e¶}¶ß(z@Ôï¶9\x001a÷å}Ë
½À\x001fûéMéH½âID;pJÜ\x0006'-Ü\x001e	{ÏM,CìÊDV´\x0014Æ:!è	84À¥ò59S²®¡íÈ\x0010ÈkU\x001a=\x000bÇKxÄA \x001cí¥Âû\x000cñ¶
ôÄSz=Æ%v\x001cù´µ°®\½\x001fbCá¥	åPÙêÛ-2
D>wG\x0017{\x0017HAN¹ï\x0017\x0008k$i\x0017/½Ä\x0001\x000f^"\x0005ãh°IôÃ\x0006\x000ce\ýb­qØ>~zü|£9G.%vU¶©|mnN½\x001f§
máÞüÃËÊ\x0015pMU\x0013@:'Cm\x0005.f\x000e×ì6Wb~oÕ¡¯§xGsM¤½åÒHÈÛ\x0004òã\x00198\x0001Åá×(ü®uâ
(¤KnÝ\Y\x0007F@[\x001bO°Ö@¬Å=\x0012\x0012ïÔj \x000b6P\x0002ÄÈ\x0001ÉÙ:½²i®aµy=bã@N`\x001a^YûC#YJ÷òùü8U\x0007¶ ;¤
ËÎ Ú° \x001b&@nr~\x001cÖ¡©GìpÚAV\x0007Äv¦*Øù¢Á²\x000eD«úì)_g\x000fê@	(NÉÍý\x000bÚJÏpìÀ\x0006­\x0017±ö@\x0008\x0010Ü_Å°B\x0000ûÉÚ(Ãµ,Ê§µeû\x001d,Z¢ËØ}{\x001b\x001f«\x001e\x0003WS[Ó`¬WÞþp\x001a;ÐÛF\x000bÊ´õ²5¼õÝê\x0014"ê\x000e\x001e\x0000<\x0013qXíMàÔ\x0004ª¶ÉlàëãØþpÅfL©®!Jo8	\x000e¹÷ ºEo¾3S\x000eáóÛW¿øðÓw«vSG<*§û\x001ctu \x000c¨aí\x0002\x001a÷u)½0h\x0015K\x000e·Ò­¡¿2â}®²pxeIç=aÎ}õ\x0005,:z\x0015½aù÷|ÁT;ûyPrB-ôEhº+vüau1\x001dÈý0èÑþ¼=g>\\x001eô¸bY¦â\x000fä\x0008È¬|*Oµ\x0016¯Ç2b1,\x0015h\x000fä~1åÚ¶
f?¹ÀÏ\x001c[·é<(Ï\x000c\x0013t6\x0010<\x000f)ñYÈ\x0003²¿\x0018ggQJ%;\x000bA õÎúaÛEÎÙ)T\x0015ÇðÛ÷n4zZ~"\x000b\x0003\x0018sÿ
	º\x0017Ù2N~ÁÑjkÖé»*+\x000231Í\x0012¶¦ +\\x0007¸\x0005ÏsIÕXÞÄ}YJz\x001eÈÝ+$ÕxN´b¼ß½¥A\x0016mÍË£kÇR¯Äþs\x001dQÉ\x0015ÉÝÛÁ'\Ú1î[ïg·Þ*8;+[\x0007\x000fÍL\x0012¤.`Ê¼!×å\x0003y¶\\x0002Úb\x0018ã\x0002>	\x0014Ù­Ã³\x0003ºEk=ÊÓuaøóÕõ^¿ö\x0008\x001fåLÜÆ'X\x001e`®Æ;Øó¹âÈ\x0014ÃV%½/¢Ö\x000c_0§wÈoµ_\x0007b;Ñ\x001bV;Sµ\x0001²Lh¢dA½Ò\x001bÛðD4,ÌVg\x0007»e%ã@îZYÅ$È8&%á£ÛV~t+©Å.C\x001d\x0019:T³¸9)M	sr¶rscÙ\x0008-\x0006êz¾Ï\x0005¸6á\x00138ñ¤×êGà¸Û9{gcsâ\x0016\x0007¶\x001aâ¼&ïÈÐ\x0008¬N±GdÍ\x0018Ôm]#S\x0018tTøò9x@;ø\x0006\x0002Ô\x0014ÝhDO\x0008í\x0018OËbò\x0001\x001d\x0000:\x0003_R¶] jå9PÜ4©æïÜ¿a±\x0001gÇ`ÍQü°¡7\x001e÷ÕG&ãâ<ä!\x0004õåcêÙ/æï\x000e
]Æòr=Éu¦~nnz\x000cóûø¯èT]û¹ë°AR\x0013ê\x001f°\x00074|E9 \x000eø\x0012ê×­%ó\x0006\x0011o³
%\x0007ý·ï>¿úÍOz¸Õà##\x0001\x0015Îäu\
E¦óÝq½^zoìb\0Í âtÓd,OrSËâlØ°\x000e&\x0007Q¹¤o0­8z\Î\x000c¸ËvQ7JÊ5X\x0007\x000bÞ\x001dFd\x0008p\x000eKí\x00087ªÊÉ/õ ^tM%2kòyøt£¬\Ò@\x001aÌC:è(\x000fK^ÞF£¨\*\x000e²q²3y\x0008É\\x001c­ºï>ªÊ%ÍÃý)HÜÕ¸,+vK)#7ªÊ%%c£ÖYÌ45@×ø$6c,\x0002ëAV.åh!»,kn¼½¾dï%Ûµ\x001bUå^\x0018ÐU­ÈT-Ë<5§T×5­\x0003\x001avou×+\x000ep\x0018ùáYp0ó]ßÍ£`]ÒôzÁUWÚË¬~r^³¼Ü¨V'\x0007\x0010t\x000c3s"æcózDïÛ7³ÄV *"Ð¤PLJ¼1Äe,n
7*
èM¡Ãèÿ×Ïø|³y"~Ñ>Ëè¥ì\x0003¥ö¬jýïm\x0014}(á%ÓDÄCâA"£þÂßÆÊÇÞ³ÀÛêÑó^uºl\x001aå7U§'¹7\x001f©räV\x001f!\x0006õÇÏ?¾½\x001a\x000f4	RG¤OÌRT\x000cùø\x00155¨ZËÝ\x0016{á$\x0019±åøíµ$ÞÒhh7\x001bJi9GæÀÅoÀ\x0005VMdR¶1xÏ\x0006ßFçPÁ
2äs\x0004ø\x0018Ø¹ò\x001d_­ß±¬\x001fnÐRXè\x0013®aï\x0005\x0000äà\x0019y= ñ@yebÔêiÍ\x0017Û	y>\x0006q¬È<=~§
\x0012ÿðt;	Pù\l	;!J/Heµ7óÝEÌ/ì\x0010cÌÎ@\x0013½³üGRM\x000c©\x0002*{¹Ü¯qbvÊK\x0014kÍ¡\x0012½^¹N©#Ì[6Îs\x001cLXÐò8e\x0006eÉjR6#Û8qF}&=¦8îØÁq[³7q '@Æ\x0001:Y¢mfÕi\x0003!!o#·çàvGÎìÁá\x0008r\x001aæ
¡<nÓ:\x0013Çn|wOºòêsCãJ\x000720hà8y\x001e|\x001daý:´c©G­\x000cÄK}¨Vf[¸z\x00033·TÇ¢W\x001aÞñU§u\x000fÃ\x0001
£Ç¼þð-uF&\ï×âý\x0007.\x001cÀ=X\x0003RM%`\x0006\x001a]\x000bu\x001eÐ\x000cÊr|ú
yÕaÓÉ¹:6ÒªÑ!<­\x0017}!Kp ':)È%¶qÜÏÌ%¶i{\\x001dBiÑ !w\x000e-,Òj5Mù³âz¯uÊ\x001b/\x000e¦^Ñ\x001aF\x001c¹D?È3âÏrþó­\x0015ÎPbÍ6ÝË#ín_Ûþ\x0004÷P(º³Kôe:Ún\x0014Ê\x0011\x0017:~)ÖDí\x0011VûUÈ2æâ)\x0011ÇÛÙsQ¡f¢(ÙÂÚå\×5ÌQ§!Ã\x00035A\x000eu\x0004¶k\x0019í\x0003\x0018ª\x0015:Y,\x0003p\x0018ÁC2½\x0018Us G@Æ\x00198)YÃ©îR\x0013#;³\x000eUã8Ë[³-ùWdl3Ð\x0011~@^çF}\pÍ46¢!GFÎKÆÝ\x000c%.tÒ\x0003çÏ-çÏ­»¨èºA-èÁ\x0005;7\x0014È,ç¸­7kq\x001f7û´Ú\x001b$;ã·­,¿(Ðá¢¤;JðÈul^32\x00178ñ¤ÈW÷Ñ #\x0017\x0001ÍÈÍÒT¹	Ã¢Ý¶è«½aao\x0014ìæLª«iÈÔÃ¼YÛ\x000f«KciÊP?MV\x001c\x00077íÖ-nÔË'Pý£¦¡ÖXQ·ÿ²n9 á\x0003Ö\x0002ÄC6C,qGã»¸çÊXZÙÔàÞþôÿ|úð¤³\x001b=\x0018! ÿî©É)ÿ?\x00083tÌd½¿NÀ¤\x0011ÚK®º2TX:Jùu*GÔ\x0012Ø2Þ¯+óe¨°\x0014Õç>\x001d «\x0005Æ\x0012MDB\x000efÙN \x0003]ÇBNF¾xÝÆ+väÚN:ë¢ÈR"KÑ[óÔSkðäåj³s\x0007r\x000fuâ5ËSÆ}fd{q×¡ÌRdö¦Èq°\x0006É\x0016(r\?3 ó]Þ&·\x000e<.êÅ\x0016`³®²¡ÊRÚ\x0018=K+¦9òÄÚ×U2TYÎ1²tg/\x001f|A;,C¥¨bT*´5(¯&÷>/Úµ2ôâ\x001e-C¥¨"P/Xi`6êã[T¡ýZ$ïv\x0000
ºNûñv\x0004\x001dø\x001bú\x000b¼\x0003ºBe&ç\x0018Ò	&\x000fÃ]+ÊPÃ)½=óíêq\x000bç\

wÚ¼õúöß¡ã_ 3\x0007S[Mb9¾\x0007ø\x0018æ´Ö?= \x0013­:9^u%h·ZôÕ9×¨.ÚyZt\x0019ýjÑWG±SBÚ¢syvÑËU_Exè¶¯È\x001e>b\x0018\x0016×d
¹M=\x000cÝÈ¼â¸Xñ"\x001cÚq-àZ2F\x0018æêÐWK¾:Ðä¡K¶\x0008Ë«Î«U_Chñ&uâ¹@{ÇINã
Co£\x0014\x0016ü\x001d:üÅÏ>ÏEMÿ²\x0012É;ñ\x001c
"\x001bb°ºZ1³§¦^ä\x001dÈp\x000cUË Òa\ \x001778MÙïê\x001c:8\x0019¢ðmÑÔWk®E_\x001dC\x0007Ç0,ó¶èLæ é>ºè´ß; á\x0018ê|­Ì.¼èaÍ-
»:\x001e!D\x001d6¦Üaãpg
÷ê\x0018zK+¶V}%²â4¬¸\x001a»:\x001eN¡Ò¦aÑZÄG`ÏÐ\x0000÷\x000edO»Î{Zó°é\x0006ÏÑ¯ #è|gwèÄø@\x000c(GÄtë·¶Yvï\x0000´å\x001c[\x0019£;ÇäÈ¶äº:>ûõ­ýmÍL¶§{«^\x001d@\x000f\x00070\x0018º½÷±Ï\x001d9ÔÁÌ­ùÓ_@\x000f'Ð§×ý\x0000Ê\x0001%n\x0015\x001f+ò\x0006o¾:\x001e\x000e ò\x0017ñ¤l\x0011HvC T8P¸:\x0001O Ã\x0010LÛ\x0014±I\x000f!yQ\x001d®ÐW0À!ÔNyËû\x000e¡e\x0007í7]pu
\x0003Âz7¥¬Z.JÐÉSdàkë\x001b\x000bWÇ0À1Ô¦Á
[ÏSUGl\x001d,ï½íexu\x0010\x0003\x001cD\x0006à\x0001§\x0013\x0010yÑK°[õóê$\x00068rcÃCÙ¥H1©ì½È¼ló¦®Nb\x0018
z\x000f\x0004ÆCN\x000e¯%ÑÂÕA\x000cN\x000b¼À}¨48Ù1i[wúÂÕA\x000c\x0005oÎ2\x0010hù¢ø¬P¿TxÍÛî¸:\x0001N¢V¹ºcòÚOùÓî\x0008µå:âÕIt\x0017bHê=i ·U³AÂ$¿:.\x0011<;²úi¶G\x001cM­»#^mé[:¼®ð\x0011y\x0018¸ ó3\N@ÓjºÚw1cª\x0000Î`9â´¥Cn,xµ?"î\x000f\x000b_0R@êtº$áV>ÑqÀKäö~#Z|°è\x00085>+~x
µè_ Ö\x001f±ýáë"iX;½öó\x0001à\x0002nk¹õ¥éÍ´jM\x0002±Þ"í\x000f_?PÁ°+ðHÞºQ²ç ^\x0007-Ï\x0019âIräýO\x001b·îÏ?èXá[É\x0013â)\x001b\x001eãI*JÕZ²f´)õÞ&-ZêÄ£þü:\x0014uÓ\x001e\x0003bB\x000cqÕmZJ®ºQ~¤
\x0015Ê\x0013xB¦¦é\x0012SX\x0015v£üÈ!/vWù°ûáá»Ûì)³!!\¢=d|%ØµÍkî%\x0014·\x001eº»ÚSÉÄ\x0017î©Â{JÜx\x00016a2Õb>U,ãXiY§n¬7UáM%vÃYlP,ImÎ$~­é®7UáM\x0015T\x0014·3{u¦µÛÈ)òløbüRÇ÷@\x000e\±Ènu\x001d®Y\x001eFÞú§f'»#wyu©=À¦e\x0018AÎäÕr	ëö\x001d¸«ûH£¤¬ÜÅ\x00031\x000edÉ­¥a.wd¡ã@;Y¥­Ñ¤
Ï
)Åúµ*Á\x000e\`É\x001e{
\x001d3ôûñ8°Ò^Ósd¹\x0003w9x_\x0012ò
\L¼äT¹QBÞ!ëYÕ;4\x000cçi2k\x0000-Q\x001aMI-
\x0003Ðv=¬ú@¶°3J«O\x001fÈ\x0012F\x0004ú'3H,uAÛ¡ñ\x0008Â,äRBúmnI©~+h\\x001dAÍÓT|\x0001ZG¯;Ztä/\x0018ÖE\x001d\x0018N`q8On\x0008\x0008"Àlb×òÀ\x00074\x001cÁN\x001d\x0015ÍCX¿#\.(p;2A\x0015\x0014íÈ¶V\x001cB§ÈìêJÞ\x000c}u\x0008a2OU\x0002oÄEÇ\x0013\x000eò0l¤n3è®N!LæÑt\x0017pOâ±1L'Y¶¸\x0016]Ô\x001cvh5b+NÎ³)ó\x0004ìªegç×£yvh\x0018ÍãkÂ±êGyÞ1\x001fõ\x00174\x001d\x001ad9h³h#:î×¼^T\x001dv`<8µ#YW¬KæiB\x0012ßúuÑaGÉ<òÞ[Å\x00193~ÃÄÎ?o¤«\x0008£yÔw7\x0005ÊÜòks¥¢Ã\x000cyä¿\x0000MÊ\x001dâÀGB)Át]tØaböÃcÈQðí¨û³åÍy,\x000e;4^\x0019¦+ÿ÷ã\x00045~Ì:ù·]-§£[
hrÆîa[ãpoñÞ¼i¼E\x0002Q¡Û\x001fÐé\x00058/ò¸³ìÂ\x0010ùî«\x00041ÏewAÌ/[¸Å6Ï[°q¾\1\x0005{stå<¦ÔM´y¥¶ÙñqÄÈ\x0017þ\x000bùú\x001f0ùëÿéõãÝ(ú«¯þ¤,¬oÞþô§÷·ÒP³\x0012'³òëTcqRHØkõ¬»Sþ}aßXt \x001ak»5Ìc-ê ÖÄAHÂ¯\x001b×\x000eàÎ46Þ*:\x000e\x000fS¿V)H¼]+Ó8;µOßÒÀýÖÁë´W¼u¾LÿÀíDc\x0013\x001dÒIC!C8jo\x0017C¥ÈÙ\x0001\x000bsi\x0013\x000e\x001ciI?B³¬U¿ù,B;\x0013QÃ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-09.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-09.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=|¼¹\x0003\x000bÿrÿpö§Ëû³ïHÛÓ{"ÿÊ(QÉ¯R.óëËe mõTW»+öúê\x000fn/ÿ*¥òà?|fÙG?yÿÏ»«÷ÁC\x001aä{yu5Î,¤âI\x001e\x000bxTÑºÅUärÕÆ¤ÊÙ¬Râð§ß*'¾\x0001iÝ­u\x001fýæa\x0007>Ew÷p?3yn><ìÏOäs9¥e}\x0018så§Euã\x0015y0«yR«·ø«dp~kÕG¿x\x0010ÿ[\x00139$è·»³¿pgÑ¤.\x0006w©¢·Ëò\x0013=T­FÈØº2ößOè¹0§¾74«pÊ©o\x0011D_l[7\x001b?øÞ\x001a$L¡Oö¤/õ{
àmO¶B(L¯\x0013\x0010\SÊabJ]_[óiz£Æ±Btà8EgËz³Æë8£M\x000b:æJ=ò\x001bÛ\x0007ìª\x001dÕ\x0002v.Y1Æ\x000b\x000c\x0012~²6¢ÍÜT®!:\x0002àa\x0005\x000f&`·ÜÒºkÙT¤Ü$\x001a¨..õÞNöõï»÷»Û×oOtis´2\x0019óº¹¼m\x001bTèÚþ¾ú[Õ'íªüã\x001f>³ì£<lßß½±à¯ÆÚÕîìoä£*@åøïàj*ÅêáÑM\x0011-\x0012J*YÔ§\x000fö;PåTâm\x00076Ö}ìG[áæ\x0007aú\x001bÀá©ý¤Vçþ¹
XÉOVKZbS!¥ #_<±«Ò«¶*¢âª´Tû|ÙG¿xý|µ¿¹l²ÿ\x000cäS\x0005\x0004éFF'ÍÒÂ!ýï	á>'z'ó*\x001aYM²µê£_<\x0008ýÖÿô\x0003÷ð¤q(ßÕ@àÖÉP]Wê'âWzÂc ªJ¦\x000fDÍ}ô\x0007_ÄÛ\x001f,¸5\x0000uV+O\x0015\x0012¼n\x001cq«aÌ-°0~PÿøâPUD}\x001cj¾ì£<\x0008ÿãÕ¯\x0017¯ßA\x001cêÔn¸Å\x0016|vICZ_(nO
àÎÖÃôÜð*Þ
¯ûè7æææ\x0013Ú65ávº[µKdlû5så\x0015ð]Y¦É_§Xð7gÜªtúÛ|ÝG¿y|V­ú\x0018~D¹ÐI2\x0002ÖúkÉ$H\x001a*Íµ©p='S¦¦7eæë>úÍÐ³ÓW\x0017PWqòì&v7ÑÆg·Äú¸/\x0011¢Æ¹îüCv³
gÈnN}ôG\x001dsq=\x000fÝ4©\x0019¬«s¥³nÉ\x000e¦\x0012¥YÖ\x001fMÉ<§¬fÎÕ®ûè7esö»x\x0000¹2\x000e$ºÙ­nªç¦?\x0018\x0003ês×[òäa *>\x000c\x00142\x0016Af\x001b_`P5gÁ¸ÅS.'\x0004\x0002\x001b¢@Ö¡Ä,6@7è´ÎlYY7ÙÍO×\x000fo_¿ÅÝ<mÜvÓYuóÄbt¥Hv©ñÑµså\x0019ÅÉlú8ù|ÕG¿xº½üÙ£îµ|AAXJ2ü´\x0018G©Ì<2åÔ7wÿ~\x0014Nû	ÃVìe^%Szu¡L9ßÀ\x0013Ë\x001as\x0013\JÜÕ{S¦|÷\x0006o\x0003OPÕj\x0015Pµ:e\x0008%q½y\x0014J1ÛÊá>Ô¯è\x001aëÂ\x001d©³\P¨EÏC_Í\x0010k\x0019´Ù\x00146 0[\x001f6
×´äU>ôë+ñ\x001bºkøQ'`Òµã>¸öä½\x0014ûX8l£\x0007¬ó\x000fXbæÙ\x0014
2}a»­^ýS·¢\x001bècq	fÈÚ@Ï81^N(*{6Ð^]`ýÔ·K`ödÙ$;\x000eL+\SÖ\x0003u¡SñÔ1I`ÅÓ\x0007f§Ë>öÁc\x0015ÃEüá=öÕío?Þ\]Ê!§KT©k£ÔmÊ¤ÜÛQ­bAz4XÁ
EÊC±f
k0Û´@n$Ì6j3Ù\x0011¼nJÂýdûF\x001f@n><a.\x00038³Ö\x0008ð,	Ày2u¹£½\x0001³¢ÖWEÿÚcÏV"A{e«ÅÄ=U&ã
Uv\x001fï>Ü÷uâô\x0015ýVYiL:Ô¬Ö]ôX%\x0018ôSgú;Z¥Ó§¯æË>úÉcþPòâ ÝKú\x0013\x001dÏ×íà{ÈDXnî2_Ç\x000f#¡ÅÏÎå±#a(\x001c¢l]
8ÀÓ'&t¶Ì¬/t \x000c%dr<H#w5Û·	\x000b[ÿ\x000e¡3æ;}\x0012\x0013\x0006\x00089vÝmQ»\x0000ì`É	^>¥nÉ%Ànd"\x0005ä\x0016Ù¡¿
c­Èv1¢C,ëÜuUÛb]ôzkEn­	d0nÐ\x0014»5[Û-yÒ¯¹â¶¶\x0014±ÅÏËå*g:AèÉ ¡\x000bý<´@ÉÍÓbó¼é\x0016<kz\x001c\x0018Y7oßÑ;ëL\¡áEËÈIï½FÊgÞ<#7ÏÔAjÃ¤F\7ð'óC¯aCm»Å$¦\x000eAævlP(\x000e\x0014ÊwgßìÞ¬ØÒ&+Z]x)M\x0001\x001aºã\x001e}ôµ\x000cÖD=i\x001f·ââæË±kÇ1¹Ü9¯u®ß¨¥¼í´\x0014Ï\x0019Ð¬¤[D6\x000fÅ\x0013Èºè¿ñ8zÛ©)fJ×I\!HFÑÅÈ@>éz\x001c\x0019\x0008È­ý[ç:<m=N?\x0018-\x001b
²)4ò½ñ¶"7ÓM\x0007à¡+3 \x0003¤cß}«Ç4\x000eáÁ\x0001ÿ\x000b3ÒîÏè©?UBªà\x0014­nNy\x0016}ÚÊ|­"V§?ÏG[%Ó=ìQ[àí/½Ô\x000e%N'»S)elüxcrcè¦A3\ñ\x0005'Cr©Ó³ãM\x0000\x0006æ\x0011r\x0016°û[ËîïäºÃWB\x0013ã}Éý}ÆÁ\x0018%²D\x000c©Nh|qJ\x0007ÿøª\x001f½1\x001a"A¡£°zþ¤g9Ñ\x0019XdË	û}X|Ï
`\x0014Äx½s½£Lt°\x0015\x0012mìJ\x0008ÒÜZÈrT\x0018]\x0010\x001eî\x000cO$\x0019%^Äfl\x0017\x001233v\x00158ÃE\x001eÉVØ;ÛÙ7¦\x0006¬FK¤B#³CÖÀ;OÐVø{)mÀ¨)³Ã

OE`jµÞyI-B¯\x0014´6Sn\x0015\x001a"xI\x000b³Úidmæ\x0018[GÏS®õÀì°"\x0011ñÏ8Ô\x0015
RÁX¢_È%')hU\x0008b´Ã\x000c¹Úáv!\x0005Ø+.a:D\x001c·.n%Á]#­M=î)WÞ­Ët\x0011ô~7ö'ËdP\x001eéÌËÈé0B\x0007èv]\x0002]i4:ê¸a\x001e/åÆ±\x0004
Ú´ëBº(¡ë\x001d8ÒdÿØqÈ: \x00037Ñüu=ö0sÌ\x0000¹]R$Õ,%òZDÃ|
ÎIq(=\x0019ß\x000eÐÀL$Ó]ôJí\x0011½'/Cm¶®ëb\x001c>°.\x00113%\x0014m%t=d¶\x000eµC­Xu\x0012¥Ú|_¤bJÕÃ5[GÏÀÑ#Ó\x0019"	®O\x0016GO\x000c=çS]\;»u@,\x001c\x0010ÒL¶ä,¦èFZv£%WNÝÚF\x000bd6ÙÁ´Bvý]\x0017½½\x0005zk\x001b-r@)\x0001íqÈoY´< &\x0014Ø­]´ÀÒD\x0016¿Â«èä.Ü\x001dòÚ\x000e1Ö\x0015\x0019¨8#\x0007k¶	çÇ\x0010rÞé0)hk\x0013\x001dp\x001d\x0005)s§\x0010G\x0008Ò
¹</f·i¾Ú	ËÑÂ{;¾£T¢t"
RnÌÔC_´ðÐY\x0000Y3ÕÓEM\x0012åòËpAí·öâ7<ÆJ\x001d<$í¡Ý£ ß]îßì?^îO°H1v\x0011A·Vo\x000cÔ¹Ì\x000cU®í×ðÿ¥û­òéü¤ÀÓ\x0000Ç+\x000e|Ì½\x0011Xçøl\x0001¡\x0016Hä:¦\x001cì\x0007Ó!q6\x001d ÃÓÃ\x0014½tÁ5rç%éiXauÂ²ÌQØðZfo»(WÑá­À \x0008$#Ë\x001d«W\x001abãØ\x001b\x0000\x000eB\x0010ÈÄHÈ)KYtÈ¥]mÐ°\x000b2¼bÔ\x0002¹`\x0006'W3²î\°Év@\x0006O)(!eB\x0016ÁdTÈ\x00067ó\x0016`x½/y\x0013pø³8\x0018±/\x001cH~ê)\x001d ÑSr\x0011¦\x0005ä7\x000b=¿Y:J\x000b2Ü>¯D(+&IÝ\x0017£îM
4oÝ?tÈªL2ÿ \x0005íSÙÌ\x0007h¸äÀ s$y\x001dÌ0¨.\x0004ÂÔUZ ½0+\x0013¨Pá*IÍúÈ{õw·nKObäÄ\x0003$t\x0017£ÝúJ\x000b4\\x0017¡¼¡H
d×\x0001§©§´àÂe1\x0011÷íÀ -a+	5z3\x0007då\x001eê\x0005\x0002ÇNí[i¬æ0\x000b¸k\x000fs1\x001aÉ{å8QÊ·\x0004¥i¡Ö>cr²Lé?=|5¶ð²}\x0017·Òþ\x00177t/®Ó\x0011mLVT	5×ÝK;N(\x0004\ä«(@wêb\x0017'²v\x001aÇ_`Ûe·\x000e)¬é\dY\x0018d³\oRz\x001a\!Ow]ÇdMóÕS!\x0006U¯\x0016	ÝûÈ5OHè\K÷\x0006\x0002.6g©Dl¾\x0018Ëüî\x000e	Ýkx:cSOÆ{\x0011$2Iz\x001eÁ\x0015òÏ\x0012	ÝkØ¨$y\x001bùîâanÓXÛk¸éj£Ès\x0006H.ù0~¢B÷âä_4dëºR7kdî<\x001a5O.ÈÀìBö\x0007\x0014èpMBhÓQycâ¦iÒ\x0005Ú<"ÿdÏ¾\x0008b\x0007eb x·õtîé26#{µñ\x001dÃ¯25\x0010\x0007ã\x0016èv:\x000cG`Ñäñ
md¬|ËéIâ\x0003\x001dî÷··å\x0015ÿðnùú²Û=·ü×ÿü\x000fÒÜ¿Ê³KJ\x0006¥}n\x000c±1ÃD¿òÂ¥Ä®Nê³£p«|zÇ¼OQh\x0010»î
:½\x001a\x00072\x00022XägH£Ä
k8wÝ`æ]Û'ªØ\x0017Q	cH_´bØ©Ö^ÁôËB·²¹£E®Ê()\x000b2è'g0ÀDuDóv\x000fïv¿îNÓ<J\x000fµÅä\x0019¨ËL\x0015N|;(ñpÊ×Ú¥¯\x0012_0jR\x00109\x001eÃ û<l\x0016qâ¨µ\x000cëÐa\x0011õ*LÍ\x0005\x0018ê«8æ\x0015\x00018J'`WiçõUAw\x0016Odþj,ã\x000e2MH¿¬V®	Óñ\x001f¡ÀJx|4Z\x0014+%®\x0001\x0013ÈÑÎhñWdÈæô\x0002½¸9|·%nyÇPkÐU\x0012¹`>Cws²ì¯P!iÊô`Å\x0006\x0008¦hÉ¹²3RÊ©\x0011\x001b¸\x0007äf¸4ÁG\x0000\x0014¡wQ\x0012cÊâ3&*4Ø%1+QË
Dÿ?sï¶d×qd	þ
ï\x0016÷Ëc5UÝeÒZR÷+ìH\x0002I%\x00002\x0001ð"³úyÿè\x001fðsv¬å±wR\x0005\x001c&ÔVme%+ãøöððËrw>´am.Ùî×LÏÐó¢4Ç\x0003gì\\x0018Ú»ÂýCíwîW6ÏÐS¡­+¸ÒËI\x0019\x0008ßxkùªÄ^\x0005Úa³k\x001eµfûUÂ3tùÌCïTÅ\x00062VÅÚc\x000eæ¦Â=hJ\x001ewj¹ÁòYz@6è)\x0012^paj7u\x000cÝbG\x0017ÜAà°ÜÔLKÚÒ\x0012IãÏ^»¿(\x001f%àûbå9]»+zRÆ§¿àwyÈ\x001f¤ì¶}¸?]ç¬Ú"mÓ¸Í¶h¦\x000b\x0012\\x000fµâ¬½á·_È%\x0003_¤ð-\x0003
CR­baw\x0013ðfIÀ7Á2j¶±Ó=&p¥Ef
¸'´w¨}:\x0001ßT\x0001{²·Ìf\x0013.3[A··fC\x00072pãú[m:[Ô£°ÏUZð¢
P~Ë~¼ñ\x0013ÙxõÜô	`ëÍ\²ðMý`aÝ\x0000êÌE½	=ÿ·CGÔYøâ,\x0006;=4#+àäËîÛ»$áef\x00106ª5Ù ï$Do2Ûæ¯´dáÔ'°Vb7Ó¼Úvw}/úì<½K\x0012¾¹"¸,Ç¬_cè±
içé]²ðµI\x0016bàb
\x0013Û\x0017#÷ÉFÀÊ^²ðµÝf\x0013\x0000zé\x0007b_Ä¾³zçU_²ðÕWê×¡ffßþ0»"6÷5H;¯ú\x0019\x0019øÞÍËõ\x0016-"'êOmÿbfy\x0018»OZòû2I\x0017²\x0001¥¹èåT\x001b3=2¶Z»ÏZòûÍ\x0000cÒO.<²\x0002\x001a4;ÁíZÖ}.Îï7ã``\x001a§¤hoèÐUÙì'øNð\x001f½W¾uûT¨3ôv\x0013«ÍÎìÆ¶
:\x0018u\x0015s< BéâA5 ÓÍüS§«ûEÜñÌÎÀsÆÅëÜ\\x0010<²Oõ.÷À=\x001fç"kôqª,·Mø!

K RîTã?à\x000c9Qb²wz¹òâCÝ>ûÓéîþõµú\x0018*\x000f5µm;L·,pIû
Ô'Ê3üC\x001bþÌX\x0019JNTtf0äì´G8©85¸ý>®¬Ý¨\x00141}<\x0017¬«Ñ¥²\x001aö;$,¯»\x0016¤"·WØÉÕPÒ\x0016]¹ýF®ÌndÜz°4Û}ô¤æÂ=Ã#K§ú~\x001fWÖ^T¤9`IbVr\x001claÇa\x000cÈÝéãÊìEU)WG8r{Þ¡°\x0012úg\x000e£d³\x001aï3r&g\x0007JÊÍàBkqv²:³ÛO4+=î°Ñ/µÝó;iù\x0003pà\x000ch}	9¡ÂÇH\x0004tÇüî\x0002»
\x0019Ü\x0006\x0019
güâ\x0012X\x001a#!·ó¶ãW¿a6\x001e59û\x000fð\x0019z~ÃZ¹fZ×Û^à¬x\x0012£oîè#Â;Ù,8\x0011Râø\x0011ð&dÎ:\x000föíÑ7¼Þæ¯\x0013yzCV¤<;:P¾á$ß¶O\x0018)QÞB;ln©®ÐT¸ZjOÁïoÏÐÛG¬Ò\x0004QcûflH«ãzPv\x001d\x0006Õä\x000b\ÿå§fÌG/^8OZ¼V7ô¶ºmÙSÉ% ë?TjºJþGR\x0001MH:Y\x001eò
Ø¨M)üµ0m\x001bp\x0006¥\x001cfr\x0016Þ-#Ë.=à\x000cÉòdéy\x0014:!eDMä4¼ó»¹\x000b2ä\x0002¢\x0002u&¡öSþ"\x0017Nj»]rÀ\x00197Ò¡ÙT38«2Úaÿ¡¹\x0000C®¼Zjäo2§Ï·d´}ç­ïðÄ\x000646ÔÈe|w\x0015/¹=áÊU8"s¡Á\x000bi±
@÷æ+RÈ>±´½ìÆö²~ÿúîþÍí
cMØ\¦\x0010¶þDÉ
@-ÈÉAh\x0002ÜÁ8²5åªÓ~Í7\x0000·ÄÂ·-îeºw)íWÆÖÄ£f´T\x0010R#½\x000e5Ùuve{\x0016ÁÿÏ§»g¾½êX¬ªj®ÙÍ=)Ý$p$ÜÍÜ©þ%æb-³	G}ÎT=5-ÖØ»§ Ä¬ÚBc'È/\x0017ô\x000clËö9ËÔK!¿ìNe¸ \x0003ÙRæëpY\x0019Új\x0018V*»ôá\x000b0ð!\x0013½cÖª~jõ§ßs¸/¸ÜÞ\x0005éáÞýFÇ\x001aPÃ¾=C#\x00139¾²/;ér\x0003Ë`â\x001e}@¤ËúJbvó*9&\x0016GÉ»\x0015 [þéþôí(¬¼>½}w÷ööÙÞ}¼½\x001aå2ÛÌlÁ\x0014æÝ4\x001cLí½x¢Õ.ÿèå4\x000bå2Yúh¢âç:59-ý!/\x000bçR6_C)Q,\x0015sû\x0015¥(]·Ê,¬KY`NÀ¹§
 «\x001c\x000fJ,u)¬\x001aâÂx6'©VEßñ»}\x000efa]Êq¸»­V+ßO\x000e,¬ËOÆ^\x0016=éËù)Ð;\x0019;¿w9¦~¸ÒxsY-ïÙ1õ3c'\x0001qtAqýÿügb\x0006Ù &Å½D\x0016\x0017ó2Í§Sµb÷ëgdü¦\x0013\x0011+ÙWõþäý*â\x00199Òå"\x000cM¤W>)bq-\x0007³	ÎÈðd\x001a-|ì¹]R­7(=ÚIpxõhJ»
®Ç	\x0016'ÈÔJ\x000eýÒAÿ@7Ssz*\x000b3\x0001[\x0004Ä\x001a;X©GrTÒ¥ùjK%f;4GâÖ\x001côµ¡¡y4²\x000f\x0011Tø¢ÿÎ©µ#IC÷¹ìJu[£¤õ®ý¿\ç\Rö{(2Kß\x0010ùôÉ)pñññiÐ\x000e=\x001c\x0012­\x000btídëvë3ôg+õN»õ\x0019\x001ad\x001d-æ©zó\x001e7¤f>µwe¿Ýz@C»µÌg\x0000þX\x0012\x0006#}ÅÈ\x001cÐÓ;ÝÖgdè¶Î|§8Y²ãXÛwÃ´Óm}¯+,!ë¶tc\x000e½´µÓn}ÆvkêB9\x0019ºÝ\x0013\x0004;Ã[ÏõeýBþéáôòZ{J\x000b©T¼R7¯µál^Oê¹¥&¯Õ\x0006
Ì	\x0019}v\x0001ÑlãsÙ\x001fatFFî¬\x0003ªWG&óZ\x001aËnoî\x0005\x0019³I"÷1îàúØË\x001btåÉ\x0015lH>ó[S\x001a7Tóþh®32PVdÐi&\x001fÞ\x0015BVSrÜÏ­¡1·Ö\x0002Tl\x001bh\x001f.eÍª»:ô<ýÞ\x000b\x0019Ô\x000bYì\x0018!¶A®Ð\x0000­@\x0006Swn¥$Ï·ûãéý³Ò\ñ÷«-}ÿ¶ÉóEF©ÀÛfÓH£þ\x00135ñÉ4\x0004¾1\x0006l&}Å¦ÁP}N::l½N§êcóVáõqB{¢çØr³qJ½õzÕF§\x0013I²A\x000b^\x001f+Ù\x0013~×\x00088:·Okw:S\x001f[\x000c	ºèdi9\x0002«y>)\x001cNPEKtk#\x001c\x0016BVOÂx×ò<#J\x0019*\x0003l[
÷®ÅÂÁG,u1ïtî«Ï9ìRÔX­¨fîxë÷\x000bÙc\x0011Ç¦¨§¨óû\x0017Ó\x0018ô\x0005ñ\x00150\x0000ÐÁp$\x001aÎ~Åàý>-ë\x000c
>×Ý.ÐçàÈ\x001bìãyøÕ<!\x001e<
ó\x0011ò9\x0005ÑñÚÉp\x001eA´2\x00064´Gûv½¡cR!jF\x0017\x000c9\x001fÌd:CcnçÆUétDyÊµé!äî¨ñàQ-ÖâT\x0008/a6ÝFÖ\x0012Ã#ú÷\x0008~ax­@ °YÉ\x0008jÛjÌ;«Ù¥@õÕÒ:.<ñû\x0017\x001f¯U\x001cv³	\x001bÇcÂ\x0014AûO09\x0015¾ªÒöûàÌþÞÒ¼Q#rÎÿýÝ\x000fí\x0017\ë½ÏAeã6Õ_oø¨ùÉ\x0016ÍüÅº&"«ÂÒ@{79Et9Ã\x001fÔuÍ2ÿ£=öÀ<4\x001e9z\x001eYw\x0010×O\x001aâzúø÷?Ü½ºÖ?\x0019\x0001Ea^Ú²!%ôÍ[\x0010Û¡¢öØ&!õE~R?@ªÔ\x000fÐ~-Æ\x0013ÖØ}¦EÐÅW\x0005ôW)ÐKª*õòï2-îºÙl©n×\x001d\x000b5j´âùeØ\x0006
\x0013Ä>	|UÄ¼\x0013Ãºü?/Þß>ütúðîîj«\x0008|P\x000c\x0017¬¶tPq\x0013~ú'31YE\x0014ÕTr9Jâñ¿Õ\x001bVHgz·ÇªYE\x0014ÕÊèmØzØÈÈ $\x0016dÝëÀo®ìùëÃéÅíû÷×¯\x001eùg>¶éÒ¡ÑZÊ:/»\x001d}©ýº¢ÌÁþ\x001fýµ{ì\x001a¿þã3[[¤þð¾ýïä®t§\¬*ìÜ¦ Úþ}þ§«û&]bjf¹ÛÌ\x0017¨¶\x0006/ûÍugäy§d!,ææåU¥NyÁµìÓ=.ÈÀíä)Ir\x0004éÊN\x0000mÚ¯üÃçyÓ*U	\x0002`\x0012Lª÷¡\x0007«j*-TÝï?We1i­¡4&J
^q\x00009\x000c.ß\x001aB¬äáä®\x00121²z§5$î\P\x001bÖòïÙÿjÚúáj\x0003Jbúø²M(ñ¸È&jê\x0017\~´º\x001dúz\x001eùÑß»ó0Yt:Z@óÓ]ûIÏþåj\x001b®e \x001d'S}J340´ÚFâá'
³¿¥l%;Ù¬\x0016,ÞW©¶Ò
\x0016Ñ¨Yy××¸ ãÔA*\x000b·7ªÑý#\x0015¸\x0018¯\x000b0ÌNA\oSn\x000c!kªMØ©B}Ý|¦©+¸»ýøì_ï>\x000cyö§Ûë,+\x000eÖ:¦Ð\x0018)DÉæ\\x0003\x0002j`éæi^Ñ#Ï´è\x0012É&$©8K¤\x001dZ~ÆÜ#\x0018m¥=í\x0007óèÄæÿçÞÞ¹3ôÜ:'ò(àö:ÙB\x0000\x001b´ç\x001dí,+ÿækª.N\x000fé§k¹¥Ñ*¶j_8vÉCflàBVø¢û§Ýò}1
H\x000eS¾û§~ô\x0017ï\x0019ß£ÔÃ÷DFÏsÈíËkÆi\x0004«ç_"¹ìð4Oß?~hRRÑqÈ`¥\x0001»²2'\x0014\x0016¿¸ OÏÔ9o\x000bCt\x000eIUóì¼\x0012wk»\x0017d\x000fgÎX?]ËÔü\x0017=W3Ëà ¬|a«\x0006\x001dÔö/ê3ãP¾,{¦¹ìõ òJl¾ö\x001f§×k7j¯Nl&\x0005ÏG\Æò¼"-D¾ªb¦@m%&(ê\x001aJæ®ñÑqoÓ\x0005y-4Y"º¸¢ÒÃ#Wu\x0004\x000cEÌ&fÜ9$Ã\x001c+\x001eÀYjÙ¦}AªhxKK»¡
U4/å¼æn§°÷^¢N\x0005=Ý_«{BæLñRh7{hÓèC½ÜÓ4\x0002ÿDÙ¯&$e\x000f9Ç¢@HêéUR\x0013ô{ÃÑ\x001e:ÕeÝç \x0000ßYÑÄ`#¿,Ò±~Ö¼S¯\x001a©Íÿ«	ãôòZ¡FJñÑM\x0013Sg^\x0012Lüx¢ý\x0002ÿ`¨atZ³ÈÜñY´jî>O¦K*÷èÇ¸ÕÕÂè¬¦$è1³Ö^Hf'¦çMÙ_\x0017:L­¡fA\x0015P\x000b\x000féóÉ¯e¶¯GGG\x001a÷·²òì!}ÓÔåZîQ.LÒÛVÊJ»×}ªrÛ¾wº\x0006\x0005VM3<8òc?vo8ù:­ó÷¡6\x0015¦áÅ"WåìdW¢íZiò{"×4»ú\x000f5!G=±3ÆvEa^t{pùíN¼ }åýÚXÔ#;;Oh¾°¾]Y"¶\x0017SÙõ
.ÈLmÇ\x00165ÞD¢¨z6òÑÙ]nÓ\x0005\x0019¹M4XDf^\x0013\x0013¤¹6\x0014&5\x000f)îö!\x0015¹i>ÓFÈÑD![ÈMnwâ\x0005\x0019(7ûZ÷¨Æî¶8G=\x000e4ÐrWå­1ðÛ°{ä¦\x000b2\x0002RÅmbf\x0013o\x0005i¬P8ú~Äl"\x0012m\x000b$N×¼>ú~ñ¼aãHÌÄl¢)óFÖrSÍ4q7bûSqÚtVÔ¦y\x0007MJÎË±!ms;£Õí\x001eµi
º@¬Ô¦Nw]©M\x0017h¦6Í'ÙÕâ¸µSéç	.{¹úÍt(bé9¿ù\x0008jÍF2´Döäñ³à¦Ù|óñíÝ·w?îÅèâ;¡ÆË#Ð¼Q1Ñó\x0005ØÀ~£Zç\x0016\x0017[\{&­ßÝ¦cstk\x000bWwkåOüð±ýGwò_*{¾à\x001fx\x0000Øà[é\x000fã_û¼¼ûñôýGðCnýï»ûûÓ«Åí¸¾}î±·Oæ¸7¯*â/³Æâs»\x001dÕ\x001c¶4/ÜÐjñ;Á£/îñï"\x001a|úÌ\x0003ó\x001buNÎÜ"Â\x0002\x001f2[;\x001bäçÚ[ÒÂ1vØi^\x000eÁn\x0000.!vDÙ®øò\x0010vüÜs§cì4±)òpîbf¦ªc9+²;ö%4ù\x0018;Oì8gÔ	v,Ó\x0016ul7-hÇöyåÊ\x0012vØs¨\x001bv±~vOtì2í\Ç.k?\x001dAW\x0010wØøNrláÞ³¸SbX·N¹DðËË4F"\x0016\x0010·tÙ!\x0012Ç7®³¿í±z[Pï8{]\x0005»\x0016ÍÒ>óØÜ1¶\x0003õ\x001e;).â6vìØ>±zç¼3èÀý\x0004ÏyÖ¿¥ÝªJ\x001d;ÎùãSÆFCÂw§Ú\x0010¸`\x0017PmàÎ\x0018úÎ¤\x001dê3ÃåÉÀ.\x0012·qñ\x001a¾z¾]\x000bíñí±ùso½=¾>v^\Ó6=©ËDôØ-?¬\x000fëà±\x000fÔ³Ç\x0017ÈÎ\x000b$\x0017ÝÃÁÍ
ÞÌ¦VdQL\x0019L§ãëãàú´{&¶LÊ)¨ãÍÝK
|mÁ$l¸?6÷PhÃ®={:±KPÐuõ\x0008{Þ,{­3<\x000f¹Xvî¥\x0019ÏÃªy|Ü¼?9O\x0006X\x0007\x0003<*ð^uÇ\x000f\x000b\x0000n¶t£Ë\x0005B5l
ßN\x001bv\x0013ø¼@¹é]'?{\x001e\x0006¸ã\x0007³³\x000bÀç\x0005\x0012!W8y(ô´µï[´Ì;=èø\x00029¸@íÝ,\x0001N\x001efF³\x0017¶ãcÌ;¾?\x000eî\x000cl\x0006©d;¿ÆÁmfðþnúã\x001bä
\x001c<jMô\x000eî\x0019ÜÅÎZ\x0002W(K³\x001dØ¬`ÈÚ¦
{Ê²AdÇwÈÃ\x001dAAàq:RÄT£ÒrÓÇ8ûã+äá
Å´Í§ìZ\x000e\x0004Ù®¦ò÷\x001c¯?¾B\x001e®°\x0004áa\x0001N$\x0015`\x000fðî\x001búã\x0007ÎG\x0000\x0014ªóåO\x0004\x001eù
ÁÑ\x0002~|?=ÜÏ\x0016¦\x0004&ÑÎ)Ãg±IÌ}b?¾~^O¡Y8xN~pÏïõüå¯§ëiÂå'<èW¢wK\x001fßN_áÜÌñ³Uu;\x0014\x0006ï\x0017(\x001cßÎ`XÇA(¦Î\x0018{|MvÇÛ£/Ö6\x001c_ 0/lªØ2EÄàÁKU\x0007OÝ\x0015
Ç\x0017(xÀ6è|¦êæ×\x0001îR\x0015Á>¾?aÞ\x001f¡\x0005\x0016Ä6³ÆÓb\x0003\x000b¥Ãp|}B¯é¶q-cÅ\x0013}MOqD³v}Jïñõ	p}LÙ\x0008ª]â¼ö5-ûcâu8¾?\x00017ÙÌU\x0008\x0012\x001cßÍÔMm8¾>a^T
¹-*ô\x000eÁ]Ê\x000cÞ³¢Ç*\x001eQÅË¶TæèuK>(ì\x001e)\x001f?@Ñ28Ù«\x001c\x0019¿f\x001eØÇ×'Âõg\x0019¾¦ÁOY²Cd'½ï||y"¼>2´\x0017Ì,¦¾Æ·¬,\x0012ß¹ÇãÛ\x0013ùõ	 á.ÏÿY&¬vð¯Oë\x0013·R`·?\x001dÝz®Z\x0004ß\x000f~|{b\x0002ya£\x001b¸ÛvÈ\x000b\x001fÜt<\x001eß\x0008¯O{\x000b\x0018Cç\x000eÊ\x000e(õ%{#»T¯O×':R'\x0015Ï*ælNN×ãç'sg `\x000bÏ°õóã:÷"\x001d«xrä¿\x0005¸÷\x0016f\x000fÿ-D\x0016ywöÓ±"&PD\x00137\x001aPWDXÉÙÛ\x001er¦c=Là\x00059CîxóÎ\x001d»X*ýfûÅOÇÐ×Ô)\x0007¥ædÅQ½®õ0\x0015÷³_¸{µ~\x0012_;^8Õ½·t¬	ÔP&\x0002 Ç\(qÝ¾fRéÝ>Z2\x001dëaâ ÅÀÁM«OFâX*c®P>~#2¼\x0011!lóÑGOÈü-M±\x001dùøÈð@D/pÔ)e\x000c?ÖtS¯Oë#¤\x0005\x0010Iì)JÀVÏ}\x0019\x00137ßA¾£ÐÊéãÌ5}k>¾\x0019®f¬A¨ä\x0005eÜU0qòã»!}m\x00039\x0013µv¶1äUN\x0008õ\x0014óñÝÌkwÓ\x0002x®ä\x001bæö+µ7ÑåørfHÁµwÙ;'Ud`+;únå||93$°e2!ä\x000eeN3K¥(-ï¦¶\x001cß\x0002÷G¦@Vò
9#\x0014ûå,ÇW¨XÒÄ"\x000f*(ôo~\x000f
Ëñ
*pRÄt­`[³
»\x000f+ÇW¨À\x0015ò\x0001k\x001dÍ;¡§SR\x001f,@(Ç7¨@ýçÓ²µåø\x0006\x0015¸A©lCGzÙÎÕ\x000b#Ï¬°;{®\x001c_ 9ì9Àc'­m´êè\x0005ãr|J&p)¸D/P\x00037\\x0018)¸r|
Ü Ð?7ßSÝÀ[\x0006·cyéñóV°\x0008èäÞ©-Ê¡ès<¬9Tsk (|?­»á'Î\x0019åÚ'\x001d\x001fê¢µ í¡\x001cBñ½sÞ¡Ê	¾8i\x001c×S¬EG«läñ~C\x0011Yâ(h-ºY^¸&rK ênvn<.§Xé¦xèî{òT¼]þ^ð8.KX(K¤Æ6M6G6±í%¦ãª¥ª\x0004\x000bÜ\x0018
ßÚ;\x0011Ù%\x001fK­ìq]Âb]"\x001brmkÕ^Ef{;v=ÚãÂÅÂDà\x000c^"?\x0019aÃË»è¸2a±2\x00118uã\x001c\x001f5Ð½JRØ~¬è\x000eln
»\x0011»HÅTè³\x0000³h3ü\x00162ü¸Ýúìµð\x0015ÍÊÅ=3¢³¶\x0016²¶âZd\x0010LqsçPª\x0004Ó	bö8ok1oÛ\x000cæEö\x0000Q¨å¼2\x0002CÝÃ±º©îµ=yª{ñâòö×Ø\x0013ug\x0013s\x0001µ\x0001ÕÝoººgRðr^\x0013js\x0016rR5¯Ú}\x0019psf.Å¨©\x001e§û,¦û=\x0011}Q«Ð4ÌÀqÚÌbÚLæÏBTdÓç³:éö8\x0001e!\x0001%+X2\x0016²V\x0018õj¸8Æ$\x001e\x000b\x001d2PÕXL\x000eËÛG\x001e£-Ì\x001epc=N\x0013Ù\x000eA·®[Ç´\x001eõIË°1Çy"\x000by"Y\x00011Lbi/GT\x0001ã\x0018|~)²)*0\x0019ºÓ*ÒÜÖÚÏT¨;àÅæ\x0008\x001dÀ÷IK0¿\x0012²óg
º¼Ú\x0015²¼xðü\x0005Ä^

ÒjL!iÊZáûèrz\x000cÿ\x0004!RÅJ0 8þJ\z6])c8\x0001á?1ëê\x001eÁw/\x000bI\x0008¿ÞP¢N¹\x001cçåcö\x0018ÝY@/6r¤d)¹Ó^\x0010«Þ'Ýµë÷î!½\x000bìÄÓ³;=¼úx%rbô}b\x0004ÃùøQÈÖi;~»\x0008¡§ª~wrbsü\x001e+ßèg{È¦\x0007\x0005Û³ÝB!\x000b\x0016¾9 jÐ%²ÿÛ~ñ \x001c\x001bmÉ\x0000=Oô\x00164FIåüQj\x000c2\x0012²SÏ¶d^&º7Ö&¿'%½{ÒööS{¦Ñ.D	îàèry\x0008<TVÊà]ÙíBä\x0000p<9ÑÆÑ-\x001d=ìÜ$mÇðN;öérOú®Ò\x001f8}Þ\x001fÐÕÿð&¤¾Z&\x0007õy'×¹²Â¸Q\x0019\x0016;	Å-àÆ"o\x0019Ó?ÿ;Û\x0002ÿ\x0016xÈGñk\x0001¡¸dÌë¨ÚJu\x001c6a/\x0019)½.¤\x0003¬Äd©3³(uÏ´{þKýÙ^ªúñÙ×·\x000f¯nö¨O¤»Â~§ííCg×LHoHv\x001dé·ßýJ­û\x001fà\x000fñ¨oZA5Ì9\x000f©ü{cXg§\x0010ö>djÅÄLmL\x001dÛ+îÞìgÂ¡¶}CW²ÎòØQÅ«9¬Û	{:ðÒéá=8ÁæÚt=½bÖ\x0015e½éyh¿¡oo\x0001\x001e7²:g±{è¡\x001fTÀN\x0013Û\x0015ä÷ê(o\x001f8QÝbËu\x0003\x001aaç\x001d\x001còýE&|ôÝSá£ïpÛ\x0001»Ll_P&roX&Q9î©[\x0007\x0005]'¶-7¬\x0012r;\x0015ï÷kÛÚã¶Olà¶Wi\x0002\x001dL\x000e£Hq¡Y$#ü=¾Àm¯Ò\x0000\x0001jdN±+µÄ[»Çm\x0007l¸9RØ\x001e\x000bZ§nÏ;«á\x0008Û¸\x0003d\x001dîOÉ;ï<'×ÓXts|-gW\x001a¬0ÿ]¤\x0002Kòv\x0019´eoª7'°Äü\x0001ªî¼Õ\x001f³,íXÏß¼®o¿»\x000fÐoÿëô±wèþ¯÷ïß½}vûþÙ×§	\x001e\x0018\x0013àÀvª`k±\x0017?É5/rÃ®JB/>Ñ<ÆÝ @+þV÷ï6Åo§.ÛTó©£_\x000bÿâ³vjÕèRÛÐ\x0003dÛ\
(ïa\x0013Üy
¹V}ÀÞT?J_êl\x0019qSªè¶çàñ^\x0005ñÊ»©YT\x0014\x000c8¾\x0007\x001fôQeXTôWûËÇWÜC÷§öÅ¯ä\x001d\x0019çÑR»Áô½:\x0013ò÷dXK~\x0012·ýå²Ó·¯\x0015fHF\x0013\x0002¥5d\x0000\x001c×gÚäj\x001eïÇÒ8²¡[h\x001cz{\x000f_\x000bxu1ÌeÓ×î ¥%igÇ¤è7\x001cÞtÎ7#\x0018^6,hyï?æ\x000c
svª¿¹?½[GÛbTB 8Iê"[âÇØz«©D\x001aøðÔj£µfG9¾1Uê!±ä\x0018´¸KÌ´ã\x0002ôôMe
%ö\x001aîç)I£ûâ^k$@c=Òb)BÜuC)¼`µ\x001b¶ªËë_Ë·ùíW;õ\x001fßÝß5Á?®\x0015\ Ê£ÞÎâ·öûK!.|±àZØ!#õaAaïT\x0015Í>¨@ÌT¿ç©NpðT¥Î	\x001eÏ*p\x000fÌH²vÇ\x0010${÷ª½/ûõÇÓýÝÎôOý²Iñô¬+³\x001eo±\x000fV¾¬©_Î\x001ch3?Ä1¿t×lg®7Ü$Ä¾¼-;\x001b+\x0011Ú"ÿ;o£,Ï}<jÂIsBÌn*C9Û²>rKIR:cªÞåà\x000cåÕÏuæ_Þ~è+ÿ|zqºßa£êéfðRÒJ¤1ÍÊOùÇ\x0012mCB*)SB¡Dá\x0006\x0010éV,AÄ;Æ\x0015¾Ja¥jnÔ$\x001f\x001fô,(÷üo¿¾|óËë=;°;\x0001êS¿¨j%¶5EbYAÒ\x0005\x001a\x001cöû}ÑÁôû-`\x0008H¹\x0004\x0007g~ô÷.¢ñðê¥ý°^Æ¶}ûn\x001dNú©^|PÍíÖM/¾dbÎ·­~©¨RçÜtnY¿±ó.ò\x0003\x00036Úû]#9ÁÑHÈ<eOa_\x0013¦ÊJýn~\x0000ç- ÒoOIqÏ\x0003%ÌhÂY8\\x0013\x001b8\-\¼\x0001¿ÚT
\x000e²Î·W·\x001fÞþí§üý)ø\x001f·\x000f·\x001f®äéÉ÷Q´<?mD\x0001	¡à\x000bÆÚ\x0012\x000cù(K üD0îÂÓc®rP5£º7\x0005 Ál3xN\x000c³ÂÞK.\x00036¬dù)Ó x\x0012\x001e@bvÊn¶þhîAa¶Í¹=}|¸=-»å?Uaªb©ÄèWámÍñi4\x00076\x0003CBÊ\x001dùÑß»È>ß}üýnÿñxÕÜ÷«½Ü¤möÓ¯1ØQ(E§IIîË^Û÷!!Uh:8óc?wMº}ø!ýx;Eÿ×»kI;\x0015
ø]ôöb\x001c7	-M»í]¾uÔ®ï
»¾ýÌ@Ï\x0001«ôgÒPzëÙÊÈs¬Y³HÐ*+ÂÀÖ\x0006Ì©ËØ'¯T
\x001b¨,íÔÔTÐüq¦%Ñ°ãZ½þðºÚWw_éDÛ5³³1qµ\x0018O¯Ò4ï±ýú\x0005uEÑ!\x001cõ~\x0012'L?¤\x001c>\x000fY×:\x0001yR kòÛhÏ\x001c*ç³KÄËwÕ8=¿Ù=ÿö÷õEUþrzØ]@ÿÉ	6¯(\x0017qªKSxÆÂñO\x0012T\x000fùhöpüÐïÒS\x0015`YØø¹½\x0007Egx\x0000\x001bfdÈìWd¯è©
Ny°28DÕRÊmy±çMy¿ÿ÷íÇ®õlø Rl~\x000b¯eâ`=
áR~\x0012S°ûm\x0017{²íÆEJ]Ën7t¼×5í\x0006[èÜ\x0013\x001bÊÎÁÐ¨äædîÁNPtî°\x0013)Ùh>ÜéHéã³¯Û½\x001b\x0013ß\ÍÎ7óÄ=\x0003Më´lÜDÒ.®{\x0012ªè¾\x000b¦¿ÀÓbwÏüèï]¾ÀÏõo·?;¿@/È_©\x000c\x001fa\x0016¬\x001c Ö­~\x0015M\x000c@\x0012q
íæIò%\x0007ùjíó\x000e±ÀëdqÔó(¸ó[hÏ_ÎPÆ:ø*^XÕ¦\x0012°7S\x0019m23bw±E¬v(Y
jîíðÃtNc\x0003·£\x001fMØ\x0006:÷Þs\x000c'çy\x000e!Äõu½}ý"?èBÇÇg|÷ñþîJ\x001aÓ¼öÂ=àÆnÅ«Ô\\x000c/çÌÌ?Û>Ä£\x001e×\x0002\x001aÉÞàÉ³øm5aÏo\x0007hâT¨EÚô6v\x001b2å ¦=\x0012!@Ã\x0010'ÙÖm©è íÔjqz\x000b{î>úW¿Â®¿¶ÇúíÝ»+å2$U*\x001b²Ý¼°ÐiL.·\x000c¤_Ð·HXI}È¦_ÒIÉ;8õ£¿xúý÷··÷pIqMå\x001fOwW\x000b°eg§E49ÜÒ' m¤ý\x0017ÄQúÇê\x0010CDú6í\x001eùÑ_»È>|0îÕÃýu	Ö5p\x001eqËõÊ\r\x001c¯\G÷ØïO¯¶1îÐ«µë2¤¢©Ä2L\x0019é¾qna\x001a\KÏÙ£RË^U#ÿ4Ï½àçÆ÷X	§ÉS²W×\x0000p$X[\x0005"\x000cT\x001aîâÔÄÜæRËÉëñÉ+ÜæmOí¥\x000eÉSUt2B1­á
ôV\x00190¥R|æ\x0019\x000c.2E\x0018î]*'·sh02\x001bÊxTJj2æbþ¨_Q\x0000GÖoÉûVÒù$òªRì)\x000cðCU´\x001eâ\x0014)\\x0002O\x0010÷ê{¦Ñù¾Ì\x0004pHk´/ã@d/\x0012}P5å{â^\x0006P\x0002v\x0005Mt8òFÆeÓ\x00040\x0017y-}Ö]&PNô\x0000\x001fÔ\x0013±]FòÒÐv\x001f\x0014µ ø±¬ãð\x0016Ù|hC¬Êã®Ä¼±¾©v\x0019\x0014	èØ¨`Ñ5\x0012%³ÄÕôÙ0\x001aa\x0000\x000eè1§Ñ¼é¸\x0002z»S\x0015ësgú±Â\x0004àüÛ\x0003Ö3«¢So\x001fÐËÀÅ	
\x0003\x0017«2Êf3dÄ\x0012Ô\x00101dÙ.S\x0011\x0001\x001dÌÄíÓ_Ôi±¤Ñ@·LF\x0004t°º.Ñ<TiÚ¥{dÕÐß\x001cÖ\x0000æ»b~µû
9¾×¥kfeÂ,È^fÿmÀ÷ìKñ\x0003\x0011\x000fC6òdÐ\x0007\x001a¿&#H(3è}\x0019\x000fÆòHoØ\x0016\x001eéN\x0008\x0000ëeÆpàQñ6\x0015Ç\x0008\x0019­.\x0000>Õ%ÆLCéåß9©\x0013ça\x0000Ë´ò\x000eÓÊ,À\x0014-g5SGo\x0006g#ào_¼Be|/ÚØ>ÓÔ1K´Ée\x0002T¡
tY!Ï~ÉªÆ2Ç`\x0008§7»\x0003+ÜÓä\x001e_v×\x001aKvcÃB\x0018ÜÀ-.Í\x0008\x0015=¯ä}÷©ZÆ½mÆÑ\x0003¡\x000bÕ\x0013\x001ds×óPë¼MÅèBêuL8o/Ò¢0wßû_í¯°þÄ25­¥yn>\x001c\x000e«>ÒFÿ4Ü¦Äö\x0001d¸+ª½\x0018\x001e	Y2:M½\x0018¬JW\x0017ýLoèÖÂ3ÝÌ\x0015\x0005«ÞÓá3\x0017\x0007Ðk\x001aÓF´è0ñ¶Ô{úB\x0017RõÂ
¢®ùê¾¼m\x001f#ÿôåß\x001fNo¯µ\x0014ª4IJ¶Ç.¤\x0010ÑwlW¥\x001bÈ/Yúÿlú7ÅS?öW¡bxQè?Ý>¼ó\Iê3o!l}mB	$'g¤Y÷I8_ûB¯ú\x001e
Ñô \x0014¦.ì\x001fú»\x0007Oï>ø÷Säÿrít
\y®3Ï%£\x0006ñ\x0019­½_÷\x000bU\x0004×iÚ]2ý\x0015\x0005çÅQk²H÷%ªÁ¦ÅºÚ°+d»CFJy,ÝL«s\Í;¤ ï>Üß½\x000cfóÒÿúñá×kÝÊ}ä¥l4¬h#ö·;ij+Oò9\x000fnödtÝhÿÐþàEæç\x0005\x0014vþããèÉýpº»¿\x001aÚ\x0016U]ïM«\x0017þýN·Å\x001a¡³\x0012þIZD@:é-v¯\x0014\x001fC\x0001¯ã^ôö÷¶ÚmÈ0Ð4\x0013Ë&×L-O2\x0003¯¼S~ùz\e··ò%ýëíý³?ß~{­
¯§\x001b\x001dRÿÑgÛ~n9×3|í¼ê/æ5\x001aýM_4	õ\x0012LÏÅ©\x001f^¶ÊÒ!nvo\x001eÃxÍBZ¿@Ç	\x0012¬¸òÞ«\x0016ëXè	±/þjÓ=­óØ4üç¿~ðUczßÿYc¾y}zóCgOµÇôJuÙíÊïy4\x0017B@¨Õ"!ÀTßK¥_È\x0000,\x0017M:\x000b\x001dÀAF}8/,uÎ¨0²\x000cKÍþ
\x0015ûOY6»óA\x0003ôé¡\x000b×{PùG¦­)1Ú`Yÿ\x0011ù\x000b&½êj\x0001Bo\x0003«Ó\x0002Xk5Ú75´ ¯HO}SÉ2ÔÕ\x0002¡§\x0005\x0010i\x0014T\x0017fÚªï\x0019ú|ª}º
7\x0007aD³ÒëGýª\x0004}Þ\x0019´qÆ°ÍV°D\x001cY\x000e\x0004¹ù¶=\x0007kLôõX\x0017qq.n¿rô7Íº^½½aá\x0019'±y¼n¾C\x0006£Éj'yb\x0016åÿí)Í¢×e\x0006 þU_s!RfÁ£\x001a6Ýêýìë\x000cÀ
\x001b'\x0000F\x0018+Ô7£â\x0014ùf¶¨ÓF,MÙ\x0000¸aC<ç°Ã¿¯Ðu<\x0000L¢|´;\x0000ðMãÿðj6ìØÙo \x0003<\x0008Ò¥ýñ\x001b4\x000eÿó3\x001dÚéÒGO\x0005ã\x0001½ªy\x0001¶Ëï4×&Ñd`}vóªâF\x0013Wbì	Í/çoéñE\x0013jã\x001d$ºúè\x0016G&?e¨MÙ\x001djs¦6\x001e
yÐ\x0014)ofÁ¹ñ6/3m6hh#ÓN¦¤¥\x000c§GìxC¬\x000c Wêb¦XVÔÿøñö»&æÿÖtè¿}szÿíé¥ª\x000cÎ´ø|ggýÙUH¸ÛZ!g²¤n·ñM-|	Þb×äª\x0014»qg}ÝTèøHÿõ%ö-`ñ,çoÞ¿	\x0005\x0007ðÜÝ~|ö¯w\x001fý»p_}\Ë"ÞìÝ!óØ\x001dê?\x0019]áB\x000en|IwV^HC\x0014v\x0005ð»Pk|åN±r^\x000cö+ÒÒü\x0015µÎ,L\x0017@r,\x0011Äcì0õ©E1m5\x001da¡fÇ¶XXkØaìÿÇàÁ	;1´WÐy\x001dcFÐ	îAÝè]ýËú9Ãå|\x000f
§aiò1xàylÖ8Ûö¾np:¸\x000btò8Ö$ªIK\x0008~´Ô7¾QÿvòÎbtò±÷!\x001dK<EP¼E\x0019\x0002nür9T%óç4cÐÒ±Ì\x0013È<Ï=\x001e\x0002.»$IæN}Ð±¿Kí4#ð2O.\x0003Nüy\x000cs,x\x0007¯¸ µÉ<ôYBj§\x0019W\x0010Kí
å7'8\x0013x6|ly>Ö?Ç$ÿç²L°\x000b`oòÎòVºåí}\x001f´E+kJ"ñv¾ÔCS\x0012_ ?8uñôÈÍ¿$0º²­ÿKðþN\x0019­ÐiXzä\x0017_"ÄOö&eß|ÇqU¯~±ÛûðÊÜî<Ñ×y\x000c¥3Ä\\>\x001f_hñÛ;'\x000c¦\x000eø\x0002/Kyô©F+\£\x0015äW´ß\x0015ýü\x0015ÆÍª©HÀ%T\x0004ÌÛ`ÁíW¿!¢GÅ+àÚ
\x0003øfeuÏ¶yKÀk¥K<r\x000f\x001avÓ ÁÖï5`ûÏLë-[\x001bt°¤ùqÌ=pú¹\x0006è0¡ÅS¥SÐ\x00145÷c÷ö\x0003ýv\x0000vcÏ\x0015Õ®Ouk¤;¸É\x0004ÞÌh?¸~;\x0000<¼ëÖ¢ÝÁólw\x001eòF>¶ûþ1µ\x0005\x0006ð<Á/»\'¦NZGöØJÝm_ç´ý\x0005ä2í$\x001dtpß\x0013^\x0013<d>u_¸ã´\x0005\x0006ì:õ;ùm\x0011`GH	ôËÃê=F\x001fùã{éá^f\x0007iÜ´E\x0015\x0014ö\x0002a\x000fj?¾\x001eîeÉú½L½\x0007K_·çï¥w\x0000nðäNÈ»Í\x0002Ïc-?¾ÞOlI¤%ø0C¬Ä\x001f³§2üñÅôabËâ'¸¸é¹c;Ç\x0006%ôuþøfú\x0008fvnï\x0015pg©aYVqig\x0010ðãé\x0013H%oä7\x0001·vÎRéà1ñÉÇÝx,\x0008bqáÆN»\x0014ÉñêÔ\x0018\x0002\x001fË^Òñ÷Lð=Cèn<X\x0014¸íË¶ò1xFe©[öÅu¦n_nba«ú¸øÅ}Á×gº/Uvx¸DµÜ]¡¹×bÈ£NPçéûwX\x0010Ø"ì==Ü½Ø2ó\x0001v-¨;Ø\x001bÎ¦e3bcWãÓû1N27;\x0011¶6óChÝ]nv^§È\x0014·à±*{9¢`mç\x0001|zÚI&\x0008Á\x001b2\x0007|R6pß\x001bû¢6
\x0013<Îï@þ~»ÿ\¶\x0007#xÉÈ¨õ@\x0007\x0003\x0010îvÜÀõª&\x0016:øð©\x0016°~øLøAãk\x0012¸yþ«yøî=Ô#wûÇw\x001fß¾ºVÉEo(hî%òþ\x000bb5	¾m·í\x0017qã\x000fÔ_»OCX8)±ýfënæW©ù\x0015½
üëcÇªï\x0015 o÷*Vk·Íð=È4\x001c\x0006Åuè±±¾V]\x0001²\x0011ÎY%\x001bØ¹)îÌEpk\x0000¼n[7D&2X/"x`p\x0019`'BÑRßÔÆÎXò$ÓmYÝ&\x000fç¿¾ýö×°cû¿9=¼[Z\x0014?Mñc(R\x0017¶¯õ\x001cï£·\x0011ßÇ\x001cÇ.À/¡ù5þæ¨À°»\x0019 Z&GIR7¹Ìêí+îÑ
úZMð°]«"þep ¡@U\x000cT±\x0010éöEtÚiØq:mÎä­ÇM\x000eîãÜ$"Ø>\x0012´ë¿¬_	§³imÙºò\x0005Zv\x000e£L¨e©AÇ1\x0013H_«]\x000cd\x001bÏÜ%RÈ§júFA`H\x0010\¿e±n@\x001fÛÓù¦\x0018h]d;wû[uúPòOÈö=\x0019÷7*LÒ3%Äí\x0007ÔÜûÃÏ¿ ÉÒÑ/\x0012²Ý+ÿ\x0016£´°Å¨ûÍ£¯ðü+¢ôÀÇOmM\x0002¦ö1\x0006Úæ\x0003ø\x000cÇjs¬¯·yCI·¿ÑÊ9ÁÃTÎphz9y³ù1#¸ã$qsº1ÐÚ	àS;¥3mAjÆ\x0013\x001dÌØÞ\x0004>xî[\x0001Û\x0001v\x0006ÍOÞÎ\x0003»*ë2ÑQ\x0010@{\x0010xD÷²=¡l w%¶¦\x0007A»\x0000>C_ÃÖÕ)àÍñÈ.£Juý\x0005\x000fÚ\x0001ø4c>¸pÑ¥RÐ«ÑV²¦ödVÐÖ\x0017°§õõM\x000c	¾f
ÉDFï#MQñ ]&À._¡\x0015c72¢\x0014·I=\x0015oOÛcÓ6<ª+¸MtýcZËÇ\x000eeì=\x0004é\x0012e\x0005\x0007X¯X0q\x0013©C¿}JÛ!Æã»\x0013çÝIæÑ¸sç\x0018lØÚÅ»÷5eÇ'ÎËãSÜ\x0008Q\x001díUÁ{%\x001d<Á­\x0017.7H\\x0016~Ä#×®ÛÕ¬g>ÖÂ@â+/\x0019@]äÙ²QVÖÂó_\x001e~¸û\x0019æuýáôì~¼»}xw­ØÉRj*¥T!x2ðT\x0014ïZ^ñd.¤ë\x001b\x0000Ö6#íwtaõPaûÆ±\x0017àWI\x001e\x0011	´H{N>jû;Áãfc
\x001e|æã8
ï]LÕ³x)æùoþö÷\x0010!_\x0008\x0018×â_øHw;äj·*]s°c±Nºð\x0005|\x001aÓºü&\x0001cÈj!`¸\x001bü\x0011Ó\x0014>Ä\x0002\x0018D\x0006ý\x0008\x00026\x00100Ú\x0017Æ¢z»Å\x0018%\x0004Wø\x000bs[£~\x0004\x0001\x001c	\x0018æ\x0006Âï\x0010û\x0018\x0015( +ì06uió\x0003ØÀ\x0006îº©\x000b\x0003ÃU%4rfÚ\x0004p¨©7«l¦ÈÛk1\x001b&Gy×\x0013¸ìÂÝc`Lpd`ÄA\Ø\x0018\x0018þÆT¨Ú\x0003Pö\x0008\x0018
\x0004\x000c9)|ÎæQÕ»pl\x001fÌ\x0018L~,qâ_0v1söØ¸V]Äèöø\x0017\x0000\x000eü\x000bI§\x0000ÿ"Ù9©fP$<y\x001eí]\x000c{ü\x000b\x0000)ÐËºÉ\x0010)å\x00112S^|è^ÍB¿ØD¿S<%^­¼Èö9½áã.ÿ\x0002À\x000b)9<àÕ»9\x001bd(¹ç\Mèõ¨\x0001à@ÁhÖ<àõ´³£ù,rV`Ö"Àû\x000f¿|ÿ-¬·Ïþ|÷ÓéZ) \x0019¤|ð°9 Ön\x0013Ã»ÿ\x001ezFè\x000b¼ß&í\x0006¬ú\x0013\x000fYõr:Ü\x0007¿âQ	,_áëÔÉ¸ÿ¸=½\x0015rü\x001fNoî\x000e­Oô¨Rf/=\x0015sI!$Y¨î§Fùvíêù"µ7ÙþVRîE\x0013\x001b§äÙ\x000büàìèRä\x000cJª£ì&²ïµäM6õp\x000b\x0013Ré¹'í\x001fl¸~âJ#X"76Bxâ²SÈÙæe&/ \x001cãÔÌû\x001c¡Ý
Ç=©X¿l¹\x0000à\x0004G.÷ìi9èÈÝÊÜ\x001cµA¾@ÇüÙÐú®nÐås¡_/ÐÉ\x0000´é^ûö
Ã×â\x0003\x0019º?"éH é³\x0005N¡JQ"d8
Ø3¥ \x0002].KÅµÏLÆ¤ORµíÝc"©ô$)«h¿úMJüÇ7·o_½ûøËW\x0006\x001fwið>\x0003Û¼y?9NzÖÑù¬^V\x001b]×üÒ\x001c:õ\x000eyðv6öóAþËäwg|¬üË7;ûá¿ùSÏ¿t}\x0005ìã¯@m~É\\x0015îûZ-/Â\x000eòçb«låLÜö~9Ëï\x0011håÝì\x0010]\x0004(9¸ä¾êvð$[~\x0002üèhfö«ÿh7Ø?æ\x0010|\x001bhØÀÅ£\x0005ð1i×$
c!:¸hôÂ"pÐG\x0019ÙY&x3Üà7}ÌÝ~GX)Qí&v\x000eÓA\x0019\x0019ª\x001d#7o¨®(\x0002÷S*!oMï\x0002.Ó/\x000bJ%$ºH2ñpå-\x0011x\x0004©@V¤2\x0016BÍéà\x000e±Z@:\x0006O\x0000î¦¯#ànNb\x001c"¯UÉ¼çcð<ÁKÑ\x001b\x0005íË9å¨<N\x0002/\x0000\x001en\x0000[\x0006U±®\x0018%\x001eúã+ä+`OA°\x000b!\x001b6°º\x0007vg\x0015ã\x001b\x0014\x000c(bFWÀs"\x0000|\x0006å\x0003¼O\x000cÇ\x0012\x000f ñ¶Z\x001d<)fõe»¤:Äe\x0000\x0003G%®¸5Ø\x0011¯'_ý\x0010ú\x001agÀÖR±vÍÿ\x0011¸\x0007p;éûàu\x000füXäqÜÊÎy¸úíJqF¿ù¥·Äc5 lVò\x00199ÐíÜ~2\x000bú¹Ï©c'\x00076ËOÚXò¢m­Ê÷Öp\x000c\x001e6pé`tðx\x0016*6´7\x0008öWvkÛ¤¸æA\x0008|Å¹8)\x0001ò2\x001bÆv¤ã68y&òñ\x0013-<u¦Ì\x001avSKf¥=,±p \x001fëazØ¼D4¶9Rm´g>xésó±Äó¸¤ð¼@¹ùË\x001em-ì\x001eçî#õó±À3C?c3±ã\x0005ùÛbU&ã ëaí\x0007/Çö°G\x00013ã\x0004<Eä\x00137ð\x001aøí4½ÆÛÓ#.Å6\x0003D^8;Ée¿8\x0015\x001f»W\x001eÁO_ê6Âôì´x2.9)Ë5eÂ>ÿðË¯éG·ûøúöþöý\x000fË§Oôw¥ÀEg	æâïº\x001a-^ÙdÆè'òwÙË=\x0005­úCNX\x0001?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-01.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-01.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þåÝïo×M¨\x001c,Í\x0013ãP%Ã\ {Jö\x0003ê´\x000b¨[ô^L7WQ\x001cLKÔäWfi\x0007äØ]­ã\x0002á\x00065\x000e\x0018Ë(\x0013£×ö<ÏÒNtF=Âj1Ëí$\x001a\x001e\x000c·Ï\x0003`wM?\x0017hgQßy¤Gµ\x0013uÏþn0}TÚÒôs\x0006òtÍC]WÝ\x001a\x0014Æ¢-]2ÁtÒÎÒ\x0003}A\x001eèMøÉ
¼}\x000b\x000fl|\x000bK\x0006Iµ¥ü¤s9^7¾ç\\x0016¾á\x0005Û³Nj\x001dßQkx,³\x0019ÉëõUþço;±ê\x000b6©azÔÑi\x0012LUO¬sb\|×Ñ¨\x0017lÒÃ´£\x0013J×']À\x0014\x0004s\x0008¼m@Ôö+\x0001|\x000fM&\x001e^âyvØ¤s`PàÑ&\x0006óº?cv¤P@üÓ°é¢0\x0015é{\x001a²¿´\x001e«û?Ý¬¯'\x0007®6Õp¹p«Ñf¤Ñ¯NÞÍMcñ46\x001cj?_Õ ÁDó\x000e$t¢¼WÎ\x0005-; =Pnlæ!Ï\x0003ÀòÄùRù¿í¦Þ\x001cÐ ½SKEuOm:'ÚgL,Òzh+nR_\x001d:âªË²jbÜ8VR=V½Q³èÐØdYq\x0012°²ZîxÑ\x0000§oïÏ&
p £=K&!\x0011Ç½q*a\x0014×ú77r\x0016\x001d:ó¢1\x000fí3_[çÇ\x0008tK15ßÒ¡K¢¯\x0008³çìt±DV\x0007+}cYÓ®\x00070¤]k"©SïYbGZfyôÁöÖ¬\x0019îm¡{G±¡SV\x0007\x0017\x0007^5Ë&\x0016Û\x0007Ýn¦Å\x001eØÐ+Ë4Z\x001dJái\x000ca2É!-»Õ\x0007v!cCn^K£Íy×zLæ^SE\x001dÚ"Ý5"´F.E~Å©îÄ5ÍÐþ&\x001cìÌ,Ph­\x001dùdïá\x0000w½÷ =(ÔÊÌNÕÎgì®vvñ\x0017Ñ_a2s$uÞ4§Ï»ÊÛªvÁ\x0003\x000cuéæã\x001d"!r\x0017b;Û! \x0004®&©¸ì8i\x0004$¦vJ\x0010z*O°¶LÉ\x0011£#í©ÏKn¬	»´ßÐF;v|;ì0/iÚy\x0012 È½ÈÎlÀ&)!6Ì"¾qz
r\x0017\x001f¶ùäÒ?àºQQBL4oÌ6é®zvKUàr;zj\x0014ÖL*8}ÔÐFvçÀo0÷'@rÎÑÙID£ùß»qö
\x001aÇÙ×Äu'?_®S;`ö¾<1·3hn\x0007\x001aG\x001d;|ê\x0006¼¬ûä\x0006tØ¥P\x0013mïf$s-.6±1·áévlà>Tmµ\x0006s«;¾}k¡\x001d\x001d·fl.ØÀ\x0014\x000f\x000e\x0019×!Uvv¨aâW)ö:BçÀÆ\x0011:ÞÓÑ	\x001f³4oÒ\x00078@{j
)dn7øÉuÈ®TÖ|èåÈ#SWg÷ÂNQV0wÔékvV_Ç]]/p"\x0002\x0007*S\x0016~â9èÎ¹l'ôà¸«&eðòî§ï\x001e?´ðà6b8|mÖ¿¾diü Jë`ìòúÂgb\x0006\x001bY6Ê¢ÚI\x0006ÞÔ[ NÌLÝÚ\x000bþ;Q\x0006ìàuv\x0005§¥l¸î\x0019
;Ë5´1\x000cn#ÀÐ¡Áït\x0006\x001a¨þ\x0013e¯
3ÎjÚ\x0013u/ÈðÆ)y
?&×\x0010ÃDz}°S2(\x001b¦å»ß>½|ýþñÃòýÅp\x001dBÜökÁ\ëÀcGÚ6æÕFí9º6lhE¹\\x0001\x0002qÕë\x001c·NDXáñ\x0017÷<l&Ûvhpì´Õ`@Ë3GågWxþuéâª¶xÒPbÔAÈxUº<
ÍÕïä½ 3tr~-¶}¸\x0004F
ì©¹ÆaéO¼-(\x0013¬d#Í½\x0006ìR#Æj!útbç \x0001Ê7a?²òpF\x0015\x0011+Ûâô<Ó¯eïL¢¡5²×.û#îéK\x001dÚb\x001fÏÁV¼`«\x0013×Nµ<ÔÞ¦À¹\x0019Gr`'\v\x001a]Á\x001d9E\ùw]ÝkC_: ÉÖnh\x000eÈV±XÜä\x001b¸XN\x001cë\x0003{8ÖU\x000bô\x0019¶¡¼È:MQq©é¹Z÷ÆÀ$òí@0]3
lÌ2ïÞ¶àÎoÆ7l\x000fQºwØ:®DiV<­yêÛ3ew	äúòî7O*q£\x001b@.®iò^½:4)\x0014\x0012m}Dã[\x0018ß¹Ø?w\x0016*j(§1Ñ@\x0017_[é{üð`øçî\x000e¯6Ï,Ô6\x0003\x001cH
!U©\x0001â4nû¯\x000fh«®´êà§Æ¨´êÙj:ôlÕ\x0011P~8rjt$Ï43óNhD 3h\x001c\x001c,xG¹s}R [¤·f-/Ð £\x001c\x0002
\x0001÷u\x001a\x000f\x001cÊD_Ê»\x0001!\x0019øÊÙG9H\x001foöÎ\x0003R\x0018Z¶©`s  \x0016d¿s´ºØ¹\x000f`\x001c.vó|AÝU&\x0019ÛJÓ\x0002$îNiÛ\x001cx@ã ©Â\x0012/\x001bhÄ¦\x0004F\x0008½·þ\x000c\x001aô¦%|©Àtñ\x0015\x0001áÍBo_X	\x001d\x00074HÕ\x0017]¿&íHÙ	Óªåf¢Dij\x0010e\x001a¢Y\x000cÂr#±ÝYf<ÏwL\x0015§Ê5Ñ\x0018z¥Ür"7úL¶5ÔOj¿}¸pn\x0015d×Y-^{ÆªÜPó\x0012ÒÔW?K[
ÓæûÖ/'Ý\x000e±:DÂ^UQYösÀ\x0008ý,­áL¹ ª°\x0012\x0018~f\x001a¦1©
~ßï\x001d\x0019Ãw3å²®\x0013ïÜÀ §´\x0002mä\x001a4È
ÉwÆnXuX«ªLº\x001d½ø·qí:4©äRÞ^£\x0001êï\x000c«]Éíxïr(Ö\x0018ìåÝ¿ÿàþå'Ã)ÝY\x0015J¹F\x0007Þ¡\x0007ß:)ß ú®¡q*©WÃð´YÒs1VU))jª-Ñ¼ëó|µIDPi¢Rfin"\x0004SOÄt;ôà{W§=\x0010Eæ>`i@OÕiçì
t\x001e%äê´£\x0006V]\x0012³SJaOùøÛÏi\x000f=UoöÉ'7Ør\x0001Î`ioï\x0010·ò\x0012hÇÐ-·ë\x0008l\x0018\x0010\x000cT2\x0005t\x0002üóô¨rAP:Óæ´: Û\x001eÁÒ/ÿ|ÿÕ\x001bN\x001f9ÙÚ~ãäCfsz¼ßÀË´\x0011sy)} øbÎNúiñÉuõ? AT®\x0006~SmU\x001d\x0016¸å'¹.v}¶j$ë\x0008bM$Ä=\x0013{b©
Ùd4:pFqOSEãI¹=±®×Y¢Wl(v¨@+0×wè~AßlwÈ
üîù^6ÌÇ°3ËNáa\x0008#Q úG(P§ìÕ´µÙwgÞ|ì%·\x000eæ·åó(ÃôÓO´;4Nã2R(.²©Ã×°ÆòÞ§º!SñôþýýóãÓ­	!ñ,F\x001f®×CGWSe= zåI\x000fÞþk>ñ½ØkúÄ6Xz\x0012ÃDÄ\x0017_EÛ®Dß\x0005Ú!t\x001añ ¾\x0006_iJ\x0012}Þµ¼Ê\x001d;Ï·ryÌOZâ!ºØâ}ÝM¸@\x0003Õ\x001e\x0013\x0005¯Ðü17ûÇ:üthºBA\\x001dÇI ¥zÓ`7Y\x0013=ØQcç.9\x000b²Õ«R¨+­:ðg\x000cMÍy¹ñ¯Ð°jñmÀ\x001e¥ ²\x000bÓàB2üæ\x0002\ñ#¦Q£Td®Qº\x0019¸yzÛ\x0015\x0018´%tþä\x0008qT©\x0006öÌã\x0018|\x000e;í,\x000fwËÐÎú_ÿýüÃÞ?~¼\x0019YØMzõµæ\x0011\x0016£ïatÞ[yu¶ð~vîJló=Amá\x0001å~Îc¡È{ª\x0007UÓ)ì+©¨C[ \x0015)\x001d\x0007Ô¢ÔÛ¡óÊ¢Úúàìå\x000eü|kUo<@ë¼\x001a.,^Sm\x0013\x000fÙô÷\x001fÐÀ)ò0çºC\x0013\x0011%pQå@ö+«#{(÷«B&ØCE`õÃù1n©·
Ã¹Ccs¿ÞâPï÷\x001b,£\x0016Ýd>7]Î~îr®É4qü\x0011#6Ú¶ð·í,°&þ`%dæÊ\x0005Çt\x001aîß¶ÃÀ:tF\x0016²CBo2ü¨éØiç¹Fp>³t\x0001K\x0017ÞÔ>rÛ¦\x001c\x0017¦ØØàNxÈ>Î<äBâçiâ±,n5\x0006jOö´þa°WË\x001d~C\x001e`æca
bn\x001fñ«Ç§ßñË¯ZÓçå[â\x0018CÓDSØàÌ3ÐgGò¬Ó \x0017çOr«\x0012ëdÊ+éDÕó\x0012~Î)~\x000b4¨5ÛyÜæ +X0ð3:\x0003¥8\x001c;rûÛ}¹ÃÏå\x000e5\x000c^¹Z &¹\x0016??\x0014}ã¯aË\x001dò?(Û¬ã%y|»W]÷:\x0017è\x001f©³¸\x000e}2K\x0001NÛäÃ>ß*x\x0011\x0017³ç:]f¸\x0018\x00155ãÑSð\x0016PköTÅÙSY~Ä¦\x0010¹A©.$>ãÔ4ÔØJë\x000c¼\x000b2¤à\x0013f\x0014Ãx2	.Ø|õ5£t CF©ÆBMTÙrÛ xS;RÚÜh\x0008=·±ýéÃ
sz%\x0008r\x001e\x0004:yÕh
iñ¯ß7¼Ïém\x0004ÆÅT_ÀxB*h\x0017\x000c±¿bé±[U;´\x0003/-\x000büX2S*Ø\x0019ÖXÉµåÜýn³Æ{Òe\x0005®Ê(¤8ã+*sjý¦~e*\x001cØ\x0005óz&oª\x000bõ\x0016ÎÇäÜ*N\x001b5í\x0003\x001bâ1cpÝÓxô©ßY°7óG§Ï"µôË
¿S·xõ <'ç\x000c®\x0015'ÅÝ½ú5¹e*¬/n¥\x0007|ºóÔË\x0010¦70é¶Yk«\x0007p!`|]ýÊ°}(¶Ý$ÆûÓmf4\x000b®ÄóÔè\x001b'uÈÚ§bîRs¾K[tðÕV©\x0014=1­Úû\x0016­\x0014%7\x000bBí·È'w×6è8GÐQs85{Ïåàd©A>Ý@CYñ_ßüxÿ§K!èootLM\\x0006
ùJPÐPÉ#ó¤¼>möä\x0008m&\x0002,ùjkn¥\x0003}Úfjá_ÞÇôltä\x001b4«S}L¾®e²°£äl4Ê\x000eèDÐÈQRZÁ\x0004=}.»UY9Ae¥½ h©Ñ×\x00147Ó¾ê>/Ð¡!/ of\x0012\x000e5`S\x00176uO9úmLy1	ÅÉ\x0008ÿ)Ð¶\rßd[¥Pÿôò§ÿv+÷+ó\x0014>\x0006áxQCÂQ)\x001a÷ÚÏÑlË¦q¹3Paò`8Q³wäZ\x0007ËjÝ¥ëì\x0004
Â\x0014\x000f(\x0011\x0001rm'å\x001cmä|DnI¥]wq\x0012\x001a\x0000GB¦£4ç«/È¶Ñ0µÔì¨[|¯Äv\x0013´Ý\x0013ç.Ð\x0015 irµÆ\x001a¬\x000b;k¬6áµÍÕRç«E\x0017M¢
Ùþ²èY¾µ*AG\x001cóèÚûvÝÝfü$¾_Lk3Ü5£6dhF-¾Oüº ë¤JR'a²@×>XèdW[\x0008\x0018K
H\x0007\x0013§¿¢¯S\x001f`ÏI¯j0\x0017lR	¸CÂ¡§\x0007ØSãe=¡®\x001cÐ¨
D£A3$D\x0015à¤tömÔÛHå6h\x0007¾®:\x0002«O\x001e#Cú8ÌUÅÕÍ¸5[Wòuò¥²+ovßN\x001bÖÇ\x0011îjç+löÐ&Ô¼\x0001×e3@væ)\x0017ñCqª±¯fÏÂyvßÒ7SSãÄ­T\x0001$ã\x000eéwüÈðÍ½ØP×êÌÊUã=.ÈWVa	z[;¾@ãY\x001d\x0012%â^ðàÛÈ\x001d¥×ãf¤n¯hÀ\x0015à<)Ìsà§Z©ì°¼½\x0012/Èpq9\x0003©b0\x001cTHÓæõÛæ\x0018\x0002\x001c%Íï>|úp+²óÒ¶zÆ\x0000©Z\x000c\x0017íº3o"\x0001¾dáz%[Xàª´©ÄòUø·\x000e³a\x0010vl¸3\x0008céT±=Ï,\x0010\x0017 \x001dWå\x0003\x001bsRÄ\x0011Ò­wu\x0012xódÓjx»n®Ý\:Ø\x001cVâ\x0005M\x0013\x0006+\x0013g²Ò5W_ºÀ\x001dÿ\x000bÙ\x0006?Í\s¦»¦àÇ*OiðÖÿöVX<ËC[æJ»¸m¨±¡ó\x0012#'ï8©bc¬±XYª>Ê~¹\x0013+¤Øõ?Ï=½\x001d¸dV\x0013ôK>]ÌdõÂ\x000eØ@\x000bvlÊÌÇ0"5ýÏ3äH\x000b\x0006\x0019	¥IÕ{Yòd.Èuø±Cäþàgc4^Ð\x0019ræ\x0007\x001aû*&Å)««rú»Ìß\x0005\x0018^~:ÓÁhb×NþKûyé\x00074½Ïì¬\x0013ãÈÎ~²³ÒÆ6\x0005_(¾ðÿñð\x001cc­ÿÞ¬UÜpÉ×5á£\x000b¹&!UÛÃÑ7ÁÿÜ8
8«N0½&µÓ½2Ùai èÚë\x001bþg1¬î:MûÊ§¿Z\x0016\x0001s©n\x001e
gpØÛµtzS%ÇÊ¾`Î\x0001\x001f>\x0010ÑÓ	ØöÕO»©%\x0015®¹Ëò-)å2
\x001d.ÓÄ´a_n³\x000b2'«ÑÛ(,øÌ¤Swµ\x001e¿¶Ó}|÷«§ç?Ýp\x0002[²,\x0008g]½
»\x0002T-¹`´÷õ5\x001e¶ME;FE\x0018\x0015:¹¡*¤kîu\x0011ºý¼\x0017h\x0010\x001b·\x0006\x0007ÁæÄg×ÉÊýJxÕÙª!y§"ø(¹>7u)BËúlÉ\x000bÁäÉÇüäFØK^thà°ÊÏ\x001d-\x001cª\x0012íi,®5\x0017>ÄûN°-.Û\x001bÒÍ1PÒÇÅ?mÍ'\x0017\x001d;!vDn¶9Óøµ\x00189ùlÍ~úÍþýG9\x0002÷\x001f\x001e¾»\x001eKÌ\x001fÙz~#W\x0019L\x000bW
{çø¼³ºJ5Ð_B æÅHr2!³~X¨<ãÈÕæ\x000b¯Eý\x0003º Öaù}ú/"*«¸Ì7ï:Ï»9$÷}5¦â°Dm\x001b <ûL)t¥¿\x001f»±,Q\x0000[Ç÷ÁªekR±3²¹ëókíÙ²-.»f²u4ì¶j?Ñ´Íú\x001cõÍ$FüÈWX|\x0016hZ¬Ó\x0008£ÌRà\x0012&Û=ë£ã\x0002ë£Ú ¿¤ÊR,¹ðIu\x0002±ëO_|¥w¿½y+ý7ÝxX3ËnpÌ¢ó(VeK#µ¿´ÏNaòû\x0003èX/©mPþáí]Úi1\x0018u0\x0010ðb´ÿLÊÅôìú#½Ñ\x001d)\x0013ËAaàÖ9Í£YKî¬íÍû'÷®¨\x0001
ØÃ2«ßÕÊ<¡í Ý¸¸w/ï~ýð|;Êc¨Ü×ØA/#vÕ~ãôF¸k\x001bÑÀ:ÑNõ>\x000c¸ú4\x001aÎËËyòiãìÚéÓ\x0003Ifæqç5OF
îD°Îü\x0003PerÑM\x0006ß÷ûH¢5é~@£V\x0002¥îGFÙ2­ú\x0010\x001dÚ$7ëTòUí¶R>Á'èTwb\x001eä7ÿÃ7ßÞ¼v£6GéñÃÍf\x0004z&éIØ®ç6rkmÉ¯OôU1¹\x0015ù<OiH¥:Âà:Ùã<ÖÄäùhb\x0013­;CÆÁuXI¥NSüXéL¿ð\x0019A<O'5N\x0002AÕÍ£Éfè6>y=É\x0013\x001bIÙÈc&«
òÿ%ItýÅÛ¼½Íq: Çqó#ÃåB-Ë¦nEMå­CCf/\x0006\x001cÐ
ÂsÉìdÖ\x0010¶Qv8 á3\x0006?ïn\x001eJæât2¼ß6\x0013\x001dÐ	\x001f¼D¶\x001fÚÅÐûa	\x00072\x000cKÐÁ\x000b#dU¸ò\x000f¦é8ç\x0006½öÒ_°qNÅjìD;[Óy¼î²ó\x001bC=»»>¿¿]\x0007}`=«Ø¤[\x000f®V\x0000¿\x0015»ü×}¬½K;õ0ÈzØ¯þ?|Ç\x0000ç}0ÿø ¿þÖH¤4³Í×ðIY~XÀ-Í\x0015y\x000bÍ"\x001bZq-L+n\x001aã¨Ôm¦­ÉrÇa6­µ{åp\x001eÐ\x001eÊ :C\x0005È?³Æx²ìú\x0011\x0000®WÛ\x0001ªë\x0001µ±T¢øä³$\x001e÷Î	È¢¹æÊ6úB·Ïn¶}Bâün-£kDgª9à1ü3\x001cæ-f\x0015\s-­\x001ad\x0000ËâÃ4µ-òì£\x000f÷\x0013h\x000bÞ±Á'F \x0013\x0017ÑC²MO\x0008\x000746HYy¿\x0003@Ï\x001aãs§,l\x0002êå\x001eÕ²5³ßÍ§©\x0016æw/=Ø*¦®Sk]â¶®Úl7ª¹\x001d\x001a\x0019Õb}8Û0Å8ÛñkÙ©ýYO©·þâÃ×\x000f\x001fÞýîùþ\x001b&W¸»56IøþSr®(
¥Å:ûF\x001bGÓØÉÑÌT\x001a6f\x0012eâ\\,í6ÞÅy jÖ_\x0005 ;	v@W]Õlê6­#jÿÓÃË\x001foõi#
4!k¯N\x0004u\x001c'±[|õÙþ¡
«cú\x0008VÐÌ4U£}r{\¡\x001aüô}ü\x000c=òy°`U½ë{¦\x0016-;É\x000b.´¨eC¡ÓL\x0008^ÎåiÅn{/õÕ{A¬ú|«¾jXZÏ6mKUÝ\x000f¾VºêÏðÀtó®Ç6p/«7¨ETÇ'\x0015PkËìm¶H7\x0000ÏU
cXj­²Êk0}Tçæ\x001dìÐ\x000eWmÛ¼¸+4	ä(=d\x001aA»a«ôé°ÿøe÷\x001f\x001e\x001fo'6Ã\x000fgò\x0006:\x001c-&\x0016½&º_½?ë$ÒZª$ÑLt²ÕòïzLÝzo­\x0018x¶DÌ>Ælî o\x001fZ%ì-|è k\x0012µ»Yü'öÔ\x0003_\x0000º\x0014oÚÚî*×\x0010cÎW1YåNcg[Ì±)¾°~Ä\Séçdùüé»¼OÙ\x001dÿøòÕãû\x001b]FNîÜY¤)_\x0011Qù*×^ÞHÚgÇ¯\x0008eâW¬ÿ¿}çOÌw=½¼úÃóÓ77K¾åªYÍ\x0010è¯¡ñY.·j.w¯^)ÛWn7ùæÎD|³J·\x0002¯¶5\x001bZf(îRk$[#Ô\x000e]Ç)ËÞÜÆ\x0017¯ãh(À$<ò1zu\x0013±7h\x000b\x0011{ªÔ\x001d\x0019L×àï5Í1µ®	íl2Î\x001d\x001b2Î)\x0016ìóâ§\x0012,§}A+¬Qãç©¶êÇw¿~þû¿Ü÷ãæÉ>&X\ó\x000f\x001f£4 øê\x0017õÞÙë\x0016
-äc\x000b9\x0017Æ$ð.Ù{ÈE>¾k«î¶PÆ-¤Þ.4ª\x0018Ï2º.yN\x0019ú^yÚ«=°A½FõÊ\x001dX]"U,=ÉGá&\x0018_vôl×ÊÎ-ôþécß@ïÄ×½!mLî6ÊÉrMf³bñvPµÒôêOÌ>}²>ó6MÝ\x0008r0±Ê¦xG-ìÙÇÍv;
ik\x0003Z³\\x0008w	½8[¸M§\x001a,÷3¹káó>?=þåÝïäËÞºë}a\x0001?Ó´¶.^(ÜVrXm\x0019Ï·Ð\x001b¿Ð¾2!Lt£z,_Y4Q`ÇÁöÙìË­pAÆÞxy¥®Yf
T3Ë\x001e\x0004.7JxÝÊ¯Ë`¿\x000b4\x000cökmæ@'õKÝ¾Ì9\x000b·Õã½@'6cð@ËsH\x001bÒOó7MÎa'~ÆÁn\x0008M(	Öp¾A+°\x0004]ÜvÁ\x0005\x001a\x001eÚfëq¹§\ù\x0011\x0017ãÒC+\x000fCãî.Åÿ\x0003Û:Ô´
6¸&\x0007¹¡ÅoÕõv¿`{\x000cáÜp>\x0004[ÂhØÚ|ð·Û&ö\x000b66ö\x001cùºëºåå l.ª*T\x0018~\x001bÐCs®Ûñ\x0014
Ïµ\x0008Ù¼uK¾@ã\x0006tP´ð©\x001aþ\x0012c¡âkî\º¥ëóÍ÷\x0011çF¨\x001aË\x0011\x0004Êêh¼£«÷¸~Þ?}}ÿ^/°5vÉz_ÿíYïd¬ÿáCKj<}øðø°vÐ»í­?}+ËêÊðLÓ\x0003Q/¥?\x001dX3ú[ÅÅÍ}#ÝÊÏ\x000fªÔ¯z^?âjþÖ±\x001e^¬1Æ¦\x0014ü£ü£·1QÑ^\x00032QÓl&òIÅzêÕD¡ÆUÔåç4Ã$åïÅ_k$÷kBà\x0007î\x001f
qlNþÚn\x0015bK/¥\x0012óÚs3ã_=^úo^><~ýøíÅZ\x0019¦/Úá¿\x001cø¯h+êq*bm¯YÿU\x001a"#JN\x001b»bjÚ`ßo¾}ÿL§\x001büï¶\x0015&ú/]Wóoph¦ÏoTRLñåq+röirô\x0007î\x0001\x001b"î\x0016']¬¥|ëMZ\x000fKüIöÀ÷ºwÞÔÍô]~_»Á¸S;hvî:k2\x0015¯Ê?\x0005~¾\x0003\x0006gûà¦±wÝ\x0019òµ\x000c¡\x0011N¦b+ÍV\x0016ÃÑÐ\x000c\x001bZ¯¯?CöcÍy\x000c¸Ð%\x001bl\x0015%;Ç{´ûvá\x000c8\x000c`\x000fÓqeÉ4Z@@\x001doCã\x000c8\x000eà\x0003|]r¼3deKÈU§4,­Ú\x0006²:Íc\x0007ê`{KÆ\x0007Ðªï\x001aFmÀ\x001d\x0017Aa¨)ÉA©\x001c\x001do\x000b­ØZ¿tj\x0003rùwßsh>yàVÝæ\x0001=B\x0015®£¬C\x001b²F\x0018ãa:twèÎv³Ý\x001cëh"\x0015èHCe¯gC®½uÉíºÁ\x0002\x000bò\x0008Óª
¹Ï^\x0015 ù Ä¶êE]\x000e÷\x0007ªËÉ¶¶#iªf±w·5ï2§Øòùþ9ý\x0013¸kß¿ûÕýÍü´b\x0012]2ÚCtY|µv8Ò©\x0014	·~\x001a'äûS#9íBèùvSq'C(*¾5n\x0016-÷Zïj®t¼ë÷yÞõWtðÚp`£\x00140\x0005æè\x0014\x0011]Ã½å\x0013ÇÿûÃWþ\x000bdI¿yÒ\x0004ê>rôOHt\x0012
ÓÜùa\x001eñ»ÖÔ×ë<¤ú}\x001fWàb«éÁK\x0012bã%\x001f}Ó¢\x001a\x0006tF3@1~s\x0019\x0003ö¸³£ÉYp1(É©ìs&lÛTbKsÃµ©)¶à\x0011)y\x0002î¦ÛÖlg÷\x0002À [P°Å)ð¸ð\x0000\x0006
ÛØ\x0017a§D3F\x0006\x001e)î£ç	¼K~¯;Âº3yÂ^¥ãÐ(¡T®vflé}\6ýÈ/ï~ó÷ùøðüÏOËlø\x001ft¶µ6Á\x0013áÄá¹Ò(¢^=þ\x001aÄåW\x0016Åë\x001c-ùqºÙê=É{%¤!®?!Q.Åª\x0016þôëW9\x001a@Î\x00039ÙÑ[¢È±ñ±\x00072m A¶M~1­¾H\x001eY([h½\x0015º\x0012ÿÃZ.ºu-\x0017þ\x0005:\x0003t\x0005RUNvCv\x0013tZÛ¨\x0007ôèGÚ`\x0006Y\x0011x¨(È¡°A[\x0019m\x0000m\x0001Ú\x001aPj:
È¡\x0005Åèã\x001b¶5¯áÀ\x0001ì\x0007°8\x0011óÿÇÜ»íhz\W¯Rðý\x0014â|¸8mM7Ì\x001eløf0 dL»XE\x0017«dK¾Gè[_µú5ø&ý$\x0013;âû¾X+\x000eIMæ¯Ê\x0002\x001aÝ-%µ\x0018ÿþâ°\x000fk¯­*')ýa{´a25,\x0006ý<6Ôj£e\ù\x0000=\x0016\x001fâ JðÛw\x001f?T:Õ¯ß}|ÿÝÞV\x0005ÔM¹bÍækè½ïÆòÃ'¹\x0000¼©2º¿\x0018¤\x001eÍý\x0010¤Öûõ{Ó¸sÝ{r\x001c\x0018§ò*H=
 Ì/ÈR' àL©1~¡\x001dÒ{qÃ¥×5×ÄjG$mE¶a!EÙ- øº?zÁdÌZÛòÆi;¬ÙÍ@\x0000\x0019ììÚ¾Ë\x001a¦^a°è<@×Yª~:¤\x0007´ï1»\Ð`h£^gZô¬«l[Ø-:À¢
º:"4aÐ\x0017\x0012§¬\x0010\x001e\x000bô\x0014ªÐÝ¿HåøC>@&êx´G·Gy%\x0008Þ}Ä\x0004>W\x0002U(7MÄ$¾Ô¿1RpÛÏLÜ .©\x0004W¸\x0008(óa	w^	\x0007jéAmV­\x0015l=\x0005½öM\x0003ãdÕ#vó\x0014ý\x000eÛEJHÝ?£ôOjrB³eèVA\x001eU6:t\x0006è½íØe/\x001aò\x0013ÎÝ\x0018,;sk0wCÒÏ¹W¤à\°¥í'®Z%ònÖm\x000c:æ¡ù\x0004¹­:'yâu«c÷\x000e\x001bÌ\x001d$"íÛdPphEaÖ!«6Upw"
H¡\x0002Ä~8±¥E 5C\x0017§´ÞPS¾ë\x0010\x001f@:H£~ßNSjqË½ç¼­;Ðê¼ÃÎ\x001d;$L5¸rÏRî"§BË«#Ð»ÕÂÍ\x001adsÃ²U\x001bn\x0003ËNÝF*¸Í´\x000e¾äÁ¦9#LÍZ2\6yÄl\x001cä\x0003;EÀÖ\x0014aEË×È`qâRµ)<»uÃ©±j\x0013±â·¹µ£¼WÎ¹I6n°\x001d\T2P\x0001ì->A{KÖcñÚïÔæ)s~\x000eÒX\x0006)sï9Ûbsvíª\x0014ôÁ<°!\x0014÷\x0012-÷T~	ü6pBWRg\x0015{³\x0007\x001dDâå\x0006Å,(R~ÂFN\x0004x`Í-èzJ±oYÂ\x0008JpÛ`8?\x0011ê±tnsäå\x000f\x0017vùxhoù¦²ÐoÚ°++ÂMqþ
Q¾/\x0001 \x000emx[k\x0013aûw»kÐ\x0005Ä]ÉA°Iª¶`;6wýa·\x0001\x0005àÐ¹\x001c\x0002ì_­âÔD¡àânÍ\x0011Öì2­Y\x0005~Í¬æ@#7Ñ;7Çi\x0007v¶­ûkfÝR±y¸¦F¾;ï\x001eÎ»/N\x000fxÛÒ`G{Û\x0004ËëVÕ{»û5ÂýZÎ~×s	I\x000bÿ\x0015×­¦ýWQM?ä)÷`gÎý½UäO©²ah[?e9ôkè\x0004¡MÜ÷hÌ(ØnóR¦®n!¢\x001b¯ãµìâËÚJ.¿X\x00059eÂ\x000e¡2·ÒÝ8°!m­íLõ²nM½¶eÝ\x0005)dÕR\x0010\x001bì\x000c×«äM;£!Ê\x0010ZL\x0018£Â5É\x0010jª@m\x001c*
3§½{°\x0010³X<L1ó\x000e\x000cªM\x001fS§RCZ¦\x001chý\x0018bÍ-\x0011¸ækÊGßr\x001cyý1ë\x001f.ð\x0012ôF\x0000ü.X-1xù§jÕÌ¬/úCK`\x0013\x0000¼\x001cL;¥ø=\x0003¸ÍMr\x0003n\x0015Ë`V\x0000/NVÀ»D;Åû¦fwÓöÏiSÙ*6Èðy¯U°-{\x0010þHÛ99x\x0007\x00009u\x001d»\^\x001a?§3¼W¼®¹Am7WxýÃ}´và2\x0002\x0002±]`·ô@Ù@;ì\x0004Ø1ÀU\x0018k\x0010K\x0006gzDCM]t·ÉÁ\x001f,\x001b-B2¶7Eï\x000e®©%­ðísæu¢§þ¡gü²rKØ|©ûF#ÜXÅÁ6LÂuîÛ0Æã\x000c\x0004\ÓK/ón+øÆkÓàµ5pCàWNÁWìÝçtø9uèS|
¶8qmz¹ËµÈ¯}Z»õ\x000f'xmv}¨4ñ?o=<\x001dj±½\x0012ú{_ö»\x0006\x0012AY9M§(¯êhòÜnÛ 6+\x000f
V~ÔOppüs±ZN´Ë]4MÑNmnÛÐùì¶<W´ËerOBðÄ$\x0013×¼7\x001d6ï[ýÃ\x0005î#=Q¾/a;køì·uo²õ\x000f\x0017tê½²l÷\x001a·¸wJ¨µÍ°³w×ª)Ð	²J1Z\x000ezI\x0014\x001füöþÝ5\x001eà\x001a\x000f%ª4pîÅ¹ÀëPûaû\x001aÀ\x0016ÝÂ=,<Âä\x0002nÒð-C¤h­Ü½M´|w\x001d\x0006¸\x000eC1±\x0001M©	Üh\x0006A&2]ðB®¬)ñBdøt¯ÎCzsH~ëpÞwÛK±ë}ÕÇÂÐu®V\x001e»%\x001f¦Ù¿\x0000x(\x0011fwø£¤EÊùç3ªÛ¦)\x000fÎ×Û§è«¯é½0Þ\x000b\x0018ä]\x001fñ¥;énýÖ\x001fr×gjøÊ=²/½ÊG0´^¾DC}ùÎi\x0003ÕÇ$ãc½5©a¯^±¯¥×X+ôxHd^2È\x0019OµlË7mwfù\x001bíÌârö¦FñcÖ1\x001cç\x000bé½xïËÕ\x0018`ïGl<Ô~àö¶%ûö?ÂòñH¹ø\x0003åÎâöÇ\x0003w[HeØBQAK¯<S.{£8åâb¥\x0014oùÝþ+\x0007$Ë\x0013-s,e©3í¡dÚêíö\x0000[:ÀBR
°úl(ß/-9ÃýPÕ«Ê"¿Ý/ÿ[àE*4¾qîý\x00129º=EÖlÁßÀ¡-0â[\x001aÈnTº->Ud;êû\x0016RÄ\x001f¡Ë*Ñë\x000bp7\^¶\x0005Î6W\x0005Ââ²ê×ª?2e\x000f#ÅBJFÙ`<×Ð\x000eh¬¡ð\x001avh	\x001fH:TRy\x0013üºÐÕ ±Ð\x0015=º\x0005;sÎÇG~½n¢ÆsbæÄî(£¥\x0000»\n\x0001-â\x001d°[n.\x001cØ\x001a±=rIåÔ:*½è\x0019{Ù\x0007Þ±±\x001a¥»\x000c¾@û¡`dÕ\x0000Ý^t3S`\x000fè\x00066ÀeP7º"lÏD®&dgv\x00061`rIºDÈÄB÷ÚëáøE#VÇ\x000ePdH\x0019\x001fB-\x0019\x0003ºà³\x001bve¸ë9y|b#mnyô\x001f½6Ñ\x0013;âº1\x0004-@ÎTÔ\x0019:¹u5ôjhá­pÚSb>ºó¼jk\x001bb³j%\x001dn¤[\x001a¤s\x001e(J÷[\x0010Ç\x001b¶Fl9G#ã¸©\x0014e\x001d¤þ\x0016EÜ\x0003\x001bMÐ\x000e<½ÈÚvbw·U»\x000fiðC*Ó\x0012\x0010°µ%\x000efì£vz¡¯{\x001bü¼'ÞÜå:Z1ÓÏ«\¤h¨t©Ï¡éÜ;§Ó9½ÒÎ\x000c¯ô?¾¿Gña5÷©Ï4×Æ¢M¶ïùØõ¶ÊÙ*Çi"ú^éh~yúV3ØWL\x0001\x000eQõ6Ûö&ÑMÆ§ö\x0008\x0004§´Û\x000bèh!ÃTþk>åæç=¤¼Û\x000eÚÑ¡tRâ1Jea8\x000cO´]2¬\x000eh`XU"\x0000x\x0016Å\x0019Ð\x000c\x001d_³\x001d3\x0011àFZ±{m\x00189³=Â\kõSyíD²tÄL{v#tb{¨Zï±\x0013\x000fêN`\x000f\x0018ç)Ð\x001aHÜèT¨\x001aiÌOèO¨pya+\x0007\x001c\x0005Zs*Ôo¢\x0013ÚÓþr£QWMÈGkÔ\x000e9zÚ\x001e@ËÑ*3\x0019¿<'\x0017­\x0017r\x001d:i²\x0007ÄíJZ
<_C´ó¢·Í]ÙEùCç \x0004$Ê)b
:ÇuâT_%m¶ü¡/Ú£¯¢D-Þü@Û£ì&·fn\x001dÐÈ\x0011	\x0019Åvìt:j_.Ø±NO]8\x0014
\x001c`»Þ\x00141k4\x0001Ë¶\g¬#WáÿuÊ9ü\x0001é-"ç¢hD6K,?¦\x001eõGþ
vø7Dü r0\x0017X±rúvò0c\x0013u×áþòþ½\x000c®¼U¹-1:;©m\x0016I	y2ê¯ÒÿË3p¬^\x0003SØº©=B
[T­¡XòP\x0001\x001a9j]lÎ1\x001fÈ\x001eáÁ¨UåÀÈ\E	*×8Àm å\x000f\x0017´MXUj8\x0006¢Éköz[\x0011\x001cÖ¡{h.{ø|Ç\x0013¾[\x0011Ñv0£Ð±{÷þÛ7ëîOÌÓJ5avzÖé\x0017é8t*Å~\8Gzrävä\x001c\x0011ÿÍy5ø]õÉ6ómß M¿í½¨AD\x001d\x000cóJ¬I·Ø¨ó¬G¿K¦È`°îÕÀ¬\x001brv­ÇÖÍo_Cvýí\x0013½C\x001e\x001d\x0016\x001dÂàwÕXÆíLíÀÔÊvmx¹çÕ@«K\x000bõBj¨C\x0007ïÐ;ò©²n±\x0007T>~Ú­:Áªµ§îüò3Ñ+G6v«þ6³|<¾x÷þíýw\x001f¼ÑIõ
 %ò¡G_^ÃM%·!èoi)±5_fL7ª|Ù \x0006õñßÃ\x0014ÞÚÇ8j\x001cud ¯)*7ç#1c#z®sD×ØT\x001cUÅÎ£\x0012\x0006_oqú!]âÏfj\x0011>ÏÞû
Ò=©Yº:Ø{"ö¤ÌBS	\x000bü\x0015\£\x001cC¢;\x0017Gxõ8ü­7¾°\x000760a7ûñÑ½\ÁÓÜêÖÀ\x0013Äx\x0001ó¤9Ú84\x001bÐ³*ýhµFëÐÀµBú»ºöþQÔëÍÐ\x000cY~J\x0005ßìCûP$
"ÊL\x001cØxWÔ®ìª®Ò°ÇNºÿzÿñ÷7TýF±ß\\x0007´\x001c9±rPÁå6Á¾âüù/7ªÅ¾ºEËÛªÔ5¶éeÐ"\x0016¯DÈCÑ]¹à6dà
ú4ï\x0012\x0006\x0013´4P¬\x001bÓ\x001a46¦ ªSYÈ:Qwô{lZ¶`ù5hx¾Ð\x0006Ú:ÅéÇYÜbjE¦ÖÉ®\x001b't¿e2Ö}ÈÅÉn\x0018­\x000c¿9³qÀBf#\x001dâÜ'²ñcc¨@Ð±Ê\x000c,\x001aÞ\x001atBcxêÁ
Ó1\x0005û»B­'/f\x00074®Ú\x0001·Oø©£)\x0013X k,¿àg7hàgãÂ\x0014¾üï\x0019IüÒVÃ/½Y¶Ö¸l­L¾ü«2wµ¦Á ¨¹¶\x0000\x001d\x0012v[zcÏËNÝ|ôU^ÃÆî\x0013$Âjºgsè¬i/-RATÒJSYæÖ:ÌÆ&Æ M\x001cD»"T:¦=t¥6¢Òlî'ù\x0003®\x001bÒvUG*\x0011¶eì6`Æ,Ú\x000f\x001a¶C{\x0007`"%+]d\x0013ØÞM\x0001Ó¸½Ód\x0013äÙ$\x001aÉ(ßÛrB&Ø»oio©P\x000eehe*ØÜÞUºvÑÚP¡-TÐÅ$¶ÅÜÔY\x00135s¥\_w÷ÀjËÛ\x0004L"9\x0012^v\x001a¸S¶MNßÄ\x001a674wI!óÉáF&[\x001fÈ\x0015]½A{Þ%\x001a­í©C ùdÅ\x0003«ÙF¿ñ\x0018ä\x000f
D¦â\x0012© `³¹S
CWz\x0015ÛQGqÆÂSq1ùe\x000f~¨ê¦Ê[ñ²\x000fl6·f\x000ePàÝ=\x0010-bkJS\x001b8ô¢<=gu>\x0013~k{×Î$è6øÃ1D'q¬ÕEïw\x0017ù
LX\x000b¯Ù\x001ez¨\x0010Õ[ÊíÞ`\x0018\x001a9\x0005\x0007y\x0015\x0016Í©X]KÑ\x001bl¯\x0018\x001b9Ua\x0015cs®¢\x001cÑVæ[ü\x000fìD{\x001b\x000bµICjXwGèçüêí<Ý\x0011òó*\x000f²\x0015FqQÙ7\x001eæ¢KªaGÜ$ªöº6ñéµÃW!\x000c\x001cu\x0011ê\x0015¯u\x0003\x001dðHÊX¨AÿHZÈÜï\x0016ZXôÎ\x001eØp»JC+ÔÊ±rÍy¸\x0012FTbçüÞ°¡-Ë¸MCan\x0011\x0018jE©ª\x0004·Ù&ÁÁ61¨1\x0013sv¹\x0003_¯ÍW+ÿà\x0006:ï`¨C*û¡Å:\x0004®¾\x0007]+s!í°\x0013b{lí¡÷$\x0018òjPµ\x000b5î|Ì>¦ÆG8Ê4Rª7\x000fEPË]¡7ï»ü¡?
	¨>1ð0A[.8\x0017_\x000eeÞíîÌ>Ñ\x001d\x0002b·óSå2¨Ì\x0017h	5´&u\x0012ñv>X¬Ó´é-³ìñ´»Zõ{£µ÷F#S&zQglö\x001dQÍ3SØ\x0015¼þá\x0017Ù½ð^xIf^¯p£ècjê\x0015%ànCÕ7[·ç«oèµôà(S\x00134ð88Ú+Ùªæø¨\x000f{ø\x000fü\x0018Ïf\x0003ç8«94ë6}~Á>\x001fäX=Íý)kÛ\x0000®ÕM«\OñsÇÕ³Öjv§q6«·Ä\x0010>0[U%dJh\x000c/\x0014)©gòXÿõÝ×oîßNsWX..)+y»Îß\x0012\x0017ÿú\x0004·ªáÖ\x000b\x0014\x0010¢V«rßtÆ¬\x001bé[åfïEAwD*ÿ\x001dnÒr7á\x000e\x0019I¿É°C\x001eþ@élO	\x0002Ý*Û;h\x0014üqM óö\x0003AÇ+ÅÐ¡¶ØØ9ØoØ\x0016}µî¼³ INò\x0005ëç*¾o-%nÖíÀ$"?ÝC­r£i\x000eöµ'k<º&Ý\\x0001=°-bB
¢ÑCf}%Il5\x0019É9 Á\x0011h¸eæeÊgÁ®%a·û\x000e>¥s\x0016®±\x0010Í¨é¬éå¾iðù9«Ü°=dmvP\x0014\x000eõý\x0006hÅ\x0005¬ò4ÕTÉx\x0007´Eh|÷¤;c}å)qX®»\x001a³ØéI=¡AJ\¡°¢XrJ\x0005¢E«t·WwbúBrP\x0017j[ÕuéØôâÅÐÊä~®\x001fÐP'w!B[T¦C\x0012SÓÂ¡èUÝÛ~Î\x0000\x001fØ\x0001.ÏMï 
"êI¶\x000eTÜÁÖ;ÊÏ©¦\x0003\x0019RM6iH´P\x00166w\x0017{P'T>RøSÀÒ 1`±%°¤&ãÈÖr\x0008åa©;;ÌÙ·\x0003\x001b²oëçÑ7«}×\x0017`ýÃIÀ)ÿklMuÇÏè¼!ÇÁn=«Ön;µv§¬ús#[bæòÃ(³­ÎSþï
t\x0000Nd{^¥\x001cvCÞ¢\x0008Jþ§u#°\x001aS pE4Y+B1\x001bH4\x0018*øfk×?tp­®"¹@Í¢\x0015>à)\x0018:°s\x0000l\x0012¢î!$Å\x0014pîtþ\x000eß8\x000eõ\x000f\x001d<c\++W´r=,¼=\x000b÷óz\x0014°\x000bõi·[¸þ\x001dþçÂË9ÜÛë\x0004Ab.Î\x000eô¥» IIÃ«8\x001c¡Ô\x0016¿\x0006¯¿{Þâg\x0002ZùÎ·n·C¯vªÔØ¨Qn\x0016H<K{~î6org"RCáZÄ&¡ìdb úM\x001e¥*ÄWª=:\x001bh\x0013\x0001:p¹GÌê¡YÕÙhv\x0007m\x0001:×\x0010|iÃ²Öñ¢æ\x0005Y£!CÉ©9a"E¹r<ÙCë!*­ÔùyFCÀÃó¤ùg´ãv<«9bz¼Tç¹"
\x001aXè\x0002±kHOÐ®ÒÐ\x0017]m
\x001aºÚdCn»<­(L#Çc@®þEÞ}Ã\x000cßÐ£:¾wv\x0019Úclõ@óÎ\x001c\x0019ÍaU YØ\x000e%²Ôt2Wl55²Õ\x0006!7ÚÔBÜÓCn®\x001d6
 :\x0007AaÒ"ßáè(\x000e\x001dFµ.ÓàÔ°¡Jë\x001ds\x001e½åÆ[«8\x0014ÈJ­\x0006*u&^ª!m>Å¥kóÙa\x001bÀvÒ$Ù¹ÈiE\x0011· ìP\x001eé:\x0015§Vö^}ñæî\x000fólÛ'¾\x0012e¯²+\ÇF\x001cö1\x0011Ó\x0008eÅÕô/ðJøªÙüË"ä±\x001e(¨&Ê\x000b\x001d!\x0012([Ùx\x0004Gô©é\x0019-r¤q<Q"ªÁ<v¤'sØ\x001ft£=,Ô3cÛ=\x000e«(Ã
Y\x0016\x0013H-²\x0004G-q¼¨\x001cØß	MØe1>\x000cWuÀVúÄ
\x001bR
>bKTY Ã$ê-»­ELUm\x001bv[W\x0014`ÝVsw¿a¥ßboß°çË8C¢ü)\x001b¢:m\x001aó~g¤\x0008;ã)\x001aÂËmÒD\x0017Z`\x00076ø@reÁö6C&Úp\x0007llDEiø@»Ñ\x001a`Û;Á±ÃTu¬Yè\x0013\x001fØø%5Ä/ÕÚ<XÍ\x000e;°)éùm>°ñm6NN¹Â(;dñ\x0003öeR±eâD"\x001bÖm]Õì;=1tn\x001aþ\x001bs[ y­@Y^Fî°vÑÃURsªÄ®&C'§«%k\x0016»o%Ø°\x0003æ==¥´Ü0Ô@\x0007Ço­RvÁ<°áý¤©~!5\x0016­òp\x0003æ½Ù#ò\x001eÅYPÉ\x0011æ\x0017§Çµ\x001b>¤i,§E¿aC¿\x000e
ÄÔaÚöf°IeL®D"\x000fl\x0018û\x0018Ð\x0013­sv<µ\x000fÃ[Þ w[;Z2ÇOéF>\x0006¶Å$aá®Ø9°ýøê×ï\x001e~úéÝÛ·÷7êKÌ\x0007$`ìûÆan¤ÄßÕïzÂP\x0010O~î\x0003è¦²à°77Uó?Â\x0004\x001cè#JZ\x0014Ê\x0015\x0003Ä\x001d\x0013´aã\x0008§aÅ¡mÒ\x0016Øÿ¡15\x001f<Ì\x0018¢eïVãf\x0013æ'úÀ'Ú£ØAÁV8OJúQ©9.Jcà\x001cjä\x0010×Bñº#»D~À®Y#³8´\x00076¦)ð®ëæç?\x0010\x000f*¦	ºp[ìì¶h\x0010û(Ø.ë&ÊEÁ®u¾rv7Ø	\Pc \x001ew,ôo,\x0017,DÊ©RAçÛ¦b[\x0005q0^Á¶\ú,Áúm7\x000f\x001e¼\x0018"¼3®Æq\x0007wLMÛÎ]'6Tãr|
òCÖM¢øè$ÓÞ»RgÆ\x001a¢E\x00134+ejð\x0010àú$-\x0006
ÁDñ\x0001QV°\x0013×'\x0003ï@ÓzÚw7¥ú$µã«èg:ÞeL-\x0017½r/ìä^&KÿZsC\x0008Í·É!¿ Ul\x001cÙ°y&\x001e}bÖuÕ\x0003\x001bëª·\x001c\x0006²\x00121Öc¬\x0015\x000b7·\x001eÀÐþé\x0005ÖLÈåf!·eØ~±\x0015CV2ÿ
\x001adþA	\x000bFÅ\x0001\x001eËÕÛws)ä\x000e´j$JLÂª\x001a·D2µAÏÜ\x0001\x001diÕAUf\x0001(­,ûqâìÕÆÖ\x001e§JëÏ­µæ>\x000f5\Qá(\x0005/Ô\x000fì\x000cØ(=-RøÃ\x0006QCÂûæ	ö\x0010H8ã<\x0018R\x000eL.CØÆk.ð
\x001bð
îgj\x000f\x001bdpÉk)xÑåq\x0000{26:û"At\x0001[-¹²jìÝ{àñ=v\x0014ÀNå¶JÜÊÆ\x000e5HöNí4í?\x000bÁfy\x001e%W6 \x0007WUlQÓ?¡¡¦¯q\H\x0010}x\x001cÖP­\x0006è¶G\x0016Ýs
Û[:\x001aöHü´\x0017sóôºuK`v¾¿X$Ëìñ\x0004E"üå´Ã{S<µ`!øû7wß:ÿpW\ø\x0008ýÛû\x000f7Ëz=4W\x0005ÙË,\x0008\x001aì¤ïûe¦Ym1uf-ä1\x000fºù	þüéüº)(LÊ\x0001¿½ûáî§nÔÉ+¤\x0006êÎËUO£\x0015wW@ìÈNÄ-_ög£Q«NÞÑ=øºì+"çYQ[>v¹C:ÎêYÆdÖìë\x000e\x0018Í\x001dÞtYn\x0010Ú¡3=Å°u|ÖD^:¡-èßË ÌÞe.Ðh®L0`hµ¨{<V3>¾ú»»ßß½ýððöVÑ<U4PFUDËò$×ìÕgs§WÁ\x001cÇ¸¿
ðèÏ_5äë\x0015ÿàãûßÝè;4¡\x0006ìT÷^ý\x0011^²\x0004°O­ð%_F 9×äç$¼h-Ñòù+îñå\x000fPÆ\x0017\x000fÎ£+.º¦øóE¶¬¶l{rÒ«ò{¹ @[\x001e-ÕRE\x0011/.í\x0007tE[Ò·Y.\x0008t³r òAnz©iD
¹O#*È	Åä²	ÜV#i/È¥¡¬:4\x0017½^¾çóØ7¹i*\x001fôZ½\x0008è\x001b¶\x0001D\x0003êÈ¢\x0005£ ÈÍ"rYJ%i¹Íg?tdj5Ì>á-/ÐdjÈE¯ºF5gð¼J¨FY®Zl\x000fp\x0012C'\x000eM¡~g\x0000öÈ\x001eE\x0012s4èâ;ñ¬émö&nT\x000fìÎÇðZyS,ãÇ \x001bËR\x0002\x0019ß&,T\x0001\x001b6¨\x0002z]"\x001e­	\x001d\x0007\x0013N¨\x0005Ý{Ó$7_ÒÀ¸y]¼åØ¤*^±Ù&>×éJÇ¢bwO¼Ü\x0011\x001aÊY§æ#'<U^wj\x000cEJ¿aGÀ¾å.O¤å}Rþw¼îTcz«76?Ø¢µ\x000cÓÛ;Â#bG\x001dTl°ÍºmD-_\x0006[ëJX­^£IÊéä\x0004st¿l¶ í²|ÞØ@ËN\x0001\x0019ï\x0005Û²æD0ÍCZäy\x001bvÏóÎÎk.1\x0010ÔK\x000b4\
LjãæPÊ\x001f:2jæJäÎWö,Â\x0011\x0006%ç\x001a¶ësÞ$ä_¤\x0004æØ
v¦\x001e\x001c\x0006©n\x0007¶M"ã±SÇ.ßÕà&±:ÓEU\x001cãÆÅÜ|I\x0007_²lFÈ;f-pØn°wöäünÝ¾¯Û\x0003ßÉ\x0000\x0005ÛcÏEÁö,Õ\x0012býnAbhØ\x0011°Ë)\x0004a¯rn<ÞS6±¸L\x0013]õ±Ó\x0015Ù÷°ÂTC\x0004f> »áÁª
+ûUo{\x000e\x0000"F]Æ8¾¥¤o°Û\x000cÐeß²`Cß²w*¡ò°ù"Ä·@ïÞI {'B[Ý"U¹\x0001àòÚÑ²Së¾\ÍyjØ\x0019°±¼Å's|øÈ\x000f¥L\x0014¶åJtG°c'ìüãG}kñ\x0000giïº´·÷Vá¹\x0011=\x0015×T°o­8áæ\x0006L=\x001b&ã\x001ezgDvÒ'AË\x000eìd[;iÓîS&øRDÛÉ¤!Ü%Gf!Õëº»¦2\SA2¦°n~ØÑS)@|Ù½¹ºs×àö¡\x0018\x0001"rwîÿ!ètp.76Ñè\x0006F\x0019\x0008Ñ¯)Ñj3hïLÍJ¦ø\x0012MéßlRÿpKWt\x0017S\x0017Ñ
zs´"Õ\x0002Zÿ[¡Nð\x000cà\x001e¿f,^cp´x\x0001ÏU°J/w*x§A{a\x0013uV\x0008Ö \x0001£\x0013áQV\x001e'ë-®Az§\x0005\x0016NÝxÕ*\x0017nï¬âÐ*d\x0002\x001d©VÉÂYÐ¨Ãä±Ö
<h\x0002×A¦#*Ãà´Yn4f¥PRÁ»BI59xß1´{\x0017À-m\x0016Óê¢%\x0010[»õ\x000f\x001d\x001cGZå\x0018\x0003¶+\x000b¸a³ØF\x00006¸þ\x0001w"<õ1'¬ 	¸¢\x000fZ\±\x0016[.jj
<[\x0006\x000f\x0002vsUðaå5pXNº­àÖã6§¨$	\x00175ÒVÌ¼ò¨¶sW\x001bx»ê£\x0014¥\x000fòVôÎ=fKèe\x000búqqõ
vPx=§^\x0006'cMP4HÕmdVäèÿr÷þÛ[u K,Ç\x000cð j\x0007µØi\x001ae¡[\x000cô\x0012ÓµçzLcMµ1s°£{m,$³dXZÈ
J\x0000åì­§-\x001cÈ ZTü4\x001a)¤\x0003+[	¥s4lå]Ow9x×Àé¡¦°j\x0019?AÐ$w(Ðqk: ±%_ÞT\x0010/Î)«è\x0010í:E\x001fÛ|Ê\x001d4\x0010<b@\x0011®fCX\x000bdh6h\x001a\x000bWàÀÆ¦|\x0019\x001c	Í\x0006òJQ¿¿á¹1.ÏÓZ\x0017úÍÝ«¿-[õîáí­´Z½\x001ed.ö4x$ÿ-ø\x0012}i*/:\x000eæßf<î\x000c9v8)PËª|aâim¥\x001bh\x0013'mz¨´®1 \x0011»\x000eZ¹¶ÚÎ]6\x00074tÙD­°yL;[[VÍÒó1·\x00117óqçD=H­\x000fÍØÞ°TRláÌ,9tB£A\x0002AËxYÒ'Öo\x0014Z|\x0003í=\x001d)·»f\x0011\x0016oôpËTWof\x001b\x001eÐÀ6év¸É¶B;D\x000fWcMp-nÝiÆ\x001c\x001fº¾,Kñû¡,úªò9\x0007¼\x0007tVdjØ{¼÷xþ\´UªpN\x000cÐ¶5ÜçÂØË\x000cÍòNÑZ»y+ÌôV¨\x0013c%ßOòÆ~\x0018!\x001fM£høÅ<kð44Üú\x001añêÍøÒ­Jr\x0006åt~õûrçtßÜÝl\x001cZâN\x0012_CKEd\x000c,%Ä}¡q.i«q#Å¡Ê Dv\x0018Å4YôFÈ±h»CîU×,¿ýy\x0015r<u\x001e¥¸$×:f=¶\x0003\x001aõØD¼µß\x000525ÇqÞ­Ú7ð't'ÇÞC'zËl¨A2\x0012¥¯ª5Ù='\x0004\x000fh`f
\x001b®\x0016RT\x001b\x0013«\x001bÔ¶/¦\x0013ºs²\x0002l\x0014\x0013\x0017ûLVë)]\x00072ôJÉ´\x001f\x0010\x00121i^4\x000eUí1Ç¨'4,Z\x0002²§FÄ2\x0015ÒkÛR_;hÒ\x000cÇ\x0001qÎ \x001eÕÄÞn>²<Ï³a³ÐÞaÙÄ4t_ð¬kkÛ(Ô»ëFwws¡<v\x0017ÕÒêüê7hà3gj,Þcä;=1[?[ïÓÆv£']\x001e\x00042I²ì½Ø.\x0011ÛLø©ÔrB;\x000eP¶-^\x000e\x001fÇÄR:\x00059\x001f\x0002,\x001bè\x0000ÐR\x0003\x000bJ%fwsD·Mí\x0005{:NlOÖv\x000e°#÷_\x000b±k¥e1ÓöÀhí:}µ;¾äpû	Ñ¨bo»¾Ì*zÉ\x000c:þÅÞ{\x0007¢­ûÃvá]b°2\x0007\x0002=	D\x001c`Ù\x0002É³Ç\x0006>I°tð¯;¸Ge®bAÚ"³k¶1\x001dkÒ/\x001dþ\x000e¶Ag?	ùÌÎÏÙãb¬]\x001f_}ñýÝ\x000f?¾úòN<[5|\x0019\x00178!ìóI	t®Øª+¤å ²×/ã¹:Çeô\\x0016ÒLf¼ä}¹f 
\x001b"5déÀIåXoáÙi·ÓîIÍ]p11+ó¢8wªãÇ[cã \x0004o-Ü\x000bYÜ\x0010´W\}8æÐ-´úÌø.Uhø¤~äÆzLÃÈ²M\x0008Ú-\x001b5\x001f\x0003\x0016JY¶aaþò4³µCKÏÌQó\x0001\x0005\x0001r(\x0000ÜYï8\x000f^ÜD·f¸Øiî¥s	\x0013ø5eÊ\x001dêË\x001a>4)Ù\x001d6j#®Ð£ÇïOKE\x0003\x001ba¬\x0001\x000eYækô1Ñ¼\x0005½Óë¶½\x0003\x001b\x000f\x001b\x001cøåY<~ØÚ\x000eå¸b¥*\x001aD}²!¿¼+\x0007øf¼Ô¬\x0012¿d*ôah6dÌJáÔ¿\x000c\x001fÒçÅ,´¹ÇÂyä\x0012I¡·uó0Öñ Q)nIJcíüEV
wO\x001a\x0018ä6´w\x0007\x0003\x0011\x0003ìú!l/¿%Ó¡ã·1rëÂ jëNUKGU õzò²&/{·@²%0%¯ºäÔH¬ù§ÕlÁ\x0003\x001aËÃ	16
MIÆò\x0006ÖG
o\x0003-è÷Ç÷6\x0007î¥*÷Ü0Ä%l4|Ôt;«A8!\¥¡ö2\x001e(^°ãÆ­>°Á­Ö!PJv\x0002ChÏQ®j­üzAÎkÐÐooSªfkÃ=,-ja}«é:ßÜ'ÞE½ÐoØ¯¨cD`o»!ãªÒxlÜ®\x000b{¾Î­"s\x0017ÎâsÛ ¼\x0019å5Ìé§]\x001e<\x001cl=\x001b;Õ|\ð*rwÙx\x001a\x0018\x001du¦É\x0005Úq\x0008cjè\x001f\x0017Ä¿ÝÅ ØÞ]BÆáZU\x0003\x0011Í¦JD[1j*60jHAÒµÜÜÑÁ\x0017«\x0010¶e¤
@Q'ûOE¨0JTÇØ¹º%DÛ`'\x0003Ø\x0016Eï³ÕD\x0006O2{\x0002±½$/º\x001bÛðJènÔ!b\x0011-;ûÝlÚ<²\x0005Í·ACÃ]ñ\x001a0/åUÇÌ«whwTKJk\x001c»P¶"íò\x001dys{o\x0016CtÙÐm÷¿Ý8ýÌ÷ÙÕIzgHj!9"\x0003ÿ9ÕÒ\x0017ù\x0006?¤³t J,@\x0013AÊÎ¤§ÙËX¤ý~\x000e\x001a\x0014Hwf2+µS\x0016àZÂX¤-\x001b0¤-ÃÉ¤z¢Ì\x0012'äªL±ÈG5`ÈG\x0015ç! ð ¬W¼\x0007^²mí Q
½äâaN¹\x0001¸å6eÅfnZzUÏ9¿!Õsbí9¦ÈËRú\x0017ïÞ?üþFY\x0011!ô2Õ×I%'gÜÁTÏbðzk~.!ÅÂi­nÀg¡Ç\x0001\x0008õF¿F\x000e¼|8ôÇvÈô¥s\x0013×:5
\x0017äÄ|OßÆ\x0002-~\x001a²Ã¶ùâ91yÐ5É\x0007Mz\x0003\x000c\x000cl£ò"úåÜ;c¸Ñ¼¬¹Qwk~3c\x0002»Å\x001a0Eú-ì`Ö©´\x0010LË-G\x0004­\x001c"Á
­\x001c\x001cÿÚ\x00141´å´âÅÂ¥ËCþÉ\x001bñàÝË;\x0017¬JÃZi\x0005\x000bÍÑ\x0003»³!jW\x0004ðÓÁnlNZ_Ü´S\x001e¤|Y\x0016ådR_5ã¡ny³E÷VÃî­â@wàDw®t-ðëëmv¥¾Ýn¿¯¾
¨©s¦l@cy\x0003æa\x0003úþÝ\x001eý»ç£¿Ù£¿!ôÀ¿æ0z×7ÂEXLë¹Ð¿~þÚ·GÿÝóÑç1L\x0017ú7ÏGÿ~þ=Ü\x0001ú\x0001¦Énr\x0019F> ¡ö¶\x0005u¿\x0007¿þÒÿeþ/tßÂ {A\x000f|ßáõiSé\x0016ô×\x000býîùkÿç=ú?wtG³P¥ì¨\x00083\x000b^µÚ¼zØ?À7M\x0010ÉÔÊ
+Ýå£.6í¿}÷Í÷·\x00120,¥\x0015Ýñ;l¼ÿåFÆ,Ìºq¶+\x000fiz¹Íª\x001fs½Ü6\x0000¯TI\x0014g\x001bK}BÉ×ILs\x000fÅÜ{(Ê£ªW}";\x0016-È<\x0013Ï»6u\x001es@gXt\x0004
Ë(óS\x0006hÇ>2îV\x001dpÕ\x000e\x0002ø$\x0012Æ(»l|ÊMùX¥_gVÊ	m\x0001:ô @¦ b\x000f 3ñÒ§Öíµ[tEËi\x0005è\x00129a.\x0015\x0017'2¦*ü6WÀOh
Ð
ußÊé%zG&Ï®@×ëÅè\x0006£S\x0014Þ`¢¼Fd\x00072s¹ÁÖ\x0013ÚÃª\x0003\x0010GbÉ«3§øF\x0017Û\x001a\x000eèÞÖ`£´èÂÞ\x001bs^&\x000e\x0007&'½©Y¦¡fY°¹\x001cE\x0001Á±#ÏÀ	-ü×3ëÀ¶pÐ=Ò;
v¢ú\1	H5­]jî\x000b: ¦í\x0007j9ð\x0010:±6±CÓØÓs¯ë\x001d#ï?ÀX)eÿ\x00056I¨Ó\x0016Ü
\x001b:¹ea8FÃFu\x0010Aih\x0019Ð1'½ÂÁðw\x001fßßè	fb~\x000eÍE¹ÔQÁ|Z]ú³á-,1A
É\x0018-y:ÈôL}\x0007Ò¸Énk\x001dN3íè$rÄ©ëY\x000bõi\x001c\x001bs·hÃVhxËwt\x000e.L«¤ï !;\x001d-rÿ«|F hîfö¾UuæÚ\x0001í\x0008\x001a¦çÈ\=iª\x001a\x000cR©\x0005;Køt(hÌ\x0015ñ`\x0010I|ó\x001e5<3-'t"S£àL¹pß%öà8ú\x0010¨\x001b\x0016ÂØ° Ùz( å¬©\Y\x0013²C~¨ÉÓn ­¢­\x0007EÖ,|ôaïñªHÄ#\x000ec+¶ªcS`ÑqÈÕçYí`ü\ñ7o~þsUÒúâÍ»äÿý­\\x001a?ÛáFiû0$Êîb.$åÜ¬nøMÚ~.Ä1U½ù	ýúe·ÎÝ:&CòK<_\x0016öÞ\x000eÜX\x001b\x0016\x0002ö
\x001a¨ÝÊb=ÉJCI¢Eó@öÜ»´kÛñiöð\x000bõúì¯\x0003t	×Ï¤ã\x0014\x0002\x0015Á¤¶w5^c[¨fÊx\x0000}%·\x0001L¦:e\x0019@4ÏesË°ôËïÞÜß¬ù­|4\L×À4·èZÕ\x0000ïóñ	¦\x0003¥ÝÈ~\x0002$HI\x0001{\x0003\x0012Ë<\x001då*=OÇ: Ós¡gâ\x0003\x001aDËÿ\x0012\x0012>e\x000côº\x0012\x00002tJ-S½±\x0006$Q\x001dBq4Kº2ì|ÀÎM5`\x001eÍvPø¡6è\x00122¯²7Ü¦¸cUzËLë1ß`[ìá¥AáÙ\x000c]\x001e\x001bÕdÝµØ¾FV±3Ð&d¨¹Adn=P½½ª6Éid
\x001b¼Ò\x0012³`K4Ø³¸©]é´;d°Hm\x0004º§dIX?ÏàÜw\x0011Q¨¼Ô<ß`\x000746\x001e(ü¥	H;IñÞ\x000eËº£ÁÄÚQÆÿøJëWÿåcåc¿ªûb\x001bk9Ærár\x000clvÒ\x001eúEßèMc0ûjih'³ò\Aô\x001a'\x001dÆ4(L		2/Ëî\x0007rO&OYûÇ.äHÝB<áq¹®ý\x000eÙ\x00012mE]æ5RÉ\x000b²âO\x0016[p\x001c½æ¹Ýá\t/¡Xi@èsÊ²#Óc¬#1%Ñ-¨às³Ã\x0005~\x0007à¦r$/pO\x001de\x0005ôç\x000bøBº\x0019yä\x0008×dõïÊn»YÂ:\x0011\x0017Z´î¯d¦Rª?ºÌ?ÎøDÙ |,E{r\x0011aOÍÊÉw\ó\x0000ògíQU9%¼?Lµã\x0014-cç\ËØ~1f a÷1\x0003¶,°¥¡=\x00106mår®\x0005ÄE\x0019»b\x0007
¢Í@êwÎRSu2\x001bqrªº÷a5\x000fà\x001ekZÑö\x0000\x0018'\x0010J\x001aºA
:W¢LT\x000b}\x0018Á
\x0012©ëÍøèF®IëÍº£¤&Õ@ox8WÁÔè \x001aÕ!.(~
Û v\x0006²pÁN64VTÓ;Yp\x000fè~õJ1¦öÙ[÷¬ýeª9+ôfûEªóxÜ~Þf`Ç\x0001»RãJ-«bS¥Ç °·ÌTHUü1ÒõZé«~·K<ì\x0012\x001bQXÍ{öñ
ç]Í¢ÍÌ\x0018ÈvÌª$oï?|¸\x0019AqPæÖv?Û ;ÞÈäØ\x0017qh¬¯,Êñú]äµ\x001fòZ¹Äò\x0010ãÈhnçÞêòû½]6\x001dÐÐh&\x0019t)\x001bÇºä%\x000caM\x0014õ*±¥'A§Woþ×ûï¿zs÷Ã×\x000fßÜ6§''½M\x0011jÕmÍIªwmRêg3^`!­¼)pêâ±qûÏ\x001f\x0014êZF~f\x0017é!ú.À¨ñ]¢\x001f\x001aÇ$vEÊ¸\x0018¶2ò\x0016é\x0006bf\x001açD EÑ\x001d*ÜJSÞrXr}¡¦!e\x0003ý§ïÞ<Ül>\x0019\x001dÆzlz	ºë9Çx\x000c²ù|ãòO
qO¤IPQ¼\x001cÆ=ÆrEÐåQX¼\x0007
½\x0006ðò£\x001b*ÝÔo\x001fWaÏ	Ìoo `Oo¯\x001d?X­2Ì)Ü\x00038À\x000bº\x000e\x0005ÙÒ8c¹B%×\ÂBx°!§ì,è~\x0014dC\x000céò\x0012q)Ú%g\x000cé\x0003Z#£\x0000
=\x0014ÐÕ\x0000mW¹Ð\x000cÏîþáG\x0019ðr\x000cÝ©©Û(ì¹\x0012KXº57wÆ<^D#ÎÈ-
h5ÙgóæÎIïb4NzKA«÷ÂD¹\x0013Y(=sgmPG:}
m/hQ±×Ä@\x0011g}\x0015ðäè©\x000bzU\x0004¯ÒëCh[>óûûo\x001fyoõSÌ×bÎùJ\x0001ïedù\x001d¡F\x0000/pkêÊ\x001bøåÁ,ÖòÝæå¦¸¨Å·×ÎÙ*ò£1Ë"{\x0007]j.÷_¦ãÑ±\x0002MR\x0005Ú\x001eÃI7Ð=²(«ÎW×MAV	{³eÑì \x0007S»©\x0016ß\x00039Á¢	/Ð\x0011}Yt¶\x0003´]r±\x000eèÎÅò¢	d5ì\x0016Í\x0014Äâ\æáF©\x000c²Ýª@\x001dD	:34\x0003WzÐÌ:AÒ;$  Ë5@¤¦\x0002ìY­5¨6ÃdN¥7l
êÁCtTuì\x0003ò=ËûGØâåÖ\x0012À\x0004mØ= ìÍ^W¶Æ)t"`Í\x0006>¬Þ\x0012«Wuµ^ýÝ\x001fn¥Óª\x0003\x001eôþÜ\ÂÄz2}ëe<²:Çìg·éQØLÆ~Ãlxq\x001d@GXú±ìP~¼­\x001aa3!NÂf.¢ätD\x0003òUd>\x0001#7ÒÚLÔC»ü·­î¸v¤=iú\x000f¶vöNdÇkÖ´fÇKvÃíÊÙ;aPd¶Ð\x0016\x0014\x0014d\x00089Ñ\ºèSUÁSÜ×{{^õÐ7=[º6îÏ)î\x000e~Gà0«T²\<ó386¶\x000e\x000bGÀÚõ)ýòîýûwoß>È½\x0018ò<»Ò\j>VtMúHW	\x000cÍø|\x0000j8jm£&õd#Ê´â)Ua²²<»8}ò­í|`\x001b´ùo)@Ù´@GVSQü¡ªz§³&ÿÜùTÖ`!¹Î\x0004¥P'GÞ Á·
:ScíÀ&wVæ\x0014Ã¸Q©#cD)\x0013¼\x0008Zë6¿f\x0007­\x0001\x001açUUh¢|çLÃÒ\x0004:®ßÕ­©DÂg¢Ar\x0004)\x0007\x0012ö\x0014\x0001ØENË*\x0014ö,»÷¯0õPv\x0014§×tºdÊ­Xi×¢ýõ2QT6ò/þå\x0007P\x000f \
ÀIa?$¦\x0006"qÌy©ìy"Ãy\x0012f5\x0000[Ö¶SiCIÕ9¿j|ÿ¬SÀäIÚ\x0007^6qä/V9ÌÌç\x0003\x0019\x00148\x000e\x001aÆ,CÒ1Õ*\x0014lB¶\x00043óµÕ¨µ#)àNñ,\x000b§\x0006\x0015´\x0012\x0012pø\Òº{óñá§»q\x0012µÒäã{«»}rAbyàÝ\x000bù{&¬ê¤n.fº6×\x001c
¥¢\x0005yhMÂ'{ÜÅnr\x000eh\x0007d¤òtAä,­,¬ùIÊ2c¤¥8G\x000b
;\x0002½UxÎéý°é#uð¶ÖIc\x001eÕ\x0003;Â£Züö«¹'ÊÀ.\x0016Ñ\x0003\x0011m.ì\x0006:\x0001QÓÊXÌ\x001e@ÿmeZÃf\x000b¼l]ç«¥Ù\x00178°Ñ\x0017°Pò\x0016lÝÕ¢ó£èSJ;¶`Ïêç\x00076¨\x0017W°·\x0012Gù\x0014ÌýR«°å2«Øs/Õ\x001d\x0014a+À\x000e%U\x000cÃ\x0001lb¹s0|`÷`ø©[0ÍÝC'6\x0008ýdÝ\x000bQQ~\x0013KZ(ÏéFß$øÊN[\x0008D\»\x0004",2Ïe'ZÊ×7ËjÔ]uÔ¢æÿõñf,(^ØÁ÷îà[\x0005óÈ\x0012¯PÙÉ
Õt\x0016\x001a²N\x000fBCÑZ\x0008ªbUî ¹{Gô\x0012¿\x001dSg7Ø(oY#4°OPÃÔ\x0002K­-©Q>ô<_ðîó\x0005](OeÛÈÊn \x0007g[nö;\x001a6(Q\x0007ÚK±v\ I"\x0011ô$¤ë½3	­ \x0007èçJþ5&\x000blmß¥I\x0012Äi\x0010s(ÐºB\x000b¶7ÃNnØSRïÄî¬áÍNôÔ&Ù¬Ø¦w\x0014:ï±Y1©CèîÂ¶ºrRÔU4ÊÎåúm¡\_®ë×\x0000#ë\x0017<@\x001fób]Üd×F¡,È´7A'¥\x000co\x0016x³,¹qiåñ}ñîýýÍÜ½D/.=;¹]º;\x001d%nu¦\x001c>ýbÚ^c)T¹© )ºüº1UÑ<óï¯ìÊ<sW¥r\x001a\x0019\x0015ä»-±\x0015èz!ÌÙ\x0008uô¥ö¢hÅÀø¨`;R\x0004é\x0008Û¬
PN­öÏ?<üp÷öÛie\x001fÙ¥Í¥=æeß§+ç$ãs_ªë¢üºô°>\x001aY\x001f:ØÎÕÊ*&äéEê\x000b¾¶/Ì×Ð¬¡âÁ*Ô³ \x001bÆvW:ÀÂ=AÇ_XèàsÌ¦OvèÃlïÉÂÃTC{ºÎ\x0008|\x0012)ãÓ¾ä\x0018\x001b]Gí|T\x001b´ÁO3´Ý\x0006í\x0002Î\x0002(ñ\¥6©O$s#¦\x0010ÔjÍl\x001d°sAz\x0015CÈ>7JÄX½\x0019µY¶\x0006/Ì+Ó«ô!Ë {%"NöÖÎ»ãWi²ß¼/w@S¿\x0015ÝÀ°zHd´s\x0004(YÆö¡?JÑL&öCnÈGzÖI6§áIáÙ%&\x00044ÏrAmÐ\x0006\x000cÞtU\x0002í*cÙR\ß÷¶M|ß@ÃÀw\x0019FêÁðaAÎV#Ö©gj~Xý(È&Õ>méjªSe¤@ÇJ[L	oÐkçhëLâãR<\x001f*Ü9oÔÞü¨ö\x0016¥\x0019-\x00124	<\x0007È%\x0008Ý4u5lhê\x0013ú:wHg@ì\x0012}ÇX"ÅqÝÆ¯å°þþîíº%VÃ}Ú¤\x000eÖ`Ä©Y6¿l\x0017ðül%1ý\x0005lÍQAa÷\x001b\x001eýý«Ï±àH|õÅÃ\x000f÷\x001f\x001e~þ\x001f·ó¢\x0012\x000buÛ*°<\x0003å¿\x0001oÙÃ/Ò²û\x0018³¯S¬ö\x0015
-ÚüGþªj\x0017gã§W__øýÃ»ÿ~!\x0003gØÒ^<TqÅ¡A\ÉðÏék¬\x0002àJ>\x0000x÷#\x001e5Àßá\x0005\x0011\x0019ßÜ¼YIÛ%ª¼ÆõÅ@)K\x0007)\x0013SÜ¥\x0017\x001aP³.iÏb\x001bGe¨\x0017CôµÝïü	Ê\x0012Ã6»¡ääÂF|Dâ#2ð\x000eÔ\x0019m	ÄrJ©N	^\x000cÖ;\x000b\x0004\x000e0ç%Ê©á%³YjâCóÈ\x0003ÚñaÚ)ð´fÃ[!Ú6Rr\x000cCG&\x0006\x001d×âdQ\x0001Å¥¡ÎÛæx-Æx©1W*í`0"Lô\x0019:\x000fÍ/%Z_\x001c&oVïþoÞüüç·w7ªfæ\x0004÷\x0005i}5\x0016W¯\x000bºÚ¤.ñ"å½Ý33}	?\x0011ì×?áÑ¿êY\x0008¶ÿôêw?|}÷¡¬òÃ­n¶8h\x0016\x001by`.«\x000c\x0019aI&¿~\x001aÂ_ú1Ñ\x0006jÁú\x0017<úãW\ùEwð­òZ)n!\x000cÝ÷9Ô©'\x0017ÛÖÖÃýÙ0å\x0017ª
Ù4çê¯Am\x000722
¥\x0013Æp]¼"á»/³ÿT\x000fÕÊ?ÍëÒ^ä\x0006öí*ÏmýÊøøêïo&µ$E°Ï½\x0001¼8\x0014 -^Å\x000b_è\x001bo\º¹Ìã<÷î7<úûW¹¢ø7Ü&X§\x000e~¸¿ûx£;o\x0010TÌ9\\x0012=^Fl>d^Æ³^\x001fµ9mïã@zÚüÇ~ý²\x000fë\x0000vÏ\x0002^\<lYøòîáýÃÍT,uneü}~\x0013
¬÷ÅszvÍI["l
¹¨Ý³ü
þþUoÐæ¹ÿáþí³Cè\x000f7n\x0011\x001aÚM´=me{\x0004ÒZòËÐ\x0015ÖÉÙEÐÀ5ôÒ\x001b
\x001a£\x0003¸\x001aNß·¬7\x001dBc\x0012©\x0012¾!\x0015iÒå\x001c~«j¼«>AÁQ$)Ë©bÍ\x001e\x0002t\x001cV]	¶«>ASY¾âk|iJ$"\x0003ï\x0006UõuVm<jjã\x0001V°@l´4@71¯U·ÍÀ
ö2x3Á²Ë\x001dGÉê\x0012Â2ÿ'y³ë¶QS·«cNl§QCXºmxî©\x000fn¥\x0001åw¶ø*ïþ³èÛãr»DT\x001aòó6ùë.Õ\x000e¶fÈé\x0018Ï÷ù²\x001fÙÇºx0FTçhÀV	÷\x00076¦6¹\x00062¦±aÎHV£iä³òßäu*Á©\x0004©SBE ù\x0008ØöÈ§=\x0012Ø#:P¢ÍùèîÈ9P\x0005ÁéÜZ7«Ö@nÖÒ'\x0007«>
!s¯<\x0000©_-\x0012°qò >Júõã\x000f·£¤H>\x001eÐØ)ÈÉ(`î\»\x0008?gÿÁÆÁXÿGýâCÄ­ûðê·w?H\x0000u³À);S\x0016è¯ C8þnZ¶ãKÖ\x0004¡º|\x001c4«m\x0008\x001a\x0007K93ô¢\x0018MÂn%lj#=ç/\x001d\x000c¬\x0015F\x0010êDiªßiyFS±´_÷\x0014Å¡§È
\x0017«7B\x0015hÍrK28¡õüýªÝÅÇ.ú»w\x001f\x001eÊ¶9wÑ\x0017ïÞÿðNH\x0002·
ü\x0006Æh¼âoçËÙÉ¦µWÄ¼Ì©þË^²;\x0019lÇ/GÀÑO FÒQ\x0019BÆ\x0001,úh.dh$iÁh4D~Æsâº\x0016¬G'ñ\x0002>Òì¨FÜ	\x001e©®\x0007Ü´U/`U
ÙÂÆÚ\x0016Õ½²lÚû>Ò.d\x0018­\x0012\x000e?\x0014d\x0014ù.È¬Yç»óW$fC»^\x001d?ÿÇ
³\x001d&é\x001dÒú\x0007×]\x0019°ðjKÜK¨\x000eº°R\x001d?Ç :ãl\x001fª#³U\x001ejW&o¶¦\x0019[¼¬\x0019(I\x0007\x001e
Õ ê´ÅÖ\x001cälÑ-´{§õPªñu\x0010òx×_ÈÜ;\x0006úó"Cñ\x0002PÔy!½cyÕ<}7)åÿÖÐFÑC'¹Ñc}´éÈí¡+ÍXDÖÎc_³Q¼}«PÎ\x0018%ÞM\x0012<®|@  á©äÅ9g3ÛJ°\x001eß½\x000b\x0019zi£AÁg-\x001a0Ô\x0000<ôÑ5Rø\x0014éßMÚ>\x00059@[½\x0008O¾ÖÔ¢ÇÓOe<j\x0015×^<\x000e
\x001a·b®÷ÔUÕôÜ Ø\x000fÚcåï Æ.K\x000fR2wéÍ*xºÅóÉgÚAÃ!ô8½²Öb¹×:ð8©ÔÆ'M\x001d \x00174\x001c\x0016.°ö_Bö¼¡SC_Ò_'ø¦Uæ^rv%r¡Ê9üyå1ÇÏûõ¡q¤ppöê\x0017<úãÛG8\x0016ôæÝ7woä'MKr
yýÛÐÀÏ½ßßÉ§¸Ñ¥Õ÷
}¯\x00127ç\x0014°ÖT\x001cq&9¥Dß´.«\x0012gÛñ±}{_¾Às¾Õ3º\x0013þý]ù÷¾*ßÆLÆ¶|1S<[×<½YÈ¥Úö5æ^ÌN)Ïè$2ÿúþ3Iâi\x0006å>;óàWû¸â^*õ.YÕºyOË\x001aj¥x¿úÛwoÞ<Üj\x000bÉ\K\x0016*[êHK /åÞÔàbkl÷yØ(¸Glôw\x000f\x0005gV¼}R Ý¤rÚpøþÎg\x0011b¾öQNºMÿ<l×µøßÜß=ÜÈ4·ª\x001c7çÏZEÓt}ÙÕñõg²{´ÆlÉeÿõßþûÿùñýÂëxâõ¬p¼£²>]GK	åþ\x0012#òµ+]m\x0014/d_·ëvóôë÷"âÿ~¥xé¨ðÒ\x0011ÃóÝ²Biñçûî$·ÝAz9ËØÑ2_Ü½¿é{pÇ¸prúH ÔúÜqÑd×\x0004\x000e?\x0013»øÉ.â\x0010Þ½ROt\x0008#µ¹)\x0013ü©%´[ÐâuY´^¦)Å/f\x0019ëFËüï\x001fWcçj\x0017R*û3i)¡ÉÚî(')¥ÏÄÃùukp$³ü»oÞÝÈ*);CáC9-çÍ[NëÝ\x000bÒS\x001c«vãgb¸0Ë¿~É#O3¨HÐv	uàB5L	
ý5¾"kk'ýça\x0017ä²ý§òO~÷ê×\x000fïnvïÊ¬`tðK×íâ¯×¹¯-RÍ1Â@¡Ù¥ì\x001bÞ/1Däûå$-§ª¸w\x000bãx¾ê³Ù0Á)~ï¯ß=Üè Éq¡\x001bF÷
\x0013{ÅÇ\x0005ãåÌ\x0012F³üæã\x001fÞÝ(ÚvBôÁXR·KÊº³v¤­ÄN»eº^¾|÷áîÛ[Ý/åÑAYoåÊÅ{¾ÒFD_/]\x0005¯Ý4\x0015Þ_Ì0\x0011ï·7\x000c\x001cË^!N\x0007JMÈ^\x0001\x0002tÙ+1ÍR\x0013/f\x0015Ç»³ºõåý%ñö\x0001RÒØ3É^Y\x0019\x0019)ÒÝÝ\x0014§g¼u\x0002[§¸.%²þòÝÃwoïÞÞèò&ciq±ÎÖ»¸Q%L:&^\x0016ÖÑZu~[þÙï¬ÕÏÿsî\x0006y!Go¹Þl\x0017»ÄD\
)~>±µÖ\x0010[ÿãýû÷&ît	Bò¹oT\x0002xOV\x0019\x0015ê­üÆM¦¹õÅûr¶\x001eîo"`DÛ Ây!\x001b³×¡*V¬¥ÏÃ8{(oÔ?Ý¿x{;æèÉUsv,¢ªä¦óªñ-PøL¬\x0002/w$¿¼ÿæV\x0019qç,]1¶u\x001fþo6»\x0012\x0017\x001cí.·7Kÿ½½¶úÃÇ·\x000fß<üxÚé0\x0000ü;ñ÷ÿß\x0001þ\x001f´ÀØ^[}íà²\x0016®Ñ4òR\x000bË\x0013-²ø5?¾ûñcùï\x001eä*ÿ+íÍ+ùÿQ:\x001e>¸(û²	¾úáß>¾Ëoá7ß=üñFÛ\x001a­)
T[Óò"\x0001{\x001dÍÛ¿BxüËÑì\x0017d?&]&"æ¬_uR\x0004þ¹\x0012¡úoWHâ\x001aç&N\x000eaÇ­c'?\x0015ãk\x0000lM³ÒÚøå{ìÔ±£ã\x001daçë¶.\x000eØãÜÈðÕû7¿ûæ\x0006§äþ§W¿úáç?\x0017OöFÎÈÒý¢¿rq2T¼
~lc >íæq*º_\x001c9r¸¢NxT]f¼üà»Týñ4j@~¼¹¢mm÷Øö¹Øním°µ	U¤\x0007£s»dËªØv¡	½²s­\x001f\x000fÕnýu¨¶
ª¹I!NÐ£±Ð¯8\x001d*õ{óöÇëê\x001fîßÿþÝ»[9ø7çÑ÷ê\x0013ßÇ9Ç\x0015I¸J>ÂE{Ú[?qØ¢ûç=èUªÑoÑ/\x0001'£»wèò§g¢#°C÷!>\x000f}ÜüÞüáã¿ÝñòóÿûáþÇ\x001foõ¢x5¼(.º3R±Òò
©£Ú×ÏÂ\x001dqj|S±ä#÷7e÷\x0013\x001eýùuÆÌ¸ý\x0001=<\x0017]G5^ '|ýÓ³àÇ=ô/ÿþ.¼ýã\x001b\x000bËk0ÁÅ3M\x001d¢\x00101z¤«côÙ^Ê!\x0019\x0008fú
Ç\x0008¹è},ÖÖµ\x0005¼3+mffeUÞÞÝßÞ\x0010}®`W¡=W[A>;\x001b|j=ãÎ¼ÐußOFÏãåÖÑs|.ºQãÅ|¡Ëþtt¿ý¦Æ«ç¡êð½{ó±\x001fª_}ùþþáVIYWN\x0015eJÒ51Ü\x0014]6#L°6zí\x0013\x001f+«ÔJ06^m³Tî¸¼ÚÝOxôçWÔqÿ\x0000z~.zqvwèA={íÁLAî~G}2z´Sx~¢GkÂÖ2)<Û2iÿUÓó¿jNã­p¡çK¾û\x0019è[»çôl»kåvðõOÏ\x001f¯´\¸ûá_ûvãZ¡ZAÔWSæôô"¯Ãoßð^f¨Tíñ>KÓ©mf½ÙOíî'<úóe÷Lnà»\x001bø4ôñóß~wc·?"G_\Ã6o\x0015RË\x0014gâs8g/6©Ú³x2:¬g\x0003þõ¿vËñÏqã×nV«¾U\x000fí6?áÑ?}?þQ}÷ãwý{|ùîÍÏÿãV9f¯5\x000eI.wEÐ×êê¾êÂçcöÓeÝÌ$\x000f|¿¬w?á±_/o¤\x001e\x000e\x0017xÔþ¹ài\x000cG;xÒÏ\x0002\x001fwÎ¿§ôÓ7ì;ç¦->\x001e\x0007«â\x001cÉ\x0000Ò±åË¶	iÄ·JWL´ù\x0005ýöºkÆ-yaÇ«Kö©Øyô«:vvÏÁ\x001e÷Ì·æßÿí_ ÷+áï}|ÿÝÊ\x00129¦²NmI8²À\x0019\x0014 \²:Öú\x0013+®jdýRM«K\x0007F\x0004 zãV²Æ÷U5íç\x001fü¢t\x0000ØWéÀ\x0018\x0003J\x0001\x0005[\x0004I
\x001aÖkâÒ

pê»'lß×@Y^\x000coz'kûhû9T	íñ(\x0001vèØÙ¼6í\x000cÛ$iÅØÙäE\x000f°{\x0008dD\x001f×\x0012¶Å\x001abù\x0002yÀN:\x001f`÷± Ì#\x0005VÕ\x0007\x0000Uì "c×©WÓ\x001dÐÁû\x001dP>¦§+5\x0018Å\x001bªwÈü¹SÀ5gt:LQñ
\x0017^>ÁÜ*OØ\x0006°a([Á\x000eÐâ_±]æ¯i\mñ\x001fo/\x0000w´Ub?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-08.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-08.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹\x0007/^\x0003úUÌ¹öCYt8*:\x0002½Iõ*jL\x001f©\x0000E\55øBÔjÙæ¸¡YÔD<¿=
º¼
°æh)qZJÈÐiã)\x001fÐ\x0001 )q*âØWÍ-EÑM§Ä\x0001\x001d/è`±ô\x001c©°jÎÅÑ±»Wzg¢\x001f5ïëF\x0003úv\x0011[Äe/UcIîfªâ6_;;\x0015¬ß$¿='¿m;yX\x0019	1\âÃ}ÑKÏÁçÅ*¾ÝD+cÖ ûÙ#»¾¸Â¦Ã÷Y§«¤ºç¤º(¾£Q\x0012ÉL{a\x0015LV\x0017=\x0012\x0007´}ÖwwðÊÕ[+$ò+	Ûv8\x001aÅ&.ûÔíÆ*Wï9Wom%\x000b-\x0003o°("Yn^´h«®sõsõ-¼Nhí|ä\x0019:q¼=¹JñÝö\x001bþö;@¯½\x001bì\x001e¨Q\f©3?èL6Í´åó"^´å1·ãZ»ToÙ4Eîj\x000b©ç¤ù¼_ûçkÓdsÝ\x0019ßî\x000c\x0006dí¥à´}û*císSÀmíw×ÚÃ§1\x001a\x000eâK³ôICñ#K°}ÏÏ\x001d¨3¥Å\x0007Lpj¾2Ë4¸1\x0019w$8o<zÛí°\x0017d}ùê&Ó\x000e;Z}±cëwëo[ÿís¯ÒMúQ\x0013\x001e
ý"\x0017B\x0004¾¢zôNÝ§m»\x0007»_µ®\x0007a\x0017åµ\x001eoñºÜs¼ô´ùO|í×ÅÃ5VÛ\x0013±ñ2Iç\x0017u69SÕöø]étÝø\x000f¤Ñ¨w£Ú&æTSÙ5£àã·wËãÝò\x001eV£6I\x0011¤ýñ#£¼3iíë~\x0007K\x000f\x0018+§ $ª\x0012ã~·µªónA¬üÿÿ}£X«§´|yóÍw\x001f>¿Pò-(bV³â7}\x0014+6¶K{wõ¯|\x000bæ'³Çö¨\x0010¶­z\x001bJ\x001eÄÿ¹w[²ë8®E\x0005ÁwuÔýò(ÒÛÖvH:<¶Cç\x0011Ñ$ÛbÛ  7Ð²¬\x0008EìßØ¯ûÉú\x000eþÉþYs­YcTÕ\
u7\x001að%\x0014\x0014±rVefå==9æu¿åõ)Z\x0011Ð\x0010ÕÎqRÅq¬vn]Ð{BñA"XùSm+Q2(n3\x000e\x0007?·§h®ÔÒÄ£l2\x001aÏÕ\x001d¹í¨í[ËËS¶!M\x000eY#s
rh1\$¹-MÐ\x00132ÔÝÊs§,LG!ÎÀÑB1'ÃÚeÛ!¨"\x0006Ûskzá9
|\x0014­6}áW1D\x001f¡m:\x001ex\x0008l\x001ae×lºós\x0006Î\x0008\x0016Û\x0019õ=§ëK\x0018Î9­F,W=}\x0019¿q¨^\x0016ûuW'Z¶n ©na¿ éÜzPc,_\x001bè Ú@\x000cª\x0008·jü:ÁëygÒÖÖ¾±\x0010Mdç\x001eÕñûQê\x001f¼hfNC\x0014HÃÉ¬\x0019z\x001ajá)¹q98ûeñ	\x0016ÈÛ\x00188
é\x0012­¾Õ(®\x0006vô!2þ¨SY7F¦Uèý1¬²xða.Ö¾¼àý«o®ïnÚ¢g\x0012Ôè¦Âyþi<L×9Aä4½TÎMÃÅ³¿ÐÁã)±\x001deº\x001dúë"÷	õ ,÷\x000cÝ6ºÅ/Ãq8®[LB®Ë,ja\x0015üÛû?>`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?='2¸ÑáS\x001a²EdkØ
T)Ì]Ðt¶è«ÑvÖÙn<Ì\x001cxÓµ\x0004ä\x0012ØÈÕÒ1\x001e¬[\x001cî\x0010È¡</p><p>]sv	?Nh\x000c?ÌI°hÐ\x0019+ \x001a~¸ÀÐi\x0017"Èù\x00137Í8ßôØ\x0017ñ2À\x0011¯lm	ûy»²<\x0005\x001bÏ$¢xzxÿýRr)O!g¾ÑBz¾Áo/þ¸ÿ\x0002\x000fAh=;#çær\x001f-8!P®HÃiNcØµ÷\x000eG$¢\x0013Ûëxa,óA\x0004¹dÚÞÆn8l<\x000e,xä1(#Ó\x0014>v&×3r:±\x001d^E¹èîÓò\x0002'_º\x0017»zônIÉÉ½áÆ5âÅ8ì\x0019Uôí:\x0008
!)ËYOÔ
'\x000f{¢4ã5»>t\x0015Ü\x0006Ó\x0001Î²çZÚbI·MÊ¹%)wL¨\¤\x001f¬QYY{\x0000y¼\x0004ÑgtVSÐ\x0000'}ÕC\x0012{M\x0007¸%)\x0017(Ú\x000bÞ\Ì\x0014þÆ}ZÎÍi¹hFÓ®"ëô\x001c4³<åd\x000coºÌÀÕI'&hÓt&_¾`2»¿)ì3\nÎpin\x001døLSî,F\x000e\x000b|ì²\x000bWû\x000eÞ\x0018MZdå\x0018©ö.Ð©6¼]ÀqÛ ôÈèÌÍ\x0008G&U,kN/=W³\x000c²ÄSÃA\x001c,Ûf1Èým¦¿ ¶5</p><p>Ð¶þÉ«?,ç\x0003Þ*=\x0018ák¥ÂAV\x0006ûeÌçv1_KIÁÆq¥ýÇñ	h­|\x0002_fÆL\x0011\x0004¥¬ö=¾çøNñXr:kk\x001d}Æ«K\x0002Èµ\x0011þ3<Ã.ßT²ìvÂ1eÔ\x0011Å·\x0016\x0015NDÔÀ¿u\x001b4Èâð\x0019ao,Nß\x0015d;=ðÛØ\x001aE¾ýñá§_|³QúHwJÙp	ÉÔÓÒ±Äp©\x0016eùZßq
~'ý#]®Ek\x0017M¿kR8¡$1PK¿>\Bó\x0014<`îN%\x0008È;Ñ"[7¨¹ß,Ñ¿ÿåÝÛ??¼YjôÎìjôÇ/\x0017§B\x001ag´J\x0008\x00161§T6\x0014>²\x001c]£t<¬Ñ{oF~,ã_©&ïLáüêí\x000béO¨ïþîÃÓ7ÿá\x001fç-ìÌn\x000b»ç·°DÀ.Ñ¯K5øet:B>
\x00135WÑíÞ¿¥ÀØ
]¯qðÒ¸\ò³¿vÞh¯Þ}xûOÿ?sï²cÙqd\x000bþJã®¿\x001fÃ¢ªUÕ\x0017Ô-µTÐ4\x0011IÈP¥2¥|°(\x0001\x0017¸¿Ñ³FO\x001aêqÿ\x0001ÿ¤¿¤Ý|³}-s÷T2\x0018I \x001e`©¸Âo3s{.»ùý\x0017xü×wÂLøì«?üáîýû¹eò®_6/\x0006\x0012®>Àvü\x0016i\x0003KçoÉüúe\x0015Û""sêú[B+²=ò½¿vo\x0008:üHè´N?</p><p>Z\x000bÍ»ïo_~ÿ__L«\x0018ÚóúvÁ×ñiâÒBÓG©}Àûø\x0015¶æ\x0006»ýjÜS\x0008K{pÒCÃõvÐu\x0010Ãëüx\x0015ªøØçÝ\x000c¯÷ücsûè	\x001bº³g3¢`KË>A\x0019h·8oÙ%äaal\x001dÛí:rÄ\x0011TùDVaûya\x0016a\x000f\x0019w-4e|BG3ÛÂ\x0007'ãus\x0014OØq[úG\x0000[ÜçN±\x0010¶Ñ~±{q{{óÝÕÌâ\x000foÿúHoÍ¸mBrS®\/aÚx¥eUW¿Ïõ\x0018Y«?èq7R)²ãnN}ï/ný÷oÿøç?\x0019¼õG7+\x0005g'Ì¦Ëm\x001bÙd\x000bò\ÿÇ\x0017p\ÖÑõïý½³EýÇê¾U×þöÍûo£Qtñ¾°oM9½/+Î\x0005{~I\x0016~6÷é\x0017$\x0012ïO3³;õ½¿xºúï¾ýö/7LÏ¾Ù;ù\x0002_ü¤zz\x00032ùÏî@}</p><p>·×û>ßõÀ\x001fw£\x0004Þ·÷
b\x001cmÿÇñ{qL¥ýÜXç2 Aw#\x0018wflì\x0016ù$Ù\x0012ÍÐ~1EÐéGBç=t\x0006èNßpÆtåy"äô¿pD\x0017ç\x000eD\x000eÃkiîà(_Kb°\x00171EC3\x0003.eßÇ\x0011rÝç</p><p>´A·%7/Æ¡+(/WÒ;kÙ\x0017³ó\Pv\x0005¶tò"\x00049Z5/¡3x¹ÿqóºÉðcif\x000eL³ä\x000cO÷ÈW4ëí2:#ÀO¯±3W>ää^þ\x0007¹¸1\x0004râLÙHÉ- åXûµ5Ö{"íh´ºH</p><p>*O®A\x0005-a^K\x0007È\x001eÎGswíõy ZhÈ´5¥ÙÙ\x000eÁ½\x0005\x001dþ^\x000eÌÏ²LØ/ÌÔ\x001cá6Ò¹ü\x0012÷s©@ßÎlVFê\x0004\x001e&Ê\x0005\x0002N²àc¡\x0018Eræ\x000b\x001bu"\x000f\x000b%´8a<3ñ2\7¢Î`I4RZL\x0002rùâ\x00015¹WÅ¦\x001a\x0015 \x000fó$5Ö\x0002¢qØo\x0008\x0013]F{dë\¤\x001aÈvØ&\x0019S,¸áiº\x0006m
ßF\x000boW¶i.oÖ
|b\x0012\x0002ç9ãïèÓ(Ö,ïDy\x0012¿á£­QÖ)ÊXx¥KG}Ò¥@¿¶ôúÝÂ:\x0019eb£CD\x0013`Cæ§&:W\x0005\x0000yX§õ\x0011Q\x001b[\x001b2­¡jÈ1¯Âï\x0013\x0019b5\x0013Æ$\x0008w$\x001fJöØG%Ýó4; Ç/0</p><p>LpÏ´\x0015RÚÊ:²ÇZ\x0000xX§è\x0006Ël\x0017¹L'
§S\x001c\x0000r\x001f"^\x0018'£Ç%åæ\x0012ÇLÀì:êÂ8\x0019e¤ \x0017F\x001a"ÈVéÀG&ä\x0018Í<Õ\x0002È\x0015ÎìG3fí\x001dõ+ËY°¾\x000cd0NÑF|·dt;R\x0014OTN´9¦á6Ï¯ný²iýÍÝëÛg7\x001f¾oÿð¡Á=Z<ÙÀ×t&<Âãóó§p¡>2×½Û\x0003ß÷S\x0017ïB×\x0019ýÝÝ7¯Ûÿúáÿ|öêÿûÿÇ¿¯èÂ>íö[\x000cÌY:Ï >75~Mç\x0014~\x0012\x00176uÒ½úrSlÊm)£ÃTÒLL_ûÎéÎEË\x0012\x0000\x0007\x00006çº\9üsím­ËÈòDN\x00039ÖÑÒkÂùùL®q\x0016e_\x001a¯\x000bp\x0019Àó³Æ³;ïØ\x00104ä´±1\x0007ô°1Ò6fò\x0004º ß^\x0013ªR\x0018ú2¶û£À¹¹{åuC\x0003èñ
[d\x001eDuÔ¾Ú £ü¦qa±h\x0004 ÇGla°Uô¼Î>nwÑÏm\x0003¡sß\x001dsæ¨*Íò</p><p>t]¬\x0003\x0019Ðn|Æ\x0014"Æ\x000b5zìikÐ\x0014ádi	ç£\x0000y|ÅÔ"<\x000b²×¼úâ\x0010xû\x001btê1Û}E7¾böf\x0010\x0014°½9ùRUÎn&«ï¸Mä\x0017#ûå«f¾WÌ}¢\x001bî«¡\x00077»z>pÙÂÔ¥äg\x000e©ÞÂüQ^¸¡]äíÀ"#\x0014Tçè¶dÛiænS\x0000\x001e/gµc·w\x000f-Il£à`¦äµCkhËyCF{¸cÆ$oLÆqZÃl\x001cOCûÈ\x0005¹ùó\x0006¾!¦æ
\x0012XC¶Õ.ÝÃ\x000bòp\x000f7rq¯LÍ}\x0003Ú/Ø\x0014\x0002ídL*^´ÏÉò¡}û \x0001z|Ã$X\x0001¾aæ\x0006O¬w\x0012\x0017ç¹
\x0012Ç7L²d\x000e\x000e]\x001c=Ñ\x0007õ	ÛXîÌ[¢\x00013qtf«^¹.\x0008Ï\x0001:\x0003tJ}\x00146FBvF]´Yð\x0003òK°#\x00148´CzÁ$*i\x0012\x0016ç\x0000=$¯I-å6äaÃC\x0012ùÐi÷Úd~m\l>SÁGj\x001cÙÜÂzXÌ±f'ÓÎÂM'6UÜ;® dg\x0017ü5\x0000í\x0000:2tÀ©9vJ\x0013W¾\x0000
í?b<!Xð	Û\x001b´jåhÖ6Ì£¾\x0000úÑJíß§ôÊæ\x001dÍ</p><p>;¡vï\x0003D/ÒÈ}¿j%zfÁM\x000eÐ z\T\x0011ÝØB[VÒ¡ýN@<\x0008=\x000f3£¡^FfPæûÍ\x000fïoý÷ÞU· ¡ùÔ\x0016+\x001b8«ìGq»§\x001d!./æSäìBLáãÂ1¢\x00072\x0019\x000c7Øo¤¿ô2¦ÅBI@\x001eù¯ì3>½¡\x0006r¸c°ì87³»\x00010d©JÄ¼4tdg¹Ï'\x001fVj¡9ºÊ'F\x001b Ñ\x0013y\x0018m®{J7ò:Ò#ÖÅ¦:$\x0001ª|^åý]]çÐ/È¦í>ô g<²-ê=?f\x0017A²T\x0005³©\x0005s×¹÷%­ü¨ü\x001b\x0019M\x0001Â+Dg\x000etælû\x0016Uh\x001a94uÑX<)?RjÔX¾æ\x000bgÌâ)ÊsMÁ¨6\x0017Í\x0011²ªvAoä ×É\x000bd]\x000f¸®I*Àª¾\x0012W³)\x0000
b\x001bQ ¨\x000f­dn±\x0006p¡Ò\x000c\x00062ð\x000bzb\x00163/\x0000
©b.Yj^¶¡¬«JêúDÊÊ%Ê%\x0013f¬\x0010àÅulL6|ÏîN	Á%\x000bøý\x001c7KD£º%dcÃÆ!Ê!\x0001 ¨!\x0013\x0015Ðµ\x0011\x001a\x000e~\x0014Ýb½
@cßA$\x0007µ\x0019þ\x0014è6W\x001dúêC\x0016C&Iø\x000c\x0017ÛËN\x0018Ë\x00082ßºqÈ¢rÈB6\x001dë<5I]¬Ê\x001bK-£\x000b:(´Mp\x001b9!s£4ød¾°\x0000ìt\x0010\x001c=\x0019|\x0005 ñ¼èºÔçÃÜN
\x001d4\x001aDîX\x0004Ðr\x0004!'WÅ\x001e»Qwj\x0008N¤\x001akëíßÏO­ÜÓN1àvzè\x001ez©2A!\x001e¹öRáV¿¾ÓCðO\x001fK\x001dº]Jûhö\¥Nq³SD\x000fõäjð1Ì²Àzºî-ª\x001b¿7*¿7\6|*NtMòjf×\x0007mýN
=\x000e¢8\x00036ô¬\x0002ô\x001a$nZKiÁø\x0003Ð ÍYÇ0 p{D-Ê*õ-S~§\x001e;ý¹K@Î</p><p>n\x0013mg¶½:RLS+á\x001cIÃ!!Þ)àèÌI\x001fºs.ø\x001aú¡ÂzëÆ'l¡<wË%âÞj>Z¸ýN
=tu\x0008ÿ%SJ¥¦àêÔ½÷ÂïÔÐ\x000f5\x0014vZhKÌ{Ã0¨C~\x001f;-ôÐÖ!»±¸ÄèÐN94G%&ìô0@ÏY¤þ\\x0002÷ø§`øÔÕ/Ø\x0000z(¢p¬C:\x0015ËïÚ©mÔ¥Á¾Èv§ah¢
4Ka\x001dO*ùQjïú	;M\x000cÐ©\x0019sÏS{\x001e6©F\x0005\x0016õàÚéb\x0018ºh¹´Þ¾\x0012r·S\x001b¶¦5ua§!ÂÃe±¶.[\x0018µRÀf§\x0001±ùép!Y\x000bkÙÓÇ§îtÆa§\x00011pD$Tèx!í³ñ#`N¶2\x0006PF3vzõSWVÙV×c\x0019ÑN\x0019\x0003öXyêÞ*ZWK©Í0½¢\x0016wº\x0018.ê\x0006/`mF>P)ÄÈM9ÕöZÜéb\x0004]t@Gv86ä#q¿ÈÅ±;]C\x0017_\x001f±\x0018vlBô4BÑNÝÈ¸ÓÅ\x0008ºh¨æ*ÉCzpKPïëe¸ÓÅ8tÑ¤^Bg\x0012\x0018ü S\x001fMq§\x0011z\x001d×9«{ó]\x0002½ÓÅ8t±Ý;ÍMØÌv¯9d<Ûäzù2ît1\x000e]lá5\x000cffïØ\x001fËªkº^;UC\x0015
XæÖñ{\x001b8R>¥¸ÓÃ8ô°ý4Ê*·\x0014fò5\x001fk\x001dÓN\x0011\x0013(b·à\x000b</p><p>QÃ\x00102<ßÉ>ÒN\x0011\x00134\x001cËîEpm\x00021å\x000f©¼ØØÒN\x0011Ó(@×0ä\x0012æ*OWmÕP]ìoÚ)bcaÊ\x0005\x0016»Mso}ê\x0012{¶-í\x00141ÚvM\x000eC®öØ\x0001iÖ£¨S÷Ýñ;EL &ã«\x0017²áúYé¡KÚ)a\x001a\x000fÕS¹¨SÈÓCä\x0013§nK;%LC	e.</p><p>ßÚD+Ìe\x0002=r¬}N;uI8¹@3´©à^	ñNyðº\x001c=Çy'ÒÙ\x000b\x0019Ï=ÝñõÝí\x001bÐÊr\x001c9óNì2´\x0005`\x0010äÄ\x0012\åC\x001epåld¶t\x000e%Îi¬Ay^>bÞ}Ä\x000c\x001fÑPC\»HN}Ä¬~Ç¦i\x0000å®à!\x0004æª¥4aó\x0010Ô«eºÍ+»¯X,<-¹ëôùÓ\x0012TyZ</p><p>[T«ì>cñ`<\x0011Éwòòª¯Ö\x001eÌÝG,c­f</p><p>õ;¡\x001eibUcþh\x0019ØEäÖãÄÅ\x0018TÈ</p><p>ÉP×À}Ì2ÏÝó5	\x0007S6	çâ¥ÀÞ
%TúT\x001aº\x0008îÿBÎô\x0017¬5ä\x0014f[hÈù½Rû"4[n6ø¶\ICzFËc\x0017ä2¥Ù=Oq\x001dÉ!wà.#x0Ø¸&	qNMª\x001cN¿|?Ñ\x0010a²/¿r·l\£Zµ©\x000bÿW÷¤v§xzÙ_\x0000¥:!½à\x0011Èéü\x0012{Ìîù´I}ÚL}l9ÓºnÏÙ2£Yfÿ\x0007:·\x0017Ø2øéÎú\x001aÇ"Ù-8\x0017ÌQ±S-gÿvóá}\x001f~ÿh\x0003ÒÑ&UêÅkw¤2E>X.Ô\x000brIò?pîÃ:WU7T)aÞe\x0002À>*æì<Çòí«ªÜhìÔ®\x000bsy c/Û v­Íe3Ý4³L-\x0012í\x0005+ö\x0013\x0018Ó¹\x000c\x0016II\x0014\x001bò¶b?ù5u\x0007ñ^\(jÇ¶\x0011\x00145J"	Ó[;ld\x000fC\x0018åWb®W\x000bßöõ~ûêö\x0011©hlQQ×5æÌç\x0012ÂË\x001bû$"¾îZ_¸U"¾>ð½¿u-âVxû¦Øö".4ûýÞ±;ã¼®\x0007Á#°R*I\x001d9ñØeMë¹&C{{)$` +^L%?\x001b©Û]t\x0007iá\x001f\x001dÈ\x0015´\x0011\x000bá2)@ÓÊ%rÜ\x001cµ²ÖJ«´ÒJ³\x0001ÂÏO	ÜåRc÷\x0016\x0017Þó9ÁOgµ´±¡ç\x0004Õp@]\x0010.\x000fhhhOÖs;\x001eZTtU-%ÁûÕÏVÍ\x000c\x00074ÈÐv¤\x0018©Ü"&;¯»3´|¯ülø\x001c»ÂÒMóìQTwbÞó\x0007ø½÷\x0006ÖYTaádÿ_åj8ÆïÁW\x000e×%/xJLDâJ\x0018\x0015æ¥¡­¡ý	8×bç¾Ç÷Õ<7Åp-Æ\x001di§'"­\x001fij«2µÙîMX§Hyy§t;Ö;Q­m~\x0007µÇDy²ö	=#ç¼i¯ÊÖnnùÞ/´¶¶UY[É|\x0014xñ¥ï\x0008KB2Ú±ÝXÛª¬mi÷gö´Ö§Ù«\x0019÷Á|am«²¶%\x001a©\x0015dj\x0005Ìó±$uam«²¶Âô\x0018\x0018Ûùu uyª8+9Ó=B\x0014?1\x0016åiæ]·[Uf¼T éÐ0²Ï<w\x0007¥£§zi©êÂÔæ\x0018¢°¨©\x00108Çj&`¼\x0015Â¹:$(;AnªHqæ2GWò9Ú¡UÇ²Pl<9y¬ô~a}éHÜ}®\x0018k1\x0001¯ûtm¶T®î9åCk$Ûû¦Ëjª\x001f}(qT¨\x000f,Àpâh3Õc5Ó
qª§ÑzIr¹ÔÚu®Õ}º²ÄTTs_¨à\x0011³QtL~3ô­ºim\x0005\x0007¼ø-á9úEÁðäMómõÖ®G¸§7¡7iÿê¿w÷ÍëG"·\x000b9ªAÙ¾vÔ?ÀûÝ+îi(§ÜG\x000e­Ñ\x0016^û ¾¾\x001dr\~¬f±\x001d\x00010±</p><p>Ti\x0004ÖZnèÈ1ñÄçj­( cÉ\x0014Mz1ÍEÉ\2%ZÍl\x000eæÅÓ\x0019ÔÓÙâ	|,Êô\x0003*W*Ð,\x0012eÚ\x00172¶d}ú¥¬\x001dçioIÿ\x0003\x0005ÜÕ\x0004¯o¯b\x001c­3UÞ4`ÿå»wÏ~uóûG¨/´PÆ	KR\x0019ßÖÃð]\x000bßÜg¥ÉÓÒøò:EÒ¸<ñ½¿ve´\x0014\x000f×ï?<û\x001fþþîöíûG</p><p>S\äV\x0013¡6;'/¡\x001d¬\x0000>\x001d­?½Á</p><p>Ñ?¸¿ù¸\x001ce°d©\x000btÖË²\x0011¥pÊ3¦²b=aB³9ü`\x0001|5Ô<-Ó\x0004ìúÀêÂh9%&Q\x0019îXÍ\x0018evêµÑr:ç	]bR¨ öf\x001b¹+ú\x001c×33\x0007,öëÓì®\1w{s´\x0016{ÏÜj²å\x0008ò¡«>$|äå\x001fMÈð¼`,=7\x0011¿ßÞñïì-Ç{ðC6Äd¡o^,%Ú\x0012PòªÊa!ýûÛÛ×ïïnßþ4)àÌÉ/\x0019>:]p'üÞ	ùØ?½­}åÈGÐ[M9àPpKvµR>.«óh\x001c[¸à:Së¤.\x000eÉeijÅ7S¶¢ð£oW^gÏï©âU¿wÏ~ý¶YòGú¨5p\Êþ|<eÝ54ºJ)Ë>ã¹æ_|T¯>ª\x0017r</p><p>È6ÅÌáj#\x0013Å¸ùª^çßÅ\x0000	C`\x0006\x001a¾G·\x000e¬¼²äÁflÊ\x0012¢*ÊMVnPHiÞ~Ñ\¬\x0000¹É»ýðöýmsãnýòöÑÚOÍÇ%AÛÌ5TT1½¯êó\x0011pë üe»¡®­P\ùÞß»PT¯Y\x0005¢þöæÃ+á7iîÖcÑª¨»\x0019¹NCÐ\x000cm*O\x0000ÙÜþ\x0008õNosâû~ìtõÿLÏ2÷äU;õgpn#Î]\x0008!ÇÓ¸º\x001f·ãf.QZ(|æPU\x000boåx®$·²'ì"b­ã\x000bi'i´ÅVÂPÉëéC3¿¦_\x001eÍù@Õþ´DÇ©Ó:</p><p>7±ÅÑ\x001eKýµgÏ>}\x0003ÑpéOøâ#ßûsÕÍÛ/\x001e\ËôV<VÙfÍ_a¿é|ì«D§äp bCû¤÷¸S¸ãZ&gO=ÕÇø\x0007W3µà_ýâÏß|ûê{d¨¿i>ÛÍÝÛ»|íý¢&¼$Ô;\x0017mçs>®EFÅ-\x0019é=FIúdË\x0001Ø\/¨{C§	©Uf[2\x001d¼\x0014üÑ´²ÿèc'ñÎâ?	­*t\x000b¿ÿ'/äohsûâ?ÿòí\x0013ÏÛù×o^ÿáæ¯\x001fiI\x001eú¼bÅ¨Í ¥z}p5°Ø¶\x0016ixÎî©¾¯,&^y[E]ÿqCÝß:3\x0000íä©'V¯'/\x0005ó¬Yºa¨MA^ý^«{ô3×_d\x0012¨\x0004¸à
ÆöóäÛªV~\x0004\x001fÍü-B\x000b}ªù</p><p>\x001e#÷~\x001bBo±Ò$6øîUýæõ\x0017¼·â!±	®rªÃç|å²©Òï[ Ù\x000e¾'\x0011\x001b/sÏ\x000f%C¯÷Ãï_a\x000fi#iýV³óÆÑûïlofU´\x0017\x0008>/ªL4Å\x0000à\x0005×êf_-Óä7S\x001fæj\x0004\x0007sæ²Ãù\x0001ÙÆ</p><p>+íkÑ·</p><p>Ùùy  ë®\x0016öW\x0004c\x00108p%ä£\x0019,o¡ÇTd\x0013\x0003³àÒe·Ý\x000c\x0000½ª!ö¶j5_ÐcÂ°Ê"5XA&Ø0*dE\x001aüÕÛ_É\x0018ÈªÒ\x001f\x0007Ü\x001a¾Ý	DþíäË-ÏóÔ\x0014¹©\x0006î+ÑÇ\x001c\x0007\x0002Î|\x0001>Õy0°áà.a/¢\x000cx²ðÄ¯¹%j;°óiq«DYPóhÚÚ+Fvk]yÜöäÖáÉ-ºæ^þNÎÓÛ>ô)F«¦\x0011}Ì+WßÎ\x000eWcùè.ªïÙë6l\x001d\x0003ËUöæÂÉÝ²\x00075O.Ûc\x0005}{ëvLÿÖ¾"#kZ±ñ1\x0007ábô0ìo=îGjôÖ<g·Ç*¼9øz÷:jAGe\x00103\x000c\x001du}Mãf\x000c÷6ªß{Üê\x001dÀ
½b¥_örTFç\x0005Í'ì÷®&	Ý
ôb1\x0007Ý\x0002\x0018õU] \x0012;¦ÌlÜs\x001b=\x001dÌ¹|\x0012øì</p><p>}*öØV¥uu÷õ··¯Þ|dUîa\x0017 òØNH¡ Ô\x0003[¨,·Ù\x0005ÐRÓëÏÒm÷n	s\x0011W¬d&-kÆ3LÍ</p><p>²Òü\x0008 eõÑàLÌ\x0016=Î\x000br\x0000\x0019å$bkoQt`\x0019çYÇc\x0016AÄ\x00138xS\x0003Ï´Î¡\x0001{.È</p><p>1óc\x0001äH¢í\x0002<AU]e¥÷Ç²\x0019íbÈ	\x000c-ñ\x000eù\x001aÉ)o;µÛU¦¦!@Îp\x001b4á+qWÊm0íP0e^\x0003È\x0005\x001e\x001eÈAÚL-¿<\\x000b½\x0004ª÷nÁ^ûv$l£Û`\x0012Åp¡Z×û</p><p>m
½¸¤9\x0015 \x0013·:E×5Åî\x0014\x0010Ò,
\x001cåNHÌ\x0012?ÜYÚt°Õ\x0016\x000c|ó«2.À\x0012îGv Ø·\x0017RÂ\x0016ZÿÅ\x0003¶î^;ù?&\x0016>$ÓÐÑ\x001cdj®ZQ½Ë3³S\x0017G¸÷£°ïCsÙ´ F\x0006äÌÆ]0á9Ë4oS\x0008åàáÛ	µ­LgµL S ÚN²àvçØíëI´Ân7O_%ÛyTlÞ`Û\x000cR]¨«9·\x0007©¢]nZ¦Ò\x000fuÁ>òÛnUáB\x001co{À\x0011\x0010i\x001bïÙø§yÛ}|°\x0004Ü~Ú\x0006á8Æã\x000fV¼AÍÙg\x0003\x0000\x0019wé\x0008ëð\x0019û¿å*¹ÝR¬Öòy/jÃp 5\x0014ïÂ5[x\x0014Æ\x001d[±f»RÔ\x001e¨L;ûäÌdWô¾-1ZË·²¨}M\x00072Þ\x0006ÍxudÒ£öÂ-Èí\x00074>\x000e\x0006kqìíX5äí:7ØÂ_á¢\x0003\x0011\x000e·°\x0006ù=\x0005×ÉI	jmÁ/ÐpÓVØ\x001c_ ùÌ¦[¬½ ÃM»s\x0007¶E\x0015U¯=¨ÒlÞÜÍx\x001f\x0016ïÃY¢\x0014iØIÝt{.\x0016&«.ªÕÇ\x0012¼GJ^`xÆ±ÉéµM \x0006ë!\x0005»ÕJ?33Uµ</p><p>²\x001b\x0002"?é|wô¹¸ém§JÍTÕf*\x0000,ÄíßS	±Ê7é]\x001fS¥j+\x0015lÁ¿\x0012hc¾:\x0004«£\x001e;G!U\x0015î\x001b²A\x000e}'
7ÎÌy\x0019w´4ÏZYµý\x000b²J\x0019âë(rdv~$»´\x000cBªÚ×.fz\x001b=?î³kãµjÃ\x001aÇ\x0005®Ù\x0010OY©ï3s\x0010RÕ"¼~f\x0018nsMP¢ç33°'£\x0000¸Â-Ü²Ì¡ék·ÌVõèÏ_ UíÁ«Â"¶¯É\ád#Ç§-\x0010^%HôÎËr ÇÊ\x0004ñt)`Ì\x0000_SøßüSÙ¦Úûj\x001f6NzKg5MO\x0006Gz{\x0003\x001cR¬J	I\x0015`wiôÎj==Û\x001eÍ¢b\x001cÍé\x001a\x0000yX'#!Ã@6Í=\x0001¾vf5ðÓüÒ:é-Õ¶	Þ\x0017«\x0013Æ3\x000b01-­ÞÒY­É¸¿Õ\x0008ÝYÄ3\x0017î,´ÞÎC"àÌì«62\x0014:3oõv¥¬ÍÞÓÙ¾ AJGº
«Ò­¦\x0013öÍæIïé¬B\x0000\x0003½!\x0012\x0003Rº¡yLt\x001b~µ	+ÙAºÏÉ ¸'¡ãhÒe·Ø0Á>µ\x001fÓ¦NH9És·ì_ûtqá\x0005[í\x0005Ûö/\x0014¬'8öUM`2"	ÜwZ\x0008)\x0012ñ(s SSnÎFEöÎ,¶G\x0001ôPCñNa½@SUËD\x0016v!=±ÓC\x000b¹ÊìÐYñ{*8Pty±</p><p>Áw·´¦^=\x0005Þ©û¨ëäË\x0005\x0019s+óïË±</p><p>ì\x0014\x0015´P.ómÐSV÷|$vzh¡ÔT¸ÀghÜSÒ\x0018¼f§]NYçu.Ð×É\x001ejÌ©#ëï,w±{ßùÝN\x0011\x001dä*×ï2]t GÁðåÝ±Xz§\x000e³:D\x0007+§¦oèÕ{îÝíÔÐA¦2\x0017Õ\x0010±CïÔÇéÌ}î{§\x000eSJ\x0011âR\x0002M{\x001fú©wjèÀYoÆ\x0014ò«¾¹«\x0019¡ãT¶÷Çê\x001e=\x0008µ³»à©#îÒÜ\x001cÏ{ßÙ]ÜN\x0011\x001døëBKuåÊÏV\x0008IÕ\x000fè&:èn\x0008ÄÙ7Ýµ·ìyøífªÐàX#\x0007U;47N\x0004ÃIòv\x001bD'Ó\x001eÂOo0[á½C24ùÌÐã{ZhêQ9!J\x0014Ö|@\x001f[áÝ%äÞGâwÒ1èùk,ô	ÐûâçdEHý­õ»Oèá\x0013zªË't$x\x0007ZÚ'ìÖ4o´\þÑÑ\x0010Øêú´jiZÞU1Î
Ce¨ýð\x0013Oïo¶^õà\x0013«Bá
\x000fzs\x001cS7Sb\x0007Ç\x001cÛ\x0005ì\x0016Û"vûWFÛdµ´\x0000Qæ\x001a©×#</p><p>çÆªúÍTe¯^õÁÔ_¼zóXÉ§&Ãª÷É§aÃ=|4õ<Qò©Sº~Dý[Í©ÕæÿS¹)XÜì a5¯ª\x0012~èu
\M\x0002Ôv$Lå\x0004é÷¦wXß¥Y'Éõ0@Ê&¥Ë~)ÇÙ\x000bÎ4õÏë"¸¢+«2</p><p>¹\x0010Ês>2\x0013Ch75p5gÐ\x001fxpJbsJ"½\x000cj\x0002Øy\x0016á53ÊÉR.¬ôýVÍzâ*k'ÆLN44²i\x0002÷.¶\x0013ûu\x0001ÜªàNZ\x0016 M¯i!3ª²Ã:÷t\x0001±Ä\PíÈh]½êºj'v\x001aµ"WkïzÆ¨ \x001aÇEH	]\x0018ÚÚM%Y«uo\x0015ç?îÙÒ\x0012s¡X¤µ,¦µ~ñííî^÷ÔûoÞÜ½ûØ	±È¼ó2\x000cc\x001eî£]ès,»eû$ÌÆÏNÙ­ \x001a/*.7ãÈn·ííhñ»"\x000fã'+\x001cG?´èógÑxzÐjOÝN&êÌ\x0019r`jt)!ãÙ*C¾ à\x0001äa£R\x000c\x001b\x0011\x0013jó9Y\x0010íå\x0014p1A\x001e0jr¶v\x001b·ÌÇÐ'SrE.l°<pj¶?\x0004óØæ6lÛ¨\x0005IÔÅÎRÞ,Wn?í½E³Kââ¬Í%ùöÿëýíÍÇ*ÝGÚ%\x0013ë`\x0008®B±ââDwð\x0017|ÖÉ,º8¹%\x0001¤<UãÕCLt]±&³N;;EUÍe¿àÐ®ÔÈí+Çí}ñ¯\x001a\x0019¿øáÿ}\x000c~u÷ÍëÛ¥l|èó6§ÃFçÌÙ!bè\x00079I±ÃOcxÿ8¯3hÃk\x000b´_SnÐplSZ~ß 
¯i\x000fh\x0014ý-aÜ¥\x001a+\x0014\x000e¥×\x0019tYAæb\x0004äDm\x000e¾ª%íÂ#»ô:6é&\x001b\x000cgmñT{o2©Rô¶o ÝÎ Mº CÒQ¶¸9:³çÜ ³½\x00142ûa*+xGUO£úPÛ\x0007TÝDfæk\x0003äáxÓ'6UäÄnGVü\x0016îh@ýÃ sÿ}â\x000fì¥Ã[!/Øw\x000748\x0012¾ÂM\x0012Ò-~eFH×<¹96¾^\x0007ÆÆÉc\x000b»X:7w¹¶oÑ+e«¬ÁUª)k`JÆ¾y+«Ê\x001cÙ\x001fUÁ>5ØEh½\x0019</p><p>í
®R°í+`¯¤/UÉ x\x0010ì/e0býooþôçwby\x001f}>R¬(¨·k_~M±B,t~é\x0012-/~æçtÊ¿l·%îÌÈ\x0017\x001b^ë¹%Í\x0017ñ7\x0007Ã¿9£ÍÖè<ÀÇG.ízÆú\x0002\x001f\x0012ºM\x0013¾N\x0014ÈâùE\x0018óáÙïn^=ûòöíû»×ä/ÕôöÅ®-¦¾æãZ\x001edû<îH=yÿè úª+\x00028(ÿ·?ýùæÝ»£uëÒ\x001dñîÙïÄ¡y$ýò÷²ÆREö\x000eAª¥\x000cÂ\x000b¡aíqÓÓ¸3\x001fÃ\x000btÜrgÁ)ÒT.Ó\x001fã\x0007Ò\x001fkH.Àß¶Ô\x001aÀö§"ë¹\x0008Ù%F>	\x0017ÙyExÙ.\x001a÷pÈúÉ \x001aÈâÈ(#Ïë.ÀîLi^5ºØYøóñ1Ì<B\x0016\x000f3+\x001d G¸\x001e\x0006\\x000cMx·Ë\x001cT{³j\x0001Ê\ø·7w¯ßÿÓ»ùú/\x001f\x001e-Wâ\x0003\x000f\x0000ø$\x000eÀ5OEËÔ¥.â?óý,Y\x0007N>\x001bÊdÃs\x001aÍCWóAvíþ^!é2\x0012Ðú¤¦x¼.\x001f8;©\x0017äá¤úMJ}yð\x001dë\x0016Î,^¥æD¡É.ÿõÃ\x000f¬´ç¹ÁàÇX}ðþ9,ú\x000bBøúT5\x001d\x001bÃ|íSZÍ[\{(ë®h´ý*N%\x0005¿n¼ÏsG+­´a¡Ì-­\jÀëè.O-­âd[ºiN%e«k_iY</p><p>_,\x0012\x0003¿}óáñz\x000c}ä0¥Ä\x000f%M8y,\x0005z^àðf\x0003²}p%ÔqGJ^dÖ\x0010¾ªyéÀ¿X
Ûm²=&h£Uy¨1\x0012\x000b£äT_Eê\x0003¼½z>Ñ*¸­P$±PI p6 Éüúù4AÃöäg6<U¯J¸9-ó»\x0013\x0011u·³Ð\x0010\x001cGÖbÇu¡&¢®Â;½MRì¢\x000e\x000fÚøÒE\x0011*è"TSCxtBRIXOYtá\x0001[× ®AIÄ\x000b= E7\x0013gNvK\x0008¼\x0019ìÐ8*)Leðùdr+}<È\x001dL*yÆ\x0003\x001a¤¹xÜ Ú[BÈú%æàzyrÑQw\x0006¡[\x001b{Îfêð\x0006á\x00084´\x0012ù÷Î«f\x0003z÷\x0019¡?MÚ`P¢sU\x0013¯E\x0019\x000eÙ\x00148¥\x0016,fs5§7\x001fýÇ·ýÓãlËÇ²\x0006ëò\x0013ú^±\x000b2%É\x001c=3¸ãÓÒ\x0011¿
ª¹3\x000b¹¥\x001f®¸@\x0012m5Ô\x001aóAWj§F\x0001=	²&\x001a\x0016AP>Ô\x0016ÎÇ\Ý*¨Mì¶õn¸øýæÕÝ»G{-÷ô­qWÑO¸±ïèz²ÚKécª¢íôs\x001crß·y>@\x000eÄÈ\x000fVæ±en6`I»oÍ¿Æ´¿oRÃï&\x0002Ø\x000c$%í½5\x0012h2åÉd;P£ æJ\x0000±	7FE#=|ä´ Ò¢</p><p>x\x0019æ}ûÃÿóhì\x001cN=àÕ¡k>\x0019W\x0014ªS\x000c?H"é2 lRæÕ nÔ¼êÕcZêºNt8+-äð(µW&Ø¤ÄÂWYçE"\x0000¼\JUG¶U}$M(ÚaÇåX</p><p>#vëõ7í+=\x0016Ë£SÍl¹\É\¼ôqbI ´|º4÷:\x0013º\x0010\x0017&sÙúÞ_¼ÈB;x8F6ô'\x0008ä\x0014ÓGoÔ\x001fþXAÇ7=Ù°ØÇj«\x0014\x0000t\x001cg©{.Z.ÚkæØ;Í'º\x0002yÏ\x0005ª\x000bë^Ù½lCñW`\x0008a²Ì\x001d¹í%á|B.+óîæ\x0004Q/O=ûòÍ·/ß<VÙ¢É¯\x001a/;7$Ô([® \x0002ù¤öýc]Ibb¤îSÂ'</p><p>\x000e~¶ó¢\À<Q$~\x0016i\x000câ9Tµ\x0001Í\x001ds<³Cà´C\x0010#\x000f÷\x0017Ã	±ê	×îÃ¹TzR©ó\x0007¬ôfê`Iµ3Iè".èK8óÕ³\x0016²ÿgËi·Jeb\x001c\x001b²Ûhc¸´¼´ÃrdÝ°Ìòþ½þÉ«ÈújH»ï¶+hm½Nèøã \x0017Å?Øå\x0004½£?Mí/[ê¿5\x001dô¥</p><p>$«MüSÑ7|t«UËlE\x0003Êg)þe*wYU:\x0016.N\x0017ÿ¤é:Â}\x0014î8Ê¦ª»\|ß/\x000f¦Ña\x000fþåöÝ»\x000fï®uõGMt¸ úò5gçD/.wrR½\x000bÙ¥L:Éô²Ý|4x¥7ç¾÷7¯¾\x0002,©ûêæØÒú{÷§öã\x001eÉ©8`¢3.]Ýc\x0019Ð\x001b9ë$­rùÉôkó\x0005¦\x0001×ö\x0005dg=\x0007\·ç¾÷7/¾@G\x000e¢ÈÀUÃ\x0015y?ÈÕkÊ@Jóc¬K~ó\x0001¦g¦]®º¯O}ï/^\ñ¤\x0000ýäÍ;yóX[\x000b¤ÃÉTFa¬f\x001aFj?éÉÚd7îqvErõ\x0015ý¡úoÉ\\x0019\x0013\x000e3Î\x001cSãfJá\x001eØ*O}Õ©É¡8ö©öØb=ùS\x0017lb^¤ÕÛí_UãÝyÂî­Ó¬ô\x0015\x001bf¥m\x001e8\x000c\x0010\x0005KíÂ1ÃÅåUÊßR7á³_¿mÿ}óöæ÷w6,\x0013¼bm\x001aL0Âù	7/Ì\x0008O\x0017«íz\x0008gÓ\x001em~@¡$;aºTö\x001dÓätT¿Ù×õwÓ+{ÅQ\x000eO\x001b\x001e±=cKjvþ®ÇÇº®l:Øfà¿zóú\x000f2\x000eus÷h\x001d>2þÄ%tæý£DßÃeÈÆ=aQgóÐæ©I´ýpù\x0008yÔ.7ç¾÷7¯>?dÏþãÃÝ«ÛGÛR\x0013Ä¬ài1gãL{¥ºü\~IlÅgÿ\x0002sHçú8 \x0005þÍ¹ïýÍ«/àÈ¼\x001d\x000c|Ï~óæÃc-\x0003&Ñ¬zt.â_ÝA¦xõ×êAfôY/",hìK
AësßûÕåqÀýJª?½üáï_¿ù v%ËÅ{¿ÚIuUPKsc®#\x000c\x0012\x0014­rQúÁJÆàzm\x001d÷RÅÓëòí¥²!¨ÅTæÅìüGtóý±]Àkù\x0013áõ~%yæ~ÉkÞ¥Å¦\x0016nÙ«áµ9ÖÁS[dyuÔ~üâG\x0017=·$¡gÁ»^\x0012e¸åàåÌ÷ËÁSè»PÇvXòn?Ú-ö\x0012v<±¥-ÂRZ¸M4íÊ2rÇYÒ	;sK\x00027s\x001dQu*Ûô:ÚÑàç\x000eÛ\x001ezû¥XARM|)S{yñáûã\x001f9#º^ôòXM S¸`.\x0011·-Æå3[ÜWTùîº><Úº$Ðòx\\x0010Ëc\x0011Ö¸!2=\x000enI>«÷vÁ°ØvÈ£°{$7>k¥Yìm^ôYC?ë¥\x000fhª©yÓ>î_½º}öËvQ_?Ê7NFØé\x001b§zµ9¥'òøÆ¾vM~"ã{¸sÚò¸-J[¶cû1-Çþ\x0000Ø¿h\x001d;J«Ý<û\x000eÈn Á`ßÞá#Õ.3²¾ø8\x0013;\x0002°\x0007àHG\x0016z¥LÀ¡²&\x001eµ\x001dòiiJðé\x001c7wÕEF\x000e\x0014\x000b7L3ï\x0007\x0000²^|g\x0003£\x0000ËwÀÖ\x0019Â­Ó\x000evu ê¼Éo><ýZû\x000c÷ú\x001bO#ÛÞôý+\x000fË¶S²³	'_Gw\x0003(Pñ\x001bÏ\x000f\x001b\x0000Ø\x0017)\x000fZ2\x0001­`ë<]¥)vî\x001a\x0001àñþgát\x001c÷,l\x001a\x001ecá7æ¿Y°\x0012ì%W¶Ö#ud\x0003N\x0016ÚY²ìÜì\x001ej¹¹\x0013Yxª	ùX·vÈi QÖêa·_fý\x001d#§Åh1 \x000fo¥±Ü²kcå37¹¡çè­;àúÅñËç~â\x0001.s©<@{ÚÒn6É=\x001f«FvjbÇ\x0013`Gh\x0019\x0011-(\x001cÕ\x0018¶Ô¥süØ¢Ø¡(R\x0005sa:No\x000b7íøA5}\x0013´Ý©\x001d¯\x0011¦`xoee³ÃS+Ás¥.xE\x0001:ÀgôW\x0006.\x001e\x0019»Âå+²à9{Ðüì´eø<\x0005i'äÐ)bï};tbù¨ÖÜîdú,ØîSÒ;\x001eøµ5täö/«\x0001¸\x000c7-³\x001aÛ_[3í-`1X÷×¶»öv§.'ù§íCÔ%\x000eèâ1=ÜÎLK]b¸¬°s;uqC]j\x0019
}.æ2Ú©\x0003{®²!k&é\x0004èá×´_p6#</p><p>t°8"Ô iø¨A÷ÅMn'Ò\x000e\x001c\x001b\x0013;ð¶G³¹b!±·íúÈÛI´\x001bLÛ\x0017»r4'®\x001cL{SÊLÑ	ÐñÇ\x001eÚiZ\x0002¼k %h÷]òIÚuÆ 4Q\x001eªÐ\x0000îÿ±ø\x0007ú\x0002¤àÇã(c+(áÑ:~\x001c\x000fú gîù	
çÖà.2\x0006ÛÈ\x0014õ.d¯+øF¸\x000f0'¥³7Òø«»wsoÙ'zío \âõdZÆB\x001cnWô¢Ø¼d÷lÁËö\x000b-ØûÞß¼ð¾=ïT¼°JþÛÍ÷Ï¸ó±\x001cñZÉû¥§Y\x000b	}"'ûÙ?Á¤\x0003÷ n}ïO^Èbùïyì~þGJâ$\x0013%[\x0012c<cÃæóaöC³¨æÉr«×^ôËvEìEï}ß/æïîí¹ì¦
Øíiì°Hc_Ýeq,)?\x001b×Ä7¦\x001díÝ,Èj`¬_æ4vIÆ¾â\x001fÌ`§\x001aù\x0007¿à\x0005F÷Úa!eí\x0007Þ+e.Ëbú]ÁùóN¤Ú\x0000wR\x0001+\x0014³þ+\x001f=Ê\x0016À\x0007¢ìËÍ`-'nïå¹Á#{&\x001cþXSÞ¦}ô<í-B`7\x000bPïIy<¡è6d¢2BäYuÈ\x001eaPµ!çN\x0019ãì|°\x001dr\x0000äÊÈ\x0001V9sRÈ~"½@ä\x0008ÈvÐ.géôî9d83¦K\x001b²±\x0013w,"§\íàÍÒmì`rf\\x000eÞÄµöý¼CÎtæg¶¸V·Ùóû\x0017,;ä\x0002göçÜlÖN¸,K4Ìð³u:G`°IMá'dÃ×<Eð|à÷}¯U"x\x0006\x0015,q¬ïUà	ûçå\x000bbÙ¨AG?/OEhG§.\x0005NmÐ9SG>µ/óöT\x001eZhZt\u\x0011Zt»ÝÖ&4'¹N\x0011<B\x000f5´Æ6\x0012Ù^^±=¿A\x0007\x001c1l§vfcFè¡-=ÏèhÜ`àS9Gè¡.²IÇÃ©[H_èB)¿A§ÞBlwúb¾H^ßS·§µ×^Nhaê#h7oð@ä¡06Ñ\x0017ÛsEïÚI\x0012/¤G;±v\x0016 Ë\x0018ûõr\x0005Wx4h\x001bÉ?F÷)ÔFh½42uý>Ru\x001dÐ\x000ey\x001bä>Å#;Cí"\5Lþ	´AjQÙ&Ë\x001fÑ\x001dájPÑ$	ö&»påE"Û\x0005Ë¡]¶ÙBÙê´K÷bÁfsþúÍ«Çòsb¬ü}Òe&ZìJ°c¸[dÝ<ã|)\x000f\x0012.£\x001c\x000fûÖå¸\x0019é\x001cä§Zþª9L\6\x000c\x0006V¡+ \x0017¶'1\x0005<íGdðr\x0002\x0010¡7A-\x00132yf¡D¿\x001ag9¹·m÷\x0013ÅçDb[l½ü \x0003\x0010	Wû]z</p><p>õ§\x0011ÎPö\x0011.qÔÒRÜ ²jßÔg¤A\x0014'"ò{lÌ4\x000bÈ§´\x0004IMÃsÜn
\x0013yN¸\x0005Xå¬+\x0011ù N0ø¹(\x001f"h»\x0015çâ\x0013"qææÇ\x00070z:åÌ_G\x001cÙ#n~¨\x0019mY\x001aCXsÚµòKÂD\x0018Èi8Y:qs\x0002+"{õðQ^{Ä=â .0¾	WG¹N\x000bÃ/Z8Ð\x0011¸#7\x0003\x0015áó5\x0007(á%Kñ\z«Æâì\x0011^-#ÛÒ{ÑÇe\x0010Ç]¿¹ò\x0004ÐÃo
BÝàòm_.svâÅûËW¯Þ¼¿»mÖá±âv\x001bX B°Cå}oÕ:Ý '1P.¦Õ.7¤-Tµc)È!QâõØÚ.\x0004q¶#azud¿:Ú\x0011£B3ãÙBMÌ\x0007Û\x000cä\x0017zú×ñ¨Oý	7u´À3/)aÉÉõ¥ß¥Ó ÿô\x001f³¹D\x000fñ\x001d\®F}ÌÍïýµ\x000b5v¥F¿øöæÏò\x001féæ\x0003®\x0011kG±\x0017Î×þ\x0002Uðkk,OõÊôQJ\x0014­V"ëÑTµ9XÎùª®Në<ù":\x0010pô\x0018'\x000e×dzd©Ñêg¾fTüæ\x000f#\x0015D+*2î~ìüÊG«^ù*L ë\x0011~/GGÆ2|ù°\x000eá_ÊÅ}\x0012µ|å£åW>¶@ÿ¡Ökúä*­]òiâ«CdÈ{eØ¿Ö\x0014RÖlSÒv¹7äØ÷ô¹­d\Ù\x0001.nOøOV=!x\x00133:ß\x0003î´\x0005O\x0003<\x001a\x0007+ÝS ªÄhs7\x0017¤L\x000fò»g¿¼y{÷úöýûyòæ\x0013-I¶/ËùL¢Kâ\x0000òIdþ),IèËÇ\x001f¶$E?Ç+!,ä·fí\x0008­-IÑá¥M°«T\¬ÈÞ[v/±®
IÑï¼eXC\x000cS¡µâQTþ<É­ã¢sè6Ö±\x0007C¹ Ð¾;ûI\x000fZ\x001fáð"nÝr¾}jcRµQÇ\x0011û\x0007JêEcY?¡\x0018·ÎC¨È²ÙÍ/CIÓx1\x0015FvGsÒ*!v=6%Ädù
b­é\À°ü\x0007ÂB`,n¸xÇÀÔcÙ+¯ÞlëêÐÒò\x001cn(\x001eÝ:?\x001bi±¾hÕâØsúöHB\x001aÌ/\û±Çú±\x0006²\x0004ïÿ\x0001$«\x0007rÈ\x001c?dÞ<Ö³\x0008Àß¶Ð/þ\x0006àìBåW\x0018\x000b\x001av\x0015³U¿p\x0007FçöëÛG\x000b9½*TÎàYæy@hì±Zò§\x0017XÍCû\x0011.w¤Mqh\x0013G\x0006Xñ·2ß¼IËGÎêJq¾Û\x000cÈ¶rmÔ§\x0014Õ-æí²ºR,å=¬\x0013`°#[¼Ú¤2y½6:½rVW%\x001bu6fô3ûçú Q\x00139²[¦¬.ºö¤s\ñ6qºMÈ\x0012\x0017\x0001øÂûõíû»÷²tçÍã¹qZ\x000fO.ôM`äQÏº¦·Ò\þ$!áÇÚÅ¨EÜ%éo'¾¸Óã×rÎ]|eæ÷<\x001c9o,T Ú]¨ülµTwl÷ß+òxeYLÀ[.\Û(Õ)ä²z?×\x0002©\x0010ôíLw¯^ÝÝ.¦??Mj¤/óSé4Í-ÃJ¾$s>	\x001c]/ØøÞ_»Jàl	+\x001f;ãTdì=-f°ØÑ\x001e©ð$±×Ç:¾ZeûÁé\x000bq"ÿXyý4%ÀÄ	\x0014¨×¬<
ió%`·©ìiý¤#Ï</p><p>» «üêæ»7wo\x001f+ÉZ'Õ}k«\x0003JI)ÇÖº)B_\x001eøÞß:]ùÆüå··ïE?ywûêq®¼@"¶pÿZqOÍ¥À\x0007DZ@êgÌk{ù{ÙnG.Ý¿Ýïý¹«È\x000e\x0004ý×¯n¾¾ZÅ_ÝÜ-hH>UÚê\x0000¨e$\x0003Z0
õD©Õôs\x0012w?7u.O|ï¯U7¿x°o¸ýºïîô³$÷-l$sçð¹\x0010äöºº,EÒ©¦Ìí1ÀÝÍá\x00116\x000e[sJ|°w¸´ûã_ýâo/ó»ôý\x0017\x001fÁ4°ä\i¿ò\x0001vEo0ñÙ~\¾2
¸bj\x0019¤U(¤?õñ\x0019¥²öâ¼\x001d|ÏäÔ²ù§ÏÙB#äÿu.«_|4z\x0005³\x0005\x000f°òÒ\x0011'(Ù!d\x0003wÞ£\x0011)ÒØWô¤=ø¹Õ¤8\x0003»X¬a\x00164·\x0017\x001dKo65éÙ</p><p>»\x0005RTz/O"\x0012\x00115\x0013ïÀSoëLû;OãÎ­5Ýi¸JÌ$Ñµ8Cà"u\x0002¾¿4®Å:K×"\x000cµî\}Ð4U$~ÐÕ9%wóööëoo^=ûêöëW·o'fOÔ©öT6\x0018×¹'ù\x000cqÐÉ\x001fÆ\x001fÎL§¼\x000bé!ZËE¡ýîl\x000bqì)É¹H{Ì·Íµ²¦orj\x0001xÑJë<\x0018\x0018þÃW®©\x0004M\x0016Q"0Ú1#'ò(û®,Ù\x0000OjêÁ2-<¨e¾ûìljÈÅÒæaçh_>ì:U&\x00019\x0002r\x001e÷ì\x000c¶bf^ÄÑªt"</p><p>­A'p\x0002à4ºÐå2Ês»ÇõÞ¸)7\x0004¸\x0019,</p><p>(e\x000bÍ p(:\x0019vÜhææ#\x0005nÜäè\x001e\x0002\x0015Â\x001brL¤î~\x001e¨GàúÅ\x0003ªw¯ÚÎíø\x0003z,è:ÎLGöÌ'vqnj\x0002`P½àG2²\x0008\x001d	í±t^	éõj»Ó= '·Ö\x000fV8y&©µFL¶'äf>¦¹tD\x001el³C\x0015\x0011®\x001cQÏXZôË\x00034<\x0005&½_²²÷~7K\x0014H¯ÛÍÛ¹_\x001e Á\x000b´N\x001d\x0013¦}å>@7\x0005æÇ\x0001\x001a÷dû=¿!5ù7äP\x0008ÙÖ#U½û\x000e>¢Pqøñ¨W×ûöÆU[\x001c]iÐyõ0ª\Û¿Þ¼{ÿæµÌ¡þå±\x001eÄè³s</p><p>U:	íH\x0018JF³¨pæ§s2ÛG~°Â~\z\x0010Å¢Vx\x0010/E\x001efJôAÓ²\x000bïa¶£7¹\x0008\x001f){:ã±×\x001d§÷P-\x0010*R5\x0005½iî\x0018¿àNyáØµPvêíÜ!æù¸	\x001f\x0000:[É¦t}@`­.\x001eÆ·oî¾¿ÖÚÿýí\x001e+æ	Þ&¶mõôÏl
ÏÁ*f£ãþtîY3¸\x000fæ\x001c»Òî·£[Ü3*+5û\x0012-\x0019\x0001ã´ê\x0014Ñ¼¤ÎÞr}×|F\x0006ÁvÎ@®½3Å¹u\x001c8;:p|`~/sß9{gsK\x000e\GM"Ö\x00141r`ÖÌ\x0016íN¤[\x001cÉÇáï8©</p><p>f:sPw¼tÎ,\x0013\x0013íäí^Q]zgy$«á;%ãé[«`Ò\x0017Ã'N½\x0005cáíX¦\x000f)5Xó.¡¤c·=Dö®/dJ\x000b¯Ä2ÇO¥{a@7÷\x0002É3?h®H\x0017neº\x001c¹iX\x0014(N§ÅÝN¶sÚÛ¢\x0016nÉ\x0005\x001a\x0002÷ö/äqhg±H]$Â\x001c+b\x0019×^e&\x001e9tFÿO¶L\x000f¼çpÃåîØÙ\x001d¶L#Ù\x0006\x0002"³ªº\x0005Äï=Wnwj7NÝ^À®w×\x000biÏ%DKnN[w¥vvpèzÿì+D7èÊ÷Ñ¢¨¾îqgFý0£Í\x0016\x000eÎ\x0006m-ö,µ¯È±¨éèwænP\x0000\x000bQÂ\x0018L(Q\x0006jqGró+3=¾¦\x001cÍP;öC¦]µ¨¥\x001aìÍ¼®g£z«Âî\x0013úñ	½xí#]$íÈn£°a2±\x000fjä­e\x001a;©´û\x0005°¥Ö\x0019º&ÓÊ4-ÝÖüÎçüëÌªð.B4`|9Ó¢M\x0012Æ</p><p>v5³öOä±Ö\x0007¢]îFù\x0008Â}APZFv5z¾r\x0013ç¥\x000c\x0016[ftË@\x000e#³\x0007hRÛe\x0000\x0019ôÆÃZ´Ü\x000242«\x0013-Ô¶¡#p\x0000#Çð|\x0003nß³@«]\x001brðÓÒrDNlø@Õ@MHe¢n\x0016mÅ\x000eÔ[edþèÑòßçÞ53ÒÄ\x0006"ìöà¸'\x0012nÙ=ö1Âí½\x0012nÉOÖBg&+(Toü{rrÁ\_cÁ¤H2m\x0019)Î6øºNÉ]!%¡?¶\x0008g+\x0011dÅ\x0008!Û}³g\x0017dÈ\x0002J#»*?Y8lþg]ûf\x00074fÎ\x0005Li\x000cW9­ü¼)\x001eÁmo^_\x0004h\x0019Õ§\x0016Ãp¤¹v7\x0019#\x000fY°\x001c\x000eøhX\x0011e9\x0010\x0000\x0017³î¹Dö\x001c¿¼í%®+E×SRÒ&Üÿö#ww}D}/9òj]:\x0017ZtBî\x0002ÁdìÓèz»ù</p><p>v½Õº\x001eò\x0018<Aä\x0010ûTøâÓbf\x00191*-\x0018á	ùgaaÛ-;âW©yËòí³_¼º¹{ûÝÍï\x001f+á¸ä\x0015"d0$\x001b\x0005)\x0019!F©?/\x000bn'\x000bn#\x0015B¦\x0015%Î{\x0018Â1ã¾p¾ýôU=¾gM\x001chñ¼ÄíäÇ\x0006\x001b×	\x0001Þ ñµ\x0003*O/u	Ç:ØëÍû\x000frpÊ\x00074Y%u
?\x000e-ÜNÈÝ«È}#\x001b÷ÊÕ&r×¯CdÌûà¦@ÂÉÂÐå\x0008\x0017Y\x001dý<8;Æ_\x001a²ì­¦ûHtÑq\x001f·ëÇÁùá5È67JË\x001fóWëÝ*uiÖ£AÿüòííUÿÛ§j¼áÓZÆGmA ¼¶óÁ?¾KgÚ\x0003\x001c;ÒÅzÔÎIàll´çIY[q£3ÝVØÔ\x0007°18¡&×¨ÂÖÖÎ !â\x000e\ 7ßo¹ê¨?ÐÊµ×ðÇÇ¯n>zòÃ¢bsåÒ]²ît[Lâ^</p><p>ÓMÍS\x0008K{¹\x0017Ã,,Üúº?ó½¿wuó«Ä²Ñcî\x001aû\x0011îVf÷ÚøÆv=àÔ\x0000ÂSßýü0G½xsæ{ït÷¼.Xö"\x001eõ_¶\x001fÕÄÿîÞÆRÑI6¸ë*ûÜ|ÿç§­\x000fÅ?]Êfíéz-÷%Á\x0007-óõÌP6\x0016~\x0010KùösK¯¿8\x001bÐ#\x0005×ÀÁN¶óAí³Sd\x0014­×KDúwµ\x0011uêæO\x0008æ¿Ý¼ýýc\x0019³æø%\x0012°Ú»N\x000eáFRpÁÚÿ¥[èÏhÌ´\x000bö²Ýj\x0006Ø\x001cúÞ\x001f¼¸yµïË¾}ûË7\x001f$QôX/¯ì\x000eúGøÿ¬/^Nù¯£öÆ\x001cìÝ#jß\x001cúÞ\x001f¼¸|\x000cÛ¿ú	ëÔEåÃu
c6LJòóÏÚ5¡]³\x0000;Á*%iÿÀMy>'ò üQuúºB;Ho·o \x0003(Á\x0007W8Êk»3\x0010Íúz@{(vL~_\x0008P\x000bD7.9¤cõÔîÔPqòB\x0001Ð¦ª¤|É]J§MAùâÁ¾øon^ÿð+ \x0002hÚç®"<ëcAºµ\x0019W"ÀaýØEBu[üéÝÐ1þÁ®xa+çßüâO_ßüõö{ÒÁ>\x0000£õÎ.§/Ê\x0003ÄíÎXHkjhNGÂ´rn%PÎ*b¡ëï||«çËYÈsèr½.igð²;õ½¿XKÚøß¿
·ôì´7ÿõ#]{Ì×ÐJ¿æE\x0016SEÓQSÈþ¹KOrëB)öPÔr½\x001a[Ú¡Ê\x0003GíÐRí÷"õHû½Çf(¿ö?\x0012:Õ-v\x001a{§¬À\x000b\x0003»!\x0004X+ÔtEìfn'Iùó\x001f¾ýÛwpë2õýN£OÓ»¦­&zl	qÑp*¸ç,HÕd¸ø³i«U\x001fà¸(¹¶¾÷\x0007Oào¯Þü¥®RÑ¿»ùðõ·s°\x001a¡þTÝõJyó@©\x000b«9[jÒè?£îêopÜ\x0014vf\x000f\x00063Åæ_\x0000Í(\x0018®ñi¿·\x0005S½°Á.\x0008+ïxYcöØi,wÝ²ÂqðßÜsð3²ë\x0001ÃhÚûvñ\x0016ø¢>Õ×
\x000b\x0001F¯A¿½{ÝÝÉ»ýD½
¦ÒÏôÙ_÷Vi</p><p>>ûk&Óø$z+>è4½Çõ(­õ©\x000e²³²«ÏQiKT\x001fµ¦yò\x001bÝ\x0000ör\x0002§|´\x0018\x000cdìÁlÀa*\x0005àó\x0011\x0011f$ÐË\x0016ê\x00003V2)1n:æÁ´»qâqàö8Õ!)"ýX2¹8~B{0\x00018\x0003;#%È)dºcYu?Õã\x00019
ä<6@´'/\x001a¤mG¶YjoÞ±Ñ2ïó°åH±,û+\x0013Vdê¢-OÇ·²C.ãÈ-\x0010©ã}5¼+­ý\x001féSõ3G/ ×qæ&pn ËÝ@aD:½,Ù¾fú\x0016s2\x0003z,¬Nê\x0002|Aß;ãÆ¡½ãëvÑ\x0000ÐCMdY\x001dßÐ{%kÐãæØ¸y·\x0004@\x000fEéë\x0010\x0007´l®.¨*í!ñh/rK[\x0000\x001dà­w£1_î:b~UÞúBÞV¬nnw\x0005ä¡,2¼\x001bÆUÛZ°w;\x0019j:lÀÇî\x0018»S\x0016;ÅÊ&ãqäH¬íÈÏÝ¢Û\x0015¶Èö</p><p>1g"îµvæPé6BQç~
\x001eêbmÁ\x0017E´¶1KÕN½¤;}\x0019'wÕ½\x000fÝ<94 Ç¶¹*d¼\x0005Ní\x000b6×¥¾äN}ÔkÝN_ÆæÉÚwo7}Áð^Öº0rOk¸ºÍU¦²ÆK\x0018k</p><p>è;É}\x0014¾\x000fÛ-Û©\x0003u1\x0011ã@D%u	ÔÝÔN\x001dz³¡Ûé\x0003}\x0015°rêf</p><p>BûÊ\x001e®k\x0017$Ð;q	T1Ñ©­Ãþ4QÅPØ~\x001cýÐ;q 1°ÉW¸ÒwQ\x000e}´C»Â¸¡0²n	<`[¨EMÖ{¶L¶w!¸Â8P\x0018Ù%1\x0004¤xK'\x000e¤í\x0005-sªnàzÐG±ªÊùsz·¨­XÆHó¢7\x001c-Ø£p\x0014\x0019TNth\x000e\x0007ìºô;=ô\x000elÅC·SÝ³¯g«eÑx\x000eÐïy\x0008Gæ\x0005ÁýÔô	­ïÓSJé\x001e(ã¢f\x0018¦¾æ\x0019\x000fÍ7\x001d\x000e¾9¿SC\x000fj(Í/ã¦,«léui^\¿\x001azPÃæÖUh:\x001fÜ¶GH=¦ó;eñ ,Òª\x000c\x001f±ÙVºèÂ¾X8ÈÃN¦\x0001d3:üÛãBv|æcí|Ø	^\x0000Á\x000bvltg+ô\x001aHG¢·EB#ÞIG\x0008¤.nÜ´®èJÐCò©?[a÷\x0011C"pjÙ¦QØàñãúF¤°û¡-\x001dÎ©¬*Ç«¼[/Ä\x001f¤ã»»p×MÖÇ%à^. S_vuÇÝ]Ç@ñlD­R\x0003Çn1¹\x0010V\x0018\x0017º\x000b\x0019ww\x001d\x0013CSRÙ[oÐ¡ûàrÜÝuÄ»6c\x001b@{ÖÅ\x0016Î(èÞv\x0017\x0002é¢×¥\x0005\x0014úÂjnKZp\x00004\\x0004\x0015ã®eI\x000c=ä¾\x0018N®7ï.$¡\x0005ÉÏý°{}ÑeE'	±®\x000f	å	É>ã°{ò</p><p>"¡@³6¶ÈA+óN®3Ú4Fµ®6z:µ9\ß¼û\x0019>£,e\x001cì%§:TôdËNÌ&zF{{´?É[Ód=° IÜ²b¶ÌdÙ\x001aeáÓ\x0018\x0014KîÔ\x0008ýOaM%/(ÁfÁ1I%µ¤§Ë\x000c¸³ªà\x0004\x000eôV³=\x0000\x000cbcÜ\x0018Gª©¿D¤ýÁó=Ê\x0016 Uè\x000cÊo<55LÈ¤üÂ¶¼Lå\\x000b#ÃÃÓ"jGf%¨ç2?:ëþ\x0001
	O:´ò/MT\x0003IRÉùÅÍë×VÄñÊN8SPºÇå$lÌ|\x0002ánqÉ
Í¤´Ë{uâû~ë"a{â¢?_Çàa\x0003ÎL¢§ÙW'\x0019UÆö\x0004>¦ÔË¾\x000bpLsÈ´e>.»EÊöD\x0003¹\x001a\x000c-\x001cÝxËfMÿzFÿ5\x000e\x0002ð*é\x001a®ùÊq9f{V+rÁ\x00073q¤\x0006Ýü\x001eËqá/ú>ÏàtfzÔgªÁ©\x001b9xÁFâþ\x001cóx£éÌú\x0016X%¿jr-\x001c ¯\x001e¹*\x001fb"\x000b!8¯¥¦"¯QjjÁG\x001fV\x0002ÝôXÿáÇ\x0006U|\x0013Æ¾á±¤\x0010"Fòâwq.7yY7\x0000\x0001Ü"\x0011Èäú±\x0005©Ý£)|.®Ênç¿ß~øîÑ|\x0008Êö:Æa\x0001\x001c|É\x0018e\x0016þgT'8xv'¾ï·®\x0008ºñww+
sÏ~3\x000fò}g\x0015ö>[eîÃÆ$kêSu´Ä\x001eì\x0005?îo¼»V\x0011Nl°çD\HvK¨)Ö\x0015Nnð¿<\x0012Ã\x0019¤7Û[W\x0013ßcÝ8
¿
ÙC©Bè`\x000cZUn</p><p>Á¬ÝLkôù7Ç­Ü*eÃ{\x0007ïÝ£5Æ\x0018O¿Î%çÏà§\x0005nD²Ò?gÈ Å¯½A_Ä</p><p>N5vC	6òÏ½ä`wÈàW¦à7ù3\x0014kF~ï]Êó¶9@\x001eÙL+E\x0005ÈûHå[y¸\x0016îÒ|\x0011¡°|\x0019d<=Î\x001fKcÏUéäü	\x000cÕßæ\x000b\x0016Hu×\x000b\x001c\x001a0­n\x0012ä©'õ\x0005\x0013z]ÃâÿýÃíë÷w¯\x001fÝCQ</p><p>¥Óé]za</p><p>\x000c%6»×ôÔ>òq½G\x0013W;r>Ú½®\x000eJÍcj¿ÖqZ¶ø>\x000b¿0³E¹>UvvCcF0){d\x000f¥¤cÈ2£r\x0001ÇJû\x0003xÕ\x001e*\x0002\x0002\x001e"¥8\x00072ó²ëè'\x0010\x001bÕ²f\x0013ÈÍ±þùì¯<X©~N¯säÆckEÈTïjoü\¿\x001b«ÉÒI\x0000­4RCh®V]d^\x0005´'2´±¶Ð\x0018D='L¸7_<ó\x0003V¬÷\x0002p\x0018GözX¥xÒØg\x0016u©.ÞçyoðzÛ§¶ÀY®\x000bù4²\x001e±\x000eî\x0011)¡^ùÿl\x001eùToOGTÕùÍïû¹«\x0008\x0008'd7]«Üx®J¬¥³CæU\x0010þ\x0018nÏ\x0016â."#£-
àtH\x000b\x0015æü¤wm´kCà~@LÂ³2&må\x001e9k[êdãÓ\x0017\x000fïq¸{÷Oï>¼ý'¹°/ôÐJ^îr¸®ámKgTXÕ`rÅ¶È\x0001½và ¥\x0010Zõ\x0014¸ÍOóÍ®øàåßÿâ]ù¯?ß]ùçïÚç½\x0015wïfÃcé~¶ºÆÚ¯×V%\x0004áÖ°pCEÓà/~l©n\x000eïÃ\x0014!×KB¹î'\x001f=Ùíäí¿°%?\x001aÛ?¥ò»\x0008@	Û
ì\x0006ØÂ\x0005\x0013\x0010;aS[Ãvy^mKØ\x001eÎ\x001dO</p><p>\x0012Á¶\x0006\x001bxûÇrm\x0016Ï\x001ca\x00078·?}ºM=
;bL°{~5î±#{Ôh\x001a¶T;!\x0012hØ´l/ú87Û\x0012rS\x0007º\x0011c]nÛ$FIO	:Aâ
.\x0006	"åÐ¡\x0017ý¶\x0004]èÔ\x0011®# µ\x001c\x001aÝ \ºÔ=tS³ÏO°eë"}Æt
;ö%ª\x0002à×\x001aP?w<\x0004\Ê\x0006\x000eî\x001c_I\x001f´{¥´¨õ,.\x000bxpêVj ¥lQG;z	ÜÑÉ¯­ïýä\x001e}Ú~rÒÊØÞ¾¹§À=\x00130íÍG²mQËÈâíãÏÀ\x0003Ù\x0000bÊsúÉó§m¯=\x0016´Ç»Ó¹\x0015ìq~¤gÃ\x0018ÊÜKØ >Ñ>\x001fæ$Kw
Ëaâ\x000b·ÅÍ
¸úsî%¾H#s";ØE\x0007.a\x0002EwÙ</p><p>¸p&Ñ¹3KS\x0017äýí\x000c;Ã¥xZ:Ð\x000fÎâ»ýv{ýq ?qÌ\x0000ËsÜ,«O!l!%\x001b|	\x001bÔÇ'p{,\x0005AlUlZôø\x00128¨O\x000cgû\x001cü²Ê\x0005N^Ù\x0007) Öí\x001e\x0007OOÌ`j` o_óâøá	\x0007ù^P\%äÉA,¡\x0019;ô\x000b÷ûéñc\x00164Iz÷\x0012³1\x000c\x0007¡ßM_3?¯\x001eÀ­zÙr²\x000cÞ;ßüþkzü\x0015ßdùNX3«>QB\x000e$\x001e^\x001fñP2\x000b!?\x0010¶ÓFú½øHÇÆ\x000b·\x000e;'úÉùÂ_´t\x00128Ø+yË\x0006xl6<B\x000cêÑû£1w/\x001eÄ0x]\x000cRÐÊÁ\x000b¡¯½%<ìÅ0X\x0002\x0007\x0019o¾\x0002?\x0010
<óÁ
hû×'Àë\x0013Æªi\x0001,"y\x0013¶æ¼õ¦ÀýÉ#¼ \x001b\x001eã÷'XúÞõæ¸\x0017ñ\x0008"HÄC)|ð`Y.[zâ^\x0010#\x0008b»cxïC</p><p>l
\x0003
ØK\x0014Ô\x001f·¸¿òÈ;pðMv=îIêà~nÃ$ìBØ.ÁÁËsvRås÷´8!_<\x000fGE¦öKdpÏà\x0007îÞ\x001c&GJ\x001b}è\x0010ý|ú®ôùªÙìtöõjÈsä|Ví|ö»öÞ¿`Õ_\x0008çJ\x001e½Uþ
¥*q×ÓûþDHÓHþ^u
\x000buuáåþ5
/^3</p><p>AbûoTùé(YÒWûÃÿøÍH\×ª¾{öo·oßLåÐOÍÄÈav4áü\x0015íæí¸¥&=ÅýDIf¯ã©¾ë5é¤k\x0017>ô·HdMT,\x0000°a¸\x0000lO\x000f \x001dâ)5FN.Ì7Zâ¼ë°#y3.Ã\x001bÇ\x0013· rÂ%ä°¦\x0001\x001b\x001eW!\x0011-öÕóÔU¸; 1Ü54¶a³Ió6+ì¸H\x0001|Üw{äÏ)~'	\x0007ç\x001a¸ó%Ø/v²\x0011x\x0004ð\x001f³de/]`[s{OQ#`gÂ§µ-öf¼ãÄ\Gö³\x0015Ã[!+ö©7sßlñX¥ÖïGe}	ÿDÒ\x00149éEøÛëúÝAýâöÝÝïo__¬ÙHÑWeÐÚkÈO÷åúk©'Ájû5BnëÐ \x0015ë\x001edQ¸Þ2hV^\x00108yIìIµ0=)\x0017fæ
Âvm\x0003t®ìÐ·Øl¥³ef&hOÐ\x00106\x0008J²5löuV\x001dí\x001d\x0008ÛÂ¹ÅV&Âf£ãúªMm\x0015\x0000zX\x0005çì9Ó¡\x0003ø4èÌ7búT´öZ\x0001:ýHhmo\x0000:ÃøçÃ¯l!#'dÓ*ü\x000e$/@\x000fØB8éÃ±2y\x0000{\x000e\x0011l)sW
\x0001GI¸\x0006
cGºÀ\x0011_Ãö«\x0014ï\x0000\x0014o\x001f)ö\x0004Nùc£Ê\x0017¶ô\x0012ýôæ\x0001¸\x0005ð±ªgºîlëêä{\x0014¯HkÔÆ-à|ð®5Ós</p><p>ÐþG</p><p>àß\x0005ìðc±÷:	/µLùG÷BÁæB\x001b¬áçÔåªëèéÅûò¯ï¾Ú\x0017~Ý¬ô³\x000fR?ûòÍ#\x001bgÍ©òìòõ%òåBtu"¥"î%</p><p>)>¸1éz[ü\x0012yq\x0001 \x0019QCÅ=¶¶Ù\x0002O\x001f9û¥k
Ø~`§«Ú\x0000,aä\x0018ÛÏ-\x001d\x0007v°¨¯õ²Bx|­\x001cøkùþ^hË\x000bØy`·p/VÀæÊÉ)IèýóÚB\x0002výâ\x0001I¹WÊVFl[øÒ¢;â$Y\x001cç\x0008<è§°ª>\x0000ø8y\x0016\x001f\x0000w\x001eh)7ï¥CJkìÝïííï§9«±\x0007õW·oo¦OTØ\È>¹ì/\x000cÍü\x0018{ÚØ~fõý\x0019\x0004ÂÇM)¿QÆ~k\x0018'o0l\x000bkªjÉ)pùB±Ç\x001e\x000ct9¸H»²­ GÂ\x000e=K¦-\x0001`\x000fKPe-¥'lúp\Y°ãª;\x0000°Ã=·¶2\x001dáÜ\x0007n÷\x001d\x0014IøÂ+sór,ÂN?öÜÚÁ\x0003ì\x0002Àö\x000e®\x000bv»^r3iHNRJ½¨\x0008>ü°O\x0006wÛk±\x000e®Å{Èë\x001f"IÄ)</p><p>¾¸õÛ³[o~\x001cúdÄBù¯oÞ\x0011\x001aàÆ~ö¯7¯^-\x001c>Õõ°ÜôÓ=ôËÇ0\x0011¢æ'õTÍS2çÍG8\x001eÇ})Ç#W±d~>¢PUq(,C`Àvðb«W\x0011=Õ¥[\x0013¶ÑÎ;Æ	\x001b\x001aáu\x0014y"¿Ãq\x0010rÙ8<Y\x0001
>­'\x0015`\x000cí¹1¡\x0008=4^ÜüáÃ×ßÂ`\x0002ÐÒ\x001e;\x000b\x001eK(Û	IUª½°¡5·Æ¹LÖðtbéÝ{×®\x0017¥\x001fØ\x001c0ä\x0011ê\x0007¬µJ28ó^¬\x0010%l~`ó\x0010\x001dÓ¼3l¿k_3WÆ\x000eó\x0012QÂ\x001ea Ðþ\x0000çæÒ\Ó\x0008J\x0007Ë¹\x0017ï+@Ãû\x001aÆ\x0010Næ¡([aè\x0005Ù\x0000a±EF,'!Òu\x0007uì45Û¾øczÿºW9</p><p>¼¬êèÎå¯ïnß¾&\x001e?Mð¥iÃõhóå\x0007E\x0006/Ìö ©}"Áo"ä\x0016k\x000b´ä\x001f\x0017Æ¿;ù½¿zþ\x0014yù>üerïÿãÍ_g\x0012OL\x0008oH:\x0012Â>¤½Ì{t\x0006=U×oèÛ¢\x001f¼ü~EÊì4AÇL¶týråÎãQÑV\x0007 ÕñB½6Â6i¤sXUp\:\x0013\x000eÄÑ\x0001hO§\x001e½âhÖªZÕ ÜÌ¨@Ø°í°\x000c²\x0017Kºìdúd:	¢¶:àJLoª^7ÊõñúXéuó«Ö\À*QI'\x0017nïúMÜ£g¹&\x001eÝ\x0000Ú©\x0007èBÇNð%Çá{9vâOy,éÐÁ=`Ä­¿°<Ç&Æ\x0000©=¹Êçî´qSÀ0À!q«\x000fnçs»òÑ¢7å<\x0000ÜÒcÿ_s+Is\x000c÷ÇÒYé¦ä*`£ÉÖÞg\x001d;M\x001dsï¬sXe@\x0001<\x00128dÞr>ªó\x0008NØyA0KÐ(\x0001|Ô<n_\x0012duß\x0007}Ü\x0006\x0002ìJØ\x001e;\*!Èç\x000e½C|êB\x001dàÐÚ\x001c\ì0jA1Î²ñçyó©òª\x000b\x0015À-Ü\x0018</p><p>?å«.n¿lC\x0005pG'§>ºL-".³mgÉ«.TÀF1ô\x0018Îd$æýÜÜSìs'mÕÞ\x001d`\x00078w:i	zÌaè¸\x001f\x001bÆòQÚ¸tpèÊûä\x001bçrst½»pJ\x0014\x0000x¢Csl/ ¦|ÇE\x0015PÆ»½\x0002¹L\x0007>Ü^\x001fnã6^Y¬¼ %p°ãBQ</p><p>ÝJÆñÈË¬AÞ¥\x0005é,£zZ´µ©:m²¸e,Ô.,Söd{C'\x000054Ók-<Ð+Ñ\x001ce_1£z\x001alÒk\x0006QW5ïUü~ÀÝ\x0017÷{÷:«¶bÀ\x0006õ\x0012;4§ÀcU§B\x001fØZ\x0001:\x001244>¥æ¼%fOE</p><p>Aÿc"%pV h\\x0014ª\x0013Ö\x001fvøÝ¥ò³W éà\x0006îD¨séÉ¯ì«dÒªg\x0019ÀAdîdøo¾\x0014\)ÖÀ\x001d;YÎUÏ2`þÈà\x0010tå\x0007¢Éè\x0007'â²:ìõ'þHÍ\x0004</p><p>ªº¦ï\x001c\x0015aíX5D\x0003¸¥C¯hò´öZNÎ\x0013\x001cáH¨½þ\x0004ÇÏÄ\x0010DÙ©\x001dØfQ²ºEÝ¬½\x0002\x0005T \x0019&</p><p>Üçjà;·Ýi\x000eû\x0007.@_7ÑqÕ)÷5ò,õ\x0007\x0019Ö^?C¤;W_ßªçóûe\x000f:`£zÞÑ~Áî\x000bÓùÊ¹§½_x¯\x0001Ù\x001c>û-zR\x001d;åÂÑn\x0013öú\x0019</p><p>|ÜµFég¦hVXo\x0013Ú+h¨$,	Zó¥
nUH²n\x0012sîõ3\x001a:8X-!X \x000e<¸ÜSM\x000c«¶\x0000·|pp\x0010#\x000fÈ¶³£Uz?ÏÔö\x000fØ¬APUQ?ÌªÛç°lû\x0007ðHà\x000eÀC}®°9Qú¸\ÜËaÌ|pö¸ê csãvêo~ÜKJdIH%êqç\x0006®8JO!ì¿f¢¯	µÊé\x001aIÝ²ï)7ö2á§L8\x0017MÑ/''>|'\x001bNû/"aÓä	-½éØ|n×+wiÿ)Sfpèè©\x001b\x000f¤n¯Ûb_\x001fW\x0002\x0007\x0001ñ\x0010õ¸1t×¼ÿÙ\x0012´\x0005h\x001aÎ\x0006U¾\x0014ÓÃÂ¼ÿ¿&äUB\x000bÅcepno=Ffòþsf\x000c¯,W²½"²frþ­=èòâçýçÌ\x001d!lQuÜéôìÉ1%÷3câèäË°\x0002Îoé#meç\x0005ÃeÈ~Ä*;Ô­ÐëSduÏ4­ñß~_`Zã«Ûg¿}óú÷TBh®5ý>k/ë\x001cs!ÆçeÜ»P@~Þ\x0012ÂÔ}ßïs¶»ßû«§y÷¿~ÿW¼ùwÏ~wûöÅ\x001aÇO,\û¤±¢\gdZØU\x0010¡é-OU¸´¶®h´órÜ\x0011çÎÚ3'å®\x001c]øþ<þìX¸µ!÷\x000eÖ)\x0003àPö\x0018ã¶{IýKCE{>rìsSZa{<yè¼~Wpë{kß8ybÍÍ?ä¦\x0005\x0014À©t®âßo~øû?¼|u÷óôSkP!ªrÌ(}7Ç
#%i\x0019HéÉËRù"\ÖTª8O[bä:Q\x000béxv&t§]G'2ÆG·×¡OTä|\x0017ç/«YµÈyxZÎ\x001c83j:óL\x0016\x000eÈ\x0016\x0011£Ò¼°Ê\x0000º^èlt`w"CXç3± Ô¢n#pÃmì^»N`ÌsD?²á	Z§\x000b</p><p>µ\x0007/S	ç</p><p>\x0005\x0016{,Æ9ä°³\x0012\x001c²lVÍñ'4´ÆW\x0003c¿¥\x0005Ð\x0011½\x000c[\x000cÏ<\x001d\x0019Å©ýDOh\x000cM±\x0019Å\x001ady@î\x0018	ÈINàôc¼û@\x001eâÂ\x000fú\x0012çlææòÍÝiÂäÊ\x0015øßÞÜ½~ÿì«7\x001f\x001e«!-\x0018Ï3ê1kGZûýêZi÷×T\2M?Ã!;\x000eþMåÂÁN4[©¨­¬Ò\x0017A.\x0004·`4µJÊk+\x0015µ]±H\x001dT\x0014é¡¥7rä²\x001a:Gh!\x0004¹\x0019Kei!¦ö)Kó\x0017µùsæÍ\x0001'¶\x0016SØÄW¥÷\x0013\x0018Æ¥¨\x000f\x000el¹Ýl\x000e[¿äÖv5j»*cGX}4+OÁð¤A<Vé8èD®pd\[íÈdUºLÖ\x0006;jíbÃâ¡IPù°×;-r»nCxù\x0016nñcÌb¹-@Ãàbµ|èÀåö¯¨S÷"ÍTÊ?¡ap1\x001a,Ñ43Êm¿µT¥=Ý9\x0015òOhÐ\x0014á\x001e\x000bÛ¸«èçm*äÐ Ò2¿\x0001}*1sw\ÍÜÆ\x001a\x0004ÖTÇ?¡Aô¤Q\x0018\x0013U	}M\x0016¬9åóCãzh¿ýë·Öö|¸ÕÔ»Ï$G\x0019é;ª×«éøG´Ê
éWÆ\x0011mMd*Ù)\x0010J¡Kâ¤>Wdð¤¢%¾ÁTÙ·\x0019TÚ«33\x0018\x00032<`:UJPõ6Õ}]MoÈðÉò=8râô¯UU\x0008Il¯Þ¯+0\x0017Êv"¼æÈ-GÍ\x0002ª#÷×|zÀ®Èi÷æfÃõ\x0007d\x001exì°Û!ºWw2Ïö3;9L(|\x0014d§'ìOXB¾Há¡àYâÂ©Ù\x0014»ÐMvä\x000cv¤\x0010³[	lãÇêÖ®é
»@Ã\x001bf+ñ"JpÇ0òÂºkìG+\x0003Üàoè\x0014ç?\ø\x0016â#&£ü\x0000\x001d=5Hg<Ä\x0010òò\x0011»Bã#\x0006\x0017íÕ¸D­<}Üb;;ÀB4c³d¼GË8Ï_0ôÜúü4^ùi\x00042·â-1f´§Y´ë\x0018ì</p><p>àÐ>ªÀ\x0018«Í¨]¿ºWh|u\x00136B\x0017W·½ºøN\x0007ÝÚ\x001cß]¡aî¾¹xÈð!4\õÎ5CZ\x000fú\x0015\x001a\x0014Ñ\x001aºk§²ÕkÊ°êÊ»"CO^÷,R¾\x000fUeH¾\x0007\x0019SOÞ	
zh<Öºd)\x000bµc\x0007 9\x0004uÕwB\x001e6\x0012\x0012ç\x0014kUQúQö\x001aòNhµ¨L£ììsrølVVGûÖN\x0015\x001dö*°]</p><p>Ø\x000fàS\x001d:.6¿\x0003ôÐÅö,aw\x001aEºjUj¡7\x000fO­x'4è¢h\x0008</p><p>å\x0011òz\x0003:ØÔwB\x000f]4ÒZ\x0005Rm3\x0012úR\x0015]=r;U&<k]CF\x0013u\x0004&gn/[õàÈC\x0013´ÊAµø1çª4ñ`°Üi"´ßµÿ\x0000N\x001cÉv4]áRyêµ¾©õî§±J\x0006Ü,\x001d8râ0¼l¼;¡aä©2ßP:ø\x00050¹Û\x001dÍq;-®;5Td·\x0018Mj\x0005eK/;Ôwj\x0008lFX\x0013ñ­õD*kY ]Yl~\x0007hPCÏ$R&Sk¶/Ú_2]
§¾\x0013\x001ag©\x0012vÝÈ»EjX¸ìÕNÝé:¦~¾\x0013\x001aÔÐ%¦2ä?úâÔxé}NS7ß	]@[(2'¼¢¸õ³Ëf¾\x0013\x001a\x0014±y½(|²%N­'Hì²ï\x000c}|2mºóJÅ£½ãµúøNè1\x0016[ìaJ¯RæF&>uÖz±J\x0014\x001d)LÀVÚ²\x00180Ú÷NX\x0018í/\x0016#-) Ò\x001b5c|=Fûwz\x0008­{MÈ=°U\x0019&§èól\¶îÐ0Ø/Ù]H­TßEe:p³q¬}\x0004hêÜ;¡A\x000fm&÷@M.É\x0000±ZöíÐ¤}l¾kKÌ±>ëÒ[õìÀ/@\x0013¢1m£e±Sá²ís\x0017SÇÞ	=hCjLÏ±Üe¨åH(HÔE¯ûõ®È£[OXÃ¹àUÙ*em:Ì±Ðw§\x0011´Ðg,,æ¢Æ³*,Ær@ï:\x0006ø_ÈI½\x001cÔ;nú¢©Uï\x0006¡¶º9OÄ²ÔØOéCÀ\x0013=ïàÐ¯:°&f8ªí[	§\x0016À\x0013\x0019¸v¤\x0013\x000b\x0002Lí)n*a¤~èPG\x0010ê)7a\x001cÏDgåö­Ská	\x000c\x001c>M
Q:s\x0019ltº§v\x0012@¢£#'ÝX¬º´\x0003«s÷\x001c§~Å\x0013\x0018¤ÿ\x001e\x000exò< .Ù,9OäAµ ¤NàGKÑ¤¹ïÃ3wÉZ!Od Z\x0008413(\x0015\x000b½\x0014£ãî\x00140\x0002\x0006"ÈµRL
\x0003÷\x0008|j¯<q±EZ\x0006rRÁld\x001eè:×kÚi_\x0002í»°àO@>Rªª¶ÕÙü§®Í\x0013\x0019´ÏQ{bNÚ*¥­GUsëØi_*dÈ±¬}Í\x0018)ÃßóJS;è	
úç\x0003Is¦±c©)iîÙ»¼SÀ\x000cÔ654g\x0019Â§;\x0005¯|c0x§\x00194Ðy¤·</p><p>\x0014]´\x001aë±JÞé_\x0006ªbiüUFT\x0003ÙOÕ\SºØMÝ«'42X"mÖ×èÕ(s:nw*\x0003\x0018ÐL\x0003ØÅq\x0014\x000eèbOä¡Ò\x0004\x0007i°\x001c2N\x0003ûÀ<:1öäkÞé`N`A32¶NokÔDé¥3AM½¶'ôPBiÂ*§9,¡SRµ¸N9w:\x0006Ê\x0017z¨mÈj´\x000eæºìá=¡
®9_TQµô\x0006ª:\x000fbÏÜ\x000e\x0016ÐA_ûÐ/Ô®3Y!>#Uv:X\x000e¦rt]\x001d#O\x000f·ï\x0005²²ÓÂ\x0002Zè\x0002ÆÞ9{NÎDÕùÚ¼²êg>¡\x0016öqBhçËÈk5ô=\x0007VvÊR²¤À^®-úoÈjÉëÖ¿ìÔ¥ºB­
_¬èÔcxL\x0000¶¡-É;ª·Kz
ïÃ\x0015}èãªwêR</p><p>("Í¡TÉâY«¾bXÊN]ÊP¤ÖY% .sÒ8ºÞWwúR¡{¶\x001aªË`\x0011)¹Ñ§înÝ)L\x0005i/\x0000°</p><p>eÃÝ:ÞEÕ\x0012uLZÖÆT\x0007öÃc</p><p>E8</p><p>*Ù\x000få,õe<u§/\x0015ô\x0005¤\x0019G7½\x000bÊD»îÖÝUÇ%ýOè3FöøCJª\x001dîøz;\x001d¬C\x0007£´°Ì\x0019G<þÞYå\x0019Øð©;\x001d¬C\x0007û\x0016"ÜZÇ{Î¼xÂê5ìDÏ;M©\x0005Ä¹R_ûG9W£t)d<[3ä9Jë-ÜU7bþ½\x0008bÍFê,\x0010ÃZñ©5Ü/ç­ò;\x000e&+k6\x0012bG'\x000f$ñ\x0005:\x0015åI\x001bÝËb\x000eâëÍe[ slÆÍ4Ó§\x0008[bQèþ¿Ý\x0015Ù­ýñ½ØÎ2ª´´rà\x0013+µ5ÜlÕòÅÍñx\x000cÛJ\x001eNP}L©'S²Ûg\x0007à¥T`[mnª"lK^Ý\x0013©Ó.y4x7xú\x0006¹ý\x000bí\x001fè/yÁ¡ÍÊ[Í\x001dÒï^ïÅ»ù#O_\x0016+1ÛCO¸I²³ühzËÕ£ËNÂzpÖÄ¡½BØ\x001f\x000c×¶åá¡¿ òæë\x0012¾Ðìs9-\x0016´_q\x001d7ñ5H¯ºt¤WªÙ:v·åáfë\x0012¸
.Êî0Hi¸À1|Ìç+Ì1
=·z^ý@¶	\x0003\x00138GÞ>(S}Èe.»­/Èa \x001bZÚá.9Ñ\x0015p^6«]ÇÜ\4\x0011'g]&</p><p>«X,gçì1\x000c97^O_¹=\x0004ÄÕÔ|	rðcT\x001c9¦Ú²uù\\x0007òe­ÈydOE\x000e\x0019\x0007ã%\x0012¦Äuïò\x0001=$ÞEfwyÙ®D</p><p>º'K\x0016\x001dÆ\x0017h7N\x001d\x001c¶ø·ßÅµ\x0018¢Bö\x0007çÖN6F\x0013U»·LKW\x0002ú±½áäÝÛÜÂôt\x0003·ÓþöæÏw¯¿:ÕS«&km\x0014\x0001ª\x0007ðªHwû¹ñ¢Ë5±1ñ²´\x0000ú¤[HÌ!a6Ü8¹$O<q1·í®¥r%/sr´\x0013~i£.ÀP3mÿÿ*öV% äTð\x0002\x001bè¼È\x0013\x0012Mà7d®x·ge=µqA\x000ctS\x001c\x0008_;\x0001\x000f%ì*³ì5g7-MÔ\x0005\x0019JJébW(Ñ\x0014ßNsIW»ÌOdH@\x0007Ê7§;\x001a2í¼Úâp"CI³;pÍ¦M\x0008IíLµ¦.ÙÕ¯ÐàKª\x001f\x0012I.Gµ2CíÏqy3¸qA\x0006%\x0011îúL/n¡C«)L+=\x001c:\x001a</p><p>ÈF½{öåÛwïn?<Övý9ãzø\x0008'z\x001b0Hb-ýyª¾S?ZZ®IõýKZ\x0017Ê!Â¶E³êßu®§b'+uE\x001e}\x001dÙ\x0013Q¬"¦îü¬8\x0013ÝÑÛ1©+òh±ÊbO`m*õ·GaC\x000f'3u
p`bÕE\x000fÌ\lGËøäG]GsdÂUB8Mi\x001c®¨¬sqµèëDNpä³¤MMy4)«ýÎG\x001el2WàÑYU¸Y$\x0018OÑ¾dß»&ëw\x0005.ðí</p><p>Ñ9_ø@Þx,É9·Z»"¶ª^}Ã#[¦Õ©Êõk¼vý.ÐÐò/¥¼6<\x001b]lQ\x001f°7Ìæï</p><p>=ôoc7îµ9K¯ò</p><p></p><p>X</p><p>\x0012Q</p><p>\x001d\x001dÆ\x0005Aw":ÛÛ\x0005çÿ+ôÐÀ"Óáð¢WvàC­zO`gõ</p><p>=´PÚeh\x0005¡(goÚ©×}ÿWè¡òÔT<5õ°E£6e6e	Ë¶ÿ+r\x0002ÙóÏ+©!ÝtUÔ.·±ÓChú¯1PdÐî\x001dÓw±=eU\x000e»lú¿B\x000fM\x0017¨¸¯V\x001dZ1p\x001fgÞ)"´ü×epÙ\x001ev?Z«6gº^­[þ/ÈÐò/bþiIÌ\x000e×ÄõðØT0·ü_¡Gào¤ïÚÑm`Ò(ZÕlÜÄ..[þ¯Ð\x000eÄ.<çC£ëÔÄN#w\x000e´¹/ÿ\x001c@:\x000c\x001b\x000fC£á±E I\x001dzÙ;E\x001e\x0002][¤\x0008·Q¸\x001d8J\x000e®üØA{T7¹DÒï(õ\x0010î\x0005ë¹\x000fý\x0002=úÐ£¹¬A:¡à`@'.f9Ó³ÿsW÷\x0015\x001a\\x001cHòÓ\x001e\x001ablfzóE
¦ÊFÀÛgÿòæí\x000f,\x000e\x0018=(E ë¯p²6\x0004¸þÜa§*Î½÷ááÔ¢SÛýb\x0011Cø})\x0018«\x0007G,6\x0017å õ-\x0016IÖ\x0014\x0011+±&=ÑÊç»"\x0003\x0007Zs&\x0003#ÓJZç¶Æ÷ÊÜ\=+ógÆG,Jc:Íj©q\x001fêÒç»"\x0003³tæ\x0017:2-`ujêIÈW®Ù\x0015\x0019hÕd¸\x0018·A©÷Ñ)ÿIÚ®Ù\x0005¯ZbÛ\x0016R\x0004¼Ä|¾Þ¯×\x0016È@<d1-gÆVÛö\x0012°?,zþ°P¸B ¹Á*ðØÃÅ`Ñ3¢õô\x0005±l z\x0014\x0015òòM¿\x0002Ã\x0002Ýµå¸×ê,_Þ\x000b4\x000cÛ¹ã]Mæñ&qÇ»÷}t1\x0010Wô@@/È¢H\x001e\x0002æ\x0011öÖÌ6ÛzM&ðáÙ¿þð÷×?üýíÍ«g¿½yûöæîÕc%Az ¢\x001d\x000bÕ$
²ìîéVWõ\x0019Ç°ÝVówµsWdRUØ2ÐÁÛ¦.\x000b*Vluà[É¸kª\x0001³¬\x0017·Úù}\x0002C\x0017`¦¤¢\x001cª«\x0007é]nü>#\x0018iNý´Ó-JZæ*¯¸q\x001dÙ\x0013Ê3Ëx*\x0003\x001f­i;äBW¯Ì	\x0017º\x000b¥%®vrÈÏ\x000cö$ðclà1Ý=½\x0008VõÍÁh]m%§¸®±©:ÂÞ,[eM&f\x001c95\x001b\x0010Ë2X·o¬ß´ohæ)4
jíà2T¿\x0002³@\x0004ÙY\x0001SÀ_ZbvbIQÀ¸&.Q«^YÙ\x0017¼S\x0013ËjW!\x0004i4za9AÞÜ½õx¾Õ\x0014iý¡\x0014r\x000eÍqÌ@ÍOï\x0015:ïî9\x0008m!K´òDÁ9R·~Mf
±Þ\x0013²\x001a</p><p>KÀØ¬Ùv®À¤\x00035ñD_â½þØS=Gé\x0017T</p><p>ýÙÍ s{W2\6v¡®]+²]W¨>\x0013\x001f,Õ.×ä¸N\x000c,Î\x0012î\x001a6\x0019A§\x000e.È\x0015µ\x000f&TCàe\x0016rh~ñs\x001fØÿ+t CÕïûÔTð=Û°ÜsB£\x0006\x0016å\x0016cx~P§K²ûËÄÂ\x0015:±pÀ©Ó§V!zZnÇ9Y\x0001!³\x001c¬ç*cRí</p><p>.\x001e_q§'n­'>1\x000c÷3®)a°¸àzÖ\x0014¨ªyYrÏFHì1£:\x000fÏ_¡QU\x0012&p¢W-bÇ×l-½ø²S\x0016ïè}Å,ªì±à!	NàØÏwÎ²\¡Q[2.	B¿e¹Sâè×³óWhÒ\x0016¨kOf'Ø©î9§ªøH÷uââµ³ÈÅÜ\x0019c¿"'ºg\x0008½5<ÌTÿ´=\x001bç¹ù+t¦CÃ\x0004ºtg\x0005¾\x000fvÊ­ë¹ù+t¡SÿÿÍ½kfÉ,¶\x0004\x0017P÷ã'\x001f\x001a^
nS-\x000eÁ¿B²$S(VQÙ]Ä\x000b\x0010Ð6´\x0003q\x001dÜV¢ð\x0013ß1ó]¨ú&É\x0019\x0000\x001fm\x0019_xx¸¤+Võz\x001aUö=Û¹öÍOhÜ\x0011]®E_\x001c\x0017°4É½>·öÍ\x001fÈÁÐ\x0005\x000bå\x000c\x000f::¢Ú,6îÛæ'²¥1Ã\x0013ÔVÖØ`ÉYCVwíÐ£\x0002\x0018tÈÊî¼\x0016^z¦;2¬½ó\x0013\x001a÷!\x0015m®jQ³©N\x001bÕ¾u~"c\x0015É\x00088¯\x000eÓX¹!ÅÔ!~pµ_\x0002ìD\x0002Æ]¦ZÙªê¼oCÐ aªm1ªRé½´¹\x001c¥ÅÎ{{® 7\x0013û+ºøÎòtë\x001cä\x0018÷\x0015x(\x0008ÈFR"%ó¬0óx
m¨ª··=QUû3ü\x001c}</p><p>ÿ@rÜ½\x0014FçjHÃO4ü/.'uhj`ª|ÝäÝûÙÇ9o\x001f_¾»OÚF>júµ3å\x001eEk\x000cÜ¤ÕMÒo¦:\x001c>ÇxY&Ó6íi\x001b!mª¥Wc\x0014ù\x000cúªãá¿¶:\x001cÀ'×Qü¢°eÅ8rìJ\x0014jÜËA\x001eÈ\x001eC¯ÙÝÆ\x0007ëCZímêk\x000fÅ\x0001\x001c\x0000¸P¼È_E\x001e²juëÌ¸5\x0013| G@vÔgYZQº\x0008InöÌh2@\x0019AD|#ÝbØrw'ðÉÝµÕpWßO«áF³W<ËL\x001a\x0011F-¸ §Çé½¦®\x000fØ\x0012,2`Ì9,"UómñûâÃ\x0006J°u$ÖeÙ`QØáª-;_(A\x001eÈ°ý,1NDF60´j\x001fÍs\x001b%È\x0003\x001a6`t,æ©GªïeN®\x0017`7J\x00074ìÀ6\x0003ØL^Yù¤=¸TëE\x0019÷äÕN±&\x0014×</p><p>=dBÒGÏqn&\x00074¬hOuéóå\x0015íx«Hh±/\x001cÐö7¤²J¬íÊp\x0004-\x0016¹k	Â,zÆß?üüãËïÞ?ßÍ~&ØXÕùnÚùN^9pÉKrë
\x000fÎï\x001cì×\x0018Ù\x0018ÅAl)i_À^¢K\x001fé¼Õ5D6ºr\x001c\x001aTÄË[Øä÷x6GØs\x000cþ\x0010¥\x0008Q\x0005^ÉIòë8¡&P\;Õ 82³EÂð_ßf©\x001cËÿ\x001e\\x001bkb\x001a¢Ó\x001a#CÒl¼*@t×\x001alÇ5,^"\x0005z5\x0019\x001e·¾&ÍRöÔ¿.³Á¾^YØÖþ2Û	ÌR9n×\x0002\x0005"^Ùð)Óú\x0006íöÙ|£²ùâ©MÆ¢\x000f{Xûî\x001eÈWÒ\x0001\x0005ô\x0005l&lá®Â\x0006m÷©q³T¥\x000bõ+\x00084QúTf<Ô½ní\x0004Õa,\x00059mu8
\x0015ãÅ±É¥Þ\x001dI=?¬êÝú\x000bîUk\x000f`t7TÜèá/-;ãô´O¥~èÍÜfY1Nlàfð0R~ü¸Qùñ¾êÔ.ä\x000fXuö5ú	
\x001aî±bDFM\x0006¾¢É F÷	r£\x0012ä¡wVÐ 
/hÝù<\x0006}µW@´V\x001c!\x0002®\x000e­µ\x001e¼Úæ"?nT~\\\x0000û9t\x001b5·	\x0006÷S}µ[y'äª	zG½]z"{ 7*AÞ\x001dCà,\x0015i\x0014ÖVgGéV$\x0014¹Q)òv\x000cW¾g+oqSøémâ>AnT¼ËiC¢2eÏÍ2U¿CËÐ\x000e½Ú. .+"ÿ9óuÈ6',K\x001aM¯ænÒØF¥±ÅÄ	\x00039J±n\x001eÚGá××\x00087ùf£òÍ]æ?{Ú,Æ\x001fôN\x001c©Ê«\x0008º¤ý]S5l«Ù\x000e\x0004\x0005=®æ\x001aÔCå5S)0u¤ñ\­F¾HU\x001aªlkÚÐyÚ®\x0000¶=0V§±îSF¥*Û =&\x0014úíBB¾Õ©H¬?û7©J£Rí'ñI\x0016¢\x0012J-ÜòÙn®^`Ûåûf8Mº	ÒÇìðXea/\x0005Õ</p><p><Ò×Áñ_øÂÛÆïÚëoË\i?´OË!Ö ]zÿ
õßPù/4\x001eü£à\x0002§\x000b·¹´\x0013qÛy»uLûõ?þþçÿ¼\x0013å¬*òÀà¥Î\x001f\x0011¨µÝ§oÙÓ&­íÕw»Ð\x001dªJÖ6÷,\x001d\x0003Ý\x0019íÙãw¹Ë	\x000c4ªg@V\x0012ê5p\x001d Ç°åMä@È©"Dâý,\x000eC?k6\x001d².ÜÏoØÎ¨\x001f\x00016{_³¬ß|=÷u^\x0017ÕFv\x001b\x0013ÏfÏ9ÀF\x000c3\x00113×\x0013jàr{öu®;Ñ¹År§´g³×Ñ½iàÏ½Õ\x0003\x000c:ø\x0005¶{viÏßÐ@buh(U¹:ÄÄZÓC*o£
\x0015}k\x000c\x001aöWbIë \x0007\x0019êjÕ¡
Vôª4X²íê\x001bó±¬\x001fV\x0014ËÀÇ6U2s\x0016u]xñÐF
Y®êÊò\x0015\x000bz0H®ã¥\x0007w´\x0004é¹fè4_}\x0013ÙÒ|@ÎU<HÏ´F5\x001dnûèÀ¼¦¡T[­"´µ!«\x001dÞI\x0002ëËlBãÊKHÑ³CM4WDÖzû~Ð áÎª¦¨V \x000cê_4qá±½J;¦åVN%1wµðÈô#ÁKµeqðt\x000cÑ¹õ]6á]æ2\x0019$\x0008ùO\x000fë?Ì(®V4~XvP\x0000Ú\x0001¥ôîõa6-\x0019\x0017´	*ÌkHfØ2_-iïhÌhÝÕÎRµ8\x\x001edô«cÚ{\x001a5Ü\x0000]²%\x0015´\x001eT®«Ýây· «HéªQ³u\x001e\x0006\x001a«ÂOVì¥>jÔËS= ë¨KÝÛ~Lèt9×meÔ\úÈ}»¬ô¥	iÔh\x0002[k¥ÄÚ +{i"ãFdéþô½¥\x0016HJvË^ÐõrÐ»«Ö©Î½Ïe%\x0019\x001dÐ\x0001wLÅ\x001e(Ñ1 áé\x0016ãkÕC»}^OhG\x0013~ãÒd¡Ö2»«{Ñö4j\x000f\x0014ðòê¨\x001fÅÕÁ§;	ûEu!rô\x0018l­æ\x001c\x00136ÒQ:\V8§Nã[X3\x0002\x0013\x001aw\x000b\x001bJ¢NS}æu.ïêÍ13
ö\x0012\x00051?1º='jâ\x0016\x001e1z\x0002p\x0013\x000cY\x0017dûd\m&°\x0004BÍ2då\x0018o;ÝâêÒ\x0006MâïQ/gN¬=3·ZsLhK\x000eS Ú{\x001b´Jì÷\x0007Q¼Ú\x00116¡c\x0007ðôVç]oë[M?&r`d\x0014â.ê$Õv3í¬ýÛÎôcBÃfñr~ò\x0004 éà*f\x0008Ý¼k5ýÈ\x0006\x0012ßY_ZZ¤7Û½ëÇÎ4hLì[Ë~"Jô)\x000c[°Õôc"ÃvqÔCUgtPÃuµýÐì\x000cV{ï¼4\x001f:×d{¾l5þ8 ¡Q\x0003\x00079%\x0016SÒä=Ê[?&2n\x0017O½pU¯×ïYÄÕùc"ãnqäNí:¢:¥C·Y­?&4\YÀäFÕÀk3«ÒIõ·õÇÄ
<d\x0018ñò²`nKô}\x0017®\x0016\x001d\x00139\x00112\x001e\x001drH)h>ÿ}¿XV	{%@ÍGD(Ùº\wr\x000cóåÕ¢c"\x0017Úày_¤åkà­âº\x001câêÐ1+yÑ|5\x001bú·EÇ\x0001
Í4\x001a\x00069£²f\x001aÅ«GÇæøTî\x001auä½bjýjÓ1¡q³R>\x001eu8j^zÎu¡â«Í=ßâ,j©FÍqñÂ¦c"\x0007\x001a´Ç\x0002AÖ)\x000fU_³=
»ÚiLèDÐ\x0005èúBTäFÓ{\x000cVÏ:`á¿×Àø(Õ¡^}]=/&4ÇKÈV]©m:XM5ùn\x000fpµ¨¡A#
"En_Ó+/ä×\M/&4ÇKK·UY*^zì§ôêL1ùa\x0001)oÛ\x0006­\x001a¾jëÕèrµò</p><p>®<Ê\x0010¦õ¤fÉó\x0010úI½^Lhz\C\x001bîÚGÅØþ8\\x001d/&.®hJ%\x0011#â\x0015Íùôà{Îcµ¼Ðø´(x.K0GKå\x000cÌÈÔ¬\x0017\x0013ºÐ>Äö:\x001c\x0017ñ\x001bòÂ\x001bR>«åÅ®4j¨\x0002È'åÂ?¿ñ]\x001däÕòâ®ê\x000e ©¶=àÀ4ô\x0000a5¼À\x0013sg\x001cfMU[<Ðnq5wÇÉÕðbBã
\x0000½òÑëêPå&÷¬Õêw1q=­;\x0008¥M{j©Z\x0019Ië¸\x0016>õ!_íÂÊç\x0002¡\x0012»-.w¡\x0019B5W»°FÚàÐìÙ\x000e,ýª¥Ê¼«Ý¾Ú^LèDß\x0010ÞZ-¾g¶\x0011U×¥¯W\x001b±rM\x0004nqqzæ\x0007s°¼¤}/·¬\x001a\x0013ºÐnÁæ$ÉMóñ\x0011xÔÞ\x001e^\x0000{lk\x000c\x001fÔ !\x0010³z\x0003DÕ\x001c]ÊÐ«½X~\x0016ø¹\x0016Õ{bm\x001b\x0013yäLçWÓÆPc\x0002\x0007Z×©iX}F%>¨NÖ\,>\x000bü\©|!d,Êaª::©]Ny@_,>e`VÙ\x0015¡dÇë:«\x0010r|ÅÅg±\x0010l¡Ú\x001esjíYJ]¹|¨L®\x000e#\x0013º\]·-rÑg\x0008Ë5HóÂß¶\x000e#\x00076\x0016\x001dl¥QUg6	Ú\x000f\x0013Õb1Xn\x0014@\x0016=~U8ã¹¶a0¯VU	\x001bèÜøÖ5ë|X®\M¶å+\x0017ïÅ\x00166\x0005^"ü</p><p>5G
ûªüi±üé\x000cÜ\x0004\x001bÆ«çÃ)Ù¡pz5Õ	\x0019\x0010&\x0018gGe3Wª\x001fÀWó\x0015J©\x001b\x00168?</p><p>ôØ?´­¡ArU¢´.}í7¼*$Z,$</p><p>=\x001cNÕ7ä¶\x0019½=WßÐ¯\x001cv²gË-\x0019tz¶ô90²¢·,Ô¢\x0003¥\x00107¤Ë¶´²Û:aJuç+)VmÄ\qWÒHØ¥Mõ\x001cþ#
\x001fåÑZ$\¹\x0002Ã£O=#\x0019V?[-\x0003ç¦E</p><p>\x0006\x000b\x001aØjr</p><p>ryØ\x000fE\·³ã¹íM\x001bg±æÚÓä´nXØÕbváò/\x0018\x0017ÔìQÉ¿}Ä\x001f^®?°üøO	Wé$'ÂfûÂôXu%öp"æë\x001f\x0011³bõ9jdpYç´9=<2Ù_­¡ìi
\x0019È§ùÇp\x0019\x001eÚ¡n\x0010¾»^BßñÞ³&«} ål_ûÐz>\x001bèÿíéÃËóÃ/>}xüðÃø9s¥Ëu\x000b»þ+¼HÇ<HðÅùf> ©lºÐV&q,Lîkã¦È?´P¼Äsæªr\x0008¶ì¾\x000cþ\x0017H\x0018DtÂ*ÁÚ·ÔÚ°sÀ!1&§</p><p>\x001dgí\x001b±\x0002× #®ôä\x0003\x0019Ì/*ñ /Ì</p><p>ÈovCm&r1±8êy²/)\÷\x0015/À¿mû¹\x00064ôs\x0019ÉmÃ;%+ÊY.Ü³#~}[âà\x0006+jðâhG²rI¬´dËU«Ø\x0001íaÔ\x0006Cþ\x0010¥\x0018ë n80oß\x000eè3:2Êdþ(}Ð5°¹\x0013l7]h\x0007rüÉlñW-qpB£K-Z@DÚ.TÆ\x0011[Oµ]/î·/í\x001f¼S'®OÙê\x000bÝß~%=\x0012zPóVì¶üüçP²¢d·ag"¶ßE+&)Ù<\x0004\x000e×'nñmÈ\x0006y5Õ;¥ÝÆ\x0004<ì\x0002Ö\x000cîð\x0010Ø -&bÊ¬#¼5\x001aÈp\x001f\x0005=p\x0014IHòKóÙ¸­êôDíÃ\x0004uá7Ð!(Í\x0014tÏ×^Z\x001f-ÆèF\x001c8ÏÝSMâ\x0008QºhÍÖÎZó\x0007ºyøKÇ¼¾tóp\x001f3ôáVÃ^àÒ\x0001ÇC¶[I	\¿vÈ´Q\x001cõ\x0006í±jVjÐcÖ¼Êº½Å&2\x001a-\x0019HN¨Ó©ð[ra_g¾ÄDj\x000fX¦%+s(}
E¸
û]÷;·AÈ¡\x001cw,¾W</p><p>\x000e}ï«]h\x0003}Dä\x0016%ú%ÅP\x001eõ\x0015ýÝ(ú{Ó®dý\x0011YË$¥tAQ×\x001dÏ^ÞM8ÕQ\x0015USæNº\x0014ÍÞ¶cBW:\x0008ZÛ&~#Öúý®û¨!#VÓ£v</p><p>:íÍ5&´£S\x0016â>¦ÌÒ)}kòÆµàA£â\x0002ÉäÓ&qß?<ávüËCR¢Ø\x0019½1^ñßuÿ°¤[±­µ\x0008k_Ù©)zO"o\x0008ðF\x0011àÇ¨Ñ·[Ñ2Ú¨¤Ð¾3y"\x0017\x000e Ì\\Ö\x001f¹\x0002É
)Ó«Uí*
\x001aå¦¼Q</p><p>Ö£>\x0010ö\x000cxÝÜ§ÚC'
LCHl	ì°a¼:@¬²J*\x0016gº(éG¥+\x0014{élÃÊÖM¾\x001d\x0019\x0013\x0001,FX(\x0016Ç\x0015Pw\x0019y'b\x0006f\1 ÔÖ5\x000b\x0017£6ã ¹í\x001203¶!±¹/¼xw}ç/¸Ã\x001fØÉåÝ`þ\x0003¢fímQéßF>U²¯Wý¹·XXý\x0001T=¨*°Ô½s,ïaûñÂùùþüüááW\x001fÛàá\x0017òÝGl(;U</p><p>/§¢\x0008·\x0001J,ëÿ\x0005í^Û4ñ\x001b'H\x001b7*Êd¥(­æÊl_"\x0013\x0018ÌLÅz·ü[ìVÎª\x0011ëè¸^í\x000eàó\x001d²!óÇ¢t{ZP¤4ÀËÖät"\x0016Ñà\x001eD\x0015ùYÖCÜÅÞ\x0013ùÌó¤v+CP\x001fÒHyv}ÛÆÞ\x00074Úüé!l~\x0013á\x0019ò"c4\x000câVÑµ\x0003ÚÁ|\x0016ó1I>a[+l=gÌ}Ê@þ¿/[\x001cë}?óW"ïÂÛ^¡lz'±m%¥!}þ\x0001¥Ê\x001c¤wq9®\Ø$d¾y|yþp?m4i\x0011W]¶Y;\x000eÜnVÊH3½ÕqUCù.ù6M:%iÊK³ÒÉêüFÝ¥d&2Ää¼ù¥ç\x001cÝ!}Vl¶\x0016Inýº&²§1\x0003=G\x000eUgH\x001aì%$È\x0010\x0017Ê\x0016ÍÊDBÚæè'2\Ùc\x000bU
ìÿ×ÖW7¾ÙÊ®Md\x0008È\x000bi\x0005\x0015IªE\x001e³jÎr[Ùµ\hÌÐÜ#­á¬:ÃÃÖ¢z\x0002W\x001a²§÷ükãõiïO}àbÚ$\x0013oW²TÝ]FlË^sBÃ>)¨WäHiôÄÚFÉ»}kÿDÕ\x000c­\x0015¥Î?\x001e·OÙ¼ïë°ðzh-öUUjÍº3«\x000cÏÐ«µLnµÒÊëùi¸_-8ÌkØ=¤µ".,cÎ=Ï³&\x001f\x000ehL>dæø"	é¬Z ÒPÀ^\x001fÛ\x0013\x001a§Cµgf-,óaûØÍ\x001dy\x0013æ¿t^®ÿ\x0002þûo/\x001aY5®ý¨Ò£à²«üßâ=~B\æ·C\x001bôÁåØÆþTÑMñ¯\x001dÛ1o:¶·DS\x000cñðþñáÏ/\x001f?üþNO\x0018¢R0vóÅ\x0013xh¦R\x0018Ñò\x0010y'¯ºq7\x001cBtð)CÒ¶Õ}¶·ü\x0005\x0019aY"ðQ-§ªãÒðØuJ7î\x0003ß;QÔÓ \x0010ßå\x0010Hé·¨öÚiö\x001b\x001bÈátúrKz`ùê\x0010TÏRêÜ­Aäð!e\x0004æªeûà \x0015ð\x0006E{ã\x0002\x00129|®ýï!ätÓ\x001c2³+cÌÛ×ßD.0\x001b\x001aÒs¡|^
=nïªíëo"ÊN»NàdéÁ\x001aÛQ¾IAî\ã"\x0007\x0010m2\x0002ã;}?å³\x001d£¿`\x000f\x001cÈ\x0016\ ~hç)\x0005±m"t»P\x001dÈ\x000e\x001då6Û?O\x001f0ê¥áã^É{B[P$[¡[Õ³W»\x0013¸Ï%º}Õe\x0002[Pô>±-¸(wñøæ,I¸òÌ\x001d\x0010\x0016753bx¡Öºqe\x001f÷Lè\x0004\x000b:Ê %#QÙÝÍÊW¬\x0003\x00196aÎ\x000fÜ\x0017y\x000bDËõ6?q\x001bSMhØÆãþNò0E;lQeèñ\x0015¯¶!è»B¾\x0005IyQ«öav·óxÏ¢¼\x000b¿¤¨èQª¬À\x0019[äN\x0014·\x0019\x0014ÏÌÊ\x001f<¨üN¸\x0012=aé	·\x0014ÅDYJ+¶WP«z£óîú±ÏaÈüÝËó\x001fþp¯ Ä(×öXÔPYk»m¾5ßÌ\x001dÜìèukºAþ\x0005Ó
A<b )\x0010ÛÑMRì5²=Ï\x0002²¾¤\x000eä3?*Å#På\x0013ûS2x0µ.E"m\x00148O\x000ex
¤\\x001d\x0015á¶}'.\x0003øÑ½&\x0005\x000eä\x000cc®\x001fMl2\x001bMPùÑÜõóÖ7Ú|æt/ÖÇ«kk\x00158Ïn\x0016/_ùtG¶ÕÎ¾ªyÒ=!¥[[(
ùP<½\x000fÄOC~\x00178 -\x000cÊ¡íì \x00066h®ûìË>1p@{NØÑÖ\x0002Ç|&k>y'Û¬ä\x0000\x001dðÁÔ.\x0001ª?5h&\x001cú£¥æjå2_ôÐ\x0016põ\x0015ù-æG\x0017ÚzßLhX ¡¢`n4\Åma\x001fs;mÚ¸@µK×_=þåãûü½Ü§¨UÕ]Ým¡3Ê't\x0018Á÷ûó­ÎÖØéu?~¶\x0016§ÏVo0á\x0013k`yöj¸÷@<Õ·©Ü\x0003ù\ã%\x001aòR>'²g&p¸ ×MäóÔ."\x0005K¼-KF6\x001c÷HÍu$>ÏÍSÚnAäöf@ÊP;{éq,ûûà@N0æ©ÜØ~\x0002÷s\x0019.ìÍ&lÏ±-Ör$t\¹$éG;Ðz\x0017\x001cÀ\x0005Æë0JC©\x0016¥\x0006ÞëÎl_x\x0013¹òáX 6ñ&ã1;\x001b÷'ö\x0013»´ø\x000f¸ç
\x0013\x001b2¿ñ¼!.§ÈH-Â)òÓçïxn¡ÚÏ^Û¼WÅ©V\x00151Ê\x000bzÒ¯-«2¸þÐy+\x0012°Ù%Ë¾<#ïKÛ>%ÇÈÜÌé´IÀÞ×f\x0002ÛRú¡3­ý\x001fWJæ</p><p>K\x0018\x0019Æe[Näs[hÈEu.*\x001fäPfÇ\x00150tXÄ!Jq\x001br`Vu÷¢\væD>w¦´¬£ùLV\x001c¢Ôs$|ÞíÌ\x001d\x0016\x001cbyg(Û­¤fÃP0\Ã´\x0003\x001aÂ4\x0013AgU#+¥¨Wðè=]6ýò\x0008\x000fÀâ;ÁsfVÈG'ç\x0015´Q[rLÈJs\x001dô6þÀXæ$CÖb6"	e%»%¥ômþeBCëF$ÅO±½ jHIVíÂ°w\x0010ÐPBJ"bBÅYÎ42;WÛ\x0010ä¤M,\x000fJÕÅ;=è½7ÑFR#i
&¡b\x0012ë5++Ñº¹æ_&4ìDOFÙB¡ÕáÔv\x0019e§«Ý\x0002ÝÔ²\x0011q¢\x000f{JÜêX2{§	ýHäW/?d*SçR\x001e WÐP\x0014ëYö¬%SP7^ßãk\x001dnBc\x001d®0´c&f\x001c@µËtOMÐ\	/LË#\x0007µÇó^?ù\x0000Föh;ò1\x0016«êÓÆGyÐG¯>"8´Ú\x0005<zåÈ£nOáß«zÏLÐÈLµïð`=¼\x0004dNf\x000b¯ÏÇ¦Zx\x0012®\x0016\x0006Ã±²ZÎFYÅ\x000c±c»ãÞ(þ\x000bô\x0001S`\x0002´ð0Ùõ\x001f0Ü%lD9\x0001÷=~ÖZåuCjÔôÛç§ç÷ïn³\x0016¾ÝËôÑe&ÌÔ$pü\x000e\x001fá[gwãÞ,\x001dØË?Z×\x0014|°P|ÊbME]\x000eÛ\x0005°í4ÖÔëY{Êb\x000f\x0014 ÷\x0012\x0001Û\x001e\x000c.\x0017gÔÜ£ \x001a2\x0001fZ\x0014Ï-
ß\x0002-Î*»03jPCÎ°ÖÛÒ³$c\x0011Dª«Ý¦ì¢&òtä\x001cØã;ÏÀ/*qQSyÚ²WZ[v</p><p>"âRÉ\x000bv_ÇÓsÀ\x0011g</p><p>Å\x001eÍòGWÎÕÊ@ÐGlÃ\x0016\x000c2)sY9§´
×¢æò4dT
oçt¢\x0017HVK£A/fÔ\\x0006]üÛæ£ªù(V­²góDÍæ	>Y"rw&¤eWèªo\x000fÚÑÏqµ:Ð?\x001cu³ËA\x0019\x0016ZxÁ¸¡GµÚÍßf\x00044\x0018|»qºÛwEµ«N\x0012\x0012Ò(\x001f/\x001a\x0018nÛ½­Ú>	0|çÈ¿Ó%¾\x001dj\x000e»\x0014D\(¯|xúðá~e"Uß5n:Úêó;\x0003µa\x0011ezCW(1Àý{¡Íº\x0017Ú{ÈZAÙß\x0006«\x000c	¼w»a"ux/\x0014*HåÊ¬¤´MZè_wIÒ\x000c.ÃÅÀréíøx
Á«<oö¨3\x001b"_ì~\x0018h!¶hSµuªû\x001a0G\x0010±À\x001c·T\x0014r\x000f¯ÖüCÔWN´1D!m}¥aÜ(¬±xTWüoí\x0010GO]9í¼¯\x0011M`(fñÈ¹ÕÉÏY\x0017N*^vyçLèóÎL\x001f(uã
\x001c­R\x0005²vÏKÐP'Ï\cJêÕ9ä0t¬\x0017é¨ï³/\x001dõ~*ý\x0010jâN?«¸AF³ÆHÇÕ^2&zo\x000b\x001f
Ó\x000f¡EÊê`Ov8ìàE¥\x0010</p><p>mÖ9ÓýÉí\x000cÍK>ª|8Än´±Ä>ÃÉó\x0014úÇJ£Èçò\x0010ýiL!µ$\x0011í¨XU¹\x0019>²WË\x0003d×R\x0008ð¼\x0014®\x001bVêÁô®ÒÏ¡1OF{'\x0002ÍUäæ°³â\x0008\x000cêò&C\x0010U =#	gÛ¯Ç³%)\x000ftõê!ß\x000b\x0016hÏãÙ'TÊ7<\x001f¾ïµ\x0011tB\x0003\x0001Á=¥\x000cQ\x001bH¾í¬öÕCg"´#\x0013h\x001fJ\x001b\x001cîèÖî·ÕGö\x000epNÉ\x0014³\x000c4¤×C=h5ºÐpÛy(öçÄ,LêQ{</p><p>Éï¨Ü·9ÁÐOÉtÔØ\x001ej!¨y1\x0014iýõ_°ÿÂÝ6[\x0015·ÛÞ¤¿àÅÖ\x0014­&¢Ø1{ô®ú´i ¾­HpS½2â\x000b¾E\x0000ÊW»ïÿ­óëù\x00070þ¾\x0008^_
|ûg~å'\x0014ü	Â¤ÓÑr\x0012CT\x001fA\x0004iÖ\x0004Ð*3ôðÿùt·ÄO©tþ»îÈx<R¤£
DDí)½]\x001f;OäÇ3?Zd(øQL«ÈÁ'±·ü¢MCåv}àk¡6#dîÛ»Ðó«SS¥Ã¶·w"{\x00183»ÙÊOeoUG\x001dÒWÈ:h\x0017\x0011¤!³Ð ø}ÏU¨¦Û|V\x0019\x001acf'D471+·ª­ÈÐ\x0004N4Í¨Nà)¢Dç$\x000eÙfÁ´ÂP\x001f/jÈ´
Ïª¨¾³[9»\hÀHÎoôJ6Â\x000bÍ|_Ó\x0012CmÌ¶WWo¡P$»6f§B¡Á\x000b^S(ZbH\x0006
÷þ:buñÇ}¥uââö#µæ\
=)ÛÓTy	Æ}÷ôDí¸³>tF=fª¸\x0008\x0013÷D»	ìiÈ`b,m\x001bgY
yû\x0016¸p\x001dÆÌÌo¸\tnwÛ§í´¶PÖqÐ­
ÚpFP\x0007*aOàÐ¸O\x0002µm$EòÊ+(]h\x000bMäz\x001c2ñ£Åò]y2
Kî«ÕL	ÁÔÕ\x0018o÷@½&2\x001fê5ÒG½¾Î&´¥Q\x0003
3\x0007ÿ
\x0015}ñ\x001a¹ZÐÎÑ ÁJ*±;¼Y%úòX\x001fg\x0013\x0019VôA=¿H5\x000cDºOQ³Mè@\x0006è¨\x0004$Í­xÖc¦¯öÃýâ±\x0018]R· {II×Ä¶4<q»Dò\x0010õ~\x001a3;ºùaØ²Ê#LdÜ-ä\x0011,|É\x0001ÍG¿íùõE9\x000b(pê\x0019ì\x0014'Á»¡Æ|µ\x0011\x001d_+`øÚ\x000b;ò!Í"ïaÔWÖvÔrHmÔ\x0001*å¡°ßG\x001b´z@fu\x0004È°\x000fs&:L»ÎIòÃ)+©áAº>°'²£1`QHsÂW´«Chéj\x001fzÜÔ\-w\x001b3W\x000bÃh\x0008\M{'t$h4!Ëthè¸M</p><p>Ld¾[àÀkG¥>Kù\x001b:?ÂÜ«Ý\x0002½2h|\x0016E£<eÙ2z:×|ÃDæÝÎ»V\x001e\x0001w\x000b·þ;×\x0019í«gï®4hôì</p><p>^|5Ñ&öØüjI\x0007ËÈìI!©SýS¡³\x001cÖDÆDv4\x001dèô!R¼\x000f9p´±\x001bo®½\x0013ÚÓ>Älåa6\x0000VîW¶ì\x001d{'t \x0008ï¼Ä<0ÔÂ£\x000bÑ\x001e^ÀW»%D\x001atâ\x0014«ç¨8®\x0017×WÓÞ	ÍÛ\x0005\x001aÚ\x0001¯¯qN¢µÛ£§£®¶KÀí\x0012gc\x0002I8´AóK6\x000cSÕ·w"\x0017\x000e=ÀæÃ\x001aî\x0012%\x0018vu¦«oï®4ÕØ¶R\x0000«LÓòßvÆ½\x0007t¤(ïk|d²¹£óÎUö¦½\x0013o\x0016Øà\x0016æK«ª¦Ò\x001b¼âÕf¸Y\x0012ºÔJ\x000fOäS³ä£\x0019fuÖÈ±¤,Èª¿¡GK«ÿíÎ\x0004
o*â]0ñÕÚ1¿ê³¾\x000fyEÏÖ«,Ac/­êÖªª+#tïjø:¡ù#bc\x0010/\x0019c\x001a?¯>bâ¨b<u\x001fª7\x0017÷Æ¬\x0013?"<¶B
*N/îðvh\x0011\}ÅD_\x0011"¼¬9EÅÁêpzàfü\x001eIÚ¡½<\x001dç~ø}(³ó·
éöt\x0016öÔ\x000f)i0\x0005=\\x0012®¾aÆWy\x0007Nóm\x001a¹¡¤M\x0008-vÊ­¯¾aæp	 å­áÔÊc£Úq\x0001¬n¡\x0013ºÒ¨¡MÏ îÚÂE63¼æWçÍ\x0003º`:\x0005}\x0001¢­J9\x00174fôÒÏbb2/\x0017\x0003&&rsAJ{~*b\x0018G\x001f¶öçg®ÉÎmNÀdç\x000bg%ïh¡·ÏÉÔLÊ¼^X<9\x0016b[NýN7+sé69_;9ùÿúô¸)m¿àøï1½ÏÌiêh±Æßpõ
ÚoøÝWà«	j\x001f\x0018&¨Xvvt*8á\x000fÜÂÂ~\x0001åáí\x0000S\x001fX4\x0014½dõ+ÍË8W?\x0000Ï>uºKlÏ7¿\x0012Ïh±ý8Ë^ù
qY¤\x0010ÂùZt¯]½ÝFÈÀGÐSúöéç\x001f\x001eþ+xjBæUz>Þ~J¬¤_ûúVüåöê.##\x001b¨Rð)2mÜ>²ç\x00070ÙvU¬|>
]ûpË¶OÉ1­J½Ôm3ïD¿sÌ|Ï DÄß\x001aZL`¤Fo?â«\x000b`W\x0014ÈpÃ&ªVt)I\x000b¼B¶[ÚDæg\x0010\x0002'n`uµªÉ°Û\x0002Ë\x0001L\x0005\x0016dìvdl\x000b\x000b»yEm{c`Ó=zçÞ|ÿø]Û\x001e~óôÒÖñ}v¥ô'³ïóY[nr(u&\ÿô>øÕ<£zÞÊÆ\x0014¤3}DP~r\x001e\x0002¾WÈg³4÷A\x0013¡\x0015Ê\x00036¼xÃ\x00140ÌvSNä³0[\x000fëÐ\x0019Ã¦^Éõ´-,OÜ³\x0007HÒ``\x0014a\x0013ÿxý»r¯9#\x000c¸RjBâil]\x0015çT\x0002=ºXeï\x000fä³AL1ºk¡\x0005¹×øÀ¯-³P¸g÷ \x0018é\x0001÷ËfÃ=ÍBà&\¶b+\x0013ùì;KµÒ²P"\x0006ò¨ç\x0001÷2ÎÆaf Tª\x0014*Ðç5r\x0010!ëÇììNLÃ®\x0004÷\x000fß<¾o\x0001Ëó½N\x0012«ÄU]§¥ß\x0011CBÉ=\x001fMÿ\x0014ouH¯ÌçHjXÅ%t<^iÁTVí5OO\x0017ûý¾</p><p>_XÅøfÌ&ýCÀÊ</p><p>Ë\x000c\x000fÕUFÂ*\x0002\x0017	
h(lSß(³ \x001dY½UDÂ*öDûdf#Auôõ÷]Ùë	YEð·Ò\0ªkÓ&®r¹Ðe¢·²¬sÔÔC(²9Ð¯.Ô>RM\x0015Ò8\x0007âaCòò	öÐ7Ïïe\x0013µ+ùùû¾Êî³ªá«¬§\x0019P\x001aAÞ H\x0008\x0014þå:9Ú,é\x0008¹=Îµ!&Ü\x0014¥éE\x000fz\x001b!§çe3\x0019"Ä¨úå,'ü\	[)±\x000c\x0005\x000e1Lä0È0*´ª)\x0019¯m4\x001bË\x001dY\x001c\x0014ÏË\x0016å-0.Ë­9\x0013 G¬ÙÉ©:j3?7ÝPeXï¤\x0019Y"/È"¾o\x001c«ì]î\x0012Õ«ñDÒ,Ç\x0002ãAô3!«­?D\x000f×°>iF;ÔncV$«D Ýáz¹\x001aO$ÍÈr\x0019×\æ÷^;K©Yò^ðfâ\x001bEzú\x0000YX7\x0008l3o<4Ñ¯ö	\x0010²\\x000b @WHV\x0006%S¬Ú%\x0017þ\x0013\x0018\x0016³¼\x0001U\x0005Ú(Ó­ö¹÷J\x0013ú\sm\x001f°\x001fj%wP	Õa^ÉM\x0013ø\\x00186Q®VúÌè%)I\x0016\x000e{íò\x0003\x001a\x001e¶\x0007ô«gûÛ4Ï¥aÅÎ²YÚ°\x0005®J¬ÍØ½ÐÃ\x0006\x0010p£HC\x0018¹\x0015¥\x0016FóçÕê\x00005äÎ\x0014\x000eÿsÐN
z\x0018ñnÌNfóâ1;\x001b2(-U{üæ=çfBnN4Õ5p4RTwÕ~õ\x0015\x0019cH@\x0003\x0007{mÕ¹-ueq°\x0011\x0000xâKù¾Wé	Ò\x0011\x0005_w±\x0018ªâ
\x0001\x0017âÍP¥¸Z\x0017Ài[8Ö©gXðB*Ï[JÌFÃ´H\x0015bùxÊÉ6¶w\x0004¯	ö\x001d¸¹ÆÂDIÉurÉÊÀ Yâ\x001c®åd<ëaI\x0012yLôÕRö`ßxkû¤<cøÚöi´ö\-ºÀn»\x0010\x0011Äªì0ªÆóÜËt»Î[ Ãí¶(</p><p>\x0006\x0006ð	Îx¾csÝ¼yMZß¼?ÿÓcC¹[Wg{ë\x001aâÏnûçl²­C¸è­¢õvùäÏé»^¢õ6o(ov}ª\x0014n\x001a\x000eUWÈ\x0010­\x001bj\x0013»_®¿\x001aÞAiõ­-IweÈá¢\x0011O'âØÄ9»"ãÚá¸y\x0007DòQvìÛÆÌl.TðÖwä¸Ð\x001b©ª,eî~\x0019uµWpy\x0007ÈÛ\x0005Zº«ðÒùBÏãþZÅ·6Ï\x0000t\x0013ùT1k\x0015/a*½6!.Ï\x0000o¨c JÕ\x0006í³<D÷×&ôõ\x0015P\x001cÙ»À¥\x000eY?-|Ñ¾¼\x0002¼©4\x001bKáÇðs+çpÑ¾>\x0004Ç[¬\x0006Å¾±{\x000f³»x</p><p>å)Ðb,Hgµs/1EÆò{+\x0017sÑts\x000c\x001a,ãa\x000eÍ\ 927]è\x0007r 1ôI\x000bm\x0015\x0019ÉªØû6Mèëû¥¶-}¥å1ÎWo[x~Ûø1¡a\x0017:Ò¯\x0011]#2kt7K=O®ö¡åç8È\x0004µÿ\x0012q2Õì\x001bzáë4a\x001fî/­W/¼í³kBCíÔh¸äô[£½ÀKKoHß¯J`FU\x001cké±ä¦\x0007}y¾´ç\x0019ô¡e)®3qÛÓC -.¦¼>_&4W3AHÊ<Ï"³\x0016¥ºm3ÂD/HÆ(íJ±¢ã¶ï¢\x000c\x001f\x0004\x001bÚNÐL\x0012\x001fmÌ\x0013~ub/B\x0000Ïìø\x0003ÒÃH\x0004âöµ5Q¥æÎ*w\x000emeàk¼ß$M×n¯Q>¿ZsÔ6VY\x0002\x001b®\x0019iÐ²¾æ&4òß0Y{B\x0006xÐ½\x001a½\x0002Ôï¹6æñ¬cöyaLÑç3¹w¯ï¹	äÈúQ!(bª¶öï¹	íB3\x001d«</p><p>\x000c*u¶Ô)4ë{nBgiØÞ ¤	Y¦z\x0004\x001bM\x0005ý¢ëüHÞ\x0010ÃýQÄÜh#¿ÒMèJ£v°ª5ñ­\x0005¬Eúo[µãIg\x0008ùdXdiÌ\x0008ü\x0015I/Xçöí\x0013\x0013\x001a\x0010\x0006ÈÕ9duÍz\x001byªGGïF\x0008"-ý\x00139Ñ²®/Ú"KÑ¶¾q'´§¯\x0007^°ïP\x001bRÞ3§ºßàkÿÄ\x000e4!\x0006ÏNõ¶Ç/o°í¸KÚèv±À×JîYÓµyb"ÃF,X\x0006m§©j\x0008òfí4µûæ	­úXáø¨ë\x0016
VG»\x0001ü¶{bBÃF¼`ÓÔP.O®xµÇ»öÍÚ=1¡+Ý.>Áä.j×\x000b_©LkÃ\x0001\x001dùâ²\x0011 VÇGê	ûµÍaB+ýsMw<­\x0010Ç+ÄõfmsÈ¸ô,äëÛ £î\x0019vjô¯¸¶9Lèüµ¾úØæðEÈv5»¼=-Âê¤\x0001/¢ùü°¥MEö¸ß¸Wè\x001eÑåÒ­°×£Uý¬E­ì\x001e÷F¿P{o\x0004©½PÉ^çÄ\x0012··mÉ.¾\x0017òÕÐC¦¡;\x001aº¯ú¦ñ|üÈl+\x001b³M\x001e:ñCÃJk6@ur&2{59ÁÒä êM^*¸Ðáp\x0002WØ¢wüµk&ú«o\x0015'~$Æn5uQA¼wÔgíY[9v\x001fi^uÃ\x0001wR\x0013Ó­à½\4Æî¡"ßÐý;¾#\x001f/£M2_~ÑL#w]\x0013í¶ Ë² yä©Çóa«&5/!NgÙEd/7ÍtÒ,	\x0001ÃY.\x0010|y{ís¾üß\x001e?<üûã§ü¿wÊ·7$3÷¢+ÞâëÑëy¬ýìLÏ<¿UÆÜ\x0015Â\x001f·Õ­*c.\x0016\x001d°zÐ"\x001d!>îüó6a>A\x0018Þàgm\x0013RÞ¡e¯o7(k\x0016\x000cÅÕÖ³ê´¶©äÏ±°\x0015FµÜß\x001dñ»´öDR*m¡\x0017ö`á¶Ãu5õ¬:­mªëçÉ
9³OzµjiÅºÕ@ÈèÁN7bùJv\x0004¥\x0016\x0005\ö9â\x0003\x0019R\x0012ÑBsdµöÆâ\x001cqC³æjÕAØ´+Üd3Wàt\x0005<Æþ	7FµUçMò(\x0018%RTägR5H<|{WOÏªÄ&elÉÂ= :8s\b\x0018\x0002«WKZ9¥d^x\x0017ú´ÒÏòû,ñ5\x001dë»\x0002+¯]ø¡¹Ê\x001e\x000fÓõ«EV)!±fMæªr	Jy(îÄ\x0013\x0019-\x0002Rsr`U\x0012±,bä0ô®ö\x000b:¥´\x0013Îã 
Qs|QÂm1ìÄ\x0013\x0019¸\x0017\x0012Å:BÎ´ò3H\x000c\x0017Ü\x0003ÚôÕÂ|xEëÈªÊ\x001eG}bã[59Gæ\x0003ê÷l aø¼k\x000bzÙ°pü³\x000eZöÜ\x0002ç³r0Ý°rã¬{ Ã.4JÙÕ¹Eÿ¬Í,:v[6Ñ\x0006Ú¼\x001cp-_Y)Gù¼\x0017\x001dÈ°\x000b
\x000bä¹¢\x0006]º
ÃÞfB\x0003k$VTõ\x0013\x0015&l[j¡§W\x001dÎÜk¦B\x0003k¤\x001aJÜU\x0001R\x0008ÙÛTÿ\x0006ÞH;ñvªÿ";«VôØ,WûÐ\x0001qD\x0012vpâ9OYÆö\x0015µUyïY³ò\x0007´\x0007¯@ª\x0013ÒA×xVgë©À5+?a¿H£\x000bÆä	ïób¯\x001eö6:\x0013\x0019\x0016µ¯¼ô\x0014±/kñ¨\x0003újU{páÚ\x0007½¯\x0006ÌÛÜùUí#Ý»àÓ²Ë»üî;Ðù+CÞ5u>\x000cåéÚj^`\x0002S§ô6q>Ï%]D\x0013\x0014Ömÿ8±¬LÕcvÛÜè\x0001}æFÛ%MåúìØgÔÇìÔ {\x001aiÍ2NèsÔòÑà8M¾ò­\x0015,?\x0001Bì3½f\x0019\x000fè\x0008=r!ÒèXñ¤-áª\x000f=»Í2NhhesÏSeÄ\x0018îïé5Í8¡¡é,Tº\x0014]ê4±\x0013:pDÌ\x0002úlê·9¡f/\x001aüÚp\x0017òÙ÷\x000fß|z¹\x0017õ¬-!¥Kln£-Â¥\x001e+æ[uZàÛg¼£Û\x0004ñ;zðÃqªêí¶²\x0011°Uw\x000fé\x000cæ\x000b´ÿD-êµ-ÈVÈiË<ÈO·´\x001ceÌ¬f¦¼1¯Ýaya	\x0014B\x0015³Þ\x001bM°\x000cÛ\x0017ú\x0004D½'½Xê;gòÊaÓÄmÛæD>\x001f3ûu÷êÝ\x0011Ï&0\x0014\x0000Ú-:GmÈÌ\x001côn7ËkO[ÖOÿP©3LTÞI~­½/\x0014_Øog\x0013¹ÒÑ|ºÙ©1+þtÏä®Y\x0003\x001a²</p><p>ÑPãm¦·´4ý\x0018ôÆo>ë§î\x0017zmZÏq=üþãñ/Ï\x001f¾øÙû§O÷Ê&J;\x0010Æ:­Ç1.þ@ãwi)¼Ù)Øòã­ëYéIxqK\x0013Å«+\x0014~ÚE6îOÁ\x000c­ëÒ ÍR\x0014ÔË;ÓP¢¼B>ïû\x00143Ê#Ë\x0017E)Þ²Ôõ£î|\x000cÍë) ,7íÛrd¶}x\x00139Â\x0013öá4N%dV0´\x0017½ë\x0007.ô®K\x000f{MU²¨½Xô%lÙ·\x00138ÓQÓÀUîã×²èf+>q¡u]|#\x0003|¼Dúc
W-8ïöéÏ\x0003\x001az×E6\x0014ç"¨Þé¶\x000cþÐÈ¬^-fëhÔþ\x0014g6Jxî\x000f3íØtôö7\x001eSß<¾|÷ôþýóo\x001fÿÏ?Üç\x0012¯\x001en¡ª·c*Æ\x0010PZº\x000e·:¥\WLÿñ^\x001føjÃ>Eécâü_,ºîS¯\x000e¯m%\x0007¬\x0007X\x000eÔJ \x001b¤6ªcl4ô®=G\x0007òi(\x0014%§)ªG\x0006j¬ª¥$Ú®\x001d¼ö\x0005\x001dÈ\x0019Æ\x000ca·\x0019hñ ÷4H[ê¦S¥s\x001dþô¯í[tl8Oï\x001f~ñòüøáNÑí\x0006È[w>®Ò;ôB1½àòf
æ9|ÚK,]+TeI!*Sp¯\x001eÉÉlð|^?âïà²<ñ-(\x000ch~~wÎëÊ§:Ïk"WGZÅ^ºÑ¨`9öäÌÊ9!7ã
Z`·k´Sbd\x001e~ØÊ\x0013÷¼'²DÝ¬l)\x0015¡ÄSÂ0(YY8\x00072¤f,õä\x0001Ï°Gbe4\x000e\Nia	Së´]Câ­0t%6\x001d\x001a\x00074$Oj!WjÇÜÀöù@öp¸_\x0019Z\x00072äN²#©i\x001bÙQ[[=\x0006¿7§Èçbnÿ =\x001b<»5ù îÌpõVò×\x0001
Y\x0019\x0011\x0016\x0004hk¹bØ\x0016\x0019¿HüÞ?c"Ã>ië7\x0017hF¶I-çÑ¡qµQ,¨\x0001µâñíGTy/¬	>ºóE¯Ã\x000cY;qBË=\x0015\x0003J-¡ã¶u C\x0015K\x001c\x0000¥fe¤¤ºr}_\x001e\x001bsÃ\x0003\x001a\x001e\x001e¢|faYI\x0018)Í¬àÌÞ?cBC°<\x001d£&R2£EñÚé¬ì
4&4<=D=-ÎÁçå¾ã·ð°*¹Ú/PÊèÕÓGdA.e\x0013nþ«íâàí\x001c\x0006#òÊöüª:ë°oÐðJ\x0008E½#WP\x0015OJ0\x0017Î\x00074<\x0014Ä}
³h4Q|\x000bïUÚ!]ô\x001cÐç¸	-yëYï\x0013º°Ôa0°·é\x0002\x0019ÐPoï\x0006\x000f(,w\x001e5ó\x0002Â¡`vÜ®¹\x001f)aò(Úß\x0016JQ_3p\x000bRðÇ¯Ü´9ç'7íKg}KMw:ç»³!Åýv*Ò\x0004ìÔ\x0005\û-¹ê¸Þ\x000eÂÖ\x000e
.4Çäç° mO~~om\x0014çe©Æ1QjU+\x0014«îË|Õ~Ò\x0018¿dl\x0001N¨½ÿ88Â«ñ9=¿ûÚéqåjòÛÚ9'¿=ñ\x0004kW)F\x0012.ë\x0010ÓlÄa\x0007\x0011\x001bsyz\x0017ýÓ\x001e$¡
|» ÝHGZ¢M&+ú}o÷:®¡|Ö$fUÉ°Â'8G]<\x0013Êje2\x0013ÜV}r\x0002\x000c+G</p><p>\x0018*×\x0016î±ä¢\x000f\x0017ÖåY\x00152l&"¶OÈh3¡'ï7&ÁY\x00152lÛ?$Õ]Ø\x0019¼\x0019UGpV\x000e\x000csÁèÆ±Ep{¹×íÓìÀM?ÁE\x0007DÃv÷2\x0007[\x000fØm¦`\x0002¤Ý0âd¹ÀeX£EPnû4;ËO^ß&¯î°íËì\x0000\x0006­¤£ê6\x0015í\x0007çhÂ\x000c\x0011{VE\x000c\x000b±¦=î8\x001c1{dwñ2;p-
\x0019C¬SÝD"ÔË1Z¯v\x001fð"Û10ÕëQSMÎ
ù{æG6\x00016su²?_êI¯{æ't} Â,+ÎRµÜUï®üÛ³ª\x0014µ!£×\x0011\x0003­øÚ¨ÃèB¿Ú@´±@NÔ(+\x0016_YñTlj.:ç\x000fäL_\x0010®[\x000f2-më¿à`cmÞ|\x0007t¥©=(ôKRh¥ð¨{÷ÃÎv>óËL$åðu-ÝD|.gÚ\x0016÷«u\x0007D@{(\x0002!2M5wÏ·A
×a\x001cÊªÜ÷Óï\x001e¿{~¼W¥Ï\x0015ÊM´ãAÔóñp[±Vÿ	ôh>K ºM®òyÖ\x000bö.EÑT\x0007kÜ\x0008f©òyC\x0017y»\x000b2½\x0017ÈúØµ	Û\x0016ù&°g`Ð6£\x001aÑ¸à3;nÅ6'2<´]ddCV\x001b^ôÝ\x0018¹'¦ÖCÊ,E>H
\x0018Ñ.§HacÚÖø&,Ôø\@\x001d9ûèIàç©\x0018´íõ2KÏsµ0Ï_	ÙÛùÔsRk`*#7P\x0013Y"ÉK\x0019Ó^bÇ(ý|)î`rÇøB£ävxÌ¶¤}`ú¡Ë\x000cÞñºÈ<æ£ÕîjÿYÜ\x0011¯öhä\x0015ÇÞ¨]\x0011}\x0013!¥*)ÙöL¸Ô!2AtÕ!sµý,n¿õ{õxÜ\x0008\x0007n Ïwf/:´UçEUÐ\x0017Yá\x0003\x001av_\x0018;nBgK
:«#\x001aºe\x001f"\x001cÐ°\x0003Û+üäúvhÊe»ÌQ^\x0019}5W;Ðb\x0002
óï±ó%Ouàù8t®ö =Ø^\x0012ç¡\x001fkà\x0016i±cä!\x0018uµ\x0007!áB\x0000ªo¬.1\x0015Ü\x0015kÊØd\x00074f\x0003Þ'Qø¹T\x0002\x0013,{Ãæ	
°\x001b'\x0005#Z¨Ú+¢®4!¹öètq> a#â7l\x0018£Ú\x0010ä³1tÜL\x00072ìCq=:§ºd¶ú\x0012O9Ú9õãnp> \x0003}Å³Å5\x0016Q]¦1óq7\x0004ZÖþ	»¥d«©#N
y\x0012>aE
W,-æ\x001c¹çø1Ç\x0012×ø1zÅýíÓ§¿>=üâÓ_Zpöðëç?></p>
  
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

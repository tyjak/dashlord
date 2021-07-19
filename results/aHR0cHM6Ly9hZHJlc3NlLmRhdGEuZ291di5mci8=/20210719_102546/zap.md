
# ZAP Scanning Report

Generated on Mon, 19 Jul 2021 10:19:55


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#gNLF`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;¿\7\x0011¶n©÷²!êþèá»ë¿n\x0002mdINÈtbÞr\x0005«¥Ë£OO\x001f¯â-\x000bØv¢\x0013o8äH±]xJ¹û,¬6¯sÒ
WUpU'\Gc<Ä>xáñ\B®ÕþôU¼Þ\x001eô\x0019{\x001bûËØíÑÕûû­±\x001b·9£\x0016\x0005p\x0014¶(\x0012\x001cÔ¯7ÄnN_.Çn´±þ6¶\x0011·`\x0008\x000f|¸$õ\x0002IJ¤Í·wÀV¶­ì\x0000lnR8|v8m\x001f\x00028b1Vï¸Ü<4àvc¸±\x0019	º22n#,ý\x001eë\x001dÜjÌ\x0014\x000c\x0007ú/ä9^\x00001ÃÆ\x000e*\x0010GÂÈ\x0013B:$\x0018\x001cåfe³\x0007wîy\x0001\x000cK¬Mî a\x0015²¥\x0005éQ\x000cñÃ½äíÏ×\x001b£üØ\x0001ãô+\x001cåÈ£"\x0005Éðy&²}'ÜNWYó\x0013vYacØÚÑ vÇ¢è¦=\x0016»°
»\x0019ÂÎ%]å¸î)«\x0006Ä}V(µ\x000b{!\x0018°;>´îFe¢8 WO\x0013é®\x0000\x0012È$öÁ®S©¬ î\x0015ºwªMÿÛû»÷W7·\x001b«\x000e\\x0008dðPÜ£~c$Ü.-:L¥éÿq~yñüäì|¡ôÀ'þ\x000e\x0000^Ów´\x0002\x000f\x0017[d\x0001òCà|¢;Zï!Ù\x0000ssÐÙ\x001f\x0002\x000b_F(Oî®ßoõ \x0008B*¦¼ »"\x0017$1\x0016/\x0007\x0018£<¹8}¾ØK Ë
²ìÆ,²¨UºåqÚ!\x0001'5Âh\x0014ò\x001bæRQNÌá\x000f\x000fb;`+\x001aTTQ~[CcZtßÒÒ¼\¸×ÌÖ(?Gv\x00000w~'Ðùýu\x0000Åû¡\x0016à,E<\x000bø[;ùåúGÐº{útcEÀª\\x000c!Bñ\x0016!3)Ôl6ôY\x0019|ÚÉ³Óï@ô.ü'.$CYýuÚ3Ò èü\x0000©\x000bôdá(É¤&r6Óµ­G\x001bÁ\x0016ÁF\x0000\x001b/=hm&NbÔîïi4ÙÙ\x000cy\x001bÖ"\x0004
XãÄÅWÅ³¡ üX·\x0016? «\x001foßm­*IÜNá\x0012\x000cÝN*ªÿ¸pB¬Ì±\x0002tòêÕùÓ)½A¿\x001cÀç¬ÏÙ0~MYÅðÙáø©Z\x0012e;ñ«
¿\x001aÆo`â7á·ÐJðëíº\x000f¿¨Ö_¯¿Ë'5gÈ \x001aðÓíÅ©Y\x0015NüÕö\x0017ãûb1áúØZÄïÆDÍR$ôá/d
àóµ£ø
§é\x0015%Y"3	øI4:\x0004¦³yÉ>üNø\x0018ÅïÌ±Åý3U\x0005Â§`(>e{á\x0017"jjFOÿüÝÛÛ`Á
5ú)X|M^Ö=[róÏ>:ÿn\x001d¤+Aº\x000ecô\x0014@2ÚÖÜ¦£s{ÀäÕZòÅ\x0014\x000c®ßÄÆq~\x0016Wr^Ï^«\x001a`Ú
¦í)HËZYüÚ\x0001§(`Sª£Qªx4Fo®ï·\x0012áEäiTC\x0003{3ð\x001c¡~\x0019!åóÓôôñÙé%\x0010à¯b\x0015\x0015VÑ\x0015ä\x001a5Æ\x001e¹eÖZC_'õlÁZtl\x0004¬qÜ¿\x001d«±\x0013VMÙÖ8:çølÚ¥	«¬ÖUv®ëDqÌ4ÔRÒ\x001e b6ô{\x000fAuòàëw2~ýeÞöåÕo·¿_Ýý¸Qç×e¥41¦0¥¤tb\x001cÂ]OÝ¾<y}þçï^®¢/â þ°8Ñ^\x0013»n¸ïQ\x000f¢\x0018h\x000cÛ\x0015|Q¸\x0002\x00031\x0006>b\x0012Uj}æC"óDêM1Ð«Ã4´!Üýê§Ük\x0002\x0019®)E\x000b\x0019X¥\x000fgÃñ.ÄTz6|\x0000ä'Or³	¤¸\x0016÷¼:(Áÿ((Á@·0/JÊ\x0008ô¸ó4ª3?1Ð½Zv5¶ì@>â\x000bPÌpix7\x001cÜèbÔ¼²q\x001bvò5¢hé``	\x000e®ßs#±¨VÛ<MÀSë\x000c0t´l#©ÃE8_.\x0017FB\x001cÔ\x0013ÓÜôÝO\x001b]»æ\x0002*¶\x0011ºud,EÙlR¬ajúâÉ"ðXá*(Q~p(ùË¯ï¶¶±Im³Â#Pj`ÁPrÔÙôy%ñøìÅÓÓ\x0010\x001fa\x000b[ÂþDXµ\x0005wXc"De
µ¨\\x0008\x00002;ç¬{\x001bnSGý\x0010¤¹\x001aöý»ÍUPÉ\x000eäxP\x000bÉK=U·(^>}µàÊ\x0011rAá\x001a \x000bÙYg®bÐ.cX¹Ë\x001fV·4ðoÄl*Ì¦©#\x0008¤âÒ\x0000\x0010¯'ÎÖ\x0011ËCï'\x0019õfö4fz¸	¦F\x0015>&2ÿ§ÆL¾A93ue. N×b2	¨ý\x000e»IãQ³U¼À\x0018\x00042i¼C\x001fs$TDîçä¬BlÝQ\x001a\x000f\x001bP/XÃ?E_°Aü"_\x001e²ÀÄ\x0013ñ\x000b¢\x000c\x0001ùÂU\x0017~Wáÿ¤·\x0015¿£~\x0010\x0005c*ðÓ¥RÌ\x000eÑwâ/\x0018wð\x001a4_ºdú\x0014ÿ,h#ü7É*Gÿ0ü\x0001rô\x0011Ú\x0011@;
F$h\x001b»P=Ðæ§á<rÐ\x0005@³JÎ\x0005çñoGð·£3¨/Áß®îÞ^ÿú FË/ÑÂc?^¸\x001cc\x001buðãÒy´ÒFÌ
\x001b-ÃÕþ;ÁïÕ}\Þp\x000fÿs\x0006¢KP Dw"Ó\x001eÁ=¹¾û%üò§\x000f÷wº¸~û\x001e\x0000ê\x0010tHÜ\x000bÀZÚmB\x0008Ë0åd¼*Fx^<\x000b¿üéååÅ.N?{p\x0006KP¤£¹«BT\x0003ÿêC*ô±	i\x0016cl\x0006Ri´hð\x001e\x0005
a#ü«\x000f(7(Î¢#H\x0004É\x0001¨BápÀ\x0014\x0001õ Rßz\x0010ôAenVá²B\x0006\x0002\x0004\x0015Í}PÍoâÝÛb>\x0004GõÛýõvÌi PÊÛ\x0014\x000f{£-wbéÕ?\x0004\x001fõúr¦?¦\x0018^èhU
~`/]»aô\x0012GDa\x001ahi\x001d[\x0010\x0006¡¾BâÝÿ~ã\x001cö\x0012Ä\x000e³p\x000f½»}÷6C\x0004:,¾\x0002i\x0000ú"#\x0015:wkd©ûÌn\x000cwÐó§3}Ù%ÆX\x0004?¾>Vÿ¨ÿz\x001d\x000f}\x0000	ÙÙû»XvßÑð
\x0005<µqèC§Î§\x0010\x001f]^¼/½×\x0010©ð¯\x000e´d´N¡è$=çH%	½úz\x001fÐç\x0016{ÝÚ1Z¢Q
 ]R\x001b
ëèQÿÃ1£vÂ\x0008sZ¶o\x001ds*Ak'´5¼k\x001cö\x000c½Ýé]Ã¤H\x0016ù×\x0011æÏ]×:\x001aÆPf[k\x001a\x000fûQbjÃ±Åèb;Ä¨
\x0004b¿Þuÿöÿ«\x0003ù¿õÛ»ßßÇK]ØØð¯3Èon®~j8
!\x0013Zãu¸1\x0000!\x0005ÐÙZõ\x0015\x0017sÂKOÈÏÎNÌ\x001f\x0013N\x0008¡¤ìÄ\x0019¢²äÈbÇ"¡Ô>£,Ôp\x0006QB\x0017ü«\x000f%	%@È(û\x0003N#RºÊz¿ÛbÂé[LÏ\x00126i\x0011&­\x0003L¹\x001c7àò§í[NÏ8éokhâ²&át\x0014«ykv[Oòê}ëIj|\x001a
«Qt\x0018ÖSegÏ\x0006S×÷oþ\x0017f@bÞãá¿þù·ë÷Wï·_r\x0017\x001e&Åã%G©Ä8\x0003\x001cèéö`*©ÏE¾9}~27\x0016\bdäø£\x0003¤³\x000csJ w·[á
îMàÏ\x001fBùËï·ÿõ·ÛlÁ«\x001an>Ã4ëäLø¯\x0014²¯¥
^Ì*3×\x0018Ó=ì+ÄxÅÒ´S.\x000b8\x0016ªÔ¸ýøîÃD9rs}ôâ\x00063Ñ[?¦ðÖ5\x0005rÈ\x0011Ï4Èìb@\ÖV>üüÕÓ/\x0013çHø°^Í³\x0005\x0014V¤Æt²\x0002úÒG­°ù$ÐáÕÉÅ:ó\x0015Á
³x;ê²ÂUV¸q+8WÁÑEz`°ÂÃÞIVh¹\x0014ÃôYXzÈ
¸\x001a}\x0017 \x0018É³\x0015*E\x000fÎ9º\x0006jµÜé±3VZ\x0001Ã/ChäW	7E7Eí©\x0015ÆÐ}÷\x000f\x0003Uê&3Æ¿o\x000eÜähFâFL{Ê\x0019%Åà^fðúmð\x001dÞ\x0006hb\x0019|\x001b&ùÀ\x000c<óÃÛØýËà©ª­âÊðjH\x001bÉÉKyIoh^[<%ú¬Pµ\x0015j\x0007+\x001cÎ\x000f-¥S§R0C1Kfì÷}\x0003Q?æ\x001f§?@&\x0012Y·
ÒÂ\x0006çü±ÁèQÛTg`\x0008¢gbé\x001d ÛÖ2{a;ï¡\x001b¶P?p¯0TÓ@¢¢s#é~ËÕR¦ \x0015·ä%nÉ\x0016Ü\x001d\x000b¼¥4Å\x0005\x0017®?ËVä9BJ;Å"çÜ§©\x001aùÒFo\x0005nª%7cKNCñ$q¯pK\x0017c·X]kF^-¹\x0019[r
ÂZý.Ò\x0010­Y¸Ûí¹Ë]µänhÉ­Ç	\x0010
Ã\x0014\x000cÝ
g´äf1vkEîE\x001cX±ú\x001b\x0018¬´´<1\x00001\x001dÜ9Gàí\x0008óÊ!ÂãÈsäÑ\x000e±¡DöXF´^}¶yâfs\x0013t\x0015â}YP?¦Bý«ûÆ\x0013z\x0005²öB\x001a:´YÊ²eÞÇT±qry¶jç¥\x0005\x0015!g\x0005Â\x0003\x0005S¼u)vl\x0005Æ3,ðf)Dî² z\x0007~ø\x001d07½\x0003:\x000b\x0019üYÑ;P\x001bvP\x0005<éf\x0005ð8hö°òñ%$]êhµ\x0014\x0018Ø-.³É\x0004Ym#.÷Y¼h\x0002ÓIÆ\x0007L ²ÌÎ&ÈÚáäXÄ·\x0010BûÿaÔÎâ ¡e÷où7ï>\x001c|Ïð!;Â?r« ø)õ\x0010{Òu\x0011r7{\x0019áÄ´Â&\x0010Höþèæê>Øpòþãí»÷×GOîßÝ4
 ÉEµ\x0001²àQ\x0005Õ0ôb
\x0003:-\x001f\\x0006SN¿:úüôèÉåÓ³åc"Ù#Yid;Ù\x0013®R¢=\x0002\x000bÚØÉS¹ÅczÀ\x001eQÙ#v²'\f\x001ahÓ$¶à`£\Wøæ\x0017ë~{Tõ~ÔnïÇMïÇ'fBx?v[ýqÀ\x001e­J{@y|\x0017{Â\x0015\x0013¯\x0010àÐðd4Þä\x0002¿Z<ÛûíI}dñ{í7¼Z\x000b/\x0016\x001a?Bt·èØúí±Õ~³{í7-qz&ØC\x0003ÚN[\x001eûíq=n7{¨\x0002Á|"Ô\x0002{\x0014Ï±ä²§:Ü^çR¹\x001fA\x001aJ\x0019kèÞ~¡ýæleÝëýðc
õ\x0015h[Å×Ã(sÉ¾7(\x0002~\x0001ÿ.Ö0Jaj%±ì\x0019Ì±ÂdU¯~{¦BE´'\x0016*v1È0äñÕÒ\x0017¿\x001eß\x000f_?ûíáÕ×µzí±\x0006\x0006LR;Jô¨Ð(Ãs/!ÿ2î ü^\x0019\x0004Y]\x000c\x0002ígô×V\x001fc\x000f¹@É¿LxÀuå\x000eàq\x000f{|ø§\x001d\x0014¿i¯)Þ±VÓ\x000bR~wÿ&\x0012iØd`G"ßx]ÝÝàÄæò·FþLhPN3M\x0010JÓ{aÜmHN\x001e=;¹8³\x0012kè
+Ñ\x0003§à\x0008úðà¡\x0019ù\x0010\x0013xÌ
Ö»åwÐ\x0002^\x001f¤¨N)ê4\x0001\x0007´mw·»ºû±\x0001<¨Ñà'.\x001d~\x0011!þ\x0017ù\Ù?üüù«ó¿\ÌðØU]a\x000fÑ>ÃóCÊ4\x000fÄ Ù=\x0017kþ¶
}q¨éPïE\x001fb{µ8Kì$\x0001½È]vq°¡\x0019ýTÖècY{\x0004¾&þR­@Â\x0017[VÔt\x0015\x0016k¾t+üÔ"!¦\x001b0Ó\x000fD¥×þèêîn{jÜ9X9õtª¹\x001c´sëÂB^óäâb¡Y\x0017W]®º\x0003À` A×r½NúTßpb±JÐ'\x0004Bzû¡o
@(TcV]h»äj±jÕ¹\x0019ZvûÅ*MI,¯pTØ	·\x00185´"\x0017¬B\x000e#È\x0015ÍLBKnîf²À{½[o\x0000/ÓW:¡¬ôüö÷È4°9sèsfÊp´Ñ@Ð¼\®%qÃççSû) \x001b]B6º\x001b2¨J`²Ó\x0018ú8Cti\x0008³\7`æõu^Õ×Ahøêc\x0008#o[\S\x001a#ì\x0012JËÈÅy\x001cÂ<úþäU\x0008\x001fç¸\x0003Ü7,Ñ0ræ\x000fÁ¯\x0007_þäîêýG\x000fo¡%¦a{OïX¦L¹Q\x000ex å\x001fvµ!_n|ùçß\x001d=<^W3Ìâ7?þöëïÿýÃ4wvuF°\x0001¢OsÀ¢\x0003þñúO¯~¾¿{÷Ó{\x001c\x0006VaY*M+æÀó\x0007áü\x0004Ý³°Æ!úÕÜ\x001cj\x001a~wú§Wß_^<}ò\x001c¢Â³£4ýùµ­a}f¾\x0001áä¾~Ð8\x0017çzp&\x001bq¶ M8E¸â ÎC.\x00010·ÓûÚ\x0003Në)íqé\x0010¦>T
l)>Üýúþ#È \x0010\x001a@÷£;YÞ\x0008ÔJaÒÈº\x0012@·
d?Ç\x001eÄ"tD\x001aÀò{\x0007Iùå\x0012©Ü`üÑ\x0014úHç¨°\x000eó\x0000©òÒ!ÒO\x0018ýú¡FFø£\x000f*\x0010A¤E\x0015á\x00103	j\x0008à\x0015Aõj7¨Ð\x001fôAUXQU¡MªÂæ¥U]Þ©-Páì?ú¶j8DªÈ[\x0015ØF#T#\x000eéÐ\x0007 \x0006L\x000fâ¾Uõ&ÉLÁ\x0006PÐ¾\x0000P
áâªªýV\x0015J¾ñG\x0017T#Ml\x0002¤\x0012\x001a¥"ÒÈ±\x001eÒ¯ô#u\x0010cÆ\x001f_ýûwpÙ?:\x0017U¥»YX>/ °VU"T%}Õÿ²¿¿{\x001bùl\x0019¤ïnïÿÖpLY\x0006C¥\x0011'\x000f×E 	\x000cçÙ¾tNUÃ38¿;¿üËü9UÀÆ\x001aap½BÊµ \x00000m,CGv%:i	\x0003¦½«Éñ«çP-\x0007ï\x0000Óy¦\x0011¦ðf7\x00189w­¦N¦\x0000ÓyÐ>K«é%Áäv7á\x000bÒ}«ÉLù¼ðÒYT\x000f{3\x000eFRí·\x0018àw®¦áøÒyòJq5io~¢9\x0000\x0013
\x0006`
©
ô¥\x000b³ß'÷¾/\x001d½\x00116f~ãþ´´\x001fc¾ôìLËqcÚØÍ
Î=f#\x0010¦ÚÍiÂ1Á;;´âF>"ðÓ\x001bKNS¯ìa\x0007§»ïóÄÎ\x001c`:\x0003LøÖqg:vÈÞóý_yà®\x0004Åøãìú\x0008Dbjd#ÐpèÞA\x0013\x0012î"Ð\x000c!¤M~ÓÊOÝ\x000e\x001ezÐ¬\x000cK\x00014*³Æ\x001f_'Ðÿ}õs\x001c.\x0013bO.¾kÂçãÓT¥^RhÌ{2·"]\x0014h5¤\x0011ã@)cå?¾^°oÞÞó7\x001fb¾=f\x001fpe/ï>Üß´5ÌÓmÃ|R¼-Gý[üª=¤ü\x0014ìåÅËËð¿gT\x000b°<þè\x0002«}¸ÏÇ¢i\x0000+\x001cpX\x0002Xnß¸C¶Óy¨sëú_@Bòß?\x0000y70jÅði]½}ußðmÙpóàñÛR"D¥p|\x001fÌ#XÇý!Áó§ßÖÉóç§'«X\x0005\x0015\x001f¤_=V\x0011	d\x0004RÈ|XÕýõß`»*Èâ\x000fØ®\x000f¯î ¹×òq	ÅSÈçµ§oË)ü¶\x000c7|5\x0000xxr\x0001ù½\x0005·õão\x001fþ\x0016\x000f­\x0018ê³´°TBÙb?Ü8Ã\x0014¯÷òº6,ëJ¬¿T@©`Â4CüÑ\x0003Ó°$\x001c\x00070\x001d4¬D\x000c(å\x0007XAùÓoo7\x001fË\x0010º\x0018\x0016>¹\x000b¿_½¿º9º¡ð¥e3xëS×D_ ï Ý¡­St\x0001P+\x0019´btøä"ü~òüäì(G5ó;äç_?¾±?ÂÒÃ}MU=CÞýv]7ÛK\x0000:Ü¨È£ÎÒñ&%¾ð\x000eEwk;¦ªÕÓ×\x0017ó7\x0001øÕÿóî¿>Ä\x0010PÇ ib;\\x0005\x0013Ï±\x0010\x001bNcgS-x\x0011#ð²Í>\x0011×údÏ@³Ä,ÈðOe?L<õé\x000f\x0015O}d\x000b~x\x001b\x0016ü!Iyn>ð ¶À{ %Jk­$æ\x0007µà5øpÿáyXøKò9(¬æÔÂ*\x0003öHúê=ÊÂµ=Ú#\x0018F\x001bhìf­Ì±;\x0003i14'HEs\x000c¥Å\vð\x0003öøÊ\x001e¿=ZOÛ-¥D{Â« (|vµ\x0007¹ÎÑCEÀ~{<¹*Ï¢Îh²Ç=\){DeøÖíµwÛË½ \x0015î7naì!}?Ù\x001d\x0008¿\x0018Ì
Øã*{ÜNöXú9À\x001e\x0007\x0012#É\x001eÍùBîMW¯Gïõz¬M\x0014ÐàÞ4\x000c\x0010Es¬ { MäËØS¹7½{\x000bw]Û-
à¥ë#£ÏGíí®¯fXzI8	xð)ËÔÅ=<µ\´\x0011o\x000c'ðÔ9Àh¯I)\x0016£°\x0003"KxZ¸\x0014eKDiÉ§¬_=¤½\x0015-Q±m\x0003L\x0011ÀÒLQjùJ×k,Mùß¨ë¥HthYî'ðV0\V~¢JK>å8ê±[ªª0¸¸ôR,6ÒÚ/c.MÑû¢±\x00173§è³\x0017Q61âÄò
 ×\x0014SböùTDþT¼¡\x0000MÌO2e¥]¨×\x0012[Zò)-[%á& Ð}9ì'qÐ\x0015Ëé¥,ç\x001bz-q¥%n\x0017KL¤=¸½°%NSýDº,O¯)¾4Åïb
p\x0005àîRàÈ¢%qÊ>Y²R>ï´³êtü/¯Ã\x0014/TjWáéc2Ïx­a¡×ú ßå¤÷ZAª;ÚÂ9ÌM`ÔuxÅ¾Ì©Â«£ïrÖC\x0011/EÈÁ\x0014:Þ\,â-*Z;ÙRõ|ÃÞ§\x0012\x00049cLï*®%í1þEâ\x0016^ö|ãÞ\x0006%"³\x000fRéË?êÞÉê´çû\x001c÷^P\x0015"\x0017tbÆÒioÍ\x00179YxuÚó}{\x0013¹\x0000Rd\x001c;\x0005Sª6²;;1sx[1»­¼¾ºAz\x001d\x0000Þ`±\x0014¾@\x001byeF_¿òÞ¶l³×'gHµ\x0003ÿÞu³DiÖ§î¬ß,<ZÁ,\x0013Å£YÚÎÂ©Ðrn¶%K³>õl\x0003fÙ9·\x000eæYÔëÏ\x0004k6[ÍR¥Y:¹M¨\x0012Ñ?\x0014\x00048Õ/¥zÀZ#ëUº´êS×o\x0013Ø¡É@Ò\x001eo\x0006Ìij:àºå0j5Ëf}êû\x0006Ì2IG6}Z´\x0007×È§eK³>½÷\x000c¥P5%-P#$³,úA'¾¤U®´êÓ;ÐU\x000eïtÌp\x000fs-Ñ*Ï<\x0005®ãËåK³>½\x000fõ\x0005¬p¸\x0007\x001e\x001dW\x0012ÍÒüZîð0vt\x0018\x001f}w\x000bCy
ýpôâÝõÝ\x001dô'Ü\½ûsS?a\x001a-\x000bñÃò¢õTN%ÿãç
;úî\x001cFû 'úò\x0008\x0004¦/ gáìäù£ï\x0017*ÒÙ6QÚ&öµÍû$í\x0000¥F\x0003"±\x000b\x000bÜ`Jö\x001a¶vÓ\x00184NÆÉ]³ã\x0003(®Ñ8Þ^¸åÂÉ¸qª4Ník\x001c\x0017]É$\x0015¹bt\x0019áb¹-qØ8]\x001a§wß\x001e³EÂÒk£¤êZgà°e¦´ÌìkY\x0008¦$:\x0013I®_QbRåÎaËliÝ×²pWÁ¶C¦,\x0000ç$])µX»R\x000e\x001açJãÜ¾Æé\x000cÐ«>\x001a'òÕß¬fÇ\x0007ó¥q~ç\x0003ç*\x0006\x000cØ\x001b<àè\x0002mÙõ$EfÓåÌæ^ÆéàJÂméÓ7g½sùøÖ_öãuh²wl"0òçÀ\x001aÞ M)WFøM«"\x0013¾shÂLn³ñ
 vX@5õE­«B\x0013¾ol\x0002zAäñFQååYAaÝZÖjÐº*6áû\x0006'F¨$\x000ea¥Êg\x0001
ì¨òËs¼MøÎÁI._³È¸Æ©üêÔÊ8ê°uU|Âw\x000ePíº§4\x0008Ï¦Ä\x000f3Ô³Z{\x0018´®QøÎAJ\x0008¿°µÒå¡Òéò­\x0005ÿÂW\x0002^\x0005)|ç(ÅÄT\x0008U2[G5V!Å\x00176®
RøÎQä
«*\x0016øÈ}cf5Á0f¨Â\x0014±obÂu.)\x000c\x0004ñ®Ê`Z/Yç¿p"ª0Eì\x001c¦p\x0013ü\x000cÚË0Í\x0010"vº\x001b°/ýîê\x001cÊÎT\x0016Ìù!Ç¤ð9Aôe?;Q\x0005*bç@ÅÄÆtaé<PÔ# WÛ\x001d\x0006­«\x0002\x0015±s \x0002µ6¼\x001d$ÿRÌtõ«µÃAãª@EìEÉùs \x0016ÎÉ½|ûåAqëª@Eì\x001c¨x\x0008íuZC.,ZKTá`øÂWrþÃ_ë¬ó_ÿ£ÒÎü7µyoþÃÌ»®Í»þ\x000f3ïmmÞÛÿ0ó®jó®þÃÌû±6ïÇÿ\x0004óX\x0000X%üà\x000f1áG\x0014²÷GOîn¹¾iX\x000c"X-ÐÖ¤ÖøH!â2ÓÉâI@4²GO.Î-^\x0005¶²ÀY`¼\x0017\x0014dA\x001a=!\x001e\x0004µcå,ë°@éÒ\x0002¸ÓY`3¿\x0010$Ð\x0002\x001b¢
´@-\x0017m:,p¼´\x0000DY\x0006-°\x0018O]$@¨)Y0í"³´j·z\x0017ámdý1Z <ð(áì41þh·ê°Àêú;\x0018ÞFN \x0005*ÏS\x0004\x000b,ñ*ñåyv\x000b´2¥\x0005ºd\x0011ï² |ªä[Ã·\x000c¿	FÒøTø\x000e\x0016î\x0016\x0013­ëð\x0007¨W"qþÍÕÑãÛ»VmÎÁl+§^JrDBÈÅ\x000b\x0011\x0012ç\x001c=>¿x2O"¡Û\x0012º\x001dnÂ\x001dÿX`j3äärZX¼ípÉ\x0017¿ßVèÅ0®e\x0013xß²\x000b¤eçtÉ\x0006½M\x0003ì­Ð¥(¡\_/tN×0È¨â5L²bÚvÑé4cW\x0015v5]\x0005i\x0010»Ë$
yÒË=3WBÇ\x0001ìÞøcÈ!è4EËi»ûå¿Vð²Úî\\x000eíwï,Æ;\x000c¶¾À\x0011zG\x0010\x0006jGð¦Ú4Ü\x000cíHþO\x0015\x0012\x0005£æi\x000c ·\x0015ñåÒ]+x_o\x001b?´m ï\x001f¹È\x0006ÇÑ¿ïé#¨ ÃãÐÙd2ä­\Q&Ô®gPÕ±
#àÍÓ\x0002	V\Î\x0011\x000b³ëÂ\x0007ßBÊ¿¥»Ò¿ý&8E«ÄÔ\x0008#|"ó^°}<NÊ4Ó-\x0011äåù$õï¿ÿãä7ÿúgää9:}\x000f×â7M\x0017`\x0007\x001dªH|Ï\x001c}\x0006B)bËÒÈÎstòìáidç9:}\x000eWâK_4KêÒ,©w4ËbñÏ	{ÌpêURY:Ã7°\x0011\eÛÓ&Ç\x0018±E8ll\x000f\x001f:Þ*¹[î\x0001\x0019°	U\x0018§í·ëþ4
\x001bã½<ÌorÀg¿]Sê"ÚU\x0010]í`\x0017ç8UA|_ Dì2KÔ¯Kìûº²\x0017t§\x000b¯HÉÄJ8`ÖD)\x0013Í*Dè÷x[4\x0019\x000eTSüS £\x0019¶ìRµ]jO»£]\x0008S&³~ä×õÅ¼;8Y¢]xÜÏ.`ÏÂÆ# \x0000Èk@96¡¿]¾òðð¸ççÅVy{\x001fÓ\x0014\x001cÙåæÚ\x0001»\x0004«ì
uûÙ\x0015\x0002=j`ÔÔ\x0004'9ñIöÅ¼¡Ëé@/³ph\x0016WéMa °R\x0010\x0017îrqÀ,/+'ïåNÞHÐ\x001aEJ÷Ì²åõD<¹r»è6K:ÔÏ»ÙeA7ÞdÌaiÁ ]ålPsÀ.`ßÓ®p§aÇ\x000cÉX\x0015ÃÆn¯¨1Å
¾ÜvÓo\x0004&é2ÌÒ»½0n\x0014\x000bH\x001dlt¾\x0015\x0012%É0-Y_\x0006\x000c\x0013õ±\x001cw4ÌR\x0007:J:.Áçs4l¥Â2b­ß\x0018<ïùÆhNÂH'i\x0018xzcFê/è;r%|ò\x001eW;z{í§Kç9º{MIR£ÇU»l\x000b·­xUÎ\x0015>¸~§\x0007/n®Þ¦üE°ìô§w\x001f2\x0018Âàì@tx¡,Éò¹em\x0017g'R
ãèôÉÙÓ\x000b)\x000c2@T\x0006a\x0003tl|MySG|PSHÁí2¹{\x0005¾²À\x000f[Àé./rB\x0013ë\x0008wË¬\x0002íð\x0015+áºñ·\x0005¿Ú?j|ÿ(ïçåû¹,Xæï°@U\x0016¨a\x000b¤>\x0016Xöp¢OáÛM°å;P\x0005¦²À|c[HW\x001f°þf>`å\x000fÊ}á\x000f\x000fpäúèÕÝ¿þùÛm\x000b+»Q\\x001cÛtÁ$Hb\x0004j|Ìxx¶¬ÛYÙ_]¾>_ e'øÿ\x0001øÁÞ ×\x000c7Ö%\x0011>\x0015@@­|GðÎ\x0012<< ×aàP\x0018×áx,twPÐ¦tÓfü>BDüð8\x001fd\x0015°½Æ¡\x000caÀO,óÀµ#|i+áÇç\x0011ü
tÿòK\x0018é>ËÃ\x000c\x00087÷m\x0004«\x0006\x0018­\x000fúRÂ"QùìþèñíýÝûw7MÕ3«gÌ\x0011gcyKÝòòèñùåÅó§gëÀm	Üö\x00037LèÔÏÄ¬wøÁ:Ë\x0017bY/¤\x0011vÑ\x001a\x0011`çÖ®\x0005WãÞy}L\x0011BR\x001eC/Ívà®Ú(nd§Ì=UÁ´¢\x0013Jå\b¸._W-\x001dZ\x0017-\x001d]Ðm\x000cq+-utø|=YÖàh>W#tÎF ûpb=5¸FgqÕ}nF±Ë¹\x001aúÕÝÛë_gq\x001a·\x0018Zrº^\x000c
ôÈè¨¬09iÁ½ºäª>ò7ç¸Ñí´ä&°Wt¾\x001a¡\x001aº\x0018n\x000cj\x0014\x0006èÔ§
åkªTûåþóFè²Þ0rhÃ\x0018Úå¼¹ÒDÁÎ½_>@ÛpzÉÍÐ\x000by,&\x001cj¸b¹wcY¤¶\x0011¹¯½¢\x001fñÐ°DD	!zÇ¤4Dï\x0019Nþ\x001d\x001dzÙ±\x0014 O\x001dK]ÐCÎ±l,ó¢KËÆËôÈUåÏ\x001añçÎ«iÖs&WPõþ¼\x0006è¦>\x001a*úÊEm)©	>\V÷\uS¯º\x0019Zu#\x001f9õÙcÙ=»'LÓ)º
]ÔÐGü"d\x0003\x0005\x0015äw¨o\\x0018JË]N£+~¨\x0014Â?£\x0014òï¿ÿãüî:ZòúÝÍÍUS\~4$j¸#ùG5BåÅò;¨h\x000cÎ/N£]¯,´¼e»Di×!ùî]Vã\x0014ÓZÞª N\x0016ÐwÙÎ)Þn,
;¤ß\x001d3,ÝÅ£aJ\x0010a \x0012û\x00106pº¶\x001b¦JÃ\x000e	x\x000cf*iC<ÐBá@\x0003¼±5\x0016\x0011ÃtiØ!\x0007ïaÒ\x0010·°6Á&IR6øÆüJåvÙ°Ï^\x001e²U¦´êwðuyH(&ÏÁ­VÀÌ\x0015ZµÞ\x001a|]¶4ìwð\x00034\x0013\x0004e[t\x000bÚ«¤CÛp\x001aôM\x001bñjOÓ@yZâ'¦ ¹*&\x000cÖ²U!ß1MØ'ïñf××æ0õ¤ÊÍb\x001cp7ÿ²¦]Õ¦ý\x0007½6]¿6½ïkûÿÉ6{\x0018XÙÏ\x001a${DSJN\x001e\x0013\x000c±KBF(VVe\x000fx¡!\x0001Àª)¢4å3B\x0006=¦xb\x0014\x0006^ZâP\x0014\x001dê\x0010«·hM4\x0018#Kc>#_ÐcÇHÌ¤+é3ÁâHx·1ª4æ3¢\x0005],g a[d\x000ee [¾±ö\x001b£Kc>£UÐe?f>_\x0004§t*å<Ú~än1\x0019\x0013\x0013ñvRÈ4úùFø:ö\x000f=úù_ÿ÷}ÛÈ¤!\x001bl2úà2ÎW¤XñZø:ö
=úþôùÒäI\x0019y_\x0000£6À¬¢D\x001bbÃ|\x001a{lP[r!-6ê5Àã 
 \x001b+ÉØ\x0002F\x00169\x0016Ø2¿D
Å¼(Ø Ù°
\x00018UG\x0018Mÿ©\=ævSr¤Å\x0004k+\x0013¬\x001d6!àé5@±\x0007\x000fªbr¶)\x000bÛbS	N
`©95Ü>©0¨\x000c5 ±-SÇ&èÚ\x0004=nÇ.@\x001bÁÙ?e6\x001c{\x000bE}3`MÐÄØ\x001dßÇ!+Þ3¿,ò\x0019\x001bfjnh«
pã\x0006XHå'\x0003dÖV$äe'ZñûÚ\x0019ùqg\x0004y\x000bø9ô¡§R\x0010Ç¹!V\x0003Dm\x00187À\x001c[<uü5\x0019ß[éo5 vD~Ü\x0011Ð\x0011~\x0002a3y¬hQº%\x0018°ök6 þýø7l£Ê.\x0019­àJó\x0016Ú÷\x0013¨?a?ú	\x001b\x0006ó\x00172\x001ff
ñO½¤lYø¬Ý
V}Æ~ÆÁ\x0006"*ÌNI\x0012
´é\x001dØe\x0011\x001e\x001bDmÃè\x001cß\x0003\x0012ØÔ\x0013Þ\x0003õ4ûÐîïAÖ6Æ§Á\x0006O9|«\x0004Å§\x0001º¡÷°³\x0005²~\x000brü-\x0008F\x000cÇÖ:\x001a\x0011ÖBRxÊ6u¨m²!ÜÌ«\
üáAÙÜxvõëõïw·÷-½\x000er\x001bIE\x0013Fî#w¸\x001723£{½â¨;ðìäÅéÃÓRso² \x001c\x0005\x000baÙ>\x001b\x000c(\x0018d¡\x000b'tj1õ2\x000b\x000f»ÜIÒ\x0016#\x0004¥\x0011ð8jf8M\x00140IÕË|.À¬åÎ6bì+Ø`ª6ë\x001e\x001bløG\x0012±\x001cè½\x0003åR4båÒÜa\x0016\x0011Z\x001aÁÃ.`Æ¹dï\x001dÑr9·Ì+ÙaZ!À\x0008«Ì°\x0011&&#L¢Ôó±WlØ{7¹©)\x0012lp±)rÈ\x0006\x0011\#\x001b\x001cÍ×ñ,¼ìÜ¦ùº&#Då]áqÔ\x0008EÚ£Üxz\x001eò$\x0018qcw#\x001c«plÔ\x0008)82aL\x0013\x0008\x001ed°²ÝÝ\x0006_ùWx\x001cµ\x0001\x0018Çðp>%ñ
Vç\x0017±Î£Å\x0008_\x0012~üá°>ÖdñùXÄé1BW»	\x001eGp<ÓÞõL2/È\x0013-
F¸ê¨ónø¨S\SM\x0008DñMHM¼K!äØÂÐd¯ß\x001f}\x0013|ðÇ¬Nºø<ú& /LÛ)j4ÁPYïÀ­¥;¬P\x0007V\x001fØ
hîødEú(ÔäbíÆ\x0019µ\x0006+«­0ÃþI9ÍKÑ
ääV\x001a\x0015;ÚÕ_E|\x001e´BKÍÇ<+P{\x0006e«Ìj½»\x0011üÀáÀ\x0003`è \x0004¹Àd\x0004£\x0010P.×y»¬\x0010\x0007V\x000c\x0007ã\x001aÈd¶Âãgá\x000cÚr\x0013I\x0015òÀáØCÌ\x000e­}TV\x0004øh\x0005[©´[ÁUýqÃó¨\x0015\x0005]½e©±\x001d¦h9í(Ë÷þ¸¹ò\x0007V&\x000b,\x000c¡¦áð.rô\x0001ìaô.ä¶Î\x0006+ê\x0010*>\x000f[Áq²Ãkaè¢,ÉdºeñÖ.#ø\x0011ã.Ê±<ØÌpÞ \x0018a$\x0019Á÷·âà´àã§\x0005(ÔiÌÛxò³á\x0014\x0008óÍÛ°\x0005}\x0019\x0018a\x000bþ²ÎHsäH	F8`Ç\x000eFðÁÑi·÷aaí\x0011vØ?<\x0015W'^|\x001e4\x0002Øjð¬âDJ\x0018\x0008N|ö\x001e¢}(FÎ£\x0011õÈyß`\x000fÈ'÷$£Iâp×ÞÏÉP¿îb
]L¤è0Éæ4\x0014ê@hj½VPjç"\x0011gË¥RRtrÖ,àY\x0016.Z\x0010E/ÆL\x0000zOªöó\x0002%
\x00055a2·<D×nÐª4\x0001\x001eÇLÐS\x0005x0Q¤\x001cø#2½ñ^&¼IÔ)Syâ!P§ÄòÄëï>\x001e!°\x0017`\x000c¬zü\x000cM9}\x0007lø\x0015å&Ø\x0017§¯¾::Ã§5Üy&-á´^Ü\x001aæ\Ñ\x0007\x0001³H\x0017']Nn4\x0002ç5p>\x0000Ü8¤\x000eÀi²Ûzã+Ee¦£\x0016à2;ÿ¨L\x000cì\x0010D ß\x001aPC£·a4\x001cm¸XJm\x0003.ª\x0015Ç~àÚ¢\x0006\x000fWÎ,M´ÀÌ°#nUãV\x0003¸Ã1+RØæÃ¯\x0016\x001c§º
WËÓèmÀë-.G¶¸Éóa<ìfÈS¨¤;«\x0011¸Ýs§ØÊ\x0019ÂãÀ\x0016\x0017T\x0002b\²\x0006\x0003e#Ø²ÜM\x0013p£\x0008\x001c\x001e¿->Åb\x0011w\x000cÅ¾	Ü\W¸!Hý6p×ëÍ¿õö5î\x000fóÄ]\x001f=ú[9ztÎ'Ü*ïÇM²_+K4\x000b \x0010\x001c¡\\x0011Ml\x0002ntufÂc?pGãþB\x0008NCj\bAÞ\x0000AÊ8ðð3^%ÌD\x0003\x000b·RS(=þûïÿøþúîMÓeÒ¤\x0008\x000fw;Ø\x0002§!Bð¸½¤ÄÑ÷§\x0017\x000fê\x0010¿Ú\x0016yì`cøÃ®áØ ÄD\x001aw÷¹\x0017B-\x000b¢´c×5v=ÝZºÆ	å±m×\x000b$t\x0001þr´Õjú-y¬¼A\x0003 áÙ\x0000H	l1#I\x001a¥üò Y£\x0001\x001c$S
\x0003âó \x0005!nÄÞ{\x0001\@i\x0007	7éÈÃ´§\x0001I2@ÊA\x0003<³Ä\x001f\x0015V\x0003'²¼Ñ¨\x0011¹.vµÀ\x001eX`-\x0006ü°è?½Át\x000cÐ©ìù\x0011pÉ+\x000f\x0014\x0007
\x0008'\x0017¹ A\x001dÞr¤"\x0005ªí]_ôº¶À:¢?ø+P¼6\x0000\x0007O1CËá\x0014ã(/â\x0016ô
ôò4Ùf\x000b®x\x001a\x000e-fÃa`vÒ7\x0004\x0012\x001eÚ8\x000e³cÅÊãÔr¹ñ{fÎ¯"JSægÃLúû`6\x001c\x0007j!µ\x0015Õ~[diËühx-@ú¶ÀÇïEdx¶¬ÔÐo*\x001f
o3FCË(Í¹{\x001c
4ê$\x0019ëa Ø`.\x001f
oû`tæÜ	+ÚfÂûÅ££ß\x0018S\x001asÈÓe\x0001i¬èI¢ñN3¼ÿ¢ç®¶$M,\x0010e_\x001cþð \x0014-¿>zqõSËà;\úT\x0004g(Éà±Ú7Âl:\x0008O^<Y\x001aúHÐ\x000bÖVÎË¼\x0003;0ûà-Î&ª¼\x0010[¡°v¹ÀØ
]ÖÐå\x0018tKuEÁ­:N\x001dá\x0016EI\)onkèvlÕmª°\x0007ä(Á\x000b«î3öÝ×Øý7±Ûc\x0011ÑêÜº$ \x000b£
ýþèáõ\x000fW¿7Ô¢E¸{¦lr&{®°cÚ¬T²\x0008úåÑÃÓ/Oþ¼Ýñ
»ãcØÃ§\x0008¹ÅÔxÏ5CÅlx\x0003Ê[áûG\x0003àÃã\x0008|©±«DX/R°í¹!úYãÌ¶[ÿfô¼Z|x\x001cB¯,VoEì\x0000ÐiñÞÚÀtÇð¹2F\x0000?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ü}ÿÆ þ	HÏl\x000e5
!ãôè7\x0017·· £xµ:¿½¹üÃ°ºÕ}°Ñáì?%àé+R~ªàõôåÃ\x001aÖôÁÂ{\\x0004\x001eM¹ñº\x001dE\x0010|T[£Ú>T%áVyPÈv\x0015\x0014nwÈMóa]
ëú`Ià¹ÕZã¢2»z­»I}Mê;ÍªÊrMqME\x0010%z\x0015ûºaC
\x001bú`ánNj
\x000eÅ¾Tn#Y6Ö°±\x000fÖ+ÔÀI^«h\x0018[i<Ä°aë¬²­³Ê<ÓÒïDy\x0005r£\x0017r\x001c_Pu@
[\x0017Fó"¢\x0011B\x00110Æºø0=yÚÄ.Ù\x0019¼àÔ
4Ýi ³¬³Gr²²	^²3zYSü&"\x0014Ñ\x001f?]\x0019Ímì^é,K¦5\x000eä¡sòB­³ÇÚaMü\x0001ÌÄ RÉ\x001b\x0015KX8£Mü}\x0001LØPBSbFË"à%åäåOÛÄ0Ù\x0019Ä 7ÆmÄ2.Y*Ïm¼Ôði¸ ;\x0003\x0003*Eí\x000bx(ÌLÏ'eÓªÆÕªNW«\x000cÊ\x000c-HÎà&+\x0015èÆ\x001c¶ñ_ªÓij\x001eÚ%<^\x0015d©áÓ33ù´KP.AÙÒ0\x0011*ÓR Ó\x0003®ø°Í&S}LÀ\x0013.^\x0016¤Ý\x0014óSG:!¨f©¾M&`\x0006°/\x000eLcV&í²âÀsHÐÍ&Ó}L8K#i@â.`ê ¼9#Ýmt{ÁíÛcÂú\x0002nø¬¯%ÎÇé|Øfé¾-\x0006©YC:\x001aI\x0003ì¦º3L7Qòi=¦;÷\x000ezd»ÉÊ\x0019\x001dKhÓv$)áí¼h½~zy|ø|r¶W\x0013ÖDaH1\x0003r\x001c2\x001bU*íKc[$çÕÝÉë»«Ëë³Õnà\x0002¨j@Å\x0005Tb.+iÊM\x0002ÙI­:\x000e ®\x00015\x0013\x00104â"f3¤)2¤úO¼\x001c@[\x0003Z& O·W\x001aK\x0006¥8o\x000c\x0008Ã\x000eðM+Ù\x0011¯á<Ûzòç
¨ðÅxfRÌµüJ²\x001d\x0017à\x0007î
4$#\x0005+\x0010\x000fÐ²ä,Ó
\x0014ä1¾o\x0019ß3\x0019M m¦ôÁ©æIúò(dä¶°È\F=ö3zÂÏü¸~ùº0í
l{ñAPý¨,U¹vPSßIøãêîÝaDU#nyC!\x0005\x0018LEt,Â\x0014\x001c@\x0010Q«IõB\x0016¢®\x0011·|Í\x0001D(¸£\x001bÈ£â*\x0011'u|Y|¦æ3l\x0013ZAQÏGs3´,Ý5íp!ÐÖ[Îð°\x0005%
Wú-ÓÍr\x0013º\x001aÐ±7"5ém¤êei-Í!\x000bjK\x001c\x0010Zþ.ÄP#\x00066¢#\x0001À\x0001\x0011õ)¡½ .þÌ\x001bÁÝ\x00086#H£âøS'H
LÉ
ââ½,\x001bw#Ùþ&t)èn¨îo¬BßÃ×,DÉ]vÈuã 6\x001bÀ5æ²\x0013WVâr-(¹K11S\x001arØ\x001aâ;ÂfVÍ2TÜe8x#-ét¨Êüö½ÇymÐã®B»AXKâ¨VÚ(qð\x0013ï8\x001d"]\x0013O\x00147 $:KY \x0018MkiÀ!í±\x0016I¿®;ä²Ï®49n»¸DGN»ìfµï\x001a5S9e\x0007'h$ gT<$¢/\x0011zBxp.¨ã\x000eqsRto^ÿºwj\x0010tðK,jI[\x0007\x000f8Ð`@É)\x0005~(fH÷åt>\x000c§j8Ås\x0011ëð\x0006µ\x0019¬\x0013\x0013¥Í|Km
§k8Í\x000b
H¶\x0007õïEtE¶KOø\x001a\x000e­á,\x0013.ltzâæWj¸pà|
çypyê\x001fYÎÒ
Þn,7qÁcYns½Ë¶{Ïã\x000b\x001b+ÝøÊ+ÃÔ\x0005·nñÖ\x000b¾-Vv5ß¶\x000bï}Úõ£>Û\x0010*wò\x0008C[ß¿ÿ×?O¾_¿> \x0012äPÑ.ý;æz8I'\x0005\x001fÕäÆ½:Y]|¿:»Á©jNÕÇ©¨2\x0006tv³hn¤ûüwærêSwq\x0006³!\x0015ÌvÃ·\x0019'H%Îû0\x0011î¸¦æ4}²\x0014n¡\x0019$k\x0003<hâ<=mÍi»8ÓeÒ7PkÅÒ¤\x000cäÝ´ëæaº\x001aÓõbR»²¯º7Å¼ñ\x0008Ý×¾Ó\x0019ª5\x0015¶T\x0013X¯iy	1`6g¨9C\x001fgÙî¢L¢s0§\x001aÇ³	{8cÍ\x0019»8­8%\x0002\x000fÒ°¹K±t)k5\x0019¼YUé\x0013xyÑÇ)[*\x0012\ÖL­XþÝe\x001búâ)	`{¤¾OSÒÞ\x0013£	Ø }Þ\x0018lúd\x0000\x000eÎØÈ{!ûOÙøOÙç@u¹fÇäè±`\x001bl©lòÄãl\x001cìóL>ü0æz\x0008p8£Í};^DpÄ)\x000cö{oêõò-¯¤ºvLXº/Â\x00000¬Éª|xÛ\x000f
£\x000b-0\x0013ç³õË§û\x0003CO£$§*TÀb\x000b\x0013I¦6ìÔ^{r¶º{}±o\x0010mÁS5ââ\x0019\x0005¶qî	\x000fó @1µu8xºÆÓL<u\x0005/æèÑ`aMÂÜ1\x001c<Sã\x0019&õäw@ËEàÇ5>®Ê±ðlg¹x
2%<\x000bõ´!ë©·\x0004\x0016«ñ\x001c\x0013O[L§\x0005{ÃL¨Üé·\x001aøt¾¦ó\:êX ~ãÎ\x0012¼qèBM\x0017¸tÃ=v04(#ð\x0014NóbòPÆÁ5^äâe§,\x0007ËÌ&Èt~ê\x0019ÃVÉG\x0016ü/\x0019\x000bd$p[PBÅGé\x0017ÚN¶\x0011\x001b2T¤É¶ µDö£Bó´1&¯­\x001c¾&dHnÌH|èVd¤âÄWìçÆ\x000cÙÄ\x000cÉ
\x001a0LI¡c!­*à#·\x0017ÃÒïÛ\x0004
É\x001aPÓOé_¢ô!:ö\x000b\x0013Cux|MÔÜ°¡ËÀàäO6ß\x0017ÓPiLdñ5aCrã8\x001fQ¢./â³PK£lâä\x0006tÌËâ\x0002RzÓ²`ûùìd²Ã×D\x000eÉ
\x001dJQ\x0011²Tõ	Yp²\x0016K·o\x0013:$7v(EGR\x0010Êgú
_r/S%\x001c>Õ\x000fÅ
\x001f¶ÌÇQ~snÑ\x0006Ó`bñ©J5áCqÃG:\x000f\x0018îE\x0017÷\x0012°}ÙÇ±Ð8¯½qpÃ\x000bTg¥¼.§ÒòX*]\x0018ÞT\x0013>\x00147|~I>\x001e\x001cÏ[¬²J§Ê¥Ë¯\x001e\x001b=`>2n_ïQ((]t1_\è^T\x0013=\x00143z\x000c\x000f\x0011½³Æ\x0012+\x0013\x000cÍ\x000f\x0011SSay|MôPÜèQ
v%Ì\x000eè\x0003d¥÷qÕD\x000fÅ\x001eÀ«/Yò\x0005aêÑB¾Æ;+®wá\x0015¸{-Ë¼KâþÊ¼S6ÅÃ½²\x0014:ÌNk8zª\x00071<\x000fÐDg(­\x0011§
2jÊ\x001de-~\\x000cëë\x0012ÇõÉ§Ï\x000fÿú½y+\x0003ºß4c\x000bjM±RÒ\x0018Ê\x0004ªéWÓ«ÕÉ»W·\x0017ûòVD©kJÝA	²iØÖ¤<Mú.,¤Ü®dAÚ\x001aÒv@Bñ\x001cvµi\x0012(\x0017.U;r¿,HY\x0015h\x000f_ü=3Ý:1¥*ËlR±icR§\x001a6çºå\wqj_Jp°©1R9\x000bf
~ãª©6ÐÙÓËã×§ý9ô\x0012\x0003ÜNðG!\x001aõø\x0017'g7wWïnî\x000e£©\x001aM±Ð¤!ÁÐÉ&¡Å"ì?yt¦k4ÍAD9\x0016¹t}Â¾4\x0013\x0015¡M\x0017Ì&³5å\x0019Íg¯Ê,\E×t²,Îæj4ÇAÓ)tàIßC;=ìR¥H×O&æ£ù\x001aÍ³¬fKO÷\x0011zw¥2ÒÛeV\x000b5Z`Y
­c]³¡ñE\x00192ùëeÛ3Ö`e³\x0010¨ößJ\x0012ÌrzÝ_\x0004Vç$Mý=Ëd\x0002­"C\x001aUo©\x000e7N¾#ÌgkÝ-Ëß&$º{/¨ïÒiêmý"¶ÆßJÃÕ6 ²ô Oª¤K¢Â2¶ÆáJÇmS^¼\x000fäq]Q\x00154qºZf6iØ\x000cÍ\x001bò\x0019@\x0014\x0002\x0007QK:ØéÙhM4¬p M¤ã\x0007|Rl÷vÄ5Ò']¶\x0015p yñ ¦S;\x001e=`<\x0016MËM\x0010]\x0014Ee\x0013\x000f$+ ÀàVj\x0016¥©ß¦\x001c«ôä±m6[\x0013\x0010$+"\x0018YR\x0016!y\x0013¬kô¶Ì\x0012ÓfÙ7mbd\x0005\x0005\x0018!N³Ã¤\x0003EÅMÑXNØÇKØT\x0013\x0016\x0014+,\x0018%0`\x0005¥@&|@s¡ M¾cÌGk¢bE\x0005#"j¬\x000f§p\x0011nJWñ²/ªÚC8+(\x0018£¨È&èHõÜÉSø²\x0003¥jb\x0005\x0005£EQ\0¥}(=¦vÙåE5AA±±\x00115LRl¢\x000eÝ´'\x0008ÍM×üÌFkb\x0005\x0005cífh$)Æä)(øéÂèÙlMPP¬ `¼¦\x0012¤,\x0018³\x0003	z3ÐoY0µÍ'µ¼O
¹X\x001a;4`\x000fl¦ÔqéÖ\x0006bN)£Ûrúºà}}òîåáñþùa_AÃ
_¹MÐYl×¸@ÅJOuï
iwwW\x0017·{²\x000cDhjBÃ&\x0014Æ\x001f¦»\x0001ª\x001a§è¤tr,DW#ºo\x00121Ô\x0018#¥:M:£ä|ö Kù6\x0017/à«K¿\x001d\x001bÊf¯HþfÎÌh\x0013#¾9zM\x0017Dhìf{{Uv\=þõ/O¿$wsÿüyýq_æ0EFª\x000b|<¶B\x0014J:CnoéÕÕ\x001fo®ß&sq{½zuR6O>7=ß¦ãÂ§Ò\x0014"äD\x0008fSªRuØ²\5à>÷0$[RÐr{ã°)uC©¹ù--\x001fµ`è\x000eU\x0006:Ø0qÿfSÒðm)Øð`\x001f³-¥£u9õ`Ï¦´
¥í°e\x0000\x0011ÁJµ¨èá/Nt/°)]Cé:liOuy<5\x0012M©ËëßDm\x0001\x001b24¡c\x0007ºÓiA¯k6\x001d\x0007h{³}$ãRªÆ]ª\x000ew)\x000cÝ\x00054\ô°\x000e¢\x0006Ðü\x0011ÜåFþ\x0008\x001dæ\x0007öÊ\x000c`ÿðÑ¡ô\x000f_¤c)°Û\x000eÎ÷#Î÷ü\x001d\x0014qèOçð~ G?U·l\x0006]ó7ÃÉ\x0012zÈ¹î^º*\x001dáÃAMA})\x0004qð
\x000bQm)\x0004\x0013êpcÐé;ÄòÃ»<Ó>òô\x0014\x0002\x001aètì ¼~Z§\x0013÷ýN^+×ÊËO]'\x0002<À?½<¯?î=¿Åtè(5O\x001eu\x0017Lðô¨
oí
ãåë7«ô#<ÃßÜÝ®^í;Â!¨®Au\x0007(H+ÒÒ®éüÉ.±Ò9s\x000cP[Ú\x001ePg v'G"9Åtß-eZã!ê ¾\x0006õ= ¶,Oèï69®ÍéÃ©£X4Ö ±ëÓ§5uÑ£¬uúô4âWæÉôqÊv/õl&°(~z­Qe\x000c\x000c¹Gy\x000cÊf#É®d<te\x0002\x000cÏãq\x000c\Ð`G®)yfí0,ýuú/î÷ÉÁh\x001c&L\x0007©ÉìlÄî´´ïÝî1ô¯o®¯/öéÁvpÌ¨¸!D\x00112<\x0008%Z\x001bÝ°\x0015Ós-XºFÔ\DxNÆ³\x000b\x0006\x0015:\x000båeYÚIb\x0016¢­\x0011-Û)Hþ¢r8\x0017Ù\x000c\x001dæ\x0019ÑêI9m\x0016¢«\x0011\x001dÛéÌ§v\x000f\x00130ÑæÂ\x0018£\x000fZqG\x0018\x000fväËC=ee®	¤\x000b·.»éxQê\x0007Ì¤6=Ë¡F\x000clD\x0015(M\x0004u\x0004X<ê\x0003Í1ã²G¶	cÍ\x0017Ù|ÞP\x0015÷º8E]ä\x0017£]ìndãn$ßß¤C/ÊäÃ\x000f
\x001eÕ´¥w`\x000eî½6³lo\x0003\x000eÑÑ\x001bÁ\x0019	à\x0010éímÇ\x0004\x0011\x001bo#Ùî\x0006Zd©o¥þ¦"¨¤\x00036¾F²Môº<\x0012JCÝ$©dõôèùß¸q5ík Ü4©`ì\x000c&ÖÄ¦òvz\x0004\x001dËÍ^ìÍ\x001cMy/Ôô~\x00135Í+¶&\x001eáäPÝµ³ÃËh=UÓ\x0007©K/)U\x0011ã4j\x001fåûò=Ò\x0008\x0015Ëóf2ªÅ¬¦MvÜkÜóµukËäwØÆÆ6¹©!ÔØVª¦§÷11ß0Öü·`¶bùè]
yIja\x0012^~Ô\x0011âTåÅ9hEæ§\x0019[h´®´ÏóÊüÀ%Ô\x001e{\x000fÚ£~©1åòªÆ%lGé¶\x000céø40¼Ê]Ä6\x0018Â@;hü\x00101ó½­\x0006ÈYúª`ýíÓËãÓË§õ=xél-\x0010oP&ÂØRÈã¡¸~âõîíÍÝÕÍÝëËÕùNIçÂ§j>ÅåóÆ¹\x000b]~¼¤·\x0007¯üdñX\x0005¸ßzº¦ÓL:ã6×#@\x0005ÿ.L:Wp»¶sá35áòY\x001a¿ª¨<\x0016òdD7ùÀ=Ûr¶&³=ß5\x0014%4IuT7ãÍd§9ká¹\x001aÐ±?­£ªÅH"\x001bÉbe¤Ò÷å}Z_óy®\x0001ÇdÀx\x001aÓé\x0006MÚgSï]L\x0003\x001a0°
¨`ÜÔ`@cJÕV\x0011:w&,Û¹±¦\óå\x00142¯\x0014ÌR¯¥·Óå\x001f\x000cóÉÖ1s=³\x0011\x000ek\x0016\x0014LÊÃié³\x0016B±tÈÆùI¶÷¡\x000c£¶ÐzçÊlÅ\'c@Ö*\x0016'\x0013pø¸[¬á\x00106Xrw±Ì
ÐS\x001f¦\x000c\x0011ÜÌAÂfHîF1NbÕ»Ë@	qôÆêÕt](Ã\x0011ªf£(öFºKt41\x001d

\x0011«\x001e§n:\x0008¢Ø\x001bÅ;j¸i+c\x0013MÐÔpá¦Å¸XÍNQì\x0012\x000c\åó­ÞÒl`¨7Ê\x001d>\x0007\x001e$lvbï(©\x0019\x000fú=\x0013ëó¤¶\x0005°Ù)½S\x000cUÂ)\x0008\x0013\x0001|¤\x001bI
.BÊ!BÝØP³mèË\x0008ê¥ ¸tú\x001er6{#²ÒÕvÊ¦?þÛ1£ôcÐä¸¿EP±IàýdÍ<æ@y:\x001ds\x0004>®¤ëß\x000c©[nË¯÷Ï#[Â¯ü»ãàAÐ¸õÑ#ÿ£[!A8$ªS.Ò©ÛØC\x0006Ý!ß\x0010ÆÂB=(ìÍÓËó×õãÞz¨'"½t/ÅQ¯Ji\x0001m\x0012wÐ\x001bûnuµ¯àèLMgti)V1\x0010\x0007 K\x000cFÈ s5cÒiM}UN\x001c\x000f/Ôx\x0007Løjì¨Ê\x0018\x0017¤³ÓCæÓUS­\x0012]5Õj&£nhK\x000f¿´Ô~èìt
¯Ù\x0018»3ÒE\x0002ñX¤\x000eséëNiñ²ð!¹[#\x001d¹HØBÓ\x00138Lf&Í\x0015#'gß0ø½!¹Ã
bqt:Ä½\x0011Ãæp89×ì
ÉÝ\x001cÖÜJ£O|²SS±g½fÀQ¶`5áè\x001b1¢Ú¢T|JeKFSÂ§¦\¦Æ£Ø·0wÕ+'09\x0010ùîÍãúC\x0016O:úüååqÿLV)Q¨&¤ûJÀ\x0011LB\x001d
Oxsµ:ÏÚIç7×oï®ö	<¹ñ#7è\x0012ñðDqÒ!
\BXr2ð§_Ègj>ÃåK\x0003Í\x0017#¥ÒÓ©½ðH\x0007­ù,Û~\x0001º3 %ô6\x0004¸øûºÏ±ù<ÊÄD*\x001dâ	êÒ-Å\x000b5^`ïÒ¶\x0018EI©\x000b)Ë8úÑ\x0018ò\x000eÀúAÙåqÀì\x001dî\x0005¶\x00081±Ê6¦¨q\x0018M\x0018¹\x0018\x0013ªºÃpýåÃúã^¶a-MlHg\x0019E\x0007\x001cÖxö	>Ø
«·ç«ôÝsN	RÕª\x0003²\x0008E\x0007\x001d°30AR¥µÓ¯
äAKê\x001aRó!½9yCñ¡!¨5Åe=VKbÜ\x0011ML\x0018¹C3\x000cbâ\x0002Ba©Åê\x0006I·N\x0015J¥.úâYÑÖ\x000f	EUÙ zH\x0007\x001dâd\x0008Ã®Æs|¼ÜÕ=\x0006½¬\x0001°ªi°Wâ~B_\x0013z>aPÏ7XÐo,HíÜFø¥&\x000c5`à\x0003ZÓ¤®PÒð\x0015+ídÍ\x00170Ö±ÃÚm<ÌÌ*\x0007ÚÑc£Ñ~²\x000ch>aÕâkò%¶\x0011]-¸µ£\x0011iØr)b\x001bX:"KP$6ã\x0015I:mÖxú\x0017\x001f±	+²#®ØÒ¨æA~bÂ*.EÙ\x0004\x0015Ù\x0011U\ÊÒ\x0001Q\x0018x"\x001d\x0010\x0015I\x0019\x001a­Z±	+²#®ãèá|Ytàí\x001csè\x0008!¸";\x00023TÛ7ô\x0006 \x001d)'bäsÎ~;6¡EvÄ\x0016\x0018XLEÙ¦ZEàmº{ØÄ\x0016Ù\x0011\\©ÉvtE#JüÒ:.\x000c~²-²#¸@³\x000fÚ\x0010N¸]\x0004Ék\x001a7ã¤¸\x0017Q5®[u¸nc7~±hè¨HOÌfTGÀ'lOÛ\x001dn18ÊÝ¸tÈ!Ïm©{A\x001b;ÙéÃÚÐªq;ïv$Ô\x0011ãVôqu ç==ÇË7d³£\x0015G§Ë(ÌXÎ]]\x0001çê@\x000fáÚ«¥ºÙ/¿_¤Òø\x0012ÎÛ¥uA¡[x\ÔÍ~Ñüý"9µäsÌ\x0006Fëè\x000e¯ÆýÍÑü
#\x0003Ù|æh\x0004ùE#¦\x000b\x0019ÍnÑ\x001d»E\x0003£îù¦\x0010*yø¤shKëf¿èý\x0002\x0003d9ìädGºÿñ\x0010<¾\x001d
£{6L ~\x0015\x000f\x0012HiEc#L³aLÏñ%ÀÀÜ\x000cB$Eb»ô\x0006hýbzö-Q\x001a\x0004ð¤S\x00147[è\x0017M*é	.2NØ.\x0012\x0006_DcåÂ³i6é	.²4«\x0008AÚ±:(*µa!¢hXrê®j	}(uÖ¢É1µQµ32còNjµ\x000f\x0016
ÛÃÄÙ'0Î>{ºVü(i¢X}µ>¹Z¿|ú×ÿìíh·0\x000c\x000cÓÊnHÒçým¨W|ç	òä
¦j¼ºØÙ
âGÙÚD§ØtÉç "©µ\x001b:Ú9jóæÒéNóé\x001c¾jØHr©4&4híw8ïl¦f3l6[\x001a­Ö(NâRÐ£>$\x001fv¬½x¶Æ³l<'¡%\x001f¸í)\x001er\x000c¥´Ûr*t\x0007÷¯\x0001=\x001bÐ\x0014CÏ¥FSØÛÑI:Ûv±FüOë6ºlWÚ¢ M|	l6äï
b@0íeðø]´\x001dvjfò5+O²¥§Jûh²°\x0011®\x0016K×lÖd/¾\x0014ÏhUH»\x0003\x000fØ6ª2\x000eåÐÞ=HØ,AÉ^*\x0006kIâ°Ô!e¡Ùb\x0019¢j\x0002bG6q è¨`AnDç\x0019\x0007å¨°ã¤0°Ù)½SR(J¾¶LÕpôhoßqèOØì\x0015ÅÞ+P\x0004Õ_ÁQ}\x000bT9ný®ö|Âf«(öVÑà\x0001Ñ^£>ót\x0017M¾{éf®ò"@\x0018Ø[E"1\x0012Jù¦ÕE@,ó×ªÙÊ½Ó 9%!¸Ò-¥}©
:wÈUÚ\x0006YmAS\x0014IÔ°g-Ï³2.]ºq6íl@:\x001f»@Bt\x001bé|j±\x0010¡nNÒ}VÎ9VòÖG>e\x0017\x0013¶§i¶;4xWé\x001bã©Á{z>sbZ\x0000Ã×¨5ûH=HÒáFQ\x0002ê3rT./|Ú-Flüµfûkc5è}e+ZÆpADª\x0003îç\x0010ºÐ±½(C\x0012\x0016eüVQÅ0»Þ¥æ\x00136\x0011E³#Á\x000bg-m©Ï§\x0014ª-ö4M8Ñìp¢¥)ÇWê1Y[SN^KÏ5¦ñ×í¯uºpz:y9j+t¥# ¼\x000e]Û\x000f"6ÞÐ°½¡N\x001b%àÁ\x0006Î887,*°q\x0007b{g»M:{¹Ò¦.Ët?ï\x0017[±ÙÌ¿ã&¦øJéèPn\x0001!,õ¦Ù.½]ÅiÇA¯5Gfz\x0008·qZ8híbÙÛÅè\x001f\x000eÐ\x0007°rÊvc-æ\x000eÄf»Xöv1éNoÉq3«¥h:çgw 6ÛÅ²·É\x0012¼Ùs\x000fÐ²ç&ÂiM¨YÊ\x0012­ð»á{©-?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=z{òêü\x001d¨ÂË\x0017\x0007[ë34aSÓU1u-Ñè
îR&niêNE\x0012)þ¦ª,Z¡êú6Ñ:u@.­I\x00154$	«\x0010IKªiÆcvOñ¿hq\x001cÒZ<3þp}ôáó·wå`¤\x0008ÇÀÒMg+\x0008OìXnÒ´Ì4#~{zôáÕóô«\x0003%\x0000\x0019Ò5n\x00002°\x001cSÜ;ç\x0012\x0014\x0016\x0012¥YO¹{"%>O{)q\x00171iõ`qËd¢´J\x0016«3\x000e	ÏÛ?ÚéM%¾Q¤7Ý_ÝÞ\x001cTÀ EÉ\x0006×Ïæï¬q-hfÛ0ùìòäüì.ÏL»02qDx\x0011Sd\x0015P \x000cÇØñÿ1Lå]MåÝr*,:¢Ú\x0003Í];»\x001báÅ\KìB¨`k¨`CYËUÃFGê{R¦té:¶\x000e¨hj¨hCáyú~F\x001c|-Í®!OÌµ.£²9URv\x001c«(x9µ1+(cù±ç¥\x0018ÀbºÎJä\x00082\x000fÄMCÁÝ<ü|Øu	ê®\x0014F+²ýü¤³b\x001a	â¸i$Ø³³÷¯$Ô¶&Ô¶\x00104>\x0017Z)ih9\x0002¼ïÕz\x0014'\x001e`\x000c
c\x0018a$Í¡D(#Ë´/Óbë\x001eF©'_Zê&W\x0000>êÅí§ÃÖ\x0000K?©\x001eÐZ\x0007%êG\x001beÔtG\x0002?ÁI½8~ÐbeB\x001dkB\x001d{	¥ç\x001cµ!Gr°=\x0006Í\x0000áúí#¬'¬C)z	%»o±+QP\x001b¥®D\x001dåÌúö>BÛ|eÛÿ5-²Vsÿ\x0016B\x001dâLÕM\x001f^hðB/s¶]\x0003Ì#\x0013ü\x0003átÑÄrB!ã$\x0000'\x0008=Ðç?]ÿ{9AY¾=\ÖiMàYB*Ð¨\x001e0¶\ÏbÝô<yú:7qÆ~u~¨ä&\x0001Ú]\x001d\x0001ñÇ>BgK%\x0002ËBËlq>í£tC\x0007"9È;[\x000e2ºïnòÇÃâ\x000b´.²gll\x0019$ä¦1ÚºïÎ\x0010ðÅ\UÆ\â¥\¸D\x0006\x000bHÏ¹FÎS\x0019ö6c\x0017s+tpIAck¼èc vòq¤ä6{ÂÕCG¤­Då¤}9úp}ûÃÕí\x0013OÆ´Æq3p¬iuñ¥Jn\x001az)§ííÑÓóoOÎ'.\x0011~\x0014Z7·õ\x0019æñ¶~{ýåËÃ#P)ý÷6{+tñâúrq'^\x0002\x0000¾}ÿ\x0016\x000cðÑ£ûñéê«/_ï¯Ë\x001f\x0012µý>È¿ß\x0004ù}nÐÂ¶¬³ÿó¿þ÷É¯W77w\x000fé\x001eÈK´ïÓOW?ÿød@Óµ¯!
<"\x00197\x000bÞBJÐãªÒuýüåÉë7o¿9;:ùprvvñþÕÛ\x001dPó¡\x001b ¸\x000cº\x0007\x0008ãÍ¸\x001f\x0014¼Ð¹\x0018WYë³À¤´Á\x001d\x0000?yöûÿå~þû§ô2ÿ4þïÛ;üuúãÍçTM¸	7Ä¥´\x00080i)s°^9E£%8T¥BÞ^à'<:}qöjo%!^QS¯óÎ¿¨ÚêÎ\x001e¾ÞÝ\x001e$i*\x0016\x00052°Wyþ0pÉHÒÂJ¬Ú)ÎÞ¿»Ø:¨ÀT
¦zÀlL\x0012ÈBÎ$!e°K×\ºËÇôjEYQ\x0004fr/¹r\x0017\x0012\x001d\x000235é\x0012£Ï¨SÙ\x0014
+M´¤[õ\x0015]
åº |E\Aæ\x0005u\x0008&\x0003	»
,Ô`¡ëÜç\x0019G\x0008æÙã\x00050§\x0018L¸!°0=÷¡>÷¹\x000fçìê×»Ï÷\x0007ùði`\x0018\x001eÿèrÈ\x0006Ç9R«X<Ë[pÎN>\¼Ú7$¤Â45¦\x0019Ái@\x0008bú³Øb¬lá0Ê
0]éú1e\x0008X\x00180qBsV&*\x0008ÆtSý;©¿ÿXêo>öb½\x001bÊ\x001b°Î0©\x0011óêe!©²\x0013{¡vmØi&Ìww·_Ñ)Á\x001fß|þòå.\x000f^?p\x0004ÐmÏWÜ\x0004\x001cóAõTÞe(kà4\x001aæ»ówèào^½}{±\x0008{Å®jvµ\x001d^æ6Ûe\x001ben%\x0006xÅêÉ\x0004³1¼®áõ:x#°3	sÃ\x0000o\x0015ÁÙÜ\x0018ÞÔðf\x001d|®ÏJ\x0007\x001b\x0011éØ\x0018»5sfa\x0005º­Ñí*t9ïl:pù`Ìâ¬²¯hÛÂ»\x001aÞ­»Ol»VåÄHvÏh9§_VÀû\x001aÞ¯7:ÇÁrLñ w2çPÑ)ÜøÀ=¬¼­*Õùám\x0005GÛómåScDÉ¨n\x0003Ï$¤ãÅÊcc5é\x001a#óÌ\x0012<6ÞúÌËFËËj\x001eW3¼
4âÇiMO	­7Ö²Ñr¥¢ÄatæCÌY\x0004ïØ\x0011Ts\x000f¡\x0015ô¶+Õ\x0015ä\x001cº¢ãåë\x001aå\x000f»\x0002½¹¯råÅw/>£Í§Æ(vlÔ®q+ß TC\x0014ÿgL\x000f?ðóËH?;g]Ý
¤µ¼®¹r,qeñÔÿtõõúêáèÅÕç«û\x001f¤&Um)ÝÔUånFbë\x0003ÃOïNOÞ\x001f½8yuvvr¹o W«j\5«qÆ<;ÀTd¶\x000bíè°ç¡Ö\x000f«kX=\x0008£lP°¢\x0018\x0013\x001d ¹\x0003=BjjR3Fjd*¤HRÕÇ\x0014þ	ß¿Ám%VWÃºQØ¦ä'Z*\x0001ÜèuÁÝ6Ô´aV©ÔµheNÜ\x001f%T¡µó¯önÜÊ	IëÑ\x0007y½8Î>«q&'¡\x0001×\x0015áº
®Ø4*Eý.ÆèóÇûë§\x0003"a\x0017·Á\x0008fvQÍÎEõ³º\x000b\x001bìN]¾âù.§ÑK)&ã\x000b1áábóyÕJð\x000eß0{l[\x000f¥©)Í\x0008¥'ï\x0001ü~%©iñ\x0004 î6Í®`´5£\x001da\x0014"e~)`C\x001f\Å]¼fî*uRÊÆ3HG³ö\x000c:\x0004*Ë\x0003ÊJ¾IV½£O\x0013öxd\x000bhCÎú\x0012ý\x001bþ\x0011óÔ@ÖX?|þz0w\x0003>WÊÄ%>xe\x0007r¹\x0002G|rücÚaýþÕ»ýÉB¦j2ÕE\x0006¾·-®,iLÐú¦¸²r\x0015®Ét\x001fJÕéPbXFfÍ*4S£>4}Ì1ìòh4%ø»WÙÌöaø@\x0006:h!ã\x0002-y	2\x0006\x001frjHt6$w\x000f_Óe}y\x0005øõúËíõ\x0013yUL.Q \x0006ÇHW
\x00003NO¯êÅûwé²¾<?|8}{~úvOÆWMAÕ\x000eô!×¼]ÝßçL+¥¦UBüóÒZYÜc	~«#¨\x0012\x000e\x001aÈOäõÌ.h_ò³ÒFþ\x0016\x001e\x0016{Ó¬\x0015ª±Ôr,g-Î\x0004\x0004,¸\x0001*gÀúï<PÛcS\\x0011,]cé\x000eia\x001dÊÒ
6¯Ê5VÈ\ë%Í:ej,Ó'­h²´$åEPZ¹\x0004\x0011¤UÒ"#T¶¦²\x001dÂ
2wÅ°<­XÄ{¾¡Y%+WS¹\x001eY¹Ü¨\x000b²R>\x0000§\x0003oµ_sàc\x0015;°´Í\x0000­\x0011à&§×'\x0008+\x0006úð$]ñ
e«\x001e:ô\x0003èy<æ+è'\x0007q	¾¦ì`5Ò=â³¥3Äge>[8©¾bXó\x0015U£\x001fTðX°°ª åÉM\x0019åL©ò\x0019úÅÜ}É\x0003¹äcúÜÃzÂæõ5 µlXsôõNwÁÙÈp:
, Kd\x000cÑé ×Ñ}½¾oéð\x0017Ké\x000c&t=Ñ©\h`Lôy·<Ò
Ù#5µÞjú^Ý%í»	![¢â è,|S/Ë\x0005-MS;²§J*4U£©>4_°¡\RËfÉøâÒ\x000e¡\x001aÍt¡¥\x0006ñ|Q\x0005Nv¥*Ø\x0008\x0008÷X­-"³S¡ÙÚí9ýzuûã¡\x000bªø\x0019°ÞÇ¬@ÈMÖ ?ÔÜ\x00158}wrþbß)ßÿâ~úñóWâJÏ¥]åÉÃÍíÕçäÃjòa%"ýrÿê\x0016Èãàa¿-E\x0018¼±¹\x0005îQ)Ësù¾®­<yv~òjoAt\x0005ßÎüY°>þr÷õ£þ¾ª¡¼:z}wscôs42¢ÿn!Ðh§9t\x001c|nïÆÂ7nSA³£×\x0017g§\x0018wëå÷7á¿~5)\x00172 oîA,¯¯î?ï¥\x0008Æ¦H\x0011 wÅ\x001aÓLá<\x001e¤xs	Òx}rùê:&Óÿ}üß\x000fö
ÿwÉ¿Îñà¿\x001f=â\x0002ëâ=ý÷äâÿýèHU1ÿ\x0015ãë«\x001fî¯¿îý\x001a\x0011ÞY&Ë\x0001\x001e\x000cTÚç5ÍH³áDu6ð\x0012½>9ûöòôÝÞ3QpT£\x0016âÈ#K#øaïÎ\x000e'àèh\x0006qLc\x0016â(ke\x0000GòYõÊh:«ÂQ\x001cWã¸8:$ÿ2á8þXà©°t¬\x001aýX¡Æ	\x000bq¬Iuø	'\x0016é\x0002F\x001cëÇpø¿²Xz5k\x0016¥D.o\x0007\x0018\x000b\x000fWvó4gY.=Ìàlk¾[*W¥×\x000bãQñ4gY.:Ì
ÿs8w6ã\x0018ª.Æm\x0017»«.\x0007yÃ,\x0017f«®r\x001fy<.\x001dr+%òðK¼§9ÍrÑqV©q0Á\x001a!ohÙ\x0010Â¸8*âêï\x0004Ä¾þLð_né	¢\x0013td&D
Ù¯§Xj!\x0015\x001clA§Zª¼

»Áø«ajµH²\x000b±ûÅ7»i\x0003\x000fhJÿøýÓOW7\x0007
krÑ©P\BìTX]ÓÜ\x001bÿ\x001eMêéó'gss\x0010*0U©.0oãq>VsÊ1t#ð«\x0004æ¹©ÑLÌbõ2£\x0003\x001aÂ"3ëÐ\æ:¥{3\x0011
,K>õ ö\x0018Í¸Ud¡&\x000b}dN\x001eKCd\!\x0003\x001fTEF«¤VY>¼\x0004¢\x0013Î³»\x0002ÿ\x0002mô\x0000E\x0006Pj\x001fÇà§·lÞoîáßþüËÕÍ~?Ø¼\x0004\x001eï#.ÝÉB&âT¹¾¹|uþüÕ³}ïÇ
JÕPj9Î[IjÔCíÑ\x0014±"sa\x001cJ×Pz9\x0014¶©æ/µ 6!,æÏPªl¢\x001f25Y\x000eeB1B\x0013^\x001aö\x001b¼ÔãL¶f²Ë¢9ÎúÞàê.²BÂ\x0011*;G\Íä:d®3\x00069\x0005A=ï\x0000%Éá%á1\x0002åk(ßq¢dn
\x0004 t9QÁ\x0017 W@\x001a*t}½Hw/8* ð<\x0000\x001d%åä0T¥BQK.*C\x000ei9 ¨ØXËq-%\x001b-%;ÔTÐET±<Ðe\x0014,*eÆ¡\x001a ;4\x0002 ÚgÖR¬:¥±n\x001cª9S²ãP&´"UPü ®NP	b¤Ts¦TÇÂM_úOº3r´\x000b^bãÊSµ¦¯ãPEkdJ{êÍ®ØÌØ\x0015JA5§Ju*lúËv\x0006×Üy¦*²òÓðF\x000fU£ÔÕr­\x001ee¡Âî\x0011OºJ;Ö~¬Ã®\x001fö\x0008®^Ì_Ð\x0005K¯0£\x0019\x0013ñÆ¯p^§¡ªS\x000bt¸\x0002ÀcýI9\zÅwS6åzà"¸¢1ëx'MùQÑ\x00193R[\x001e!KÞ¬øÈ7["8\x001cåC~8\x0001!	ÎXü\x0015².6tá³Ã\x0005Ê\x001eèÂÓG\x0015¥kpmòQM×s®HxÈR~\x0003wÁðóbÏüý>\=\x001cýn±ðDnpE@§¾¡\x0003mÙa¿ðö&êÞüºéõÝçÛ½)!|)ê\t-¸\x000bôuå=\x0001ÂtÐëWç\x0007A\x0006\x0003bRå\x0019+2;÷KL#K=P¦2ÿ\x0005%ìäã	»/½ïÈû\ËXÒGpäa.\x0013¦\O¥d+0UíÉcï\x0001ó"÷±`ÀËP÷õ´âÑGì\x0000Ó5î\x0001óØ\x000eO!%åJàÆ	>]VÙ\x0015`¦\x0006Û^ß÷ºVia&á¬púZ³Ö\x0014\x0006ï\x0002³5íRi}"YÏÚè\x0005{ùaúí\x0002s5ëû}\x001f­\x001dG\x0007iL

»J¸|Íå{¸\,¾\x0005¶-Òø¨­å\x0017È4yÙ\x0005\x0016j°Ð%00:7ÔFs¨K(~\x001a©\ó%c
\x0016»$¶Ó\x0016F\x0004®\x000e±¼ÙJÕ\x0008lõkuF\x001fçOÓcË÷\x000ek\x0004fÛÔ\x000bÞËIkÃS\x001fTú44}PÃ
\x0018Ñ(´\x000b\x0007Ôÿ\x001e¢édÈ¿¶\x0003Ýúék
"ãd¹ç%¹!¶ßvî^\>yPfu\x001b\x0003a©\x001e¬¼!c	^bá;cÉ9ýº\x0010K×Xº\x0007+Æ\x001c6&YàJwÎ\x000e\x00079÷	\x0017bÙ\x001aË.ÆÂ$ñ®\x001e$O.òÚ\x0016\x001fúþèAò5ïA\x0002;ÄU\x000fpØe6ÚG÷sJb!V¬±b\x000f;,§&\x0003VädðÓ X\x0007loáòk¨pILá
)ÅRÆ±\x0004¡õ¸´dsÜåòóApcCò\x001b(Òð)oµ³ü\x0006+¸ó.{\x000e<<¯KÅ\x00118ÕäàÛÝÛqú4ëÒ\x000eÍ;i]\x001díÂÛH/"&\x000eÑ}´åBÊq8ÙZ!9Ó`÷¾7ì\x001fª¼±0ëûâ¸â"~:\x0019¦\x000fÛP5Õ¿¾»}øùúvmBH=t9©íøVJ.uáá~\x000fÏµó÷¯OÏ÷U(ïÓ¿hû\x0003báj\x0017üßW?c'ïóûë_¯ß]?ä¯LnlJ\x0003-ÿåËÃý¿|¸þrsxØ<ç\x0005-Ð*Ïå°Þ\x000b^}¦õn^\x001amyôöýåÑÓ·g§ß¼<y½Ï/O?\x001e=¿8}¿¯/Ñ|÷Ëß~ûùïÙp~ÿ\x0011\x000bY?VisóäÇ«¿]/¤¶^ñR<1\x0016yX/CäyÓ¦Ls~D½\x001bÈ
ÏNþ}ßÇ7[üü]'ÙùÕ×Ïw·9Ð²ZEj×Ê;®Ò\x0003\x0006øyÿ»n7FdJ\x001bËÎOÞ½º8ß\x001f'ªU¬FA¹\x0004\x0004­e^\x0013n]¤5æ\x001a[÷6#Ö5±\x001e&\x0016eH5\x001e!\x000bYÒ¶&\x001díÞÑMljbóÏ c[\x0013Ûab©óº.ÀôÙ¢y\x001f,x×o½Ø×Ä~X\
#dko±_,\x0014a7C\x000e5r\x0018EæA[,\x000cé8GOQ8\x0016Îm'äX\x0013Ça!ëHªP«å\x0016üÉ-\x0000Úø­ÉÖ²J\x0016ÃR¶ix\x001a\x001a\x001f©¢ÚbA\x001c\x000f/5Ã\x001b0·fdØ¤îw³5ù\x0005	'Còõ\x001d\x000cÙX\x00119lF\x000cÎ%Íg\x0019u\x0006)[>\x0019Áì\x0006T®fn´²\x001cVË8HÓ\x0012²Ì{l\x0001¹¬;ÐÛ]?Ùhe9®A\x0019ç1åÖ\x00199ÏlHÂn\x0001ÂfJJ¬Ù2[ÜËA;%¬În\x001cd`ðè6\x0003n\x000c\x001c¶$\x0018\x0017¤\x000e\x0017g\x0019;Å'9ªÍü\x000bÙ\x0018\x00129lI¬´ÔÁbR!ËØÓâ\x0013\x001fõv
®±#rØ\x0018\x0019Râ\x0019e¬|Nî¢«áøòí.j\x000c\x001a6$6/NBÆ¦¡å¬"ie¿kj^ÏÜ\x0018\x00125lHþ¡rn\x001f$Ã¦ÄjKë:AÎM	<®=ËÙlfJTó$QÃo\x0012l®#%çp¢\x001a9\x0019Â²/çõf.¾jÌ\x001a6¸%)ð6\x001dqLbvÅ\x001cÃvbnì\x001a¶Æä²îä1SöÆ2}tãvÌýSãöÏÛ²9KcArRóqÞÎ\x0004ªÆ\x0004ªq\x0013\x0008GØN\x001cÓÂÇ63\x0007§¶;ÎIQã&Å¥@öó³ªó8Ë®øùj+fÝ\x0014=lR(ï)\x0013}\x000ehâ¢qÚ#D7ó5tcRô¸I	\x00196Pm>ÈÙiÇ~ÜNÎIÑÃ&\x0005+\x0014\x0013b\x001e\x000c\x0004r¶Þ²Åf¦[·Q®aÂeõÌu@À\Þ'>lçëëÆ¤èa\x0013L\x0014ÉÙS3	0HúÙíÞÚº±)zØ¦Ø\x0018SaS3\x0007ç<ügølí^Ûº±)zØ¦8«Ó¦#³£¹þÀëïHÎû£ãÝÌMÑÃ6ÅáöCÃí¦gÒü\x0014ô>l'çæ]¥ßUÎK¶Ý8¾Ae½¡©cëPæ¤¸±zØ
¢÷©\x000cIY\x001fÓa6\x001c9ò~»· i \x00197ÁrPÃàøþ|0´Qü~a;æÆ\x0008a#èL¹eRt\x000e(oAc7KôÆ\x0008q#\x0008[å¸\x0006\x000eÍÙyÖÔV\x0000ÿ4z3¥a\x001a#h \x0003çÙ]®ÂûÇQÅT)²\x0015rë\x0019·.;t"ÍZxÒpNËÍ<}ÓX?3lý\\x000cìÍávéHÏF~ìvÒ®gn¬\x0019¶~^ùÔîB3í²ÓsÃÎm\x0017 0õ3ÃÖÏ\x000b5\x001b\x0015ùáª½b½hµ\x001e¹1~fØøy¡øq¢­¡<«×Î8>Î\x001b\x001eÆüaó\x0003þø8KjÅ£!9l÷8±ý³Ãö\x000f| <
uÌ#¸Y-qÊoÇÜØ?;lÿ<.Ê\x0011æ$èAeÐ¾ff¿kd\x001bûgí÷©N'â\x0014ò\x0006\x0004÷Ý0\x000ec\x001b[bmÏ\x0003\x00133ÈWÐ\x0004GÚÙZ³Ú°v¶ÃÚ9}OÌ¶0[ÁqE»á\x001bPí*Êv¡òTRö§Ãÿ 5äVôk´TýP`ðËo@Þ¬oÈ¿¨êµ?\=üöõóíRÇC¬ébÉ±S¾\x0004dü"\×÷áäý¿½{µoIh«j\5k\x001d×jXÝAÆúÓëu3`]\x0003ëQàH\x00131ºoË\x000bÅ²3\x001aÚoU:M
l\x0006ÑÝ 0¦\x0006\x0003ô6ÊÝ;PqÔkk\;ë):ghprèøÂ	·ß\x0007íäu5¯\x001båÅÐ\x001c§á¹¤Ä\x001bÅ¡æpèÝ	ìk`?
\x000c®%	c	\x000f½¦"Ç^Â\x0010W'o¨yÃ(o\x0010¥ÎÁÙÜ\x0002\x0002ö¥ÊO\x001dÈ§u\x0002Ç\x001a8\x0002ëÈq\x0017³I³¯l$çÒdÜJÀ²µ\x0018£&Ã»\x0012ÀH\x0012Î'Â\x0010÷GÄ;\x001b\x001d,G°÷ñBØ\x0008ÄGËSAåFÀRÃZ-´±#\x0011³Y6±hµ2yb=p£$ä°Àý,âo\x0012"f3gäþH'qsëäèµ\x000b 
8<Ê\x0006díØ§\x000fæOßG¬{§Fï]ð®hb\x001c.M\x0013;â¸Õ©PÍ½SÃÎ\x000fNçæ¼jZ¾ÜK'9¤\fk®'n.\x001a½xÑ¤Tj~zD>\x0015Ø1ËO\x000f³T\x001bÏ4[V¸ÍµS£×.ºÀñogÔqÈ\x0002öc\x0016!º¥ÞÄaÜæÎ©Ñ;÷\x000f<\x000fº¹szðÎ)å-T\x0001¶ô§YX\x0002| (Ô!`Ý>6þ	.n.\x001e½pÿHâæÎéÑ;÷\x000f#º
m&÷Ç?;3z@M@%{AU{a¿_¡\iÙ	ý
vÝÂR#½ïú©i,EÕ½ïWGßÝ_ßÞåüe-\x0003¦(\x000c\x0015§b¤Ãìn\x001dñåéùÅþ\x0002\x0015¸ªÁÕ\x001apx8C¥2M=%\9©z6uqë[¯áÆ´5É[R9Ov8T62Àmjn³Û´8T1»$Ï·OÝÈ.n[sÛ\x0015ÜØÃM~³2\x000fÜ¶\x000e\$ÎT:»é\x0001w5¸[\x0003n,7ó\x0018ÞM\x0004à%ïû\x0002¶\x0004÷5¸_\x0003\x000eçZRò]*î6Á2PJòÄ\x0003Ý^\x0003à¡\x0006\x000f+À%ÅÁì×|7·\x0007Ê\x0007Àc
\x001e×\x0003-;à6^û])}wê@ùN?xÕbÖG¬!·©\x00137g×\x001cUþ9'X­Øx Âr@ämâ'ÙÎzÀ6\x0017;ó©ó$^Pç¥
0\x0003\x0005ü=üÂLì>höÆîã\x0016\x001føÐF£Eïs\x001c(Aq1#©\x001f^ê%rî\x0016 ã®óó´÷èIzUÓ«ô!rM¿uë¶ÓI§¨Þù1|]ãëø\x0006Ãd¹º?pL\x0012|F¶Jtd\x0017½©éÍJz_èÁ4Qý¹\x0013¥Bn~tlMoWÒkSrÒp\x0012Æ\x001a_:Ìqõâ»\x001aß­ÄÇª\x001a¾·º©=}¾¸ak|_ãûøð¶£^\x0013#\x0017{[íCöä\x001b©\x0017?Öøq%>6¶p­ºá¹(öï`	ç¬!üº£ÝLÌíÈá\x0017XÌý\x0001Ä¿+õ
[ß]Ù¨}¹Vï+QêîáSÐ\x0017«B©\x00072ãÛËßhN¹RubªD[\x001fTIîD®è³K\µ.üF÷ÈÊ\x0007§ÒñÁå©Ê¡\x0002]üã6üWí.\x0017óý	ír¡F96óñúþfqt\x0014ðÓ.Ã(qØå±H/\x0000'Û-+ìþ· Í4Ê\x0011g§guli¬jdõO¬kdýOlkdûOìkdÿO\x001ckäøgF\x0016í¸êüv$Û×£\x000f_¾\Ýÿ°PÝaË\x0011G½p+!uáâ
çÖÃùµ4´íÝÑË÷oß\~{HYÛFsz õ\x0018º\x000e\îîK\x0014!q*è@Qâ\x0008¹«ÉÝ*rã¨èÝãîk\x0002·y6â°wÛËíkn¿[inctð$%nÅ!ÌMÉCM\x001eV[É±Æ\x0000gBüG"/ÃÐ7B5z\'txî/Î"÷|Æõ\x0013E\x0011Üµ+nw®ø Ìó\x001b.UgG\x0016øSu¡½à^ë\x0014\x000bf\x00022:V·Ò<\x0013z<\x001b\x0011\x000fLl\x001a!×
¹^§\x0012ÕN%º"uÍ­)¸ò{SvÓ°5ìØ¡)\x001dÝr%±2OLx"\x001d0aß_$pÛÛuBwñÆA\x0016F°ZÜúÀ4
]®ÓèF°F÷øXcvË]m{^\x001a.W©ttW4©t\x001fÊì\x0002M-Mf·ão\x001bvÕ¨FµN5Æ¼'\x0007Ø#\x001cûÏðFiaÃÅ¦'F5þ¢Zç0\x001aÃ'&¨Òd(-åwpOäw{Ù[qbw \x001eéÈD«ù´+*ýÇ·ÿ¶èfWë4»\x0015GÂ\x001dF¶80µã¶Þ®j4»Z§Ù£æ\x001dÑÊÒäi\x0003ßT¿1{£ÜÕ:åîËä\x000e\ÕÇC·"{\x0003Ré.«ô${óÊP«\x0019\x001e×\x001cz»8¦N\x0017ïÊq"\x0005ÓÞØ%µÎ.EÉ	ßHÍªJú¢\x001eý¶ê±±JjÝC\x0003ûãhHb\x000c8ô:;ì©¦Ïy½yh¨U/
'4·ÂD­Ëô\x0014Má\x000bü\x00176}lèÆ¢êu\x0016õ\x001f,wÝT½Ê¤by\x0017]S\x00130uDoQ\x0007æO 7\x0016U¯{*ý£ÅÞ%½Ê,aç\x0017é\x0018t }öd¾8\x001b\x0006b,ü£fO?¯zu´\x000e\x000f%Szù©Ç\x000eu ¸\x000fÞMC\x000eC´ÃàõÝÃ
®2ÀMI·GÏ®¾,>ó¢äxAø\1x]sïØ{phÁë÷g¸ÎàèôüèÙÉ¾%Õ_AÕ\x0005µú¯à=æJtÅmbÚKùýä"î¿®ÿ\x0002zý7+µ\x001a\x0007¹óm\x0019M½?S7ú70õßÀ¬þ\x001b`®¢×\x001e{4åªuy¾ÍO­ÿ
výGÀ®\x0016ºÇb7²Ìñ8aã¿B¬ÿ
qý_!
lM/ÜókEÙã°¿^cð¯ [u´^\x001fá°\x0011jÜñÆ>öèy´|Ø_\x001aÙÿwS\x001a+»Pß^}¼¹»]
¯qÖ\x001díÑì©æZð\x0008¨÷O
(Kaà'ÏÎ.Î\x0017«\x001a\­\x0001÷¥7\x0018'ZEÛ.y\x0007AÔâ)©w\x001aÜ¬\x0002·Åú\x0006M3òá§r\\x000e4Û\x001aÜ®\x0001\x000f#O^ðÀ%\x0017U(\x0011âý\x0011pW»Uà\x001f'^\x0018
÷¹ÈõÑîlpûÛ¯áËy<¨úÀ«	
¸ß?_`\x0004<Ôàa\x0015¸ä"B¡ù@à¬Õ\x000fíl\x001a\x0000¯3O1eÉÍnz0üÄÛ¦¢³¦èò-Á[5¾Fã\x00056BÖ\x001fK³ã\x000c»3øìÜ\7äz
¹,S4|EäÞQÈ\x0006\x001e\x001bOÛÃÚ·¯{Ñ+Jcî9w<\x000c\x0006Ì\x000fW?\x001cÙ¼h×lÅ¬jæ=«¼$CYja5\x000f_±t´==±d9´®¡÷¬ù^$ãªÌ°_ÞðØxªW~9´©¡÷¬\x0000_&éX6[ØPª\x00068ø\x000b¶ôÉRÀÅÌ¶fÞ³\x001d|Y¢`×ôà5ïîÚ\x001dõ\x0013±Ó\x001ef_3ïYÐ½,á\x001evÃ*RB21\x0007®ä	Ú<Yòº\x0000ZNU¬j§ÿôÇÿûõúêa©Â§2¡Ç¿Ø\x0011'Ë\x001b¿<ywzòþi`U\x0003«q`A\x0007ÙÓø\x0012Qày¢§V×´z6Òü;8hiç!<þ
ï%65±\x0019&Ë\x0016e\x0019|\x0015èDØ]ÏÂf"¶5°\x001d\x0017±,\x00118Uz\ãÉ\x001a>\x001eÊÛIìjb7L\x000cj"ò(4[É\x0018[\x001aºÌÅ-&ö5±\x001f?\x0014ká-N¥UjVZ~ýTFe1q¨Ã¸ËF\x0008ìÛrtµ/\x0017ïÉÜÛÓÄRO\x0014\x001bøu\x0018!Yû_~úüãíßÚ\x0010\x0013¸m%FQ¼"\x001b)¢¤|ú\x0005fäâòÍËW/Îÿýi|Sãønçúñbæx8Ï±h­ïrzWÓ»µÂ\x000fWÃÅ Psç-M0Jì<=\x001fjü°\x0016ßÙR \x0000g\x0015Áÿåì<ýÔ]/ôÔ	Ñè¼úù«/_\x0006½§hÊà,kK\x001c¿Ì«Sû#:¯^¿9yûv±\x00035½¶"]Û5ìræe.Fò\x0003LiáÙÜû\x0000\x001b×5¼^\x000b¯8îm/ð*ØþÄí\x0010¼©áÍJxxùÒO]º´\x0015EÏÇ½G~ÝÖìv­à\x0003\x0017C¥ÆnSTØ_§0ÄîkvÿÏ"w?Õ4~oÞöåÕÃ×eüJXI¹\x0006'\x0005ïöÁÒËÇhiö:º3'ïß=ýÐõ_b_â³ç/\x0001×U§Ù:NÄÀCu\x0003ïD3ZìÏ÷þ%>
J\x0017"ÿ%aZÄ¿Åý\x001fÿýëõÑó»ëû¥	Oçhñ\x000eöp¶ÐÑé±ÊºýnÂåéÓ£ç\x0017§ï/©6úÓÕ\x000fW_¾ÞgPýýÃÝoþö3\x001d\x001a<*gÀvýë5JUS±Np\x001fï>ß"v\x001a»Uá8\x0004ï¼9÷\x0007oc©'¼¤ÑÙ£Ï.^s\x0006\x0008\x0008²O^
\x0006¨~µ\x0010Ã\x0014òE\x000c²»G	£4-÷cÀ§Òÿ·0þÓúßn9w:ÿ»ëûAí\\x001f]^ÿpw»Å\x001aö\x000f \x0013.wv\x0013\x00153\x000büQÖ,ß^¾\x0006ÅrztyúíÅ¾±b-P5\x0002Pøå\pRCÆRæ8m>6©Ô SÙ2¿¯ê¿þú7x`Wg4Äó®þv÷õ\x000bêO?]ï§Â\x000c)Æ÷ðSíÆVAÑYZ\x0011×ÕÔ\¤\x0005à­óï\x0017ïÞ¢\x0006ßìÅû1>ü×Ç_ÈïFoûìúËÑÙÝí×W÷?|Ù\x0005/Ú\ö\x000bX \x00192\x0017ð\x0018ÀA\x0014\x0015mû\x0011ñÊ]¿8=¹üv_\x0018]ÿ×póéú§JZüñ¾\x001c=û|ý÷ý< p¬Ó¡ò\x0011xòî\x0013P¡9gÂú¹Ï÷öèÙ«ÓÿX\x0002\x0004ÚÂv\x0001¹cð·\x0012
ä\x0001
\x0004$KÞ¾\x0007èúoÿóêîÿ©$¯é·Wo¿þËéÃ×·Q>ºñ(áçK¯	\x001d\x0008|bM¯æ·'¯Îß\x001d¾qz¾ÿ\x0010UL DÂé¯÷ÅU}Î>_?\x001c}ûùk*i»ºùõêþ¾ÄhS\x001a«\x000cÊ@´\x000e\x001d¿ÓXÚ\x0000#¿Íñ~uúþèÛWïRíÚÉÙËý³B#;Ò&£J\x000fòÖ5\x001fsðç#q9\x00137à"ÃÒÅ\x0005¾KjñBá)f4ðX2ZmM¯ÈÐ\x0019É"\x001a¡@j\x0018ÄHR\x0013b\x000b´¬!:ÑÁvìü5#ÞLh8»>¨\x001b>háÓÏ\x000f?¨\x0019mzôìîÓOW?\x001e¸NÊ¼\x0014&ø\x0008\x001eb\x000e\x0008\x0017Ãdõ\x0015±\x0000iÎ\x001c>»\x0000ÓóbÿÅüu×¾¹ KOnnî>ÿvÀ6ã\x000cî¬%\x0014|@§m!\x001f­¨7Scsrvvñêßöbû_\x001e®eu	lÞ}¾ùõîÀ'\x0017u \x000b±sò,\x0003
µÇ©\x001fa^2ï^}¸Øÿµ>ýøÑ}úÚøu$\x0003v\x0018\x001c(ó½dð©¿
Ü\x0003|N4o=u·Áëÿå¯ÿUè\x0005Ö\x000e}líãz))À§"wÀ)?ÅHvn\x001fÄ­¿~ørÕúüOZ\x0011e>&ph\x0002\x000e­ÎUxh§.?Ö}\x0018¿þö\x001b¼bjÅ³Ä´ië\x0001\iË¥çèH
zyTICÆÈ>ä>\x0008÷õ·[ù[ûðØúîÎç>ß~ùíï¿ÜWç3ß\x001f\x0016R¸¾\x001a\x001et)¸\x0000(>z¾ÀzÆ;ûvwVó»0ý_¾Àíü\x000bvÞÜÃåúüK^Ç´ï°à\x001c;
®×Ì\x000eìy³æ§®ÇËWçÏ_½Ù¿t©âR5êáÂ¶ô|Êt@¡'eçf\¢\x001e.]sé\x000e.l\x0008éDy\x000cftô\x0011Í:0S\x001e0¸ëÆç\x000f	w/ïI\x00050¥H\x0007®û¶æ²=\x001fR¤ìe\x0012åÙ\x000eBEÌæ&*!.Ws¹®\x000f¹â%ÉÂ¤Þê$/¿ê;+ôp)q\x001c\x000b\x0004Ì}ö\x0019K¬á¢:>V\x0014¢\x000b,¦4	yL\®Yo×5Bö¨
PüÈT!PE\x0018ÜåÉv[È+)»î¤M£*\x0010\x000c7O\x0010X´¤\Ó\x001a«\x0015`ÍÙ]\x001fLËZ\x001f_Räpãì´|'mY¢4\x0004Ö\x001c~ÙwúÓ\x0016¬^#mèS¦\x0015«× V©æø«ã\x001fBr,\x0013açN´N&É5Lµ²ËRzö´¼ÔºlNt\x0013\x0008f
YsüUÏñÇy\x001b6_L\x0001¶TD¦¬Y¥ûwÓãÃÓ\x0017*\x000eö¦û)øElØ\x0000(±Nÿ±u2>v|S§S"¾iA%´W¿i\£9íªe»ê¹\x0008|j¸\x0008%*¤£c\x000fH®R\x001eÀö©eûÔÁ¦#EÕ±xú'\x0004VÃ3\x001cól=Ù-ÿbZ\x0018puôæ
þ#7O}ØDgÀ´§ü\x0003~U\x000e\x0017[×ÒÕ\x0019Å£7'çï1kô4¥ª)Õ\x0008%\\u\x001dÜ\x0012Zb(rËX\x0002q\x000bN]sê\x0011N\íÈç
X\x00198âÇØD­I_\x001eÑ\x000bG2¹p\x001fù±'±Xí
ÜÒTpã	õ\x0019üâ\x001bü1Å.Þ\ß~\x0000ìë»û«ÛO×7{I
x\x0002\x00116HêE \x0003Ãýé¤¦ÐÜ$ñæôü\x001dü\x0003h__\??=;$Y?½O~×(ÐÂÞ~ýxõ÷Ï\x0007b
>
O9+
	\x0016PK¹Î¼a¿\x0000¿{vò\x001f{×õTÄª&VÃÄ6/í\x0008TO&CZ0]|äæ\x000c#ë\x001aY\x000f#kÅBÖ\x001c3\x0019U,dóÈý\x001f&65±\x0019&v¨SØ\x0000#IÈ¢ÊÆ»Gj\x0018ÙÖÈv\È³Âh[óÎB¬tó>0Û\x000bW#»q)+r¢wt$!»@ÄÁ<ò>}Mì×\x0008ÙR\x0006×ÓÓ¹(¡I£Ü#Ço\x00189ÔÈa\x0018Ùç\x0016b@\x0006\x0017æXC j\x0001ë\x001e¹ÃÄ±&ã\x001aNq"LÉ@õë2XÍJÙ?z.\x0012W1
´"b\x0018\x0019gç\x000cB{2
rº
öQèe¹µ|ã¦O9.iQp¬\x001d\x0019\x0012é9ß\x0018\x001f?±\x001bÛ'Ç\x001fY>-5Fº¥±|õvÀåã¦\x000f¬µ¡³¬+C"U\x0011òfD6¶O\x001b¿ (â4\x0011©2s4¬1üvzY6ÆO[?gÓ\x0000@säA	2xR\x0019ÖèíÄÜ\x00129nK.Ö/õå\x0011XeàR­\x001bÅ,Ç5³\x000b¬5N·d)[fvj;câÛ§\x0013ZíÝÂ«nrãR\x001f\x0003\x001aîhYw\x0004>Òs\x0011èq?¿$OÿjØÛ\Û\x0000o1tH³·¡Cq7³*Â¶Ôv\x0005µh|$r82ÅGZ¬>fFýâk5æ	ø\x000c~A)î·W\x000f7éúùÓ¡ìn@WÈä0ÇPI/+m=åÛ«¥Þ}{òþ,=P_=?PPàT
§:á¸Ø\x0014ßÐ\x0014Â\x0003\x001b--ÃI·\x000eN×pº\x000fÎXÒ\x0001Þ#M\x0011TA\x0005J`-©áL§äJ\x000eÀ\x0007Aa\x0012¥\x001dÇ\x001e0Cl ±öÈá/ªñ\x0004X¡~ôÝÝý\x001fÿß!:	÷$\x0007Ê:\x0008[©(Â\x0008ÚhFã§\x001aô£ï..\x000fÔ\x0012\x0017<Uã©^<ãË<2ZI­(ªý8}ÒI§k:ÝK\x0007ºr\x0015\x001e\x0007óäK!-'©áA³ÏÔ|¦ÏsÅ#ü"wZIÇÂó3J¯ÎÖt¶ÎóÑsÕ,ácÐ(3®s\x0017«ñ\/\x001eØd\x0019Zªµ\x0001<Àb2\x0017néÂó5ïÄßp!\x0002ê¼ìÅÃ/½*:oíÍ
5_èåiuj¾\x001bfpà¿ÇÖ,Øµ7Ö|±ûó
^\x0007\x001c§éûJ.v\x0017vå÷­\x001eò¨Å\x0000 ÌÉ\x001fåÁ\x0001ù\x0000ÎÅT»ä×&\x0002ñ¨Ö·.µ\x001f.ÍdM·ØQ>¶?³\x0001qS{K1eÝ¾ÑL®;*(û=?ðRIÉ8g¨ÓB\x001aAq\x0008¢m\x00027»\x0006Ûò«'ùBÍ\x0017:ùplJ~\x0004x\x0007¶BçÚpµwÖ¬\x0004¬Î!
Pü		UC¨þLbÚ\x0011¾\x001eäòùçë¯ÿøïûÃù¤_rÙpQb1tZÎ;ß\x001f=õúôÝ«ÓËC\x0019=1Íâ\x0008_\x000fmY\x0000ç\x0005vöå¢\x0001L¦\x0008®Pñµt\x0017®Ùt§àOó!Pp£kÂJ®8Ò\x0013¿¾ÎÖt¶.P.ÁåeÕ M]ªfü.8_ÃùÎÏv%Q9,"àõËåõ6<X/£Ónr#´kÕòÓýoQ3\x001cÎçÊ4º´¿Áqó÷õÎ·Â¦j6ÕÅ\x0006¶ë\x0002-FeBf3ì÷yáGáÔTpÊUïµ§L-·T§ë{$WÑXÃOp£f=¾§¬¬L¹ê¶*¤\x0015He\x0003MnÄ&\x0001ÇÍ
aÎÏ{jjû®3ê§¿|N{V\x000f\x0014¨GaÌ.*`hºÖ+ÉÂ\x0000ìéWiêþÆ§j<Õ§\x0004\x0017EyE\x0005¨Z+ËÓnãú(®ét\x0017]p/ùá-\x001c=¼áÙÍ²\x0013«¢Ò5\x0003ó/Ò§½{øz-þí\x000fü~@·áÐG*t\x000b×½IgJªjºË÷ïN³¹?ÿö Þ¯'\x000e/';HX¼Ñ\x0002sD¥]C¥k*ÝE¥MV`ÊcQ\x000e4s\x0015jTäI'©ÉL\x0017YihI_ò}Q°%/)×¹ÌuÁùö\x001c:AQèD°ùjÒ\x0017Ñ	\x0016j°Ð\x0001\x0006ïÓ4=?¿h"¹\x001dÚzV¬ «\x001e\x000b4\x0019w9ÂH'µý\x0006jAÀÚkÒh~2 ¬¹²ç^F\x0005OÓ É¨Gê&ÑÎqé.Na]u\x0003tº\x0005é%½ü"\x0012$Æ[¦ñ­_Î[\x001cüªS;**;#ë´ðÞå|\x00154=ñ¥Twa.øìäíV^LÍ¨¨ÌèB:åpJ\x000e@<â\x0001èTIL¸¹ò\x001e:]Óé^ºPÒ&ÊPu1Ði¶ò¾Á~:SÓN:g¹+ÍKK\x0013\x0003q¸d®ÏÆÀ:èlMg;éKcïQ6\x0016¹FÏ`©
û +e×\x0006ÀÒÍ¨\x0002`Ë EæÆQìüuÔ%Ä>ç/aÔÓ«'Ñ¯«£\x0017÷½\x0003Oî\x0010`à>y\x001cÃK&\x00065\x0012ÚÎ°jÄÜÉÑËW\x001f.À{\x001aSÕj\x00003:bä¢;\x000b	q_n\x0019¢6ÊÔTúææêÓã±Z{«á\x0008R÷\x0007Ff\x001duW¨ònÎâ³çKfgUxªÆS½xá¦\x0018\x0018FÞ\x0015µ@¹\x0012dòmªl\x0000P×z\x0004\x001e\x0014
gÞ¨IÃ\x000emn\x0000ÐÔ¦\x001f0rõ=V~êÈ}wüC\ûm
h»\x0001A\x001fªQZ\x0014	ò¼'ª\x000cKÐO\x001bB¼­Û\x001f®\x001e\x000eLrH58J(u¾¾-<æ_Ú\x001fNÞ\x001fæÀPªRK¡B\x001aqp\x0001?jÁuARÍ×<Á$åTÈÊ\x0002?ï¯÷×?\x001f\x0004 |Ó\x0000òäÁ»â's\x0007:
3&\x0003\x001c½ï.O_/¢S5ê¤S\x001bWäíiÆwg¼0ç\x0013ôàé\x001aOwâáº
zdàL¨\x001c61Ûµà·si±\x001e<Sã^<ÅA\x001dx]Ð³Q\x001bÍq\x00130Çk¥gk<Û'¢áà¦ÓFçj£¸\x0018ÅYw´\x0007ÏÕx®\x0013Ïs1³ÜQ\òÌ~[Mçk:ßI]WÆÇ¦%\x0007g\x001f÷²wâ\x001a/ôâ	NÀ'Àé¤E­\x0019}×wo\x001bw9ÝÝÊ]^x\x0000=ÏJk0uÑ-»}PÝj\x001aUT±ii|8zñÇï·ü~ustvýéæúþÓ!o\x000fk¤y8§¡¯Bs\x001f\x00088\x0003j¾¹íý\x00110»<9;:;}~vzùüidU#«\x0015Èà`\x0015\x0007ZEmIùÖ{Y\x0003¬k`=\x000e¬=\x0003À#Qtá5	ØÔ¼f7\x000fÕÏ	?IïÑzôÇz`=}©hñÿS÷vÉu\x001cI¾çV°Å÷ñ	¤ \x0011f\x0000É\x0006IÝª'\x0019H¡$L\x001a$ëúénã¾ÎËtÏ,C;¹+\x0019÷\x0008÷8\x0011'ódD&»ÕfEÀT¿\x000f\x000f\x000f\x000f÷¿WÍo\x0000\x0007wÚwG
3C(\x000fEpU¡·?#"k§\x001cªVy{ò\x0006~ÆíöãÅ|\x0019©Þ¿¯hQ=:/ÄÛ²Ûí0*óWå:pÀ\x000bêfÔ5£\x001e\x0018HC\x0012^á5ä\x001bDQâ8ðàÖÍhjF3ÀèË­Àr+\x0010\x001c94pqX\x000fikH;0Ù6I 'E3G~ÐÃéæ¨C?¤«!Ý\x0000d©gV:\x0014%r\x001a!¿>A»!}
éû!½a#¤`Ý\x000e\x001d"3ê
\x0018CÍ\x0018\x0006\x0018Õ)"àL¢P\x000e®¼\x0008­-ÒÏ\x0018kÆØÏ\x0018í©;õ2MJa3¤ýRnÈ½\x000c»ZÒ£UJR\x0004\x0001\x000b\x00192kÑÂ²\x0007î<\x0003¬o\x001f[Vüî¹\x0017»$\x0005\x0012ÆÉgÑ@¸k¬Y jÿú­êë÷²0
\x001c<Ã(ösîäáò\x00051\x0014µùVrªóÞ$\x001bìnv;§¤Ya\x0015GBÁ>\x0014Ð\x0001§k¸\x000e{Óp%\x001b\x000b#xF\x000e\x001fÛ9·\x000eÎÔp\x0013ô&á`v5º\x0013\x0014½³&\x0016â@ªØ²ØÝ~ÖtuhìÙï¸%fr)|´.=N9O)E°à(Õ#`Zô¡PÔ³¿^ãvË¥ûÉ;ÒÕ!²%p_Yòëçà¹²R\x001fÎCY\x000e§k8Ý\x0007\x001bx°méé1è\x0002§\x000e\x000b\x0008,³5í\x0013EõÂS\x0002\x000cea×\x001e\x000c0.`3ûÑXÓDc\x0017i¹\x000bI%ö>à *
Z\x0004f\x001e,å<®ç^ðT§úñ(\x0007üAz5\x0003:
¥p0`ÜA§k:ÝI§\x0002Å¡\x0002j<ÒØyÉcg\x000e.tÑÎôÒI¡
ábÆè$'ÍCï¢]x¶Æ³xF±z1ê~qà=ÒEàp­e\x0007«ñ\'eç\x0014]<x
þEäFw(ú¾ÎïßÞ½Ø\x000bA¡\x00175ë<iÎ\x0016Ð2\x0014´\x0010ZfûRÅ\x0018Ð:¦j4Õ\x0006æ®Zi\x000e~è \x000bZ(Þ¦k4Ýæv£fJç]ãÚçãåhrß\x000eËb¯îÞÿz;­9\x0005T«ÛåB\x0017OÎÈ¯,®.=ûW\x0016Ã{GL\x0014J¿\x001c½âlX£¿VPX
¤k ½\x0014\x0008+O+_V,n\x0017¿>\x0003\x0002µ÷.i«{×²©·j\x001a(A0P¶\x0004TÄð@µw¬ÄÅw¬\x0005\¾$Z{MÝYËÃÖ_ý£\b\x000bÛ$|â¦631ý½n6:g$6Ýl\x000e§o¼æ6úä(\x0013±¿\x0005ã`î\x0006\x0017C\x0008®#©r7­øõ»ùQ<Uã
ån¨]è^sj\x0004ûj8+\x0001u
¸6wÃì%ÃÍÏ­\x000445àPî\x0006`»Q\x0000ån\x001c\x0005´5àXî\x0006Ç\x0016ëÜ
¾;\x001fÍÝð\x0017¢üEäVãÏo>ÜÞ|I\x0005CKúª9ê$&\x001dÆöúªé6íùÙÕùÙÛT/\x001b\x001dS5êÃ&í
Îñ,\x0000lú¢l\x000búÙtÍ¦ûØ¨­ujÁfNó¸yI¹§!î=\x0010ô°©ýIUõ¤Þ\x000eµ<"ýé¦å=\x0004x^·¢9
©jHÕ
©¤=ån9úTfÆÀ	íA»ö¼\x001dcÔ5£îfÛßiÖºMJz4)Áâòà"ìc45£\x0019`Ô]\x001dÆ m
iû!µ¢g?\x0007ÛE½fÆØªTw0~ÿýÑýü\x000bí¦?\x00182`_rLMD&ì\x001eoþéÙÃ¯7	Ðxi=
ÄÏ\x0010àïÄW+}êÃ°¤äÇÓt%\x0004\x001fæåó³ª\x0013¢cGò¿ì0\x001b¯«ÁÜë\x0015Ö7\x001d¤¿Vy®RøÔ\x0015Gz[D\x001fQ\x001eö
\x001bÊ½Îa\x001d\x0002ã\x0013*
&îí(­Öy(w\x000br\x0001¤üé\x0006çüæO?ò§÷\x0008úþ¿\x0001è;\x0004}78ói3or\x0014úÜ¹7Í}Üôg$ýùO?¤9ò¦þ\x001bÊ_ÿç}ÝB-]MÁ°¿¿½ÿwÁ\x000f·¿\x001fÅ4Ú¢E)ÿ G?\x0004Ï#\x000f*fá\x001eýte\x0005;ÿìüò
Þ
¯Î¯§ÚÛ7¨Ù@¡Âüç'\x0006\x0014,÷î¨Z\x001bG¨%\x0011e\x0013ÔÜqlpTñÀyT-EVÑ\x001dqP\x0015çGn\x001bÅ¡:¥ó\x0011FU+^\x0000Jj^\x0000Ñù
QsÛÁ\x0005 Ê¨ZåyTµ*k5Ê-\x0017\x0000|¶\x001fEÅÖs2\x0002´Ì¤\x0012\x0013²3©W[Îÿ®ïëÀü{¿\x0001ÕÈl§¤
øØ¤F°Äì&¤`Kâðú|ûÀg\x0013\x0013RaL
o)\x001b\x000fYÿAP,§e\x001d¨15*\x0007&aL-µøA5¦ßÈÖ\x0015]h9<ªØjÔÓRÕ¹*\x0013® II6/U©6d\x001c>¬p0Ù\x0000pí-,\x0001%yÿû-÷Ì.@Ü\x0005¤ûñÉ6R¹\x0004\x001cEÐ|d
\x0007WØLlW\x0010;AºÂxÈ
TENÄØ>Ã¦ÇMav .Áõ~bð\x0005<\x0011+Í&,/à(V[°_þåý¿ý«¨î«×\x000f¿|¼y\x0014ÎYM"¸>VÚ\x0004È¦`ëÆ+öå\x000f/Î¦²\x001b\x001arý\x0016Ò\x00188064°íMÜ$oqÀ×;8¹qÈ½û³à\x000b÷gÁ!ßçÏ¸øaëÏBÕ\¼þk©þ&ï~¸;\x0014¥ÂÜÊ\x000f·GÁ,æ§`:5yøË\x000f\x0000\x001fdÌ`»~;ïeùòj*é­AÜP-GÔ9¿\x0016\x00115µ\rØÅlñþý\x001cAÜ\x000bO-E41êS­(ª÷úìN{|\x0007O¶¼,¬FÜë"¿\x001c1¨Sçèsn\x001e\x0010bGºL¨å!0[y\x0016é½(\x000f¢:Í~ÇÇ<\x0007}§\x0011À|o\x001a\x0018B\x000bã\x00010HMñ\x001dé&ÂËµ0ßÆÖaeÉ¯Çvß<Ëb6TÖ/J\x0003¨`·J°\x000ew
":¼\x001ceÄÒ\x0016i-"_\x0006\x0018mH\x001dMÑèy\x000eÁÅ±^m´ùj4À\x0008Î/
] cô¸ ][GFW¤@W3Ò¨\x0011Âeb\x0018ÄõÙó5ZÓáâÝVS
\x001bO\x000eYî \x000cïé1;OáE\x001dh\x0018Xtþ\x001dhåÐ\x0000Ââ¯~@Ô«1É*Ê¤\x0011/)¨¨l\x0006\x000cn\x0019àÔ ~þ|ûPÓrO'/\x0016mTTÆ©!g\x0006;ÎÑt³Ù\x0015
·lðW/fcÇ\x0015\x0014\x001dÉ\x001dP°1T¾GçrZ¦SøøËPþ î¢Cx9T°IÖ\x0015\x0019æ+§´\x0017\x0012|k
âà=ë8TüøóûÇ\x000f×·?ÿ¼(d;q£E÷\x0015ó3\x0002ò¹Õu}þÝwÓ·Ò
nÏù[\x000cs»Q>Ê.{~H'f
Èbº=¿o!Ó17\x0005<­s\x0017s¸Ø«§\x000e>Môãíù|Kñ¼¡ÀiPpË7Ù¡R§V\x001eõÓí¹S\x000bé<*IÆL'v±r«\x000cá¶kçöàCÙ`w¼ÿÛ¿ÝüÃ\x001cÚºW\x000foÿ9\x0010w\x001f\x001f\x0011\x001e¬J.¨\x001a\x001dgkò%>;FT3¡¼zyýæü{Ì¸x1}NT´{Þi/­¡òªè%\x001d}bº*ã\x00067{ki\x000f\x001e»ïì/VýÒ¸.}zÿði[eà¢ïI\x0011îÃÜSÔ^# N\x001diÏ._N¥6Lì
,f
6¦þ\x0017È\x0014Ly\x0002µ|\x0014/\x000eÁcL·á_ÂÏ¿\x001eZ¯n\x001e?/Ø\x001d
ãñÙ¿i¥£V¸Ôþ\x000fE(
¶ÚËWg×oþJs~ÿ\x001alïÜX
æmJVK`âð\x0002U¸\x0019lþu{\x0001ØÞ±\x0010\x000c\x0013«Ð&'°FÌäwW\x0000\x0007cÁ=`9¦Ø=bX^MS\x0019Uî{\x0005#4¤\x0013?-\x0016íbKÁ\x0002XöÁsK5¶Q!\x000c\x000fØaoî\x0018×\x0007õø\x0010jãË\x0015¢7'¯oÞ=|¾}|¼;nÌ¶(7ÂzÎç¹N;: \x0014ÜK\x000e\x001eb\1zvòúìéË7ç××\x0017çG\x0018Pè\x0018ªHU5\x0017\x0007!«Õb\x0003¸)6bM\x0007n#ÙËjrau\x001aW\x000b\x00145r¨Eê©w´\x0005¨°Eêêªü\x00076Ê«»ü?\x000f\x001fcªà¨\x0007zõ0ýùúcñÌN}i\x0016ò5æÛW//^<{9Õ/¤ÂT5¦\x001aÁôC\x0005[\x0016Â\x0010\x001d§zìïáÔ5§\x001eâô)ë\x00149±¹$N~\x000c\x001d^NSs\x0011NUSÇ\¥\x0002ÞIæ<xííå´5§\x001dá´3'°ÁHjÛ\x000c9\x0018(ÑYÜbyº\x001aÓ

§MÕ[i85¥R4z9÷5¤\x001fÄ¾×9·+âv"NÍi(>l²BÍ\x0019\x0006S°¿ëTÐÚLõ5i<Õ\x0016K3Öq\x0004\x0013uÅòx46w$sZc\x0003ì<v2\x0001¥\x0014èÙÂ\x0011P<\x00084rú¡Æð+\x0007nÔTVO\x000fh{\x0014EØcPÐ\x0002\x0015ò4ïu8èy}J¿ÁúÍY$\x000e#l³\x0011h#\x0019i£UNì\x0001m\x000e#9r\x001a¡0[HwÿUÒZK\x0013ï¢ÜbâÃH\x000eF°Í)ë\x0014ÛìdI\x001cïÜb<ÃHF\x0012f;dÎ`Êi\x0004\x00068]iï·
´9äÐyEDºDµi
J7GÝÕ-8\x001bK/L=Í$ÙÐ«ÑJ6¡ù\x001dª1¡jÄ¤ð\x0014\x0016Èæ\x0016]h"¿\x0012-V¨jÝä\x0011Ó$ÃÎÖc\x001fO:\x001c'jS2jÞ\x0003Úly5²åeÈÓJ
<6?ªÁ>NÙë¡lö\x001aÙGÒ,\x0013\x001b>	Ê&P\x001dËW\x0017ÎëQ)Ð/W¤J\x0018­çö¡ð\x0002ÿÕ-InsIRusü\x0007Õeîû?§F\x0011\x000fwÇ\x0003ÎÃ½3\x0007P\x0019:¯\x0000£9&¢âÏüýË\x0017ß¥Æ\x0011//¦\x0014H*^]óêAÞ$ÃqXx:C:M¬(¶¤¦R6»yMÍkFÇ7Ts\x0003ìIy\x000e\x0006X:\x001a`-\x000eÆý]
ìF\x0007\x0018ûJÅ\x0012ïÌñ\x0012£¢@ìL\x001ao7p¨Ã(°×I\x0000\x000eW\x0004°kWâh£Ñ[
pu\x0007Pº¾\x0003t\x0002GÅ[ô^\^\x0012ÚJC:9cÌ\x0016\x0012\x001b¹g#l\x0002>\x001f?¼þòÛo÷ÇÃ¦)F\x0011r,ÅÈHEs\x0018ó¡´\x0001Ø³\x0017¬\x0017oN^¿}õêrúùªà\x001a×\x000câ¢\x0016D¾¶\x001a\x001d²¬\x0006:±]fO´\x000eV[³ÚAV¡
«1|Ó
QÝÖÕ´n#Ô\x0006Ömä$\x0006w\x0016:`C
\x001bÆ`ñàò\x0019l¼¥Z\x000fðm$ãû°
n\x001d\x001amh 7ä1"¯£vÑèÚ
JÂRê`S\x0017o#ßÿ`O§ôìÝ»ß\x0017DÕ#za|J,mâPyº\x0012\x0007ÓÚ¾åÙÓ§g~!.¨ªFUC¨xãÎ¤.Æ,MÇ&AO;â@\x001b5®ü\x0007SÚ¯G@\x001dêzÓK#Ê\x000e¤x\x0011Î2©\x000e²\x001eÕ\x000c­PU:!\x0005{\x0014Õé\x0017jþÒKh&ÕÅ]¤º&Ð=Fm¦ÔS,Ë\x0008ïÈ;Ðq²ä¯ÔÔ¤\x0013"±Ç<EãRm:º\x0005Dpj©â\x0015øIóÚCjkR;8¦1ÝÆpL¦Û\x0011Á'q;÷T¹\x0018ÕÕ¨n\x00085 äHöµÀ°f©Vðf
¥ßJ+§¯b=¨¾Fõcó/"gg\x0006AbL°\x0000(\x0003\x0012FUÉ\x0003«\x00075Ô¨alT±8ÙäQU^0Ò´T­¾÷Æ4
*Ìäë¢¢SÕ`UbÉE¼/v V.\x000016ª&7DÆQ
Y\x0015Þ·ò°é»m\x000fk{TU\x001eÕ{#\x0019+GoCF¦Ri\ý&U6g\x001c;¬PiX%\x001b^Tnóà0¯«ÓÑâ\x001eÖæ´cÇ\x0015\x0016Nñ!à\x0005Çc¤òÆ5èMXS@\x001d\x0003ÞêSÚZ°\)\x0012#â%\x0010ç]À¥¨i¶\x0015#\x0019tå\x0004J¤/;KØY'p)jc°ä Åé¬\x0000·Õª\x000cX:l±³Tc\x0005Ô\x0015Àò&o¬ÃªlVÚXf\x001d©ÚÏ­Q¢M¯úþöñ\x0011þÛE@\x0006\x001bF{J\x0004
üüê\x0002¥¥ÁþõZÎN¾?¿¾~ùâÅ9¦\x0002\x001dV5´Z\x0001-É}\x0005hÉ·XÇ¶\x000b\x000cä¬íêÖ5´^\x0001MylÖÓ\x0018d«é~ZSÓqZp¶(X¯a=Ó\x0008[®fX¿³\x0019³­íªeA«Âh\x0007ÁUÁ¹röèdv5³\x001bfÖq4(S1\x0017
´âºåé§~èPC\x0015Ð.õØ¥-pìÓYC\x000bZLÛ\x000c@Ç\x001a:C[¾I
\x0015è´Ó6FZ\x001dÂÉå»ð`V<\x0003×\x0001qÑ¸½½ÄØ\x001c%\x0003ca,e?\x001aË£l\x000ee\x0010·Éøi¢cIÂÜ8zàuÆñjÖ\x001b:Ù&rü8\x0001ß®\x0018Baâ\x0004íÁ¸\x000bÃ?\x0017dè¤n\x00139~è`ÊX+êfÔ\C+¤ØÎrÈæXãç
fqS\x001e¦W(¢.bc\x0018°\x001dus°ÈñEû@\x0017;ø\x0017q¸T;*SJ\x001dZ¶ö
´_1Ô|f¹kZRZHÉ¨ì¦VÑSãF\x000fîJôíÉ\x0005\x001dâAÒ³°vÃóÐ4©
Éajsê»}&K\x000e\x0008Ü®é±Â¹âç	·¡\x001dQûìR­×Z$\x00150\x001cx¸aqõSl\x0004q®<m\x0004×ìþ¯.O±È «§º\x0005iPÄÛSäëÄtúíSl$2÷¶bößV\x000c_Q\x0016Ây\x0011H¤D\x001aò\x0005\x0012\äKªÎ\x0007_\x0008§k8Ý\x0007'-üM\x0008É\x0003©4p\x0012|ºul¦f3lé$HlØØ¼¼RM¾ý/³5íSIµ\x0000á¬r¨eOt~ò&´ÍÕl®
Õå2S¹Ù$ @q\¬¦\Çæk6ß9©9¡\x001fá\x0002¿1I)(f§^9§¡f\x000b}l`áè¥ÎÊÈÉ&)l'Õù©Ð×Q¸°oãBUúôì×/Ë-éÆÙ\x0014E{l\x0003g\x001céà%\x001d&Z\x001d\x0016Ë/ßÏ½ý~ºaR\x0005ªkP=\x0002\x0003H 6U&PE¹\B¹|óå ¦\x00065\x0003 ð@Q#<;ri¨öÅRd8(/Ô
jkP;4¢¤,\x001eÊ\x0006Tqþ3EË9]Íé\x00069cöÕ¬Ð\x0019ØcÐÛÌ»¯1ýÈ¼;{ª(Äé=½vjo"gjÍæÂ-\x0007
5h\x0018\x0001µ¥ÚQ«Àã\x001diÈ\x0005\x0007EÎºAc
\x001aFÔ2W¦äÇcð\x0013\x000f
ÚõRVQ\x0014´ bh<-@) H\x0017 l\x0005Ã\x0001Á¹Z­å¤­­\x001f1öÆ©]@Û°Î7% ­ç\x001f6Æ^X{ã\x0004ßµe]k ÕcÙël¨ÝO\x001c²%qèÍ¯üûÃÏ\x000f·'w·¼ù¼$F¢X|\x0011ÓÇ²¾
FvØ´_á¾y~þò»×pµ¹8ÿñúìÍqfU3«qfgYb.]ql\x0013!IÇÔoÒÏ¬kf=ÌlPk\\x0000ÁH^ðkÛ\x0011ÛØ\x0013KÍg\x0013Ôb1Å\x0019\x0008YI\x000fð+æÛ®ÝÏ×±%_g\x0008Øä\x0004a¤çúÔ)ØN¾\x0013ô±¯ý8r(eÜ\x000enN\x0014ëóE;µsSö·9ÔÌaÅJÖ\+ma÷\x0019²o"Hv¾&%\x0007º«#ÎîòcF ±ÍU\x001ehk,iìi¯ø «ÂffN6fNÛ9¼éK¾à¸SòÊ¬¥\x0005­\x000fë¡1Ù3GÃ¯åèñòê\x0014\x000c@w»ÕÑ\x0018\x000e9n9,ÆÙóíàNNGv\x0010¢®íäky?t³
åø>´R*pSÔto~òvÑo;d\x0013Jµu\x000bÚEö9£\ðÃÀ¼\x0019Ídç\x0011rnR[ÈYÀfÄõ\x0000îsÃ´\x0013$\x0005$Ô\x000cXz&ý\{£\x001aa)výìáñãíçÏ\x000bb9XCÃ
\x0013ïÉ¤YoMð1Ó.i*\x0011È\x0001ìg/¯_¿y3\x0017Ü1ûù÷Fí×\x000fõâc)\ðíHóX[g\x000c¿ÒÌkÜ\x000càë\x001a_¯\x001cý ù¹F\x000b~ð5\x0000Í¯\x0006ó%¨\x0003ô¦¦7ké¹¬\x000fð-¿¡ZQ\x0012\x0019äÁÎgkðmo×.}O)ç`U4=8 N\x000e?\x0001O_oFñ}ïWâ[ÏÒÀ
uHIXÁ±Â²ÐÓ)\x0019ø¡Æ\x000f+ñ½§t#TÃ\x0013$X\x00139@\x000bþã±Rª^úXÓÇôzg6Ý\x000e\x0017l2ñùAüº"L}U\x0011Ö¿x"Ëcª'³ï\x001c[ãl½üÙ+í¾2\x001d\x001c\x001cÊaÄf6<þ}½_\x0019¯u|yuóåýýÍãÏK\x001e`aØ³\x0007,ä{³\x0011Zpi¼ôn2ïÕÙÛgg×ß-\x000065°\x0019\x0006mñ=±Æ^z¥n,áUûo>j÷æsûéäÇ¿ßÝ>.(ÖÚð¦ØNÔçì\x0018\x0017¦\x001fá_üp}öãÅùõlÍöþ«Ú½úô¡ªRÿ,½f-9ëdÔ©ý¨¶Fµc¨¥it\Ol­&hg
szH}MêH%\x0017À5²Q-ÅFzúÑ¯\x000b5Ö¨q\x000cUóUX*Q\x0014$5wsÙ¶\x001d¨²ÝUcÛJ(ÎWJÒ\x0013¾¶TX§zXm%öÂ\x000e#¤Ñ\x0018¹|@ÃuX\x0003¬m@?\x0014ª6w½£[2ÀÀ»kæE`\x0019¯Þ·®:´\x0005\x000f¯n?ß}¾Åt§E}=\x0014\x001c¼ÔE2ìz°l{Ô5ïw'Â«ó7\x0017oÎ1ßi¦ëCÁV5¶ZíCJÈO\x000fÝ©ÌíH|j?O­\x000fçêJz±MmV`cçc±}éë\x0005÷A5úHêBl+÷ß$.W÷7ïoOÞ *î\x001fÿþ¸Ð-#³¦¢<5$ï
Z&~p_]=;?É¸×\x000b8UÍ©F8á¶Mõ$J\x0017ï]Q­9ìîi½ºÆÔCÊw1m\x001d\x001a£='Ûbô½¦æ4#¨ñG9\x0002ø2DÓ.7­ÖsÚÓ\x000eqÊ\x0012°ð®Üø¥)ãyðÆßËéjN7Â)BÒ"Lãi¹\x0016G³\x0008\x0007ý^L_cú\x0001L\x0019ôn·;î\x001a¨wI¯(»3Ôa\x0013L\x0011\x0005z´R$,â£ºl÷CNÎú=*K¶ôzQ\x0012\x0019dI\x0007ûY@\x000fæÚô6æSØO¼^åÎ
	µ\x001dË~?(í¸\x0018S½ÓHúB\x0008DK\x001c+#<+\x000b©¢CYÆ\x00080ç\x0007ÂÏ:UD¨jBÕOh=é¸	ÌÛ\x000fRWö¹ôÓ:nË!u
©û!â×Q\x001dxéÑC\x0000XÑ1çý/45¤\x0019Ü%'À~Wüh4S\x0015³\x0018ÑÖ¶\x001fÑ'Mü4n©1´ö¥TQùzñÅ®tý®\x0005±%,ÕSzëy íLßbH_CúnHì«Í/ß,g C9Äçä\x0016#\x001a1\x000cL¶cá-|ånÇ|ÊÍtX
Y\x000bÔË)á²Lñ2kXÛ"¾\x0016gô6ÛÈæ¢,\x001býÓ?©4zïÄ\x0013NþrûñóÝÇëO·¿½?þ\x0010là²ÆÊ²`(O©Ë©RT9¦ÌÁ¾kÈúÏoÏ_¼¹xqrýòåëó\x001fÏ/çÞ°Í~\Ú¸t?3ì)\x0006\x0018ïõ9_\x001eÃd`zY×Ìz|!`6ÂÊ\x0003[§^ï\x0006MMlG\x0019{I\x0005_GÅ-ù¤®rQMWN\x000c@Û\x001aÚ\x000f³M"\x0011i¤±T6\x000f4½3Ê¨Å¤Tç\x0000³«Ýø@ÃMÏGÚÜeSz\x001bx 1~½\x0019´¯¡ýð@£¦Ø\x001aPæ\x0018
¬ï
ö#ÔÌa|q j_ \x0015-©âTz)ÊÌz\x00195t\x001c\x001fhî¡Äæ¤55¢Âd7~èúáv§ð;2ÔÞ³þ»\x0001\x000f.ÒòPÑo7Ò²=
ÇÏÂÔKAí6"501òF|©\x001d n\x000eC9|\x001aÉK2T8Ò:P5/¼²\x0013EºP\x000c@7g\x001c>\\x000c*<J¿;\x0011É~(îû¤&]¤\x0001èÆNËaC
ëÃ1´ÚnÀúà7[å'ß\x0013\x0006¨\x001b£'Ç­^È
9:\x0004*\x001d\x0005jÃî³S¢ýÔª1 jÜ\x00048½\x001d\x001dØG49ÑÒ \i¦VWù\x0001êÖ1\x001dßA$µÔ*I$jÏo Ø§}CcÝ¶kH\x0006ï+C6[r·ot«³¦¡\x001fw^ê\x0016gºôû\x00113¿/\x0018üÛÝÂÔ\x001ai\x001dÇöÃD£+Òì\x0007[Ìî$Ø^]\x001cK©!\Uãª?=®®qõ ®ð&µCÂÈ)¸{9i\x000fþ!®¢uÓº÷
íTðþk¯	\x0007º~^ªGT*P4ª°P\x0015I\x001cÂÉuDM$õ¹|sDÃì¿ô½Þ.dlÇêÊðRàÅ¼<ig¢½ÈºFÖÃÈà!yzDFJY\x0008\x0004,Ýt*^7r«\x0016Ç6¨\x000bÉ
ùÐ`oÇ\x00129^³Ì9¢WÕ5Øûäz\x0005¹6©µ[2\x001aBqÉå6¸z\x000bzÍ\x001e\x0003\x0017ûÅÂVÙúOïîïôýÁ\x001e\x000eÒCJ¢£\x000e(\x000e>­R¦ãÓËËÙ¶?b¿QØ*§}1£6"&ÀcHaÈ\x000bs×K\x0019mÍhû\x0019Áù1Ä\x0008Æª¼\x001cwt\x000cÞÍ$¼.eô5£\x001f`Ô\x0011Sí\x0014)²«\x0013¦\x001531t3j\x0018Gê)\x000c¾s¸È	V³mò2Æ1ö3Ý\£\x001a\x0013½ý\x0019Éã¨ç4\x000b\x0016BÊvc÷ïlÌ\x0001¥¼:±Óaµ%F\x0015f2È2ýªjSªª¯\x001f~ùxó~Á;\x000bXFE)â\x000b±|\x000c$3y,]¿üáÅÙ³ãp¦3ppÃ-	ø$!EÉþìq³Mÿô¾¦ÓOÞwá¡j\x0006ÇG+Ð\x001bÖËfòZK\x0007\x001d¼wÂ¶"`Oá\x000fðPIùd{Ö[µëY¯èµTxåYÀ^\x001eTÙNIdÔ±~jü
 ª\x0001U' ö\x000fÜ\x000cBQ\x0007k°ÚÜ	Æ¨ÍM»\x0000u
¨{GÐûÒ­\x0002E¤t\x001eA§¸­ÊáKG\x001f`åð\x0010$þA'§fÁ7od\x000eÝ\x000bo©Â	0Ç)CØçÜöK¸
=ø|·¢ïîn¿\x001cß*Þ²>8ç\x0011IMÊ\x0015©+}0ì}yòüåóËï.ÎßÎ¥ëîæ)³§÷ýðñó
ÜÞºò³Jí\x0012nnªô4ó¤9&ûòÅ3¸È-IQûÂzÊìi\x000f}Ãm_î\x001cÔD\x0016ÕCùÎqD'²ÿ\x000btý\x0005zý\x0017\x0018jÂ"Ào§{´	å§¦ûI~©?À¬ÿ\x0000Á²¹\x001a\x0005\x0003}*7Õc*Ðý_`ë/°[|¡)Kæ/ànhR#ý_àê/p«¿À\x0005ÎmÂzªl0]\x001c©§/.£_àë/ðë¿@aå'§6ræ­/xÇú\x000fô@¨? lñ\x0001\x0014ü0C\x0008\x001f\x000bÌ¶æ5\Ë/#x\x0002\x0003ë\x001c{É:ì<Ñ­wq-nö\x0005ÒGfÀè¢ó-\x0000¨\x0008ÝØ¼m·ÞÆ²9Íäêã\x000cóf\x0003WrGò\x00171o?a»E$Ü~PÇµþÄÓ/_\x0016\x0001BJ\x00170ðl§=gÑJ?­¨¸¾|ûã±\x0018Ûó\x001e\x0000W
â¢Ê\x001aWó@±_6;=G"«ËiuM«\x0007i/\x0011\x001dª\x0005ÔX\x0001J¸³\x000f\x0017áêý;¶¶Å\x0015,ä÷·÷\x000b\x001e¸tj|_\x001dfa¥ÇDê|^§\x0003\x0001W°v_>yóóÍ§Ï°Yø/ö)uM©û)=,Q³Âf~òMÆi@aN°r1¦©1ÍÀ`J[\x0006Ój)\x0005G¤\x000cæ¬¨ÃbL[cÚ~L§4?ÅZ­xÎ\x0015)ê85ÓCéjJ70çBáZ¢T|:K]2\x0019uÌ¢êÁô5¦\x001f\x0018LT\x000e§t
'È	\x0002×AQâÖsZ\x00121C\x0019\x00060ÁÅ\x00144(¨Isî#a\x001a1\x0013ð[L\x0019kÊØOi=vwIc\x0019\x0005\x001e'ÏÛÇN;dË!+\x0017FÛZËbùX\x001aÚwàXæøA\x001aK#(oä\x0016\x001b¨
ñê&Ä»|4µN2mÉjÓH$Bd£9÷x³²9äÀ	C\x0018Ø\x001a±(-êÆâØ\x0015+ót¢YÂ\x001f Ïô#ÆÉ?Ü<¿ùp{s<Pd\x0005*å#Ý£bfN%Ã$|¤\x001bPÄñG\x000c_<?»:?{{\x001cSÕj\x0000\x0013c+ùFÝ\x000c3e0ühnâAe¾^J]SênJ\x0003SÊ	õÞ#!åmJòìá²^L[cÚ\x0011LË½ß#Ï\x0017°fÑt5¦\x001bs-9Ü\x001f\x0004WBJ\x001f¸P×ê)ÿ½¾Æô\x0003£éì©ÔiIRT:\x0016h\x0003ÙK\x0019jÊ0²Ïáz\x0011Ê`R¼/EäV\x001f\x000c®÷bÆ\x001a3\x000e\x000c&Ì¹£Á4¥³eiúµîå¨ÌVS\x000cpÂ¾¡"òàDÉÐÖ¬´e?ä¸÷r¶Ö½ß¼·¡H·?\x0004G·aé¸«²óhtÖeüéñ×ÇÛw_È$¡!º¼»ýròÝÝç³/\x001fà\x00040\x001d\x0012\x001e\x001c~÷þ÷º¿ù'ü[¤S\x0006E¯\x001d×à\x0001eÏ
îV¦ímPØý\x0015ï\x0008uþäòâüíÉw\x0017oNÎÞâ\x0019yø"Ù°¡V!þêC%\x000eì~\x0002|k\x000b1\x0006Ç\x000eöâ(ÔJ>\x001c»Á3X§\x0017Ïgó\x0008|ÙYC<¿	\x001d\x0018nüÕ=µX\x0002áD\x0012B8ës£@ \x0013¬b¸\x000e\x000fØ'ø«\x0017\x000fNbh¥Å\x0007\x001ewyðLVè\x0004¾¨7\x0019>ÌÁ_|:ñóyñYëP\x0010\x0000ùÏwYÝpÃ8»ùô»¹!\x0007\x001dg7>Þ\x001e£²ØM*Ò¬¢\x0002>Nh\x000b\x00075¯9)\x000fÚ³ë³×/&B>-\x000cìRó§Eïþkaþåþã·Iê\x0002\x0018,Æ_×\x000fîn\x001fâà«yvDa£\x0005ï\x001eÚ	\x0013³ëéº~ùz:NÛâÀÚÃ_q"µýÃ}\x001f²D\x0008à° \x000e[Ç\x0003¶\x0004-å:¦¨+àhÀI'\x000f\x001cGG\x0003Æé\x0018Î?Ü¯û¿\x0012\x000exÏøëò6u±øô)%.Í\x001b$¸\x0018f5l\!RÙ°Ö*f_×å<´~.ÏSÿ×¯_¾<¤ÿíï¿½ÿ\x000bb¡ç¿\x0010ëñá_¿Ü\x001e7CüZ´OâjH¥4]»¬6\x0003\x0017ûT×/ÿùíùI¨\x001fÄýßÓ6Ã1þººù\x0015\x0006óèÔ\x0019\x0014É ¯\x0001Î$ÑárÞgÖ³p^Mtuö\x001cÛ\x0000.Á\x0018-Æ:GÄ\x0011'ð!lr\x0005â\x0003>L\x0007\x000el2üµ|tH\x000cFGÒð8·ÑðÀ¾À_ËylÉE2\x0004S\x0006G\x001cXÓÇ`Âw\x000f"VÇ\x0005,ç+p}ï\x0016ì1KoëÚK\x0004Êª¦;ó£\x0008{Ëù
üãé-¶CB§ß÷1¹t\x0019C&ÌWt&3Q
­-
«ú°*k\x0017\x001e¢?ÀðÐ\x000f7\x001f¾=¹þrtî4jôû¼÷\x0005¦%+	S$\x0017NF{ÀJþp}öâ»óë·Ó²À©\x001aNuÃ9Ep2ç7%8Ip%;z\x0014N×pº\x000f\x000eÃ}Mé\{\x0000lÑÐ2S%»|ÍÔl¦ÍdíYd\x0013téRV¸Âf\x000fXô\x001e6[³Ù>6kN³ñ\x0012p!yÜ¬2´à<dL{Ø|ÍæûØ°Ý9
\x001cÊzä£Ð\x001aËû´<Â\x001a.tÁa+\x001bC+\x000e{\x0015'#¢ÒgU®\x001c¹XÃÅ¾\x000b1tRíB~ãóÊñÈÅupR4FNô
]\x0010¼WÁÈ9\x001a¹èwFîgÚ\x0003×Zà>\x0013½Q\x0014ïó@Go\x00088tjåÐ5&XöÙàôxMt
lpóàÉò¢;àjô°5\x0016Xö`çh¯[-óv<©þÀ©ÚÖ\x0018`Ùg=Ø6\x001bÊKï¿0n^G¦3ë\x0007Ù`ÙgaÄòC\x000bNªã
á\x0015;mJu\x0007D.r/t®Î:õÎtÔ7S« r8ÒÉtÍ\x0011!ûÎ\x0008¸#åò	Ü®!×IÂØ9¾.)%Ö9%²9#dß!áçx!Öïd[\x0012¤\x000f<tv¥-iÎ\x0008ÙwH`"½ Î¨S\x001a¹ Ë\x0019aÖíXÕ\x0011ªïÀðo {$©K\x0018ºÈÎ¦
=tÍ!¡ú\x000e	\x000f^È\x0003aU~±å\x0006¡õº#Lµ~zß!\x0011rïÐ|ç
9\x0011R+Ì|)w®uÇj	ÕwLÀÞä\x001b¡\x0000\x0007ÏYÚ\x0014×+éBõ\x0014ÁÜ\x001eÆN\x0017·.zÞ\x0015Z»¢9)TçIáMñ=iÂØ)\x000e¡+ë×ÙbÕ\x0014ªï¤À/²vÒRI%\x000c0¼î\¹gBu\x0014QñI!ña±Ul}XwPÍI¡úN
Ø|Àp²ôøÀ\x00171¬ÊYG×\x001c\x0015ªï¨\x0008ÖK3[Bí
ö
{(ëæU7'î;)0\x0001Dg[9ì9,¡¥ðäh§×nN
ÝwRàºõÅ\x0016lí¢\x0016n#[¬B÷\x0014Ià1Ûb\x0005§¬ÉÑ9©98çÝÊ¡k#:}\x0007EÀIÚ\x0012X\x0018É\x0014ó=QK¿rèBw\x001d\x0014Ø;(5bÀ¡Ó.<Z:~mÕqí¦h\x000e
ÝwP \x0002cSl)F®b´MñÊn\x000e
ÝuP\x00180|P(Ñ²óÖ\x0011+ïØº9(tßA\x0011aféY\x0008ë1òG\x000bÅ^»Ö+M±n\x000e
ÝuP\x0014¦ËÇXjØFë-±QzåÄ6çî;'¢)7Y|\x0016É¦X44ÜÊÀi,±é³ÄId5\x001d\x0012N-¢0åX·[McéL¥Ñæ÷\x0008\x001dÈ\x0008[f\x000b+/b¦±$¦Ë³9Y\x0015÷ª8¥­ê¤å­º2ÌiO5¯ø'=ã\x0017Ê \x001ec´c%iï¥sl]xGû}H°)½¤´Ñ¬X:Î´ÀTEòðôÊ±úésûºó¹÷Bp\x0004/äVËøLaË3ÅºU¨íWch»ÇPäm"(\x0003(\x0002Ï2v\x001f\97í\x0000ÞôÀ\x0019çs/¾$F<àÒ\x001b\x0014\x0018éÂ:w\x0005\x0015È[¼w]ó«|p_\x000e\x001d`B	Ð®\x000cýù%ÅÁ\x0010²¥JBÓª%
x\x001c\x001bD\x00161Ö\x001aVô\x0007M+\x001bLòüòã\x000c¦:Ò(ºËñ°Ý;\x000fãN\x0013½Écaùö3Ìò|û£ U´[ìZÕwZTåy9êòÌb}ä	×¬nRÑÚoa\x001b%¶®Õ%k\x0014åQ(£K\HÙ\x0003û§Wí/\x0001U-¥é\x0015Âºâ÷£&&e
ÉÀþ×¡GpªÆä<£ªfT\x0003;\x0000.ørÅN¢1C¹\x001cR×z\x00082Ò¡\x001d
åËaI\x001e_\x0002L<pàôB\x001aÒôC¢4X>´µ\x00089ç\x001c«ð8ÐkÌå\x001aH[CÚ~È ØýõetzÅ'ÈyÉ½®týÎQ¢\x0001

\x000bE\x0003©ÉûA'm=£¯\x0019}7£Ñ£§.ÌÂyß\x0000\x0019mnë\x000e\x0005{!C
\x0019º!¹]:B\x001a:´|É²îPÐ¦\x00172Öq\x0000Ò/äÄ;@*_\x0018×o\x001bÓl\x001bÓ¿o0PR"!¾l\x0012¤\x0008)ã¡\x0014Ù^3ÙÉTVzË­¥É}aÿ`)\x0019\x0019"Y\x0012ûÚÀ\x0010É}V9Ä\x001a*ËÎ	OàÆ±dÌ¡,¶î\x0015Z9ëiÞtÏ°õ"%Ënw\x001b¡Å\x000ccVej9ÿ\x001f}À*­úý¬Åªkù):xQ\x0002?BçF\x0014ZEÇ1ÊOºÅo9±ò(¢ª\x0011U/b\x0014_\x00050Ñ\x000eJôf{èÛ¨kDÝhðÕÌ8z||kÃÁ½CÊ¦\x00064ýM6/õ&w5¡­	m/!úB´Y\x0014ö¾ ¯Òòû­ë\x0007Ñ7èûG%]ð\x0015×e½ÔdwÊ+î¡\x0018nïf©íNeôniWö\x000b]s£ãDd@\1Fì\x001c#Zí¡\x001foîïÿøDûì×?þß%g°ì^b\x000e5ÅP
\x000fé¬?ÁÏ	þÙóóYsiÄ-2¢\x0015"êf×1JÌ (±¤ð¥âÀ	rÚ\x000f\x0019×5¼^\x000b/²\x00029&Ù\x0019¬ËòZb'­ê\x0018»©ÙÍÚE£ÊÅÉ{ÌÍ«Æ\x0014§jæ<\x0002okx»\x0012\x001e#Ý´jd[,K:¾q\x0008GØ]ÍîV²+Q¼Yç¸L\x0005Y\x001exy(\x001fs\x0005¼¯áýÚüzRáÙ\x001f31n\x0004/÷ídÕ?\x0018pï\x001f>¼\x0001'òxMÓ.õ	K¡éÀ%\x0008ÜM\x0002cÓ~êÎ\x0008/_¼\x0001?rº¸U4\x0019U
¡JK©ë\x000eÜG
\x000b)Ç\x0015ààL;=¤º&ÕC¤°óõ1R½£þ­z¨´i\x0000ÕÔ¨f\x0004ÕF.Vp¨ö\x0010©Ì#HN¹­ö¡Ú\x001aÕ\x000eêÈ\x0013ÀrÒwðÿ¤Sâ\x0005\x0000~zrysB/\x0015¯înß\x0003öÿù_ÿ{qá½§\x0014¤~\x0008É\x0016Ø %É*\x0004HVáì.^]?\x000f8VB^4Ý+Ç©\x000eaÿxûøñöËÝýñåà\x0003*±Ì,Pa
gT\x000eµüx~ýâüíÅåqLUcª~LizôÖbRUFÂÂ\x001bÛ´_´\x001cÓÔf\x0004Sð\x000b¹ðW¬
v0Õ¦ÒÕîO;¡Æ\x000c\x0003Kswº\x0000¦\x0013|ñð~\x0015¦ÜßAÒî7\x0018ûåþîÓÈÀaXÍEJc\x000e¥ð@ÏLûåÉù\x000f\x0017¯gÏþý=$í~k±å \¶©5=X!(ovyHÖ¢\x0017´.1±¥b'),Qzà\x0017Ø±+{)ãÜÏyÇHß	\x001e(,\x001fm¶LÿÕÃÝÇÏ]6ßDË%\x0000\x0001¼«¼tP¼ë£6ÔVÎN^½¼xñ¦²öSõÄW7¼zWY9\x001dYºFRÑ|ä}\x0015\x000f\x0016=/¥
?=þýñËO\x0018kðp¦ß\x0000óêæñÔ!Étéþø÷OÿtþÛo·Ï:ìôºiì0\x000bÅ½r\x0002­«\x0001Ï_¿zuþ\x001a	¯Î®/gD"ÂOüï¿Æ¬Æ p(WòÝÃ$Ð/\x0002\x001d¬¨4­ñÎw\x0001RIó\x001eë@3k°æ\x0010,y)ß½¼J"Íù6PðsôûWà\x0018à
a\x0003pM/¾ª³ö­÷.Ð\x0018\x0007Sç¬nÀÒ{q\x000bn|è¢\x0001#6¸Ì
ÿ\x000bk£·\x0004X­$Ø\v\x0006&Êù2â¬/¸àõeq\x0003rÌ\x0000O¿­'Ù\x001a\x001bìkMÜi"ÇÄ«-Éñ\x0018J¿­''\x00151ºûYÈ©\x001esß\x00089m@Ö.ý¶Å+ÚÂæ~ÍiÌ	Üo»ÊÑ¤ÈMì
¬òÔ­Ò 6_\x0011HÜÀm}¡\x0018&ÿõ^ýö	¯o\x0006+ÎÓo×\x000f_>'à×w¨ùóq\x0001­EÑbÚ:Pü\x001d¦\x0000\x000eøò ù~ùöM|}ê?/\x000e\x0011¢#T½ç?Ø½:9¼ywûi\x0001¥³¤\x001a\x0011CôYÑ\x0002,u tB\x000bûäâO×gOáO'\x000fE\x0006%¿@w~[\x0017©\x0013T2\x001fC Ñ\x0019@¥\x0004´Î§J\x0007©nTiN¼Í¤.«Py\x0017¹à\x0005Íñ\x0006¤&Ô¤&\x000c\x0006CÑÝ%4¦\x0004\x001c`GéI\x0013ÖAjmMjí\x0010)¬N]@EÞLêÖ\x0010t!uÍº¡!Eí\x0004Á¤N²Mî0j4ÍÖ7C¨*é#ò zZ§$þFÕ®G{l÷c-4Ù©À£ê"y\x0000<´Ô\x0006¨TrÌ¨J¡\x0006JÁÇN®©<\x0005Q½-»Ò£é@5-ª\x0019CõÂ ÉR¥[;°ZÁFÕÇ
\x000c´ªaµj\x0015­°:£Ë\x001e#l\x0003l¼\x000eu°:Û\x001eUCÖÊãYº[®>ûã"Xë\x0016¬Þ7¬Þ«¤0-°ÊÜÜ\x0019ÇÔ^ÒÖÛ5´ã\x001aÆ5(Iu®É¸ê¼^¥4|`9¿ÅzíÞC{+(MÞòzU\x0018»Í¬­+¬U¬>=èÝA\x0000w\x0003M\x0007Á«GøÛï~»¹_â©:-Ø_1àºH=+VÀ²JÊ©#ëÕõÅg\x0017¯Î.§\x0003#\x0005Ô6 v\x0004TiÊ\x0005P\x0012®\x0003PMÕ°\x0000j§´\x0003Ô4 f\x0008T³
@4C\x0003J3RäWcZQcZ1\x00198RüÄ\x000c$ãsjãw`\x0006Yc\x00069i<%¬¥^JÖ'§	Yeâ÷×\x0003ÚL{\x0018vÀñy}Z%\x0011¨g/EMÞO;8c3ïqhÞ­§·$\x0018PwJÔK\x0013Ç3L9SË9¥Ð5g\x0012ê\x0007uüL\x001b­ötæÃOðN¶÷\x001d¤²%c¤öTÑ\x001a5\x0002­T&¥gz ô¤zHmK:´HñvJ\x0014#n4r£UÞl0ûÓHÝ\x0010inv©S\x001d¾\x0008#yH'oü\x001d Ê7 Ê\x0006Ó\x0002aD\x0003ÅÓà¾Ï\x0001ïö5q\x0014T·«T\x000f­R¸ïç\x000ch1\x000bT±_ªüd¸´=@åÐ	
\x0010¾F[NÐÁ\x000b??Ô¨0éAwÚÆyÂ\x001fGH=;%+ Ô*>Âd\x0008­Ôµ³ïFf?É:Òì;]L3i`k\x001a7ðó¤kw¾\x001bÙù\x0018eòSÒ!\x0006&øåK5.£ ¾]¦~h*Q&ß,÷¤Oüè6\x0018Rß\x000e©\x001f\x001aRM}¶Tçô_ ->T\x000c\x001bO¡]¥ahb\x0014:º7ÁéIYdVÉøI\x000fihIÃÐ\x001a6ûºÂãîæÞn`öck¢â\x0002\x0007Zð&íï\x0014\x0010¤\\x0001Cª6üØ¤qä$õ:R¶#%³\x001dqL9$©Ådì|9©j]S5äz|8¡\x0003*Bóf_Ë
\SÕºQjÈòÖSZ&©£±SÉ¤bêÁ¯4¶¤qèâçêÍí¾àu\x001a'T;HU;ûjhöÁÝ§\x0018¯Ã>\x0014àãBcLÌZï*eZÒ¡½ïX\x0003Ö©ÊJNHÊO'ºQ\x001d%5Í-\x001f\x001c 
&Mù.ÂYºB¡|Ò\x0006¤¶%\x001d:õC¹"©¦×\x0008KO»\x001b¶\x0001\x001e5\x0014áÁ1uÖ©ÏY£iLTM\x0006Í{HÛ½oö~ü¼ëÀû£ä\x001bQ^¢õ\x0006·RåU\x0003ÊYZ] ØõÌI|Ç\x0019+p}öeò7Øú¾5R~ÄH\x0005\x0011N
Sî#\x0007¤Qó2[vLÃÐ\x001bíÔàÓI3çä3t\x0007glMT\x001c1Q¨\x0017miãë4¸3P0ç}\x0003ÒvDãèò\x0001¥5ÝJñµW©Ý ¸«EC?\x000ejÃoeø\x0010áè]O\x00056QRó0ilIGLT@}\x001aS#s%?jFê
^\x001f´lT\x000e
©1\x0014×w0¸üòdTY¥\x001b¸ûºuøôÃ\x0017\x000c«êÂZ~\x0006\x001fGÔ©
æ¾u£ô\x001b\x0015¬¥X$nüüTâ¥
ºlü
æ^7&*\x0015â\x000fz\x000eòàs\x0004\x000f©ãØvný
Jæ®?\x000ezÉhg
§!ÊòH®.b£¤¶¹Aá\x0003¤pm"\x000beIªÕ{%$ÛR·A,R·\x0011>=\x0014áCÐ¬\x00121]ÒÛ\x0015§sh¿ÅÜ·q3=\x00147Cå`Ï TÏ
 \Õ\x0008¤[\x0018ý6v¢b'¨Ó+xú¬ræSe\x0006êõ¾¾i ÌÐ\x0013TsÞ\x0012)¦sePçxãG¹ÞD\x0019iZÐ¡!5ªø&NæçG¯|9ðýú©7í%ß\x000c]ò\x0013'#Hñ,Æ\x0012X'1­Ñ7CF?\x001aÃSm~x\x0006\x000eñ\x0018¹ä\x001cÍÆ7|ú¨îø7\x0003×<o·\x0007×\x0013MÁ(S\x0002|Màønª^uYdªó\x0011R|S´0Ê¢¼#=Ê¯ôT(¬w§\x0014¶¢Cê
gäæ\x000bü÷§÷ËÒd¥$éh°;7en¤Ó/ûWg×ÏÎÏÞÂ¿~v=wDÄ¾!öÃÄJq¸ß\x0008O\x000bÂ\x0005ÎVLùª½ÄÕc\x001f\x0010ó[ß\x0008± \x000eÞQ\x0007Ã1êÀÍ\x0016,\\x0008¦N^ä*\x0019\x00119\x0017q\x0000Ù°*t\x0004ëÊ\x000fjÁY²dRMÞ\x0008z}³ýøJÆQÎWmíb\x0016N£Ì\x000bCNfüö"X#8¬%]»àÅß¡x
)¥r\x001bâØ\x000cr\5ÈtÿBdJ±\x0008£\x0004rú­­\x001b¹\x0019ä¸b\x0005_Â5\Â5-e£i÷x¸¬¦\x001fYJQ#K)Æ­²§\x001ehà£YÎ·R\x000f(Âdà \x001bÙ·È+Ì2+PGT²j\x0019,3oe¥nY\x000f³°§ª ;Z\x0019ÓpDØjÿIÓ,füqxe4\x0017'\x0016¼\x0001%\x000f³Ùje´§\qü	Å\x0004*
\x001acÎÉ\x0012fò5©\x0017¸=HäøIdiòRV^QÐÖùÈo BM¦æu3·ÛÏo?|¬¡Aöë`\x0001Óý8^·a®r6s6FuY\x0018p­ó¼ÿ,¯
5éÚw39¯
KaÙ\x001aÚHk#8:\x0000\x0005\x0016ímÃ\x001cÛµ\x0011×\x001f!\x0014j¬\x0018ZÏÇy+Ë¬Ú\x0003P\x001fËAÎÂ~ÙÌyO5Q¨e6u?íe6-³\x0019g*]L\x0014v£ËËÙ;ÇÌå\x001bÝÈºE\x001eÞ6«- ²\x000c´}áµ5½À¡\x001dã0>ÆÖóºNnó®R&j¹þ*%jü\x0007µhÜ¯·\x001fî>¢tÐçEÞ§/	´`¢\x0003LXNK5u¨Iïêâ\x0005ê\x0007M©oíp«j\x0019LÙ°¼Æ:>G¼\x0004Ç9ßI`7Î(3#¯Ð\x0005ì\x001b`?:À0ª\x0007XJC\x0007_	·Ìjpô\x0000W\x000e\x0011\x0000[3:Â\x001f¼$!9\x0018`m\x000c\x000f°¬¡íã

o\x0018æÜd3zÅ%t`ÔHþÈéWÌ>`Y=\x0010b¿\x0016~ ì&¶¨\x0001MÁÍ]6°\x0017×°\x000b\x001b\x0011«ÆFàÄpGÍí}£·\x000bê`\x00032±|Ýè$®âHÌÃ~bc8\x0001ÃïF¹¬¾Ä´\x000c\x0016[mCÜ®
=¼*\x000c·*ÞËSZ\x0014\x0003Þ~N6¦·ÊlK=äðp(GØQ\x000b¬	\x0012£\x0005âiý>b'\x001ab'F]À·ÎDl¨\x0007\x0011:@íäáÜG¬D³ñÇÑÃÃñK¦\x0008d1!ÿúMe³*ðÇqâ@\x0002\x001cp}tg¯Ådý@'qkÛÔ°mÃÂ[J*KyÏ\x000e¼	¡&o¦Äº\x001dc=<Æ(\x0003ÍcÌ9.hÇ\x000crZã¦Ø¸Rê$\x0006Û&u!\x000e´\x001d¿Z¹Ñ:öªÙyøã\x0018±\x00124Æ(\x001fÉ\x001a+Ëqdðè·\x0001(YX½ìcQÚÇtÛ8Tî¢:©í¥Å\x001cË©7ùlº\x0018[e\x0001¤M%_¤I¸òùíã»Ï7¿,zé\x0005+AÇ\x0008vtö©k]Þ~Ó¥QI¾òùùõÕÅ³\x001fæ$3²jÕ:dºä§\x0006·º=d7Ü\x0006¹ºH£\x001eG»\x0012\x0005ìÑ«ÏÕ©ù&{õjZn¦\x000bÙù\x001aÙù\x0015£,¨\x0011ctQè\x00142gS\x00191}ÓëCöÍ(û\x0015£iÚ}Fp\x0011ò§hÌ´\x0012]\x0017²r
²r+\x0015÷¦X¤\x0018)ËÆDv<µX½Eú­J\x0004\x0005gQV9Ï~ÿmYx%8K½íct²È¥x¾ë93}9ýõÕÈJúÍ4 f\x000c4P\x001d®	æ\x000c\÷ãÔä3H\x0007g	\x0008ÖpÂM#[2L\x000bX\x001bØ#vb2ÙÃé\x001bN?ÄYòj£âbO¸kÐ"uRÍÉ¥-ä¬ò\x0000ÓÛ!ÎÈyKh¿
'{fÓo¹\x001dU´\x00128\x0018âä\x001enY'2¿\x0003û7ÖO \x0016J!\x001d/ä\x0008iÐ\x001cµ\x000eØ\x000bSS\x0006(o%ûiºtÏ6\x0019'{óR\x0014Õ©ç\x000cP¿¯\x0007U±5¢qhH\x001d[Ñ`È·\x0011Õ<¢fZçu9h%ã Ú\x000cª¢ä¥\x0003gÿÊX®
z2ýw\x0011iLtÕs=fBï¢\x000bo\x001e¾<~¥Å~\F±§e¼*ö,\x0007îËÌmòÍË·×\x000bTÙwìNÖìN®d÷¤ðå¨}Wÿ-íL|¤]5ìj\x001d»\x0017«Ø|)ËB¥»ÆwÃ\x0007WÃ\x0007·ràñÕ6û\x000bÆE*Ä\x0001¯×³\x0005¡ÛÁÇPÃWJãc#/
\x0007àÛi®:±yCê¢Y6R¬]7Ê`V^óÑ\x00070©6\x001cz)¡Ç\x001f×ÑkÉE¦\x0006%Ë\x000b\x0004¾×)9­Ë8@_\x0015\x001e!½2ké\x0003'\x000b¡ª\x001cÇ\x0017IKé\x0000¼n^¯\x001dzL¦'\x0013
»PL>-Û8@îÛa÷k\x001d\x0018)à©íNè¡h&aÇá-½Ê³§¿YÉï©\x000c|*\Ïê\x001f®þÜ\x0013åW\x001f0Q%PèßíÓ¿[Gê\x0015\x0016½£\x0007a8¹T¢gËNÐgÇ«ÖS\x000f¨§~ö÷Û_X©þ%*õ6ZÉw//J\x0019Näb1ìËz÷ìÇó\x0017oYþ³F#\x000c[k\x0015'Xà2Dkì)ÁªâÃ?¥9q0g²¶Ö\x0004\x0003¤	6:¸\x0014å
ó/`t9=\x0000ÛnÂëeÃ\x0002nC¼¨³EW\x0007KÏ;p\x0008)¾ä\x0018yÈd÷ãÆfåâc¸`\x001fT¹=fX+v\x0002Ë¬\UÕáÊÅ;þ\x0000¬K­I-ÁF\x00122ôºgM4ó\x0019à-ïØà:!\x000ck\x0005Ï¹¾Ø´ðºMÖ®Ò{aÌ48"l,\x000cmN=­XzCø*'ý¼¶åµ£¼;ÑÝ\x0010Y;ªäa±ù&¦LùÆác¸`\x0010¬¢`¢aÛ`\x0014\x000bHÁø\x001f:{xmÎÌÚ
/É®\x000bé«û¿Ü>>|\Bk\x0005÷^\x0001Dg1\8\x0007WëcøÕåË\x0017?_¿j×½­Ôm\x000161Ø\x0008÷ªÄ
s2·¤îpÚÖ£Öå!ÖîÊC:Y¥$ï\x000cÛÄx.2µòB\\x0012­Ù¶:!6Æ!Z%d\x000e/Â2\x0000>KHzgèæ\x0001ðÇbZ%BM?\x000em\x0014ùÂ¶­Ó\x0017;¸Å:hú©mocTÝ\x00103b½¹[\x0010¼sØÔ3=ì\x001aì\x001eÍ%¼ÆñÅ\x001a%\x001c¦\x001f0\x001böùÙÅlênB­än\x0001Uù1T[P½æ\x001b)é	ÞÌt\x000cXêQuc£
+@\x0013i<ÍÀ\x0002jgº\x001b-\x0007õÍú¡1"kIbK®Hõ\x001eÇ¾\x0010î!­\x0004\x0011t×5¦TQ\x000cÅ`}j1XKSÐ\x0003[*E?\x000e²r'BiOsN¼Çf¹Ä\x001afú\x0006-gÍ\x0002(UwK5Ð\x0004°êÒ	\x000fî¼4®aº®£µêÅ¬»^,]ãJ\x0018Ù\x0002HÚ(iX\x0003÷òq:o¦\x0003Õµ¨n\x0010Õá1Å­\x0011-¡òu<Ì¤«-G­³ëÐ¬ª!T<\iPÁ\x0013 <\x0019g¸¶.÷^TÝU¥ìª\x00126çô\x0018¼Îq3\x001eg85øÛå¬u%°8ÆJOLÀ
®«ò<®u¦ÉÑrÖ*í\x0016Y\x0018bEnC¬6+2SÁÏew-GmÀØÑ]^)å\x000fþ¦SC®`0¼³üt¥FÅ:\x0011Ë ¾\x0005õ îÔÑZ\x0005fÚVûð°dHg1C;õalêÁCÙþÃBg\x001d<çyKE1©Ø×1÷ºò¬Qþ¿xÖ[ð\x0015Ü\x0015Í¦JñÜ;·\x0005«lÆUË±qµ"¿·\x0019\ø§6ï)ÏîJyòYZë
a\x0006Ã®s\ß°¡h\x0008($àÊZiÿA\x001f0T\x0019æI¨2\x000eoN.o~_\x0016Õ\x000cü\x0019­æ·\x001c-\x0003ça6øt\x0012Ü\x0019üç¯³I{æ§¶\x000c\x00062}¤¨È¤Ü4Ô«ÒI\x0000NÙ_JªdCªä\x0008éN#:E5C^6\x0012ÎLJvVÕ7HºëoÚC
\x0007¾§1ºäó]\x0016ÜS½´¾AÒ]\x001f¾\x000eÒ\x0010\x0003G\1\x0010Omøà\x001fà¼B3]Õ´T©fC)5²£°¹¡¡ÌB/Kdå>gg\x0016ÚfL\x001d\x001aS0ýÔ;*bÈôÄ\x0003ËÌ%ge5©ov\x0014þØO
\x0013Ó 3©c\x001fUØ²NçRáÖÂ²xe\x0013#;*õg Ù\x000få\x0015\x000ev+çkº<ÝÅ¤¦±§ÚØS/\x001cçòÇPji¢å|-ç'[ÈtºÔ:À£\x001aÌ\x0018EIõ(\x0015nÖ=]J\x001auªÃÈ:up²åÇ÷ynÈe
é\x0006³oDCjÄ\x0010©	,Þ\x0007\x0006\x0015[äd½²÷§U;;HÛÓÔ\x000c¦(_d4rS¦Pd\x0006Ý:#\x0015#zRUÙ"J%íe|9y\x0005ß¢§\x0015I\x0015ä!\x001aÎ6%F\x0005÷þ£é\x0019oO^ûw\x0014¸\x001aY\x0000VûéåNÏ
cI\x0006Ý*µko»\x0011±nõ8±°Ü\x0005#5 Ï:UWÒ \x001fÏ"Yì\x001aä¯rL/\x000bØaTà\x000c¶\x0000E\x0011ÒºÜìÔÎUd÷\x0011«x?C°Ø\x001aCËÂF`F]:	O_µ{u¬ÿü\=\x0012\x0000±÷zâºÙ$\x0010fýÈÊ	.$\x000fV*ª=3ò´hØ>óT\x0018&Ýl«6$°\x000cm\x001d,üòxûËÇß\nába¬Â%}Z­¹ [»ù'£·×ç?¼øë\¸ Ýnªt(@--\x0012»XáàPÌ:V´Ý´(}äldk!jý``ö\x001e\x000c£\x001aÍ:[`jË!'w}½æ[\x000bY«ÒDdõz\x0015û\x0010\x0011+bÓ¸\x0016}jå&[åu±úÕ°J\x0014
 VUSM,-\x001dít:v\x000fkhYÃÐ¸ú\f±\x0002«u¥«ã&+ ©\x000f§UPêÃ;EÑ"ÂÂ?EÀºôËìI´\x00109$7²²\x0005á	lÙW7>Ýü,íÕÃû»\x0005©\x000e\x0016SMéì5Nc¼;_ÌT©*8h·^½~}öC²³W/ß^^Ìæ:$ZÙÐÊA\\x0017=åE\x001aÔ%ZÍ\x0012v2\x001e¬¢í§­ü\x0004¼\x000eèÁÁUEJzZ¹æe\x0002¤;X§ÜE%©ªç\x000e[U¨âÅçêæñþî_Z\x0006Ê!o­%Éúz\x0013¸d-ú¹7\®Î®//ÎgsË2qU¾IÚ~Xñ²ÖTEX\x0006&«ªî\x0000®T´L¥¢Õ
,\x00155[ÈCì8\x000bÂÇ2Ä\x0000×^±\x00176@l³¢/\x0012{~\x0007±ØÂ!\x0013\x00075'^¬1Þ½ô#s*="\x000bl\x0016½cd?­UÖìEìÅ028\x000f!?6j°\x001aÔsÍ)¶lÑëù`NÇÖkOº´ýª®\x0013\x001cßñ/c\x001déí	l_\x0019ëùØÎ\x0002ðÜtSçÀD6«ãõû»ÛÇ»E\x0016#\x0006´èX°ãÃÏ%vîl\x0006Ü×Ï\x0000öb\x0001­khÝ\x0018­\x0014\x001cã©ÂûV¨\x00124l"ÓIë\x001bZ?JkJ\x00173Õ9ZÂ £¯\x0011Kqëk¼yÒÆy;peMXg¤íd.\x001e\x000bqë\x0017ÉøÕd\x0007¯Ù©\x001e8ÉN»uì´§
x²5/þ8Ä«TiÔ\x00151"\x001fÎÎç^u°¥W¤åP\x001d\x001c\x0002xkËÏ·7_¸j®\x0019cÆ28øÏ\x001fìç
Ê=?{s~öö(¨	5¨	# »R\x001bìq/¸3+§{¨0/\x001cº\x000cÔ7 ~\x00044HY®ÃÎcb\x0002®t\x0017ÉZ\x0006\x001a©\x000f#SÍ9õîºF>$xLåº¶ÅF[F;\x0002é4õAóÔKÅ÷	-¦\x0013=\x0016Ê*#E`R\x001e!µ	bóèH7KGgGwV\x0011&QG:H°ºÄÂ¼'!wo47RPq^ru!©iI)\x0017%àìs\x0005½WÂ°Ý¤L~\x0007©oÇÔ\x000f©øØK
åð/©ïá®3«ÎF\NZËó\x0000i\x0010#¤pB	ê('%=¡zeXæZëi¹Å¤uQ
\x001eObÄF£KãC\x0019¹\x0018[,?­çÅ¶;Jì(¸\x000fÊÒø\x0010¯ää¥K#ÑéÎ\HÃ¾,{ØÉ²'\x0007åúáËÝýý\x001fÿ±è½W+~b°p¡ðW0\\x0014eæ2ÒÁE¹~ùöâòò|ÎG!àP\x0003qàFcK\x001f<\x0000¶l¯Ì\ð¾\x0007¸*N
¶.Nê%¦ìô¬|\x001fIù\x001e;\x0019x>¦´\x0018¸R\x000fü\x0000°à*\x0013cQQ-½j>âf/&vÍ\x0010»á!ÆW\x001cÊ¯À\x000cìKÁ­:\x0016;(À\x0013Ïda_	8Ø¦V¡\x0013× À\x00182Eý{+Z\x001fÉ[Y:¾õ=&\x0011ÛqbÏêØEÅ3réä;Ó¿¡\x000fÙ4KBá5aLÕÏÙp÷"­GéAr®Ø®\x0007Ù¶£lGY\x0007Ë½Ã°ÿx~èq¶ê=?\x001f\x001b]Lì\x001b[¬ü°56Ú\x0015ÿ\x0001\x0016µÊÆ
îhìiM¦.äZp9ÔËÝÈ
¼\x0007*\x0017ÃÚì¼UQ2ò3\x001eÏ2âw\x0014g,cOShôÉË»Û/'ßÝ}>¹¿=ùþæË?N^}¹û¼$½\x001dEÒbò(Ç°RZ\x0017A½0Ö\x001fÜ|\x0017çoO¾»x\x0003tòýÙÛ¿¼z{ñf:Í½`«\x001a[­ÂÖínä[xÌ#nwÐ
\x001eåÖ5·^ÅM¢ª\x00013aóÝ-$ÙN\x001aî	åcØ26Øøã
p\x000cEçuB¹æiÀ%\x001dÜÆñ¦NrFkÖwÒJ£t­ÔÊèþäé
ìÇ»ÛÇ%Þuì.Ã\x0015\x000e(·\x00118ÉE¹É
Z\x0019]<=
yq~}XÕÄj\x0018N\x0016Ê·*NUbÕt*Q7±®õ0±ô,n
l,\x0016v\x00139`ÖMljb3>Æûª`\x0003\x0010îbë8¯_¹ÉºînbW\x0013»abì¯J\x0014kJ«`ÃÝ\x0012TP­ãP\x0013ab%èmÅzE\x0015.èù\x0010'ÓuzwõhÉTñu\DÄ-*âswGÞyZÙvx];ï§Û½÷óð0K~µÀ¸\x0015·w,®´ÜnaèÞ·Ðï×@\x0002Íw@Í";GúËu\x0019åY3\x0003g»lø\x0012<'«ÉØq~×ó»ÿ\x0016ã¦¾ùó/\x000eÙ.\x000e9¾8°µ/ÖEÀ<×8Û°´oEß´+zx ÿóV´lW´\x001c_ÑFNøH\x0001:§ÊûØÐtüÜ\x000eô°6¾¬hÅ9>èÒq¥
´jGZ­\x0018éÿÄÕqÓ®á\x0015ýàíÃµ~PÅ¯ûùöäòf\x0016¥fË)¬ÚÏI¬¾ÔÀÎçrÌÊ_©}M)ÕhJ-E4%Ð°y*Jx%1yx,E¬rP{Ót#ZÃõ\x0006¿÷k´¸µ5vl_IX
á4ËþA¹ÒÝàÚ©$>U*çKó\x0013Ê*OY¡÷k»\x0011uÌE\x0000¨\x001c%I/ß\x001bÉ²í^ÏGÙ0º±»\x0018\x001f
P1ÌîT\x00199çÛi9¾¶e´ý0U­TyëE,,Lw[[È\x0018Õ(Cÿr\x0012+'²B¡V¾"Ê!Ï\x0013N<a\x0010nñt?@AÓ,¶å00áyî<\x0013\x000eo.\x0006I,ÍÞ{æ¸¬C©\x0004¹\x001f0Ç\¾ìCX¹\x000ehl¢\x0012ýFQS}Öâú\x0008ÉoA\x001d\x0014îaÔªaÔjd\x001cIü\x0007ö\x0007g^\x001aÉåÁÌ?-btÍ~®Õ\x00163Ê"û¢\x001c§9\x001bÁ^[\x0008óï~\x000b\x0018cË\x0018\x0007\x0018\x0015Ki?ÆbË¦´4+gZËP\x0013â\x0003£H
µ*ZaÑ(rÑÃ¬*å"ÆÖrë\x0001Ë
N¹§$ki§#Xä\x0013<´ñ]-}QUâÚþl²«¿øøùîãíçÏ²Teä`«1ª\x000b­â
p$?áû/Þ\¼8ófVP9!Wtx¹qdZèrS\x001b®Kw®\x0014êÌ't0×ÕþÕ+
g®\x0018ëD¥ãHÆ¹ÓNèÐ@qhðØ)É'G2üXÉËÐv>#x\x0011tÐ?µIÁpÎïI>\?|ÛÚÎXÖ\x0004.7\x0013Ì±Y8¯\x0002døéúåk¸¨Í)keRÝêAR-Ú\x0019¾XÂ]GVÎIîP§\x0012@ôÞ~CN7Ä=Û3(\x0016ØðV°}P3'Âò!­V, îVl\x0017ª7lÈ4Pf
ö^ç!qS£V¥pX\x0000äÇP%·jÑAR¥< \x0016««ftK£úfTýØ¨\x0006®hÑÆu\x0005Y\x0014Ýi\x000b°T
Qâ#¨Ô
\x0015\\x0013à\x0007YÃLýB\x0007«lYå\x0018kÉcÖ:PZ\x001cu\x0014a¦ö|1ª\x0012ÍZÅ\x001f\x0007M\x0000ÝèXi¡h5-V½\x000eÕÚl@'ªlÀO'¯\x001e>|XêUyêÆ\x000e2¥ï\x0017ç\»¬[øéÕË««E°h\x001dÀî4ë:aCÑÃÖ|\x000cËI÷NÎ¨ÖuÀV×\x0000[÷Eí5Ü\x00031`ÛiG°,ù2\x0019o^\x001ae
ßU
5²j1|òúæÃÃO({xÇ>ÃJX*cÑ%EÜÌÕ¾>»zùöõë¹b~"5
©\x0019#üôà¬8-%Låàæ\x0004ÖÖ]xTÉ!ÔÔÄ«à¾@³/¸%UsåQëªF@­Ê\x001a{Pm(q±ñ8%0ÒlXÏ¤\x0016£VÂZ	\x0017ö »êwM|iS\x0005ÏL`¯fÊE²jÑ°j1Æªc.xÎ\x0006Ó/\x001cú,
Ø¯aÕvÏ\x0002hÛ4\x0019¿¼»¿Yb©PfvÆf ô6\x0016yPµU\x0017gs*cV\x0005­¹+híÁlPµ\x0011,\x0011¢wìXÍ\x0004w\x0017bÖ¢\x0002º\x0011\x0015XÎ	¦ÅQÐUÍ½Ðë\x0006²3]\x0005\x0017sV>5rÖNõbN\x001dY	Ð(AzY\x000eÝ\x0000	Ì:8UuGÕ nú9±zÑ\x0002\x0016*¿²ôU=Ü)®\x000f³\x0002"ftýQ\x0015¡Z#li\x0018h9gB\x0019åïã&\x001d¢Ui\x0014P¨<«Ç?þãý¯7_þ±dH}à¤\x0014'ÃiiÚÎSI®s\x0012õêìúüÙó³·9«\x001a\5k¸«±CÁ\x0019jß\x001d¸^\x0005îYkyE\x000e\x0011V%¬þI½ù=üëÛûÛ%Yº(HÍ"\x0001°éÙ§\x000e¨C\x0011Â\x0019\x0019è×'Ï^þóÛóËó¹\x0004]Â­\x0001WùA\]\x0016ÑªäsX6ÿÒë¹»\x001c·Z¼(*Fq=×\x0019m©;à\x001aÅ¸ó½Üã6£«G×rà5 Òf¦åÇgé&³úh¬i\x001c¤Ul­Q»Ô\x001eS¢,NÏy\x0002KhK+·2\x000cîÚUa^Ý~ù¸,Ñ\x0004ö\x0013_²1ßÞ\x0001¥7¥®y®=ÜÕùÛ\x0017ó9&\x0019´ªk\x0006Ðª¬¹\x00034\x0008VÛN T}\x001fyP\x0001t¦¬y)¨\x000b5¨\x000b\x0003 XR`v TÔ¬ÃN%`¦\x0000w!gÝ<\x001b8ëæÙ\x001d Nå§K\x0004Õ§úÇ¢M¦^V>\x0001\x0016 Ô	ìaH\x0014#¬\x001eûEQöÑ\x0003^\x0008Úô×qU.Pì\W*\x001eXÐÉRñ0]¶\x001cÔ7s¯üÀÜ')]\x0016	îTQ6Oð¥<xN\x0014ú8©L\x0011 ªøZ¶øúÙãÃÝ?ð¯>,i]¥©å&TS\x0003J @N×9ä\x0007¡g×//þýôål\x000f\x000c^Ý\x000b\x0000¼ë%G¹D[\x000eZ*Vt\l\x0004\x0007í\Ë¥nò(kò(W["ËÙ\x0003ÔÇÙXt	Ã¤f/ºª_\x000faµ´ÏÝìX´A\x000bFê\x001cãrvw°s1®\x000et³¿ÐÍÞB¿º¹[¤((c-)î/æJ\x001cÑðº:»\x0017A"ÖP³1V¸B*Z\x0019Ö\x0000\x0012*¿ÏÎ5\x0013]ÎZ+ý'ûB\x000baaÁr#dXÑT¤Ï\x001dÒeÏ!ZJZ_)EåwJöqÀþã|ä^R2Ì¼#wÀÖêÐâ±c°¡¨C\x001bðÎ#½z±@¥<®¸ÕÊÕÊ1V_bsx9#q	pË
ì\x00115¿°®Ù[nlsYl~é\x000b,E¾¼áZ\x0017¸I\x001eSJ\8²»lu\x001aÛ±ÁU»¯ _ÂyÇéÕÒËy[{W\x0014\x0006©\x000biåêjöæñ\x000eîf?ß.»IÚ8-%þe¾QTA¸iÇ\x0007~zs}\x0001³7oÎgë~\x0013®U5®UÃ¼\x0005çá2kìH'Yz\x0014Ü\x0004Ø5ãë\x0007ØsLá\x000b.Çm¸(½\x000eo\x0002\x001c\x001bà¸
8ûÂ
+¶è0st¡æçÜu}9°Ü[Áb8¾cJ\x0005®ú,3\x0002Äqî¹y	1Á5{\x000ek¬÷ÕýÍû,ôtóÛÝç»·'Ï¿|øp{¿ÈÃÑ»^$\x001dM,mà\x0010Y8x{uyö,k>½ºxsvñâüäùÛ««óË92eLTîÔPðw·`Ü\x001eovÀÃeeD\x0016;²ê%e-G²\x001c;ð¾;¿¾FõÚ$\x001eðòíìÝ)±\x0007Õ°\x0007µ\x001dÅõH~$p@*ê\x0012ùkQÚAî³ Ô®MG©r=}\x0005Ì¨Óðì×ÛÖ9¾Tð[@ÀäÛtuâÊ"i§{:¼=y\x0005Ä(ÒðìùùÙ¡«P·u(­\x001bÚDÍë\x0004¸9ní,wÙf®\x0015P'¶iÆÚ¬\x0018kã;§MÅÎ÷TÎaÓ5RÝÔ¾\x0019l¿f°.®(\x001aZïrïfÚÕ,ÆÎå}L\x0014\x0016$î¤9Â.|¼í(í#ï.bFJÃp¥æ$/Â\x0006¼>?R×gõÞ«\x0011
\x00004ÒW
Cýüæþ\x0016,ø¢WNj\x001eõµ<",\x0015®G<úü
a´]\x0001\x0007Ö#\x0005ãx]?Es?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹
ÿãø¿½\x001f\x001f+\x0000Ã+\x000c;Î·\x0008: AK	GzIÖè¾,Ôê·øåöþæ¹ìW0_­mé$\x0017Ø<\x0002"ðâÃk#°F&,=îí+úY¹Ë\x0001\x001e2¶ãc5¼§ê@%!·\x001d{p*\x001azãö%ÕÂeûæDTç­ÿËÛ»%Ù\x001bY¢S	t\x0018Þp\x0018¿"TñÆÌº~ÊB¡\x0014o3I\x0019\x001f²®ûUÓ¨\x0011ÜÖFÎ¤Frá;öÆa\x0003`\x0003q»L,\x001dfI½\x001cÛáp8Ü×Ún\x0014_®þüðåïïû¹.2V
z\x0004YhÉ/(CpòæêÏ·o~¾;Kè´\x00034¶ÇÁº eÙ¡:0¤àØ·Ûé`?Ú4!fàÆý'hmó\x0010L®¦Ñ´h\x000c(¶yg\x0018^¥§àò3zëIk	ieJük?:öÃMäS««,4\x0016_ý¹\x001a¥\x0018­_¸¸XØR0±ÏD\x0010ô¢«ñC\x0016&Í\x0017Ö¡eÎ¦
Ç\x0017î9z%(ìÂ^\x0018\x0011\x001dKP\x0013p}Ùh\x0011®á®\x0015g\x0019n³.9\x0016%ý+`oY1\x0014T³\x000f¬µåDûÅ¹\x001f-\x001ef**`ñÀmk\x001bø<\x0014WhÞcûáâC3p­¤!Û¸¸x;±1Ýv_QFà\x000có\x0004\E\x0005¼ºü¿[ÝQ\x000cïÎÌÀu²\x000bTæU¾D±v{X?ÜÓáÓ\x0003p==+çÆÓ Û}µÝ»Û\x000f\x0017ÇÇ`*\x0001³z§\x0003XRÉÈnaì¼àØ8\\x0016¶>\x000e78Mp
G]pW·£æ?\x0000×bñÔê\x001a\x0016E²ñ>-È\x0019lq¾\x000bO¤J\x0018\x0004OmÆÕØfLmºö3P?ÞÔY,§7\x0004*îk\x001b·§HæKsa\x0018/ò\x0006¥?¯o¼@L!¶ÉX¢3P7^o:?Çñ\x001aESbÉ\x001f(;\x000fª¬¯iV±úñªô(è'îj^	Çä»È·Õ\x0014ÊSH}^\x0014e\x0018¯Ækpúc\x0002/÷ÔE¼ÄR¤*e\x0013u}w\x001c.È§?Ã{LºrVøÌª \x0004«Tó¬úãp\x0001ï\x00130q¡ð8Øè·hçæAIUvÛºÍfp^Þ\x0019¸HV¦(q\x0010\x0005¶\x00140\x0007¤\x000bÓ2ã\x0011¯ÂëbpÈwa\x0013<qkÅÌ89Z×b\x00011ýq\x0018o¢1Íî`bÒ£\x0008/P¦cCÐë\x000e\x000bÏ\x001eÖÎ¬¯1ó^\x0003|	\x0002£rójÄ»0ÓqXsr3'\x0001L\x0012\ï9ö&vÛf"èÇ\x0017 7s\x000bòÖðdnÂëÙ\x0008ÅxÛ\x001c1ýx3\x000fÜûâ3Ù7{¯µ$­p\x0017.o¢@w3©¤Ì@Ñ\x0001\x0004©!Þâ½ívñ~¼øîåü\x0014^§i\x001cWoc¢ñ\x001aä\x0006Ýûux\x0011Ñ\x0013/¦¶[¼\x0008\x0011Ë±)AàD0à\x000f\x001eûá¼I}]Ìwµ.ÑLæÃØ)_ÂX\x0017}=\x0006^?\x0015}âFë7\x0010^C\x000f¸ñb\x0013wSxcxPáôts¾ÐøC{Lj\x0000/¾OÅ\x0007ìmb¸Ìå\x0000Xø+áa¡ûbdðSá\x0001\x0002_\x0000jÛ\x0003¼03ÞöÔm?^|eO\x001cÇ\x000b[8\x000b\x0002Y#\x001dXø®\x0018aªòàb8£'A\x0013"tMÑºàmórõãÅ­\x0000SáÌDôñ:\x000egÛêu©/V_ÀTÝÁKÃÁ×
Eî\x0011­+ò)í\x0006Î~¼øß\x0005S¹\x0019²-\x0019Kx
s	xRðKx×\x0015%\x0001ßoÁN­¯14Âäih³\x0005Ã©dXX¡\x0006,ÁI%½	¥L"<Î¸#^\x0010åf\x0011üº³\x0002ð©³"&\x000f4]ú\x0005(7\x0003I¹äºÀ\x0010ð\x0006\x0014¦®A\x001eG
,T\x0014oÅ\1\x0013\x000b]!`\x000bRS®\x0010\x0017¿´á5--÷6ÈÅÿ¯ÃaæØCüúËéÆ9Á 	å~¸XÌ	S\x0015xÄ\sõÔÑ\x0010\x00003£&ï:´\x0018oÃTÐ\x0005m¹\x000b\x001f®èFjÉ¥eq\x001d\ÌuÃTÂÔ¥És£±1\x0008ÊºR<]ÙÜÀJUö¦\x0001SJkfq\x0013òûk6*\x000e\x0005³\x000c\x001a\x0003Ú\x000cj\x000f1Ù!6wT¢ä\x0017hÛÙÐî
m¢þ_î»¿'\x0001\x0008~}ýíáêæã×O\x001fßD­/_ûÅt|HÝ#\x0011®Õµ 8º
y|\x0016:÷ÝíÕÍË·¯^Þ½DÉ7oÏÊêì\x0010S;Ü\x000cbCÍØÒ,ÄS4KâåùüÞ;E6&\x00179Ï1Y½\x0011º\x0007/\x000bä\x000b9Ä\x0011ÈL)>\x0003Yä£9"vLW\x001c¼`Äê¼ÌF?â_äÿ¥þwR\A'Ã!â$ãùé÷¿Üx¿~¹úõ¿þã?oþú\x0019y¸±çùå§Ïý\x001a«\x0010w`²Â\x0008C\x0004h\x0005I±Äÿó©|´âé«\x0017?Ü¼øß¾¹ºùé5\x0012rã?~ùêõ9ÕbDõ´ôÇr<Uº­Ñå\x0003OSx¯ÎkÏÚd\x0012¡Ç#|&\x0014*ôÙ&g©
°Al²çe\x0015gmr:c½MÞÒ9`­\x0000Ö6
N³MáB\x0011dÒ¦¢\x001c¹Ú&ç?Ûä°dlÈ6] ´	\x0012Å#|'ë)C:\x0008&9\x000f\x0006}¢Í\x0017# )WÀ#Ø\x0004tQ±©ub¡\x0002QüN\x0017zì\x000eÙ\x0004áã_ÿúpzö<ÿã>Þþ5\x001eBýôåËûNü\x0014órU¼
R}6î\x0017n­QîÂðÕ;\x0014xõòæõñ\x0014úéÕ7wMÌH\x001eÿÂ/0\x001b\x001e½2ö{Ä|¡?á\x0008f\x0012ýÃì¹V\x0000ÚaûsÆLÊC\x0011óyA½#±@Ï®s<+hÄ
rWqÂl¸	þ\x0002\x000bå\x0011Ä¤\x00047Xóx\x001bR#@ºá×øÂëÈ\x0011ÌÜÿ<Ùñ¨\x0001b\x000e6c¶ør=8õYÄÀÒÌÃåÁ¤¸Êç¨`F\x0002÷YÏpÕÊÀ\x0008ÒK
8U\x0011óÒíW&g æÂ\x0007\x0018E\x0000ñR[ÂÜ\x0005ÅÀCÆñ$f¼~\x0011fË4\x0012Á\x0004V\x0016R'\x000f`öéÁz\x0016³çq\x0014,ÞdÏ`([ðÂÇ8æÝà\x0004h­4¾ä&\x0006¹x4\x001cèà\x0002Íç\x0001Ì(KþÂ\x001cWFÖPL(ß=uÔ+â´XéÏ»>Ó)Ì,©\x0002V9´ÏíøÏ/Þ\x0001GAãgKL\x000e\x0013¤â1Ù;Êà¨V\x0017\x0004\x000e`Nü~2@#§\x0005µa52_xs2ðB_P~8\x0000\x001aÙ\x001bÒ\x001fS\x000b
ø¶4\x000e8Ò:\x000bögu¡h\x001c²JBÉj2Ý0Ñ%I×a}ÚÐ:ó¤¶K×9-Aúc
´\x0016Ä8£q%ëí$A_¢\x0008;\x0002Z!h5»Òê½F @*\x0004:^²Î×§»Aÿ»\x0013¿IwR¡~þí÷\x000f\x001f¯~øôíC/I\x000f¨\x001fgå=\x0017\x001c@º ¢\x000e¹ðæhß=½»}yõÃ«wÏÏ\x0011´ì âúN@\x0015»2\x0010+\x0005eì·c¬\x0017(2G±\x0016ÉÎÃ`K\x0003ªCµj*ûBo¢/<`Åã®\x001cy\x0007À\x0002\x0000w"'½\x0013­ÙûôÀ(Ø$W\x0012&À"Ñ\x001a÷SêLÇw7ZYyíf\x0014,v5Ã\x000cØü®ÁJ\x001a¹ \@\x000bÔ}`ÿ×ß?/Mû\x000b{\x001b2Ö¾~~ø\x001f?ÞÿÞÔÅ\x000biÖ\x0017°*¨kzz\x0017ß#.µ
D /_½}}{õãÍ6Ì2÷~\x000c'jÓkzJ®©½\x0005¨½\x0005åÉ/F\x0001 x\x0014ðqp\x0000¨æMe·D\x0006\x000eØãÚpù?\x0002tWö9\x00024Ð1kbd ôBi/uç
\x0002ÝU{\x000e\x0000un\x0012\x0016K>ôÚÄ[\x0011¨¿¼óG\x0002Îû\x001c\x0006\x001a\x000fÕÜÒ\x0014?½"\x001dD_\ñ^Î¶\x0006î«$GVÔg\x000e®øå\x0001@Rß+êd_¼\x0003àD	Áã\x000bê\x0005ã´&A#NÏ8ý:Iï0NZUòÚÒih&
\x0017tÕßù\x0007ãGNäa\x0003jº3tâc¸¿÷\x0000Eá:3óå\x0003GQOÌñÓS\x001f\x0010î©U{\x001e»\x0018­	N9Ð&\x0012AÂ	\x0017ôò+×\x0000Î}õëª\x0012DãÚr÷­q%6]îG\x0019\x0001Êì\x0005"\x0003§/ï4ñÅ×¢\x0004§\x000bÄL@ã÷Ç7=X>è1#¡a\x0018:ùÓË\x000b³fc@ñU\x0011äñ½¤¸\x0015I@Â\x0000^v\x0010è*L\x0004q\x000c§°ôÒ%Å_Þo	Éªà\x0014°óïð^²Á\x0013¡B\Ð¢ßí\x0015?mÇÿü¢\x0014¯.\x001f\x001fAªK2Z¸	"R]6Ó\x0005¥1¤\x0006KlæðÉdQÎÏúÀg½ÚóY¿*wIÔÅ\x001c>b\x0000¢¹tØ\x0003\x001döbËòì\x001cÒ\x001fà¯\x000fÉM£¿\x0007Ê~~ÿðùóÃÕû÷_¾Üw7,hGµa#ãe$P'¸\x0002*G\"vP¾»}\x001d±¾¸¹{óæ¦6IXJ¾8\x001d\5:Ã\x0005QÒ\x0013Íe)wI{\x001co¡Ò8×
¢:x5\áÊ\x0013\x0017Xùáâ\x000b£ägÆcp±ÔGÞ´¼¥ó×ÉËÍ=x±Ì	\x0011Éö\x0017Oðç\x000f\x001f\x001er;ÎÍoßÿòíÃ×o»»#NzÓ'WL`\x0012vaB]]¸\x000bÜ<~ûo½¾{úîùÛÛw¯Ï5\x0001³\x0001ÆV\x0006àekÞ\x0000¡\x0001D8)d­?]ð	\x0002j\x000c\x0016\x000bXQÎ¸bÁÙ\x0003ú\x0005P[\x0000ó\x0016xC-#É\x0002j\x0018\x00165m?¯kuÄ\x0002dËÞYÈ³'-°ZÐ@É4ðØpòªºP\x000c9d\x0005ø¸3iA!¬6²åNätªél\x00068ýä\x0004ÿç_þöþëÃ/_\x001fúép\x001b§8äµ\x0004_yRF×½óoñ;ø¯þéîííÓ··-ô¦BofÑK	Ô}²¨ZøGXo\x001eÿ×Á
>Ì/>s<{¤Ýòeõ)\x0002ósx\x0007ÐËøwèñç,ü@ãB\x0011¾ât\y^|{~b÷\x0008üÚóå´ë£óä\x001b7\x0015\x000fh¢lô8\×\x0013zºáû\x001a¾Ï\x0005\x0010ñ~I2Z	J!¤:¸\x001fÀ¯$ìñãÏIüÊÔ\x0010H©>\x00154²eün©÷kå«Àosø\x0005\x000f\x0018Å£\x000b®9ôHÎÜù7ç#ðw	\x001cÂ?Ià\x000elÞ\x0000¬-¯t`¶\x0008Í©BXµ{
Uz·¿xr½}þúåêÙçû¿ÿ
ÛØûÙPU+Oç}\x0019\x000c¶È\x0017\x0000@
Ê\x001e\x0013Þ¾¹zöúæç?a\x0003ûY3¤ÊÔçÅø\x0017O*+ðIõþão\x000fý¹\x0003öPþ&&!¶Â­BÐÙ\x000bâf\x0000>«Þ¼|v{>u ì2ì±Ë0	\x001e	´\x0018¼%ÙLÔ¯àÏ\x0013\x0019\x001e\x0000¯ì\x001e¼²àÃÁ\x0003Q´tóÐ\x0013<»ÁëjåõÜÊ#CÊ5c\x000fL£¢ý|añ\x0000vS-¼[xÝDa;u1Èý<»è\x0001ìÖï±[?]cT!ìÌ|(Ç\x001f8ÜU«îfWÝ¤\x0004'#·\x001cìÚïÈ{Àc¿n\x0003ïàÏ\x001dú§÷ù0pÁòÆ;Ê\x0013B\RZÑ\x0000Üyâ
ûÓ\x001f_º]I
'\x000e\x0013ïmµÃ<½ÿü\x0019{è\x0006Ö]FyBÉ{ãHÛ æhT°\x000c©\x0016Øýõkì¢»´ðI÷\x000c'$¶¿H³\x0012;øï»ÿ0p¸Æ>ç\x0007¨4]Èæ\x000c³Û\x0007q¾\x001b~\x0007ýîÙÍó\x000bjmÃ\x001e¶
3°\x0001{Û -\x000f\x0015u¬¡ Âî9ú`;½íô\x0014ld5;\x001aXË£\x0007áÂÇ0jS¡6-	tày\K}\x0017\x0011ôùQ¶AÐ¨.¿\x0003?gPK\x00123ÖIÒ8kM´y.\x001eý=\x0001¥\x000b·¬\DÊ)\x001fñ*MÆÆ7qïZMíá¼¦ß(j]¯¶ZmïiØÃ ¿"\x001d=V3§È\x0005ÊÕaØ¾í'açF\x0008\x001b<m\x0007;\x0013\x001bÅmeÛÊ\x0019ÜÑ£uÆý[Dáb%½;ÆEZæ%¾^n?µÜÆ\x0012õ¦qédÌÄ¼è\x001c\x0019·î¹	uáF2å\x001dnü9[;z=5Î\x001bî0¬dåãAG\x0011©\x000f·ªÜ\x0004Îà\x0006W¸yp3®7\x0014úÌ\x0006¼\x0008w½Þjj½º¦å\x0006A2+\x00116%%\x0011öùïQØ\x0016*Ø\x0016fw¥'÷öüXf%ð¶ì)TtÁÖ¢J\x0001ñçqØV\x0004ê¯áPd
\x001bW\x0012liì*ï6õ®4s»\x0012\x0007f³ú XK\x0003³MQORçg,Fq×g¥;+\x001d\x000fìEÜ{#îÀ¸Ï7[âö®ÂíÝ\x0004n¡/ûI°pÏÊrÓrkÙs5î\x001dª«\x0002þ\x001d\x0004\x0013le-^w(xÇkÚ3\x001e,
8mñd\x0017ºQúé§¿|úükwÏ\x0012À3^J	xá\x0012çµ\x0019xüû«§¯^>}õúÇ³zÚ]í±«9ì\x0012\x0014kSÇg	»T=u]­Ã®÷Øõìº\x000b*\x0000!7?³ ÅDÉ\x0003L;K\x0019ÁnöØÍäºc÷)ù\x000cX\x001e8\x0012¡°KM:\x0002Ýî¡ÛY1ÌËî}à~t),)Í\x000bÛ\x0008v·Çî&±\x001bÇ#«>z>UÉ"6­{3¢@÷{è~\x0012º/²§>(â\x0016\x000052Ó?ßi{\x0000ûö¾"$ÌnUM\x0005\x0015|§æ¡¸UÿE,
3ºò\x0019=ë4ñ`"®æx¶ÒÈp\mMO¥ÛÏ\x0001ð¶Zy;¹òØG,ÿHÌzQ,Ü¨.Ì·\x001eÀî«³ÉO\x001fNY9½\x0017|{ªìVw^ùù\x0000x¨\x000e'<¤}¨¡¼Àì%þ|ÿþ\x0011èÃÃ¬ÃbÅDÕ9rxÉÆ/]öPùLõ\x0019g\x000b;Oiaë\x000e<ß/Î·¡ª
ñRÍ\x0006ùx¡¦¡i\x000få	:þËÒ¯\x0004o*OÞ\x0014xeY~ÊÓ\x0008mSdö©¥Ð]
}Öã#ô°mÖÀÍ§\x000e\x001eeÝC
>LÞ°\x000b\x001bh\x0013xVÀýº$ÆÇä(Å\x0007c¶\x0004Õ
ûöÃÃ/_?¿ÇöþW9Í¬e ¤@ªÊô*g³ðHÄ~^1r»öÝ>¿}úöõ\x001d\x000e¶½û\x0019ð«²úñ/¨êÊúìáÓïü¯»o­\x000eä¾/M¿¹cºÞ=~à×g·¯^Ü¾}}þÚJÐ·\x0013
¡×\x001dËãÐ3Ä5\x0018^K­¨ßE^ÐÌ\x0018ÁnSW%­Tß7ìw¿ÿýóûßG¡±\x0016k\x001cNâ\x0000?C¼aÁ¨öûÍÕÝ_ß½¸ô\x0010Mà·nA\x0004_7\x000b\x001e\x0000(Àû2¨§97\x001dÍ^ýàU\x0005^M®¢3xÜ®VÓ,\x0015QeÑçiw\x0015x7\x000b^P¿\x000bVexHÅ\x000b¯\x0019¼Y	\x001e*·Y·ÑÃ£Û\x0018î\x0001ðØÐAnÓÎ)\x0007À\x0007½\x0007\x001fô$x\x0015pä*WÜ_ê\x0019/boß^G°
»Å®\x001d\x0006/ªÜÙèã`Óó\x001aÖ½
a6PJ ö\x0000pRÂqA\x0016ïy9í\x0007\x001f*ðavá5½\x001c8¼[\x0006ïÙkdè¨À÷ßuä#øü#Kïé|u\x0012\x001b2\x001c=¢í¤r\x0000¼\x0014\x0015x)fÁK*®ºTg%ìì5=\x001cýÐM
}v»
ËÈ\x001bÐ³¤+NÓQä\x001b\x0001ïjð'	Lù\x0010Á»²_/]ê5¾FïgÞ\x0010CÃUzNp4À>ß3Ø^Õk¯¦×^Qe;®½&=lhä\x001d«z\x001eûÑ×k¯&×\x001eUú\x0004¹=¾Æã(Þ²É5×UR&³§À¥X'³¸M^zÒ*Æü`ab&µ­ÑÛYô@å\x0003'}¡sVsN,Îó\x000b\x001c@oj·7³nïY!ÍaÅNN\x0003Sva~³«~dô§,iEçµ×¬Êí)%®ýÊû´õ1k'YãSßL^{KUbÇ#3æÄÐ\x0011ìõµ³{Ö\x0019*Ü¤`O×Ø\x0018p<£·+#Õ5úÉ\x000b	ê\x0000¡\x001f\x0001\x0018}àÓñ$5ÞÕ~ãfý\x0006\x001bR(3ö{\x0014|\x0017ì\x001aµíG_¯½]{\x001b¨\x0011ßI$á¥#\x001dU\x001dEú\x0011ôuÄq³\x0011Ç
Ñkæhq\x0016@w5Ñö ÷é%v\x001dû''ÉñÇ¿~úüûý×ÁkÜ¸4e<S²T\sØ	Þ÷
ß½üéÕë\x00177o\x001bE×l\x0012{#X`u\x0011ÛèÄ&øÝ;d\x0002T&À\x0002\x0013¡£\x000bM a\x0014âLC\x000bz¢ç\x0005ûÍ?9IÙYPÔ\x001e£\x00058UKzz@#z¶Â\x0011¶2Â®0B±v´Ç&ehöÈ×\x0007±îKÐ\x001bÿ¶§ñ¿ìéy¸ÿxõüá×÷\x000fßzÑ\x000bìà"P§èÂè#hz2\x0014þ¼´\Fÿ/·7/¯ßþxwûî,ì j¾\x0008Ç¤ÜÃþøÅ¯>ÿÒ<5ðJtwu·\x0008©@ëå\x0007¿ËÏ
è^ï¡{=\x0007ÝÅ¸oXë\x0019½,¡µw\x0007
yE\x001ecN¦ÙIJL|Ç
²@oÔú¡KQAÇsØ5	'ìDã\x0016\x0003/Ø-;2\x0007ì±ËIgwJ¢`Æ.Iµ\x000b¯çììá<iw?vëBÝxfqvc\x001f"ûú·I\x0017§úq)\x000eßóhv!E1¡ã }þîí.
L\x0012ni÷¸¥\x0000S´t'Ç`È Ò\x0003\x000fÙÚ\x001eFNà¦\x0002næ+wm2nÔ\x0004¡¦§À<(Vv¨°·+\x0015Â®oTÃ°Q×\x001c\x0005$K\x0013Ù	\x0008lÏ¤	º\x0013K:i±¢J'_üñÏ¯#Àñ$K@`ë*\x000e7çh¹\x0000¡ã	ÿÅíÛ\x001eÜºÂ­çp³\x0006¦CærGeî`¸xà{¦o:q
·ÃÍ}þ.Q\\x0012n(?è!\x001dèÄí+Ü~
·ð45ä	Ì¯ä@puøÚ(nUáVS¸±ª-h½ãáOwmW^/ÈE\x000eÃ
6Ì-·¸öÜD\x001a×e[xÒ{»\x0018!îúb4¾Ü¬\x0001ý©Ìê\©¦^à¿\x001fÆ]\x0013=\x0015N\x000c:ª2
>×°\x001d×°{hL:aWÞ­ç¼\x001btéè05q-ïÛ=Õß>Ø[Ù\x001da×U÷aØ>ðc²æ<q%xgL\x001fÆ]-·[îJ)
&:`[|Æm¸jêz'ûpÛê·S¼ñôHÒaÉïKFr4é*Ttâ®\x000eK;uX\x001a¯èÚ\x0010q+¦,q<8¸;úÜ:qÛ
·ÅMoJ
g&\x001cãfÿv=D}¸]µÞnn½qe9,¹¬ÎÞí{º:QW«íæV;\x001e4|´"ò»xã,1PtÜÑú`ûjSú¹Mi®\x000céÈ¡n<'øý¨m¶\x0013¶¬`Ë9\x001f±üî¥´äò¹qÛ°\x000c7T	Ìe&¸Æ¾\x001cT1w¢¼\x0019u\x000cîuã®2\x0013ËL¬¤:¡S*.0Yz\x0003ìºØ
Õ\x0019\x000fsg<\x0006>ö\x0013àú¦
ºlËóú\x0008Ã¸C;Ìù'*Á¸ÞPü¸(q½×¥¡Â\x001d&q\x000bîUÊò<°
ìÞÖ¬-ÅIýa®\x0000!ÊAGÜÄ~è;ª­éa-é\x0004^_äÅÜa©\x0014
üD\x0007OÔjiÁ½)WO'p[\x0003;/5O½GO)cÀ6ÞÒØUÔ\x0002W	:yø\x0016Q~\x0012rDùã\x0004üýçOï\x0007¡Ãëä,¨\x0000HÁPñác\x0001z\x0012ð»×¯î.¢ÿõ»müÝ»íËOñ}í\x0004
"XL\x0001]²àñ*dQ£âw\x0004ÝÈ«^¾ÿëm\x0003ì6ÏæRÃáA°ñ"l	l\aO`Ý\x0006ö¼:Ø\x0000Øí`·[Â X\x0017r±Ø`ãY~U\x0008ÊUÄÚ\x001cèÂºeOuË\x0006±Z~î6Ò)êÔ
JñÓõ­Yä>°¡\x0002\x001b\x000e- &Í5f¬r8«[-\x001e]P¡ò\x00018ê\x0003ñÎBn2WúÖaÝtb4¸He¸V\x0004T\x0010QJ[°¶Þ6z°îÚø\x0011ë®\x0014,ÛÚÓËWDË2ò¶Y8íB«j´ê\x0018ZÄÌÉ	ðHË¢ÛRH`ZwÀ\x0006Z}Bâô		ÊýÇ¾úðþ\x001fñ0ëÅ¬âY h`Ø
ÖPcÖÜAÇqõêùÝãQÖ@¾=\x0019!òýÑ!è(iíË<ÍbI¬j\x00105A{2¥\x001bú&µÐµî\x0002Ñã«4rdöaÍ\\x001cf!tSûË¬ÃX@PfÍ¡b¯\x0019|\x000f\x0013G'tW­º]uk©a3B7LsªÄÆ©°nÑ«»Iä(ëHãåÁq{¸ÂÜ ·\x001fº¡û
º'¹7*s,~äE<\x0019\x001f\x0013çeÐ·R
B\x00075\x000bÝ±"=\x0008Å\x0003Î2\x0014Æ\x001ch?lôB\x001b'dÊÎb\x0007*¶Ç\x0000.¸AV±î{¼åöP\x0015ub7Ç0AcÇ~ä\üHØY@ð©¯U±º\x001b»­Ï$;{(	Íá\x0011¹O\x0008ºag\x000fíN\x000eä N$\x0010»#éçû/¨×ÕcI
x\x001bÄ¬EHMtÄAs)Õ\x0019Ý¸úùæ
êtµàª
®:
WI
\x0006ûs%2(ª09c[sû}hwn\x0011Ñn^16®¨U´¸æ3\x0002j\x0010ÁÅ]ÖWhýa´B\x0010_\x0011H\x0011Fkë8à\x0019ÝªõÁÝÝ¹"ÜíÎ5\x0008WÄü({ã\x0007£!Ór§\x000cWµNÅ>¸Áîá\x0006{\x0014.R«g\x001a°\x0010 ø\x0002G5£ZÏqh¡B\x000bGÑ¢¨4í³"\x001b\x0010\x00141 ÜVw\x0017ÜÝà1ÂÝ
\x001eâÅ¼4ÐêÆCÓê2ËZ{h·\x000f¯®ñêÃxµ#é×^ÓÍ\x0016<Ç1u^\x0005}\x0004®­¢înÞl\x0014®,!\x0008êt\x000bÒ	bË4²u²uâµ5ÞÃMi¾a\x0005\x0008ÔQ\x0003^_Ùz°êÄ\x001bj¼á(Þ¸Ç\x0014ãµ4\x0000\x00116\x0002[ÓÆêëªà?\x000fÁõè²Ò\x0011\WÊHº¬n+3î»» Üí.2\x000c×q© ÄÄr\x001cYt§u«öÝ\x00077Ô-\x001cÜl\x001e=x\x000bC¹¨ø\x001f²Å\x0019f7[Òö1;¼ðÄ¨ê]äç?þß_þ64³$ôf\x0019QÓ e^\x001f+zä¾}ú§K\x0003y\x001c*ä0\òÚ
\Â\x0007\x000bÜ\x0005aem±\x001bº¯\x0016ÝÏ.:¿Ê2Ð`\x0003?Zv1=ôÂv\x0015l7	\x001bX\x0003%½·\x0002SlpG¬5ª£÷®\x0013úÖ\x0008Ð©\x0011â8t¢ÀyÍMé-\x0015LmbeOGA/òjÑavÑ½e\x000e¥xýçq\x000cg¸ëÛê\x001e*Nè¡Zô0»èV×b¤k+ý>¼è­\x0001»\x0011äUl	³±\x0005ûÂr\x0017EiqÌ\x0017½á¯\x000fúnØ\x000b¡ó°×Äªûkjæ)5\x0013ü)ª:U==m½ÐC
=Ì.»¥w
§E©°ÇOP°«e¾µï=v9\x001bÓ­Ú\FÆdÌ©ÈeÖ-»2\x0015tef£!\x001eÔ\x0008]`û)EGÉÐ{úh:±ë\x001a»ÅÍÔ\¦èû9Q²\x0000Õ\x001am\x001cÁîjì³¡]'^¹Ý\x0015« ø<U=
nØM½îfvÝÕv,	Íã\x0016´bì=\x001c&ØmÝÎb!=°Ï"¸ìñÉª5{5O8îª|áDËòç±xÖ»\x0018\x0014ó(\x0011hPß\x000fL{£C°ÎÏ·ñ\x001f_àÍÀw\x001do\x0008ü¤ãm\x0014¹Eª\x0000B\x001do<rG+®\x001dtEËÀ©
\viü'¶jE}sÿñë§\x001fÄO!.EP"50gª\x0006\x0016H·=ÍÖon^¾}õòå¥Æ1B\x000fb\x001eÄ$zlÆÈ\x001ddt*ðT,!+ÓCYÒ\x000f#\x0010Eø5è8|\x0017bFSH@JB~UÒPÐwäí\x0003è¡B\x000fÓèYó7¡\x0017L\x0014ÍÂè\x0011~Gï/U\x0005_ªyü@\x0007T^}jÖ0òqà»ÊõO¨\x000eÁ\x000fT
ÏËÏúRj[þûj?~_ã÷ÓøãÃwk¯Íã*jJ\x000c.HI4aÂGTæ\x0010^0~½Öyê­+ç÷®4cS;ñeý;\x0012nüjSVCüøs\x0012¼\x0006æ7mÀÖa¦qP7¯v\x001dIN?~]ùÒ³þ\x0003\x001a(×ÔZ`\x000f.ÕîqëÄ¢T\x001fÄ©RýÏ¿}\x001e:vg\x0014ÓJ\x001a®¼dÅth±$ô·¯_¿{Ý\x0006¯ÙWÆL¢÷´`\x0012z\x00128Pü®\x0011ÑÛµïE\x001fd>È9ô¨UFì`Ø¼D7q­]¼ö2å\x000cªoâ_DÇ¯ÀýöëûO½È#FA{Ö(\x0019è2\x001b¬£ñ
çz2Í·ï~¼{Õ\x0002m*Ðf
4V;\x001cÖ¢\x0005k¸}Æ\x001e¾>Ø[?=Â®§\x0011\x0007a+`-	#±NFk\x0014¹ï·§¬ÚzÕBÔõ¬Ö(êx*ÑØ\x0002F´1)$T6´»!;QK-ö¨ñç\x0004l#Y\x0017\x001bå½2Ïo04\x0018ç¬ë©\x0004·`ÆÙ`êÆÙ/Woã\x0019ôð¡_Z\x0015¤äCÈ\x0008Ï|\x0001uéM/´FZ\x00108@·Ï/«\x0012ô­}	¡×sûÃÐEàÜÝ`8·Ôgã¸q\x0005z¸6{û
¹D\x000e@\x001cq\x00119ñq\x0007U:Û Ú·\x001b¸ª«IàD@epº(P#5¦ _è,P-9Ì.9\x000f\x0014DèÀC\x0010Ê@ñd±\x0013º\x0014Õ¢ãÏ)ì8Íg	»§\x0007\x000f\x001cåâ&&\x001bâ\x0008vUcWØµ!¶\x0007#¬£\x0017Õ !pÏï©\x0000÷b¯C£Øw\x001a4ag\x0016ëx\x0012v\x0012ßÃhÒÝ×Øý\x001cv\x000b×\x0004ÝÒZú\x0016®ù6Rp;7;µÄx
&"|\x001bÄïyïÅ^\x00189\x0017câÕMp\x000e\x0010ÓON¸dn6®¹§]ÆO²rÎ\x0014ñ/¨)þëýï\x000f\x001fÿöé¯ýkÇãø$YÞ
m\x0018Åì\x001bÞò¯7/n_þéÕOç\x0016[d\x0001 6S$A\x0008ø\x001f\x000f\x001f¿=\Ý|üíáêÇ÷?õgäú5l\x0011ÑÊPè>/0´ÿùöå»Û«Ïp½ï^¿jÀÞâ!ÂNáð8lÍ²ä\x0000h\x001f-óUZ\x$\x0018½
? ì4ûp\x0018¶à®\x0018\x001dâuÓñjS\x000b\x0015¶Ê,[íMâ\x0018a'ãã°z\x000cÚÄ&\x0018aÓã£ÓúB\x001fö lW9q\x0012¢ÔÒªõvmãÑGmÍ2ØÞîa£èÔqØ\x0010/ÂöDN\x001a/nÜ¤¯í\x0005
AØ¡Zí0µ%E KÆz¢
´%\:ã»a{UÛaVÈí2ì_¿]ýpÿþÃ÷8ÝóæÛ_ÿ\x001aqöo¥-oN£\x0004?ÞIV&üf(¿~¸¹{þü\x000eÇ|Þ¼ûé§øÓ0e{¯FSÒsõ¼)¨xiK5ò°)ÎþhÊæè£¦ìÔÑÐ¬¶À\x0016cr;6\x0005ÝfG+Ì\x001f±C×vè5vD÷R9\x001a\x0019\x00014¿
Â@¶è\x000b¤"Çm±µ-v9ÞëØ aè¥XÐ]$~\x000bÍWmQ²²EÉ5¶ Á\x000eÐw±¬+%¤g[ô\x0005ßÃ¶èú»èEß\x0005lÙ+\x0016­J¦\x0004ª	[dYo«·½[³íE\x000caYõ"Ú¢hÊ\x0007Áhü\x0008ÅÕ[ß-ÚúHi-!¿\x0008 \x0011'ü.ëÃ\x0012ÕÉ¢Ä£EXû=o\x0017GÜH>¨PNÉG°ÄÖ¬Ù,HéB\x0001Y#0dK4\x0015âÆ_º[bìÅó^Û\x0004\x0006ãí2ñ\x0003^ÿñ­W>=\x001b\x001a6ÔúEb¬ò<ÿ}©4Ñÿã?¿;«EO7~oD,ýqÈ^3ÉAÐåÒ¦-W´½Ð¦0\x0004yã{AÈîå dlî¦¹"-Ò6÷Á\x0008¹HuBÖ_è	Ç°a¬)÷ÿç$µ»@\x000c0\x0004ySªAÈF\x001el\x001c±Å¤Ç)Ï<¡\x001eÊ*7àNÈÛx\Ú}p\x001c²\x0006\x000e\x001e1öe6Øè!a»£¥\x001aC\¹²pe-QH>#.3g»ñ6¼h}\x0005ÙO@¹¥¥19%y\x0008Q\x0001\x000fõÙ\x000b#´C·yuD\x000cæ8bá±ª\x0011ëò®ã¥,¼(^ÊÃqOFÞ@>H,sàÖ*É\x0005É\x0011È»{U:Hv÷ªqÌÜt¢\x0003
{Â¬8`\êT\x001dÃlkÌö8fKû\x000fYÏFP\x0003×þL³dÙ\x0019jÌ\x0013¾áuSë¬É7Tq\x000b¢mCuí\x001azÂ5,ËRpûBågZæ\x000býHcë¼H\x001fO\x0015\\x000fX\x001aÈ¯\x001d¡\x001c&æ\x0002Áä\x0010ämÀ A6â8d\x0013®
{3+YDÌ7_Pg\x001bÂìêev\x0013Ë¬m	ÎO\x0005û²¹@9\x0006¸Þ~\x0013I\x0006Ê=qÂ\x001c}9÷5FÌº`¾Ðå59ÔÙÈËÀÇÐ\x001bDI?XäïZ¨ó½dÂÞö_É?#æP6`«òÛ¹>NüÄq¢\x001c×G \x0008¾ÿIÇZÁ*Ì®Æ|üj"$0fô
&°¡ÄæEî¼ÑÄ%È Bö\x0001GÀeIè\x0004¹³åj²*ÓÐúßþòþËé1uøTÌ\x0002¹^éu\x0005ç¢z>}v§wWWÝ]>|¹ÿ|õêËO\x001fîûãþ¢xVS±,\x001eàL\x000bìµoÁ~zûææõÕ«7o^=¿i@ßÝa]u=\x0004]rMÆè¢û\x0019ã5³8zÝòï\x0011äP!Iääyã¢«­¹H\x0016ä¶UM\x001aný\x001eºõ3Ðã\x000eå2^\tÅÐÒÚÒuqAên\x0018:Tþ\x0002SþâWôÒkb¸æQ©ùJ\x0004\x000b¡
º\x000eüÂ\½¬:»Kóýg\x0000x¨ÂK
/\x001eß¦£5\x000f×@{T\x0016OW\x0017¸¼G¡ï\x0014\x0015\x0010ºÜU®a×T\x000fØ5»Ká¿Èu®¾{ÎMØwÏ¹°ã¤\x0005ûz¼Jæ{\x0008P°¯êRW»TêÉm\x001aï
Ô½¨UIµ\x0004dè\x0017\x0018ÕÇ¡«\x001aº.h|=y\x000ceãÂo«¾rÙëÃTÎ¦\x001e[¨1¦[Ü.(Ën\x0017®»15öÉð\x0018ïÄ\x000e%\x0019¸\x0019F¢\x001avh¬Ãîêêæv* \x00175¹;~\x0002Â®9K÷òB£ñ8ö:BºÉ\x0008)ø½\x0006©L¹ú#p~°7=ØñÿV	·Ä¿ÈÂ-\x0019úí·ßþø?\x001f\x001f®~üôñþ×÷½Y\x0018êÊ\x0011§³såÌ\x0008.ªHÙ¼Þ¾{v\x0002æ¯^Þüx{×À¿Å\x001aÄ¿\x000b5ñ\x0003ÍIio4º#y\x0004F ]ÉBüï þë\x001cÅïøÒ.¦ò\x0014-
6Keü\x0004\x0007\x000eà\x000fÿyÿ1LV\x0012×_Q¤\x001bêâµÒ}væ\x0008?3ÏáÇkjÆogüÀåfaÕRüP-îYÂ¯¥ÏÒ+Úbo\x0001u÷òy(°ÖÁ×Û»|Ú½»ù£ð
\{ê\x001aÜÊ`_-øf­£Ï\x0000­EÝX\x001dÿbßX3\x0003?½ÿpÿÛÇ\x0001Ö\x0018/dÈ¢«2L\x001b÷nüçÍÆÛ7W?Ý=¿yöòü´\x0003!ßfK\x0011¹sÈ½6ÜQ®\x0000\x000e¨\x0001-"¿@^:\x000e]WÐõ$t\x0005\x0004Ý18B÷\x0004\x001d­Ê\x0003Ð¡ò\x0017ó¸\x001dirÐ*|\x0001Í=Y^ÓYå¼À4
]ÊÊa¤÷Üo\x0013\x0019qß\x00054Þ)Ûì'ëÇ®kìz\x0016»ÄBGÂ®5ÉÔ¡Ë\x0018ÂÞÑ<=ÔØÃ\x001cv\x001b¨"bwEK\x0017(@zgo\x001b\x0003Ø­°\x001b;ÝS!ÛF\x001fÇUÆNÉÇãu!v¨±Ã´Ïä`Â\x000e=\x0014è\x000b·ª­ÝÝÎº;¿ [¼Ä²;\x0000oUÝìÆ\x001aÁ®kìÑÝ&âïÝÚk`ì¤­\x001b×½y\x0011\x001cÀ^\x001fLröd²¦`Gj'>T%wRh\x0018ûI&ì»Lò(vJ\x00084øÂ±	ÃLpë¶ê®M\x0018±WmÂ°Ûkà$=è\x0002ý\x0002\x0019î0t]-»Ò³ËîÑÇ\x0011»Q^o0Ê»{-ó?\x0003ØC}òd2âÚ\x001dE5Ú_=RÎ®Ãn«D,±wNa7Ôýi\x0015%sgcï­^Ý×Øý\x001cv\x0019HqÎ\x001açA.3nó©ê/±c\x001aûä©jRÖ"\x000f4±9ÏîÞÑÊß\x000f\x001dê(\x0003Q\x0006;y2r\x001f;;Ë«Þ¾¨@¯W\x001d&W]'\x0017ÏØ\x001a
À¡à6a¿@¶2]*Ôb2*ÃiÝi\x0005Û\x0008;\\x00101\x0019ÇîjìQF{NÄ\x000c
#Óº;\x001a%;u!tY\x0005}iæ\x0010tÁôSÖÊMKAÑcGÊuØMÿj3ÿ
îÔØÝ5©L¾ÐÛ®¡O¦"©ÖgèPê2;ìn]l×¦v\x00193ë2«aVY\x0014³'ìt¦BûÝoè¦ºo]âÛê®ué	&kJuÀºd²9×âv½@3t NZ±rÒ\x0002+\x0013ÕM\x000eºÔc¸ôåjO/ìÛïL{wÖ\x0004Ü\x0003ö@ \x0005¾j\x000f¬)«ZU\x000f fß§ÄW\x001fî¯~ú|ÿñø\x0003E;¿}ýüð?^tËvBü\x0017°3îTAiâf±¡'Éÿàê§×7/Æ\x001fW¯Þ½}}{õâ¼'\x0019µ«ZF£ªªå¬QÈ3\x0017hF6fÄÄ%\x000cÛd:ÊGlÚµµ M²J+¦²±ïýûZ\x0003OeªfèA£¶×Üd\x0012K¿!juÙ\x0007ëq?N\x0000·ÏA«\*o\x0003,ñ/ìæWÐ?þOï¿\ýðÇ?#âßú5prÇç>GPG\x000cã£lvh&3^Ý½¹úá6þÓgM+¶j´b÷R=cE<`®	pÐLQ	Ws¥kça3ª¡×| Â6~­±fþã·hö³Za*+Ì\x0012+°ïÞÒÇÀ\x001b£\x001e+ÍV4\x001fF­Ø\x0015\x0002¢\x0015»:À\x0015(JiÉmøApÅ\x00149X\x0016±Mn \x0019»Á\x00193´*;\x0003oÚd\x0006I) \x0019ÍìqÔMÂ
Í\x0000½Ä\x000cìdf3Ê\x0004A*Î¿$4Q3Bµ5Â­åàÜKjéÌ@.\x000f2Ã¶^Íp\x0019n\x0019\x0004P±£\x0003G!s³3ßbã¡ÑJè\x0007Í¢Úâøs\x001dÎ\\x0003}
EbFAZ~7[!«Ã/«-0\x0003°7/µ%\x001faKY\x000e¹æs,Ç_¦\x0011Hv0éb´ãìË¨\x001d>Ï·oµLdÕ6;3þøç¯Ñ÷¿\½xÿåëçû\x000fý\x0007Gé|ÒÞ21`Òû£ÖfïÐO¯o¼}}÷ôêÅÝ·¯o7Ê\x0008Xb\x0004¶/\x0011:P1<\x001aAtÌ6úY;P\x0018M´;#ROí´\x0015\x0010SuG]\X±Ê|PñþËMâÓ\x00151	I)úF:$°å»\x0018ñìþ/ß?|¸ºùK"Píµ ®\x000b\x001ev©
0n	0ØFð\x0008fü ­dêÙÍ\x000f¯ïn_Ýü8T\x001b\x0006Ê\x00003kÃá\x0012ÒÊvÎæ{­Ç\x0017!Âïßcø·	GÄ¿\x001bp<?æ>R¯èáÜáñ\x0018ÌO+
°7\x0000Â´\x0001V\x0011XÜµy\x001eÝCé#¾I4\x0006ÇB)*\x0016Ê£ð³×güTtÆr-0þæ\x000e\x001eÂbû
,Í´\x0001xy \x0003L j\x0015ÓJ×$j\x0019¿ãÕCø;^½£ðãi¦,ÁW´þ>\x0008Þ¿¶Ét8fÀÖ\x0007\x0003¨6@­\x001ahÐÊûÂä,m3å\x001e´\x0000j\x000b`Ú\x0002áëÀ!i>\x0003°»,ÐÍ\x0001N\x000btp©´±UÏb:¦+\x0012Àgüóc<ï?`%íÙý·\x000f\x001fºôTjÒ`5\x000f£\x0018Át\x001e
Ú0ï®°)9ÃXC{vóîùó³\x0003Íl¬«QzN±×éT\x000c{ªöÆ>`©l1Ël¹TlKæ
A>ª%¶²Ä.³Ä0\x0010\x0016m4\x001b\x0003lË\x0005ñ°ã¶øÊ\x0016¿Ð\x0016Å¶8.yÄ½N\x0013DÊ\x000eNÃQclåbvijÐXø°l+Æ´\x001fÇqÕqë¾`VoÀ\x0017\x000eö2\x001d8\x000eúßac 2\x0006\x00052Ç¹o4\x0006½Kùv»Ù¸1¾:bü²#F\x0019ªh¬  ÌÙvA´á¸)ÕñËvHC\x0018ÙÉ\x0002¿\x0005è2¯<ýGlQ-jÙgÑÔÁ\x001bm\x0011Ø?\x000bæ\x0015ê)º2E/û,¦5`ï¡Ï"xïféó1ÕÞ÷ëö¾âÌ\x0012¬eZ\x0019# \x0004²æëß\x0001c Ê°,*\x000b{MqÌ\x0005.j6Eö\x000cÐ\x0001Sªï\x0002Ë¾KLÈ\x0014eÊ °2ef×M²¾#ÆÊ°ì»\x0018L1¾¼@ifÿ_Æ=ÂÑ\x001fª¨\x001cÖEeEü\x0011ñËÈBÕ\x000c|Ô²hzØjÇu;fc\x0002Ç\x0012Ó°1=tùÆÈÝB4FÖ\æSFr¥\x0002i\x000fJº\HÔÚ\x0013.\x0007	µ1«6
jÒ)=\x0001üet\x0011\x0017Òë\x0003ó 5\x0019#WÝÊPHj¨:>l2åÓ<5¾¶fÕ®Ak.\x001a\x0007OÉ\x0018ÉDH:¿ÞÚÏä:?ó¸ï³1Ë\x0018H½ÊÖèõÁyÇ6¬Që\x001cÍbYI6)8{Óº=Á1n®\x0012Í=ßí¬1¦H^Å|\x0018¢tQ¼2pÉÜ±Ê&cÌ²ÙNvLK&ÑÁpPÈ÷×_gd]/Ë
f2("\x001eKüëÆÑ§q\x001a¼=^vÀ:\x0006u1@à\x001c.\x001bM	7EË¡Éÿ{À\x001a¨=
Vy\x0004Wbw¬¨}á\x0013\x000fm
\x0003ÖÔ\x0006Ë<
EÙrÝôóM×n\x001f·&Ôß&¬û6Ñ\x0004\x000eÂ¸\x0013O3ªG<gØú´	ËN\x001b¯®IÄ\x0017µ É"X­zôÌ\x0006mQ¶ú2Ê.û2Þo
³
ñÉ¬±n}FÕÅfµ¬Ú,q~¬ÑÉ[µå×\x0019cÛÃm\x0007¬qµ5nÙ·af\x0016x)\x00068æR2®=ï6nM]¡UËJ´\x0012ÕH.\x001dE(\x0013°®\x0008½?§ÕEZµ¬J+]a¬E\x001a}O·N~5î\x0011ªª.mªeµMé$)ñ&ioNÒ\x000c+$\x0019×¦\x0000:`¯­YvOsyõ,¢ÝD³\x001faÛ@ým`Ù·Á7\x0000r4¤P!c¸Ç`?ÃzcêO³¬T+ã÷ÐttºÀ÷4ÃI
6Ü¯7¦®\x0008ªe%Ai-óTâ\x0010¢£j\x001b&´	m\x000eØR\x001f5aÙQc¡ì\x0019df/ã, 4;MÆÑuÙI¯+;\x0019ª¡\x0019ÔE
$QWb³\x0015íyÇqcTµeðç*cÊä\x0014Êð	0¢\x001e¡J£ë¾\x0006½¬±Ajþ.Ry¤:ÉÆ\x0010GH<1\x001f!i_;_ædZ0\x0017¶É\x0019K±Iâ*tÖ>BË	Ê\x000bï­eÖä\x000f¬Añ%¶F²£µçèÆ­1¢nk\x0012Ë"3ª|äÈzêÎ<Oç¬ocT\x0001àÏEÖH¦\x001f3J\x0008î\x0007±ò\x0019tË­ÑUGÑ«Z\x0002¤\x0012\x0002($S3ümÈ\x0018ù\x0008AÀØúÓØUF\x0004àé´Ä\x0013g\x0005Ü\x0014àtSÀç5¡þ4aÙ§A=\x001fr´x½ñ¤ÚÂ<wÎµurXS°îÛÄoÏÊ&\x0012d
N¨5Ð\x0018`ë\x0016Z»¬V½¶Ä.P &\x0019ã¸YÓ6õÁ¸1¦ú4Ö,û4^òì9²Ó¡)Ëï^´ù\x000eX\x0003µ5«6\x0004¢\x0013\x0010\x000f\x001ej¤Uy­4vYF8À¶Æd\x000b6\x0005X¤	¬×ð\x0018nV5ì²²ÀB\x0000Ù¢O/\x0014\x001fÓê\x0011|Ì»ÚU÷3á,\x0017ÏbÌÍÊ°®o³\x000c\x001b\x0013ó½1øsÝwq$ð/5\x0014Ì\x000cÏ\x0003x§×¿;9UµàÏEÖ\x0018G/5&ÞÐ®\x001dYÃ4MÎÇ0ÆÕÆ,«\x00038ÍZ3ÆBwç-ÐÐHëtu©qzÕ¥FäÙîägP\x001aéâìÌ?F4sõK[öRb*kêhb)@¾>z¾\x0000wÒI¿¬^h~{»ÆòKºÂæl\x0010ë¿¯»iü²n\x001a!²3ã\x0005FHêÈÆØ6/÷¸1ªî?WnÏ>D\x0013b@\x000c\x0007¬Éã'`\x001eáÕÉ×sA~Ù`@Î0Ú5 v<à$2YãÔúÓ×©¦_j
gz«4\x00124\x001b\x0003pÝÄæ½1n\x0005Gå@\x0013¯ÑI\x001f¸\x000eü#4¡úúÑÉ¯ztò!:\x0017½ÕZÍ<\x001c<¬\x001cDS\x0016þ)u{_ÕÞ\x0010÷?O:\x0018k,ßg¤åY Û¤ÂÃÖ@lÂªd3y¦=£-óIÏ{&&·È\x0001kdµg@®ÍÚ6
YÐÍY·Íð\x0008\x0019
Ô¥@XU
Æ\x0004ìNÆPQCZ>6\x001fÇ\x0018]\x001b³è²\x0019³|Öò66~$ºÔHÍ=¨Á´	~\x000fXckkÅxð\x001bÚ5P¨Ü
Ñ\x000bÑH\x0003u½	VÕbh\x0004"q56\x0014^Þ2î1Ü¬Î\x0000`U\x0006\x0010÷¾&/\x000b²¨Ü\x001bNg{\x0006T¨§\x0003aÕx`ü.µã}¼X£y@06£æ\x0001kê=³êEÐ\x0007äÉ^æ$p;­<\x0016à\x0011\x0012gðõð_t¥ñØßL­t\x000eÛµH¹\x0015crâä\x0012m	÷\x0003ÖªH?Wy+ß\x0006ÛÐ-\x0007\x0001þ6¡­X5lM\x0010U&EU\x001aÔ>¡9#PC*ê×òi\x0008v¹5²\x0002A.\x0002¹.[\x0003EÍ[1áfbVYnªÊ4A-*ÓDkÂ8'6F\x0001Þ7Q¦	ªþ6jÝ·Ñ\¦A\x0012#CûF²âMuû\x0003ÖÔhaÕ#Z"\x0013Í´pØ:[ø\x0012%5;Çoó\x0008³õ¡&¢	«h|ÐÀ=\x001b\x000eû\x001cÉÓð>CÖ¨G°¦.oUåÍ$ÐN\x001a\x0007ºdÂó·ÑõÖÔïhaÕ;ZÒl×ùæð\x001dI\x0015G\x0001û\x0008´'¡\x001eß\x0008«Æ7<\x0004ËÖx+p+ÓS+æ§~:\x0013t%@Í\x0001{1Ég[Í	\x000eQñ\x000cå¶\x001ax\x001b¡NÂwµeFI×ùC\x0019½Í§\x0005æ\x0000ÙdÍ;T>µ	Ñ«lò!\x0000w\x000bXa·B¡±\õl*\x0018eD¢OÞ\x0006¼ã_<9U?øåÃÃç_º÷u$`|(\x000fRõ\x000cåÐ3ÁóÛ§Ïo_?m±ñ¢\x0019òÌzÔ\x000e<GY;i\x0002
â1
ôHþÙgÈöÚ{ì\x0018þ \x0008Ð\x000ch\x0016Ã
b#I\x000f#¯P¨Ê3Ú¨!N]4DsHmÌ\x0004=Cw\x001a\x0002!g*\x001cxëh³[)\x000cO\x0006I5AoôHRÓgÈn¢!ç²Ía×²\x001fç6Èµ \x000c@ã¥Ï\x0010[¹]åZL£!ä¢!L2®\x0012ÃÂbC*×²k\\x000b¿\x0008½\x0004 ¹¤è«8ü*å\x0006\x000eÇ>C|\x0015~Ïu6
\x001b¢yð\x0004 `6G-jÒòJ\Êú\x000cj\x001bÚ\x001e5$\x0004zÎ\x000cª\x0014e\x0004Ó6øø=ïu¨¶\x0008,Ú"Àm\x0006ÕC\x001cË·XÞ"C
MÊ3²á½.¯!\x001fì(æ\x0002ôE4qÏyÕ!>jH¨¾È¹fæ\x0003PYØé\x0002iV7RmúâQC¤¨¶\x0008þ\ã[('LºTÒf·¬Þ6Òûßi«í8Sµ<ðE%;\x0014\x000f3\x000bÍ7båõêè»#ÏIk÷\x0019Î~\x0003ß,HàJÅ\x0018qf%ªÚíò\óâðA¢ø
EXIu£l	ðæôY¢O.$«n$Ì5g\x0002\x0018~{\x0011<åµ\x001a!gê´\x0004jK\x0016e)ÆsdQØ\x0012Ö\x0016Ö#<s}Ôi£\7ÚÒFZ
|(jNµX~%AÚº½%nÕ6)ªGøü*xð©¨EXn¯-ñ,1»<;g\¡H¢&n·ðNK|mÉ«QK´#\x001av\x001bw"K&RÞlY}.*Q\x0019¢Ä"C£nK\x001bÑù\x000eõÍ´\x001b¼î3ääâ¾èæòlÙ·,r¯° ¤ä\x000fâìêM¢Lu¨sý"Ã_DÐ\x000c\x0015ñÂëH<¨dó:¼àõYâle;Ó0ZL	\x0004s­gIîK`K1euÆ¥ê°¥V-É¯÷VÄ\x0005èå°\x0005ËsG\x0015jß:78úE¼¡Ê©5ì%>^\x001eµª,ÑçæG-q8d­DýØ¬*\x001dxß\x001b»<ãÒuî¨\x0017åhË\x0014¡L4RGãFÞLú\x000c1U1[ã'\x001c5Ä8dMXIÃ;\x0010ï¼ÝýÈ\x0013j§%P[²¨
ì<i\x0013Äo¢©2~\x0013®\x000c¶úÙ°%¶v®s3âÃßDpèBÊ¨Ì´\x000e1vñ6à>Kê,X/Ê}<\x000b=íFzªÌ\x0017%VÓV\x0014\x001b¶ÄWÇâYòQK\x0014Ð\¨w<\x0000±Ýx+\x001fº.×éEõ:Û°g}\x0005@y\ú&A-\x000fÂ¡þ&çÆ\x000e¿Iºë&Kø:\x0012ÏÎ\x0015]nyè
®6dM+mx
Â\x0010¨¨\x001d0µ\x001bGçZþîcêYt3ñÒrBTþt0ãþ"«\x0013#kKÎqwZ",\x001fH\x0016\x001f(\x0008[®©X=B\x0005Ñ[
Þ7EpEø\SÄðÃ	«\x0011\x0010/ÜëK-uD¥eÖx;ècÞ%w\x0007ý³O{ørõìÛ¿|ø½[õ\x0017\x000cÉ¨¹àØ\x0002ç>hû
ëÙí«×Ïnß\={÷?_Þ¾8¯øk²@å¾¬mì6;Bÿðï¿¼ÿøð¥wýU<\x0000óx¶Ñ¡²ª\x0015ÈÂ.Tþ\x0011?ÿOï^Þ¾i ×v|?ãq\x0004º5$\x000bj@_\x0007FÎT¢cî¶\x001fùþ^Ê\x001eC\x000eTw¾\x0011óCB\x001eH8´_túÛÊYì¤·XKsNÚXMf\x00119iùÚÐAHÙ\x000fÝUÞâf½Å_\x001bB®ò(09C\x0001ÞLºKQ\x0001ÇSÈÉ \x0007\x0018#\x0015Ié\x0000ò\x0000\x0012vm×-ºÜºÉ\x0013ö}7ù¡UO£}	»PôÀ¿mR\x001bk¦Ú\x0003Øe]N®»%J,­}\x0002L0\x0005{[Â¨\x001f»6\x0015vm&±sî¦ã\x0019Ocäï\x0004]Ënêe7³Ëîña¡g¶+\v(Ø\x0017.;@}¯u\x0008{\x0011VÑ¥}\x0002µ\x0016\x0008{\x000cë¶ªÕº+9¹î¨
¾ÃÎîN©%b_	¨:Ì¨\x0005aÆÒV\x0015¥<\x001c³\x0018Æ®\x001aí\x0003Ø¡
ï
fÃ»Åæ@Ä®p\x001aC$\x001f­\x000fr%v¨±Oú»õ4ª\x0015\x0007Q>à\x0019z\x0007\x0011úÈ©ZßCòÉº¿\x001cô\x001cO\x0007ÖÅ\x0002 @\x001bìh£RF³ñ\x0004Ç¿xrB\x0013üùÓ·¿?\½Wû½7\x000f¡enÖ;\x0001¹\x0011ÐÅTÏÛëWï~¾½z\x0011/!7/\x001b\x0016ìXeO\x000fY`<÷ X$\x0003Ê\x0006Ä«\x0014S4t\x0011iX *\x000bÔoÀMñ\x001bHÔ\x0008ÎäLg»è³\x0007,ØXÑ\x0013RãC\x00168ÃlÖ\x0016i£¸5è
\x001bhj©	»[ªo%M(MYV\x0007n.×âG]o\x001f\x0003&øê+ø\x0005_\x0001WB!ðLÁªÊWèM\x001a0aw\x0018D\x0013N´? â\x001f\x001d	AÎP\x001ciñn\x000eUD
ó\x0011U@sGÖË¢ò-éëîÒöè·`'&Î\x00131Éc_! W|þ
ö\x0008É\x0002KÇ\x0004µ8¤J\x0001µ	ó$g*B\x0004\x001eü\x0019Tq¤.\x0002ß\x0001\x001bT}4«\x0005¤
ÕjÅ	=\x0016Va¦KüëÅ6ÔßA-ø\x000e(¯ìh;\x0008ÆÑÜë\x001a·ÃâÏ`êÝ`æw4î5ÑÀbñBÀÇ³é\x0012Qé²A'­ÛÝã~\°ÝÛþ\x001e>~~õüþã×\x000f¿wOBêxQí"b
'\x001b}\x0003Ñæ\x0016ùÓíË×wñ½|{ûüÅùyÁ\x0004_nsÑ\x0008_îæ¢\x000fâ\x0019È\x0017\x001c\x0007À\oñ|\x0008\ _?ÔøÃ,~«©÷\x0008¯\x000bÌXkY/Yºæ»÷\x0010üÝK1Âß½\x0014\x001f\x000f4õ¤½Èá\x0007:Ñ¤o 
áßDj\x0012þHÍAüXÊ¢å·\x00021áÇ&û\x001fâW»ó8âW»óø8~v¸þDB\x0017\x000bÏë\x000f­b\x000c¿¯ñûiüã3	¿sL>mÞTf\x0015t\x0008¾¬áËiø1ægÕ\x0019ì¾ãfN\x001bø\x0014V²Ù"1_×øõ4þ rO\x00172fáY^\x0017%q±)Õdû\x0019B_Ç~5\x001fû=ðÛ÷ópSpô°tõ\x001dTø\x001dLâO<Ø¤b\x001ec¿ÈcdÎ0Ûj³ÇõâqQ
ûqÑ\x000cÿÅý×÷_¾tó
xTf]/IÙ\x001bx`&?+Ò«\x0019ý·woÞ´Àï:"x8
£àã\x001d\x0018X.Î\x0010§"á»¤	ÍÚÖ\x0000x¹ë-à¥:ÍÚFÑow0\zAè£¾9ý=>\x0006±=zü9\x001e1ÂeH\x0005Ò^sIËêæÛz\x001fz¯O¦½ãI¿ÚùûW7ï¹ÿük/t'S\x0016¡;\x001a%ä¸xAAsÂå_no^^ÝÜ=½yýãeÜR»=nü9\x0001Ü\x001aC\x0013«\x000e	ÒóX!xIÔ4 |s¸\x001b¹Ú\x0010¹Ú19\x001d@\x001eÃ$QkÅ%·4è\x0005VÒ#/hÑÔtèG\x001ejäa\x000e¹Id­	9,I	Æ$%´5ºqë~\x001eqë\x001dýü!Ü¬Ô\x0010q'¶\x000c\ëf§\x001fx¨9àóâÿa(¸ù8éBsØ©\x001b¸q§\x00187å)Ê\x0005zvñJÃÝÏ¨<æ´C?ð\x0000\x0015ð\x0000sÀ\x0015U\x000f\x001c¶£RËfÖh@EUÈí®z|W½9<F\x0003!/aE9bîÍn³
ùFïèÓ¬¹\x0010¹3-^NÓ\x0004V\x0002\x001e\x001c/¹jN/\x000c\x0000·5p;µäAQ\x0017v¼:ê]V@ÂÖ\x0011øºèL\x0005Ü9àZ\x0012¯[¼Ði«R\/\x0006Ó|ÿï\x0006îe\x0015W¼+\x0002&r\x001dêîQ(\x001dÉUiÓ\x001du#Ç\x0001\x001dò4¯1\\x0001\x001dr\\x0011FtÀ¦ ëÈ¡_=ýÓÁ¿{ú?â2Hu'\x000e\x0012e¢ðBu½è<M©ð!\x0003¾¦~âÊ\x0000ü«ø¨HM\x0013u3yø#ÞHuIuW|Iä¶, 'u\x000eðñáê×ÿúÿ¼\x0019°ôN¨\x0015$³\x0001²\x0001çûÖ]\x0011òåíÕW7\x0017\x001a¾3ö]¯QÀqçið¦	t\x0010êÙ\x0008.¦Úv­{'øM--¼\x0005\x001fLî·×\x0001È|Ë\x0000ÉÕl\x001d4,#àC\x0005>Ì¬ ­\x0003ÊÛ\x0000Ü9ís\x001c\x0003à¡r\x001bv\x001bç¸C\x0001¥|¨¯\x0011¬¦1j\x001døý«r\x0010Õ«ò1ô.xî
¹[$-½cmH#»n§èeåôøs\x0012=ðØµ\x000e½çPémQ×ÍÞÆ\x0001ô»R\x0012¢ß®½#5[\x001d¬ )K\x0014\x0015Ò¼g"Ð\x0003èu½öz:â Ï.UÂ#B\x001bÀW5Zû¦8Ò\x0000ø]RàOÊccÉq¼EÊÓì8Á·;£\x0006ÐÛzéí´Û{à.
!YÙ\x001d¼a\x0012]ì¸[~wßFô'÷í#èS/îY®ÍxÃº-k·¬\x000b5öÙÊ¹"§\x001d\x0012s^s;\x001a6\x0017­Cïë`ïg½·üäg\x0004ÊgÓQeªÐ|7\x0018@\x000fõÚÃôÚ{Éý\x0002Û\x0014­=\x0011êÄµoRÿõ£ßWÞ1¹Ó\x0007­ÕLlR¹Þl$7®{U'zUíY¥¦÷,
\x0015ßkKÍ\x0006S´öÞ-D¯«KÉþ­õèÚ\x000bZx\x0016$\x000b¯=/|Óz\x0000z\x001d,Õ|°4²¼ØBÊ\x001e{3ú¶ÔÝ\x0008zW£>¨´æJ
ÅuaW®TV/Ìp\x0014Ôk\x000fÓk\x001f=ð\x0011=åg1"úæ#}?z]_Kôü½Ä\x0000è\x00017à\x0003(\x001e\x0000V¡É8t\x0015¯
9ù:~RÇ9r©u4Û	Ø-ACñÛ×µYr§µÖ×ó\x0003ñ/öó\x0003Ïÿøç§W?üñÏ\x0008ð·þáq­\x0012#AÀF¥ªÜb`q\x0002§[IÚóÛW/¯~¸ÿäÙùáq¿u\x0018 ü]ÁAø
)\x0005i\x0006,wmÔ°YÉ\x0019Aïô\x001e½ÓÓèÿ?CLL\x001b\x0008<k7ÛÐÌ\x0007ÀKQy\x0014Ó®£hÖÐÄË9·\x0017³¬
®9k8\x0004^×àç^kóÄ¥÷¬ðQFMS\x000cc\x0008¿¯ñûiü\x0012H'7â\x000f¥5Ú\x0013w¹E:Çø«ð+7_"YE\x000e;BSõ8þ{]&âLt#ð·\x0004×pp\x0018~ ç\x0018w'ß´u<\x0015o¡uè\x000eá\x001aÿtÜÑç©-Ô*­sØ×JsÜ\x000c+·¯ªÝ_Í»?N7hò\x001f$âð'£>ñf´pý¬Ü_Éy÷·,\x0006¡­\x0007Æ¯\x0005×ÅÒð£T\x0015>\x000eØ?ÛÐç\x0011GÄ\x0018¿j6:]ûÄÏ¯]ævø\x00083\x001cEq:\x0003â)Æü3º9è3æF§f +Íñÿ7å9âÝn°ON7Ãýç_¯n>¼ÿÖû\x001cùú"\x0015ë»h\x001ewV\x001eOºyÙóËwg\x0012	¼=x\x0007³à%ÖK#uàüÙ¸rw4Í!øÛ\x0016Âß½i\x001d¯%U÷#~è	¿\x0006¾¹ë&ÍÚ\x0010þà÷øÆï$7\x0019Kã±!á÷\x000bV8ð¶\x000eÿä%ù¾Ó\x0006`§K.à6&z\x0013,\x0000Ûµw»
0ÿïùÇ\x001a\x0010S!þ\x0002¶\x0008RXU*W¶)¥=dU\x0001VÍ\x001a à)Cé$ëæZ+¸ÒÖ8\x00193ÀÖ\x0006Øù/àQ4\x001a \x0003ÎòdÄß*@\x000cá\x000fºÂ\x001fôô\x00070©l\x001dk4e\x0012\x000fdö ozÐ&
0ó\x0006ÄÈ_,$j|;\x001eRâõ&ÍT'~ÉÁ·\x000fà\x001c|O\x0007wõáþêùû¿ \x001bâ×÷zÇT½\x000fÀQÈÄý,=\x001fGX\x0005\x0000ÍwÒ\x001f£\x00157WÏïb\x0012qóöîÕÙ1Õlbo\x0004þ6"&\x0012el[Z¦û*m=¡oÈí±:Ù Ý\x0002\x001b\x0004Û\x001a«=ÛB0lZmÃî<@\x001böÄÓÇm0Äé\x0013¿-\x0014\x0000mþ¯!#BíLa3mjêBR3j°<¼\x0014|9{È\x0006+*g²b3Å«½%
uev0x.®Ð,R\x000cÚ «ÈdåÈ\x0004Ò\+RÁBi\
¡-d9fÄ.ÅC#*\x001e¿Ã\x001fB!|2Â\x000fÁb\x0005B6ãGM0µ	f	?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=zùÃÉÕéÉõâÒ.³ÁTçôüCÓÛX>=O¤§7¥^à\x000cÉÑ\x0019V³\x0004®ÖÎÍ3[Æ+M
é?ùÂ°ÓÖ¶3y~æô!gàSóWÖÎzs\x0008NWsºÍ\x0010côùµ@\x001aE	49Ù\x0002þ\x0010 ¡\x0006
= >æÒª\x0004JcRm\x0006µ×eúÕ\x001d\x00007/6-r«I±|zn¦ý\x0013½\x0018TÊß\x00079¡á\x000eNºüº\x0012h:\x0007AÁÈ^Âù¥A\x001f)6¤ØC\x001aõ1¯Qk³wôL\x001e\x0018TÇClzh\x0013l÷NÉwÒ80Nj\x001cùÛ{üñS\x000exÝ\x0004{\x001eÿ\x0004tÃI-$/?í&Ô¹=ý2Id\x0010´ñOÐã HVÆf\x0006¤a-dQç¿½õþ Ô7 ¾g\x0012K\x0006'ÉM"
\x00184TÅýs#iãI¡Ç:ªqËûI»©Sb²©ÎJ`É¦Îá!HcC\x001a{>¾ç!CÉ¦4ZÌr.`Q]ðAö\x00136N\x001f{¾óï,È¦é<³&²¡¬Ô\x000c6n\x001f{Ü¾wZÖ)M5lSâ¢\x000eâL±ñúØãõ¶eÒµ@SâÄ\x001bÊ,S¾S\x0011RÝeR%vÉ¤!_\x000fI%g¶4£÷\x0000¤MÂ\x0000åTù:¥)>»SNlªÕAlÚ\x0004(Ü\x001e M5?eãç'\x0018
¥A6Tâ\x000e6\x0011
{"T¹®$ªcMÊÂ\x0013	\x0014õA6T\x0013¡°'By¥ókw\x0002Mî
ó2u.\x0008©;È¡\x0004\x0008=\x0011J*\x0014\x0002æ+©¤â÷á Q\x001f\x0008=\x0011j\x0012xÌ )ÙÝ¾Pjí!v¾n\x0002î	Pª~2¨ò$¿:YÔ+/\x0016Õ\x0007\x0001mâîO)g*\x001bßhÉN\x000b\x001cÚèC¬RÝ\x0004(Ý\x0013 H³YLj¨©}2©â¡ÔA"©nâîO\x000eXu<ÔÎ¤F\x000ePÉÿ\x001fäã7ñI÷Ä'«ùn\x0017\x001cu\x0019\x0003o|]>¾ô6ñI÷Ä'Kµ8¼Ls«T¤(;\x001f\x000frÎ×Û×=nßi6G¶)îÖ©fgjb<\x0008iãLu35ÉGe"1çÌTkä
u|ê\x0014ï>ÍnOèí'>rÚ7:;Ô\x0010øG§?Â Ò?ïÊÜò\x000fRæöúæñÝÝíÃíªH*eÊ;êÅ\x001dß\x001aÇëÔy[ÅùúäúÅÙéåï\x000b&ÖØ©\x001d	\x0019MT
`ùÂ\x00148>y«¾î­ÇÔ5¦Þ	1ju\x001c\x0019\x0013äþy5ä¯\x001eáË·ë1mi·cRë âìúÙ\x0004çË5ùwüzJWSºí6\x001eßëQõ%§øÜBM[\x0008¿¼á×cú\x001aÓw`Fåèú1¥Í2JÖréC¬ÌPS\x000eJ
YT®<ePù¼$×ÎðDn¿RÍ½*ÞèÅÍ§O·G?ÝÝß¯ÜB(;Ý\x0000æ÷PÚBZnsÕ¼ö«"}qòöíéÑOgçç+`u
«»`MÉ¨ãØis¡\x001aõ"F-±óWM°¶µ]°D1&Vå¦>ôé,Bï
\x0013+>u§»Õ×¬¾_\x0019S*Nï ù\x0011?Åü'Î#ë`QÍ,6³Ùº}øõöa]þìJ®pÙ° yoiÿôÕÞO§¯N/õX×3*v¢Bn \x001cJÞó\x000cé~ñµøt\x0002ý<,Øybbÿi'AòËíÑÅÍã§O7[wÐ\x000f¹¶.xµÜñ(§ÒøK¢§qtqrýöíÉ_¾ÀëV÷á·_~®^Ão^ÝL>\x0015ùÞ×Ot¿ß¦µ{óású÷ùhUp96Ñ=Ó4ßÆ\x001c§d< ²ñ_¦xrqõOç'G¯N¾èE\x001bôqq5
5uØâ4uüM(^HRÂ4@¢YK\x0002:â	$Òìb@RVÁ$é¸\x000e[I>ÜüËçÿý;{@ò{äÅÃÝÿz¼ýüùöáî\x0019"§èd\x0013\x0012Ð\YÊÂµV\x0017W\x001eú\x0012éÅåÙÿ¸>½º:½<ûx7\x0019IéJk8òê¿øãï\x000f7÷G¯o\x001fÞÝå>'@1ÑM0kA!­y\x0002M¹\x0007&xçý\x001c¶ä«ÓÓËó£×§/ÎÞ\|ù
¬©aM'¬çqÆÆägäæ4\x000f\x001a\x000e^fÂÚ\x001aÖvÂ¢ìT\x000b)ñÉ¬è¹ù8jµØ¨]¬®fu½«@ç*êÈ\x00196ä\`=\x001e\x0004Ö×°¾\x00136\x001dp\x000cÃR¥\x0012dX
Ì\x0013l\x0010-QØXÃÆ>XpSÇ\x000eÁ\x0002	äýE¥\x0003\x000c\x001bÃA,×0¬Ôl6-MffÓÆ\x0005fÓZ­\x0013H³õ ´ÐÐB§mM¾:¶V'n},È¬ÔâÂÂÇvÁb\x0003°ÇÐ¤´t&Óò<\x0010Â` \x0000Q\x0001r3ÉdZL,[\x001bø\x0003=*\x001fµ	Ð\x0019\x0014 \x001d¦Ì2\x00196páb
QFs\x0010Ú&(@gT\x0000Ñà²eË7 Öð\x000eÉ\x001ff\x001d4a\x0001:ã\x0002XÌâ\x001f´Å@\x0016-H³s¦\x001c1ÆhCC\x001búýA\x000e¸ZOrÞÙ\x001f\x0008«·\x0007aÅÆÓb§§%E9±¬³ù¶)ë`=wÑ6\x0016{=­âÙÎÖNE.Ó\x0002kïD\x0015\x000fDÛ¸ZìuµÀÃ}\x0012­¶ù>Ñæ¶\x0017*Ì\x000e\x0007	bØ¸ZìuµJQV@°V\G¦ÍÒ|q*Í=\x0004lãk±××Ó1¹:\x000ck"[vWû0\x0006Û¸Zìtµ*º,f,1÷ç$Z\x0016Û`õaÖlãi±×Ó¦¤6\x0002ï0®, ÓæÞ'Úaú0¦m2pìLÁUðTJ6$óyAQ
þDK­ß\x0007¡mâ\x0002öÆ´¯ø$m~jJ¶ElÝ=±6Ç\x0005ì</(´­MK"·À%Ã\x0006¡þ Ë@7AL÷\x00061*ÜÉ´ÖÄ\¸C¾+\x00046ì®Ù¶	bº3Q[Ëb:#Ð ÙÉ¶üÞlë\x000e³hu\x0013Ätg\x0010SÞdÕD«ù\x0006V,Z4¥Ôh¶½Eêb¤<É%Z§ä\x001aI\x0019\x000e¹èá QL7QLwF1jwcÖ Iâkbå'Ý\x0004+r4£°M\x0014Ó½Qì¿	¶bº3Q[t%qq|ëÉ\x001dQ\x001b{\x001dÖ\x00041Ý\x001bÄRRï¯-MÎã{¤ß#Ó¢?H  ¦;XrÙ4 g¢õÓ¨ÒL+	öæ0¾¶	cº7a¹íð¤ÊÞ¦´ÉJ8H\x001c3M\x001c3q,}s\x000c\x0001tnæ ZY	FÅ¸/ÓÄ1Ó\x001bÇhþ`¦õÉ×\x001a^·À£`¢vxÈ`È`z#ôù³mIÇh1F+¶\x0005{Ói¼­éó¶6Ær\x0014R\x0000$\x0013\x0012mãX:ý\x001efÝ6\x001eÌôy°D\x001bËºMàZhù&<ÀÃàº-¥i»µ+¥i\x0017D:s6îI¤Ó0Å£Vã4þ 7\x001fshì¦S:F>¥ë¬\x00135Òy\x0015\x0003\x000e{º* ÿÀU\x0001÷÷3ñçgVEP6«Ú¥UA·S\x0006\x001c
î½j>?o\x0004GÕ5ªîCÕ&×ÜÐv$ï&T»Ûm\x0000µ5¨í\x0003Íj[\x0013hpâÅ¼\x0003¯ña_ôÝ\x001aç?ÒçAz¿Pü\x001fÿÉòÏ¾ãMË4F6¿ãQïT~	·jy {ArßíºäeÄ\x0011¿5FÛ\x0011w\x0002ä$\x000eys÷û»¿={,nSøBy´SFüªõqtO´¤\x0010yröúÅ\x0013u\x001f
ý\x000c\x0011ËØúW7\x000f¿ÜÝ>çöµYZÂÚsØi1\x0006Ã·±V\x0006qÍÑÉåwg§O9!FÃ\x001a
7¡9<æmb§
,òðhß¤®%Ó5Þf4/Â)÷È\x001dfd4/FÓ~¬\fk4»
ÍppnT<{ÁÀ¢­ÔË³?¡[æj4·í{²ºA²×â '\x001dél5ëö?\x0005®E\x000b5ZØæuîÅJ\x0014\x0003&4P\x0006Ó$¡>4­çaCïÔôYWåãï7¿~x.jxP¹±DòlÔöóð;\x001cñ#$©òæõÉ«/*ªøßIá£lØ\x0017´CpRVÙyå5NÙÊ+Ää!Ü5KoSVbÛÜ/©d©ê\x001aTo\x0007MvttsG>x\x0012?Ì\x001eÆÙÈÑ\x0003TXt5¨ûNwÎ?w¾Ïu¤7¿Òw\x0007¾Bu¹ðüæñáv$-ä É?ëtn"´Ås\x0008
Ý4Ê¦ùÓùÉõå)¯Ìó\;zòêK_¼âÃ\x000f·ò\x0005\x001eÔ¬S^Ë\x001dÌ&í\x001c\x0000\x0006ÔÁ\x0002ê\x001aPo\x00064ÇÌGGsË|¹°ÕP³£|¦æ3[ù¢ÍCº\x0013`:ÔfÕXàY§Ä§?°­ùìF>+Óërâ«
¹:\x0001:\x0013G\x0001]
è6\x0003ò0VúÂ>¿zNRF,èGù|Íç·ò¹t\x001aá\x000fì=EçIùçu\x0019?0
\x0002\x001a0l\x0005\x0004®.¤/\x001cÖ'ÍÑ\x0017vÃ\x00165`Ü
èCE\x0000Ó1\x001fXúWçi¶dA?º\x0004¹æM´ÚJ¨\x00155NL$\x0003Íj´.wÊ%\x0013úa7
m\x0018Ù\x001aGLr3P9½Z#5óO6äNÞdC(OØÝM ­Ä\x0018VÈMRl\x0018,Ã¢o7a\x0013I`k(¡!
*Û\x00100J0N\x0001\x000eÙ»îÍnÂ&ÀÖ`B\x00155uJ·Ñ°¯ñbÃ8þh\x0002[ÃI:ä¢5ºñrùìdÜmlhMØD\x0013Ø\x001cN\x0002ä¢ä®]î.!gE9ÈqØÙ4ñ\x0004¶\x0006\x0014Ö\x001e\x0013¦M+JÝÆbB=ê¯¡	(°9¢DÇÃFùÈèòy\x001c¶5£MD­!ÅÑîÈ!\x0005H!0FÉÃ9\x00036\x0001\x0005·\x0006\x0014\x0012µ\x0012ò¢\x000cjÀ Å\x0000£û\x0004Û¼«»vÉ]+ÞÈéÌ\x001c³»6NI@1¦?±n®0]¹Â|õpó!\x001dï\x0012çsIµæ×\x0004jÎ\x0018\x0012|_£\x0016~ðÕåÉE:Ö%ÆçÁ°\x0006Ã
`Ôaiø»¢ÉO¯Ôh\x000bM[·ð.[Àt
¦·X\x000c0ß/Û¢8¬ãâÁLÍe¶\x001a³\x0002ðù\x0005b2\x0018óÑâ|¹\x0005ÌÖ`vÁÒ±ÃA>{.\x0001"Et8±»=è\x0002s5Ûh±évÀh:j6\x0015\x00060ô%}Íå7\x0019\x000cÎ\ÊóÄ\x0004&9r°ËsÐ\x0016°P-\x0006KÇ©àHÓð­©\x00125qqùtâeV·+Ö\q\x000bFYaÞ#½ÃM2Ê!ðÒ÷\x001a\x0016Qt\x0003Xuä!ïª¶ÙÈ¾?÷\x001cÉP\x000fCî\x0015Z¿¿ÅñCÈe¤RjØ`(7\x0001.âÈÆëÃ&·¯%/W4ðW\x0014±#ò-TÊ:\x0017	Ç¦MYÞ§ËÆ¤\x001f6ìMk\x0015ÒÞD{Ìß*ñó\x0016p~h\x000bÀ\x001c\x000f6âD\x0001r¶fåX£<HÆët_Ô40¿¡æïííãÝý³îCç'd;êÏe¿fäÀ\x0010ölr3ÿöôúìü\x000böçßoûü¿\x0005\x001b»_Ü|zÿ\x0005\x0008\x0018ÊNPw¿~øÛ>=>üé§Û\x000fïo	
è0ßGM\x000e[\x000fi\x0010åGñôËÙ³W\x00179z{}yôÓéÅËÓ©øäíËë/ª\x000fP<Ú*\x0019Ê?þÇ£ïo\x001eß}||øu
©£zÉ£¤p\x001e}n\x0000§Çìë1®ÌÍH§¦þë£ïO®_¼¹¾|õ<®©qM'®yJ]Â
Üp¥å&¥¾þ@´¶¦µ´Z:È\x0015iùe\x001d¯ô³cXSê>Gi]Mëúh½·\lË5i¤I}È¶E&i\x0014××¸¾wåz.QÎ\x0019VøI+×uõ¡hcM\x001b{áîlÎùUBmVÖAZÎ.¶Ìo]\x000btwÎn!p>uifÁiZ\x000bö@K\x0017\x001a/\x0006n,Û³äKæ5ÙáR\x0005sá=ÐjÆA§\x001fó¹-@Q=xÖ§2ÓäóÂ`\x001b/\x0006nÌçBäÃT\x001eð\x0016.*Y	\x0006\x000eµ\x0012\x001a'\x0006½^ì¿É²\x000bN\x001fæÝ\x001cHn%\x0012¯\x0014Ö&ã7¾QÞÐðN^d±"â-XÃÕ)D|!¯ÙÎ[R×\x001dsQRÜ%²Ñ\û\x001c­6e
a3ëPÝ\x0003å\x001fªÙ¶¯oïïþú°*yt$¢îò¢ {\x0004Ð¼("ç8\x001eÌSF>=z}z~öã\x0017uq*XSÃ>X#Ú3*\x0006Ì\x0002v)Npsù4,é0¬¾fõ¬!ßa5kT§ \x0011]\x000fÃZàÄZÍ]Ý\x0004+\x0010dXÍêÏÉ9/5Å\x0006\x0016û`Ñ\x001cË"°<H#¹\x0005VñøÔ½k\x001dÇ »ZAY¸ÇÛî¯"X"¡Á«A@£?²"Y#b\x001a\x00044  +Í\x000eîRz\x001d½±\x001bá\x001eqNâTzd
õ\x000ceP\x0002?xFø+üQXýA°ÝÁ#K\x0003Rª¯Pî¸b_Â
­µ´Öw´~6sÍ£¡ÇÀ*\x0017Y\x0019\x001c.9
ØÐÁ!Ø\x0012³=\x0003*º
|\x0010\x000c·gºb/¹a
ÚÜÑæ1Z\x001aÀç Õ&Pt«\x001bfÓ%Ïf;,vF\x0001Ç¬\x0002m¬h¢5¼¨\x0008\x001cr÷B\x0011­9æÔbwjqìÔÒ\x0012f/´P3Ödh\x0007áR ® íì\x0002\x0019\x0006·=m\x0010¯Ç¶îÿ\x0002\x001b±Ñâ%·q;-7A{\x0000c´\x000e¹°Ûª¿0·sëÌ1ÚÖv'Á\x0004_'ÒUÚftÑJ)Ú°×ñËrÏú6óÓÕ\x000foÞ¿½ÿ¸	6[W7WÑAàu°\x0001mF×]´º¯¯^¼|üüÉí«aq	c°T
\x0013FÈÀ°FN­õñÍ°~	ëÇ`}&¿ \x001e\x0003~æ,°qv\x0014Ãå0r3lXÂAX©ù.þL¬O\x0005ÖKö£xµÃÈÍ°q	\x001b¿rÉ¦%l\x001a\x001eo\x001969ñj³µrf!_Ä6Ãæ%l\x001e-ÑnÄ¦
êxûi\x001dWS´³Í[a¡W]Cºª\x001a-dNÑRS½ÿÚÚé\x0002\x0018R\x0006q\x001aM+* |\x0019\x0004´Gx\x0010mw¿`èE\x001aE\x0005l\x0014jíÍ$Ø\x000cTá¢¸vá'úÅ\x0006v\x001d-jØ*8]O\x0001B\x0010Õ\x0015Í1ª\x000b]\x0007ëÆDr³·6OÏå\x001cd#p1nÜ\x0002Û=4úù¡±²>}ÿéíwWwWÊ/î?}Ø\x0018\x0005\x000e\x001b4¡Qø(\x0012\x000eæ¢Cóúêéó×O\x001e?»º¹zT~qûúåÃônIïöÑ§dÅ¶¥\x0010ët¢\x00001 ß½\x0000á²ÌõøivâÓ"dü \x000f\x0013\x0017ËNø/£\x001aÍq°|P\x0019ã÷§ðMüü$XníãÇ\x001fwòÓ:ÂÐø\x0013ó;q:\x0003\ÌGðw§\x001fv\x001ezäÌù[Z­\x0004{r{á\x0001£çï?ì<ÿú±ñó\x00038µ6þÏ\x000fvç\x001fwÿèx¡aåçW[\x001f!7þËõ\x0006zþîüàÞóC½v\x000f-Á\x0005¡]ß¹ù\x0011üÐá}øþø§
9S^&&~wðõµÝñ±;O@W7ÑñM¼¼\x0011ô2ÓâË£¿;>vçññT©ß×6ñÂ\x000c¹É\x001f.Ç?j~×Éßí¿\;ÂªóÃ2ôIÔÏ¼z7?.Ç@Ô\x001fÌ;Vú±\x001f\x001bìV	½ÎðfbÑà\x001fÈõ>0þcÁK^\x001cå¥ræ
bd\x0013J\x001cÒÅS®¡µKZ;,Ý<Îª\x0000C%J^AjÒµ|Ûã\x00128\x000e\x0003\x0017å8Ãc§å\x0013°z\x0011*4;\x00088-Óðy 6\x0001~´*ad&
Ï\x000b¡RÑ£\x000ep^\x0002ça	Sv/õC\x000bIJ1B¼Xñ¤\x0000^C«ßØuÄnf\x0014ð)®~U
&¼x#)^~eÙNì;b?L\x000cñ:Ävï¸(Î
Ò\x0013¶¯\x001f!å6/âÔë·p\x001d>Î\x001côøÙx¸ôñbè|wp£å EÜ4^=Ò¦i½ØîôíÅuÐ¾yGK\x0006Ûx8Tt¦d¸dq80_Tq?\=}üV
~nÁØ\x0017¼8Ì\x001by
IY\x0016vNÕF\x000cìà¢|5Àa	\x001cF
ò$ I_H\x0011ªoÁ×Å2(\x0015o^òæa^^8Wxýã\x0017®à%?\x0018üaÀ\x000b\x0005·è®V\x0013Çr\x000e\x0012¿oYÂ\x000e%ýjâÅ\x001a#
qìã3ÚðöüL\x001cGÜ)·JÝmGÖ7\x001ej7ö\x0004.æ:]ÔÉª³qÆí÷qqC<QË\x0010jùÑû[q=´|q±Ø° `>_|\x0004+¸^Þ¾Ú\x0002KX\x001c
R4\x0017B¤DYÒ.g/;DÛaÝ\x0012Ö
Â¦ë870p¿ED1\x001fÎ^®óÜ\x000e°i\x000c:ZY²uÝ`ð¤èÄ\x0001^t·Ãæ%l\x001eÍV\x001c	GsùøÃ±f@w1Ç¸uñ4@÷Ë\x000cÂz[N°Þ¥Q\x000f\x0001>¶×\x0006cê \x001bö:ÑÊûK\x0002®ð³x1\x0001¤ íÔ\x0001\x000cêä%]EÓ  °ã.§\x0016ýåzÄí´>A\x0002!VÚ o\x0013%ÌðB\x001bÑ^\x000bghý×}ÉB\x0007\x001b\x0006EkåØ:\x000cu½,©/¶¹\x0017û\x0016\x0014°±
¼6ÄÐPèE#°ÉÅ\x001f+¶Òvº\x0016F-J\x0007sQRÚ1È\x001aÚ|eèÜ°É:,½0¥é­sG
\x0015\x0001\x0007>¼\x0008Íô^ì#Õ85§Ì8Îì$uBXÜS\x001cÛÓ{ ìs\x000bói±\x0004ÀÒk¤)\x001bÓ\x000e\x0017ãéÁû^iy_5\x0012Ó%?L£>\x001fæ´KN;À\x0019\x0013/j2ÐJg[\x0010Ã{9=ò f8Í5\x0004³|\x0010¸»úÀáí¶¶òâ%6\x0010@Ë©¹\x0017 zI³Gw9º¤y´?ÐNó\x0012=|~¿ý\x0002=,ÑÃ.ôâÃ\KçÿØ:\x0003\x001ezÒÐ¡/\³`=8#ìÎÐ&ÊZa\x0019Ûë\x0006è¡BÛÒJöîÄÀ¾#ó{³»Ýíb·À\x000bh
{¨Ë}\x0002\x0015i·\x0006
{èqî¸Ã¾ówÄNMFQ2¯VJÛ.¶þ«Ñ±;î¸ë¸GÚrÜ3çè-´f®\x0007
ö·£û\x0017½à/zwW¯î?|¸¿ºûô«ço¶Æ'¶È}R3PÂT@®ç%§.ùüÀÈÍÕ«Û/o¯n^ÿùêùãæùÓ?íåGY\x0007\x0003Pk¥ë\x001f\x0000Ù­N\x001eÈÙ«ÿ\x0000KuãOÔÍÈÀ[^¼\x0000àZ\x000fX
<	ß¥p±¸wèOàº?;àOPýï?AürÐý	Â¿Ò\x0000Në4\x0000\x0017%¶óHø-×È¼\x0014zgãê¹½Ê?Ðwqy·È\x0002\x0016°8\x0006[\x001d¶N©ü{÷´h¼\È³\x0019Õ-QÝ j"\x000bT«vB«þ¶Å°a	\x001b\x0006a§²Æé\x0010\x0014
(\x000e­ÐÁ]T
Ö´dMc¬¡
\x0016 'bî\x0013r\ñb´­¨Ð\x001dW\x0018=¯òXâÚ	pv~Á¾\öº\x0019µ;\x00010x\x0004<Ð8ùú¸ãú¯¤¥É<0æé2­ûKüÍº¿ÿ5Á´lãîêéþÇ»û\x000fo¦h±\x0012ºðéý§ß&B´6â¦¢ñÚñ\x001eÑQË¤7%àÎ\Ó§·¯\x0006|=¥b?ç\x0019ut%ªµ_/]92îë¥+wÏ½tåf¯\x000eþò#Í½ûñ+\x0006¼#À»¯\x0018ð'\x0002üéë\x0002,ÑV\x0017kÐU0·Íºzùæï<úAPçLMüÒ.5Þ½\x0010k÷Ö\x0004Üy½\\x0005e-ýòñ>?zÁ:Ö4Äjc}\x0008¢5P§X\x0015V2Õ5w=
±æ5\x000f±"ÔGlÚ*ë¼ÞÂ\x001a¼­¬Ù\x001c"V¶Âº(ÌW¡¦k,VÞ\x0003XP£ó"ÖóvÞ!VèXaÕ×j-\x0012+ÛVY\x00015¥5P±CÅÑÓ:¥úëò¶©°Nkâ\x0003\x0000ç¯C¨¶Cµ£J º	ê\x001d\ÜõÊ\x001a\x000f:\x0001®cuc¬VN@
:	µ*\x0000¿Xe³Ów~ìó§Ú£V>?å\x000e(V©=wÖXCÇ\x001aFYëI¥Ùâ4P­Guþ,Z\x001bBíì\x001d³WhëDûÂ
óQ-A\x001c³z{bíì\x001d³WåZy`Ö\+I®â\x0004äó\x0000h\x0008µ3WvÌ\ÙÀ¨ÔEI¯ì¬\x0001ª\x001bàÁ¥CN«ëì\x001b³W3\x0015eÖyÖÄ
¬\x0005 C4«ëì\x001b³W.^W%@+ÂÙ´"=ÜTé#à:{åìÍXSa´Ø\x001e¯)UCb¥R ÊzP;så\x0006Í«ó£iA0ÖÒ
*
é<p}\x001fkg®Ü ¹2u8Ba
bzX¡ª¬é\x0018å:åÆLá9XHÔ¡?±úXu«·àwêÖnÈSýÁ<1þÙÝÇ7ïßÝ½½¿ò°\x0017\x0013ï/\x0000­Â[DëY¶`ÏË\x0019w ÿìæÕãçÏnÜÒ¿ðAh\Bã0´¥\x0015^U#\x0014H>»\x00065¬6!}öì\x000e0Û%³ÝÁlkJ¿@\x0017¯]Y\x0003A|Ùó¹4ãÌnÉìv0{ê5KÐ`sfæÏÆ\x0003Ì~Éìw0Ç:f\x001cHÅM\x0013s¹â0\x0017³C%tØ\x0001$ÎÉålO\x0013\x0018	ÚJ¤ëÏÕCÇ%t\x001c.á¹á82ÇºR \x0003w~Þ2\x000eÐi\x0007´½æ8=q[
1'9Ñ+­UãÌyÉw0{¶ªÏÙ¦rÒ%\x000c>ïÙ\x001e\x0006Ó\x0019\x0016³ºAc÷æb\x001aê,æìÍ¢Þ\x001cÛCkM\x001d«S7ÙÀÔQd}\x001crg\x000ca5,È\x0005í|­í&ä$¹§#åÜYCØa\x000e­§ y¦\x0011©lÃ$T<¿1NÝÙCØa\x0010)qRõt¼r°P{Iò¤#½%è,"ì0.×nÇiÏ¼ÄÐ%\x0012j<÷=NÝDØa\x0013CËþFz«gó\x0012Û±þ|òoº³°Ã(\x0006/ùõh3y"\x0013u\x0012ß4æóñ\x0004ãÔQ\x001dV1Tó\x00121×]\x0011\x001cøxÄ\x0014\x000f<Ôs\x001dø¬ù¦BðQ=\x0002µ±_\x0014å\x0017¿ò;c·ûØs³5µ\x0017t û")àç\x0012\x001bCrÿxÿáDîôQv3Íl«)d×\x000eI-|ÞuºC	Þí\x0012|9)/i\x00005>XQãÍÕ\x000fxp\x0006¿\x001d©ÁßµïÅ$nÀ\x001fÈ\x001eNÙÃ.¹C3Dò$^Â\x001cñ¾]8\x001dN3$`>7/iCB\x0006=±ñ,¿\x0007S/f(Æ²\x0007gG,q	üI[²ûx]\x0015be\x000cÍØÇp1\x0001¥áµKÞÏLÚötZ`ÈX[d¦Ç\x0008~<\x001e/=GjxÝ÷3³f¶ðf¹!9
qêó©\x0011\x000bù¥G\x0003ìÀ\x00195³%×â\x0004Úl'oÓ\x0003±hãQÀa	\x001cÆs-|,ÀÞ_s
5YÎM]ì\x0007àN½M§øs3f¶`{	x#m\x001a!Ù²i´ì^n8UmScÚ·w?
!Ë\L¥±ÖAU;xÞHW_<¹y¤DÆ%2î@\x00067áX\x0002ôÄ\x000f­®9|æs§c\x0000Ú.¡í×
ýã©ÝûíÞ{\x0019qXÀÿðÿññÃû¿¾ÛX\x0015\x0002§øl\x001b\x0016\x0018Ñ9ÎØ¢D>Wu+\x0013\x000e\x000bû\x001fn_½|þÝ³Ï±Û¿üÓÿ_?1=¯ýî®.Ö0\x0015ÒN¿PG#¡\x0011C\x001d\x001a\x0001¾\x0004µê<Bq¦n[Î¶q\x001cßSwâ«ïn>»=£Ch°\x000f!POr\x0010TW\x0012s\x0015ÁÎ%\x001fZVîú \x0002ÖÜOB<S`ºT¤H!5ë©Eh5­ÿu\x0008­põA\x0004OêvBÈÔ³5\x0011|\x0007ê<Ó\x0010?{ZÜ¤ú\x0003ñ ÿx÷ÓÿùtÿÛÕÏE\x0003Ü¼}{÷k!¹7ê¥*5a2¥I
p®¶ØÈ\x0014üñæÑ¿½¾ýáêÛ«'Onèo=j¨v\x0010ÕÕu`\x00055¦ëé;*i<\x000e!uKR7FZb ËB¥²0W
uÅ\x0003¡Â\x0011¤~Iê\x0007e
üùË?1mªB­cz\x000b©·ù\x0008Ô°D
Bå1RE¨´ÀóI­[\x0001\x000bªm©]¨q\x001aÇPc®+ÀTÑ×\x0015`$U\x0010ÔxÌ\x0001HKÔ4x\x0000êBJ#¬\Ï¤9Ç#Hó4\x000f
5°\x001ew¦ö¨OBMlPig=\x0000=D©â°T§×BUnX;«\x0018\x00158ªÐ)U\x0018Ôª1ÕAx$ÀÌÑW9«ÈjÕÙ(ÛÅÚi\x0000\x0018S\x00016B}â^ñ$¹\x0008ÅáÓ\x001a#\x001cr\x0004:\x0015\x0000c:`z\x001e\x0008\x0015#×&¡¥\x001dú´\x000f`ít\x0000)â\x0008_D¬Þ&Wgù\x000c$GVè´\x0000©ßI®ØùV8æ\ý^¬ÊÂ1e3Ôì@9\x0003>²%\x0000\x0013Õkrñ\x0008O\x0000;c:Ë\x0016OµW[Â¼P=Á\x001c#»W!\x001c¡\x0005°s¯pÌ¿²\x000ek÷¤G¹ªÊäØ\x0010|ÆÂAU>»¯FË\x00158/§\x0015ä´zpG°vZ\x0000\x0007µÀïÃj;-`Gµåh X-ÇE·%\x00160 VË\x001eácÁ<ukÖ°-ü:}-SdQä/®k»I­õ\x0007Ý\x0000íBó\x001be°\x001eýr÷ëßîj\x0006ëó
Ì×¼&Ø@óÙ?¤*Ü	ÖÌ£$\x001bì4P¶üà\x0007ÊX=úþæéK)«i­\x000c£Àhët"\x0002æu\x0016t°téV\x001fÄë¼nEÃ\x00026sÝ,¨\x00076Üy4£À~	ìGcªoí%ä¦u]±\x0002Ç:þ©\x0000ûó@l\x00148,Ã0°©Óc
pñÅã\x0006z½«Àá\«\x0002Ç%p\x001c\x0005v\x001d\x001cëÁp5IXG­\x0014à,Ü\x001eà´\x0004N£ÀÈÍ\x0005Ø`]Í]kÀmÈÊnà¼\x0004Î£ÀÆ×\x0012r°Î\x0003«`SÜ²ªÕLòG\x0008.\x0002\x0015-l\x0006!¤Ú\x000eSi\x001bg=ÃTâÂÀRÃÐ©a\x0018ÕÃÔ\x0003QýÉ©\x001cjf1ØÌÄq%Z\x001f%¶\x001d±\x001d±¹ö\x00158¦:^­Ø°\x0003lb>Ìr@g9`Ôt\x0018ê8©ÄH;\x0014«ðÙ³&\x000eÙ\x001d&âÎtÀ¨í\x00004Â:"jM	\x001e­\x001cp±N\x0015Ã¨.\x0006ÄúnW1\x0006&Oñ÷>
Üi6\x0018UmÅ¤R¦éP$wíùÞ¡cÕF¾ÐAÄØy8êb\x0016o½\x0016\x001eÒ1¶\oñI±9ê\x0018c§)pTSÿ'ï;\x001e}Ý	@\x0006Ú³ó<¥i¿6þËÝ>¾\x001b=ÉaL[\x000e²ëj@8m1\x001cæÆ/j;gÜ­¶PQÓðÅjø¬
ôå}éÛûý
ÃÓ7Ê ñRAüð¶0ÿë¯÷\x001fÞ^<\x0014ô@U
Þ´Õ\x0002$\x0012åà\x0019=D\x000bÝË'\x0005÷ûÛ§Oo_~v²å\x0002\x0012¨4TaZ]ËäR\x0013'5ÂVH\x0008gFN\x000fiV/Éhù\x0011ºH÷I\x001dæwpÀ\x0015wR\x000fé^\x000f\x0019"?\x0014ÈÀ³?JT!\x0007¤-±»!ã\x00122ê!i\x001b2¤ücò\x0005\x0012Î\x001c]=d^Bf=$¥\x0018Ñ¶\x0000Xia<WÿjFè/÷ÀíF#\x000ex²(yd\x001c?è@Î\x0007Pv\x0017\x0007\x0006n\x000eØ:\x0012(yifñaóòLÍë)»\x0003\x0003WÇØkQ¦A&\x0013\x0005òÜ§ÒCv7\x0007ôW¢À\x001f\x001c£\x0004á\x0011ÙU-á\x0000Êîêþî\x0000ÚÐXeNbÖcÓB\x0007Ø>÷\x0019\x0016\x000b\x0007T¦'Ôu£Õô8F5q6={tYÖsÖ\x001fªß|økù\Ì\x001d\x0016ßÙ³áI¼7ªa"¿.¢K+ÞÆÕ«ß=vÑÇ0ËÚMÆC5¡6Ê	&"pj\x0013,kJ\x001a¿º\x000fÏ.ñ¬\x001a\x000f©khÂ=Ì\x000cI¾¯=ÏÄëèÜÎ}uÂóK<¯Æ³\x0012\x0004Ñ^vô;kYU
^Xâ\x0005-\x001eXIúFZÛU#l%«\x000eÎ¯$G4xq\x0017\x0007¤"½°\x0013é¥\x0004¤\x0006/-ñZz^ªìbHu-\x001bIË*ôÖ¢/
^^âeµô\ºX53\x001bäÌ«kH3\x0017U¨ð\x0016IPÒÊFË #.ø\x001cøðÜÕÖñõVCo6Âì\x001bz\x001ePä'Ik\x001e¬¯3\x001b ¶\x001bèÄ¡NZ+òó"?°ûn\x0007tv\x0003ô#ó\x0013¹9g_hªy-©áë,\x0007¨Mmï1\x0011PïÙË­IkÉw
_g:@m;
\x0014°Cm¦ª*¿ÌQ\x001eíùÚÇ×Ù\x000eP\x001brè8\x001ah3!Ë/XJ(º¯3\x001e ¶\x001eØ¬GX{wh¦yÓÎ{ñ:ã\x0001jëáxÈ`\x0011ß¢D·9Zª|Ú©þ:ë\x0001jó¹Ï»VCÎ[sI=Ç}×\x0003;ójó\x0011ú\x000b\³hbÛwâuÖ\x0003ÕÖã¯ÓÎ¨ÖÎTÂ\x0016Øz,*@D¹\x0017«èè:ÝjÝç±\x000e`åËÁeá	çË±Ï­ÇN· Z·\x0004CMj\x0013Ï\x0015Î\x0019Åv8³O7ÛîôYõé+Q9;öÞ·2\x0017#Icú\x0017ìâëcJõéKN|?_{UjIjû¢JÛ?«>§P5må}6z©q£ÊÙùÓg	ß-Ü¦×ß.¾Ræ\x0016äi\À²´\x0012ñ¢_¯\x0019L>·g\x0001K0ÔEÔy.Q¹\x0014òÇ\x0010\x001bØj¹ÈV0»\x0004³
°rê[ú\x001aá"?6ÉeE·þvº\x0015Ì-ÁFb>\x0007J\x0012«­ý&ñÆIb«\x000f[Áü\x0012Ì+À¦V\x001c\x000e}rKÞû$µØèÏk±5`a	\x00164\x0012³^º\x0005SNÜÔj\x0012ÆùíáK®¸Ëæâ`r1Óæ«7âBh]aÅ^m\x0007KK°¤\x0011X	\x0012sn\x0002óÕ&hA¬_K¡l\x0007ËK°¬XqYQßg¨\x0016Ô¡D_ÏóÆ
°Enô«ÑÆËá\x0008ZÉ|\x0011Ù\x001eu\x0001½æW¨~K[Ï¤\x0003"þª/¨ÒåÌW´¬Sý Ñý\x0010£»N;©ë½4®æ\x0008\x0001î\x0007ò·4.vÇÓ\x0018¤Pß¸ç\x0002@§üA£ý¡8òÔLîF§¨fÈãj\x0011ÄV²NûBýÛ\x0014³ÔQÒ~@ì­\x0014ù\x0005·¬Sÿ Ñÿ%h¯©HfN\x001eÆÚÅ»§ýA£þ÷×¬ý½ì60ådI»5¤]§¿Óþ Qÿ´Ó\x0011\\x0017çXCNMý¯E¡ÛÉ:õ\x000f\x001aýP:<,íÆ«óÑ\x000c\x0006é@°xÞ¤ ÃNÿ£FÿSm o"AJfíQÿØû×*%\x000bu\x0010\x0014É£°uì\x001eo\x0011;\x001d\x001a\x0007û\x000b$ØéXTéXÓF6rå]ZË\x0012m'ë4\x0019j4V5Ì0Jy¤¼Îµ×ídÎ@Î(ÿ:¿¢ân×sæ+\x001bv)3Û]L«¹´ÉËhry¨\x001fÓcJÒzµãV²îfZÅÍ,î¿©\x0003¹ª3k2»ÿÒ¿y½ó`+YwÌ¬âYÚ=+	í÷e7Ûbs\x0019×²àÛÉºcf\x0015ÇÌÒf\x001d\x001e¦â\x001d\x000fe6¶uø\x0015\x001fc\x000fëS\x001c³`$1CÊëÍ´Þµ9/f÷ãºcæ4ÇVòzöÿC\x0017?k¤\x0016ÃâÚÐv²>¡Ð³6«diÚ)Tn%³QÖÊ0¶uÇÌ©< `ëÄ\x001aðÕ|³{Î\x0019¾j²\x0002Ë²è
\x0000¥\x000ccÃ´bÎ°öL¿\x0001\x0010ÝI¢±\x0018\x00146_Þÿúéîb3+Û\x0015\x001b-ÿ>[ôp~\x0007^Þ>}}s©p	[pjz\x0014¿ºÜ¾")Ø­<vÉc7ó\x0004ÒY" ,Ï'Íz³SµÇ-yÜV\x0012À\x001cLzy\x000ekc´üy¿éV ¿\x0004ò[\x0017i-p¿åwæÅòj °\x0004
[b{R"E\x0010Z¶\x0014ò{w¦¢¶\x0002Å%PÜ\x0008D]â½\x0019	²ÁÌ_,\x000c ´ÄI[q¨­ZÒ÷w	\x0002?Ø(Ð"\x0019G:Èl%­8;ÁyàÍ,¡ÑK\x000f½VÜª\x0016i|Bà[Osµ<\x0013É\x00088ç©Á­DZ­zÑÓÈe\x0005nª\x0000Ë3Óð5N1ÂVÍè²\x0013»ãg¹Í#Û³­Dj­ºÑËz\x0018"²\x001c7(¿\x0005+H[:Ý\x0008[£§Ô¼r\x0010"+_-ÏçÚJÔ)GØª\x001d½\x0003yð¤Ôr}ñ©/c,£óÇ»­Dv­êÑËEk«­\x000bø\x001fö¼6f+Mîhò-
vz\x0008·ê!\x001f°èÅ¿MÕ¸NÚÎË\x000f¶\x0012u·\x001e·Þz¦\x0005W\x0013QñÏj5ÐüF	\x0000âÙþV¢îáÖ;\x00160¶\x0011xN¦M-ñ\x0012\x0013%£·\x001eætî©IËv»«?\x0014»7ïî¯Þý|÷ëåòÈÄöÖCÙÊ_­ä\x0019mX{2¼zrsõò£ÇÏn¯Þ|{óôb-D:ñ¸\x000b.\x000eâ\x0016\x0007\"\x0002*.z&cÏÕJö\x0001\·Äu£Òå!ô05Grz¡¨Öù\x000eVkO5´xÚ°,ä(\x0007ôow\x001f>^
ýÊa¼\x0002ÞÀC¨pMªïW³Yå¾¸yùêbäwÚ°¬äØBæQ²\x0011\x0014×%+åM+]R:6»d³*6\x0017|ë#¥Õ¿pò \x0007qýÙl;[²9\x001d[\x0001JRÓ\x001exÛ\x000e\x0010[Y]ZÍlóK8¯±µb3cà¥\x000f
Òú\x0000ípa	\x0017tpÎRª¹µ¢D\x000e?Z±îÎ\x0003\x0017hQZ\x000e5Y¦\ÎYë[6;ÙÒ-)ÅÖüÿX"î(bg4XímÓÀå%\VÁyïx6A/C±\x0013ÍË]O
nf[ÆÐ\x0015yl\x001cÕ8ñUM¾A+\x0001ïWóÛá:õ\x000b:ýK¡/ðëqÜUY>¦ôÒõÂ°íp\x0003¥KYr_¤G@îõÈNºNNxÅQI^¥©cV¢=8Ñ«£ë®+èî«/!±fÊJfEØµR\x0005\x0018v×\x0001u×ÁÓ ÓùÕOBÒ`\x001e¨zÚN×»#J$ÚÖëDmÛ¼C±\x000f+c\x0019\x0017b1¥^;Ý
³SR0\x000c>H~\\x001f´]\x000f÷£*'_sùÎ°Ú)Ù©#(.
÷âÕÑF\x001eç)#j\x0019¿üNgrLZH_b!öURQÔ/2:¹É8èåýx:\x000fæ\x001b\x0007Ó­¨yñæþÃÅu\x001f\x0001³\x000cýE\x001ab\x00128ôª\x001fïû·Õn\x0017ÍÇ·//ìþøñt\x001aÌ7<
Fè}â\ñìd\x0018"eâø,\x0006×7F\x000f!º%¢S#rtQÛhÅ\x0007[\x0011ûZ!¾°ä\x000bj>¼P%H³\x0003ù#ËZ\x0019è³\x0007C|iÉÔ|!ó³\x001b´Ï'0ì \x0018!l\x000eàDH\x000e \x0016Qúß§SÂhr;û\x0019»»\x000cêËì\x000bI\x000e,FÓüÖ½\x0010Üî\x0008ÝE\x0001ýM¡ömF,J;ó~¡häSÓ\x001bbì.\x000bèo÷²\x0012Åâ,Æ$C°¼±»0 ¿1EÓÔ`Î3HÑI½Ò\x001cË\x0005ãv\x0011»\x001bú\x001b<Ïa\x0006ðò[J\x001dk\x001döë\x001dì­þÆäv«Ñ;Þ~S×3UFªåÜËØ]\x0019T_^¶\x001d@\x0011)G6Ê\x001e2à|±»2¨¾2ÁÆhä¨
s¨'{\x000e\x0018»+ê+\x0013-ÑËk#½¨\x000b£Ý}­mw\x001e­Þ\x001d+$¡\x001aBð(¯ÆÎH'úÉb!Äî8Zýq¬E²å,¶¹¸¶r_ß­wlw\x0016íÀY¤â6$.¦c1£ÃzËIÂ\x001c&¯ûÑ/÷¿N|<Ýò\x0002\x001fdQÝ¶è\x001fiÒÊgRèß\x001f}ûtã¡\x000fÃ¹%ÓÁEàUÓêX2-S±]ÿ4§G\x000bK´ C£Î\x001a7;ª¨¨hÆØNê\x0006õliÉtl¶
àp&_K#\x0011¹!²YsrÞ¬éßå^Ý½{wÿáÍåÀ\M%®çf\x0000çæ|ÃúûÖ«gÏn_>¾t\x001b¬99pÖôÏp\x001bè\x000cÕZò[\x0003\x0018®¶2å\x0016ËCÈg\x001a¼5a	\x0018´Á´9\x001eíãH\x000fa}¼.-éÒWF·È\x0017ºåè¦mxÖI'·ò\x0016ì]nù\x000fX\x001d­¢\x0001ìî\x0006h/\x0007µ
 üs×6p«ä2Ïç'nç³'Ï¾Öò³ïÛ·÷WßÞ}úÛ/o\x001e¼12H<ûÀäh¼2wúðû¤³oo^¿øþñÅÑ\x0002~¹\x0015½þ@\x0008©ýøþÝ\x0005*,ÿn®z\x0008\RRþq\x0016fV&¡\x0016\x000bûêù³â\x0012(n\x0005²AÆ\x000bX÷\x001bÛô-8ÿ\x000fâ¸|¢vw»0óØ!¹¤t\x0003´F4^­Ò¹Ó¯÷åÄ&¼foä½:--©´äÅýÇ7\x001fï¯È.\x001d)ð×³¦´ß÷´\\x001bBoF_Ü¾züêöª\x0008ía \\x0002áV ke,cL­»)S·\x0015¿®õk"4@n	ä¶\x0002¹Èá\x0010È0¨V0E±õ(OZò¤­<%ÔçVHMæ^ªÛ\x000b·@ËÝ$iÒíÛ²i\x0002\x000cðø\x000e Ni!\x001aþdÐ!Øz<êØ*¤9Fç\x0017ö\x0005G\x000b»\x000f?Ýÿí³0Ýù­\x0007ÈQ¿*÷8Bæ\x0002{h­÷ú8S#Ð\x0001­@qêQÆ­P¹¶Ô³cÒ\x0013aìrûÓ$®Îyu÷ã§!\x001aÅeÁ¶R\x0004Ïó_@ÐÃJÆ«o^_ÌðtÅ\x0015¶\x0015W\x000f\x0003An@1·YîFr,\x0005è¬Âj+P\\x0002ÅÍ@ídB¶ä¥öðä%OÞÈ\x0003Eó$l<À.âB@j\x001esºôÍ´¥o¸ûïwp\[ÊR\x0002gqBv"\x0007ò?Ü>ùo7\x000fãØ%Ý\x0013Ls¸\x0001*¼®9¯°ÝÈâ,n#7R\x0014±Í©/.£ý¬7´Æ/iüVÉ`\x001b|k¦-/Õ\x000bbÍCÛ1\x0006iâ&n¥É×²\x001aÖ[JzC®ñç+©6âä%NÞ\x0013ôóâtÈN¯6Ö¶Ä\x000bgjp\x001bÎrÞî¼tìañ´\x0019Ï¡ü\x0012¤\x0001RÞ¸\x001b\x0015Ïr¾nlM4\x000fòäÖ\x00186Ímd¥ÓzhÊo;ÊÓ)\x001dØªu¨ËÈó÷²¢u¢5í{ùÝÈÓÝtØzÕ\x0013p_t,´Qbÿân\x000eÞ­å´×Øª\x001e¦ÉÒ;\x0013L+û¾mYÌçmj\x001byRÇ¶ñ íÁâÁ)5\x0008mpày1æ6\x001eìn\x0017n¼]\x0008 &¶PÊ\x0010ÄÍâ&\x0007?ÊÓÐ§\x0019±å,©¢+Êª$\x000bÝùnê<ÝiÆ§\x0019Q\x0000¬·­8Øvj\x000fÀ¿Ìó£q}öô\x001bjö/âùãÝK\x0018ÿâÃû\x0017cxGI\x0017|êÈã<yZÌ¶´JøãÍËoK\x000cÿâåóW\x0017\x0002øåXNåÛHLÊw8®ämå%ZÍz¬Âsº6ØÍk?]}÷á=õ¨ß_ÌXSN'©¾K¶ÚX6\x0012Bóvµo__}÷ò9µ©ß^\x001eyê ¹æ mÅ£OW_ö}¾æÎ5àQ\x0010ÂÊè1\x001d_Ây\x001d\0Söè¨þ\x000eøÒI­X\\x0019"¯£Kº¨\x0014]ö<·­ÐVæd¥l1®Ûéðò\x0012/ëðb	)ëÃó\x0001¸Ë¾D%rð[© ßgN°8xÞ_¾¬\x0006åE-qyñ¡¥¿ÃyçÎë«GÏ/ª\x000fìçÂ~C}oå·i-OÓ\x001aò¿ßÿõÃý¥7«LK\x0001¦Ë`y\x001f \x0014Ï|ÒmåòÌûjÝNß^Ýüéö»·\x0017_ÔN\x0007JÀ4PâÅÛ»$5ÿôîÍåÄ<-Aæ<\rÒ[þÁ¶Ø¨\x0014õâÉÍ#ÉÍ?½y|)3gNñÜºçIQ¼¿ývÿëý»WoE\x001a­®FµJ\x0001DI>º¾\x0000¢¨â\x001f~¸}zûìÕÕÚ\x0003ôOw?ßýö±ü+å\x0017§ènîv¡Ch*;\x0005VÅáÂ6Ó\x0007»ÉÃ<ì!÷yÚ\x00079©s\x001axE%µºÆ~bénô´DO»Ð#!zºàÃb¤Z&èª½Ü-\x001a¸§ÚÇqpê\x00016¡HyÎZ\x001c'ãÖCè{ew³ww\x0014v]R\x000fÅYb¹Óä2blF÷ý¬ÊÝèÝ\x001d]AËOaªò¬M÷®ÕMÂ±ìÝ-}×´vÂU0ç:±{yÀ8õ	w³w×\x0014öÝS¤¸{fïúyà{Ñ±»©¸ï¦\x00167Èa3Iì{`j¥ý\x0000ìÝè½1ÝwQCæ¿\x0017À%\%þã\x001cfù£\x001dËÞÝTÜgNôõ:¨\x000b\x000f«\x0017?kÂ¡\x0000v7\x0015wÝTr\x0005¼HÎì^RÙ.x8½»©¸ë¦\x0006DCH4¤\x001eþt(¸í\x000e»Ýç:FàîÒ)?]\x000b\x0005ÈBÉücUíÎºÝwÖìq(Ç\x001bePCú\x00148Ö¢Úî¬Û}g\x0008Ù*¡Ìn,gÇÇnû*Qvc<\x0004CÅ»+§ñÉbHÅ¦Í\x001b\x0007µ
©Èº®`êcJØNÖ@-GTÌAÛ:'þå§ý¯RX2ñÝÿvõßß¿¡ò)J\x000c\x0015êþÃ¯ÿù\x001f\x0013V .ÆiQ2\x0003®óã\x001aªlâ¢°úöåÓÛÿ\x0016ºþ÷ç©zêsAdÇS®\x0017ªxLMü\x0016k9PÁ©ãG
wûpÊ±ð\x001abÁr\x0015\x000f\x001aä!¹ÁQ×ZåsÞw§\ á©ï·'Q\x000båÄÃÝVÄ÷É§øÿQÅãk9Yá)ö§fn\x0002*8)î\x0013O±*Ií´÷wÂ±Så
á\x0014\x0013È+-vÏðPøUÛÏ¶\x0002\x0015yòãÊ¿9 ò, ´Ød2\x0004D×]sß3oï.<´¹¬~/ÏsË\x0007[dxÊ]\x0007Å}§	¨Ô0\x0001e'@Ñ;Ö?ÉÏ\x001b¬¿\x0006V# ´Ô2]Pâi\x0016¡8­V÷»Ê¨­w\x001b%\x0004&W¿.\x0019j\x000c¬\x001a1ñ
­Â³j7ÂCõÙ¨\x0010P$C&\x0002Ê'\x0008H{îøá> ¢P¡èÕôÚ§* °Üc\x001cb¬Í\x0005\x0005fí\x0001*7þR|1.ú£/&[ãe¢2\x000ehÅÅOÿô\x000b\x001bÏõ¬/?}¸{K^ÓÓ»¾ÿôá\x0012÷%0Æÿ\x0015»e
JQëéDV3\x0011\x0013\x0019\x0017¶¾|ýòæ	ùKOoþÇó×/·0V»?À\x0018¬«È\x000bc\8àBªé\x000b£t\x0010c9\x0016v1çZQU\x0018Cà÷\x0014\x0017c}*vÎ»îd,'Å}ëàê¬nòQ\x0012\x000fv'¯\x0017F\x0007!V\x001ffPÞó§½ä$F'b<êKW?b\x0004±ø£Ó@júÒ#Ó\x0012JÛö¥OÔï8cQ1ù+¿1âÿ|\x001fÿv~ù¿\x000bõH/|\x000ekxöÍ7½#Î7ÿøH´oÿz÷Ó/÷x§\x000eè©ª´\x001cGk¹ÌÕ"O\x0016L)\x0018ìU%=ÿ9¤hí¿»!âÇ~EÜO¾»)-äU!í%§AL^¼=ÇäÀ:ÞG\x000e\x0007¯Zj7x¬Î2<²VµÈ²HäÇK¼Æ{ÁCÝq\x0011ÉÊs[Eã»¨b8\x001c¼*ÝÝ\x0012\x000fb#bª?P$.g%ÐcþÑä5ÄÜ-r¨³oÌëV\x0016"ØºùE\x0001ÔaäÕ\x001c s\x000c,sGÉ*sÓ\x0014uWÛ²Üqf¿ÈÜÊöK\x000b¼.´ÈÆ\x0000\x001fL.\x0016g·Ð}]\x000fBBGHB¦Í\x000f¿¢\x0012ïzªUØEê(í1\x0016¸:¡HÝ¤Ä@ç0þ\x0000©Cb©\x0003UoWK$.h0æpS$\x0001ÿn©ÇëÌ:\x001d
çEIê RÃ5£¤\x0006\x000e°ÿâ¹ L.ROì²úEçaèåw\x0003\x000c©ã7¬"uã¸¬µHÝK|âñR/f\x00140¥®ØÔ\x0013OÝ#¯K®iNx8z\x0011\x0006\x001c`K\x001d¶\x0018ÇgN*[\x0008¢aÜbrÄaèåâÃ\x0001Æ*{\x0003gçÑO£\x0018ÝãñÊ±üp5Ú»NñyäQT#\x0001
û\x0001T\x0007XSµØÐ3µyT©»\x000e·¦dñ\x0000kZ\x0002PM7³"T(Ç&Éæt¸¡z
<ÀÒâ\x0017IÞ¹ë$g½Vo\x0015©£?\ÃHvx÷Yçg¢\x0018]Q6(\x001a&3º=
þ@/æ\x00080I¿¿r¤Ì\x0002\x001e`0×\x0016¬\x000e[Âháblo8þ¬söþ_Qêå\x0008â\x0001&IÙËY§9º8\x00026ãñRç'A©ÓjX{I*RÏÀRGî]YJ=Ã5\x000c\x000eÙ\x0003ô:ò£uAO^òu\x0005Ý	º9Ü¡\x0014= Ô¨oÈ\x0015Ýòj:é®¢Çt¼Ôb´Ç(ÇÀ×4vÖ]\x0012©/&y\x001f^apz
Yÿ	=Zzû¬è9	º9Ü\x0011 Õºî\x0008Ïñ¿\x0000½üî\x0008÷ë÷Gç)æËÙåÿbÁ\x0012Ï³_L±ß\x0015cO%S
s^2\x001b)\x001fÅËü\x0007ÈÇ|,	\x000eOãö&ójÅ¼¢9>Ûn+¾=FþuU!»öZÀCûø7±&Vüx\x0008¾ëzüC½%,_`|
\x0018ùôã1Ç¿Ä®­m\x0016v\x0007IbÛä\x000fº¿ÿ°áîßÓâIòß>Ý}øøæþÃÕÛûß®¾¹+}úøñ2\x0018ê!öº_gÏ«"øª0³5'iÈ{}óòÕãÛWT\x000eóÍMùëõ«W\x0017
bfHK_?%û\#6N\x000bxO®^ÄP¯^Æd=
³üyé¯!ÌÄã@	Ó×Zµ<Õ(ýaì\x0005~ÂtéÇ_¢ÎYOÉeú§wo~{ÿîê\x000fï?ÜÿF¼÷W~ySH¯\x001e½ûöþãÅÒ	G;\x000b&£MH4ÅJ'\x001cwy&\x001ao×Ñ§7xþìê\x000fÏ_Þþ@Ü·W¾\¯\x001e=òäös/Üô`=ýÇ¿\x001a7½CÐüKpÃ»æ¿å®lÿêOoî?ýãª\x0016Ø\´\x0006Á\x001b±\x0006åHs¡¥9HÕ\x001aÀé[ÉÛ«?=¾}ýç«ZY³ª*ÿ¯ª\x0016|mTRÉÿuQÕÿ¯j®Zÿº°Z­øWõËÏoÿßO[èoî>|¸ûk]^õíÝ¯å?É{¼ÿôÛCyP;Xb4Î«396bN®÷Ú¿¹yùòæ»ºÉVãþ0\x0015ßÝ¾þáóîâ\x001fÌ¯ÿù¼4E\x0014W÷ö¯oß\¦ô)N\x0015ªÕµ5ì{jâ`×ÖDvm
ûÕ«Ûï<¾@çÿiìÏ]ÐÛ\x0006é£û\x000f?Ýß}úÇå¢Ú(¹ºä"ò&!Z«P\x001f22µ¦=`\x001aH®n_>º½yýçÏ\x0010ðk®ÓJ¨	þúÏÿï§·å[L¿½ÿûbÄ.Zãc\x001dóJåQ±-¹
4F8I*Þ>zR>1	ôÛÛ?=.fë³léo?\x0008¿,Ûsè\x001bÿíÍ»ûb_/Å\x0012ÔùÅÈ<\x0015Ä\x0006©|:md¸º}ñøÙm±£í{óÿnÿñÎ/\x001feÔÿ?¿wÑ\x0007t\x001eÿj¾Ø`æÍ¦\x0018óµ\x0008+0å¿}ûüÙçÛðþ×¯ù¿NÜ]½|ÿ÷»g
s{¤v¡Ú´ä7§0\x0008ææêåó?Ý|\x0016ÃäÿóÓO?.\x000b\x0004^üRBÍK\x0010¡x:¢Ç¬O×ÜÇÕ\x0010r
}ñ}	'·\x0010ð;ÿ\x0006\x0002k¥XÈ\x0006]&\x001co¡)\x0004']%[\x0001äÉ{\x0003º\x0007\x0000\x000cÀND£"ðÝü²ú\x0003jxüëßî~ûílÎçªóíicÚ±0TÓ¢þ\x0010O¢ÇO_ÜüðÃ¦q:\x000bL·Ät_/f[ëØPé\x0007zÚb¬c}tTv\í6õ¿1.Mî\x001aÇ-ÇnÑ7\@¦§«o®n>¼)v§ ~óáÍÝ»/ë)g®ëµ,'¶XçùÝ<$<ËN<¾ºyù¸Ø\x0002úÍËÇ7Ï¾}Ò.)í\x0008¥\x000fuÜ\x0013}{Ïã\x001a­N
ýâI±ü\x0018§_rú\x0011Nê<àÒ¸Ü
W¼AVs¤ïçKÎ8Äë \x001eâÜÒV8%Ñ\x001dü1Æy>¶p\x0016ÉâôßÐ\x0002â~JèïÐÈ%*þTÎDÊ\x0001Wc_d(\x001dÜ\x0011 Ý5{Ç°R\x000f\x000c´>Z¹ï&\x001ep »G0r\x0012¥¢¥;ÆIñì®ª\x001d\x000fPLÐ]$\x0018¹IÉ¡tê\x0015\x001dD¾û\x0004\x0001\x0005\x0014\x0000ín\x0012\x000c]%\x0017\x001b($^®Y@å)½Èö,)©\x0007Åî2áÐeò¶o'Pé!-\x000e\x0013Ð\x0018\x000eÐ¡Ø]&\x001cºL%\x0004J­
û,\x0002´nx\x0000ewpè&É&ljdR­\x001d¬4=y\x0017ò\x0001 ¡\x0003
\x0003 Ón\x000e.?\x000cÈ+»mªòâ/\x001d!ÐîÆãÐÏÆi×g>äµ 6\x0004ÉÈø#.¼5ËdFäYÂrÃ}\x001dåuÄ
1Hu\x001e-=Ü\x000fÚ]x;rá3Ä\x0016µÛiÕFýð­*\x000cá\x0013j±\x0003ÅAPg\x0019tb® Yê\x001bNØ1P×º¯õ*Yó»Cz7jsëtOòñÅÅs§	/\x001d«µ'qµf9¶úþÝ=·\x0018w÷éW	@§n×Ön¸e×woVê+hðí³[n2þîæõ¥ÔWãÅ%/òzàØnZÅÆÙ\x0014¤"ãy=Å\x0018®[âºQ\¤;ÜJ,C\x0014Kà¼¯h7,yÃ(/â5Û\x0001Z\x0005Æå\x001e®uå\x000eÑ1Ü¸ÄÃ§×Ì§×P/Q-n~\x0010óyAâ\x0018o^òæQÞ\x0012£rÊÚÌêü8*Æju>¯\x001bâ\x0005Ói\x00073\x0008ìrë\x000bä\x001aò0^îÛZÃÍ\x0018p¯ÎõÙü(B\x0012®3å[ÁR^©®\x001d\x0003îô\x0019*´âÌR(X]¯(3\x0013Ln¡\x0001®Ô\x0001Û\x000eØ\x000eK8¯HM{­ÿ\x001dç0ö¨#Ñ©`\x0018ÕÁÎ¥f£lï³Æ&é\x0001òù¼\x0004l\x000cØwÀ~XÂAZ
HÂ(Z\x0002;ê\x0008w6\x0003FsÒÿ¤ý´øÐ­ÿá°ãÐ\x000c\x0018¶\x0019´^R¤\x001b¹x\x001a¬[ÓéJ¿ì\x0018pêÓ¨xi2­Ä\x0012¦	L\x0012¦ÂW%V:\x0007±3\x001a8l40Óã\x0001i\x0002ù\x0004\x000cò¬áL<
¸3\x001a8n4ì|$ä\x0010èà\x001c\x000eÒ\x0010Ø;ÁÃF\x0003t©Qç\x000eW¥O¿=Wµ®´«\x0001wF\x0003G\x0006\x001d	Ãý:ÞHiøÁÖÃQG¢3\x001a8l4#2·º8®g³SÔÅ\x0012>ÈQÃÎfà¨Íp¾¬P@ n%C&å ÜÎdà°É@#Û\x0012\x000c3.\x0016o]ÎÃQn%vF\x0003G\x0006m 
¶e\x001fÄp­ñÜ¯¶\x0018\x0003î\x0006\x000e\x001b"`öÒÊÇg/\x0004,÷í(a;\x0015lGU0i\x0005Iï\x0010Í\x0018'>ÏéÓò8o§í°\x0006,íü\x000eef¯ô¥X<êÆÙN\x0003Ûa
L}ªU¾è%R6¼\x001dò|G)4Û)`;¬¹²ÄA ­t,`\x0019:°Òy2ÆÛ)`;¬ërqzDCðÌÙ#\x001eÛ©`;¬!És¤
\x000b
ÑjwâQ§ít°\x001dÖÁ\x0016ifY5ÉQÊFKX+'"\x001d¦#ºd\x001dÍö8ê¯f\x001dá¦uYìôH»ìA>ëÜv7ì¶\x0003ÁÓxlu×¦\x0003ÑÞ,Ð­Lo\x001c\x0003îl\x001b¶\x0019\x0003{GÅg"ßÖ\x001cÌQ\x0012î\x001b7\x001aI^lÑiµ¦$Ì'¸(£;£áv¹í|U^qÛ\x000fºq®Ï¶\x001bt]qi0z}\x0017.ò­"\x0013\x000eã\§Ý\x001e\x001dÌ5`\x0016Àí@îâ1àN\x0007»a\x001dLù(ÖÁ »ßËð¢á(ÇÝu~°\x001bö!×íDìQEÂâ\x0008C>êEÃuFÃ\x001bHÏZÈSqm°ãÐ\x001eO«}g6üx¶§
,DïÙ ¹V	\x001få\x0008ûN§ùqÖò×%ÊlÁæ÷¸°ï<K?ìY\x0016`Ml\x001avÊV`ïp§$ü¸£¤O\x0000ç=íÅQ÷o\x0008ñ ³á»;ç÷Ü9#v#óþ
;=Y³Ý8JÂ¡ó|Â°çÃ~0úÜÒ«&¶\x000bwÔû·ùñäÎý¸ãÒ±SÏ°NÃ¢£Â|wÂ|7Î\_\x0012-M\x0007C!á\x0006¦Ã\x0011½qTÊËÇOZ¢!\x0013{]Ø{ÔÓ\x0006H\x0019wHù÷Ê\x000c]öAð\x001b¨øAy\x001cÌ{\x0007v9Ô\x0007zäit|g#S>ÂQÏÍæ\x000cÛs»)À¸az\x001e­­2Ò\x0006Òyx¢ópÎû½Nvùe\x001bG/#ÍlÃ\x0002
svu³Ô§¤£OÀ³Ó_óé\x0008ÞõElå\x0007çi/ßüýþíû\x0007Z:\x0003mÅ ªõQy\x0017%UhÝIÞ¢ï£zùøO·OSç´vIk\x0007ia\x001a>*\x0013tª»á]­Íø$FUÓ;qRÐhZAãíÇ7÷ïÞÝ_}ûþ¡	\x0014`@új¦BzÝ²Ks
ó¹×yûêñí3Z\x0017ùüÒÌFKBÔ\x0013º6¾¸ÈuñÍ­øËÄs¡\x0004´K@«\x0007v\x000f\x0008yälöR\x000cêael¾Ð-	\x0010,ZGÅ\x0012\x000c­\x001cítòÐ\x0000 _\x0002z5 ÚkÇõrûíÜ²òh¡Ä\x000bK¼ Æsªæ+\x001f°Sëæà×ÃÊ» 0.	£Ð{)ð\x0005Ï\x0008ÎÌãêN\x000e\x0000¦%`ú\x001aEYM¸h4sÓ^£J\x0008­¦\x001böjÂEy©ËK\x0015Q|PqÍ=ïWÒ´J¾ÞèIqÙD\x0017\x001b³s\x0012×-ÀJ¸ª$ìl	èIBÚ¬V+Ë
m$\x0018\x0010\x0017Ë?ØÚð?ØY\x0013Ð\x00134mSR\x001bü1+Ã+³\x000fBì¬	èÍI	ì¥Ü=É~5ã[¡¥_)\x001fW\x0012væ\x0004ôö¤(Aa2Í$G.qëvÄÎ¤Þ¦¹ñÚ$®OtÆµ
æâ9%agR@oS\x000bË\x000f1y©±ÎA\x0006]\x0017ol7bgT@oU\x0002.úZ\\x0015¡õNâ.s\x001eë\x0000±ÓØ¨×Ø4ád.Jv(\x0005q>­\x000cÆW"vJ\x001bÕJÛd¤qÚu¢B¤±½5\x0002*¸\x0010V"}\x0004 ×ÚT¦×úUê{_ñnæåÝ\x0007\x0011;¥j¥]þ\x00146%ÄvW¬\x0017çát,Å\x0000b§µQ¯µÂ±Ò¥¹ä\x0014NëRÊ»b§¶Q­¶M\x00082=z¿9yLæf¯ÖÆN'¢Z'âÖÈè\x0019eåBÊ2;\%b§\x0013qÀÓFÉUÆ"DqqZ}G0+i\x001d%bçi£ÚÕ6%Èã²Û\x0014²¬ÆIÙ0baöJÑvZÑêµb	Rl
êSqwØHmHTÝR´V´z­h[R:\x0016;h¼\x0004,mÖÈJ)\x0012±ÏèÕb	¤xCIJVúdK@Àq­	CØ©E«WÖK¾9\x0016õck\x0012´\h	ZpwØg;µhõjÑ&Úh8I±\x0018kÕ¤}?®}+	;gÖêYky-m\x000cIGr\x0016Â@õ;	;Åmõ»\x0010:aëp¤y<,D{s`¶SÜV¯¸1´ fÏQÂç\x0016´¬>ê\x0010]§r^åØTö&Ó´=M÷\x000bÑõÎTg¢iu\x0015Ê´Å\x001c¥å ¸ÝÝ]qú»B52\x0019l\x000e«b[÷íâ^Ëâºèô'ÑLÃ!§ËR~É\x001d­6)ø¼×°ø.®òú¸ª89²yÜË\x0008rräÍ\x001eV6x+\x0011»»âÞ-ø;'0ê³U°ûYÀwÅë/\x0001\x0019c Ë\x001aôìm\x000býöèî¶xõm19´£8OÕÊN\x001e)Kpº\x001b±»-^}[(ö«\x0003pc*\x001a%ökÖo\x001fº\x000f\x001dÔ\x001fÚD7´âÿ\x001fA¦&F³;Û\x0014ú'\x0016ýöSæTMmÊ[\«V\x0002v9è?s	¦ø¿\x00012 3¥Ü\x0010Í^ÄØiÅ¨Ö%êµK4¡(W¼ô"D÷z±ÓQ­\x0015
\x0002¼	&çTBçù:S\x0001Å^Âî®Dý]!OÑ²\x0010Ìk-\x0016E\x0010}Øû±-Ëé\x001c)ãÐ¤ÅTiÓðV`#\x0008¹MíØý4~Rpbº¯éÅà¤ÜË,Ë½¾®j\x0008{
jG@mÅ0ç¡rXÁ£\x001f6þ´°ÄÏ%OÞzó\x001b­úéû·\x0008]H\x001e5¦kDóx]AVÏxNøäùëÇ?Ðî¨Gßß>y\x0010¨%¤\x0011½|}2M®c0¥j#­=÷*ùìÏª%X>,û\x0015$A>Ö¹6­}·\x0000Ã\x00120¨\x0005è£ä%r 	n\x001aÅ,#AY¹ÕJÀ´\x0004LzÀ\x0012_ñ\x0017\x000eI
Ü\[`åHG8?éûÅ¾\x000e1æÈ­A\x000514Ä½Ç\x0010ºk\x0002ú{b¥¢;Ç¶ÖÃy)ÙM°²\x000bNIè:B§&\x0019gÚ¸U	\x001d´Ï¼R©$ìn
è¯
=
±S\x0011³¤]÷p%^U"vw\x0005ô\x0005æ[Ç­CtMaïEÄî² þ²\x0018Cõ\x0015ÑËÄ\x0019òx\x0004ñ<ÐR\x0012ö&E}WJÀ,é§Ìc\x0016KÕ\x0014öÞÝEAõE		Û7ÎF&ÁÚ6	:\x0011÷"v7\x0005Õ7%\x0014KÂ}:XC\x0018ë¥U2­5û*	»ê\x0012J\x0008\x0003lU¢A¥e²TrJ\x001d¢í.\x001d¸(-ÛM\x0017\x0005Y#¶Ó+Y\x0013%bwS¬þ¦¶aÌáqm±Y!%awY¬ú²ø"9+ß\x0019hLÅDè\x0008+{»Ýe±êËBí4Q\x0010te¢\x0016¼b÷jDÛÝ\x0016«¾->¸¥Ã^ì¼Ê7ÁJ)\x000eÑuGÑ©¢÷(»ås\x0008\x0012ª@vÍ\x0007Ãó8ZØE§?¿\x0003bw\x0016þ,r»C¦°'\x000c¦\x0013×:\x0015|ÝAtêèr«ï-\x0001=5_O u\x0011tÉw"úNm{µÚ¦éì(®¶F"\x000bGv7bwW¼ú®\x000brizH\x001d(\x0001|\x001bA¶\x001dÓêí¹/5÷Ý×'HÄ\x0012QObËÒkj\x0014xÜve¸ösw[¬ê'tæ«£4LCä«Ëõ¦
¨QÒpn
sºéÅÝ§·Wß¾ÿôëý\x0007ü õ¾åïK\x0003Éìï´R
óâæõ«o¿~zûòa:\Ò¡.ÜÆ\SÞÖ·Ç
³ÉQÑÙ%ÕÊ.J] É7áðEvç7ZEçtN);\x001bÚ«\x0007Î1YZ½ÝÊc¹
Î/á¼\x0012.VTb-çµË\x0005**ÚvÑÅ%]TÒÍÎaâhÞ¶¯°6ò_hIûU&Õ¯ZBRþª(\x001f5ë=\x0015[^²eímµ× \x001fUvr/Ò®!¯¼\x0001hèæaX¤\x000c7ãÑ\x0010[ãð\x0018Û©¸.TÁõjX©\x000f²±)Ù¶vÕ¶z\x001cÎ#c\x0015]§è@©éó­¼ØÉÛc[xWF9ªØ:M\x0002ZU@åTmÊZO\x001f¶õ\x000bG³RZ¥Â\x000b\x001d^Ðáùlé©\x001e» ÇÎµeXÉ
ªè:E\x0007ZMgr+t2®ª¸{¦7¬T}©ð:\x0002Zbô\x0013\x001eß
\x000cvÆÛ§ï°»´¨½´f.lpQ¶.aÀt\x0014^wkQyk=\x0015ÉÍÒsãðMåíÆëü\x0013T:(ÞlU#¥"³\x001fÄ{f%±¯¢ëÔ
*ÕÏØÐ\l\£×]\T^\Ú*\x0000ñÔB"b<Hëaç¥ ÒMñTÖ,\x001eTÛ\x0007¡³Q\x0005vj\x0005j¶dñë&<¥Ó²hVÚe4x¶sT¬ÒQñô('¾\x0015\x0017àSn~Ô¾ok;­gZÏ\x00079w¦©<\x0013w¼²QHÅÖÅV\x00190zh« ($2­74ä.e\x0015^\x001f0j52yyÐ®\x0005Oì\x001bÞJb\×id«ÕÈT½ÌÒC/;ï\x0000exeH+Å*¼N%[­J&\x000fEÊE\x001d½0Lx©\x001bËv'^çéY­§gÚK5u2r³	´5:!­äëUxÅ°ZaÛüí)ÓÃæ¶
iÈ;Í­í\x000cU\x001a\x000cÊ1Ã\PÍÍD\x0000-\x0000J{/ng1¬ÖbX'j\x0012¤ÍbÏ¤50í\x000c¼]g1Òb¸\x0012d^¡9ZüÈaZÃy\)GWáu\x0016Ãi-ÆÂ \x0015½AõÊNéuFÃ)£\x0007}\x0016o/DFJ¼ÃÎDëLÓ"0ÐÐÊPwðØjäW!Tx}Qi2(©-<°\x0012cÖÖ»Úe ÂëLÓ\x000c­E\x001f
;\x0003ÐrÛ+5\x001b*¶Î^8¥½p	µ¥%Ý<ð3·c·Ó¹Î\8­¹¹í\x000fZo\x0006Ø9¹½ÓGv½pZ{\x0011S{·(^\x000bgiM5ÞÊL\x001f\x0015^g/Ö^\x0018/\x0013~éZp»\x001fà¬SV\x001eû4x¾³\x0017^k/Jô(93\x0013eïªiïgEzû¬­ïìWÚ\x000bWL&_Ë{³\x000c®\x000bqg\x0006ÞwæÂ+Í\x0005Iç\x001a&p«HqÛÆÏ´3òö½ðJ{A®\x0000O>N&ÈjuûûâÎ<·ïìWÚ/.¼þUJi.\JÍÍ3m\x0006\x0018I\x000c\x0010wâu\x0016Ãk-õ1\x0011ÚF¶~8ØÁ·ïLW\x000cT8HJuM×©\x0010Ü>{ë;áµ&Ã¬Ø£y\x0005AVRI:4ØÙ\x0019*¼Îdx¥ÉpqD!ý×<L»¸ðâIù$
^èLFÐ\x0012ö@\x001b!ûþ éY«.UÑu\x0016#h-F´²½+rxab¬Ê¾S\x0017:k\x0011´Á\x0005¶Nè³43\x001bÕ\x0001WF0©ð:s\x0011´æ¢0ñ6â©´=x¾¥|ÖÖéªð:s\x0011´á\x0005­\x0015Ä6ÇÊ\x001cÉ
 Ýùm;s\x0011´æF->\x000em\x0017q\x001bn\x001eV6{¨è:k\x0011´Ö¶?I§?Ò/«ì 	o§­
:\x000eZu\übîOÎ3\x001efi
\x000e°3p\x000c6\x000eZmì¦íóõÓëÌ\x001e²kù¨µ\x0011~\x001a¼Øiã¨ÕÆ%æá\x0007ùh\x001d¯ìÆÅÄ\x0013³3£\x0012;u\x001cµêØµ±É©e¥gÛ<Së÷\x0005±SzQ«ô\x001f\x0005çC[×þ\x0006ÜYm\x0011;¥\x0017µJÏ8YíH\x001bÃ3ïúLØæ­\x000còWáuZ/jµ5íìÑ6q\x0005Ú4Ü\x0019<ÆNíE­Ú3so7\x0002'.0·ÉY~o\x0015RìÔ^Tª=CóB)ÛÈk0åýÌçiØ©½¨U{åÛ\x001añV\x000c
1·²ÒÛ«ÁKÚKJµgsKÃG0ì\x000eð1¶}\x0011;_FS§öVía\x0002¸èRÛÀ\x0001­ª\x0011Ò¾ÄEê\Ñ¤N\¸6Ç\x0012[
Hzmêë>:¥´J\x0019Q\x0006Æ¶ço\x001eíöy\x0003©ÓÈIµH¹©<3ïMùi¥Ú\\x0005×éã¤ÕÇÐE£E)jÙ\ìTx©ÓÇI©-
\x000eç\x0015
Ùò³(æ¶B!î|wL]Î"is\x0016å"ð¨;QÖ>|Û¼óy%õÕ¾ZkAI\x0001\x0016^>|Ìó æ½IÜéã¬ÕÇTÏãI¢çq\x0005O¦{¿³H*wú8kõ±É2I#Òöi¶µIX|^é+Váuú8kõq\x0000ñTBðÜ{\x0019Ûú\x0013·2\x001f@×)ä¬UÈEÓ¹ØÌ\x0011éA3\x0017û.nîTrÖªä`¥>\x001a=«dÒÐròv\x001e½N)g­R¦Ry³Ul«ÅSÉûÜ¼Üéä¬ÕÉåäñèÖ\x0010d2\x0005fh\x0016ÍíÔz¹SÊY«
J®ÑDÃ\\äöF°2\x0013U\x0005×©ä¬UÉ>Iss(bäÈ»%B½[Ù¹£¢ë[0\x000e¼ÍI\x001e¼#IQ¢¦ãJÿ\x0002\x000fNºÍR%ÛÜ,\x0006yRímlË\x001bÒ¾Æ\x001fèûÍ¦¦\x000e\x0015ó\x0012\x0005\x0017h'\x000bñ¥6\x0018lg¶\x0016ú³iÖç1²¡\x0004Y\x001cQmãÊ [\x0015ëñ´JÙ-¦\x0001w\x0000\x0015AÛGµï\x0005\x0008ú¦3ú¯Jñ¡È _-ZpÍ\x0015Ý\x0015é;EV+Óîp>{àxl\x0002ÒØyæ[\x001b¬¥âë{ER-Ûº<iâK÷]\x0014ñÉë¨\x000f+kU|©çÓjæ"4Në«k±\x001c:æsûà o£ÿª\x000c@jâC\x000c\:ÙIG¦÷û\x0017pÒ\x001e§í³\\x0006\x0017åH"=Y-àv\x0016ÂiÖrÄ¶"+DÃ­JE|s¬±/s\x0006Ð[\x000eÐZ\x000eÓ\x0016PÏW-=ÇÔ¶¸µ\x0019K*¾Þth{øl´ò\x001cDÑX-4yeð¡¯·\x001d µ\x001d&ð&Ã\x0012XHÒ;µb=\x0017Wfõ«ðzÓ¡m3¤P\x001fJC0<n®o\x000eÖv*ç6Cm¡-\x001asÅALA²Y®o\Y\x001f®âë¶ÓÐÒ4*>ïø¹kNl¯ÝW\x0010\x0007ÐÛ\x000ePÚ¢HÄoö\x0005¨z\x0006	eE®s{¥×Û\x000em#$\x0005lNÄgÚÐ<°Öî+\x0003ìm\x0007*mGAFMjëãDP\x0002iY*QÓ>¿¹oÔ\x0004m§¦
FøB\x0001rG\x0003©ó;ËW\x0000{ãJã4Å¤~_O,>)ìrv_Ñ\x001eô mÕðX¹XñD·à¾\x0012\x001bè[5AÛ«i½o¦Ía{Ø \x0007Ã\x000e¿óvôº\x0019º\x0019É[®©ÇÀÅSØ\x0012inm ¯
¯WÍÚ^Rë\x0012ï\x0002\x000cÔnÈºÅåõ°2û\×«fm/)¦(/\x001eË5fËÖ^Õ\x001cìëJ¾\x0014´Ý¤¶\x001c¹Äº\x0005ó\x001cô¶L$Ø}§¯ï&\x0005m;i %g@EýItsó¬`§çÒ·¶ÔB |r%ð\x0010ÝìvÖ\x0004CßR
ÚÒâDIRÃÑ\x000b*§þ´ÙîsìíÉl\x000e­c¶\x0005F4½RÒ\x0006R._\x0002·}÷£o*\x0005mWiq£ÄwqÉIÚ \x0019IùÑ\x0012}|½õÐ¶Z2&þAÎd
Ò^ñõÆCÛVZnªT\x00039\x001a÷)ÇOÆÁÛ¸3mÐ·¶¯ÔÂìú\x0015>\x000eN\x001c\x0017öÕzAßX
ÚÎR\ß S0H~|=J`·Ïyé;KAÛZj\x001bU	|}åó:·ïõ\x001eúÎRÐ¶Nâ«×ùÈI|"½9Ó¾³\x0014´­¥ågÍxP¾\x00037+qå¾
\è\x001bKAÛYsÊjñDv~e!¹®7\x001cÚÖRÌ-ãRî°Ø
Ê\x000cgöU+AßY
ÚÖR²\x001büÂë'f×íÔ+}g)h[K1{ª»­âC.£\x0017·jg>²ï.\x0005m{iQÁÒx@U}^ô^\x0010½·¶üRÅ×Û
m)e\¸ú&'HÊ M°¡tûøz½¬máÄâòæ/rû$¡íöîuûú\x001eIÐ6IRÊÅÉdQß^@æÙ´3åÒ÷!¶\x0011øðL>MÐÜæÝ×àOÆÆ©ï¯Ê/çeªqáÒ*\x001böUYCßL\x0007Ún:_`í¸ÊÄ'w§[Ð7«¶[¤'^\x0015­wó"½fÛöMx¾\x001f\x000c´
aÓéc>ç¯m\x0016>¶ìvz}}ç\x0010h[0K;\x001d
xË²\x000fÖ!ìS.¡?|A}ø¦ñ?øÐñ8Â'½CÖî|\x000cìûK@Û`Bâãæ!\x0007÷,|\x0017ûªp o0\x0001m¥}+,?ÓÊ¿\x0012J\x001d½}Ð·p¶Ã\x001a3~Á'×coÎ*¥Ô\x0006ÆJ+±Í±áX)$±Ô/º¯WÚ>	kZ©©å¬¼Çì-\x0013ê+ÂA[\x0012NÏ\x001d$'?ósã°whL^NG'Æò\x001bÊttÍÀ,\x001e%W\x001chicµ\x000fq'd8\x000czÈò2h$Øªë©Ó[ÙöD\x0003ö\x0012¬2X×¦>8++\x001a¬ñmÔçÎ`\x0004ã\x0019eqÔµ¶¸
1´ú° O
­\x0004f¼>\x000c'a.ª\x0013±ÍÂÿùÓÕ÷\x001f\x001eØ]\x001adnH}ø$¿özVJ¿}}õâùË\x000bÛ \x0005	H¨@*Ââ\x00192zcê7-ÿ×]ÑÑ©ìÊj¨&oªf³l\x0012#Ñ²õçßf*¿¤ò:YI
<PXÉ¢\x0012¨¸âím
K¨ rmM&Õóå:p"E\x0019ÝåVú­6CÅ%TÔ@ñCdn{3\x0012M"\x001d\x001f/-\x0006É·\x0007\x000c0².*vûö@å%TÖ@¡\x000c$ô)Ñ¬Ý
%yÅîô­L:=ÇØonãe¬Ô4g¿ßJÊn3V¯;5ÊÓFQë>y{v{\x0002ð+õ\x0001±:ý	\x001a\x0005j¤®=9¬\x0015¼TK;Új3Õ)PÐhPâÃy×25"µ¥&n­Nu3ë°î#rHåktÅ\x001f±éEY±:Å\x000e*ÍeT\x0019
óBKÃ;©:Í\x000e\x001aÕN}ÒRm\x0017dùljÓÁ]Xß7cuº\x001d4Êü~hÂ\x0012Û\x001cÓ\x000eYX¢×\x000eå\x0007U;¼ÿô±`ÝÿvõýÝ§¿]}óéãÇûß.ò\x0005hû|2=¥×½ë!JßÑTRÔ\x0011>ýª0ÞþpõýÍëW?\}óúÕ«Û\x001f\x001eË\x0008vªvÒÃZBü¯âÒØëÉVÒkg½¦¹üÖá\x0008ÖùX§\x0017¦¯ÕwÀ\x001dßÕv¬v\x001eÆj\x001e"å\x000bEÃíÙdwZz4Æ\x001a;Ö8Æú;ÉuÎ1±¯un¾&Ö©ùú«eÍ\x001dkþJY­ëÃìò\x0003	³¿»ÿá¯\x0005ö»Oÿ|wÿ@&À;\x0003RtSþâ÷\x0003g[#_©	úîöùËï
êw¯ÿÇ³ÛÙ\x0000Á´KL;iÄû eÕ³-¾5Ê®ì>Òsú%§\x001fà¤¶J©A¤r5þðÁI»±[ñGôqÉ\x0019\x00079¹Kz ê«VáDiq³+9?=g^ræ!Î6\x00084Ä5±Tï[\x001fè¹®æþ\x001aÜ#Ê;éê1<âò¿RØ+1\x001e´»H0rhît¿Q¹6Êæ\x000b\x000f+iT=gw`ì&y)u/a5·Æ\x0017ÎÖ¸oVféA»\x0004cWiÎPy\x000ckPßºYÍJK\x001e´»J0væúTÈí.ÉK±[«ÑRsbwpì*µý\x001d\x0001$ßZ8e£[k×vW	Ç®\x0012Èt½Ðzè\x000bhëÔ\YÇ¬çì®\x0012]%7î¢öE×»Ö\x0016V
TôÝMÂ±dæ\x0002ôi\x001cP\x0005m\x0005è~e¬²\x001e´»I8tRÁiIÚ\x0008Q8E59ÄM²ÝM²C7)E\x0019ò@«¶\x0012{M-K¹R8¥Çì}»¡{B«@ó\x001f©C4]éºÒv\x0017É\x000e]¤ä¹\x0014¨\x0004¤Ü8^8¥\x0012­\x0000\x001fñÝ»d.Rr²«Ä×gÓ	Ô¦Öi²R\x0014¤\x0007í.\x001d»H­eÇ°>³ªoË-V[bÔ ®»Inì&a¨u¼¦¶Þ\x001aÉí><\x001fÌ\x000bÄûxÿé2qsK9­æLö<\x0011WÛ\x0016xuûz\x0003\x0015.©PC¥07Ð¬\x001e~¹s3àZYÁF(»²
(\x001a¸(3PV«¥6r¶èÉµ.TnIåt\x001f»ç!ZvÚx$áØZ\x0015ßF*¿¤ò
*¨\x001c¸Êjs\eÕæ ÄÕfÝTaI\x00154²[#rîz~\x0010$£7\x000e\x0015Pq3Ë\x0014Jñ¶\x0012	ÆZ#\x0010\x0015Vg:lJK¨¤Íó¤\x000ewüÊ\x001c°%MVg<m¤ÊKª¬\x0010\x0015½ÊJt\x001dêY­¤´Ö(Ôü¢;iP£\x0015^KÞÆË¥4wÜ!)èÕúv½î²\x00059UÓ\x0002R>U z=2\x001dÆêô:h\x0014;ºëÈ¹é\x0005'õ\x0014>¬\x000eÛÕivØ®Ú]*\x0017é¥èÅÞ({\x001f#®ÖRnÄêT;ht;´Ó8/\x0002JV
Èý¸ºN³ÃvÕîR×Åµ\x0007@\x001b\x0006Ñ­¤«6cuª\x001d4º\x001d¸\x000c\x0011fël%ô÷qu5ÌF¬N¹B»ÙÕ©wÐè÷""Y¶R4)ï\x000cI\x0018ÚÆÕÙX~\x0007/jIÊ=rq±X=\x0004^ÎV\x001aw\x001b°Óð¸]Ã#m\x0005!i­ÄX¢L©ûd\x001c«Óñ¨ÐñÅq¹\x0016a5Ã\x0013°Qù\x001d\x0017\x0011{×}»ÿÂÂêT<jT<mîáº\x0005éájÂ,\x000bÃý\x000e?\x000b;\x0015ÛUü\x0017V§äQ£ä}&§rURÒµ\x0019ýêüÑHÇí
Þå"\x001eQYÅç\x001fÉ4?yµ<z#U§Hq»"-T^2ÎÑµuàÉ´Öf%»\x0015Ëv\x001aË*4V¦¼­¬Gæ\x001a\x001b³¤qÂzsÈF¬N7XnÈ4Hc Ó¼mwÞ¬omÙÕ]B«¸\x0005§MIòÅV{\x001c¬Û!­îÄ[Í¯+îjd\x0018$\x0008£·7\x000cW·´lÄê¼Õ\x001cùàÛ|âdÃb\x000cv\x000eXÇC\x000b×\x001dy§9ò\x0001¤_\x0016?²\x0003HÏ\x0001µòÎ¿\x0019«;òNsä}6<Úr\x001bø#z'\x000bÆÂêLÉX}ÖHsäV\x0008\x0012J{©®­.\x000e«£á7buGÞi|ù\x001bY3îÈs®Xm\x001d[\]µ\x0011«;òNsäi$\x0019Ç<¶-Î;Ø¶ü|u~Ë6*ßx¯9ñ6·Ø¢ü2óÑÂ¶Å)¯NÚÕx¯9ñdïZd$#µKr#ÓHÌw'ÞkN¼iý¦)\x0006~Ù°!Å\x0016­öªmÄêN¼×ø/Õx¯9ñ¦ÜIÉÎq«ô\x0003ÐRØa¬Ð\x001dù Ärlk¥i¦\x001cû¦QVqF»:j#Vwä&æIIüT\x001dÂ	+\x0016·®ö2oÄê|Ð\x0004\x0017ÉËT,uæ³å¥ô-®\x000f&ÚÕgá\x0015G>%7g²xÁËfõèVû17buG>(|òí-9s'k\x0000©f{\x001ewbwÞ£æ¼\x0017ÃÃÿ(£[
ÏÒW\x0015×\x0007m¤ê{Ô\x001cw\x001be\x001c\¶XÅ\x0012\x0016\x001e\x000fSu§=jN»5ç®T\x0005°ê)U©öä´bwÚ£æ´[/³/³mæ\x0016µ±¬V×Èl¤ê\x000e{Ô\x001cvlÙ&Ù\x0012èc;Y	ÇUCêÎ{Òwp24 ;'\x0019oïSÃÚq´RwàæÀQ¬îÄ'Í7­W\x001cçZèh©N±òØø¤9ñ_\x0012Ëã_îN<Ó;kÚª[\x0012mîª©\x0019\x0011Vç\x0005mÍô`V\x0005ö%C}è\x001aÿù\x0005cîûÿ/~ò)rûñDn?*\x0012Jm:ß´ã¿hü\x0019pu÷ùÖ\x001cxÿEQóE¿hb×ÀÙ\x0017ý
>(ª\x001f\x000cSÕÏ·w?Ý_ÝþúæíýÕÿ|ÿöîÌ¥¥Ù
ò(\x001e¾ç)ÙÑ0
[½xróèöêöéã'·WÿóùñÜ\x0012Ï©ñÂ5\x001b(\x0013\x0003m\x0002i~ÒÑûðÂ\x0012/èð¼¡ ç[²)ÉÖé¢ZüNº´¤K_Û·îÛòã\x0016é\x0005\x0019)\x0018\x0002¯f·NÒÀz¾îãþë~i¾îóòû~y¾ù	wR-æk;Ø«>¥îûòò3\x000bVó^\x00126DÞ±B\x0002\x0014õ\x0007~Ð¹BÖò\x0003.d}[Èþx÷îÝýE¶bÊj¯B*\x001e\x000f¯M´\x001e¥\x0010+ùó\x0019$O
Ö\x001foo=»}\x0018\x000c`¨\x0001£X\x000bVoXµddRZ\x0019¯­!³K2«\x0012Ü#¨b31N\x001eÉgÛ5`~	æU`erë4e ~L~LÖ\x0010\x001a²°$\x000bªI¯%¶¬|×À\x001f3H
bq9÷ÍeÓù7*´³Ð\x001cß\x0000's
Ú\x001b\x0000Ý
\x0000Õ\x0015  ¦æ±A\x0007ý,²³ÄËu\NÇ\x0005ü\x000cV¸\x0002ë32\x0019.o´Òu§\x000cTÇ¬Ä§\	UÀZý¦GilI+£m5h©CK*´h¯\x000cy0!u®	?\x001f`¤ Ãî\x0002 ê\x0002Dùå)Qé$?¹$o­ÉÏËÖ õ&@w\x0001<²i/hIE\x00017ët× uG
uGÍ\x0001~\x000c'?õ8ß&º¬ô¤iÐº£º£F©IV¶´\x001b\x0019MÒ"Å¦\x000fi\x000e8µéàsý¾}ÿ\x0013ÐWOïßÝ}øù\x0012a\x0000t­'\x001a'ðûi!\x0005wH®O>ûöù#
¦¯Þ>»yùíÃ¤vIj\x0007H=\x0019®$-áºî\x0010¢7ä6ákå-aÔ-IÝL¬G\x0006S_<ÈóM«#¬´aI\x0019(½i«ji
TÒ V­®ÎÒÆ%i\x001cúòÅ²\x0005éâu¼*@äú6ó\x0001Ò´$Mc2
ò\x0018N2­E\x001e£khÎïû\x0008i^æ!\x0016Í$»:iqbmÝÏQ^|W¡õ³3\x0008®2¨\x0011iÀÖi^\x0014T\x001dJ³/¤¡3{Ò#¨Ð¡Â¨LùYd
"Ó¶Às}ö´Sú0¤õ
\x0015/.´>ßý¶$Ý6î\x0001ÔNëÃÚ÷mtOÅº×I\x00039·Ínekë\x0000j§öaLïGw=ÔÚÝå­1óI=äRùÔ	Õ5[Jù¤f)\x0008skÉý\x0001ÔN÷Ãò÷YÆ_³\x000bå'\x000bÈ¨+ó\x0007P;å\x000fcÚ?%©ð\x000e`y\x0011· ÑX9\x0000HµÓþ0¦þé\x0001Eæ\x001aÎ$ú\x0012©	ª[\x001f7­DÅÎ\x0000à\x0001 \x001d4©²®²Ø\x0016Ó\x001e#Uì\x000c\x0000\x000e\x0019\x0000*:³²½~}ãSóRVÚÝ\x00068{Ìé7NêÅI¤¢©\x001c\x001c,ÒNýãúÏ\x00055É \x0019#ñ	MSùÍ«\x0003¨RÅ!¥¡UJÓdä:À6y"¬´\x000fv:\x0015tjÆ,¥æ\x0014£Ô\x001berj^êÊZ³\x0001ÒNOá*¡\x0014\Ïs¬DSÒÊãâJ°ÔvwßÜý)¡]hx×T	§Ú\x0008ñ¸²kj\x0000µ\x000f¤ÇîTnê!È9ùë\x001fâ¦ÚîFÙ\x001b5ùþàLÙöÓ\x0018é!_¿»QväFUZ\x0016%À5flÃÿ×7\x0012hI»\x001beÇnT\x000c2\x0018HY¦ÖØ6¹\x000b8§®»RnìJ%\x0019ÞEË'êÖÙBÚÜ©xHØïº\x001båFnÔäùù\x0019\x0015ÅñóÇvWÊ])ò¦l#µÍÊÇ¢vwÊ
Ý)0¶­ù å#½\x00143ÿCLë·Ø¤þ8¢T©V\x001dV­£û<Ä9vZ5]-\M©Iå6
\x0014MWgUÒæ.Û¶<Ô\x001f¡\x0007Ê/êÔ?
Ý¯bQS\x000b­Ù·¶&¶¬êÊ.³!Øþ(rÅ\x001c=Ý´õV[¼vwmÜéIpc'¡\x0018/y\x0012¤ËÉ ÔvT\x001ca[ÖnTáÞ
)ëº\x0008]ò¡\x0007\x0001áT¶\x0008×¬ø\x0000×¾Ý2'AA^W^ÆØÝ\x0012\x001bî\x0017\x000e\x000c~46t52ßPsqù\x001d(æG*2B(ý]àEK!ºL½è/sÒ\x001aþdëhñÆK>Tò9k @³[°>\x0000Qû ­xåoûxvgµâ+2\x0003`ñúC¬-$¼ñz:·¤s_ðü\x0012Ïkg}í+×ItÉÔ×ù";0{áÂ\x0012.|u²K¼¨ç^$;Ë£N\x0003)\x001d\x0011ßÉè,=_^òe-_(·!0_ ¯>Ý\x0011ÞIúN\x0007½ÚSë=D~÷\x0000\x0014ÚéK;?/tz\x0005Ô%¦Xå\x0019Û!¥$ß\x0017O\x0012 zÀNµV·\x0018J!áðÜk\x0011h¼\Ó}¸\x0013°S. Ö._^Ý
\x0006õ\x0015þò©\x0003LJ@\x0000Þ\x0002G£Ûù\x0005\x0000ÃÞOÜé\x0018P+/.ÁöäR\x0017£\x0003,`<ü \x0018\x00113±N\x0006
`Ì;½+ìÔ *Õ` ²íéí"aæÚW>t|©Zd'_ïýiÝ¿ò;ÔdúÂ'¤è½Ø\x0011{¿p§§Q©§\x0007\x0001vj\x001aÕjúË\x000b°SÓ¨TÓ¿\x0000;7\x0010µ~àï ÀÎ Ò\x0004ê¹ò
EÞ×¢å\x0010aOæt\x0001³\x001e¯3"¨5"´ÁpZd]ðá
§!ÙÐøâ^\x0015Ø\x0019\x0011T\x001a/.?Û\x0010«4!¿ülgB¬Ú|iùu\x0016Äª-ç­:g¹ý¼\x0004JâÄàisëf@\x0013ëë©Îk±îñêÅO¿^Ì\x0010ÅÐ9=Õõ×¬q
2¤ÂæÓq`¼ÞíêÅË×O\x001f&sK2§#k£=Åo\x000cÖ¶%Ó¾\x0016\x0015\x0018t` $û¢2[¬%´ BKS\x000bPàå\x000euÂK¹\x0015­Óéß:´Ô¡%\x001dZÑ<u¹Lï\x0013¦\x0015þÎËTa\x0005Tw üi÷43_N¼ÌDv§­-:²î¤¡ê¤µôÅ{ò9ó¼\\x001dNkäuh¾CóªÏ\x0019*âêç©®­Äpôb¼¬»\x0003¨º\x0003Å2I!<í¶áF9´\x0014=ìC\x001dZÔ	ÍÊPpoe\x0012£q-Mj{4\x0007v×\x0013U×3ÖáHG-òÃ\x0006`lRK{ÐruÃÉ %_l+J­=\x0012n¬QÍCml\x001aj»¬(zy_ñÅ5\x0007\x0016Z[Gfòëi;fU:-»6/tZ\x001d![4m"Ûc=çª¥Ìª¾&-\x0019¯9÷ýÖ¡´KÛÚNÛZ¶}æF¹
[)Í¾sÖ©4«Ri6é`#ã>\x0014/Àé\x0012,\x001dY§Ñ¬J£Q/tÑ
¨{î2È¶\x001f\x0007»\!Û)4«QhÁÐ,¿f¨ÏàÐºÌi3¹
ÍujÃiÔÆÔ¤7\x001b(©\x000eqÖg{ÔÆ\ª5îszïç½áçm±\x0015h}Òu
Íi\x0014Z([mèÕ\x000b°ØÿgNÛUu`}¢Ñ\x001a4±¿Ùt\x001a_PËC\huÂæ´ãRÖ©
§Q\x001b¡(\x000e©U(æ \x000e]÷ÞK÷Í»ÔëÔÓ©
Ì²\x000cÙ{ÙÇU\î¶w\x0012Í®+Ðé
§Ò\x001b\x0018}³\x0002ÅG\x000bõv ÏÔN\x0007àêÐ:GÈ©\x001c¡äÛ\x\x001fP\x0002Ï[e\x000fî¹¾Óh^¥Ñ°Äí8B%"^_\x0012¿¬Óh^£Ñ\x0002Baã¼\x0012z·p\x001eaU÷Jó*f\x0001e\x001c®§]ÕB\x0003(ytºØBÖ9i^å¤ezxû\x0019Å\x00152©Õj¾N+Ñ:}ëUúÖb
\x0017\x001e3<óÁIí M§EM:´.&öª8ÉpÝó¸³â@Êx\x0000w:HÖ\x0002¯2\x0005vÑËZªÔZ2m\x001aÉ¶\x0003¬³\x0004^e	hl]Ä&3WKAÁYf{,»ï,WY\x0002Ú+=ÕE¸zÒ"&9i\x0011öX\x0002ßY\x0002¯²\x00049ã¼gØ)­=\x001fm,\x0001vQªÐBg
Ê\x0014Øè¤Á»\x0000q|ç#È\x0006ò÷÷x\x001d¡³\x0005Ae\x000b¨ÔPzOé~Ö³mÉ9ìÊ¾Î\x0014\x0004)ÈN\x001a\x000eJX'eüÑ\x001cµ÷hÐ 1\x0005ê´ H\x0003Û\x0014¸¡Ð 3\x000595+\x0005Ô\x0003U\x0016E«ÓÉ?:²î~\x0006ÍýúÜbhBã¹\x0011\x001eg¥¶\x0003,vW ê®\x0000Bk\x0014¦¯iùk:{È×ÝAºöEeÖõ¨1ë_\fõ\x001aë\x0019ÊÿxöÓLÓ°\x0006Ûå<Ým¢Cë®@Ô]¯g2éöçOë/ud©;hIwÐæ\x001diVM\x0016\x000f<ÚcÐº£TGz¤H-Sýêfç|Úé¦q¥]_öA°mú ¾\x0012ëÃ)`13J@oÛ»1Z9xRøKþÇ®ðÝ\x0002:§\x0004üÂ\x0011)¦SBL:B\x000b\x0007¾½\x0005qÒ@\x001d¥=Z\x0005ã\x0019aT\x0012ÒZ<\x001f[j\x000bøõæ#JrwW>0}å¬a\x0000iÂ¢\
·ºO¯û«9ÝJ§½(\x001fï?\\x0014úâ¢DzQ¦ÙaÓU¦¼\x0001_ÓAeP8·0qXx§Ê@ä9.\x0012Fíéûtþ6:4's}Ë\x000fx®ïÕíÏ½ûpõoÞ¼»ÿx	ÎQU-ðj\x0017ï®lÙôH<«\x0000y}{uûíw7/¯þíõãg·¯\x001eæÃ%\x001fð­àÁaxvgµxôAg>^Èæek^\x0019T§£sK:§\x0016y$wL¹ne*¡\x000eÎ/á¼Zt¸ãì´¥Q?Â\x0017ÎÛ|u|qÉ\x0017µ|\x0016ÛÈð nØfþù.:¾´äKZ¾\x0010Û ç`ØpØ\x0018¥
)æAI*>èn.¨¯.Õù\x0008`äL¥\x0004\x0008pe/´\x000e°»» ¾¼ô®Ê'°Ü\x0014Y$çëqçõîöÐj9~À¡µÃ÷Ç G\x0010w\x0003\x000e0¨ïHlÁ¢o+XmûÚ9§\x0007ìî0h/qÊ­ÀöÈ²E) Jve¤¯»Ã ¾ÄØÖÅÐ\x0006g'\x001b=\x001b äóq:ÀÜ\x0001f­\x0000S[\x000bËiä\x0013\x0018`\x0016¿SÅ\x0013f\x001eÄ¦\x0010 Ê\x0010FsÁûÃ¢\x0001'	q§ÃÎ¿B­E/So_\x001d´¼)\x0012Û\x0015ñ+±t½¥VÓ$P'gË\x0004¥P¢x°{\x0001;'\x0006Õ^L	ÎsjZpVÓØ´àÞ3Ø©iT«éb~\x0013ïz \x001d\x0006?±\x00175íO\x000bÕFµ\x0006síX2¢\x0008P\x0006ÕHä|ì¯ÓÒ¨vµh^Æl3¯\x0008ÍIvz
Ø©iT«izn±Í\x0018ÞBd\x001ft²çsHT|¶ÓV­\x0005
ñ\x0015-\x000f\x000fSÓ¶S2V«dh»0ð~be-\x0018eªg²§\x0005\x0002jÀNÉX­)a\x0011;
iÚ\x0015ÄJ&´µ(neH\x000e°»ÃV{i.jn:&²qmÓ7{é<\x0018bWáG-bjzÐ8\x001e/T\x0018³05FèMÝ2ÅæN¦ß(Ô¿\x0016{b(ª\x0006ÏÈ§ÆóÝ<jQþt"Ê´¢4u\x000c}nÃ³¥mh6ym\x0004.öÅ¾ª)ot÷ÕèlN\x0012G´övù\x0008ýíýßß¼}{yÁ£ÌÌÄ\x0017l\x000cTÙK|F*£=%éöíí\x001e?yraÅàÙ%Uâyk¥\x000eÚ8¹vêXp|\x0008ËÉüLÖw3_ây%^ «éüXô5;È\x0003ã©g÷3ïJñâ\x0012/j?n¦.N\x001f79ÊÀM\x001fZF{wSãå%^þÚðæ\x0000\x0007ðÕñuw\x0003´ãóÙîóZõ÷¥J¯ênAôÜÄ`eî;½xsE>áu\x0015ùð²¿f:¤Xï®IbÍñØÎ\x0017°r Ç©rú\x001eýrÿëwWoï®\x001e}xÿæ\x001fWOî~|ÿÀ\x0006"´T°z4H%Àõá\x000b1Õ¯ÍÉF©Gßß>}üìêÉÍÕ£Ï\x001fÿ¹üâç\x0017W\x0011	,.aq\x000cvªÙ¯«¹\\x0000\x001e _5td<õ?Lk´vP´Å{àåNXËë&Ñ\x001a\x001e Mdë´nP¶åë×Õb.\x0007Ù÷bx:i.Á=\x001eÃ¬yÕO\x001dh\x0004[\x000e0Õ^TX9\x0007ö4§=J\x000bý\x0015\x001b½c6ÊrÀ\x0012\x0001òä0ªÝ­^F9\x0006æ\x0018áBwlaôÜ\x0016%Úrnë%\x0003\x0010\x0000é$7LÛ\x001d[\x0018=·¾	×cfNytÎö´[f¶;¸0|r\x001d¿%k\x0006×|Ë\x001cW
kp\x0008-v'\x0001\x0007O\x0002ÐH>­ÉÒ.n\x001c/WÈR<\x0006×w¸~\x0010×¹:\x0001¯àºiÑÖk9½-ÂA¸¡Ã
¸Å-¨c\x0002+oe\x0007lÎ¢s¹;è0Ä\x000e7\x000eâÚÌÛk\x000fsüEsq\x0011O¦íµÇà¦\x000e7
âÒ\x0018Øz\x0018h\x0005ïÊÌ)tÿz\x000cn§\x0018pT1ÔGd\x001aú!Á\x000c\x001a9¸1\x001dc æ\x0004çä×AÖ\x0012
ðIH[íÉµ÷!\x001dÛ_;h~Áz.àK´Ë(°·N\x000eîéâaÜÎÇµ£N®V\x0012Ä8.ô¢ñ\x0017¬týéãaÜÞÉ\x001dµ\x0011(uUöEüÿÔ½]ve7rç;3\x0001s\x0001\x0011ø\~b*©\x0014k1?©ëº/ZL%-ÑJªL_úµÐ3¸ÝÓ¨ôH.b#\x0002\x00078<gó\x0000{KÍ²«ì,Z\x0012Æ\x0006"\x0002ððE¥½¬nëÐ6Ñ\x0002\x000eF\x000b4Þ@v®7¢è\x0011dçuL.6\x000e
G\x001d\x001a)æ¥ugfê¾h
®tÀÆá¨?SêD\x0019Þ¸Í-ÈÊ:¿Ò®m\x0019:3
Ü\x001f\x0013<	ïåzÏhÜJÞ\x0001\x001bgÎlÚ¶ù\x0005S^£7b\x0013â:\x001bÁ4þÁ\x000cú\x0007UôU\x0002½8ñ;Xt¬{\x0011)´\x000enã\x001fÌ¨ H!ãÒ¨hË¸Ûò¢~¬iü\x0019ô\x000fÊ#\x0017«\x0004ª8ã7²DÉ¸.u¼¯iü\x0019ô\x000f*\x0006ñ¾^(dëòYÃpØÆ´YÑë¤\x000et$\x0011O¥D\x001c3¹3Ù»ô¸²\x000enã!Ì  ½àÈ{7<X(-®/1î:!¹i\x001c\x0019t\x0010`Ô	¸¼¶ÖÊ¨Ö\x0014MÊÚúâFÓø\x00083è#\x0014Õád+JJ¢ãFâhýZf¡q\x0011fÔE¤;ÉÞ7¢\x001a;\x0011Ø,ì6Ò\x000cã6÷\x001d3xßI?åºÞdgÝ	ßÎÜxHmg\x0015ZÛ\x00181;jÄHÃ#Gb4Ã\x0013ØÅ5+å\x0015lc\x0013ì¨M :iä`É\x0013ç\x0000²\x0013vGx
ã6ÇÌ\x001e3gIíoÂ-ÍAér.î×\x0005¿\x0012n³qíèÆuÀBhÔ
o\x00054ìÏü®Pá(®kv®\x001bÝ¹N4\x0007?CV·H¸rW÷¸Î9sÍÖu£[7Å6Qh\x001dÝ&ò9»¯G»Î^pÍÖuÃ·\x0008CÏ\x0013®ö<)ÓL\x001d\x0019w÷o\x0018·Ùºn4ÇdæÎM¸$QZ²Ï²u­^k\x0010ÛÉô\x0003iúËõÕÍë»o·7_æ(\x001dhyv¦!É¢a¢¾m³gPÞ_ÎNßl^¿ýxqþæ¾ú|õõáþ0\x001dÔtðÜè°¦ÃçFgj:óÜèlMg\x001b«éÜs£ó5nt¡¦\x000bÏ.ÖtñÑiÕXcõÜðZgñÜ¼n¼~nîB7îB?7¡\x001b¡ÃÐÃÐÏÍcèÆcèçæ2tcõs³ÊÐØ=xnv\x000fÚ0ô¹\x0019\x0016hN.<·\x000bÍÑçv4 9\x001aðÜ\x00066G\x0003ÛÑÀæhàs;\x001aØ\x001c
|nG\x0003£Ïíh`s4ð¹\x001d
Ó\x001c
Óy4¾31Ó¬É,g%Z;¯j¶§ò*¦9\x0017æ¹\x000bÓ&\x0007Û¹0Í¹0Ïí\æ\çv.ls.ìss\x0019¶9\x001aö¹\x001d
Û\x001c
ûÜm}nGÃ6GÃ>·£á£áÛÑpÍÑpÏíh¸æh¸gs4í[\x0006ÍãÛ\x0018}¾¦Çw7·×\x000f\x000fóÏ.h\x0014»Ñ_$Uô¨­\x0014\x0012\x0018··Öìå\x0019½¼¼;¿8ûðaæÍE8±æÄ\x0011Náp!¢6S¡TL;ÜûÌÝÉikN;Â	FUäÒ\x0001EÅ§S_UdÉ­h\x000fôUurúÓpÆ{~\x000fÎeeS\x0003"©\x001e²{Ë;1c\x0019\x00070ÓÂ±\x001a1\x0015Ëö\x0004ip^­°;u{F\x0011D£B}2RÆ
Dçö¾»wrBÃ	C\x001d¤ñ Y!ùì^ú\x000eQ{\x001fY;9MÃiFÖÓÆòÖn¬Ì\x0001-ÇÈ\x001f¨Øí\x0004m\x001e9Gà"×gÆôÏcy3\x0003"\x0001\x0018\x000f³tr6çH\x000f\x001d$\x000b,\x0005\x0016TÑÊý,&@mÔ{+\x001d\x0003½Jû»ñG§´ái´ñÝÃÍ×¯×¿]yØÜ9Â¿m>\ß?Ù¡j¥Õ\x0000<\x00191¹¨ÖD]¼ýpþþýÙë³7\x001f6Û©Â/?n>]ÎÔ\x0005\x0014v¨Ùa\x0019{P,\x001bnÕÈÝßÝD­vä²cÍËØæ¹\x0011$ÆÂ_FG)Ô;=\x0013KÑMn\x0016.»a¡ä@#`´\x001cF!G½îªÛ\x001aÝ.C·(ý	i¨Àå§²ÛaWJt)»«ÙÝÂeçßtRÕµ¼ì<4#T½.»¯Ùý2vÈë+ÀöR1\x0007;³¢\x001a=,\v]:·}äê¹´ìJÌnÈRöX³ÇËrRµÜj¬½Þ]\õ "ìÔB¿\x0004ÒnÒI\x001cié\x000faÕU×­K]èS*\x001dÞ´erX¥KÙ8ÍZZ\x0015¾ñ©z¡S%eùb!y¤ºbe@yX½ñ©z¡SM\x0017[zÕséhZw\x0014+\x0013ÜºìSÕ\x000b½ª5ÒÆaÒ±|X\x0003K\x000c'\x0013éWµºqMz¡oJYD+íx'\x001d )\x0010+;Þ­\x000bß\x0018x½ÐÂ\x001b/åÜ&\x001a¶à¥}5"¿&<4v\x0012\x0016ÚIã8ù\x0015hv\x0017ÏjeÏGµ¡TÉøîÔõjêzÿrõíþúë<¬Ö,Ú©\x00162ZÉÌ@\x0017Ì×±¿~¼<{ÿ4\x001dÔtÐG§h¨9ëïBàRn\x001aÉê¬Þ\x0003yÄcé°¦ÃÎµKFOöâË­ÌsYÄfj6ÓÇ65)g
½äO\x0002Hç¯¬ÜÙ\x0010]p¶³\x000b\x0007^Ç\x0003%Ø6\x0001·?\x0004çw'ÏôÒ¹Îu.\x0017\x0005\x0010\x0012¯Ùê\x0018ï\x001awg\x000bõÒùÎ÷n:_è´-·TËú$i×=ì\x000b5\è_º¬A1-\x001dìeé\x001eksvÑÅ.v.³<(;¦äÎ5\x00018\x000bË®*é%C¬z×.ÊØç@ßû@d µ°l×éÖMôú	oåËúÒ=NÉ\x0011\x0016Îsf0l\x0017^ã't§£\x0000\x0005eãÑe^<ÉÝ$\x0012m<Ý8
Ýë)¢æxÌ±xYÐNÎ\x0005.<\x0017ºñ\x0015ºÓYÐ¬2\x001eþ\x0019ÀÌÖ¬VoÀs\x0017^ã-t¯» 'ÄÀ«%'\x000e¢?íðP\x0005Ï±x»Ðþ\x001e;£¬\x0013ýC-\x0017ã´z¸,\x0010Ð¿Ð\x000e\x001eæO.)Dñ½Ýzät \x0016~ÜÆcèN\x0001\x0018e>\x0019É\x0016a12'ÏÙðX?¾\x000b¯q\x0019ºÓg ÑÞF\x001a÷ß\x000b¹%:Ý\x0005÷¨èÁÆi@§Ó\x0000vÌfÙPÇn¾k\x0004ñifaø\x000e×N¯Ö°Twºº¥Cìøñ\x001aÄk(½Ìk@{»èõ\x001aÁÒØ´lXtù¸ª\x001c
Ü\x001dýÝ×x
èô\x001aè\x0015?©û\x0014ºYF°ìÔleG\x0003\x001a¯\x0001^\x0003Ù#Þk\x001ek \x000c8r°\x0014¯ñ\x001aÐé50ø\x0013ÈfÙC\x0014&é\x0008\x000fÉ¬<\x001eìÑE×Xeè´Ê&E bWt\x0011K_]ê4°±+ØkWþà@ï$-T§aIa1Ë8§°\x001f^0*Sò\x0002»\x0012ñ½÷\x000cýÓuU¹îã\x000b@Sñ&@í¹\x001a\x0006#Ê\x0010z¿Ô«%À\x0016ð¡ï¶ï=±\x0012\x0005èe\x0002"¡.\x0004ü×\x0016ð_û\x0000+\x0013òRp/z\x0019Tí\x0001YxÑ5Û)\x000f9ÁrÕ\x0007¨Ýv\x0005E×\x0014£á´Éè,Ìÿè\x0016Pw\x0002RL¡ GV\x000f
½ß­È\x001a\x0000üÜ\x0002~î\x0003´A\x000c
\x000cY´JG\x0018Ð/¼'ÀO-à§¾O®mÑó¼¼ª ÊÜ.ôpª\x0005Lÿê#¤r!Ãn¢\x0005yO\x0019tÉ\x0007/ÌóÐô.¡Ö'|/\x000f±(aIôì÷ÌêüÀ?·\x001føç¾\x001de\x0004v4ÁÅ\x0014öñÝ¤I~ß«ïÛw\x0001]	bÒ\x0011áÂ\x000e2ßÍ\x001eÞ\x0010¡Sv·Öþs=,ãÝ¯Wçé\x0002Ò\x0001¾®3i#æâ¿`.-åÎù-Ã8}y\x000c\x001cÖpØ	\x0010ò\x000c]gh\x0010Ëp`yLÚv\x0019­él/Ý$cé\x001c!Ht\J©ú\x00032¤ÛÞÊ§\x000f\x001búð }Y5í;çèÜN/ýü®ÂzÙ§Ý^{	\x000fT\x0017WéV®ò¹ÅRÔç\x001cD>\x0016@iì\x0011¼OÉ"4«÷ú
iõè\x0001ð¸÷?ÌCòãeä¹¥Fnm4´¡]:zî;æµ/ì¾öòÚ¸.n®Óú}¹úò°yquÿéêë|]¤q):àéªFLgÛ\x0007®äwKQÈ²$Êó³´oNß|Ø¼8½|qú~®ÓìN«2¡¼\x0001>wf¬qÙ«iÀVÎÐ\x0004\x0019Ng\x0014ßZÙÔÌf\x00013lº*ò¬ù8¢\x0018åµ5¯\x001dß\x00174v¦¤qXå8­±\x0010\x001b|ìÆG]ìÆ}(Éèep+:ëÊ¶X
Ù×È~\x001c\x00194×yï¸t
!ÈÛá<ò(r¨Ã¢Q^­\x0014M)Ê;£zò[9ÖÌq³T\x0005å´Z2rºäë÷¤^\x0006«\x0017Ë°}±\x001cN\x0017L/O4A$\x0002\x0011ËMÉªÇþ(të\x0001Ç]`²¼ÅPÕt6Í^\x001eÔz¦N7.P/ô¦<ç°¢,8W\x001eÃöäEF¡\x001b\x001f¨Çàé¸uã\x0004õ¸\x0017tTäÊÐ\x000eùÑ\x0016a[i\x0001ëynÝ¸\x0015=îWlð¬,Vº\x000c\x0004O×HIÜê=\x0017ÆAhh¬\x0007[\x000f\x001b¦ZüLdËJC,Ð«mi\x0015ê)¹Ù»ÈÜ!7®¶nÜÈ¨R´¥îÀî\x000e\x0003]âÇ«dÂäÉ¯±QñÈ¾ü&ó2\x0010åC³¹V»Á¿Ú-\x0000üù¿~»þºI7¿¯_¯¯¾Í"G@\x0011$VX<×(ä]<Íüî¿|<{¿IwÀ÷ïÏN?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=:{1»¿:p\x0003ç©\x0016\x000e\x0005º\x001f-7?!\x0002²Á\x001e«%\x0003_Î\x0012\x001aªbfw£8sbrï·¢
¢Z4Ç¦\x0013 iÊjXAºrØc\x0000màOTo6KN\x000fò\x0013y³ñSw\x001eï¾\x000cN=üþ>ü>w\x0012î\x0001l>à±^åÎ¿\x0008'ÒqÀ+vÆ0sßó\x0002æb\x000eÒÄþßd5ß¯hhMÎ/;h½
\x0016£\x0001ibãïA$\x0000\x0011\x0016Êd\x0017Å[~swZÎm­J¤
¿\x0007)ÈlVq\x001a8Nx>6¹íT	4°ôûÀ«Ì
°F*Ià%"Ï/²Îh·\x000eiâäíûl*çç`Às§(Ù\x001bW6·[4pÖ+VIÑt\x000eÕs®\x001dÊ\x0013³fåæ\x001eøã\x0015HBU:\x0015È"\x0013d6]/¹\x0004iàrW iGù\x0002krc)z³\x001b\x0010æÎÝÌuD#¯ºf{ÃH\x0016ÀïF"3h\x0001Ä:;ÉÉ¿¦URy
¶\x0016ô&k Z]·½GÎ|Íþ¶Y&\x0018­à·h\x001fË}bVZJ®Éha22\x0019Hdò¶TLIÅß.Ä¸\x0012MßÎgmq´\x0003íw\x0010Å4Y½r¨>¤É*jÎT\x0016\x0002Eúv¦PY¿Ãí¬d"Í&&ªóDS\x0010©ã¬Ë´Ò§Á\x001aöÒbÂ ç½\x0018¸\x001cÖ§Ák²a£uÂxÚNXyG[ÜpRÂë¤äk\x001b\x0013x(VÑv²%Ïç4;\x00041,1Ww_0\x0013ÞîãÁ»\x0014]}½þû¿wT
@\x0014\x0013ó\x0018¨IR\x0005üq-¨(6È©XáòàÅéù\x0014\x001dÿ\x0004±él¹@\x0007²ïÿ¶AÊË\x0011\x0012V0Ç\x000cZR«\x0011¶cLØ­E}¸\x0005ÒG|(	\x0019RÅl5 ²!
/\x001b ê¸¬\x0017Qöä6J\x001frë\x000f.¥J-y)þ¢ \x0002ÖRM\x001cÚE}Ï¹q-UÖC\x0003JIÕy\x0018Àf
`XK7e\x0017Qöé6Ê óDj 4Ie6SÒ\x001d\x000fgG«'¢ìû×+¸qY5­¥£l\x0000xS\x0011÷"Ê¾ËÝFéä!p\x0015Jßñð<\x0015dß	o,¯1æeR9^Ê©\x001bo	åÐ1oÃÄîôòÁmÎçÉ(\x000båT*c\x0011åÀWo\Lê:Bÿ,còg¡ñ§²C÷½
\x0013â\x001dAÔ
\x0019SR4©¶§ZÌCßD\x0019,Ëb¨\x0010ò&EÊò¸\x0011m|ªÅ\x001cøøm!ð\4T2iqJ\x0019y\x001b8Áä0\x0007n\x001b&ÙàjbAIÈ/
\x0014}|²o>\x0008\x0004Ú(]~ÇÅòPÒ'ç\\x001cÜNOäºq\x0019û"JOO0¸xIò£|à¥\x0014\x0013yE\x0008¦ùS®\x0015"\x0004¶%
Æ<a§²ûekïm¹R;hËëÛ%oKõDîÆ0ðj\x0004\x000f]\x0006ZJË,Þ»üÅÌb\x000ec±6L¸Ë©Y\x0000§
\ÏÇÇL%ê1¯?|ùí½|@\x0015×»Oog#FZ\x0018øPè&¥\x000c¸-)ÃæPê|*\D
×ó3\x0012Î=áKÄ~\x001e­³
hðË£¶zB2t¾yÈz¤áKÄ~$ð\x0017sßð`VrÇ¹ÇvF©ª
Òð%b/4Q0ª²¯`§ÌtÖ¨hø\x0014Q±H¹ê\x001a¿¤}\x0014èi\x00045$'Ó\x000eõ<Ãwý+ä¨§;É\x0002Þc´p\x0010ë:¤á;Ä^$áøU\x001e³ÈÉ\x0008`õ#©ÁO¦ê¯\x0010û×\x0008n¢U\x0013\x001eåóY\x000bE\x0019ND¿ò¬
_!ö¯açR8lÌÄ¢f\x0016æº¯6~Ød>þïk`²¬<(Ò¬5L£gýL\x0010¸&m\x0007\x001cþ\x0010\x000emÞÝò?°Lf2]4zØbAùÀ9\x001b¸\x0011.S\x0011\x0004äÉW¶z¦Ñ+Ä~&\x0011H#\x000fgdäº	X&\x0013©\x0010&®E\x001a=BìGÂçuÚLt\x001dRo\x0008o¦)ï¯\x0005iô\x0006±\x000f	væ"&Øì6Si©Á­»ßN}
\x000b¹p\x001dÅø\x000c\x0015¤Á\x001fsq}ôoí{6¿ý\x0002AËt	Ú÷w·\x000f_êñëÕýÃ\x000egN¢àDÖúÄ6Ál\x000e¢¤¦\x0016\x001f§«¾??{ó\x001að.:¾ÉÙC\x001c×#Jz¨	à©¤ÞPLé¬öSæa\x0001â¨d®\x0016QáFËÚè^\x0015Ý\x000eË«¨ìÔ[8ªõ®^EÿÌMJù"wâ(1\x000cVd\x0015âïòáÓÛ·sNû\x000fû÷8\x001evö¤æ§ì\x0001\x001ae\x000e]6mZs_ÐÓWpB~8ºø\x000eÇÂî\x0007ðÞ÷Á\x0001 ®m°ø^Èa1YðË\x000f\x001b\x000f\x0016pM¸ðû\x0017,8¾2
Èe.íØÊ\x0005­ç,o=Ø#¿\x001f\x000c\x001b5²©oF\x000fØ]D>WÓuEM`\x0013þü^0ì ¡\x0005Ã1ÎKsÔ
\x000bö\x0004\\x0013Nô~.ø|åKZ*^÷¥7,¨0w]ÕsM8®û¹<ÍJÄ\x0005STDç7e­Åô\x0014÷rEI?"éTÓUªH\x001a\x0003ÖkØ¸T\x000bfoÿ¼ûöyú:ýáú~óø~×Ã£\·Æñ¶3¹Þ(¨a\x0003\x0002\x0019×\x001fN..¿3ª\x001d¢Ñí¹('6\x0011\x001e.1Ç\x0019H\x000b\x0018¥Æ§Üü\x0006¢Ñe¹\x0008GîZZ#+³Z\x0002 iê	2©±\x0001it9îEX:\x0017pk\x0003³ùBxò¨áÖÜL
H£r÷½H¨ÞF«Äré=?\¯\x000fs	Ò¨i/´´T(äÂ\x000b"Òr2=Ó@4jXÚGäQÞÓ"T~û\x0001\x001d/Ò¤»Ð4êIÚ¿HÙmÁU2µäU¢ò\x0000Ø`+·Ò¨íhÿî\x0016äòi\x0014*H\±\x00007Ë´o_42àuË`AD\x0018ñ¹ww¯\x0013z	Ò0¬®ØLXù\x0011
Iè.¥Ýé\x0001]Mf\x001a!l
QHÂ\x0019Hd(kýTO\x001fnÝ\x001b°\x0015LZý­#úÑiËL\x0015µ
L÷ªÍ$óÌ\x0018ÜLá\x000c£2:°Þ%kõH¬¦Ôd\x0004=Úi°¤"#ÙI·¼\x0001DZ<'üÁ2Q¡?î&
aÀ,\x0014m`"õ¤\x0016&|u'3³Ói³d8ZË%Lróå}/!NÞÜ>ì4Li,oÔxßQéG±\x0002~Ô2\x001fµ^Bt|töf?Ï°o/vy>bÄù£Y.\x000c½%JÌàÄdé^5Ð°`o/\x0010Ä)\x0016ÈSb±{V(ØéGÔj amÞ\x001e ¬\x0019¢L¶1Ò%§	¦H\x0000wû: a\x0019ÞÞ\x0015\x0008ÓåOÃ¸éìGK{:\x000b4,¸Û·@89 ×	\x0019¼k©\x0016Ð*ªPr²¤·\x0001hX[·oPû$_k^Ñ\x001fáòª\x0010§Þ\x001ax\x0005jûy,eðÿR©qöÙèN\x0018j²¨¦\x0016h\åµÿ¬å\x001eÔ6¥=Ó!£Db\x0014Á­2CãR©ýk\x0014È\x000e\x0001Q®ÓÅ5
äDâídQB5Ñ¨Ühï¹\x001a\x000eÖï3MÃlmT#õ\x001a¢¯¿_ß¾\x000b	ÌWûÍûëù"k¸ÂH3\x000eg!sÑSÔ\x001dâð
JI¼:º8úîdî.ë\x0000
\x0013û\x001c\x0019"iUùfN:zâÇù¶«\x0019Ë½@ø|ÏéM&okG\x0003uròåªg¨Ü¿@¢\x0010	\x000e\x0019w ;©\x0019\x0008\x001c¥U@Ã\x0004å^ \x001féÜãÐSªHs\\x0001ïüÌ\x000bh5Ï°à`ÿ\x0002yjW\x0016\x0013\x0012´>×G¯û^Ã<é^¨)\x000b\x000f^«Ì
3\x0016ì4)¹¹0§©\x0007\x001a\x0016\x001bì\x0005Â«¼-Î\x0010\x001cy>afº§\x001ah±Ý¿B1g·¥³y@\x001e.´¼@y*ìbq¡Á^ cId\x001cÓ#oÊ
MÕ«6\x0000rÇûÐG\x0014´ ßõ^s%VPëlÐ¸Æ`¿Qtl\x0014ñÚ\x0008Ù=sÊý\x001cê\x001c­"\x001aU\x0018ì]¢í©ÇN>½·é5®0¨&\x001a\x0015\x0018ì]£\x0010ó°j¼8DÆ¡Õ	Ó2\x0011Õ,£NÂ½«#¸\x0001\x0008l´ã¤£WäwvëVgÔHXõ½\x0014EË\x000e>8BÅ,\x0005fÑ_Ç»/SO¹\x0007¯®?\ÝÝÞî\x001cú&\x0004uzHÀH\x001b'\x0013QçµÔ~2
zuòÃñùÙÙü\x0018°\x000eÖ0®ÀÂùÝÎZ8¤*\x0007GÃ.h±\x000cêúîZüùç´×x¿¹¹»ý°c;e­þ\x0014Oë\i\x0005î2¦\x0013\x0007¯.NÏÏ~Ø\x000f4ò\x001a÷\x0001\x0019]¢!\x001fÈ@¢æ\x000e\x0007CÙâzÓ¸G44.5Iû\x0004\x0017
ÕBS	\x0006Ó¸÷ÙÔ¸DÑ¢¢\x000ff¹i-+­\x0016hä4î[ ìªÉ\x001f,¸<Ù
¤á\x00169¨\x0006\x001ay{\x0014Vêä-\x001db 4ØRDa\x001dÐÈoÜ·BeVFQSzºòå}\x000fÂÚîÞ¿Oõ\x000f§\x0007ìÍ\x001fînßÏ?`£C#jÃ2\x0017¨	f©\x0012G¨¹J£A\x0014ûÝì<ï-ØD­Ë^0QQ¾M|.¥=4.z\x001eû\x001cÝT
´k¢Öe?\x0015\x001c_ãäÔHf°÷\x0016ÌÎ×cï\x0001ûí×ûk7e¾\x001f\x000f.®ï°+b3{¥X\x0010H\x001e!ÓwtÌ\x0008\x0010éNæ!.NÎ±\x0019âhîNé@
/º
('éé\x0008¼-&@I®\x000b²q*±Þ\x00045ÌÓîÂá\x0008>3¡Ç7ÃâçÌ4e\x0015ö#=º¿ofj\x000b/îÞ^ßî\x0016&UM!\x00141ÉZwR³88,Ôô{ÖÅùó³\x001dªr\x001d¬Q=B\x0005VI\x0000
\x0015ã<AÒmÖ©ÉÐ{?øü>N\x001a­/\x0007o®îïqZ÷äL]=\?\x001c¼züc\x0016Òâó»¡®\x00160ùyy¸è@*=\x0019K½>xs|q»_'çêÍÁ«ËUð¾n3/\F>äÎ\x0000Ø2óÂmÅ
\x001dE|KqG1Í¸Ø\x000eCÍ\x001eAÐd"¯#\x0017¼Â\x0016~D\Æ;Ú¥Í¼ZbðÎÒd,¯\x0005Ý²NêÉc)ï¨¤¦\x0017ß÷ò\x001b-¬¯ÏÊ\x001dÆ\x001bL\x0000P¿ÑSâÊm×\x0019*.\x0016\x0001BÐ¬zî5ÊûPï\x0016\x000b]Æ;*Æi^^#¨^[\x0004ØÉ´\x001deÿFÙ\x0019\x0013¶wT©Ó¼¾X\x001foÔ\x001bJµÇ^ÅÒ£7]¹³wTÆÓ¼¾JS+pl³Ì\x0015Fós
]E\x000by'äc`l\x0011ÎêY\x001e\x0002]\x0006V3\x0002®ËÇEIí\x0006ØQ#®XëØ\x0000³l\x0010_\x000c<\x0016<n^aìwË\x00172¶ä©\x0003pä¨\x001eÎ%Å§\x0003\x001e×Xµ9Ë¾3CÎ\x001c\x0003+?¥º°\x0018xw\rg(*^@Í§B|gpê¤\x0000ÜRÞqÉXû\x0002\x000bdÄ\x0014Î¡×Ô\x001fÀëk'\x0015\x0019ò\x000es©K\JÁUðÑ(ºm·~[;L´.Á-ý¸Ñ\x001bRÊöøwtàÔ¤èíBà[;°Ã\x0018Îã¦oåb¹3Ì\x0013.ðHêm	¯ §¼Éegµ-ìbJ`8\x000cjp6r_ð¬8êJ98éÊ¥Àð\x000f¯Ö8|\x0004óì¦HD`áM1\x0011O¹á¼©ug\x000eü\x0004ª@Å*\\x001bc¼ô¼#ô¤nA\x0013¯ûòçù 7÷W×7³p2\x0004^M%HÑÌÀ ~\x000b;]iõæâòøät\x0006æ\x0017óñ½ÿ¥\x0003süåóÍævóþ\x0013gÿõåúËÃN	E\x0005÷\x0000qE\x001am\x0008î\x0001Ê)ß¹h_¿:=:;úîÓgÇ¯O^¿Ù!¥ØaÌQú"Æ<h1~ÍC[Qä?l·o
bÌ-££÷þ´1÷ *.5~ÂeÌÑø\x0012F	w\x0012uÞá¦©"Ò\x0004\x0013{\x0019­59\x0002_´¨è©Ë:æ¶E@5åX¯AÌQì2DOÏ¼\x00191ËÛ¨­ëÿD1Ç\x0008á.ß\x001eéÜÉA² º'AäHjÙ*FR\x0016(£¨\x0018R²ÝñO´\x001c,\x000cÔk%P 0¿Ä¤\x00197|\x0005Ú57¿}\x0010o»\x001dNÿÜ|ºÚ<âmrºy7\x0002Æ!¯4A\x0015ó'y²¦çî»Â?^\x001e\x001f]âerzôb?HÎÔü¾ '(Q¦®an\x0004ÉÛ¿\x0012\x0004\x000bàCYHÓrh\x001cÕ*\x000eNoÔ¨ü$W$kI\x0003HgEÌb\x0012:m$>æÇè¼$Ù\x0019\x0002\x0012á\x0012\x0012µ$bK\x0012Ë(#~\x000cèi¤6rÐÑ®ä°"+$b± \x0001`oLáX¾I(P\x000f"hJ¥°¹\x0016/ð&±Ý{¸2\x0003$&æÌ&\x0011\x0016\x0013$®+!ØHB1=c@úUHÂÛµ7¸ºÙêIòS\x001c{ÉÏ~¶³í	i5P^¡\x001eDÑ6¡\x001eý%ñ]A\x001a\x000fòÓû\x000fWáäÓg\x000c°äùæÝÇÍ®É_Dò\x0005\x000eWô4ùXÐ]I¿¯0BçG/þy4\x0017MuxrpPÏc±M4;a\x000e>Ë\x0017Ú®£Éq@\x0003pE3+j\x001aç\x0019ç|°ÀªÖ5@Ùéo\x0000Ò*`y¨Þ\x0004-eY¡® Ð\x0002 ìá7\x0000\x0019îÉ\x0010é:ÊUØOË+Ôµyµ@×_ùý©
sã>nn®\x001eæ[\x000cÁÎ²2Þæ¶^p­Là\x001d¢[¢]pnÜ?NßT@
vu
µe\x000c	<ïÛ\x000bTé\ÚI-PÍ]\x0003%X\x0012N\x0019ëèy\x001cE\x001eý`Cúx-P
^\x0003eôv¼ÊÝ}\x0000\x0015x\x0014ëùæ \x0006¼\x0002ÊI\x0005ÊèXVJñà\x000eë»ñë"¨ü\Ü´R(çDS2PH/ZÎ9ÞSV­Ýè9|iZ©­^µÁY^y£;É»ÖvKÉ\x0017AåP¦Í$DV¡\x0007#gØIeÀ2-P9¬iZ)¯x¶Á"9%­~´RÆ¯ÜS\x001cã´- æ\x0004e¤ìpL\x0013ØòR©¸Ò&p¼Ó´VK\x000bF· Ï<5â¡u=ET\x0014û´Y\x0005ªT\x0010Sy"\x0018\x0005ÉçOº»ã¶m\x0015\x000eùöË@'\x0014Ï\x0017\x0012få-ÃÞÛÇL-J÷¹¢o\x0017ÅJÀþwë"ùcH\x0008w\x0014OjÇ+y\x001d\x0015?Þ5QYÉ;JIÖêC¥C6k\x000f\x001f¿Ð5Aé2\x0015ÜCL\x000e5? q>àíÏ_ítØòâãßÿõ\x0000ÁÔ¬ã)°3 _~\x001a\x0002KÉ¢¿ä	ES\x0016á\x0012Þ@Dµi\x0014ºT1åj\x000c¥q¡<1\x0015.åÔB50\x0002ýL.ä7\x0016¥\x0015¸êT&Ð[Õí¦Z4
aö#¢ù\x0006\x0010¹¤\x00127dÒ¤]É4bö3EAu)i;Qi`0^í´iàßU1q\x000f\x001c0i\x0016
¶¸çÒ.ÙNâêöÛ?ç«»yKàT\x000cÊ\x00044ï3àÐV*È7³×ðéù¬\x001dè\x0000M\x0004V»bÈZäÀc9-Ë¿¨a;\x0017*ÔáLT»q¢lTÑ9ê¢<ê-«&Â©Ý@AÑÓ TÎpÖK¢òký\P\x00074\x0011Jí\x0006rtÁI´¿P;g£:fõ<\x0013QÔ/\x0016iô°TèÃ)Ê\x0005òaÝ\x0002MDP»<k}K-\x0005©vRN6Æu+4\x0011=í\x0001òô \x0007{:RQ:\x0000±DÁ²=ýëïl>lfîþ»ë·÷×³þ@\x0019×\x0004ÚÆÙs\x000bUãaMîi0ç§'Ï/Nö\x0013oÙ
"Cç^\x0007³È3\x0011L3ÔµDã\x000bm/¥<ªTÚj[Àa	ôÕ¤N\x0014îFúùË½wwGª2\x0002:\ëm­¢ÞnëÍtr BÄµC6´IudÞq±=æ-´§2.Éò²zÒlD\x001bZ:4pÜ\®0Q\x001ef7`ûr\x0011flf\x001bÙÐ,Ô\x0019[$©).dóÓ[pfé÷÷Ùö\x000fpÇ\x001dÝÜ\e»õãÝío×ð·óÆK;÷[ØNÆKXEgáÿ¿c+NO³éúñüì?.Oàog
*ã©.jÅÃ
ü
ç<á xàÕÆuxº§[ñ¼É\x00151¸z4Ð\x0003*\x001fðêu?à.iÅS¶àIVÆñ¼WÏËux¶g[ñ0Óß¥£4§ÛÇXööq\x001dëâ¹V<; \x0010Ï8ö¢Jq«}W`	ïâùæÕËÅôq\x0015í=J\x001aÁ·u+\x000fnèÒV:0|L\x0017l\x0004\x0001:Mº\x0012ÖHµrëÅ.^\p2\x000c}[å¸4\x0003þKyëÙ¸nëÉ¾Un6Ë\x0000\x0015\x001d\x0019ÈNn6\x0002yï­\>Ù³{²ÙðijÆÅ³\x0011e¬¯\É×³,²Ù´À]æÈòAHN¯öXÌ|]É%|½³+\x000f/Ø\x0016GÇÃs¥"\x000eä¢{Í®*Õ¢k÷ßo>NçêÅ?hÜ*ËdÂj\x0005ÊSÓ)Ñ¼\x000b\fc´¹¿\x000cËË¿ÿú²¹ý°k¨ç©XÒách~WÐàbhË²¼<~}töC
×8Ñ²Kk[T¢ÀqÉ+Q{\x0016ÓÉ¿]Ç5Î¸T¬\x000b©è9©W9
*¢\x001cÃ\x0007?÷äXÏ5N¼T¬ÔÔ-/±¶&íÚÒ\x001dæ0f]Ë5Î¿T¬u¤Á\x000cßÑ×\x0019\x0015ù%\x000eGÖ­Å\x001a§a*°"Ë\x0010Iç|Y®ÒH\x0013I4ìá²åûO¿Ï\x0004­ÿ÷ýó·_®î¿n\x001eî®ïçK±CÓ \u\x000b÷ +#Bä:ùØwpzpþüõñÅOGoÎO.fGl\x0011'³\x0001\x0011\x0007Â\x0013¢#Ùh£Ë§8\x00135ò
OhË\x0012FÖ¿ÁZ{\x0012åÐÊ8¹ñ\x0011µ\x0001\x0011Îiþ'µ\x0010eT³¨h\x0015Ç9jD]Dg)!J_RºÓµ\x000cÍÃ3Ü\x0018-\x0015¦Hô¤\x0002!\x0006¾(¬~0lF\x001c§Sê?´¢çCÎ²¢i+¶¤Ygjgê\x0010ýï÷¿¿ÿ6Ý|µ¹ÿ¼\x0001Çäîv\x000e®#È&£Íã¾P½ª@I!§3¯.^\x001dgr~¶\x001flä¬\x0001Ã\x0016Òç\x000cAf¿\x0013À\x001cW<\x0008=Tlá\x001a¥:k¸tn@.¥x¸çÆ¤\x0018µëgw#ý]ÆÎÅûëOW\x000fóÌáù¤IZÎq/k\x0010_;tëøâäåñùýµÅ\x001a=¿V`iC3«³\x001a\x0002ÊD\x0013ûõX£×Î
,[:\x001d\x001d\x000ce²°º\x001e°\x0006YÎ*¬2%Í;¶TK/4\x000f_«WkT§UÅ\x0015\x0014©\x0012
Ô\x0000å\x001aÊÄà¦Ç¨\x0015QUTÑr¿¤Ó¤mÔµ"¯ÖL	D\x0003×°(ªË\x0008\x001ew
\ßCdj\x0017§èM\ÃÒ¨*.%h¸\x0006lúÈ$é"\x0017túéz®Q\x001dRÝî\x0012i,\x0002\x001dÆ¬Ó\x0011¶uæb¦ð½\x0001kXTw\x00185«qàrY²\x0011¥\x001e_L×üì£ÚÄ·2ÎÕ¿º¾Ï!@ØDE`45?0\x0004C³Hs\x0015[¯NÎfÇ¾nqÆqú\x001e\x001cnWN¯Çy\x001em\x0008E|\x001båLq~?{ømbu^o®o\x001f\x000e~Ü¼ûíqGÅÛêÉ c^"§Ùauaêè½>:9{sðãÑÿ¸
ì:`ýuª\x0005³¤\x0004(uTT\x000f`äë;7eª\x001a¹ú^V%Wà&\x000fJ\x0013sv\x000fÖEø'/ÂF°¾ßP	æ5?*£&.}HËÒ\x001cÎOE\x001e\}Ç¡vÁ\x0002ÇæhO
-gw\x0017ìÄeØ\x0008Öw\x001dêÀ\x0002ÄY\x001bDâ(Uª.)£Ýä¥ÓÆ5ô\x001d*Ápn¢-%Mð\x0010Dò\x000e²Z5`?_Ýýñí~Æ\x0016áÙ\x0007eøh4<@\x0004l¸ÊbK¡È\x0004\x0018?É+Z\x001fû¹Æ)Æ\x001a.K\x0013\x0015Eð!ù]	Ìpë½63f¾\x0001lË«\x0000³çg£ÄZî¯Äa½¬¡¡fz\x0008\x001a¸Æ%L5\"E\x0014ÊN\x0000¹\\x0011\x0011Ó&°qÏE\x0005qE¤\x0010¢FÒØ4E\x0017EÆÜz=×TC
\x0018gï\x0000L°\x001a¡±ìrÉ¨f®î\x00062j¬n$Ó6Kè\x000b\x000c®i\x0012º1U>á[¯\x0006£öæV0MÚVhÏHÖð(?¾Z\x001b¹À)¤3\x001dvÄ¥Ù	^­ßc44³\x0011\x000c«Òó©ôÜ]ëá*'ó*­É°×ñèÌ60_$ÿ\x0005N­Ô<¤½l~3Ái#£	dØ ?¦·EÞKa-RÍÕ\x00187Ñ\x001cÍF2|öÊÛßíp¤ôWäV¥òzjÈnãïbó¾ã½ºÙ¼K\x0011\x0007/7ó*Ö8Mêû¤ÒTª\x0016Ñ½¦G\x0008ß-|uzô"gøßz4+`ýÛ·¿î¸\x0014\x0017w\x000f\¢öróþêæêúv>ÓoI&7þÃÚä£©K2!\x0019ß}s¸8¿|Ãõi/¾;>=>9ßbå»	\x000b,©ÈÚ¨øDnrc\x0015\x001a'!Òãs÷µk!X¾¹ÛÀ\x000c¶f\x001b¡|,\x0013®¨ºÖÚhÖ/X¾¸Û¸¬6dì­T¹\x0015\x001fH.\x001díÞÛ-X:}÷ÇÏãíÕ¦=à¤\x001efy\x0000\x000b7cî÷Á@NÂ\x0019kGPxsÔèö\x0013å°¶ÈbE&Yx/(ÏåËèo0ñb¼­²ûÜ$EL\x0000>\x0003\x0015#á{¤ä"Q?þtMH9m@RøH\x0010JaM\x0000Cá8Îðzåë\x001a$\x0013ÉÑ.Ï#¯¦\x0004IiÖñd;^Ï\x00038¦\x0004\x0016BSz\x0019\x000bVYÇK¬Eê\x0019§ª%Â@¾äW¥\x0018b°µ§-ø-[[E\x0010iì\x001d?:YÔ`»çKz²j¤`\x0010\x000c¦yäÇ\x001de^Ä	½\x0004W5Å!ÎpNÂ$Âº/Ç\x0011WÃ:inJÿmEyw\x0017l\x0014+èñ¤edä\x0007\x001dÔ!ÏÉ"§\x0002gd\x000cëL7G-\x0017\x001c\µÚÒuâè\x0005ÓAÄÀ>¦wël7?æ4¬Sªì&ª°Âu²EâZëDÁhË·ÃÁ(4hÄåÎ\x001bÜásÜÒ­³\x0003ü¶Ô²L2§Ó´\x0000µÀ!X\x0019^H\x0014\x001a7Ù\x0001Éòúø(Rqs`ìºâÙKH\x0008 i79²\x0003xèr-SN¬K\g.ùõ­\x0011®^³
2\x0015=×±\x0007ÞD/o-H\x0010kjv+Y¾\x00089èÉà.a"!î\x0016&åÒ@à\x0014ÿ:¾|¥ãaDÒ®<t¬µÝÀã
¨!Êeõ
'E)`j±d-íE\x0002çßãM/mpÜ5­XvâÌo·²\x001f3=æ¬ÅÑýû»ë/»\x0006]y0¹6\x001c\x0000õ&àðö\x001c\x000eHßUÂº¸Ì)£ïÎO^ï\x0018sÕA¢ ©\x0001	VÆH!ÖÆÐèRÁÅ\x0014²+È·\x0002EEÓ\x0012{%ò;nÔ[MËî;î\x0012$
\x0008\x001aÏÒ$Ê"Y_GÍïæ\x001fíûÑVÂÀóûÇù|\x0000D×ï·ô\x0008ËHS\x0004UW
/ó`>\x0000ÿv¶:a\x000bÓÝDûaÀ\x0000w+ÏµË^z®¾UF\x0016§\x0001bî¡¹F`\x001ayÎ$xEE¹Û½Ò\x000cÓÝÌ\x0015+ÓñýñE`cOÛvÛÌê`ÞJûå­\x001eì\x0017\x001f7·`\x0015_]Ý¿¿¿þ6»c¬\x0000±Rnú°pKùín°6/þyt\x0006VñÕñÅw\x0017'ÿ¹h»qêÀú\x000c$=\x0003V«¢½êV¢.!Ú~°Z"ÉodÒZ}HK¤Jýuë¶¶§ö£9G2\x001f\x000eì3¼\x001e\x001aÃ* â\x0017q3q\x0001\x0014Ã\x001dU6\x0016§åö:\x000f÷k$Ñ\x0008Gjd¨Á\x001cÆ¦\x0010 À\x0018ÎVÙtpú\x0017Ø~\x001c\x0013¸[ÍKVL\x000cÊ¢;\x001c&,s=N×úT® \x000b\x001eb\x0010Ïc¦V,J:ZÉÝ(RÈ-³Qa\x000b\x000e%úZ\x0016ÇÑÚÄÃH4ü\x001aa¥[µ6ýK}?ÌS7Æº\x0019¥I·\x0002þS]UËv\x001cÊðÕ¯M,úÙpkP-¤rÅÃðztU´àPz¯\x001aGPµ\x0013®çzd¥èµÔ*)VáPj¯~utV@'§AÂêH>åaÕê´^ýòÄ<\x0007Çð1ça6Í\x0013ZÃ\x0019½j\x001cEÃ2\x0001ÇX\x001a\x0018\x0015eyâÇ\ÏÃù¼Z\x001eT^"¹q\x000cçI5GÐDt«´oÇyûîÃ½ú<¼"¶Jbè½ØÜüý×\x001fÿ÷ýê/!é ¡(¢\x0006S\x0008]=«Ùöß\x001e/»¢bè½8:=þ×ñÅìûq³c­\x0017pÚHYJcu\x000c²È\x0002hfd»rv,ç\x0002Î\x0010©ýDiË¤pý²ìOµ\x001d\x0013¶\x00003\x0016½`Ô/àåD\x0007Ó\x000e÷äBÎ1i\x00078¶9ïNZ<Áé¢+\x0001y\x0013è/º/<É§úû«û·7àî\x000cqxÈ&H®AJ²\x001eOª)\x001fíï/Wº#\x0014î`õ=À:,\x0015yzL@mÌ¬ÒYâa\x000b\x0011_Õ÷\x0004«°´YX1`y\x0008wõªí´àVcõ]ÂºÕ²µc°Z=IOe`õDÎ§\x0002ëÆ/¿ÝNä3þïÿú?'>cÃýõ|µÅBtVX¤×\x0019±$
øE\x0008\x000fN^¾Â\x000eÙD[¬~f£\x0016Ë§;,aÜ.¢ì¦`éÑoÄê§\x0015ê°à '³Ô­	+òl+äZ¬®K]åê"Ä\x001c¤6\x001eùÊÄ8Ú[5TèøM|0[/¯\x001eowîv\x001cRhÈ¬ÓCÐÙ\x001b\x0008^\x001e_íØç\x001d¾±Ú\x000fc5«Xè*ó\x0016\x0017'&*#&,B=NßHíÅQ` +\x0006Êd\x001c©Jô\x001cÅDLVÓ7N\x0015«\x0013óY¼],\x0015ð`}áÛÅ¯Z~¼Z±::kEäf\x000cÀêp4o¦"Öz~ÄºuPÄ4\x0007\x001dA\x0018ÄÕáZ¢bK;M?BÜO\x0013E²9)·àr·\x0002*Þ9~¹« ùík|x{5}ßïéjÇçÂìzC³÷,Æá¤\x001f´\x001b\x0005\x001dØÐ~±³½C4º:*²H"pÇ8|wje\x000f½^¦\x0005HýÔx
\x00123\x0005Z%§s¡= )î®\x000fvüÙF7ÙþUÊÿÊkê³ø¾\x001eø«É©ë¢§{ä+HiÞGjÈj»ÂÄÆn"\x001a]ªû0HûÈ\x0006Ök\x0010CÖ`üºEêæª*¬£g\x0016\x0015¤Ï
u\x0016Õ\x0007\x0019©§Ô»\x0000©k*à>µ´<M[\x0003$GúÜð1G\x0011^\x001bR7gU»Jº¬%
\x0004\%J\x0007û¨â(OÔÔÏ[Õ2©<V\x0012Ehr!2Ö«\x000f>v=R/WTäÕ!ï%êÕ¨K1ÑO9²õH\fÕ\x0014\x000cõdàtÞ9\x0007&M}?\x001eÅ]V1qMS\x000bSÔ<\x0006?¢U¤rÄs`Vï&. jarÇ\x0019`sY$Y#pýÉ.`úôñ×Ï¿|\x001cú\x0001\x0007¯þþ\x000bÂ¿ÿ{W<ìe2R)K3ÉÁ6.p5
ö÷Èw:wn\x001dq*9Ö©-DT:K\x0018ã ªáÒ\x0004Ô¹á*\x000cÛn\x001e.É\x001b(m¶+4NÙí\x0003úüÍø;1Y=
u®\x000e^ÜÝ\x0002Õ?nnþþkÂSqP0C\x001d\x00182:S6ù18ÊU;Ç\x0007/ÎÏñ é\x0015î'\x001d¾æ·ÂîÊ\x0015Ù8\x001e;W\x001a`Ìmxë'$í;
Í¤¥\x0014:7Ö\x0014\x000c
ªÉ\x0002E¤ý»T
¶\x0013D®¾MÝlvC.%YB:¼<\x001bQC´¼¨\x001e\x0019²ÆïQ;~äX:¸T[QL§<F=#©L	Ì^:¸l[Q½àau8\x001fV4¼ªrô:³\x001cup\x0007·¢B8®iUQêVUÐ£\x001b²@¡\x0005U¿W¿o¦4.þþëÓÝãÍÕãÎø\æBÚ\x0010+z\x0011\x001d§½üTÉÚÅñËóËÓãËÙ\x0010½ÃÔO}Õ0á[4åõ æ\x0007l»ãÄ³HÆµ0õó_UëcR	Ké(«ÂMcV¹±\x0007ÓÆÔOU­\x0013DW3=2=!*ÅYB\x0019Gå}mLýLXÕ:i¥\x00171s©øÑ@(]2SOð-LýtXÕ:PÞ½c\x001eöë$UÉMU¶0õ«8ªÖ\x0006×¤=\x001eÊÈ½JËß®¨«Z'­·i^GEõ\x0001\x0016*rwêA¾©_ÏQg\x000bH·&g3sC[Ø'9~'hB\x001aÖtT1)#¬\ÖçÀó¬\x000c~}\x001aVvÔA©¬ðÆüW\x0006QHá&\[ \x0006å\x001dUP(¦@\x000b\x0015SÅ\x001b2YnþËgÝåÒw#*dîpO\x0019iÍ;*8WRÒ\x0013\x0019é¦Mt×a£ãÿÓDæ·åãà6Zº÷L,ÕTc\x0007¼\x0002íÛ»ÏÁOÉ\x0017×?ÿãÅÍæú~>\x0004´6Uÿ&õwÉ²d\x0012k£s\x0003¾4ã"ï\x000f^\x001e\ìÇéUèTààéüå`\x000e5\x0017±¢¿\x001a\x001d»&^\x001dN\x0005
:vô<\x001e5ÏA\x0015GÐÓ+·©Àyv]úV/\x0014©¸J«Ñ%×Ó¹âêpdY\x001d0GD.%W\x0006j9zÁlÂéUùìÇÑ°$·L§,	§R½?¬Î¨Ä¢	§s±ÕáäQòäu³êmÐ¼:ccÝ3¨-ªàxJòæ\x0011|£¡\x000c(­Q¥b\x0013O÷>«â±9¨Këãéý\x001bîÿ2xG\x000cëëÛxºWY\x001dË¸C\x0019\x0004døÎÐrÕY/]ÇÕ<Ògin\ÎÜ¤²Åè=¬§{­VñçÈ^¿ß\x000eJ¾ì\x001f3ôf÷ó\¿½ºÙ<\x000eî­JµC­ä(\x001cwE2{ïU#Ü×\x0001ÚÞ\u@°2¯`\x0005©8(à³ü\OM#Ð6¢­]!}HúØ<\x0017hè1Å¹bó\x0002íeZ¹@Æ§Ü\x0008öÓ`Õt\x0006²[Õ0²\\x0005´
e+\x0017ÈX\x00062@@µäN)þbbX,Ý\x0008´½ß+WH±öAj¢ÁÂ8QWhø®Ó\x0008´½ákµaËà\C5'Y\x001b6rW«¶w|í
	\x001eÚbåÎ\x0011S¢{sj\x0017ðl/ùÚ3&Ó\§tè\x000b\x0013<EÆ
Úº×|í
É\9}Ú±×ÚÄÄ0Û×HÔ¹è+×H\x0004¶CÞ(DÀ¬(-\x001e¶>6\x0002unúÊ%\x0012¾l"<÷´D\»~:w}í\x0012É*øËúÙ'çbÁ×* Îe_\x0007d£`e\ì¸!ïÌh\x001e&\x0005hÕA+â"õ\x001f
\x00020K.þ+*±ñu6l¨k$ê¼\x0001T®\x0011\x0004=|Ò¬á×S\x0008Ò¨ì6ÈaQW#\x0011KÔ¯×9W¾äÌjÉZÞq\x00185\x0012Üf\x0003\x0011\x0019ÅtDîG²Õ|ÀGYuøYg³Å\x000bÑô\x0004\x0006GÍQ%>¸i|ø½\x001a>Ö4\x0012¾f\x0003\x0011ÊÁ\x0013\x0011+\x0019ºÓ\q\x001c×í#ÖÕl3\x0014ÎáØÑ\x0012ÙÒø\x001cV9X5§ÚöµP9~â]d¸V\x001aü"»n\x0017ÁVMûÚ<1&\x0011iª\x000bFQ*\x0016Ö]jØÑ¥öµõ÷µÅ»6R²ï5D\x0018~4ík\x0012P|X\x000e@(D1¬#]¨öµµoD\x00058:ªrñ\x000f_?\x001a`Wë¦
°¸"Öò=«âárIÐh¯®åÛo°\x001a¢ü××WÀ:O£ n\x0015Y
¯[[r\x000e<©ÉNTL½>9~~|ZÒ«Ú\x0012cn\x0002À¢¢\x0001n :`Â\x001eÏ\x001aPzRûPpx\x001b¯òçP\x0008ëYÏ¨/×HÒË¹î%	¡Ì}	e$,÷»ÐnøòÚÒKpîEqZ¡`«2áHò}FúEõ(dâ^\x0016+xÛbýE\x0019ÅzËÂÚå_h¸ÛË¢"y\x0011^
zÀ\x0010¬;+Ür¢WV»W.sTK\x00055¯Ôè¾uÊêX\x000cÊoÑ	Ê\x0013$ÒÔ)·=AËÍJ'«Ý+.n°õs>(\x0012J,~\x0018jíeq\x001bóV|Ônz³¹¿¿¾ÚQ5|¿\åä"KÞb	\x0003÷\x0018LÕ
½9º¸89-Àìð\x000c\x000b0÷òlå¤\x0014¦ë<ñð\\x0008ì\x0014MªG\x001a8U,§\x0013¥ \x0010&AÐè\x0003%=ö¬C\x001a\x0016î_%j\x000c!)Ö/AÁ\x0005^¥ñåÔÔoV©Z%ÚÒs\x0014\x001e£yùp#\x001bØ4,<Ý¿J^sE¸jr¢W?j0hAêw«T®¦\x000fÛ2\x0005i²R¯\x001eiXôZ±<yÉÊ\x0005PdH\x001bËV¸~·JÍ*°Eò´»=i Ñdh5Ñ¸Þ¶b/9RU\x0016Ë\x0014	+¨\x0012Ó8ûÓÊÔ«Ç©\¦Ò\x0019á`~áMÏ
Ì4ÖZic\x001a\x0015ûî_'§²\x001c
0\x0015Ýëè%×"»0VehcêºCÕÛd\x0001¢­\x0004QéÊÏ6*2Þ¿D¦Ô@[ÁI²\x0008A\x0006%7£XÏÔÉmV_»f+\x000cL5m%10kµî\x001bW8ïgÒBSeÀ$Q\x0001ÇÖÛ­¼âºÙÍjS\x0019i6²ÚÓ8J"Z»µ\x0007]O5DÊ°»dÈÍ°H`ÓI¢%\x000e4[:\x0019×êU\x0012Å,á[\x0010­RiXsfJ¤¢©h970IÍÞÁæÞì`ÿ\x0011­\x001fK¬µ1uòÀÕ¦Ò³¼\x0015<\x000b7¦§¼Nz\¹ØÆÔ
Ø*.gN)v,\x0016ECi¥½ìf§«×I²^Å^â0\x00156\x0004ãjÊ6¦n0Y¿N,5\x0015#éG§"¯n\x000e©gêFuL,u\x0006H¥à0Îª°Î~\x0017Íë6\x001eºç4Îm¤5\x0012e/Eß
¼nÖÚþ\x0001F½¹I&ËÂýñp½cf\x0017·»¡\x0005>\x000e\x0007ê©¥y
>©\x0017´Ô\x0018áþõæd~^W!S]2ÕHÆ\x0003±\x0012>§[yd÷q¨\x0019LwÁt\x001b\x0016\x001c\x0005\x000bß\x001dsË/uîÉ¨Â
2Ó%3mdxñEúÔ^Ý¼÷¥ëÚ¬f2Û%³mdF\x001d\x0012µ9EZ\x0008)²R²«Ö\x000cæº`®qÉ\x001c©A+°4¥»tÞË^sc3ïùÆ%4°TÁ8÷Lc(L¥V}ÌÐ%\x000bmd\x0010bñ\x0001À.¶,¡¢¤)dr
YìÅÆ¯ir[\x0006E«Äñkò63kÀdßÌ6ÚYïIÀDB¬[h(`V¯°²²gÌd5\x000b\x0002ïï|\x0001H©XÊ\x001a|ÈhqÍõ¬l4gp\x0002è0ZU\x0017ÑjÐDB/UW&¬\x0019­gÎd£=Ã\x0011\x000c\x0015N47o\x0013ÝÀµ¬gÏd£A8fÈGªäkÓ\x000eR\x0015÷¦ì\x00194ÙhÑÀÀæÓ)±£$\x00144ºÑÁ¬YµE&M\x0004\x001c¬©º:If\x0004F\x000bqÍªõLl´ià¡Ñ»t É¡©QbHÑ\x001bÖJ¦DÏA\x0013md¨[%é{ªr
\x0004úïiW\x000eÕ3·ªÑÜÂ÷\x0014´Õ?$¯Vò×T+öêû´mNmðù\x0002\x0004\x0005Â\x001eå¯i»­\x001fÍh½@µ¹µi<í3+ÓE4Ïþ¶X³Íz×j»\x0006cñ]\x001cìÍú\x0013ÂR_\x001c©\x0015d½[@µÝ\x0002I\x0018v4ÉLd¤bébt+"\x0001Õ»\x0006TÛ5\x0010*hp
\x0004R¹Ræ\x0011jÕ\x0019è]\x0003ªí\x001aÀNu\x001aæÊ'\x0014¥ ±%4áÖÞ5 Ú®\x0001\x001cßÇ\x0016Íhjë1°(\x000b¬ß¢k òlí\x001f\x000câôï7_¯\x001e\x001evÔ'¡okrý¦ÎÙMl\x0016§fC\x000c ¾?ºüéøÍýhª¦ZÑÐ;ËM9ËÚòÁóÄ\x0018«§/öj:Ý¥Ómt8µ2ú©=)ëP\x0007\x0008ühíP+x\x0015éÒæÏê¸m\x0001k¾¨¯\x0003u%hí¬´!Õt¶Kg[×ÎvZ»xlÿR.õ¶ÓÞG5ëÒ¹ÖµÃ\x001aÝlI´ÐT\x0010pH!­_\x0007ç»p¾ué¼Ëã1°\x0002¤h`é47[8¯×\x001dÙÐ¥\x000b­K\x0017=WÍjÅ/¦!ò´\x000cì:¼U«éb.6®\x0014r\x001f\x0012»â#ÉC»È]\x0018b=¢gEëÅ\x0012
²Ä8¶ /Ý¶ýAÄÉû«®M4Þ\x0013^j®\x001c\x0006%\x000er²Y¸­ª_·x½«B6Þ\x0015iÚ¢¦Í½ù]\x0005¢qn\x0016Õn\x001d^Ï\x001aËFs\x000cà\x000e\x0000\x001dÍ!	\x000f\x0019nÙZ{WÈ½\x0006Ï\x000b\x001c¤G
\ÒÄ\x0007çÂº­×³)²Ñ¨`}\x000cû\x0001\x0006_éÛrþ\x0019èüª»LõÎ­j=·2òLDÀãqN)àg¼¥;Ï\x000fÝ;?tïîn\x001fÀý¼\x0003ÄûÝ§Ã\x001e3ò¤µÎ5#°ûìdÆëûó³7à\x0003èE\x0005¨êªe Ñp\x001fÂ#\x000eJ(#\x0005ÔdìßHª»¤z\x0019i04ªOa£Aàk/:9coÚ@M\x0017Ô,\x0002Å!3è0£øZN°7#ýôÜFj»¤váÇÜJ¦°×G\x0002p+í\x0015].&u]R·lM±wt^½es\x001e¤/ Ó\x0006©
ÔwAýBPª±ñÞÁTB¾µq\x00048»²OòñC4,#U&5ÆáF\x0005ôM\x001aìÊ\x0001¾ÚHc4.Û¦Û5UàSsq´Û¯?lk#í:~äLÖ.*8mãÒ\x0015sÀiãVH§Â\x0013|~Ù¿¡\x0016^Q\x0010.\x0004ò~ÁM\x0017\x001cN\x001b6SnæoCíY~¹ÐôúB\x0008r\x001cÕ¦$u-\x000erà6=Ó?t8«/©@\x0012«@*\x000eé*jÔa&Tl\x0003íÙÓ¡ïY\x000b
»SÓÇ·©\x000e8	NïÅS|ü\x001aº¡Õ\x001fßGA\x001d\x000c%8Sl¦ä\x0013||Õ;üC´Ô³:º\x0006\x000f{'\x00128¬_^
\x0006»ïÂ\x001f\x000cÜÓ\x001f7÷ï¯çgGz-\x0005OÛJÊg¹¸Rknf·Ó¯c?\x001e]|w2;<²©.j\x0002SØ©IûÑå\x001ci\x001bg\x001e4_¹LwÉtÛåg~\1áh8}ÔJÝ³J0Ó\x00053mK¦-U¼HìÀ¢ZyÅ\x0013ÊpÆå
0Û\x0005³m`Qqp«CäêF-xÊ·ÓÓé¼J2ß%ómdAp!FYñü1UÉ¾;5\x001dìTÅ.Yl#óÃ0m5WÎ*ï9â\x0016ÓÑM\x001dì6¡¦PVc\x001d\x0007­\x000b%K¦&¯J²ÞÉmG\x0013\x0006ef1GeÙÊ2Ó~A%Zï\x0008ÈÆ3`Ê\
Mã\x0011Í\x00145LcV¢õÎl<\x0004¦èÐ "ÙnÍé½3 \x001b\x000f\x0001F$´h\x0008ÉóO#gMâ\x001a¦z@5\x001e\x0002!ËÛqIE0§Êù\f9¬\x0018\éV\x000c®ôûû»ÛÝãâ²<t\x0004½zÂè.v2êxytqq~¶kh\!T]Bµ0Òì	)¨Ð<\x0011òC	\x001b\x0008uP·\x0013\x001an=X@M\x001e\x0008\fdLTö3\x001b\x0008mÐ¶\x0013ZErM"ÆÀ©\x0005¯¹JAùéªÈ\x0006B×%tíÚ\x001f\x0012`0ì+y.Û]:ý|\\x00058ô}mÏ÷}<xù÷_ÿ×Íü`\x001eÔúÏa\x0004¸\x0010EZÊI7iüyyðòøèt¶n©TJµPy|q'*kI¥Ý	¼\x0012Jw¡t\x0013÷,\x0014C%HÜ\x0006ÏPa"Á^IeºT¦ÊØÿÇÜÛåXvãø¾S	ÜDê\x0013ç)\x001c²ã iDd\x001aÝç¥\x0011eG\x0003ÈÊ,äG¡û<õ4z\x0006§ÆáôH®¸DjK{¯\x001d!®\x0007÷v\x0003
{;«úg-¤(òON«.\x001f\x0010E÷*´\x000f¸\x0012"MRùÊ«¨Bà\x0006:*wY*\x0000\x0016)>ÖvaÅ®MB\x001e*èÊpË*ÍVQ \x001e³Pùç¥IªØSEÝ^÷\ÊdäN¿ÈÍñ\x0010QïÜy¤J=URQÑ5×
£H*yÑvR\x000e*÷PY\x0005ä\x0001Î,ã%,Àö\x00011m5V4çbBn_5±\x0012Nq·hZÒ¯\x0015\x000bVj'±FË®2íø\x0013:yÃJÁp}yÙî+wôI¬Á´[mÒQGÉÅZVK¦!\x0019]k¯x	ë¸\x0002Í¶
´Çê§ï>~~ÖG»\x0012+:~Û5¾ÎsÙÅVõàÖTwoîuÐÇõg¶ÕMa\x0016Kº¼êÖàÁ¹ö¨{&BäÂ\x000bU\x000bfx\x0003åÌ¢\o¡¿{\x0016Ì÷`^»`E\x000e©+9ñ\x0019yk\x0008v\x000fXìÁ¢
,\x0006¹a:j¬ã-f%\x000f\x001a\x0006mA5XîÁ²
,\x0018Nz\x0017«.\(Os!­g2æ°ìx$Ug\x0012+^´jQ¶X	ì¥&¯\x0017ù¾@\x0006ö(<-?\x001cÝÝî\x001fþþÌµ7Xyê\x000b/á)Lñ¸Þ"yõó3·^ár=Sq>\x001aÏ|¥ÒbB	%\x0000Öß.ç¸BÏ\x00154\`QæÂ-\x0013À«Ú\x001fIè3]SãJ=WÒqµ44£ª\x0016ö\x0016.ï8\x000cþæ\x0002;:#êã\x001a6þýãPCõ3bÆ·çò\x0012>×\x0002mæV±nþÚ©_\x0004\x001e\x000ct`V&9[¤)\x0004õb"F\x001aÖ³þ³`Ø¡\x000e\x000cEÏÀbìzB
qØ\x001d­W?Í¢¹\x001eÍ)Ñ¢¤¡\x0016Æ_ÓV\x0012¸ Eó=W~N'ßt_SÒO!­g\x0016gÉBO\x0016' He\x000b\x0015ð"£Y/3%Ìz¦x\x0016-õhIFÓ%ä\x000cXO!Ê÷´ûgîÑ²\x0012Íp·«¥I,Í¡½d¦õI´Ã%i1iFÇ\x0016L-AÅ¦eÓ\x001eLp586Z[¥¹µi\x0016°I$F\x0011¥"u1Y¶ÁàZ¥Å-N\x0011£ÈÓ:#£ÅéïÙmv°¹VitIþßÍÛ[kY·Ôv¸=Ô\x000eF×*­n	øBW¼Ã,ª¤\x0001×{ÒgÙ\x0006«kµf7ñÛ¡ ÞeÙ\x000cû.²ÁêZ¥ÙåDÁ\x0012xx\x0019\x000fQ\x0002H1»n½Bw-\x000elQÇ\x0006á0ö(5ã&æ×/Â³dC°J\x0010âeæ½¤407gåÓ/
Ù\x0005¥ÙÍ%\x001aâz¶pPkG'·N·þ°9Ë6\x0006JÛF=W­\x0019Ã\x000f'\x001aTìA\x001bÌ\x0007(ÍGrâä6¹Å¶j´Þû:Ë6\x001cRP\x001eÒr%q[(íGÈ»N\x0002\x000c'\x0001'ÁWY%Çaùf\ìÄFÑ¸=a8\x000e'\x0001'\x0001åQ©x+ÃÓÉKpdíLÏðKl%\x0002?ê0U¦ê\x001f\x001fx`ëÕ¯\x000f¿>=<s\x0011,ÓH\x0016®ê ÆAf\x0000ÇÁWýróÇµ^]_]ß^½H\x0006=\x0019èÈ¸Ti¹";\x001e\x0014\x0016³äËí"Ã\x000cÕk\x0016ëXÇ,·AÆï¾%6\x0019>§\x001aÍõhN¹hP§ÔyÜ¿§72{7\x000c^Tæ{4¯\5#Ã'#ÉiE^µ6*ÜBÞ\x0016z´ D[ÒÛË°w#I¢,Ã`<D¿ë{Æ,ª\x0017Í\x001dòjõ5³,\x001a\x0008\x001aìÛj©GKÊ­fe|xq\x0001K±Ü²jYRXiéÈ=ZÖ¡*jD«Fb ¼jÀ·\x0003Ê\x001dh]c\x0002Ù[£ÞkgN?\x001b\x000f'\x000fÔÛÃ6ú\x0002¥3(7ò\x0011Í2(ÔdÝÆö#5Ûà
¬Ò\x001dÔF\x001fSãY\x0012O%³kÁíb\x001büU:\x0004\x001aBXOi6'
ÄlÄ!à G«g\x001b\x001cUz\x0004ª¨ëV¢Ë*ÛYÖo\x0008¾\Q÷x\x0004;x\x0004«t	¾K#6zaDÞoQæG\x000f¹z¶Á%X¥O(\x0017=SÍ[9mNPp24>]6dp
Vé\x0015Hµ\x0006m%jãâÇâå[éÙå\x0015ìà\x0015¬Î-Pá/rUr#5Î´¢\x0012»Ç-ØÁ-X_À\x0012áV\x0015\x001aÚ\x001cÜaJÀu`;Ø`ð\x000b ó\x000bô\x0014ê¥Â$p\x0019@Ùc\x0012¹9¿ÇÀà\x0016@ç\x0016¨\x0000>qEx¬d<Êª%³çÂxGÐy\x0005R:°\®5í¶ºif÷\x001cR\x0018\x0002èB1^<`°Yõî)Ç´²y³ËðÂà\x0014@ç\x0014hÈº¡,åL&³À\Y7³mp
 s
TÞQ+»KÀ`Ù¦E²®Û¾à
\x0006§\x0000:§àÊª>B\x001ad°<å	e@¼}lS\x0000SpN%`r\x0014loZ¾ê®o:8\x0005Ð9\x0005 \x0013©,´cj½oßÔìqô08\x0005Ð9\x0005W:P
E\x0016kBlû/¼\x001fÆ\x0000«Ùpp
¨s
þ0iÍø\x0017jÝ(\x001clHÈ{ö\x001b\x000e^\x0001u^\x0006f°
±¡ê\x0016\x0013\x001bHêö°	\x001aíu4E£Nc\x0003\x000bUà¶°\x0008\x000fÖló¦é¨À¢üÐ%Ü®Þ?þûÃß>=^|ÿôÛÓã§s|tc`·µ<\x0011±ÜL\x0004hRætÏ]½ºù«×ßß\x0015ÒÛïooî^\x001e\x0012¶@bk¦n\x001bi\x001e\x001eúyµ®Gt\x001b\x00109]³¼ìJæ¦¬cj\x001aopúµ¡\x000c\x001b KD,`\x0018¤,6E\x0017¿^ÒB¦\x001e2mÌË=b)\x0015
õ\x001c½<Öø±\x0016O	\x0019e\x001a\x0003vÇæú÷OïË©þíñâ¯ïÏWðÒh'974 ½jã$#5@>ë\x001f¯î^ýýÍÅ\x000fWï^¯ä\x0015Hè!a\x0003d,\x00017(@heÄØ¤âiS
=$nYI\x001azÆ\x0015eò°±\x0004¦®D§jL×cº-kI\x001d\VRütM\x001ag\x001a®.aø
0}é·`È`\x00053ÊL­^4­ÄjÌÐc-îðF\x0016#ÏÏ)ÊÒÓ7Ø±Ç\x000ePàSÖ\x0005ß0kÅaù\x001b|ôÔc¦-þPîÃô L\x0019ü\x0016¢\x001d<7bæ\x001e3o:BM\x0015ØE\x0019\x0008NG¨½Ùîÿæ]F<`\x0011W`ø{Çi\x0016@¥J^Íµ+sô@[\PôÈOàTÂÈ*)ËÞ4¨z7æàì&'\x0014[ó\x0006U¯°\x001c·JT¾spCv\x001f${S
<
-¬·LüR\ãN#85çàì&G\x001cvþÒñz¢¨kkö7øî#²<\x0011)òÔ`³\ø9úÈ2	º#÷HvpDv'ÊM`Øó´jâ.¿@ýéû9\x0007Od7¹¢,#©,Õ¾p#v­ö+~\x0003\x001bo\x0007Wd·ø¢\x0012\x0003KøîYÕ8TÏ\x001a\x0012\x001b1\x0007Wd·ø¢DR\x0003|å<PòþÓ\x000e3-Î\x000eÈg§	ÏÕÊ;lÏ\x0004û×\x0013\x0006g\x0004[Q²QW1¢lY<:¯g2aÿöñF´Å\x001b%LµV8]\x0015õ\x0014Ñp¦oðÝ\x0007o\x0004[¼Q¢î¸IQ\x0013\x000fÄ0b=\x0013¬<Â¨1\x0007g\x0004[QÇÑÙP¬'òrzÇ\x0015ÆÉåýÖ\x0013\x0006g\x0004[QrA2H\x0001]\x001b0bE&0Ñ+ônÎÁ\x001bÁ\x0016oM^\x0013'¥yªÆÍÂþ\x000b\x0007\x000cÞ\x0008¶x£Tn\x001c|i\x000f$mÇdPTªû\x0006f\x001e\x0006o\x0004[¼Q\x000e(½Z!/\x0015£Ëx1
Jé\x001b8M\x0018¼\x0011lòF%ö4lÊí#ò)²bÂJS3Â-Î(û¦ÂT¢
\x0019$W\x000c)\x001bùq¿UÂÁ\x0019á\x0016gD¥/<GR`®N­2R±\x00192\x001dÝ3Â-Î(§ÄµßÅWíR\x001a\x0019(\x0003\x001a2Äý\x0017M\x001c\x0013t[|Q¹\x0003É¤­\x0008µÊ\x0019µ²+µ
jÌÁ\x0017á\x0016_T¢7IÖ L¨`\x000fËù
B:\x001c|\x0011nñEå³JÇ\x0010¥Á\x001cÛxàú1úìû}&\x000e¾\x00087ù¢ÒkB	¦ÈÆS\x001a#³[)¶Pc\x000e®\x0008·¸¢ì¥\ÅF\x001aW)½\x0008eÿ
Ò 8x"Üà±"&cé*Ç\x0013ÛjopkÇÁ\x0013á\x0016OC\x0013N,^©ê¸ÐØËÐ8Óþl\x001b\ÛàñI\x0012È$ß\x0005¼ü\x001cMcö/§\x001b<Ûä²çqî%Ô\x000cõYlHªPBd?çàÜ\x0006OHîã¤d¹ºÛ\x0017£\x001c3­Ô\x0002«9\x0007Wä6¸¢ò©YÝ8½ÄÇà¡­ç78ín|,ÚàRñKs
÷P';clÍ"P¾sðEn/JT\x000ffxð" L FÀNã
¿Áq\x001f¼Û`äËþLÒ\x0001½ç\x0019ö(µê4\x0000î\x001b|÷Á|º
æ3QMQ\x0012N/Ó©Q$¢Yy»ÖbúÁ,ù
f)!Ä{*Fgµ\x0007\x0011´$]õý\x0011\x001fN»ßrÚIÅÂÈ ã\K\x0001¼¦`Nß \x0002Iÿöç§ÏGî~ÑïQ@ãpÞÛ\x0016F\x0019ñ\x001b¼\x0010;s[Üç6Ü\x00042\x0008\x0004i\x001c\x001fýVùÝ7Ø«\x0005÷ËRëÑãÒ/úEµ\x000c\x001c5+2\x001f,/7ùìü\x001eÚ\x0008ÿ6D\x0018Ú\x0017/Þ?\\¿øûÓ\x001fÿçÓyY7_ö+r\±¦Úhüxk\x0005|\x0017¯®.®_]ýL\x001d/\x0011BO\x0008zÂrm¯éOS\x000c?¢ie|iµ4SC=!ê	ãË&nz
®\x0015hÚÕ\x001ao
¡ë	Ý5\"eD×\x0013m+ÓÜû}Ïçõ|\x0019Ø§\x0003Xû<áA·r÷&\x000c=`ØtL\x0002×|{ÑË\x0010åÃq¼Ý\x0016ºØÓÅ
Ë\x0017¥Ò,zä\x0016iDÉÒç½©'LjÂ`j\x0017DÊ¹X\x0019'ß½·/Qû^ÀÜ\x0003æ
\x001fè%Y
ç14ÕMØ»]\x0007Yj³\x00011Õ\x0000\x001aå@F\x001capÒ¶!Ô\x0011¾DïL¼:\x001fãBÈªÔÎfYD»Ú\x000b¬A\x001cÕ{@~;!Só&­Ð\x001fíj\x0007©\x0006qð&VïNBË;ZùÌÙò0£rEQË5«]è\x001aÂÁX½;	%\x0016÷¼T½.r3­E8Û½88\x0014«÷(¡\x001c°e	©Ð^ÔpÄÂf\x001dÞàN¬Þ\x0004HÒÏ_ÎG\x000b\x0019ÈC<½\x001bê\x0008\x0007bõ>
ØYü1£¹ÌìS¶\¿\x0012kë\x0010\x0007b78\x0015¢×@%1<h\x001b\x000f*\x0017«=ô\x001aÂÁ©Ø
^\x0005b\x0015M&Tÿ²Yztqµ×T\x0008W
^\x0005¹Úý]\x0013AJ"b\x0002°Ú]¤A\x001cÜ
lp+Xkê\x0017\x001dãË>Í^mTÔ w
n¥ ²f	¹e\x0011E\x0008f-Å7\x0007hUjì¨RóõâÇ\x000f\x001eÞ_¼~úõãûóm=Ñ\x0015·\x0012¥ü\x001fd¾ÇÀòJýò÷ï.~¸y}swõêâõíõWç»{ì±4\x001d¥a\x0014 <mc©®O¬³ËNlóWµÓ÷~\x000b§§¢!®[?ùØT\x001bóÊK½\x001e4ö q\x0013¨måT¹ÎEÌåÎ%\x0005Yký\jÎÜsæM¤\x0014ÇI0s0Rñ\x0012mø\x0006_ÞGiÓY¢j[àzkc9ÐÍA´>B\¹t8KvÓa¢:Vk[e82\x0007­äz¥íGO:&»í8p\x001cÔy·CåC­úö\x001b\x000e§Én:N¡xrç¸\´MÄ.SÊÓJÕµt8OvÓ¢:¼ÌõÌ	Ú\x0014(R·\x00125}\x0003\x000b\x0005ÃM\x0007ò\x0003Rn1«ËBurkejÒá@Á¦\x0003U\x0016MTpFºOyrq%¤S\x000e\x0007
6\x001d¨C[ÓèeÂV\x0012Í°â79ú¹Ïîó^í²û\x001aà\x0012D­Ê¦µQ:\x0019\x001bÌ·p¨`ËÝ\x0008\6\x0000w\x0007Q
\â9pÁJé#¥\x0015v\x0000C:ýÊ½õp¼þç×Ï_>\üðé\x0019Âò+[\x0000S"Ó6Á;È\x0008\x0008ùô\ýÏw÷oo__üp÷2\x001aôh B[¦\x001eÔ\x001b\x001cD\x001eB(âÍVÊ1\x0015d®'s:2\x0013Ø\x0013ÑüxVêÌåOÉ\x0000Âµû\x0002Í÷h^\x0016R°<yÐ\x0004W\x000b0ËE¦çÖFNûÐB\x0016T«Fõ\x0018.µU«\x0013Í²AÞö®ZìÑ¢rÕ+oL°AÂcS[Èã¤h5ZêÑzÕXÜ#Ñ\x0002Êªñ\x0010ª\x0000fEM{´¬[5L<ÿ\x0016|Å^È¢íùÝÜ.²iF·f¤PX\x0005*R4|¡ÉälÔl\©àW°öVep©*ÿ²O\x0012õ¯ê¦i\x0019È°,ZZS7U 
öÖª\x000c.y#¾\x0006\x001a\x0002¨)Ç(±`ñ{ì­\x001dì­U\x0019Ür>³h\x000c¤ðXÉP\x001a\Êõb\x0017Ú`o­ÒàR3SõR\x001e¢dð)YõÈo\x000fÛ`p­ÊâÒ®âq3eÙêÄê\x000cxÙÌJ¢D6X5«2k%
â'\x0013êÄm"3r[2nÛÑ`°\x001e ²\x001eË	å·æò\x0019ùªQv \x0015»Wrï
¶1$R\x001eÑrµ¬µÅ½s
\x001eí6ÓJÈ®`\x001b\x000e)è\x000eé2Å(\x0002\x000fuOËùÊ\x0016W.>
¶á$î$P/\x0002ë&¯²2P$rÀ=§\x0014£\x0000º£\x0010ln\ØHé Jý&gE0ôÛ<\x001b\x000eg\x0001ugÁ\x0017\x0017Õ@2PÙ Ë\x0008Ì\x0010vyR\x001cÎ\x0002êÎ\x0007Éh>Ë,áBÉËFSLö 
G\x0001uG$é3³¿¬³
Ë²±Þ\x000fk:\x00063lxTÓU~\x0018ý¯\x001e~}æ
"×9¹)G\x001a\x000bÕ\x0006\x000cp\x0019Ò¢F¹¾ºº~\x0007z\x001eæÁ\x001f¤ônÛ+¬ÈKÚ¸ö
;Å=\x000fÎóÔ
µõ3<!Y¿zQ`q=e!}ËX.é¹Ç\x0003\x0019/Ì\x0016ÖJ²¦|\x000fäghL]\x0012qÈ\x000eÛ[Ü¼@¡ç	³<`üÒéL@FDbr<wÊ¸ÒÔ1\x0007\x0014{ 8½@\x0000õU*e_Le\x001d·@¦ÿ?oWSþ\x0013@©\x0007Jó+dk1lY!gæej¤\x0014ÛØq\x0006(÷@y\x0016Èf«çOV»\x0019\x0017
Í¶BaM\x000br\x0006¨»-âX:õ<Q¹7È¬	*b}ÊÛ1Ñª\x000cõ\x0014Ñh¢§m4¥¼å]\x0014¹¸'F+vÈ¬ÕÁM\x0001
6ÚN\x001biªQ\x0016CD³ûªjý!¡dÒÚÓõ³DàÌèÅÊ\x000fceò/~+\x0000ç-<[,\x0013wåÙB&¾°:½äâ»ïË\x000f/`a\x001a,tml\x001aDÖ$.¡9ÌªÜNå{*¯¢ÊÜKcåáÄ\x001dfX­mLSÅ**¨"\x0019ÿ!\x0012A-ÖRô/W\x0014+¦¡r\x000f5P\x0016¥Ûd\x001a©PIÊ¥~µLc
ËÛ]³ßIdÌÊ¬@¸,%õãZ\x0005¶s
ûÝj6|¤ê\x000bæ¢áêùHñ$ßõ\6\x001c¿jåUã»_ß?þãáÓo\x0017??|þòøõ¼Üfql2÷Ñ\x0004`#\x0001\x0018\x000b¾ïÞ¼{uóËÕÝ÷\x0017?_Ý¿½ywVgS¸ ç\x0002\x0015W\x0010Ñòr¹CÎ\x0015eðb·ÐôÒ{j0ìÁP\x0003Æði´.À"\x001aIý9èsXj.×s9Ý\x0001+
ÛE¶?ðÉpQ^gM
æ{0¯\x0002+·ºÈ\QÞxÁrÙ^áê¯.j®Ðs\x0005íñ\x000b©q Oº \x0013ª
X¯P¦\x0006=XTí0H2,Ù\x0006/O·È³!C¿gç§+é\x0016,Hó­)$µ0¯,¼2â®\x000f{®¬Z/%*\x0017\x0018\x0010ùKôÒÄêB\x000cÛÁºx9Ô×\x0015Å%Xú\x0015Ë¢Þ\x0005Íè#ö©[5ÙhõUf\x001fí
õT\x0002d	u0H\x0003½\x001bª,ÕdÝ·:Ã?Â£x2$Q\x001b)_{G²µ:\x000bK/ëü5ç[k\x0006U\x0011pHªÉ\x0006Kfu¦¬ÉÉÌáRÀ$nÅ¸gÅ\x0006CfUÌ\x0015_ÉºF4	­É®
.ñô\x000ea\x0007Sfu¶©®XÙf\©],ñO{¶ÿ`Ë¬Ê9J¬e\x0013eÆMvQ\x00195l'ÁÎåÌ5&åËêO\x0014ùH\x000e¦þLM6\x00183P\x00193\x0017Ü²·x¬:?,ºöÒ¹l\x000cbUÆ¬Ä"*K#d\x0010xÍD\x0019³ßC6D± 
cË\x000füL¼ÜG¸V\x0014\x001fdáp\x0011\x00063\x000b*3["{9\x0001\x0016"Ï¨ÍhEØØ\x0019»g
,¨"Yzáá¤\x0005¢L%ÌÁ\x001eî¼»¾æà\x0000@å\x0000ÔxÍÐHñ\.$\x00042;<\x0000\x000c\x001e\x0000T\x001e¥e\x0004½;\x0014w£\x000cCöä×·
\x001e\x0000T\x001e\x0000©wÍYù®¬÷2%,ÛÉ\x0006\x0017\x0000*\x0017PÖ¤¹\x0000pÜ`C\x0008ûÌ\x0019\x000e.\x0000U.\x0000s\2*´f9Ë\x0001p \x0015.ì¹\x0002à`hQehË\x0006\x0017=¨åµÃs¤Á]t\x0007Øñ5q0g¨2g\x000eÌr\x0019'2ÛîåÎ·H\x0006o'\x001bN\x0000ªN\x0000
\x0005ñï\x0000¶¢\x00162©¯
4,q;\x001böSí3jUB\x0006sr\x0001.ÿ+Û,á\x001e°a9Ý6£\x0001|Õ$IÙºdÞHº$ÝvÙ\x001fÝ6#ÝÐêÀG\x001e\x001eVb \x0010Ck÷¤ÜàÊ7¹dE\x0011|¹\x0004p\x000bZ;F½l'\x001b\x000eÓ\x001dbÎ\x0002\x001bØF\x0013øv4=Ä\x001dæÌ\x000f\x0007Àë\x000e@±®-\x0008<W5û&OîÁí0g~8\x0001^u\x0002¼iÎ	".¦\x000bY\x0003ÛòÃ\x0001ðª\x0003àMlY è%Ôö±\x001d\x0000\x0008;¦\x001f\x000eW\x001d\x0000O\x0003Ár#ã,P	\x0016]#ÛaÎüp\x0000¼.\x0006J ¾6Çæ5­TcØÌ\x000eÃ\x0001\x0008ª\x0003à1æ,%8×\x0012L£aO}l[YÞLè\x0007ÅefEpò8.¥Ý>\x0002dCôxÆäñ9Ò¢å<]ÿþø·§\x000fK\x0003õÿç]ýíéËÓ\x001fÿ<ÇVb°ª\x001cÙÐ,ºÀÝ#7\x000føhú|Ðõ7?Ý¾^:¨/®~º}{{¾¿é §\x00035]=g0\x0004~ØÅê2\ÿð«gÃ
Õl\x0005'\x0016Ó\x0018;/+\x0017\x0001Ãz:×Ó95\x001d8~1^òØy#ºD1örõl¾góz6X¡
ÃÈ5O&Kñ#ìÚs¡§\x000bzºÀâq%ÏUÕÖëJ¼¹\x000b.öpQ\x000bg3Ô\x0007E\x0003¤^Â¥GAÆ¾íMÏz¶¤fÀ\x0011!ÍH.ú9ÔE\x0015ïºkÓå.«éHÝ«\x0016:Çum"aH¥£{ÖÎfXm­\x0007~Z7P:Z\x0017åËÚ¾íG7Øa»Á\x0010§ep\x0003}[\x0012©g"X±'ÃÛn°uVmìlpü@Eò¾<p8.sO¸dyßâ
æÎªí]¹Êð¡µ%ª!]¤ªÒùöX\x0014;;«µw¤ð3+ìrnÅ\x000b&\x001c(÷xY;\x0018<«¶xå\x0004pí±/ëöÐ\x0005»ÇËÚÁäYµÍ+nZÂ§%1Xñ)lã¤q×Á\x0018lU\x001b=\x0013ì¥hÂÒ=Ot)>æ0yEM×I QpgÔ;/Õé:Ëìw\x0017*?KÝ¼vÏâÁ`AmËÖ\x0011ë²$ümQ\x0014Z©óq\x000fÞ\x0018\x001akMr1i"xlèé£\x0006Q>X\x0015ïw}Û!8\x0006utlÚÃ\x000cå\x001dYTâ\x0017^»{l\x001e\x000c\x000e\x0003´\x000eÃg\x0017¸ð¯8îú¸Kçxd\x0016IîZ¼Á$Þ$SÛ4[dP¥\x0004wB7¼ëé\x0006\x000cZ\­©ãÆ¨ÆgJi§°'ÌÁ"Ö"ûL)ôz,L\x0014é(mKÿÂ\x001eºÁ Ö ~à:2ú/ãÞî²ñP§=x8XdÔ[äbòêh\x0007Râ¿ägPNí0\x0002KO7\x0018dÔ\x001adË5Ûq¤\x0012ÚíÇKLÅ=t=Fµ=Àã&HS$\x0007i"¹åù>u­Ç\x001b³\x0015Z\l\x000eWú´õ$z/njXÛ7XdT[dëLí[.«ç¥Æ&xËyO\x000e÷Xd\x001cBxÔðeÌrXiõ KìQÌ\x000b»íà/Pí/\x000c
â©
@tC]<'cIwuIÆÁa ÚaØ\x0000Wîd
0}[gä>³2x\x000cT{\x000cª\x001c4,¸\x001a-\x000b®Ò~\x0012f·\x001d\w uG	Úëß\x001f~{üðL¿ëRÝË×Tg\x000fS·"¤vu\7y×?^}óú|¿« a:´róI|/#\x0011(VFÂÏ¸ºåfÉ|Oæ5dT%R{ÒS\x000e±ÚäIÎªõë¦d\x0016-öhQFóÍt\x00027ÂD42° ¬ä.´Ü£e\x0015\x001a{v¬
r\x0008Àó(B\x0008¥(®¿W@P£ÙáZÕ\x0017-¯_fP'?òä!l»Ç&kw±¥-©Ø(\x000f+ç\x0000"\x001b·ej\x001f{uÔlÝ\x001dÛ\x001dß±_fóï\x0011ÔþÈ¡p\x0006w!a×=»­»Àºã\x000bìËh¤~\x001cÛåº6ªÑ í\x0016j®§cgÙÜÀætlåî\x001c*a\x0010\x0003¢dÙÉ9ìa\x000b\x0003[P±ÙlY\x0005ö¼×%\x0017EbÝU_:Ë6\x001c\x0005Ð\x001d\x0005[.\x0012bZ),¤\x0001RâHÉãogÃá( î(´ü:9ù wêEUÝ­§fÑ£º£`­«]·4£\x0003.¹WZ$-phÞÖ
\x001f\x0014u\x001f\x0006r°\x0014}^Ò$ÁFaõ°wÍ\x000f\x001fÔ«>hñFuÄ¢ümYA%¼.©§ï±m~ø ^õAK\x0000â$Þ$æo9\x0000×\x0012;\x0008\x001déÙ\x0006ûáUöÃSË\x0000\x00178MT¯
Ésñ¯+h{ì®\x001f¶Wm7OÏ­üI\x001d=ÂÖ\x0010¤0GfsyÏºa»\x0005Ýv£BsÏlÔ¹_/	Ñ °a\½$Ì²
þ*¨ü_Þ¼ª\x0001ÁxàMÖß¾¦c£a\è\x0017¯OÜÙF %©È°Æ!¸~Áz\x0011Ñ\x001f_°üxÁú¼Ìûíã\x000f\x001e¿<#ÖÊ5·>\x001a© ,UçÉØµTõý21îû7¯_ßÜÝ¼}\x0011zFØÂHã¹\x0018\x00192r\x000b&É\x000cîÇÄ\x001e\x00137`ROee^SËþJÕ°f_®Çt[0
Kloî¤Ì\x0014%¨tgmG*)CO\x0019¶PÒ\x0006^LwÉk\x0019e|@´g-c8:=å\x0014\x001cNÏõÇ/ËÑþÛÇ§g\x0004{Q\x001aïM"áèZÚfD+¬D«þt\x001d¯ß¼]ÎöOon_\x001e\x000etpÆ¶\{¤9°U\x0016'\x0003GVa­²MÃ=\x001b*\x0017®|N\x001e\x001cGJªÜPb$%VB¬xúi5p¾óÊÃ Â\x0006aÕ¬S\x0018!X³òð©Ë=\VÂEI\x000b\x001cé®U]Ð9%FOÞ§vP\x0001gÇó <\x0010&ËùÂâL\x0017Åo²çì°ç¬vÓa«»ëdM\x0014\x000c\x0013p×Ò\x0019?Ä
ËÆëB¹\x0005ÄÊ\x0014&R2¶~Ýv.LÓhf\x000e\x0011­\x001d\x001eÇ
>>ýûY°HÎCj=\x0013\x0019Z]öj-j±Åwonÿå%*è©@CUªå.CZ.V°	Òf\x001eÌjªb\x0012\x000b{,T`¥r#ca\x001d[B\x001d\x0011¿ÜF¹õ%¬\x0005¥X®Çr\x001a,G´T½[ëÄrñQRÂÂÚ\x0005c\x0012Ë÷X^l«ù\x000f®VÕrVê×Íj|<\x0015z¬ Áj°\x0016¯m¢9F[¯¾¤=UT-Vlß0bíª¢ÅÊmkåµÿ$Vê±\x0006\x000bã%7 aYkµú®?I{ª¬\,`,_¥2ÅJÒ·w|Ã~®*.b'ó\Q\x001eÊA4u$_Òh|\x000e·C\x0006^cáixXør£©é´¯VOB
öÝj\x000c|*VÛÈÁ`5ð~É!W(\x0017·\x001bR;Øw«0ðBÄÀª¹Î«¤ùõ(:ã\x001eV_d&¹\x0006\x0003oU\x0016>\x00037e,R5±\x000eª7¾é!í \x001aì»U\x0018x\x001aÃ²Å\x0014Áë¦'uåCïà\x0014Ã\x000c×`à­ÆÂgæ\x0008mµ,ðo}ÐiÇæ\x001a,¼UødhÏKO;ÈG$'Ñ»°Ý\x001fÚÁÄ[§Ò2VM\x0003àvÆ²\ò\x000cYÖë\Ö`k0òVaåIëh-\x0015ç§j¹Ð\x0004éf\x001c¦+¹`°ò ±ò2q|é\x0018lß±\¤\x001dW²\x0003Ó\¡\x0007¡O4úVH$\x0013ªñB0Ò\x001aWß\x001e'¹ÆX^cësDo\x0007ô¶W×ËzY.¿ã8\x001a\x0018ïftÍ\x0018Ò¸/G<Q¼£[îK8(R[.¯\x0016ñ¼@gýÑ\x0005&köÓ\x001fÿüüðá¯Ï¤FKü«ãöôi\x001d\x000bç'\x000bëfÿ§û«×?Ü÷G÷ ¢C-\x001dm1\x0019¯\x0018¤×\x0018AiõÅvÎõtNI6ð :ÿ3¡ÞÊü?¿sí|OçÕkç9ªö!ð/Ä6æÍõHq\x0016.öpQ
N)Û.rv\x0016"t.#0\x000b{¸¬±Í ´^¤ÁÐX9\x0013ë\x000fÞÓt ?³'ðÊ9å°æ`\x000b\x001eJâ8ù3Ú,Þpd­öÌJÿ"áù #ÕÐKËvaÝ£Îâ
§ÂjE\x0001÷hd}v»\x0002M\x001dÝ7\x000b«=\x0018\x0018¥\ËÆâÇèëÄZ^oµÇ\x001bNÕ\x001e%ã£#<\x0016\x001aôr4
é®½\x0007ÃÑ\x0000íÑpÅYkh\x0002uMÍ §xÃÑ\x0000íÑp^$c¹ø\x0019\x0011Ý.»\x0002ÃÉ\x0000íÉp\x0011Dw}\x0015G<çßËiY-AÇ\x001bN\x0006hOK(\x0002û	R\x001b\x0005\x001fùu4\x001aXm.Ç\x001bN\x0006hO·"iO\x001d\x000c,X\x0014lL·\x001e~¾Èâz/?ô©÷¯\x0017w\x001f?ýããÓ3\x0012\x001fÙ/zpX\x0002'jý¨Û.Ê
fî®\x001cw\x0017w7÷7w¿¼¹=/òÁpØÃ¡\x0012¤bsÒëFÓá|Z¹ç(à|\x000fçpÁ48êö\x001c-7~ÖJ¾T\x0001{¸¬\x0003?\x0008ÁJ=4UmËÊ­ö\x001eOÁåã=×|þøõóÅûÇ»ÏL-J®JQQ?åa\x0018Éµv#H+U\÷oÞÝ_¼º¹¸{s~nH:ª\x0008!4P¡ER®¶Ü,¶¾lSù=£Å\x001c¸\x0002
{4Ô¡ÏÈ­\x001e4Î\x0017MÔØ¨j\x0017ëÉÌG©½Ï&Ë¤%Z,)fL»¾§ïÑ¼n«å$Ãi2	\x0012ò¤º(ý1åpì!\x000b=YP%puø\x0012uÕ¡4{Ð¹Öì¹,ödQ÷9¡Ú\x000bþµX0ù&°R,¨@K=ZÒ -E\x0000õîE³hë#»$ã|\x001a\x0006Eë¹rÏ'À×ü%K8aMõì¼dyåc\x001e­\x0013¿'ckTkF½\x00132HÒ o´²~¢BAeO{ØFG ó\x0004ÅòAü\x0004ù\x0010\x0018¡²+i\x0008\x0005Û`n­ÎÞ&Ì<ÿÁ,µ<,:ñeYNc\x000f\x0005Û`p­ÊâR"_EO"\x001bM\x0011\x001c×\x0011áJ^ZÁ6X\x000f«2\x001fK\x0019\x0011w:3ÉéLrZm^ô.óacjUç4Z\x001bKìSÏBùKËUuÎÉPU·R5Ï\x0006ÃY\x0000ÕY4ú¸\x0016L\x0012cõ[_¿¾?\x0005Ûp\x0016@u\x0016\x0012\x0004¿¼¼/ê¹¦ÆáÔÝ)ÅCå^zIP°
\x001e\x001eT.>ÑCÔxXWç\x0014¶í-dÏ'5aÐ(\Ü|Ýóô\x0007e(àbäâA±cÛÈþ(Ü-&aÌðß}üüùé¯\x001f>¾®\x00126TÍ	ë²\x0015UL\x000cRV·Tp¯ÝMïÞÜßßþðúÍ«ó·SæÃ\x000fÕ|4Ö¬~^o\x000fcx¢\x0014ZDw¦*e\x001eÐõN
è\x001d×t\x0016À ©ôrïJ
p=o3\x000fè{@¯\x0006´iIÅ-Ï$Ff¡\x0002ªß	\x0018zÀ \x0006¤\x0008kÆ\x0011E\x001e½èÓ(×©\x0007L[Î\x0008\x000fÃ¡\x0015LR..yÍxîYs\x001a°ð
àQÅÏÔ)òNi	N\x000cc;$)¯\x0017+¾\x000c\x0008Çb¨p,zÿðôáËÅÏþq¾S.9ò,h\x0013.õR¶Kåõ\x001eû«Û×o/~¾»ýå|¯
Ø£	Óå#À/\x0017?=|úòûãY\x001b]®[¢°HO<Ø\x0019¬ÄÈfµuëþíÍÅOWwo<«T pÐÃ\x0012®|HéLõ«\x0018]\x0002/â1iÍ¨ð\ç´xåúZß¯K \x0005Ü¬\x000cdòå/Wzçñ|çÕ«\x00179ëoÊ½\x0005FÊêEþ¶É­%85x¡Ç\x000bJ<¤w\x001cl
[{\x0001I°Þ7\x0017{¼¨]½ 9\x0006#7Ê$0^.A~]Äx.\x001e\x001fÛxT6~ÿðéo\x001fÎwñÐ\x0013úemXÈÎq«G9\x000c|ë\x000eàW5\x001fîY¹ûéæõù\x0006\x001ea
l±Ö¿,pn¥è9¿SàÎTuÌÂa\x000fú«IS.\x0018ÜsYV.ð[\x0013äU\x0001¾y8×Ã9%\x001cÕ!×-\x0013+,§(sí\x000bÛªñ<ïÙ¼ö«¶\x0010éðUiê\x0014¥\x001e\x0006-¬¿ Î²-èØ2Í\x0004Ñ£¢ÎbëßA<Ó±0\x000b\x0017{¸¨+·[\x000bËndÃ\x0010j\x0016.õpI	¹Í õ\x001fKRrR\x0016çÊ"gár\x000fp	XvÏJ\x000f\x0014åSÔ\x0011aÚõU\x000fçb\x0012
Jkè¾\x000c#­wÛÔªó\x0011Wë<Ýè\x001eþ!g/\x0017\x000b\x001a\x0015i¹çÉ¶~\x001fÜà\x001f¬ÒAäXwÚ²é)II>«_U\x001bL°ÕÙàHá:\x000f%¢áZE2D±%áL×ÅtpÔ-V~\x0018¬ï\x001f?}:\x001b,ÅÕ\x0000CYªúI=uùó»f\x000ekZï.îoîîÎÇ"pT+IP ²2\x00052]`£tÎÔ@$\x0019³ò3\x000b=\x0014j d\x0004;¤\Û \x0016(Öe)+µvçr=Ó|>à¢H\x001aò¹èÆ,£ÝdÜZÉæ$ï¡ü<Td\x00018¢¼\}n|¾íH¡G

$úb(Ä¶ËÛx¨Id%e3Éz¦¤ÙP¶\x0003+Ña¬á\x00055\x0018a
kÂÃsL\x0013±áéE(ãx®\x001b\x001aÃ"a´ËÁ3U\\x0013h¤\x001aìU\x0018\x0004*à²¼T¦ÖÔ,­E¡üJºü\x0005¨?Ûä\x0007Ëù]ù,ç\x000f{|øºõ_þúá|\x0011Rð^ªiL*î0Ö0zÉTíÕ¼úéæêÝbÔ¹ýáõÙ*¤\x0006\x0006=\x0018¨À\gÀDåH5Ä)áª\G ÏPªÁ°\x0007C\x001då\x000bfJFÞèK\x001c-\x000bfò\x001e.×s9\x0015\x00174\x001d\x0001²í¡\x00066h\.\x0007&5ïÁ¼\x000e¬Í\x0002¡þ:~ë@kÛÁ\x000e®Ðs\x0005\x0015W±]¬m@l,÷Y|pAß\x0008¬\x0006=XÔ\x0019I\x0013Ð%ÎNµiæ@ÚÎÛÁr\x000fU`Å¢å½o¥¤\x0001Zð\x000cvËÑ\x0014£øÏ/ÙÚÛ¿ýýáóçÇìêýÓç§ÇOç£ÓCúÒxõ\R»\x0018G6!öÙÛ~¾º¿¿YØ®^ÝÞßÞÜ½H\x0007=\x001dhéè\x0015ÒUº\x0012\x0019;Z\x001aùûð°ÇC-\x001e\x0002'\x001cÁ»:3Ü8×òáû)[è\Oç6ÐÕÇ*Xf\x001c&	¥Îö·Ý-t¾§ój:wÉû&\x001dI\x0008²ñpçÒ\x001e.l«\x001fÖ(Ñ\x0019£
²[Ðb\x0016Õ\x0007ÖrM\x0008Ð#.H;¬ÜÚJü\x001f÷á¥\x001e/mÀ«m\x0015P.¹5ÅBx,A\x0012\x0003ý\x00076áã,·©Yî\x0001ïëÿøçß3Æf~Dî«tâ%BdA\x0000\x000eðÝw7?ß>cÍq®ÛÔ\·\x001a*,w~R\x0007/\x0013\x001e\x001a±s:gg	±'<¶z\x0013¹%ùh\x0006:×%$	ù`Ý¹Ó;KèzÂcË7A\x0018|áàföpi²TÃÉ`ûç\x000eñ,¡ï	­ßÌW\x000e"\x0002%\x0004M\Ê\x0012¸44\x0004cÏ¹¶YÂÐ\x0013\x001eÀ	Âr<\x00027ÓRgt}°*çcµ\x0003y\x0013aì	-á\x0004aô,PfÑÊHµD2GòÓ9[8K{Â¼i\x001fÊ\x000cßrOä\x0002`²L\x00186oCw¬\x0015åðØ\x001c^?|zÿ\x001c^ù\x001fX
Ï2õ­i
qhÏ,àõÕÝ«\x0019<èñ@\x0017Ìrt\x0017<Ûðä\x0014\x0013Þ32=\x001eªWÏp9p¹òØúºV\x0016\x0015"\x000e²V[è\Oç´tåøV#
Öyn%È\x0019Y@º[Ïì½Y<ßãù
ß6ðÖÃ(:o\x0019Ù\x000f\x0017<»\x0013/ôxAW~H?¿­Í\x001c\x0003B:çgébO\x00177Ð¹ûµ&IC|¹PÊ·-AÂ>¼Ôã%5C\x0004\x001aé¼õ,«ýRÃTÚ×©:¹äÔñø^ Ùe¬¬2ÊÞó°ÏìÙÁìYµÝ#e§\x001aãEÔ\x000cä¹\x00010	Q_ÄóéÈiø4:EôõáÃ¯Ï$dÁ×qvù«Ú
¢èÀeX_»EïõêõõùI4Ì\x0006=\x001bhÙ\x0012û3\x001b
v^)¦&\x0012ïÃ\x001e\x000epT\x001eÌ+W©ý¬õsÕ#1Mæz2§$+\x0008{áÑ×Á¹å8464ûØ|ÏælA\x000c±ôðlå0Hµ£[u\x0013Ól¡g\x000bZ6ä\x0000ÀRã\x0017¹MÑèÉ$ø·\x0007.õpI\x000by\x001a¥8Y\x001c¬e
9¬_t_\x000bîÈ\x0004w\x0012y>}úõ\x0019\x0003W¶x×b.\x001aí8Ï"U$Îp.°»½»~Æ¾1\x001aôhÇÖ÷y´h"K\x0003©\x0011zö
[\x000c¢3pÎøN¡av\x001cq¾°j4\x0013\x0004xÕ²|Ñ¬¨QV-îBs=Úq¸ùÒ\x0007­`ÆeûÅ´±;-1Ý..ßs\x001dÇ/pQ7aõô4\x0003É×H$Y\x0018=å39´Ð£\x001dÇ/}MË"\x000bZ\x0013© JiFËæÜõa
-öhÇ\x0001æ\x000bht&eÕ²ôÄ{\x0015´}\x001b-õhÇÁå\x000bh!òËù2Ê¿'pÖ¤Îsï\x0015sd¹'ËÊ­\x0016/ÙnÀ3rb\x0015¨\x0012\x0011KLu\x0001/\x0019Ûã÷\x0005²rw\x000e¼hé\x0010²9.Û\x000eÎ½\x0004Ì±@é	Bªs
M_sjdçîS`\x001b8Â_ò\x0003¢ï\x0008hmÛimóë1Ñ,Úà\x0006¬Ö\x000f894àÐåÈÂæúzh=Ûà\x0007¬Î\x0011Dk¸û\x0003\x0010m­ßZâ\ù¢!îZ·Á\x0017X¥3He¯%þ¤ íeÉËk¢óv\x0017Ûà\x000c¬Î\x001btWfté\x0012$Êe?5NÓ£
ÎÀê¼A4FÞ\x0011éºv©jôÜØ\x001cÛ`s­ÎèÒv«2YÞðÓ:m7ù¤Éíù¤06Ð¶\x0008®
f\x0010[\x0012¥¢lä\x001aï²ÝèEUË\x000f}{ýþáéÓÅýÇ÷OïÏÂ¿oÕÆå,THí«RÍÚG½~uu{wqÿæÕÍí«ð\ç´xåÖÇ­ª¦ÜHyí\x0016áÒ\x0007+UCç{:¯¥³å"xñâeæñ\x001em2\x000f®¾iðB\x0017´xÅò¼\x0005SB\x0011n7RIîýÎÕ=^Ôâ!H«)¯«Í\x00159´Zr\x000c+\x0019$
^êñ\x0016/<¿\x001a\x001aßÇSo¬è¾c\x0008+ÇV{¼¬Åó¡õ0¿t|p³­£ûö^\x001fÎù!4,V^¼Lâ\x001d·?NXS\x0003\x001eª7_{2,W\x001eärhGw\x0006Ôñã´H\x0018Ò"_+áãsp¡xÅðì\x001bÇ-Q$Íú«Ã»Êwóö%4èÑ@æËºñT`X\x001f¸ÜUÛ\x000c-³\x001a:MaOºEQ\x0006÷PdÉcÒ¢Éí¦ñì!s=Ó­
2\x0011Òü\x000e9´\x0011Uf\x0017ZèÑr§\x0005Q½¡ïÉ\x0012h\x0010ÛçÄ]\x001b-õdIù9Ã¢«Àd ³éñ¬¿ª¾V\áx<Ë\x000fÇYË\x001f\x001e?|yzxî=¿\R«*{ÊTÃ_³Ñ4\x001b¥Æ 3Ë\x001fn^¿½½zæmF\x0000¡\x0007\x00045`GLU\x001cKÎ¶ÕA$ ¥3wÃi@ì\x0001Q\x000fèêÀº\x0001\x0018Ðba8÷¦?
èz@§\x0005´4k±\x000eQMü\x000eGVD¾ÆÞM¾\x0007ôê\x00154ü°O+èero\x0012ià²ççÓ±\x0007ê\x0015¤dpn<J59~\x0016!À­{\x0010üqÏ?©zùéñÓóE\x001f¬?ZÁTL|bwîùü§»(ûßüIÝË\x0004`AÅÌ\x0018\x0019Fdx|¹P¹rO\x0003b\x000fZÀHf¦êTÆòµ¹AÚµIå\x0000ñÌ'\x0006t= S\x0003B­\x0017"@
X\x0004Í`Ù¢gRÓ|¾çój>W§ø\x0012_ñx¦~á²óä\x0010sµãÓ±\x0007j@oX#µX\x001cùÀ\x001e9!U\x00160lýÀöx¦«ÇòÏ\x001e?~F7øÜ\x0015-\x0011=K¸ÊX\x0003tkw´\x0012$ü|wsÿ$ïñHW\x001b#åÙBä\x0008¦Þok¨\x001cCj·ïõ\x0000f
{6Ô²ÕçeÝêø0b×tt«oÂól®gsJ64r53\x00189u\î\x0018-k±oÙ|æµh®5C\x0014U\x0003D[MÏÎÃ\x001e.(áLIAËP\nù32\x0004½]¿fÌÂÅ\x001e.jáòrñYV.\rÛvPa-VgK=[Ò±\x0015Á\x0012Ë«spË%È¶ºZ$>\x000f{¸¬KÍÂÑKn³+YV\x000ewN&Ì¯QÒ9à'¨ÅÔt\x0000HwØ·nvô\x000cJ×àøgY8)\x001aNé £±ª¥\x001b|U:\x0007\x0007Ò8L)\x0013¾@¦âMeåp\x001fÜà\x001c¬Ò;88,\x001d[V¨Qh«Ûy¸Á;X¥{pæpZ
HÐnCnO\x0002n
¶°J\x000fá,HgN¹J§\x0016ºVå6Ð
\x001eÂ*]\x0004ÆÜDªRk6±((´«uþót°J\x001fQfë¥)\x0015¼vNSq½\x0015f.\x001dÝ\x0016iÄùXîúþáâîáËãû÷g\x000bé¡q\x0019<\x001b&\x001f×VE\x00082ë&\x000e\x0003;»BºWW\x0017wWoo^½:[J'Ð\x0003\x001a0¸Ká«!Ô2RDSÃjQ=\x001enÁc\x0001\x001cOÉ=á~6*wÞ	èz@§\x0006Lå\x0006!^&¢õM\x0014VÓ\x0001
@ß\x0003z5`l]D>Õú\\x001aÉ|¶âå£RÎòÃÑ\x0001¹ûøùá¼¦!=SÈP\x0012¾s¯¢GQD\x0017×ËsïÞÜ_½\x0005=\x0016¨°l}ÃK4êIìx½Äuë·ë9,ì±PU"õÈT¦¥DÞ¸P­·îÎQ¹Êi¨¬_$³\x0008ÚdH\x0005oz\x000c{¾¡ï±¼\x0002ªu<BqU£IÒÖ7õ\x0014Î\x001cVè±\x0006D\x001eyk\x0005¼¬¾ÊÅÀyâi×Ù³TâèíÐ.ÊÀ?¿øõñâêë_¿~þòxñö÷_\x001f>ýv\x000e-:ô¢JcÂ
OÜ\x000b¦ÉÞw±åÏ¯®®o.®Þýð\x0004FßþøæÝÕÝ÷/ñAÏ\x0007j¾r\x0014kÍIá\x0003©
sA\x001cÍ;\x0001±\x0007Dý\x0002Jo¸)öG\x0002\x0006þ¶\x0001L/½Ïõ|NÍWÜ»qíí$\x0017\x0003b\x0005ÐÚ­Çbr¦ÉUÀï\x0016eÛ÷\x001f?E#\x0019\x001dn!¡´Ì#÷ÒA\x001f0\x001f}·Ú¾zóú%&è@ÁDÕjÈL(õò>D½ÑÄÍPØC¡f¡"&¤	\x001a,ÐN\x0003w)i&×39ÍB9.Ú\>^D^¨pøz'\x001b\x001aÊ÷P^³P5$³`¹\x001c²Ä>r#HÛ?\èyfôYëÚPÉx¨99|ÓP±
(e2²%!«Ê\x0014åjR~Þ~ìRÏ\x0014L\x000eyÚµdP\x0017&\x0019óî\x000c8¡i¢Ü\x0013eÍ*9¬*DVZ¡©ÇX)nþt]e>ëíÍ¯oTTòËs\x0005­äFíõ7T£\x001d×\x0018rkä¶f1UÕ ²VMÂí\x0006Ê\x000eÜjL9½FÕ\x001bõýÔO\x0019ì>¨¡)©\x0006Sn5¶ÜXÑA¡\x0016{®&¡yY«Ókj0æVcÍ½o_0Ä¶VÀ¯Ûe­âöµ\x001a¬¹Õsã¥à¸\¬¹ê³ì++-»}{`\x0007n5FF~ñ\x00195\x000b@kÕîÖn\x0010úVR
FÝj¬º	R_l©r\ÖJ\x001cÆy³T0X\x0006PYÄ
ke­Zøîe gY+ÜN5APÅSMFÞÆÀZD%ThPÛM;\x000c\x001d4\x001d¥¿ÕÚ$El]¬àp»aÁ\x000bÆ
û\x0017§÷m20¾yf\x000c\x001bÜ¨¤J?\x001c®
×ï\x001f?yú@3½Î\x000fÆ.¦\x0019O«Å\x0010ÄÄÞ{×7¯nîßÞ¾¦©^ç'c\x0008\x001eôx ÅË´ßRMÏb½®É²»Ó°O\x0007=\x001cjábjåÖÙËHJO"f\­îw®ëñ\x0012o&\x0018/¶\x000f®½bÆ\x0013«¯Ãó=Wï<É\x0017OÍ¯L£leñÒI\x0004¦£\x000b=]P/^9ñt.XþÄgä\\x0013«Ã=^T\x0016ý\x0018J1³­Q¢oûÞz¼¤^½,Y}S>s1ö¾­Þ^¼Üãeõêe.\x000e/«\x0017E
«ZÉ¾Ñkäøîb2»|àZNÊ¬.~µµÁø´oùìè3´NDu\x0013?\x0007ç ý¹>´äNðû\x000e\x001dì²Õ\x001af/=DåãrXIoqß
n0{Vk÷È²°<"\x0019>+y\x0003l\x0017v~ÜálXíáX$a9,7ÕÔP36Ã¼ÏÛ£ÀÛ."øýá/ùúx¾}\x0008Ê©
2i$H\x0006\x0016r{æÇ\x0015öãÕþôîæ|ã\x0010#¹\x001eÉM#¡ÁCC\x000ez4*C8ÉÝÍ\x0012((\x0002÷2[ã¢ÄshD8rz®CJ=RR ÅúÆUk2ë.ÒÂ\x0013g\x0000§ûi¨3³¨3³/"Ð\x0008¥r\x000b5mà4°d\x001av·ßÞHåúl\x0017(¡ÁÓ9mH|%u0Ë4lo«Øß`\x000eN*¦rÙÕ®í¦­\x001bÜ\x000e\x001bÜ*v8x)	¡3'Û©;tvó~\x001av¸Ulq*¯äPÛ;\x0011ÝCÑ	Ë¬mL0ìqPìqtmj\x0014µçW?S.v²­ë\x0004£\x0005Wìqª-u\x0002~äCç\x0005Ó\x000bÓ$Ò°ÅA±ÅÛ»cAòâUÊ÷jËtúþ2Ë4lqPlq¥+gj!»\x0015Ìm;å­æ	-\x000e-^EÖ«¸çæ¶Â­Ømõ¾8lqÔqlq2MõäýdC+[?ÍÍ2
[\x001c\x0015[Üä¶Å£J\x0016&{H¨l^§a£&LqËÃ\x000bO-ÌIÖ·ôæ)\x001dÍ(?\x001c¹ï?~øëÇ§óú\x001c¾\\x001bäC\x000fÒ7§ïß¼þáÍíyat4µpÜ,N0vaà\x000b\x0017Ç¼!6ÅÎ$#^\x0000²æhBHùá«µg?<<3|)x[\x000b\x000fudmV®1!^¡kÝÙ\x000fWçGB	\x0015ôTðÿ=Õq)qÝZ}¥¾ÇÇO\x000fïËwüüù¹RZÆ6à7\x0015¡qNDB_z[8a{G}7wW¯Ê÷¼¿\x0010zBÐ\x0013æÖËBÝÌ|µòór§)/- ö¸\x0001°ÊZ,KíòçEôÞö"º\x001eÑm@MÖ½§Ù\x000b";l\x0017ã1Ó"ú\x001eÑo@Ìò
\x0008%lNT\x000fbNüÊC¼\x00161öQèëä\x0014\x001882)·|¹ÑàÀ½©GLzDcDD\x001a×Û\x000b¯DA.zR-bî\x0011³\x001e\x0011Ú\x000fxÛ^OR1
æô	SØõ
\x0019×Ýq\x0015Ëèºùå¼à\x0012,±=IÇ¼×êØÑpë-7UU³²%2¨Ax0¦­ãÞób\x0007Ëm·nÏsH-P\x001d\x000b?öx\x0011vri·Ù±e´zÓHµ6ÂØúÖèPiL°×zw½0Æu×vÅñÒ½\x0006å/\x0013ï,.¾¯k\x0019\x0007Ãc7X\x001eLm;B{9\x000b&¶o}ú(ªdáXÃc^^÷®ÂèÚ:îv`vôgæN\x001a93aqË£·¼³¸¼ÛÉÀpf`Ã!\x0012FÌ¬\x0005P\x0010¥;ËåÝG\x0006#\x0003\x001b\x0012sS\ËÏUTq,nwÜþíÏËý¨ó×ôÚ×`om$\x0001%,Ä×¬\\x000ffIíq¿í*\x001f¾þûÅþü&¤§\\x0018AÄå|:i·âe®ÞýËÅ7wß=#ÛbÛ lWÿ;\x0015åÖbé\x0002re\x0007ºÓÚy¬Ðc\x0005
ÃK©¢qr,ÚMÅ­t\x000bÌ2¥)©¼\x0000ÑR\x0005¡v;çÂ]Æê\x0002-Û\x0017Îpy¸ä\x0017³løV\x0017ä£[¹ÖÍS
ÛÝªö»Çe:Í\x0015.¥\x0014Qb\x0001'GqjØíVµÝ]{;.@¢ú`Sã+\x001e/rñ\x0013Õ!\x0010¥\x0004þ×øéá?¾úãÿ<Ýp\x0001X\x0011Û1Ù`þðzN\x0013Ô5½ñÓÕÿºyu{óLãøñÓöó\x0011äXZ`Á½ìe6R\x0001<}üP\x0002b\x000f\x001bÐÈ÷-´~,\x0005LÜ>pê¬t®'t\x001b\x0010/\x0013\x001b\+\x0013WÊdh:ÙJ>ßóy=ÏÜ9\x0003¢}{ÞÊþ4®Óñ/lX¿p8$éÝh	ðdýN°\x00120öqÃ\x0016´REß:µ|û¾Ã\x0008ÏM|©çK\x001b\x00160ñh½¥Á\x00069JjEâ¸\x001b0÷y\x0019ä#L\x0002Or%«áÌJâE\x0005ØùÚáá~0äCYB'À\x001e|ÌJó\x0012qt%[|I7\x0005KÙhö%ÖµU<}ÏW"\x000e¾Änp&	û\x000e&îVðØêÌ2îE\x001c¼ÝâNZû=*L¼\x0017­mm\x001e§¨\x0012qp'v?!U\x000féË-3­¾Dg·!9ËV~8\x0004
÷\x000fO\x001f¾ü??=|úõñýû§gjÏËgf{\x0003Ññ»H\x0008òJêáô{uûúmá»»¾yõêöl	ºðaÏj¾P)ºl9Ruò<é­9ùÆJ@×\x0003:ý\x0002\x0002O\x0013(\x000b\x0018ä2Ô2¨rà>>ßóyý\x0002Ê]
h¸õ\x0003á³§%\x000cJ¾Ðó\x00055_Ì2«
¨ÉoHAn\x001eN+÷±\x0007[\x0016C\x001a"±C«!ÉÅ¹\x0007Ìz@¦\x0016^
ÖB«÷.[pç\x00119¸d\x0002<¸äù3¸?¾|ãÌÒ½9D'\x0018Nr}JÂÁÊX½!Ý4ÎFÛÖÐJQº\x0007{r3Q\x0012\x000eÇØêÏ1æöT\x0013c;'VÊÈJx
%cO\x0002ixÀ~ûûãÃç¼\x001c=zH\x000fa\x0006&\x0017EÞ\x0001¬åßþxsõö\x0019\x0007\x0007Çö\x0019Òð&ü"\x0016\x0004õIêÈ±lT%9ÈkoT¡§
**l\x000eÊÉeEr±\x001eÖPÏc¥\x001e+i°l|<uòÌXÒìå`ånù"Vù¯:Î½\x001c\x0004T¾|YÈ~úøáËÅOÏÔ(ù\x001ce
R7\x0015ô\x0014¸pò%ß¾]ð~zS\x000eÀ»ó¥J\x0002\x0008= h\x0001©ò%sn\x001bhüááêøÞ«\x0005Ä\x001e\x0010õ+èdx
Ð½<²\x0005n×¶ûÏõ|N¿2/ÊÒ\x0008MyÆÈ©U¿Ø½¾\x0007ôú\x0005l\x0019@J^Àd[ÁA<>\x001eZÀØ\x0003Fõ
\x001a8\x000f\x001d\x0002½ÚóÊI\x001c5\x000bXî»ã!¦\x000b0\x001dâO\x001fÿöøáá·z\x001fúïÿü¯«O¿þþø?þùëïüóÙ\x001bG`±bÿXÈ ´$V	û`àîÍO7¯¯¾¯×¢âÊ~¼ùåæ¹F\x0012{ÜHbk.u\x0013l¹\x0008±Ú«É±Úm:ØÍXÃP»½\x0015{VÜÌjåEÕdÒbà3$»
c\x000fÌVX×ÃºÍ°å®\x0014\x0018¶\x0004\^(?GYØð-vAèaÃfØ,#M¦äR½ÅÇÜ\x0004¨|¯¸\x00196ö°q;läÉ\x0019¤\x0001/f¹1Ã ©y\x0001<\x0018²«¬=1\x0007\x000f\x0017ß?ýõëùx£üÇdMË\x0015t\x00110XæQ±¨-©îá9Ì«ïox÷\x0012bWbOpòù_B,K=èßW:ÌmÊ¬\x000bèÎ\x001e§9@\x001c×\x0010Õk\x0008åûÖ\x00163C]oP?5HÝ½w8¼.j\x0010\x0001l~ùáÈæòã×OËØ?~úòÌ»^¹H.qÝ]1£iW\x0017³¾#KxùæÝÝ2½àç7wo\x0019?GFha#­*r_hnZ,'R!]?íj\ìqqëâË\x0017÷òñÒ,\x000fíÍÊÅ3>Jë{\¿\x0015×\x001e¶´º\x0015×fy¥tÅV}\x001bÜÜãæ¸X\x0016
Çzgæ0ÔoÌîmí2,È\x001e[h1Épd4â¢:*g£\x0014\x0017ç¡r\x0007¯\x001bxÝV^\x0000¹\x000b#=øs¿Ðú°î\x0002Ô´a 
[iM4\x0016KTÇK¥>íoÂ\x0006Þ´õ¨QS4_úJPÀ%ØÞGü¨´°\x0017Ý\x000b[w/åÏ]âÝb\x001a ®\x000fæ\x001bñ\x000e»\x0017¶î^(×\x0017+)9'oµ\x0010°¥5ÏZ^\x001cÖ\x00177¯/¦V\x0002\x001c¬¨\x001f\x0000Â!QüxõÅ­ëkS\x0014ÏF%]</×\x0006'®b\x0018I·w8o¸õ¼Y\x0017ÚÃ³±Ká\x001eñ\x001eÙ[¿ÓhyÝ\x0010ç¸­\x000eU	åÔ	?NÐU4­jÞa?¸Íû²lÜ\x0005OÏÈ¼rgDï¾Í~p¿p[ý\x0005é4:N\x001e,9#M»çÍ8sq¢ô»_¿,Wë÷üó?èúù ÁpÛ^ôüéZ"m\x0003åÝwo\x000bÄõÕ«½¹{
z6P²9HÒçã!	pIÄÑâ \x0018¯s=Ó.iò¼¤PÍÏZ\x0008õ
©öÐÃù\x001eÎkál{s£ñ1\Kíá7ÄþpëáB\x000f\x0017p\x0010Û"zw@öDI,{\x0018&Qêáb\x000f\x0017µpÅ­#\x0007¥\x00146µëªÀõQ-õlIË\x0006µE{Ùr^Zó éb\x0006x»\x0003.÷pY\x000bWnH,ùèôØ\x0002i$T6oö\x001c^7Ë,W$\x001d\x000b\9I]Fuîd\x0006/c°{¾ª\x001d-°Ö\x0004Ó¤\x001cr\x0013+\x0000+©Ûr+{è\x0006\x001blµF\x001e<Ø?!\x0002£\x0000¹\x0019á¾½MO\x0003\x001djéLS¸wÉ,29Dgd°}Áßcèìà"¬ÖGP7	²\x0003C'*9-Xb}ûnð\x0011Vë$ÀHÇR\x000f#\x000bpi#l°\x0017»ÓÓ
NÂj½\x0004	ñóÀÎ²Ã¤Ûdi\x0007(¶n\x0017Ýà%¬ÖM\x0014\x001a]±Ê£g/âüåOì¢\x001bL±ÕÚbdâ'sj¼âJqÓêtI=u\x0007\x001d\x000cÆ\x0018Æ8$ï¤ÌÞ\x0019Ï¥\x0019©I@Ò0=p1\x0006¥1\x000eeÉ@\x0001çQ\x0016_!\x0006ÅôÒÅzº1 V\x001aã0\x0004\x001f#[$)¢<ï`v}ØÁ\x0018Ò\x0018ïfÙËºÂYßtRWüò÷¸1\x0018L1(Mq1\x0017F
ù0yëR4r\x001d\x000b\x001e÷\x00040bPâP \x0017¦åHDäJ	¥ÆäSöÐ
¦\x0018¦F­-Ý´v!Ê,Û â\cc\x001en°Ä ´Äå@¢\x0008ÞÂ\x0012\x001f	\x001f¤àß§´ëH\x000c\x0011;(Cv¤Õ\x000e½a\x001fBËº!ë¦§\x001bü\x0004(ýDÙVAî°@*\x0006u\x0010°·bì|{â\x0013\x001cü\x0004jýDäGå=#òàÓÐÚ$\x0002Ø=\x001f\x0016\x0007?Z?\x0011 p'\x000cD\)/sÐd\x0018÷yÿÇÁM ÖMË\x0003!§}vRØ\x001fì®È\x000e\x00077Z7áiÂsj"8<Õ\x0019y\x0004ô¸ëÄâà(Pë(Ê'¼ßy¬&¸¦rë3î±v88
Ô:
_ì	ñ¡§_ÏcÅ£\x001c
\x000f»,\x000e\x0002µ"Û\x0018Ï\x0015§RoSíC)òÑí¹áà)Pë)¨ß\x001biíê=;¡·­\x0012Áï	ípð\x0014¨õ\x0014Þ\x0005\x0012x2\\x0010E\x000cïv]wpp\x0014¨u\x0014\x001a\x0012¸6¾»\x0015@Àt£p£pZG±tÙsõc±-µ-±\x001cöa#ìù°nð\x0014Në)\4ÑµD±¯tñÑîJwºÁU8­« Û«Ô\x0006;m=±è Ù0dN\x000f7x
§õ\x0014ÔPÌ
t$á<û<ÅÃ\x0003ÀCáÆ\x0007\x0000­§ \x000e_\x0015ÉSÈ¶sÝñy×UÑ
Â©=E	¸f9e#\x0017\x001eÌ©~YÊ¯ìñ²nð\x0014Në)h|\x000bw\x001ebmíH¶°+Bq§pZOA2}ü\x0008²4\x0011'©¬Å}ìqcnp\x0014Ní(² =°ÊÜâdEi3EÜõa\x0007OáÔÂe¹g§rW­\x001dEDkv=(úÁSx­§\x0008`D\x0017¸²µ+VOlÊ¸'zò£ðZGa£ekWþ9°<AÌÈ!@\x0004Üµíüà(¼úN\x0011´º\x0016wÏïÙÉ;IÛÑUc\x000fÝà)¼ÖSPçY½gÁ*MOkgåÈÏ»Önð\x0014^|ö\x001cI3	9ãÉ!@´y£ðãS±ÖQX+µØ`ÊUÖ/"¦ÀA;\x0015í	\x0001üà(¼:÷Ä\x0015Ë´ñÛ	É1\x0019jÂôhðZ/a}\x001d"W\x0016\x000eBàö­,v×\x0018Ü×gÚÀÉLï'ué¸9Ú]\x001f|×ú\x0008SÜkMÙ¡\x00081Éô6Z¸=\x001e,\x000c>"èÓN¶\x001dV'e©Äºxéü\x001eK\x0012\x0006\x001f\x0011>¢X1Ë­rQ2vô±+\x001f\x001aÑôp\x0008Z\x0017\x0011iÀbõ®¹\x0018áZ\x0012\x0002ºÀ+çÂ\x001eß\x001f\x0006\x0017\x0011´.¢\x001cwîC(Kç¸õ6&ÚÚÁ3\x0011\x0006\x0017\x0011´."BÛ©.Úr¶Sè,æ]k7ø õ\x0011&	]Y;»¥µC\x000e×'Ûµtc9ÖEÐ8Ãz
+wXn&K(ÚéT·Ë\x000cN"hÄ2iÌ¶\x0003[\x0005­k\x0018=t\x0008Z'AïþÜMf=òrÑqâ`1îÚu\x0008Z?A}W5aWÖ.ðtbvb÷¸ÿ8ø¨õ\x0013KN\x001d¬1Æ.WXÙw°+ä£êË\x00044,\x001cbÊ|K>Å=û.\x000e"j=\x0005M`áÚT¶`­ì,Q2µÛå)âà)¢ú2á¯ÿà¨ê8I`Wá	»np\x0014Që(¨dsb©MÐLäÒ¾I^'\x000e"ª/\x0013NèÀ9ßî°ÀB¬1 ì¢\x001b<EÔz
Ûºc
xêXê\x0003¿<Årx÷Oq¬<Uß'ÅõÀëý°1[NÅÆaì­mp\x0014Që(l\x001b3\x000eÔ8\x001c<EÃßµ¸=+\x0006S´¦ØRvâ\x000bL£9Ãb9I±KZcgËÕÕ1]6¼é,\x0017FwU¤Á$­9¡!K5f\x0007z;±\x001cÈäµèÒ®ì4\x001cØ¤=°Fô&Þ\x0013se³Ü%N3iv­ÜX­=\x0012æ\x0015Ôë?\x001a/÷(S´iÖì¬N\x001eDV\x001e	³ !\x0017ìPW\x0015´]Õy8\x000fYy\x001e|.²Î\x0004êû´¼p-oâ÷Yá<\x001c¬<\x0010uê # ¾Éêû¸ÉìÉ\x0010çá8dåqðT`ÇV\x0018r\x0010+\x001c<Ë¼\x0014¸°Ç»æá@då(ßÕp{\x0002+?ëÕï*>Â{³ã@X3\x001c\x0008ú[í9ñ¢à\x001dÛ»÷a\x0017ÜXdo´>Â¨o:¤4îÙï÷aOØdÇN'ú[%\x001dsò%EIÆkÛ.ìyq²c7\x0011ý­®l¶è\x001b\x001d0]vþÛ,^\x001añÔ~";ñ¢n\x0015)bv\x0014{Ô\x0019£m	ÔW\x00199-\x0016ÜÐ&<j%âÕÛs.O´Ý'd¦¿mòr0²-\x0005°'mú;´
\x001eÁçh\x0016\x000b\x0007N²;4z|\x000fÞx2´=\x0014ai®[Ïy'\x00169·\x001bpÛâù:®ã¡(\x0011ä øýáý?\x001e¿ã¢JqéÚ%tbý§¢MÍzýÇ«W¿Ü¼}	\x000bz,P`EËµ8ÉYÔfØä¥\x001c6åõ«õ\x001c\x0016öX¨Y­\x0012s\x0001Q¤±Ûµ(Y©H$ýíX®Çrªè¥\x0005\x0012ÿ\x000eø#J\x001bgÆõ^9,ßcy
\x0016Jan¹ØË\x0014±ò+·
ålVï\x000csT¡§
ª­e¥9¶ÌCÙZò	ãzÈ;G\x0015{ª¨Y+Êªò'tÅs\x0006ÞY"\x001e©\x000el3Vî±²rgq¡fY\x0017ÑðO(³FÉ²mÆêü¥Ç£NÒ>bÒÎGeA<ÌF]WsZ¼Òªµã\x001a­©ÆFî\x001e-1\x0005\x0014¥À×ò¯»\x0003i°¤VeJ3z\x0007U¹j³ràjX.*;>á`³¬Æh¥CW!%í¹5g®(,Ðo·¥v0ZVcµ¢is.S3\x000e¦A¹\x001d5Ø,«1ZÉ\x0017£ÅkÅ­ðJå\x001b¦õ¬Ú\x001cÖ`´¬ÆjÑ7Lí½Ï[ù
kÇO\x0003UÒPQg?<àòj\x0005¹ý¼^"=Ç5ØR«1¦ÅÇ\x000eTvUv¸¤Jµ8¦\x001dÆ\x0014\x0006c
\x001acÈ
2\x0017Å¦±rImo´gÚ{æ¸\x0006c
\x001ac²ÊÔLµ¶råVÄàw`¡©Æ fr^0gq\x000b\x0016õ¨Jqà\x000e\x001b\x0001Cl
à4QvÅ¢¹¼ëc¼¸^¶05ØyÐØùG:\x0002©1-Èæ¸HQ_:ã\x001aì<hì|¢ºçn7n
HXÜZ¢û\x001d!3\x000c\x001e4>cæ2\x0000 G(SÏ¢
(«\x0015óÕ\x001a,=h,}&µrä¯h.ù#bÛó\x001e¶§0zÐúÌ³V	ËçK>­\x0008\x000bÍ£8XzÐXúLÍáõ¶Oâ)ËWd°õâÂÁÒ£ÆÒgÏõ9\x0005+ÔÊ¦\x0015³`Ù\x001d\x000e\x001b\x0007C\x001aCO\x0015¥åhå\x0004Ï"®×GÌQ
v\x001eUvÞË4
 }\x000eù"\x0018Ñ­'3ç¸\x0006*ÊßÄEb:iá\x0002#¯]Ö]ç¸\x0006\x001aIô4ðHª\x0005\x000b¼¼\x0011ÂzEä\x001c×`RQeRsïô_\x001d#HNÚáv\x0013AEAÍyÑÛ *tuÎ7 PgÚ©æ¨\x0006{
{\x000c
há×\x000f\x001a¯P×
Ñ²w.îà\x001a\x000c**\x000cj2¤' \x000f\x000b¦
Õ&o5¸}o¹Á :AMÖÕ\x001eåY¼*\\x000e¤Åy\x0006ã\x001alSØ®T\Íò»ìùT¥\x0018Ê\x001fòN
âa½ÏakQ"F¥|\x0016·%/\x000f¾7Å1ºà·7nL *lj*¿.%/§1U.o\x0012\x0007ÏÞÙíip7ØT§²©Æ¶Õ«iñA"ùE
Û}£\x001blªSØÔT¼ 4ùP]\x001eÖõrIö×¹æ÷9®Áª:UBÂyNÐÓxZEëB¿\x0005+ºõ"Ú9¬Á¬:Y]\x0004áùe/£DõåãÉö2ëSs\Yu*³\x001a\x001270"
ýãåBQEKhÖUG¦¸ü`V½Ê¬¦V§\x0005ÑËöÇ<vl{?\x0004ª^ÀÌf\x0002}ð[ê<õ*\x0017¡íæÞ\x000fæÞëÌ}{]Dï%ÄqAÇÏµñÌq
æÞ«R\x0012`ùE\x001bI\x0008Ý£É²¿Âv£ê\x0007cï5ÆÞú$×
µ\qqâ³óöPÂeª|Áo\x0018"\x000bÅR\x0016e;S{Vk0õ^eêIÁ®TgjA\x0016­\x0003y÷\x001dï\x001a~0õ^cê#UVÛ\x0015)ÄÉbêy½¢Ùs\x0016\x0007[ï5¶Æ×w
ð6Öõò,\x000fð£\x0012Ù\x001d¶k°õ^ õª\x0003^Ë}Cú&Dâ\x000e\x000f\x0014\x0006K\x001ft\x0001t\x001d&L»+»EvV\x000b½xÆ\x001cwp
>¨\x001eò¢T2\x0015Ëåê4\x0017ÊÕ£F¿#P
¥\x000f:K\x000füz
NÌÒ\x001fjÄü`\x0018,}ÐXúHC«c]/ÛÃ»\x000b¹\x0005'=%\x0008a°õAeëcZRá´^'±P$!-i~Ïëg\x0018¬}ÐX{O"o¼^T\x0017ÌÏýÀ«eÃ¯8FèÂzÇùAÇý\x0019´XÙJù^^ïßÃ\x001aL}Ðz_\P5©He©j¨Gé+LÁì\x0008oÂ`RÆ¤tJíOÆ`«fÔ2-ÓDÙô;ÂÔ8\x0018¯¨1^®Ï5·>\x001efy4YòÙnßôq0\x0012Qc$H)1W¹\x0019\x00199ÉÚÉêã\x001aDT"\x0004#ézgM­"×%ÄÁ\x001d9Â8\x0018¨1\x0012º¸kã)qÂÓ°
WP¥]Y8¨ªF\x0000G*GA½m!áì8ÖPiì\x0004f\x0011½CG\x000bµ\x001eÁK\x0004½\x0018²ÍXCD\x00185T%ôâÏ\x0008è¤\x0019?çìëz-s\ù\x001aóEíuN\x000eÐq!\x00062;=·ì4ÄIUÜd¾\x000c ûj&rr-éµã8¦Á¬&Y¥fT¾6ò¼4\x0012J b{r)
!aÒ\x0015x\x0005.X.hµo,õjÖk]êqk°öIcí\x0017\x0007n\x00193»²sùUZ<ãºôù\x001c×`íÎÚË¶G\x001fbÆ\
\x0012@¼Ðí5XÕ¤«ñ±`åö¥lÉ:hÂìÙ_ùJªr*_k¨(Ê!-\x0011^/\x000c©öÛÕ<¬*[¢®fN\x001cÞ¬Ì`IaGyP\x001ecÖ\x001cÇTÖ¨¦ÆË
YyJ°\x0016$¶;J×ó°í³jÛCûÅd-=ÿKÁKËØ\x001d7¡<lû¬\x000b&\x000c½Â\x0018¸ò¸X E¿.Ë1Ç5lû¬öÚu{Q\x001aË©<W>§dÖå8g°ú\x0006º¥òYå\x001d½]\x0014®Z\x0005M`ÀuÆ)ÙõI&s`c±Qù!y\x000cc±ìN
½e¡«\x0014Óú\x00009°±ÐØhv~\x000cv© °\x0008µ'ÂU®õJ¤÷·\x001dl,ê5ªVà¹z©\x001cI)A3RÄâ\x001e¬±|Ö¨v¾C.p\r_3YêÙ°nÏNØ£¢]Õ?åykÒ$Ú,3³\x0014ö\x0005Û~ï°G%öª\x001a{JØç¶ó9¾"²ñ·ïû£\x0002{U=i[ÎÇ¸ÜØæ
/\x0007òÌÖ\x001cØ¸ïUÕìê@ù;\x0007G¬	8bMÑmO®Ú£ÂqUå8	ºòÚ\x000cH\x0013Nn.r3ÖXmU\x0005Ú>H©*F\x0013dhZL(\x0006Ì®Ot\x0003;j-Ñì{ïQÞ`\x0002Ec[¼¸\,Å\x000e°që«5ª)\x0013@\x001d5sâ\x000c\x0018l/\x0004°cy¯UÕ÷R\x0002·~{M£A¬Bj\x001f;VlÜúªJZ ]¹
fB\x0016cÒ\x0004@3¾¶ÛÖ±dÕªjV\x0001QÞÜMÀK\x0019îÉmÇËo÷cu¨UX+ÔìIHUÏpÌ·îb5vp[_U\x001eJ_µ\x001f\x001cÞ×\x001dfô{ù´®]<\x00076n}U\x001d&©\x0001s­600\x000fjCiËqÔØ±\x0019lÜú¢Ç¨ô¥&*L¹*\x001f¤\x0016\x0013`{@MÝã~úÜ³9ó?èù7\x0019ô\x001cô\x0000P\x0000ò5=å=Ý&Æ\x001fÓy\x0015\x001c³\x0003°É\x0018\x0016\x0019[FÞKï¦Ôf>\x001eYÇÅïÿû?ÿëæó\x000f=»lHCµyÐ¨­c\x001f¨ä*sÃ}fµ½ðÕÅÍýÛ«×?¼ÖõÌå£\x0013lZÚsðªâàl\x001d·Z)ý\x0012éß\x00061\x0000ªKê\x0012/~þú\x001fÏÈ[Ç5£ei\x0002Ë\x0014;ËãvIïvÅ Ý_üüî_ÏÊ\x0013\x0008\x0011ôD0MD©úØm"ò [Êð'4amb×\x001c\x0011öD8¿FT'ZJÔª
6fY"·VD1\x0007äz 7\x000fTÖ¥fL\x0000`]äÅt|^\x001dA0ä{$?DqU»p¶EbÑfam\x0016Ç\x001cQèÂ<\x0011dùlGRq£ ¹µøy\x000e)öHq\x001eÉâò.»,\x0012\x0017ö.c|2#­ÖKÌ!¥\x001e)M#¹\x0012\x0001Ö\x0016¯rþ\x001d¿\x001a§\x0012D\x00041\x0000kþy\x000e)÷HYä8Z6>f(HR"\x0015®Xf
éX¬¤f²Ñó\x0008ÆòÏ|sõ\ÂîSZËÌ1{ÞtÓ¨\x001344¡7ð¨\x000fi'¡uÚºì`»í¼ñ¦©Á¼Ã]\x0006§¶*^§¸ÖÖ5Ç4Xo;o¾I÷¹\x0016\x0018*à¹cÖ´C·Ù4ÙÁ~Ûi\x0003^Ìa\x0012kIz²õ\x001a\x0011=&Y&»Ö¶;Ç4\x0018p;oÁÚú)eÖÝd<åÓm6Nv0ávÚSM\x0014g
	)Öi6Ñ9\x001e¤¸ô7oe\x001al¸7â4&&Vóäh^\x0007K±rO~MJf\x000ei°ávÚ{zª¨\x0014NS=uùZJ
\x0016i0âvÞ®\x0019:Çª¦åàxÌÚÌµ) \x0018L8Lðr¸\x0002OF2¤¡_÷wH\\x0000^<ÍZ×Ã\x001cÒ`ÁaÞ\x001b*]©^rW¬Ö\x001c]íÖ\x000eÎ1Ñ÷´\x0005÷fåÔ½ù\x0001?8ÖB)Hkéã9¤ÁÃ´\x0001÷´ª\x0001\x0012f¦ºL\x000e?]Hkµ\x000esLµikY¹\ÐËR[QsÈ3T|p[ý\x001c\x000c	¦
S±;2Äúoyut2Ó­ ¥Ín°\x00020m\x0005#;0·
à\x00157çåË­ÕN!ápèpúÐyzâl,\x0003áT&'¶)¤Í\x0000Ç\x000bæü\x000e§7ðZXN	À§\ç_{¤#\x001aö7Îïoz×Í|æ\x0019¨¯"\x0011¥
Ñ°Ù4á°Áq~V¡9lp\x000eÂÁ¶Nk£ç
ó\x001b<ÄØl\x0013=T2SK P\x0006{#\x001bv¸ßá³m*\x0001oeC#±DMkU\x000csLÃ\x000ewó;|Q­ç\x001d\x001e"KÝ\x0005o Erk½£Ï3±cê«ü0è`Þ?<}ørqõá·Oüól^ÎÛª\x000bh¨|¡öí$dó°ª\x001auuûúíÅÕëïïn^\x001e\x000e´pÅ\x001fs«¹!5°å\x0018µ´4,\x0011ÄjBSÁçz>§æ+w«*Ég(V¯jMÖ:Ãn×{\gøÐ\x001f­_1=ýúýòðëï$¿z6ºÊ\x0018êÀ©]ùËZxNE5)ÕÎ¿\]ÿxó2ë¹+ÒpI¿`y\Q\x0012æz\x0012\x0016\x001dÖíX¡Ç
\x001a,*\x000c^.\x0011)Ó³®å§-#~ÑÄÕJÄI®Ôs%
\x0017V&ÂÊyMõÊ2¾¹|ÍÕ\x0013ð\x0002V\x0001\x001aM\x0007\x0011éøZmÙÕÓ3º¾¶«Úiå\x0002ZSÔ¤Öë¦wn\x0010·zW-ÙÕís¾&\x001eóÄçýû§ÇçhSÕ¦[C\x00126<2Ô\x000c+\x0013øÁæ\x000bÓ«W·Ï*
3\x0016ôX0\x0015H§Ó²ý\x0002\x0011©%«ÁKeÝ0·D=\x0016*°r\x0002I	"\x0018ÏJ_%\x0003!TVbù\x001eËk°\x0014L
µ.°djd°ixQbÅ\x001e+j° pc¾¡Iª<-*QÝ\x0015Ä!½ ÄÊ=VVî­Ä\x001fÆ½\x0005iûjÙñ$*b¹?ØÅLÑ\x0003VÙ\§ÍRy\x0013s
=Ê³\\x0016,X\x001e ¯>ýúûã?þøg1¨g=6©Np;-ÿµÚe¸¡!@Ê'ÆëâÕÅÕ]±§¿Üÿó\x0012 ô \x0007t\x0014\x001eVC[7"Õ\x000cñdñTxØãáõ³qmù/\x0013ítzõ\x001b^'ô¾\x0007ô\x001b\x0000I£¼>\x000b8¯\x000e\x0014*\x00190Ø}\x001f8öqË\x000et<|Îäbå2¯ oÆ×\x0013s¢\x0002Ì=`Þ²µÖLP¥Qi\x0005S\x0003<ñYs|pt_¡Ì!\x001fáï\x001e~ýõ÷¯Ï=Ép\x0017Ê±­c"\x0012µp
ÎGçâ»«ëë\x001fß·'pt?!\x0018	¾Áxä^­âß9ÓDs\x000fâ&\x0018ìap\x0012ÆgÙN©&\x0013@\x0014é-*IÂñ²fÅ¾^|÷ñéóÅ/üó?}8»}2Mhå"\x0014_ó:²¡"\x0014â.ß]|÷æöþâÿuûú%2×9
Y2¯;>ÕY\x000bX\x001fËA¥¸t;YèÉÊÄªzs(¬eyC\x0019ä\x0011â8\x0004]Kz²¤#£.£*w\x001dl®9zJó\x0013TH\x0016w|Í®0¾-\x000fÒ
´\x001cóÛP\x000c)Ôj'4¢Óüð²9@náã<~:n¡ ß\x00083Ð$ÊÅ¾\x0011-\x001cÆ7ÿzs÷\x0012ëAÜ\x0014H\x001a"Kï\x0019<\x001b\x0003"HZÇâ\x0016Ð9\x0010/»V¤\x000en. r-ÃQÊm\x0016$õ i
$\x0003\x0017®Z:kÜ	EÒ
\x000bz~ûæ¶}_"	ü$°$þ6\x001b`äØ=KÇq1\x000eqñÃÅw_\x001f>üöøéé|Á=R{_Ê}\x001e/}ErAÎ¸ÃÓ\x000bÎÅ««ïÞ]½þþæîö¼ÇÇã\x0018x
®,RÍz[RHm\x0008Í-þÏ¬Äs
8ìáP	gÃ²\\x000b\x001c¶Êv/Á¦sq%VRÀ¹\x001eÎi?«ÈùX+É]Z9®h\x0008c\x0011¹í8Y-Ysýð¿'¢Ò¸:e\x0002ÐJä\x001bdØ'U>\x001dí³ë«?ýéE\x000eè9`ÃÕY|\x001eRÀ1Dà'÷ù)\x000cì1p
Þámãð²\x001e\-´Ãõ\x001cnn9\x0012+5ÒÔ\x0003×IßEÎÿ8Xf\x0016Ä÷ ~nAì\x000f°r·\µÃoÀ\x0008=FÃ\x0008]&\x000e\x0013«j\x0018qx9ÕáØkM¤\x001e$M$Qhµ¤&x£\x0010Q@6`ä\x001e#Ï­Gó\x000fËþ\x0000^dÛþ@=Hç<É~¹\x0005q\1bI<ózÈy\x0019\x001fg9F;6gÈÊáy9P.\x0015A¾,HÈ\x001b\x000e\x001d\x000c³d¤zÄ 2hHR[°ÁØÁÙ9cFe«lÌlM/×o#7lYÁÙ9km}÷¢%1m·J9AY\x0012¿áØØÁÙ9sÚÀ.°Fº¥ÊÇ²$nË\x000c\x0006ÍÎY4ª´â8%G\x0019i\x0016bn¡À\x0003\x001c\x00078·$Ü4l©\À²e¥\x001eS±¬[¾Í`Yíi
Æ±\Ø²"À»$\x001dÂJ
$qµsÖº§ÅÛÅÐ.k\x0012ÛÁÙ`Ô`0®0e\\x0011aä²$¾jÄ²;DÚ[H\x0006ó
sæ5gÖ«~5ÓÜJd²a¿Â`Õ`ÊªNa#cóR·%.g\x0003È`K`Ê\x0004#åÉçöqßpp`8Á0uµ\x00151r¥\x000f¹\x00195¿!HáÜÀÔ¹	Vô²ËvÍ\x0012ÅGÓv+ª@Üñ=ÚAÿ\x0002}ýð÷¯¿>}xæÝ+Btfb`k¨°/ö1­<A__ýüîúöõs³xïÐ\x000eú7èÁ\x0012zb[b\x0004NWG\x0000Ù;kïÓ\Øs¡Ë¶2\x0002\x0017\x001auÐÒ\x000e{À\\x000fæT`å¬ñ\R\x001bj	õà¥¶³òÊëø4Wè¹jÈ¯\x0003fÖ1Wpb_y\x0006=XT%\x0019eËÞ2à¥ïÔ$±\x0006,õ`I\x0005Vn.Üªk1sf+\x0015*z\x0006·å\x001e,«ÀÊ¾bsn(^åO(©âqN°\x0012¬\x001fÊ\x000e´ú¤\x0019;Q°VË
Ê§FvòÀ« \x001bíëÿ\x000c¬\x001d\x000c¬UYØh\x000375³ÜE\<²|Ì+\x0015\x000fÓ`µ*\x0013\x001bç\x0011ª&f0w\x0000²iÛÁ\x0006\x000bkU&¶ü?A¸7ðÂE![+õ&ó\x0003×}Ëª°¬­.\x000bò1Ãq<®"\x001b¬¿Uÿà2·=5dsrí\x0012á´p@A6«²ÿÅc²Ø5®ÊöÐY	Ñ\x001f¿i¨È\x0006ûoU\x000e  HµüÃËZlZv9\x0000>ïùý·*\x0007PäcJ|Æ\x0005Å1É\x0001pk\x0005³d08\x0000P9@Ò\x001cÙª^Bd©eÙN^1Ud\x0003\x0000\x0003 WÞÀ\x000f\x001aX!i\x0016ýãZ²1ÂV9@wx3Üò¶@`¢mQ\x0002³\x001d»\x000c\x0006û\x000f*ûÿyÅ\x0006\x0007\x0000*\x0007@ZcüDm\x0013cæCnWüã\®lp\x0000 r\x0000¡isZúÊý÷Nd´J0{µS
\x000e\x0000tñ?¢Ì¬¶lqiÍòá}dÓÁ\x0001Î\x0001øÄ\x001d¸¤ùÊ-7Éåö²\x0007ÇÙ4\x0015Ùà\x0000@w\x0003(>ÜËA`9ù\x0014 åùòZ\x0005ö4Ùà\x0001@ç\x0001 K.M=rÛ±ÿq°ÿ¨»\x0000Ð#\x001c'ßlæWÉ\x0014¤ÒÎÓò?\x0005Ø`dQ\x0017eg\x001a\x000eêÉK|ke~µ°xlLdèÌl	Ç8a`\U"[\¦<£{âìQN«Þè\x0016Å*ÅÕ)\x001d.(My\x001açå÷x\x0002jÀÿ«w»|\x00024ë$J+CR~ÏÎå\x0003íòuñ\x0007¹Jó\x0018Z\x001b¶\x0001\x001eWz¸C[Î×ëÇ\x000f_é\¢ö®Ô9RNY\x001bíöyì\x0014Þ]\ß¼~ûLß;.ùp±+O}\x0011¨\x001cÓÈI\x0017ÇRÛmø´\p\x000e\x0007{\x001cÆq¾\x000bR£\x0004?A\x0003ÏñãÂ4ëÜ<P¼\x000c-'Å­\x0011Á6#ák¬§y|Ïã§yYØ\x0016HêRlnWñ;Ò,PèÂ<È\x0017 Ãv>\x0007Qb(+tO\x0005=P\x0006:Tç.b\x001aüÉ ]¼ÃJEó\x001cPêÒ<Pæyè£±ü:Íû°õå\x001e(Ï\x0003\x001dötù%¤$\x000bt\Ú4ËcG£8o\x0015©ÂcÜ\x0015}\x001dÔ<Ç½.
Fúï\x000f=ß%ì£g	Ü%t±5C%Þ\x0013\x0015¯~x\x0011\x0007{\x001cÆñ±h\x001f¿$à[^ðäMh\x0016È÷@~\x001aº¨9\x001bª\x0010oBðWöÑÉSÐ,Nìqâ4\x000eøå±`Õ!±Õu§ÎÛYÜãäi\x001cx¥%	^Wï
h¥Ä\x0014ÓÉcÁ$\x001d·óô~¦\x0019~Rè]\x0016»Þ¡Õu`Â\x001bÈ\x000e;ÚNoi\x0017\x000f\x0003tØ¸u)8q\x001aé¤FøE"üXíÛcõõï\x000fùË×Ç÷g
\x0010zÛÞ\x0004ê\x0004eÒnçÝ\x001dG×?^ýéOïn^½\x0004\x0003=\x000cLÃ ¼\x001c\x001a\x0012ñLÓêòýñõ|\x0016\x0007{\x001cÅ¡ÎÿÔv\x000f;øÅi1Îq¾l\x0016Çõ8n\x001aGÓ7E\x0019Þ¶\x0008ú¤"g\x0012Ç÷8~\x0016\x0007«Ì"ïdùX.µð\x00077â\x001e'Lã¸f|R«WB×^*\x0003lÄ=NÅ¡|ÎaïÔr\x0014ì®`Ç¯3³4©§IÓ4i-Åqÿ/qïGräùn\x0005\x001b\x0018ZxÜÃôbaª0\x0007\x0002k@²ì¨_d(\x0016$¡EÝ¼èúi^g	³£uh'³\x0013éî\x0019\x001f\x0010þ¥ÚN·\x0011Æ¢Jª_yFxDøåïA\x001cÇÎºy\x000c§e²ä\x0007xÜÔ\x0010E)R^Ê¬íÖ\x000b£4×a·Cª¸\x001dª¹sR\x0012ã6%¢/áÄõK9.=\x0011\x001f?ýõñËÅßþøí9Qºf"WÃd
¡ú7s\x0011>¬K\x0015^ß¼ùùúíÅïxÿÌ\x0013>®_Ìqi\x0018\x0003Ë\©
7¸à¤9À¬[\x0013U\®år:yÒ¤­`ÎÕ²´Þ?b/ßry\x0015Wác\x0000A
ä\x000f?['CU`¡\x0005\x000b:ER®`ÜC]
&ý@ëÆx\x0015Wl¹¢Î`Y>d}ÏZdpÌe\x000f­üÔ%ÁxôR5ãÇl°RÖ\x0004ë°®
,·`Y\x0003\x0016ÒÇè¹Ö\x001e%ÙbëÎW\x0015XiÁÎWXÒ»\x0001Ta£Çmp¡²SG\x0001Ö\x001c=±é\x0018\x00193\x00198ÉÐâgeY\x0008'=ùÀ®Þïë\x001c¤ãR?&,\x000eV2TvÓæ£!ë\x001c?¨<À­ª@:éÍ¸HÇ÷
ÛZ²ÎõÎ÷\x0017 ¡ÇÕf4fÐÇò×´ëÐ²¬sþ òþÁÂb3Vå)Rpâ·åÑ\x001a°ÎùÎû×c)°¥I\x0017Eô3¼=rCçüAåý\x0003^T¹Ûs}(²1]_
5d÷\x0007û/®§2`ÃB- õÉpduî\x001ftþ¿>Ä,×à{i¤5RÖ\x001a\x000fmÌÎÿî\x0000Àîv²Y¢é%¨®ÄËl­; á²û·:÷ï4m¦ÎDq`ßxä¶h;÷ouî\x001fS?T:ì"\x0007äå`:âþmï×¹Ïz³`¡:ú È*K\x0007|íÜ¿Uº©Q$í¨ÊË6ÛôLiÈ:÷ouî¿>Ý» ]IYùdìÎÿ[ÿ\x000f\x0006H'¨Ú,r¶1¥\x0014l\x001dYWu'Õ\x0000a\x0016äl(\x0005Y5±Ù¦½XCÖ\x0000Vu\x0002 X\x001cM©È)\x0002ùMüMCÖ\x0000Vw\x0002\x0004Ë_\x0013[²\x0003íM\x001b¤%{Óý¤!ëN\x0000«:\x0001\x00026V&)Ró,\x0010Çzi<`3×\x0001Nw\x0006 {æÏÉR}\x0007læº3À©Î`\x0012ç(#bé\x000e\x00149ììý¯éº3ÀéÎú §fÝ¼\x00030ÑÍ½cGvë£?ª3 üÊÐ³)\x0007Q©Iöæ¦§YCÖ\x0001Nw\x0006àõlF\x0015S×K¿Ý¦\x0015^CÖ\x0001Ny\x0006\x00141ÖÇ	?´\x0003º3ÀéÎX¸´ÕºÄ
Yðú4\x0015Xw\x00048Ý\x00117\x001fæá|]ºÑ.OàF\x0006¬;\x0001î\x0004¨\x0017\x001frf\x001eX	cuâ^ÅÕù§óÿà8ñ\x0000õnX=R\x0014Ã\x001bï¼¬×yYÒ>Y_Ã\x0019ÏÌmúJCÖyY¯ó²YjB¬Ï,#\x0015#'kê}÷\x0008Yçe½ÎËâx.IãTS8CzÃ\x0011/ë;_æu¾Ì²"èÔþM\x001f3/b\x0005G\x001e'¾se^çÊ²8Y\x001bN}4\x0006sä:ë;_æu¾Ì:4Nà´5s¹Ö>VuÎÌëYq$Ú[mæx¦:V|³ÍÜ¯Ù¹3¯sgXp$ÔBc\x0001B1:Ç\x0001î:\x001bt×ÙÂ#EÀF'Ï¦x\x001dNÎ\x00057Ãbd2Y½
ÑúÏ\x001cj	kh\x0015WçËÎÉ,nÀ¡Ò@·²\x0008­lÐ\x001a²îÆ\x0018t7Æ"\x00156\x0001ç~c¼üáHr"tÎ,¨YeùÇHR\x0008%\x0019õ\x0010`S£!ëYÐ93çi4L}\x0001;ÑÂ\x0017}Í#WÆÐ9³ rf\x0011'¤Ò:Ki\x0016@¤Zx\x0003ØC6ëYÐ93ïäkÖ³\x001e&à%hp`Åîf\x0016u73¸ì
_T\x0016AnfùHÌ v>#ê|\x0006&Ê\x0017ÉJ¾Y.×Å.ç\x0003dÝý'êî?ÁKD\x001b'ßq0ï?ùH
8v\x001b3ê6fHÒ?æÍ¤<3\x000cDm£Ý¤\x0001ëVÔ­þ(Éi[I\x0012±\x00181Þ¸Ï'KÝúOºõ_É¨D´®,ö²\x0012ý)\x001bÝK
W·únõÇ$>¶n\x0004#µêY®²\x0007\x0016YêVÒ­þ\x001cå\x001c·Å\x0004|.Ù#\x001e#u«,éVY	T0n³lÙdÎw¯EV¤¾ìÓÇOO\x000f\x001f/¾ûôôôðõô±\x0014È\x0001GÏ\x000c\x001c\x0006Ä)à\x0015×7·W7\x0017ß½¹½½z÷\x0012mÁ¬\x000e¬Þ1
gÀf×;\x0006Wµ{×ë_æ[4¯C«LàBÌÏßzý´ù&Ñ¤B-ZT¢yi\x0006Ç\x001ey¡%pKÙÈú4W¡å\x0016-ëÐêEÛK¥\x0001z&+O¦m=¬­\x0002ZD×Ñd\x000e#KhU6]f×\x00033tlÝ6\x0000å> Cêà"	Ú9ÙMNÅÖí\x0003Pn\x0004_&';\x0015ve~\x0006ãÀ_fÛÄTlÝF\x0000åN\x0008Qªá0ÅCl2Òi+X¢cëv\x0002(·\x0002Î¨ ý
/\x001aÉq\x0015vY7\x000e\x000f¢%¿:\x000eê#¶ÕRùôïß\x001e>>~øôõ9e\x0004?åô]1ShzÂ¹º\x000bG¹ïõ¿ùïï¯n®_¿ywú¬"8ÛÂY%¯7¢y\x0006\x0011$$\â)WÃnÁ¹\x0016Îi-\x00074¢\x000b³ul7\x001eÇ\x001dÒ¦ÃHæ[4¯DÃi	óô«ISà\x001cÝê£aW¼g\x001c.´pA	W7*MKÄÑ¹~ÊÀ\x001fuÓ©-\Ô®¸ p®§¹¤!¸]Ùq¸ÔÂ%½å"Áá>++?ÖÏ\x001aöôUÆár\x000bõüm8í\x0007ÏûÁm\x0007t¨ØJËVl\x0019¦\x0008ü´\x001f,ÕãTÇ\x0016\x0004nÕÁ5\x0011ôÀFKç¨©Þ\x001c¬¹ú\ :»\x001e4 ¤ëÏ\x0007å\x0001±Ê<Ñµ,Ñ\x0014±èÖÙb%]w@ö(\\ÿ5\x0013eÙs\x0004qÃpÌ
CçAé³a­¾ºD¤­ZÂ3áÎ8]çAé3æhÉÔ&íè"ûº°¨¢ë\x001c1(=qFi0þ²sléÖ
%\çë@éì²Ç1£?\x0001VFâ\x001b[g©td¶s&VéLPN9ÐÇÔÆPØì@\x001e¢3ëË¦é/}À¡°Ï\x0014lb_\x000fÄDNÖ\x0002+Áø²Î¼Ïhwß_áTØ\x0017ÉlKfd~)Ø\x0004¡¯:4×¢9\x001dZ
,ªFKÜ~$]>e]\x0019¯Có-WZ-½Jf%Æ;¥©8pÈj±EJ«TÖ½ÊõÓzªXÛu\x001f£h¹EËê\x000fÊ\x0002fÖKiüûÎìÜ1´õ`Õ\x0004KpðË×ï\x001e>~<©P9êV¹ròs·þMÞÌ&KÆåÍ\x0003úí»«ï®nnNk\x0014¤õÕ\x0004K`p\x0000ª.1*V¨çæ|
Ô¿É\x0005²kE0\x0005k¡\x0002
5m,Y
x\x001a¦ÔßP-µö±
(ßBy
\x0014G[C\x0005JkWCmÃFÃL¡e
ãLØdá#AÍ
\x000e\x0008ÅxÕP°ÎÎCÅ\x0016*j <\x000fB¨ìÉMP Zk.* R\x000b\x0014PÞzÆ^ÎyóÕÛ«¬óMé8Tn¡²\x0006Jº%ë'ê¹\x0011J\x001c]Ëº(JËT\x0014Lõ\x001edÛyëÕ+\x0017ÈÇ;{·¯8hBÊ#PÀb±Ó(è\x0019JÜ\x0001¬¥]FòúºM£çôý§\x000f_\x001f¾}¾¸þO÷=\x001dx¬¯\x000e\x001a®W©Ök))±e=¢ìû÷\x0017ß¿yýîêýÝÅõ¿¼¹¼ûþ%@×\x0002:5`½å'ÈºdceÚ3k
\x00065 o\x0001½\x00160\x0014CãMAåQ\x0019¾Géb\x001b×l5`h\x0001Úâ.PÏêÉÛÎóoXjmÝj­Æ-^ÔÛ'\x0016Uû%) :6Z¼Ôâ%½õ2g
&ÍzÎL\x0004Þ\x001e­\x0003Ì-`Öï`Ç->\x0006+\x000fÙ~wðö­\x0004lÜ\x001eº\x0018£ßÂV4f(Þ1ÏP£J\x000f~ã&DVMè\x0012	\x0018¨J>Y+[dó¸Ó\x0002v>\x0006ÔN&\x0006NÂT@ÃÍÿÉ;&4\x0001\x0005ãë\x001cQöýdèï¿}¾úpZ¹¬>Xæö·\2V(¯£e}¸l\x00038Aøû÷w·¯9àÖù¡ìû©Ð/aÙ\x0011\x0018Ðó3\x0007\x000bÁÖ]ö*0×9\x0015X¦T\x0005«OvÒz\x000b)³ÅvFt(À|\x000bæur1¬\çà´\x0010ç\x000flÚ\x000eõQp+h¸²1Ó;\x0018Áì\x0012ë3\x001cc¶aÝÉ®\x0002-XT\x0019,RE:~IÏB!Ðý	¿ä\x0011å\x0016,kX\x0010Ä+ìa¯ö@h³\x0019c_Ô+\x0018\x0000IjÕÝiØ`;ÓÜÈÂz6ïxõáÛçÇçZÅ±ÑKã¤¶g#Eq;¡ýíÅÕë÷w×ÏTc\x0011Tj¡\x0002
»w%zç£/\x0012ØKe'\x000eô\x0002\x0013¤U!Vý\x0003öªW¿~úVO¡>ÿÇß~ùÛÇ/~<É¨zÓçµõ
G×rÔûêÙ®¾ó¾\x001eC\x0017?ÝýËï¾ûÝÍÛÿëú%Dß"z5b6À×\x000eï%V
¿Nqäp:\x0018ZÄ ·"UKNd0ræ«[Ü(\x0013ê	cK\x0018õFÄ}1¯AïgµÂ\x0002\x0003V\x0008ÃQÂÜ\x0012f=aN<Öû2ý\x0016\x00119Q\x0011×­zÄÒ"3Vba\x0018ï3÷ \x0008¸VLW#..\x0019\x0011Ù%k\x0018KæÖ*ïì\\x001a¦²`Ú,ë\x0010="t GtË|A\x0001¥°ÐNLë±s ÷Å¹æ\x0007<N$­\x0019\x0006B´ëh\x001eÑuNoF¬#×]khÃ°|½\x0003\x001eÝ/ÐynÐ»î
è6Ì\¿­c<¼a:×
zßs:ÈX\x001f\x0017\#ÇÓÿ	n\x0007:ß
zç]ê¡Rn_ï©\x0014\x000bÅ~F\'lô©cLg|j+¾1æ¹Û\x000eý\x000eÕSÅ¸Nßè\x0011»\x0003\x0006ô'L©"*<÷nKVtÜ¨\x001b7CSôÝ\x0001\x0003ú\x0013¦\x00040<×AV+Ê´í\x000fiÛ0VÂ(\x0002ÞÍN\x0007Dð.®«Ðõ|ÝñbõÇKq;Å}\x0006vÜ¼ËºïA\x000fØ_¹Ï8["\x0017¼Ôæ¨\x0001Ú»c^÷eë\x0019»ÃÅê\x000f\x0012Ñ9óBÄ­=3&³uÐ3v§U.õ]`XF\x0007E5gÇmU\x0014bY7kè\x0011»ÃÅê\x000fÚ£ärÊ$àVLIfÝ\x001aªGì\x000e\x0017«>\2\x0001á\x000b#jFÎVx¯;Xì\x0019\x0007Kñò¶*e¾
XÂ\x001eØë¸¸±;Y¬údÉ88Õ\x0016v9sr\x00015\x000c@Üö:ê gì\x0016«>ZênqC=á8\x001fÐË;q\x0010òQ;ºîhqê£%c
{°r\x0017Ks\x001eÚå(ÏÔuk±;^úxÉ&:Öû\x0008&Î\x0005G\x0001«SÄG\x000f\x0018×\x001d0N}Àd°Ràê«z&t"b\x0014ÍáÇ¾ëÎ\x0017§>_ò4ýcv\x0001H\x0006³2\x001a
éW+\x001eÞ1®;_þ|ÁÒ{\x0001è²ªÌ¦ÕÈw×²Ý\x0001ãÔ\x0007LÆñ«¼cªw´¾57%³n¾\x001bg¬uQm!èÕ\x001f?Þ?}}®\x0004®bÍÂ\x001bSøºPï)I¢êª\x0004|þpsyûîÙ
8"³-Uy¬X¢\x000c	p)>]áÒZèNGæ[2¯$£J÷9ÛeF\x0005[ÖOQ²õÜ°,sÃ®þòøñáâoÏ¶:ã\x0011:å0ÿK\x0013\x0018cyL[ÖõTW¿½¾¹ºøáýõ³½Î\x0004f[0«\x0003Ü\x0005UHZe\x001aï%1½\x0010kÀ\\x000bæT`^b\x000bÕð$ã\x0002?Fl^ç£U\¾åò*.Ç\x001dm¥ºs¬raóz°´+´\AÅ\x0015ô¸ÉÓä3\x0004KÜ®kËºP\x0005\x0016[°¨\x0002Ã¡(sb<$¹xÃ=Î6¬çøiÀ ßºMªós÷DAY9 2®\x001a3J\x0003Ö-}Ð­ýâ¨s¢ð¸r\x0001GPë\x000bãÅº5\x0006ºEVx\x0010w=<ÊyQ±q-Ù "K\x001dYÒùêUKUF\x00056ÞqH×MHWCV:²¢"<\x0005Á'²0_*wB¶ÖßÐÙný[Õú÷õPÙ+tøËô\x001dë×7\x000c\x0015X·þ­jýc®2*
Ê¤¹G&sëP¬Û\x0000Vµ\x0001¼\x000b¯¨P/\x0015Ökð2 Ðnò\x001a°ný[Ýú\x000fbÈÕgxV\x0006ÁÉÛâ3\x000e¬Û­«[ÿq\x001eU1ñ@õR}\gÎZeeÝÈQ -Ùú?ÿó_}}øüñÓ·`ÆqgI(Ø6ßc!¼\x001dEqsqõîêîæÍûÀl\x000bfu`Þ±ÇHÁÐ0ç
ÆE\x000f&m¿ÇÁ\\x000bæt`¡LÕ*\x0015\x000c+\x000bâü&)|WÄÑ7çsùËë¸"¿6ë\x000csí"beþ[\x0005q®Ðr\x0005\x001dW¶³¤ÁFMrcõÊB\x000fupÛÒ8Wl¹¢+ÅW´ð\x000c\x0018â¡3×zr§\x0006+µXI¡ÀÂö/ÖÆs¾\x0013;Ï§Ê-UÖQ9Çþ+eÃ7~Ã9ÎzBmäF¸ÂÚ}6>ð_?=}½|zA¢Ú)PnÒ°D'\x000f\x000fÛ¢ìúÖý¯onß]^ß>çWÃÚ}6<0\x0000\x0016<?ÜludgTHÃc	å¥\x0000s-SÙ Ò(F\x0002ÍìUÝ\x000cðÖpùË«¸ü4-{²Wa¥ù(i·`ö:Ì¹BË\x0015tö\x0002Q\x001a®\x000bß¯e}¶\x0003X±Å:s\x0005Ñ³C­\x000fRÚþfî°+µ\Ig.I©Ùê÷3mÈÌÂüÁm&kÀr\x000bu\x0006s¤1fCf-÷(¹¾`Ö)S
WS\x0007\x001eÌèÀi6\x0019à/ÉçP\x0000¿SÜ9LÖ¹0Ðù0Eÿ\x0018åwx\x001374\x0005»-NWu¾\x0002tÎÂIr\x0019\x0018I\x0013F\x0013\x0017/¶#]0LÖmKÐíKçeÎN
¢ix\x0006VXgNÀÀ¬¦\x0005×?h\x000fÊ\x001f>þíÃsXãq\x0019\x0007gÌ\x0010VX§ºëß½\x001eÁ²-Õ`A$Õ®z\x000b441\x000cÓùøÎëH\x0006ËµXNeaI!M¥\x00169X\x0011ü^ßý(o±¼\x0002+Æ,\x001d\x0017I<\x0007Qp\x000cvÏSb\x0016+¨ÖVâ,b©K;*Õ~Â(Ul©¢ÊXæU\x0014é\x0004K+Ë¸Å«\x001eXð©¥Jª\x0005\x001f¨*\x0014©\ì¥à¶\x0012ü\x001a¨ÜBe©\x0013ýq\x0000V÷Á<\x0003ë\x0014 \x0006«´XEUf¥¡i]\x0019\x001aôç\x0017ìI\x000cRAïI5®´z\x0007Î£>\x0000CHËÍ~'%9ÊÕ¹RÐøÒè¼8°Ï¢¢Züù¾\x0014:_
\x001ag\x001aT$BN|ô °è«ì\UG¹:g
*oNTgsõÐ³\x000fìË\x001cØ(VçLAãM±ÍÇ!Åùþ\ÑÈ=U¦Q®ÎÊ(cG3¿\x001b³w%R9ßI@çPAãQQØ4r Xzeod¬ÏºsFÕ¹TÐøÔP¿\x001dé ¸\x0016ÕN||ýÿó¹:
\x001a§q	G\(¶?ûz\x0017\x0003Æu=¡\x0002«)\x000c6©#\x001bÀ\x0002ôÆ\x0005KXnsþn´³·\x001ag\x001flye«^¹\x0008k\x0019M°ç©Áê¯Í\x001a_\x001fÈÑCàW½&\x0019½®q\x001bZ·\x0003\x001ai\x0007üõÛÅ\x000f¾ýõáóÓÃ_\x001eN\x0017cáÉ\Ùf2&¹)lYd\x001f¶¾ëýÅ\x000foÞÿ|uw{õÛ«ÛòÅ\x000cç[8¯\x0003¾Ô\x001b\x0014­¢1[Þr{\x0018ÄõDs%\lá¢\x0016.SF-§È3Í½ã;Hkq%[nÙ²
\x000fÊ@p^Cõ2Á¢\x0008°Õ/VÁ5\x001dk¦´ª\x0012terúH
%å"Ø^/ttÝ\x0000íp®Ö&\x00177ë"!\x001dÃ`\x0019¤aýîéýùþéÏæ#Aæ®çÈ\x0013¤Â\x0014¶=Ûz¶ÏäDî.oxÆÀJG\x0007¡¼\x0006j9PLbÓ £÷D\x0007bË\x00145Ly\x0019\x001b$ ¹\x001a
ù|¨ÜBe\x0005TâE_ïúë<[fYíÞõ í\x0008¦e¾Hcu)TnÊýruÝ¦©º\x000eÝ'ËuZèu}ó½õÏgWá¸
D×\x001fï¿}=)z¢É<¸\x0013¨Æ""B%¯üÁïß\x0014;`\x0010ÛØ!\x0010g©¸¤þWfå¯Iéf\x0001Yßl@\\x000bâ@Pö<Êzñ0\x0017Ç\x001cke!\x000eßrø!ú|¦à\x001aW³°óbußó\x0010HhAÂ\x0018HFÏÓ­xVø¡õº.\x0014\x0019Â-F\x001cÂ\x0008Fæ\x0018×/ù½´c\x001d0~Ã¯wh\x000býøðôùñâûoO÷Ï\x001d¤\x001e¨~\x0012¦\x0013\x000eÒÂu0,³â¹º½»®Çéíås§¨_ï\x001fQ\x0016\x001aÃ
2"\x0012å)Í[Qé7Y\x000f\x0015Ô`¹\x0016Ë)±\x001cµ<\x0005Çe°\x0015Kzi×E\x001a,ßby
Ö2èÜ×Gñüø¬Ç\x0016pïç\x0011c*¨¨,+:£\x00160éÎ\x0005\x001bôØ­]\x0002+¶XQ2?±%å$XgR5X©ÅJ*¬À¹\x0011ìöã3Ãfiã%\x0015P¹Ê\x001a¨Ü@6$Î\x0007aª#°´XEåiä\x0000zðSiiÅâN¯Í0	\x0005V{O[´Æ¸êEÖP'\x001f\x0018.¶\x0008eH°Zý|®ÞÇ«|¡®\x0002\x0008ß¢¯{f¬¸N»i°:\x001f\x000f\x001a'\x001f0)Bæ²=\ÚRX×Ìh¸:'\x000f\x001a/\ÔºE\x0004TÁV¹ØqÅu0OÃÕyyÐ¸y,Ê¢¨Ç6ÍM®\x001f/
×ïØùyÐ8z,å)e\x0004¤a	£´.\x0015ÓPuþ\x00144\x000e\x0015T '\x0011çòÅú<`¬\x0003{±s] ñ]Á%Ö¾ÆÒ\x0019Ò\x001cÖËG\·\x001e)¸lç#¬ÆGz)ô\x0015åF(ï¹ú7äs¸âú~\x001aWÔ×_~¹?E1UÓ(2ª\x0007/ýÛÛòµë·ß]¾d[$«@ÊH\x0004f æró¤ùr&o¼\x0006ÈO5DÓÆ²O\x0003´Íç\x000e\x0012Å(j\x001cWÅ\x0004\x0003¯V\x0013\x0003°õu¯2y(·DYAToW4r8À,(H6p7.l)^DÊë¥7KûÃiÉòè\x0002	óäå\x000bù3
Ô\x0002¬{*\x0008éõiÉrfr-Ó0\x0001iEgÅIWT2) \x0004ÈÛJQ¨ØB­WÓsP\x001e¦\x000c\x00112\x0019ÏÓê\x0000èV\x0015 lkGrË´^OÏ2Õ{'<¨î1\x0017ÖsÃPí\x00054wâ/>?\x0017( Uuâs\®ÇUàÏ·7Je;ªµÃ|~QU¯DTÞRø¹.*M(j\x0004ª¬7a¾þòôðñô9¿\x0014~	KUè\x0012[§Û¯ßÞ^Ý¼Äa[\x000e;Æ\x0001K P\x001a÷â¢\x001a¿	\x0014\x000e¸\x0016Ä
D¹U¢<\x0005ð4v.»r\x0006o1ü=Ô\x001b`i8\x0017\x0012ós·iÉ\x001e\x0002	-H\x0018\x0002IË¨ik8\x0003\x0019d}Ë\x001e\x0002-H\x001c\x0002	EV\x0008\x0004VÌ]Z\x001d\^ëÂ\x000c¤\x0016$Y$ðX¢º÷_±AXmÃåulb#·\x001cyl¥zÉ­¡K¡\x001b=HÜ:³6QZ2Zv¦ïÂï\x001d	¸MÅÎ\x0008HëõlíK\x0006)2pÙW\x001eR¤ãÒº\x0018f¤wªc^5\x0017ê2©nUjäKë\x000cÕ\x0010HçUaÌ­¦È`â+j\x000fòE,²Ö)\x0018\x0002éÜ\x0019ù³z\x0007¶1Òc1p\Ý¥õô³!ÎÀ\x001bÉÜ!^A,'\x001fn=\x001cs#¿ÿåñKïJð\x000fF¾P\x0010D.{B)­Wsë\x0007¦ë¤pnîÿzÿôë3%?\x001e§\x0019Í\x0017¹ºät»¤ks{5?7?_Þ~ÿL\x001eÓ­.¶E\x0004/Cá\x0008£ùÊ[êå Ì5§X¿¾ív2¾£X®År\x001a,Wæ>b\x0015
\x0007g\x0008T¿_±öJG±|å5Xq\x001e/X !¬ìø#¦m\x0013å8Vl±¢
«z\x0000GXÜzá\x0003¶V>ò\x0011S4XØ²Rf¬z\x0007-ü¢hpµÖ^Ýð(Vn±²jÉ¹R±bá÷$kEêvúåÇ±JUÖòV°\x000c[ÇO¸¼.,P`5g>z-£Ú³+§Å\x0015ËGö\x0010y¯Z~«÷¦\x001awê¼K¶¤øTßÅ<çÛ½ú§Q®Î¡Ê£\x001aº´U®Â=.\x0006õ5và3v\x000e\x00154\x001eµ.\x001fï\x000eg\x0005\x001bn\x0011	ÞîUAru\x001e\x0015T.Õð8=´ú,V?v£wk9a
WçRAåS}dU
ce¸	D\x001e»â7S1Æ¸Ö¡<û	M7\x000f}8\x001dà\x0008ÙÏÕG\x00185,©á,OõÙÖXãÀ«¯N\x00078\^_!r?éy¤-4b.nª\x000e@¤`8>µ½×\x000c3¹ÉiÌ\x0004sWâÌÄ5òÜLçCù\x0016Ê+ 
Ð@¦T\x001fþólçì\x001c\x0015)`+îNô|)´LAÁ%
\x0004\x0015¹
7;`geÍ¶
w\x0018*¶PQc(;W!V¨XÑ9x´Ó8\x000cZ¨¤±{$+\x0014\x0016(pÍ>K2n¦Û*rË5Ëª\x0000p\x0000Vüd(ËKÊï%d\x0006¡J\x000bU\x0014Põê\x001eé\x001eS£s\x000c6ÛDê:õ¡³\x0019Þoj\x001c'
BA*à¼JÅ³ªÜNeò0Uç¦@ã§ì|\x0012#U5#[E^Un\x0013\x0013UPu~
4*\x0005¾·gï¨¯ÎYÃK=íÉ\x0010
Bu
4
æÓõ8Òàl='\x001c&MÞs©:§\x0000
¯àê\x0018Ôlw µüÄñv-×§ êÜ\x0002hü\x0002ªà_@$òê¢\x001fëÌöÊ>LÕù\x0005P8\x0006¬ú$5<\x0013\x000b\x0005U3Ö ­ð½z&UÓ¸·\x0017£°\x0015N9`weI"#ÛÂ\x0013/Ýê\x0013\x000fSuîÊ*ÜË<ÃÎÀ\x0012ÿ0Zñu³;ôoª¿é)®z\x0001ÇÑ\x001eÄ1«d«ìÄ]mU\x0015©:'j\x0015N\x0014\x0015c©-\x000cê½Þó<î*|¾¥:\x0017j5.\x0014%)É±×ËÞÜS\x001d{â@QÙ´Su÷*«¹XÕLÌôdËqcÌ{ÚdT·²\x001aoU\x001d§¡iuò>g7_öì£Ùu~Á)ü\x0002zvO\x001dçFcìØ\x000fÜ\x0017\·\x0001b\x0003NÕÍ\x0004å\x000b×\x0002XÖ \x000e>Ü¸nY9Å²Â\x0018²MäØ3)cfH#\x001ey«\x00185¾Ø»èÿ¼à9ü?vñ¯h#âô\x0015º6$.3ñ°§Aù\x00127«W¼7«Wüã/\x000f¿þãï's\x00136\x0006NB×#kÃm`­GgÖÓåëú»«»gº4üº©ÐÕcþe²9°MCÈ©OÃzNÛrb;¹Ì)ÉÊ|\x0005¬dÖðxtËp«ÍN¸¯12ßy%Y&ÅÇj³Äm6·¨6;á-ÆÈBK\x0016td©.ú 6£\x0014²\x001eÄf\x0007Àb\x000b\x0016`+Øá;j\x0005\x0013Áþ²1T¥,)ÉdF\x001cnÍlåNNÞÇÈrKud9Pî{2\x0019%ÙîÈò/-WQrÙ©ê,Få\x0012uéýSY»ðf5¢úe´BÒµÉ\x0012-ÿÌµOÇl\x0006ý\x0001 <\x0001¨×}e´\x000c²3·21
´î\x0004\x0000Ý\x0011à(k&+´Ê¸\x000eM¶ÿL\x001bãêü?(\x000f\x0002<¿
\x0019uãX
UM¶ÿþ\x0018Cë\x000e\x0000Ð\x0000ÎdÙ\x0002F\x001aãY\x0016Ú^ùø0Zw\x0002ò\x0008(»ãp¡Q½½&\x0013göJ5Ñº3\x0000t³ÀZ£õ+\x0002u²\x0007\x001cOÐ\x001d\x0002 <\x0005pDDX¶'o\x0003©\x00124'®ÚchÝ)\x0000ºc ÚRS\x0015-ó\x0007uVj Ì;í\x0018Zw\x0010î$Àm\x0016«3ËÙ¹U'\x001aG³ÝI`u'³«0¡GdÎ¤»µÝI`u'\x0003]TÉ\x001c·¯ºe®ûTdýS@y\x00108Ã­ýÆzyàÜ²	Ò\x0001k»³ÀêÎ\x0002\x0007eùÍeiÛ#íN\x0002«<	\x001c?QL/r,Qä`]§âê\x0001«;\x0006µ\Ljè³N\x0006ã&i\x0007'r
chÝ1`ÇK¬Ñh¦y'V;â4ºSÀêNj\x001e\x001eimp\x00027\x001bmùG¶;\x0005¬ò\x0014\x0000\x0008-rÇ´\x000b¬ê`[Ð¡@ëN\x0001«<\x0005,eg4Þnù'òCh®;\x0005ò\x0014ðI®ÞÌíYh5!XØ\x000f\x0017¡uÇS\x001e\x0003Î°N½q\x001cÜ«Vã)·Î®\x0007,©ÐºsÀ)Ï JÆ\x0007Ò-SvÐ¶âÓ
´ÎÝ:¥»
QÐa}.\x0017Y¿Ã¹#\x001e×u\x001e×)=nõ\x0018Ô
h°]J\x000e\x0003ù G\x000e)×y\§ô¸!ò³88ÜÈC7;´Ô:ë\x001e×\x0005Öc1Å·²ÒDÒ\çpÒáÂ²Áõ®8ÏYÅÉNv¢Vf\x000c­s¸Népë\x0001J÷õ?â ÎËÙn÷:<GÑ|çp½ÒáFûö\x0000J]ÒQ Í	îÈ+ÊwîÖ+Ý-§R4
s)lV¸=àTâw\x000c­s·^énùÒh4ú¢©_·ÈãÓw·n¯¼uÓ$ÌNEçó¥\x001fì§ruch·õJo[\x000f&d{ò\x0004ØÀ½àu©\x001d¸ªùÎÛz¥·pÄ\x0017\x001f9ò¥Ãíµð\x000e£uîÖ+Ý-¶1çF<G´r|\x001eÙ»õJw<\x000bíèÅs\x00149	üïÜ­WºÛ`YYÍD\x0011{­\x001756ßÖ,£ÎÝ\x0006¥»MK&*&3«ë+
Ú\x0017{è\x001cnP:Üº+=\x001d\x00051¼}µ\½}<Ö9Ü t¸YZÑjôòÀ²fnGT[ÖyÜ ô¸M:êò¦Ã¥xêZ<°CCwõ\x000eÊ«wqïH\x001c·ªÛÏ)Äy>ë©<\x000c°\x000e!Õ\x00029ÜXíÀ9\x0015ºÃ (\x000f^\x00051¥1º\x0016Ä­\x001dÉ{î,\x0008Ê³ Y	v$n.(S©\x0012\x001bí[ë<nPzÜÊCBYfè\x0004-Ëç<°?cçp£Îázìt-ò=Yø[\x0006Ï×ïyà\x001a\x0019;\x001b\x000e7[ÙÓ&½tÃüÇ\Gì\x001cnÔ9\Ô'\x001dICzY¾>íØdÛ\x000f
®ÎÛF¥·EoÚIâ·\x001eRøglØyÛ¨ó¶\x001e\x000bK\:\x0012¡9I²û#YØyÛ¨-2	ré°³>6ÊAp$\x0010û"\x0013³õ(h\x0017oK\x0007»ãdö¡7AìmÔ9[oD\x0017W\x001a©&{+¹ìc³»yGÝÍÛCÔg]i4Ï{\x00160v'ÚoÆÈºc ê\x0001ìå8G½èR\x0005X=1ó?Ãh©;\x0007ò\x001c\x0000\x001eB·[²Xs\x0008\x001c\x0008
¥î\x0010HºC`\x001aeñùäÁþ3ÎÔ\x001d\x0002Iy\x0008XhNÏ£\x0015DÿÆ\x001fq¶©;\x0007î\x001cÀ¯	-)N4YMB·Á\x001dAëÎ¤<\x0007ìR9\x001a|P©5¬o\x0003\x0017ÈÔ\x0003Iw\x000eTïÅÊ&Ã+:¡$ËÂØmêÎ¤<\x0007l¨2Îä"Ç\x0011ÿ\x0019w´Ô×\x001a*\x0001B'ñLhåv$@ºc )\x0001g8Gã£~Éùø\x0013m`cdÝ1Ç\x0000J\x0012P$![Ù\x0002Ë}ãH|4w§@V\x0002.JUBâ®ñâè$\x001d2Zî\x000e¬<\x0008\x001cõiÏFã\x0018Gä1(ÇÖ\x0003Yy\x000eP¶s2çÇO^VÚ\x0001_»c +\x0001\x0014±f
¿O¢á\x0017¬rw\x000cdå1àã\x0012\x0017<\x0004\x0007Ô±ÑN´¡uÇ@V\x001e\x0003NæE¢Õx{&·¬´\x0003î6wî6+Ý­+,3_ÍÏ£9|$AØ(ÐúÚn¥»
F*õQ¸®\x001c9/wÛ\x0003¯¨ÜùÛ¬ô·Þò°n#ë<­Îr\x0000¬tî¶(ÝmpRÍ§'}Î²D8D KçnÒÝÎÉk6\x0019ùXîë¨Ñ:w[î6DI|â\x001cPÚ%Éö<R	Y:[þÖG©7Ì¥J}\x0016É¶x¤\x001e¸tþ¶(ým(\x0012IÈý\x000ffñiGÖ¹Û¢t·>K#A.ËI 1«¸§¤<Ö]»òÚ\x001d\x0003çÀÊøÁØÅÝ\x001eùÝIP'Au·´	
PÓiÝ\x00042µ*n'f+Èº (\x000f\x0002ìgæWTb}Ú`¼Ø7c.5h}ò @µ@ZjÅqQ<F`Øjáü`\x0002î(À¿Ô-ò¨jÒO+\x0001¤ 8\x0010\x0018cë[}ò0\x0008A.kEºCPbÙ\x000eÜ ïö*UvK¯ÈåÂe\x0013\x0001$\x001fµ\x0019é¤BëÛ}ò8\x0008"±okEÂjñ@\x000eô
ø:³e\x001egb§´\x0015\x0002,\x001aÁ\x0007WÐ·|â_êì&'\x0002*Â¦ÕQ\x000eô/Bßó©µ\x001aÍk\x0000#O½ £R\:\x0010W¾ë\x0013ÿR{X9f+ËaÅóÑ·jË*¶¾ãÇ(Ï\x0004T\x000ccýå$Ã^Y\x001c²²yýHëFöÔ7²ÿöþéÛ×§¯NÂM\x0003 ÜÚ¨É2±*\x0001Æ°vïº¿½¼}ÿîêöÝõÛ\x0000m\x000bhÕØ´ÜxyâL^böë¯\x0014¾\x0005ôj@\x000b<HNF5%Ö¶ïU\x0000Æ\x00160ê\x0001ã+.`³|~%#ù÷\x0013EÖ
¾Üòe5óò±x\x000chÍR\x0005¾{
\x0001®\x0007@ø²Þ#?üéô\x001cÎ\x0010I5§îÝzµ±\x0007¸õöÔö¸{ýã3[w=Á^Oá%¬$õ8Þ²¸¼áùÑ°\x001fÛ\x001aÃò-×`\x0005\x0019ö\x000bõÉE×¸h¹4ÝÃþ?\x0015Z¬ ÁÊ&Að,ö\x001eØj?J?\x0006\x0015[¨¨ZY®nP/¤Gû\x0013ÍIcT©¥J*SEN\x001fC\x0000¾µÅºÎ\x0019k¿öj\x000c+·XYµÞUí,4\x0006Åóð*\x000fû/¾1¬Òb\x0015
V1<¥
°7>¢ô¯x`ÕJ'tÂæòÂI6pÁ~QÇ\x0018í¸¬+s¯ Ú+¨\x0010{ï\x001f s[ ò[ÕAPª\x0000|ä:Í\x0018"\x0008×ùX\x0000@Á`6gÈ
\x0015k_2a«Û Ú¨~A¾Ë[.Ì2Á\x0010\x001dâ²Ý²·ªe_·#O~ñ°Ì°(Âµ¯e5ÆÕ-{«Zö%²R\x0002¸"£`\x0012OVõæÔ
ìY.·\x001eSídLõ¯ßé\x001fÿð§ûÈxsÿõëçöÝý/|úÛéÛXÝ\x001caFÑ­ÙI\x001eyÛ$Ëû
z3#¿{w7Á¿»|ûöúÛß½Ä\x001eZöp=Hå\x0007¾P)0\x0016a®ÍÔÌ#ð±á\x0003n4úïæ Dö,¿PÞõn?\x0000ZøtÜò1Ra4Î\¢'n}y,¡õs=·ìù¸áy·I¤ÉÜZÃ\x0014úúgÁ\x0016¾\x001c7|%æ)SRP¤¦.m\x001eÇç °zEÕs§E=|ýüéß>î7¥!=+\x0013\x0015nõõÛnlÞ\x000fUþöêÝÝÞ<3ãàl\x000bgõp¦XG\x0016ám¿ÄhÍµlNÉ\x0016Æqâ]Z';Ð\x001eó-×\x001a®n{'zS\x0014öÙÈWÝ\x001bº©\x000b-\PÂÅYÍoêÉ_
FZ1a¿j\x0018.¶pQûY­4E\x0000°\x001cÏ¢\x0007wÌn©EKJ´\x0004¢\x0000á\x001d\x000b"\x0006\x0010ÙA\x001c\x0014z\x0004.·pYûQ
\x0007¡
$n^ÏIQkÜ¿â
²5.ôqFk9©ºsÛ\x0002HM,¬u*áz\x0007¬õÀõñÅÍÜKTµKù!'\x0007\x0003­ËAÄÄP!LçVÖý+ò(]çå@ëæ²\x0015¹\x0016\x001f^y¢³Ò	oOxGé:O\x0002ZW#"ÅføÙv"Uq¶[g\x0018Âa¨WÇ_\x001f9\x0019\x000c\x0017íBJ¤Ý[P\x001an³(\x0011½¹\ý\x0012kaÜ K´ôm=Þ\x001dß=¸ ÜãpP\x0015K\k\x0008GÓ\x001aæÓÓ×\x001f¾=~üxÿí/'¿[v¶peV\x000eaª\x001f{\x0015LäQ)Él\x0004Ù+ÕÛw\x0017?¼¿¾¹¹|ÿÛÓ\x001f.®ã¢$<ÎçÂôÝ\x000fGIÌ#ìë+Äg6ÅêZ@×\x0002:5`ð,C4Ò~dO
2- o\x0001½\x001eP¤wª5ç6x\x0004ä)n\x001c-`h\x0001\x001a°ºÉ$Ê\x0019L2¼3J);O\x001f\x0015`l\x0001£\x001eÐpã\Àk0\x0019Vþ+±jÀÔ\x0002&5`ò\ÅcC­õ\x0013\x0017^Û\x0019"Z¾Üòe-ß4Ñ.|\x001f#Q(¸:M\x000b\x0016°´EoÀÀ\x0005ä\x0019KÛ3\x00190±\x00057E\x0005J>è½´ÞM§¹b\x0010\x0001±n*ò\x0017f7èóNlcpý°ò°~óñã§§¯Ï\x0006;©\x000b\x0017²\[båIïÖO777on¯Þ½\x0004c[\x0018;
\x0013%°ß\x0002û)	Ìº·o\x0010Æµ0n\x0014ÆMOøÉ2Eð£Ô{¿.t\x001bñ-\x001fIüÎ$¢ª1q_wëk÷ Llaâ(Læ:Øê
^q)ä\x00136ã-\x0007YrËÇXbuL\x0014sây\|fÕ+¿ix%®÷xþéþãÇoÏNH8ÈR"a¹¬®®b?]ÞÜ¼fÞ4ÁØ\x0016ÆÂ2\x0007$\x001e\x000cW¢H	n÷Ò oaü(L ¹O\x0015ÆÎwT«³[×'\x000fÂÄ\x0016&\x000eÂ¤À©	Àp	²~íºj\x0010&µ0i\x0010&'ÉZ-\x0013¹[,FnåôöôAÜÂäQ\x0018#\x0017qõª#ï7S\x0017\x0007aJ\x000bSÆ`¢ÅÅ¨f"1sK·ëdý\x0018L\x0013Ë\x001cä\x0017MSD:\x0017kR¸'Y)ÿÈÊEÖ¿$¿\x001e\x001f>~¸xøñüÇ×ßêÏhø<³)uoQ	\zgã:-øÓõÕÝÝÕÅÕ;L
^_]¼~_¾ÄéZNw\x0016g4Sh\x0017AcbÄÒ6¬KRÏÂô-¦?\x0007\x0013ÇEÌ\x001dÌ&×S
ñl¦è\x001bukÌY¡å\x000cç3ðÔäÃþØ>·\x001b}£³@S\x000bÎ\x0002­\x0017¹²±\x0002kI¸â8º¿~ÛÅ[Î|ÖÏ¬f2ª\x0017ÓO\x001cw\x0005·ï\x0005ZZÐrA¥ýßT¼)Uýj\x001aÀ\x0006Ý¨\x0004\x0003
½g:Ï5A|UÂLj¨\x001eÖë\x0011µ\x001cÀY¤oó\x0013xïGøã\x000cwÄÁúu¦\x0004µ³%õù¥²>\x001eC^¬åÊ`<zæ\x000eÇ
)õ(;sèÞV¾ÛÓ#È	Ç¶8v\x0014Ç%NÖá¬Åù.³çB`\x001f·:c8®Åq£8!òÕÒZG·¹\x0013÷Õ\x0004\x000cÚã[\x001c?lÈïi\x001b2\x00109KíH°ÛI\x000ec8¡Å	£8ÆQuÜ¬3p\x001fH­üô\x0018Mliâ°q¤ °:ýé·ÝÒ	v+0Z4C7è!POz¢±RF¶	Ê1ÜÒäaã\x0000·Ì[}ÅOY\x001cå}\x001eNiqÊ NÆÀ\x0010HøcV\x0002Ì©Èc6mE
pû7:A3Ê
ñÄMjóÆZBCy;Åk\x000c§÷ÉãN¹ptÈzN ×¯ÅmçÁ·Í¡óÉ0êsÉ¼Ïi*Ò\x0018Î{VCiÎ'Ã¨SbÄT\x000bU
eg¿<§×\x0003lKaÇx:§\x000c£^9ã]Rwõjghñpan0ÛvÚ1Î)Ã¨W®`ñ\x001a+:Õ\x0019\x0013Ä³Íòtn\x0019Fýr^\x0014Ñ/ÓÔ¤tÍn%1Æx:¿\x000c£¹\x001eßÓ5g*¥ó²|
Gh¶õÊc4_aÇl\x000c\x0007"pÊ¡#Çl¸Ç"x¦u:Ç\x000cÃÙó°dÀ	Ä\x001c·²\x001dñ!\x001eÛyf;ê\x000bí¬é²OSàg}Èg.\x001dÛùe;ê³\x0005Y:ÑÐÌædø\x0008~[#=ÓßÇýräyµ8è\x001cO6üH\x000fe;kf§sÌvØ1Ì¾±ÙS¥ÚÇóÚëØý(Oçí°cös²\x0013yê\x0015¬ÐZö²|ÒÐvÙ\x000eß!q±µúXëçêáuc<g¶Ãj¬¦õ\x0013¨¨8'iä\x000e%¹;Ïl=³³ÜââÌ|Æ#å.ÕÏÝ_o¶£¾\x0019}!ÕñáX§\x0010yýÐz°U\x0017\x0019ãé|³\x001döÍ(=¯gõJ´3¯çsßÆ®sÍnüÒ\x001c9jí°Â;1\x000e\x001d¤(p\x001eOçÝð­¹\x001e¥$ÞæItk\x0006ïÙ<ÛÖ1Î=»a÷\ÏsJÊcH|Ñ°Ì\x0013Ï[Î®sn8z\x0000aq?,ð¥Ú-sq:ïãßëPäæcy¾\x001cFäÞ|æ×ê6»\x001b¾Uçl[üâù°@IÉó\x000e÷ßÿòøeuÀãüÿ|Æ§
VR`ý'¸j»bÚ¾ã§÷O\x000f\x0017_>}ûrññáâîÓx)\x0017º¨Õ«^!u´\x001cYO Ä\x0013ÃXº¹¼¾½ºxûæýÛ«»7¯_Âµ-®=\x00137;Ì¦ãdd\x0008i¿·COë[Z.­³e
P`ö\x0004ÏC(þdÙØ²Æs\x0017\x0002¶Ê$ÂÍlÚ`èSqónK\x001e7·¸ù\Üº­ææÀºn
e³rp$HTq7µçá¶q2»ê!Ðð\x0016®,¬ÿ;ºYs\x0004Ï¼qF¨7¯3ÙÙ´É
ñîóý_\x001f>y8é¬+EúX||ÅJø¢»³éY¬®ªþïÞ]þ|u÷öê´ÇÊë
ælÚDÇ\x0008\x001a
ÎótIÔÏåù\x0001n\x0019{\x000cÎµpN\x000fÇK\x000fµw^ö÷h\x0005oá¼\x0012\x000e²´uÕóÚT\x0017É3³\x0017\x001bPÀ\x0016.há\ÓDdÀ-6;sVUd±%J2çe\x00142F3X¥9,­z³F\x0005Z¸¤5Û2Ç®>¸¨ÅKd×m+up¹ËJ8\x000f\x001cMÀ®.î#LÜrfw_Ë
¸ÒÂ\x0015%-"T\x001bÌ+Vyùbv/D?ÎÖ\x001c\x0017è~Öraò>5xÍ
2~Óñ®ëÏ\x0006åáÍÀ\x0003\x001d·û´\x000cÝ6Ä©è:\x000f\x000cZ\x0017Ós\x001d6¢Ív+@¬¢ë¼\x001chÝ\x001c\x0016«QW\x0017¦\x001a¤ÑQè¶ºg*ºÎÖDÇÐBâéÈõïbÕ8·\x001dL¢ëö+h7lB\x0007	¬¡¸(mïÑ\x001a:Ûm
«Ý\x0014	8Tzl4*<è°º½XÁ\x0010Ýº ¦+íîþ?\x001eORe¨KbÙÚ¹h>(ñÊ7Iì÷\x0017wÿrý"mqì Ã§ÙÌ}]øü!¸iò\x001ddq-\x001b5Í²\x0013SIsR«F*HKm+ã\x0010oqü(Î(ÉSX\x0019KAú¡6S,¡e	£,X!8Û)Ù\x000f`o\x000cj,v§³r\x0008'¶8qx\x0011GV\x0001ÍØèI_*DÆß NjqÒ(N ir\x0003:h§rÃ Mniòð2\x000e¼¥\x0012\x0016ôfnFdMÂf¦´4e\x0006ï-¤\x0007(Ç}i%ÊÝé<\x001cÁi¯SM\x0007ÿÖÀýÊucÏ\x0005¸É¹*Mù× Oïýqr\Ñ°ñ\x0011fÌ\x000f9oB¦<?Q\Ot\x000e¸§Hù©Y>Û&¸!Î%Ã°OÆîÉ<i®úÄÎÊ×¹lêT\x0006y:\x000cÃNÙi0\x0015ò$3ËÛT\x001eÃ·µâ6Ê<_aÇì¥!$á«ìãÅ1ÍÄ AÎ1Ã°g6õ\x001dð\x000cí#GúFGu§ó0ê\x000cíÒJàÞûzÃàï\x0015wÚbç)ë`Z1}ýîÓ/ÿøûßþñÿ~>YÌ\oÃÅÌ	Eæ´_áX&í+\x0011Þ½ùîêwWw§ËË:VL\x001fQ\x001fr&ÙD]r9\x0007mPoh»\x0001ÔQ8×Â9µå,µ\x0011ä$a#×ú\x0018Ô{=\x0000ç[8åædÒT±5Y¹qi7	1
\x0017Z¸påæ(~\x0002\x001ebW
Ç7ÆoÔÏTl±eZ6ÇâßõÚI´\x0006ÓªüUw\x001eÁ\x001a¸ÔÂ%-\x001c¶«Ïé¹é®Ë\x001cQ3'$|Gár\x000bµp§+U¸Ì	rÙ
v[[¯A+-ZQ/¸@E\x0015
^Ñ7ÜRj`?#7ÈÖÜÿYe_Fàêco¾\x0007V8/\x000e¾ÈG=\x0004×\x000eÊã!¡RØ|ë©7Ó@=ÿ¹HèÀì\x0019hèºã\x0001Ôç\x0003æ\x0003y?ð÷\x0012Oü0Ö\x001cYtÐ\x000f < ªíÐaWê¼!åtZ)ûúW£tÝ\x0001\x0001ê\x0013"\x0005ÊRÇl9óYF\x0004÷Än*u\x0014®; @BpGA5ÔFå(«nÖÐÀu'\x0004¨ÿ\Ëu'\x0004¨\x0008\x0014Ä§
Ë\x0012OèM¨I¼.ºc[¢;"@}Füç®;$@}J\x0004:÷ëm\x000e¸ßÈ'²[Ü\x0016\x000c)Ðlç­úÚfs%AL2ÃõVBÕ^¡¢ïêüÒuÎªoÂ±á,PÞ sB¨Zn£*¦bë<U{ú\x0016µ´ä¼[	Ð³4\x000cG®L¶Û­V»[s)$µjPÏØñ\x0001Æ5©S±ë\x0011ÛuUa³ýª°áS¶ð¦õÀ7âé
\x0010JÚ\x001f±1|#^3&5bb
ÝéÖ>ÞÀÖ,ös\x001f±ë^ÜÒõâÞ}úð§û/_>.­«ÿ\x0017YÈÑYCÕ*XÁ.
!;¡»7¯¼|ûöÍ3õueÝ[º¶Ü\x0001²\x000c|y\x0002µ¤sz\x001eàÉÆq.×r9ÅêðThë,Ï*^*[ãö£Aó-×\x000c»éØÏE*%q\x000e2íÌ@
YhÉòc&nuø\x000eK\x0006P#}ÏØ¢E\x001dKRÈ]1en\x000bKù{\x001eAk__}è\x0008[,Ü¹Â~Á\x001bîÌ°W;¶®~-¶÷\x001bÏ¤kë2»I\.¨@\x0018çW¾-Ô¡\x0019lØkS¿{ó\¢¶¬ë[íÝÅó@eêNG Ë\x0003\x001a*\x0010WÚ°-»\x001c\x0004r-\x001b\x0006ªç#\x000bYéU·|\x0017ök!ß\x0002ùq ?N\x0011\x0008ç=\x0001\x0015\x0006Û±<@¡\x0005
Ã@6ÎåM3\x0010LÛ\x0000í\x0014
\x0001Å\x0016(\x0003Ù¹o4ã	V¦°PÞ«¢\x001bâI-O\x001aåñ%Îq>4\x0010~õBm\x0018(mï@¹\x0005ÊÃ\x0006e×\x0007 I\x0019;\x0016¶Ð&2
TZ 2l¡ìfé\x0018ÜdÄ¢²5öÝöË<­Ç¶+ý¬cQh!GQ<k\x0018h¯¥c\x0008¨÷ÓÃ\x001aË¹húÅæG\x0019D\x0012\x0001
õÛ¹¦¡óÓ0ì¨}*sI
n2Ï=AÀRõÕD{%¾CD£aOí«{6³Rq\R\x000eË¾ßQ\x000e\x0013u\x001a]5ÖEöE ?¨sÕ0ì«]ö³Çl£ù03<Q¥h÷\x000e2ÀÓyj\x0018vÕÞY¢\x0019ï\x001f.lõ&RØBa¯Ñv¨óÕ0ì¬Q¿Ì{²Ä\x000c+åT\x0013m³YD³aoD£ñ|G3ÁËÞ?×D³aoíü¬"&ÊÒ»a¬\x0013\x0013íuú\x0010ÙÎ]ÛawïÀËº°¼áÂ±j¢p¦{´¿¶ÃþzR\x001d g\x0003EÑ*\x001bÕUW\x001bmó@DýÅzØaOÚl\x0014ù6µÈó\x0011rîWëÜ£\x001dv®\x001e²ÁÉWeØRI\x0010h¯öüY¢z§ê_CxÉ¢ööþñéëùþÓÓýiÝ^W\x00027Jj$±æeÆÉfäüÛËëÛw\x0017ß¿¹½<©ÝËL®er\x001a¦ù%;Í}ËÒé-43Ôæ¤U@\x0016*Cùúí\x000céø\x0002ðHro@­W\x0002*¶PQa©ºÓHO\x001fxñÓ.¯ÕP\x0015P©J
KQ;\x001eBYÃ\x0003¼Ì\x001b*ka\x0005Si©>ÙHø¸º\x0005\x001aë½\x001d/ë\x0007À8\x0014ô{O±ù¼$1\x0001Ü<ñ\x001e©´ÛõS[AÕí>Pl?¼VFRwssÖDeNéZSKAÕm?Ðì?»È\x001dºBÑüâ¥dÑuOª[ê Yëõ³\x0015éê¦÷ÁDe4ïY®Ê®}ºm*ÿ'®«/ÿöùñ4\x0018ö"P5KAE\x0005Ús2Ð¦zÜ\x0019íêíOw×/²ÙÍ*Ùò2\x00142·L\x0018\x0011Òt°\x0011¿ÑÁ¹\x0016Î©à&)Lê³1ñå\x0013o\3\x001cäÍø%\x001doá¼Òr>âl½Ò¦$®\x0003µy§"^\x0003\x0017Z¸ ´\x001cö`sð"ùÄ"\x00156+:¶Ø²E\x001d[Á\x0002ãEÕ²g8»3wFÃ[¶¬e3©7°Ì\x0005T\x001b\x0012mÚ\x000cCW±-\x0011¡É\x0018%\x001cmP\x0003ËÀw1»3ÅV\x0003×ù\x0011Ð9I¿ÏÎN.çBJæ9\x0005'²Æ;ãzÆèÂÚ\x0003þVýÃÃ§Ï|æª\x001f«±æö\x000c3i}Y\x0012à.#\x0008ë:Ìë«7w?<wÝ\x000fk÷+]X`\x0001HÄ è\x0017)ùÄ\x0019#Hë¤©
Ìµ`N\x00055å\x0004\x0006@#eë6à\x001aîÍxO\x0015o¹¼ËÑ EëïHùËs0"B\GT\¡å
\x001a.\x001cEC'|6eN¯y\x001c\x0010Å+Ì¯µT`±\x0005º¥_¦\x0006Ébä|ëE¹Ö\x0019f\x0015Vj±Ê^qÎwOëË°D\x000bIìµ\x0016=Vå\x0016,ë>d¤VþIïÞ\x0003H¾qÄý;ä XiÁ
¬þãùC4=4ÑbnÙë.\x000f
X{.-]£¾ÂÈ·\x001cH©&ãç\x001c#\x0012z·¯òû¡>æNj3Ç~RØ ­S_*²ÎïÎñ×cÈÍ²¬/sÑ­Yg\x000bTdã\x0007ç\x000f(\x0015ÈfV2Î2aæ Í:×\x000fJß\x000fÔFmr\x0001Ê\x001exÏ¯;\x000bëY)*°Î÷ÎùcN¿\x0003CVMfSéÉ:/\x000b:7[ßé6s¬UçäTëbJ\x0015XçÌ@éÍ\x0002?©·
,Q\x0011÷Éi;au>£L4\x0003\x0005»©ÀÁE	\x000fùÈÎ´ÝÎ´ºY\x00162ô\x00193XáÎ}kÖÏ¦A°¸¾]ÇþvýããÇûÇgJ\x0012]ýÇ³ÀL}\x0007$ãg°ûwÅ\x001f¯o.¯OW$2m¹¬«^®Y\x0006
µ³y\x0006H\x0006Åý ñ kÁ
Ì\x0015\x0001+% \zÚ\x000cù\x0016Ìk-\x0006$xS¸Ñ¯Z}¿ë\x001e\x0018\x0015XhÁÎbNädê\x0005§daÙ\x0001Yl]=¬\x0002-XÔE:-\x00010LÒó=Ömb@*°Ô%\x0015õ<\x0001fJ%Å],¶ëÆ\x0006ÁJ\x000bVt`uÀ\x0005ë7]^G¦4`Ð»1\x001f³Àÿ`\x001dK-áÿµ*ð\x0018\x0017¬Zë\x001fôîu\x001eÉt
k$
O\x0016r,ß\x0015mAG»[rÄô\x0012m©¬*úW\x0014iÏMU¿L;]··h¨\KåT¶*¯(SÝ\x0017Ï­+©ö¯;cT¾¥ò*[%óA4À×ód2"ú4\x0015[¬¨ÁJU'¬¡\x0001ê8×O!\x001fÖ\x001a¬Òb\x0015µ¨q
&VCêYtÍýÌÒ\x0010\x0015ô»Pµ
ëG¤3\x000e¡ÁÑs{æü\x0015\x000fÝ\x0007Õy.\x0018B®L#w
.uæÚ\x000f<q+¨V\x0017°Èº\x0005Çi¥(1~¿.¾\x0005kg
½3ýùñéÃÃÓ3SÝ<õßÈqÕµ(¿í\x0007\¾¾}}u{:D
°ö§ÐûÓÁÒ\UKÅz\x0015íU¯f»»q\x0010Ìµ`N\x0005f\V£¸ú9Xßl»ÏA°Ð\x0005\x001dX\x0014­ÒdæLMåâï<\x001cáJ-WÒqeê`¬\¥\x000f«3åÛ½ß¿H¼\x0008æÖkßukÿá¿¼~øðøñôôõJ\x001dî%\x0015ÑdÝÌaÀ®.^_½¾¾yfSºõÚwÝÚ\x0019¬Z,\x0008\x0017
¸\x00179\x001d\x001b×CÌTX®År*¬z*\x0018{ÉÜ\x000cÝY\x000byoù\x0016Ìë>d4`½}¯XzmZØ«ÀB\x000b\x00164`®$Ò2â¬«	§ïn\x0006×¨Àb\x000b\x0016u\x0016W©/4P\x0007\x0005¡yå§ÝCr+µ\Ig0 ùCST®æ1Î¦Ýcr\x0014,·`Y·öE ½\x0014£ì-O`·i×ë\x000f5Ù\x0006tbFg²Â!ÍRò=k$yñoÚUd\x0017\x0003\x001bÃêMCÂ­8¦V\x0019\x0004\x000ePçõHZ\x0015Yç/@å0\Ý´
E\x000eë*ìÈòîkíe°u^\x001eBW\x0019õí4R[V^w'·Ò\x001b~}\x0004(YX-ðþe\x001cÛâØQzç¢r\x0017¦ÑÔ@5îõ»Wõ1\x0000ãZ\x00187\x000c\x0013çá\x000fhÀb/õ2QØ6~¯@f\x0000Ç·8~\x0018§Ì%¤³q¨Þç ¢qÎ	-L\x0018\x0014ê­Ø¦PS\x000b\x0000mö
\x0006pb\x0013GmóÙxáxêFÎ¦Ðí¸\x001ag·èe\x0000'µ8iÔ:Þ¼¢/\x0015,7"÷L³®\x001f\x001fÉ-LV|ªfÝPÕ#p=tµÍ¦Qc\x0010§´8e\x0014'Â<ºâDÃ)'`©áúß
{åz/ã´§Yèkºå±E\Næ<+8Ê3Uëì¢\x000eát\x000e\x0010F= öB¥ec\x0019î¢¹\x0014è·*C<ÓQ¯BãÌ\x0013\x001c\x00150B*lí\x0000AnÃèF¯ÿìùU«Çså\x0011ÄÝ";¨/à¬ónÐäÝþúøôÜEÃpHØHÛ¼^4X ÕmóZõqù"mIì Q=Ðå+\x000fG-ü¶:}\x0004Åµ(n\x001cÝÑq¶O
7ÝfÆé\x0018oIü\x0018I=¾3Ðc\x0019:_·XËÓÙó\x0012Z0â(\x0018lKçw\x000f\x001bÅ¬«YÇHbK\x0012\x0007$*RÝ]æNæ\x0002Ûæ\x0011Ô¢¤1£HíÍ4J_\x0010Ü^­²}A ä\x0016%\x000f¢\x0014VêF
=a@üþÛé9\x0019A)-J\x0019CÁã¶2HØÊ\x0007î\x0003°;ù¯\x0001öpÍSï\x0005\x0016ÏÃ\x0003ëñA7ÊÂõº¶¬5^ÆXz_;æl½³$\x001b\Y¬hå\x0013mc\x0007#,·1w+\x0004fªg"É»º\¸\x0002d\x001b\x001a!é-y[\-n!á\x0006<iK:\x0013¥ó¶0æn±\x0017Ép\x000ceé\x0005\x000c^B\x0015ë$c,»AKå_Y$ë¾Ì3²y­<ÆÒy9\x0018tsÞÐ,)¶dyî\x0013W²êí×\x0017Ü>÷\x001fþòøô|~\x001d#\\x0014Sª\x0011wJ5¦M\x000bp½C]ýöúöù\x0004{^ß^rûì\x0019Ë\x0015
Û\x0018\x001c,í¸ §[CØßU`¹\x0016Ë)°¦\x0008\x001cÅ¹pº"÷\x0002ób»¹Eh°|å5ÖJ\x0008¹\x001eéd¬,ýXgÙÊ®k$¬éVÖÓý×o/¾ûôôôxÿù×p\x0001¬ôOcþrU1JNhg\x000eÇÛ«ÛËwWïï.¾{s{{}y÷ýK¶Å´ç`bý6\x001do1I®/JýÛ:éZLw\x000e&²ãËcf\x0007²Ì\x0015pf¯ÝHé[L\x0016&\x0017­U?\x0017é]_BÉ\x0012Üßë\x0011Ôb\x00163\x0019T"\x0019§¦Ãù\x0012±\x0013_Ô"Æ\x00161eÉH-\x0006SRöÒ\ö\x0002\x0012ZÈÔB¦s Q0_ØtC5><>Ó¦a\x0017
ÊuHÛ~ÐÄ»û§§ÏÏ=t¬Ü]«ô|ÊÉdÔíôI¡óÝåííÕÝõ3Nr\x001dÞ¶¡\x001f31V¦sdBs$TÈ\ä6\x0015?:4×¢9\x001dZZ\x001eBu\x0013Gº8\x0019nsi_\x0007{\x0014Í·h^iµ,3å0]Ç1\x000e,ÄýÜ£h¡E\x000bJ«\x0016f}Uó;É-s\x000c·[V\x0016[´¨´\x001a§1àK\x0003¬«Õ\x000c?²·â*\x001a²Ô%¥Ñ\x001cÇ¬\x0000<g\çÿ¶m[VZ´¢C\x000b§¡B}kÎóBK° mTÍ\x0014hÐ»5¥_óéâØÈ¥áVö\x0007r¢u¾\x0003ÎÃ%\x001az1idÐ\x0013ÝBÆ:í:JÖgAjn¥ïþô¿ß}î\x0002\x001f¼hdTez\x0016¹¢Ìéú¤z÷ãÕå»çnÊi}\x0008¤æ
:À\x0014^qsy%cOEwe3ÇgÈµDNC$Wv°K¨§ÈÄÎ²®þ\x0019gò-×0\x0001Ç*q=qUx\x0008oÖ¢9ãL¡e

&¹p\x0011ð2ÎßNvßön6H\x0014[¢¨!
\T\x0000ÞL]\x0010Ó_.\x001f6;×ÅA¤Ô"%\x001d|8 õ<Dâ\x000bÎNþs\x0010)·HYÑ\x0005Úr>²ö¸Ob&Øy\x000e2©hÌDP4@L\x0006ùt;©¾1¦&ÜÞÒ( ¥^\x0000¢[f¨ó|Ñút?×9AïÂ5>\x001c·?}<¤EZ\x000cµón\x001bdê\x001c&(<&fÿ,-r\x001c¬I_\x000f8âmÞ¦"\x0007¡:_\x0000\x001ag`,ó\x0014¹sÌ»$
!\x001b%ï¡Ü:,äVSÿÞ}Â\x0017ãçoÏFAÓ+\x000e\x000e\x0007>ñ2ÈkñÄ5ô
>\x0016ë½\x0008g[8««0kÆbÅ°}\x0008,od·\x0007²\x0012ÏµxNk»z\x000e: \x0017ªªÖ\x000b\x001cYÏ!»J<ßây­õ"ð\x001cNã-_\x001d"wû88qï\x001b¦\x000b-]P\x001b/J\x000fßf|`[1Þ¦PI\x0017[¼¨6²þºEÛÊ8ã`«t¯ÃK-^ÒZ\x000fµX\x000c¸ë-¦-'â\x0001Ãx¹ÅËjëÅi&!U`xîfAv§\x0014ã\x0016¯h­¼t¹@äÖ\x0008Kúô\x0018]sÊ»õ\x001cÀ\x0011ë¥Àg\x0006£¢Ü³\x0014Äxû¯Üa¼þÄP\x001f\x0019ÙÈÖÄ7\x0011^>}Öòu^\x0019Ôn9;9Ä¢\x0001
ã%!}"è3×ù=P;¾¥/ÇZîn¯g\x0014\x0012·ó, v-eg3á\x0005\x001f\x0007o¥$æDxv®Û¹ Ýº\x0008']
g#Càòvgö\x0007\x0001\x000fóÙnsXíæ\x0008 ³å\x000bmË¹±\x0015Þ×ñuÃj7G\x0008\x001b
H]­àÄ¹\x0008¡
óu»ÃjwGÀ=æË\!\x0010¥}ÁÙ\x0016¨¯Û\x001dV»;°ý6Q ^\x0011èÎ×lnáUòuûÃª÷G²R\x0002SQ]á>\NJº­\x001e½ÏuûÃ©÷GÊ¤\x001f6µK&ÊOI³äZÖL½;Ú\x0019r´Cú!r#ÎrÞ þ-\G\x0014\x0004çí¦Á`\x0018sÝ¥è¤KñÝçû¿>|þòøì|»µ¾¤,\x0010x\x0000BÝ\x001f|ºyp+´ww?_Ý½½~fº\x001dSÙÊj¨b¡>-\x0000Ç\x0002uÕ\x0001Sá¿ñ¹T®¥r\x001aª¸ÇzÒ¦µ\x0016¥\x0005¶¬WÊ·T^CUw¨eª@S\x0014ñvÇ{ ¬¯w
ªÐR\x0005
UñKhÐH¼Ìte}î+¨bK\x0015U¶¯xYYêËËY¿¹§+rËU«ªL\x0007Hk\x0015b\x0014mý|\x0006ÔºHËå>ZòóÃãÇÿøûi¬X/\x001eÓ°ë¡báê1\x0017×B(³ÏúùêúææêE2ßy\x001dµKB1°ìxZê½SÚM(\x000eÅ,êÈ¼\x0003A\x0006d½È´ï\x0007p\x0006ÉRK_³° \x0013.2µOFÞÛî\x0017
YnÉ²Òfi\x001e6\x0007ìic²K^c?Ý?FÖ>ýòêé7°Ð\x0012?LÁ[\x000e\x0017&ðqûÝ»ã ZèÐÒjôxlÓ£/ÙEyÿÀ\x0016n¡r¥QÑ\x0015BMV\x0015+q¬\x001cÎ\fe}Ë)íÔË\x001f~½zI/p\x0017\ps·ÚºýA?_Ý~yû\x001fÙ\x0016ÌjÁ"KçW¬åÊºÖoG\+¸\Ëå4\8\x000c&\x0001ÀÍÕÙ;)NÛª8Ìå[.¯ãr¬zÃÁ-é\x0005Ë$\x001aë·3£\x0015`¡\x0005\x000b*0(<sE\x001eµæt
iKÃT±¥**ë©Ëdªj¦Öfï¹Äµ,
,µ`I\x0005\x0016¦ö(ýåÙ'ÑãÝÖ+¸rË5\	\x000b1	\x000cSYóº\x000f.s4-®{÷U`¥\x0005+*Õn!\x000fV]«#°%³¶7ól«
0npæÅ Px´~ÊÈRì!dI¼\x001càê=¾Êå×/I\x001a7æUô\x0019eäEÞÅ8Õù{P9üýM¬
dY#g£Û½9ßÃX»\x0007¿G,Ã#s2Ýl$3ºÉ¼kÀ:\x000f*½ã¤v^L\x001e *Jy-C­"ë\x001c>¨<~ò,!6)£Ì.,\x001aé*Ø\x0016ähÀ:\x000f*§²§pSýnªG2\x001fyñM#¬sú òú)\x0001×R`v«©Øf°7|¬sû òû8\x0015f¤\x0019ÅAdr 98â÷¡óû rü8tdR§âÙaÄ õ³vo:ñ(í<¿Uyþ'7aé\x0002
=
\x0012yÚ\x0008mªÈ:ßoU¾?[ÃQMã
Má\x001b7ß\x0014\x0014jÀúÛ¾Êûçì¤c*ZÒyÊIäÃ¦èJ\x0003Öù«òÿÙEIaW¿6{Ùå©ë6R®*°Îÿ[ÿÏEêÔ\x000cúÿYì?e1Y:rµ¶ÿ·*ÿ³Q\x0006^ñ§ÌRü¸
ê+À:ÿoUþ¿Ló¾ÀäÀWE\x00144bms^#d~=ÏËd¾\x001f?|ýôùâ·÷ß>?||&üjd«ãAÑÉãm3¹äçë×ïÞÜ]üöòýÝÕÍK`¶\x0005³*0{\x0007\x0005æê`\x0017r\x0000Ìµ`N\x0005\x0016\x0003),cö+7\x001cÈ\x001d#Û\x0003\¾åò:Å%í¦¢ºÉ`Y\x000e¥µz
,´`A·Ä"W\x001b`ÕmädLW\\x000fbVqÅ+ê\x000cV(n1å)\x0003EQÔwë:\x0003\x0015XjÁÎ`{`çúè9\x0000åÖ2¸*¬Übe\x0015Vq¯¸«Ïp3G"Ïëó\x0001¬Òb\x0015­µD
ÈpsZ\x0014\x0001\x0011·®äÖp5¯p¿\x000c+\x001c\x0003Æ*Ã$óÏu\x0018Rcî;BÖû|¥ÓSÆ{2ôåD\x001fä·?@Ö9}PyýXOíÂí_kkªÍøÎxWè¼>èÜ~\x0006¹Ysò;HêÔ¯³H*¬ÎéÊëÇúfs<q;à^Û¼®\x0012Uu^\x001ftn¿Þ«­\x0015Q¸\x000c$:ñ\x0017GlÖù}P9þÉfÞÆfÒc¸tªÈ:Ç\x000f:ÏO±ÉfÓ[ÕfìËÂ³\x0012:ß\x000f*çß®3«B·,SÔóz(¬sÿ óÿ¥s\x0019T«ÚK)\x001fø¶;\x0000¬ò\x0000B·©à
y¤5¹À\x0013Óvþßêü	ìÿÁÊA\x0002Á¼V¡Qõw~¥ûçÑS¶>±ÅxÀ7ëQ\x0015Y·3­ng,FõN©ÜÅ\x0018+ÙZ\x001fWEÖíL«Û\x0000¬Î\x0005M¹gáÃÜÃZ\x000eBCæºõïtë\x001fâ+Cd1r]Â \x0008µi¹\x0003\x001bÀu§¦Óà¤Ë\x001c\x0007\x0014PR°6â*¬îÈtª#3ÄqH\x001c­+³ý\x000b£ëV¿S­þ\x0008/?òÔ÷1qÕ[§nT`ów*ç\x001fÁD\x0014@ö,·\x001f15BMwëZl
ï|¬WùØéö¤\x001c«¹ºÁÃgï.²^uÅ¹«Ç\x000bÍÓ®d±/\x001f×ùg\x0015Y·ü½nù×Åü-m½QÝp´ß(PuËßë¿M\ÏiëAîÈd¼ÆòºðBÅÕ­~¯[ýØ\B\gVIqÛF9@C\x0016ºÕ\x001ft«\x001f
åì+Y}\x0014"ãºÎMI
¬[ýA¹úEÊÆ\x0006à§oq\x0013Á¬Ë´Td}L·úr,e*¼--\x001dqþ¦/b\3?\x001a3p¬åqÏÂSÉ¸çy§æZbÄ§®ìñOÏÄÕ'Ç9¯\x001a£·ÂêËõÍ³¾þáö¹ úZaÄ§®ì\x0005$¬ïÅ\x0014ñ:Kêü\\x0007\x0018êq/4DäZ"7N\x0014\x000ce¸\x000cÖÒ9)h¥×êNßË×\x000c!ù\x0016É#9;Ké\x0018ôa4ú\x0002¨¢§Þµ7ê\x000bÃ@¡\x0005
ã@Ù\x0005	³
,\x0015jv$®Fb\x0014\x0015-Ñ
¢\x001a)L±é³y±ÒF,t\x0018)µHi\x0018)\x0004¢bRâ\x0000fÏï3Ø¶$\x0012å(+dÉ-Õ\x000bÌ\x0010°<a!N\x0007ìH¥E*ãFÊsN\x0014TW\x0015\x0015:9	É]ë°\x000f#µáèÔ\x0017½ÀzÖ³R½[yÃÙÂ7\x0005\x0013×i¾q¦ÎOÂ¸£\x000c.¾
d'7\x0007WÑN¢\x0008iÒf\x001aÅ0Sç)aÜUbåÜ@6¹'s+`EÝuÛÈ0ÊÔ¹J\x0018÷¸æ~¿j\x0011î¼ªëÌDÆ(Sç-aÜ]â4\x0013ªMË	x°IH×øv\x0006Í0Sç.aÜ_F,\x0012\x000fÞÔ!\x0003÷Í¡\x0006Ù¹L¿q^ÒSÝW=z©TB:w\x0014&F:	ã\x000e3.Zá	\x0007ÁQù±ã\x0001uõ¾~ö
ï\x001c&{Ì=`Ták¹/c£-ÙÉíVG0ÙÎcÚqÕÐìrT>\x001eK`;síd»Ë®\x001d¿í&\x001fJ{K\x0012¡9`U\x000bÛéÜ\x001bío»ã^¼n;öâ¹\x001e2tKÁ\x0001Pd'¿Õ\x0001\x0019eê¼¸Uxqiî5\x0005¤Ú&$\x0019Ý·ð3u^Ü{ñ90:Yl\x0012&\x001e°V_[õÈQ¦Î[\x00177EÔ`\x0016]@&/Å?n·(o©óâVáÅ±³qÞwõãââ õ5\x0010Ï¾\x0015ØÎÛq/\x001e§|Iµe/\x001eD)Èî(\x00022u~ÜûñT\x0004qöÕ+QõJ\x000e"!\x0003i]\x001agêü¸\x001d÷ãuãqçT.g\x0008\x0006#­-v«1Èä:?îÆýxÝô¤Öa2©ÚL'°Ì0g¿Y\çÇÝ¸\x001fÇ³^\x0008\x0005gd\x0014jµjðÍìq¦>F \x0008\x0012`g%­ñ\x0018ø^\x0000Eî*å\7î:éÆ]f6s\x0005ÈÔ_\x0013¦Sf*\x00007l¦ºàÎeê\¦SÄ	P­>]}ÜÍúÄÙ6ó¤6RûÃLËtã.3ahn±ÓÜã%ü2Õúì\x0007ë\¦\x001bw\x001eßy\x000e2iÔ×sÏ¬\x001cGê<¦SxL\CtË\x000c'¨×;6Ó¶}~©óN\x0011+eBM½Ï)Ò<ßb;ë	|ç1½Âc:/L8§¬pã\x0011÷Û³¸ï<¦\x001f÷Á[^WSá¸Hoo²ïãHÃôã\x000e3Ôw¯ç^#ÃK"\x0003µßl4ÄÔy'?î°uÙ7rÀR>\x0007çºÎ;yÅ\x000e5èÍÂ\x0003i²/¬Qiýºu\x001c©ó\x0004^ñ\x0006öFÆÚS`lzÛ\x0019y\x001f¬KB·ë"B\x0017¹ô«Úi\x001fÁå\x0014ýÒ\x0016|î}.t».(î)õÂÄ]\x000b>\x0012QÆ¹¬\vv¬ tïÍ H¯`¢e\x0003X\x001c£ârØÌ\x0008ÝE%h²\x0019\x001bÍQKÊQ\x000cZäþ6\x0015hãHÝ®\x000bºä\x0001\x0018` ò\x0019ÎIWënÚ\x0010S·í"V_æh8µ%ÓÕ)àÃÙÁ°Ø-¦¨\x0008AcÁ [ÉÒI\x0004\x0006	i#*?ÌÔ-¦¨\x0008÷Eæ!)Ê:9eÞnCÚ\x0010S\x001a_M¡	Ð%Ï7LeìâvTý0S·¢Â\x001b#Á°hZgöò®+gû¦Ôùð¤\x0019Ú ^l?&¥\x0015áü\x0008têxRÄç0eGuë(\x000b@g]òX»õ2ÊÔ-ñ¤Õï\x0015Þ.ê9®ûôÜnÏýP\x000c\x001a~ßE¡á7÷ãXsî4\x00061ÈíI	àü´tÅúeõËø)yhd®^¦¶×S#bççCîËB&w¾h)\x000e¼òÜ"Íaybº\x0015å¸Õ\x001fu\x000bfM\x0016, dv\x00102NÂ\x0014='t°<ò½äÑã§\x000f_¿J8\x0015ø,+ø`\x000cHÄÈÖÊ3Õ«wï^\x0006³-U\x0005^ù¬\x0016y×ßs
ñþÂ\x001fär-Ó\x0019ÌËdY*vJxRyçþóx\x0010Ì·`^\x0005æ£|É\x001c¸P\x001dG®p\x0011åZ
S\x0005\x0016Z° \x00023]+T¹\x001e¶^#Ù`»2\x0013£X±Å*,Ò>\x00123B÷ç\x0005æ÷\x001fð`©\x0005K\x001a0\x000býBð¼òkJå\x0016,«ÀêûÞ^P\x000c·óÀU$>nut\x0015`¥\x0005+*0\x001c\x001eÇõÃ[ôåO[yéq°¶Âe%{ô2Y\x000cRÙ\x000c2\x0016Æ`¥5\x0015êî;ýA²Þï«\x001c?NH 
¾øÍZ*uÜçu~\x001fT\x00120ç}iùvX´h¬\x001bAU`ã\x0007ç¯ë
Lð\x0014âÀhöï6£ã4d\x0005x³7ì1\x0012Ëð\x0015Ëo!ïwÕ/FÉ:\x001f\x000b\x001a'\x001bQF\x0011
ûþYaÂÎ£3\x0007ü\x0005t\x001e\x00164.6\x001c§\x0002!^cóm\x001f;\x001cÅ÷\x0001VRým\x000cßVuS¾ý÷o÷\x001f.~xøøíäâÂË!Õv\x0014\x001c:Dã-D¿Ê´×Ö·ÿýýåÝÕÅ\x000fW7ï_b±-\x001dcñiQO\x0004Ã
ÖÁp\x0018\x0019J;±m\x0000¦ºÐ\x001e\x0006}j!åãY5ôÿüÏÿ}ùù\x001e¯Ð'eC#êEO[°z*\x0017ù»9OñÐ	¹\x0002ò¬\x001ezqywWéê¡Ìè[F\x000ec
s&\x0015\x0019\x0003	¾8KñØ¦\x0014þ÷¿|ù×/é+¥§óå¤²zñúO\x000fO\x000f¿<>|n üo^þÇßÿúéÛÿ@¬êól®JÍ%û¹qöU]VÚ\x001f*â$]õúîêç7ïÿïß\¢ÒêÅë\x001f¯n¯¾»¾º{¨®sü¥!ªé^XìüúF"N4ùùi{6Pµ2þÒ\x0000¡$'\x0001¹¹O\x00102\x0015hútç\x0012a¾Ë+?\x001a\x0016WòG3ó¸*4\x0011\x00039«ÿfé\x000f\x0000ìÀ°ØV2ý\x001d'
÷~÷ñþÃ\x001eN\x0013ÕWo¦¬W½(ÏsuRT\x0016òËaÙq¢rïw7\x0015ëE ¬±ýpðE%»>Ì½c(QKsÈÁ\x001cbÂ|
Fi¤º©<¶âMeÄÈMÍ³ÏG²duH9s\x000b\x00086ÆùÃeCÓ¤ÿ6SD3E¥ê³²ß(ùgÈL»	r¢Hç3áúÊõãëèÓ¡\x0018/§ÅNG°T{ú¡A
^ÊcÓ¬òH1ò¦ýL_þ`sø\x000b]Ö§+úåÓÇ§§»Oß¾>\x0003°"Ï§pFI3ÇG	¹¥TÚ¥tyûúúêööêâîÍûw\x00034õã/\x0015½vÂk]i\x001cõNWåà|\x001cL"X
N0n^Ô3=#M¤Jê\x0019ò\x0001ã`i	þ\x001a§\x0001zL!ñ2\x0019øS¥ÎÇÁW\x0019ÇRÛ\x0017áÐÊÉ!Ap>\x000eziü¥À¡v¦Sì|vTb\x0018gÎµ'ª>'\x0019î¯MÆá\x0006UæðÊ4I]\x001eê\x001b\x0017×Ëd<\x0017¸ Mfã\x0014|>Sw\x0001þ\x001aÇÁÖXGÆ)sûnÅ±ôdó8÷l\x001c°\x000fÔ\x0007é§¢`t³\x0014&6OÄÅ\x0007æ\x00038\x0011q4æf¾2ádÞèÀWI3]ó§øÁþ\x0001¨³£ëçøþóýßº×õ&Ö·ô\Q[f3õô\x0012ìÂö\x0006ôöâû»Ëßx^·8±lKï_ÆÁÌg$ùF8ä¨8~{ùy\x0001ç×o\x001fÿúí3½÷ñ_ïóy|âgâ?þ×O\x001fù`\x0018ù/\x001au=×Gvd¢Ä\x0007Eè<s=È{};?\x0013¯^¿¹9õÑ\x0016,\x000cÔà/%W`¸ÃræX\x0012Ún\x001bË\x001eÂâ§«\x0016\x000b;`-kjÔ­T\x0019¨\x0014\x0018­U\x000ea¡±ñ\x0016ËÍý%åH§½ry*ÛB¯\x0014Îàòÿj>|úºÞzoï\x001f¾^\>}ýôøô\x000cT5\x0005}Á\x0008\x0004EPC©÷EZZeªÕ.÷·×·ï..oß½¹>1F®âo¨ªWWGa\x0011K{0 $­«»Çµ\x001e
"Þ*¡"\x0015'"\x0014]\x0000\x0002ÎU\x0014¨îP9\x0003ª~}.Ô@Ùùà­Gl½à\x0013\x0014'úÂ1(|¦Eíç\x000bfÖ¾E¨9W8Q6ï"%S]Ñi`VZ¨LÔh¹õ)£¢\x001b
Ê»¹C\x0000
\x0005s B\x0019'Pþ¥ðõ´Pnúdd(?!ÂïµìúøÓ!á&G%|a)ØT\x00013<\x0005pÜ1¨ºIrÑB%¹Ôù;AYöq\x0013PA\x0001&<¦\x001f**3g'S9.Y©8ñ4	\x0004\x001f¢Â\x001bpÜmÊg?w\x000f"<\x0016Rq\x0007\x001a~ÀuXBG­\x001dà´Tø6p´ýæ×DE\x001d×=úT­\x000eZîCàw/vëMmC¡ø²xªrh\x0007\x0002VP\x0003QÁ4Ï?À{ÂìµÐVËé7Ï,?
ÿ¥¦\x001fZÇ@¦ÂÑ]· ÀbÎqêÿúç\x000f¿üúks]\x001eT\x0017¿~»øéþó¿Ý?~üøéé¹ \x0013åÁè1<-vT\x0014ðËs¯3\x0015>«.¾ñÓåÝO×77on_äÂ×ôÖÙÐ0&ù-r\x001c4(Æ\x001d\x0004ÃgñÔ}­\x0003Ã	FËs=Î\ÉHà)ç£\\x0014ÓrùY!c;ß\x001c\x0008G0vñ8±á \x0018¶8:ýôó¬)66W\x0000!X\x000e\x0012ÇLG\x0018\x0016ëO\x0005û:0\x0012ÊGwaZÌ\x0015Ybé \x0018çD=XsÎ\x001cc\x001e¤WÁxd\x0005\x000bñ\x0018\x0018`\x0006qú¡#C\x001fFñ\x000c³Pß\x0014X¤9l>|Ðdoé¬DÈ\y)V8\x000b<%'\x000eaqúôC	\x0016ç§Î
{ÛÌe&\x0003wpù\x0003¶N?´dE2çXD6óQòÔîèÇÄ±9Ó\x000f%Y«çÌPÀ8x!³\x0007Éðüé¬8	Gâ\x000c\x0017Ö&×d°\x0007Áð
6ýÐE\x001fæÚ\x00164Yæ0òÔñÇ\x001f\x0013\x000eaqÌôCIV\x000cç±¦\x0008î¼\x0001l\x0010W9ºÌâ6êd3\x0001iª®Éø`ò\x0007MJ\x001a¿~èÀR}`\x0017¾U÷A\x001fÓY¨`W\x001fq\x000eÊHÔ\x0007@27,Ïd~N\x0003:'iÀ`\x000fz3·é¬z}C6Ë@y\x000bÇ#\x0010<N;\x0006\x00160¸8ýÐMó¨¬\±§^øhC2ü1S<Ïg|ùöë¯Îo\x0012\x0007ß.¾û\ÿ¦§ÃÚ@Úõ·a~âº$o\x00117\x0005
ï/°°ëºh\x0003\x0003Xâ	Rç9@ã«<±\x0018(Ì%»õ\x0011\x0003\x0019¨Àæ\x00119Lcñ0ý\x0018¥	Îpð
'ü\x0001J\x001cÇo\<@.Ã$c4aÜ]i\x0012MtÂ\x0010á§¬+Ó0
:\x0011k54\x00018¬ifØ\x0014äLnýhë Ä8
Æ/¬SÑD)×¨Ç2GÞA\x00025!o*¤icx&K(ÒÍ³Ê\x0002>W%j6Å,Ã0x\x001d~\x000cÃ Ò>Åÿ
¼\x0012\x0012ôç¯\x001aü÷~\x000cÃäôjf'²LH\x000c6a\x0018*sN¤æ\x0006`¢Í\isà
x: .á³··Ã\x001fg\x0015&z¼/\x0005)¨,±Lì\\x001aLE;é\x0019\x001f¡Á¦Lv6\x0005¬\x0008`Ûl\x000b²Fi"OQsHa@\x0002\x001aØÂ>uåà|a®ì3æl_3Õ\x0004N?\x0006a¢3í(Ô2
{¸19ÒÙ\x0018ÇLÿfú1LS"GíÐJs ^Ð3gÒÓ~¨ßþðWh\x000bÕèópñÓçû\x001f¾üû·ûg³\x001c³:Øg\x0003\x0005)È³öÈêsuñÓÝåÅÏWXkÿ"\x0018
®¨Á¬Ô³ÔÓt»V°Èq±hÍÎ]Z\x0005­NøK	\x001b~~ä\x0006
v"ã(\x000f¦F\x000fe\x000bK\x000bfó<\x0017Á0÷O°¢Ù{\x0015é°ª­²Ú^\x0016£ú\x0005~Á¢yË~]Âz\x0006\x0018fæ\x001e\x000cGüÍ»1\x0018Rê®`k%B\x001fr\x000b\x000eúMÓ
\x0002É8ºo|â8J(vçé¡"Ã.êé\x000cêù\x0002Ö\x0018i¦Dã2W(V\x0017wÔfX19ýPÚÌ\x001aº­`Å+/yÇg`È}Ù½\x001el\x0013z\x001a5Y6\x001cáñ(\x000c2LÇ.>p\x000c]ôôCû1R"Ø×\x0011è[F~z£\x000eÃâktú¡ä¢ÙÉbf¾\x0005G3I\x0004±Å\x000ez\x000c«tú¡#ÃT
ã
©=áuªñ½/GMêÄÓ\x000f%XÊb²`¨è\x001c\x001b\x0011ÙÉº|Þiù\x000f³_æc|ïüæ7?}¼ÿ0]w~~üøñþÏ×\x0014\x0006©u³Øá\S(5²Ý+ø§Ë×ÓççëË\x001fN¥N\x0017$î`Ò ÄµhÉ\x0017êTì<r¨êKä92×ÏD¯¨©tç£\x0008_\x0012øKE\x0014gÍ\x0012LúùQFrK´<êþãOÿ\x001dh\x001bêÿÛýç_\x001f+Åó9s,ºÌ\x0001u3r·\x0010
\x0008­ïÍWo/þÛåÝ÷×·§
f\x0017)¢äÉ\x0012P©\x000fS\x0007TþÉQ\x0003|x\x001c\x0000Ây\x001c^	d¹ cjÌ£zTã9ìºñe \x000fOöÿ	kk\x0014*ÏÍ?þþéâæþï_Cõì):\x00084C­®!\x0014BX³«7\x0017uýÜ]Þ\C\x000b\x0012>iAËeg\>ê	8¤]Y¿MUL(?ÈúÔ£L.´5$¹¢l\x0010ïµM¤PÅ³¿xþ×ø·WóÔ\x0016\x0003ôíÜçA¦úåY;püÛ9.\x000eJõQ_<};.\x000eÊÓsî|&¬Z&/\x0011ðä¬'»Tá¬ó*$\¥(êNÚ½üô[DKÏ°=òé`ò\x0004F»ïêÂF¢ÂOÀ\x0014¹ý"Ã¦ÖZ\x0005W_`Åa(T¤ÍÒ§\x0017øÜb)wÈR\x001d\x0002\x0016Z\x001c
N\x001a¬1µ	ê÷¹Û!;8â5\x0001C\x0013\x0010î Ô#ãø/Ùñ\x000b\x001eeÙ\x000f@Y\x001cbA¹Ð\x0003\x000b¯Îõ\x0019v>_Äù¡ãÅ¢¼ÅôCÅT7_roJt- Öo\x001cøqdEõÍºÃLÞ.}jfú-2ñÔ¶
ÖÙ\x0016
Ã\x0018\x0003­¡°Ó\x000cEúe¡øãUë\x001dq\x0008¨¿ñéÎ!Pü Ï#	ñ¥²AÝ\x0011+y|jN?@|\x000c¸0â6\x001ca
øÊ~¨êMÒõ\x0011<øÔ£k÷c²GÎ¼éÞ<ýÐÝ¡\x001c\x0017¡"ã;\x0014ç7c\x0008ët\x0015\x0014\x0016ºD§<_\x001c6'	Ç\x0006ËPxô¸

SÑko(ÿÀáþÌÝt\x0011¸Ëo\x001aVz>TÁ=W´\x001b\x000f[Tè5\x0015QÎC\x000e=~ÛG\x0007õøôáÓÓÓ·ÊÁ\x001fþü¯\x001f¾ü~WDQE\x0012:Á\x0017ÕÝã/Ïuh&<]bsØRõ_à\x001bpÊ]zV:Á\x0017ÕÝõw'[4\x0017 ©Ö"(¬Ü¡Pß*ØBáXJ6[y\x001a\x0005\x0011ugjP¥P\x0005:|½]zçý\x0001 ;E[u@)Êå	ó d!)=O]õ¡\x001a\x001ew*\x000bô\x0012½kH%þ\x0015Ão&r\x0007\x001a\x0013)ÇG±&KMô«dV\x0015jcDÿãÏþá?ÿ~\x0016sD	Ç¥i\x0015¯?z¶\x0019k¹c¡Umb\x0011E!ØïîÅ¸åë»7\x0003Ds¨IGd2±NãäÈIæEO¤K=A=\x0012Ë\x0015^¤à¨ìÑÄè@áA,¼\x0016í÷s.r\x0013ÊÁ\x0018JÔ\x0016\x001bäÅ¹ßr<\x0005ñÿcîmë8<ßWÁ\x0013Ð"<¾+\x0010(Ô\x0005	\x000e@Èºg#$\x0014jPDMU­æ5f;«Òlîæ¾\x0001ßdäGºGfyNxf-ºÌ¦C³Vý*2ÂÃÃ?þoN/].ÀÈ%q9àÓÜ¶\x001a\x0015¬Ú[?ý]ÿç£kú*ªvÎÙÃo\x0007§ìÅQN;h3héã\x000cW~¼j{Q:TÎ9»x»(ÂVq0]3ÎéÁÁ\x0002>S[þ9Dgjg½ß«Ôè§Áÿ_$4\x0010\x0006!cÔÖTTÖ®\x0002þÏâJÐ]'NòU\x0004G¹ª;\x0000³cì>U\x000fÆ¢\x0011]+GzpL¬u\x001a\x0001G¦³7éØGr{MØ\x0002\x001e¼h5H'Ð; £y^Úcö¢'\x00021;Ý¿{HAsPøà¸âÍ3«Y^¶\x001eçôà°Î(âè2]`Vò=kô\x0006\x001eLçh'âAEG.6
þÅHeU«\x0001·a;ûâ<>\x0017ù\x000c¦Çç{*\x001c²Æp½\x001dÔX9Sþ\x0010Øe]
\x000b\x001eRdÑÕ°_êåÔ
tó;òØD=ª\x001cñGíE\x0001òÀ]øó_þR¾\x0016vjùIzéôéÇ/\x000fßþùtÈw,²T/3ô\x0002P©,Ém;¥÷6è9^¿¾º¸¹8¿^ô\x001f+\x001aø©N/6Ü\x0012ì\x0010\x000bÀrëì\x001bqÍ¡Ûú"0\x001dªÙæ¹!6¹2\x0003	Éª¶¯\x0006)\x0004kê¯\x0005`hÁ©4\x0012'!\x0011£Ynè\x0002Ûñ©ò\x0010Í&Ã\x000ex6W1ÏhÖp	)ìÅ,ÅhMi¶\x0000-¿½iÑÂ û\x001dê×Ì¬Ûfúõ?þ\x0007*m9|»QÓúäì×»ß~?yuÿt÷ôË\x0001PD\x0007³\x0005£f]ã¹\x0017#¿ÐgTGÏ¾?}ûþäÕùu&<B¦ËûwøS\x0016ÀÇjÌ\x001cMrõ:¿>9ä\x0014öÚhx,?h6r'O¥\x0016
É\x000c'ÍÚÍ(öýô×¿üüû?v\x001b|n\x001e>\x001eë9*»z"-[Qà:döªÜo.Þ\x001cì6\x001aaj·u'\x000c\x001a\x0008Ê\x001cÄ¼:e>,»
0ð Ñµâ>&6ï\x001cJE$!ÉÏùË'õ×\x001fÉ\x0018/§B[h
>ß=ÿr(­ÊÚÖzÁ\x001b\x0007\x001c÷5\x001b\x001e¬oK´\x0005ïNo_/V\T*\x0016\x0013aA\x001c&ú\x000cñiè¿µ>oÙ'o?\x0016þÿãÿÉ°ôXNä\x0012«lZW%\x000elS¾Óõû?¼ùõ×²ZX\x0000\x0019j$\x000c=¬_ï\x001e\x000eÌe\x0012U\x000bT°?Baõù\x001bM«XBaèc}z}q½T/72í\x0008~w2\x0001çb^©\x0014C\x0016íBpt«5B¤jAÀf\x001aw­¯.fÂ¸×R¦X\x001f¾õ.Ó\\õ(þøÓ¿Â»úÏ'×÷ýö¾\x001e|?RrIR\x0019
®ÖðÀþ{æö$ÿ:ÿpe§Gô8\x000bÜ#e
ôt°5WÃ)D(¿ÿöëo¿ýÞt\x000c(7÷OOÓ±vd*àºÆZó±\x001f\x001f¸=¹9¿¾^zÀ\x001cS¹¿.\x000eàÚX\x0014¿ð\x0014\x001a\x0018Å/Þ»ç{Q¸\x0002µ\x0017%FqE\x0018º Të\x0006g\x001a:Qòel½\x0000ÅZ
TT2J­\x0018ô~5Ê´¾«\x0007%Ôjr±²:«å=\x001böÝ(µ¦\x0013%8Í:\x0011,ë\x0019ª²YtsÝ HôãÏ¿ý¹\ødÁÿ;ût÷ûÃý\x0013«­?¼ûå.Ö\x0007:®¡¦.k¯Ó\x0018\x0016µM,àìòô}~i°âúíÓ×GÑôPK©ålÉpP2¿@¨\x001bD'í«\x0003í6£aÁ\x0012þ!E\x000b
,¦\x001ai×M\x0000-ü\x0004_î¦eÃ\x0017¿ý~÷åKÙ^o>eWè°l¬«\x0015ùÒ
«vKS7|ñöýéÍMÙco.³#´Äôp§?Þq1U´^µ7\x000f÷ÿöÏÃ\x000fÚ¡'«NTÕ=4Ô©î\x0006÷½7m~Î.h\x0011ô£yþûßþ?_þ.\x0012èøçe¦yu÷ù3\x000fB\x0003Oö\x000bOºÿòåîcþ×d"\x0013ñvÇj	«\x0015VUâ\x0019TÅ-æ: eÂOwzûêüææôÍ»óçÕé»w4\x000céî»/_ó)ç(¤~üûÏ¿>ý\x0019qð)\þ@¦ìm<ùBÕÕfX#ýÛÇ§3\x0003e,?:\x001cNc/\x0000Þ(jz2Oö[¯®ßd\x0000ÄÉÆíÍÍRiµúñÞ¥ß LJ«/ïO^?þv÷ðùþä»ÇÏ_ó{èþóý\x0012R~î¨@u\x001c\x0001åõ6:_dÃþÎm\x001a¢×WoO/Þ|wõîC~\x0018/\x0008Ó©\x001fÿöüpÿ\x001f÷S§ºîï¼Zç¿?üüí»ÅÅÂþ9Wº*°\x0013§ATÑÒÀ
7Ìþb´ºÅó¢¿¿8;?]Z²	\x0018eâ`q+-2±ÖÎ\u\x0006£\x0006ò
\(¤jÅ\x000b\x0007ª¼pàOIëf0Ç\x0003c¨N~\x000bWÄj8ù¬!¥lÈé+REUþO2\x001b©XáZºZµ\x0001K=¯VÝ^^oýÜ0#\x0004Ãb=^._jä\x0010ÌG`°áM"\x0006{¼ûÇïjÚ1r¼{ÈüÓ2\x0014xKih\x001f\x0012Î\x0010B\x0015$ÊV5ÎB¼»Èæ~¾é¼AB-F\x0019Ktß\x0014¤\x0012Û\x0005\x001c¯\x001b+RÚ4\x0014{Veu2ÒP-[8êæt?~3ö×¯fúîx
?<Ü?ÿ-_>ßþÏ\x00013_È\x0006Q~\x000c\x000cÍ!Ud´4©ía+Öùí¿
³·âqë\x001co¨¶ÂWøPÜÙ<Èeskg÷
ýí W-] ý¾ã(\x0013í³ì\x0004\x0012\x001eÅR6âÑ\x0014\x0015KgéÈ7L}A¼ *\x001e¬Æû\x0018ÿþå÷ÿl·wO_\x001fî¿.»9ù3rMtfxæ/l©~.ûAA·NÅÛÓë\x000fW·×\x000b¡\x0003õcøËGø)¯-ºTÃès½Ë\x000ehöå­)§ÒË"\x001fCê@4\x0000@ý¬ÆÄfs¡Ëõî<¯Ìõ\x0015}~Ö±Sëý\x001dúã\x0018Å~úöÇÉî~þÏçû\x0003V>?nÈ»8ÔÚ\x000cÞ\x0003\x0007~­nnküh§oxâ«Wç':=ûo·\x000by r0¬+)2±XhíX
¬\x0005m6 ÏÿßUÉ³c\x0011k¬ïî¾><~¾ûtìò&ó.PYM,M/<Ê\x00024\x000b84*¿;ýpqõî4ï¸ü¯>\x0010+±4µ\x0005c4hØoÅ
aq½\x001e\x000b\x0005¥^?DXfâ#\x0016!w±lÅ²&mÃÂ¶ò\x0008+¿bêJþ%&±j÷S\x001b©pÖsùCB\x0015ÒºNÄ6*Wìa\x0014c7bá3\x000f\x0014+°(dÆ¥\x001e\x0018±<ö\x0005ç·íxÀø\x0016z1½«¥¨69:\x001e7«Åâ\x0010ÍÆ\x001d¦\x0001¤ö\x0001ew qÄÎ%¢rº¹¥MßP+|÷\x000f
°bþO	Öd¬hHæR2\x000eNùm[^£|ÐËáO	\x0017Öä\x000cÎ4Ni.\x0013à0Ë>X\x0013XU©psaît2PehìA$ö
ÛÇË[¼ü)â\x0002nD¨¯WÔ®\x0000\x0007Ü$ö§÷Ð
.ëUþq)ÒLÃ¬ÍÐK\Àß$Í×s\x0012ò§K)r	Q«Ä¡ËP7_zãw,j?Ö	¹0
ÀÎ}\x001c>K\x001bÃëµÑLX_¸¼\x000b»< r
\x000e¡ÒzRÛÎ£-µðåO\x0011W¶ð¸4ð¾·K÷´ÙæGè"|3ü)âÂqeiäò\x00033Õ~m´\x0013®T6?E\*]äÊæÞÒzæõòÛ«¤?%XÆ%jî8³,
XÆÕ'·ÓÛ¶+æÞIÍ½±4,òrñ[;{Ã\x0014aãíèõÐ\x0002"]/\x001cÒG!
HC1`jÍÄJ0{ó\x001fÿ¢dék+ÖÉÙão?Ý¼ºÿôi1
àRÀË¼\x001dnê¼X,\x0013\x001cÒÔ5än¬³«·ùöêüra`ßHhí°i\x0016ë$D\x0001®ÁÒæëÂùÙês)rTÆlCÌÿ¦	"d\x0011-	ÕG|áÁ[§®Eªc]OèýÐ{9ad§B¨ÈJ6ºµË-À6ÄìfO\x0010£#&Å¯\x0014oÜ\x000b\x001f\x0007Dk81iÜÆ­\x001aÄ´\x0006$±¿b¨GÌõm\x0010-l\Ål ¦Q\x0018±d2\x0011¢\x001a
÷3¢Q`hÛiÑºÙZË7#Vã%Ú\x0018æ£/]kÌÛ\x0010Mc\x0015ñ§\x00181»Ã\x0010Q£p0:ÂXâ¶1ÚÐ0Ú°1UFl"ÃXû'R­åzÆÐìFü)ft~(VA)Ð\x0003°²\Lzãní§+>µ+a¨Õ ò¬qJ t\x000bbkvô
»\x0013½¢\x000eÌ\x0018KÚ\x001d\x0019
éü6Û¶ÿ7Ný\x0008\x0005rÆ ÙaEÆÒ\x0003Xß\x001e*ãÚKPA"½µñ/òÚøéîäÍÝÓ/XÚqÈ×\x001c\x0013pùÆÖ|\x001dìÄùÍxyzòæôú5Öv\x001c!4~Jh¼0?½-5¹#\x0006\x001d	¾¦wa\x001b¢m\x0010í
Ä|M\x000f\x001aÏ8âÔaJ\x0015¼µý¾AôrD\x001c\x0016Dw`~ÉñqÉÎ{\x001dcü6ÄÑ0"bk\x0017û\x0010\x0001^PDÖ
r\x0003ÆJ\x0018f}~ÂÑ\x001dCÂÖ\x001dë#Ô:S"Jÿ\x0004F¬[1ÀFÄd§É®XÄXß.ãÚÙøÔ\x0016Î`f\x001d\x001eDçI\x0002düF\x000cäùäýÃã§CÉLá;,`öº^ÐúÕBNfØnOÞ_\]^,e3\x0019Ë4XF\x0015p\x0002\x0000\x0010V`¬ªà Ú\x0007\x0019V)V\x0000\x0011\x0016\x0006\x00168+gØoU\«\x001dtX½\\x00137\x0006¹\x001a7æ8XiÇecb(ìSÕåÊGuÆ$÷a¬wº¿´\x000cXö\x0002\x0007Ü\x000fåd>Õ¡èy÷Ï\¸GÁ TqªùP/Ñzüõþ3Vtþßÿù¿Îûééùórî×äw\x0007üdGoô\x0005ØÃã	v<\x001fÎßaIçÉù[3q\x000c,LÁ\x0010Ì`\x0006\x0003$°Íu¥ìj-Vb%!\x0016\x0017wf,=` \x0016H§ÜúõÒÍÔÂ/wÓ``!r\x0010\x0012{¼*Ù@æ\x001b2/\3OÕ§\x0011((^3\x000e\x0016Ø¤a5\x00194k\x0006Ò5KeâLY3?LXAáx¶dn5i°\x0010ËÓ©Xt\x000cÒwBëåÒj0k¦`¥½K\x0000\x0016¸5/É4Ôe2ÏÊy6õ_ÒAcÆ@H¨\x0013#b\x0015\x001cEõ¢7¼fa½½p­}\x0015~Ë\x0018H\x001a./\x001bzt3XàA+ø¬^Mæ\x001b2/$K¥Z¾i.cl.Pq{5Wl\x000cY~«Y½=bAª\x001e6YÒ\x001c\x0015³aý·ÔÓw©\x001aºX$hVUëï\x001c\x0015_dy.fv\x0014WLhO&\x0008&VBÐS\x000f/®v)Xç®Y\x000bjµÑÀ\x0010Ð\x0014-ÉÐ¼VÔ\x0019\x001eu\x001c¦df4íøgUû:éCË71Õïñr\x0002vÿ¥T1þý@Ý >_9\x0001I)r2lÕLuÞù\x0019²óRËøïå\x0015ÎOá¼\x0014\x00157J&bì\x0019ëû¢ÝpZMá°\x0006AFghªn4~Æ.tºÒÍÒ~ºfé´tí\$Ûfð\\x000c÷ºõèD5·ãºáL\x0003g¤pÙP1¯Éw8\x000fÁZ®
u1-t¶¡³R:c8;k}\x0001DgXÇÁÍ{kÝtã5tÓk¾\x000eX´3¢3\x0012éÄç/Ì¦mçcsb£\x000e\x0019ÒÚeÏ-ÑÚ)UêRÚD\x0017µÒµS<Z*ÓÅ\x0017\x0003áª\x000e»\x0013\x000b²\x0011"d+\x0011¢n6\Dcò0éU«ÉéDä\x001bd\x000bní0þÁÀO+\x00127¡\x0018ïXFû¹k¿\x001bÏµØLqÆ3/
«=[;£+-·\x0018þ{\x001a<Ñ%ñÆ*:«,W×Yâ\x0004?×Òùvñ¼tñ t^¼Äib£|]¼ÙHC7^jñ\x0014J\x0015¬ÑÅ½Ã4M¨Bå6l¹Æ°c©a\x0013\x001e,{O8*GS¦Ëª£®¶ÜcÜàáO\x0019\x001e	M\x0016¼Ä{°<IÏ·­b<h\x000c\x001eþáùD­¨ÓB±]0Ürî·ãü/jètñÐ½£C=cËÉ`[ñÌ¦Å³íâYéâYÿ>-¾Ã\x00068eªF^eÊ,õü\x000cñ*ÿEéz¸>yýðõäÕÝCIyÜÜ=|þzòöáç_ï;\x0005MÂDGqô¼-\x0019\x0003\x0010i*\x001a\x001e	ãåÅùíÉë\x000f'¯N/JÞãæôâÝ·\x0017gß/\x000có\x001d\x0002\x0000í\x0013\x0008\x001f\x001c¦Ê-\x0015á\x0003I\x0019\x000cN¸bq\x001d½ªÑÌ\x0008PÈ\x0014¤æÁ¡|Ìeõ\x0014Ëj\x0001\x0005ÍIÁü\x0006ãhNªz¾m\x0019\x0011rùË¸<§|±[©î;Û´ýÈ°\b¹(Á2\x001d;Tn¥|L²Áñ\x001d\x0016\x000b\x0014O\x0017\x001eÿ¢£ºÚ(¿ôéî÷\x0003h\x001eT\x0019äXF`:JçýÅR66ÏÄQV\x001bõ.Oß\x001f¨\x0018>æ¤\x001cÐ)x#ÝÙã¯÷'§¿Ý=\x001dZ»È=SÉj5\x000cáÁ\x000eqÏ\x001dââ\x0003<»ºùp~r-Ê\x0011FTÍ0âO)¤×\x0015£°q|(ÂÊ«ÈCÒ\x001d\x0006\x0005ÖBz\x0016-\x001eÿb/&Èï¾ýñéáoÙü=þçó\x0004/6Qñá¸®ÒGî=óÍ\x0008¿;¿¼ø·lö®þÛí1>g\x001b>gå|#Äù\x001d6(d>ÅÓü|ô36E@8:¢Ð+1!8~\x0003¡Äðàîù¸æÅÇ¦±\N\x0018[Â('T®(ß5\x000c\x0008^&\x001cg\x000cÅ¦äEB\x0018ÀÊx³ñ2Óãüåä»ÇçO¿`ºõì×oÿûëýÝó«
\x000c+?\x0018¥KÛ\x0000^mìý9«çl5ú\x0008ß]Ý^^½»ÁôëÙ÷§\x001fÎOo@Û\x0006Ún\x0006Ù`´~AÉXKÅÎ=ærf­\x001bfü¹\x0001Z±¶;ú\x0013T!Wº¤lR3Ûv\x0015õÄ\x0008Ö\x0008È©­ã!PØ¾Áùe¶WÎéíÔ(nÔæónWúÍÓÝáÞv»Jê£\x000fUÔ!qÓ\x0002;s¹#èëÓC=î\x00070Å\x0003òiÇ\x0007|Ò\x0018Ê¼ñ:*XØ²tÎOéÒaldx£¢Hg3À½&ÊÆ\x0019«/àófÊçÏRª7eÛJÑhëê¹y÷¨\x001b/4\x001f7?n~g%î\x0004S,`VúXõ½àÅ\x0006/ñXm4ãÙah\x000bâ%\x0016ØönÛÙzÊ\x0017µÏrÑ\x001b6ÜReztüuÃÜ3¦\x001f\x000fûÊ&x¥ÍLÆ\x0013xK2ÿÛ8DÐbÍÉ\x0001A7 ¥ù °ä¶Âæ?zp9Å-Ya# i6`á*\x00034u13ì0û8\x0003òÜ\x000cè6}bp- \x0013\x0003:C±ël`¸9ûµ	pîi(à\x000b¡á\x000bAÊçòXtN\x0016&=õÀÂÖ	\x0018\x001b\x0003?¥ÃÁ\x0002h«à\x0015Ðn²F7&\x001a
\x0001S Ö¤"Ø@~Á²6y²\x0002Ð´â\x0015\x001cnL\x0017_0ÐYÖ«ËOâM'Ø´&ÆÈML\x001am`\x0002z(`\x0000¿¯NÛ¾/´ \x0005Ì·Ø\x000bZÀÄ\x0019O\x001c_N\x0007\x0018Àlû¼£S]øvê\x000e>lm\x001a\x00005æw¸òd\x0004L\@K\x0018
\x0001±b0\x001aH\x001cbmVt`íLl¢\x001fÐ¶\x000e>þ\x0014\x0002F ¾ö\x000cè¨Ã j\x001eÕ\x0001ý&\x001bhMsñ§\x000c0\x0012Ld@\x0016\x0016B½¨ÄaÓ!¶­jÅ~*¶OÒ\x001c{]$\g¾ÎÙ\x0006úÕ·-Êmz<$ù«èé\x0019)R[\x0017_~^n¸By¹È9PÓ}I^®|Dm\x0017Â '\x00177g\x0007º­\x0006:ðS:ðRº¨XEÇc¦lsu\x00109Ì?;á&u\x0019Î\x0014.)n6ð¾¦C¨­Æ\x00166,\x001e« ÊÕJ¢\x0001µG*±\x0014ylªç¥lÚfdÃ<¹-¿9¨'\x0018Å\x0015dQó®KJoÁ³íÒYñÒa¥\x0011\x0010^öa\x0008µ¤m«b#¥\x000bº¡\x000bZJg#My¨½Mû.:N¾'cfoN¼\x001a¼¤xÙo¦°\x000bN/Ö\(¬Ùðm¡=\x0016 ?\x0016\x0011¸6\x0000çJXÂK\\x0016â.x¦Å3b¼ìIRQvå9½47Ì%¯·à¹Ö\x001e;©A¶ÚrØ%ß²ÜZê$èDãDWâÅvõ¢tõ²\x0003Á©hÍ³®BJ0ëv²¢
­/ÜÃÍ&¦J¯QaªcêÔ¼·ÜGgZ7ÀýÍ&a8¬å×8ð¨:½å23&4x&Hñ<OÀÕ\x001b&Ó ^Õ­3\x001b\x001c\x0001\x0013[º(¥Cy±\x001aLd£â:òüN÷ãûð¬nðð§\x0010\x000f'
	\æc8Ú6¬mm\x0015Ûìpï\x000eNI4\x000b¯«èr[è|ãªàO)ãb-´\x000bô\x0004Ò<WBk·á`Xß~[/þ¶vTøÊ7\x001b½/´®ÒP[®\x000bÛÚc+¶ÇØûÁ;/Ò1t¦ê\x0001ê-\x0007Ã©æÛâO!^àTlÌ¦F)h\x001bªò÷\x0016ì Y¼¢Ý&£CeSàjC:°Q;Ï;ÏnÙyÎ´¯\x001f#}þ¸h©\x000f6aí;\x0004
pH»-O\x000c7\x000c\x0014<#þ¶*\x00022^ \x000cB^=[5Óæê>ºñ\snñ§tõB]=§©a1¯\x001e\x0007÷t\x000fîuâµo\x000c'~c¸dJ;,â-âqËÏ
vÅ«fïáO\x0019\x001e6n
ÞJR1U£"Ç¥´ªtâéæ	äµô	ä\x0015k\x0012']ø¨£g<°\x001boO®\©9Ðew*ßòã¸ò|-G/iáÄç\x0016GËy¢ÓÃèH(Âr\x0004·Ò\x0019?\x000e\x0013dÆ¿x9)%ûå\x0019K{ï\x001e\x000eÑgÏÎ²¹æ \x0000:w¤\x0000³Q[,í=½8\x0010Æ+dS{\x0012_NÍI\x0007â<KDWo(~
us&M÷ééY(9-AShY¢Æ³tWö«høì\x0015Û6Éÿ Ú4ÿÓ6ö¥¢ú4÷	F]Ñf\x0013¤hÓ\x0008Yl#d\x001dhX¦ÈæUb*G\x0016åðzÎ¼õ¢¥\x0016-ÉÐ\x000bíPÐd9°FÑf\x000fh'i÷í5WhHKQ[àÖÊ°á\x000cøËË¸­
+Øb¨«
CLsH/Z{\x0006¼ì\x000c@zÁ²­«Ù­­²­ÑmØg±1¶øSB=^jXô*±¢¬\x0005îâ³ÿN²Ô®Y­r,Íá³áUD¦ë\x0018VµÁÚ\x0002è)\x001aþìFÃ^Eà¡$\x001ejw±¦JÈÎºäh¦¹¢À\x0008î¨ME$3ij\x0000ÇøÉháõ\x0017\x0001LÄÞ\x0010Í{\x0011Z~B³Ø©s&\x000eÆÚÇÍ!ö¢µ«æe«fÃ¨q
\x001c¬6V´ç|µ£h¾´(L$'òév«=>z8¤Ñ?"m5Þnä\x0004\x0013õ\x0013k³py^Ý^^,«:\x000c`\x0013V¦ÀP^:]\x0015\x000b¬Ñáæ}½`¡\x0001\x000b2°\x001a:7ÎQ?G@¹\x000et
K\x0016o\x0019eß\x0012\x0013JÔ¹>*Ô\x0018ÅK\x0016âÕè\x0000ÓJ5L)\x0011Y¾ÒiEËö,ZÃ\x001dÿq\x000bÙDÔªl'#såR*½ÃºL\x0011\x001aêc¹1|>"ÝfÚid\x0013]Æ±ëËÞGÍÀV¥[\x0006-\x001aÐB\x0015uÃ\x0002J.ÉÆ\x0000\x0000¡Íµõu¢oV
JÐfY7g5·ªe×ÝGëqéE\x000bEÃ"4(\x0006ÄR#Y\x000e\x001eë\x0018Ì\x000623QÍdøS@fQ#ÔÖ5pxÒ¬ÌÿqáVïB\x000b-ÈÜâ©$áLÔª¯TÅ^w²\x001bVÍµ«æd«6¢z4í($Ã\x001diXã·\x001e-Ø\x0006-X\x0011\x001a\x00046k>³DÖrÕûõ¢¹\x0016Mdq-\x0000\x0007ë=¦Rér%Uö ·ìµØ®Z­1TÇÝ´!2YÁ¹e>Î&ûÈlë¥YfyÐ@p\x0014J\x000bÉ³èhvl×ûBÖ5+flÅáÚ© ÆéÚ;ÆÙ2N2ßl³&å×CV;	\x0003ÔZv°,õ'`PC´(òlLÔ\x0019ÑÒ\x000bZ3\x0008|6Q0g=Y»hQ¶hÑQ)zÌ·\x0011§\x000b\x0012\x0005×smø©ÝiI¶ÓR 	¬1XEj±IB
w÷¡9ÝÜ\x0003øSæ´*±½RÈ¥j\x0005:ª{\x000eh\x0011å\x001e4Ó|Ð\x0012g ¹"°Uª¤\x0014yÞQµ4[|\x000eçS?%hP3ÞXÀå4W30]
)w¡é\x0016Mdmóß³\x000f=
*¦ÍhÀ\x001fÔnx|ºööt²ÛÓQ\x001dc)Ü2$Ý*\V¶áMàbó&À\x0012²üú¤ÙiQ\x000fO1áÕ¹æ×Oß>?½ìùy\x0001CUGÙ1
)ã\x000elZÒ\x00164Ý¢É¶Z~\x0008£\x0016\x001eËRxZT³E hº±¸^,.æ\x0005<\x0017º©ªª	¬]ÒlÛO'm,®·2
\x0006éVeOr>Q;ÇM·z§æ[ÏÛË<o?¨ùw3îµÂmYómxÈËâC80Èòeª©"\x0018®\´K±ø\x000e²0i#ÌdÁEÑ¢¡L6ÍAµ+ÙÛÖ\µ\x0018Í\L'ZH
ZH"´Q\x0014cßCè6£ÕöFµþ|FhÈ"ÈÈp2+õmåè]DÙl¨uEë¿gl\x001fíQöh÷\x000b)\x0002û4y8s!×ÎØ\x0006o£,zëó\x0004êetêcóÂ;F\x000bKùÅ\x000e´\x0004ÍÕ@tµûä¸Cq\x0012/\x001aÅBF0[¸{\x0014Ìá\x001fÙù~9þÅË\x0019vòîþùÏ£0$\x0000s/HË;)Ï#j\x000e\x001dwç·ß\x001d\x0001\x001c§." 9\x0008Ç\x0008QHòÙñ'Mooë nuèyÐ\x0018\x001aÄ9+r\x000cÑ\x0007~]af%¥4N":t3ô Ææ3Ï\x0005?!æ÷| ¡X¾êï§ÄÁ¼lJ\x0007ãD*\x0015\x0019Tª\x00142Ù:%ÔfA\x0005\x001cÜ
¨­µ\x00112´36æ($pÊÏEÃÕYj2¼k¶aP\x00029êA\x0015H?ã\x0013\x001fÄö\x0012Í8g*Êcà\x001d\x0019f÷E©\x001f\x001b¬Ü&uw<ô°PI×ºA¦&íÊ¨§"£Nïï¿>|=9ûôøåäòîç_ï?\x0010Ýwo\x0016Èÿ¨XïuÞL\x0019#ùþüÃÅ³Ë«ËÓ³ïOoß\x001fA\x001dKX
*¬bµÊ³v\x0015\x0018Ë\x0013Ç¥x¿3íÐÍµ¬£#¬\x0013?ZÄýÄ
ÅÆ\x0017ÃNN±s¡TC³\x00014¬Û\x0002\x0016\x001dÄD¨ôj1²\x0017+ì¿56«ªãºe-\x0015Äª\x0006rª¸gÝÀLJVÊ:UaM¤Âº\x0015=Ýáhé¤(Ý\x0018µ§x3ÊÎÄrÅ°¾Ù\x0004Óê\x0013\x0011l\x0014rK:²\x001eJÔ1pÑpaÇÊð\x0002;©\x000cÀz\x001c\x0010LÊ\x0005\x0011jcG~é0ì\¥\x0018vH)°\x0013\x0014\x0011¬¶üàÑÁ²\x000e	¨
\x001bçZ>¥°fTìAX3Qì\x0011Áæ'-yóN¯\x0017ÁWI\x0008?ç£ô³Z]\x001c¾±J;ÿÅKÓ¤£ß?~þúðéÓÝº¤JøT2\x001fF4(B\x001bË\x0002Ûz!\x0015ñþêÝËËÓÅÒ¤Om´È§\x0002*Ïþ¨5¡\x000e\x0002¬¹\x0012ï\x0017üÑ^ÀQú£\x0000&-\x0004,	9\x001e+Àý>EW4Ò¼×	\x0008cu\x000b\x0002B[ÝÒ\x0003hò>Tà¢ÈÅóÉò£ÃÏ§t\x0003:hVÐt\x0005QÂ\x0006Ë\x0010X®Ø¿µ	Ð¶V\x000c=$z¶e\x000bCú8>_ë<Me!B{/ßkÅù\x000cÊ\x000c/ûû§oô©M\x0006\x0016ÚÆâGRáò\x001cv´ÑÌêüeÊëó\x001e¡É\x0001uRÐWVd\x001d+Þ4©æ©\x0018Ò[.\x001eZÐ´\x0010¢N\x0019µÍ5
P©\x001f#P375s6ß/*£ÔÓ²á¥\x0006µ\x0012\x0013#\x000b,%\x0011¹&Ñ×´íl\x00145´¨a%ª3üäDT=Xt¼/ÿ¬65¬6­dÅfb­Òb«c³qX¸}$°©Ý\x0003ií\x001e°ºê\x0012@\x001dÏ	Y\x0010#ÍêË`A5»\x0000ÔÚ]`\x0006¬[²|¯»h8K¢\x0017Âu"Xh-+¬´­\x0008\x001b9Û¤(\x0000a9f¬`¡½B\x0004ë=\x000b~íU\x000bôÒô\v{¡ÑoF
-jXê¢j[\x0000\x0016/E=gÖ3öÁ\x001aÝ\x001c/£×\x001e¯¼®¤%¬çÚ0çb7X(\x0014\x0016ÁNÚF\x0010vÇêU)
ÅJÓÕ²,¬VKN©Õ47,þ\¹°O\x0017&Ø öc2,,´ `mc
ðçÊ\!²ç\x001f¨\x000fÒFÎ¹AÚî\x0015àÀ\x0006Ö­Õ,ý\x001c\x00027F:ÃýÁÚ,48XC»\x000bÂÊ] òãÉS^N¹\x0017zÕ-\x0014HXmhL\x0001þ\Ç\x001a\x0015Îpó:Õ¬8jaûÂÚIÛ\x001dÂ¶mw\x0002Ø\x00109Ô«uà	<ÎTùÛ\x001bëÚÖ­½hU0T\x000cS&etPûíÛQÆ+aÛu«\x0017Ö×©\x0004í\x0019ä\x0015hÚ^ÖA:,Kî"£\x000eÍøW?\x001dî\x0002( JÕà&ð¼o¸¥vAX±)ÿêÕò|\x0017B¤å±`nÆ1ìAÕ	Xù«¼c\x0013=\x000e¹\x0013!{\x0007|>Ô|£LQñç:V\x001bX\x0015ÇÇÈmM\x000e\x001b\x0012\x0006VèyÐÉ:½¸2ëÜÅÕÅRT\x000e­j¯\x000b\>Í¬Ó$~fu3~a\x0017«®sCö\x000bÉ
8\x000e©are3ê4S$\x000cUAiÃ=áÎ*.ßÓ\x000b.\x0002VH
+ÌÅ2zX®(£²Ü~dùÅ*È­¨Æª)*þ\
Ðcé!*Ñ\x0010^VØ[¨Ö\x0014ZÓ\x0018VkVYVYg,Fìî¢Nm\x001eî[[öª¥aÐÕ²Z\x001c\x0006Ý
à_?~¹ÿôðíO÷ÀZq3·ðbÀÚ×\x0006\x0019 ×W7ç\x0017ç×çË1V\x0008m¦Ö¬@Äñ\x0010Ü±\x0014J5 2*n«nÖ©@ú\x0006Ò¯Ìo~VhñÎR·¨Çö/\rï\x000c
dX\x0003\x0019bÕ3ÆÂg6z?Ô@N²&8Y¯ôCkÞC\x001dæV[f§¹I\x0018µm\x0018µ]\x0003	ÀÉ\x001d\ÉáLtË»q%u»zÕRfcNW;súÞ!²py\x001dá\x001eJUæº©r%Îuk-Ð\x000f\x000f\x001f?/óa\x000f
¼X)6ÑEm \x0014\x0019Q{ö\x0017¤Ý¸xóî(ÚaD´i±\x0007
\¹\
¯õO)ºêÄ/>èb³Í²Yá²\x0019à©\x001bàLÄW¬8oæ\x0015zzÙ&¢éÍÍ²{fZ¯Y\x0004×ø¹Z§n¶Ð¬[\x0010®\x001b©E [ðÍ\x0000?ÌâÒ8>¶Ø°E!ãa¥\x0015 T\x001bbbeÍuö²%?eK^Æß³0(\x0019B2¥¥¨hrOI³\x000fÚN6=!&D\x0019ñÂ
b=eØ"+ñ\x0019.X³jÉ\x0012wÁMë¶Ý\x000e~Ïi°ô\x000eL8\x00142È"Ô¡³1÷n6ß²	¿jp&H*s\x0004Èxµóå	Ýl©eKÂu\x000b¼ã\x000cæø¤ÒÅå¬üöÂµ7^
¨/oè£ê"E3ôñðÐI¿ïk¯\x0006-½\x001b¼§\x0017r2V\x0017ÅARWÎ.ÍëóÍÝÐÈ¤um9ö?qBÅ*ºS­Sk¶ÜO\x001aÊ°qt:ÆmptzF:{üÿÄ±é÷OO÷eNçr§E~kD\x001aîîQÁ^\x001a29ù\x00087\x0016ììêCþ\x0013¦_çÛwZ.*(LAá¿0¨ÿÂ v
jÿëæ¥ôÍ\x001eÅ¿À=úæéîsF¼^\x001e}<\x0004êu¥ÇØÈýÐ.¨©Áys}ú.S]/O<f\x0018Â@/Là\x0010±ðâ/Å\x0013ÐÐ¬A1S\x0014Ó\x0012UªJëB-)5 ì|£dÒÏb§,¶Ek¾\x0014ò²\x0012þ/ÉZ
æ·L?Â¸Þ	/T 1\x001c*wß}®\x001dþÙ\x000fã§0¾se@sA\x0007ÎL¥JR¼xeæ¦~0	0\x0018á¦Ýë\x0002®qÀ"®iWëgSØ»0ÃÄjZ\x0018*ÌÃhk]¸
&MaRïþ\x001d\x001e¹eaâ\x000c®.Ìª-3©±@§:ipd\x0014&Çº\x0019\x0018è¯K³ÎÌèÖüvÚ_ÜÁT8k¸f¢&»\x000e¦1¿ºÓþjk¹Ú\x0004}(K¹ûPb}SÌÕOÓX`Ýiq\x000fWôB×=<®
¬¢il°î5Â®äè@qÖ-²,k´ôÃ46Xw\x001aa
<¼µ,
õb\x0004¤.Í*»§\x001b#¬{­pF`Ãg=ur<F\x0011ïí°¦±Âº×\x000cçG]ðL<\x001aÝ¹É¶Yu[êÆ\x000eë^Cì\x0003á¨-J9¥*YX*¹ÖÀ4vX÷\x001ab\x0013^LVÊ¼
Û\x000e\x00144v\x0018zí0V2ÑÊ\x0018O\x0003J×Ü`éÜ:Æ\x000cC¯\x0019¶5£KÃ\x0015V¡*Ò®´ÃÐºÁ½v8;lùLÕTõÚ3]·k ±ÃÐk1`bê\x0015e\x0012'ñyi`ÕéÆ\x000cC¯\x00195@³ÿK\x0001à},kWù5Ðaè5ÃNqÁcÑåKaôaÝ®iÌ0ôáT3íeB&\x0017±°f%ÆîWÑ4f\x0018zÍ°³Õ5wÂymê
¥×-Mc¡Ó
2õ¾ÌÎh¢ò[}¾vèe?Mc¡×\x000cç½bô¸4t{WIÖvôQ7iÌ°é4Ã`\É(¥1\aì#O´tV-iì°éµÃ e[ãêJÖo{wÆ\x000eN;\x000c&Qëg^\x001bK=XÁ'ÅkcÖ\x0005GL\x001bèµÃ~b
kã¹çµ	«¼sÓ\x0018bÓiÁÖ\x0011\x000bF»ÚQª ¹Q«îoÓXbÓkq>ÜøÞõìLÔwT[}ÐOÓXbÓiÁúê\x0010ë*Ö·n57jÝj,±éµÄÑ°`0Ø\x0005\x0005¨Òñz7a\x001aSlzM1v\x0006¸º6Ô\x0017Tð\x001bÏTcM¯)NP
S§\x0015¨eÁº4\x000eV½£lcm¯)F\x001fÂVs£wT¨s­\x001dÄUØ6¦ØvbÐ2ÚÙp<£ÁsÇ³j\x001dLcm¯%öãwÒÀ± YÒ_å÷ÙÆ\x0012ÛNK\x000c¨ÔÉKã©¶$øÀs©òÚ¬£i£Ã½8@
¯©ú
uÌ\x0001¬;Þ¶1Ä¶Ó\x0010£X\x000eãÒ$î\x0008ö\x001b·Mcm¯!Æ!C\x000fuª±êüã=¬Ò:Æ\x000eÛN;\x000c®VÈ\x0019T#´Yª4ûç«n\x0005ÛØaÛkQ\x001ewæhu°ÕïÓëÂ ¶±Ã¶Ó\x000e·õÆÌo\x0017Ok\x00035òhÖ\x0005m\c]¯!FU
Mû&÷&ÒTEv·îD¹Æ\x000e»^;ìÓè Gn£\x0008cZÁ¬ò³\c]¯\x001dNU©
°ÛÏÑÊDö³ôº\x000bÓ5vØõÚá`j.*?ëè¾4<°*»\x0012ë`\x001a3ìzÍp¬¯\x000e©6éåG&\x001fo½Îò¹Æò¹NËgT(ñûB\x0003<+%)^\x001bµ.\x001bå\x001aÓçzM_\x000c5¼=·´kê}	ëlklëµ5ùëÐ\x001b£H\x0008?'\x001e[ÿßV\x001d(ßnßyºqüUâIX]|aòS\x0001Ö¹\x0012¾9P¾ó@å\x0003Ãæø@'*Ô¼^õúö+á;]	£\x0015Kµ\x001beê\x0010ªÏ§Ã*3ì-ì;·0î[~·(¨4ãh0í×Ñ4{Øwîa4w¶^ÞÔÃ\x001eXõ/Ã¬\x000bf\x000fÞ=\x000c\x000f\x0014^\x0014êËß÷°6«\x001cÐ\Q¡óÂbHR¤@Lï0\x0006&V^Q¡ÙÄ¡w\x0013SºÐø:³JÕµ>wÃ \x001d9®MFÉKsñÛïw_¾Üs\x0003Ñéç\x001fî?\ûãËýÓ_\x001f\x001f\x000e \x001a\x0016ñI¨4ä\x0008ÑQÙMöØaº³/Þ¾?½¹¡>¢Ówg\x0017çïN®ÏoÎ¯¸º¸>B­\x001bj½\x0011;ÔiÂÕ4¨Ì³4mêP¶POÒ&¸Öf\x0013µ\x0005Ú	/\x001f ÉoÙÓå\x0002ÏÆKØmÅ6Û\x0016ÛiÒÏIh\x0008y\x001b×µnËR·PO^3\x001a_3\x001b¨=åì\x0001Ë&;&Þ×¦\x0011ñÜ\x0002í\x001ah·\x0011:°8böd)$²á\dû/böÍ®öÛvµ3µ\x0016\x001dÕ¶\x0007¯´sÿ*êB¦F--+\x001d)E°n!\x001emUvÄ\x0017ù¿
[7ØzÛb³\x0010uÂÒDªÒAÍ\x0015ÆNÿªÃ\x0018\x001a\x0013\x0012¶P5ð±zÒÈ	\x0014[>Ûô¯ÂÖ&µ×\x000c\x000em®çW\x000f_NÞÜ==Ý=ô`ñ\x001c3OÚs\x001e*ðxw÷È¬í¸=yuuqsòæôúúüÃ1ÊØPÆ\x0015Ár	EBRSx\x0016ïÇa
[)Çà1RZ½ÒpÊ>crò\x0015EíÒÙZB9>\x0012\x001fÉbJ¬¾£\x0011GÁD[Y\x001e\x0006ÒÊ(¯£\x000c
eXAé\x001d÷+gË\x001fcMbeôìÙPSæ2ª5kéY;=:WÒe-UÕYkÊr^ýØÔù \x0004=4\x0016õËÉÙÝÓ/ºWS6Ftr5\x001cý4Ñ³v!Ì\x0002beþéõëåV\x0016\x001b\x0013¼\x0008g\x0014\x000eê 0§X2ÁÀz\x0006æ-åQº Ú¤fþÔ|à³oÿüå ªO¡çù­CÐ­\x000eá5\x000bßöìüõ²èN;\x001dý:
\x001dýS´_ï;æÑ\x001c\x000e:>É5\x0010-wüªy¯¨âÜ¾=6öL#ZÒ2´ì\x000e¢s	\x000cð\x00005\x0016\x0014vù-3ë õ¡é±«\x0000Ñð§Í\x0015Ukd³¡¼N
\x001bÏ2nÁðu±Å
Í¦q¼\x0001\x000fÇ©ç¼pÎÏºh½p¡\x000bB8EIaáè£Z[×má^ëbs®aC)a3æ\x0005¡@£\x0016":\x0016".\\x0013}h±EB´H\x001aåV\x0016BØ(½,µ\x001f4	?¨áwÂT\x000béÒuì¢êy\x0017µ\x000fn¢bpå¡/Úm¿0³\x001aèZ\x0016«³­\x001eh7\þ¯û±)ýÆÿ~Ý^
¯¿ýñ×û,_ù.zìó\x001d6\¶âTòâ<k8XòK^ÿpþßo{¢K
]Ò^é!Ä¥\x000c·Ã8)':»dãºðôf,çÏ&ê\x000fÄÙVÔÕü,í×Vvñb\x0017Åx(ô<\x0004Rò;ò¡Å#¾°ô\x001aêâ1À\x0000\x0000FÊ\x0007<õ(©ÄíùûPoþ-ëgÆ÷$\x0002\x0007e\x0007_\x000cÉHÙã¢[,cUÕ>¿ttûø|ó}ñ§ðx!ù»¤c$\x0015$çB`\x001cÜc|6þØ´Óå¿x\x0019Zoøüç§Ï¼áX#èQó¬üà"\x0014çÏnöÏÏ®/Þ-zÃ\x00047V\x0014#\x001cD!]þ¬­<éW\x0004C³w2\x001cÌÇbzáR\x0003p8Lô®¢+#Ãùª½\x0016\x001e\x0012]tcå(Ò\x0019+¥³4®±(Ã¥Dtu\x0006­Þ\x0006ç\x001a8'ã9Ñ÷\x0006ã\x0013Ø`çãôtcô\x0015J^Hgé¾!jÖÿ3ÖóÒy5\x001fÙî\x001b¬å¼*!\x001cvóX¢ÒÈtu¼Kòz>¬ÚI7ÎFº\x0008B:<ô5ä»\x0004ë
pÑHrà&Jk\x001c\x001e8­Y1/xÃÕ\x0000f´uv>pÒM×\x0018â$µÄÚ±JjpPÔ¿
«cÝ\x0017ÂüGé<´\x0001Ñü\x0017m@t6yøôéñàðhn`MVs<*Ð\x000c\x0011bÌç7\x0017W"\x000bÌ\x001aÆ´1¼\x0018|\x0015h*ÆÂã8Ez\x001bâØËàÖ \x0002E¿3£! /#¿ló\x0011^Ìu26Ë\x0008kÑ%
öà!\x001aûî\x0014gÉÝH8¹Û2a{·õ\x0012fÓ\x0008\x0011\x0018ÑÖ|\x0007;Û8V\x001c!¢ßO*\x001dG@ÕºÉd\x001fuWìÍF;onº\x0011Ç\x0004\x0012"Î$:\x0010\x001dÕøåUä^¨©©
uY\x0017st¦AÜÏ\x001eGD»8,bv\x0015\x0012O
µã^\K\x0018wê\x000fò_¼Üy\x001d½¹ûýáîôLÔ,Ç\x000c{Ï,g³ÿºðð}súþâô(mÈ¬Ì°\x0018gÔeMtíL)-¼±
\x0003®&láåÎù½Ã\x001cÆýçÏ\x0007[CbU]MµRÃ;îÒ+Ò¦óßõ\x0014S\x0018çïÞ-Ç\\x00081L\x0011Ã
Ä1ï\x0012ÊYy¯Y¶<.æÝ{\x0011'a¡Øú\x0018qDã¹[zl\x0008`7?¶Ã~W16Ë¨åë\x0008yñh\x0019µ-.NAäÒ>Ê¬FLÅÈº)ù/^¦ö`\x0019YQ^&´z\x0010ÀÈV:\x0001K\x0000È\x0001,«ç\x001frù¨`A\x0019ê>\x001f\x0001\x001cÓi\x0008\x0008ZNjÌ@ht-l\\x0004¨C\\x0011u#ú\x0006Ñ¯@då¿\x0018¸-/²$¬ÕÑ.z\x0011'oÎh\x0018\x0011/!¿\x0011#ËNe\x0003Ä«\x0018Ýì³S\x0018\x001bÄ¸
\x0011èCÛq+Ö±NóO\x0001bsXü´\x0018T\x0012u¨xì@ôÜ¤cØ¸®ùÐnÅF\x0007Ú¨\E5tò\x000b\x0001ó^Dß|h¿âCA«	\x0011}íÔÓÐ çÍ¢\x0000±ùÐ~Åö<Ë+#ªrÏ ¢¡jJ\x000bXì½\x00161ìx8ù\x000cîx8ßûãéñóÉÙýç_\x000e`fO'oB?\x000eJ¤­|3r0i)ûðýùõÕ»³ów\x00072çF\x000c\x001fg^+õÒï¿W.>-O\x00148í~Ð\x001cO\x001a\x000bÿ\x00085öUs\x0004Ý.Ö]\.³jó_¼Ü	Ø\>||> 4\x000c©Öº»¢pQZ»«j
Ì§YÏoN./ÞÜ\x001e\x00197°##ÿ¢ÈµîÃåãóO\x0007\x0007
ÉµÛ|é±©éãz«çãÓè=\^Ý¾:°z¾µ5ÈçÏ)\x0016®Ê\x000f\x0011wEì\x000f"¼¨^Ê}xc;\x0005âù=ïë(g
\x0015\x0013á\x001dñqÚÏ?\x0002ºñBóuw\x000bFã¡\\x0008Ñe[3¼>UÕÑói¡\x0014ç8)\x0011¹Qÿ\x000b«õNúíÝ·ÿ÷ëA¹`j\x0003I8§ÚÐû=:Ê\x001bîtEOÆÛÓ\x000fË\x0007ÃìdFm73r-?N¨LÕZK½D\x0011\x0014ª9³XcÕ\x00037j! 	r¸A\x0004\x0010Cª/x¦»á8¡¥(p\x000fÛØãl\x0016dl\x001e_ì\x0014ñpÊÖ³\x001a\x0013Ã-ØâN8ÓÀ\x0019!\>£\x000cçU-\x0016Ò
F²
Î¦ö)ÿbç)á¾ýñåîóÇCñU²\x0005JÜÌ	LJ>Ì;ÐÈw~súîÍëb@\x001c½SD4I\x0018TE\x0004_]?®->ÐìD\x001cu\x0004L\x0011\x000e_h¹{4Bd9\x0015¬dÄÅÄa'âÿ2e¨¡\x001c1êºËaðEL\x001eKéÙ8Öì#bÐ+\x0010\x0003KäDTÃ2Ô_ÀuJ¥%Ï¥\x001315IiJ8a=1I$¨\x000bEE\x0002Dh\x0010wma\x000f"O¯À\x0008\x0012';\x0013ð´\x0014\x0005fíÎÿÅ=Lå;)»«çï\x000e\x0008Ï»\x0014a\x000f!¿\x0005T\x0005\x001eCX´7W·g§TñÝNÔ\x0003á@JÊãjØ.xªQ\x000cJ±z@K\x0017]\x001fÞ¤É,ã\x0019\x0010ã)VüÆ\x0011è´gºÅíw\x0004/ÿ\x000bl´ëò_¼Ü©ï|ÿõáëÉ«Çç§\x0007\x000e±
/\x0002[4®*\x001e$ÃÁÁùdöíÉûó\x000f\x0017\x001fN^]Ý^¿9\x0002iÔ\x0014Ò(9$j1Ð\x0019ñFÕæÈ\x0003\x0001£ÞN9
F ¥\x0015ÙdSÁW\x000b\x0003£Æ%ÃÍ¦¡4ë>¸§\x0019aÙô\x0018îff]ÒÒÖ¶26qÍZÖäIþÁÂÀ\x0015 aá@z?ô~
¤cU\x0017ß¥\x0016\x000c\x001b\x0016z\x0005\x0004Í	÷«N¸gí8oyêVI|xÂ\x0014Q¦2­¡¬S.û\x0015¬e\x0014]¥4\x000bA¤~ÊÐ\x0018¢°Ê\x0010ézÝD~/ç/ÎÁá\x0010æ\x001fV"ÊÆ\x00105(
C
¥á¡\x0017¨B>-
;(-\x000c"ã="\x0007?¥ÄQ?Ü?-×d¦ \x0015e|òQVE_\x0001¯Æ±ÆKÏw\x0002\x000fC>8¿^,Êd@×\x0000:9 yA3h5½2\x001f\x000f\x000eIzq?öñAÃ\x0007r>Ð4Û½dõ¨/?`¹JÍ·Éö\x0003¦\x00060É\x0001]Í:Ö\x00164å-?\x0003±åv\x000bßdkæ3AÌgtÑò ì2ÙÅ|üø\x000b«¥N¯N@Û\x001c\x0011+?"Æó\x0002bl.\x0012_¬\x001fx>ðÚÁ·;PÇ\x000e\x0003u¦®íõ}þñt(T\x0002(.4\x0010P³ó5ÅcÝ®ÆÍÉõyþq½\x001c-a@3\x00054b@41¤¢cÍ{[·ÿÙ\x0008è¦N¾®§ä#\x0018ý\x0007k\x0017\x0012ó\x001d4é~<ÃeÈu³\x0005oî>~¾;T\x000fé8Í\x0018cvohîáqhª\x001dG9Ù7§oÞ\x001eC\x001b{J\x0010m§¥ä(Z¨\x0019§¿2½ëM4\x001c\x001d	K\x001d¸}l®as26\x001fX(-åmG²\x000b&*îZKÝ\x001a]lyËn'²Ô³n,°á°V\x0007GWÙÒo:º.È¶ãº\x001ce<b\x0014zXôÉ$n"UI/x-]lÀ.íö·\x001eg³u¿9Å¥Á¶\x0006ÔµWãécÓºù¦øS\x0004¢T\x0003[pµ\x0004Ó\x0003YòTºØÚ³°Û§yÍc¨õ\x0014öÐÌ3Ëi\x001aý
p¾ó28S½y\CX²+\x001bµ3\x000b>h\x001f\já$Ö\x0017WE:óÊQ\x001fi°^myá6}ÕÐ\x0006\x001d$ÇÁcÜ^ç	?0ø­Wá¶Öh\x0019ÁÊê\x0002Í±Ûd½¯lKM®GàrÚQ<3ÿE\x0011ÏÞù\x0008w \x001eX<á¨Ïr'dÔ<F\x0019â|{p¾ñn9\x001eHt1Néb\x0014ÒYM¹ê¤Qçxèì09£\x0017GzèôäÍÍ\x0005Z\x000bñã6H\x001c1á\x0008ÏGnã³óG¢\x0017\x000fZ¼]Í£xÞbÆå| \x001e×û"ÞR¨¼\x000bÏ¶xV\x0017\x001d\x0005zÆÞr½º¤¸wÄØÅW\x000f\x001e¨\x0006\x000fð¢1lît
%yxµ¡?ø¥lz\x0017]»õ@ºõ¢\x0005DA'îpMvuÙ»[J\x000bwáµß\x0016¤ß6úµ\x0006Ðä\x0002àÄFêÅ0K
-Gñ\x0006E1Íÿ¢I3Ü|=ùÓó§O\x000f÷\x0007ú\x0007$®¡\x0014æ*¶Èé´eìè>ÝÍ?Ý^^^/VÂ\x0013ÝÄ	ÈtS\x001f \x000eï@Á2Ë\x0005Ü\x0011Uå)X6\x001b\x000fï¦\x001b\x000b×nZ¸ÖGg¹ÙÐ%à¹È	LÌ¿Í]µ=t;ò%6ìÈd¼Ë»Ü\x001d\x0012Ë	Ø×0¬öÀ\x0003ä!æÎ \x001eó,Ýåé?]®ù³q'7Úi°ëÜ}zþù×
VQßÆæÁà\x0005°\ó·\x0014º9½¼=û~¹ëè¬ÒÙÝ\x0007ìQ:\x0008¬w¡³+ ¦þ \x0012Ù%	N¼1xn×:}§Èö8Q^Ðùd\x001dãùEÿ³oìîB>¿ë\x001eåÃ|\x0001õô'OÉ6çC¬\x0016yùÝÅ7êá"_Ø}ö\x001cãË7+\x001dÜí\x0017ÖÏj*Ý;ùRò¥ÝÇÅq> (E\x0002´1\x0017F)MË§¡Ù~øSú}#·\x00138Gõ/Î¬&l:\x001fº=¾Z~~uÕ«A\x0005ÀÀ\x0007?ðÎà\x0015®\x0005ïÀT\x0012TE÷X±ñ\x001c?F\x001dÍÅ×í\x0011À´£ÑlÛ-{þpÿÛïùj{:Tø\x001caÔð§\x001e×àka±ÓjÉåûpþö}¾Ü®ý\x0016"´SB»Ð³(:$[Çn©ZÛµÙÝ~èW ¦rµÑÄ
ËuÞ·Ó\x0012Ä8ErÄ¤ëp#§D\x0001pÍ¢\x0005)ë.ÄØÖUæ¿hë*O>|ûãëÓ¡\x0000Z¨âNÑçHò¾Êñgq©ôÃùë\x0003!\x0003
\ÂÕD©Ï\x000bi8\x0011ÉÍ>X|·\x0001nÌp;iÈ\x000e8 \x001eèCâÙLù\x0011j\x0013éB1I\x001foà¼\x0010N
c½\x0010.\x001anÙÃ²E^9½`\x0000\x000fÃ9åÚÜJþ=í\x000fOßþøíñùáÓ§Å:Q	e	RKb1l½¬ñáúüíÕíÅååòã8ÇD\x000br:µÓD½RÂ\x000cü:×fAÛ¸3S¼ï&Íù\x001fÌæÛÇÏ_¿ýÁ­\x000c¯\x001f>>ß¼½ûåî\°¶:6ù\x001fIµÐr¶9Ìo¯Þ}8ç×\x0017onÏOÞ¾>=¤'7h\x0004\x0016+±VÑº*M3à²k~¤øÆ]I_ÛSZü¹ÖG:Q	ÅÅÕÐlcµf>\x0017¶ÑjÓ¦Uó_`Zõ}Þ®w\x001f\x000bëÙão?Ý¼ºÿt Ý+e/±Jô ¬àpã¯ÂPÐì\x0001Ü­§o
èÙÕÛWç'¯Î/¾\x0008rl«BHl«\x0012SfsN`\x0012'Ð«0©-eÊ«)]l}´ü\x0017è£M \x0007ñïòùÏ®äòg\x0007]Gtiêz\x0019¤\x0002¨\x0008Ø6\x0013²'¨\x0000qvz
@v'ËÒN§PL¥^§¢ö=a#©\x001c\x001aõ\x001bÜXBÖØûÊÙWöäÃNÍD>¢zÄ`Îý²\x001cÄ0ôGaËZ\x0007OkØ*[3\x001c\x0006rÎµ Ô S¡Ç^Ù\x0019Àÿï?Ýý\?òé|Q~¼;´\x0017Q
åÑ\x0005¢<J<¼/6ÏÁ÷§gôOoòUùæty#\x0012âdjFÄ¾l1bà\x0008q\x0011¬\x0008Ã\x0002j°ì¥¥&¾¾q|\x0012"#¾\x0008å~¬)2<YO\x00030ö
ÆÉ\»Ìa\x001d1£w<Î¨ÈA.IÕàRÍÃZ¨Bû^@\x0005é>ûõî§§oÿ<Ð\x000f;\x0014¶Q¹*XÉ®ây\x0013í\x001cßÙ÷§¯®óSá@Iÿ7\x001anÄÓJÎ\x0007¬JúBìó:S\x001dÚ\x0011 r@h\x0000a\x0005 ã
ã89«\x001cki\x0004\x001bfÏr?oø¼/Rh1º|;§ÝÊÅÐ¦Ýå¦Y@#_@£¸´\x0012\x001bÇ¹òÎs?{p~Û\x0017¶
 ]\x0001hØÌd\x0017B;\x0019¥\x000bB[\x001c°\x0002°9ÂV~
;Ña\x001b%íÁÀ£w*å\x0019\x0019ÐY1 Zºúðµ¸²æUæ/nÀÐ\x001c ?$ºöå \\x001d\x001f\x0012[k¸\x0003l\x0002ÔjÇ\x000c7¡O$>ð\x000cx ë\x0011	kw ÖqÅìãxÍ=|÷¸\4Ý,
Ü\x0003Áñ$m\x0007ÜcS¹ÞnO¾»Z®e$;E²\x0002$\x000eeG.\x0001ÃvÌAîCòS$ßï0ê.Í¯"®|r/Yô\x0002Ö"Å)R\x0014 ¹RWW\x000cwòfð\x0001)Æµ\x001fnrãCsã\x001feÊ\x0017\x0001Ç½"ám|Ppn+@&bjö·\x0016lpSgÍâ\x001c\x001a`¦ú\x0018kuELÍ\x0006×\x001dî, Ó<NÊE\x0016á°Á¯ÝáºÙáZ°Å=çg2}ÁHÜ©c[½.\x0011R³Ãµ`\x0007Å¢pÐ\x0011õxÅsml&EI Ùâ ØâÁòÔöl¿y;yÅ£V1
±©5á->Î½Æé\x001eô\x0004ð<#\x0010møj¦f`gÄÛ)j~Ù¹dX¦GÁÌË®©Ùâ Øâùüs\x0002-zî\x001fÀq\x000bÌ´ÚdB³ÇA°Ç* %\x001f5\x0013"Suªñêýd=n\x0004{Ü)ï0\x000cðµÌÄÃÂ×\x001aLÓìp#ØáÖ±J76>\x001aº®)±9\x0007¾©ÙáF°ÃM\x001açk\x001es¼\x0000V¯S³Ã`çuuHéÎ¹:\x0008º\x0015Ç\x001215;ÜH\x001c\x0015ÏÒù\x001ax£\x0012ê:ùµßÎ6;Ü
v8Î¤a&ÏSËJbVß,¶Ùã¶+Ôz0£ÂÉÌ\x0014×î'Ûzâý{\ÅªÆÃ³©\x001b!ñ£jg\x0008©Ùâ¶+\x000c·\x0012)\x001f\x0011WIq4Éé¹XC\x001fR³Ãmÿ\x000eÇÒôÈ÷J|A\x001b\ÕUÒz-k6¸lpóÂ§zýmÒõVQVîÍ\x0019Û¦qÑtb\x001a·"
\x0012\x001f\x001f\x000e5ñ±º5»æ\x0014ñ\x0007Q³æ`Ph¼¼zs±ü\x0014\x001e\x0008­\x0012b\x001dÐ²;åòc¨çÆªpÐé)!Ö|
	óuHÙ\x0007i\x0012j«×¬\\x001bü¬õê\x00004j'
ÿb&üé§ëÇç¿Ý:ß3|\x0003aO\x0004õÒsÙ¼u&íï¼?½:¹¾ºý·óËcXveXtWcý²c*¶\x001as>M7Ry	UÞi¤Ób¬¡2ùà#OÐpnæj<e\x0007\x0005ÐI\x0019Rí³ëýÃÏ\x0018¶zõ¼\¬ì\x0012¡û(ÀcGu-\x0007I~>\x000cóþâ\x000c#W¯n\x000fÔ+\x000fãã\x0002	ÇE\x001fa~÷PG¨5+AY,:Ü\x00068úa\x0008Øøa}:\x001a\x0000\x001dS\x0008ZSÍ¨MvÞñéçsÍ\x0002º\x0015\x000bX«4dB\x0015?Úp\x00163\x0019;ûø\x0010\x00106+èä+\x0018\x001db[K´eCÌüë¨\x001f04K\x0018ÄK´êpÞÄijíùe²å#\x000fÁæI9aþ/o\x0012ÁwÙÂ`Që×Cv¸ JÉaÕ9Pì~ç¿O±f3U­\x001f\x0001ïL\x0004lÒG}^Î>$ÄHæ\x0000h8R\x0010]ÏS\x001f\x0007Ôi°AªT;fÃüõ~²ùí½¿{^¶Ñx_\x000cÃ«KÅÑP·\x001c
\x0014µE4´Ù48§)\x001fÎOo éiDÃKH\x0006Éó\x0018Ë¼`/\x000c¡ÕîHüûÕh(¨<]5+[6PÛç0¯`ÉâÖÃÔ\x0004d!µß3È0ª\x0008\ç­Ë\x0002ê\x001c\x000b\x0013yV£M¥'\x001a­)Aó\x0007k¢VV-\x001c\x0002®WM\x0013
 aÃ"6\x000c-Ð\x0007M\x0005¼bÝE«×Q\x0000hÑdç\x0000Ó\x000e¾hm
ÊhÜ¹dµÛf[4+C\x0003SÛ2°í&Q\x0018ûù­ÞðA'cå\x0011
C`\x00124íkfR\¬}&.Nl#B¶Ðn¶ Ûl*\x001a\x001a¶Ö<FÓq´³¦£)c3ªÙmøSÄæL	\x0018ÁË<\x001f=¿­Yi\x0000S%+Ø²7ücS0î±}wÿp \\x000eòF£\x0012*\x0016F\x001eZ£jÔÎ~ÍïÎ/«å\x0008	¦HÐd\x001c»F7\x000câ#\x0007´¬w³\x000bÕd¦HF°JÜøWIÑàg\x001cíS£G«ìÈ
xÆxD(¾\x0002YÓh\x0008Ü\x0014É	ü\x0008,zã\x0003g¶i-"ùn$MYeåß´4\x0017ÇèWó)O\x0010}5ÅQHËOÏìIµYýÕâ\x0014)ö/Q¨\x0011?]VÏ7
¿³WM\x000fR"%Á*%\x001e¹-n\x0007\x000b\våp<ê:¤i-%
½Ëä\x0006-Ì]\x000c¬îiÀ¯fjM·Àv\x001bàÊ @p²¼HnÖ{é\x0001j¬¤\x0016ISg@\x001c?ÝeÔûJ¦Æ(iUÊ·	IJa\x001b÷b-
ZÿÝ\x001a# \x0005VÀDnH:Ç=#µ\x0000jõ25GN\x000bÎ\¾i£­å.×Ë]BX»NÐìo\x0010ìoç<Yq\x0004¸
&\x0004Åã\x0003²[·Ö7fCÿ\x0016×\x0015J¢\x001ekV=ð¿ü¬_k.¡ÙâÐ¿Åq²\x00118kÔ°\x0005ok\x0004EHÍ\x0016þ-/ÒD\x0015
8\x0008ì\x0012[K;ûVî!j68ôop\x001fTÏZZ ¹
ÀµL¦Ùà¦ëäx\x0012v¾ª0¥æ]\x00142\x0019\x0012Ô\x001f\x000b(¨?ºL%¸Mi¨usèìEz­Dïj\x0017H0<ß<¹;¸D×°\x001d
Õn\x0010\x0003s0\x00189¡âOô6\x0012}*­õ
ÂÉÌL@Lè\x0015uX\x0004TH£äµÝ9Í¼\x001a\x0004z " þ\x0012\x0006àñCÇÈÂ:nzFÉm±YCü)E«z1f\x001eXdÛr®ÁÏ\x0004\x0005\x0000ÍF\x0004ïÄHÃOì¨¡\x0013;ÊÃ^©mû\x0010Ú³\x000c+\x000es>\x001fæð Ø,KÓk\x000f\x0016\x0019-fô;¹8\x001e¨X@µ2TbÒ<]ÅmGÅ6ºd©&Fº\x001b0r¿³²\x000bî8(át{oK\x0008}sñ§\x0010õÝI4Tß%J3]\x0011_jùäXë\x00174J£áP\x0013J2\x0013¢N3Á9\x0001¢3±)Â0BDãù#ëì\x0010{UÊ=]\x000eÞ¶nÌ\x001b\x0016Ä`ÅV×\x0011Ñqý~¾¤YþP¥mæ&ª\x0006\x0011
\x0011­ä·ç£h\x0015³ñN\x001c¼Þv£k\x0001Ý*À¡+)Ùüdu4,Rs¾ÄAyI\x0010ÛÃ\x001cå\x0019g\x001dòHÆD±8M\x0003¡±\x001b¿r\x000c
a\x000cbBÔzçùÃ´)ðFÄ÷Ù&Ä\x0004Í"&[ÄTs°6\x000cC\x0010{]ónÅÁ(Ù\x00141:¹ÅÑu+æ[ZóiVr³¹Ø~D­¡ñ\x001eÊo©ûå·ÃyÆ\x001e9]ÅÔ¼fÓÖÚ»Ñ×Q\x0007n4L+sk\x001e#[ð¹1í0/Àü?u±c \x001e\x0018q.ì#@öÀh\x0018­-'©òÖ«É½ÄCC½3[\x0019ý\x000e£x;j¬U\x0011ÍNÇÑ¿\x0000Ñ´_ºÔ¾Ë\x0010KMö`¾ómÇq~\x0017X\x0004ØÛm\x0016
­\x001fQ~K\x0019½&5®¼Pó\x001f\x0005Þnó\x0018µÙÙF¾\x001d®"CØ!N¿lÊ¸íS\x001bÓ.#þ"*ÍÒRÎÖ·u®"nÜÆÑ
¯j\x001c«P¯jGÉUd4¬èí[Ç\x0015©=2ø[Êh8{×Ñs	,êmÜ¶\x001d­j·#þ\x00163Fjz\x001e\x000cCáÄT6=\x001b÷£UnQx\x0011"£*©W2=z¸d¯¦Ç©ë¨Û\x000eþ2B¢Xl^ÇÀ-+Æ;þÖn..aö\[\x0010ëÌbL´ÞðMhX2Î{·É\x0001×6¶\x0017!þ\x0016"¢\x001c9½³\x001c\x0016	
\x001a"Ëúä·Ý2;\x000fj-~QgF\x001cÍ3ÔXá°N;øe\x0000ü\x0016\x000cz®lNÄèw\x0018åëò<¡2Rî\x000b0ÐÆÛü[\x0017bË\x0018¢1DEÅ®ÉCLèÈñ0[§#`L®5ø[Èè\x0003P)Á°5I\x0010
ÿ]²nåI\x000ev\x0010ÅÛÑ\x0007Ç\x0005bÑ{Êª<xfK\x0007K\x0018}kyÊ\x0011\x00142bñð©qRu`Q\x0017.bË_fÛI©=2ø[º\x001d5Cdß"àréQ \x0016ûü?Âoº	a"PÞø[ÊªQ´)½¬\x0011FL
ÛâP0i¼\x001f\x0010A¼\x001d\x0003J\x000f\x0001*ª{ex;m>8ì¼\x0013@üNÀYfõep&\x0007Í½2·£nB@¡±&¿\x0011åNx\x0008l\x001d\x0013¾¬ù½¥y;¦m\x0011
°;ÛÑJ·#>[}yÀ #9¡r4U×1mËqµªe´òç¿ÑünÍÖº¶0\x001aÆêKM×\x0016FÔL2âoiÜQÑô¤-Y,-â\x0018Ô#ÂÞ2\x0010]\x000fÄßbDWº*
b`\x000bORdÆ°Í:Æ¤[Æ$ÎgayXEÉ\x001c¦\x0000Fe=#Â¶¬eF
;ò\x0008³S²þÀè)LO¯\x0004DÜt\x000fBv\x0015\x0013ÈW1!4:lFNuDÊNç/=×yÑÏhtËX~\x000b\x0019\x001dN¤\x001a\x0010#kÄÅìÝÒ\x001eÜ¨-í)¿¥aò¥#e#(Ï\x001aôVF·Ã(0ççÔàò¤2ñvÐíÈ¶nÇ¹\x0002"\x0001#ØÆ(¿¥0¤\x00101Aw!jgy\x0019q\x0018ý&Ä ZÄ ¾b\x001c\x000e\x0001\x0018>µÉ­!'_`vOx£çjÃDfQ¾\x001dó÷Ä¨Ù\x0003ä2ãÆ#\x0003mö­ü2*\x0012ÈùAhi\x001dZå¼\x0001¿É0F·Çh¹uLz(êÈ$\x0004­£±Ûâe¥rÊ\x0018äEZ:oB5¬£ÇQï±\x0014Dñ^m«Ò
ª;ßÒ\x00003CÜ1éÒ6\x0010)^F\x0013\x0001`í2æOôc+=iJæKÆ{þ¸\x0007t%\x000c\x0000O°Æ^WIH\÷mÃl±àMÆ»½ÄFÜeáo"¢[ æS\Ì\x0008ÖÓ8Ð\x0010b\x0015«ô³·t7ßdf$ò2@Ë\x001d¹±\x0008{E..ª\x0003Þæ0ú\x0001'Ýå\x0003OÃ¡}Þ\x0006\x001a¬TÅá\x00044½ÅW²s\x0017K?_r
_rB¾ü\x001e£~,î¥C\x001cyÀ\x00057\x001b­íæ´þ!ß´õ¯/[\x0019FËÿ\x0006ÎÀD\x001e³eócm\x001bàè\x0015À©\x000bÖ\x0007{Ri>«\x0007%Î\x0006ZP³u\x0008ý>6>\x0001déC²ùÙ7¬`\x0002àau9;Ý\x000fÚ\x0015Lâ\x0015ÌG$ú\x00010?£©Ü\x0017\x0004\x00186\x001da;¦\x0001
f\x0001ûø¢§lAÞwÕ\x001eSbÎoÿ¹[¤\x0007P\x0016ÔüvD\x0013ø<À~þåéñÀ`Õ¡§&Ce¯·-\47øöþ¸\x001dÀNß½¾¾:0U¹`Ê\x0005".Ô{#\x001d3\x0007Üíát\x00157m\x000fËL¹+_hÔ\x0018½DÔælÂØ!ë6pÙ)\x0015q\x0019U\x0005jµ&Ý7gk³Õ[ÖËM¹l½\x0012×¹c¦ø å\x0019xÖ7:ÌR0?\x0005ó²\x0005óue'*VáEVôuV,LÁ\x0008ÌÌ\x0010ê\x0005[Áìº-¶Û­®ìÔT¼ºûôóãçÂvQär|OeKQ¥¯Ì\x001c×«ÓË³«wG±`\x0005",OµÍ1£T½\x0006Ã\x000e\x001cª¿­Ç2S,#ÁÂ^\x0012
3fóæíÅ\x001dtÎÁÜöêÄ²S,+Áº¹pµ¨è1ß¦®]å¦XNe\x0015{ÀÕ"±}\x001cåÉ«¥7`ù)\x0017­Ö\x0010¿\x001b\x0016Ë\x001d£ºm±Â*\x0016+° 5J\x001d\x0005à\x00127îõµ³wv'VbE	\x000b¬¯>G76;98¯x=UR%\x0011+b$e±T\x0015Iwþ_ð	§sv¨¥½\x001b+»¬ä
ñö¡ÅJ¬4çl\x001b/qµ6^dä½æm\x0003\x001c\x000eF\x0011ðº^³þM'WcäµÈÊ\x0007]n\x001cÚ\$'ákÞ]aý××"3ï\x001d¿ÎQZF\x0001WíÖïhâz®ÆÌkG,:¤èéu»óÞA5F^¬¼O¬0_F9\x000f;n.Hë¹\x001a+¯Ef>\x00065?;XÑÅ¢É\x001bîjÝØy-2ôÁ²\x001c\x0001Ë5¸^¥jèÕÍÕ\x0018z-±ô TIôÚ<+\x0016ÔÙ*N
ß±1õZdë1ÉÆëÅyÜ÷¼\«¡ ±¨ ²¨1°D\x0000Z.jôõàxs\x0019?÷\x0000êäj,\x0017,WÒ¬\x0019dtàjUox\£3fýGÆHÈH¤\x001aÈfªÈ:\x0017®QXoàj\x000e#\x000ecJ\x001c(ÆvJº\x0019½UuÄB\s\x0018=ì¼Êò£¶×Çç/'î3ÚÓÓßÁ0*Ì
Y¦FJp\x0016h}iìZû«ÛËó\x000cw}ýïÇÐ`\x00062´üUãp\x0003Ã\x0015úz\x001c$°»f"43E3ÂU\x001b2Nåsr_°uÀÛ\x000fÐì\x0014ÍÊÐ°¤\x0002\x00006pÓ¦Î\x001ar»¾\x0008ÍMÑ\x0010-#¬\x001cûø6ò\x0000Zô¦\x000fê§h^?'ÀjçØè9Ó
i\x001bÐÂ\x0014-\x0008ÑM\x00078V²IÕ¹_v××\x0017Å)Y\x0014Õ)-\x0018ã
ÃÄá\x0000ë÷<2\x0011Z¢%\x0019\x001aN Ì¡	,üg©\x001e.ù-sòtC««jR3ûeC\x0005\x0017\x000eÙà¦³ØÚË@x\x001b$[24eÙ4);eÆpë\x000fªË@\x000bo\x0003lÍ£\x0008u\x001d^íT
¸î;h"´ÆâjÉÕZ\x0008Ö,³\x00051{¯q\x0011ZcqµÌäâUú ÚÔF\x001dê²ÙÝ¸­1¹Zfsµ6´h¾Ô{EcÇÖBÜô=\x001b«e\x0016\x0017Ã6Ô\x000fZcÕU¢s\x000bXcoµÌà¢º0	ÐélEx,%tçEÛ\x000btØ\x001a«e\x0016·ÌäE3ç¤jÀn¹Ü¡1k 3k\x0018g!ùNM\x0013ÈÖc^7µç}w±i]ØÆ:øü\x0017/#GZO^}ûãîÀ8\x0010Ka\x000cÌì¢<\x001dåî\x0015o4=\x0013Ñ¸=yu~º8
$ÿ\x000fm½nìÈ';{v÷åîóã_ï\x000e}Â£Ñ^±Ü\x0010Ne§j´û\x00148;½9}wõÃé1\x001e;å±Ý<P\x001fMÚ&\x0016hBiSâ{áÄ^ ?\x0005ò\x0012 æ	áj½´òQPx&¢ãùi\x0008ã\x000e:ûõî·ß±Þì»Çå±\x0014XÏ\x000cU \x0016§\x0016\x000c;<EUý×ý´_¨~û\x001e+Î¾»ºXKA¶a´+\x0018ã8T7p_OJã\x0000Û½í%FL
b#ú\x00111\x0001·%c°'ºq"\x0019Zñ©#3\x001aÍ£¾RâY²ùnß$È\x0010õø2FDü)ftö\x0005Ï\x00004ûQ\x001aØÞ»D¥¶´k ]M\x001bæ­Iº×¥\x0003n°z%AÇöÝ¿É\x000b9{üò5_Y÷>-Æ\x0000$pb¢\x001a´\x0017à¢\x0006êÒ°·\x0013Ï®n>ä\x000bëüòò\x0018Ö8\x000c±\x0016pù¨ót8¿tà
ôËV{An.­\x001b.­E`Æð9,»\x001dtÞOÜÅªÂÞ³ª\x001fl<´\x0005Om\x0017\x000bCXd\x0006ìté%"0¿\x0017Âí\x0006q¬"áO\x0001rTøÚØ\x0014Ç:\x000cjlËÏ¾Õ\x0012Æ-\x0005,$\x0001ÅÌÅ\x0000oT6Çù^,{\x0008{!¬n0ãOiäSZ5\x000c0Ä\x0015\x0003*\x001aæf\x000c\{OÐ~¬ØbE	É7\x0002ËDb\x001cfX/\x0013(c;l÷\x0001Ú\x0003\x0006®
bµzÍ\x0011`\x0001üÙãóïÞ\x0012N¢r<t5&ËÈüo\x0015k?1ÅïgW·ï\x0017=&Â\x001a=&Äª\x001eS\x0017W¾(Ñ\x0013ç\x001dÊe÷\x001dn®±\x0013¹¬pyV×Ù±ReþÌefª
z¹&&?s9-áïÉìps\x001a|ªÇ1í×fôrf{\x0005ÑþÂéI´¿²A
ñàXÚ3ûjû9n®ØpEÑþ
¤6¹\x0002ÇÀÐ8mW|µ\©Ù_I´¿pÌ7[¯:\x0015%ëÔ¾ý\x0012p¹ËìDââÓü<ç®[\x0000®ÁKi?ÅÙ¥Ç0b\x0015Í\x0012\x0001"(ÇWÐçü%»Hì¥fÓk\x0010íz\x001c¢K»^éz\x001ay\x001cM\x0011VEÝZ/-3_C(#_Ù\(¥#GgS0ë¿áøª\x001b \x0004
\x0014G\x0008;Ù2Xä½µ\x0008è\x0007síær¢Í¥\x0015þààU2^ù)ÃûË¯2^Crz²ëó/ÔÑë§×w}øåä»»O\x000fÿ±ü2*µÖ¡\x0006^\x00022rKD6e3/£××'¯O¸x}òÝéåÅÿs\x000cÑN\x0011í
ÄÄ­kº\x00196ÅMÁíí8)¢"z9bÐ¤è\x0015µ|ã(NBt0ó\x0008!Æ)b\èy¹ÎV\x0006\x0019\x0004à:ccÓê\x000f­ônqiÉøùÏ¿¢[{¤Ãó\x001c]$8K1«SÍa®Ìñüì{ôk«&ôniiÑx\x000fXx\x0011©]\x0002\x001bì\x000cq¬;Îx¶ý`f
f$`X[Å}\x001cAe9µa2é¹2Ú^0;\x0005³ÒOé(°}H\x001eÙh8k÷V\x0002.7år²\x0005«ãË³¿Á
LÞò\x0018=;[ÓËå§\^¶^i\/]'2PÇúÌ¸\x001fý`a
\x0016d\x000b\x0006lÔÀë:úÄêº`³_½`q
\x0016e+\x00169\x0001æ¡ùºÁ|«ZíåJS®$[°f@\x0013%®½åÆ^´N°I%¦¼Ï9n®òõSbå\x001e-«î%kí¾Èðòu\x0014M)kæê¹jÌ^²Æðk¡å×u¡\x001f\x0019Xàî	;sa
È\x001aË¯e¦_Ã\x000bþéE$\GnÍ8àý\ÕB\x000bkÙÅ@0®½¯I³L¶á`êÆi)C\x001bËSïªs&kïu{aF	Yc2´ÈfÛwc½Zoª.ÛrCs2AèÑx\x000c¦ë\x001cLH|-Ù¸ÁA³ýA´ýq¾â\x000eÖÈ­iÓ¹åÂæ\x0000è\x0000`¥\x0006õ-\x0012\x001c2³P/ùæÚãd»\x001dÚ¶îõãás\x0019"õå=¦h\x000c±\x0015k¶\x000cÿüìª\x0003
¦P ²ËÝA'®L3´{ÅýPv
eû¡pÄá\x000fèê(ÏÃ¶¬Ù+Uêò»Ï¿Deÿïÿü_ç\x001f?=|9¤\x0013ëè%úF;¾jØ¨çb.'ço./ne\x000b¦\ ã"é¼DWì¸òm6VÜ	e¦PF¸Xª\x0013Å¼/w5eÑ[Àì\x0014Ì
ÁR¯q6\x000fµ\x0010.Í<ºÁÜ\x0014ÌÉÀP"ÇyÇr\x0002JÿP5\x0010\x00016ì/?\x0005óÂ\x0015\x000bµ¶7¨:¯\x001a?e	\x000btÅ)X\x0014\x001fH\x0006óµ\x000f9ÈZáâçbÆ}`SOßO<ý>2\x0019ÁM\x0001ëzc¬:J~.ãu\x0014,î°ØÜ@ÿøüðíO½ÃÄ:
Ø$Mâ&ÞÕÙãv¯j°ØÖs{q~}È¼Æ]3\x0016¨
#bÜU>pù:\x0011yÁÑéå2S.#_3EÝ¬ÆÔÆ>gÆÆòY¿µÍNÙì5ãîòú\x000cñÀ%5ó*\x000fÝhnæ¤Ë\x0016kË©ZS¾õâ°Â-l~ÊæåËÆÝï(\x0004¼nüI÷\x0012ø"´0E\x000bR4E"û\x0011ÕÎ(â«â
3é9\x0001[²Eù²\x000fkcÉvÛ«E\x0012¡¥)Z/\x001b\x0015é9¬\x001a÷®íL0ëF]\x000b£Í}>ùîñéë[@;
ÀûæM;ÃËeã~(êöä»«ë\x000fÇp`\x00038
K±¡\x001eHÊdÚ8¸8fczWÇù18\x0016°Glý~,¸\x000fÇNql÷êØÒ¾JmÒ4tÌÆ±ûq¿­¼\x000fÇMq\ïêPfVR°ï#GqÜ¾kÓGã§4^°uX~)¹qqøÜëý`o\x001fMÒÄ^\x001aK ì\x0006Ã-z¼õ~ µ\x000bgâóá1W½ß
ÖÇô\x0014uØ;]5 Ò¾<H\x001fOsÎuïAG©VÎe\x0004*\x0019Åþ(~HÄýhn\x001fNs°tïÉÂdl.Cq¥ö\x001eÞË!®\f/ëÞÍ¬!TA\x0004¼a©« fÆæª{h½¬{73\x0012H®A²\x0013é<µÎì@³¡{/8H:\x000fácRepù­O\x0017!\x0019êôF\x0008\x001dÀPqÞ<Ý}þåäòñãÃÛ]%Í!!í\x000fõ\x0013)®*ñj®\x0006ÿÍõé»×'Wo.¯÷\x0001n\x0014=G8ç¤p÷7Î\`íC®ÅñÚÌ,Y?Ü8O\x0013á|Á¡2ãð>°ºöô;à{\x000fûy
\x0001\x001e5\x0011N+%¤Ã\x0001\x0010g-PçëÚÁ¾\x0008O·xZ\x0017Ê	@<\x0018\x001d8OÖ¹~¼qªbÁ3VZ\x0012©â9VáfSÔß\x0017Z<á¡ÕAQ\x0007±Eá3Ãz8éâ­\x0007Ë1ÓÁävì¢CýTR.±Uj,\x0014%Ïn?ò-¡æÓ\x0002\x0008?-JIPÌ\x0001\x0005}I\x0014*(Ï7ÛÐÓg\x001a£2Ln\x0015á9öx°«äUp\x0019á¹¹k¢\x001fol6*xf£N¼ÈmõÙüò¸¨ ¸,Çû}U\x001a	kÌ
8¡YÁ
\x0013êÅ¶(²5øA·ÎèÆ&\x001b-´É\x00103ÍðmË\x000c
Z¼ê\x0001\x0004½'Í!ÂsÍ·5Nøm®Uè\x000e§\x0015º¨X6*ÝbULhéÎÔ\x0015\x0007uñP\x0019\x0017o_ßT7\x000eÃ,xÑ\x000bñ²¿KMã\x000ec9MæÇdgs¿<WÚ­[Ï¸Ao»àÕù
ùrãÕSnËÉ°ºù¸VK?np|e8\x0000Î,ÇÀQÃ çB\x0004]x»Q&ÓDöîã¡èÂò5jQUcTsêÈíwaô\x000bÉÞ\x001c}Ý`ibúG©Ð\x0001 Ãã8XKÕp¡¶sóN,3Å2\x0012,e«\x0006±N|F]M54\x0017*ì¤²S*+Z,Çq_E0¼ª¬j¶Ò©\x0013ËM±h±\x0012
Ù
â9ãjmø~å%XÑ°:
¶\x0012Sâ¯Jýª¹rN¦0e
\x0012&,P\x000bu©(áQ\x000cÿ\x0005K¦XIHõbÐN£/èªô\x001fÞ¥[%±Y¨¹\x001dFM7ÊwîÎìú¹\x001aë EæÁ¸îÓ\x000bup~'sÍÖNwr5\x0007QN"æ÷t5ò@Ie?êÎd»»¹]¯EÛÞ:\x0019ÒÌi\x0018÷×lY_'W³íµhßOcÖ¦\x0016(ëQ¸a¶¨õ\x0018Wùcº¿òït}ÿðôøùc5j:Ô\x0017©3Nyþ\~Ýí\x0007ý2Ú÷\x0017×Wï^\x001f®R\x001bð\â¹(ÅÃÙJü@©©[\x0017Yn1?Pæ¶Z?\x000fS>\x001f¤|6±Ü
µÑÅúü; ýt±Y½(^=ï*]R/\x0002«_s¡OzÎ°uó¡&Åtó\x0018\x0010ý2záäO9\x00196ò\x001bjöÄ
\x0000S\x000bÄ+è9&o<K¾\x0010Ý\x00063{¿÷ó¹fûÑ£Â\x0005¬BInì\x001c÷Õ)Úüñ\x0005Ûð\x0005+åKÆ<G\x0017\x000cW*Z.òÁ©}[ø\x0000\x001aë\x0007 5X\x001aBzç^§\x0017\}Á
Þ¨¢´\x0012Oï¼£òÿä¶Èóûoÿßï\x000f_\x000f©i\x0005Trm²©ùqÀO©´\x001fÙÂÒ­ï¯Þ_|X\x0016
c2\x000cÕ"©MÔà°q\x0016\x0017dW<Îê\x0015ô¢).\x001aN1òUÛô°©5Riÿå.`³S6+þ O	ùéÇï½Ä\x000eJiUêgsS6'e\x0003¨\x00155\x0011ê[ÔúºÝfêVúÙüÍKÙ²é%ù`\x0013ê\x0000\x0000ÇÓ4óºÍtRõ³)[\x0010²a\x00016él\x001a\x001fJ¥q	¡Öu\x000bó¥lqÊ\x0016¥ëæôtÝx<Nä(VÞo³\x0015ÆliÊ¤ë\x0016ÆI\x0013ØN¨\x000b»\étéfDÑð*)\x001c>\x0003«yã.x__õqfàD?[{)Ho\x0005TÐ#oãLÝpµ­ÊÍµUõÃ5÷^\x000cËJôÄ÷©vû&\x000e\x001d-\x001bN7\x0017Þ\x000c8_Ê¼UÅ1.\x000b\x0017ê ²M;®±¾Zj~ñ«òÌü¦¦ØH°ª\x0006Ngf\x001c3¤2Y\x0003\x000e'I³è»»¿\x001fæâÛ*_SÜUn\x0003¿\Qsþå»Ó_ô(¦)QLÝDJ\x0017¹q$\x0002Ïp«¹O(íéT÷\x0001MôbLhôb\x000e\x0013¹ÐË =ü¦7Lþh¦\x001b§\x000biÜï\x0005iú¶?¤¹\x000e$¨:yÕDOÇ0¦ýB>¤v#éÞ|ä8CP¶Z Rµ\x000c1ÍÖ`÷ ¹\x0016Éõ#	@ß?yn93?\x001cÚ×H©EêÜÝ¤ØDyì¥òÄµ\x0000ø_d[$Û¦$ù²kM\x001d©Æðè8\x000cè ríVrý[ÉÖ7[ÐÃiÆrßTj=¤\x001cNßIB8ÿ#L\x0012ÂïïþúðéÓãçÃ5\x001a\x000c¢3\x0006û¨*±æËLSÞíÉûÓ\x001f../¯Þ\x001d\x0001º\x0001Z\x0002Fãµ\x0011\x000c4=q]mÍk&\x000fÜÇe&n}æ*A?\x0017\x0004Ö9ÕÊpÍ3ü\x00182ÖÎä0;ÁF¦\x0002æ@\x0002\x0016\x000c+*ãÄ\x0006\x0016{N=1°\x001fsì\x0006\x000bÍÄ\x0002°üê¦\x0015SÑsRzl3ûcqúÁb³÷ËÐÅn°I§¿\x0013\x0002£\Ù\x0017&ëçj·Xl1äª_RqíÒ¨sa`?|×\x000bfuó%­|IÙ¢$o!G\x000b\x0016ØÛ3j¿\x0005»\x001f\x000cZ0ÉÞÇÙ\x001fBQ\x001eJÆ\x0010\x0010ã/©öç\x0012væSâO\x0001X6úTç¥\x001cª_\ø\x000fiÿ²î\x0006kí¾\x0015Ùý2ÏÀ°¦%q\x0017ÅØ!ÎÕ÷¹I¸)CáO\x0001\x0018æ#èSªÀ0T}$0·þTº,\x0002\x0013áH/êoQ(DLï°Z÷\x000e³Òc½`¾\x0005ì1\x0004£©\x000c)q088\x0016~=\n'\x0012o:²\x0015ï\x001f¾Þ\ûã¯÷\x001e>\x001fèâü°c«x
Hhn\x0015Ø\x0005¿¿ºþp~r}þÃùåÅ»åN^·36\x0002é@LçÊÈ\x00083L÷â·:i&îÉ\ËàÌ\x0014Îá\x0012ª!T­wÏuf6íõ²Ëàì\x0014Î®cí\x0012Çêø]kÏÅ¦ÎMén=:ÒÛQ"mÛÚù)\x0017ÓA-SÂ\x0006rn\x0001µËÓ´dtaJ\x0017VÐ±ÄWõ÷¡*\x0002ì\x0015þÊèâ.éj\x0017\x000brG´¯\x001dûª|2º4¥Kbº:´\x0007Û´jOtªmZ{%ç"ºIp\x0018m±âa;ù@§Lí°u`à~¯®½)ÄW\x0005Dn¹ËN&E©50\x0018WßD×Ü\x0014Z|U¨AÕßÐÄ4Ö·âÈºmwnî
-¾,ò-^>\x0017TqýòXÏÅ¶Õkì±\x0016\x001bä|Ñr\x0019+.dÕÌà»?oN×<-¶yZWMÙäê\x001ceê °½\x0016¯^¼Re&6\x000f'%!ö»\x000cùüåëýÓa	É\x001bË¬ÌJåa>å#A¬b\x0018Ô]~u{óáüzy^\x0002áy7ÅóNGMÖ>[¿A9Þ'ÇºËXÐ¶
Î7p^\x000c7´ï\x0016>C/|<\x00083\x0015¥]|ùÄo[íJþf|³^ã$µ\x0003n»AÃ\x000b7¸É:RLub¦N»¹\x0001X×ç§¼öjÒ;TÓÞ©ãXÙ\x0011!ÙÑ\x001aÂ
@\x0001A\x0007q®á±kl\x0013-\>Ñ\x001e.KuÔ	û¡\x0015sQÂÚ\x0019=×ÔÅebû\x0015£ä3ú¨¨&áa\x0013ù\x0011Ac\x0004\x0019êÐÉeÇ\x001b\x001f¹ì¤\x0011©+\x0016uÂúÁÏÄD&í¯lÖÖî/k[.+âJZT\x0012ö4$úFÒX¿/kÖZ¬$Á
j¨ÍÏXÆ\x000eaÁr\x001aé+:½¯\x0012ÜåÚ¯èD_\x0011±hµLþÃÜn\x00175õá¶_»»\û\x0015è+\x00069ø+ñLàÌERþÏ¾Ä`/Wl¬\x0004þì. Ìo²&\x0015µÁÁ¨Ò®Ç\ÕJ.oõÂ²õ\x001a^ÌÉFKÁ£¼^F¬x³/Jtëÿ§î]ã8uÝWÁì\x0004ûÅ0\x0002)4\x0017×\x0001	6@Èz"+\x0010\x0005	\x0004( $Ök¬Ù±3Ú½\x0007g´ß@o²ä¸{¸geV¡23"«·Ùnk$Y\x0010E}_~·\x001bõð¶ÎùÕÍjªDVzÞ\x0001\x0004Û=Quu<þ©Z¶óÓãÝXdúHf>\x0012¼³(YIª»\x0006äNò*nÇÉç"Ù>\x0014£TÙ$aòh»Ô'½~ó\ÈÍ'
ª{o6J\x0017ó¨»"÷T g\x001cI\x0005Ê\x0006éU5ÃåÚ®£.V7«÷w#ÑÍÄÞmÌåðÅ!vy7\x0017õ\x0013)³\x0007\x0017Ç§ÇßMQõ¤/0ü\x0017k¨¢x¹=Öa1QA¨\x0008\x0003Ï¤
©O\x0015R\x0005Uô¢ce¬µE~ZIÏ~"\x0015j\x001eUô}ªèë¨8ÇÛÎã\x0008TY¨ò\x0013Ù±³¨tÏÝ\x00180¯ÍÍÇÊÊu\x0015·h\x0002\x0016ªNU*>Ùûl&\x001fRÕ\x000c\x0016\x0016Ä\x0014\x0005\x001c*Ý`\x0005¾}°ô`bi]1³À4\x0006$\x001e¦>;\x0002Lî\x0012ÿÃ\x0013u13±Ìp´LÅhÁMBnØ>$\x0011Í4)IEü{b63\x0003*gj\x0006«~XZV,
ÀcÚ\x0016'ÄòÜí¯;1ÈÔ,ÿî
\x0008î\x001fJß×¿þßÏW«Ç­\x001e\x0015ù
bèÄY,Þ`\x0002ÙvÎÈw'ðñü»¿¾=9¾À]§Ù n?Ë¦\x000e×çCøîØÕºb1\x0007Ó>©óYM\x001b\x0006´¡Ö)\x000e±\x0000­îáÑJSóD½\x00057\x000epc3.ö¸Áµ]ª%»2R×kí­'O½ËL#-Öp%v#À^)ís¸\x0018\x001bþ­½L\í\x0007ëLûÖ\x0015]^¼\x001e^ºH\x000cî\x0013ÝÍZxÃëÛ×rKP\x000c]£©\x000e÷
¸k1\x000fÂv\x0001ni\x001eUèr\x0016í÷Éô×jÜuOZÂMª\x0015\x0017»òlð©«|5\\x0003¸O\x000c
¼9\x000exs\À[z\x001cµ¤¥\Mv\x0006ýdyz-¬YîèHS©\x0015Ö\x0005öÎ
C=ÒD¯ãê¼Õ´f°Ðhsl\x001cZÝíºÍ ¥§\x000eÛmûZx×nâ
¡7~NÆô\x0019Ûæe|ý©¸Õ¼q8¾±u|)×w\x0006e¥¶,$cWíe|ó`k0¹ukÀ(ª+/eÖÂ×|
Ó÷\x0012\x0016Ü¡ý
H\x0018ñÎ`²ø
D\x000fp·\x000c
¸V\x000fö\x0006«[÷\x0006\x0014:Ë\x001b¯§¢CòÿHçfØ"÷±ñZ¼Í6ÊÙ2nâ¯âD\x0018äÝÅkÝà\x001c¶®õ\x001cÆñ-×V¸ODör£hßÚBo\x001f_~xüí÷?¾g§$º"Ý=Þ\}YÝ¿'ÖoW\x001f©ª{ÚÛt$Èß|w}ss\x0005Ï+ü\x0015\x001049Èd¤Ó\x0016nùE\x0007 f\x0013(æp\x0018áËÉô
&´Àó\x0004=zvvyzòÝñù·ô\x0013|{üêéªgþòñ/íb5<ÿùêãõ-Ç\x0019Ñ\x0008__Í\x0006Ý%`:\x0019rKî\x0016
-[æv{1<ÅýüßN^½|ÍaÈg4ð/B\x0002¹»}x¼û#ô\x0014ïÿ÷þ×ÙãÍLêI&\x0011{ÊAÛb£áÔ(Eå\x0011¦\x000e×MP\x001fàÀO\x0003Ã®_3)í"°Ò¥ô\x0017uIxÇÖ×{Ä\x001d\x0002¿àúeñD[J¯Ö\x0014§\x001fÒr\x001c/¼(i_KxáxCËæ)U¸X\x0012R7\x001föÇ\x000bÙ.¿¦èh\x0001fØâ(¡ÑKi?ø\x001býõº·¹­aßÜÿõOØ~W\x000f¯n½OØ`JÃicuil|lähUtÖs>ý8õó\x0013Ü/Þ¼þû\x000eöðþ_>sº\x0007%y0üÅêúöó7ÏV÷·«\x001fÿúç|ô\x0014¾*ìqÖ±Brp¨Ä²ÇaÊ\x0014úÅñË×o\x000f\x001d¿>~¶kÐ{à0CZ\x000emW\x0019Ü\x0005\x0000®uæApµgp¬\x0012My9¸MÝ'\x000eÃ;Ë#n\x0015\x0017)ï
\x001c­Î¬sæ
\x000bµñ|\x0016Z\x001d&\x0017f%5RøµZð1\x001eâk	Ü3øôÒ¬âÖ\x0018O¦ÇRpWÂo\x0008\x000e7*re\x00018wV¥î)ÖG%9nv\x000f\x0013Å\x0006\x0011¹¦ä(á¥ô\x0003Éí^føÇ¸ºùõÓÒ¹÷öîñ~¾©aj²àih\x0018cJå\x0011jIæbë½=»<\x0004ÆHÑË}¦Òj$N¾\x0004c¸$\x0002£¾¸uTÎ$Æ\x0019m7MêJbÔA÷L\j	{#±iOÏ#\x001fßÆÄâpHuéÒÄl;\x0001ñ¬}.1ºt\^F\x0012%\x0015\x0010±+]ÛÇ0ËÖ\x001b`:eS\x0002÷\x0007ôkÐàfCËid8ÀnË\x000eãqÙ²sª¨)Ò\x0000ÇÒÏ\x0013S©¬@YE3ë¾2\x0018½¨yÙ$v>¯§D,IïpsÛ>jD\x0010öGL­/è±\x0004Ù)*\x0010¡iQ¶	k\x0012OaânwA=/\x0006°è±7&pÈ\x001b»Ug£ÕrzÌõ\x0014 ;ûñóO\x001f¸¾\x0005«Z^~ü´zxèT^?Ü_Ý^_ÍÇÆ³¼\x001aYÌ\x0014ê\x001e\x0016ì`üî#äå«7Ç\x0017\x0017¬\x0003süâüäõËit¼\x001cã×\x001eØ3e.\x0012{(.F`÷E`\x001eÙGfu#»=¢åìX±X¦Kú'`\x000fl `ÝÞÇ\x001d\x0006\x0003¿öÀ	\x0018Ùa+ÌÂÎ÷.\x0018÷{W\x001b»8A³[Mn^3¥Õ	 'öC\x0002ºÝ½JÛÐÑÃëö2eàÖ\x0018ÖÓ]1{.ùSÈ\x001ew\x001fmìr¼/g\x000f%¦{ÙØ\x000f±¾ßhîjßK5ÀÄ¯=°+ÊÜ!vKY1Ä.6k°vïì°~ðk9»Wiìx%ó]%¾!\x0004·÷í\x001dãq/ãî|·TMÑ&#vÝ{ÞíÅncÇ\x0004uüÚÃZ--;hÜ]q\x0011ã>Ý\x0018µ5ì¿
auÅÚGýa<xv¿zïÂÔXa­iÛì¸\x0010 )ì¼[îìyÄªí/\x000f\x001f_ìò]öháÕÙE´NSSP¤µE³êk<\x0000UÝ²zV\x0011~\x0011«¢lW\x001aØTâ~\x0002ü=\x000e¬\x0016ÐÚH®\x0004Ä¦\x0008¥\x0001n.)(C4g¯Ë~ \x0016ñFEy=Ä«K¦,Î[¾@úìæsy#\x001cQ-âMÊÌ7'ÙO²Î¢^<yz¸ùÞ\x0016ßß\x0018óÍ_ÿëóì
>§`"pq\\x000c;©ÂÁ8kG»<x~~V¢Ï§gOöÉ\x001cÀ£\x000e·û \x0007#`0K:k\x000c0æéq\x000eÖÑkZ\x001bk±
\x001f¥jQÙ\x001f\x0007_sÀ\x0000ð\x0015|÷5ø¿þñçïîé{\x001aöK­rD¹ròáXîè'Q×Á¸'{ÔÛ}!îÑ¦#j4ÛN\x000b&j,æ5VËÛÌ8qôÍÛ¥çÁr\x000cº\x001d\x0016ìºÈÞ\x0011e¸\x0007Àj%\x000e\x0012w»ùjiÅSÝNy­ì~;{9«ñFüÔÆÍ¸uÒº¿|ý}{áÍýêóÃÁ³Õü\x0015¸}gÎûÐI\x0017d},ÉaØNl$\x0008Ý³ßÞ\x001f¿½8xv¼+ae-6ÝblìRÈ¡.í
5\x0000î`8Âk=g¤«¸·¯·-Üp¤\x0012\x0011EíJêr­øØã5]çöÉi!,&©T9"·-\x001cçdVtÊöI]qñp»\*P\x0008[ÉpS?\x0007Æv3L
n,\x001e<¢ÇÒù]2ú\x0001\x001c,ÒÒí\x0006ÕÛ#¯KåÒnÇp\x0005ø×Û¯YÿAö)^T&\x0008­îß×Åé,Ínç´)ºßý¨ÉqÖþÿàøüÛif×6,dÆf.å8t¦\x0017÷
ìä³díyû\x001ePÏ\x000c×\x0015\x001efÑc\x0013YÕj¯È(záýBdç)q}7ÌÆ\x001a\x0019æ<ËF\x001ag¾ûÉ_~(b¨$öêîöó_ÿ,\x0016éêÏûù©YÊe}a\x0005>U %\x001a¦Hz$%áÕÙë·'Å\x0010=þþ|WL
\x000e\x0007üj§ÅbXh1ËÍ~l\x000eShÞ½]ÔÒb\x0003Oüj§M\x000fAïa&«2¶[5#íÈ«¦µ_\x000bh=åu0-eÕ`¾´\x001dín\x0013´\x0016µ¹ñk\x0001m"O\x0006Ñr3b¤-\x001dØv$V46|ùñÝ?ö
û°w÷w·W7sqñ'a½ås.f£ÄG\x0010æÍÛ³ó³×'O¶f\x0018ðbÞVË£§XàMEÙ\x000fxuR|.\x0007owßæ\x0002¯Þÿ~÷\x000bù\x0005PàÄõ§ÃÕÁùÝ»¯~¼¼­\x0013Ö³ãÈ\x0007e½%/ËMtÉÇO\x000eÎÏÿÛÉ³óË§ÅÃ\x0006ØâÖ_
w?ÊÙJbÀæè[Äòþ=cséBl\x0017Ë\x000cñ`ïLz¤ÖL\x001dÓ~©5-B¥\x0017cgCm#['\x0019ílJ'\x000b%#7
ðôuuû\x000b	iÊès?\x001c|w÷çêÃÕãýLS\x0019×#Ü¹ùfú¤

×W¬¬È9³ûâà»³ï_\ï²×Ü[§u\x001bw\x0011i¡Ä\x0017$Äæ \x000föô6]GÍååÔ©é1É\x000b¶P¸c°%Ë~!v(ýj\x0011\x001bæyH\x0005[\x0007$qÄ-ZÁíòÃ/þçÞÑøæfõÎ\x0019\x000f^­î\x001fà×`fc'\x0017Ø±\x0008s»(?ÃgìrËØÎíÛoNÓaÿéãóòä.nôÜ6Ð]\x001b¹c fwÈ­¼59rínä.q¶Ü¼aÓì\x000eÔû\x000b§	Ûü\x001e£ÈûÆ}Ä-&-T\x0007%IZâ4$ä\x0010õnïL
÷Õ×¼úøñ©éM÷Á\x000fóëÍTÎ\x0012
)èíKÃ\x00088ñ%w3åªwÈt\x0019|±ë¤éÑnLê\x0006Z#é¼Ñ¦C\x0015y\x0010ùªýÐnLåzÚä¨®\x0013iQ0¤\x0004ÞèVUpýù0\x001bwc
×ãFÏN:J\x0011%®éõ:gfä,¬Ç-Aî%¸Ó\x0007(MÆq&¡ò¹º»¯\x0000õ¸è¾]\x001b,Ui\x0011®#\x0013ï\x0010½\x001b]þÝ=ZO[¼.\x000bh±\x000b¹ïæBñëÃ\x001d^¯÷ÅS7þþÛûÏ$gMÕ¨±ÚÝãg²;¶¿?^ýy?×aK;p¢à	EsÑ\Àb¾ÜEÃî\x001dâüìò-\x0019Ïü\x000fþ~yòýùNí_RöÀ\x000fWD\x001b'Ìêµ\Ê!LcÓõßÎ\x000f\x000b\x001a]ïß¡,\x0007âÃÁB©\x0011_v<ãÝm¶ãÃ>Bruñm¥l\x001c\x001bfÂôñFâÞÉíÞ\x0002ÛùáïÄ¯=\x000c¿w%¦üýQÙ(Ó?äTµóÃV_{àwE\x001boiDÎÚvI\x001f»ï\x0007ÍüX¶ö³ýxKê?öaci¤ü\x001c\x00110&ü\x000bÆ_cO\x0002zìá\x0007£÷ÏlÄòJu\x000bØ¤PTþ\x0000_ì/|\x000cý,÷ÿfuðüúózÙWß¹Tqk\x001b$ý\x0003ÌoÉ\x0018òADùFÙO\x000f¿|{LÍî'Á=¬Z\x001f\x0016c\x0007¹â:	°ÿ§"V¡BækZTaÆ¬©\x0002ª¤àYÓ\x0014Ap_â\x0010\J©|Ô#ÜMà\x0016ÛÓc\x0001¹¦â\x0004uXrâ\x0012v¦+CNÝ$\x001c[íîv.z,%\x0007ÀâBA\x000b¡ø5³ÓZ²ùÆ\x0002xmä8ûè±\x001c\x0005JA\x0001*¸(ËN\x0012=ÍÓ¾	Ý+ã¨åè,k9\x0012Q`\x0017HK¶#7Ï6t\x000c¨Ócñ¨\x001b¾ÂºñÃ£8\x0015Ñç _\x001b9ê·Óc)9L\x00128Ù\x0016\x001c1skà-:öLÝ è±Üb\x000b6\x001es¸÷é²HØa>§Û6t4ÃÀ
nD·"S¨h§ArîÏ~»ï}Mà$ËN¥à(\x000eX¸áÆJ%\x0000\x001e9<\x000c³ÆígsùôûÕêö¶ª#à\x000f\x0007ÏoVÌOÆÀvsÞð\x0004çä\x0006l±\x0015xH·¹1äç§Çÿ1	»yâ×Ã¢PRæÝ;~¤\x0000+Ù\x0002\x001eïÞû£E\x0007F\@¥ÝË5´#SXs\x001dëH\x0015R%ê:î×Î\x001a
üÛl5\x0017Úé\x001cåpeÌÅíÄÛqH\x001f¶Jw+¹|Ø
|o´\x0018\x000e¢G;­÷b\g_Dà±W%6Ví_K> Ýw\x00045ÐF¾Ã8¬&U@\x001c[-fFÚßL@#=ÚiÍÚ*ÂÌ\x0000¦Õ^9;ãº;\x0013×`\x0015=Úq­ãde\x0007\x001ft¶ý\x0019G
jqÑr3}ó­a.(ºÄ\x0012n,Á\x000e¹VjÎð~¸/Z\x0003Òc\x0011­bZì\x000e\x0004WæBLÓ®¿q\÷Õüøc¿öp
õ\x0001\x000f\x0007ý?¨¤6\x001aãK\x0010áÒj%Ù":öv\x0018\x001fv\x0007\x001a×ÌX&pqpn\x0019ìÞ¦vø\x0002\x0004FnÖ5FEþ\x0016»^îáQõ(í\x0001ÞbU6¼×EK\x0001ó:uG¯æìËUô\x001a3úè±\x001c?¬Ç>èb\x000cQuî\x0006únRÇßÇ¼·X\x0007èxô½LÒÀÆ~_Óþæñëë\x0015éæb\x0002IÏîx<xñx=3ßÌ{,I³ìkJìÌXR'N2?9a.\x000f^\¾Üí×¡:4æ\Ï¢«EuÎs\x0001?LÄz¸ÿ?ÏL»hæ¢b5²í¨>s]\x0017\:¼xðbÎlpD;í\x001d\x0018EuêýÝ¬\x0010¬»¬z¤¾é\x0011\x0015Ãý´BÉùÔQ&ÀA\x001d÷Hw°\x0016MNÛ³;+iÉO
eÁ\x0001nDy·âv	Az5RQËëÐÛâz.\x0006^l\x0018SÔm,ni¾ø,¼¸,\x001aQJ«åõ¨¤@v^¸+É*Ã\x001aUËSW*\x0019<üî\x0011\x0018Ó\x0015²_\x0002ì°O$»?±k\x0011ÑJÎrvgUðFä]4QvÌ²§Y«Ò\x0006\x0014yÅq\x0008\x0017þý\x0001SÂ"=\x0016\x0000\x0003VIT¶	.O·Ýîbj÷«\x001d\x001a³åÙÌKÂ\x0007\x0004L(-\x000bQø@î¦ô_÷DLçåÙN%C-ÎÁXnPÊFqÇýM	±<µ<Û¥÷/\x0002ã$¦pm
;òÓÚ|bt+ç\x0002â DíJ\x001b]M\x0013Ê#3ø½Í
£ð+Ïvâ¨£îÁÕs\x0008á÷<Q²rÒMLM=Ê³Ø`S¡"9âl%Y\x001dÝSÝLcLÎ%Æ5WíÄØ.Â\x0006&Î¬=g¨üT']-óÑQ\\x000bmæÒYgÁ´dwqJ2Ä)îÍ^3\x0001[
ç\x0002àXö\x0007\x0004uhîÔmMØÅf\x0002Ö?ç\x0002â\x001c¨­,\x0012õÆz¼°\x0006eãRX5q¦1^d\x0003\x0019k-Ûð@KF:Jtð-\x000eÏO¿~ùécìË^ô#Kç«
\\x0015(J\x0014¦ix\x000cÝô  Òùåñ$-f§\x0018»÷a¥­}Ã6Ü	\x0013M_æÓâü\x000biµØ\x0012%íhS'S530=VÔ.\x0016Ñ\x0016ù/ U¬[´2¶fDB¿ÚÉ²­¸ÆNó)j 7*j	$¨éãb6.jµÐ£\x001d×(\x0016³\x0005ÜÄÝ,\x000c^ñ\x0018W´ë©Åí4çÛqÁàáØ"OX¦õBkö·+¬µÛimiIÈF»-2\x0005j­ÿe§Ù¸[!°j\
JÝË´ZÉBófF
ñLZ èÍl²:Ú´)Ìò`I.J³7Z.I£L\Tî"`^,uÌ[\x0015Ú=â¢t?=ÚqÑÒå\x0012é\x0003v1Ë\x00059ïoæ\x001aKÇïó\x0017\x001b×²¶5êÏFÁu²/äéÛñ|\ØÙ%Æ
]øH\x000b%up¥\
«L÷¯Yt\x0002S\x000c¶n¢4±\x0001Ü.3iL\x0005¿\x001a\x0017m]·ä\x0004F\¶tQ9HËd\x0010yö1©ZZOWâ%Æ\x0018"Fúnz#4NíÄ÷¥&&º%GR\Ø
[zÏÑ!!a<3\x001bs\x000e-
<ÑcÑ¾PúFÁàÚ\x0012ºÂ© úåðßØß®K·´¼\x0008×KêÓp\x0008ß\x0005w¬°®\x0012\x0017ëìèÑë´ªÄ]¹tvI¼O~NÍÈ\\TºÒaÑè:i"\x0000wàÒ\x001b\x000fGW¤	ÃÌ4ÅÝ´¿Æw¿¹\x0007JPÄÁími¯t|ûþ¾¢¹ÁÀE\x00149±ÐÉeÃ#læ¬¶Ò]éøõ·;õlÖÜ¸ñ\x000e6ß6n\x0010q2\x0015v÷à]\x0002Ö2\x00171Ú15¦&p¼Tù=\x000c¸Òg
r³\x000fÉZ\x000bmÝS\x0003\x001bPÒ{\x0000wâWu¨b\x0019\ÊÉ­\x001dËk\x0003\x0007ªÃÖ
n(¹ysX<Ö°	ØjÆ\x0006]-æb{\x0001\x0019\x001e¸UÁ\x0004	áv¿\x0013E£UåkÓ%ÉyuX´(\x001dwrû\x001dò?ÃÕCî«Ên÷×?ïW·\x0015¦G²r\x001bL--¶¬â\x0014´\x001fé\x0012°\x0001þÝÉùñëIp¼}CWÖ&\x0006\x0013"û2¥_ÖiÆÁSÁ­0î\x001eÀ£\x0014SÀéÃEèïlÓ4#m³|+O¬<hjk@¡¼|È~¢E4yaRÁe²GFoo+õS%v.\x0018\x0014à9n:Ñ~h\x000b¹ÅNz,$·Ö@Â¦¾å\x0000Ò)ÃÏq×£b0VªÉq_açALlÆ\x001aãÕÚ×±Yþéúkþq éÔEs.V÷W35âI#B¹¢å\x0002k¡D\x0018jÐÓºK\x0000>?Ù%
¿F\x0015©ËfT0¨cVE7]dµQä,ÆZ+Y7lÀzV£¥íRÈZÚÐ ÂlÇ:#>uX¿ÜÀê\x000f×¨E\x0015\x001e+]×¨3¢y3Q\x0013\x0016\x0015.@k"«Û`¦£*MÄ\ÒHOKSÌe6VÍ¬`j®\x000b\x0015P}EFú½W¢nhO4\x000c«áÆ».*Ë!h\x0018ÖN×ÆìUc\x0015\x0014=a1¬/°ªÂ¢Âê¶¬é|ÿ¹°X¨CFX
Û\x0013k	Ã$Í%G\x001bÛ¯ÉíÕç9ùc°\x000f¿}zR_÷ü\x0011µ#V\x001f?5ô\PI²'0Â«\x000eï¡ÇÄÏÎ/I4âÕ®\x000bkâNrg\x0001±µ\^\x000cÄ^ä»uF°:\x0005 k5ÞÄè±\x0004\x0019Û¿\x0016\x0012«?¢\x0018k"Ë¤\x001dqÅT#ã1F\x0005ÈpÙ(2¬ÎàV&®\x000cÎ \x0000â±Ü°ZbrèÐc	q\x0012Uw¸>K[n\x0018ìà=N\x000b¬\x00189¢Ç"b/½k
öåË4§ÆÃL\x001es0W#{Êg[8ÈpãA}lö\x0014qå3î\x0016û$^ûð\x0017\x0010£6\x0011_üá^'¾­ÎÔ~DÁ­\x001aÙb¥#= c¦
o\x0017Ø¾ÎÊv!;ÜhÉv52j@ÑcÉ\x000e¥\x0007ì]±|©00ÊB<¶R\x000bìðÂIE§Î\x0006¥\x0013Ø;½{£Ê ÕÈÚßØeÈÚPÅ\x001a9T¤? \x001cÕ]³ë1×[=1:óí²µgµåR\x0004§±øK\x000b±Ä~÷±]¼3¿¦îèµCbÒ¦\x0007ÙÍÓ¨ {\x000b6=+akÝ3\x001c#,	ÓÃ]vÛ\x001a´sÛ7fº\x0016»U8Ù5ÒÕ2¸nB °lk\x0006A4º}dUAàÜ»@kx?`°ÑÞÎÉ\x0003êR¹\x000c\x0011(sÚ.¡U
uDFP4\x0018
¨\x0003Rt¸9Lã}\x001a\x0013\x001c«\x0002%i7Ý¼R×É\x0014Þri\x0006AÚt\x00057\x0016\x0008«\x0002µ¤A×\x000ejJHC'¼,z\x0017Çw¨ù¤kït\x001b©u¢âQ\x0004ÅÌT§\x0006·\x000cô&þùÑQàBZµu·ï~®r*/m¬\x0014ØlÖj¯»\x0004¥±ú(A}
ÿ|3´ÇÚ»\x00017±bO`N¦Å¥øLMNzOªFx¬Ò\x0007ª\x0015ÃÙ½\x00157Å%1\x0000ÔÉRÁ*]ÑYMd±\x0019¬Uïò®;W\x0018,\x0019Óu\x001ekç\x000bk\x0003¦ë?ª»¬$«\x0019Sì¨cÝ:ù«ÇÕIz\x001a&ù$®\x0015rQcM¢kY7\x000fÿêqu\x0014g%Ö$ÍGuVbýÙý­­.0ß<®J²\x0014µY[ªÑI~\x001bÈW±jTÈ GûÀFÙ`µMg\x0002w.uj,S\x0007»m\x0008TlîVë\x001dV\\x0006cAà:TÌ#¥Gû¸f¹wcºW°âYäÏ0Ç¾	Û)d-8¹2O\x0002°®%bÚêVE\x001dêºð¢y
hqcN¥\\cCv,a¹µ+»heÅä>.<\x0006P'©t+tS¨ÅÖdôhU]úot$D°F\x0006vÊ¯\\x0003KóKf\x0001\x001c³â\x000cº;º²îü\x0017cJ\x0015u°\x0018\x001c¥GûÈºn×J\x0012ÅM2²yÎ½`\x000cöÑ|øô[éµY:\x0010êÕÁÍÿç|¸¹~ß{Ì©âïFS\x000b`¹ÃbèÖk51\x000bN\x000eN\x000fN^¾¼Øµ\x001døXÚhméYI"FÒÝ(*´(c41\x000f*pñ¦ò2\Wô`ð{v\x000eDJÃ(¸Á|\zQôXÀëJ\x001d\x0000ð\x0006l1ÆZüZ\x0014®t\x001e\x000fÜÔàR\x000b:­
¯.jy\x000b\x0017\x0005ËV\x001c6f´&¯\x0012w\x001d^\x001bJ:\x0002àÂÝVwW:\x0005¨±zÒJÞáÁÛÆ\x000b¦
ÌëÙW\x0018áF#mT£¾\x0017¯tôX2{¹e\x001bð	ædör«(¼í\x000fwpH4O\x0007ÅÃBÜ8\x0013\x0013Ð°¿Å9\x000eôX2ºÜ\x0006kK£ÛáèÆ±6\x0011¼ëL\x0005¼©Û\x001cL`)£Hz7Øýí\x000edk\x0016®¶ \x0007qÀ\x0014+Þ\x001d\x000cY\x0003¯0\x001ekxñf\x001dÅA\x001dòtÀÞí¼9Ønúú)Ã¼\x0006×*ÐÒáé«c	ñãð²`
Öèìmx¢æVËÎ6¼%æÕ%\x001f\x000cy¹m&Ê\x0010ì\x0017ÕÂé\x0000Ûåù`J®\x001dÎnxÇIkq±\x000ev¡¥\x0013-o!.f1q×$ÇúÛ0¼cK³xÿÐ?~ùòá~³ªGQð¼ý¼º¾½ß£\x0007k.°whHr\x001bé(­í¨ºù¥w¾~{üòõÉ.\x0011\x001e°H±·\x0003;Ï"\x001e\x0005Äbé<\x0007£Í~j÷­\x0001î&Û8ñ`³\x0000gl\x0002È#<êQ\x0005¼i?4\x0011çÀ¥nÞy/77ÃÇèF\x001bñÔ\x0002\x001b4}Y\x0006%ÜÜTÜq;Äþ\x0010{5å®"&	.»pÙEVóÞfîî
7#ÍíÛ]´k1Àgü²iì-qx\x000cG\x0007&V:·ÀÔ\x0013÷ÓÂ\x001a1÷g\x0005yw
ë¤k»\x001e«­'îêæÛózû{\HÚÈ<6e
1VáÓc\x00011¶(
æ},½Hìº\x0006ófL ¸WÙ³`V(9?|,R³BÝX7jbªY¸W(Ç½i}Ð®äéâ¬à"Aja½øý¯úýý»\x001fÖ] Å\x0002Z\x001d^ÿxuÿ¹¢\x001eÓz8ò¸7\x0017æ¿RHØF±½S#ý^Å\x0004:>8}ùìäüí.#h
k¢s®7\x0012Eÿ\x0017åÌKMÖ°Ú\x001dUU¨EÖ¤%§óBæÜÉr¡{ÍÂ,\x001eV\x000f?Ô´!?\x0019Åwè±9ZU¬c\x0018g¯KKÚd³â:\x0004oFuu«Q´\x001e}\x0010f\x0007\x0017&ÏÌ[Y{kÃ\x001e
&
\x00181§Èiç8qY}ÒQmk\x0019æé£¯\x0002Ùâ\x0015ÄF¿\x000c\x0019Ûÿ²:s´1'§»ô¬ìâJbd__DZ´sZq9ÓKraÓ\x0018ë\x000f]Í×\x0010\x0017.@êÚW¶fc¹\x0015Ís\x0016ÐÖ!w
6 ÃaKÞ\x001eÜ\x0013¸\x0015\x000eCåyòÄ®`vX\x0010IeÌ@Yqa?LfIÛ£|{\x0006IqÒc\x0011³WÀa.ïºl\x0019ær
²Á\x001c9®À®\x001c\J»\x0015\x0018äØÆíoÌèY Ç"æ uVÃ\x0011èyj$Ry¬qi=3æMöc£MÌÙ°`4L ç1±\x001azÛ\x0006úÊwKÇ9p¢ÕNê3Á¸mCíÕÔpè£wy¡áSà\x0014y\x001e±Ìg£»qVcµÌ\x001eë\x001cè±ôv\x001d3cxç\x001eÂ*©½Õ3\x001bd^º\x0006±ôç1\_
óYÄUôzÖ0cü\x001eÆ\x0019lÏÀ{\x001dX\x001b%q\x0011ÆYÙÏêÍGÆ¿\x001eñ®]¶:Ì·-Î¯Ö+7U¼RÅLUý~Ù\x0002ÓYKÙVrBÙ²>\x001fÓK¨&FÅvz,!Ö°\x0000­\x0010;\x0019eÛ5\x0007*çÖBæßóã·ü\x0003p5Yç0½Y=üöXS6\x000fÛ®\x00144as
n\\x0003V\x0012\x001fÙS\x0015\x0007o/þ~¹³b`
j(V¶4HGà¤¯\x0019J\x0015FTSù¬\x0003\x001fF\x000b+vo/¨6pi\x000bØÍYÊ0f\x00147ÌDÕ\x0018}ÔjÉ¸¢ëJÚ|i­côÓ
nºb`\x001cöú×þøB}Â0ñVoÎ¿¯Þ\x0001nE# \x000c\x001bbý\x000c8(3¬:\x000e÷\x0007ò¸¥Èèüûñs Þå~[\x0013ãn ;B+1\>DëÁs]¿rA²ÆÇ´W\x0003÷Å\x0013-\x001fÇ4Ä¦\x0000ãÆÈ#<QÖ_\x0007ÜõÌ\\x0000\x0012@U'«c}G<qï¨$îÕ<,\x0018bnù\x0012¼/)L8ÆAìãD\x0018½\x0018D\x000eË¹
)±.!2Ô­2]\x0018ãq[¸X£l,= '89L¼*·~0Y¥\x0004ÂOU\x0016×!\x000f²õ[³\x0012µ\x0007ìYÅÆH\x0016¼c"ÕÈrÃ6dø¿§\x0015ÈNÔ\x001eÑb©\x001c&ì:dÔ'¦Ç\x0012d\x0018Z\x0019eÌa)ò;â
Þ©×\x0012\x001b\x000cv\x001bµ\x0018ìu\x0013;bVãÍNN=§÷8È\x0006­j#N·Fd4~YL\x0013³4Y-D\x0011.A+h1òÝ£Sv#Aþ»Õãsóø±hÖs\x001e+åK¾c\x0006S¥«Cç}w|ùlg\x0006ÿ\x001a\x0010«,ln#LJü\x0010`s\x0006iVAuEò\x0013Å3\x0011;m³zÄ\x000c·d:Ä\Zøª¼®HÊØO±ªE4á;÷*ÃýÀ³6JÞs\x001cÓÜOØ\x0019¨&ôä4¥AdA%ê»\x001eÄý ö
\x001ej\x0011mÉ\x0001¥Û¢ÌE\x001aE/SÑO3	±þ 7¾fÖ÷\x0019Ã	Y[éÔ\x0011ü®À<D\x0017oz´0ºÈÍÝàE»RM\x000c®·ZÆÍ¿Àv-#eó¦\x0003Wo\x0019G/wX¿\x0005Ý\x0013nAäB\x000b@ÌÓ]\x00001
c\x0018ë7qP³PË\x0018\x00129qÛÑÒ*\x001a\x000c\x0018Y/\x0013ÞØx\x001dÑ©íüã­!\x001b¸ü\x000e\x001d\x0000JÙÎ[1î\x0016Ç8L®a$/Î©6`¾[iX\x001aìýÑ\x0013ú+3!1÷\x001emIDwÀR/â\x000b\x0000i¤Ïv4\x0013îÊäJ3­#©­ôc\x000bA\x0012¸³±\x0012Wf/ç !MvÓ°h
dèVM(	2unÉ½X<\x001cR¦aÝ\x0014È,!%Ë<±Æ\x0013ÞÓëf[-`Sh6{`+r<']Ç8á.ËØuØjb\x0014}l\x000b÷\x0003.è\x0002F³E;q!	¹nTÕ\x0004$½$ÄÒ'\x0000!½í ÷³nPï\x001eMV${\x0001RuÛ¤\x00179­hÇÚU@bek0,
dæ\x000bWA¬\\x0013¢¬í½\x001cÚ\x0006/2¦å6CNo\x0000£!E\x001ddÝqc'¼]s!3õÝmô©â\x000c¼ÿH±<@îÅ\x0018ïõôjÌ¥\x001e«ÌHk\x0018ÒtÇÍ\x001b`.$dl\x001dI,±(¯;ªPÚhÆl» ù¤\x0002ÉLH¼¾Ñ£	\x0012¶F6È©L\x0003`*v¯{BÈa.$@-7Ø\x0002iÄ\x000f@±,¡/yÛc\x000ef3Z|\x001d¶åòUÞ¶fU\x0014:·\x0013ç¬Õ\x0005´ãf(óZ\x000bI\x0005bÃEÛóÛîî6°KîcÝÐ±-~©\x0002)]11:Ñ"d\x0008²ÇÄxÒØÖãF[KÃÇ#)ë¦ë\x001b\x0012í~ Qì\x001eM>HbÀ¶³e\x0007êÂ\x0000¹KÃr\x0002z4AÂâ\x000c»¸¶³ìAS¥ª3\x00191â$RÍõ\x0002\x0019Sé\x0012\x0003Òá\x0010 'ÊåfBbV =Z ±I\x00117SÛ^LÝËH¡ÉHÑ[í]£0F¥»\x0019Å/é{ô¨¸N\x0016H«\x001cÕ¾Ñ\x0006\x0014K/æ JL\x001eK}÷\x0001&)=Ú =ë\x0004Ñä\x0008CÌÇè&*Òg2b\x001cÏûF\x0017¥®#ßn²-U\x0015Àh×W°½x$}Ñ·lp÷\x0011$¼b.\x000bÎs	!@zi/\x0006¯Ç[o½: ÞVfHn÷^cÐ\x0002\x0007\x0019p\x0013\x000f­;¹Ýq\x0013\x001dË¯\x0002d\x000eëÜÇë\x000eèØ
-Þ]Ä3¦ÌÉ\x001aÖe+µ\x0006|Rf\x001f\x000b' 6l\x0010ØZH\x0007Ûd\x0011µ`H\x0014EtÒÇ\x001c;\x0001ï\x0011\x000bMBn.¸"÷o;³j9Öi\x000bcÈq\x001f?è÷ÉüQ\x001bz¯¿þùáþú
Eàá»D\x0018;Â/×W ç\x0019{ÉhòûØ+`CRÑ\x000bÖòàúR3\x0000tù\x001fG\x0017'/Î_<­ó\x001eð?ÝäÛØ =ÿùêãõ-fÆ_ß=N\x0010¡þ0]_,¼B0Ã\x0008\x0008q)\x0006pÑÛ~/±\x0002ôüßN^½|Ypç/Ï.§¸4\x0006èQ\x0007¥nxB00º\x0011È|.ÑK\x0007¸¿\x0016*Èî?¹«ûÏÂ5ÙûÕíû\x0003Àù·W\x001302Å»hv9Ð{z6Dî:6	_\x001f¿þö\x0000>¿~:åµ\x000fyÐôh\x0004u¥è\x0011@\x0003Øa\x0014MGÐb!º¬Ià§\x001dTÝ¥_?­zµ»§«·¥%Â8\x0017L8âBmñXâ0p\x0016y^\x000cÑç­ñ;=>xM\x000f®oßÝÝÞ>^u¿a\x000cü0×^Å££77«wW\x0007ß>¾ûyõñÇ»©\x0005êÀ\x0014Àò4{E*uø¯\x0014í	5[\x000bôÍéñsL
o¾zvz¶cÖd\x0017\I)\x0005Ð\x0012ÆÕbA+9<ª4ÚÈì;ãÞÿÜßÎN\x001e>!ÚùÝ«ûgwNolÎ\x0015å\x0000Ã\x001a\x0012:¹+\x0019µ.ùØwy\x0015¶7\x0008w~öâäüàÙÙ÷;w¸5!M&<Ö\x0006F¼À$Às%\x0004\x0000\x0007Mèv\x0002v³n\x0017!z(ð«Ð¢\x0016\x0010\x0000*\x0010¦´\x0010ú9C8I1ìÔDè`ëÀ"&$t¥ß1¡*kÐé­
¹þ%£ªÀ\x0011=ZÞrÂp3\x0001rã(|ÉE]\x001d\x0001­o\x0006üã>«ë+êbL\x0005\x001foV÷¿^ß~^\x001a^'®[8þ
Sy^\x001bNo\x001d°oÏÿï¯_ì ùñêÇ»\x001fß÷¶¸ç7«Ç«û»Û)ä(\x000c\x0001Ç@Æ«.­Q¸?È<®¾;ÓãËó30VïW\x000fï¯ºßÈæo§3Ê\x001d­¿qDµ¥YàëÕ§»¿þ9	+¤¢\x0003\x0003\x0005JáÀã4Æà¶Fªt\x0006|}üæìôäl¹&p
í\x0013\x0006SO
Ê\x0012\x0000s2Ô\x0010]$M\x0005F>¢Q¡\x0001±TÎ\x0002"ªu+Í¥\x0018\x0007\x0010CZ4)\x000e\x0010S¬Gô¨·XF\x0014P
b½Ø\x000ctÚ«	Q)w0&©jÄ\x0018\x001dE\x001el2FsÿG
»Ë¢Í\x0003'K
"üB¶z·Xà#ôÏeG5XÏïÿú§Ì:\x0000Ó$³	\x0016r\x0012%2XÌÜù\x0002lw\x0017wZÈTqõüüdG½U4\x000cHC\x0013)-\x0016[ly¯Kp\x0011H¹÷	ØòIm\x001dnõ¤y@ÛÆ\x0014E |\x0019S0²BÙ­½ÖQîCnëÍ×j¥ú¤TËÔ8¨ÇÔÁà¼±2¦Oìæµ¤°WôIqëh\x0019T\x0014#`TN|ÀAU÷$7P¨lEõCTßøþó¡çë0,|\x0017øý\x0017Ç\x0001 :³óN7ª\x0013¡n¦Â7(Kú­?\x001c¼ZÝ_ß>LØ:çi²ìHÝ]¦iÞ¾¶K[õWÇç/_?`¾\x0004S¯\x000fINõZHìR­\x000b¤W|w»ÏAo-ûZJ;¤´
¨ùky\x001bey+¤ì< qk\x001dÕBú!¤o´Täó\x0012îºÌKÔþaJí·P-e\x001cRÆ\x0006J¬¿gMô%Ê\x0003ÎÈBÏnñX\x000e×kY;¬ËpO0å\x0010­Ó(Ä\x001dVÜlJ?\<¾eñ¨"ÓpóåÌÚÿË­¨r¸x|Ãâ10\x0019£ìQ¶ö¨ì1/Ù\x000c(³i\x0018Kí)¹	¸+Ýèé\x001bÃ«Ç/x!ìQÒý°þûbt\x0016ÛCÉ\x001bO)Í¶?±R\x000fv¢Ò[ºú+*%AJëJÝ\x000b¾qñËÂP.<zL\x001aÌË>TKT÷Æc¢­\x0013(\x0003ÏJÒÂÇ¬-xbÌ®å}\x0017yf:Ã])ÊSèÖ\x0016û=6\x000fÞ·Í-ï;\x0018*9 4bi\x0010eí¤íE\x001d¥\x001bÎJ×4+]é\x0002H+\QÚ*Rºnû\x000b\x001c\x0005\x0006
Ç£Aÿ\x0014CZE\x0012Ç\x0008i×÷µ+ÇÙÁ.älÃ.ªl|']¤H\x0010ÒäÔE\x0016îBØ·O¾áZJ0Èi\x001b'{ÈÉÝ×û,/|Û\x0019^\x0007	¿ïCzÕ²	ÙÐ\x001dáQQjzßÊ9d\x0016ÎJ?44|¡!ZHJw|;Ë*Èí,íðÇÌ§\x001ce¡
\x001a]Ìb©|±LâìpÎ-ÿÐ§\x000cªaZfrð5\x0014ºY\x0019;¹Ùá7
©\x00052EJàë¸eJ»Á\x000b7\x000bíß`\x0006Á4Q*\x001eJ¬â(Îjòê\x000c©ìÂ÷\x001d\x0019B6\x0018:ò1¤ô¹4tEJ9Âmv\x000bðàCé²\x000b»\x0016J¾âÚ¸øûáXú±-Í!)CbWZÒ\\x0004\x0019±\x0005"Ó\x0005\x0012xCçÊâ-Ýb\x0015ý"Ê¨\x0006/<ª\x0017ÍäÊ­Ì\x0007+ÑXVo¡Ôjá­\x000cnË\x0003JÛ`³)0ÌgÊÎ\x001c\x0002z\x000b8\:±eé`æ¼N<)¸°û­µiá©2Dñ¯£B;»×e\x0018¾É!ah!\x000c\x001da,É¡(~u§·½ÕÃã;µ\x001cßXLf=\x001f:Vü\x0004Þ\x001d:\x000bWwCÊØB©Ã!;Ù!\x0005vôJ\.6/\x001c\x001a\x0019©ÁÈÐ9ûÎç¯m)\x0015\x0005ÊÎ\x0013è:¨ópÌ-û$V\x0006[\x001eJÃ-x1Ñ=Q\x0019Ô²Qc=pß{UêkÇÒúC¾6F/gñQÜèy¡_H0ôPP¿kô\x0006yööc\x0016UÙ*µåm(è¸lZb/\x0001¥uõ\x0017G§âjJ2°2ÖÈ+6-;\x001aµóI\x001bf¦§\x00032
²\wl\x0000O\¸Æµ\x001fnDô¹²H\x0013R²åsÇvñä¶sj)Í\x0006eÍ\x001d»\x001cSb\x0012=á*±Í\x0006eu&SÞÆ:\x000c\x0005ß82Ã0\x0014üîÃõÕý$g°Yò_°"ª\Ä½N¿d\x001eYçð»\x0017/OÎ§H}\x001cúØDj2eü#iæðÆ,¤z;_O¤¹]n	
k>Ñß=MÑ¤qH\x001aÛHñ,òLê\x0006:¶45c'æLÒ\x0014\x0006¤)4\x0016L82SbLIõ´6\x001c31³\x001a`fÕîõÈ¤N°:5brÎ%\x001d\x000ehn\x001bP\x0015\x000e5æCyñZ0\x0017¿v«R\x0012?6PâýÇsj´SE\x001aåÐ»ñôËAµ\x0019jÓ\x0006$\x0005.b«\Þ¬\x0014¯$k\x0006SÔ¦)ês©\x0001ARÏ2 8¤Q@Ç|\sAÝ\x0010Ô5¦XÜí\x0008êJ\x001d,Ê÷óÅ(Q\x0001ôbÒ0$mZK\x001e#i¼ê=/yíº\x0001Í#·õ¹qÙt¢d /g}ÄÔ2GU)êÆå v¸êmÛªO¥±\x0010\x0006uÈkIö¦¸ò]¹N4"Ìa¢ÑlL¸®[ÆD´RJ¢Øá\x0005{ÓX\x0012Ï\ÐáæäÚ6§¨»c>ä"G/^L§4æK:|ó®íÍ¢\x0008SVRÑQBR+¤;`+Hýp\x001bõmÛ¨/ºH
Ã\x0014®r2¦c®Äy¤N
Hj"\x00053KÆ\x0014\;Ê\x0017þ+¥\x0006¦lîJ OêFo3ò¼*­Ä±Â+Ì~O)¦0ËçiP\x0003Ò H\x001dú\x0013©ª\x0001\x001bUJå\x0011·Ù\x0001ÐÑ³¹ i\x0008Ú´ \\x0010T+\x000c´\x0016oSN² \x001eó%Ï$Õi\x001fHKKy$õY²ºrbom
nñ,ÃY\x001aÛf)¾{S@5Úø_¾çY\x001aÕr£4
¯w©íz¬)\x0017 i\x0003F~ä2 \x0018ø"\x001aGx¤N:¬¿A5\x0014è7WÞß=>L&A;Xð±ì§ÉH\x0011¤Ë:ðëwv;#`\x0004ýæä{ ÞÑ?¾k\x0006¸¦\x0015\x0017·ªr1A\x001f$'0¤,´Od\x00064Ñº\x0001ífÍÆ\Z<{D$\x0018d_u.m­­&Ú0 Ý¬ÛM\x001b3U¿PÑ©`Cb\x0019v¬:
ûÁM\x0003ÜÔ\x000b[¬eë?¯q\x001d{$±|w¼(b&®\x001bÌ\x0005×<\x0017r,ñ\x00074\x0007J0\x0014q\x0013¼\x0001î¶áÒ;\x000c®u2`\x0005hÊ\É(F6,4©Qu:îe¥Á6\x0016·1V~ ³°KÎÈ.Ãb;QµV»\x0001-~lÄk
\\®ØÞWÉÌä]§\x0011/¦5ñ1Xr_-òK«Î¿¶A¯CS\x001b6ëzfãb2#Ï\x0006½¾$\x0018-.\x000c»\x001dëkáMÃéZ§G§ î¢\x0001¬.¡´\x0015ÏµÚv¹4ñÚ!ïf×l^TíE/X\x0000Ût0¯ßÇ^fÜð¤p­GÇV¾å\x001c\x000e(NÏ¼6H\x0019jÔû8*Ìº`¥ðnÖ%Îæõ
H\x0015°m+/·(´ÛyG-´q0\x001bðc+mnÐöµr%çÙ\x0011{áõCÞæÝ!©nt­.½aÂvâ\x0006ð\x0003í7
Í²Ôz\x0014{L%/»YPëÝÁËækì¶ë¸×\x000e\x000f7Û|¸a£½\x=ö\x001fæá\x0015O·~ÂïÑ\x001b\x0006Ó\x0017?¶áâò
(ÀaaÙ1o9U?'BÆ-¼qp\x0016f#o<ÌÝjSì·1ÉjÛ.´lÁMqR8m¸FQæ\x0005í½¥d\x0010y½Õ\x0016â²³\x0002¬\x001cºUtÃ\x000bß8ÂÔã/W·¥Õéó«Ç¯Ó5Ö*°÷Û p.\x0017¿À|%·\x0018;\x001bÇß¼.=M\þcM¸f\x0006h¦\x001e
®cÅAg°\x0005 Wª£\x001e mçËÎe³\x00036[Ï\x0006¶@\x00112!\x0019ÞýG1ÂöD,{.þáÇë×ß©F,è<|úåK\x000b\x0010\x001a½fB³Eh\x001a\x0008u\x000eò$i\x0010î9¥\x00161@\x001cÄ¸u$m"vr@Û£ø¹èéôF\x0011¿Ó0!\x0015F/I\x000b0¥àÁ£ÐÅ\x001155&Ó%P÷\®hö¶\x001aôº=Ì\x000b\x000côî×Ü»	þp2\x0012ÂØ­{FN·qï \x001a.\x0016ä4¶Ó\x001frÀ:eNõ¨\x0016$»-ÑiL[\x001aü®O\x001a\x000b[÷à y³º¼ºv\\x0005r¨Ø¤#\x001cá¢¡¥Ù·MÚ\x000e\x0006®7í7Çç'§\x0013i\x0000Z %§<é¤\x0015m$RÅÕÙ±Kô\x001cH½®VDHüXOéK3r¤tV$\x0007R²Béíµ92\x000e)c=¥S«t
ú0VdÈ°\x001d®\x000b©HKH­¦\x0015*2õÎãOWÓÙ¨ÓSöÈ\x0014ä:Îö¸$·\x000cnÿ¹88>}³£ÑbÑô\x0019M\x0003#öî.\x0007uD+XÒ\x000fKA%z ¶%Ej\x0019mÑ60ZEº½È²7\x0008\x0018\x0013~;Ö[Ëèú®1ò\x001dÄ¨]ÉÈ½íÏ«eô}FßÀ\x0018"§!\x0018LÕfÝ(Ç\x0002\x00188\x001f·ï9µ¡Ï\x0018\x001a\x00185ë$
+=ÈÚÅwÛqWË\x0018û±±d¼\x0003"ú9±Øsz\x000c¶[û¹\x001a\x0011ìïR¯\x001aC\x000e=J%G\x0015Ýö÷<Æu,¶GÕ²?ú²¨\x0015ÅÈi.ZÞw´Û\x0016Ð­\x0005\x001cîß-\x001bx²T¬>Qß.ÚÀ#3¦ílÒZÆÁþ­[6p¸ÂhÞ\x001c±8uÖ¼ç°\x0016r°ë\x001d<zv\x0017¹_2½m¹ÐØÅ'¡\x001eìàºe\x000bÇ}[w×i¶ÎÕòºG®¬3\x0019\x0007;¸nÙÂÁ\x0016ç[îJÀö<ÛY/µý[·là°kAÄd²ÀKFñÝ\x001aî»¯\3\x0011\x0007Û·nÙ¿»+ª=²\\x0015Ücº3fëâUË\x0006©ÑpN+Å.¬gF+LÚÎ\x001b¨\x001c\x001c2ºþ\x0001£§ôé¢°«Ä\x001a%>\x0008ÝÒ4CÆ´\x001c2Ör Ð8Ì\x0013fÄÒþÁaëßÅÛc\x0018¸+Êº\x0019¸+*ì3Ïó2ä®\x000cûú¢Àºõ·ÇÕ6.³þðqìÂ \x001cW¾u;xË$	¼¥³tà°*3uà°ª¬Wr¥ÏáÚBÇÙj\x0016ïïfÕ´±ÂUL\x000eu\x0013;÷©7â¢\x000cÛ*´Õ&æ&kÓ°\x001aÂÛ|©À¦5ld+¦ß\x0016¨¶4·\x0016j[`YÒMÄ|\x0006vZ\x0006Y`Fm'b×/°Í)\x0010Ú¦uå9d\x0002§¨s~[@¨Úq°9¦¦qÏR\Âf¢ëÔS×{\x0016\x0015/GÝ\x0018ÒÆEåÃ!¿|°ôì®½Á¸èOÔÍ¯ÚPs¢\x0012&òÊx.at.(^Å×7¥·XÛÖ?
ÑFv*tÆË\x001djÞÖþÜBÝÑ\x0018FT
C>j#äóìñ~:\x0010\x0010\x000c5\x0008¦á4\x001c?wÞ¯×ý¶ìø:\x0010ðìò|$·}I®\x001aÐ)ö^\x001b
9²pûJÛé4u~\x0000è«\x0001µY\x001fô(Ô(×u¸lï~Ë³\x0000Ã\x00000T\x0002Ââ-û9y°Ë«¡¯\x0015í¼PÏ\x001c¾8àÕ\x0003*G÷ÉÄf¨OÚuÛä2¼4ÀKÕx°t­\x0018\x001cJ|Z>Ê)®ýq4\x000b0\x000f\x0000s\x000b ß\x0002\x0018G¼£DºõvH¾
Ïª>Uõ;L,J<g,%Ð\x000e#®"\x0015¶unê\x0000õ\x0000PW\x0003úTQSW®>ÑJ«\x000eÐ\x000c\x0000M= \x0015C"(ÉºpÞ&~ÅX8±\x000cppØúCÄ&ê¶;\x000cvéá%¢9\³\x0019¹ëÌÛ£¡yÚ§¡ùYÊw·H\x0017º0r%tÎyÄÈwØmqº\x0016N8ótïÌã%mLÚÓgõ&§ÝLÆ·´µtÛÀù½»èö41á½\x000fÒ\x001dè½\x000fÓ\x001dæ½wÇ\x0002\x001dÆ[îìïÝt\x001e#»û"6s<78ífZÆ¼ÜÉIíYT\x0004\x001e;[gÄñ?o+ßzíªåµ§Î\x0001\x0017tçñ±»¥\x0016OÞZF¹izzñÁ\x0005©Ñn<yé¾©7]FåÍoºfÑjU´.èå'YôAÙÎÅ5r±ùö7QUÃ$ÕJI\x00184ëxTs·ï·+êÞ¾Ýzû¶åí£¬½áK­ìvºx©ÝÎ­¬åÜÜlË¢÷£\x0002ØÕów	¡ÃvÆê<Lí´ôZ"Ì£´tO!ìàtõîçÕã§ÉWî¤\x001céò°t<ØmÝßÝxáàô\x0018¾ùfrADI7PZ+§¦ÇÒâ2\x0001ÅG¼³Rs\x001eeì	Ü\x0003eì\x000bÜÏ¥\x0017Â	ë¤ÈÏ2ÝDO¼ï:Êì\x0007Ù·PbC²È5G	èÄäÄä\x001c¶O¢JÈá\x000bÏ-/\x001c¶´¢xÊ½\x001847$Ë>oW®Ì¥\x0004\x001böÌ^X2\x001d
ÖÎ³«ãëéÞÙ?Ia\x000b\x000bV`]²«rÝnLÚA>;9=8~¹«µ¡@®\x0015á\x0010²¯\x00077\x0017Ò)[ÀF©¤ÑëÝë{&c\x00180\x0006F¯9Õ\x0006R-»FÎ,yy\x0000[ Ü%©\x0002Û°ô¨9»[Ðb\x001e£V\x0019IyìÕ\x0010*Ì®«Á®"L\x0019\x0017d¯ø(C\x0003eàæÑT´\x001aYu\x0001&¢¬\x001b½ív©CÈØ\x0002i¼¨ì¤\x00108Ñë(\x000bpH.\9:æ!en ôÓúUÆª²¾QÇ¥6v«¥ÎLz\x00009ØÍgC®HÙ'\x0012\x0006@HÝõIöÛ]\x0011k)íÒ6Pb\x0012)¥Îl®yÖ¥ÔÛWÉ:J\x0006Û¹K
ûyö×Mô|±c¬(+°[\x0003f\x001ed\x000cÃ3'ÔCZ2JÄhá}R×\x001b¥Q@J#]tfBæ!dnÔ*ü\x00076¶guÇ¤X\x001d7å'J\x0011ê(\x001aÌÊ¤êg¥Å%Z;ÌtãFñ,MGtóf2!£ia4\x000b2ÂQÎ±3rÜÝ®d.¥\x001fRÖoè\x0016E{ÊöZu³2³gVf;µ2\x000e)cË¬4\³­=VòDìpUn;O«2\x000f)ë\x001d\x001aKÍc\x0019­ÌÊ¤X\x0018!Ã>¿ûB6Ò\x000eÎdëÏ\x001d\x0018KËY\x001a\x001a\x0005(P²ÍÈm¬ôÃ¡ô
CúÇ¥õ²¶8Cñ¼ dÔ÷ZF\x0019K<4,q\x001d¼p0Ïä\x0008OIZ¦ç¥gc\x001aÚ©Á®\x0004ÈÀ)ÚÁaÎ%Â0²\x000fÝmgR\x000eWxhYáÉÊ
w¡4î\x0003Ê,ò=9ø2æA¦áP¦¡4Úr.ÆV¶~³cÙÎ\x000c'ðRÊá\x0011pE\x000fQS?IË³Rn·7ô^Spbt
Áö4I£W(òÊ	Q¡ÅÇNÖÌºa$Í¥ºC[¬\.;e\x000e|ÿ-Ü)³\x001b2º\x0016Æ\\x001a¶±YY´\x0002)\x00143ånYÁÃ9[æ¤å	i¢\ÇrZ\x0006Ríî\x0010;\x0017Ñ
\x0011\x001b¦¤ÅHç)i)Î»¦d\x000fd\x001aR¦\x0006J`au>ÌÓð\x0005RDÍáú³Ì\x000eÒf8%és5¤w<!UâM2XQ6Kv·ù$b¤|µ^~Aô_pþxupòþãÝíûg«û«ÏN;[\x0012_ HÊ\°Ckg¶¯\x0010'\x0007'ß¾:{ýíÁ³ãó·ßO`öÜ-ð[ò¶TcºÐIWéÀb^g%òËö÷]\x0006©	3ØN\x0017ì ³6Ò4)YóDó¹Ä-U^·5Ù{eÂ\x0007¯î\x001eo®o'ã%Þq£>ìb+úÖ½óî2áËWg§/_3êuu\x00142âÇzH¥ç!\x001cÔÒk×¿%'ô\x001ej)ýÒ7P\x001aM@×Õë.\x001b¡4»ëÂgR\x00063 \x000c¦ÒÆr·ó'\x0005H^;îE\x001fü¶ß·r8¡e,a\x0000¹39\x0016\x0019²4\x0005uà,iÛ¨¬¤\9\x0011e_Ìi6¥+-v\x0012¥«YÄHóÕ\x0010·Ó\x0016ë(ÍZ»\x0018)ñcÃ¼¸2]ÙWü¾£	K\x0019×Ù½ÄØ\x0017W?\x0002<@&ï
\x0017ÄèvëûÍ¤ìuWFÊ¾ÆüY)÷1Ìj¢bHY ·\x001bÏ4iSÞ1±¼#Û\x0019\x0007çwï~^}]M)?ÀPªCÒ4Ç\x0006TW+OH\x000b±­qyp~\x0006ßÿÇñn}©	3ø\x0012Ê\x0003NlE¯\x000bgÈ²xÂÎ\x0000Ô\Î¾è?vPïþWprT\x001a¸9Î\x0017´QÉx\x0006½-5XÉ\x0019{ÒÏØë²×d>§Ï#[¦ô&°ÉHSí¨wùgcöôú\x0010³\x0017+	F¯t¤Ï±\x0008M!fr¡\x000bS«4\x0018Nú\\x000fyÞ¼Öæp¸Í9È2Êz×­b.§^ÇÃS÷"âó9\x0013\x0018G%ÿ\x0012µ\x001f$\x0015&¥¼wïv¹²¦AáoÄ½³wÿqØ!m $øüþêáÓõÍÍÝÔþ©a±°Rµæ0y^Ill&¬Ûµ\x001c<??¹xóòôôlç\x001e*°f\x0008k\x001aa½\x0015\x0011L«$#ÜÈæ\R#Fg
m\x001aÒ¦FZØBYFÝXñ\x001dÙà¤µq¶#\x0012sam/\x0002äðiÛ`½\x0016g\x001cæâÉÐFÏ÷Lm·ë¢[`Ã\x001064Â:#Ñ}g3õÁEØÎ\x000b«õ*ùlZç\x0007´Î·Ò\x0006\x0011¨wÑÈ)m\vÛ_Ó\x0000ó ·Î\x0004°ÄêQfO¬®\x001b\x001d\x0005Ô\x0017Ãö:z",5ôl
hên\x001eB>u7kõv·zZ¯\x0006´ø±6uí(\x001dúKÊ^cy`¶$
´z0k½nµäÇá±E³°a¤(Â;ÂX£iZ[¤é×²A¨ÛÀ½]ÝÜ¬îßO]\x0000°\x000e¯c
]wglpqwÇ·Ç§§ÇçßN0®MAË]@ª!±%YaL³ÏçÈV\x0018ñ×Î\x0004ô\x0003@ß\x0000Ø]îS@G}\x0011ÃÆÆ5¸»ß×LÈu\x001c\x0013!\x0007aÌ¹\x000b·c:3Ôi\x0016\x0011\x000eÞl¨ký`º\x001e2eÖ\x0000H[R\x0011Rñµ9x;.5\x000frí&AÈ~£ùFØ:BúC'kF\x0010·kë\x0010õZä\x000f\x0011ñcÃÛNE	\x0018}v\x0008ØÖ)Ç¥fQölhZ7®ae§XR¤2ÁþÎ¡V[ty\x001c^\x0017\x000eeP)\x001f«!C¥4\x0004nHØ
£\x0008ëëà\x001fD1çQ\x000e÷ÈÐ²I\x0018K
\x001fÞãòabÑmo2$\x0000Ì¡Ô½^\x00124-ujÀyWÚ\x0000fÖ]gDÖbv!Ý¡­9¦×®¥7¡\x0012\x001bã%¾Ó\x0007#5VpU6Oy!¦CL\x0013[\x0006Ó)±24V~ò`ZÝÉìî8\x0017Ól`6ìEØ\x001d ôoC\x0005=ÉMQC`ùìnÒ<\x00133
Ïp\x001aNqÌ³ÅÂÔ¹SôÌÙ%Æ\x000cqÙndì-d[\x0016º7S\x0001à/´ÙEFÁÌ»»ÊÎÅ4\x001bM/]IC\x0013)±òÒ9Å4fûDìµ\x0012Óm`ºÑ¤ö\x000fH£\x0014
(t\\x0015J?62lP6X\x001c4\x001dMäWJûK\x001eå¼-\x000fUéõpjzÝ25ÁÒà¦F6Döy%\x001d®`Y-|åÞå!¥k¸óxXÜÉóMRz2K¾®Ê#¹\x0015³\x0018ÃðRFëOsçÅ\x0007ê¸pIK]ÖÛ^Å¹:\x0014\x0003³{Ùð#Ý¿?\x001e®\x001e¿®¦\x00001Å§Hík°×¤aA\x000c,\x0012\x000fæ§\x001d`\x001e_þãxq­JÚÔ3\x0006`¡|bÖÄNr`UØíèÇ¸îèAF×3¢L\x000cç<cú33FÓå<ouiø®SÃ»v«C4\»I\x0013\x0003\x0019
WM>!BZEè×\x001a¤H\x001fk	\x0015Ü#JM<Æ\x001c¤%o;ñ¾õui0\x0015ñc5`\x0006@naë\x001cç\x0010;¬°áÚ\x0015·­%2\x0011LÞ¡+\x0008=.0¯_~ü´zx È\x0000\x001d¼ÿïÿü¯Õã\x001cKÈpÞ&àE>\x0015ÜRTß }ùêÍñÅ\x0005Å`øû\x0007ß\x001eÀs\x0002»'¤eÖ"îÄ½aF3Kuµ7qÛw°z§@YÁ^ç­ 6¦­,Ä\x000e<{q;`l)Æ~;Á¼q´×¾\x000fÄFßÇ"lQÕÕxûHlá99§¢Ù\x0016ÌhãÖ½,~]\x0017í2ðäÙñ2R,Hý©Ûm-Vs\x000e"n]ÈaÕ\x001b\x001c\x000fÏoV\x000fW÷¾d\x0003».KhÀíÉr¾w>K{'úÉ¯÷ç°y\8¾¹Ùë£&×j²$¥c
\x0004ßîÁ>åÔyÒß\x0003j\x0018 &T¸Î\x0015×\x0013v{c··a³?»\x000ee\x0015iÀÚ8£ØÔ¤üÎÍÔP1QÃ¶J=j/ù\x001bP³jCE=Ð¢M"\x0006Ôvcv÷X¬\x0000µ\x0003PÛ\x0006\x001a4ÇuFI\x0008'nÇ$Ót»\x0007J\x0003ª\x001f úÆ1\x0015§\x0004,þ õ6ðÍ/SSå¨q\x001aÛPY7\x0007Q} -\x000bQ­\x0011T¿]úÚ\x0007¨¹	59V4L5j\x0005p?P«E$ÜÚÝMÚg£j5Øý)i¿5JO
'AÜö°É°ê0bÏfµCÖ¶\x0015¼åþì\x001a÷Wîp\x0006Na5O8¡\x001bXýµme\x0005¬£aVlÅãê°Ý\x001d+XãµmiaK`.¤Å0½q\x001cºË0\x0019\x0001Ú\x000c§iÜ[­â,#0\x0001¤¿·,OæHWq9«\x001dWø±usÍAl\x0000\x001aa:±Ø©;ÍbV7du¬*Q\x0012\x0014±j)á¶ce\x0019Ûc-gMCÖÔÆ\x001aà:Îu½8\x0007XäÄd0rOÜ\x000cªY\x001a°\x001aÕÈjåÔÊ*\x0014	Òünùé1×>¨kÝ\x0003Lw
HN"ºÆ Àvi=ëÐh1V\x000b\x0007×\x0002\x001c1MÑâ·5â\x001bPó\x0010µÑ\x0014P©C-\x001a\x0003Ë\x0006e.\x001fù»»\x0017ôlV;«¶q®¢"W&¸\x0016ð~¥\x001c¯6.3\x0006CIà\-\x0001\x00138û!óÕÁ·W\x000fï\x001eïT6¢äãº\x001c\x0002>NQ*þíÙåù³Ýr\x0004k{}ü\x0000\x0016?6Â¹¢"Ózª¹ u¡Ùê×ÍÆq\x001bc+nvÜÀ\x001cC²âO\x000c9ó¬n[¿7õÊ«7
B5¼\x0006ÉPÒ±Å¨òÝé5\x0012g«àõ~Àë}#¯Å]­\x0018ãy³uI\x001a\x001dáµ|\x001f¸q\x001b[q
ªgpÙ¥Õ
÷\x0005§}a/£³!7Ï¹\x0007)\x001c\x000f\x00041 »V®Û=Ã\x001ap³\x001anVÍ\x0001\x0008v\x0017 F\x001f×ÂÌÓlÛ±Ñ\x0006{\x0003~lÄuIÜx	ã°\x0017Ì\x000bÆÅÇÅ¸pë\x001aL\x0006úÜ¾ÖX*\x001a#Á\x001bX\x000c<\x001d\x000c*o,\x0007Ön0¾ô¹
\x0018f*7kÒ\x0001[vÑxÑÖ#òx5Ày\x000387\x0002{í¸Y\x000e\x0018¬åxN\x0005§ÃvË¦\x0016`¯À¾ÕtðF?è\x0010Ü¡å\x0011NÒ7[§í\x001aÏ\x0016à´\x0001Z\x001dÖª9âáìLPÒ¼Oïg|{J\x0005×6o
8pµ\x0015/'Ó\x0003ïH\x001a^
°ß\x0000nÝO\x0000£Rb?dç\x0006`»}£¬\x0002\x0006cÂëH¯ÇÊß@ï\x001c\x001b\x001d\x0005FJ	HR\T\x0001VôEÞ®Z\x001c\x0004zGìsf\'8"cØçÏat\x0005+Âý@IJØVr\x000biøº
\x000c¾qÔ+\x0002»XÝ¬>®nßOwøÁ­*s=­J,(cSRØo·³êòâøôøÕñëowË3f/o\x00100oÁËx0JBiÃ`Q\x001fE0w\x0016ýÌÅÔké-ÄÄ
.rþN&pË)2«ëEÿDóÎjÎ4äl{íK\x0000ÓuRìÃÎ(Â4¦	\x001b¬M(¬»hòÕÃÁû¿þÇÍtË6X&ÅlAÝ	\x0011Ékäa±t7ç'§»¶\x0015Ò~]:âLj@õFQ\x0016f¶*.RuAÒZ(÷Ïiíf-E>ë=éâóêý´\x0011\x0007hIÊËx8\x0011EÌ×E/Þ\x001e»{nr46ö\x0011S¬Gôó\x001d\x0014â¸_@²R?ë1¥
ÑÐÎÖbøÆQr\x001b\x0016õëÛ¿þ9¹~`¥)B-ZÒ\x0004Ë7ír\x0008ï>)ß¼|}2ÎÒ}}Nú\\x000fjà\x0012½NÏëú³fïEHó
i6)\x001cèËê]R`JÍ;Ê3\Iß?Îz÷\x0013[-\x0017x¡ûB²FÍvÀ¸úVÓùå\x0004®·\x0003\üØý,
/záø~¥reÉÛíÐV\x000bn¯Ä\x0017qoÅÅ\x0002Þ¬­¡D9JôÂû\x000f¶×Ç\x0001¯Í¼^\x0004»´ê6«(\x0005bÌÛÂH-¼q8\x001dbûtÄ\x000cò\x0003#ú ã«F;ÌæMCÞÔÊj"<\x001f­\x000eõ>ÊðÆ\x0002\x0010ópµ"§üzx1\x0003Ú\x000e÷Åj²QGDåì.\x0003Úr Swi±»å^N\x000e^\x001cïî$Bpní¼B87p^Í\x000bÙqQ2PEw>\x0007Sç\üiºè\x0006tÑU\x000eVppÿx¶ý	os»·Ó\x0019pa\x0008\x0017*áP¶D\x0004\x0003ª\x0006rÊMp\x0001çÝn÷ä$Ï\x0017K¥OUt®ó4 ¨ IZ\x0018ñûÏ`C¶XÉJÉÂ\x0016H\x0015ç°sñ\x001bt75£um1¢Aqñ\x001c4¸\x0007\x000eÁi\x00138®òÙ-e\x0012.®o»\x0008\x001f«àrH\x001cÚÏYÒ­á\x000eÎpn¤îl­'ÛlCÙæ\x0019lÉiñÎ"\x001cW¿:tO3Ü2º<¤ËtÆp\x001f" Ü,IZ5"Ü\x0013óás.ÕÎ¹¤$dÀ\x000ccÇ6XI^R7ÇJrgÐÙ!­ßæJàè¸¦Ìfié/Kèü®rÃiWRsÎv/6g¡K#5£3è"Ö.
tMñµAÎ~åðz¤ðv\x0006ÝpQÄêE!Ù\x0017DÇõc.9#tK×«"Õ®
Î¸E:c;É\x0018»U1R¿:IÕ.«Z:°L\x001cç0Ã\x0011ÆÕµMÏ\x000c\x0007í
%+;«\²ÉÆR<­á,7©ìíÅ>\CGè,+.¯8¨¸<\x0010êùîúæ\x0006Wøëäy¦¹7{LÔä_±ãûQ@áò]ï^âó\x0004@î¹ÑAÚ]QlD½\x000c¦çY)*3þ
Û6äuß\x000cDö¹\x001d9:øÀ¦MZ¦ªñîlë:àue\x0008\x0002÷+CªMqCFÌî\x000f\x0018ä1N»c#UÈ:\x000ef2~ld¶ØØR\x0017èJ\x001fcê9Õ©æ¸Ý\x0019ÍUÌÆ>3~lf\x000eb:81¬\x0008&\x0005Ã\x0019!<¡
Ñl×W\x0019Ú0²oFÖJ\x0017¥ö\x001d\x000e=3³-\x0012¢ßxmBÎCä¼\x0000\x0019«bMû\x0018t\x0002Ä)BÞî\x0002TI\x000c´´Åõl°Pü:\x0002ðìêöî¯ÿïótà·6ÔÓì\x0002\x0015YI "m½W	\x0000<;y}öòí\x0004aßíª'\x000c±#ú\x0001m§è¶Ýió\x0000WC@ô\x0000§Ánðæúêþþê\x0017÷w\x0000<éUÑ²±,_I¥¦æ\x0008\x001a|oL8ñÍËós8ÏÏ{\x001cØ\x0001°	K=­&\x0014¸pFêt'¢\x0005æ{bCæØÎì={ðo\x0015óA'°Ùl;9íº§02ãÇVf\x0014Ù*×dÌ\x0003b\x0017¶·Z\x000b³Þ­B_Åìì`n8Û>7"XâÝîÓÉ\x0003@¡\x001cðBa\x0005pX{2\x00118(¿\x0000ØtRË!/\x00026â$²Ln)³Î\x001bùÚða¾6¹²_ÝÝ~^}¸<$¼Î\÷¯rôì­\x000bVIÈð	\x00115ðéñÁ«³×o_¼À
CÜÐë\x0003×Å\x0001db@°Vd+ÍM9\x0003\x0017®òÃ\x0006|cã¢\x0001´ÏW7«÷
ÞR\x0018=4.*k8¨áw×Ã\x0010ëóãÓãow«*0©\x00196Ò¬KgbÔéQbÜ`b¶zwºM\x0005ª\x001b ºFÔTL°7¤9ä1Í"(æGÎÙiÀ8á\x0006Y4Ój
n\x0011¨åÀÛ±#b.j\x001aÌÓÔ8OM)Û¥M+v¹vÊÉÛ\x000fcÂµÓ¨¶ÜÝ{Å{`o\x0008$Ü=;ey%î\x001d6\x0012ëYsÀh÷®<Ëçg`Êî¶\x0014íFê\x001aR\x0006ÕB©Bj¬-±×Üu!n;°U¹Ö{AÌd\x001a0mðr£5ü\x0013\x0006<Wí\x0003å¶&Í|J­ÉÐúÈ\x000frnÝ]?à¯oî¯oßÍÈÄÈ\x001c\x001cÁ\x0014ÛîÍ\x001béåhb»Îlyvöò\x0002}sþòõó­ ó\x0000:/¦!î¤\x000eG«át\x0018¥+}\x001a+2¬îWp\x0002ôF\x0005g%µöHð\x0004&dÈHÈÚÏÿ\x0004%¹õR\x001býÑPÈ\x001a6¯w°{Mß\x001et>Å\x000cÈJ·Úeé\x0016vf`­ë\x0002÷®Ý·G\x001aÐØkv\x001bðc\x000fôÙ_ÿ|÷ó\x001c½4oKB3ö\x0005èzÁËÍ,jµ-é²\x0006}v\x0002ÿ`·f
%£µW>Qå~&\x001e\x0006¹Æé.±!&Ç\x00006\x0016jODå×¹xt\x0018\îÎndÐµd'FÓ\x0002jqrrç¼ÀÕDAä0¼»Ò\x000f(}\x0013e|CÓÓKS-tà2hÜÖF©\x0005Õ.ôAñc\x000b©\x000b<Ú±¹½\x000b\x0004ôâíÙ ?\x001aÓe!=+Ê\x0018°ê\x001cZ^±×>\x001b\x001dEhT³G+lû
vd
ÀôZ¯Àès%YÐ%û\x001f\x0015µä«§$bÖÉo[{£dÊò$\ûâq\x0012nøâáÂtpzwûa:a	[ë\x0014-	\x0015²\x0011\x0019QCâ÷«Æ\x001aÁ|÷\x0012®L\x0007§g¯_ìNYbàuì
n\x0007îº)Ø\x0015ØÌ\x0005+É¤Ýé¶óUQ[ï÷ªP\x0003#åêáàù_ÿ\x000b¹þ¤u¥//:´sîdE\x0016ö¬ÈÉ\x0005XSøíÿØ¹|\x0014\x001còk\x0000¥
Í)¼DSÆÚÁ5
`ØâDâØÙ ÍÒ\x0013R½45¸F<|¾ï-\x001cE÷.\ø\x000c\x000b'\x0003wf=x}7y$RzÖâÂÛRiáQçV\x0012·Ý¾Üõàõ\x0019\x001eB%¿!ºðCüñ·ëð3ñÁ\x001cÑ¥èÅêúö3U²S"µå«SèÈîï\x001eÿøææêáãOW\x000f\x001e&vôå`À¼ YèQÞkPÙõ[R]þÇ7§'\x0017ß\x001c¾9¹ Ö¢\x0017Ç/_¿¥ÂöoOÖ}ò\x001bæ½»O\x001fWxa\x0011ºa\x0006ýñý»Çë«ûùÔÊ\x0015\x000ePãÝ3\x00115Øö©M¿ù\x0006u?³þøüÅÙåÅËóÝì¿þüËÝ
Ï\x0005\x0001§w¯ýã\x00156l çWÔOk\x001e8ê0Jf\x000e°g\x001eFÜà½[n\x0001[__Ih\x0003üôìíK\x0000u\x0002\x0003\x000e\x001bëùÉñéNêÕOÖ|ý£7CNa¤_¬þ=Æ°¡ë\x0012éÎ\x0001+(ìæQq^\x0017Ôa\x0019Õ&*íãïwªúz·º!>ã\x0017\x0002\x001e?þxuÿáêþújþ\0p®\x0007ÂDûî Ø-³ä\x001f\x0005mûº<OP\x001e_>;9qrþ\x0012\x000b,v,·5,ì*GøÕ
K¢\x0001©\x000cjTÝrË¥\x0019\x0006Õì^msi¿\EóéKo±Wÿîúv>hÆÆ³\x00054äÒ æ\x0010\x000b@,OT«ÌÈD¥·þüåë\x0011ÊO×æÁsá
« æ¿_ý¼OP¶Óð>n³2»¾\x0004M.¹1Ê?ù·ã\x0011HÿxóõcÚ<¿ûZ\x0003ið#£ÁP¢­WØ¬lUÞªñet~ö1D<x¯¿\x000bþÍÍêØÇ¯V×0Mç/©Tì\x0011\SÒF\x0013»L\x0017yÎv\x000fëÓãçb2¿ìåîc¡c7}vó\x0016»í³Ûÿ3Ø9(ËºøAâGGÇ_®à1=ì\x0019óÙQE\\x0019lD+'\x001b^¶x)\x000e¢o\x001bìÇß¼¾\x0014xØ9zèìøãWÿauON\x0000\x001fnP\x0015ü|õéóê\x0003y\x0006¿[qk0Çvï o¯\x001eúæýÿuöõ
aQÂÍµh4\x0018¸½àÁ!\x0011}é¼ëIÞ\x0015×;÷ñ%ÿÒõÕ{©¯º{\É\x000fóúäòoß|{pö£èùñ·Ç/ÈøÝñÎ>bþ|û\x000b\x0018\x0013ä-ÿ\x001eÜÿ¼úø®\x0013s~"°ÌEUßÂ¤Á\x0003øðT$÷±×*â+>-I\x00160`#ü'¨±ûê
]0&ÁÑÕmí\x0012ð(\x0012Vc³)àN\x000b8¥Gì\x001d\x000cAóøjò¹\x000f¶ÕÑ£IàÁ\ELAµzàwï¾ýíW\x000côã©f\x0006ñ¥\x0007\x001f°äïa\x000e7
ZsKG\x0012µ\x0011ÀhCÆ)q?/íbG°/\x000eÞàUtGyªÿáþåýíÀÐ\x001bÚþ«û?ç!c\x000fo_ÃQÇ¡ÎÞÊ\x001cÁ¬éb¿syhø\x001f?ÉZóG:¨vhì<È3\x001bî§9\x0017jtæÓ&ã¿\x001a\x0019Ñ£\x001aÛ\x0014ÓUÚ*Lªà±Ö¥r	c|¸höLíÐíLæ	b8Éàv\x0005ÚÊ~\x001eQSrOÐ«Û\x000fæÏ_)æÂÐsúì\x001eþ`q©Mo Ø<\x0004Ö\x0006WC¶\x001cöñpÉJib\x0003é9)Ã?ØÎæ¸~÷)ÿRn²@ì\x0003ýâñêÏûÕãû»ÛY£\x001dC\x0012Å|­ÁDArÏµw`\x0007cgÃuáòäûóãËoÏ^ï\x001aó5=¦Îk³\x0010?âiE|úI\x0010ßåd\x0005\x001fßê¿\x0006?à²\x0014_:PÑè\x0007Ëø*\x000bþäÁÓÿÔ6Þ_ÄoP=\x0015ÓN\x0019ß0>õ[øà£Ú/\x001eý"\x0002ø!®'Éc°Înøù÷;ûçWÎ¡\x001c§ðçÁ£Éyáj\x0015\x000cÅféÖ­2\x0012b&Çd\¿<q¬ÉZôHéBÝj
z´o\x001bÑa'óv\x0011z²¬WfaÆËn	\x001b½:Åóþ\x0015è`8û¼lÔ\x0015¥#Ð¨[\x0014@.ó¥e ºwÿ\x0012t´ð«\x001d\x001dk2\x0006µ¨3]Ègmþ%àRÕ"pl0Èk\x0014Û=ñ'éX.¸GôÏø©\x0013`¼7üÕÕ_¯ngÍd+#J
2Ímö9cj¥W'ßÿãäõß'©1%Ò,ÁÐ\x0004Øê0á¶Ñf\x0019îX³±ÌÅÆÈ¸\x000b°ÑÊýPw£\x001d³\x001cCSæ&h\x0018g»h¬\x0015\x0015jÐ´x£#èà}7µk¶¹Øx¨¹°\x0000;tvzñÌ\x0015ênÿÎ¶fÿKýÔî]G­(êHÇ\x000e-MÂö¥\x001f\x0008îÝ¶f\x001f1¬°d°QÒ3w§¥¶ÍÝikÌÃqìÛl>|¡X/ú<ÂÆÔ~}÷g	LNß?3öU&h*\x000b¤Õ´+=Ä¼Xý5êSé3¿>û\x001eSÈ($|;²w%~\x0002Ìps¹0[Ïó#JÑ¾a¥¤¸ÙÊÅ3£¤ubf1`£Û7±Æ\x0006í\x0016
3ò:å"
\x0014^ñµÅÿ\x0005ÄxÇÜÜï*çr\x0005\x001a[]8ÌwéMÞ\x0013ô/¿?~}$»	K·Ò`·;xVÓ»gùR2Ö±BÄð%]Ë\x0012J\x0015~b£©Æ¡ßó®¼A#êù¿íò®|þåúúË§\x001d9\x000eo1ÇêñfæàÃa^fÍXnÃ«R«3Ä9þ\x0016³¯.OwÚ~\x001d6¾Q\x0017q\x0017¥\x0003t*ÃUÍò\x000e¨Ä\x001e3~Â«\Áýëçw¦
JÔá\x0017VØüõÏ\x0012¼Â.\x001fn®\x001fæ9á\x0002ÜµØ$\x0019'>Ýçu0bø©Ó\x001dËnNJ\x0004ëàäÅéË\x001dåM}î\x000cË\x0013¿\x0016pÛnûÆ´ÖXwçdÀ±dïÜ\x001aÓ¨èÑ\x000eîñ°\x0011ðWrO0|V0éö
n>}Ìé\x000bÕ`&]«QP!AéXùðé³à¦§9F:Kã\x0007é\x001cÅ;\x001esT|h"cí>Ã\x001a\x0011Tw}-/ÞïLëýLØ/ï(÷ÄÚ~¦fVÉ4p`\x0016\ì½ìtjÿoú0Þ{­?v¢\x0010\x0013LÄ´\x001bú¸c;þLêß{ÂZÜÜ\x0013~jý|äîn\x0006kÊËí)ùTªÃ<V\x0006ü¤?ßÿn®~ýAñ¥0\x0017jÝâow÷W\x000f¯ÿú\x001f÷]\x0002ÁÝý»9\x001bU	s\x0004ÊÂ\x0016\x0006¤\x000cÿ
ï\x0007Îc|¹û\x001bwý\x000c;;?¹xûòä¼K%8;ßQ¤áP×ïìOTþMt¯E<¥\x0011Ð»A¾Y>²(e¼Ö\x0004Ïvt\x0008:gÒ¸©{V÷\x0016¾;Æ·ßâÆÌLz´s\x0007Ëª\x0016Î
	¼³\x0008¹ÇôÔ\x0005vDì¸\x0008;¡a¢bë\x0014»ç=5pãE\x001eíÜÖsÒb7\x001eUÎk\x001fµx$ÝdÜ \x001bw\x001d\x001d\x0016·\x000e¨\x0014®IÌ½\x0019 CaßÜ\x0006}ôhæ\x000e)³¢µµ`H³¯Éë;¦)¿^\x00037\x0006!èÑÎMÆl\x0017èp%þîêü\x001faÊÚÀ^=z´s\x0007)bÄ³£)KT2©=·ùá·+éÞGÞ¸o=¿Y}ârQò0GÛswó×?ïn×'ãÉç\x0011
Ê\x0014iþC,¸+~¦HM~KÎÚ«7g§'g¯\x0007\x0017ç§ÇoF2ÇûO]­f"ÚÒ\x0017\x0015\x0011Ñ1\x0008W*ÃFJ\x0017"ZøImhC¤\x0004"BÙj\x0018;D\x00124Ü\x000bâSþ¹&Q<\x0005\x0011}iâIV\x0010¨[/DÄ¤ÍÄ¹ùè¨Z\x0019þtìÞsÐûO\x0005§æ\x0011bj\x001e¶GBtdñ º«\x0002>,\x0019Ä\x000f_¯þ\x001dë½qºØ¾ðíÃÁ3°-o&ø<\x001eM´T\à:ºClÛkJ)\x000bÜÜ6_²\x0008ó]\x001c<\x0003Ëñt\x0006\x001bi®fÃ\x0016JÆ\x000e\x0013K\x000fËÐCÐ\x000bÉ°°+õÕõçåPÈ%]cB³<j!Åhè G-Zâ½Ïk\x001bJÉ& åQ#îÓËÐÅ´<+Ùt\x0011øÅ\x0000çZ);A¶Ì!ûÅl²<éYËæåXÃ\x0010aÔÂFhZ\x0019½t\x001d\x0018\x0007yyV²)CÞ{`Ãq-Ó­8\x0001.¥óÍx\\x0005åY»xº]#\x001cl&iÌ\x000c§´Ã\x0005\x000b
p¸\x001a<Áaú(ù¢
\x0014µé:
.!óDæ«ÉàÆË°ae8Snï\x0000'U\x000bØ\x0002®\x0005zÖ²\x0005
%\x0002\x001bjASY\x0002²ñ¹ªÙ<´\x001aà2
\®\x001f8î±'p|bÉ&¢±±ìR¸vCyVÂEKzÙ\x0008\x0017T0Fm{%pQzÃ,K\x0004W}4¸Tô5	.Ê©å\×ìÒ×j#v¥*Ï:8­"yUèx,GâÌX<µôÒ\x0003*Cl¦
,\x0018\x001a-d³®èÌ`@ÞjN).³4p¶zà\x0014×ò\x0012¦3\x000cátô\x0002\x0017¿UôÄg%¡l\x0002gJO
\x001d\x0018\x0006néÙÒ\cê\x0007Î%6ÍcÄÎTØ)\x0003g\x001462X\x000cg\x0008®~Ê¹¢Ip¶r%¹
ØÂòå<±ùz6kÙú\x0011LLj=\x000fl¦è¬\x0000\Zº\x0001Ûáàò¬dÓÒ]-«Ò»\x0000'\f6mÕR\x001bÓfq¹aÆiê\x0001lIùõb`ÏÑÎ-\x001f8O\x0003ç\x001b\x0006.ípè>³\x0002g\x0019.,Ýâ\x001cêÒ\x001dg\x0015[Ì¥\x0019 eëKßb\x0003Ó1	ÍçÖÝ»ßC´äÈ\x000bt§éÐÐwÿ\x00023\x0013#¸G\x0006\¡\x00017`¸\x0001Ò[
)å\x001d7è³óç\x0018vAçPºËõúêÍ¦ËJ¢\x0007 Ó1\x0016Ý9liSv9Às;,
<¼]\x001eÑ£\x001aOÃ\x000b-WBzsl\x00124EdôLzz½Váa*z¶-x^Î\x0008§aP\x0007jÀó<x1¹§WE\x0005\x001dv:
½\x001eÙ\x0015t¹¨a8\[ítØËÂ\x0000<\x001f>^kðð|\x0008½C¢\x0002\x000f$=ãiôlÓà¥Hxg^À\x001cã\x0010\x001b-lßêQ\x000eUE,\x000f^Ét\x0007:Øá\x0017ã¡yCz<\x001dÊYáÐù\x001aR¡3^^­ÉO{¿*è"^Ì£m¢ó¥Ò\x001eñ`ÏÓ<ó"Kr¤ÓÓ××\x001a<tjÐ£\x001e§\x001bâ)S$Á\x000cØÖ¥û\x0001Þ~6c\x0014-x\x0016ñZv\x0015
%dô2åÅàèånÝv²Kððå¦\x001b\x001c\x0005$\x001cæ+$¶ï"ö¬Ñ³÷ä\x001e\x0004zTãa\x0001Vq89¼^Øg2÷ÜÓv{\x0015^@¼¦}\x0005®Ö)Ñ¾Ä$`ð¼L=¿ÃéTC\x0011Xz4¬@\x001dWèÝzòòÐÊÈ2xa¸\x0002\x000fïÅGIµ¬\x000c«Â¡g:ÃNØå<B\x0017\x0016o+[>ÿ
:,ñÖ\x0005/\x0014å<Äó`ãâó\x0016ïÆGô¨Ç]¯ÄrPÚï>Ñ$SÏî°ákðpöÒ£\x001a\x000fÌw\x0012v#<G2YÇ3·ãÞX)Oô¨Ç\x0003û\x0017\x0006¬`^\x0018.:z[\x0001Ù\x0006:4µéQOg=»ÇCñ%#º\x001cdê9³ØÊØ/Ç¦Áóz\x0013\x00153ê
\x0018oùÑcÓÔs\x000ca\x0003t¾à© /×ï\x0008 LãýôY½·¿÷¤×wÛç7w'®¶Ú%veôº\x0017\x0013\x001ekº\x0013
\x0013ûv:z½\x0001¦QÂ\x001edü×HÆ\x0006\x0015\x001b
Èè\x0000ZHY(C'Ï,2Oªe\x000e³^
o$@V\x0004d"ÖòíôñÌ#+B\x0006åY\x0006\x0013©L4Mó\x000eK1èRM\x0001ËÕítTÌ\x0005Ë6\x000côÏ\x0001ó¬\x0012¬,Ð\x0005uHq\x0017É;=3¹"¦\x0005gå\x0015õ.äB­áÈ#VÊ6"jKìÍEÃ±<ëÐÇ\x00154\x0019á©¼ZÞíXF£fªGÍ\x0015×&¢Ávi?ó>í6úR/¶\x000cê·6\þsÐl¤Î¶\x0006&ÆÎ:¯ð
ÛögþéR*\x0019ñÒß«¥xäÜíq4å-)fáÁ\x0008²°G@æ}Ãnú\x0011¥^âòàÕÙåéË×sØÐëÙBàL&ìÕyXbÕ.rgVdÛj6°¡NPÔõl1s88Ãäô\x0003Ø\x000b\x0006d>¤Ål\x0018kÁ¯j6I)Á\x000f[haÓäm@ÃRCüªFå.jEZ\x0019Ñø7qñ¨iJãÔ
l!Sj\x0010\x001d¡³\x000f\R~\x0008GèæE«\x0001\x000e=Kô¨CqZÍpK.F\x001e¸¤ôâ¥ 1@BZ6lL)l©H¼\x001a'\x0002\x0008g\x0017³¡-JZ6ce\x000fÁJ]\x001aÍE±Øò¦/½\x0001\x000eÿ
zT\x000fâ8\x0004\x001e\x0012¤ïF\x0003·^\x000eÎ5Â}úÍüöë¾J\x0014*{\x0003Î\x0007¯V÷\x000fðk0\x0013Ñ/,ç\x0008?ìvÙJ,Xâ­VmÞì/	
ÿ\x0013Çç\x0017å?1
(;p=`\x000eìê\x00029?B)	V«­cµ	P¶áj@
«¡ì(\x0000XX(£\x000b
+³\x000fÀu!e=¡³\x000bFF-YMÊgÓ%#l^h\x0008É¦#®\x0010\x0005x\x0016ºR=BùÌFòLPªl\x000fdB\x0006Â@%î4¾t4@BßeÂl9è\x0008\x001d'¸\x0016Â$\x0001 X^%)w¹0~Á+\x000e¿ß\}þ@\x0013TY²\x0004¬¿]Ý¼»}?uuÅ:QZÆ(¾@Öh±W\x0007\x001b¢Ý\x0002ð·sØ\x0012¿Ým ¯ùhº¯8¯±NéL|E·
øvx*ñ0rÒó3ÍÇ3\x0012ÌN\x0018³Ó­d¾È\x001a§w§×Õðal"ú\x0006>å8¦ýIè\x001eDÐÙ·²\x001aºt±åå\x001a>ä(Û.x1úøsnGÄ³/áºH-CÁ}QÖ)2ÿdZÉËf§+ \x0002\x000f#í©\x0017n¯x¹<4|½ÿðr¼^·Ãû_Çw)zT\x000f_*\x001d|pòab\x0000_!õÂ·óâ]:ô¨ÆZ_ÒÖ\x000eùòm%Û\x000e\x001bN6ãý©¾>|&ó\x0014²ô03ë\x0005°Ý=>\x000e#|F\x001b²JÿæÞ&¹\x001cI×Þ
7peøÿ1(%SÅ6TQbZgOdÄT²"\x0014©JÕ¨§w	=ýF]£o\x0011¹^É;Üq\x0002Ás\x00028§­8¸ç¦Ô]ÙO!\x0000»ÃýõÄç´Æ<È*RºSÁ\x00149¾	îô\x001c\x00067,\x0000dTZ
("½ÀC\x0013õc%@Éjþîh!,Â=\x001dK\x0018©\x0014\x0015ÈÉ\x00074\x000bU´óÍDM\x00035¾P	Ì1"a wD\x0018\x0002\x0013ÆÝ\x0010BÛsmd\x0016\x0013ÊB\x0018\x0014Õ\x0006h©ÖXE7ßNÑB\x0008µ7øÓµù\x0016qÑ>\x000b¼¼\x000bç¢Mx 2ouç9¦;ØÁ()KÇ$w@\x0001à|yj\x000b!(áO;¡Aõ^$t^£Lä\x0004\x0007LYØÅ\x001ajR]ÇÄx\x001c\x00002ä\x0019\@ÈU´QÌß%-ðì c×WÖú\x0019Y\x001aU²	0Ø­õ£h³\x000fÐb5m' ¥¬"U\x0003!ÛB9ß5\x0010\x001a(g6"t\x0011Zj¤×c\x001chm¡ï*k#|w\x0019/: ¥¼Gäns2 \x0019R]A¾Ïï; ½Åó\x0000i\x0005­¤\x0015Ò±ÉÑóÍ\!oþöþ»:VJ?òéë\x000fZkÒ\x0011Æ'\x0019øç\x0005\x000cQRC¨Cõâéã\x0017\x000bÀ`Sï»QÃ\x00020a"¹0i\x0000{
Md±¡Ä\x0006"\x0008Û²ÁuéFý KØÒÌ5z0Jå\x0019Õh¹v,!°\x0018íóçOþ=>+ðcà²\x001cY"â:Ï
^\x001bÈÙü²\x0010<tüP\x001cgèLèüâ?å@åc\x0018\x0019¼
<\x0018øifÔ¢\x0004÷Ì\x0010\x001bÛÇÍHÍh\x001aN\x0000þ4¢¥ÓIE*É3àôñ4oÊuigÂMüifK^Z¹}\x0014¼Qù\x0011¸}a{8lFÂcÚ\x0008ç³ü\x0003zÍ±<z¸h\x0018n&­Ö\x0002\x0007´øÓ
\x0017uqí*,OG½©G\x0005\x001dpÐUãLÇg
T\x00021¥|}©\x001dì9¨RÁæÔV\x000eªú\x001c\x000cùÕaµz¥:àà@¸\x0003|÷Ü¬
bOÏ$¥Òb9\x0010æQëE\x0007\x001cèr»Ð\x0001g8\x0015\x0004Íª\H@ýøÉ·{Ô9ØÁ\x0006S3]\x0001SÌøU\x0015eùV!®\x0018çHÛá ·¬}»	2b=9>_V-}Ô\x0002×\x0001§±¶\x0003ÎRþ\x0011^°\x0002×\x0012\x001d§\x001fUI5³\x0019PhÄækÕ\x0014Cb#'÷\x0002
jãðÈ\x001fi³pÝÛ;ß\x0019ò\x000bòÂ*\|T:ÛÎ\x0006eøÓÌ¦Qh%A\x000eIº\x001fÈY\x0012\x001aÌ:àpÖIÇs\\x001fpv%ÁÁH\x0016òäTïqøøñJ0øb

YÅ°g·É\x0003Þ°
JSñbMËÅe\x000eG¡\x000blb}l9;M>ðín"\x000fµNH
Ò&äÑõÊFèÙ@:ëf\x001a\x0007[è\x0014ôªªºau\x0019]Ìí\x0001°vPOpÔà\x0003\x0017ëlÔÚ\x0000\x0007C¥êãÖ²dKJ­C¿ëü3Õ&8ñ«ýæ?\x000fEöº½Êh¯.îî7EÒ¨AJ7\x0016Fÿò¡\x0003\x0001£ûéô(£½:8{».\x001e Á\x000bKhG\x000b\x0014=JKÑ¹1ô¶\x000cjµv[4sÇá§ÍQï,\\x0014$&c\x001ciòEÔ\x0010Ü­\x000cþl_·à3[:¨¹{ÛY+IF.ÆqÕe\x0007[©hhd\x000bµ¬S0Ö+ËµP%¹ÌEý[²E\x001cQ\x001bÛÙ,\x001528ð15­c47>¥ÑÔ÷_ÿþ+¸·ÀMÅaï\x0012Y»äÑ£á0ihÄhSRØ9;>Wä»AÓ®àá{/þ´ãiê`L»/òÕ¥4U-×ÕG/å\x0003\x0001éý0.y_Æ')Ú\x0007Á6¶%ÊP\x001dÐ\x0010½nÍ\x0017!\x0007?Í|ZSjØÆ´$i Ò¦Ë|ÆÛ5Uù\x000bù¤·üÛ
\x0008ÂË´)åÃ!`YEé¶_@ûS\x001e5¨,\x00024ô=-\x000e\!ç)RarúOÍ?6\x0000b\x00061§\x0010[\x0001¡ñØÑ'\x000e¥^/P5Cò
Ö5^,\x0006t(·íd; )ÑÙÄ¤ë\x0012\x0000.Ew\x0000g\x001aàÛø<^j¾ã ¤/<à£}øÂÝ|¿\x0007÷ÍþcQÒGà\x000c\x001e$RH±ID(~÷\x001e\x0006pYçQærì\x000c`P\x0001o\x0011) XÓê¶¢\x001b[ÛF,ëX
Ê[cï\x0001+ù\x0004T \x001a\x001f=µbñP&,jí\x0001,C~:ßÿiìn63AÛW­L\x000eEQüIÂôey©ì#Ù¬f,P\x00070X^>Ëµ^B[i¤g¨q\x0001w+\x0004ýoüi¡yÚ\x000f+esh\x000bßr»ãS\x000fþ4q¥åh¿À¢"Pû;jK.PÜÁ&®è©ÇC}#ýn\x0015¹\x001cöp¹_1\x001f!0
\x0010:0}~yñðy\x0003\x001aHÃ \x000fN\x000f4®îëT¸×æÞÜ\x000e\x000fÎ_-ÒÕ]\x0006ç¹>Ì\x000bEj6®¼lÉya±
pêË·ow\x0011ã?ÈÕÀÏÁÍ«ËË½æ^ç \x0003Ð:
G\x0011\x001f==ª\x0006ëÆª\x0007'/\x000eON\x000e÷\x00167=¯Kúf\x000b`\x001d)CÜ^\x001c\x0003´Ò\x0011°\x001eç¶\x0001ÆþYøÙ\x0002\x0018´\x001f|\x0006¶ö\x0019ñ*G:\x0006V\x000fÐ\x0016¼(;?[ðÐGî~\x000fÚSK&ýR÷;LÀÙ\x001d0¼
àO?pTLTúôJ¤î4\x0017Ì8µ×Î{÷Küøñ\x001e{àÈ/ó:¹}w{¯.¯/ï7XQ«èÛÃ+âF\x0008ÉW´²îàõ\x001dî½:<>|»\x0000
Þô\;ZtT\x00073×sU+%üB=rL}û.ÿøöñÝ`ýñÕåÃÞ\x000fW÷{×Ó\x001aQw.YÔ\x001cYZOm`2ùâ#ët|tx¾÷ÃÑÛ½ãAjãâîÃåülòüøG¼¾Eç\x0014Þ¦Òÿ{ñëåg\x0018çS^á\x0017××·Ð«¦efñÃåõõ\x0005 \x0006ð\x0018²§bS#ñè<³	X\x0006êñ³P_Aÿ"$}qx||þñðÕÑ	MQzQ& \x001e\x001c\x001f§ÿ\x001aS\x00039ÔÜdÚO
ê\x001a\x0016Vfjm($ÎD·kj	\x000fÄøÓ-D.×LØ ¤3¶*=zçk½\x001a¦´Õb£\x000ey¸-T¢Ö¥]\x001b\x0008î\x0018»Ô¶÷bËÈ]	Ûù¬y\x0007-¸\x0003>ÀKý±Aj	ú±AH0Ë\x001d@\x0011 ¾á%l!¸wÔ]aëÏæ·kw²v\x0005ý\x0000â\x0007_éå!±]ì
½Â\x00032É Øt³9Ö(ÊýãÁ¿mû\x001c\x0014\x0011ÞÐÃËyÂë9¤\x0006×Cù-°-v>\x0000¶%©UëMå}\x001dòÆ]có\x0008Nì\x0014leu$8Y\x0010°£,\x001bÄüo`KhöÆ^n(iÍ»Ä«ß\x001fàõ
I9ñ~wÜ¿¨«/\x001a\x0015
hØn} ïn¯¾þùÏËµvÏ9÷,äJ0\x0010RÊvÏ\x000bÏmÈ
{ `RÕåüA<;=zs8=¢ªÌ©¯\x000eH¯H++Aæ²	¤>ø\x0004	x7ì\x0008õ,eÀq@@.>eÒ\x0003
\x0005?v\x00043Qz!©£\x0007f°~
!Yz\x0019Ò,»¢\x0004\x0005f×Ki2\x000b!%§¦¬à6Ö|þúðqòÇ»ËïwW\x001b KÄ\x0010¡ØYÐ®Lþz) <;üùìh\x0001$L\x0018{eË Yá0\x0014å*är{MÙ»älm;dÙ\x001d\x0010 ö,m)$Û \x0010ôÙ\x0011#\x0004Æ¶Ñç)ÈH"¥X\x000eÊ6(ì
\x0011ÞV\\x0017"\x000c\x001e¤
©¨\x0016\x000fN3h7õ_>IÿE[\x000efrÄÉÊûûõ>Åb¹W*
(Êóùc@\x0006Hã\x000cõ·|ûv\x0001%tV÷Q\x001aV^\x0001µfM¶\x0008\x001bOÍbH,ÃÐ]NSEA:Ü*w¸&Ìè\x0014\x001fî7ÎbJf2öùQÂ\x0008¬\x0008B@Ú!¥\x0012l'\x0015J\x0013í
\x0013êºÇ7ã2L¨Ò§\x0003.I\x0014\x000b\x000f¹ÌVm¾¾\x0017SNí¢\x000c09,8ÂÔ\x001c]C\x0003b±z£!Z	\x0011íZÌh©º5}só¡AÍo.wwÊQ}¢ë\x0000\x0005É£v`Ìv\x001eæ0­/q£Å\	\x0002êaìÿ.ÃÌÛ3f¤LO\x0007+²9rÛîÍïö{ü"Ð\x001c¡\x001eÔ\x0018óáêâf=¤UåES »Ù­z\x0004ÄÿÔû5AýËó£Í4y8Y\x0004i±Ô\x001a!³´\x0007Br§n\x0010ù\x000bm\x0001yùùæ·ï\x000fÃ'Ù\x0002	QßûË»ûõ1$\x0014GP*JAt×¸Sì¥6
\x001a\x001c\x0007ÿ¶)N\x001d\x001f½\x001d\x0007(?ÒéiS&Loð\x001eBLj6ÑFk³=¦úÕýñEMÙÌ½7@_Ë\x0008.ºà4ËI}kC \x000e\x0000í=ìÎÿªÉXü
äÑ7Ñ­Æ·àù¨9Ëa¢Ì3A¹NÌj'xÊaã\x001añ´ÈRXP¢S9åå)¢ÕÎådF/Þ
÷î740O¶^¼
ùZ\x0003%Ï$\x0017Ã³¼r!²«\x001b¢1kÏq"M\x0019®¸ Q<Ú6.K#n£\x000bú'.¾C;àZi´ñ\x0018Ùé\x0014\x0002óäÝ\x0004¢×	ö·Ë;å¡7WAø§L\x0005öö×«Ûõ;M¥­\x001f`%è­fw;E®4GKÐ\x0012n4þwMò½ýËÑéùìf\x001b0j\x001c(ÛÎ\x001bÁ\x0011\x0017Gd{\x0007®×Î 5ÜZfH"¶,¿±1r½
§\x001anGx©Üï×wSaK\x0002\x0004\x0007äázý\x0005lJ¤s t~ÔÚQ\x0018\x001dq\x001böáÛ£ããÃóãã$ÙB@%P\x001e\x0003\x0000á3\x0013 Ò|PlÞ:»\x0000J\x0000Û\x000e¨h\x0014NZAkÉ\x0000Ðê²LÌRÀqÌ·\x001009Õ¤h­æ7©(\x0015b»Á\x0011\\x000e8Îæ,_A\x0007ifÏ+HasÀ¹\x0015;\x0001\x001cçr® =¡jË'\x0016\x001cr¥ß\x0015 \x00061fÀäà\x001b\x0012ÞÆ{ZAÁ×oV\x001bÞ
 L´¯ }bh	q\x00009\x0019ï±Ge7¤]Þ
\x0018IM\x0006J(Q°$¹ûÓGµÝ\x0016üzuá~\x000f\x0003\x0003_aÿõõÅ\x0007|½þÿü¯ÃO×W_7DðÐØ\x001d\x0019©%§C¤a3£A"ôqÌùúøà\x0005>Ê\x001eï\x001d¾<>z3w\x000cør&±/mAÒ~Æ» "¢a>5\x0015ºwðAóq\x000fg\x0007UZËY/YÄÝt*Ön>\x0019~ûôÛÍä÷½ØûñöæþâjS(\x000c\x0001\x0011Ý# \x0018N[ÐPé@
ýô\x0011Y!\x001eìýxzòöàh6\x0016þvýÞ}¾\x001ez\x000bT:\x0006\x001dµù_¼\x0016Ñ;êÊp-+ºI\x0002ë[z-å$"Ua[í«ç³~ë\x0000kÆÚð,	UDÈ+XËxñì´\x0015lÆ\x0003È¸V¼¸ÀÓ£¬\x0017?°w3×\3^)kkÂs<a\x0008T\x0004¹\x0006$zV\x000eðnÚÏj§#\x0003ÝD\x0007ñ¥¤Å\x0013¼x0\¿­ÜÑâ=\x001a³põ¬Â¾pz¥+{ÏqOHaÚEhæØð#[ù\x0012\x0005ÁT¾\x000cx\x001fp\x0003T(í\x0004o%¹Ô§-µ;F\x0018cNþQÅ\x0003Ô;Â\x0003\x000b?xJ	¢\x001d:\x001b\¦ÛÝ\x001e'é4\\x0015i´tt)rçT/+«\x0006¿#³,¡N\x001c\x001añ\x001cO&p¬B\x0006x¬L\x001bf.¶v<¸ÔBó­\x0006á\x0007E\x001aõ üà÷°ddvcù\x0014D	J4
©Ø1f%Ã¾©ãÆ\x0008awcZVÙ¢6>á²RdL\x0017,Ù$¼ÒT¢ü\x000fr÷øÓxsX
øÒ\x001f8\x000b\x0013*ò$;¢®ov
D5\x0008t&÷\x0004#\x001d5\x000béôQ¦ó/Í|ðr¦bëÇ5Pí?.èJ×niuÖleZ¾Ûo7J ^\x0004¼Z5üâánC}\x001fL÷£9]\x0002l4FEVñ<¸\x0014}ÀûÑñê_ö\x0018\x0011ä¯\x000fÎÏfú
â@Ý­	ÑæÒ\x000fÌSgDH3C\x0013!=yì\x0010_Ûk)Æ%0[\x0011aÌs;\x0012¢¡z\x001f
~ý×ÆþíîÃ;ncp¼ÍqïåíÃÅZB­£iØÞÀÕ3\x0010\x001e ÖV(CL§8ÿ{&àö^\x001flF\x0003qþüÛ\x0016ó\x000eLh)ÄÐ(³!\x0002öém\x0016qî\x000eþ¶ y¹*Dy\x0006UB£*Mè"½d¿}ü]}p|ÐÝ
ñîñÅÃ?6>¢D×n\x0000lù|y\x000b\x0014Xàq<ø·MA¦÷øàü?Ö¼¤\x000fP!\x001fzP%¾h\x0001©Ïò`\x0004\x0005	 êô\x001fu»%\x001d\x0005pËIµsôÉÓ¢ZªÌu\x0008:\x00191½[T8ÉÕi^\x001a²©IlQÒ°À
óY2*¶ï\x0012\x0015ná
³\x001c\x0015»\x001c|\x0014ì!zeé©Ix¼ev½m²:îËw@à@9Ê<í\x0008wcÅ³¨wÌ'¹víV%
+õyZ\x0007A}FZí\x0018\x0015Zßð§\x0019UA\x0001Uörcò9\x0008\x000b´DÏo¨
Ë U×\x000eHñLÈU\x000cP\x0019ks0}êÕ8 {¬Ðû¡LÏ\x000eH±ß3ò<déòG\FÝ-©B*üi'u6w}Ã¸ã(Ì)HvÕî\x0016õ·¹\x001c5%z\x0018¹m\x0007H¥eØ©\x001d£B§\x0015þ´£jª\x0005ÖòDn¡KXws¬¾øþË;\x0001²\x0015Px#9×·7÷W\x001b h2D\x00101¥ú\x0016ÖX
ÝÆãËò/
^Ã¼Å£¹\x0017¢\x0015#xÛù·Q»¬®
Þ'ùÈ.\x0005\x0010}®ÿÚ	"¨åß6D¥²®º\x000fÚp"((êJ¢\x0015Ý	¢Ç/íÛ¿´
ôÆá\x0003Ì²ÄHRÜRAÉ®\x0018#f4¢id4ÞÒ[\x0016Ì¸E×\x0004îxGf\x0013\x0002:¿+Æ Q¡SVF£¨e\x0008E¨jÒS7(Víj7&?\x0001\x001bÒ\x000f\x000cdsa·ÆÑÎ¥a8&zg\x0006*7ð·m3Â«\x0007\x0011:Á1RâÞèü®6£Æq)ù·ÑSý·i\x0010 ÉÄEèß\x0019 AÀÖÓ\x0002c«]¤ÏìÙ{OW\x000cëcZ¿»­\x0008rù·Ñzª0IªäÙ¬(;3Þ\x001a_ÊòoÛq\x0011tF½àp\x0010PfTqwß:âí\x0007Æ?cDÃÜòvdBµCB\ÅØ|\¤,\x001eÞE¨\x001a+x\x001aÂ³h|ÓË¿m\x001fZ\x0019Ö·3É)ã@º¥).ß
¡D'WölEº\x0000M\x00108P5gÍK>Ðîê\x0002L.¸AG¼Õì8Åóm¼ñÝð¨(\x000cÄàÎî\x0017fG5\x001døÒ¾4\x000cÎüôE\x0012Á:¹3Fð\x0016óo\x001b#h?\x0012#Ô%P\x0017¥¤×CP2Û\x0019#6×çß6FhO¤o-
;;0ú\x0018µÙÖ|ëoï¯>;b$\x001e&1^ß]ì½Fµ&u²4Z:-¤ã\x001a\x0000\x0003ã\x001fW@0ëõÙÁÞkü«M\x0016«wl;¡f1¦ÏÓ\x0013¡Ñôha*Ùn\x0008à`#¡`r$ô¼\x0019I¾#\x0011]­á¨Pa)!¸y\x0006q25G§¨v³^eÃ\x000fÚ
¬Á\x0016xzR´ux=|ÜWÐ±\x000b©	QUg9\x000fí¨Ý\x0000»¤b\x000f  ¯ä^\x001b|ÜÎTH¬ú®\x0008!>¦Ði-\x0014uT¤r\x0003×2Õó8\x001e¹\x0003BJè05P´ñäãx¡\x0014/aÜ-ÄyîFµ\x0012\x001b"i
bÁ\x001b5\x0016\x000bÖHS^®¯JÙÌ(EüôIÂÃ'ê^áPç½³Ïkù´H÷\x001c¼(²N:0¹WÎ'ûè\x001a\x001aììÏÓ\x000bxvðj3G.ßÂ¥¢Ïª\x001a(w¦ø©ØÈzg\x0016ëJ;¸¾üñëÍ½ÁòO14¤zsy·÷æâ&}Öï\x001b\x001aS¨ \x000bOI!ä\x0011y\x0010ÑÎ­­G9\x000e¾½7\x0007'éÓþ<Û\x0015´BIH®\x00135\x0005Ëd§£`5\x0003\x0017V/IAlØm¨0\x0005&t¢jË&;¾R\x0007*ûô°¾\x0000®4ýÛì#b³lw"Ô(I¶^Ë®©ÔXæ­»P5Ì¸§Ef|zçWo	\x001dN;D}4s¼\x00055è,\x000f\x0002ïH9©oÉ\Á"\["×Ì:>ÞÂ¼2MÏ3)D¤f"P~ã7/±¶¹UÃ5¡Mç\x0016\x0019ËùÑK\x001aÇTC\x0012\x001f½4øíUb\x0007^þí\x0005ù|!ì6YV\x001d%Ësâ°ÕÇ\x001a½¨8ZCõíWêÏûÕKQ49c`\x0001TL7lÉ\x001a/~{øú\x0007ø Ðµ?«²°7ß7Iç©<¬\x000fT5Öïr|bcèrÞª*ìÍáÏ³Ea+@¨ôÁ\x0016@\x001fM\x001eQ\x0002%\x001f)\x001c\x001b}\x000fÏÈ;"\x0004	};|â^D((}\x000fr\x0007yj/4ìÛ¢½êõ¼jb+!\x0014áØ`\x001a	¥Ï\x00117èZºãa^	ËQF7¯¢ÙJ\x0008û66®!\x000cë%­`ç\x0004)Ø¨
 »\x0002tPÅ?MQmìNNèÚ¨ù	\x001bÄwvEÅþ>þ4\x0011:	
®z¤\x001ac\x001b%uWhN¿;B	²Ðæ*hV6¨¶\x0002BG¶ÝvgÆÆÃS¦×­khò+\x0014\x0012å*w\x001b¸·, jgGÙÃÃ#þ4\x0011ê\x001cõ 0n>ÇÁhÌÍË¶ÒÁ\x000b¡·ÆÚ\x0019	8%4D$\x0001òf
>ÜÎ\x0008QìÖ7aÁ>$\x000e\x0008'ÀrH¤Ù\x001d ¼½ùÐºZr\x0005\x0012\x0008y\x000bZB'JÄ\x001däî\x0008a\x000bÖ-Nfõë@ÏÕ6\x001d¢¾»C\x0003\x0017ñ§Pbv\x001eå#½\x0005§[Óëdw_\x0019k&B³¡\x0011Y^Ïs+?Îeaw72\x000eíG9k\x000f\x000cÉ\x0003ÙÖÐW©õ*DÍt0]ÏêÖ«D±µ\x0004Vm\x0015ØwÃ\x0006ö4\x000eºX\x0017º
2\x000f\x0000\x0001'BñèËPÿ´vÎÅ]àIvÎ¿M|>\x000f/\x0001>¡¨ö)]Ãì
:Ìí\x000fû»lõ\x0005!·M´	\x001e3>ømyÔ´C¡]ð=î:Zùó\x001aËÏW	£e's\x001fÍÖx\x0012ª~òo\x000bµYF\x0013LKL¨YÊ;Ëêkf7'W*\x0018)ø@IMÌªS Z,ÞÉ×ÕB h´Ì0!î\x000ekòôiìä"
MÒâh_^ÜÝ]Üoa5ªpäß&D\x0012Í\x0004DgHIÇ*Ã9;Ïï»B4Ø\x0018qJPB¦ÛÃ*êU¶EÖU{¹KDNBúÒ¹c\x0014>´¥l¢\Ô\x0010Û\x0015âã±EPØMG\x0019¿\x001d!z\x000eGp\x0004Ùn\x0008áåx?ÿ¶\x0010tøÜ4\x0005â³¹$Â:IDZ(Mÿ][\x0000BýGþm\x0002\x000c<Ö0zE\x0002\x0001°jÉ
»\x0001Ô\x0008ØèÉ@ß·£¾o\x001f)\x0003g-­ÁÅÞl\x000f¸55cÓ9¡\x0007"ÈÅå\x0004\x001côDð\x0017\x0016~'|Æ@\x0015RþmJnyÉ\x0012ñZ\x001a$JËG1§²>ìæ\x000b§pÉ¼»Éì_4Æ#*«:AÐ\x0019¨_Ï\x0006NRVp\x0017\x0011y÷>#¾oC¾LðÌB^á\x0017Kø/±%¤½øb¿\x0018ÌMÉã6q<ÅÕgüÇü\x0014¿VàI9,\x0004$%n¸¥*\x0002d0¦ôÏ¹äÅÑ+üÇ@Èk#ii&íAMÞÎ¶1ùÀE+Kñl;å'Õ¸»Q¡\x000c4ö£â\x0011
1ú\x0001)\x000brÛIÕ±^Òz¾p+© \x0005·jÈ=óé.g%v«§D¹{QËÃz\x0007*#IúáðD@Udån\x001c\x0002ÒÊK]¨&E¦U
¥ú2Ä²\x0001&eø{Q=f;QÇQ6\x0000\x00031<kÃN\x000e\x0004éæLÇÉw\x001e)\x0018ñeÊ\x0002L®¤\x0003V4îw»OqT°ê$=\x0010\x0001Ýä\x0015ËèHi\x001cÖ³;Tn%ï@\x0005q5jÑ\x00165,\x001c8):9Ô¢\x00175}´ýè:WÕJªÐLßßÒ£úªþ\x0011«¸w\x0005:P3ë!5:>\x0012iÖ©\x0001RÍe| Ðº-ê»øþ·»Gkú°wrñçÿ¿Ö3QÞx*Æ
QGjóÒE¾FqvÂ4ßùÞÉÁÑ?R$æ©xxí"(x6§%s\x0002çYÃh\x0008\x0017Ù\x000eI?YÙÂÄÃ5\x001b"õh4×U'©,Ôä\x0016¨¢¾üëÅÜÐ_OS\x0008\x0003Ï2ÄTüVPe0ær¨\x0014	úüùÒR\x0008"ô%)5cG·\x0002;?Ë?\x001fx6 $=Z$Æ3Ã¤u}PÊ½¿þû7ÔÛZ-Ôë«Ë\x000b½®¢\x000f%a[&áGð\x00029öúèðMöaÀÈ¥Í¦HK¥ù£J¾pµwaZ\x0019¡¬Yõ1R9mb¸\x0016Ò[ÏµëìF#$MØëûØ¤ñ+Ëx\x001e|y&ÈÉ¹7]Lw¬dÑcBR%|m\x001eÎ³Î¬´1BUéûÚ\x001b]\x0004dN\x001b]´\x0014Ö\x0005	=$6vA¢Zá\x001dÀdHµ»d]övH\x001b°Í\x0013 S¨ÂEuaÈÂÎ I½k%#AÂÔ²Ä('\x0007Sv1òð \x000eFG×q\x0014 ô§Æ_[®s¦Ú A¢3ô-d \x001d¸\x00083?< \x000f\x0006oÙmVRwßøûça\x000f-¥
´\x0011bÉöþòëýÅ
É,a¬\x000eLø\x0006Sî÷#á¬Î
Ü\x0006Üäb\x0001ÔóÃ7o\x000fNö\x000fßäÙér¾øxñõþî²ü\x0003²ÄwÿÕ¿×ï&æ&~Ý;½¾úvuy\x0007LÊe¦L·÷÷\x0014\x001eÎAe\x000fût
3ÏùÙ´V:\x00128ð$1¾}@\x0006S N~::<{³uóáöææ¡^§!\x001b\x0014E\x001aÛ\x000c\x0017u~
{góDiø6³Ùè6³M}Â
dº[Ñ ÷0f4'¡&´ sÞ8­\x001b&Þ·dW®Ð±l2âí\x0006ßTêÜÞf@%6
!ÔlÐÔ\x001eUÇ'¥3\x0000ûMç[
>©a6\x0003/ÖÛ±IôT¥è\x000bXG
pÉÉy¿\x0005%$\x0013\x001c`n	§KuÀ\x0005ç±\x0018à X3æÙ`àîl\x0010\x0007áO+Á¢\x0006x¿ò.hÏiò¶z÷ÛÃõçß\x0005Làé«Jú«ûÿó<\x0019Ëûul\x0016ª«\x0013YâÉÝ\x0012ô3ZúB7É\x0000mU=ptòvïùéÉÉáÛpP¢­m\x0007\x001eÍ\x001aðgÏKhÜóÄ'¤Ú\x0001ßãf´¥|!\x0017|\x0003ÉÙ3àË¢	O6]\x000bÞ§ß¯>ý=Î;ùóÿò¼ù]\x0007Êu¨ðN\x0015%IÓ\x0010Y¼ÔY;:­ætÔ`\x0013sD\x0016e¥\x0016\x0010³ÍÍ·\x0000_=\x001dÖ	lK\x0006uò\x001dd)$Ëé0óÛò~sªµ\x0002Ý,û!­dP\x0000§7'2zjOd ÎEd£Kk)¿ÿÇ§ÛK(Ý\x0007	yü\x0019\x000e¸G\x0012*eÒæO\x0017iî\x00186hG¥µªïªãÁhÌâ\x0013ñ?\x0010Nüø÷à¾\x000fç ÍÕû«?ÿ;0Ï.S\x0011Ë\x0016Ckéñt\x001aa"ê#£çÉ¼\x001e.àG°}©\x0010P\x0011
}*@°w¤ÿ\x0003}ü|óËo\x0003Ãyã¢OëOàáA ¾ñ,\x001f0k\x001d¡±ss£ KH²¥|
$Ù2>\x0005l	ÿõ$\x0006\x0008\x0013þ«"Ýgqýi¸goï¯RÀüùòæ~ï/\x000f\x001eÖ#«
Þ[:\x0006è3¦0Uy\x000e·tõíp|úö(\x0005Î¯\x000e\x0017òóçÓu%5X\x001ejÖ\x0008\x0006{æR9x@ÿR\x0010Æúï-¹èhµqYE[?¡¦ËÔ\x0018\x0014Ù\x0012+á´.F5gÀ\x0002©¸¼\!QIË\x0005\x0003³·å¢óßÆå²²\x0015î/\x0007«¥õ¢\x001a\x0016Ü_fk°´C];C\x0014Ü`}\hVç
&C\x001fØ§ïßÕÕaAÅñÕåÃÞ\x000fW÷{×éz;ü~wñðq­\x0004s\x0002úG!aÐåæÒIÌ_GcG_óèð|ï£·{pÍ\x001dþ|vpþÃü-WøVáüS\x0005,oO\x0014P?O\x0014\x0010eT³ê\x0013\x0005,½ÝO\x0015\x0010\x0006(áÏÓ\x0002üúñþ*\x0013\x0003:øSrKXhrûpýç?×y#
Ò\x0001ïØhÎ*B2R-3AÍe\x000c±¼äôüøp.4\x000c·\x0017ßnÁA
\x00163­äÙ\x001f~½ÿó¿¿­µË\x0002f
|¿\x0010½H2±H¥Ä#\x001f)-Ö·?­qìµ¹ÿ%þ%9øÖ.x¢ÎÍ§Ëµ×\x0004Öú£Ã\x0006ýEØ ]¹7ÚÙèã#\x001f\x000fN^\x001eN\x000fo©PPøI5 8'\rÕ°ÊJ:OÕ-Åén\x0016ÈaáÏR\x0016ãð\x001cXtÀô)°Pü\x001eíDü¾\x0018\x0005bAcE©¢$åHÓ²\x0014\x0018íú¿\x0011¼AI×°.ÚÂ\x0000¡¸Ö\x0003}\x0019J;Fã\x001aY~{ò\x001aX,¸9øC\x001c_qzØìA¹\x001e\x001bÞòr#&X\x001eAêLC\x0010xsz2{nïÞûï\x0006£Ð>·¹d¤y*dÔÀKÛ" ;Jh\x001f½z
Ït\x000b²QòÛoþÓ*:\b÷1àY\x0007'\x0011Pi)\x0011Qã3\x0016ûòFl\y=\x0014ê³þÝ ´__Þ|¼¼»Z\x001aKæ
_Vq7kzò\x000cJÈ-M|á<<ùáðìèíý»\x000f_ò/S¨(!¶ú\x000bL
!@Ômã«¢ÐÂ
¦ÎEy¤¾'Þ ¢ÛÜÎf:SÑF:(Ê¡\x0004\x0018Þ½\x0014?#Ùÿïf:'\x001aél>|¸v_\x000c]P\x001cþ`\x0015g7\x001c}ÙæO+ì3eµÉ=©ií\x000cåa\x000e³/_Kàê\x000f+¿¬sâÃ\x001aE\x0013èñËÅBg·Á«¿¬lþ´ð\x0016A­SYÑ7á\x0019Ã­}[DW/k]<mÉª¥ðÖdn0´Ã[?×§D§D+Èû\x0000\x000fºÃ²MI\x0016Ó;ÞÌV ,Á®Â®
Ï\x0007óLÑÎt%Ø¨93 ü6lª^:Õ¸t>°×\x001ebºÚ=%\x0011©\x000f?á9»Í±P¦:\x0016ðÇ6<\x001b©î%m<e\x0016Ò_Ò\x000b\x0001½£mèêc¡Z\x0005Ô0Ñ±\x0008!w¬\x0000±ðPI¨\x001fÏ×ç[\x0017O\x0007ÞwÒñ£º\x0005\x0001A:\x0015qÛBÅzñbëâÁ¤ë\x0017|ÈS	v\x00131Û\x001c\x000c-ªÅ?¶áÉXL\x0014\x0014ÎÂ(
Þz^ocòt}×êÖ»Ö'Ï\x0002Û\ñL¼õ-ÐYç-ÖqÈýÕ_ì+YÑýÛErå×à\x0014Èzè4Ù\x0014Y\x0005LZá\x0003ùQÊÍ¯Þ¿\x001d¼8=ÙÄgÍ\x000fJ\x0005Ûø¼`»âAÀQg>RWHËµ¶[ð¥Ñ/Íná3Ý\x0001øÇ\RgàZ\x001d³E¶à\x0015_læS\x000e¯Y\¿ÏÄÈþ³vy	\x001a\x001c^Ø~£Ã»Ïù¬\x0008\x0005ÇÃx\x000cMÔ\[§¡ªx\x001bÀà*ÀàZ\x0001¥¡¢\x0010yv\x000cñDvøuø\x0000Â\x0001 ü±
\x0010^¦"Ù?-pb^\x0002ô\x000bÙ\x0017³>Õ\x0006@-ÌÊ\x0000&_¾\x0012%Ûõ.^ó|\x0004!ÓU×\x0010<+JK\x0018\x0014\x0005*{¢¿:=\x0019<»Ôx²Æ=|AÐDD\x0002[|zO!\x0007ø	ý|ºæÓ=ë\x0017\x0015\x0014ÅõÓø\x000c|Îõý|¶æ³=ëö¢ú,í³¼2R*Å|#·¾Ï×|¾/¹\x0016÷w®\x001fÓ
ÛÒm¬{ù\x0014Õñ\x0018
.æy
Äç\x0002¥í¼\µhâ\x0016|¦>¾¦gý¼ÄYÑX\x0018¨¹\x001e\x0015\x000e\x0008\x0017\x0006
×Ë7tÿ\x0012\x0016\x001dë\x0007uÆA\x0011_äØ(XÍõFÏU.à«Ï¯î9¿\x0015G t	û\x0014«s-^ÝçWzýLÏúy\x001e'\x000839å\x0012\x0005ï¿t@ú¿¯«ù\;\x0002}yO|Zp©v4l-ÌíäK.ÐÏè\x001e>o8ý¯ÓU\x0003¸|\x000fÊÞ:9W\x0015½ÏÕß×u|_¥ aï\x0014\x001ad¤ð\x0017\x0006Ltóùúüúó«Ïòñ5`^2²ÔÃ\x0000ó²B;4¢NäÂC×*Û\x000bF>>,ªßJö%\x0004\x00152ºÜ`/ÚZ-¦Ò\x0007¹häóÇÅ\#F_1ú>ÆÈCÒ\x001dâsW0ø0¥Üw²á\x0011âÌ*0ô\x0011Bí;UÁñ\x001c/ÌMò-mM½\x0003?\x000b\x0010ÑÏêùÒÊ		¸\x0003TÌ¨&K\x0019MÍhú\x0018U ¶eÈÇb\x0019\x001f0\x0006Ï·ÝdÄ¾\x0014ÑV_ZÚ¾Om³â\x0001\x001d\x0018*/tíµLáoDLù]®[ýÅ~¥xøáîj]¸\x0004çÄ¡®1ÝY\\x0007Ð4åcL\x0018¥\x0002WrZ/ÎNf»ó
\x001dÒÙ6:\x001d þ\x001a\x0011\x0002wL9~7\x001a7\x000f¶²ÉM6ÂÅ °Ã\x0001Lµ¢\\x0011¸Y\x0004çfn¥tJ\x000céÍIO.Tt¡NÈ\x0005å9\¶Ô\x000eFær\x001a0L»ø\x0005o.HÏt±ú²±ñËjcKÕm¤\x000bØ\x000bÎp\x00083íý-Cõg­ßUû@¡!t\x000fÁ\x0005Á	T¯¦½¥xõP­K\x0007ú\x000cô¤å<÷Ô
Å	T\x0003-¬[àézõtëê¥[ÌÒ»\x000c(à9Z=N_éæn\x0003«ñ\\x001bI\x0017¤Ç^%³LôRr¨[ÑÙ½ký¶Qb²\x0005èÂ\x0010\x0018\x0016/òØk¶Â\x000b²Â\x001b7[´x \x0005ÊOÑ\x0001o5X<\x0015¸*]ûmlJ
\x000b+¼è\x001bñà-
Hb\x0016ß\x0003<ëø¦µa«ê\x0016ß¢ð()Dõ-4fL^½°á²]gj<Óg\x0003w:%\x0007\x0002À\x000b®äýV«gëËÖ>­Ûvø¢
x¾\x0011ÏÂ¤LºÑ¼¥¢ÉôiKñÓ\x0019¡«çëë\x001b?®\x0015»ö\x0005XÀ¼zJKÃùé6åexº>\x001aºõhXe¨¸*
jpÅî â\x0011Ìå\x0017âÕW®n½r-iK!\x001eiK\x0012V\x00038»Í¹\x001dæÓ\x0000Î´î</Q\x001cÎ-åú4çà½h«O[\x0015ÝjV¬µ%üIAÐÔÿÂùVlåjWã¹V¼Ó£\x0014Å\x001ci{òêE±ÕÓõ¹ÕÍç\x0016Æßey\x0001á°Q
è\x001cw5A1Â6t¡¦\x000btðTéÎHNSéÀÎÛøñ¦öDM«'Ó<ZÃXÆwJ7óÈ±\x0010¯öõL«¯\x0007î¨+\x0002&EægT\x000f\x0017\x0005\x001f\x000c¿¯g\½z®uõ\x0007Åx"rz/\x0005+³²\x0015]½x­Ç\x0016Äh>\x0017\x001a\x0005àñÛrùÅÀ \x001f¯ö\x0006L«7àRÜË\x000e#VêÓÚ9öÃ6¾\x0015p^\x000b\x001cùp+W\x0016/¸mâG[§|lkÎ\x0007Z$-5¤Ù\x0000s|*ÔVtº¦Ó­tÉIVdS¬ÇÙíXuH½V	o«Ô­}\x0001Ûê\x000bx\x0007&á¡õ,je}Ùx¨lÚWûð¶Õ÷kðX\x0008*)-ÝÃPå²\x0015^ýq[-òÿrak£b[
\x0008¬hN$Ç¬:\x000cä\x0012?\x0006¿ÕÞ«\x0001Ûê\x000c\x0004á	ð<4B&s\x0017VÚmî3\x001bëÕ«\x0017$J6£«\x0012J\x0016^\x0007Î
D³Í}æj«çZ­^PyJ\x0012¦á-ÆáXäÏY3«ü6'Ã©*ñãTcâ\x0007µ¥ùkÒV/i	/lc]\x001d¹Öø,\x0018®Ù"z®gv§¥W­b\x000cW»R®Õ2\ö\x0006`GÔKvDí¸±©\x0011¯¶+®Õ®\x0018¨w(­à\x0010(y¢eõ¶\x001b¾Ö;Q¿Ö/²ÉÒÐ;Fjð{$¬îÚw\x0017Bç§3>\x0016\x0007Ðk8\x00125\x0001À×wéç§«Ë?ÖB¬Äeà1NpÁz°¾°:Dà\x001a\x000f\x0000ûú,ýüttxþïÕ\x0010Xu\x0003+ÏõUB:nO\x0000
y\x0002vr^¥
X\x000fu7pò»4­p2ßÔß\x0016\x001c\x0017DèqA]?°\x0019\x0002þ-áq\x001fÐ
ûâK²Â;âµC^ÛÍë\x000cÆïÀ\x000b
ù\x0002
no\x000b3§w\x0004ìÀ®\x001fX®\x00168w*!°,[XïjGø!°ï\x0007vèv\x0018ÔF¦Vv\x001føYÑ\x001a%v\x0005\x001cÀ¡\x001b\x0018´ç"Q¡Jæ\x000er)¼ÂvWÀq\x0008\x001cû'åúôo\x000cì\x0006¬¶Ñ£×³nà\x0012ç{Ct\x0012+ÈÅS¡P\x001fÔu.K¬vtqÈú¦ë¿êRLNRÉb×\x001c\x0013\x001bkwE\]u²÷®Kk,Ñ9Ä]áùÜEåXïê®Õ]'û/»Óø¸Æß1!ÑÅk<zKê'®.;Ù{Û)t"$­qNÅzYÃõäÊïêäU×ì¿ï"Ïç\x000cÖuªTÀ[¿£\x000bZV÷ì½ð\x0014<O8¾?\x001c÷\x0014DÇUxF]­quáÉÞ\x001b\x000f&3a

»4T\x001eÒ\x0001»d\x001bË·t\x0013W7ì½ò\x0014d¥"ùÅ TDkì\x0005;\x00151îÊVTWì½óP¹\x000e\x0003÷±cýih"Ûõ>VÕ§úï<½²ÇTµÄeå¼P_\x001bpuå©Þ+OAÀ!©D\x0017\x001e¼è\x000e\ÌnÝ\x0015qu¨Þ\x000bD	µ@ê7BÑëHÀv?ºòô.\x0010UcÕkð«\x0008:
zI\x000cÉvò§väjªÊ¶©~Û\x0006\x0012×ªX
IK,}äm¼F\x0008³¸²\x0014ªßRÀ¦à\x0010ÚP\x0011CÈ=(9;ðtuðtÿÁ\x0003!OòçuQ X\x001d<íÕn<]g)ú\x000f)}BJyèÙ.!ÓÖXÊwï¯¾|zøþàÔÓU
±\x001e\x0007§¥aÖÚ--\x0006Ô3Wù
,p®µ
^]\}½½A\î³A;ï\x0008Jè
\x0003ÊõÒKUØxupôæô\x0004yaJÐD§Q¨­\x001b²ª-`E.5¥çjRí×.ð[¿mé^Êª+V½\x0005+¨
g\x001cªuJÎ%gÕ\x0017XÊj*V³Íº*ªÍ©kZW/¨Ú¼ÎRX[oØm\x0016ÖâuÕüÆc\x0014ëLY³ýu\x0015¬Ûæxål\x0015«ÕeßÝÀýa­Ýze\x0007ï\x0016aØÖ\x000eëÌ32\x0005¡tcõ\x0011=\x0012Ø­W¬Xã\x0016¬!+7"¬,\x000bëË3©×ÞY\x0008+k\x001b+Å\x0016Û (n\x000f0&VÂ\x0004¯mYCµ°2ô¯¬/3d2\ô<näÁTó²7\x000bYU½®c1²&Vçâ\x0002l²\x0005Tj|0>6~Pí UÕÊÂ\x001f»iwn%ÑæQñ¹I±ÐÎK,¥­ï\x0004µÅ¥\x0000\x0015DyÔ@TZóËµe\x0008Ø¸ ¶Ö<-hU©wÒÉÐR\x0000o5¯­×jV0g!­ÕNÐ²'\x0004-¹ÈCA\x0010A/í®ì[/¶Ø	^V)>\x0014¶¯+)^Þ>|ZK(¬+ØE
.ýï³¬³Qx³÷òôüåáüsv3\x0015iK\x000bÄÓ\x0013pmí¦7¹Ù:÷Et±¢­tÞàÙ\x0006:(YÈpk*I+àY\x00027ìÂïÚHç¥eá+(5Ê>´ãïªåLËþ2¸ä-\x000cáà-p29Åè*£oçÈ\x0005q!py/¼[\x0017j¼Ð\x0007s\x0011iØ¥`N®ôRÚ6[Í»\x000cÏÖxmV*!°Q\x0010ðlã\x0001«ç¸;ÅI;×Â°\x0008¯>\x0016¾ñ\H¥"FÄ\x0017©GßEÁ\x001bå6\x0016%
.V8ëHý\x001fÝ\x001eKpF»ÙÎÈ,ÂS5jÅ\x000bÚ\x0011/¿\x000c¹èmq\x001d\x001añ´ªðÒ\x001fð@=ú¢ Sª³AÑriÛÛXÜØúquÚyÑÕ£øVhUVOosncýqcëÇÕJ=Ë1"ÈYr¨×ÙíètM§[é@ùè\x0016Il\x0001!\x000bÑÍöI/¢³£»¶Î	|úG¼ò,-¼.^ªÞÆæÅ+ÐjótÐüi¥ÆP\x0005A\x0005_·ÎÎ¶0, c\x001fO4zyRÃ¸OâRr½¬óÛ\hR¨\x0011_ëÉ0ÐÅè/pÂ/­*á\x00051WT¹\x0008OðZIá§d7^c>\x0002ð\	èÂ~ÙB>3âkô¥I~2}Ý\x0014ÔS9\x000c
KØn÷YUãÙÆ[Ã@ûvÆSkÉq|t·ñ\x0008pÃ\x0010\x000f:´àYí¸ÁG\x0019A£m¼*öÎÏ6
,â\x001bí>Ùºû¬.3U23$\x0011¡¢ç7mÄmø\x0006]*ÈW·©,;¼Ôh\x0001ÆÏóáå@(\x0019¿¹®Kâm\x0004!ÀÑ\x0002¶Þ\x001dÖ\x0012ÇÒ¬%kØzå¶úÀnÄçZù@c7PNÃWåuiâòz¶Ùb	\x0012¾âC¬\x0016>â
òµ4l_t ¢	P\x000fÝÂëjt»©ÖÛÍÉÒo®an1­_ä©\x0005ÞluÕèvS­·¹Ð\x0012ù<vãã\x0000KZù±º}#®\x000f°Ò\x0007Ø©Ü\x0006ÆpåªÜ±ïÑduñi|k\x001bH<ë}]+<\x001f}Þ4ZZ)WÙ2÷\­ÚiÍU\x001f½Êã©×\x0013º0$ÔH\x001b¡	<\x0013%JYú\x001c\x0015\x0017¦\x001aPpÜ°ºDôP=o1b
>\x000c½PAñz¾\x001bw\x00007\x0013\x000eº~ÐfB­ØÅ´9UI(LÏÚÏ
eo@\x0002ÛWy\x00175\x0003+í¼ËEcÒäÙ©\x0011ú,r\x001cgoÃµ,ÎL
^Z=þóÈôqB7SZUQZÕG©}ñY#(éà÷¶Á±R¢¶n\x000cáfÊXSÆNJèûÈ\x0011{2×¤l\x000bcÐ\x0008Òr¨mNTNôB
z)\x0003.A²
VËuj!W\x000fO\x0008©Æ\x000b!¥Ã\x000fë])oC\x00086arrÏbH_¯¤ï[IPWÎ)ó´)y\x000eMþ
/¥í<9f4kC<k®A\x0012Å¼û8\x000fgbpD\x0012õ&ØUÎ<9ºn\x0004éaý0e*,Ó¥Q¼\x001d°¬$-"\x0010NXrZhj\x0013VrKXðÇ6®ÀM®Á$\x0007;äc!\x0003­¤=0ÚÄ¥\x0006V\x001a¾â ;¾\x000b¥ÖòÄ\x0014\x001d
OüPºæuôÓÞÌ&.½rc$
»\x0016.\x000b~\x0010nxàJaRÒ³e²µ\x000eqZÄ{#Wð\x0015Wð\Å7BbÀ¶AàÒ.Ðz¹é§¢M\¦çæm\x000f%©M\0\x0008JÓw\x0014$µ
­\x0011¹ÌdVc3­¹öWæ\x0012+\x0004*ÓO\Á\x0012W\x0016\x0019ÚÈ¥MÅ¥M+*û+yRÖKÒÓ]Ó\x001b±le\x001b± \x001c*K2\x0005È0Óà`¨c,ße&ÌPò:q
\x0004_qÜÁ	\Õ+¬KÉ {\x0013ÕÕ¶?¶qiÍªÚ{ª¶¦ì®qíãR,S-×P*e\x0019VÏÈHXE\x000cÖr7MZ­¾Mome\x001b± ¡sOËeÁ/[\x0006×$¬éwäX®²\x0011Ö5Ú\x0008\x0019yÀxÀÔ"®\x00153¹iYÍL¾fòLJ\x0012·ìDØÀ¶ÔôÙx[\x001fBÛz\x0008¶NÂ;Ñâ\x0013\x0000ÕôVî£iù¢\±æÍÛJÑ{I!Ùø\x0014ãÑ\x0018üô\x000bû&.'*.'Z¹¬b1cí,ø[§-\x001bÓi}ÍX²Æjr\x0005a¹<O 4ÂQ©®u îD.×´\x0014Ðf.]s5ÚR\x0002_²ñ\x0006¢\x0016\+¹:}L¶fj=Ö<\x000bä=H|LGªèy©ú¼yÔ\x001ab¹F/\x0010\x0012ÑÒRit ËÓ|´Z}ÔùzkùÆ­\x0005	ñ¬J¸"ÕûYÏ¹SØZ}\¡ÞZ¡qkiáHÝ(G5.	Ë\x0016'pZ¿v3V½»Ú\x001f\®\x000c¥-\x0007°^\x0018¾¤5ëò²ò²\x0015ÊPÝCÔ\x0019QYQJt¹\x000e^U¶Ô«F[ªmdñpP9§ÉÞË²á»¨tM¥[©\x000cW:§hÌ$õÚïÿ'ú¸Lµßá«åyLªÑF ¥Õ*_1NÈÚÈU{Z¾ÕÓyI¹\x0004u&?ÄñgÓ\x0005¬\x001b¹joË·z[:Ec¹ß*\x0018Snê øÑ\x001bâ½.®Ú@øV\x0003aD\x0019i\x001c?Æ[ÈH\x0010®\x0004ÙÄ\x0015ê}\x001fZ÷=¤TÁÙá
Û<´]1¸\x001aË5bÁÓS~úL\ÙBDÇ\x000fÛb¦Îr\x0003\x0014õÞÂ?·QÒg6\x0012É'BÕ\x0019¨ÚVÜÌ\x0007c\x001bºÀ¢®Áb£Æ½ü\x000e\x0006\x000f
ÔTâD Nj\x0003Ï$=`²ÎÙHÙ´q*O^\x00050Ð9v¹X[òÛÓ5\x0014ó`Âgâz&ÎÞ
am÷(ÐA³@\x000c¾hN÷7g«­y}5ãNG;\x001d\x001b	A%\x0006CQ\x0015Ü(dÍvðbBS­áÔ\x0000½M=!®¨õ[ÍjýM-Ä'\x0000g+Ph¼\x001b\x0012\x0006×L(#¾gb_)3Ð\x0015/a)ðXºÃ\x001a\x001e
ÖFèbÎaqj\x0019þf"O¶\x000c[!\x000e»ÁÌh\x001cÈBÄäF:Uªðè=Ýú«"ÆõS&7"\x001aqj\x0014ë¦J\x0019É]Ö\x001aò*e¸PfÚ§\\x000c¨CõuhÿÌP;Q²¨¨\x000b®%\x000bÚwïD=5C\x0015z¹¯ë*Ãïw\x0017\x000f\x001f×¿cÆ¹~t\x0005õ^ØÀ!ÌX<dP\x0003pøóÙÁù\x000f\x001bùTÅ§Zù \x001aÏG\x0010YÄßÆÈW\ú0³írË\x0008½\x001c\x0012BÀÜFîgó®¼©\x0007~Ï±oê
¡\x0002\x000cÍV\x0012ÓÃKE$¿j\x0015\x0011úÙnÎeÃÉHr?úfÂt\x0015K
ïµÆ:
l3p¾âh\x0011¡Õ1²ù )\x0001¡}¤ÄwT%-bäl­Ì2ÀúÈöâ ½Å\x0011#Y6'¢àH6ºíöáðÒ\x0003DÛ¼6yô­áU/G\x001dGÕ@Z|¶(j\x0019¢w\x0015¢wÍä%ð\x0011\x001c}ÉI¹ñdV¾aéeâÃÊËÖ¯,J^@*1\x0007¿¼ÒÎ÷¼/C¬/\x0014Õ~£ÀØ\x0015êÔ.ÒhGØrU~»Ã<lo\x0006DÛ¾*|Dv9ËéxèOúÎÛÙÃjZÌÓº\x001a\x0001A×0ÐÔ$'µ(ïv»Ã<\x001c3~C;"\x0018D_,b¤faoù3«¨'\x0010/î>\~\x0003´5`ûG\x0006-P¿:*ºU)´¬\x001blXÃú4ëÓ¬a-¨v&!\x0018ÅªþÌªã3\x0007
¥\x0002æþ¸íº¼5é¸Ñf¯ûÌª^CÕ¾Þqý\x0011dþ\x0002mCÅÛ0êí¬Ö5¡n'L'%ð³\x0018kA9Ðg\x000f1nhê¯l¿²\x001fÞÌZ6R¦\x001cf·]ÍiyN[#bºù\yÕÈ	%Å-â:'\x00046\x0003Ö6[·ÛlÊd\x0010Ä\x0016"\CËöFnéÚfv
\x0014Li\x0019°\x0003\x00115×Äù-c\x0015[[mÛnµ½fÁô-iN;eDy'2["êÊG´ºÙGô0ÒË\x000f«j]òjørf»ólëÃb;\x000e\x0017ÅÁIç9W£;Åa¸·sq¬¯\x0011};"6dc¨\x0001Úi©Ô\x0010Óe7\x0010!,÷\x001füU£ý<Í-Jªô\x0003å\x0011¾¥µÝh{Ö]Ú>âLL;§\x000fYé\x0013³\x000cÇ\x0006Z(þèã}mé09á|wp¦\x0010_\x0013\x001eiorc\x000bM\x0017c0Ê0ÈQåüÃÞë»ß\x001f.ï×åí´(Ê$ÜÞ9,¸ÞÀ8­×÷ï½>8ûëùáÛÇ¯\x0018\x00191º!bt}' \x0002HnÂææìl\x0013á0_\x0008\x0007ù&D#XÿPYýÆÈ=PÓ\x0019¥±F\x001f:r¯´-
ÐDÌG{#¢\x001c
ðÁ¹õÄÝÃÞÛ_o?_lÈ\x001dÇ2ñZ
úÀ:°l`úÂÓÇä|ïí_N_\x001dÌ7gfõ jc³¤\x0010ó¤
\x0015sxÍÇÃh7\x001d·,eÓC6Ý¸nºÈÁA­½ãûjXóôí¼Í\x000cÙLëºYRZ
1ÑmZ7(Âvpv\x0008g\x001b\x0017NYÎÂFWfªÂ\x001b\x0000U1},ÕÊÉÖ¥|Cöºä»¦«é´Ñ\x001bÎÃÜ££\x001cÍnÈx­gò8\x001aX<(bÔÔëè¸j\x001f¦3Ä\x000b\x0017oP¸
_V´ÒiDÂÅ\x0013è`#\x001dOUMz:_Hçªµs­k\x0017
x\x000bQ9jñÆ³\Ê£ñYt¾¢ót^\x001a®yO>)bA=\x001d¯]Ñ]F§dõelü´Þ®çLA=ÉôÜ6Véjín]¼èÙË\x0007:Ò2pÂò±z«Åsõâ¹ÖÅSOmUÀ\x0014f<56Üçk<ßGE(*Í\x001fÖ1ðtzåg¤7á¥àÝp
K_{PÏ/\x001e>_^oºÎraTÔÎ\x001b£(¥ÉÜ`ö\x001f¿:<~ìÜe²A\x0004\x000cám&s4A¢"çbÒe!ÆdÊm	­Èl;)Ëuòðòs±O~h`´Ií%h¾B\x001b÷\x000c/Aì¯kYh,üàÝäCñ\x0012´P¡\x0000\x0016 IG\x00075¡i®Q¾hÊx9ï¨Ï¡\x0005[;é@¹ªÿÿü¯Ó»\x000fWwëJ<\x000cª·å²f¨ÉG45Ï­+nºÖhïôìÅÑáÙ°\x0016jÌ¥\ºË°7§%Ud£\x0015?!\x0005g'+ù7UúÝ6ëw7¢A\x0008%Ð %¹OÓ½\x000f+²é/)e
&ÛÁ¤f\x0011
\x0013=2W(Ip£û¸TÍ¥Ú¹àp\x000bzMs9%\x0004\x000båaZMbm"\x001b¿MdÃñ·\x000bÉ \x0017êò§´é~W¹~>]|\\x001a+';6\x001a,´%wDMî%µºÁ$k.u\x0005v\x001bÉlõ1mþ(jß	à\x001a\x0019!Réd±&ídJ¡¦\x0005±L°U+;èû±¶\x0018±Ýb@!×Ñ\x0005xïËÅ-VE¾4êû±þ±õkÚä©x~\x0006wÎÒK½ÅîïL&Íd5ì\x00062)ê\x0013nEó\x001açð\x0001\x001a]Ø9Ï½SÜ5Y¶¾\x0011MÐd3\x0004)F\x000b\f\ô\x0005­ç{Êa}8¢©v´\x0014FÚj'`X"SBó]@ªÑµ©ZO\x0015ÐÐO\x000fÉ\x0010\x0012R¦8\x001c0ÓÊÐôh¯éö½\x0006ýJÔã\x001cK\x0001[~\x001232N«Ùn&³#²æE3ÂzwÒzE­.7Ôt9ýF²Ñ!ÐíÀ@×Q¤±kã EM·Rm$\x001b\x0001Ý~\x0006 °´oD¾ÕC4åÒ}\x001bmä	éVW\x0008\x0016MqC\x0015¦p£U|\x0006Æ\x0003 \x0016ºµRÇÑ²Åöe\x0003\x0011l^6Ge¬6y«S°!\x0016^63:\x0005¦ã\x0014@\x001e\x000cnpìtDË¯	j\°tÙÌÈé6­^7°åæY4kmG´¬¯¯Lß\x0015jF»Í´ï¶\x0014xò\x0015
¯Ô\x000e
UÊfC]3z¦ÛÑ´cëáS<\x0003O'¤d»æe×\x00195¶>\x0007Æ6d÷¹Ã9ÁÕÂÛ}¦It\x0013\x001dÝS¶ýré6 .d°lY&] ¤¾Ð|ó-ãhÕbóªI\x0018½g\x0011¤ë@\x0008cÉ\x0017¡K;\x0012µñÀ?·iV
\x000c¾\x000cXrð\x0004I[m<\x0014w)\x0019¡f4¹r,U¨ÞS\x000fþãüòR4;Bk\x000c$\x000cã ü -½õ¹ x0G
«zÜoUMÑ\x00034×\x0006"ôf\x0005\x0005Ç.À¨ù¦»20	%Ðb3/ïÁ[.Q\x000bÊv]©\x000e5L"ïø z\x0003Bô¨ÓÇ²Õì´*ýF²0"\x000b\x001d§ ¨ä[:\x0004Ü2ªg\x00047Å\x0011YkJ!­ÔîXÓ\x000ehÆÇé9\x0012Ðd}\x0015à\x001bÑT²j.P\x001bh\x001a®\x000b¦µ];MÊ\x0011Zsd Aw
ÞY.ß\x0015¶ÕÌ¼¦hjÖ\x001c\x001aHP$ÏÕ\x0015\x0001æîeÁ\x000c\x0007Ï,6!¼\x0010m\x0014\x001e«öð\x0018"jô\x0002¨[e·#\x001d\x0008ºÛõ¸þm)Úè.Píw\x0011/¦5\x001dÐ´ho©Øu@&HæÛ¿gÐ<ó-À´¡\\x0000\x0015dy\x0000í
Ü_\¯m7j°óI<}ØÜ¾á­çáBÆö\x001957²\x001c®Ýrødn)<)Rv<\x001eSr\x0011ÏtcôF2;"k÷!}T|±ÃÌl\x0012\x000fpÂð¢©®ä
£Ó\x0019ÚO'<`Óàæt\x0018rJÁ»2\x0012Ç¸ié¹
dZÔñ§\x0016Íñ§\x0002ýfGÓàu%/\x001a¨¢S\x0011 ÷Ø6z÷ÑÍ\x000f?\x0016î\x000eí\x00063¬²£\x0006*Ó\å©¦Þ6íZÕW;þ¹
ÆâÑhP\x0015yjx¥\x0008Ð\x000bÙsµëQÎO·çü\x0014å¡\x0012@\x00104Ëra)> ÷2ãå´ØèF´ÑfÓíMÁ#*	h:*ÇÀ«æ7FK9V%Å\x001aÔ¥«rü\x0017\x0017÷·é?².\x0007\x0003Á0eI¥ %\x0019\x001b\x0015#SzRt\x001d²_\x001c¼==9\x0003Ór\x0008¦e+	\\x001bæ}FÙÛ´xì	Í·w­çrzÈåt\x0007\x0017=ÉúäØ*J 8Cê]'÷C.ï[¹´§âzï#Íª\x00041\x0002ö·íªXÏ5Hj;\x001e1¾Ë:Y²\x0014=©ì\x0001AQ'uc­¼Ç\-\x0019ÉA\x0012Ac¾ªuÅG\x001bÈÙ\x000e,¸3HÃk)g0×.r\x0015r­d*zö3<h\x0013Ó£J
ßùcÎw\x0001¯%Ó®úÚµ}Íô7ÉUä°n%\x0003\x0007ùdûvÕéØºd\x0012Â_\x0002S\x0006S}\x0000Æí4¼\x0013ô
{ï@íX´®´®D\x0000Ég$ùþ\x0015×}Ìè\x001aL7éò2\x0010r\x0003¸¤áÝïãl\x001b÷z°9YÓ
Fz­h1\x000c¿ùÀÏ×:Î£o$«Ï¥i>\x0002úÕ¸j4°\x001a©1«ÝßIfUõ1­jý\x0002$ß}ÉQå:o[ÂÌÎOiuµ`V7/\x0018\x0014:ò©T$dµ+`v¾½x=YmÈl³!\x0013'ccæ,ÒYöýu\x0008³íí\x001bÈê5kßd4Z\x0012×,\x0014Á|Á9½Éö®\x0005÷å°sSÛGoòäî\x000cmÚý4'E\x0010|ÛNS6Ì\x0019\x0000Yh'3L¬V\x0019ùQ\x001c´ìüõ­d\x001bo¥\x0004fcIÅHMÍV\x0005~ÛÑz^i-«O¦k<Pò%Vï:ê½üëåjÌ5ºdP"\x0017©\x000e3p©â°²ÛV\x000cÓ+@e[]Ø\x0008#âªÓ«4NGÑÕ\x001bß5oüd!×SZT
ãí5×ò¶\x0011¬vú]»×\x001f5Go\x0001&Áç\x0015\x0013¥)*ÊÎ}_H×|"ÿ7Â\x0011;ê\x000fLÿßþ`6.(\x0006^]_ß®­s÷BbÐf Ò\x0003Þ	òy {^/ðèøøôxkàZØÇÊ©ÿB°	³\x0005Sÿu`Ã:÷\x00046¬s_Fæ¤¥Bßè#¥.¼aó
Z´ó:©ìÑæÏ`¾\x0006óÍ`U¡¥ô*òc«¤Lxn$S¡ÞdcÁÌÍ\x001f3
²\x0017éj<4Å\x0010\x0012}k¦íhµ®YH¢Éy;è\x0002Ì>¿wÞ0Y\£z»,Ôd¡\x000crÄDæ-÷°9O#À3ë\x0003\x001b¨\x0014\x0000Xt­`FñÛ\x0008¾u~Áñ²Ìq}`VW»Ìêæ]\x0016É\x0008yv£\x000bU]F+fät\x0012v3«É\3\x0019\x0015¹Ö;­x¦¤~ÞådµÅl6\x0018 [`R	,ÜF%`Éëå¦G\x000fn\x0004óµ%óÍ,ù8ÏÐöé!ÛÖÆº¹AÊ¸B¬¾c­ßÑ\x00055\x0000¦=xN¡HöÈ¬uÓu\x001bÉufé\x001fãXyzó\x000eK+\x0016xÉ\x0002©3z\x001bH1­éÛd±Þû±}ï{e @æ"kJ86°6NOÙ\x0004&G\x000e\x0006þ¹ñk:	\x001e"-\x0019mPÓâ%³]LúºÄ?·Þä-Ö®ô/+¶dÎN\x000f¹Ü&k\x001bnD3\x0016\x0007ë\x0019ÔV£¢ÁädH"\x000bÓ%,\x001bÉ\x0006ýòH¦d+MddgµçaB^;ËG N7lFS#´f/Û
]k0¯$]ë!NölFKÿØe7\x0012\x001d¡µZÌxVhÐÊf­[#c¾\x0016ËVÌ·®Xr
Ñû1è°Ðô?¯<
ð±¾Ë+K\x0017G
¦
-ô0X°èoÃxu(Í`Rõ\x001dÍ++Û}Y\x0005ï\x0002ÐàÝ&¿\x001bUîfºu6¡©aÓ\x001a\x0006¢uÕ³(\g`àT\x0011¢ô\x000cK\x0016¸\x0011í"a½\x001b¶y\x001f@(î¸ãÛû«¯_s\x0003úë»½Ë¯÷ßÖåd¡õ\x000bÛtÀC\x0013\x0011ÍÀÜ:Í®ö¸åøôíÑ7¹\x000býõÙÁÞÉá·?\x001dNê\x0015P5\x0004U} Pdf2¨
¬`C\x0019üíGÏùs Óú\x0011\x0005U\x000fQu\x0017jÚnÜF¯×¬&aP-²5F.[Ó
¨fjúV\x0015\x0006Ó\x000eó¹¨î+H¨bä w¢Ú!ªí[Õä\x0018ø|Ä¥\x000ct@Ø¤¸ìÊì\x0002Õ
Q]ç¡ÒÏ(\x0018Ó¡Láçw«CØÉ÷÷CRß·¨Áce\x000c.ªÆî\÷G·³\x0019zèD
CÔÐJpiUÙ14\x001c²éq]g'j\x001c¢Æ¾ï/PØ\x0017Ï¤Zg\x000f½À|þÍ.H×Í¿èÜ\x0000¹<Ðà\x0014%N\x001c@ï>­ê8	ÔÉZ_U½wUÖ}\x0005Ö\x00109\x0000\x0003YK6Aïµº­dßuå@<Èu,±µãe­®\x0000Ùw\x00078HK®P
5%Ù\x0016w²¨Y}vÕù\Y.j
ñbâ$ÛÅ
 +c%û¬\x0015¸zlS<j*E;/ÖÑx×6V\x0018ã\x00081íJ0ýÅ>þyøjôêêÃ¯´k\x0008ØgàíU²p4\x0008ÆF??ÂäÕQúk-¾øxñõþn\x000esP9£Ò%RY#mä]jmà¨(ù:¨\x0015æÌbÆül³rõ£¨\x0006O=ì½¾¼ûð}
ú1Kº«iEsp4¨\x001dvjN´îõáÙ7 Å
-6¢\x0019EmQêH_8\x0000\F³3\x0017ÐoJÞÞÅ#v|ñªq\x0013wúÀs:KØTµlR5®rüt\x0003Iâ\\x0012\x0018dé0O\x0017ù´éf¸ª^\x001d¶+\x0007}hDÎ-ÓÁQZ:»þ³ÎªÑiu«ðöÞ^Ü¤\x0000øàææb-¡\x000fEf2Ý1y8RPÒ'i5ó$½÷öà$ÅÀ\x0007''\x0007\x001b0¡Ì|	|z Ø	ËYÕ(-å\x0016uäôÈ\x0019Tr|s®æfÈ9³)	3Ô_=t|v\x0019~Pâ¤AðAÊRfæª©`
[ùhhd=ZìÍÅ§
ý1Zòí\x000cÜ¬Sâ#Ï/±3Rãx¼9xyr8{\x0010ßêå\x0000øF5|\x001bù ×\x001e\x000bE)	N)Àà5]vÎÌ*/ä\x001b\x0018m\¿ÑP\x0005ÙýÂ÷\x0003M¦\x001e¤nOÌ.â³Õú\x0007³mæ\x000bÑp\«é¦|`\x0010üðèô¼S³\x0004p("\x0000n]@Ð,¶ü4T2ö\x001eÊ~òÛÐ*ÍE®\x0006tÍà48\x00024ô\x0010éuy»
~¶òv\x0011_¬ùb3D{À3Ç\x0019xA\x0002\x000eÖz;[¹¶\x000föÇ\x000f·Kãúe¹\x001c\x0004dí´üeÝ|Ñß"ÀP\x001dÚR/Ûy+\x0002:ªåñ,?\x0016PlõM¨>°	\x001fX	ç\x0013¾ZzNøÆ\x0018ØÆ¨M&pöF¶c
m+\x001eiË\x0002$\x0005¿D¢µ\x000f\y`\x000e¤Ð&	3¯bä\x0014k$\x0016æ\x001fâÿdü\x0004A\x0007\x000f\x0012_GÆc!êd\x0014s®WÉ\½\x000bo$k¤Qé]\x0002\x001aë\x0015½K\x0002fÅ/úÂÕ¶ê5[­¨\x001c\x0014âºG6.©La¾Ì=ÀÉõÆü4*¢ð«D
oÖÌ,Y*"\x000eV\x0019\x0014º¤­5\x001aÈwvõþêÏÿÞÔAÜ[A©\x0008Y\x001eûaÎ0?ñÌ;\x0013gGÏë\x001eÍG¡Lô\x0015¤ïtyæ\x0006fw%'¡*)s1\x001bÝ/dÕBÆL\x001fÛ{*KÌÈoìZÏ(/FºþÖºÑÅÈ×1yf\x0013úÔ]jµ÷Ì\x0016RºÒõPø)ÕÑ\x0005\x001eí­à·¼5m=\x000b!}
é{ A¾¶d%xãÙÃ´Ñêý\x0016þ\x0002Þo___|Àwåë½\x001fooî/®Ö6Ô@\x000fÁ*Òü$¢\QÉ\x0019Ï\x0003}}|ð\x0002\x000fö~<=y{p4,ûæ\x0018cª!¦z²z©,¦\x0019b'iöÉbº!¦{zÖUïð\x0017ðþ¹Êóýpwña\x001eÐD\x0010E$ùä°ç´²ñNsON:måûáìàÅ¬\x0005Ê\Ã\x0012*·¯l\x001bXÀ\x000eV?ÑTv	\x0003\x0015$gGg&Ü/"ÓÕé¶%K¾Dî²Ë%\x000bè\x0019\x001fá%Íwo\x0006S\x0003£
K&d\x000b\x0019\x000còÊ\x0019¼(Ç\x0011	m¥e`íÌéMhèá\x000c+ÏÂþxÜëû»»µO,é,°<\x0011d¾éÂS%ô\x000f©\x000f\x001d­y`É¡\x0002\x000cí»!\x0013¡â¹EÊyµY3Òw\x0011`¬\x0000c; Ð\x0018\x0003\x0000 ô$åëea7÷±p(\x0012\x0008åx`îfD\x0013ËcvtZC]F\x0018Úù¸z=â{!UåÖ<4-Ï_öþúpqwuy·î|`ú&¨*Gpi[Ú2öQ&þàÕë½¿\x001f½M\x001e×8*DjH¤¼¤g½ "7VØ2¥\x0005©ÇÉ""=$ÒMDÎqg¤Jp:o9s¨Sã=¶È\x000cL\x001b&o>À\x001clpÓÿºa"£ÆVm\x0011\x001d\x0012Ù&¢d\(ÝY2CÉÀ@ºoÜ\x0010Èµ\x0001eÍC\x0000rÛY \x00011Á>\x001a´È\x000f|\x001b@o\x0007 \x0005x²n\x0018S.\x0004
C Ð\x0004$\x001c{b pE¢52Z&Þ3\x0017\x0011Å!Ql!JG\x001bû\p\x0014\x000b$WÏ¾4\x0013t	Q©ÛÊöQ4!\x0019ËÊÒ:Ä%0	éõ^Tì&\x001d\x001478&¤"Q \x0002
\x0000MH¢ç»ÉÊfË&£íã¹õø¸\x000c\x0003¹GéÃ\x0005@*T§\x001fþØ²¹µå\x0011\x001c$×\x00157éÇO)\x0015Ï¸Ò¬ºCBÛñß!\x0010xøè¹
Æó9|1yH±ØÃ\x001aä9iÉ3äDr\x0002¨\x0010Y\x0015ÕN+fÔÚÎS\x0014v~6ë5ù\£RÁ\x001f[Ð¬BÁw@d)aºç8gvç\x0002²Az\x0017Èê\x0019­\x001bÉ`¼­¦\x0002Uðêy:\x001d\x000bæ7¡i_¡iß\x00065PÌ~Ô"ymãl\x0008¶\x0004,Ö`±m£9º÷\x0012Yäñ*ò¬*;?ût\x0001Ú \x0004\x0003´z:æF´äS	´Y.\x0019»¸X\x001fÖFß¿Ó®ÐnCóÌE·#ÅSY»\x0007:lúÑlfÛÐB.±Çç)ð7¼j<ð<Ì\x0008_,BsÕùT®í|È\x0017i¦\x0007c\x0016Qz\x0017úÎ§¬+ÕÑ¥(_°ö®ÿç?ÿëàêÓ\x0003t(Ý¬»\x000bTú¸¢.§ÈÀ,>IQkFÆ\x001fî\x001dï\x001d\x001c½<V¥Ç¯Xu\x0010ù'Öðè¹m9,·ÏÞYVÄjX\x0018\x0006ÄÊ·c\x001döâKêÅï5Ú>c<IU(Æ©¢b3n\x0000n­\x0017Ön³²é&+'ÀÝ%ZË\x0015¬FO¾Á5ÐºziÝ6KþÅÄ¢ôX)\x0000Y>É\x0002TÆ=r;[iMMk¶¡\x0005Y1ÊI¦\x000b(çý¼f\x001dwãÝwÓ\x0004kkØGoï-K«Yt\x000cÄÀ
ÑòÂGQO\x0003«\x001d%±¤\x001d&±V¯ï\x0007\x000fï/ïî×ÏÃÔË6½´<J*Ö÷uk9ßì\x001d??<{;ñð!\x0007ªµ\x0000¹­m\x00143Z>DM\x0000gU2õ¤ÚïbÊP/åãó¿\x0012´£x\x001cN\x001e²âQ\x0014Ã%ÊÉ¡áK)CJøc\x0017e:ç\x0007©ð,Ô`ÐÆ\x001c\x000fCh\x000c5dè\x0004]$EJo0M"P8Ì¢ðcî6H=\x0010Å =íúV\x0012faæÝP Ä\x0015Ï~M©\x0007u\x000c\x0000©'ê\x0016AÊ2Æa\x0012f_\x0014¯¤Pë«6@ú\x001arªXi!$ËÁûL´FMö},¥\x001cÎÉè\ôRjZÊ\x0014Y¬ Ysß­·\x0015¤"ûsXÞîyî¬<XÇÉÈl1¥®Lå_·ì|OïË<
\x001aí\x0007\x0013ÿ2Ú®\x0003~lyõzr\x0000h£FÉëÄxz}õíêòn}¥R°¨ \x0007)\x000b¯¹\x0003Õq´\x0006Å\x0015ã°ùì81\x001e\x001fýttx6\x000f©ª\x00132HæÜsG?oèùßR\x000f)u'¥cYÅ\x001c\x0015~Ò³Ï5£i«ÍfHiz)\x0015\x0006å	r4Õ1QZþâÎÏ÷.¢´CJÛûÅ-ylQð\x00005\x001bG6é6¹HÛQº!¥ë¤Á¢ÔW¥h¾WZ_`½Ür[ú!¤ïÄÉFÔý"bÊ\x0015¹2ÝÂZ1/Ü°r,."\x001f<¿¼¾¾üö°¶²&ÝÏÍä^RFWòÄÝtÎ×tk??<>>üé|¾UWEä#aE±è\x001f\x0018ðÖ,«\x0013\x0011¤\x000fa{H=ÔíPaNz" \x000e$A7Ê%áezkH34\x001dÉ$\x0014*®$¨â´óg{)¤\x001dBÚ\x000eH\x0013Pé	VRsÍ×\\x0001Üâù{q)£\x001b2º\x000eÆdÊIÊÈJñt©x&£
rÜÀø^8Ô\x0002´«õD\x0001Ü?¾Ø{~0÷^_o(\x00130ÃFB+I¾\x0005t\x0003$Ý¨îëø`ïùA"Ü{}¼¶XébM\x0017\x0006\x001dTgÃ÷\x001dt¦pú*UýÓÕåÃ\x001fkM¶Ò8'\x0000å+$k­xÁ:f<(²ÁÉLÿûãN<*ÆU8Ò5ðxÐ}È\x0006\x001adI¦ÆIÇr
!Læô×óØÇ6ðè<\x0017	\x001bil)]/\x001a¾é?Ó²>*Ïj\x001aô³ÚÉ.æ¿¥Ï¼öD iÖCá
Ôáã\x0015ç\x001dìÜ`$êgýù§ÓY%\x000cZõ1Ûé>æ¤J¬¢Qxà¥\x0007Á(}Ñsé	_þ/×kþb<å×Ûë£óà²Uühãù[+IßÚ¸8ßLñâ/§çÇëëës8µÔBUC\x0017hP\x001cIi½*9Ô\ëÇÃ{@e¾3Vòw\x0000i«Öð7ðé×¦í£ä©é1Ù¾¬î`¼ FCcõòÄáÞ\x001bøæëÙ\ÔC6øc\x000b§¥\x001cãi¯©?Êà\x0014e\x000bc¯`!p\x001a¾ê°ü[ï[Q7iþxqóé2]\x001b·7k»ÍÒ©Æ'x.Ð6»Íga© ægRýxpòò0]\x001f§'³U)j¬ë ßþK/Õ¼1\x001eçRacTä¡¡Æ³Ö£·¹J;¦¨²Ð?å\x000bxÃÊ1«{dN¯!éLÐã«Ö\\x000e\x001aât:¬]ºÓc@²t þ\x0001]\x0005è\x001a`5\x0018ù±y\x0002Ã·õD¨ìS!tïâ×ðåûý»\5¢pÉCØûá
à½¿>\~¿»\x0000,nëö_\^]__|\x0000(\x0018£"ð5Å\x0008\x0003
à8\x0016Ð{x\x0001Dª\x0014\x001eá¹8<:>>x±ÌðùÞ\x000fG\x0010úîýõüðç³73Þ\x000bÔPT«	,-$.©#àb5j¯Eî\x001bÛ
\x000c|XÛ¼bÿû`\x0011\x0016\x001d\x0018P\x001a\x001a\x0016Üçß§\x00063Ð÷óï\x0013CK\x000eXº
òïSCóP)\x0018!ûù÷ ]]é;3ï>&{»ÿ\x0011Âý\x0017×\x0017_°EwÉäbÌÄîá\\\x0003\x0012=rx)³Ê.3\x001dì½8>x
îø\x0012\x0016\x0003,æi°(`QOE¾û\x0004ßèÓ¿Å¿ûðËµúð7ÊPO½½¸½¾ýüþ*«p©OXwß¨ç\x001bÈ4ø\x000f6ÊºH²)\x0000M¡	 \x0005ö6F&g?å\x0010n@qz|úêùQ%42Ï
vt\x000bÖµ¯\x0013k¹2+±ê¬¡\x001f\x001cLvß!k
ñ&\x001eË²N#±Â«%ÖÀ¬$Ó»#V0g[°¬~Mëª5g!`]³2ÆX<ñp¶U\x000b´»¸®T X){`[ Ýª\x0013¯gQ
¢\x0000ª\x0013ø*¨!\x0010ªßé²¦í4ñ¶ÕÆü"\x0000¬$+X¡0¶k\x000eþwÄJN'«WYµ\x000e¶\x0000¶ê\x0002j\x000c\x001aÅ.5Y¿Ø\x001a²IÅeØº*ÐâàåvÇ
a÷Xÿº\x00056]R´\x0005¬ÍºHUEÇÛUí\x0010\x0015.­þ[+,}\x000b¬PÃ-\x0016wî$V\x001bvh]KüÛ\x000fËv@æ)0yaÙdéü¾
ì{{uùûÐ\x001dÀÔîÅõµlÉ5\x001eä¤ùÍ`îsR\x0003Ú1ÕhbB÷àøõ<ËÿüùúzÀrvùËÃ§Ë½/·×þ\x0013ng@\x001c\x0000k0\x0012Þ¹\\x001cáµ
Y9(M¯¼èìðÇó{'\x0007¯O\x000fOOf±.nß?¾\x000foK\x0018\òçÿwyñ°þ\@êÑdsU¨\x0007YTÃ.Òè\x0018g¼=<8I=\x000eaÊæZH\x0013eÖ\x0007ÆÝÄ_L)SÌ\x001få¹[h.ßp÷5\x0005ºX,a\x0003ýx{óqÍþðb¦\x000cfÂQÇ¨¤÷,H¯³<P0^0ª
ôãéI%]Ó|ü{:yYÀ@ö|ÿàÛeúÐj\
Öþq{q÷qí*ypk\x0003®\x0012TÛ î¸ÔèÒ7\x000b¾^¥\x000eOÎ\x000f¡å$¶\x0014´ýÇéÁÙ\x000f²uþÝ{\x0011¢EþÝs¨iôý.Ùxrýv±¦H\x0016\x001c=¦Ý$ÙÌF'Íãïwøã\x001eD<^¦^°Â¤Lª)ðrtþ¤( \x0018zd\x0006\x0016Cé!nJ;Ý\x0012¡ÌfòJd&ÝÍdL¦)¢/Pô²\x0008>
\x000cet/\x001dBÙ\x0016¨ä\x0013ã\x000c%	Ê:UVª{K¹!kryJ\x0016@¹¬&
VS-ÕÍäL¾ÉäzP`²
e{É\x001b
t@É°\x0017*\x000e¡b\x000bTr¶Éæg7ð¼óÓ 0éÛe\x0011¬¶¹lÚç¾8Xàn\x0007r\x0006/_oì¸.¦Rµj2SÑa³\x0013PE³ºûØí¤BÒCU)Õb§"ô¶Ð\x0017esÊ]åL7Uõ\x0005UË\x0017P\x0019©Ëù3ý\x0004]î	?a\x0019Ue©T©\x001e\x000bGÈ¨ÇÈ_°¬è5\x000bª2UªÉVE(týY\x000e',¯½VDøú\x0013-_\x0010\x001a»*mül\x0018RÔ`Êfï5\x000cºr^t÷\x0002µ\x0015ùªÊ¼P:÷ÄÂEìýzº²
ºÅ*Ä\x0014YË|'G\x0015ÙyÑ6×º\x0001éÝéºv^¬B2æVJù<ð3QÔÍvTUÐMV\x0001f\x0006\x0012Îe<iO\x0005] º®n3
sÐÐ\x0013<\x001d?Ê?z\x00145ì¤ªn2
.fap Ê/ÿx\x0005OìE·¥Ò\x0003£Û<\x0018õÌÑ\x0007\x0014&+Æ¢\x0007ÃNq\x000cÝ\x001f0TT¡Ê\x0007R-\x001b0äÀ^È.÷½LW¥[Ü*(ëäëOå\x0012çdC	³L/©Lºi1é>EËÂ\x0007Ãñ\x0000J±nM¯E7E7-\x0016\x001dr\x001a\x0002R-1S\x0005¡rÐ|ùénWÏTFÝ´\x0018u\x0007å\x0014ÓÞ´ËTÚ²£ uïF7Q7-F\x001d´Eþ~ÐÆ¬|¦R&Bõºz¦I[ºKF]\x0003*\x001dj§$ª\x0010=»Å*ôº/¦²ê¦Åª[\x0018©HÎºÖY6,Q\x0019ÁVQ{¨*«nZ¬ºK\x000bÄ»\x001d0d¦
fu\x0006U/UeÖMYw:K7]*Ê²¯ìø©h9UeÖMY\x0007yrO!<t¢R\x0012ÍXò
Ýûª2ì¦É°§/È6\x0014:lr\x0010(¤æ/è{
­\x000c»m2ìé\x0003ZòA!Ý\x0005±ÚìPSU¦Ý¶vïÊ9P»'(Þï5í¶2í¶É´Ç\x001b.r\#97[bÀØ\x001dÅÛÊ´Û&ÓnU«¨\x0002éÂ£JnÁöú{¶2W¶É\yGÃ.±G\x000f¨\x001cù{\x001eÆVöRUæÊ¶+/³\x0014\x001cR\x0005öB\x0005«Dõ(é¿ª2W¶É\x000bU6ÏØTe)\x001cð®²($P^Ón+se[ýPÇTÔÞ¨hZ/P¹Þµr½rMö
Æ½Ò«¿È³0·£ªìkz\x001aI_C.\x001d9fÖpÈ¥»w»«ìkÊ:ºÈî\x0015¦d,?âÛ²V½¡«ìkË:Æõ°!w>'*x=ÊT¦×\¹Ê\x0013uMé\x0005cs\x000fI\x0002}fJÅpÚ8A«SUæÊ5+\x0002nöc"\x0014d*£øûÙî$WY+×`­\x0008\x001e.ý{òp§\x0004\x0015"'=|ìµV®²V®ÁZ\x0019á¹¼Ê	*Êq~(N=u/ò±ò
Æ
¿_~cvB,\x001e\x0005ßÏó\x0007\x000cÝI\x000f_\x0019+ß	M\x001f0N¤\x000fhòËwÚëüÀåE÷mã+[år¡ºøV\x0011rÆ\x0004%$gh}·­ò­ò­¶*øBÅ	>gøföý\x001f°2V¾ù+\x0010UàYIÃ=È^?ÔWa³oJªÛ£\x0013UÀÉKølªøböÝ\x000fÌ¾rC}S.\x0014j\x0016"YP5 >Àñ^wª{³W&Ô79|íù\x0004® m¡êª,¨oò÷Àà\x0001ïåÈ%Âd
¸mºwU¨Uh\x0004É­\x0002¡lÔ\x000fe£w6¡2
¡­¼#R\x001c®\x001aÀ³§hOI1;©ªã\x0017_²ê/@KÇOé°ê­\x0010\x0008\x0003\x0013Zâ-¤\x0006Æå\x0004zJb\x0007Föûz±ºjb[ÍP\x001e	¹PuôÐ&hî\x001cð¢Ù¨k'ëâ*¨öI\x000bþöòîîrïìöáÓå:&)] çe§Éd=s)§!o\¨WêíáÙÙáÞÙéùËA«EY#9.Ì¹0\x0007\x0014Do>\]ÞàtÌõPiïÒb\x0001îgäúÁR^?¶\x0008{\x0007'/\x000eOp*æÁË¹\x0006æ\x0001a\x001c\x0012ÆvÂ`ø&tÁqc¥Àq\x001cvµ\x0001ªaôþ¥øçfÆ\x0014äx*ÂôÔz¥dàz¾qáÎ2BóîÒÞý~yó.ý\x0001äWóïsPDøtÛrfÿ§ëéï/éÏï\x001e®¾îG(\x0008Øè\x0001É6®Æ}(ö.§Ø\x0016
ÆO\x0007Ç?\x001f\x001fî?\x0007-§3µ!¤%ópò_<\x0007o"½Ácðüö;\x000e5f\x000baÿÕíÍýçÛ»«}x:,\x001eðVK,òO6Ehüñ\x0006À\x0014À7x"þ\x000c# \x0011\x0017Ë¾óòÜß\x000e*{\x0007-ÔÏ/\x0013Â\x001f O(,}F»ÿ<-ÓW¨ÖD\x001dté`BRcéq\x001e¶là\x000f$µbðQçùùÑ7P~9è ~~ðþ\x001d4j&\x0005\x0006*¶Ü¸ÓÊ&S¼C a>,\x0016Ì$8r\x0013\x001c$Ý¶ËÝ/ÍpôÎCá²Ìc´
¬íÚ¶l¹¤M\x0004÷¦\x0014\x0014yV V<úwGh¹
£\x0019Íâø\x0005ü¤\x0011ÇE\x0001Ô<@Ùaþ»MÜÿqÿ÷ï¦¶³Ë½×éÐ}¸úrGq\x0006*Õ_0ò â,"àÆ¢Btv~¸÷úì(Ù²×\x0007ÇÓ2 ö¾úvýþÁ±<úü\x0005e¢hþãÝÅ÷ô§5DÐïÕ$´áÎ\x0012jR³yÀO:zõ\x001a¥¢húãÙÁÏéOj¥+®¼DO+§Ç;\x0014\x001eWn{z\Ù<<\x0011.\x001e£Hª(ù/öG¢(Ù~­µ]\x0011eVQñÆäy;\x0006ád»ÂúÛhåÎì\x0016ÃÉ
nê2_³r1äW
­XmIJË¥òa;<]áMÝçkñ\x0002>oèÜád²ÞRM|q4ÖÓÍØ|³\x0015ÜÔ}¾\x0001N\x0013\x0004\x0003&,Á)\x0016Ó~Ã§Ý@ç+º©\x001b}\x001d]Úk>Vt´%9bk0*o~¨§ÿbäB¾º|¸!\x0011ÙC!,T	xÑÎKgL,psK÷êðüdRgÀ¦lêi±é!~ZlfÈf\x0016\x001b²¹§Å\x0016lái°©ñYPÎÂë»?ÿ	76\x0010z!YÚÜÈc\x001a±Ù\x0002\x0011Sd;g_!çÉË\x0001ç\x0018Ñ\x000c\x0011ÍDtCD÷$\x0011Ã\x00101<EDYíEù$7£¬6£|»QV»Q>µíhë{\x000ewõ\x0008ñòûý:´\x0018óxa°1ÐÄ&«yä½ù\x0014óh?¿6zä¸ÀÌÀÚq9¹úp{½.\x0011\x0011@TÔ¬¥\x000c4­Z{åK¨!æ\x0016íäèÅéñÁ$Îº©º¸£\x001aÕ«Ù|2\³dÖe\x0005Z\x0003AÎ3b10Ê\~:çu¾iÂy&Îã\x0012S5 ý_\x0006¥j(õ4 l
e\x0004¯¶òÿÂ=¥Þýâ>o_¦²§8ÌíðÓõ\x0015ù2f\x001eµÿ<\x0019³ \x001dK@t9íì
vÛBöTAJ\x0010sF9r!ÏÏ\x000eÿ\x0003-ÓJ}÷xïðåñÑéÌz÷ñ÷\x0007}9\x0010ÿ·»«\x000bÒ\x0006\x0001KÇ^â\x0000íµõ4ëGIAK\x0005Î\x001cÎ~y\x000cöfïßÎÏ\x000eNf4+²{k%s¹\x0004È¢Ì%\x001b@\x0007:%2¢³-Ù£Dý"2h!uÌEl|\x00072ÒÿId\x001aõÚ·#Ëù·V²`PD	×LgÁ§D\x0016r\x000f®Ùô6k!{ô~°Ì)Ó5°Ïò?&2©eä}¦¶'{ôz°Lg\x001dEü¹\x0013É²8\x000e|Íí\x000f@Vj\x0005ùy;9\x0018¸¹¨8q\x0005éØ\x000eìÑ£Æ"0Éf öQ"ó¹H\x0016¾¥ÙzÉXIªyEl®\x00014N»ÁÇ\x000cf±åg;´dvd»=s&f4Eh&®Ð¶_5òiFó+S\x001ba@]&+ÖtÚ³«;ÿ·ß>\x000còö«+üõíÃW¸?báÊÙ»3ÄÜ8îN¬ÝÃ\x0000¥ô\x0019O¥+uÒtï½>=\x0003w(>ÉÏ!~»{ð\x000f\x0013\x0017è\x0003\x0006$øãíÕzB\x001cTow¯Uâ¨ÌÍûFY9}\x001eÎÁç\x0007¾\x001fOðÕ×h\x0003\x0012;K\x0012K)ð\x0014Ú]ò%¯LP\x001f¸\x0015°¾M[\x00160äúcX@+Ñúi:\x001aÊêHêâûÔ½Ëv\x001cG`û+øeïÇâ(H!)ä\x0002\x001fVWM´\x0002 DB\x0004\x0001*@P"Gý\x001b=½[uÇ=¼3ýIÉ=Çì\x001c\x000b·`x»\x001a(RÅÎv÷ãî«p_ÙÊw~ÿ¸ÊÃÀz_Q©£\x0003Û«Éíð4 µemjMÝBvþêâ´³x·fúí·¯¿IÓ¹tÏWË;8¨ÓÇÇdUHµWhEz^A\x0010Rô\x001d­`.^Âáö¬!ª0òÑ\x000cÄ0\x001f$v&ä}¸ÚR\x0011ñc1²m1\x0010ÃæÝ4dSk1lÞ¼\x0005XzôqdKb S|y¹0\x00088\9\x000eåGGÖÏC9r*?q8ª5\x0000\x000e§Ã\x001c<,q(£$öÛ\x001a\x0002	å@jË½\x0005tï0\x0010å¹,VBnjÅ\x0011låQa,\x0008¼\x00169üÅÐ3Á\x0013Ñ.WÂxÅF½©úÃ\x000cÞ\x0004r¹m\x000e9Ê\x0011~ô;.¿ È\x0018\x0002\x0010IÛ|p¿0¿Ýñ7\x0004Þ\x001cþfBÊ¿#Ô¹\x001a,½AòÔF+Gb ÂRÃ_\x000c8¸.\x001fÇª4M Â\x0003vÃÖo\x0001±OÒ¤/\x00063:ùø\x0010r¡6Z
M\x0019/Ç¾\x0018ôïÔà\x000b\x001e\x0019\x0004Ä#æ\x0001\x0002m|2îáV¾½ÚZ¢ôpðÃòóÍÝ.\x0013ÙxÍÑ\x0008&rjRØ(C<:O+<ëJ
°@\x0017?\x001d÷¬%ª¸6K\x0006q¼7\x0013M;á\x000f¥Ë\4O\x0007L;¡Çq-ß­ä*ÍsEÿ\x0017ÿÂ¢Î?ÿó^¯VËO{
O\x0017òÂ6{1'\x0008Aþ\x0016fý\x0014¶\x0017¯^\x001fåâW§ó\x001dFúðáòëCçk¾¾]^²\x001b\x0000¥íýdJ§A#é¢\x0017e\x0019±ø-ß¯´`kÍöúdñ¬ÔÝ\x0000gZQ¸íËýýõÝmÇª:½üÄ³Cw0¥.¼,\x0005&OQÄ!y¸\x0011ÎÖÕé«s\x001e\x0018º%\x0007\x0006³¸\x0005£òBål¸
P­¼Á(*W¦c¡êu8'^\x0014«\x001cÝÒÁ(>£§\x001c÷±À±À'"\x0014]ëÏ6lt\x000e?\x0016\x0002|é\x0013¹Ü\x0001Ç\x0012rö\x001d?Ñ\x0014lx\x000efy­=\x001eË\x0003|\x0000ÅçJ1< G£p$h0KÐ\x0014RÎç¹øäoGÄ!Cx0\x000cH½ÈïHæÉÍ\x0000#ò\x000cÄôÂx\x00182\x0007ÃÀ·É\x0017ÆÁëùÂ8ïËÁLxÓl\x000f\x000f¿½`\x0011\x000c\x0013J\x000cÑÆr{µ\x0018{Ù(\x001e\x000e6	&æéaø,K\x0018]\x001b\x001bm0d\x0018\x000fKl?O\x0003*ñ1Iß},\x000cYÇa°·ÞÌ}ëpe¤b\x00169A#±<Å*Ö\x0003(|)êT²ïø·-(ªåþÚ¼ê®L¶»$øüEäñ"möáÊ:\x0017ÀÈS\x000ccÙpPb¼Èc»}¸\x0014iÖr\x001236\x000fAAÓÁ°È\x0013a\x0002LÄ5h-Ê (I\x001c¯ÃÊÀzúL6:9\x001a\x0006Çê\x000b\x000c\x0017%fÒyHÒL\x0005Æñ/­ôáÉCÓ\x0003J)Òk²vÂ\x0005Æ
\x0010Ýp±¹(\x001f\x000c¦-ÉÂÃGÄbZÏå{\x001f_:þ\x0001Oõ|¹º\x0002çàÓN·Ê\x0006ÁñäVq DsÄ\x001cg¯|\x0004NÕóÅé3ð
Îûüª\x000e\x0019uí´áÊ,xÓ&ô$\x000ft2Zoûnmd¯0,Xx`9þ¨L\x001b\x0006àñóîØÔ	Ûh\x001bXe®\x000f\x0006Ó\x0000ÎÌùzð5;3Îo\x0013\x0002md9ÅÛø1=ØÍ\x0014å([Á{W¼w0U·é×&²
ûyè¡9\x001cÊÅ8\û<=_àéÌ|r\x0011&Õöë`2o\x0012L?¤Ø!E¾hq«ã3\x0000í÷_~]^~øVj`¶òîÓõ§\x001dTi,µÉ\x0001"\x0015C6\x0008d®?\x0015Øn¼Æ¨Çù~¢JZ\x000c!²\x0018ËËÁ\x0017íû)M\x0013,ÌÀ¬Þö	\x0013mD7ö\x0012\x0019û4\x0001Èàê\x001côu¬I\x0005×~»Ê\x0019
´\x0011WØ\x000f\x0004ÂãS&
\x0002ù\x0018Õ[/ùp 
~\x0000P´iP\x0014\x0019ÁD\x0008[¥6v»½½\x001bèÝ7wÝkýÈ¡²§×«·×«=¡²bQ\x0018Ä\x000fÈ\x001aöý`ÖqÃ¡¾à@ÙÓ£ÓçG§Ç}²\x000e×ºµËùTûò.\x0017;at¢\x000eê\x001b\x0017r\x0004\x0017]ñ6.¸Ø\x001aåø¼ääó"\x0005ÝÆå\x0015W\x0001\x0004"Ê\x0006ý0JËmH¨\x0011\ô\x0002\x001bÏ+Ã`PÓ8>¯È¹ ³¡GpÝÐÆ­q´Óäob
¹Èjhäò\x0014­08®0ZR®\x0002À\x000c\x0013¹(ü×Æeó8xÊx¬á~ÕeD#¸J`§QPÄC_îWô%é©Ç×ý|wóuS~=\x0002Ó×]Îr<¯Câ\x00000½@c4fA¿å¹\x0000ßÏÑWû9¬O\x0011\x001dCfÍaöÓ\x0003-B\x0001{ÆoÅç@x\x001aaSø\x000f\x0003?ªó
:¯©\x0000\x000eá¿\x0015K\x00039:âh?QT\x0007*q ©ÏáÑ@M±ÓÎ£#~\x0006G 7Jâ^\x001f­é»d1
\x001cª®ámá {d\x0018\x0007¨ýà2T\x0014\x0018D.\x000c\x0007-f EGè
ø*\ZÆ4GC
üUT]5ÙÂÑ\x0011rû9¤¥\x0002~k/(vãC¹¥2½¥ÅA\x001b\x0006\x0002OU{z.¦\\x000fÉ·C|+c\x0007b°76ð<<\x0015_É@#¯ÒyDYØèó "Ö¡ jøF\x000e\x0015qä1ÂÀáTÛx->ßl\x001aËqÿðÛãnã\x001dk~1Ø\x0007â*¡\x0005Ù£~3¿B(¯ÎþuÑk»wpjÙ>\x0000\x0007'f}\x001c\x0011À\x0012\x000eÛU^l\x0017$Cyjá:ÇSÊÇàH(:\x001diX
Çº\¯\x0015§±ûqBÐ\9\x001100KeÅ¥\x0002ÉªI§SÚ\x0001§£\x0014×\x0010ã¶&©èxJP0[\x001fÔNß~_Ý¼ûæ2gÃéþñvy·ßvú\x000cN
òëp\x0018«Ïtzuq²x¹Ëzê°}ãe
dSbí\x0000\x001a\x000eÒâ.½\x000e`\x000bÝ7>Í@:7÷`\x0014{l¥Ë>ç¡­sËØ,ÄJÓt\x0016òI,û\Á½t¿\þúû{ñ­Uüìöþ\x0013R>]®ò`»Þ\x0016Î°Ëd\x0014Ðhr"¢ÔvË3xvòê\x001c	.Nq²Ý>°J\x000e\x0007Ã\x0005
1³)Z}\x0005\x0012ÃPw\x0015Ø$öÛoÚÌVÙÎÃÙLjløNIz¦2ôSÙ*?-8
Xl=v\x001a8¨_Háïélü\x001fÎæ#½\x0004\x000bê\x0010pc\x0003½\x0010Ä\x000clÅÛpn¹\x001d
Ù°zÎpã\x000bÉ·à·i¨F´Ê\x0008\x001e\x0016±&+_7¬\x001431k+Í\x0008AnÕml\x001bñðs¬JáÜH/À¹En\x0018
^M§\x001bæòð+\x0004<\x0006.!\x0013Z	Ça«÷ß\x0008WÐ
U%pB¦|F\x000b\x000cgä6\x001b­\x0011\x000eþ\x0011rÄSÅå%:\x0011Í­d!éÈâWë\x0019î\x001cWë´ÁÙT«ÑçF?3Qü\x000cïAÁ[P#ÞC\x0004m\x001bI­ð*/³ÔÄ\x0004uK`®\x0019\x000eý÷\x0000JUG$´Ï\x001cà\x001c»\x0005Aé\x000b\x0003¢jÌ{pE;À+\x001bq\x0000\x0017\x000ciU\x001fç89P
jzÀ¹r>«\x0007\x001cÏGêÁ\x0008\x0003{\x001f¦ß9Ü\x0017¬ÇÜ¹èÈ»²¸Æ>«¡å³\x0008·5~Ô\x0008\x0007÷M·ß9\x000bÿ?©M\x001eþ_5{ÆFó.µ1ï><®¬Þ0~­þüÏ×ÿ×³ûëÇÕÎ¢\x00130Ü\x001c%\x001c¼Ì¶/öMQ&&B¾¹mÏN~ßWG\x0017§ûÖ¦åP$'È÷\x0003k¸mÛ2sßèÑý<Âuî~«OúûÕÛ=>H¡¦äÊ¼;\x0011*QR~îÛ+O5û§Ïû<\x000eÑ¦':(R1\x0002¸\x00074ï\x001d=)Qîü·â«hÓûÜOd%\x0005\x0008Áñ4y\x0003\x0012¦aJúQö¥\x001f\x0007\x0012múû8¤k#
(/ÄÕµ¸:ã[£b/Ð/¿~½õW[®ÑÿùÿëÇ?ÿ÷ÇOË]%g\x0016÷ø\x0004IÑ1E\x0001LaÖÁh·^¥\x001f_½>>_ô\x0015u°ê»4\x0018ËrE\x0010nª'±©×¹c³õ¬SÕ_o\x0018UR5VþEIFk%\x0015*¾-X©ßÀ]<¡D¼£ \x0019{½NÆ1\x001fQ¼\x0013Þ½ûæn=\x001cüs¹z³§!\x000bE¥\x000e:ïs/\x0004VKXÇEbË\x0017<;øçâôþn¬\x000eQ÷Z
$2÷÷XÄmXhr£Ý\x0012¶h!ê¨Dá\x0008k8<\x0001Ùuoß¸]\x0003P÷\x000f\x0003\x0002	@'\x0004jEs¬-)lÐ\x0004ÔM§\x000f\x0004²é¥ÎeÚWjE±ÌÜì\x001bi$*},-H¾ô¨â\x0006J£;ëyH\x001fñÕ®þòû\x001f[­\x0017Ë}aLaS³\x00065\x000b
Nwè	²¾X\x001c÷G0;LuIûl\x000ciw2âD\x000e(ILËj\x001ee7\x0014iÓD\x0019pLRcÒy¡rá«rLzâ1m#
`\x00021iI¢\x001f\x0013Jkèv2iÓp\x001arNK8±PÄèVk-g'2m!
9§R\x0010ÆÓ: ØxÚ\x0012;mbÚ,A\x001aÀd\x001c9\x0006¼ó\x001ckFIÀU6bzÿõËo\x000f¶>»×÷\x000fö\x000c6PiT}Jæ\x001c\x001bJ
Ønr}5Q¯_\x000f Ú¼M\x0003b©¶Ã*S\x001epÀJ[0gÓ\x0008ßÏ\x00138´¦¥Ò
!dÙÄ\x0013Ú,\x0019\x001b@d©Â<Õi\x001a#\x0013¹¥\x001e\§ôÝ0¢ZÇ
D
T\x0012\x0005HykrB²eL£ì)a\x001bÄ]
H±8O`5Câ\x000e\x0001'û#\x0007\x0012}SQ7HóT\x0015T'¿(ßMêiÔ
Á\x000eE²ådo%LQpbÒk+]-D´b!ë\x0012G¦	í!F]â&!~ÅáHh-±zºmÉ!j\x001bÍ$	Pº\x0016\x001b¤ Õ` IrUkÒ¸e@O\x0008=ÖÒ@$î]lA24A\x0010D©bU\x001c\x0017°AøpòêîÒ-\x001eåëÕÿ±ÓìÆâ K\x0015Oî­\x0017JpÖÃo­^Í®÷Ãt\x0015í\x0010\x0018%K
\x001c§AmQrÒm)R\x0019\x000cS{¶ûa¬KÎlª±\x001cÁQû[\p[\x001da0]v\x0008\x000c\x000eº"«ßÑÜI\x0001÷\x000b*°H`4Kí`ïg\x0001§ÚxúJ4m
ë\x0014J¸Ûæ\x0016
éÚ°`b|¬c
$ÀWFL¸1µ£¿ÅkJ¨Ãß\x001a
®)ËÇ¢·Õó\x000fEéÑ\x0003Pðù°ÿ\x0003æ4¥UðE¯ë	\x0017¦7ì¾\x000b¶±Q\x000eN²\x0018vvK\x000en(L\x001dÚ\x001bBc}q/¼á¦Hí$\x0017
êmEgCi6\x0002\x001fûiÈ4M)æ°\x0007&OÕú1M8n\x0011Á \x0010i¸I*ZT¹\x0012E\x0000)4u:Æg\x001b\x0019Ï\x0006SÊj¾6Ûâú;YìÝjI!³¬ÎWËÏð¯Ké½óÇÕåýNÕí}©j3¥^\x0006&\x0019ïu}Àùéâ'øÏÛ;¿8}új\x001b?¯n~Aw\x0013ðyqìÕýÝ]²%L\x0002\x0002Õ|
)ËÇ\x000f×\x0008$¢\x0006µÎ'x\x0015\x000cîÌÄ\x00047XôékY\WhóúÙÔs²¸xqÖÇþpúêåö)S5\x0015Ù]©°t[\x0012UÚ¯¨¨Üâ°U7
Ï\x001aÿ\x001aNeò¤U \x0002ÛÙÊLå½&*-ÃXªw¿­Þ½Û-\x0004X|¾¾+6áóåj7ÏÓE\x0001M4I\x0017Ñà©Å¦RcÓV4¸a/ø|±}YMHÕ\x0000"Mö\x0001@\x001fÐÍÏÊ3 R³\x0001Â\x000b{¢\x0001ÈÑ\x0007<Bí¤jãÐõÝ¹fBÛ\x001dÒO\x0013¢\x0004D\x0011\x0015¸%*#j­&@´~"¡»z÷Á<vçctÖH\x0000ÌÿùöÏÿo\x0007£ÄïÓ\x0002\x0001÷Tcw"0zirE ¼\\x0011ÿYÿþYkÈÎF	ü³çÛ\x0007%v)á@°PK´cJ!¥èû"%üóòuÔZ¡£9\x0017%îZH?­\x0002´Wòô\x0002\x000eèFÿ\x00010]´¹\x0003\x000001f?\x0017¦ÂÑÌég\x000cf~:VâRIÆÌ\x000e `ZÔ3aâ>'é§\x00193<(ÀKÑX¨0=½pm\x0004:\x001dsabNúiÆä&Õ`5øFÂgL¡i1.3\x0017&ª÷ôÓ	0ù05V=fHÅÜø8\x001f¤ÁDúi\x000cy \x0017P4<aê<$\x0012ÿÌÎw3±ÿñIúiÆÔ*{ i%Î²Lä#¦,4½þðkì\x0006æÖÏW z>}Ú\x0005)A¶çfó\x0000n¨Å \x000b\x000eÈ\x0008\x000ciò\x000egï«ë­Ï\x0016Ï@õo\x000fA\x0001¢ôQ¦éL(,kÉÿÜ]Æfã:8x#Xü\x0000MNÚ[cÓXÅ?..zLÿ.Ì.lå¯ò\x0000\x001fØÖFé\x0000È;;¦óá~,iE# y¡È'S\x0003)òù ù\x0003\x0007åæáÛ¢¶\x0007ñÅúÀù:\x0004#ðÈ\x00170ÎÄYôÓÈ§r³\x0017>\x0010W1ñy[\x001eH¾23ð¡Aá[ßTO\x0006|>Å¹2_`>WHOçÃäjúiã\x000b¶ðáp3ùh¸0òÍó<\x0014F+ÓO#^ÈR\x0001ÏYÌåæã\x0013||zø\x001b¼eÕ''O\x001e}R2¼-¨aÏxrô\x000b_ïõ\x001fÝëÎ
\x001føÛÏKð:0Ð±CÏa´Ag¿^K\x0006¯+þë80«7Û(Ï\x0000óè§ÅñÉ	\x0006Hö ¦Õ^Å\x0006Vcs¾\x001e-ãHÝy\x001dÈÂ±2\x0017\x000eûÎ}óø>i\x0015|5Õn$4\x001fÝßýrûx}wµÓ5´E9{©<\x0006àÐ5\x000cÜ.+}oÄ¤² ½zù£ÏútôÃKµJ×\x0000íðz5×ÑÃÕíòó2íNï7vò¦0t\x0016tj4B['M\x0014!f¯çuvptöìdñÓbû&õ\x0012\x0017X32kÉCÔt .¸©â^¬SâÿêôÓ\x0008*£
¹g\x001d@}¤ \x0003³Aq"ú hßÊÊÈ\x001d
jhü\x001cZ%é\x0008ê#û²Jî5Å[8QBÉ
15S\x0005¾à%1½eg6æù8m*o°#85
O\x0000P«@\x0003¹6*ú99Ó"X%F'Î\x0000ù
®Ýnï\x0014\x0011Ò{]Åý oÕÕÛWI¢ñVm¿K±5\x000cÓïÄt.-CFÝ\x0004¢_Hº$(¼w»OÞ§è\x001aÆì÷BºÔa¸\x0019kÙ\x000f©50¼ÊIÜ\x0004i,Qµ
S!ûåþæám7l_1þ¸ÄQÏî?\î\x000e°I[!Çt³w9\x000e(é¹£Y7è8Á&9Çn\x0017O÷ò¦:£ô3
\x0018}Z\x0019\x0016\x0002Í7ÏË@ß?D9;0ÆÒÏ(`,¶R\x0004¬13iñ\x001b\x0000¸×j\x0006FaõMPkð	G²P\x00036Üy

ÛÜWlmL\x00199ÕåíG÷©ç
cãÆõêÃÍ§åÛ&Á$_½Ë,;¢½Rd\x0000\x001atÜ÷T\x0007?\x001e¾8>_lï\x0012ê²ª»Sb\x0014lÚ*N^\x001e²FËË¬ÕÖÎúéòÍ{©úïÁåÍ\x0003&Ñö\x0004\x000cÚªÙOV8·7[ ÉS\x0001ñkw{*¹N÷\x000cói;¢Iêö½
)\x000fí¶¸öñæúqõçîÎXyrG=zöùºjW\x0004\x0002XX}é¾îöÇã£ÞtËS_>ZDÄ{³©\x000eÎ«Ý	!ðéÈHõJCC7%JûUö\x001býgÓ^Dyûå÷÷iÉ\x0012rð~\x0003\x0011÷SîbJá"|àÁcûaò£\x0004{&
\x001fòêq[å^JtShn3%´SÃ\x001fåÅs ÀLÉð ¼¦ü_LûÏgãTSàT"ÏLFNM±bäd)ªì =53Ñµ\x001d=3ûAøHÏ\x00079\x0003sª½þs\x0003§If\x001cgdNG÷\x00138
ÝÏ(£Ìy\x001bÄ×KÛ)®\¢@\x0012ýqðâþñöænw~Zó;\x0002¿¢ \x0008\x0013§×ïF?0ú\x001f\x0007/^]\x001coÝûZrÝõ\x0018TÚá\x0008¨¹É>£²622ì\x000bF4²\x001aà4#Y5}Þ`\x0015´bVBÅ®ÈYQ1,ß
Í· ÆÜJ
¨ZÞÔÎJ2þMÚ1'+ÚÒ~ämå\\x0002	§Ä\x001b°²­gÒòºé¬âRë?B7\x001cµ^NÈïÿîúöv§\x001aÅy¦ìúé@ivmE K\x0000\x0007ßgé­\x0015²\x000cxytrÒ'\x0006>¾{óõK
Ka&\x0005ÿêl,|ÚþÓNU*\x000c\x0017ka\x0006N'Ô+ÉFîõPÖ{\x000b¢®ß:¯Ëº\x0011ÒO\x0013 tl\x001a§¨
ÉKïXÕG­æ\x0002T©.Qµ\x0002b°lú \x000eÉ)¥áõ(D{e}3`D?mVÃ\x0005oqå½ÏØÔCïFÍu
¤ôÓF(eÚB6­½OÂS\x0010ßø^/®Ð¥WÒúL\x0004&ßr\x0014ö¸dKÎ è\x000c­ì38[\x0001
ÆÃÒOÛ\x0011
Çk\x0007ïÁ·ä\x0008\x000b.otÚÏõÓ<ôÓx1¯^
>H¹. dãÍÞèM3!nJ?g\x0010#¡T¬öRRe\x0007\x0010öF?\x0006\x0012~½¼ý*ßt-¡5àÃÁùÿï§]	9P6O´MZÅ\x001eR=!µê¢RÑ}Õz\x0005ðìàüè¼7#·\x0006ä\# yx:ìKÒâõE
\x0006\x0012>8ÿÙ¦=#À¿^n\x0014\x0012§×·Ë§·×»ë	]^íFO 'fäbÑÍ}"\x001b5óây*>=:Y\x001c\x001f<=9Ú:\x0015	H}wwûñs§M¶õ>\x001eÈxðb¹z8À50»uX\x001b\x0011êÄ¢\x001cõN÷qæÅ½\x0017é_µ8=ËÿªíÜ]Þ¥ÉR¸v	ÿZ¯\x0015þ?ÿó\x001d½½½yØ\x001d2\x0010Ôºm\x0008G\x001f=\x00066"e¯\x001f±^0|pôüäø¬ÏÊY>|x¯¾t+ÊaÃ?\x0014,ÈÛÝ¦#ñx\x000cÁ\x0008É\x00169©yd\x0017áÅÁùñÉ	\x0018[§§\x0000á\x001f×á]ì
ó§\x001fnö\x001cä\x001apñ!r\x0017,uÌ¢Ï_à%O\x0007?lï/¯¸LR,-\"w¼"\x0017×v\x0000W	\x0005õ×W7qq:u(\x0017\x0016Âx.LTs©1Ê	\x000bÙç\x00074qa1k8/\x001d,ÛY\x0012\x0017\x001a/å8¸«toè¬\x000b^¨ó
\^\x001d2Äj±|÷-\x0017¡k3\x000b£òMÇU²9J¨R\x001coäH£îk\x0013iã¢\x0018ã`.çXVÈ\x0006wå¢}öÜ³W³
-çåó\x0002t^l?igø5Z1ËqaD24\x001d`Û]\x001ePtëµ,Ç\x0015fyèöÄã\x0002¿QP­\x0012\x001c î\x0010\x0012®7²ÑÂ%Q6§á`-õ´ÕÄªæ\x001fåÕ\x001câ\x001e­Ö'ég0\x0018®§\x0013Ó\x0011§\x001eå^¤\x0008ö¡/9Ñ\x0004ýÉég0à¬$\x001cbÁj]à,z\x000b+yÓÏP.\x0005ÚÚÂE_\x0012x86ú©'­xÁ°.\x000fÌÇ¯qÿ\x0004é>+¼\x0005L£vÔ-*Rà\x0012tbÞP\x0006_ké9Ü${\x001b¢ÚÀ°©Þé\x00160Ú^\x0007`\x0018¹c0Q>¥Cºjú\x0003\x001bÄk
<´ÀMàYêÃ\x0015+%$~OiP\x0018¦Á`ø\x0012¹Ë3r'îPØ\x00169l\x0005[>^¹7o·ªÉçË;­V°Â¸çN\x0008*
Ò>\x0018®±LqÝ\Ï\x0017¯÷qmû{À,\x00189ô%\x000f8Ý"S
N\x000bH\x0015ö\x001eØ\x00100´æÒÏ`0KH`.ä\x0000&X;\U#å,\x0007JÓÏP.ðòØ\x0000®d Ð´\x0011 j3\x0018ÎU\x0003\x000cÏJ·\x001c\x0018\x001cSÚ¬\ÉAO\´]\x001d7ë½úh\x0000Á²«ô3\x000b<Æ<4\x0005Àrq©\x0001G$Ë|\x001d§Sá\x0012yÔÞÖ\x000fÅÂ\x0016\x0010f\x0002\x0003McB\x0016¤+õÐ8'û²¶\x0003È\x0008~uÕ\x0004%^<{úîñÃÎ8PPöNÑ´þôZ\x0016C¬Ûà¼ëâàôÇ\x0017{Á0ynm\x000b\x0018ºÛÜ\x0015nÉ\x0012óZ°Á£c_¤´	,
\x001bL?ÃÉ\x001cÍ\x0012Á
ö$6Rè,°3)£åÌÒ"ô3\x001cÍ
ê\x0012Æô\x0015Õ\x0002ýã=«¾\x0018ý\x0010´;ÿñÃ¯õ\x0014Q&ãà.8lM ¸¨åØ\x0000Ù\x001cÏ¼÷þt|r²8ýa/_\x0019ÿÔÀ\x0014*LÃJÕ\x0007\x001f¸Þ:t¿Þé¯\x000f¦[Ôy¼¸]~¸¼¹Ú\x001d²\¤MC¶Ï¯¿0±L?^,^<=~¶°\x00042Ú\x0008q:¬&BM¥Ó`åZþÞÞ7öã½¼KÆ\x001aÆiÅzÂ×ÓûÇÕòáá~Gú\x001c´¸\{Kà¢bd® ðAîæ{úêâtqvöª/o¾æK¥\x0013Æ¶ñÅ¶J|ÖP\x0018ÔHWÐÛÞDo+E¥~\x001aøp2Ð!%aÉ'Ð8Ê|j>>ô\ÒO+\x001f\x0019ä\x0001´Y\x000ex\x0000 7\x0017ë\x0003£©ó$ý4\x0001`QT¾Ãos:\x0003G\x001cñ	Æ^\x0001Ý\x0008èDÝF@°~É\x001eÀ91?aáX¹y\x001dûò-í\x0016\x0001ÛÂ=6\x0000çb
áÙbñNÌu\x0007\x001d&´ÓO\x0013 ¶[Ò\x001b6\x000eGAæ49û÷>I­y\x00001~Z\x0001)\x001arñ[\x0006d¾þnÁ|þî÷Ï÷ª[Ås¥~À*§g·÷Wïöt	*c¨ûÊ\x001bù")å\x001a¢ß\¦YS?`Ó³WÏ~ìï\x0011\brÎ1 ÊÑü\x001d\x0003®¡Ò!Ã\x0002Ç°û¹´¢Õ\x001bí\x0018Pl¼£¯j\x0000+#:ô\x001a­ã@Á¾n\x0004(&h(\x000ce°TØòéwKÈa ×òvySÕcv×Ü}ZÞì\x001aZE¯L\x001d\x001f¨\x0010\x000fää:×?ïn9yy¾8î\x001d^Õaüf0î`Fªkó \x0018±Ì ó{tM\x0013â7r"z>F¡wb´%\x0018ºGa·0VËÀ3Â÷UÌ\x0018Ùo\x0011\x001b\x0016´{Tb\x000bcÉ·1:\x0007ýc\x0015sqã\x0005\x0007ü´êm²\x001bXKõÁX·Cõ\x0007Bl^¨Pª,g\x0004DÛ¶ý\x000cÍÚ?\x0005\x0019ç uËïE«}þU\x000b#¼\x0015Ûþ^\x000c-¢ÅCTR\x000b\@F\x0003¶&1ñÝÝeÒh^tÍ¿\x001eVðÏ¾¾û´[«\x0012\x0017×A±&¹w\x001a(Õ>­ø¯ÅùéÑÁOG/ÏûDø\x0013´í¨Ú9q2\x000båGSáoàFÎ\x0011éÞ\x001e1I%È®R\x001c\x0008K¼ÒòTMï\x000f}=\x0008Ìjø?fäTXó¦´\x0018Á	ö$m¸'6ÒÀ¥R©ìü\x001f^a\x0010E1\x0007j\x0005yc\x0003w£GQr]Ñî~ë \x000eg;º0\x0002TêÒ-é\x0014w&\x0007ËõFìñ&\x0006þú2\x000f?×\x0003Oï?|¼>x¶§ªÌDV<
¦Ò¬%V\x001bP§¯^¼>:xÖ[F¶¦éNÉ\x001d\x000b.(6\x001bÒÌô\\x001dÚ±yzó%mdU¶\x0003É4{]*ÏïÍd6n\x0013È0I«dÓ'4%ï\x0016#×«õ¬ÚÞ¤\\x0013Yw£è@2\x0016ºP\x000erøNÎ\x000cÕÛðÔHÖY':øÌÈT\x0010k%\x0007I´Ö½E\x000fM\¨ÌiáÒ´ß\x0014Á\¹eBYºýÌ\x0001d«ë÷oß}þÆ|y<8¿þðqW3\x0010æsl)8\x0016n\x0019@)¿¦·Ë¶°\x001f½xÝÛ\x0002ôÅÜ¹ß\x001f7eF*ØÆD·{ôkz\x001986»F[L?³'0|Jc.Nú$ì\x000f
]­\x001bùÀïpd;;K¡\x0017µ.OTîÓ\x0002Ãù0Gm\x001aùÀÊc½/4
y\x0000¾b \x0018»Oï\x000fæÛ)
âs«\x0011²Õ.Vi»Çk Û\x000c$
¢\x0003¥EõD\x00040F¸¬QÛÞÞf>\x000cXûV>ÓáS\x0014Ñt¼®	ùÌnïr/ßÇ\x000f\x000f¿\x001bìXæ~~º¹F´\x000c\x0014¶è\x000b©\x000c\x001d$\x00064¹î%Ï\x0018ÿÙgËÇ«j\x0008ÂOÇGx00÷Ìõ\x001f$û\x0006\x001e\x000e\x00167;GË¡°vTÖ¤4÷EYÍµØ?·»eàì`qÜ?Z\x000e\x001d¸ó²õ\x001f<ñ¾^?¢óù:1íTwë²HÃÉxPx,TÐ}ÆKé\x001døçÑ\x0005ú¯Óî\x0006Öª\x000b¹Ø\x000b.DWÖP/\x0018V|ÉÞQÄº"Öcçørr]ÛÌ¯LEßW~7ØTÄf\x0014±×kb[\x0010l)\x0013¢ÏØ\x0018E\]c3ê\x001eûÒ§°å\x0004æ\x0012Ç6bzy²þ²Tèñà\x0019x}»' µDI$-x\x001a¶<Ó\x0016ì¸þ>
ÚY\x000fî^ïÜ\x0004\x0006²\x000bX¶£\x000c#ÔTÑäq­\x0004Õ\x0018ZÅ\x0015Éà\x0018öVµ\x0010úÐ7\x0011FnJÆ©Ô»\x0003`ÅâìÝÁÑB¨t°lf\x001bDuº\x0010\x0006"4Ò\x0015Â9¾²µ]Bk\x001b\x0008\x0011¿²2<\x001bÁ\x0006©êßåO\x000f%t\x0015¡k"TKJµò4gDÛ¨q²Óã\x001fJè]Ð»\x0016BÚÞ\x0008-Ap"pÃÚ9^J¨^Jhy)É%BÍCå@½³wáì®ÐÄ@@)ê§,\x0008-õV§©9PsJPûÞªÎ\x0006<©jY¨Zð@a\x001bº`m¸Ò/U«½½M±FM'\x0018i\$¸*SG<\x0011\x0019!\x000e^ê\x0012*Ñtë\x001c\x0016'ICéÎ~Ú5ÔY£¬\x0011µèì'KCÿüß»f¬åø"¿\x0014PÜ·T<¡ØßèUÒ/Ï^õÎVcFeºuÊr?£Ñ´õÀ£M)ø5;¾±¿¹ª\x0005ÒT¦\x0011RC¡Ë¦_\x001bK\x001bèµ\x001dÛ c\x0005\x0019Û UÞ%F\x0015¡9\x0005%Éïû{Z mu¶ñ$q3\x0010%Û\x000cí\x0019\x000bÅNôvct\x0015¡k$òÚ\x0008\x001e`}Q;\x0015ôPD_!úFDa\x000eíZ\x0001rwÝ:oåfùÐ¡b\x000cmà\x0000rWO@{ÒJÏ\x0005\x000eÁ\x0001\x0012«Bº\x0002Ò6JpW,[;ôÑåBºþ~À&ÈXC¶=l¤èñÐ3ä: 5õÕØMUcªyvÿ¸Ú'ÁMùÒx\x001cn)×\x0011#Zý|Ï^]î`³YÅ¬Ù¬x¢*5¸oa2·BãÎ/¨Ò5Ò;Øk}~;Ö¥¡Ë²áüýÇÎßóÕòîÍ^-Íy#¿î{V¾\x0004&z7º!ßóÓÅË\x001fö±u">Öþ\x00006§Ù\x000eSA¯[Ë\x0003n2©ÎÍ\x000c?7°À¸\x0017æu\x0005µÚé\x000ebëè:\x001c+`\x0006³Áô¾DD\x001cÇJ\x0015Þé\x000ec«ÎÍ6\x001boIY7Á«XGkv\x0019×Øè²91-rjFõ\x0004\x0013³Î»õÏL\x0018Ìf+6;M(\x0017Ö9°ÛTä1»Ìéal®bs-çÆs$xí|l,BÌN§}\x0010W]4¯ZÐ\x0002\x0007e$_g|É\x0017ÉO¡c\x0004 [\x0018þLe96å\x000fÕfHØöw`\x000eF\x0015ZlnåØx£\x0007ú%µ30-TÒ-4H·Ò\x0018¶\x001dvµEò:1ùºJº&­ y\x0002§Í2)"\x001aC&²ÅJºÅáÒõº¤Æ®Á¦«ÒX\x001dZl84_ÑÑ\x00108ÃêS\x0000>Y´ÅêÆ7jJÙ#\x000e¨ã¼Y³í
\x0010\x000ca¢z\x0008i\x0003ÏP8Ëã1°d\x0007ÜÚârï\x000cÚïaóaÃ,\x0007Á&×1ªS°Ì÷\x0018æG\x0005+ëÊ>hÉWUX·¨N_õ­/|¶â³
|ð\x000c,OÊ ÏÊ+ÇÁvÛ\x0013f\x001eÂ¦ª³S-g§!:¨\x0015ãñ0¢¸/Ù1ÏT|¦Ïp\x001es¥rªÙ\x0013|\x001cD\x0017*ºÐB'0þÄsv\x0014¢Ê`¢\x0018ö¤9ðu%üT®\x000f×äKè\x0003Vç\x0008Êº\x001ff·K=/V|±O\x001dßØÏÁ\x0011R\x0003${-\x001aøBu~¡áüàûa¿4:ê\x0012Ü)×Î°É>¼°\x0019\x0008¶+øÎöÌEÚÓV,\x0001GåyÄYÙ"÷ßÙ®¡°LhlÐØ\x0016BµNU
½~!ª8a;þÁ®"tMê}p\x0017¤tbµ¦Æe\x0003`ÇÁ\x000ek\x0007{\x0018 tE÷\x001fk8P\x001bK?Dïj\x0016BW\x0011º&Ba×Q\x0000KÛ81P»&ã#ûê¡ø¢pÄ³.4Ò\x0011÷]\x000cªÀ\x001dL\x0018+ÂØDX\x0012\x0006j=ªÖjCµ;x7\x00100TG\x0018ÚPwR6rXS¢³º@Úp@)b-\x000cÐÉL\x0015]"+eAÜ\x001eØ1\x0017\x0010±c/\x000c@Ä\x0001\x001cki\x0013\x0015ÅhK¼Ìì3h\x0006!\x001aY!\x001aÙ¨BñCp\x0005C~*Æ­\x001bîÆßD%þýÍoauÿs§¾^\x0000¶x³º¾z\x0007h^$@%ñßõôzõ°¼Jõ¤Xá7{	
0OÄó&Æ<­ÁH%1¡øää\x0008°NÏ\x0016Ïª­_\x001fNý¸\x001bº[Ù§Q!^ÂñåÜ$°©<eÜHÿ4¶táÒO3yH\x0003À¹¢@Þ`ÀØÒÜ)lR¹4\x001cÉùv8lYJ~=\x0015H§¢ ¯j=Ö~¡û°ÔwËðsgìíéru\x000b¾/îqÛ\x0001\x0017\x0005/óóRj\x000bÿ¼Å]*	N¼ß
÷tqz\x0002Þ/noÛÃ'Óð¬üÛJ\x0018pbXÁëÑÞÍÑG¬[Ï
\x000e\x001bçrË×4Â´«N\x001a;ÐåÝC\x001e=l«\x0002¡ÔLhÇ\x001fá¯Æþò>Þç÷jø×åí®¯d)±\x0007\x0002%hüºÆäiö\x0006\x001b)t\x000fÚ³\x001f\x0017ÿ¾ØÚÓ¥J\x0005é§	\x000bÔYÚ*[#ÓèHÄÒ8S6]º }ßíÄzsy}\x0013óp\x001cìüÛÝ\x0018~»ü|}»|ØÓ\x0005S*Ï"QÙhöNÙìW\x0002b°
íì\x00007Û\x001e,¶ÇwéÒ¢ÜüÛD§@zË<
ÎãD**H§}Þ¼®£Á5w\x0013é"ÖäßV:)ó¾0\x0017\x0003\x000e\Vùì\Í«ÁÜ÷=/u0J\x001a?ÿ6~Y\_+3\x001dhü\x001c1ð\x000eNèd*g\x0018EwóU]É_Q¥{W]»\x00177«å´¨~ç½ÃdIJ\x0002§¼æêÀbÕ\x001f]ßxq|ºxÓïÃSxwÓO3^ÈË´q.
ß\x0004º\)\x0007p¡×.Ù\x000b÷ñá\x0006äP
Vmîx}\x0000CìíÝõ®¯\x001a¢ô¹\x000f5¿>:%AKVýÈØþU:~þr{3KKaT@f0k°\x001f\x001dÁU¹*Îã1ÛK"\x0006Ä¶Hm\x000cæÊ
ß¹©¬\x00119OãJS+ÒO\x000bWÇ®WÒ	X:J\4Ë\x000ft7½w(\x0018®S±\x0019Ì\x001c®\x0002\x0017Çä³_c0\x00047
5púiûÞU$­\x00149¹\x0008XFÓõ
ºÏ\x001cß\x0003öþáóÝÝ=EïÔkÅ\x001e\x000eö[»Þ¹<\x0004\x0008ý\x0004Ú¬\x0002.Z~®~\x0015D;mÝ5\x0017\x0006vjæÂõõL!ym´ s<ÖàD\x001b7W¶ÍbÜ\x0014"rW\x001eql¢y?\x0011gá¶±áH1\x0011¤òå¸ÂT*vD\x001b©<mãÂ}/áÐf\x00179ÜQ\x0005`Fi`©Ì=ý´Ê3SpkZ9N\x001f\x001cdeÝD2ÑOÒO#¶i\x0019
*oÐ\x0000Ì±\x0004Y­F]ýêä]òMh\x001bngóÛíòàÕòËN£BÉÈW\x001f»¸mö\x0002"ó÷¶sa9ß\x000f§ë³):`ð¿Lµ©p(	Lú¼Ýc&éØsù\x001bÀPê81\x001aÇ\x0004`6)ô\x0018$]k\x0008'aìj\x0004ÏéB\x0000\x000b¹OÁç_\x0006±çî7¡\x0014k\x0007ÃÚ½Ì\x0015]\x001egSmsü\x001e=MÙs÷\x001bÀ@q¸f0\x0019h_5(påyÌIG\x00023¾G\x001f5á\x0016¦v0Â@	LE6xÀöL6ýÄòn¾V0ð<|Öà\x0016«lóíW8,ÄØcZ4åqD­dÒ\x0000\x0019®f¢I9\x0018$\x0013?æ·ÖØ 4Gñ=ç|\x001e<å­¤ºB\;ýeòpöæS£rxj\x0014&îÔå{êÉh4¥õÔ$mÁ-|4!\x0003£¢y[¥ 7ìd4\x000c\x0015´«\x0000\°\x0005\x0003e@ñZ%\x0014»2L¿j¸©Y\x0007h¨ã/[²JgY2\x0004QN¿jß¬p\x001dö=]dÑáLÞ\x0017
ö¸Á¡\x0019;Yoò®ïñ¦Ñ4×Öïétî\x0016\x0007ON(Ü6Ð¨É\x0014#ðfúûÄO³*\x00088NO3'uNËãU+am3Ù@ãp{ó÷4,ÔàåÉDð7Bð¡\x00197ùÐÒn²fU"?6_µ\x0010C.XÁï)ÙÓ\x000cbòUãap­hQ±
v¥àæ«f'\x001b\x001d¸8U}ª÷ë6?P\x000b¥áÔ¬Ã½M9\x0006dèÔ¤Q\x0001\x0007euÊå[ð@EÌ]G&×º@ÄéfÇÏ7\x000fÉôÀÿlý®vUb\x001c
Ìà¡\x0006ë¥êÕ1×þwá>m}§¥²`§ý\x001d8¢\x001dÁ]÷ä²H\x000e\x0008)¥·«Q!õ|\x0000ØæS\x0018\x0006\x0016Ô\x001aLäé>Ok$0±ýº5ÑÀìV°Èï\x0000ä\x0004ÐpX#G^ÒÒäI`X ®]3\x0018XÜ,"x $;´ÁìöW0\x001c\x000c\x0007\x0006Ð\x000câ"Ë[Ôò!
%Û¤õÔ\x0013Ã\x0011\x001eV7¡uFÒ«\x0002æÊ§4rû³l\x0000Û\x000e\x0003S&o(öi¸_$0êÂ\x0013ë	
\x0007Ã(o.Í'[Ñ[\x000f\x001c¨5=Á½\x0006.ø~Äôä§à°FGçå=K1Û\x0013§\x001dÎµ¡!¶s©R\x0012\x0011<Ð,Ä¬zÁ°a$Êf.-9\x001e\x0004\x001f/oIAo80×ÄÏ¶¼¦6.\x0011¨¿Þ+aH\x000e'W/i)&\x001eXòXÓO#\x0019hÇ\ô\x0005Çæ¢/K=ëÀ¥{\x0012:¹,Öá¦Æ/)\x0003Î¬L\ÂçU\x001d(*$¹\x0000*µb ûüæ÷ÛÏoºÁ \x001aVeh«åËÕ\x001esQr\\¦dÓf3²Éb}Çh6åÁâtñâéöbÿª¬h¢
2·é`Í£É#ÜÊyørÃm¤©ØFë6,¸\CzhìPt|X*->5aé§
\x000bÃX
D%\x00052B,i¹\x0010h+\x0015v¦&*\1M9ß¨E®ã\x001b¯rL\x001b\x0008Çc¥\vúiÂRBæq:ø
W©.ßPÁÒ\x001foÿxÿ®ªW-kYO«åÛÕÞ+rìB¸T3\x0003¡o\x0008BÖÇmTèx.÷V
®±6¯Ö0,\x0019ù\x001d
\x001dóL\x0001ìÊ <c­DMh¤Â>å,KãQÅ¸³.RþFx)'aY¼ì¶sã\x0007a9PÖ!S\x000fF§âª?ºïàêiÐ¢6L?mT¢bÂYZ/íÝ\x000eK¦\x0015ô\x0013°<ê\x001cßQ<°¬
y\x0012»Kns¦K+É\x0005Nn\x0015Y
Ph7KÕ\x0008\x0005ÿò\x0002¥òæZ ¢\x001c\x001a77oU;
X8ùZ6^,¬9õå¨l²iÒN*:«í\x0002k8T\x001aÇí\x001b¡¼ò¹µ\x0003©\x0002Õ&\x0018\x0015nÚY}üúð6üò\x001d\x0003çé§`-?ß?®îÒfÁþNC\x0013W½Ò ¤S¥wÒ-omÏ+<[üôêâôåö5\x001842´y¸òÆg0ãó\x0018Sï\x0013z&2)l2\x0001­hEÃíqÊ\x0012c\x001ek\x0003/Ôr\x00125ZÕ##\x001aÐTBSÍhØºáJÉdv\x0019q\x0001\x001fgi\Ï5\x001bf³j´Í7M¸áUArR\\x001aGÇæÒ6l!±5_6åV*\x0001¥fÍíÜjÖ7 yÇÐB\x0000×?WHðµu.\x0002s¾¨5z*ZÈ\x0016k¥À¡	jcÓ>\x0007À\x0012©6©_4dÇ6´Þ¶\x0010$\x0015la¼+·t\x0002\x001au3\x0001ú\x000eàÃ$²ö\x000f¥*Ð8\x000cf5T\x001có\x000b¦¡áþó'ù·
Í¹Ò<*bóesVr\x0001±\x0011\x0013%Â'ù·Í*Ç`	FZÌÍs&\x001e\x0003Øf\x0010e\x0004\x001bÖqäß66Ðã|n`ÀRm¿\x0001õÎÔT¥_ù·
÷TE\x001bu\x001eÎë%½\x0004­íÄë\x0006P:¡éf4x	Ô(\x0014°\x001a)R\x001a²mòaâ#Ué¾æßF4ï1\x0019ÐàªûÑJ \x0006\x0015§¡YÒ®\x0019
®?ç ¥æ\x0018±\x0014iñÌ$2ÞIþm#ÃpÄ\x0007f,sa±ÂIBY|X1õ¦\x0006£üÛÆ&\x0014?Q\x0011y\x0010îãd\x0015¯ÕT±«\\x0012m®]´Á\x001få\x0001l¸Ñ»ËF\x000f!¯¸Äöóäß&6ïÀT£Ä 4T`¬\x0010Í\x000f9QÅë\x0014ØÊ¿hàèù!¥#«MÃ%T¬\x0011ÂD\x0017A+Ì=çß66©\x0008:6\x0015¨OcÐSÙdbk½n Ðõ!E©%×\x000cj°à¸]ÙÆéh:¡µj\x0004oqÖ4)+\x0015Ó\x0004GsP
Ð¶/úÒf\x0013Z«Ø\x0005×S²\x0000	Öø\x0002[(Új³e0Ûõ[ù¸íV;ðXßÜ\x001bói§=i\x00055´¦¤@\x001e\x0010¥&i£ÆçùbgÂ«ã¾Q\x000c\x001d*ª_i£2®\x0004ÿ\x0005ÙMê\x00159
Å¬­TZQ9æ¸S(øPò7ÎN£ª6\x0005\x000e>+gÑ"ÍûPð¬l,Y%7
\x0010\x001a©°*\x001a%"\x0016a8n\x000bå4¯ÙLß´QIÂ/Í×Ý<\x0012\x00143\x0012>OÝ\x0002,Ú[U\x0004ÎJ¢ù$»ë\x001b\x0006>B\x0010ò¥|&\x0010\x0014«"RÓ¨R<Èªæ¥X4Ä\x001c\x0018Ê\x0017«4\x001doÔx\x000e£úðÁþæ~I·\x001deigóÏ»?ÿïO×ËÇ	%&¥åZ\x000bþ|¶¦lFÎhIÈó£ÅÅ^jü0\x001eFÌf¥(dMpüåÂ\x001615HâeL?-HÆS÷\x0008vTRX\x0005ÇÝ\x0005.\x0017ØL2\x000faº\x0014ÒSyiþ§XÔÖÃëÛejcþx³3\x0019è\x001dxB2S\x0014ht\x0002\x000eñvì°m4¦¾>Y¤\x000eöç\x0017Ç=©@ýó¿ûpýØé;Iã/.Ó$\x0002I(úÉÓÕÍòîÏÿ\x0007t4 \x0004
q\x0001Å¨Û\x0000ÐÁ=tJÇ\ë\x0011)þôôxñò\x0019hÞ4öâéâìÉÍÝÕýÝÝãuùo9r_Ù0\x000eìòÃá\x001a,0´"ÂÇÃÚHÜC6\x0004ÂëíÕÀûÓðX\x0010#×{ÁQ89\x001a"÷
\x0010iy|ú"ðïEç9\x001dF5Q\x0018ã8r\x0017ÖÀ/âÓ¨ äÀÍ?.sX%#wuãÈ­M\x00039ÒBÈÄ¡q©FÂ0.¨z4\x0006®\x000cã\x0008¾|\x0017¸'6¿\x0014à°\x0004ê\x001fGP×Ò@\x0010yãÜÓÉÃ÷\x0013*ßÅæ \x0016¥a\x001cÞ¢??L\x0016hÈ¡
HÚæ0\x0012\x001aÐyHLT\x0012Gä\x0007ã{>ÌÕòÍò\x00017sõsPÏ0\x000eö$!\x0008V0¸\x000c¢½'1\x0006¾Äø\x0003¡¾a \x0018sÎ_&í|Îo\x0006¤	HHVÔ8\x0010ê\x0019\x00049\x0017´1ñÓDÖÎ $ROñÜq Ô\x00143ìDH68\x0008Ør@4iàÎ(\x0010î3\x0019v"¸# \x0015å²j!éÑØño;7qØ\\x001cZ¦\x0015UÀ¡\x0002«\\x001bÍhm'ÍÏËÔµ·\x001cøqpû¯'çR(
\x001f0mXÆ\x0007¬Ç_WA\x0019"5f\x000c\x0014°ú0\x0012\x000fFúYÒ¯U\x0018}Yùù

«¡Æ?$#mM\x0001ÉÆ\x001901}¤8ô#aH$LqÍ\x00018\x001fúHV¿/uóÌ@¯XÄáÑ¤|d\ßÑV´éhìàû\x000b6¼"á"C*OI6t±ØB\x001co9J¼/rø}Q\x0018"J&,8|u­¤cÑã¿\x0012ü\x001fé+Á¿tøW\x0002HBÆ¥-êI\x000f\x0015\x0019ãF¿#\x0019Ò¹\x0007\x0003$®X³¸n¯e[EøÑ/I$q7TÚá{vàë¤.eüDÞð£öãÍjóó%\\x000e%ª\x0008\x0017C Í\x0015.ã
Ú$ ]¡:òdÂ\x0019¬nQ¤$ßV\x001b?|øeyuÓqB\x0001áÃòîÍêæn\x0017\x0006N§1É\x001b\x00063m\x0007\x0001\x000ee¦ç\x0013\x0002þÊ^\x0001\x0017?\x001e¿\x001cB=Ñ$&Ï/D¨SE3ø¼§\x0004I¼\x001cOÝÀ$XDóy\x0006G"¡åcX»Rû£m$Ù\x0011\x001cJÂ ó`áZú:?Óf4\x0008{>ÃH°þ7[OÎN/G\x0006¿F$vüÇá\x0007\x0003IÀã	H\x0002928É÷Äñ_½¡(!Í§OW6¥\x00113Jd\x0014«üx\x0014\x001ai0\x0010ÅØ4c!¡¤{B±¹l	QÌ\x0004\x0014ò\x0006¢à¬[þ@&+\x001e\x0019tÞÌßGN )cx(\x0012)Î%\x000b7¡\x0008þ>ªÖM(q\x001b\x0002fµÒEÎfï\x0003P\x001cË\x0014c& ?6ôTDJ0#
\x0016/fñ\x0016d¹µJN@¡\x001eâa(
ó{ùªàd\x0015\x001fry\x0008MÀ©_a<Jh:èTPªÙ|*¸Þ2\x0006ª\x0012JSîÃòá²6î\x0013Ï#Ó\x0007ÒüµãQà@Õð·,Ö\x0012ÎrWæÇ¬ÆËÚT3ü-\x000bI\x0015°Mr¼ø\x0010Wqå¢n\x001c0éÇ_\x0015µ\x001aÃß2ÜZ\x0016+VQ\TúÈgºÆPnz\x0018\x0005#2j:\x0014ÃR\x001f÷¼C\x0019/k±:X\x000f7\x0010°ÈÎÄRD\x0003ÎÄC	ãM\x0015îÿ\x001fx(QÐ3ö8¯>qøÀoG¨	\x001fZ,\x0007r`çµÉ(¦<cï"[oÂ<ë%\x0017PpÆ\x0006Ý\x0013£É-.x¾'J¿'¨¸Ìð¯\x0003&AÈÂ
|ô4n\x0000Q!9\x001bâinû]Ø´J¡;¨\x0014¸Cµ²§h\x0013\x0008}Ë0ÅhÒ\x0013d
°,\x0013Ë²Án2ÌâqgP6V$Ãøñ>¡
\x0014T	)¨2ôKY6)ÑævdÈÉ¼'\x0003ÕÐûÛ\x000b~\x0007f¥Uù|à\x001a·ÏÜ79þí5Üú?îï>]½[Ý<|sêXë£ñ\x0018ÚÈ©\x00070kCáÒ\x0006j\x0018ï«dÝ?^½<öãéñÙ9üÁË£5PëïðäðF\x000bÎKØ\x0007§Ôg\x001ebí¥µ\x0013å0Ç÷sB9÷ÞÂ£Ö<Ø\x001e¼q1Ë\x0007$\x0017â4¤\x001ciühdZzÊ)m8LíH9\x0010ÓawDLv1~6©\x000böá8;ßtt2¶òXØ\x0012\x000c1åá§\x0001èiL¨ob29´ÊÓÎHï­ó\x0014íD\x0014¸j"²iø\x0006R0|¿½R,\x0002r	ÿ\x0004&ÊÞ·09OnxÀ5P\x0006à«3ÅíL\x0014Vkºáy&8SL+!ómÊ%mX×)Í4&Jê·0\x0005*- 0d»\x001aï,3\x0019;ñSt«É¥°p:§pHÎi_ilâ0W\x0003R\x0014r}L\x0012ðÉÄcÄá®&$>Wzu\x001ch\x0002¤<þ\x001b_vÃ9îÕÄ\x0014)zn O\x0017u9&3Í\x0018à\x0016&¼Öë\x001b®éÕÅ<Ú/1M»á\x001ckbÊåéÛ¥\x0015\x0014ÄÄß.
³ÂDÑ¹&¦Ø\x0004:E;L\x0010ÖÏd\x0012p®	4rEbú@LÅLQaâ}Â=Cm\x00123bºì\x0014\x0019(-a\x0002J\x0000:'?ñ>Q\x000c±)P¤7É\x0002\x0011É\x0016Y 'Ê'&¶0iEÚ.Ùs!¿» b\x0004Ä1Å& l{ã!a9.ñ8¶¤vF\x001c\lAÂlôZ­8zs:\x0014WMó\x000c8ÊØÂ\x000b\x000cùÍ\x0019\x001claÊãú&0Q+N\x000b\x0013Núç7W8$&ágáÜ0ÑÂ\x0004cÉ©K=&@\x0014E±ÃÝ43¡M@\l\x0010°c\x000e)Òäp<¤0ñã±F!\x0010-9Pàså¨Á¢böÆ§\x001d\x0013\x0016\x0015¦7\x001eöå.åXº¡¥°éÉMSs¼Âë»	X`ÂÞ4½7ãSæ#àtH·\x001bn\x00101¸ó»mï(é Q|½é³IlIâp,>}6~p~¤ä
g-H:\x000fM§$Ù\x0012V³\x000bÓ\x0004%þ¿´®\x0007ûn4\x0005tu\x000eè~?\©`MÇ¦³
i\x001f#é9m¨n
ß]îÄWJ¤/(\x001a±À]\x0011\x0014\x0006ó%H\x0010aÍ"¦º¿Ò\x0016±õ+kª	Èdùj¹\x0016çÓ<\x0004øWéC^µJ+2\x000e£\x0014\x000f\x001eX±\x000eâT{%]/Ûö\x0014cpÅÜT:YçxX±ä\x0013©ÖÅèßÍ;\x0014éóµ}=\x001f0¡\\x000c©\n¼ðå\x0015ÚÎKÊiÌ}G¶ÔFÙ|S°5ï\x0011I\x0007\x0016R\x0004(}C%K°uZ\x0000\x0018®ûUºîßÑÍ\x0002¦7éÍ÷ã5t±\x001aïÕQâåý¥ûò['Çùú\x001bäÞÞÞ<¤vù×yðìzõùæzu½³¸<àîÝ¤´Ï¥÷ ÷
×êº\x0000ìëÜ/ôüäø,õÎ¿\x0006êgG§?\x001d\x001f\x001eõ\x0017zw¨s&ôïF³¥7êSý»Qçå7ê,þ[P¿ûýöN\x000cY|>x±¼Í³}?}Z%êóåÃÃÍÛ»/»J8p	\x00175\x001dÄ(¨þTiÁkZÔ\x001d!\x000e^,2õâüü41/ÎÎ¿ü·\x0001´X¡Ç
i\x0018\x0007âº«]\x0013.íI
A\x0005cæÃåI?SxE?\x000b\x0019)³	¼jv´sò\x001aÌäãÏH^z.×\x0000{4X\x000c5iÊ\x000e\x0007=çmÐ"Åª§àâÚ¬ääx\T%¹#ÝÓíMéÿ\x0019y1h?Sx#ájn6\m\x0007&XÖ¤)uSh#\x0005»p×\\x001aAÚsótDä­\x0003Þ\x0013y±\x0004%ýæ
Óã\x0012·ö1/·rá^ö\x0019yó¤½I¼ÊçpýO\x001aZ&n\x0008*/4ÁÍÊR\x001eSno\x0008X1¦\x000e±ÄËÂ\x0001ÇÍÉå×j¼²p.\x0001ð*¡\x000e©í6%\x0002n¬çwLÄM\x0019%=åxA\x0015ç \x0004î6*óW\x0002ßÞhæ½\x0018O?ãq¹È+isÖP\x0019Ë÷VÔÅ(Sqñ2I!\x001e\x0006M¸!§\x0013¯·Ì[÷ïMã58Ú9ýåZ\x001cÒÝ\x0005CÇÑå×Ä\x0019iS@}ÊéJ¶Ç$»WÈ4#\x0019p­b»Ìú9EÁ\x0001Qég4¯ç<×NóT\x0003k\x0003©6§å²ÁbWú\x0019Í£<ñJOaKÇ§SõàQ¸W_ßßý¶L>\x0005®
í\x001b}
n\x000f°þãúq­«Ê\x001c+§DHU´p\x0003õùMÈ2nô5ø:Àø£!lÙ#neÓ¥£\x0019w\x0001æY_RÑBßàí¡8
§V¶³)CSPÒgÎo\x0007Ø\x0004uÉ8Q÷=dËuÇlh¦ÆrlÔi¬4À±Ípj\x001b{í\x0006\x001fôå:[Ø\x0002YOÞÆºàw$\x001cUý¶\x001bh\x001b¡è-DÊ¾He#\x001dÓõ¤mpËÕÕõÇ\x001ddTûÛJsrÏ´!¤R-\x0019NjÙ"·\x0008+¡¹ÃQÑð¨$Aæø¤ÔáÞ
g5wÉ(iø\x000cVp+ÃÈÓá¨R¹\x0011Npô\x001c>ª 	#\x0012N.ðGµ3^®Xn=8\x001dËC
êL¥¤²)87³÷)\x000c`£Òåïïrenë\x0017ÅÑ¥ùÐÐ\x0012Ì_Tpù¹·nwÊ\x0015º­l oYc\x0019M\x0012\ðEè\x0019®[âÝ\x0008õÕ¤³À²\x0004'©ØÛdîH8ªEmÃM$}?ÌÂW\x0018ÉúÔ¹\x0019Ø¸\x0004´ùàTz\x0000È&\x001dÕ9K\\x0004EpÖÏ\x0001Gmp&ú2=Bâðñtr":Ïï!Ì Dp¬n~\x000e\x0006ÇBÓh\x0018\x0011-\x0015«{L«¸#`\x000e8êFosê0wãRgé3\x001b\x000fhñv\x0006º±\x0002xð}\x0013e¯ùëâ}\x0013üE­Ã¸ô©ËÖ?Y6«\x0006Ú±Ô+f9?U4gÁ»JxWÍ§çí¡ \x0007¡\x0004e\x0016¤E­{'Ç¾ÖT¡Úï/ùº:µ»cÛw£øÃ§_?¼1Ý©\x0000ÿz\®>\x0001ÔÁíõÁéãÍÃC¦Þ¦££\x001e\x0018¬×¢*\x001bi%í\x001a6|Õ],NÏêàäèàôâøì\x000cGª÷¦;Õ¯¿ÿq×I\x001câwìöþg÷b¹ÚÝ¯&¨S\x0000+µ¸"Â\x0008\x001ef
§Z+þ4@îÅk<¹\x0017Ó\x001diØ5\x0017\x0005\x001fZ¸µi
0r%«\x0003U\x00084éOÕ
\x000c£¨rÑCÛiyC%xXAF1Ú\x0011VÝ2+5´q\x0015Ï9âÆ<þ\x0008°ø+ª&«Q\\x0014¦iâ
ÆDôbrþÆ\x0018k\9¯0+'ù¸p$+°ÛS·¹êYÂ£¸(<ÓÄ°Ç2\x0015Ç\x0002\x00148[¡6\x0004ì\x0008(nÂn£·\x0007*ÂWTÜ&\x0003Rm}ë§qì£\x0019\x0017Ï\x0003E°ÈÂK©É`4È¯
,¨C:0Pêt½@xðaòõ*aV.Ç`®\x0003f´,'ßÞ\x0004\x00062>WUà
ÐT\x0010`§+1]NpÍg*ùl\x0013c&-[ækFRL¢#ç®h6bÕg\x001b²Ù\x0017H/3»íF{þaºL\x0003qs£àç¾v¬>%S\x001b\x0004?ë#a&[\x0015R'?@·¢á$¼Ç\x0019c\x001c+§
ÁÜ\x0008¬®ÃSÍ:¬7§éDùÔ\x001c«K5ã±­'t7\x001f¥/ê4O¾°6²L\x000baº¡h¾Æc»nµ~¸Ä	7\x000b¦òìdýøõmü\x000e¤LÇ&ÍR\x0018\x0017KéqqÖP¾\x001c©	ì7á¦cö\x0003ÒÍ\x001f»Pà\x0014h\x000bÇ-¼IYj\x0017ËH\x000eñÍ¼´ãÿÑ»ç£û¯ç1ëÿ5\x0004}\x0007 ß<þñû*Ý\x0004\x001fÆGööÓÁùÍjys{{ý¸zÀOtµ¼¹ÛYå\x0019\x001d§¹®\x001fÌæ4e\x001cÙ$\x000fv±Étª?\x0001ïìùùÁùñéâøääèâô\x000c?Ù«gãgÛ]É5³px\x001c]§ÑÔ¸:·oh#\x000f3´
Üo|üævíÞÖÀ}ÜW¹séFÍmþ+¹/ûòïvÞ\x0001ïIzOlirÕkO´+ýÒ&ÔÝ\x0018ó_!øÄòß\x0002~à\x0013oÊ_\x0005þà\x0004èà\x001exþxýåÓNu)\x0014¥S\x0002\x0006£Ø
IaÛ:dÏ/þí¼W\x000ftþõ9Ê³ÿ_¯\x001dw7§?Å*hELÚÔnnþ÷\x000føã9ÿmÿ~vÈþb«·÷¿?ÄÎ÷?Y\x001eÞ\Þüù\x001f«]­Pik Ì¡\x0019ãí¨8ÑYò7¬àÅÁéñSla\x0018BBÛ\x000bÿ»HníÇxÙ¹ÏÞ]¸¹+] W÷·;p¹\x0008õ$(Åq\x0005¬{¢x-Xp\x001bs9^\x001c¿¤Æg¯N\x0006ñJ&2-¸\x0007Ø)Ü\x0000K\x0016\åêV¿Qd¹×§õÌp\x001c0ß¥ @²ÔÒ®Ãïj\x001cÙýoï¾è\x001cç\x001dø¸|H}<\x000f\x0007Õûëf¸Swdzx¯ä½à.\x000cî°uràøÅëÅYêß9;Xþðêø\x000c.\¿\x0010^#òï\x0017Ña;ý|wrå>ÝÛ$ß·\x001f\x000e\x000fn\x0001òüþñöþñay·³cË\x001fÉÁp1\x000f­Éº¶bSs\x001d¯ù\x0011®à\x0013`<uqòêâlñrG£Ö\x001armÃ`t<ÅãRÊ<eOûÒF\W÷´\x0011¾»½§¥Û$dþyÿøöv¹ºÞ¥l\x000c!\x000f\x001eÒBõNÊh¬Ùª\x000eí¯.,Nú5S\x0007#§\x000eaxÇW\x0003ã(¸2>7\x0000\x0001©²8r5ç\x0010\x000e Rk\x0016\x001a´t zbk8#Öö5G©´æ`u\x0018\x000e\x0005\x0004gÄqa3\x0005¹\x0001¤.Ùl9\x0010®ê\x001b\x0006âsaP:\x0011A#\x0015R\x0011\x0002ÀÇ\x001b}"\x0014e\x001f\x0006=ø>_\x0011\x000chç\x0003	¼jc/L\x0013\x0007U\x0012\x000e<\x0010çò\x0003Õ´IBá\x000eD~2¶çªî\x0007\x0001Ùr²åfè%±y*\x0016"\x0006\x0012yÊ\x001aZwU\x0004jô«)bn\x0018õyM' d£\x001e(ë\x0005\x0008b¼ q?ÿ(¿\x000cD\x0001ãMd\x00148\x0001¾Á§Êù¢bÒ©P@aà\x0007\x0012ÙÈ\x0005\x0014\x0010't(¥ud·ä\x001aI®
6s@@9YO\x001d4f´<YG\x0006?dE\x001bÖ
\x0012m>2ÊxÉ\x0006$oäÍ@­\x0003&+\x001dLØyzÉ4Ù\x001dgÆâþ¿.ßVáY2§\x001f\x000ep`ÅòfàQéäÔ\x000enR¥`·ñ®C]Ç=}vS+\x0016Ç»,\x000e\x001dïøk£s^\x001cZÚ,.ÊäD°«(®
vÿv?d\x0008ÝÇ?®?¯~M\x00057iÅ\x0019NàL¾¾¹ûó?w9!Î^\x0012d¡á ðM\x001d](áêÄ+ø¯\x0001¥ß÷øõóê÷ðKç3þ¸üp½|L\x0007õz\x0005þNs\x0019s&&wW
Mõå`LðÎ#íëE?.^\x001c-.Ò!½>\x0005¿ÿ>\x000cË»+ÄÂávJ?\x001c¼ºÁB¤]\x0011x\x001bBL­Q¸é<JÆ«tð$\x0011-Ü°ê\x0005¬vÀê\x000fÄ¯apbWTÃaPS$\x0016¸Öé:¥\x0015§\x000c\x001b\x001bd3Ëû[¹úèëhÈO×«=÷\x0006ô¤æ=%p¡¹\x0008Vó\x001aãf\x000câ§£S¼8}¼\x000b\\x0019Üq:%?­\x000eËæ\x0005&¾\x0013ñ¿¾{ß­íº}?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=a\x001c¡)	íá_>ÿöÿzyøú\x0005\x001blb¸\x0006*\x000c¥*¨k	Xv\x001d}2¤÷,PÒ\x001fti.ÿåó\x001f/o/?¼½<$?ÞÜý?·7××K\x0015èè¦\x0011Ô%\x0017I1ª×\x0014÷}"
\x0007}í¤£÷&Ré}*e¤z(2\x001eH)\x0000\x0005\x0007yí £×6P\x0013VJ\x0004ÅÊ\x00165
ïéã2a?ÒÑf\x001bitÈCÃÃòFÌ§
¤4;#©\x001d?~üW¹nRíTE\x001dc³Ô%¹¿HZ\x0008On'\x001d\x0015%4~ýa!\x0013©Ç²ôõS¼\x0013I\x000b\x0001Êí¤£§¼FRªöq\x000eBiiM=}½\x0014S´âÜ\ö©°ùëkgÔº\x001dQ©+©\x000bÕø¤3¨Î\x000cE±\x0011ÕÄ\x0018R&Tã7þú÷ß~þuöùû\x001e'W¾¼Pkê)T\x000cÍ27i;,
¨:è¤É\x001c¿¾PGwêõ\x0005Î°¼½\x001dÚTWÐN\x000b¤Zh¤!«nx6!Ñ:²ªX`\x0006{Òßï[×®½\x0016§ÎÓÚ\x001a²¬:TvOÚmm¥MJ\x0003­v8\%Ñ\x001aÝ\x0013uZñÕªÒÓ\x0014nZàÆüá¦5{ÂK%\x001aaIØ\x001cNÔ;Ä*Rgsd-Jèv+Xk¢u6xÄ¥ÅI±´gUzg¸Êîi\x000f¸±\x001b\x0017\x0000A°Ê`\x0006âzÔ²#n!¯»\x0007.58vãOå±n¨RÑpi÷´^ÜöØ\x000b±¶5	\x0016U\x000ctI7\x0002k\x0006á¨\x001bkÅ¥^Èn\;h".NûÒé Å@pÜÕq'âÕõ>­.
@J^]Þ¹Anß\x000cßÿò÷?ÿõkáxKÅßÈûòüø7Vÿ½xùy
¸ÅBjM{Øó\x0015Ì\x0004\x0017È iéæ\)ÿ\x001bÑoo®þ-I\x0001_Ü¾Y÷\x001b$g¼Ço\x0010\x0003\x001d²q.\x000c]\x0007Ão`@ñNÑÿÿü\x0006é¶Ë7P\x001cµÙ0
¿\x0014µéÙ+[ç/ðô\x0017ûýëÿË¼yýömÝv÷(b(\x0012±ÃÜàH\x001c¢C¤{\x000c\x001a7w>\x001dÝê\x0005å(\x0015ÒB)5»Hv>@\x0001##´ÇÃË\x0016ÈQØÞ´.=QDH¼\x0008¹´R:^ÊCYíVÊQ¸ÞDIµ¢N`±ð*}pO×5/Û·\x0016ÊQÞDéÏ!/e2Âq)É\x0012àRî¶+GÑy\x0003$9H·\x001e1ò¢\x000fNâö 7Gï\x0011-£X·Ò«ô\x001cC
R:\x001d,Sî¶0l=f@Ói\x0008Óq\x001b¼£¼\x000bv¯µ\x00044-(·âh1\x0003\x0018(ãåÅÜëOâOo\x0002tÆÆpføäVóÆtÇóÆ'1ýËëóÏs®çÓã¯_ï¿½{yþöóó·ï+|æPºÎºôÃü¶\x0008ë¤â%
E\x000fÇ\x001cì§«w\x001f.>½»½ùôææÓÔjÅ<rD\x001dÌ^¦ñ\x0010\x0019[±\x0012r>RA\x001c÷G\x001dÈ#·Ô³Ìá<yP@\x0005COÈt5\x001fÊ7wF\x001e\x0019ÖUöd¹¢á\x0017Xò70\x001bÚ\x0019ZHut\x001bw0Ìl3³³
`
ç\x000cÌ2 B£×ôväIb¡Ù9Ú\x001añîHÉ;\x0007ô\x000c\x000cú¯í@\x001e7t áX\x000b_ÆJÌÂR -
µ-Ð¿(õ­ºú°ÏðkD¾|zº_µ#$[\x0011\x0004n\x000eD\x0015Î\x001a¶on\x0016\x0015\x001b\x000e?DÒ«ëëeBm\x001eþü3kñ\x0012óù·û_V¸¸tî\x0001`P!í[
©\x001a9þÌL*à\x000f/~Xv\x001a\x0005é47¾TÆPk\x0010Ú¤\x0011NX\x000c	%pÔ*´Nóâ
¤ÆÓË\x0008\x00187¨ä&\x0013DûNû[ÖT&\x000b\x0010Aùâ\x001dAbPy*EÓ\x0000:M7jÒÆDÒa\x000eÖ@jRw1ª\x001dI§ÙðÒ?]n@U:Mb¨!Ð\x000bCüøI+rj{*oß:é"lA\x0015N'aìè¦Ë\x000cb'cj7G\x0003ð\x0015¨ðâ~}Vs±íO+ß\x0019vo	q\x001b¨!ØòJå¡;þtÿÓñGÆpdòW\x0013\x000e\x0012E)LA=\x0008\x0008ã>"Bï_·Ö\x0013LýjBÔ ²tÁ¨$\x0011bÃ!­¡Ùi	Gvs5`tàdâª\x0019,óD@¬¼â\x001c:zjÖ\x0013\x000cæZB/\x000cé8i¾!ððFÓW£±èzÀ\NOZ\x0012X\x0000âxÙÐzÂQ\¿~	]\x001a<\x001cWÐ+z)öÆ\x001a>ÈâxµÐjÀ\x0001_¿ÖcølÅæùÁÖ\x0008®fsîxÖq=âØp7,"Uïã*j,¿J«3Pböe¢\x0003qZ(:·©&\x0010Û\x0005EB´"§äq¿²\x001eq|Z\x0008Þ\x0016\x0004Æ\x0006\x0010u6âøg5"+fv º0ÌFÂÉð\x0002ïgHè\x0004\x0017\x0001Úù÷\x000eB\x00125ìØApE¥7(>7ìÄ Ðm2ÿ]ÿ<0ç\x000fußÿþò<£=ùz$\x0002¿z\x0010ü\x0017\x000c]j\x0016³ë7¨¿ÿûíÍâHZù'ñç?¿üÍÔ÷ØÏ\x000f/k\x0003Äà(\x0019.©\x0018)^\x000eEÈÃù\x001bìçËÛ!ÖZ*è-°(NhÂÂr@7Aç7]\x0006\x0004\x0000\x000c\x0002Ï¹è\x0002ØÄåÝ9ÝQÇ fX-A\x0005q\x0018NÏ^¥°(jiÁ\x0002M£
\x001dêPñ£ÓÎñ-ÏÍ?Ä7qQ¬Òö\x0019\x0001\x000bDõ²COÚð\x0019uR/\x0001ìmÝöM\\x0014¢´íúúÆãzIAuâq×s¢\x0001o [¹²ßo\x00023.Í`\x0002è¡\x0011GYÞ`aÖY5±·o\x0001Ã×\x0011Á·33ïf¾wÉjJZúÁhêÇ}j¶?icc¨\x001cÔÊP6Îø (A+»ø\x0014³?.ªÎû±eR(I¡T¹äL£SäLq(1%eÁÍÝ9uÉ©ûVÔR¢Cj#È¬\x000c>Þ\x0005Ô ®\x0003Ô`ß Jw^e\x0006Ý0\x0004uRZJ¿\x0007)MHåM*zPã~ä
U$×\x0006TÅ"ÌæQ«]*{¶i¼jø¤4\x000f\x001e2	&þ\x0005FUs¶h5©\x0018|Q|þõìâË×Ç§\x0015[U" mUÓ¢©üßòVå\x001d3Ñ?]¼}{wyu}\x0017J^èå5á\¥§Qm%ÆB~
Ò-\x001a«F^Uòª^^¯ÒÈt|IR¸ÔC\x0017<¼$9\x000fÐÃ«K^ÝÉ\x000bÑ­S
\x0007g{&\x0015o)\¥*íl®÷`\x0014Di\x0014D%ÁÁ. >IÀ\x0014Yê\x0018Ií´\x001fd}Þz\x000f\x0012.Í¼\x0011=Eè8V\x000eOðô\x0000W\x0007Nö8Ôº¤B3e,ôX\x0010\(g_Ázx«
,»w°\x0013ÇUñ
\x001c\x0005°¼#DØ\x000bØTÀ¦wG(uN\x001b\x0002\x0004[4ÅyèØä¢ckäµ\x0015¯íÞÁú\x0005#°¢í+ig;E{h]EëziÏq\x001cT(åÕ¶¯ð°×òú
Øw\x00035\x00130×@«$o\x00067ûîÔC\x001b*ÚÐKr³i3@(?8\x0000ãkN\x0002¯Cí\x0000Ê_@¯¿P1à¡\x0015F-BêÍWkÞÀv'\x000c¿ná\x001d½XÈ\x0018Q\x0003Q\`\x0017x¯õ­ã³^w¡MR/ÈkÎÉq\x001d*Â/\x0006¿¼»^w¡\x0005iôa°\x000eT6c±\x0004õÙÚ\x001eàÊ]@¯»Ð¤\x001e\x0015`B­ÖÜ;"fë\x0012zp+o\x0001½Þ"Æ\x0007çTüC0R\x0017¼&ÍH\^±×þ­ü\x0005ôú\x000b\x001dÃ\x0007ÉU\x0016·Æ\x0000ìéîÚ;\x0001«Ê ©^¦µCQ¶\x0001X\x001a\x000eµÉÀa»E³ã\x001b§\x0015¥l.6\x0013ý\x001cÿû×5Ù¨\x001b\x001aM
åp<7íAÍq?\x0008ö\x0011½A¡Ç»Ó¸ªÄUÝ¸8Ç\x0013±¥øÌ\x0000¹í\x0018æ,Z\x0017±)M/1NÄ	*7J§Ö=\x001bw\x0019÷î	·Û\x001a»Øu\x0013KT?1\x000bçÔ/\x000f|'Rr6­Ü\x0004,Ý8_êFùÒ÷÷/ë=,gx§OÙy\x001c²È9ÙFÎC~çýÅÕíÕ±T\x001b'LÝ(aÚJÓ\x0000"*\x000cÔ	Ô\x001d°\x000býxnw-«.Yu\x0017+\Û\x0007-PªD\x001f¶ílõH;«)YM7+\x001f174ú\x0013+·JËÙ*vV[²Ú>V EÅ\x0006"ÊçpzOÁ¬ñjçt%§ëã:k\x0010Ä ÒÓ±2Ò0ë¬\x0012I;«/Y}\x001f«XúzÏ%½ a`§ ¯=M¬¡d
¬¬ð"£ïÅçaLÒÜÖ¿\x001c·°\x0016Y~7Îò¯Åj\x0018ê5V\x000eÅõüB¶\x0001nùºÓÄZ»>?\x0000oLy~,\x001eL¶\x0015\x000eú\x0003~9qÓf\x0003þôóã·Ú\x000eà\x000f:·\x0002ïZ3¦h'ð¦=ñ²z#ãfè%Æþ<Ú\x000fRñu\x0007¤äÞs3+¤ÔÀ<m¥-âog×÷¯Ø'ÿm³\x0005É\x0007Í@
ì!Qß&Xv¶"ì\x001d¶È/	\x0007\x0016¬P²B'+d\x0003¦\x0004jFVjÁ-_sÖ±Â\x0015FA\x000c6D¶U\x000fªî°o©åC\x0008NSqã.'ù/Ï¨m$þÅcÛ\x0000Fw\x0006\x001eÛÐ+øÑ'^ÏP\x0005.ñr\x0012$Z½xuÉ«»y}ÒpD\x0007I\x001e\x0002\x001bb7ØãÏÀëymÉkÿyyAÌBüAñÈúéùõ¯\x000f_\x001f_VÝÆòÃµAhàÍ\x000bby3Ü}º¹ûéòÃÕíiR(I¡\x0014R
¿­úsVË\x0010|5Ùb¨fPUª.PT»¥Gkí©aßðìF\R}$É¸TT
Kzñôô,íçÇøÇ×§UÖ\x0004ö
ØKèøÅZZ.¯ñsßÿâúú2ÙÚÏWñw×Gl-óêW÷òj+\x0002@¡\x0014ýÀky½ó\x000c=¼¶äµ\x001bxÎæÀ\x001bh}­Ê¸s·\x001e\_âún\MÊ\x0011\x0017åeÜÙçÔ\x0016\)Æ\x0011\x0018L×ÇûoßîesûÃãï«Lm<_@«\x001b\x0017Z\x0000M.»Á±®3¼¹xÇæö«÷Ç\\x0018G
b8m¼\x001bw­ÍbÃ0¯7ÒC«JZÕK«l®¶¶ì\x0018È\y7\x001b÷àê\x0012Wwãz~\x001aêÚ\x000cñjö\x0010ó]\x000b-¼bìw¬Òt¨<ôõ\x000câß±×sÇ5VäQ\x0018Æµ7n¶\x0018Ã³\x000féÿÑIX(a¡\x001bV°ì\x0010V\x0007Ú\x000c9ý\x0001öhP³V´ªû0A\x0005"imÁ3ílWÿjÚpÕFx9¦ÑÔî7ÏßÎ~?XÓJ  FÚ P«b¸I\x0006®\x001cÓp¼¿o+xõéì§øå®\x0002æ5÷\x0016p­\x0003×ç\x0006\x0007¤\x0016g5K´j{Bae\x001d¸±\x0019\x00062ÃO÷_\x001eÎ\x0006´³\x001f_\x001e\x001f¾®òrs¹\x001aõ3\E\x0006jVBëãõÅÛË³á§g?ÞÅ_àÃÝ¬ÆB
âío\x000f¿?~MÏh
\x000cÁq\x001eÿÝ2\x0018.\x000bÐz¶\x000eòí\x001f/ß_}H\x000fiy\x0017k¶YÖÌýÐ¸3È}\x0004ëó[°áw\x0013ëÌÿhöã·)?Ê×ºpkí²<®Çéôªf¸,ÇÌ\x0015\x001b\)	·<À\x0006Ï£ÒÕ¶~#°ïü ZqÝ¤Z¡Hµ\x0002\x001fdd\x0005¿²Ù(%+®I²b\x0019Ó¹³ÃdÒO\x000f¥\x0010È\x001aL\x001cèçèÅ]y.p|\B4·°.Kõ\x0015®ät=ÁYöwv,Éïp]¡Í6\x00124ta¤ä\x0000ß%P\x0015ÕrIËl3N+©¬?}Ï·wÑ£3*\x0016É§ê¼xÂl..9¯¼
Õ?góû_fç|xýýþ+"*7 \x0010ÿåÓýë_\x001f\x001fph5ÂE+;zï4©1BÅ¨Á
ñ¹
\x0010\x000eµÿòéâ.¦bÄðÇË»÷\x0017\x001f\x0016t_j¼ñµx2!^H·gÐ©
ª\x001c¨¸\x0005o<Wb%\x001eö[û\x0007:Å\\x0011O§özÄ+&¬mÁ\x001b)¼¬Å\x001b \x0012Ð)Ñ¡p£[4;mÂ\x001b\x000f»XÕRÃ\x0004\x0016\x000fÁ¦ì¼V1e¼\x0011¯>¿\x0005o<áb%Ðé¡#âYZë"Ng\x000e9îMxã±\x0016ëðâ¥)Õ<D<)Saª\x001aff&º¢§e\x0013ÝxÅJ:jâ<j³&W\x0012×\x000e\x0014ï<}&6ÑÇW¬ü´àÎÓ¹ çôa©Ç4Â)ØåXLGV¬=\x0017tïxN¥H\x000cùØè\x0015»l¼XÂZ>\x0003éE\x0018\x000f\x0006ÝÛÐ¬|0\x000ee\x0001ø&s4Vò9É>
Sýlö¡õÂïâ4&úó«ù\x0004e)}\x001aï|éÚÝÅ\x0014ê-|c¥\x0016¯F|Ê¦Ç\x001ctº¼Tnï;ÖoX?M|ØR\x000f¼~ü}µÜ%fÈ`¬>\x001f\x000e\x0003½t~ã%Ö$>iØ¯Y½Ï÷vYvØfäKÓÿ<6`\x0018Å|c>½qòO÷¹ï0äÙ4y\x000e\x000fì×ÙWÛËP\x0012\x0006\x0006ÿ»}\x000fêôä=jSÑ'Ö>1úÜ@ùE/º\x0017Nµ{ºýåõekw\x0004M[©dÊAøR\x0005Cý<\x0004äD6ìuõ3Ç\x0003'Û]_Üýpw»4(±\x0006£x¾	\x000c$n6\x0004ÓÞÝ ë\x0012ÇkpÐ3v¥\x0015"ù\x00160aBÒ`Ê1óÆvS3\x0007¢\x0015bø&0\x001cs&Okðé¥\x001aPÓ\x0011=h$÷QôÞºÇhx¢\x00164\x0004÷\x0018ð\x0015j|ý`\x0014··\x0005ÞcÊës+\x0013XH©Ù\x00086w.×qßdðéõ×h\x0006ë\x000b(¬³¨0%e\x0013&Ý´½\x0010úHÀþéîÝåJº±pô::)n;6^\x0010\x001c`¤£\x0017|T9\x000b3[­\x0003o,\x0012½\x0012ÏJô\x0019\x0016\x000fu@Ï&
\x0005W16ÖGÜB\x0003Þè¦½\x0012\x000f°Ð,­.UJ+\x0003é
5Mt£öZ:î°ó)\x0017\x0002&ðiê
ÊÖË}¾íXM{\x001d\x001e\x000e8µôm±¬,á)zgx;í¼ÑMv-ãùãÖ\x0007j\x000fWF+¯ø`\x001c»h7àe½WâHúR¸x&É\x0013ÆÅ³¿mð»¬ÞTÂ{íÇ\x0015©»\x001e\x000f®à`Xéäôñà]ÆT¯{%Å'R.@)w°+»|ÝÉ]v5¥»D<º\x0012¯=iùRI³B\x0005Ò#wÙ\x0006¾ø\x0011d]Fñäo­Ã7\þ¼)B|pì®ÓÀ7¾k¯6Ì*évE>ì;Wd-Ù\x0016\x001f`ï;¾k¯å:©ÖyÐÍA\x0001\x0000E\x00051\x0006=ëià\x001bßµWóAÒD>Ïõ\x000fèø\x000eY³=øÆwíµ|BÓös¤}\x001añ¤`ë'Ý\x0016\x001bðÆNÖ-\x0001R]däÃAmÉµÉ@YZ-\x001f;àMÔ0×âÅ5K7m|N½\x001d\x0011Ï±çõ>ìrzñ\x0006:3Î"tz\x0005d¾@2çµÜåób2\x001azfãèy*®äL£4õ³G2)
|ñAuF%Q
ê­ÑéåYáÓ\x0001YèÞv9½ø	=Ö\x0019Û£õ\x000b
iÐºX¶.Òmø¾÷êÏßþlænlOñJùæùõáÛ·Ã,7gS¦G\x0006zÊ@5\x0018JHá\x001bð2#Þ-ßÜÜ]~ú´\x000et<\x001e£	4?§Å
\x0014\x0017#(u"è±´w+èx:F\x000bhô)&q\x0006ÆS)\x000b\x000f¢ñÞs<\x001bc=gS©ÙÇ}(PM\x000c¬½¦//8\x0012Z·ÇE·¢º¡Ï	ñ¡÷1V\x0010\x001dAÇ3<Z@£\x0011÷6¿,¤[¼4\x0011\x0007_\x0016ü\x0011Ø
:áÑ\x0002ªôô4-L\x001aN\x0016Aä'8qì«\x00154åÉË4ù?úËÓo÷ÿ3Ì[RäüòÛ\x0003ÉG\x001fKÎ\x0005\x001cù*\x000f/ÖÒ×T\x0016=BsùöË\x0012Ò5èÄ¶F»D'\x001fR\x0001Ï@ª(*ß\x001bubK\x001bP\x001a$öÒcH³Q#ª\x000fü\x0016+ÜoI'Ö´Ô
âdN©jVi£¡EµÇÞLQ'ö´	&DÔ¡º,r*{0ûG¦fÎ9máôÔ­\x00109c|\©¶Fñ>=wlF\x0018Ô\x0016Ô\x0018*§#åq3&¡,¤òñÌm>Rßþû/¿E3õòð:È÷Hù8\x0005\x000f8( ]8è½Å\x001awbÞ^Þ-éöÔ3æi\x001d öI\x001d+\x0002C.W¥ª¤èÅ¹	qÆ,­Ct¼+ÃðÐA9\x0017ÒØÖ\x0002%¸wB±G+\x0011%],C\x0000~¾\x0005ôb"¡6'6ãjÂ\x00193´ÐÐÄQ\x001cªrâJ§¼.Ê\x000eîög,ÐJDC+\x0018¸H\x0004;}y	OøÕx3Vg\x001d\x001eh~<õq\x0005uºü\x0002=¸Åâ¥Ö\x0010Ç3ØÖ"âkez¬t6PÁ'\x0001
µ×.\x001c½-4\x0000
6N\x0007~\x0011^Ñ.4G³÷§\x0011Íøûo¯s\x0016ûÝÃËÏÏ¯OÏ_O8\x0016ÊÄOÑ8yh¹ÀK/yë`Ý}Þ]ÞF¿r}³ÐÖR\x0013LözBMå\x0005R\x0004zA\x0001½9b
\x0000G\x0006{5 t\x001eGT¦2\x0018\x000f^/^\x001få2½pd¯×\x0013J¾ã\x0004êN!}dkõ|5!¬áZD\x001bÐÕé\x0018\x0003Ac^	t/(\x0015[7!,âzÄ\x0018Ö¦<AÀjúA8/"Ra©\x0016Òé½Vqd\x0011×#Z¤}ÀqÊ\x0011\x0013 8.oâ\x001b\x0019Äõ|Þ\x001bâuÅ&íWi
\x0006TG\J\x000bàä¹u5¡\x0017VHnO \x0010åpËÆ¶(º\x0011\x00068V½yñ«ÿ\x001fÿùðeÎd¿ýíþõ÷\x0013¥s:\x0017)O\x0019
O\x0013Ô_ÃÇEÀ·¼¸{¹\;WàìõJ<,\x0019z:"¥jÔaJ/^\x0011ïh\x001aµ\x0001od­Wâ	Y£\x0007<7­õÉh)å1Ü72Õ«ñtRà«\x0017|R\x0013x.©\x0013ÄÕsòÈ	iÀ\x001bÅÕkñ¢§\x001bÊ"\x0007º*'øÛ\x001aw$UÖ@7r"képÈTHt3øÊÒÕN¢Û@\x0007/ÏðXÛÔF|ýüúøíìýýßÎ®ïÿzú\x0019'(=\x0016¦'k\x001cÛ*\x0015/)ë2ÓÐ?5\x0012_ßÜ]}:{ñog×\x0017?
\x001a¸?K£\x000fýñ\x0007oâ\x000fþ=ýâ\x001eg·÷¿?ýå=T
(ñ\x0010|"G{(Ïwú0sS¹8û	e=În/®Þß|øá4¦*1U;&Dwbè¶Y!ÂÛÃ\x0007ëæ
=1u©;0ã©!Ì¥)2ablÂ\x000cvÕ´%¦íÀ&!DL\x0013Ð\x001fb\x0019h\x000cµ\x001dßNg|`3¥+)]\x000f¥LMRÌ'Å7\x0014´n6ÑØLéKJßA	Iê-\x0008TïTQ\x001b¦[j¼[ï±1CI\x0019z6¦Lb\x0012Aà\x0010ÒÔ4Ä´>Ìµb¶b¦	.Ù\x001aA;'êÿº@2eÁãrj`N¿99\x001döH¦1ié³k®§äW~æÎÚ\x000cY\x0019#Ùaö)Ô6½ÐÆ°ÃxJOø¹.ÃfLSa\x000eÌ\x0000Tæ\x0010Ï
$Ù¸FsBÔé\x001d¬¦ì±j¸ü'ã.ÙU
sË\x0001v0H²2²Çnê4´ãYq¯ÚB	ÎìÍ5\x001f4cVvSö\x0018Îè+\x001dåÁ£w÷äÒ]¦{C^©ÇñÖu[Â \x0010sûðûßOEtÎ\x0002gWt°6Â>{¼g\x001c«\x0012\x001aÄan/ßÿûiV(Y¡Õz*\x001e	(>\x001f\x0011´¨ªPÚÆªJVÕÇê\x0014ÕfÇuÍ²ôÁòÂ\x001e+wh5%¬é\í\x0012\x000cöC%V)i\x0013hq´P¶Õ¬¶ÕxAUÑÁ86TqÃ:Jdi©Õ-6Àº\x0012ÖuÂ¤ÑýxáX½0ÌzLå Õ¬¾Õ:Î\x0004\x001b¯Óp\x0008k$ÅÍ\x001aÃ7À\x00126tÂ*|\\x001c`H¢¾\x0011VsR\x0018ç\x0013ì\x0002+EecE\x001f­ñl\x000cpâvH\x0007\x000c»1öh­c\x0003mí\x0011ú\Ñó°¸i\x0003­-°»öX[I\x0003må\x0013dS@!LÊ½\x0018ü\x000fK\x000bAÎNáX\x0011}\x0003¬®`u\x0017¬ÂÎÉÛ:céÕ\x000ffãeÜN^AV^Aö¹\x0005%|Ê7FZT#Nkë¤¤«	s±k\x000fmå\x0017dcËH;Á\x0005C%`--­Ç=Z`+¿ û\x001c\x0003\x0008â\x000féZòF@
3ÎLmeâ\x000e\x0010U?\x0018´;_¿\x000fZq_¢ÕÉà\x00008;å´Rl\x000eP\x00163åüôÌÛÖíÍÝçA\x001cîómR³:Í	%'tp`Ò­5rF·ë\x001dG1+:Ý­\x001d º\x0004Õ=\x000b:\x0008:GJ£h*©Ò»H)f\x001e\;(mIi»(}þì,£¤æÕÔsÉ¾\x000eN_rú.Î@ nxÀV\x0004
¼=çºÚAs\x001cÎè$Ma\x000eçH
Ã¤ôéµÞåÓËê$É£d%÷¶Dï	T\x0003\x001f\x001f\x0014¦!vÏçÉ$c?\x000c&iÇ\x0005¼
\x000e[Àº4ÿ	Ï\x0014Bzì\x001aÚÂË¢Ù¢è&É ¿{¹ÿúËªw\x0013\x0018²+ÎbýkàKK w\x0013¡f\x0008ï.ÏÞÝ^|øaù¥$£A\x0006Mh@\x0012èÞ¹ôÇ\x0001
Gf%´OÝ\x0000¦J0Õ¶f6	u9kYFL	îOó6\x0019sÞ@¦K2ÝB¦&)g½§ãÚ\x001cÔ\x0016îäL©h\x000b)ÑLÓ¢Å (y\x0017kX¾Iñx\x0003ê\x00133&¦Ìd¶L\x000cý	éépÈ\x000e\x0016HRÏ;\x0008Û\x0016Íh®mÑ<52;Uy¼j»C´ ù\x0012Í·mµ@À	¾æBð\x000fçLb¦\x0005,`¡iÍBZiÍ¤ä+­\x0014ç&G\x0003ÙÁÝ\x000e¶V4¡)I\x0017¸hæp5\x001f©g$}ZØj?Ðæ\x0008¤ôµÃÜP*ªÄe£°ÊßôEeå\x0008d'Ðô=\x0003×£*Vqà¶aUÆV6Y[c4U®Eßé¨BQ	C2\x0003ÑwÎ\x0005x
lµmæ6\x0000\x0015 ºaJ&EÉTß\x0019ÿòL\x000fu\x000bZene½µ'7×bV?;Ï\x0017Ñ\x0016°ÊØÊ6k\x001b8\x0007âb`\x0014dÓ©!ia«¬­l2·Æ\x0008ê°p\x0016-h«¤\x0000
ülúPY5h³jî\x0010t(sN_Ô÷´væé¸¬\x000e Ûì\x0017ç´fÒâ|,\x00086ifÊv@íð@}\x0000\x000e\x0013¯T1'\x0002IXx«ì4ßÖÂVí5hÛkÞ 3àøm ð)p3¥\x0015
dªÚjªm«áíp£h|2\x001bCoS^üRË\x0013)×W>p\x000c\x000e\x0013fû6§Ú×dCÆÑ4"ÆhRO¡¸8Ü_ âjÓÖúO÷#§zßäìå9û{Ë=yø$Á¦.ÌÔ[¯ÂÓ¬^yøAwÄ\x0019\x0015Ï¿ÿ|\x0010oõòPk®\x0004> ³19ßéq&ÅÍû7+0¡Ä\x000eL|"\x0001GA*7Ãï¬óep&¥ß\x0001ªJPÕ³Ñ¡Ñr\x0002+¿*y¸´êú×\x000eNSr\x001eN7\x001c%PmRó¸\x000ekgv\x0000µ%¨í\x0001\x0015\x0014VËâ\x001d
ùF;wÙn\x0007u%¨ë\x0001
Þqâ×\x001ej´\x0015U$ú;øÆ=@C	\x001a:@\x001du$£X\x0014\x001aÆ»\x0007úsUí ²¶M=ÆÉ\x000bHãg"ñ$»\x0011ÿ\x0011R¯ñnF\§\x0003´:L²ç4yy¸\x000c\x001bÃé=åÙ;?ÓqÑN
ÕBÏ\x0006e²½J¦â\x001eå8ÒÍèÝ®\x0007ýYÚ/½ÁfªOK¼Þ¼¼>Ö.$·9TszCåH0\x0008|\x000fOxÁ\x001e+îÈÅ^onï®	Bgp(Áa\x000bx¼EÃÀ­ãÝ0=C\x00008H¯º\x0012äL.z\x0003·*¹ÕFnºs0-FÉ0p@\x001fkak\x0007×%¸Þ\x0002\x001el*\x0006\x000cñ*é)K\x0000\x0010\x001c¯øÑFÚfnSrM;\\x000eÉdÂÖ	Û¤\x0019-}TZ¨ÛÜv\x0003·?ÔYëøÇ4$\x0000¤\x000c\x000eÇ\x0006\x001bµ»\x0012ÜmYð\x0018QM³\x000e@ýÌ \x0003ï\x00135ÛÀíKn¿éd
ÔO&½!\x000c
ådRæ:CúÁC	\x001e6L\x0012¥
B\x0005\x0016\x0019ÛCÓNúXaV3xQLÎGl!ñ\x0011C¼Ê\x0019:êÊ¥8ZZØN^»ÍM~3M(M]\x0010¼¸É-Ul\x0005qL8±¼òrãtXVBà"JCü=s\x001f+kç®ü¦Üâ8}zræ\x0015\x0007ZqÍ5óÑ¾\x001fSÃh&¯\x001c§Üä9½d\x0018ÿ]IÒ?îrÏ\x001d3áè¸¦vòÊuþÔ½Í\7ïù*ù\x0004ipÇ·Õ*EeQYÆ\x000fMÝMY¶#q"«ùQ÷Ö¬ú5z{WÓûyz~\x001f¸#s"Ã\x0011ÑmÝ¥2Ê¦T¿ö\x0003¸;\x0000÷¿ÃY±3¹ZR]ÈMG\x001eôú\Ä³h¿_à\x0011Í2\x0010ô»\x0002ýóo'¼Yª'0Ç\x000eÑ\x001alç\x0010×\x001fûA ß\x0015äg?\x001c;4ì×|\x0019?jÖB£L=Y\x000ec|
òè\x001d×t§mÏl§Ë©\\x001e\x0002#{s
AØ]l¼LA»\x001eÚÍ\x001bºËäÐÛÊH8ÒO×ï\x000c§}Ï¼2âöTCGª«ëÃJ\x000fr\x0000.gËA\x001e:Ì\x001bÚDî\x001b(ÛPÞ-h\x001egn\x0017!\x0017=t·´ù+å\x0000ï¹3\x00033È\x001bU\Í5
zèt¥\ßÒS­¡©1²¦ÃÚMÎ,tî¡ó\x00196íZwjpÉ&´»ñ¼þü1\x0003Ýbø])Æ\x000cuN×²¦íµ\x0018\x001a[`YSB\x001e£á|8tåÑÞ rë.S»ñ\x00126E=C.ÛvFÀëÓ\£\x0016øiê!¶À|pq\x0011ûh\x001dµTFx¹\x0008Ct3Â\x000b)í*´ØS·T9s9è!ºÀ|xq%zs9jÄvÏ±eLîY\x001e\x000cá\x0005æãÝ\x0015ÛPÙe¿Ääv/máry\x001e\x000cñ\x0005æ\x0003³­â«\x0000réoq!R(\x0017×æ\x0018LS\x000f\x0001\x0006æ#
ÀÍÔùùF'æBÌF}úö{T¾ã\x001eñÔõ¸»~zÿëÇ'°ifx\x0010ñÞä³\x000cÈA¦^ÓT'N]·Ë¹ë§»ç¯N\x0000Ç\x001eüàjA\x00013kvå«VêXbqô|T\LÏm{î«\x0005
·óÒteá¦\x0000\x0003dÎ\x0011ºÌQ»\x001eüàfA\x0003eüI6N+\x0005\x0004ÑÍÏþXo\x001eÜ÷à\x0007\x0017\x000b*pyÐKÙòü\x0004ÙÚT6tIêÐS\x001f\ÉN
¦\x0004wSçºÓøu\x0015ÿ· s\x001f¢{ò\x001eç\x0014n\x001az²w±ûf²ÿýáÛç÷OhRÏ\x0017sJK<wi¹V+ò¬ü\x0018yõÃ»û»ÛmÝÓ\x0006i{H;\x0001IÏú\|J£"?ë'©ÒÚ¬ç8\x0019Ñ÷^\x0018±5gyã¥3\x0007i°\x001a3®e¢JÈÐC	H#ï$0ê ©òå4å×\x0014¡µ±\x0013\x000e¯Å¢Ð`x¿r¨EL=bAl
Jc\x0004R®ÊÇ>\x001b²;æ¡
ïtÊ&s\x0010=lmkwKrí>HI	\x0003%è)\x000b\x0006\x000fôôöÊUeÎåö½7k N\x001c$LxÉrl\x001d·yW\x0004c[%·[É¶´n t3FîÒè`ÌR\x0011ËïfÊíJÂ)\x0007\x001f\x00043Nj\x0007ù{;)~±­`ß¯¥#'BþÁ8¾Ëf-ð@êïrÑ/tH¨X÷ÿø·\x0013ú×=\cÍû\x0012\x001d{ëY,Ø\x0008Òm¿r\x0016[æÍ,å£oèpJÏ½ û\x0001ÝÿwB\x000f\x0003zøï\x001e\x0007ôøß\x0000½D±¸÷\x001eV<\\x0000~»JW/\x001fÞ_\x0001¾Opn=pÌ,4VÜF\x0002i\®³ßÑÿÊÍ]ý_y\x0012\x0014{P\x0001õ©õ8Dh®\x0003Qú/`e\x0006Ô\x0004hìAã\x000ch\x0002\x0016æ,7H2HÓA¤ñg­ÂïtPpû\x0017nT¼PHàXlÏ Å¦VA½ÜVç\x00159ÞVx<Û;\x0004\x0010¬-H|X¡\x0001äÛWåºÚh0Ãê{V?Çê[Êl¦¢¡Úa%\x000f[ií\x0005QÅûr"¸÷´üò\x001fÿöùý/ï\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=÷Æ4vúÈá-)º\x0007eHÎSkóËìÿT£¦¾ï_í*?N0\x0018
¦\x0014þË,Õ\£æ.T¨`½9rÏÝI\x0019wNiÉÁÿ«>«&ÎÂeC7Ïì\x0002çþÍü<ÑÇÚ\x0004\x0000Ý\x0017\x0001ælsb·\x001a8GçÒ<
Qýì¹KyUWT>:}xüñîïÿs¨y'\x000c\x0002Xýbèã\x0003\x0011\x0015á´T\x0010{}tzyõ
\x0001÷7ð0 ©\x0001\x0018°\x001c!ñúZ\x001c=\x0013â\x000fÆØ´\x0015ÐÕNnAÉ\x0010\x001f-5¬¥¤qI\x000et#`¨\x0001C\x000f Ö±¦r(!>tDÙÍ\x0006L5_êáÃ\x0010P¶Ç\x001b\x001dÆÉìLØW9\x001eï!b>5:È ¦;pâäVµ¢\x000b±Ù#Z¾I~÷]¬5¨å°Ü+P\`P/Â©Ã¾Î`Uê6¢;\x001a=:Ó_n\x001dµß\x0015}t5á\x001eÎ-àéÂDCÍÓR\x000c\x001f\x0010O¿;{3?¿+þúèjPÃ}\x001eÒÕ®\x0003Ò\x000e~ª\x00163ia)®jñ/\x0000\x0019kÈØ\x0001©D\ç!u=BF<R\x000cL!S
: \x0015Ð\x000b\x001a¯ÈH'´²ôfÈêíÓo_%¥m(m\x0017erLéÈ\x0001Ñ\x0003xH'¥o(ý×fKeÚó\x000645
¼~¼ùôÓÑÕäK¹+Ä£¸&ù²¬ù*ÞößQÛÀë«·ß\x001c]\x001dÌ
!©á\x000c®¾°[É¥Ì¹<®§K®y¤ë³5ÁYEáÅDÕ\x0014Ù°Uq\x001b¯á¼\x0010.Ð\x0001Â@ÏõÙjzÞlÕ-:àb
\x0017pCO\x0008½ÝG´µ\x0013í3Z·\x001b\x0002DL4ÍåÔëÛÇÇC¹Hù\x0019ßhºC'V[L;Ï£ÔûõÙÕ^­÷ËÔ\FÂe9¼As\x000f½7jË";%h"0[Y\x0011:xç\x001cÇ\x001f\x00063ô¶\x0016óüÎ)\x0002ó5ÿÀb
\x0016E`ty³I³ §Ê÷fþ~#âJ5W\x0012qa`,Ác»!0ê\x001fsa\x0011å\x001a,\x000bÁ4>PÆÌµ EaQ\x001d¿\x0013L·ÎBä-~_éfWjÙ¶ü}Ém©eûòw!»\x0001å£Úõ\x000c9&ÁíÑé/w\x000ftQ\x001a;\x0014·
xÖ`\x0017¥ÑÓs¯Ú¯\x0017yvtúÝÕùõþ^J45ä\Âe
¤¦h`MÀh`ôôÆ	o§!m
9WpY\x0001i¸³Ë\x00102ðµ±ÜÏ·Cº\x001ar.à²\x0002\x0012æ"£¡.	í©0äæ\x000c×ÉèkÆ¹|Ë\x001aFCIr¤ 6@:^\x000eé%\x000c\x0019jÈ¹zËópéÆÓ°É\x001e\x0004âG\x0019\x000fOØ6WôAÆ\x001ar.Þ²\x00022ê0L\x0007sc\x0003Hùß\x0005bl%ïú\x0018SÍ8nYñµ¡n]\x00039a´t!\x000b1½!s
9WnYgH7YÒ!
\x001br3"§PGG®:¶Í0±èkCëùR3V'e\x001bnäñfÈ
ÇT\x000cÖ¦\x0015S&\x000c¡}_î¤lâî\x00088:\x000e\x0003ïí°
¢øIË\x001fÜ¿\x0000e\x0013ptGÄÑ\x0016nl#¥Å·úòÅ3S¾-£{B"\x000f
uuIq1¾\x0000d\x0013rtGÌÒ)Ü<Y\x001fÓÞ¡\x0007ú\x0010÷\x000bz¯lBÇ\x001cXÞ²«Dq\x0005\x0018y;c\x0013q´<äÀÈè8.Z´TÜTvÎ\x000bP61Gw\x0004\x001d\x0008dÉ*éÅM\x0019·\x0007\x001dÝ\x0004\x001d-:&Æ)4êqò1\x001c3\x00031Ìö¸c¸c:âNPÔ\x000f\x0007^(\x001bÒü`ÊæM§²;¦ãã"å}a@Áo&õë\x0010òö/nÚ{NßE\x0007\x0019\x0006XXD\x000fÉ!Ø\x0017øàMØ1\x001da\x0007tÓqY¦LÒ&w\x0002Î\x001fÚFÙ\x001dÓ\x0011v¦,ÊðÁÑÖ&þàf;e\x0013wLOÜ±¤
m<P\x001dlIîÒ¦~Ê²·gõ+F
õ+4$ôéèjè¬¿¿8 ß\x0002%X¯Z\x000e@x\x001f«K\x0002Sª¿7\x0004ýpt54Ø_\\\x001exÒ!DS#\x001a9bwÚQH\x000cÃ7ìm"lN¾}¶\x0006´b@\x0013(ÍR¼$Ô×ÏNtT+&´\x0011]èäùX¡,\x001c<X \x0011¡Ï\x0011hòfÄP#\x00061¢MTëî­§2|Háï¬¶¯ÄX#F1¢7¬2n4\x0018t¬ä1\x00031éÍ©FLbDÇ)?o5½2fÇumÃI\x0017¢n]ÜçdKsÑ`ÊÔ¨Õd<!7­Û}ÏÑr§\x0013öñSGÐü\x0018Ë\x000f-\x000fó°Û\x0019\x001b·£Å~GkÍßºm<ö3\x0000Ï;iÆõ16~GË\x001dçÄ)\x000c£q¶\x000cÇ°yWW	|5\x00166\x0008íXN\x0013\x0007\x0007\x001eÅÒos|ÑgÔr×¨ß\x001bW\x0005§Ñgm]\x001fbã\x0019µØ5jXB2gìä*I7UÁoFl<£»ÆqdÖ`FQ0Ogñ\x0002N'7YlD§h\x000eèÖÉ\x0014åYÃÎÍáej \x001eÎbJnDÃÃ¥\x0011q\x0004YÎú2bØ\x001c_L\x0013_8¾ü#ÌØ\x001eiåá\x0005jqKC	\x00042*\x000e/Ñov¦	/F\x001e^\x001cÏ³¡>\x001a·47gÎfJõ16áÅÃYsx\x0000ÙG\¶\x0004·ë­Mt1òèâó$Åb¡*\x0019nºÓÛc\x0013`8ÀhÍ}\x0012{Ê2cØ~É2û6b÷­=&D\x0007²H\x0014ÒvÄÆ\x001b¹ÿ\x000ef?%~\x0001oYF+Å\x0012Iqó®¶\x0003·b\x0007^þe¹UÀ)uÅ;ørç\x001dÛ8p+wàÅx¤÷,öþ\x0018­\x001d÷©¹ívl<¸\x0015{p]®ÑÉ³\x001dQOM\x001a'ÁoÞÖ¶ÍK=¸5O¹RÇÑpïJRÛÝ£mÜ£»Çrp\x000f82£\x001c\x001cyt\Ú|r´{´r÷\x0008ã\x0005é¢¥ÁS\x000epÛÇo½=5a\x0003¸\x0015\x001fÀ±So'Éú\x0012|¸a¶éSêcl\¸»p(¥\x0013\x0005kE«Ä©<¿=â\x001aÿèäþ1NZA ¯âÈó$9¿Ù®ñ=Nî{Ê\x0007NdGj1ssìæ3¸kóò\x0019<ÂQ§©æI8:ó@R½y[»Æõ¸¯Òõ¸Æõ8±ë÷\x0018ÒfJ\x0011sËðÀ]°ÛwL³«xW\x001bç¸ÿÙaÓ\x0001µ/j\x001d\x00087o6µ\x0017oj<×OÃ|Ö\x000f×<\x0015±íícl6µ\x0017oj\x0010ÒÏÔáiSÃ\x0003!1æÍÚ7«ÑW£µ
T½g\x00155ë&µ=ãèÕ¤¼_ûFlJÍ­6 b3	\x0014'Á­~ämY\x000e\x0005RÌß5\x000f®â¼½=ªº{\x0004&çü|÷ù ºN¤G#ë\x0002i\x0015ß¹FÍ- ºùèìõÅùõ!A8olªn YÆó^­TÐ\x0002\x000bÿh½Tx½\x001aÍÖhV¦Yb«xF\x0012?\x000c$Ú\x000bÙï-h®Fs2´\x0018Y.©Ü\x0007\x0012	ýÑ\x00191jµÔ\x0011´\x001aÍ×h^æI(Í:\x000béxÓh\x0010_/õE¬F5Z¡\x0005K·(ë\x000c«Gr=Ñ®&L7»@\x000b·A0¬Çeé¢\Ðxª´eêf\x001bhá>0ºöJ¥'ç©X,Ú¸­Ù\x0007Z¸\x0011\¦\x000b\x001d¸\x000fê\x0002ç\x0002ï¶vZ\x001a´$C³\x000e|ÖU
B\x0001ÿ
lSþpºJÆ¦5N*ö6R*SÇÈþÃíè&ØÚ Ü
ÊR=Cúh`\x000bt'»Bò"¶f¹\x0019ÙrKÉ>¯ÍÃ¸¤ÍI6oËV²¿\x0003[\x0010³¡n9°ùHlÔ\x0016väDlÍ^0²½Ê\x0001\x0004Å\x001aâ¶øè¹5.¶W=Ë¦Ã\ð"L\x0007\x0010hzürsh
\x0008\x000cßÀj\x001a=x®\x0002ÙQå\x001fzà?\½?¹x\x001eÊÖPV\x0000\x0015¹ÛÃÅ\x0016\x0003(Ý\x001eÒD¶\x0004ÊÕPNf)T\x001fòÆ³&S¥wV¾\x0000Ë×X^f«HU2\x0016\x0013£zxA¬\x001dÙZ	V¨±ÌZ¬Y$ß©©l.z'Á5VY+µRe-ÂÊvËÚJ5VY\x000bk¡`F:Å¥Ny\x000bV®±²ÄZª>½Ï$±Ë³\x0005²Þë©ªÙ\x0014DàÖYËðZ§Y*Õ
SÊ;²Ú\x0012.Ýpi¹hÍûtliP\x0005	H3Ç\x0016{5.^|<\x000f»,·s*º)GkÄÚ½)	¨\x001a\x001f¯ENÞPÊ\x0000´´\x0002¯®ÀZZ[¸\x001a7¯E~Þ°÷\x000e_ÃÀZÌµ3EÂÕ8T-ò¨\x0016:\x0007®â.(üPõYÖvCøÑçÒ"×õ;b©XI\x0017\x000fþF¶\x001bñ3úÉwñWL]ñg^©®ÇJõU¢9^½Qtª\x001fX©h«>k­|ýÆôU0ýô0	\x0018a¦Ò'ûXlÍb×°\x000c\x0012aT³¨
+\x000fL3­c3nH\x0000\x0013j°Ò0f
ÅÈªéü\x001aÕNÃ\x0015 Ä\x001a%®´K¤ ¨ý¢ë3ûíä}§]R
VÛ%a4{ÅÉ0¶Ó0¹fÉ+
\x0013èÎ\x0002µ)øá¦Íy=Ku"QãdåN2Ó!O\x001bçÃä¾¤[\x0017³ÊÇ\x000cÑ~ª6!\x0005Rîp¶¦ñ1z¥Ñ%z£\x001a%~ò¬ÎÝ¤\x001b/£×º\x0019_ílOî\x000eþ¶\x0007\x0002\x0016×°¸u1Þ\x0019m$õ¹\x0012*ig+Û¹}\x0003ã×/\x001a|aâNµf¬îüJûÕ+ý¯tý!}h¨\x0001ò$íÙ^@Óx`½Ö\x0005\x0007Ê\x0012ºr¸¡\x0011\x0008ä½:mÓ¸`½Ò\x0007\x0006\x000eÒ\x0014¯«Æò@Ø¹\x001b\x0017¬Wùàâö\x000c\x0017\x001c;\x0005ÍUË$u´ë[Â¦qÂf¥\x0013¶$ \x0002*l\x0016-cH¬!¦f¶\x0000¦qÂfíA/sùS¬	Ç¯\x0005IùNÓ´\x0007½Nø÷Y4¦qÁf\x000b.\x0001Á\x001eã'\x001eWT\x0001\x0012;C¥i\°Yé'»4\x001eØ¬òÀ]¨®Ú\x001a\x0016ûTT½\x0013sê»\x001aÆéUNo\x0008N4\x0012°üÒ\x000b4
{i\x001aGcV:\x001a\x0013è
\x001aæ*Q×\x0015mDÎðd½mWîmIèiT8Î,.JK¸S\x0012Ð´\x0017§ûÉr·®\x001dF©k'\x0006ÅNË4kØ®\Ãe?Ez|1t£ÌÆÇ`ún+¶YÃvå\x001aó&Ò$Ïkk*:oNÿ?uï²\x001c×$h¿
vÿj`q¿VI\x0010¢P\x0006\x0002l\hÓµ¡%I\x0014*\x0008pQIZõkôî·5ý\x001cõ&ý$x{dÄÉ\x0011ç¤Z\x0019#âL\x000büD¸{øUV'X6`È}b6ÏåN[eó`=?Í£QÕQGFçÁjÆÒKX¼N0\x0013]\x000f\x001fo\x0006n\x0004üMãË\x0012ÿ°a'A\x0003A\x001dçòaz¸eJëU½\x0010\x000c©¡£m#êAéÐ2®¼\x0008Åz¯ÖÚ\x001aÉ4 >¶Ð\x001fnÒzU/ÔL
"JT`ó=óë	ÿ\x001e4Y¢É>´ïÎ8-j¶y¤ñk!·.2]é.2\x001d`Ñ´\x0018&Ô'3S.2®aQH\x0019©pë²¢²ëi².2W¹>2+\x000fA|x\x0007 û\x0015ÑÖó-hKê×s\x0011£cß}w\x001a°Þ,\x001f_Âÿüü²s$\x0014f#ÁDP\x0013\ÞGYG\x0017N\x0003ÛÅÅâMø¯¯\x001b\x0006§Øê¢FH1\x0001ÒSï=ü\x0011[½§ì¬eÕsv"¤,!e?dp#$\x001aKai\x0004ð.^U	÷ªTý*OìAÏ¤±îB2êÊ¶uÌd"¤)!M?¤+HAÕºR¬¦Ô²=HÒv\x0002d¬Å"H\x001c	*ÉÍ¿8¼¾Ý\x0013®wªÜB\x001c\x0011\x000fåjLí\x001e(«ëÍ'Üo\x0008ßq¢Ä#I1\x0010ãõüËÍ«{Ã'\\x001c\x0018éCgç\x0019r.Ï=ó~þÅ)\x0007\x001bÚ4Ø°RP£{lõóÔßgó¡ó)«ëÍ'ÜoÁiü"P\x001a!çØr\x000f_¼ºß|Â\x0005ÿ#)\x0019w\x0003ï:ü\x0005ïwwËO4küâ_ÿõÓËÇ»Ûw\x0010q\x0005l²§|ÎAúj*è»ÓÅ\x0011\x001c¿8~wýêôäß¶¾LÜÀ\x0005LùÍbê\x0012S÷cÆ,ª]\x0016óú1«¢\x0018;S
\x0013ßÕ\x001b<Þ\x0001ßóòóÖÊøàh`­]µ:hJ\x0008yaÇ\x0017\x0007ï\x0000îjñúø»OËÏË§çÇÍ¢\x0004\x0014½ÎÁ\x00034\x00153\x0016·«
Ñ"ô\x0012p§\x0004e	({\x0001µËÅ)v¬Ê\x001aÆgôwà©\x0012Oõâ\x0019Ìã[\x0006/A,\x0005¡r1±¶³Ntº[xùé\x001c\x001cÄ$<ú¸b¾ôLÉg¦ð¡ª\x001dynÈÇÆ7£tð¹Ïõò)K64K;±ª\x0007´c5ó]¾\x0004ôÝ9\x0006\x0019õ ^,Á¹\x0007°(\x0011PEÑb3 \x0004lM.BýÇ(¹9V,Õ\x000bX+èn
\x001d^Y4&\x0015FBk\x0005\x001ck=è"¬44ïUÑ\x000e\x0016\x001aà%Ñ\x0016ªfS!=\x0010ÎfãJCón\x0015
«ªPË@>\x001d+eòä\x0014?ÞjØEh+BÛKÈ\x0019ÕÆRµ±µô\x0000ã>g\x0012V÷w_d&òÔ`±\x000cË\x001aïÁ\x000eê+Þ¯ìÂK<pg\x000cÊåj>¿añW).\x001f£1^öÚ\x0013OÉ*
\x001d+ÑP\x0008Û\x000b¾\x001eYì\x0004äUÔ?:ð\x0017Ý>¡@ãV«VuþÔr´I¬ùaã°_9­/\x0007ß?<n~EÅh6Mø\x0008$iÈ5õ'Æ7#­ß_ly;\x0011(D+TÔW\x001aGàP;ÉåTlíÈµ\x0002É\x0012H¶\x0002A>\x0016\x0007:(I½CÖñ,¡õ~«V S\x0002f wÈHB\x001c\x0014ëìx]Uß'[]ÆôÑ­Ç(+VÒç\x0012¢\x001c$rLôç´1ñ·3åÁYp´)Ocò,¥u?n\x0017\x0012çÃ¨\x0000×ÅU+Ç·D0\x0005ÃbûÔÉ'¡\x00029ËõH
~9u¼%Á\x0007¹8@\x0016SE8pzé2pø(ª*Ç:\x0011YÈr*279ó*ÆU9G=°bä¶L$V%±L,Üj\x000bÇmÒ0æ&\x000f$Ðû\x0013².õTd%ó|¨DÀ\x0015=ç¼¶#\x0008\x0013Ml&KÓ\x0014\x001c\x0008oÓ@Oß\ìØÄöÛ\x0016²2Ã\x0010\x0019À h÷ü¼c¢§¶H\x0003{°p¢FÅ½.Ûäí@¼îêj«Sf\x000103\x00085àY\x001a.\x0004³\±ØÊÑ\x001frB'K:ÙI\x0017\Eê©Ç\x0018\x001fÑ.=6\x001bÞ~ÍxªÄSýß\x001e-\äÞ\x0011çFÛMñf<]âé^é)ZÌ\x000e-?T\x0000¯Mþ¸ëmÕx¦Ä3ý\x001f¦«3o&cäÌèÐ&<7];VÖ\x0003]ÜüøÓòñyK-\x000bþv^Û­éµgr­ÿõZã·ï\x0016\x0017W[Ê4\x0008Mh¢\x000bM3\x001a¿¬\>uå¹ÁjäýÔ¦J4Õføj£ÃÖðóø98=d¦$3]dSï©2*RyÓ¹÷=]æºÐ\x001cÏÍºLæÁ$JäM\x0008£e7»Ñ\x0002Ôà1\x000c«LÓÓÁâþÓíÍ=Ô\x0006ýøqùü¼¼ßÂi\x0019\x000c´@LA¡Vïss©Â\x000bnº<X\x001d\x001cAÐÛW««ÅY\x000b³(Å\x000cfC\x001a\x001a¦$â"\x000c\x001bÇê!3eÉ,ÿï`V%³Îl]î.eyÇ»_µ\x0014USëg2ëYÿß!gY\x0006ÎÒù¿øÑ¹\x0018z¿Â\x0014\x000fü·Ëm:
rÓkã-¬ÉÓIÝú\x001c¹ë·\x0006\x001cQâ6\x001c.SÈQHJÛÕ6\x0000·¾¸¾\x0011G8²\x0011\x0007E§Ý0¬Nuy\x001bk¡oÂQ%jÄ\x0011ÊÃ`:½¢\x0002ãü±Ìz±l#.qt+\x000e+?@\x001c81è¶ú5SÝcJ\x001có§KÇ8¶\x0011'-º£ñMØùæ`\x0010.Jg}¢_#+q\«tV\x0019bh¡ºy*ÚscYh|Iãÿlá\x0014i`aÊÙ5ÒÙáµVnTË O¥y«^þãx*EÈÿDM(ar\x0019Ãä'áYðô´J-ï\x001e¶=]\x001efk\x001c©DgX]XMô9	/ËËUÚlqz¾\x001bP¢\x001bP\x001cbý¡19å¡ó´Lg§â13Ìèø?z|¸}ú×¥É07Ï·Ï\x0007Y>~¾Ý<±Øxx÷á8\x0000\x0003¹yn¬\x001a/.ÎO.Óã««¿,.^lY<ËÇÒ\¾) 2\x000114~\x001ef¶RÔ«îAL*KR9U¤X¿¤¬Î\x0003KdÖþá4ìT¤j\x001a©\x0012ãÔ½nsÊ³èEUm<T¤z\x0012©æÔ¡Â­¢ù"ï
ÕþÉ¤¦$5ÓdÇ\x001e+-s\x0000Oå@\x0014¯;'ÚÔN© Û0SãÝ\x0017>O¼`{¹Q®$uSeJô\x0015å»LóJc.÷¡¥Vî\x000cÃQ|SPyÞa\x0019.)ÇcÊ}È\x0017\x0013õu9é\x0004HÊ/Ã\x0012\ÉWz\x00081ç¬.!5_©Eüã`ëöÿÇßÝþró¸¼ÝR~.­¥\x0011$ÁuÅµpáÿ/\x0003µ­j\x001a«ÅÛ\x0007ç§'ï/\x0016'cãT¤Ãð¤AéVqÐT\x001cÛ,U])ÿÉ ²\x0004\x001d.o\x0004U¾>¤ÀqÙ¬ä4m\x0013
öªJÔáføFT©©bkKkD%¢õ^HuI:Ü\x000eÿMÔL$etNÃ×Ç%ÂS]ëjMüdR[Ú¤\x0006\x0005ãf+
	ó\x0019ðF)µ\x000fRWºWÊÑº@n-µ\x001cINO%mÙ^>¿/Qý4TÃ©·?ø¦Ë\x000bz\x001az X`\x000f¨Ù¦&ÝÏ&*F/=ë
¥¢6.]G¾&ÖFj¢r"ÏpC0SÔ,\x001e<½°VfO´SÞæ[å%Æ[´Ìýrû`­,\x0015fª\x0014Ä\x001dð°ú¼Qf©Ú½VO³TJ(Ê[
Æp²¶\x0008Ôªç{a­L\x0015f«\x0014Ø*¬\x0006\x001bmÂ3Jôµß¯Â+cÅ§Y+ðûñ±"£\x0013 `ãHjßåU2m2ke®ø4{\x0005ï>j\x0011¦\x001a\x000e¡À7@L°ïµ2X|Å\x0002Öô\\x00116{\x0001JÑÔ\x0019SWMF­\x000c\x0016f±Ö´âE8-/
©ZP§²Êbi\x0016\x000bÂ)8ð"¼§±j>°R¼ÂÔ%dY+£%¦\x0019-ed^ÔÄcOdÕ¤^!°\x000fÖúm5Íh)c©p\x0010Æ_Ð\x0019Xí»bUp2ke´ÄD£e%9\x00030ZDã\x00190y\x000f\x000b{9\x0003Ù\x0012\x0013Í\x0016tÑ¢\Íê58´T\x0003½3P-1Ñl9'9(Zõ$ËÕÏïÃs\x0015Ù\x0012\x0013ÍS4Ò0nZÄÜÔ¶\ïC¿ÊlfËºCC\x00132Ì¡C³eE¾[j/¬Ù\x0012\x0013ÍÍqKÜå\x0010î\x0016­(Þ}°VvKL´[ÆÐ²\x0015\x0011\x001cí4Ë7è,Ê±ºât*«¬ìh·Â\x0003\x0006k\x0015£aëá\x000cûjêÝQY+»%'Ú-çhÔ\x0003l\x0015(WGmÎÆØ}Ä\x0005de·äD»\x0015\x001e[X\x0019^\x0013Ê,×½èWY\x0005'Ú-\x001f\x0001É'\x0005+ù\x0003ÚìÃÆÊÊnÉvËkÚÃ\x0006®6NR^ºìjïC\x000fÈÊnÉvËüÜ¹d·(Ún$Û~ÝSíV\x001e! `\x0014/¢æaIõ8ÿÉ¨Ù\x0013ÍÖÿ\x000cjeµäD«\x0005á!\x0018è\x000cX\x0018r/Êµ2Zr¢Ñ
Î\x00006@$.¥Ô0äÛ÷Àª*£¥&\x001a-ãèbq8\x000cøÍ Úñ}(\x0001U\x0019-5ÑhII-\x0014Ü¯\x001eÜ<§Ü^\x001cBU\x0019-5Ñh\x0005'K\x0010«Ç\x0002ÂÉÒû¸Xª2Yj¢ÉÒz\x0004÷\x0014w\x000fº\x001f/íÅmQu*k¢É2yÄÐ\x0016\x0007!Ãs;Göá	¨Êb©\x0016\x000b6¦!ª¥\x0002v@%±j½\x0007% }­[ýDå
rE7;Ðñ5¹\x0006v\x001f°\x0003í:õMðÂÂK{P &bÝÑ×\x001foïi[ëâñþæöîn\x000b§åv\x000cÂaµÉdYß\x0003J'àèã·'gieëââìøäô´\x0001R²\x001fÒ\x0005Ç
ppË(í!/	B-gCê\x0012RwC:°LI*\x001f¨ÒØ
)óÎqiªÔP'äp\x0018!sºîÉýþáñËÖGÊË-Âfgîøj4ôúxX¨øýùÅ\x00060Q\x001e0ô\*WþHòîï4>¬¬K\²K`¶\x0005q\x0007Ð	\x0007V\x000cùîàR%êÍ[+¸Áú 0Ú\x001alÝúf×\x001e0]é.0¹nÐIãq«\x0012Jl¼¯µË\¦\x000bª5éIZÜ(\x001d-@qlÖ´%íáõr´aÜäåÏ"/ñ\x001eo¢nÄr%ë\x0012¤`\x0016$e­¢Ñü\x0019Ý,0_ù.y­¢ÎåjkÃ)]×³ôñZµvéVë)\x001d(]¼c¤kº¬Ò­¼K¹®özÅ\x0012¼×+ïäX\x001f}ÒCVi1Þ¥Æ¼ËsÎ»
éåaåè
ûf°Jñ.5\x0016Ì¸§ù6"Ïnµ\x0014t´RÏú\x001eã],<Ñèc¦­ã¢Z¬jåÁ\x0006d&ã]ªì\x000fY¥Ìx6³á\x0019àL\x001b¢\x0018×#\x0019uÎ*mÆ»ÔçäI½ÚÐ·åÈö÷v°Õv¹è±.Ië(µÈõíçiIf|úi#Y¥gEä
êÙàlP/ËjñÊ¦±Êdµ\x000fÛ¡gãn\x001fã¥yîTò"é9Þµ¨¼XÑåÆ\x0006¥\x001d P¹ê³Ò ô$b4?2ãá­¬Id¯`H üãwï\x001eÂ#ùhùqy{³ekµS\x0016
ù\x0019*£5JT[¢ßñÑâÕâìäxËÚj6ÞÍÒôî«Çex°?ÅÊù£ð-òâÂw°\x0015\x001d7ËZGw³Ê½ºXúe,?
Ø&J4Ñ&4L\x001d^s¸ëËz'WY?*ÑT\x001fZ.
Æ¡Ãá,>/zõÕ¸§~4]¢é¾\x000fÊaJÄµ\x0010<z±V%\x0011ûÑLfúÐ4õ<éÀú,<àòlU3Oj¶D³]h°\x0006[å³&ðZÑÜ¼kàK4ß\x0006C\x0016h:O\x0002\x001c²¯öAùph)OCKßßÜßÜÝá\§ÛíÓ,ÏËe\x001eãiÜ	çÅTo÷ÇgÇ§§8Úæüò¤	Pª\x0017PÅÍG©Ùã~¡b¸¹«÷ªu\x000125R©\x0018¥z\x001blBì[\_o~yÜjUi\x0017öWZ\x0007}Ø*Võ6Øc\ÊõÃñû6FQ2~F\x0018\x001b§òw&eìòÐ'Sù"Ó\x0018eÉ('ÉFqC¯?ØBrÓ\x0019ùpù ×å Ôw\x000f¾n
¯<[(ì¢âç)mõºSì9w~\x0011ÐvC\x0012J´C\x0005}gp(xl%¨<è×ñFøV(YBÉ.(\x0013iX<H[N\x0006Ì/mR%j\x0012yi\x0016&\x001f\x0005O ¬\x001f\x0019PÚ
¥K(Ý\x0001eijª\x000e¤õÞå3µ>Ô?Cm^¸BPÅòµüsÏºàõzAø:%p\x0015þÿaxÜ¨bf5\x0004ÕÐËÅ¼Îox^EËp±-KE¢d\x0014ý>\x0017ÅB[ÔÊ¨çÎò
I.HYBÊ~Èà'Ñ
DÅ±j\x0015Vñæ§Ö©]ªTß¨$u	©û!u\x0001W_xíWuÕã\x0011.HSB~È`õq\x0008\x0004H\x0012×\x001d\x0007¿Øå3\x001eóê´%¤í\x000cj\x0010s\x001fp&%­ñÎ\x0013TøXN\x0017¤+!]?¤³«a×âÞÓ@p&Çc\x0014]¾ô$éV·\x001b§Äå\x0012$Éù«ù\x0004Q³oóPòJQò	\x000bzÁ\x0001%-Ïý¾áïáTÊ½N
}ÙÍ\x0019\x000fmÇA©Ä)WÓù×§mOøæåDüîõvæOOCîPózq5ûú\x0010°	}\x0008«'±þJ^\x001f\x0000>á\x0000¤ÕPëä¡qd:ÿ\x00000Ss	á1J\x00075¼\x0016\x0010QÝ±ås®Óp®HãtÑ÷½ªmÞÛNuP\x001c÷r\x001bþê ÌÈëå\x0012ÊaÎ·\x0004zÅpø¬HÃg[©|\x001a×Ê8Ì\x0001ØTª½¾Ö¨\x0003KXúO\x0017Öp\x0018åSýýÍãçÛ
°Xjo\x00030Ã\x0015vº\x0005MHµ\x001dÞ½Aß\x001f_¼>¿~µ­®Ðd&»Ð¸¡	Ä½JÑ\x0017oÆ¦v ©\x0012Mu¡A
 IÍ\x001e
o+a\x0008Môì@Ó%îû ü¦iø¶\x0017TNëÍØ\x0002¡\x000e2_ù>¡yj\x00026&\x0001\x0004Ëé{j5²â¢\x0001ùapÒ×#	aÐËãöð¦	ô\x000cr¤\x0018^È\x0013è«èP÷\x0007+®/vé\x0012LwI\x001aI\x0000í³\x0019l5åÍÎIl\x0004®\x0004Î\x000e2AËÍ¡ßÀRD:\x000e¬F{´ÉaO2Òh¯\x001f÷;\x0016\x0003JÄrò\x0010ç]Ú<\x0017Y­Å^-.^-\x0016gÛÎ\x001c&ød^qÐÂ$ò\x0004\x000cå%®Ì´«õËzm§g\x0007,ä·Á¤J&ÕñíÜjþ#}o]þxrmÆv\x0007.¡ô·!(S2\x000eAiþ«àÇ:Z\x0012§ºÊµ(J\x0007+¡\\x0007<¤>OuäGÄjÑ©LÒV§Üv@y(×NêÀÒÓ)o4sÊNbCsÃªm¨)Ãïïo\x000eÞ.o·ù÷Á[õT^\x0002\x0003zirº¥©C\x000e\x0016®{ø8øþìøàíâd«O°¢\x0015\x0013aWµ\x0000Ê3ì\x0007k×¡VN÷ÃÊ\x0012VNu^ÃÍHi<-<\x0008L§Y_´Ö\x0005Ëíp'eeìñæéãoÏÿú?[3@\¢8\x001a\x0001sÊ«Ê%[./_ýûÕñE\x0003(éD'rTb\x0007\x0013\x001dÍ\é\x00193Ýè % ;,w®N)»¹tª¤Sý²Ãg(xn´\x0014VäÉíÂLnï¡Ó%î].ëQ'ãv\®fò¸â=t¦¤3ý²#w\Ç¬sÇ×kîúèlIg{éV3¢\x000b(»<yulE@\x000f+é\¿ìÈR.o\x000c\x0010yÏ×H\x0004¶Ît¾ÿÜÑÜbeh{<y\x00180'ºb«\x0001(cÖ/;Ì\x0004(¥¨ ¬¸³l½\x000f¡\x000f¯¶\x0015ÝÆÂçF/i²:æ¹\x0014olçK\x000f]e+x·±°\x0014¥VQÓÈÍ%~æ­à6æÝêØÀ¶ÅH\x0017\x001eû·\x0004Õ±ûõÄc\x001bà\x00037@pVWFA°÷òæq;ÎEylU-XvVøh=\x000fÄz//ZøDÉ'zù`Ú4vZyCõ\x0017N¬AÕÄÑ)|²äÝò³\x0014*Q\x001dÔk¸*}ÓÖÂ§J>5¦ W$->\x0017¹\x001eTËÑº·\x000e>Sòn>zâòCªa±­j£ëaãbèxö\x0016wwTìövùø\x0018þw¶»YÎ8mEÉîTÚÀsÿ!¯:ê\x0016§§Xìövqqq~v¶£ÜM\x000c}Q\x0011\x000f`7$,âB1jshÒü%&Ýj#O©KJ=RPók8\x0019\x0006Û¹ºJd"¤/!ý\x0004H\x0008÷£²f\x00192Ï¶·ÎÍfä ù\x0014I®j0aEJN&«ø\x001cQ:>x]:^÷;´íâ´:7=ð¸%¾e^\x0013jÙx!zã®P>¸ß×\x000fm>W
ÀJiñ,½*\x001cï~èb%£ HN¯Í \x000fiß\x0002*Èá\x0004?\x001daàÃÄÀÇñÓO´OñøÓÃÝÍ¶\x0015"@­=\x0018Oi¼zãùñå;Z¡x|t~zÜ¦K4Ý&soð\x0013(áÉøyÎìD¶áZdV®EN=T÷ÏËÛ­!BØ5^Q"Ã©Ü¯j6O8»Zl
\x0014\x000eW#³r5r+\x001e§L£\x000cw6½(Ú\x0001#
gâÉ\x0012OöãQK¡£!GJPûM{­xªÄSxZäù¸ÎææÔn`õúú³N:[ÒÙþ£§ÍÈÑS{;zªZÓ\x001a\x0005XWõ4P\x0006?\x0001\x00074IÇ¨\x0003,ø®Ty¦7\x001fí¦ä~XÔïcpz5 åâáåóÍýæEm+uÈs\x0011«åÕÖ<åâüúõñÙ¶=r~XGïc@\x0017\Qà/h^\x0014Ëµ(\x0001n|ºM3)áL\x0017\x0008Obµê>ÀY¼Ü­jê+Ñ\x0001'\x0013\x0018Y\x0011xõ¸}ìNj¸B+uîð\x001697âÇ³ò©\x0002êbÇÜ\x001d\x0014%äÚÀÝ0L\x0006;\x0013$_AÒDcçª®Ò²\x0013 EÞf­X^\x0016ûLÂÄ|FS2Iôµ+F¾\x000fH&`ÃÝã§åç­ÚZáJH\x0005´\x001c.}ÙhÁõÁââhñºLd¢\x000cF½âË3øÏ\x0014óÍ\x001e_ËQw©Lu­²çÂá¬´@_î^5%4£\x0012Ít~NC\x000fa\x0008WÒç$åbý¨_ÕLæJ2×G6!\x000cÝV¬Ê\x0013¬*Eo¤¡rJ
ªár*\x000fÄÙ\x0001ÞÆ­<µnÆuòÏÏic+þyûi[­n¦dª^\x0005Q«)*qüÕUÚÙ^õÑ\x001fVõ©bª(KÕqJsÚxñòô|ûsãÑ×åÝËÝÍòe³á°\ËzêÔÚ­ª\x000coÚvq}yuòoAG?,N¯O\x0017×\x001bY?2§*e÷
²»\x000c^åâ~»gÃÑ¥Â.çW#<êa#¸)¯ìeðð\x000c\x0017gg§?üü=KHC­ûò¼5
¥\x000e4¿=.ÿ×ÓËãÿºû~\x0008LÀb68MqP\x001c¦\x0006\x000fU³0s$8ÂÐÀ¿X\x001c\^_#÷\x0003WV\x0007ðúj±iÛa\x0005\x0018þ5r\x001a Ê|Ð1\x000b°#\x0000ù~\x0008ÃÝ×\x00089S±\x001b\x0007\x0010},\x001bÊdD\l2\x001b1\3;
Q¨X¯\x0013\x0011%<"¢å\x0019Ñîé;Û\x000fK\N¢Äí«RCC\x001bPBQ0Qbíã4J÷ñIÝÿT\\x0017rê_\x000eÞ>¼ÜÝ6Féã³( jØ»¾5ì\x0004J°Ùn\x000c¼üë·ç×§\x001b\x0017VAOo\x001e2Ýëo\x001c28Wê\x000cGÛ|KÿýÌ3y
]6±y\x0007w°¦8ø5Bzib\x001b¼å\x0018DMYÞý-öÚl¬gÖ\x001fþñh¾|#°Õ\x0003~½Z>>ý×ÿyÚ
\x0015<\x001a\x0016³®A`N+îÀ\x0004d»¢À¼Åm\x000e\x0003¨W«\x001f/7Úã;ó§;òGøõêæñ\x000b6"mâ,.GôQR6¨hc£¤UÉ\x0012kNcPPÇ\x0017ob?Ò&ª__þ~ó3Pç
¿^\x0005IÞü´|yÚÍÅ"Öû\x0005.ã4\x0004Ó\x0002²Â'aéà°\x000b\x000bZ¥Þ-®/7é\x001fÍ?Ë(¯ð¯_§7\x0007¯\x001e>íÆràÁCX^(\x0001\x001blüVÀhRÀ²Jc\x001e\x001f¼:¿<ÚÈô\x0013\x0017?ÿ\x001e»ÌàÒÄ5,é¥\x0001	ÜËÊuAR.~AÃdx_G$îÇz ºn\x0002
\x0007*îZi\x0005ët\x0002²±ý\x0002Î¹\x00170d0\x0002AÁî,"Ðþ²(Ü<"ÙÅ	\x0008ô	H`Pq\x001a\x000eHÁ¿·5kc°8 Å±j"}5¯ö\x000cÊÓÞ»\x001dLwËûx¶AÁÁ¯7Ë¿-ï\x001e\x001b®\x0011\x000e\x0015zÀ5ß ¦ðg®§å
\x0003¤7ï\x0017§çW
L>H\x0008~õ0ÅêÈ\x0014$î[`\x0012é,\x0019¹¦Hå§kÒÇÕL\x0001Êoçeâ((Ãôè§Û\x0005õ}\x0011îs¬\x000eÇ\x0011~½Y¾üþ[\x0012\x000fç[Æ§\x00006\x000eÏJ\x001c&óÅ/\x0007½\x0018ãD×ý÷<µÚ\x0018<\"ò\x0006ÞÇ@$aH$²\x0014ôè"RÏâùËS<Ý\x0016^·çöþæéùá¥å(ñÔ\x0015\x0016,`\x0002ÙãWs\x000e}\x0002íÙ¨¢|srv|\x0019¼T\x000f>§Ñ3ÁO
Tw7¿ý~Óà\x0013ÀL8A+@9\x0013ù@
¨8í\x001dä$\x0018:=þ÷¿nñ	
&\x000e\x001f¤	Vx@\x000c\x001cDÜ4\x0000L\x001cM\ð\x0008äè£m\x0017\x0012ÿûï¿}¯5xÜÃ¯àÏý\x0005bÊ
v×ùØA\x0004L\x000còBñãAßNRÚ:Á¡û\x000b\x00047Rýão_ÌóïÑ\x0019g.,>ZBÅÈçÛÇ\x0006iq\x000eC1 \x0006\x001a
º»á\x000bú \x0001GeÀÇÕé\x0002JG^\x001c_lÙßÄ¯^¢ên¾¸ëèæËcÓqw,í@§ÒÛ[\x0018tìÑã\x001b\x000cÌ-}E\x0004\x0017\x0018~µ\x0013ñ\x0018&O\x0018xrG"A\x001f+\x0018ÕR;¿Þ~ý=9áÝD\x0019ÿç\x0014÷ÜõPà6F\x0016Á'\x0017)M\x0011z¢øõÂ]ØÀtyu\x00011ÐÊóo¿Þÿþk¤
'Ý¤Ó~zó{ï\x000b9}
G'¢\x0003¥<,{PÂ+pØOÿÚÂäqq¢)\x0018µ8m>0A¼D¡Í\x001e$RÉQK¼é\x001f¿üöôÏxÂÃSÜ=*¶[®\x001fÄéL,¨\x0008\Æ9ÒêAcà£*\x0018è
îo¬ÜºÚvû
¶pÎã®¹>6Iª!èL}(éLÎKÞ\x00001
\x001eÆ÷²	ð}z\x001a¨ï1/K1/\x000fg£Ù`\x000b-ë\x0016`ù\x0006=ÁÒ'Õ

±Vëú\x0006¶\x001bñãßÜ§hÈà×ÛûÛ0!\x00049{\x000c/\x001cnEÑÉâ~TdoÏ¯ÏÎO6¿"~þYG (ü?þ>ÎdÞ¥¾,× ³¢'ÊÉe\x000f\x0002¬Å\x000câ_\x001dn¤úxÿë/·Ñ\x0017Î!ø\x0015TÅ»ý×\x0017Lûî"3*\x0006jé¨\x0001¥ÇD¸«n\±.\x000eÞ\x001d¿¹éßÝp\x0010_pV«|1}pT#[0Ú
Ù¬\x0019õpúØàÙ
¿:Ù|xæ8JÃaæ!øï\x000cìý	W½X¿\x001d<{+ùò\x0001d\x0007ÀCwûñáå\x000e3»ÜD\x000eî4ÒAB8ÅBÒàùD7X\x0002ºWç×§[²úøééå÷\x001fã¥\x00087\x001d~b{w\x0007µA±y\x0011Jðêºèl(ÎÍ«\x0004F\x0014Û»S¸¯\x0015Û/Ï?tQvP¡\x0007¿.?\x0006\x001f¶AhVbLK:Xö¡RL\x000b
$Ð·r\x0014ëbñ6x¯=ÅÏöNFë\x0019n¨L·ôâ&\x0015§íô\x0015aëËêÃ$\x001b\x0010\x00001A;,Ö?äÅñÉäeA\x0015¾_\tÚCeã|P\x0008y³8\x000b/Ry#üMJ­
1ð«
òäÉ0q\x0003\x0018)n£ wn\x001f?V\x001dTÁ÷_=²r2½l¬ÒL¶(+\x0008dåÇ#\x0000;©¾>/?
ÎÕå²E{û\x000f¹æxªÂ|&IØ|N1^-KÜ¼üøÏ2W
åO·Mo[¨ õ>Q¥r\x000f|1úzb\x0013ÓÕâÝÉ¶·í
\x000bÖ¹*ÖË&©Ei\x0019\x000fSx,W¨ê=3\þV²!ê`ãÉ}ÕZc|I;	\x001e\x0013\x001c£©Rû¤¹ù\x001a=ëp@á×Up\x0011o\x001ew½\x0003Cåô>µ\x0007,\x0019\x000c¥Âp\x0019â^\x0005\x001fñøbsàë\x000f¿Û_nË×äûûçûeC¨ÙpÔ9>'DWLC
\x0006>'7D(Þ\x001f]\x001d-6\x0007\x001fÕ\x0017õ[´×AÁÀ¯÷á.Û<	ë£cïmÜ~\x0005¶\x001aFäa"þ[Ç°..\x0017[ý\x0008þðëÏ?\x0016\x0019÷Ó÷jù¥I\x0006+G+XfÌk_º#×#óï\x0003ÖâM\x0013\x0018f4»ÀÂAÇ2\x0005\x0008\x0015¦#¯DE\x0011tÇ\x001e¸R9J\x001f\x0017hz`êP¥·¤òô\x0004\x000fçoÜéê\x0001Â6ÎúÈÂYâéàÃ8o\x000fI«Ücé\x0000\x000bÿm\ö)\x0015k\x0002ã\x0019sÝ­ãÙØFì \x000b\x001fw~L\x001b\x0003N¨X\x0019ÃTT>\x0007ûÀÔáW\x001frJ§,.UK,²MÁÃ\x001e°ð¯à®\x001b,ø\x0014¨/%§Â@\x0012'i?Aï#\x000bÇû^2-âTÔH¬7ÌH"¬qõÚ\x0005®èT°A`|{é\x0004Ù#C/ú\x0015N\x0005\x001b'óz,WY9¤/8ºëM©ô\x000e²ð¯\x0010ªWÅBî\x0013ÏÛ[ÍtÍ?ýÐ):¯eì\x0018shÂq3¨ü-\x0019Kîö ²p\x001eí\x0005ã¹<	V|3\x0004ã\x000cúbC§\x000cÊ\x0017m·ò72îr"ô2
jd&öð1aWí<f,G^ö¨üµYb\x001bâ®\x001d\Ð¡çz5\x0006u¤Êæ\x00125¬¦$
²ù`A\x001bºN
k<ä"é^jzº©¹ä|ªÈ+¦f¡ô\x0017u?çÛåc\x0019àqXJä0¸"Y\x0002ÊPBTo4¾[ÿÞ.6Xâ4\x001c\x0004­÷ò6j¯@\x0012Ú`ÂÄåf!¶Ö\x000b·V"åß²LmEj§ªXÕ\x0017Iù*	]Míô^H}Eê'R\x001dv¸ð\x0013)¾#´\x001dGtêIç4x\x0007©*K\x001f{-\x0013©'\x001a7\x001aì%­Î©vNÕÊ×Òd\x0005µ#'PgazAu\x0005ª¿YPçJPç&8/\x000e]1A:Jí*¿T¹¢w*ýE1éñtùËÃmCT?öyc¨Z8J¢\x0006\x0017\x0014ÛÜÓp\x001d(ßl.^Aæ~ô\x000cûÑ{XÁúL\x000e{\x0004ÑZKVÔ×B¶Âæf¥Õ_\x0014=¾þëÿ{N\x001d^»9\x0015ÖÔp³¨Q¨VÑ\x001bTÚÍ÷þ\x001az½® Ók'©(IÅ$Rm³	Â5\x0018,2:\x0007æj>©æß
TémK\x0005zxÖãxÈ\x0018qq\x000cÊC4\x000b½;1ú\x001e,/ÔÑ®\x0005¬(aÅ4X«¡ .õ)èÍ°F\Õx½P?¬,aåDÉÆÂâ$ÙÀ\x00159\x0005Ck
fÃê\x0012Vã°¾õß6,¯/ØÔ\x001böÓJ78´Ò
\x001a/¿ÜÝ6¥v h+éå$]À¥g¨\x0016ÛÛñß\6Àª\x0012VMÍ!6\x0018ø5óZRÌ¥v³Õ|Û¬ªr
¢lË!5ß\x0014r5,0ýE1¸úÕòé©­\x0017NèCO¬\x0012
ÊUÐãu\x0001hm_-./·ôÁ
Æ# ¥BÉ¨S9Õ1°6ü,¥æaúO\x0010MN-õÑøZH¥¤¥
\x0016\x0017\x001d-­}v´Æ×©¹>900o7¬(aÅ4Xî²¯e9ä4XsxJÇÍúae	+'JVÇ¹,\x00116VÁ¥Ô\x001cIãì~XUÂªi°å\x0000kAÉ\x001aG×_²=IÖ°v"¬»ÝðqÀ0¬k³\x001f+íèíê­Ö¥¿X9ÝÅà¾ÝoCÚcñÄâ;FQÂV\x0017O$µºc_Á)JNñírÊS~»ºäÔýáò\%\x000c«!pEAñ\x0004W/¨)AÍ7+P_\x001dP?éjEå°ð\x001e¤\x0004\x0000$£Ñ¤n	]´ªaìBáHÌÇÆ\x0003M©
\x0018¿K\x000e²ñ÷ã¥âå\x0000À7[\x0003WbpÂ¿PNBÕ1ú¼>NË\x00058v¼£¹T\x000e\x0017\x000f\x001cö@K8
]?£¡\x000b3\x001e\x0000'WÅ/;=]A¡á\x001b[Æ7ö$ZÃó½Ò¶ÈÖÒ!\x0010ãE\x0001Ý´Ä²eSk¨\x00002¥*XNÈ~\QáoTº4
JÑ\x001d£  àþìáùñæàõòÇ*yo=ö+éãöR(øö\x000cU\x0017ÎFÜÎÎ¯.\x0002çâí¶»ÅËAªé/À¡ZM²ì\x0019Í3­4v5ÛfólN²XßìWËÈï|\x0015Áj.Ãñ\x0019©zD;
\x001bª¢ÚC¢nGúj{ÝóGX@\x000c9\x000c?~0´P^ñêæñ~ùø9¶X5T©Zçcä2æZ¬ÃÉ-átrNé«qSðêøâlqñ:6Ym®UýÈÒºdµâ\x0004\x0017\x00188\x001f\x001eHÏn^~	¿?7\x001cUÅ8ögJç©¶\x001dÆ²GRç¤\x0018'=¿\x0008"=;¾~\x001f~\x000fÞ	]\x0008\x000b®À·\x000c++X9	\x0016\x0006(§Â\x001d\x0019Fee¹ÃrR\x0007ÕÔsic<H\x0017çÀ}§\x0007çàò¥\x00016\x0018Y\x000fj
úÜxP^);\x0008ÿ\x0007§Ô[6z·JØËëm¬"ê\x0001¥3+\x001b\x001exõø¯ÿúýöîàøi÷d\x0008¦Ã\x000fMê!-ÃH«W\x0012C\x0001V¹ñÑ\x0010¯.ÿzrzp|¹y:DF4\x0015¢éF46.ß\x0000DgÐ¦\x0006\x001b\x001b¸¬ò~´/£	Q§nÕe"ÈÔgüæqyÿ%èTÐþ_ ëÿ¾Á¿\x0006­\x001e-\x0012©zÁji\x0007\x0000»¦6uÜ¼¹X½	ªõ`ñ\x0006&\x0000mî"nÍKnÍgpC´2yÛR³+Ò¼\x0002©Ðt9!ì¦\x0016î.îx$´]qËï zòÍËí]0¸­\x0016ÁK\x0018gÆ+ÔK\x0011\x00195-°
n\x000btó\x0005K»Ó\x001cØ\x0004É2¤
Á#|»\x000co¬q=8¹i:»0"Ã§aUÓæÁ\x0019d4çd\¿¾]'Ö»`Z\x000fÎ¯·\x001f_$å\x0015)BjÃí×I \x0016vU%R+ÍåxN³\x0017Õ\x0012\x0015Æ\x0014ö£Æõ³8\x0004Þ"	Õ,Ôñ.õ\x000eÖd\x0007Ü5ØpmßÞ<Ç\x0014ÖAdzðþöSÓ$\x0017\x0007ÃeRV \x001c}Õ°Eé:åFýÂ·ÇW1u\x0010§\x001e¼?9Ú6Öåc8oØ¡ÜPdz"ðÿºxøôµÅÝ
ïÂT-$ 7Õ5Å*ç¨
âëc6A^\x001fý°BÌh¼.\x0012yÅ¹+&ä5ú\x0000>|æ\x0014_1y\x001aFuÆf^¬\x0011	ÊÊol¢:\x000fÿ¸Ýü\x0013£,\x0019e7c°ñPd\x0013\x0019¡kB&FaUµ¡¸¾\x0007Që\x0012Që	
h!u\x0000\x0015\x0001:¶©ç¸\x0003ÑT¦\x001fQº4-PZÍ|áÉ\x001eT ÜØP»R}¸ùèüéîCÕpõîî!îÁë£\x0002×ËÝíð\x00066î¡¤\x0017&<Î\x001dT°,\x0014àcVÑÃþúôäMx\x0013\x001e\x001f¼;=/,aõì¬\x0000rcÕ\x0005Fþ\x0000iìh\x000bO7ÇÓ!\x0008iDÐ8Ðb0þö/\x0011ÀqVºÁB¹HB\x00100\x0001\x0010u(\x0005iph·\x0014V\x001dú;\x0011<\x0018\x0013£Ï Eª9\x000e\x0008\x001a\x0003xý\x00088Ï£\x0001Aa\x001491pÄ`È\x000c|\x001a\x0003x/ºùB\x0012fø%I1à°)¡\x001f¦}íB\x0010°\x0017P«`<Oë}84Kd\x0013	 ©±é8\x0006ñ§wf p±å\x0019\x00084­\x000b\x0004Ô4ÒÏ\x0010T¶6-\x000cNTb\x0016h¸¶x ­¤Ã@°û\x0019Â}ÐMwÂ	\x0006¤\x00049ØÝ\x000cÚÒ¥àzª\x001cpìNË¥°)J\x0005ßÂ¤uJp)dþ\x0016|âÅ¤1}»\x0019à\x0007{dPq÷\x00050p\x0014\x0018\x0019\x001dW
\x000c8¯A\x000eL¥¦À bþ.Êsü\x0016Q"S\x0018x4Ö¬\x0005B0eSQ\x0016\x001c\x0008¯&¶ÒÂ`f\x001aDlìåM_\x0003\x0016l)j26Þ¤ÛI\x000cÔ8ØÏ\x0000àmjRú4u?0¤i»QOz'Èn_\x0003^\x0001ñ·\x0016\x0008ÂLÁr3\x0006F<AH<JèiÊÇnfÞæ¿H²t\x0001Bh\x0018"\x001d!\x001cÙn¥Ü4=Åa\x001btü­åH\x0018h K\x0010qì0\x001e	I>ÌT\x0006hæF¥þ÷ÀÀ%´\x0005%\x0006çRQà¿\x001f\x0002\x001a¥yÕðAS¡3g5ù\x0011Bl¿Å4\x0017ÇÖcÞ¢²\x00056._\x0004\x0008¦Ieã¨Èt7T\x0010-ZB\x0008ÉÓ£\x0016¼\x0008V,\x0006E®ÉtI1ñk\x0000¹hÓ\x0012Ú¥ú5ø.\x0002\x001e­ñk\x0008rèÂÕ
\x0001ZB´h	\x0011\x001euY\x0010§uuA\x0010Ü)AÁè~\x0008Ð\x0012¢Í§ûã\x0004h	Ñ¢%D0©¿\x0004ôÙÍ\x0011ÂfWMUUPÌE_\x0017\Zòë`ã\x0018Z\x000eÅÈ»µ%\x00017T´ÝPÆS\x0012 \x001cÄÓâÒÑÍ\x0008\x0001Ë\x0010âo-ºJå\x0008t;49¸~âSC\x0008Ë6\x0013\x001a6=w\ìé@¥mÉËúRÆ M\x0003JÝ
ÞP\x0017'§D\x0008Lk+¦\x0005\x00018\x000cRå²ÍzM~¶\x0015\x000cF)E\x0008V\x0013Õ\x0004Äão
ºÊcYjz\x0001³dCCÃ¨
\x0013ãø[Ë
eèh;];éIUq?ñ\Âè­ø[Ã`\x0016Bðô\x000cg\x001cÈ\x0017O\x0014\x0002ó¥Ú\x001cá?ß¢\x0008Ö4Ý
ÉènH#&\x0008È\x0005Æß\x001ae8\x0006øô\x0002\x0013Ê$º|Üé\x000bª\x001a­Ï\x00174hNC\x0019TUB¹G\x0002\x0012`ñ·cÉ|*,;ÜÒÆÞð9\x0014Cë%¤¤%\x0006{+vÂò4²\x0008T§Ç`\x0014Eþ\x001eRÉI\x0002~þ¿!ÇßZ@\x001cÛO£1w¶ ^ecîGù¦°åO_¸»-×Ã]H\x0007Ë\x0003¶¶å\x000b»zÃ\x0017
²I¯\x0010X`ÇëZ6Ã\x0015H\x0007\x0003\x0018¶Ö8¾k7¢\x0008zE
Dô\x0018bñI\x0010í\x0008Ç·^5\x00081xføÓ,NßBÔd\x0002\x0002­Ø\x0013âøÎ«\x0006D¤\x0017\x0010y\H\x0010\x0011\x0019JÐO{B\x000cÿ\x001e7\x0005y\Þ\x0010\x00106\x0012*C¯\x001fnë`Ñ\x001c!Æ6¯ Hø\x001f\x0013dÉ|Êå\x0003¨Jñf\x001dÔ;'QúY ¿ÿãþ77uJêâ\x0006We#1èÝ~©àÜ*è6\x000bL
æUE&X8:Ôö\x0017Çg\x001b7¢W\x00109+ôgBäÌÐ\x0007Á!¡\x0013kÂ`)E\x00160OËK\x0001C\x0008ÂCU06\x0019\x001dÂ\x0018¾]\x001cÐÎ\x0012Gp	Ð)Sá2\x0011[s¶süâ>ýòëïÅ7yûpÿü\x0005&g.c6w\x0013à:mk\x0003÷H£?\x0002Õé»\x0018¯Lõjy{~võ\x0006e.Êìíf¤u\x001aaÀ\x0010£\x0006î»R	FY0Zù0\x000eJáð\x0010¿5ËÆPöHh\x000e
\x00148[ÄáFOM\x001c°\x0016kN\x0010	ú\x0004\x0012Ö\x0017§3#)Á\x000b³$6Kg7\x000e¼Não­Ò	×X&^HonE*\x0001©É4åmú3ÏÎ¯ÿøüró{­nOOËðcÓ\x0006ç
4Á±çÆ9É \x0003\x00084B0üVZ®EÊ\x0016ðçÕúêÃ2|¦¢ÏD}XÄ?\x0006¬g\x0018süc0\x0007w
\x000f!AN\x0007ÁRÞZòwµ¨uñù\x0015Ì7~\x001b¬ãÁ.ß7#\x0012Q|²Dß$¢*\x0011Õ7¨KDÝ\x0018\x001e:r>R_ðÑÜÎæ3%éæ¸Î	\x0006\x0010ÌÁ¼\x0018\x0011ÚA-Ç\x0014B[\x0012Ú~	ê4ç
\x00089\x0005£Ù*¬Áæ#º\x0012Ñõ#ºCeAqßA"t9¥6(FBèKBßM2\)ã#u\x000bJ¯H+ç"b=\x001dimÖÏ¨éª@8Íáæ6\x0017x±ùµeé7-\x0006çØ¥@¼E9Ê\x0017ñ¬þ\x0014ÆÊ´ð~Ûb\x001d{l¸Ý\x0006c\x000eÁI3û¾ðÊ´ð~Ûâø!FKy|°¤t\x0006££\x001aÄçú\x0011!©Q!öQã¾/\x0010¨<Ôc®[{©¹t5c¿âÑüN£Îi!NU
Òë©âþ÷\x001eEì\x0007\x0016<¼üü{6Öÿ\x0008~¡Æ`]\x0012\x001açSéÍà~,\x000e.Î¯ÿíºÞ"´öK´Âp& \x0007Ay\x0001eu\x0013rP\x0018ÖKóa\x0019y­@^)ª~\x0017gÃ\x0002\x0019ï@\x001bOÓßÙOñÅ\x0005¹UfÊõÜ\x001b_7B¦\x0000Ø+è\x0018Ï	\\x0013ÌSkµ[Öq«\x000fæöë³ú¹\x000c¸¦gÄöWôizmxE0Gs,ÓiÅ\x0016À\x0007ÄbS\x0003B\x00051Õ\x0016`v´F\x0008Ù<%\x0018V\x001e\x0004\x000c.&c`Ü´\x0005ÃP\x00182`h,bT\x0002êH\x0010CN\x0006­Öñ·&\x0010\x001fWýÒGaé¡)è\x0015®qï\x001cú×/þïØý]J#=\x001d|óø¸|þûònk5¡Ç)îPâ©lK0AæV\x000e+\x0000.\x000f¾?¾¸X\ýe±qõWE\x0004çDõ\x0010Y\x000b#<\x0007Ç4ª\x0014KY\x0001)uMDËû\x001fù×§x!á\x0007¿-(2¼-í¨rDø\x0007ôÞ¡\x001bä]]l¹ Xp\x0003\x0007¼âo-\x001c°Ô\x001b$¤ àÄª\x00027|»:ú¹\x001bäóOOw?\x0008\x0002Q-øí_ÿqðîñáÓ×m
\x0007ÇQb^IE
\x0017ó
¸å\x0008ö
»Êj/\x000eÞA¿Ð¦\x001eò\x0003¶Æß8vG=\x001fL´¢P=Bx5\x0015\x0002Îjü­	BÛ\x0006U\x001ekaÌ\x0016	Ã×Í\x001ceøª	\x0004z»-^\x001a\x0003þ\x0011ä\x0011êâx¾{xxú\x001co\x000bÈ\x0003~»úzûñfk:O*øÁ`ðâþ\x0011Lçq
ÐkS×ñ\ýpòêxSúðë§O¿\x0000	¬ø[ÄÕãÃo7[Ô\x0007\x001er\x000c¹òàËdv
V4\x0019\x0017}ÀR\x0012W\x0017çÿ¾q;«ú _n¾þl?äèYÜsõøùfùòëV¿HÂÓ%È\x0002\x0016Òå°±µoûþøâõñâúoÄøÍ{Cwkû£6ahéÒp`(·\x0010\x001899(Ü° hû
cd]ÔF\x000e%ÈMõ¹.i¯pãÉM4f\x0006H\x000e¬6\x0008)Àþ¼öÞdïy\x0006GNeµpÈìÄ;¬\x0007ÕÞQOÐs>ÌÈ¾¬\x001cÁ§B~È\x001e{\x0004É\x0018ÃV§\x000e\x000c|Õ´aäG¿
­[Àz\x001aÖê\x0010;@pÿa\x0013\x0011¹¸fõ²g\x000fö<O\x0001ÕôíWÆP\x0005·1\x0012üÅte2÷Ó¿Íè°Í$|U©\x001aü\x0013Iî³`3D\x0012­m³6ã7©ë>]ÞÜ	Å\x000fª\x000e±Ådo¯¾\x0004"  90R«~­v·dl\x0013Ù&\x0012\x0015|vª§N] Äd\x0012;ýÞn\x001eÛ\x0008\x0002Ã[y¾8\x000c5Zqqä0;ßA2¶il³HLZ=\x000b*>\x000e$ÚR¡[¡Ü_\x000cWþm$V¨[5ùd^æB=½Ö°Ö\x00012¶ålóÇah
º\x000c*kñãH\x001aVëuÿ\x0008ÑªKTðS\x001dV+9Ñ«ðq\x0014ÉD¬5¯u­1ÛxSQ\"¡x}¸9>¬µ4v\x0004M"Úm°Ãð!]dû\x0014Ù>áÞ\x000e±ýiÕ\x001aKs\x0003á5\x0013\x0017 $\x0012KÕn^O79£\x000bÓ6kzAQ	ísø:*\x0002\x000c+®\x0015ÙtÐ"÷6XÊÞig©\x00020Ø^º:r­9¡\x0004WÔ6»Ää¯ãÞÃÕ&	Ùª×àÀÒ«×»CoÉ[#·Q­5Kt\x000f+$©±:\x001e@°5e¨\x0019\x000e\x0001\x0004ge»¤²\x0004
\$Cï\x001b5ýâ@PR6k5hÇ8@PpØ\x0000\x0019tt\x0016®L 4#µ\x0014Ç°Á\x0017°0ù³Ö=ÑAB[ÖÛH,©5Ã
53×Zt;@Âÿªl\\x0018ê£W°JM\x0006y\x0000z\x0005O\x0007	jD¶ª\x0012Ã\x001cÖ\x0016y\x0003£):C¬Ì\x000c\x001bÛIò^÷&\x0012IFMý9Ä|në`35\x0001ªV\x001fÉH{\x0017ÇªÜU/¼Î\x0015üÓu\x001at¨Vf4§s\x0010	¶\x000fseò+g­ÎµVµ·@
´ÎÍ\x001c3YÍ¯\x000f\x001aè\x0000	\x001aÍ´jµ\x00183Â\x0003qpÌ2r_9kÄ\x001d$\x0010§hÖ%ÁÌÈÕð\x0005:¯gµF\x000e NÓªLÞ8ä9bB
çòÇ3>N¸ý¦](**\x0005EïÑö¹¬çgDL`m\x000evzM\x001db à<z\x0003vE²6¸§dl«îF\x0012ûÄ\x0000"&\x0010MC§ÑMoÙ±-ºM£VgèÓ\x0012¨éÎ´! lW\x0000e\x0012ì ÅÌ_'N6J\x0012\x000e«m\x000e\x0010\x0004ýN]\x001e0\x001c
Ah<CL\x0008O\x0005\x0019]%¼\x0019$?Ë\x0001\x0004%"49|­Ó¶\x0003$¨!×jr`28£oã!\x0014IÏ"Ó¿
\x001cu×z^\x0015Ô+èLÂÓÇqù	*ø\x001f\x0004³]«ÿªÂÃ\x000f±á\x0012ù\x0014½q*ÄúP\x000e`o\«ÍáYÎÐú1RõÚª\x001cã\x0011¼ñÁQó­Î´>ÇøøJ$ùâ@m2H¸4¾õâH}5Î±²F;æÓM\x000eØoß|q¸M)ÏTj\x0015Âë<\x0017cÍÉãÀ\x0010mß\x001cX3\$Pô\x0014\x001bçùâÐ ïI$á»úæ+¬ý¡¥G¹Áª¾@B°ÁøÍI¸¾¾ù
\x0007µ&È!`Xü\x0004j¾â3\x000el¸¾¾9L¯³³\x0016\x001e<\x0014õIxäL×%àûV¯QÁT?\x0014\x0010XÏ\x001f\x000eÌ*\x0011;ãÛÿ\x0006ßlÁ\x0007X=üPxN©Çð\x0004üÊáP5ÁYs8+È*Xå·(\x0000+åôHE5Ï¬Å]ó+¸
\x000fÝ5*,\x0011÷äàéñæ¨´T>÷Ù\x000b\x000b¡ÎÇO
Lï¿µ¡À\x0003\x001c6Óæ´Õ9TÏÖFQv @ñj¾?\x0010\x001bp+\x0013¾cÖö3D\x00029.Õ\x001c\x000cÖæ6¨6*ì\x0010â&²ÛwÒýª©)Öòã²¤4\úíòqKÅkÚß²\x0011È¤}\x00007¨Û\x001d#iôÛÅÅÑÆÚÛeK,Û\x0015\x000f\x0005"5UÇ\x0000/=Pý\x001c.Wr¹\x001e.»\x00082X\x0016«Ã÷¤'¼«ëQ{Á|	æ»\x0004\x0016'ïæê\x0014|42\x0013uz»\x0013,wà\x001f{È\x0014.\x0003ó%á=9¬#ªÛÑzÉDE&º>¦¤wYx9`6Ñ¬|c3\x0007LU`ª\x0007\x001caX\x001eàx\x0015S?ìz±t¥»ÎÉµ\x001cÊ®ne\x0016Sv\x000eY¥-xº\x0010Ù6Á3àòl$3ÇgÉ¬Ò\x0017¼Ka\x0008
#Ú(ËD
#\x001f¥æ(2ÁJ0(rèÒ°ëa:§¿ò \x0017¡Ì)*!º\x0014\x0006ËãY¡\x0018lÉe)b^²Ja.\x0001\x000bÐU~\x0013«·ReGl/YeÅE\x0019g>Ç¸]gÉ.Ñ¸/Ø 9¬Òe¢K)MµçàahRÿ6;\x0018s<\x000ca*0Ó\x0003Väl\x0004[¥]U>flÅÕÕ]WSKjàÚÈÌJÍ±²Òf²KA#\x001e³ð<\x0016t\x0001hÐ \x0018\ì$SÌTÌ\x0014Ï\x0013¶¡Àê\x001dIÏúYÇLU:Cué\x000c©i=ÑÛâ¿\x0012ÉÄ\x001c/CU\x0017@u]\x0000¡ :ÉC²L9Déü4ÓÄÊ­Íé/âÖæç¸\x000bñõÃýò÷åV2«©ÎË×5N	g:\x000f/duCàÅùõU\~øúülñ×E\x0003*áT\x001fÍLQ\x0010\x0003/ºTwM\x000cl@7)ÙL\x001fZy\x001b.VEcM\x000bEx½w \x001fÎp¶\x000b\x000e¶Úhª{UT@oóÜ\x0007ag
Îl®Opá\x0019ì©\x0017G­ªsÏp]ËÞÏæK6ßÅ&\x001cµ\x001eBA,>S_¥ê¨[7[ñ¶c=ú>ªã£RO¡à¤U´áA°:ÛOWé\x0011Þ©HØª´Êú\x001cÄ5ôöÑ~ºJð>MRL\x0018EL\x0012\x0019In8d¯®R%¼O\x0004Q\x001e¾AuÞWÁõÜ¯Zé\x0011Þ§Hþð\x000bQ]VþmÝVQÝVÑw[ÿp¸êÀ®\x0003ÇçA!,%-U¼\x000bIÆÁxºy.¬\x001düÍ7¢ïê)_\x000c§|Å
Ò/\x0007¯OO[»µb4ÓO;&Ì0Z¼$äú£áõõÁ«ÅååÉÙn*YRÉ\x000e*¤D9NKÃ¨b-\x0019Õb¯=L;°le;°8Í&ÒÙOú}\x0012Ö §ÖIåK*ßAÅ\x0014u:ÂBJ#\x001f¹¿aý\x0015ÓÅëÕs´þX®êlñÃ\x0005)X«­Á!µ^Ó\x000c,±ö~oâjp
ÁÆÓ"÷§w·÷Û&!ÄVfó×)\x0010éD\x0010©õ\x0008ÑëãËw'g§Îd&Y2Éf&
.Rv_QÓ92\x0018øÒ\x0007¥J(Õ\x000e¥r\x000c"L\x0010:·ðõE;.¡t;Tx}\x000f©v{X\x0006ý\x001a}P¦2íPÚcß±¶\x001c\x0003µPArÒë
´\x0019ÉH¶\x0003)<¨ýåÎÁ<I^È\x0019ßÎL®)\x0008\x0007\x001b<!%O=«æ\x0005.×â\x0019íP¾òíP0#\x000b\x001b¬ÎMÒ*?¹_×í_¯ògâ\x0017îLëGäô8®gBmÑêí\x0002û°¬E¶ü6dæ?|¬¹>þÙ\rho$ØÅ/7÷ëàíòe«O\x001a>C\x0005a£wö¯òºÔbñþø,¢\x001d¼]\owIMl¢;E-ñ°\x0002$oYðy\x0007HÉï%ì\x0013yÙq\x0003u_(9V³ûáT	§ú$\x0007#rpÒRø\x001c2VSñµ´uzº\x001fNpº\x000bN@ã\x000f®ãÖ\x001eù<²Mº§¢\x001fÎp¦\x000byKÁ<XþÛÂW¥¨õ3%gK8Û'9(µÄr1Éh}ó<K®\x000eÑöÃ¹\x0012ÎõI\x000eÂ\x0008\x0017.nê\x00125\x0006\x0006ù *ÉæK6ß'8¨ó£ÕN yàD\x0016Ü n·\x001b×*¸O\x0007óð.ÂZ\x0012 £
?¤I¤§Hx¥y\x000e\x000e
*­2¸9<h\x0016+¸J\x0005ó>\x001d\x000cS°h±à8ÍÆ8Îòg©æx¥y\x0012æ^	\x0018G\x0015é8§ÉåLªóêýt\x0012æZø\x000f¿\x0012\x0016æ]j8Î!Ç\x0012PË\x0015M\x0005V«¥ì¥Wýt\x001aæ}zÏÉ\x000e¶sáeyK§êx¥y\x001eæÎ:*\x0000³BåÅ¼"7ûj3Ïkâ"æ}\x0005/ñWh$rO4nèÊª&\x0019«zDìIt\x001a¶¥·y»óLã/*3!úÌ\x00043*¯\x0014&D\x0019-¨~PtÒOWûê]"øêìÐe¸äªË¼«}Ð*ÔV	Ñg&@päÓû[e%D\x0008\x001awµu2oÈ:Ï?×uÉf?]e%D`\x0010i#=\x001cÛm£è\x0004Mÿzæ+GTVBôY	XuMsÙ¡\x000c\x000bDæuZÌ¼®\x001e\x0016}zØz
\x0013Jè,Ô±E8A}QRùyzXTzXtêa)²ªãy;´áù£fY)bÙ§­e\x000e*²\x00159p)w)d¥êdªÉðX/\x0006Ãöñ\x0001+Y­¡´óèê¸D§¶c&-Ë»Çó84)gFtd¥íd¶³´åÅ\x0000EÎ7Bêhª]ª.0Ù¼eE\,yûQ+M'û4V\x001b,\x001c	\x0003©F1øtyH¶IWùÃ²Ë\x001f*\x001c`\x001cû^)\x0013ig^×J\x0011Ë>El ?\x0016ûoL£^¼Ìmr""]8¼tl\x001e«\x001d­¾V à°ÆÓÍóNT¥U"6ÊçáÚCÞ&
§QyòåÌÇª<bÕå\x0011sÏTÞoÃ\x001c4ºFÙéüHó\x001e\x0013ª²\x0012ªÏJüñ¢«¬ê²\x0012á(¨¶Ârs­y\x001e:¤fê\x0013UG¯û¬\x0004ôÖÓ
æ?o\x0019YÍÂU3é*C¡ú\x000c\x000bO~fW>1zìv\x0015ù]+C¡ú\x000c\x0005$é±ÆÈh
\x0006-
Å1YyªXUBõ\x0019
ØÃ5Æåe6ÑîïéÆVªXõ©b[Ü	ê»1|~OH;Ï?Ñ²Ó}ÊÎêÕ\x0010boéË
+2\x001d÷\x0014Ó>Ñ}úÄ
Iu"¶\x0013RçV¡X]gú®,\\x0005G\x001d\x001e4\x0006Áp-rïÉ<¶êNè¾;\x0011Ù\x0019\x000e\x0000\x0017:wFÎzëÄ\x0012%\x001düsW¢S\x0019ú²ðÞÆ@±÷9E<;±#>üü²|¾y¬³ßáß}S¹;]\x0017M@æ\x0013þ¢'ìnòvÈà´S\x0017g4AF\x001a;3 "á´÷Ar\x0007\x001eT0¸\x0012-\x001c3ÚÍã:c·\x001c%¡]rÃN¾Ð9\x0018:7\x0015*>¬\x001dÉÎó\x0008Yxî!s8ÙjG6Ëç&räý\x0007òË\x0003a3HÍ\ì®qã\¸ÉÔh\x001f
U·ÊS¨\x001b©9\x0018ßó6D%ìF\x000b\x0016Úó¸¥a{\ç.¸Á:.4U¢©~©éÜ\x0007ã	*\x000c\x000fÝÜm<RÏÖH¦K2ÝO&¡\x00088\x0015¹\x001aL\x0014ð\x001cÈ\x0010jÌLIfzÉ`\x0016§Ý\x000cK]
³¹\x0008^M?h¶$³Ýd"'0´a\x0012«í|îÐf#%çÍ³Ò!ñ®
\x0001Ûe§Wõm"@Ì\x0018jm\x0010¢û³~d&Ý×ü
*ÿÃèåÃ\x001dx¿¿ý´¼}Ü>ýjõ`TjÊV\x0003ÁªOzy~
eÞïO\x0016'\x0017×Cf0Q\x001e00\x0007tÔ8ÎüÕÎ©ÕN?\x0007L`²\x0007LK2«0Ü5O.Syv¶4sÀT	¦º>åjâº`¹\x000e=°\x000e
mÄ\x0000©:c±¼ G\x000f·ÛVÁÚQÌhÃ\x001a£`WB
ÇëMÚéè\x001f]üïÝh²D]hlµ\x001aEÛ¼B ×(
¿>q¨\x001d­zY\x0004´ô²è¡Ó[4 Õ.ÇÇ6Ù¨p~øI=|Ò7ËûÏ\x0007o\x001bd¨f
ÝJïóe^«7\x0017³×\x0007k7,YäËbK\x0016ûç²øÅÿ©,¼úF¼õ#Ak0*r½6àWíD\x001c]áè?W6Õá­Fçù±à[ååjy|¬§wuðTç·\x001e eÍ­hÔåû«D\x0007jÂ±CUckëñýÃãÎ\x0005I7T\x0012\x000f\x0015õ\x0008?Òz\x0019µà÷ç\x0017o\x001aÐD&ºÐ´ 0\ÕX 5Ò¨³"Ës\x00077ÉLvY\x0006HZoÛU'3U©oÌdæ["«C:ñ¬ÕÏ&\x0007"â\x001e7#ã ÈX\x0007á°\x0013¥N»»Ø+zôuù|³m7W..íL5¼_±{B ÕZ~qzz\x001c\x001bF~X\\x001d/®w³©Mu²±ÕàrQ\x000cÚÏpÖÏã¬ã¬N»Üó\x001eÔ¯@K´\x0005\x001bl*î¦«>+ïü®áÆ>­©û)<ÃòÀh&ç}W^}WÞùa¥ÎëÙ\x0002]~$,ººS²ÎTt¦Qg)<-\x0010Îæ
XLÌ\x0014«à\\x001fÈknaÒÇµ\x0002f\x0008V/é ãb`ñá\x0000®z:anÖ×m\x000b«ÇÈ¨.0ü\x0013®$6LåÉívdªÁñeõÃñÖn@1Ðs\x0001Mt¡¼è
¶Ý0BSyÊÒx_u3,Ñd\x001fÍ¥\x0007ÐòûÌ8t©L}\x0013d
N\x001aÔ¶ÓÝò\x0013ÙÔ·ËÛÇÛ}F\x000eß.È¬¾]\lµ«Ã«ÀD1täèæqkG¬gåØUAù<BntæÈÑñÅ6±á×d«¯¹\x001bÉé¼?@3L{\x0005¤ì;Óôáè\x0005õ
ÊÅÁ]xû\x0010~öýÁ¿þß÷7÷Ï[°\x0018¼\x000b\x0012\x0016ôÎc\x0013¿âFâioÏÃ\x001fÎ\x000e\x0016\x0007ïÏ®6ÿ\x000e`.æÌ
,¨Ü¸eoyðî&±×7w\x0007\x0017\x000f¾naãá+¢¢Qéh£´£+\x001f\x000c\x0001\x000fÇêÝq<a§\x0007\x0017çG?lÁpüyÎ6¼\x0015Å0 \x0007ðno>=\x001c¼^Þ\x001d¼{\n\x001dÙl1.\x001dÞ¾Öâ°@å0Î\x000cwD\x0005¾ã£ó×Ów\x0017Mò\x001fþ©ü§å\x001d^\x00008öG_o~\x000cß\x0013/æÃýóòËýíM\x000cj
¤îqùû\x0012Ø\Ð°25éJÏ¼H\x000f¬ ¸\x00142\x00179\ø}±øëâ» +Þ7óüìjñæìäxcd³â\x000b:[Lá³æñÈÇI³t:%Dæ¸áy6\x001flÞÂ\x0017«%ø)-\x0018àX*\x000cpPFµ\x0017º >Ô\x0014:ãN\x0003 7i³Q\x0000´¤çÐA
\x0018N\x0002\x0018\x001e2\x0012?/TÔ	Pq ÀúÄÙ°po\x0004cÈ\x001a\x0000\x0005í<\x0000	¦&\x0000 ÙÓ'\x000e\x001fÂNº \x001eÖß%@|±\x0006@Ãñ\x0006\x0007¸§\x001b\x0012þ5n\x00049tvÄO\x001c¼Î8'\x0007\x0000\x0015IPû=\x0001Â*I,9A\x001c÷>\x0003 ñÑ\x0002ê¹|<.\x0004¨RñS`ð\x000eb^\x0013\x0000Sº:\x0010Z¹'B0"¬H-Â|\x0008W"Ü5dFþ§®1\x0004·ù\x0014C"½JÑ\x001d\x0010¡JÕÁ\x0010ë\x000cÝ~®	\x0004\x0000ø$câ©\x0013Ò¤\x0010
\x0008Ð':Á÷E\x0007û&Yp\x0004ãTcLiöx\x0004M\x001fß\x000f!¬\x0011bJ4,WBB]-éè\x001a\x000b%öt\x0006a»Ð$[âX\q \x0019c#l\x0016á~1äJøTUíP\x0017\x0008÷dK 2#¦hB	3\x00030Í\x0018\x0003B\x0007\x001fÊ·g\x0013\x0006%#&)p}\x0011ÐáT\x001e\x0007]ç\x0012\x0001
ß\x0008Ã-\x0016Ón2ÖI\x0007B\x0018	J\x001fT\x0010r?ái×Ä¥ê1øÆ+@,oÌ÷D\x0018îtO \x0007µµö+Âü¥W{!\x000c¾ûwrÇ\x0010\x001e\x001c?2&3\x0000Ðd](÷\x0004\x0008ïºI\x000f;/Sñ"\x0000Æa\x00160_de÷D\x0018îtO<®\x000bÐ4âÉ$ãÛ)¨Ã=\x0011K"']\x0014XÍÐf\x0019f\x0011ê=yÖ:xÕzg-Eö¬Åóø6aì	óû1ÉÐf£'Ý\x0013k\x0008áÌS;A \x0008\x0005&Àç¿bî\x0014æ	ÿ1É2\x000büÔ\x0017"
Þì37j¬Ú3&\x001dtÙ\x0014¤*0È
a\x0007\x001aó½\x0005nTÕT©ÆÖ¾\x0014¿Áá)ävO>­Hõ·`¯'s®,6ÝsãV&{o\x001f?qNÄ¡\x0014mÂÞ:\x0008&J£Mûá\x0014\x00129åTy*Ê
Yø¹ì7·{¨Ø`\x0012Îç´{\x0004ãø1¾\x0008
Î§¦GÙÇF\x0018léçT.\x00158A Ö¦É\x0005SHIz~_.%~w;õ»T¨\x0000\x0017§q¼ïdÒ©:l\x000f IvêWiôn: ä{\x0018«r<`fú×÷2×8]\x001e¼Y>>Þ~yÙÌ\x0004)*\x000e#Ô³§K#\Qèà¡¯\x0002ÉÅÅÅÉ¥u\x0015FJ_´`píÒ,Áâs\x00150 ö9a(m6`\x0017«\x0018ðõáW8l0lIÙiÇÓ´ß \x000eM©\x001d-îãÐîÙ}ü­ü*7\x0007Gw\x000fO1GM<O\x0005¢¿I0.Í&\x000fq\x000cÏ2²83§Ç\x0007G§ç1MMd2\x0015\x001a~©o\x0006í?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=º\½8Û=P[t\x0011t±Î\x0004n\x0002\x000bUaS®³TÚù	ï\x0011£\x001fÏ °jèÇsöØ\x0017$\x001fWdÅ\x001b\x0011\x001eÇ\x0013?ÿãý?löÇ\x000c~}þ|}ÿ6¡=½¾û<É±DõD'5¦8-ª¢d\x001d ®ÅÕzÐ\x0016ëìÅÓ7O¡Ótzù:ù»SÕúvëävÓÉ«õo÷ûÜZm¨\x0005l²Vî¸\x0000\x0019£77\x000f®V/_¿ÙíkW
\x0003§=?&qHÁ\x0017iRd	Ö\x000c"¬e\x0019\x000f
\x0015ì
\x001bÝÄÏú·¸5\x001cgß®oï÷ùùé@
G±\x0014¸*$xg¡¥@"ZåÓ?øBOW\x0017oF\x001f\x001b¢Ñ>\x0019EÔ.`Þ;:yËzU\x0010]*ÊþAA½\x0006~MD±{WäÅ²êe¬®j pÞÃ«Æ&³¸\x001a¸\x0006*_HÈH
Ê\x0003zXàj'³\x0004Ë½P®¹\x0007|\x0007\x0006Ak\x000fKÎcÎ¢j¸¢¦g`1\x0014©y$§º\x0005Éª~*KÚ\x0004X
­Âm\x0019\x0017mY'C\x000coy{X\x001a&²@P\x0011ÍV3\x0008Å#Ëòn\x0014^(R¼³Yù\x0013'³hÉ\x0002a>PON´\x001cæ~\x001f1,YGÈ°À¯,Éù¡ZÚt(¦Ü¼¦Å<<rõ° \x0016=Ýê*\x00059}»²i%¯£a\x001e\x0016Ä£§]È*\x001a\x0017ÞÌ\x0002á\x001f\x001a\x0010Ôt\x0016càØ©\x001fIáND©o\
ïÒBò,£\x0007³aPR\x001f\x0013Wµp¸E,î\n¶0¶êw¸/a\x0010AË)\x001d´\x000ci/xSÊqàéypD\x0007\x000c¶ü82\x0008Y\x0014tâÒeÊ(/+Ë ²ÓÁ\x0006pù1q]'·n	
ð7óºv§\x001c\¨tÀ ËQ~L¿è±N0Áxøuå\x0000ù;HÅØ\x000f£íßïu¾h8#\x001eßÝÞß}^¸¾\x001bO	èêK·o\x0001}®\x0000\x0015²î\x0005`Áw\x0017o._¬^¤Åo\x001fÅ¦\ú
Áù}0,a\x001d£\x000ceByã,\x0015Õz5PiÌØ§;Gf\x001b¤ÔÒBün*\x000b\x0003Ì\x000b£br/\x0007%%Ä²kP>(oÔ-¾\x0012¬]~§#Üí\x001e\x0011[T>\x001bWuó\x0007rÎÓ¦{é<<¿¥cÛÅn
Û÷áþ«2àÀ´×\x000f{\x0001¾Ê`ëÑãÊ¶\x0014K1*z#õ[\x0014·@¯ô±Î*¯òØêld\x0016©·î\x001f!.u>?i F¼	UÛ\x0001åZ,\x0008Éý5ô f°ýû]ÓiCw-ÑE¤pøÎ\x0017c1Rûìhbd¢\ÎºNà\x001dD¥Ý\x001fBä6\x0014¦&êäVCp©z|Ù¾4<ä@8L#\x0006`'MVGè ±hEgi|BmÓQû±»a!G'QÖÕîúb\x001bÜètÎ<«YíÅ
uhúpwc»fµ/±fUPP?Z û$\x001bõ²)¥S»&µÏ\x0019-\x0019ÈÒ^hìàB¼\x0013\x0008*=seµ³T$iÍ\x0017â¸ÑYDë\x0001Ý54oùÚyR\x0013H³Hð\x0010ÅÁÑ¢\x00087]]ó:Í,¼ômm\x0017g£\f\x001b!»_Ó×~:ePè\x0000cä¨ò\x000cT!:ypk\x0011º¾Y©nÍi\x0015\x0014\x0003Ç7ãK\x0002k\x0006\x001eD(èÙa-\x000fOúû)ïÄ:©ýÀ)éÃAæë1DVid&uÏz,3\x0001í0Ý®(½ë±DHã¢F\x001f\x0002äÄÆ4.ãIVÃõ\x0018"TùQ/'m=ÓGkùîß°lÙÃÝs=(wuÇ7<DT\x0000\x001f\x0018T\x0002u\x0012¥íÞumù%LXÆÈX7ÆHóÂ\x000f¬N¢d7\i4\x001c\x0007Ò67,/	¢As'\x0011ô6ûL£å
=ÌkG+Mº},4EØ}ð«Ã\x0014Ñ´ö²¶ÓÒ}¢a0³\x0013'Ùi×c«­\x0014úÐ>Æ\x0014\x0000RÜ4máÉ\x0003¹¾Ï4ª|PË'\x000fYT0!²×8\x0010î$J3Ð÷ùDûéäd+òª¢µÚãN¢d|OÜ\x000eÊhE>#ö°3¸òë¤I&È÷!ã\x0002\x0017\x0003h­9k,ùm¼èÝR¢d|\x0019B\x0010\x000c#\x000fK\x001a¢ºáÛAÎd'Qúà¾Ç\x000c\x00194ñ\x0017\x000b%(¸;®uCÙÝ> ôMì±BèÉçWY\x000fgéSò,\x001aæÖu\x0012¥\x0011ö]N#zøºÌ(mÚØ:\x0016:i\x0008ù®¨Lúk59i"pTTÁ]æ\x0013!$\x001cº¯Ú¢\x000e³i¿7µZÕÆ\x001aMB×ùU\x0015Y\x001cÊµ"B\x0011C!ÒëöN¢dB1B/o\x000e\x0013©¢\x0001¿=¯Ý°]'Q2D¡Ë\x0018)Ï·.º$ß1ª_Í\x000f*F:!
]Æ(ù>V/}Ò4Õo\\x0014¼\x0012µ²gjkÊNPé4\x0014¨øÈÔ\x001a¼(\x0016­4Y: öLlh¢x*EñbÙd\x0013%\x0017\x0013ÇÁ%b'\x0012DÛe\x001b¢½@\x001c¶¨88>hÇíM­\x0018v"¡¶Söø!¤óóc3	-¤\x001c¤	t"¡¦Sö¬ÿ,×IåbA åxµI¿hµÉÜ÷Uö\x0018\x0000øÕ\.8«>\x001dF\x0016\x0012ÒüeÏî\x0003,Õ¸ZÃ¯]=\eÇ4\x0000X~L'xîfo£õVÊ§­m!\x0011Ê"eÏö¯£à<\x0002´+ \x0001\x0006\x001dÂfû_©ün¸¥¬a£D\x001dM²\x0015iáFæT~t iê¹"PJM£d$]<Æ¶DþT~t\x0010Õ¤B<&\x0007@*É3îí$ÂjS]¾62RLõl#R±z¶Ë,7©ò£Ã\x0005È¹Ûå<¢êý2õL;¸»îDÂzS½î¶g?©Ö\x001bË Öûe\x001f\x000e©UùÑåp+UC~>\­½sbÙ^\x0004«üè:$q,Ân¾\x001b\x0014ÁÉu[æ)Á¤åGÃ-Yv\x00026\ãêäöËn\x001f¤ÎMá»Â#&rsumDi\x0008A\x0015iY¤VÂÊæG×q[qx½¶6ÎÕøúÂõ\x0006müè@$L;#\x0012\x00053¬¨{µS	[÷\x0005I6WØTç\x000en¾×ímHTÊ\x000eP§vTÔµ\x0008\x000ep(rQ°V¢ =?º¦6\x0007G«ZIúÓ2\x0016ú$¸\x0000}¹+Ò"H[\x0016[Ü8\x0000¾.¶Aî\\x001f\x0012òVd_ò\x0013\\x0003Q¢^öh7Ë´ì³A¬&?¦\x0013	Á·Y¹òb¶¢:%CÅÅ>$¤AÈ®\\x0008ôß¡Ô\x0003£k­¯5óE\x0002\x0012Û¿ß\x0005%\x0011®}Ù\x0010vã$'.Ðææä&&¹ìÃ!wAöåCM¨D°túp,eÙ$dBÈ¾t\x0008aø³©\x0018K\x0007¥ÄÃ>ÒPM¬\x0013\x0008;íÚÙLà\x0012
-EÝGl¬\x0007¶S'\x0012v¶®\x0004u*A-s~tÜ!Åz1\x001a¸u4µ²ÞÉe6É \x00140?:\x000c·9¦«H\x0006\x0014!I.Ùv\x000b\x000f\x0016NV~tR@\x0010'7\x001bÚ_ÛÎJ\x0018ó?üþ\x000bd\$Æ'?®ï¾}\ïÞ ~¢¨uõE:Å\x0007ÍkMéàÓÕåëïWç[	¾ü(
µù1\x0011\x00052T\x001c\x001d5\\x0008F)2*÷b
º6<&Â¤Á ~=1Ry`\x0004·ÚVzà:öÀ ²
0NÕúq«)x\x001ct¨ò±ÃÖF=0(mÃc"\x000cv0\x0012Õ:\x0019ä_sõxT\x000fgp\x000f\x000cjÛð:25å\x0019ÉÑÀpOéA¿\x0005µmxLeÔï -%WU¢Âf1
*µ{`¶ÇÔ¯TuE¢§¢\x001cFO<eÔ ¸ß\x0003ê6<&Â¤¿RùªK+[[.WRràôôÀ ¼ML·x:Ë\x0017-fKù¨Ð\x000bg\x00181ð/:`p#\x001f\x0013aÊæW»ú\x0014\x0007`e\x001cä ÷À K\x0002\x001e\x0013apXü.\x0014ûr4gâ9ã\x00077ø=00À²Ã\x0000[\x0002	áH\x0016"¤³\x000e\x000b+»A´¼\x0007\x0006\x0006Xv\x0018`Ïêâé_®0!Ô­iàmõÀÀ\x0000Ë\x000e\x0003ìªÔJäK²´´¹+«\x001aÊyöÀÀ\x0000Ëé\x0006ØÊ\x001cÎ0è¦ÝC\x001ajè\x001a÷ÀÀ\x0002Ëé\x00168­çº\x001bHº«K0ì\x0014+=È£î\x0005Ó-°\x000eY2,°£Ù\x0018à\x0005\x000b\x001bê!ù1\x0011\x0005W4.HÁg	8®tQr3£T~L]Ø»[Â¡¦Â\x001a¡8vfæOß¸Ê4\x0018X\x0013é]9Mâd>xNRjpú­0E'm\x0017	®ÑäÇÔoÄ½sÒ¶$C oÄLJ\x000c\x0002ñ%9ù¹¤Ç\x0017wÇáá\x001ei\x0014§p*1¸`Ú\x000bó»5â×OøF\x0008PæÇy\x0016%ù°§îÏ¡¥Ö»z\x0016{å#÷\x001c\x001dfÚ\x0017-ç»a¾\;õ9O\x0018TÑâq²~ÆeTÇÆ\x0010©i¸L\x0006&­ªâä9\x0013	Æ[3¸8Y¤ÙV}\x0000ó6ø·\x001f¾äª:´ÍÌ,w·F¿PVÞ(Û£GÐ4@4O¢\x0018øw'«Ëó)\x0010è\x0015n¦@ÈtæÃ¬OçëXjâå+¶8¸\x000c®àv\x0012Dúk¸VÅùÀ\x001dî\x0011(\x0010!\x000cNG\x0013)\x000cN2ù1\x0005C\x001aú .¹.t®µ'øA\x0006ÄT
Dóòc\x0002×SmÔ\u\x0011¸Aoúî\x001b/_ÞÞÛ?¼´l\x0013ÉÝÍzE8»ÑC%<\x001dè#\x0017\x0011)3Ôa:=J8g«)@H\x0006Í©@!XNwHs.;çb=-\x0006y3}<¸êÈÊgSyæ ¾À%^1³.Æª¢;óí\x0003B,\x0008É@HJµt\x0002ð\x0014Û}?ì×Ý\x0003TÐü\x000c¤#§
Á
/'a\x0014\x0002\x0006å\x001f}@Ó¡cN{~\x0006ò§Pò0ééá¹º\x000f\x0008áû\\x0000>\x0015HÕ¬kÆÅ·³/\x0014´\x001cÈûô\x0001!ZÇô\x0011²¬\x001f\x0003¥3MsH²4´Ã6f]@ã1\x001dHæèC^õÜÈ5\x0001IÃË~ØN½\x000b\x0008ÀxL\x00062&·[Ê@,\x001dàÔ}-\x0006Ç> ØÅÐa\x0017½¬ÕÐÎÅ%·%T\f¨QÍ\x001fÓ'µ®\x0008-øìd}ëA¼\x000f\x00081t\x0018F\x0017«ð:Ô×(\x001cl
÷\x000eÈÍ4\x0016\x0000A­$?¦\x0003\x0005êÂÿ\x0014&\x0000Õ\x0011\x001afvñÀ\x000cÅ\x000e3½î5Ó¤.gØëù\x0012QÙaì. Ü"â1yçÀ!¾X:f*ïàù2AaÇµ.\x001eÅØa\x0016¬\x0005$pñK\x0003ä9`\x0010\x001bîÁQEµ¯gÛHÞ*]ú¦\x0013<Gñ­«á5?ìÇÜ\x0001d°>ócº/¤²Ô\x0017Eµ$»\x001e±NèÁía\x000fÅa"?&®¹zØX\x0003í«,¤ å¢	m¡ä\x001fÓW¼¨ª´¸\x001e+<:Ôñ\x0019M&ð ?¼ý:Y\x001aDå®\x000b'·_¿ÝÓ =_l"\x0004¥x äk6\x000eW\x000c5rN.®^_ì¹þø«ÿ\x000b\x0002é41«¯G§ïn?]ïÑSÙ¿¤­å'¸a¥Ja¸âüôêèôä"ý×\x0014ôoG×$/â\x001cGÁQ¼ÔÍ#ýf;p$jMóc2Ê­Ì3\x000fJþBr\x0011Ø\x0018>âoôðÀÎÍ'òHsLfº(9Ei¹TPak¥. ì^¹íòT uæÁ£\x0004%Èè\x001d\x0012;p,\x0012»¬éú^MO:ß²dJò\x000f¸2G=\x0012ñÚ\x000bô÷?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=;¿\7\x0011¶n©÷²!êþèá»ë¿n\x0002mdINÈtbÞr\x0005«¥Ë£OO\x001f¯â-\x000bØv¢\x0013o8äH±]xJ¹û,¬6¯sÒ</p><p>WUpU'\Gc<Ä>xáñ\B®ÕþôU¼Þ\x001eô\x0019{\x001bûËØíÑÕûû­±\x001b·9£\x0016\x0005p\x0014¶(\x0012\x001cÔ¯7ÄnN_.Çn´±þ6¶\x0011·`\x0008\x000f|¸$õ\x0002IJ¤Í·wÀV¶­ì\x0000lnR8|v8m\x001f\x00028b1Vï¸Ü<4àvc¸±\x0019	º22n#,ý\x001eë\x001dÜjÌ\x0014\x000c\x0007ú/ä9^\x00001ÃÆ\x000e*\x0010GÂÈ\x0013B:$\x0018\x001cåfe³\x0007wîy\x0001\x000cK¬Mî a\x0015²¥\x0005éQ\x000cñÃ½äíÏ×\x001b£üØ\x0001ãô+\x001cåÈ£"\x0005Éðy&²}'ÜNWYó\x0013vYacØÚÑ vÇ¢è¦=\x0016»°</p><p>»\x0019ÂÎ%]å¸î)«\x0006Ä}V(µ\x000b{!\x0018°;>´îFe¢8 WO\x0013é®\x0000\x0012È$öÁ®S©¬ î\x0015ºwªMÿÛû»÷W7·\x001b«\x000e\\x0008dðPÜ£~c$Ü.-:L¥éÿq~yñüäì|¡ôÀ'þ\x000e\x0000^Ów´\x0002\x000f\x0017[d\x0001òCà|¢;Zï!Ù\x0000ssÐÙ\x001f\x0002\x000b_F(Oî®ßoõ \x0008B*¦¼ »"\x0017$1\x0016/\x0007\x0018£<¹8}¾ØK Ë</p><p>²ìÆ,²¨UºåqÚ!\x0001'5Âh\x0014ò\x001bæRQNÌá\x000f\x000fb;`+\x001aTTQ~[CcZtßÒÒ¼\¸×ÌÖ(?Gv\x00000w~'Ðùýu\x0000Åû¡\x0016à,E<\x000bø[;ùåúGÐº{útcEÀª\\x000c!Bñ\x0016!3)Ôl6ôY\x0019|ÚÉ³Óï@ô.ü'.$CYýuÚ3Ò èü\x0000©\x000bôdá(É¤&r6Óµ­G\x001bÁ\x0016ÁF\x0000\x001b/=hm&NbÔîïi4ÙÙ\x000cy\x001bÖ"\x0004
XãÄÅWÅ³¡ üX·\x0016? «\x001foßm­*IÜNá\x0012\x000cÝN*ªÿ¸pB¬Ì±\x0002tòêÕùÓ)½A¿\x001cÀç¬ÏÙ0~MYÅðÙáø©Z\x0012e;ñ«</p><p>¿\x001aÆo`â7á·ÐJðëíº\x000f¿¨Ö_¯¿Ë'5gÈ \x001aðÓíÅ©Y\x0015NüÕö\x0017ãûb1áúØZÄïÆDÍR$ôá/d
àóµ£ø
§é\x0015%Y"3	øI4:\x0004¦³yÉ>üNø\x0018ÅïÌ±Åý3U\x0005Â§`(>e{á\x0017"jjFOÿüÝÛÛ`Á
5ú)X|M^Ö=[róÏ>:ÿn\x001d¤+Aº\x000ecô\x0014@2ÚÖÜ¦£s{ÀäÕZòÅ\x0014\x000c®ßÄÆq~\x0016Wr^Ï^«\x001a`Ú</p><p>¦í)HËZYüÚ\x0001§(`Sª£Qªx4Fo®ï·\x0012áEäiTC\x0003{3ð\x001c¡~\x0019!åóÓôôñÙé%\x0010à¯b\x0015\x0015VÑ\x0015ä\x001a5Æ\x001e¹eÖZC_'õlÁZtl\x0004¬qÜ¿\x001d«±\x0013VMÙÖ8:çølÚ¥	«¬ÖUv®ëDqÌ4ÔRÒ\x001e b6ô{\x000fAuòàëw2~ýeÞöåÕo·¿_Ýý¸Qç×e¥41¦0¥¤tb\x001cÂ]OÝ¾<y}þçï^®¢/â þ°8Ñ^\x0013»n¸ïQ\x000f¢\x0018h\x000cÛ\x0015|Q¸\x0002\x00031\x0006>b\x0012Uj}æC"óDêM1Ð«Ã4´!Üýê§Ük\x0002\x0019®)E\x000b\x0019X¥\x000fgÃñ.ÄTz6|\x0000ä'Or³	¤¸\x0016÷¼:(Áÿ((Á@·0/JÊ\x0008ô¸ó4ª3?1Ð½Zv5¶ì@>â\x000bPÌpix7\x001cÜèbÔ¼²q\x001bvò5¢hé``	\x000e®ßs#±¨VÛ<MÀSë\x000c0t´l#©ÃE8_.\x0017FB\x001cÔ\x0013ÓÜôÝO\x001b]»æ\x0002*¶\x0011ºud,EÙlR¬ajúâÉ"ðXá*(Q~p(ùË¯ï¶¶±Im³Â#Pj`ÁPrÔÙôy%ñøìÅÓÓ\x0010\x001fa\x000b[ÂþDXµ\x0005wXc"De</p><p>µ¨\\x0008\x00002;ç¬{\x001bnSGý\x0010¤¹\x001aöý»ÍUPÉ\x000eäxP\x000bÉK=U·(^>}µàÊ\x0011rAá\x001a \x000bÙYg®bÐ.cX¹Ë\x001fV·4ðoÄl*Ì¦©#\x0008¤âÒ\x0000\x0010¯'ÎÖ\x0011ËCï'\x0019õfö4fz¸	¦F\x0015>&2ÿ§ÆL¾A93ue. N×b2	¨ý\x000e»IãQ³U¼À\x0018\x00042i¼C\x001fs$TDîçä¬BlÝQ\x001a\x000f\x001bP/XÃ?E_°Aü"_\x001e²ÀÄ\x0013ñ\x000b¢\x000c\x0001ùÂU\x0017~Wáÿ¤·\x0015¿£~\x0010\x0005c*ðÓ¥RÌ\x000eÑwâ/\x0018wð\x001a4_ºdú\x0014ÿ,h#ü7É*Gÿ0ü\x0001rô\x0011Ú\x0011@;</p><p>F$h\x001b»P=Ðæ§á<rÐ\x0005@³JÎ\x0005çñoGð·£3¨/Áß®îÞ^ÿú FË/ÑÂc?^¸\x001cc\x001buðãÒy´ÒFÌ</p><p>\x001b-ÃÕþ;ÁïÕ}\Þp\x000fÿs\x0006¢KP Dw"Ó\x001eÁ=¹¾û%üò§\x000f÷wº¸~û\x001e\x0000ê\x0010tHÜ\x000bÀZÚmB\x0008Ë0åd¼*Fx^<\x000b¿üéååÅ.N?{p\x0006KP¤£¹«BT\x0003ÿêC*ô±	i\x0016cl\x0006Ri´hð\x001e\x0005</p><p>a#ü«\x000f(7(Î¢#H\x0004É\x0001¨BápÀ\x0014\x0001õ Rßz\x0010ôAenVá²B\x0006\x0002\x0004\x0015Í}PÍoâÝÛb>\x0004GõÛýõvÌi PÊÛ\x0014\x000f{£-wbéÕ?\x0004\x001fõúr¦?¦\x0018^èhU</p><p>~`/]»aô\x0012GDa\x001ahi\x001d[\x0010\x0006¡¾BâÝÿ~ã\x001cö\x0012Ä\x000e³p\x000f½»}÷6C\x0004:,¾\x0002i\x0000ú"#\x0015:wkd©ûÌn\x000cwÐó§3}Ù%ÆX\x0004?¾>Vÿ¨ÿz\x001d\x000f}\x0000	ÙÙû»XvßÑð
\x0005<µqèC§Î§\x0010\x001f]^¼/½×\x0010©ð¯\x000e´d´N¡è$=çH%	½úz\x001fÐç\x0016{ÝÚ1Z¢Q
 ]R\x001b</p><p>ëèQÿÃ1£vÂ\x0008sZ¶o\x001ds*Ak'´5¼k\x001cö\x000c½Ýé]Ã¤H\x0016ù×\x0011æÏ]×:\x001aÆPf[k\x001a\x000fûQbjÃ±Åèb;Ä¨
\x0004b¿Þuÿöÿ«\x0003ù¿õÛ»ßßÇK]ØØð¯3Èon®~j8
!\x0013Zãu¸1\x0000!\x0005ÐÙZõ\x0015\x0017sÂKOÈÏÎNÌ\x001f\x0013N\x0008¡¤ìÄ\x0019¢²äÈbÇ"¡Ô>£,Ôp\x0006QB\x0017ü«\x000f%	%@È(û\x0003N#RºÊz¿ÛbÂé[LÏ\x00126i\x0011&­\x0003L¹\x001c7àò§í[NÏ8éokhâ²&át\x0014«ykv[Oòê}ëIj|\x001a</p><p>«Qt\x0018ÖSegÏ\x0006S×÷oþ\x0017f@bÞãá¿þù·ë÷Wï·_r\x0017\x001e&Åã%G©Ä8\x0003\x001cèéö`*©ÏE¾9}~27\x0016\bdäø£\x0003¤³\x000csJ w·[á
îMàÏ\x001fBùËï·ÿõ·ÛlÁ«\x001an>Ã4ëäLø¯\x0014²¯¥</p><p>^Ì*3×\x0018Ó=ì+ÄxÅÒ´S.\x000b8\x0016ªÔ¸ýøîÃD9rs}ôâ\x00063Ñ[?¦ðÖ5\x0005rÈ\x0011Ï4Èìb@\ÖV>üüÕÓ/\x0013çHø°^Í³\x0005\x0014V¤Æt²\x0002úÒG­°ù$ÐáÕÉÅ:ó\x0015Á</p><p>³x;ê²ÂUV¸q+8WÁÑEz`°ÂÃÞIVh¹\x0014ÃôYXzÈ</p><p>¸\x001a}\x0017 \x0018É³\x0015*E\x000fÎ9º\x0006jµÜé±3VZ\x0001Ã/ChäW	7E7Eí©\x0015ÆÐ}÷\x000f\x0003Uê&3Æ¿o\x000eÜähFâFL{Ê\x0019%Åà^fðúmð\x001dÞ\x0006hb\x0019|\x001b&ùÀ\x000c<óÃÛØýËà©ª­âÊðjH\x001bÉÉKyIoh^[<%ú¬Pµ\x0015j\x0007+\x001cÎ\x000f-¥S§R0C1Kfì÷}\x0003Q?æ\x001f§?@&\x0012Y·</p><p>ÒÂ\x0006çü±ÁèQÛTg`\x0008¢gbé\x001d ÛÖ2{a;ï¡\x001b¶P?p¯0TÓ@¢¢s#é~ËÕR¦ \x0015·ä%nÉ\x0016Ü\x001d\x000b¼¥4Å\x0005\x0017®?ËVä9BJ;Å"çÜ§©\x001aùÒFo\x0005nª%7cKNCñ$q¯pK\x0017c·X]kF^-¹\x0019[r</p><p>ÂZý.Ò\x0010­Y¸Ûí¹Ë]µänhÉ­Ç	\x0010
Ã\x0014\x000cÝ</p><p>g´äf1vkEîE\x001cX±ú\x001b\x0018¬´´<1\x00001\x001dÜ9Gàí\x0008óÊ!ÂãÈsäÑ\x000e±¡DöXF´^}¶yâfs\x0013t\x0015â}YP?¦Bý«ûÆ\x0013z\x0005²öB\x001a:´YÊ²eÞÇT±qry¶jç¥\x0005\x0015!g\x0005Â\x0003\x0005S¼u)vl\x0005Æ3,ðf)Dî² z\x0007~ø\x001d07½\x0003:\x000b\x0019üYÑ;P\x001bvP\x0005<éf\x0005ð8hö°òñ%$]êhµ\x0014\x0018Ø-.³É\x0004Ym#.÷Y¼h\x0002ÓIÆ\x0007L ²ÌÎ&ÈÚáäXÄ·\x0010BûÿaÔÎâ ¡e÷où7ï>\x001c|Ïð!;Â?r« ø)õ\x0010{Òu\x0011r7{\x0019áÄ´Â&\x0010Höþèæê>Øpòþãí»÷×GOîßÝ4
 ÉEµ\x0001²àQ\x0005Õ0ôb
\x0003:-\x001f\\x0006SN¿:úüôèÉåÓ³åc"Ù#Yid;Ù\x0013®R¢=\x0002\x000bÚØÉS¹ÅczÀ\x001eQÙ#v²'\f\x001ahÓ$¶à`£\Wøæ\x0017ë~{Tõ~ÔnïÇMïÇ'fBx?v[ýqÀ\x001e­J{@y|\x0017{Â\x0015\x0013¯\x0010àÐðd4Þä\x0002¿Z<ÛûíI}dñ{í7¼Z\x000b/\x0016\x001a?Bt·èØúí±Õ~³{í7-qz&ØC\x0003ÚN[\x001eûíq=n7{¨\x0002Á|"Ô\x0002{\x0014Ï±ä²§:Ü^çR¹\x001fA\x001aJ\x0019kèÞ~¡ýæleÝëýðc</p><p>õ\x0015h[Å×Ã(sÉ¾7(\x0002~\x0001ÿ.Ö0Jaj%±ì\x0019Ì±ÂdU¯~{¦BE´'\x0016*v1È0äñÕÒ\x0017¿\x001eß\x000f_?ûíáÕ×µzí±\x0006\x0006LR;Jô¨Ð(Ãs/!ÿ2î ü^\x0019\x0004Y]\x000c\x0002ígô×V\x001fc\x000f¹@É¿LxÀuå\x000eàq\x000f{|ø§\x001d\x0014¿i¯)Þ±VÓ\x000bR~wÿ&\x0012iØd`G"ßx]ÝÝàÄæò·FþLhPN3M\x0010JÓ{aÜmHN\x001e=;¹8³\x0012kè
+Ñ\x0003§à\x0008úðà¡\x0019ù\x0010\x0013xÌ
Ö»åwÐ\x0002^\x001f¤¨N)ê4\x0001\x0007´mw·»ºû±\x0001<¨Ñà'.\x001d~\x0011!þ\x0017ù\Ù?üüù«ó¿\ÌðØU]a\x000fÑ>ÃóCÊ4\x000fÄ Ù=\x0017kþ¶
}q¨éPïE\x001fb{µ8Kì$\x0001½È]vq°¡\x0019ýTÖècY{\x0004¾&þR­@Â\x0017[VÔt\x0015\x0016k¾t+üÔ"!¦\x001b0Ó\x000fD¥×þèêîn{jÜ9X9õtª¹\x001c´sëÂB^óäâb¡Y\x0017W]®º\x0003À` A×r½NúTßpb±JÐ'\x0004Bzû¡o</p><p>@(TcV]h»äj±jÕ¹\x0019ZvûÅ*MI,¯pTØ	·\x00185´"\x0017¬B\x000e#È\x0015ÍLBKnîf²À{½[o\x0000/ÓW:¡¬ôüö÷È4°9sèsfÊp´Ñ@Ð¼\®%qÃççSû) \x001b]B6º\x001b2¨J`²Ó\x0018ú8Cti\x0008³\7`æõu^Õ×Ahøêc\x0008#o[\S\x001a#ì\x0012JËÈÅy\x001cÂ<úþäU\x0008\x001fç¸\x0003Ü7,Ñ0ræ\x000fÁ¯\x0007_þäîêýG\x000fo¡%¦a{OïX¦L¹Q\x000ex å\x001fvµ!_n|ùçß\x001d=<^W3Ìâ7?þöëïÿýÃ4wvuF°\x0001¢OsÀ¢\x0003þñúO¯~¾¿{÷Ó{\x001c\x0006VaY*M+æÀó\x0007áü\x0004Ý³°Æ!úÕÜ\x001cj\x001a~wú§Wß_^<}ò\x001c¢Â³£4ýùµ­a}f¾\x0001áä¾~Ð8\x0017çzp&\x001bq¶ M8E¸â ÎC.\x00010·ÓûÚ\x0003Në)íqé\x0010¦>T
l)>Üýúþ#È \x0010\x001a@÷£;YÞ\x0008ÔJaÒÈº\x0012@·</p><p>d?Ç\x001eÄ"tD\x001aÀò{\x0007Iùå\x0012©Ü`üÑ\x0014úHç¨°\x000eó\x0000©òÒ!ÒO\x0018ýú¡FFø£\x000f*\x0010A¤E\x0015á\x00103	j\x0008à\x0015Aõj7¨Ð\x001fôAUXQU¡MªÂæ¥U]Þ©-Páì?ú¶j8DªÈ[\x0015ØF#T#\x000eéÐ\x0007 \x0006L\x000fâ¾Uõ&ÉLÁ\x0006PÐ¾\x0000P
áâªªýV\x0015J¾ñG\x0017T#Ml\x0002¤\x0012\x001a¥"ÒÈ±\x001eÒ¯ô#u\x0010cÆ\x001f_ýûwpÙ?:\x0017U¥»YX>/ °VU"T%}Õÿ²¿¿{\x001bùl\x0019¤ïnïÿÖpLY\x0006C¥\x0011'\x000f×E 	\x000cçÙ¾tNUÃ38¿;¿üËü9UÀÆ\x001aap½BÊµ \x00000m,CGv%:i	\x0003¦½«Éñ«çP-\x0007ï\x0000Óy¦\x0011¦ðf7\x00189w­¦N¦\x0000ÓyÐ>K«é%Áäv7á\x000bÒ}«ÉLù¼ðÒYT\x000f{3\x000eFRí·\x0018àw®¦áøÒyòJq5io~¢9\x0000\x0013
\x0006`</p><p>©</p><p>ô¥\x000b³ß'÷¾/\x001d½\x00116f~ãþ´´\x001fc¾ôìLËqcÚØÍ
Î=f#\x0010¦ÚÍiÂ1Á;;´âF>"ðÓ\x001bKNS¯ìa\x0007§»ïóÄÎ\x001c`:\x0003LøÖqg:vÈÞóý_yà®\x0004Åøãìú\x0008Dbjd#ÐpèÞA\x0013\x0012î"Ð\x000c!¤M~ÓÊOÝ\x000e\x001ezÐ¬\x000cK\x00014*³Æ\x001f_'Ðÿ}õs\x001c.\x0013bO.¾kÂçãÓT¥^RhÌ{2·"]\x0014h5¤\x0011ã@)cå?¾^°oÞÞó7\x001fb¾=f\x001fpe/ï>Üß´5ÌÓmÃ|R¼-Gý[üª=¤ü\x0014ìåÅËËð¿gT\x000b°<þè\x0002«}¸ÏÇ¢i\x0000+\x001cpX\x0002Xnß¸C¶Óy¨sëú_@Bòß?\x0000y70jÅði]½}ußðmÙpóàñÛR"D¥p|\x001fÌ#XÇý!Áó§ßÖÉóç§'«X\x0005\x0015\x001f¤_=V\x0011	d\x0004RÈ|XÕýõß`»*Èâ\x000fØ®\x000f¯î ¹×òq	ÅSÈçµ§oË)ü¶\x000c7|5\x0000xxr\x0001ù½\x0005·õão\x001fþ\x0016\x000f­\x0018ê³´°TBÙb?Ü8Ã\x0014¯÷òº6,ëJ¬¿T@©`Â4CüÑ\x0003Ó°$\x001c\x00070\x001d4¬D\x000c(å\x0007XAùÓoo7\x001fË\x0010º\x0018\x0016>¹\x000b¿_½¿º9º¡ð¥e3xëS×D_ ï Ý¡­St\x0001P+\x0019´btøä"ü~òüäì(G5ó;äç_?¾±?ÂÒÃ}MU=CÞýv]7ÛK\x0000:Ü¨È£ÎÒñ&%¾ð\x000eEwk;¦ªÕÓ×\x0017ó7\x0001øÕÿóî¿>Ä\x0010PÇ ib;\\x0005\x0013Ï±\x0010\x001bNcgS-x\x0011#ð²Í>\x0011×údÏ@³Ä,ÈðOe?L<õé\x000f\x0015O}d\x000b~x\x001b\x0016ü!Iyn>ð ¶À{ %Jk­$æ\x0007µà5øpÿáyXøKò9(¬æÔÂ*\x0003öHúê=ÊÂµ=Ú#\x0018F\x001bhìf­Ì±;\x0003i14'HEs\x000c¥Å\vð\x0003öøÊ\x001e¿=ZOÛ-¥D{Â« (|vµ\x0007¹ÎÑCEÀ~{<¹*Ï¢Îh²Ç=\){DeøÖíµwÛË½ \x0015î7naì!}?Ù\x001d\x0008¿\x0018Ì
Øã*{ÜNöXú9À\x001e\x0007\x0012#É\x001eÍùBîMW¯Gïõz¬M\x0014ÐàÞ4\x000c\x0010Es¬ { MäËØS¹7½{\x000bw]Û-
à¥ë#£ÏGíí®¯fXzI8	xð)ËÔÅ=<µ\´\x0011o\x000c'ðÔ9Àh¯I)\x0016£°\x0003"KxZ¸\x0014eKDiÉ§¬_=¤½\x0015-Q±m\x0003L\x0011ÀÒLQjùJ×k,Mùß¨ë¥HthYî'ðV0\V~¢JK>å8ê±[ªª0¸¸ôR,6ÒÚ/c.MÑû¢±\x00173§è³\x0017Q61âÄò
 ×\x0014SböùTDþT¼¡\x0000MÌO2e¥]¨×\x0012[Zò)-[%á& Ð}9ì'qÐ\x0015Ëé¥,ç\x001bz-q¥%n\x0017KL¤=¸½°%NSýDº,O¯)¾4Åïb</p><p>p\x0005àîRàÈ¢%qÊ>Y²R>ï´³êtü/¯Ã\x0014/TjWáéc2Ïx­a¡×ú ßå¤÷ZAª;ÚÂ9ÌM`ÔuxÅ¾Ì©Â«£ïrÖC\x0011/EÈÁ\x0014:Þ\,â-*Z;ÙRõ|ÃÞ§\x0012\x00049cLï*®%í1þEâ\x0016^ö|ãÞ\x0006%"³\x000fRéË?êÞÉê´çû\x001c÷^P\x0015"\x0017tbÆÒioÍ\x00179YxuÚó}{\x0013¹\x0000Rd\x001c;\x0005Sª6²;;1sx[1»­¼¾ºAz\x001d\x0000Þ`±\x0014¾@\x001byeF_¿òÞ¶l³×'gHµ\x0003ÿÞu³DiÖ§î¬ß,<ZÁ,\x0013Å£YÚÎÂ©Ðrn¶%K³>õl\x0003fÙ9·\x000eæYÔëÏ\x0004k6[ÍR¥Y:¹M¨\x0012Ñ?\x0014\x00048Õ/¥zÀZ#ëUº´êS×o\x0013Ø¡É@Ò\x001eo\x0006Ìij:àºå0j5Ëf}êû\x0006Ì2IG6}Z´\x0007×È§eK³>½÷\x000c¥P5%-P#$³,úA'¾¤U®´êÓ;ÐU\x000eïtÌp\x000fs-Ñ*Ï<\x0005®ãËåK³>½\x000fõ\x0005¬p¸\x0007\x001e\x001dW\x0012ÍÒüZîð0vt\x0018\x001f}w\x000bCy
ýpôâÝõÝ\x001dô'Ü\½ûsS?a\x001a-\x000bñÃò¢õTN%ÿãç
;úî\x001cFû 'úò\x0008\x0004¦/ gáìäù£ï\x0017*ÒÙ6QÚ&öµÍû$í\x0000¥F\x0003"±\x000b\x000bÜ`Jö\x001a¶vÓ\x00184NÆÉ]³ã\x0003(®Ñ8Þ^¸åÂÉ¸qª4Ník\x001c\x0017]É$\x0015¹bt\x0019áb¹-qØ8]\x001a§wß\x001e³EÂÒk£¤êZgà°e¦´ÌìkY\x0008¦$:\x0013I®_QbRåÎaËliÝ×²pWÁ¶C¦,\x0000ç$])µX»R\x000e\x001açJãÜ¾Æé\x000cÐ«>\x001a'òÕß¬fÇ\x0007ó¥q~ç\x0003ç*\x0006\x000cØ\x001b<àè\x0002mÙõ$EfÓåÌæ^ÆéàJÂméÓ7g½sùøÖ_öãuh²wl"0òçÀ\x001aÞ M)WFøM«"\x0013¾shÂLn³ñ</p><p> vX@5õE­«B\x0013¾ol\x0002zAäñFQååYAaÝZÖjÐº*6áû\x0006'F¨$\x000ea¥Êg\x0001
ì¨òËs¼MøÎÁI._³È¸Æ©üêÔÊ8ê°uU|Âw\x000ePíº§4\x0008Ï¦Ä\x000f3Ô³Z{\x0018´®QøÎAJ\x0008¿°µÒå¡Òéò­\x0005ÿÂW\x0002^\x0005)|ç(ÅÄT\x0008U2[G5V!Å\x00176®</p><p>RøÎQä
«*\x0016øÈ}cf5Á0f¨Â\x0014±obÂu.)\x000c\x0004ñ®Ê`Z/Yç¿p"ª0Eì\x001c¦p\x0013ü\x000cÚË0Í\x0010"vº\x001b°/ýîê\x001cÊÎT\x0016Ìù!Ç¤ð9Aôe?;Q\x0005*bç@ÅÄÆtaé<PÔ# WÛ\x001d\x0006­«\x0002\x0015±s \x0002µ6¼\x001d$ÿRÌtõ«µÃAãª@EìEÉùs \x0016ÎÉ½|ûåAqëª@Eì\x001c¨x\x0008íuZC.,ZKTá`øÂWrþÃ_ë¬ó_ÿ£ÒÎü7µyoþÃÌ»®Í»þ\x000f3ïmmÞÛÿ0ó®jó®þÃÌû±6ïÇÿ\x0004óX\x0000X%üà\x000f1áG\x0014²÷GOîn¹¾iX\x000c"X-ÐÖ¤ÖøH!â2ÓÉâI@4²GO.Î-^\x0005¶²ÀY`¼\x0017\x0014dA\x001a=!\x001e\x0004µcå,ë°@éÒ\x0002¸ÓY`3¿\x0010$Ð\x0002\x001b¢
´@-\x0017m:,p¼´\x0000DY\x0006-°\x0018O]$@¨)Y0í"³´j·z\x0017ámdý1Z <ð(áì41þh·ê°Àêú;\x0018ÞFN \x0005*ÏS\x0004\x000b,ñ*ñåyv\x000b´2¥\x0005ºd\x0011ï² |ªä[Ã·\x000c¿	FÒøTø\x000e\x0016î\x0016\x0013­ëð\x0007¨W"qþÍÕÑãÛ»VmÎÁl+§^JrDBÈÅ\x000b\x0011\x0012ç\x001c=>¿x2O"¡Û\x0012º\x001dnÂ\x001dÿX`j3äärZX¼ípÉ\x0017¿ßVèÅ0®e\x0013xß²\x000b¤eçtÉ\x0006½M\x0003ì­Ð¥(¡\_/tN×0È¨â5L²bÚvÑé4cW\x0015v5]\x0005i\x0010»Ë$
yÒË=3WBÇ\x0001ìÞøcÈ!è4EËi»ûå¿Vð²Úî\\x000eíwï,Æ;\x000c¶¾À\x0011zG\x0010\x0006jGð¦Ú4Ü\x000cíHþO\x0015\x0012\x0005£æi\x000c ·\x0015ñåÒ]+x_o\x001b?´m ï\x001f¹È\x0006ÇÑ¿ïé#¨ ÃãÐÙd2ä­\Q&Ô®gPÕ±</p><p>#àÍÓ\x0002	V\Î\x0011\x000b³ëÂ\x0007ßBÊ¿¥»Ò¿ý&8E«ÄÔ\x0008#|"ó^°}<NÊ4Ó-\x0011äåù$õï¿ÿãä7ÿúgää9:}\x000f×â7M\x0017`\x0007\x001dªH|Ï\x001c}\x0006B)bËÒÈÎstòìáidç9:}\x000eWâK_4KêÒ,©w4ËbñÏ	{ÌpêURY:Ã7°\x0011\eÛÓ&Ç\x0018±E8ll\x000f\x001f:Þ*¹[î\x0001\x0019°	U\x0018§í·ëþ4
\x001bã½<ÌorÀg¿]Sê"ÚU\x0010]í`\x0017ç8UA|_ Dì2KÔ¯Kìûº²\x0017t§\x000b¯HÉÄJ8`ÖD)\x0013Í*Dè÷x[4\x0019\x000eTSüS £\x0019¶ìRµ]jO»£]\x0008S&³~ä×õÅ¼;8Y¢]xÜÏ.`ÏÂÆ# \x0000Èk@96¡¿]¾òðð¸ççÅVy{\x001fÓ\x0014\x001cÙåæÚ\x0001»\x0004«ì</p><p>uûÙ\x0015\x0002=j`ÔÔ\x0004'9ñIöÅ¼¡Ëé@/³ph\x0016WéMa °R\x0010\x0017îrqÀ,/+'ïåNÞHÐ\x001aEJ÷Ì²åõD<¹r»è6K:ÔÏ»ÙeA7ÞdÌaiÁ ]ålPsÀ.`ßÓ®p§aÇ\x000cÉX\x0015ÃÆn¯¨1Å</p><p>¾ÜvÓo\x0004&é2ÌÒ»½0n\x0014\x000bH\x001dlt¾\x0015\x0012%É0-Y_\x0006\x000c\x0013õ±\x001cw4ÌR\x0007:J:.Áçs4l¥Â2b­ß\x0018<ïùÆhNÂH'i\x0018xzcFê/è;r%|ò\x001eW;z{í§Kç9º{MIR£ÇU»l\x000b·­xUÎ\x0015>¸~§\x0007/n®Þ¦üE°ìô§w\x001f2\x0018Âàì@tx¡,Éò¹em\x0017g'R</p><p>ãèôÉÙÓ\x000b)\x000c2@T\x0006a\x0003tl|MySG|PSHÁí2¹{\x0005¾²À\x000f[Àé./rB\x0013ë\x0008wË¬\x0002íð\x0015+áºñ·\x0005¿Ú?j|ÿ(ïçåû¹,Xæï°@U\x0016¨a\x000b¤>\x0016Xöp¢OáÛM°å;P\x0005¦²À|c[HW\x001f°þf>`å\x000fÊ}á\x000f\x000fpäúèÕÝ¿þùÛm\x000b+»Q\\x001cÛtÁ$Hb\x0004j|Ìxx¶¬ÛYÙ_]¾>_ e'øÿ\x0001øÁÞ ×\x000c7Ö%\x0011>\x0015@@­|GðÎ\x0012<< ×aàP\x0018×áx,twPÐ¦tÓfü>BDüð8\x001fd\x0015°½Æ¡\x000caÀO,óÀµ#|i+áÇç\x0011ü</p><p>tÿòK\x0018é>ËÃ\x000c\x00087÷m\x0004«\x0006\x0018­\x000fúRÂ"QùìþèñíýÝûw7MÕ3«gÌ\x0011gcyKÝòòèñùåÅó§gëÀm	Üö\x00037LèÔÏÄ¬wøÁ:Ë\x0017bY/¤\x0011vÑ\x001a\x0011`çÖ®\x0005WãÞy}L\x0011BR\x001eC/Ívà®Ú(nd§Ì=UÁ´¢\x0013Jå\b¸._W-\x001dZ\x0017-\x001d]Ðm\x000cq+-utø|=YÖàh>W#tÎF ûpb=5¸FgqÕ}nF±Ë¹\x001aúÕÝÛë_gq\x001a·\x0018Zrº^\x000c</p><p>ôÈè¨¬09iÁ½ºäª>ò7ç¸Ñí´ä&°Wt¾\x001a¡\x001aº\x0018n\x000cj\x0014\x0006èÔ§</p><p>åkªTûåþóFè²Þ0rhÃ\x0018Úå¼¹ÒDÁÎ½_>@ÛpzÉÍÐ\x000by,&\x001cj¸b¹wcY¤¶\x0011¹¯½¢\x001fñÐ°DD	!zÇ¤4Dï\x0019Nþ\x001d\x001dzÙ±\x0014 O\x001dK]ÐCÎ±l,ó¢KËÆËôÈUåÏ\x001añçÎ«iÖs&WPõþ¼\x0006è¦>\x001a*úÊEm)©	>\V÷\uS¯º\x0019Zu#\x001f9õÙcÙ=»'LÓ)º</p><p>]ÔÐGü"d\x0003\x0005\x0015äw¨o\\x0018JË]N£+~¨\x0014Â?£\x0014òï¿ÿãüî:ZòúÝÍÍUS\~4$j¸#ùG5BåÅò;¨h\x000cÎ/N£]¯,´¼e»Di×!ùî]Vã\x0014ÓZÞª N\x0016ÐwÙÎ)Þn,
;¤ß\x001d3,ÝÅ£aJ\x0010a \x0012û\x00106pº¶\x001b¦JÃ\x000e	x\x000cf*iC<ÐBá@\x0003¼±5\x0016\x0011ÃtiØ!\x0007ïaÒ\x0010·°6Á&IR6øÆüJåvÙ°Ï^\x001e²U¦´êwðuyH(&ÏÁ­VÀÌ\x0015ZµÞ\x001a|]¶4ìwð\x00034\x0013\x0004e[t\x000bÚ«¤CÛp\x001aôM\x001bñjOÓ@yZâ'¦ ¹*&\x000cÖ²U!ß1MØ'ïñf××æ0õ¤ÊÍb\x001cp7ÿ²¦]Õ¦ý\x0007½6]¿6½ïkûÿÉ6{\x0018XÙÏ\x001a${DSJN\x001e\x0013\x000c±KBF(VVe\x000fx¡!\x0001Àª)¢4å3B\x0006=¦xb\x0014\x0006^ZâP\x0014\x001dê\x0010«·hM4\x0018#Kc>#_ÐcÇHÌ¤+é3ÁâHx·1ª4æ3¢\x0005],g a[d\x000ee [¾±ö\x001b£Kc>£UÐe?f>_\x0004§t*å<Ú~än1\x0019\x0013\x0013ñvRÈ4úùFø:ö\x000f=úù_ÿ÷}ÛÈ¤!\x001bl2úà2ÎW¤XñZø:ö
=úþôùÒäI\x0019y_\x0000£6À¬¢D\x001bbÃ|\x001a{lP[r!-6ê5Àã 
 \x001b+ÉØ\x0002F\x00169\x0016Ø2¿D
Å¼(Ø Ù°
\x00018UG\x0018Mÿ©\=ævSr¤Å\x0004k+\x0013¬\x001d6!àé5@±\x0007\x000fªbr¶)\x000bÛbS	N
`©95Ü>©0¨\x000c5 ±-SÇ&èÚ\x0004=nÇ.@\x001bÁÙ?e6\x001c{\x000bE}3`MÐÄØ\x001dßÇ!+Þ3¿,ò\x0019\x001bfjnh«
pã\x0006XHå'\x0003dÖV$äe'ZñûÚ\x0019ùqg\x0004y\x000bø9ô¡§R\x0010Ç¹!V\x0003Dm\x00187À\x001c[<uü5\x0019ß[éo5 vD~Ü\x0011Ð\x0011~\x0002a3y¬hQº%\x0018°ök6 þýø7l£Ê.\x0019­àJó\x0016Ú÷\x0013¨?a?ú	\x001b\x0006ó\x00172\x001ff</p><p>ñO½¤lYø¬Ý</p><p>V}Æ~ÆÁ\x0006"*ÌNI\x0012
´é\x001dØe\x0011\x001e\x001bDmÃè\x001cß\x0003\x0012ØÔ\x0013Þ\x0003õ4ûÐîïAÖ6Æ§Á\x0006O9|«\x0004Å§\x0001º¡÷°³\x0005²~\x000brü-\x0008F\x000cÇÖ:\x001a\x0011ÖBRxÊ6u¨m²!ÜÌ«\
üáAÙÜxvõëõïw·÷-½\x000er\x001bIE\x0013Fî#w¸\x001723£{½â¨;ðìäÅéÃÓRso² \x001c\x0005\x000baÙ>\x001b\x000c(\x0018d¡\x000b'tj1õ2\x000b\x000f»ÜIÒ\x0016#\x0004¥\x0011ð8jf8M\x00140IÕË|.À¬åÎ6bì+Ø`ª6ë\x001e\x001bløG\x0012±\x001cè½\x0003åR4båÒÜa\x0016\x0011Z\x001aÁÃ.`Æ¹dï\x001dÑr9·Ì+ÙaZ!À\x0008«Ì°\x0011&&#L¢Ôó±WlØ{7¹©)\x0012lp±)rÈ\x0006\x0011\#\x001b\x001cÍ×ñ,¼ìÜ¦ùº&#Då]áqÔ\x0008EÚ£Üxz\x001eò$\x0018qcw#\x001c«plÔ\x0008)82aL\x0013\x0008\x001ed°²ÝÝ\x0006_ùWx\x001cµ\x0001\x0018Çðp>%ñ
Vç\x0017±Î£Å\x0008_\x0012~üá°>ÖdñùXÄé1BW»	\x001eGp<ÓÞõL2/È\x0013-
F¸ê¨ónø¨S\SM\x0008DñMHM¼K!äØÂÐd¯ß\x001f}\x0013|ðÇ¬Nºø<ú& /LÛ)j4ÁPYïÀ­¥;¬P\x0007V\x001fØ</p><p>hîødEú(ÔäbíÆ\x0019µ\x0006+«­0ÃþI9ÍKÑ</p><p>ääV\x001a\x0015;ÚÕ_E|\x001e´BKÍÇ<+P{\x0006e«Ìj½»\x0011üÀáÀ\x0003`è \x0004¹Àd\x0004£\x0010P.×y»¬\x0010\x0007V\x000c\x0007ã\x001aÈd¶Âãgá\x000cÚr\x0013I\x0015òÀáØCÌ\x000e­}TV\x0004øh\x0005[©´[ÁUýqÃó¨\x0015\x0005]½e©±\x001d¦h9í(Ë÷þ¸¹ò\x0007V&\x000b,\x000c¡¦áð.rô\x0001ìaô.ä¶Î\x0006+ê\x0010*>\x000f[Áq²Ãkaè¢,ÉdºeñÖ.#ø\x0011ã.Ê±<ØÌpÞ \x0018a$\x0019Á÷·âà´àã§\x0005(ÔiÌÛxò³á\x0014\x0008óÍÛ°\x0005}\x0019\x0018a\x000bþ²ÎHsäH	F8`Ç\x000eFðÁÑi·÷aaí\x0011vØ?<\x0015W'^|\x001e4\x0002Øjð¬âDJ\x0018\x0008N|ö\x001e¢}(FÎ£\x0011õÈyß`\x000fÈ'÷$£Iâp×ÞÏÉP¿îb</p><p>]L¤è0Éæ4\x0014ê@hj½VPjç"\x0011gË¥RRtrÖ,àY\x0016.Z\x0010E/ÆL\x0000zOªöó\x0002%</p><p>\x00055a2·<D×nÐª4\x0001\x001eÇLÐS\x0005x0Q¤\x001cø#2½ñ^&¼IÔ)Syâ!P§ÄòÄëï>\x001e!°\x0017`\x000c¬zü\x000cM9}\x0007lø\x0015å&Ø\x0017§¯¾::Ã§5Üy&-á´^Ü\x001aæ\Ñ\x0007\x0001³H\x0017']Nn4\x0002ç5p>\x0000Ü8¤\x000eÀi²Ûzã+Ee¦£\x0016à2;ÿ¨L\x000cì\x0010D ß\x001aPC£·a4\x001cm¸XJm\x0003.ª\x0015Ç~àÚ¢\x0006\x000fWÎ,M´ÀÌ°#nUãV\x0003¸Ã1+RØæÃ¯\x0016\x001c§º
WËÓèmÀë-.G¶¸Éóa<ìfÈS¨¤;«\x0011¸Ýs§ØÊ\x0019ÂãÀ\x0016\x0017T\x0002b\²\x0006\x0003e#Ø²ÜM\x0013p£\x0008\x001c\x001e¿->Åb\x0011w\x000cÅ¾	Ü\W¸!Hý6p×ëÍ¿õö5î\x000fóÄ]\x001f=ú[9ztÎ'Ü*ïÇM²_+K4\x000b \x0010\x001c¡\\x0011Ml\x0002ntufÂc?pGãþB\x0008NCj\bAÞ\x0000AÊ8ðð3^%ÌD\x0003\x000b·RS(=þûïÿøþúîMÓeÒ¤\x0008\x000fw;Ø\x0002§!Bð¸½¤ÄÑ÷§\x0017\x000fê\x0010¿Ú\x0016yì`cøÃ®áØ ÄD\x001aw÷¹\x0017B-\x000b¢´c×5v=ÝZºÆ	å±m×\x000b$t\x0001þr´Õjú-y¬¼A\x0003 áÙ\x0000H	l1#I\x001a¥üò Y£\x0001\x001c$S</p><p>\x0003âó \x0005!nÄÞ{\x0001\@i\x0007	7éÈÃ´§\x0001I2@ÊA\x0003<³Ä\x001f\x0015V\x0003'²¼Ñ¨\x0011¹.vµÀ\x001eX`-\x0006ü°è?½Át\x000cÐ©ìù\x0011pÉ+\x000f\x0014\x0007
\x0008'\x0017¹ A\x001dÞr¤"\x0005ªí]_ôº¶À:¢?ø+P¼6\x0000\x0007O1CËá\x0014ã(/â\x0016ô</p><p>ôò4Ùf\x000b®x\x001a\x000e-fÃa`vÒ7\x0004\x0012\x001eÚ8\x000e³cÅÊãÔr¹ñ{fÎ¯"JSægÃLúû`6\x001c\x0007j!µ\x0015Õ~[diËühx-@ú¶ÀÇïEdx¶¬ÔÐo*\x001f
o3FCË(Í¹{\x001c
4ê$\x0019ëa Ø`.\x001f
oû`tæÜ	+ÚfÂûÅ££ß\x0018S\x001asÈÓe\x0001i¬èI¢ñN3¼ÿ¢ç®¶$M,\x0010e_\x001cþð \x0014-¿>zqõSËà;\úT\x0004g(Éà±Ú7Âl:\x0008O^<Y\x001aúHÐ\x000bÖVÎË¼\x0003;0ûà-Î&ª¼\x0010[¡°v¹ÀØ</p><p>]ÖÐå\x0018tKuEÁ­:N\x001dá\x0016EI\)onkèvlÕmª°\x0007ä(Á\x000b«î3öÝ×Øý7±Ûc\x0011ÑêÜº$ \x000b£</p><p>ýþèáõ\x000fW¿7Ô¢E¸{¦lr&{®°cÚ¬T²\x0008úåÑÃÓ/Oþ¼Ýñ</p><p>»ãcØÃ§\x0008¹ÅÔxÏ5CÅlx\x0003Ê[áûG\x0003àÃã\x0008|©±«DX/R°í¹!úYãÌ¶[ÿfô¼Z|x\x001cB¯,VoEì\x0000ÐiñÞÚÀtÇð¹2F\x0000?></p>
  
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

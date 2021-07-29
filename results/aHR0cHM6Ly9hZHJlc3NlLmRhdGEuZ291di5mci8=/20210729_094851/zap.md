
# ZAP Scanning Report

Generated on Thu, 29 Jul 2021 09:40:48


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#H3DT`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#H3DT</p>
  
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
  
  
  * Evidence: `<?=ýôñÏwé¯/?}X1`cyÉa¡õÚyn\x000eü¦C\x0003Ï}yúâù÷oÒ__¾xrvÐ\x00063CÍ\x000c\x001bµ¨\x0017\x000fß¡\x00133Ï;LÐÝÆÃ	h¬¡q\x0013tîvIÐ)N6\x0019\x001f£g¤cÙÔÌf\x00033Åg\x000b²1Ü®¹ß×hu¶^rÙÖÌv9)A^ÔFÃ\x0017´\x00084Ë>·}{ÙÕÌn9\x0005
¬:R\sÉç¬¸ø
,vdö5³gVe}÷×që2æÄh£ÏÕ«
B\x001a:l"ÐÉÔ0ëÂ\x000c;\x001et¬ã\x0006á(ïÁ>Hmæ¶å\x0004}¶4l\x000cúðø´\x0015µzQÌ\x000bu´üöþ¥\x0011ÝaÏÖ
R·Æp5ÔÀS¹8¹Ä~ÈÔ®Ûñ2AÝC½Á\x001ej¥Á\x0006
F¦æ&[CýGûQ7öPo0ÚH¡N2)¼|&Ð S\x0007µãY7\x0016Qo0ÉIÒ\x000c\x001dÅG
#\x0004ívnL¢Þ`\x0013uÚâ@\x001b,S{Ñ{ç2óÃÔQÔ\x001b¬bBe\x000bC£©WkeÃônÔYÔ\x001bì"5	\x000buÈ{Å¬ðn[\x0003º»ðj\x0002º1z]L\x001e!\x0006g¹hNSK¨Pí;\x0018¤n\x000c£Þ`\x0019ik\x0003_F¯ø\x0001î¥5t·^SCc\x0019ae46äå³bc\x0002r¨w\x0010h,#l°Æsï»¦¶l\x0010s >[û;HÝ\x0006\x001b,#=~ðetÈ%Ô¸hE®Ï\x000cS7\x00116XF«¤p1ÐÒw¡VEñíxÔa
ÑkM]·Ã[#SûY\x0018hì"l°¦T5\x0007
ÏÅÂ8qÂÙÖAêÆ.Â\x0016»¨Iz[áDS¢>ÛÓ4HÝØEØ`\x0017uà±@ÉÅq*\x0002âÎÔÐ
C7v\x00116ØEÚ\x00169A)
\x0008²5E1g\x001b\x001c\x0007©\x001b»\x0008\x001bìbº¼dÇRò\x0012\x0012ïgÍ±±¸Á.Z';}Ös\x00121n;ù\x0004uc\x0017q]tæR \x000ffÑã¤Í©HlÌ"n0^æ$.Ôb\x0016½8N»¦\x0014°M n0Nñ"Kí»Ç\x0015hAæã%¡>ÛÕ3HÝØEÜ`\x0017-È1/Z\x0016õ22î(\x001eYÄ
f\x0011£tÎy\x000cR¢H[ $ï»£ÖÃÆ,â\x0016³\x0018å×'\x000b)¶\ÉKF<Sç7\x000cÝXEÜ\x0012-\x0006^Ýî¤L´¯B\x0018ü·\x001fuc\x0016qK¸èY¤Âry\x0018ðN¨wx\x0017Hbv4Bqç?|øóíÍÝûIi"l\x0006\x0005p¼â/Åâ^ÚÖ°\x001bkýðäûë«7ß=Ìgj>3ÊçQÒ¤4_&ÖÊ`\x0002×¯^YÍçj>7Êçdu\x0006ê 6<`Yº}Cw\x0000ðj¾Póóã\x0007{\x0005¼\x0012=\x001d\x000cÎq±k~×òU­ýúÐ±\x001e0ØR0C{Ty^¹F)wîÊµÐÞá+\x0002åñ	hs\x0001ÏÐ.Sí¾ò­&lî\x0008\x000c_\x0012ZäÊ4\x0013UÆ#¡Ü\x0012ïz5asK`ø\x0018Y¤!2À©L¥OÿÆfÂæÀðEq(¹2Ú{
re¤ïÏòZOØ4fJ)\x0008Y\x000fªAÂ\x0000\x0000+3e\Yf\x0004³÷±ZåÀ=Ð	NZÃTã$³ÜKï¶íVè?ÌiMYLË\x000f?Þ¼[S~¼¹xùßÿõ×»·?~øùîvÍ
2e8(Mm`ùD\x0019}lN7ÄÿðôêñRòôêâåõ\x000fo\x001e=}ò»7×\x000fs»Ûmâv´3ÁÉþ\x0017Æe±'w't ;C°Ì±\x00112\x0011'6]ßQI½µ3N
ëxêMteL6Nóà´M'õ\x0006\x0019XAX'ûmõÉI¡³àÐÃ&p_\x0016ð;ã\x0005ü¤\x0005oî¤Þt)©`LN\x001c¨x)Í7úä\x0010¥YðæRêM·Ò'}'àeÔ·+U©I£î)ãÍÝÔ.'mcáËéÃÁÛ-)pÙ\x0011\x001cË	.'ùÞ<ý4ý\x000eÈÜe\x000bÖÉEå³ØÍÕMWÓ«2ý;·\x0012A\x0001'à~@?\x0008ÞH8lð<+9\x0003	{öÚ¥Ö¨\x000fæ³àÃ\x0016	§Üºæô$Z¶9ù¡xz7pl$\x001c·HxP¾è\x0014\x0017dù\x0005
\x0011åañdNa\x0016¼qÜ"ãA¡àÑ¹KËÓMb~Úõ\x0005oÌ\x000fn1?)t/æÇY.àK'^¦ûÆ\x000bígÁË[.g\x0000]FAÓTh\x0016\x0015\x000b\x0005üdRu\x0012Ü42n6É8\x0004\x0019»¢\x0006§ìË6C<=x\x0016¼q³IÆ\x0011¹¦VEG*3ÙËnÓYÊYð6ìÙ$ãºXJ"(ã\x001f½\x0011Q1°\x000b8ª£Eé\x0007RÿôîÝÛ\x0017¯n~úëÍÿ|\x0010\x0019\x00145´±tçZ-\x001az_VÚÚ^ÊíéÇO®_¼ºzöÃÕÿõ0.Ô¸0n \x0019á\x001fÀ0ý\x0017Ê¦îÔQ\¬qq\x00127ÅdÀ[O°£á\x0006þì\x0015Áµ5®Åu%¤nRÆE1vâº\x001a×Í\x000b\x0013a\x0008ÜãÁ\x0005a±÷È?ëk\ÿÍ\x000bC¨qÃ$n
»ÍG²Ý¼W¼\x000eÆí¶ê\x000cÒêF1èYÍàmI($-ÔJ:sÑvËFyMÃkfyeÉl\x0004ÇË\x0012®\x001c®5½´ã(msÓôìUó±xo\x0008Üëpe\x0002ÚnÁÕ(o#»zVxTÖ'ÞÀ ¨[GÎ×u;p\x0007y«Á ê0\x0018d×@*\x0001:Ö
e|,õîÄÛáÙÛ\x0016AÖæD<;.ó'ó3¼ÍmÙÛFÏ$ÅÏC\x000ea+º¬[Â6JÛÜ6¼mFIê\x0012æ72ÔFè´[@?ÊÛÜ6¼m:EÓ(\x0017[)qc·Àg\x0017Û·íÐÁ²¤B#K¯âFu»#GyÛ·Mºägtï"\x001f¯ó×ÒÝ\x00021\ã\x001b§þvÚ\x0016\x0003k3
\x0016JÖB\x001aòS ´6SÕªì§¿Ô¿¶è_'¥¹T¹&ú7tËyÆß¶Äo¿uâæý2\x0007oò~9î²k~ýO®C\x0014E¬h\x0003»ìÝ¢ºñs~ßóûoýu+\x0019zV2g){|,8£¸ÝÉ:ã¼7-ïÍ·Í-/ÎòþºâkKüuZ\x001f\x001bÉ\x0004ÊûB:a¹tÝ\x001eõ#ÞÓÚé<Úò\x0001E^+WûÝ]<ºù²\x0014ý]ÝýøñfM½\x001f½\x0002çw\x001c\x001b©í]ðÙz\x0000e6{õ~o.\x001e]½ZÊþ®Þ<}~u¶âO¸]Íí¶pÓu»pSîÝ `¹	\x0019ÐvËr¦À}
î·+¤úæ\x0005<Z"Aq©3\x0018íw\x00055xÜ\x0004Î­K6ÆäæÙ½Ia°g\x0004\x0006v\x0015C¦ÀK\x000bõ?\x0003ys9õ¦Û©"U=,äZ^µ1h.2\x0007ý\x0007#ä\x0018³Ü¡d¹ÝÜ}þðîöâõ_>}¾ýûÃÌ ¤XÑx\x0000È\x000e)\x0004Í/
¦wÚÏ®Þ¼|òøúâõo^¼¼þÃÃ¸PãÂ$.\x0015¯´«1¿# *©ÓÕý	à£¸Xãâ,®å
¾ÔgÐþuYÌØ-õ\x001b55¬ÍÇÆ\x000få%D'µvÝñû£¬®fu³¬H²q=/éÂdFàv\x001câú\x001a×Oâ¢+¸ÔuZr?´m7é6\x001bjÜ0KN8\x0016¡*PÉ¹\x0019s\x0010u´ïnÞß|ùú¹O\x001bkÚ8y¸ÔD_\x000f|ÕE7\x0016ÚîÆÁÃ­6\x0002C	úR\x0008|Õ¬º\x000c¢\x0014¼ÈB÷ù`\x0014·5\x0010\x0016\x00025ò9åbà¡&É*Èò$\x0016{ñ6*WOê\\x001atÈ¸\x0014>e\x000ba¼ä_uw\x0014Á(m£sõ¤ÒMß]Þ\Ô\CU^é_ìd#ªÁùá08× =öÎØK=y\x001by¬×b÷ÁmÌ´\x00134\x000b&Sò\x0010j"wà¦H¯û\x0010:ÊÛØ	=i(~1ámÌ´\x0013\x0018Ê3³Å(×x±;IC¡Èòp3ld!]R¸Èí\x0017é²R¡ÞË\x000c-r$þÅÌ::ãÙ#\x0006\x0013(3í±\x001c7\x0019d&öÝ^¿ñ#~Û\x001eñÛoþß¶G<	üI¥ØÓN
-þ¤¨µ°Wd¡õ,2:_.^2\x001cÀ.JG:^&e%òÛôÁ¸ø\x0011}Aöz®~zûùÓ/·\x0017Ó_þ~óõA`\x001d¨äKÖ¼¡mõT²\x0016¬¸\x00119
|õìÑË\x0017O^]_<NùÃÕë¡Fydy\x001dÕ*x\x0013Ë6h\x0001°\x0017òÿOÝ»%Ûu\x001béº]Y\x001dð
dâ\x001e~¢¨e\x000e^T¼h\x0014K2Ís$ÒÅK½ª\x001bÕí÷Ý\x0003÷¤Zr\x0003ÀÔ\x001c\x00039\x0015rTM-JÖÇ\x001c@þ	 /¶G¶jäXÀØÊÉq³^L6È,C³ú3ìzd§FöIúFQB¼Ôâz¼X\x0005 Cö=²×[Y¦\x001bjÁF¦$06òZX1\x000f\x001c{à¨\x0006.Þ\x001bcPB\x0005W¶Ð\x000f!^½GN=rR#Cà¾KTß¡M\x001bÊ¹\x001aiÎ\x0013ç8ëlÈ­U#×Ê
©õ°z2M\x000b£?Ö;dW\x000e÷\x0015ÚÇJIE\x0012ö¸zU9Ï<8dP{dºSå&Èà]Ë{ÆÓØ{ØÖÁ#Þ%[Ë\x0015 KkPÄ\x0019£mþmµypÉ öÉ1zÙ|!È|ù8¸¸:c|\x001e9\x000cÈA\¢ nâtä\x001a¸&ÖÁ¬^eÏ3\x000f^\x0019Ôn9qeð¸ou{IÒø}Zm&ü3æµ»ÁÆ<¸ePûeêÃ;0gÎwÄàNf^\x001dÎ5oæÁ/Þ1£\x0016õà\x0004\å!ïþþ8ßÜr4kàiôF6·û»\x0018/#Ðr7êZr\x0018ó '¨×\x0013É\x001d+FisE°WÏ#óÄgF½g¦Ç¼ÑËÐèZ\x001cgÓa.\x0003È\x0013õ¡'HÅla\x0012ÉÅ¶ÿüz\x000f¼yæÁÍ¡>ú,K\x0018eÀúiiX/Ñ[íV:Ï<¸9Ô»¹\x0012^\x0000Ï
t\Ã.7\x0002ñÀ\x000e\x00077j7\x0017s¢²ªjæÄwÉ%8¹Þ¯N.f¶£³zGg\x0002¿\x000003´üÍàVóç\x0007?gÕ~\x001af"ÙA33H\x000e²÷«×[óÌCÜlÕqsHR\x000cH¹C\x000b²²\x0001[í\x0007;<^d¨ó/jæ!l¶ê°9Ä,mÑ\x001b~o@ßZv\x0004o\x000f;fÛAP¬ZPbr2\x0003\x001eÊÒH|<1ÒØÅûÕ×éyæ!Ö·êX?DiûSìÜî\x0012½o-.¶_Ð!\x000f\x001ahõ¡>eFr\x000cêF;òJsXm«4Ï<h Uk`0Ð\x0006ñBà;ft¾Í*Õ1}óÌ\x0008Z½\x0008R\x0019\x000bÇGÝ¥\x001f\x0017;¯vüfv\x0008:µ\x0008\x0006\x001aåÍê\x0005ÞI\x0017«\x0010VoÌ3\x000f*èô*Ø2jÿZiò#O«>Âaâ\x0006\x0015tj\x0015ôI\x001aÅ\x0005r\x001fËb>ªJõ\x000e\x0003\x001e4Ðé5Ðg\x001eÊBí¥·]Dssn¼ËW+ /²ÇhLpm\x000cå\x001c%&ËN<yP@§W@Ú¥bavrsD\x0001Ójì<ó N­B¢jfzæ©'*Îf«upóÈ\x0002:½\x0002Ú6³\x0002Rw`Üèç\x0003ó N­¾\x001cWE\x0001)·î@ãØÎiu.ð<ó N¯èåHµ\²gÆ(ÁþO~P@¯V@V\x0002:WNâ6¼õW§¹Ï3\x000f
èõ
hÚ\x000c\x0005\x0004Ã9³tv\x001e½pÜ\x001eô\x0002zµ\x0002º\x000cráìäv¢5U;Ys«ó\x0008z½\x0008\x001a÷a\x0004/³¢}k°^É7Ï<È WË +W¾¥+'7\x0012G\x000br±\x000e|óñ¤xµ¤ÐÚài{ÄÌ'\x0014\x000bT]Û¦xµ¦P\x0012¢\\x001fS¬
º·åàqï~Ð\x0014¯Ö\x0014\x0017£\x0004]9¼¦ª¥D$¹Õ¹yæAS¼ZS\x00025Ðvàæ&ªÞÚvâ>n=Á?\x0007µ\x000e\x001eIH*s¢ö¹u\x0008ÇÝkÁÕ\x0005µ«\x000b.IWÿ\x0000òêã\x0011[×üãÎÛa\x0008:x\x000eÎ¢ùÖ×ÕìAÒÙÃ\x0001\x0018¼FÐ{òÛ\x00158KçßjTÃz:å<ð°ý~û¡¢4­ûÔ¹$M[\x000e´q\x001cv_Ôï>kÛ\x000b&%\x0013ðZ÷\x0010»qÃîúÝ\x0007A\x0006\x0012c9 Ô9<è¢\x0003C:.å(\x000eÛ/ê·\x001f¿_\x0016ùàÉR\x0005ØËxÇD4ýÞ£T#(à¸ó¹+¤¼Z¹5<ì¾¨Þ}¾\x0004s,$Ö,Ó"\x0017f'iùÑ¬\x0016DM3§aû%õöó¹JbX°ä®h\x000bÒ°ÿzÿù\x0004!L×Í|¥ØÝÐÁÌÃþKêýçdÒô	îÑîZî*éßaÈÃ\x000eLê\x001dèËÁ\x000fe9vÖ<\x000b¼,Õd÷yæa\x000b&ý\x0016ôAÆáøvÔ¶YB¹è.öðW!ça\x0007fý\x000e,d<\x0001ª¦øRß&iµ\x001dýjóyæa\x0007fý\x000e,K#±KldeiÈÊ\x0008Ç=_æa\x0003fý\x0006,q\x0006_Ð%#/e×	r<îV?\x000f\x001b0ë7 f9´Òå­lÀV\x001b~äåm\x001eSÕ\x001bÐ¥À½©J\x00169UÊ»ärà°R\x00088+81ê-X~£ÝÂP/ÉÀÐ¾A\x001fWrâÌw\x001f_¿?{\x000f¤èµï÷­4K.R\x0008\x0012r\x001c}äú¦[òÀ&]·4Ç2Û¨>\x0000YIÃu^2´c8N\x0011ÍÏÑÍ\x0015èÁ§6\x0013ºüò\x001d´n\x000cù¸#K­ß8êk;¤äeclÚ\x0008í:	{¢HñÜà%\x000c¹b­xé¸\x0018Ómn«üòP\x0007åÝÁ9z¸\x0006=X#\x000fC4ºM6h2\.®vÕQ$õ·AIëÿ^"ý^\x0000B»K\x000fYg}\mÂ®Yãß­q-¶¯µ5\x000eQ.\x0013¨¼×¸YmÝ¦¨jûS¹bü%[Á±dÞÿ\x000b$ßÁÏv&\³3Ïj*d4j_Sqè§­t?¤|+Ë®\ºñÒ2·Í\x001fX)4*Pq*Z\x0005¢Tiä\x0007g\x001aTÆ¹ÒA®}v­ñâT~8s*?¨£C+s]ñæµ+\x000f¢\x000cÚï¿/6+<]42yõ¦$¹äMi1H«³¸ÚÌb¸(åY$[R\x001fÉ\x00128wºoçKÊÜò\x0018;õüÃÙzÖ.\x000c_g$ÂËÈ&© \x000ef÷b^\x0019Íx>TÅª|sÿéÇÇ÷oÿôú?ß¼ý,)RN
§ \x0012l[î\x001eã¥²É¥\x0003ë\x0008ö\x0007¯\x001eß<~ðô«»o\x001f=]Ýv
\x0016{XTÁº\x00002©Õäâ1jK´àlk\x0000°êÝ&am\x000fk-°\x0013Vè\x0002[Ö¥Vf³ú\x0018>	ëzX§³,úNÚ¡y,ëqµ¥ÿ$«ïY½Î°¾eú\x0000
o\x0005î[á%Ùnõ¾f5ô¬AgWÊþâüKçùr©8Kììêð9ØÔÃ&%lëü&HÏ\x0000­óC^}$Í=lÖ­hP¶4::í®¼:Vzµ#kº!ç\x0005#1<5¨L\x001bm+î_('iGIÐi³­Õ\x0003Æ¥´×<ÈSÇCh\x00077\x000b:?ëâé
 ¶~©!J9VÇ½LÒ\x000e¾\x000btÎË,Ï\x0010!ey!H\x000b\x0008ù\x0018Q85?[`£\x000e6¥6\x0019¦g²CH-ÿ%­Ö\x0010ÏÑaÙ\x0006e(\x0002ßã\x001cÛÚS"«=Uf½×0#}ñ`mFºBvù\x000ej\x0003ËnlEÚ«Å³ZvÎ\x001cÔÌå4$	\x001be¬]Ô:;¬^rÎzS÷3ö\x000f÷:#/i}5\x0003;b(Âëu&Ó\x000bãtìá!§YfZîmSukÕû\x0018ÖnO&áÔ¶¿">þª÷\x001e­	Ý°	$4^\x0018
¯ôÌtá Ç6Î#qÃ<éÃôù\x00048Ír_M\x001c·Oþ\x001c×kq©\x0013%W¿*¬Ä¢õÐ	\èæÓ°ø^\x0017ðAK\x0008Án8HKÒõÚ¹=¬%\x001e\x000fëå\x0007rX¯s[¿|÷·×oß~~f+\x001aßFXG\x001a\x000bÅ\x0013EL¤)^#­\x0013[¿|ö»§O7Æµ
,ö°¨¥!Ûµ/m*GJ+3\x0019ùÖ\x0006×«U'YmÏj
·6p÷F/\x001dËÀJ÷Æs\x0015°®u:Xj[Yþ¢LÁ¬\x0010ÄÕV\x0018¬¾gõjV\x0019fP\x0016o\x0012Xi\x0004WKi'YCÏ\x001a4¬³T=\x0015ÿj%E6§Äq\x0002ºì\x001a{Ö¨³+Ö¤ºÚÅ®(½rÌúQ}\x00126õ°IgØ²L=Û5ñ\x001cÌms¡_Í¡c=\x001dÕ\x0017\x0017k® sBÙ^³ÑËã$âjwªIÚÁÇÒÉþb´ã\x0002¥çúÅh\x0007w\x0000*ð\x000bÒ\x000e{\x000cT\x000c³Ö \x0017%\x0012`õ\x0002w\x0015uÊu(ó\x0003Ý6\x0003{/Ií/ÿèA®\x0016N#\x0017kØõn%\x0018~ç3!GºÕ¯qW\x000b\x000fÖ;ÎJC¬ò 'ÈéõàeÎi c:3S§ºÊlW\x0013^§»3Ce3b
Ë`Úó v¶«Ç²Ùøö\x0019ÕÌ!\x0012'\x0013¥¶I±E
«%Ókùã¸?êÖ²kó Ê
¤	±!VßÐ¦y¿\x001fy¿×ð\x0002$NÜ1Ô\x0000ý\x001a4'¼zA6ÒnÍÒù¶KêmÛd\x0010\x0002íÆ\x0017Âjbü\x001e\\x001bÎÇnÌXùG~¼yxÿÃw\x001cy!\x0008·ö~OTYs´\x0005Á¼1OèùÃ»Ç7\x000f\x001f<üzëþCP±GE\x001dªCñ¾©èpÍYÈÐæaC>Õö¬VÅ"ÈX):CHzÊ\x0008t«\x0007IX×Ã:¥aåzß¤ÌfÅÀ¾ÖÚõy\x0005S ¾\x0007õ:«fyë+>Ëµ\x0014¸·\x0002ë\x001d&ac\x000f\x001bu°6Ñø\x0005F\x0004î\x0015+\x0017\x001f°Þb\x00126÷°Y	ë9aÙÄvÄØ¶å\x0019s3¬Ý®ÐÏé¥ÔS\x0003í )í_Tj ßÙ6E;:X-b \x0006­,öèÛ\ÄtÐ2ÁmÒoQ² ï°òK.Ò £üþA\x001dÜ\x0016èüV2æ#\x000ctoW3K¥;ÍÏv\x0008ìàº@é»Z_bYCµQ\x000b­kñV\=MÒ\x000e¾\x000bÎ\x000b2¿-û\;I§\x000f\x001d|\x0017(\x00175_æ`4\x0017¤\x0017ÿv\x001d~ÌBÀÁ\x001f Ò\x001fá\x0016âå\x0010Ù
=#ævB_-k¤\x001d\x001c\x0002ê\x001cB,ç\Ï'±Ø&\x000e´.?\x001b§ÇIØa¡nÅ\x0014%¡v.\Z\x0016²ÜÂú)avØc¨Ûc4xV\x0008.JauH2\x001a\x0001`cFÛ\x0014m\x001ahr!Ú½¬ZÃ¯ýe!ÈË.õü9\x0006vð\x0008¨ó\x00081¢<7P÷$-%%ÏÊ¬¿7ÌÑÚ!±Êx¦¨\x0017òuGZ~YmÛF!ºÕWóIÚÁYÿ¢f^\x0008EÇ¤+j¢\x0008V3\x0012&a#£Õ\x0019cò|¼
åDf¸±\x001a5³`÷\x0005Çè\x001dÏJ_KU|½Héa\ýàÛª=(R´CðeuÁ\x0017y//\x0017\x001c#ä>\x0006pµÓå$ì \x000cV)\x000c>ÊYfK\x001aéË)ñ9
6\x000c°Aé¼B\x000b\x0010|>H!I*>Àê°úIÚA\x0017¬R\x0017«å	Á\x001b	¾B|\x0014Xm\x00119\x0007ë\x0006Oë6$Îl.k[\x001bÜ O»°>rfvp^Né¼§\x0005yÜõ9A®¶©ØjFë$íx¤t\x0008Ôa5\x00174¥)Z\x000cÇì17ì1§ÜcÞÊM\x0012õj.´§ÕbÊIÚa9å\x001e+á¡\x0017am!Xi'eV¯êç`ý°Ç¼r9Ç\x001bOd\x001c{Ùö¨\x0017V»LÒ\x000e{Ì+÷XÙXiËéÁJ[yÒ#½8\x0001¸V·\x0012r\x000bä\x000eÜn@Û¥"F¿/FXñÅ¸6åQ\x001btqxÆÄ)J)eÝ¥\x000b\x000ceÜ\x001ds\x0005
ý;^}
w¼Ydê£RO¼\x0019ô[ÍQ_¬[­k=uó{ë¹ì{í-\x0018O\x001c¦Gé$×`Mº
5öÜÈVkäY§õÙÉJQxs:®ÖìÌî¹nn6ïº{õ¶³mÛ¹ïºc"2zÛ==@Öu,\x000f¿âu|¶U6¦{±Ä·xà)eïÅÚ\x0005éA\x000fQöÜÆVkãT"uÏ\x0000ÑF
ä!b5cx'3Ø³'ò\x0003yâùã§ßÝ*ÿgA®s\x001d­_s	 ê[~ÌèpµTòËW7¿{ðêá³Ï3.GQ.Gg i
,Ñ#'ß:p,ÅH\x000f}×SúÒÏS\x0006_G£\x0015J0'y\x0008n5ºÙ\x0003\x0019ìY\x0016+yößþöá_ÿôæ-ç |õîÓÇ×?þ¸#á\x00121JÕiùóõG\x0011eJèÜÅ
ô_ß=yô3\x0011¾zöêåÝãÇ\x001by\x001eæ<\x001bÁÔlo~¼ÿ¡öþë¿\x001f¼ÿéõÏR<\x001c\x00077Ô3s&ÚtÍ\x0012B^Z¦ß<~ð°X÷æÁó'w/>=&ª0£¼PTc­`D5æ\x0000LÛcZ
¦\x0005É¶-»)±1[\x000bZL\x0017\x000f
¾§ô*JÛÒ¦
f
\x0011)¨yñD>\x0019{Ì¨úæ ·])\x0007ngHý÷ä_ºGÈË©<B{Â¬!DÏ\x0013HM^ÞEëç6\x0012jÛ
°æì\x0008ã\x0016Wíñ6Âºlx3%\x0017;ÖOb\x000e{\x0007T§\x001cb­`\x001aný³g\x0004óâmÆ$ç°{@µ}\{ñJ4\x0016®æÿ£\x0002¶«IÎaûjÿ\x0014mç7J
Â))\x001bLb\x000e{\x0008TÈ\x0007)¬*~GÊ)ÊÞj\x0017ß\x000bæ8qØE¨ÚEô^X1]àÉ½Å"\x0014ï]9¬NT­Î\x0012\x001fK¢N@ÉïF'WAx¹E÷$ç°:Qµ:#ò¨±"BAv;Z9Bc>Àyâ°<Qµ<3Ô0¾{lË3HFL\x0017ß·ç8í°<­fy¢­äÏûÛim;.\x001f\x0011zØá³[Íg§>Ûæt\x000bÁÕ~%<²tñX4É9|v«ùìåtFyûõ³g¾£¤Ë³\x0016Ê]ÌÊãtÃgwªÏNóåO$ÕZ}WÈ×v7h»Si{¼%57Q\x001b@!]:´Ob\x000eÎÓ©'	\x0010¯Î²\x0000"s¢$\x000eb¼8¬jsØENå<©[}n\x000fu${è8¥Ë\x001dÕ'9]äTÎ\x0013<yLÙE|\x001eòâ4×õs«·æLYþê×ùÙÑZä5ö´åÀRØyºöÙóÅzÙÏ~º[ä\x000f¯;\x001aYñóOëÒ\x0011ÓÅ&FÓßq~¯>
µ«+Ô³E±õ\x0008+ôz\x0015Oõ
~ðë¼\x0005qñÖE%îè¥\ü¹º\x001e\x0017à\x001c\x0017@\x001bä¼ÑÞf>¶j2ë/¦UìÅÍxvcWÎá§\x000bÛ/Þ½]nÂÿü¿þ1RWÛ\x0000¥²$85a\x001d¬V\x0010}ùêægOð¯·®\x0017\x0019\x0016{XTÂffq	c+s°Y`ãêÐÊIZÛÓZ%­$¯Ar¦¥\x0005Z#°iu¼Ø$¬ëa\x00166È¸æ\x0014
5-ª´\x0017èÐ¬&NÒúÖ+ic1htÍÍ´]Q·hCO\x001b´¶mSÝÉ×ú2L»:k\x00126ö°QkZ>\x0005@¦ðK\x0007;Û9\x000c«¹v°©MZË\x001a\x0019F©'\x0005?#?ç8të
_æhsOµ¦En\x001aé¼Ê
²fÓê(9ÖSÖ¢\x000bF\x000bøÔ
ê¹³l1Y\x0008ëõÅs´£ieÒkoé\x001cN\x000eÐ\x001cÂj«ËIÚA\x0018@«\x000c!S×ãF1,÷¢9g«ÕÐs´2V\x001aB ÷§BÆFIhÀÓØÊ\x0016[Í÷Ä\x001d¤\x0001Ú@õÚuº<\x001aê8^½­<T©à®NÄ\x001d´\x0001´âPç».¸ÞQJ­\x001eàÛ!gãjõÓ$î \x000e `¨\x000fúëÌÒ\x0006\x00057¬\x0018Nâ\x000eú\x0000ZðâÅÐÄÔÂ\x001a©Íp6o½÷OàâàtQët½Â!\x0018ÓJcù°ë\x000eÆqpº¨uº¹5z¡-á8ç»(¸x¢áxxÐ\x001e|æùHå¨î%ù2Ê\x0001Ý¹°Þ\g\x000ew\x0010	Ô\x0004HM7\x0002\x001dv8!ÛÉNsTÎy\x0008î°ÓP»ÓPîçã=8n2ì¨z\x0017îú%]ÅuJ8­JÐ\\x001bv»\x0019$íú²uÍA\x0011\x001bÜ®ÓºÝ_è,é8×i\x0003Ý_êäÛµ­w ÷JQk=Y\x0013Øv0ÜîÒÃ\x000e:FtÍt*ð÷:`\x0003íDYt"³ç\x0005Íæ.>h|Ãhá\x001dªq\x000f1µ5ÁQYq\x000f¡¹caHsæ(½5R¾õXçZÙ¬Ä¸: söÂéú
hJÖp|K­j'\x0011;X­O\x001fWZöç·¹ßvJq|þé§×?îxm\x0004Ã\x000b¢ü
å\x001emÅ\x0001_<\x0004\x001b¿zr÷xÝ°\x0002êzP§\x0001
JÑkÄ\x001b¥{¾ÍYNkþb£ôiPßz\x0005¨µR\x000e¹Ä7¡Þ»Ô®.\x000e'æ=gTpBYõ=§Ø\x0016è\x001e¯fép®óþbØ¸\x001bÔ\x001d(]¶S\x0010F·Äùíû7zûú7O^ú°£\x0015\x0018y.Nk\x000eÀ\x0012éØ\x00108c8»iÍwK°ß>ôÕÓ»'w¯^l¸\x0001aö=³×3;¬kÖ¹>ÎfÞ[\x0008p9\x0016Ó1Ç9ê_N=å;ËÃ~ö\.Ô|ë0æÜ3ç«ÖÆòzRìlT\x00083·U@zý9\x0008Ú\x0017êaqÐ_ë¹\x0014\x0014Pm5c(©úùr+_åî¥­®ëEÚ~ÅÛÑ\x001a;¾°\x001fÈ\x000bÛãO?¼yýöæÅ·úñÍ±wEÝxctK­\x0017É±<Ëqã ñøÕÃGwOo^<zúÕãGë\x0013\x0011\x001b-ö´¨£õA2gaésÄS¥ó£^M\x0007áÚ\x001e×*qË®³q\x001dÏº¢¹\x0010bÜ´:\x000bq\x0016×õ¸N£é+Ç!
-\x0017ë\x0006\x001f\x0005w58Åõ=®W.Ý\x0012ïð\èx8\x0017z+k\x0001ÖGÖÎÒ6(i-pºêR\x0016Ì
y¼dÿ\x0006G-ÝØãF%nÌòv\x0015ù¶Ä'ÓL»:ut5õ¬IË
ò`A¡Eä\x0010R3íê5ê,nîq³\x000e7¢¥Ë\x00057$i-\x0017<\x0001\x0000¬¶ÕÄí\x001a"B\x0018¥y³«µ>Åº^ÊiC»¤6yõúa\x0016w\x0008PjD¤g\x00151oÕ''Ìõ¦!³¼Ó\x0005¥×%£òÐð\x0018
ç:a8á®\x000ekvcCõâÊä\x0014?¿å\x000c'/-\x0019w\§ìrfî\x001cÚé¡á\x0014ëX\x0001ÐNZ{ÒþZ}Ãó9<xÃóøÓû\x001fvÌõE,ÇãÌC'!scwÌ%=Ë£[»ÖyüêùÃéÔ
\x000f{<Ä\x000bVîÊ¦Uº(5uÞmèØ>:ÛÓÙI:c¸È\x0006ÐQ®HM\x0013çÚ°ô¸
ÎõpnÖtkPé¢¤5ÚÚ Ö¥ 3x¾Çó³\x000bÏ0\x0001\x0015ø;^xÒÀÈ¯ßîÅ\x000b=^µ\x001e4¼ü(bm´E\x001f6\x0002¾}x±Ç³Ök\x001f×\x0016\x0008\x0017¥Ñ^ýuÜz¼4\x00072Q±Õ£X	îËÇ]}öØ{¼<WT;ó¾ ¬mëv@#
¯Ã;\x0005CØ
îY|5³\x0000ÐX\x0007mô*õyu:Ç^¾Q3fE\x0003â-Ï§ÅÐ¶®\x0014è\x0006\>¹n\x000cÖ\x000c\x0010ÍÀh¥î¶\x0004ó\x0005¼ÖzhÀ¬jxié	ôKcRö\x000cçs«y{ù\x0006ÝYáH^\x000eEË8\x0006·ÎH7×\x0012-^k¿A8`Z9@V\x001fõzçÍÑÊ_\x0002n\x001c\x0011öá
Â\x0001³Ê´ª@D9iNÍêHÃ½|rÀ´t\x0004®vEä¢øæ6\x000bûZß\x000ctÀ¤vXÀ6A\x0002~»dÂwmX\x0005vÀ¬x\x0004ÓÄ#uîE:px±dy\x000f\x0007ñÀIñ(G\x000fîHµ\x0004¥\x000eÙ~Òª,ÿ»oè§Ý3ÊÃZÇo²Å~R«\x001a¯]~8xgõÎÁzXð2ÔÆ6[Ù¬\x0016Vìå\x001b¼3ÎzgRÔ±^9kì"ýÑ­öÖÝË7xgõÎ(\x001d\x001eÁz	¬d4\x0000ÍÒ¾\x0012nðÍ8ëí)löÛ\U(\x0015³ñrû\x0019¾Á÷álÜ;{âÈe=ÿu\x001f\x001dø1°ò³[×dNÐ-®Å¶ºè,
ÿk¹ö²`Hþ¨GòÓ
ÌNJç\x001a%´IãÖI¿8:2]{ð=§ôóeýñ>\x0001JÀã«
ï@b|s¥-ÁSsÈ4fðÜÕ\x0008¨x_¢-\x0019w\x001bpã
l§ØS¢2BiRæA·Ö¦öÉãÕ\x000bÓ÷½öê'^{û\x0017f Ìàzn§»6)4]Ï\x0017ß}¥pnË¨Ú=6¶³'÷²NäY{´39|GÝ¤»àòD\x001fÞÿôfGÏ:ðÑI\x001f\x001c\x0012gF k3¸Yuà\x000f\x001f<y´Õ±®èæxJB
}RÏOzû·=§cÇ[fIçJlAk%[Ù\¼ù=%õ¼xõÕÓ?|\x001eÔ÷ ^\x0001J÷nK\x0003@ª\x0008ðÎÙp\x0016¸M\x0017\x000f¢»AíòÉûÔòÉ9ñßÜ¿ùëç?:¤¥Ìy¹J§ö\x000b'¤,	Ôêf-oéü÷ÍGÿþyLì1Qùõ½|ÿÚÈ\x0008²áÉ=qu>Ã\x000c£í\x0019­Q\x000e\x0007Ô8Ü&ÆleÃ+©E®ÇtóH\x0019¦L)]Â!\x0003w gªí!ëû(}Oéu\x001fÓÊVªy\x0011Änõ¤?\x0019{Ì¨À()è6òyFPJt^\x001dÎ3CzÊ¤ ô®Õ1\x0017LÃß<»$YÑ«#\x0002f0s5Æôr³\x001cP\x0007ó\x0005ÓJ]\x0012\x0019özÌî-\¦QpfÏ]"ñõ\x0016\x0000\x0007×¾ú\x0011£kWøv:ÎZIG\x000e7ÊF¬%¸ÜXmsð p´<\x0003cÚnuC1\x0007\x0004\x001a¬<¿\x0012UÏn;Î\x00036;\x000c.	\x0014>®VBÃä´	\x0013%?ªÂ¯À,Îâ,+±M[\x001fnÜÍ7ïÞ¼/T;ú8êÍY\x0016x\x0018
2Ù½\x0004òëuõw/è_õìÑóò[\x001bML\x0004\x0017{\Tâ\x0016ß\x0019BÅ­	×óA\x0008-\ì\¦¡µ=­ÕÑZgÅ¸©¬\x0008N\x001a.'§°³Ñz82ëz\§Ä-\x0007u6î2\x000b¹ÞxÃ(ÔoÝ\x000bÌáú\x001e×ëp±,]WS²if§kÈQ®Xw½°o\x00127ô¸A»Óð\x0013±!JÍ\x0000i1¬Î¥M=múÕ®\x0005â\x0018\x0000\x001ft\x0001à\x0017ïÞ||¿§Ñ;õ1IÈ>\x0001øBÌ\x0019*ZÂzùìÝÍ\x0017Ï\x001e½|¾up\x0016ÌÔc&\x0005fú0P0câ¢dg$#\x0004-ýïê1\x0001Î²¥Ê\x000fÆÓèÃüß¯o~ÿéíôKÛÒÚ4.§¥+ÛR\x000fdÈÕtë*a\x000f½¼»ùýWO7ïÙöÌö_Ù÷Ì^Ï\x001c\x001dW'¡<ºzãCÙ¯wáf=sü×°óÐ©­®éV.©@§r¹\x001a\x0015ï(]"ô9v«o?\x0003¿\4ÙVô9µ½º\x001c¿±¦
\x001bD9í$¹Kw\x0017\x001bbNPÛ\x0004g9¸	NMdr<yýáÃnxP~ç¬õ^\x0006cZcåÇ¯Þ_j<¹{ñb«\x001d\x001es¦Øs¦¨à\x000c2f\x0012,Í\x0015«YîÝ;ÞE'0tÛzZ\x0005¿\x0016Z\x0008þL8\x0013êN\x0013_¿~ÿÓ{z!z8¯«ø,Oó1:ñ\x000bf5[@¿¾{þäÑË=¨Ø£¢
®/Ú­´¹§.1Ü¶1®¦/Ï¡Ú\x001eÕêPyÚNA¥é¨je«]´Cu=ªS¡"pRx±j¦÷¿\x0005\x0015%·Å¦Û£\x0019Tß£z\x0015*\x0015¥ó\x0002(ñc¬YjQâ[»>Áh
4ô AgS+³©\x00188¶ihB4G Æ\x001e5ªP
È±1­pràÇT\x001b7±3¤©'M:RËÓ8 üÈ\x0000£Û;\x001b®·NBÍ=jÖ¡f¾J2TGØÖ©L²ë\x001däfHOW²û7º=x@	®²\ÎDy0(2µñú2Ã:JN«è¥ãntÒ\x000c½°VY{ÈbA«@/V¹­VÎçNÒÍËj=Ä­Â V S«Ò¯Æ´ÇL¤Ja]ï£2Å:¨\x0015èäªÄ+Vü6\x001a%^\x0011Ö{]¨æüHnL×½ùáë÷?ì\x0019\x000e\x0017Â©Ú\x0000$£\x0015}ûü\x001e×¯bÊ_Ü=¸5\x0014N ±ÄyÈ\x001cn¹$FI\ðITÊ§Mæ'\x0019mÏh¥t=¤S@F1$\x001aÞ?Ñ!íÅ\x001e4¡g\x000có\x001eyÈ\x001aS\x001cH¼yÞ\x001cñ±bÅjË®OÒ~T\x001eÀT\x000eáÐZb+5ÙI&öÎ9*ªPËÆáÔ$jækñjqR2ç×o'fÌÚ%zU³J¢×¯n+Á¹]Ac×häZë\x0006Ò^Ñ·%p±YÒHºrÙcÂ¹\x000f½ÿñÝÃ}¤Ý\x001aÞ\x0017\x001c!ìmòöåA÷øÙ¦þs\x0014z´ÚäÉe\x001f}iîZke4©Ý£º\x000f0ôaÖÔ\x0005\x0001­Ë±\x0010Û\x0001)lõ¯Þ\x0007zÀ4\x000b$­Ød9F\x0018M£¦\x000f[îr\x000f`\x0017½Ð7\x0002ßIhN&tÜ$¨l\x0010ô²\x0006×»ö\x0002â\x0000æÓñ!Ø¦^&VÙl6z
î#\x001cv	Ìn@ãýøæ#rê8]2´ÄÍCVf\x0000í\x0000h§÷q\x0014Ç«ÐÈè<lu\x001fv«÷ôÂ·å\x0003m\x0003\³t­\x0019Qñ229
S\x001b(ìWk\x001a?k>Ýy¦ë¼ôw~|óöõÔaWôY&Ód'÷¡õ\x0012 ~ëO½züèéÝV\x0006\x0006µ=¨Õð,ÈY¸EÇ9\x001dN¾5º@b?¨ïA½\x0006çØ¦-µ	¶
4Ù°nuÞÏ\x0019zÎ áÄÜnË\x0001¼~øâ\x001fÅÛ­¦±û9sÏUk\x000b\x0014¶ûW¥À~y\x0000h¾çzµùòpË\x001f¾,V¾}õ¹M\x001bî|?ç¸åU{¾D?-¸Ò»ÔG-üV÷Ýý 8¢\x0006È³{wsËÁÙ\x0016\x0005m\x001ctö\x000eÎ	4ÞÉfÏ¯YÅ¤I6½wòUÁ!6u\x0003©S¢LøËÖss©BÚÜßjÒ¿tð£ r¤àÚ\x001b\x0011ú\x0016\x00171´ ý¯?xRP¹RHü\x0000¿\x0008=÷þô1É:]oy3E\x001a\x0007Ò¨ùúÉ·YÃôKÎ²¦M\x0016_Í!M\x0003iR&\x00192\x001d\x0013\x0017=\x0014P/\x001fß¬6\x0002\x001dä	4úD[ß	iæ\x001b²¡¤õÝ
wâ O¨'NÐ%ÔCîËäc\x001b¸ÕÕ~?çàõQåõéq\x0007\x000eçÜ|i\x0012WºÞ&g
tpú¨
I]lóÚs²;*&\x0012ÒõLØ©m?¤\Ô­ß]\x0019Í-U©F<-Õõ*ÛÀþüTâ»S	ÀÍÓwÿùú§ïß¿¾\}Ä6p	ÇéuiÈ\x0001{åß°\x0000Óàu`ú÷=ûöîÉ\x0017Ïïê¿ï³àØã5à´×\x001c\x0003ÅÙ\x000b8HÃ	4[7Þóà¶\x0007·ÿB\x0016w=¸û\x0017²¸ïÁý¿ÅC\x000f\x001eþ,zðô/\x0000\x000ep6è¶üà,{ùÝ§Þ¿þqÇ?z\x001ao^ë.BMø\Ô&p_ED³~\x0001Â\x0019¯^¾z~÷xó\x0002ÎÆÝ\x00122þºñ¬\x0006ÆÈ@\x001b)^ ÿç¿þûîO?¾ÙÓÝÐÔ*I¡\x000brâ4hZ\x0006ÕÅFA<ù¸0ßÜ}õøÑVov¬«Ùú\x0019ÇÎ])øÇïÞþéSùïçïÞìI¥¤\\x000fÃmK\x0001¸:°¦VÇ¼Y¼þâæñ³§_½*ÿýüÙ£­·fwÐ³;ø`÷æ,6)?\x00187ã·oÊ¢¾¹ÿô×oË|~­\x0000Ê¤FKàÏP4ºen.îo\x001fu]~ãßo¾-ÿñyòØÇ«ÈÍéêÏ\x0005¹\x0003\x0000/\x0019ã6n\x0017FNÎ.Dæ\x001at-7â[^uj\x001bà)mt\x0006|eFP:»[/?òòõû÷\x000b÷Ë´\x0016%à¢è\x0012p\x001bç¥ï]^\x001dôüòîùóùeùÑº\x00056ö°Q\x0007K¸ÒÝÆðc
\x0015ð´î6«wÂ\x0015véê[ÉW÷~üéÝÛ\x001d]©VE±£\x000cBé\x0007åW\x001f,¾zðêñgO_®½úøó\x0012ß
JöÓÙ(µ¶ÂK'¯\x0010ÒjÕqã[\x000f|<»µðñtk±|ë'÷ïïßüðçü÷;²\x0008\x0006
Ô\x0013,µ\x0016_n fÉÂF»KûÉç\x000f\x001e\x0015_ü¼{(¿`æï£\x0002Úh¾/¨«"ýåo\x001fßßüÛ§×üÅ§ü}\x00070¥5ó	\x0016\x000b;\x0017!g\x0007\p\x0018/7Ê+¨ÿöê®b¿xu·FK[)õ2Q0v!§õîo¯?~$\ËÏ\x0006î·#ûÍOïóüõÇ\x0002üö5\x0011\x001b\x000f`ªÃB¤èT-}ë\äêÞrO?JéÅ«ç7Ïïh\x0013=½ëz¶çzö»/×â\x000eÜöàö
p\x000c%F,à!-Ï\x001bê:&n®áºÛ\x001bÜºüäê;÷0\x0017[b!XþªÎÐpeIÕ´	K©]þ2t¿¦©ÆóóÀØ\x0003£\x0016ØrgÀ\x0002\x000c\êåÚ-»t8
ØöÀV\x000b\x001c°^uùªf¹æ Àüæ~\x0000°ë\x00128f¬yÆdas[·\x001fõH\x0013Þp}Ïëµ¼.Ñã6ñFº®\x000b\x000b0\x0006\x000cl¸2æ\x0000àÐ\x0003\x0007-ð2\x0002¾.Tg«\x0014\x0003sÍ	\x0019Ø\x001f¶ bÏ\x001bµ¼õQ\x0011êeÇ\x0006ÆÚ\x000cl\x000e3pî³\x00128$[_ì
p9g`õ\x00114Æ¤\x0002ûlZÂ085Ðz5e\x0015Ä
\x001bqÃ4ÜLL¼"yóÀ\x0000µ0² Rm¹Ph\x0017Øp\x0014mWAÛÜðXA;µïÌ­ø\[\x001aÓ¾\x000b Ønp\x0015vUÐWQ>ýÓ_îßü°O9¢¯óË©È§\x0014\x0017å°^±÷+\x0001\x0014'<¿{òÍç/×\x000eù\x001d0öÀ¨\x0005\x000e\x0006ô-ÀâX¥Ã¡cm^&\x001d\x0004ìz`§\x0004ÎEß¬\x0000\x001bqÅ.Y\x0010àÃ\x000c{Þ¬å-ëî \x0015jJW9Ü(¼>nJÇ\x00040\x000c+\x0002KÂ\x001b\x001a\x001d\x0015\x001aqª.8ß7=ñ\x000cp\x0018\x0012\x0018\x001cW/v`M\x0013/+\x0002jòT!ÛÎm\x001f±9÷\x0012KEÐWïïßþñ¦`ït\x000fùÃ4\x0013k®¤#÷`%À\x0015Ó~õüÁÓ/o
îç	±'ÄiBËé¸"Òa\x00138ô
\x0012éx~¨¹\x0006Ñöv\x001a±\x0004»\x0001\x0015\x0013#\x0006\x0015WÎ?\x0013®Gt³%X©\x001dc(\x001eµô· ÆfE<À¡G\x000cÓØìÈÆå:.\x0010aEZ'\x0010c\x0018§\x0011\x0003Ôw
BD\x0011ÓEBåXs5aî	ó$¡`nùè+ÛÅñX#ÙrkÈ+\x0008aØÏ0½¡säç©Âöm\x0018DPè¯v90l\x0016Ý-4%¹^1ÔB\x0015ÚÏ-Æ5`\x001cv\x000bÌn"æ	UÆ,Û%¸$NÇ«·\x000b'	cú52â(/³ËÑá§0Ú2X{bÐM!
£[;N0\x000eë\x0011§×#TãUÆP;+\x0016Æä°Dc\x0019®e\x001cÖ#N¯Gð¾æ¹ÑT$ T²Åõ \x0015×ã®ß38¬G^\x0010<õiª(vL¶ù\x001e®þÖÖ\x000c±fL®\x0010c¨Ó\x000e
cóOðpµ\x001dí°gìôYFÁññ±¯\x0014¥6éÄx½\x001d=c§÷\x000cuç\x0007Þ3Þ×\x0011\x0002ÑµºË+1ø\x0004ã°gìôù'3ö%¥õ\x0007gOïïö^{xz²2Õ\x0007rc\x001eS÷\x0014»}h¬\x0012»÷à
Éï¾ïÓo¿×2Cí V©/>{ö$o@^æ\x0013]ÅlÏl{#÷I0{â\x000e[\x0007¢ÑA"PS¡E/Áb»Á[Òx;\x0011¦\x0003¶=°U\x0003ÓÔ\x0018\x0001öMàmsúÒòz`ß\x0003{5°[/9µ\x0017©ÑgríèÓö]Âçýw?\x0006sÿ\x000fG¡Kìùøõ\x0007Êßzÿ\x0003¥o-\x0017\x0008±bú\x0005óoDVÛÜ,\x001dD\x000f$÷þ·\x0013\x0015|´éSù¹ýá·ï^,o¬\x000f)IëÅÊ»*½L>K«þ`Yï>}\x001dõ»×ïëÛä\x0005*\x0013W¤óË½Q^¨ÐÔ\x000fì3¦p¢zþìÕKÙ8¿»{¾úþØa\x000f\x0013`!¥*å%,§\x0006Qa\x0001Xð
´ïVÙ\x001eÌÎX¦\x0015Uåq1o\x0006óWÙËõXn\x0006«ø%½>¤£°b±W>}H¸
Ì÷`~\x0002Z\x0002'\x0006+gêj/õH]¸\x000f×p+Ì\x0018Rõ\x0003syº^À¸ÿ$¥«Àb\x000f\x0016§À\íU]ÀÂ\x0001oIn8VÀ\x0010¯Zù©\x0007KS_Ò/w®8«¥x´~ÉÈ+\x000c$IÉ{®<ÃU>_b\x001fVk\x00170W\x0013}Fï:.\x001cñ­f\x0006,\x0002%§-\x0016£·º'\x001dÔ.w\x0005Ì!\C6zý	·\x000fÂ­©dÎ\x001aqûÉÖ²ï"Áâ5dÛ\x0019¿O·Gü1c\RÌ\x0007Ã\x001föí5d	\x000f\x000b&Ô\x0017ù¢ßaYp~ÇAP¶D×8X\x0018\x001c\x0019Lx²\x0012\x0006×\x0002iç!/ç6\x0002Ë91wW®ÿöºzÚ\x0003ËóêîOPêm@\x0003Áêb+Q\âm\x0000î*ËáÏ\x0000q
°f<&±|Zê¼Î¡Ë¼O\x0005­\x0001Ìý\x0013NýÁxBûúþ?o,8K*\x0004F`.X©'&!0éÕ4_?xøõ\x000e(ì¡p?\x0014b}¾uÔ{úy-P<³àôP¶²¿\x0012K¹\x001eÊí¢\x000b3à\x0008ÖµU\x0015¬÷þ³P¡
S²ÃÄx²Tp,öáØ,Tê¡Ò¥Äú?ÙRØ,eÕP~gs6@ê3¦rµs\x001d*Ðôòjª,rzKÁ°û`bûE¬é£tü0=±@ev¥TÝ¯\x001a\x0016:L¬tðõÀÑù2$\x0016(\x0010¨Þ{Î.)\x0018{þyOÿm²â
\x001c\x0007ùådX´]À²\x001a6î×[ÑË×÷6\x000eµyd\§=\x001dj\x001dû)\x000bq4Õ×\x000f^m\x000b?÷å­Àv\x0013æ7ÕË\x0012X\x0001\x001fÊÐ\x001a6Ë2gYÁa{\x000e»\x0003\x0012G{ÃR¯\x0005
¦\x0019älí\x0004q=Û\x0003â!Î\x000bHX\x001a- m
[§\x0003ñ=ßõe¸sT\x0005\x0011=J\x0008¥Á\x0008=FØ¤?7e9xq~\x00163
 Z©±\x0007{ìA±6oÚ/x±Gl Ò\x0002f\x0012$õ iEJ\x0014»d_Ò;±½Ëyvd\x0010¯âÈ=GÞcTöm\x001cÆò½DÓ\x0005Ä)@`tf{¼\x0019eÙj\x0011îëøÜ\x001d-Ë¶^åEÜèò}×ÍuÛ24Ü·N\Þ\x0003êÅIãñn\x0007ÏÝ<úárõ\x001fïëtáËÎÞf¾Ç)Î>ÑÜÅÙsÇ²û³SÅ\x0017\x001f¬O\x0012î °ÂÝPå_ÛÂ÷²³ª3Î47\x0017¯`²=Ýo(Ãí\x0006I\x0004\x000e_\x000b\x0014½²\x0008\x000b\x0007Ø½P®rû
\x0015R\x001d\x000fLÉSÇ¤\x0005ÊÄ¶â{½P¾ò\x0013P®ÖiÑ×+:ÁLFÔÁ÷ÇY¦Ð3ýLå_-~&<-_\x000fr2YüQ¼pÉµ\x0017*öPQ\x0005\x0015\x001d=¼2?âë¥\x001e*ír\x0001kãÊâ/½!>J\x0001yó9¼âëå)ïg*Qq½/¡NâËf)²¡\°ú¯\x0007£çÜï:mmÎKTXN©õ@\x0001!\x001b¾dðÁº+ÖÔ /Ëº\x001a®>c±²,[\x000c3MXX¾bLb1ô\x0011à
`
ÎX>ï\x0004ÈË\x000cáú9­|Í pï\x0010Ï®±Ê\x000fN­ ^Ü¿yûêc?¾y»~i\x0004µ2ý\x0016\x001f¥-HðdóIk×\x0017\x000f\x001e=}I°/\x001f­M2ìÐ°GÃ)4
bâ)¾ä³+§°§@w\x0015íÑì\x0014Z9Ôcõ\x0012_Y¾\x0015«\x001a\x001as\x0015ëÉÜ\x0014srl£B\Ï·\x0010!Hh\x0013»s¬\x0006Í÷h~ö{";Ù²ê¼<³·£m×}ÏÐ£	´:\x0000ñd5Î\x0000ðÉRv±,ödqRvùLQâ\x001e6òFc\x001a¯BK=Z3Z¬éf(·£\x001aÍÉ}³µ×íÜ£å)´\ÇoÔ°\x0015ªçð9ÊçD\x001dÁóW\x0003l¯\x0006_Üø°þÎâ$\x0005\x001ei¢â\x0002¹ÇãÏ\x0017\x000f^lä¹4\x000eì9p\x0017\x0007´K8Jõ(\x000fëÅoÃö\x001cv\x0007GÊ¾mÿtr\x0000s<Ía9F
ëAÜ\x001ehåN\x0007B âã\x0005ÄÊåRùUÐ\x001e$ì\x0001	\\x0005]@Êçr-Be7\x001aØÄ= .ÉA\x0006Ê.2õÓØ¶wèÊ}
d\x0018LY@{æÑO!'­ª\x001a¥¥ô³ZròÌI9\x001e=ùve5:ìépÎ¦ZáCßÎËî\x000eAÍu~PEg{:;K¡¶k­ç\x0008ÃïJÎÊ\x0012wÝë¸
Ïõxn\x0016\x000f¢ÜwÓz\x0003'\x0001¨\x0004í¾s\x0005*<ßãùië%\x00119(Ç\x000by\x0000s¾-=®À£z\x0001þz0-7XõÎÞB½\x000eò\x0019óöòk)«ã»ûq{ÜÏî\x000fÎË\x000ba\x000fí
\x001fe\x0001Zå\x0017\x0006çFßR~0ö®ùæýë\x000fëâøX¿.Òù\x0006ÖÈý?µOùC×æåçw/\x001e¯ö^ëÀ°\x0007Ã	0\x0007 wë\x0005\x0012bvb³î±AÁe{.û+2ïÁü¯\x0005¬ß¥\x000bØ²Kw² ¦."\Ü\x0012dÜ^l\x001cåÅkØÎoÁáì\x0016üÉý÷oÿø~ý..åZlWDÝ;Ég4Vn-Ñ¥\x000bé?O\x001e<~ðôËç[×\x0012ç7ápv\x0013þ9°@éyìÓÐò%!kW¼\x0017orö¹\x001eÌÍX¬DÍõB¼|ÖeØM½¥b\x0011®\x000b\x0017âûÁB\x000f\x0016fÀHlûoê$J¡»Îb©\x0007K3`Vä2ÃY@\x001a¤J\x0002Ð¥KèÝ`§\x001ceñ	²¢ÜuÜ£¦\x0000õÁn2%1¥\x000b©eûÁÅ\x000f3«\x001f½¤\x0000¯*wrà½o\x0012Æ÷
«\x001ff?¹¯\x001aéú¯äÀ%àÛ%z\x0006¹lXþ0³þ¡°9O°\x001c°Áx`-%\x001fç\x000b¯
ûÁå\x000f3ëÿ\x000bÃòÇåÿO\x0006\x001b}ÿÌò\x0012r³+£\x0006©^ãÛ$yEë¯YdcÞRÌá\x001eÿ³\x001eÍp)k	Âèa=\x001a`Ë\\x0002G\x001b\x001aöÖ\x001ftÃ\x0004\x001eßÿç»7ï×bl0\x001e<ê
S¸­ºÄÓ\x0013/¼¯ùêæñ\x0003ª°û<\x000eö8¸\x0013§èNí}D7pîÖU9VM4¶Y\x000bd{ »×>% æÇ\x00040Ò4ªb»ú
Y\x000bäz ·×B1×\x0002}ÊApr{\x001a\x0001ÄB&ªB\x000f\x0014v2¬\x0019\x000bkõfÑÊËÅ³\x001b¨	 Ô\x0003¥ÝÌS[öRÌ@\x0001eQ;ë&¾§ù\x001eè\x000b
 \x0012\x0015
Þ<üóý§?Þü®v\x000e¾¼ñ!pâA±<gC@æ\x0016\x001f`	§Eýøîæá×\x000f^}yó;ê\x0010|¹L0~÷·÷öÿ·ýptýpóûûOïÿóÍ}m|Ä>\x0016÷¯?ýõ7ÿëþÇ\x001f_SÅ3¡¡+ÑÝRhS9W×&ÑFK¾Óuo¹2ãùÝ«¿ù_\x000f\x001e?¾£"æ¾©øï\x001f¼zþí£\x0007«m\x0006Ôâ\x0005PêK@¿¼µçä©ã|®¬å`V~Ð¸õOo?÷îÌÚ±¼ù¢|çwõíà3¨e'Õg¡ËÂ¥0PËÆÌ\x00155IFý\x0019k7Ñòæ²\x0006­>*\x000c¨Õ¬JÔ²YÝ[P\x0001É÷.¨üÊ
x$jq»V\x001aSíÁLV]æÝ\x0011*PÙN5*Ô!-j§&-È\x0012Q¡\x000e¬-¤`\x0018õòZU¢?¶×¢Òú¬65Ô\x001cq\x0001Eý_V,\x001c\x0008Zt ¨mê 6T!.õmMi;ÛôÐÏ_|{R£\x0006[\x0004i¡f:÷/¨RëJ½ìVu¨tv=ù<µ©j\x0005(¡¦:³ ÆØ6UL×¢þ¿ù\x0010ÜöZE%`þýýOï>¾yûúó6#×såe@J9IC!Nb¼øõ\x0017À\x0012EÿþÁg/\x001f=]»\x0013\x001e Y¥~ÿñÿ½þó\x001f
ßøÔö§·÷ÿñi\x0007\x0012-FzSÛ%G\x001aÍ&òÉµÑç\x001fúÙWO\x001füÛ«µÛþ4-¸)&¤9N~JEÓ¡:JGïì\x000b^\x0005×P}w¿pÝÏab0_ÛÆ-`¾]v\x0002¶ö	ÿò×éo÷ÝføÝë÷?uÓénþHÏ"oé­õóK',\x000f¿¤¬TæH.x¨qFÊ6_ü¨¿»{þ¤TwóåÍÝSz]ß\x001döÓ§¿þ©£~òîí_~¼ó¡Fá[yû\x0005äHé®Ë`â²ôÐÕ¯\x001c\x001cðÓð\x0019ægO¿yüàÑÕÀ¼óû7æ¿ååºàÅ§÷7?.cu~øóë\x001d6,v³·UWl\x0008µ	VÙ´å^mh\x001c^Ôjê4òx¦S"ÌuË}ÿöíû×ïÎÂ´/¨­ÈÍ·{V¢¥ÑØ¾:èr ^Z¿\x0016<ÅA{¸h»åZÜ|»±\x001aÿ\x001aü\x000fÝw}<{~ðU¹ìÔPxÐ´\x0016ö)ñrûx\x0008Æ×Î8tãØ]lÔ\x001f\x0005»ÿé/÷Úå-û®\x0015ªÌ!Íl©\x001f9\x0004\\x000f\x001eê­\x0007O¾yðÕon´ØÓ¢:ÚgËÀê\x0016à²\x0004\x0004Ø]v
`Û\x0003[­yKLæ°\x0002\x0007¬3ÈÂ¾YxuÎòº×é\x0003uZxS¼
ËÂB^\x000fÐ'q}ëÕæ].Y\x0016Ü\x0018(õ¨òf1¯T\x001e\x001f\x0000\x001czà ¶/PþC\x0005\x0006b_Ñ2oLñÆ7jyÑPúÒÂò%\x0017^ÃÅ\x000b"\x001c¶"R\x000fÔ\x0006¶¤\x0006ÕÀú8V\x0003\x0007±prëIàÜ\x0003gµ\x0003=ÅåÈâè5»Z8³K&\x001cåùqO\x0014Ã¨ðÒ°j!¦7?Ç&Fdb\x0017Ö\x000fGÄ£Æ©E\x000e3UDW\x001bg¾"¡_B\x000c°~3I<è\x001ch.S¯´\x0010#.¥ÔËýI\x001cÂ&\x0012:\x0018\x000eÔJGi"UéèÆLb	Êg\x001b»£\\x001b\x000cR\x0007Z­Ë\x0018)¥¤\x0019Y;3>ÊSÀ v V;»$åT\x0013\x0007*«ZL\x001cÅÀñòQUÁ;h\x001dhÅ.»
kË«Jg¥Ù¯¥tTä\x0003ÒZêÒÒ§r±ntË ':Qx1oHG)\x001d\x000cJ\x0007J©s\x0006\x0004Ã%äiTTBÏ\x000bø¸\x001d7H\x001d¨µÎ\x0001\x001ds\x0017\x0013c @ü0Æ£¼\x001a\x000eZJ­sÆ\x0000\x00171ÔA§ÅÄ\x0001Rù(qÆAêP+uù\x0014\x0011S,Ã\x0007ãÄáOLÇYx<Ñ©.Zz\x0014¨w5QVq9$ó*Î!\x001eµïpP:T+O·ÃÈs÷\x0012þ¸ÃÖÄ t¨\x0016:*¯áC¨¸#NæES<Ê\x0017ã t¨VºÚpt±±ÇÚNºØ\x0018¬,cwÜ¾\x001b´\x000eZç();UOá\x000cÒ/ÙSÈc4GE\x00138è\x001dªõ.¶KR\x0008XçØ\x0015\x001bcs\x0015þ¸U1\x0008\x001eê\x0005/Éª°\x0001êÈ²bcqÆÙ\x001e\x0015Äã w¨»zGY]±«]»É\x0015,¾Ø\x001fe`;¨U«]m¼\x0018Øû:A\x001eCäÔñ0_l\x0007¹³j¹+a\x0004Ö%&ÎIÍQäÃÎ¢vÐ;«Ô»bcG/ßÕ\x0019Gy®G×ô.ÃQÂWZ½ËÖË\x001d\x0010åc%ñ³(\x001eF<\x0008U
¼¬ã%ÑÄBdÎþ°;\x0015;\x0008Õ
^9g°«@DÚÊa)s`|Ø­ \x001dÔÎjÕ\x000e¡Ç¿e\x0011/=Y\x0017ûæ¥\x001fÒ\x0001ÀØY­ØQ_CË~"@Ë=Xî\x0017\x0003;wxØAì¬Vì\x001a<KÐ|ËfÃC	ÚÜaê1ÈUÊ+\x000fÕå,6¦ÄvÉïpbã¸òj=Oì\x0006½sZ½\x0004äe\x0019\x0008î´ºRqÞ9¥Þ9ê\x000cÀ7%ð¼4ÈÚ­ÊQ«Â
zç´zGë8\x0003ùi\x001d'±q>J=Ü wN©w®á±*´u-ùËÜe£ÄÃ
ÎÍ)£*iËWmÅÏåz¾+\x0011ï{Æu«pZWÆß:^\x0013Nò[Êñ¿­x7öÃ¾óÚ}Áosn¹6^\x0012_ø¬	G9
{jò}
5ÇF°S\x0013n\x0012§qH¨\x001dýýqJí\x0006îõà+øª0Q½sM\x0015µrÉ\x0012\x000fÛ]Û÷ÓË»\x0018\x0019é¤W¹±Î¡¥kdÁ>LP\x0010Î±ñ¼aðÔe\x0000È9
ÐÐ½@½\x000c@±7Ã´ûgàN\x000fî¨¶×¥Ü\x0005LÍöÌpØ{¯ýÙB±úâè\x0005ïÂéÂ\x001c»{ÏlØÙ\x0018ú»¯ßÅÑô\x0013å\x00016PV]á®\x0014-à¶Ý\x001b\x001dvÃlãÏ\x000c\x001e¯X)6K \x0018Ú
]ë\x0004©dY)ç\x00067×\x0018ü\x0017¸ñ}+¦ú®Ð#Ý<¹s\x0003åºë¾\x0000(F¥Ü<ï\x0012åzï%\x000f%~ÚÊ/ÿ®\x0007ê¿ë³¸Øã¢\x0012·Ô\êá©c¹éì-\x0005+9­ó¸¶ÇµZëÚÚA¬\x000buò'=[\x0003o¿6Íéz\ßãz-®£ÖÞ\x000b®s,©\x001b=ãÂV&ý\x000cnìq£\x00167H1/\x0016ùÎÅ°´ÁÍ=nÖâ&N!Î\x001eO¯}9ñ\x0001\x0016ßª¨Àír¼é\x000b+æx}¤â(y8nn9©Øo\áÏáLíÉrmgVÌ\x000bÊìªy³7näCÎñ\x000e{
´ÍÚxÓcí²w]çpÃ\x001b´«!×¶e9l¸\x001e\x0010Å\x00198ÈÁà\x001a@ë\x001b¨Ô}C	5¹øÁ´gT\x0008\x001b)-s¼o\x0000­spX{]\x0012¯£\x000bq~\x001b\x0011_\x0016üV½Õ\x0004/\x000eÎ\x0001µÎ¡\x001cP}-\x000f¤A_bßÀw´1\x001fµÙpp\x000e¨u\x000e\x0007i¸¡DhÍ¼®-ÍjÆ\x0019Þ1ÌQÇ9(aYÙcuÔ5í6Ç%\x00139Ù¤
8\x0007µsµ\x000cÙ×ÒJ®ö\ð\x001bÏ§s¼nàuZûÚÚËR\x0008\x001d¿§\x0017ûz.ÚÊa³fpw\x0010\x000bToö¥%²~7G­ßA-P«\x00164\x001f¥7d)\x001enù1ûÒ9ÜA-P­\x0016¡¶\x0010È®:NVo\x0014ë:{uÓ¸eÅº\x001aÐ'i#°À]¬ë\x000es\x000e¶¡ZÛhxr\x000e\x0015`\x000f6;HÕJ[\x0008u`K±®Ë
Bï»Ík7Ææx\x0007­°j­È\] gLk,¿2Ålð ÈÌGbµTÚB¨¬\x0006\x001by,\x0006ã·jàgp\x0007¥°Z¥2âE*ªA6/J\x001ftÔ\x0005\x001dÂª"+3§\x000cM\x0013¤\x00144¦|\x001dÂj"Z\x00116ª
\x000b\x001dË	T\x001bzy\x0007¥°W(E®«×Ri\x0017Ä¼\x001bs¸RX­RÐkcµ®5\x0012]LÁ:ð¨0Ý\x000eJaÕJ\x0011Û!³l6~¹£jL6oØx âuÃ±Â©\x0015 \x0017ÞäN¾Lê\x0010ÌVZæ\x001cïà\x001cÖ9\x0018W;Å\x0016Þràle\x0013\x001c¥\x001b\x0019H{=î°\x001cv9mæ5FÊ²÷±\x000eºòÃrðÚåàÛ)\x0008chË\x0017Px9wb¯bïé=¿éñÄË\x000f·%LÇ"\x001d?^Ok¯\x000f4u©EfìÎÀcÌ\x000e\x001dü \x0016^+\x0016;eÄ,Ya\x0006Z\x000eé(Üa»yív£\x0007 6/$®\x001f.¼Q\x000eÅÛ=&xÃ°Ýv»\x0005#oñ\x000eµ\x0018Df\x0019\x000fòfaØmA»ÛhÐZÕâ\x0018©ÿ!ß§Kó§Á9Úa¯\x0005í^+'ø ¡Ã2m¼Jö¨×
7æ¢Tyk/Ç7!Ë
g³\x00041'IÎ¥bÌk±Cún|~-Áu«ô?ÿõßÏ>\x0014¤7ûrâ\x0003eÔ|\x0004¨¤ p¿¥P$n3³àæÙòG[¯Å=.jq)½<1n¸å',Ï\x0002Wh7:íMÑÚÖþêëz\÷k7®ïi½\x0016¸ë^9²\x0003É2'!%¦5ÛÅ\x001cûiCO\x001bÔ¶]\x001ab,¸T¯Æ\x0005T.!ãPg
7ö¸ñ\x001aã¬[ó_Èº¹Yw3ux?nêqz£9~^I\x0000\x00138Pç8²Ðnçuí§Í=mþµ\x001b·{'0¿rëÂ¨hjIëÍ?³íA¬ZÏ~)Ó\x000ez\x0006jAûEL;\x0019¨Õì2í fp\x00051-úu7ëºöó\x000ez\x0006jA£âðjÝh¥WYFÎv	Ôtæ\x0018ÜAÏ@-hµÏÂKEâ¬¿ æ]k9;è\x0019¨\x0005ª=ã:\x001aZÍë\x001b®ÛÌ
ßÏ;(\x001a¨%ÍÄ:B±ðÚ¥GCís×m¼ªÌðâ i¨4\x0008¬Ux\x0003m<Þm(¼éX\x0017\x0007MCµ¦\x0019O¹±\x000boAú{é#\x0011Ý¸Ùâ\x001dij]\x0003W\x000e»Ìë9_ l·(ë\x00017bOñ\x000eÂjaûÅì;\x001bªÅín_0Þ2ÐÅ\x0005/ße\x000cðo¨;ì\x000eÔTöWõ¼9Rr´Sã\x0007A\x0007ë:\'\x0003SwØÏsbÏ\x001aNJq©ý©
\x001c@jåÄ v½°z\x0006Ôö V\x0005\x001a%7+ÆÄ\x0017y\x0005Å¢vUzg@]\x000fê\x00165-jùµ§\x0018T8ízNÖ\x000c§ï9½3Ë3O^B¯Ôzo80«b;\x0003\x001azÐ \x0002µr¹\x0018©_\x0013·ÍRJïp½ÓÍ\x000chìA£\x00064,¥Õ¢[LîTöY\x0001M=hR9§È£\x001bb\x0002i\x001d\x0014Ã:X?Ïpæ3«\x000c\x001aA)Ýý½á\x0019\x0003Å ë·á\x0013 §\x000bÅÛ\x001bå\x001aMÍ¢Øhs÷ë=`g@GYRéR}!\x0015äËÜ\x000e2é\x0011 .JüRc)\x0002
,LIR³\x001ebÒA@¥LiÁ«&ÅVÌe\x0003\x0014Ø¼Þ\x0016qtP&PIÏ2](u mióiã¯?ÓÌ\x000eÚ\x0004*qÊ#ÓbS×Þ\x0010Ú~2ëé\x000cè M \x0012§âè3ïüÂ,Å[à\x0014\x000f	K`\x0010'Ð¨S6'uòËÖB\x001a\x0000d®7\x0002 ÅÁ¢ÆÒ¥\x0010²Mml\x000b¢ôu±\x001b½sfH\x0007o\x001aoZ\x001ezBsS¥Ò0J£C»Ñft\x000có5îzx°T´­«z\x000e^KãçØú88)Ô8)j	çB%ÅÄE\x0018TîmX/Ñ!\x001dö>jö>Ý®YvR(IªT:0Øpy\x0000È,é\x0010ï¡&à£zc.¼ÖJLÙKYî~\x001d©\x001dö¾Uí}º\x0005æ½o	!ü\x001c\x001bé!§\x0012ÿÝýxº×È)RG*§N?%ßb©õ¾=s¬ß¬ßk\x0014×î#hÈ\x0008ªý\x000fa¡s\x0005G©U2	ln%N=]õH"L±ízò\x000eÞ{\x0019Ë)\x001aðN\x00014aìÍÇüýæ÷ï~|óîãÍÃOï÷ÜK9ê<!+·\x0001Eú9kÇÙËAÀÃG/ïn~ÿìñ£g/o\x001e¾z¾q1Õx±çE-¯\x000cÞs©i¸<³ÂEïª@µ=ªÕ¢zGi\x0003D\x001btJ°N:+R'áËÑæy]ÏëÔ¦µü@\x0014|>ÂÎËô/Km¦Áõ=®×âºÈ©É)º*:®4tý ÜÐã\x0006-næcv
Öñ}u\x0012\x001a`ñò<\x0002\x0005nìq£ÚºPG$\x0016ã\x0006©Ç³m§Ã¶Zêi\x00039\x001eé-­Þ%>\x001dF\x001b.¿\x000e)xsÏµÖµëñ¨m¢Ô\x000f££,Þ|ùµp·]\x0010U0êå\x0010¸
úàfe5\x001cäÆ`T4µ¤YÉ1¶A´Ê®\x0016\o.OS\x0000\x000f\x0006jM«Cß«\x0006GiÁë¤õuÑàËw
àAØ@­l6p¤bî:üX\x0018/\x001e\x0014À²ZÚã\x001b¹\x0014çÐ¼D9ýCYß\x0007ù\x0007\x0018´
ÔâV¼X­\x001a+Ád\x000b\x001bù>>z{¹´\x0002xP7PË[qcÈÑCbaÇ¹õn¥¢\x0002xÐ7P\x000bþ\x0019©8°[îªxàxT´\x0003ÂVâÐ{>\x0007ðÌÈÔú°ùr3\x0005ð q Ö¸ÓèúåØ&K\x0018eÏåËu°óÀ8h\x001cª5.d.ã^Æz\x0006\x0019k%Hæ(àAèP-tÐéÑÎKc./Bg\x0002\x001eÏnj¡£i0¼!Ing¥^ÈËéõ
àAèP-t\x0000-ìÉF\x001a\x0011X:ZT\x000bC>H7pÐ
Të\x0006pStÛZ\x0005Ë°o\x0015¸\x0013F­\x0013âÔj£\x0014iâ+wþÑ­4¼V\x0000\x000fN
µNùºdyÜ\x0002ÜÚå\x001bÞy`;ø\x0008«õ\x0011 %o4\x001c\x001bíb;\x0017y8êÔiÇ+\x0013í#\'\x001bÎ·©ÙIªû=^~P\x0000\x000f\x001bÎj7\x001c
0("KèQ
x]:êúÌ\x000e;Îêw\x001cÜÖ¯
w\x0012åËE8
ÞaÃYõsòPQ\x0016°îçEªÅ¥ÁåKõy`7l8§Þp.ñ«jYÁV®¥
°kg£+W9¿\x00006|\x0001|ê?ûÅûû\x000f\x001f^ï\x0002^¦,'Ç=<½\x0014·ßpÒÃs;\x0013øÁÍ\x0017Ï\x001f¼xq·\x000b\x0019{dü@¶=²U#c(¹Sj6¤ÖIN\x0008®D\x0012*d×#;52UÌ##Ë\x0004JLÒ9\x0017·z?Ì\x0012ûØ«:K\x000fÇâÝ$-PVÅç¦Oð7èy\x0001ËÂ21SÚ\x0015âãc\x001cõÈN1ùSYdJxZ\x0015\x0019Q2zä¤÷\x0016¶õyÅÜòÛ{\x001cä\x0003s¯Bö(ñ8}nªÊ~â~l¸9\x001b\x001bþkµ2ÊwôÉy´0;É(¿!\x001du?Sd´Ù«µë¯õ¿¿ýÇßßßÿxóÅë÷\x001f\x0017¶ÏG¥©T:Õ©Ç`ØØ\x001e6ûÜ|u÷´üõã/î¿\~þYxìáñJx\x0017i¨\x0003ÁgÓÞó£¤è²â·:xÍÃÛ\x001eÞ^kùå~±|vÜ®\x001fËOÅò[=.æÑ]î®µ{b£Cgô$Ü=
çÉ}Oî¯5z\x0006T÷S¦Ñs3úfW²yøÐÃ«ÍÞàÁò¥W±¼¤Úx»Ñ÷@\x0003\x001f{øx%|\x000cÒeÊsÅÑ$iìÝÁË&õðéÚec$gà!³å¥h?ÖKæ\x001e>_kù8XMòñcù.\x000epÃ\x0008\x0000µé9»ÚìsUAZ%Pßd§¡\x001fÕõZy
Ëj©¶÷·\x0010X^ßl*8\x000f?\x0008\x0014\«PÔ=½
\x001c# ~£Y~Ð(¸V¤ê\x0013\x0001Ã)Â-uÉ1I\x001bþ°1?W\x0003?È\x0014\«S!Kö7õ7\x0017o\x0019%£Þ9¤\x001aúA§àZ¡JV&\x0011²ê#¾Íí\x000böà3\x0008\x0015\­TÐ}{\x001f-¶ÍöùX98{¸ÚÛæ/\x0003JsúäÓzq\x001e\x0007o×zûèd"30mRÅÇ¨\x00106Û\x0016ÎÃ\x000fÎ\x001e¯uö©%Soa.\x0019EhóÁ¦\x001fÏR×\x001e¦R±Æ6©JÛ\x0018\x0001©¡\x001f´
¯ÕªdÐæÀy{Åö\x0010ÄÛovG§\x001f´
¯Õª\x000cD¿ØÞ-·\x001fÕörá\x0018üå«~5ý Vx­X%Û\x0002Lj/	lû\x0016`æÍ¡\x0000óô»ÇkÝ}wVã\x0004ßî!Á·³9®g~p÷x¥»O\x0010Në>qmL\x000e²Ð\x001f\x001bæØÁcÚ+=&=¿ðDbcbëg`¥ñBÀÍÙ"óôã\x0005Î>'\x0019 g\x001e\[9\x0008þØ0Ç\x000e»Ö^¹k)\x001bPü=Bë(mÝÛÍ\x000eÌè~èµZ#ü®×ª:Vsmõs³\x0018en þ×úÍó?\x0003ú«ÿ\x000ctwÌÕ³99©lRÜçzk\x0007ûüÙ\x001f"^ÿ ÜRÖì¤á\x0007¶ÀÍ¬ë.\x0005Ïÿ\x000c×\x0007Ê\x001bJÀ\x0017²é6säìÛe²Ýjß«¸	?UßÕ»ðû«/Ã}ä|OGßzQÒ¢ÏíöÃ\x0013üùü\x0019"÷Ï\x0010ÏßüñÝ§¿î\x0000¦ßÜÆúAPÊù
\x0000kæù£/½ú÷Ïcb
Lº¸¬¥¸@Íd\x000cJå^JÛSZ\x0005e\x00082eÎÆKoé\x001dóæ5Ù^L×c:\x0005&Í:¯ß<ØË9É\x001a
isbÐ^Lßcz5yÖoÙ8mf\x001fåöWkn{)CO\x00194Æ\x0004Éy¤ñ\x000f2ÜÊI[÷\x00107'\x000bîÅ=fÔ\x00183Ê}\x000f½17:\x0019L`¦\x001e3i¬i¤j¹h}ÎOC1ø¸%Ã{1s\x001b&ÍEåÁ\x0019Ò,4\x0016Î\x00030»;ü<ÜáO¸Íñ4kË\x0002ç_nÓÙ9jF9kµ	uå\x0010dNÎËÞo]´îå\x001cD\x0008T*d9!)Ñ««Ép¢Ba;:ÙË9È\x0010¨tÈó`\x000cC.FV§»\¼39È\x0010ht:ÖpU\x0014q	§ÌG	\x001b]\x000b&8\x0007\x001d\x0002\x0010yân0´IØÅÛ\x0003\x0001÷r\x000eJ\x0004\x001a)¢FÀÕy¦,Ó¾0H\x001d_¾\æ;É9H\x0011¨´ÈÉH½åÈÞì)a\x0012®÷\x0000à\x001c´\x00084b\x0014%\x0007:iðÓ[·>}:Ä\x0018J¬$±Ð#L[\x0005©bp\x001aá F¨Q#o¤Ä¿ü½­ã[K¥ÞhR39¨\x0011ªÔ\x0008øÅ5\x0015¶A=ÐB%Ê-¿s<\x0012iÔRÓ93}y5¨Ö4bN{ÄêÄAP#F-¹--áL\x00029ml?Èìå\x001cÔ\x00085jD\x0007×~Ð04îWR«3·Gp\x000ej\x001a5òÕ(Ñ\x0000,ÙíF8Ãå\x001a IÌAP#FÔ%·v$e³s¯$\x0015Ï.n^
îÅ\x001c´\x00085Zä½\x0004.cÛ`xæ\x000cár;IÎAP£E.ÜºÖ|ÆñfO\x000e¥g\x0003\x001c 8H\x0011j¤z\x001fðñ
¹Ã.Îo×Ù;1í DV£DµÌDÚ$9¾õJ­MÛ|òØË9HUÝÎaÛë \x0003\x001an¨Ù\x001b=±'8\x0007)²*)jçLjÍR)\x001fÝm>îe\x001cïæ4:ä2:ÔÃÜt¶GÈº\x001dtÈªtÈ4[Zi~ÔRêÖ7FOìç\x001ctÈjtè¤ÔÒM&zuÚNoGìõA¬JL«RG×úÍ\x0015QVMëmÐ'8\x0007%²\x001a%r^j½©Ù4·ìNQZäõ.Ã\x0013\x0010Y\x0010Ù,é»6³\x0011¤èßmÎCßË9(Õ(\x0011õjw|x;\x001d6$Õ¹\x001cÞÌ\x0001ËÓ
RäTRdäNÉÇÜÚ\x000bÆÖ§í¨Ó
Jä4Jä@\x0006JH8gÝÖÛO`\x000eBäTB\x0004rØð!¬Ù'\x001e±Ü FN#F6s`*:Ùâ¹ÈóC¢÷\x0015?{9Ç"\x0018Õo^xN=¥ã¡#¢97(Ó(M·µ\x0018fF´>½2è"z·ùèºsP"§R"Ë}¯SA\x0002,ÛË!î\x0000ÎAFd(ÃÒ´A:·Ïîq£¶y?æ Dn^¡\x0019]u\x000f¹ènù¬!cX"=&\x001d9\x0008Ó\x0008\x0011¹K¾§IÐÎ\x001a±õì\x0008\x0007\x001cýàà½ÆÁ[/Tr"ëíòã\x0000ÈÁ½û_k\x001a\x001f¼»Wyw'7sÅoÊôpj\x0007y?òãûºÊoÚÖ\x000e©D!"!¶;#Þ_üà¼Ê\x001fI_ØVÆ¥Ñª\x000bla{Õ.G*ª\x001d5o9\x000bfk@wÄ\x000bf\x0018vyPír\x001aI÷\x001e\x0002¡]{\x001c\x0010laÿ\x0004ÍþÁD\x0003ç¥w1gbg/W\x0016ÕõÃ\x0006

2\x0015(¢í"è>¸ÖÄï\x0008Îa\x0003\x0005Í\x0006*91µ«m/-T)õý\x0000Îa\x0013\x0005Í&¢yíÜU\x0019P4È·}a}Å~Ì8l¢¨ÙDÉq1½¼ð6ò<ú<ZÄCV\x001c¶QTm#Ï¹É'l7I¾\x001dÕí\x0011¹}qØFQµäæÎl2¼ÂÓí@.\x0019Tª]ä¥'ª÷F*¿³ËòÙÍfð^Îa\x0017Eí.bNkÛÃ 7ÌÛ ;9Ó°J¢´\x001döÚMRæp¸]$·sØFI\x0015Íµ\x0016`.z©¬ÉAÒ\x0000¨Mã\x0001ÃúLª§¬_"7
ë3©Þ²4]´ÎÝÊ\x0004\x0018Ö"À#Vg\x001eVgV=½$\x0019÷`©?<\x0011ñíX6û\x0001«3\x000f«3ë×+¤1RüBo\x000cpyððYùfÍiX¶¸¤ö¶^"Û#9l¡¬ÚBIÞ^ÐC\x001b ä\x0018lÜåÁ³s¨¨\x000b´+eRz'¯Q'W `6\x001b©ìÞñç¸e×kpS<3£DHò\x0010S~È;
ì\x0011\x000f)þ6*Ûz¶Û\x0004Í:y@+S£ÿn¬(ÿs|%òÍ×ïß¿¾ùöÍ?þþöÝÇ\x001d¬Ôá«Nâ©Ô?\x0004)77ë	ýß<º{þüîæÛGwO½ü<®íq­\x00127\x0004Àds[	6È¸ªâþI^×ó:­ycK\x0000%ûTÄ\x001b©êY\x0019A¡à
=oÐò&#=CR´²tcJÒ<á ØÔÃ&5¬¿\x0015VÓ:pe©øry}Tñ\x001cnN_p%~7[~m ±UÒ½*6V;¯w\x0005\x0004\x0001\x0018´»-9©£¡Áê2rÏ¶1àñ(ÞÁÖ% ^\x000bnÑ`®µ|¶.%'q\x0007ß\x0000ZçP¼Ì³+çWYÀ%~`çà6&oN\x0002\x000fÎ\x0001´Þê½¹­ÍÒ\x00136±¥ZÝÅõ¤¢IàÁAÖCÐ2\x000cLWÀ¼$ÈÛÆ Æ9^\x001cÅX½\x0013´
G\x0013\x0007db \x000câu\x0007\x001b\x000e\x000b\x0018Õ\x000b8ÛÖ}Òvå\h\x000eâ ÁèÒ5	8j=°·^$cy\ã\x001aa©Õ6çN(\x0005Ú\x0005L\x0019ÎÕ¼¦=`ø,ËÁ^ô¢	vÐw	x$òU,âÈG¡L½ëxÓeëÄ­Áú%çlLym¯À¦yq¼6¬··ò\x000f|õ:ÇÙpâ\x001c»\x0014zî,¥e¢MÉRsÒ»ÖÁú\x000bì^nß%ãe\x0007\x000eÍv¿|÷áÃü÷{\x001aã\x001b:Òó%¸M<¼\x0013¬Ì&¡áÃ«§£¥×îÏ^¼(à[­v\x0019\x0018{`T\x0003$ÕQZÌÔ²\x000e8]3ûð.óûmOlõÄ"ÔÉ;+ÕàL»pÞ¸ $v=±S\x0013G<=4y~\x0010+6d\x0007\x001b×=ó,±ï½ÞÆoôTkC¸às=æ÷ã\x001e7è
\x001cä.:Pþ-\x0013·gfû¹±\x0003ûc\x000f\x001cõö
r£æCºspQq#¿q8õÄé\x001a\x0013Ëd¶Øfõ\x0015\x0013Ë#9¬\x001fHgsOõ6nCU|*Ç}ñl\x001cÐÓ\x000c±»#4iÑÛXn\x0002CJ2f\x0007BéÖ\x001cF<ª^îbBê³´a-6\x000e²ÝFÙÕ$ò \x001e \x000fª¶ã,
ª\x0019bù\x0008RxgýÆ{å$òàAïãÒòsõeUãz <Ë;87Ð{·²Ý\x000c×\x0011QÙ\x0006/äØ2\x0001Òåùa\x001aäÁWÞY¤SE9Gq8´Ìcg6zçqØ{¨ß{)Kîy(ÎYÜÅ©À\x0008òQî\x0002½ú½
UÄÔD+' Mj+qýÕÈ`Îâyê®ÉF~qÿæíÇß|ýéû×ïw>\ÙÀm .Ûä$¶%\x0008­Gó/\x001e<zúòæëWÔ³êó°ØÃ¢\x0012VfS}tc§¹ë©ós¬¶gµ:V\\x000b$^³Ü\x001d(ËÒ¥ªc`]\x000fë°A\x001eæÓå#\x0017/·>¾hÕ÷¬^ÇZ\x000e÷\x0016\x001a+WAi!\x0004¬\x0010s°¡
JÃÆæsKäãx{åÐ*$×¿ç`S\x000fÍÍ²\x00198§À\x0002ØæºÖï/§`OÁäâ¸¶È.ê£Añ\x0006\x0000-Zw'6î§5ö¼ÓmöîþøÓ»·¼ùêÓßî÷½[©EÌ\x0011FËíIw¶èÛ\x001aíÝO=ýòæ«Wx°ù®lÏ;îÙÖqo\x0016·\x0004\x0005u\x001af^z#Ë3¢Ì¢9ì\x0007ÑÚÖ*i=J\x0017)-É\x0015Ñ»>²j\x0012×õ¸NZ§Kêú-\x0013Ar{èÂ£ë{Z¯5nâ\x0008a1næ	 ÞÉ£\x0011®·¹Ä
=nPn4ê
Ì/ö¦=Á$\x0006ü[ñ×$nìq£v£\x0019\x0011«uQR`£\x0014Õ\x001dVó¸&qS´ÖÅÁºü \x0007!\x001enÝÜãfíNæuË\x0001Se¥Ð¬»>æk\x000e·»\x001f±§}Ó¼9·§²×¸SA¢ËHæ]o#:É;¨\x0004(ebi;Ü\x0016¯¼'·çdXN¤\x001dT\x0002´2\x0011QF^RÚ½æ$\x001fÂ¬_3Lò\x000e2\x0001J V~µ;fÍ/8­Þ£T\x0018\x0006¡\x0000­R¤Üµ\x001bcYÃkZ\x000ePV) 4çPÌ\x001b$ßÄ··õÊöIÞA)@+\x0015Ùr*m^ú®s·~#ã\x0016]ùÿx\x0007©\x0000­VPÛ|¯´çoÆ]?þNÂ\x000eB\x0001J¥ OlÜ`¥"2É,\x0001·Q =P R(\x0005®?ËQÜ®<4Ö»|NÂ\x000eG\x001fÔ}ÀñI-SU¬¬\x0004\x000bröÉë\x0017¼ãÙG«jÈ^Á\x001bIX§Ü>1îz\x0012å$ì j¨\x0014µ\x0013#5
ãD*çdÜõòÓIÜAÓP«iÖñµXáµ2Ý+ùÜÖîzrÉ$ï i¨Ô4j^aTy¦6wÒnd$NÂ\x000eZE£¢ø³\x0016m¶>fwP4T*\x001ay19ZZÛæÏx/!®W\x0004Mò\x000eZEsK'¶jß$u­¡Øw½:yw\x00105ÔÚ/véd\x0007U³jUK-\x0015ªüÞ¥ \x0019á\x0010ï lV}©×\x0012#¶\x000cvz\x0010û\x001eåÌì lV+l\x000e\x001b¯·©²~9­¨üqÖ/x'yÇk=­¶ñ$Ej|éÙæ|ýzéÅ$ì lV«lÅùJàPö\x001dOÊM\x0011ÅùFs\x0012ÛAÙ¬VÙ\x001c7ì,æmóÏ\x000b.ßm¥5Lâ\x000eÚfÕÚ\x0016[§dû\x0018róeGwÐ6«Õ6oÚU9Å\x000e­rÈ:{Ô^\x001b´ÍjµÍ·â\x0016ê¶Â®75×\x001b67HÓJ\x0005eËr\x0000\x001aj³ðf£]¯\x001b¤Â©¥ÂIè\x0010BjËÁËÅi9\x000c\x001däÍÜ \x0015N+\x0015Ô»C_0­P/Ë]õë¼T8­TxÉ\x0014É!µèIÛµ­ñ	H«\x0016ô\x001a|²¯ô÷\x0014º\x001deßA-V-|3<½ºóUJQäb£(`w\x000b§äÛ\x001bñ­A5Ðäí ËH7ÈSË\x0005Ê\x0000¿\x0010L\x001bA\x001cxÐQÈ
rá´rQ«}ñdß(÷\x000e\x001bµN¼ÃQÈiB!ËÑ8Ðm$ó ¼¸-0Çë\x0007½ðZ½N´)\x00179r\x0007åpÐfóXx­XdËÏ@ò&í\NwPv=\x0017r\x0012wÐ
¯Õ
)wÚk®UéVõÁ±¼Vx­V¤%1¯Ú÷ÔÀ¶XÇ\x001euîÇ\x0001­VÄ,Ã\x0010C-\x0002¨öm¾\x0017zgóVxµVØÛSè ý^dx\x0012\x000eGá\x000eRáµRë¯yOÍ½Ð
¯9*eÀ\x000fRáµRQÌË\x0007yÊkËÁËÉ
ºþ÷Tx­T$'·$Áªbe«]/Ç£
P\x0004­P¤(Np¹	[Ùc\x0015º\x000c\x001fÄ;hEPkt$,Öu­õh«9¦ù@\x0007ñ\x000eb\x0011´b
gp\x0016û:\x001alÃÕ°Aì»^)6É;EPE\x0006Ç#^w°\vÅ³Å£½C\x0018Ä"hÅ¢¬\x0007~\x0010¢\x000eÐÊ_Å¾ñ¨{¨0¦)Å"C\x001e
¡ÄìRâ\x001f}Ûoëµ5¼Z\x0004¥Zä\x0012ÛzÐ\x000c\x0010n¥Q©Äf\x0018\x000es\x000fX\x0004¥Xäq¡¥&¼z£<\x0015ãaÏaÐ Ô\x000c\x0000WëF¶HUf1ïúL9Þ8\EåµYqVrËG%\x0014Ò\x000f6Ê¥:u/9wP·¨T·l\x001c)ÞAæjåë\ó\x000e\x0007á\x000eâ\x0016â¶t\x000ecgfá4Ê\x0005e9¤õÚIÞAÜ¢RÜ2x.*Î¾Ä\x0011V¯ÜBQ]ÞA¼¸E­¸Y\x0019RìkxÊ\x0018M>å\x001br¾q\x0010·¨\x0014·ræáÆÙÇÔzGÉF»Þ&zw\x0010·¨\x0015·âså¯qÓ)Ù\x0019e»\x001dtñ\x0010Çäi­¸¡àÌG{° YfGe ÆAÝ¢VÝ¼9ÙW\x00124h^k³ïz#ÄIÞAÞ¢VÞ°çö!IvQn·¸QÃ?Ç\x0006yKÚW!Ì-EÒR:½mÙEÕ\x000c-`Z\x0010é\x00003×IïARl\x0013%m¶\x0005ìÎ\x001e\x001dgÎ¡Ñ¨©)÷AraBÛz)ØSÆäQ=Ç\x000eV]srÜ(\x0002lÇ9\x0010¾^ ÃwgUcAªÆ¾ºÿðñÝÛ/îß¿ÿÇß?Oë\x0000[V*5[¶-1¥$Ø¯×»~õàÅËgOo¾xð|³öY±gE\x0015kñmöVzyéObÚ¥j9Ð­JÇ\x001c¬ía­Ò°ÖK\I%-5¹Ä\x0016ØV1¶^X>GëzZ§4-e$sk+°<æÊ\x001a\x0007LíÖ\x001fcçh}Oëµ6pÇ>Ã]¸ÊM­\x0005ÞúÌÅ9ÔÐ£\x0006­aÍ©¿`æWc*$õaõ²d6ö´QiX\x0017n\x0003¶î5Ï¶RÔ®o5£M=mÒÚ\x0016x.\x000eu{ç6aÆf
ëé[s°¹ÍJÓxðÔ)µ¶¬Û&ÂëS§hû:±ÐêÄ¦mKÍ\x000fÙ´ ¦
Æçüz3\x0007;jVÄ"¶.à¤¹µ­ìjc\Û\x001cî \x000c dä%>\x000b­k\x001eì\x0018\x001dA\x0019@'
%Ê²}×ÃÄÒPþB¶Ùúõô\x001cî 
 ÕÜzKÃ´³'yðëíæp\x0007y\x0000>PG\x001cÉé,oëaþ´ÓÀ`Ð\x0007Ð
D·l\çd\x0006{1®a½^pvÐ\x0007Ð	3,K7S7¥Ú ®Õ\õvÚs¸BV"2È]\x000e=È×¨Åºr·çÍzÆË\x0014.\x000e\x0012:p¦¬\x0000Á-ÖEîZÖ\x000eá(ÚA#P©\x0011HÄ¼tsæì^kHõôÓ9Üñ¨£;ë\x0014ãfiTîIµ_$\x001bº°^#6G;(\x001a*\x0015
iøy5.=¯Øº\x0016É²r\x000fZ	 ¡VÐ¨ó"¯[\x000fÜdßBë\x001c×s]æh\x0007=C¥!Ý2Õ°<´UË:y\x000cô°I4G;È\x0019*å\x000ciÁB9KÔL\x0017R®ââú9ÚAÍP©fXN½\x001cÑ3¯úàÙ&\x000eò	¡VÎ"´Q!!s1[Y¸­<;¯÷IÃ\x001dä\x000crFÓX\x001fè\x0015(V\x001fæd®{òx\x000f³Y­eÓ\x000e\x0011Ô¼
\x0004Çõæ º\x001däÌjå,£ÜóÓ\x0015zMj°Kwzö¸ë¯îs¸Y­åÓiÓUãÆ6åæ¨µ0HUJ\x0004
æ\x0014¢%û/ïÜáka\x0008«bÇ&\x0011tëXi½«\x0005ï\x000e
mì \x0011V{ä¡éÀ½îêR5ÂÈ\x0005<è\x001e×\x000e"a"a!ñ'ûÈe\x0014Å¸ýæ;È¸FX¥F@Y\x000büú@Æå0\x0017tn(Æ=&\x0016³FX¥FXçåV,SÑ\x0007»1ÉãA7xnP\x0008§T\x0008öFÏØÜ\x0017\x0012¤\x000ey¿X8;HSJ
¾-¸ä£\x0013n0rëÓzé\x001cî \x0011N)\x0011@-ö\x0018\x0017²\x001cy¬Ií\x000cqÐFsÃÇ)<6&\x001eÔLÏ\\x001eHgõØ¬{ÐÚ\x001dßw´FS\x00119\È\x0012ÜPÿUõZÑ9ÚAÑVÑ¨5\x0019+\x001aéoÝiÁJRÏGí´AÑöÔCå\x0008l\i\x000eiË9¢­Üõá¸s´ 9­ eKÞ¸¼tÊÌ6\x001b\èãÏA+wP4§U´Ë±X¶åoÅ¢\x001dõÞç\x0006EsJE+*A	CÕº ñB2l'àúüÉ)\?hWj\x001a]\x0019v\x000c4.oÅ:I;æÔ\x000fæVÂ\x001bò´q\x000b\x0013ãJCµ@1ï!¸Fx¥F¸`H#\x0016Ü¬I-0Øº\x001bÑs´Dx¥D \x0015å³Ó
AªËz\x0016Eî\x001c\x0000?ø\x0005¯ô\x000b\x0018Z\Nî¯\x001c£äWøä9£a\x0005í>£
;	t3uV[psl¡îA÷xa\x0008Æ2\x0018£ë\x0005\x0008¸VØúVË\x001a`½v|vX¹A¹r-¥¬°[\x0000ijj½úº\x0000\x0007\x001dzÂ\x0012¢\x000c\x0017,­\v\x000b|ñb 9a#ç|\x000ewØhA¹Ñ¬\x000fô¶à:)¶´>Çæt\x000fzèÃNÊV¢1ºS \@T¦¤`"9&\x001aÃNÊæ\x\x0001Læ\x0011¥¥iÈ\x00079Ý8ì´¨ÜiÎ/\x0019Õ¸4[¹
\ÝDXÏÖ£\x001d6ZTn4ø\x0005°A¦\x0014ÅÖ0)âAYmqØhQ¹Ñ\x001c=\x000b.\x0006NÓ-ÆþCi£TbÒ-é®kt×ù£¥Þ\x00015ÞÍ\mYjò@\x0015ìzBÿä\x001bû95d55½Àýtîä5X¢\x0007³¥;\x0019÷SØWKíH«­\x0001Zø{½\x001eÖ{wïNî»1[7¹n*æ7ïï?í¹àÓï¢L¥µ`¤&\x0005Ö¿¼»ùæùW'´=¡&4­Ï²é$§I4\x0002ð\x0000D×#ºiÄ¢]édDá#R$\x000eö\x0000Dß#úiÄ@ lÅ(·\x0010ä
¬Èïõ¡G\x000cóVL·¦&\x000b;z2eDóm¹¶\x0006.îC=bE$eâ\x0016%ìX\x001b£4b)«rõ ³\x001b1õi~CÇÛÄÛ¥Ä®B\x0015bÅë?tî\x0011ó´\x0015½î;%¤"ÖÌå$\x001fÚ¬7"ÝØeÖÿÙnBå^3Z'\x0014h1\x0002ûE+)H°ÑAl7#\x000c0mÇä\x0016ÞQy4ç Y±âz\x0008²pð0ï\x0018i"©li/OÉ[Ô\x0005ÓÖÁ}ciÏ\x0008ÞJ?\x001dçÃ­,F9>ÃF^ÉnÄÁ1Â¼gÌÇa\x00163b{â\x0004®×Áïf\x001cÜ\x000eLû\x001d:\x00109ÖÀ\x0000rS}Ê\x001a\x0000\ÏÞÍ8ø\x001dv<h¼$b\x0014^WC×ÓlÇâw®v<88\x001ev<\x0000K¹Tµ£3&½a\x001d¯WA\x001c\x001c\x000fN;\x001e$×üæþ°ãI\x0014_N-Wok\x001cãÚéÀ¼Y\x0002\x001eÉxEZë£öv#\x000e-NG¶\x0005RtÐæ$:èä\x000e×õëÝ\x0003Çi\x0007\x000en¹­°Ë\x001fN0\x00006g\x0007ïc\x001c\x001c8N;pä
3£ÜÕÚì]3âõûÆi÷
\x0004ÒIa8¡*·Àvcª×nÆ!°ÅéÈÖ\x0014°`Ûæìû`P¯Ï
Ø8(\x000cÎ+÷Í\{QbFh6¼Z^ìàºí¼ëöm^ó§²1ãÚwÞ
¾qpvÞ-\x0006+ÄÈÃµ-Ý³
ãõv\x001cw:ÔSÖ¢Ô
ÒgA¼^¥í°\x0016íôZÄ"{IÌ¸­¨mz}ºÕ^F7,G7½\x001c\x0012ö°1ò\x001b¡\x000c\x001b\x0017w3\x000eËÑM/G´BÅz\x0014\x000c28¦úÊ!f½eÇnÆñrgz9"d)\x000b.¼í['yS1éúãª\x001d1T÷#W3\x001e(5Tª³Ô!ÛnóÖ[Å~\x001eõÿ§îýí:nóÁW9/0§ºÑÿ+WGô1E\x0017E*¤èJæ&u,1234ébê¹Êíï\x0011r75WãçÐäI¦±\x0016Ð»q´Ö>»±,Ú)W$Ær¾ÕÀF\x0003\x001fâý\x0005¸±-ÀýîÍ~ýöêû×¿¼ùå_?üú·£û´\x0004ôª©\x0011'µ]îa_0â»'¾½}zõýí\x000fO~øýóëÜãý-¸±mÁÕa®	Ñªfq?	M´ÇLI[
!í¦ç
Ü®ÇíàÆ"ÆºÓ\x001b7CÑ!NÖ\x0013nö+W
Ü¡Ç\x001d\x000eávÆW/K<\x0000\x000co¤÷eÿ\x0015K;õ¸Ó\x0011Üa¨Yp\x0017ÃÏY±På#3\x001bï\x0014¸s;\x001fÁíÊu\qç\x0018Úl"M¢\x0014öÓ,\x0005ìÒÃ.Ìíi:(/
\x001eÔ'Whûw8S \x0019me\x0004<\x0014\x0002\x0003ï¼Ê\x0019 õ÷\x0015ð\x0004\x001c/ç\x0001\x0017aÐ\x001en"E¢±\x0018½-uÚS\x0005 å3\x000b\x0000\x0014¸E\x0018´â o~K\x000c
\x0019<søNûSÆ
Ü^àöGì*åkÂY£+¬
â4Á)»\x0002x\x0014Àã\x0011à1²ð	®L£©úæLb\x000f\x0014\x0008ëTo.èÉÞ¡\x0010ïÄ3\x000bÆawEÃxZ\x0003ª³7\x0014î\x000cÄâÍºÎ\x0005G+ÄSÞTà\x0016\x0010DB3%ãs*'VÖð\x0001ý®w\x0005p\x0011QàHDq¨¾âé[\x001aú
%X>ßû\x001b
Ü"¢À¡ËÛ\x0017ØX$Í+_èË~\x001b\x0005n\x0010ÂÐÅ&eP³@Î\x0008kÚMÀë¿fp\x0011	áH$âØà¹&ãFl©ñ1\x0018&f 2Y8ÊºÐº\x001b¬mêhõ
R6ûÝ»
à"#¹,¤ÌÀks·>²¾æ-Î
Üyà\x0008ó8oPÿd
á¼éý4#ZC¸\x0018Rà\x001ew{ F~§Ä©  \x0001À}ÞæÌ\x0002¸ \x001fw| ñT®MÇ\3|ÄÃ~\x0019J\x0001\Þê\x000fÍÜ\x001b%ICìc9
Ïûó6
Ü|Ü\x0011ò\x0001×ö\x0012\x001aS\x0008··¬7`ãþÔ¶\x0002¸\x0008âîP\x0010¯'Þìs¦`\x001b\x001d\x0001Ïû\x0003Ñ
à"¨¸CAÅ\x0018¾@@i½¾DGô3õæãEPñGM\x0017°dk;\x000bÎ<M) â\x0004\x0015dyêÄr®q&ÍþK¾\x0002¸È°ü\x000c\x000bÅ@hÛ#q*¦øèS\x000bã\x00133\x0015/2\x0015$SÁNlÄ\nodñà¹=/O
ãþ~!Üs!ü§OWß½ÿôöÍ»«_ÿ«Gw\x001fß¼»~<õSd\x0014 ß¬QÜ·Ëæþ+È««ï¿zúäÙÕÍÕ£O=\x001bzÜp\x0004·ÏÔO«Vù)\x0004\x0012àO\x0011ö×*p»\x001e·;»pÉ)ZÖ\x001dÜ\x001c|>ó ?Û÷¸ý\x0011{Sq6ó\x0002s\x000cæL³Ã8îÐã\x000eGìë,WsC\x0013z)\x000fûJ
Ø±\x001d;\x0016\x0012NÔrP/\Íûc
Ø©X»fáNw½ãSr2*)õ\x0018Í<%¹Ç\x001bwbP-\x001c\x0007¹bÙÞgF&Æqw
Â±k\x0010V\x0001Ïú>2ª®\x001a®ÍÒµ'°+ðm\x000fÅïhJFq[*¥DØâõ?0\x0011¸öH \º7-½®eîbÔ5\x0002éq\x001fÇ-\x0002=\x0012Q<X*ræ\x0003xôíê\»Ã8páöoz¼¯\x0011aúöYÿÅ¯°û3Æ\x0003¸-LPð\x0015étÀxýá]ýÿù¯ÿþöîÃÏïÞ¼þxÉõÁe\x001e\x001f\x0010x®\x001fbæ{;Ëõ?Ü¾xVÿâêÛ\x0017=¹}ù0x×w\x0007Á'Ë×dÀr-Ý}xú8å²¯Ñ¨\x0002ï{ðþ xßC°|ÿTåÏ\x000cËhÀ\x001e|8\x0006¾\x001eyîA3!sXãNâ²þþ{
|êÁ§àq|À[^oí|{MçFæ4às\x000f>\x001f<6XÔ_ïûØyÅ¢à@íV©³qð¥\x0007_\x000eZ>gZùË©\x0005ÔÇÂ7¢¸_\x001eÒ?e1\x0008¾Ëbtè¹ÎT\x0005õ¬Mè\x000255¦\x001cç:ì©b\x0001ow6r¶^àjX®.åí\x0019\x0019
x\x0011*íÁX	(\x0005H¦÷'Y*^­²;\x0002|<
>ÐÂwÜPd\x0019;ßJó¹	*
x\x0011mìÁp³<~®,eã\x0010Ïó)¥ýwg
z\x0010\x001e\x000bG=6\x0002Ïg\x0018ÏmûõG¦¯Ù¹«Þ8x\x001dLÍ ·õ\x000f\x0006EÉ\x001d\x0007ËFSgzú5èËÂAÅ§\x0017Ò½Ã\x0011uê³°ì±Éú©	\x0002\x0008.ëV¹³§jFcÿ\x0001¸­24õÔ\x001b!c±f	­½Y\x001cCËìkø¤ª©k-­\x0005¥>¦\x0006Íùñ^Øüñïê\x0007ò/¹ÎùoÉÔÚkßü·õBG79G.ÿr'ñß\x001d?\x0005ß\x00088YËÀñ§´dmª\x0013Ô\x0003twï\x0000\x001dû\x0001_ü\x0000¥û^\x000e{1DOS*\x0019µY½g
#\x0012g\x0016R(?Â/÷>Â/\x0007³Ä
w¨n\x001d0ýF*å\x000føÓ½\x001fpÐÁpúÚl4\x0011
w÷Lºm{Ó#õ\x000fþá4yüâýÏïîþýÓ%¯|Æ\x0019T\x0016]Ý6á]qU¸àÖúö×(ÿîöêÅóÇÏnþñÕ÷=
=TÐBõÐ òÆ(sBznrèr¤®Gê¾j£ú\x001eªÿ\x001az¤á«6jì¡Æ¯Ù¨©G¾j£æ\x001ejVA¶\x0017eÜI6òtGLûCPK\x000fµè F~\x0012Ç\x000b\x0001[5
Wû\x0003G v\x0005+ÿæk6«\¥#«/eWAVVÇV_Ê®®¬¯¾]\x0005_Y\x001da})»
Æ²JÊÊk	8ã6dÇ\x001alÜªQ¡Sv¹\x001cª`,«¤¬L\x0012]\x000bVJ\\x0005ÖsÃÎc\x0015eu¤\x0015
µæ\\x0012ßÔ¬ç£x^¾âr¬´¬µR¤M\x0019·¸³$drÜe\x0014÷õ6°
Ö²:Ú
6·gÔ\x0006%}1\x001fù\x0008X7Å³@°\x0016èX«Bu49\x0013/!±'ø".øU°\x0016(YË´ÊqØj±bÍl×ób^cW,\x001dkÕã\x001aC;®5æøÕ*Æ³\x0002nc\x0015¬\x0005:ÖªgÃ@J¼ÄÐúÀa\x0000Sù\x0019X\x0005kµ¾]\x0005kµB&]Îê[Ýz»Uº\x001c« -ÐÑÖ²« -PÒV^GÖrÆÖêÌf%&\x0008å¬*ÔåP\x0005kµ*Tª#æ\x0008¼ÁÒzÏ\x000bùÌÆ\x0008VÁZ f-(
+µ±#B»:ÁZNÍZ2nA2+w¬å³rc\x0015¬åt¬\x0015Z[w®EË\x000f¬÷|\÷¥Y 
Òr:ÒB¨·\x0004h*½Þ³ÌFÚß±9UV\x0006¤®I©'ûE¢yÅêrÓLs\\x0005i9\x001diaÀD°õ¤ªgñq-Î -§$­/dWAZNGZ±Ðd.§y½zå;ÁÔ!¬´´¾]\x0005\x00138uÙ-QÈòé«\x0018Ü´\x0014Ò¾üË\x0008T/Àë \x0019îr_öÆ³D¤k¯½s®Û^W¯¬d¥\x0013Áz\x0012µ!5ÒÊS®Z^>f(C¼lª*ü\x0008]\x0000'\x0003éÌ´Æ\x0008V\x0011\x0005¼2
DjÍ\\x0006\x001d\x001cEÐòÁxVQðr¬"\x001fôÊÚ{¤\x001eØÅ³\s­\x000céë\x001aÀ\x001ak\x0005eAûËØ5\x0008×
J×úÌXk\x0000¸7]Yc@
Ø7ÿñúÝúÊýø×¿½ûõo\x001fîÞ"ôÇw*¾»R,¿Ó/¢r+pÃÝf¨E¿\x0019\x0014nþxûl}ì~|û¬þÑSü\x0019o^ÕÿûÃ?\x0002ú\x001f\x00013~\x0004]È±ù5V ¬#ý´=qè'¸þ'¸\x0019?!áíl%\x0005nÆîâóJ¾~ï?ü#|ý¯DäË0\x0007bê?Á\x001aµq{\x001bö¡\x001f\x0011ú\x001f\x0011fü¶ÜMÛ¾fíö\x0006C?"ö?"Îù\x0011x«;þ\x0011Ý:Àf	øÐHýH3~Dn±É9jã5\x0017ËY³½BùÐoÈýoÈ3~§Ðäs\x0013Æ0mßÕRý\x001bJÿ\x001bÊß`]u\x0006ÇÍhÖ°:¶Ùs;ò#ºAT¿pÌp	ÞUöÌÁ)´\x0015@ÛR\x001f~`:{êê·°¸v'
8ûDb®³ÛÓÀ~à:{ìV,¥Q"ï®³`Úzí%È~ ;;í|¢\x000eAo\x000b«JÛ&\x0007·»L\x000fý\x0006Áuv\x0012ÙÑ°\x0001ÎõÓ|É¼£Íì(­\x001eú\x0015ìì\x000c¶k\x001b¥fâ×ë[ì\x0015x¯þ+\x0004ÛÙ\x0019tW±&¨\x000b©­ò¼\x0016Ê¸íwC¿BðAxõ[\x0014ríÌylý\x0011ü)vÞq\x000eý\x0008Axv\x0006ã\x0001·_\x0017ç\x0012EXËgçS\x0005\x0008Â\x0019Xé<årú\x00144V_?Åö³ê¡_!¯v3\x0008¯b¥E.·aoËj:Ùíºå¡_!¸\x0002fpE«hVß6<{\o¦¼\x001b
¶ëY~`\x000bÁ\x0016Ùø¢Æ»(dMA¹ÑÙ¿B°\x0005Ì`\x000b\HC~,\x000byµª}å¼Ïp¢\x0004[À\x000c¶(Ü\\x0000o\x0016´úÇ\x0000O¹ÄÏ\x0010£\x0004[À\x000c¶çLqI;3wL	¢ Ýä_áD¤u3"mò-Ò"]PUµÞ²/¶\x0005\x000eý
Q	tÇKÞ¢\x0016"+SdNhÁr+V½üM÷n'øÂMà\x000b\x000bM\x001cÄù¦
ÜSX¿Å¶ìÐ¡_!«\x0013nH¶¦±<Ãælón\x0000þ\x0016v[ÎùÐ¯\x0010¬çf°\x001eN~hÅ)\x0019\x0004S\x001a_L¿"9Azn\x0002éáòÈÊ\x001b7\x0000x²¢ùW$'HÏM ='äÜPx+.R:\x001f¨0ô =7ôp
(¹-;0ÁyÖâØÑ=ô+\x0004é¹	¤gÁ5·°­L\x000e>6ý¢í	áC¿BÜÜ;\x0012(\x001a¬y9¯otÜ\x000cÓ|Îó¹ý\x0004æ®ÄÌY­\x0012\x0005÷pìI\\x001fú\x0015¹ý\x000cææÕ\x0016¸Ý=\x000fÓÎ¾ÔC¿@°¶ÁÚ®\_ûHkE 6iw¿-èuè7\x0008Îö38»º5-G¯\x0016ZU\x000eóïx^>áMàl\x001bygÔ²ÃÖLâS\x000bÉÖÌO¼àl?³QxÜ:xÞq\x0000m\x000fßÞMxèG\x0008Êö3(\x001b\x001b_hái+= f°<B_æÿ
AÙ~\x0006e;Cê¼Å:w\x001d)eõéa>ÙyAÙ~\x0006e×SÄ¦²áé\x001fÈmÑTÿ\x0016é\x0005eû\x0019z|;s³\x0007ð¨¾==\x001f\x000f²Ã\x000cÊnCc\x0005+9tÙÂWÒÎã¡_!(;Ì ìØVåâ\x00131_ã\x0003e·çµ\x000fý
AÛa\x0006mGh¯· ÔJ\x0006%7¥­í¶§C¿B\x0010wAÜ<áIö©þ¦x3?ý\x0008¸Ã\x000câÆGmR\±­æ\x000c'Q	¶/\x001fú\x0015²ùf\x0006s6³T 2]8ß¦ýü\x0016¢ ¨;Ì n\x001cc£Æp,|\x0002Qàí~ó; î0¸Á\x001aÊ+¨Éº9´áÜù¾-;Ì îÚ84Nðzöm`!¥m¹úC¿B\x0010w@Ü(ùJÝÐõ®M\x001b¤\âL0ù
8Q\x0010w@Ü`O®í#OK \x0004?«ëåé"
â\x0013\x001bN4\x001eQâ(ËiUêüO!x;Nàm°¤Mº\x000c-0ËG7¿70
Ò\x0013H»þ\x000f\x0002sv'LÃ\x0010æ§(H;N m¬Åd?¿³OÔ£Å=¿s%
Ò\x0013HÛù@}¿9\x0006n¦Ëô+Ügè6²ev\x0002iã3j¢eð«Âür¢\x0002Ë&Í~ ¼8ðP\x0006R½\x001e\x0011W\x0004Ã\x0013¿>Ï£O+Ò\x0004®p¦~\x0000Z\x0014ï\x000c/\x000fñ­öáãöÊ¡_!Âl\x0010f]M¡xÝ½i/ª¾ð\x001b½÷Û\x0011~QiBÂf´DÎ\x001d¹o6\x0004>P.ÌO>p4Á-p¹\x0015)¹aß,ÀFÏúù`ÝtºÈÂ-ò\x0004·ð.âlÑò+ª[JB\x000cÍÚù¾íl¯nJ½\x0006ø''^r¸4¡xÚßDnd\x000eóû\x0004S8i.ç*üÃþ\x001e\x0006´Z)Rý2Â×²®ùßucpTî3¤µ\x0016î,\x000b3NÖ2çZhÇYsMûhKú\x000cáIÄrÃ»ã	I½`\x0018ºkTÇ¤ÄlÊÄü¸\x000b÷<\x0004{¯·mL	£B\x0004¬ªn@Êü\x0011Ãú=~¹÷=ûH®¬\x0018¹¢^XYmþ¹2á¾IÁ7ò{\x000f3özÓ,mdúo©ëîÞá:î#¸ßÄ¬WÙX2kGùÂ»ÃüÎ:¥ëO÷\x000e×q/Ä¯Ç9ûÈ\x001d_¸$ý³xÉ÷~È\x0013®Q¾7\x0000p°\x000fÜô\x0015üü[ý!?Ýû!?Mø"ü\x0012SYö[¯_uä\x0003Ìì°u÷ç»Ý2ßýýÛ»\x001faô·ÿó_ÿ}ûóÛ7\x001f/qï\x0014\x0003iþÔØ
ôF\x00065BÑ¬OÛúDß?½y´\x000c¤?½º}üôÉË\x000b\x0000C\x000f\x0018Ô=oÞ(©\x0004üË\x0005°£ö4Ìv7ÉN\x0001ØõÞÂm[ýOÑ\x0008ZØ±óæ\x0005U\x0001Ø÷ý\x0011\x000b¯\x001a¥Þ¢IÊ\x001a°¿-\x001c7\x0014C\x000f8\x001c±0-ñÉ!P#/Z(Êçm÷S\x0000=à¨·°ãæÄÊ¤f
°\x0011`¿Ýb©\x0000zÀéýÚkky¢Z\x0016lg_¶\x001a\x0014s\x000f8\x001f±0$d0§(\x0011\x0018ð¶\x000c¯\x0002oéñ\x0016½
uµÕKÕ5y\x001c\x0013!w35\x0019Û
K»uXZkßÂÃÅ\x0019\x00125%T\x001at|\x0011û\x001cÄ6ì\x0001Þ\x0008Ì\x001bÙeÚ\O\x0004wû×\c3U \x0016aØ\x001eÃ©E`¯Éç¼iQÍnp\x0014ET³\x0007ÂZ>\x0001Î-¬ag\x0007!N³\x0010(a\x000f	 \x0011Ô\x0011.pìw~³&£\x0008\x0013²6¶dlø\x0007JØØØDg¹\x001ek
n£ÅÆ¸æ`t×\x0017G«r´zP®±ÎPã\x0019x··\x0008«0ÿõ\x001eæ¿ª1\x001b¤ºûyí<\x001f>\x001eÖÝßêãLÌ¼úáÃE[\x001cJ¸³¢N6Ü¾`Z^\x000cn{\x0005&}yõÃó\x000bÜý­>Îôiü\x0000ÔRxP7xÏãë¦éæÀó0T×Cu:«:®~D\x0017ùíØ8\x0012\x0018Ìõ
{6ñ¹\x0018ªï¡z\x0005ToLÛû\x001bBâ~\x0003©«+Ý\x001eÊ\x001b\x001az¨AgU.\x0018\x001cËpáµbEZ¶Û;Æ\x001eiÔ\x00195òÔi(ßHMa)\x0018Øy\x001bz¨é¨Që©\x0005¸wTÙn\x001d{¨YëUa}
`¸^b¨<áTìb¤¥GZ´F¥Mà1ù\x000e)*w>1¿\x0014i·ÕÇ\x0019\x000f\x001cUhÊh\x0013J¤¯J\x0014,
\x0002q»g{\x0018«ä*%Y\x0001'ã1Y\x0014È^ÍÊ×3g§\x001c\x0000+\x0008À*\x0019\x00008\x0002ÔënÓå:íîëa¨\x0000¬\x0001 É\x0015àaµ¼|:ÎªUãÙ:ÈÅXE°²ÊheiIJI86ëe\x0008pa{\x0018ª\x0008VV\x0013­¼q¾ÔvÒ[\x0017YÓ# ÂUÆ+oýY\x0001®â	k<_¨¹\x0014+\x0005ºåÚ¤LÌ-·².5Ç\x0005W WõöBõ¯z\x0001çáO\x0003@ÉµKÛ\x001b\x0007±ÊäZ]/¢%LY94µ±DS/õ\x0013\x0005@\x0004WÐ\x0005WÏ«S÷ÜÓX!\x0002;ËS¡à
ºà\x0000éÝ\x0001%3#«\x000bñ\x0011ðsR\x0001\x0010é5èòkçø²]o«Ôj\x0002¥$æ¬¼Ý\x00137U$Ø Ë°=÷z/DàÖ¸e»noË\x001aÆ*H\x000bt¤sdWÜGZ©ÀúÁ¨9\x0005«`-Ð±VäÁj×Ó2LccaçD,AZ #­\x001a±ø\x0008ÔÕJ\x0017ô ]¯ØÛê\x001f£X -§!­/uuq\x0008\x0008ÀóÃcb\x0012´\x001c+n72WÄVó¥*Ô×6\x0007\x0010ÛØjX(\x001fK\x0016öÛ®½&y¹ß vJÈ®\x0014`\x0006Ãf8Ê·\x0012¿Ü¸X!6ñþkní÷wïß]UÐo>¾ùp}kÎÊWDSq³VPÓ°Ø\x0011e#éùï?»ª¸¼|òâa¼Ðã\x00055ÞÒf©}àK\x0002Ä6úê·5l5]\x000fØi\x0001¥í¥ï«F26°mû\x0014K<'î?\x0004Ø÷½\x0016°
×Ô§-;\x001c\x0000/¯åì.è!¼¡Ç\x001bxMñ¨*ÍC¼ü­¤6ôyv7Í\x0010àØ\x0003ê\x0013Qx\x001flZ\x0006\x0015V\x00036TxvÁæ\x0010ÞÜãÍ\x0007N°=-°õ|\x0019ï¶\x0006néá\x0016õù¶\x0010²"\x0007²/\x0017½RpÛ\x001d\x0005àîé<B¿y{ÔÀ¡­_÷mê¦¦m;ì4À3Ô¤a=o_ÆË\x0004õ\x0016³ÏÛSÖ\x001a¼3¬4_[)rA¡\x0001\x000eÁ\x0006X`«ÁÆµñi\x001cd'Ù8ØõÓ"\x0015\x0011ÍêCÃ\x0019ïu&4ð:n°-¦¹yEL³ê V\x000f\x00025FlÇ&!\x0010Ï²
Vf%> ¢\x0004è£D\x001bß)¸\x0017"ß\x00120ÍÆ l\x000cj\x001bcÂN=°Á^\x0017b\x000eGÍ\x001f5PLK}°±SÛ¸\x001e^jÒ\x000fv\x0011]^mÌÚOp~sØE­±÷\x001eÍk&ß"ÛÇ«\x0017ï?ý\ÿ×\x001fß_vABµÕLo¼)·QfÞ×\x0001¶U
WÈ/¯^<õ¸þ¯?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Úb4vÀè?=0ú¼O\x000fîë'\x0002&>þßßanr:\x000cá×Ë«Û«ëÏ÷U\x0016­\x0011ù,Â@O]d"f\x0001C'¥òMÚG'§\x0017GÇ¿ÍÇb ú\x001fáîë_Î¤\x0015)ø_¯>]"¢\x0017¯NvøÝl~ýnÁ´ÑZåÅ tÀ¬*õLznË\x0006è^}8?~\x0001ý#\x001cü¯G/\x000f\x0013ÖûÛ/_\x001en.ùÿ_ °t­T&7CMT\x0011u\x00153U®-\x0007*ÔºÞ
DøU3Ï9ÑA\x0019!À«TVñ\YtïA\x0005
¾t+9¡+QAO$ET¹Ä=Q9l|º\x0007U\x0010ÉN\x0011TÖÒVT\x0006²õ\¦ò¨\x0002Ê3ï\x0003\x000ceøÕ6U.\x0017_\x0003T\x0000Ñ,r¹GbèËNÅ8´Í\x0015))$,­ò\IÆÊÃ\x001eX\x0010DÀ¡
ËåT£«Ö3±¥1Ër\x000f,HeÅ¡
+>S*ªgt^Q¿\x0004ó\x0013öóªùhð"`\x0002Ëç{Â"y\x0004À²û\x001d
\x0012TÈphÂr:§*\x0006e\x0005ö­@¬ 5aYl)¸\x0007\x0016Ä\x0004ph-\x000f®_ÄêY>\x001b ©âTàDÆ¡*B?
¤R\x0012J®2¦K'8¿ßé\x0000½Â«æõ.@Aß0\x0004\x0008 ´\x0015ßoÅ;¸µphÁ\x0012\x0010øÏß0\x0004TÐ\x0003,¡²moå¿×
-EÀ£´\x0011K,(&¿¦·EÚ\x0001×s2KçXøÈfëÓÍw÷\x0007>!ÅHu÷áùâzñsñþÙÖéî\x001d.O\x0017lÊ§KEOk²7qÏç\x001fÌv¥[Bf²`y3j}\x0006nÁ\x0004¦ö\x00063Éx0¢\x001d:\x001a'°,è§L²a#åØµXM\x0006Øð«L\x000b\x0012Ã\x00012ìsÇªt	yaÆNûj20Ú¼j'\x00139{/¥3ï!ª·I§}pû~Mèèû\x001cÆÏ©%[9*­3²éÓ?o\x0008M«1;µ\x0016
þ]ÏqhDKßSçÛ[YÌ\x00074\x0019ØXuÊ\x001dfÕhÐ=\x00106´tAJ\x001a¢A·¼=%éUØd\x000cé}7\x0001Z84¢ÁÒ§\x000f*³o'	~wØ¬%¼\x0017YL\x0015F²@^§ ¤tlçËbç[!Ç,×Z4
«L·/5	¥úù6m\x001fAÕ-	Íë±Q5\x001aX\x0018ºgfT¢©¥Ð úÜ\x0010\x001a·6«>í\x0006\x001b@·ï\x0002\x0001yûy©IÐý\x000edlH5H\x0001Þ\x0013
ªqqhD\x0003±üJF\x000fv\x0015¡)³ï±fCú7àÐ,CIÖ¿1Ò\x0003Î%ãÐôþg3\x001bF4íR\x0019ÍY:q]\x0010ÖZZ#û®5\x0007Fk¶Ô4´ôp4kÐ5Àg4ièJmÏ+TJè\x0003Ç66ÈBá³8\x0003ê\x0015À\x0016\x001e}ÑôPßÍÀrÍc\x001bT6\x000bá&¶´]#\x001e\x001f6­6ò)ÈóÞÍ#[³Y\x0004Y7/ÈÃb!GØ\ÜóÔØå"Ml*¦×\x0013fP'6«Ég\x001d[lé-ºï´a£<6¢¥³gMkÓn7eÖö4s¥<Ü<6¢©¬\x0005G\x001b?ó¬õüJ?ßóBHÿ+5¼ÖMë&U FÅÖG\x000c %\x000clJ:b\x0003¥ilw·FÜÜÀë\x0000&>®D\x001f@/cñérëEÌØ\x0017\x0018vJÙ(J,eÖ®wR}\x0000¹ùËÃ]Lé_^,0ÔCY\x000eÿ|{Jh2hÐç\x0012\x0014uòµ\x001a$Û÷
\x0002}×P½fÒÅô2@&-\x0004YrÍ\x001d[ÅôýÏ?¿ý%º\x001enaÖÁb¹,½¿GÑÖé8_Æfz¦Ò¥
ðúlÝ\x0002­ùÙYn\x0002¾\x000b\x0011"óZMC42÷Q\x0007Ä\x0008"^(bîi	Á=
b:\x0016á×\x0014D¨½ãYTÙLÿ`È}^\x0001qxzLC´iÝY1
Qa8 :!²ç6ý$éµï,ÞüõçÕ\x001c\x0007CN÷Ôc\x000e\x0016×w¤\x001f³åÉ\x000c¥ªÙk¤Ò;&["^ÙÀ¯ygÜÆMñß Ì.:5Óe©Nt(?¹¬¢³Îykö§³ÌN¡3;\x000eN\x001aÃO\x0006¥-Ï]\x0018Zq\x0013è4TáÐ'ÒîÈ.Temd\x0017jt,\x0010§ãùÛåuüccüîåâÝòjÓÙAx\x000cmL®.\x0010»óÖÑ®Ð6½h^Î_\x001dºw\x000bek{\x0001\x001a°\x00085[*(ZÐ\x0005QÀÜ¸=R	\x0016!&C\x000bXº\x000e<E :rÙ\\x000b`Ó\x0019\x0012ÆL:,©4Ët+\x00174wÇ
jB²K²i\x0019&_øpÛ\x000bÌå8^3\x0018øÀó\x0012\x000b\x0016eîÌQ0ÖF?\x001aN¯$K/Dc\x000b\x0013Ðò\x0001÷e2&uö·E£)òé´p{NYT\x0000c\x001b\x000bù`\x0015¸\x0004}\x0006YµÓÂÓpìP\x0007¦\x00048\x0018òØ\x0004&§\x0018U:ùÃ3<-¢#Õ.H?\x001c\x0005ÕÉÇ&0%\x000ceG¤)ÓààE2\x0013`Êöû
ÃÍyl\x0002\
\x000b¨ÏÑhÇ\x0018ÈöuéØ\x001e{Vyt{×ú-¡Q4j>%\x00082	%¹Ò/\x001derÔqZM\x0016,¶j­Ïd\x0010}ÌdéLTL¦ö\ÿ\x001eÜyl#\x0003	Â|Ê:\x0013²K\x0006^\x000bçLú\x0016jÉà\x0011ÇÆ9ópI" \x0005dZ\x0010£áÐJ2L0Êcó×¤<\x001d©p|ä¯É¯0ê\x0004¯\x0005Ã­\x0019·&4®1dbüÎ`r9ìIÛ\x000e¦\x0010¬ygQ¹ ?!¿÷¤Ñ<cYç²\x001dLèO·W`]pr\x001cVø7ûÛë«í/y\x0010·ÌF²Z#ùý@JÃWÔê)ÿf~r~zq|4ö/x¸"phÆó:\x000b¤8UHÿGV£ðã.Z<©Ñ1c#K\x000fXòÒkÉVZÚYúÏ¨ßÏEL\x0010\x0013ø4äÎêÌgPã\x0004ø£g	q\x0018{©ç»ÿòãúý\x0007Ì^H;Õ¬j©_¤\x0007üÏ­\x0001cÔ3-é\x0001EZÚ\x0005²¼üð\x0008ÉÅÁ/Ò«ýï;q\x001cdë´ágD^\x0000\x0014AN^!áõÔ\x0003;\x0016\x001ceËìð,';\x001a¶¯ÓFpûàE\x0017}ãìp¢jô%ë+)\x0006×Àð&jàQðÄÅ¡i~èù­¥a?mº,{\x0007ÖÌ\x0006 
¥\x000884\x0000¹¬ö
®\x001eM\x0019ÉÔñìéÑÃ\x0007Q\x0013\x0005¦	J«æG\x0008H)A\x001e_R\\Ü\x0007:,jÙ´ ÓÓBå\x001b\x001fþiùp.#Ø\x0013{Ð7\x0017zdóQs\x001f¬àLT·\x001e}h\x0001\x0002%+\x001cê x*L\x000fµ"PB§\x0019Úc9x­âP
\x0004Ò5\x000bí©óèMÉ+\x0013\x0013>ÙrñçOû	=ª`Eum¨³Û\x000fX0·%kKZÐ"D¢Ü;\x0004³¶\x0014A^®-i6¡ÎN9üLp
V¦¥ê`,»Pµ\x0016|\x000cÅÑi\x001dS¹Ç\x001aÒNã²\x0010ÅY\x0003^»ÄØ»¹É@µN\x001b
Ï(\x0015PjÊÔF)>¬×.×6¢57i\x0005Uð Ê\x0007$Mçt\x0014çG\x001dku@1mµ(ÚÒã\x0013IAT#W]ðBr£®Ñ*"	ß\x001c\x0016$\x0017s³ù|§qº¾æÏ6~RÇ\x0004,U#SÐ® \x0014,#Év£³r¯S@Â=C\x0013çìså\x0003W\x0017\x0019É;.÷ÒÎ®ïç8´0¥{\x00168¤kj²Hä¯§Ö\x000cì6(ðqáÐ\x0000e@OVÅ\x0004\x00002Ål\x001b÷ÖA¡×Ø·í<_\x0008®º@¶¿aÛßI³×!.a¢qhÖ¹\rh¬çRj¿5\x0015ÑÝ8SPñAkJ\x0017\x0003¬ÜbÇÖ«U2y`òmL\x0010#¡%¥\x0015G»ÒCR2\x001f«©\x0002Íýç84AÙòõÒól\x0015S
°lî°\x0007\x0014¼dÛÑi,GË\x0015F4Ù¼ÓCãh]_\x001d\x0013·ú1®
&¨Y0\x0006TòmL¤Ø[2ôö»¡;æs\x001cZ  É $(päü:°~´r¡

\x000f9-Ûî\x0018½¦ì^\x0019 Ñ x¦@m\x001f(8ÊuëynðiéRÞ@QEþ|Tßl\x001a»×çÛo\w"ÐLoÎÒÀf1£¹ÆULÐà÷9\x000e\x0013\x0019òàÎÌóD\x000bÊ¨ÑPV\x0015ÓÄÊÆ­\x0017mî$\x0014dÔX\x000bÊRÜCkÌØ\x0007*\x0000TÕb<	\x0019&(©Ø¼³
éÁµÏ!%¡oÝó<6PÙt äã\Â)¥ór\Ó®\x001f
\x0011m£2Ê>,?bIÃ\x0008éÊ¹\x0000~»¼ÙâeÎ
\x0007ßÎ\x0007gàôd¯\x000f\x0014{uÓO~;<\x0019Ë=)LÚaZQ#S°óÂÁXÀLÏ;ò©\x0010oV,(/Å¡	Ë+ºú\x0012\x0016ÏV\x0010:8Æ\x001aI ¬¤2X¼gD\x001bU\x0014j÷$F×	
îD^ÆûaA²\x0003\x000eMXpBåÕ\x000e\x000f\x001c\x000eÂ3\x001d\x0016×QÝýþ~ù\x0015ûQA).ü*9W³\x0017ËÅÏ\x001d	WRk
J\x0005_3_5RR0T¥;yóÊJðÅÙüï£ÙV\x000b\x001a»=Ç¡	L»w%°³jÔ5É¡¯¾\x0019¬¼jÚÀÒwÌÕ´\x0008F	*7G®Íß±kUÞÕÄÎSJÑðÞbÝ\x0012NgN`zÏ/i!ÊC\x0013\x0018\x001cóùÉ,%ô\x00042tÌk1'Æh%Øß­û´ì*ª\x001cßÞ_ÝÝ]~¹¼¹\x001d,o¯~\x0010âv@§\\x000e"ëtÑyáAgÊ¶åðp=>=?zóæðÕáÉùìàìôè\x0011ênPô©ËÉ éõJõåJ°¢#eq\x0000\x001dfÔM\x0007åüÒ ÚA4\x000bIÓZ¤r¾´{T\x000fËÓIÙ;õÛ\x0007ª\x001cJ;ÎA
bþø?>`
  
  
  
  
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
  
  
  * Evidence: `<?=íÚÏSÆv7\x001c¥L&½ká?Ö£EYRÓM'r:nÄ¦\x001e\ÍæZCàÆ£Å.Z\x001c\x000668÷ÛÖì ÀFý¼j­óÑdJÎvbt­\x000cÛ8Qó\x001bPòXÈÈU'¡õÂO@]49\x0002Í£\x00036'$\x0017{Rß\x0015ÿ*\x0013ã$0g©4ÁÐ/¥5'Ø\x0012ìnøÙz¨JfH\x0010çæ5+výÀND©z%²ú¶¯¶{}w\x00018ÔÞvXý2_~¹|{½ø\x0005\x000b]ô>igpé¢ð9HëµÃz\x0017£\x0008/i@ïñï{/\x000eæ¿ì\x001eàÄ9¶¶[,__|ê¾È\x001d\´RÃàs\x0002pb°2umôZ¥@íG#¸ýÅÖ2È4\x0000<1ÀIÙ\x0000\x0011$C¨|½\x001eB¬WNÚ\x001cØP#5Õ¨Ù\x000fx¿4­\x0005XÇ"sXÐåi;â8«¥ÿqßNbd
nqýö>g§÷ ¨\x001aêÂý\x0013ó×\x0010Eå%qprU\x000b¦hoûó\x0017g½Ó ;HÕX\x0004¦WJèLHl	oR{õDÕ¢}Hk\x000fLr\x001c«yÈ»É6É¦·\x0002Ó¹\x0011GË\x001c\x001dCu_õ8QÑ!\x0006\x0004ý)\x00135ñØ¹Ì£y(å®ÇäÓ\x0006\x001e\x0014¿xP¸%\x001e¿[m\x0017
Uªç'\x001dö\x0006y@ðæ¬Pà±L:úd\x00138bÃò\x000b\x0004¶1\x0018hÃÈ
k§\x0002q^=\x000e)C$­PÈöÇ²B~«\x0015âÔ±z Ð^u¤#-X.\x0007\x0005\x000f7\x001dé\x000b4,ÐÝÖq¹UêP\x0010h²ÖÈ²\Âo¼õÃLè\x000eRã\x000eI) yß(é=-\x0013oÙxÑ*Òô¥Q²Zç¾`\x0014¨¯×Ñ0\x0012)Ó0oØ<Ýú	]ÿ£\x0017Iòánãá®@¢>\x0015ã.\¤ó©ÊÌÄO¤9\x001bÓ¸ry\x0004\x0013zºUJØÒÃ$&ßH%kâLT\x001c9f\ÃãÞ\ä\x0000?mÒ-÷.àk2I\x0005,KLØ\x000b.ëÎpÿø<ÍÏÉ0\x0013J©g\x0012Î§hhbrØ\x000c=ífy)ÚR8ñ\x0011L\x0004NÐ9»ÏcÝç3®¶]'\x001aG2B¹õ\x000e\x0003bÌ\x0014ÈîAÇ\x000c1É­Ïxjæ\x0016Ú^ÓºcNBÓÈÜW.\x001dó²}ßß·\x0005±àu\x0019\x0005\x0002\j:U!{\x0001+ÀY",·åûÒjï0\x0002Kä&p(<½BÂt°\x0002+\x0011ì¤'FÝ¾¿wßZ\x001ax3á\x0008\x000cîË««Åí\x0006S\x0012ìGì&0þÝ\x0013ç\x0013Æé¡Ù*\x0008±½Í£ùÉéîÞþþ¼Ïã­^½wîÃýû9÷r±¼ûÞÏb°¾Õ¦\x0015Bµ%\x001bL
\x0002kU.ÿ óãÓ®×áZ\x001fÎFÛÀ5~-ßy	vlêJ%¶ú_6AÑ_ÎæÙÐCN?UÉ¹ÿ¾®µ5¾ótÕ}6÷½\x0018ú,¶ÀÉ+éö©Û£Ë^Ñ]G¹¨ú2Wù\x000cþ5ßN¬9´ÉiötÚe)\x001f~zøq×À×±Ñ\x000cÙ0.
¤ªÜ8ôÇ1E\x0018ÿ\x000c}Ü\x0014TÆ[/_ú8¬~úGïõ£\x0013Á\x000f¯{ÀtúümíQ×9!0Úu¼#µ2ÉAµ
|\x001dL ÔV\x0004\x000f\x001cÈdA7ÖÝ\x001a©Mõ÷Ï/oÕýä3[Nnî/_¿Ûd\x0004¥!l(ä´]Ïyx\x001cè¡²!´?rx¶÷´¯[uûûxIðÏð÷M\x000e\x000cß++ðû^Ò÷­ã¿ß..\x0019$p1· \x0001®\x0000Y¬@\x0013{\x0008°>£«»\x0000x\x0000`	\x0016Uk ²÷I¡gÃò\x001a\x0010UVO[WÐ*üQ\x0001$NP½Á\x0008Íë U=ÕñY¬sW\x001eßÜ\x0003ÈÍ}?
¾9Æ¤\x001b¡%uÚóF¢,IWÂQ\|U\x001f8><Û\x0001¨Ã³õò¸Å´â¯¬a2m)
yÊõ\x0006Kai­>× U¬Ô×²ÊëT§T*ä²PX)ex¥¢°[c­x/«°üüjâòP/ìZ-s\x0014\x00155±\x001aE\x0015Q¾%,8ìÙ\x001cÆÂ]Ò)¼ì\x0006¦a­¸Vk°Ð©©ÉâÇ`Ý;A)µÖ~\x0019\x0005E=®F@\x0019ÊW\x0012\x0015nf^+E\x0016±+:°TC7pÅå[³NÑ³S<)J.¯-HqûÝÃ¹#\x0017J¤ÆW*ºh°Q\x0000aµfú\x0018ª\x0007îèÊC\x0015y±ØÝjÒ\x0008LZ-·6P½\x000f\Ò5k¥\x001c\x0011Å\\x0004D\x001ccZozÖ\x0013q1÷erÅºÑf_\x0003\x0014ÖåH\x0003b}\x0008jÕQ^\x0005åR+1\x0012\x0014Î`dñ¹ÝóÆ\x0003\x0014\x0008ÚFÒ\x0013á¥ñ\x0014\x0002225âH/MX\x001f\x0002ªâñ¸ã.+§<<5\x0002 \\x0011SÛ?~\x001aýn{3ªnf9.¢³®]õbõ}sæÞ%\x0003;ôvû­71\Ö\x0011°h4\x0017­ò\x001cÜ\x0014\x001dÁÙô\x0008«PØË½\x0016Â§lGäPTß\x001cìåÑ¢»]£8PuÒ\x001cí\L\x0008zBË¡È¡æ\x0001âGJ\x000cÃ\x000e^LöÍu¿ÈA
°\x001c"LæÔ\x000fzÇõpÀ\x001dÒÄahì\x000c¦ FG\x001cª\x001b\x001fÅ\x0001\x0007K»J\x000e\x0019ðMçcj³\x001d&ÙÑ´Ý1\x0005a§}\x001dÅ¨\x0004\x001d\x000f+9¸ÞrZ0ýn¡c%èqL\x0018"rDY*\x001fùN?\x001e\x0018C4¢\x0003dè\x0013
l\x0007A~Gf\x001dg\x000c×uÍÂ Èu\x0018cµÑEvSHÍÖZ3\x0019&4UahWd	O²û\\x00042·àpØ8\x0019\x0003Í¬JÙñw®\x0006nS):,¦ëÒ5Å\x0003b\x0005º,HÑ\x00103µ\x00034p©\x0000ã#êT_å\x0006\x0016\x001cZ¹3ß"a¨\`\x000cá"Ë/%&ËQÌö1¡v94©´i9t¤åpÃOß\x00168Ý¦ZåéxF½â÷MjãøNîmrîÕ\x000b0M\x001c!-Mæà
åüä;n\x000c[+H±lRÌbÿ»Êï½,IQ\x0006ÛjIYídØã»Â\x0002=ªÉïÊúµ}Ë\x0011Òà=Ê¸3´-J7Z©Ê\x0011àhêãt
Ö\x0006YýQ®¬¼\x001eØ]*T¿³HG%ü\x000cÛBkoQÅX 4\x0011©\x000cÇ^Ç*W×úû·7ëü//¯ßÞ_lH1PÒ*æb\x000c$Ù\x0015N£H,X ·ÖÎ|¹wðâl·/®áYq\x0019Vð8lÄxB S\x001c¤:¹¢qa+\x0015oá0H÷\x0006xÐ±KI\x0005`5ÐËg¬Ú
gÅSXsya»$¹yçì0Ø.¹Öø®åYñ\x0011Vl\x0017ö¬K8^ç\x000eº¸[N\x0012ÝfuJÿÈ\x00118qÐÏD¥¬"ü«J\x001eôá¹Q<ëìL>=X;N@XóM§gmî\x0007ó\x000cßwlåF^08\x0013\x0012¼ÙÓ\x000c[¦ù\x0004°Öy:	þûnÜ©\x0006õÒÐ©ö6Oê\x0004&£xß¬ßvàT»q'[åa9ÈdMnÝL|²µßrxrí\x0018$.AÉ²ZÓÖµdõÚ(Á\x0010ÓÍÏòæÃºxæ\x00155ÞÞåÒ¥\x001e(t-g#ÚÈÜ;\x0016,¹\x0014@A]´'§»ûëï\h%YC\x0004o{ÖzA_')ÀÑLïÔú<°j¦GvÉÚ`8C\xÎê\x0011#M9\x0011¢ç8Õ3­<´5LÁ¹\x0019.·
ôáËLBl·w¥ÿí¨Í3x°óq2[\x0008ç×»']µ@
r\x001e<î\x000b\x000eFã1|ÎÉ\x001fç|}
ô WX¼¶ßÏ×Ý¾Óåý\x001fl\x0012\x0008Îé'&\x0007Sp*{v\x000e(C2ÊIêZ½Êtz|öüyßs×ÂY	Ù\x000fã`\x001b²XRÉK\x0000\x0002\x00130µY«\x000eÔò¬DÅy¢¥ô\x001bà¡ñ!X.Ç=RËµ®çALn\x0010È\x000bGï\x001cÜ2óx"§"®¯\x0013aá\x0013T.ÿ<Heölý¶ÙÀ%}X&ÂÇHR\x0001±V\x0002\x000c!}°úÝ\x000f»î½¼¸ÞÀ\x0003+dXNb\x000e­^,¦çÙÝ=è;D-U\x000b`3D­${%±m/Ðø\x0018h¿¬[¥YæAä{hm@\x000fÑÒ
¦%\x001e/Ùzíù©Z\x0007\x0017lpqr»A´«á½åT3Á\x000elç¦ïÓX÷ÐÂ\x0004Ï\x0019gpb¹dÙ;Á¡\x0016³^1ªyPz5´0xÉÉ-\x0002¶\x0017Ì)è\\x0002Öþzýº
G)U_§Èõ\x0011Ô,\x0017Â\x001dµaep\x0019¯T}j\j\x001b|¨\x0006ëÌó©aq£üúW´g.ÕòHÖ#Oô\]\x0001Z\x0019×£õÙxÕ<<©§ñý£\x0001Bû\x0015u\x0013»\o	Õòà0<?c\x00002¶x÷,¬wÔòà\x0004\x0011"Y`ê\x0016\x0015¢EÁÏ÷¥~\x0018û\x0008mÃ\x0003§#x0»­Ò&5¦srL`»ýÒ xô\x0008á
y8T\x0012IÁ\x0000mYòíêqXUÒ`¼Ç>xÛM \x0007mhPùÁZ__Í\x000eÆúÓì°vËó¼béã8õ\x0008GpoÅ=yÐa·èððDÒnqUòës{ªià&1²\x0007Ìæ\x0017=¹ÒèjQ¢3nvQsµRYlg@
­l\x0007¢"n^(~-ìz¹^:'$7\x0002Iª<>'©\x001ak\x0003ç¶k³¾Âf"ñùkÐ\x001fÖªW­y\x0012ë=\x000b`¯SÝ¢÷ÊÓ\Z'È³ åú B\x0019/ÑGuþ¼»ùN\x0012¼ð!e\x0014éþéâêêâîîfw+#\x001cáµ1í%«±_;\x0007£ýhw÷ôô°\x0017æbyùÍ¤Þ)±\x001fr3°ÓÅý·þ8vzM\x0018C\x0001Jy¦Ó£:õ0°\x001e§ó³¾ÉÏêyÿõÝ·­¸ÆîÇóË[´µþ´X¬I¡\x0004Ì(©ðÏ:Ê\x000e\x0016\x0013Û{³ûrgïð¤Øzõ#ØwçÙÉ
ÿEü³{½¼<¿¼Xöï\x0007~Ms£\x0003ÖG¦$Âè97µ[~¸{p¼·³·{|ØKq¹´ÃU28ÑMmÝ1±¿4É[\x0015ò»\x0014£ãä\x001f£â&6ÝÒ¨#L]ügïç¯¾¿Ó\x0017\x001f\x001e\x000e~Á©_\p ;î·8ë\x000e2ZÁõx¾+MhôW{¥ë?ì×Ør\x001eß_`£§§ïþüÿ6tôñ8kY\x0017\x001d8Î\x0019l£\x0003·ïÇñÙ.vzzúënéo~\x001fBdOi%\x0004\x000eß¢:¹èMÑ|m­ÎÙI\x0014Ù7ZKá¸Ù\x0014PRxKVX§h¡"[úµ\x00146
áæÌ\x000eÊtñªÙ\x00113i-8ß¾\x000eÃVM!ó=gMÞ\x0012[lj~<	B{µ«!\x0014{©p
\x000fu3q\x000bÎ]Gå¯§ \x0007uíbø¦Y¶¤ÊýÃîV#¦QÓ®ÂH\x0019\x0001å¶¤4*P$\x0001/×êöõ²å\x0015K\x0014\x0017³«æ]Ýô¬\x001aËÚ´ð+[ó¬¦ô®ZûàxìÎZÏëáf¤ì\x001eäà*UòöèÄ\x0017­ÌVD-V½H ÄÆ\)áÙË\x0011W­\x0002W¡\x001añà&!Ê^ñqkä5ßjÌÇa\x000f«åD\x0018e\x001fû1H-y[¿mz:%»JeAæ\x0014·[¥¬\x001fCÂ^»$%w*)ìÊù\x0007·}\x000cPë5¨\x0006)c¢ÏÙ\x0004\x0018ïaÛÕtò¨F#åäqH 7\x0018Z$X.E\x0019wóCuªYÇ"u^«ú}óO\x0014'Û§æ\Ñ4¼{¨Fa"{h\x001cµd\x0008\x001eÐõ\x0010ÜðFNßÑHä\x001e\x0004 Ïwiª)£)¶¾\x001aÞ¿1oÅ]Kÿä®$÷³ãûËÛÛEes)\x0000÷-äÞ±\x0018>dk_ËNö\x000e·$9\x001díìÎÏÖð|¯¿¼ÿ±ª\x000f_`ÓÛ
o¬3M½8\êWØ¦î6¼¢µ9><{±îmAt\x001e´!\x0008åK8C\x0015`\x001d"5¡ó
.âÎ«BkLÏB[ýh©\x001f(\x001bU\x0010Wk\x0008BZ>\x0017*²ñ\x001dLx\x001dâ´è¼	\x0003\x000c6Øòd6AÀÔRbÍ
®è¼\x0003'Bò\x001d#r\x000fc\Pêw¦ ¬\x0008ÙÁÍÐOø
\x0012%ÓÛ\x0007~ô¤eàP_åf8OM>\x0011\x0001ßÄ\x0004!9
ª_£äUPtåè\x0010\x0005Î\x000cg¡îJQWnFB}0LÁÑ½Úµ¤]&1n\x001d­E1W»\x000eöz
j¬S»\x0016%fÓ\x0014¨÷dy©´´!\x001cË«ðª4*ÅlKN3\x0017ªPX»×Ëi\x0018\x0001[FM-x`±¥ýæ&É`ú°ï\x001a3.FJ\x00155$®yÎÒ\x0013-î[Í£{°òc2\x001aK\x0016
ÛãÐy\x0011\x0005«ãR@%±I\x000b.\x0018þÑp®dÆ\x001bÃÍ
%fùë$ÌÖÒ}ÔKµü£µ{\x001f?-@\x0019É-Ð/ï6U\x001cÁËëèL9Í­®e1Þ¸;;\x0011í½<.û ïlÉ*É\x0008\x0018ô:\x0010Ò¬Ö²ïXvÚ§#ÉGi\x001cåçP±á¯\x0004·àUcY¼ß¿|Ys¬ï\x0007SóR+êí\x0016R~§\x0014}\x000bbÑ¬94gÝ,Æ\x001eno½a(\x0002ç/zë¹\x0010Ü\x0016=!ÕÌMÉvõ\x0008\x0018P(7\x0017£\x0007j<f¹½­è&SVÀ|\x000búÆ¶;µ7&Çóå\x0006áì%\$jòçµ¦lS\x000c¼\x0016õâóÃãµâ¹EÒÑìIà_aWíòFÙ0kõ¥èq\x0011U ¬ºP+\x0015IX7GYB6:ù¸Þ.ìCòí\x000bÿ`UngGßþçúÏÿ\ô_jÉÙèQxti]\x000c»ß­\x000f½B'³£\x001eï\x001eìî®»Ô-öÂTÒXC@Qa£¥L#¹¤ÐøÐò¨¥i;¨j×ÆðÈ\x00030\x0003Yõöu\x000b\x0013âÃó[Ó¶\x0001jq\x0014¾EÉ]Æ\x001b¥Ù\x000c0ÖO^®1P	\x0013u\x001a#0 wÃÅ§IBG­1\x00127òKyó½-fnîï.fÏþüÏ§Åòîâã\x0005(\x0012W\x001bîï¦Raá&7iî6\x0006÷íÌ<\x0000\x0015ð\x0014æÇ§»/wAØ_w¹ZTt¹ÆQa¦\x0010u£0N²vã\x001d»]}×Å9\x001a\x000bã dPTà\x00165X×§Cpú
][j4\x0015Yú#©°H:'é·ÊqÃ\x000cl\x0017º\x0015\x0015Ùþc©\x0002%¸,ÃFóÜîX\x0007v,UiêCæi\x0003]LÝ¦J¨saÓ\x0004-Ç©W;X\x0010nS¿\x0000\x000ck\x001a?{óßý»b\WQåâ\x0017ýð9z\x0017#­Q+eysr&?{6«\x0018\x001eÃ¤^´I½BõBÔ>\x0007S5\x0004u\x0016³\x0007ì>\x0007#IM«\x000b©Ñ¿`¿«7×oÊp°½ïÏ\x0017Ð^P=a´RPóA0õY¡óªã~yyxð"i\x000c\x0007sØõ
\.£IÍÈ\x0005\x001fIa¹îf¿Ãÿ>\x001cÂM!sö	9X@I\x0011sj=úy§É(¬Ñéì÷½§°d=\x000còUï=x¤|Ì\x0017óÅëwÉ¡MI%PÜ]~C\x0006lå)\x0008\x000f\x0019fÆãÒXL?"HNÂÓ½ÿùåÅ|gþô×¾ÌöÇ¹÷ÒÐÇ¥dÉy>ÎuXÊ<åãÔéhàã»HÝÏ²³\x001a4\x0000.Qö\x000b#¿Ný¾.]n¦¨pþF\x001eW³=ù©\x0005ÂTýêü<ü­wÿååëwþ'·#[óu-±ä0ë¬`oai\x0004|Ý9É¾áà¨O\x000b~ýå\x001eX8½ýÇ:_§öáôuj!þùu«åg×öv5ã6÷/?ÞÜÿøÞ!\x001dNãÉ2ÓøüüX\x0015¬\x0018Ó\x0002¤h\x0006nîï½<<ûß¾fÏ\x001d¼\x001a?\x000fO6eFðxöi\x0019Î\x0018E ÅÚº\x0017a; lÍ\x0000\x0012\x001cÓÅÈ¡\x000cÌ4ãz&\x0013ô@Y¹\x001a\x0001dùÕµØàÇ\x0010\x0010wén	)8ÜÇ¯Ç\x0016åÓêÂ\x000b°cÜF\x00004*£¶\ 4uãÅ5âQ °F0§H\x0014sR Æ1ý\x0011¾~»\x0008kËB®\x0016³åÍ=¤ß]ôÊ \\x001f.V\x00119Ô:xúÙÃäB³T­Ù\x0016³\x001dt»íö©KòÕÇå×Ë;·¶\x0011ÄÎâûëw½Pð\x0016×XQj'ö\x001aæ\x0008N¼x\x0008µ3ÿ'È\x001aÕè\x0001\x001aTLH§ÄLmiJ\x0013ø4\x0002a\x001b\x001aò·«äp¯ÒÔ\x0002\x0019ÕðÜÙ\x0017 \x000c½Ú.¦~~#¡¾\x001f÷\x001f®\x0011\x001b­axDÒÇE³æ\x0008ò60£¸\x0011 \x000f¾9>\x001a&ô\x0002\||-ïõúBXÐý/þ¸YÞõâ¨uTÀnE	D{6ÍÁZ³I¨ñï>?<îS­ÛD¥\x0005^5\x0011\x000e±¡<SZIa\x0015cfRë\x000eN\x0005ÓýÍÝÛ\x000fk\x000b,áÎ¿¼¹ýnA)äë°ð}Õ.)|hyæóì\x0004§\x0004`9^{åA\x0012=ýu©ä}doÞÝ.h·}H<W×\x0018è\x0013h´±¸Æàt~ñm1\x000c\x000f¸L@cï\x0000\x0003\x0012½ ÷?Üçëvuã\x000b°Ë\x0016W·}j0&ù\x0019¾å2gøØ`KJ]T±¹P/À\x001aïíôZ?­ïS\x0004tðûXJÏ3¹ÔÝ\x0006ì\x0014BgÅ·Ö`ðó7_Í»?b»8ïôþ3µ&Yk\x00034
­T\x00109ÃÑú$f¹\x0004¥ùúéÙ?ÎzçËWwæµ[|M7\x0006Lxüób¹øÒ»ùÁ¬Ì(ax$®\x0005-O£6­·úÅñü÷¾Böy\x0016îæ/ã8¿leÎ/+Ã_vß½x\x001fnÎoÖ¨Þ\x0017³!\x0013@äe\x0011C`©Û\x0011\x0008OÁ`Z2UÝ\x0019[\x0002«>\x000eH¾~#@tärçã\x00072d¥;\x0018\x001aá4\x0001¥«þW XA\x001c1\x0007ÝñAá\x00026¸(\x000fU·M çÂ\x001aòÑç±\x0013Cî={uPË7½¢\x0012´\x000f*Å``v\x000b¸$wóófBsHp´÷ì\x0005?\x001d?ë\x0019ÁÒÆyµè\x0002-êò>y'[DäÁôÜê\x0001Q¨<WÊTGúnÁê³/kx\Ð	÷öê²W«\x0000ú\x0011hPPT¦SU%0ÝÂÃ§åÙîïó\x0003xaf»/ö÷6\x0008u&Õ¢MÚ)e\x001dA*©Og|.@Êe¤8Oì/ í¬©¶¦ÂñÜòc"U+\x0015Ä:
½Ô¤wB7×\x0003ä\x001fÚìyÍ\x0017öbÃ}ÅÉùåô!ä<T­bÒ\x0001dokscÀ@ú·Àð-¨\x0005SXîa\x0018ÌÓîL)¤öA	dx\x0000ÉÙßü\x000btû7¹2;ó»Þ§^8c
.\x001dÕ{Zï²\x001cÜj½&Efg¾sxÚ×C²Á¢¡Àj./ra>p\x0005j\¹LË¦\x0018ÍetËè1ëE)<¸^1\x000f\x001c\x0007.k` \x001aÏu\x000eÛ@o6\x001f0PÌÛF*\x001b?é¬ÞÜ/o®ûîò\x0006»rdÁgXðRU\x000c×X>¼¤l\x0010¥cwzxv|xÐ¿*/£*Ë\x0008ÿ"i¶­¹\x0017ß7½J{ê\x0002!÷zD
W±{éwñh÷ÇýÆHá2\x001d.SÏ\x0005\x0002R8ý Iâà¹Ï\x000ba\x0002Õ9¸\x0013i\x000eE\x0011À2M¤Ø¹¹¼\x0005á»\^^,+D(V6\x0006|³\x0000q\\x001c\x0011[~¶Ã½\x0013\x0000;>ÞÛ=®nÏ6\x001f*Ëcøà6DÎ0ÒO\x0010°-Ú\x00154#WPa2)»rÈeA@XÜ^p\x0012õdÂ\x001c7T
!Ø\x001a\x0010«v\x0001\x000eÞo×`øô\x0016-\x001b²å\x000eHÆG`GS¶ý@\x001c\x0000\x0017\x001e¾ßæOÁ\x0004Ú ò¤\x0017ÝÅv·¹\x0013M\x0013°G'£(b]Uâ2tðÀ(jYÍ¥ÈfÊ\x0010ëP¹\x0011TÒ\x001f\x0014vb¥w\x000bL5juáµm\x0019	µT 5r\x00161¬SQgGüîÜ/aSûÈ¢Ô\¡=ãtÞGÉml±8­y¹:Rwçì\x0018öu\x0003JÎUã
\x001dKWìyd;Y\¿îóû\x001aitnCªÐMN \x001f\x001c©\x000b%\x000b@=Ì\x000fö«#\x000eðÎ\\x0018\x0006p9è\x0004÷qí­~sOrê{Àj\x0008E¦'\x0010ûAèiÍ­a&ßaòÕLFr.\x001d mPÛØ f2Sè0j&°Ë©=\x001a£ÖIqª!\ÉLºÃ¤ë´`t@gÙ»bdùñH9±A7[\x0007\x001a½G\x0017¯ßá\x0019ß¿¹?¿¸î£Ú¥¡i©\x001d÷99\x0014\x001dx<\x0014Óz×RµwþÒ \x000fÏvv\x000fú½X à»ö\x000eº\x0006bË\x0002¸\x001dÒ\x001cÁhE¡µ\x0014GÉ£Y£ÿ°â8%E\x001b\x000b\x0015íz.¬×#ÖbÖCâ
óiPµ\x000eft\x001b\x000c5íZ0¹à©æA¡+#/NRÚÇ\x0016(È\zªe³Ø\x0018>¶\x0002\x000c³\x000bÌSy{}s~ó×û\x0010­&Y¯\x0004;Xa\x001fCZ</µ| ëç³]LYyqp¸³ÓØ\x0007Yh³*15ê<®\x001bWC\x001e\x001do1ß+£¢~öW jÓFE)9\x0001\x0015\x0001Óo09ãÒæX@^Vë7UWöË[ÝNlf¥ã¿ÿú÷<Oº\x000f99	¤ó|¹Ä4*\x0000Ã1ö\x0001;Abç|{Ê'p\x001d¾íØ7ÉI*ÆÄ¸¢vÌæ8àþõÍÇ÷×\x0017ü?\x001f¢t«\x0003\x0006P°\x001d|îÌ&¼\x0006ÛHaÊ\x0012<QLBCÈ«IÞßþX¼sk\x0016\x00054±ËåE¼~U°7yU°-¦Uñ\x0006\x001e&\x0016KfS\x0005±½ã]\x0010=Ó]!\x001cøg\x0004mRMóHAôm\x0008Z\x0019o¨ÙÉDnÝÄ 
Z Ès:dÚ#+\x0012ßjarªw5
Û	4Òæ8­ÐØ pR¤s$Nü(¯u;»ºàÜÎþüW\x0017ËËëþ\x000b\x00150\x0019\x001d\x0018\x0015õ¹ËªÀ*íÒ8¹H'`sïï\x001eï\x001dô\x001dæ\x0016ÕÊa®¢>7ÆMÊgî#püÉT*P<f:ÕJ¹]
W1'\x000c'ßuö\x0008e=êÉZúòUÜ¿è©g»¹ßxñÈ¥³`;\x001bÝÁ°N\x0016µä´{j\x0007\x0012R»pëð¬ÿDµ\x001eÖ´m\x0006ò:ã#â»
È\x0008
\x0012§\x0002=,m\x001b\x0000&\x000fE 6À)ÊÄc&,Ðû°|wþiÍÁK´\x0017ý¢\x0011M­t°½À:x\x001a#
È\x0003ÿÈ\x0003/,¾«»Ã8Ýå\x0019ÆÁ×ÎOy,\x0006j¡îQr<ÎíâV]µÏ3(¯Ó^í/¾Ü\.7<c&ûþ`qlÌí°A\x0016YKÒÚ¶x\x0004óiÚªýùï{ÇÃ0ù,×Ã\x0003`@l§\x0010Â\x0002ãâ\x00160y£ªa|Ì9u\x0008ãr\|à#³x¿\x0005K~Þ«Y\x001c\x0015)50FÓg\x0016#·`Éõ%Õ,&d=\x0015OÈyt\x0002käùüz5\x001aæüÝ¥¸¸}P­fïâõÍí]ÿm ü|~µ0­&µ\x0010\x00108Ô0)bKøqé\x0006Ð<=<9í»M-vR\x0005NÚ,ú&\x0017.wê´\x001fQ©¶Ái\x0017(U­ÈÞ\x0013X\x001dô\x0003û¼:ÒÓ[%;
óxveR
²y\x0016'ÆcLîu$´\x0000-VÇ[¹
N»$©\x0006GÜ£\x0006LíH³0\x0001\x0007£0\x0019Cù\x0013qÚµH5gÇ\x001cDUÇæÒ\x00148;^(Vuìø£\x001cu¸ù\x001e×Ý,\x000c|Ý^nx©´¢^«°>Ü_Ðh\x0004¤´]\x00074;;Ùë}©Z@+wk\x0018ÈÀ.¥ìT\x0014­y¡-ªËYôXá¶\x0001Z¹]\x0015+êMÞ2ï5iò`\°.¨pé\x0016@+÷«\x0002È*V.|¤y\x0000¤-o\x00196¢\x001e\x000b´|«Íòjµd\x001dçË?ÿÓï7*·áÇBÑn)\x001f¢ãÂ¶¯\x0017uY¬àè¶f\x001dâ°Ù5
\x001c°_¤T`\x0006zÆpí|\x001cF«\x0019Õ0¡$Ë!³>\x0011G'ÍNàè6\x001dàÈ#\x00082ÊýÛ\x0003\x0013\x0015ÃMæhõ¤\x001aæÀY¢Ù"à1\x0010ÄÝ¿é2ËÉÇ£Û®v\x0003Ô\x0006Iº¶¹$\x0015½Õ©\x0013f*G·aíÐùP¹_-rH¶\x000bâÇ±ð\x001bÏ±Ú²v\x0000\x0004»ðÆ¸<[\x001e\x000fj, jÜ\x0001¹úÇWÿ åÅíìÙrñéòb¹Áõ¨\x001b\x001dÜ\x0018¶þÒ,ð\x001f\x001cU0ý\x001dÏövûLÿ\x0016M·ÁÃ0M\x0010E 6%²å\x001f/CQ\x0013iÚíjh\x001cµ\x0003Éz¸§m2A\x0016ñº
M·ÝÄ\x0010M»syÑB\x0011OÈ¨\x0015ª±P¶Ú©n»
ÌÆ+>Â¨\x0013N´ã\x0017çnùQ¨ë\x0007Ç85e¢f%¿_bÏÈ
¢×-\x0013\x001c#A\x00046üã5J=¨cÉï{Ø4r\x0018®ÓÌe\x0004\x001cè\x000b®=¼Üäq,\x0000#WßÉIx\x0006#ð´+&°ÐyÂ)\x0002ÁbZ«\x0007·o
^§ÿL5^Ä%ãó#t³U\x001c%\x001f¸¿­ÓòqÄÒÅNB4\x000f?ÎòuBÓöëNë´,\x001e±pJcy^8ê)°oÑ«ÏÞ$¼N«Ê1·S¢HÎ+Ä[¡Y°ðlm§sðÕÃ
åcWÜw\x0011Gã2\x0017ßÜÄÅzjÉs1û&YT*\x001fs\x0013ô4Ñ³B¬ß³Ü	\x00130\x0007a:Êÿ0\x000cÎ\x0001 I²O1ÆÁùàe\x001aÃÒ±\x0000YBÈ£C\x0000&ÊÜ8\x000b`ÐÇ\x0017F¶}g£a:f@\x0005Éeh\x0000\x0013\x001a\x0005Ü;Ï»ôà\x001c\x0003ÓÑÁ`0RY¬ rI5Þ3\x001f\x0019æ\x0008\x001d¹~ÿî»{x~_ÞÜoÒárçN<½:Wuä¼\x000fI^\x001eõª¿-ÎÉ\x001dÀ \x0018ù\x000eeÊB1\x0017c\½ÙÕ\x0018C;\x0001çS"Y\x0005÷ß]Ûãè×!\x000e+È;84Vm\x0002s¨ÉëÑ1[8dà\x0014\x0004ÁÝbÑàl[c¦Urt®Ì\x0010OEÇYär[LÊ%{èÕ¨Äh=Ã\x0018ºñjÀr\x0004²$§AX±Æ«QÉÑ±+Ê\x000f¡ÄR>VrØ\x0000±ÎM¾µ­·yÃâ]<îÀ¡z:V\x0006¾\x000crh~¥ñWÃ0[ã]©\x0004éÎ|©¦$Ø ]"M\x0004¥\x001d\x0019¦rt§¾\x000cq8Û?À\x0004!bhd.Û¸Æ«Q	\x0002·EVß\x0018Ð8â*µ/\x0011WçYY9\x000edi>½óo\x001e>sCy\x000c¬\x00179T\x0004\x0004¹EUÑ¤z¸1\x001b#ô-Î;7È!H
qð¤qÞInSIñðÉ\x001cnÃå:hl0kÙgà±óbN[\x0008kü¢µ n\x0008ÄÄ² \x001aîW\x0016D\x000fn-Gç¥«8 ÁS\x001aÄ¬Ô¼ 9ü\x001a¬\x0016¤óÔ
./;£eÄKÍ Î®Z°õ ÇnpE<¹\T\x0001
tg"<°UëA:¯Ýà\x0018¾»8±8$G
µ
Ó\x0017¤óÚ
.Êð\x0019ÄðÝåä:mãäË»â´\x001e"Áþ\x001e9V\x0019¥Ì\x001d\x0012¤¨Ëú¡;täòâóÍâCX¥³
³\x0001
\x0019E\x0017³UU\x0005K\x0012¥oR;ÄÙNoÞj\x000bn¬­ÃQÂ$e@àÂª×	n>=\x001an\x0000®[9Ov2ÜxSk\x001dÇ¨´\x000b\x000fµÛÑpkríÊ\x0005\x0002F\x0014ùlµ*rq{¶5ò±náDn\x0017Ê\x0007Ípr¢\x0013}Ø\x0008¸5¢ªná\x001cNËw4äºQU¤é\x0016Cpß\x0017_,>
]Ö_\x0017©5h\x000f\x001dOsÊ\x0017Bd	â\x0002ÇßR§õMt¿Îáß\x000fâm¸®ñð	¦Sçt\x001eí\x0002½\x0012éü\x0017àm¸°\x001bñpJqd<[©\x0008e]IBz³8©ÃÛpe\x00076Wç\x001eÍ(\x001dûº\±Ë@\x0014÷i»cð6ÜÚÍ«\x0017bQµàHÊe'®\x0018¸\x0017up\x001bníÀÖúÎ\x001b\næ[[üak,ÉJº¯\x001f¤ÌÕ§Ýk{|y¾¡
\x0004\x001býÇ&Ö(\x000c\x000c\x000cg0\x0004óp3÷ú¥Ç;kÅ½Y\x0013 >½øøéjc\x00146\x0000â¬\x000eC9R \x0012ä\x0001ÿ ¸r2;Ý}y´¿!ÒØâé¨y¢0TîàÐÈÎKÌÝglMz#\x0012¯>Ü-ßø÷­\x0005Ú¿ýÕMi4¡fÊÞbµ7Ü\x0003
Å0W\x0006Ø±äQ©AN\x0012¨^âüè_rAÓ\x000b,æÞßý%M/új;\x001cÔÞìÑ9²À¬æ@W\x0008qåO\x001cAôt,\x0019+9\*]B\x000eiðUI\x001c.\x000bCàà)@²Y\x0005âMJ;À¹\x0005ñ !ÍçK Úo±"Y\x0018ÿ\x0004+MÌ:\x001022HJ:Ï Ïªñ~:H~\x0001*AD\x001aG :¢íAræ0N\x0017ð±\x0007d}ç­\x000eH¶1ë@lý@°/Zâ\x0008V1é[a\x000e61«·FÊ²5W$¸²5vòÖþ¬µ$Ø¨ý\x0001ý+H¸7kÝ½ÉÃkéÞ¹I*÷fºhe?sõyõ¡¬U¼&ÄO¿Á¥Ëg\x0015	ÎÎ»#qÒºÌBMdM\x0018HDi\x00107áÄrWÖº5Q©p\x0017I°øÙä5ñ\x000c¢äô+Ì\x001eë@HÝ-\x0017esæ«£{_à
\x0012ò¾W?Á8$àhø	öå	Ó	ü%d½ý\x001b%=n¬¬°XèD\x0007\x0016«ÁòyE=qúyåIÕ *ßaé=v#\x0012Þ\x001c©¦Ëz"¨zÍ\x0015>¿F¬É¿@¬q?ÜJaúùñëg
	\x0013¥Ëó·\x0005	uÆ­\"Ö´h­æ5ÉyZ¸&n\x000b\x0012\x0010iªZ¬éT\x0007üÄÿ\x0015$ÜÄ½Ä¸Bâ\x001d\x0014ÀM¿ÃÜ8¸N\x0016¹L:É5\x0010õtu¬äÝ±¥Oê«CócêH`!,Éz\x000cÖ\x0004"|wÜ\x0016Ò\x0004Dª\x0016k:WÙÓ%v|LL¹ÃÓ÷\x0006[êZ±Í\x001c áòë\x0017dÕÄÆé¯\x001ff¨#£á\x001ai¢c&ñ¶ìM¯\x0005ZAB~*7'¤	ts4«k¶¹ÃÓ-?ì¿¢ëåZ(FyÄý\x0015$4¨nw0k¤	(\x0007ùâDi\x0018ÄË>
¶bsh\x0014Qõ`ÛVZ\x0012%yIÊÕé½Ã\x0015K\x0002·NWµÜ>*×éßiIDÑÖ\ØbIàÒéjm
'	4çU%)\x001a®7bSW]/Ö&O$Q(&Cp¯øj\x0008áV Lü\x000b(`\x0015M­æ¢g}QYI®h\x0019Ì\x0001I pÂMµ\ý;A@úZ±ú·ðø\x001a\x0010\x0007´E/1FªÒ\x001c5Ïg¤ç6f£T¸²$`[\x0002±¬\x0018E?ýââA7µRÕcq!]\Ðêe \x0012Ãª|ÓÙm\x0002	HTS+Uqz´¤Íq°:\x0004ÂêH4[¬\x0008ìª©\x0017ª>ÅNHC³¬>ë"Hì\x0016Ç\x0015\x0016ÓÔ
Uy,$Ïp@$½3ZC2ýÁ³ Tmµ®\x0018\*#J[
Ê\x00131å¸ö*\x0001\x0015$°¯¶Z¸bgªX+(Õ\x001c×éú3\x0016~Ûjéjó\x000c\x0008%dÛD!\x000bÉ\x0016\x0012Txmµx56e~$4Öâ\x0015ö/j¨@¸z\x0017°)îNÆef×*1­^Í¨\x0004ÓÕG,þN\x0012¸À®^3²©Ño\x0012'\x001akYsÂ=ð¦à+áë\x00154£7ßT3ßá"OàÈL'{ã«ïÎßybÑ£î«í,\x0005&+º|ä\x0003.Íõ:èuywøz·øßxb1ÜïkU\x0002g\x001a-É)tÂæÝ	ºé*\x0001
E_mh¡Ä>
	wÙGaøX9ÝGB_}ÁôU\x0014=¨¦äK\x001c	\x0004óc&à¾zÇ\x0000Ý\x001ba±­Ô,Ñ½!¶
\x000cø¯êÓj-+k\x0018Äac<¸\x0012ÅQ}êZ\x0005	¬e¨v\x000bH]ä¹ey"ÑÆ\x0017ëbºk\x000fó9Cõi
&ÍíM§Õ\x0016ÀèrZ·ð»bG¬P­8\x0006R\x001a\x0013Iê3Htd§ÝÂ?\x001fAkÕ£E_#\x0017cÔ%Zoõ\x0016\x0018p¾bõÓçC±-\x0014¦\x001e\x0011Iq§qóI$p¾bõÓÙ¦D#^7g¤7\x000c[\x0001\x0002\x001ac¬÷uº^¾Bâ©!nòÿN\x000fka6W¬\x0016i>5]Ë$#}"\x0014wÚ\x0016\x0016(j4±ÚÕ)ró\x0004æ¨ª<_AôtÃOG\x001c
\x000c6äâq\x001djÊ¼:Oñµó ÀÖÌK®>²¡hÃy\x0013<Ù"\x0002'ïa ¼\x0016Æ$#å2®¦"-\8Ø±/ÁÔîÒß
#ÓÊÈúmú\x001bÓo¬@\x0018+jaPÞj_¼JõÚA¦Æ\x0016\x001a.Ó"]¦êùË/ÓõÅ÷×S&5\x000f7Ý_ÌRGÇ>\x000e\x0003R$íÍ[tD"sÅÖ\x0010±{æ³ÜÍqÂ\x0003¯¤\x0008\x0013`e(	°\x001a9bbÅJkâÍâÓuH\x0014xÀlrøÝÎ^.îÒ¸ Û~\x0014#eä`(¶øÍ\x0005.
«³N®ê÷'³óÓ4.¨oÞxõÎÝ-oÂÃ<ò\x001b\x001cÂ°Q§õ©«\x0010¥9²ü×lnÀÅîèùL~rÓ\x0017jp:õ\x0014U8Á\x0014#9°\x001dcÁQ[átê?+pBHâÌjºEFwº{êpî¯on¿~lm\x00165¿ZÌö/\x0017÷?6dl>¯\x001asÊðôH#Hú¦Ð`\x000b\x001aÂÃyÞßýoÿþãÓ×\x000f\x001fR«1lÞîé@?]üX\]ÞÞ^n8Ñ\x001aî\x0011»t°È\x0015RÌ$W\x000fôÓùÿÎ÷÷NNöúO´üj¿-.´\x0001\x0001æ?\x0016o\x0017W\x001bI²wÔ¡W\x0007Ñ±î­H¿3¢Ü\x0006\x0014/æ½C¬;\x000cphðO\x0005ÍÃa\x0001þ_ù}R0sc\x0010>}½r_S%\x0004ª¦6e;×\x001buËäÓIÂÎÈâT±%L\x0010«êöÎüi/Á¯W\x001fÿH'°\x0012þyº\x0000!wsÿ±\x0001C,èáU\x0008^
ìÓ\x0001\x000cV³\x0000\x0007EtÄÊÓ9È·Ã³½\x0014îíåù#QÀ\x0016âýÛ""çâ\x0018´N)Ò\x0013ùõ\x0001³,®È}º'\x0015\x001c ªãH­hó\x00151 ?\x0005
ÂyVâªwi\x0004\x0007XÚ¿àªõÀ\x0011;ùh\x0018°Ä\x000cI\x000fGâ,ÕW°\x0002\x0014þ©¢P1µLA
J\x0012ô¤D\x0019GîÊù\x000f³ôébÀ\x000cÿ¼¼¹¿º¼^lÚ\x0013oKzTÀ	ayO¨ÕÃ¿îÒgû{\x0007ó\x001a\x0006øïáa\x0006l\x0002\x001e²Ê¨ «
+Á*cpÝ\x000cåz\x0006¬\x001bÁ?\x0015ë\x0000yÎì0<}Øeu#ß=\x0015õ\x000c\x00013üS±\x000eÒp\x0006.Î#´\x000eBÐ=
²ûì\x000f2À3í<ºY¼Ú\x0011i\x0002"Ê®fÏ.®fGW\x001b¼OcWÓ;«ðÎ$ ïwVvå×Ë£Ù³ÝýÙÑþ¼÷I+T®Cåª©"Î¸3DeÐïT*pÊtÝã2*6\x0015FEj×Êy®\x000bÑ!Ý\x001auY«n¶Ô0¯ÎÃ{}í;ï\x001e\x000fE¾º\x001dßÜ¿¹LSBó$vøk'¦E*\x0002ôÊ\x0006§æª&bjK\x001d\x0010B\x001aP(qDC±:æ§Í8dx
\x000fÏíõèI\x001d®b\x0004áÃªp+æF\x001eÀ\x0015l`.³=\x0017QGqåÔ\x000cäÂ´|¹¢,\\x001d=Kýnà\x0018.'h±ln\x0016k´\x0015÷0Ø­@°áqGË£LT \x0019Òô\x000fÜBi2Ur[.é°égÔZåèÌ[ÂzIáx½µ©\x000bfkÑ&×â¨53)Ù5­Í­üð:úÀkf¶ßKhpÀF¢)\x001b¸(T¤@iW­Iò\x0018Gf¿-¯¿v²q\x0019ë·Åk\x001chp×Ke
yÄ\x0016NByN±.äiÂÒ¹V^}\x001bë·ùShÐ3¼KÅ¹#¨pìkÈT:"UÐLµöâ,ÝqP©\x001d!B)°g¨<É\x0014 Ö¬z&b&ýò"7\x0000(LuS	Êcc\x000cÕÊb\x001aõ]-^û\x001fm«¸Pí/onn7t§ò$Z8E:·Ln"\x0007xÖøùñ³Ã\x001e3½\x000bD&r=Ï5ÇH$|\x001e}\x000eD8ìúÇ°\x0008\x000b Ý\x0018¢àÕÖHÒY\x0002Ù.TY#¹\x001d\x0011'\x0016Õ\x0013åÎÕ\x0000¤Dî#@Þ@kÖ\x001fïz Øs\x0017Æ\x0000¡6¬3f\x0019\x0000D?ë·\"Îxª%r:æ\x0006\x0014@ä#î_z÷¢cäD\x0019$>H'\x0017¦Ðc°¹\x000f#X\x001fè)ö\x0016ÉÿÿÌYTG³ ·\x001bh,æÁxÊ*RP²\x001aP
²«~Áª\x0004
Õ\x00005 à©·ÑoýØw\x001dÿNz%\x001d\x001eá\x001e\x0019äÉ<qNIÂìê\_¢>bððÙ¹\x0019ÄÞ}¼{ïÊÂµÝùÅâã"M¥_"¥öÏ¢\x0012$QlË\x001ed¦å$³­(÷kwúböë¬k\x001c}`xx\x001bdá[P7\x001e?yYvn\x001foÒluæAÔ\x0003\x000fë[%P
àÒ\·,;Gg0g;\x0013ÔUÄO\x0003SB&"9ïÒH\x0014\x0017èãaLÎ8&Pæ¤k^'Ö)\x001c¥ØÃ$®\x0013-\x0014\x0017keu((t\x0006(/Óì)\x0011[t¨¡Ã,B	»V\÷çLToZ¿	JÔ\x0019V*\x001f)µVOêÍ$¡eDüôg\x0012Ð~7¨4ñ\x00088\x0017t¢Ôz[j\x001b¾y÷x\x0003ó
aâÃóøÙ¹ßßÏ¿v£(æcµ·\x0008gÇèg\x001c·%9\x0014,÷ÊÜÜ9Lÿ«\x000f\x0001Ü3øô 0ø^\x0004\x0002Iæ=Ö\x0013°C\x0010$¤ZÅÏv\x0004è\x0015)\x0012BÊ\x0002\x0004)\x0004!8a\x001a\x0010ÄuÐÀ¿\x0015G\x0007ÆÏòl,¾_Î»ÕB\x000ecÍÓv(fÓ Ö TXsxØ×\x001f×ÙÿÜëv, W*~z\x0003Y;\x0004 ¡S#© ThM@Þ¯Ué7\x0003½½øk~=@Ð\x0010 \x001a²óÉË»ùãýý{\x0013l®ÔfKx¦è.{J³
6G¥ZL'/§g''\x001b¬C\x0004ÑáÉH>c=IO£V`\x000f\x0007Ï}$áäzpE\x000efM²6_iäÍ;dy÷/-0·\x0017BÄ·	z\x0002ÈÊY4¼¾½ß-.6 ÅJ(â,6°Iê\x001aî5)bpd~3y}t0=½è\x0005\x0007\x001d®¤hÝO"´x¦\x0003Çë.¸îÐàb\x0013\x0003Ù\x000e\x0003\x001c\x0003\x001cäù&l$¶õ\x001aP#\x001b¼£Ç¡\x001f"/M`$'¡¹>Â.­µ	\x000e\x001e¯ÊÆï\x0005\x0007
}\x00130^+íªW\x000e2\x00195ô±p:¶aÐí»*Á©N:r&o+_ïEê\x0001wñíóû\x001e\x001bH\x0016Ïë9ÄSºy\x0012"Ö/\x0007\x0015+f£\x0013*­\x0015\x0001Ëgÿõ\x0014)Ý\x0004Þ«O\x0010äã
\x0012?¿,î®\x00170FïöªBÃ°[ÎzØ\x001d\x0008Ì\x0007
\x0013Þ{Ü² \x0014[öËìø`\x0006cô:2'j\x0014h¿\x0003~(a¢ç* \x0008¦\x0012\x0007\x0014Ijb§¢\x0011åòöV©;84±cÈ(Ç·»ËN\x0018\x000e/m3&b÷ÆØ>W	æE\x0012è0»ÿ\x0000s<Û\x001d¿ØëÄ¹ºr¿~-£ô;ó»»ùÍâ{÷9Q0AO$ãPÀ4¨`;'Qià?,5£éññôpÖERR\x00088§ñ³\x001dC£\x0006\x000cÈ]ÅÑ6É\x001dí\x0015k£¸¼ùzý©jfòj~½?ÂD©ùÇÛÇ
\x0011IÌ\x0004Ý4S\x0010Æ=BÒ4¬sÕM~5=MÏ`ÔÎô×£³>DØÔ¤?U)\x0015`ì\x001bªøb@ò²\x001c\x0007½Mz\x0003Åºjôm:Æ§#
·ËXV\x0005@\x0006\x0010aþD\x0012\x0007\x0017HÎBuD+ê\x0001n\x0014\x0011u;éO¤\x001c\x001d#Æp\x0008
¬tHÄGî\x001au=éO$dj=\x001dÂ\x0006út°£\x0008NDF\#ì~ÒÈc»éä2i×t¬¯)çÜ\x0018"Éâ®µl±\x001ec	,õçÁ96]ì¸E\x00121~& ~Ö_\x0000ÔÄ.@Áv\x0014\x0000FàQÒR
H÷çfþÞG[\x001e4ÙÊ½y0¿ûü¸ÉÁ\x0011lz\x001c÷<l¢H>3è¨,\x0012®íZu'h:¿uí\x0002	\x0014X¦Z\x001f¤3#'\x0010\x000coK8EW\x0003Îíqï£®\x0001\x0017|Ò\x0003zûxw³¸¾¼ëæ>pðä\x0001\x000eV=T´Ã®q§Óá\x0006\x000f£þá?=:;>\x001dì\x001d÷\x0012à\x0006(j\x001c)û É\x0000Î( |µoíPabþ¾\x0004þ±nÞ_½ûÈÞ-çè<½^Ø¤BËØ1\x000b\x0005¸Ã\x0000¬â1q0=rz­¹ñz¶ûj.\x0004d®ÇO&Hª±ê O\x0003ÔT¤
$\x0013eE\x0013ðiÈV RQ«DRÀÔëc/Û >Ü\x0008ù8¢\x0000Ô\x0013V§BÜO¦7\x0017wÛÇ
!\x0018i\x001deÚÿ\x0015¬¡èw\x0014§b\x001daÈN\x001e¾8\x001du\x0007b
<ÐUoÆSÊ¤\x00001L?\x0016\x0014	\x0001CðÖGÑÚèxlùÈÛé4ø\x000b\x0002ã¨Á@Gò¹õÙ\x0007­tp)¹l§Â\x0000\:RÑ¥\®ÜúM+\x001c<A\
ØX¹<w\x001aeY 3g×_ÓF<\x0013
\x001b3\x0000O£!ìÀS¡iñPyWu8Çð$$wÇOóÖrJ	`Ú§qJ*ºvÒâAYñS\¨¥2³F@á¥kË!\x0003\x0006\x0003sÞÒÍð#ïó¸ÕWeòîîíãÃå<\x0013¡Ã3\x0002
Î[N19\x0019Ë7££ÚTò\x0017Kö6dd\x0002ÁbÛZÖ\x0003!úS¢/ØYïr¸KSJ£½M\x0007 @æpülG:D\x0011\Ú\x0015®d&PC\x0008Â6¼y{y\x001f·\x0002þÝÐÉ\x0012v#
[L»A¢Éië\x001a@îÕ÷÷\x0017\x001fÊ.È:º%HÌ½¼y¿Á[êSÈ-(Æi\x0004RÐ\x0011*ùÊÒ¿\x0001s0bÕ\x0012äåî\x001d¾ìÃUT
<8\x001c>!¥ñÞ$úÎ¤{{S\x0017ÜOöç7î+¬\x001cÄ¼ÐY\x001b\x0004ÅÓK0rsûÊ[°?=ìO\x000f»jïJ
\x000e­5â§\x000f\x0006g´$"\¡8ö]\x0005#\Zrh×1þ\x0016\x000cpÓÆµí\x00180Ý\x0018}þÉÎ\x0001ºdZ\x000ckü0
\x0001Í,â§\x0007E\x0010¬ioX\x000cGqÈ »PIé¤\x001d\x0011ý[®\x001fvyOÂC)Ój@C8ÄPÎ\x000cÄ¨lüôÁP<%\x0010Ø°ü0o1RhL³\x0004ñÎRÊ\x0015û6ô \x0008\x001fª¤Ö°=\x0011cb¥\x000c*ìÀ{"|ôðù~\x0018e×}°h5\x0018pe\x0006n\x0004µ=~úÜV\x001d\x000b\x001bÐè\x00192ið8½\x001e£+ \b@\x0001>¼íEb¢÷.8¦Å\x0002\x0013$¾jÃ¦iAbã\x0008\x0016Ó»ÿmóDrþ¯¼Ë½G5vÍ\x0017Ù÷óëb~3Ù¹ßwÇw\x0018Ðh\x000f^\x0004\x0008ïh:b­¬\x0014ìÉ\x00019w\x0000µÛ	\x000cu!ZÀõcÓe.Ë)"\x0018\x000c\x0008ØÚ,é
u/>~[\ÅT\x000fÐQ|ÔR.6ìô\x0012ÇPÃð9N\x000cÍq«ÂNUù£ÇG/6lÓùÅ_s=	 èT´|úxI#Âº;cwP\x00064$\x0011#@ÄÉÔú\x0008hï§g{8\x001f¬ãB\x0017,XØEB\x0002ETG¼µ
ß\x001c\x0018¤$ÖµS®bé³.±`CÇ¶\x0011½\x000bôÅy\x00174µ&®\x0004w\x0016FÖO`\x001fïÖ}ü\x001c«DiÌÁãÝûùÆ^C\x000f±±Õu¬IÇµNÀ98;~9íõóqhË¿ôóc\x0002è\x0003àÀ*#\x000buªéÊØ>iÌ¾\x0012"\x0008ÐùØ,\x0001àåÏÖ\x0015p,MÛ\x0014Ðc\x001cc²AvYRÙ\x0015C\x0000 CRül\x0003Pà	N\x0000>Uê&\x000fFîk?Ï\x0016\x000bËß[Wu
)2<àZ,î6	Éð$Å\x0002BÁ*\x0005aTlE\x0019oàº+á	nÇìxC¡PF-6ÛÐõj÷`ºí3]ÛV:è¾]éN-hÔs³qÕ\J>\x000fh°*H\x0001lEiq+Ûõüëïñ9#\x0015§Ì'»w·Ý© A4ã uHvÒÀ\x0016x¬ñIÚ$ô<¬révöºsA¯¿^-þ>%(`\x001fßÍo\x001fß.\x001e\x001eº×\x0006Å.
Ñäáà7\x0017Yy|$$1¯ L§Gg;³Ó®¾4\x0001?ÞJñíMÝ4Õ_o°Îr`Ò6IÁÉoá4\x0006ÐÂã,«mMRýu'ÅâëÕ­HÝq¨ãr\x000eä]Þ-ÞÎ/»su\x0014×*©OYm¯@C?£\x0014R\x0008+´>¸¸w<Ûvu]Ybåþû÷¸n¿½gçoÊ\x000cÅ%ÛYÜÝLÛ!ª4$\x0014¥°µS*
nVÚ1\x0010;ÖQÙ5Ù\x001d\x001fN_L7%\x0016x4¥¡\x0011\x000fÚW;\x0001l\x000bç
¦_'MwT\x000cµáåù
­«\x0017n\x001fOûêÍ«G\x0019êFw\x0015\x001a·òÑdÖå\x001c~Ëç|×cÐ6àu75âÑ¼f<óçì\x0004¬Tõ\x000c­\x001dÀ[\x001fïhÅ£)\x0010­xÅNÔ¸zLâòÉÌÇC4óé\x000f|\x0006}×Ï\x0013\ßÌG##\x0006ðy·Ï>)\x001f®~\x001e?Í×ÉT\x0001\x0014®¯©K@0¶3·O!ü wöyü4/`È6£"­½Vy»ª{ð}¾½øìâøpN\x0003\x000fÚ÷ùÕ|C¸"üqèÙ\x0000\x001bcÚL¾\x001aÊvvX8îO7DPÞ~9?1\x001f$¦,wõõâbq>ìVÒs66J\x0007ÛG
>\x001bIå:¶Î\x000b+r
^ÌNv§gÝÚÚ_WJ|½Iè ­ÉÈüËíãÝÃbÞ\x0005«*Ñ01YéLãZWðÇ\x0004â_ÎOgÓî$,g>½ÿ|_Dxfaiîî6E\x0012r@MÚ4-9æ:*fÐ\x0012^ÕrÏ`A7¦ìí;ý§Z4\@ø`\x0016óíU7\x0005\x0007\x001f¨â©ì\x000eºêÇ7[\x001a*9ÌØ9>Úï\x0006ùb¤´±Þ\x001e\uñóúòócÐÉÂzlÈ\x000bV ¦*xð»yÔ.¬&W­Jª^ïýv6\x0019ÄÝ»òéñ|áÎãñ\x0001¼¶|uv./6ÐhèÒ:,$É¥ðzØ4eH©__d¿³÷b\x0003ÐÃ9ÿ\x001a#;pÈxeí,®\x0016÷\x000fÝ%^P¿µ\x00006\h\x000c­;		 À®/ÛíÏNN»¼î¿ýùýAÅ\x0003¢\x0011>»óïùÅ¶"å\x000b	+ÃRI,×TT(¡bÀ¨¨Fþ³Ãéï\x001bR\x00063\x0004¤çÆÏ¿	é1¿óç¸øøp%ï¢4\x0001\x0007ñóç'æïoí·!f-5Dï;Ì¾ÅRu¯
%ß\x001bVB¼¾<\x000cÆß°uzöÀ\x0010><\x0012K\x0000¤6,©|Ä\x0010Ò·a|`×ßÅ×xi *2º|\x0016÷Ù·ó\x000fóùÅ¦,\x000f)¹ ÐñÔ+\x0003pÐ÷\x0004}\x0019V ³?v_Ív§/6f \x0010R\x0014ÒÂê\x0016$è%\x000eea­"b\x0014-\x000eÿ\x001cB¤¾__ª¸(9Q6½Ï±\x0008Æ7\x0018§äö°8(ä\x001c¬\x0003àD	Ïro.C\x0008Èî\x0011ØËp\x000b\x0012Ä$i\x0015LH\x0015=á
¢R¯4£!>+ºsG÷ÀöÅØ \x0003fBË6?XA\x0003Ý²y\x000bÆÇï\x000fç\x001fnc<\x0005\ÕÞToÏûÛ»
y´v\x001d{>»ÍÄ\x0014mp)	NH¸jÞ½GÇ\x001bòh\x000b(Ðç¼mr±MmrO*c\x0015¡%\x001fàúLÇ­Ló¿Ø·èþ\x0006^Â¬ó»\x000f\x001b´r	E,X!g²ËÄB²T"gº:½LöpújÃkpi>È?ßprÛÇó\x000ft\x0019In\h>n¦\x0008Ê­·óÏv_mÐ\x001dæÊÝH.\\x001a\x0011TX\x0008»Añ½[l| ¼ÁªP¯]ìý\x0012e!Æßµ\x0012]éÝ þ\x001eÏ@FwÝü\x0012.¶ç×+Ý»zñ1lÿ\x0002O\x0015%E\x0007XtÍ«b|m'`g íO½ø\x0018Óíc\x0006¹
5o\x001e\x0016\x001buccÈ±kNî.n
ö\x0010FT\x00195\x0007G§³
zñøðõóuKð¹ÒÁµ?¿»¾¼¿ïVþ\x000cäxòtÌ½1ØHÄºÜp\x000bÞÕôé`ïä¤[û»}ûåÝü1^?Ðþª=§ðÖwò «Q%\x0017\x000eTò6k(JÅ,9¶þ ÎÂ{ßmÈ|à\x00176ZÂ):\x001eß\x0010(>èÞ(ã<ÅáSC@º\x001e\x0016?²U\x0007<\x001ct\x0002ü©ßÞ<$SÇ\x0011\x0006Ïj~µø²©jE\x0007­Gáî(Y3LÆµé\x0012\x0014òýÙï\x001b
VnnÏoîc&?8Tãç×ùùçÇ 
7,§,\x001f£¸§î\x0002J¢[[h]\x0015}ÿ:Ýýí,üCwº{Ð\x0017ñ¼Â\x0003\x0006×á.>Ý^~ÙðLh;§.\x0007&<Fj,u9\x0008KUu/|\x001dNçìõÑÞï\x001b\x0008î¯å×e,äõâáòá¶»47ü©5§¤\x0010t4IÍ2Xe\x000eÉH¥]ûzvºwz´×)ßJ(ß`|C\x000f\x0008
,\x0001SþføÙÔÐÊ[¹\x0006¢Óëq÷ñÓûT\x0005\x0013zÉÂÊ³ðïÁ!í>¡ÑÐOé\x0000Å6¯p<Âß£øÒüÌ\x0002ÅgGp^ûPÅ"&*©\x0014z 
L-\x001ebÙYùÿèéCõp{ýöñM1<.SíÎïÎ¿m8¿Q\x0007UÈ\x0015K	6ÆR\x000cRm-Òîôx÷N\x001e³¸ø\x001e	H(¥'-u\x0001\ü¿ÿõ¿g7WóÇîkný=ÑXké¸@S\x0013º¾®
^akÉÉìp\x0012Ôî{ïùw'cóRq\x0008\x001ca\x001dÞïûùU÷\x000b%\x0004£K\x0013G%û3èa\x001c\x001dk¾Î2¯öÉétCëà Ø?\E÷#ÊÓ\x000fo7­\x000f¼Ê¨Ekf0ÙQÅ-é¡´\x0015Æé«½M«Q \x000b	>Û\x0011À\x0014Cã\x001dtPN\x0008r`Ã¨\x001b\x0010Ä;}ýý¶,ßVg
Ú9Ï¥ïØHSrl:fÂc]àT^º¶\x0001wýÓ±à}k«NÝk%gñULÑUOåÉ¾Òzÿp,nßZ®mãäXÒNùAP)²]i@Ðóc\x001dûÖêõØF1þpïÑ@ÒÐ\x0002jÅ«¾?jÖ·Vó§9AXèè°ß\x001aúéB
ù³S}z?{®J·Ï\x0004þÑ©nßØA?\x001b+Ñ·ýì°Ó\x0016{ìêl\x0002B9,Ö.Ú!ë¾¬:ßòã¡\x00112öu`¨µË}kk'ÊæþÑß,¾¥û8àsg1¼[¼ß]lx²å\x0005ø°øÉ]`¬ÂÜÿÀR½í;³éÙñìåôøE'Çw­\x001f.?E\x0007\x0017KðIÝÙº3Sc8tûÔµ=zA¡\x0011zÊó²U{«Ô­cZI@PæËõ§%\x000b½Ùã' |Û¤MXhI-1_WbR\x0010$Ù/-¶þpìw¢bvn>»Î ÛnUÜÆQôö:Q
Í\x0014u8½°Ö&\x0004\x001duÒØ;þåÝ·R¡\x0001=¦[ùÔ0Ó
Ë¹bV5ê1äh²ª*¨/{ÝkñåúOÿç²sPAh<K¥ñR\x001a#¨ö\x0001ôàúÇ\x001fí÷ùñÔ-hÛW\x001cÃ§Þ&Æ(k\x001edÿ\x001fÿþök0ðàÇÃÛÅq÷îíõ´0\x0011#H©ôV@a0v/c
ËéV:¥:tpÚ}\x001aß\x000fêØ\x001f=fÉéXM÷íüÃí\x0006EDCB!Çh#\x0008iMÃ\x0013áf¥íÝWG§\x000c·þúÓµ®Ã®Û\x0003®LáA0\x001aºú&K)\x0003®U§´\x001cjí<\x000biw\x001fS¢áü¦¼¸_rzùÿÞ \x0019 \x000f`ÊÍ\x000eæ'\x0004ãf(
Ø*è\x001b6ã îm
Kp\x0018|O\ã½³0,z	r§\x0019FAéÐ½0<{º0H	¡¸\x0012i5\x0014"æ\x0008ô\x0001_Z§µ0>{L°Ý\x00008¼ì0
\x0001G:~z­d)\x001b@B6!Eî\x000cu\x0014
\x0007V¹a\x001c\x0012Â\x0005ñÓk9´u!ø
pqDFvÎ\x001aç\x001dªaf/\x0010ô¸°/ÞâmÐ7\x000b\x0017Ä¶\x0005áìË\x0004ÁcfDZûÉÑÛË
9ã+*í\x000cÒ3\x0005Édü×¢ôvu#1\x0008\x001díìv\x000c_«)Àd¢\x00173*\x000e%\x0005\x0006ºÈ§Cê°÷ô|Eo£øöõíw\x0015]%ðøÀ_Áôÿü¸qþ@jy´zºD¸\x001ezt	¾Ò\x0001ð·³Y·\x0004¿X\Ê»hÜ/\x001bÆ¾[\x001b#æFèÃðt.%\x000f§ÃÆKæõÑ\x00016Dì\x0001\x001böw-i\x0010cfXÒà¨\x0015±\x0010ÌÉ
A{®LxÜ±îÖ£C\x0006&)RÝ­Rj\x0004Kn\x0000Ú\x0005|hI\x0001\x000e¶&\x001a\x0002Òæh)ô\x0008Üï³\x000f~»Ø±\x001a¼\x0010Éá\x0018Þ}êó)\x001a±IËþ½\x0016\x0006`\x0014Ö\x0015\x0006U@`_O¯áÄèæùpÿþñ¯(S »#~^ß->nºÍûÃ*l°\x0012h¦ê\x0013\x0019ÇR\x0017·ùxöëËügø[ÿñMÙ¸r{ËJàD\x001aÓ\x0002u\x0010Ásù+çU-jVÙð¨\x001f¾EtÅ´E\x000f\x0008ÝÎUÐ\x0001F8/sÛ`Ò`3\x001fWÍ08ýÑ½úç~qþXå»mÉt\x000b·S\x0019Ìtc\x0018þä9¿T\x0006\\x001a1Ç­ÓL'/¾
\x001dN¶eû±`\x0011£\x0002:vi, Q¢)\å\x0013¤l¿.¯ïÜÇïÕîäÅädñþñòfC¦¨áÔ%Éiu8¶,X\x0006DÎ\x0002ÙË³½Ãi÷)¼{øúÿò¦ì®¶l\x0015\x0016ýíq&n÷ÒÏ&Ù©R3ê\\x000eÆI:\x0012RTñ¢e·°ètSq·³-¬µ±9è«"80T
³B2ytY\x0015Fj»¸¹x¼¼¾ð\x0007tÉXÎ\x0003ïÒ¤Åð°'¶ìó\x0002Á<Rï M\x0003ßÊ\x0011Kßâ§\x0017eÔ?(Ç>ÎòeÜª\x0006ß\x0003|=ñÓCg:Å^a¢½Á\x0005áäh\x0008 n0\x00088;â(¤\x001e pVpA`\x0014I\x0012îAUÕ¹K²h\\x0011ð¾¢Yþ\x0002Í\x0004}wys~ùi¾É!\x0016\%gd~\x0019\x0016\x0014IÍ+O\x0014\x000c½~}¼w¸»÷zº)BOX¢Ä\x0012
X^SMl*.\x0001êÊ\x001fÄ@UHÔ%K,Ù²Z~¹Z\x000e\x000bU\x0015ËVG\x001cû3\x001cKXªeµ\x000cæ\x0016@77Mx^«1LºdÒ-Lh7C.²ÂwDÅYt*ÎÉ\x0019eJ,Óå¡ÿNÂÒ¹a\x0012ÏI|BÁ²%mÁ\x0012i\x0008 ¤8
Ô>ÃjÒ\x0015íüáX®Är½±ÀåAøÃ;¦\x0002_\x0012.\x001f#\x001c|Iå[\x0016K
\x0003Æ¯É\x0015Úy±Ü\x0008áÀY%JYËjq´ó\x0014D\x0016q­lN¾¯4÷VªJ6ðþÂAB¨Ob
¯PYf	E\¦êòÐÊUÉ\x0007Þ_@Ä³E©Å02Î$Yj+ÿ{+W% x	\x0011¸<
<\x0001.æi½\æ\x001a!!x%!x\x0011!¡¹¸ÅõräÒ\x0008ëÕ/Òª8´«\x0012\x0011¼IFxR7Ã\x0011§c/²ä²fÄ6ê2ËÈ\x0019Ñ*§X0J	J\x001aqìE­Øô×l`ìAJ\x0001\x0008\æu\x0004.ri/ÇpUbB´	.Ñ±Ú¨g´\\x0006yDu\x0019EËeäêf´1TÑÄ\x0004¹L1o|\x0000WuèEË¡\x000f»ÈQHÀ QG§îâÕÕM\x000f¥ÎeÚSsmE=¿¥¨Y±0Àµ;BB¶Ü¶ê'å%6\x0007§\x001f
^\ZáÐ×Ø\x0013\x0012\x0012æ¶A!\x001c7¦\x0018~\x0003\x001eei6\x0014\x000b`^L0ËHâÇ§Ãð\Y;p*\x0015p§·W·FéTi\x001f±}TJ\x001c¦\x0019äWE÷\x0019îôèlÿèlC=q\x0013%h\x0003ML\x001aÌó\x0014&Fµ¡Fp²p&ð\x0019a1ÍX±l\x0017ºaî\x00008]Âé68H9NlÐâ\x001a]#\x000eó~åjg´f4S¢64C
±$mªôÚA\x0019£×tpm³%m3\x001aÃ ±[\x00176µö:îY&GÂ¹\x0012Î5®\ùh\x0014Ã\x0011Á´£ä"+F\x001e8_²ù&6\x001f3L6Ñ.Ï)¦(\x0014i­\x0015r½á
»	\x001ck\9N9¹F¼­v\x0019;nWy-ÛD08TÑ"°\x001a\x0002H/É\x000c®Êð\x0007°U\x00027Jàp	0\x0016í3#$âÜºfË-lüåm\x0002Ø\x001aRÁ\x001d$\x001d*A±FÌo
¿åÚg¿?ªèTãÊåH¨1\x0012K[NBÅòÆ»¬¼z\x001dxãóð7\x001f¹êyàï¤û\x001aoib×¤fÚ:yq\x0000]õ>ð¶\x0007ÂQª¯°\x000eFð¢2gò\x0010bîF®]õ@ðÆ\x0017\x0002Æ)¥ç+ÜWlH.]®=°nì¨\x0008ÞöF8å1!ÑBçtÌs4©Dº:ý¬NTbX´a\x0007¹hÉ¢÷AMÇèÍó¿½TãÖNÔp vPã·F²_ S4¦#¹q°¨\x0004±h\x0013Ä1LÙ²>:Ó^5=\x0013^ût \x0016m8¼Q\x000bí`¬;v$¤YG0¸|$\%E ¶Ð1\x000e\x000fÏ1LKóq@»\x001b\x0007WIbÑ&\x001dÏ^¯\x0019¸Ò \x001eö^U]E\x0006ÐU²N´Éº¿ýùÆ)4N\x0019þs

\x001b¦îgCÊºâãvVVwB¶Ý	\x000bgq8±²\x001cl­\x0016£^1^\x001bÖðm·BäÙ=<[af\x0005#ÛR8«5;Ö¨ÚAw(ê*f±ßªôFÝ\x0007É7ê^@R|¥?µ] Ð°ÐÖA¶\x0013ÃÌf£\x0015bnÔê	mk×¨A\x0005µ	3áÍOí -5ñ\x0011~#õ;\x0011gíÔF\x000füJË	&÷8¶,\x0008\x0017ÙzÒ¡¸\x001cº"fß\x0016çO0\x0008Å¿¾G´+(Á}u¹YCVäãWPó¦!=
:Ü\x0015x¯÷§»\x0011o2{¹¿×\x0007ÏxæçÁcjÕW¬(\x001båbq?Ù½½º½~;¿ih\x00008±±.GsãòTL.Åx¥Z
(½Lvö\x000ev¦/7\x0010Èx¢Ä\x0013Mx13\x0005+È\x0014Wñ
É\x0016yñüjºE+*ñTãê%Ãñô\x001a"`èô9×IÕ(t+)ñÌOçJ<÷³á\x0015^2¸\x001aìg»\x001b¼¾º­w\x001bl\x0000\x0015ù\x0014òÉe®\x001a»~ÕÝåmW2Éqj[às0k(òiAûk~ÈÑhå«./o½½ÂQ;Th6æåJF¼^É~\x001eÀWÝ^Þz}\x0005M«)\x001b¢Lý ¶¬ì{3¯¥ß¼ñ\x0000º\x00104\x0004I\x0017²»´X
®7¯_¥»¤5ºËÏrÝê\x000bìà\x0005NiÌH\x0008åÝ}î\x000fé²>÷
ö\x001c¬jgR\x000e3\x0002B]fwÇ»L'J:ÑH§uÎæõ\x001cï°ôÚæØ»\x001d'K<Ùç(@\x0015»ÍKR®È®äUKã!xªÄSmxNÔB;\x0005÷°ÌÅ	A\x0011[#Æâé\x0012O7®£RàäÕ\x001f>ûG¨ZT
Á3%i\=mh@]¸\x0005Ø7%h\x00079Þ]\x0017¥\x000eÁs%kÄsùy3S¢»3ä\x000eîãðx-W\x001a\x0005a2G5¸¥á­ZðÜÙ´ª,\x001eÂg+>ÛÆ§Y.a\x0004\x001f.F¾!¼¸õ|Ûf>Y>øÇ&@\x0015®\x0007&Ò8ËÈA/-öÎ\x0016Í¼|áé7Þ\x0010o\x0010Ð`-É\x0017ïÆ\x001fA¡W6\x0018\x0010Y¸6~Ù4\x000f\x0008*ê±Õ^-K
(QQi±6¸ñË¦¡@\x0019JP²/TÐ\x0004\x000cyª \x0007äG7B1»ÖGÚ\x000fJPº?ÈáXGu4\x000bòµ\x0006@±ÕíczeÒñ]ìæº±\x000fW\x0014Ó:U`ó(\x0000
°\x0002C­ñüÀxáãØÏõÍ©nzõÕÏU+¢³&TBâ[\x001a\x0012¤0¥h¹Î½×hJDÓ¨-NÑ¶0S\x0003KÄÌ£UTkü£m¼ZDÞ¼\x001aúrã[\x0016þ6õÈ
$y!MÝË~\x0018cµ¼y\x0019ÁFU\x001bg?³¦øfëró\x001a\x0019]ÅèZ\x0019¥r4¡ÔÀóôQÕQ¹.í§
±HÒ\x000eµ" \x00155eò\x0014Mà*«-B®	v´.cm·Å¥,|Î}WÓÚð\x0008©Éi1Í\x0019¶vk¼õPþ@j\x0006þgó-s±×§;¾\x0003CÙá\x001fã\x0004ßù·ûÉâa²s{w±¸Y<nÈ½\x00044l	f ×<V5XIåÆ¯tÂ:\x001cLÿ8ÌN';GÇ/f³³Í	¸|åÑ\x000btz<N^ßÞl\x0010tT,aÓz%7+r?\x0014!\x0005|}tØÝ©1\x0003\x0012Hô\x0005\x0002÷\x0015åèÓ\x0000.ÅtÎheþ\x0007÷U_ Y\x0002É¾@BaÓ$\x000b
é)=_e!ÍÍjMJo U\x0002©¾@`}ë\x0015ûQ1GÉ\x0004&\x000e/\x0019\x0006¤K Ý{,v\x0019+¤iL^ Õb¢¾<¼âá½\x001cÃ¦o\x0016m¡sNÙ½Ü¯V	ô&²\x0015ý	|Eäÿ}"QI"ÑW\x0014	È¥ :\x0018f\x0015È%³
½h²ÌÛ
7?$¶"ÁÈh¬cb b\x0000QÐ,Iôf¨p\x0014¼\x000fÇuÊ>Ö­\ÎSFl,°JÖK\x001cò`nøqZ\x0005\x000b?¼7ØßpªÞ\x0006%)ê\x0008tóv á.vÜ>\x0006e\x0001\x001bGïl\x001eí0\x0007ÛI«(çDSð!è9fí¸£³ 1Ä¶Ñ;\x001bÆeVW±º¬\x001e\«UQ\x0015\x000c\x0007Z'BµÂhVa*ÖÔ3n\x0008,Ãs'%·\¦\x000b[÷*ke.
³¡\x001c´1ã#\x001eßÎÏA\x0015û}~wqÛÝÕÀ\x0010ôÔÇ,ÀRÓ\x000cs+E­Ô°³é.è`¿O_\x001c\x0015\x001dZ;Ñ²W)ÃÍ[è8.` ó\x0018w
t"ÃÉ
p\x001bnõjï\x000c%Jåðqcë7m\x0019¶¨ðÎ³l Ri"4ä[sÏ ûÛV"Y\x0012ÉÞDÉë\x0010q0î 0§(Ð¸\x001fBJ½qT£úâÀ´XD¦aJUú0íæX\o"]\x0012éÞ\x000b\x0004î±¢×4\x0004ê!\x0012ù\x001f*Îû\x0013Èü\x000ckäJ"÷\x0013\x0010Æ²³Â¿ôTÈÌ`éÈ|yysûøµ\×±"?q©dm\x0007.£\x0004Ú®ZÖréåÞáÑÙõçÄV\x0008ÍD7oÂöz8eJK\x0014P\x0006zSÄÓé\x001d\x0019Nw¼\x001cÊ\x0005-??.îû`Ê Ð&á.\x0019tóH
ù³ú©úé¡×\x0011Ú\x0000ÿv6;ÙN\x000c'oEÐÃ·\x0014ôqrÅþíApÏ\x000cjna\x0015õÙ\x0001?\x001e¿8¹â¨{VWf\x0012%h`
æ-öRi-T¤IH­Ìdi %lY)¹üa¡À\x0012OkeT^«1Tª¤R
TBMù\x0016*GH[¨×\x0008ÞTº¤Ò-kÅRïí4[\x0011Û,ûÜ0U+»Æ7Ð\x001bËX¦e±ry\x0017,\x0016®É¡QkeK(Û\x0000¥säXÔ¥3g/º1ÐX®\x0001K9ê&\x0005kåÈÉÊ\x0007kYÞ\x000bXlÜÄyÃ.ògv¹\x0011
ÜÅUo*ÞÔ½ëO0\x0018½·pË\x0014Á¥ ¬»Tì\x001d¼©èMx¢Ä\x0013xNÓìÕ\x0018¢\x001an3Èª9%CðT§ZñLn©È
uðÚÃjSéB
xáY}>T6y\x0019Ä_\jà_¾æ\x001b§OI\x000bCtãkn,Í\x0018VcQ\x0010o_\x0002ÖøÆ©S\x0004¨E	\x0008½(Û\x0000]¸\x000fÞ/	GÖK½\x0001f\x0014!LÑ)\x0008ãPÆ5T1ù\x0004\x0010a\x0000p\x0012+ÁàÅY\x0004FÕÖx\x0003"ôß[¹Â²N¢8_Þ<L\x000e.Ï?,ºgÄ¦Oi\x0014;äì<Ã\
Ê¤àks\x0016N¦{§½ÝW³ýí²\x0004Í\x001c\x00001O \x000f³\x000b[Z¥TfmýT\x001b£.\x0019u;£\x0013hZ¥\x0014EO¤~ÃÊû'´%¤m\x0014ÁtÈå\x000e©«{Ø`GëhùXÆ8z \HøçfLh=áNIã\x0011\x0014·8´"¬¥ZÛÞ¢âìrc-9ß¼ûô]3ª¹DÙ¨¸§æQj}uã®Wê¸óUUOTcr\x001bV\x000e\x0013%\x0004õD\x000fr}m"P/Ô·<Å»íÒÇ\x001a~_Py\x000fç\x0017·=Ç\x001dj
ÃJ°A×Ø*Ár«¨;tí
>½8:ë5ç0.c­PÛT¤+?nð#ðh\x000eÁx\x0019CÁ?²;¬]Íz~¶réK÷ç\x0012NÐüA\x0018\x000cIYz4õGqfFqÙË6pÅ6¨)v\x0013þGãiÀ³ô¬Ê¯h\x0006ó%o\x0001s\x000e¼Qï\x0001Gj!=y¾Îéj\x0005+ÓjmV»Ìè\\x0003\x001eT/.á
uJöõ øV2Y1ÙrÈ`: Â~¾­\x000c°°ß­KVÝN¦V\x000c*Ýöó»
#è¨ß³æh¹´Æ-1Çv3qz¼1 V}\x0000²=¬TØáÐÇ^Ü4_ÈæOks:z\x0000ÉÒo¯K¦ú"Aä8wiÚ\x001eÇ þÐQz;\x0012ó+\x0006]\x0000\x000bã§W~¶¥^ûÖ\x0018ãÄÃ{Û.zVn^¶~úå?ûUYï+ã±\x0017 4í\x0001ã«ª#\x000c\x0001P¬5n[\x0000e	(\x001b\x0001wXz\x001eVPaWT)}ÎGqZ\x0005T% j]A&HÐ\x0002 5ÏrG«*÷¸\x0011pµ\x001b#?Á¦ò-ðX[jáªý§U'c\x0012®Õ¾Lþx\x0012ûÔÂ1J\x0008\x0004äû&Lê£ÕZWA#¥,)8ý\x0016Óò5Éf1åªë_F×ÿ²`~>9_Þ]nL¥\x0014äK3\x0002êOåÜªp`Y.?\x001cL÷ËÉg]t¢¤\x0013t \x0014)ß%¿hÞÒ,ií«³5x[\x0017Oxò§ÃS%úéðt§\x001bñ`
$¦F[n w\x001a:{U\x000bÓ!GÏtæ§[<[âÙF<\x0018¡ù»4­ÃåüÝªÌaÀêñêèñîìêæèêr½êª×e'ÙùíÕæ.\x001cÊÌ Æ^
+¨\x0015ûA\x000f/Æ,<\x0019\x001b_\x000b¾Z\x0000ÄuÙc+ËÝiãt\x0011E×gõHßV,]bé¶Õ²è\x000c
F\x0019õ\x0005gYaQr]Ï¾X¦Ä2
Xç\x001110úÐäÈ:çëÊàûb¹\x0012Ë5`iOå(*¼÷°4\x001d{.~5öÂZUë¸,ÞúÇ	÷áFÞm\x0002³ Ð!)\x0011Î<dÕüp\x001dÏâï;=î\x0014ÉTI¦ÚÈ\x0018U\x0003Á|snYå}mG3%iB32{\x0000MÑ$Ð`ËÊfF¡¹\x0012Í5¡iCIÝf(Ô.C®½e2©\x0014\x001c~á¹óà?¡è	~àN2h¿Æ$¾Éë¯DñjL%]w§¯Qì¿\x0004\x000fð\x00060\x0013Û)Á\x000ct4«YW\x001d¾Á¥,>e%\x001a\x0008Æc^S­\x0014yMÑÝÛgcÒoNÑß	¿ð\x001cþñù¯ùÍdçj~Óí5á.È
ÎäP\x0015¢MFV\x0003\x000e~M\x000f';ûÓÃÝí0¢\x0011ý`À{¡¥8¯Ù%\x001eCý©Ìè>@EB\x000fu'üÂsf\x0012\x001eÜ>^]ÞLþó&¿/6¤À§&;C®\x0017¸éãÖÁÒa®W5.`698:Ûß;L'¿Ï\x000e7ì\x001cçP¼\x000eùéÄ\x0016Þ¸®þúòs\x0010û;0{³;¬\x001eÄ¼Ä÷Þ)\:Ø}R\x000cË¸÷[\x0010ù;0~³{\x0006ý[®b,8\x001b;á\x0017Ã?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ý>\x000eÁ#Þ-U\x0006CÉ%\x000e:°\x0003b£î¡w7Wg\x001fàN¯Þß|üxv-ã\\x000eï¾®XMÍjúXñ5\x0012«M<,R\x0007\x001ei\x0000¬\x0012O.eµ5«ícu25Àj,OÑÒ 
³\x0006³\]ÍêúXC*¬hÇ\x000c±ÒD\x001fDÍëÕ×¨¾\x000fUÙaÍµÊ.²j\x0006RåEªô³\x001c5Ô¨¡\x000fÕ;êáÆ\x0013`¸½Pû(5èu\x000e@¬Qc§Tµ\x001c\x0000\x000b>XªZ\x000e\x0000Êw
ÔT£¦>TÈs\x0000©ªÀ­\x001eÚ[jé\x0002V\x0017Ö\x0011k®Ys\x0017«ÎYX±mF1kGu,&Ù¬VA\x0015ÇórÕÞ\x0017\x00157nnõ:\­N«À¶6«Ïhi4\x0004|^1ioX°Õ\x0000FZ\x0005¶1ZºÓjÁ1\x001dÆa¡Î2äëâí*@u$ÛX-Ýg¶pCÀªa¾&I5]ÇÀêÆhé>«y0C\x000bx\x0000<*H»baAòv\x0015ØÆlé>»¥s\x0013ÁÔQrek0Ìý[\x0003¶1\ºÏrá\x001aÃHVÖÂõrtb\x0016Ó\x0005¸ëØÆté>Û¥±I\x0014\x0000@1,o?\x0003TZ¯´\x001c¶1\x0008ºÓ"`Çá3Ë{àÈRE<\x001eÙ ×`55}J\x0016>ì\x000f¬ÚÓ:<§MQ²&UlõW"2z{n0£\x0019Ïåû:h«%YÉç²»È¶\x001bÙr\x0004zßõµwÅ:ø¼bp/¤ìz\¬\x001fS\¹qi!r)±M¦äz»¿£§Ñ	\x0007NC0ÛOà4d\x0016­÷jÜ­½>ÁÍ\x0007\x001a
*NSsNNte	5óÈLDu\x001aÇmÙ\x001cT[£Ú\x001eT\x0013ØÈì\x0006­J\x0010ÎTqÇ\x001aÿúsP]êº¤
nb4,UÃ3_u°Þ\x0003°\x000eª¯Q}TuÄhvP\x0003Ññ\x0010\x0017\x001dD×z5npç\x001a4ô&h\x0002zV±Þ¦q\x00136\x00075Ö¨±÷¤f)z\x0006Oª\x0011ký¸5jÔÔêhý/~ýÀ£ÆtÈr¥T^GQå\x001a4÷:¬Wwc¢èþWùüULk¶ä3
*~ÿÌÞ\x0000íTÆÏÏ©×¥¨­ê²S^[*\x0002ê\x001d\x001dé\x000c¦V\x001cÃÄÚ*Ýe«@2ÆgRXuÉÂ®c«tc\x0000t\x0005°6n3Rì\x000bñv3\x0010ÖÑVºQ¬ºO³â3
Y+þ6_-£xãqÌ\x001cÔF[é.uåÀðkNÃz%îJL)HfË¯b¯L£\x0005L\x0016p>Ê\x0003S2«G'|ªáÆDü\x001cÖÖ\x000bìºZ.çã,u¦\x0007eìD¬5\x0007R\x001a³,V\x0013\x000c\x000cVKb¹«/àÐ&éÆC+á×«xXFí\x0002Ãaè#öÊâb\x001bÊÄ(Þ»\x00002ö5v\x001d\x0019û]dß+ãÿ\x001eßPïòêN^ÜÀ¡Øí¶[!5\x001c\x000fÖ\x000e>ØJWïÆõÜÚÇa`ÑÝçÛèu^¸]ÊTUJ1ã\x0002Y\x001c±\x00163U0àÜ\x001c0¾¸e\x0012\x0007\x0015_
ö*´©¡M?tâÚ\x0013xÔºYzËÌJ­Èìjf×ÏMy\x0004
C2\x0004­¢@;wài.t¨¡C?4ø
\x0004
ög\x0008â^R9\x001dé@\x00141\x001b:ÕÐi\x00014M6U)+YòÕÌ\x000f%f2×ÏOõ\x0014ÍùÐä¬§\x001bÓ"!;öÖc¶ú@6.r«9úU
CÌ£gmB¢áÊ@MÝ#+Q7ªC÷ë\x000eÌì\x000eÍ@\x0012¿K\x0010¢PÇ¸âñhî×\x001e
ãMr5à\x001fKYGìÎ\x0003Ò\x001aÊCíj¥âÿý_ÿûäaËò*¬\x000b¼\x0000R%ï\x0011-8Û\x0018Ï"ö\x0007PN®Fç±T¦4\x001dàÿxÃ\x001bbÁÿ¡ÊT<px'2ÚÑö0\x0006þêÉãêD\x0013\x000eÑÇCÏ;\x0013!]
é: Áo\x000f\x0005\x0019Ê×[AÆ\x0003gs"¤¯!ý|È %\x0010\x0010=óCuºã\x0001R\x001fª\x0008\x0019jÈ0\x001fÒcdÉGÒÈ¢Äaþ\x001fCÂÅY\x000cjÈÔ\x0001i\x000c-©\x0001Hìk¢3iy\x0007BªÅU­wøÍ¡Ä+MZÞ+	&­åR©\x0008·é8\x0011²Ñ@ºC\x0005ár¾8´¾z`r$ÝHa*cs¹uÇí\x00065HÉY`¼µY4¹ÓË\x0019k£;î
>Å°kí²¡pÀôäc\x0003\x0019äW!ínµ©Uu¸õñËóÃçÛûû©.?æ\x0018@gê\x000c\x0006?x2*ÍÀ|suyvqqÐÛÝS«êHk\x001e/Nó¡w
àÿÓ¾CVÏ\x001a)ª\x0003ög&±«]/±
\x0006ÀÍRÊe\x0015c0\x0011×å®\x001cjäÐìpA\x0012ß±\x0018yñ°Å2dF>ðP78ÕÄ©\x0018gµX&Çe+år\x0000| +3¸2\x0005V5\x0001ÖLd\x0017%eà¨Â)b[óÄýdf³«,L]~±ùó»I÷.[ê×{\x0007\x000b­@2\x0010¸²ã\x0017àß\x001cª2¸8ùþýùØÄè
ÔÖ ¶\x0003\x0014PÅ\x000eÊQ\uª¬zU«púÓ÷pbå,û\x0003i\x0018.3:V½A\x001f.òÊ\x0019kÎØÃiy;\x001eSËÛô¬râðçCI¢Éº= ='\x0014»)[o<Ô\x000bk¼Äë·Ëä^!Ýì¦9O8Íyq+k{qR\x0000²MÊ{Ý¥§\x0005\x0010!O;Á)Büº\x0014¢ÙoÇ.Îde/N
ÀÿxK¼%U»¤ê\x0005éÍÓÃæóOSX\x0013¶Ê\x000cuÊeY¨hl&\x0003­\x001dIÑ7¬oN>^\~="_ýÃ¿eýxËÜ¢¢¾½½ÿùËóæÓ\x001f¿Úöôè¯àG<>þõwßß¶}¾»GH\x0007g3ó8)\x001c¸Jï Á$nÝ¨Ízs}ý£ïÏ@sÞ_\x000cßþÛ³·ïoNN¿Â\x0006ÝÌfJó#ç\x0015¿{\x0006\x0003Ïn\x00033eVÏ`ç\x000bÎYÊ¨àpy#Á%ÞLªc¤Ï»\x0014\x000e\x001c(7_rÚ\x001c3[ä
B\x0010\ÅZa¢ÁUó\x001dr¡:Îa&=Ü²\x0011¹¿
\x000eFÏ\x0016\x001c8\x0007Æe\x0018W\x0016\x000c\x000fÅAå~
40'±\x000bo:ì\x0019òüI*c¨)È\
\x0007\x0007#ÏKÃ\x000b3Tø\x0011p\x001d\x000cLWq¹s=ÿ¦ÂE¤îE \x000b\\x0006ðgGWjÏgCÏ¿\x000e¸¶Lâ\x001c4¾\x000eXòáø:\x0004Ý/º§ÿ\x000cÁýT\x0019\x00070eßnþóËÝàj\x001f&\x000bÃ´#\x00043Ù{*é
Ö{j\x000bwàqQl°\x0003\x0006ÆëÛÿùþ|Ô»Ö?Üþü9¤¼c\x0016Àgy·¹G\x000b{±yzz\x0018Ú?n\x001e\x001fï~þü××¥è±%å+\x001aÑÎ]â\x0001<YÎ©bp`Þ\PãóÇWC\x000bôÇëëó·c¹æ\x0007lMÇÂ\x001f\x0000A¹qå\x0018\x0018¶&Ê\x001d\x000efL-\x001eü	{¸\x001bþ­uYþ\x0001\*nÄ°Ñ\x0018¿@Øú\x0011c&gé'Øjú¥?Aó\x0006B\x001cE)\x0012ü	^NQü»¢ðÃÓí\x0003þ\x000cü_ëü`÷üüßðK°Ú\x0002~IUÿOôKî?ç§/ÿ¾ãMc_Á_~\x0001¯\x001f×\x0004\Ì2:Ó\x0003\x001a]ë@V;y£Ëµ>ÀúþÝ;ðýqaÀE¥íwÇé\x001fvZéé\x000fVúÛ_ðåñèëÍ/\x0013¿\x0007ÉóàVÜ}LÜ1s\x000bÞÈë|úíÙ»!z¹>úúäÝ\x0001K°ÓVÏÜf\x0001wÆ
y:0Fko\x001f L\x0008ìÃÉµÀm
nûÁqK+á\x0006GÝQ§}°ðçÁÃ0ÿn5pW»%àX?/\x0012÷B\x000cgg¡ÀÝ¡\x0013>Û×Ü~	7.Ia{:&^\x0016ÔáCÄªç;ÔÔa	µs\x001cØa«s&aãªböhDÜÅ\x001dkî¸[cC>ù7&YÎ\x0004\x0002ÏCyø\x0011kr§;-÷0H`ÀvR88©#°w\x000b\x0007ÖäÎ5w^"ïéq\x0017åÍO\x0011\x0001Çý¸ãXÌÓÃÍ0±;j	8(?N«`ãSJ|3%w\x0011Üh(ÙEÞZÌ\x0005&3\x0018]Ó´`xÈrÂ]UäÉÔ\x000bl&ÜM-¾»ÉCMÀ òdå°¸Unl¦^b4q\x0000\x0017íiÃÉC7îéVÀWõRtc3õ\x0012££\x001f\,§Ük:,.Ã\x0012V\x0015yc5õ\x0012³i²Ãb
ñxÁ9¸qU7fS/±&8Þ\x0011ã°
<>×4a\x001dúª·³1zå\x0004ëNí@î¹W-Øä$¹\x0011²_ÓtêÆtê%¶\x0013O¶fÛHUPxZ\x0018Ït ¥1\x001f¼±zñtIK®\x0015\x0008+D§¬\x0004zMÖ4¶Ó,±\x000e\x0003\x0007>*XDÞJ¶¢È£Êë\x001còf\x001c&ýA\x0015m¾ýíoûÛ\x0003Eýo7Ï÷÷·\x0013¹w¼}Ã\x0001±$iS(B·¤þöìòì¢ý·'7\x0017\x0017cãù*xSÃðÚä¼â1\x0000¯¼i85ï·5¼]\x0008o\x001co%vØJäÉ&#ûY£^Yò®wËàÑ\x001c\x0019^\x0013EÇ\x0014øl\x000f(\x000ex_Ãû¥ç\x0006DÚ,\x001a\x001dI^\x0007É8C÷µ\x0003>Öðqé\x001f\x001eïèÌ'Zëg^üÝèüºÏ5|^ªm¬¸\x0003 zq\x0007@ÛÈÔñÇÛNmSÚÒÆ©2¤}¿A\x0005ÞªÛ\x0011¨@\x000e~N¢í}Xé7¸]éLólópûéÀ~qûéþöáÓ\x0003-µjz\x0003n\x0008\x001372\x001driÞ\~\x000bè\x0017g§\x0017gW§¯û\x001aÜ/\x0001O¦\x0018X8ª6Ù&y¬Sîà+Ç\ðXÇ%àÁÊ\x0003-\x001aZ®òÈZ\x001c÷¨ô<Æ|ðT§\x0005à\x001e|\x0001Î.Úhh¦DÀ-¦bÒ\x0001Ã:»Êc\x0000wÇè\x0000\x000f\x0017Ì;ë\x000cç1°£Qê¬×<*U\x001e\x0003Éõ\x0012r\x001cE¶^$ßN%û¹£^év6bé\x000fêlðÿ¼¹¿»}öwZªLô\
\x0017ò^aÒhÚ\x001fü]p}¿?¹8?»:äôª¼£\x0005\x0001×ôá¦ ÄkÁð®£ÅEír8FK\x0012&ãúÝ\x0017!_/³½þr÷øøåó ";®Ã6Æú|L1?n\x0018£\x0011Ù9Ö\x0012i¹~~}ýþr\x0002§©9Í|Niâ\x0017+ã4ïr\x0004FÅ±é|
N[sÚ\x000ey&56¸\x001eÆD®k\x000fÎ;\x0000ò4ã99 ®\x0006u=\x0002õÔ0\x0002ß=\x0004yIÓ8g\x0004\x000bñVàô5§ï\x0011¨U\x0006\x0007Ý{\x0016¨Ur@ÃheÔ,ÐXÆ\x000ef%uHÆ;#'K¬\x001dü\x001f\x0018³æpæ3÷pOF/c& ¢be\x001ah\x001b²1,ûòÎï¨&7T\x0004¸ß|º=ºº»¿ß<<!rÁz=\x000cú\x0018ÐfiÉ\x001e\x0007,~Ú{\x0006>\\x001d]_\\}Døò\x001cÈÚ¸\x001dx¸¸[½zCóá¿0ÁOÆPk±ØëÂÕeê	J®gGÃ ý÷üvF55ªéA
¨\x0000,¡w@¤Fl> [gÚÔv	5&.âÁµ£q ûùì&­\x000f(\x0019¨®Fu=¨Y+6\x0004\x0016t)ïO\x0003\x0014@«¬Æ]f¡ú\x001aÕw¡ªÌk;\x0007©Fö\x00014o]Oªº	UÂäYÄ¸\x001fW.É4\x001f'n°|¹b\x001cÏ÷O#6»JÌøz%Ðÿý_ÿûìÓýóãë¬\x001eÌ\x0001okt\x001a«\x0017)T°JÂa\x001f\x000e ^\x001c}s=ÔÖ¤¶\x0014GÁ{zÅ×Ê
)X\x0006NXáJ£\x0015P«0ÌøfútV1ê¢ÇÁ¹O\x000c§¦²mö\x0007ÌítÖö\x0000t\x0000s©»ÆZ\x000b­\x0012³ªt@ÁNg5
«ùGëZæb½?h¶¥O÷
tVb\x000cBR-\x0013øu\x0018\x000cì¾ÃZö¾ê\x000bü¨Â µd;Þà\x001a\x001cÜ§x±9z@GgÀýüô:ªÂlªæèE±T±\KøböiXÜÖMCG'7ð\x001f\x000f\x001c\x0001»«¯ì ¯äéùèô§§c<\x0008ýÍC1¾h\x001eÚ\x0017uËCÓÍÑé×meã§ÍOÇ§Ûò\x0017»ô¦¦7\x000béö"SÚè}²m/Úw@\x0016àÛ\x001aß.\x0015~Û$yº\x0001iÒXïk|¿\x0018?I÷Ò\x0003$o\x0007yïi_\x001ekô¸\x0014=$|2^à¤\x0017G\x001aô^Ï}\x0001~®ñóRü¶[GÁu·Îº×V7ç^/=ø;ý<Ú¾èçÙç7/ÀoÎ½^zð±ãÇI«v\x001f¹´ao}r\x000f¼ÛM¬95Öl3!)
6ÒaÃN¸ÁFY9\x0013®êð_'v5ñHwÊ4b®DÛD%¾\Ç¦6¤¼N\x001cjâf)ÄM³\x0013âªÙa¡Õ\x000f_\x000eÿño?¼hpà\x0006çÓÍÝýýmí¯¨¯è?\x001az]\x000eYâ*\x0008¦\x0014
£\x000fÉmî¢\x0004+\x0017ç¥GÛOOÎ/.ÎÆ\x0006®m\x000c\x0008aj¦\x0005\x001c\­b1è\x0019Á½\x0006·§cJýð|òïGÉÞÝ=m>\x001fâ2Ø;py@ÔÄå\x001d\x000b-;7Îõîüãè\x0014ÑáôÅÊ¯£?h^Q6\x0010/?µy¿\x001d¼\x0004ú4ÑÝ8§lÐIIZ&òR¼²¥ÃG\x0013?'ú*6S³yl*­¸×Ý\x0011\x001b%¡Í¸¸ÍÖlv\x001e+¥\x0011î\x0002y1)Ä(QH¨\x0017ÎÕpn\x0016\Lº|T¸0&ùDkÛ0-/ó5yâJ5fôSpâ¬\x001c9\x0013\x0016\x001e¹\ÃåGÎJ\x0013x4\x001fùSÉË!à[&¹å*ÒÛf¹&\x001e½R?\x001c"sBâf!ø¸áðÇÝ«ä\x0000l÷¾úØ.þ¸ù´Û=v8®pÙo¦c\x0003´\x00072mlxAK?\x001eH¸Up¶³óàÀªò|ÊP7Å¦yz?«áÜl8Ê±»\x000cÑ¨á\x000bk8smtñ\x000c{á|
ççÁé Ú$kIQ&¯$é»3Á\x001a.ÌC#JppaÙ¼zm\x0006pÉ¿¼°³àR
fÁ\x0001\x0015«\x0002¸è¸Ò\x001fÑò3&-Ë5\	Wªk\x0010.±7\x0017U\x0010¸üR\x000fÏãL.ÃÕÜ)tÑKýxÎéL¿sÂæÕ\x000b§i"[¨K#è\x000f*W\x0018Ç
yÆ»¶\x000coW\x0005ÈaYE\x001eÿ÷F®k|!ºaöØ[<\x001f¯¸«\x0008mMhç\x0012\x001c¤¥4[^-_×ºËvÛ9\x00131Õi6"í·#¬Å½sÊ¹ðnO81\x000fQçæ;çÙ\x001f:z(ô[hòJÂ×\x0010fTz\x0018g$UÞâ©Û# =dk%gìb
Ü¦3ãká½Å9RgGW£»ë+\x001cSã8Vu1K\x0018á(\x0013å\x001bÓ?\x0007ÇÖ8vªtt°G\	ïX:bO!t°8®ÆqS¥\x0013Ä1å-\x0002¤Ã\x0019\x0014£I8¾Æñ\x0013q¢"\x0016-Ýg	ój\x001cæh:YBÍ\x0012&²àDGS¢\x0001Å\x0007Ç\x0019[¢Þ\x0013k8\x0011¶¬
8*qmxò\x001fã4(\x0004×j4õàXÚáH.®W\x0011j<¯fÄÇo¨1Jz¥Ì*JñWJE,ºó+éæ\x0000ë'8l_Í}2Ü<;³9\x000b\x001c{Ï°nÎ°x½.cÍ¼T"ÀIñ\¶q\x0007æà4gXO<ÄøÈy:'( >^².ÍÖ~n×T¹ºâáÃæîññ¯\x0007\x000eOâqR.á\x000486VYBV­½Ùµ¢gG\x001fNÎ¯¯ÇÆµTL¦f22u´Ê\x0001!úbÚyá~L²5.¨È\x0013ÏQRÒ6	x\x0005J»\x0005r5.)8On[Â\x0019j\x0014±åó¼@R¡
Ó¡°s-\x0010\x0014/ÓH_¶qOl5\x0015*ÕPi:\x0014\x0018zz\x001bLÉõ\x0008 7Úus£wÝD]W\x001bm5$»Ã©\x0019%õÉH×
(ð(\x001bû¾ ÄS¸qääü`@Åt¦¦3óè\x0002¨\x0007XÅq$êKAÙ\x0019­yt¶¦³3ér\x0019Ùr#¯\x001eNï\x000fâ§Ó¹ÎÍ¤\x000bZr\x000cHG­xÉ\x0019'gNí9r³èBM\x0017fÒAb\x001dÓmc<]ÂÐ2±\x001b/Õxi&Õ=Jè_\x001b¬¼0äü2?SxMºw\x0010`UÔø"C½K©gSF\x0008CdË¥¶\x0011`IÄ2¶ùz×ùÐUÍ¸°ý|÷x\x000fgº"EÑ9ò­ëBÕáT´ööâ|´h­Â³5¥Å%\x001cÅ\x001cØ\x001b±\x0012"6þ\x001cºf\x0004ýA[=E\x001c\x0007\x001aHî\x0008è¼ò°*3J3°WdÛb\x0005úÑÇhàØ5kV·EiÓß¥c©Oð	{\x00018Í*\x001dU±yÛE,¯¿c¨?r²\x0015Ô7C:T\x001d\x001cò£ï6\x000f?\x001da\x00082\x0019_2(i¹\x001cÊøú
_\x001d
NùÑw'W_\x000c)«©LþáOÿaüùWäÂ)Ýø¯ÍÑÍý=üMw·CÍ\x0003\x000cw_\x001eö´\x0006"\x0013LZâô\x0010ÜUÁ®/ºL\x0013R²ü²zõqh4[úæäââä\x001aÿíH}Á\x000e¹zs\x0002ÿA=\x001bâ~ó¼yx\x001a\x0007K¸ß!\x000c\\x000e¸òð!#ÜÌD\ÑëKÚ/NnN®FJ\x000bj.Ss9\\x0010 \x000cF\x0016\x0004¦2e£q4B`®È}p\¾æòs¸p<#\x000bLK\x001bxT¿#x.v	W¨¹Â\x001c.Ï\x001dXÀå\x0002gu¢
´[\x0004\x0004f¸H®\x0013,Ö`qÀxÈ·w6%.µ\x0005ÑÄB|Àgg®\x0013,Õ`iæL,1ðDhâ2±ÀÄzvrå+Ïú<\x0012\x0004\x0016=¿ÖÃt"0O{8;Á´jT%1ß#JG\x001bë\x00026á\x000bYHK\x000e¿nØ,-fâ1}J\x001bÙ0\x0003X¤
Q\x0000sËÀ\x001a-¦g©1£¨È4\x0005\x0015,.Ñc4#­¹9d\x0017.\x0003Iü\x0000ÃÜDé¸HfÕ³T,8T¬Å\5«Ø\x0018äkZ·äfêFÇêYJ\x00164«!\x0019|]f=_\x0000\x001f\x0016}ÌFÇêYJ\x0016xÃJ\x0016ÿ,MqÄ\x0002.»He4ºLÏRfØÎN\*°\x0015W<'\x0000c¸Ë4ªÌÌReÞ2\x0017\x000e5$qá[æ²yÉÙ7"3³\x0014ÍÇ/¥ÂêJúÑÊ¥TKÜ1c\x001b0;K`\-ë²\x001d2eùù¸\x0008¬Ñ\x0016f¶ÀÑÙ¤aM\x0018v²§H\x001bJñ	2-ò/JõØÖ[¬G	M°\x0000ì-Â½d}Á­ÝàchZ§9MÛ\x001d¯\x001f¼Nø'üùösI ¼Ý\x001cHRä\x0010Op\9\x0016ù\x000b§¥ÄFj'ß]üÁÛ«ð·³5\x000b©:ËãÛ
®É%:Çt!,s5	\x001b\x00040-J\x0007¸DU²(;µ\x0014Ï×x~\x001e\x001e®\x000fI\x0007¨vI±Ãµj¡\x000e¼PãYx\x0019þ+ÇÜÛD_yÀKTÆ{Ñt·ôê'3þ!kuût÷$/xcb3YÑ"PY0\x0005ù	ýpöñüã'¼ÇÖ<v2O¦\x001c8tC<Y,qÝ<®æq\x0013yp/A a²æþy8MýE\x0008èL/¯üT \x0015·\x0002
\M\x0007çÇ/Ö- Pó©<èE3É=![S\x001cê^XãÄÉ8§¡\x0017í¹ílØ$^´M½@¹\x0006ÊS¬¥ÉFèÛ8\x0006 'ÒáÒ³ù8º½ïS/¼õvô"áIÀòV!2¶È4Df*\x0011Ä\x0014?\x0019.f¢\x001clqc/QsçõäK\x0002u\x000e ãZß\x0008*<	Qè&j.½|ëqÁ\x001e«iíùñ
dÄæ#\x0005Õ{ëusëõäkÇ\x000e\x0012¼\x001bhKï½fº¹÷zòÅÏ¡\x00182%¥\x001fQ(Y\x001a¥z\x0015µN
QHy#Ç@F`E@®÷\x0008Uñ\x001fÖ¡¨©8fÆÂ\x0019Q`3®|²^ æÞ©÷\x001eS1¢\x0019q\x001fCäX2\x0000/"Uêð\x001fTE\x0002o¾\x000cAÍ\x0018à@³	o2öÞsÚ*«}9È³£7ïÏGúqj$W#¹ÉHQQÿ½w1\x0004>ÖÁ'Ån­:\x001e$_#ù©H\x001aLl$}\x001dã¦¯ \x00051è«åAñT¤X#ÅéH\x0001;´\x0005 Ï\x0013@ä»RM&7(Ó\x0012ÁêÓ{I\x0018\x0016þ\x00104\x0006÷\x0010å(O\x0011îäÏf¼\x001cnpeÙ3J)¼ÌþLDª²ëª¥ó\x001a\x0013ÜûH\x0017.ä»{\x0006&\x00139O½yÅÊ¤\x001b&=)Ð+´Ç8\x0002\x0000¢\x0016\x0016<þiØ©HZÒÓõRÊTòàqJ\x001a÷\x0006°ùì!ec»Onô¬4\x0016Pñ³ë\x0008ð<1Ô/÷ 5zIOWLøÄøµ¹¸¶Ñ\x0004'¯Í{ÞC¦2)Lfr
<î:¥Åç %-\x000cL1t\x0014Ý(K=][¦(LÞ).c\x0008ÑÉ»\x0011\Ëù¹©LºÔõ¥öö?\x001d8r^Ó\x0014T·\x0006×¾ÔÓ\x0015&\ÿÈOñAt\x00136Ú·øî/g\x001a}i¦ëKDB'\x001c¬0!©\Ê)R÷3\x001e0Óõ\x0000\x0018:y\x000fKQ\x0003Nve1ÙÜÏÔ\:3ýÒe+\x0007ÜÙÄuÄÀ$ï	QÇn³b\x0003n¦\x001fð\Þ·ÎüX\x000bLÁËÃû\x0012L¶9NvúqÊº¼ÁqR¢\x0008lysßóP5©ùvvú·\x000bFò¸¸¿J2òH¥Ììóô#8îMô
®<Ìïñ\x0015\x0003þoOL1ãø4Rå*óD è¨FX¿ÇÇ\x000cø«)9Ü\x0002hk@;\x001b\x0010»x<»SÇÁÇ\x0018=GT¹\x0015º\x0008]Mèæ\x0013ô.öªyzIb>°\x0018Ñ×~6"xX¬Ð\x0000;1c2ºD\­òèB\x000c5b\x0008\x0006<ÐwN¨sù1¡<cAðá\x0016#Æ\x001a1ÎE\x0004½Oã³Ð=Tò4_G\x001b¾ûC·ý¬ü\x0007/úYG_\x0018 VdW¦`¼0D×|Þ×j\x001eSóì6´ò(CKK	\x0013Ä\x0010\x001f¦å@¶\x0006Úmi\x001d\x0005òQòVYZÞB²^RÖ;\x001eë\x001c\x001eWóìö´ò8O­XLdÙé\x0001g_\x0012Ö^uóg·\x0007o'XÆ0QlY@®ÈGu¯Xóì6áf>q|ºeo\x0007¢
Î
ÇR\x0003©­í\x0005J5Ðn/éø\x001bLÆ%ätt\x0001ªNË½@¹\x0006Úí(\x001dP7*g\x000eÊ\x0001(\x0005)«UÉt\x0002ÕuùF\x0014})CÃñ\x0018óù©h¡ÐMÔjÅ©j\x0011K\x001bÉ¤8¥ð©<$N
Éø^ F-ê©zqXVÊ)\\x000fg.§(ö\x0012ùh·\x0017x4aÚ\x0016\x0019\x0005&²!\x0017\x0019Í×Dv·ÝJößþëèíóo{%§¶åÏôÕð¹\/ã_8ð`\§\x0000Ù\x001aÈN\x0006rÛhÐGy~\x001dæõq4è_D^\x0013|
ä'\x0003ÉÀ#\x0004Rô
\x0003ÿOÊ=£É½<¡æ	SyÌùÀpYCPRL\x001céýb±\x0006\x0005¤=\x0016\x001aÑ\x0011R]\x0010P\x0016Ýh^Æ[\x0013R
&K(:1¯\x0010)ó\x000càÉ\x0005èÅÇ4 JWÛm
ø\x0014¢´
Ý\x0013ÎI ¢TÌG§ts¦õC­½ÔÊgóðyA
Ò;n~\,\x001eZ²ø¤äi\x0011þòÅÐD¢æ\x000céÉ\x0008d6<ÇH$ª:Ì>CÚì(j=¬£=ÿå×Íã#mxøíoþzð®%ñÔ¼ÓRé\x0010¸ð74r:÷áäúE\´n×t¦¦33é\x0013câñ!ßÐ¤÷(éhÁÙ\x001aÎÎ\x0003\x0005ISAü0ù"óKÑöYf§¼o>¯éüLº\x0018¤<ÃÆrÐ\x0010ò@TX(»XÓÅt\x0010ñòõô&Êõôº\x0018å¶©l>\®áòL8­¥
ÀãK)}X\x001cÚ%p!uÒÙ¸s'l\x00194ùîËçÇÛ»?ß>?\x001c]Ü>>?\x001c¥hÞáÃ	W$ZÍÚ¶\x000cÓ®tÉ»÷×gço/Ïn®.Î®o®^§t5¥ë ÄÅl5¼V$_¾±±/ÒË\x0013)­ùáY«ßüõ_Õ;ûöùîÒ¹ð\x0019ÀúíÿýÝO·¿»ÿNî\x001e?ß"ñ1dZ\x00114NSÇûa=8\x000c#\x001cEù\x0007ê5>9¿¾<þÙ·7ç×£ÙÝ\x0016Æ&Ï¼p5h¯<õ·\x0000SBÓ*tð\x0001l\x0007OT9\x000c¢Ã\x0001{è4y@g¹¥w!\x001d9×Ag\x000cåù\x001eÚöèËbY\x0001Ñ©Ä}\x000béà'ú\x000e:ìö²D\x0007\x0006×1]$ç\x0016è<OÕ[H\x0007þVè \x001eQ K3ËÊ\x000c\x000e.È\x001atpxcÏåWb ³<Ç\x0016eGâÎñÕB:8\x001e©O¡dÍwVQ\x0012nÐ(Yîì*\x001f\x0016Yî\x0011£å\x000b8V!Sµ&ª#Atvc\x0011\x000cþk¾ì4ùR Q"O\x0015\x0005Ù\x0019+²¼Çp!\x001e\x001e[\x000175&V)\x0016ÿr^\x000eE¥¨U¤\x0007B÷X\x000bp\x0007Äá1¶eÚð­\x0005®¡ñðré\x001es\x0005ð$<E­W¨RÈNç5T
\x001e_Ýc-À5	$:\&oHtæ{èYC¥` ­{¬\x0005ö\x001eìLN4\x0004\x0017D\x001f¯¢ð°vH÷X\x000b\x001bäÜY\x0008<Ó¥$·v
6°\x0013ºÇVó%§i|$JÎÂSk8PXº£{Ô±.\x001eÁ­DNì¬\
µ:Æ<éÑw:)3¶"\x001eÑ¹Ý*tpvM>ÑÞNNÓ>a Ã¥ki°\x0015ðà¾;«\x001d
L\x0001<ð¡\x001cß
O¥>Ã¤<³\x0006\x001e_Óu1,M\x0017\x0007<\x0003ê½H/®b,@\x0002_®¡©Ñ\x0005ñ\x000c\x0005ßçN¯a-Ð°]\x0017C
7À9K5\x0008GJÃPµUè0,ë¹\x0018\x0007iaÇ\x0014¯«µ¸pNçÝ\x001aJ\x000f£í¹\x00188xµ\x00012öA]Q+Î¯â!Û¡Q\x001c\x0002[ü_óý\x0001K)°i)S\x0001\x001aºzQbìÖ0k\x0000ùtûø¿æCbx#×,
Å\x001f5¹\x001bòÇORæç*³yÓ?n\x001eîo\x001f1övóLsã\x000fC\x0006\x001d(\x000c^,H0É\x0010 µ{¾4&N¿=¹º8»Æ?~{r3>B¾ÁÜ®¦êÁÄÍÙ\x0004ÓÛ	Ô*Ë¹\x000cëí;ÓJ	nTÍÚ\x0007WDa	&Kde\x001cÝ:¨}éEM}þ¨\x001c½\x0002Tµd9pEý¨éª|\x0011.-\x0019\x0006Ô¡XåÆÛàÖd¥ÄL/kæQY@m\x000cÇ\x0003ÁZÅ^­Í{\nTÊÒt\x0000Cñ\x0008pu1^¬Ä¡Ý\x001b3w³RÎ¦ÕËÆI¹ó°-±z\x001aô\x0018½3ûôi7+¥pº¢V<\x0002	E<°í\x0011\x0008+²JB§W°Û\lÄGOG°«³ûrbÝ¬ÝéeÅÍîÌê\x0002mÀ»9\x0015àôFKr=½°6RM:Ü3ðI5Ã&I\x000c¸¸æíÌO÷õ²ô\x0016	ÅV6¶±<ä:\x000ec\x001aVå\K÷U\x0012ÄÄ\x0015ëxd-».Î­z¿8½Ñ
i\x001f\x001e\x001c\x0003ìèfÉFyÅraÍSÀÉ\x0005G6âJ8ÏÉ
rd÷%\x0002{a%õÑ\x000b;.Õz\K0°æ(\x0006!=Ar7+'BzY±Qä\x001d
ò\x0001§Ee>±^«Å\x000eÌüdýõ*(¸Ø`¸òùççÛ§§×\x0019\x001dÎ¡[\x0005÷+Ñ¨&k·)êdý[e÷7çooÎ>~Ü»Ø¥\x0001£0`.ÎØÂ>EÅZßFÙ¦¬÷8Õ-Ø\x0004¡3ÝÁ¦Sh°¨Ü\x0012dc+º
\ç`&écúNiªÞ°6D\x001al\x0011\x0003x8{bäy\ä&Ï\x0016ØÐ5\x0008,%\x000eÞA`rms\x0005Fæl0O\x0015\x0000\x0013[@\x0000£¥~(±}z\x0016xj³ÉìÐ[2ÑÒ\x0015\x0004£R\x0012\x0000Ó+ÜKÊÇ!\x001f3\x0017/$ª\x0005Å+ \x000e¸\x000c\x0012å\x0014ö(â	|e$
6§?lÇwOz¾½¿û|{ôõó¿~\x0019ª\^IÉd_ÊIâB:Ði9HjÐì{\x000eA%üÝÉéïoÎ.Î/qäà7ï\x000fÔ¼ì,ªefÓÏ\x001cÌ1¹e:Ò2]\x001b«7\x0010§\x001cFìq\x0007±­m?1\x0018\x00199¿£$øqY\x0011S×Áìjf×Ïx$,0û\x0012W(kø= %7\x0012´w0ûÙ÷3çH3^PÎ<\x000f]£G|à\x000eäP#^äU{¼ ä\x0005)¹iß«F'q¬ã\x0002!§ã\x0014Êýs\x0014É+¯m¹#ù¼\x000eæT3§\x0005o\x000e4¯\x0005O2
DÇvõdkÞ¼àTpë, À¯]AöÁ
í¿k!\x000bÈ\x000fÍÎß®sáX-c±6|÷ÇrQ\x001dÈ­ñë¶~\x0001ëy\x001dÅv8Ê^ÛJYô²ÞWFÑ	ÝX?½ÀüÑËû h0&T\x0013Y\x0004­WÓËº±ºÛ\x0000\x0002\x0015=\x0018ï8Kcéß\x000eâÆúé\x0005æ/&v}!\x000cÕâe\x0018Ã^F¯°\x001ascýt·ù\x0003\x001dìä!\x0015ÛÇ\x0002ifÍC Ðì{înìî6àÍ)ê	¿k"x{LÄ=É«©fÝ?Ýmÿà\x0010X¬U\x001b¤lÕViH%B
z5Y7öO/0ÖàêAÊ6Ñ
ÄÑ"èÖ»
Ô\x000b ®åã\x000c±(:\x001e©­n5íl\x001a+h\x0016XÁÿ>AÆ\x000c\x0005A`ÎÔ\x000b\x001f\x0018\x0017ËÞ7"h£ÖnÀ\x0005fð¿QÐ\x00194\x000bÌ öµÓÊçâ:GgÄª%é; \x001b«b\x0016\x0004U77 ¶Ô>¦0)\Ñ³36\x000b\x0014\x0008ÿ8HA'³ö`\x0004øHÇ\x0010×;\x001eÂ3Ý
\x000f \x0015g´*ÄZÎFð«\x0011ÛFsØ%é##
¶oaâR¸kx\x001c©^&IÐnÓ½úío¿>ÿx÷§çI/ü\x0016g\x0011Q8èËäb\x000b#V\x0006ê\}¸ysqþûÑÝÛ\x0015±©M7ñPQÈµ\x0005Ø)»-.\x001cñæ\x0013ÛØöË8Zê\x001aÆ`Pú6ÉF\þÑ§ÓùÈ®FvýBvZ¡\x0002qzçãÚ/÷5õ\x0011ûØ÷\x000bÙr:\x0015
VW\x000cBæ\x000cÃ´Ó\x0011Gt>r¨C¿­¦\x0005X d|ôà»\x0017¹QËe;fµç#Ç\x001a9öK\x0019·4r|¢¥K%\x0018å%Y\x000b8ÕÀ©_ÆFã66Jé+~{\x0008ÖKPÍØ#ð|ä\#çnäa.ÄpUN

÷\x0010¸bûÆÒã³«lWjæ+Ï²ÊRo¡ÁA2\ÂàT\x0005«Õôn
_¿å\x0003cÏ~¾ÊøâNÌw
Õj'C7¦O/°}p¹î_\x0007m?\x000e:ÉÅ&ó\x001bã§û­r
^Uvê\x0012¡ZK"4¤¼Úinlî7~8çÛ4\x000cñä=ÕAÌ½S¤\x001bë§ûÍ\x001f\x001cVn6W\x0019T\x001e\x0017é©¬ùd¿¡\x001bó§ûí\x001fúÒ\x0000'CIÙvÓ<öv9\x001f¹1ºÛþyÔ\x0014Tÿ¤pß\x0016w/g³ZÍbëÆ\x0000ê~\x000bÞ'DêÒ\x001d\x0015çâ\x0018½iÏGn\x000c î¶>[Ï\x0015§ e}ÌÏðAî_Pc9ÅÙÈ¦±¦ß\x0002ê ¤åD+ÅM÷ÁD'ïÖ®¥çLc\x0001M·\x0005ô¹TIÂ±52( ;³\x001f}\x000bÏÜ\x0006ý\x0016PãöT\x0012]ü|iTItÅbÉùÈ91\x000bÌÒØ'Å\x000c©ÕY¨bXOÌj6ýªyX
ÁbÆ¡Ô\x0014MiÞ\x001a\x000cÌ{'\ô17Îô+:\x0008ðØl+|Wìj tÙ­Æl\x001bµaûÕrR\x001d¨°Çó#ÎÅ	\x001dk\x0007ÏÜ\AÛ\x0005\x0015¨dÍñ/\x001eJ\x0001Å\x0001¨k!7WÐö_A¬+!­\x0001\x001eQ¤uGXW\x0012ù8ã\Ûµ+h»¯ ÏÙvÎªx¡àM}\Ë=²Í\x0015´ÝWpx'¦¶i@DNÝvn-b×\@×}\x0001ñ¤¸\x001a8!m`¶r2ìj¾k. ë¾à\x001eÉË6üÊì³øúz_k\x0017slâ¸ =§\x0012­\x0018¡¤Äw\x00133ÖLøùÓæ§ÍãÓÃ¢,Þf\x0015Ëé\x000erLÊ3\x0015é\x0004rÄ|ç}\x001dÏYº¡¡¸ÉÔá\x001fô§ä=Âq9k0ºÇ\x0015ÏÉ\x000br¿\x0008]E®Ø9.nöqyÝgÚ=.à7-8/;®É/]§Õrçq\x0017=.:é*H+DÌ4\x000c\x0013\x001dÕ\ÈÇJ:\x0002ò]r½\x0004Ý£#Y{é¡¸ÜH`®õjNÚE\x0007ÿoÉyñVR
9Øc\x000eJiVËOKÞ}2ÌåÉðzóüøë7Þm\x001e>ýqóù§»ÇI\x00192-5\x0012\x0006¹pk¸4\x001aKQ_Ü\_ã>w'W§ß\~}~=\x0001ÜÔàf	8ü'epJ\x001e¢_z=ÜN\x0014²#i²>r[ÛE"\x000fA\x0006p@ëcp\x0016·2û-ÜÍ>pW»E"×YÊÐ­VRÓm}\x0014±\x0007Û>r_ûE"·±L³©ÈS×\x001e\x000eÍkØ\x0007\x001ejð°ìz\x001a>)^¨­±£ÊNôaÇ\x001a;.Â6V\x0006¥Yg¥bÓ2\x001aÒ¯{RRM\x0016§(ÏåÖI)VËT\x000feÇÒR}ä¹&ÏÈuyë°®\x0014}\x001bÍ\x0016ÈÜDÆ]äÕcÞ¾8v¢Ç(\x001dé\x0016×1hNl\x0017#äÆÊ*úÐ[ó¹È~b\x0019Hd©{Ëq²æeQ@\x001eÔªäýÔ\x000c(>ÔóÄ\x001ag\x0005Ý=Úô¡7\x0006T/² *ÉÛ
\x0008=KéZôy\x0018k´ïCoL¨^dC±4K4#î?a©k'ú%Er}è
Õ(n\x001a7Õ4bN\x0017ú"õ±ÒÃ>òÆêEV\x0014/©;©Ú\x0002Ï·QV#¯À}ä\x001dÕ\x000c)Ój>é!Ó\x0012e,mà\x0010\x0014ÐÇR\x0016}è!Õ,©J[ý\x0012\x0015ßP§\x000b÷qnÌ¨^dGb`ö\x0000¢ù
`Få´¤±<b\x0017ºiì¨YdGñJ0·m¡ÒÞ¸¾æ\x00155\x001d5Ëì¨62¦\x0013\x0007ý\x0019é\x000cÔbò¾1ýèm ºÈbØÏ\x0003Pq¹ã\x0003cÊHåÑf×>ôÆ%Ôçh¤IÉ)É?c¦\x000cViMõb\x001aCj\x0016\x0019R%béÀÈ[¬*!×Té¦1£f\x0019\x001d\x0012\lFv<
»\x001fùj=V¨ÝÞØQ³Ì\x001aW<\x0000|Ó\x0016±í4Î±´b\x001fzcHÍ\x0012Cê\x0013XO\x0019iï²L)Æus,u\x0017×tÔMcHÍ2C*\x000bpðj\x001e
\x0012\x0006§/éª.£il©YbK±ì¤Â÷R|\x0000ÊVÀu\x001cë©ïB·-µKl©Ï¹ÌzwZIo¯Ó¢\x0019µYó¨ÛÆÚ%¦Ô'\x0008ìÈÁ\x0005\x0014Lû$Ý²^UiÛXR»Ä\x000eÝM|q:ð$#8ÿ²+\x0006§_¬Þæt\x0017YR,»²|\bET\x0012ý2ZÐÞXR»Ä\x000eÍNÖuÆod:°6«FÓ¶±¥v-9Ãëãj\x0010\x001fË
U³¶±¤v%õÙÊ %í¬áWQC\x0016'ÀUeÞ#»Ä\x001cù¬ËÜp\$æÙ±<ï\x001f,©]ÓqNwtzJ\x00079
RnLpÓ~l¶p\x001fz£\x001aÝ"ÕBÎ3Wr\x0018à¿¿«G»óûÐÛW£EúexÆå #J\x0005\x0000üé\x0016}¬;¸\x000f½¹¦nÑ5Åiâ¿ÄT¤nuìðZ\x0011½¹¦nÑ5MJFf:P¼(}zyU÷Å7Ô/º¤¨Óy\x0019WV\x0016vÄXâ£Ñ9L}èÍ%õ.é°ÑaOÝË¶íè]WêÍ%õ.)nbýâ±w\x0018H"À8³ªzQ?|ÚQë\x0016å½\µÔ OõÂ2[­zICS E:F
¤zÇxlÙïM\x0007Uø¤ËcSyz¥ÿÓôúg¾okvHÛHÍNçÑ\x0007ûÄ[\x0016½5²*r¦7flÐxg=Æî\x000fpËø±gW¼\x001au\&`ËM;ÖJØ{znwNÏí?Ëé1j÷î\x001aµìî\x0002gd;øÁIoy\x0014Ë+\x001fÿ\x001fà\x0017þ\x0000+\x0016ÄÞ\x001a\x000e ´8óF¯\x000fgçÇ³óã?ËÙqáÅÅ
\x000b5OÂµ\x0001"zi\x000c?ÌÑ«\x0016øô7;ÒßüãKßª\x001fÚG«°äñäþþööèëÛç§ÇOäjÍw·Ï\x000fO\x0014Ãú\x0012ÃjÍU\x0010ÃÆhÚ×ãwrqqÕ7\x001f¯O¿åªÍwg7W\x001f¿Àoj~³\x001f;¹8­s)5%Ûdö=ô-â·5¿],{\x001cåµ/H2ÛR¼÷UV/âw5¿[,ÿ(\x0003¯lÎÇ.°üeyÞ;q`\x0011¿¯ùýbù\x001b9?6\x0018¾º8z¬-í(¼?Ôüa±üC)\x0018I²­Ù8áß÷l¹\x0008?Öøq±øUÙëM»ã\x0008?oË#×V?©æOÅï¶ELAöCg³=>ûÒ"øsÍWPòv\x000c\x001e3ïñ\x0005õYJ°WÖU±$Z/µßòæ9k­d½ó¶.Øí+}_ÄßZßÅæWñ¾XkDw
ÔûJ&\x0017Ñ7¶W/7¾FÆÑb\x0019¼\x0018_]^ÁÍ¾\x0004ø¢\x001fÐ\x0018_½Øúbw\x0010/G2D\x0010¾ÀÿÇÜ»%×#	Ú[9\x001bh\x001aÜq·ÿ)1j£¤\x001cêbÓóRÆR²+9¿Rª¦¤êé~êmôëÿ4µÚI¯ä\x0007ÜqÃÃ\x0000"ª-ÇlfªX·ïx\x0000~_4wªÄ8ìÙô\x0003\x001aë\x000bÛÍoÑÔû!?\x0000léýÛ¬ºé\x00074æ\x00176Û_U\x0010Ðè;#öKf²ù¹Ã&þÆüÂVû\x001bÓãd©²/öºUó\x000f\x0008s#l7ýÆ\x0000Ãf\x000b4(ÁFm.ä
\x0001é³\x000fAø\x001b\x0003\x000c[-p¥¡vcü\x0000iÂnnÅ¦\x001fÐX`ØnË{ù´î\x0011Dys]P[~\x000066\x0018·Úà\x0010]Ùî\x000c¡\a%\x000bfÌ\Òm\x0013\x001bAnµbsæW9LV\x000csÎFNÖ;\x001b\x0001l\x0000n5\x0002A\x0005Yþ¢I\x0017._øçV%mâot(nÕ¡>`\x0019Ì	¾¼sÙrõ\êmÛ
h2Xù\x0016Ð_¶}\x0007ÚÎÉ¶,¯\x0014Ï5^Ä2)¬ÙYdqóï ¿lû\x001d6ÊrTÚ=ªøBØ2^r®\x001dfìg¸Ó.^w\x001cüûpw\x001f½ýtøñËÇ_W¤á´ÊFçS\Æi8%[]µYJá>O)¸«g?]^\x001f~|óì§§±&ÆabSj\x0019\0e¼\x000fJm]º\x0005K\x0013îºuM¬iI"Ë8\x001aÙò«íÉn©´ØÔÄffº\x0006&\x000e²\\x0005i\x0005Ðû\x0001Û\x001aØ\x000e\x0002Ûè¬¤¤|²GÜ2ªTÙO½ôtÞ\x000fìj`7\x000cÄÊóh½*¢Êj!öó0»}Mìµ¿À£%ké¤ü)Éx·C\x0011jâ0LìQZ+|:Ð<¼LP[°¦5q\x001c&\x0006¸àk\x0017q\x0012|9\x0014Öíu(ª«Fþö\x0013'°(\x001bÌËÆPöÏ-\\x001d\x0003níÝ¨Á²Ö²#\x000f7¡ôEQÆKEYýÈÁQ7Íyâ.a:Ç°s¶(·Å¡eÝÄÁQg.s mºKR´ôK¿´\x0017rcñ`ÔäQúD\x001eõH½\x0001guM9Êaq87rcó`ØèÑpNCXô¥ô$Hõ\x0000ÒCüNÈÕa³\x0017b©6ñe|	©=9ËåyýÈ\x0011q+NrÅ\x0017l\x0016)ëÅm\x001eÝÈØ(e\x001cVÊ]à\x0007Fç½Dç\x00114\x001dYª\x000fïGnúa\x001dGc\x0002¹\x001cÀ9Í3 )ÑÆuTZï¦ä°Ñ\x00188¬1b¬S\x0010Ë·oZÛÓr/âæöáøí£5,dzøçdjõò@ånäæöáðí£éÚ¼W.E~´V'ç\x0007d\x000b8Åé½Èº¹}züöKÄ\x0001ª\x0002Éí%dQËaqüe7rsûôøíÓåö¥\x0013,é°d¯EÊ\x001e÷º}º¹}züöai$±~Ú\x0016Ì\x0019H©=Û/
 ë§Ç¯_ºsKE\x001dÊÃqPF¤¼_®E7×O_?@\x0019g@Ýy5M,\x000fMÈ[zMsýÌðõó¡\x000c½H
¦*OÈ\x000e¥\x0016ï\x000bhR¢S> L\x0000ìOº ¦~¨ìh8µsÒ%H¸ºÔè2×:åÖãÜÔëÇóQ¼r\x0008§J¦hî! \x001aN3P2?ÜQ~öÓoOË×P\x00137{EV\x0012{Y*<¥Å?\QFöúÍ»§\x0011±FÄnDHàh:x4Q\x0005}Ét,\x0005!\x001dºfÔýb¤w`çÒQ\x0012\x0018]à÷Ê\x0018/äÚ:\x0018MÍhúåÂ!Ö´\x000e
MÝ¾u
;­VXw0ÚÑv3ÒÜ	£×%âzf4jiL}\x0007£«\x0019]¿\x001c)b\x0015çEûëD¾\x0019Ñ×¾_¾Ló"ÍÏó
¾g\x0005d\x0016Çìv01ô_%R<³Ãy]2§¸T¨Ý\x0018kÄØ^KI@°^&è\x0018-Úú¸·2V9G8æ\x001c{äH# \x0002Ï¸ó¥p0ið\x0005[ÓÁØ\x001a~+¬¿Cðec\x0015ßÃÎ¾Êv\x001266\x0006ú\x000cÙA#¡väAÃ^êî\x0015Ü.ÄÆÄ@¿¨¤<jU4ï7ã\x0005\x00026ÉÍ~\x0013c1§'²¬¾\x001d´Å[Û|©¡QßÐ¯¿Öâ\x000bW¯LN*Ý´_-ÕÁØèF\x0018PÇ ´½ºôg12q))±\x001e\x0012\x001bÍýGGS9ÜÔv3AÐ-]ÍÄÖyì¿ØÚ#;âA9ùØÖK
Í,¥V;\x0010[ý·'\x0011OÉéAvzÊ \x0013³ø`Ô\x0001ÙÜ\x001aì¿5:¹Þ!çÕi\x0004\x0011?&\x001b/\x000f.V--jZ\x000f©\x001bIê\x0001\x0017÷¿!T\x0000lâÄln$Pì
\x0019J\x000f½kjVCÇT©]zsëÑCXÃ\x0010kÒüÊml~ks®\x0014¥\x0011=ñ×)¨\x001eâRTâÁJØít)ÜY\ÚÖ£NQqèûÓDi~\x000fÔ1\x001d·(¡ÛC\x001dÝuMbÖÖ®Ï_¶$5âÍªäp5ZÊ\x001eõ\x0013§b\x001d;©±t'@î£¡°B¼á¥á®\x001d¤ðèR
RCO%¬«<·UÜ\x001e\ì@z\x0007Jî·\x0017\x0001Ø@\x0005É\x001c ýüË\x001bÏ× êÓD>îÝ}=\}üòéîë
÷Ø[É\x0014tµxÉ+F\x0019JC
\x0017nWo\x000fWÏÞ\_½}\x0012kJ\x001c L_Ýû2ÔLÉr\x0010)"\x0003·ä}öPêRÿ^eijJó{e¨)ÃïTu7\½¬üw§-ç¨ä?»ýíþÓ'*2þúÛïî?¯¡2QZE\x001aãÅ\x001elc\x0002½ ]¾zy}=Q¿zóþúåë\x0015ÔXSã85\x0015¥k^\x000e÷r&¤l-\0N3Ð·\x000f\x001fïþ¼H¬kb½ØÝ\x0014ÛË~\x001a³K¿c?9Úl9\x001d%&êäZçfà¤\x0018¬\x000eêÜÚÖÔv¬µã\x0016`EuW<j\{na¦-å\x000b\x000eÁ\x0008µ¯©ý\x0006êäeÉ®t¦yç°)«Õ­^p
G c
\x001d7@'sÁÇ:Dy'wF¦\x0014íw@ Uz\x001b´ÞÔÉ;©½Õ\x0005Ær\x0005¡q#.G°\x001b\x001d\x0002\x001bNQ`ÛÀ;qMiÍ¤	];ÞÆÆãn¤x¼C"·@þùxGÊL2Ké^Rºàã©yê¸îááöþÓB¸p<)Ï]X\x000eÒb\x0019º¥ÊUÞ^ÞÜ\¾¼~\x001a\x000fk<ìÄÓTÜÏ%\x00084à³\x0008J
Ï1,-ó[Í§k>Ý+>£¤Û:E¯9wmË¼¾¥ÒµÕ|¦æ3½ò;nèqª¬i¶!ÜVX'¸ÏÖ|¶W~P\x001a\x000bl(Û\x0003ªó·XC¾ÏÕ|®W~.H´@u~¼ªÖº\x001bË\x0013\x0001WòùÏ÷ÊOé24,\x0004.öt®¬1B¿<sn%_¨ùB¯ü¬$Ã \x000f¶Ö-µ<sv%_¬ùb·~)Ï:6Z)\x001d8¶;¡_^¾µ\x000fZõÜ«é\x0002sÇÂ±\x0004²¹ÀKõ\x0017«\x0001\x001b\x0005\x0008½\x001a\x0016Ü\x0018æs\Öæ¬)÷\x0018W:®äk\x0014\x000côj\x0018Ú4%\x0017`¸VÉ¦ÈU.ðR­Òj¾æ\x0002Cï
¦mu|\x0002Sà$«_¬±&UËëÖZàv`\x001eYáã¼¼ÕÚJÏM\x000e¥Ö$c]ë°¢1§¹<Sry/nûãÝ·o·O\x0003Nk®¤ëÞ\x0018¥|nq'ÊËW?\½{wù4!ÖØMßßsB\K¹\x0017D(¸ð¥×\x0013êP÷\x0013\x001a~¯)µ5\x0010\y°Yzõ\gj<Ó\x0007T¶ÎOÇ\x0006%\x0000C%-/&ý\x001b¶\x0012ÚÐö\x0013êÒ_F#Ö9\x001fFÿµü¸½¬YOèjB×MHX6Ê³1B!\¬ ZOèkBßMâ\x0010^É\x0010\x0002JÅ
qÔ¾0Ô¡_eà¦§NþÊeX«ÑKK¯Ö\x0013Æ0v\x0013¦\x0000ÔF®úq4N!ËP6D[\x0013¶~å*ylÉã\x000eÄ¼âd\x0012"­Ìi	,Í`)ÂßØZn\x0002¼ º¹.	K\x0005ÚâþõAn\x0002&â.ÊhþÌh¥Ôp«¶FcC¿ÊÖ29`±)hÄ;4ai¯ÝzÂF\x001fB¿B4Z.ó4A¿²âaÚî½\x0015±Q7Ð¯o\x0015«B\x0015¥yq£nfùÌKÑW#bs±ÿ6Û22ø@}f\x0013¢Òô\x001fÜ*El½¯~÷KEõFKèØ{P^¦5RÓÐfÓxÚYé«Ý#LKúpR<êx­½ÈÒ.
[X\x0001§¾6\x001e}í»/\x000fºûzxöéî·»Ï\x001fïn¿¯É?\x0018ÉQõ¡üCÙoKÎ\x0017Won^\½=<»¾zuõúÙÕåû§©±¦ÆqjUËÁ\x000cõ`ðC õREôêÔº¦Ö\x001b¨­+Û)¨°\r)
Ò46~7jSS
Ô®ìª4\x000e%ê±6\x0016ê¥Î\x0011j[SÛ
Ô:ÈØ\x0005ã¬ë¤"Ú-\x001a\x0003Ô®¦v\x001b¨9nxr²Õj©[ÙqÒ£Ô¾¦ö\x001b¨!HXÜR)[6±,¿õs\x0013äF©CM\x001d¶\x0010ä7iåÔßBYyçÖ°PÇ:n5·c\x000cLw&mÅ¸ \x001fº\x0010°\x0010¨³\x000fi\x0015HÛDUöP-½_0·qeÄ\x0014w\x0019~Y£A9üÄí\Ùüµ´y}\x0004»±°Å4*U\x001e\x0014¨¥íAò¹j11ÝFØ`\x001b1\x0014ÛHØJ\x001e¹¥Ï%a/¤¡G°\x001bÛ\x0008\x001b#XÂ1H¾ÈØ²î\x000bvT"Ð\x0018GØ`\x001dü'¦Öâ>\x0019£
õÒ£ñ\x0008uc\x001cauD_ZYm
ú8Cl´ìúD½£MÆ:Â\x0006ó¾tpY
\Goh§4áïç?Ac\x001dayDÜcG­qR,#¹Z´K\x001d#Øy
ö1ò^néiëdÏ$âRqè\x000056ö\x00117ØGLÇYª\x0010üÔ\x0003ëMÊ \x0006»ô\x00087ÝHÜb"µ\x0011\x0017ÊÒ¤¢ìøé ¹èämïw!±
\x001e7È¤'Dû\x0005&íË¸\x0014·A\x001f n,$n±XÆÓZ'õTºÌLÿÁ\x001dHc q\x0004-½Y6&Â¤ f}i\x000fù\x0008tc\x001eqy²FÒz+í´TNÈRýë\x0008vc\x001fq}\x0004Zâ-¥\x000624Å9 Gdqôë\x0008vc\x001fq}TÓæ|\x001f±ÜGSJØÜÜ\x0004ûQìÆ@â\x0016\x0003Ió'¥¡X\x001d\x000fì\x001eÒ~Ç°\x0006\x001b\x0003\x001b\x000c$\x001d\x0012+ÚÏIbDëR0ã¦Ë
`ëÆBê
\x0016\x0012¨K:.®óÁ\x0010K\x0019È~)\x0006Ý\x0018H½Á@B!Eû\x0005áXØXæù¥\x0016º\x0011ìÆ@ê
\x0006\x0012`\x0006ÔR0Æ/¸eßRMú\x0008v^Ý`!!gÅsÐ¢.7\x0012Ê¨Uª%Ù
»1zT3ã\x0002"g/xì¼/\x0003»\x0017\x001bmG¨\x001b\x001b©7ØÈÄ*\x001bÝ]#/¤+£ýv<"­Ñ\x001bl
©B\x001d¤U8©b"÷Ô~ÒÖ[6\x0015,°öKÎ+SÃ±\x0008sGjÓh?³EûÑè\x0005\x000b¢©Aú_àIû=ÒF
ZDQ/±(?ÞhDOËGÝ·ßu4Íu4\x001b®£¢	¬¬D¨y±+}Å;¾æ>
÷Q9,ÓÉRäÎ8P½¸]aÈÐ´M"±)»¿weö\x001eí&úÿÖ çd$\x00056#)ÆÞ­}é\x0002R\x001c.y½Å7ö×\x001bxD¿	^ÓÆ"~0Óñ\x0002\x001d×Gw½´Ü`ÈäWËª³Ñ¿\x001d?òT&bùÐhAL\x0019ÎØ%ã£N\x001cT)r¸üøëÔÎu}ûùOîVsó\x0017²!ðØ©¨½ì\x0017sK
4Ï~Z¹®/_¿¸¾:7Ë@V7¨RÝÐ\x000bél°©Oÿ=2ÊB+ËMÞÌmD\x001eâÕ5¯\x001e\x0015/%\yÛ\x0013\x001eßëÏ&<wã\x001a×\x000cwZÑ6uöå³Å+«~q\x001cf7¯­yí¨x\x0013¤ír¥=Ã(+ÇW/=0uóú×ò\x001a'\x0003£P¡\7dÍ¼8·Oq7Ö¼q7é_\x0019!±p:\x0005°TÙË\x000b­6\x001bVgº¡¦á
"`\x0019DºT\x0002×MÛ(\x0007\x0018Ö\x000eZ³ò\x0005o.ÖÒÓaÂRÖ¦\x001b·¹l0|ÛPK\x001d¬.#\x0004¤\x001e×ÅnÕnàæ¶Áðu\x0003+@ËþyÊ¯\x000bðRê´·¹m0|Ý@Ó\x000bFf«jÃo/&,¶Ûö\x0002csÝpøºÑ\x0006C6ÇÞQÁ{Nò$\x0013`iÚa7psãpôÆQÊnæ8#\x000fDºz\x000b1I7osåpôÊA
·eþE8!\x0010ÅßÑKaH¿ÖE|4\x0019ÖíKU¤¢ñ\x0007çh>È~ißPÿÅkb|ù$ø\x00188Î%!My\x000e9Í2\x0004\ªi\x001a\x0010ö	6S\x001cì©H3®Åi\x001dÁÛ] 8Ä\x0000ª\x001a«ÿùöáÃ»»¯ßn\x001fV
Hµe­½\x0017Ò,s\x0013×Ë\x0013Þ^_Þ<?¼»zûîòf\x0005.Ö¸8\x001cÅÐ±T\x0014g, Ë}pu«Gq&Òµ4K<ÓJsZ¬­ïÆ55®\x0019ÆU§ ¢õ(íßò2-\x0012Ý×Ö¼v×9yÕÔÚÓPV(³ÔªÒÍëj^7ÊKKÛùô\x001e\x0014¦»\x0013Þ¥¡OÝ¼¾æõÃ¼±\x001c_2OAK*_é3#ûxCÍ\x001bFy¡¬C¢(\x0005Qê\x0015.µJvóÆ7ò¦\x0003Ø²\x0002\x0001$©þ;i³ª8l\x001aåU^êÕ´*]&Hq´Â¥ù\x001fÝÀ­q\x001b¶n`¥,\x001a£\x0016\x0005\x0019X-
Üè\x0006nÌ\x001bÚ7$£Æ\x001aXYq\x001eTè*X\x001a`ÒÍÛØ7\x00186p4r;\x001fa\x000c¥\x0016Ðx\x0019\x0015£ÛéÆAcá`ÔÄaDÙßLÅç2VÍ"á¥ÖÁnàÆÄÁ¨Ã\x0010d_\x001a:+3xSä)9°\x000en·bMv®ÄÛk-\x0005ÌÙó\x0001ªôÊ¦Yª-ë³\x0013öé°su2ì¼Wc ¯*Ñ ø=Õ\x0004\x0019À\x0002õ\x0014zD½\x0005:ú\x000bÕ¡CÍsÁTé\x000eRgfÊ÷
»Ö=	»\x001a×Ý+l%oZ\x0015Ó\x0004#ö\x001aÎ¬]YÉá$úHÎ¡ÌGýòù/\x000f\x001f×eâ
{nÓàK®èÒ_¬iðåÒ\x000cÉ7¯¿¹yv6 cFS3nFLÖ\x0019xb¤Ó%]Uâe·(Í\x000eFW3º~F\x0016"íg(¸FfC.çê\x0000\x000c5`è\x0007¤4TF$ûË	)\x0019àdèÁy#aÝ¨\x0016/Ö'C^\x001f­<m\x00171²\x0014÷t06×\x0005úï\x000b½×g«¥¼/cU%àL$­åÞ\x000cÙÜ\x0017è¿0\Â\¦©|uaPF¬.ew;\x0010ë\x0002\x0003÷E!¿¨)Ú\x0016!³=âÉÉ4-S]\x000fÙ\\x0019è¿3ÌO.åV´ßu#òB\x0003cô½\x0011Ký\x0006¬ÝHë\x0016ý	Â¸ôÒ×ÃØ\x0016^Le°ëï\x0004Õæ\x000e}É\x001dþ|ûõÛÝ÷§\x0001ÓÅÒ}jërRu\x0006\x0001\x0016?_¾}wõþæi>¬ù°Ïkq+\x000c\x0018\x0019¥ã%è\x0003Ð\x000bff5®ñt/+3`,Y\x001bb\x0011¥ÀRÑÄj>Sónñ\x001dJC)só(Q>\x0017°ÏÖ|¶/pö8Ík½\x0018\x0017lËj>Wó¹N>«JÄf­¢\x0007¹Ï²#½ôn±Ï×|¾¼n,½YÀk-Ìm@»\x0014-¬æ\x000b5_èæó¥2&·óÖ2Ý\x0007ÍVñÅ\x001a/öâQá/=)òðEû¡[*^]ËWyþ­[\x000fè]é*MaKÌ\x0006$X{lQZp\x0010W\x0003¶æ£×~X-=vNêP},
~É£Yo<\x0018u2 \x0012¢v)\x0019¶!´8\x0016%#°íÀ¬Ý\x0005_g\x0000Öcj-\x0005xÆ\x000bÇïwÖÙBK	'1á´®\x0011u\x001fî?~ûòpøéû¾¬ða)c\x0007h\x001d\x000egåQ^=ÒY8\x001f^>{÷ææðÓû\x0017oæÄ\x0013G8Óqä-µxLeº²g\-\x0015Otaê\x001aS`\x0006_f4Ãq¨-\x0017(.=*vqÓ\x000cpÒc¬m×AÌ 	xl¨XÐ]¶æ´C¡ìE·Qê ¥_E/í~èât5§\x001bá\x0004Wº\x000f¼\x0012¯ÛDIi³\x000b§¯9ý\x0010çqÏ|Ð3D\x00191mÂÁ.ÎXsÆ!N{!\x001d±Ff\x0008&qJ7ßãxB«=GÔ§¦¹ Ç=»ÜqlU\x0001KI] ^\x0011Å¤µÊé¶s\x0011Ù\x001f½¹8É§²¹í0tÝ7xJúð\\x0016A6\x0002/\x000eÝè\x0002m'\x000cO[FÉ{Êïó¬{Ùµ`lØÅ\x001cÕNH6Iât\x001aÏ õéÄV\x000fb=a©y¸O¬§¸U}Y\x001f¯U¢¥ìqv¶QÇ!&K#Vñªpg	Ç<ËýÝÃÃÝáÙ÷û»\x0015Ù 2±\x001f\x0003ÈÛ\x000ee\x0011Ê\x000bë÷òêææêðìýÍË«§A±\x0006Å!Ð\Y(O×<¦Ú)©m¥É} º\x0006Õ£ Ò¥`lAy4Ñ-\x0019Ò>RS1RàL?LµÓÜj¢|ûÅÖ«>R[Ú1R'F
ÁÑË2Z,.K]¤®&uC¤É:yé¡ÐÒ²4mNÊ¤j1þì"õ5©\x001f#U\x0012ÛÑørÞòð\x0002ú]D\x001ajÐ0\x0006ê¹M	RètaD¤\x001a¤\x0011a)"é"­Ò"¡Jt¢Z]\x0005Ô/ÍÚÔÈOð¹×.ÔFÂ>Õ²\x0000pê>àv\x0014Ô<Íº\x000fòL]¨1=¥eé_²ò²õ\x00065Fi;Xªï´QM^'4yNmUÊrJ´\x0019ØúRS³Ô\x000bÝy`\x000cO>´%ÅÓ)aS®XÒ\x0005\x001cL£\x000e¾(]¬+\x0012ã0°åQüHCYäñ\x001bL²`K\x0003À:ïÙ#	\x0003PfÊëÒì\x001b¯;õ\x0008]ñ\x0008ÿñîöóá\x001fo¿?üíÿ®Ø÷¨ÐÿbþO¥&Ö¼º|}øÇË÷7g× »SÐ\x0015°3ITR%"Pe\x0012·Yª[ëÂÔ5¦\x001eÃôÒdª©\x000eª\x000c)¶~\x000fy\x001aÔ\x000c¦ÈÕñ³¦µòî¼kÚ%ÛÕ\x0005jkP;\x0004j\x0012
^¦qR\x0007Dy\x001f^PV] ®\x0006uc ±Ì¸\x000fe&h)÷]¾¼¯9ý\x0010§e¬*\x001b\x0004Ò?æ/Ä¥>¹.ÐP!Ð\x0000åm\x000c)/\x0005í¨
\x0003º8cÍ\x0019Ç8uY\x0004¥ò\x0007¼\x0004«\x0008z\x0013Z9¬îè°v&[dK­\x0000¿åA§¼Å½Ä]­M\x001a3J±ªV[\x0019@\x000e¡<ÚâÒæÃ.ÒÆ*ÁY±Ì\x0014Ô®låù\x001b\©.ÒÆ0Áe¢
t¼æÆ&/Á*¯ÍÒt§.ÒÆ2Ái\x0002*yà¯Ðøb2\x0004Rò°ÔõØEÚh|\x0018RùÔ)\x001f\x001d¿9y0E'ËX0.Õ öYûÆ/,¾¸¥½F?H±\x000b­\x00065(\x0013òÓ¯ØESòVJïõ*{'m`Å\x0004DU®×\x001eVSà0Ê\x001bl©ÖIa6k\x0003_Æ0ª¥ý}'÷|Ý /PÉ\x0013oz\x0008Q(¤\x001b¹´§\x0006¾}øx÷ç3´ÿòý¶µ30ÿq\x0019ÃLg÷e? Öe\x000eÓRñ|\x000fòcÞAXm³å\x00035 çÐ\x0015ËÄí¥&Ø'io\x0015´5\x0015ô¢ìí³ûoûkç®À|Ç1E Ç]³~Ö³ïV,í*X3â\x0000#Ä²GNY	Z^\x0004ãÜLþNH]Cê\x0011H| µ$\x0004YP*{!íìõï45¤\x0019¤
ÀêBËhJÙ¯I=`!m
iG ñ\x0002dm QöÙ¹ÅÒ®ftý\x001e)c¹7bÌ·Æ×~\x0004q\x001aÅh%¹\x0003AöCÂõìd\x000c5c\x0018`\x000c^#äÒ(:Z®ÌöÓ\x0018kÄ8ÂLèôýR¡qó.Á]ÖájÑ\x000714tc@e[ÎãÜ\x000b'eki\x0006LòÓþõ,Ê2:9¹ùò¹7Gh,
\x000c\x001aåJÂ.M\x0010F0ûÝ\x001ahL
\x000cØ\x001aGÝNtË9ÑECÎ>ètR6¶\x0006\x0006²N&¬ÐÕáq \x0002\x001bÒÕ	ÙØ\x001a\x001806$J`
\x0014Ax \x0014ñX3ã¢uB6Æ\x0006F¬q\x00052Ý\x001c#ß[6\ìps\x001ak\x0003#æÆ\x0018ydJ_\x0000mpvwo¦lì
\x0018\x001c
RZ\x0012lbl(î÷PçÅ\x0011^è¢Òª§¢Ïí¶{@Ø\x0018\x001d\x001c1:XfÚQ°¼Ê\x001cý¸ùæ`\x001b9ès¥×»¼t$Wü¸P~&é±2yxúÀòÀõË÷Ã¿ýõóßþúpûép}÷ñÓÝÃÇ\x0015®¯Ç\x000bË\x000f3ú¸:ji¿_\x001c\x000cþüýáÅÕë«ËëÃõÕ³ë«gOsë[oã6R³¤{!ØÒ; \x0016ûDf°¢s<}üByü\x001adNTZû,
.½}KÅÅ#¢v5¶Ûm¢¦\x0011füeWR\x0013;rûÛo;"QÆaÄc´\¹K\x0003«ºH¨Ã¶#\x0012Ë;)ºR+\x0011ÊËóâÜÀ\x0001Y×o<XÞxFÁ4æ\x0019pÇ\x0011ýåÝtq?g\x001f¸>-DÐúùÓíÇD~wøt{xu{¿ªhê'eÛ¶çeFþpnz.\x0015ùóõå³«é\x000fW/(Ð§ºZ®\x001ebÕZ6×Ðè@\x0019à=7$eÖÔ´fT²Ç\x001efm©\x000e0ËVFñËÐ6üniÃé©
Ó©}}0æI>Ccªò£\x0004bâÉ\x0015×^IÏÜúé¿ùãí/·_¿=,ó`Í«ytä¢nÚñÉEÝ4\x0016Ïâì¨éé¿úI\x0001Ù\x001aÈ®\x0005¦LM7j´èm\àú]ø\x0019k\x001d«Üj\x0011\x0001æ½H\x000b(Ë\x0012\x0002Y¡\x0016ãÜ®U@Ð|3XÿÑþ\x000eDæ´(Ì´Eaù\x001aþøåó·ÛûÏkªØT(µa¾l¦öQ³J^\x001ab>=^ä»øã×ï._¾>w\x001bÍiiÄz¹÷ÒìBûË
?s\x0016K\x0012¡
aë\x001a[oÁ&§ë\x00120GøÁú¡¥Zò.ì\x0014è¶ÒN i_þå.ý»\x000eo¿ÿûíçÏwçwß¿}ýøëÓÔc³Ù.?\½Näoßÿ¯Ë×¯Im¿÷öÙOOS»ÚSS{nâBsI©qÒ_2»»£\x0017ZÙÓ\x000biËlºtR^Ü~ÿôiÍ¤63ÞÑÂ\x0000YPX¦êêYãxâÖ=§ÐöýõõÕÑ$É?8eÇ}.°ía÷¥°Ã\x0005%ú$\x0005\x0000N9õB\x0001Ò\x0018»®ÙçÛ.v¸p,÷¤\x000b-Ç\±lt3KóÐÆØMÍ>\x0017äö°G%kf©;Uó\x001c2\x0018fZ¡±#»­ÙíV¹-0.*Û îæw¡»\x001a}.Hï\x0012»Ñ7S¯m\x0019·%éâÓ\x0001X\x0007º¯Ñçâô\x001eôäã\x0013S2i%M5MéÝ=Ôìsñz\x0007;µñK·^J.´Ì8µ\x0006jZÆØcÍ\x001e·ßT/íÙI»G\x0019"'r_,(\x001bb¯ò
VÍç\x001bz\x00042^.¹*Vº`©o\x0005¯çÒÁãð­YÝhWiÛì´6îÂÉ~\x0008yÏ7´KwGøÆ®ÂFÃÔu\x0015|HÿÎ\¢-khEÝäUf\x0015AË°wþ8Ú¶¤3{º3Ð&Øh\x0010ËKO\x001e{ùR=gÌ¾·µÑð°QÅ'-(Âc\x0006K
\x0006ÌR4ÆÞhIØ¨&é¼\x000b;\x001a¦tä\x001cù¥>ö!xl4
nÕ4¦ü¢R6Å§&Êft\x0013:oÆàû[ï«-ã\x0006\x0003-\x0011ä9<ª<ñÂÒ8¿^øÓ=6×6þz÷ÛýçÃÍwâ~~ÿíÀxñýþëû¯×é©ýü¯°ú¦ÔAOÇÇzm©æ¹:½®^\x001dnÞO?àå»ÃôO_¼ùöÍË·ùöÉ\x001f£ë\x001f£wû1)\x000cäJ\x0010\x001b§_\x0003Qºg'\x0004nÿ5¦þ5f·_CN\x0004\x0007æ^«Ö¹(CÓ\x0003ü]¾­Ýí×h%¾hË¹Ñ:/ßFÙ¹\x001dÛ«Ûí×@à:8JúÄÈF\x001f×;Í\x001cmþ1¾þ1~¿&C¥!d<c(}\x001a\x0019s¯Ì\/Äö_\x0013ê_\x0013öÔhÒÝ£\x0014ïÆ´^2+\x0010ç¦Ônÿ1±þ1q¿O3\x00158M\x0006"×\x0011¥O\x0003ò¾­ÿ.·¦¸\x0008sC\x0013ÁÊ§Q¬\x0003-ßæïòc°ù1¸µÑ\x0017·CÀ
f@)O1þï¡¡±°ñL.|<®ÈÀ:Mz"ãú÷ÐiÐ\x0018OØÏzÒØN.VPÜÊÎ\x000c\x000bÙv©í¿¦1°õL\x001fGñÄ¢\x0018èI'ã\x0002#ýwù9õýÌ§veAI\x0011<Ö\x0005IªÍ\x0015ºoþ-ñý¬'mDã±WO#ÜÉjÿ]~Ncp`?<\x001bYí\x0015,÷Ák#j@ÍEÜüs°	op¿ø\x0006Êë\x0016zYí~ÌK³\x0015ÍM££q?\x001d
BüükËÝ¬³\ênb«¸Øþs\x001a­ûi5ÚþÌ[Î¼$¥ãefX\x001b\x0017°ýç4\x0000wÔ\x0004ú\x0002y8\x000fM¼e­FóÄòÏñþïázb£	pGM05Ïä#ãÇÒÏ1²Îÿ]4n4ÞQ\x0013(ÉtPYÇÑI»£ÛTÇ~ª@M"ÓÏ¡
<d_:È´E;7»dûÏiTÞO\x0015(WÖñ¡¦¬`þ9EQÏ7ñþ?*\x0008ÍËÉ\x000fÔNA/'×·\VÿË÷Ã«Û/O×Úi0¯¬ï\x000côv2±\x001f×\x0011Ïú×©²þùûÃ«Ë7ÏæYÑÿáþÿýö§ý\x000bç\x0000ÿøööÓ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=<î\x0014@c!,qÔÏÆqÁ`¢\x001fe$;!\x0012HB®.\x0016¯¯\x0016?]]¯NzÐ¾ÿóÓgþ"LÂ\x0001í7»5ÑCxíS>BCdL¥¤¹#=*1Y\x0011½o§ÿþ}ýE&ÓMJlé~»þøx»k4ÍNc;5Ë-ãý+Öûé\x0012ÕÛåáùqï
A/=®Oó\x0007°RçÏ0ÑþûâíãÍýú:¸½\x001dÎ%vK¨¦\x0002\x000fC:»7zæò_ÁàñÅÛóÕéòup{\x0017úÆSb
'3¤@\x0006¢¬\x001e[\x0016òØ !º\x0005§S@U	ª¦à\x0014µÀlpÜ\x001eÛÍ}®\x001eîæèª8ØXPè¸yõêèëÍ·8káûâüæúá>üÅ.£b\x0015Õ8XæPÙZ[xûIÑ|·óóèÝê}\x001cµp±8_½>;
±T¤jIuIª§JKY<\x0014#á¨GK½GJt\x0013ku¨Ìmû`\xÖ5\x000f.ån½8\x0004QøÅòùzL$}¸RQc«Ì×¹Îº¢¶9¸åâ\x0010Äá\x0017!J\x0018ÚE	,¦\x0002® \x0016AE-ÝBäÚ\x001e\x000b?\x0019YÈj:²ÉòZS\x001e1ø\x0012zÙd]ï=\x0019YÈz*²á"ß¯en\x0011Â\x0010j2ìfc&#\x0012ÙL^eoéMËê<\x001d;¶¼1ºC1'#Û\x0012ÙN^e(ä$AÛÜÇtÖ³\x001d\x001a,Ð\x0001î\x001di]Ië¦ÒèÂmlòD7a²DHOraò\x0002û\x0012ÙO^`m I."\x000bO\x001a"v
»^á]Äµì1¼Ê\Q!TìÉÆm×¿ sÛLv"ÆfQ\x000bè+¥îVP~Àu\x001e\x001cQÏÜr#|²\x001f\x0001­DjÈ\x00154ÔCÂk\x000c.s÷p2²l!ËÉ\x0016\x000e\x000e±ûS\x001d\x0003uisçwWÑ`2sËõñÉ¾\x000fª°@\x0014Ö\x0019ÓÅ2gHÅ\x000bîæëã}\x0015¹Õ\x000eb"÷\x000cCåZ!(z¹enù>>Ùù9ci¤*,3îf%e~1ÓÌ[¾Ov~Vñæ$¨£1ìá<ïÌÜò|º\x000b´¹ÚÉÂØ"ê)¶óËm\x000bä} ÄEtu2®èÚÌ»²#SEË	éNÐqHq¥uVt-:wMn'×dæ\x0013\x0014 kæ­Íc¢5É¢\x0013öÅ<hß¥¦;ÁpC¥Î	ªu,/s·zw2rË¡É\x000e\x0005
\x000e)¤ó9¤>·¨î«ìdæG\x0011=
\x0014Ù\x000b\x0019Å`ð_^ç\x00173Ï¢eÅdóì`\x0012\x0002"+J¶IKÍe÷\x0019c2rËÒÉîß,[NN6t\x001ejdî|tô\x0005=´{1£![NN7tP\x0016IùbkÇ
¡áÏ_Ì8Ë¡
·\x0006\x0007 FA\x0007LÁ(\x0003=/N[á¾\x001cî;Oã$£	õ¡ÛF>À¼Xì,[ÖYNµÎÐ:×Y3êæ×27Îú®
Üdæu­³gjj¡\x0011ÙPIÉ\x001a6úåÎ`+ÞSã}\x0019þ\x001fåÖ[\x0010¼I{C«¦aòå<·ly\x00149Õ£H\x0018"¥/sNQÜâÅ»ç[\x0001¿\x001aðK\x001661	\x0019ÃXIÌ&w\x0013½ÜÖhyA9Õ\x000b\'íbPèòÈ2\x001bRtÄ¦2«\x001bTSÝ dÔÇ
óªÎÈ¢Ûù3¸å\x0004ÕT'\x0008¥¤
Oó\x001akiH/çOTË\x0007ª©>Pr&hcxæI°ÇäRêå^!TË\x0005ª©.P²\x0010ác\x000bf\x001c×%á¤X¤î®Lfn?öLvPXo°ÛG1ª>6\x001e\x0000!EúbÌ-\x0017¨¦ºÀp\x0011É	\¯TÞ\x001a:÷Lõ\x000cðÜòj²\x0007äf×YíÉäwVéºâ|[ÞDMö&±ÃA ³\x0001Çê°\x0018u]ºî3ö4æXcT>\x0004ÂßO=gñc¨bÇ\x0002î²\x001có\x000bt?­7ºõÔ¨\x000eTIvSóV0ËtçîQH\x001e!ýô1ÖpQ\x0012üÉÔ Cç\x0005w±ð3õ/<Xª[(;cÅ?n¬øÇÉ+®\x000et^pK\x000b.²ÎáK¦Í7\x0017<\x0004ð\x0017\ÀÔ\x000cÙdÏñ\x001dVª&?óï\x001dt6\x0007]\x0018ìP:®\x0018 ¦Ö¿ÈÇGÙ"\x0010áM	×â\x000eæ\;\x0013a>ÏN	½B2lè,ªÒ9çºX\x001eÆ?Û)KL9\x0005Ó6³0,?È
YY\x0011¿û0_O©JJ5D*a¨"ÉxR¾KöÔ«×c\x0012ÓLÁt,W\x001aIbÌ0ô=\x000b2\x000cÔ\x0017Ö`º\x0012Óí+fY$Àc@=§g$ri4%\x000c¥e\x0019³\x001bÅ×c¶\x000e:tÒ½¡éð65/rDÉºepõ­3Ä§\x001c"¸	ê\x0004\ðiÌ¥Ì¨ÛãYÏÙ:D|Ê)\x0002Nì)9\x0015IÎÖ)âSÑ¿x=ÕfÍ³jÕ<ÜÞ­wVç:A\x001eÓ1y+Òål_WCªsOOÛ*3Õf¥³jU:ÿÅt|³nÇºÑão¿¬¿O«O\x000fw»*\Õ\x000c[\x0011¢	Â×¬8|\x001d?q7ÿüþÃòâ"q®ÎN¶\x0016¸òÍzQ\x001eëE÷\x0016T r
¨jÆËx\x000eõ/¹Ïï°Æuå\x0014P]ê}]ÑÖÝÓÝuÂ¢Ê|´ Xd)ïN{¬ ýÈXû¬\x001fBÉb\x0012\x0017È5ãÃõõÍý.N\x0006C{cÏaøàèÐ¥Ì/&Ú÷ÊÃåñÅáòõêô¢i[\x001f ÍïÂÔNAå,Êi¤ÚvN]*<\x00025R/Êsö0¢\x001eYí²B!bÜà\x001dXÖÓ(K­zenkaE~ÑIë:|°á\x0002DüÌJú ÒX\x001aç$­\x0015²½	ä´] \x0005ö~*îLê¶JR\x0019°v½oÕ\x001bâ¢Ç\x000bþ`ÂVYY\x001a·G©jÈ­ÐVÐº¯k½C¼Û\x0018üôëóúéæ±
¶×Ü\x001dèý$ûèF\x0010\x0003\x0017Ô\x0010b=<?ÝÇ4îV ¨"eÂÔT.iX÷ìüìêrU(JDQ¨,^GÃ!ó[ÈæËw«#«\x0011e(«\x0011Â+^ð\\x0006CýX\x0018IÝôC-¡*	U-!ç\x001eózÁ5q¬F\x0000ZtXÚtK\x001f«\x0011u¨ë\x0011Þ\x0000·\x0016\x0013½á¯é\x0015Q»n¿q5)ùL5\x001fp¡±GC\BOqæÝì5¢-\x0011mý\x0012R/9Ì¯BÁ¿ð×4ÎFÛnãO5¢+\x0011Ý^®¢/\x0011}5¢´\x0007\x0012ãP(WL2³Út#ûZBÞ¶ÚÕfCËGïb)ð R¹àZºWãZÂEäÕ&\x0011¾³E#\x0018Æïï\x0008\x001a\x0004\x0016ç"¶ì
¯68"wQ+\x001e|_ª\x000c®²ÆZðn¦±u yõ\x0016ÂaÓgÞÔ\x001a µ&y\x001f­º÷ázÿ\>5^×ú?èÁAJmPDS6-DºGéc\x0002åSò©vK\x0004Ê÷ [R4kiçû\x0018Q>"\x0002åÇÚµÌ#§fØ¤P\x0006¦\x001b8§TA£2eÇôóâd}ÿåùæúáÓ\x000eL'­PÛY\x0010PÃ¶XzÀ\x0017]qizm»Z,Oß^­^\x001díF\x0015%ªÊólp¨¶ÃÖÇ|Î%\x001f~ÿ®B%ª*\x000cÊãÂÀ,=èFQÊá\x001a*P]êI ð| j¾X\x0011Õ%_\x0000Ô v\x0012¨yæ bî+kz\x0004ÔÁ*T_¢úI¨ÞåÙ?\x0001\x00156qIÊ\x000e/µªÅÓ\x001b~6Õ:\x000eíéL5íRç35\'PÅÚ¶TÓLUXWÓ³¬âµe©ø$SeÃ\x0005×6ËºÊE¶/rþyËPñI
òßÌåUÅ²k5ê_ê\\x0015\x000fÀª&±zk-l¶VÍt&ÙäÄÚ²«|a\x0005Y\x000cÖ?lÝ\x0011ìÅi±iëê³mÝ\x0013t\x001eð2»µå\x0004ø$/\x0000ú\x0001Ê4«;ó^U×buSX\x001d¨ú46\x0000Ç	
CÂ¢/´ª-Å'9,¨\x0010#k\x0015Â\x0015ì[\x0016¢\x0008W^dUEËaI\x000e+¾&R\x0010(I
\x001dHdõ"6@´\x001cä°¢<Í±5
'	CëQu@\x0008\x00051Ûaõ$g\x0005#¨°%ÜöI\x0000³f,ÐË|þ»\x0012Ü\x0015Lç\x0012>\x001b\x0000C³°ÔËÑòVb·cß(\x000c$.#\x00055\x0015Ê-%U¬-o%&y+'E«>\x0017\x0007èùì\x0001^´å«Ä$_\x0005­41ÎÓµZÅæ\x0014$í¾ØNbmy+1É[A¿ 6I\x0003+ÎH"¿¾\x0014kË[iÞÊò\åäc?zZW\x001aV ·ÔÄW±¶üä¯\x001c\x0005cÌê\x001då,$4&ÖánÝ\x001aTÙrWr»jFC\x001d§i¹Ù¶ªnw\x0012kË]ÉIî
¦Ô¡j&4\x001aª¾¥W\x0007@ú"¬-%'ù,/mîü\x0012\x001a"XOÏ Ëý"¨íTÐ4\x0005/8XbÂ\x000c)ªËÜ#ª^&¸-%'¹,¯9	«ÀX'¼´(Y|\x001dÐrYrËr\x000ef*\x001a®$rÏ>\x0019\x00015,\x001dUÅÚrZrÓòádá¤\x0003/ske°­t²}\x0011ã*[NKNsZ^~Cl¡9z9Ñ¦íËì×ÓÖ¿m][NKNrZl\x0006\x0004Ïåã.;ë²UËk©)^K²à`i&\x0017¼\x0003a¿5Ë/b\UËg©I>Ë³Æ¿Æ
xÛi_\x0006µå²Ô\x0014%§ú\x0017é¢PÀ\x0011òêE¢AÕòYjÏÖdIËj)Û\x000eÏBt°^´å²Ô\x0014%¹äÙ\x0004@\x001a\x0003\x0007\x0001<\x0018¿Èjy,5ÉcA b]ö®Ø£xtÕ\x001d8	µå\x0004Ô$'à'\x0019W\x0018¬¹+kå°®E\x0015jË®ªiv\x00152+\x0018µB5\x0005\x000e\x0010u®)4}eÕ-k¥§X+ÉXÖ E±i\x0007hf\x000eï\x0017YWÝ2\x0001z	á¬cO9È±GZåËë°\r\x0015jû
sÊÁÆ«<B.XVKÓÑh\x0016¡ì\x0019j;µu²ô%Ë³%Ã[È\x0006UX(ö2I!Ý:YzÊÉ<øVÌ\x000bØ\x0014Þ\x0007MðÈô ÖÁ2\x000e\x0016z\x0011p\x00122I:îwK&±¶v«´[9¬%Æ\x0001^\x0010«\x0015Ô
¥§/ÂÚÚ­fÒn
ß\x0018¥ÿ#e¨Ï«cÆ)±¾#0­íj&m×\x0013kø|íw¬7Âæ6 ²²Ê*/\x0013_ù¢ ,9Øõ\x0014Åyã	4Ied±\x0002ª-8"RD bmA äjbuSº\x0015æGBû2¶ñÈaãNBþ·Ù/É²¶(ü8)¥\x0013°0ãt)xÕ\x001dþ;íÚÕÙ\x0014bâ
3í°\x001c\x000f6q=³:3/\x0013}\x000b·\x001c¾á´}\x000cýûô|\x0008S;åú§Ãò#b½±)&¨$Mw\x0006¦I&l
ÂUÝRá¢éí!K\x00012åîÀ3²²NLw\x0007gw{'\x001aâ\x001bxÂ±!9)´í":tæÜ°®j]ØÐ±j\x0013
±\x000c6\x0017
Æ£GÎoõÑ{êNV­xÿ½ßÒ5}ói²Õ§¯»zû¹1¤Ø\x000e÷Hl©Ì\x0016ÝíãØÛ\x001fçZ\x001d½ÛÖÚ/7»¾¥+4fÆ" ^nÀ\x0017ïpª\\x0013w«k\x0011e(ë\x0011¡­?\x0005^Zä\x0002a\x001e=4n­Pª08Ul\x0005\x0001DOÝ*¤¾\x000eó\x001bf#ê\x0012Q×#jw\x0010¾¨:·Ø!À\x0004]\x000bìÐµ1zSeB7*\x0013Ï÷Ïß?­wM\x0006]Ý8ÌÞ3\x001aø
ÿ\x0005í\x0003Gåjñþêâhy¹Nt².Ü¦]Ãþü"¬Y·7¾\x0012Npª\x0016$­\x0014p*£g
åúÏÇx8]ÂéJ8ï0Ù\x001fà\x001cìÁHç)/­|OÓG\x001d)ñL-\x001eÃÒ8ÊÔS\x0003.Ñî°ÉJ:[ÒÙ::Îí\x0001Þ9­F!AèoÍ_¶Û9^IçJ:WKÇP1PAkOêCôâ¤ôÜmçK6_É¦8>1¥#µË\x00102Pt«\O'k\x0015^Q\x001f\x000fÖUòIÏlX;k'©Ô,\x0004^37\x001eo[ãJs\x000cþ¾-ÊÑä/hùº\x0003ª*ñD\x000bOTâ\x0019	ß4áå7euvgÝûVíÉh\x0005ªñtÀ\x001fTQ
¶S3Áñ±;~p¤T\x0003Nw\x0004¥Øi*ÄÂà*\x0010Þ­¯\x001fwÝ¬Âí\x000fg8a±\x001dXIÇi¤ééµ%\x0005ªUÀ<Y¾>»Ú*KT9
ÕP[p¸øÚ<\x001c	= öTªJTµ×«jJT3\x0011UÑ`\x0007³+5Õd\x0010ª\x001b
«P]êötUÙF$\x000bUåmÔ/w·ßw\x000fø34yÎ1E=\x000få\x001fª[IÜp¾=9¾Ø\x0016n#¤(!E=¤
d\x00023@2«È\x0007ÏI3\x0011l7ÏV
)KH9e%=/r"º¥Î¼æw«\«!U	©öt%u	©'¬¤#o\x0014 5\x000bK+éH´×ê¡[êxHSB)+Ù|n\x0018Ù
c9÷\x001bVrX£u,¤-!í\x0004Hx² ¥4\x0006Wÿ\x0008©i
4T¹Ít%¤ÛÓ=éKH?\x0001R¨Ü\x001f¨¡ÿ22\x001aê\x000fñÉ3\x00110\x001dL9À(ÕA£æ\x0015ÜfIß#ôQm%\x001cy´ëúãm\x0004QòÜ©×Ú³Fip¾?]·1¯÷Ó3ÊnÚ7ü\x000e*ÌAS\x0018'kÉ³Äd÷\x0015u\x0002ç§6ç§}]ÏmÎ\x0013¼ÏêÒSg\x001d\x0017t\x0017\x0012=}ã9¹Þ\x0008Û É¶ÐÀ|^\x001c}ýóÿ<Ý¬\x0017×@¼Þ\x0015hZ©½*OC\x0010ZPí/ï¾Ýd9Ì«ÅÑ»ååjyµx½\x0008?ws[üçpË[þçpë[Ïá6\ê\x0018ô"O\x001f7ùBÚV\x0006©\x0007^¢\x0010ÙÈv\x00162Ïã¡\x0017+79æ¶±a×:d_"ûYÈ*d{®s\x001d6Ï\x0003¯zô&ï\x000eÞ¶"ÿ\x0011fdóÖÊYñþr´~¼ýr¿¾ßù\x0002#QøHzo±ÝAJasH,\ÊV\x001d-Ïß.Ow#\x0012QT#ÂË¿È,¨C\x0019v4eMYêQ-¢,\x0011e5¢Ñ¹¶Ý	zhZæ/ëUT#ª\x0012QU#Ê<¿Ñ[w Q;*ëÿ)ÖÅV¨KD]\x0008Â1xà\x001dâ¥hIe8q:Ðf/\x0017Ñ¶\x00161ü§¹#À*Êá«¦AØ\x000f5®DtÕ«hun
µ\x001cÜ¥4$\x001aK\x0002ç"ú\x0012ÑW¯bøÐVQ`à*¤´ôO
£\x0011K*gå[Ò\x001e-#on^m»AÇúH\x0006¢B\x000f~}þ*¶Ì"¯¶<\ôéHì]ÌQ\x001b%QÃØ²:¼ÚìpgÂBßÅe´ô0'\x0007\x001fûÇ#¶4¯>ÓÜX*\x000eed\x0012­NxÐ3f°P´¨>.á?¤Lh\x001c+Hõ:Y?ËuÛºª\x0019ÛNýqñq\x0004Cb$Å¬9éYKÛ£\x0016]\x001dµÞ8cDV¼qîSP¦6IÕ\x0014ÒÏ6¤fïHõæÛ±ÎoÇïáJw·ø°þrÿp·\x001dRBí M\x0014\x001aÞåb«	÷tL¿1
p´:Y|X¾==;Ù©JL5\x0001Ói\x0018êL\x0007\x001b¬ÌÆ¾ÛÆ=\x0001Ó¦\x001e3xBÑH×rkUþäý	ÜJLWbº	ÁI2Û¶°ÒÝfen¨ÇY\x0016×\x001c\x0010Uq:[·]\x001bq:×ÁÍ\x0019Jm\¹¡Ý8aþp³¾_¼½}¸ø\x0017\x001d \x001fVËÓÅÛã³Ó³Ý¢\x0004\x0014µa\x0011
vx£ûß»ÒMµ²\x0004\x0001!÷]\x0008÷Deu=0ý\x0017Å\x001a@U\x0002ªê\x0015dT[\x0011\x0008½gZal^ÁÞt@
 .\x0001uí
Â\x000b\x001cõâ;Ò¡4Ý\x0004f-)ñLõ\x0007ÖðtÖÏBÔ>p\x0016Ò]»Z@[\x0002ÚZ@=GØP×½ËêÒö(ØWò¹ÏUß&u*òtuë\x0005ì+Y\x0003èK@_\x000bh-É®Âøw\sP>+({\x001f+\x0000K)c½IÅ'¶0z\x0008fÈSÈM¿+©!lûZG"Âe!·î\x0018\x001c£ \x001c  ëlÂ#áµ\x0004¾2\x0002¤FþÈYñcö.ä-GÂ«=	Èý¡\x001d\x0004Ý\x001fKÈ³ÔGÏhJÂ'áµ®D2¯þpP0¢±Ô!!mÿÍº°e«yµ±ö2û\x0010Ï`\x0008ë`p<Å3s\x001do\x0019C^k
%ç¥±ÁRGçl³sÝh\x0019\x001bQkl$ãÙØhK\x0013#Uù(Ï]BÑ\x000e	«O²/î)\x000cX\x0013 
PïÓ¨"l³\x0006þ¾2ê2\x001e
u¨Y\x0014;/-*Þ®Ï<4m¯aüésòsmü/3&L¿Áàg
×éo£o^P¸*ß\x0004¿®\x001f¯Ãÿ`ýûÎìÁ&V\x0015\x0013D)µC=Ñm²¤4Ä»åùë³ÓÓåíf\x0014%£À\x0008Ex¶i\x0011Ä7·Ü¥zá'`Ê\x0012SNYJKóßT4wK¸,y2P¼^G©JJ5\x0012\x0006\x0008a3£ÑPB\x00159Â\x001eÅ£	ºÄÔ\x00130%£G\x000cTy(CFÝG¶Û¯<Òv
¥Î§Çr¼]\x0005JK=ú\x0016S\x0016³s\x0005-s£i¹¦\x0001MLçf8ÕÌàËõ\x0018V½itiÞß^ßîÀsÒRIõ4ê\x001bÔ\x0004±L\x000e\x001a£÷Ç¯wLT\x0005G(qtä¤\x0017+U®c\x001d\x0008ÍF£É\x0012MV¡é,bé\x0004=\x0018\x0005Ø\x0001óþ\x001aÛ±hªDSu«&)»äÀ\x001e¤w¹ }\x001e.Ñt\x0015Z\x0008 \x001cÖH)\x0001écü *¼\x0007\x001b·FÌÔ-Ís\x001f @\x001e·Îõñ=ÓÉjÈlIf«ÈÂ%\x0014+_n\x000eA\x000e\x000cû&W¡¹\x0012ÍU¡A\x0016\x000e×ÌQí©Ô¹Û\x000eÔ%ó%¯[4OJM0t]d\x0005ï<v}¸Ñr\x000cZHW­.ÕÝl 'µk!&ð¨ÙîGÊ@½íÐM¶c,T\x0016\x0010\x0005Ó´`$È\x0008:³\x0016¬å\x0005x\x001b\x000c/5Ò)EY\x0010ä¾áèQl-7À«ü\x0000¨XS¸$\x0010\x001c/kÔÆ0ØK>­elyµ]ÙHRQúj°Åb,[Ë¨ñ*«\x0006\x00173³\x0011Øò'u\x0019mé([*¢o¿®rîTÊ]5¶C

[f²îcîc\x0015¥Glðï\x0006Tø¦\x0003iÕmwhå-;´Ç\x0018_G5\x0016mãkf\x001b_¾\x0019ërui:üóâäù×ç]ýã>\fÏZE}fÒSA\x0010]>\x001a
µ8¹úÛÕjk£;ß\x000cà8\x0004pµÁK`¡
÷E'\x0010"%®:6¯QºQi\x0014è	6\x001b?»
y·õ±\x001eÒ¦\x001eR
²4Öä¯­\x0004Iô@%â\x000cHÃ6¶¤aÅ<½yþ¼OÃ#Cò¼6ÄS4Íå@t_þïtuõf7(ÑD
	Þ\x000eÎ\x0003\x0011\x0019ua\x0008ÖM÷UÉLÖé\x0003dFÀ\x0002ÉÈBs6t<Æ¡é\x0012M× Ùâ\x0013\x001ceË¾Ãg«"3%©#ËÃ7\x001c§êïFcmî:Ý*4[¢ÙZ4§qÑ¢ÜvB#k×U)Á\x0006¢b¤r%«¢²\x001e¯\x001cL+¡9«*/íÄ\x0001U\x000bæK4_\x0016L/\x0006\x0001BÒû³ ©ÿ\x0019U£\x0017¬¸ÛT5]åuvýÜQîAhj0\x0010¦;è¯fÅxÛÎV\x0019Z'\\x001eC)·Jh>£ÙnÙ~\x0015ZËÎò*CëÂí:ß\x0005© «ð\x0011óþïÞ"ªØTMÕ-¦GpèØ¥ù­¹\x0003Zî`l3Æ)õ6ÖËçÇ]\x001bNéfZ£¡NwËyE\x001d\x000b´¿.\x0017gWç»ùdÉ'kùâNK/fì\x001aÏE¼R\x000eCåS%ª^?ÓÌ¹R¨\x0016\x0016PdÀn\x000b`- .\x0001u5 Ì\x0013£§Z94¥aÊ\x0015c\x0001M	h&¬ U\x00021Râ\x000b+HOßª;6¾Ï|¶Ïe\x000c¢åhZr%íÞ#jñ|ç÷ïûNÃ4y±="¦ö!ùXÉh8
Ø\x001f\x0019Öf9\x001fi\x0007tïjNI!¦\x0011ÏÉºþ p,´a±¹ÏuåÀCXÕ:®ÛëXÍøo°6íomª¿µj*û¸¢[wSÝ¬º\x0013\x0013F#êM}fíZ\x000f1ô]ß\x0004¦í¤2üqVêæÉð\x0018«T·ä&÷hGÖ(Ö÷z\x0015þ³ÝÄ¢$\x0016ÓÉmÆçÁTù\x001d(V}1hYBËéÐRåÃÏ,I\x0012\x0019\x000b)Õ\x0016¹jhUB«ÉÐP MÉi\x0010°Å\x001aøf\\x001dï¦1§Cë\x0012ZO_i§Àº\x001f\x0016i\x0019ëÜd·h:´-¡ítèâiÓ5:ÅDóîóÉth_BûéÐ>1éöxë°*U¢«\x000cÍÛönÁó±©¬C§)¼\x000c5\x001b6/X¶PáòããÍóo\x000f·»|	\x0004\x000b*ó´
%\x0001\x001b~Xæhyx¾ºúñìxCATY¢Ê¨ÅØP\x0003\x0013o\x0013*oºz\x0005Ã*PUª&¢ò\ôìâxæ*rëæ@5A%ª.Qõ^¯ª)QÍ4Té1ç«ÂÍscE\x001eû ¶(ïU Ú\x0012Õîõªº\x0012ÕM\U××Xä©h&w.¥Ý\x001cç\x0014T_¢ú}^ÕÂ\x001bD»µ×¬-ÃÊ÷Û²c¬¶-wWe\x0006hü\x000fCy|0\x0003ùª;p\x0019E+7_ô$k´¿/Þ<<~¹ù¾ë}±ü2ê-Éë2ZQH¿ô"^,Þ¿]]\x000cÎÏÙ|ÒDñX6'TYKyðøbï\x0003\x0015+
ÜÎµ%¬^;_\x001d½§®+Æi¹PCã\x0001U	¨&, §ÚO²0°\x00048äÆóéOW/  ^\x0017xÁ^rÆu~\x001cêï¹ª\x00014% °T4%\x000cùb\x000böL¯\x0005´% °ªry\x0004G¹Cå \x0015¾\x0004ô\x0013\x0000©2:ÜI\x001dÙ\a£\x0006ÒT£ùxÛþÕ\x001b@yÀñE+ÀØÿ\x001c\x0000)ûÃÍO\x0019¿m\x0015ÙY\x0019¿\x001598¼dl\x001c §­mÍÀõg¡\x00164á6Sß¬?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ûi{üä\x00179ÎÇ/¥óë¾c.ç½x
!{Cbj¬¢ß¹æ¸rFÜ³ÌÎyëÚS=Fxåz±.\x0000ÏüE\x0004+fD°ç\x0011\x000b\x001d51ª\x0014^\x0010)ª\x0014î\x0014²l2K\x0002\x001d_D_äYf\x0004¼\x000ex¦JêÒ\x0013\x000cz
¹ZX|Í\x0017Ñåèg\x0011e)n\x001aÞGÒã0ú\x001e¶"à·æ{ørBü³L\x0008´ñKÎ
ãI+<$\x0015\x001dZ¾¢X:ôEl²ì\x000fÍ-<ùrO·»»ûÝ¯ÍòVÁN;rX\x0007½¼S\x0005>WyÔXb§·ÛóËíE51"\x0005±\x001c&\x0006õäÎä\x0010oGbGî\x000bi*²\x001fýÄª VÃÄaÇb8A>Yº9Hf%)Pë+¾·nbS\x0010Qbf=ÝÃ ¬ÂS":£0gxPU<ÝÀ®\x0000vãËXRô\x0000ä54Çe,ó\x0010×|p½ÄÂc lXZEB\x0015a³IÑrÆU,~âbãÉÑ'\x0003\x0010u-3 Ä
\x0015sÁÎ\x0011Kíªºñ_?Î\x0016òÇáaÉ"§\x001eê\x000erE*W²5\x0000½AïV\x001cÊ\x000c¡\x001d\x0005î`5c,LÖd~®<õ\x000eÌ×3æëaæTÆ¥£lH5Ó%äm=\x0013ó/3æ_F9§PÛ1\x001cst@AÞÎ¹Z4¿ùÓùÓè83ò\x0011ëc·CÉ¼Í×_-°?° ÷3èýè@{\x000exgcB
óÔñP®g÷¸¶bôv÷ÐdÌAÙ£CSsªWÐdËUu\x00071¿ãíörÉvç¥[1ÍCjÔ\x000e&>RCM`\x0019\x0008\x0015°c\x0017£2ê\x0001Æ`épl{Ã\x001d\x0016\x0007Nz(ëb1Sf2l\x0002;/´´$¾\x000fû÷íCujT\x0001OZÊÚ
o\x000f¼Ó´«¼
òÃÉe°ÙëÎ\x000c*§ r\x0008Ô¨ÜDL\x0004Á¢®¡\x000eà\x0016V=eÕc¬R¤mÄ¡}\x000cæ\x0006SAgÔÅÉo@eóùÏI\x001fÂáôµmB$FQ
¿Ç·´d\x001c\x0015ã\x000b=º>céjq)Qô2JïÕòÒam\x0016ºç\x0015½¸\x001eF9eýãxpw\x0019åáA\x0019\x0019½È^¢ý\x0013ÌkUÆ¿}\x000cá$ÈíÝ·û»ýæj÷ðíþáæ¾ñAFÑd(ÿE\x0019\x001aÉ¹ÄÄ«ûI·çï.NÏO6WÛËw\x0017§\x0017µ«ßÌK{L*íÙþ}w(aÿù{øqÿí¾­ÈK0K%\x0011&ì«´­@¶\?\x0015ýíóC\x0019ûÏïÃ'ï.Îëcnæ\x0015>&Uø¬çÎãÊòÜÙEä¼\x0003g*e\x0007ÃôrJ/W\x000e=÷E\x0005Õ\x0008\x001eé
Ëiþ%>L¯§ôz-}ÎQ1úÌJ¡s\x0002¯¼»é­å°_ÄeÜlooö\x000f\x000fÑÛv|ÿýzÿð­QYÇ\x001bsdSôKS0.ñ°f04*í¢\x001fúíéÉåeôµ\x001d_¼yrùî´á+éW\x0010ë¿BÒ±_\x0001®òô
0!7|Jó/ §_@®ÿ\x0002ÁêH\x0015$a×JL~åcTÌB¯çú
Nð\x0015¤;$0û\x000e~d¶\î>7Hþ\x0007ó^'ë	:Ç¤ô!HäÒºJÚî!­år{\x001c K%¬Jdµ\x0002\x0019\x001byIÏM%½@ÕÞÒê\x00155BmJj3Níttëqf\x0018Â\x000bÐkFj\x000f³×D*5-áyý°¿\x000b´ÝæjßV\x0011\x0007¥ºíY:Ü¥ KÍ ÅáÉy Þl7W'\x000b¥Gj^\x001d©Ô´¨g;#¤_à=6NÂk¯ë\x0005C¦[M¹Õ\x001an­©§$Äy}r×J\x0008&nå\x00172ÜfÊmÖp\x001bGù\x000c:\Hè|<WS	·ø\läæjW\x0004~¨`]üû÷Ý
äó=Üî¿Â¾|½û~{Ûæ± \Èñ9.ÐB.khÐÄ}üßßoO!§ïòìä
vçëíûp/'næØ\x000f¿ý||Ý\Þüýþ¦¹Ñsxó¿\x0008Ó	Ï1YG\x0007ûñ	}Î«ÍåéÓËÅâð}È\x0005\x0000lÅ±\x0015\x000bÇ`zb8­PáI¬
× õlÐ®vk ¡6OÔJc)
Ú&l÷Túg\x000fv±DÜø\x0012Q ­ï\x0012µpÔêQñ æ¦ò\x001f ´Y\x0007êØf}\x0018Ûò,\x0003ï\x0004­i¨+îò!fS25ÌT\x001bJé~\x0012Ò\x000f\x0010»\x0012\x0018ÁåPËUCíD:D¬(¿È(I\x0011t\x0001m;òò\x000cá«\x000e\x0011nP\x0001YëÁøN%ðääâ)éÙ\x000enSrçYÙwB\x0013a¼-:Xj)\x0011#Ü¾äö«¸\x0015¶\x0010´PÞ^ÉÁ~ ì§
#Z¨áPÆÃ/b\x001cR³Ïî¿ß|Ý¼Úÿýækc\x0005­-:¢;K=\x0012C'IL½XJÎ>»x
wûÓ«%¥»Äí
n·ÛH]F@\x001eÂVR2ï+.>pîf¯ð\x000bz-\x001cßß}
O»ÖØ!³ÕlþqNm<­ÓõgÂñÅù«ð®9o \x0015SR1FJFS$EÜCX ­;à;HåT\x000er\x000f·HJg3(K\x0011\x0000)[¿ r×Aª¦¤jTf½`M£¶\x0012\x0017Ù¯¿µ:@Í\x0014Ô\x000c¢D\x001cÌ¼£L\x0018mòÌ×V
N¥\x0006\x0012\x0007\x0015%\x0005
$dé/øå6\x0012T\x0014¥\x0017¬ô ÷\x001dí	@tÉºU¢\x001bSÁþ´ìJJ×DIìÇMrã\x0005b%SÌ(\x0010;EÄ¼RöÙK,xA\x000c?\x0011kí
\x00031HÃùD¬@bùd6byè\x000bÄðã qx2á\x0010,Î9ÍÐ­!mM
¤\x0017XOLÌ\x0000¬Ë>\x0012\x001dÀ
º±ºäªã©ÏL°3© DÚðò[	ìeêÉ×DøÅ\x000b],«ÝÍÝ7\x000el\x000c'1ÌÙáÊj\x0012\x0018\x0015?UÖuÀ¾Ú¿CýÀjr\x0006±ûÝ¯bçâ1] i\x000c^½r\x0017±\x001b5e7j\x001d»SØÅW¿ILïr\x001cÍLû¼ä¦ 7+GÝ\x001ei¥6çYZtÜéZÎö\x0018úÁÖ\x0004ôÂ±1\x000eÝ\x0002%.\x0018I	)PI\x000b¦Òôy]\x001eªÕ\x001d~\\x0003\x000f\x0001vJF¡£¯@-4Í=%TôÁWÓÕf¦²=¨Y_ÜÞØzÄøQÛÊ&að4ê,I;:K/X/*G\x000c#\x0017g§ ·\x001eé!v´ðª²sik{¶\x001e%\x0017é-\x0008ýÂÐç,SÄÍëEý\x0003ÜrÊ-WqKÉ£Ü(\x0001jE\x001cMí\e©\x000c«)¹Z7â\x0012«îx|Çbû\x0006KÝG¯Äx\x0007Éõ\¯\x001ds©ÑÁèöó!_\x001f\x00007Sp³nÈ5ç`×\x001a\x001arËÜ\Â\x0001r;%·k<åÁ\x0006rå°0æÈ\x0017JK;ÈÂ!Û\x0010À/^Àãüv·yuó9\x0005.¿Ü·=Ó´\x0015,»?YJotx¹st\x001f8ÓÏ¶W§¯Sl)ýÿÕJ{9¤öq~(5
Æ\x0006ü½7¨8½½½¾ÿþõk¶yà\x001a¥P÷TxøkT\x0013!)g]ë\x0001A>\x001cÞ½¼xu\x0015&%LÆÇÝ§Ý×o\x000fµoq¨}ßBõß\x0002ª|%uAòémo½\x0017$¥ké%K_£f!Ð×å×Ïð5&y2P^\x0017i2<5k
_£ÿ[,¯¨CTú\x0012ê\x0019V\x0014´=ÄÆCÁz°)íÁ3ªÕûkÅðåðÏ± l\x0016Ý²ÑoT(ã]WÖ3\x000bnvf¸ÁáWë¿Ä¶¤"¼iS©&ì\x000eG=|¥Vidw¨y\x0002òz*x}z{ÿ­í4OkP}@Ñ\x0015Á-Õ.[»(rµ9=»x·p5\x0010©ê1R×p %E\x0018ÉiÑIh'å¾\x0018S?ªs\x001dµàÔg \x0018l*ã\x0016\x001aVµ£búÅØük|f\x0007RK¶MxÁ\x001e¼õ«¦ß«Ø ÈdË\x0000*~}ä÷ýkÄG8(,µ\x000fÔá¯)IKK:øVVz8üðÊ{UUùHØPµ7Á\x001fÇ¹£¾\x0015Ï×N2ÜylÃÎ\x0007UIy»Zâ3Ïú²S%|0Â@Z%\x001cj­91 '':èèþr\x0012õBÿªd}Åãíòd1#ÆÎUæíTe~\x001bzë ß[¼
ÜYA-éûvsë)·^Çe\x000c\x001ewÂfÙ\x0002þ,­bí>è\x001b)\x0010¾âëèõÃîîÓæC£\x001c¹¹­¨ùLZáöÎ¡´#à°¶__nÏ_m>lÏª\x0017¸ðÑ?¡Ã/^èIhuûýsØûÍËï\x000f¿ß}jmy\x00071JÌ\x001eB\x0014^EÇ\x000b3|cº³·ï_Ýx²yùþòõûóWKùÄ¯\x000b~½?ÿ\®ô\x000fÿÅ\x001c¯Ü\x0003_ÁbíÓÁ$ì©^Úîá×ýÝ·Öná\x0012<rä'u¨ä%}8fÐÙh°Þn/ß¿[L%f5eVÃÌ6vø¢ÖÚ£ ô\x001eÔµ
:l¦Èf\x00052F¶\x0012²Âaæ4ÌÏÂìM8RÂóìà6D\x0005±¢\x000f÷7ûv\x0011=ºÏK\x000f)Ò©\x0012\x001esbÂGY?\Dé¼p¥3ó¬\x0001óB\x0014I0Ç÷w­L1'I0Ç\x0017ç±Ií¸Ë³ÌùËû}[k&å8ÕB'\x0016¼\x0018£È}¾\x0005\x0017Eb_^^,´eBBî
B×\x00082\x001a\x001a\x0011\x0019\x001eÀaï+"\R?»ûß~L\x0015Ðó<\x0011=Í#\x000f\x0013ÿ÷Ýíæåíî®­|\x000fä1ý\x001dä\x001d±­pTb\x0018Þ!\x000bâÀï7a²Ãí¶yy¶=?Î~x¦0Ôár<äéåvûËÃþÓæÜ4&aÇN®)Ï1\x00172¤
)JA|ÂA°=ûÓåÉ«Íÿ8]ÊÁ6ØÏ$/\x0001\x0003ýLÜ¤Xê\x000eÔ\x0018hÅ¦}ÁPæ8ºa!U_©½Ê=ÄRk \x0005\x001f¥=DÃ/^\x001c¤^ÝÜü¼ßÝmÞí\x001e>µ\x0005´5×dU\x0015¨\x00072.	ViÃF\x0017ÇO¶çwÛËWÐ4;ôð/3ò\x0004Ii×«Ð\x001dJq'É<Vp!º®ä¨±ÛÝ®eç¿\x0017ÙGá\x001dø]T:h\x000e²Ë]®c7\x000eôU";Þ¯È®¨å\x0004\x0015ö\x0010;gÅ¸s¶ràAÑ&-\x001a\x001b.\x0016§\x0010S!¢ûðº_¹Y#3\x0008ÒÀ¿2:³?'z¹WùÚÍj-\x001aXè7a#`ÕWrzá]¼l¶9`#êH\x000eÜ¼ºoÓÈ\x0016ÒPÑdáVO¢¦ÌsL³á<\x001eÒÎ¡W\x0017 ½:]"\x00015.\x0001Ö`ÓcWÐ`µbF3ó\x000c\x001e,¯õìcåÅ°Â#¬Y_JBº\x0003êè9Õ¥ÜTj4ûPUªÆPNP\x0014ë°5\x001dð#²êJÅI\x0017«Ð\x0005+ü8À*ÂûS&#ÔgIðîÂpe¾ÑÇê|Á
ªZý¬ z|D^&íW£\x00052sVIjä6ºkå¡MIXú\x0012mú×û_w #\x0001Ì?í\x001f®Ã\x000bôßÞÜß}Û}n+°×L£*!7Ü¤&\x0005\x000cíjåÝ`B¿>¹|³\x0005M³ÍO'/!2ýæâüÝöõÂ_çp\x001aGÏ\x000e{®¯ÃõvÐ}\x00004LçÖAk¾(¾x®¯#4\-ùë$\x0013ÜY\x0005_çÿÊ·QÅ·QÏõm¤Ék-|\x001b\x0014Ò0Áþ¯­µbë¨gÛ:áò
¿\x000e§Z\x0005È\x001cÈS¯UXñut±uô³m\x001dCú¼±Ä­c³\x001fÍÖd\x0012¿,Ý)á\x0017àNùi÷ë~÷=:¼o\x001eîï>ý³É ³¸ípÉa¡9ÞÀÚXñø	üÓöÍÉö}tu^^¿úóÓ°b
+þà°r
+ÿà°j
«þà°z
«ÿà°f
kþà°v
ka!Ë\x000ey¥ÅÃLsìjS+\x0008\x001f vSb7N¬±E+WZ i\x001eÌ\x0019JÜ5¾\x0012C\x001f öSb?L¬\x0018å`*C:\x00031U\x0003°Jmr?0gÅ\x0015ÁÆ
%ê*\x001b3W"±¡"\x0000^\x0011M\x001c ./µ\x0015·Æy Vø\x0008öÂÕ³!\x0017W\x001b_q·Å\x0006ÃiY\x001cÒC\x001dÙ\x0011=ÛBæÅ\x0005ÇWÜp\x0006Åä9´òÕ¸÷(ã&ì½JÕé\x0000rqÍñ\x0015÷Äñst"\x000bþì\x0007\x001c/.;>~ÛYqÇ\x0005ÔÎâ {C\x0007y¶eQ\x|øÆsámìéÒcD,È[\x0002ÄÏ6ÆÅµÇï=èßo\x0012\x0015.ôÄÒ 	L7uÅÁ3\Ü{|øâ\x000b\x000b\x0015gGdåQ»% \x001f6\x001f{¶Q..>>|óAÀá]mèY\x001eÞêF¹&\x0013Ñ,«O\x000c_}.7û\x0008G\x001c%vhat\x001eåg#.®>1|õ9P²¬\x000bÜ}ÆÓyáüãÞ\x0001äòU7|õ9aÑkÍ¡°Vâî3¨s\x001a+\x0011\x0001äâê\x0013ÃW\x0003}-<A\x001bQ!2ùdLM}\x0000¹¸úÄðÕç¢¢%\x0005Ú×¸0ò©¬o)\x00177\x0018¾ù ]-\x0017ÐÝ>í=É\x0014=TE
g¸¸úÄøÕgÝ\x0011.ä°¦S-Ô=+¬J\x000fÊ\x0001ââæ\x0013ã7ã¨Û\x001e\x000b
¿\x00022\x0011»Hï\x0000qqññÏÉ|ñ[D\x0012q~U{÷xc\x0000¹¸øÄøÅg&Í_T*ìé\x0016y.\x0013N\x0016×\x001c¿ö |FÅx>Þ\x001c­Zíô\x0000qqíÉ\x0015×AÁÃ@ìð4t\x001aëJ\x001b\x0001ÞâÎãw\x001eçGÞ ¯EÛM\x001fxë¥3sü­ç]¶Ý8ÃäÜ°®\x0008Ø
 \x0017\x0017\x001cë9CÍ­Ã¾Ã@\x0016\Y¡+e
\x0003ÈÅ'W¼õ8u'dåóá±§ò\x0005Âm!\x0017W\áß´GÇ\x001e\x000e2þ[H\É\x0002\x001a .®<9îäT2ÛôCÊ|rÀQù¶1\x0015]ë\x0001äâÎ+¼<«\x0004Ë\x0013ï<®²\x000fÀ?Ûæ+®<9îå\x000c#KçE8-ú\x000cóÞ³ü¹n\x0010UÜyjÜËÉUnz\x001e\x001b\x0017² ÍHcíVÅ§þ¨±»ð2/ã \x001a§5g»ëýk[?9i8(m'=|Cýäx0çRÂ¬uáÖ¿¿\x000cðoN\x0016*\x0003Má\x0017"¦³ÝMS¥\x0001(gaf
í§ä\x0014áàéªª¸:½¬3Zã¢ÚÍ¡(Â¸\x0017Î\x001cJ\x001eßî¿Ý|\x000b}ßûÖÆ\x000f}¶ÒâÎç¼:]+ºâ
¢âÇ·Ð)<üyöþäÝ»¢&Fï\Ù	~\x0001áç·\x000f÷¿îïv £uÿñË~ójÿËÃîîcc¯Á`o¦V	\x000c8ñx\x0013Ö\x000bÊ¯ªõ\x000fz{yñæä|\x000bzZ\x0017aoò§ËíùñÂ\x0002Aü?9â«ü<] dµ	",=\ÚBW24Æù]ÁïÖò\x0007SÉô\x0005Â1bRB{¬\x001e³BVJ§¿ÀTWÙF\x0007Ýª/`\x0006êø\x0005\x0018u\x0017F`í\x0015¢rz\x0001S|\x0001³ö\x000bÀû%'&|aò
âªò¨\x001dæ\x0005¿\Ë\x000fnÇØ+¼S\x0010\x0007mX)ó\x0014Äõ\x000b¨b\x0005©µ+ÈiIÕá\x000bØt
ÇP0?ðëgÚÂ×á_V /!M9 gáÈµªáÏwíÊ8\x0001\x0018Ì«h\x0008xCÍ×ÂC\x0001eS1µ@á?Öª?ß%Y*3\x0017¢d\x0006\x0019\x00168õ¿í»®)æ9È\x001dÄ
>f°8&Ø\x0006¤â§+¦÷Ûw'O^M\x0001ÒÍ!\x001d@þûÃ·Cû°"î\x001a\x000bºxÔ\x0011H¥GÁ:L\x0015]ð Ò£Jïé¿|w¨rÿp\x001aÃù»§¸¹\x0016\x0005787É¥dDn¡Y[J²
3hk>¾(:ÉÕ|ÄKK¹WS Þ@¨Þ\x0000­6TÒBà¤\x0010lÛÇßg@* sF1e\x0014C\x001da\x001d¾ÖX6\x0007
\x000f%ÕáóÇ¸fD9EC ¬\x001a(\x0001*©\x001erA]8¡ÉÍ:D5ETC û¬Q\x0001Zã¦âÁR%F¡\x001eÌ63ê)£\x001ebäæÈª²Â\x0010v8òHáÂñJu3£21FNMÛ¡ò?µfàÜ(²âºof´SF;Ä\x0018ÎxË1	¸%FF` ­btSF7:×\x0016{åiÎù0×Ô\x0003ØÉÐw3£2ú1FoçØÏ/ÕÊ\x0004Frµ\x0007F+cN\x0015K'8\x001b]\x000e%?\x0005E\x0003ÉóÆ¶\x0015çe3dyÍÝ3B`Õb8Îý\x00112JA×LåÐXÜ2|ì1Y^'L,Éë\x0008jR\x001c\x0018+Å¸ÍÅ=ÃÇ.\x001aË±åG\x001cGwaîRk*\x0012ÍÅEÃ\x0007o\x0003#$\x0004"¤´ U¥ ¿\x0019²¸iøØU#tÞ5Ð	g[\x001aR÷Ñ~ìªùGà+³ÿ¿Â¦¹ÿvóõë\x001e76ÐYlûq÷ñf×d¿\x000bP#N¹]Â\x001by\x0014;+º`\x001c;z&J1äÙÅ»Ó««\x0013PßØÀÃc{¼=>Ý^-q)·XË\x001d,­M.àãX®\x0015°+î±\x0001l9Åk±\x001d\x0015È«É	ÄÖ>?J+\x000b¸\x001f[M±ÕúUbÐ\x0019\x0000-\x000b\x0015®\x0012+³3àÙ¸õ[¯ä&öX;©\x0018ß%uS\x001bìÊ
ÖÏm¦Üf%wX\x001c8Ü:0kr)-«=Lú±í\x0014Û®Ä\x000et\x0004c6qS\Î*a­\x0001n7åvk[Î×<sn_XÞ5Ë»ÛO¹ýÚå}ØZ\x001cÑêÎ\x001eºJÊZ#5wýÛ­Ü}ÿ\x001dMhXè\x000bÈÔÜÞÃÈ©\x0019¬w»ï\x000f7û¯\x0000\x0017V¨\x001eÉ&\x0018Ûccp\x0008H\x0004~)»}yzryÅ]@&\x0000>.R Á·:@\x0019Â$¦`îÄ J`ÒÉ$§ì0\x00134ÏøÑ\x0001å]´\x000e\x0003\x0014´U±\x0000\x0015%¼\x0001Jñt­¹\x0013}­\x0001
j:9BÁE ÄºÙúEüè\x001b)°U"<\x0014	J­>\x000bP¶\x0007Ê±¨®CP ¬&¨/1\x000e\x0005êBñ£\x0003'Ù\x0008²I¸*0Å¬È¤í:&\x0001K\t®ó`±¹Ää¤O,Ø|\x000eæ~hI¹Ê_ÿ'\x000c\x0014T-Å	ÔÝ×Í§ÿó¿þ÷öïQ.²\x0006çÃ,²\x0004\x0007>¬h´\x000bèx\x0007LñÊGØÞl¯6¯6[Pl T@¨Æ\x0008c
\x0011\x0011rµ9íBöñc\x00001<ÅñÐ0Z¥vD\x0001Q\x0018a©yí$ëAÊ}B!Ç\x0016	Ñ¸<Ï\x0016Ît\x0003ÈgAèUü\x0018AôG8 ­C´w%:]Æ\x0008ÿñÕÿSR¹yÔì»ÿþè6/·Q3Gh#O/o\x0001ê\x001e8nÜ%}}¢º¼xÿ\x001a` 6	þi¥a6FÈFû¤a
ò¹\x0002\x0017\x001a·Î­ [	þi¦I½Ã"
L´D\x0003)É\x00154B+;f¥\x0016ç2F\x0012\x000fcC$7z

¬é¨RÒJ£È¸:,nG¦\x001c­\x001bmÅ\x001apUÃ?Í4I¡\x0008hK=Çìrbá|\x0005	ÿeÓ3O2ú-eÔd'»\x0001¾QA'õ \x000c¨Ì¹\x001e\x0018\x0016«_$dJ)ºÂ»%Xíf\x001c&>âGÇÐàe,¹.]¸»2+V0jìøÑ16.\x001d}å[-æ\x0011D\x001a¹æäã Æ\x001a?\x001ai÷±\x0003dX¿¢
\x001c 4á¤`Û\x0018\x0018uühÆI/P	/.ïonÒþ\x000e\x0007âøAÌ¡\ãEúlÄJU\x0019×±Ô"æã'\x001bÓ¤£XI)ÇGs0_Òg+Ox\x0011ø4<a'ÿ\x0013<\x000e\zÛAe
8í÷&äôh¤aàñ4\x000e/q%Ð3=\x0003TúlÅ	ÿ«#>J8"¥ÁQkFÇG\x001cß\x0003\x0016¶ÃÉÞ¼Iá>
Oùæíã\x0011p>[yTêW\x000c<ÌÓm%c_älüäáÑ:MÍ<\x0006åÀã\x0010'vû8Â¯Ø[\x0010}>q\ìã\x001bql*t\x0003\x001eIÓ%ÜÕ,Tt¨ö{\x0002<P\x0000<áÖR\x001ayl.±â,\x0014 \x0016>yèNã#8ò\x0018ÇgÅö9\x001dé³GÒá\x0013\x0007B\x0019k»Òð_ê#:n:LA¯u\x001e£\x0005âà\x0013bõlùÈÓ~sÁÃT:äÉ®I\x0019õkg\x0005\x000e\x001d¤ÏV\x001c'b\x0015iÄ1ª^¡y-5GG¡í8
]t÷%\x001c$¡\x0001Çqâq+GBgÚôÙÆ#\x0018I­¨´\x00163l)´3Zqö(ð§ÏV\x001eÐGD»Gî\x001dxÀkxÔ\x00071(h\x0000lÞëñ\x000e0ÚÒ=ªÀÅ#
_qQ¨xo©ö{K°p0\x001bâad\x0014*c\x0005òè\x0015s¥c`$~¶â\x001f4-eÏÈ§\x0019ºA£vî
\x001c\x0010æO8ÅÃ8\x0019a~:Ö¢ºb«kðé¦ÏV\x001e\x0011EÓV×´ÕµÎ&³+x¢ìiúlåÁ\x0004		¦\x0005O²,Á²´È\x0013\x0006{ÅÅeã|ÙùBè×\x0017ò0äÑ+Æ'
s¤ÏV\x001ecÉ\x000c\x0013ÞHW\x001c\x001fF»+S:q~»Qøï\x0018.}Amî¾owÿ|Ø/=ÕÙîãÚ\x0001MõìÆpäm\x00120ØþbûçËJw\x0002\x0006BhBvÐdo2i\x0010\x0001G?F0æÖÐÀãHñv\x001aØW\x0012i<¤fG\x001akFñØ^°£Hî·ÆáLÓ\x0000zÏ#\50á{¨E#rèG«%hD¦±r\x0005
ìF­zh\x0012\x0016ô@Om¡"\x0011|\x0005
ÆLÇ\x001cq×¯¬\x0018\x0008³fÁ@£
Ë:`\x001c>Î\x000e'3\x0018ðè\x000bÆ­XC\x0013,\x0012«;hR«-\x0019\x000b£³\x0017ÎhtÎÞ\x000e},`º\x0011üPRëò¸d2Z±zcWøÑ±f0¾¦!\x000c\x0005¯0+hxtétya\x0018Fû\x0018ö\x0018ÓD4~Å
¼çÌ\x0003§	Å³¥\x0005½ä(ëÖLUtX¨ë	\x0002Ê\x0007\x001c<k4WfÅâÑ]¡:Î=f£|J¤q´µqH£Øª±\x000fý\x001dbÇ3
]Ý:¥ï¿¡þö?¾Lb¯ÓØðý÷Û»ýBþ\x0000%µäjq\x0008|{\x0010¬KÿjFÎ÷g§çµ~i%YsÑOf\x000e\x0011|\x001azc\x0015ÞA´°\x0000d74ÑP\x000f\x0005¡ÕRzÐÂ×Sýhùp\x0012ö\x0007]J$ãÕ\x000e²°æu76tñC	\x000f*ïÉ\x000caâ9¦3\\x0004¦LÓõ"¼&¸÷,ï\x0001ö\x001chaIØ^4
±A++>Jl ¬æmt ë\x001f5OÑ]\x00185:9¼Îû³\x000cïö ý}Ç÷{?9Ô°½Þþëæj÷ð\x001bt[üþy¿\x0018_\x0015ï¢YÎÈx4`(¼EØTïäjsµ½|\x000b}\x0016ß¿>©?%\x000f|ðô\x0006\x00005¥5)/R}#\x00185\x001e\x0008¬\x000cÕ\x000f\x0013ÒûrPÆ®s@èlÒlF #BùL\x00193@((!Q9sd,ÏcÈÍó\x0010Ý!Ü\x0008a°\x0015%\x0011ªT\x0001¶"å\x0014	Æg\x001dR>ÏÀ\x00182Ê4UØ%.¾(¦4IÆùà\x001d[ì\x0008\x0007\x0010T3i\x00001|\x001aøôó,BðCË±E\x0018M¹´Mê	FPð2µn¤þÀaÕØ$ÿ_%\x0014öûÃîfbN í¾ÿ\x001e@\x0016ñ¤+S.\x001eO:OÂj¨\x0002Å\¼Òi1iz|¶}ÿð»&8r1õÒéCn\x001eóx
Z\x0003CFI_z=\x001d!	øè\x001e¼\ Å@\x0005Õ^´\x0013\iÂâÁÓ\x0010>ºñxT\x0000<m»3íÓÏ0·Q\x0016&~ôâ\x000b\x0004g2B#\x001eY	Lé\x0008ct\x0002òYâG'\x0000å\x0013´\x0001Ó=\x0002t \x000eÜôÞ²ñ¹ý.¾ýö_ÿ\x0015Ý±\x001b\x001aní£B\x001b´á:ù|{óuù½mð\x0001	4²DéÁaË«\x0003Zj$a¶ÍÉë³Ó«ú£{9Æ@42üþhÁ¨þhd\x0007üaÐ~Ýß_§öüN\x000b»ôr÷õÛþfq
æMj#È_©¤ôE£û!?ÔÂ.½Ü^½;9]Ú¥\x0013¼ðo1z\x0004"\x0002\x0012ºäa\x0015\x0016Ò\x000cP\x000e}-\x001fÜn§ÜÄ\x0017\x0012¦Ø± H¿qÏ1~\x001cª\x0004ãGÿ\x0000J,£FqÊ\x001b	F\x0013N0à3\x0000
ðkÇ~@F9~Æ3ÊÝÐfX¹« 	ðËîúÞ°x\x0018Ã%{H
\x0000!ÏÏû»op-í]¨rEg\x0001(¨`Q)Ë!Uñh9\x0001\x0008x^¾>9\x0007×X\x0003Ý¬¬ Îp\x000cÍ+
BH},²+CÇ2Mzér¬ªwì\\x000eÍ\x0018\x000br9Õß	ûh¢G'Ý¡²\x0017ÏZ*{b<î<'ýKæ\x001eK¾í¤Ó\x00100\x001ftQ\x0002ÑæÇ-|ÿ{þXÖN/\x001eDõ¤6¡\x0011O0¦1{Pi&(©H	L	\x0007Ì£©Ë½xP\x0016\x0018?zñ@Ù
]\x0003á
q¦)®ÍÙcI"Ýx\x0002ðD?\x001ecl«¤"À
Dî3ñhÕ@\x001f\x001eW:&®éþáãHbpø\x001ceòêì\x0017Ì®ß¹Pç\x0002\x000eR6Àç\x0015{Ð×Å$>c$=k¹[?½\x001cü/Òg'T¤\x0002R\x000f©Õpa¨Eyóh"}/_,åñ¶ûV\x0013"¬?ÆkC¹¿ÆKLysþYÆ/Uö\x000el_x;b|\x000f²Ï0f\x001c¥ä9÷hîv\x001b¼ùíÉ\x001fË¤ºt{³Òä/\x001fnî¿Z¾~S¯ÓXQG!ä°öh\x0015ªÇ\x001c¸¤¸tvz\x0012\x0015É_^^¼Õ\x000bCc×àúì/B_\x0014\x000e\x0010t\x001fs¦ÿzpß¢Û%\x0016/M]jûoÿ¬!Zï!ÜæEF\x0016NÉ]euyÐuyrùîÏO3IP)\x001fíLÐ1\x001d\x0013$÷x\x0018BZ(Õã9±
JÆtôÙH\x0005õnav]ÌyqñY¯|~¹ÙÇÝ+OPýòÙüãorâ\x000fDþÞÞÞ× ÍÂËáÙÚ
\x000bÞ}\]®.ðöì¢çÈò2W>Û\x0000\x000c\x0015\x000f\x0003'q\x0000>Ëðè\x0006\x0010T=D2;\x0002 ÚA& Ç\x000eE¯µXr\x001b\x0010e¸u\x0000ùØH8z\x0010-\x0006\x001a\x0003\x0011ñë\x0008,K+{\x001cÏ¾\x0012Ï-Ë©°}¾Õ\x001ay>?üj?}ü+Ó\x000cöXú<kucÚÃ\x0019Ï<\x0011i=èª|5ù/ÿñ«¹c1¾\x000e
ðÏÙns¼»Ý-\x001fàJ`qgx\x0013\\x0018ìÉ\x001fÍ
v¶Ý\x001coÏ¶\x000bGõ<[m\x0014>\x001b&ØaøprtTf\x0010²cÿßÿóþo#|\x0003yÈ¤=Ûýý>¶Û¨Våv+%\=6¿JC:¥Mm?\^Vy¾}ý|÷·ÝtGíZ·A×ÉhñY\x001a\x0019Ãa#\x0019Âs\x0012Wì£²Ø\x001c!ýDT\x0015\x0011EU³%õóýîîî		|ßkè\x0015Fñ[r<\x0006Óôñ7ÚÏ\x0017Ûóóly¢Km¶Nª.:ã5Å~ ¢\x0016³Ì9ÙâÑ2÷v:c§tÆöÑaÉ;ä_P\x0016'ó9»áÑâ¦f4:µæi\x0015¼ç¼<
¯\x001fºúsj\x0003¯ø¤ñd';ñè\x0003:tyÊR+èRG¬L']\x001f\x001d¼ÌYÒ61¢ÉÂ¬\x001b;­\x000b:­»è´SGäUq\x0014L\x000e\x0015å?^å×NçÊóÄõ\x001d(Úpº Ú\x0005§6¼kij\x001fèÀó%ïÃÓT8\x0015½*\x001cGOç\x0013ù¨,N3`Åè	Ö9z©N2â	\x0014¾
x2C|´|¼\x001dÏ\x0016\x0007\x001eüØ§LlõLît\x001e[«É§\x0012FoÕm\x0001Çù\x0014Ï÷]\x0017\ÁÄ\x0001O$<É2Þ£Z:Íxð¿8½Ìxß±\x0012õò|®`¢eyã>*®ÓN§¥'UßÒÝ.ý5¦\x001cÊ|¢\x000cÂ
¼ò®mxÃRªr\x000e+\x001e­QÂ\x0018l) \x00104áÁ]xÊ\x001dÌîôª5\x0013?|%LÐÊ&\x000bC¾\x000b\x0003Ò<I)\x00149°ÚYzu[¿\x000eÏ\x0002Ï.<ÈæFG\x001e\x0008À$Gc8Sè	>sRtÓ¹ÂR®Ï\x0012Îä÷H'¨\x0010k»jð4+ð4ëÄ3ö\x0008\x0013ßA+Ô*2BÃu·ê6ÓLp}V0:ö\x000etl\x0001å© 
nãuxºÄëÛ\x0017ÂHÔeJx\x001añ{&<Q\x001cÈðc\x0017\x001e¤aþ´\x0018Ý³át¡m»Î
ÕÂt}\x0008[\x0015óÞ )fn\x0019EÛÂ<*ÎÖN'Ë±c'\x000fêR	¯L>
_·1¤(ñún\x000b!
Y\x0002g\x0011Oç#¯\x001c<SÒu\x001eÈ0b2/<4B\x0015\x0015fðy½o7]¹ð:\x001fgÁLÊ×T\x0018¶µá\x0011N\x000e.#W
)\x000f\x0015Óy¨ppw|_à\x001c=íx¨<*HÕWº,X\x0019\x0015&/GEE~Édªö«61Å\x0001?vá1Cn\x000b%\x0004Ù\x0002ÂÇ¡Ñî\x001a<Wì[ø±\x00079K1Q\x0018=Ü\x0019Âòç\x001f6âÙÒg;y,¼½óÆe(\x001a`ÃYhóÎ]µö,×%^ßÖ`ÁøÌ£³}8X+ÊIµã÷­í¼o\x0019ø¬E\x001e=+²ÞèÚÑS¥gU¥Ç£,3Å}jr\x0016VÏqÏÇ\x0000ÛñtqiÀ]x\\x001e&×`ªåö ©»î
äJG²ëó$3/õ\x0001OSPçm»
M\x0017ëÎé®uÇ<÷\x001bC1À´ÏBçKcÀ÷\x0019\x0003aÜåÔOdãsE~°UVY\x0003Þ\x0014'²7]'2tû9¢ûB¦re\x0013\x0006T=ÏeëKïóY@Ô6WïqRÇ\x000fx"¿ÖYR63Åó}\x000bÏ:Úñ²M¾PH 9lÙ5·\x0019
Ô©«6V¤vð\x0019Ì¨\x0000\x00139'Æ\x001amäÑ]!Sgù\x0011\x001aÞî°ÿ}süe÷m¿û¾pØAÔãÄ\x001avYØÂcAÉúï7Ç?mßlß?	Çù\x0014nZºÒD',e\x000e*«@e®\x0014U\x0008+ùLÁgzù4ù, û7W.ÓàÙ2§\x001fo\x0012
xÓ\x001a&<x!Æ§£\x000bk7ã©³+lg{ñT\x0016¯`\x00066=\x0014\x0013Ç\x0001>_ðùÞÙåGTõÍs%K\x0016Ûá¾¬vèÇz7­µi\x001b>o[%Iv¹|e\x0018õh¥M\x0007_q²ÈÞ£E¦ÖÊè
UÄ§ùã~>Uê\x001d?u¸4¤Ê|\x0007cE¯Ü\x001dMñ@°oøb@ºÓx.éÏ/ %×áqVàÅ¼ÞÝAÒ/NP1\x0010ËùfÌ¯;û¸.ùt7\x001f£å'ÃPb!µ¡GF¼âVñÓËûç¡ljä#)/OÊ9Æ¬;üÂÝXðAâ~\x0017æäÙøÂËêøfÂgÝ|3ë>}ÀÀõÇ¨Ö+´AfYû\x001da¬þ*\x000f¿H5ËY´3²,ÊÂpï
)Ö\x0008HëN#¨¨\x001a]yk\x001e×é¿Y\x0012!@[\x0002Ú^@çIeO0E-R\x0014#©S¯ôãªÏÍ\x0007«>\x0002N¬úF@Iz£ÜKRH^SQ5T¸¬\x0001\x0014ZN\x0001áÇN@Eq\x0017ýË\x0001PåÌýJËv@]\x0002ê^@M1?\x000eÍi\x0004
\x0001ÚJSfÀrEç\x0014G¥oS\x001c\x000elÜ#\x0012»q)g\x001eõµôðù¯o`âR.\x0001ç¹6\x0003Ô2àà\x000c_3Íþ\x001aþõÙ\x000bþ2üâEü\x0019\x00120¡Y,zø·¯¿=Ü,v#ô:	ÃH\x001d6Ã>\x001fÿ¥û!\x0019\x0013:¥J«·§5Hû×ÿºùòUDI\x000epA2Ûúêþv\x0003­Ö(_Ã\x0006°ÛýÝÇý÷\x0000\x0004âøS:¼Ô°Y·5ØCUpØÌíìäüøôäýL¯.ÎNNÏ^|¼ÿõ×ïw{úóG2¬ké$ãá)nÌ¥ò\x0010 (L$Sr5\x0019údÿñ\x000bÈ°}  )­æÂüç\x0001®É\x0019âyÄV\x0011eúG,¼4­2Ü?,ö¾@2±l^ÓßF¦RA:É0|\x0008æ4i|\x0002­\x0000{¤\x000c¢	ÌÃ1©¤ô\x0017È4ü%
\x0019\x001e\x001aýdü¿î%¨*\x0016e¦¼w_î\x001f\x001e\x0002Ç"P\x0016\x001aÎ\x001be å%¥Ú°Ì\x0010Mhçf;3»ÌÞýtqy\x0019~û\x0014ZÌ¯(,Ðà\x000eõæb{\x001c@\x0003Qýf\x0019Dsû¿3·Ñê:2ø\x000f7ïîÃÿú\x0012\x00148?ÁJ
S\x0019Ë¥óÂAû8ÁÌ-2¨Úøpúúü"üýq\x001cðÈâª?ü"®ªÙF\x000fîoØ\x0014(9Aà8°9á94\x001e\x0008lh\x0003\x0007¶ðFd³3*·6ÛËW\x0017§OñÙÏöóÉ\x0018û|P\x0013'4\JV#\x001få/ôòq&ðn:ü"ÞRS¾¯_¿ß|][\x001fã¥
"*11Ì7Hh¦¹õØiø\x0011¾««÷§WOðan
òIÖË\x0007"\x0016ÚàÚCQ:k½3xòz[Þ&¼bødÿðÁÅN¹`ÿ\x001e4½LÙ¼5ì\x001a<Uà©ÙU0diôtÊ\x0011ÙU4x\¯Áó\x0005\x001fÀ31m\x000bðÂ\x001cm_ÀÓhxêp5ÆG\x000e(ä+*B[\x0001Si\x0008\x0000Ý\x0011\x00176\x0010aÂå( .\x0001ûGÛØl%\x0002:4å¢Åñß9\x000eÈK@Þ\x000f(D¬n\x0003@îR7d\x000bj»y\x0004Å)\x0016¦bø±\x0017Ð$É¡\x0000\x0018öCò\x0006@Çp\x0004­ç£'=¢'ê\x0015%ßþÛ6\x0016ä-\x001cáÖ¼`\x0011\x0004\x0016°[â\x0001èñò\x0015ÆZñ8\x001f&m¶§ËÅ"Tå"lD\x0014)\x001d^Á³KBÝ^D\x0014hNYîV\x0012b\x000cáÇ^Â`%\x0018$T\x0012o9ë5n\x0013a¥®Lr#¢°Å 
Û=ÐmË\x0008FVÜ'ÖE?
\x0010:++û¤Ðü5Õ{\x001f~ñbÂ÷\x001dã?ï\x0017ñ\x0006k4ÙY\x001eÎ8ÇÁw¸µ¿fï=TÈ¿>y
o:ÇæÅtø\x000c\x0001 Ä'X²QÃ âU¢µ«øTÁ§ºù@?Ù!\x001fêrÁÛVd>SÙ$|¦à3Ý|:¶~¢ñ\x0005·ð\søj7]#-øl7_8¦iøÂè,·yõ­+\x000c\x0005S\x001a
mtN\x001e%#ßC_$\OvÂ¥A>W¾BÂ/WHxÂ½¼ý×/ßq õ\x0007\x0002èp¶@rM2¢V\x000e\x000f\x0017V; ¯6/Ã[®JÇÅlkÀ¿º\x0018¼ãý÷o»Ïûå+Ø+º?Lx§\x001bkHUmü÷ã·Û×'Oð\x001dÞÀgt?}|/	µ'@KVUÞpm²\x0004\x0003\x001cÊ
âüR \x001e^!hÃ\x0008'ªgóS|ñr\\x001dáË\x000bV®¿ãýÃÍ×è,^BF \x0006ØY\x0016ºÕD§Õ1±\x0010\x0018Ó=\x001c\x0016áñÉåéUô-/Ê\x0012T\x000e$\x0002\x0008 Ê$%\x0000
¾\x0013èÜ¡<ÀiJN3ÄÉU\x000c®\x0001§õè*² Z\x00111¥Pë9mÉi8e°\x001c\x001dÞíø\x0006µ\x0010[CPÅ+oävPÉÙ\x0014\x0014~\x001cx\x0003µ\x0000
\x0012W¨Ä×¨vîä\x001d\x0000U%¨\x001a\x0002Õ2j¤\x0007P\x000f)02Æw\x0000ªðëAu	:4õLÇÂ'\x0018QÐW2	\x0014ü\x00068¢~=¨/GÔ¨pÙOâ@n$¨r\x00027\x0013Èº­\x0006eì¯»\x00025\x0019»TË)ÜàG\x0002\x0007\x0015´ÓÓ z¾~\x0006Öë9ëu?«\x00129:\x0007Yå¸R³£]gÙQ³aUcÃª\x0004\x001aÀÞs\x001e\x000eÃª\x001dî~\x0008ZÃªgÞZ®\x000boí\x001e\x0012R\x001e>íïî\x00171¥i`\x0018\x0001Óhl"f!¬ñ(®\x001dûrùêäüâ)Êé\x0019¥\x000b{®\x0012t¦ÒâcÖã\x0013hxW\x001f³­®t\x0003`4áPZbGRS\x0000ä\x0010VRN\x001f\x0016r¦I×ö\x0010ôîÈfÜ³ÊË¬\x0019ÓÉr0å\x0000¦s"]JÁ\x0006
÷\x0013KAµpîã¥4\x000f©uCzVl\x001eÏ\x0006v\x0007Èd(ë`Úd3qn%Zò\®roKL;ée
7'Lx.¹ÉUZ\x0003f|Rê	¦{¡g×û¿þ?H[\x000e\x000bj©0ÁÁÁ¥©Ë@Euøê5ß3\x0017!Wn%ÈS\x0003Ú®°\x0001È°e¢ç\x000f \x001dù5'·\x000bTÔ­cô\x0005ãÜühc4GÉõâH\x0001\x0011j"£ªàZ\x00199/\x0018ùÜ<nm\x0016
\x0012ó¨â8¢\x0007FÕÝÐ­¢\x0014#JA1"@ZÊ@/%gèÅ
¿_°ã(eI)R$~\x0018JfR»M\x0018KMW?¾(ya\x0014E©»]7§\x0002}*ô	ôXºÆ\x0015³äuû!¹dózÆyÝÏéxÊç\x0000NÔ\x001f\x0002§\x0014Ùwi\x0016^OqúY\x0014'<°Ë(Îínsüpÿû²&<rcQ%ÄÁH­\x0005%,snµ¹\x0001ÅÇË¿,xiüÜ"ò3¨Ñ@á]LÙ	Cê\x0012Ölõ
o#,!?;Z\x0011ý\x0011%\x0015e#Ý@Ó
Ìö«E!\x0019e±s|Üá»nLípçø°Ë#îÅçl#×sÌënLËéyÆÓî\x0006­\x001cø¬ELz ?Î!?¬Ê\x00149cé,ÎyÎðä5ïk\x0003§P³ÐP/JSèõÃî\x000eþ|·HÊ¶õs\x0008ºë8É[6U'ÛðJgä­º»ãõåö\x001cþ|wry¹àq\x0017ó ²\x0005û¡á¼KÄÚ¥wö\x001a¯KaØÂ\x0001ß\x0005ì\x0011vãC\x001cÎ%\x000cøØm|tÚT_Ä¾\x0018b¿nØâe¯½B+\x0019ëS+ñ<%~\x0008bí>Âû°ø¶|QÕi·1PMö²Ô\x001a.+êÁ³í1lº\x000f'ï@U%ª\x001aB"TÎ%#²ÝlIñv\x0014ÕÍÏ\x00067;\x001bÞÜÜ=1û @Ê8Æ-9:ëL\x000cSXº¾^ÃKîf\x001e¥'ºù,Kv(dø§'»V~¥¡yÏ\x001a¸­\x001càf¦r\x0003\x0011h\x0004>d$\x0007Ìú¾iS\x0005ê\x0003'<>,ÄÈ¤Voéõ»°¯øUÝ3«\x0019Ü@O\x001fÑø\x001c®Úmx¦À3ÝxÁ|c\x001aßå<u¼¶d\x001fXõ\x001a¸â(t3·[\x000b]ìtÆ£Ía@D8\x0003®\x001a½é[WüøÖm\x0001dNâÃ¼S\x00032Z\x0004XK+n\x0004,w\x0007ïÞ\x001eÊ$O\x0000ÔØ\x000e,\x0000k¶\x0010úi\x0001,×\x001fï^*ìß´=lØ¾È\x0007±5|«jFX\x001b-\x0007Ðv\x000f`Àp6{Òå\x0006g"9\ÝqÕÂçJ>×Í'¨¾#\x001c
dæ" Ñ\x0000Åº\x0001tå\x0004»î	\x00162ª\x0017\x0000 Ï¥\x0014RSæ©²5K¦\x0011PëÉKQ$qòÝÀ"ÄAT(=\x000f«n`å\x0017¼j×sÆë^F¹M\x000e²6
âð5'£=É0\x000eb^ÎòÛý÷ßn
Ý9­RÛ\x00150\x0004Ã]b=^u
G16Í©1¾=yÿöl1t8'û9pÎ¶s\x001b§aªÈEÕ4ÈQ¤Zðö®Ïv#§ÐÅx
=2 VG
Õè\x0017\x0000Ù4çÖ³ÊÖ#cÍ R\x0016 R:PRsèÀ\x0010Øf\x0002'ùX-1°
TÏjDÂ_çá¿òdl\x0019ºø\x0004´(\x001d­ Ã©­è£\x0017oÞ,CÚèj@Ú\x0017¼ Ü\Þ,x©`1É¨\x0015\x0001\x0011'î©L)ØØè	ðVÕ®ë
40«ûOQÊ¢Ä3½x\¤\§g\x0018f\x0008ÒI.cq81qKNDél|\x0012\x001aÞ¡6Ñ)!\x0019	©\x000cz$aôDél t±é$\x0010B!\x0015÷³3Q.Î®XMx='¼î#ô©ÿ)\x0010\x0006ÓÖ¥\x00196 à\x0008Uõ²n"\x000c;ù:\x0015L·\x0008üªw@W"Ü%XÌ¢ò´KêÉ\x0017ËJÌÂR¬Ã«ýÍç»Ý²GÄyÆðW0\x0014éQer`I×ÃÍÕÉéëómÝ\x001b¢ìì,T¶8\x000b¿o>\x0000ÈæøË¿þß»%®bÒ°4ÓcN\x0018¼²p¦¯Eßo>ÀÏðóyÝ£8MÁi\x00069Qÿ
P\x0005Ã\x0006\x0007ç9¢ºZæE\x001b*ç\x00041]è\x000c¼ÜßÞîÿþ}\x00192|?rÿ~
5ÉÇ´Z°)*\x0005à/OÎÎN>¼
Ï\x0016x¶\x001bO\x0018|\x0007\x0006'
"D>w\x001f9ü|~^Öâ\x001aÿDõX]\x0015Nn\x001e£²ñj¶©Ä\x0008ÅN\x001b¦¿¼X*ÿ\x0007\x000eY
\x001cöñAùgd\x0012°\x000bx\x0012è\x0004gî÷â£×?|:\x000fÑT=Ì-%x
^\x001fhâF\x000c\x0019F\x000cû\x0000µ=R9w*½ò]ì7ø­¬¾V>]òu\x000f NmG\x0011Pci÷\x0019p^;×	èÊ\x0001tÝ\x0003\x0018ì\x0005\x0002\x0016¬T\x0001\x000b¥¹f^Û¿m\x0015±	T' £TC'|ê]\x001d\x0000\x0005\x0015ÎI=w4\x0003ró×CÏÀô\x0017Å
\x0004\x0015±ý? \x0010«MO¢X\x001d«8Ãq·È	/é\x001d \x0004cO$1PSlój\x0003ÊbO ë\x0002Y¯@ªçt» s' C½$!/Åô!OÃî\x0011z7N
J(4Ð\x0010nKÔ\x0002±ÜWwU7õõúz\x0005u¬[LÔ\x001b\x0013Úç¢þ8£þ¸b\x0014ô\x0006j©-%$ó\x0005ý¥NèO3èO«V5>'Ã@\x001föáÎP'ó~Æ¼_1Ð\x0002,ú4Ð\x001esJñ Eíëþe\x0006ýËf¼\x001cÌh¬j\x0006QöÏ¶\x0011¿Ì ¿CsG\x0005Áü£sZ\x0018©çPãÔ73ê\x0015ÔÁú\x0017Zàª6ôÈ\x000fÔÏ6ÖQÿm9²/Ú"5¨½\x0013õÚe-Ø<\x0016ÍJÑ´`füéþîÛ¡X¸óÀþ\x000f\x0019Ce7Î
¼S¸ùAÈgjgüéâüÝ¯ÍlÉ@ø-Ù,!®²\x001fÊ
Nîe©\x0017,¡'\x0008å¬F_ÈB¬ïv·y
í|eûG
QÕOZ ªòZ8Ûn^CZû\x0013|\x0013ïDà
Ðµñ	ZR^J\x0011#Ð$¦R{Í4òbüL÷øiMúxR2*IíÒøÍKh;ùl1~¶{ü,£øF,C\;aüjçf#+ø\7\x001f¨Hs\x001c?9¸N9åòüV¶p\x001bßôµ\x001aø×j\x0013 gìä8V§\x0017"iXm]Ìkä+÷\x0007ïÞ  Pê\x00100<\\x0019:r*&5K\x0018åSåø©îñ\x001aC\x0003èÈa\x0007Íli\x0000çI\x0007¦\x001c@Ó=Ú¥PA\x0000\x000cïÖ\x000cè´Ërîæî\x0003VêÇ\x0013º\x001bÐç:[ói	\x001aHúKf^UÞ	XN±èb\x0001¶\x0019GÁ5ªÎwÆP·¾âx\x001apîO\x0014¥?ñûæüþáÓ¢\x0003)\x0004Í OLöæ1ÙÓk^µfÎ/._=\x0001'
8ÑMÇÓö
tR 71Ð\x000c¶sµºV:éf\x0012é
OÉm°_.ïï~ß}[N6ðÞØ¨Ö.\x0012h©ÈÃçeyv	syqþ`\x0010.JÝ<ãÀ\x0015ÞvLkI¸.> QÕQ_»y eS\x0017Ã©ÓI°T{\x001b{Þ\x0006N£towpºb<]ÿxå¥òÛE(ºù\x0014w¸o¸gF\x000cpúÓ\x000fqB»Ï\x0019þ/¹ã°4ª¶½Û1§\x0005f\x0012\x000bÌú9¡\x001fn\x001aOmò6
"§`«×ç4ÃMbÛ\x0000¨!ÿ¢æ.D¥1%F0ã×¨+AÝ\x0010h¸
-
C¿\x0010\x0013K n\x0011:\x0002ZLC[)Ú8õÁ\x001ch£¥\x001câ\x0008Zs¹t[\x000fí%èg@0¢\x000eGTS09^y®¶Ní¡\x0000ZÚCí (=\x00168£ôF°_Y¿zæ*9Õ\x0010§¶T¾§¹B	<¨@ %J­\x000eÖb/	3²Âi\x001eÛr
ç\x0005é r ª\x0016²é\x0000-O'1t:à&*D@VFc\x0013
\x0010t\x0007×\x000f*Ë%*¨\x0008;\x0004u\x000f\x0010A%Ù#LÏ\x0013|\x0006@KóN\x000eØw*ê
öT5\x0001â~yêW/Qf|©(\x001b°\x001b±DEÒãÔ \x0013z®z)I\x000e&<N×[N¦È¤×#FÂ\x001cðD\x0019`ãa1ø¡Öt\x000côã\x000côãÀ\x001d
rP\x001c¯&qÐB§\x0000\x0017sµ`b\x001bêüý&È\x0007¹Ú=üº_v£\x001c\x0003Ç,*\x000fv©"9\x0006\x001d½\x000b!ù«íå%Oj¢xR¥/Û4cr\x0016»GL©+FQh6p²ZvNYpÎ½æmLQR°pR\x000b£ÀIµ>f®¬ÕE©äìá©ä<DõÏÝEB(PÁ\x001e\x001a\x0010xM1\x0008ãENÂ¨\x0019ËÐ©âÏÛÀ&ÍÉ\x001fú¢<\x0007âÅ\x0018­Ô\x0004¼ h%¯Ù\x001fx¦À· i\x001a=|ZÆ	|»\x0019/)£æê%x®Àsýx\x000e®ç-æ¾\x0006<M\x0019\x000cfÝìNkÍââë^}V¢²²<©Wx­(ÇËÕnF@^\x000c çÝ#\x0008á.\x0012 Â6¥\x0001PI<;¾ÐÉ¥\x0001°Ü\x001f¼¬Òo!IÅ# 'E<6¯uì\x0004Ôå\x0014ëî)vÜ0VûÔI0\x0000\x001aC\x0012|^ËÚ	XnaÞ¿Ã\x001aÄ^UÖª#Z9j^ÙçK<ßÇèq\x000cÌ\x0001\x001fe!I=/Bê\x0003\x000cöñÄdTÉq¾ëe\x0014tÎ@RÆcP£X~!ÝÈx=g¼îeHÄ"îÞ`·\x0012\x0011ÛÒ¬dü8güØ»W\x0018Õ\x001e9p\x0006£A!r¡øðb\x0014|îCçÑþöv÷bì\x000f,\ÎkAÇð¬zf)ázîú}{¶=¦\x0018ûåë¥=>\x000fbóh-ôñ	wPEàè\x000e|\x0007Uy?v>\x001b
lqà³/Ä\x0001\x000f\x00028ov7\x000f7Ëz.PÀãÒY£ÃØé@\x0018Cï¹\x000f\x0001B\x0008çÍöôòt!\x0010å\x0014Q\x000e ìô±Ì?!ÒÂ!¢8(ã,3~0¬ù\x000b\x0011¿oÞî\x001e\x0016{y\x0005bß<;õÓugÌ^h;ï\x0011tï7o·µþ``ÈÌ31\x000b\x0005[A?»O»»O\x000c\x001e§æÂ_EÊ
÷\x001eÎ¯Ts5rla¶Ù¿Ú\x001f/$ü³\x001c\x0000%\x001b\x00014\x0008\x0018ì¦\x0010\x0006ÔÒ¥·3ë\x0002t²\x0018Aø±\x0013\x0010Ju*(\x0013`\x0011bÒ:ÇÛÎòùÃ®Ï\x0015\x0003\x0008?vòyá¨IÈGÔ?\x0012tSW\x000c ºî`£ï®P\x0005,2yqo$&\x0000;Kqváæ*A]R{DêÎ)\x000e\x000e\x0003 d¥ `Î¬uC81hh\x0010wÝ£ÈaèÒ(2ªÝ±ä¡4Ý×?@^wBJf3$È¥\x001a-ê*àäÜ¢éFüø\x0003âÇ^DÎS>)£ÏudÌäÕ8×è;\x0011\x000b!\x0002B\x0004}{Z)K®n\x0017 $*uçyéæµ	Ý×sÆ¾©\x0006Æ\x001c1
óáWk\x001cEä\x000fEÊÍ|^lÄSúÖ\x0014ðîþn÷Ïe@é¨çi¬;ÀA´ä\x000bá~Þìì\x0000x~q¾ýó\x0013²\x0004_}
B\x001cñìèÂ\x0014a£9^¯âS%êçc\x001a\x001cØTn:üF\x001eòÅë¶C\x000bà´a!O\x000fÑ>@©
Õã	E*ÚØ÷¡ì*>[òÙ~>*½±+Ä¦ 9XÉ]ý¨i\x0000\x0014¼\x0018@1·\x000e\x001b\x0000Sï\x0017\x001aA\x0002T"\x0003ªêÒ\x0002X.AÑ¿\x0004c$Ü#ÂáÍl5'Aîæªr}º\x001cÁ¹éÐ\x0000\x0008\x001d[	P Úm8ùL^óX_\x001f -\x0001m7`°ÿ(SõÊM\x001f\x0002YÁ'Y1ÃuÏ°äxÚÄ\x001eBæ\x0011\x0012$ø<ã¤\x000fO\x0014Ã\x0007?öâAU¼Îã¤\x0010¬bä\x0000YyÆ(V\x0000*Ö
È§<ðfBuI\x0019#·ó4ô>ÀòQýgL,I\x0013\x0007@¬H£4ÇÀ·j\x0000MÉgºùg ¶ø\x0004u£\x0014423Ïaí\x0003t% ë\x00074\x0002µ\x0003\x0003 DaHË}ày\x001dD\x001f_y\x000b«þ[\x0018~S(Ë\x0005ZÜR®X¿?\x000e¨ËKD÷_"Á\x0014Â<AP\x00150i\x000bsøOâ\x0016\x000bGtòé¯\x0000Ã£\x000cU{qñL[Xî¾ä\x001c$®!È\x001c\x0001²*Àí¼\x0016¶\x000fÐ3ì{gØAz?ÜÂi0ó}ÝGÓÀgÊCÚt\x001fÒÁHa-âi0i	ð¬µ>Àò6Ý´óPíLÊ\x001b\x0014°L\x001cÌyØ³\x000f°<dL÷!\x0013ãÚò\x0000òÂ>+¸y±K\x0017-÷°íÞÃ©u\x0004Þ"á¸AWwXn\x001exï\x0003,¯9Û}ÍE]MÚÃÜâkÓ{áUKÐÚb\x000fÛ¹°
Ðæ·RæË)^`R¯à+Ï\x0018ÛÆûÊÈ}-\x001c?È\x0018ÌSy;\x0001Ë\x0019îß"\x0000\x0005F°\x000cÈrÄ¯º(F\x0010~ì\x0005\x0004C\x0001ý\x001d\x0002\x001b·\x001aësj\x0005Ç;ùtÉ×?jbëK
\x001aCIA^kö°/\x001dF¾Ûa\x0004_P=\x000b]°³1óuO¹¢K
¼øÜIÝð\
Æ>Æ;ad)(&ENZã2E\x001ad¼îeä¹ªÎps2øAgr¤æ\x0002Ý\x001fç\x001f»Ç1\x000bý\x0018è?OãH
|B³µæz\x0019§Úp¡c.\x0005mýÌ¸æ@TÌë1ü¢{=r(²ÃtÜ0×I;¼G$]Ëº\x001eÙid¼3ö®G®9äa¦\x0010<§=#s! W«¬WegûZý\x0010|jx¢8Fí
â¤q\x001csq¥}¨ìl_«\x001fbO
ÖåÓ\x0011h%2Ê
»ê\x0019%t9á\x0017ýã(%\x0006hm0øtè\x0017ÊhgÝx=Gì\x001eF©é-\x0005yá1Às\x0011\x0018_õZ6l¶\x001a
ë^ÎkuD]W
ùäXN©^x=Gì\x001cÅhIi\x0011T1¸Ã\x000cyÖ¡ýÐJÆsÆÎK&0zªK´Ò£\x001e_`¤\x0008^XkÇñÓ±ó	.\x0005\x0003cxä\x001bt=°½sÁ»nÄý\x001cqßí\x001dQkh]x# sÄQºæ\x000f\x0019TÝ¿Ì\x0011éEô\x0012ª9SF)§ÕÈsÍ¼9@7áç9áçnBEZ\x000cVf?;ç: Ü¼Ö¼ñËñK/£¥¦Þrjqd¥ºh±ÎO\x00077sÆnO¦7VØ.\x0010\x0019!yóÅnÄ¿Í\x0011ÿÖèp\x0014SÏZ\x001cEéuao@üÏ9âv¯FNÆA5JÚ.93WÔÓ/\x001a\x0011oç·\x0003§Î$I\OßRÌ\x0005Æú\x0018åü\x0003÷´8ÄöÂ±£ð\x0012\x0014á ä\¡»ñzÎØ}QÐ+^ã(ò%øÆJ7ãÇ9c÷E
§
\x001a\x0013Rü,èðSIÅ\8·ñÓ±û¢2Å­fy®åq\x0007ÛÍ¸3vßÔPçÅ=Ò\x001c\x0018óéèç-Öú\x0018íì\x0010~Ñ½g ø\x0003eÅ\x000c³ÔòÏkóWEÄñzÎØ¿gl~U\x001f´QY!æ?´èfü8gìÞ3âð\x0011qÚ\x0013cvÈÿ ÅÞÍøiÎØ½gXÞ3:	·Æ¹v9ù­3À­í\x0019«»÷c¢ÏPãªÑ/OÙÌ×w\x001b\x0011#öZ·yrè)O%ÂÎXB´ëLÇøyØkÞ\x0002"'í\sãÙB
t#âí\x001c±× p7\x0002(kp,Í´*/Æá0VNÃøòÅ$¿ß¼ÜÝîÅ\x001d\x0008ÚKÜ*aÚ¢ÉM!\x000bâñ\x0011<Ù¼ÜmÏ#Ý4F._LBät^©ÚåÆ¢Æsòè_§Î\x0016cg»ÇN\x001cQ¢\x001dl @p¸A+\1t¶{è8$-%C@Gw2sù>:W\x000cë\x001d:m\x0003\x0003Òi¬=2a{Qn4?Ûè8+Æ³ÞÁÓr´ðxÉ°ðòE\9W\x001añD1x\ô^ð¤cÀdx:\x000b_U\x0002\x0004tª\x001c<Õ;xºvzå,æCþ5³p_#)ñL/d¤Ï«LFBÓIRëóöág
ï>TÀ¨ÒÇ©PÞda«\x001fòºèD¹1D÷ÆPic(E\x0012<.³p\x001b­9UD¹1D÷Æ\x0008/Mô$)nS¾1L9Pä6Ògè=ôt¸ÍtZ\x0019Î¿ä3Z[Ræ5`O+^9·®sn!H§Ô$L´¡vÀ\x0010E[çK<ßg,åÔÿ\x0010ÖÅÑËºÆÐÑ{\x001c¯È¸EÆu#^NrÒÁå\x0016ñÉx,F<]âé^<H\x0007ta]Ð\x0016\x001eG¨Oãü\ ¦Nt½s\x000b¡Zx¸î$t\x0002Û\Û©Í#ç{G\x000eD´ÓÄ`\x0016X\wú®Æ\x0007Ñ8\x0012ÅÐ)Ñ;t\x0001Ï¥]\x001bÌ\x0012:5§ÖcNTü\x001ax²|^ÈÞÑ\x0003wA2ô\x0004#w\x0001\x0014ê;Â«¸\x000b\x001añÊÛVõÞ¶\x001az&c\x000fX+iô3¤#à+¡6<]®=Ý»öÔöy;´+N=Åª\x000bÍgé>ó r\x0003ñÂ;ú³;\x000cÜpãÝÑ+Òoe~Û¸5ø\x0011Ã®|çË¨k q«\x000e=Sn
Ó¿5-è¤#	\x0010å\x001dµÚø¡çt\x001f]é\x00170½\x0001ÈQÀ¨\x000f\x0007æv\x0011oÊëÌt_gÐÚH¡ÜFéßðo¡&\x0016p}¬Á3%éÆSä\x00049@LºÕ$ßnÔº©-\x000f=Ó}èA\x0003ÔÝ§´N\x0011¬T'¶âÛ¶×s¡\x0015Oå»RËÂÆi×ÊUV²)dÓo\x000ehZç\x001dG!JZxbÕ\x0003Í\x000f4Ûû@\x000b×\x0014§v>9Ð\x001a C%Ø\x001bkèdI'\x0007\x0018\x001cW\x001ed# Âdy®­Yc$ÛòÌ³Ýg¢²ÝçÉÂØFÀ«è,´â£×ëX\x0001+YKÄSyô\x0004ú\x0006x%¨Ñ\x0008§gîÆ^Ï@xz'CÏye±§=p­9óly"Ûî\x0013Ù:,Óp{ºmµ6´ò~PèìÃy»äÇ	ôÌ\x0001O\x0010Þ\}°\x000f¯<ôl÷¡\x0017N:ûVH0ªÐ5Go3Y) àø\x0004x\x001b½z9!Y\x0001LÝf¢
Íç`Ý×sÂëNB»7\x0012b%S0\x0005ô³\x0011~\x0013~ì#\x0004QD\x001cC\x001fCb0Æ+©/íæú\x0008½ j5\x0005¢VÉ(µÙ³ÌWmb\x0000ÜÏ\x0001÷]«<ÉÒ\x001eN\x0004TsÎäêIþeNøK\x001f¡0T¨à\x0012Il5=3Q©Òh'ü<'üÜG\x0008©©8a]¶q,·"ÂñvÂ/sÂ/
aÑDÍýÀ¬$Ä·\x0003ÞÌ\x0001oú\x0000ÍË0\Æ(%
\x0019\x0008XÉVl\x0004Ôlv\kÖy\k'³3×Q\x0013=\x0013Ì?êÀUÏh'¼\x0013ö\x001d×`\x000bb2¬·#4g§&p~.Ù
øq\x000eØwZkæ©tD1Ò-3Ê5èýºm¢Ùì´Ö¬ó´ö*ºÄÉt}Â8t5_ãØ3«\x0001\x0012Â;­\x0006UÛ%\x000c'Æy¹¤e\x00088ë\x0008¯çV¢^L\x000bÚÈF\x001dMº5n\x0018\x0000ü8\x0007ì\fÂûì&©#\x001eÌþUq\x000f93\x001a°Óh`R@F\x000fï\x0013C\x0003¨V
 ¯A×½\x0006ÄÆ;Âê\{j5EfÜªp4\x0000^Ï\x0001; 8Æ\x0011ÐP¡²Î\x00008o\x0007ÖçÁ ê\x001eAÈCD©\x001e\x001en;\x000c )R¢ÜÚU.\x00195\x001fBÕ=à\x000fdDH:\x0015F3z}Úu¾^åg\x0017røEï\x0018K:«¹&1\x001c£È¦	ë¢\~v!\x0003aç\x0018²lZCe§Ä`\x0003´NCÂUþY±,\x001bCÀ"¿½Xzºï\x001c¹\x0006eE©ðzNØ9`OcÀ&\x000c§D/È~éJñ\£ÁÍaøEï\x0010z5»ÎCC24»,æríÄ*/-C ì\x001cB¯0}(\x0010êìÿ\x0005¥\x001eô\x0011]Í\x0012&9+\x0012&ÿív·9Þ]ïî\x0016õC]Ø³$Ý\x001er RbÔÂÝÕ4q¢¬÷ñöåö¼.!\x0018}Áè\x0007\x0018Ã:ôd4\x0008:\x000f\x0015Ãâ\x0010è^»S\x001a\x0019§)v)v­á\x0005@È£í,}nDÎçæú!u	90ÒäfÕ<÷U¹\x0017líHÊr$åÀHJG)Ð\x001bêN\x0003õ7\x0004Y=ºqINJ²\x0017¥\x0018ÜÅï»å=ÍH\x0016Ø@|\x0008\x0015TÂ5Cê\x001aÏaQöÅ_¶\x000bÍ¥âðÙÛ.4ë\x001d£rø?¨X\x001cNAMÝUMEïi´©Îi@é>\x0006\x0018a\x0008\x0015é2	Ç\x001fåðjQÙÄËh*Îç´×\x000b{Qäx^í\x001e\x001eÑ¢à £\x00029ê\l#O&ÔWT\x0016ÜÕöòò)º¢Õ\x000b+\x0014vð  \x000eÅ
LÍQÑ0WÕ@I\x000bD"\x0002,"\x0011
lN¹\[\x0005·\x001c÷ê{ªîÁ\x0016:ÍÓ¬sä¼­ R\x001d®BUSèMú-õ×f\x000bÞ4t
ËÎváÍb`rÅ(	­+Z>\x0002)Ì«&>AM®¢ÂCêi µÉRVë¯hõ×}Êå.u"÷4Ð6×£\x001aÿ<u$Ü¸\x001c\x001a'^~ßo÷wß\x001e\x0002ÈâÒS A@¿\x001a\x001bâjjOîûÍñÉù»Ëð«'¨&ì*J²7cóÍù¼_±\x001eÏæ»Û\x001fJ\x0015Ú¹dÁ%»¸Â\x000b¹ÌEÃ¥t\x0016ß\x0014ólçR\x0005êáÒÜf12hª}QlÖÜ4?¸üÚ¹t¹ºzæü0æÐ¯EçB,5?xÛ¹lÁe»¸D¶Ý48q±ÑËJá?t>ìàrÅ<º®y\x0014\x0002½R\x001a¸=N#ñ`\x0002\x000fcù\x0002Ë÷a©Cß'FNvRvõÃ\x0003¶«Fß5áä×4^\x0002ËÁ¬õ,×\x000fzêÍ\¼<TSµU;JMltlH%pÝû,/~hwÑ\x000e&K0Ù\x0005\x0006ª8\x0007å`§Q°ÙÛy(·\x001d¬<(xßI¡$d\x0002§ê/u¤4¬1s?T·\x0012Ìô¡t\x000eG+öp,w>¶?çÛÁÊ#÷aÐ\x0001K¾¼´Ö´Ærêù!±¡\x001d¬Ü¼sWrjÁ\x0006÷x>\É\x001ec?:äÁD¹øEßâ×D\x000b-IËÑqqÈ\x0012\x0018^ü¢¼½Eßõ}ð\x001cA£\x001c\Ô¬)®A.YZa²Ë\x000cÓ°®ÐY\x0004ºò8`Ôò=¾¹tÉÕ3\x0010üÂs?¼Øs\x001fBjÁÅ¡íû(fÅiÖ3`&©·¥º¬¾\x000b/\x001cû¡=]\x0013W*\x000c\x0018,\x0005­%÷¿=åÃw¹Fxª\x000eÕ:Ó¨Ç®#h+y|òváñ1oòÌSçv./þêÞnË#·ó}zZ\x0011@|,]QTµ^\x0014É)ZÇsÓ«HVKô¢È>üèeûj^cîæÒëy\x0003½É<É	d\x0000±\x0013{gU%2·åvU-«BF \x0008à\x000féll¼Ï 4\x000b\x0014·\x0014V¬Ãò.Î±èG\x000b\x0017H§×A.ä( ¯2õ¤Ôd=Ø|C\x0002ªZ
V²\x000chô\x0018Ç»t"w\x001a©µ\x0019,¨\x000fÙïm×[,Ko9©¨/)TÃ±\x0019,i%Åêí]¡«=^bÒl\x0004'\x000f½ëÁ²\x0006Ë6°JQNï*\x001cS7°"oáD\x0002i\x0015X>¾\x0010Èß\x000fI3T\x001fúíÍC\x0011!@±\x001e"1Q\x0008îdDäëq«ýü§ïïñcù8ÍÍ#Í]
×ò".¿!=Ât(ÂêáT9ÊB7\x001f	ßþÛ½3â%\x001aðÊLí\x0003³ØQ\x0019×Ç!¼8ðÆ+V<ôÒ\x0019HãÖû;_®qÜå¥Hc
^\x0008Gë®m0Ywß.~¼ùí\x0001!Y<<ù¤IÛ¿\x0007³¢MA£g\x0017À^_üøè§{Äd:\x0015j*+L\x0005\x001c\x0001P®¢\x0016äËÒýØÃXØ\x000fôÙÍç´»èâýÇ?½ýõþqÑmwÂebv\x0018ôæLSÐDÏã¤=È?þó}Ã¢\x0005ïÍ\x0011Þ\x001b\x0013\x001eM®C"È1ÞAi©4À÷ö\x0008ï­	¯óì	gû#2Þ¨\x000b/Ënn=Þ»#¼w6¼QXNºvèuJðî:è×ÒÝ\x001eÑÝÚèÆ}c,SõE§«C1cq_\x0018ðþz÷W\x0013^9$zí¼èRim×wÄ»kñ~9ÂûÅç%Xu¨\x001fÖqÍçpùX÷ë\x0011Þ¯6¼1ò\x0000Cìª\x0016ñ+î×vá½?Â{oÃÃ1á\x001d"W04<Ñàtu¯õþé\x0008ïlx¹îóp{eÎñKWË+ð \x001c{µ\x0015~8/^Ü|ýüéÃ}§Y¤\x0018¿çÍÉÅ(jº%L\x000bD\x0017Ñ.^<zuýüéÝçÙæ57±Aúëú¤åØtü\x0008J\x0017õÛáæ\x001a<
®kð\x0018à\x0002Ky¤\x0016LT:[:\x0018{X\x0007Î/g\x0011+áf÷\x0004Ð\x0006ç$î&¸:½k\x0010\¨\x0011\x0019.ÖÅ³b%\Ñ+FËµ%»åè\x0005¨«#\x0017¢(p/Sëá´åÕr®7å4¸ Z
%\x0014\x001c\x0003OJd\x000cpà\x0014\x001c8\x001b\iß\x0012ûùiâ³Àqü\x0004®ø\x001d\x001b\x0002@}V\x0000Ûg-¹Nó·ÒÔ·?%¾\x0000¿k3@Ô`Ñ¸ÞÚ'üIéº7ñfàü\x0010Z®½c3Þ\x000c`Ü\x000cÍÕ^ò^haIâ/êùÜ,^+­cÚÅE£+.ö*Úä¦AGÝÿúÄ1\x0013xX¾#\	§
\x0017­Ëµ>%é<ðK\x0002WN\x0004=-pUÃU\x001b\.ÃÐÐ2®îðÑÉg-K·ÑkáPi«7<ìÚê\x0016>ßÕP\x001b\x001fmÛÄ|\x000f/jcßÇ÷æïéãBêz@Ä¹²Ðx\x001báÛº-àèN¢etäÿÅÍßÿ÷\x0007ÿ*BE4\x000b6W¾	ócVíIKdÏþ_<úùÒN8*\x0001\x0018Å1+±¼Æ\x001ff$·ôA¨ÒÒ\x0013î:*P¶\x0002±Z>=¨\x000c\x0005¥UuÒ'°\x001a+*¬hÂÊ8*ÿZT¸hrÜxù´æ¯ÂJ
+°Z+BÙí<4¢ÈE~Û'\x0012]«±î\x0000P£øUd4iJJ%=\x0017ÀÒv\x0014eç´T²ìÍ\x0011Ù\x001b\x000bYW¿iª+¿ú\x0003Ø\x0006®t¼\x0019Ówó\x0017ëßno\x001aÀý''PºÈþrrÐÎËñôAqÆwýè§«Gíç\x0007èPÑ¡.Ëp@LÈ7Òt:I©Ó\x001dAÇZº¤è\x000eä¢!ñ¬íâs\x00197w=³­CË
-[ÑÚr{æý\x000bGk\x000eå!/\x0015\x0017­§+jÑ\x0015ë¢K0nW Õq9¸T\x001e¹\x001am®L+.\x001a-W}\x0011ÍÕ8å	=qéL-RÝc8¯W·.¹\x0000ÈA\x0015s(\x001cL¢t'\x0013¸LtzÑyëª£ö«*BÎ5Ä[¾,Q\¸ëâw\x0015Þ\*¹á\x0005gÅ\x0007¼PYh£(ÔÕÅò±õtIíÔÁø±\x0004\x0018úco\x0001\x0019+ãëÉ\x0004!\x001b¶yá¥Úo¸Nz=\x000bÄ0èNäýLxÚ¡\x0004«Gð¸Ö'q÷Z£ó¢k°çÃÎu\x001b\x001b8+[³\x0017Lx C¡$UÃòEÍZ¼¨ñ¢\x0015¯fykÙÞ%ÓQa`¯c9éM4Á¡C+\;Ç¸f$Tà¤\x0002Òlå[Ð¹Ç£Þ³`Û³"\x00089È\x0002Ý^òº+itv.?I¯ÅÓ»\x0002l»"Ra\x0016!ËHÉ\x0012TtêêÛèPÓ\J$%ã¡S$C-\x0011D.¥La±ÐE\x001d\x0017G[`\x001cé\x001fO4*B¬,\x0018ZbH\FÕ\x0016á\x001dÏpëð@ã\x0015\x000fTà\x0004´Ûé¤ªØàPÃY¿,ËÄ_\x0016\x0012?#µÏ)¦\x000b'#½MtUÓU#wC\x0017Þòz¿ÕG\x0007¢0Oº$-x¨\x0003P´\x0005 Ô\x0011æEEÈ'/À\x0018½àáð 	OÇxhñ\x001a\x001er\x000f2é4Gé×®Ã6\x0005\x0005+\x001eLbß¹\x0000d\x000cé]\x001f7é\x0003#Y\x000f\x0016 K,ÐòKN~\x0012ÈDtª*iÂÓ\x001f7Y?n\x000bÑ¥®Äaå§Pt[¨ÄoO~êv'Mm\x00167æ@ÏË(Àµ-Ò#?Û³ú\x0008ðÍ1à\x001bc8\x0005ÔgÑ\x0001Ç\x0005Hyw\x0003<\x0011Ô5\x0005ÊJéBetV\x0013"\x000eõ%ÒâP>D	Ó®O+½1¡ÑPt\x001eè!1
¡\x001f{< \x001cpþ(±ÒËø1£J9ßÀ Û8Çåa\x0003ácB	Û\x0011\¢äk>&î.+±S\x0004Ë%\x001e&Çý±ÑÏ\x0000^Þ¾ÿåÁ¼|\x0018\x0006	\x001e0ú¸NôÄûmèË«'?ÞÓj\x0010ãÑ3@ó\x0005\x0012º¼úôíËÅf¼o?~½¿\x0008¦å´\x0012½P
1\x0017`%OÑË«ç¯_^<mæûùêÙ«{²ã±B\x001c×\x0006D¨IÆ»&\x0012aÄ0f/½\x000b\x0010B,\x001b\x0010[ÖËcF\x0012÷Ö³ä¤_©y£ÄÆ\x0015c¶36Û%\x001e\x0016ß29®(Æ*\x0001Oï
xT¾ÛbYùîÏ·¹ý|ÿ5iËÙµ\x0010³Lj¡'wÑäYlômûäç«ë\x001f¯®\x001f K,ÙÈÚ\x000e!4Ç/¿ÓhFó'S 
dYe\x001b\x0019Mn=Ì\x001b\x000bY¿\x0018øZ\x0016#dE\x0015\x0013Yni\x0006¾ñ5}\x0010\x0016\x001b.¿M­!÷¿4²CÿË:´¤e$8ìsªD¿Ô[¸\x0016mé\x0012\x001a8\x0013\x001aÔ!)T%&&¾p2VÑÀ5W¶qùq1E]]½¸ ¢,í\x001f{)FY6/økh¿Uh4\x001eDñ:VQ/\x000e\x001fÝÈ-EÝ¾\x0005T\x0008ß]ÚÉ§y:QûþL\x0012ÚÑìÏÅØn=Ü#¸7\x00168Jhå
~u.Æ=­\x0006¸·Gpo-p)Ê\x000f©ðaUè%ONÅ'½õpïàÞà\x001c]/Np¤ÁÇ5Nn\ÀºÚànànMp(\x0017H\x001c×\x001bÀþDÁÆ\x0006÷×#¸¿6\x0004ÊÄ.ÈY
°H\x0010KÖÜâÀz¸_à~ùÃD 8¯õïp¿ZàH±¯\x0002<ð\x0000ÒB_ù¬e\x000b&¸÷Gpïpq6ýBØÛ\x00118í3yà\ÝÐ\x0008çr\x0014ï³\û"$§=pq&\x000fÜ©\x0001Gu$Ñ(rõBµpoà,\x001e8×,g×4)¡7uGoÉÃpé8oMòµ©9òç÷o¿~zÿù¡þ}9\x0012T\x0007ÅÙL)C·eQ\x000f«÷Gþüäñ«çO®ïÉ­ÓQ-Û4_ØÌ85§3#õpr¡Ýè«óîFõó°.ÍLV3& 3¢¯ÁJW\x0001½Tk\x001a_¼° \x0016eÆ²ÁX\x000eå=õPM6Æ*åîÉuå8=,ª4êç÷¿|| (b\x001c A&)æT²Üð¸»º;~òã³{ú&6ì\x0014Ýì¿\x0002Æ4°$ q&\x0016ª¡Ï-§¸«·s%ÜÜ\x0003v¼76¾,{\x0012Edý8ÄóÜUYö\x0010_=ja'\x00171K-Þúåãû\x0007|`¤¢Ý2T«zEjK-D®\x0010îÊ\x0014<ÿñÙûà\x0004\x0014\²ÂÑq)\x0017\x001c\x001e0Ç\x0001\x000fö«éæ\x0017\x0013U]L¬¢\x0003/¢øt¶îû\x0012\x0018g¿r2aÅDWíÕv\x0001$½ A+¬ÂÐ\x001d
AïÈµ×ÑUe»j¶\x001dÁºÃK<E±ÙNº:Ë\±\x0005n.Ðà\x000eÂ	/[ÎuÜÀ»ãB{%^ÐxÁ\x0017T©Ä
=\x0016Í)§t2¦ÝFÎúiéÆßË^¾;Ý¨h\R([
\x0017´·\x000bvw\x0017å¬ 9×]\x0008¨åR÷µx¨ñ¶£÷;Á«åäQò³\x001cï¸S\\x0007záuáQÎÈo¡\x0010¼<ôLzüxû]xYãe+^îø1ÐÈ«N\x0007â­;ô1Vz<õRÛøp§­ûº842R!åþu¥g\x0000`×Y«Þi;ß\x001b#ß\x0010øðí\x0006DwôÆØØ\x000e\x0005\¤qÿ3)\x0018ß¿uS\x00101ôX½è¦ZÄ`¸S.ægR0~næö\x001aÝ!\x0006]KE6:Æ=\x0007¡\x0002ýûÆVÒEe»hµ]	4Ê±Ó!Gy9\x0008ôt4«	\x000e\x0015\x001cZáHÚ\x001e\x0006\e]\x001bW\x0007ÝÝ*J÷Ó¹|ÔsçDêÃÛïo?ýõÓw÷\x0007ï¡ÊS
ÆÌUÜ¤ñ$\x0001òéLÑ×WO^]|uýêÏÏþð\x0000Ü|J{\x0016Ó­§sYª\x0002(\x000br#õ»\x001f\x001a².)Ó%«í¼è\x0015¡\x000b<Ã²Fù®y¡güA¸ô\x0014ÿéÝ?¾lþý!Ùþ¿ÿã>úüîÓû/´Þä*}÷òÓ¿|úøe*£ÀB\x0015x\x0014\x0015ï%f²WûCÛÅ\x0013ÒËçÿøüÙË±Ì.\x001e]ÿðüÉË«ïÞ|ûéãÇo·ã\x000f§D-ò
6¢Â=\x0008B¯K¥º\x000e\x0012Áòãì@j\x001eØ\x0000h\x0008ÙDÝ3l$Ò{f+M­¦;Ú6¤\x000c=0"+ñÌT¨¼[iº\x001bÞÔÖ6\x001aëU/\x0004½ \x0012µR0Ò>¢¶\x0012(æ\x0012Q¥1¥45Äì@jIY±!4=÷6¢.+ÛWýVê>#Q\x0010á\x0011)tE!bòã»\x0005Õ½o!Qï7ºÀ\x0002V(\x001e\x0017¼|·.7meúç¿ºü)rð0\x000cO~ûÛÍ/ýâêÕ§o?Þ~ùôáË\±\x000b¹\x0011W[9ýã${.<äÀzòÓG/_ö{«WÏ__?»zùüéË5píoBÿc¥¶6¸\x0004]HèÐåéÙc/\x001dÈ¸ÁtaêÖ'Ó3my±Ý¤½2¤¼®%Jm×\x001f^p\x0001I­è&Añ3Ðµ¿	ýÙvÐ1ÉvÜFt(¦Ã|\x000e¸¶äòeGWCMç»\x001eYcÙÕsì	ºì+\x001b¾kÀÞëJ{"ô\x001bÉ\x00067uàô=ëfºOßþþÞÿ­ÑþíéÍÅ\x000f7ï?ÞãÚ0NÒ<ÁÓ+ìÙ\x001cÝÑ·?ÑµÐÌ\-ñôÑgw»´¿½ý×÷oÜ,h\x0006ºxùéý§»\x0000wür\x0011Bj&^.
rpUx*èÁ \x0017/?yþÝÍç··ëÿÎÿÅT^Ä\x0011çá\x0017\x0014{>jÑðíÅÓ÷¿}úöåýÇ;íÀ±+
Õ
\x0010\x0013\x001b¢öÈQ@\x001eµ(¸yø'?=ýòÉ³;­1 Â\x001c*\x0018 xP}\x00012
lÒ¡¦9\x0013[¡`\x000e\x0005ë¡kv\x001a\x0014ÄæÓ4C'P!íPq\x000e\x0015×C¥Ê±^¨\x001bï¨ÿ)ñÆr]¸y#\x0014Î¡p5Tî\x0012Ò\x0013\x0014Kß7Wcå3[Û7B¥9TZ\x000fÕÌ\x0003}¿Q#ªëÇrÛb©\x0012v¬©<Êë¡hnc\x000fù\x001c°äüôk>ï|ðq;TCõkª¼|Ì9ÏÌ¦ÓO>_/*Ù\x0008UçPu=\x0014U/ñ×K}"Kû-uó×ûK#\x0013_ÿïtÝû$¢rýnv\x001fr¦åÔ±f¥Ò\x001eÝàÒIc¨GÇm\x000bK¾
UÝîÑ½òèÞâÒCokP-\x0018âÒ=3¾\x0017;l¤R.Ý\x001b|:ðÕ-í¿æÓ\x0013S\x0005Ù½e#òéÞâÔSLT¹wvMË*Wp;rê~½W'¥vþÂ1\x0014Ê
\x000f¸c\x0007*§î
^½yÍI!\x001a×kÌÊ¤¢)GÍöãÏ+§î
^\x001dàp(ûiPM¡Îq&ï8i¼rê~½WÏ¤jË¾µ«\x001c5b©°#RðÊ«{[§Ù&\x0012Tù^_4%ø#¨ÛWUP~=Xüz;\x0001\x0019
fAU\x001cÞv&åÕÁ«ÓpV\x000eªBèÎÍU*ºß\x0014~\x0006=4$?^7_Ü|¾y÷þÎ¼.¹^"APTÁË¡\x0002M\x0003ëiLí\x0003Mæ\x0017D$5výè'wçs\x00025óT\x0004«©Zv K½DÇß¯¥V[µèýøâÚ\x0000\x0015T^o*\x00125zÂ\x000egPÇW ë¡f\x000b½AÍ\x001eÏ\x001fª7ªÂH\x001c'\x001aÝö\x0017ªBªë\x001bH-
l(E\x000cµ
Ã
Ãzªæ\x0011\x0012Sa\x001a/°÷¤ËÙí\x000f£¢ë©\x0010ù2/Ðûçî@lpüj´ªªEU
*¸e´ùT\x0004*ùÍ¦òNû\x0004·Ú)à\x0014 \x001f°øò®\x0006Nß\x000bÍ\x001cÞ\x0005ÊVóÎ³±\x0012?i©A©ª@m^ëÁk§à
L!ËPÐÛX{þà\x0018p;\x0016j,Ã\x0017Q)ô\x0005s\x001f\x0017Ú°j\x0011¬´Ý3\x0004½ÚÃúå%»®@Þ°|í-ª%æå\x001bù

\x000b²²\x0016äõÖ*ûàKòXNâAæX6û\x0018\x0014V\x000c\x0006¬(Íêë=vIWzLc\x001b<¼­Ç\x001a+\x001a°H§ß\x000e\x000eÏ¸Eçâ6;­X4V1,yc¾Ø«Ú[óæw6/ø¤=i²xÒþôÞo=&È\x0002\x0018¾Ùn«\x0004\x001a\x000b\x000c°9ø$© vMÈö	§)T
n·\x0016*÷ÐàL]îjd­*wÙÍSHSüæ\x0005ÂÊÎàµðpqLeNüØE.p{äá/o¦ÿêy¤E¿Y\x001b@äØçô`\x000b=\x0007[©`k\x000b[8Îtd:>¼¹ýüõâñÍoßî¶\x0018%Ð©ßÕN\x0013\x0015(á¡\x001eìÑS*\x0018ºxüè§×+ÀÂ\x001c,XÀHK©\x000eAfmÀ2Õ\x0011\x000b\x0018Ö=`0\x0007\x0003\x0003XÊÜ«K\x0016½l³ýz\x001a½6A({Àâ\x001c,Z,æ ·o40\x0012¥Ì|\x0017"ïK1\x001e\x0017íØÀp\x000e&y¹ù9\x001aD;\x001a¨5ïáJs®dáj\x000b\x001e3\x001b\x000cå\x0014£ÜHÆ\x0018Â\x001e°<\x0007Ë\x0016°T¤²¨-«ÞL2½\x000b°Óìv}É2\x0007+&0ßKhí\x0017	VäJxí'Ø\x0003Vç`Õ\x0004|\x001eA¨<B,Æ~\x001fðø4qyí^-þ^Áûù
!§>v,Vdñ\x0003Æ=dÊy\x001fã^ÒFÖPø=\x0005äå\x0010\Ú\x0005¦Ü·ø1zî\x0007eûØEþÈdR¢	\x0018p\x000fòcÞäÈ\x0010å¹'ÐÃ
QåÍD\x0016jÞµÌ'ó&W\x0016±«^ÒÇ¬ã\x001eµ"ß£Ò|¡=dÊcxËÓ\x0018Án³4Èj¯¹kõëlÚ\x0001\x0012­Þ·'eH(ÛSvAD¿\x0005Ð»¢£\x000cz\x001f/x/>½ÿøåöë×÷7wF±¿ub
È5ôÇÉfÕÇ.«nÅ_<òìåÕ«WO\x001e=Ls*´P!«\x0005Ära%	K'\x0008\x0006°ÃÓd.g £÷^×Ýìä8\ÄÔß¬\x001bXÈ'\x000f±\x00060T`øÇ\x0001K
,YÀ¢ì2¦i÷*
D¾\x000fkdX÷eµÈ²i¹Èµ¦Í{¤K^d!£ÁÉóõz0¯WÿtÙºZÞú5>¶$+91FYþ1¼V\x0019È¼úÞ[¾&MÃÇigú\x0003Y¿¾ 'õ\x0011\x00164m4o2Z\x000b\x001a»Í°LS\x0010&²\x001c\x0006ÙÏU;³úYhÍ±\ÊpÿoMþ¿1æ# ó\x0011p¦\x0013\x0000¸·r Ýü¬öF£½±XÍómÆdµ,V\x001bÞv\x0017Zróp\x001d.ýf=\x001f
)\x0011ÓùiXD3]í%þä?òI
Å\x001a>Wñè\x0016¨m\x0003ÊR¨\x0019Ú"6;¡¼Ì0\x000cP©ï \x001bÍÓ}Ô\x0014\x0003UõA¯©\x0005pêh?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x00011¥þZÏs\x0012W %ql&ÖÜþ-)p./rAPWã-Ú$âm3²Å\x001b¿\x000c\x0007ù<¬\x0002\x0015[×î\x0016hYCËvhÌhql©÷9l¾ÈÆ(p5èë\x001aúºÙ\x001e»#KæXæZ8\x0017`eý\x0017ÀmÊq]+G3ò7T\x000e[+}Î\x001a½EÜúòXØ:ó¶ä\x0013I®à¿£çt·.Õ{Bè^\x001aÊÁU¨r\x0015O³í[Vaò4ö\yHÏ\x0010#sÆ}4S*Çæ®Cëx±Û¶\x000eKY°p\x0002\x0008&8S\x001c¾ÚlX)ñ´\x0006®e\x0019\x0016\x0006r

;RXâ\x0012\x0014uø8Û°\x000e[®ãi	AK.¨ç,AæÔ'«»b¬þÃÂÂe¸r\x0019O\x000bâÚöx eX½KvìJtëÒëðå:VD´|\x000eÑí\x000eO\x001eÍ[Õ\x00156IÅ}s\x0011Êe<-kY\x0006%@\x000bî1\x000c*ÅÝ\x0001¾Ê\x0012b¹§µ\x001dm_¤ñP\x00128«»òHÛßÛyÙ:ruô~O\x000båZ\x0016"ñ7/$v¹ÊqÁ«\x001b\x00185²l!µ\x001b_Å\x000bÓuÍ Õ;<É`§\x0014ÜÌ]GåÈ{ê×ç¯\x0003S\x0015U\x000eÙ¢Ò3\x0019¹¡µå+,¤òä=uì-\x001f$æ»\x001bðéÇ°X~¤tª?ivá2*OÞSÎÞâ;º>m
/")7+éTT
;w\x001d'ï©joYG¤\x0013p\x0018{S`ïMÎ¦ÿ*zUùòêöÆlqjR!xXJqJ÷\x001fD\x0017.£rå=Eîmõ^Ô\x0003^F·ó¡+cù\x001aë¨|yO­{KA¤¼[«ºÞ¾\x001e»(^i÷\x0015NP²òè=5ïMEE\´uE>ä®£Ê\x001d~¿\x0010U¹ôÚ÷/â¹}<ú\x0014´C°\x0012 /Ä÷7h\x001c_È@~\x000b­¢òç=\x0005ð-ÃS/\x001aÌ,4d®¤å^4aR\x0011ÿÜ¯Q\x001fÌW9+Ëý\x001b\x0015Ì#Ì¹\x0010X}
÷¡*7¨Vq*rS\x0005\x0005G(I'AÏî\Ëþ\x000e\x000b\x0017RùÁªø\x0016÷¡¸Å\x0002r*lÆÒ\x001eö_E±*?¨Öññ\x000fR\x0010`qyíâ+ù54«r=eþ-5té>9kVê¯O Avõ5>Hå	Õ*0=LS\x0019Áo\x0016\x0012¹õ6ýÚ\x000bì®®ìnOÑËçà2«¼:âó á¯¡\x0006fA-ú\x001aº¾H\ãøab7ËHáXiú\x001aÊ[þ\x001a_ã¦AW\x0006K¯e°$/$â+LÞçÜ\x0011IÛþ7Ú¶\x0008\x0011ê¨ø43ï·ß·°\x000eÌ6e¼ÚNªªðÂzêjÞSCô |  
ÖÖÿúúÍ1À§|ãÍ«ãö\x000b\x001d±.u3±\x000fTí©c9z
ØïkEìï\x001bÑBlJbÓLk\x0016±\x0016A\x0018$
%\x0000\x0011Þ\x0000|\x000e°´ûY\x001d¶Ìêx©^_>NÕ#;ë\x0000£î\x0002ØsòOà=ö(þ\x0016ó»Þ\x001d&U%©j!:Ò°\x0007pE	¤'ÝJ×?rgt8÷ÄîgrØ2c\x0016©Îï*h°\x0015$RK4ô®WcçÔ ¦	\x0014GPää#¬±J%\x0003@J%V\x0012»ì­ÀiKNÛÄé¹3p
:AYÜhDªWÑQ_ú\x0006P\x0017çYÇØ{Ôfóê¸ü\x001b´r,\x0001b2i(ICH1!rä0åYg*\x001eS.E¿YK\x001aKÒØD
ÑB\x000eãà lé)ÕzMÃT«|ýî.?ÛRÑjè®XáP0Úù;T\x0011õ\x001a_Öf¿Éî§QÜ$TA\x0015ÐÖsWD\x0003ÿÕUH+³/ì¾\x0012&¦ræ©Åî-¬©ý½ÇöP\x0007òál}Ý9¬¾RS½³9eÚã\x0010L6§ëX)YSÙdOâ~8
§\x0010)ÒS.\x0015\x0003®b¦¤«P]\x0013*ög"Ó¯¨0\x000cïÎh°\x001aÎ\x0010òõ\x000f¢V¶_¶\x0018ÿJ\x001bã|5Ã¿¿Ï\ÒÊöË&ã\x000fV¦P)¯éÎ\x001eQiâ=æ§¬ª*;¥ÚìT×@\x001dPC.\x001bFTÛ¡ö·¸Zù)Õä¨´SlRá BÆ?ZÚ\x000c±ö*¾ß\x0017¹m)N¹~ÆJ186\x0007þÛ¦xÚQ\x000bß\x0014ù{§#\x0007\x0000ØHaP¥\x0016l|Öõµ`}`¿¡\x0016\×ZÐ ÙtþË\x0017\x0001I\x000bòdiÛuÑ@5XG\x000b¶µ\x0016<gÁÊZ°²M°\x0006l¨`Å¡s5·X7²¿½à|ÔmÚb	D¾ÇÍ·\x0015\x001dWj¢N·\x0015q)\x0010Ê×÷*xÁ.÷/^l?þ6å&\x0008çs§2\x0005\x001a¡s! 	{ØþlÖú*èÅñÙë\x0019~Ä¬Kæ'×mÓ­#\x0011\x001bl¡5×jÝ!÷OiC.&l%èëVjï
E´F\x0005\x001f-@Ò*pþB>êÊQÎ4KÔÛfY»Ô-õ#H\x00126gñ÷÷\x001emµ¨å÷!jYZ.\x001056àV$jêi\x0018!î¶b¯å\x001d÷\x0006¢Ã\x000føZö5\x001e@?nÞl'Y:,è
pñÔ¥\x001c½â\x0012zØÒ½>¾|yr¶ys<jêâþ-}\x0014|Ý9UI¾F4Òë|	¬¤\x000fÊö'2Í&µ%©m"Õ"\x0005\x000e\-ÒrÇ*O\x0013³X]ÉêÚ¤ï°y	ÐØÔ@/\x0000*×\x0002Ê~óYù|ûXóâ\x000fæ#;l
}vÖç!\x0010ö8ê\x0010k|ìÏ=j@.çb&düAù(¬£y´!H9X~^²Ã\x0017aS·Bí\x000fdTÉ&ì?=|ù´ùxûióâánÒ,I¡»öZ¦¿b\x0014dyT-æ\x001fôyW3|uñîjsvrµyqq:V¯ö\x0019ªd#°cyO¶\x0015\x0006Â\ô&gvgû»E7³ÛÝ.dwôVf<ìH-IîÜÛUõ'FÌE\x0017û3<\x0005Íð¤xù\x000f\x000f7¿Nqz\x001aG&\x0005ÕÝó(~ÜÓ|yæM\x0008Ë¸¸|ùÓ»óûOÓyVç|N¹{ß\x0011¡{T¯ÎÜè\x0015ïTN]rê\x0016N¥ø	Ò.ä\x001cjë¸\x0015»\x0011¾?8ÉiKNÛÂé~OI\x001a77&\x001dgÏ¸yR\x00141e\x001e×wÝÀy!~wmJ\x000fQ¯÷ET+|{`Ýî±n\x001fk\x000cûácèö}
wßlïþ6Å\x0011[\x0007¤ØÁ<\x001a"\x0008l\x000eD±C\x0008Ã"Ý7Ç§ÿzT¤ªTó@° YU\x001f¢pæç°AªKRÝBê M\x0005ö
(4òÉ\x0018¢Ëáçò\x0019¤®$uM¤Vs\x001d\x00044õÒ£ÚS+Uÿ´§¹ ¾\x0004õM `§<ª\x001bt`£¤.\x001bÉ<BÏ 
%ixÆ"%hl\x0002uú%\x001are%6ÔDû;Î\x0004µj²Q^Òµ£Á\x001aPï>4ûR:ê® RûËMÉj¸iª\x0012=5ö(kì\x001dyc¤
'ÌÔ¶Å¢\x0011T¶ýûJÎ>ÃG¾5¬Táûºn2©\x0003j!}>\x000c I5tøZ­cük\x001dÐM:=cX®ÎæS\x0017Ê5°dýH7¡Y°ïkØ÷-)©#ï.«Ë@c\x0005Û«±z\x0016ÜÔZÐ´¹¾\x0016È\x001aV¶iÁ7Ù]²6\x0004²Ñ\x0010pe\x0005 Ú<º\x0015PÁî2ì:J kS L\x0001¢ñR6ï.'\x0015£\M\x0017\x0007ö/Ù÷µd[v×·Rë\x001aµI®ÁP5\x0007 \x001an¬\x000c±*Ë5ôß\x0015Í·\x0004ÛÚ\x0012´hìW·\x0004ÚïE®\x0010Ðw+^\x0004=Þßýóÿ>NíS\x001aè\x0017\x0002VqD]>uà\x0017\x0005ÓßÄ"Ãâ\x001dÐå9Î1\x001chUÝÁÆ\x001266ÃÂáJ9zÿ0¹,\x0014\x0003Ãn2À@ÿÆ´»D:¤í\x0012éfã\x0006e±oQºâØËe\\x0013\x001dãÆ0¢	Óqmk[q}|«©Áó\x001c\x001b\x0018+Y\x0017F¥gÐVz+\x00157JÓé÷yæaÀÎJu¡¿\x0008ò)îð\x000b/\x0011WÊ+µ7ØÍµ*çÖa>\x0005UZíú§Î'Þå¬!q³6ØEL\x0001ÍûMâ)7\x0011{\x001a\x0005Öa¢J\x001c$®¶jÞr1v71Z8~×h`þ\x001eI
Ä\x001e«V=N6¹\x0006\x0016ái'a«\x0010G2nç\x001184Ë\x0018/<²7\x0006ä<Ý	ÄjxçØ?\x0007ú)ñ!\x001f§Êè!kòu«ñÂ\x0006ç³×\x0014\x0003\x0002¶ ¥¯¡¥ov8>²Xel\x0003=ÚõOøj`{Ì±9@-sÀØ\°¬\x001cës\x0013õù tÑk<ß¶ÙS;N\x0007A³¡\x001cyj®ÏÓÁ®\x0007}½\x0007Ý¬\x001dß\x000eÚïIÚ7K:JÉC\x0012ÑmStì\x0004ÏHÑv­}¨d
­d;´s¬Óè\x0007)ïÆíÆ\x0017TóyÐ{VÍ\x0006Ç¢¹¯1:\x0016I5§_zÁ±Lt\x0013¬ÇvÏz4KÚp\x0014#ÉHÖCú.FZÉä)½'iÝ\x000e\x001dE\x0017ç\x000b{\x0014³ö¢Ë\x000cý­ÚçC=I·\x000bÚ\x001eç®à[<NDLÆCòù_ûäÞ¹¾Þ\x0013ôwàÄ÷ e3´\x0003+Ì×î:·Íù¬Ñq-Û!÷4Z¶kô·s-j/ZRÍÑ\x0012ì7Ç@>¿l;á¡1Ócÿ	ÛðºÞ­Êñí¶¡Øó,í.\x001c¶\x0019U3\x0019	Ì®d\x0015_ÉÂBÖór´GÒNhÎ6S2\x001cyKO	=¸ìÏØÃlëY~ø]:Á§ÍÉÍÃÄi\x0010Öç\x001a,\x001dÉ?ð¶Ë{\x0018ÉïDÖ\x0017gS@u	ª[@}guwæþØ3sTªSIMIjD\x001axÆ´ÆK
jÀÑÅBp\x0008\x001f5Â\x0004:p±eëq|Ò6É\x0013Ð¨â&\x0006y$è\x0006ÊD­c\x000fôÓÅéJP×&Nu\x0014øÃ\x000bvÄ*:¾\x001f+gAêKRß$Rï(Û
>|j¯
,§Ì\x000b?Rq54¤¡u3e÷¥|Ú×ÊSp\x0003ÿË£>w*i,Ic\x0013iLMwrºq.e\x0004\x001aÑE'À»V\x0006ÈÙµ2¹¨«'|{ÅÛ	4Ó¢ý\x001av´H#APÙ\x0002SÒ£ï$J\x001dÒ|""\x001di\x000b3\x0003µòM²É9y¯è\x0006¨!Ïe\x0008©Õ\x0006£®b¤deóeÑGTOVÊÜ\x001f"¡Òû\x0018ia3´2§²ÉâRÔ\x001f
û\x0007á7Ôs\x0003HWÙR9Mö4hK
"`OuOp&ªÎôÜZÙSÙdP\x00163Â²2M0PW\x0000URMf*¸@Ó±5È¿>\x000ea'P\x001dÖPTU\x0019*Õf¨p6;)*PÛ\x001cGÙî4Û_
:\x0017´LUSh\x001a¢ìB)Pè"	\x000c*ëi\x001c¿HZ\x0005}ª)ê\x000bÑ±
¼©õÝ\x001a\x0018 8\x0017´²RªÉJEí©+3 Ä~6érNu\x001b*dÏ@­Ìj2SQP^f"u´£|\x0007º7URM6*}qúøÞâÔ±$Ò`Øñ¯bMU\x0015ó©¦ /H-<1m!
àc\x0014¿\x00058R1\x001dUWöT7ÙÓ\x0018==´'TÁ÷±Zw[j
ÒÊê&s\x001a¥§Is`¥$gØ¸\x0013êøcÙTÔÊJé&+Áã[	GÙÃÎv>*®òõ«­¯Û¶¾ç\x0012dOéÄçïHWqRºÚSºmOù]Ø\x000fJ)x@ºªP+Ò\x0005Óÿ}ãkLÅî\x0006-òTD8©®\x0011O\x0003äò=Ê¶%Æ\x001e ®Ò
¥\x000e]\x0001Á: ×5èu\x000b¨rÔ<!ßõe©jËwÖ`\x0000VRëZ\x0005Z`ß¹\x0000°VT¥"'×È±²\x0019>Esºö¹iÒ\x0000d]\x0017\x0001ðmJäÖ\x0003"ô7°}L­\x0005\x000b\x0007Õ\x0016É®= \x001cªÍ £å\x001aáVqYÕ}z\x0012mÎ~#ÑªÚ\x0012HÕl
ºÚxËrÑ\x0016tv«¿úì+êZ²mjà<¿¬À\x00063o§@\x0013ø>}dæå,5ØÖjÐ$Ø »\x0003û§p¦»ðc\x0019ÙsìMmdl\x0001¶1%±úØ\x0019YÏ\x0015zàfW¹]3{
kÚä
_>îl\x0001µÝ2<u\x0013D;M0ùù§¦Õm°Rt\x0017WÑóuÖ|zý\x0003¹æï®m½»ZX¿Õ£«a]\x001blä\x0016\x0013 ³\x001f\x0001µ\x0008Ý\x0011vÒÉ`àÅjoîmz¼ èõÃýçþwF=¾ÙÞÜm'±*øò&?\x0008\x001b¼\x0012NÍ×"XXnåÑ»»^_¿=É°Ç/_\x001evoÄm\x0002VÍÀFºÜäÔ\x00188tËÔä\x0014ÔÆQ¤©k\x0011ëX\x0007"¶%°ý\x000ec	\x001cÛ}À\x0003X\x0002v"ßÄxp\x0017?Ð\x0000ªXÖÛnÉ¾ã\x000e\x0019Æ@<®HÆ/cmÿ£v\x000br¥Æ²]áHÏ\x0007\x0006ì-Í0Áò
ý)ÍM\dI¯©¡[:0\x0018<\x0015|ït£~M+¼ÈÍf©-¾%$jL h.õµ¶?M§MÔ7µ¨o¾\x000fQ_×¢^  ßPÔÛZÔ\x000bôã«z+LÝ
æ\x0018~ÆË»Ï·¿nû}ób{óëíçiÆÃSç\x001ac\x0005\x0019;ÇO¤Ö÷¿æ¿<}{²yùÓñë7\x0017Ç/:y;X'ÓÁª\x0012V=sX]Âêg\x000ekJXóÌam	k9¬+aÝ3õ%¬æ°¡
Ï\x001cvw³C²Ý¶ñ\x001a\x0019¨±Nsh\x0019 Ð²?\x001få)ðAÇ°»7#pÝ(`LÉá»ÅN<!Ë8pöSz¢\x000f"ë\x001aY·"\x001b^HR\x001bñá1¢\x0006ÐÞ#~\x0003²¬e3²pJ>Ò6#s3ý\x001dÙ\x001am­È¶U5¾UçbU\x001caÌÄEì×\x0013ñ¶\x0016qëÎûf"VµR¨f¥Pé=Û
Wl¸{\x000fpº?\x000b¼ÉZlkkÑª\x0015ßÎZ¸\x001aÙµëÅ\x0006ÚÙZØÔ¨\x0003Õ4Ý@\x0001CÓÖ»®·^«I\x000e¦ó!Úå>Õ¬-#þ&ë
È¡F\x000eß\x0017ÙÖ^¤ÙS3/âk)ûvÇ*²c®LÁd)ûµtYÕRVÍRþv6ÎÕRví¾Zró}kô\x0011é
ÁèÏ×hÚ}Ûz÷=[«ùe{\x000f	ºìöübûø¸ý0i\x0016\x0015fO\x001a)\x0002\x0018pàäHqÁ;à¼¼<~5ÖFWïOóÕ¢:\x0003ÔÄÀeX!I/I8«HÅÈSí\x000cRWº&òì9\x0000\x0015\x0008+\x0005'C)1Òlf\x0006§/9}\x000b§×\x0001'xævd\x001f»Æi£3G'cÆ\x001236a:iZÜ5Kº\x000eIÒ¤@O'-
u´(gÎAÍ9\x0004¹gâ®\x0010:r¶¶T#IÐ3Pe*PíPÌ³üðy^u]©Gê_f V\x0016J6(\x000fqbÜ5{æ,8ÉÕntÎÔdR]ê\x0016Ò\x0000\x001ff\x0008	\x0018Bé$®SÕ8RR<\x0003ÕV¨¶	\x0015|ià^Sµ¬`¿*ÃH\x0016Ü\x000cÔÊLÉ&;\x0015\¤¡ÃÙ\x0000Pç®ªHúÑ\x0004Q+S%lUT]Çg\x00138_ßuZr¬°d:©ªÝ~Ó¦Â\x001cEBÕ}íÚ;ú±ñ	Q+Ç¯<?VèP<¡ìáI6]!¹\x001ai ?\x0003µòüªÉõ#SU>®f³ºmÏ/\x0010\x001eEgl×XM\x001b¾¯Êî\x0007¢hÊ5Ï
@ü§È`.ûÍz®}a¤\x001afNÀRÓ¶Áz\x001b:G\x0000&SK}g±FZ$Î¬ÙÓ\x0003Ó¦\x0007ßDië?¢\x001cæ9\x0015\x000b¶8d=R\
ëwí~WQY³§²¦M\x000b¾5Ø\x0013¬lì7Ú_RíVµö+Û.)öÆ>Á\x000fÊñ/ÿóÿu|sw{»yóðéó´¡\x0015G¬ñ\x0012\x000bî}®\x001b¯²9>yzr~~²ysqõv\x0002½*éÕRzh<\x0018\WÞ+c\x0005ñcéÇ
ôº¤×eo8OÈY³²ëO::¸ºÞôv)=Nu$ÍÑ«ï\x000e\x0016f¬\x0007D\x0003},éãRz\x0001gM:\x0015{,=Î(Ò\x001ck\x00082]Vz#*ÆÒVîîh\x001eZÜMZêþì¢fzSÑôÆ\x0008N\x0007ÅÙ\x0013è»Q«Ò5ajÁ/§AÒ\x0012x\x001cdû*¬ïÂ)XP »¿.ÅKÚ±\x000eäM«(ÆpÒ*x\x000eg»&ùïf@\x0004Ê®\x000b^òá0uÇh±ÅïdA·\x000b·±Ns\x0016ù+8´ º\x0008ÁNÎ¯ö}oÒùò×Ûßîî1P¸üçº}üëÃÝã\x0014n\x0005æGS<¶mÍ	.òU\x0007¶$ê½ÿéäõé9\x000b'W'?_^\x001eV%´j ìà»WGß=´¹"Mÿ»G\x000b´.¡õ\x0012Ik\x0019ad¤¢\x0011û¯³¤û«Ô M	m\x0016HÚÜ¦Î 1\x0004NÌ+T¬3ýIB-Ì¶d¶ßv¸\x0012Ú-Ð\x000e)xF &äz\x0015/Ø\x0017áEÞjÐ¾öß¤C	\x001dHÚñËÁ\x000e"T\x0004Â\x0007O\x0013û§¡41Ç9~\x001fµkYà[¾)ue¦å\x0002;
!7µ4Vu)óðc\x001eü<Ðs>5øVQÙ<üçvîÐÅ\x0000ð#I¶Ús£N;pi=[Xµ÷¶nUéÉ©þñîöqbkÀÑ\x0007>°Ó(\x000fíxü\x001bXÅÞ×\x000bf¦"ÈÓËÑMUû\x0017d¶ÍÌ.v-xÍÆ¥ñ2î\x001e\x0007G}â,fW2»fæM©³ÍZe\x000eÂxÉù\x0001Zô§¶´0ûÙ·ëF\x000c<J\x0007·$_gZ~U\x00033¶«>\x0004*ç\x0010µ«4u!ÞåFN£G­Ç$j©ìþ! Õö^>|ùÎ0w7@ÿpÿ~\x0002q*Ò£æå\x0001Â½ôÚí½U<4\x0014l_ÿ\x0013âÅ»·éôryô\x0017ç?\x000e"3®*qU+®\x0016:(/á*K1©\x000fØj;8M}Iì[!æàÝÝJÓP(ïE7ë6\x0016ÊO\x000fªD,c318\x0010JDõÆçWe î´8¸9²óe,m¥Ä¶\x0019Yt7°\x000eÛ«$·íb\x0006îÃ@K ùB®BvíÈ\x0002ÍZBV
0àèÍ'Bo\x0007ÒLfn<Y©±l×cð"4¸Ãåu\x000f'M: x7pËÚ ßJe»\x0016+Åw2 ¹9Ú\x000bi(üôz ½Â|b%*Ó&ZElÛ@ ¹£%jD'diû¯Á\x001a+ç¡½ªCÂe¤<ÖÑ\;f\x000féGËc»Ç<?Ô<¬XWÄºÝRtãØ¬O¯\x001dÙ¸±zð7\x0010WæX-0Çì³Kó\x0005Eî2\x0007\x001e\x0006æ\x0003ëjëéÖ­zrÓ\x00054ø<º\x0008Å¦Í\F4HÓ\m=Ýºõ´\x000f~÷îó³â'Såúsì[â
µ«þÏÑÛM£b(kqD6_ç`Hv
Ûc\x001cèÕ\x0000-khÙ\x000e
!2E£¶B\x0000m¸T\x0012Ù«A\x0017G,éí@ªFb\x000eö\x0003åÓ-°zÙÊ\x001b1½l5\x001a\x000fÃ×\x0002NKêÓ\x0002æ\x001bz790:\x001c0×âÍâØ2ORÌ\x001c8@rü\x001búûµ\x0004 5´tíÔøü5Û'÷DÍOÿC=Þvc
ÝÌü-wcñÕãºY=\x0002ïÆ¤\x001eÔ§p¯«\x001e×{êÑLý
w¢ª©U3ô·u1µ¨Û¡¿R\x000b³÷x\x000c?ø¡hjýò×íûí÷F±Iå»!°\x0010Ê|\x000f\x001aãùq~|òùË_\x001f¿ûql¨±Ù¯ä2¢\x001c·5W(î¤¥¬À§ØÄkù®yà:ñ)îAñ\x0012×4âè;Ü]\x000ez0Ý``9Þ\x0006¯+y]+o\x0008Ý;e9E2hÉâ\x0015f-ù7´òºÈó\x0012ç\x0013¯àÆjÊ\x000c\qÍæ-§¨¦\x001cÍÓ_­i"ÁT\x0002\x001a#\x0018`Ã\x0011pè¯l\x0011pq\x001bD¼m±÷N yËÏ;A:q\x001cËé'ã"s6Kùú;\x0010óM-æVË&©ý±>õmÎ¦Â\x0006>\x0007TUÎ\x0015óvOÌ­ªa\x001d7£\x0006òöó¡;»úñ©³Äü¾\x0016óûF1Ë¯ª	9&'1»\x001dòj\x0016Yî¹UÊ\x0010pÞ:ØßÎÈ\x0005îæ®\x000f´p¥\x00197{ÑªÍßr\x0003^×Ñh3\x0004DtØ9 ?ú\x0005Õ\x0015O#¥\x0018µk&\x00103p0\x0014òa\x0015¶_ä¤Q­\x0017#Ã/Ù{¤ôUÀvóóÝ-þçîãÇ))ùQ*'£y<ä\x0003åKÐ\x0000Ðc)ÇOOð?§gg'#ÏR~?íÏW	öó±)Hö\x0012¢¢Ì\x001c#¿ü©ò>òAI\x0012Ù,A$fAG'©IA§g\x0008ù ±+Ý\x0002bE5°^<®\x0010 \x0015ÊAõgd4Bû\x0012Ú/Æì\x0017zOÃÑºY;$é\x00045æ\x0002gc\x0012;,ÁÆz\x000bº\x0013À)L$nÍ©A\x001bs¹wÑs²\x001fb¼\x001dQkê¡\x0003Âæ\x000e\x0010®(í]i¢VK¨:2ô	g¬üöã¥×\x001døH5×|ðÊÈ%VD9Ï\x0006ÜÜäÌwiRa 3T#¶­°í\x0012ìØ5gs<IÂ{ø
\x001døØÀëÙà	l`P|Ãè¼£\x0014b¯0ø ðþ$¯6\x0007)+3(ØA-»Æ\x000eÏ/ykÂ	/\x0019ãHEð|WP.±ÚzNéw ì&oM­dà±ðz6x¬Àã\x0012pc;ÏãE\x0007ÎWa>"Ë­*\x000b®Xpí<M§\x0002\x000b
\x0001µî2:ÂØ|²ÙÜUäª®ÚiÎîw.æê T\x0014\x0003}\ÓeªÊù¨%ÎGw)U4­\x001c¨»ª±/³+·£¸\x001df²ª`ªl¿µål;ïÇælÍ\x0006¯ì·Zb¿áÃ­\\x0010<\x0017\x0008y\x001dm\x0007¾ªÄ+û­Øo\x0013\§ÝàxTÞ&pk|\x001fÇËgWö[-dCä"ç\x0015fÏ'Ç£;\x0015ÇæT«ëÊ\x000eêEì7\x0005¯\x001e¹|yëÐr¶Ä\x000blÂ½a¹\x0005\ðc£;çoÏ*1!oÑ²äv¾²;Cã\ÁK\x000ekåÑ]>Ío\x001f\x001eîÞ-ý7Wm­6Û%jãJµ¡çQÁMc\x001fKÙ@~Sß¬FÎy!\x0005ù1¢Û¹["t\x0015v	¿&¿¥\x0013\x0005\x001f=Å*a0¾¾rÃ§Â]¹ÿüÿ¦uC
)Ó0W«znÛ'\x001c´6õB{y9ÚU }	éçCZ8(7\x000e; Ç®É³u#îS!C	\x0019\x001a ©\x0006Nù9IIÑÍ\x0019éI10±B<«ôÎÒ\x001a&\x000cq¬Ü$Â¢$\x0010\x0016}$§#êîía45;Õ\iêÆ^ð§RªRµ|j7¦R\x001a¼iJ_[p^\x001dógD90\x0010«m-[öu\x000cØØ.nÍ.Ò¾\x000e<@Ù°\¶¢´
\x0014+Xú#IÖ'ø5¿vù.è«Þv3>x¾\x0005ÅÆ3¼·\x0005÷\x0008³Øãv±õ)\x001f©üîYm\x0006¤ÃÅÐÙ zR\x001f\x0001ñÇ+pÞÔ7ÏÐPú¦/þ!«¾eY/çr\x001bÕ\x0011½;YÙUÂt»\/\x0001ûo\x0011\x001f#Oû}ûéS
~|øÓÝýÃ¤\=å\x0018H
æÈ\x001d|P\x000fªirýO_¿9¾ºJ¡Ñ\x00178=¿\x0018MÕû©o\x0011SßZ-i°Êp]÷Ñ["ýÝöZuI¬[à>Ùzôêá<]­:-\o9F\x000b±)M3q¹U
8æ\x0004DÌX\x0001¸?¿°\x0005ØÀ¶\x0019\x0018\x00120\x001cQl¾µñÊ\x0016kÙß:¼\x0005ØÀ¾\x0015ØzA\x000fXÚû\x001aaPý.v\x0016±ÜB,íÞ¾Ë
¢><|ùøðe\x0002¶\x0017Æò\x0003V\x0011\x001bKçT§.ñ4ö\x001fK
lì\x000fõêâÝÙÅ»dY"7%¹YFs\:nÏà\x0015'RëpPEæÑÌ/Ä®¸f\x000eÅnrÔ\x0008\x001a.;±\x001fÚ\x0005üa)\ ÌÙëKàEýNð>Å9;N²F»Þ ¼ÝÔ7\x000b\x0005/4·ÕC­a¥áK\x0003Ý\x001f¬7£_×èßØ­ß\x000bF \x0004«?<ÜÞÞÝßbÛ×ûI÷BðÌ\x0002\x0017\x000csíy°J\x0010ýéQ\x0005û\x001f.Îß\x001e`\x0007ØóÃüªäWKùµ9â\x001c\x001eO/{FqIPýç\x0005ôº¤×\x000béq\x000e\x0016§ )C³¼î&ñ\x0004ÓÿöÞÎ/kíYª>zïúàøÉÌ®ÝCè/×m¡7û^Ê$/EE3p^xø8Wã\|@TÁ»<øÄ[\x001bi«\x001a%G;TÀyáâì0¥+)]\x0003¥Os¤\x0012e7p\x001eO2(\x001e+*H\x0019JÊÐB)(KX\x0005ØdÉãÅÌ@\x0017Ô9e
ÍY\³!¹¼Rù\x0018é.\x001ak=A\x0016¢M¤T\x0015¥jQKy|Ò\x001bz
\x0005JoR
¶gaVG6í\x001eÎGPXh%aR*;Vï\x0015MÄ¬vlÙ>Ö\x001f91ñvÍfLKéëF`£°åÛ§|"Ì[¨(]µ×-íuAM´Q¦\x0014æc}ð\x0002ÊýÒ=¹+Ý»\x0002SÿyóÇÛí\x0014Kïtìzû(¡¨,|Wð\x000b\x0007ëÁûÞ+°ðo7<9\x001e1ð\x000cªKPýAM	j1¨/A}\x0013(N|öt$ò4_\x0014B\x0013
\x0011~ð­\x0000\x001dè5´_'wÅyó(áË*8?\x0018>¸Á¢S§\x0011\x0003Mpf`Êz\x001fµm$8,HED\x0003EÜX[Ì§¨\x0006»Oæ¬¶lÜGñ(0§íæ|\x001bÎX0#Ã+
ÎáP³9lvÃ3?½
]é¨O¡Ð	YÚ+l¥"[Øì²gJ\x0015gõR\x0017¡\x0018¨È<\x0006ÍµÎÙÁl­9¨®BuMRõÜhz¤y 9ÎOSë V[_¶í}@¥ì\x001a\x001b©ß\x0000¢Ftk\x0007\x0002æy¨ªR\x0000Õ¤\x0000x¿DC3
yæ¦U5á¼YV¿HèHvÛdø#7ÇÓx±Î³ÍÀåÀ\ØâEM\x0016\x0015­3a\x0003_ó&/¥É^©\x000eV\x000e?÷ÎQ×2«-;ë\x0016E;@}£>ò45o»¬\x0018\x001e\x00159O
®k5haývjp]«A\x0013ì7Sí\x001a´ì°=5pö\x001a¬b
B
\x001bÚ¬/ÂÀn\x0006säª\x0005lU³\x000eëûõý3Ö\x0002½§\x0005ºM²\x0010jda/uÚ
gB0\d6VìOÿ\x0010yúGwõsÂn¦Ü÷áu
MÁg5jûdm×h²ÿ(ÐÝøá°AU	ªÚ@U×=Xr³@Êä½êo"?T¤ºÔvÖGºEuëÆ¼ã\x0007\x0013AM	j@qBÙ>¾¶º\x0013éø\x0013ÍDR[Ú&R©¹u©í3\x0006ß5\x0017íÏM\x000bêJP×öí5·b´¿ðÛs-¯WýÕsICI\x001aH
\x001c©éÜ\x0012Â î§Rw\x001fß/ÚùÒí7ûvöº\x0004éö\x001f·\x000f÷7RS\x001bÜ|\x0005(áö²{$kXÄ¡¢;¹¼89<íö\x001e%Ù´3\x0007G'\x0003%ã\u\x0013©Á¬ÆIKS\x0007n\x0007\x0008ØÀ¶\x0019Ø)®<RxIï?o\x0008\x0000øPút\x0019»\x0012Ù-@9Û\x0006ev_éf\x000fVüO'%ql'6b\x0003@æ¨Ë[O×À|°øb2³¬vlß~.:\x0016³³h7ÒÃ ¡±lÚèEóÓuÅ¬Á;P\x0003\x001964àÇ;\x0017:è±Þ&3¡«\x001d(Û· ×ÜTAÁi\x001c\x0008¸ºÀÚ¡úóÝ «=(Û7!Îº C89Ru×!ã\x0014ËµC\x001c\x0016ÈÙR­¹ÂQ§2'\x001a¸ØiôÁâþéÌáíÃ\x000b$e3ô=¦v°±\x0013«Ù:U{ív»á­¢\|â&ûì¥b¯}°æi:re6T»Ù\x00088W¢\x001cø?ê½¯u\x001c¾%
]E\x001aª=ÔðX\x0018	:54ÌIÔÅ\x0010\x0004}°9ÈtèÊÖ©v[\x0017ÔNU.çHéÓrô§O71W¦N5:«<r	Z\x0006-i"J0ÚÇhôékA\x0017ÂÎî\x0017
ÏÒ\x000e\x0008Dó4Nç%Ý°4~
\x0014ú`?ÃÈð¹ön$´)çÞn^<<~xøp?-
	9êå HÒt:á\x0017Ìb\x001b\x001d\x0019w²yqqùêâÕùh\x000e\x00121«Yµ3ëØµÐ\x000e2SÀ£ð\x0014ä7«&d]"ë\x0005È]û7\x0007qËã\x0019BìF`ô×Ï5!\x0012Ù´#\x000bÏ¯­8ß'w·q¡ëíûï\x0001C\x001cZuÄØ<&°á ÈåÖ¶ßs·)sÃÔyÛ,i©ù*Û9ÊúÆK\x0017NÆÔÅØRî0ö]åÇÛÍÛÇ)I»ZE'¨+\x001c@Cy7Á
²ÌÑºawònóæòdóæär$]Wî\x0004H¹»Ñ
®Ãf×\x0007ª§\[,k¡|&3Òwg\x000eª.Qu\x0013*¾oçÞFpòHôI¬¬\x001aìÇ6*sXMÉjÚÄ#Ð3ªØE=¡r½\x0019ë{5Ô¤¶ÔÃ):	NM½Twº\x001aGÚ\x0018ÌAu%ªkC½O\x0019¶\x000e\x000ewa\x001b8J\x0003#°®ú\x0012Õ?k\x000b\x0010KÔØ¸­8M_Yì\x0004¥2«£ç\x000c\x001dõhaëdÖ¢m¢´»¶sµUáK
Ü
Ï\x0006E\x000f\x0005 Øál\x0012và\x0012SîßUI[°ÏÓHM \x001c'P\x0001²¬àí$Òb­¬l3W8.Áä¸\x001c+]\x0003é«£N¶:Qz{°Ã\x0019YrÿrJÚ²¦}\x001elÀ\x0016	Vi¼&&Xb\x001dIr%ØÊbÉ6¥¡/\x0005¡\x000bµY³ NÚ\p^[ÇgSa$MiÙ^ïü\x000cÝöÒíï1\x001f\x000eÔ¸º\x0011×):ç\x0015Tã\x0002\x000eºn¬Zv8 s°mb5:×ÖÜw\x0019»ìuZ;Zô>G²ÛZ²m´ÖÒì\x0017¬§\x001b3Ç\x0015\x00070ë80iö¤kÚx1yHte¤\x001e^8\x0014íWYè|\x001f¶+\x001aÅÅY¦scpMçsíÈÓ<³°­ÍB#®Ü\x0005A)/Ø*½®\x001fÇ<_¼×{âm³\x000bØ»Zw¾W²ëÕë]Ç4=\ÓÞ7\x000f,U\x0016þ*\x001c;4z\x0001\x0008~´KÔa^aõÞõ\x0012ÄKÅ°ÒOO¿oá4þqÒ@q,Du\x000e\x000f;!Ä]sN\x001fxM¦ÁPW«7Çp\x001a?»\x001ajÔCÀ¦\x00046íÀpZ ±»ÚÐÛl\x0008×s\x0011íè³\x0012÷ ]IìÑcqEN2óZ!ÀO\x0007\x000cZ\x000bsY±ä|Ý,h!»Ü8\x001f©\x0011{\x000cû\x0019\x0017ÆÊ£æa«\x001a[-Àöt+
Ôg1ûõÙéÑr3½­½ý\x000e´ZÕÐj\x0001ô×\x0017õ\x0016«¼cø;Þä=|\x0006Ûßnï?7Ô#ãØyj­\x001d¨ùË®¶"þ
 ³·ð·×'ço§\x0016$wøªÄWKñññhx´7\Q\x001dCÈ±d\x0005º\^ü\x0001t züà\x0002æS¤OÀN'bñÈÊü¦ä7Ë¿@1OÑcg©üjnYlÿ\x001bÇ\x0015Ør\x0005vñ\x0017ôLjUÆâ98\x000e¤8-áw%¿[þ\x0005\x0014×ò\x0004íéù\x0003¾£\x0008Q÷_\x001d,Y/Wà\x0017¯@uýr½sGQQ\x0013*ë\x0014¼X}\x0017r\x0005á{\A,W\x0010×ØÇ¨\x001eâ®è^su-x³Þ gÁ
º»ÓìÊÄò@Ó\x0012°¯¡£ÀÉÁQö\x001fè,¡öÆÝ1ú3êÇè£¦F\x0016hM¹CHìïn¶d	GË]2SM£¸¢á4*l&ÆKè¿"^²Ê%ËÅ>\x0019"y\x001cÛ¡(ÛGt»¹?Û§a	°÷\x001b¡E['I|Ün^ã\x0012>ÜOIFÑJG´?Ýõ!ÝÉ\x0005R!¬÷è³òÙñæ5Ò¿:\x001fKH{O È­\x0017q[ÎÛÅë\x0018jéá}wIÛ\x001fù÷c\x000f\x001cÀã~ShëTÌ2*~¼µØ,%¿3zn§¤£ë¿iµ-¹í\x0012Y+O\x0019\x0013Êæ!ÞÛQ\x001ezTýç\x0016Y»Ù-a\x0016êÈÑ#\x0019¶\x000f#f­ù¡T^»Ò(k_rû%:\x0012ÔQ¤W(e»ý(XØ¡ÿ\x001a¬\x0011;Øa\x0011vèÄ
çpEª-M÷Ò×ïÚ¸¾E1?£¶{nÃä-\x0008\x001cÓ*IÞým\x0018Z÷dq_våõ\x0002\x0015S\x0001°²Mæ\x001bilnC27ý\x0015£ÍèÛ\x001a}ûÝ ë\x001a]/B·ºK\x00162
\x001bqæW!ÝeàÈ5\x0015F×
£\x0017)\x000c&¯þyNüàâû³5ßÔä7K< f­ÉsæS·Åç\x0017öý#[ç¢°6kB6\x000bÜ/\x001f\x001fîþN¢7&
\x001eØ\x0011] ¤-oÙ¦;1	SÑ¿¼¼8ýWü;ütÊ\x001at¹ýH«a
¶k\x001f\x001a±\x0013P.ã\x000fàþ
K°å\x0012ö\x0003%`¥zÓS\x000e(Í\x0008R4E×Áù@Jðü5½ëB:.-\2þ\x001aÇG,ÃMkà^y
\x0013b±¹k0Õ\x001aö#à5HÓ]\x0002Â±5Zñr\x000eÞ±¿%Û¢5Tº$WP¦`pv\x0008\x001eT¥Ü»ÝÀ½Ûuÿ\x0005ÈE¨JÔre\x0002SðcÑ7xË%±´Ú¶5¸ýÞ\x0003Nì*?uçîI/(FjnìªÑ\x001fÓ\x0013ãQ38µoðµøäª;n=û¸ý\x000e\x0004®8>W\x000bîJ¤»M1\x0006ß½	!ÇkK^ÛÈBáüP\x0002ß\x0019p¬\x0014$CuÆ;Ü^ÜíõÏC^ßÊ£]WË\Å\x001fÈ,Z+üÈ\x0008ÒYò%olä\x0005Oé{©/
µpWÒqÿ\x0018&Ê÷\x0010oÑØíZêÍ\x0007V[\x0004[+\x0015Ö$`Óm¸Ø\x001f5\x0000W\x001bN¶î8\x001c£@É\x0003\x0006ÜM¤Q5^Iîù2
5\x000f¸Ò`ÙªÂ8\x000cD;Ra+i\x0002vRà&{øÖ\x0001®TX¶ê°\x0017\x0001{Ue	<¶\x0010»\x0006q 
ìü=§£Dò\x001a7ÏÞm§åd·­ØPÿZ\x001d8©÷¢ÜÝUFÏ\x0014ò¯µ}öB.³_\x0012òõ³G¶µ*ÛVUþ\x001eOýò¡òg/åXK9¶JÙ)8¹sÿ8qDÃ¯x(¤Ã-ogËx[Ë¸Ñ\|ÓÍ÷¾F~ÿÜ¥®!¸hdÆY\x001e4<Èän\x001bÉ÷I\x001e,±µ¸®­E£ûvÖBÊzëIÙ¼÷tÜ\x000e§a¦Íg#çöÅ²¹Ì×{ÌrvÚð-iTZfÞY±Æ\x000f3·{Ì&\x0003Q¼îâ¸@gî:\x0006BûµõnèfÝ\x0008gâþö×«î?\x0010òû=!·\x001a\x000cc:G"iØ£ã6¤\x0010)¯'áë=	·j²rG:t\x0007>Cl8ÁÇ\x0014AÍõÕ"Çf=¢Û{Já\x001bM\x001eNª:{1Ö\x000bd¦ë»­]ßísw}em\r«^Èn|²Q2_\x0019¦\x0011°]{ýá±
³ß×È­{\x000fP±ÓdO»¯ó} ÉëéÅj½øÓsÕkaë§®\x0017ð\x0003|êÂ\x0017·6ü\x0011\x001d¨æ\x000cóï©©"ü<;\x000fíb`õ:/N.ßþ42õ±cT%£zV[áT%Çc,
\x00049þËíãç»ÛÇôñÿøpÿï_î>~øõÂ\x0008
¿>ì«\Û\x001bðÊ\x000cVý³èÿåÝñåÛÓË¤\x0002¼8ÿw§gg#:Ð±ë]/cÇBIMì6?ìô+\x0008½¿ge3º)ÑÍ÷%vW²»ï½³ÍDÿ~	¾Õ`\x0006\x0016Zçd-¼ä
\x0014ªØÿªÙ®6]ÌA³ý®ðwç\x001527×'zö6éç²K\x0017®\x001bÉªúãé\x0005Ês]+Ï"üÿ\x0007ÊsS+ÏÍw/kÝ\x000bu_v¹-Ji~)\x0014Aw§ÿ¾@ú×µô¿/åqµò¸ïLyLm÷Íwf÷]­ûî{±û{mÙEnËvöðyóéáË§ÍGl&w÷)5\x0003|$T\x0001#¨é¼øG]wiÜ¤a¨xdsuñîjs-åN¯Rk9X\x0000þÿ\x000e®@+PËW »\x0004\x0016©\x001dµÍ÷\x001eSr\x0006\x000bæÌ¬½\x0006]®A_Á+0ËW\x0000A¿ ¯ãU©¨S\x0006Î#\x001aH\x000e\´\x0006[®Á®ð\x0015$½f[©ºR*G[ÙÉËæEKpå\x0012Ü*Aw_!rwgê\x001e_a¨´¶}	¾\_a?Ë.«ÎZjkåá\x001eh
\x0003ÓZ\x0016­!k\x0008+¬!P/sø\x000e>çE MbURºl÷¢5Är
qÝà©ÃJ£1\x0015,\x0007ÅÙb}«$kï¶{\x0003÷¯°áCè#Mf	ç¾Òèo7Õ²\x0008!÷Ó\x001beÞøeóóöããÃo·À­E°Ô7ÓkÈKXÊIõ\x0005~ä©îÝæçã³Ë×'ÿû0©.Iu\x001bidRç\x0003f/!ª\x0013Q\x0007úXÌ%µ%©m$UdXðÙ\x0006\x000cX\x001b©ÌÔ\x0008%Öau%«{Îß¿ìéV¦\x001cÌõx¥h¥¡	{ XÅå0ãm±æà^×¸×m¸¡W/\x000cö{$ÜnvyÚd\á÷\x000bt½­F¬¥TíWÛû\x000fxÎÿêDm0¼\x001b°§Â×|Eã¸ï\x001e¨¶ï¦C¥LíWÇç¯ð¤qq~~2ë÷+u½­&¯µ-\x0000K`è\x0012Ó1ó5\x0017:ðQ©?áuÉ
l¹\x0002»p\x0005\x001eûÉÓ,1\x0005_\x001eqq\x0016\x000c}¹*¾Añhçsñ×ÂÏ\x0000$ÇH\x0005\x000cI4Mh²h{f.âàN(ï|.¾[®K!.IN<íìYúÓ²,BÕPË\x0017¡Â\x0011ohËGpCÛîÎµ?%`Ù\x001a®ë5,Ö¦]n*\x001c.8\x000b\x0003C^ìt,ÂÖ°ßå°µ6Ù¥Ú¡/¡Tn(\x0013¯¡?\x0012kYÔû}÷õû´¹|øòñöóç©\x0019Îß®¢pK
7¹!Ñ¡í|µ¹¼xwvòöíè·¨û?¾@\x0017\x0007Ü'÷\x0017ÛÛ¿ÞÞO9T8\x0017}\x0008«o®»é¶Û¤¶»=¬'ç\x0017ÇgÇ?\x000f\x001f!:B]\x0012êù\x0018â8B¤v@TTÕ\x0005¢W¡g1ÑÌg4º}jL¥\x0012\x001cè®Â\x0004\x001dz\x0015v\x0016£-\x0019í|F\x0017¨ÅÆù\x0005\x0014s	Aå¢ÆÇþ3ð,FW2º\x0006F\x0007\x0001¢\x0018Ï°\x0008}ï¥Û,<_âùÏ\x001c)MV;ðw4ÑÚÓp\x0018ãC»ºY±D
\x000e\x0004\x001açm"z\x001ad
ý%S\x0010¤Î»)y`Éö»l¼½}|DÃ9åôB³	R*ST\x0006ïTäÈ\x0007ôápS·'h8wÜ»¾{s¬á\x0007{Ó_În·Ý>NJ»Á²+z\x0019t8l._¿èHû\x0007«÷Ç\x000e²}svrüóñåpöMG¬KbÝN\x001c¨µ\x001fv¥Êý¾\x0001ûrz}¨;ùd^[òÚf^+ºÑN1°ÑüpïâÁÔ\x0007qµNÀ\x000fÊ\x0008_6/\x001f\x001e¯o§ì5mó\x0011Ö:'©KÓºb9Ùh±ñ»ÍËË\x0017'#ÛQUª\x001aQ½Á <ÑFGåÝ ÆÔ\x001cÎ¡Z¬C«KZÝH«,]ÂXç\x001d5\x0000»@0Î«ñö\x0018ÓimIk\x001bi!âÎ9bÖ\x0005AWFNs_} \x001dm\x00154\x001dÖ°®\x001d6"H\x001dW\x0001Ö3¬îÊ>Ö´þ¹+B(iC+m æÍiÙ@´Ô£Þy3Þ££\x001dè)F¨±Dm¨ÆñäTWÝY\x000b¤YF¨²£íæ&ËµèlvV4ÓÆ\x001a\x001e%ßiî\x001ff6´ö\x0008.Áè@Ýh-6³Ìã¬ôqmV[0äÄ"Ï¶Ñ±\x001aþ[Ì\x0019´jo\x0000\x001f6"»\x0016ú³b[\x000b'A©é\x0004#ø~FZÀæ\x0007òS¸Ñø\x0010yUÉ«\x001aywy\x0004\x001adÊ'.Õ\x001d¸ìÀP£ù¸ºÄÕ¸7\x0019H¼ÖçFÿt«ø­FûüÏÀ
%nhÄ
1ða,`ß¬
ç[84Iy6¯¬´A¶ªÑîy5j¡³õt6\x0003øþR'À\x0003þAíÍãJ´¶Y¼^µc¯cñZV°ö\x0016
'\x0010Ø·\x0002ãm§!`Á5¡ÆQ®	Þ-µ\x000eÒø½»B°õõcXzß¿ÚÞL9ï`´(i\x00168C$5ÐFõ7Ñ)n9Ó³þÕñËÃÈ¦D6\x000bU7	\ê|»\x000cÌøÚuì¿kb¶%³mg¶\L c4\x0000
GÑd{¼ËYyÒ¬©\x001d\x001d%~|J\x001fS°\x0005¸\x000cêø\x0002cÞ Â!p\x001bf7PçÅúL9\x001fW)éã0¹*ÉÕ\x0012r©\x00147¦óÖ\x0012¹Çv@Ü@ÚÎ\x0012K®Kr½LægÝxì\x0010Ä27T
\x0018ì@¡Z#¹)ÉÍR«»ë½¢Ñ\x001eËE<®*r[ÛE"Ç\x000cKE"7|\x0012¹\x0018D¿ªÄ]	îéJ¤yo\x0006\x000c _©àÜ\x001b"\x000f\x0003©\x0017ä¾$÷ÈqR	\x0019\x0016Om»AâÜ\x000fä\x000e5\x0012<,Rr¬|$ò 1<É"geC=¥\x001aÉcI\x001e\x0017ë\x0008Áª³¹E¤L¯Ì6Í7Ü#r|°ÓLðb,¯¡±¼í2óDà¬g\zÁº\x0012¥_Sâ²vËü'\x001eÅi²\x0008Ø9)ìæa\x001c8ÎÌÕ"ýÌÐTÆvv«¹\x0012\x0003|%
vr $<\x0008#èUÍy9iÖÐ¤Ù\x0005÷õÝÄÑÎYðÝ\x0015Â@ÓðB«½³:¬Ë&¢üab:îJ:«Ì¯;xz \x000ca+\x000e5|GÚWãUõº®ñÍO¯­¼Êæaä\x001a\x0007gQþ\x0019ØóÀßþBé¸[!÷GÉ\x0001üÓö·Ûí\x0017ÔO\x0010¯v\x000fù2î\x001aZ\x0004~ôºwGþtüúäø\x001d*FùJÙ%ñ_ö¹uÉ­\x0017pcI 'nmsAK\x0010È{¾vê×çFnSr\x0005Ü©ÓiVi0Øtî\x0001GÄéÌÁö«t#·-¹í\x0012n\x001fiþÆÚo\x001eÀµó3{ì/þnäv%·[Â¬YO<æç»,omyO\x000e\x0014{4rûÛ/á\x0006g#
¥\x000cð\x0005;èbý\x000eý\x000fÅÜ±ä¸\x001d@\x0007Æ[²zó8k\x000fÁí\x001aØf¿!I
1vØ/\x001e¾<^?äô¶	ÜVtu\x001cyÆg
L\x000c\x001c\x0015? ß/.Þ]ÂRn\x001b]\x0006\x000ea«\x0012[-Â6jh\x000c\x000euí9)OÞk\x0001ìaûýâPo\x000b¼Ý¼yø\x000cÄÄÖút¬\x000cJ	ªø±\x0003A\x0008ÑlÞ\¼¿
w/-þÒâ\x001b Mt\x0002\x0007Ì$ÎÀ\x0013ï\x0003¶Æ'Ô\x0001_>\x0013U¨ºYø\x0008¨&8\x001aa\x001cô,UÑÿzü\x0004õà×\x000f%mh\x0013l°\x001e¥h±a`2lÝHu\x0010öFÑ³iQ~>·Úp9\x0004µØl/ûÔUpMÿèù¸¦Â5¸8d0?uj°Ä4»5ÒsÓq¡*\K±×Ò	§áýxû×íýçÍÙÝý»í?¦ ¢éô­04[\¯
µ×Ó\x0010L÷î°\x001fO~>>»9;=uzüoýûë\x001a<q®\x00190¯Ú+ý¬\x0007y&Þduó

¾yÓ»¬Tý]ªü2xúsZÔj\x0011µ\x00036M\x0005»ZPµ®ãzãþ6j
Äº$ÖËä\x001cÓ¨Ï$gÐ@¯\x0019ÆÐk½týCï\x001b¨MImÉÙ\x0019Þxp8¡j8õì\x0004¨Ö¢¶%µ]F-4=vY©v3b;ýè½åm@v%²[,hEÈÑó,OoèNÝá$¾¨}Ií\x0017
:pÎÈk¹°\x000bÔÃô\x001e³\x001b¨CI\x001dQKwD:ùdñB§Ó¶ÿñv>´¬íôRC­©N\x0005°»§E\x0012&l³p+nyüØ.\x001cvð=ÞÎý|ûøáö\x0011\x0016ð?ÿù_vÒ½´÷\x0014ÐÁ±Zæf¹ víx\x0002»<<A\x001eoê~>¹|ur	kÙäV²¿\x0008U.B­·H+Å{#,Âw·¥ý\x001b\x001a\x0017¡ËEèÕ\x0016\x0011$!é\x001e#-_l¬Ú¸\x0006S®Á¬´\x0006)\x0001Þò,O\x000e\x0006Ã#%¿,õ·K·\x0008\x0008·åÞÃ\x0012ì³û÷Ííãïw\x001fî'í`¯B gj¼$·\x0004¼ßMÁ­\x000e àÆ}srùæôÕyÏÖ
¿<üCøû\x001dmÞ´eó¡;M\x001f0+üpÍ\x000f?\x0004c&ù9àJÑ5\x0008B0¹Ý6¬Âç®-ÙXå\x0013õ«+Ü
\x0000ö\x0002 l®c\x0002:_&\x0000­5\x0001\x0004cÚ\x0000[O\x00020ùÑ\x0006\x0000Ãb¯\x0004 "ý~\x0003ßù¿\x001f°Íß/-Ö\x001d¤ßoà¤½ÌG0øýF4~\x0000P";å÷\x001b}\x000f.\x0011o\x0013Óï·Y\x001bá_6¡qý`\x0000Ý$
´ù\x0015\x00014¦,f
\x001d#\x0000óá£ûýÃ/xB\x0006õK¼ÝÞ\x000fþz£Ñ¦_ï|\x0014H}
dÀ]ºûõoÏõ\x0016¹ã\x000cxßhö\x001d'Þ8>Þæj¥~\x0004\x001f°_1
D\x001buô1Jû+È( 0,äQØ1¼\¼<©ê\x0008UI¨æ\x0012F­òõ\x0011\x0010\x0005ÃAç¨tî\x0019\x0006:K\x0007ñE¦D4³\x0011mN8@B7µÐ\x00196k±2km¶$´ó	#í;\x0015\x0003N\x0004Ï®3¼~ùgv%¡Oh0<#¦é±	ÑælAD\x0014Ë?³/\x0011ý|MLi¸Ù}\x0005\x000cÉ²&j¶Þ..G\x000c%b(d¾{GU4¼Qÿx¯,\x0005¤»@¶7b¶ÁÑt\x000b\x0008.\x0007Rä|°8Æ4okaDe\x0013_À\x000fÐ&NÀ\x0002S&ca\x0015¶ÏXTû
X:ÇI\x0019kRDnÅïWåïWS~?v1Ù1k½Ó-E6\x0004¾«Ó¿)¿ôûáTÊE¥keüýZZþýBûé¿ß¿ßNøýØª\x000bBJtN¿_uVÞÙ¡ßïÊßï&­Kuá÷c!9Éß\x0007Þ9VÌX¿/¿öýÕ\x0011ÿzoÂé×KÚ\x0015øëg¨_(}¤þ!vy¤¸\x0010´ßò¯÷qºô;\x000bwôûUÌSÚ1\x000cq¼ýDÌ]´@ýÔAõó¿üåã>Æû"\x001c}±Ðmºíwù·ú\x001f~Ú~ù\¶ 2àV®\x001eî?à¿\x0017Eo\x001b\x001f\x0019c°b\x0008o\ÀR\x001f=p`Mïj?\x001d¿{û¿ºîR/áÐtònÀ.`
¤ÿyvdXØüCúãù¡¡ÀäóC4÷\x000cÑ¤ñ°\x0001òÏ-&¶ø\x001cÙlÚ\x0008öYî\x0004\x0011Å/×?ÀïùáúyÂm\x0013ÜöÙÀ}ùË\x0007-þR]P|Úüüåî1'!\x000e²Iïð.áÕãöþýÿ:¾ÆËB\x000coÓáü2*×
x\x0019WâÎKE-¼\x0014é\x0008_s¦K¿w§ùþ\x0017ù7+¾`\x001d±\x0004#ýqùÏÿ¦É©B!ÿØ\X¤+wJYÁ	m°]à
ä!,	\x001f\x0008öEúóyqá\x001bUþó9pýÇ_Â?]W¢6o>þóÿÜ\x001fP9\x0005¡Î\x0019^î~¾û\«\x0005ã\x0006\x000c8¤'%\x000c:'|¤\x0017/ëRß§*÷æìx8\x0005Öÿò÷ þá\x0002lù(\x0007°o·ø>Ôº?<@Ò;¨Ç R\x0005ÚÇ\x0004\x000bAx*S}{ÑÝ0íÃïæOCCc°Á[úc×çòöæáË?¶Ó¿½ÿs¹à» ÃÙ:E'Håª5è®3ÏåÉËwÿv|\x0018×!©[\x001b<¦A'\#©\x0005Ü<\x0006>a*:[\x001b0I,nÈçI\x0013´sôf¥\x0002OÖ\x0014)Sm
\\x000c"Ò\x001f\x000bqEnm}¸\x00045â\x0000e >³kÖP\x0006éS,þ\Â+\ô9§ÕDï±n¢@*F­!]8\x0000&\»\x0018\x0017+cÆÅQ +\x0003óú¨\x0016ðþõ?\x0002h?eßbÎíÕGìÕuùpóëm«!3hjÓÓ±×Ø499ú`ð­5\x00192cõÓ
wõî\x0012{v]^\x0000ü îãUê\x0016Ä«ÝMRG©\x000f\x001fï\x0000ü·û÷stXh®\x00100.\x001ee
µL¾Ì\x000búPïù²ÜYêåÅY\x0012ó)üâüÇ¾\x0002ü\x0012;iEús
llÕ¢3wjÖÜNasâî©skäN¡Bús
nì\x0008k\x0013wÔúÈ¼µËÜRë§q`\x001b·Nj¢×R\x0013gS&
Ù*õÓÊ\x0013·ÕO·b+·MÜ+É[û\/\x000eàZyz\x001c/m	ÜÙÕ\x0004¬tús
p¬W&EÁ9äÙø¹ÿÀ}xjH\x001aÁM\x00027kiJÈ	\x0000\x000e\x0011gUÁø\x0004\x001e|OxÜ\x0006L^Í¤¸|i,x\x0004*s\x0007pGª¢XMUlÒq»\x001bM6Å
­ó8N\x0000\x0017TE©ÔÊa\x0005p"üçrp
\x0018ÓP$,ÑKÝ\x0011\x0010\ÚU%\x001a#ÆOCàü&Äþù\x0004°\x000e{ä\x0006¼ÆKi©§Â6]äÆ±ËØõ¿ü^\x000bá·o~¼û2ó\x001es;«Ã¡ÑXìî»$f\x00113|%5e¹=ßÞyëôäÝæÇÓ·)Gïr°ÁUM)6kaã\ê\D\x001bà8´Fóá\x000bó!z¡ÉÔÿñéw«/ïÛwÍÃ®n!Ö\x001b	ñg\x000fá\x0010ìx¢U2\x001eó!Ep)u
õÃÉ§\x0002Þu\x0010»:¹<>\x001f´ÿüçë¿=\x000e¨ÅÙöæ×í¸G.ªQXæÊnà¨ªCs"RÙM¢çÖ \x0010ñÙñË\x0006GèTèOUã»A§¼­ï\x0011R¾¾\x001bôÛ?«ío¥®o7¯·÷íG´Sò£µÀþ0éª)</J\x0010ÍÓ¸
\x000eg¯ÏÇNg\x0005&éõsÇ$\x001d~î¤¯Ï\x001d\x001e
;&%<>wLpþ¹b:ùù·?ÿ¥0H\x0014E¾¸}_{w J\x0018¾9R2RÆ¢\x0010(×Õ`º~îã	ÿkÊ=â)|qryrþöt8b( ³yú\x001e ÿz·ýíó\x0003BãÞõ¨{û\x0008qÙñ×úÑ&¦J|FÊ½¨Nv80l(V{r	1Ù»á\x0017\x0012äªÕBJ\x0013Êð(gñý&¦Òt\x000bjðÔ?\x0014\x0015ß,'>uNK\x000302\x000fA\x000eÞ\x001cv¤½Í;óñÓãmíJ_>Þ~ùÔ|)+(WJku®htÞkº§Ç|±§çL°\x0004//OÞ
&\x000eV 3} ¿ûÛû?Ã¿ûÍË_·¿ÿ½5üÓÞP?F3ët&\x0016dÖô\SuáßÉù\x0006¿Ë7C£öü/û÷ÿxüuïe4uaj~k\x000c\x0018¦æN*&Ä#OfAjê¸\x0013uÏ\x0015ýY?4<|¨BåÂï\x0000KP+êGuãÿòw|\x0011Å\x001báôÇË_ÿù>§~\x001d_6oînfX­F~È/âÂò9$0tÿî|O­\x0016OR³w7§CÝNa©<¿aVwÈÚn®¶_>´\x0005ØOFX\x001d4þ\x00157±Z68/{^Ç»3ÖñæêøÝ«aóðç/÷?üFe ©øóÍãöãÝû\x0003÷4#Ê\x0000g>* \x000c\x0002ç¤\x0014	\x0008Ç¨o\x0004ñÔ½¹<>;ýqäFx·­\x0007O®#	\x0012ð©QMQª^¸|ÃîQÚvÄàêÂÓêû¿ý~]V/ïþúp÷xàãïÝ\x001e\x0005£tº\x000e\x0006'\x0011\x000f¡hJÀ\x0001p}àòôçÓË'uw\x0015YçU[È<§|S3èÓzê}(ïÉ(JÖ¹Ñ&2§sëQ .·\x0007\x00042E9$8 ¯gL$ë¡m2óü5m°´Afd\x001bmÿÝ¹³IËÍÍ\x000cªÖ\x0011	,P³°6ôF\x001bÀºf\x0013\x0018V¼e9A3\x0002@ý½ê>¥{Ö7¬;\6}Jp\x0013éÀ\x0003dZç'\x000b\x0019ÌdÎô\x0019idp\x0008	ídÂóÇôh~UÎ<p¾¦Ó¦]ýsD#\x0019Îâ.aTÕß\x0008Åd¾ç
v"YÖ\x0006S(BXKÎ¯úõà°f2ò¥­d¸!ùsÊ\-\x0008h\x0018p*öÜ«¡é?ýûï¿ÚÂ7ñ<²ã)·{d \x001bO\x0013¾¬K\x00016^Ò³ë¹TáQdgïÆ±²cjÄÒ80JÞ\x0011áy\x0016èQÿ©`Ù/5)-)KÌÍÈ\x0003Ü\IýQdÁ\x000eçª\x001c$Ë~©Ìã(<²:à)ò¾\x0014Æ\x0011ïyM\x001bå\x0002Å*Så\x001f\x00146ë½u_6\x001a~PÃÉ&)ÙÎEëwb´Ó_¹â·n\x0005ª\Zk\x0005\x001cÔylOÃ\x0000X\x0001ó§>­_üz\x001d~'\x0015\x0019K\x000f\x0011<ÚÄ¿[ÁÈÏü\x0015r\x0005f­\x0015È\I:D\x0001\x000f,\x0000\x0013 ó'XáÍ¾[-\x0017Ðtðd\x0001°M=}\x0002¼K§ìè ¬\x0010{ê\x001dWàË\x0015øV`\x000c%Ïû¨-\x0005\x0003Ñá(à´(âz+ ¢B6DyBO`ó83lrìr#\BìÐóäÙ¼Ê\x0012ÉLÃ"êy\x0013Ï-+a	ò>cÔ=gßæ%T[Y®´½\x0000' ³¿x7fàÓ\ú´\x0004?\x001cÌ\BJ¶­¾ÂJª\x0014­\x0012àr)á{\x0003ÁùFd\x000båz.|[\x0017a÷\x0016Ñ7÷d\x0011&äÖÔ°\x0008Ë\x0013\x001e!î¡Å°\x0008±Þp¶^Dk^îþ"BàÄ\ø\x0012ÜïY*E!í9r6.BËz\x0011ÍÉ®ÿO\x0017¡jujN|}¢N^çnC¹\x0008D¬NZ*:ÍÈ|=´\x0008³·Ö$Ø'ê>D \x0017\x0001k\x00084åP¨0#íøÐ\x001aööus>ìþ\x001a°íSÌå-\x0006 &¥8
~B=÷CÍØÛ\x0012­iÿ\x000f·DÊ-Öæ<Ùz\x0011Rb×©ì­=,'¯\x0001T(*:t÷\\x0005ÌÊïÝº¿?ÞW\x0003\x0001õáþÃívüep/\x00139À± WeàK
õ\x0006Åéß9<
x\x0013úô-ð]¿:9þß=gJÿøü¹¸ë¼L\x0003X>m?~¼»ý|èÅjÿ}]«rùÕ:Zêy\x000cÿMÎª×ºï\x0004\x0006°\mÏÎNOÞâcÕ\x0018&ßH-ãÔî²­TÚøÃ¿å"q:ÕóÉgq¢¥39%_í\x0001'M¥\x0000Nå=s8r\x000e§ÄÏþX\x0004³dNW>R!dº\x0013JFºÛ¡Y©;A\Ì	\x001f^gNe%§U\x0008EGTozÏØs@ÓÓ[úc	(6ÙÂ.º\x0008ªc
b1ü\x0006kK Nö\x0005}3@UHiØéÏE"5ÁH=V1åìÂ1ilÃÿð7ïSõ \x0007@üÏmj{¶9ùðñî@\x000eÈ~2
~êµÓÒàq¡ñ\x0016'ï¢\x001eÆ7Ç©G.ü¶Wg§W}÷½;ÂÅ¹K	\x0005¶¬t\x0012mhJ÷ä\x0000Q?ÕËÃ×"}âý//à\x0007yB(øÉÍÛ¹ýä+M)©Û>Fì\x001d2hÍî^:ÝW¨7'gÇÿ¶sñûª$TÏPú\x0019\x0011ðÌ/õ½°2Ý½ð-æG¼||¸\x001boÂðä\x0019\x0002	ù&\x000cç
Ñ%Âóåu\x0018¸ïÇóÍËËÓá~\x000c\x001d°*ÕB`ë©\x0019{xçâv\x0017u{\x000eg\x0013ëX/$vE\x000c{\x001e.°õoæÅ\x0013Ùb^Sòe¼:ºÜx\x001c­Îq2Hx§\x0013V
\x001cXæ\x0010ÛØ.°J9sù\x0005&Ð+\x001f>§Ñ}.üp\x0005\x0019»Ø-16s'bÃ~_ÈÀvà,2\x0007ØÀ~¡e¤wqï±8BGVcå\x0007\x000esCI\x001c\x0016\x0018;·!¨ÎvB¥\x0011×YÄ\x0003×\x001fsxcÉ\x001bJê0U5WÅv¹tÛWev×ø­âut5\x0003ÒU¹p\x0013ßm§\x000f=	L³kO·ÐÕé øÁÁ+AM¨\x0011ªïç W¾N.tvZhÖ	p\x0019Ôð*Ê\x0010èv\x001eS#WÎN.ôvp&ê¤£qI1¬aÅk¨råïäB\x0007ÿfç>Ä\x0000=IÛ2Dì+¶\x001c¹rxr¡ÇÃF)\x0015
GA*M\x0017Z\x000f¹òxr¡ËS\x0010¸¹,elIãIS2f¾~\x001bz÷\ù<¹ÐéA\x001bãâö£{\x0019²â§zlì²\x001c¹rzr¡×SÚw\x0016Ã%ãÓd$m?çÝ
Èß\x000b\x001d¦ñ<(dÉ6Nq|ìbO.ù\`U@\x0016Ze	Á[~©óØ\x001e.fbAÕEÑÙ¸üÌ¤*£¬\x0016\x001ae¥]\x001eRÉf&âA­à\x0007çÂòxSUFY-4ÊÒ+6ÊNE6Ê Ç\x0014";\x0013û\x0011UY8µÐÂI#±\x0016"!c¸ÌEó\x0012[8#\x0007\x0018ª²pj¡KR&UV\x0012ky÷
½þÏ!®\x000cZhàð"%ï½\x0010­ä\x0010º§\x0005èlâÊ¾©öí[ÈXW±½^\x0018Û\x000b¼
"E\x0016\x000bOBèÒS[\x001e]è*¸×\x000bûo"äÊè^\x0004{¯ù|Íb!¸ÈWo c6\x0016ªç*x6q}µÐ`!¸6DÌ¹Á\x0001\x001fV\x0019y(ck\x000eråEôB/"4·Ñ\x0002dK§\x00119ÔIY.÷"º
íõÂÐ^8§!²à
à\x0005\x0017r(©ì\x0000²8¶;ºîJW²§¿ý¾ýô©¯n¯ïÆ\x001f6F*Â¢`#æò[øk5ì²T\x0011¦èÉ\x00158}ýæøê\x0017quòâ´¿Ò®Z)\x0017aV]\x0004Î$É}¥jg`O\x0006Ï5Ä=_¡i\x0011®\[w\x0011VS£'\x001c¯MõoØ°¾COV\Ó\x0012B¹°ò\x0012h¨\x0006\x001bæïzN§EÈ°x\x0011v7·\x001aRpÓÕO³\x000fÍ\x001d¤±X-ç{ãG\x0008\x0014ÈbëXE¡/*ìú¯^mÎ.^
\x0014öVøªÄWëáãèNÁ\x001bAQ®´\x0001\x001b\x0018ßöÕúÎÅ×%¾^Qún·\x0005T \x0014]\x0003>7í©M
¾/\x001eå\x001fÔOrW·ãýz2NPq7@\x001fs5Uä²L\x001c=^^\^\x000ewëíU	¬\x0001+\x001cZï\x001cLÔT\x000f\x0000ë Ðkü¹h"¯.yõR\x0001\x0007ôJÉÃb*C~|ÿe:Z¢\x0007[NlJb³PÂX¾iHÂÝm;\x0016p²õXä5ØÄv©»\x000bJ\x001bÀ\x001dãrô(<\x0011ØÀn¹RÐ]\x001f\x001c&é¹HpÐeÍè;øDÞPò¥¼Zò¦ÈÏ;]`+Gßã¦\x0001ËÚ¬-´kXO(äî]9w9ÂÉ}]¡Üra\x000b-\x001b
YÒ\x0005°\x0016GÂ±Cw	5vÛ0\x0011¹²mr¡q\x0013Ø9#ChÄ4L4£Ú&cÆÞÂ'"WÆM.´nx¥\x0013T÷d\x0014éÞÌ:¾fWrìð~\x0000\x0019âÜ_rÝêî\x0007?`\x0015ëëûÏ·Lýjûx\x000b<£Üû
m¤ë>+Íú5gmö\9¼¾8{Âà¯/OÎÏ;0º\x0017%:&É-F÷hlr9\x0015\x001aû¹0zÏð6öJì~
±\x0007NO\x0001vKßpp_`±ëðÔ4±Jîa
¹\x0007yD\x001aã\x0005\x000fæpLbïièÒ\x001e+ô¸\x0002:Néð9SU\x0006ï\x001fÈî`ö¾Âá\x0016v)*IIËËá5'¬Ko°[v§6Â ø$¬&xY	>
õ[\x000cM\x0017)­\x0015\x000ec17ß÷²K\x000eïyPobWµàÕ\x001a7:O\x00166V	ÁÝà½1ðê{âÀyðÀ§Æ]\x001d\x0015ÂÙï­¸ø\x001eîáñþîP\x0013Ì=ø	#\x0008'#\x000fè<öØ¨\x001b\x001bqñ]ÜÅåùéX\x0017Ì\x000c/¬àÓ?/¦\x000f:æk8ã°ÛP\x001e}\x0000ì«HY^\x0017Å\x0008§s1á2z¥r²5ÚS¥QîÆ}o;¼^ôíûí§ÏCè1VOÿ¼\x0018]\x001a®æ\x0000ÌH\x000eÊ\x0008ÅÓô0l\Cð¦p®\x0008þy1½Þ~@o\.\x0008\x0006ÙkzwÅöY='¡6µùeûDq¶Ë5GÊ£l-±î1õ¦óFj®\x0002À&M«ñ_?á¿^ÁêXj'â¬O%ò¸oC¤3G°¡§MÝä\x0005Ð5­Ü»òÏ\x000c;êç;,Xûm{wÀÊÝþ£ö§û6ØMôªå4õ5ÓØ/ø	üÏ\x0017§X»öúøtÀÎWÐªVkAÇl·Ì¦NK*4Õ`L\x001ayØºÄÖ+a\x000bûXàåfz²¥\x0016¾ÜTòiX3\x000fÛØf%l|Â÷íilK­n	û©Ï£¶%µ]:
È"jK¡\x000cP\x001bÃÔ¦çYk\x001e¶+±ÝZÂvù§%®0\x0003aÓd\x0001­EOmá<l_bû¤íe\x000ez!`\x0010 ¿\)Å&FÚ¥Â\x000e%uXKG,\x0016ú$j8/EÞÔ=Në(nHp:y@èN½ñ\x0007ëÐûüò\x000c\x001aMøáV°÷E\x0013éeÜó82VlÝ[ùæýÿüçýtûx};^3=²Ôè5Eí¼=¢­\x000bÂ>èYÆnà!¿¡o~Üütrùâ¤¿«rµ*U®J}­U9~V×Þp7G'±½XZêKÊY´,S.Ë|­e©Ë4àcá{v½R\x0019þZ~ì®eY®\ûJËr1§©Áª K\x0017\x000e86:Ï¢Q[Y\x0007}¹*ÿµV¥5=\x0006k#4ÝÛê\x0011R{jÕÃ½hY±\VüZË\x0002g×ÀPÌñà®&²ö%«º2úkm-Í:¨¼b\x001dRÑªz*Ë\x0017-ÊV²_Í\x000cRÅ¼Õ\x0012\x0007#ª¼*CM±×«­KÛ=ë®mýTþ\x0007àÝ~¸}lNoq`	rº>\x001e<ÒÐÔ=1½eìé\x000fèx_\æ·h»gÍq\x000eôÊËÀr|\x00101Þ°\x00117:ð2¼\x001eË\x0001³\x000cW.Ã­¼\x000c­°x4-Ã©#
QÂ7ÙÛ/¤i\x0019¡\FXy\x0019ú à2r¼¯£¼¾^"S×\x0000áFº¢ß%½Ð\x000fÊ¤\x0017Øã\x0013Z#tê\x000f\x0010;\x0007\x0016\x0010¤¢¤/o\x000cuíí}&á%pôª¤WkÒc:\x000c\x001d]0M6Ã;E\x001fÀè¸\x0002½.éõôFqº\x001aÞ^æì#lB[Ù\x000c¶¡oJ|³&~P|}ÙiM²	ßlMÆ·%¾]\x0013_\x001b\x001e]øÙ»ùÔ\x0017:Ó\x000fMýCïJz·ªðc'|§\x001eob	?\x000e§\x001eL¦÷%½_\x001e+WIô\x000eÓ>è£\x000bì3j&ÓÇ>®Iï¨îÖbÌ¯ûIö/ÕL\x0018I\x0011ß©:/VäÇkorZ!*æÇ!Hßª¡¹ÑsøkµªÏò.gm\x0002\x0010T3ã-Ï\x001aÑV4\x001cÌ_}¹¦ÝØ\x001eô':º\x0002÷\x0016s²Hþ#£ù
·ÌßýàÉýOê´Óîu\x0003Ëßck2Gn\x0013}êé\_\x000bRïÃKPå\x0012ö/{-Á{¾\x0017÷6PSgì¶Â®·§¦»e\x0005º\ÁþásÙ
"%Qbè#s\x0008¬Àê.öé¹ÚoY)°5µp	Ý>ÆGA\x001f¡sÁ\x001aÒ*K°å\x0012öOË\x0010Í£\x0012ÐEìôÈ\x001cºR¸\x0004W.aÿ&mÙ\x0012[Iºþ\x0017]\x0018\x0007GJú
\x0007o\x0005'.!KØ¿_Z²\x0004/¤ÅÖi	F²CëüîóÇ
+(\2T±êW°\x0010Ä±MÕx¨I¤4D²gæRË\x001a**W5ª\x0011\x001fçú\x0015¼Ím'¼Ó\@\x0004axü5TVõÉÞ2U2ÝÓ#v®É®ÍóWÐn\x001dÏ&+£*×´ª°\x0019DÎ*Áý¬éñÂñ+¤ïÞÒ²Ê$É5m\x0017Úå\x0016Xô\x0015hC«àºïÐ3¥wâ\x001a0Ä\x0014äíj¹á\x0007©»ËÂû´9ß>ÞÜ}ú4¯w§£¤ä¶"OÄåðY\x001d{RJº,¼«ÍùñåËÓ««±B(bßeY#{eÝÌ.iVGJÝ¤>æ\x001ag&å|\x001eLâ\ÝVìv
véº\x000cñ\x0007¥`Îé®[îHø\x001crWi[Ccé\x0012fCr\x0002	=ZÉì=\x000f=Mì¡b\x000f«°Ç]Î©Ç\*d7Øp ³ë´&öXiL\CcÔ._\x0016¢O-YîÜ¸Øôt\x0005haª;þãrxì=Ûmc\x001b¢\\x0010!ä±ÛÆötàm¯·ª\e¯BSNá Ë­
¾grÚà:fFÖU®²[-S´ÊËü,AC×í:$YÏa¯\x0015^®¢ñ.;&óÚÁ\x0008Ê
·r¬f\x001a¶Û«l4®»¯½ÚÞÝÞ\x001c?~þuûe|À"\x000e£bl3­hÚr®«\x0018x$º:>=»9¾|\x000bÿ¯	\x0002\x000c¬*`µ\x0006±"\x001fª¨1¶r¸\x001b3°è9LÍ%ö\x0015±_J\x000c®^çT.\x001f\x0010YrÝè©:|H1\%g·XÎy¢^ ¸ÌÄYÎ=VCÏ \x0013¨SL+vy»ü§YT\x000f¿]7£*\x001fpûpøËí¼2\x001cãØ=]¿®_¼~1\x0016§]\x0016o·')SKàmn'+Øa\x0007W ½Ý\x001bÄ¡di+Ðå
¤p,Z g(ù¼ªëîa{2¨[øMÉÿ$»kÙ\x0017GÈóKè¼Æü®±\x0002W®àI"×¢\x0015\x0018êð+pÔ!Àk\x001bBw¿ð#h¿·55ìOÅ\x0003_ò»~û]¸á7\\x0017=õÃ5)¾1°=i¨TBðnóæäíéÀlö\x0012]èj-t¼6ùÊÉä\x0003\x0012ºä§Ýûz>\x0013]èz5©NêJw\x001cFu7Ç¶o
ÝLtS¢Õ¤\x000e¢6ùj\x0003\x000eÖ®#\x0017\x0012hÙ7öw&º+ÑÝjè`a(õ\x0008Û¨)EöfÿiåúZ$ÏD\x000f%zX
Ý\x0018Je8ü/æ\x000b%mØUÁ	p°Ti2z,Ñãz
#ø~\x001eGË;ò²_\x000bË¼¸×FÓ(V#i$¡KË"áZw
¥úúÎd¯ÍújvÝã\x0005\x0018õbò<5Àk§-¬ìº\Ï°\x0003aäF^\x000e{«eeç\x000cÁÞÔº	è¹íÞ~\x0017&%ÊÙ·\x0007°÷\x001aR\x0018@
¹\x0005_é¯©\x001b¿çNñA\x000cõ}·yyy2T¤j\x0001iðTäë1×,g,F£\x0005OC	CÙ~SIuIª\x0017âí9ÉTKî¥
Q!\x0015S\x00075Ôýe*©)IÍ\x0002Ò\x0018©ÞÞ\x00078{æîP)ó*Ê£çdP[Ú\x0005 *rsË`¸SdÔÝ q=2
}\x0012¨+AÝ\x0002P¼"ª\FöðvCiµSA}	êHÔtJj|7\ÈrW¥ `¦4,ÙN¡SRÌØ´´"0×ráv%i\"SÑZr¢æ!q0Ã}"h9ÖDTÓÉ[ö§¹öx@3n,O(\x0000¿°\x0010µvP\x000b<\x0014Ãí\x001ayÊ\x0006\x0017¹\x0003iO\x000fY¤K<\x0014X¦@FÊÓ#¯Ùº>C³8+÷$ø'|¡&L¹ó\x000cï'72jx\x0012iåä\x0012ÿ$CGêè\x0019\x001aö\x0013\x001f\x0008#x'VîI.ñOÂñ¨¶\x0000q'vCÂàT£©¨K<¤×\x001fE°¶fO\x001aä2\x0007%+\x0007%\x0017x(
gÜ¼¢èæõi\x0019;Ò¡irSI+\x0007%x(ar\x001fDJ-+µâÑE@ºpCU\x000eJ.ðPplå>?QúÜò\x0004ª(b¨¯ùDTU¹(µÄEai3}ÉûÉð~}\x0017Ls8+ÿ¤\x0016ù§.4MÝ\x001eØ?EèÐ|»©¤õ\x0001jÂiJv¤l¤¤ïPEûÿ?uo\x001cÇìùn¥60°øþ0>\x0015¡\x0012\x001bm \x0001HÚ~i+Qh	3\x0010¡\x0003:§ûénã¾]»Oç¬£wrWrÝ#Ü33Y\x0019\x0019É6ifaAjéçQñáááþwUl§ªa;ÕøºD+Ê
ºAG\x0015%\x001dQQ\x001fêÖ \x0016+Jµ¬(pøéÛÇw°|1Q×\x001b«¤	ªõ¤\x001bÖöÎÒ	Ô¬¬k\x0012\x0018mãÆ¯yª[æ)ÖwÐ·\x001f"§Dåc7¨KJ\x0017\x000enpP´¥ä]\x0013àßK!6@e¯\x000f^ÛP5¥[Ö$\x0005\x001d@
²ë£¦(jämË_\x0017.npQ´òÙQ\x0015ýÀe\x001d£©¤ÎE-\x0014Ýâ¤/es)ý6¡r\x0002º\x0010cícfbPMË 
KG0\x0015¨]\x0012¿ÿ Ú¶*SøS¦ÁÒ¬j\x0002¨0\x0015èë\x0017¿þxL­Ô\x0016ªmØTÁÇ;#P\x0014#Îª\x000cù\x000ew¶±J®¤®Ø©\ÃN¥`SMÕ\x0006ö×@å÷QÒK5Êµ-)\x0011I­g\x0010HÁ_ü^\x00174¼à\´\x0000cgfG¡?\x0014,×\x0014Ré\x0002\x0000¶1 &åWÄ²\x0018N¬HÄØ¶|lÅÑªp$Ýø\x0014p.ôW®{¤à_à#Å°YÊ¼*¾ÒLï\x000eùH£`Ö°ßåD8ò|>l2UÉW¡f¨µÍPKèuàG:g5\x0017S\x0019_;;ÌÐC3ôÚf \x0000»"3D÷m8VC\x0014áÁ\3ò\x001b:,JT¶HÆ¸Üÿöôð<½\x0002¦*­éá"ecØÈ%\x000f^Lä\x0005\n?\_Ü×Cx½\x001e<*S*³ÔXÔ[\x0011H
\x0000\x001b µÃ!¼Y\x000f\x001eKÆ(
&µÉ:\x0000sIôT.É\v;d·+\x000e|,\x0006>P)úÃîènÅaW\Eïú\x000c\x0018w®\x0016\x0013ãê±óáý\x0010Þ¯\x0007·nJûttaò7wjò\x0013/ìsÑÃ\x0010=¬8î\x0006Ã\x0004Y¥r {Ñ)\x000f\x001e)4¬e\x001fd([f´»ïzÅËÀðI±7§ M¥eÌ¥\x0005½\>¢^2%Ä÷Ð\x0015þs¡ª:Ö¾©\x0016¾8ä\x0007TÐ\dk]_­­4§P\x001d{a¨/Î'¹â\x0001©¥4oB¦¹=ÜìX¤ZúâëP\x0018Õ§*sk¹µ¦·¦O^kßndqBÉõ(¬/§w²\x0013ëè\x0006~\â|\x001a=õNp\x00071*øEQ0øËæòþåáS]Ô4W\x0015°ÝäZ\x0019i|WÂq¬¿-ßm.ww\x0017WS2\x0004ÝÇ\x0000\x0010ÚVhå(fi\x0005`Ê\\x0010&»\x000e9à:· M=l\x0018â¨aHãX[_Â\x0002´èÁçÁ6Ë8Æ\x0005ØçS«b¬¥Zc°sÒ\x001aP\x000bjÐÝQûê\x0015Ø¦Ä6\x0014ìr?Æ\x001c%ul¦"×5\x0018ræ¹5\x0005\x000c;õô<\x0003ûx%Xf6®`6®YHEU\x0006F\x0015\x001dÜÄì\x0003m"©x\x001b3\x000clßGzß8ÔVR2AY4¿eêúXdyÁ\x000céP0ù\x000f­äêÌ{$+îáJ!üH\x0019o\x0005¹°\x0003-(úÅ [÷æéS]ÄÎ)¯
\x00178\x0015Î.ÍD?ßß\_MÅ\x0018í ºÂ¤j9)&mç'\x001c\x001fl,Â w\x0019{£/Mó(õR7§#gÙjzh@gÎ-\x001bÎ\x0003µCPÛ\x0002*¹QnðJå"F;9¸<R×:Ô
I]\x0003©î§¨â\x001bbn>O\x0019°ÇÜ·\x001aR?$õ
¤^qr\x0019^­èË÷]øÛÉÑ÷°y q\x0008\x001az|YDª(º\x0007§A`R\x001bG_\x0016f\x000eòJ­\x001dæ.\x0018SRGÎ\x000b5Q:WÔxþó<Ôr+mØK=¶â¤\x0004è_Ã¼îËÜ±z¤\x001aÎb#
;©²ËaàbS|ìòYCZl¦²a7õà(\x000eÞ(\x0017\x0006îü\x0002æuã<-¾lXû0;9kG\x001aº\x0014Ç $OÓp¤çJ\x0015i±öeÃâ\x000fBóâ2PÇñ`ºWEø?M¤ª<ñ\x001b&*JÉ\x001aO¤êÖT0ÝÚ\x000f_¿*fªj©ø^B¹P0g)\x0015"*Î~\x001eØDZLTÕ0Q#Æ8\x0013ÎçìB8\x000f\x000cÏT¸ç4\x001e§ª¿\x000fdo¿Üés4ÐA\x0005t&Ï\x0000Ûu7\x0006`éd´ì\x001céóý¯\x000f±\x0019Ðæîþá§Ç\x0013ði\x0006õB¼¾KàRÜnÞ\x001f	\x0003òùöæâ\x001dv\x0002ÚÜí.Þ\Nh1»\x001e²ë5Øñw1Þk$vÙu\x00197Ç\x000f±zv;d·«°Ã¶çµ\x000f*Ï$Á°èÃ±PÈ"t?D÷« knG\x000f.î¶Ìnýø¬GCô¸\x0012º¢ät*
£ÓÆ©¡ë°Ër¥®²T\x0001^Òe
³Â(UF¾Y¨\x000cÖzøb©ÊuÖªê
®L<\x0013á»«æHJc=|±Vå:5Ñ¶\x000ew&Ê\x001bWÊwÎòH=k={±Xå*«ÕÊ®2Ç\x000bRÙ
ïË|yZ	^\x0015³F­2kgßßpv\x0001ø}}D^f!{[ù9·¬ñ]Z×ÝcTWÃ5ÌYcÃaM¼\x001cÖÄ¿ÞÿcâõìÐù.TWÐï1&\x000c\x001cÙÑüÓ×Û¿l'^Ì&ª[P³ÿQ%g æV\x000eTÏ5êtÏdµCVÛÈêiX±TP\x0003§õK?êÊÎDõCTß*aX)ûTjv\x000bSFB=Ö$·\x000e5\x000cQC\x000bªqYZ\x0005«z,u\x0010Vvµ2âBI
ë !
Ù%+KÐÊ
(\x001aN\x0001l\x0013$Ï0^×5wi;\x0019.¯AìÂ\x0015\x0016¬°¸Þ
;D¶­ÈC[ÑÈü\x0004SBH×­´\x0005\x001b\x0018åên¯å_|¥Ë÷ÝÃýûIâ®wpç=³Ùåé¼iÓb\x001d©ü*äÈ¾»Ø}·0@úî¡1Tåû²9ÿyÿË¯OûçiIÄq#ÂÔê\x0017h°Í¢M§Òí­?VkÇf¼ßÿiûöfssqµ½Rv\x0007%ð¾ä\x0012Në/´àð9Ì¥èr\x0016uô¹îÆ\x000b	Þ6¥^÷Õ¹{yy¼Á`j\x000bTÛjå\x0019	
\x000b\x0004ñáuIÍpÉ\R]ê\x0016RÇj0êsÞ\x0016\x000e*Ý¹uìéf.«/&o\x0000
ÅÜ$±*ÖÂVº\x0000f¬òf.kpCÖà\x001aX¥a	f\x0002¤ô®,¶ÎÕXjl\x0019U\x0019èÖ´Rµ'RÃ
¯£Õ¬Ì:¢GK ª\x0000U
 *RP\x0006ÔfU\x0010\x0000uä¡¡Õh_°Z|ý±åë\x0007Vúúá\x0003Ë\x000fXõÈÒA\x001d$Z!hN´Z¼U	r \x000c\x001c½ø8÷*ª¹÷ÊvË\x0003êJÐ!Õ5}áß3!§ènM\x001dF¬øúeï gXß\x0002ëÈ\x0004W\x0017\x000fWÎáE5ö3U3@6Ì\x0000eew\x0004À^@¢å*r{\x0004mÇ[ßÎ5ÅfSÕÂ:¾Q\x0002¬Ê*ªui¨òVÁº\x0012ÖµÀFG¯c\x0000\x001bóå\x0007`­ÓÝÈ.\x0006Â÷.ÿbÐúõåéË\x000búºÚ?VFDP+¢\x000b\x001e61\x0013¸îb°£9<|ýþ\x000e}Ü?m/'\x0003"®èj\x0005t\x001d\x0002Ë8çÉ­Å/.\x0016Î·\x001c­d×Cv½Æ°».¨ã\ä{²,#5\x0018+±!»YeÊDJf\x0001\x000e\x0010¤\x000c»hãÄ\x0019R9g»h7Ý]´iêDb»yÖ³@&\x0008\x0016\x001fñj,ú3ËÜ(Rõ+~+ö~Ù?~¸NYoNå\x0008Nªê®m¡\x000fÜ%LGÑu^<R¼ó?ßooß]ìnSÊàëÑÁ¡	jhZÕ\x0004\x001b»ÖN¬J±]×`}¤Ps	fhùCà&¸uMÜ~Ý\x0007MÅâ^;Í}\x000bõÊÁ%&¡	áhÂ°\x0011¯JÉi+Ú =oz§zYên&\x001dQk\x0002îÊÃ#QOµÿÅ«ô¹Ë[ÞÿüÏÿ÷óýþË§û/«p}À3!ç.c\x00088w
p´åk\x000bþF¹Ë\x0018az·Û¾¿Ú½ÿþ$~<À+à{¼
å×\,ó9ó:ã§¢ªoåà,À·}vcÂ·rÈ\x0006üàsü	è\x0003½\x000f\x0004mkÞ¬3øV\x001dÐ«\x0015è\x0003ö(ÔÉ3&·øÉsbR.à£ú,ü¯î¦9¦jzígþEQ«\x0016ãÂàª\x0013àª|
Ãº¥ì=g¢á2N9Uvýæv{u<¨Z !ºY
\x001d<Ï.ÛIC;ã¥ì*PÛÑí\x0010Ý®\x000eû=	$XÁìÎ\x0018îÖ¢Ä²QOs[ç"ÈAéR
ä½zõÝýËG\x0000H³=áon`çö=Ë^E\x0018+È:øÆÀ­;k\x000fª)a\x0007/0_ÏvØÝÏwWyÂ'øÍ
lú·S\x001e´ñ\x0007\x0017Fã\x0007\x0017Fðoî}ø\x0004ø³\x0014\¤àev\x0019;ÏY	w¥÷ÝÍÅ\x0015 Ï ×CrÝN\x000eÿ$K8¢?	¹IÍBèÞéëÈíÜ®@nX{ÔÃFOR±¨£\x000f#9^Õà~\x0008îW\x0000W<HîÜ½ç8\x001f\x0000;9®B\x001eä±\F.~ótIí\x0013ÓÔ:3E«så)QµÇÓ\	\x001cWèz\x0002úH*c5z±<å
ëSzØ
)\x0012B4YîÐåèÃD\x001dz±>å
\x000bTbóGB]DDp\x0013KçÇN£%èÅ
+,Qé#'l`\x0012&i¯£~&¾[Ô\x0017\x000bT®²Bûé\x0002äíér\x0018GÅg gÅì\x0002\x001bÙ\x0005_6W÷Ï?\x0000øB'ÆúH*xÖ¡ ^6N³\x0008¦7ñÈ­£¿ÚÝ¾\x0006\x000bN\x001b \x0006è\x0015
ÀÊ\x0005
À¬Ì\ºà\x0012Y.ÌÃwóµ/³À\x0000;4À®ig\x000fØi\x000c¡åooÜÞÆ#µÂ\x000bøã?®ÇïPæ/f~\x0015,¥\x0003y©£ä\x0019t¤]t\x0001úp	è%ðæéñþsªÏxÜZ*Øf1:%$ÃÿVu¾\x0008ÜKÇ[\x0017?}¹{ê6.·WS+ÌQCsÔ70ÇH\x0001|/Øë*­\x000bë¥Òd:r
/0'\x001e¦?E]úøw\x001f\x001f\x0016\x001b\x0011µ¦Ý	îùÀ¶'RSÇñÝùÅÄ©`PD\x0012|þU3Þáýðfÿòòô¥êj?jn\x0004iC(\x0001Xj\x0010|¬¶ëuµ½»»~?ö¾MÀñ\x00008¶\x0001Ã\x0001 r\x0013êZäÄ!eM÷l,ÝTû¿\x000c|jÝÁ »ÆAÂ*s(XmítìåªfÝÁ »¦A\x0002_8i±ØÁe`ØåyVL6\x001b\x001fdJØ³\x0007k0×
ô,_?ü´¾ÿüyùJ´Åñ,
Cxò\x0013¼a¶#b®\x00039Ë×\x0017o¶·»wï&\x0016¤\x000e¡|\x000c_Ðcx'iñöéËãÃ§\x001aIÔÖÁäl\x0013Áä]\x0006ké\x0002\x000fÍ\x0013\x0016o¯ß_^\J 2 \x001e"73ëô~¢©Êc®TböÒS8òhï¯ §Z\x0003îÐÌ]¡ÀR$éÊ`\x0015õ§ñB\x001dkIWÍ=IÜ¥ÎÌ\x0002npR(Hà0ÛÃ¥üà@z>Áècò\x001c5SDër¨ÓçFd¸{\x00102^C\x000c!;· Ý1=èÊ¡ÖÚÛÛ7\x000fµóT¿ëçúR\x001cbâ6æXQô|nE
¢û'\x001aT5däe³}||À°N\x0016\x0007\x000bÍ)·
[ï\x0019ì`víX¦ÄÝf{yy\x001bßiæÁ»\x000cöv\x0017­ÐJQ:¨L-~³¸èòÁìX\x0018¦\x0006Ú\x0014Ð¦\x0019Z²Z\x0015Á#-y¨y#µÐ²\x001ddÆÔÂë.-(Î¾\x0016©\x001cëÉV\x001dKìØí`ÛËÎ*^þ)
\x000f~K~\x0014\ÝV×Ú\x0014ØÚ4beÁ\x0011Ûè\x0011¤Và<å:;=\x001f[\x0005UÌìô¹m¸-¸Ú6gü`
l^A¶\x0016õ
T=òÀèåÁµÒËòZyó|¿y»~xú´ô¦osvCÀZ5A\x001dÎ½È×ü\x0018=]ô÷ÉÛÝæíööâújÂ%\x001bÌÐ\x0006³²
9Ô\x0012\x0002
÷e\x0013Ì×Éèýz¥	Î\x001c¸âp
\x000f«^àöðÆé3a\x0001ö\x0002¡Vó©\x0017HöÄ½UùPÁ\x001eF]AÐ\x001dÜ&n1æx|þ\x0017F¨¡\x0011jU#ào±
1\x0017>Â7A5M`Âót	fhYÓ\x0004ØcHlÂb×\x0013LåÃ\x0000Æ:¦d
FP\x0013îCmv\x000bØûq?½\x0016¦}¢;£¬1å²ú&|	2²¾ÿüÃîF}¹/·ÇWB\x0001ïðnExÝõWèuJ¼Ö\\x0016çÈ\x0007ÔÓwÉýðã/Öû\x0006$Ö?%#À\x0002Ûü\x0015PðZk{D°d\x0015´ÝÈ2t\x001bêë§/¿µÄ¯©×£.·ús&ä½Hâ"ùú\x0001¤ÜQ__¿ÿ0\x001dÿõ©3^|}²5\x001a½
L¶B\x0019OA\x0002§BV´xW\x001e¯²k>\x000cj=¨ÊÿþéËb|l`§(\x0015\x0005cc¹g6UèÃx+³ï¯ßÏVChµ\x000et\x000cùõ,Kç\x000b¡»~5*EÝZ õ\x0010Z¯\x0003íd&Yé0éFZw©Vq¼\x0010~\x001e´\x0019Bu ££*uXààó\x0004­Ç»ÇÍcvCf·Ò@\x001b\x001dÎhª¬)Í­	ôXè\x0002º\x0007
Næ \x0001ÊÍÃÇÛÀ@N;k\x0014Íà8S\x0003öøc¢S]l÷âü$j\x001f\x00170Í+êX}ö,ØÌ
Û¥Iy\x001dv@ncÕ\x0005«^Î
Ç¤Çuc¤á|X/\x001c¡ÚñlÞ:\x0016àGNy0¦
\x001ag½	c´â·\x001b5\x0012£ÂÚ³\x0006u \x0017`U\x0003¬\x0014^"\x0000VRsÞª\x000c{,Ã¥\x0002vÛ°ÃÔîjXÌ\x0008¥hlê¨\x001cV2&X\x0017i=VÀº>\x0008a]Ñà£\x0016\x0016\x0016¿44_\x0015r'XgxdÍ±d¹\x0013ÖI[6\x000c«6{@êRÎ|\x0012ðà'?Ø±¦\x0012WOÂ\x0016ÐËÓ&ðCÃ.`º]@ë3'ó|ÅJY¯¶m
 îþ\x0000wß«(\x000b\x001eióÝ\x001cö¬nõ£\x000f	ã°¤*\x0012\x000fG\x0015¿\x0019ùþéS¥úçÿ:Øm§\x000fàÍ$wáÓøÒ\x0010èé\x001d\x0013É^rGL)dG¾¿¾ÊjUÛÍåf:l³CÛì·³
Ì²iÎ\x0008\x0012ä\x0006Ól¾tYy¬N§Ñ474Í}Ã¯-¸\«l56·É¹D2R	E§{mÓüÐ4ÿ-¿5[\x0013À×&<%´à×&ék;àØh[\x001cÚ\x0016¿¥m$»_¦>\`!u\x001cáV·M;É7ÜJÐ¸ç¤+\x001fuÂTRÓ\x001723W6®ò[ÎJm²ógµÈ4É8M]yÓGÄl\x001aç\x000f»Èzw\x0010Îùòðù¥Óúey¶ôXÏ._àÖD²ÊGn©ô\x0013\x001cCÞ_¼»ëÔ§ÞNä|¨\x001cÜéo
ð|kørÿøNàïî??ïëÞ\x0010½Êå°ÒäÑ)KoÑs\x000e?®pyÎáïvïn·S±eun£RºÍÍãþãZÍcQV ÷W3ÂpUÃK\x001a)<Þ\nÏws;àöåÎ\x0004µ®	Üa0A\x0007-É$©­£Ôáë«æ\x0002\x0013ÌÐ\x0004³²	C\x0010Frö¡U\x001c(p¼\x0005nh[×\x0002ðtT¤y$ññ1ùï<¾ü,0!\x000cM\x0008ë -W$c\x0018Ú([ÁÓHº¯ýÐy\x0016¤ýÆæ
¨¿]Y\x000cÛ²\x0019ô~óáá~s{ÿééùû\x0010Ü´=gCá\x0013Q¾¾¢¸£}H¹ø5û°\x0005ôvóáb·¹Ý]]¿=ivC\x000b´[Ç\x0002\x0013Ï¨Ñ\x001bjc¡&s¤vj©\x0001}"	\x001a$«\x0018 P\x000e!Y]1[àY\x000eGÙ#ªHc\x0016\x001c¿õ\x0012~(fPXi\x0006)K¹¨UIJYÊXÃ3H\x001eé.[õ\x0005$Â\x000cäé\x0017ü0qó\x000cÿôÃ¯ûSâ&So\¦\x00140ÔRÊ\x001bÌ*Î®ÄÑ>ïwÛ«óí¤ÀÉ ¬º#Wkwý;PÜDQÑ#ØÐ	:ÈcÙèz®W\x001bô`¨AzK
{\x0018"·\x0014F}Dä»\x0006Ý\x000cÑÍz£_*\x0002¾ÃÑ¨æ7!Ø{W±ÕpÛ!·]oÈen³ER>\x0000\x000c¹è¤3FJdkÐý\x0010Ý¯î#?ja¬ïÐyÔíH£\x001aô8Dëºfý\x0000ì@\x001d¬pä\x001f\x00187yW.Ëq½1dYßàº\x0016Ê°ÿÓt±ÇÊf'7L\x0003ÿ\x001eS\x001c\x0019<wÏûßî\x0017»eÖ;Êµ\x001aF£1°ÙP¤Iº#Ï3ý½\x0017nX\x001fv·S®%`&UM°C.8¾ºKG­Û1+f¼Bj	ò ýB\x000c?\x0007ËýUwMD	¨@o¤|AqãmFßoºßäWC~µ&°Yu\x0005øÂÝ3ñ[Oâ\x001fR\x001d[¼õ\x0006¡\x0001f=\x0003\x001c¾NP.\x001eL'*\x0000vFGÚ}\x001bï©[c@\x0018\x001a\x0010Öü\x0006ðV¨hç·]PÕYÖo\x000bfâÅâ´\x0001b @Ç¿(Ë\x0003_ï_>~9±N}\x0003ø4Ì\x0015«gÁ½éÚ¹´«ÊÞñëíÝùû©T\x000côç:\x0003Ôz\x0006Øè\x0004%á¡h¤%¬Y@OI±ÓüJ\x001e\x0006«ä`\x000fºßùíáñq?Ý×l\x001f®RêLS\x0016Oö4±Ù%§\x0011ªñ\x0019´Û¿ÿpqy¹=Þè¬0@

P+\x001a`±`v9µ\x0014ëÄ*\x0014º çû\x001a\x0003ôÐ\x0000½ª\x00012W\x0002YØ/5í¢øþHÉ_b¢¯÷4®ûQ©,Ï\x000eÂ+ü8L¦}óüÙðõ/¦QZÍ-¾\x001d\Z\x0014÷Ê¦®³Ø+u¼þ\x001d\x0005çn¯1-þô\x0003ª9ÌÌ6¦\x000cÿùéyù\x0000Ûg6Ã\x001aûÎ\x0019i)7\x001e#S¨\x000fÿùúvr\x0002ÃtlcÊ\x0004È&råtîGäÔ7²;3#½1ªáõ\x0010^¯\x0007\x000f\x001ePÎl?Ú\x001c\\x0000<\x000f¼9rçÏn\x000f§5e ¿y»x^\ßâ³tÝ5&à6ã³®éÒ\x001c©\x000bî£ÛÍÛíÅíÅîÕÇýûÏÏã&¨¡	jU\x0013¬ÁâÃd\x0002vËÈ\x0016xO\x0019Ìp(L\x0005É;\x000bN~	vh]÷KPg,°]>M=ä³	bÖ0¾
Wf\x001c¢>ÙW\x0001B~¬Ø<=6C5T'l%å\x001c\x0005ÿ©\'\x001c¼tñA~~\x001c+_Íì}\x0006\x001a²«¯³ËàS\x0006b·¹©\x0018°ì\x000f°\x001fyc\x001ca\x001f\x001bú\x001fàÛëCð×ð´ë?}ÞçÅLßÞKÅ\x001f\x001f`\x000c¹Õ%.Øß\x0003×,\x0012ü1ñHCóëwÛü¨ø\x001eô\x0010P
\x0001Õï\x0003®ÝXÑ\x0005³ø5ÖÒ<Ü\^\x000cvAr!Co2/ÀÀ>°8²\x0000Ñ\x0007Î2ØXKs±;*\x0007b#ÔÐ\x0008µ®\x0011NâÙv\x0011¬kÎ6\x0004ÖG8\x001aLXd\x001eÚ ×µAYö$-¸Â¤¥db1N1Ò< Ú\x0008;4Â®l§R\x000etÀÎ"\x001bÑEEâÆbµ\x0011~h_×\x0008ð##8¬	Çj`\x001bªlC\x001bâº6øH7[Lû¡à²³a¤ê Ö\x0006YnMëîM":ð¨1y>ïMgS8&\x000c\c\x0005Ü\x001d\x000e/&ò@ß*É¼6ùÉ\x0002ûÏçë	¦)e.\x001dÎ[,=MÝP²ÞëIWÿð¢kdéê¯`\x0008\x0015yu!Ým]HµÇùvd\x000f'ÉéÈÈ\x0008Êé¸¯\x0012R¿<|~øçUIïÂºNÉ´¹½:Ê£áuWkR.NMÈíeçöýÅ»\x0013¢qgjÿ:¨Z|½¾¤OÍ5\x0005|tPÊFáøË\x000bÂjÌ¥(Y|½º¤\x001fFE8¯D\x000e7Ý\x001cnÖ¡Ï²Þ¬ÖGêjÑõ\x0010]¯®a¤	\x001dÏ·|G×¯>æ"Õ¢!ºYo¾x~)ÂÍF=I«'t:­ènîVC7¤±\x0003è:äü\x0017\x001cõÀ\x0013F\x001e&ÓDôA³JøEºY¡¼Øþ'|ßÊ#÷Ó½C\x000fÅÆ°36IÐ\x0005\x000bÒ¼rØL$T\x0014¢ óö
¾jå¬Ýååv,áÀU\x0001®V\x0000×ºk´\x0015rò:pcÀ\x0004k$\x000c\x001eÃ>5ä¶\x0018r»ÆË@µ?VxFzt¡Ó\x0007
GÿJty8[$Í\x0016¼lÞ¡\x000cüþËÖD_\x0015Ú?ÜßÐ°;¢¾Ï¡»Í;Ôß¾ÿ_'±u­Û±±i\x001cs«3êËg-Ëé§\x0004ÎuþùPZ\x001cx¼}úôùûÇýóË­`Ç°Ü<I`\x001ay®Úö*ÉJ¡×iýçÏAèûíõÕ»×»ËííwC\x0007³«o2èÇÄAá\x0018ÜýñãÀ¹½ª\x001aùÓ;¯Q\x0007ÿ¬DÁRXÁÆÉwÿÛÝõÔt\x0011ö°q½-G>i¢ÖDÀ#ô\x000e*õL\x001d¦Â<`>\x0004Û#£\x0000ê002Æ¬Ìª¹Só\x000eÓ+bPÚ\x0013³<¢Ì4YÞUç_ ³R\x0019T=¤Ö&pW6läs\x0014T0ÜáHq|M$ÕèÜ5³¯ÅZzÑNí06oîØ?TéJÙ(¨ªA9ïì\x001fFÃ\x0002M^L].vÔ\x000ecófwûz{1!/eóé\x001fÔà\x0017¯÷4d|LW:9/¸«ê¬B¦µã\x000e°RxjVÂÆ\x0013ü\x001fÆÔ¨"MÞA\x0010ÝÁ\x0002b8ØR>ÂÕ»òà÷I
È\x0004<dÎrõFæK\x001dìaSJ:°§Ã]{Û?ð\x001fJjWR»fjoh±9ËJ¿Q¹\x001c,q?R\x001ePM\x001ddA\x001d\x000e·ïZjù\x0006yg	\x001aæ{ÚY<ø9P)qSýä\x0019;»#Ì½kbv¢u¤]ÈÍãMjühy¨é}\x0015OÊ©L­¹C\x001dË¡ÍCí]ÎM¡\x0006/%IXÀPSË{ð\x0019ôF¬¥2\x0016>·6Eq´uÞÅa´¥å\x0019b'dÒfÍ\x0010éU	ÛÆ\x001aå²\x0002#ÜÛ,gÊkch\x0004Ø\x0012[¡í\x0001´mvQç×kÏa¨" ñ¢¡ýê\x0019\x0012\x000e.
ðtièH}ÙÜÝ?\x0010°úªÓ\x001b«ocûôÆÄr\x0017ÁM5z¿¹ÛÝn¯FFääuß\x001e%êW\x0005#g(Ê|u1Ë1hÔmù}\x001d/fë'âXOtRÉéç\x0001¢-\x0010m\x0003¢\x0011(«¨\x0018^{­ëªF:6d\x000c\x0005ch`´ÜqËÂµ%¿©¤\x0002ãXoñ\x0011Dó×ÿöù?~ûÐïÄÞó/ïéFHkÎ$B\aÏÿÇíÓ/ûOÿü¯?ßÃ\x0014Ïíï°ØÖå0\x0001_4ç Hp?;\x0008\1·ïþ\x0007\x0010n¯v°\x0006«éüýåæûñËì\x0010\x00193¼nBÖ1\x0017Ø\x0002²¦\x0002O£­Ê]¬»wÚU%&á¥\x001fË\x0003¦ÚëÄì¢Èmºam.&yWÍ¶\x000e2FÜ\x000fÂîõÃ,ó¼u(c0ÌTW\x000fÈ^®;ÌxùM?\x001a9I\x0006Ì:ät\x0014\x0018fu\x0019¹k¤¹\x000e2ú\x000b\x0007NÃA£lÕ¶41%b×]VWAV\x0018@J?\x001a±¬Î¾Ljouw­7¯ô£\x0001ÙÇ\x001cHwÚ\x0006¥	Ùðd¶1¬;Ìè·+×6Ì(çm:f§vYF\x0006Æ\x0019_Ñ×dkÂ«ô£\x0019nH©\x001a
áÜKe85\x0002-@ëÅªÇ	*²¿J?3û@ÏÀ,\x0003otZæDHiRúÃÌèM§\x001f
ã¬¾{fxÁKÌÁ0³vkÌÏ/Ýã$¯R\x0002ó¡ÐÉùóÓÃnnþAê¡3È]JÉH\x00078Ô$÷n`¬sÕ´^Ï8U.·óÛëÿµ¹½þËnhÉ÷òÎ±\x001fÜpú1×\x0019M»\x001fó\x0002Ö7@¢¼ZúÑn\x0001¶¹\x000fÙ\x0002EO¹`A¤}Åb	È·°\x0000§\e\x000e¡V$\x0019"
dÉò\x0018`é^^V5\x0000·FYî\x000b
ÀèQCÅ
´6\x0017Þ\x0001ZÌ8A«
ÀV¯Ò\x0015\x000cP¹t\x0014_2|®ÿ\x0003\x000b\x001c9Z`J±gÖ[pÄ\x0015Xj\x0001T>ïCàbåÇ\x0018°@æÖ{`Wßb\x0015è\x0000PúÑl\x0001¶Én\x00188¸ÔÅÆ Ú
/\x0003'¾Åw`0Û)ýh· ç4$\x000b4éÔ\x001a	\x0017Q^\x0007AÈoa\x0001V¤\x001fí\x0016`\x0018-°!ç\x0005Æði ô7ù\x000eP»3ýh·@ÄÝ\x0006\x0016xöØ¤F?0[ çÜ¦«-°XZ~¬`&Ó\x0004éÈ·\x0007\x000b4\x0007}GU-ÀXú±\x0005Î³\x0000(\x00074À\x0000Å_AãV\x001bàp\x0005¸uÈ\x001dÎÑ·|\x001a$éd@Ðßd\x001d£Úù«ô£Ý£P&ç9Ýúh'r\x001cì°ÁÛoq\x001a¤Üôcó,¯\x0002+°\x001eNdÍ\x0016DífÜ¼ê-Àwôc\x0005\x000b<yÖ`Anñ\x0003\x0006-\x0006ØoâÕiúT$×\x0014ÿÐ>à\x0012éÈ¹ó¹\x001fØ\x0011]`çN¯¸\x001d=üöüüü¿Ó
\x00077Tøër©X\x000f¹¬z\x0006pÐØz8\x001db©é|Ò4;/¾ò¦²jíÇÝQà|w»»¸\x001c\x0002)\x0010ÑíÁ¿ê\x0011Q\x0006/¥Î¸\x0014\x0016IZT©LW\x0013bT£\x0001Ô:Dø×à_\x000b\x0010Qý%\x000f"¥ÛL(ò;«\x000c\x0013Aé\x001aÀÔo-ýX@hc~-q©åº!Dg\x001cÏaïYÂ\x000cz~,`\x000c"wÄ\x0006FO\x000fÀ\x0018éb\x0011ôø>\k0ý¨G´ÂæG\x0014Ðö9G\x0014nJñ0ê8ºQU1Z¼0ãeÃèh\x0018aéðW\x001d"\x000fcßý¹u:Òî	S\x0012ÿð»Î=þoñ\x0012)\x0007éoîºÙÜí\x001fï?ýø<\x001bWEK;QÊñN$¥Í\x0012¬\x0018ýösºÖÝõíÝÝæn{¹»ún¤\x0018¡DGE?Ó\x000eQV\x0003t-S\x001dçF&\x0000\x001eÆßsÃX\x0018Ó\x000eîsÞ
;¹ÔWÐíèî¿\x001c\x001d6\x0007ü«qº8\x001fü\x0001Ýhº^\x0019ê$½±õúäø nm;¹#25¾È/S@ÞÍ\x00177~ä.FÇ¨µk\x001fô É\x000c©e¸ÊèÆ;\x001eu?z,FÇo^¶OuC!\x0011êT6ÔGê~tã®Dÿ{ü\x0014Ü§áéjÿn\x001eîyúôy.4&O|\x0015B
æ\x0013dWL\=ºr¿\x001dædÏ å¤Å´p6æ%i\x0010\æ·\x0013¯,]4ÄD¼`\x0001.¬W^5à¢P\x0019áw/×ÚKj¯f	£ëp\x0001.ú.±et½¡ì\x000c#¬áWK/\x001d½.\x00089~×ãb/WéÇò¹«Ï,á\GSWðÜã!³qÿc¯­ûÏ¿f5²W)à²\x0007\x000féeîÒÇpúÇÂÝRËÃi\x0014öqÌRM<\x0017lÁ;\x001aKK\x001e¢an[N%¬c³¿nk|Æi^LãîÐ)¶\x000f?üÃÿê0+ýx\x0007\x000cx5ýåþÓÇ©êÒ\x001cÅ\x0010a¿n\x001cû\x0007ñ:þúýîj¬\x001e­\x0007XA÷*ÿü½ªtÄ¿OÒ\x001f\x001eÌßÿþ\x0013%4\x000eÓ\x0018oç.nçÉ­8;ãYÈÕ\x0018
oõ;'Êb]ß¾;\x0007S\x0012½Ï+ù\x0017¯\x001fh«½lÎ÷ÏØ%wîJ
ð÷³\x0008®Í=`º\x0018nE!æ\x0012[éP£a`Ö$»Ûoo±7îøªbö\x0010
ö\x0010ZØ\x0005ú*	\x001d_DDF÷1\x00176KT´\x001bÝ\x0005êÑ-©\x0001\x0011º\x0015¶	ÝR3\d'
/\x0018vNÿð0½Ç\x000f¬zv'\x000bv'¦\x000cÞèrX\x000cö\º\x0018éà-»\x0019Ï¦XÀîKvßÆþ/îÖûÝ·»ã)üôì§ñâAìÚï,Õìj¶\x001d?6±3Íãî²P
Î\x0019öÂ¸\x0015ç\x000cì+Ü\x0006z¸Õà¯Zvô`¬Á\x0002Û
å\x0010Á
kn7Þ\x001fÓ§ÍÕ\x000cR$Ã­_õ¿x%õhY)\Jdéd\x0007g®Ø\x001bª¡ÍÞ	\x0015G_ûæv\x0017éÉµ\x001dkÛLn38BX&÷D®ý¨×ROnäÜw9GNýt\x001cö\x0004ât\x0015Or
ØOY\x0008iT¡«\x0002}¼»Ñ,ô@ú98]tîfddPYå\x0016çË©Àã<tDÏyÕÿââ&ÐIguÿéGX©?ïùuþõ\x0006ßrèQ\x0012\x000eÛì\x001d(ìáH¯Âo5ïw$³º½ú\x000e\x0016ë¶oo¦j6À©¡\x0001Nµ\x001aàIô\x0007\x001c¹fpwäûxÔã±°e\x0006\x000414 f\x0003\x000c+$\x0003,©\x0016\x0001\x000b¢U£ÛÍB\x0003\ak6ÀÓ{\x0011Ü7\x0014E#Á\x0000¾"G'×6 \x0016\x0006ÄV\x0003Lÿ0ïÂwÙ\x0000í;\x0003&Ã{ÕüR\x0014k\x0018?6\x001a\x0010$=|ØÔpÖ@Pë7P½XÉ\x0002%\x000b\x000blC¤Úª¶C³\x001b£\ù;Ðåw Û¿HùØm´[ÆQG¶`¼Ðl\x0005¦´À4[\x0010un\x0008\x0007\x0016Hª£\x0005Ï11þÄ¿ÐXZÐ¼£Ç\x0005ýùrá\x000eX@³\x0008µo×Ý0ê;´Àµ~\x0007°d³J\x0006ú\x0012\x0002¢hÔôúGëf²¿7&\x000b¼oE÷")-Çr%uÂï`<r¶ÐPZ\x0010¿\x0003G_@àe,Mçû×±\x001fQÉêÁËcL¶cÿòéo"õG\x001f,á}»7áhþ8Ëñ,£·p\x0007®éÚûhüëFüØ|ÑUÆS½\x0015e×°¸½/µàã¡\x0005\x001f[ï\x0005\x001e»1§\x0003ÙØÜ\x0019ÝjÅ>qëÏ¥ûC#î[\x0017Æ\x001aÙüM\x0004
å¹\x0014º/be·\x0008løáÐ\x001fþ0ëA¤ü$;ß\x000e»ÒÉBnöüùiöË#¦\x000f\x0019~°(ç¢XA[~z\x001cFp¢è{Ì\x0012\x001dxddëÈÖ-Fæ~(\x001bë¸T2xAeì1ÌG,ûg\x001aä¡LU\x001d²â\x000eê8ÊÔá\x0005\x0003mÚw\x000f¼'Kïg2«P0\x000fKd*³\x0002UbÆ\x0016Aå$&x¯Å¬Æb!3>ökJSðüî\x001fñqÒ\x0014N´ÍDîÝ<T\x000c¨DFÍ2zV®CS\x0015\8Y¶0\x0019µÛ\x0006ÌZ/Þ4°¥yÞ²
FCB Ô¦n:Óiþ§uV@é}wef¥:·\x000f¿=ÜÏOl²\x0008FÅÀédÚÒ>mY´y{ñaTÂy¯\x0018â+uXrWË¯,\x000f<æ æÛÑB\x0013?jû¬ÉoD\x001còãÇ&~§-JJ*3¦ÛO¢\uìMô\x0005;|lcÇÇ|ì$)"Ê¸\x0016¾K2W.;\x0013\x001fÅ7\x0006øö«úÚ©\x0003¾bäô8G9F0õûíÜÌ+Ë¯áO
hÛ¦>©ãq$¨8
V±ï\x001c\x0015¹êø;¡G\x001cV½×òËÐeÐé®4\x0003v\x0012,
Õ¥ët±õ8Ýºõ8\x001a|\x0013Éå2ºË­x­]ÂîË±÷­cïD  \x0019ì`ÝØ\x001bêOrC×;Z?}n1 Z¬QN^:*dråËª\x0017nfUÚ<~£B¹í«Ð¶ïG¸!a+òNùÆa¡{6À¦Ðî\x001a\x0006ç?úÐ7º"N\x0015I"¯áGÏÛO³/\x001epäò\x000e*ò³öý\x0006¤åT××·pÉKoÛ«v\x0018_Øaü*v\x0017!È}Cí2ºò\x0013÷§\x0019¹FX[\x0018bí*Ã\x001ch[Ê%.vL<j-µÄÅÂ\x0012\x0017W±DØîâ\x0002³Ì%Öòä\x0012ãÎÑbKbùÄU¾ôºHÈ.³\x0007¾\x0012Ûs32{ê,\x0019\x0017hI:/V°Äv%ý\x0002%jò\x0005Ø\x0005ßÅ\x0019&27\x0017[\x0012KKV]¸]Y^ð\x0005±¼¤²P°dâù}©%}
A²Ä©\x0015,ñ1ê¬ðít\x000c$m\x000bßèfWÊ\x0007\Ù`
KYå;$ãXÖÜs#ÑÕ¿ c\x0011?®aP$[ c\x001fÁptY\x0013QèeÈAr\x0010Z>¯0½°ù¢Ë¦x\x000b~.	!\x001aR³Ayµ¼ÄÇÂ¡)éñp\x0005STnKò®KZwAR6­mòÅôJW°Ä{M\x0017om#µi-<ëiJ±öJÚ¦àç\x0015LqXõna.Ù<¿dP¤¦hÅ¸bÕRS.|ÈôyX\x0007
¥éß\x00102+åU/Ýêß	\x0007¦Lñ(ÝM±Tî¯­"%44eõoÅ\x000eqú¼)6Jòh
wÆæ¨\x0005ey\x0019¸Í­íÚKë\x000e,q«X\x0012a×Ê\x0005:\x0008NeÈ[1\x001c ã)
\x000bM9¸¥Èu®)èÅç>ÉN+grÿ--z­¾%\x0007+Å­³R¬Ñ\x0000¬\x0015¸Äiv©4,Qa<\x0006ºÐ\x0012åBqÒ§Ï+Xú)	[)\x0015Îòs\x0008dÖq\!v©!¾ÿLàç5¾\x0012ás³\x0007\x0007ÓÈðóy¤s^£ìíêXZ\x0012VñX0»Ü©l	VqæôÂ¨%SÔx´Þ\x0014XÜé\x001d½]¨T.KHÝÜÿýùéKE²9V·PryvI¯ºÚ\x0004\x0013jt¼nvÿ\x0006æMe-ý\x0001Ú2"èUkË	'Î\x001bÓIå
J[\x0005cfîjq1n\x001dc¢'\x0000\x000bî	]Uà¢Ò\x00150¤\x001d}cú\x0011\x001aãKV\x001b£©\x001e\x0018\x0013\x0014éÌ÷
´\x000e\x001cä\x001aÁ»ÙÆÄÂ¸1VåL¦ÔA\x0004YÊÕÉ	o²Á\x0016i}±üíá#ÕBcPÁ;'éÂ\x001d\x00059¢·\x001eõ\x0002ßÀ\x001ae
kðã:Ö(zy³Ú
lPVÈ\x0012:¥çHÀ×[\x0013uaM<.;]m
V_ek0Án³¢¨\x001eü!Öè\Î·ÆÖ\x001c\x0017\x001d­·Æ	«£a?§yÝ(w:\x0019j5º_Akðã:ÖH>7
¨ÒW\x0013iÙ¨\x0010¿ÅDÓºøjðã:Û³ ½\x000ck\x0006[\x001a')§ëoaL(9®¬Z¿=wåCpÞS\x0005tÔy\x001b&¨ÒÅm)¼\x0000mVr\x0003jðd£\x000bÓ\x0013÷ý\x0016c¢(Çõ·«Á@R¶\x0005üÿ,$\x0004þ¤ýL\x001bñM¾X~3q¥oÆ³\x001046N¥Ì2°Æó<3UBÐs­1¢Ø\x0002Ò­â;\x001b®Q6A³\x001fà1Á¬	ßÄòRcV»Õ\x0004z·ø5QÇ\x0003oHç\x0001¿ob+Yë&`(&cMT¤w4:8u
c­o*'ÚöxýW#é!Üâ\x0015ÇÐ%MsM¹vãO-Ö¸ò»që|7Vs<ÊGÚ\x0003<ûútBì\x0012[|ùÍø¾\x0019Íi_6õªGK\x0002\x0017éðM\x0002\x0001&_KXékë.\x0015\x0000SøÔôQ³1ñÛlÍ±ÜÌâJI\x001a÷É\x0018c»õ\x001f)æOþßÂ×D±§5Iûi
k,÷\x0003²âsõ%ª
53s#+ÅÁ«\x0018ã4ßÐ,Ýçõ\x001fd÷Õ¨9mÒê­QÅ}\x0013?®5Ñ\x000c5q¢Yþj¾É²\x0019QXcW²Æ\x001b^6\x000eÎ\x001cG2\x001a^e0óm\x00005T¿a¯fD)¿Þ\x0017pØ¸&»i\x0011·ëì\x000bD¾\x000fØÓÕ9uFé\x0014Hë\x0015Ä$¦ô1ôÍùÃ?ê\fßIS\x0008º5ó\x000bö´ìÙæüâ/§y{ý\x001eäz)pg6tU°Ü|-Úñ*:àA\x0002I UÀV(J:B%IÊ~Æ×Ü\x0014Â~\x0007lÄ\x0010Ø¥ÀÒvZ\x0019^v1{íxýé·ùyÀ¶\x0000¶Ë\x001dÇJR\x001fmZ{Å0^P	¬
`µ\x00188rÑª]×\x001b.ÄÑ|Ó\x0007ì\x0011vËG8PbE\x0001_¾»)\x001eàxú
z&¯+xÝR^ðüy|5e\x0000/½\x0005\x0002ïøõ¬7\x0014¼a1/ìd\x0015\x0015\x000c÷3Äö\x0011¬	±Ò¦&Ë=B.ß$´¦Î®°úºGÊ.>)fdRÎ\x0003.÷\x0008¹|0¦\x0004\x001c\x0016¤º\x0001#ìø!Ò­4%¤+ö\x0008é\x0016o\x0012Æ³Ð÷\x001c3õAó\x0008{y2p\x001ep(\x000fæ°ôdÆ»\x0003m\x0012\x0012EÉiÕq\x0013átNê<âX¸>2.u~Ð»¦·©ÔC.ò
\7)NçhÏ=8
\x000f4\x001f\x001eCùÅúóCwçT_\x001f­N6*9Ýþ¦ÑÇ}õêâ_÷//IÅøíçû¹E¿>æl,¯à69ÔqÅ¯j<óçâíÍöî.)\x0019¿}»ªùÍÈý{\x000c"ãsÌbfì©áîE
·²¤ª\x001bñ´ZÚ\x0014\x0003mZFZt}sà§@«v2°,g\x001c>®Æ\x0016n8¯ó\x001cÁ_4L3M²¨è,G)Ç|\bk>¼\x0015²¼AY<qYH\x001f\x001e\x001e\x001f÷?ÍOr®\x0014ñMÈ\x001cªGÇ9
Ì\x001f../·ovcB\x0019Ûö÷]V§U{8GºÚ:\x0011IËI+Ø\x000e¹¶nF¢wÇ}bÄ­R%ºjC7ùDw>
Ú¼µ­êÍM°\x0006]èº\x0005\x001dvh*zQ\x0017gÁ\x0010;¥?{+ÆÓ¢°\x0013]µLu`722ZÜ)\x0005õD]Mh)Ö³÷\x000ekb7¢iÊÀöµ×\x001f©.+m=Ï9ÝóÙ]ÉîØuÌõ£®¸¸D9Ê¤óS-TêÉ­)È­i#·9;+)ÇeÙ	­ú1«ûÜ7+EbA°N=¥Ê"\x000c¬Óñ'Ø\x0005ì®/®m¾Xï\x000fî¨è[ûÕ¡ÏH\x001bMîËQ÷£\x001eè0u\x0001\x0016¬¤\x001dÆDÞaäxjâ\x0002öX²Ç6vÍ}Þ\Ð4æ©Þê	Ð\x0005à±\x0004MàFP/\x0003\x0017é¦ºco×N¼\x0002Õ³;Ql0N´m0@ØÀ®Ï\x0004Ïuº\x000f\x0001ûxóæ\x0005ì²p\x0005lr\x0005Ò¸Óqj\x0003½Wá¸ó±sTôg³Ç=6±{­XX"À=4ç\x0010k\x001d\x001c;\x0013ý\x0018ëÙ½)Ü\x0018üØÂî
6ì@ö(
WÐ\x001aCêà]®¹A¢²Ò=&ö:gvÍ%g¦ßgâxªc5»¥\x000b&e\x000f;_Pó\x000eðÛ»Î\x0017¦kø²â¤Òè\x0003ø\x0019\x000fðJ0=Æ¸èTû\x0007·í0ã½Â\x0016À[UÂÛ\x000bSÀ÷²À­v"ÃÃ¯92`Æõ¿\x0016À»\x0003x×\x0006o5¹b^^·{\x0008ú$1´"¼;oñÅ\x0002>­z\x000f,¡\x0010°XàçëÏ/½1)Ü1lbÄ±°y\x0001)×xÊ\x000e½h\ãs\x0001{%{h	o$vG\x0003o)'\x001cØ}\x0017Â[u¯	ñ½Å#\x000b¢Ó,óÊQ@É|Åñ`m[¼r]Øeu\x0002ËME1§¡×|ò¹Þä¾§1\x0014óÅ®#¤uâ#Ç\x001fg<ÄÍW¢<h;á®î
X§S:Ý\x001f°7\x000e¼9£ uèºÀÁ¤éØÇcí\x000bØe9Ýñs\x0013;\x000bÄ\x0001|w4áÄðaÍö\x0000¾-r­ì\x0019/Wp+I\x0013\x0007F¨ç\x0000Ïw\x0007ðmçªòäÄ{Ú\x0005ÝÈ+_s¯ÁJû\x0012¾qÊK
\x0015\x0000|<;<W£Yñ\x0002"\x0007Z²]5:ñnÜ^¾çpç\x0007\x0003ü³Æ\x0007«2\x0007+·\x000b¬§f@\x001aÝ_w+i¤r\x0007ð®
^Gz°ñÚ¥Ã*;ñÜu/®éÃkSúðÚ´ùð^sÒToH>¼!ý-<\x0004V<]u\x0019/HnO,¹å±¼6Ê@]¶ñrU³\¿ði\x001dRªd/ 	W\x001eÉMC¾lÞ>=Þ??ÍÕDpIp#'éØ\x0010»ÔÃÈµ\x0010Æ¨év?ï7o¯/w·×\x0013J\x0008Ü\x0017Ü#²rmªtJÈ1p&TèJ¸\x0008mÔ!÷Ó\x0003mA¦ä-'M>Ïì&&õLbÀe6\x001f¦N\x000e²ù¾l^ß?þöÏÿþñÿ5_×Vd-U \x000eRèîR\x001aB><sã\x0012ý4£ßo^ï.?ì¾\x0016UMðR\x0017ðø±^b»féM`­¢èèJ\x001d¼8ùr]E¯KzÝHoRºQ¢{)E¬#_ï°\x001dÅ©@
}9qdëÌ°gíª\x001e9þh L¯àN\x001f«àC	\x001fZáÑ×ÊìDÔPlT2ûÉÃ¿\x0006>Ø\x0002>ØFx86\x0003Í\x001bÀÕ.ÓkÊ~Ç_qÞ¨AÇi S8Ò"zì-`ó±t»Ãg=ÖM­H\x001feA\x001fe#½³ÔÀ0\x0008ÌoÌ2æ\x001f²1ÓÅi¯e1s´l9\x0018Î #ÂçD¯\x0005ïöb¼ûî\x0002z]ÒëFz­Øù
B°[`dT´ãØ	¥#ôÇ½/F%zl\x001dxEùx)PàhÒS\x001eo\x0000ÇlÅýFb§×¦q§Ë
Ò];WlÁ'w\x000cé××%|ã!«°i\x0005­WI\x001e\x0002°\x0007Í»ÍIaÆ\x001ax[¼m\x001dy/)	\x0002µ
)1\x000f×+ÑÛf-\x000bèK\x000fA·z\x00088é³ê*¬WËý6>tëuMørÞ¸Öy\x0013$\x0015@Á\x0018³x¤X3áíÉz¢\x001az¯
z¯ZÞdt8£´çÍÆð¸¯zFràCëÀ{Uq\x0017TU
ðÔh#X3Ñ¨|\x0001|(á\x001býJmMGU\x0014ÞþTp£>\x000b66/XM-\x0004|µ«;÷\x001b«Oæ\UÑË¾Õ5ó|\x0002úä!gúÈ¥9Ù]£¾ô\x0010b«\x0000Ó%ë
úè4;õç>\x0019J­`7ºØmðcãÈSn§FÒ=vàÜ\x0016×®a7Å¸\x001bÓ:îQ\x000b>§Oié½,°êÀ÷½è\x0012¼3­F9:¤ÀZ<:¤\x0008þd\x001eJ\x0015»-Ù[ï"å3°æÏW\x000e<\x0019²æ¼\x0006>\x0014;%~l52?Øïó&òÈ;³æ\x000f²¤oÝ)#÷¡ó!X*+Iï;úñf\Kè]IïZé\x0015ÞA2=Ë\x0001½bz;.¿¸>ô±ÞqòXð,]\x0000ôT±\x0002ô'Ë¨+è­(6\x001c+Z7\x001c:`\x0003\	\x0005O\x001b*±\x000fÆ+ø-@EÜi½\x000c\x001dn²s\x00130)»\x0007\x0002»Àgz]5ðSÑ\x0003W¢»Vt\x0014Íä^{ðYV'ë*ÝËÂ#Æìäø¼Çô\x000ej\x001aÉw@-ÇÕ^\x0016À\x0011zß\x001a¡7Fyd]F©ÂD¯N­ÔÐ»bÚàÇ6úà(Úç]P¤½i½Âý|Uúrâ´èÑ9Êè\x001e¸vTJ÷¬\x0015Ï×P\x0006èCk\x001eµôÈ§tp¥ÊQÞ-SîdBJ\x0005|,£¬±5ÊjakÏ
\x001a¼·/àVðÐk}2é°nèÅÃ<üªøßÿ7\x0000ûÁ¡
\x00180nµá_\x001a3\x0006ò¯ûC's¿¦\x0019ì×^æ*Ûö\x0007ÜÚ§BîýËËþ§Dó|ÿòòôð<\x0013Ý\x0005êZ/Q¶)]	\x0014[ïùX{¾}Àonwww×\x0017·'¹¥\x001crã{u\x0013¸¢Òy#¢¥\x0018\x0008°SÕ\x001d¿/B\x0005zlF·4êp\x001dtLÎ}É'Ú%ì¶êÀp-ìRwíP1/yÆJOÉð£NN\x0015»Y¿§sêá\x0017¯ðcÎZI\x0002v\x001fîkö2u\x000eaÒåBW/£äÎÌ1N$®¾ßnÝÝ-übjfvÕé]¥0ýbv­QHmFYòé0\x0005}äD\x0010¡½\x000fÒ'ö\x0014¤o`WgÑÑ¸ë³Hs\x0006Ý\x001e\x001a÷q\x001avØ\x0018ÓöØü`§T\x0003i\x0011ê²ó¸ÿås7wà;ë?4%Þ\x0004¾
Âg4RÜIt¤\x0006;Û·¯/ÎOã!~hÇ÷\x0008K×SIH\x000c¾Ëÿ\x0018!Yßg<#¾tíü²ãGý.uS@Âx³ßE\x0006ôÛe>¢Ù\x0000\x001d)\x0013°zö21s«Ë\x0002\x0019ï ½È\x0000]\x0018 Û
@QÖü¸)ákø\x001b m3`Zñº\x0006øÂ\x0000ÿû\x0006Lñ
\x0015¦¦JFø\x0006\x0004·¨SK©~e\x0003=È´oBFqöbÊ%ô
ð\x000c²f­\x0019DÊ\x0006­	QE¯;½^?ý¼éjPÃ;÷´öNqç\x000bMâLÖOÉ¥åcëõõ¶\x001dâ²Z\x001cÒ¦æ©\x000bhµe¥X\x0003K´¤¤U¥h=ìëàª\x0002W-\x001c\Ø×\x001dáJ.ÄI	Ïk'´ijp½\x0018âz±\x0010\x0017r§ö »fhNZ\x000c~¼sH\x0015n,&Cü½OX¬´¸p¥i\x001b°\x0019c\x000c5x­¢Þ\x001fÖO%\x0013TàJQÌ]ü¸l6\x0008A\x000fð&ÀHö£å$xë'z\x0015Tñ*Sð*³p|¤\x001bgè\x0012Q¥µ´ÿZ8`Æ³\x001djpM¹ï¥Ó\x0001õÑtè¤\x0008¥|·÷S\x0001¡\x001a^[\x000e¯]:¼&RE¤BâÛK\x001a_I­+lPëà\x000e\x00121\x00107Æ¥Ã«ºs-JÊµÃÖót\x001fÃú¼5x.7=Þ,áÅ<êÜ\x0015\x0000v\x0007K\x000e(\ÆêUöÞÁ=ñ\x000enìuã+ØÛ\x0001¿!æ÷~*y2îTH\x0015n,q\x0017N\x0007å\x001cåB\x0019\x001f<ÄFhæU\x0013að\x001a^_òú¥¼\x0010·º½Ü!ÚÂ|³BÂqÀËpCV(×
¯¢\x0008½õnüúTÅ+}Áªuðjî\\x0005»ãú.í\x0002ï\x000eØ(i
ÞòlÓKÏ6\x0005 g×\x000c=3\x001d"û\x000eÞ®3¾¶\x000fvé|P]\x000c¾ÎÓa\x0001\x001ePw¸5û:ñ0\x000e\x0016S\x001c,Ó¾lÎ÷ÏÏ³\x000bA\x001dÖ%æW2ìaÈsñ\x001ey±ßì4ïÝæ|{{;UÁJÄ*\x0014Äa9r¤%ÂG\UÉ\x00074\x0013êçuÈl@v~1²åÎäCË.·T»jej\x001bÚ¬¥;x>Báânÿgûåþñï³C»ÆRýªA%ÿ\^\x0006ç\x0016ã\x0019Jýáo½Ý]þÛIö>e\x0003Ùeh\x0017ìWà{\x0000M\x0018E÷1¾Ó-ïãZ\x0008\x0010×ª÷!0»ê+c×kÁç \ÿ\x0002&±eè~z¹ÿõçÍÛýóÃýæüéÓo÷ÏsÅ¯\x001dª:\x001a~§è\x001d\x000cþ7Ü)\x0006ÜçI·ùÏ×w»?mÞno/vóë«\x000f»Û)\x0005ïlC3¼ü£¡\x000b3ô
fhIÙz`=ÓÔHÌJ^Év¼àR3\x0006EÒhF.þCÚ¡J;Ô\x001fÔ\x000eWL+éÖWÛd\x0018á\x0002å7É(ØÝ(ÐYl-­°ÔoÃvø\x0015ì\x00082?f\x001aÒMô\x0000®ù»\x0008vòfZgr\x0007ê\x001e¨©\x0013Ã·ýæû§çæ8À]Õ¦cÈ"qÁùô¶\x001aé)ùûëÛ7\x0013ïÈ\x0004Þ«÷#¸RmàÖR-8\x0007ª,Õ(-Àðã!­Jøìü\x001eÞ¾\x001av\x0005\x0001×ôû§O÷\x001eîg«Á(¬j¤\x0017(ÝÕK®
À\x0008zú;`¿z·½ºØÝNx©l@\x0018\x001a\x0010Z
@ùR\x0015ºgäìë\x0019Á]ÞÂ¸ÿB~©üRµ\x001b@Ú%JÐ\x001cè5'!øñæ\x000f\x000bùUÁ¯VàW$ï\x0018¤´t\x0004\x0013¸ÊÔM< ,5Á\x0015&¸\x0015¾\x0002*
Rxòôð[è\x0014dfì?U\x0016èb\x0015ëæe,»7è\x000e¿>f\x000bMèÜÓF¤Ûw¢Àù "x
÷\x0018a;\x0013&Þ/4Á\x0016KÁ6/\x0005¥$'\x0002ær9Z
®ÛLýz»©6y7\x001dô[²¯}û®î¿üöðø8¿!©cQ\x0013\x000bM*Ä\x0003ßÄr29ÝBgsµ{Ò`cµ%\x000c\x001dÐ±\x0001Ú
Cî\x0015(fF]ÒU×öUM¸o_A\x001alY\x000c¶l\x001amÃÁB0¡kN¤W2øé\x001aª
ð¾é\x000f\x000f{þ,\x0018qIõ$&FIE¾Ò§fÄ	\x001c³\x001eV\x0003\x001f6AËûäò\x0011÷(\x0000Üv\x000fý¤¢\x0001Ü\x0013¹õÜ¾àö-\x0003\x000eó\x00028àÔ[ýàx¯m	n&8*gdê Yÿ\x000e[þÐËi\x000c§[ûÍævå.ØÆ-ºá\x001d±Û\x0005;ßEê¹û^ä\x000e¢iûæ>\x0010&Ú~z;ºØ]DÖ\x0002\x001ft®L;aÑ¹²zþ\x001dMë.Bîd÷¶âV8{N[¡h]_¨<Ê\x000fçÓ'r2Îi±çùà}»¼\x0004^ôñ®\x0007Or±\x0019ÜòS«×ýÏh¼9\\x001f>MÇÏ¿Ü\x0014J!×û;'·%¹m"\x000f\Ö\x0012´ë\x001eÝd7ÉOkSÏçvÅÆ¢\ÓÆ\x0002[¹äüþé-r\x0003x/OwøçÑZYLq+[¦¸S3\x0012­t¬ô.kÅGõ¡ ÷¡5Åf\x001bô¢Lº\x0000\x0016Ó\x000eV\x0003w}\x001c&ùRµÃ¹tü\x001bâæ:\x0016ìÁµ\x001e¸-6rg[6òÔL1@&ÙÀ=g2ëxºÃ\\x0005¸)Á[¼q»{\x0006\x0017T.1\x0007É'QªÉ]qè;×rè§.yk¸Gd\x0001J,´kØmV#÷¢ð\x0010½hq\x0011qyæ0\x0017JÜã\x000by~ëðLnOÝÏ'WÅãÇ1W¼±h8\x001cm,\x001d--O÷;O^.Pß¶@±\x0007avn5x\x001e=©©Y\x0015õéfòóÉMIÞ²B-ªJy"\x0017½9\x0017ªpRÝ¨Ü\x0017»¹÷M»9ê\Ðl?òvs4æ'åykÈ]IÞrùt½¨ûÄ 9¿IÓ
 çr¶¦ý\x001c£o	\x001cft·SãJ«Ö¼|úXxl\x001bñn7WYk$\x0010µUîtG³ÙäA\x0014Þ-~l\x001añí==Û\x00016gNÃ¿\x0018d±!âÇ¶ÅIÛrjöP\x0017§Yo¦`\x0005i\x0001Þ4ÃçË¾r¡\x0007çD>µfÄ6¨b\x0007Õ2Çmô¤Ëh5X/pÉõé¾NóÉu±\x0007Ý²#9\x0005Á
Àù\x0008Ò'jÀ}	Þä°\x0008Câ-\x0006E»(}2Èn«DÕzòP·ÜápÈ#+jEcn|ÍÉR\x0006nCSäÖ\x0006ÉG\x0010lê\x0002å]º¸\x0012'õ\x000ckÀË!wM×f,¹,
np"Hz6´2nÆ:¼\x000cÝ¦Ð-úùÍÐHìÀþ
@Èpº»ãlòè»PtMw!\x001fxK,å1e9ù}ÅwXÆùcS ßÁ@3¸â?¼EP¾^/Æ\x0012*¹¼r¸OP9\x0007¶ü Pz ¥Døõ¢CR¸"þ>/G÷:òºKu\x000cS²ãz\x0017ç$ÒT û\x0008Ñ\x001d©)\x0005ÕIãÀßáÌÀõn\x0014òà=+}n@G9\x001cV$bÍHØ\x000b95SÄòõóÑ¥)6ôô¹a®£Va^¤Ø¤^÷ûÝEÓMç£;S¢»&77h¼1'tpÕ©J,JJÆ´B®w!J,\x0005zÛ\x001d\x0014Ûò%oQÃ\x0004ïü\®.6qª°\x0016]\x001d$¨¦t\x0010|bÉ\x000b@·$\x0003ÎìÑ×»\À>>\x0014ûã­} ö·dw·\x0014A®{Ãø¯¦ciÅÇ-ø¯õBì7î[ü¯TÝ=GG\x00157àqø_­ùà\x0002ÃÿÕà·
=æ@)JêýÞA
ÔxêßØh9ô\x0018\x001dm\x0019z\x0015Î,GE¤¼Eì\x0015ÀWÓ\x0010V\x0019z\x0019Ë>øEªé;ÿùþO¨w¹ÿ­B-\x000fENrÚµ¾%\x001e¶Y´
%ôÆ°á¯·\x0017W(w¹ý0-ó©\x0007*PãºÚR ÀÂÿ#¹!-V\x0008[ËEÔbËaE_Ä­½;lu0K\x0014%Ë\x0005ÊÂ\x0006H£»K5w,¹c\x00037ÜÜèuÎ:%ºìDJsÆËÑÉ½`\x0014ÛJ)ø¦Éâ»ÉbÃ×e4>\x001e.¼¾»bsw¼42öýæ\x001cè`OßÈ\x0014¬9T4C\x0018&\x0004T4ã
ï6çð7`WjgªÜl+ü¢¨»ý²ùþ\x001eÐ\x001fªóZj\x0004nüç~Ô4è>Äq¡ô.øýæû\x001d_L&@g\x0005Q9$Ç¢\x0016tÝuw¢ï+\x000fQ\x001fÅxµþ\x0012rS&rÇç0èáÌS+j\x000e¦ã NÛÞ×F"z!ãWîYñ%
z¾#iTÛçQQ,\^ÌtÝ8Õ-\x000bÓ£L´%tîì£´£ñ\x0005è¦ê¦qªsØËãë£þß,Qì£\x001a¿T/@·¾Ø_|\x001bzÄçó\x001e\x0005\x000fær5ÍËT·Ï¬A×.\x0013\x0006\x000b²
]÷§ùÕ^²Ð,\J\x0003«EËAi¡N¾¢¿ßÜ\Of"°\x001c\x0008$"pú¼\x0008ÙkíÏLº\x0011Áq¤è2ªp¾ä\x001b\x001dxå§õÛç »¾\x0010'!»¢Ýd
²ê"t
ði\x0007WÎPK\x0007»\x00122æP\x000fSNõï{bAjEF6K'\x0006Üó\x0011¯|à7~åñ4Êq\÷¶\x0006Y
z¨"²*¨Ö óD*~J+®h.³T²ÆgUÍ 2\x0008ñóBdåHìH)lèµØ YG\x0018\x0019½/g!\x001b["\x001cÌ@\x000eÂ¢V\x0012þ\x0008\Ã§aâ¬4Ê6Èvé&g´¡RÂS\x0004=í	yF÷¶9ÄÃüZ$\x001e&ØV\x0012;IuW
ëý
\x0011\x001bÊ	ÖZ,_ì\x000eÝbdO:å
+´³>|pøtpj&°/gÅ0\x0015¸\x00128Jz[SØ°8ÒÚ\x000b$ú©;Y7\x000fÙ¹\x0012Ù¹¥ÈÖPøRÏ5H\x001c
9t\x001aK7W!\x001e´¦JÄeoª*b\x000bë
ñE^ÓT¤¥\x0013Ò4U¼Ê¼jé±g='ZáñLaJ\x0015\x0003¥Íj©ã:C\x001czw9!ãçeÈNX\x001abðèY\x001e\x001de/\x0010XÅ8£UÜ\x001cà(Jà(\x0016\x0002ÿË¼!X\x0019\x0007Èfù\x0018óÃô³©a

òîà³]é\x000cE·Ô\x0019Â¶cÌs 40\x0015­§\x0003Dèéß3}¹ôR\x0012È2b§èÌpÐD\x00114Æöäcä,bøÖ1N±Æ0L"Æ:¶ÜáOj¬=t\x0012²Z¬)-Cº\x0018»i¡'b9\x001e©"²\x0016éóBbTgÏKÏY~_ÇÜè¼[\x0000úéÞVsÕ #\x0010UÑ«¹Ê±
ÙçlaZäw\x0000¸:Ñ=Dy·Î1
·ÂyKÞC\x0004vE@d\x001dS3´ìTvß\x0014ü­¬}¬nÉ\x001auA	\x0019U
òIí5%/(r\x0002k [WNeëNåÔO7\x001d|8¢×Fêª¬:Yj>wêx½[Ê\x001b4%AK¼æ"âý,N&YÎCv\x0003YDDv^.EFu¨\x0004²$MMeô:·SøQÆ\x000c]\z¡Ø6Q\x0012²Äh\x001c"n"Ñ:1\x0017Iµ±ïä±oh/\x0016ûúé\x001fOfÅÜø\x000eõÚòk¦6`6FyBìønóúú/×WSÊ¶\x0019vÐ)\x0014`]\x000ckyFXTM"ý`8J\x0014=³ÉÕ£\x0019"G³\x0018Ù)½YìÐ'i=Mb'¦D@ª¥(FYåÃìÈß´RÊ3\x0018ØYFy\\x0016©\x0012yÐ6\x0019eXì©)\x001cÜG:Ðñè0·½L¼J.çå\x001eÉÌ­ÈP\x001a&2s8¡>9Ìq1sä@s9¼\x0008Õ)uôÙÌ®WÈlÄræ@\x0005¨©×!\x0014zé;äæ©¬},E\x0006á\x0017ÈàÍíþo\x0003¼\x001fçR\x0007~Sn\x001bö.Ï\x0001{\x0011¸å\x000eú3Ìn·ß\x000f÷»ìÃ¶±ìS÷û×r\x0008¯e\x001b¼`7	{\x0006ñ5Pø.Ù\x001dß¹W']Á³dS:Dò¸ßÜÜ???Ô´Çtj©ï^É.U\ù½OC¹Ünnv··\x0017ÓýIUÐ\x000eùµmå\x000f©\x0018%\x000fº+&\x0003,·UÅÎ2+\x001b\x0010
\x0003B«\x0001Öq.³T¬Íªà¬yòËÑÉ¿ÐX\x0018\x0010Wø\x0006\x00027\x000f\x0010\x001cå\x0015ØU\x000cP£;æ2\x0003¬\x001a\x001aGH\x0001AHp´³\x0001]I%\×c\x0002ï\x000f«\x001a0¼SÚWx£lû\x0006¢ Ü \x0002­öOÛñ§\x0006-äw\x0005¿kæ7\x0014I3Rp\x0013|\x0001\t#ôÊã?ÈVu¶ÈV]8LÁ\x001bô~éÖ)|W`&ÆóÊ\x0017ñ\x000fë\x001d)×·\x0019`LWOÁò}JvUÃSÊÜ\x0006\x0008Ê/ï/\x001eè{\x000f|µýçÏûæw.qè½ÓÔÁ \x0005S(®1\x0007â´»¶}÷nûf²Ý
IkÊ!µ-ØûO¢ÇCmxf\x001dS©'bÇÕØ¦À6
ØB«#SÓ¹\Àz8°{h6 >.UEÈª@V-È¯Miqv"\x0004,©	\x001bÎékÓÜÖ\x0005¶nÁ[\x0006;"ë÷(îé'ÅDÓljei7ïü\x0001ÔâwCàe\x0003ütÿ\x001bn&³Ó÷P\x0015
Ë\x00146.%µsÉ\x0012[ÒÇ:»íän\x0003¼Ú}ÀídÂ\x0004\x0013Rì¥ï>\x0006¿x%¢wXë17£<¨®=aÖv"Õ!\x000f|ðbüú×'cNön"¡©CA\x001dZ¨5I\x000c\x0007åá\x0008\x001auW\x0013v\x0010ã\x001a[ÕØª\x0018lÕ2ØïN\x0001+²rLÃÀÝG[kUc÷·>ÄÖ²\x0001\x001bK&4a\x0007*o\x001eHh{9^ÍTm
lÓ­¨½\x000f¿£ç¿àÕéc~>v1·MËÜVÔ>6Èàº\x0005I\x0001ÜÃº\x001et, cËXsGµ\x001d7\x0004O\x0011îøàõx±\x001a»ÏâBlÌáúCì#ý-(a)Âê¼\x0001%\x001e\x000ca{ª0À´Åõ°}±ýùíOº3'	Üv¨\x0006\x0008'	ï#v<tTÝßy\x0010»¬Ð«\x001fí;Q(iè¾+äD;¢ùØÚè¿\x0016\x001dÉá\x0017¹#yWÇ¹ÿôùË~®GE\x0010\x001c×ÁVÔ	\x001fUä\x001cAÄíÕ»÷ÛSÈÒ¸!2~\Ê¬eà×+Ì¤i\x0002
´a¢à,h%qVrñ@Û$.Ö+ë\x0012¨Dílhð\I­JjÕ@
wø¶a½g-xa\x0003\x0005QP}uFï<êAb\x001aR\x001bß@mÏl ¾K@jz­p\x0013¯Ð|l¶añ¬F\x0011Ø¼¤&\x001eü,ø\x0015Ù¬6«õ R\x0008Ðøq)´E/:À8½aµ8uc¯£6¦ ÆçG´¼éYpCrv\x00018ªÔ)\x0000\x0005ù×Úö\x0017\x0005µ\x0017ÇÚ¡¦\x0017u´f A\x0001Í(æè\x0007¢\x0016ù\x000eÖµ\x0010©SÖÍãþcz	
·û©xbÞ$1\x001e#`fwÝ }\x0017If\Üãær{^à?»½ÈÿÙSðÄgÇ0I\x000b<\x0012Sjñä²\x0002¼gxèWÀhó°\x0017àyèñ7­£¯»Ñ·îëÑ\x001f;Ô¾Éå½e*¿jRö6ufú\Ñ¹\x0013Å Iô&tb_ãsgØémêËôn²+ÓAurÂ7­ø±SÎ²ª\x0011°c\x0013ïpuø"Wã\x000fB"$üA\x0008üÿû¿þïío\x000f?Î.Ç\x000f°0¹ï¼@=û|7VEÊÅD)Ö \x0004¾Ù~¸ønª\x001aàû\x0010w¡\x0011^vMÝaXè\x0005\x000eT\x0012ã71×ËÖÃËþí\x001fáñc\x0013½váá}\x0017-UÂxõ\x0002xSÂVxÜ)Iÿ\x000b\x0015zè.DO\x0006k]V`×þ°µ§Ö^\x0014^¾ùòP±TaAD¥=Ë
úÈ\x000f¶JqWË7ï/&·\x0018«às®Â2`£Y\x0013^Á\x0014qÜ^ª\x0013*\x0013=lª\x0007ùÉZb-\x0002¶¦ÔÀ
°\x0005ÔDOy¼fD¯u\x0000\\x001eÒ^¾¼¤¹¼ûéñá¥BUURÜ\x001eFTÓJÿ"I\x00129S
Øw×ïï`2ïÞ\^ÜMõµ\x0007áXÓ²	==Le?\x0017k<YÁÞZN~ä©$×\x0005¹n$¬`£dß\x001ez`Ì'
­«ÉM1æ¦qÌ¥¥\x0001W\x001cM	\x001c\x0018ðñÐÕ\x0002îbÄMãKO}\x001apãè÷}7âfr3©$/\x0016¨i[ HNë\x0013\x0003Äíºå9¡c[\x000fî\x000bpß8É9¬ÒÌ4Ã©é\x001bæ½¯¸­ô\x0012\x0008HfMó¶")MØw\x0012òKífVCïk\x0011ÎÆ¹")¥ÃJl\x001fÏ\x001d`º§~A®E\x001f^ç\x0008?	\x0006¶YàdgòlA<¼Æ\x000ecüAZøÅ+W<¿»ÿõ×ù¯ßR;*¦ÍÐ _Å¢QÑ\x0013\x000fÒ|°óÿÝîæfòá;q«^sÀ$\x000fK7\x001b,°K«Ô;ÌªÌ¯±Úú<àAù\x0019d³É},È}l WàÑ¦¹îµ÷¤	c¤¢®u!ål®\x0005îúnGiª\x0008Ñ2ä:ÐÍÍ;\x0013)õÐhMÅÐ\x0001<ñÓ7·ùä±$o\x0019òÔ\x0010&\x000b\x0018Ë\x001cFL>®\x0001W\x0001.ÃÐâ 	\;ü8x¼zýôð²ù\x0011¶\x0017Üa~ùa?_f*Fz~KIÜùÕP\x0007K©A(\x00111ã=üõõÅÝæ»ÍîíëíIC\x0006s\x0007
)æN!à8fg\x000c#»Ô\x0015\x001b.0Ô\x0002\x000b9gh8Î3\x0004îãéêÜg%Äð*Èb&}xøéÓìäµJ'¬BÕLÊ½u!\x0004×ãNÍ`\x001e}¸xs5¹\x0000\x0012µêsÏZ\x0015ÉçÕØXò\x0005D°+y¤¢YMn\x0006lÎÒI\x001eEA\x001eE\x00139Ú)«5§\x000bãÖIä.\x0014ÍM>¨GEòTº\x001cN(\x0012ÿÂË\x0012KÃÂ8a¼!Â\x0002òXÇ\x0016rl\x0012C\x000296°x\x000blú¬¤gäÏ%wº\x0018sü¸\x001c\x001c^(ÇP²
\x0015`ø×çú0$w-\x001b1Ò´\x0014vD°¤U¥¨2\x0007ÈÇ\x0015ÁêÉËyîæy*\x0001Í+Tàð\x00139\x001c¯D.WÜ\x0015½,ö\x0016ü¸ÜÓN+\x0014N;ÒXí*0ù,föÖ2¼uðö2Ô\x0013^°N-ù\x0004J¢ö'¯SA²PZ®²7p\x0010¾Ãô\x001cY\x001eG¯ÿùß¿=üó¿ægÞb\x0013rñÎ\x0007\x0016µ1'Q+|L3ü¯oOæÝ\x0001ª0@µ\x001bùÂ.\x001bàYÝQã\x0001K\x0006øY©Ãs
Ò©â\x001bÀÏm&\x0004aXÂ+Áû%ê®Òõoâ\x0015µÒèÓÍµ÷1\x001e^¾âïS!HT/Àòª´tLé`\x0002«\x000c»YoçÛT\x00072\x0003Þ\x000eám#<¸aÄ®$úk|¡aöñ¥»\x000cÞ\x000fá}+¼Á}>ÓÇ^ßîS>øñflGéGê+\x0008=\x000eÑcë¤é®\x0018´ÐY$9LHé-\x001aø\x0006\x0000ÐËÐ\x001fLÎ/öX­`H\x0012ÜRX\x0015\x0006~<S·^ùPãÀ/R9NOÂdzú|ÿ8ÿ\x0012ë¨\x0000
»iP2¦\x000e^ð¬·3$Íñ
òO×ïv'áU\x0018Â«Ð\x0006\x000f\x001f;<ç±WÝ1t3ç´2ø|øþí\x0017áhWÃeJÃ¶G>Ê.Ð7~é®a\x0007§;­Øþ mB}=åç×\x0016¡Ê¡äâ3KIaÒ{Ï©\x001a\x0013ä\x000fgüô\x0001e\x000e\x000f(sìª#§Nò¨ÍÀz\x0012>t¥Æ3äç«rÌ\x001b\x0007Ýs/yï w>\x001f\x0004\x0017EÍQ®A×m£\x001e\x0002§ö\x0018øÁÌG®o\x0015q¼(`Ñ¨\x000f½z\x001ayüÍ\x001ffð9´À4\x001bPL|êsRLüÙÔ\x0001*+âAãX,Ù/ï\x0001pþÑ\x001a(./ï\a\x001byÔ~4\x0006êbDî\x0010ù@¤¹ÛÖñÍOzö\x0007Y'Íf¹\ÔvÁ\x000eÔG²\x001eóesþøô2û ÂÉÏãàÌAÇwn,\x0019×Î|pÏ/¯ï¦\x000e!\x0002vv\x0008ììR`ÁêòÆç
@\x0004¶s\x0005;Ï3\x001f8\x0014Àa!°ÆxLæÅ>¬ù-Õ*z\x0018³^L42¯âzÈ\x001bõR^¸ÆQggß9Ò\x001a.\x001fvV­3À²ß)dj¦i\x0012kÇ)ßÞv½¨M¤È»ÛtÁólbUL	ü¸X\x0004.á÷pa#_Äð½\x0001¶Ôú*â>)-\x0011wYiÕÄØg*/;\x00175§Õ[!yÍøE\x001d±/6¶T
»X\x0006\x0016\x0006qVsOãº1\x0016\x0013\x0012âóµÎïÿ}u¶¯\x000e5}ÞÞ¿ÌÏ[M8\x001fzÖ8Ã}x]ädZÏTTz»»J\ ðAN¨Î9¡-äÓ]0\x0017\x001a\x001dz\x001cä®f¤.Ì@WN¤Ü.\x0008\x0001¿x\x001f¡·Ý¯\x000fî?ï#y¸Ëð¦§ÄYîÿ!Xk.}\x001d3\x0002o»«Ý»wÓN\x0012âë>õ\x0002ñõAêE=¾\x0014Tmç<hìªÎs}"Éu\x0011¿)_ÆáO­³\x001fS\x00192>KÈØ8cÖWÐ\x000fR\x0002¾H	X4úy¾§#ÑX\x0019æOV×äW¶à?\x0008×¾×g>§\x001c[|w¡Ù£¸T\x0014o\x0008«ò\x0007Yð\x001fd\x0000ÔóÛ*8\x001f\B=\x001aóYØVüV\x0016øø±
ßxÌB|\x0003÷\x0007C©Ó\»cÌêk·È·£õ{ðòõ{_ÂÊ\x001e\x001aË Ù\x0008\	º[	Z}½\x0012VZÉàNãwÑ\x00179 ­\x00079ñq¿¹}BºüàÞ`®c*ÙÄXEöwì?LHÞ\x0013N}Ünn¯ñãÎZÎÝ\x0014½³5\x0004EWÓ§ç\x001f÷\x001d¤À\x001c\x0007Z
ûkÃã~ÛùõíwÛ;IÝ!uYþU\x001dºY\x000fî\x0002]ø1îÏØqFÀ\ì¾H\x0016±½hÀ¶¬­k½Ik¤Ü©Äiñ¹Ø²OMsD¸\x0006n©ù¦'}×'ÙcgÉ
Ü&&i«aÚz\x0015E\x0019\x0006}÷üð4»¨\x0007°<\x0015h*\x0001·UJÅf]Ú Æ;%\x000fcpïn/®'KÔÊ\x0012ü"©,Qilöë÷\x000fÏ\x000f\x0015Ý×#E,},'æ\x0015\x000bìFøó\x0018:UÆf¿~{q{1u'Éèº@×\x0008tåÓ\x0019ô½/
+¾¹zþ	&ËÝþñþÓ³5\x0015ÂL\x00125i£ø\x0000JÏç3¸ãàov×·o`ªÜm/wWßÝî^}Üÿ¸ù\x000cÿqþÃ\x0001¶)°M\x00036·åm%`Ö}®g¬¶¢hëA\x0002Ú´@û3IÌ*\x0005ðäL=~o­§ö\x0005µo!NîlFÓI\x000fG½bìÎÕØÖ\x000e±QÄn9¶8\x0013$Ú¦#¦dlÒï\x0000l1bç,\x0011fW\x000cµk\x0019jðG$-Fðl³Þ&\\x001a}`æñjê¡î£_Á¯åóÚGí*Ï\x001c¯FßMì5°<ð\x0003á\x0017è\x0007\x000e7m Ìæ÷÷5Î8Ö\x0017çÈyÄ$uªYãôn\x001bôx\x0013êáî
F\æÓóû\x001dúä£¶Ø$/
Ùú_¼JýÙÀÇÇ
1Nï½£4\x0005\x0017
wÃÕÆZ«wjVN×ËË$È9>tz?ì¥º°¤ºð¸Üì>>=VUPeE\x000f\x0013¬aE`)Ôz?FÓ\x0013àï\ò:M?KØAA=ÂrAý\x0002Z/
?3\x0007Üb(Ñu\x0001ðªbS°ú¯ñÇOþ\x000fåQ`öÄå}
E§n=ûçýé\x001eÊî¢~õæË?ÿûùþáÓ\x000b¢iïµÉ9}8d)«\x0015Å¢´"ESa\x0003J¾zó~w»»¸º{\x0005s\x0015ãÎ©5ÏövûÝh\x0013ò\x000c¼G]M\x0006®EzJ\x00032ZJ	\x0013â\x0005:Ùí`p2j0pó=
\x0019\x0015B"S1òå\x0002áF2¸¸Z2@JñyïÏ\x001d¢&FÂéTÚ\x0008\x0006ÓÁW\x0005S\x0000\x000c¾VÌàB2G­GK%`ð§\x001fÿö@<níIø\x0011þ¡tûyÿ§\x0013l"_~`Ë6
Ó\x0012§.\x0005Rp°\x0002Pøòüúê.]×þ´ýËõ,>^Õ|&Kà\x0003_~uÉ|ô\x0006\x000eQ®ÂÇ´Ï£Î|0RÓ\x000e¢\x000cñ%íº\x0015øx­Vóù¬4h\x0003¸rø\x0010A|øì:xpÞØß1\x001eï'\x000b¾ÝTx\x0012÷½§;<ü7/åÓáßü\x000cVÇ_>Ýo.>ýø\x0005|{tÌ`wù\x0008nÍËÃÓ§É=ÆyðØ8£ÅK\x0011FGÔ\)+¢÷Å8þåúj·¹¸úîýÝ;¸<£\x000b\x0006;Í982w\x0017×W\x0013ûÍ8¯\x0016bcés!\x001aTõJÄtÝ\x00101äî
k2ç5ÔÄ¬²Â!0»TG9?¤Â0ç:µ5óÌma¶:å¸à0\x000b|KJÈ:§Èá0°22üûBãdVù&Ãl0\x0004äaöÞ­Ì\x000c×­ØÆì%OçhRÝtb¶ÇÙ&õË\x0015±\x000bÿj47¢1x\x0015JÌ.§\x0013\x000138ì+3Ãúk0Fì$ êÖ`îÎ\x000cÌ!%\x0014­É\x000c\x000e\x0010þÕÀ\x001c45Á¶\x001eCÌÙKðX¡c¾.¯	
+P¶­B¸n¤¦ À¬äY$dÏQz½\x0006òËþgõøëÀ}ý°æ-+OZÓ79¬p|3®³¯/¶óþëù\x0008ñ_§¶^xoM\x001d^Ò5ÀÓóÿëòéÿüñSzÏ¯
ÿº|úüðòrÿËý§Ï\x0014Ñ¸G	ïAµã¨¯b
>[$_\x0005¦,©¡¯"ËÇX^®ß]ÜÝíÞî®ÞQ\x0010cÂÝ'J\x001cõ_ÿþüøùçT\x0018\x000bG]úÁRj»Oï}¾ÿtÿåùÄþn°&\x0004°uÎ$\x0017#/\x0007;¡v¬¬\x0006¬·»ÛÝÕîýh=ÎÐcbPúQOèrà\x0019³\x0014¾"æCÓÓ\x0001d7k\x0000âdI?ê\x00019\x00134åtaJ>neÂ\x0018\x0013þðÓó¿ÿ\x001f7pìùuíæáþùù~óýýãÃËþ\x001fÓ\x0011¥òòöáCÁ4\x001d#%%
SnÓüvs±»½Ým¾ß]^Ümÿ2\x0003\x0010\x0013lÔïð·ÿ÷?û?tûðÛÓãczOØr\x001dûj°ùÒÑ&5-\x000b,\x001f/¾Ó\x000f×Û\x001b;ê¿î_>ª§ðÀ÷Ï?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=|jaX\x000bØé6ôÄK¥\x0012ÇlLñß¾ºz»È©F@g\x001e<rªÉcHábÓØ;S\x000eyÁ\x00142+ëÛ Ý)G«H¨þû?ÿëò\x000f\x001f\x001e>6@E\x0005H*\x0004|³\x0002,îfÃg¹<»>»üîúêÍ&h5\x0007­ú@'îÈ\x000cZ\x0017^ÈmHAo\x001cò~Ðz\x000eZ÷¶\x000c!eß6D>iµ²î»
´6} 
±G)t8eR¡ ÖC¸ýÝ\x001c²ëùá#\x0013ÙàËèÝFnq?è0\x0007\x001dú@+öCDÔ×0\x0014\x000f¹A|°\x001bô´¬*é\x000eÑZ\x0010«r\x001a\x0003¾ø¨Åÿ±\x001fu¥<döà1däègò 2\x0015 6º¢¶!«p¢¤á\x000fXIÿþîÇ?}¾ÿH\x000eïþín?æ ¹ÓBâ(æa\x0006>i»Îyôû\x0017ÿðîòM":¼øýÅ\x0016t5®z¡\x001bî»é§{¡&nÆÈõ\x001c¹îD\x001ee¡ÞÑi0 O\x0003¨}d£ÈÍ\x001c¹é=óÀQÔ²ô¤c§\x001b!_YÕ×\x000eÝÎ¡ÛÞC8V\x0007aá¦1\x0006Öf½îÜ\x0008ÝÍ¡»>è\x0001ëµ<Ãë¨ó\x000fÜSÆÌúl`#r?Gî{"ø['Ó©¢\x0015×KZÈã\x001cyìD.U¡]ÆÕ0Ì]ãÿº>]×\x0006]Ö:½S©\x0007p¸yÒ^y6Îrêë$|Ø+¥.;µzö£\x000b\x001ek\x001cÎ½L¨m°\x00044b¯ÔºìÔëÈ\x0012À\x0003È*\x0014J5S®Ìú``#ôJ¯ËNÅ\x0018x%p},!gjÕ`Ök*Ð+½.;\x0015{kbly©Üèj
ôõ^¨Fè^½\x001d:p³t£GðÒëFèb½\x001d\x000c`\x001d#p!·tóäÈàw\x001a*ì¡\x001f;uÒKbÊt¼~\x0008Ãå.¬lì5Jp¿yô\x0018Ù¦
ö\x0018xÕUeT¯MÂ§Éz]\x0016OÀ\x0016W¯ìLnÇ^éuÕ­×\x0003\x0013\x0006aäïù®[öz×v\x0007¶c¯Þ©ê~§vý¤\x0004\x0000Cgär½µ\x001by8LÃ>ü\x0008àzxüØUÜg) ÌàeçËoP©\x0001âß_Ü~suóf\x0011q<E\x001c\x000bâßßß=þîõÃýóóýÙÅÃóÝçýû\x0002z\x001a+þBRÍU´Ypí¸//nÎ^_]ÞÞ^]\Ý^¼[Ü\x001aÀøÕ\x001c¿\x001aßadÄ\L©'Îì
åØ,\x000b \x0007\x0008@×ÆZZ\x0005\x0004è\x0019|ëqR3x;\x0007o\x0007è­)þ£æd\x000fëí\x0002¹\x0000¡_\x0000P6¯áíQÎr½A¹~à\x0007Wù'xß+\x0002¦\x001eH[	É\x00016Bã¸Î2±_\x0006}ºGCO{4~ÿôñþ?}ýásCÃ\x0007æ(\x0013Jq£
Ìeã×{º~ÿêÍåëïÏ¾¾~·¨æ\x0019±#Ö\x001de
oàC*{Mòvã¾ïlæM\x0007ä`
A)DÙ.-l¼fÃëÝØÎ\x0011ÛCö8ÉÅjG2}ÇFÝ°\x0001±#v}×jCBå*[?\x0000ñz*}\x000fdekó\x000fP/Ý¹¾{øÔ´§\x000bÂ6F­e\x001eRcL¡Ú·Ll®/®Þ®mèbàj\x000e\õ\x0001ÇÍW¤ñB\x0019\x000c1Z\x0016ÞNÖ&àf\x000eÜt\x0002/íY
¹%	¸òÜeÃKlÁ=_§îÊû¾Ë\x0012ÊM¡û
\x0017Å²YÝÚ\x0001ütv¹]?}~øxöòîáãÇ\x0016û\x0012çë1BiiÖc¬÷õ«wWoÎ^^\½y³ü.Í©M4Å&\x001e\x0002\x001d\x0004ïàL<µL¼¤Kbkc§G\x000bh=\x0007­{N\x001awxQ\x00143ÄD\x0006(
èx³\x0005´¶= !º4ª\x0004ÉÍLéBX\x001f§lÁìæ]Ïí\x0000y¯1°§Ë\x0011l9çUÝÙÏ1û®söÅÍ\x0001ûD%VZ'Ö¦\x0016Ða\x000e:t\x001dt\x0019èBñÀ3bêQ\x0019vÒq\x000e:vé@ÙY¼\x001cÌITì".È\x001dyêHJZtt<ñC3·µ)M*vÔ3]ZZÉÒ,&¦2¡ñå¨×'\x000b\x001aP«ê¨U×Q#s\x000f«iÉ©5ã8,×\x0007j[@WwZu]jÌÃ²AT%æúÖ»3\x001b@ëÊóÐ=®\x0007\x0016Ö¸õ*ÄÒ0aÌ´`ÕEÝú´POÝ/\x001f~üãý§,çª#ÆM«Äliÿ^oñxyõâûËëWË¹Ó.B=u\x0011¶µ\x0007O±WÝóa^	\x00196¸÷µs°ö0XË9\x0003<YöBç«àÖ7on
úÄm\x0006¯#ÃÏg/>xxÜïçÛPj`·i\x0003±¢¬bÙ`%ywöòÕ»ë«-¸j\x000eW\x001d;MdÊà\x0013ÃXÞÙ\x001c]i\x0004\=«®çÕ«£ic¸y
þt}Êb/\;k{à\x001aë¹ªaÊÆæ¨6úÌ÷Âõs¸¾çîÒKC:r4-\x0004R¸Çi\x0004Ü8\x001bÃø®&\x0008c¦\x0015
\x001btØ;áÊZ3t¨\x0006AÞ¥Ò¹À¢å\x0006ëõÐM¸æ4þ7Sü\x000fh_¸Û\x0015[Ì5ïÛsL-:u\x0011{·"zwöúúb\x0013ªCUG¡BxD	ZmÈ)´½Û¼\x0005{ê9R}\x0010i,\x0004D¸<@Åt=}µ\x000f©#µÇ\x0006P®*{=dÉÓ»±}PÝ\x001cª;x¨Áp {P
ïà\x001dÞm\x000cOíêçPýÑS-\x001d\x0011øûóR\x0005êñÚ4Ì£ê¹_\x0019\x000f#aQFÜÆ
è}Pã\x001cj<x¨RNA9b\x0017e\x001d«ÙÒ©;pNÁº\x0005ëí¯¿+<ÓRätFGUjt\x001cÌ\x0008­
#¶,{×\x001cq¬¦Âj:T+XÐXúb©6\x001fîÃZ©*yPW\x0005Q¦ùp§\x0014·uOË\x0007ØTY½yP\x0001`&,LP¹1A97\x0010ªªÞ:ø®\x0002ì?
s:äSæ5\x0002kíª\x001c|X\x00155±`åí\x0004Ú©¡X«¥>,%J­Woôí\x0018\x0003 ªW¥¾*e°1²\x001cª=IËÑVªzWêè»Ò× \x0011Ü/£'m5à\x0002èêaé£\x000fK'&îÉ3¼\x0019ÕnP}îZ½+}ô]\x0001T®TºâÙ
'#cÝX?±Ï_slõþ y\x0015sïº,b×%\x0010X\x001fdÛ@kOÛìÔft{÷ðþîó§³×O\x001fö®sÜi¦N^¯
\x001bÍFÝýöâêëwoÏ^¿º~µ\x0005ZÏAë\x001eÐ^²V0Òò>>¯a:õ\x0001\x0016Ðf\x000eÚt¶ÜM'MÁ×v:éUõÐ\x0002ÚÎAÛ.Ð¾ðý\x0000hGä\x001bº0ÒÅ°êÙ¶vsÐ®\x000bt4Mïz#¦îÆ¬Nò1V|ÌíýÃcîZ|l\x00187%\x0013\x000ew\x000fÚ	^»çõz\x0000y{yuû\x0015o\x0016H\x0018´V= E®¼\x000cÚ\x0015®
l1"Ð\x001b·£\x0001´Ö\x001d q\x00160·vM$emZo"i\x0001mæ M×õ\x0010Ì4\x0007GQ\x0000¹ò\x0000ZdýJ7`¶sÌ¶ç \x0005\x0017ÃAÇÒ«¨4Dz½¤\x0005´vï\x0018gáuóÚQL~\x0004z¾½\x0005t\x000e]'­hÞ\x000fNzÖ\x0015jÙ£×ëÍ

 §|IÒx¢\x000b5÷²¦Hä¾N©é!®&"[PW*Oöè<\x001ciÍ\x001d;zZ²¤ë¬Ö«j-¨+õ!{ô\x00076·¨Ò+\x0003Ð~£d\x0017êÓ\x001aj\x0014·þåþÃÏwÿqÿ¼\x001fsxñbÖ5o,³?ol¾}÷òõåõËº¼Ý¬æU\x0007d\x001f8\x0004\x0004¿®\x0010êBµ²l@¬çu\x0007âhH^WÍ´½Ö2b·¾ ¯\x0001²C6=÷"ð0¿¶+{ãÙ½³ëcM
í\x001c²=\x000e9Ò D&ò\x001fòUö®Ð¨­·ù5@vsÈ®\x000328t´LN{W</êsU¸\x0001²Cö\x001dÕ´Ë,Jì\x000c¢\x0010!ûõ\x001aw\x0003ä0\x001c: \x001bÁ¹XmØ\x0019±,¯o\x0014Þ8Ç\x001bûð2]s,»J\x00000/s
\x001b>ÝnÈ3GcV9Ù²Õ&z\W0\x0017ºÝõ\x000cb\x0003âÚð\x001d·|\x0012n,z9-t{q¶ÝcÐ½áÇ-\x001ff\øí\x0019øKª*Fî\x0018\x0007ÈvÝ-Ú¹²#ò¸!Bi./\x001aUø¢\x0012¼x'®ï\x0013Þ9Tç\x001cº<\x000cÃ]R¸"(à¼\x0016ÑùÞËNô^	Úýï.B*[TR*­X·¡ô{®÷\x0003§ÿàòlÕõ<¥²\x0013ÅÔ!È&­SÏmIl\x0018¿sf£\x0001²CöMB\x0008nÊ·®F­»
ã\x001cqìAÌTb¤\x001aZ®ÕúÝ~È3Í<#d:YÇÒ]+léHÈT\x001ctÌ\x0013\x0019\x001dÃ\
R*Þ*bËZØH\x001eíÁ\x001cO&0á\x000ffíio>ÿùþñáùìÛç»Ç\x001fï\x001eösG8¬SñÚtÁEU£\x00147n\x0010ý¿;{óêÝ\x000f7W·gßÞ^Ü¼¸¸Z$`\x0019ô\\x0006=B\x0006åÊ\x000eòPÐ`JW¬l\x0016ÂÌ0#p¼ÕP"\x00170õcÚBV\x00137G\x000fÈ`ç2Ø\x00112à\x0008\x0010ï%gæ=\x001d"÷C+·UkÁÏeðCdí<6ØÉ(\x001bIÍ:)É\x0011!Â\0B\x0008Y%Áò\x0000ç¼ôNo°\x001f\x0010"Î\x0003\x0000G±lý\x0006ÛK2xÄ¨côD¨^Åë4M]kq®è6ñüE4\x001bS×\x0007P\x0010j\x0010¤^¡OáI
nhvcXÿ\x0014#Ì
¢
wdÐËvÌ\x001f\x0017ãæ@A³\x0014#t¬\x0005ëÀÄ	1rÚHÛRå]P­R¨êY¨\x0011ÏÂÆ´²/\x0011\x0004.·éPÜ¸ÙÐÙ,Eõ.Ôwa£ÇþÎ|£JMYÂ~\x00137\x0007¥¨\x001c\x000f5Âó8±,m\x0017¥CE3\x0011\x0014®Ç\x001dþ[¸J
7ä]²\x001eODÞà£mÙYÁRTv[0ÜÖ+.øãeÓVrúO­OB\x001e1Ü³Æ¬\x001cU¼\x001f\x0011VèÂÙ.yöfepÅ#\x001f%;í¹pj>
óöþùùn?nd¤Ô¼í\x0014»áøÉb~+x{y{{±	×Ìá£pqm\x0008
L©R3#±
ëý!»áÚ9\{üt\x0005k\x001a¸j¥\x0007§ð[û°>:»\x001b®ÃuO\x0017n.©w¼\x000c<\x001cc
ÚõÕ;ÑN^§SÕÄÓ¥Ì¥pàÇi1î\x0018¼ÕÝ//\x000e\x001fDÆë°©3ßÒs\x0013åV¤µ\x000fou\x001bäáë½ò<Vï%¯jrºôÉ"¯Ù\x0000¼ZÏñjÝs\x001fxQ\x00136ì\x0005æwdò­\x001d\x001bxOû®\x001aD|ûùññþÃþ×æÊ,\x0012.¨ ãµÞL\x000b*¶\x000cøÛw77×[põ\x001c®>\x000c×jÎ`K\x001dÎy\x000b\x0016/MÛÚ\x0004²\x001b­£5ÇÑúÂq¯}A[¨³íÆ.Ò-´ê´mZ¶é\x000f\x001f\x0012ào>ï/Â 9£à,°ã&1\x001bua8Y7¯¯\x0013âo_½[,Á¨ÓiU:¦áMË`
\x000cã-ÌH«Ç»÷=üp\x0003¤ãÛð5öË¥oÂuóðãÓÝÊAÇ\x0018J\x000bo\x0016KÎØ8K·+\x000b/Ó\x001fÝ\½xu½¨\x001c\x0018±×5b<£=%HcáÚ5Î\x0011©	\x000eÿ,>¸\x0006ÀJ×Gß\x0000\x001b´oÉ4\x0010{
*\x000b\x00188mÔSö¢\x0005±Q5b\x001cÙ>\x0018]õ\x0004X(jï\x0000À4cíY¾Æ{\x0000Ã8\x0001ìÄj\x0008ö\x001fûâÞÜ?~z¸>ã¿yzØÿøÀDó¼¥à¦\x0014­M!a^\x000eüÞ\Þ¼½º¼=ã¿yuµ¨2\x0008¼«À»nð\x0018(ÉB!M[U`\x0006*¿²é\x0008úP¡\x000f½è/ôH¸nUÂ%»¼î\x0000úèæè±w \x000f½M×{6){#J{¬^Îj¶3Ò\x0019\x0000è
ô\x0010cj*\x0015§\x00069\x0012þ´# ÁÇ%\x0001Ýðó\x001cWý'\x0015K¯\öö 5úØÞÑØ\x000e WÓá\x001bæxË\:\x0007à\x001a¾é\x000f> ß|÷S[)5\x001eÀnE\x001d>{±óªTÀn8¯(ð×z\x001cº÷3*[ºùï;%\x0000O\x000e\x001fÛ2²Ú1\x001c9;Vã\x001a?X¬^øØkË\x0006×3\x0013²ÉZ.Ìµ\x0008`£:i\x0002¿úW´æ\x000f÷Ïû	Ñ°Åã£8\x0014©ª(JÉò^»Sð?\Þ.\x0012£1x=\x0007ÿ+:³	¼
ªdLÀU£b¢ÖÀÝ7g\x0007öyÙG¥²O\x001fxð\x0015JËW('¯ÊîÌålÄ\x0001ðºº5º÷ÚX#|\x0002×¬Ñ\x0016$\x0015§øy9Uu\x0000¼¯nï¾6ðJiQ\x0006®ü
l«\	þ\x0017ó\x0007ÀÇ8\x0007\x001fÅTµ\x0001g2a¤.\x0000å¹P\x0018\x001aÍ6x9ëî\x0007ðøÙZ£¥|é\x0001>_åüü\x0001ôÚVè±Q¥\x0013½æádpÇÐê&ôé¡BX=\x0002ß×ð}/|Q¸¥Ó\x001c([V}Çåp¶\x001d½©¯é½:\x0006)èâc»\x0002\x001d~ñ\x0013¢Ü\x001f×nÃW²Öö²WÝ\x001bg¸4\x0005á §ÄÚwôîðd\x0007|U©LõkáI\x001b|¼ïÔ,\x0002\x000fWÓÃ\x0015ì~¿¹\x0003¾\x0015|øì¯ÙSPÖñz
\x0019y\x0006;úw_¹úò¸îË£\x0003V\x0007s\x000b¯a¸æ;\x0012\x0006ê\x001dôøæèC÷ËU¥*\x000b18O°J\x0017¹¡B/\x0017ÛákmæðµþT\x001b|\®\x000f_\x001bM^¦´°Ä./í9¾Vº_m
Ãóå\x001aé3zÞ+ãÁ·\x001axñµ«,.~ö¡ûÎ\x000fíÃ¹¢Ã×¢Ð,\x000fSµÃ·ª:ü¬ëo=Ó\x0019ç¦UDb$ðÒ|¸¶öwl·¿×B\x0014ã"kMá9c/WÛ\x000eÀw§ð¥âel\x0006b[/\x000fÜ)¯ÄÈ(EÍ3#ltÿ>µÐè4s²ZZ3¡¶Ì\x0003\x001fír·ì¡ëS\x000b\x0017¨Sô\x0013äô\x0002Ú0êBwA\x000bBî\x0007 Å¿ø?þÛü¢ÿ\x0005N\x0008Ýò¿¾øãýÏ\x000f¸bé»\x000f\x001f\x001eÿðù>U~²mÖpã\x0008býî§ûß½ýãÃý$àRC ¤\x0005\x000eÂBP6Éñ\x0004A´ÀÁz¤3\x0008r6@ýÃÅõ5 üÝ7¿{ûýÕå?}õâûËW7¸j	ÿ£W7ß½»|óÕÃãOïË_\x0010ø?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=ýôñÏwé¯/?}X1`cyÉa¡õÚyn\x000eü¦C\x0003Ï}yúâù÷oÒ__¾xrvÐ\x00063CÍ\x000c\x001bµ¨\x0017\x000fß¡\x00133Ï;LÐÝÆÃ	h¬¡q\x0013tîvIÐ)N6\x0019\x001f£g¤cÙÔÌf\x00033Åg\x000b²1Ü®¹ß×hu¶^rÙÖÌv9)A^ÔFÃ\x0017´\x00084Ë>·}{ÙÕÌn9\x0005
¬:R\sÉç¬¸ø</p><p>,vdö5³gVe}÷×që2æÄh£ÏÕ«
B\x001a:l"ÐÉÔ0ëÂ\x000c;\x001et¬ã\x0006á(ïÁ>Hmæ¶å\x0004}¶4l\x000cúðø´\x0015µzQÌ\x000bu´üöþ¥\x0011ÝaÏÖ
R·Æp5ÔÀS¹8¹Ä~ÈÔ®Ûñ2AÝC½Á\x001ej¥Á\x0006</p><p>F¦æ&[CýGûQ7öPo0ÚH¡N2)¼|&Ð S\x0007µãY7\x0016Qo0ÉIÒ\x000c\x001dÅG
#\x0004ívnL¢Þ`\x0013uÚâ@\x001b,S{Ñ{ç2óÃÔQÔ\x001b¬bBe\x000bC£©WkeÃônÔYÔ\x001bì"5	\x000buÈ{Å¬ðn[\x0003º»ðj\x0002º1z]L\x001e!\x0006g¹hNSK¨Pí;\x0018¤n\x000c£Þ`\x0019ik\x0003_F¯ø\x0001î¥5t·^SCc\x0019ae46äå³bc\x0002r¨w\x0010h,#l°Æsï»¦¶l\x0010s >[û;HÝ\x0006\x001b,#=~ðetÈ%Ô¸hE®Ï\x000cS7\x00116XF«¤p1ÐÒw¡VEñíxÔa
ÑkM]·Ã[#SûY\x0018hì"l°¦T5\x0007</p><p>ÏÅÂ8qÂÙÖAêÆ.Â\x0016»¨Iz[áDS¢>ÛÓ4HÝØEØ`\x0017uà±@ÉÅq*\x0002âÎÔÐ
C7v\x00116ØEÚ\x00169A)
\x0008²5E1g\x001b\x001c\x0007©\x001b»\x0008\x001bìbº¼dÇRò\x0012\x0012ïgÍ±±¸Á.Z';}Ös\x00121n;ù\x0004uc\x0017q]tæR \x000ffÑã¤Í©HlÌ"n0^æ$.Ôb\x0016½8N»¦\x0014°M n0Nñ"Kí»Ç\x0015hAæã%¡>ÛÕ3HÝØEÜ`\x0017-È1/Z\x0016õ22î(\x001eYÄ
f\x0011£tÎy\x000cR¢H[ $ï»£ÖÃÆ,â\x0016³\x0018å×'\x000b)¶\ÉKF<Sç7\x000cÝXEÜ\x0012-\x0006^Ýî¤L´¯B\x0018ü·\x001fuc\x0016qK¸èY¤Âry\x0018ðN¨wx\x0017Hbv4Bqç?|øóíÍÝûIi"l\x0006\x0005p¼â/Åâ^ÚÖ°\x001bkýðäûë«7ß=Ìgj>3ÊçQÒ¤4_&ÖÊ`\x0002×¯^YÍçj>7Êçdu\x0006ê 6<`Yº}Cw\x0000ðj¾Póóã\x0007{\x0005¼\x0012=\x001d\x000cÎq±k~×òU­ýúÐ±\x001e0ØR0C{Ty^¹F)wîÊµÐÞá+\x0002åñ	hs\x0001ÏÐ.Sí¾ò­&lî\x0008\x000c_\x0012ZäÊ4\x0013UÆ#¡Ü\x0012ïz5asK`ø\x0018Y¤!2À©L¥OÿÆfÂæÀðEq(¹2Ú{</p><p>re¤ïÏòZOØ4fJ)\x0008Y\x000fªAÂ\x0000\x0000+3e\Yf\x0004³÷±ZåÀ=Ð	NZÃTã$³ÜKï¶íVè?ÌiMYLË\x000f?Þ¼[S~¼¹xùßÿõ×»·?~øùîvÍ
2e8(Mm`ùD\x0019}lN7ÄÿðôêñRòôêâåõ\x000fo\x001e=}ò»7×\x000fs»Ûmâv´3ÁÉþ\x0017Æe±'w't ;C°Ì±\x00112\x0011'6]ßQI½µ3N</p><p>ëxêMteL6Nóà´M'õ\x0006\x0019XAX'ûmõÉI¡³àÐÃ&p_\x0016ð;ã\x0005ü¤\x0005oî¤Þt)©`LN\x001c¨x)Í7úä\x0010¥YðæRêM·Ò'}'àeÔ·+U©I£î)ãÍÝÔ.'mcáËéÃÁÛ-)pÙ\x0011\x001cË	.'ùÞ<ý4ý\x000eÈÜe\x000bÖÉEå³ØÍÕMWÓ«2ý;·\x0012A\x0001'à~@?\x0008ÞH8lð<+9\x0003	{öÚ¥Ö¨\x000fæ³àÃ\x0016	§Üºæô$Z¶9ù¡xz7pl$\x001c·HxP¾è\x0014\x0017dù\x0005
\x0011åañdNa\x0016¼qÜ"ãA¡àÑ¹KËÓMb~Úõ\x0005oÌ\x000fn1?)t/æÇY.àK'^¦ûÆ\x000bígÁË[.g\x0000]FAÓTh\x0016\x0015\x000b\x0005üdRu\x0012Ü42n6É8\x0004\x0019»¢\x0006§ìË6C<=x\x0016¼q³IÆ\x0011¹¦VEG*3ÙËnÓYÊYð6ìÙ$ãºXJ"(ã\x001f½\x0011Q1°\x000b8ª£Eé\x0007RÿôîÝÛ\x0017¯n~úëÍÿ|\x0010\x0019\x00145´±tçZ-\x001az_VÚÚ^ÊíéÇO®_¼ºzöÃÕÿõ0.Ô¸0n \x0019á\x001fÀ0ý\x0017Ê¦îÔQ\¬qq\x00127ÅdÀ[O°£á\x0006þì\x0015Áµ5®Åu%¤nRÆE1vâº\x001a×Í\x000b\x0013a\x0008ÜãÁ\x0005a±÷È?ëk\ÿÍ\x000bC¨qÃ$n</p><p>»ÍG²Ý¼W¼\x000eÆí¶ê\x000cÒêF1èYÍàmI($-ÔJ:sÑvËFyMÃkfyeÉl\x0004ÇË\x0012®\x001c®5½´ã(msÓôìUó±xo\x0008Üëpe\x0002ÚnÁÕ(o#»zVxTÖ'ÞÀ ¨[GÎ×u;p\x0007y«Á ê0\x0018d×@*\x0001:Ö
e|,õîÄÛáÙÛ\x0016AÖæD<;.ó'ó3¼ÍmÙÛFÏ$ÅÏC\x000ea+º¬[Â6JÛÜ6¼mFIê\x0012æ72ÔFè´[@?ÊÛÜ6¼m:EÓ(\x0017[)qc·Àg\x0017Û·íÐÁ²¤B#K¯âFu»#GyÛ·Mºägtï"\x001f¯ó×ÒÝ\x00021\ã\x001b§þvÚ\x0016\x0003k3
\x0016JÖB\x001aòS ´6SÕªì§¿Ô¿¶è_'¥¹T¹&ú7tËyÆß¶Äo¿uâæý2\x0007oò~9î²k~ýO®C\x0014E¬h\x0003»ìÝ¢ºñs~ßóûoýu+\x0019zV2g){|,8£¸ÝÉ:ã¼7-ïÍ·Í-/ÎòþºâkKüuZ\x001f\x001bÉ\x0004ÊûB:a¹tÝ\x001eõ#ÞÓÚé<Úò\x0001E^+WûÝ]<ºù²\x0014ý]ÝýøñfM½\x001f½\x0002çw\x001c\x001b©í]ðÙz\x0000e6{õ~o.\x001e]½ZÊþ®Þ<}~u¶âO¸]Íí¶pÓu»pSîÝ `¹	\x0019ÐvËr¦À}
î·+¤úæ\x0005<Z"Aq©3\x0018íw\x00055xÜ\x0004Î­K6ÆäæÙ½Ia°g\x0004\x0006v\x0015C¦ÀK\x000bõ?\x0003ys9õ¦Û©"U=,äZ^µ1h.2\x0007ý\x0007#ä\x0018³Ü¡d¹ÝÜ}þðîöâõ_>}¾ýûÃÌ ¤XÑx\x0000È\x000e)\x0004Í/</p><p>¦wÚÏ®Þ¼|òøúâõo^¼¼þÃÃ¸PãÂ$.\x0015¯´«1¿# *©ÓÕý	à£¸Xãâ,®å
¾ÔgÐþuYÌØ-õ\x001b55¬ÍÇÆ\x000få%D'µvÝñû£¬®fu³¬H²q=/éÂdFàv\x001câú\x001a×Oâ¢+¸ÔuZr?´m7é6\x001bjÜ0KN8\x0016¡*PÉ¹\x0019s\x0010u´ïnÞß|ùú¹O\x001bkÚ8y¸ÔD_\x000f|ÕE7\x0016ÚîÆÁÃ­6\x0002C	úR\x0008|Õ¬º\x000c¢\x0014¼ÈB÷ù`\x0014·5\x0010\x0016\x00025ò9åbà¡&É*Èò$\x0016{ñ6*WOê\\x001atÈ¸\x0014>e\x000ba¼ä_uw\x0014Á(m£sõ¤ÒMß]Þ\Ô\CU^é_ìd#ªÁùá08× =öÎØK=y\x001by¬×b÷ÁmÌ´\x00134\x000b&Sò\x0010j"wà¦H¯û\x0010:ÊÛØ	=i(~1ámÌ´\x0013\x0018Ê3³Å(×x±;IC¡Èòp3ld!]R¸Èí\x0017é²R¡ÞË\x000c-r$þÅÌ::ãÙ#\x0006\x0013(3í±\x001c7\x0019d&öÝ^¿ñ#~Û\x001eñÛoþß¶G<	üI¥ØÓN</p><p>-þ¤¨µ°Wd¡õ,2:_.^2\x001cÀ.JG:^&e%òÛôÁ¸ø\x0011}Aöz®~zûùÓ/·\x0017Ó_þ~óõA`\x001d¨äKÖ¼¡mõT²\x0016¬¸\x00119
|õìÑË\x0017O^]_<NùÃÕë¡Fydy\x001dÕ*x\x0013Ë6h\x0001°\x0017òÿOÝ»%Ûu\x001béº]Y\x001dð</p><p>dâ\x001e~¢¨e\x000e^T¼h\x0014K2Ís$ÒÅK½ª\x001bÕí÷Ý\x0003÷¤Zr\x0003ÀÔ\x001c\x00039\x0015rTM-JÖÇ\x001c@þ	 /¶G¶jäXÀØÊÉq³^L6È,C³ú3ìzd§FöIúFQB¼Ôâz¼X\x0005 Cö=²×[Y¦\x001bjÁF¦$06òZX1\x000f\x001c{à¨\x0006.Þ\x001bcPB\x0005W¶Ð\x000f!^½GN=rR#Cà¾KTß¡M\x001bÊ¹\x001aiÎ\x0013ç8ëlÈ­U#×Ê</p><p>©õ°z2M\x000b£?Ö;dW\x000e÷\x0015ÚÇJIE\x0012ö¸zU9Ï<8dP{dºSå&Èà]Ë{ÆÓØ{ØÖÁ#Þ%[Ë\x0015 KkPÄ\x0019£mþmµypÉ öÉ1zÙ|!È|ù8¸¸:c|\x001e9\x000cÈA\¢ nâtä\x001a¸&ÖÁ¬^eÏ3\x000f^\x0019Ôn9qeð¸ou{IÒø}Zm&ü3æµ»ÁÆ<¸ePûeêÃ;0gÎwÄàNf^\x001dÎ5oæÁ/Þ1£\x0016õà\x0004\å!ïþþ8ßÜr4kàiôF6·û»\x0018/#Ðr7êZr\x0018ó '¨×\x0013É\x001d+FisE°WÏ#óÄgF½g¦Ç¼ÑËÐèZ\x001cgÓa.\x0003È\x0013õ¡'HÅla\x0012ÉÅ¶ÿüz\x000f¼yæÁÍ¡>ú,K\x0018eÀúiiX/Ñ[íV:Ï<¸9Ô»¹\x0012^\x0000Ï
t\Ã.7\x0002ñÀ\x000e\x00077j7\x0017s¢²ªjæÄwÉ%8¹Þ¯N.f¶£³zGg\x0002¿\x000003´üÍàVóç\x0007?gÕ~\x001af"ÙA33H\x000e²÷«×[óÌCÜlÕqsHR\x000cH¹C\x000b²²\x0001[í\x0007;<^d¨ó/jæ!l¶ê°9Ä,mÑ\x001b~o@ßZv\x0004o\x000f;fÛAP¬ZPbr2\x0003\x001eÊÒH|<1ÒØÅûÕ×éyæ!Ö·êX?DiûSìÜî\x0012½o-.¶_Ð!\x000f\x001ahõ¡>eFr\x000cêF;òJsXm«4Ï<h Uk`0Ð\x0006ñBà;ft¾Í*Õ1}óÌ\x0008Z½\x0008R\x0019\x000bÇGÝ¥\x001f\x0017;¯vüfv\x0008:µ\x0008\x0006\x001aåÍê\x0005ÞI\x0017«\x0010VoÌ3\x000f*èô*Ø2jÿZiò#O«>Âaâ\x0006\x0015tj\x0015ôI\x001aÅ\x0005r\x001fËb>ªJõ\x000e\x0003\x001e4Ðé5Ðg\x001eÊBí¥·]Dssn¼ËW+ /²ÇhLpm\x000cå\x001c%&ËN<yP@§W@Ú¥bavrsD\x0001Ójì<ó N­B¢jfzæ©'*Îf«upóÈ\x0002:½\x0002Ú6³\x0002Rw`Üèç\x0003ó N­¾\x001cWE\x0001)·î@ãØÎiu.ð<ó N¯èåHµ\²gÆ(ÁþO~P@¯V@V\x0002:WNâ6¼õW§¹Ï3\x000f</p><p>èõ</p><p>hÚ\x000c\x0005\x0004Ã9³tv\x001e½pÜ\x001eô\x0002zµ\x0002º\x000cráìäv¢5U;Ys«ó\x0008z½\x0008\x001a÷a\x0004/³¢}k°^É7Ï<È WË +W¾¥+'7\x0012G\x000br±\x000e|óñ¤xµ¤ÐÚài{ÄÌ'\x0014\x000bT]Û¦xµ¦P\x0012¢\\x001fS¬
º·åàqï~Ð\x0014¯Ö\x0014\x0017£\x0004]9¼¦ª¥D$¹Õ¹yæAS¼ZS\x00025Ðvàæ&ªÞÚvâ>n=Á?\x0007µ\x000e\x001eIH*s¢ö¹u\x0008ÇÝkÁÕ\x0005µ«\x000b.IWÿ\x0000òêã\x0011[×üãÎÛa\x0008:x\x000eÎ¢ùÖ×ÕìAÒÙÃ\x0001\x0018¼FÐ{òÛ\x00158KçßjTÃz:å<ð°ý~û¡¢4­ûÔ¹$M[\x000e´q\x001cv_Ôï>kÛ\x000b&%\x0013ðZ÷\x0010»qÃîúÝ\x0007A\x0006\x0012c9 Ô9<è¢\x0003C:.å(\x000eÛ/ê·\x001f¿_\x0016ùàÉR\x0005ØËxÇD4ýÞ£T#(à¸ó¹+¤¼Z¹5<ì¾¨Þ}¾\x0004s,$Ö,Ó"\x0017f'iùÑ¬\x0016DM3§aû%õöó¹JbX°ä®h\x000bÒ°ÿzÿù\x0004!L×Í|¥ØÝÐÁÌÃþKêýçdÒô	îÑîZî*éßaÈÃ\x000eLê\x001dèËÁ\x000fe9vÖ<\x000b¼,Õd÷yæa\x000b&ý\x0016ôAÆáøvÔ¶YB¹è.öðW!ça\x0007fý\x000e,d<\x0001ª¦øRß&iµ\x001dýjóyæa\x0007fý\x000e,K#±KldeiÈÊ\x0008Ç=_æa\x0003fý\x0006,q\x0006_Ð%#/e×	r<îV?\x000f\x001b0ë7 f9´Òå­lÀV\x001b~äåm\x001eSÕ\x001bÐ¥À½©J\x00169UÊ»ärà°R\x00088+81ê-X~£ÝÂP/ÉÀÐ¾A\x001fWrâÌw\x001f_¿?{\x000f¤èµï÷­4K.R\x0008\x0012r\x001c}äú¦[òÀ&]·4Ç2Û¨>\x0000YIÃu^2´c8N\x0011ÍÏÑÍ\x0015èÁ§6\x0013ºüò\x001d´n\x000cù¸#K­ß8êk;¤äeclÚ\x0008í:	{¢HñÜà%\x000c¹b­xé¸\x0018Ómn«üòP\x0007åÝÁ9z¸\x0006=X#\x000fC4ºM6h2\.®vÕQ$õ·AIëÿ^"ý^\x0000B»K\x000fYg}\mÂ®Yãß­q-¶¯µ5\x000eQ.\x0013¨¼×¸YmÝ¦¨jûS¹bü%[Á±dÞÿ\x000b$ßÁÏv&\³3Ïj*d4j_Sqè§­t?¤|+Ë®\ºñÒ2·Í\x001fX)4*Pq*Z\x0005¢Tiä\x0007g\x001aTÆ¹ÒA®}v­ñâT~8s*?¨£C+s]ñæµ+\x000f¢\x000cÚï¿/6+<]42yõ¦$¹äMi1H«³¸ÚÌb¸(åY$[R\x001fÉ\x00128wºoçKÊÜò\x0018;õüÃÙzÖ.\x000c_g$ÂËÈ&© \x000ef÷b^\x0019Íx>TÅª|sÿéÇÇ÷oÿôú?ß¼ý,)RN</p><p>§ \x0012l[î\x001eã¥²É¥\x0003ë\x0008ö\x0007¯\x001eß<~ðô«»o\x001f=]Ýv
\x0016{XTÁº\x00002©Õäâ1jK´àlk\x0000°êÝ&am\x000fk-°\x0013Vè\x0002[Ö¥Vf³ú\x0018>	ëzX§³,úNÚ¡y,ëqµ¥ÿ$«ïY½Î°¾eú\x0000
o\x0005î[á%Ùnõ¾f5ô¬AgWÊþâüKçùr©8Kììêð9ØÔÃ&%lëü&HÏ\x0000­óC^}$Í=lÖ­hP¶4::í®¼:Vzµ#kº!ç\x0005#1<5¨L\x001bm+î_('iGIÐi³­Õ\x0003Æ¥´×<ÈSÇCh\x00077\x000b:?ëâé</p><p> ¶~©!J9VÇ½LÒ\x000e¾\x000btÎË,Ï\x0010!ey!H\x000b\x0008ù\x0018Q85?[`£\x000e6¥6\x0019¦g²CH-ÿ%­Ö\x0010ÏÑaÙ\x0006e(\x0002ßã\x001cÛÚS"«=Uf½×0#}ñ`mFºBvù\x000ej\x0003ËnlEÚ«Å³ZvÎ\x001cÔÌå4$	\x001be¬]Ô:;¬^rÎzS÷3ö\x000f÷:#/i}5\x0003;b(Âëu&Ó\x000bãtìá!§YfZîmSukÕû\x0018ÖnO&áÔ¶¿">þª÷\x001e­	Ý°	$4^\x0018</p><p>¯ôÌtá Ç6Î#qÃ<éÃôù\x00048Ír_M\x001c·Oþ\x001c×kq©\x0013%W¿*¬Ä¢õÐ	\èæÓ°ø^\x0017ðAK\x0008Án8HKÒõÚ¹=¬%\x001e\x000fëå\x0007rX¯s[¿|÷·×oß~~f+\x001aßFXG\x001a\x000bÅ\x0013EL¤)^#­\x0013[¿|ö»§O7Æµ</p><p>,ö°¨¥!Ûµ/m*GJ+3\x0019ùÖ\x0006×«U'YmÏj
·6p÷F/\x001dËÀJ÷Æs\x0015°®u:Xj[Yþ¢LÁ¬\x0010ÄÕV\x0018¬¾gõjV\x0019fP\x0016o\x0012Xi\x0004WKi'YCÏ\x001a4¬³T=\x0015ÿj%E6§Äq\x0002ºì\x001a{Ö¨³+Ö¤ºÚÅ®(½rÌúQ}\x00126õ°IgØ²L=Û5ñ\x001cÌms¡_Í¡c=\x001dÕ\x0017\x0017k® sBÙ^³ÑËã$âjwªIÚÁÇÒÉþb´ã\x0002¥çúÅh\x0007w\x0000*ð\x000bÒ\x000e{\x000cT\x000c³Ö \x0017%\x0012`õ\x0002w\x0015uÊu(ó\x0003Ý6\x0003{/Ií/ÿèA®\x0016N#\x0017kØõn%\x0018~ç3!GºÕ¯qW\x000b\x000fÖ;ÎJC¬ò 'ÈéõàeÎi c:3S§ºÊlW\x0013^§»3Ce3b
Ë`Úó v¶«Ç²Ùøö\x0019ÕÌ!\x0012'\x0013¥¶I±E
«%Ókùã¸?êÖ²kó Ê
¤	±!VßÐ¦y¿\x001fy¿×ð\x0002$NÜ1Ô\x0000ý\x001a4'¼zA6ÒnÍÒù¶KêmÛd\x0010\x0002íÆ\x0017Âjbü\x001e\\x001bÎÇnÌXùG~¼yxÿÃw\x001cy!\x0008·ö~OTYs´\x0005Á¼1OèùÃ»Ç7\x000f\x001f<üzëþCP±GE\x001dªCñ¾©èpÍYÈÐæaC>Õö¬VÅ"ÈX):CHzÊ\x0008t«\x0007IX×Ã:¥aåzß¤ÌfÅÀ¾ÖÚõy\x0005S ¾\x0007õ:«fyë+>Ëµ\x0014¸·\x0002ë\x001d&ac\x000f\x001bu°6Ñø\x0005F\x0004î\x0015+\x0017\x001f°Þb\x00126÷°Y	ë9aÙÄvÄØ¶å\x0019s3¬Ý®ÐÏé¥ÔS\x0003í )í_Tj ßÙ6E;:X-b \x0006­,öèÛ\ÄtÐ2ÁmÒoQ² ï°òK.Ò £üþA\x001dÜ\x0016èüV2æ#\x000ctoW3K¥;ÍÏv\x0008ìàº@é»Z_bYCµQ\x000b­kñV\=MÒ\x000e¾\x000bÎ\x000b2¿-û\;I§\x000f\x001d|\x0017(\x00175_æ`4\x0017¤\x0017ÿv\x001d~ÌBÀÁ\x001f Ò\x001fá\x0016âå\x0010Ù</p><p>=#ævB_-k¤\x001d\x001c\x0002ê\x001cB,ç\Ï'±Ø&\x000e´.?\x001b§ÇIØa¡nÅ\x0014%¡v.\Z\x0016²ÜÂú)avØc¨Ûc4xV\x0008.JauH2\x001a\x0001`cFÛ\x0014m\x001ahr!Ú½¬ZÃ¯ýe!ÈË.õü9\x0006vð\x0008¨ó\x00081¢<7P÷$-%%ÏÊ¬¿7ÌÑÚ!±Êx¦¨\x0017òuGZ~YmÛF!ºÕWóIÚÁYÿ¢f^\x0008EÇ¤+j¢\x0008V3\x0012&a#£Õ\x0019cò|¼
åDf¸±\x001a5³`÷\x0005Çè\x001dÏJ_KU|½Héa\ýàÛª=(R´CðeuÁ\x0017y//\x0017\x001c#ä>\x0006pµÓå$ì \x000cV)\x000c>ÊYfK\x001aéË)ñ9</p><p>6\x000c°Aé¼B\x000b\x0010|>H!I*>Àê°úIÚA\x0017¬R\x0017«å	Á\x001b	¾B|\x0014Xm\x00119\x0007ë\x0006Oë6$Îl.k[\x001bÜ O»°>rfvp^Né¼§\x0005yÜõ9A®¶©ØjFë$íx¤t\x0008Ôa5\x00174¥)Z\x000cÇì17ì1§ÜcÞÊM\x0012õj.´§ÕbÊIÚa9å\x001e+á¡\x0017am!Xi'eV¯êç`ý°Ç¼r9Ç\x001bOd\x001c{Ùö¨\x0017V»LÒ\x000e{Ì+÷XÙXiËéÁJ[yÒ#½8\x0001¸V·\x0012r\x000bä\x000eÜn@Û¥"F¿/FXñÅ¸6åQ\x001btqxÆÄ)J)eÝ¥\x000b\x000ceÜ\x001ds\x0005</p><p>ý;^}
w¼Ydê£RO¼\x0019ô[ÍQ_¬[­k=uó{ë¹ì{í-\x0018O\x001c¦Gé$×`Mº
5öÜÈVkäY§õÙÉJQxs:®ÖìÌî¹nn6ïº{õ¶³mÛ¹ïºc"2zÛ==@Öu,\x000f¿âu|¶U6¦{±Ä·xà)eïÅÚ\x0005éA\x000fQöÜÆVkãT"uÏ\x0000ÑF
ä!b5cx'3Ø³'ò\x0003yâùã§ßÝ*ÿgA®s\x001d­_s	 ê[~ÌèpµTòËW7¿{ðêá³Ï3.GQ.Gg i
,Ñ#'ß:p,ÅH\x000f}×SúÒÏS\x0006_G£\x0015J0'y\x0008n5ºÙ\x0003\x0019ìY\x0016+yößþöá_ÿôæ-ç |õîÓÇ×?þ¸#á\x00121JÕiùóõG\x0011eJèÜÅ</p><p>ô_ß=yô3\x0011¾zöêåÝãÇ\x001by\x001eæ<\x001bÁÔlo~¼ÿ¡öþë¿\x001f¼ÿéõÏR<\x001c\x00077Ô3s&ÚtÍ\x0012B^Z¦ß<~ð°X÷æÁó'w/>=&ª0£¼PTc­`D5æ\x0000LÛcZ
¦\x0005É¶-»)±1[\x000bZL\x0017\x000f
¾§ô*JÛÒ¦</p><p>f
\x0011)¨yñD>\x0019{Ì¨úæ ·])\x0007ngHý÷ä_ºGÈË©<B{Â¬!DÏ\x0013HM^ÞEëç6\x0012jÛ
°æì\x0008ã\x0016Wíñ6Âºlx3%\x0017;ÖOb\x000e{\x0007T§\x001cb­`\x001aný³g\x0004óâmÆ$ç°{@µ}\{ñJ4\x0016®æÿ£\x0002¶«IÎaûjÿ\x0014mç7J</p><p>Â))\x001bLb\x000e{\x0008TÈ\x0007)¬*~GÊ)ÊÞj\x0017ß\x000bæ8qØE¨ÚEô^X1]àÉ½Å"\x0014ï]9¬NT­Î\x0012\x001fK¢N@ÉïF'WAx¹E÷$ç°:Qµ:#ò¨±"BAv;Z9Bc>Àyâ°<Qµ<3Ô0¾{lË3HFL\x0017ß·ç8í°<­fy¢­äÏûÛim;.\x001f\x0011zØá³[Íg§>Ûæt\x000bÁÕ~%<²tñX4É9|v«ùìåtFyûõ³g¾£¤Ë³\x0016Ê]ÌÊãtÃgwªÏNóåO$ÕZ}WÈ×v7h»Si{¼%57Q\x001b@!]:´Ob\x000eÎÓ©'	\x0010¯Î²\x0000"s¢$\x000eb¼8¬jsØENå<©[}n\x000fu${è8¥Ë\x001dÕ'9]äTÎ\x0013<yLÙE|\x001eòâ4×õs«·æLYþê×ùÙÑZä5ö´åÀRØyºöÙóÅzÙÏ~º[ä\x000f¯;\x001aYñóOëÒ\x0011ÓÅ&FÓßq~¯>
µ«+Ô³E±õ\x0008+ôz\x0015Oõ</p><p>~ðë¼\x0005qñÖE%îè¥\ü¹º\x001e\x0017à\x001c\x0017@\x001bä¼ÑÞf>¶j2ë/¦UìÅÍxvcWÎá§\x000bÛ/Þ½]nÂÿü¿þ1RWÛ\x0000¥²$85a\x001d¬V\x0010}ùêægOð¯·®\x0017\x0019\x0016{XTÂffq	c+s°Y`ãêÐÊIZÛÓZ%­$¯Ar¦¥\x0005Z#°iu¼Ø$¬ëa\x00166È¸æ\x0014
5-ª´\x0017èÐ¬&NÒúÖ+ic1htÍÍ´]Q·hCO\x001b´¶mSÝÉ×ú2L»:k\x00126ö°QkZ>\x0005@¦ðK\x0007;Û9\x000c«¹v°©MZË\x001a\x0019F©'\x0005?#?ç8të
_æhsOµ¦En\x001aé¼Ê
²fÓê(9ÖSÖ¢\x000bF\x000bøÔ</p><p>ê¹³l1Y\x0008ëõÅs´£ieÒkoé\x001cN\x000eÐ\x001cÂj«ËIÚA\x0018@«\x000c!S×ãF1,÷¢9g«ÕÐs´2V\x001aB ÷§BÆFIhÀÓØÊ\x0016[Í÷Ä\x001d¤\x0001Ú@õÚuº<\x001aê8^½­<T©à®NÄ\x001d´\x0001´âPç».¸ÞQJ­\x001eàÛ!gãjõÓ$î \x000e `¨\x000fúëÌÒ\x0006\x00057¬\x0018Nâ\x000eú\x0000ZðâÅÐÄÔÂ\x001a©Íp6o½÷OàâàtQët½Â!\x0018ÓJcù°ë\x000eÆqpº¨uº¹5z¡-á8ç»(¸x¢áxxÐ\x001e|æùHå¨î%ù2Ê\x0001Ý¹°Þ\g\x000ew\x0010	Ô\x0004HM7\x0002\x001dv8!ÛÉNsTÎy\x0008î°ÓP»ÓPîçã=8n2ì¨z\x0017îú%]ÅuJ8­JÐ\\x001bv»\x0019$íú²uÍA\x0011\x001bÜ®ÓºÝ_è,é8×i\x0003Ý_êäÛµ­w ÷JQk=Y\x0013Øv0ÜîÒÃ\x000e:FtÍt*ð÷:`\x0003íDYt"³ç\x0005Íæ.>h|Ãhá\x001dªq\x000f1µ5ÁQYq\x000f¡¹caHsæ(½5R¾õXçZÙ¬Ä¸: söÂéú</p><p>hJÖp|K­j'\x0011;X­O\x001fWZöç·¹ßvJq|þé§×?îxm\x0004Ã\x000b¢ü</p><p>å\x001emÅ\x0001_<\x0004\x001b¿zr÷xÝ°\x0002êzP§\x0001
JÑkÄ\x001b¥{¾ÍYNkþb£ôiPßz\x0005¨µR\x000e¹Ä7¡Þ»Ô®.\x000e'æ=gTpBYõ=§Ø\x0016è\x001e¯fép®óþbØ¸\x001bÔ\x001d(]¶S\x0010F·Äùíû7zûú7O^ú°£\x0015\x0018y.Nk\x000eÀ\x0012éØ\x00108c8»iÍwK°ß>ôÕÓ»'w¯^l¸\x0001aö=³×3;¬kÖ¹>ÎfÞ[\x0008p9\x0016Ó1Ç9ê_N=å;ËÃ~ö\.Ô|ë0æÜ3ç«ÖÆòzRìlT\x00083·U@zý9\x0008Ú\x0017êaqÐ_ë¹\x0014\x0014Pm5c(©úùr+_åî¥­®ëEÚ~ÅÛÑ\x001a;¾°\x001fÈ\x000bÛãO?¼yýöæÅ·úñÍ±wEÝxctK­\x0017É±<Ëqã ñøÕÃGwOo^<zúÕãGë\x0013\x0011\x001b-ö´¨£õA2gaésÄS¥ó£^M\x0007áÚ\x001e×*qË®³q\x001dÏº¢¹\x0010bÜ´:\x000bq\x0016×õ¸N£é+Ç!</p><p>-\x0017ë\x0006\x001f\x0005w58Åõ=®W.Ý\x0012ïð\èx8\x0017z+k\x0001ÖGÖÎÒ6(i-pºêR\x0016Ì
y¼dÿ\x0006G-ÝØãF%nÌòv\x0015ù¶Ä'ÓL»:ut5õ¬IË</p><p>ò`A¡Eä\x0010R3íê5ê,nîq³\x000e7¢¥Ë\x00057$i-\x0017<\x0001\x0000¬¶ÕÄí\x001a"B\x0018¥y³«µ>Åº^ÊiC»¤6yõúa\x0016w\x0008PjD¤g\x00151oÕ''Ìõ¦!³¼Ó\x0005¥×%£òÐð\x0018
ç:a8á®\x000ekvcCõâÊä\x0014?¿å\x000c'/-\x0019w\§ìrfî\x001cÚé¡á\x0014ëX\x0001ÐNZ{ÒþZ}Ãó9<xÃóøÓû\x001fvÌõE,ÇãÌC'!scwÌ%=Ë£[»ÖyüêùÃéÔ
\x000f{<Ä\x000bVîÊ¦Uº(5uÞmèØ>:ÛÓÙI:c¸È\x0006ÐQ®HM\x0013çÚ°ô¸</p><p>ÎõpnÖtkPé¢¤5ÚÚ Ö¥ 3x¾Çó³\x000bÏ0\x0001\x0015ø;^xÒÀÈ¯ßîÅ\x000b=^µ\x001e4¼ü(bm´E\x001f6\x0002¾}x±Ç³Ök\x001f×\x0016\x0008\x0017¥Ñ^ýuÜz¼4\x00072Q±Õ£X	îËÇ]}öØ{¼<WT;ó¾ ¬mëv@#</p><p>¯Ã;\x0005CØ
îY|5³\x0000ÐX\x0007mô*õyu:Ç^¾Q3fE\x0003â-Ï§ÅÐ¶®\x0014è\x0006\>¹n\x000cÖ\x000c\x0010ÍÀh¥î¶\x0004ó\x0005¼ÖzhÀ¬jxié	ôKcRö\x000cçs«y{ù\x0006ÝYáH^\x000eEË8\x0006·ÎH7×\x0012-^k¿A8`Z9@V\x001fõzçÍÑÊ_\x0002n\x001c\x0011öá
Â\x0001³Ê´ª@D9iNÍêHÃ½|rÀ´t\x0004®vEä¢øæ6\x000bûZß\x000ctÀ¤vXÀ6A\x0002~»dÂwmX\x0005vÀ¬x\x0004ÓÄ#uîE:px±dy\x000f\x0007ñÀIñ(G\x000fîHµ\x0004¥\x000eÙ~Òª,ÿ»oè§Ý3ÊÃZÇo²Å~R«\x001a¯]~8xgõÎÁzXð2ÔÆ6[Ù¬\x0016Vìå\x001b¼3ÎzgRÔ±^9kì"ýÑ­öÖÝË7xgõÎ(\x001d\x001eÁz	¬d4\x0000ÍÒ¾\x0012nðÍ8ëí)löÛ\U(\x0015³ñrû\x0019¾Á÷álÜ;{âÈe=ÿu\x001f\x001dø1°ò³[×dNÐ-®Å¶ºè,
ÿk¹ö²`Hþ¨GòÓ
ÌNJç\x001a%´IãÖI¿8:2]{ð=§ôóeýñ>\x0001JÀã«
ï@b|s¥-ÁSsÈ4fðÜÕ\x0008¨x_¢-\x0019w\x001bpã
l§ØS¢2BiRæA·Ö¦öÉãÕ\x000bÓ÷½öê'^{û\x0017f Ìàzn§»6)4]Ï\x0017ß}¥pnË¨Ú=6¶³'÷²NäY{´39|GÝ¤»àòD\x001fÞÿôfGÏ:ðÑI\x001f\x001c\x0012gF k3¸Yuà\x000f\x001f<y´Õ±®èæxJB</p><p>}RÏOzû·=§cÇ[fIçJlAk%[Ù\¼ù=%õ¼xõÕÓ?|\x001eÔ÷ ^\x0001J÷nK\x0003@ª\x0008ðÎÙp\x0016¸M\x0017\x000f¢»AíòÉûÔòÉ9ñßÜ¿ùëç?:¤¥Ìy¹J§ö\x000b'¤,	Ôêf-oéü÷ÍGÿþyLì1Qùõ½|ÿÚÈ\x0008²áÉ=qu>Ã\x000c£í\x0019­Q\x000e\x0007Ô8Ü&ÆleÃ+©E®ÇtóH\x0019¦L)]Â!\x0003w gªí!ëû(}Oéu\x001fÓÊVªy\x0011Änõ¤?\x0019{Ì¨À()è6òyFPJt^\x001dÎ3CzÊ¤ ô®Õ1\x0017LÃß<»$YÑ«#\x0002f0s5Æôr³\x001cP\x0007ó\x0005ÓJ]\x0012\x0019özÌî-\¦QpfÏ]"ñõ\x0016\x0000\x0007×¾ú\x0011£kWøv:ÎZIG\x000e7ÊF¬%¸ÜXmsð p´<\x0003cÚnuC1\x0007\x0004\x001a¬<¿\x0012UÏn;Î\x00036;\x000c.	\x0014>®VBÃä´	\x0013%?ªÂ¯À,Îâ,+±M[\x001fnÜÍ7ïÞ¼/T;ú8êÍY\x0016x\x0018
2Ù½\x0004òëuõw/è_õìÑóò[\x001bML\x0004\x0017{\Tâ\x0016ß\x0019BÅ­	×óA\x0008-\ì\¦¡µ=­ÕÑZgÅ¸©¬\x0008N\x001a.'§°³Ñz82ëz\§Ä-\x0007u6î2\x000b¹ÞxÃ(ÔoÝ\x000bÌáú\x001e×ëp±,]WS²if§kÈQ®Xw½°o\x00127ô¸A»Óð\x0013±!JÍ\x0000i1¬Î¥M=múÕ®\x0005â\x0018\x0000\x001ft\x0001à\x0017ïÞ||¿§Ñ;õ1IÈ>\x0001øBÌ\x0019*ZÂzùìÝÍ\x0017Ï\x001e½|¾up\x0016ÌÔc&\x0005fú0P0câ¢dg$#\x0004-ýïê1\x0001Î²¥Ê\x000fÆÓèÃüß¯o~ÿéíôKÛÒÚ4.§¥+ÛR\x000fdÈÕtë*a\x000f½¼»ùýWO7ïÙöÌö_Ù÷Ì^Ï\x001c\x001dW'¡<ºzãCÙ¯wáf=sü×°óÐ©­®éV.©@§r¹\x001a\x0015ï(]"ô9v«o?\x0003¿\4ÙVô9µ½º\x001c¿±¦
\x001bD9í$¹Kw\x0017\x001bbNPÛ\x0004g9¸	NMdr<yýáÃnxP~ç¬õ^\x0006cZcåÇ¯Þ_j<¹{ñb«\x001d\x001es¦Øs¦¨à\x000c2f\x0012,Í\x0015«YîÝ;ÞE'0tÛzZ\x0005¿\x0016Z\x0008þL8\x0013êN\x0013_¿~ÿÓ{z!z8¯«ø,Oó1:ñ\x000bf5[@¿¾{þäÑË=¨Ø£¢</p><p>®/Ú­´¹§.1Ü¶1®¦/Ï¡Ú\x001eÕêPyÚNA¥é¨je«]´Cu=ªS¡"pRx±j¦÷¿\x0005\x0015%·Å¦Û£\x0019Tß£z\x0015*\x0015¥ó\x0002(ñc¬YjQâ[»>Áh</p><p>4ô AgS+³©\x00188¶ihB4G Æ\x001e5ªP
È±1­pràÇT\x001b7±3¤©'M:RËÓ8 üÈ\x0000£Û;\x001b®·NBÍ=jÖ¡f¾J2TGØÖ©L²ë\x001däfHOW²û7º=x@	®²\ÎDy0(2µñú2Ã:JN«è¥ãntÒ\x000c½°VY{ÈbA«@/V¹­VÎçNÒÍËj=Ä­Â V S«Ò¯Æ´ÇL¤Ja]ï£2Å:¨\x0015èäªÄ+Vü6\x001a%^\x0011Ö{]¨æüHnL×½ùáë÷?ì\x0019\x000e\x0017Â©Ú\x0000$£\x0015}ûü\x001e×¯bÊ_Ü=¸5\x0014N ±ÄyÈ\x001cn¹$FI\ðITÊ§Mæ'\x0019mÏh¥t=¤S@F1$\x001aÞ?Ñ!íÅ\x001e4¡g\x000có\x001eyÈ\x001aS\x001cH¼yÞ\x001cñ±bÅjË®OÒ~T\x001eÀT\x000eáÐZb+5ÙI&öÎ9*ªPËÆáÔ$jækñjqR2ç×o'fÌÚ%zU³J¢×¯n+Á¹]Ac×häZë\x0006Ò^Ñ·%p±YÒHºrÙcÂ¹\x000f½ÿñÝÃ}¤Ý\x001aÞ\x0017\x001c!ìmòöåA÷øÙ¦þs\x0014z´ÚäÉe\x001f}iîZke4©Ý£º\x000f0ôaÖÔ\x0005\x0001­Ë±\x0010Û\x0001)lõ¯Þ\x0007zÀ4\x000b$­Ød9F\x0018M£¦\x000f[îr\x000f`\x0017½Ð7\x0002ßIhN&tÜ$¨l\x0010ô²\x0006×»ö\x0002â\x0000æÓñ!Ø¦^&VÙl6z</p><p>î#\x001cv	Ìn@ãýøæ#rê8]2´ÄÍCVf\x0000í\x0000h§÷q\x0014Ç«ÐÈè<lu\x001fv«÷ôÂ·å\x0003m\x0003\³t­\x0019Qñ229
S\x001b(ìWk\x001a?k>Ýy¦ë¼ôw~|óöõÔaWôY&Ód'÷¡õ\x0012 ~ëO½züèéÝV\x0006\x0006µ=¨Õð,ÈY¸EÇ9\x001dN¾5º@b?¨ïA½\x0006çØ¦-µ	¶
4Ù°nuÞÏ\x0019zÎ áÄÜnË\x0001¼~øâ\x001fÅÛ­¦±û9sÏUk\x000b\x0014¶ûW¥À~y\x0000h¾çzµùòpË\x001f¾,V¾}õ¹M\x001bî|?ç¸åU{¾D?-¸Ò»ÔG-üV÷Ýý 8¢\x0006È³{wsËÁÙ\x0016\x0005m\x001ctö\x000eÎ	4ÞÉfÏ¯YÅ¤I6½wòUÁ!6u\x0003©S¢LøËÖss©BÚÜßjÒ¿tð£ r¤àÚ\x001b\x0011ú\x0016\x00171´ ý¯?xRP¹RHü\x0000¿\x0008=÷þô1É:]oy3E\x001a\x0007Ò¨ùúÉ·YÃôKÎ²¦M\x0016_Í!M\x0003iR&\x00192\x001d\x0013\x0017=\x0014P/\x001fß¬6\x0002\x001dä	4úD[ß	iæ\x001b²¡¤õÝ</p><p>wâ O¨'NÐ%ÔCîËäc\x001b¸ÕÕ~?çàõQåõéq\x0007\x000eçÜ|i\x0012WºÞ&g</p><p>tpú¨</p><p>I]lóÚs²;*&\x0012ÒõLØ©m?¤\Ô­ß]\x0019Í-U©F<-Õõ*ÛÀþüTâ»S	ÀÍÓwÿùú§ïß¿¾\}Ä6p	ÇéuiÈ\x0001{åß°\x0000Óàu`ú÷=ûöîÉ\x0017Ïïê¿ï³àØã5à´×\x001c\x0003ÅÙ\x000b8HÃ	4[7Þóà¶\x0007·ÿB\x0016w=¸û\x0017²¸ïÁý¿ÅC\x000f\x001eþ,zðô/\x0000\x000ep6è¶üà,{ùÝ§Þ¿þqÇ?z\x001ao^ë.BMø\Ô&p_ED³~\x0001Â\x0019¯^¾z~÷xó\x0002ÎÆÝ\x00122þºñ¬\x0006ÆÈ@\x001b)^ ÿç¿þûîO?¾ÙÓÝÐÔ*I¡\x000brâ4hZ\x0006ÕÅFA<ù¸0ßÜ}õøÑVov¬«Ùú\x0019ÇÎ])øÇïÞþéSùïçïÞìI¥¤\\x000fÃmK\x0001¸:°¦VÇ¼Y¼þâæñ³§_½*ÿýüÙ£­·fwÐ³;ø`÷æ,6)?\x00187ã·oÊ¢¾¹ÿô×oË|~­\x0000Ê¤FKàÏP4ºen.îo\x001fu]~ãßo¾-ÿñyòØÇ«ÈÍéêÏ\x0005¹\x0003\x0000/\x0019ã6n\x0017FNÎ.Dæ\x001at-7â[^uj\x001bà)mt\x0006|eFP:»[/?òòõû÷\x000b÷Ë´\x0016%à¢è\x0012p\x001bç¥ï]^\x001dôüòîùóùeùÑº\x00056ö°Q\x0007K¸ÒÝÆðc</p><p>\x0015ð´î6«wÂ\x0015véê[ÉW÷~üéÝÛ\x001d]©VE±£\x000cBé\x0007åW\x001f,¾zðêñgO_®½úøó\x0012ß</p><p>JöÓÙ(µ¶ÂK'¯\x0010ÒjÕqã[\x000f|<»µðñtk±|ë'÷ïïßüðçü÷;²\x0008\x0006
Ô\x0013,µ\x0016_n fÉÂF»KûÉç\x000f\x001e\x0015_ü¼{(¿`æï£\x0002Úh¾/¨«"ýåo\x001fßßüÛ§×üÅ§ü}\x00070¥5ó	\x0016\x000b;\x0017!g\x0007\p\x0018/7Ê+¨ÿöê®b¿xu·FK[)õ2Q0v!§õîo¯?~$\ËÏ\x0006î·#ûÍOïóüõÇ\x0002üö5\x0011\x001b\x000f`ªÃB¤èT-}ë\äêÞrO?JéÅ«ç7Ïïh\x0013=½ëz¶çzö»/×â\x000eÜöàö</p><p>p\x000c%F,à!-Ï\x001bê:&n®áºÛ\x001bÜºüäê;÷0\x0017[b!XþªÎÐpeIÕ´	K©]þ2t¿¦©ÆóóÀØ\x0003£\x0016ØrgÀ\x0002\x000c\êåÚ-»t8</p><p>ØöÀV\x000b\x001c°^uùªf¹æ Àüæ~\x0000°ë\x00128f¬yÆdas[·\x001fõH\x0013Þp}Ïëµ¼.Ñã6ñFº®\x000b\x000b0\x0006\x000cl¸2æ\x0000àÐ\x0003\x0007-ð2\x0002¾.Tg«\x0014\x0003sÍ	\x0019Ø\x001f¶ bÏ\x001bµ¼õQ\x0011êeÇ\x0006ÆÚ\x000cl\x000e3pî³\x00128$[_ì</p><p>p9g`õ\x00114Æ¤\x0002ûlZÂ085Ðz5e\x0015Ä
\x001bqÃ4ÜLL¼"yóÀ\x0000µ0² Rm¹Ph\x0017Øp\x0014mWAÛÜðXA;µïÌ­ø\[\x001aÓ¾\x000b Ønp\x0015vUÐWQ>ýÓ_îßü°O9¢¯óË©È§\x0014\x0017å°^±÷+\x0001\x0014'<¿{òÍç/×\x000eù\x001d0öÀ¨\x0005\x000e\x0006ô-ÀâX¥Ã¡cm^&\x001d\x0004ìz`§\x0004ÎEß¬\x0000\x001bqÅ.Y\x0010àÃ\x000c{Þ¬å-ëî \x0015jJW9Ü(¼>nJÇ\x00040\x000c+\x0002KÂ\x001b\x001a\x001d\x0015\x001aqª.8ß7=ñ\x000cp\x0018\x0012\x0018\x001cW/v`M\x0013/+\x0002jòT!ÛÎm\x001f±9÷\x0012KEÐWïïßþñ¦`ït\x000fùÃ4\x0013k®¤#÷`%À\x0015Ó~õüÁÓ/o</p><p>îç	±'ÄiBËé¸"Òa\x00138ô
\x0012éx~¨¹\x0006Ñöv\x001a±\x0004»\x0001\x0015\x0013#\x0006\x0015WÎ?\x0013®Gt³%X©\x001dc(\x001eµô· ÆfE<À¡G\x000cÓØìÈÆå:.\x0010aEZ'\x0010c\x0018§\x0011\x0003Ôw</p><p>BD\x0011ÓEBåXs5aî	ó$¡`nùè+ÛÅñX#ÙrkÈ+\x0008aØÏ0½¡säç©Âöm\x0018DPè¯v90l\x0016Ý-4%¹^1ÔB\x0015ÚÏ-Æ5`\x001cv\x000bÌn"æ	UÆ,Û%¸$NÇ«·\x000b'	cú52â(/³ËÑá§0Ú2X{bÐM!</p><p>£[;N0\x000eë\x0011§×#TãUÆP;+\x0016Æä°Dc\x0019®e\x001cÖ#N¯Gð¾æ¹ÑT$ T²Åõ \x0015×ã®ß38¬G^\x0010<õiª(vL¶ù\x001e®þÖÖ\x000c±fL®\x0010c¨Ó\x000e</p><p>cóOðpµ\x001dí°gìôYFÁññ±¯\x0014¥6éÄx½\x001d=c§÷\x000cuç\x0007Þ3Þ×\x0011\x0002ÑµºË+1ø\x0004ã°gìôù'3ö%¥õ\x0007gOïïö^{xz²2Õ\x0007rc\x001eS÷\x0014»}h¬\x0012»÷à</p><p>Éï¾ïÓo¿×2Cí V©/>{ö$o@^æ\x0013]ÅlÏl{#÷I0{â\x000e[\x0007¢ÑA"PS¡E/Áb»Á[Òx;\x0011¦\x0003¶=°U\x0003ÓÔ\x0018\x0001öMàmsúÒòz`ß\x0003{5°[/9µ\x0017©ÑgríèÓö]Âçýw?\x0006sÿ\x000fG¡Kìùøõ\x0007Êßzÿ\x0003¥o-\x0017\x0008±bú\x0005óoDVÛÜ,\x001dD\x000f$÷þ·\x0013\x0015|´éSù¹ýá·ï^,o¬\x000f)IëÅÊ»*½L>K«þ`Yï>}\x001dõ»×ïëÛä\x0005*\x0013W¤óË½Q^¨ÐÔ\x000fì3¦p¢zþìÕKÙ8¿»{¾úþØa\x000f\x0013`!¥*å%,§\x0006Qa\x0001Xð</p><p>´ïVÙ\x001eÌÎX¦\x0015Uåq1o\x0006óWÙËõXn\x0006«ø%½>¤£°b±W>}H¸</p><p>Ì÷`~\x0002Z\x0002'\x0006+gêj/õH]¸\x000f×p+Ì\x0018Rõ\x0003syº^À¸ÿ$¥«Àb\x000f\x0016§À\íU]ÀÂ\x0001oIn8VÀ\x0010¯Zù©\x0007KS_Ò/w®8«¥x´~ÉÈ+\x000c$IÉ{®<ÃU>_b\x001fVk\x00170W\x0013}Fï:.\x001cñ­f\x0006,\x0002%§-\x0016£·º'\x001dÔ.w\x0005Ì!\C6zý	·\x000fÂ­©dÎ\x001aqûÉÖ²ï"Áâ5dÛ\x0019¿O·Gü1c\RÌ\x0007Ã\x001föí5d	\x000f\x000b&Ô\x0017ù¢ßaYp~ÇAP¶D×8X\x0018\x001c\x0019Lx²\x0012\x0006×\x0002iç!/ç6\x0002Ë91wW®ÿöºzÚ\x0003ËóêîOPêm@\x0003Áêb+Q\âm\x0000î*ËáÏ\x0000q</p><p>°f<&±|Zê¼Î¡Ë¼O\x0005­\x0001Ìý\x0013NýÁxBûúþ?o,8K*\x0004F`.X©'&!0éÕ4_?xøõ\x000e(ì¡p?\x0014b}¾uÔ{úy-P<³àôP¶²¿\x0012K¹\x001eÊí¢\x000b3à\x0008ÖµU\x0015¬÷þ³P¡</p><p>S²ÃÄx²Tp,öáØ,Tê¡Ò¥Äú?ÙRØ,eÕP~gs6@ê3¦rµs\x001d*Ðôòjª,rzKÁ°û`bûE¬é£tü0=±@ev¥TÝ¯\x001a\x0016:L¬tðõÀÑù2$\x0016(\x0010¨Þ{Î.)\x0018{þyOÿm²â
\x001c\x0007ùådX´]À²\x001a6î×[ÑË×÷6\x000eµyd\§=\x001dj\x001dû)\x000bq4Õ×\x000f^m\x000b?÷å­Àv\x0013æ7ÕË\x0012X\x0001\x001fÊÐ\x001a6Ë2gYÁa{\x000e»\x0003\x0012G{ÃR¯\x0005</p><p>¦\x0019älí\x0004q=Û\x0003â!Î\x000bHX\x001a- m
[§\x0003ñ=ßõe¸sT\x0005\x0011=J\x0008¥Á\x0008=FØ¤?7e9xq~\x00163
 Z©±\x0007{ìA±6oÚ/x±Gl Ò\x0002f\x0012$õ iEJ\x0014»d_Ò;±½Ëyvd\x0010¯âÈ=GÞcTöm\x001cÆò½DÓ\x0005Ä)@`tf{¼\x0019eÙj\x0011îëøÜ\x001d-Ë¶^åEÜèò}×ÍuÛ24Ü·N\Þ\x0003êÅIãñn\x0007ÏÝ<úárõ\x001fïëtáËÎÞf¾Ç)Î>ÑÜÅÙsÇ²û³SÅ\x0017\x001f¬O\x0012î °ÂÝPå_ÛÂ÷²³ª3Î47\x0017¯`²=Ýo(Ãí\x0006I\x0004\x000e_\x000b\x0014½²\x0008\x000b\x0007Ø½P®rû
\x0015R\x001d\x000fLÉSÇ¤\x0005ÊÄ¶â{½P¾ò\x0013P®ÖiÑ×+:ÁLFÔÁ÷ÇY¦Ð3ýLå_-~&<-_\x000fr2YüQ¼pÉµ\x0017*öPQ\x0005\x0015\x001d=¼2?âë¥\x001e*ír\x0001kãÊâ/½!>J\x0001yó9¼âëå)ïg*Qq½/¡NâËf)²¡\°ú¯\x0007£çÜï:mmÎKTXN©õ@\x0001!\x001b¾dðÁº+ÖÔ /Ëº\x001a®>c±²,[\x000c3MXX¾bLb1ô\x0011à
`</p><p>ÎX>ï\x0004ÈË\x000cáú9­|Í pï\x0010Ï®±Ê\x000fN­ ^Ü¿yûêc?¾y»~i\x0004µ2ý\x0016\x001f¥-HðdóIk×\x0017\x000f\x001e=}I°/\x001f­M2ìÐ°GÃ)4</p><p>bâ)¾ä³+§°§@w\x0015íÑì\x0014Z9Ôcõ\x0012_Y¾\x0015«\x001a\x001as\x0015ëÉÜ\x0014srl£B\Ï·\x0010!Hh\x0013»s¬\x0006Í÷h~ö{";Ù²ê¼<³·£m×}ÏÐ£	´:\x0000ñd5Î\x0000ðÉRv±,ödqRvùLQâ\x001e6òFc\x001a¯BK=Z3Z¬éf(·£\x001aÍÉ}³µ×íÜ£å)´\ÇoÔ°\x0015ªçð9ÊçD\x001dÁóW\x0003l¯\x0006_Üø°þÎâ$\x0005\x001ei¢â\x0002¹ÇãÏ\x0017\x000f^lä¹4\x000eì9p\x0017\x0007´K8Jõ(\x000fëÅoÃö\x001cv\x0007GÊ¾mÿtr\x0000s<Ía9F
ëAÜ\x001ehåN\x0007B âã\x0005ÄÊåRùUÐ\x001e$ì\x0001	\\x0005]@Êçr-Be7\x001aØÄ= .ÉA\x0006Ê.2õÓØ¶wèÊ}</p><p>d\x0018LY@{æÑO!'­ª\x001a¥¥ô³ZròÌI9\x001e=ùve5:ìépÎ¦ZáCßÎËî\x000eAÍu~PEg{:;K¡¶k­ç\x0008ÃïJÎÊ\x0012wÝë¸</p><p>Ïõxn\x0016\x000f¢ÜwÓz\x0003'\x0001¨\x0004í¾s\x0005*<ßãùië%\x00119(Ç\x000by\x0000s¾-=®À£z\x0001þz0-7XõÎÞB½\x000eò\x0019óöòk)«ã»ûq{ÜÏî\x000fÎË\x000ba\x000fí
\x001fe\x0001Zå\x0017\x0006çFßR~0ö®ùæýë\x000fëâøX¿.Òù\x0006ÖÈý?µOùC×æåçw/\x001e¯ö^ëÀ°\x0007Ã	0\x0007 wë\x0005\x0012bvb³î±AÁe{.û+2ïÁü¯\x0005¬ß¥\x000bØ²Kw² ¦."\Ü\x0012dÜ^l\x001cåÅkØÎoÁáì\x0016üÉý÷oÿø~ý..åZlWDÝ;Ég4Vn-Ñ¥\x000bé?O\x001e<~ðôËç[×\x0012ç7ápv\x0013þ9°@éyìÓÐò%!kW¼\x0017orö¹\x001eÌÍX¬DÍõB¼|ÖeØM½¥b\x0011®\x000b\x0017âûÁB\x000f\x0016fÀHlûoê$J¡»Îb©\x0007K3`Vä2ÃY@\x001a¤J\x0002Ð¥KèÝ`§\x001ceñ	²¢ÜuÜ£¦\x0000õÁn2%1¥\x000b©eûÁÅ\x000f3«\x001f½¤\x0000¯*wrà½o\x0012Æ÷
«\x001ff?¹¯\x001aéú¯äÀ%àÛ%z\x0006¹lXþ0³þ¡°9O°\x001c°Áx`-%\x001fç\x000b¯</p><p>ûÁå\x000f3ëÿ\x000bÃòÇåÿO\x0006\x001b}ÿÌò\x0012r³+£\x0006©^ãÛ$yEë¯YdcÞRÌá\x001eÿ³\x001eÍp)k	Âèa=\x001a`Ë\\x0002G\x001b\x001aöÖ\x001ftÃ\x0004\x001eßÿç»7ï×bl0\x001e<ê
S¸­ºÄÓ\x0013/¼¯ùêæñ\x0003ª°û<\x000eö8¸\x0013§èNí}D7pîÖU9VM4¶Y\x000bd{ »×>% æÇ\x00040Ò4ªb»ú</p><p>Y\x000bäz ·×B1×\x0002}ÊApr{\x001a\x0001ÄB&ªB\x000f\x0014v2¬\x0019\x000bkõfÑÊËÅ³\x001b¨	 Ô\x0003¥ÝÌS[öRÌ@\x0001eQ;ë&¾§ù\x001eè\x000b</p><p> \x0012\x0015</p><p>Þ<üóý§?Þü®v\x000e¾¼ñ!pâA±<gC@æ\x0016\x001f`	§Eýøîæá×\x000f^}yó;ê\x0010|¹L0~÷·÷öÿ·ýptýpóûûOïÿóÍ}m|Ä>\x0016÷¯?ýõ7ÿëþÇ\x001f_SÅ3¡¡+ÑÝRhS9W×&ÑFK¾Óuo¹2ãùÝ«¿ù_\x000f\x001e?¾£"æ¾©øï\x001f¼zþí£\x0007«m\x0006Ôâ\x0005PêK@¿¼µçä©ã|®¬å`V~Ð¸õOo?÷îÌÚ±¼ù¢|çwõíà3¨e'Õg¡ËÂ¥0PËÆÌ\x00155IFý\x0019k7Ñòæ²\x0006­>*\x000c¨Õ¬JÔ²YÝ[P\x0001É÷.¨üÊ</p><p>x$jq»V\x001aSíÁLV]æÝ\x0011*PÙN5*Ô!-j§&-È\x0012Q¡\x000e¬-¤`\x0018õòZU¢?¶×¢Òú¬65Ô\x001cq\x0001Eý_V,\x001c\x0008Zt ¨mê 6T!.õmMi;ÛôÐÏ_|{R£\x0006[\x0004i¡f:÷/¨RëJ½ìVu¨tv=ù<µ©j\x0005(¡¦:³ ÆØ6UL×¢þ¿ù\x0010ÜöZE%`þýýOï>¾yûúó6#×såe@J9IC!Nb¼øõ\x0017À\x0012EÿþÁg/\x001f=]»\x0013\x001e Y¥~ÿñÿ½þó\x001f
ßøÔö§·÷ÿñi\x0007\x0012-FzSÛ%G\x001aÍ&òÉµÑç\x001fúÙWO\x001füÛ«µÛþ4-¸)&¤9N~JEÓ¡:JGïì\x000b^\x0005×P}w¿pÝÏab0_ÛÆ-`¾]v\x0002¶ö	ÿò×éo÷ÝføÝë÷?uÓénþHÏ"oé­õóK',\x000f¿¤¬TæH.x¨qFÊ6_ü¨¿»{þ¤TwóåÍÝSz]ß\x001döÓ§¿þ©£~òîí_~¼ó¡Fá[yû\x0005äHé®Ë`â²ôÐÕ¯\x001c\x001cðÓð\x0019ægO¿yüàÑÕÀ¼óû7æ¿ååºàÅ§÷7?.cu~øóë\x001d6,v³·UWl\x0008µ	VÙ´å^mh\x001c^Ôjê4òx¦S"ÌuË}ÿöíû×ïÎÂ´/¨­ÈÍ·{V¢¥ÑØ¾:èr ^Z¿\x0016<ÅA{¸h»åZÜ|»±\x001aÿ\x001aü\x000fÝw}<{~ðU¹ìÔPxÐ´\x0016ö)ñrûx\x0008Æ×Î8tãØ]lÔ\x001f\x0005»ÿé/÷Úå-û®\x0015ªÌ!Íl©\x001f9\x0004\\x000f\x001eê­\x0007O¾yðÕon´ØÓ¢:ÚgËÀê\x0016à²\x0004\x0004Ø]v</p><p>`Û\x0003[­yKLæ°\x0002\x0007¬3ÈÂ¾YxuÎòº×é\x0003uZxS¼
ËÂB^\x000fÐ'q}ëÕæ].Y\x0016Ü\x0018(õ¨òf1¯T\x001e\x001f\x0000\x001czà ¶/PþC\x0005\x0006b_Ñ2oLñÆ7jyÑPúÒÂò%\x0017^ÃÅ\x000b"\x001c¶"R\x000fÔ\x0006¶¤\x0006ÕÀú8V\x0003\x0007±prëIàÜ\x0003gµ\x0003=ÅåÈâè5»Z8³K&\x001cåùqO\x0014Ã¨ðÒ°j!¦7?Ç&Fdb\x0017Ö\x000fGÄ£Æ©E\x000e3UDW\x001bg¾"¡_B\x000c°~3I<è\x001ch.S¯´\x0010#.¥ÔËýI\x001cÂ&\x0012:\x0018\x000eÔJGi"UéèÆLb	Êg\x001b»£\\x001b\x000cR\x0007Z­Ë\x0018)¥¤\x0019Y;3>ÊSÀ v V;»$åT\x0013\x0007*«ZL\x001cÅÀñòQUÁ;h\x001dhÅ.»</p><p>kË«Jg¥Ù¯¥tTä\x0003ÒZêÒÒ§r±ntË ':Qx1oHG)\x001d\x000cJ\x0007J©s\x0006\x0004Ã%äiTTBÏ\x000bø¸\x001d7H\x001d¨µÎ\x0001\x001ds\x0017\x0013c @ü0Æ£¼\x001a\x000eZJ­sÆ\x0000\x00171ÔA§ÅÄ\x0001Rù(qÆAêP+uù\x0014\x0011S,Ã\x0007ãÄáOLÇYx<Ñ©.Zz\x0014¨w5QVq9$ó*Î!\x001eµïpP:T+O·ÃÈs÷\x0012þ¸ÃÖÄ t¨\x0016:*¯áC¨¸#NæES<Ê\x0017ã t¨VºÚpt±±ÇÚNºØ\x0018¬,cwÜ¾\x001b´\x000eZç();UOá\x000cÒ/ÙSÈc4GE\x00138è\x001dªõ.¶KR\x0008XçØ\x0015\x001bcs\x0015þ¸U1\x0008\x001eê\x0005/Éª°\x0001êÈ²bcqÆÙ\x001e\x0015Äã w¨»zGY]±«]»É\x0015,¾Ø\x001fe`;¨U«]m¼\x0018Øû:A\x001eCäÔñ0_l\x0007¹³j¹+a\x0004Ö%&ÎIÍQäÃÎ¢vÐ;«Ô»bcG/ßÕ\x0019Gy®G×ô.ÃQÂWZ½ËÖË\x001d\x0010åc%ñ³(\x001eF<\x0008U</p><p>¼¬ã%ÑÄBdÎþ°;\x0015;\x0008Õ</p><p>^9g°«@DÚÊa)s`|Ø­ \x001dÔÎjÕ\x000e¡Ç¿e\x0011/=Y\x0017ûæ¥\x001fÒ\x0001ÀØY­ØQ_CË~"@Ë=Xî\x0017\x0003;wxØAì¬Vì\x001a<KÐ|ËfÃC	ÚÜaê1ÈUÊ+\x000fÕå,6¦ÄvÉïpbã¸òj=Oì\x0006½sZ½\x0004äe\x0019\x0008î´ºRqÞ9¥Þ9ê\x000cÀ7%ð¼4ÈÚ­ÊQ«Â
zç´zGë8\x0003ùi\x001d'±q>J=Ü wN©w®á±*´u-ùËÜe£ÄÃ
ÎÍ)£*iËWmÅÏåz¾+\x0011ï{Æu«pZWÆß:^\x0013Nò[Êñ¿­x7öÃ¾óÚ}Áosn¹6^\x0012_ø¬	G9</p><p>{jò}</p><p>5ÇF°S\x0013n\x0012§qH¨\x001dýýqJí\x0006îõà+øª0Q½sM\x0015µrÉ\x0012\x000fÛ]Û÷ÓË»\x0018\x0019é¤W¹±Î¡¥kdÁ>LP\x0010Î±ñ¼aðÔe\x0000È9</p><p>ÐÐ½@½\x000c@±7Ã´ûgàN\x000fî¨¶×¥Ü\x0005LÍöÌpØ{¯ýÙB±úâè\x0005ïÂéÂ\x001c»{ÏlØÙ\x0018ú»¯ßÅÑô\x0013å\x00016PV]á®\x0014-à¶Ý\x001b\x001dvÃlãÏ\x000c\x001e¯X)6K \x0018Ú
]ë\x0004©dY)ç\x00067×\x0018ü\x0017¸ñ}+¦ú®Ð#Ý<¹s\x0003åºë¾\x0000(F¥Ü<ï\x0012åzï%\x000f%~ÚÊ/ÿ®\x0007ê¿ë³¸Øã¢\x0012·Ô\êá©c¹éì-\x0005+9­ó¸¶ÇµZëÚÚA¬\x000buò'=[\x0003o¿6Íéz\ßãz-®£ÖÞ\x000b®s,©\x001b=ãÂV&ý\x000cnìq£\x00167H1/\x0016ùÎÅ°´ÁÍ=nÖâ&N!Î\x001eO¯}9ñ\x0001\x0016ßª¨Àír¼é\x000b+æx}¤â(y8nn9©Øo\áÏáLíÉrmgVÌ\x000bÊìªy³7näCÎñ\x000e{
´ÍÚxÓcí²w]çpÃ\x001b´«!×¶e9l¸\x001e\x0010Å\x00198ÈÁà\x001a@ë\x001b¨Ô}C	5¹øÁ´gT\x0008\x001b)-s¼o\x0000­spX{]\x0012¯£\x000bq~\x001b\x0011_\x0016üV½Õ\x0004/\x000eÎ\x0001µÎ¡\x001cP}-\x000f¤A_bßÀw´1\x001fµÙpp\x000e¨u\x000e\x0007i¸¡DhÍ¼®-ÍjÆ\x0019Þ1ÌQÇ9(aYÙcuÔ5í6Ç%\x00139Ù¤
8\x0007µsµ\x000cÙ×ÒJ®ö\ð\x001bÏ§s¼nàuZûÚÚËR\x0008\x001d¿§\x0017ûz.ÚÊa³fpw\x0010\x000bToö¥%²~7G­ßA-P«\x00164\x001f¥7d)\x001enù1ûÒ9ÜA-P­\x0016¡¶\x0010È®:NVo\x0014ë:{uÓ¸eÅº\x001aÐ'i#°À]¬ë\x000es\x000e¶¡ZÛhxr\x000e\x0015`\x000f6;HÕJ[\x0008u`K±®Ë</p><p>Bï»Ík7Ææx\x0007­°j­È\] gLk,¿2Ålð ÈÌGbµTÚB¨¬\x0006\x001by,\x0006ã·jàgp\x0007¥°Z¥2âE*ªA6/J\x001ftÔ\x0005\x001dÂª"+3§\x000cM\x0013¤\x00144¦|\x001dÂj"Z\x00116ª
\x000b\x001dË	T\x001bzy\x0007¥°W(E®«×Ri\x0017Ä¼\x001bs¸RX­RÐkcµ®5\x0012]LÁ:ð¨0Ý\x000eJaÕJ\x0011Û!³l6~¹£jL6oØx âuÃ±Â©\x0015 \x0017ÞäN¾Lê\x0010ÌVZæ\x001cïà\x001cÖ9\x0018W;Å\x0016Þràle\x0013\x001c¥\x001b\x0019H{=î°\x001cv9mæ5FÊ²÷±\x000eºòÃrðÚåàÛ)\x0008chË\x0017Px9wb¯bïé=¿éñÄË\x000f·%LÇ"\x001d?^Ok¯\x000f4u©EfìÎÀcÌ\x000e\x001dü \x0016^+\x0016;eÄ,Ya\x0006Z\x000eé(Üa»yív£\x0007 6/$®\x001f.¼Q\x000eÅÛ=&xÃ°Ýv»\x0005#oñ\x000eµ\x0018Df\x0019\x000fòfaØmA»ÛhÐZÕâ\x0018©ÿ!ß§Kó§Á9Úa¯\x0005í^+'ø ¡Ã2m¼Jö¨×</p><p>7æ¢Tyk/Ç7!Ë</p><p>g³\x00041'IÎ¥bÌk±Cún|~-Áu«ô?ÿõßÏ>\x0014¤7ûrâ\x0003eÔ|\x0004¨¤ p¿¥P$n3³àæÙòG[¯Å=.jq)½<1n¸å',Ï\x0002Wh7:íMÑÚÖþêëz\÷k7®ïi½\x0016¸ë^9²\x0003É2'!%¦5ÛÅ\x001cûiCO\x001bÔ¶]\x001ab,¸T¯Æ\x0005T.!ãPg</p><p>7ö¸ñ\x001aã¬[ó_Èº¹Yw3ux?nêqz£9~^I\x0000\x00138Pç8²Ðnçuí§Í=mþµ\x001b·{'0¿rëÂ¨hjIëÍ?³íA¬ZÏ~)Ó\x000ez\x0006jAûEL;\x0019¨Õì2í fp\x00051-úu7ëºöó\x000ez\x0006jA£âðjÝh¥WYFÎv	Ôtæ\x0018ÜAÏ@-hµÏÂKEâ¬¿ æ]k9;è\x0019¨\x0005ª=ã:\x001aZÍë\x001b®ÛÌ
ßÏ;(\x001a¨%ÍÄ:B±ðÚ¥GCís×m¼ªÌðâ i¨4\x0008¬Ux\x0003m<Þm(¼éX\x0017\x0007MCµ¦\x0019O¹±\x000boAú{é#\x0011Ý¸Ùâ\x001dij]\x0003W\x000e»Ìë9_ l·(ë\x00017bOñ\x000eÂjaûÅì;\x001bªÅín_0Þ2ÐÅ\x0005/ße\x000cðo¨;ì\x000eÔTöWõ¼9Rr´Sã\x0007A\x0007ë:\'\x0003SwØÏsbÏ\x001aNJq©ý©
\x001c@jåÄ v½°z\x0006Ôö V\x0005\x001a%7+ÆÄ\x0017y\x0005Å¢vUzg@]\x000fê\x00165-jùµ§\x0018T8ízNÖ\x000c§ï9½3Ë3O^B¯Ôzo80«b;\x0003\x001azÐ \x0002µr¹\x0018©_\x0013·ÍRJïp½ÓÍ\x000chìA£\x00064,¥Õ¢[LîTöY\x0001M=hR9§È£\x001bb\x0002i\x001d\x0014Ã:X?Ïpæ3«\x000c\x001aA)Ýý½á\x0019\x0003Å ë·á\x0013 §\x000bÅÛ\x001bå\x001aMÍ¢Øhs÷ë=`g@GYRéR}!\x0015äËÜ\x000e2é\x0011 .JüRc)\x0002</p><p>,LIR³\x001ebÒA@¥LiÁ«&ÅVÌe\x0003\x0014Ø¼Þ\x0016qtP&PIÏ2](u mióiã¯?ÓÌ\x000eÚ\x0004*qÊ#ÓbS×Þ\x0010Ú~2ëé\x000cè M \x0012§âè3ïüÂ,Å[à\x0014\x000f	K`\x0010'Ð¨S6'uòËÖB\x001a\x0000d®7\x0002 ÅÁ¢ÆÒ¥\x0010²Mml\x000b¢ôu±\x001b½sfH\x0007o\x001aoZ\x001ezBsS¥Ò0J£C»Ñft\x000có5îzx°T´­«z\x000e^KãçØú88)Ô8)j	çB%ÅÄE\x0018TîmX/Ñ!\x001dö>jö>Ý®YvR(IªT:0Øpy\x0000È,é\x0010ï¡&à£zc.¼ÖJLÙKYî~\x001d©\x001dö¾Uí}º\x0005æ½o	!ü\x001c\x001bé!§\x0012ÿÝýxº×È)RG*§N?%ßb©õ¾=s¬ß¬ßk\x0014×î#hÈ\x0008ªý\x000fa¡s\x0005G©U2	ln%N=]õH"L±ízò\x000eÞ{\x0019Ë)\x001aðN\x00014aìÍÇüýæ÷ï~|óîãÍÃOï÷ÜK9ê<!+·\x0001Eú9kÇÙËAÀÃG/ïn~ÿìñ£g/o\x001e¾z¾q1Õx±çE-¯\x000cÞs©i¸<³ÂEïª@µ=ªÕ¢zGi\x0003D\x001btJ°N:+R'áËÑæy]ÏëÔ¦µü@\x0014|>ÂÎËô/Km¦Áõ=®×âºÈ©É)º*:®4tý ÜÐã\x0006-næcv</p><p>Öñ}u\x0012\x001a`ñò<\x0002\x0005nìq£ÚºPG$\x0016ã\x0006©Ç³m§Ã¶Zêi\x00039\x001eé-­Þ%>\x001dF\x001b.¿\x000e)xsÏµÖµëñ¨m¢Ô\x000f££,Þ|ùµp·]\x0010U0êå\x0010¸</p><p>úàfe5\x001cäÆ`T4µ¤YÉ1¶A´Ê®\x0016\o.OS\x0000\x000f\x0006jM«Cß«\x0006GiÁë¤õuÑàËw</p><p>àAØ@­l6p¤bî:üX\x0018/\x001e\x0014À²ZÚã\x001b¹\x0014çÐ¼D9ýCYß\x0007ù\x0007\x0018´
ÔâV¼X­\x001a+Ád\x000b\x001bù>>z{¹´\x0002xP7PË[qcÈÑCbaÇ¹õn¥¢\x0002xÐ7P\x000bþ\x0019©8°[îªxàxT´\x0003ÂVâÐ{>\x0007ðÌÈÔú°ùr3\x0005ð q Ö¸ÓèúåØ&K\x0018eÏåËu°óÀ8h\x001cª5.d.ã^Æz\x0006\x0019k%Hæ(àAèP-tÐéÑÎKc./Bg\x0002\x001eÏnj¡£i0¼!Ing¥^ÈËéõ</p><p>àAèP-t\x0000-ìÉF\x001a\x0011X:ZT\x000bC>H7pÐ
Të\x0006pStÛZ\x0005Ë°o\x0015¸\x0013F­\x0013âÔj£\x0014iâ+wþÑ­4¼V\x0000\x000fN
µNùºdyÜ\x0002ÜÚå\x001bÞy`;ø\x0008«õ\x0011 %o4\x001c\x001bíb;\x0017y8êÔiÇ+\x0013í#\'\x001bÎ·©ÙIªû=^~P\x0000\x000f\x001bÎj7\x001c
0("KèQ</p><p>x]:êúÌ\x000e;Îêw\x001cÜÖ¯
w\x0012åËE8</p><p>ÞaÃYõsòPQ\x0016°îçEªÅ¥ÁåKõy`7l8§Þp.ñ«jYÁV®¥</p><p>°kg£+W9¿\x00006|\x0001|ê?ûÅûû\x000f\x001f^ï\x0002^¦,'Ç=<½\x0014·ßpÒÃs;\x0013øÁÍ\x0017Ï\x001f¼xq·\x000b\x0019{dü@¶=²U#c(¹Sj6¤ÖIN\x0008®D\x0012*d×#;52UÌ##Ë\x0004JLÒ9\x0017·z?Ì\x0012ûØ«:K\x000fÇâÝ$-PVÅç¦Oð7èy\x0001ËÂ21SÚ\x0015âãc\x001cõÈN1ùSYdJxZ\x0015\x0019Q2zä¤÷\x0016¶õyÅÜòÛ{\x001cä\x0003s¯Bö(ñ8}nªÊ~â~l¸9\x001b\x001bþkµ2ÊwôÉy´0;É(¿!\x001du?Sd´Ù«µë¯õ¿¿ýÇßßßÿxóÅë÷\x001f\x0017¶ÏG¥©T:Õ©Ç`ØØ\x001e6ûÜ|u÷´üõã/î¿\~þYxìáñJx\x0017i¨\x0003ÁgÓÞó£¤è²â·:xÍÃÛ\x001eÞ^kùå~±|vÜ®\x001fËOÅò[=.æÑ]î®µ{b£Cgô$Ü=</p><p>çÉ}Oî¯5z\x0006T÷S¦Ñs3úfW²yøÐÃ«ÍÞàÁò¥W±¼¤Úx»Ñ÷@\x0003\x001f{øx%|\x000cÒeÊsÅÑ$iìÝÁË&õðéÚec$gà!³å¥h?ÖKæ\x001e>_kù8XMòñcù.\x000epÃ\x0008\x0000µé9»ÚìsUAZ%Pßd§¡\x001fÕõZy
Ëj©¶÷·\x0010X^ßl*8\x000f?\x0008\x0014\«PÔ=½
\x001c# ~£Y~Ð(¸V¤ê\x0013\x0001Ã)Â-uÉ1I\x001bþ°1?W\x0003?È\x0014\«S!Kö7õ7\x0017o\x0019%£Þ9¤\x001aúA§àZ¡JV&\x0011²ê#¾Íí\x000böà3\x0008\x0015\­TÐ}{\x001f-¶ÍöùX98{¸ÚÛæ/\x0003JsúäÓzq\x001e\x0007o×zûèd"30mRÅÇ¨\x00106Û\x0016ÎÃ\x000fÎ\x001e¯uö©%Soa.\x0019EhóÁ¦\x001fÏR×\x001e¦R±Æ6©JÛ\x0018\x0001©¡\x001f´</p><p>¯ÕªdÐæÀy{Åö\x0010ÄÛovG§\x001f´</p><p>¯Õª\x000cD¿ØÞ-·\x001fÕörá\x0018üå«~5ý Vx­X%Û\x0002Lj/	lû\x0016`æÍ¡\x0000óô»ÇkÝ}wVã\x0004ßî!Á·³9®g~p÷x¥»O\x0010Në>qmL\x000e²Ð\x001f\x001bæØÁcÚ+=&=¿ðDbcbëg`¥ñBÀÍÙ"óôã\x0005Î>'\x0019 g\x001e\[9\x0008þØ0Ç\x000e»Ö^¹k)\x001bPü=Bë(mÝÛÍ\x000eÌè~èµZ#ü®×ª:Vsmõs³\x0018en þ×úÍó?\x0003ú«ÿ\x000ctwÌÕ³99©lRÜçzk\x0007ûüÙ\x001f"^ÿ ÜRÖì¤á\x0007¶ÀÍ¬ë.\x0005Ïÿ\x000c×\x0007Ê\x001bJÀ\x0017²é6säìÛe²Ýjß«¸	?UßÕ»ðû«/Ã}ä|OGßzQÒ¢ÏíöÃ\x0013üùü\x0019"÷Ï\x0010ÏßüñÝ§¿î\x0000¦ßÜÆúAPÊù
\x0000kæù£/½ú÷Ïcb</p><p>Lº¸¬¥¸@Íd\x000cJå^JÛSZ\x0005e\x00082eÎÆKoé\x001dóæ5Ù^L×c:\x0005&Í:¯ß<ØË9É\x001a</p><p>isbÐ^Lßcz5yÖoÙ8mf\x001fåöWkn{)CO\x00194Æ\x0004Éy¤ñ\x000f2ÜÊI[÷\x00107'\x000bîÅ=fÔ\x00183Ê}\x000f½17:\x0019L`¦\x001e3i¬i¤j¹h}ÎOC1ø¸%Ã{1s\x001b&ÍEåÁ\x0019Ò,4\x0016Î\x00030»;ü<ÜáO¸Íñ4kË\x0002ç_nÓÙ9jF9kµ	uå\x0010dNÎËÞo]´îå\x001cD\x0008T*d9!)Ñ««Ép¢Ba;:ÙË9È\x0010¨tÈó`\x000cC.FV§»\¼39È\x0010ht:ÖpU\x0014q	§ÌG	\x001b]\x000b&8\x0007\x001d\x0002\x0010yân0´IØÅÛ\x0003\x0001÷r\x000eJ\x0004\x001a)¢FÀÕy¦,Ó¾0H\x001d_¾\æ;É9H\x0011¨´ÈÉH½åÈÞì)a\x0012®÷\x0000à\x001c´\x00084b\x0014%\x0007:iðÓ[·>}:Ä\x0018J¬$±Ð#L[\x0005©bp\x001aá F¨Q#o¤Ä¿ü½­ã[K¥ÞhR39¨\x0011ªÔ\x0008øÅ5\x0015¶A=ÐB%Ê-¿s<\x0012iÔRÓ93}y5¨Ö4bN{ÄêÄAP#F-¹--áL\x00029ml?Èìå\x001cÔ\x00085jD\x0007×~Ð04îWR«3·Gp\x000ej\x001a5òÕ(Ñ\x0000,ÙíF8Ãå\x001a IÌAP#FÔ%·v$e³s¯$\x0015Ï.n^</p><p>îÅ\x001c´\x00085Zä½\x0004.cÛ`xæ\x000cár;IÎAP£E.ÜºÖ|ÆñfO\x000e¥g\x0003\x001c 8H\x0011j¤z\x001fðñ
¹Ã.Îo×Ù;1í DV£DµÌDÚ$9¾õJ­MÛ|òØË9HUÝÎaÛë \x0003\x001an¨Ù\x001b=±'8\x0007)²*)jçLjÍR)\x001fÝm>îe\x001cïæ4:ä2:ÔÃÜt¶GÈº\x001dtÈªtÈ4[Zi~ÔRêÖ7FOìç\x001ctÈjtè¤ÔÒM&zuÚNoGìõA¬JL«RG×úÍ\x0015QVMëmÐ'8\x0007%²\x001a%r^j½©Ù4·ìNQZäõ.Ã\x0013\x0010Y\x0010Ù,é»6³\x0011¤èßmÎCßË9(Õ(\x0011õjw|x;\x001d6$Õ¹\x001cÞÌ\x0001ËÓ
RäTRdäNÉÇÜÚ\x000bÆÖ§í¨Ó
Jä4Jä@\x0006JH8gÝÖÛO`\x000eBäTB\x0004rØð!¬Ù'\x001e±Ü FN#F6s`*:Ùâ¹ÈóC¢÷\x0015?{9Ç"\x0018Õo^xN=¥ã¡#¢97(Ó(M·µ\x0018fF´>½2è"z·ùèºsP"§R"Ë}¯SA\x0002,ÛË!î\x0000ÎAFd(ÃÒ´A:·Ïîq£¶y?æ Dn^¡\x0019]u\x000f¹ènù¬!cX"=&\x001d9\x0008Ó\x0008\x0011¹K¾§IÐÎ\x001a±õì\x0008\x0007\x001cýàà½ÆÁ[/Tr"ëíòã\x0000ÈÁ½û_k\x001a\x001f¼»Wyw'7sÅoÊôpj\x0007y?òãûºÊoÚÖ\x000e©D!"!¶;#Þ_üà¼Ê\x001fI_ØVÆ¥Ñª\x000bla{Õ.G*ª\x001d5o9\x000bfk@wÄ\x000bf\x0018vyPír\x001aI÷\x001e\x0002¡]{\x001c\x0010laÿ\x0004ÍþÁD\x0003ç¥w1gbg/W\x0016ÕõÃ\x0006</p><p>
2\x0015(¢í"è>¸ÖÄï\x0008Îa\x0003\x0005Í\x0006*91µ«m/-T)õý\x0000Îa\x0013\x0005Í&¢yíÜU\x0019P4È·}a}Å~Ì8l¢¨ÙDÉq1½¼ð6ò<ú<ZÄCV\x001c¶QTm#Ï¹É'l7I¾\x001dÕí\x0011¹}qØFQµäæÎl2¼ÂÓí@.\x0019Tª]ä¥'ª÷F*¿³ËòÙÍfð^Îa\x0017Eí.bNkÛÃ 7ÌÛ ;9Ó°J¢´\x001döÚMRæp¸]$·sØFI\x0015Íµ\x0016`.z©¬ÉAÒ\x0000¨Mã\x0001ÃúLª§¬_"7
ë3©Þ²4]´ÎÝÊ\x0004\x0018Ö"À#Vg\x001eVgV=½$\x0019÷`©?<\x0011ñíX6û\x0001«3\x000f«3ë×+¤1RüBo\x000cpyððYùfÍiX¶¸¤ö¶^"Û#9l¡¬ÚBIÞ^ÐC\x001b ä\x0018lÜåÁ³s¨¨\x000b´+eRz'¯Q'W `6\x001b©ìÞñç¸e×kpS<3£DHò\x0010S~È;</p><p>ì\x0011\x000f)þ6*Ûz¶Û\x0004Í:y@+S£ÿn¬(ÿs|%òÍ×ïß¿¾ùöÍ?þþöÝÇ\x001d¬Ôá«Nâ©Ô?\x0004)77ë	ýß<º{þüîæÛGwO½ü<®íq­\x00127\x0004Àds[	6È¸ªâþI^×ó:­ycK\x0000%ûTÄ\x001b©êY\x0019A¡à
=oÐò&#=CR´²tcJÒ<á ØÔÃ&5¬¿\x0015VÓ:pe©øry}Tñ\x001cnN_p%~7[~m ±UÒ½*6V;¯w\x0005\x0004\x0001\x0018´»-9©£¡Áê2rÏ¶1àñ(ÞÁÖ% ^\x000bnÑ`®µ|¶.%'q\x0007ß\x0000ZçP¼Ì³+çWYÀ%~`çà6&oN\x0002\x000fÎ\x0001´Þê½¹­ÍÒ\x00136±¥ZÝÅõ¤¢IàÁAÖCÐ2\x000cLWÀ¼$ÈÛÆ Æ9^\x001cÅX½\x0013´
G\x0013\x0007db \x000câu\x0007\x001b\x000e\x000b\x0018Õ\x000b8ÛÖ}Òvå\h\x000eâ ÁèÒ5	8j=°·^$cy\ã\x001aa©Õ6çN(\x0005Ú\x0005L\x0019ÎÕ¼¦=`ø,ËÁ^ô¢	vÐw	x$òU,âÈG¡L½ëxÓeëÄ­Áú%çlLym¯À¦yq¼6¬··ò\x000f|õ:ÇÙpâ\x001c»\x0014zî,¥e¢MÉRsÒ»ÖÁú\x000bì^nß%ãe\x0007\x000eÍv¿|÷áÃü÷{\x001aã\x001b:Òó%¸M<¼\x0013¬Ì&¡áÃ«§£¥×îÏ^¼(à[­v\x0019\x0018{`T\x0003$ÕQZÌÔ²\x000e8]3ûð.óûmOlõÄ"ÔÉ;+ÕàL»pÞ¸ $v=±S\x0013G<=4y~\x0010+6d\x0007\x001b×=ó,±ï½ÞÆoôTkC¸às=æ÷ã\x001e7è
\x001cä.:Pþ-\x0013·gfû¹±\x0003ûc\x000f\x001cõö
r£æCºspQq#¿q8õÄé\x001a\x0013Ëd¶Øfõ\x0015\x0013Ë#9¬\x001fHgsOõ6nCU|*Ç}ñl\x001cÐÓ\x000c±»#4iÑÛXn\x0002CJ2f\x0007BéÖ\x001cF<ª^îbBê³´a-6\x000e²ÝFÙÕ$ò \x001e \x000fª¶ã,</p><p>ª\x0019bù\x0008RxgýÆ{å$òàAïãÒòsõeUãz <Ë;87Ð{·²Ý\x000c×\x0011QÙ\x0006/äØ2\x0001Òåùa\x001aäÁWÞY¤SE9Gq8´Ìcg6zçqØ{¨ß{)Kîy(ÎYÜÅ©À\x0008òQî\x0002½ú½
UÄÔD+' Mj+qýÕÈ`Îâyê®ÉF~qÿæíÇß|ýéû×ïw>\ÙÀm .Ûä$¶%\x0008­Gó/\x001e<zúòæëWÔ³êó°ØÃ¢\x0012VfS}tc§¹ë©ós¬¶gµ:V\\x000b$^³Ü\x001d(ËÒ¥ªc`]\x000fë°A\x001eæÓå#\x0017/·>¾hÕ÷¬^ÇZ\x000e÷\x0016\x001a+WAi!\x0004¬\x0010s°¡
JÃÆæsKäãx{åÐ*$×¿ç`S\x000fÍÍ²\x00198§À\x0002ØæºÖï/§`OÁäâ¸¶È.ê£Añ\x0006\x0000-Zw'6î§5ö¼ÓmöîþøÓ»·¼ùêÓßî÷½[©EÌ\x0011FËíIw¶èÛ\x001aíÝO=ýòæ«Wx°ù®lÏ;îÙÖqo\x0016·\x0004\x0005u\x001af^z#Ë3¢Ì¢9ì\x0007ÑÚÖ*i=J\x0017)-É\x0015Ñ»>²j\x0012×õ¸NZ§Kêú-\x0013Ar{èÂ£ë{Z¯5nâ\x0008a1næ	 ÞÉ£\x0011®·¹Ä
=nPn4ê</p><p>Ì/ö¦=Á$\x0006ü[ñ×$nìq£v£\x0019\x0011«uQR`£\x0014Õ\x001dVó¸&qS´ÖÅÁºü \x0007!\x001enÝÜãfíNæuË\x0001Se¥Ð¬»>æk\x000e·»\x001f±§}Ó¼9·§²×¸SA¢ËHæ]o#:É;¨\x0004(ebi;Ü\x0016¯¼'·çdXN¤\x001dT\x0002´2\x0011QF^RÚ½æ$\x001fÂ¬_3Lò\x000e2\x0001J V~µ;fÍ/8­Þ£T\x0018\x0006¡\x0000­R¤Üµ\x001bcYÃkZ\x000ePV) 4çPÌ\x001b$ßÄ··õÊöIÞA)@+\x0015Ùr*m^ú®s·~#ã\x0016]ùÿx\x0007©\x0000­VPÛ|¯´çoÆ]?þNÂ\x000eB\x0001J¥ OlÜ`¥"2É,\x0001·Q =P R(\x0005®?ËQÜ®<4Ö»|NÂ\x000eG\x001fÔ}ÀñI-SU¬¬\x0004\x000bröÉë\x0017¼ãÙG«jÈ^Á\x001bIX§Ü>1îz\x0012å$ì j¨\x0014µ\x0013#5</p><p>ãD*çdÜõòÓIÜAÓP«iÖñµXáµ2Ý+ùÜÖîzrÉ$ï i¨Ô4j^aTy¦6wÒnd$NÂ\x000eZE£¢ø³\x0016m¶>fwP4T*\x001ay19ZZÛæÏx/!®W\x0004Mò\x000eZEsK'¶jß$u­¡Øw½:yw\x00105ÔÚ/véd\x0007U³jUK-\x0015ªüÞ¥ \x0019á\x0010ï lV}©×\x0012#¶\x000cvz\x0010û\x001eåÌì lV+l\x000e\x001b¯·©²~9­¨üqÖ/x'yÇk=­¶ñ$Ej|éÙæ|ýzéÅ$ì lV«lÅùJàPö\x001dOÊM\x0011ÅùFs\x0012ÛAÙ¬VÙ\x001c7ì,æmóÏ\x000b.ßm¥5Lâ\x000eÚfÕÚ\x0016[§dû\x0018róeGwÐ6«Õ6oÚU9Å\x000e­rÈ:{Ô^\x001b´ÍjµÍ·â\x0016ê¶Â®75×\x001b67HÓJ\x0005eËr\x0000\x001aj³ðf£]¯\x001b¤Â©¥ÂIè\x0010BjËÁËÅi9\x000c\x001däÍÜ \x0015N+\x0015Ô»C_0­P/Ë]õë¼T8­TxÉ\x0014É!µèIÛµ­ñ	H«\x0016ô\x001a|²¯ô÷\x0014º\x001deßA-V-|3<½ºóUJQäb£(`w\x000b§äÛ\x001bñ­A5Ðäí ËH7ÈSË\x0005Ê\x0000¿\x0010L\x001bA\x001cxÐQÈ
rá´rQ«}ñdß(÷\x000e\x001bµN¼ÃQÈiB!ËÑ8Ðm$ó ¼¸-0Çë\x0007½ðZ½N´)\x00179r\x0007åpÐfóXx­XdËÏ@ò&í\NwPv=\x0017r\x0012wÐ</p><p>¯Õ</p><p>)wÚk®UéVõÁ±¼Vx­V¤%1¯Ú÷ÔÀ¶XÇ\x001euîÇ\x0001­VÄ,Ã\x0010C-\x0002¨öm¾\x0017zgóVxµVØÛSè ý^dx\x0012\x000eGá\x000eRáµRë¯yOÍ½Ð</p><p>¯9*eÀ\x000fRáµRQÌË\x0007yÊkËÁËÉ
ºþ÷Tx­T$'·$Áªbe«]/Ç£
P\x0004­P¤(Np¹	[Ùc\x0015º\x000c\x001fÄ;hEPkt$,Öu­õh«9¦ù@\x0007ñ\x000eb\x0011´b
gp\x0016û:\x001alÃÕ°Aì»^)6É;EPE\x0006Ç#^w°\vÅ³Å£½C\x0018Ä"hÅ¢¬\x0007~\x0010¢\x000eÐÊ_Å¾ñ¨{¨0¦)Å"C\x001e</p><p>¡ÄìRâ\x001f}Ûoëµ5¼Z\x0004¥Zä\x0012ÛzÐ\x000c\x0010n¥Q©Äf\x0018\x000es\x000fX\x0004¥Xäq¡¥&¼z£<\x0015ãaÏaÐ Ô\x000c\x0000WëF¶HUf1ïúL9Þ8\EåµYqVrËG%\x0014Ò\x000f6Ê¥:u/9wP·¨T·l\x001c)ÞAæjåë\ó\x000e\x0007á\x000eâ\x0016â¶t\x000ecgfá4Ê\x0005e9¤õÚIÞAÜ¢RÜ2x.*Î¾Ä\x0011V¯ÜBQ]ÞA¼¸E­¸Y\x0019RìkxÊ\x0018M>å\x001br¾q\x0010·¨\x0014·ræáÆÙÇÔzGÉF»Þ&zw\x0010·¨\x0015·âså¯qÓ)Ù\x0019e»\x001dtñ\x0010Çäi­¸¡àÌG{° YfGe ÆAÝ¢VÝ¼9ÙW\x00124h^k³ïz#ÄIÞAÞ¢VÞ°çö!IvQn·¸QÃ?Ç\x0006yKÚW!Ì-EÒR:½mÙEÕ\x000c-`Z\x0010é\x00003×IïARl\x0013%m¶\x0005ìÎ\x001e\x001dgÎ¡Ñ¨©)÷AraBÛz)ØSÆäQ=Ç\x000eV]srÜ(\x0002lÇ9\x0010¾^ ÃwgUcAªÆ¾ºÿðñÝÛ/îß¿ÿÇß?Oë\x0000[V*5[¶-1¥$Ø¯×»~õàÅËgOo¾xð|³öY±gE\x0015kñmöVzyéObÚ¥j9Ð­JÇ\x001c¬ía­Ò°ÖK\I%-5¹Ä\x0016ØV1¶^X>GëzZ§4-e$sk+°<æÊ\x001a\x0007LíÖ\x001fcçh}Oëµ6pÇ>Ã]¸ÊM­\x0005ÞúÌÅ9ÔÐ£\x0006­aÍ©¿`æWc*$õaõ²d6ö´QiX\x0017n\x0003¶î5Ï¶RÔ®o5£M=mÒÚ\x0016x.\x000eu{ç6aÆf
ëé[s°¹ÍJÓxðÔ)µ¶¬Û&ÂëS§hû:±ÐêÄ¦mKÍ\x000fÙ´ ¦
Æçüz3\x0007;jVÄ"¶.à¤¹µ­ìjc\Û\x001cî \x000c dä%>\x000b­k\x001eì\x0018\x001dA\x0019@'
%Ê²}×ÃÄÒPþB¶Ùúõô\x001cî 
 ÕÜzKÃ´³'yðëíæp\x0007y\x0000>PG\x001cÉé,oëaþ´ÓÀ`Ð\x0007Ð</p><p>D·l\çd\x0006{1®a½^pvÐ\x0007Ð	3,K7S7¥Ú ®Õ\õvÚs¸BV"2È]\x000e=È×¨Åºr·çÍzÆË\x0014.\x000e\x0012:p¦¬\x0000Á-ÖEîZÖ\x000eá(ÚA#P©\x0011HÄ¼tsæì^kHõôÓ9Üñ¨£;ë\x0014ãfiTîIµ_$\x001bº°^#6G;(\x001a*\x0015
iøy5.=¯Øº\x0016É²r\x000fZ	 ¡VÐ¨ó"¯[\x000fÜdßBë\x001c×s]æh\x0007=C¥!Ý2Õ°<´UË:y\x000cô°I4G;È\x0019*å\x000ciÁB9KÔL\x0017R®ââú9ÚAÍP©fXN½\x001cÑ3¯úàÙ&\x000eò	¡VÎ"´Q!!s1[Y¸­<;¯÷IÃ\x001dä\x000crFÓX\x001fè\x0015(V\x001fæd®{òx\x000f³Y­eÓ\x000e\x0011Ô¼</p><p>\x0004Çõæ º\x001däÌjå,£ÜóÓ\x0015zMj°Kwzö¸ë¯îs¸Y­åÓiÓUãÆ6åæ¨µ0HUJ\x0004
æ\x0014¢%û/ïÜáka\x0008«bÇ&\x0011tëXi½«\x0005ï\x000e</p><p>mì \x0011V{ä¡éÀ½îêR5ÂÈ\x0005<è\x001e×\x000e"a"a!ñ'ûÈe\x0014Å¸ýæ;È¸FX¥F@Y\x000büú@Æå0\x0017tn(Æ=&\x0016³FX¥FXçåV,SÑ\x0007»1ÉãA7xnP\x0008§T\x0008öFÏØÜ\x0017\x0012¤\x000ey¿X8;HSJ
¾-¸ä£\x0013n0rëÓzé\x001cî \x0011N)\x0011@-ö\x0018\x0017²\x001cy¬Ií\x000cqÐFsÃÇ)<6&\x001eÔLÏ\\x001eHgõØ¬{ÐÚ\x001dßw´FS\x00119\È\x0012ÜPÿUõZÑ9ÚAÑVÑ¨5\x0019+\x001aéoÝiÁJRÏGí´AÑöÔCå\x0008l\i\x000eiË9¢­Üõá¸s´ 9­ eKÞ¸¼tÊÌ6\x001b\èãÏA+wP4§U´Ë±X¶åoÅ¢\x001dõÞç\x0006EsJE+*A	CÕº ñB2l'àúüÉ)\?hWj\x001a]\x0019v\x000c4.oÅ:I;æÔ\x000fæVÂ\x001bò´q\x000b\x0013ãJCµ@1ï!¸Fx¥F¸`H#\x0016Ü¬I-0Øº\x001bÑs´Dx¥D \x0015å³Ó
AªËz\x0016Eî\x001c\x0000?ø\x0005¯ô\x000b\x0018Z\Nî¯\x001c£äWøä9£a\x0005í>£</p><p>;	t3uV[psl¡îA÷xa\x0008Æ2\x0018£ë\x0005\x0008¸VØúVË\x001a`½v|vX¹A¹r-¥¬°[\x0000ijj½úº\x0000\x0007\x001dzÂ\x0012¢\x000c\x0017,­\v\x000b|ñb 9a#ç|\x000ewØhA¹Ñ¬\x000fô¶à:)¶´>Çæt\x000fzèÃNÊV¢1ºS \@T¦¤`"9&\x001aÃNÊæ\x\x0001Læ\x0011¥¥iÈ\x00079Ý8ì´¨ÜiÎ/\x0019Õ¸4[¹</p><p>\ÝDXÏÖ£\x001d6ZTn4ø\x0005°A¦\x0014ÅÖ0)âAYmqØhQ¹Ñ\x001c=\x000b.\x0006NÓ-ÆþCi£TbÒ-é®kt×ù£¥Þ\x00015ÞÍ\mYjò@\x0015ìzBÿä\x001bû95d55½Àýtîä5X¢\x0007³¥;\x0019÷SØWKíH«­\x0001Zø{½\x001eÖ{wïNî»1[7¹n*æ7ïï?í¹àÓï¢L¥µ`¤&\x0005Ö¿¼»ùæùW'´=¡&4­Ï²é$§I4\x0002ð\x0000D×#ºiÄ¢]édDá#R$\x000eö\x0000Dß#úiÄ@ lÅ(·\x0010ä</p><p>¬Èïõ¡G\x000cóVL·¦&\x000b;z2eDóm¹¶\x0006.îC=bE$eâ\x0016%ìX\x001b£4b)«rõ ³\x001b1õi~CÇÛÄÛ¥Ä®B\x0015bÅë?tî\x0011ó´\x0015½î;%¤"ÖÌå$\x001fÚ¬7"ÝØeÖÿÙnBå^3Z'\x0014h1\x0002ûE+)H°ÑAl7#\x000c0mÇä\x0016ÞQy4ç Y±âz\x0008²pð0ï\x0018i"©li/OÉ[Ô\x0005ÓÖÁ}ciÏ\x0008ÞJ?\x001dçÃ­,F9>ÃF^ÉnÄÁ1Â¼gÌÇa\x00163b{â\x0004®×Áïf\x001cÜ\x000eLû\x001d:\x00109ÖÀ\x0000rS}Ê\x001a\x0000\ÏÞÍ8ø\x001dv<h¼$b\x0014^WC×ÓlÇâw®v<88\x001ev<\x0000K¹Tµ£3&½a\x001d¯WA\x001c\x001c\x000fN;\x001e$×üæþ°ãI\x0014_N-Wok\x001cãÚéÀ¼Y\x0002\x001eÉxEZë£öv#\x000e-NG¶\x0005RtÐæ$:èä\x000e×õëÝ\x0003Çi\x0007\x000en¹­°Ë\x001fN0\x00006g\x0007ïc\x001c\x001c8N;pä</p><p>3£ÜÕÚì]3âõûÆi÷
\x0004ÒIa8¡*·Àvcª×nÆ!°ÅéÈÖ\x0014°`Ûæìû`P¯Ï</p><p>Ø8(\x000cÎ+÷Í\{QbFh6¼Z^ìàºí¼ëöm^ó§²1ãÚwÞ
¾qpvÞ-\x0006+ÄÈÃµ-Ý³</p><p>ãõv\x001cw:ÔSÖ¢Ô</p><p>ÒgA¼^¥í°\x0016íôZÄ"{IÌ¸­¨mz}ºÕ^F7,G7½\x001c\x0012ö°1ò\x001b¡\x000c\x001b\x0017w3\x000eËÑM/G´BÅz\x0014\x000c28¦úÊ!f½eÇnÆñrgz9"d)\x000b.¼í['yS1éúãª\x001d1T÷#W3\x001e(5Tª³Ô!ÛnóÖ[Å~\x001eõÿ§îýí:nóÁW9/0§ºÑÿ+WGô1E\x0017E*¤èJæ&u,1234ébê¹Êíï\x0011r75WãçÐäI¦±\x0016Ð»q´Ö>»±,Ú)W$Ær¾ÕÀF\x0003\x001fâý\x0005¸±-ÀýîÍ~ýöêû×¿¼ùå_?üú·£û´\x0004ôª©\x0011'µ]îa_0â»'¾½}zõýí\x000fO~øýóëÜãý-¸±mÁÕa®	Ñªfq?	M´ÇLI[</p><p>!í¦ç</p><p>Ü®ÇíàÆ"ÆºÓ\x001b7CÑ!NÖ\x0013nö+W</p><p>Ü¡Ç\x001d\x000eávÆW/K<\x0000\x000co¤÷eÿ\x0015K;õ¸Ó\x0011Üa¨Yp\x0017ÃÏY±På#3\x001bï\x0014¸s;\x001fÁíÊu\qç\x0018Úl"M¢\x0014öÓ,\x0005ìÒÃ.Ìíi:(/</p><p>\x001eÔ'Whûw8S \x0019me\x0004<\x0014\x0002\x0003ï¼Ê\x0019 õ÷\x0015ð\x0004\x001c/ç\x0001\x0017aÐ\x001en"E¢±\x0018½-uÚS\x0005 å3\x000b\x0000\x0014¸E\x0018´â o~K\x000c</p><p>\x0019<søNûSÆ</p><p>Ü^àöGì*åkÂY£+¬
â4Á)»\x0002x\x0014Àã\x0011à1²ð	®L£©úæLb\x000f\x0014\x0008ëTo.èÉÞ¡\x0010ïÄ3\x000bÆawEÃxZ\x0003ª³7\x0014î\x000cÄâÍºÎ\x0005G+ÄSÞTà\x0016\x0010DB3%ãs*'VÖð\x0001ý®w\x0005p\x0011QàHDq¨¾âé[\x001aú
%X>ßû\x001b</p><p>Ü"¢À¡ËÛ\x0017ØX$Í+_èË~\x001b\x0005n\x0010ÂÐÅ&eP³@Î\x0008kÚMÀë¿fp\x0011	áH$âØà¹&ãFl©ñ1\x0018&f 2Y8ÊºÐº\x001b¬mêhõ
R6ûÝ»</p><p>à"#¹,¤ÌÀks·>²¾æ-Î</p><p>Üyà\x0008ó8oPÿd
á¼éý4#ZC¸\x0018Rà\x001ew{ F~§Ä©  \x0001À}ÞæÌ\x0002¸ \x001fw| ñT®MÇ\3|ÄÃ~\x0019J\x0001\Þê\x000fÍÜ\x001b%ICìc9
Ïûó6</p><p>Ü|Ü\x0011ò\x0001×ö\x0012\x001aS\x0008··¬7`ãþÔ¶\x0002¸\x0008âîP\x0010¯'Þìs¦`\x001b\x001d\x0001Ïû\x0003Ñ</p><p>à"¨¸CAÅ\x0018¾@@i½¾DGô3õæãEPñGM\x0017°dk;\x000bÎ<M) â\x0004\x0015dyêÄr®q&ÍþK¾\x0002¸È°ü\x000c\x000bÅ@hÛ#q*¦øèS\x000bã\x00133\x0015/2\x0015$SÁNlÄ\nodñà¹=/O</p><p>ãþ~!Üs!ü§OWß½ÿôöÍ»«_ÿ«Gw\x001fß¼»~<õSd\x0014 ß¬QÜ·Ëæþ+È««ï¿zúäÙÕÍÕ£O=\x001bzÜp\x0004·ÏÔO«Vù)\x0004\x0012àO\x0011ö×*p»\x001e·;»pÉ)ZÖ\x001dÜ\x001c|>ó ?Û÷¸ý\x0011{Sq6ó\x0002s\x000cæL³Ã8îÐã\x000eGìë,WsC\x0013z)\x000fûJ</p><p>Ø±\x001d;\x0016\x0012NÔrP/\Íûc</p><p>Ø©X»fáNw½ãSr2*)õ\x0018Í<%¹Ç\x001bwbP-\x001c\x0007¹bÙÞgF&Æqw
Â±k\x0010V\x0001Ïú>2ª®\x001a®ÍÒµ'°+ðm\x000fÅïhJFq[*¥DØâõ?0\x0011¸öH \º7-½®eîbÔ5\x0002éq\x001fÇ-\x0002=\x0012Q<X*ræ\x0003xôíê\»Ã8páöoz¼¯\x0011aúöYÿÅ¯°û3Æ\x0003¸-LPð\x0015étÀxýá]ýÿù¯ÿþöîÃÏïÞ¼þxÉõÁe\x001e\x001f\x0010x®\x001fbæ{;Ëõ?Ü¾xVÿâêÛ\x0017=¹}ù0x×w\x0007Á'Ë×dÀr-Ý}xú8å²¯Ñ¨\x0002ï{ðþ xßC°|ÿTåÏ\x000cËhÀ\x001e|8\x0006¾\x001eyîA3!sXãNâ²þþ{</p><p>|êÁ§àq|À[^oí|{MçFæ4às\x000f>\x001f<6XÔ_ïûØyÅ¢à@íV©³qð¥\x0007_\x000eZ>gZùË©\x0005ÔÇÂ7¢¸_\x001eÒ?e1\x0008¾Ëbtè¹ÎT\x0005õ¬Mè\x000255¦\x001cç:ì©b\x0001ow6r¶^àjX®.åí\x0019\x0019
x\x0011*íÁX	(\x0005H¦÷'Y*^­²;\x0002|<</p><p>>ÐÂwÜPd\x0019;ßJó¹	*
x\x0011mìÁp³<~®,eã\x0010Ïó)¥ýwg
z\x0010\x001e\x000bG=6\x0002Ïg\x0018ÏmûõG¦¯Ù¹«Þ8x\x001dLÍ ·õ\x000f\x0006EÉ\x001d\x0007ËFSgzú5èËÂAÅ§\x0017Ò½Ã\x0011uê³°ì±Éú©	\x0002\x0008.ëV¹³§jFcÿ\x0001¸­24õÔ\x001b!c±f	­½Y\x001cCËìkø¤ª©k-­\x0005¥>¦\x0006Íùñ^Øüñïê\x0007ò/¹ÎùoÉÔÚkßü·õBG79G.ÿr'ñß\x001d?\x0005ß\x00088YËÀñ§´dmª\x0013Ô\x0003twï\x0000\x001dû\x0001_ü\x0000¥û^\x000e{1DOS*\x0019µY½g</p><p>#\x0012g\x0016R(?Â/÷>Â/\x0007³Ä
w¨n\x001d0ýF*å\x000føÓ½\x001fpÐÁpúÚl4\x0011</p><p>w÷Lºm{Ó#õ\x000fþá4yüâýÏïîþýÓ%¯|Æ\x0019T\x0016]Ý6á]qU¸àÖúö×(ÿîöêÅóÇÏnþñÕ÷=</p><p>=TÐBõÐ òÆ(sBznrèr¤®Gê¾j£ú\x001eªÿ\x001az¤á«6jì¡Æ¯Ù¨©G¾j£æ\x001ejVA¶\x0017eÜI6òtGLûCPK\x000fµè F~\x0012Ç\x000b\x0001[5</p><p>Wû\x0003G v\x0005+ÿæk6«\¥#«/eWAVVÇV_Ê®®¬¯¾]\x0005_Y\x001da})»</p><p>Æ²JÊÊk	8ã6dÇ\x001alÜªQ¡Sv¹\x001cª`,«¤¬L\x0012]\x000bVJ\\x0005ÖsÃÎc\x0015eu¤\x0015</p><p>µæ\\x0012ßÔ¬ç£x^¾âr¬´¬µR¤M\x0019·¸³$drÜe\x0014÷õ6°</p><p>Ö²:Ú</p><p>6·gÔ\x0006%}1\x001fù\x0008X7Å³@°\x0016èX«Bu49\x0013/!±'ø".øU°\x0016(YË´ÊqØj±bÍl×ób^cW,\x001dkÕã\x001aC;®5æøÕ*Æ³\x0002nc\x0015¬\x0005:ÖªgÃ@J¼ÄÐúÀa\x0000Sù\x0019X\x0005kµ¾]\x0005kµB&]Îê[Ýz»Uº\x001c« -ÐÑÖ²« -PÒV^GÖrÆÖêÌf%&\x0008å¬*ÔåP\x0005kµ*Tª#æ\x0008¼ÁÒzÏ\x000bùÌÆ\x0008VÁZ f-(
+µ±#B»:ÁZNÍZ2nA2+w¬å³rc\x0015¬åt¬\x0015Z[w®EË\x000f¬÷|\÷¥Y </p><p>Òr:ÒB¨·\x0004h*½Þ³ÌFÚß±9UV\x0006¤®I©'ûE¢yÅêrÓLs\\x0005i9\x001diaÀD°õ¤ªgñq-Î -§$­/dWAZNGZ±Ðd.§y½zå;ÁÔ!¬´´¾]\x0005\x00138uÙ-QÈòé«\x0018Ü´\x0014Ò¾üË\x0008T/Àë \x0019îr_öÆ³D¤k¯½s®Û^W¯¬d¥\x0013Áz\x0012µ!5ÒÊS®Z^>f(C¼lª*ü\x0008]\x0000'\x0003éÌ´Æ\x0008V\x0011\x0005¼2</p><p>DjÍ\\x0006\x001d\x001cEÐòÁxVQðr¬"\x001fôÊÚ{¤\x001eØÅ³\s­\x000céë\x001aÀ\x001ak\x0005eAûËØ5\x0008×</p><p>J×úÌXk\x0000¸7]Yc@
Ø7ÿñúÝúÊýø×¿½ûõo\x001fîÞ"ôÇw*¾»R,¿Ó/¢r+pÃÝf¨E¿\x0019\x0014nþxûl}ì~|û¬þÑSü\x0019o^ÕÿûÃ?\x0002ú\x001f\x00013~\x0004]È±ù5V ¬#ý´=qè'¸þ'¸\x0019?!áíl%\x0005nÆîâóJ¾~ï?ü#|ý¯DäË0\x0007bê?Á\x001aµq{\x001bö¡\x001f\x0011ú\x001f\x0011fü¶ÜMÛ¾fíö\x0006C?"ö?"Îù\x0011x«;þ\x0011Ý:Àf	øÐHýH3~Dn±É9jã5\x0017ËY³½BùÐoÈýoÈ3~§Ðäs\x0013Æ0mßÕRý\x001bJÿ\x001bÊß`]u\x0006ÇÍhÖ°:¶Ùs;ò#ºAT¿pÌp	ÞUöÌÁ)´\x0015@ÛR\x001f~`:{êê·°¸v'</p><p>8ûDb®³ÛÓÀ~à:{ìV,¥Q"ï®³`Úzí%È~ ;;í|¢\x000eAo\x000b«JÛ&\x0007·»L\x000fý\x0006Áuv\x0012ÙÑ°\x0001ÎõÓ|É¼£Íì(­\x001eú\x0015ìì\x000c¶k\x001b¥fâ×ë[ì\x0015x¯þ+\x0004ÛÙ\x0019tW±&¨\x000b©­ò¼\x0016Ê¸íwC¿BðAxõ[\x0014ríÌylý\x0011ü)vÞq\x000eý\x0008Axv\x0006ã\x0001·_\x0017ç\x0012EXËgçS\x0005\x0008Â\x0019Xé<årú\x00144V_?Åö³ê¡_!¯v3\x0008¯b¥E.·aoËj:Ùíºå¡_!¸\x0002fpE«hVß6<{\o¦¼\x001b</p><p>¶ëY~`\x000bÁ\x0016Ùø¢Æ»(dMA¹ÑÙ¿B°\x0005Ì`\x000b\HC~,\x000byµª}å¼Ïp¢\x0004[À\x000c¶(Ü\\x0000o\x0016´úÇ\x0000O¹ÄÏ\x0010£\x0004[À\x000c¶çLqI;3wL	¢ Ýä_áD¤u3"mò-Ò"]PUµÞ²/¶\x0005\x000eý</p><p>Q	tÇKÞ¢\x0016"+SdNhÁr+V½üM÷n'øÂMà\x000b\x000bM\x001cÄù¦
ÜSX¿Å¶ìÐ¡_!«\x0013nH¶¦±<Ãælón\x0000þ\x0016v[ÎùÐ¯\x0010¬çf°\x001eN~hÅ)\x0019\x0004S\x001a_L¿"9Azn\x0002éáòÈÊ\x001b7\x0000x²¢ùW$'HÏM ='äÜPx+.R:\x001f¨0ô =7ôp
(¹-;0ÁyÖâØÑ=ô+\x0004é¹	¤gÁ5·°­L\x000e>6ý¢í	áC¿BÜÜ;\x0012(\x001a¬y9¯otÜ\x000cÓ|Îó¹ý\x0004æ®ÄÌY­\x0012\x0005÷pìI\\x001fú\x0015¹ý\x000cææÕ\x0016¸Ý=\x000fÓÎ¾ÔC¿@°¶ÁÚ®\_ûHkE 6iw¿-èuè7\x0008Îö38»º5-G¯\x0016ZU\x000eóïx^>áMàl\x001bygÔ²ÃÖLâS\x000bÉÖÌO¼àl?³QxÜ:xÞq\x0000m\x000fßÞMxèG\x0008Êö3(\x001b\x001b_hái+= f°<B_æÿ</p><p>AÙ~\x0006e;Cê¼Å:w\x001d)eõéa>ÙyAÙ~\x0006e×SÄ¦²áé\x001fÈmÑTÿ\x0016é\x0005eû\x0019z|;s³\x0007ð¨¾==\x001f\x000f²Ã\x000cÊnCc\x0005+9tÙÂWÒÎã¡_!(;Ì ìØVåâ\x00131_ã\x0003e·çµ\x000fý</p><p>AÛa\x0006mGh¯· ÔJ\x0006%7¥­í¶§C¿B\x0010wAÜ<áIö©þ¦x3?ý\x0008¸Ã\x000câÆGmR\±­æ\x000c'Q	¶/\x001fú\x0015²ùf\x0006s6³T 2]8ß¦ýü\x0016¢ ¨;Ì n\x001cc£Æp,|\x0002Qàí~ó; î0¸Á\x001aÊ+¨Éº9´áÜù¾-;Ì îÚ84Nðzöm`!¥m¹úC¿B\x0010w@Ü(ùJÝÐõ®M\x001b¤\âL0ù
8Q\x0010w@Ü`O®í#OK \x0004?«ëåé"</p><p>â\x0013\x001bN4\x001eQâ(ËiUêüO!x;Nàm°¤Mº\x000c-0ËG7¿70</p><p>Ò\x0013H»þ\x000f\x0002sv'LÃ\x0010æ§(H;N m¬Åd?¿³OÔ£Å=¿s%</p><p>Ò\x0013HÛù@}¿9\x0006n¦Ëô+Ügè6²ev\x0002iã3j¢eð«Âür¢\x0002Ë&Í~ ¼8ðP\x0006R½\x001e\x0011W\x0004Ã\x0013¿>Ï£O+Ò\x0004®p¦~\x0000Z\x0014ï\x000c/\x000fñ­öáãöÊ¡_!Âl\x0010f]M¡xÝ½i/ª¾ð\x001b½÷Û\x0011~QiBÂf´DÎ\x001d¹o6\x0004>P.ÌO>p4Á-p¹\x0015)¹aß,ÀFÏúù`ÝtºÈÂ-ò\x0004·ð.âlÑò+ª[JB\x000cÍÚù¾íl¯nJ½\x0006ø''^r¸4¡xÚßDnd\x000eóû\x0004S8i.ç*üÃþ\x001e\x0006´Z)Rý2Â×²®ùßucpTî3¤µ\x0016î,\x000b3NÖ2çZhÇYsMûhKú\x000cáIÄrÃ»ã	I½`\x0018ºkTÇ¤ÄlÊÄü¸\x000b÷<\x0004{¯·mL	£B\x0004¬ªn@Êü\x0011Ãú=~¹÷=ûH®¬\x0018¹¢^XYmþ¹2á¾IÁ7ò{\x000f3özÓ,mdúo©ëîÞá:î#¸ßÄ¬WÙX2kGùÂ»ÃüÎ:¥ëO÷\x000e×q/Ä¯Ç9ûÈ\x001d_¸$ý³xÉ÷~È\x0013®Q¾7\x0000p°\x000fÜô\x0015üü[ý!?Ýû!?Mø"ü\x0012SYö[¯_uä\x0003Ìì°u÷ç»Ý2ßýýÛ»\x001faô·ÿó_ÿ}ûóÛ7\x001f/qï\x0014\x0003iþÔØ</p><p>ôF\x00065BÑ¬OÛúDß?½y´\x000c¤?½º}üôÉË\x000b\x0000C\x000f\x0018Ô=oÞ(©\x0004üË\x0005°£ö4Ìv7ÉN\x0001ØõÞÂm[ýOÑ\x0008ZØ±óæ\x0005U\x0001Ø÷ý\x0011\x000b¯\x001a¥Þ¢IÊ\x001a°¿-\x001c7\x0014C\x000f8\x001c±0-ñÉ!P#/Z(Êçm÷S\x0000=à¨·°ãæÄÊ¤f</p><p>°\x0011`¿Ýb©\x0000zÀéýÚkky¢Z\x0016lg_¶\x001a\x0014s\x000f8\x001f±0$d0§(\x0011\x0018ð¶\x000c¯\x0002oéñ\x0016½
uµÕKÕ5y\x001c\x0013!w35\x0019Û
K»uXZkßÂÃÅ\x0019\x00125%T\x001at|\x0011û\x001cÄ6ì\x0001Þ\x0008Ì\x001bÙeÚ\O\x0004wû×\c3U \x0016aØ\x001eÃ©E`¯Éç¼iQÍnp\x0014ET³\x0007ÂZ>\x0001Î-¬ag\x0007!N³\x0010(a\x000f	 \x0011Ô\x0011.pìw~³&£\x0008\x0013²6¶dlø\x0007JØØØDg¹\x001ek</p><p>n£ÅÆ¸æ`t×\x0017G«r´zP®±ÎPã\x0019x··\x0008«0ÿõ\x001eæ¿ª1\x001b¤ºûyí<\x001f>\x001eÖÝßêãLÌ¼úáÃE[\x001cJ¸³¢N6Ü¾`Z^\x000cn{\x0005&}yõÃó\x000bÜý­>Îôiü\x0000ÔRxP7xÏãë¦éæÀó0T×Cu:«:®~D\x0017ùíØ8\x0012\x0018Ìõ</p><p>{6ñ¹\x0018ªï¡z\x0005ToLÛû\x001bBâ~\x0003©«+Ý\x001eÊ\x001b\x001az¨AgU.\x0018\x001cËpáµbEZ¶Û;Æ\x001eiÔ\x00195òÔi(ßHMa)\x0018Øy\x001bz¨é¨Që©\x0005¸wTÙn\x001d{¨YëUa}</p><p>`¸^b¨<áTìb¤¥GZ´F¥Mà1ù\x000e)*w>1¿\x0014i·ÕÇ\x0019\x000f\x001cUhÊh\x0013J¤¯J\x0014,</p><p>\x0002q»g{\x0018«ä*%Y\x0001'ã1Y\x0014È^ÍÊ×3g§\x001c\x0000+\x0008À*\x0019\x00008\x0002ÔënÓå:íîëa¨\x0000¬\x0001 É\x0015àaµ¼|:ÎªUãÙ:ÈÅXE°²ÊheiIJI86ëe\x0008pa{\x0018ª\x0008VV\x0013­¼q¾ÔvÒ[\x0017YÓ# ÂUÆ+oýY\x0001®â	k<_¨¹\x0014+\x0005ºåÚ¤LÌ-·².5Ç\x0005W WõöBõ¯z\x0001çáO\x0003@ÉµKÛ\x001b\x0007±ÊäZ]/¢%LY94µ±DS/õ\x0013\x0005@\x0004WÐ\x0005WÏ«S÷ÜÓX!\x0002;ËS¡à</p><p>ºà\x0000éÝ\x0001%3#«\x000bñ\x0011ðsR\x0001\x0010é5èòkçø²]o«Ôj\x0002¥$æ¬¼Ý\x00137U$Ø Ë°=÷z/DàÖ¸e»noË\x001aÆ*H\x000bt¤sdWÜGZ©ÀúÁ¨9\x0005«`-Ð±VäÁj×Ó2LccaçD,AZ #­\x001a±ø\x0008ÔÕJ\x0017ô ]¯ØÛê\x001f£X -§!­/uuq\x0008\x0008ÀóÃcb\x0012´\x001c+n72WÄVó¥*Ô×6\x0007\x0010ÛØjX(\x001fK\x0016öÛ®½&y¹ß vJÈ®\x0014`\x0006Ãf8Ê·\x0012¿Ü¸X!6ñþkní÷wïß]UÐo>¾ùp}kÎÊWDSq³VPÓ°Ø\x0011e#éùï?»ª¸¼|òâa¼Ðã\x00055ÞÒf©}àK\x0002Ä6úê·5l5]\x000fØi\x0001¥í¥ï«F26°mû\x0014K<'î?\x0004Ø÷½\x0016°
×Ô§-;\x001c\x0000/¯åì.è!¼¡Ç\x001bxMñ¨*ÍC¼ü­¤6ôyv7Í\x0010àØ\x0003ê\x0013Qx\x001flZ\x0006\x0015V\x00036TxvÁæ\x0010ÞÜãÍ\x0007N°=-°õ|\x0019ï¶\x0006néá\x0016õù¶\x0010²"\x0007²/\x0017½RpÛ\x001d\x0005àîé<B¿y{ÔÀ¡­_÷mê¦¦m;ì4À3Ô¤a=o_ÆË\x0004õ\x0016³ÏÛSÖ\x001a¼3¬4_[)rA¡\x0001\x000eÁ\x0006X`«ÁÆµñi\x001cd'Ù8ØõÓ"\x0015\x0011ÍêCÃ\x0019ïu&4ð:n°-¦¹yEL³ê V\x000f\x00025FlÇ&!\x0010Ï²
Vf%> ¢\x0004è£D\x001bß)¸\x0017"ß\x00120ÍÆ l\x000cj\x001bcÂN=°Á^\x0017b\x000eGÍ\x001f5PLK}°±SÛ¸\x001e^jÒ\x000fv\x0011]^mÌÚOp~sØE­±÷\x001eÍk&ß"ÛÇ«\x0017ï?ý\ÿ×\x001fß_vABµÕLo¼)·QfÞ×\x0001¶U
WÈ/¯^<õ¸þ¯?></p>
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
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

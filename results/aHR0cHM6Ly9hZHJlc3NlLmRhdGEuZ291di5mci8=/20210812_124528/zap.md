
# ZAP Scanning Report

Generated on Thu, 12 Aug 2021 12:39:05


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun
Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T
T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=§õ-Ö&&óÇÇÛïÿöû?\ýrûÛ?\x001e¯1É\x0004l\x001ek/Ó*1\x001a\x0017s_`Æà[\x001a¬«\x0010BLM§ïÎÿ
WI\}{zry¹#<IL+\x0001òÕ§éÕ.\x0015kZ\x0015ÐËjCJ#kÀ8hbMu\x001eÈÚ'6bM\x001b\x001fzY½ÄJÕ\x000e-)\x0003«K\x0019g`
É\x0005Ø\x0015\x000cVÓÏ\x001aBrWU\x000eCÈ\x0007Ö´) ´\x001fb#V¸ëv\x0005«JÕ3Àª½H\x0003«O	X]Ú³\x0011+Ü}×ÍAX\x0017\x0018¡@V\x001cC¬Âoù¶Àªòýç\x001d§t®XÚ5eîÔê-o+$±ÿTqz©O¤Âó
PÂ²\x00140[¾,Þ%Ò}\x0005ìá°\x0010®\x0000è}lC\x001c®@ò±\x00016y\x0007\x001b±¸+DÖÿSñ*Sé	\x0002³êÿ2?w×_FªöÃÝ5üSÏwT^²Ua«gbÞà|h`Eë Ù\x0008Nãèúpvt\x000e¬g3&\x0015ëNÕö°b Y\x0005NÃ\x0018Xu
Y\x0002+ÄlÄºSµ]çêÒ°m`\x0005M\x001d\x0007Ã¹JI¬8òv;Öªí:WRò>rAß;±¦ì\x001e°Z)7dÝ©Ú®s¥ÁÀ
W7\x0012«Lñ\x0017`u³Â«u§j»X-0C\x0002Uå;ÀçêÕ	ÓÊºSµ]¬ÞÖp®Xe~[.ex7bß\x001dúYE$3\x0016\­ÉóÄªù\£ßug\x0018t±´r\x0011ïÀ\x0010ÝL¬ÏÕÛ9Ã µ4\x000cº`iP\x0001À\x001a\x0005\x0008ü¸Â¬âj-,NXÃ·@a¦`-ß-_\x0017\x0006.ä
±%dj7\x0004X?ÌJ°`Á¾5[dÆìºj:_Y$é¥\x000cS¤«²¤Ýô©\x001f®Ñ6¸îÆÕòÐ¤pq,O¸­õ³ÞB;îûãïÙùñós¼{(ì£ûÏ·71¤\x0006ÿõ\x001fÿyñËíR³Ö\x0005j\x0011ò\x0001÷^¤\x000b¡b2\x0015áÿM0À`\x0016\x0006\x001d\x001c\|{:mÛ\x0016ÜIÿ®ä&Eº|ÀB[¸5E\x0012¢bÒ7ëæNºx\x001d·õ1åÛF,ã\x001c¸µcnc6çNzy%·s©rÝ\x0007\x001c$cSäFËT\x0013q¼úæÜIG¯=oÆÂÃy;6à¼ÓÊyà¶rÊ´ìåÆ¦:¹úaþw\x001cx+ßftN2e\x0008N\x000e26â¡L4;ÛÐÒÿõïwÅ\x001d?»\x0019"å\x0007¿ýï77?§ªá×¥\x0002[c(ôNY9Å(l¤Ø´\x0014Äg'CÜüàèàÍÉå»Ë\x0005°XöõÓz
õ8å¨¢\x0019h\x001d¹KAJ½!-Öã_Ý´\x0018<M´\x0018\x001eÖh\x0001­¶t¶ W§LºÅ´ÿsu\x0011Ú\x0003hàÍ
£\x0019¼\x0017À\x0019¤PFÐ©zÚb³sApgÇÈ6r\x000f$9
ô\x001a"¤±×@\x0018f¾û\x0002Â¿ÞJ÷']¨ºon\x001e¿\x000cy²7\x000f·_ñ^>Ü.üêØ
¯)ü`Üaº¢Ô\x001cÆ8Ex?ê7'ïÄÙÓø?//N\x0017 ³ôûgþËç[ygGQ>\x0000=~¾{xZ;x\x000c]Ö Sy\x001aÕ 8nÔa\x000cÇÎ.®0î"f4>~`\x0014*5ÇÆ¨§\x0004é´\x0010îâd­Vq_H¡½Ð\x001f\x000f³öz\x000bã.æÔÈ
¥CA¬\x0007ß×`é$2Z¡ÑÅÍ\x0018w±¦FF`ÀÂ
d3K5Åðr¢ /Cñ7bÜÅ\x0019Õ¿\x0007Ä0L¬\x001e\x0010bD·Õ{Ió:þhÊ:¦\x000f\x000eîLH¤\x0011WÜ¤KiÀd¥K©ýªÃüÉýõoÿ\±±wsðííã×aQÄ\x0012ää\x0016|tE3¢ÁØz*Î<6öN\x000e¾=½ü8¹:¢BORi%zÄäaX7éÓ`%¡\x0007-¦Ö
tVTëØ\x0015ö0ùí&ý
lv´\x00190b­êUÕÎþãí³.nÌ»ëÏ¹çäç»Û¯K#$X¯,)B\x0002\x000f2§T)\x0019)#ëÃ\x00196@\x000f}='ïÎN?NH~þþ÷=\x0015ï¯ÿ\x000e¶ÖÓÓRsKáÖù\x0014~²Ö\x001e\x000e1\x0006¡b$@ÙYÑ6×û£ÿ\x0001&×ÕÕÕõ£\x0012e#´ùá
üA1üñîúàÝõãÒ\x0003ÖJY¿?L\x0001³H\x001bC\x0014ÓáÝ\x0012wG3ñ'ÆU%®êÅcMÎWa¦â}\x0010´G;ø\x0008sñÈ\x0016^]òê^^oèB¨`¸Ö\x0006§èÒñ
1\x0017nÁ5%®éÅu&í\x000f\x0005^ìMÅ\x0016àPQ@\x000ca.BÝÂ\x001bJÞÐ}¼\x000eíÄ\x0017Ü$\x0005«>P³ªo9.õaóc\x0013½¼Apí\x0015\x0010¬&^g\x0019XÍåVZ«ç&»ß[ðì7(c)B=d\x0006E7éã´\x0002W\x0017XvßàH\x000b2\x0011Xä\x0013¶ìG'7ºÁTÓÊÀ¶\x0013\x0018ËÓ£ÅTÞ¤ùÃl\x0002«×U¼®\x0017XôäÔp9\x0003v\x001c&nu#|\x0005ì;­¤å\x0005(Ó<Ö:\x000f&\x0004éE¡g\x001d¢\x0006àJ¦É^¡æ±,0nÈQÂ¡Â¡Ø\x001b±\x0011p¬cï	+µFä\x0012\x0007\x001c\x0003 XËÍ»sËU%U¯\x0018ö¸+9EÅp3\x0008\x0005Æàâò	Ã-Þ\x0008¸2ÒT¯ÃãÒ\x0001k¡YÍá~:`i7²zTm¥õª
/ó°Æã\x0002ÃÁÇãz\x0007Ì§lÄ[i
Õ«5¼©E\x000exA
Ë$­LÃR\x0000ØLf5[+­¡zµu\x0012\x0010 ò\x0006m¸\x00111ò\x0000ÿ#àJm¨^µá±¼,\x001d°·Xl\x000eØºì\x001aÍF÷\x001ax+­¡ºµFÐlY\x0006Á!¦\x0004;F6nu+­¡ºµR\x0014ð\x0016\x0007ÉÑ\x0014=Ê¹\x000c	Ui
Õ­5b¶ÝÑíÐ2­¯°­n\x0000ÖÖÐÝZC\x0019~s¸\x0005)U\x001d*Ö\x0019j>ÊÖ@[©\x000cÝ«2
Xh6\x001coØH\x0005\x000fT{*Ål=g\x000bp¥3t·ÎÀùl	\x0018×"IºÀÔè\x000f\x0007\x001cfkwZk×¾×·wØ­qÔLL"ÂHÅVÚÊÓÓÝZNy*ñõ8×SSäU\x0019\x0016\x0011Qnu+¥¡»\x0015Tç\x000bÄ\x0011M¶\x0001Ø±\x00106z³\x0013®°î\x0016Â«u°\x001ak»\x0006`Ïårf#OÃT\x0012ÍtK4GÍÊ\x0016¸\x000f¸Á\x00086Ñot¾¦\x0012j¦[¨¡ÎH\x0017bØ8ÎÕgì\x0018ùD©$é\x0010^d×\x0013ÛªéÁ@
AQF·Õ¨ÌJÓkVÊÍF\x0004Ä$ÒB`	±U¸ÒTVéµÒÐUvdVj\x000f\x0018ë\x0012ïvÀ0Ý\x0002âÿÝ«¬4Ók¥y[0¥¡9\x0018\x0011X+\x001b±Î°°½"Â£f#`?Ì3O®§¶l\x0007oeVÚêm÷	c/&Õ,aLa2Ü#Ýak·qå, WÀø¿÷\x001a\x0012qX¬ê±ªïU9Lñn\x0015³Ìíø»¸e±$¢1t)}\x000e] <Â¹\x0001)\x0012¨Ö>>\x001c$]åæð\x000fÜÜëÇÅU\x001a+©\x000eNrªKÂK/ÏGóZ.æÃÑåL1dfU%«êc\x0015já´La\x0019©ì\x001eß^ys\x000bQuª;U¥±\x001càeøaSLB¥ÈG³}\x0013VS²ÎcØ3°\x001aMéC\x0019¡sÅjMXmÉj;Ïæ
\x0003«u8Æ'«§s
q\x001bTW¢º.TåCEÙ\x0008\x0007LýM¤í|_ÎéKNßùùi©\x0011\x001c©\x001c/¤#M\x001b¬áHíkaêe¬9¹¤è<TEçxª\x0001½ êÇ³ÁÐ±ÒØäÕ°¸}ò
\^:Y\x001bäPÊ2)åßæ¶ÊJ\x0008È>) £&£Ü:¯¸Û\x0015sC	\x0016ì²M®¬¬ì{[pÔ0f\x001d,G°êæ<X	ÜYUk­¾k Á \x0018Ä«5XH®¬ÓÔéèu\x0010\YUÝ\x0002Õw\x000bÔ¤\x000bÀ\x001e\x0014Aàê$ãÅ+»9 ª[ ºn¼
`Û¥Æ6c\x001dÉX\x001cò·	l%eUÅJäDZ\x001fDnË¤Fbï¬Ü5T¬¡ï`y¿
<$ÌP$Áe¸@\x0007ìÚùêÞÅ°±}\x0007«pù 
¢§b"}U$
^
×,cÕúÒ]êKõOIw«À!£ÕÒÜv¶õ}9lå\x0019è>×@FÃºÖéHQ\x0004Ð\x0008:`·9ÙJÈê.!\x000bv\x0001×ûÚa$^:YaIn	\x0011_	Ñ,d­}>ç@\x0006É¢À!¶%íEm\x0012Þ¼\x001a!_\x0008[i\x0004Ý¥\x0011s<]ÄÂµ¢R'	ÿÇÓu1¼Vµ\x0010¶ò\x000et{+ûR¶Ïb\x0002\x0005­CP
¯ä\x0017²VÚK÷i/\x001cw¼YÓ\x0011Sº`]4¯Å7\x0016ÂVÚK÷i/\x0011-93F\x000e»\x0007\x001bF°¦ÕêµØ¬öÒ}ÚËâ"L\x000e\x0016wå¤\x0002éÀ3§\ó=>a+í¥û´\x0017NêHÑ\x0016§;Y`e`kv\x000cÆbVSi/Ó§½LäÜ©bðÃñ`½#OÑ½V\±\x0010µÒ]¦Kw©ÓþVãðdÀ8\x000e\x0013àZMX+u`ºÔÂ¡\x000c\x0002Ð\x000c:]\x0001£¥ekËmbsJÂ.	«"83>±ÂÍ%Vm³\x0001³Ñu­\x0004¬é\x0013°Ø2¸28\x000e\x0017\x001fÙp[Yf¹`¶Ñ²¦¯¦K¾øti\x0016=\x001a¬¸À%ï\x0000mX+ùjúä+jÄ@0\)\x001cz¯ÕÃ/µÌ²}2\x000bwý_êÞ.Y¯#·\x0012
'à\x0013	$ò/úè*:X\x0012M¾O\x0015Äë¢¯Jª¦HGÛOßú±=Gr\x0013;ü6\x000eýíÜYªvW[<R©×ÆÉÄ\x0002ÀB{\x001c¥\x000c$Ã2ÑÉ°LLÅÏÁjbØ0\x0016Ãú \x000bp¸ê\x0012D\x0015Â\x0012\x0011¤´÷{\x0010¬ñZaÌkU0ÒÝ\x001a zX×*\x0005\x0010äÉ§Õ§$´Á\x0004±a,åZFë¼$N¾snÕ\x0001¤âX+Ø\x0012÷­±«<\x0006^8/5\x00185¢Õ²~¯\x000f÷ XãdÃõ\x0000môR\x0004\x0011ê©7W&7býñS`\x001cW\x0018s\\Ëø%÷£Ê5QOßÔz>\x000c6\x001ag\x0010Ç\x0001V^, § \x0006GN\x0001Ì©tGã\x000câ 3ðãìåÈÞ¤=ÁIGRb)`Íýc÷+fÙÊ\x0019­gY%£ÅÒ3Ú)ql4qA\x001c\x000bÕ¼-âæ
E±åQæb	aJh\x0018Íõc×\x000brá]¼\x000c6\x0016\x0019ò¬\x0006Ë\x0015ó¦
éq¨&ëCY\x0017Fîè\x0011»òþv¹
è	ðsÂ­d"4\x0016Á@(Z'¨\x001eJä]ëi\x0015©\x0018Ó÷dò®4wÒXÅ,½Å¤ó(î÷v\x001d\x0004k\l\x001as±5¯\x0012ÑTØùË\x001abÙIÉw2.6¹X^ûÛ¢\x0002*<÷ÒAµA¢î¼×Às\x0010¬·ÒX¼å\x0008EÝX\x0012¯u¸\x001aÂè<\x0007¬á4Æ\x0007Á(Â\x0010×ça9'\x0013Ã9¥ãdÂ­4\x0014n±¼Ôä)ð+m\x0003ë´V\x0010kø=ÇsÙÆ1ò¢zî²ôÑÖß´®WËî5É\x001d\x0004k(!Q\x0002\x0011ÈÜ\x0005åJº®ÑWÌIÁ\x0002M9²Ù¸Ù<æfk\x0018¨ùLõ\x0000\x000fÍËFòY³Ú9/3Ù8®<æ¸j\x0004 Sz5EHò2SsÐ,^6Ý×:<\x0007Ö8®<ä¸ \x0007/Ã\x000bÄ­ß¾ÉÜä(A7\x0007S°\x001a¿Çü\x0016ïÂ\x0013Â²úi1,xÍ\x0010ÈÍ1¬q\yÌqeÉÕ°1ó\x001a°Å°¨µ
Êe\x000eXã¸òãÂ\x001d.u¿Hî%ú\x001cqM	»³	»óPØÍÂéÕR
h\x0008er-qð5\x0003¬ñ²yÌËò0Ó6«9
Í:\x001c\x001a Ná¯b"ï2\x0014yCªü\x0015Å²´èÀ³eùæeyâf\x0006XC	e\x0012*Z\x0013«icùÍÅ² Ymsú ¼ËPä
<rÕäãXL»\x001arÜ(
À\x001a\x0002+c\x0004Æ{°\x0014µÆµtø7ËÒz\1\x0004VÆ\x0008§ïY\\x001eh¢\Ö3Ks°\x001a\x0002+c\x0004\x0006 Ë\x0015(úÔ\x001e=\x001czÌÑoª¾\x001fÇjø«ñW,N)÷\x0006G\x0011\x0013ôIíê§8Ùbè«Ñ\x00178¡ÜjW\x0010\x0001^¾æÕ°{\x0003Àíéç?\x000eY¶æíù|nñVHÒ
\x0013÷tÁ\x000e\x0002õ\x0016è\x001f`ý]qZÑ%yûä¶¸ÔNÉ½ÀöÉó\x001fÇRp'ý¼ÄÎN\x001b¨¡l¼/p|\x000em²hÇ¬Ã"èÕ.Yã\x0016@K1ns×Îq´Å¢\x001dbj0$]²\x0014²öDqj\x0007ß9<\x0016ì\x000f\x000cE\x0006Pj\x0018##o\x0007A\x001bPk\x0006Û{a£µî`¬i7Øww¡ëóö¢S\x0018\x000cÀú\x0004\x0018ò	ÀÕã,¶åy\x0014zÖ;C2;\x0003øh\x001eaÌ¶úc8VÛ&\x0015WiO^â Zk[\x001c³-ÏÿïKQõ{;å¦\x0019Y\x0018 õ·8äo\x0007,¢]ð6iýæ4£mF±nt9´+V´|2]IwNS\x0004àj®Rà®ç*Ïuyëshýç(¦"¥ú\x0014¹\x000e>eàã÷ÿëã\x000fm¢®·M~8Òà\x0017µi.øÒ\x001a\x0003»°Ö7éæ´Êà'ÆaK×ðHÒ@y3ÂÒëÙhç¼,z\x0014;aFT_\x0002fQßs*¾\x0017\x0003Mzur1'7
\x0019¸uJ\x001e¸ïGJwÂÒÑjócÄ\x0019F\x0011³ÊlÔö$\x001dÈv¡èc4KBM9ÌåÃ\\x000fs\¾[Zí>Ðþ\x0002Q¯ä]açÓÍÿÛ¸à5¸i5·Ü
÷Ag2©o'ò^ãßß?\x0002Í!ñ\x0018f\\x0016OJ,ä=¿¬J\x000c¯pN\x0003@µõ'\x001e¶²A\x0008\çÍ2ù¬\x0013.æÜÂø{£î\x0019k\x0002÷ ¥iO\x001aprÈ!p\x0012wS|\x000câ(dâî»æ8r
¡ÈÓ\x001aé\x000bë}EûéÒ'\x0002£Þî×çt3ÃÚÐÃ1RÖÚ_(5vÆ¦Üg\x000cSSüËá\x0013R	Ã¤ât\x0019,U"ä\x0005]Ëy.Ð{òü\x0014¯>!4J*ö©8É¨´}*s4>êF@9ÍO@öÒ\x0007'É9òIT7jg(¥hNý\x0007õIÃÅ¢¯±yÎû\x000b|Â(0L)Ë2îÖ\x0016ÍZ²\x001bW7IÄQæÌüûOü³\x001föÏ!gy1»)ÖÓv¸IIÊ§ÕhVÅmýÍÕ\x0011:\x001dýf·'I¿ØZRc\x0000+±ÃAÖßþëßÿãÔF\x0017d%£& {c½}2TÂN¯üÞ*\x0016×hq\x0014-è\x001eé3¬2d\x0015¬iìfPt\x0018¬_õ£`}P}W6-Æ\x0006IIkii.\x001c\x0004§¦õ²>³\x001e\x0004])\x001fx¯ß\x000c´a6¢eC±-éèo\x000e¾\x001fÛí¸í0Ú¸F\x001bOBÃÅ¶ý$ÈØ\x0004Ûv³\x\x0018mZ£M£hk6\x001aÅ´7å5y ÔÁ9¦Ík°y\x0014l\x0002tÍyYÌ° -"dS]Âöøïa´e¶¢ÍÚÜ]m²;gu	´­\x0013v\x0014íMÐhá\x00067\x000c×©à3\x001b\x0017\x0004®ëäàófió0\Ke£\æc\x0017ï,5ÀÑe8èûòó)·\x000c\x000cÁ(ù\x001a\x001c\x0007Ë*í\x000b%v\x000fFÛÑ\x001a.Q2ó%ö=d¼¡	û:]¥ZBÙ\x001eP:\x000c×Ð\x0003ò\x0003çõâ\x0016JÒàeÁb°ÝÅs\x0018®á\x0007\x0018%\x001a\x0013Þü\x0002©R\x000c¯ªë>w³\x0018x\x0018®!\x0008\x0018e\x0008â&Ö­}\x0013ÉxÛI·-\x0015s\x0018­a\x0008\x0018¥\x0008ÏÃÖ¹ëRSët ^!l^\x001eFk\x0018\x0002F)Ó8¬°È~³mê¦Ý\x001eZ<
\x0016
Aà(Aø\x00185{(¼^Q¶caVö
sÎ-\x001aÀQ¨ì*Oâ¹rne¢ùC\x000c8Å¡Mv\x0019\x0005®äà¢^_tA¤ä*m?\x0011\x001ck(\x0002G)\=;ì{*%jqû\x0005æ0Vìàh¶ãkô\x0015Åq\x0006,¡B\x0014Q¦\x0012òÝÝåçà\x001a:Ãa:«ìbÚÖò¹X\x0017ÔÅ´]>=\x000c×Ð\x0019\x000eÓY)º¶ x^«ÁÊ¾¼]<\x000c×\x0010\x0004\x0012\x0004¨[­YðD\n 5.lK3\x001dEëÏõ£>TS¿`uª<\x001dÊ\x0018×\x001bëG\x001dnàýÆrnY\x0016YÎ-v¯°ÓS\x0018®q¸~Ôá\x0006^lë\x001d\x0005UÓG\x0011\x0011âå×Sn·å¥Q\x001b\\x0011ù³¼f1®ê¦'·­L\x0018®q¹~Ôåò>\x0005êGAÑê`\x0018\x001f)\x001e×\x001bëG=n`U\	\x0015j\x0002ÑïÆÝ\x001eÀ=\x000c×x\?êq\x0003ÌÔ³ªHß\x0017ÛÄ2'Q÷ÆáúQ\x001bPÕ.*Ú$£¢\x0015­z±ä¶5\x0019\x000eÃ5!¹\x001f
Éùä¶f;¾\x0008Z]\x0011ÍÓÚ3Ðñ¹4ìs1s\x0002ÉpYý¦Õï\x0010u½|òÛ\x0012sÑ\x001aKÃ.\x0017£\x000c/Tã:®7´ºÒõ¥¦À5>}®'n\x0012XË§¢íª@]þºèúMkkúÃ>×;yÂÎ®îªÅPô0à¶¸Ða¸ÆéÒ°ÓåQ\x001bhÖõö\x00027éº«\x0014auM\x0019FË ¢0\x001ap7¢\x00047ºÚ7\x0008M\x0001k|.úÜÜup²çIÇÆ¿±¨mß^ûp\x0018®ñ¹4ìskÐ
x\x0019zLE×e¦²Ýâr\x0014m01y\x0018É¹w¨ÅäÕ¸E^!ûÄÕ¸s¼X0\x0014\x0011)"\x0002?ÿ/ÆåÆ\x0016Üx§N·\x0012Ç£\x001b\x000cGQàg(ß[ßÖ©)êÌ2éõ,ØÉQ'\x0016y|aA[YÕ\x0016ÛöÕÊ9nwY\x001cFk|X\x0018õa<ÝH\x0002«ºÍ-\x0010ÞPaù÷)p[\x0008£n!Ö&\x0015<L$ýzHº± ä¼Ý\x0016y\x0014n4~!\x000eú\x0005rNwíÔ£«rÚXúj«ê\x0017æ8Ý¼n¹\x0011è-7gH\x0005Ë³w*ÿ\ÿr$
ÌÎ\x0001ÿæÑKÚ\x000bOiú\x0008¼~Kë½\x000bs¨\x0018Ýc3£\x001b7ó¯U<'øäpÀ8êÀ»7RÑ$»H¾hÛó\x000cÇû>1õ8æeBGG\x0005s±9e\x001d\x0017\x001eC\x000e\x0017 s(LýE°Õ\x001fÖ-#aNqÇ}r8.
ÐÈ±î=D½\x0019#L:\x001cå1èrá\x001a:xÈ½ÝE×vy
ãÃÎæû]Ì\x0008Úõê\x000fz»ÞÇ'_xóÃÑý}P³Omp`f%\x0002.ô®§míð×O¾þæé\x0017\x001bÛû\x0014+®±â\x0010V\x0004/µÔÄ
ÒAZõ \x001fí©éÃPý\x001aª\x001fºHÙJý5c[\x000fQ$Ôç¸½\x0012í0VZc¥1³V¦\x0008jÖ$á%dGú\x0000\x0010¶3úÃXÃ\x001ak\x0018³kÑ\x0005\x0002Õ®×ö4»¦Øí:\x0007k\ccWW^¨\x001b(}mW¹Ùu{Dè0Ö´Æ\x0006íeÅØbW\x0010»¨w+n×¦\x000fcÍk¬yÌ®¹/¬æóeÌ-u÷\x001a¶#àÃXË\x001ak\x0019ÃêÞ-~\x0007uQEÎKÄmÎ=õÖ·P\x001b\x0003¢^.>°mÓzý!áÜ\x0003\x000b·\x0006\x000btfi\x0018\x0012°1iR\x001cw&w\x000f5Ä\x0005cÌ\x0005\x0011D£&ñzLq±n½ÅÛMÁ\x001aê1î\x0002@	¹rýWJ\x0008ðÀ«Xæp\x0017\x0018î1òúÏ4³®I:Ën·\\x001cFj\x000bÆ¨\x000bDô%;^â&fÍ½0ngÁ\x001aêAî"Iâ%®bzUËn«ÿ\x001c\x0006k¸\x000bÆÈ\x000b H«c^vÉ¾¦¬\x001bëãNÙü0XC^0È^Þ3
hd(âñ©\x0017J÷4T\x000e5ì\x0005ô\x0005YÔ\x00112/K\x0016\x001fµl\x0013ó¶\x000eÅQ¬hØ\x000b\x0007Ù«\x0002\x001eÂèæÑTº]§X´Ì \x001fðÍ½XÖÏV_ '\x0016·[\x000f5.\x0016\x0007],\x0014\x001d)5ô"u\"FOsÀ\x001aÇ\x000b½¾¦Ö\x0000Û^\x0017°¥·cÒf¹à0Vã
pÐ\x0015°d¡ø-ìÛÐbÞà¸]­;
Öëå\x0007¯\x0017F}àqäU\x001dxR}Ar¿¼¹_~ð~ùÒ\x001f©CÖ£\x0004Ú-\x0018Kâ¸¼¹_~ð~±e\x0005ká¢³\x00186t¬S\x0008Áëå\x0007¯\x0017ô7TWcÚ¨\x0000Ú[á¶|\x000f5÷Ë\x000fÞ/.l\x0008{Å"]úÀ»9\x0014ìû\x0005æ©Db^<<{rQ´\x001c\x001eHDë<Í­o`|\x000c\x0019ã0d^Ø\x0003ä\x000b¹ä/\ò\x000cßU\x00127åÎÏ¸{¶áåÛ\x000fï>¼}R!\x001f~êSqöÌ´íQ\x0007Ék\x000b@¾Û\x0001ðòÙ7Ï¿yö¤âÝé×0ý\x0008Ì\x001f\x0014¥\x0001¯£cé®C8\x00033¬a\x0001©þ²]kVAWÓ"\x000bÑ*È»µ3 Ó\x001ad\x001a\x0002ÛH\f
@i\x0011
ND\x0015*L¼\x0017\x000fYÖ0Ë\x0008Ì\x001c\x0006Ú\x000f\x0018 [Óß\x001d=\x0001\x0013ì\x0005\x001a¹A,¸ÜÆ73V*HòëX³¿«p\x0000(/Ñ²\x000f\x001bõ\x0007|ÓÿñOo~ùu\x0013~yòâã/¿¼{ûþía
_tâÕ6\x000c\x001f¬t.¬Lp\x0007òóß½|úõ×, ðõ\x0017¯¿þºþüÙò Ç5z¼Ê\x0013P[¤ÝÐ«Á!ÝÝ$0Þ¯Ñûè£l«OÄ{QHÊfï\x0012ð xZ§«à\x0014lÒ2å\x0015T`(+ú»µÛAôa>\D_TSõùOì¶/w\x001b\x001f\x0007ÑÇ5úx\x0015};á\x00190e,(¢ÞÕöO}ZO×Àû\x001aÃIµ¸9@&o	\x0014ûÝ±à«ã}ô\x0000\x0014üê\x0001èÛwo~øøýQÏNªzP=;hK\èA\x0007îe!ß>úÅëÏ÷Á5Ø2\x00066ÃâM\x0016°à \x000eÆ>_q¯0u\x0010íê]¥¢]½«³måô,MÈ%iÏV@­JäÑñãpÁÀAë&¯\x0001=Ô¿l+1é\x000e£ß)ø\x001cë
\?\x0008·¦y¾Ö2\x001dIo[Æ½G«£`É¥Á£\x0010cSB©`½¬ÂP\?¸{¿£hA\x001bÆÐ\x0016^%®ó`Qê1G=	±l/k?\x000cwUû«pWµ¿3p	¸ªcù¢#êz÷ÛÌÌq´ÆáâÇ¥zýEû=eÊ²\x001dÈ{ÐlÊö`þq¸ÙÀÍcpÉeiáä¹\x001a©YûÛu)nwx\x001fk\x0018\x0002Ç(x	¶Z·cûê,Ôº©Ì9ºÞP\x001f£e}ö6õu\x001bNQØ,<\x000e×P\x001f£\x0008"\x001fù\x0005s[óÀ&dé\x0003t¸q×]\x0019.Á
Ü\x000cÛ¬r\x0011mE\x001fAß^×LkHÂ\x0004\x0005$IY+@>z=ºè×\x001b§ë\x0007n^\x0016!§\x0014¼¸ø¾¸ TÓN²­ñº~Ðë\x0006dgo
"k^$'A»ýÓöÞËã`Ïõ>77ÛJÅm-z
ÕõØâö2ÉãhËõ.mb[Í&¼Ø¶×*2M
sÉø0\x001aôa<²Ôà2\x0001KëcÖp¡^³IpMKca.\x0013@\x001b
¬GA¥°kfár¿fsN.\x0004I{VO\x0003§\x0002È\x0012÷?·T¢ë§Q=ÎeÑù|\x001aQ§\x0014zåE7àå]^\x000cÌê¿ÊÖ9ùß-Çøó?¼ùéÃû7ï~:X­®\x000b¤Ò\x00133«\x001d/ÒÝ%4cØ\x001cEøü·O¿üæÕÓç_nTe\x0015-®Ñâ(Úz\x001aÚ¸H6¸B\x00179ÒfgÑ\x0019¼~×\x000fãEtbÍ{¹
¸à%é3Ìa{Ð\x0019¼a7\x000câå~Ðì[IXê8ÎE¾ËP6#³3xÓ\x001ao\x001aÃ[³àÌÎlÁ\x001b\x000cKÔôUÆdÞÄ2\x0007n^ÃÍæEn'XÐbXº·RQTõ²ÛÎÙVp¿óÃ_>¼¿\x000f·¬áÑÓ@^üoô¬9"¢âªÃå¨-Ö8aÞ>(Þ:O\x0003æAò&Þ\x0010}!~`b\x0003s_o\x0003¸)Pv\x0006°u¾ÃÞ\x001fhÄÂÕµÕS¶,$N"<\x00116\x0007Î\x00006÷
\x0006/\x001cÄ
¸5ò°«Õ#\x001c´¤×ÐmSLü\x000c`saô\x000cSu\x000b-N¼	>6\x000fìIï\x001cnKÆ\x0000æHàè \x0016dnNi¸v}ö\x001dðæ3
eà(g,\x000f\x0016^ÎpbìË¥Ó\x0017zg9a´³ÍÊ\x001a¦7´Ó7®z2
\x000f\x00072n¬L­GySfí\x000cy|û\x0002l\x000eØ$\x0002ªÖ¦¬\x0001\x001c¸Ý[}\x00045øÇïèÞ­\x0006\x0004÷ñ?ÿçÑ'ÓQõÐª{[ÙOòûéÜ×O~÷úëg\x0007°ú5V?5«*z	ø `}V´ìÕ\x000fB¥5T\x001aêä! Z\x0015ºê\x000fR·ê¶¦Òa¬a5üU5®¡ÆA¨ÐÍÊpª±¦4Ñm«\x0003\x001eÆÖXÓ¨Y¡\x000fÝÕ(Ø«f0¼­\x0012y\x0018lY-£]FC¼iÒ÷aV!QåØmÈ£`Áú¬Q§\x0005¨µRÿ2Êõò}­GÜ^´´\x0016Ã#\x000f[Ð=ìÛ'ß¾}ÿ/ï~:Üíà°O4¦ü \x001b\x0007ëKHv¶B}ûìÕ·Ï¿Üì\x0014xÔÄpq\x0010.\x0004\x0008µú ª\x0004\x0018½Õñú5^?W$\x0000Î¤©6à¶Ò	¼´ÆK£xúã
?\x000byé^W'F5D7¬ñQ¼)q±wÁ\x001bH.\x001bÏªk½%ªñÆ5Þ8l_èÚ.\x0010oÓ\x0001Ú\x0011Hy»¬~\x0002oZãMÃöõ:Ç\x000fÅ¨{=»B¯ÛÞQt\x0002o^ãÍ£x½.\x0013\Þ2Ü7\x0000Ò§×MÖá5Ü2
7&É~Ò¢h§æÕÛ¶»Ãì(Üu3»5\x00137oïKÌN7ÓBÒ=Õ¼{û\x000f\x0003¶ì6Jo<ý¬t5i\x0002Ayûð\x0004^Co0ÌoÔµÒj\x000e^ÑiG\x000bá\x0004^Co0Ìo¬-ö­ÁNa]ß¯Û¶Rï	¼Þ`ß|ÔóÀ«E[+õÎ¸½ëã\x0004^Co0ÌoeQM
 t¾ø&ÅH&ñ\x0005\x0018~aã­àrWã¥E'6÷Ú\x001dN\x00006\x0004\x0007Ã\x000cWÓ\x001fµpìÊ>É­bg\x00016\x000c\x0007Ã\x0014Ç3O3\x0012-Í2\x0013«G\x0002öÖ?\x001f\x0006l8\x000eIÎS?\x0012\x00015ÅHNÙ	·x\x0003FÃr8Ìr¨\x001bãYFÕsbX#·=É{\x0002°a9\x001cf9ß5>j*$í\x0004\x0010KÇë'E=h¸a¬u½\x0004ù& ¢Q¥/~
Íá0ÍÕc >\x0002ºÒm\x0000Ùi\x0007ÂÐ\x001c\x000eÓ\x001c\x0004m¬ÿy@\x0015¨Qû¦ix
Íá0ÍÝÖu¦\x001a¶¦a,Úmäó¶\x000eØ	Àæpæ@¥PS5«4!V\x000b«þ´\x000faÖ34Ã4Q¹bÎÒ U-¬Û\x0005¿\x0013
kà0kðÌ¤ZØÉ4rÌÝE\x00047	¯7¤áGI÷j´\x001e©ÈBêb_P%QwåÎâ5á9£ÚW\x0014·"Ý&Ô³¦rÞÏ
Ô¼­¤
ûà\x001aYJ®Ì2ÏEO°îÃô\x0008®7NØ;aö\x0012îá±\x0016ñ\x0011já\x001d\x0001¶\x0013\x0017öÃ^¸\x0011ê#ªCVåÈ¢J|\x001c+O\x0002l¼°\x001f¯¦\x0006j¡zá¤Ù²^:\x001eË\x0004Øxa?l¨²~tzrý\x000cï¬9\x0001Ø$\x001b~8Ù¨¾L
\x001cUy\x001b9ÔÀÛí'ð\x001aÖðÃ¬\x0011¶¯JsYß\x0007Ä¾¶Ûã%Ã\x001a4j¤"{,R\x0000/Cí¢ª1áNÈ	À6h¼ 8©_\x0000,oq(ª'¹42\x0006
g\x001a9Hà\x001eçÑ_t\x000ey\x0016'¡8\x001a¦¸\x0014´Ú\x001eH_eë\x000f\x0005/î¬8×>\x0016
3\Ê\x000fÔ\x0018\x001f5³çi¬\x0006\x0018f½\x0016a8\x001af¸L*ÈÀ»D\x0013µFÄ
ø®$ÇY¼àhàríW\x000fêÍªb\x001fºYõv2\x0004GÃ\x0004WUqÛp¢&Â\x0002¹za[\x000fñ\x0004`Cp4Lp%>è°¿èÿ×S\x001dú¼ü¬\x0007\x00182üF£ü¶LîªC\x0003EØY=Úö$Æq¼Áð[\x0018å7Æ«b
éVû+ºË¢Ró,À0Â(a°ì\x0011ò\x0006ê¸\x001ed¯ÊÙàý,À3Â(g ×!D\x0015aÒ-\x0005]*$À¤\x0010-\x0018Ò\x0008£¤©\x001fa\x001flQÜ\x0013OÜ¤;\x0017lÁ(i ï-hT\x0013OÑb!$\x0003h{øø\x0004^C\x001aa40D}ó¹kÒæ(­©Ååí¦¹\x0013
iQÒ@
²\x000f:ñ:`\x0012\x000b\x0007}õ\x0004æÕ\x000ciQÒ¨y¥z5^{Sd\x0005KÊ¨Gx[à\x0004`C\x001ba6\x0002è0'ñ&\x000bñj¼§YxV­'\x001aÚÃ´Q}Då\x0015=Òø[}îq¼\x000ci\x000e`\x0016Åá6º\x000bµ°ÓÀ=GÅ\x000bn[\x0001ø\x0004^CsqæJÒR¯Û
v(¨}2\º\x0004ØÐ\\x001c¦¹\x001a=\x0013ö©kîWÒèNmÖ«g44\x0017GiÎ{§G÷\x0005¸v$TNr¦YÑ°\\x001cf¹d8²b\x000f¢·Â'BiyGzÿ\x0004`ÛI7Js¼>Á8Îp(I¤?s
³Z½¢a¹8Êr5[Öb%Fè\x0006î³D%Ï{¢a¹8Êr¾-çaÂêÀ\x00028£æìiØ\x0000lX.²\MæÔG E}E,AçOKLî\24FipÛÿÈûâu7GI}\x001c'ÍºsÉÐ\\x001a¥9ÏZáíÎñ\x0016:©_ÕÂ³º¡¹4Js\x0012OïÔµüÓçÛ\x001b\x000fN\x000064Fi÷í6]öÄ»l¥}ªï~älc\x0016`CsiæÈÉ«\x0016Æõ\x0004#NòÂÉÐ\\x001a¥9/Q\x000f¯avj]\x0015,à«Ð\x001aKÃ\x001cçI\x0007f\x0013eÝU(\x0016\x0004Õ~l»ø0ÉyÔ¥Süt¤Ç!JÉ½Æ4fH.
\x0007Ê`\x000bs_l¨\x001eM,LÓ^¸!¹4LrRìá RÑ&y?d¸Âöl\x0018.\x000f3\x001c/þæ\x001e4+Q	#¤Iî,\x001bËÃ\x0004\x0017H\x0016H'\x0017Öñ\x0005o\x000fÛSÙ\x0016I<\x0001Ø0\\x001eg¸Ô\x0015Xx»1©Õ¾³²!¸<Lp¡w¯ºJ\x001dN\x001cDQ	\x0000Þá>	°!¸<Ç\x0011»±æé!ê	V\x00190í+\x001bËÃ\x000c\x0017\x0015\x0016\x000b×\x001cT9CJ=;D'á5\x001c9×ì6\x0003ó²y©¸×¨]ð¬Î¿l\x0018.\x000f3\ð\x000fâ  êrÑNÅvö¾Àkø"\x000fóÅm÷··ã<C-wVd\x001c\x0007\\x000b.ã.xéäY¢ÊÈE]pÒ´ÓÏª\x0014ãÒÊ¸K2AÀ\x001dÁZ¾.=\x0006NÓ^ñ\x0010eÜCxÙ\x000b·º«\x0000Í:g]¹b®\\x0019\x000f*uÿ\x0013ëSô¼>ÊÐd¦i¯àÅNõ
ß¹×K©Ç!i#]É*4Æz^S\x0000Ã£!p7|éjvÑiç<¥Ñ èÂ\x001cÝ¤V\x0019°sÕüÇñÔ¾i\x001f\x0005'ö¢{äÝ¤$\x0019ì\x0010-ÿqã\x001c7Ï1Z`')·{ÉãRÉ\x001aò!<;\x001bö\x0011ÅGðÒc\x0019+*ËSÿ?UûÃß÷èIã»¿ö7\x0014-æÓ\x000eb®ÿG0Çõ/5|=|Ê,vöÉªT.]¬]¥ò¯·5Gç#\x000cÛÚ\x0015\x000eßÛù \x001e.hP\x0015åkT4\x000fóGß´ûü2oUùZ@Ó3=+¶¨gúûGgúûñ\x001a\x0010µ45áö\x0016Ð«,\x001dM\x000bé«ïøáïøaÔÎþAëÚIÛª
Ißð¢s0ÍÌo\x001eyôhüjµA÷ë¸â9b\x0010Åë\x0017hG>ñêYù©{\x000c;»qÜ\x001e3Oõ´45ëªÁ\x0012PO5à¬\x0007h´7±êÑè¶}`¤~¬½¨£,;èf=?¶u¥q[{ÝNËÒ\x0012:â\¢¬`Ê\x0019/§\x0010â#º\x0010W"J/üùï~þéè\x000e:\x001b¸ËQúbª!¯^Ù©Â½|ñÕïõå>^\ãÅQ¼üø±Ø7°h´à±ÂlÃ»?B~\x0018¯_ãõ£xÙQ,EúàyxQì\x001bEÆÃ½\x001aÜa¼´ÆK£x£ûõ<@ü*Rõ®çáî¶Ï³xã\x001ao\x001c>\x000f Ïº!`ê]Û ;­\x0012á^×öa¼y7\x000fâuEÞaùK\x0019TSE\x001aîu8îã¥G2éõ\x0007Ý?ü×¿ÿÇWxwÔæ\x0012â²T\x0015åM\x0001}ÏK6ª.h|õÛç[\x001eI¤3R\x001cCZ¨ie$=Kèûn³â·»µ\x000f"õk¤~\x000civ\x000fm\x0006&]÷Ì\x001bbÒ¼}`\x000f\x0002¥5P\x001a\x0002Êk4d\x0011t½õ*èï¹\x0000ÔLÊM£×Æ5Ò8t8b¤tpSYô©]ªÒºg¯#Mk¤i\x0010i\x0012ºÍAÖy\x0019©0ËöûÆAy
3ÿ\x0015\x001bô¦ìµx(7\x0006\x001bèÚ\x0006F"m@Û¢Â\x0003»\x0013.>\x0018\x0017\x0005c>+À!7¨¡toûï?l\x000fh\x001cj®>\x000cÞ}ÔñdîeçdmZ@\x0005ww\x000fê)Ç¿\x000e½óï÷IÀ©û;G]¢§Àm·Çìáå\x0011¥Ö\x0018I(õwÿôþÉË
ëí\x001c\x000e|öö\x000fÇE­=QÒ\x0015[åYÚ
k PÍmUºßýæÕõo={úCÏývGáZ¾\x0003×ß3¾#$m>(E
\x0010!tQÞ¸Ùp9ú\x001d~ý\x001d~Êïã¦Ù\Se	#¤2Q\x001fó\x001c£ßAëï \x0019ßQÃxy:­\x000fW-ï]\x001b7ãV9ú\x001daý\x001daÊ¹r:"V|iï}È»
ô3þ"¿¸þ8ã3NE
>ËõèËãv?òèw¤õw¤)¿\x000eh{\R©Õ½UºioüG?#¯?#OùuP¿\x001diQ
^¾#ki:Âf\x00126|;\x000cÛ-7DÙîoéÇå§²*?ýòäÕÏ\x001f?¼ûóÿ=¼ø\x001bkJ¡Ê¬<\x000fË©rDÔ\x001bï®-o)ñ×O^}õúç;+ËËã*TYU¡FaK¿3ëÀ\x000eRé+~{\x0017Á9Ø~
Û_Ý_G+lß­­2äy/Q>\x0007Ö°é
lÄó ¯\x000eÊ
µiwÞ@¹]z?:¬Q\x000b¨¡\x0004Ya0,òs^\x0001k¶¿3és
v\ÃÝ¥¾±,õË\x0005v\x0017
äL`\x001eì´.Y»+\x0010{^]«ÖF	Þ	;¯açK°£î1ðÜ#bíþøO;Ï3§`5ìr\x0005v&UaãV\x0000hKÒ|\x0017øp;»OÁ^
mÜ%s£
6z¥¶QOIÐS\x0012wÞ¥Oá¶,y&ùå\x0003trÛËK[Ô\x001aetG`û\x0014nCp'y©Îô'mó®¸UøÃíí½8Û\x0010\x000e\a\x001càÂØV\x00047jù\x0013özrNá6\x00038×ÓÉ<wà/`Ø\x0015µ*GáÎ Û)Ørà
ç°F¢è¾ë×\x0012ê\x001b\x0001î<DÁÆà\x0015wâXÛ\\x0004 ²$ÚnÙ\x0006(\x0012\x001b;ï§`ÛàõÊ­¬ª*[sÍ£½9Èº­\x0017âöºôs¸Mô\x0017Â×ê¼I;å¸æÔTòøþ¨½Ç:h¼	^ð&<VÈ\x0012y
7IË\x000b\x000fN¨EÜy÷;Û\K¼p-k\x0010ºF\x000f/\x001en1óNÝIÚ:Ûx!\x0016d\x001bMñ)/{¢uº¯³ð`ß<Ü&\x0016Ä\x000bÁ`
a\x0008PU§P\x0016=wñ`ØÛbt\x0006·7nÐ_pk4(}/\x0016ñ©\x0005·¢.;»¸N¡61¿\x0010S±³Ð#.ÑAÛê´3­=\x0011·ñÞþ÷fQ/½©®\x001eí\x001a3èv´BOÁ¶¥+Î;ÄÒCØz)Û×ª¹\x0008\x0013A\x001bÏí¯xîìz×ß¢³×Nvî<¦á6q ¿\x0010\x0007\x0002·GI@ÅsuÔ<	u¹SwV+Âm\x0018Ç_aú?ªK)ô;Zd²#}
·a\x001cqÈ1Y/\x0005\x001aãxÔ\x0000Öi¼7ã¯0N\x0005¬5*ö5-[ìít\x001f\x0000ÍÃmÊ\x000fþBý\x0001X­J\x0004Q=×«Ú\x0016ã¬\x0002ÚÕDóÌM(é
QÆ\x0014{ \x0018G=Eâ	ºnçæ"ñ¸
UÒ\x0015ª¬Õt½¬\x0007\x0015-*{=Û§p\x001bª¤+TÉ3\x001eJñ¸©\x0016ÒÉ]IyOÍê\x0014nÃt+Y5LúxÑij×\x0012\x001céóBØY·x
·­Ó_¡KÖ\x000eBñAÙ2¸çÀæÃóIØuè
ëPq¢\x0016¿\x000c¡·[IN÷\x0010¹<1­$C:ttø\x0011J\x0014I±â\x0016çíÎt3qÎÃmH®\x000e÷?IùÁ\x0013I$è«oT\x0015Ê\x0001,\x0019Î¡+¨Z\x00183kp/Ö&]?î`bh\x0012\x000cç+ÃuWQ\x0006Æ\x0012X4fáÊþn_Ãåyæ\x000esÂ%Î®\x0007á1j2ìP·¹¸£h|
·áps\x0010ny\x000e\x0002Gá\x000bn¯Å\x0007\x0017ò¼!\x0018ß\x001d®øn&\x001a\x0019de\x0000'çÛé¶rW&Æ&ÁxpÅp#µÞÈt\x000fÂ]z,N¬y\x0007ãNÂ\x0015wR+¥xÌ5íIÇEÔØ$N|\x001eÆÄ+þÄ%ÏÊ\x0000\x000bn_ø)cÃìµk\x0011&VMÈ®\x0016VÝÆ³FNK¤~ZÚr£åÛhÙÄ\x000e\x0008ÄÇð\x0011/ÁÇz\x0002{¥zßI½\x0003ýÐLlðð\x0018¾kÖ¯\x0011yW©ÝÇ¤[ÅÍÏs1\x0015ý·ï\x001f¡çG·\x0005µ\x0018äKa½¸%¼
u\x0002N4~p\x001fÜÅ£ÏCäè·V«\x0016.z­QÀj¾+Þvqwã*\x000eøíÇ÷þÏÃçx\x000fvÉ.\x0004Ü@Ïç=\x0005TE\x0012·ûRõÛ×¯\x001d\x0001kÀ8\x000c8\x0004~ån3G[\x000b`"÷aýãý\x001a°\x001f\x0005ì\x000bH\x0013zÌ,ÑÞ\x0002£6oç\x0018v\x000fõQÀ´\x0006L£Á\x0007×\x0000'îCõòV\x001cT:Îï\x0012ÐQÀq
8\x0002v¨\x001d1¡nGrõ3\x000e¼ïæ;ÏðÚåµs¼öx'
Í\x001d¢PcÞã£r5vÁ½òu
÷ÚÕÅR¬z¦á\x0006\x0008Ú`!¬¦°|óäwo~|óÃû·ïß\x001díã]T\x0005\x001a¹¹´©q\x0018µ4¸úÉ§O~÷ôÅÓ/^={õ|«W°ã\x001a;^Â\x000e<Ø¦ÛëH·ÁEÕ\x001a,öÖ\x001eÄî×Øý\x0015ìXj8«ûöÂÃØ)y}+v{ú\x0008'±Ó\x001a;]´{Ôê}®ï£ÐÚík\x001eÖÐÃ5³×©íÙw³\x0007èÙæ²ÔIìq=^4{_£\x0012tÙhÐÅ´§\x0003z\x0012wZãN×lNYe5|ÊºE|ïì-{r\x0004'±5ör	{®d¤
§rXxPUKAs}ãªáýº»xZæËÁ§\x0007/\x000bµg	ýÞúßØ-']"%Ì5^A}ÖD]K±·oú=QÖà
)Á5Vr%¨¦7«Cäi$]²{+ÜNb7¤\x0004×X)»ÞÊòp\x0012
 év´«Me%0¬\x0004×hµo.í²\x001c±o7í,vCKp2?,cOSÃ¨ÍLKÝLðà\x001a1¹LÝÕðà¶,ÇÒ»Uö6\x0004oÈ	®±SÏ\x001f´0ç¸g±CÊúÄ\x001cödÁNbÏ\x0006{¾føäz]+'eÖ¾
\x0019òÞúæØ
±Â5fM]·ÇÚÕ£\x0016=¹ÌsÀÑ&\x001d\x0017ý»\x000f½W¨-T_2¦ \x000f\x0016@;3(gÁ\x001b\x001f|$êÕÅê\x0004Afæ!ôÎÚ]íåØÍMÅ7\x0015 \x0017\x0012\x001d(±»
?ÎM÷Ð\x001cw¼vÜ£÷*º¼xÑ¸rõ×qtró$xobI)¬\x0011¼®\x0005_ú+@\x0002xÕ9r{}Íg±XÒ_%£Ci²@nªlf\x000f^·ù25\x000cöÆÓøKæW7»q4þ¢£\x0001Ôw~¢Ï±7·ìmÚ8	Þðª¿Ä«5ë£Þæ\x0017âC¼\x000ftyb©\x001eÌ]¥kw5×ðÑkKQì¾ô5Lµ;\x0003O×\x000e<·(=\x000c¤Ô}úûÐfB·%±kç=cêí\x0017,ª\x0013%eí¸s¹LüNâ÷½+ð0°ldÀÐú¹á\x0018»J×îjÊý¼sæ$ëk²G=szY±|¸fy»#IûDî®ÒSÔ¶\x0000Ú[¸w\x0012¼±|¸fùP¼Uð'ä\x0016ð^\x001fj&R£ññ\x000c\x0011ôé\x0000kXÙ
\x001d.ßÂ1{ä£qñ\x000cÔçú\x0010Ü`O¾\x001f=âõT¸ip·\x0007§7WËØYÊØ\x0018õÂÆ¾\\x001bqogØÙ0þ¦z.ü\x000fîlJ]%.s¡÷¤ïm4:tß\x0004ý%íþî¿¬Aeì\x001e§éUÔ¯®ø,»Ï\x0016ãM?ÉR_	]\x000fÑ\x0015ksBß\x0014íÑi©ö¶Rþ\x0005¼yô\x000b¸rþÕÂG½ºöð\:;¾F{:æï8|\x001e°ësçSCËzq¿tq¿ÿ\x001bº¸~ÿÏª\x001fÿ|éÜxUæ6	ìAû\x001f9+êõ+üï\x001eÁ¿æw~eøå÷o\x001f\x001d·KçÓÁNç×ÿÝ#ø\x000eÏ¯uß<:û×\þ¯{öáã3ñû±d)ü@Ør[ Ðu/4·\x001e\x0002îqÌ\x0000îbÐàk^Â={-êD¨+k
Â¦`áÈ\x0011úþÑ\x0011ºø;p}\x00142©\x000c&¡ô\x0017óÿüè\x0006_c/'Å9}YvåV»üððû?<2ÿ\x001fþ¶nð\x000fnð¥¥zÐî²ØGÜ\x0000{ªîwæ­ÏÿÝ#ó¿û0?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þzÀÝÁÒ\x0000S\x0017\x000c\Ô¤ËN`èvÉ\x001dÞ\x001d.WgçåõÅÍíõÕåÇ}¼ÊT¼øg\x0017p4\x0016Ø¥x/;\x001eK<rÓ\x001bí'\x0008\x001ckàØ\x000bl$\x0003\x0007\x0011òe\x001d£û¯v¦a\x0003ët(\x000f90øà)\¿-nÛ<ÿ¾9 \x0000û
²Úq\x0011¦Ñ"\x0008Ô\x001bÚUÕx³¸ýqu}±£ÍpàÕ\x0015¯îåµ$\x0001¼õ\x001c¦IJÀÛnÝêàµ\x0015¯íä5¤/}²kõ\x0011°îÑìë+^ßk_ÖUN 4ØÜhÇ x3<\x000eo¬xc?/)\x0006búÑGÖb±UÙÔ¯íàµÕz°½ëAó;n\x001ax«\x0014ï7î¶îXëW·\x000cÚsøI\x001fvä<\x000eÊo\x000eØ,\x001e\x0015Ã¡Ë¸-/\x0008GSýÞ3µ%\x000bÙßlþþr¿^>=~Am?µGs\x001bLãJ\x0011¬¤¸]\x0007~ \x0015Q§¸ý\x001c .pVÃ
)×ß¬þõöl¹8½º<][IUIªþÌ¤¦$5fRWº^R*ÖHê\x0003O\x0015Ò\HãjÝ|ÐP^PG:\x0002îkô\x000b IC*ï#]\x0007Q\x0017p,H\x0005\x001cçO/÷ß¾m~øvqúÛúe³~]|xzýü°¿\x0001ÂÁ¿nÖ\x001bX|\x001dGtlÎ=¿º=»¹Y]@»8ýqy»ZÞ->\Ý½ß5ÈEf\x0017¶¸\x000fÄu\x0011¤/_?oþ¸'!=à`ßÈ\x0008D~ñT&'±ûsw¾¼{¿út¶Sÿ!3ëáY"1ãÐ(RAÅü^±$¿²¨¡m{jk\x000f´ª¡U7´\x0012\x001bO\x0002JÂ$f'%w*Ûö@Ñ\x001efk+fk»W
XÎ«#äÅ¡¸ÆËfÄÓÅìjf×Ï\x000fá\\x001eI(\x0019¶¢fÁ
ÙT±èö¢Æ?{¡¥åf

·å\x000eÆ\x0019³Üð¥öäÿ\x000ef²ZÐQö.h
÷¹x[bOÊª1p=¤Gm-÷¹IÐ\x00123Âµ\x0010yÓÒSE1TÛ¤
\x0010Uæ;jÑ\x0003Nm~ÜöíQÚÛ65+¡Ú~\UâªN\©³b\x0018à*âÐ	×sß×Í÷â\x001e\]âêN\pj¬k$\x0015âx)5[wgSÂ$\[âÚN\§Orù«D
1\x0017\x0003K\x001b\x0003í.É×I´¾¤õ´Aq­(Ò*2®\x0003nó)¾\x00077¸±\x000f\x0017åHE&­q#×7zÓî²+kÇÐé\x0019"ÖäP¾5#¯Ï\x000cs$Ç +Ç ;=C\x0014d\x0003\x0002*£ÒÒ
qp\x000cÍwî\x001eÜÊ1ÈNÏ\x0010á¢¢%­Ko\x0003`ÜvÃX\x0007nå\x0018d§g8îÝy-Õe§.\x00126osF\x000foå\x001ad§o\x0000çÀ2H\x0001aòfSÛå\x0003ÊÃ\x001b*ÞÐÁ\x001bñ_\x0013×c+næÕC+.\x0018úÀåÛnudØÊÉ\x001eO\x0016ÓaÃ\x0019*x\x0012«¼\x0016ä\x001eÉm«*G¦z\x001c\x0019â*\x001dBÉ¶QÓ´?\x0008\x0014\x0004óî\x0013:8·r
ªÇ5ÄTQAÉ\x0013\x0013bè ÐÛ\x0002¾°«¹i\x0012oå\x001bTo©\x0014\x0010uñ\x0012¯åd¯-Û×¹=-óV¾AõøÄ;´½£ê7\x001dlI^öZ3Fïá­¶êÝn\x0018Do^
ý =1s}÷u>\x0015?\x0018úwî7ÏÏÅæeq±~¾ß,N_áîõÀ\x0001=¦ñÂp{£ÉVQJ~\x0019\x0008£ÚêÎV××«Åêvq±¼>[-NïàîW%¼\x0007¯xDºV~è/uUãè3b'».ÙõLÃ;Ê^á\x000bøÀðm÷1\x0003Þðf6<½ÁaMaQ\x0001/\x001a\x001f3ØmÉng²ë!ßé-ÝMQW|\x001c¯hïw%¼	¯\x0006øh¶§*ü×Ã·«/áý<x\x001cö\x0018iÕX\x001a\x0008\x001fXC\x0010ÿÛGf\x000f%{É\x001ex\x0008t\x000b\x000c°lø¦´É\x000cöX²ÇìZöðõ CÔ
?Z½Ð\x0007¿ÕÇL\x0007Io©SFãÀHÉ§=°üx§L\x001f}}¼Î:_óè\x0004Iô_²Cp\x0003}Sìw\x0006}u¾ÊY\x0007¬èÜi²\x001bNúÊÑAðWiÊ~Î ¯NX9ëEQ¬´
ôr»î\x0003Ï¥JvõÑWÇuNùýAL¯¨C\x000cg°»T£à:é«sJÎ:¨|´¤v´FI3{\x0008ÕÖA_\x001dTrÖI\x0005¶´èiÍ86z36º:¢ä¬3
nÍÄº5ö\x0014\x0006bç\x001b¿Vºùæ5¾:¤ä¬SÊcâ5çµ±\x000e»8Þ\x0007Å+Æk
tÑ«êR³N)\x001f±-Þíã@\x001f\x0019§¦)Ð4NßN\x00101zuD©G\x0014\x0018ÞÒøXKÅhxÉè¶Y|7ÃðÕ¢W3\x0017ýö*b\x001c7ÒáÙM*×|PN/­oßø\x0001ß¾¿¾.HL\x0018ì65(O\x0010\x0012MG}\x0013b;R:6üÝ-HL\x0019ìGV%²êE¶Vãôã¬â	UöG¾{¤ÈéXÄº$ÖÝFdËÁÈË²Ãäñ®ÊÉÈ¦D6s5×ä±x\x0001"\x000f¥ql=OG¶%²í^\x0017°\x0005¥\x001cÖEÎÜjaÂ°.Æ\ßtbW\x0012»~#+®7ÆÉó¹Ð\x0002Ì#³Ûå»}Ä¾$öÝ6Æ\x0014(ï=K\x0017ä¤ÆK¸\x001eÏÈ¡D\x000eÝÈpí\x000cáâ±GZhzÜÁÛÑVò¶2$9e1Ç+[5d\x0014\x0005YR\x001c]õX\x000859T»/ôo?£H_+Ô\x0015\x0013s\x0018ü²\x000fGd\x001eæ23õ^S;Í­Ù)\x001bDmA\x0006	àÝòØë7Øë\x000eìÏo°?ÿ±Â¦\x001b³-Ä§ üóÝû¯Èüqó¸y^?dåã¯Ç'\x0014IÛ]R«±AO¡ö7»è¨¬ÖT¥ìSGaQRûþ\x0003B\]®®çY.cy	^íÐF³o&Öâ\x0007E¨t}ÿå÷ý¹*çåÜB`@\x000b\x0017yê9÷²©@IF¾>;½ØÏ§K>=\x000fuhZ4\x0016E\x0012 	\x0003à¨ÊØÁ¦\x00044
Hc¼`Mè!¶1(\x001e\x0007=®2r(-éìT:|!c¼@£\x0011Á|J3_ýûº\x0012ÐM\x0004D*Õu±Y8çëlTË­¼	³-èK@?Õ:Òù
j¶m¤×Få­Í\x0017J¾0Ù,¸\x001dµ82\x000cÈ\x001bÄ¦\x000c\x000f\x0006%`j@£HÛLE\x0007ç>Ùúú|pc/â\x0015]ÕØN+¦ò\x0005®¬UÑá\x0007vTí§À\x0017Î5àV&,\x0011ÊÉ\x0016t%È
&\x0006%\x0002\x0013¡âÞÈÐî-DX\x001d"rò)âä¤M\x0012â¢]<h¬¿®\x001e\x000cX"rò1b$¬Ò8{X,\x0000Ò\x001e
8	°:Eääc\x0004µß\x0008Ðpý1\x0010\x000eúDMIÕA"'$*påÐxä%>Áý®Á6ëÞ&\x0001V\x0007z ¡ò\x0004)
µ\x0006â.!G\x0008ÿ4=°:Iää£DDÎ:`p\x00120\x0012¦þªlÃ7âÃ\x0008«³DN=LÂ65²÷YÈ(iÄq\x001dÊ	«ÃDN>M\x0004×fÃÕBk ô¯rTÌõPBU'jòy"yæ\x0018}±
\x0015'p²Ìuª\x000eù'{kØÊz×y*\x000flåÀaöFQ3T¡äyÞ2
êï}âx\x0015F5×[«Ê×¨É¾Æé¡K²VqE\x001c­A;°ÚÉjúNæ¨\x0006	i	ê\x0001¯©h3\x0005OWDOÞ$§ôje<o(¸È@ÙQ«®6¼I°øtWã±rÃPùÙ\x0017'[6ÆçÛ\x001d~0
Ó²·Q¨QÂ+Q«áþ4Z­qøOý\x0013~îé ØõA	l\x00130[\x000c\x000f\x001bfôyýðÃï-(\x001cÓA!\x0012süa¥)yÞ\x000bÊ/Í\x0015¿\x00035=?½<!¸ 1ü¦_Þq4Ñð0-"ûÓõüòr0(&Æ(ì¥RPf7hóiy­c¬{Ëáô¼¹ùvÿ\x0015ÿï/Ö\x001fî\x001fîÿøã~oºÑ&´\x0006`A.ÒjºÃ\x0004Ô³oQ®nÎ>à?-\x001fÎÎÏ>}:\x001b5+\x0003\x000fad\x0006ö½ÄBäÔ]@\x001fIÀÜz\x001bd{æJ\x0017p¨C7p¤d\x0014ØS´<\x0015\x0002§æ Þ)Ä*¦$nq<Á\x0007éxº}^ÿmóüKäo^aM½Ãá¿;aýM×pKÍï¾\x0000ä$uÿéî\x0017X§Ëë\x000fïn¯?¯®o¸<þæêîútü~Àµ\x0015®íÆ(oI¸ÖÒìM­\x0007Ì^VæòÊ¼¡ß¼\x0011Ö°¢%!d¶/\x001d_Ab/F7®ÚÔ\x0005\x0010\x0011µs$°z~Ü|{Y|z^}Úßíñ9"\x000bD,*È5øýr¯\x0004ì± yu}¹º¹Ï\x001f®vt3«*YU\x001f+>:dV¯ò5G\x0005Âb;\x0012©.Iu\x001f©
t%\x0016|\x0013¹\x0008IòT\x0016Ñîøê`5%«écõ2­"\x0005Ù$Å\x0001ÖÞ&Âº\x0012ÖuÁjlÊ½^(xMsz"WK´ÇâÂ°¾õ}5i$R²¬Qø\x0004,!v\x0015ÍÉt\x001d°±}°Êr\x0016üKÜI®=\x0013°&)èc°ÊÚiõy-\x0008_¨\x001eµ(Nh\x0015\x0004\x0011À¬£×¬©-"E2.\x0007Sí«ú}¶/çãa1ÈHÌ±9ß¸ÇÓ¾eVÝÌp8äì­HB\x001däÆX­N&YÇYÌAÖ\x0002~0Èoæ3÷Ãf¢Í?\x0002øýz_X\x001e¢\x0014*¸\x0012P:\x000f\x001c@	¬\x0010éwdYÒáûaµBñæ\x001f\x0001ÿlV¯EExµÜªÃ=â\x0006ë(ßí}V\x0017Ød&\x000eàì¬2­ã®\x0010Ø1é­°xVgi¸GÜ`åä~JURª>Jµ°3¥DIQîQ(uI©»(ËCõî¬\x0003$90ÄMiJJÓGéù\x0017O(©Pï(¶¤´]X*¥¹\x001d(\x001d¥ÛàTf.¥+)]\x001f%)\x0012%í\x001eì¡>\x001a¥/)}\x0017¥1ù¡\x000e(MÄ\x0010&Qòl1ø¹Ò­v\x0016e()C\x0017¥v¹P\x0010(á%è\x0017WméÒ½e\x000e¥¬~qÙù\x0007|eÊ®(æ\x0012*ÀôÖ³+Jhs0·%Éa>L{âØc|z"&©µ\x0001¦31]éú0­ÁáéG\x000f4ü\x000c0

uåçb
3ôa*%R\x0011SâcYÂ\x0014Q\x000fs}f¬0c\x001f¦Ö;¢Ä
PJÇÝÎýÍÁLi\x0007>LA\x000eõøùG·AðNÏUs8u\x0015sà]SåÙèÔ	¹M#ù\x0008²qCj\x000bâÂê®klp¹c
²_|zúýéñ\x0000ÕNØæ¢sN±cªÇG~jë#Ó ûÅ§««ËÂ5_°²äÃ?§\x0003*\x001b¸u\x0014Å[óS
¶Ô
ÝÞÍ6û·ÙAµÑÖ9j\x001câóFÿôá?ÿý?Ï_\x0016«ÇÅé}\x001a½58Djtä0\x0003BHUÔªh³>-Ê»_Pî¯\x0014>Ea÷SÄ?=Û1xk V%µKí
A\x0019Ëé_ESx°c1½\x0003Ì§6%µmky"<]\x0002]í¤RÃ ¹ãXÚÌv.³ó¨ô-õ1Àaï\x0008Y']ùÐ®v³
F$h\x0001±¾£E\x0015.±8+&Ï¦ö%µK\x001d¨kØÁeÏS­TRL¥ÊG¡\x000e%uM-³H\¦ö\x0004-í\x0000}\x001cSÇ\x0012:ÎVX\x001fL	\x000b\x0008\x0013ÉÔN±ÿÇYÖÃY}µ½®=\x0005áÙÖ¼®s>+\x0019[\x001d\x0005»>bf1Aå"!Àö\W\x000ckDÓv´Yiÿ\x0008Û±ÈÂÑÄ\x000fþÔ»RJ£ki(ø J\x0017m¾-~xÞ<§ëÍ·ýÏ£N«Îð^
ù\x0006á\x000cÿVN7+á8\x000eB»\x001f®W×i´æòvu3þH:ÐÞÌ£.=$|¬CÏá\x001d\x0018Ê&kÖ\x0000ÏÁ·%¾iüAÜ
¬Ïj9ÊHzÜQ\x0010ì\x001a\x0013Ù\x001fJü0\x000f_\x0001¾£6\x0019G©Q\x00036\x000f\ÃÞìé \x0017ÚËª<
?Håiÿþé\x0015n,\x000f\x000fÿØ6\x0017Îq\x00156_UqÄ\x000b-yÌ¢ìËøþê\x000e..çç¿Ô17#j_"jß( VESáp^"p¶%?\x0010q;
\x0011íCD®L\x0008'd\x0016C\x001d)¨
§mù\x0007\x0012ZU\x0012ZÕ÷;\x000fÊ\x0002Ç}e\x001b:ãPÊ]«s\x000f¡3%¡3}6\x0014\x001fp^¼£è¨óW`ý×\x000cÄX!Æ>DpKlÄèò»\x0002 F=XqÎfñÕïìû~gì¥'BÇRoÚ\x000bÒ¿\x00146ì<Áö\x0011êPwî\x0015O3vÓJÌU:	Ëf#¶\x0007Ï\x001dèdµñÏ®Ýâ%
SM^1\x000fÜÐNóè\x0018év\x0010ãÛdNTÉ\x0008\x0006<æ7Äåïîôç§õó×ýÖ\x001aK
±7»F£#yocõhKÈòâýõÕ\x0019Àþ|u~u=cÇÍ¬JdÕ\x0001x\x001eõ\x0019¬f½!£%dÕ\x001cýÐ¬KdÝ,h0\x0001­\x0014\x001bªpíX3Át`S\x0002nà¨ñòqt\x000cMòã4¹1\x0018\x0012\x001e\x000bÙÈ¶\x001fÙÐª02ðÿ"/d9ú\x0012>ØÄ¾Ø	ß"ÐÈÚ`±<³ÖÄ¦lú$d8OÞLðºz!½\x0000'¸ø´yþõéa½÷Næ|}×Fòh!hfW\x001b\x0019û²\x000b¼}Z]¼:\x001f¯0`ÎBÃQ»toï\x0004\x0015!W#\x0001(¸âAx@R\x0001\x0007.ÏDµ\x0015ªíGEqUB\x0005ç«\x0012\x0001ÕÒ=×gI¦Y¨õ¯ßÿóÃÉ«szOÃE×°dT\x0017Êu\x0017ª«P]?*,\x0000S\x001fÚ°\x0006B@B­ÒcÓP)\x0019`ü`;`\x0010\x000byþóßÿãÇ§Í\x0003þñóýÃÃAbTªe\x0014\x0019\x001a\x001c"Ïo+­x!OqÃRÅW·«süÇñmh?¼*áÕ?\x0019¼)áÍ\xeYNFCI\x001b¸Ø(îcjv#öÓ\x001bQÑ¹øZPE~R\x001b\x001bðY}\x0001²Â¯ðuå\x0012|AÑÍ¿½®7Y_åtýûÓýãþ·N\x0014v\x0015¹\TXS\x0016ñ±3rCÐJ¾y½ù»åõ*ëª./®Î.÷ÚÔvJOöÅ¡kùÉK4\x001b8
\x001fçúÔwB@uç\x0004Ê;IyæP!Ì\x0007%hì5i8!N\x0006\x0001$N:Á¢9O7\x0013´\x001aYW*~ÐÅC\x0016Ø°JØ¢à\x0012w4¬<Â\x0012x\x000bìûÁ¥e-\x0007°\x0003M¶Ö©×lÜ¿\x0014ÚZ °1+%\x0002ü \x001cô
Ï_ï\x001f×É}|¾ÿ}ýð\x0015Ó{ÚH°MØ¦;\x0007&\x0011\x001b_1ßïH #\¿m#á\x0011\x0016w\x000büóìr\ØÇë³åù\x001d©Ûü\x0005¤\x0017Õ\x0017ðâ\x0018ß@áÓPú\x0006õý¤3Tg\x0012KÇú
JU_\x0001ÿÿ\x0015ÐÃ©ü\x0015àr\x001f¬§Ê½`¬·Çø\x0006
â¼ºT\x0017\x0003?BÞ?½>lþ\x0006èT\x000f}¹þ\x0003?Ù{
F{NÉs¯IÁá\x0000åþQãûSðýÕÝùêg@§zèËå'üd?¸.Áõ\x000cp£FC\x0002ÇÑ²1sS\x0012\x000eI>&·)¹Í\x001cnðTÇ¬¥Ç\x0016ç,8(çr,Ýà¶\x0004·sÀá\x0012s\x001b
;×²Ö¶s<+YyÙÌmtû\x0012ÜÏ²¸ç6ñ\x0000¾RÅd²æÖnîXrÇ9Ü\x00159ak\x001a\x0012Äw.(~\x0014G\x0005ÕÖ³ö&x\x0012Â\x001eý,Gã\TÛ5ÞÊÐôoÎ¿¼dUÅí\x0006Å\x000ff¬H=YÀÏ/°b4¿çzwÔ¥^6\x0010Ñ²Á\x000ff8uz\x0015S8Î3'§\x001d*óñÂi¾MÅ\x00172Ob\x001fêñT_y½÷ëo/÷_ÓíìçÍó×õßÒ¨ßÝ\x0001\x0018¶?ÒÊ\x0011\x000e¿Hc¦é\x0015%äs´¿0«÷~ys{ö!]Ê~^]Xþ\x0008ÿA3
#ämylBNå±ýÌ:°\x0007Ê~býqV\\x001aôÛ(w\x0014z©åö%q³U\x001f·Ò2\x0017\x0003\x001347ÑcpN×	\x001fÞ*uö\x0019[×ÆÖó­
GèÎ86¶²4)\wôG2v½®å¼­ã·tØÔ*¡×\x0017\x00118{§±c
\x001dçAo/ÆÂÌC\x0013Qw¡:­¯\x00166þ9\x0007ÛY¬ÁÉkÄ\x0013QËëræHØ¡²6þ9g?JÀ÷l\x0012\x0012Ì
 [Ø0;ººÌ\x000f?(JÚW/÷ÇÇÍâ|ýûçÍóËÞFâL¿+Q
?½Ði~:§ch¶ZçºñÕíÙêò\x0012Ï÷«ëqµ_¦V\x0015µê¦\x0016Ñü\x001ac°åÊfhA\x0015ä\x0011~4æmKJ,Ú~KK\x00175¾Ì¸üP\x0007Ð.P)eðí]Ô±¢ÝÔÉÒL­|.Ð6F~Nªdí¢¡^ÕaÆ\x0002QÜ\x0007w´HYV\x001b]ntÇñM]ÔiØ!\x0012«îï­J½¢çX\x0004·y|z½xø?ÿ\x001bká®^7ßöc{¸\x0011ð4tX%Ü>><?K¸<´°Ñ£ü°º¼ºC¯pWw«Ûw_Ö_Á=sÛÛÎáÆÒ<·\x001bË?#sKæÍûÂ\x0008÷^{ûÛÏàö"æòfàÎïfÛ
ØÍ²ÏNìÁg'ìTÝÍm
uw:Ée\x0015ÕB¥óMÝ´^îjÈ9ëÄ\x0007U¿c(cùZ\x0006kþ\x0018ö\x0016!ÔMûøÁ óûý\x0003ú_ïÓs÷.Y÷
ß¹Ñ|hLÓÚëï\x000fô\x0015ü3:g»Äû\x0019Rª\x000bÒÇì¢=^åòLaÄK\x000b½*ÈFØ1Rº2ËfSFêñ3J\x000c¢qW\x0006iKHÛgJ÷
¦Ôùñ\x001c)©\x0006(M#ÈFéKJßGi¹ÆN¸È\x000fsp³â9\x0013Ý\ÊXRÆ.J¸þóC§\x000b9On\x0004Ê0RÖ;¼oc\x0005ýä^å×\x0017À4\x0003¦mÝ¦aV»Göm(OÒ\x0010¤5ì¬id(&îRP&ï APfò&\x001a~x\x0013ûi\x0013Ù£ýðµúMö°YË:Ã*\x0016éCiðK­\x001cÊ°V¥Úß!ª\x000fÞá{Ûõbõõ÷§Ç¯\x001f×\x0010Þþcq\x0005\x000fßö\x001di$ÜÍ±8¶s'\x0011\x000cØPZ#qìL«nn±úpquùañ#·¿ð÷Ø-\x000bµTGogpÃ
¹å\x0017~ÜÑ¤QÕÍóÕ§­J:
\\x001a[W\x0008ã\x0007xîÓÛàOõãâÓæ\x001f/Ïë½¡
JÂÓ©ª³TWi­ç)ÎÊøæÅ8¿\x000bþ´ZÂ«_n¯;\x001a±\x0018XÀº\x0017Ø
"üØ\x0005Ë-Ãaàæõ²×¼¶7\x0013O\x0003HÁcÄ¬óL
8\x0006³¡ïÂõ%®ïÅõg\x001b\x001a_r*Í:¡yÚ«iªfw\x0001Ç\x00128vÛ×HCëA²\x0006´c)`\x0000V­M×\x0003,ë\x001d×»åQ<4ËAÜ&b×XßE\m9Ù»çRX·ÄV¸f\x0000bÇºÐ*¨Öf
1íµWÃ\x000fø6óþ\x0015naXñð\x000cÝÓ~^\x000c\x0017-
,òëñ£\x001b\x0006a(5VÞþþ\x000en`Xìp
gÞÕ~\UâªN\\x001fH`5áºÜ¤\x0011Á'jtÖìTZ[ÒÚNZ+É¡Á}Á³\x001ch45­õèÀÖ©¸¾Äõ½Æ¥|¤×(²©	w\x0018q	áåØp¨ÉÖÝ\x0003Ìö]w\x0013g=H\x0015£¥\x0013Ãà°N6p[åºøsMü¹=\x001a\x0010Glzxkãfóà\x0004b%rCîVÊJ`37\x0006O¯/© êâéõ!ÕÎíIÎ¨\ã\x0014¬d\x001cöûT¤*.ìnn·«»ÛT\x0008uquw¾«ÜH]EêzH5JL*\x0003*¤æ-C]£àÏt3Hê+RßE2÷H\x001d'tµËb7HÚ\x001eÖ;TÊTÊ.TÌÈYBUTÄ\x0007¿¿ÃÏß¼]LCU5ªêB5AäyÂ*¶ùOÅ¿¿l\x0019ODÝ
'Ôt\x0003j±\x001f¬ºíu²ú\x000cq\x0001\x001c\x0003ÕÕ¨®\x000bo<ª1)¨Na­êæù5
Uëj\x0001hÝ³\x0000ð$ï\x001dSÛ.èY;b?ñ\x0011HCM\x001aºH
5mQá\x001fIw\x001b\^ª¦\x001d\x0014LC5±úýñÏé¨^ùüó;27\x0015\Ø=Æöè§i¤VT¤øg\x0007)XRe£:õâÔR\\x0018©\x001do.©¬Ie×¤\x0001\x001bRiQ®¹4n 5íNÇ¤ª&U]6Ån\x001a"«®äfÕ¢0_3\x001cZï)Ûµ§| :\x000bØS[ÜL¤8\x001bü9\x0002)LUQ\x001f\x001dV)Ëøç<¯ÀoÑ¾]ÄAé<8\x0016×­?¡e_\x0000qÍ!aK[\x0011.\x0016U\x001b)~ÚHó[ÿÍúþñ\x0005»\x001eýºyØÜ?î/\x000cÖ\x0004*Ô\x0012ÎpÄ*\x001e
ë¡u/Èý7Ë³Ë[lüøau¾:»Ü%yIàª\x0002WsÀCr´Üsë\x0007\x0004\x0007,Ü¢²Ç$×\x0015¹Cnã@n\x0001È\x001elÞ\x001c-<F>Vª0ÜÌ!ÇVÇ\x00038f%Y\x001bx¢²Í{o7¹­Èí\x001cr(0,ó<hÂZá·Ë|¼hòb)BJ\x0004O!å?\x00079lÐÒ\x000fÒ&ÅOúù±\x001e>óC\x0010Ocª1·NüÒ7Ó|½üæ;~3\x001f\x0003:\x001acµgY«Ê:ÉõüÊ5UYúýÌw_@Ïü\x0001°d \x000cîÆXv7vp7ãeh\x001d_@|÷\x0005ÄÌ/à\x000cUv×ñ81/!1xx_@©:[¬R³\Î\x0010¦NÊ\x000fO¯¿§Ñ½\x0011$A?	KÉ g"· \x000f_I­\x001f®î.v¼\x000eªäT=àZ<µIy³\x0016Î¡Se,E<	Ó¦Ëaè\x0005\x0011L\x0012'\x001c;lÏÑ9@å¸¤_þsßO\x001f©{\x0006\x001d\x0007ÿôQG\x001f	&¢¾Ô¨/}¨ZÃçÙ5ÎDV>\x001c\x001dW<\x0011u]£®;­Ê+@5¬Úl\x0006;\x0014U¸XË[à\x0007[yÓ§ûß??§/±O¿ËRñ²¨\x001f£HcÌAMh6	fQÓ«³÷×ã\x0002"\x0003¤)!ÍtH\x001b¹=ÍU\x0007­6v¦8e¹\x001bR	UÏÝSi"ôðBxñôøò×Íëó~eK¯¥"eK\x0003g,M\x00084ÂÓØ\x0012Ê2ãï\x0017W·?¯î®wõ\x0013\x0013¬-am\x001f,Ü¥=±*l,J¬T\x00045jÌ\x001fÕ¬®\x0015_S²NÂòGhÈ³Á°ë¢\x0019Ä\x0007Û¾¢2©/I}ç\x0012\x0010y\x0006\x0007<Græ°\x0004\x0004U#-PÂ>Xaé	\x0013Ö\x001dÖ«£ñ°\x0006Å\x001d°±]°8=ôð\x0008U\x0011<xOÇö=n2«¬Vì\\x0006Ve%~µ$LÍ¤¨ÛÉÕëUVK@v®\x0001C\x000eË
\x0012ºÂ9\x0007T4\x0002W\x001dUD\x0007sV¿¾ìûùq:  \x001fÛ}sí¾Â\x000c¨m¬¨Å»* \x0016J\x0013Ó<«¡2dUG?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-15.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-15.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001dÅ\x0000²qÎ¥ùúöö÷Ä\x001aáçÿ×3Dp8\x0013øþhÂãl:\x0018y£¹ö\x0008\x0017ÆêàðçoN§´o\x0008U¨¢\x000bÒ\x0011\x000e2\x0014\x0014&3¤AÆkcÐvP7\x000f\x001f®ÚË)KNÙ·¤Qw\x000fh	sÌí2LC*%jÚT¨ª\x000f\x0015´QUA°\x001b?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=zròêèÉå¹k$ÓÈù\x001c{|!$=o¾»½î>:ZH§Àar
²ÿ
Nmõè=?9úîÅY\x001d\\x000cßÿþéÞn\x001cYÙÂ¶>ßÜm¦P ì}ÀÉu\x001f6¿#B´<6à¬Ò4\x0008ßãêÆI\\x0011÷«Ó´Íó¿å\x000e''«!J\x0014QQ
·%àxi\x001bD°Òx<ÈÈbm*è¥è\x0015, ÚÂ|\x001f`	Qã<\x001adQ\x0016MùhhZ;|@ÇóGX0y\t¡þµ,àî\x0014í¥%ËT·\x001d\x00114n\x000eÎÔi\x001d·ZG\x0001Ë?®¼À\x0001V~ÂÙü<7×\½¿§7×N£Á¿þ\x0017¾\x0000\x0017Ïvp.åÚ¼E\x000f\x001a#ÌÇ\x0001.u7ê1ûÝo5åÛñý×Â\x0003Iuñ\x00045
öM8Sûf\x0010V-ÎîñîÂXwáàP"M<!uÌxB
ô!\x000fï\x001bãOmºx¤<¦¯\x0005Â8\x0010â¨´3\x0019q¨S{\x0010\x0007>µíÂÁ}\x0015ÄãÓp.àñ©=\x001fyÄ*í\x0001ãºxDdí\x0001/Ox¤c°\x000e§¸4p¼%\x0018%§µÌAÀAgU6\x0003'ëú·?þ0¿\x0014'}òÇþ#¹có\x0010Q\x0019ÜÍ\x001c\x0006\x001cI\x0012
iwlpÆB'×\x000b=¯£\x0016tº\x000f3\x0004^ºê-Æ\x0016¦cmé\x0018iÏKú\x0019Òn\x0003f"\x0013Ñ:5+\x0005ÜFgÇ¨¨G\x0019Ò1nM\x0001]\x0003X\x0016Ïæ-³ÅåmÔ§<ÀÎn\x0003C F\x0002~úq:²p\x0017Ñ\x0019Á\x0016Qt\[Ä0]|I\x000cÙá¢\x001bb°Þ2.û61´\x0013Å X\x0008 õ1\x00196!¸t.µ1i\x0011Ñ$\x0004ÍB\x0010ÃBK ¶
!h:Ô7r\x0010ù\Æ8ÈÀn} àO\x0018´ÅDdCäoaÔè·À($
\x000f\x0005<X\x0005}\x000cÚE\x0018þ\x0018ü¦h\x0013Ä\x0014è\x0006\x0008\x0015X\x000ct]lFÍ4&dÄVráé`
L£$1xÅ:é¿\x0005\x0018HÙl$-\x001d\x000c¸85_\x0016!¨\x0007`\x0004\x0002>¢l´.(ÜMçI\x0012O§¡)>\x0003\x0010`#e£´Y!äT=@àã©Fo\x000bôZe£tÇ¬*=WP\x000eO§\x0016n\x0001\x0004(\x001bMeH%màJE¶¼ \x001cø[\x00085zeáø/Ùh*]
Í \x0004K!X\x0000\x00029|a¡qSÍ6J³
\x00177Í4\x001f¥à¿*P+ñ?[>Kñ=\x0014Å\x0017\x0012ù1¬\x0015²|Äv^àÅ·¢ ;H\x0002\¨or6\x0016¡ägá~¾w»\x001e6G<ç\x0018´F¥Ò^ï£)à\x0011ðiIÀ]Î»\x0016k_b¡(\ì\x0003\x0010pyN=>\x0000¡P&\x0013Kùø\x0010Ü®6\x0013\x0014\x000eö!1èÔ÷\x0006\x0004&Òí\x0001bH«\x0015Q\x000ca\x0018¢ð°\x000fA§êMÀ[$\x0006Í\x000cZïfÂÃ>,\x0008Ï\x0008iÚ$\x0008Çð»»\x0019¢ð±\x000f\x000bÂ\x0004\x0001g4dIhPq÷.o(ìC !(	F<I"f\x0018þ\x001a}H\x0010|;ÆÂ² \x001c\x000bB]\x0013Ñ\x000cQ8Ú\x0005¢\x0001\x0018	MC¸'Ad0£&¢ò´\x000f\x001bª¤ÁE4Y	Â\x0010Ã£rµ\x000f"bâÃÇ% ²NèQ3QùÚ\x0007(°Ü´BH¬æC
)(\x0016Ðí\x001b¥(ýí¿ìæ¨\x001cî\x0003\x0014àNÈ$\x000bø_º:¤¡Ã\x00181z>*û$Ä1Ô\x001d\x0004éà]B\x0015Ù#\x0010¥¿ýÊã>$ªKÓõ1MÅ\x0003:$V]\x001fÏý×É¢ôº\x000f\x001f@²!­ö@½È\x0014úA¢\x0002çèªF»ùçÉ¢òÿ\x000fËô"DN\x0014æÛ©aÃ\x000fIÕêgþy²\x0000£©Z
§ÙÊvúN/\x0011iwßçÍ\x0014xýe\x0001RµNKDHK®'ßbK1,\x000bJüþÅ²\x0000»©Zm§KB¥åzs!ü0\x0005\x0008Qýå¶\x0013§ùªFÛi\x0015åvÁÝ3ÙÝ\x000b]\x001cÜ8F\x001bct£Õ²6\x0011ëp¤ØD\x0011Ó
v \x0008fÔja©n´\x00176ð³0ÀCD^ÐF[ ðÃö\x0002®n<©n*¬M\x0014Sa¢\x0008)\x001eäâ)à\x001fÔgÄ)
§ù ÁvFv}Éé´¼êb\x0002\x0014J7j'¼@\x0004;à6­<CÈ²ÐaÔ\x0001Çd¢iÔN H\x0010>*ì&\x0008V\x000båFÕ\x0002\x000f¦Q91¾_ïi\x0018%P(A\x000e\x001f7\x0007PbFåôÿð?]p)=ËBË\x0002\x0014Ó4*§\x0018Å(pë\x001c©J=/ð\x001avT\x0016\x0016¾mú"\x0012ËZ}:"6d÷Bá¤Bób¯\x0001
\x000c#5}\x0011{ídú"ÖNæ\x0013RdÀµÔ£\x0006\x001cI¶é`?;ZíBécô\x0002g$©õ}\x0002ðm¹\x0000
¿nDAïCåÕ\x0002SZ®ÉZ\x0000DL#\x0001\x0002lV¤\x000f¢#S8?\x001aSÃ¬»kTN\×>È40;½\x000fá#¢l\x0018=¨\x0018%vÊé]ê½\x0000
°_tà$X¢0\x000f²Síoåiî
¾ñ?[¬\x0006|äp\x0005ìÿòt½+Ïá\x0003#FO4\x001c1ÛÄ\x0001Éàà*
§hMr	óìwé`GaDL0±ez'y%Øì÷x¾à{PyÓ\x0018H,ºEHª6\x0008\x0012Ë\x000eù\x001bXð-?"é\x001bµåÏ»Yb±_\x0002\x000ceÓ¤oÑT.æñ\x0015#<ÃxÎ#
g²Ù3J³ò¶k/ÜÀ^S&æCÌÁsïû¬î\x000fööPVíòüÍç.&<£
T
ÖÖá\x0016rÌx:ïÈ5¼\x00115Õ\x0015òä7ÿÙB\x0005»m(Úp\x000c=âõ\x001c\x0019­îär
£Pql#J#ñ1¡Éæ"
ÝF¼§aêP\x001bI$åÆ\x0003<©¸X\x0001HèvqÍ÷¡\x001aÔvU!\x0014m·(XðÒ3+PRò«\x0015E\x000b"º´A:`v:²TÄ
©ä\x001eFH\x0014AZÅÕ¨Î\x001bRÛàË÷o7\x000beÂÚåâè\x0013¹@Õp)Óõ6n\x0005
·³4k&±\x0004CYk\x0014\x000b\x0019¸8Ù©a\x0016Jµ±`\³\x0002%Âòó«*Ïì&¡ÄX«T\x001c\x001a¶ÉÜ\x001a³^I*t\x0007E^ó7ÆB	²F\x0016\x0019ÈñÇ­\x000cÜ\x0000ÅbËðQ7\x000båÉZåbÒ\x0002
`±B¸§åâÖ\C-kK¤«9`9\x0012¡°\x0010Å*ÓB\x0019³V©p&\x0015^¤YÁâò\x0017
bi¡¼Y+N[ý@*ð±\x001c³P¥wû£(<kEñ©î\x0000þÚ\x001d3ÏßG¬p\x00138ÖJ¢ð©:	Ekzµ¢P$±h½BY8Öî³$W;h»U\x0016Zú\x0006,V­\x000b%ÓÚ%²\x0018](®!\x0016³J[¸±Q.âÓ¸¨'¹\x0006S\x0002KT+9N¬µ\x001fhfÁyb¬/o\x0014V p[e£X\x0002ßD¸\x0001"ãOû©àN¬â³Ý,ck·þT×\x000bnür\x001az"î^ÁB¶F\x0016\x0013ØW0\ø(<×¢«\x0010W\Ðnk×\x0016º\x0014q\x001aåKÑó)òkN\x0011nÅÔí6×ú45\x0000Ä¢]Zg\x0006ráiÊ®p\x00168\x0001ØíZâÌ\x00056tT¤\x001bEUÚBYÀöç\x0019]\x0000\x00068\x0005Ä%"iÇÂôÓv««ùÕêóKÄqT\x001bó¶k\x0004SÅ8Ú/¥\x0014gÿá \x0017ÈÞMk:þáoþþñE ãéOW\x001f¯oh]Û7·7÷´¯m!ãß
½K<C)îÿ)ß%O¿=}~vAÚ¾yqñzÏª¶
-\x0005>¾H´TýE¢¥\x0018M\x0017\x001a¦»)l\x00140T®\x0012ÔÂ\x0012^Vr\x0018-kRKõÓ½RãªÀ0íq¥Ä¨¡+7`Xr\x0014íöý??üíÁ\x0000OG'×\-Í2À¾ÈWr¹ÀD\x001bvì£Ð\x001dÿêèäì¿\x0016\x0013V(åìC(XÃË©\x0005Iù\x001fy\x001fÎ-T!^rlÀA\x0012tYL¤ð,ÈD±\x00015îA~\x0007I90à\x0010´\x000eYSø\x000f"9Î\x0015V	¥\x001c\x0016pPSà·¨Å9T\x0004ÄÍ×ða\x0005J9'à TBv£\x0008tÁÁaÃ\zÍ\x0007JG»Q*FR§c°!P¡âÏ8etÇIÊi\x0005"ÓÀiæX\x001c<6	Å)\x0016©â(ÕXÃ\x0007H\x001b\x001a\x0016\x0010p]IL,QS÷L\x0014Ò¬°*9ú×ÆbU¡XIQ.\x0019\x001dûóZ®øB9àÖ¦,R¥J¥`ÀÂp\x0003¥X~N­ á ×_NãJ9 <®ÝnWûm¿úþG¼\x0011l¾\x0012Áæ;Jsh
£H|rö§ìpi£ùÇßý \x0016]ùwW{æo\x0018nÌ\x0003áä¼å"LÂñrÉµzyyºÇ­Ú"ÍøÉ\x0007B¾¤áæf/\x0015¿\x0005£[4ãîAÒB[\x0003þ\x0010É#\x001aæ$O\x0005;Ì{©ÇfÏýHÎaéYB2Çfº¥¤ÆèUBe\x0019ñ\x0010RÊ$v|8o©v4X%"\x001e\x0010pq¦#D­j\x0012.T£\x0010SÓ­	)*
Zª¸VJ+êaò8Ü01y*½ÆÚ\x001fv0¢[+'ÊÓ´3\x0019a²6\x0005Ëú4X"i\x0013.g]Ã4\x0005(¦\x001f=PÜ5\x0000\x0007õ	 XPFûµP\x000e¡\\x000fÄ`fòpJNÁÄÈ-q§î®ÑrªÈI\x0001¢óg

ÏÁI\x0018ùü±EÐS5ú
2©qz*páÔÔ\x000e}\x000fõSÃC
ÖG\x0013\x0002[÷\x0011F*ø>*öÍgrgÁSÐ¬ðrñÝÞ¬[ß¿OÚõ¾G½°\x001c0k\x0017e\x0007cô[íZ©òi6¢f#vH\x000b+¯ÓKÄ\x000fEãÊ¥¶¨^g³Àk¸àÒéâÂÉ§)ÖáhJb0¡´Y§ðø
ß¥oø®Kµxzã¤ð©}ADÁ\x000eÌj\x0007¬\x001f\x0013Ö=\x001e\x0003\6U>¤!­àÄlN¥[
ðµs½M\o»Ì¼H++@\p5zòd¬ ç±Ñ½v®«ÄuÕó\x0019ç$üÉÐÃ£[=ÞWÜ$ª\x001eÇ		g\x0003KK\x0006*KÆ©!Ãµùý\x0017ó~ó Ø8
TüöêîýæÇ=\x0017P<4M\x0005K$kòÇjA©øíéå×'Ï\x001eÌ+=H$]\x001eX\x001aòÀRG}e8\x0001sn@h\x0007Ñ¥\x0007p³<MK
ÓÖ	É±Â!¡+ô`jéa$|¤Ø5 åYñAt©èÁàÒD.åJFÁçÏö`
o'ÑÑ¥\x001cÏé&ñ&E½\x001d5»RHeh²
ÉHJgORR+\x0015<xK=ãÜIô` êA"/K!q\x0019©áa¦*Ä\x0007\x0011>$*jí@²²Ð$KU\x0019²8më>[®'í@\x0002FNLT ói3\x000fíß-½\x001bB\x0011\x001ak\x0003\x000bÇ,*p]¸úÊÆÈÏ\x0008ë\x000f?ýþãý\\x0008èÓÑ··¿/O¶/ëÒ\x0014¾h¨\\x0012\x0018g¹á^\x001d}ûâoË1²-
U¿\x0018\x001czîú¹÷WP\x0019óÛ
3NÀæèÉçûû«»ë=IZÌõQ¨æ\x0012\x0005%-w\x001b¯gôûäèÉ×¯O/Ïõ¨ªoÝ\x0016(Ðg©¨o5R¹RêJÁFPõ½Û\x0002¥"Odóp½ÐÄ\x0010\x0019E}\x0010\x0002îª¯Þ\x0006(©bêûvÜf¬\x0015\x000fG³zµê»·EN8;O\x0002\x0019q\ÓÍbr3N\\x001fS}Õµ0ÙÀCä\¹×ÔÈ¸VPÕêöGêA\x001fkúvÜÂgåCÐT¥
Û°W\x0007	 ©4OÂu/k¡ªa#Tàvåà§*Êð|\x001aðëf\x001cÌ>ª*}ØF\x0015}Úä\x0002TÒ£Ê#áù¾Á>XäÒ	5Íj~tÎ<×È\x001b«é\x0014<Ì¯ü\x0006+\x0015§\x001f]6ÁóP4\x0016'\x0017U\x000f'ÕêK¦êZí2ë\x001cç\x0004ÉlÖÎf}Î\x000bn`³WïÝÕ/³·2î0ZÖ+)yPÁ4F#\x0001iÁ¸jk\x000e\x00087\x0017µÀÔ¯ò\x00030"êl\x000f°k4Á¨ÀRNÎ=¤Úav]\x00030§²\x0006\x001cþ\x0012\x0018&\x000f¿Y%ÝËw?\x000bÜrmRû\x0002\x001aÍ\x0003>æ/Vúåt%H\x001e*\x0011%êryf6\x000fr÷\x001d0¹Û¬\x0006\x000bêhL)XëÈÎ[Î\x0019æ·½4?þtw÷ËûÝÃôùèÍgøûöÜ\x001cé~5Ö>tàkí¼9úæäÍÓ\x0017\x0017-\x001cÅ9:È¤I[\x000c®Ì³¬-ô~P=ÖR¢\x0006DCx³uÏ´6<jB<xc÷ \x0014nõa©`´P¬J»ÐPSx\x0013Xá»­ÚQó|X*>\x001f!#5×ªê<fB\x0006µF*\x0013}\x0018EÚ<\x0004>Ppdÿù²TâÁ^¢\x001e"pu\x0010\x0005Ôjê¼F#tÅ8ÊÃ\x0007i\x001eÜÛ=(ÕÞ¼j«³®¨<\x0007D+¾äÌ\x001a´vÂÜ\x001e\x0016
\x0016I¤¹cZGj×QVry¬\x000fæ5ì,ð;$\x0014ë©N\x0002´VQ£Òù\x0000É°Biwö÷\x001d<@y\x000e\x0011ï ÇtK¿ÆÂUÃ,!OÓÁÑTÝ­yLt\x000fêc{PÊÂae	&-\x0004\x0007\x0014\x0011hqÊ\x001b0\x0019»F[ÊRÃ,SaF\x0012\x000cö²@Ï(¸­\x001f\Ì]r©&4ÇFì\x0002OgIó°6\x0013yî\x0014ý7ÀæN_ã\x0012Öi6ÄôãüêÓÑë»ëÛûåÀÇ\x000ec\x0004qÂZÎëHU\x0018.Æ²ïùüôÕÑëË³\x0017¯crò\x0017÷_ÊÕ\x0007\x001c!ü|ôô§ÍýÕæ3úRçðOý´ùøóbá¡4Ø¬Åuà/I@¨ì\x000f\x0003o~{òúôäÍäZ]Àÿõüå\x001eÖüúóÝ?æSvÿú_?~¸þ´§"Ýé\x0015l©ì\x000fË4Ù)7a.ùsúìüìÕÍ\x0011\x0005ÒÌZ¿\x0003H¸è&äy$$ÃÎµb%ÒÌ*½\x0003H¸$^.JQ!\x0006^ä\x001cW±sQÖHï®oÿðïf+H]}úùóÍ§ÍÝýÞ´\x001d\x0017ï«éÍºÓ8\x0016¥¶3)ég§¯^¾¹xurùºk·\x0013¬ËJ*DVÂS#ð\x001cf×>µ[ÝÚåø)ýU4YJxÞÞ\x0003`v¶È§\x000fl·\x0007¬I^û¬°	Cpåmþ"±ÝâÛ`X2\x0007É)\x0019¹ü\x0008§90X-?j\x0000s\x001f~¿ý»¯{8}·¹þðáêþ~Oî,ª<÷	ûVè[:\x001eÃ\x0018å\x001f>=9;??}ýzù¡Z=(6h\x0002óØ\x00181Õí¢)C>?å\x000e³¢\x000bìA¿\x0005,D\x0006\x00131n«½ãC\x000b\x001b8{À\x001e$Õ$¦)£&=7ÛÀ¸ÿ1,mMíázÇþK¿äï¿ú\x001fõÃ
OGO6÷÷{VG	,\x000b\x001e\x0004çû-ÏaW]iñxròúõ¾õÍ[º±ï\x0000\x000cøSÇT
\x0001n)/K´¹@C=\¾ÛÃR·ö\x001d\x0012\x000c.»"\x0018')f\x000eÉ\x00155~®a«\x001d¦nî;$\x0018iÐR"\x000czépÙÈ\x0011q¦Ó¤\x001d¦nï;(\x0019O±h«¬¢Å.¸«\x000b2ªí\x0019ý0u[Ý!Éø@E3íÞ¡ä¹¡É\x0007\x00167©­©\x0013x
øüO÷ëû9î\x0013<\x001b®nn®~½þ×ÿ¹[lTÂCî	k\x001aÞÊºÌÙWïÔò
\x001e\x000c§\x0017\x0017§ß^îéX*ðvÜV¼H1\x0002,zW4Ær\x0000ßUy¼^¸«¿_üý×©D\x0013Ç·k_¾¹°#üêæ÷EWE+N\x0010ãòb¾(áÑ4ðwÌ ½ºÁO/þÖ\x0004êFË*ü\x0006.Mû\ÍWsÆrf=ÖÛõ¶\x000bKÓìæà<oô\x0004.Ã%Ür¦â0Öß7pû\x0016î¸XbúO÷'wÓm»§ãVhJ\x0010;»íÎó\x001c2õ¦\x001a[¯÷'Ó5»¬Mêï¿ùõùxzuýãÍõÕ>EwðDr\x000f.àKSF\x001a\x0001åÁnÎÕ!¿::}}zöìb¿¦3\x000588ÓÏN<«=\x0012\x001fÎ¡7äô\x0015¦\x001eç\x000bzøv³²½"ÄfÓûÔù8Í\x0002BFEwð©Ã¸\x0008õ?o}él\x000cOL?ÎÑ¯ûùúfoß\x0002\x000fÓ2\x0001þÒñKîf\x001bÊ~Bðå^]~õnó~óéþnaªI~\x001cdHO\x000458\x0008@y.ûótïTcÓ3D Ð@¡(6m²à +È"ð3
8,\x000bÓÁá>üí÷\x001fæÏÛ¡>áHÛ¡d	\x0018k²Dr¾ÞÿPkîõûß~úáéÓàlüèô\x001fnoÞï¹|ñ-\x0012Ò·\x0011\x0002#>É]Rì\x0013©54C§ßIüzÃnôÏ\x001f\x0003_WÓó«£'·ïÞ_}¾þ°$\x0013¥ÒÞm\x0017\x0003ö\x000eÑx3\x001d)m\x001fq»¬+I¼xsùõé³ó­¶ò_\x0010Êý»\x001býF\x0014t¦\x001f(§»}g\x0018î\x0007MXì¦MÜ:Pß´Õ\x000cG\x0014ÉÓK<¸K\x0018òýoñöCáã7{áýô`?$Ïõ¾Zþ\\x000eyiÀHÖ\x0016\x000c\½,i°
n\x0011Mí8ÿ¢ÜÝñëÏBÙ«Êç\x0001ý8t{\x001bp*4µÉiFÏÔº\x0013y¥ª\x0012\x0001 \x001d|o/a÷ww¡pÄÖô\x0003äñì\x000eÜA°ð{Låõ$r[Zí©U\x0007w\x0017Öâxv|ÀE\x000eñî\x001f~ÖSéÃÒ)tôÛÛ\x000f\x001f®7Ë1vs,\x0013\x0007ÍÊM¹E\x001e4j«æ|*Ç=??;YÖR\x0006)oè&\x0012\x001b©¡×\x0007\x001cÕK«b\x0013}$W?ªßU,A\x000bB.Õó
øTÇ68ëS:<Xì1FEõQêÔW\x000cÎC­¨ñü\x0004\x001cªe·2\ÿü2}v±¹{{÷y³¬¤Jñ\x0012\x0017¥¤a!Â±K\x0017ñ¡\x0011.N.\¾9YÖÐ\x000c °Àzúq\x0000ó&¥6à£J	©xH½\x00079\x000e_îìû\x000f\x001f\x001bîÀ FOkp\x000f\x0008\x0016¤(¸ÊÑùrâà42îà¿x;Qoÿ¿\x001aþ°ÔÙ\x0007^\x0001\x000f\x0018ÄY®ÉXú2«¼÷ß|/¥¼ý	Ï#V\x001dN?.6¿îUm$íM²JKîÓ6Ûè)ëª.N¾kú×cõãWÓ\x0003ÿz¼µÓ@CÐqLQ)C]zÎràûoï~º7:5`§ök4/ïþõßû®5m6Û·Ìád\x0016n$®ÂbÜ\x001cx`ÛÆÀ`ÆÚMc \x001a;74zÁòi×AÀ=û
\x0004#\x0018Ár\x0005\x0008\x0002É\x0000\+×Npgü?~Ç\x000cBîé\x0007\x0010\Þ¾ûiÙÅvJR
-øÒÉcQöyplk\x0001\¾\x0000·rù&\x0010¿½ÿãnA	\x0018ÎF_}|ûávÑ\x0004ý\x0003_ÒØ<o"\x0015\x0018J\x0019y\x0010·e"e¤O?9±Ç\x000cÃ\x0003Ô\x0001Úþ¢Î\x001b\x001e¶Ên­"ÏMZQÊ\x001eÌÕ|?r¶Á%S%êÓpi¤0sÓ\x000eäÔeKÊ{¦f{ÛÙLÉf:Ù4ârx½Zú ô\x001a\x0003á³-Àíp¶³}p2PÃ`JJãKéùºµn6·ÙÎæJ6×Çfx°+°Eè3ÝÃuÀ¶VãB	\x0017¾¬ã EuVÅ\x0017FW\x001dVÙwZÿt:U\x001dWÕw^ÿ|C¡U\x0006¥\x001e\x001dÓ`S,ågó\x0010pIÐ\x000bÊj;\x0017ýhAÔzç¢\x0007#¥ÙáípA«\x001fnÙ¶ýrpr¹\x0019Î¢c+µÜIñÁ#â\x000cC\x0011\x0017\x0017§ß¼hS%êÃ(Z Sø\x001aæH\x001eÛ;iv\x0013[½pºÓpB|\x000eë&hµ\x0017Ó\x0006ÉíÖó÷ÂÙ\x0012ÎvÂ)¾)Tn6\x00008
\x001eÀkm·_¦\x0017Îp®\x000fÎð'\x0007wW\x001eHÎ;%½xP
Ð\x000bçK8ß)9A«\x000cAr7«ÄÀçA¹uh¡D\x000b}hz,3ÉÍæy	ðÚ"ÇIÝÙp²6$=\x0004+¯\x000c[9\x0019\x0004/0rNä¯º[üÝKWY\x0012ÙiJ\x0014\x000fÁw`5xü\x0013ÔqçßZÒKW\x0012ÙiKÀyJ)\x000bø²ÇÖ9-øËúÝ±Ò½t¦¢ûÿ{»äºn$ßw*{\x0004\x000c ñ\x001d~"eZV\x0007Eª)Q]Õ/\x000eÊf\x0015G&«(Ñ§ªÎ4îÛût{\x001c53\ÈÄ\x0006ö^{\x0013¹tÊ\x001dÑmv\x000bø#È\x000f+£Ë
\x0002´î²¿n\x0002½V\x0013·+¿k§sZ(tÇ\x0016gËmQ@¥Û+dÒuB§J§^`=/\x00037¦1¼'l\'ÃºS:-:ÅýÕ3ãl1\x0017i U>Êv$¤tØiÚá3
y&:\x000b1
q^Q"¼2»YçB:èÔ\x000edj\x0017ªz¢ ö®q¿¬ÑëNèô\x0004dz\x0012}¢N\x0013µ}Í\x0008J5Q~\x001d]èè.ÙrÄº©59íÈ­Ë>òns¤Q:tï\x0010ç_°CüýÝï·÷_6\x0004r0 ã"k>ä=Qr©°Àõ¸ß¡üýéå»
ýæY4hÑ@\x0016SÉ2ñ6\x0004Æ¯"´\x001fKëÈLKfþPFs-ûC¡ù\x0016ÍÐ0Ó³lRçùùWg­££Ë\x001a¿\x0014+B\x000b-ZY\x001fU¦@\x0013=ë$Uc9f/¡PD\x0016[²(#\x000bT\x0001äU¤ÚÌq\x000eQØï "K-Y®4\x00158\x001eÍ\x0011q45_µÒ¶.Ü$jVÆF!Íì£+ °TCaÕ:^Òd-'JÉ2ÍiÂGá\x001b¿ßLPÄÖ\x0019
dFÃÜÑ"¸ÑÔD\x0000­©Ú\x0018sÆörGEltL;¾¹Ý~úr÷¸c;üÍ8"VRjz?5Ó,Öã\x000c(\x000c¯¯³^\x0017#B®i\x001cÝ\x0015ã\x0010	_ÌaÓ\x0008J¯³jh³ûc\;cèâáþ/{¤¦°\x0014Xqã\x001aU§Í&.¥vÞÎ¤»_\]¾ÄLÜ£\x000fZ>òyn0\x0001b|BÈ]­ü~[+) i\x0001\x00140ßó\x0013\x0015=âXpÊÁÃÉ\x00028Ó3F
h[@+þÂµ®v\x0002¤\x0018oµ\x0001]Ëç¤|ÊQëI,À¢\x001e!Ê\x001bÍ½ÂÌ(\x0018\x0019_lùâ\x001db¹Ó?©ÓA\x0003§áÌ5ñ¥/IùLâ²òn\x000b\x000f\x0016TÛ<¡\x0011P"ÀæÝÉ¸®0bpXQ\x001fðRÆ!);4z³×@\x000cØk X\x0004K©dél4=µ%ÈÕÞ¨Õ
j±\x000cL Õq\x0013Êp\x0017½¨¢\x001c¯Ó@-\x0016AìúK\x0006L¡îáªfwãÙrÀNc´Xd¦\x000c2üÖ£Æ\sí\x001dÌÔ.I\x0000Ç\x0019\x0006í9âq\x000c2inÊà|\x0019\x0015,\x0017¢´V©\x001dø\x001e2ÿB\x000c\x0019ßMí\x0013©5>Ï³Îÿø^sQÈ\x000f%êc\x001dß(Ï0ê?b"ëõÃý/×\x000fO?ÿz÷x¸
Érç~aÑâ\x0010Æmqlãy\x0017çë«Ëï7¯¯n^üx~}¤D=\ÀaÕ%\x0015AO¹U¥Åâ6ùùê«±\x001d*\x001eØ²Õ¯[én%x1R\x0011¶\x0007)78P³¦lÜ\x0005¦ËNôÎ\x0003rþEß\x0004ïíÝoG^}v\x000btÉ\x0002s\x001a¨@E{K.ÌÌCì!ööüõ± \x001eCA\x000b\x0005£Pø\Á%²W¥°KS©½°Ü\x0002 î\x000fI\x0013`\x0016Ë\x0008°pÑS5;6)àFÞÜd&Ýv\x0011m±¬\x000cËTcyrÕVk \\x000båÆ¡¦Ø?ÛÊRî{^m\\x0002Ìvñ\x001dÄò-`©Ú#Ö+¯í­RÜ/´\x0015`\x0016+\x0008vaò<TÓ\x0002yq:8r3³xÅÙV~T±¥\x0002ca¿C6&ÑR:é£­f;\x000c\x000fR¥*	¨¥ÄAN*Wó¥¥\x0019m\x001ckëOBª\x0004\ÞÑ]0bë²:\x000bAUsÍ7\x001a\x001eäê\x0005~Xá3\x0017vt£\x0004wÏî£Â­¼MÓ
×ÂkÄGgéf:YÊëò}´ú\x0012{íÝ$\ÄëaG\x001fÇQS\x001cýnEãóÕ»IÌMF\x0018Æê$^\x000b4>Zwâªµ\x0014YËù*ÖêD^\x000bT\x001e»R\x0006òKqî\x0019>ð^\#§ºSy-y\x001bø+\x0006àf%[sÅ´\x001f\x0016\x0014`u*¯\x00052O½ã§¬b¾+c¢\x0007ÀÃWpu:¯%B/ÌÅ\ÎÕy@u\x000eypk¬Õé¼\x001e\x0016z´VÜ\x000eW'`ÉZµ0ìwè\x0018çNèA$ô®qj\x000cÉsxLµ×ó\x0007:\x0007ÎÛ½\x0008½//QzÏù½ù^1½y\x0014sq\x000f\x001bJ¯àê\x001e\x0004J\x001fóuöb>è2\x0014ö¦4Õ)=H\x001eã ¦6Z"\x000fÕÅXµk¾	ÿ W'õ0,õh®ÀÎ \x0015´d.*5bª¸\x0000«Sz(}^R6#fÕmf[ÖùýÜ\x0000\x0001U'ô \x0011ztâÉXU¥9¨\x0018f{R
cu:\x000f\x0012÷<2$\x0002ÞeÉX<\x001d\x000fçY¯áê\x001e$J\x001dSOuãÚñ¹ÈïîùJ6?\x001a`\x000cËtBoDB\x000fÔ!\x001aÛZ¢sOBÏaýfÈ\x0012®NéÍ\x001fFéM§ôFèÓ§TíE÷E\x0017¸!h¶×
çÙôa\x001bÒ\x001bE¯8ùïs¯Nì
\x0006½jyuJo$Jß\T Çël.êÝÂýÀ¹«Sz#Qzã¨»FÀnT\x0007û:½vþ\x0012¬NéÈ§×ôÒGø¥Æ9§¿Êêê´ÞH´\x001e§æ$2¢\x0016{:\x0019Ãï\x001fiÿ	NÀÕªj¶\x0017½î§\x00004!sñÜ\x001c¿Æ\¶ÛV²\x0019ù&\x001bWÔ4X'Ë½9|k\x001a<Õ-z+Yô\x0007|%g¨/µÆ*l~\x0006\ãuÙnqYÉâÂ\x001e½ô\x0011­áxDr\x0017\x001f92ÈÕ-.+Y\©_°²Z\x0018\x001a ÷nÍ	äºÑ	^3ð"ËXù`d,¿}\ñ\x0015]·ædÍ»Èò\x00136 çGo÷ó÷\x0004\ÝêrÕå5zÌ\x0013\x0006zZÆÒ÷=°æíÀu«ËIV7ü\x0019§§¼ÅÓÑ¼Y\x0013IõÝêòÕU#¼\x0001³ÍøÊèk_EXc.ßihWò<uoz\x000b
ô¸Èþ3¶\x000f]ÁÕ-//Z^½D\x001c\x0015Aâ\x0015Ì6½g\x0005V·º¼du\x0005MnjÀNQWðò±Æ¿	Ýê
Õ\x0011(ÇÓ±È=°ÝÜ
[N¹D¹ær¸)\x00135Ô¯-.­yÆ\x000bÝ\x000f%½d,g8{\x0016ã¾Ä\x0015×`õÏx\x0015\x001fëq\x001d­âZìEs«¹QÁÃXÝ\x000f\x0015_"6\x001d
ü\x0015Iç\x000f\x001cãÝ%\x001cç@ã\x0008>\x001af3Itá½±$\x0012®nÕGÑª<r\x0012'jêv¨\x0015gî\x001e\x0018c:ÈÕ­ú(XõØ6\x00045ÿ\x000f\x000f\x0011
¸k·SÄÕ-û(XöÓ©csü2ãõ¥×¼·ÄnÝGÁºOµ_m\x0008ù,¢ÉtJ×Ñ¡j?ÿu+uë>	Ö=æÉÑ<©à\x0002Å»@áá¡i¿nHÀÕ­¯$Y_¡êÔG,×!¨Ù1õÃPÝâJÅ=SònB¾;jæâ9ÇÑ­¸j¤>\x000bA²¶´c/\x0002ÇT[îZ¿a\x0008Ë ½Ï¥$K'N\x000fàO(ÓÌpF°]!õºOÂ\x001fÇ±ÀPûØ\x0010´§¨\x0012Lcn\x000b×þ \x0002\x0001Wÿ­$k>Ûì \x0002ÏiÌWv¶¼:\x0008Ö¿~*É\x00023sã}íÆ\x0000Û\x0016ó¶ë#\x0005ÛÉ¤H$\x001cÅYªb%éy\x0004¦×¬üdñl\x0004\x0004ãzóìËsNI\x0006l±5_rçÕüÙz0¦çOÇ%\x0004Ù?åÁ)ss»¡úå%y]Ç\x0016.TÚà³¬ò¥1Ôgi¿´a\x001c¬ÆÖãïØ\x0019¬Å7ª:\x0013Õ`fM®îßµäÁ8å£\x001ahy¦¢wÀ[.­\x0011êþeVKf1ê(·]\x0013\x0015\x001eåÊÏ\x0001\x001e¤êW½ä
\x0014»É\x0000-°â·\x00160~5\x0007\x0006·\x000fõ+_òÚ¸\x00009¸|»¥\x0019é*ñÜdcW\µuÿª§Çõ2\x0017~-ëËa\x0007ë\x0002¦\x0015?p5ËËìdÄIÖ=>\x0002\x0011Wé6qmç;¯x\x0005Õý3¼Sáä'º
å3oCÚð°_¾(É\x000fj«S)G¨yÿ\ªq xNÔ8u\x001b\x0002±îï\x000fj\x0015vé\x0016Ð@Zy\x0017È\x001dS¯kä_\x0005³gDxIYÞ\x000b1@u~@ó\x0012kßåxÊ«¾Z"ÿ¢¯xñðôåé1ÿ\x0019î7g+Lá£Ö@X\Úc\x000c÷¶\x000bvÖ¥}quóîæ:ÿ´9¿Ü\x001e©,b\×âºÅ¸&¥Õ(\x00135\x0015È¼FgeONë[Z¿ÖVãjìÐN\x0005[K\x0010´'ã\x00167,ÅÅ¶\x000cÔ­\x000f\x0012>öLÖUt
\x0007mçÓ£ä¸±Å­Ë\x00056^ÇP'FòLÒ0
¨ù*¸©ÅM­Ë\x0011ûl]ÃÝÊ\x0003%$\x0004=¯óbØmîÿ$\x000bj\x0011-N,3äå¥»MÏ	¼Ñ0ûUp{\x0015[,c.QÓÔhÚ&\x001eÿ£a>}AÛm4½x§D3F<ævG\x0012\x0006ï¸Ñ^¿åy¡3/,6oé,:ñbF\x0006Ù×xæõó9ßr^èxaéên÷^×JEå9ë:(³_º×t¼f©}\x0015ÇáòÝG±òfçÛ\x0007Z;ë)ÈymÇk\x0017Û×ÐÏwðÚ\x0015$RA\x000eNøJë¡;aÙAjæ(È+,Of5ã8ËÐ×9Ù ;*`ÙYöu¬\x000fÙÉåQ>Fn:¨ç\x001féÅ¼¦Ó\x0007³L\x001fJÍ·\x0002â5u¿E°Õ¾_çt3>Åúà4\x0015{ôÑ¸'á¾a\x001cç2ÜN\x001eÌ2y(1M*P~+gÜ^\x000e<µÈy»íf\x0016o7³\x0007L¦í¦yÝW_Ó\x001dÇfÙqË!ðñ¦,eºggÆUO\x0005­_\x0005×vêkªïÔA\x0003i\x001d¶îá©­^3.æü\x0015Ün5Ø¥«\x0001q8¸©Ñ\x000b¥¼Ò\x0013q¾\x0002JÛÝ*ì²k\x0005ârCui4îÝ9zoÍ¼êëh¯ë<u·ÔSÇì\x0012¢t8ã\x001bÔ:ºµùè¿«î:íuKµ\x0017HK±ÃÜ*ò%õl_Ð_gùºN|ÝbñU@OX\x000e;×:Løx ÞQÎÛ©[¬\x000el\gk~9·ñQÍ'£ÈaûpÎ²xN¡E=xñ
Ó8xr$}\x000cûñvZæ\x0016k\x0019\x0006\x001aÊfÃÜ(.w°Ô=\x0006gÏ~¥ÅÛlnéÉI@¥nÑaíÄ5×ÔÑÝcw·¯ÃÛ9¾n©ãY Ö/\x0006wIË"kÃL¨E¸¾Ó^¿X{£§W\x0005\x0017µå(³lÞ\x00035LrÜÎM÷KÝt´ni%Õ!q×	ç<ï¶ùGI9nwRøå'§$\x0010uVå-8ø:\x0001>ß_,f\x000eN´ASÆ7FFÌWÖ\x0006ß\x0007§ûe\x000f¶9ôd]:)\x0002|¥À¿ïÌ/W2Cå\x0007ÙºÛ­ætUÞùrT9oçFúån$%¸/g|Rð^\x000bzþVÎÛ)¯_®¼\x0016ó&û*M}ÝÑ¾¼\x001eüWz«\x0008ôån/ðôÍTX\x001cØM\x000fú+Ý1C§½a¹ö\x001a^
_·,e_g³NyÃbåÅÍF°VmÝÈÈw¾º@Û¹èa©7Ìâå\x0003÷/l\x000fa³ß¢x\x0019mwL¥Ç\x0004údednÖ]Ã3êÌ¬¼_I\x0019Bÿ*¸\y\x0003\x0005ÓóbÛK£}\x0012D¾\x0002oìVC\~a3¬\x000c\x001e³+øÂF\x0003
¼÷_É+SnÛ,³<jß.!ÆWm®¾Åê+ê \x001c\x0001øip¾\x0017Ë\x0012Þ\x000f=ï¼QÕ¤|!"?\x0012û	\x0012púJÆwÝÕKL²OÁ,\x000c­)]ÄegGÈ×ËE¸r]\x0000ìdfä_´
×ßüóÿûÛÓ1¾*r27(»eåFC­-²K¶\x001fzz»ysúï7¯\x0006¨ ¥\x0002\x0001U­ó\x0006\x001c
»ÀÎ3\x0004\x0005ûËs\x001cÊ´PFb*Ï¹
\x0006\x0002wD?SíWSÙÊJLå9ðmt (r+õ\x000c5×&z\x0014ÊµPNb*/ÌÅTÊ¯1\x001551Õ~\x0000kÊ·T^b*Cå#ÙTÃjQQã\x0000zn°À(Uh©ÄVú3`}.ÇÖ£¡­LµßÄr*¶TQ@e¹?ÏËJÂóñN!ô¬·û%yãT©¥J\x0012[qo\x0006L\x0008¬j\x0005¿ Ú¤\x001c¦jZXê:Ê?åTM\x0005IÇzXsAÒî°;	V/í\x0012mÇ1K°Ô£D;°­4×»{ªv-ÑvhÓAÎEê8«P\x001f>ÈÇ©:m×\x0012qÇº@¢Ò\x001c\x00147\x0019°årªNÛµDÜe,\x000eÛd,Çã¨fZ·Suâ®%ên=OcE* OÈÍ>3Õ3Gwê®%ò®yJ\x001cvwÒDeëÈä°f\x0013vê®%ònju=vN®	<jRÏ´=\x001cÇêä]Kô\x001d\x001fÉé\x001bzW·¡±¬ïa¿<p\x001c«Ów-\x0011xÃ½+óG\x000c<J7x_÷á~\x001fÙa,è\x0004\x001e$\x0002¯lxe6÷©ë÷k°:\x0007À\x001b\x001eD­eëçS'Î
\x0018ê]÷a}ÇÄ\x001c¾»g[\x0019*{ÀñM<ÛÛå¾\x001ft\x0002\x000f\x0012:Ê\x0017'éñÊ²¾.øý!uãXÂÃ°ÂcM<!7Ëyª]Á,&þ3qªNáA¢ðÚcuuÁ
Ôù
/uÅZ.ZÐ)<\x000c+<&ùðÐIâé6ã¼âWìÂNáA¢ðG¤à@rî\x000e\x0019 Ö
¹i[£XÂÃ°ÂãÜoÏp±÷5O\x0012¨õÑì=ËSu\x0002\x000f\x0012WóÊÆig¯ÏB»?ÈuÉtênÕ\x001d4¡:\x000eÈíRd½û¯RãP¶amÇÁ;ª\x0006è¬â\x0011ÕËí°îd\x0005V§îF¢îÍ÷\x000bS÷Q
hÕCgÅ½Ðô¡au/ÙÁ¬\x000cÙá¢\x000c*\x001cnÈÖÚ/Ë\x001aÇêÔÝ\x0008Ô\x001dãØ£ÀIË.h^[iÍGìäÝ\x000cË;\x001e:¶ÖdÅª¹ÉuÔ«åÚ`:y7\x0002yÇ' G\x0010ø^á¼¯ñýÊýq¬NßÍ°¾ã¸G[=xÇ£~¯g¿_ó3NÕ	©\x0019\x0016Ò@J¥HèfÑ©ã]9x·ü\x001bÚN¶¬D¶òzÒº:4×ªª£¼â¶Ý·\x0005GôÖù£\x0000«®ß~²í8T·®¬`]¹EI·o\Þqt&¦å®íÖ\x0015¬«\x0018«6\x0018\x0015jz£\x000eay\x0013®¸êX×Õ·¯¸}\\x0019;~\x0002"¾*WýìdÓçèò=º\x0019Àu>}^üz÷ÛÇ{|õ9{ø¯Y\x001cÿó^q\x001fn\x00034o5_¥uó)_üxþúÕ%¾ô]ýç«#3Ê\x0018Ë¶Xö_\x0005jgnþÅô¸óðôez"»|xú¯ûß?~útwÍ`Q\x001aÍ­ÕI¤	Ä]y\x001bº¬Ñ«wÓÛØåÕÍ^]¾uqqþ< i\x0001\x0010Ð*Åõ%ÞøÒ\x0018b\x001dQº¶Ï¶|Vj@UîgÎ)Ì¬gùÕÎBW¼µÎµtNj=¼@\x0016Á
ÙÔ\x000bÛÔçVãù\x0016ÏKÏ\x0003òb\x001d6'-m#µ#<kº6øBË\x0017¤|ùv\x001b¡î\x0012¹×`\x0012ßÐ5`[\x0004\x0018[À(6 ã	ñ.8:Pµö\x001c/·Ö¯ýÂÍs¢\x0001¿2Â±§\x0010_#\x0013\x0011r¼Ç:·ÖÍË¢	¿²\+F	4>H­\x001fYëµ\x0012£;Öb¶5Ða6lÙ& ø¾nýzÂN\x0004µX\x0005ëH\x0007o¥[rÞÈÔ*7\x0018Pk\x0011Ý)\x0016KMÖr\x0006Û|£/\x000cºæÙ\x0018ß[ö;ª|çÉ§ú|ê\x000fZõ-~Î°\x0001ÞÁuq»ys÷åcÆ¤Ãq#¬¶äËLÍbËÛ=_Y]7ëäâtóæüÝ«ÌH4GæÔ\x00168×Ã9	¶ ©GOXýPZo\x0005
äÊw½ù÷Ù1U¡eÃ\x001f\x0005l\x000eoÒ¥ë\x0006w\x0012J¾h¸eEÒm!ç\x0002¸ØÃE\x0011\x001cX\x0012é ó\2¬!:\x000eâ\x0010ÈÅlNñ¿³°M?ÿa¾j^ÿÍddÚ\x0010·\x0000<e}QvEy;|÷ûíý
!\x001cÚ§9\x0007¤wÞR NkL\x000c-gÛ\x0000À÷çïO/ßmè§gLd$H%³ØÛÈÝ3\x0012/2ã[gYäZ$7\x0014«ÿ©ùá\x000eèè7	#ù\x0016É\x000f#ùÄËÉE¾Yk¸þßºö¤!ÕÇÄ		\x001f\x0013G"fzN·\x0008èu,V¸k\x001b¨\x0011åÓ|'_Rïv²zýðåËs\x0008»Äµ#\x001fÓÎ+¢±ó\x00057¯¯Þ½;r3\x0015´T ¡²\x0004h½¯X&ÑémÜ*,Ób\x0019	\x0016\x000fBÎÖµ]qU\x000cæç¦
bÙ\x0016Ë
°ªà\x0003Ï#\x000fÀëÊ¸ùV\x0017X®År2¬R{6­-Nö©á\x001a3ßrÊ·T~ªôµacå[i wsÎ@2n¾¡Ü Uh©*k:lv°á÷5ßÝz\x0010+¶XQ\x0015ù\x0019Êb7+»åç\x0007é\x000cb¥\x0016+	°P\x0013heùÈy">ð[AÞ+öáö¢®÷Ú=g. RläÃã}Ô¬¦Ø\x001ee9W¯ñÃ"\x0018õÅÇ\x0006MÁIå-»VÆÏ÷\x0019äêT^\x000fË<~Ç\x000bW}2ðÁ²Ìûù\x000eÒ\ÌëaÇT\x0003àç\x0015üà9Õ ~Çùéß\ êaEÅgkCà4tlåZ¡]ºST-TW[Ceo³ÛÅË+¨\x0015â¥;MÕ\x0002QÙF\x0010ë²ç*1ê²/\x001fäêDUKTÕDîc£¯\x001da]5×üô1,èÔ\x000b$ê\x0005ÆZe,¾a6\x0012}\x001f\x00190ÈÕû\x0002À¾´Ô>e\x001fµ|ECíóÝ\x0006±:§\x000b½.\x001aÎX¶ÖfñkÄ\x001eºÝ\x0008Ý\x0018m¤ôÌåko£j­åK^^QDR±y+\x00056óEº~ÚvÖh·Bêû&Í´ðû"·çuª¾(k?ÔE\\x001dþÈïÒéÝ\x0012¼ç\x0004#ðßÐ»'
FÝó­\x0002m÷åîqÇvøqÝÐÕID9«§e¨z¶f#ÀÞ§\x0005ñ¢\x0005ÊÃÐ\x0004Ð6Å,å\x0012\x0007@!_qÃÝ£\x0013ÀlúÈY:\x0001ËeIìÉz¿èè»Q¸
<e¦§O\x0007ßÙË]zÈ1ù âÙÄ%-\x0010÷Dä&\x0013Ý\\x001c{eg$h`\x001cÙø|jÓÊü\x0015\x0003\x0005ú½À8iÌ8¢RXoMàÔl%þt{%ãD¶%²\x0012#ÑA÷\íïQ\x0013è!¬0kÜ0á\x0001Þ: 1¿ÙHÜ¥×ì!\x001aGò-XRn\x000c62­Kë\x0013ãÞ|q¤Ð"\x0005,\x0019)qH"\x001fÞ5~³U9N\x0014[¢8n¤ÈÝSMRÇï\x0014÷´´çÒ#¥\x0016)Id|ÄûÀVª1Á½Ëâ0îr\)·\x001fÎWõ¦¶ñ½zñRÒ*éqYB3ñ\x0002'u-Õ\x0003e/ê6Ôi\x0016ÕQ¬5È\x001cö2NÇº\x001d§E[\x001fÚ±ÿBýtÕiÙëd 8P:§`:TªS0°õ s*ì`Á~äáY¬\x000fJÛpööm'/Küñ»³7×\x000fÿ¸}úû®øþîþÛ¿Ü\x001d«\x000cö¥A\x0004ç"gSf\x0017pZñØþ¡ÍÒ=»zõvs}õçÓ?MyïÏ/¿?}y~$sQCØq\òéAÛñü·î6?ÜþãþáË\x0011@ÇïuùX>áù\x000bìí9mv>ëùëW\x0017ç\x001fNÿ|yõîy.h¹@Ä5yÆ»HÕ+Qq;u\x0007»9»20Ó\x0019	\x0018X.~ÅÌ6Í\x0015Ô´*¸Ý¾È2.ÛrY\x0011æRá\x0000®¾µ8vf\ÜÙ)\x0003s-\x001b\x0006Ã o8)\x001eM(-¨¥`å;wXå[,/ÁJcÏÁ×ÑùfH+ßÃî-\x0019XlÁ¢\x0004\x000c¯¬å@
8SÀ\x0014u\x0019Ã£sÕL-Xå»\x0017ES1RÈ×jÇZÅV¯\x0000ÓVèq±À¸8pà2ÚPÛ \x0006~þô»Iá2°N+ô¸X\x001a<êcs<yñ\x001b.þÎxZèN-ô¸\\x00184\x0015-b¼°\x000e[á7P¬ZCÖÉèE¤K"Nçã\x0012 èjRËn¿P\x0019V'\x0017z\/ð@²èõL\x0006sÓøír Eþj·o,tdAò)\x0015·ê\x000fx8ñ££â×½èvÛTÊÈ:%Ó")sµ\x0014\x001c¿îÍÀ\x0008j·\x0003¬	Ý£w¡$d\x0006Ûou¦Ã«ÞÕåïVÐùc0îQ;bÊ×Ã\x0016Ô#5±ü'k×È?ô\x001eHeµç¤¥ìt×7wàtÝç!\x0019Y'³ Yl+K&C·B}´7RZ\x0006Ö©,TV+êóHø\x000eî5?\x0011åÓjÍ	ÊÈ+S<\x001a,`s\x000bJ6ñJU²ÝqP2²NhAä©´3Ï]º<÷~^­úHÍT ¢5\x000cË[
\x0018ççÄ´J3Lw\x0002\x0018Ñ	àÔ'4\x0018\x000bT-Ëìnü¹\x0003;\x001aÍ`¶3\x001d\x0000ßÔËpd8göm×¿î
\x001dÉ\x0007âÆ¿Ü
R{tB¸om½°g½ð\x00024¡{\x0003,ûß\x0000\x0007/SÛÑD_§f`1\x0015ïE×Ï\x000fÚ¤>{;ÿ\x0002\x0003B\x0017w7~óâ×»ûûåµQñ¥\x0018K1m\x0019\x0018çz\x0011ßì\x00006ñéâü-þgþx~yuy8FEH®\x001e	\x0013\x0012þ8
\x0015L)\x0012Àº\x0019jU\x0015¢N\x0015Ê·]CÆ ò7ÝÀ\x0019ÔÀÙï·w¿>üöÏÿ>|\x001bÀY\x0014\x000eµºö\x0002Ý>Ï\x001b½{å|ºy÷ãÕëc¯ÄdZ&#b\x0002Î¶5Üá\x0008£üv´ç3ÙÉ3Q÷\x000boO\x00140Øvk4v÷åH\x0000äZ '2\x0012'íxÃ¯YùÃq\x001cÛí\x0002\x00120ùÉKTÓú|\x001du\x0019kÝ\x001d\x0014.@
-R\x0010)Ö>LQ#+ÕwÝ|Q\x0001Ql¢ÈHõÆáû\x0008\x0019©VÒí^ÆRDF¢·Ú¸¹K6\x0012\x0013Ý\x0014q¤&§\x0016uIÌäÈLÑÕ¾Þuiï¾1ÔK¥D+\x0013\x0017'8Ì¼çfÎÜ¢x?!M\x0000\x0005\x001d\x0014ìÄ$Éòìü78ïkwH©Óo-\x0010ð ©\x0007©Ó±ÎÂ®ùÿ\x0016÷ÎR¦N¿µDÀ\x0013ç¡9\x0005µg²ÑÛü¸ÅûNw\x001a®\x0005"\x001e\x0014¿u8í¸9ñ6m<-'Ýi¸\x0016x¬Õ\x001b\x000ejæF4ëÍÕUÞ©¸\x0016Èx^QÔÇ\x0019À>ZRµÄ|7éF\x0000Õ	¹\x0016(y
ü´ç rnRt¾®ó½'¡q¨NÊµ@Ë³¥(RïlM\x0006\x0003RGÝÁOãPÐ9HÄ<ÿ«ÉUáäè©Ý\x001b$@êÄ\x001c\x0004b±oî1½\x0007M¯SZ¬Ý\x000bÏCub\x000e\x00021Ï{Ã\x001dF\x001c<\x001b?ÙM\x0010@uj\x000e\x00125\x0007Vóü'à\x0005Uìnïf\x0001S§æ Pó¸\x0015Nï¸7k4õ`Å\x0015\x0001:5\x0007\x0003×r9ìÎî/?õÛ½i¢\x0002¨NÎA&ç,\ì\x001fØÚ>d·Çµ\x0000ªsÉ97AÈ1õ|Ë÷s^Sa·A\x0000ªs\x0010Èy¶\x0014µúqKâPÝ«Ä\x001bg2p\x001apFUÕ¼ÎtÌLÛ\x0015µøFe:å4\x0012åL'\x001bJ\x0019ø4\x001d,Ôn¦\x0000ªSN#QN8á\x0005øé0\x001a®ø±q·^QÀÔ1$qI.'¨ì\x001fÔû\x0002¿\x0000Ø\x0016«¹éDÊHâ\x0006ß\x0010ªÓ\x0003#¹¥C¨Î2[ñ·²Ýæ³;è7ê\x0016º\x001d]èX¨¥ù\x000eò\x001fy ?ÛDµ<<f»unÿ\x0018ëÜvëÜ®ó2\x001f=P4[>&v\x000fòß\ìqÚnÛ?Æ"wÝIìFObJ\x0004ÑÅL\x000eôèÁmíÒÞT7I ±ñÀ`b}ðøWÆ\x0013ÍÎ[Ñ$ õ­è_û%Õ\x001e\x0010í«\x001b
 oî¿èÛ\?üüëâ0S}u,¤pbâüTÑë«\x0017?\x000e`A\x0005\x0002,]cÖ¼òmí¥kÒn\x0008]eZ,#Áª\x0015Â\x0018ù¤º0~ió3\x0006lËdÇB
|è8í9#ÝÖ19vÏ
\x0015a¹\x0016Ë	L¥ê¬ª|³âRëj«ýIG\x0002ªÐR\x0005±Às´Ãgq¥¿¦\x001eÑ6îÏ2\x0011`¥\x0016+	°ã,.%N7ÇsØ8ß@`\x000cK÷â P`
=¸d©Ñ2¾v¥=P\x0015<ÕíB-Ø\x0001;5¹b­¥êÍé:8_y>ÈÕ-y-Xó\x0001ÃØ°\x001b"²ªr¹ù\x001aïA®nÑkÉª\x0016+iJÈÐ\x001b\x0005\x001eñ`÷ÖDXÝ¢×Us\x0008IM]ÄìËÔÊd;_Ö=Æ\x0005Ýª\x0007ÉõV\x0017¡\x0012$[
\x0018\Õ­z\x0010\x001d>5]Óa¼ê:hÏê]ÇFÄÕ­z(=\x000e­¢U=¨b3'ì|¤AªnÍ`ÍGc¹ã2FF©MÝ@\x001b×ìÅ¾÷¾M\x0007\x001bºUð<uñÄ.Û|j»E¯wÝA]ÜÁ·÷¿lïòá×ÛÃMæ#s\x000c°Úd>ßÎèÇèÚ\x0001Â/¯7/¯O/¿ß âåÕ§ÇÒ\x000fwB]B\x0001\\x0002b\x001aáá{ PW'¸ì\x0002up¦32¸¬\x001b¥­MÞª¾¸÷0±ÅîTZÂf[6+cËkÑÚ¬ºÚ\x0001C\x0016[M3í´´\x0005pm\x0012\x001c$t\x0016\x0011¢OÔ¿\x000f°\x000bcs©
ÏÀ=·\x001ft·ä´pÍå\x000beÉz
ÓÉ0ê ¹rtÆ\x001e7Ý³tÝÓÒEçNÂ$$¨ntÝ\x0005Ec\x0017°Lð¸éý®Ý¢ÓÂU\x001ceü¿'d9\x001aWÿiµÒp®cs2¶¬s¤$qvF^tÕr\x001aô:Ë.\x0008wD¢¹\x0001'ð\x0004Ú¯FÜDßu[b»ÔÑ%\x0019ãd0\x0015íRô¬&q\x000cCwì\x0004ê\x001aíb¾M>üxh'å-°\x001dt\x001b\x0016\x001bÖÚ-¦D¥L\x0017X1ßl\x0015]·î@ºî<µ*\x00081\x0002v/ëN1
ëö,të\x000e¤ë\x000e¨åXÀ$k>(bd)Núø\x0011û\x001céÖ\x0011®;çªíJ²+t$ºh×­;Ó;'Âu÷¬%:Ë#³@q'èÂÊug:56B5öêÄX¢Óë\x0002L§Â:ºnÝ\x0019áºó<¬ ²*²\x000bî9½{ÎvëÎ
×§¬¢¬Æ\x001eã\x000f\x000b~ÝµÝµÂ\x000f\x001b<Å\x001e\x0002GJ@Ð:0ZK×É\x0015Ê\x001dlñÎMÁù\x000eÀÜ:ÏÓu[Ö¶¬F®d\x0018\x0004sÑQ\x001d(\x0012ccÚT%tÝu¢/«§\x001eåË:\x0017Ð	èjáó?ñÌ}çYºîË:ÑÕX\x0017P2F\x0003C\x0005C2£pbÆJÛuâD¢±Þ¿¬æäwà\²\x0008aå²óxhÌïEP\V»D\x001fÖ$¦óá¸gü,]·)¼pS\x0004îZ\x0011ðÅ*\x0010\x0000XÞ²ÐUÇ/¡ë6\x0017n,w\x0014 °û\x0003e:J
`aÝ²Ó;ï¶ÓÍ\x0002#¼3ö\x001a1ûcÕ}\x0007é1eì®Üi\x00005ERð\x0017ÿ\x0017)\x0003vÜA¤D³lèÙ&$ã©Y\x0015ºò£QKw±Úm_©¡\x00167ç??|:Ø¤Ò+8Ç_G &\x0007_*gFÉ¿¸º8ÚJí6°TÍLg¡°Úº>\x0008\x0006Î§w£ý&Ù±»£P¦2\x0002(Íá³Ä/\.Z\x0012ë½(ì8mì8\x0013>xÓ³Qd¥:µEï÷Æ\x001e'r-\x0013XÉò\x001cgÌ¥§\x001a\x0017k8¸½'æq¨ÐB\x0005\x0001©í\x0010cä\x0008º\\x0018Â
¦Ø2EÁ§ÜZ\x0013ékÂ\x000e¿ÿÙÝæk¢}×	ê;í\x000eËså¾ËKuU¤%K\x001dv
ÔÎôËÛ§¿\x001f\x0014Ð|Gá¤l2Å\x001d§¯C\x001fÜryzó§ç¡ q(,> ©å88©\x0016&rëÏhgKÇ L\x000be\x0004r§c0r8{\x001dÂn:	mì8Ó6Éà´\x000fÇVµÝ.¬0k¡ÀPÜ<É\x001blIJ_Ïrq"x?û\x001e9\x0006å[(?\x000eñRêj\x0019,
Q\x000f\x0007AoÁ=Æ\x0014Z¦ 0\x0014ð³­ÙN¾Êÿ\x0018ï=·Û°@\x0002\x0015[¨8\x000ee\x0003OÒ0¡
BPÔ\x0015Z¦4Î\x0014,·w7Ø»õ\x0013¬òc6\x001f`\x0008ª\x001d»;kç8©Ù\x0000\x0006§î¥<Ïå fÓ¾Æ¨z=\x0017\x0008º7ì)\x0018¯« «í¢Ú\x001fç>NÕ	º\x0016(:\x0000Â3ù~f¨¦e§
Ân\x000b.	U§èZ éÎp#¶º\x0005V\x0005NT\x0005¯VØªÓt-\x0010uÌkäÆÐã
s¾ îµt\x0016Pu¢®\x0005ªnÒ	:WÄ'\x0013ò{
Â\x0005P¨ëQUÇ£\x0007 \x0018¸\x0019dP¶	Ø¿ÑSu²®\x0005º\x000eÕÑ3>ð¼àL=ÿ3uª®Ge\x001d[ º­¥ª¯îk\x000f<»F%T®k°k³êS\x0005ãøXöi¹,@'ì0*ìh+ÏXPØ©\x000bç\x0010<\x0002¯uè\x001d\x0004ÂÎÎg\x0000n½óª»Í$H½>ªêh¨Z<ip <õ"KÜù\x0005",?¡Su\x0018Uu\x0014ÄÕÓ\x000c
ª§Ö¾Új~æÖ\x0018U§ê0ªêØ³ÙÕ\x000fx\x0002ò`>î[\x000ba~¼â\x0018U§ê0ªêHe9uÝ8Ã
2|ä^\x0014Ù\x0005]a«NÖA ëAsÛ%ãýv¸¢¯Í
±NÖaTÖ±%rmcìv$_Ð|¯±»Í
%T°@Øq\x0010\x0005_"j®¬¯Ýú\x000f\x000c\x0013\x001dêt\x001dFu½tæY9è%GbY7+|PÓÉº\x0011ÈºÓÕR&"ß\x0004ekTÁ®¸,NÖÍ¨¬c×:üw\x0017*°µ7§­Gà
¿ÊtÂn\x0004Ân,\x0007@
¤\x0013Çsø¸Ó\x0002ìÍ§\x0011@õñ\x0017®[Í|NÜÂ\x001bnÞo<Ë©:]7\x0002]×¡ª\x0002ÄÚÂT©ºÖÍò¸étÝ\x0008tÝ\x001aAÓ®RÕÞ+\x0000z\x0005U§ëF ë\x0018WuYq\x000fÎT\x0015Ô¬¸\x0005N×@×umubt¢µíu\x000c°7\x001bF@Õéº\x0011èº\x0002®2FÕIZµ\x0001?ù\x0001°cT°qa88A×¡Lµ¡Ö^K\x001f\x0001íÝ\x000b{Ìþ:/vì~Tß®ªåje;]·ãº\x001e]í~dÀ°:~\x0000³ÛÔG\x0002Õéº\x001d×õükÊ+6 µEt6U]_®
¶Óu;®ë±¦cN' å:z.ÝÎ¼\x0012ª>²>®ë1\x0018j\x0000âÇ\x001aÃS\x0011³¥;Æ¶\x0015J«½¯]9Î\x0014OïÅ\x0005O×fç[q<k³;÷È¹G\x000fO_&ª×\x000f÷_~½{<ÚU \x001f;\x001cùÀ:O*Ï[°öK^Ý¼Ð^_]¾ûñüúhõ·Ù\x001d~dÊð#\x0001÷µ\x001eÖ`çÄ\x0006Å\x0018ÕÝê\x0017À\x0016ÎÈàp.)r]vn+gk[\x0007³Î¶tVh:g©é¾·Ô\x001a0û\5¯º¹Q\x000bÐ\æKn[g\x0000x°¼õ[ÿK­¤\x000b-]Òa:ï\x0007\x001e;çôv?¬K-\\x0012Â)S]íi`mu\x0012M\x0017©Óé^Kb\x0012Ð\x0003J5CÞ¢QÜÄ\x0017òY×mX-Ü±~r5Ê\x0008·µÛ#è®Ù\x0002¸nShá®È\x001eÙIí\x0013í9\x0004Ï¯:©Ò¯SbÝí
-Ü\x0016Sú\x0011éw\>®j71ã»¸ý\x0012µëR5&Å\x000eXÉ\x0007658mµÁ&å\x000bGî ÛA\x0002È\x000f
°}»õ,ÉgS±\x0018¾_Ün^dÄ§Ç\x000cù¿ÿ×ÿs~¿ùñöéà\x0004%w(çf/¢¼jå¡­	Ó*`v\x0000^dÆëL¹9¿ÜüxzsxPÅ\x0016ñ§Û]È[1¥ì\x0018trw/ëüP}åg0\x000fZR;Ó9-g8Ãzó¿ÿx÷ôw\x001auy8+'û­å+G¿-Z\x0013g\x001bø\x0012,Î\x000bÕµ
~°\x0013þûWç7¢ÇZôOd®¾\x0002Ndø£MÓóVfÃÅXÐti>Ù|ZÇæ{6/`X×5¡YmzÓÄV\x001e
®\x001dB²OvpÙ1YêÉìR§B´\x001a;j6+ÓÑlmóK¹Ùê»RÃ%\x0001ÑXÒUà(\x0008á¬åõÖ=/\x001e\x000edëæR#§Y\x0015ù \x000b¼àºt¢%\x000bn«&¼än%kÎÆrläEÝ¸Ê¢3¡\_ó²óváN
§¶\x0015\x001dQt\x001cßÞÝùx÷8047Õ}çâYù +7Fì\x0018Ñ¨ñÛóËw¯Î¯Ù¹÷\x0004Á¥\x001e.Ã\x0019LV¤voy\x001b\x0000\x001aDû\x0001ì#pÏ[®ù²d»[ñ0i_\x0017ãYz-à9«Ùrmb¤\x0004nê\x0019ýÄ65Ó9ûæñãç»ÍËÛÇ¿ÜÞÿrÐp!oÒò\x0016\x001c\x00026n\x000c§Cä\x0004ó|@@wx½¹~õö|óòôúåéå÷G>*£5~JÅÃ_\x0013\x0002w[Ã\x0012odN\x0012\x0013£Óm\x001aÒ\x001eáaO
v3àaJ,}óéöç\x0012¥À£ÿ/2ãA6\x0015õI¢ûOò\x001c.D³KÛþûo.N_XÅæüåE|\x001e\x000eZ8Ái\x0008\x001c¡³JqGÛT\x0013_Û\x001cÓ\x0005h®EsR»yê!kóyÁM
¿ö\x001bhßÕ\x0017°-\x0008Í¦uÍ\x0018ÎÇk ¸À1\x001eÓ¶\x000cZÀZ¶$ý¤SG±j8jÆÔÖpkØt¿\x0017Aç\x000b#½_ÙìÍÑ;CLuhG\x0017}]@g::#¤³5\x0013Àâë_9!®£ \x001dÆº®Û\x000fZ¸!´×\x0014µ6r¦l²<Õ\x0018¿Êt»ÓÛ\x0014MoíYÇ\x0016ôvZE½-¶\x0001<\x0001b^u½\x000eã2äw§ÍÙíßî\x000eÏØÕÓö²×[Gì\x0006\x001eñãìÞÛÈÍæìôßoÎLlc"h`\x0008µ¦ÐçnÕùâ
´×9nÈ´DfØFÉÔY×Ù\n\x0012Ë-¶Þ[d[$;l¤4Õ®LVÂº6²\x0012§\x0010º½Ìâq ß\x0002ùa\x001b¹úä÷=JSH¼\x0001ó:\x0012\x0013}PD`«{Éqøãw/îî?Oûî?nþõîÓ¡8·#IÎ\x000fù\x001e
«×	ÃóË·Ó®ûÓ\x0017?_\x001c\x0019Ô¹ekã\x001fîV\x0017j\x001c.\x0002Îhð¸Wö.Ûæ@û|mgÔ\x0014©wQÌÁ\x001f»à\x000c	×Ï·\x001f?}º{<¬]>r}¾YYJ/ÔùH/ë-iÓ»5B3	ØÓW\x0017\x0017ç×Ç\x0002^D«{Z½Ö×âY\x0012¦V¨%í\x000e\x0005Fqí´Uj+ë³P\®Ò/>}Æ
óæ !FÖ#\x000e±¼;Ârý¶O~çúâæâ-n7\x0019ëð°ë\x000cbëÌ W°×ã°y\x001bEÔ©}®¡-Jc5[ÀnÇÉòF±\x0005\x000c¦â¯,Q+(\x001f÷\x0006R¶hÏÈ\x001e-Êq²¯	ô¦ñ\x0011U\x001b![ú®í\x00035\x0016ý\x0014¯1\x0015,+\x0001þ8½¾Å@\x0008r\x001dÖ #>
d6qMEÈ\x0006´¢5Úï½>Å0\x0008r\x001d(\x000f}p0ÿ·¥.ûnó&ßêlPÈ\x000eä\x0013\x0015±e\x0001ËÂ
Ê\x001f\x0012ø.¦zZª²Ï7oòµþÉÊ¤Xë¶\x0010Òâh_^ßþã÷QE.\x001e~¿»}:ïÄèß¢~`!&µkÉ\x001ep"ýèº+ á®OÿüþÕÛI?®nÞÞ\x001c;fa×9¶FûìöËyyûûñì©\x001cî\x0007ÀÄaª÷åÆm\x001eb©\x0015=;}÷.c^¾Çþºaù\x000f»¦E4RÄU\x000e%d\x0003*òlT\x0017\x0002#Âîø\x0005¶E´b+FCÍÂ\x001dà`\x0008*PÖÄÍ½\x001c*1¢k\x0011Ø>¨ò¡ubEöÆ2¡ÞO\x0013\x0012\x0013úÐË\x00180^8\x0019Ñ\x0001K³\x0003k\x0008Ñ\x0015K1ì\x0004Kò/ÚRÓ­?ðåËÝæÿïóå@e6\x001fºï<x 8îtm@ö\x0013cØ#x÷î|CI2Ïò7,æõj\x0002²û¢¹(\x0015<Eî²ågr$¸\x0000ýó\x0018þ\x0002ï/~½ûíã=\x0012?q;%®\x0015G+ßÚÈ¾¤»ªì²¾~ucP¦2ãPÚÒ\x001còè0çº÷ì=t\x001eµÉµLnÉ\x0005\x001a\x0011\x001b±1´æò\x001cJxO a\x0005Th¡Â8·ÔY+:§¹^!ßÈM\x0006h«f¥P©JãPù4ÓeIá\x00108\x001a`¥E\x0013]ñùt·¤ôèÂÚ*Cg\x0019[<.$`Su]
¥TÝ¢Ò£«
©\x00029\x0001xTqÍ^Hzê.·BªnUéÑeÕ	+½&*gkHÉPÑW2]\x0013ôa*kw*ÿ7ï²mßÞýöðçóËKCÙ·\x001eë?öD/\x0002Ìæ¿=}õçA@h\x0001a\x0001 -¶\x0003ìqa\x0008ûñ¦½Ñ¿r@Ó\x0002\x001a) Î@4dACí=ç°lÁùÒG	 m\x0001í\x0002À'9Y0T@Ï\x0016­\x0001ð¹Ï	ùòú/÷Øi\x0005R\x0014=»ë¾®ÀÙ\f	où¼Oa$ÛÏS\x0011\x0014¸­ýV¯ÀÐ\x0002\x0006)`´ôR=­@JôÚW\x000bÎW®H\x0000c\x000b\x0018ÅzkAÍñ\x0000¯¹{»#Áä©\x0005LR@ìA8\x0003Ö`mHºF®\x0000\x0019(ÓJJè\x001dÝËb¾$²\x000bç\x0012÷sÇáSk	ûDzL\x00135
`¾æR¹5¶c)|f~Î¯;G´ô ­«\x0005
_¾m¨\x0016-\x0001\x0010v\x0007$ÓX³rÔédkxÀjÞ&ó\x0005ë\x0012Àî ÑÒ$ZwâB5!2yîbù5LØIµ\x0016kµ
%\x000b ß\x000e\2 7`ì'\x0001vJ¨ÅRè<_{´ã6¥\x0012íðú:?¹N\x0000\x0008Ð\hÌvJà¶3.J¸V	¡÷\x0007Åû\x0018\x0000}`gÚÅm\x0008À­ýÆÐm\x0013\x0010o\x0013ïi¾y^K¹]møÅp­VC·M@¼M<O¤::v	yLCRóÓ$|Ý.\x0001ñ.ñÜù\x0001Û§r6T?aµßØtÛÄÈ·	Ða¢,Ì´KøV¢çG=J\x0000»mb\x001cw\x0014óABÅíT©kO\x0013Óm\x0013#Þ&nÚpmº\x000bÀß\x0018vÇ£Ë\x0001»]bäÉRLXg¥;çàkÐíÞÝìÝøh/_³û8^\x0005dCÍõy	ôÑI?Ôä\x0010ah	ç®&G	}ò¶5ÅCÁP7ø¬ä·&uüö9Ø:®nÞq}fx\x0018PO³¨óJ,¾:\x0001Ï"È¼ÇôpÑts®á3R¥£V\x0001Åqb4\x0007é£Q1F×1ÎÝã3b½\x001eMuS"&)\x0018C¼)bì£\x0016¯Ç|««§åAq\x0018Ù%ÆhÖ3¦qî2ú\x000cc¤¶©ørÀë\x0011¯PÄ\x0018ÒjFèö\x000c,Ø3¸âÔÛ>Ñzä¨\x0017\x000eöZÍØí\x0019ï\x0019
'dFÇ`uR<\x0015\x0008\x0007x®Fì¶\x000cÈ·\x000e\x001c\x0019Án¤<wupG/TcÝ\x0001ù\x0001nY¥ßÔ\x0017%ïj\x001eûÙW3v;\x0006ä;\x0006¸ý\Ì*FÉ®1ò§6êØI=Ähº\x001dcä;&ß¦Ê\x00088%ÅÐ·ö\x001cÁé³À\x00172v;Æ,8e\x0014%ªç¿?5É*'!#êù&T"ÄnÇ\x0018ùÉÂSÞR°Xèð°fqï +Bìvï\x0018\x001c(ë	1\x001b¾´á7\x0015ñ×2v;ÆÈwLöm\x001d1ë7\x001dÕ'Uøã±¦!DÛ-F+_Öáûùèõ	é\x0005\x001eU}5b·\x0018­|1ZO©´!9C³³3#?Nù0ßVDÄØ­F+_Nc/ÑzR;Å«ÑÏw\x00121v«ÑÊWc>ùSãTù@¶NÈÝO2ºN¿Ý\x0002ýöØ6ÆÓ\x0014_Ííè`õztÝqò-ãòhÄ%Xn\x0019\x0013ÛÑÎ¥Ç\x0008\x0019»õèäë1ïå@ógôtñ*ç \x0007\x0018±\x0003þjÆn=:ùzô¦®Ç|ÛRdG_\x0007\x001a½Ú¾[^¾\x001eqV\x0018!êêÝú:Ít¾¬°SG/WÇ|÷lE¨ã\x0011ñ¦JþX\x0014o±[~ÁjL<q-FØ¤S`çvz£\Ø-F/_ù|Ö4e2Dj×£±ò\x0018Õ|kW	cè\x0016c/Æ|Ö4\x001fÖGN_N¡ÎLó\x0003,D8\x0006¹8¦)£«0\x001azä\x0005U\x001fy]ZïnË\x0004ùÉ\x001fsEl.\Ì\x0018ùÒÅõË1ô\x0001=ùÕë\x000e2cýÔóÓ.DÝ	ò\x001d\x001aâ_Àt[/_áÝò\x001d\x001c¶N\x0003P~gFÏf¸ÚÝ\x000bvL¬F£AÜ"àGÜëùNÉ"ÆnÇDñIJ±cA§]­ùÃéùvÜ"ÆnËDñ2°ÑPóÁÌHIÁØo`ýzìöL\x0014ï\x0019LV¦\x0008¦Tk¾\x0011:uô9f1u{&÷LR<»)\x0004\x001cÞJë\x0011øÕÍ¦ù9\x0011"Æn=&ùzÔº\x000evZsfF>­íê/ºÕä«1{Ýä|Å¦ß<\x0017!Z,]Ø-Æ$_z;Ùxjv\x0006ûVçópõ}P«þÕHÉW#(*8\x000e\x0001ü	D\x0019vÀíjçV«þÑH\x0005<{4ôú\x0016æ	
 lÝ0îè\x000bæ\x0018dÿj¤ä;\x0006gX\x0012d¾l9RpËýÖ­EiÕ?É(ùÌË°¤>aÅ{½Ëð·>0 F¸óB("LvT>!â³\x0011-H®ºV¯ß4;Oò7Âiúl\x0011\x001fï·.\x0005'ïØõzçPþDo¬Þkªl\x0000­5o\x001a\x0015Wïì'Bù\x001b!Î@(Ï\x001aÎ§\x000c·X2iõ1£û\x0017B-"L5á2x£h$%¨#c§¬AöFþFJÛ\x0004	\ïX\x001bVF\x0013¦j1ö{FþH¼¢Áà5íj\x001e¸\x0016_íßêþPËß\x0008±nªäk\x0005_üñ\x0002Éñ2s`,£\x0008²ß2òGÂÙ\x0013c>õè03Rek4vuB÷oZþHc|J9\x000e`R-hE]%¢Yý ÍN&|Ëà³[9
q\x0014\x0008\x0007]\x000b6àhêÛ\x0018c¿eä¯)q£²àJó­{Ñcúòâ]ó¡\x0014	[¿íC\x0011s[Î\x001e>~Þ\?üãöéï¥(ìþËíýãá²úG;;9gêQ\x0013Bimý¶ïæÙÕ«·ë«?Þü©T]¾;½¼¾9\x0006
\x0013Ùö%Ðþ;üqªþ?{xz|¼»ûLf}óøÏÿ>ÒMÊhlÅ/Ã\x0011-Vl½^ò¸l{à`ýÿÙÕÍõõùù[2ìüç# Sk?\x0007Mw_ø\x000eL­c¾úëÃýÁ®11ä¯<å£äÛ\x000b_±CöÐ\x0013õáÌMßt\x001aÇÜ¼¹º|w\x000c,v\x0005NgÙêæ\x000eÝ\x001ej;ÃX\x00159\x001el\x001dm\x001fÑWZÚh×&Üî¶ó=;}û,`­.\x0000µ\x0011b©!ÝñXSÏ%D\x001eúu¸\x00080tAlB«¸³9föS«°àyBJ»ßWJ\x0008º%\x0004-&ÔÇ%ëü©L¬Ö\x000e\x0007å[Wb\x0011!t þÈY¸Kî×ªðW\x0016T×ëo\x0011¡é\x0008Ø\x0005k"Ì·kËs\x0008\x0003ekÃ:BÓÙÐÈm3jlimc¹íSþ´\x0014=.±+	}Gè¥øÌ\x0011KS½¬['T|à¸=F²mÎ%¶\x0003´\x000b\x0000Céçý°lB=¸oÑÑ\x0016ì#Îvj=Û#þ(`\x0014}rÀyßM]å\x0012\x001aì®¤í0ûøãwmK¯LûøðñX\x0002ÅCÁ0\x0008ÅåÛìîNÐ¶òÊ¬×W¯\x000eç¥g@<Í¶s2î\x0018üq\x0007ð·]E<\x000e@o\x0001\x000ff1\x001ciVA2A\x001fä{ÆQ(xÎ \x001e
Í8\x001e\x000eüVÒO\x0010\x000cLçqà\x0018\x0016gR¬â³=ßÞ÷}O[¼.\x0017ó%eAs¿ÐF D|\x0016;\x0019X»µ\x001fj,æf}÷øøñ.\x0003>çüû\x00005í ÌèÊu}V^¾?¿¾~uÙó¨ãd¶Æ£Î')þ89ª\x0017\x000f÷ù¼yñëío=²i§\x0011¶¨ÌUö8ÖDµã ^\]¾|»yñãéë7Ç6l,©oÉðG\x0001õtd`é:Ö¬&Yhu£F¬àªë75tvÔ[\x001fWØgÙ±yÿ¿î\x001e\x000fòe7ç(eß
oj¸X\x0007Ú:vúëc74\x001cÚ±ysúöÝùÍõóÐ3\x0011ç|\x0016×%\x001b®\x0014v4u\x0012\x0018ó\x0012vk\x0019MÏhär °ýzyÊZ\x0013mÍî(\x0000\x0001£Ùi}í%©õÝæííãÛ¿\x0006U?<ÞÞÿw»Çgd¨2³ àµ\x000e&PO{89|÷Á7oO¯ß¾,]ª~¸>½|×»WÇ¦-Ã\x000b¶]ä-.(]äßMÍ¦ÆO§ù\x000f¿a{¼÷º¼{ÊÓitJ¥2/;\x001b5f¥y\x0005Øþbònjô´¹Øæ¿¼Æ\x001eyG(í\x001e«ÎðA\x0016\x001f«ÞgÀbÐg£±¾¯Xö¨ó¥\x0013ø±/¶\x0013'ßg´bÆçô°\x0019«[2üq\x001c
+\x000b¨Dã/®~àxl¶±\x0002ÍC\x000bfÜjùà0ª\x001d
\x0004¥kêi71Zô\x001d\x001a6G\x001aGÃ¹ü\x0016¥ià1(\x001fX«­[fjÑðÇa4­4G`B>Õ°oötòrô\x0012´\x001cÌýôË£~¼ã6BÛæAåd{ºYS?MCÇËLw\x001eîïïÊ*íi¨Óy\x000b¸K²Ó=\x000b_(lvUçCíò¼6»Ã#îæ|
g\x001dì¬Ùáåÿ\x0014X\x0017Jï,Ä¥Z\x0000ñJßJÄ£sc-^ÞKv\x0001^¾MNñ¿Ê<\x0005lQ
\x00052\x001d\x000f¸_Kÿ;º\x0005t §I|Y¸³LñLgé\x0012eÿ¬¥Ë\x001bÔ/¡ó¥#JÆÃ7\x0007Gx%âñ"]Öâå}\x0015¥x&å}Z¢ä\x000eT>%
ñ%£Ý;\x0000÷Uè0Ô·m&óÇÃËëW/Ø·
[jCù¸øú5í[u\x0000O¯±ö²KMWþ¯xùe7\x0014Hø/X^~¡îÝH­F\x0016\x0011þíÖ~J°«ËOw\x000fOS\x0008ãôþ/w??<=~9è³ ÛbÄ4=´'oã,\x0018©ÓHËw³yw}u³ù~szùò<ß+¯\x000fµSï\x0008\x001bi\x0012ñï\x0013a\x000c%	2Ù\x000cç
¤Æ.j+ Óï··ÿx¤\x001eo;Ý2ÚÏwGØò¾(	q¸CÈKIhT2 hrç»\x000f<="e¦\x00172»\x001e]úëÿü;uñø®\%7ä\x0006\x001cáqÆ
¡Ñ4©±uà4áxÓ\x0015Ù	&/ààáÏ í6\x0018B1ø­Êæ4%ÙiZGYZj¨ÇQTiwÏÍ\x000cË/pÝOÝ³ójÊ\x001fîØ:çäÀb	ÅnKU·w\x000eOhê½É_ìàGª@Ð\x0002Á0PP%s6\x0003¡\x001f©\x000b\x0010ÐÙé\x001cw7\x0003\x0016È\x000c\x0003YUÊ&ó¥Ñ¥Ò\x001d;á\x001cBZ>ÙXi!mì8PÀWÄ\x0002\x0004¥í\x001f\x0002EZDùv!kÜ\x001fÀB¾\x0005òÃ@F¤\x000c¯I<o3k\X\x0008\x0014Z 0\x000c#\x001aì\x0004/æ¥**\x0003\x0019ò\x0019ìò5\x001d[8Ì£qÀç\x0013â	pÙ<txXþ/ãI-O\x001a·¥ËF\x0006J¥«R\x0006Ò\x0011¬Y\x0006DÏ»,Jb!k«c\x0013Ùj¢L÷B=¬Ô.¸25\x0013aat4¦Ç;³\x0018\x0011uJ­¥Ú¥I>¯:¡o¦\x0013ó°§\x0013j=¬ÔYùJñJ>è},©+ÙB\x0016hÛc×D0êae´&+9Ì&e×ÃÖÃ\x000c´[(ÕºSF=,.ß^è¡µ"}4où£Y·\x0010¨SF=,ßÐD6êaqtÎát¸\x0002\x001eÎy^Ev)P'zX\x001d³3_}'Ïlò\x001dØ@Ð#\x000cã·ûfÐ#\x000c#f\x0002ºr$(ï~Èk¾¸pëCïÆã·ZEÐ©#\x000c«ã7üh\x001f\x000bÃ¬3±\x0008{æ&1à\x0017\x0011tz
Ãzí\x000cÕ]#ÇKl¹*FÏDa©:½q½P¥áÞ7eb|&Ò¿_è@§×0¬×NSã\x000c¤\x0015ü' ¼î\x0015 Å«¨k\x0018ë¬8xZ×¦UuPüÉÌR\x0003uj
Ãjm+oÈãÊ\\x0000¢Ä<\x0000ËL§f\\x001bf·He
 H~¾\x0003ññÁ
ðäD6amÌº\¦Hc\x0008J+9"Í\x0011\x0019e\x0016n|ÓßñÇÅ1_\x0013\x001dÙ\x0008[\x0014¢|M¤U­ãÒ\x000béÄÑ\x000ccö[K*U&²Ô\x0015\x001c3ÐÈD:Å¥Ë¨ÓF3¬ùvxBÛLkz4°\x0006\x0012[È/\x0006ê¤Ñ\x000cK£5©n4\x0003¥1N»L¿[¸õM§fX\x001b1ºgh]+{\x0002\x0014Ý«Èë¥@6qmÄ~ò\x0004\x0004ª~´
\x0014\x0016[¨\x0013G3.ßÌ	±/kÇ}Y´\x000bíü,\x0002´ñk¨¨N\x0003urmÇåÚ«Ò\x0008Mdëù\x0001ªÊµ]JÔÉµ\x001dk,{¦­¯\x0002l)â\x0008¼ÑüRq´\Ûa¹6yëOaY\x0007],4ÉM´4'Éúì¸\cý-H6\ÙD_cÜÒXíÔÚ«µ±e(l±\x0010m4°õ\x0001,]E\Ûa¹6)QPV§\x0014ÉO3ÆT\x0013-½ÅÚN­í¸ZoÁ1Ú\x0013\x0016fuTié"êäÚ\x000eË5hÆB~µ:µ¶Ãjýí¶ëÔÚ
«µ	ªttÂ\x0006*¥(;!teÔÆ.¼ç»N®Ý°\C\x001buríå\x001aß`È×Ä"\x0008¡ný¥wF×Éµ\x001bk\x0000(Má²OÆuÉæV¶ÒfáÊv\»a¹6N\x001cè«Ù2L\x0004\x001bdòÖK½Y×¿¡
\x000b6øP$f\x001bamcQ#mÙWSN-¼\x0013¹N°Ý¸`[Ã\x0019`ÉÆRmDóãÐF°t¯uí\x0015\x001b´:òªRQ\x0005~Wµðub»qÅÎÇlä3Dàée=Rné:ê4Û
kö46»|Ä è´À\x0011Qö\x0002\x0017®#ßi¶\x001f×ì|ÎFJUÁ¤iÃç,\x0001¥°P }'Ù~X²³I %ÿÍø-Nmä>>r¢N²ý¸dëXª÷\x001c6ý/\x0015ÙDã\x0007åÉ:Éö\x0002ÉÆÉF¶Ä®U\x0002Çz\x001d®¡N¯ý°^CeÀWÆÉH'N1P>.aùN¯ý¸^ãÈ\x00062¥A\x0010i÷öK?Yô0¬×ßÐF^ûq½\x0006SÆZsß\x001b²\x0011 ùÜ_¨×¾Ók?¬×\x0010i¢'&`iNÄÐ55m7\x0001K@Ôéµ\x001f×ëof£Ðéu\x0018Ök\x0008\x0012\56P-l¾|\x0018>@¾¢N¯Ã¸^³\x001d:½\x000eÃz
ÞÆ[xÈ\x001a~¹ÒïûÊ,u\x001fC§×a\¯¿:É\x000eãíBÍ2w¬®ëN±ÃxH\x0004ç[Ïo_dA;N¾Lqá½(t\x001d\x0015;\x001fö¥¡7ÖXx`+,â¡\x001a¥ÁÇÐç©ÇD¾:Å\x000eã­]uÖ´*Å;ÙF\x0001ØYKzáÝ1t\x001dÆ£"ßÌF±Sì8®ØØOm\x0014Nè\x0008	ÎM´ôÕ:v\x001dÇ"ßÎD>Æq}\x000cúÏý2´\x0003Ï´z\x0007qnáF:ÆauÔ±\x0006\x001fÃöQ6\x001bÎÐ7³K\x0013Vb'Q\x0014à\x0013$\x0013º7ZN2Rn©^ÇNâ¸÷èU\x0019.@w¾6ÕW³KïÖ±ÛùQp·¶\x001c5Â\x0019\x0002tÛ×\x0010È,MOÝÎOÃ;ÿÛ-£Ômý4î¬9UÆã hb9Ú¨nµ¥ù\x0018©ÛùIpýV\x000evêvZ\x0012\\x001d]=DÄ\x0008h0ÐR\x0007;õÙ×ãëZ¹í\x0011K7Y\x0017ëñ¡\x0019HïÔ¤¨áEC¼\x0003-ëüGv¬á
Å°0\x001e¢û"©1ð¿z§yûÓ©ç@\x001b\x0017ÁßlÃkx¥\x0005:Û¼®Â½tÇ9ýÓ.\x0008©¿û0ì\x0000LAuù\x0011\x0014hËk<¥\x0015\x0018n×ZN`,o\x000c>ôM!6XJë÷µòÁ/ÍvfËH¾bS¶\x0019\x001c×\x001bè»®l\\x001að{ËËKÀ¾ÙÅÒèn[¬|BÜ&!z\x001a]Ù\x0010+\x000c×d\x0017q@ïZ\x000b´ÀZ68Z÷o<ü®dë{\x0000ðà%ñçÍø³À\x001b7±nFz6ÉÞ8To|q.À®µ¬dm|ÿe°üÇd)§¬¾,~óRæ§/wÝêú\x000e1¨\x0012nR6©DHeÐVVd(vaÓÒååö´ÞI´Þ\x0001Æ%ÍÄmÓL,?6{XºîaoÝ\x0004ìåu©=]È*¶ø.Ñ\x00030~zò-¥kãÒd*·£^n\½ðptôÚcTMbà´÷\x0005\x000fbÔgëo¡¹·µï×\x000f÷¿Líê¼9¡wc¹\x000eXG>°µÚ/Ù¾Ù\_e²7×\x0003dÐ,*t ¨\x0018¿æC\x0007§ÞLSÿ\'f³-±¹mÕÔUî¨s-´Ûïe as-±Yà/w'¹:ÝB
aÕ|Kæed¥TgJá1äH§ÀÍ¦VÁB\x000b\x0016D`F\x0005NTÁ\x0001 ªÜ;@Õ»bRûMo$l©eK"6=¥\x0015³¥2Ë\x000eoiü®ý ¹®\x0014ÃhÛBÙI;Û4ãûµãú]¥¹)
\x000e\x000b\\x0005×ÉéÎÎ¢âØ§Ç\x001aRÚx½ß+H\x0002g:8#ÓTC?¯¦Z~ªêZ¿J>t'mZ¦m\x001aG¢ÝR¢\x00088½^\x0005X% ºÛ§Z¶Q³aêë{¤¾àØC&Õl©¹î'ÃlÐ\x001d¤ ;I¿­LÍFÚ3A)Ù^Åèmç\x0018Ö_ÐÕéÞo`4§w\x001aä_l\x001b£aç×·?ÿúÏÿÿñ¨#IgÄ\x0002YL,
f½MÎÏ´\x001dÃÞ1¯O_üx>Â\x0007-\x001f\x0008ù\x0002Vwì|¼²ï\x0016âªw$]ÇgZ>#µ\x001fP\x0010A\x001b¾·\x0018\x0017Ùx1íË°\x000cÎ¶pV
\x00174UéNA\x000eJ¼jb\x001cû\x0007¿ÎµtNlºì\\x0016_.æ=âÈz\x001dié¬ã\x000b-_òe¿Z>aÆQ >NëU;e|\x000bðRÄ;Wñe>bsòH;·F\x0019ô_'âÓ½²È¥ES\x0003
Ý\x001d\x0003Ö\x000c[0û\x0007\x000c°ÛºZ¼w±#\x0003m_ç9¥Ì$Ã
Ú§»
¢Å;$c¨TS:\x001c¥úr\x0001kÅOw;D·H¾±\x0000fu¦ÖHVÕ´\x001c»ö\x000bw[D÷Hv©\x000c'çmQ§ª\x000f32\x0011 t{\x0004Ä{\x0004'ËéúæZüª\x000cXEÆ\x001eèÜ6Ì×m\x0011\x0010oàÊ\x001cSäKe¼%Ö2ÛÊ\x0017fº/\x0000»-\x0002â-\x000c7xK5´c}ýÀn­\x0008B·C@ºC\x001c6ü$\x0003&W\x001bOåò¶^f/\x0000»-\x0002Ò-â4Pù£NÊr´ÇFþÀ>­Ô@Óí\x0010#Ý!\x000e_(x\x0007rm®Á¨¸r\x0003Þýn\x0010ì©aÈ|`©)\x0013öe«\x0017ñµ|Ýþ0Òýá,Ô\x0019LÕÒ\x0005ûjá¬ùÝ\x00061â
]\x0003Ø¦.Yn"¥ëËå\ßc\x0011`·AxlÏ¸Rß¾,w\x0004QÉ¯@Ûí\x0010+Þ!ø\x0016@\x0016´õUÇq\x0003Z­Ö*í .A\x0015Æp
amòâ½\x0018mVºù¶[Vº\x0002=Nÿ¤-\x0004ê°â#·\x000eÒ\x0000+W íV ®@l@É]\x000e\x001cM|Áó#[ë\x0005ºn\x0001:é\x0002ôæ~n¹ªy·ò\x0010vH;©Hû\x0010j?T\x000b\x0006Í"¸ú¦äú°x \x0013C¯Ø¦®À`
\x0018íÊ\x0015èº-â¤[dv­©\x000cÏ[4ç³ò\x0014qÝ\x0016qÒ-\x0012 v U¾V\x0005o\x001b Ï4g\x0016àu1@ÄÛÆ\x0000Ç-\x0018É\x000fÌ\x0016¬í\¯åø)¬UÁ.N\x0012üì0²uK®ãÇ"Çuqz§pXBév£Nµc\x001c®\x001fî¾ûòåh's\x001cª©9WÞÒtØd¹¢¶³Ì¯¯._¿{w¤yÅ\x0016\x000fx*»ªDø\x001c¶<#!ÓÍ<ÊÈèLKgdtØ·«Ü!óP,0lÛÎw\x0017ÐÙÎ
é"w\x0007\x000c\x0007º©»¤\x0019/ÎH \x0008Ïµxî\x000f·ò|çåÖÓ¬ç9P÷-/=fÇs\x0008ðB\x0017¤xûA¿]néµQl¹$èRKþ@ßÖíkhðùèî¿ \x0019Ã\x0005K£\x0007P\x001f¡y\x0013<ÞÎÿóy,h±`\x001cËa{\x0002jì
1M¿§;&F±Le\x0004X	EidùÎáé2\x001elmCnçÜQ,×b9ÁGÄ\x001bn\x0011^«\x0013u)ÈéGysÎü£T¾¥òãTy}ã\x0014b,ETÙ!ñÕVs\x001eÝ(Uh©à\x0013Öp\x0019\x0018[ûØÈYëW\x0019+µXI`,íF+KÕ~é¶æ¿Z3\x000c"Øç6íÅÆq{ÞhASâ@¦3'b<gJä{ÄÜõá9:åw<6ìH±}ÿ\x0001ß¾3Þ»Û{TØ£\x001b p?
[[c\x0005\x000e Ì%ºý¯ßñÝé%JìóÐBÂ\x0012Hj Ï$nf\x000eIÕîT³ù>bPÛÚ% ¡>
a6£¢g5Å­tTÙ"\x000b@]\x000bê\x0016Nï§ô@\x0019\x0015÷!1!rlÔÎ\x001e% vçpÅ@U\x0013»ÀñÉùôñóQcæýBáÑ\x0005Ë\x0000¶/l~þæ½9yñêí\x0000\x001c´p \x000bäÕiDM¥\x0000 jI·\x000f³½a8ÛÂY!®û\x0005³¼jÉi\x00114{¡\x001ds-\x0013Âå#Bz\x0011ËN¨¿\x000bzKôpªgc¶Ãp¡\x000bB8\x001crÉý\x001eò£ò\x0000¨Ý¹ì|0e\x0018.µpI\x0008Ã7Èr qù\x0015\x0019<%1ÍÇÊFát¿[¥Û5ïQÃ£Ìêä¼\x0014¹8=Ì¿ç\x000eÓÎHé\x0012õW×¶Dýq1àìª\x001d¡»\x001d¡¥[â­ºiP|7\x000fK7nÂû/ÓUììñ®x9\x0007CdØnXXìÇhÎÎÜ)n6o®.ßM·±³ëó³WG®b	-&,ÁtÛ \x001b­¹(\x0019£¸ìmÍ\x001ekbPÓ% 8\x0004	*(ÝºCàÄCô\x0019¾\x0006¨kAÝ\x0012PÌþ¢È\x000b\x001c½\x00085\x000fÇÄÙÙzÃ elv{\x000bÖ}ýðôéãý\x0011>À÷
N\x0004\x000btUÒçÙáÅ\x0019¼×W7\x0017¯.§2-Pú½\x0008©lKe\x0005TAÕO¶6~°S\x000eõL jÊµTN@\x0015}Í\x0003\x0002!ju¨%»³\x0019¸Ã\x001f°»½\x0001\x0017LýK¿ã\x0007¬Ûmß-ÎÐxåÝâÅ¯w¿}¼ÇãìéÓçclÚY~Z\x000e\x0018Q)YßÑr~«ê#c/~<ýê\x0012³·WÇlçw\x0017¿\x0016a»ûínÒ±éØËºeãK.7ã¨\x000fè>ý»@¿>Ô£yhâãì\x0016túq~Æ	ÂéÓä\x001btÓ§¹}gúôÅÞ\x0000Ögñ Å\x0003!­½?1\x0005d\x0012çâÚ\x0004}8h\x0001mñ¬\x0010//>j±\x001bl<¡ê\x0003\x001e\x0013cé«Û\x0017Ð¹Î	é;¡í2=¦Øk1q%oé¼Ne¯ÊJB n\x0013&iþ°.®\wZuÛB	é«íK0½«\x0018/Än©ÚÐ*æëö\x0016n\x000c\x0005¢¨2&×\x0014óÅ:ºQAÿ"*åë$\x001aRB\x000bj§°:ÍÓtqEË/\x001aþÂq9!ì
\x001fLÂ·b¶3¾´äíxçîðÝ<O§~²¿*û?hóâýñö·»Û§ârÞ~þÿòöáç¿=Õç\x001fêö¥¾{wûø_ÿÈÿÎûbTÁ§äJ÷\x001c\x001c[X%F,BGºÓëÿüów?¾>?½).çéÛ·ù/o¯^üûÍ±7 ÚZa,\x001e?Þ>}8ÁÄÜ`»${ï\x0018Ú\x0005\x0013Ê\x0013UA©-&~à\x001fOoÞM|ÃxÐâ\x000co
ë\x0006²¢-iÖFyU2Ðå\x001b¯À3-áùò\x001aÖ³\x0002ÐF\x0007úÈ1ù\x0015x¶Å³Bë9ÐCÐ ¬A\x000f¬çR)®[çZ<'ÃÃùZÓCQ\x0008>ªòqó\Ö^Ê»eíÇõ-\x0017Z\x000fè·)\x0001\x0017\x001e[OæVÐ.ÈèU'\x0005.f¿eÚ·B*§GÌ^U¹:® -]\x0014Ña\x0017Òk&Û.&¼!¡ñ-o\x001ey_ÌÌåtä\x001b°è)ñ\t¥X\x0008ÎÐÉaò!	´1¸]ç
¾Nõ´Pöðrº\x001då¯ë|iv\x0001)ªR¿®Ó\x000bw\x0006Z®;4&SnC\x0016g\x000f\x001f\x000fRéDuah4\x001aè\x000eÉQÉF>*h\x0012ÍDE·É³«ñ\x0006\x0006Z\x0018\x0018I\x001eP`lé)alÔ\x000ccÍ2\x0018ÛÂØ!\x0018l»f¦õä¦h\x001dPåLâJ¯Äµ$ndÁY~kD«(If\x0010±øÅ\x000f²¤\x0012±É0\x0016\x000ba<ðzå/	-L\x0018^/S9r	¦x\x0012eÊÊ^£Y¸^b\x000b\x0013\x0007-\x0013Ê¥\x0018ah´\x0003Z¦\x0010&Øe0©IñåI+¸¼hJ4\x0017-\x0013h'éàÒ"ªÑEcÔi)s8\x0002®ÚÒ¾&Ó!<\x0011ýe,½Þ	\x001epR\x000c1*]\x000cãU¤¯dî¥Pãzu	7q½ÿË«Ø¤óÀ¤é<xÈGÕtåùáaºòä_ä¿Þ>ýýàïñÒ5ùê\x0001K"C9óc¤C\x0015|k¯«|`M\x0017\x001f®¦\x000bOþEþëéÍG5-ªYSÒýv\x0007¥¼Þè)[üve¿
ªî¾ôdÙéKÿ\x0001\x000bmZAù\x0005\x001eÅo>Ýþ<ó\x00168»8½ÁyÝÓ¬Ui
\x0000ÉKôÉ­Ó÷æâôÅÈ3`Cf[2+"\x0003ëÈÏd¦Dr\x0001+\x000b\x0008,Æ5`¾\x0005ó °ØÅ?\x0002Ùu>jÅfóÃ§¹ÿÇÁ\x0005V\x001a}NPÙ»\x0001Z`¡4'ÊXÉìoÛÍ\x000f\x0017¯^^þùy(h¡`\x001c*Pæ@Ê^N1Ó¥o\x00182y½É´Lf	GGsÏ°P lT\x0015
3ÙÉ
\x001a;y¼H\x0014&ËHi_À\ËäÆpJ|Ú~;ZP.m?Þ
(ßBy\x0001.5[\x0019Ê\x0013\x0008ÊðÍFy¿\x001c*´Pa\x001c
4¦\x0016K\x0005lÙ:A\x0019
g©CÕb¨ØBÅq(\x001aÕ<Í&\x0000Ì±ã¶+¾^jfYã×£ªcÀô5`C¹¸\x0018ªñ¨
yÔcT*_Ý=QùxR®¨&ñÇ\x0003µ|Eé^ÌÇÕ\å{\x0007Ðæs¡¤»\x00006âf*­«îÔ\Ë¹²
\x001f)K\Áð¥Õ\x0000E³­YNÕi§\x001e\x0016Ï|ò½\x000e\x001c\x0010\x0002Mî_\x0016*µüÑzêqùÌV.9®(
E\x0001b¨JeW¬õN>õ°~â\x0008Y=ºìÆi4\x0015Df[E³bµwú©\x0005\x0014?Véù\x000e+©ôÊQdfº}/ 
m¦rùEçP½E¦Í§»Í»/\x001f¿\x001cú1#h­2¶Ôfæ\x0010c¢w\x0002åf,ö\x0016Ñ6\x0017ç7çï^½{1´AÌuz\x000cù\x000bR!®Q.A}PÙÃn×]9ÕTáúxÿñîñ«\~ÚâÖëËW«[\x001b2Ó\x0019	ÂÄ©rtkìQ´#äyE\x0015ã*4Û¢YÑJWEDÖXö*XÖ ¦Uh¾Eó"«%¨VÃ8¦#ÓÄöåq	ZhÑìºw\x0011òÆLìµâcdAË÷!»
-¶hQý#­5R¤×8M» jX·ÔRKDdQ£+=\x0019
BIfÈhT+¦Íª¥Ö¸f(\x001dJÄ/xåÄÂ\x001d\x0001Äfè6ïPµÔl»WÛ¾ö<Ý\x001e	6\x0006ÍN¦ôf®¶ä_kÝ-ð\x0016¡NÆ\x001b»nB²ÃH8\x0002çÉpHÖ\x001a:\x0004òGÜ}\x001aAê²xË/zññøðñ3\x0017%ÍKt)DC÷æ2dK\x0005Ã÷ÈèæÄâÅõÕ«·GJ\x001a6hÙ@Æ\x0016\éá\x00143;W\x0017'j-3-\x0011ÂÅ\x0001]MrÖ¼óÀç¦[ú\x00028ÛÂY\x0019\r%¹7\x001fOÚÏd¸P§ö\x0019v\x0011ká\x000c.n#tùÎIÏ6Þ;vs½;\x0005\x0004p¾óB8K/'8u&Òó=mîÄ"¶Ð²\x0005\x0011Á¬²ä07ü¡`«áìÚ%\x0017[¸(Ã
à4z\x0013\x0001¾&YgM\x0000Z¸$óùâRîÆ\x0010¨X\x00190{7«ña\x0015\sÚ9D§s¶´ÃF:Ë·Ñ°½aåÛà:ºþ\x00106xÞ®Ó8B¨]^¦ë\x0002hKèº#BËÎ\x0008,¤¦Ô\x000e\x0008PÓ|àÈºQf\x0011Ý\x0007\x0005©ÉEÅ|¼9\x0017u³­\x0018øááþËÝýÝ§O/\x000bùÚ\²Ù§OèÅ\x001c\x001d6m³-\x0018øáêòÝùåùÅÅQ?)î^ÿ"{\x0000¯\x001f\x001e\x000ed:\x001bCé/\x0001?~§ü×W7×Ï|P¢1-\x0019£Ák\x000b?\x0010æÌ\x0002jL\x0014o	ËplcG\x0003ôÍ°W@½\x0015kÃ) 4z`\x0001kqÜ¨u\x0014«kf`÷Ñ¤\x001aÜóÊ/Ä	-N\x0018ÄÁ\x0014\x0001Í».QX6Ð\x0008æ0\x0005\x0019Î\x0007­}÷±Î4Þ½¦½Vê6·÷w÷\x0007£,¶\x0007çbõ|~GJØñj5xR¡Íéæýùå±àÝõamåuqûûÃÇÇq³Pßü°\x0007E3\x0008­ mÕ^ªÌÅéû«W×Çò0vßºµÛqªïîyüÈ\x001dÍæ¸¦yTå\x0012U|å>\x0019Cp5r1{\x0014_~}ôÎ¿`\x001f:ÃA?¾àýÍw¿ª¯9*<'×Æcb7A\x0019U
3c4\x0011úïwùnóãù÷¯.·¹ð\x0007qL\x0006BÂ_\x000cQ\x0019P\x0014æ°Jô:\x001ajÁX:\x001dà:l¦¤ûs%ÿb{®¼¿{ü²yyûéöðJWÑcè\x0004·7¢¸Ò !º cw¢¼?¿~·yyzqzd©P>îvYZê¶${l^>|øtw\x0008\x000böÙ"Ó\x001e4ÆwAÎÐCw{ð´dxl^^]\x001fã
a+¦"äÇÛûÍxw÷øx8«\x0017\x000bB¦ÙpY\x001fðö1E`£ã\x0018§÷M\x0002³R¸>½Ì\x0007ñÛÍ»óëë£I³ªÏì9C7rñkÅÅ3)Çø\x0004\x0018(-\x0011ÓÓ\x0003Ýmp\x001d\-´àÙÙr\x0010~rðWû7\x0010àN¼¼ûíîñ\x001f¥\x000cùìvR®2õÙ¤\x000ctDÑhç ¸ËÙ_É\x00121ÅO¢öªDÃf¢ËËÓ?u×.¥Çg§\x0007Ä+Ó<|Öwö©¡AÑzyûáñãÝ§Í÷w?ÜÞ\x001f\x0002\x0002,WÎ\x001b\x0013B>§Ëvæ¤fÖ1.öPµ^e¹ºÀ0ÊÙéÝØCe1¶\x0010(ïÿ\x001f£u5­¦ÛÍõÝoù«ýó¿ï\x000eá(\x0003ÓÐCÄ±^Ù!!»OåMkêÒ\x0014·8y\x0003^£\\x001fPôÌñ?õ»ýH.úä¿úí¯\x001fî\x001eN|üQÞ×ì"²A<g\x0013mtå;êrWuHºyõúÍæóë×tØ¼Ç|¯ÛÇïþZþ/áà\x001bÖö¡_4á.óOO??\x001cùbæ\x000eýe§'Òi\x000bôÅ0s´û`ß\x0017I¿¸yq¨r·å\x000b\x0004\Y±Ë1c°\x001c§LÝÈ¿¦f­y%ÑèÊ¥`¦\x00053\x0012%ÃÊ&0\x0013Ë3Gþ5Å\x000cF/Ý\x000bÁl\x000bf\x0005`Q¬½ô	&¶f0\x0013Ùb^1CKÁ\\x000bæ$ÒP¢l1ì)RD\x0001£]è¬\x000ekÀ|\x000bæ%\x0016Ãf'd1¯KåH¶\x0018eÆeé¸jñ\x0016,H,\x0016¨ÕE\x0006Ó¦Äf2\x0018_¶Xðn
XlÁ¢Èbav\x0006£9\x001fÑ`'2\x0018¸U\©åJ¢µOé¸öS¹ìdQ}0~ÉU\x0006ÓªW%²X&	f0\x001c³Å\x0016+ÁS´Ø*}Õ½îK?ZSÒ¦ÑJS>òDFýö]ærktLwÊ¯%Ò\x001fñHÒÅf\x0011*6ü1MXEÖ)¬\x0016I¬\x001a¿Nd8GÆ\x0012YÃÉ¬]µÌ:Õ\x0012ù\x0006\x001bÆâ\x0005(Ñ:Äâ\x001fÔ*²NcµHd­b\x0007\x0003ÛÓ±f\x0000KSkÎqÝI\x0016i5¬\x0019I«rE0Ï&ó°nkò%»ÙM¿Î\x0011@ô\x0001SÉóË|ù¦M\x001bÔê|4½áÃßÖ/»!EÃ\\x000b f\x0005uÇ§Ý5 \x0015Ú\x000fo ¤½Ø\x0016v«â§y\x001dÅ×>xPí¢%!\x001aÆm=H¥óÊñ©àåhÊïÜ\x0004²c´-zñðéá>_àNÙ=ýòË\x00112J.ÍÎ¨)\x0013\x0007voÛ5ÛÍæÅÕÅÕe¾Ä~¿9»ùþû# ¡\x00041d>\x0017NÈ\x0005Çk91ÚêPÞÕ\x0005¦e4rFOÃñ JSî\x000c©<ßá+0ÚÑÊ\x0019
½fF\x000c³gîùÊ`±=ÈjH×B:9$&¦Ò
\x0015\x0013\x000c
£aDçw÷Ê\x0002Dß"ú\x0005ºäÎfDì\x0002ç/\x0012\x0016³³WC\x00162,4X<2Abo5$[Òì¹\x0008\x0012H
»\x0008`ùùáöþáËA.]³\x0016¡.ù\x0005Ñ(\x001a°§úáôòê@t´\x0005\x0016\x0004@òåTó"`\x0019m9pS\x001crð»\x001eñ iQÌ\x0010J>\x0014ãh\x0011	ÅêÄêaõ"\x0014Û¢Ø±ÏJGÐ|Te\x0014(wQ\x0015\x000c\x001f\x0008\§%Eq-\x001bBqÜ|8C¤½ogC\x0010ÄÝ¥\x0012y©¼øtûòÿ¸}üü[F8\x0012\x000eÒ'ÖÖó2$
\x0007ñêu&ìD]^\Þäóü?N¯ß¾Î¿}\x001eÏ´xF\x0011GZHÉâØ,êï\x0006K®À³-\x0015âq$
ëîå®Ó¬$s-\x0013eçÖÆ\x001aeÙkË\x0017*\x0017ÒZ<ßây!\x001ez®Ø.ÒXgü®|­r\x000eÖ.»Ðâ\x0005!v\x001c'Êy_ixÕ¥ÝóPL\x0017[º(¤\x0003SF¹à·M´ð´Nl»hÃJºÔÒ%)]*cSÎ>·\x0019\x000fxáÅÝ'\x0014)]\x001bÍ55þi}5\x001eØR·;}[vlãê\x0001ýí*6.Æe9f^(Ëõn
%\x0007UÙ¸¥ªé±@¿`Gçß>Ý}Î\x000eÙÓã»_\x001f\x000e?\x0004åíkØ§MY]<m\x0010\x0012Ç\x001eâÎ\x0006ù·\x001b|çzÝÿxu¨ø¿\x0005\x0016\x0010¤
Ê°Æ\x000c=ÚT¾²J®F\x0007µ[\x000bhZ@#\x0005=¤¤Ì¦ÃCq$ÎÅ¸Ï¶|ö\x000fh@ß\x0002z) è\x000f\x0001íTæZd½Ý}&W\x0002Æ\x00160þñ,Ø(!nb%$tXKä(®Y©\x0015#aµ\x0001u·µx\x0013'&{\x0004N4ù¦Pß·¸'ß
Ânhé.iîöùØ(Ùñ×²\x000eÚ´v\x001bënhé6Á\x0014\x001e Ó8éÒ¤\x0007?=óí^9ä|Ý&ÑÒ]\x0012 ýÀ\x0000\x0014ÁqõEbÅ"¦%)ý¢\x001dÙðôñó\x001d%?Í£YÅ\x0017{ô\x0002\x001d-?\x001ai^ ß}¾Ù¼¹yõöü`úSe[,+À\x0002jU<{ \x0007|Ïak\x0017öäÆ°v\x0003 0\x0005@¶YÑn7o\x001eo?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=½{»AX\x000b8÷S½1
É(«Aßóä\x0006',í\/kA\x0004×ç0ón£[
á\x001dø#0üüRÐ\x000c$c\x001el¼k5Ü85¹è\x001eó
ÜU(þXmô/°q9¤vÇ? ª É¨ßS\x0006ý!@¹á9\x0006x8dL$\x001cK*[;Ë~béç,zó]¸\x0013­Ì»ø},\x000b}õÕõêãcõÑÜâ*	ÿ	HÇJ¦Õ£x²ª97×ó×\x0013æ_zýáçäÕ\x0005?×Á\x0017yØ<Voµ&¶\x001dH\x0005h-\x0016ÓX,|èqîm\x000b#LÈÕeåj»}øþ'ûRÆ\x0016®×\x000f÷OOø~q0*\x0019~_Gx\x000cq]­èëXÛÅÅùÍÍùÁ¡à%rÎþ!Þç\x0002v~v}¿yùcýð°©~\x001dÆ0s/XEBìaå:æÄ\x0019±\x0017"½>¿ºûïÅÅÅú:ðI>üðñ×T_\x0010þÛð³\ÿ²~üøP_·é\x0015®ás¥x-Ãâ9e¤k~¡åâíâòõEe½f\x000eèÝüUü£\x001b\x0014\x0014\x0003\x0002#Ç\x000c®Y©é®ÛúD}Pb©Cì\x000cÞ\x0001Ecüh.4ßÃR\x0011~8\x0007Ü	ã\x001fÿoóÖâ%yÁºÙä¶.7/¿Õ\x001c0ö\x0002}E¯RIZ`pN\x000b#[Ëu1[^ÝýO¾?¶¿%pÚXLÒ[Ç;wÕàkNÀ
ÊÊ¢×\x001a¶ÀL!éh¼]Ä[w\x0017pêXÞ%X\x0011u\x0016aÄY\x00149×Ö\x0011Ø}ÿÞÿp\x001fw\x000edè1JÑûøøç¿«ËDÅB\x0018Lç±Q\&NbôÛO\x0010³Ð^WbU;Fó(@zºl\x0005ëá\x001fá\x0010äBSPDý/Ô\x0004¬	÷\x001dIØ\x0012,x\x0004æ\x0004ÔyDØ½EÛ\x0004¬sü£Û×¸~
Y/OÐ¬I!¼`Y\x0006\x001cÈUt\x0002	ÿç\x0004WI¸ç¤#0,\x001dG \{|ôæ×u\x0004\x0001³&öR´\x000f:±à ÅÓØ8aÍ\x0008
 áûñzÒd\x0003\x0005ØKC>4)a£b\x000cèS	1x\x0015\x000bÕÉÈ
ÑvÛzÀat1Æèt\x0002rJc,7\x001co_J«\x0001\x0013Ci)u!ý"¦.@,~6\x000fvîãzs_½\x0015jÐÙcÉÕÌd¦ 2­G*(`ZÌÀç½¸:·PÐÎô¤\x0013\x0018G\x0000©)aaKkÎx®Äs=ñ\x0002\x0007<á¹TIj!«bø^=LP@<0Ö}ø ÿ6p­´ó\x0018ÚW4}á\x00123O4øD?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=|õ¢\x0006\x000ef³;Û\x0004Gs\x0002\x0017Hhé2ünc\x001f{¬©ãÎ7ÀQ]²Ìé[\x0000'?µI©\x001e\x000b¬ÕÂÁÇi©#º°\x0000¾KpI®p\x001cÝcyãµh°Þ~ß\x0017/6\x0015gÅ¹màsµ©ÉmDt)ùJ4\x0011\x0005RTº\x001eÔ<D\x001b#\áàïF&NxìÉo\x0004ÎÝõÇû_ß\x0017v}'u\x0017³gð·×eÏ\x0000)\x000ceÞOºµN^ö\x0001Í\x001d½: \x001c¡\x0007­\x001e,\x001e/×\x0006+Ä=Ã¨\x0002\x0007û1'Ã0.%\x001eeê\x001e°
zeï£	X\x0014ôÜ\x000eÈ@$Z&æ®¢@±GßFÚilK!¬@£29\x000fJ\x001b6R¸csdØ3@N f\x0015²ü\x001c\x0001§ù¨íØ\x000c\x0005LzF¦YÇ#2=wÓ,u·i¾q/_KÛ]\x0000E\x0008d3?v3G¥F÷^´_MÖD3Ã4S«»ù\x0017Ð,Í¦©Ïd\x000b}q&2ÝTG7ó¨m\x0014\x001c	\l\x0006÷t÷àrùûgª[DO%-§7\x000f÷©}ûÁâÃâ>\x000fö|ÔÔõ`p'\"%
R\x0007\x0004EÝeBÈQ\§>î\x0007ó\x0017óó4ás6\x0008*þv÷ýòwÌFA%Ãw\x001f\x0017·÷4Hù\x0011$X\x0008Ó\Ñ\x001d\x0012Bê{J&g¯\x001aúðàoóÓóÁéÉ½ý#\x001ezZF÷·´¹:PÅÈ\x0006?8#®~óo÷WúáG2¡°:\x0011óÛÅçåÝâûÁ¬o|2æ¬o\x0002Ý°±çª{\x001d{ÖåùéüåáÙü\x001f/.\x000e\x0013H{@Ð´Ä¥\x0006\x00163¸¼\x0017koáYàÞÄYYà¨ \x0008\x0016#âR\x0003Ü02(½\x000b<Û\x000b\x0013·ráñ½l+\x0010¬BÄ¥

èSÄHæj$.\x001f3ÚM§\x0008ÕHx|O¯Â¡\x000eªp\x0000Ëæl6îÃæM¿\x0003_\x0015\x0016ýÞ}½OXñQX\x001f(@®n\x001eÜD\x001f´ätà¤\x0006\x0016ºÎ(>"L\x0001|D# \x00049>¹\x0018ö\x0018{Ðê(ÌQH\x0002¥~«9\å¹oòi!]^.|p\x0008	\x001f7Ó²ê\x001dúì\x0006\x0003\x001c\x000c\x0016\x0015$|³M`éïc®èðº·¿ê\x001cúì\x0004£\x001bÿ»\x0006\x0012^ïà[ ¹È5¬ÖHNÂty®?Ôý·¨IÒ4ïÐ\x0008»H:V\x001av°)s`H©Eâ&ðÊX\x000f)Ào)\x0006îÊá\x0007\x000fDb¯Í(¿Ù¹áè£´ÔC2¹.Éc{ Ï}ü³0ÂmF$|KIËTDÁü	Ñcý«\x0011y$o£\x0011ø\x0012 ¬>&<{ãzÝOì\x0000(àK^Zê\x0001©ï¿\x0003J-\x000c}\x0010Y¡ÊI×ñíc\x0014¼\x0011V`<V\x001c¿½\x0017³_n®ïyü`¢?¥ØÂÅóX¬
oÙÜ2®gmà\x0010\x0006le<ýròê\x001cË\x000f~öË­ÿô¡S\x0002f×%¨´\x0001$hûîQ\x001bê±8Z°±\x0011¢ïçÝu\x0004ºl|oæ´çÞ#»kN}\x0006§ðö&?/Æ(§\x0000\x0008Ød+-£\x0000´æB^T\x0008\x001cèïïF\x0007~±|5z<-ÿ½\x0000ïô»¾R@ß!-¿Ü<|XÜÞ\x000cZÞVä@TÆÒLm°¸%?0ªêåwþrrñb\x000e¾H
\x0000b
\x0000R°?\x000edæí=Oiñ}:º}x/?_ßÐý~Z^,·N\x0014Ok\x0012o$Õ\x0014Ü§Í]ÏZyq¸fãûëwÚK\x0006L³Ãå`ñöæáînðå\x0005|.E¹Ú\x0001¬z)/egÈ^AËÁ\x001c$ÒÙÙç\x001e\x0004\x000côã2
A<ßÀ\x001b0òe \x00083@¼î]¿&\x0004\x0018zÁe\x001cü \x000f\x001ecß/H«³Â\x0010½÷à&\x0008èýá2~\x000e ø\x0006à}R±1ï3	l\x0000ðãV]^ÿú¦×ìo~}¿|÷q`s\x0007J?µ\x0018\x0005-\x0005<@­4Ô9}@Ê^$xþê\x001cÜßA³ÛÚ!ß¤eíÞpõðKS\\x0004\x00051=a\x0014ÊH+eÿ´yÍwSp©F>]Ñ|Wøö¨\x001d÷¤\x0004WAs¶´4½îD#Û¿½þ,¯K\x0017ßâÅåðîËåâî\x000e'h
<ÿQg\x0012ñøÈ÷_sKqø\x001b½¹Lg¯ægg8;kXþüþkøt@ã\x0011àl1Øhª\x00018ß:Ä\x0016·É\x0013\x0000YÄÇ¯èÙ¸Ï`çá9\x0006ßßGûå{â|´kÃOÁâ£««a1è±ô1õÐ²_ÖÀy$\x0015ä~¬Ý\x0007#Xõ?'à#Døù%b-\x001eeÈ=ÂnÃ±\x001e\x000c§< L~¬m\x000cÏ§ïòK\x000c\x0001]µ´tx°ÖùËºÙ4>MÈÃ×,¸®§bt#suTôb½óë5\x0007Ö\x00077\x0006!-ê1i±ÇÕ ?=¹\x0019¾P5Ò\x001a´üu¡-=±y|bÃ!ï\x0017
\x0014öó9l¨gßÚª<¦*\x0016×ÏÏ×¨ÐþðíÇ\x0012\x0013,ðq0-wï\x0016WÃÑ\x0018¯TÎ\x0014\x0000+"U3.\x0007-ì=3\x001e\x001dÌ×\x0004bºíÓ\x000cÆ´m\x001f"$\x0002þL)á
c\x000cyÀíMâ¨Þ\x001e0¿yGßÿn\x0014´4"bSq¹g,>é÷åoBð\x0010¼ÝÎ\x0011 ÷àý(\x0002\x0011¸2PD¯ò)\x0018À\x0008Rkë)\x0008\x0016`1'ø"\x0002mX¡5Ã|\x0000\x001aµþ\x0014~{g¿üøi:B/çÅíâÇ WM#	\x0005\x0017\x0014ç":¸ÆìKh\x0017\x001eOåyq:ÿçðr\x0007	ëÐ÷ÓÒ\x0000Ép!IpÞçÙ
¹¾\x001eJB$@£4
AàU\x0015-Ì
\x0008·\¹\x0000\x0019z¼>²\x0012\x0011æ\x000bîGÙD"%0Ï8#r¹º²\x001d¤M\x0010i*\x0019Óª\x0019\x001b97Íê\x0005ÍçváyÞ\x0008v@\x0000êöòëÕÇTü\x000eÑÉÝÝònð¥\x000c ¨e\x000bÒñ-w\x001a\x001fýMðX>ÉÉÙÙáY\x0015\x0018ìP´n\x001a\x0007C<ÀÐ\x000302c\x0011\x0010§\x0016M@3\x0014?#hTä\x0007#g±\x001f\x000c\x0006GÁ\x0012\x001ccã\x0006ÄIñºX<£\x0011Gq\x000b):)¢àÔ\x001f°\x001eka1F}¼Q·iÂh7¶W[ÿázØB	ÑF®\x0014ÅDvª¶P8@$çÒÉÇÛgG/^¡­2$\x0012û¶\x0006Hïê1EöùÀ6V,\x0013ÑÌÄã\x001d\x0008\x0008R
ò\x0004Hï\x001bÈdÓ	}` ZAz´KÃzH_ÅâæÓu¯äï%¨ÑûÅp4\x000c|à'yb'\x000bé®O0={ò%(ÒóùºpØ·?â;ý¶|\x000bÆgèÛáGyLØÁH\x0010½;ÜAçæ¦_Ã{oÑ§'ÇÇÃ\x0018ÞÙ»Åwtq<Æ~ZÐ÷\x0019«a·X«s°àïø\n{\x001d{ÐåYÓ\x0006Â|ù°|Oy\x0001û\x0017¥åÕâíåÐüÍL
\x000c¶Y%G\x0010ìX*Ñ÷Ú¿½?;\x001a\x001ezÐÛ\x0019;õá²vgì3KÙ-\x0018RçXD0!To¾_õÖ(JqY¿µsÜPK¤)Ý_Ç6,ÊmÝ\x001a#Ð¸¬ß\x001a\x001f$ygÇ]p,´ìv®ýè/\x000fß¿ý¸KF\x001aÞ5ÅÍÕ®\x0016Ãáè(ù\x0004_j)\x0005+¦¤tÖÞ÷\x0005ã|öúx~´&ò\x0011Ã×Ï×ËÔ\x0005Óöåê94v|\x0018\x000343¹×QFÃmp )\x001b@8-åç\x00174×ñb]D¨\x0007\x0008; ÈÐ\x0002Èq`6Í2¥¦Ð\x0000ÈäáËòÏÃh[\x0000)¬3R¢\x0001\x0010¨	\x0012IQIG1E!ò$aã6\x0001äQ¢ùÞãl\x0015 §SçÞo\x0008(S\x0008ü¾
\x0000ElzZ@RåÁ-øï»QM!p\x0005¡÷áOO³ãÜõ\x0017û)uM\x001dFp9\x0003%úcMW¼QÜä\x000cbi\x000e·2"ÐÌ.¬ è=¤öüçºô²\x000e\x0000öMÝOË\x0008\x0000'º
\x0018\x001cÆ=Ä´<iCFÙã\x0006\x0000X\x0018Q\x0000
\x0007ç$\x0002`á"G´\x0015\x0015.biClØÞ\ª÷¿¦KMSÝñâûðü\x001e¯iTÑêº6Ê9\x001d\x0006\ ~Æ¬\x0019ÙóýÃ\x000fóý#¦õ¡å¢DY4q»øòeàûÄH2Ä\x0004¾§Qbô|5@ªÅÇ\§ùùéüõëaJtJñuÌê[ÔÂNÌ`àfr\x0012À{\x001cSn \x0005r\x0004Õ'a?^ºò\x0015\x001ctÎ»ü\x000eþ\x0012ÔÏåpú£á\x0011S\x001f²U9\x0019Cì5u\x0002ýsßÁ_*:Zó
þU=,\x0017&	\x0012tÇíO±ðAöÕØ\x001eÌ'kÀX¬^Oü"\x0013Í­\x000cg\x0000¿<¯áde\x0017\x001f/\x001fRR\x0015&yà2¿þ\x00002mP={\x000c®Hs²óë¬àª\x0005¾b¤ù«\x0017 ÊÖèçnÿÔØ(-cû\x0007«ØÍÅ«ï)ËäöØna\x0012\x0000-ã2\x0006\x0000Ø2k\x0019/s%¡½Õ9; NÙ\x001fcji\x0019%ôô>FÙ	\x000eiy\x000cû6»½w\x000fm9,¸.ï¾>,¯\x0007«¥1M\x0007ö¡ËiÌ3àSz6ñéáÙÿ¼8|5ì\x000btûGÌRNËØþByºD\x0001\x0002«)áÏr.¤íM`\x001c\x0005p÷û÷7é\x000eS
Ór¼üp=\x0018XuàkaË\x0008|GQAA\x001f+¸CvÀ^ý
/^­«ªÛkñ>5¹Å`lZÎn\x001e®.o³\x0003<Ø\x0014duya0¨Ö¹wsâBÿuðìäâøèd3¬¾¯/\x000fÃ¸^^/<üÄc#³OÞ\x0011Ï¿4Ü²ÂkÛ+\x001e½\x0002Oxøi§·=f\x0007à2¶=\x0008\x001dÓ\x0013rns!òç«~*×Øö?ü»_¿áö\x000ewNKª/Þ\x000fÒßcÇ\x0010Ræ\x001eýRzÝp.' +Ó{Naõùóu\x0019\x001aúrñFk\x0017]´¼Æ,­÷F®\x0015P<$À¡âÎAêµ.yY\x0017Ï\x00077¸þñí\x0007nB;ßnáãCyk6äiB\x0011ü\x001fÏ¹\x0019 \x0007¹\x000e\x0016tR¯Õ\x0001~ÿ)|þápÆÚoï®|Ùbqï°\x0017P;Ð\x0000Ô¥Ëhðh<ó\x001a³¡ûe°ó3|]s\x0007Ý¥{KÝMñ	\x0016\x001c4è\x001d\x000bçt`\x0012oäwiÉÍ\x001e\ì?\x0004§Ü aÇüêÃ'+ÿÐüNË³Å÷\x001fÃ²\x0007QèeS ØÃ1.P\x0016Ð\x000c¦W\x0008ôlþö+\x0001ò\x001fþ¼9ñÃedóÈÞ£Â\x0007g
0\x001b/¨Kr\x0000\x000b¾×"fdsé?\Þ\x00064eÑæHË³Ëå¢\x00140{8\x001fKè@¤`²JËY¾×½úÙÑ!¾*¶ÆZD\Öo\x0007\x001e,¿g*\x0004 î^\x0013E/\x001eR½9Z¶i\x0019ùn\x0017¨J\x0014\x001f\x0012=Û[6rkêôiÛ7G1-c\x000b¬9¡PËºÆF¥ò\x001bbj#Ý¼9:/¸¬ß\\x0007A;ËÈ!W|\x0000Ê\x0007n{:êwÆ¦;¸ìÃS\x0014\x001fxd\x000bÏ¦è\x0001\x001f¸²9r\x001bå6ì\x001c\x0019øå\x0018¾ÜçÍsÜO;=ÕQ±§elsÏý3Ð"ç>(8B.'\x000fxßÎê\x0018-ÝOË\x0008·aµë6WÌmÖº¼y¬Þüí{õþ*J3F\x000b2\®,²tâ êó\x00048Ý×j9	»bï\1¶·×dRâÞ*xyÞî·FkØ>\x0017\m\x001f¹\x000b6âáÙ"hFçï½ª6lK+F\x0012áS7
®,Í%\x0017T\x0018n4í­tS¶ïÊ(ÆòðÞóðC\x001eâ\x0014t®Â\x0007[BMÙ>×LVJ8n\x0002\x0000Û«<È\x000e\x001cnû^È²zûUÄhYÆi\x0007T\x0017S
}0y²S¿*\x0018Û^Kîkæ±ý\x000c\x001b\x001fVEt2TïîïÝïÔp\x0006uRZ°	üýA_Ê\x0008ncö7{à>k\x0016wJõâ³ØÏd~v>,s®nïnÌâ=ø`q{û¯ÿ\x001c\x001eë\x0003f» ö£¶2\x000e îÓõÜ	0¦O\x000fO×XU\x001d4--ã\x0008¢ÈÙZ!è+\x0015e'u]ê<àÃ¥Z~r	\x0001öüÃå`ñ¯ÿïWàAã#åy?
\x0016Õ\x000bZL\x0013cÚÙ~ªó\x0005Ô§ãû\x0007ìp±ýSa-ùóx\x0005\x0015ÅSD\x0018#b\x0010¶}ÿÿQ¤\x0013X¿¿[:à\x001f)Â1¼½®ÿüëw÷\x001fcòèr\x0017ÙÅìàvñö_ÿg0¤äÓ(
"Ç\x0004Î¬äê·ÒÏ\x000eNçó[\x0001\x001fvÓ
\x0010Îñ\x0018è\ªfE\x00108*AØ¢ä¦\x0005DîZ\x0001\x0002n eªEäD\x0013\x0008ãalQ\x0006;
DI\x0015yÄÕ\x0018
Ýù\x0011Qò}äÃ{¡\x0005Äí\x0007ùåÓooV­/¯/¤\x0001Xö"\x0000\x001c>l\x0012ÚZ¶D""åÝ\x001f¾:Zã_ßÞÞ|í×\x001cyr
Fq`×(vtp®È[ÅiÉ\x0015[cXÉn
÷=Û sË\x0003£¤³yo\x0011Ú÷ÎCÎGöÆ"\x0003ÞÛ+\x001ehfÍ[Ç	_rã\x0004WýZLià	¨Fq\x001brT°7FÒÆ)\x000eê6ÍÆ½%§ò\x0019,D¿\x0003oýÖ)1þÙl\x001e:l+ù³­î\x000e{Êgca£\x001b?lA9û¸·à®\x0001°wÈ{Û®«ßÛcðrto\x0017xRÂ7\x0014r¯â&²xÜvÊwãÒ0º·á\x0000\x00145¤çgÅ©È ÜÄ\x0014&O]óÆ¿Ú{×Kpò\x0010|u'V¢°·O-óÆÜÒÈ5ØÛ9mró\x0019%úý½êwFË^\x000b4ÏoØêuÙLÆnk3áz¡#äÇå\x0019ÈRÏlæ"\x0017\x000f¡,Í,\x001ez¾lýÞ[!ÑÂjïFWÛw$rØ;.ÑÁûIîXgÖ7\x001djwvI UH4¡;\x001e·¹M\x000e|\x0015p³\x001dI´Q\x0006\x0017,\x0006Ü<å\x0008¦ÍÊçí]»ît\x00188HË\	\x001c©Ãf½9$\x001dròí\x000eíòÔ£üOËØæúã\x0007.7ìºãKÛ¼wª,OËú½\x0015vÄ£½Ü\x0018È\x0018Ë9z ëc5¿]_ývsoS6
&E$]¾\-7ÇW\x0008Ú[Û\!i47K\x0006/®¨0z}<\x001fÞûöþ«ûö.Yj\x000b¸í+¾~\x000fmnlÈé\x0019: yLWµv,Ð£}²ÿÏµþjoÿÔ\x000ei|ôèë\x0000\x001aÕsÛ®g4Å~ýS°®bËýOaÿ.
SR\x0015øOSö\x000f¸w¨\x0001àaÖÓ>äqBÊú<z	#zõ\x0000.?ê?LÊiÂ²ø´ü\x0002Îò»á\\x0018ï¼áææ"½@ÓXUÉMè\x0003¦e­(îòÁüù°Ô\x0001ÐØ4<-£\x0000ÃVÉ)\x0001Açb\x0002))*¢Çjýþ\x0011ÿÒ2¶¿s¹\x0019ÈsÎÇû÷FF·ÿtý`®.SÈ\x0012]%\òöa;\x000b|Ïa;ï].\x0015ÐgExÛ· 3áÈÝý×»÷¿¤\t,±L-\x0008ÿëßÿãhø©\x00006ðyð\x001e\x000e¦¦­\x001ak·¹F¼?J$½ÿÖìó2Òxßõ»#ÑCE\x0006t@Ì)\x0000Ü\x0003(~`ýî¿ßIëñþE|K\x000bæá\x000fæ¾àÜ³H¹Ù Þ©\x000f\x001bþ\x001dNãóª\x0017¯Å,üá÷ñë{ó*¡13µ>]Ìþmñîë\x0003Æ\x000bÂ8*ªõ\x0015+=¬ö¥@Ó¢?\x0014c>û·ùA\x0000Ãôÿöû\x001f2Q\x0000
ê´`\x0006ÀéåÛáfÜéÖQ£\x001a\x0004ÁÇÝ .09l?§òlvzôl
)®?}~ÿõ×$\x00041hËËÅ-Üá¾|ªkaq\x001a:OvÎM¨}ñNör~
ü?¼ýoïß\x000c&\x0018\x000bÌm\x000f©"åöÃR&Iyøñ\x0016Ç)¤çîJøñ½\x00048ØûÅ0í?¿ýøãë¢ÌH\ÞQ&â`ú\x0006¾£ü'ý!)\x0001\x0005\8§r*b9\x0002$e ®áÃû\x000föá>ñ!\x0012\x001f«Áâ`c¤ü\x0017Lç\x000e\öî5gø u¯?\x0003¦?Í¹ÿðýòäÁì#\x001cøIÊW¤t|ºùÝkQÄçúnsJ¿9\x001fÜþÛ»øåó2%_¦\x0000Æíoï×ä>\x0017ÍóÏ°EÍ¹O¢kc×ëùúäôü°jsû¸l.=©}Ü<§½8gWë0aslÉËÈæI`sc¸$\x00056Ï\x0003ºÁÓT\x00136G\x000fÍµêÈ\x000eDÈ]
ø\x000eÛÐ»	{£¹§Ãø®ÆÂØUº[.Ã
¾§jë7Ç·Y\Æ>ÜäLS°0s½­óÝ[9asÌÖOËøóËU'{gMWã'\x001c9:7iY»¹1p¿Tüc³\x000fyo3á¢a\x0006DZF>\x001cãÿ¶Ûûg:Ý5«T½t£úÍS |ìÃ+\x001eð\x0014¥ü"
\x001fÞÕôÈÞcXíæ\x0011\x0003Vi\x0019;rÃ3°#V_é|ËCþrS}Ñ¬ú=^~/
¿Ç\x000b¬4åØ#áCo\x0011»ê!Ý{_UéT È^ã\x0008àè%Wx\x0019~\x000ewØû²«ð +íª §/<\x0002³[\x0003\x0017<â\x0011\x00143Ïª!¬¹*àóÝÃ*.N0ÆûÞUqM°*ß\x001aÛÈu[`éQNó>ßïaxc\x0010>èk{SiqVÊ~ZÎ·­¿\x000282\x001c©Ç\ò\x0014 Tó'z!³ÃÓùAÅÖè\x0011¥eýÖP\x001f9ÝÐeÁ\x0017}Ì\x0019ZÙÖ­Ó¤ø´¬Ý\x001aÎ8ç\x0001`w\x001e]"rã\x001aãzr¯rk,ÊØOËÚ­`v¦$\x001cá»dC×ëWZ»3æ]¥e=½á\x0007Þ\x001aÓL¹u³Í¾<Ø\x0016Í[£=¸õô6üÔMrVÓ|.£0èÓµnñâ´ÐÛuG\x00143¸ïºãxÛ¾5¦ê¤e=Á½ÛãÞD^S²\x0005Ø3Reöîå\x0011Wn\x001cñÒ2JnCQHý\x0004Ü&_j+j·þãã§?þ¸J1\x001b4)p9»¿¼ºº¹\x001e$¸\x000fØª&ßxÎhõJwCD/N~vW5Û£õËÈö
ÃãÔÞ\x0006ß*ò$þv¬é¶=q\x0019Ù\x001e{µSÉ.ðó¾Ç\x000bGÛ{ÕkiÙ°=º\x000fI¢m/y´jÚÜ\x0004ÏðÃÝ{Z½awt p\x0019;z,g¤\x0014?ìDE»bå\x000c¿"»³awô p\x0019ÙÝâÉS#M\x001crA¹ó\x001e§«óöýNÕÛ\x001bfbíS\x0002
mÏc©a{íuÞÞNøú\x00031ÚkKSw\x0015ºv8Ó··½üÂíq~¨¸õÊÑS\x0005\x001e}.ó2ÈLü4Y¬}{låÔËØ×s·&,/æÇ¨UÇ÷jÊîXr-Æe¹Ç_%ñ{éB¦}!êë·Ç©b\æ`l*R:9VQr\4\x0017'Ñ\x001e½\x00191.s¶_NC.ó ñòä5\x0019'}=º2b\èX)ÙÃÑ
¹»9¶!$}#â[â®Fä9Å­scø26W.3Bz\x001f1ç#ËÔ®u­³Yæ(ÇF¥\x0012Ú·\x000f¦1Ò+k/ó4\x0000Ðp¹-hê?Ý¼=*è´n¯óØ{¼\x0002lÚ©{%I=ö!\x0005ÆCÈù+iÿõÖÆ_¿¾ù¹OÓòöf]&ÙUrñÓ½¥Ð\x001fØ3?=?<=Yó<ôýÞ}H=\x0005Ñ{OËùòöóp67:Q42zCÏ3ÒQïp\x001fuèe2Âæ/×Dæ¿¿¿Züþ¦h7±¯o3Ó\x0015¨GÀ\x0001(T\x001eùq\x0018$±wE21wr\x0018°\x00195
ÁE\x000bd´Gª±cunu¡ûÃ¸G!|\x0015NÿÀva\x0012\x0003¦i9¿]^\x000e± ·¹>\x001bþ5è|Ã\x0005{Q³o]0W'pzx´\x0001»­1jµ[k¯éêc7\x0015IÉ»
cz9<ö¦~×nÎ\ZÖnmTz õkrmp]Ã|ÝTn"§edëÈÉàs\x0005OêÀÊ_-{¾rëi\x0000iYOp\x0013IÍÁ¿öÙ­²øüÇgíÚ	RóÒ²~küj"8\x000eHÖ¶ÎY¬àW÷\x0012æ«·FïÝµ¶>\x0013ÜeE½t,8qÌfÁº	[cíµñ£\x0004\x0017ÜúAbmªËS5;ÑàH¶o%ÓiY¯\x0005`Ö|Ô±cð¹Ëu;¿\x000eË®±e
ýâ\x0019übß¤¡\x0014×÷³³ÅåõýàÔ@é\x000e<×S[\x001e­ÕïtîåHCÌ2;\x001f½:\x001fn\x0000ÂhpÈK\x000f
þX\x0003GÁ
 ¤}Pq\x0006³B\x0000\x000eVò\x001042 \x0005
R­Ü_ýb_®æ\x0017ÞuSl\x0006s$Oia¨\x0003\x0015l\x0001\x000bÂ\x0007ömX1I\x001eaxÖ±\x0019î\x0014ÐS}pª\x0011ÛËØ\x0002\x00179\x0000¶<ÙÛ^+ÉIØt\x001fnÃ\x0006¤à¿p27vq:on\x0004ÎôÁfÂ±e-H¤dÊeÂÛG\x0006S6³}p¶
\x001cN&lØ,Ù\x00116s\x0012|¯F\x00124×æ\x001aéf©õ\x001bÑMåÛ`ºCí½ O\x0002çûà|\x001b8pVhÎJ\x0014àª\x0016%l·!Ã>¶ÐL8ÕÑÍ¸L·L¶U1	ZìCmÐÀ½6ü>%4\x00175DçSù\x00107ã7)
é+\x001aéfØ\x0001M#M	ëÎ´_Ê7	]©\x001bÚ#@ºH5\x0019q5ØÊG³ün­ÊÁpr]"\x001d\x0005â*Í\x0005§ n®Ð\x000e²Q=®60]VB\x0007Æ^F·©z­úAó@½D»h2í:Òm\x0008®P\x000f²Q?@\x000eQAÜ²ÌúÕÁÆÍ,4lU\x0011¬»À¤¦Þ\x0013}kÉÊÍd°,ôlU\x0010ÛÈÃ©j~\x001f8á#Ûr\x001bj¡ d«PÜ¼!.kV±º­\x001dª*Ä°j\x0015Ã2÷/Fpï±3æ6\x0003WHaÕh¢cã<Â³Øã¾BM
)WZè­RXr;D¹lÍØ\x0012µêW\x0014VRØi\x0014½	\x001døu\x0004gÿ\x0003:á6Ó`ªÂªU
\x000b*È"Ú±îÏýDtz3p\x0014VRØ<Ó$F×ù7{\x0007\x0006ÚOn®\x0010uªQÔEÃ/F!b
\x000büH\x001d\ØLõ«BÒ©FIç"ºgÈmÙñ«+±!Ó\x0015Ö°j3-v\x000e ×&Lê \x0007\x001fláÀè7q.\x0004±n\x0014Ä\x0018#\x000b+¯Iç:-¡6ó¿t!u Æh5å{ÔÛtW9ÓÍõ¯LBWHbÝ(±d=v¤Ë6éH·a GÁ6A\x000c\x001e4?î\x0007Ì¢B¼3¾tý0è$t Ö\x00183MØ³Æ\x0012\x00196ëÌÊÕYNºÄºM\x0012cß`Élg\x0014G1£ïrêÙLÿëÂ\x001cÖæ°ó{EÜÝ	gLèH·!ºBMè65aîÖ9m3éÄÂ®P\x0014ºUQøÎ:Áò0i×y\x0013fCyR(
Ý¦(R5¾²*.E\x001cÓÀ´ÓéXSè	Óª'\x001c\x00176aY)¾+\x0011ét\x0017¨3\x001b¢+\x0014iS\x0014`ãè>"äÏ\x0018r&\x0015nC¶3¢0­ÂåL¤]g²ë.¬¾¡eg
MaÚ4\x0003\x000c¥\x000cT\x001fËæò\x0019O¦\x000c«·)
\x001b}Î\x0014
ø~Ì\x0007+x²T°Á­g»îk\x0008]¡(L¢pèºz"<\x0002,Þ8\x00197³L¡)L¦xzÚ\x0015Â´i
\x0007~,gÝ¦N	\x0004.f_ÌÍ\x000c\x0000Sè	Ó¦'r0z"p_HDg¸M\x0004\x0006T\x0019ÝÎ-\x0014mS\x0014ON;[(
Û¨(B\x000eu`-{\x001dåü11[¨	Û¦&r°j\x0002Ð)uØ-»'\x0007Â·\x0019í
=awLOØòýµMOxa9î	¯ù!1\x001aÎ{\x000bVo\x0018Q´°;¦'l¡'lðÒp\x0013à\x0010DnJ\x0017#:×N©Í4-4Ý1Ma\x000bMaÛ4ÇtW2í|h&Ú¹mkÝÌ>q¦p;¦)\¡)\¦ðÊ³Ñ\x0005ùQ,ºìÉ\x00106\x000b ¸BW¸\x001dÓ\x0015®Ð\x0015®MWxåx$mÀyD4\x0008\x0004h;ã6|Pt®p;¦+\¡+\£®À;Kè°ã|ÌwÖf¾³r3Ì\x0015ÒØ5Jc,&ÛÓÓ¤/Òd¬ÈÌ1WH;×h\x0017ã \x0000²P<&\x001f*¶P2áÜ¯±¾\x0010v~Ç/o7IÇz«¹©CÄ¶\x001aL:¿á}õÅð^öS+'¿cÆ/\x0013Ø\x001al\x001bòÛ÷]RL\x0008¹M\x0015jCÚ\x0015Æo3\pü\x0013â¸è8b{\x000b>Ù¸á\x000b/Äo\x0014'*µ_&ÃÓäw»Ð½QXµa2V(äIh'\x000e³LùVDíéd³°rC³8\x0014ò$4Ê\x0013)r\x001b,l Íw6¨<\x0012\x000b#6CW\x0018O¡ÍxrZÒðrtÇr¶\x0018¬Ì·BËÍÌâP\x0018O¡ÑÑ\x0016!?z\x0006¹º³y"¯Õ~³+\x001b
Û)´ÙN\x000e\x0010	Ú\x0019½± s"\x001b¶Þ\x000c]¡)BãÃ]tM\x000cþÈï;AÄìg\x000b½!ºBUVU!©\x0006Ò\x000efUÑnÃÄP¦\x0013·:²ù1\x001b¸Nw¡l³\x0014ÀßÞìÆÆBÚÅFë	4EÝÁr\x001a >tzl¦x+#ö\x0016¶aU_\x0012í>þ¸ÿâáÇòþÿ>ût9\x0004*`r3)\x0008ç<öpÀjBá²#zS\x0002^\üóð|vöÿ\x001c"ª@ã¶Äu\x000fÁ	Iêo3D
Y@7ÐbÊk\x0002¢-×ôc\x0003\x001f9\x0001)h?n\x000bI'\x0008	Ê§q$Nä¢c\x000b²]1®Kê÷DnâJ(®(2ß#4\
!á\x000eô8W¬#Ý¤dPÁ( \x0003¸Q4\x0012Å1\x0012iró>åä\x0004õ¢ 	þ¸%FñÂHj/Ó\x001d\x0012å\x0019ÊHÌ\x0004>ñ]z\x0018!Áü°í\x0008\x0014ß¥\x000c1\x0012³µÓñ%M|\x0015MÀâfOÏJÕ\x0001,Ëåe§A%\x0014Y\x0003ÅKê2§ø\x001a@éXR7	PJõU÷\x0018û\x0008\x0010ÏjÊ_\x0013\x0014KV¤ê=©5@	%*}T(!õD%¢t"Å	ÂÍÇX Á\x0007ýq¦Åæ]dÂcá!¢\x0018M=¥í\x001cE¡\x0006ñÇq¢`\x0019.ÍëÊ-Õ\x0010Ò¹\x001aK(£¦@Ñ%\x0014]	\x001a]%(©akâ;(SØ\x0012IF\x00168ÀgDÂVé»¨^e|\x0003\x0014WB©Ð>	Ê&Âd$ºC2(¾DRs\x0011	µP\x0006þäò®\x0004¥ã\x0014=SB	¥æ&#\x0014î\x0012PlÌP:N Þ¢%\x0015Q´c$¹cR\x0013¤[úÁ\x001fkøü¦Hdæ»\x001apN"K(5ê\x0007¡p~,	eÛ%(¦2ie)Þdxó\ ÄuH¦p,¥¬nµ\x000f\x0002±Y¤äX¦Pju\x0010¥)TL	s\x001d\x0014Í"¿;\x001c9E÷ÈRÌÊ:1ëQd %\x0011\x001dËö÷\x001a bVÖY5²Òé	¡¬¨2Á8ª³ªNÎvE
`\x0007PS
\x0003|¢ßü¬\x001e+o«º=¦kH£;f(q åë#|ó¶\x000fFî¿­±is\x001f{Ì¤ò'ô\x0008WE=o\x0011Ë¢Ä²øïÇ¢E|Ó/ç|YSy Ãìýrvµ/\x001e\x0006\x001bw)ës×(#}R\x0008AÆà(þUôþÆ¹\x000e³ç3ì\x001d5¿8^ÓZ%£\x0005ªØ
ë\x000f<¡Â©GPYêÛ
¨bÏoÆÕÕ&\J´àÒ4\x0001Ì\x001fBu9\x0008\x000fi\x0019ü&°d\x0001K¶À\x0012dK\x0000® )¿\x001fq©L­^;vXª¥Ú`¥²\x0003<EO¯p\x0008«ë\x0013õ&¸tKï
¹L\x0001Ëì
,[À²;s®ÀåÚîbª.@\+§ËèòeìÍckÅÕ3Ô\x0010W2ÔDªîDjl\Ô~Ó	Âk¥vX|-ê¡á\x0010=\x0016\x0004¥\x00024\x0008Gé¦\x000cò'd®\x0005[\x0011Í\x000bªK\x0012ßw§©&@S\x000eÌÊ°SXJ-Íº½\x0018\x001bË`W#Qººs¬^\x0015c®d~\x001a;u6{~G#\x0000s«7\x0019\x0004¦ùÔ\x0002\x0003eCÃÀ\x0000\x0018\x0016Äqcu$½ïyÕíÀ|	Ì·PLu­f´ÈãLbç:y/§SÌGé[Râ$!n\x001f$]\x001eo\x0011ÄªÁAý[\x0001S­Ø?sÙ¢\x001e\x001b\x0018ì¹y4¹Øù\x00182´·YLkõ¦ßTîÆ7ÿýýÓË\x0007¼§7`¯\x000e ØM\x001bYmS\x0003uU|1özx\x001e\à<=\x0001u\x001cêãQ
xÌ
OÂ&@>\x0003Íx\x000c
®°b)\x001ch?î-no\x0017IpaßÙËÁ¾³Ø\x0013RÐ%\x000cT}gñä\x0012¨hú\x0005xgóÓÓy\x0012\ØöhÍÛ±N/Û¡g@§LHmp/ïfËûÙëÅÕÍ]Bxóð}³"-ª<]Gqñgè\x0010à+Ùp\x0004l\x0006nÇëùñÉYÂzrñ\x0011.\x000boú=Çá|/Ê\x0011ø±½ÿ¯ÿÃëÙß§ËiÆ\x0008¡³3\x0004à\x0016p¨\x0012þ#]T1þópö|vøjö727\x0006k\x0015ç@XÜ\©\x0016Ès°×(Õ~\x0002®ÜQW\x001a©§ã²\x0005.ÛKbß\x0007Í¸àfÒ$BÇÃS\x0010Óq¹\x0002Û\x0011\Ñé>®ÈyãUÀ°#uë\x000cØ»ub|ZL`0!õ\x001b\x001aÞÊÀ°ÍX\x001aã:¿½¿üð°½\^?\x000c`\x0002T\x001eý¢Æé¢\x0008ò'\x000e)ízýlæ§çG/.\x000eg/\x000f_]\x000cæu2 ³rØDjf¥ê\x0000aû\x001fA\x001dVqÆ#2m¸³ÒýÉÚ\x0005\x0011\x0002¹®(áI#Jkðp,\x001añ¨¨Ëø9	Ój>ã\x0007¶RÔùÈ\x0016ugóh\x00044Ï&\x0010¼æ\x0019Ø 
Z1©Ü­WÏÆð}üqÿõ"I÷ãå÷w\x001f\x0017·Ã£9\x001d	I\x0002ODwó¼½Æª¯çI¢\x001f\x001fþãào\x0000o\x001c,QÉzTØKf\x00118\x001c­Eó\x001bC\x001eÙéM/>Û*:×G?¶ 
\x000c*µ\x000c'Py"½BÃjTÀ
oúí@Á/°\x001dèk6 Àóyy3ìù`¾\x000eÝP8aËôd¨°S\x0008¿\x0004Å¾¹ü
\x0008ð|^¬wÊ\x0018VìÃ
°(÷7Á2«ESÙ½¶Ð
\x000bgÕ÷©};w\x0004+¹­\x0003\x0013lÁ¿°ËKH\x001d/\x000f³ç÷³gË«+\x0010]8er(òì£Î\x0013îPõðs}êaÒôxß³T\x000eÁ~>:=;:<>\x0006\x0019S'×ÐNéò\x001a~A¯Ô§·K4VÙ>¾¹þ0d§:g8G)bB\x000cõ\x0015\x0002û¦Ñ%Sº':vV*ÔÇ'¯^¬¡ 3(÷»\x0012 gXå?î\x001f,>Y|¸^²óñ~q3$û\x0003¶ÛWèg<½§+/en.L¯6þ`þòõüÅ«CöAÏOÖ©¥\x000c¯§\x0018àb'\x0010bÒÙ²®\x0010\x0014Tª+| 4Ûý¿ï\x001en\x000fWkJ¨l.z`V»Èµ6¹\x0001¸Ó½©{§\x0017e{xpqzxqt¼.\x0007ØÊ7\x0018t]Õ²À%Sý\x0011³ÅÅýò\x0012oÈÿ¸\x0003\x001e¼üq¹¼ý¿\x0006¨è=õîMT\x0004}*Isi!x< ¾ÍõmÅ\x0010<;¿\x001fâÈûÙ\x0019°ãÑ?\x000eOgð±B£pÌSÉ\x0006\x0008ËÏ×ËÏËëûÙáÃ%û\x0005h´æü5B\x0007;|yôê\x0010ìóÙáÅC8ü\x000bÐmÃ
û;ª\x000fSí,LÝ©w\x0016¦éÃ4;\x000bÓöaÚéú0ÝÎÂô}~ga>Ì°³0c\x001ffÜUývò"µßQ¥\x001aÚY=$\x000b=$wV\x0011ÉB\x0011ÉÕD²\x0010ñrge¼,d¼ÜY!/\x000b!/wVÊËBÊË\x0015ó²\x0010órgå¼*ä¼ÚY9¯
9¯vVÎ«ÒßØY9¯
9¯vVÎ«ÂãP;ër¨BÎ«óªj\x0017å§}#, ]á´ûégØ`,3FÏþÇÝòvñn( \x0012àÇ=A=\x0005Î\x0002¤HÌ\x001eÂ¸þ \x0014¹Á¨f®\x001dÎ\x000fz±\x000edüy¨\,ÊÍR2-l\x0016÷7×\x0003ø&öIqníùüüèäÕºHMüy¼\,ÆËí\x0016JÓGiv\x0015¥í£´»ÒõQº]Eéû(ý®¢\x000c}aWQÆ>Ê¸£({AXÎ¨Û-²)w\x0015f¡}ä®ª\x001fY¨\x001f¹«úG\x0016úGîª\x0002\x0002»ªd¡äÎ© iUieâ¨y²2__-Þe;óåâòö²òé
ìÉdi
\x001d\x001c¦Ã¢¥ó\x0002é\x00058ôÊ×^\x001fÏ\x000f²©ùr~tzôøÃ[ÕÛÒØ_¬^²\x0018éëË»w`\x0010ÿF;\x0003|}tv\x0000¦ð\x001aR2<Ógv\x000eëÃs;\x0007/ôá]·RÜ\x0008oõ\x001a°3ø»!wîrÈârÈ»\x001d²¸\x001drç®,®Ü¹û¡û¡vî~¨RwìÜýPÅýP;w?Tq?ÔÎÝ\x000fUÜ\x000fµs÷C\x0017÷CïÜýÐÅýÐ;w?tq?ôÎÝ\x000f]Ü\x000f½s÷C\x0017÷CïÜý0Åý0;w?Lq?ÌÎÝ\x000fS:\x001f;w?Lq?ÌÎÝ\x000fSÜ\x000f³s÷Ã\x0016÷ÃîÜý°Åý°;w?lq?ìÎÜ\x0005v¢é'\x0013Ïñrÿøæþòî\x001e%¯w³Ã÷Ë«ßð«!\x0001[nQÓ\x0018uî¸(b.`p½
Ûãó£³3z<ÆTíçÇÿë\x0010~5SõqªÝÅ©û8õîâ4}fwqÚ>N»»8]\x001f§Û]¾Óï.ÎØÇ\x0019w\x0016§,åçî
PY\x0008&¹»I\x00167^îîÅU»{dqäî^&U\&µ»I\x0015IíîeRÅeR»{TqÔî^&U\&µ{é­pXW«:Ïü\x0019\x000eOÄ\x001f÷\x0017³~ehJç{¸\x001e*|÷Ø\x0003&õÎBkÃØE\x0012ÐËªñ«Êwð9úÕ¡)ïâÕù\x001a©<TûU\x0007/öñÇýÅÔãäîî_ÿy7T9í]<"Æyi¹ô×ié©?³!®à\x001dÌ_ÏÏNgÃNÑ[z\x0005¨Õ|\x000f\x001cb:\x001fÜÜÑ#ú\x0019¦=\x000eRLjªF\x0012ëº-5d\x00022q1­UnÕÄíàäÎS®ã8(]Ò \x0010[Þ	d·Hµ,6ª¥TLÓëÀ[
*â\x0019ÿ\x0019üñ\x000fnráûÙå¿þÏíàùy\x0019÷\x000cÕÌ\x001aa°Epz¸·<\x000c.FÑwnOráûÙÑáiï\x00083 \x00191åÁ¨^«däÜ*yöjyùaÐÏÖz6;íóø-+¸é¬þÓ4WG/Ö0\x0011!±Îõà5H¼5Ø0µÀ\x0005þ¦f¼Bæ@[\x0014W¢ñ%\x001a¿]4¡D\x0013¶&hâVÑôg\x0000n\x0016ÈÐÈ\x0012¬C\x0003ÂÏÃN3Ü°X8núí£õ?7r®\x0013íÃÁ\x001fkà4Ñà¸\x0012NÝ\x001d:8¾SwÉ\x000eN(áÔÝò§\x0013K8u×üÉà7+TÞ¬§£J8jËpJVö[fe_òß2ïBGàÛcJ8fËpJ¹\x0013êä Ay\wpy\wÐ¢é\x0018&©Ð\x0010K\x0015ët÷b;»2U&+tî|×§ ¢\x0010;øã6Ï*ªBâ5pÂj\x000ccã1E2\x000fÌE\x0007i
\x0018]0\x000eþ¸UÚØâZáU|\x001c\x0003¹UØ¢Nsk¿\x0018­Ì¶×ÆÕ¡)M¯XizaË<\x001e]á±Õ-À5y4\x0000G\x0017\x000f\x0000Gïw\¼nFCØe5Dc\x00041®\x0003\x001cG2cª ø\x0012ß\x001e\x0014«
(Vm\x0011.¡è-B)yÅnWlÉ+v¼\x0012J(aPb	%n\x000f+oÛâ
rå
r[¼AÎPÌ\x0016¡Ø\x0012Ý"R®¸-ÊPÞ °½\x001bdeÁ¶Vnm­4%í±­¶²=¶µÒP¶Ç¶Vú\x0012ÊöÔ¡±²Å\x001b¤
\x001d?n\x000fJyÕ\x0016/³*/³ÚâeV%Ûª-²­
%íYqV\x0017®!þ¸=(å
Ò[¼Aºd[½E¶Õ¥\x000eÒ[ÔAºd[½E¶5%¯-ò)¥­Ù¢´5%¯-òJ\x0019ê±[\x000cõØ2Ôc·\x0018ê±¦¼Af7¨4Ì\x0016M§®n X±E(¥:´[TeXÐV\x00058¾Þeh¢¦X}~yläý(RÂUE\x0005\x0008I©m^~"$¥¨µ5¢ö¶*PúDHJA[\x0015'}"$¥­
>\x0011RÌVEI\x0006+¥¬«²O¤\x0014²®êAêi2¶*püDHJ\x0019[\x00157~"$¥­
\x001b?\x0011RÆVE\x0006/ùÄWñ÷Ôk\x000bD
^Ó»»Uüðneo]\x0003Q|\x0015£<\x0011S|\x0015§<\x0011U|\x0015«<\x0011R\x001fû*}üDPJì«\x0014ò\x0013A)5²¯ÒÈO\x0004¥TÉ¾J%?
PêäP¥\x0008J©CR~"(¥´
[¶¡¶¡FÚFo¦¨FÂj;«B+$boJa\x0003RÚ\x001aiûTPJi\x001bj¤íSA)¥m¨¶O\x0005¥¶¡FÚ>\x0015RÚ\x001aiûTPJi[õÈýDPb)mc´}*(¥´5Òö© Ò6ÖHÛ§RJÛ¸Ei\x001bK¹\x0012·'W(Ø\x0016Ü\x001e\x0014]BÙÞ\x0001¹òeÙmñeÙéBðã\x0015T	qO§Y¼\x0001ÜÉ=A	¶*\x001a\x0002}B­+ßÅ\Õ»Ø\x0013Aq%UÜöÔ¡s±²=\x001dä|yý\x0016/s\x0019IpU'RZü®Êâ*(%U¶hñ»Òâw[´ø]iñ»\x001a_
«ö4I[+,Ö  \x0014í¹%BPÎLpÉ\iñ»\x001a_\x0002\x0001ö$­Ûhö"üjí
SÅ\x00185\x0005J)âê,þ'¶^\x00147\x0008Ü\x0016¯xáJ(U¦Ó\x0013QÅP¶x@e~ ßb~ /ó\x0003ý\x0016ó\x0003½²%íe¬ø2?Ðo1?Ðù~ù^Å\x0012ÊöL'¯\x000bÓ	Ü\x001eò\x0006é-Þ 2UÑW¥*>+ßu}Õ»î\x0013Q¥|Øõ[¬\x0008òeÁßbÁw¥\q[+¥Kæ«\²'Rºd¾Æ%`üí\x0005¾AQc
q2(¥Ù T?êVA)o¯¸AR\x0018¹\x0017		¨\x0002Pà³mäÏµøUPÊ\x001bTõäýT\x0007TJÛ*Gõ© Ò¶êÉû© r¥êù© ¦SÕ;s{\x0013¦*$¥«yf\x000bäö\x0014ße%¨	\x0000^ |òtèc)áb Î±ì?Ýeç÷H/ë\x0018\x001d#Ñb\x0002QB¿\x0019¶XÕ\x001dÊ\x0004ÎPÀùTPl	e{®G,÷Xå¼\x00070Ü\x000cY¶ÊÇ=\x0017øÁ;2r1\x0001.¡Ô¥\x0017=
\x0014[B©Ëéy\x001a(®RÓó4P|	¥.§çi \x0012J]NÏÓ@%º'"\x000bs\x0012Ü\x001e\x0014YB©Ëéy\x001a(¥[\x0014qe­{¬ªu*(¦RAù4PJi[UëþTPJi[UëþDPÊ `ÜbP0!X«þ\x0017SE«ø\x0006Û+w"\x000e~±?î^¾½¹\x0001+\x001c¡<Ø'Û	A\x00019¸w\x0001èB
6Aø°z9=zvr6\x0003H\x0007Ç88yM{lmBjÕ<\x000e~±?î-.¯óTä!H!DjÀ\x001aÔ\x001eûÚ¥FÔ.ÒãPt.®\x001a°Í^å)Èã\	ÈU\x0002Òrz=k\x0019s\x000fjá\x0004Ý\x000b-´ÀÑ+Ó\x0001á$_¢
\x000ep5D\x001fë÷"Ó\x0007óñ>¡ÇDMVâ/\x0001BñW\x0005\x0008\x001c6á\x0013 \x0005ìä\x000c\x0001¹\x0019¶Wv"tq`øc\x0015 ìè·{OL³3\x001b£f\x0012 ¿R\x0008\x0008¬£PÜ[]h\x001fö¤&@ØÊx(ôÞ;Û\x0000é\x0012®ei»§<ó´ÞyebÄÇàIb7\x0007#\x0001Â\x001fëÌ
lÒx\x0008äµ%@ 3\x0014\x0003=W»	PO8" \x0014uGÖñ¶º;²Ü\x0006:\x0006'§Ý²hT	¨¬ÅÆ	{ûó«\x000e\x0010è¹V@>¦ÈÈ
ûøãþñònv¾¸½ÿ×\x0012Y¼]ÞÝ-Þ/\x0007æBXüqÏ¦ðÃ\x0006ÚéE_\x0005iÎ¹\x0010W\x000cÃ Îç§ç¤NæÏ\x000eÏÎæÏ\x000f×ÌÐÑc`k\x0000¿ØÇ\x001f÷_ß.îg/\x0017÷\x000b@òW\x0018\x0000¯Oçç³óó9üy\x0014/áømÂ«yN	Núy\x000bxÄ+c¾Äoo¨ÑeË÷_ÿþ\x001fG×\x001f®°Ó¦fLì_ÜÞ!è¤Ì\x0001?\x0017¤Å>rÏÃßÐÜõSk\x001e\x0005OÏögG¯^\x001c\x001fî_^¿»¹¾~Xvxdë7\x000bÜ|1º»Ýh\x0014G0\x0002¶ãÝ¹µ¦×6ÚÊÝå§_?]ßô>üôa9{ÿ0{}ùÛÍÃÕân\x0000\x0000lCûG-Pæ¤ýá£icHòÁþ§\x0017³ç\x0017³×Gÿvrq<?«Á\x0001wYí\x0002\x000eÐKz\x0017p\x0000'Z\x001cZs¾\x000b \x0001À\x0005 J[f¤m§\x0002\x0001²;\x0001\x0004d¨Û	 pª~'Ä}\x001cÚ·- ËÏ×ñ\x000fÓããåìïWW\x000f\x0003\x0002Lß\x0016\x0008C\x0014Þ>½_)¼!f\x0001v8ûûÑññ¼ß£xx{â±íµÜ%ÙùHó2<X6wÝuíí^ññÄ\x000eÛÚ\x001dl»°½Ý\x0003Çv#Fï$¥\x0007cÏ\x001a%%Mlj=x\x000câ?£_Ã\x0014í\x001fÁüã7ïbpS¾\x001eÍ4rt{ø|ÃÄOJû»üùÑNÛ\x001f\x0014¦Tuû\x001bÇ/ödþ~Îeý´?H4ãrd%-7OÌguÚ_+\x0015ejÒñÄªÙ/(2ùKæ>\x001f&+Ä\x001e|h÷íl2rÀ\x0001¶Ó¶\x0006~U"Oc¤\x000cv÷`Ùà¹´»\x0011ä¬/\x001b¦<H\x000bY#ôT²Séë
ÖÙÒþÙdïDâWì\x000fÿ¬\x0010<¸¿ã\x001fÀ`wyÿþjÒþ°Ç¾ª\x0010<Ê\x000b&¾Â\x001bØ>°§	ÄDæs=\x0006*TÔo×l\x0006¿'Bþv¿]Oûv´Ôk¤\x000e¸+.«\x001cÂû[¯]\x001að2a8ªBê¤\x0010h>ûÆ\x000f}è¤þ$ÖÇ\x0018ªª¹õ°½öÐ·,ôï¤tõqxª¸úÊ`Ô¸O\x0006´\x0002ÜgóÍW½×Æ}À³ªÊÜ	Ù7¯jp%½DäW|=Ø	ªÂÞ`ãÈwÏÓØC°8p\x001a\x0000}þ#´¯øx`XU#vàãMgoð§»NæG(?þé¶¬+d4ÜtïÙÚPZuÚbÊ­\x001f\x001d^uÜ~/ðþQÓPôýyûøÈö\x0015\x000fü¢+Ä\x000eFI,íî-ÍÄ IGý ¦}=üWºÂÖÊÒ\x001cPØ\x001f\x000eùNªÌ÷v¥Í[uÐqÒ	´·{ùÖ5dhâs®9\x0012\x0005
\x001bzJc;%"~gîèÇTNÅçÀÑUæDëX{y$Ó\x001dþ4s\x0007Cñ¦ÆÏx\x001a/\x000b\x0003ï¦Fã>µiMÆ\x0005ò+ÕÙÙ:fòëÎÎöý\x0018\x000b«¸{Ê8\x000eí{ÐS(Iåq|\x0018t^$ö±\x001d®©º}fO+¦¿Ì\x0001AcxbÖã\x0006_Åç¾3Ûóñ±Á«©Rz\x001ageîc\x000bÛÇû&í]]mÍåûëÝ,´\x0012lÊ\x0003ó¿ÜÐÌ«ôå2y$vQWØ:Kû/ÿr¸î¶êÊqç:\x0007ÏüÙ¿$q°\x0003¨ÝVP\x0006lÓZ\x0003Àek)O\x0006\x0001,r¥æ`«ô(¤ðUh[¡=D\x0010k\x0000Ñ5'ÿ\x001c^k@ððÇ\x000f¿Þýùiê»ûËA7M¦'£ËRn\x0010¼]-µï\x0007·¹8;?ª\x0002Q¼Km\x000bDñ(õß
âæÓ×Ïö#
ÿåæv8î\x0011a[º\x0016\x0018ðå_Ì¾7 0}\x0018iæü/'§kø¢\x0007¤w$Û\x0005Ò;í\x0002é=\x0016n\x0017Hïn»@èYdû@ò\x0013Å¶,®nîï®¾¿ÿõïÿqx={¶¼Nù\x0003^tÈz-b7:²R\x0016Hf¯fÏ\x000e_\x001d×\x0000éÝß* Vr\x0018Kæ\x00082\x0000É8´£w}«p(¶íÁÐÙµ]\x0005:Ï¾\x001dHïúV\x0001\x0011\x001cÙ\x0002o_Æ\x000c$G¥\x000e¤w}ë.ÀÈñU¦#\x0003é¼­v ½ë[\x0005Df·Oäç¥\x001eE\x000e¤÷Ä^Ç«Ì#JQzi\x0002Ã/j2¯\x0016b¤\x0002êF=¸"&NFÂõH²DSn%G|\x0017v~2\x0012~þ«E¢90\x0007HÂW¤³ÔU\x0017\x001c©Drÿë÷o·Ë\x0014\x0017\x0006\x0014\x0002\x0014/\x0017·÷ £ÈÎ7ÔÙ(Ùê]Jõ\x001eÂ_ÎOÏê\x0010à\x0003²u5\x0008¢ïÞB±ã9ÉSÛùFë\x0006\x0000æË÷ú¾'Ô\x0017p\x0006,®\x0007]\x0005ÑEh\ÀPeú~\x0013è¬[=\x000bÌüÿ{þj8@³Ú\x001cmZüglw©yh7¨W·\x0017³£\x0012C§^Ýv\x001fÿt8Ð}ügt÷éËiw,``W¹\x0013\x000e~\x0015kØ\x001c\x0013ÖñÑÍ
ö0IG\x001a?=\x0013>¬20ZvÿÈÖ\x0010þIv\x0017ÉIN>òãþ7_ÃÃ¯í@â?/\x0016?.ÿõ\x0003WÚ:ÊÆcw\x001dËÇü`9£\x001eö~1ÿçÑ`n±xó\x0016èÍv\x000býâ\x0019&^Áuý·«Ù\x0001üÕååÕðóÖ\x0003Ö\ð»Âæ\x0019ü\x0015M¶æ0çkv0?;?<:\x001eGbúHL\x0015\x0012ê.(\x000fÍæ\\x000cÕ=\x000fi¯]=\x0014ùÆ|ZFÙ@gàõÃo7¸¿á\x000e¨rÿâînq\x0008^ã¶NFmI÷\x00103TÈ¢\x000c ¡)\x0019çìl~¾\x0006\x0008^_üÛÉñ\x00007\x0014û\x00157¾0\x0018¥£ý5u
\x0000\x0000¤ÓþrÚþd¼ý7ïÿÇâÛ·Oßúf=VqÍ^-î/o®\x0017WË\x0012\x0003@\[ÎAÁì	¼À\x0016&$\x0018MÏ>\x000cä\x0014\x000b¹f¯æçG'¯æ àµ\x0002\x0011\x001bøÕàÿö\x0014C\x0012ÊqàîD¥\x0008¡üÄ
\x0010±¥_Hã\x001b&1«vÚP9)½tZ©£Ôf8µHe	\x0010ÉJæ\x001féõ|nZ»
!±Ñ]\x000fI\x000bzr\x0006HAQ\x0003øÝ\x0013 qf|+¤öÎõg0¯ðn=\%óêÑë%0óÀÓ­,^§ðäézI¿â!Ø\x001do×Åñ U``\x0013«\x0002C\x001a` `¢'\x0008ðçAÊ©\x0018èJÕ`pzÏe1¯·\x0012ì\x001d3\¬1\x0001\x0004Ý¢*Bx*ÀÃ
àð=º;\x0018¦èGADG!Í(!\x0002@àè7\x0002azw¸\x0011D{<N	F\x00006°WÌ\x0010.V~*.\x0003x\x0014WG \x0014ù>\x0000BùA¶\x001dy÷[ü@\x000c8ó
ÿ\x0001+ðàö\x0006KïC¢Â8l\x0000(vjd1i#2GDoW¢\x0002Á\x0003\x0010\x0017ÿ<<??\x001c¶@V8)ñ\x001a\x001c.°'\x0018áZZê¤YKÍ\x0010k)'v\x0002\x000eEHi©\x0002¢-=\x001fE\x001d­¡G{'M\x000c\x0004:Ú\ûñáOH\x0010Ìô \x000f?.A\x000f±\x0006Öå&ye@>°SÑfyåRç¡\x000eÂÅ?@po/1Á.-cû{pK3
"ÇK\x001c¨\x0012É÷Ã9\x0013ê\x0001|þð9Ü>\x0014i¢7o/î\x0005\x001cÌàÁþp\x000f¶6Æô®æÉ³£¡jöÞ¾\x0012\x0015pZÖnl¼ gðÕZQI\x0008\\x0005ÞØr²FÍÆêöÛ\x000f´A¥JÁ!X^..¯®n®î\x0006\x0001Æ\x001ed'c¢¸Þ¨N0¯®áËùÑññÉñgÔ\x0007ìi\x0019\x0005\x0000¾X id1S3²f,òa
\x0000lìQ\x0000°Ö8$\x0000bÈ\x0002@æ]­\x0000Rj¶¯\x0000\x0000ödd¥`â^ÖÏ2k%gÔ¤ý\x0003î\x001f*öÎ\x00054\x0011ÀÊ\x0015\x000b4\x0000°îS¼ý\9ÚjÈ	\x0012Ü×\x001b6\x00077Ä²­ÒÉ®6ze¦Ñ:¾sÎ×X»s²ìBQ\i\x0017)Ó¾3ÇaÖíì"«\x0013Ë+ÌÉ¥û\x000eRO\x001cÄUhÝYbÿÍ´¬ÿè`ómÓ dR\x0004Þ¶Lmß5µ;c»Í´¬ß\x0019XKd34ò5\x0003ã+Â*4sz`IËz\x0016Ãç*v\x0004@ØH¶==u\x0007­Eh>hó	Ó2BnU\x0011.»øS±í­Ú·F¥Ëú­á6)ö=ÅW\x0008ºÕåªp±àkÏ¾×ê\x0017è½¸]\¿>\x000cÚ4ûjÛìÑµëØmõù/Nç¯ÏN/\x0002~=\x001cºCWàðp\x000eÔ¼B[ÌB'cÓ\x0001k°ÊN\x0001bú@L
A0æã;Y)"c\x0016:2¸)@\\x001f«\x0001â\x001dú£3\x0003k=\x0011³Öá©V ¾\x000fÄ×\x001cMn~\x000bGCj:\x001aý\x0000¸!x$ôª£ô(jØ°£1Ù\x000e°a\x0012Ä>XE\x0011Ñ1+k2"
S\x0008Â\x0011à|yE
E´¢rE \x0008\x0006S(.ÈOThô\x0002\x0007
@J)R#F¼Ö\x0019Åè\x0001Ý®ç\x0014hÑI@T\x0001DÕPD¦ªÍD\x00110Ú\x00051kPùhdèÙ
H
&«$\x001aØÊd6Áþ{ì´FÁÂ\x001dä£g²F a
{*î\x0002DMÏ\x0008\x000e\x0014£Ïæ»¤\x0010h²F¢\x0005°9Bk"¨y\x0019[èI×¦\x0010h²J¢	e<\x0008\x0015¯HP¼ùpS\x0014\x0012MÖ´ ¹Þ\x0019î+\x0003$\x001dM¤\x0010i²F¦auM>\x0003\x001bÌ|i´å\x001b¬½Â&ª\x0010jªF¨¥¨9Ó\x0004\x001b4\x001b\x000eQL\x0013ç§yUH5U#Õ,`Kæ\x0013î@­L´Ì4$_U!ÖTX\x000bÚ²º\x001dè\x001c\x000fTALa\x0012UÈ4U#Ó\N\x000bÀ\x0000LÌ&«ÁIÆ9\x0004\x0013¦ )¤ªjà\x0010ÊÈ4ñù\x001dÃEe3MÌ\x00143gåd$¶êâ¤¢ÉD\x00130ÙX¾\x001a\x001dØ*1VNÑ8ª¯ªJ¾¢Æa³\x0004@å79©³¡\x0016õ¤Ó)\x0004¬ª\x0011°VuH¢rÔ\x000exÇ*#ff\x0012M
\x0001«j\x0004,\x001ea±f;aâl\x001di¬³¤\x0010°ªJÀâ3)Ó$ìáhécQSèBÀê\x001a\x0001ë±æV³Xù¥\x0014Ëú"`u!`u5³M0\x001döè\x0012ãÛ\x0005ý\x0014@\x0017òU×ÈW]\x0007Hçxj\x0012H\x0016A\x0016l:5oGRúÁ5"ÖEÁN#±Ã$¿º¸\x001czòFMÑ9º\x0010±ºFÄâ}áW(¯=Ö'È¬ý¤u!bu5VqwTýqL~ÊH|Ô®N!buãÉâÄ[_ôSÙ\x000eÑDO²\x001cu!Øt`sÖpà\x0006ýs¶¥­\x0008ù1D)lb
ibj¤ÓÝûDzÉ¯b9\x00066Á8).±©¹ÄNs./ É¹kD°	kD2TuuTÈAÜ ,ý\x0004Çu\x0011\x0012ï§hbS0¬©bX¥Qé%$\x00139\x0001Ëú\x000fs&\x0000)øÕTñ«7øØ°gø\x00117'{Xå¦\\x001c[ð«­âW\x0010°®0>¦\x001avþò\x0003f®Nh\x0005R°«­aW4\x0008aåg8B\x0000öÊÊOO¹7¶àV[Å­BåÔ\x000ftÑù¡?å73Iü{c\x000bnµ5ÜjQºk~êÏ	wR\x001cj´8Tp\x0002]m
»¢7îÙZ6\x001f\x000e\x0018,\x000c¤ûP\x000fÄ\x0015ìêjØ\x0015hÙÒüæ
H:SÚNÑ}®àWWÅ¯!¿W\x0018,tÊ¢DúaÅ\x0014u\x0005Ãº\x001aµ9I\x0019hâCvþ°M\x001a#ÑróçÊ\x0018}\x0015ÃâQdÈüZ ¹3 ±zW0¬«bX_&lÔ\x0003!|'N¦ ñ\x0005Çú\x001a5èSHB¢T\x000eWè.]ÂùI\x0001G_p¬¯áX\x0013]Á.á¤Y-rpÜËI~¹/ØÕ×°«9çÒ`f\x0017ç/hUv|õ\x0005»ú\x001av5XI\x000bM·(%g0y#¦5_°«¯aWãrçs0é%\x0016b_·|pSÔp(Ø5T±«ãº«\x000eMß(C°©iö\x0004$\x0005»*vu"ÓD¡?(ÖÃø
:I¼y{y÷@ÁßT0®Ç&ùtý^äm6ðI§Ü 'þGÔá±.æ\x0010ìeWCðIÙ~ÒyKôñg< ½«ðø(³)AHJ`\x0006\x001b»wÀIAH\x000b~2âÞnË\x0004æ¹Oó\x000búÌ¿©RH\x0014>0¿m9écg.L²øÍÅOÄYÔ\x0004iMC
÷];\x000eÒv)|*L{ üu¤ªcà¹ç ¾SFª_ÇÚ£SºB£ÔÑâM\x0000¢\x0005&\x001c|\~¾¼Æ^\x0018Ço7·\x0003xR_®\x00089±TÆ	$EO\x001e\x001füíðåÑ+lq<ÿûÉÑé8,Õ¥êaI¬Éåô\x001c¬Cäl¨\x0010s*´5z\x0003Xº\x000fK7PËp×BÊ\x0012Ð¡Ò½\x0018];*ÛGe\x001bPYSFçd\x001e\x000c\x0005&VO´Ãr}X®á\x000cñùóG´¡Î²x9,£úïfX½H<²Vlá­ØáÂà\x0004§~a[ÂÕ\x000fÒ4ãê¹zH.ÑpAïy>FL½É%\x0008qæ2ý\x0018e(x\x001e¬'è\x0012\x000cN\x0016æ\x0004A·Ê\x0013Øþ­º\x0010]Ï0!AÒ¼×\x000f¿-Þ/¯nî°#ÈñâÃí2Í<\x0019ñnOsøÏ¹\x001c¯6:û§Æ¨6Æq5¯/þmþüðøäÚ¼8=<¹\x0018©ú0U;L<SUQ¤Î`å\ãb{Y\x0010ÓQê>J= \x0004rª=Vüô\x0003ÝýÀát¦\x000fÓì*1m\x001f¥@LorRR*ºSl·æB\x0019[Ãt}nWéû(ý\x0004bb-R&fW\x000e¤cW\x0006bù\x000b`>Ì°«Ä}q\x00021M¤>HÌTÑéc÷dRÔ?NÙe6h\x0017;JMYj 	*È` È\x0019¸<Lù\eý\x000b\x0018S\x0016úGîª\x0002\x0002S4\x0010¾9óc^Wl§]®	0Îý\x0015Ô,\x0014 ¬â<\x001dÌ\x0019Q[÷ãKú+¨Yh 9A\x0005aäk¨\x0000\x0014æ:Pä/­\x00059\x000b\x0015$wU\x0007ÉB\x0007É	J(eÒòEW2ç=
ý\x0017à,ÜU-$\x000b-$§¨!lÏæù\x0016ù\x001c
Ñ:×\x0019ïÿ\x0002Ó]\x0015jHíª\x001aR\x001aRS<!¥;¤0B¨i:GÈë¿ÀvWWS$<\x0018\x001f\kÆpÙøøÿ©{·ä8$Q{+X\x0001-Âãnz(H6ð2 )6DH5Ih$=mü;øg\x001d½³\x0013\x001eá\x001e\x0015È*¤g\x0016»Ù6Ã2\x0011-±>ÆÅoá\x0017¾DýâzÎAvÂ*óÝc¬¹úB©es´\x0007-ëÌ1Nç `e\x0012Y\x001fK9A%%3qÁ9ÜvXqÛ½vô¬`K\x0018ë¨9)-OÇøíî£¡\x0014WXJ\x0018\x00119¢@¹ÎÖµpÚn\x001aë8jö¸æxBàêàzm9Å'èíÛ®ã¨Úã
Ýþ\x000f¹ï:Ê=®¹Hÿ\x0018Ðv_¡Þ±\x001eJvK\x0019	ú&ç\x0011ïòÝ\x0013\x0007E\x0016ð\x0007â»íïé.¹Òj¦^ú¦Ý ®\x001dß?N11ßÏ»Ã\x001e×\x001f\x0010â4\x0011jÅ¯yYr\x0005Lê´û¿½Âg"8èá@\x0008Ç³ÔMP±\x0008Ã¬5N6Ioc3=±¹Ö&®ÉP­â·¬¬5Ý68ÛÃY\x0019m">e\x0007vµÄ\x001b+Û¸«®sB8Åõ4>´W·ì\pÚ¹ïª\x0015WÁù\x001eÎËà²HRÐ\x0007¡õNË/ÊÆm=s¡\x000bB¸ö\x0016Q\x001f«Å¶r¶Sz«àb\x000f\x0017EpÎR\x0007ì|Y³)NÊxqIÖ©î}p\x0015\êá\x000c.¶üWoT+ô\x0003Nm4}£¯5p-ÚWe°Ñ9ÕÞ\x001d²HYl\x0011øÌ%·måô¨ d\x001aÂ%Ç\x001d\x001b|TìþYÓêF½Ý&èô µL\x000cçÿ§¼»RÁé)Ç\x0001ü\\x0005ç*ºAÒi¨ÃÜVK\x0019è\x0015XÛÖ^\x0004]Õmt4Ñ2qâ²\x000c±M»\x0002ç\x001dsXLÛØ`X9\x0010®µÜ\x001e0zDiÝQ¬Z¹rjj4)2.?¼{òüÃÍûÏø(üäêý¡×jÏ\x0017\x0016bðS\x001eÒ,Á¥î\x0005áòÙÓïN?;ú\x0012\x001f>=übm§É#Õl\x0012á@¥C\x0010MD©\35êÎ\x0002Z \x001béLOg¤t"\x0000]7Çy$Ö®oV°ÎötVH§
\x0019\x0000\x0010]h\x001dH²-JgtÚç{</Ä\x0003[£\\x0010!qÞ&=©_¿raz)B¹\x0014Ï?~øùú}öwìòîæÓ§ë«}w6è|QI\x0016»l:JÅi¶Ð_>{rö4;;wùêüÅ³ÓC·6L¯E(×B\x0006h[B\x001c>¨Ö½Òîì}Ú
h{@+\x0005ô\x001b
:\x0017ë¬®\x000ch¡ué¹V\x0002Æ\x001e0·ØrÌÚEjðwAêNà:>í#èd>&ÏùMÞ\x001aN;­º6+z+¡\x001f\x0008½p	±< p\x0014Oå¿É7×LÛ­]û	¼$J¸É©¶,\x001f\x0003ç!ßV¼AÈPÊø¼\x001c±ðN×\x00017DêØ\x0007­w¸ë\x0011F
èZ#Ûlrdh=ElÚ*\x0005a¸# ¾#à°Ço\x0001ôíY4èÖ\x001eÀm?Ã\x001d\x0001á\x001dñ1&nt{¸Ñz°¼fó&\x000fr\x00100Â]ø\x0007+;0pM´±]Òuf¸ÆFz±ªÑÑ&\x0003W|\x0006Û\x0000\x001dl\x0015ÕfPÆF¨3 Á\x000cJ\x0018qøN%dmlúÏuv ´RÂE
ìÚ\x0003\x0005O}44\x001fÃ¾»þ\x001aÂ2D´#¬CEeÒÚ{îÚé³r¦Pl=aLßµs-cW}ÀWRÃÁ×ÙWw\x001ciª±\x0015èm+jy(K¨ª\x0019"ÔÎ¾ªÚÙ\x001a6ÿ7kçì\x0016í*O±*o\x001a9ÔÙ)¡ÜR\x0001jÛC|öGH³xÕ5\x001d\x0018|âÒùA0èÁ¦ú¢Si²\lUï1\x001c³\x0001Ìô`ÓøÐA°ì+z%»\x0016ÖS,5{Â~ËÀl\x000f6
Ñ\x001fî­\x001d±8¨¬i«Ðº;ï2/ãr=×4ðr\x000bZÙBÌ\x0017Ìð+µ´'6¿\x000cÌ÷`ÓÈüA0ëøÑ û\x0018¬ÎÀòë¤C\x0007}\x0003XèÁ¦a´C`Ø/5\x0002¯X¡Ò\Ïé n=Ô4\x001aøÜGÙ&\x0014\x001a²Óê¢]ß½t\x0005XêÁ¦øÃ«¥¹ef\x0016¦uµ"'\x0012Ù\x0014·ÜÆ>\x0004ïîà\x000f®\x0017\x0011R*V,±³ºì5:»	lø\x0012o°¥\x000beÜ%î¤#7ÆÎFæ&°AâkÈ7A·ÔÊØºIjÇÕ`ÎÆ-B\x000f"ÿÞÀA²¸Ë\x000cÑ\x001fud\x0007ÛF½E¶êAækÐÇa;ºÁìZ\x001aêÈ\x001d\x001cM»9Hý{/\x0015ÉZ_¥èÙ¥Ö¡¥zm­z\x0010úZ"õ±*\x001aà\x000c§\x001a\x000fC0ÎòIÛÈ\x0006©ïõä¡\x0015#[, eÁd\x001c°Îìy\x0015[F6~-ýf×Ü=ê¦)uh½ì	\x00055\x0001ø
6$ÇaÚsÛuë÷%%,#\x001bÍW0Ã$\x0018zl2´kIonßKØ2°AbHb¾¨'á¹}¢µ°æ½VÅEê«\x000fó÷f©X¾úäöúäOWw{[ø\x0007ÇíàòÿlyrW´©uHÌ-8¹8;ùÓé«\x0005<ÐóÀB\x001ev\x0013\x000cwE\x0010¸ûµ×.\x00042=Y\x0008\x0014ñZ\x0018 THß¤Ra-íìÒ\x001dÃ\x00177j§d#5*\x0008¶ùg°\x0012\x0002¹\x001eÈ-^!C³e¬rüjW_w\x0003Àê\x0015ò=_
\x0000h\x0002OvdCëSê<(*'Oj@ïÌ8¶ðíÝÉã\x000f·e.uÅØû"\x00149åÇ \x0005È/B<ª¢ïþ_'\x0017~÷êäñ³ïNê\x000f\x001fä\x000f¤|j×/3ËN²i ö¢\x0016
ÃKø\x001a@Ó\x0003\x001añ\x0002&Ã\x001e-NX®/¦ó(y\x0005»Du¶\x0007´â\x0015Ìjz¡Q­¨"\x001f\x0002Ýüm\x0005ô= \x0003\x00066uOd\x001dbßz1Ào\x0004=`\x0014\x0003Fwoù,'«Ô=
éÌt¾)\x0001»ç·Wo®Qwß^<¹ºùx³¯áIP8âö\x0016\x000c¶T\x0007²,Tè\x001cËç\x0017§Ïj
ËÉÓóËóOÜäò\x0012²\x0013 åcWÃ\x00168\x0003\x0007Ú´EÒQj\x001bé¹ËØG\x0004i\x001dÌRä±_ªoé³\x0006ÍöhV²¦ä8ßZA(A©¨ü&4×£9Ùn²\x0003£»\x0014\x00105Ü¤"«B»Ì÷d^¶hmÆñf×G{Å®\x0015ù\x001a²Ð\x0005\x0011\x0019hn³c`%å9ÕW9»í¤Å\x001e-Ê\x0016Ír¤\x0000\x001dMÃ'm7\x001bÌmCK=Z\x0012¡iËX\x000eë¢¹6$Îmáê¦\x0001\x001aÂ\x0008E+|Ð(\x0016bµ]@j
Ú jµLÖb¹4Ý\x0001Óf\x0014dC³
=3.\x001ed	5x\x0004\x0001×\x001e¼ÚEåºP±-Nµgtý{ýéäå»ë?_\x001f\x0001j¸[É~fàûÉÁ\x001feºÇ\x001bÒìg/N^þéìòÉÙÁ \x0007å`>ùÀ\x000e'x=±
\x0018uäî\x0019\x001c\x0012,Óc\x0019Éz©ÄAlÀt\x0001Úü	\x0005i:\x000b^\x0004f{0+]/\x001a,m
J¾OÀ Å\x0018¶¹\x001eÌIÀá4ªªO;ËÖ¨M[é{0/Z±\x000cV\x0017,{Ê$/"§¿@êt­à
=WpÄuE½\x0002 éÚ± ëgVÊÁô(+\x0004ÂÂ§¸ú\x0004ûÔñ¸\Ci\x0010\x0010Õ}'EB6\x0008\x000b-\x0016£|\x000b\x0014'EC6 ö}pW
âB\x000bäE9ý4a)ÿý|54¾.o°ÚrÊôp-µà^\x0016É_\x0019FÍ¨«g
Á@¥õ`Ú\x000f×\x0012+ÙLx¤5]\x0000Í\x0019A1µxL?Îm9ÚÕ4XtJÁ¢>R|ýà³no>í×å)R\x000b\x0004ü#r\x0002\x001c#Ô}Gû!X|röÃÅùýº¼á¹\x001eÏIñ4ög$n\x0003
Í\x0000Ý¬Z\x0015ì8ûbÀÐ\x0003\x00061 nÅD8sÛÒ
ÝÌmØót¸\x00180õI¾¥\x001c¾\x000cs0KAÛb³\x00150tYT´ø¯g!Ý4ÊM²¨îNÄw__}|»ï"Ûlp\x001eGPSðÀ/ë8jfðÕÉóK|]yòíéåw\x000fC\x001eÒÈ!\x001d\x0006-EhÊL¶¡8*=ÿ-´=¤]µ²tô¼\x001b½+?÷F%t=¤CZE-ßÊæ\x001e6\x001c\x0008óådBÈÐC\x0015\x001eH±B_»!}R^ÆÑ©;æË½9ÿù«O®+âÕÛ÷W\x0007\x000c\x0006Ç`È®"\x001dG¬\x0004!³Ôw=mÏ<?}ñâ¬ò~wþôôföSÌ\x0017L\x0002ý\x0015MsØ0&J\\x0012¡ØÄf{6+dK\x001ciÒ_ÁV!ã4õóÖ%pW*LS7Ãºùâî\x0016;V|¸Ý+ª³\x0007K%ª9èÉ°I¯µIJyñê\x0002{U<»Ø;½¡Ù\x001eÍÐB\x0019ÉZ´2eWÐ\x001c·cÅahÐ|æ¿\x0006´×y+ÑFízßan(ZÏß^Ý¼ÿôàc7*QüÜfCâs*°Ê]\x000càÛÓó§/Ú3ÈHiDJKBv\x0005Xnà°	;V<AêíR\x0019S×Ü\x000c0\x001dåÎäíÀ
\x001b2©S§ðé\E~LCÉ3}ÖRØ^\x001d\x001fÖ®O_}¸»ý°Wnò Vjëq\x0012yv\x0016ªÝi*Ojg'ÏO½ºxö P×°(\x0003aüg\x0019\x0011&ªñCç&E	v\x000f\x001dÙ¶Hr¾wg	£\x0007\x0014|¾y_Â¨O¯no÷ß¹è9M-\x001bª±Dv£\x001dáUèüi >=½¸8¸qDåG*¿
ë\x001féåEáFò(KV!ê¸
,â\x0006¦®Wü&\x001a4¶p!vFÍ,½´Äd\x001býO±ùåmøý'î\x0005RÞ.þóCÞ¦Ó¬Q>]½¿º-;öíÍO\x001f>~D¿eýæÇ«7·ï®?\x0015*4
0HI\x000c`k¡)¹LÇ]\x0012Ñ~<½<¿øÓÙoþóYÞ2Ô-/Nó®Ýûöügûü§\x0012\x0013Ñð×:J|\x0005*ù\x0010Q}\x001e\x000eR\x0005Ó«Zr\x000cP³¿©ëP±S\eM&a9HaÅîã|æã°âð¥ú¹róSyaÆÍwÙÂ®¨Á8Ú}[æ£lA7¿üþßÅÐ\x0017öE)\x001f\x00177×w'ßÝ|Î÷åîõõû7E¢ì!\x000cÁ	è0\x0017Ã/òÖ×\x0003j¢ÕÃÎ_½:ùîüe¾>¯¾={úxo¾EÕBåCYn±¢ÕìÜf³Úªh\x0011gÊmBÓE¶ÔO\x0019­ÓÐ
ç¥W{\x0011L2[y8]ÃöË;{÷é¿É·xt*âëß\x0003\x0005Þ
e<7 5\x0016+¼\x0011Êf¿e¸\x0019gðéù\x0012¦¼FÈ¥>å\x0005HêBMÌY° ¥ÃXW\x001fß\ÿ²	§râ/\x0011TÞ5\x001cnke¸±Q%ªc@6­\x0015Örà/\x0011W¬¹¦+Õn\x0002Ø\x0019\x0008+¨\x0007Öêa,\x001cã¿DXÙ«Ä\x0002$Ä
\xõ+VPjåjýþú½s7Ýi¿¼þtrýxm¡ÒñùõÇ÷WwÜÜ\x001e¸IÙòÂ÷ÑãU,÷Ñö¡å>ú4HÚË³\x0017'ØñÇól\x001cæÏÏ.¾úÏó%¨YkÃZTìh¡	\x0015\x0007)VR\x000b@¤¡Ô\x001d´^×¤1øU\x0011ÀÀI´ÎèÈB.Ä#¢æ\x0013d×ï¢kã\x001dþ£§ý\x000f$óhe»[
l\x0002ï²­U\x0007$Ãþ¶\x0015\x0015J6ù±Póaò«QMi4PP³ÕåèV\x0002¿HÿÖa5©|ÿ±,1^9Ã¤\x0000GDÍÇ>®FEC÷_QcsìáÅ¨Ú\x001eó¨æ\x001dJ«Q}v£,Ý*.pÃQPëSÀPÙÍZ¿¬ÑTa=\x001c/kdV}Äkï4z½¶ÊÞV¢Ó3Rëº:,Jàu=âiÅì\x0006½Z]ýY³²Ò«\x0015VÂVçTkÀ\x0010NÕ\x0002Ê°Â2GTX§7h¬/ÏzóÓ­ýp×\x0019WØ¤ñïÿ[º4îáÊ4»×ºXzX9S\x001f^Ltç\x001dX7ì7÷gµÑ;j,\x0001\x0008ÅG(\x0000>=ªNL*Å{õûYóýUe?üý\x0011³`«k×"=ªUí¦VÀ`|\x0001ìhõ,\x0005¨x\x0001\x0000¦"É°±\x0015S\x0001Yrï\x0001<x
<:Iåc	Eö>®\x0014 it\x0011ÆÑ5Q`ó\x0019\x0016NÛG\x0011òðMùX´\x0019%q.ïÎ÷¥¦ç¬)<í\x001bÝ¡ >¿5×êçþB|øýc~¾~ÿ\x0019Sk¿ýp÷ñíõçÏ\x0007b:\x0001[}²0\x001e[}ÐÅU ªQd!ÆÁË¾xö\x0012;É<9{ú\x0012Ól¿}öêò»³/÷t:Èêg¬t\x0016S\x000b¤uÜp+¥\x0006&x\x0003$Ýì\x0015¶æ\x0016ÈØZsF HSþìã@Vçb
¤Øç¿@â@Nz#·äùâ Óc13b\x0019WUÑøêãWb\x0019\x0006ëF¶0ÚðÓû×\x001fºuüöê6ã\x001d\x0010â	;mi
(':Y·9º¸
`¸$ß^d\x0001\x0002ÖG\x0007\x0011bGåpÅ2Ö¼\x0010Ø|\x0019\x000cË¯Y}#¦Û·ïÞq·×ïßÔ²6\x001a\x001f÷ë«\x0011aEÁÖ\x0002uÛÄÉ\x0003t)ý4FqþÝÙÓÇµÀ­Í8ùáôP<xÇÙ\x0014«8µf\x001a{[xb
dN[¨ý@\x0006Ûâ\x0014ë`Ý#G°Nq\x0005»MÚ:êÊ¶HÅ*Xì«_\x0005JÌ\x0002`\x0003\x001eÇ
«§vß&Ö\x0016ªXÅêJ\x0019\x001a¢\x001aàôÄ]*j	½\x001eµùª+XC\x0015\x0018
ª\x001eòò\x0014:0¾\x000bm>±¹Â3{µ7éòÈ\x001bv¼N\x0005¾aÇ\x0015\x0007\x001ayõ\x0006ÞÄúúÿ~\x001bß¿íÄ×?Ü½¹½:d§ºPj±ò\x001dG\x0015ÈNU$¨B¾Yøçg¯\x001e_.\x0001¨·ü\x0008P="@
sýó\x00008"ôO#\x0008Ø\x001d²|<ywP\x0010°/T}|Ë\x0008¾^çlG¯°ÏÞè\x0010\x0000\x0011]X%
`)\x001d\x0007Aó*TÏ5`ç\x0014\x0001Búüûß~ý[gòp\x0011â§ï®ùðñs)«Ø\x0007íxz<\x0008\x0006\x001f\x0000«\x0001\x0011\x0013½ÞZïG\x0003K\x0011QL<vùrouE\x0016j¿ßºw¶\x0003+oóçïßÞå¿ÆÍõííu\x0006¼ý|uòâîí¡@CíÀV\x001fç=\x0006\x000fÑ¹Ì>'¿Î;5ìXy?úÝ«\x0017//ÏÏ.ÊûüÅËÓ\x0017¯ö¥é\x000e¨õ2ý+ bÚ\x001d¨\x0011Ö¼ýð/r\x0004ð	\x0002ýK°öÙD_;k6pÁý°f=¿þ\x0015X±E¹ù\x0017\x0003h{¯Z\x000e\_ÿöW\x001b;­õøÝõÏ7ïKÏ¸»?\x000eÆ2"g`ÿ\x0008ÔìØw¦\x001a\x0017Ñ\x001bÖì´Ç:{rþ´\x0018Ü¯þóP`åÝOöÍÏfx!8¹¼ùõ\x001fö_k¥(ª\x00026U­îµàøÉåùg{mîû)Öùð÷\x001bC¡Ííx\x001c!p\Úhæ\x0008\x0016¬\x0000?Qüó\x0008(JùO$àg\x001e\x0001¿<Hàë,V$püQk\x0014½£»ü_ÀÊ£èJÍd^2#ö\x001f½\x0016¿ýñîêú5&'â¬\x0017èß^ýt0X\x0013tiÂ-n­5ç$\x0006²þ­uÓ\x0007ì_þ°\x001f$¼ýùZ»Îx}0á5)ô¾b}<Ã\x000e\x000c$HÒ;\x0011TÞ:ûx¶û~î\x000f\x0003hÑEH.XêÕôzçcûþÀfE¿\x0016¬\x0001\x0004ÊwÄa5\x000f\x001dÛÕG
<{ãW,AÈß\x001d|Ä@
ÔÈwÂ
0\x0002 ¬-¯]X³\x0005ø^\x0014\x0001¼\x000f\x0014Å	§4êÏ\x0004\x001f</s+\x0000pö9þZ\x0000`c©K26Î	"k^+-ÿþò\P>\x0016\x0000]§j·SSSüLô\x001eÌ\x0018^\x0008aò±ä\x0008*zCÎóO\x0013KD$\x0008Á\x0015\x0004X\x0003W>ì£hatFÑ+iÞ\x0003\x0006°cÖÈR\x0000L¹À%§Pa'ò\x0002o\x0001I¢@ob>K5+Pê\x0001â²k¨C{\x0002ËúÉ\x0013%Ò«U[³¦ÊÇ\x0002\x0000G¯¥¦ÃÔS\x0018çïW+n! tùX¢\x000bjI\x001e\x001aÕX\x0004Ót\x0001\x001bÕFÏ
¢}
ºAàãë7fÑMÈÇ >ÒP\x0015RÌÿH»à-´l\x0015w\x0011§ÓS>\x0016,Õi²\x0010ç||<H\x001e\x0015òØ¡­X>\x0010@)ûË\x0004 \x00125Æ3xB+\x0001Nð\x0013à¬oÊÇ2\x0002_	²"¥ôl¬Èâ\x001a5/\x000e\x001e:
ºJåeb9¦,
¡*æ4Fç\x001bÁ)E={\x0016\x0016PØB±L0ùÒÓºÜKh\x0007\x0011«\x0005ê½Ôfv7\x001e¦\x0008Å\\x000cKäs¶Î¸\x0005k\x000e¨¶QL<^\x0001EY°PH§ú¾m@ù¥¦ôÜ¯Â¼ZÀPªzðs¹¨ö-òä·,!¨<%k0+¨\x001f¦À»Q?hì2ú°P(C	ìYcÓ«°Kµ)¯\x0002°Ä´~.9\x0015¡¦[EM\x0018R\x0019Ñ%6]\x0001D\x0017ä³ÿ5¾ù	¥\x0015\x000eÂ(\x001f\x0017×'Ï?\x001cu`û\x0016_ mS±p+×L¼©³çÏ\x000e$nt\x000c	\x0019Ò"\x0006Åo³ÁV½\x000f³¦\x0011â$-i1\x0001º0åãA\x0010±M¨!À
	â×Ö\x0010!®\x0008\x0001ßðãaT§\x0014\x0008\x001ciO+\x0001dBàV9}ÞTúüîõm\x000fµñá{=»,±jÞDØº4C(1t,¦íb`\x000f$HvX5\x0004$ÁÂö3òe«9=\x0006{W\x0013\x0019åèr*¸ýõö_gê\x0000\Ýþ|õñóï\x0007 Ðõ­¦WØ]dëÊ´uÜ8ì[ÒSq½ÖÓ'§/ÿc	T×}
Pïß'ó_¾[©'ÿßÛ7\x000evv\x000bëíÊ¦y¢FàñìÁE|rvqþøáïh\x0008²Lõì8ìð\å½qÎMHv`ßí¾þõ]¸.¥¶XP>.®?aîà§¿Ý]>ðN\x001bÀ«úH\x001bSËj©lÎN 1ÿüÛg¯^üÛ«³ûgíõû¯ûçÙ|îò7^}¾ùûÿ\x001eXümem6\x00121±>â\x001b\x001dÈmÇæëÓdßWùN_îíZÛ±d¿\x000bÑÍb\x001a¾ôÑÅÄI
\x0016 ;\x0015e=Í¾mêh,ÒØÅ4F¹Ò§°d\x0017\x0000ù
'\x0014¬ÒQJóÁ}ú¬S	¯åÿ\x0016bÙÂwÉ°P¶È\x0007CµF{\x000e1æÿlXS,Pøno÷¿}þð?wCh£Ú«»ß\x000e0`æ¤«zÀ{Ç9áy1éÌ&\x000c4M\x000fíé«_Q*:ì"¼\x0015\x0014e\x000bXo¤©RSÓmÔ*®ÂÈ~D±^ñsÉrà4²%ÁYOI\x001f&Ûüh\x0010qüô7{õ?¿\x0016K\x0001smñãñÕÏ¿\÷0GgÚðv|â¡8îÊãÓ'ÏÏ^¼ìÇý\x001c\x001e9ü2|\x0010¸zÂàäj&8\x000bT¿âÒX\x0007&\x0000h5E\x000bâ,ùýÙl\x000eøT >Òu6Æôr\x0010­MiK$¤Gºz86\x001bQuàqX`TH<Þ÷Ã$ñÏÙr,ùØ\x0018\x0016ÆÇW\x001f_xÈ~\x0003Ó
"7?´ØV¶\x001aJ°ôãÓËo=]B -!0\x0016_E*¡¶mVALàÃ*\x0004\x001c&T>\x001eFG°K<Ê±\x0010é¶:7é\x0008ò\x0000\x0002¨ßÒÏïÐl¶ê\x001fguRG"ïµ>t[	\x001cI>/Dv±&ªíìäqV%8\x000cy\x0001\x0008h\x0018übê+\x0010\x0019Äí\x000e°s°äíÿ\x000e¯_c\x000e5bù¸èûîÍWC/\x001aBàIOOìM!Æ"
îlº\x000fÄ½Ö\x001f? z-#vËÇ÷7·YÑ\x001frÀcJô¸ï§ÜÙ±¡H¶ÇÌpK¾?¿\x0018uü\x001e\x0008­JX¦|>L3G\
Y¢8¥å\x0018UoD\x000ba\x0015Æiý\@a\x0014ªÕBont\x0002[U
c¬âö¿~zû©ÜW|KÃ|F¿ÿðñP$ÀFÅ\x000fØ ºÀ\x001bm\x000bUcO|B¿v «Ô\x000e\x0002·¢|<\x000c\x0001Ùä«\x0002<åÿãÔë:¤£\x0004p'\x001dT\x0016C.5åcÁJXE¢+y§Yhn\áÃÔ<_
Ð*/\x001f\x000b ²mQöÇÁ¾U^èÒá¿@èÖ@h}oêçÃ\x00148ÆQ%zTðd\x0006Ú$èûiXä ÄÛß~ÿP:Î\x0006lËR>¾ÿp÷ñóA\x0017\x0016[ÀiÊ9h\x0013-Ö¦V]\x0016G3çûg¯._ö\x001eä~\x0006LyÆ\x0007\x0019<¶²ÐUfæßðÄ\x001d£©ÊËéòRµ
\x00025*~,X`HXtõa\x001dès\x0004F´\x0012w·ÿõÛçO¥
]y[Ð}qÐÄÒ^qS,=ë?DÇýq Ù³XË \x00160\x0014	ÿL\x0006
iÊÇÃ\x000c8[ÎÕ
·`5Ê\x000cÄeö\x0010ÍZ\x0010aÑBh~ÿ÷¡FçÊJpk'm&\x0005ºK\x0019,^©òñ0ÁÎîT%\x000cU3' oM!0'ñòñ0\x0004\x0000PÉc5¤\x0006a\x0018.ÙñZ´\x001bï~ûÕú÷x?K³\x0016UVâÓÉã\x000fw?_½¿yÿá@©ÔÒ«jþ;ãq¢q	&J×²Ù]°¼8yüìÕÓ§çO½ØôáS\x0008¿¿-Ï\x0001#	éùíÕûÏx²H\x00018PÆ7ÿÝ)\x000eï¤1K\x0007q_>}¹EkUü3ü\\x0006pqL5upÜ9åk\x0000U\x0019{l'¥qÞ}¾Á\x000e¶\x0001Ýò0Ëv0\x001eÅ\x001aOÈv8p#ý\x0010©æ\x000f\x0013\x0018â\x0014\x0005ÓÙ\x0016 ÉS|A|J­ùUç¾[ã¹AÆäÍøa\x0010ÿîîã/ \x0008&0\x000fïúåãáÐseb+äÉ¡Pn2?\x000f¦:J¶+®~úÃó\x0003w¨@×\x0019?\x0016@(ïkÎ,LZeOä6z¯cë Ð{Æ\x0005\x0010·Ú\x0019#hÉ\x0003ÉSk\x000e\x000cm¤5\x0014YÇkm\x0016a\x0011ºdG×¡5UZe\x0017Á\x0004ãó\x001f·¿ùë"Z1|\x001f\x000b^3l;\x0016ÙNñØ\x0017½,×I¶¦0\x001aí\x0015ãa\x000c¼!åc	r\x00144\x000fN;ªÓ¶&PçV\x001bíø¾\x0018#ûºxz\x0011Ãr/G;ïe½r\x001c\x001d\\x001eÄøÛß~úåª4NÁýÀ_Ï\x0011âí!±tK©1Hk#\x001d\x000c\x001d0)Î\x0015ÇÖ1Ï\x0011â»ý\x0007ã\x000fó~S|5üþòñ\x001cßu>}:Ø³ÄEE
¾\x0012&^QDÖh
üyÌÊ\x001c0Î.Î_¼x¶?¤Ñ80Såò±\x0003ÃÁÄ¡\x0012Å\x000cxv]c\x0012Q\ÁÝõ¿ôfô9
Ép_.ãÙêmµy\x0018¬\x0006w5z\x0018¤õ]Öw\x0011øí\x0002O¨¢K\x0019l\x001a3,ô]d\x0017-IÞ\x0018WI,¶X¤Æ¶®-I\x001aQ\x001e&\x001fÕíwÅqB]OKòñêçCÁÈl\x0012DNSÅ®O<ÊÕsf¶aããòôÉpäÛ77¯þkÁÀ$\x0003üx~ýûw×\x001f¯\x000f¥\x0019x\x0013°ËQáðÔó\x0014C\x001d-^\x0014ÿñøOgg\x0007üé\x001d\x0006Þ[üXÁFXÄ,rjyY{Ä¢]
O)Þ-\x0004qÀ	ÔyE(È\x0001À\x001cV¯]\x0010­L/@tKUË\x000e5;RØ°\x001fuLd³\x001fêw?(íTîjeñãw×¿~¼¾»¹=d£¬ö«®	ÖQì\x0003L4\x0015KMz=¾ªuÅ\x0019íÇË³Wç\x0017û®\x001b\x001eôxðÕá\x001eÏ\x0008ñ"ZÕ\x0013Ë6\x0003\x000e)\x0012ÙÚÆ\x00177\x0003Ú\x001eÐJ\x00011æ\ù<Ð\x0003°L\x001a}¸Ïõ|î«Û_ßãù¯\x000e/ôxá«Ã=^\x0014ã%Ný\x000b6ð;\x0010fÆ2ß·/\x0007Ä\x0006ÏýúEé\x0006G
-Ê8ê mµeÏ\x0003&Xî\x0013îK	ùéoI\x001b=T»\\¼¼¾»Í\x0000\x001f\x000eØhQQ\x0010\x0016Û\x0017ÖÚ3£ø*Ó¨ÁÉË³W\x0017ù·û\x0006¹\x000c0¥),QebÑ8`,=w?ìµ\x001c\x00063r¿		@\x0003úÏÔOÓ¢UBïàVÃD´mÊÇBì!\x0019nÅ¯éI-ûGÀíåa\x001ag\x0012À`úoÊÇÒm\x0002r×\x0002`\x000b~KÛD,.Ä
,ùº~S>\x0016²@àè$h/~ea\x0000øÈ¸°úÈhmJxÃ¥4\x0001Ó¬*L>=Õì2
@ëõ½Ø±\x0000&\x0015_%-^\x001aWË\x0004\x0002U=¢¶ê6_ðiië$úo!þþ®<\x0006üx[3²_~¬yp\x0007"Ùc-\x0003Qîesæ)fsBÈIOÓ\x0015O^^Ö4¸\x00054®ÄlZLãK\x0014»D^âîøÈ0Í]xÆÙw?Å7EÊ \x0003Å"/³\<ôV\x001e±\x0003d")£Iè]»\x000fYw/|ò2³]\x001ezµ'\x0018­U92Ê-¥É\x0018e(V"{M-ÎåÞ±ÖéIN¦ô].ËhBöbª\x001bp$¥¦9C\x0005¹Y\x001dÜ\x0013À\x000fÁü\x0014óï~A\x00012åãÇ«:\x001b3c¼1ëJC³\x0014Ø¨£\x0012øñôb\x0018{÷å\x001e+°ðãðGå4ýd<÷ñ\x000fØ\x0019¼¾Ó¦1÷já×c ª|<ôõøõÞ¦:¦·D¯#§ä\x0001¸\x0015{ì$õMùxhé\x0003ð\x0010¦ì²¶*\x0006EÙ,ÎLrg\x0017}½.5ñõóÁÕ7l\x0001¤ÈÃµòê\x0003\x0008Ø1dá÷ã;dý|èïo9{$$×\x001a\x0016;Ï3È@¯ß_rvËçC¥¹\x001c[¡gÇ\x0003#?Ð'#?}YÌïO\x000f¿n¸%\x0006èêß?DÊ\x0019qÚjcÙ÷k(Ú\x000b\x0016Ü>\x0000l]o¦ö\x0010Øö5òí3¿þÝÿøÿþ\x001fèsë¯O~¼ùéý×·"ã.[\x0015!:È\x0008ÍF9»ü\x0018èª\x001fÏxúìÛ\x0003\x0002ù¯ooÞ^÷(cãâfdQLÅ*jAHY\x0012pû\x000e;Iã\x001e\x0016\x000e\x001aµ@µ|Þíý`'ÈUxX«[k3-\x0004ÏPfl\x001f!íý\x0010KT¾E#sÐ\x001aÅýàÍD|¡f{c?Ø\x0005ÈÁ\ä\x001b¥\x0008\x0002×º{å\x0011R¨ÙfØ\x000f)n(\x001e±ÌX×\x0002®OpFOÚÅK¡¨7\x000cÊzz\x0000Ø\x0019$Ö_©eÔÄ\x0018BÕ¹9B(o\x001fJÔ±65Ï'*±FH´ÛEHïü»?Ê<íiÁÚ¯¯Þ¿¿>ùöê÷CB*b\x00020[µ±É¢\x0003\x00080?øìÏg§O|{ú\x001f\x0017\x000f0õjK\äa\x0014Ú\x0005ÎôK\x0014\x000c²NÍ¬-§\x001aÇé-¥ò-åMãå£¤TÅ\x000e¢M£ë,Çª"A\x0015¡\x001eG,ë8Ô¡9%céXU(±"Ï\x001fÔ\x0018¢QhÓüìºåTU*©,1
Ð@>\x0006.ðu\x001a6\x001e­*\x0017ÄX©»Th	¶ï¡^s\x000f³ªÆwü\x0003\x0011§¿^¿/±Ï\x001fîþëPw[Ü»ú~\x001bT¤±(Ñp¡<\x000bþxö´D>O^>{õçýÍ~\x001b\x001aôh AË\x00022/ó	³ür\x0018\x0002×Ù8ºb4Ó£\x0019Ñª)@Ñz^@à5ã0\x001f1íÁ¬\x000cÌ6°¬\x0016À"G±'\x0015¸b2×9ÙAS4ñ#¨äÈ2\x0008Ãjíè/Ñ|æEh\x001a¨ç]ÐºLN¯»ÙZ¼õøb²Ð\x0005Ù¢¹Z.·3pâo4\iÛ¶h±G²EKívæC\x0017©\x0013µâ\x000bYÔn;j©GK"4\x000c
ÔE\x000b;öEp\x000fÝ´Z
ÒVÐ°XöSñõ­¬´$ºmA\x001b\x0015L\x0013ø¶jÙ<#\x0016\x001d­V¤­\x001e\x0014\x0016i\x0002m5w=W2ðM3ËôÆ5\x001bÔé\x0001ÏùyÑ iOÏ³ìdÂ»mÐ\x0004Z¦
°_\x001f´
õ´¡&µ
ÝD6h\x0002-S\x0005ÑaË°B\x0006\x0006£H,ò\x0005Í&Ç¶\x000b:¨\x0002-Ó\x0005»°"Æwià@ä\x0001GÖª±ÔBÌ6(\x0003-Ô\x0006_ÖVÓ6Ð2u%!$Ù0\x0001\x000b3ÌÄw¢Á sA&s\x0003´e\x0003Íóv¢<È+M[
£+lÙ¹«ó\x0000CÖ+MWEÍÃÚ&m\x0017Äl\x0000\x0001\x0000­\x0019ÍÞò5åusiÛ\x000e×\x0014d×4)
ùù¯´§è
\x0013\x001blÒV0\\x0005]\x0014¸Ä\x0002Æ&4©\x001aUÛB,Ç«?ÜÖÖõ	+\x001eiZv´Ô=Ñ¸Í®Ôæ\x001e¢"&=\x001e°\x0011uâá3ûbUØæýÝ[Eñ"\x001anö=\x001a`·¡ULdFm2L@M	3t='`à{I`Sx'ù¶)\x000c¸·Í %D\x0003 í2½"âÛ\x0005ï²Û\x0016~¸w\x0010Åç\x0004TW\x001f,=2a´[	?_\x001c	ñ\x0007sØDmø%\x001e
ö_7^\x0014;]B+]Båø¥\x001aH©Ð>DnQ6\x0019É6\x0005må#cèKaKÁ¾;ùáúýõÇ«[$üáêîöP®\x000ce&]Ú(\x0012<pÁjv_üpöôìòô\x0002q8}uq±¿kVC\x001e\x0019V#gÝR_@ò¶{JN\x0001oXÛ\x0010f­èUÈ¦G6ëW9p>
ºtäÊáYåU\x0015«mOl×/rØVyí-'=ÚICMÈ®GvëÓRÐa FÆ°K\x001aÍñ}OìW\x0013g\x000bÎp4Õ²§ê[¼&Î;Ñ«CO\x001c6¬1½\x0013Á#J|áf\x0019ø\x001e3k;Íá\x001e\x0016m±gëW7²¡mà®m<®óêaÕê¦8­'VÜü\x0013\x0018VØ&ÃÑ\x000eÄ.WôZÉ\x001c\x0015¦Ýò\x0019n³¼mÓÑ\x0014\x001euÞz¥¸b®\x001ed\x0012nn÷à©·ÎÒÓkµ^ÌP{àÀ´
 Ü\x0014ur³ÆÄ*æAëéµj/bWp»{XN¼ÎEr)­b\x001e^«E2³Ù
nä9<¯óñ\x00075¢×ê:\x0003ìÌÀÝ\x0012\x0001ãxüø«w6\x0006á¬×Jç¨²'\x001eèl`3¥1jÏ\x0019\x001aúx6\x001eÄ³^+ó\x001dlqHí\x001dÇo}à\x001cm§gbÀ a½|Æ¾´Ì»£\x0001\x001cgs0ÿº±
y\x0010Ï°V<çeæ\x0002Þï\x000cl-sÚ\^æÅvÆÈ£K²^:{Û\x000c|¬¡Ñæ5·x¼e\x001e¤3¬ÎÙg\x000eäG\x0005Ûì#¢)#G\x001a0x%°Ö-ø®Iíi1\x0012Êù\x0007\x0003;\x000eæ\x0003;«\x0007\x0002ë5
>âÑ
Ô7KÂy'è'4\x0006\x0002ë\x0015JH-Ç)q×\x001eÀ ¼Ìó\x0001«\x0007Ï\x0004Öº&µo\x001d-³£PY@C£ém\x0018t ¬×Y"\x0003ÙtRM§¹õXsf¹>9èQÁ \x0000a½\x0002t;\x00153»\x0008X§Vé¶ÈfPf½\x0002ÌÖ\x0005¹¬ëøU"¸V¯cõñ\x0007ubÖ«è¹$\x00174¦eæVÌhÝÑî\x0019C\ëÕwÜñ\x0016p¶\x0006]@ÃÑ\x000cg¦µÍ MÌzmºÊ^K-\x000e\x00037 Ê«<(\x0013³^\x0004Õ*Kmyn&µU>d661ëµI2­Pv\x0003¹suîx¢Ù\x000cÚÄ¬×&ÙJ¼ÎÜn\x001d

6,\x001c-D`\x0006ubÖ«\x0013ìº\x0013Z¡z *4ÎÍ§¾¬b\x001e4Y¯Qç×Î¬ y<S°ï Ï\x0003XÃl\x0007bWk\x0014­4§|`KLMç9Ä¶Îóï:«\x0007Ê®÷©bàð\x0011èåsÙ\x001cÍÝ¶\x0016´«µ VlÑáÀrFM<»ãE\x0016í \x0004íj%U\x001dd8\x0003Ö{Î¢bÿd2gk\x0013óøÒ³Z\x000bjíù\x0019\x0015{¤SÔ94Î\x001fOqÛA\x000bÚÕZ\x0010S6)/\x0012£NÑÙÅ6¬\x0005çRÙA	ÚÕJ°\x0004\x0013w-Mæä\öO&è61\x000fJÐ®V\x0018L¤¡4Ù°§9\x0010y^KóÉ2«\x0007\x001dhWë@ìZM	>`]øÑ9\x001eÍÖ°\x000e´«u æÂijÐ±+hÁ±}´'p
³\x001bt [¯\x0003}äÐ>tÙ!®Ip¼0¹\x001bt [­\x0003uöª(o	°Ë;§ßrTÃ+s4áì\x0006\x001dèÖëÀ¼Î\x0010Bá9";O0ÂÑD\x001b [­\x0004Ñ`¦pBÏ\x0019l­_G/ÆYÅ<(A·^	b_%\x001bX\x0003I\x0005'û»x¼ç57¨\x0014·^¥dÛí}çZ\x001eo²î/ÜnÏn½|\x0007\x000bÍ@â!½\x0016»\x000b\x001cÙ\x000f²Î¯uI7êÄFsQøZläLr\x0007û¤3ù³ò-\N\x001dûÐâuGC\x0007=E\x0007½\x0005]ygr*Gð~\x0017ÎõG!*ýåªçNß\­NIíyÂ]ÖÔ®8x9õá®\x001a3ÏJæ\x0012·\x00167§\x0006Ápá¤å\x001eËCÈ¯'È¯W#\x001b\x001aST¨\x0005J0õÊ(93Ü;Ó°éL\x0007\x0016$ùPÓ6¬\x0015a¹\x00030\x000f­5\x000fCÞý 4Ãýp÷¹ä«>Ï4ZË`sA\x001aãMn¨ëbà\x000cº`Ç×Ëg¯^tÕçù'\x0007úT2\x0017ô\ â\x001c§µ*QhÙXÎ\x000cã·Ëô\FÀ\x0015°kIõö­ÙMB\x0004Ã£½Ý\x0018$Ù\x001eÌJ\x0016¬
»È;i¸¥\x001cyÁÂ&.×s9Éå¯'\x000bÜDíÆyN \x0008^o\x0002ó=\x0017µ·p\x000bb Æ¹ØFoáR°ØEÑ\x0011sÜ1Äæ®ûYûy¾cÉ½\x0014,õ`I\x0002­$IXØÍè
Xj\x0013åÃ&aÑÕ\x001a£\x0010S\x0002²¨\x001c¦\x00131Yí1ÿÏ5°¸\x0005l®\x0012ñ\x001aæÎ¶¥Ã\x0019¯#ïep[ä\x001eä«\x0016\x0008ØäÍã,ÏHcçk="\x0003ûÉöõÿmd Ó\x0002I°E\x0015m&V¯lëé·-Ù É´D¥|1¡J\x000c§<9_&´\qRl/%\x001bD\x0016É²/+2ºB^$\x000b5ó<¥>¯Y¢#\x0013[7\x0008ã(5)Ù eµ@Ì&|îãÝô\e²0ã\x000b\x0010Ò¦5\x001bÄ¬ÈYt)ø\x0002h¾\x0000Ñ·¹à&l¹\x00000Y\x0010YìÿËºÜ\x001b®àµÊ\x0000è1i.AÎ@Î¦¼Ü\ÊîjÀÌä£Ç\x0013\x001cl\x0011ÿ0\x001a±\x0012!«}ë\x00134\x000f\x0004±C\x001fNé°EcÂ`ÆÀÍ§\x001f8Èèã{<çÃ£´ÛB6\x000cËQ\x000f°éuh¯jSÏÑ[î%\x000cò\x001f\x0004ò?i\x0005\/#½Næ#Ï¬¾éø\x000fò\x001f\x0004ò?a2gí:\x0019\x0002Ú?Öú;ªIÕ¡\x0014l\x0010ÿ \x0010ÿ©tÎ©`\x001e"å®XÕú8'\x00136
â\x001f$â\x001f\x001b9W½\x0015\x0013Í/Ï\x0013ér7`\x000bØ ýA ý\x0013§8:eÑ>¢\x0015s,ÌR\x001c_³`fþF$ýCkW\x001eçiÚ*Ò\x000b¬S²\x001f)Ù ýHúc¾_\x0001ËJ]Ì2V±i¿IþAþ\x001bü\x000f­\9b\x001aT\x001aï¥V\x000e\x0019£\x0018"ñ\x0015\x0013½}d{×Mr,d³²EÈAü\x001bI\x001cã\x000b²f\x0010ÿF"þóf±bÂ^ìÖ,Ð,\\x0007R²l\x0010ÿæ+2ÿÍ ÿDþc)
¥\x0013$ãH1d¸q÷¤q¸\x0014l²F"e³@¥\x000b\x0010³väN£{zºmF\x001dd\x0015É2\x0017(;.¢èÖk~\x001bØ 2¬,òùE\x000fÙøD\x000e\x0000þDà\x0003(êÝ\x001c\x000bì6EÎÃÂÇ»-Æ=¼(ÃÃ6¶Ñ<G´­¶ÔÛÖ)ï¶D\x000fÀìÈ\x001b¸DRsÓ³_Lc}R{5ÌÛ¿Í¼·zA¶z\x001aûª×ð¶wÆëd× §Cå«÷z²z¯%Îål\x001eSÒ9Àn±²Ûb\x001cãÎê(ÚÙ yvó\x001a*«¦çÃ\x0019¢	÷vV	w\x0016gZÑÎzN\x0007Æ	lð)ñ[VïÍdõÞ\x0008à²\x0008&/9G\x0014ïpªmì¶¸2L×Z
¸#EÚa\x0010·Åp7½EMñ¬îG%ãxg±3`g!q\x0000Ä+CYVµAPnËÒé{·BËnÅ\x0017\x0004òS@/äCmVùLs\x00063Üh0LG\x0008|{^³]¼\x001aç%ØåÑ]^¿ÿûÿ<¾úôéæÐPb\x001cIZó¼ó@®=\x0018Oº,Ë¾ÙúË³§g'O_¼8z`ùÐöVLh[×<çâÕu|³gÂÙ>["Bß\x0013z1aVcµTß»Ôú[M\x0015t&M¬©5±'RÂ¨b­\x0014ðx}©ÀÈrPÒl35\x0011`ê\x0001\x0010°\x000c
ª#\x0016²Z+õµe^½\x001fj¾Î³ç;xGºÇRÌQâå\x0003CÎ¬÷Úp?\x0014\x001cGA|¸¿mýôpµø\x001eGìàS	Áó%±\x001f(\x0015öØH8\c-¾ÇYJÓë®/\x0013Èi$\x001b÷gÉfï\êp¸ÆZ|c¾¼$i¼M\kå\x000cMîÊÇp¶q\x0008q¸ÇZ|1.\x0010i\x0011Q\×e!¯¢Ssiå\x0012D\x0018.\x000bH/Ki\x0002\x0012\x00081©Ö"ròÚ¼0ª<é]
{­\x001b"\x000c­\x0012WñÓ³µ^"Äá²ô²D\x001c7PCA>@à\x0006\x0003Ø*¡"ê2,x\x001bâp[@z[J7Û\x0012äqn8eWcH\x0010íf¡\x0008Ãm\x0001émXMë\x00081(,<+è¶h7,A4Ãm1âÛ\x0002ÙU·D\x0018yã\x001a>íÒfÂá¶\x0018ñmÉW÷Q¨Ê\x000f\x0013tHä¤ÄOÿØf+âp[ø¶\x0018Ío\x001ejO*£ZU¡v3âp[ø¶\x0018Gó\x001d|6Æ8´«ÚAôfëu6Ã]1â»b<\x001dCÇ\x0016,okwy#\x001d®\x0015_\x0013£=\x000b\x001b´e\x0003íp\x000b.èùÎ"ÄáXñ=1\x0016¨´Õ£½è	1rh\x0006ÔlGP\x0011âèIÉï	Ë=!&>Z±\x001d\x000bj³£b{bå÷$zêá£Õm¨á«\x000cz«§bú\x0008a½*WRÈ`(µ³Ç/\x0005\x0012x«³öÞºÕxRq»Äú¥©IÍ3Åù\x0015UG\x001b\x001bÙ»·³úe7û\x001e¨æ%mZ&"´}êzÞöÙ"ká¾¿ìû\x001b)dâ8ÇÔvW³à´åF\x001dZ­&Ï$ÖTÂ\x0011ò}
\x0015°$wñ·\ÿ\x001a³Í9«ùz²¯å\x001aò½ªÒ©\x0002S·îNf|;a|ûµ©m¸wÏaÅE/4êÄMÔPPñÉ|0H6\x001bA¹Ê\x0006îP3s\x0016ïdúðÛëO'\x00177·W¦b[×r\x000e#\x0000@³\x000bA£ñcg¬~\x0006êwg/N.Î/N÷Gj\x001b&ô°\x000eò\#\x0006º
aF~v\x001cÓ\WRÒ¬ Ä·©JÇ²ä:EÅÉEv,_i{L+ÇtJcAv]Ì6_GAbL\x0014L×cº\x0015«\x0012ÜÔÚi*\x0008C\x0003·cú\x001eÓ¯XM­yÞD\x0004ËJÑÿâ\x001b\x0014\x0019zÌ°\x0006Óp\x0011GTá8ÁW3\x001ccÓc\x0019W`f\x0013=ÑE7­rÓà&¯+1SÖ`ê¶ãÔÅ\x0005Ç¢·\x001dß;³}9c\x000bWÑ®V@:\x0015\x0001u--Ã \x0012ÍBp*Å#HM=ª \x0015:ÈÙÀb\x0013Ý\x001fª­W<n$s½óÊ\x0005\x000eÒ+ó®qªÄa+­\x0002§Ûclû ô
-äBâ\x000cï¬y¸[\x0003Ï¤WÁ\x001ecÛ\x0007-¤×¨¡`[^©q\x001ccÓj\x0017>\x0002ä ô
%äb«\x0016V±t×\x0010<:ÊÙ\x001c^£²²\x0004æÔ\\x000e] Äî\x0008ZH\x000fZH¯PC^Y\x001en\x0011-lv¼çê\x0018«9(!½B\x000bák¢£gÏòðU\x0005<\x001cA	éA	é\x0015ZÈcR\x00054ãì`
RSDn;'\x000c\x0008V("¬P¼éý^M}\x0007ÝôÑd%æ `\x001eòYIR5ití9Y'
\x001feN\x0004\x0001\x000f£/´B\x000fy\x0007<>:ÏNe¾ì¯Ó18\x0007E\x0004+\x0014ÇÔ_â´\x001b!¢6ÑxÙ·)¢0uKÛÇ75ûçÇ«ÛCt	,\x000fÁT\x0016~÷æf\x0003NM:µ<>¯¹??^,\x001e
C\x0019à#\x0018ãÉ#Î5×Lùµ2(ÓC\x0019ÁJ\x0001w-ÄF\x0008ô¶mó=éP.c²=ýJ\x0016ÊõPîëX(ß3ù¯d¡B\x000f\x0015¾=SüJ\x0016*õPé«X¨ÞÁ¬­*ByÏí²}\x0016HÉ$Q-Ì=+VSâ\"Ï¿àR
â\Käyâ¨KVÛá|aÙ-T<×_@×@×\x0002î,ÙÜÙZà9\x0018.:>Tn4jdP@×\x0002î5ö\x0008­1H®ã\x0006L\x000b<EÉ2ªA¤kL{ò"\x0015yÎ¾E\x001c½ë¡\x0006®\x00052=ÆG»ø"%éù]´v\x0012uA
2]/\x0016ê¤D\x000fÙT¦\x000c[o#Ì\x0006¡®\x0007¡®\x0017Kõ/I{tÁ¼\x0018Ú?\x0017[&­_+\x0018Ä:,\x0016ëQAl¯\x0017¾MýÅ$²ù\x0002|\x0019Õ Öa±X/TÔC
n<>ÐsóhÖë\x001a\x0018­ôÅb=ªüÝ\x000f»áh\x000b70Íû\x00177ìß Õa±T/\x0013ÓnÑ\x0000\x001e¦ÇgjÒôZÆ4\x0008uX,Ô#\x0016òýÃ2r\x001aU¢¡Iu³ÞÉAªÃb©^ÆDqÜd7;°P×ÊlXªA¨Ãb¡^z\x0006R5!¶\x0012ÀÊmÙ¿A¨Ãb¡o\kcUÒ?¨Ç¾\x000b¡\x0015ÿ¯7\x0015`ê êø\x001aÌZYñ¬ËÀeÏYÿm\x001a:,\x0017êZ;îj\x001c-ð+\x0006^EÊØõÊ\x000cBÝ\x0008zËî\x000fQÛ6\x0011
\x00021­§\x001aºY.Ô±\x0010ª£M¼8wÖ
Ôzµl\x0006©n\x0004R=\x0001G}³üä\x000bèZmó\x0016	jÆØËr©®±{:Åúlëï
{\[ÖÍ Ö@¬'Ïs!¥6´Î%^ªàÖ
f\x0010ëf¹X×èXwª!Ú&×a\0\7ËåºÎ&(·ªãÑÊZùÖ¤Ç
T\x00085ËE¨Îf\x0015çV´cmøö©×ëe;\x0008+»\Xi¡ø=CaÞa\x0015¡íå2Ùõ\x001dÄ].\x0016tþn\x000e·cÃ8\x001a\x0019¡}3\x0017ìú
´cüsù\x0015ÄA¾©5åá\x001eú»t\x0004ë%¨\x001dÎº\x0015õà9e'ç
n·T[ÕpÖ­à¬gÏæ^\x0015s{÷C{Ø ­ ´´e6®®\x0006Ímî#yRÎßÅ@ËÝ\x0008\x001cÓ0Ö\x001fãÜüçÿüËÕ§O×'ßß^ß}¼9ÔîÛÔ^2øTcpTCÍùUú±Vz°\x0019Î<?}ñâìäû³WçúÖ\x0013íÑ¬\x0008ÍÐ¸\x0006ëQS¢T`Ü\x001e$Fó=\x0017¡¡SQÉ°v(R%\x00045þ\x000fftÅ`±\x0007"°|üKJU&ËÿXÇô\x0018ES©UcóR)Ù®\x0017É0¼\x001cÍf!h;ëàÂjÌçl4¸ÄdÃ\x0015Ð¢;àCx¤iÑ\x0012[¨\x00063iÕ\x0000`\x0013Ûp\x0007´è\x0012|q¶á\x0012hÑ-ø²lÙ@0\x0003\x001bþ^BÍ}¥³<-Ç \x001e¸ 6H6­\x001eé°ýèr:Ì$
$w#\x000f67 ©7!1°kè²ªrÓr7M\x0016¿½þtòüæýá¼j\x0005ÕH}Í9àd­ì°íÍÜ¹8{qòüüéA]ê¦¯æn&¾\x0004ÐgEOÍíáäQ0Í\x0005io\x0012ÔrHÓC\x001a9¤Q<:e¥_U0\x0019&ðJîÏ([\x000ei{H»\x0002ÒãXï\x0002=HiZ	ØAvofÑrH×C:9¤\x0002Â&«w¹d}ãäö¦4/ô=¤CjEÍR«¯\x0000í\x001bc\x0018G>®c\x000c=c\x00103b#ÅCSÞxÛ2FÙ@Nê\x0008»\x001d{È¸\x0002ÒqcÊ~"§µ\x001aÅÁîÍ"[\x000ezÈ$´¥P¡®ä.}=\x001aN\x0017Mz;dÿpïîe/¡tßq)ÉyT\x001fUòRn\x001c\Û¸,Áß\x001dÊ*'Ë+\x000bóí7G\x000f\x001ag\x0014¾\x001e8°\x0007-ÍfT>°\x000f7\x000c³rP9Óð%ÚÐB:\x0016Å°¼ñ\x0008¾f/!Tm,KÂBrà$VÝÞnåzP8Ótð\x0005])\JÕÎ¤æw\x001dÍÞÌËåÆ&/¡Ì(\x0005a0¢Må\x0014-=GÛ#XAzP9ÓLðE®]ïìÉÇXkå²mÉ2(\x001daÃ\x00073Í\x0004_BéU{}ÜÈ\x0016ë\x000eÒ½)¬Ë)\x0007¥3M\x0004_Bi=Å\x0002N\x0014uÓÉ«¶fûRÂ Ï§éÕKnx2\v/=\x0005kÃù¶\x0018ÑYMÏãèâà\x000fÊ\x000c¹»\x0012{ùáîöÃÝ§Cî¨3+T^Ó\x000c\x0014ÎëyU"q/½ºxöêÅ\x0001Ç¹ ç\x0002\x0019çiòºu\x001còüXmôRÌÈ ñ5 @É5Ë°ßf{4+Ck\x0013\x000b\x0001,O-÷[97¦HÑ\æDhFSoì|Ô,0=W\x0019äUóÛïÑüZ4hÙ\x001a¾Ílv1GR²Ð\x0005\x0011\x0019ÍlÀËé9³ç;ºiÓi)Wì¹¢Kq?lÄãÄâþ\x0018Îëmh©GK2´6´
²ýL¯¡AsS\x0019ç'^h]óÆP½\x0010	¥®"Øb\x000bÍlºzT\x00032=à4ÏÂìÂ%N.áþiÎ§M[ª\x0007U eºÀ¶QL°\x000bp\x0005Ì,á°mO\x0007e eÚÀ\x0019N?\x0003\x001eq¦W\x0013\x001eAo\x0012kzP\x0006Z¦
°Ù
/[Kí\x000fø¼FË¶í´
Ê@Ë´\x0001\x000f·­<@`U0\x001d¬(\x0005\x001b\x0004®IÜÀÉ0`#7_\x0008¶i©°ñ\x0016\x000cMË$\x001b\x000eÖÞÍ¼§\x0007ùà>v\x0013\x001b\x000c
d-Ô/Öî¼l<)ÐMº,Ñ\x0006Á\x00062Á<·ý\x0000ç[Öcà¾>¥[é\x0016¶áìîèÁÅGn(§´[7\x001d\x0018%cËÂg°×láL\x001bf×SÛ[z\x0017ì\x0016©ë\x0002pB÷ qÒSQ	ì¹øfNº-+7m|ULÊÒd]°|íU\x00060«t½f]¿\x000f¦| å«=<ªÕÊi}äiØ¥$tz\x0012f\x0015!DôÜÓ5_\x000fÍ'Bë¾ç"\x001c´Ì÷\x000c÷c\x000f)ü\x0001úÌ<$þúäû\x000f7¿\x001dpéçü\x0015ïm+6\x0001Zcf5×w-}ÿìüß\x000f¼¦ú±kT\x0001\x0003	X 4\x0011\x0004ÃF®k×Ù¸¹~¹LÏe$\FÑ\x001bÇÙ\x0008TNd\x000c=\x000fXÜ\ã²Å`¶\x0007³\x0002°¨UëÈI¸3\x001dO²\x001aô\CÂÅ`®\x0007s\x00120à¢ÒBÞÏ¬
Ü\x00015ÌÎAX\x000cæ{0/Z±@ñ¾\\x0003\x00023­\x0007íÙ¹\x0018,ô`A\x0002ÙG´bV?¢óÍ8Âg-\±ç\x0012.«¨èÉGlGÓ\x0018<Ï7mù¼\x0018+õXIå\x0014I\x001fa79/þYlÌõ;\
ÖeGyÕ8X²`dº\x0008\x0005m%£Q}y'a\x0013Ù(ö%r?Öæ,Z6ÀmlgÌ¦-g_\x000fr_K\x0004?¶\x0017áÓ&qS\x0007\x001b<ï¦Ú¶ä×\x0012Ñ\x001fw*)AâJ\x001a9ø,Î¶|]L6~-ý_ø\x0006\x000c²_p<ß#Ö\x001d»=\x0012Y[Ô¥\x001e¿\x0016IÿÄÎ>b»Ôª/]ÛL³IéAøkô\x000fºøTçjÕ%KDf&ÙER²AüküÇ P\x001dv­UÎ
·Þ±ÂL³£\x0013\x0016
\x001a@T@TÔ§Æ'JÇr­£Õ\Ö¥X0È\x0010Éÿ\x0004<k\x00023î(\x0004ãÇN\x001b
[¬k\x0018ä?ä44í.E\x000eCº\x0016"5³\x0007\x0016f¿Dü'Å!²ì g\x001fgØÆ0Fm9ý0\x0010ÿØìØä«¯ÜDµù\x0016²AüDü'm9ù\x000bøwÍ\x000cãaÓn\x000eâ\x001fDâ?zî=|äÇ\x0015\x001eÁÿýM\ð\x0007ðÇGö\x001a«ÂÐ²Ü(\x000fÙ¤øM
6\x0008\x0010	ÿ,1jýÏ\x000b]vóöÌ¤\x0008AJ6\x0008\x0008ÿ\x0004Gu«lËRâó%F4¤ì üA$üSdë'¥Ö-Ó\x0019¶e§\x0015%B23È#ÿ#òY`Üy~\x001d0l3#\x0011ÿxþëÓrÐ:µ8Ê±Vm[±Aü\x001bø7-[\x0007Éh\x000bµ¼lûHÄ?¦8Ñ£¢êìEoIü[
6s\x0010ÿF$þåÎêù¿m2£yLvÛ
ÒßH¤?zIT\x000cªBä\x001aqç\x0013/\x0019Ø-ö¢\x0019ä¿\x0011Éã¹QJÙL>fí\x0002hØ"fÍ \x0000D\x0001$Ó4SJ­Y\x0004\x0006³3È#ÿýòPf9\x0013\x0018?ïØÙé1¹\x0006éo$Ò?Y#\x0011t¶}¸\x0007d¶oËÍ7Y
f\x0007áoEÂß´Ü*\x0015<÷XË[É+\x0006°eÉì ý­HúgÉJõ+Yhq6Kì2ëgçË-&\x001bÄ¿\x0015ÿüýlÉÆ\x0016Èp±A\x001bÿ³l\x0010ÿVdýÛH=vBm!Ýô¤M\x0012ÃqQðç\x000b
RÖ¤¬3Üz\x0006[(hR\x0013J¬\x001d-¶l\x0010fV$Ì\\x001böR::xÅ\x001eu³s*¹Aj8ÔÀÈZ`Ö·Á8ÖÍ\x000eù\L6ÜM'ºÞsË3)LªÉkëYjlz*tÃn:Énú¬hÆÝIì3Ñ,®ì¹\x001f:go®Þ^}úüq/Y\x0018$m\x0010YiÑìh:öùjF·%.\x001b\x0006q\x0016dâLñ¼º\x0010[\x0013wëÃn:æÍ\x000c8\x000b"q\x0016\x000cí5\x0002Æ<®LÍ\x000e¯Z\x0008­`ûSD¾y\x000cøHX.
ÍÎÖf£;´fÆ8R\x001fþÄß\x000b.g>÷âyÇi7<f\x0012&½\x001bÅ\x0001½>\x0001zÝ,­%¾@BW\x000c£æØñÄ´íQÓìF\x000fÖ'ý«ål\x0001ßLèéÜY.4±5jSJÝ[<%[<¼­Þ*0\x000c\x0013ùágt¦Ù)îËÝ)`þããïØ9_\x0003¯ l\x000bÁÛ{ÇÏ
ß\x0005Ìrd7\x0001\x0005Ë\x001bd!³WcÇ}~Áhfo´[ôD¾\x001c¯ÇËñZÀ¦ÊtËz9Ì£H/ÅÀ\x0011\x0019½-CÈÆ{[\x001b¥[x¶<î2«²À3ÇAoR².ÅEhñãYÙ4\x0001®J\x0002OÆ9&[.FÞÙ7ãÎJNÝÝY\x0015Æ\x000buZ·ûê81Gñ¼_Øô:¥ÒôÈ%é3\x0003\x0016£æç\x0003ë#Û(ö !ðð£ö¸pù/+X¹¤=åjú.à \x001b×ÁmL·²öÞ}µÒÕû¢þªºoª\x0008ù°\x0008&vç¤\x0010´\x0005ybÕ$ÉZÊ§ÿòùúã°¿ßà\x000f[+ÎapÉ\x000c]wè·e.øQYäÓ'Ð\x0016	\x0007SÒé\x000b©ï-§\x000e6E2Ûç	ÛgÙ7ëø¨¥	Ä¦'ü¦ü5==wZzî¾¨86÷îð\x001aèà\x0005ÿæmF3\x0016²\x001e\x0000<Á\x000cîÞ­uÂåke\x001båå®SÐ\x0012\x0007ü!\x000fh\x000f²\x0019ó«QØï:Be¬Ûÿûþ¿Ó7ÿÿ:þenyÌ*"«\x000cÃ ø<ÞÃq_¨LwqxöÃ¡ÎU\x0004	=$¬t\x001a\x001fi*¤ÃîA\x0005Ò±%¼\x0019Òôf
dv 6gNaþ÷vÎÚl{2\x0011¥í)í\x001aJì\x0019DS£³¼¦\AÓ\x0006p\x001b5ÛKP\x0004ézH·j)uÓt®4u)Ù'×hû*JßSú\x0015>%\x0014ØNr\x001b\x0012§*Mg¥­¢\x000c=eXC]8\x000fT\x0017Ð\x0006\x000eB¤.QvÚøv\x0015eì)ãªµÔíò\x0018îO\x0007%\x000cIk©·ËÔS¦U²\x0013Ê±¤J2£oÇÒmìºQ\x0016«5kéxæ­Ç±\x0016føµúJ\x001dâæs©GÅ³Fóxx~½Çh4uÔsü\x0008M:7c\x000eªG¯Ñ=X}D×'iµ\x000c\x0000´é¶où Ôõ\x001a©\x000f
Mª'~6Ê\x0001\x000bLcf\x001b±0\x0007±®×Èu}\x0003hË}äþ\x0014%£¹n¹ÓÛWsëz`Ï"Óòj*Î
Ø<ÕÉøÆU`×«$»uÔ×*¯&ìZRré¹²GÀ\x001c$»^%Úcâ\x000bdsm òSÓtRç\x001aJ\x0018&¬\x0013-\x0016+é()\x0002l3TØ]q1ñ÷+t4u#\x000b$ÍVQ¯º;Ø\x001c
sé\x001eáO¾ÆÍÄU±\x00158:\x0001Y\x0000\x0010«áÑu÷^\x001e×]§{\x000b\x001bW.l\x0016óµ]\Ö\x000e\x001faêyeZ\x0015Üæc0y\x001fªWk\x001d­
\x001c\x001dZ\x0005Ö°\x000f¬âÇ`Þ\x000fÖjÒ\x001e;Éï\x0007.>ÜÝ|:yqóñúó~ºl
·In Z2xÜõ\x0017±v.ðwñìÕù\x0017çg/÷/%\x0003\x001eÐH\x0001­æ¡|XæNê=¶äk7\x001bÖ\x0015ñ¹ÏIù¼j\x0019\x0018ÑsÞVdä`6k]Äç{>/æsí\x0019Ë1\x001cß\x0014fS·Dt¡§\x000bbº6\x001b\ï¢öÃ¦Ø½n+_ìù¢/Xî;RæÐìl´ó#àl|R\x0004zÀ$^@Ï÷\x0017§ðÀ\x0012\x001e\x0019d­M\x0000v]°XVK	ñ­æ¨j\x001fÛð\x0010¹ÉÍj\x0011\x0011\x000e"Pe`pä2*Ö0¨D5\x0012-"\x001cd \x0016\x000bÁ¸KÚË÷\x00190µ5ôsÏ©"B;\x0010Z)aRÜ¡\x0019\x0013Ñ¨\x0005C\½cýl%pÓZ,¨³©\x0010x
[7î,÷ÂQ³I|"ÂARk±¨ÆQ\x0002¬5W&Æd85ßÍV\x000c\x0008\x0007i­Åâ:Ëhª\x0004Ál+^CËIúDm&\x001cäµ\x0016\x000bl|f \x0004ï-\x0007`B¾Ë&mÞåA`k±ÄÆsHyÞ-ÚïI»(i«FÙ¹Å"TB@P®û`å[%Lª=)Y=÷h#"\x001cT
HU
(Ísò´öl´&Õ
2æk+E£U-U) \x0012[*[Ô_%éË<_2("\x001cT
HU
ìF8c¶5o2?~Y|`Ú\x00088h\x0014jì!Ñ=Á¢3
J$Ûö\x00187\x0002\x000e
\x0005¤
\x0005ý%ª¤ÂLzL47÷ÉÖëæ=\x001e\x0014
H\x0015
6\x0001¥¹q¸T\x001e¬âj\x00175ûü*"\x001c\x0014
H\x0015
d=çZe\x0015Õb&íZeÕf\x000c´\x0006©´\x0006mÙ6Ä¡½x4[¯{j¿$f\x0010F,\x000cqN!mònjoâÖo«J6£\x0003/4X×Mú$rKú\x000cÈ¹;Ö¸­ÒÚ\x000c7Ùo2V\x0013\x0019U;ø\x001eL³¨"Âá\x0018ñ=ÁênÞ4}b
¯álòL%\x000fíôªZî=î50'ºRäÏ'íwUl[OãöNÚY\x000eªT\x0013X©âÙà-Ù. 2e2H\x001eËÔ1Íþ2ÛÎ1d\x000cw=mwYÂ\x00042H!Q+*²=¿lê°ns)M·<Éw\×*¤\x001a)iý%º8Þ\x001céÌùz²¯¥Îæ¦\x001a§	%v£ùX¦ÍÞ\x001dâc\x0019wfEÒ÷\x001d¬­¢HÛévk»N\x0014Ñì	\x0015[,ØÑ2E\x0011>iLRºß\x0011(5³(o²Ð°tèh«iÜt5[±\x0016Z\x0011p\x0008\
\»åùnö\x0017Æ\x0019¤¢\x0008<\x000fà*½ÉÉX3\PbU|èïyjñiL9Ä´Ôl¨=~wýóÍû·×N.o~½>8§\x0005\x0003µ5Ë'km\x000eáe)é¨èÀ|ÿtöäüéÉwg/N.Ï<;4£à \x0003\x0011\0<\x0004Î{U\x0010ëû\x001fMx4)É	r8ÛÃY\x0019\x001c´²\x0003âÒ4Ù~4iÜT9ïÙ¼­ä!Ô´(aO~Ûã4\x00045¶÷Ø\x000e\x001f·ØE\x0019X
\ã¼moúÜN \x001f»xì¡UëæTà]P2º,ëÓ¸Ûe}C$¿4{,v\x001bÛp\x0015´ì.x|Ð«oá\x000e|«\x000er¼p0\x0016mÊá« ew\x0001\x0007R® ÃB\x0012M)YT`\x0012ö¬ÙD7\\x0006-¼
ºô ªUmðºæác\x0006«¶Ñ
7BË®\x0004
XÑ­kUüØkè&áõ\x0015dÐ´Eà\x000fD×6q½ËnIàk\x001byýÎ/`ÓI^q7ÉëîäÇëï\x000fêVUwx­ø\x0019\x000fý\x0012N\x0014\x0018^é¯N~<»|º_­Æé\x0014¯¸âµÉP\x0002À·\x0013Ï3eØZv\x0013¿}dzp©Le\x0004X6qDFçýTÕ^ÌÌ åX¶Ç²\x0012,C9Û\x0001ß èñ\x0006»@1¾?2`9ë±\x0004\x000b¨µjÆj#*1ÌÑVëþlåX¾Çò\x0002,³+¬á\x001fë\x0019\x001cÌÌ.XÎ\x0014z¦ c¢±X:µÙS>µ	-ff,`\x0007\x0007ñUv±ÍSXDçÙÁÐ8µüó)¶\x000f°ÎÉ8üÝ\x0008ÂO'¯\x000eÔå0¤Â­bÛfÍN\x00054^'¸¾²<}|zP2\x0016ôX À
¢¢I\x0001P\x0017\x0012\x0007ÒÂ<¨03Àc1é±\x0000\x000b{ý\x0015%\x0019çÖ]\x000e5\x0010­Ó3#1\x0016cÙ\x001eË
°\$Ë"o¢!ï)o"
ó\x001a§#®Çr=\x0013`iOB"b+Î\x001a®qÙ«Ó¥Ã\x0016,ßcyÙ&Örã²\x0015Qsæp\x0013-ayµål\x001e+\x0008°²kY\x001c#6ú¦MÌÒµ
\x0008¯ÒX\x0015{¬(Ã²u±L O)S\x0001xØr´vnR\x0011[Jei®TL*<b,¦^«ñ[5--[\x0018-W¼±\x001c
\x000eñ*Ù\\x0012,ÿÈ\x0001\x000b¿|½°k¤Cï\x001f°%Äì¨Ùåò´×U¦îf
-\x0003OFNLÙãå\x000biù¹YHáô.pVã`Õ\x0012%`f	ÊÖ\x0003Ge)^gx¼.-[¦#¸,0ÂÍM/[.]§l^ÆòPU\x0012ªPáRh
\x001c\x000eÐíKé\x0013'
\x000bí:/÷äÉÕÇO×7··W¼HìWGm¡]\x0016\x001dä«yÅ	QýÚ\x0017yòäôòÅÙùÅÅé!O M\x000fi¾RHÛCZ)dDiGFÖ¶ÉôÁðÛup0ï ]\x000féä+ï\x0006¹\x00056µyÔªÍÿû|TÄè{F/_HìÓ\x0006´¾ùÄ3=\x000bóÁ\x0017\x0011dè!\x001c\x0012Jx¹@FÇ¹ü>ð#GHó¡?\x0011cê\x0019±\x000c^+ÁsûÎÎBEfû­éó©ã\x0018?ý\x001aî6=
R\x0012½°ÝèÉRóëõû\x0008]j
®=*xåÚC«ñ
±$çÇ³§ç\x000fÃA\x000f\x0007B8ïÛ:6\'¸6<Å&½
ÎôpF
çZÚÛ®1_69g+mp¶³B¸6\x000eªÂÕ,ßF\x0012g¸¹±Ëá\\x000fç¤p®5¸u­¸o]2lÆº\x001c.ôpA\x0008\x0017#ÏÀÆ2
z;õ¶Í\x0013ä
áb\x000f\x0017¥+\x0017ZPÞVÊqCEÜ¶u\x001b\êáTDN9×ÎsöÇ¾î\x000477mz1[ß\x0015\x0001úð\x000b·5P%.\x001c½´yÃm\x001bì¤I¥\x0018n\x0010sZ*çÚ`r!ø¶Úþâºm5v\x001a3´5føáîs	f>þp÷ñõ!\x0015¬R$IJe
Yciå
Xë³W/K<óñ³Wß\x001eR_\x000c\x0007=\x001cà<Núª¾nv(b=\x000f¬wÁm3=­\x001cD\x001cÄTVÎ'j\x0006d
÷ØwÙ}ÓÛàl\x000fgEpNs\x0016X4SD°g"¸8f\x0013Èá\\x000fç+ÇÝK¢ÉÇ¯v5È+GÍ\x0017²±<\x0019%.ó=­ãÚhppHaãqV.ûâ\x001b×-öhQåH\x000eG«<½\x0003Z\x00175±Ùq¤­\x000bâY
â	î*ÏÂÈËæh<¼õÔ =¯[Øv\x0019ô F´Pàü/W\x0017.rî&6\x001c§\x0003\x0017´9¼«óa\x000cF\x001b\x0016Jì%ÖûÑêXÃyÙ\x0005§F>Î»mÇM\x000f2DËTÂ\x0015áõ\x001e#\ðvÛ5Õ\x000cÑ2!T=m)[õ´·ºlÆlS\x000cz Z&B\x000f\x0014MÉò\x0016è0{ÕÕÖ$·FN\x0017\x0006º "Þ/óãW\x0013ë\x0002EÜ³\x0018\x0019[\Éé\x0006\x0011§e2.`:kq.[ÃÕñ·\x0007©.
tIv#4°r°3Õqø\x0004¹R\x000e\x0006	\x000cB	¸ÏxtÎ\x0011l"ï!ï°ÚH7Ø 34ó¤ªßh±.d0$¾²§\x00011Ü A&³eÍê\x0014$ÛüS\x0012ÃÁl\¹áÂìÂzt\x001fê¡s;«ä}Um_Çªx9Ýp%@x%ò¾Öâæzí6÷20]4q°3Ã©3ÂS)ñ|'\x0014Nj©:Ü}\x001d7Ði\x001dGQ¿Y\x000f^ö¹(0,P²É·\x000fÔhÓáï¥~\x0004¹&{`dDÇnDP[\x0006à	EËF'[O\x0000ÔùÒ: ³l>mÚ\x0002ñ\x0014tyËó@¥©@Óëbv»\x00182àQ©7D¥v{Bê$ÄþBe\x0019q\x0002x¢ShØÒSap\x001ebY ]F%zºÊêõñ!x\x001c9¿-Rqo¯å«øEGív8d2¿\x0016áEª5ÏþcÂÆ\x0005Ïóe±\x001b\x00170ã}à}\x0016áµ\x0016\x000fXäÙ\x0000ÕfÀ«	àÌt6\x001c¸°XlÙ\x0001w,nì6M<I$°-@â\x00179
pG\x001dÊún\x0017±\x0005W¼Ýhhé{×D!yäÈ¤ÑFFáN³À±pØh8ìÃäì`v:o³çÉiY`+ÞæôÀ=~îÍîÌC²¼ÁÖñ8¡|uÙ\x001cô1\x001cV'\x000fÑ½Ð½\x001a\ÍÎÆ*Û[ÍmKw=»iâDÓ£Í\x001csh\x0011I\x001711Ý_'t\x0015ÑaX66Ù}ÎR>}ÖÂ~ÍÆÚé#µ]bñÉó«Û¯Þ\x001eèì%*P%ÉDåjÝ\þîÉóÓ'§ß\x001dè?ÉTÐS*°ß¡\x0003PG8\x0014!´Zv\x001a\x0002\x0012\x001eÌHÀbÖbu\x001b±=&-\x001b¨XÎeïw&Ñr9íÁ¬\x0008ÌQ­Ü°r*p+7¹\x001eÌIÀ\x0012W>Fh©©'Â;;õ\¾çò\x0002.\x0005@\x0016\x000cÈùñ4	ÊMûÞH±B\x0015X\x0001
Vó3ç1y½ü¦õ=XegÖ\x000bÛ.Q\x0000
+FùäM\x0007,õ`I´b_Ã\x0000\x0019)
 =m¥S³\x0019	KÁvï&ÖöÉÏ,q0\x0016§\x0017\x001c®ØörÓ!Ó£ÐH}oªÔ\x0000» Nb¿\x001ff\x0004XÔ×\x0012±ï£²ÕLf0ý¿\x0019jwÉÜ3¦\x0007±¯%r?¯\x000e'²\x001båÐã¯kÆbÌ9{èZî\x001dÑÊdÜ×\x0012ÁÑM\x0017Ú{k¤Cæ¨¡+ÎÁ5\x001b\x0004¬\x0016IX´Â(üe¸ ?æ0>·l±Z$d³ûÎ>âfñ8f¯=¶n[³AÈj
±¦ºDã5¸
\x0016Ø9Q3\x0005ª\x0002°AÈjÍ"P0NÅG®f r\x001c/ÌäØ/&AÊHÊâ´jùh8KüÈºÉ¾AÆHÆZÅñ\x0018PíÍÜ¤]ôr\x0013Øh[K¤lPª½s)\x001eÜ=`~óv6\x0011m1Ù eA$e±3§5\x000b;ùoÙûõ4\x0013\x000cR\x0016DR6e\x001cz\x000e\x001cÒÀü$½E/Á cA$c¦Åy/\x0003Md±Aµ·r\x001bfJ\x001d
\x000cd¬qk8-qÅ&Ê¶ùf\x0010\x0018F$0¾0Ùp3ÈþùÂdÃù7_¡³\x000b6²Q$hÝ.W¯K\x0000òHèÌl2÷R¶4:\x0000øûU\x000c0\x0008¬ÃPru\x0001bÚ¢6U\x0017\x000c­1×_Q¥\x000f%×@Ë®6m	_à\x0016\x0014¥³ç\x0007
Û\x001cÎ-K§Íî¹Ü+?\x0000¡ù\x0003>\x0005gã¦\x0005Ò°Ætí¼píR¤©\x0011´¤hñZz
\x001bîÄô)ÃÚ±&ra\x001cÍí¢/ZOãhIbòÍ}3ÙÜ7ÍUÐòk\x0007CæÅk\x0002eËµÈho'hoehü\x0006h\x0014MãÛÐ²4¹\x001a¥àF`®Úõ'jÏ3?qr/GÔ&Cd¤º+Î$¨ûÒ¢äõdK\x0005lÞ¨æ&£(áh?$Ó\x001ae7\x0015\x0003µ0\x0002\x0016÷Û\x0005$ã:ÛW	gÙ´ë\x001býöî$<¹º9Ñxíö\x0012"S
/\x0007È¾3wÈ4<,Ó«4;;ú\x0015þñ§çõ\x0010\x0012zHX\x0001i©EÀj\x0002»3ä\x0011\x0018MÏhä&Pì- \x0015¥¹Ï:×ëy­ç	\x000b!]\x000féä¶ZÊªü0H\L!Í\^!¤ï!ýL\\x0006Ø¤vÛò´/¯æÇË C\x000f\x0019äAÑæ\x0000Ùäú{åÿa®Í¨\x00102öqÅv§v&\x0003µ\x000fäv×&\x001ea!SÏäÑRæR^HGs¦\x0004i!°Û]£JJN¹ð\x0006±5GMAûv»gØË(GY¾BgSFDå£HáOÿöíP¹\x0006½BÊAë\x0015Ò<ûMÀk	<ý&µAV^#ìø Îõ
y\x00170ÒPÄ¨\x0005h^K\x001esJr;¥\x001d(í
1\x0014)â×Òµ©\x0005i§uæZG\x000b!\x0007¥£åZÇ(Ë'/ 9ñF\x0001ÏGôÇØïAéè\x0015Z'\x000b\x001f¶1¢\x0016q\x0019×î\x0004ú\x0011nø u´\íÝL!®\x000cQ¶ÇÞÀ\x0011(\x0007µ£åzÇhË=9!{\x000e5¢))\x000eÒr®íºrP<Z®y\x000chnÑioÖ±\x001c2³Ód0h\x001ek\x001e\KGÇÒûÐ/%øíf%\x000c\x0007äÇd¦\x0001ä£HoHyQ\x0003«ÇÙáBÈÑë|5(÷¨hÇÄû\x001dÚ
m_/¤\x001cô\x000eÈõ±m\x000fn}\x000c2ìÒ\x001caÃ\x0007½\x0003r½cf\x001b\x001dEz­Ïî7Ïóæ\x00087\x001c\x0006Å\x0003+\x0014³»c¹»á±Ýp;;WH9h\x001ek\x001ecõN¦sö¼ãô8ïwG¸=æ\x0015Ç5_\x0002S§(\x0013°\x0012·~»ë\x0008æ\x0001¹æÉª;öUÃ\x0019YÐó\x0015\x000fGPâ0(\x001e+\x0004¤\x0019ôY¡w2$\x001fJE\x0001ú¼ÝÎ\x001eÏf3Ú1+Ô\x000e9;EPÇ>£ùé\x0016\x0005åvqn\x0006¥cV(\x001d\x001fwâ\x001cx\x001dµ2¶iÆ¹a>BÊ1v%W:Ö·Æî&¦\x001a(È\x0007ÒrC1
GØíAç\x0015:'8îë\x001b^\x0013ÔÖ-xu\x000cÍh\x0006cä:\x0007»\x00014·º\x0014#e¾9t,§Iþ³{:C\x0012â pÌ
½îØ´"y¶ù_M+\x001eáH\x000eÜ¬ð!ÒNH*îëoÚðT½¶´+ddòíD\x00027ËÍ8?\x0002ã ¬\\x0000YñJ\x0002\x0008_¼ÑrÇlA»r¸ÛV~·­kmÑÐ¨ÍL>|·'Í\x0003ÖQ\x000e\x0017ÇÊ/õm*²Á.D	<ê§4MÙL9Ü\x001c»Â\x0006ªcW*¥§1]yïy\x000f³CÏdn¸;N~wlRü\x0014ÅÝµ\x0011\x0001×ìÉIÅê:Êáö8ùíqùÊÐ`
ã9ÓÕ\x0000ç\x0001`jé\x0011(Ûãä·Ç9Ná\x000f&hìiYtql
ÍÏ\x0014Qj3¨®°2yÄq_cxê7ÏVízÇ©aE=Ý¤»åj¼°\x000cÞzÒâÍüM\x000b´øÃ6z7ì®ZéWk\Ü´\x0014ZåAÙu<p\x001f1­cb'§à÷¨I§ÄÓn·ÕmÌEÊòµÓpÿ¬-#
s0:´¸Æ$p¥TºwFaÝ\x0019Ý\x000505·N4\x0018
fXu'g=ÕkXq;?óµ>\x000fL\x000b¾éí"
OÀÕä\x0004ÈO*¨ö\x000e\x0010\x0013Í×1\
Ï\x0000G\x0008lÅ\x0013âoxJl¹ùä G\x001bxõõ\x0004T¯\x0000d©G~À÷I\x000e\x001cé¦Bá\x0008¢Ôvuã´óoÖx\x001cï>çÔek^7k^m?¢c;\x0012z¹Xq²vo\x0001X\x000cÇà÷ª9Ã~­§Cf\x0011æÆtÁ\x0019jìúñæú§\x0003Oeh\x0015¥>zK-IÀ\x0018Nã=áöÒÛõòüì\x0003ÉO\x0008="\x00111_¼¾d;.ò<V,«\x001ak\x0008MOhä¨t}ýñIÞÌ\x0005°Í \x0003\x001fg¥ÐövÅ6GêKâ³Lâ¡ÀÆrf\x0004(³y\x0011]èV zº+>ÆÄ	\x0007Æp\x001e\x000c¸y.Aô=¢Äì
ñ*zÀÆïe£#{\x0000³ïø\x001dáá»\x001cz¼ _AÏ\x0005\x0019OQª;ÀZ1ßYÓ]²©GL+\x0010\x0013õË¯t\x000eÃñ\x0008õ(\x0010WHÄl¤yBDï·æcíl\x000bp³\x001a[8Ü\x0014½âªäÃ×®Ùm´â«²'¦%ZÆMA\x000byõ5®äÒ­ Äq©¤·krÇí¤÷Cz\x0001åë	åk1%\x00061énD)%`5§Àw\x0014Ù¿l¹\x001cS;\x001apS0#oyÓ3v>ö&\x0011AÓ¹bË³
l2´9åÆóbîy\x0017_BéÔ¤WMþA×ÐþºLç¼ùp{{(\x001d=ºV\x0011µ!»ÑæKDSÈpZ\x000fH}tÎÊÎóg\x0017\x0017\x000b\x0000M\x000fh¤8æ¡V¶doü®5|	hlWVÏ5}\x0014\x0001Ú\x001eÐJ\x0001£§QÑò»\x0004Îà\x0001v®K\x0008ÏõxNTë\x001a\x0010=Û´6q·V¯¼Ý¼~¾\x0007ôR@ÌL­%8ÉiJYtÊ\x0007\x001eLiÕ\[J\x0011`ê\x0001\x0014°vyôe*+D8e)\x001fÃíÆ+\x0001Üå#;¬ÄX­G°°´\âÈM3Ó|\x000f6\x0011á(edb\x0006¢jÊM*±ês \x000c\x000fÆ\x000b[¥Ì.
¹\x0000\x0014Ð9êÇ\x0001¡Gu|
ÁÏö\x001d\x0015\x0011\x000ebFËäL&Ä1ðEÐ$\x001dj9£É\x0014+I\x0004[	\x0007I£e¢\x0006'\x001ezé%Üï\x001a|v\x0010X@Ü¾Ë¨Ñ2YC\x0015\x0019
IguÌkhhÒÏ>àVa¸Ké-Aº8pÓÐ.[*mrÜø»$«m\x0005\x0003`.¡õ÷p¢w}[rÆEãMpsÓ\x0004D¸Ö2y	óÙ«õ\x0004yõ#\x0002Ì\x0016,ïñlr	 \x000câ\x001adâ:)\x0003zË%h­Lp\x000bÉ\x001a\x0013ÃÖMA\T\\x0003fªÐMö&3æ5vOüæ5\x001cä5Håu	w'ZÃ: Ö¶K27¼n°YAf´¢á²â¤C¤\x001ej®E¼±q«6AT`§2W\x00152\x0004O¯Î$ò½5³QE6\x0001©6É^\x0012UÔ%cKª61Nñ.ûÉØ¾\x00156\x0001©61à©Cj^C·»Çq×Ðo5\x000caÐ& Õ&X:\x0019éÔÑáu
y`¸	z3á N@ªN0½ÝÐ9ô×\x001cÚ®´Û-C\x0018Ô	ÕIÖ!@Öµ5<DÜªÙÑe\x0012B3è\x0013#Õ'x+ ·YP±bÃì0\x0011à NXøf\ã&×¬¼/
Ì\x000eå\x0010\x0011\x000eêÄHÕ	hÓ&c¢3ù'VQÆwÚl^Ã1\x000c"V)Ùy÷UØ`¥\x0017	\x001bè5\x0012[\x0008l5ÿÍ RX¥DÎÙK4Læ¾\x001etÙ*kÌ QX£ØÀ\x001a\x0005sxÈ7<\x0014;oòìD"\x0011á ¯X^çcXSõ\x0012\x000e8S|\x000c-\x001fÃ|·\x0012\x000eÒÐ¥a´5g+aÕ\x00020 m±Wf«Õ`\x0007QcÅ¢&\x001fÂX-W§¸A\x0014\x00020D²p¸ÈV|[géL(óe ô	{bÅ~|â1{)@»ÈØv£å¥ó7á¤$öä}\x000b(Y\x000c\x000bGR)ÜP\x0017·."\x000c^È¸éF7,õS4\x0007\x000fñr;vU8üj7r\x001a+çÄS©aFx§£	ïp3¬àÄ,¼z6q C"5h\x0012©Af@ÊnÏ\x00144ß \x0015\x000b\x001a¨¿wi\x001e¦Ø*cÃ6Àæk\x000eêÞ	U+@½£I
	»jGËÆ\x0019\x001b\x0016jû\x0003¹·õRÎHÛê{;¯×]¥/,àó]ú|ýqrð'B9oIs×Ú,ä)\x001d+«ò­&¹êZÕw×2>å<
QÏ¬rV~xÙj®eÄ7#â\x001b!bÈæP½åÊ1=\x0005Ñ±8\x0002í¶?^í^¡+ãt\x0019±C[]EO¥Ùy\x00159`\x000bj»ãpOb5\x00123Xvc½bNx·^©Ýä¥<ÿ`Ì`¼¼¹¾ûm¿ð
{¡q¾:p6QØ%×=	&çg¯þýa2èÉ@DæKÉ^Íû
T\x0004Á´ÆS\x0006ö$:-D3=\x0011¡a+§Ô\x0002P\x000b´àZ¢ï|
×b2×9\x0011YÒQºuÕø,\x0004oZéIMí]æ{4/[4C±\x0018\x001fh?]ë;£÷%®-D\x000b=Z­#¦\x0014ìxBói×ôjO2ØB´Ø£EÙªÅÖË#¶Äà[\x001f\x001c\x0015÷äV-DK=Z é,/¸qoÙ¦3l¬Kö³keæÔÐÊlÁªa:\x0003UY\x0006_ÀGÇÍ¢Ýª»\x0010m8jZvÖ2\x001aÒb«:Ãlº±mÚP=l¨ìhÉ6\x000cõ°ES\x001eåk\x0016¶'KTcYØz¶ìt\x000f-HôA>ò÷\x0012×«öæ$¯P\~Þºªªzâ^MûªºÂ÷F°zÉXz\x0016Ë\x0012·¥h:ïéJD;_++À»à]}\x0015«g¦ÝcMé\x001eûüöêMÍv¼:yþáÓç\x0003\x000eZT\x0016ÈA\x000b:[îjö +\x001d3h_>®§'Ï½xyÈ~3Ó¶±¦´\x0015Ñ\x0019\x0004\x00194öà¨+¸4RË³\x0002ÎöpV
\x0017è\x000e§*R©Q^:V_NEù+ð\ç¤x\x001c1jÂß'6l4«WÏ»ÉÁÃ?½M\x0004Èp/ïnn¯?Þ\x001câÃn*öÇ65º6ãä[¡a®ås{ùêüâ,_ù ç\x0003)\x001fÔ¡bG\x001d[ÃCEËçÜ$b\x0005éù/{lN\x0017ØæLÞñåHj®\x000fº\x0008ÐöV\x0008m\x000eÉ(ýÆ¹ ¡ê6gíf@×\x0003:ñ
úÖY×\x0006\x000cÿÔ\x0015\x000c¤7\<´¯\x0000ô= ® ¶è\x0004*¹. înú,²/ô|Aº8\x0001<2£¨ÐúÿQ÷vIråÈïVr\x0003\x0006w|²XYÕlc\x0014?Ê¤ûÒ\x0016d¥Ô4c\x001a~È¤û4Û\x001d\­£w2+¹ðsÜ\x0011ÀÉÈp ªÓ2µ1³»ª~í\x0007pw\x0000îÇ\x00180i\x0003¦\x00160i
hMn9ñ\x0003)Ü\x0005íæúq\x00000·Yídr=¡çþÊâdø~´X\x0010g½LsÖ -h´&$µq\x000eÁÙ\x0010 xë\x000f
P\x0011öqD\x001dH¨6WaÉ£ô&K\x0007¨÷Ó~\x0006ºH\x0002ÚPbý²öV\x001b\x001aö0Uà×Rÿ$a\x0017K@\x001bLlòr\x0000´´\x0012­rRA|5¦é¯Ü\x0005\x0013ÐF\x0013\x001aG\x001f%Û\x0002\x001e¾d!Ä©à\x0008_\x0017K@\x001bL\x001cÖ\x001b\x0003È+ß,ÅæºO¦wr\x0017L@\x001bMWö\x0008VÆª[\x0003Ì¬/.68\x000f+®&ð9®l
Ñí(Þz6%.6¸rc-RÚÈ¢ºVN Bxp¢°' 
(¾l\x0013VX&\x0014¯ò<Õn: c\x0017NP\x001bN«I!$'"5©Æ\x00034U|]0Am0ñ\x0019E92Ì*L©^ü9;»±?hõ\x001a\x001cbýÂ"©ç!\x001f[©âëB	jCI02ÌjÁª¹oó>kuÓ«F­«¦¹e\x0012Ë\x001a\¯\x0002­CQÚòÖL¯ÂÎ\x0013¢Ö\x0013ú¼TAG§5oµ1ÖU§Waç	Që	}àÁ®ÑX·®hn6£ÁÎ\x0011¢Ú\x0011&Ï£¸	\x0003ùÕPÏïfv\x0019ÚÎ\x0015Z­+ÜÏ¼*Ë°S\x0012/Ã([y[l2@Ø9C«vIÆ^\x0015\x001bÊ\x0015µÁcµáìW¶3´ZgØÚ0fY
g·²íòV«Í[C-\x0001&\x0001^ó±\x0010F\x0011¡sñàh3\x0005aùõZoc¡ª´B\¥lMíw÷öàüÜó\x0011as´ü¬Í¼BMÿ!Ï\x0006~ q.¹Ä\x000b`\x001a>9\x0004ÃUÑÄ¸\x0017\x001d\x0013Ù
7\x001bV d$=cV»mª\x0019­ç7tkAÄô]òs«±¬ñþ\x001cê\x0014yj
&NG^shâôQt?~\x000f£¿iÏË©2¦e0\x000eËíýÎt¢ÝÕßq*ÖL-<7\x001b³õÝ\x0000ùÊ5\x001b«WtnòÓ©¯y\\Ï}ï_UI_£`¬¦Ü¶;\x001c·¦ 7eYwT©#?\x0014YÉýMØôu,Üûæ0ðÍ\x001d 7L/çhöC>WÎ8}Û\x0014\x0007Ûõ¿W2,Ö¸¾\x0013,_\x001de~÷0}]â6ëÒi×¥£Í^\x0004­Ûè¬5ËhÍö[£ÿà¾\x001eªCNuD-çþ\x0015ÔzÍ\x000cÞóFzÎ¥6\x0013\x0014EÕT½æü\x0005mly\x0007-E¶ÚëPpõ2ÏÖëÐzÏ3¼¹\x0007\x0003 >×{[ºî1\x001cÏlu\x0017g]\x0012Â½\x000f\x000f\x0003+4úª\x001fjjL÷i¿Û§?|¾ç:ó\x0000gI3CÞ»¥Õ+åì+çôVÜrÆ\x0014Üm}¹4$n¾>W{F?#{ö\x001c0'K¯±=Ê¥¸ÙHÄé\\x000e7^\x001eõ^>#«w\x0014¯TÅQú­)®?ä=ú\x001bÓ{;hÀÇ;\x001f(\x0000­;Èà\x0014\x0004©fvéÁû;âk9nè·Äµ'\x001f¾Ý]ýôñîûi®l\x0002Í9'.:£±xy¤ÆÖ+úþ\x0013?yúæöê§g·oO}Ü
-\x0014* ¢\\x000b¸òGG\x001bå@\x001b­`²-U0¥ZXMýÂäØ·Ð³Ö8k¡ÜùP`¤tnQÈ\x000f\x000cU²sÂq(ßBy\x0005\x0014Èáf_ðsi·Èú·>\x001dShÉÉ±­\x0013àmuÒE°\x0013P±
¨ýè\x0012­x\x0006Yµ\x0016x\x0013þuP©Junj~B\x001eªmK@ª\x0013\x001aí8Sn²ÎP|\x001ey7\x0013+Ü0P-®X½¦9(å}qT!!+ÉÆ0AÕûòó9ÉÅ:NÓ¢wÅ]J\x001fÃøÎÃùÞ$\x00103g;\x0011%É-G²j+;î9¡sçp¾?OÔèÆ¹Íú$·PÆ\x00140Cuî\x001cÎ÷çÉEñ\x0008HE'ë²
\x0019ÄT¾1\x001dUçÏá|¨*)\x001cµd-PeW
ÔDäÎ¡Ãù\x001eLöõ§k£Sk*ê\x001c:ïÑ\x0007V'Z\x0006ó½bÈu\x0003Ú8¹@çÑá|\uÔHÇn¡|À:ÿ0O¬ªÎ§ÃùN¨jHv²\x0001CÚyÉã¶ÂÎ±£Â±»t-\x0013-mI\x0019eYI¸fªsì¨pìÞH\x0015-oöÅà!æñÕ}®pì6±è_	1(¹BL²ÚÓ©:¿\x001a¿î«©Bã`È¹6XMä\x000bØ9vT8v/Ê\x0004K×\x0017O\x0000FæfFÓ?8è¨:Ç
Ç\x001e\x000c\x001fh¢\x0014×F³\x001f8\x001a&>_çÖQáÖ"2g¤K¨ä<}Gªóë¨ñëÒ\x0015\x001f]ÉEÁo\x0016Ut\x0013§dìü:*üú~ä\x001cMLb_\x0015Ô,Æ\x0012\x0004Ç©:¿
¿\x001eÕå­ÕT\x000bÄÀ²ÚÆ¿ íüºUøõ`¯eYY)ÔuH[	ã\x000eÔvnÝ*ÜzI§øòeyä\x0003 Z«\x0008\x0013ÇwÛ¹u«É×÷S!#ÔÛ\x0017#ÇÒ%G\x001e¦ê¯_4~}ïA)5\x0016*¬~ÝLPu~Ýjüº¿N<þ­\x001aJ*\x0006BÈAmçÔ­Â©{¬S©lÞûªz'\x0014íÄ¢êüºUøõ&¡Z\x0010ÇTNx*Ûyu«ñêFn-X\x0016±K?§äÅiªóêVçÕùûQkD¸,WÁºÞyu«ðêåä.]\x001aÉK\x0001µÖÉqËA×yu§ðê%â{â\x0012uäú\x0013åá4¦qK¹Î©;S!HÑ9:\x00085	~ü´å:§î\x0014N}\x001dó°PY¼zË\x001f':î\x0014.½µ¼Xª\x0017ß_,l4TÏ¢bµMs«iugþ¼{ÿ?¿ß}½z²ûr\x001aÎø}á«#ybm©qùà$Â?ß<ùÇ··¯¯Ü¼:\x000b\x0013[L\x001cÀ¤ò]®d²Y-9\x0016¿+\x001dÒ{ÑRÚÒPZyð\x0004/\x0013oH0Gjë²½1]é\x00060©å.°ì0Fo¥Ø3ÅCc´¾Åô#Ö\x000cuizQÇX§:º|P\x000bC\x0019[Ì8\x0019GMï;¾°T¤\x0008ÞÀ!Ý\x0004-ej)¤bØ%\x001bw¬å\x001aØê\x000eZÊÜRæ±É
E4Dcmþ¢)åð&\`\x00035½¦¦ÓµQX3Èõ\x0019ÄPö\x000f\x0017AÎÞ¹xwzÂåR¦hø«Ø3×Å/ðÙ¡ó0â83î\x000bä\x001d?\x0008`\x000c2²y#Ð6Ù9$\x0018ñH9°ÊsÁÕ¿Çº×7|¡ã\x000c\x0003Ë³$d^jñÚ¯\x000e>aÜ·\x000e]Âç\x0011×I]Úì"ß¬ÒgmD¿´ë\x0011ß\x0019k\x0013z¯W=öev\x0007ç\x001fk1;ß	\x0003Î\x0013{jH(1IX÷h\x000eÉ)9±s8â<c­\x0007 boN9S4Õù\x0002öÄÎyâó\x0004ØöÄ\x0005ÊÅY6\x0011ýÇì3ãÔ\x0018R\x001dÏM]x&¥X\x000b©\x001d\x001e\x0012Ôrv>\x001e\x0007|<@ºÞ«\x000bd®¡\x0008Ó\x00056;v¹1\x000e$Çä045¦ë¼úøZ²è.áá±D8\x0010\x0000mÛÇÖYNsÂiá\x0012\x001f½D8\x0010H\x0011kÓ\x0011¬ø¤l°Ô^"\x0012a\x0017p \x0012kiï(Û^|Ý÷\x000bäsØE"\x001cD¸Î¾[1\x0003?¼cù¯W\x0011¬ZÎ.\x0014áH(ò¾~s\x0016ºKNdc½»·]\x001c²\x0003q\x0008Ë\x001eâìf¥ñ(c\x0014Çé/qØ°]\x001c²#qhÍ«ÄWæô£6xøÂZÎ.\x0010Ù@DFª\x0010'*AÅ\x0012Öã\x0005¦í¯hFÂ\x0010]ëòNGéEÀ´Nð\x0017Y]\x001c²\x0003qh±¦ÔHYz©Z­Y=gºDÖi»HdG"\x0011UñêDË÷À\x001c×îëtÕÙE";\x0012=¥\x0019¡jÓêåñ\x0002ÝvÈD¢è¥Ö´¶\x0002G¢PÅÀ¹ÀÝv.Þ\x000e¸xjµG\x000eE6Él6qß4q\x000cÄuÞÓ
xOJâÈçÉø­ÂÄ{F}ä:¿ä\x0006ü\x0012qr=\x0001yÏµÊ8%\x001aÅºáZÎn¿»ý¾LfåRè­9åÌ¾#\x001cäìö\x001bÙG9À\x000b*ä«Ärz«áÈ^à»ûn}úÁõÉm°4xH¢¦\x0011Í\x0012æ÷\x0011Fw~~ÄÑÓ0u9\x000eÖåXUæSyþÈ±ü<}ÖGøæ²;Ù\%oý%\x000eG¾iéZqïô¨eiF¹\x000bA®bÀ¾Þ¤K$ô¾^QwCGNÙøÆp\x0015\x000f\x001d9+j¼Ä\x0013Bßx¸<ÉÐ/ô¯2¹^\x0006Ë+1ú\x001a{Û\x001b\x0017{ÃU§7,}øX\x001d¿g}W\x0003¾:þK$Î~kW£òèò½¸}×Kß_ï~ÿð\x001a\x0011Ý}-¤ß#ÆPòzÏ].Vúl¤`7lªàþtûËÓçK\x001fâíëBùæa<lñP\x0017Ê%öM\x0005SÚÆËl®esJ6º\x0005.?«gwL¢¥\x0014B5]hñòËRrÜtL®t\x001eb­åÅIºÔÒ%%¯B\x000cÖ×q\x001cXK÷b¯¼¡§k\x001f.ãÚÇ¥Á[/¶Öñ\x001akUøäë¶\x0005(÷E Éæ\æë¤[\x001c\x0014ôQóà$^·3@¹5<IûsÁoñØ|÷\x0006U\x00152Ü\x001aÐm
Pî
I>¯§ÆûõàhêÁ1ùþÂ`¯Û\x001c Ü\x001d.Fé%ô¾¾\x001b³±éXPóa·=P¹=\ù¾5zzÓ_\x000e´å\x0014!b)øIç}ÔPn\x0008\ÛÕ5û\x000c\µSr#|1Íòuû\x0003ûf¥rW&k®WýÜM§Ü\x000fð\x001dàëö\x0007*÷KIÂn zïõ)Â\x001c\x0008óFy¯Û\x001f¨Ý\x001fÞÉsc N?¿Ú¯\x000eË>Mú?Ûí\x000f«Ü\x001fó\x0010<7»Ãþ4]?Ä|\x0000®Û\x001cV¹9l´b¼HoÅ³ªpÒ·ØnoXåÞ°9J\x000bK\x0004à&$ë\x0018o2òÚnkXíÖ(Ë®Z<+Y_Þèí
ðu[Ã*·\x0006M:æ»ÛHò¸~^*ß¬kqÝÖpêÐáêç5RZ\³¯ËÏM¦\x0006®Û\x001dN\x001b:h<4_Ì$nÅ¡\x0007wmÛ­õxýC\x001b9lÌ%z9«Cæ\x0005opúëv»Ãiwó\x0015Ú\x0003²\x00046Ç|n61uÝîpÚÀa\x0003eË\x000b_\x000euõy>îz\x0013`Ïw»Ãkw\x0007ºú¨à\x0003\x001b$áó³ïv×îræM\x001c;èçA½ÑöÆÚÉÄÀwÛÃkÇ\x001fîý|·?¼r,¾ü}-òÁ­\x0004_~añÆL\x0006\x000fßm\x000f¯
\x001e\x000e%o\x0008<G\x0019Íøa%g;\x0019|C·=6¯ªuQe'Ëî ªr¶\x001eÌÞ\x001anw\x0004mfEï¦<Ò\x0018>ö\x0002Í\x0015ï2\x001bÛB·;rwÐl"¾\x0012JÅë;\x000fÔÉ±%©Ï³öëo¬´»\x0003½¨I¦z½\x000b	¸*Óq|±[~Q¹ü\x0016\x0005u{¤hHþp±çc¥\x0007t.±[~Q¹üH\x001f_ÊE©ePÌ\x0017æ\x001fì[¾åg\x0015a2µ\x0017ºùþÞ\x0001VÍ\x0003Ì®0õw÷ËÙ~£Í\x0012¸vr}àq¼<Á?n1\x001e3Ô\0Ð\x0010Óå
F\x0002Ý¶{]½\x000b[DP\x0013\x0006ê¤qU\x000e\x0004øu¡JåàGã	½'u¯\x000bä\x001böÃ\x0006í¾^=ùüý÷Ý§\x000fî¾x£É¶d\U\x0005À±`B}ÿ(>é°\x0008ãë«'/ÞþróüéóòÛ\x0007)mKi\x0007(C®j\x0013ÑóPWjWÌñ°Z¾\x000eÓµn\x0000Óû*Õ\x0001U~"íï}m:¬^«Ãô-¦\x001fÀLõzÕÅ$r\x0006©êi'sD×_\x0019ZÌ0Y¾4\x001fVlÁ\ËÀmr¡Ê±ÃÚµ:ÌØbF5f6\x0010ä-¢Î|·)Ë]\2x	ÊÔR¦\x0001J"b¸¸wÆÒ?\x0013Ã1P:ÌÜbæ\x0001LW\x000f®¬RQQºúÉ\x0017ØAûÇ1Âl&HÏi}\x0015ªÌ^¶P\x0006ÙBñØ¨\x001b\x001d't0À\x0019£Üdã\;>lq§òRÓ\x0005V'tQ\x0008ôa¨Ä\x001bS9K\x001cbsÚTõmÝaYe\x001df\x0017@\x001f²\x0011·Yâ\x0011Æå,: 1\x001f\x0019|£ì¼;èÝ{ù=Ê%E1\x001cwHºså\x001a,/ñÍ;¿	\x0003\x0013\F
o\x0012\x001d¸ªì\x0011ýg\x001dfç8aÄsR7,{NgªK
 [=\Äç\x0001×	ÆËVGV\x000ftt'U?û\x0005ìëÄ\x0001×Y¢ö^ãÂóã+¡C4.I¨ë8ûÄxÀ%wR
liè\x0008Û38Ùîxd0¡³Ë9Qtfêà\x0015½r:d³	Å/\x001bcÍ¡>Ë\x0010åòÊçf
gr5§\x000bøìÝvÇí\x000e±Ö.gÌT}¼¿1m·ìÈ&"e\x0013ÙìÀ'
Gz\x001cÂ\x0019.\x0010LÚ×,®yçNï>ÑVís\x001fD+7B.«\x001d\x0019å¢<a¶§õõÙL$P\x001cpï\x000clÍý%Ryìz£¦¼\x001f§i
È\x0014d\x001e@pGÆ(ÏÃ[£º1£®,k¹\x0016²'¥c±dw._`ëÓ@Þ®ïô¤èèZxuRË[Àr\x001dª|3\x00179%õ+ l+$äs\x0012ÊDì¤Ue©µ\x001e\x0007u°Ñb*¿ Û¥§¿ÿÛîë×ôÏ»÷»/¿}8X6~9\x0018§qùKNï-\x0017ÿR\x001dp·ïþòòæõëòÏ7On^ýøôa<×â9-¼.\x0003H÷·±\x0002æ^×_\x0003\x0008.oJéXÜüçïß\x0016¼W\x001fî¾ÿÇhÌþFÆ\x000baðU\x000cû"W/Þ¾YÈ^=½}ûO\x000fsaË\x001a.õN¦{×d\x0018C²µ¬¶o&×Ù\x0016Ì\x000f\x0016óJ³ú,ò5jxçnÆ¯)Á\\x000bæ_ÒJ­ª\x0008UO¹?Ún\x000fJ0ßyÅl=~¹ì¤kÔÇZ!{UZ-XhÁêS&¹P+Y\x000e:þõ¦Êå)Å+*¸hÂ\x0005ÏGðI\x00060£¯EÛÔ÷2\x0003Z°¤1XÊòðE²Äê¸\x0019å¢\x0005Ë-XÖX.\x001d÷µlÜøé\x001cIs²XSãNîÕhLF\x00138¸B;%>,c0¹.þ¾åOKÖ;~ç1D©¥îõÉÈò\x001d7\x0018g>%t\x001f\x0014?ÒÄ\x0019¾Uò\x0005½Û×<»\x0019\x0007\x000bç\x0007ë§:5\x0016ba\x0019´´\x000cäYÚXÊa¼ßý¶ûúíËq²ÎõÊ÷û$î\x0011ëT»\x0008R
F½Õ\x0013&ë\?h|´Nî´bÒ `¡.³í¬óý qþËÀÕûÿgUäªÉX*ºÝ!ë¼?hÜ?U\x0004± J²Fôi0'©Ìq&^BçþAãÿS@¹\x0001*	,OÍÂýDöìÌ\x0014YçÿA\x0013\x0000"\x0015<¬&\x000bùz]e$äÄ\x0005\x0019vsÓ§ãÂÎý£Êý^z½yöë¾ô"2O3\óGó\x000f¾:ÿr@/ k\x000c\x0002Ì%ì,j,Ý^\x0015[ë¡ÖþH0ã1°óe¨ñeÁ\x0000E£ÅfÑÒ\­_;Jzæ¦\x0016Yç0Pã0(L²L\x0003\x0005n¢«¥Ô%qåØmKÔlK\x001a
Ëò;9[Ñ3ïä|IÑflf»
`5\x001bfðô\x001c?&d\x0002êrXO3dýùR³\x0001,Z\x0011_È\x0005«Ëzö\x0005rÊfÝ\x0006°
@ey\®]æôòZ©{
LåðÐ\x001dÆh¾\x001càÖËôâ5¬È+\x0018\x00192Y¼H\x001a©l¸EK*WKÂ§\*mAÄÐØZ\x001cNíÎÓYcù«»à´ü¬I5¬Ô!ÓD´¦\x001a4W¿èF3Xí9ºÒ¶Õ{,\x0017»goÓ\\x0015§ròRØf(7[¿«Åm
¶ÑJX\x0003;Ýy KþRVÀç\Ï\x0003S\x0017.ùÖ_¹|ÓdjN\x001co °35y^Ê\x001b©	õxc7£±Û\x001f\x0014½¹]s´]U.8\x0014-úhÙ\x000eQ¼cýä¢{·Ytï4îRï'Çvî/®YjË1Låàæ/ï7_öýãø²[\x0019åRMõ]ÿè{5ßW¯ù¬î"åÖÃðdbRI\x001fg.â'þv÷eãé7
O"^C8H«²\x0017G<uUl÷¾·bÕÑ(\x001a9\x001a/Wò®h¤\x0002Ï©cévÝ2ûò\x0001Møb=-z4~\x0006;ãP\x0010î}\Ð}Ü`­ì\x001cd\x001cSÉ¥¤]ª¿f¾®ÝY«
³TÑÎ»ÙgV÷ä¬ä\x0000fjk\x0014÷nãñ\x0014ûö\x000fõxàî­<§uyA\x0006@/y\x0000ßrLzÍÆÎÝØlW\x001e(ÝJHR¬R7\x0018ô<\x0015À»\x001f´hf5~%ä*rKM¹Ú¢lÓL\x0012÷2\x0015Ô&*¾Ê¬S
{äK\x001c9Y \x0019ãÙMbUyÅò9Ù¥|*[é1Û\x001fcO¹Ý÷wÿv¿®\x00017\x0013¦ÁÇ\ÕôýêÝ/ÿyõÛÿù_ÿûöSùáT\x0001\x0006\x0016\x001brµPdÓ¥h¢è\x000eåûu-o¯~¸yõê¯~¼º}^þxªþ\x00027e
Ë Ï\x0011ÎEµ\x0003\x000bòZÙ\x001b)º»\x0000¥m)í5I=ÇùP\x0005Ø«ã\x000f´ÍèA]\x000bêÌéë[Pºd_\x0005ÌP=¨oAýE\x001dÝØrãsoÚOèÞ¨_\x000cr3\x0019ÔIæ`7±\x001cöÓÝýâU=hlAã\x0010¨©ÓÚl-dÄ\¥"Ã"[=gj9Ó\x0010'UüïW¨(À'ñLq{r\x001f\x0003Í-h\x001e\x0002*UOJ7¬hA¾|Ø\x000c\x001b\x0003m:hÐì;hô&ºF\x0003IC]£gôdD>"
$\x0012Òçk|K½¬®\x000eU1ûK\x0018´I0\x0016Hëk?)|íO©Ò-\\x0000´\x000bK0\x0014°©	.Ä,òÿR½¼H?HÚÅ%\x0018\x000bL)Ò3Fú§\x0016\x0018®w».0ÁPdBÌûeäÖ3[¨ô@\x001b´\x000bM0\x0016Êá«£dt1)Ô*k¼'.4ÁXl*ÇoQ8ÝËXg[71Øù]p¡èTV¤(;#Ê\x0011Å¦"¸\x001dÑ]âãwÑ	ÆÂÛW®ó»Fvµ3í"A\x0014»ØC±ÉÒ41¨,°\x0006k9éö:w´\x000bO8\x0016\îÿ8ÑóR/\x0013I±g\x001e´?1
E'\x000bPEQË\x001f×¨­}t/AÚ'\x001c\x000bO\x0011«8oUg?Ùêô\x000f´*éI»ðCá\x0006ÇK«'àub_êkg\x000bì{ìÂ\x0013§XË mÎûü¹6"CºM;¯c^?Õ|âSäu*\x000fÃ\x0014.`çKqÌ|Or = ¦U9ÔG©æ´²c.ª\x001c­Î\x00142G'¸¤/µýuÉØÆ/»=Esµ(ì[>ã\x00052hÛm';´ßa\x0010´ñóR¬çûÍØÖAÒn;Ù¡íd¡\x0016tRqOæokÇu°i·ìÐv"ù2>8\x001aòÆ1¿çö\x0002 ®ÛOnh?NÈÌ \x0010AÓñ{¨KMOÚm(7´¡¬5rk²\x0008µóÇ÷õøt[(×í'7¶¬¯ò(%¦®Å½\x00054WÚû­zÒn?¹±ýäör\x0004øEÚP¥Ü\x0005\x0012>\x00177¤[ßIe¦ÃÈGÒ²õkºï.pOîRÆ>\x001dsUf£ÈEæRw0¡\x001fÒ\x0013#OF{!µõç\x0012O$å»\x0016¶`ì\x001em~ÚKµ­oOµOYýü$W¾ä\x0002 ïOr1\x0015\x000ft*\x000fQ6ÆµCÆÅPïøéÐ/)u¬u[_<øºÓÃ\x000e.\x00040YÙ\x0014¹\x0013\x000eõ.±jýv! \x001f\	@´Li|\x000c\x0017þä\/©ü\x0019ÉÀá»i(ëµo\x000e¦ëÕ\x0017üùn÷éêÏß?~øt\x0002.ÄßW)µzÀxíu½·«þ|{óüê\x0017o=}~âÉ°%C\x0015YÜÇÑêl	£5Û÷R\x0013\x0015mÑ¬
-\x0005ÚÐË\x0012,«ÑÕd¨Hp÷\¼ÌµdNg´´L6üdcC½d\x000e9ß[l*4ß¢y
Z*Ç \x001e\x001eNw\x001cÂ\x0013\x0011É8L¡\x0016-è¾'ÌI!m1YÚ\x000f(û±å:9Ù\x0002t@\x00174\x001b%ÌíÍÔ%Á°æ8Åm8\x0006\x0003\x001e\x0017üý÷!\x0015ZnÑ²\x0016eW0£Ä\x00144\x0011J=pÕ µÓ° >WÉæý5\x000f[ÍÞ\x0003\x0016\x0016÷sn¥A\x001f\x0006tqÀWµD$euËl(_t[\x001f¨eë\x0002\x0001è"Á^Ñ\x000f³T \x0010[õ\x001cS\x0000º@\x0000ºH\x0010a?ç×¬EF%FÕñ¹éþ\x0005
­\x0004 \x000b\x0005ÎII*F\x0019¯b}ðõ9¶.\x0014*\x0016ÐD\x0006®&Bë¸ÍR\x000f8Û-¦¹ÕÖÅ\x0002Ð\x0005\x0003\x0017®q=hÐ\x0008ôl7Ù¥>»{çw\x0015[\x0017\x000f@\x0017\x0010ÈÙÊn·ÁÛ:VzÎl]D\x0000]HðFzé±·yÇ\x0016¦Â;t!\x0001T1â¨é¡QÄTÒG
WØÅ\x0004TÆ\x0004'¥í\x0008"êRìV]H¸ÿ2¬bë\x0002êB²rrA²\x0015\x0002¸:mýþu»­?\x001dè\x0002õc­[\x0001ÔÒXêad¶m»­
¨
>ÈË4¢¿æO¤¢ÓûG\x0015Z\x0017\x0015P\x0017\x0015Ó3ÍÔåç}åôì\x0011¦)vQ\x0001uQÁ-©äÂV¢\x0002\x001fFµØ¸t_\x001eUÅÖy^TyÞê])É:Ö#_8·M;÷º&¸óV ÉÃW&9ÁlUh¶ó VV¢ô²Ñ'()o¨tÊóÚþ\x0010¯Û¥ðr3}ÓÎr3³tN(Ò¤e0Ô\x0008c4IR¸ÉT¤Ð\x000eëvMò»T4¬.¸Uàs¬³Ùï0+
ØÍÍæ2öÜ]ëku`ðrT\x0002XU\x000c½/Ã©;\x000cÞ#4JDº\x0016áKx\x001bÌ£\x0008Nò¦x:K?R³º\x0015]4Ðw'|üøù\x0014\x0014Ý¥Ë}%È+k\x0015\x000c< ]J÷Ï½8a1³\x0015Z4ÐWø?VòKK­üP\x0019ä\x0016Õ\x001cÎ>*´TACåéO7<2V½Ü5G^%ÎÂjJ£aS\x001aý\x0010­JÎä9ä½ÌËÓ^H÷\x000fX
®n]faa®7§%I²l¯êÐ9ü(r\x000e©[[1i\x0016<òÍÍN<±XË´\x0014=ÃÞÂE?j6¢d4þ\x001båÙS¶"«ÍsÌß1Õv _OTÆËÓaHCëÞù­X¬_üÖ~RÒË»\x001f¾~ýüý8[¶6qHÂ \x000f°\x000eå*Ë{\x0008GF\x0003¾¼}öôõë\x0017o\x001f\x0006´- Õ\x0002zÏELîÚÖn\x0005ÒÍì=>ÄwØë\x000boá¼\x0016Î\x0019ÚMà³Âj=¾þð\x000eì\x0018\x001dx¿y«¢pü\x000fÿðòãîýÝÕëÝOßþÇ/\x001fÞÿõîãu¦V`\¤*WÕäåÅô¥é/Ý<¹½z}óôù«_\x0016Ög'b:\x0003b\x000bJ@ÈA\x00044M\x001c\x0003JåÏf*ê\x0008mù¬ÚUÜÖR¥\x001f?Fºq7cGG\x0000]\x000bè´\x0016kugñx\x001e¥R¾^öö
t#¡\x0005\x000cZ@¬
ÔÒ!M<(zéÐ??ð¥/©ùàÚÈ
t"\x001fE\x0002t\x0006çø n\x000b\x001fõk°¹a\x0016M#½¤>õ/â*Dp\x001b/C\x0019õÞ\x0007~¿z¹ûø·ÿú}÷å8`ëSøÒ\x0016^%³±ÎáÊ©WÁ\x0012\x0017øöêåÍ³Û_n^=-\x001ejñH
UN¨\x00145ê{\x0008í¡I>ÛòY%_(+JCt¢ï\x001ed¢¢\x000f³ös-ÓòkÍ@Ñn
"tWÇ|ègíç[>¯^~µ\x001a'¸P\x0005²ÛO¤<8ëQÁ\x0017Z¾ þ¾õ=.P~ÊêI\x000eªô\x0014\x001cL\x0011\x0014|±åj>mY\x001a\x000b}UwrÒ\x0002¾t°Îñ¥/©ùB\x0015¦5X÷\x0013é®áàPT\x0005_nù²výíGû+­:\x001aÃ1Ç×<¢{6Z\x0003Ì%e\x0006\x0004\x0016¶^fò2ßáÙß
¾>|¨ãRãË	;©lUz
8é_ \x001f 
 >{nô®ÊâCUH\x000eg¿o\x0017?@\x001b@H¸<qÕ\x0001Ú 
¨)äÙ\x000fÜ\x0005\x0010ÐF\x0010\cødeà\x0001Ô$æ«O\x0002v\x0011\x0004´!$\x0001Ö.µä°8è:Óizt\x0011\x0004´!ÄÇ¥uPC0ÚË¹.6\x0014ôÚ±\x00051<u\x0010M9\x000ct1\x0004´AÄ{$Ëç*ah²\¾ÓÿIÀ.6¤ä$Ë·	ä çEåÖ\x001c&½ vQ\x0004µQDxiË½d\x0008àeÜ®w\x0018û4_í¦ËÖåi\x0004\x001e¸ApòVððU\x0002°s¨N¤m¨kÐE\x001eù$Þ*d6QÅÎÍ ÖÍÄstÉØz¯Ül¦Ý.Fí.¦7H~?ð¤¶ÂB·Rüøä\x001a´Ý&±ÚMRr\x0001©8*áCÄÚè{»i*Ò\x0001ÄÞQÓÏ\x0003é4g\x000b%^Ë*<
Ûj`æ\x0010Ó\x0006QñÚ\x0008$èêE~>|%­ÙÉÍSîºwJF_%*¼\x0015Ur,ÿ¥¦òÇw\x001bÄwÃ\x0007wo|Á/[G¾´¾iä\x0004«÷ÚÔ\x001a¤¶$9¢_|¶LÁþz\x0008±ÿÒú\x000fö¢Ö%àã\x0008R¨õ´×Þ|é ýÒ1\x0004i\x0016ðÔK+\x0007\x0000	,ÐÏn\x001fñÛ]qÆê»é7Ê4Ûûv%\x0000ò¸,\x0007µr>p¹Ûl»Çv[X>÷nó¹K ùFÄ['JcÖÕTlÓÜ7dÇß6vüíÑÙ1uÕ$ë¤ßè8Sªýü6É¤(öýÇaòlº©ËY.ØÕ¡\x001cZìþÉpH\x000cõ\x0012â¬£ì½:Ü ·2òG=\x0013kuiúé%\x0007L\x0019cÉzø¾^.Ä[z\x001fëçwÏûÍîQÆÅ@\x0017M<T3\x0018ß \x000f·1ß¸d,¸E2öåÏ¿ß}Úý¶T4üã÷Ýñ	®)\x0001¤*\x0016RÇ%-«
M=ÞËW/~¹}~óãRÕðooN\x000epÝÔ4\x0010\x001e*ñÃñ¬ÁI7Ú,fk¤§ÉõÒq\x0003t¶¥³J:*òj¼U\x0008\x0018Ó¾M­/\x0003\x001c s-ÓÒei¢³6ÊÙT;"\x0003Ì~YßÒy%]¨ÊöÔ}k\x0006|Õ/\x000cnÖxÐJ³ÓÎØ=µÒfãÒ= <&\x0017²_IúêåçOßNð\x00002\x0008\x0005\x0003\x0017\x0006"5±I»?ðÞ]Ø~%\x0015ê«/¿y\x0010[BT\x0013òé«Ö»öhä­'\x0018\x000fÓx¶Å³j<ªb\x0003Òe1OÉ­\x0015K¹ì,¢k\x0011þ\x001bk!\x000cü\x001e_v³,A°\x0007JB¾\x0005ôjÀèyÐ0jØÕ\x0003FW¥MßÛ|ðH%oØTMà«\x001eúÝÕÇÝÕOl÷áÓÝ	:ÜWºSMM@QöÛ×ÔÜ/¥\x0011ïW?\x0015²§ÏoO\x0014\x0013MÕ\x0014\x0001¢\x0016{+VéAg÷JÃ÷5\x0012¶\x0005´ZÀuvÖZO[çbf¿\x0017ë6 kùÜ\x0000_Í_°j_ûÚÄî\x000e¨Î(\x0001}\x000bèÕK0ËÌ;ëä\x0008ÙWÉÓ¡\x0005\x000c\x0003\x0016ä\x0019$¶ÆËç=$Ù¤-\TÃ';#]Áí\x0011î«³(ñRÔ\x001f7IA\x0008©Éäß÷gOóå/«ÍWßPa<T	û N\x001b°)Õ'\x0007mÔ\x0016Dyñ¦¢B>Âe÷e£÷+½{Âñ\x0003úø¡\x000e ë,àÕ½H\x0000Î¡Ö\x0014ú\x0003úJûuî\x0019Ôþ\x0012\x0004©\x001a
òc­\x000b> ­ v/íáêb¤Kñ´\x0011ZdZOÞ×ÍÛ\x0003\x0002jÎV¹há¬ÂEçsF\x0005²PÏLÙÜZ9pï6\x0019wÑÜþþáãÝÕ«Ï\x000fL\x001c\x0017ñW+zïåØYÇ{ø{ý«·¿<}v{õêÅ©8B-\x0015*¨\x0012éf¥\x001aàø\x000cê\x0016¹¯ó«Á²-Õ\x0018ÞeE6\x0011äKZ+ó«(!\x0001s-Óík¸ÊG«s¡êüò§À|\x000bæ5`å¼[µ;#\x0015,\x0016½\x001eêÔ\x000c-WÐpP5wèÅS¢ö\x0013xîK;iÀb\x000b\x00165`ÅCHE¹Â°¦6OÙû
4`©\x0005K*y\x0011´9ª
R\x0017Í}p
XnÁ²\x0002,P\x0008_Z'\x0005ð\x0018÷Âf\x0006¬ÉE¼«¹ÈÙ_\x0000\x000b\x0019ÖÅ_åàf¼+ô>_åôWYê\x0005Ìz,ÜïÕu~\x001f4?\x0002VºPoð(¦\x000bYþÐ¹~Pùþb3~v\x0011k\x001dtªwîñ¾^²¬óý rþPo]ò®aíMáÞyK\x0003Öù~P9ÿb2~ª¶<¦(dù~ª¬óþ rÿ%ï¶Rû\x0010ä\x0000½\x000fKÉLe\x0018Ð¹PùS}/ßÕK$+ì\x00040µ\x0001:ÿ\x000fª\x0000@\x000fxµ¢ÅH`rR÷14`ÿ\x0007M\x0000 IÉR	®l_k3ãg±ó³¨ó³±>Ë:#v1 x²aÆÏbçÍPåÍ(41{~kR\x001d\x000c3`¦«\x0007Y3
9ÝG¼Ï:¨icu\x001cî¾*­\x0006\x000föoÙëyéÝ#90u5\x000b«Ýä´y\x001e\22
\x000c%{y?\x001eçÞÝê@×4¹ûµZê|¶\üGªOËGsM¹ýTho_æÖªa\x000bX¯d|\x001cÒÖÁÄá þYli;5þÁáç»÷\x001fþöÿ}9uPÜÇP\x0013*\x0010+G:\x0011^Áû1a½@øùÙÍ§·¯N] ¤­¸I2ýÃõAiÏPðê Ü?ämð\·¥íÀÕdúÇóØRír/G\x0005ÎÂ£
ÕzxÏh­çZB§&^ZÄH\x0013ëW½®<ò^s>`l\x0001£\x001a&X±¬\x000e\x0018yvÝë\x001c&Ò\x0002¦\x00160©\x0001ssg\x001eÅ/ÇX/,\x000f\x0006R\x0002æ\x00160k\x0001Á$é¢$_~WO®j\\x001fX§\x0003lÎ©ÉlîÌÏ#66úÄ|\x001aS\x001dShï+Nj	{/¨vP"ZÕIT¤ÅeE²Ý}Õ8-bç\x0006Aí\x0007\x0001,uÈ:ä\x0011èK\x0018[\x0011\x001fÚÊ']!t®\x0010Ô¾p)?eÄÉT	/w`4r£´q8\x001a5VjPH§oÁZ$s_Ûü\x001c#îÌ¦¶íÆ¬µmÏ>ûðõëÝïw¾]}¼ûzõëýtwb\x0008AIY\x0012Uz/².åTûiçP&ÉÛÔ\x0017}?{ñæéë×·¿Ü>sõìöõÕ¯O~~{|lB\x0005Å\x0016\x0014\x001f1¨mAí\x0008(
$+(=9-\x000bÓYqÞF<óýî·Ý×o_sºÓp:iÒ*1Ç^[·\x001a}½
ý]ã(§o9ý\x0008g°ëa}ÝüÙ³`úþ	~\x00143´a\x0004³Å((úH%Ô\x0004\x0001½=c\x000b\x001aÖgbéÍ­\x0019\x001eSÖ'W\x0005{»\x0019í5
ZÐ4\x0004*ÒóÉÍ/\x0016|töå¬zÎNzpÇç\x00164BæZÍ¥f.²Ecp\x000c
p	Ö´huöæñ:QèÃÒ#KÐ¹'\x0018òO'ÒnãÃÐÎÿ;v\x001b
vÔß\x0014»uxbàP^òÇ­\x0014ú\x000b" {±Ve°$Íoî¾|Ù\x0015ì\x0013\x0017XÙ/zÐ$ÜB\x001dÜó%'#ºÀj)÷2%i~sûêÕMa~\x0018\x0012[H\x001cD~\x000f*ÀO¤ÈÏæ`\x0012Ò¶v\x0000²ä!ë\x0010PNkÒ\x0018ä£B(6ª(]Ké\x0006(3òA3\x0004ºá2s\x001føea¾9é[L¯Æ\n.×jøàË\x0017gáÈY¶,½TJÊÐR\x0001c\x0006Çmùå'\x0010ÅRndð°B\x00123¶qÀ.ò£eðï\x0008eÈÍ\x0011.±ÅSËFv\x000fpeA î9nýZ®\x0015x]¦ïJÌÜbæ\x0001Sz¹ï§-³¿\x0013F6f8Ü¨£lt¹È©\x0001L\x0003uûäú²\x001f\x0002×iØá`³\x000f>úèSÂxÍ\x000bÓUí@07£o\x00071»ð\x0003úøC7Hû
\x0014¯\x0013»ö²ud\x000fù\x000bì!è|;è{Ùèy½-NsÜåT¼f:Ø\x001b­Äì¼&èÝf9\x0008G~¶(Ý¬ÁzùæeÏ?\x0002½C*KÓñË@ Ù\x001f\x001bäæ]içC\x0010s·ìHH/±\x0012\x001cG¡È©&Òë²D¡t	\x000fo»&é%Gj{¤Ï¶+HiCqôR@\x0010R\x0014?\x000fæ\x0012°m·å\x0018ï\x00062%Ëêr¡ØU@½´ÓHp\x0001ßdr\x000fõ e¥F¾\x0010	ªÙyÛ'é¡ÚH¶ß?|ÿ?:\x00015[}sãN½¯W?}¼ûþåÄÁ­$"Uë\x000en,*¸¼T.|\x0007Æ}þXÎk?=»}ûêÔ@ã­¬¹ñMÞY\^jâè±HúCmáãÃ\x0017¢
vìº«Ù\x0016ÌjÀ(óL&D	âÁî\x000b\x0007Â+,æZ0w>Xñ4 ½dô2$\x0016\x000b\x0019\x0004ìÐËäù`¾\x0005ó*°Ú
\x0000¶¤=|l\x0010E\x000bçâýB\x001a°Ð\x0005
Xù~YÖ~-n\x000fÉÖO9Å\x0015[®¨á2Nú*é!%@\x0016Í\x0000æº?Z\x0003Z°¤\x0001³FÔ\x0015¡$	, \x0019²\x0014Ý»x`\x0000\x0002,·`ùñ,±¶¶½í³;¬\x001cç¹\x001d¾¥GAº(Ë·<Evä[¼k_\x0006G\x001evßtu¦\x0015³Q\x0011­e'+Vó\x001a\x0015Î¿¯n$¼}ïÚYûÀ@\x0013Õ8ÉID\x001fÅ\x001dì\x0000|\x000f
YH÷u>Î³Ý¿þpBV&\x0001]}qOÙ\x0006ÇmD¹û
þþ\x0014È\x001fßþë§§$e\x0018\x000b[,T`Å,S\x0016i

V\x001d\x000e\x0014-åZ,§±\x0016ÔiUuìnÁªÝ>Í`\x0016+h°êsê.5b­P±îûØó©RK4T©\x0016X.jÊ\x000b\x0014© r]LºõO[ªüX\x0016|;Ü\x001cÛc\x000fse¨í%frA`JU@É\x001e\x001cUuöÒêçìaÛÓzÕìÞj<:¤AÝ\x001f\x001c;ö\x0010\ù\x000b7\x0019¿Û¼<Û}½zòùûï»O\x001f>}>õhCò\x0008ëcH9ç'\x0016sPgV\x0001\x0015\x001f9¼¾zòâí/7Ï>q*\x0012¸Í\x0008Áâ\x0018¬Y$LWXCak\x0005©Õ\x0000<,Þ­µ-¬\x001dÍUír±,Ï³²(°6\x001d½MÑÁú\x0016Ö\x000fÁZÊKVV\x000b<®Ò\x0013M\x0012ÃÚ\x000b±5\x000c.ÙÀ¯NÅ°À(\x000eB\x00021,\x001c½óÓÁÆ\x00166\x000e\x001a6ÆQZ¥\x0006]ÉüÔ\x001cÇ 'M-i\x001a3k\x0008×Ññ\x001a@.%tù$Dkàè5\x000e6·°yÌ¬¡6oÄù
×YEí6\x001d¿FWÁ6i¿Û>L(L¥ë*®³Ø\x0015r¼	Ç_£t¨}8\x0018\x00076Ô\x001b\x001835gÁpÙñ«J\x001dk\x0017
`0\x001cd'çªD
wë"@d¡\x000fpXÚQOÛ\x0003\x0018\x0007´dEÔÓ[>hµõ\x0017Ú_M{¬Û>ª(ü\x0016Jaq2ï\x0004\x001dòJq]Z	]ôáðµ\x001aªãxªeð\x001chÍG/u¨]ð±èEõL\x001b\x001b
­Ìà,îàB«^0\x0018¾ \x001cv\x0004+î\x0000e /ÿËD0è"\x00180ËB_Ñ!\x001f}\x001dúÌñË¸Ã:òzÔ.~Á`\x00003UØ(Ð$)¦­Ör¸ÌÅ.~á`üÊ±
·DÑI*+\x0015ç\x0006\x000fÏÕÓÓv!\x000c\x0007C\x0018$\x0019¢Xü+_\x0019Ñ\x0015Ubï.\x0013\x0016°?Ò\x000c\x0006±ff\ÜLä°Î²ÏùØØ[õf/¥¼jÞ-Ü,ò9¹·¹º\x001böxÑ\x0016w×ãîÆ\x0016a\x0001ÏDù-Ç\x0006'ÓàÝZèqa\x000c\x0017ëÎ\x0014-\x000bÆ9\x0004+¼Á\(¥ÉM_÷êÆÞ.\x0007'9\x0018^'±¯¤	pxÎÍ}{Þ1\L ,S!Ç30rÐÍ\x0017JÆ©v _¾cæ¥'\x00166/ÉëKüMr(Ç\x001fºq¢{GXcEÿØ­X\x0013IÞmIo"Ilr83ù2Øø~ÓùA\x001fAú×ldª¼äð&u/~\x0019¢r!Þw=ï£Þs7>-\x000fÚ\x0006üÈØ[`ØrXw5 \x001f¯+9\x000bxgl!zCóx({øðíîêåîë·»ï§f\x0004PEø:-Ð.óRm-Ø÷l?yúæöêåÍë7·o_ÒV&lð|¦rú^ÛOC*'G¾×¦9fÂÍ
\x0015m¡ìùPÅ:\²VåäµðAÄF#°k¡Ü¹P©l+öé!ãJ­üÌü2\x0001y³¼TP¾ò
(S¡JªøÝ²¥|d\x001c*´PA\x0001åXV¤X
H'kd¹¨\x0000ÒÌB-TT¬©À\x0007â²¦¼\x0007\x001a·®)Ó¿ë R\x000bÎ
"\x0010h '+8í\x000b\x000c\x0011ÃÄîË-TV¸)»w	uÜJ¨\x001déh77H\x001a¨¦ùÏòEçT\x0018W\x0005ú\x0005\x0005À}Nvb÷AïÐ5\x001e=p/R <º¶Ïð\x001b*ºþÝí,¨b"»­\x0019°\x0014e~øüýãÝ¿ï¾üvõçÏ\x001f?|þvõäû\x000f'\x000b\x0002]­üÏÑ,tù\x000føCZìoU~xñöÙmùéÇ«?¿xöôÅ«'o_==U¿È ¶\x0005µ# IÊ\x0015P¹Z«wUÎn\x0006¶rºÓé9*Â\x0019÷U"Ù
hÌ\x001b\x0005õ-¨\x001f1hI!Óð\	 ":e]_n3
\x001aZÐ0bQHÜ¦]d\`DWÂnF[rÆ3\x000eqz~\x0008
Ô&µ«Ï\x001aåË÷ýH£ ©\x0005M# ¤ÔÁ_\x001eöK4É r2½Es\x000b\x0007A³8'\x0014ª\x0002Z-j.±éÛ\x000f»Ä\x001b=iIó\x001a\x000fs¨óW£«ß\x001eñ\x0012»\x001ez?àði<¨$^æ{¯ Fn{-¤K|û¦ë@q\x0004\x001eS\x001d|_K\x0015\x0004ÎâH/òñ»È\x0004\x0003¡©||ÇSc\x000b©ºE(\x0015R{\x0018
]là\x0004å¸\x001ecõù¼ócMî2\x001f¿M0\x0010
(Ê{jÉ\x001dªh\x0008]ÚÍÝã(h\x0017`$8AXBÒbQ»vS%)©Â|Ö
=\T» 	\x001bß\x0014F¼\x0013ÐÀõ*×@\x0015AN :ó6Ä4mN 5ÁuèËÓt\x00086h®]I­¿@lr\x000eï\x001di\x001eñP¤½Æ3'urÚ)Ê*Mñ"9iÛNµ¤ù»l\x001eÑ#/\x0001#÷J>ÈÙÈËø¨¾Omõ¨ô\x0001§\x001aE¸»äT\x000e´:U+\x0007\x00179ø-°\x001fä¥ëeY· \x0013¥CpÕ·ÆpìoË\x0006y©\x0010ó\x0000\x001aXÉ}k WU'3\x0016¿=¡z+Uí¯w\x001f>}û\x001f¿|xÿ×»'\x0010\x0011×èÀ#d\x0002K\x001d'r öõÍÓço®~yúäO·Ï\x001efÃ
ulÖK%yR\x0006´\x001f÷÷Uqul¶e³Ën®esJ¶Àñr\x0019Ãg\x0002\x001bNÐÌ½2÷\x000eíH¬ôÛTÎÛ*³x.³{-Òåen\x0001ó¦Öº{Eåç£\x0019×÷oÙ¤xû¿ý«Ú¸Ù©6.;õó÷oKiùËïÿzwbðcô)ÐHÔ¥1&d1\x001d8¹CòfÓõâí¥¸üåÛoO¥d0lÁP\x0001iÉD@K\x000fKÐ£¢ÜÕf½(Ë¶\Vk0n\æÚäû\x0006\x0002s-S¥%£¡!q¸®1u¢ßHV+Á|\x000bæ5`>IÅb9LQ\x000b3¹\x0018÷í1S\x0016K-XÒ%'=kÅ8¯2yo±\x0019®Üre\x0005W4¹\x000eÃ4\x000bRiºpa\x0001k®LÈY\x0018ÅBäûðU\x000fxõ\x0016.ícÀ¦©HIÖ»1\x001f\x000b`ù\x0012'Rxç÷\x0003ÜÓá¼ß\x000c\x0010Uu~\x000c4,Q\x0007õ~´\x001fßÒ»Ú\x0016Oñ	²£íçBÖy2Ð¹²t
ìÉêd\x0005p²ü½Ùtº*MÖy2P¹2\x0000çË4I\x001eFµý\x00106²ÓJ²ÎÆyR"]Mæ3×ý  Lqr\x0019N}Ë\x0007ÁB\x0007\x00164>#Ê\x0005vÉi¥\x0001m\x000c\x0012.ÑÌÄñ}\x0015ðB\x00165&óV\x0002¹Ù$\x0002#S¨Bf¬sÿ ñÿd³ S¯y6F8\x001eÌÃè¼?hÜ¿£Ó³\x0018L\x001a°¬ZéóF3\x0013È±s²¨J\x0016\x001dÊ¾4ÞÛBE°Âæ8c3ìE¥Rm9Ò¹,:\x0007ÖJ×¾~façdQådmm¥&±\x001aÉÒK\x0012X3dE¥\x001alnÄèDÁÌ½ò9Î\x0004sì¼,ª¼¬ÍÕePÀj\x001aÅfõ"q
¬ó²¨ñ²¤\x0012%\x001e\x0003½<\x0013¢ô¹í<\x001d%XçdQåd-JMGÎõ[$Õ/Tc?\x0001ÖùXÔøX\x0012ôäQt¾äì§\x0004£tó%vn\x00165nÖã2¸L|ùib½¤´SÇ\x0012ÛeÙVeôótAðõÀDR\x000c\x001c\x00006]Z².\x0000XM\x0000p!°&{ÈËrh2"]-Y\x0017\x0000¬&\x0000\x0004S§X52b\x001e\x0014Þ,Rõ÷\x0005ª\x0000@cèØÿ
`ÙIñ£â\x0004Xçÿ­ÆÿûP\x001c\x0005\x000c@>¡j°ºíÈ7%Yçf­ÆÍúb(vÿ¹\x0001äm®øÿ)uÞÌª¼\x0019 \x000cT+®K!±Ì³3\®ó\x0018Nã1|Éüàbkù
\x0018#\x00013Î\ç0ÊaÐ#.¶«@ ÛZ\x0000i¦%®s\x0018Nã0h\x0006õÚ\x0014"é\x0015.\x000e\x0003Ræ\x0008WÒí$Ãu\x000eÃi\x001cM2\3PÏìÚÚ	ÙÐ#ltµdý
£ÆcXàl3:¤øÕfIföIe]0:MÂÅaÔr¥Ù¤Ij·§l×¹2§re¨÷w]Æè4\x0019£5Fáq\x001c0!Õá²dÉ	²Ð9³ sf É¢ï2Fúñ|2ã\x001dÖ\x0005_NLë¹\x0004¼Ô\x0003Û\~;\x0006ú{)úYáiIÁxý%\x0006pj\x00069\x001b\x0019H\x0010óT4o\x001aç8m|§q¶Èsä\x0002U3\¢aÔ\\x0007:u9Õ\x0016Y¬\x0017Ç»á\x0007\x001d¼ÿ3ã:Ýî6v»Ó°¡´h\x0015ß*/\x0014à$|º8\x0008Á_~Û°ý¦¹¦
|¯\x001d2z)4 ] ÌÔ+\x0005ìûù£¾×ø\x0010'OÕ\x0018ôÍ,­XJ§àÞmà\x0014»Á§,\x000fbH å	1\x000b\ÌS×h®\x0015Käk¡E-ñì47Ö¹ÁôÂ÷/è$Î{RCZÝú\x001a¹\x0017õ³ýI	\x0011\_\x001aç[â/mMÞ¦Îî[@@\x001d 9\x0015Ñ\x001c.Æ´ ^\x0005«WùÄn³þjýaÆ}Wã\x001fu,ôÒ'>\x0005·ÛÀ)Ü1½IÇ\x001buYs	P»¦|\x001eÂöÓ"è>-Í#då\x0002ºÐ]µLJên
fvãZ¬Îµü¡ë\x000eì&ÒZU¤-\x0003~ÖC#Ýp&×Pëü[±aU\x0011¦øÅZRÇép®¡pÊpP\x000bªP»ùªxÿ£N¦(»Ý4û5Õi\x000f4lj½E*§ÕzólN\x001aîHåUµÚÝÆjªä©|G~\x0011EV)VKuFúI«\x001dK6\x0004\x0006!,\x0016\x001a½ùôÛ¿ý×Õ/\x0005£üðû¿ºéx³IO²÷e³Ú\x000cüf\x001b\x0000Ý=Öç?¾º½ú¥üªüù§Ç\x0003¯°ûg\x0005\x0016ãc=l|Ì°\x0018°¥\x001f\x001f%ìf´±áÑÆ,>ûä¯»ow»ïÇ\x0001\x0013%©ì~¨\x0014«\x001er¨\x0015,.\x001f]~ò§7·7o\x001f\x0006³-ÕE¬2Õ\x0018éh¾Õù\x001dÁÛCº¸g¹\x0016Ì©ÀªÒEw±\x0016/¦CÐgù\x0016Ì?¢O\x0019[°¨\x0000³6~
s\x000bVýå´)-èÁxëÍä\ÃsÏ§"Yc®Û
¸\x0006^kjÏUHaæ3¶JëøÙó¿#ékÊ\x0002s2¹¨dRUF\x001bN2\x0017òÚeÊ`¦N»\x000fÈµ+å3¦j07å)Z%\x0019³yo²ì÷âñr¨µ|=¿,±ù~Ä=ýJ°oþýîÓ2àêÇÝÇÏ§7eª\x0005?åD!ÞBZÜ¦\x0012éæ×ÛçËx«\x001fo½8\x000c[2Ô¹ZðC6ãÿ(¶WiSÙÌªÈa¬p\x001dJjÝl?o[MåZ*§£\x0011]Ñ \x0017µ¤r×&HSh¾Eó*´$w×\x0005
ª5"\x0004dcß¯F\x000b-ZP¡h)ímI
1rNÌÏ­ÿØEÑ²TUÑ<\x0007\x0000À½Ñæ¾gjÑÎh¢\x0008\x001eÊÊçRl»Ô\x0003sùÊ¤×È-ZÖ Qs\x0010\x0017\x0016¿M]jµShÛ²ªEkgè¬\x0003æ5l{f\x0004à\x0017¶¥Õîä)³A\x001f\x0006TqÀ\x0002Ô8°(XØjß´³Z\x0017\x0006@\x0015\x0007H?P\x001a{¼C°^\x0017\x000bsl] \x0000U$°ËÓ[Õ\x001a°v¤\x0000Sl]8\x0000U< É:a\x000b$ÂÂECÖnTÔl]<\x0000U@p §åÆk}3· z×\x000eó\@. *"Ð¥°9¼öqe³u½¿h­\x000b	 	ªrU`á½\x0000©ªü¥8~@\x0017\x0013@\x0015\x0014hò@Ëeê¡}Z·iBëb\x0002¨³ut-I¦Êr7¯\x0012Î¦<\x0008v;\x0001U;ÁÊ×úâ@ëb³®>PýÇ8\x001al\x0016nµÙ:óa¹^]_ºJ Àªù\x0012g>iÙh]
tîÍ\x0018*h<\x001cÙõ¢¯ý\x00008Û~*áÉ¹,iÑ'\	³\x0008Ñì«"lvS'\x0018ðý`ºÅ	Óo\x001e\x001fn%×èúNóÙD '%\x0016{,áu_Y>·qÁo¿1xåGv&ÒMÖh}ù¾«\x0005ÅÖôÏú®¹uXºÝcÊO§%ÆûMGÏ<!\x0014\x001cqÀÛú\x001bÀ{¿Á{¯Ê j]·¡\x0011\x0013Ë#N*s\x00036\x0003tÃ9\x0019oB\x0013ä£|Z)Ïé%Î\x0006ÜßÆ¹X¥oùÃ×Ý|\«û¸%â\x000e\x001cªkQ\x001bÎúÉS\x0005üå_6\x001f÷_\x001eñ×MÆ»Sí\x000cwmå$XÁFWÉ]Óiã\x001dyxÜ_f\x0002ÝF¶\x0013)^Þ}ù´ûþÿ~8!w\x0011³±2©Þù,\x0017ÞsúnÓfêð^©ûåí«ç7oÿ§§$/\x0018\x0011[DT"&V&[J9ÑTµçh\x00191\x001f\x001dS¦@´-¢ÕZ±(8w	ÔwÃýÙN
lö@»\x0002ÑµNH\x0001kràHÓ\x001bEsÂ1b>6:Kè[D¯^%¨±`¦§\x0002"ÅåÄ6\x0003\x001cI¨@\x000c-bP#¢çû²à!p\x0006XèX\x0011ó<bl\x0011£\x001a4\x00152oÄg$ô2\x001eµl|D{_ZÄ¤F²ñBy\x0000\x000eúìeCÛ\x000b|çÜ\x0012f5¡·²¡=
C[\x0018\x0000êwÞÈÞ\x000f 6â\x001eävq}î\x000c.W	\x0000¢lçi\x0008}dÑ\x0016+ÃúíÌ\x000fØÅ¡ï·óI&{Æ¡\x000fº¸\x0002ÚÀR>²\x0017-9jäwü½0¹ée\x0008]\\x0001u`)§_®?^\x0002\x000b÷JúòÉk`yÐ\x000f2v\x0005Ô%Sß7\x0007¿\x0012\x0007«Û\x0006	~>ÌïÎmÞo\8§9\x000e¥LÚ»$v<6@ålÄÜ1ØÑ¬%×vEï«×>2cë\> ÀÔmç¬_TÐ¸.FïYÍÚr±/5ÔL"öE\x0003k\x001e¶Óf9!ó\x0011¹d9N:\x001dD]®lé\x000b¸EÓC¯¦¥Ì.TÊìD(6\x0018[÷±qI
[öÕÓËÙ ît=éL°ÞxSÔ\x0001»,ùNrÇ¦î*\x000c\x001b¢Þ \x0018ä¢¿ýì§Å f>çÙ`ê)ËAPd¡\x001dÍúá¼\x0007\x00052^`\x0007¹\x001eÒéMi4§Qæc@¢¶4Îù-ÔNñZO
jÊrYØ\x0007o¡© aÅBÚùuéòþ52¾S\x001b\x0013dV\x0013YÄ\x0014ähiÞ\x0019m¾7\x000c|pã¥A\x000er¤Ù/Ë<b´³ñVÇ®µdq4|dpÑKºËò7Å­?¼½\x000fge9÷(å\x0017tòô÷Û}ýJ;_¯~¾û²ûôáûïÇ\x0007e4$u­\x000bÎÓ\x000bo\x001d\\x0003Ðé«\x0001|úËË×¯éçõÕÏ·¯n?}ûËélB-%\x000ePÒ4¨e×dª¨È+¥h\x0011S§½\x0000¥m)í\x0000%$ ¸\x001a3ðË)\x0002QÔ<v	cº\x0016Ó|rËÏ}\x0006Z­% åó¾¡ö|\x0001Lßbú\x0001Lk94&ÒÎáé}¥ÄK|óÐR\x0011JÇU+DÖKÉÏáåcÀ\x00046w¥tØ`~¿zùùû§o\x000f(j\x0016\x0017ê\x001d8OòqÙÊ-®;²}Þ^½|ñöùÓý=is
Y\x0000­\x0016(%põÏy·\x00169¼"\x0015®\x0005tZ@aÑP\x0003\x0012gNjË)çðÎV\x0000ú\x0016Ðk\x0001Í"a¶\x0000\x0006WÕ,¡Ê9A¯ç7\x0002\x0018ZÀ ¶`®#&ÊYù\¬\x0006ì§^ðÅ/*ùbõ\x000bgÇR-h£´\x0018f\x0001S\x000b´Ñ,\x001c
?áMlc}Cuvö\x000b·¢½i¹×S\x0012Êüj0JV@\x0011û(ÿ\x0005ô\x001d ×\x0002&pµÅÑ@}ì@\x0019\x0017E/½S¾0öFmÄ\x0010x¾kYuF¡
õ3?Î®ÃM{râ\x0003¶Î¾p9.¨®Zh.#ã74åx\x001fôH-»\x0004½\x001fwïgËÿçýï?}þv÷~øõÃÇ§\x0007Æx*î[\x0006d.5&\x000b"4\x0010¡³èËg7O7ÌgWzñæö\x0019ýñ×§Ïê~c`lq\x0018¸¬M3DzoX@Ù^Vûb\x0002Ø¶Àv\x001cXÚé\x000b0bw9ùHïpìEÎ']\x000bìiN*[Øb!T;6:~\x0013¼¾åõãKç\x0016Ü w\x0006ÉJñ æRö
-o\x0018çMü>\x0011é|i\x0004ØïÒãc\x000b\x001cÇA*Ð¼Ô'n\x001f\x001fü¥VDjÓ00
SjaÖoNRÇ_\x000c|!\x0006q\x001fá\x0002¹ÞU,Çí½°T,¨g\x0011\x001fé+\q]ëÆq½#ÕU>Ç<dñhbàMá n{5»ÆÝ0°Ìé]ê\x001cÛW&âùÍEòÀ\x0000³	Ë`¼Ll*Ï>ÿÏ'\x0008i\x000c´\x0005ó^äB6(\x00116]1¯ÖJ¢g/ÞþÓ¡°ÂG\x0002åZ(w>T
Rñg£åã°]W¨|xÔùP¡

¨Xûàiâ8ý\x001b+}Ê\x0019& R\x000b\x0014ÏÕY!%æ\x0018+½sb©÷óÏjÇ¾ú\x0010ýÿæEårGE?\x0015ù¹;Ú\x0014¯³PqÖ\x0013Mºßü0Ý\x0016óÙÜu&½zù_þö_þö_wÇïÑè
ÈÄKµõlæÅÿ;\æÿúêå?¿º}~{{ò\x0016m[Îgs×¤|&$uGðc|Äª\x0019\x001fä5åÜ{¸Y\x0003i[H;\x0000	V\x0004$iÈ\x000f÷\x0007@D\x001a3\x001e.)Õ@º\x0016Ò
@¦*Ö\x0018ËùLJ#¨ï\x0003úyKú\x0016Ò\x000f@ÃÌzL\x0008åX\x001f²¨·¹%C\x000b\x0019Ô©¬jiÇ¾>t ©+Ø#Í\x001aÈØBÆ\x0001HûÓP±× 3Úý^Ko~w§\x00162
@-Í%1Ô/ÈÞv\x0017ØÛ¹EÌ#vîÝ°\XÖ\x0011òV §¿5ô\ïÊ\x0013u)pÙsqëR$\x0012ÑÉ¶9Öþ¬¡ì¼$èÝd21Ëâ×åÍ!ÖÆ\x0000:XMSv\x001e\x0008ô.(ª¤KlË(WpL·@CÙ¹ \x0018ðA\x0012_ZT¶w4¬v7º#må\x001aÊn{ÃÀþ¶àyâK ©|Ûòìp7%\x0016\x0012Íã4%öy>\x0011JÎ$\x001124\x000bd-ÔV}azï`·Ãq`[Ø÷ÖÐ$nþÜ2¿8úyÆÎãC§¡­"*_¢·åÞQ+y\x0010â\x0011\x0019\x0005¥í<º\x001dðè@#YDú^³Ê)Õ\x0007é^>Ò>ª¡ìóÞï%ØxVOÀJmå*G\x0008ôG\x00104]&d\x0007R!:eÇ±¶ÏcmÅõG:¾4Ýº´\x0003ë\x000e\x000be\x0014ùÞ²¡¼ìðl\x000f·\x001dª¾x«	º|ó\x001et_\x001fM%çÏÚjÏÿ\x00052ËÍT¤ªÏ¸¤(½²`¸ð\x0006Kü©gÜ#¦ª\x0005ºeµq\x0004víLtÕ{FIÆ½\x0014ÿ9½\x0002À÷+\x0000üÀ
0ÑU\x0017Jã¶\x00139¹\x001c\x000e·f«Î»=¨ÓsF*	|.·Ü\x0013¤¼\x0000 ÍC¦VÕ@ï\x0006r÷(1³¤Âr
\x0013E¹¨üm§³\x000f\x0013{Ì¨Ç\\x001a`XÀ;&¬MDFô±Á_À±ÿæqäSëK½åàÇü\x0018ë-Çô/ßzÌoC÷Z|e ÊãL02\x000e\x0005²ç\x000c½9ÃÈV'-\x001c±g-ñ\x000eÉÕ[£#ýÈ:ônãôÛèïÅí¾ë·ûAmdEÔ²Ý½¼\x001aÅ:kò\x0012G%Ìw\x000b´üóÔ+4ÜçD¯\x000fÀr5\x001a¹ù8ìí#û=¦êãÑÊØ`S½1\x000cóÉÝ½lÄ\x000e¥#n
«û¥\x000cÒÍ³\x0004N?ÄYÛo&kG6t=³jÚë¨>D{X_G1ß3j\x001eKþ\x000esÙùïûÿ^¿óËv|±\x0014@n\x0012£\x0015Õ8p0ãòqû(÷ª?*/+«ðÚÈ[\x0015ÈÕûÒÂ¯éxyÙó5p¸}
Â®#á¿\x001fÍ¶hÛRêÓhQ\x0016_,\x001f°¶ç¡<F<Q<x\x000ekÑ¶EÔ§ÑhÊT%ãeòßñx\x0005ú9`¾\x0005Û\x0016O\x0006ó¢\x0019\x0017K¤Ä½>òÈ«¨ë÷\x001f"sfÓ S~Ñ¨üüe÷ýë×Ï_éáö§\x000fïÿzb³fz£½\x000eK:i¤d^6«/1oM'Ê\x001fý¡¬_Ý¼}ýúÅkzÆýéé?Ú²-.áR\x001f\x000c`ÅÅµ%¯´
l8Ô#z\x0000öpéÚÔ>zÃº\x0016×
\x001a¶ä\x0014
["¶aËZ\x0017/ìÛ\x0010&pC\x001b\x0006­KZnaÅ]Û\x001e\x0017ëf¾&^z.ZÜ4E\x00061;iÞ\x001a~·
>äCr\x0000\x0003¸ûÊÅ)Q^\x0019\x0014i\x0004nàÅ×ãÌ\x000bWA·\x0000$äãx98iÃ\x0014e³ÙCª\x0015j¿Ð(é­.w7ìÄÖ·Lúì\x001a,òÑ\x0014f÷mw$ì¦Dî\x0012Â>|:ÅeÒ]¯kJlxN³"ßäÝFÝì\x0015§p?\x0018öôù\x0019h¶E³*´\x001cx¬E,2õÔ1\x0005f§È\KæTd%ß]/\x0012$Ã²\x001f.Þl3q@æ[4¯AóF\x0006¬&+ÇhFz\x00104t\x0006-´hAeµ(b)ÅjH)Ófyw\x000e\x000eÚ)Ðb\x0016UV¥àuµZä¬sâ\x0008=IèO¡¥\x0016-©¬rÝ\x0005\x0011Ùç¹ýçÄ\x0003%w
°ÜeÍh*Ö¶\x0016`9O\x0005Ô²Ò\x000eÔ(¶/#!´:wæ<6ë®y¥E©²s\x001e¼«V;Piª@ëü-¨\x001c®'Y#¿²Q5û(þ\x0016ÍI×q¤\x001f6\x0002õ\x000bÊÛÒ<ëõ"/\x0001)É°Í\x0010ÅÛZ3µÒ s· ò·$_y\x000føTmYò6÷=;\x000b:[|\x001eØn\x001f\x0012Jhâ\x0013saS\x000e\x0017:\x000b*Kú ·(\x0015fÞ\x0007 û\x0000üýùK
¶}±Êw\x0018\x0015Â\x0016Y2Ü\x0015¤,l\x0007f|iØ:÷:÷Qø\\x001aÊv\x000b¦²¥)×}¾¦ó\x001f.³\x0012ÕÒbâd½Yq»\x0010ç¾içCPçCÊy\x0002%$\x0018¾\x0012t^4§ý.v>\x0004u>¤,2o«ßpå¬ì\x0005¹õÖù\x0010Ôùb7Ãë-\x0018:âlìS.v.\x0004u.$¸ëTwå/ê±z4÷E»
uIÛ\x001fíAº¤
UY§±ó¼Kã*ÅÈ\x00075fëÒ6ÔåmtJ\x0015m½Sq^fòû°]H°*$Ø.$X]HÈïùvp+Vó¶Úm­\x000b	V\x0017\x0012|Õ¹\x0001®\x0019ÍfI)·³µhý\x0011^\x0015\x0011\x0002
Q\x0015÷AQÍN¹6ÛE\x0004«\x0008å\x0014oÍóý\x000cIÆÈÙN3l]D°ª\x0010 Â\x0012Ñ\x001aåLÛ-\x001fwr¹u!ÁêBBÉäà·\x0016ÇÆoW\x0005lÎ³Ù. XU@\x0008\x0018ø¿\x0019\x001e£â\x0002ò\x0018Â6g³.\x001eXe<\x00101É\x0004\x0018Y\x001cÚî«Ùì\x001c[\x0017\x0010¬* \x0004\x001açÌÉ\x0007H²\x001bD~ÕSÕë\x000cë"SEFôÐL*»uAN®õSGR×Å\x0003§\x0007d\x0014Øç¢g='\x0017\x001c\x0008Z>Ô7ª`ëâSÅ`öixÙ\x0012\x0017[æÚ6bZl®\x000b\x0008N\x0017\x0010e\x0011¢\x0012Gy©3\x0007ø¹ïÙßèªA\x0000\x0011Ä^¾çú0V\x001c®¯\x001btîxàº`àtÁ s¸\x0012¨¨£P 
ð®\x000b\x0006N\x0015\x000cBÙ¡ü~\x0000u,Yñ¹¦ú\3Oº.\x001e8U<ø½G\x0017\x000e*\x001c\x0004tõb\x0006EÂÞ\x0002;£¥CÔ
¶.\x001c8U8T÷±²r.õl6+g\x0017{`8¶\x0002ÍwáÀ«ÂA°¬\x000fÚA9¾[V!ôvîVÆwáÀ«ÂA´å+òJ\x000bry\x001aI\x0017Zò\x001e¾\x0006^\x0017
a}V\x0000¼æý)ï\x0007á@j®Îsxç\x0008EªÊ:Ë5&#_3ä¹ÏÙíO¯ÛÅ]¬Z\x0002í\x001e\x00082ì¼°Ù©è\x001eºH\x0015Têõj¡ßS}Ñ?¬ûAõ=©\x001b5Vi\x0004äÚ¸ébÎ\x0012¥ÀÍ=nv\x0006\x001a_ÔÓo\x001eÏåk&8¾{4ß¶/å#\x000cýæ±\x0000º¦­·Óøl\x0005\x000e¹\x0006^4\x0005f¥fÊ`ÚÚ\x000fÒ~øú»÷ú\x0013Ó\x0004ÜXïà8\x000f©\x001eæ5}Y<_\x0011>.#\x0016?³A,~æq!:Üì\x0014Ôí\x0014ëYTÆ9+\x0016\:OLÝF{\x0016T\x001b°,=¨×%/À°V%¡*\x0015ñf\x000bXräÇä
ûqÇkUï\x000f.ì*¾úýÆW¿<Ö»ç©\x001f£ö÷Ü ×ºÁèáÚzæXGÈ\x0015G
rL§/Ç\x0014¹¤m±cZ\x001d?ÿ¶ÈýôùÓ·Ý§\x0013¢Ã~Ë®âÈÇU±ý¾
ìÕ·o\x0016\x0011³^<sóüæ°àÙ\x0016Ïêð¬ÜN»w\x001f÷\x0003¸^g\x0000ÏµxNi½è¥¯l\x0013©ov¦§\x0008ÓÖó-×ZÏó%{6Á®-"ÝJ.Ì\x001a/´tAi¼Tç¤ÓÈºm©Z#³íü4]jévcdîÏ4§w=ñÒ\x000cHÉaðÓ¾+gÊ®å\x0007:d¿¢¦¡XnÜ-\x000ePÄë½á:°\\x001b4x"êÊ-\x001f>>>ÛòÙÇÇçZ>÷øø|Ëç\x001f\x001f_hùo"Ã­\x0011T¸õÄI_ÏÓ|©åKÎ~µ%fõ/æñ\x0001v\x000e\x0006\x001e\x0001p½¦u\x0010b"9¢\x0005\x0011K¢Åý9û"B\x0008ý\x0003ß\x0001Æ÷»ßv_¿}9ÆHEz\x0011éUN·QH;q\x0007½æ}\x0012Çy£;\x0012\x0000h\x0003Ý
Å\x0014jØüðmÍoÞïÞØüÈ4§j=þ4GV\x0019y[\x000eÇÐw>>}³fÎ7On<½9þ+\x001b¶l¨c+)\x0002×´ÑLÙõØV\x0016 ?õ\x001587	g[8«£n"ÍR2\hä
u[ábßÇ¤s-ÓY.È\x0000úòU3Wó\x0014ËÅj¹^@\x000fç[8¯³\x001c4YD)Ô\x000eV\x0000Ö¿
´'æàB\x000b\x0017ûa\x000f<ëÆy##ÜL2K-[Ò\x0019ÎxV)M).C\x0017¶êÃ)¶\x001aÐV?btpXÛ9è«á²L3a3á[M×y\x0012Ð¸\x0012ZsÈý9ÉGîK(K\x000eä³úÉÍ
Ýf\x0005Ín%Wbù-7ÑÛ¼xúYqp³.Òjm|XªÝºÙò\x001fwWOþºû·»\x001fsÛ¯»§µ¡\x000cðHÆÊæÕò=\x001a\x001eâþìæêÉn^Þ>{¶á~½yv\x00066¶Ø8\x001dAä/rXæ]®ZQÒi[æG±mmg¬m%ü$×E96Kå#ÆpIkû\x0016ÛÏ`§úôY\x000eö<çÅçºH\x0002\x001cêB\x001eÅ\x000e-vø¿fÄ\x0016;N`ü\x00077äTC°`t\x0006#\x001e\x001b×;Zì4íâMæÄ}?DÜÃfÂÙ$vn±óÌ"IÜÓ³Ì,È­-Ý)\x0010Ã\x0005×ö^sañÛfÛ\x0005ªw!nÊ\x0007­ÌlB&\x0008xdîô\x0010w\x001fof\x0002NÇ¹òGC3ñØÞYVw<¤o1ÊÝ\x0005\x001c8Ö	Ú¾Ñú\x001cQÎ²ºÑ^ÔÜ]À\x0013E[fYéÀæ6YÌ}Xýd»80\x0013rÖvð;\x0006Aá\x0016s»Cê=£Ôç)×í¸¢»ìO/«$ÈpTUy9îÎ\x0007Â\x0013D~Òô¤\x0015DÉÔJ¤tù«\x001b;'\x0013N0:L(ÚxVçÍBÞ@¸ +ÁnmãÄÚNeO®Gù\x0018\x000b(øpY*yHõåÜÝêÆñÕ½ä~k\x001aXþ'ª+YìÌ!Ç^\x0012»[Ü8³¸3®Å\x0016¤ÎEô-sÊ
^ã¸ÌÑ[m\x0017$íDüû®\x0010Û\x001fo&¢Íß»Ûöÿ\x001dûu§\x0016Ï224\4 µ\x0016ËÚ¿Ø\x00126I÷òóø®´Uÿ\x0004yt³÷5äEJÞ\x0007.?OxA©ë.1¾®à¤æ\x001c©1òRä\x0008Ýñlùy"5|û°\D\x0000O\x0012s¼X<Â%¢ü®,í\x0013F®O\x00187\x001fïþõË\x0011¢e+f\x000eé!:¨\x0017RuÔ\x0010ûw7Ïn~u|fh%Â\x0008Ï&J¡ÊSÇªK^2gAÚJÆildÏEÊÆîÜ5ßÇ8\x0011öÞH²¨\\x000bäÎ\x0006\x0002äa¡!zc÷u&¡íû UH¾Eòg¶øf3Pg
¡®gFÍ¥Õ\x0019HÅn®_©Ê¥\x000e¿¤a¹·ÿúñÃ×Cr!_óXê(O`X\x000e2	>ç\x0003ÅWÏ®n~öôõ\x0019l¶e³J6¸ü)R¡ÖÚþLC¾W¶`\x000eÏ|=ÍµlNËæÅñh¸áÍPá\x000eµ~*à|\x000bçp¡ 0ÕÕ¼\x000c£
p¨æX\x0001\x0017Z¸ óûÁâ±Êl'\x001bÃe,×Ü²Ðv@­éäR¼Ðk\x0014ÓÉô©e²é\x000c]·è@»êèî;1]ÜØ,pá@¥¬\x0002®û® ý°eò\x000c\x0013ò5S±l	\x0003eÐ
ºÔÑ%%]²,@\x0011Q\x0014kP(¹¶ÀÅ¹-\x0001ûn¤Õ
¿ÓáadE¸uÝ­tFf6\x0005s¨\·ëñvÊ0r\x0003û)\x0014ú%N/n&¨èû'Ä?|ùüñT!ÑòV×=k³áfÕ²c\x001dã|ìÖüç§¯^<;QHTñlgx|£ï(OZ3È\x0008Ü¯ê"¤\x0007Øò\x0019Ì·`^	æðÚ³l?ÍûäÉFr\+g¸#·±g-FÓÒÑ*>kê(sÒ¿ä\x0006ùpãÒf\x0000¶\x0006\x0010üæ	¸ä_\x0012*¾_ý°ûòå?OÃÀ*®P¾ªãÃ5A¶kÄ\x0003ê'o¯~¸yõê\x001fr-S@Y®\x0018*3ñ( êÊ\x001e¤ÍÎ
-TP@9n\x0000(PHì\x0015ªÎ_\x0019K¥\x0016*) \x0012\x001f\x0010¢2:§@E\x0010\x0001÷»ÈÏj^Õh]\x0018\x0015Õª
OÚ\x0004un_d%U\x0017\x000e\x0008
Õ-tP¬ôUqò<±dCLD­ÃHÝ2\x0007Å:§~!þz.°`d¡ª	äPt6T·ÌA±Î}¤î\x0015Êìg\x0003fÉ\x001bC¸7MÕ­sP,ô`V$kùbMFYOá@îH`7\x0001\x001b¬¯ÎF¤â"é\x001cÇiÎ\x001aol¨¿;ôå\x001e\x001aw²ÐÄcÏæË\x0010ÇÉ+BtuÓ=ú(kÜÙHÉs»^IµD¡\x0012¡+j¹C+iA:+\x0008Olyâù<õ\x0011Ië³\x0004¹\x001b-<\x0007\x0014ïÎ5QjÒù_-³æÒe¾å>\x001b= fq&ÒÞ}/\x000bÛo&yG\x0012¡ä±qÇ¦8\x001f\x000f¨Ì<80'l\x0007æ\x0004Ó^ðì®^~Ü½?·ÓÈ\x0006äÃv6&Ó,`X\x0007Ï`í:x®¸¹zùìæÉí±¹\x0012a;\x0019'4S\x001aÎá\x0002êîXÇ¶\x0004ÓbV¦Ìlßx·\\x000fÌ¶hVe2g¥
64kþKD\x000eÒQyø}É\ËåT&+vJl²*ùáQ\x0016úýÁ³M\x0016Z´ B£NÀµÃ`¢z±\x0005\x000b
Ê¯\x000féu*ÈRKT\x001f³dç×?Ýt®UÃ\x0016Xb!lk Ôh¹EËº­\x0019Y2+ÓÌI®\x0019¶V:w\x0011\x000fM8oÖaÃE?jÈ0ð-\x0013\x0019«ÐÊ	ÌW£\x001d\x001a¡r¶Ñéà,D\x0001ççPMøµçí\x0019cõh´ãÎ\x0003\x0008±s¶ô³Ê¯âöW:/NMzÖÐ\x001e\x0012ÍÒìÐ¶}Ý¥û>ö³ð²áV{òs2~ÊÒñ¿ì!ª3\x0008ÁÃ&+$ÿ´\x001f:÷êîÓÝÕ¥ÏþÔ+\x0015Ùðb¶zè\x0002g¬å\x0000Ù·ÙËä9\x001a¾xõdéµ\x0018\x0011[DT#®õkÁ½\x0006®ðÉ\x001cMmy<ÛâY5^ñwë=] YUQ\x000eyØìú|v\x0008ÑµNX¯)(DÐñZ%ÀÞ¥|ä~¦Ø\x0010¢o\x0011½\x00161®\x0002\x000b"Ýv®)¯ÍÜ;^þpu\x0018ZÄ ¶""ß\x0017SS»\x001c\7²Uìáñ*ÄÔ"&ýZ¬â\x001d<½ùðn¶(Vt§j\x0010l\x001cQé,Ï=åKc]¤¶2ú4oF×
Ò]ö\x000cýBiMo8î\x0015ß\x0013¤^ÂÉH\x0005s_iK\x0006Hcæ'å°\x0008\x0003» ¨&XÆnND¤Ïß\x0008[>Ù}úöù{a=Yz\x0002æ_pÉ©×\x0005Ë¯hÞãA
É'7Ïß¼x[PWÞmÎ\x001e\x0004gµp9ò9&±9î\x0000¨O·þà;U\x0007÷ ñ\ËçÔ|,®\x001d¡^R\x0016>Þ0nieä\x000b-_Póá5®w\x0003\x0010C­zj\x0014\x000f.Ïæ\x0003zk\x0017\x001fý¬Dtrõ®\x0000ù­ÏK?óÞ\x0014\x0015bÚ>§¥î9íûÕÏ¿ÿË¿|9«B«øo¹eÈ
*T¡%Úåuïo¯~~ñö§^SW¶Ïk©{^SáLË\x0006w²­å×»Ãµµ\x001a\·-¸qv3ÄûÉ_wßîvß¯~£WÕÝ÷\x0013\x0017FÔ3ÃOª!{®R²É°v¸ËÙ\x001d\x001b³üäO7onoÞ^ýxUþýa\lqq\x0018×pn\x001e\x0003í[\x001frbfU}£;èÖõ¸¶Åµ£¸ÉÉ}|,ÇD\x001e:_(·,³.ëZ\7\x001bëâ
µ\x000eËîbrÄ\x000b-\x0006ßâú1ÜrÄk1.ÈógJìdýòÞt\x0011ÚÐÒQãÖ\x0001AÅ¸{\x0018I	Jê7]uã¸±Å£Æ-;K\x0006B|ÃQò;¾N+ÇÍÃ\x0007$=njqÓ0.Êû@pN\x001eS3²ÄË\x001e\x000e\x001e9Õ¸ÍÃ*¹]3º\x001a¬ª2\x000fF°Qf/y/Ãk ÕP^C\x0005ýbÈÊ¤\x001d\x001a¹)\x0000¼L¢«Z%ÞPGî\x001cuÞ.lå²õOw¾|¸úáîýÿü~÷åîã)ë$£:R\x0002\x0016\x0006.QÍ{i{7Lº}þêéÕ\x000f·Oþñíí«Ûg\x000f"6e%\x00051ÇÈ°3#>BF\x001eÛ0Ò\x00102v\N?\x000f2u+~|9t9<.È¸=ÙÇådóïwêýöÏ»SUöKÁøÚ9\x0015è*Yw\x001d·¡;4ý#ìÍ¯·Ïë
÷Ï7'kíãæÉðPG3\x0014×\x0011jYäþ¨\x0014¥@vÓG<@g[:«£34\x0005p½®#É\x0004äGuQzpVø\x0001:×Ò9­í¤ò9\x001c\x0016×$\x0011tpèûb\x0001<ßây-#õ\x0005/;ºXñäÚ\x0001Cÿ\x0004:\x0017Z¼ ÄKÈ:\x0007\x001adc$Åz~Öz©ÅKZ¼LíÒëÒ[H\x0017¼,%&\x0018Í¬õruxH7\x000bëÑ×@½Ë µ]6ô\x0013±ïã\x001d«á5¼\QÂ\x0019ÃéwÈt/¼\x0016\x0018g\x0013Ä©$|\x0000î!ÛAï>\x0019\x0011¹\x00004ÐÕ¡[^ý´F
Íáu.\x0019>
\x0004xgd\x0007¢&AN\x0003vs9À×9ePzezç³kq\x0001\WXÌÇ1·¬=7¹s¡sË ôËXB\x0005¯>o¹(¥/ðáÏÂlÄÎïÒñ!8.æ	¤YÈï¡Ë;òÊýuú\x0000_çø@éùJ*Å%î®ðÉê³)AîS\x0002úQç)\x0013`>\x0017%pÄ,{*'
»MgÊ\x0012xwÊÏS©ûBåc»M;Y	#\x001b¸\x0010¾ë	ßé\x0008©DÑrnòS-
Ä`f3«nÅûÑ/\x001eW\x0006\x0003nK	NY?³8\x001c/ïO\x0019¥aÕnúi\x0014\x001b5CêÌoo÷ï¾^½üüûï\x001fî¾zpåhÄ\x0001/Ñ®uËL/\x001bòpí\x0000½ð¼|ñË/Oo_x\x0010Fl\x0019QÏ\x0018ôµ§r¨[$ø,\§!m\x000biÕ¾Äc#Ç%'Õ6Fªm\x001cÚ~vÄ\x0018¤k!Þ9®C\x0010Bra\x0015_.)\x0005ÏV)\x0007Î|ø"\è[D¯·#x©qXôÖ£	Aì\x0018¼Ü¨ C\x000b\x0019\x0006 ³Ô³$ëD×ÀD%Ù¾ÀL-dÒCÚÀ\x000f·!y'ÑÐÔp]~?¿"\x0016ý5÷\x0005ÍBÝÜëÓ\x0017Bm9Dk\x000e_p«(;\x000f\x0004z\x0017DUKN¢bíÇ5¹Æ\x001b\x001f\x000e¿r¨(»Ý
úíMe\x001c»IUßÀMôuïÌ,Kã{}õe.jù6K\x0019§¢ï\x001akÃ\x0008\x0015?\x0000ç\x0017RÏB\x000e©e\J9Ïí\x001eîuÌ\x0017@«\x0006\x000ctÊÒUª«^>\x0004×?]Üç;ÒÖâó&^ûÜÇkÊ'^}ø÷\x000fû¯â\x001cz\x0014ù#\x0017TþÈ`¤ÏÔ=âÅ)©xõô×òOÖÆæMÌö¹Ùçrú,\x0005u¤o²±ë=Ä¦jÓ¶vÓqæLÃ)\x0019P>\x0016pT®åt#V6NáDºü\6w
âÎó7µó8Í¶SÎ4r«\\x0012yØýv:ßE®ØÔ=\x001f°A6õGjñÐ\x001fÏ\x0000Ä\x0016\x0010\x001f! m\x0001­\x001a0ñ\x00011ÚdÈ\x0001ª´\x0007ô- \x001f\x0000LÜ:
^ü÷þz18\x0006-`\x001c\x0001äÆrf\x0004°~âx `R\x0003è¢k\x0001éG-¢k2k³TÇfjû­=¨Oq\x000e¢5©òN¢âëÒ{÷éÓ©ª¿LO>GáÑ°÷åÛ"}eæp9Ý2FðÕ«ÛçÏO\x0015þ	$¶¨¤\x001f\x0019\x0001QN6ëÔ%©óZÌa¹
\x0015¤m!­\x001a2¦xüjÉâÂ×¡K&%ñ.D\x000byd$£Ù\x000e\x00154ËSö[\x0017Ûñ¸õ+\vÒ	\x0004^½Áoýoý×þö8?76ãK\x0017Î÷zNÃRÆTo$Ct³«#]òaí|%æ»\x001eóÝc5ç®çÜé'rÂ[\\x0011p¿¦ËV&\x0000	Þ^ó·ó7=§çwÁòÙ\x0013ßÞÏÕeNØsG\x0017»­_¿¡¿HC~\\x0010¿ÿÇ\x0013ÑJ\x0001¯7Òòm½Røæ¾òá³íí?=e[,«ÁB\x0011º¢\x001b4\x0014,yòH\x001eï{9\x001fË·X^g­´æ~ÕÙ/LrD-)÷©bË\x0014\x0015Lå\x001f¾Þ\x0014¦ÄÃsmÁî«2[¬¬À¢ÛY^XVÄ¶è¡\x0014å\x000bÎ,,è×»fÁÀ­).KË¥;PÆ\x0002_zôA¬\x0012k7­£ÆAß² «äÃH*\x000eÃ®\x000eÃ\x0000;6or>¨@¬(íÜ4\x0012,\x000eÂÖûíH·k\x0003£N®\x0015\x00169Ò° µ-¬\x001d5Yñe
\x000fU³9É\x000cò\x001fÌ¹Ô°®u*¦\9ò%^\x0006FÆ¨ØÃZüjXßÂúAËÒ¹`]\x0006Ôw\?ík1}ËÀ\x00166Â\x0006ñâ©,ßu·Íu\x0014\x0006`ºÌ-l\x001cu¾ýbÙl¤Ã&söàM:¬£®fM-k\x001ab-\x0019§²µ*Ý_¯v2ê»ø[PÇ[ËÚÖÐC7òG\x0005KJÒ­\x0012Di.z\x0011¿Íñ°^úöHY\x0014£ö\x0001a,"\x000cZ\x000f¶Ä))õ·é"á\x0000:\x000f\x000bc.6ÑP\x001f'\x0014Yôºb\x0012éÙìíÁlWK\x001d-ÒÒY\x0001Ã?¶¹&\x0003ÏàúÍµ?ä®ÛëÛcÞ_Û\x000fà±(&á%0\x0004öµn\x0015\x0013ãÀp!\x000b¿ë-ünØÛ²rr\x0002Ë/¸ÅÛò[¸\x0007sÔ\x000bº*ÅÂô!\x000b\x001cq­n*Ie©5'	»Ä(I^SßD´\x000e\x0003»Ú?pãg´Î?¸øM5Ñ3ZØäÀOV1VE6FiÃD¸ÌªH½ÓK`Ë¢¬ÃsIÕ³ä7f.\x0019sÛ6\x0007\x0017M'øåý_O\tgOÒ$ëÍ"@[dO\x0005Ò\x000b %yüC:s¯
êÃXØb¡\x0002ËI\x0019mÙûÈe´Îcb_es<¬Èw\x001em±¬\x0002+d\x0019\x001aL\x000e2[Ëó½¡§&ÐãXG\x0014¶¶Ý\x000c.NÝñ!¦r¤7ë%! \x0008y8Ïïe~+"¤´o©ü£ù¡Å
ÿíXv»\x000bíº\x000b÷u
»«>ú¶ûðé´gi9)¼÷ÖÊÌg4ý´£}YÃÍÕO/¿¹yúü\x000cBl	QOK/
¤»f½/DcÎô\x0015c¶e´zF\x0017Xg"Ó\x0004r`¹¹È­­\x0001ra9\x0006éZH§¤ÙVP\x0004\x0003\x000biRÚ(x0\x000fé[H?\x0000|àÍfÕÝ!a<!ó¡%\x000c\x0003ßÚó5R&ÕþÀFÓé÷Gj4±zHzAfA\x001b®y=\x0006 aÆ\x000blìÔ2¦\x0001FsÍB~w¯"\x001bp3áh\x000cñÿgîÝâJ²Dí©ðö?\x001dÌï\x0017ÓSD\x001a\x0002\x0015´¿ê%-D&\x0002%\x0012ÊÊ|êiô\x000cN£gÒ#9¾Ü×òp\x000föpßlaÝÐ
ZU|òËºùºø\x0012ÑO\x001eKÖád¢ä±D¸æ\x000eô\x0011ÿÆµÔ/_6ÆýùêúúöÛ·3¢|îà/tN5R9µ3\x0003}v~><::yû¶\x0001Mh¢\x0003ÍA\x000f&¬\x0000Âù§ô8\x001fMh²\x000fÑhBaÀ2ÆîOZgùÁÁBíhªDS½«æpB	\x0014\x0006à$<­-Ãª
vzmGÓ%îCãP÷F\x001bS{Î=©\x0019ÊiG³%íC[±
\x001aÎá5 é_n°ai;+Á\\x0017\x0018·»\x001cï§ø4'y0ÙP¬\x000e4_¢ù>4¶»"ÃæÆèÜ\x000f}Ö\x0015(Ò¿=[õ\x001fo#ìZjÕ®iØ±6_O9kÑx-o{\x0004nX5Ç~\x0019zæ\x0008l*oè+ÖÃVI5Þ'Öàm:¡Ñ\x0004MÇW\x0013ðæ­Y%ÒxL\x0013z5-QwJã¨\x0001\x001béf*4Ó\x0016¬7g3\x001avÙó\x0017\x001fÐ6®ÚHF·_+©\}rC:t\x0018\x0003ÛÅy\x0004È\x00063=[×K¸Z§»>­\x001eÎ¿ÇC\x0016,6\x001cfh,Uáh;ÍéJ=ÁÇN¹ÕzN6¹1E\x0010¶sd³µ\x001e°};
-ÈW\x001dÛÈ\x001aë²öT\x0013oX«¾àB\x0014\x0007Ï/¯¡áéGÀ|sùçÝíæÑÇ\x000e+eÁ0J÷A¹<ßSºáéïGÐ÷ô%\x0000¿9øçéI®´)JL1\x0011ÓSÂ±ÁÓ8\x0019URÏAÖJîo\x000eÂ®WN²[rK Y0\x001eÁ°jx=$<*â{\x0012«û\x00046[òKÖK&ÙÃÉ­pù\x0008jé±!¾\x0006\x001a3Z@×Æ&K6ÙÇÆ%E¬µ¥
mi¤d¡µq\x0015ýpªS}pÁ}F¥¯aº\x0015.%å\x001a\x000cßÑR´68]ÂéN8MmX14oËXAóÒ`¢Ô,8SÂN¸É¤@¥vÆP¿\x001bëÝ´[ÂûÎZÚ£Ìi{ËwËëÛM/$BXLc}lS1âÔcI\x000ba\x001eæÌí-ö\x0017G'ãÏ"\x0019JP¢\x0019{¡4Ø«\Á\x0015 ê¹\x0006}P²íPFQÇÔ`Û¦Ø«bÔ@\x0012_3*T;¦\x0006YÖ\x0007CÉ"FRCÓäéPºÒíPÃ\x0008Åãó[²ùÍmÍ\x0002ï2%irr ãÜ ÇÇVÍ\x0001eK(Û~÷Xn\x0019\x001cV
k­\x0014ç6¯ë
vñZ2úAßëå·å¦dmÏ\x0004$kÓl\x0011
µ,O±ã\x0005½G·Iå\x0004)JÈõªã\x0006HÇòÜ© ÉÓ
jÅó\x0000\x0014¡f@r­Ö,JhÞºê\x000e~¶üru³±\x0000W\x0014ôAÎ¦Äü Ü¨k1·¶îÙÎÙâÍáq\x0003(ÁD\x0007ú\x0013{p\x0013\x0018t´#°¡Yìí`²\x0004=`Ð\î)Iþpys\x0012­\x001e­µ©\x0012LõiNÝÓA'ß;¥){g­\x0008¶\x0017L`ºkÅ4^`àÐK\x0016\x0018%ÇÎá2%éár\x000cg¬\x0006ã	Ë	J0C\x0013áÚ¹lÉe{¸¬ vÌÐÏ%\x0015õpgs2±\x0018\x001e\x0017Ñ
æK0ß\x0005¦©ÐÃI\x001aÓ\x0015ÀÔ*%{ ¢Ö\x000cÆ«;É{.¥â\x00067C\x001a~j\x0017Ä¢ÌÛµnæd²\x0012c²KÑl\x0012kÞM\x0013º`b\x00185±ß5Ö 1UBöH
%8e¡Yè«$2÷û\x001e¶a)VÉ/Öe\x0004ÙK»\x0004\x000b"ðÞÙÁI\x001fMXÕ\x000eª\x001dTNcdyl\x001b\x0019ö95kð~`l+V-í»6q5K=¨Â]ÜÃh\x00043õ&SU"UõÈT\x0015~¹%jw\x0019^Díé"ªMæÄf*WQ¹\x001e*uvð²£pffò\x000eêê¼ë®óÎ(³.N(\x001b¸¡µÒ\x0003ó·[±ªó®»Î;³PZ\x0018± °4aÉ\x000c¨V¬ê¼ë®ó\x001e°4î¡¢1;E|`Þu\x0013\x0016g¶:Zñs\x0019³è1ØÞ\x001fêqs\x0006§¤®[OÜtl°ÛÌ¦t6á9\x0016NÄGaÌý\x0013\x0002ó64U\x001ev?°ãÈ¦T;·ÂéØ`MR3Ê=ðÆà\x001c\x0012%<ñ©4\x001d|ªä\x001bjÛ²O8Lè\x0000Ø.®1h»
=<R®O|º1Lw,I[%$§è\x001bký·­\x000fØdiÀæéíý·Èv´¼¸½»ÚÄ\x0006A2\x0014pAuc½²âLP¾Y³ÊNÎß"ÜÞÉéa\x0003(áD\x0017\x001cLBÑQ:â2³Ù5#»Ml²MrJPt<X¶\x0018]\x0014\x0014ÖÍdS%ê[· K±·\x0017:MpM\x0005yëY¨ýpºÓ}\x000b§0ÏYi\x001c=® \x001b"Sksz»ÁL	fúVM[2"½e£8UX\x00079gæ\\x0005.@¸§ð¹ïÄq|7qá?ÁpâÐ%Ð\x0012"B³øü\x001aïÜX>±cÆaÇ4h5NWB®ÍHïå+ê\x0014#_ÌéØ_n,\x001aË8à5\x001el¹yx|
¯O\x0012ÿíxb
¯O\x0016Kc°é¡\x000b\x0016\x0018=ñHN¡\x0018áüLEQW\x0018iª0ê:\x0002Sc¢t\x0011\x000eO ËÒEÏ9 i¢¨k][l4íÎå` g&7¯á¬Öbõ\é¢|è\x001f÷Ë«q(Ç!\x001baC]ÐiÔh
UÃüã|q¸!&£Ö\x0002ó@$=od\x0012ê\x0013°76£ä\x000e($K$Ù¾H4`>6´óÄ©å¹êa¨\x0015IHª}ü®ÊD8\x001d³\x0015ÐC¦\x0015H@º}<½·JèÇ\x001d=\x0005Mu0=ôþZLdzÎ¶Â.zÁµ²´m¿{\x0018ooE²%mGR4VxGÀ\x001d§h£\x0011zúáv%ë9ÜzÅªâp\x000bB\x0012\x000fc/­H¾DòíH:'zIÝ\x0005\x001d·yød©T$ÓdíL«Y²AW\x000bºr4\x000bÉ¬µºébªewð^¥j;K£6\x001cw+¦!ÆV¦JTòvY)h"Ð³(¾©SY+çicZ´pW\x0015wl\x0019\x0003¬
i\x0014n\x0018\x001f7\x000cPòn0Ïxãà_¾\x001e[á®*êØ\x0014\x000c\x0014lðÉµÂ\Ù°z\x0006{S¶\x0011ÉH¶\x00139ò\x001a¡{t2\x0004èÍTiæ\x00073*t	¤dîu\x0000¾p¶Ô2Xó¡¨~#-ì\x0013X#_\x0002ùc]W`ô:öu×&h0S'"ñú²µß¶°Hr1D±J|:RuxûQú»öÍÔ\x0012	>6#yÊ41+Xl¦¡e\x0016îáüê\x0006(W¼Ã\x0004(§\3\x0014$òa''A\x001dsµæÑÁ'o7Õ­LNçþmR`C\x000e\x0001Y9¹È\x000cQY:I\F§³Q@\x00194Á¹§¡ÁA>ÑÕb°Üa\x0013×I·	;Ï\x001dÝ~»úúõòóåÍ·ØoñåËònùmcZR\x0018P\x00081ö\x0002©dÒ¯ßNÞ\x001e\x001d¼>8~\x001b;ô-Þ¼Y.Þ6À\x0012VLåÿÂ¢F\x0003T\x000bmWæÒ>\x000e©,Iå4ÒpYÔjtâá\x0006Ëçu\x001dÏÎªJV5í\x0008°Øs'­ªÎ\x0005ê\x001c\x001b­³\x0008¦Ãê\x0012V?qXSÂi°ÜRé¿b\x0006{P\x001bO¬km¹¦³ÚÕN;±>\x0013ÓÂ:	Q\x0007bÍÝ#	\x0002WÂº'\x000e[~\x0007ð§,\x0012ÊFb¨\x0019à\x0007ä­Á<1\x000f\x000evzÑÂS?`~È&æádPÊµ»\x0016~°>üóÕÇÍµ§^ÊÁ§ThÿCý1§>/l´\x0016ãçÃ\x001b³r	P¢\x0017\x0010,> cT¤4å«H;ÙÜ
'K8Ù\x000bg<´	H|újMÏYÒøÑbV@U\x0002ªîÕ\x0018Sq:=,	
Û;{wuÉ§\x001e)ùL÷\x0006sêúÅ|~Öå
£Õq­®\x0004tÝ4JÇ1HÀÁ\x0005¤ ZMÒiäãAxUò\x0005>w"BCDîs°ÜWz$;£}
«ÞI\x000eÂ\x000f:E!Íf\x000c¢P@eL\x0012*wxs÷Zêõ¾Wú¬>xw{½\x0011PzE9.ÜJìO¢$U\x001cjÁ9\x0006x°rÔ\x0002(J@Ñ\x000bèÈ®p\x001cÓ\x000e¤\x0014DÇG¯r+,ád'ç%ÔtÁôÅÅs$ªcZÉf¾É%z½Ï~ §·Ã)ñÜ g\x0002NR$å¼\x0003ÃF+]ètI§{éÄ á\x0006Ó¨ßÕóèLIgzé¸Å\x000e³ÎÒ´´9'B«ÑBÜ&:[ÒÙîc\x0017¬ª\x0004g
:uß0³bÞ©s%ëeÓ¸©\x0006wbPRO&mÂò%ïÅ\x0012\x0006±\x001c\x000bºCàM¥\x0002\x001eÉÇ+Ò[àVoSQ\x0008³î«\x001a\x000c=ÜQ!ibtÜ\x001f7J·ãqQàø¹ÿÄ	T\x0013Zb\x0011H8sÒ§¸\x001aÕ·Û$1Suè,¦£¯^Òö¯oß}ÞÓèÃUP²ÔþËå¡p¦HC¡ÖÀ»ÕþÑÉþ«Óí\¢ä\x0012=\ArxêøB\x0016¸¨Ç¯ar(ù`+\x0018gjíM©õGW\x0017Á¼º½Ù\x0000( k\x001f¶
y ªWô¼¦\x001dí<wt¸w\x0010\x001cÉÃãí ¢\x0004\x0015O\x0018T r\x0012¨ÎíÞLê\x0015ÖÍBÓ¦ÇàT%§zÂ\x000bªKP=\x0005Th°
"¨à§\x0012A%U\x0008imGûv\x0016¹\x0005pØ\x0014RÍ±¾\x0010\x000eÇ(\x0008oò³ÐW×\x000b\x001a\x000c5)	\x000f\x0003«vÿÿó\x001fÿ¹¸û¼¼¿\x0001QÓÚ\x0018Ëð5M2K\x0013\x0014Øð<ÅéëÅùóíh²D}hÂÅVE\x0011MJj.\x0012v\x0003ú8÷\x001dÜát	§;áà\x0015[e8lË\x0012®¡Ïp­v\x0008nd4\x0006ÌôÅ·ãH¦5\x001a\x000e2Öäa«¢á9ÍËæK8ß\x000b'ÐÄ7VÅ\x0015WÂÛ\x000c'\x0006'ýµÁq®lu\x0017às\x001f°©~Ô\x0018'W2\x0010(fë\x001bÛ½v¼Å\x0010/ëEßm\x0012xìïÄEÊ4LR=Î»íwà-k¼e\x001f\x001e÷\x0018Ú0ÆX\x000ccI\x0019\x001eç·\x001dO¬\x000b:a¡ÓÛû\x000f\x001f®ïÆÉ¬s*\x000fÍ[)7Í¨\x001b|w>=9ñâp±¿Ld¢ÌÒ\x00062.yÑY,Hèyh²D]hAÑ&\x0001\x001cG~§í\x0014B-ÊéÁ«íhªDS=hÖÇ"¢\x0006\x0003ªSvôy\x001e\x001fªï@Ó%î;jºÁj\x0019\q<j¶s ³°\x0007Ì`¦ï¤ÅJ\x0008Æ\x0018%ó© ô¨\x0005Ü6¢²\x0012\x0017¯ïfßåd«\x0016gZQCdÅp²\x000cÌC·²\x0010kñ\x0012,{èLN©w\x0018lÒ©èí@93ó\x0016ðwÑy¥hîæî¨¶Ä\x00077ÓÎ4ë¡dSOÅÞyqu\x001d\x000càM\x001dÂºÜÅf<ÐÆ%\x001e8èØB\x001d\x001c½óâð(Ø¾Zõ8²©Ça·Ð\x0005\x0015eSC#Î%¦oEô4<a­?Ü\x0004<Uâ©N<iS1çál\ÈÚÂ\x001f)ç-5Ð±õ"\x0013¶*2Ù¿^^Ý]noÿ\x000e};-5À\x0011,'½\x0019èþ9S\x000fs÷\x0016§\x0007

àÙz\x0007[xô ªÜ\x001bÆakQ'©	¼zXYÑ¨JDÕHcÖ¸\x001dë#aÎfä\x000fÛìv\x0003\x0012Ðt\x0003B_[Ês\x001d\x0003½cÉ\x000f{Nw#º\x0012Ñu#2KúC¬¨Éyîõ¯\x001e42i'dk\x0006q¨îªÐ`oyu½)Þ'\x000c5=\x0012Á\x0004Ån&ÙÔ/j{ö\x0016G£.¢÷5÷ÍHé\x0004u\x0006É?\x0014Ya\x0018> Îh<d¢Ö\x000ct®ÌzøñôòËýÅõÕï÷\x001b·2\x00109\x0014*Þ\x001e5t\x001fÌøÓ7ç{Gÿ8ßÔ\x0012X­ëÀ)¦pú<!3x\x0011T@b
¿PÚÕE-SAe	* h8xk:Ä\x0000ºø~\x0019þÖÎOË½Ëå_ß6P}ÍÛ\x001enpjÛ'¥rtu]1»øùà8Ë\x000e\x0016Ç;{\x0007Ç\x001d¼ÝÈ¡æ¶@;)MÐÈX¡#
U
Á»8½*ø:A\x0002%_µlð¹w-mÐ(É¡\x000c+®®á3Rº¾±Rñ(\x000ee\x000e³\x001f<ÿ}´üvùîö¿ÿïÝ¦\x0003éÁsK©.Sÿ\x0016é\x0014:HÚ\x000fô§\x000böÌÁþÉÁé¦î\x001e	ÌT`æéy]yýTÀøJ³\x0001\x0018'ÕÖBÌæ\x0004æ\x0015v>¿ ®\x000f]­ÁF¦ï%*Qí#|l§im)\x0001Ã	Ï\x0003Ò\x0019ô×L¼XÓ¨«¨{2»hëõ²]ë%\x0019±º ãvS¼8Ø	\x001a×Ë<l@Õ¸^WT?õù\x0005\x0019||*d¾ÚIøøÃÉ¸^\x001f¤ EÕè,\x0018èßv^ü÷]_mêyîáµ\x000eg\x0000(A=Ïm6=U2Ühç,Øèow^\x001c\x001c\x001dnhÊN²¤\x0013(¥¦ASÒ*l+­·ÔáÆ6]º¤Ô\x0013(¡½eJ$P\`ØXZûÇ¯¥´N£´%¥}ª¾¤ôSÎeLô§Ö\x0002Dé\x000c9ik­Ü§Pº²÷¤xær2\x001dE"e@Æ\x0001òQ1¶\x0019i\x0005ÕÉa
GyÉãT)7\x0008ß
¤Öàÿâ
¢÷(»^ûÅ¯zÌ´Â®ªn4ÄQMA|>,_åÓ`TÇ¾\x00051Y\x0012WÖmoÝHW&Xæ#ìª§l¬óGðÕòîöþfçíò¯«Ë\x000f\x001f61jh9eÍ9\x001eRìÓ\x0011#Ók*èÕ"p\x001eï¼]üëðàÅ­|«öÀGÍ#\x000c\x001f\x0017¼äO\x000cPÕêÉ\x0001jY\x0001jùd\x0000Ão\3Dî]ñæòîëåÇÍÑ\x0018fóô2aVJê«\x0013'¯¡½98=;x¹1X$Ö{EÜ+¢	JQõ:$~)Aë<îa{êv&]2é\x000e¦ÕøVirÔYëÌôpZ;-¡l+õ~\x0015Ì
\x0014Tj§X±P¾dò\x001d\x000b%óHHåó\x001cMG»Ù]¡xu¢xó²Þ)²ôa,¶ý2ðTQÇ]\x001aÚ©ª3Å\x000fUì>@·J3\x0002\x0014=3kÿ0\x0016¡\x0006ýÜ%[K»]°vó^®/o6Dê<thÀ¥ ¨ÐNRÞa7\x0004Ãt\x001d?Áq/G\x0007Çã\x0011º$J$Ñ\x0004<SR·liÎa²\x001e\x0003ÒE$K"ÙL¤y^$HO¯´qH^BZkj×¤J$Õ³HØ/\x0016f9MDHrú¶éH7\x0013£!/¦\x001a\x0010\x0011HØéD¦$2ÍD +qâx\x000cv³2lmZP\x000bRØôõî"?\¿¹¿{u¹1@Âa h\x001c²¥YáÏ$-\x0007ÔïáþÉññáæ\x0000Xï(rÄ6.h C#Á\x0015d%D.\x001fi\x001e¶$ìáR%êâÒÔ+Q\x0018OC·-Ëï2kSêÖÀFz\õ\x000ew"?ú6î¢XM\x000cå ÒÓjåÌ\x0003'\x001eä¼t,Wø-Vo½md&·W\x000fW\x00064Ãèm*ïP\x000fMíd\x0017lmé\x001eK£L®.ïw_A«p%ïîþy\x00077ÁT¾ßp;!EÓÏâ¼?´dè!Kë:uãèðà|çù!´\x000b\x0008wôôô;Ïw\x000eÑ|>~Y3V1S©¡ã:%°A\x0019Noòí\x0015õtúMØïï_¿Ýa\x000bW-5|-T®þ ±Ø<v(gË\x001cã\x000bàx\x0016iãÐ\x0016\x0018s=\x0016×\x0017wßv~Z¾ûý~y·!×s(\x000f2Û8ºí*üû±ä\x000c\x0002¸ë§wq´wpúvç§Åþ?Î\x0017§rxýz\x000e¯7UiòýÎ«û°¸¯W;<hØ
\x000bjGàT~MSn%40Îï°Ã¥qç;¯ÎÃÒ¾^\x001c¦_\x0017þ°\x0006«M	«Í4Ú \x0008p¶8±Z*Ge5qäç£Àº
ÖM<i\x000c~K\x000f]
#­Ï1FË\x00070ôÒ\x001aVÒ\x001a6\x0016|\x000b<\x0008Ð
\x000ei)[Ä²¦"Í°ù5\x0003\x001e9ëBÉ£«ëåÆI*Ú{\x001dôR\x001eÿ{O0gFËé\x000e\x0016gÛñD'zñr\x001a_P÷y\x0010¥Ü\x0004Íq6âÉ\x0012Oöây:\x000f{\x0008\x0005<´#ëFË`\x001bñT§:ñ¼G37Ð	
è0"\x001aìÝÑðF:]Òé^:*\x0005	óÿÈD-dÔh³F<Sâ><Í\x0019°ÓÍP¤Ïiî\x001esnî½°%íã$¶\x001dòÁµS"¯»µ®ÄsxBÀE<éÈ®`zÁÙn§ó%ï]¼h>äÅ!n¹ù$\x001boqÒFW\x0016gú\x0007Åõ[ñ4Û¥µSùZ8\x001amåç^Z^ëN¡ÁéÂÅËÍ\x0002¤Åóãõ|Âà\x001aC\x001b¥ÖqFe­<O¾fÖÌå«4\x0006ïT\x0019\x0010ów4&\x000b^L§\x001coÑÈW©\x000cÞ©3t*üOûk0¢%8·¹	êx/´F¾JiðN­¡\x001d)¨O1\x000coõ£AyÍ>Öà½j#õÚ7ØÙ\x0016CÞ\ÑäîÙ«W©
Þ©7\x000c4(Ò©\þÅµ¢ñ»l¼×X#_¥7x§â0\d½Æ
uæyÄZ3sw·Ò\x001cë}¼¶ò	Fé7`.cA\x0013·ÚeÕ1Úë®OTºCtê\x000e\x0003A{.*F\x0013#4øf¨´èÔ\x001ef5|Ói£¯ H\x0010i\x0019ÚÝèÔ\x001eFSU?$+à¸e!8Öäh¾\x0016ÄÀWi\x000fÑ©=ÒT\x001eáÒcHä£"f¸¿­\x0003±ÖÕ\x0006J1>þÍæÉ&,\x0017=|ØÙä\x000b8zØ\x0011¹Já³8÷r+(¡D;\x00144vÅIkRåíÆq:ÿ ¤Þ\x000e%K(Ù\x000e\x0005EU\x0006W*Wºr§hü\x001b\x001b!Ü\x0006¥J(Õ\x000eÞÓ"TàC{Fzk Èß\x000e¥K(Ý\x000e\x0005NkbR|×zTVT½\x001f9ÒÌdJ&ÓÎ\x0014Jêx\x0008 ÊL\x0003/ÚíL¶d²ÍLPT\x0005*Ð)\x001e§\x000fq\x001a\x0014\x0016Í8æ®ríPÐ¢\x0002O\x0014©	\x000e}øØÐÎäK&ßÎ\x0014l\x001eFòÀâÐú òØ\x0001Ï\x0007ê\x001b¡Ê\x0019·ªÂk Ò\x0006 i¥<zË^©¼T3¨jyÞ.Ð¡\x0013\x0005VêÀ¡Â
Zè8eçàå6ªJ óv®%ÏrÅTh¤B(30Aª\x0019ª\x0012è¼]¢C4FÚ¼T8ÍIÏóRM\x0017
¼è¼]¤ëÜ%,'åÇ#[k-¾ÖGUtÞ.Ósé\x0015',Uî7\x0016îNÖ3\x0003-æ¡*ÎÛº
N9¦Ù:\x001f<\x0014ÆõN\x001a\x001aÛÒ
U	uÞ.ÕU4¸É\x000b\x001cò;²ª\x0019½ÞFUIuÞ.Öa4à\x0006êqRò\x0014÷6Ç\x0007`LìdªJ®óvÁ®@°£\x0006äô2\x0014ì\x0003Eè\x0004ª%6\x001eÊ}\x0011Û\x000e\x0005Áþ¯\x0005¤Eï]}¼½Û\¼\x0004=õ\x0002\x0006Ï6et\x0004±@Oõeøo}~°³wøòäôô`+P%\x00154i¤r d¸r\x0010\x0004HN¢´T\x0013¬®ú`õpq/X®\x0016|n'\x000bf^:ò±ìÈ,¥SqVOvì#sõ>Âçv2È\x0019L;iÃ¦
¬Û\x0013\x001a\x000eZ-"ÚÈ.¤AßÆ÷Â\x000fÁÇg{·wïowö®7¿ßß\x0005ÃÎZLºwF7\x0001[`níäï>?ÙÙ;Z\x001cÿãüd\x0003ÙÚf0ÅAúþQ¸ûËÏ_¾æô\x0017WwãÉçOM`±4N:xøÎ\x0003t*\x000fS\x001fö\x0017¯ßåÑô{\x0007§
¬®buSXm0zÒD1£]|Ç$NË\x001etÏgu¬ðq
lÐZ
û­IMíZe\x001eìÅ×
ê&ÀJ¸7ÙÑ
°òYüülÿò&üÅ¯®¯77\x0010¡z6ü%JjuØÑ[Aê*ÏîàøíéÁÎÏGG.y¯ó\x001eä-ÁÇgûª\x0005ü~õßÿµ¥\x0018×Ã\x000bF|Ô\x001eÉÒe\x0001
}+¾WÕòý\x001có¢¶p\x0006°äýÞÀ,ÉÈ)`r*e¶\x0014\x0015åÞÏÀÔa¦Ò\x0019SËgð1\x001cÉýÛû»å×WËÏËû
rH\x0008ïB¥^­R)\x0015ÚP1ÈW\x001fÆýóÓ½ÅÙN =Xo\x00034¬\x0002Ýúº\x0000¦¹â1Õ\x001a§>yÌ\x001bnë.\x000e½AÓÙ\x00120~î"é)ØÿÞç1o:Oí6ÜéÉKhl×²\x0007½\x0008 ¯\x0005¤ÎOË»÷Á¼j>AJ:ÆÄT7ÎRMv\x0010$Ð®?Üùiqú<ØZÍgÒÖ\x0005\x001a{á\x0007qÚW\x001a}¾m-!a\x0015Öv:è\x0003ZÎ«ü>.mý|sÏ·¯£­»§G.°\x0008ÛÁÎãí\x001dúÅ\x0003áëa~}dFWdð±\x001d
ìÔ0C2K\x001aó\x0012Ø0¶¬ê°d'©¶ÒÍÔ0RF/ÐÕU¹\x000e'ÏA35éA´I\´ ë\x001c¢)K}ú×æ¥ô¢ù\x001aÍ÷ É8,*¢)ç2¸Ï¸\x0003P
_¢Aq|;Z­\x001a§§\x0001MæVky§h²F=hà>âà\x0000%0è¬\x0014\x0007\x0007r3ç\x001aXU£©\x001eÑá5ÝOi1\x0017.8¾öÕQÞ^²úÚ.ië\x0005>i8\x0018{ü¶¦ò\\x0019®§£9]í'|ìØÏ \x0008\x0018¡Yh¸\x0017´ÂÏØOçªU=òÖãc·c^í¢¼¥§d¹\x0016ë\x0003óÊ`ð±\x001d\x000c¼	Ç ËnZ3k\x0014
$crºPãWò6~î\x0011\x001dræzxÌÊ\x000b\x001e@ÃIx	àuÖbÕü3ø\x0018È¾î¼¾ú\x0018\±¯;ø{÷õ2x=\x001bi½sd¯ëàý¢\x001bi¤À\x001e\x0003Á\x0001Z\x0013½g;¯\x000f_\x0006gìlç\x0000ROÏ\x000e\x000f´á¹\x0016¡3t\x0001\x001c\x001bEO\x0000\x000e¦\x0008^D\x0011Xpz\x001810p)\x0001\x000b¥ç\x0002;(]ð\x0000\x000cîB\x001c\x0013\x0013lÐßï\x0003iø_`qùç»O·\x001b£}á|ZÝ¡ä¶qO]½Wëöç?Î\x0003eø_à~qðÏýW'ÛHù*ð\x001eIãç	¨Ìíb°âX\x001b,zÒ&±,b\x0006*&\x0015äö\x001d{1K8î¼¹½ù\x0006ùê§÷0³sÓ¥·\x0002òa¾ZºUÁªòX³d×å÷ÁÎã·«~z\x000eã:7]-b4\x0015£ée\x000cn%¥\x000b«\x0000¥©[¥|zc×ý·~F_1úîuäQZ¦uh<H-\x000cõ\x0010Z¯\x0001ê`\x0004±[çB\x001f¹\x0010[gû)\x0011\x000c\x001aLÓSéx¶ºØà\x001eÎõKõrñû\x001aä%äíLÐ¥
\x0013n 1\x0002k½dp0QÕ¼Ä´êµ\x0007LÆö0\x0019õg É)Ökñ2hÿ°\x000c³hÕd\x000f¼î"R¨Oà\x0005\x0014ú¡¥\x00112GÍà\x0003Õ0\x0013÷¿Ü_û/ïS³Ä ,à«¬\x001f{»¼}^Ru\x001c÷ÏÎoþZ`aZÛäVH\x000eÇ=&\x001bèðÒô*hý\x0012«.Ïÿ\x0005Õ²eÅØÛÅùH(¬\x000c|5\x0013©àGÇÇ\x001f\x0019,vrWÀFII[Ð]9íA\x0014\x0016\x0017¾õ)ÿ]r(\x0007Ãa´pÚ!Lµjs~YF¦å\x000fú·øõöPaá+\x0013½X~LÇzëpz\Ú6¨å¨á¶§Gsn@+
à¼X¼<\x0018Í\x0016`¾~øðñ¯ø\x0008Ev:iì×·÷7W\x001bHÂ¿|W=!aq"\x0008fÇU\x0015Ç"\x0010J¸X¯OÎ\x000fÛ8ÂÐ»É6\x000eHn°CÃ(6V\x0004ç\x001dq'RÁN\x0007z÷Áþ~\x001dU[XLUÞª··÷ï>]²\x0018¦@òÁî\x0008&hM7"\x0016&¢\x000f°¾=oOÎ÷_\x001dnàùþ]¿Ã<Ò=yúñrôðÊ`ìÇ£ðð\x0018\x001eétøsªSãÚ¥\x0010Ð:N0L_T.×4AÂW\x0013
\x0008,éy\x0011,}\q\x001dLädÖ\x0005\x001a\x0016ë¾úh.ø?û*þY	sv{qu·¼\x0019åqpD<8^aÍ©\x0016%'ÅQC«svr¾wxº\x0018\x0019â\x0015××¿)¹11#&3ÁSÕò\x000ey\x000fË\x001b I'HXVIÞô¸\x0012G\x001fº\x0001(x¡Z\x000e·\x0018¯Â\x001a¾z	\x0016\x000fÀ¼\x0017TÊI\x000b\x00120åé\x00135¬S¸\x0014ðÕ\x0001%ÁMPÊrò)#\x001fúæ¨!åÕÃ\x0004YÚt.\x0014O³	ÂÞAÿú´P2õ\x0012ö\x0001z6{Þh{ 0o!@qÈ\x000cM»gIÍ;6té¶Cñß¼¸¦äì]êÔÓËKðùF±¸Å¤Báa\x0004K\x000c\x0001ka±\x0008k0õêéÁÞ\x0001¸{£d\x0004«ñ7jÉ\x0019ß?@\Þ½\x001b×"A\x0018À!²ÃX$
\x0014Ã­oÍ
98Ýß¤BJ\x00060:4Ø\x001cÿû\x0018»ßS\x0007\x000c¨\x0010¬:9îÿJsh\x00067Èy\x001dÓ%\x0001o2
G®©dhð±Ãüêü_c3h* å(×\x0003\x0004z"\x0016\x001au4\x000c\x000fQiÔÑt xõÑ]+ôw\x0003ÍÖü)\x0001\x0005õªÅ\x000f\x0007úøîã'ù>ÚÎa»d¹e{·÷_ß-o®FM"\x000eùB¦\x001b\x0016< \x0018[Ò
Æ\x0002¥\x001b¦\x0007öNÎÏö\x0017Çc\x0013x*(
BG÷A)Ìe\x000ePÁç>AyET~Ð\x0017ÛNå~ÿcy\x0011-j¨`¯½«wË»?ÇåÄÈäA¯§R7
\x001f\x0004SdïpqúÏñóíßDK\x0011\x001eAUyrÞ.ï¾]þz.\x0006\x000f\x000fUò¼ØÆµ\x0006ÎhKûAWçíâôíÁO'£\x0013.`U~ûxs\x001fõ)X	ðõúöæîv\x0017\x0018û]¥S\x0003Ó}b\x0010\x0008Ò4P.[]Z¯OOO6ø~¿ÚÛßÒ¦¨ö¯;ÇËû¯ãî\x000eãJ'^B\x0019ò¢â\x0014,)t#5\x001f2\x0010A[\x001c/ÎÏ6(\x000bæÙÅÅw¬\x0014ú#èóñúêëø&SÒ¥%Ò¹t\\x000cF} Â\x0017ÇåhçàåÑáÙøÆÜ|ýããÝw,\x0013zV\x0014Ë³KL6\x001c\x0006ñ2µ\x0001Yìr\x0017\x0005æÉFcÞÄöÌ\x000fe±svp:Ö§) }÷(þ\x0001k¼Õ®W¸IËÑd/Ê\x001cºÇØFB°k\x001cÝR\x001f\x001b¸=ôvÂZ\x0017¿Ýý!0|\x0018çhyqIeÃRÆÊôÞ(9´@)ã)à£ÓÐ»+´w\x00103ËÆîþýçýu\!ÈHní8C8ãÛ·Mqà3ÇêÆð\x0007Ïª¸BÙ\x0007!Ä¡k\x000eç\x0019¢\x001aoßn8ÑÞßß]F¡\x000c\x000f\x0006"¾Ýß]Ý[Ë<\x0007\x0013\x0018t)Ôév\x0019/ðvY+KI¼8?=<\x0019·¿²ö·\x0018åô\x0014øÚ¿½w?f\x0015]Q\x000cO1×^§Æ2:ø~\x0006½¿Ø\x0008'ÿúýóý±v]á·_Þøúé\x000f|EHo\x0007Åu
Zéî=PÂÔ\x001a`¼õÐN\x001d`ÂßC©g<\x001bÜ\x0005(¦ÓçPB9~Óùÿ¾û=\x001e°*ÒWñ¯°E××·÷ãQ\x0016ÉÓXsj}<´ÒhBÆ×`\x0008,ìÕÑÑÉù8Óåïßo¢G\x0003\x000féQ0-\x0013\x001càñó\x000b¹ýI\x0004Ú`½\x000b<À®	O¦¼W¸:ppÇC|üø×oñÜÓ&ÊèàÙòûÕÇÑ\x0013l=ô\x0013O¶\x0004\x000f:\x0012\x0003B	t×7fè- ì½á,û?ýÎ¾ÄÓ\x0014\x0004³Z\x0013ÎûË/\x001bd\x000f\x0006\x0004:E¢bYr'Å¸eØ½!³+,ÖþâÍÁ&éó}i/ì
\x0016q>+Cò¯oï¯¯Æ¢?ðDÏR\x001e°\x001dþ8}-7è¾>9?:\x001cý\\Ý_}Q|)ËÛ$3Ú9ÁÐHS!Áø£\x0008³¶ª<Ï;$\x0007¼\x0002Âí»«wï<ÖE\x0006¾ï//®î6\x001c\x001ah1\x001ae°\x0008¿Ö¥&ôàxb,W»ÊRß_ì\x001d£2Fðço\x0017æó¯Õå¾\x000c×úvû½sÂÒ½Æ25¸×n¶\x0010¥is\x0010îô	]ê1¿>üjQ\x0005 ±\x0015ì«¿6ÙWÚ¥ü\x0012	­Ñ0+ØÇ\x0008»®\x0008&Õ¿\x000eFA\x0004Õï¿|(#É)<®
¡\x0017NÒ$\x0018-©\x0000TCª\x0006F¶X!ÿSØxü·/S¡\x0004KY-á\x0007\x000bð¢Ó}û
e?_»Õ³áP
ôâ\x001c
R14~ÒU$àä-<É¾\x000eÎ\æ[7f2_\x001a[\x0010.»\x0010³\x0018xc0v.9ua£R&U@Ì\x001b@\x001cµYÙ\x001d\x001e\x000büïw^ÜÞAÎÈ\x00061#±÷\x0017øô\x0008\x0019Ä\x000c\x0013ø" \\x0019ôÆÉ/NN!Kd\Ìd,[bÙ'åJ,÷d°|å;°Ã \x0001´§ÝEàñ¡À*[ÆåÖ©\x0006\x0003òÄYu®ØSYªTj¹D\x0007"s\x001eúM¦V> W¥§Årf
\x0017/ò8ð\x0007ÏVXû·×·/\x001bÞÂ\x0004×$X-÷©ä+\x0006é\x0001Þ<ÜÃý£×{
ÏOK\²\x000bÆ" W°þ1+¬A>ì£\x0005¦J0Õ\x0003&\x0018´êI\x001béA\x0005D0'9É\x001bÙ\x0001¦K0Ýµ"%¶Ã9|Ñ\x0008\x0019\x001anÁ´s¸LÉeºvRä\x0013&1	vÛ|ò\x001fÞÈ\x000e0[Ù\x000e0.Tj²\x000c\x0016¦ ØHpïÈÂ^n\x0000\x001b\x0014`©Ì&\x000b\x001fÄ27\x0015càéõ:fObuÌå¯·¼\x0003h\x00036×\x0014ÓÊ-j×jxVßY°Âcê$Æ¼Xüt²ÉKÈ´¼¢åÓh!ªÜO\x000fu)h\x0010ÙÔN\x0001b\x0004U ¥am&_]\x0011¦b³_/¯îÆcÊQ?$ÿ&ø|\x001aFw$ý@·¤z!-G\x0004¿^\x001cn\x0008)g8SÁ>8å)¶\x001b,Ú]¥ñlÑ¥ÛAGmÕ¥Ì\x001b\x001dD,½Õ8sw±9\x000c\x0004EúJà+<ö¦\x000bCoÞÑ½{à\x001cÆ»[bB\x0017`î\x000fìsÐüP\x0016\x001a®qlA0ãÑNKÉ[ \x0002IÔhe³\x000c,\x0014¨\x000c
\x0017yçù\x000eþ`ÌaÈl²b]lã À\x0006P<,Ë\x0014n4]¡éN´`\x0014\x001b1Zïâ©ãÐX)Ô¦1ïÞÿaø`<ÿôö\x001e^ÁocÈÏ"~ööî¿ÿë3HÈåµå2õg\x0011^©	*ÍBÌ:Å@µQ±
ØÛÓ\x0003\x0008?\x001c\x0014'îôä\x001cÞÂOFÃ\x0015\x001e\x0005A{ñL
WxHúUªÇä¡\x0007·>Ýz¨«Îï¦Ðâ\x001cÚ
¤µH\x0010\x001cvù\x0018t\x0018Àí¥3AYàÖ\x00069UÒX¨ªÁ\x0014,mÜc,ÞÐ'G\x0001Õn<Rx\x0003\x001eôèB:4A\x0003~{ñà]»\x000e^Qd¢\x0006µx/Ã¨Y¹óñÂùÕò©.ðß\x0012®Æòi\x001d¾?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001cäRm.UÏ%xn4÷\x001aÀØ½jZ -\x0002Óm0]
¦CöâÉù\x0001R]\x001aZ\x0011isj.®E&AT)K\x0014\x0017,FÖkåjëûb0Û\x0006³Õ`Væ~I\x0008\x0016o\x0006WLqB\x0007ìdRV\x0004æÚ`®\x001aÌäsì\x0014.\x001e\x00060íyÅº\x001c2E`¾
æ«Á@Äk^1\x0012t\x0016ÆaÔÅl\x001cXhz0Ã8\x0017Øå\x0007`\x000f¿èò&\x0014Å6X¬\x0006ÃfvÄ\x0015óÌ»¤\x0015ÆÆâì0LJ¸\x0016ÙUIºZ0Eñ\x001bòpPò,j×l2\0¹,ö«å¾\x00121ÑV*\x0002ã&%Vç2\x0015-	~Y-ù¶l\x0002ãEGdZ69]6H\x0011Ù¼õ\x0002#RwzL*\x0014l¾ L¯c)&[º²þbâÜ/&T©\x001e¸:\x0006ÀôÈc¦Î¿ª>ÿÒóÜ\x0013ìbÁÇ\x000c½£ò(Ó©lY¿¨W0¼âQi<ÿ.	¶Å\x0019¹jIÁPÕ\x001a²¹ÍuÚLÍ©*Ñ&cmä{©4\x000cU¯bxÉâ\x001fÇ,\x0006Oâ¿É¡RéJÉT\x000cU­c(Ðb=§eäÂHÒL5ÇìQ*M)ÙÌPõ2Ã\x001bfÖs-?\x001c³Æg&âØ«¹¤d¨z-\x0003}³6f©·\x001ecñù\éZ
¶$ÌT½0Ãà\x0004f¸\x0000+X\x00179³æQuX)Ø¡Fh\x0019&å´"\x0011»$Ë<\x0007z0\x001e;\x000eL/IY]/eC£ÉZ£w=K^±0òÁÔK2V×ËØ!¢9a¸b4iÆ£êQK¦äÕ«äªÕ{3}\x0018\x001a)\x0010@úSKp«¹®C
®À}å\'\x0007ý­\x0019LµÁT=\x0018N\x0007ËQu-
g&¬Þ#ÉÐt\x001bM×£9Eë\x0002¶\x0004¤ú>Á\x0005\x000cVØGå9Åh¦fêÑm&
\x0004Å	ÕR6hñQ\x0011n1m£Ù\x0011\x001bÊ\x0013éâ¹ï¸¡z#Ì£\x0002ùb4×Fs£.§Y\x0007\x0003uYðg4ÿ¨´\x0018Í·Ñ|=\x001a±ó]¥ó\x0018áÑT§L+B\x000bm´0â\x001aÈ]\x001e~Ãs |\x001aèF¢£ÓcVD\x0016Ûd±Lk.#EÉËGÍ4c ¤\x0019»-;\x0018å­\x0018±¡2<À²M]ý^pY\x000fÎ\x001a{Cåò[0â1ÀÒ>\x001aíå#Íqñ¢InLyª#ÙUc¸Íq{\x0001U#ÆÁ`¯^¶¥ç@x\x000fãjôñe7\x0017Ü\x00130úNßF\x0011ÚÌõB×GÏ
\x0006¤ö)Ç\x0004Ìõ\x0018i>\x0004fÅ^¶%É&ëE\x0007eMÒiS2µ:G¶@\x0013±M|¡]¶$?d½\x0000\x0001\x0005S\x001f%XyÔRôÍô=mÇ>ðÒ¶¢ÓyO'Õç-\x001cÆ~YläiGþZ\x0013¢\x001a«µ\x0001ÞÛ\x0015¼·õ7Õ²\x0003£òÀàª\x001a¾\x000f\x000b\x0017\x001f\x0006¹7\x000eôJ\x001a£S\x000b¨3²hZ»H½:ã¸îjîjÌë@éå8³"kzõHmGëoaùä\x0011\x0007\x000fcd4Äø¤h"jGE_\x0005pzÕi\x0006¼Ý\MoîwÎ¯nïï\x0007f}[8tAñÅÜI\x0005ÝÆÂKcQß\x001cì\x001f\ìï^\ô\x000eüf8ÝÓ#à¤àØ"PÔ\x001a.)§ã¸ÔD¼\x000eÎ¶áì\x00088x½nàrû½¨\lVnÉgZ\x0008·Ú{O¯Ne~3»»\x001f(q>c\x0006\x00032[ój öÈ`8Ú\x0003¼óþÃ¶ÚzO¯Î`.¡>7²ÏXyL\x000b<üMæY\x001dQ¥ÛXº\x0016Ë:.XóBÐèS°\x0019\Õ1»½\x0008Ë´±L%\x0016º\x0003¯5\x00071¤2\x001cÒn$mcÙêM4¹÷i\x000e\x0012\x001bÚC\x0016J¯ªE¥T®Måj\x0017Ëù4Â+Å¢\\x001eI\x001bºIêf\x001cocù1{HÙzÛìâ\x001e6ë©èEX¡\x0015j±àä\x0014L\x0010ùyöY\x0010Æ4	¬«ÝãJ±b\x001b+VobÌÞ!ÄÊÿ6Ñq4]Y=
«ezê¥>e\XzH«å\x001cµ\x000fp» ÿ8©%E|­Ç²iM4:å\x0017IÈã\\x0012¦²VZ­r\x0017S\-ÖÃàl5¹\x001aÒ\®%±%kå\x0016öÂçÃeúµ\x0018T
\x0011F®×µ"ÂÀµ÷\x000e;"Si²iêZc\x001cyèî¢¬½XÆí9í@4eÜ²©I«\x00153\jéØ«Úco¤àf\x001cN[æ
< 	«ðÇ=jéÜ«Ús3Ò\x0014/-¹Wè"´#Ãª/£kéÜ«Ús¯i\x0014sª-ÒÜn"XÙÈ|\x0019ÕÒ¹Wµç^°o¸$%Üø`Z}±Æ{µtîUí¹×&pÀÉeÄû(ùma5DQü\x0008µ,ðü\x000c½­<úÜãJv¨2ß&©k5DQ¬?·\x000cÜ¤AO*B\x001d|\x0018R{\x0013ÔsB#\õjÇË\x00012tJ.AÉK	²âb>ù>ß%¶çÓÉÃ§éÃZ4µ®¦gÁ9£¹# î©\x0016\x0017s¼\x0008íâlïÍÁÙyâ{~°wùçÁå\x0010jã©1xh}ç\x000ch)¹ù1(B¡Á3\x001bàé6\x001eçxÜGÄÂÜ\x0019ÆzNùªð 3m:3N/çÙÓÞJ®ßÇ\x0002Ïñx¶gG-É1uX¼`²f½eºhâÄ\x0011t®MçF]\x000cîS\x000eg­m\x0006OE»¦\x0011x¾çG-\x001e÷Fr~aõ4\x001f=Ù$À\x000bm¼0jõ4uª{kRÉX\x0012+²¹·Í\x0004¯\x0011x±\x0017Gàa`E\x0011\x001e\x001a\x00074ÝZhb§õx¼ÆÊBYY>oòx\x0012X=ûXï(Ê\x0008"yüÑËOÆ7#\x0008E\x001138{ìM°Ø\x0003Ï\x001b/WäPã¤²¥\x001eÎ\x00113Ð	\x0002_=^\x0019à±úàîO¾Læ\x001f\x001e\x0006-@Ít>r»<°©³3ºqv·ùö÷÷Î^]öj\x0004ze~O\x0002T£\x0000Á§7\x0017°vÄ\x0008¦k\x0001K\x0001u\x001bP\x0002º\x0000+\x0018\x0017-hD3ºKôò6\x0019ÅgskÝ´\x000b Aóv
Ù\x0000Ð¶\x0001í\x0018@\x001c\x0013h\x0016;,©¡\x001d·{\x0000@·É
º6 \x001bwG\x000c¥ôD\x00146VP,`§)\x0005ôm@?j\x0005ÁÖ µ\x0019W0[AQÛæ\x000eûMøB/Ýá<,\x0007ø4\x000f
;ºÅ1\x0002pñÂ%)(F\x0011\x0006É²A¶$=5;vø\x0012\x001b¹KbP©$BÎß]ô\x0006Bµ KrF\x00124\x0006\x001bÐ\x0011 K­ºR+AÊFrèu©\x0005\x0014}ÿ~÷ùÓ7zìðÛÿ8ý2»IT\x001f'7÷Óë+ä2Ä%½|þÎáÿVTðäº´V\x0018Ë©\x000eÚîæY¥××	ôô\x001cMwo\x001fî'wÏ^^\x001d\x001füëàìÙþ\x001f\x0007Ç'ð½£Ëý\x0002FØZUË\x0008W"Ðõ\x0005UJ¢×\x0007\x0018½´<F\J´à?Eÿ¥1¿ß\¹¯]ëx·órò0¥Þy=.¥%B'°­GB«9\x0015\x0014\x00044vG9ÿÖùäûí¯Û®<ßy¹wyvØÓJo	qe\x0019K\x0010½RôÀ\x0006LÇ@D£(¥\x0000DtÜ*"\\x0011S¨\x0005\x0019q8\x000b¸¨y\x0011v{ðÖ¹jBcMÁa\x001e\x0015¬X"44'@{£ì6\x0011á÷úê}\x0003Ð\x0015\x0017÷´·j««\x0008&T¯¢Iþ>DÌc¼ò*Òc\x0002Ý²=DøÅêU\x000c¹sJp
î<­"µÔ!uî>ì¼ÂÁÓ×³i§à)§Äw\x0019ÿÔa¢2Ë\x001d,ùT\x0012\x000b¦h!§ãø|2ßt\x0019ñYµR'H»²Ã:\x001d ò:ZC=1¾í\x0011Â\x0003êÐçùÍHèS(\x0011
\x001aªSÙÈvw\x001aä¢¬\x0001\x0007ÐBâÅ·
¢9.no!áÔàÊ³hP\x0002&%\x001fFOhÈou\x001dAzËZ	y)²\x0005ëÓ³\x0004·\x001cÇí\x000eÛ[G8Û²V§ñ¬PK¯DÈ½Ia\x001dÍ¶\x000f$übY+Ä\x0003:C^H1nn¶ßâÍÆB[U+\x001c£ò»ÖÑ7j ;âÙ³ç·³»\x0017ÙU5~Ìßm\x0006
g\ÕjÁ°~ë4 \x0005Mgr2tLJÅ\x00167\x001cÿ{ªö~\x0007×è>ZKL\x0010Lë)\x0003Sâã°9åíÍçß?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9{þòèÕñ3ªC']\x000e#\x000b\x0014\x0019L\x0007;:U|jlÎ'\x0000OÁÇ	hõ|¬\x0005ëÆÄÇâY \¹z`%t0<\x0005\x001fíñ(ð1\x0018ù;º5\x0006:ÅzåtRIàSÐ¤\x000e­\x001e'·ÓÓlù<^[ñ­-\x0001cùÇ¯ë\åã¥8\x0019±kH^f}\x0018E¦\x0015²\x001cÞüÅ½\x000f\æ§/É>âóG¸?.=°\x001d¼¢¢¨\x000f0|\x000bË^¤§kÏ¹+f¤ÂñbêÂ¨îÍ×»¹û\x001dÅ³Ëû·\x000f\x00078~+\x000e
g\x001d\x001aÿé°t³D³Ô\x0002%]Ù±ãJñìèíÁÛw\x0007¯ÎÞd\x000e´ß>	\x0010$\x001eíÊê\x000cÔÂ»¼-¦ñWÑIÛÓSÐ	÷0p0ÒÓ0;d\x001b\x0012~td±©e\x0015´==	Y¢6Ì\x000eÆã~+`!5¦C%¿OÂ'ÄëÈ'\x001cÔ3õÿQ÷nÉq\x001cIºðVj\x0003
p«é	 Af Á\x0003\x0012²'\x0019(BjtS\x001a$té§ÙÆìàìãßÉ¬ä\x000fÏt\x00003«*³"ÆlæÈ¨\x001aIÇ¿ô\x0008w\x000f¿|n-r\x0006Ì¹ÉÄÑQp¸c¶\x000b\x001c'³
\x0014¶SbÔxfkn8
\x000ewö#y½\x0014\x0003ã\x00118y¬ÓÉÖ¨£ððDR\x000f<Ö\x0018\x001e1´ôG\x0017XDñføm9\x001bý'ÄOs@w\x000fÜN§Ì"e[¶A¤ìÌ\x0011à½á´±Âý	¯®öÍÚ\x0016\x0010&\x0010¥\x0016Á:\x0008\x0004äE\x0015ý½\x0014@ L0\x0000\x001d\x0005!(§y¸
\x0019øMÆâª\x0005®=¤X[-Læ\x001c\x0007A+¡ÄBZ©¥9»\x0013
# ½-\x0011Lu
\x001e\x000bA#Wê^V*õÂX¬,îå-Ú\x000fáñ\x000fâO³Í\x0013\x000f?­\x001bô4²=²» \x0004\x0000\x0011$«d$«ËóW/\x000fûëÓcäF	\x0019\x00047>ó®¢ãñ©¯ä(ÁÕÇðé~®ÒCä>o\x001dòÐ6?6jfY¡\x0002ÇE\x0007Ð<è\x001cí¾-MégZ%÷n³çW\x0000ù*áÖ\x0000#á\x0006Ù\x0006ëÔ÷!Kå0îi­[\x000edäúx ÖQ.d\x0004âdµTÐ¨·@öòu/\x00052Q;\x001e\x0007¶©`´Ê\x001bò´V|7¬ÙÄ=\x0010¶á.,QW÷_xéÓíæåÍç}Ð6l\x001f9\x0001\x0002@¬ÄÜ\x001dTä
I#;­/¯ß\x000f\x0001ÒÅùæåé»ù\x000cn!öx#Ú\x000cè¸[\x0005\x001b\x001d
<\\x0014qºãbØãùo#vÀ\x0013d±­\x001fNËøµyX>}íÉzÅ\x001a±Ç|y\x001b±iã\x0016ò×FZÄó\x0006¼O(}íé\x0015Û+Ä\x001e/é_îlþö/÷µGê¼Fb#÷m%±­L-*Ú´Ãbãd\x0013å
±sça\x0013¹æ¦¢$w\x0010Ö\x0004\x0015\x001cx{iuÜ<ÜFn)Qç\x0012S( È=¹äkÜ<­ÛDn\x001b­l\x0001à\x0006>¯aþ
¬ÜJäýYu+Ç!\x00137n¶osÊíör\x001a*Uñ)ü5NsB\x001e,ý¯~²·¿nè\x001f7oïù²9{üåöÓ¾HúuL¼»ýíöáoÏn>ývóñÊ\x001dé\x001d>²R{K¶cß¼\x0001&ÂÇ\x0018Ü,ùõæíå÷³ë7ç\x0017HÏÞ¾©ôþ$Qú\x0014Ñk+Òó\x0013Ü¤O6»Aá ñ\x001aÿ~7·9öìîãýÝç#[ç\x001c-\x001b[,¼¶²q'\x000cë\x0013\x0016\x000b§÷.ò={õüòÕ»/Ø\x0002ÈÄØ[\x000b ¤\x0001ËS\x000c1ÅÀ\ØDïs÷¿j\x000bdbð­\x0005\x0010Ú\x000eÜüo?rG4½X³wQ÷\x0001@ôç<ØÇ¹£uóùóíæÙÍ\x0007\x0000L¿Ò5Hë<h\x0003Cò,T{ÎNß½;ß<;}±g&£\x0000óu¢­
\x0018Ç\x000c u\x0018\x0012#\x0018y\x001f¦÷ÍÈ,\x0007ó5+E\x001b4*D®z\x0000m\x000cÓìòÀHþ\x0001ÕÞÁï\x0015h&ØÊÚèf°½F9ãS\x001d­pÝÞtÐ¡hüG37õüöçû»ãªçA\x0003ïÛ5\x000e¢,pKV\x001ad\x0016Ëú}X¿¾|µ³þû?~zøWÙzõ¥\qP\x0014;6g{st;Ñ$[æ¸àáÆèd#Õ`ÔdCÓÕûréAQðØíÈÚ\x0015°ØÙ÷E]\x001a²\x0015ytüã`ÓvWwtüÇÂâ§'X´È¶|îpJÖ«Oîw;\x001a\x0014¿°{Ò²\x001c-B\x0019$Oá\x0002bß#8ö\x0014ôeæveó·!ð\x00040¶9¼
E¦´·?pûà`¿é
sÞ0{
øü\x001dQÛ}OQ!M\x0002svÑñ\x001dºIª¤W¯ß\x000e\x001e2§é!3cº+\x0014P¢¦((ù:\x0014&BHq5×«Ct*¯Æ3ÍQ`\x0002¢ÜÁ\x0019©Y¨ù\x0011D\x0017Ó¯²5(LÂ´ÕçÉÈ\x0010\x0002\x0010\x0019ü¨\x000bëd+¢\x´\x0006-QØ¦(Pro!êíÆ,"é{\x0011ZéÂ(\[]\x0004N±¤ÛmñxÖ\x0016\x0014O5(|Â·½\x0017»7Ò½ÈµÞ¨Ä#ÝÉû(â\x0010üñé§_üöj^s~E9¢G\x001as Ä0>æ\x0012}\x0019í?ß[þù\x0015ôïâ\ôÈÕ¬Zëdy,ÇÁZü\x0001ZËuuàìéß»döîáñá\x001f8ÿ\x0002>Lh¦Í¿~ôÑ¬4\x0007(\x0008B<â\x000ey4îa\x0014*`L¾}átaÑd.O':ÚBÎäúqz2w\x0011O?ýùÓ£\x0019
9»ÿLt\x0004GdU\x0002\x0000S*Û\x0014ïå¾w%ë×hùæ>~³ËwÄE0{ÿ¸ùQßÌ$¹®îi\x0007Ð\x0001¯Ãõ\x0000ÖIvÝq\x000fLÌ\x001dýÞ\x0017ûÕ%íþÙù0,\x0010|Ý:\x0012\x0001\x001d| ¼%'\x0006/Õ¯à'ß\x0016Bøõß!Üüñ½2\x0003äø×&Go¾}üpÐÅH`\x0011Þ°C8»ýåþîóØÃ\x001cÙÈQ\x001a\x0003mÆæø"\x0018?Z(\x0007
÷3ÏÑîèÍ·×g{.Ç_â½{x:«v´±ªh Ò÷\x001fûOÈíÓ\x000b}p\x000b\x00165ÏiÑ?»<Oßÿ\x00109sþ\x0011r&ûÈdÛ@x`5ò4É\x0019§Oý\x0012A¹\x000bã¸\x000f
²,MÑ¦J\x001føò¥§-×Ç
»×Ô\x0001bIEc0IjxëKú¤aZ~¯¤Î\x000fÿú.\x001eù¡ñ¯+z<pÒß¤+»½rÏn\x001e?NÂd®G¢"\x001a.\x001bF©*ýÇ8¤W{·+]ïò/p\x0001ÇÓ\x0004l\x000b\x001cQV('ëÇD
ÈX½¿ñn\x0019\x0010;\x0000y{=\x001e\x00085h\x00174}|7Ìú\x000c@Ø+¥£´wñÙ\x0001@âß?Ù~kb{yûËíÛ/ëM^"ü\x0011Eéeg\x0005ËÜuÎçUÑæËó7çïÏßÏÇ\x0005\x0016¶\x00060¢s<yeÈ%ñ¸´ÕÖI3\x001519AZ`øjþµ
\x0006\x001düm¨GÜj)T\x001e1x³?ð_¢&¼\x00160È¶B>Q!N0´\x0013µ¿p/?ô¿Õ?°{ûð9=¾^¨\x0017R×R¼ä,½|ÇÊ¼QÃéæÛó«wéáµóF\x0017ç8¡à\x000eXÚy­éÝ2
ÎQæ@¦{à¿ßÝí§ú¿¸| ²±uqq\x0012LñFúêu÷Ú0y®Ss\x0012¿¸¼¾"±]¥­ÀùKÿU\x0004f+ù×\x00118\x0015¹+ÿ¯#0\x0013üu\x0004æå1ÿ\x000büûãîþ·!T\x000cC¨ødñ³$ü\x0003ßË3±¢Õ¨¸bbE 	²áåAÜ\x0003Ì¤ &\x0014Ê`ñYò~Ï[Ù¹øå?Ï¤õ¾»KÿìêV\x0003ÚõÄMF8Àábbt¼I:ÁÙ[ÿîÕ³Ë7»»\x000c
\x0008_§a ,³¼ ¢¦5FàïJï_ð{\x0000\x001fø\x0011oÕ÷
éæñ¯%!?¼6\x0011oG\x0007O]*C·ÇwÑ³ð\x001eü¾7Ç\x0018ý&}ÇÏÃe\x00182HÊM\\x0003.òüU°)P\x001fi÷R è±ñ\x0011>¶Ý\x0013\x0017ÁÞwÓp\x0015v'ó~ÿãö\x0019¶ ³\x000f÷G$T\x0003
¶Û1j­\x000cÌ8ïe¯ßsiõêìrG6u+þDBøhñÇ
\x000e\x0005è\x0011A]³FÞJv²\x0017\x0001\x0000k¬þ\x001dëXñùýã\x000f·_\x000e¡«Ø¹ÝÚ\x001b®
ZGDG×[;-sÑz./öüòúÙ\x001e's\x001f~û×?¿§ý}ä\x000càë
6\x000f?íjb\x0017ÜÖnaAÊûaR\x000e¼·Ün6PMïË½__½Ü+2ïoè´Ü\x001c+r²2HåÃ¸ËD6ÞË¬å-ôäCºØÄîx½FfÎ\x0000z:ó~#o£Ì 
4d-$ïïè\x001bß\x001d/±ä¡Á\x0003È\x0002\x001a\x0000æÎ=«\x000e(ÊÌJìàî×?ç
|ßÞü|X@3í¬IAÌÄóÌ<4¤|13/«½ë¾=}}¹;±Æ\x001fÿõ¥4ÿó_ÿý¿¥d5å£ \x0006xr\{ÉMD4\x0016xr\M³Õoþó»Ë7»åýõ£ÕêïïÁw~UÈÛHæý&\x000bE°HÛ~¤ná<\x0013[»oõú>CRÈï\x0007ù¿Ú_yüésÇáË\x0013åµÛiït\x0010\x001c²lü_\x001eÕoþû{eÓIÑá¯T0x¸¹û|Hgêü´\x0003PÇÙØÜäÓw¡þa\x0012Þ\x0006/)!?Mpº9»:}õng¨Rýý\x0007\x0016üÃ_Nò\x001fYò\x001fIN5ÓÞÝ\x0010;ãXW²)Ê\x001aßL\x0018ôôR¢RôIÛøÛçßÝ«N!(O2¯1*\x0001´¬OÂ¡ºË4Z3è*ØéÆù\x0010'Qg¿p!©\x0010¤ÿ?*é/\x000fwÞÿ0ão \x0007½\x001aæ8W"o(\x0005\x000e\x0018·\x001bK»~&ù¯\x000bßîy.\x0014ÒÝGòÿ¼ôïî~\x000f÷_e[ë%mzÊsë\x0014j¢¦çnW\x0015¨0-öHþng«Ë?Õí¹
"Ïï?\x001d7?\x0014£"J!uA¡=½ÍFvïÖç\x0017;÷·ÿãï\x001fÿåù\x001fÖG$ÄÁ3<aú×3>1zpRÂLÓ¨ÛÝ\x001cþþaÆúõýÝ/kÏ4Åwã \x0006M\x0014\x000b\x0007Wàyãö{Þ4§×¯Þì<Ôÿrá×~!ß9thfA\x001bd÷ 'îY\x001e¿T²+.]\x0003ØÇ\x000c½fæÃíï8ÿ¤©ñùýÏ«¹Ïi\x0014;Ò\x0000¬9á\x001e\x0006\x0017dæ5½sæÖ[<¿|½øÜýó§ð±ÚàuK"\x001e?JÌ½C\x0013ç9Äôêaº&j\x0017âÌaúyòVÓªëç\x001cxÏËýáÃ\x001fæócmxvÿ¯C6×Í&ÚhûÛXõDÚî¤ã5ò\x00010å¡ôÔÿÙ³zïÇ[óÛ,½\x0017Is\×"¸Èù)TaXI9òzò÷\x0006í'Y1+f¦ów{9n1|§m\x0001\x000cuú

¤q\x000bÂZ\x001bH÷ÓK	É0\x0010?»ü6æ:ãðÞyºéþöæñÃÞ@köÅC#¬cÇNLj`ûB\x001d;<\x000fÎÿÞUÅç§×g»ÂÃ\x0007üPú¢³Ï·éqwÛnÖ\x0012cö*Æ(,GÎ*îEÞLwöî<=ð_\x001f::hÂ\x001f·QAzó>~¸}8r\x001fF	@ïgvZ´4+üÖ&)ãüj·½ÿê»¡e
réÿ½ýtóÃíæm²w\x001foù²9ýD`6\x0017·\x001f\x001e\x001ew/¹Úa \x0000óÞô89é(lõ6½ú&7_]>;ß¼M¦ôÕóó7ï7§\x0017\x0004(´³«ë7³BüíæÏDÎ}ÿë°ü×ºiäìáþ#ÙÚ½]#;{HûÆi\x000fâçÒ6éeLrÇ{\x001bxÎ®.å¿2VÊó\òC¦v{¼É÷x}|Ax&ñ2ÂÁ\$+É(6Ãp¾yM¶ë"\x0018×ïÞ]î°\x0001\x0019\x0010 \x0007 ZhFÊ\x00074\x0003ÂÏd¤ÛX	\x0008K@Ø\x0001EË[Ì½Óa\x0008½\x00100z	\x0001\x0011[\x00022% Ó\x0003\x0015c\x0000Å\x0013>qÄ¬.xLK<¶Äc{à!\x0002i¿
ÑµÄè~g¾\x0016+ñ¸\x001ex¼Ô=íë`Â\x001a£dÂ}üS;@¾\x0004ä;\x0000"\x0006\x0015^ÁÂ´\x0011\x000fF«å\x0002¹Éõkñ\x0012OèG[ÉZ¢w\x000c(¼Ydâ&\x000b\x001bk\x0001Å\x0012Pì\x0000È§÷¹\x001e\x0001\x0011·\x0016o§GÚ\x001e$\x001a\x0004]	H«Ê«ª\x001e*Rë\x0008Þ¦w\x0001×&1
snr«¹©µ*·ª{øUÚ4vu$+\x0017Q¹\x0011\x0011÷\x0013PÓÄÔKa-¢Ê
é\x001e~È!d»m2­\x0018F\x001d«¤¿Y\x001dú|?¾Óðg \x0019kn¿©~ÏJJã!\x000c£\x0013\x0007\x000bkÐ\x0016âúù÷þöóOiÇ\x0019Þw·ÆV´¿£±³O+ßfÃ@í*\x0012û¨\x0008È\x0005s5¹u¤·5íë\x001a\x001e×ã°ìæìâý7?Ü|¼ùü%=Óä\x000f_\x0003*È\x001a\x0003"\x000eµq'`t m\x0016*¢æT»2Û\x0019FÄ¼$\x001d\x0010Q2Û2¢¼X=\x0013fª]Fa=\x001cf$i\x000fg°m¬ Í\x001c±õ1&y«\x001e¤\x0003¢\x0014ý +ÈøL\x0015Pz{È¶÷@ÄL¡=t¤O\x001co\x00042jË¨ÈÃ@\x0006þÛ!z¼ÿMýùçxê¨\x000fÈÖ}@´Üô·Ög\x0015\x000buÉ¶ñB&µí\x000bZÈÚî[ó{N+N¿;}y.SAÃ_eã\x0001þþIËA=fvØßy¯c¼\x001aòncó°'y\x001aíeÐlo&ôì:ý_\x0017¹Ð\x0012ÅêÎ«Ý¾&	¬µPï\x0001×òmò'ç­\x001bn	ô}S¯é÷3\x0010>ýë'õï\x0001\x00025ÿ¡ÏdÏ\x001f6/îùBõ#S~¤0\x0018N#ÍZ)Ôà²"q*Í]>¿Ú¼¸|ój/\x0013¢[¯d¤¨N¼%\x001b}MtW÷_þ<"pI\x0011ÿ¸í`ØùË3&\x00051k\x0019vþYs½yMdWïÿs>\x0012\x0013\x000cPb¶\x0018 \x000ehÓ¨q\x000cÂóã\x0019\x001c:_\x000e\x0002K\x0010Ø\x0016A¡\x001dGqFÃGÎBSSË¬\x0013\\x0004Â Lc\x0010^ºÿhy7&d\x0001Ã0x\x0011\x0008WpmA(Ù^â\x0016°0 ¶¦|[\x000cÂ |K\x0010\x0010­â:Ç\x0014ÄÈ $ãÞÍ'\x0016\x0008%Ð\x0016\x0004\x0011!&Üà\x001c\x0006\x0010ÚÊÅVóY¤% ¶ÙÁÂª¶(Òû\x0003¸#\x0016mÈ\x0008Å
\x0012ÛP\x0013\x000cÕMMl:NÒ[ïÓ\x001bþóáÄò!½~6ßº\x0008DetSë@ðj£õ´mïDnx¤£X\x000e¢2Nº©u"n\x000f[ÓÅ6'AT\x0011µ¨ÂNï\x001dX¢ºØºñÍÖWòy«}@Âoî¡ ÿÑ\x0002\x0005T7\x001bÚÞì\x0010"9§PÃ\x000eo\x0003
ËD®èuÀ\x0003êè©íÝ\x000e\x000e¥6Dí!»³D¦×ä^@u¹¡íå\x000eé!ÁE n9ngN\x0011	ßnç&[[VÄOeNq¡rN±U\x0004âx¬ÕÓÞ¥ .CåvG&{Ù\x001d%Ýó¶`KÅêjÜ^\x0012dZàä\x0014')è\x000f\x0006BúD?ÔÉÑ\x0003\x0008\x000ewë#HeÁÉ> Qªõû\x0012¢;É
³ôPJ\x000fí¤O\x001eCó\x0004\x00141.	
 9w­¦Wy,\x0004%\x0000lúùôû;0Ben\x0002()èi^ß\x0000L	À4Ô@HÏ\x0008|²°Z4Ëï\x001a'ùJ\x0002°%\x0000ÛX\x0003RmW2¡S) ü®ßµT@\x001cû0\x0010Ô±ã*FÛ]Õõå÷¥ü¾ñ÷\x000fÜ\x001eA²L¤\x0000)mÂ|i\x0001P\x0002\x0008-\x0015àsfØmÙ;G3ÚÍG­\x000b\x0000Ä\x0012@l­\x0001ÍKD\x0017
èÜA³«ãäP\x0000ù!:ú0ÕR\x0005.PÚ~PA
¹µ\x0000G7\x000e\x0014\x0001K\x0011Ô^¸­\x001b¶òh \x0001ïo\x001e\x000cÜUà?\x0018AåÈtCO\x0006T\x000câÖq¯j\x0014"IOháuåÉtSWfV \x000c§Èû\x0013ÇSc\x0006præRù+G¦\x001bz²\x0014æ'uÀD£\x001cËiÝä\x000eTL7õdÀd>*Ë
Ê\x0007\x0006\x0000vr1ÕR\x0000#ÐM=Á¶§%j+±Õç¬
Ð¿}<Ê\x0013è® \x0019R'½za{­ÊÑö%«\x0008 r\x0005ÐÒ\x0015P\x0010Êf(=Ã8G¼²l Ì§-\x0016\x0000¨<\x00014ô\x0004\x0010h¾Ã	´R¼µ
³/Ó|K\x0011Ôo²2\x000f£\x0011NK1ÚØù\x0016£ÚÕ{w°ø#,}aÞõã)}\x0014lö\x0003ì\x0001&7,EP92héÈ\x0003Þöåc\x0004z_\x000e\x0008P¸(
Ò¾Åã\x0011T®\x000cZº2ZT/\x0014Ñx HÎ¢/ÊAKgæ@Åç\¾$-z1¤DK¹\x001f@n"\x0003P=Ë á»\x000cG^pí£÷²ë2=&ùÌ`zY6PAå¡¥;¶éeÌKH½ý´Öh\x0010\x0004Ôás<Ê\x001dCKwì¢wMtV¥IjëÅ6\x00003ÃÎ:^G3÷\x001a[´A¤ß5hr°ôun®¥'pD3\x0012\x0018&5\x0019õåßÓx\x0018ÊbK3êÒ«\x0012X~;P
\x0000"ïwK\x0000æë³K¬è÷\x001fØÑ\x000f
oq+¬N \x0008(*°ªÅ£R}ÿëäÄ¯-CR²fLO\x001c/ÎÌK\x000b|gAQð§AÑ\x0011Þ"Ó¥ùFN\x001eh\x001a­<\x000e&Ã\x001f§'Çéæ/p´þþ\x000eÂÍ=þp~ jÍ³¿ß|¹\x001d7©\x0014CÊûPÌÏõº¨5Gx6\x0019!òrÌè%\x001bz¦é\x0000}{úþ|\§R\x000c)ïÇ%\x001eì'Pcþ8öîM¦\x0003Á²p(Lrk¬ÅcJ<¦~ÀðvC\x00143\x001eä\x0001rá\]Çxl\x000fýxÅC£\x0016\x0010e<b´¢ é6Äµ\	Èu\x0001Ä,\x000b¾¸=Qåã¦§ÌÀZ4¾Dã{ ±.
\x0001Ò	çûcTäå\x00034%ß\x0010P(\x0001\x001eh\x001bíÈw
VÉbÈd§é)Þð°ul­U\x0017ýX.²[Z¹\x001b\x0004\x000e\x0017X@M§f×\x0002ªÝO\x000fÿ\x0013hÍóH¶¢ÊËÉÐ\x001a9p~Qr\x0006Ñä3·DTÙ\x0003ÝÃ x¢g\x001cW÷Q×á+d}¦I¨¡ª+¤{Ü!\x001a?àe&ëÈú 1Ât\x0016h%"¨®\x0011ô¸F\x001e­Ìµ Ê4L)'8¾¡U\x0018ó£\x0019\x000eô£"7c'8ãf.Bä(½ÈbK\x0005UQ\x000fô\x0008{¼
´wwD'N\x00001Ób\x00024ÉÖºÒ*@e\x0015 U ½°Ï|XÂÑ\x0011j\x0019hCe\x0015 U Mö£'
H\x000b2ÅÌ\x0005	}&	iW\x0002ÂÊ(`\x000f£à\x000cðLo
\x0015pH\x0015\x000f{2ùq
´üðH@é%JPªF¼\x0011[ÎÕÝ~þt¿Ùhw\x0003¢\x0011¥±\x0001À]à\x0006 M\x0018fR1ü4=;wqùfò+Ë\x000e¥ìÐLvzKáC=\x001a'¥\x001bväXö½\x001eKñ±¡ø!w¸mÉÊäÍ\x0000éÓ»\x001d¹úCÅ7¥ø¦¡ø*IËl\x0017>\x000eÁåXö7Û¯¿£ð¨ø¶\x0014ß6\x0014?=øÇÕ\x0018éëçAOZ¢&=¨f2\(¾+ÅwíÄ÷4¯>JþRò\x00175¢\x001a9^x_
ï\x001b~{ã2µCzáó\x001e\x0013\x0015d\x0012\x000ehptB)~h'~ ~A¶;ÁÐ®a®Ôj~2d_(},¥
¥÷7î¥ï¶~«ì$Ý2ñuevtC»ã,õT®µR]ðVú\x001eõ®ÎÓCå¯.®nxsm:üãzjï*å7\x0016¥w\x001cæ§*\x000e¿:üºáé·ùf\x0002¤mÓà¥Q\x0004&\x0017Ú,\x001f*¯\x000b
ÝnòJÒvêí#\x001dsñ\x000e¤ur¡øÛ~Ë\x001a-Q\x0003\x0015x\x001e)%hívÔf\x000f\x0015¿²üÐÐô[b;ç¯ï¼PáØdûåö:Þí-jR¢¢&Õà\x0010e¾IoÌÇ[É´¬\x001c\x001c\x0006#Ù¸:ê§\x001fêñ\x0017÷\x000f·{×Ríû3\x0013º·Òõëér1NÓ³nëQ/.¯Îç\x0017Reù¡\x001fÊO¦?Óc\x0006_ñ&\x0008iÂßÅ\x0008°Dm5`yWAò\ ¼]I	¼ /A\x0008»û\x0014\x000e`J\x0008¦­\x0012\x001cG-Ø<Öï¥\x001c ¨Ý\x0015æ\x0003!Ø\x0012m
!h\x0019ê·nXÄ0B5âQÛ]=\x0010+!¸Ö\x0007IøR|ÁÕ	Svñ(\x001e\x000eÁ\x0010|[-x¹ÍnKJà\x0015¢(aùz1P"\x0008M\x0011P¯Zd\x0008:O_{-:pmt\x0010K\x0004±%\x0002Þó\x001c×
Jà6þôÂÉ\x0010ö\x0010l\x001d\x0006!ÏãNM5ÕBri
ÀÉ1²©úÅ\x0008j·ÜÔ/kmòM0Òýhsâ×ÜFø\x0003!TY7uÍéýÅ+é\x0016\x000c¶0ÕÐæ U¾Y7uÎzÉ\x001c1¤0!|\x0017(Þn\x0000¡òÍº©sÖ ÊbÂO\x000c©\x0017;N\x000fPùfÝÔ9k\x0013¹ lstNsÕ\x0000©\x000c×\x0002CåuSï¬©\x001bx@,álU­S\x0002azðb\x0008sÖM½³¦Ý\x001aÁ
4G\x000cÑgÏp\x0016&\x0004YþÊ5ë¦¾Y§ðy¦U^þiÒ\x0012\x0015ì \x0001[¢Ê7ë¶Î9\x0013îi¶\x0018¥§<\x001d£(*0¶kÊ9Ccç\x001c2\x001bëÎ£{æº3\x001dGK0Tî\x0019Úºg£h\x0017Ã\x0016"ósÁ¼Ã\x000eJ%\x0018êsÛ§3å¬\x0019\x000b'1GÛÊg=´0IPùghësc:\x0017$
*9K\x0006\x0001ezëÒ"\x0004k¶ïNzý37!M{	7!ÈÓ9ø=Ãï\x0007*¡rmÐÒµ
\r.òePÂwo`T.¼¡òmÐöå¹%õKqE&õK#FÉí*æ\x001c¡òoÐÒ¿A\x001c§®\x0007\x000c`¶~Aî3Î\x0013-Pù7hêßÒ]ËTéå&t(>oÎ
;W'\x001c\x0001+ÿ-ý\x001bä\x0010¬a¤¶\x0003*oÿu»rÂc¨ü\x001b¶ôoÃæ1fcàd{£Å*&·\x0001+÷-Ý\x001b\x0004RßÁôÇ\ÕY
v\x000fµÑ\x0018êÔpK÷6pCrÖÊÜ\x001eE
û\x0006i\x000fP=?±åós(#Ó[Ò\x001f<\x000e$áÍ\x001evó\x00031TÎ\x0001[:\x0007\x0008éáÀ4kAçwOz8gÑ&·ÁT\x0017Ú4½ÐÔ'ÂyI\x0008Zx²¬
¼é
]lZ5Õm0Mo\x000f8NéxÒñr¡£\x0010[º0Ù¯º8·ªó\x0000\x0018×Ûn\x0006|\x001fÑ1d\x0002Bù\x0011\x001d'å\x0007\x001aEéSz\x001cïøxÃKÏÌR\x0008BÑ\x0019°MúøPëãCS}\x0018éA²Ñn+C1Æ&µ«ª\x0014-\x000f¦úø_{K¨ø\x0014ÊÓAÏãk\x0010ÍÒà¹<¯}t9ÓÔ$[O®:6½ëC\x0006\6ùíë4s;GP\x0006|òuJCÕUs\x0000ýP4\x0007|ww\x0014#\x0018e¾QÖæ
\x001cü²yíÒ®Hü»W;Fm³èP\x000eÍD\x000fQÞr$:/Kï)ývÔN\x000e\x001cKÉ±ÝGw
Ø¨¤öf2\x001b$Löû/\x0012Ý¢V¢
R}¦Md<ìo¬AYT
»¤ÃD·¥è¶ÙW7v+ºÚ\x0016Û H\x0013-ìJª\x001e&º+EwÍ¾:\x0018¼L¢ÜúnAZPqW\x000fäaûRrßì£[à\x0002ç°ÿHj´:æ~ôA\x000f¥à¡Ù'·*ï{Å¡yj:ÆåïÚGwè±\x0014=¶ûæQ¨¥\x001cmsaÑÙ0cK.ëîH5ûìÛ~vÏFÝx÷\x0006ïjx<LöÚ¶ó¥ÎÑP´È.ÍEN©Ìpª½ò¥º3\x0005¯%¹KëÅ®íFmÜÕLqì7ÕíÜ©<\x0018¾;Sã\x001a\x001bóê_ÜEãuì;ÕÍü)Qáò]5&eÇÛ\x0002CØ\x0015;\x001e&{åOu;êÃÖÎøm¡z1ù»\x001f}d*ª9Ô\x0014³oé íãN{9îGÈÊ£êv.5­	8\x001c?ûö¦\x001e\x001b°ëÊ¥êf>FÞa\x001bÆ\x0000?Â1\x0018ÛÎÈT>U·sªQÉ\x0012\x0006¹\x001eCG<:tÊ£B3´¼Àl£\x0001>êè]>/nGæã0Ù+
Í<*¨ô:eÙ*z9òÐ!î\x001a>9LöúuÚÌ£R5B\x001cú\x001a\x000e}Ñ5\x000b\x001f¡ò§ÐÌr¼MvXlnä´\x001bw\x0010Køa²Wþ\x0014ùÓôUyÖ³I9È Ù2ïê\x00148LöÊB3
\x001aó ¡\x0013ä\x0013c1¯öÆ]ïÃd¯\x001c*´s¨\x0011¥ÛÇÑf*>3´»æý
É^9ThæPAÇ\x001cû¦K¿û61`v\x0011`\x001e&{åR¡K¥z¡¸%\x0005Ì&O\x001cæòÙõ.öËÃD¯<*4ó¨\x0000nkÜÍ6¤cþìüXKdÇÊ©b3§\x000cJî2UHÜý\x001cP»ú¶\x000f\x0013½ò©ØÎ§\x0012KXí\x0014UA2xæèd\x0012V>\x0015ùTc\®ª\x00055ð\x000cß][é5æØX\x0006ëo;¯jtÆøÝ]^"e"äïnþîWÅf^Õ8(Æ\x0014ä­å½gðë0Ñ+§í*±µH0ã<Ðªé-åd¯*6sªÆC2J0¤ãNK1?z}ô©|*¶ó©ÖËbGd59c\x0019¢m9RöÊ§b;\x001a@bHKËZ8¯¡·C9»8r\x000e\x0013½ò©ØÎ§ÒEüÙÃ6}*\x000f&³«Gó ÙMåSM;\x001aº[LG¿ºe¿DÓ\x001fÇ^TSùTÓÎ§:%ãÕDEùìVâ\x0001·Åþ0Ù+jÚùÔ¨¤ù,EIVùî\\JßÝ\x001cûÆ6O5í|ª\x0017&¸tÜjðøÝMÌÆýèJ©\x000b©í|jÌ²[ØN;iG?ú¼WNÕ4sª\x0008JºýÈÌäX&\x001e-{åTM3§jUW¶¥mª\x001ciprÞq×<Äa²W^Õ4óªÔZi·;ôÄ¼£ó¾íèÌ©¼ªiæUm^sà­²9\x000f©µ¬q8I¡·HöÊ­fn\x0015if[.\x0000ùî¹_Ãìjõ>Ht[yUÛÌ«ZÌ+ÛÉÒK¥CEãNãGÊ^¹UÛÌ­\x001a~bÓ\x001b¥%µ±mïÙE8wàOµÍ|ª5(Ý&è\¢QÞIä®wm\x00008LöÊ§Úf>ÕG+UF\x00079ëèAf\x000f;új+jùT\x001a@ça\x0000ã1wyªlÚéÍp¤èusR3jQÂä^H\x0019ÓÓ>ßÓptZÆV.Õ¶s©>Jøþ¹¡\x001dm|dâÑ¡­\ªmæR­VÛQÛ-/ÏÀ!,áïÑg¦r©¶Ku*³k\x0019zo\x00037\x000f\x00049ï!\x001eAµKµÍ\ªE%	\x0002«u\x000eUtÒ4»ÆÌ\x000fÝU>Õ5ó©TYâ\x0010ÒlÇQGz\x0002nÚ8ú¼»Ê5¹f®ÉñG7IP^x>u\x001a~ë¹Ê¶»¿T§«Û7\x0019HçÔàÍvH-E\x0001bdBÜÔ²HöÊ@ºf\x0006ÒGgàS\x0008ÏÄ¿)\x001eÈ}'GÍA²ûê¢úf\x0017ÕÉg\x0006Ä\x0003\x0018òT\x001a\x0005ÇÊ^\x0005¿¾YðK{9\x001d\x001eIÔà6ÈîB\x0016]\x001d{Ü}\x0015Búf!$í÷å¯®´¤­Ñ!Èt¯=ºEÉWao\x0016EÈµà\x0004C^\x001d) 72änî%ôu«u³\x001aÐa¡·Âè¦\x0016yPË\x001cýÙ«hÀ7\x0006bðBR^&`iÏø¥];¹\x000f<T×44»¦´sM\x000c\x0012Í.\x000bÑé\x001e\x001f\x001b?ê«V_=\x0005¹ñ$òWG4\x001eËT\x0002j×hßÍ§Å\x00144 \x0016cd-{P\x001d¡ùª\x0007õèg\x0013ÀS\x0008É\x0018·f\x000f¹\x0014Ëå&´9z´µÄð\x0014\x0001\x0008(Ç!eyã3«v6WÌòÀ¯\x0010´<E(æ±¤4\x000eTÍàè¼\x0001·>¹\x0007M\x0001`î	mÝ/3Ø\x0011£_$æ)\x0014Eµà¬zÈ"ùã Þk\x0006¾\x001aÔV\x000f>+OÊ\x000fÅøäË/¿ýù~Üé_¤2?ÿú·´\x0014æñÓ$±M1%?¿\x0001¨`9¬<)\x001b\x001fQí÷xyúþÛó×ß½\x0012\x001dJÑ¡èZv·\x0003Í¡gÑÝ¸6Èî
\x000f\x0016\x001dKÑ±èD¶"_}è \x001bE×ù£ï\x000fÜF\x001f=DùèxÀAÎðÍ\x001b\x0008nKÁm\x001bÁÓó5ð\x0017GaAS.z\x0011<î*!\x001c,¹/%÷m$§\x000b"º,åÂ8çA¢ïÚr°è¡\x0014=´\x0011=Â\x0019%×(9Uê#rZtã\x0012KÉc\x001bÉÓÃiÇJ\x001f\x001d¤ä¤\x001bÙÚè£ïâ³9Tôa\x0004qkÒU\x0013Ù\x00035/óIæ¹ò\x00031.;É\x0005¯}Q\x001bg\x0014!\x001f \x0013Ë\x0007ÝÊ\x0015¥¦¦\x0006W®H·ñE\x000b\x001bô±\x0005h\x0014««Iv»+}°ìE×mL:­\x001a	´\x0000Ü¸¹d7*7Â&G½2êºUÉ\x0007YþîQÓZ¸Qö _}×,Ö.É)>4\x0016cE[A?HÜuq{ÿËÍÃÇÍË»OkÜ×Òí\x0016\x0014äÞN+ô|ÉìâüòÍéÕóÍËW\x0017\x0017ó¡oF\x0001%
hBåÜ\x0007åZÏÏÚ¼¢ÆÏÆb\x000ba`	\x0003\x001bÃHÇ_â>ÆbzÅ\x0008éíê+`\x0012i}¦¢¤ê}4ÌÅ¦\x0017hcve!\x000c[Â°a¤h'6¼4SZhíãM]Â(\ë3sà>(a¸\x000ccÎº.DáK\x0014¾1
£ÄLQs­Öb§ülgëB\x0018¡\x0011Z\x001f)/Ô\x000c>D2Y\x000cÃd\x0018³;\x000baÄ\x0012Fl\x000cÃFa\x000b\x0008h©¿\x0007\x0002¸°b@ÏÖ@ÁÐµïkíü-2°u~y±\x001fèÙ\x000eû8*·¡[û
L¯b\x0011îÏX×\x0004=;¿\x0010Eenus{kÇ×\x000fé¶\x000b%Û	Æìã~!ÊRéÖ¦Ê\x0005k#mäËám£ºãºõ%§¥<Y\x001dÒdÍw<Îe,ÁêCë;n·§
ò\x001e\x0013Åâ\x0002è¹\×B\x0018Õ\x0015ÖWÜ '¾\x0012\x000eë\x0003VÉ¤'\x00004RGuÉ¡õ%\x000fÙ\x0003°e\x0010K×\]á¼\x0010GuË¡õ-÷VV8 Ï\x0011ñ¢à}µ.ÄQÝrh}Ëy\x001b]\x0008F\x0016ÛÒÌ\x001c*{tkü7¬ñå\x001böËÝ/ôo?\x001f\x0005#ýgeµv ¹bét\x0006áÔK×cÑ}ÿê
ýáõù»CÀ@	\x0006Ú\x0019cªñ®û\x001c²Éw\x001dgkiËÁ`	\x0006Û1*¯/
ÄsÞ!¿?Úa1%\x0016ÓA1N\x0018\x001a\x0002êÜ\x001b
éÖg¸+ÒZ\x0006Æ`l{0É¿ó §\x000e\x0000\x0019ÀW1¿Òg¹§q%\x0018×óÊøqihÝÊìïr(¾â;è\x0005©
yÔ¥\x0008I/\x0019\x0014_\x000e&`B\x0007½äÍ9ôà\x0005õ"«»Ãlbz9X]n$<dw	öA»Ù±·Å`2;äè1U\x0007ÕàÑ9×Ä\x0019Ý\x0015À,\x0003SyLÝÃe\x0016K²a{iP&´mvgtået\x00077\x001e*\x001cëSÙX^ÉëKÈ\x001eFëï?8UT\x0017Ò\x000fg´k%Ef\x0017IÒ«»/÷\x000f7ï¾l^ßüòÛÝíã>8)â\x001aáð?ÿ·³û\x001fn~ºý\x0006¶\x0014pV\x001b/ßüM¥'\x0000*Nj«k\x0015/Òß]½zy}õnóîýæõéï^_ïÇ%\x001eìæ\x0015FZ[ôc¦{\x0000d"\x0013ò*¯&w/\x0005dÛF\x0004(ÒÕ¹¸Ù¼¹¿-°lX¶Õ\x0002äM¶\x0006Ki\x0001iä-ró¨6Ó[l.N7o.Ï\x000b4³Ëg§/w:\x0001eJP¦\x000b(\x001d%ÀI p¨C\x000f LÈ &ÍõzP¶\x0004e;ij\x0018\x000e#Péô
i\x00010>iÉ=«Ë@Qw\x001aº'¤ùH³@ß|óöÓÍ\x000f·«û?o2r:½ØÀñP­Û..P^\x0016\x0017L\x0012½½8}v¾¹ºüÏÓ\x001d:Ë\x000e¥ìÐNöô¦áOVé¼ÒÐÉ¼ÔÁ2Ù±\x001d\x001b~wÌ\x0003oÁe
§4[ÇI.ËeÂRxÓðÃk2Nã¡1²")}ù<\x0000¯&¹Ú	ïJá]Cá!/ÿ£íí<\x001f¤Uöó\x001c+|(\x000f
·ÂånÒk1æÅÂ²¢:ÉTÑ"á·è­Q
¥7ùÜ8ËIz\x0004ò9ù¤×ÊÔR\x000fü>Ü`ò¸y~ÿÃÛÇÍ\x0014 &ùÁ.\^§TN@¼©-Fíó¹Þ<¿|öþüújó"Å§)HÜ\x000f	JHÐ\x0001\x0012Ä\x0018ó\x0000\x0015ò£*@^*4¿ôl
",\x0011a\x001f%)îKt¦\x0008`¶{«Z"2%"ÓGGù\x0015O:\x001d¹ëâ<EÐ\x001aD¶Dd» ¢Å7ù\x001eIî+HR2!ï\x000c]È\\x001fDÛ)¤#a\x000fC|ÍJm_\\x0003É|\x001fH·\x0013%-Éúë`Äj'-5½I¡\x0014zAb¦0ÒRV\x000c\x0002'%5µv±D\x0014» òVVÛ-:ØÌ°¸c+Ü
H9F\x0018½¬ê)Ð<GÖ\x0016L[\x000b>¿Ú`
¦:rè\x0011:À0Ù\x001a·z\x0012ç2±KçÓY©
\x001dtØÁ\x000f}"¢')&\x000fì:¢§¦ªàA÷\x001eL©'!
~ëlUK;®«ðA÷\x001f\x001cÐD`öMr¨
TôÔ\x0012R\x0015?è>\x0001
R¥\x0019®SÞ ®s$Þ\x0012Q\x0015?è>\x0001\x0004Ðñë\x0000"xaók£Ö`ª\x0002\x0008Ý' ²ë¬¤l\x001fò\x001eÜ\x0014\x00066½KU\x0000¡ûD\x0010c÷ÏÉçm¢¦!\x0004Tþ\x0016úø[²ýÓi×PFùSchiÇ¡ò·ÐÇß\x0002f¾CµåÞ²\x0011!½a\x0011Ô/õ.î6ùÕlÆu¾N6E9\x001e_\x000c²\x0006Sån¡»U9,²1Ê°&/N·%¦ÊÝB\x001fwKãëq{\x001c=ìn½Ê;A\x001fï¤3\x001d$=Yj\x0018Í6,gfY©òNÐÅ;>=+òÉsMO^å sJáOæN×!/Y\x001dîÐÈ¡°cYé\x0004¦ÉuÎ\x0019Põ¸.¯Û^\x0018yçyM\x001fvÈ\x0015°æ©
W(	+o]¼m Ý¦òj\x000c·)ÈÌæ¡¥\x0015ÇÊÙb\x0017g\x001b\x0000ó\x0016tâ\x0004\x0007ä@
º©*o}¼í¸YF,\x001e/?³
·¦ÙÎõUêÌx\x0017o\x001b\x0014J\x001dÆFO\x001bÒFL1\x0013¶§¢%¦ÊÛb\x0017o\x001b`\x001b³Á³ªÌ~5½LÕÓ\x0016»<m}(Üö#«u\x0014%5M~a\x0015=`è!h×Û4«)?mCÓ\x0004\x0004VÁ\x0003v	\x001e|òLy}£Õæ£P\x0008S×2|À*|À.á\x0003Ùâö6¡`R*/IjúhÂ*À.\x0011×îDK\x0004a>ÅÎuÙùÛ5L\x0015@.\x0001D:XBõE"¶yZ\x0006õHK-o©\x0002\x0008Ó%\x0018ÒürL~Ú\x000e\x0004\x000eL¿Öô6*0]\x0002+)_&N@XP\x000esèÚÒ*~0]â\x0007ëýöµ\x000e9\x001c'û-jjù\x00084ui½Køà<äM±IM¢%¯ò+pv®o\x0015¤*0]\x0002\x0008ë\x001cõ\x000fZ
^F~¬Ñ(îÖ6Í*0]"ôÛ9½¬t°\x0010¶¯õùfk0U!é\x0012BØô\x0010ma)æã.krCZ´ók­×`ªB\x0008Ó% 
D_\x0010Hu.ÑSCH¶r·¶»¥UÅ\x001bÃoR.?æw\x0018®ÁTù[ÛÅßZë6¬\x0005\x0013V¥£bÈnª§ÊßÚ.þÖaÆ4<2DOÛ]aËr
¦ÊáÚ>\x000e×j\x001a¦\x001dôäì1·\x0006QLYô\x0018ÜÐ³»µ]Ü­
)ºc\x001dY¡ÊH\x0001\x0014|Ó\x0001[w²õñ¶Ææå6\x0011Çì=ª!¤ÊÙÚ.Î6¹\x0013/ZÂ¬%£µ\x0004\x0010mµTùZÛÇ×j/ñu¹ãÐ\x001a/ýÓ\x0011[>\x0003måjm\x0017WK6ÜH\x001eY	%E²áyCWÓÊ­\x001eë¶ËcÝÄ¼ ®\x0015ïS·6\x0007ãºi£««¢\x0007×%z°Û/«1 ÑkÚÖáªèÁu\x001eó\x0019\x001310²}HF/Ï°Ìïp\©\x001e\èÁ¢é\x0010K<m¢§ô?¢§¦­ý®\x001e\è&%%Ý¯u®4Y'\x000bÙBÛâº«\x0002\x0008×'ô¢eL!½sYM.§]mÓ|«;Çû¸Û¤\x001bIøS7¯¸Û\x0010t\x000eòZV\å\\x0017çdÒ\x001dBÙûîrÆòãi~§Å
H¾²\x0010¾0ÔÖ!Û_·uÛdÕóÊ4ÓÒêùê6ù.·É(·Mqð09¥5®i?Äbÿ´
äý\x000bË·(DWT\x000eReÇ\x001c\x001dYz%Ð\x000bõô\x0019ý°ÓMâ~ºÙ¼¾¹{¸;j¦	·=\x00031JÎß\x0010C	7vL§¿Æ\x0001ºô÷\x0017§×§¯®^\x001d\x0000\x0004J Ð\x001cHà÷\x0007\x0007<\x0011ÁÔ
jÇ\x000cæ2\x001c¦ÄaZãÐQÊJ\x001e,­=\x001d[[éÖ2ÉÆ5@\	Äµ\x0005\x0002vã1\x000f	`A~\x0017%\x001có\x0003½Ë`\x0012Fh
\x0006Êä`AîO\x000bf«IK¶J\x001f\x0011cÐ\x000f\x001dµ0
»ÍvK~Ønù¼ùîæñ\x000f\x0012÷83;\x00140\x001f\x0003@r\x0008@\x000b¤y\x0002q\x0010ÌÒ³¿Û|wzý\x001fôóìf
\x00060 %txãÅ\x00137(¡Ç×;\x0016-E%
lB;®Ü
,ÿQaÇ4U\x0001³T»Ëa\x0012iª\x000cÏå\x0004C\x0011¢\x0011ÆøH#\x0014óÃnQØ\x0012m
?#
Ô>o£ñTI\x001baøI\x001au0\	ÃµA¤o¼}Á+ÙÝ¬<\x001a9SóÛ\x0017ð%\x0008ß\x0012DzqñBã(Èâõ:A\x00185ßA¶\x0018F(a¦ºðÜta¶Æ\x0016µlOç¬\\x000e#0bK\x0018éI?(ôKWÎËÂ óíKA»wl±{§\x0005
#[I\x0019é¥(û½@¬\x0014Î§1\x0017Ã¨ýwK\x0007NÝ¢f\ÈcBîöPÎ:Þjc¡Ý
×\x0003×M=¸\x0005¦
\x0005y¤3=4`»Yh~\x000fÕR\x001cïÓMßx±Û\x0001^·lª\x000c_ôlvÇuå6tS¿\x0011C+Ü(´ÿé³drwìÊ]£2¹º¥Í
JÖ=BØÂ1Ý\x000fÙgvm}:\x0000\x0007=0ÈPUùÑr%\x0018÷_ä¹ñòñîÃí§»Û£¸MºA99\ò$Ã\x0018§à\^¿GÇËëWgç\x0017¯Î\x000f\x0001\x0004% h\x000f(iM\x000c\x0001¥DJr
6L§Wâ	%Ð\x0001\x000f\x0018-
¢%\x0007¼¦Y\x0007ÞIn¦]G×\x0007®Ç³h8£\x001a4¼¨H#Ó\x001933
³\x0012Quât#\x0007éÙ\x000eC4\x0019h9\x0013D¡ÖÌ`üô¸ÒJ@X\x0001Â\x001e*J(UdM\x001e£UA±,_®Dd+D¶\x0003"Z.<fîöN
²FiÙeqºx¹\x0012Qe\x0016t\x000f»`4QP\x000e±²*ÖåX3Ó÷´\x000eP\x001eH\x001fí¶ê\x0000èBGr0üqT\x0011\x0010[5\x0003ò0\x0019 ¬DTY:èaé(o1ø/ÊÔÕ\x0018¼\x000cfZ7Í\x001a°\x0012Qí[{X:2\x000cÆ:"BÂñqÞlèÒ[­¡3Ê"\x0003 aR¤y´à¤+©(È@\x000fBàA\x0011ccËCgªCg:\x001c:ZÇT\x0015)^0R4Bp6\x0007\x000c°@G½\x0019NåL\x0007Wdh\x001f ?H¬¯À¾5
ý;­ëh¨ _!ò=\x00109Ç\x0001j
ÄÌQV\x0001y\x001e§X	¨ºC¦Ç\x001d\x0010(Î\x001eÃ\x001f'ü°¨AV¥ð§á\x001d²Õ¡³=\x000e\x001d=Øp§Ë"mPåºÓÍß+\x0011Uñí\x0010ÿ\x0018zª\x001c\x0001)Z\x0008)$\x001e9h¡©ªkd{\£äx\x00143\x00107.Jü£\x0004iùÎsáv=\x000c·Rå\x0008D\x0007Ï\x001bÒßH@7S\x001fX¨ºF®Ç5² ÆÅ`ÁJu\x0016÷\x0001Í´\x0003­\x0004TÝ"×ã\x0016¥GøVú£æ\x0010ÕGË!jT-%®ºE®Ç-²)þ\x0019¹uQ­ÀóÊû\x0008MÃg«¼ëáhZÑó3"DÉ¦\x0010UÖEEÛò\x001aY,ú\x0002Ä#
ÍMÍ\x0012ðdi
J9«%%P2ßÓ³ô+:e¾ÿRÅ\x000cß|éð\x001e'\x0006¨¡Ñ!¦ÁpãFzñ±C;½Ôg\x0001\x001e\x001b0Ó\x000fC¥Tîío´ÇïããæÍýÃÇõ8Ò±B*-\x000c@ÜvüHÇ(@ÔäÂÎ³ËëóïhßóëÍË«ç{0\x0012iV)r'jL\x0007©idíLÀ×\x0018æ.KáJ\x0018®-¨ô§Ç ò:úa4B\x0011J\x0014¡1
Ú®\x0019Îª(ÉQÄIþå(2¥ïx-Tc\x00186 2\x000c\x0014Oü£¬ ©L¯À\x0001\x0015\x000eh#y\x0013m2\x000eù9Å?âô\x001e¥\x00158ª+®\x001bßñ\x0018\x0010þÇ`¨ÅäÊqL\x000e¤¬ÀQÝqÝö£Ò)Ôg\x00186¯"	²\x0004&Áä¬\\x0001£ºäºí-G5¾üG\x001cN\x0006¦
­ëc\x001c¦Í©êCÛ[:L·\x0019i|ÆÈr\x0015-ÖÊª66\x0017ª[\x000emo9BY1:l]-èÞjÁa§bÆÃq\x0000>)èÒ\x000fÒxùâþñ¿ß6\x001a[¼ªÑ<KÂBi4­\x001c®N¿¸¼~öíù\x0001Ýï\x0019\x000c` \x0003ÌâãiÞVh\x0005t^ÊI¯ØV`°\x0004íÁ`\x0014RC"E\x0019¾G\x0019Ü4\x001aì\ßÀr0¦\x0004c:hFçeoÖ\x0002FÂ\x0014=íNÖ±%\x0018ÛA3>ß\x0019\x001fÄÇÛ!Òb0¶Ý1s%\x0018×\x0001ÌÀ"N`Ê\x001bF	ô[;×ö´\x001c/Áø\x000e`,×8Ó)Ób\x0013\x0018cF¯úV`B	&t\x0000Ã-åéA\x0012ó3\x001a©@ëy\x0016ÆåXb%vÀbhgT½\x0016I1<\x0015NÙ\+ób,ù¡2ºLÕ\x0001\x0016Á\x00139dF\x000e\x0019¨ÙÇå`jÿß!\x0000È\x000b2[ª
\x000cyí,©ûr0ÿ×\x001d\x0002\x0000¥¯>PhK\x0010'«ß\x0001æÚ´£©\x0002\x0000Ý#\x0002ÐÂü\x0014¨yÃf\x000bÀo0kZ©\x0002\x0000Ý!\x0002Ðy¯bðfë4=³F&ÕÌvÐ/GSE\x0000ºC\x0008,2óz\x0012«±\x0013;#
Ú·\x000b\x0001tå5u\x0007·IÄÌ|ÐÒ{@³Í^3Îò2/\x0007Sy\x001aÝÁÕ(\x0010n±`Ã	Ï*#M]³un\x0017Ï@e¡½u¦¡díY°9n/Í,YÕr0=ööÌæ¥\x001fHõÅ\x0004Dä \x0000pKÿ`4*ª'Ãéí¨ßæÓÿü×þòCwóìþÓ§Ûý{w5CÎ\x001cÎæ²\x0004æEqóVj\x0012Ó7ÏÒ/g\x0017\x0017ç;¶<gLXbÂNô«{¢ááë\x001cCïÜ\x001f²\x0006)AN ¶[}­Ëu¦É\U8Ë¯³\x0006-AÙ> 'BD2\x0007Hé©-zræÕ\	ÉuÒS²ØvKÀÅ+\x0002Òá3úmÀs
(_òôñd,	P\x0013°2¤PT¬ß\x00055iº\x0018+B	(tÒ÷\x0012f\x0013m´{c^·áæwS¬QR,1ÅNJ2ªN#\x000bRt\x00017Aá<ûü
Pù:Ú\x000e\x00166F¢nÞ	BmyÞä3\x0011Òt»ÆZTºB¥{é*Ó\x001eXmOäBé¼¢©-×U$¡;\x0012ÖÄYæ
¼Q2Åærþ\x0000¢ªb	Ý) n1å2\x001b\x0012ÏM\x0019\x0012VÕ<uÐª\x0008©ì®\x0019£¤Ì\x001côW\x000fâSl±\x001b63\x0000È§\x0019\x0014Þ2\x001aíIoi7bK¶£+8ÈàL\x0000×âªijö*kxzèEÞÞ´ÍÙÍçÏôÆJ=\x0002ÐP¹¹TçF´ð>i?)\x001a{£ÎNß½£GVúë~8PÂöp\x001c5F,V\x001e$W¢3ße3\x0016¢Á\x0012
vP\x000eÀpæÛÈêBôÉÓÒ±\x001e¯XÆhL\x0007ÝD\x001d=^å\x0000\x001dCÜ§£õ<Eîr8®ã:('ÅGR\x0004\x0010RE\x000cÂ}IS¦óÃÙáø\x0012o\x000fgÈEr6ßZ¡A\x000f2\x0012\x0007v\x0007Áb8¡\x0013:h\x0007u.\x001b\x001dWHQ\x0014'vÐ,\x0013K8±v¬\x0017¿\x0013¢¦?\x000ep\x00128ÑNÜÁh°\x0014N~`^Gõp;ò®õ\x000en½\x0013íøy&ýåp*¯£;¸\x001dï2Ë¥÷H\x0015¾\x0011\x001ec\x001dæ×b.ÇSù\x001dÝÁñäx¸\x001böçòÛ\x000fkËÃVù\x001dÝÁñxÊ9°\x001bU\x001bÍÕðØÐ²\x0015»é	í äGÛviÔ\x001bô]îT@h\x0018äèÊê\x000eÔíî¾ôæã!ÅhÅñ(7ÛF¶\x0002Nåxt\x0007Ïó¿
\x0007*K
\x001d,õÐ~Å«\x001a¬&qJþd<ó+¹ã©\x001f\x0008=^\x0008\x0006s*áÑ9
Mx´àçÂ^§2nÐÁ¸E@p{¯Ñ9Ðq*©Æù]\ËñTÖ\x0000:X\x0003\x001aJàrtZºJÑÒ
$îí¬\x001bTæ\x0000:V:1¢³Bz´m+ÁÙ¶Òåh°²\x0006ØÞ\x001aä\x000eÌì{Ì ¡q(p`r\x0006i\x001aÏÌ² \x0006S\x0002ì`
¢Oz\x001c&WJÎ\x0019\x0008aFº6í\x001e×XÙ\x0001ìa\x0007|\x0014\x001e\x001dUl´\x000e©ÔÎÌÔB<\x001dÀövº1¸S.(ÚCÃvÚXyÀ\x0019\x0013\x001bâ©ì\x0000¶·\x0003FE\x0014r	
¨¤G²0/QU;+_ËðÊ\x0012\x000e@kÅvm ÖrB~f¥¿ÄBÃÄ¡×|ÆIÞfá\x0001FjÉ\x001aÂ\x0003¢«³\x0012\x001e½Vn~\x0007Ãðà)¬dzÀ0bTsEq©QB\x0004»az¹ix	]\x000fLTF¡¬X\x0008&\x0008J\x0016BfþÓ?N¹zÆ
[Ê\x000bõöîó\x000fGµ7!\x0004+c±N{Ù%a\x000còfÁd
Õî'êÛWïíêmÊ0 \x0001aø}ÇL\x00136\x001aê\x0011\x0005î1	\x0007£À\x0012\x00056F\x0011Qz´-D\x0010F\x0018:nWWî~ñ\x001c\x000cÃ0Lke¨\x0013Y;\x000c¹¿ÌX\x0019h\x001a¶^\x001db2JË\x0010l	Á¶¾\x00161¯Xª¶\x0001+{ÕÍçÁjp%\x0006×Z
¹'\x000cy\x001b¾\x0013¹\x001dfä\x0017¢ð%
ßZ\x0013B;é­1²
0¡È[wíÎvÅ\x00050B	#´Wgm8ÌKUÉí\x001f~gOÁ\x0002\x0018±\x0011Ûkû=PQ39+CîÅa÷z\x001f\\x0005\x0018=jAI\x001bü°ÁP®÷v­éüðØB\x001cËÓ­}^Â\x0001b£Pâú#ä\x0005ºÓ¬ËqTÞB·v\x0017	´{ié}§\x0008$7Fí©ÈìAM\x001aNo÷ÁÐ\x000fgN\x000fû`.n7W÷?<Ü~Ù¼û²y}óËow·³ým\x001aZ3\x0018þwþvvÿÃMú×h\x0013O4<Ìg1=¶(W'Ñ\x0004y\x0007ðz*\x0012¹8ß\]>»:¿y÷~óúôÍw¯Î¯7gs}\x001a%((AA'PLÊcq,=3&f\x0006nÚ]	KLØ\x0005\x0013åF¨\x0004*\x000e\\x0011\x0003(ô.+jêi²\x001e)A> Q\x001eçb\x0007MÙ\x000cJeMMví.\x0003e\x0007\x0002[½Mè\x0007ºR¯~þuxb5 ó %8\l213hG\x0005B®¢&)®^½~;<®\x000e ]°Õ»d\x0000M!P­Y2äAfáLÔ>Cl\\x000c\x0001K\x0008Ø\x0014\x0013`-$'cQ¨a¬ÿÃdÚõ \x0008t;\x0010Øæô\x0003\x001d¤w>Ý!\x0006®â~\x001cs7Lä´C­~3¶bü¸Ònr\x0002öåõ«Ë÷DÁUÜý \x0004\x0004\x001d\x0000i#+p\x001dD;pCÒ¼¥V\x0014!OòôÍ\x0000úáæãÍç/\x000fó°\x0004=\x0000EIì%@#\x000b.i(Jb\x000fé?ÝPC¶\x0004d{\x0000\x00027òø8")Ö¬\x001f"\x0018áèIc¼\x0016+á¸.pðDñ
Rz \x001d\x0000\x0019\x001eKú,\¬\x0005\x0014J@¡Ë
¼YÑazØø(7È°`ºa	 j
ÖðdÏ\x0006µÝ£úöáöóÝÇÛ_¾lN?}¸}ø²¹¸ýððøË\x0011\x0011µ\x0002Wª&!g`¼30\x001a§þãÅ·Wçï^=?ó~szqv~õ~sq~vuýf?<(áAOx(\x000b1\x001aj¶\x000c\x000fäá\x0013'3åGÂÃ\x0012\x001eö\x0017d¨´g\x0005^¶É\x0007ÄàL	Îô\x0005çsnPgl6dÕÍï]ÎèlGt)D2YsÜÐIe*©®ÃÁt%:×\x00139Q[åI^Ôû<9\x001c'	QçKx¾'¼¡#Úó\x0019ÉVs²}$¼PÂ\x000b=á\x0005I{1Û\x0000Ãµ7¿z5¼XÂ\x001dá¥h8Õ4ù¹è].dé\x000eð¶\x0003KW=ñ\x0019räùòåtf{ù¦²Gâ«C1±2¼E·/fx=µWE,ºgÈb\x0015ÓbUÊ³¹¢4ÙQr$º*`Ñ=#\x0016«³cHwOò¬ÛÞ½\x000eøªE÷\x000cZ&ck:NÜF-ÜÑGâ«¢\x0016Ý3l±V2ð¤?£EÒ:?\x0012]\x0015µèaWÄ¡µÇà 
;Cl»=\x0012^\x0015µèasü*\x001fNt6k¯c¨Â\x0016Ý3nñWÕêSÕ×þ=¤«°E÷[|æK#õgMgÓ	UØ\x0002=Ã\x0016âáÞöÈáÔ
³öÚÛ\x0016¨¢\x0016è\x0019µ\x0004K$£ö\x0014Á\x000b¾\x001c·`ûË\x0007u¦¥gÜ\x0012BÁ zn[ð´µNô×ÞóA\x0015¹@ÏÈ%áSì\x001bPÉ\x001eO|09\x0018¼\x001bÞ4×`«¢\x0016è\x0019µÐÔóÖï	\x001d1ß½ÉmXGê®Z gÔtÇ*\x000eh\U'ÉGµw\x000cP-Ð3lNhçI}^ú0¿\x0019zà«â\x0016è\x0019·D#-I{NXõãö½\x001e:X*laN:mØ"µ®ÈtöN¨â\x0016è\x0018·h¥NtV_\x0010í©|ù&g¥CUØ\x001dÃ\x0016­bö{Zm/·r:§{XÄWÅ-Ø1nÑÊf|I}Qn_\x001c·L\x0012\x001d¯[°cÜ¢5ävË\x0018rÜâ¼Î¯\x0006ÛØ±c]\x001fê\x0018´Ð\x0000Lüêêyë²êÚ\x001b\x0016¬Â\x0016ì\x0018¶h9\x0019¡òJOe¿\x0017Û\x0017/±
[°cØ¢uÈÉ$R\x001f?\^]¬èiÛ\x001c_\x0015·`Ç¸E!Ò°arÓCû\x0005+=]:\x0004Ú\x001dO¦hÎÈ4ÓP\x0003oÏTNÏôtzhd\x0000z¨«g|:?\x0018&\x0007\x0005ÄW9\x0005ÓÓ)\x0018BÂçäA*?f;¤áM]Zïi9ðn\x000fðäâ\x0001nÕ×Þ1Ê°Åzéw\x001f®øt«ëjr:êH|y1=ÍS²¡g0O\x0018þÌum_\x0003ûþöI\x0015ì¶c/Ê¢A
ËT.4øÜ¹³ÜNFeÆ>YEF?Èðä«\x0004ëþá6áù|ûËí\x000f¿ùt\x0004&$¾/&Èò6«
#dú²¹ÑÃW	ÏåÕy\x0002òîüÍù³oO/fÕñ@\x0007zàq^\x001e®ÁÂf/FA\x0002N¯^	\x0008K@ØEAñÄË~\x0015×\x0010b\x0010jF°³Ô»k\x0000\x0012é¢¡Ì$\x001cÌvÍ%Êd\x0001ðs?k\x0000Ù\x0012í\x0001ÈÆ¼0bÛº1¬#\x001b47X¶\x0006+ñ¸.
2¼¿sà6\x000c¢\x001f#7HÍ\x0012|¬ÁãK<¾\x000bwGÉl5\x001a¡Åy6î5hB&tA#MzAÚ!ÖgÑÎäòáµxb'öÀ\x0013TÞ¸äUÞÞ2®\x00144KÖº\x0002Pny\x001a=ªêb\x000f\x0006Ú\x0015Ç\x00173¢Ìð¡ç¹ú× ªc.A\x0002Í²Òñ\x000b&ëHwHWAî\x0013%d\x001eql¶\x0016\x0015åw¾v³\x001c´k\x0010UQî\x0012&¤¦VxY\x0003Ò\x0006ÓK°×"ªÂ\x0004Ý%N°FÞ»>!\x0002 Zk4Kõ¾\x0006P\x0015&è.q\x000f945¸=t\x0017åÍÒO®\x0001TÅ	ºK `1s \x001bGK\x0007XC²\JÏÒã¬\x0001T\x0005
ºK¤\x0010s"\x0010?\x0000+\x0008¢ÈTÏnÌ]\x0003¨\x0015t`!¦B\x001dN&O4d|^5ÙÒ·VÁî\x0012-D'³AAyY\x0002Té©ã,/à
DPE\x000bÐ%Z0Q:}
èB^%ÓNZ«Ï!¨¢\x0005è\x0012-Ä\óéBåµ*1á\x000eµãµêBpÁky²\x0012{½Íñ\x0018\x0006­f\x0017\x0015­AT\x000bÐ'\\x0000y\x0013Q\x0000\x0004òh\x0005)\x0006h×Ò2@\x0015.@pÁ{yGx­óÚ\x001bÔÁe\x001dµ´\x000cU¼\x0000}â\x0005Î_Z1\x0012r¼\x0010Å2Øï\x0008¨ü+tñ¯é¨Érä`}>uF\x0018Åa[k
¢Ê\x001fA×«\x000e<Oû¶%Y¢¼ìqÅY.½\x0015°²ÞØÇzG)£yPÙÖå^­CC\x0015a?íaêR@õ*æ=\x0010ä\x0016©p¬]Ðúû?RøS1AüÇðG©·|\x001c÷)?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ywqúÕÉÅ\x0017û\x0008ëg\x001béò³M'¢§«\x000eAå\x001b\x000e¾`2!ªf®#4¶!4¶\x0010uæu&´:ÞaÞ\x0008ùÄÚÏõæëBô¾Aô¾\x0017Qi®Ò\x001e\x001b!dD.ÚV­6Ô\x0010a\x0010
a\x0010½ÎHOêØAoèñAAÝä7!ª\x0016Qu#\x0002Ê³gDM.EÉ\x000fFko×ØnÐ½Y¼ úIé\x0012¹:ßCD¯Ý*µ´\x0001òn>n\x000e\x0019PR¡Å\x001c<ó¨Ë\x0011ëpJDLá.ÄÈðL\x001aBô¬ü\x0001ÊT«)9XÝÀ\x0011±m\x0004½\x0004\x0011h\x0005)Ü\x001dÐ­4ÚÑ\x001e4¡÷\QÞ`}ÊÓA\x000cÜ®T\x001b3\x0019¹\x001cQÆààÏÞAäê(89\x000cJÚnä{Æ\x0010UØkpáÔê\x0008Ôº(nf(6ÑÌ´\x0001ëCÔ-b¯ÁQÞQRVF¤yÞÄùtæ\x001eBÓ\x0012vïçÀu:\x0008ÃªNrøVë¹\x0006Ï}Ð"B7¢'Ñ(HÒ\x001b\x0017å!ÀÖÃÑÝ\x001eNÜ,äÿk\x001b
\x0004XÚëTÇ¶\x000e±\x001dCÓ;q\x0016)\x0010%$Qé\x000cç÷h\x0005+Ý\x0007m[c{
NÜ+èxeBWkËûwü\x0013¬µ¶58¶×àÄHÏ~	\x0011h\x0014m9ûÔ¼²A\x000fb»mïvÿ\x001b¤\x0003\x0013\x0011I¿Ökv\x001fZ;¾Ý*¾{«\x0000+sÅ­¢(@\x0012»¼Sjé:Äv«øî­\x0002ú\x0019Ý\x0005á³Ù\x0005S\x0006Q®\x001eDß\x0012ö^W4\x0004ÊBü\x0002b½(\x0016QÉµö¦½¯èîûö\S\x001d\x0011\x0005\x0015XX/)è å\[æBã§ò\x001eâX4[ùöêèÅ§ïw4¾3°{-¸©\x0014xM¥Â[*ÎO^¼~ù|\x0006±Íô±	ÇÁUïä3êÉÇuvñæ8;pÑT;lã¦K&&vec\x0008°¬×	ó\x001e×r:ßÐùN:å2Î¡\x0000M¦cÁ\x000fðëfµ\x0011F¸¶¨g?\x001cVXÈ@ô[sÁQñU#\x0017ÅY
WEW#Ü\x0013\x0005¬=p:\x0004YæÕYsÅ+ëÂ¼ºNU}«p^5táa;5zñ
Y\x000bÇ¤¬µ¡Å\ïåxºzÈO3+ûðææ\x0005Xáá\x0004Ë'Ç3rÕÐíÌêÎ©EíÕ\P,Å\x0015´\x001cyU\x0018PXµîthéB\x001fóìQYý¼¹ó0k6\x00189_½¸\x0014ÏffèY\x0014%Î¹-\x0011/ÐyÄñÖíZ«}?»ð4+ªXwôD§XjÒ
±jìlOpZtÂ)TRóØ©Ò*Ãùå\x0002<4êº\x001fs¬«Zö7×\x000fWßm7Å\x001aÛ6lC/fó bçJÙß^|µJËJv`\x0015áÕÔÞ²\x000c\x0004z\x001fkçD\x001c\x0016rUw\LS´=\\x000bâ\x0001K¹ð\x00026
¢Ý\x000eÍB,ëk,ë;°\x001c·]Ãv\x000e>%<§ë¹Y¹ªeTMU¥iª*÷ba®\x0008«¡éÜ÷ÛIÃâ¹Ñý\x001aÃº&auL¢ÁË\x00167P¶hÀT\x0011S3ª¾Át\x000b¦{À\x0014°ëá$`~R\x0002³®4¾Ðs*{ÁB6[\x001b\x001b\x0011¯0hpÎ>þtõðÜ.®\x001f®ïùts¿½à3þæ.°ûr8Ï-(ËZðÎ^¾9¹¼ÌÕn\x0017§§\x0017ß¼>»ØUñF¶¡´QJ×Pº~Êx\\x00015F×ô@­+¼Ðd*R2ôSFÛëRIªèÂB=¶w®NÌ\x001c¤¬d®"%F\x0007{)äBÇrÅ\x000cMÎ÷°~(M³yLÿæÁè7xE,Añ2	L\x0019\x000e0á¦Ù<¦ó(/Ê¹\x000bkº\x001dðÅ®]änJÜä*S-aüYùR/¯þøt{u·\x00100ã5ûy\x0010|é+¸×`0b6$õòäß_¼Ú\x0007Wç[aü\x001fó­Ã9°Y\x0007\x0011\x001fX\x0007Q\x001bV\x000eIuÍUBu
v°%Í©¬;
\x001bY4É.z\x000f³²¥p¶³=pSB)M\x0018\x0008`\x001d½è5ÐÝ'y]×p¾ê¿\x001dáðg\x0007\x001c¾çg^úGæ¦ÒÚÔ\x001b±­ê\x000clVw±E§h;XQ´\x0014»÷a6\x001c°\x000cN
ß\x000c\úÝA§¥å;cJyÍ~©fÆ\x0005;\x0008gìÐ"þÁ[²»ßw\x0015M\x0011ûÀJ\x0008Ê´R¢¨=Í§\x0016¼<yõ·½PÌe¢JB*\x000b¨\x0016\x0003O©Äìýz\x0019l är¨x®Ò[sÒr\x001cª
ÔüÍu\x0019k¨\ÇPù½=0HÏXRö0ÿr²*4T¡Ê²¤r(÷DT\x000cåÇ¡ Yê°x­kl\x001eËufÂsÐ\x000b(ÂSÃK]jÕV\x001dTÀ]_\x000cj<9:øaÉ7½×;±\å:°ââø×hºh°hµÇó}x´Tõô\x001f±Tûô¿ga\x0005ÞÚF*Ø®°ÞâW,Àª<[Ä2z9\x000e¬ÀOùÒ9a\x0019t³òEXÈ\x000eb\x0005»\x001c\x000bkó×Rn|	®\x0005?\x001fæ]UçéD¬'y:{°,¾Nfå\x001fÇ­* ÁT\x0005n^5o\x0011iì{J±X%e´©¸úIËo¯\x00010ßb\x0011kÖ\x0016þ\¥mÁ\x0017\x0011:Çç\x000eluº`Ù\x0016kùÚB,j¦¥@¤CÄ*òMz¿\x0004ËµXËÏCÄ¢%¯ è;ÇZ? Çwbýæ°\x001fR\x0003+\x0014Êö\x0015ÊhÁ°×¾]ò¾cÉkà^,Ê:\x0016<Xe´ìðA\x00127
VÏ÷\x0014-UÑÓR´âK\x0000èù'eTí÷\x001d+ÞH[(Í½\x0001#\x0016§gÏ}\Õ®xß±â±m±+XÔ¡(b©5nM}»â}Ç7¥H\x0002±x#+nÜ>öì	ËÏ\x001e¬Ý Ö§Ê\x0018¾ð8ÇR}ÐÔ½ôa5m]ìÓ¶.{F3BW2I£\x0015¸`ÃúqªÖ<\x001eó`úA\x00129§\x0015\x001føra­\x001c6¦V7N ÕË@4\x000f¤- Q3-°'*áÍ\x0003´×Cè¸\x001fJ#¸p\x0014¹XÃ¶\x0016¼1rx\x000eÁ6?Ï!¥½§[5õ#¡F¿ØGeØ6 >RÍäG\x001dPÞrud	`/ù&¦\x001dvihfÐ\x0019\x0017DEX^ õJX\x000b~´_¥Z¬\x000eåõ3¢r\x001d­Mö¦óÃ{Ðµ«Ýõ¬ö`°Ùa¦2T³\x0012þ:ìæU\x0017aé\x0016K/ÇRÂiÐ\x00014_-<\x001cHØ\x0016\x0004\eMèÌòM¨ð0ä²	Ïíx\x000c¥fÏ!4Q6ü¹JIê]©CòJå<SÙñ\x0003Ýb-?\x000bQÞRb¿ÒT R5_µ\x0007Ë'!­ø£	i=\x001c]~¸¹º½½ºÿvû³P¼ß\x0014\x0011åå\x0013QªE?£¾<º|qvr~~rñÅÎG¡¨\¨\/b4ï\Ú}è5¥Ø"-­ÂÜ]£±ò¢#cãD/dä
aL\x0011\x001d\x0001\x0019V¥ö ÖÂá8ÓM©Ó²©\x0016òY>ÏMÐü¥tÑE±³éÀ]'2JÕ=AQÉ1Þr\x0001¼REÇÌ:ÿ}¦4ýóª±¿:Õ+UT\Vïºª}ÚAu\x0019#8j \x001d\x0017dmÉÝ·³çY\x0017¤imé6>\x00104\x0016óÆ`\x001eHé\x001d/I9[iÒ\x0005Y%½"dôº\x0018Ò\x0002Sw\x0010²0ÎYï\x001eÆZ¥\x000f-¤ègÄ(\x0011Í¶4|òÅ?,Çkýlt»\x000fÒ·¾\x001br¾\x0013¯e Kq·\x0017j5d»·ÕÀÞÆ²s²"Ó$ÈÒ"ÞÊÖC¶\x0007¢ì?\x0011¥ÂúÀüa¸Ñ´Ä\x0007zÌ­\x0001è\x000c-dÿæ\x0016~\x0003©9ü,%{Ô\x000e`íæVªÝ8ªãüO@ª\x0016²ÿPü\x001fXº\x001dIÝ=(ôGO3ñx¤\x0019)8jçækfº\x0018m»¹m÷æ¶ÑÙ¥\x0018\x001efRxXxôwn¶ø²\x000bÒ·¾\x001fÒ$õ\x0010í¬B\x000c\x0018:f[>{é\x0016\x0012ú!ý\x0006Òòsª0åÀq³\x0001¾\x001eH#\x001b×Èn×¤ÞµXÒJµýIã\x001e1W;åÆ4¢1Ý¢%5D\x000bÒñ²\x001e¸b9^\x0013W3B³µ
toíxÝç¦`ø¾é©\x0010Ós\x0010\x0002¼Y\x000biÛÉ¶ýõ¬^ÓÛ°¦[¢õÅ\x0000Á¼ºM\x0017¤n¼r«»½r­MyD\x0008@^¹uP=`¯u&£k }÷q\x00137\x0006_oâ^¡Ê\x0011\x000bÞó»Ðjç\x0002Dc@tÛø\x001bÝ4Û6ÐûBô$ù¾íæsEû }\x000bÙ½·\x0015Ößòl\x0007ÚÛ\x0000\x001c÷#ºöH¹i)Iû\x001bÿV¯\x0019
ÜÄN\x0005KÇ·õÎ¹ÆV\x00061ª®#NÝ\x000cæ¯¯\x001e??`(¨¶osÃ¹\x0016`¸HÒzi¸ôDÔ	~u\x001aó×'ïÞ^b\þ»}¸uQ\x0014U,æ«2Çðþã¸7S\x0008µhÆ\x001aÞê¢Ã+\x0007y±å\x001dõï\x0016URÊ=l²ÄÃp]ëÆpÓL\x0012ÿ	r­KU¹®&\x001cjxCÃ\x001b\x0006yãuÍS	K4	4º®ÀZ4á­5¸Ð¬\x0006\x0018^
¢tñ¬Wl£Ì¼Zo)mèæmv\x001bî¶èr"k)Ôª\x0016Ì+Üa¬iÇ×\x000c\x000f°L\x000f\x0002y\x0003wfsÖ\x0000\x000f°ßRÑ\x000b\¶!0¶ýÅ¡\x00051`¼\x0004PÑã\x00155\x001bà`47çVuáú\x0018°J*Õã£rO2±±øû«?¶\x0017\x0008JÏKV(y½ù¡\x001bO«y}*,#þúäßw\x0008f¸ª~\x0008³9'ª\x000e;á\x0014ÞCs\x0004fBSúst_¨CÏ\x0017æ,s
ës\x0014ûpP¯{®~Ñb>_h9]hè&¥ÿ»éâý[°cÿ/~ü3<±b^\x0016t1]:\x0014éÂDéd7]´äM\x0005 ^ÏÜ4­óÏ¥KÑjÑW5\x0011}ÝÏ\x0006]Ò\x0000,8\x0011,K:Ä\x000bÝVQEtª\x001989ÕÙMç,÷\x0008¦¤\x0005GíÉ´²Û5b\x0016áU²\x00047%Øç9ô\x0011L)º
\x000b´1§h\x0015mÌ´}öD{OÉ\x0016qj=+«KÉb"qå­\x001b<hW\x001eô­<­Êcn0¶\x0008¿kÁxv^xj)^Ý%'â)Ý÷ÿyôj%C5Q2ÜgP®#{\x0008Á\x001b¬\x0005Ix\x0010Ø¬Ìg.§ó-ÝD=i7+\x001deÒPÀßÉÀ
EZ\x000e\x000f0XVWùY\x0002Õ\x000bÐÑº@ð\x0008÷ßÿñ'w\x001fn®ïî®^<ÞïP\x0015±Ü\x0019Ú*\x0014¦´\x000cE"õÚFÇ\x0000ÕÂ#âÑÉ«\x0017g§¯^\x001e½xw±Ôá\x0007ÿonþÆ1þl\x0007òùÕýÿµc(\x001dÆ\x000cÈ\x0004Zn|ï,æþä6[gúùÉÅéÎ±ÌUÛ7$\x000cO]ª}¡\x001c¾Æ;CÙ\x0004\x0018$b\x00014·Uwg)¡j	\x001e"û\x0008QØ.Ð^6\x000e£EÐ²\x0010Ú¢&½ÐVïxÐÊ§îË^BÇbÍ6U\x0005e\x0005\x0012Lr`ÏtÛ~Y\x0008X½E  jmö\x0002
O]\x0016[½ç$\x0002\x0007¦lh·Mg\x0019 Tq«\x0008?;\x0001­¢v\x001b/MþïàÍ\x001cpÝ>J^\x0006	íSø¯\x001eB/\x001a@?±Ùû\x0000Q\x000fº\x0006¬<ÉFXºt*½U\x0019m! i\x0001M? à0_Ð-M<ÙáÒ+÷±\x0010º	£e¤M\x0010Ê*\x001c6¤"B9_¿Ð¤Håê¼ ¿¼¹»ÞzI²ä\x0006\x0019\x0012Çd¸è¥ÒãMT¾<ÿót×Å<ÕÉæîØB\x000fð»i¤ÕÔ\x0010»Ø\x0012U0_
V¹cçzÀ6qZ\x0019Q\x0014\x0001ÙZ5[ý»¬\x0012\x0007d^tÍ¥å\x0014\x0019\x000f,4\x0012XYÆÎ+Ë.$«Ó ¤Aî\x001b4Á\x0015Ó\x0012]-
\x001a+\x001bÛh7¦Z4ÕV\x001eÝ¤\x0002î\x000c§óõ¬­\x0011[&[4Ù\x0006sd\x0004(jL¯%·\x000cè+Ètuº¢Õ\x0010¶\x000c£é\x0019Lþ´üàkæ¥\x001eösy^«*Ý=º{o®\x001ePâkQ#SÜ\x0002Ü)IÆ¥ú)¨ºV\x000c#'_-løCp¡\x000b-¸*w5ÂáúkÐ©¤ [ÕSã¿³=¥^|ÿçÿý|uóÝÝÍõ\x000e)%\x001a³\x0015eùUD;>­ÜlÍþ%^ ß}õêìt§RâO\x00179¥õ# ¥CYéZ²\x000c¹)[×K9ÿªÛE
-)\x000cÆ\x000b/gfa£sC¤\ªäçµª;IhH\x0018!uE
\x0004c	Ô¢È³<\x001fßè$õ-©ÿ\x000bBK
AR©Ñ¬\x001aî¨ãI»Û­\x0015<ÒÛz#ªp&ï^\x0007Éú½RÎ? Îûù®\x001a\x001e\x0002S5Ø¤]ÃN°"wäâÀe/\x0010;Ù°Þ¶\x000fáï\x0005\x0014¿ª²@\x001c?ÍÉútÿ~ÇÙìñ)\x001eæ¹FÂçð}R'M(y}ñ|çñÑt¦;ÑÊ«¶n´f6~î.&«;yccºÈ´ánÙ\x000ee2²\x0017ôC2½F.fsÍ¨¹¾QÎ3] \x001dºÙÝ\x0002¬\x001aÊl³B\x0014ÑB\x0016úÐâõ*Ä\VtËñ\x000b\x0016W
zK¢Õ"´Z'7m¾)«$)\`gÁæab¶±Ïb¸J[\x001bá\x0014ôÀ9où)Á£Ôfq\x0003I¹Æz°­\x0008 ÛÓ¤ò=lö»^8ºzÛàÍ­\x0013^ÌVw¸l\x0010ºØ°/\x000e[tWr
sÜ\x0015lïÉµ\x0018Îù\x0006Îù¾\x0015ç1k<Á\x0019Å\x001dUr·\qÕ-\x000e"YÛâ`Á(\x0019¶® ½`\x0003¯¶mal¶1!ÊvÙ\x0010ê\x0019ùâá-5$q\x0016\x0014·Õ°aKÅ2¶*ÔlOb={Ø Þs5·üð\x001c\x001e3
#[5pUÊ0Â=M\x0019Þ3p¢Èß¦H7´ÜU\x0003f_ÔÃµ#çûFµ\x0006Ò¤æ#Ë°f\x000b¢­TmZ'Ät-8Àx"Ù\x0010gI~'®BÎ\x0005~öee\x0001
O¢ÑOµGÜ«ûûèï\x0008\x0018Å·\x0014]	nÃÇ-wS\x000fäùÒèï|ÊMU©?F\x000c')\x000eÿzÄZó="Êi;}Ø\ô\x0010ñõÇÓ+i\x0000,Ñ[Ã\x00172*×0*×Ï\x0018];m\x001f^Ä³°zÜÂÜ\x001d\x0011åëWB6ÏöaîÙþ_:Ù\x0006Ò}§Rã'Å£/¯îwÄ"ñI+¢°óÈih©ë"U\x001bÍ*u\\x001e½<¹Ø\x0013'MlUþqd³¡Ma§ÁÄ5QØX¿Ôé0ïK-cOÆ­wàþÁÉ4puÛKxù×ë_®ï?o0c{\x0017òX@Ð	6)a·ÀÍo_¼`szñv\x001f]Ýì"ÒIÑÕ\x0005"\x0014ÇnÙÂË\x0005ÌÞ|\x0016ã)Õà)ÕçøîãM gÛø±Û2/P»\x001cÎµp®\x000f\x000eKØ7°7êR³"¢WüY\x0017Z¼Iûä=xrãZRþxºLí|þãb¼êrxz\x0012\x0010Û6¼\x0017\x000b¤\x0010ë\x0004¿ØÆ1Gµ\x001cÏ·xî{FÏQ5²\x0007nå#ùáæ[-FóíÈù¾K$Yß0\x0004àuçç5ÌâévätçÈEWn!/\x0000A|y)¶6s^\x0007Íè=é\x0011±\x001fOi
+zïIÊ
\x0016lðÔn`\x000bèTÅÊÊMQÇ²½x?¿úývG¯QÌªeÅ4Ã´ð\x0004wê\x000eóMã/üí|·GÙBÃ\x0016zØâË @\x0015-¸¸è¸IÝ"¢´­~°PO\x0013\x0006ö²\x0001u:0(dBê%\x0001,¿ù¹Ù¾ËÙTÃ¦úØ4GØA»gvk~\x000fn6)TÍ¸IÕ7p©Ù:×êQ\x000eº\x000f²Ô\x0016ù°ÀR6Õ²õ
\x001cêÐPï\x001e\x0000öã¦å\x0007\x0000Üý+à*ñ:3Ð\x0005'JQ\x0010F\x0008HÔ³jªNJóCp\x0016á|¥S\x001f9þ<~s{õ!W.½ùtÿùêæv·¤\x0016/Y]O*>ÀtÓöèÍùÉ\°ôæõÅÛ³óýxU2âad«\x0003\x000fåH\x0004*a\x001cð\x000c?:a\x000fuxÐâA7^Îx\x0014ÿ&%ùÄ¼¾(öã\x0005Ñ\x001eþìÃsT¢h¥WFEx¶à¹U\x001bªÜ\x0017úð a%þ%é¸\x0018RXÕFÕñã\x0001¼º_OÄC×')\x0011ÔÊhüHwDZ.l1².ðìÂÓ>ùvó?Cø{ü]\x001f}\x00199¿ÿó¿î·\x001b\x0016%,Bâ©\x0006iø¢¹aè`ëW\x000bêówzôe\x0004ýúôb§eI|ºJ|ø³Oi¾À´®Ì\x0007|d\ÅWw¢Ås\ÈN¾¸y)y\x0010\x0003*yø¤(^®\x001f¤ºð gÿTîh·6'ÚåÍÇOwG_<~Ü^J\x001aÿ0\x000c_tõ\¬É\x001dsXbÄÍ\É.Ï^¾gÇ»;+HÎ4t¦Îp_ð¤$Ãs,K8¸\x0019¹.:hè N\x0007¥PT7'ø$\x0015n¤³¬Û \x0008÷*:ßÐù¾±\x0013cñÊ\x0003Wß\x0002¦uä±Ã¼Ú5tõÓ>®^¦\x0016\x001d^f¹wbm-Ì¡±\x0003±®Ù\x0015¶sWÄ«§î\x0006Ø`[±÷\x000e0Ó\x001c©\x000eß +ºô$Ý3x¥~%]me¾\Ø²gÕÌÓY\x000fmö¬´]6é\x0014<µÊ	*§\x0017\x001fZ°3/T\x001dxuWWwµY¶k%w	\x001e6×¡YÁòxVÏÜ\x001aáù$û ª\x0016ÄòXUcl©ûùæóÑóO7;$m£3mÅP(u>w]
\x0007Àl~>öÕ}{ööèùë³\x0005¶!´Ýñ\x0014ËþÖ\x001a\x0003Ýû»\x0006u\x0011Võéø¯\x000f#\x0004hø¦J6\x0002Î\p{\x0000eeü" ¬ßå\x0011úH{¬ÇíÌA8¹<àf\x0002É=ñªÜÌrøË
¢®ò,#¡®ó,ÿõh±?¶®õÍ±~¢\x0007üfßI\x0004Tc`5{\x0010/\x001dýf¹¥häÍn¯/Õ\x001aÀ\x0011ì\x0006ð\x001e0À±Ê`2ò"(`³]\x0012\x0017U·
\x0004ó¾\x0003L
~[±ÎQNH\x0004sìÉÙËÀLÕÿ\x000f¯.ZõXÄË¤&.vCß\x0012ZYÄ\x0005Í\x00123ÐµÄDQ®AAU\x0002+\x0012gÁÏ6Y\x0008æ%?\x0017A(°Ñ«
\x0019\x000c\x000c'¤Ê-¢{À\x0004Ö×Ô}:{Ú§ã_}¼Þ\x001ak×¨À\x0001É³³\x0006\x0004]Ö	\x0005¤FÜ3Áöÿ}òòtW¤]ãê\x0015%N\x000bþ¬\x0002\x0001§\x001f>íßi°\x0012¢¬B\x0005ß|îËÀÅ¦é\x0012º	\x0003¾x½;|Gh®Es\x001d´ \x001b4Ô´\¦½%\x0019O\x0003ê¼¥%¬é¼2!ûpõíÕÃçûíd¦%3¡Aó-ÿ« IQ\x0015æiê¯ÀæÓµ°2\x001dñV76H\ww»v°ß2\x000b\x000ciDÊu=(ÊÉ\x001dóo±Xu
º^½Ú¹C¨ºF}ª§²\x000cU9<Þs\x001e(¨E	ÜlÕ\x001bê#u5éS©«Åê¸
ª`
LÔf#T1ß×©\x00035÷­.gØ?öIZÏÍÝõãö¢\x001e#E ¨ö.pG¥èhçOóy=g¯Nßí¬çÉxÕxnZpþ¯ÅkGÏu^´ÕYsY{	\x001c¶p	Ò[\x001a¡ìÇ³ù^[yxñÆ£êëÄË«?¶»\x0005FzU\x0008LéÂË¹ÈFÍ¥k½ÃÎï;L\x0005¶¦\x0002ÛAåRÙ`¢rªtÊ²ôP«gßÞ\x0017`\x0001Zé*ôi1KËTOR¸m/þüçOïoo~~Ü¡é#5ÅR±¦. ÑûcÀPÇgÙXã¦½8}óîùùÙÿywº9ù/VK\x0002­]Å ÂPËÙ8xÝ\x0004#k«ÜÐÇ)ë'1(d?'&Ð\x0014þ%q\x001a/Y;GÀ\x001aPÈ-ã7\x000b2®FÙ,ÈËÏWß.*j\x000eÂrS{¬\x001fÌu¸Îq\x0012\x0016vîNôîèòíÉ\x0017Mqó^Z×Ðº!Z\x001cLzq\x0000EÈpjm7@ë\x001aZ7H\x000bzë¦
¦\x0001¤ý©Lh>¾Ö
\x001b\x001aØð¢]\x0007bÖHî;â5½bo\x0019ÎTmÝëÝW9tfTVL»¼¾û\x001cý $}~ýðáqûE\x0015þ´ÝX¬\x001cE×K¬ªu¾P.íòôÕÛè\x0003!äóÓË\x0017ïÞî`\x000c)^u\x000e®ô'O²nG/n¯nî.£§~³},¥\x0005Î#RÊ\x0017	UÁÍ@Ôº¹IÑíÝÑó³£8§gÛ\x0007ñ@K&ñ	êâÅ?ïyJ.Ú|JÁ

³±LîCÁ\x0016ª	ôÏ¨ãîÃ+	\x000ff=|ÚJ\x0012Ä3ñ$¢á³.px
È­â+1Â<|²O¦-\x0010(RB7k\x0015B}d\x000eÑ¹ÎõÑ)ð,Vê02_m¢çÁéNnõè/tò\x0005Ã\x001aÑ\x0018âsieÑmX9~ÐÌ.ôÎ®.Y\x001d.F»Ã9Í\x0011º¦ßé\x0010_³; {wØ²{-×X/8¶/\x001aQË\x0001>Óé\x001d@±$shÓ\§\x001a\x000fnÎ¢[É\x0011À\x0012}Ê\x0018}ê²ØF²±dz\x0005	S²åÊ\x0011,Im\x0004\x0008]2æ=ïn;?\x0017:c[Û£ËÇowÜRÍ³¼îP\x0017»¼[GT#kù	ìg{tùî-$êïðÃ/?üü@^wãk³°ëÝ\x0015°@Z\x0001êøÛÛë_>}¸ºûpP3&û, Eâß`ì3lÜ¯Xgçç§ß¼~qòêÅéDâõÕI¥!ôáÓÇwS>ÜîjFxv\x0001_ÇT9|&gÿ\x0003jçèDÎ¯[\x0018çàØÍ(÷îGè¨L¨)º\x0004q,1-\x0011R\x000b}\x0004¶
\x0010\x0003kÇjN8z?¡Q:g±ÅU±0\vÁ[Çc\x0018Ä1\x0014¿ÞÈ»\x0017\x0013ÿ5¶iT|÷q\x0003\ï!T\x0011\x000b¯¦XÇ¦He8X\x001eBá³|o
¸é<x\x0017qËl\x000bÐÕ\x0018\x0004Âÿ\x000c\x0010*ób"¢\x0015Ô\x001d
Ó\x0013mf"L¦y1½^¥O?¤\x000cÔú\x0019°è=BÜä\x000c\x0013¡\x000fÀ\x0008Ç9|dªU\x001bc>Y\x0006Ò¡ðubt¹ÃÏ(ä\x001fí¿_%\x000f?þ{0Nòéæ.\x0014;¨\x0015T·\x0010§7ú¦ùÄÅ¾rD%Âd¼y}öjkÊNÃ\x0011\x0017ZÌ¡²ë\x0004ÑhZêf\x001894íUA}!Ç@âìë¥ Ñª1H¼á8Aðw\x0002!\x001fx\x000c$þ¯Å#\x0012²\x001cp\x0004qÄv=8\x0006$\x0010ë'\x001bo9\x0008Z¬¥ :ä8\x001fNM ò\x0011ïRÒc\x001a7Y¸ËAâ¬ÂBèTg÷?£\x001eY\x001ed ].¦\x0007ÎrxUrK\x0007$ÞÑ-\x0007:wZºbÄ?AX\x0001&w[ÉÃË¡¼3Ì²\x001eÆ8Lú,\x0018êbó1æ)[Ü\x0003¦GÑ\x0019¡WÅKlúü«P>ÞþøÓ\x001f¹¹Aëÿ¤#ÒWÑËåÄdZåB'\x001b h^6\x0018<IdÊÒåpÞþ_\x001e}\x0015}ãÊquÿáú§\x001dÓs´RHtC\x0012SÊI`1Q\x001a39\x0010æ)÷\x000f'u§Ï\x0008¨\x000e3b#h¼Dä.á\x0011¿².ì8Nû@Q\x0000-}ÆFto"((ÒÞóVy°Ã8 nx@©]HäÄÎR< À\x0003:sÞ\x000c¢\x001bå`|#%Y¾\x0008*-\x0015F{¼ä2¨¸
C\x001b	Ié34 r]~¤Ô,Câ1.ÄëS\x001fj8\x0015V÷¤Ï\x0010¨¥¾X\x0008Êï\x0011Ô\x0004\x00065;ç>Ðt\x001fV£#5]¼ãY}Æ\x001bYFÔËCíøÔjG=íå¹\x0018T\x000f#\x001aØÄ\x000c(\x001cjË+\x0015I1PE8¢®MÞ\x0008y¿ãö¹\x0004ó»[ùûÍCu%9ÿôù&B~¼¾û|ôöúþþê6½Ôï¼ÃkÍ'\x0008[ÞDã%Ý-ze®!Ï_¿=/O_½=z{zqqr~úvK¡"Ì\x0011ÂÈa
\x0011\x001az­Ã\x0004[MÔ}=b¾Æ bqKö,Xz¡\x000b!ó%Ä0ê1Ä|Á\x0019A\x000c&[õè5åÙ*\\x0010QOã]cùæ3BhIX*\x0012æÎ_i½æA$iõùN44Ï:{o]xèª\x0016²ìEB4S\x001fs\x000c1_F\x0010±Èæ\x0019ur¨Æ\x0007\x000eÊ)\x0007\x0007Bÿ\x001a?¸\x0014u~D6fM\Êñn9Ô(æÛÞ\x0000¢\x00152÷3Æ
­¨÷z\x0008¨¿Fö0Û\x0005óLå ]´";8Ów´wÑO\x001dYÆ-ñ×
$zRzl 59G\x0012\x0004`\x0017:ÞÔ\x001cî1Â.ëìKn#Ä5
c«\x0011¥ÅB^.ç\x0007¥©ÆÎ>Péefg7!ª\x0001º1Ã¨ã~¡¸\x000cFÏè\x0016l¹ÕL|h\x0000CØ\x0003q²p\x000c ¬\x0010½ËbP\x000e
æÞJBLö	V\x0011Û%\x0017»M;E\x0017«½ìpÞIÚª¦ÏÐ¹âù\ÁôD ttòE×ü\x0000ã\x0004£Ògd
â ;añêBy°ñPì&Î<S\x000c ¢¶}úld|\x0000ÈÛ\x0004oY\x00007\x0004`DcÕ!\x00101¾>#ó¬LÖn£è%©\x0018EßPñá¬\x000e±\x0012Ë#ÊÈVFÁ¬\x001c\x00157Ñ}Ð^Ìø@N£>\x0003Xd>CG35Sh²dÖ#\x000fÑØÐ,G\x000b¹ìdÞIzc¥Ï 9¤'x¼Ñs|,{chsÙJDlI¡(¹<\x0000²´q!ÅGÎ\x0001,Îæ?2DùÒ(JÉî
hÍ£8ó\x000e0\x0013=èÜXKÙzq)JÊ ÎòB<ÀNI	é3ä7gt\x0013\x0000Ö~¢cOC*)>>#\x0018¹Ë;\x0005AÃN\x0015Íc¨C8w,Bú\x000c!JÎ n\x0018y©\x0011HZ\x0006\x000e±\x00081M*}\x0006\x0000A¬\x0003ÎðÌæd\x001b!¡¼\x000e[v
Ø\x0004Ògd`vK\x0012UJÒV1	í\x0001ì¡F/8}F·\x001c\x00053Áò^\x0001N\x0014\x0006â\x0010c\x0018Ò=jðP±:§î\x0001*Q±YÈå 9:b\x000f°\x0012PTú\x000c\x001e*ô6h0§îz£`\x0012¦!ù\x0001D¼¥ÏàÑLwf,§è\x0008$a«dpì\x0001æÙ`\x0003ô\x0019!."Äèêp(Ñ\x0006Q¢á\x0000ólñ5#}\x0006\x0010±®Ës@Ö\x000eR°x\x0012â4\x001dh\x0004Q"âØRD[MN¢AñkòoD¹òCø7>^ÁÓgÄn{Ãi\x001f\x000e=C4Ú^pXDO³`\x0006ø0}>}\x0006ø0C=\x0010Nýb\x0010\x00113\x0008Ñ\x001câ:5ÒÇé3r®D\x0007Gÿ\x0015ÝL(Rt®¸õ7\x0001%ð½7G¶J¼ÍSRuÃ_ÆpvN\x0011µè/\x001dçï \x0013\x0006tovmbûÏ\x0013í§\x000fÓý&y²fÔõé/1zW.ÎXU§Z,|\x0003ÚÍ9\x0008ù;\x0014c
¹T82\x0012ÖömNü³¯·9
;!\x001dçï`w\x000c\x0000©Õ\x0000\x001cKDÙâ\x00030¢ì_þ\x000e\x0005dÉU,÷BÀ\x0017\x0001ò\x0015\x000fa\x0018£øûû\x0007|\x0006Âÿ12Ùq\x0015u4Ap\x0014¢Äq´X6óÏ\x00037×w\x001f~K]8ÍéSI³ßß|z¼]ðïùí\x0019¬çD#£,?i\x0016G¥Ó~qöúÝvm
\x00113Y¡i»\x0010Qc»@\x0013M\x0000\x000b2ÊqéöÆäö7èÑÏInDçáY\x001eDë=5Îp\x001cPÆL_$\x0000ñ>ý6'B`\x001fzIíï\x0002\x00151DL\x001c/`Ð81>
4ED¼¶\x0010¢·\x0010ã?s\x0010DÕF1b<S"p<%9Ùø7%#ÂÔ\x001dBÄpKhÔÛ\x0017#\x001a5³â(
A\x0019/q\x0014%e
ÆkïJ\x000eDlR\x0011ôÐD\x001b\x0013Ýã(z ­\x0002IÉ=\x0011Ú]%?{	üx}õýuGRÕ\x0007,u!`ó\x0016gcMàÃa°#­mæµt;bÎ#\x0019@\\x0014ODÕêl³s^\x0015oqW	C\x000fbÎ#\x0019\x001bEÇ£(°£\x001a¢çQ&!b\x001b:\x0010CÖð[Uòw²\x000fál¹Úiò\x0018#?ê\x000e0F§AÒ5\x001fÛØó\x0005Ud\x001dÉÊ=xB\x0005\x0018[ßÓð±*äó%\x0007BM%ô°;2Õ4sÜß1\x0004/Çh\x000e¸y;\x001dÙ2"'¦c,´Ôã\x0011ì+\x001ehOKl¾>\x0003Þda\x0014|õót¾\x0004\x0017ø®/Ã¦zózÚ\x000fi¤cëhÀQCàùeRI9¹^õ0Úßßþxrrp Û\x00060'x?ØçrûM&º-ÊAhéÙ¾XUQ'x=¨ÀöN°ÁÃÉ\x0013
°ExÎ¬'~\x000e§âøL\x0019ÏL3ÃFðâ¿Äø\x0011¼ÜD\x0007é$\x0019D_®T\x0018oÚî@,§¸F@
Ð\x0001Ý÷"3äj{@\x0010>÷ãmò\x001fºùÍ¯¥\x0018]2\x0014ðô\x0007âT\x001f`íIl(%ý\x0008\x001föXÉ{C\x0003\x0007p¼\x000fä}áüNvïoþº\ð\x0014þ;\x0019^ÀÎù&eðk½¼æÛ²rãï\x0007ÿË5üVei^Í«û\x000fû°âuPJ1ÎXÎp)ñQ#Í7'\x0017/¶Úº
)ûª\x001dHÑ\x0015pÊ¬\x001cuVHÀv-'\x000eà\x0012$ûÞ?þðiK.{¼~\x001c}\x0019o!ñ¸ùóû\x0013ïAÈgk.\x0002Éù{W\x0002\x000b»\x0013æPµáËx\x001f§ÅÙn&
ó4»½\x0019=~Ú!Î\x0002\x001do8Õ\x000cíw?5PO\x0013Þ»©=\x0005q¤#f¶¼­-©\x001f\x0012z\x0002ß
meNÃB?oüÞI>¨í»³z\x0016ßM\x001d¯^Á¡&c¨<ÖþàÔÓLùnj\x0005XT¨±ÓQÞà¹\x0008\x0006Äîó\x0008õ4y¾Ú\x0008\x000e¸`ìEqzY×3Õk©§ùôÝÔ"Iö'êÀíô|<Ûh]Ãî¤\x0011èi}74ºõdö,Õ\x001fyR\x0010»;WnÝû5Ðè¢ÙKIDÍK
f|éµØx,®<\x00171xr²áS´@\x000ceãï«°\x0019¡Æ¬èg\x000cF\x001fÈ·u3\x0001=àÝ>\x000fvêt~Xl\x0012>Z\x001dí5ä+ãÎ6DPÝZÜSçm-¶;Nj£ë°=õòÒ\x0016Å\x0008>ffBÖRãã§©¶ýÔÔ\x000b_\¡¬láøi\x0019ø\x0010ö÷?|üá\x000f¨½yn«÷öS¤¿¹~ÜM
©}b`K¬TÍ\x0008R\x0001WíÄ?Á\x0004´4Ø{û:\x0002¾[@Ç¡É^<¼ÝÒ\x0003lÀJ|2p\x0005f²è\x0007ø°ªø8}z\x0001µËOr(E\x001dã_:Á²Xbê&\x000fð©äÑã§\x000fózt\x0006t:'¥HáÉ·ÔNOmì\x0008\x001f¤'v?À§©W\x0017v¹¬\x0015\x00019£Õ¹éF\x0019àÓè÷§O7\x001fjÙe>Thõ4ô\x001c´÷Ó\x000c\x0001ÀÔK'}z\x0001ãõ¥í°}Gêk\x000fé4óM\x0003\x0019#xX0>ÝxØ))ÓÙûÚF\x001fÛ\x0002e¡D~ùµx:¦O/ÄÌ	\x0002ÄÑúæµ¢\x000fç§¬\x0003\x0011éÓ
\x0003HªvÑIÂô\x0008-¦x\x0004Ý!f\x0018P,}z\x0001ö9R#\x00089Z\x000fñßGo­:úþ\x0013y\x0004\x0010ç!}º\x0001£ÝËÜ\x0012\x0014¨\x000eZg
S\x0007ø\x001czÃéÓÉE²9\x0003"EÈoþ¼\x0004Ã\x0001To¾\x0013?Ö¬Hô¿¾¸ù|ôòÓý>%ëðO¯nBäØ\x0004*q\x00164Ó\x0007ÖósôÅÙÛ£¯/v\x0008-U`\x0014®ê\x0002êm©\x000cËsª<gNË\x0019³ÜÏE\x0001©¾\x0001ó\|j¬¦KpF¹usQÌ©+X®|6ø¼\x0007Ls\x00113¥--×¬|N\x0005E!¥\x001e¨8,\÷e¼~f²éG.¿ÊhÌ²Ñ²?\½LÏ¹2Éx5-C>EþùýãÝ^/Þ¢\x0010\x001fzñ!ºÉ$	ÒÙw3kU\x000f×Ñ~ñîÕ¶w
á\x0013]Û\x000eB«sî;j¤(V
´Þí\x0015¶9\x0008!ÖpÂ\x0010¡ÖYP\x0014)¸[Ç>Å4rêà
\x0011Ò]sÐÈrÃ\x0004à· ËÊzÑ«^\x0008ñÍÞ\x0010bgNzä\x0008B°Z&Ê 1<Ì:¤ïÀ\x0018F'Ek\x001aÃò\jUàPß´í\x0008aÊ6cáY\x001eBï-oeËz3Ø\x001ckëZ\x0017 ÃòÃ¡Iö"ÚâV.¨&\x0000\x000cÜÔ\x000b#ÜöhZ\x0010QÑÏ\x000cY\x001b\x001dMLAô®í£ÛÂ!$¯\x0016íå½á\x0008z\x0008Q\x001bìH\x0011
=\x0000Å±µe\x0010·¾÷\x0010¦äôéGT^rÔ\x0013G1ç\x0019{ø.{å è*K;tð)Þ
åXÑùm':/îÀÃXG\x0007\x0018¥cÙ5o8eÍ+\x001fÊÑ\x0007\x0007aT\x0018WR0Ê ²3A\x001e«\x0011\x0013#§þ)í\x000fù]L\x000eF\x000b&¹\x000bWR°é>ÐzÜ\x0006\x0018µà\x0003Ðç¤:/]áÊ3ð¡ÄùqútóiPÔ	\x0004Óc-zdnlÕæ¡ë\x0010C(!¹²0äÌFFj¤èkKÔ
Ë]¦¬a³\x0013Ü\x001a\x001fâá«_Þ?M*I-ÿügü^ß~züm_¾Zô\x0014ó^Á\x001arkÓ°\x0010ª\x001b¬ÌsÊä ÇGoNÏ_¿û·í\x0017
b¾n *à\x0003\x0010´aM\x0017Q´H*¦\x000c2V0R²Í±!uÌi\x0016c<\x000c\x000fÅo|#Âó~cÇ2\x0006BsîÑÓä÷AÆüø>ÄXê0°Ø&Ð\+\x0016È5Û2ú\x0019óSû\x0010£cF¢0jSö<Ô8æõ\x0001F\x0017\x0017aÐ4üÚ8TAþÐ|ÒX7#¿¤@zÀèC^ú"\x0004QnúFOU×\x0006!éÝ|\x0008Òç§\x0012ì#áñU'C=­]êaß>~§~ÀH+J!¥Ï¦ìæåÕí÷×÷ï÷væÀº¯ì~§±¹m\x0014É!aáÍö¼Ô£'ç_^<ßÞô¢BÄ\x001b×C3t\x001cEÒÖ\x0016§ NmÏ\x0008¢ÃjôéGô*w\x0003Ñ³Ènc°5åÌ£Î\x0000¢T\x0018]ËßnFì\x001a7\x000e6WiCüC+\x001eE3-j\x0019@®\x001fÞøÓ·\x0017\x0011\x0004\x0016\x0007åVT3QhO\x0019)ìE{\x0019ø\x0015~½ýc.ö\x0014·õÛO÷%	xA59-di\x0011 <Æ<vºÛæûâüõÛíñÏ
\x001d^\x0001­\x0019 \x0013\/@ð5µ¼\x001c«i"Ô\x0008[\x0000\x001búÙti\x001f#\x000cPÛ3/,_óã½zWúûRºìüe#G=§#]¼ëSö¶ðN<ïw&ç/¤èj¦O7cuh.7O,_î½¦\x000eàú><\x001dBQ¨÷O»B*¾§¨\x001dUÄñjúôâI`µ`Y«]|¥\x0017Ôíµ¯ñ\x000c¦*\x0018×=¹ÚYY\x001a<Å¡©°ð,²Æ£xïo~¸ýüCuËÛäO7ÿøÇÍõ>\x001fÆbN¨¥g(©ðå=+\x0019S\x0001¶ v\x0014Ù_¼>ûòË³Ó\x001dNLAT\x0017>ý.m>?K¥.\x0004¤5S\x0014Ûuþ.R§0¢V\x0003E=\x0003U!\x0007n0ËÂq]©ÙUã¼òêZÁÕO³Q:\ß_ÝÞÞüù_K²<5+\x000bi\x0014t¡ZW4ë¦2\õüúäü|w\x000e\\x0001E¥ã Í (&\x0007Ê5³5Íâ­ûDÂöÇ´nRÖ\x0019\x001a#
ÀI{ØØn+Ö\x0002º«ºª\x0003T¦¿C¤Ø`(\x001f6\x0012[\x000b.H\x001b\x0012äÎ:«töõùö\x001fßþã×tT£%Çÿ<¿¿þ|\x001d!¸wêÍõýÍ. TM\x001d\x000fs_­ tþ¥Ó;ôóÓ·§ñ7÷Q[²0b\x0004æ8}ú!QÌ'e)eH/¹ø!§gb\x000fã}øõFÊÚå©êa/>½¿¾ßS
\x000b\x0011Åà-:)\x000bÍ\x0005à%)wU_¼~~z±½\x0018¶ðÉô*}? Â6B\x0000U~\x0006\x000cúòæ¶;\x001b[î\x0001\x00147ß_îªñë«×WË'\x0018È¨\x0014%A¯[bëú<Áñ
4á¯O^¼[2¿\x0015^}öâ)lËéJS«åîD§¦oCt9êÙ=x¯ô\x001eÓ
5kóR\x001f\x000c9#Ü3DãÝcçCvhã¥$(\x0016\x000b\x0003I¥ÄÕw\x0018¼\x001cêìÆ\x0003n\x0004æ1\x00174¸ØBGº5\x000bO~÷ËÏnvá}õéñÛ«ûo÷B¢\x0013\x001fK}º¬\x0018
(Y2|BM\x0003J\x001b¼¯^¿ûâäâ%x9¥ª\x001b\x000fÛøf»,LÎöÂ\x0008\x0005j¤º6Cp¹î­\x001b\x000ekte\x0019»ü²\x0017´§ÚØ8vÓ\x0017Ò!¼\x001c¿îÇ\x0013YB\x0016ÇÎ±Êö\x0014\x0018ùÀ<\x0000^\x000e]wãir¯#P¬g$\x001c\x0010¦µ¤#x\x001cµîå®_î	cåâiølàµ'§ï¢Ëù¾ûñÇÏðóß«n+o®?ß|>jºr¿¹½º¹Û\x0017(4YÄ1k»ûÝ$X[\x0014oÔO9ß¾={{Ô4ç~s~röª
Æ=Ò+¸Üze\x0014\x0017%z\x0014IòbÁ	5¿°E~RL\x0013ÖÇq7m:7(n¤åD pIëî\x0002sÏ++x"Äøø\x001aN(F\x001dWïYò\x001cE3×Çv·ôÈ\x001cç
¹ñ(Ê\x001a*\x0018{_òøú©ZøvÞ-ý
néD1«¹¥G4¤®#å×åôh|x7í
yÁaB>õ,ÈU).É¢¹Ó\x001aá\x0015¸EØ~\x0014\x0017°b¦µö\x0019=z\x0004î\x0001aí´\x0014cv£q?<¸^c^T\x0016º\x000fùé\x0015°Ç2ãNckpñz+×^
\z çv|yàv9\x0016¦÷³nX÷ñð­®iëC<pï¯ï®?ÞÃgP<ÒsÎ>âlk¦Ãy~ò"\x001e¶\x0017§¯Nß¾ÝþTqQïú..\x0008¬\x001f\x0001¨¼B5ÝAË¨ä½\x0013ÿ1\x0019­o\x001f.?=þr}w³çja°\x0016Braã¨ÈæJa=5FíwG¯ß}súêìbÍ¼³|ÿÞÍG¨þû?þóäöú·½Á©è7å³3úñÒ¶<úS\x0014\x0012S\x000fWÛÑÉùé¿mÓ\x0000úøÝ÷¿ÞWCWÂ\x0015éÅÿè«Û½\x001acÆ\x0018ÍMµ\x0002ê5êKû#¥Ä¨Ê;|õ?úæìä|ÎXEúDÊ²\x0014µ\x001eòS«·¥ëµä§ÌxÇÝ®fÙ
úDÐ²sH]\x000eT¥\x0018\x001f):Ç!å\x0014.5}¾\x0019\x0007}"kÙ\x0007ªý³\Ù¡\x0002`<t8MANÕäÇ9s`c\x0013\x000cOD_îI¾v6èäüÎ\x001bá·µ\x0015¾íMs¹\x001d)ÊP\x0007ÒÉ·O¢5û«òdÒTÄóBL);¾7*Jäô\+§þòJæy\x0019¦®´4E\x0011/TÒ¦|¯PÆxwÇ\x0001ày	¦®eAý9PELX\\x0017\\x001db§u
+çõºÒê6ÈNÑ+~ç\x0001#½B5ÈóâK]È&WªGw ®\x0010\x0012Ó\x0017¢7pè¥</½Ô\x0018hyû	\x000eÞF¿ÂC/yá¥\x001efç³|*³¦<A\x001f\x0002'xX½»ÁÕRæ\x0018yýÓ\x001f[
óÑ7W·WwoöVfyI\x0007\x001dæ°²Tdsa÷I\x0017\x001d}sr~òêíÙ«% söx9¨bo\x000cËÕª(üÃ¦Ø¸éÝz\x0005ê\x0019^J^Ò\x001b\x0012KÊ\x0001gçÝýß;AçÌïrÐ"\x0001\x0005Ô+pö=g0ÏÕK£ÎÝÅ¨°I¶Æ:Q\x0012Ù\x0012jcq÷l«.Ô9s»\x001cU²<,
dætf\x001bÏ³}\x0012U]¨sVv1ª©^¹\x0002¹úV\x0017\x0001Ï}þM\x0017êq]jèÁ"`¨U).\x0014f\x0015>3Í\x001c^:§e·\x00185:·\x0014ªp2P¨\x0002³ùâ½»;_\x001fé¼Ýr\x000bà¹\x001d|ÀGð¬]'x\x0001¨éëí
ÖYÙº¥¬Øì¤ßÒ[fEC\x000ehìUìbÅÀÆðiBT×\x0007&\x000b?aÚ\x0015w:1{ºâu¢Îêê-G¤¹]\x0010=\x0001,\x0013ifÞÇ{IÅ·\x000fNÔ¡¬êµíþ*\x0002}ÚÃ\x0018ÇMsþ\x0008\x0006ÿrÿ9Z`äg¬i÷Úêµíâ$þ\x0017¯\x0017ñMÞÉò¹gôliåð¸#Ù\Ã1¾§)\x001aKù´ÀlÔ\x0004(¨\x000b\x0006HÎÅ×ZNû?ñM\x001eò\x0017ò)M:d\x0002=&\x0016Â3ÜsuN~\x000cpò¿\x00100\x001e9RÓ\x0000tÒ$ã\x0005(§÷ê1ÀÉsþ2@T\x0007 EôL¢IÉ-\x001d²3Ý`9 \x00174t\x0013ºh\x0012C\x001eÂ }~+\x0005iÙÓ(,x\x0008ÂMÂl?¢HaÞÜC2I#¢ñåi\x001daø#üúCef64,´0ù\x0000»Êl²\x0015lj~Áç ð»R)iho\x000eBE÷Ì8-	eÚÀíå]¡Ý\x0013ßOk1\x0017.}Fy·¹7\x0014¶LÐ¥©\x0018Qz5ý®à\x0005ô4Óg×ü;\x001f\x0002u£\x0008ÅU¤Oi¥kß«Çü!æÌÞÜ^í+^ºáöAVyTÂM9ýßñQ&nâe°ÔÔó·[R+ª'*fK¨\x0000JËX< M~Q³!P¿s%Õ\x0013
³ETÑ\x000f×Ô±JÜ9\x0006Ë]X4T%»UTO\x0014Ì\x0016Qa\x0003(j^\x001b
¹"*öhµ)vî¤z"a¶h]IÉ	\x0017Ø9Kd*Å­°käJ(º]w
UüÌ[Q\x0001ä\x0012/­<VRÑEºwYeË\x001aL©Ë4wÁÖÓçàN*º3÷M e*ì@fORôAc×UH\x0006­BúôAaF3ùRñòæIÞP°,³iÔ¹ÅÚkE-\x001eªéÓEfãYJùPØ\x0001Ëd²MRi\x000bÒ3`\x0016K\x0006Óç/7`H>52*BéÓG¦\x0002æ³%2EÒÐ\x0002ûn\x001bÏ>²Ù©t\x000f·7\x001f~ù;>E%Qm×Téß^\x001d}sóÝÝõý§»o÷\x0015pCt&´«!<óä\x000b«¢]=íVÞ$\x0003}söÕ«Ó×¯¾Øãò\x001f<6kBãôÙTÐ«ËaÔ1\x001a¨P\x001b¡`,Kq1ò®ÒüÔ²\x000fþøôýOò(ÃÕÇ÷ñ¹zÜë÷\x001aÇ
8\x0000«¹ÙKçf'ÆM\x001f^ÄëÄó×¯^¼Ûîùo½üé»¤%ç°LR¾°\x0012§W×gÇ1\x0017²é\5\x0004¯;0#i¾° g©\x0000n¡9ø'Wàª¬e\x0019×£\ä\x0004ÅÊãÏç\x0006áBR{2Ã¸¨Æ½\x0000)"\x001f¥Ô¹âòºÁ
Ü"¡?+M\x0016tC}zÀÄ
¥³SIß5¸(ºáÅ\x0000Ïl:\x0008ãRÏB.(cýaç§\x0015yÝ°w×JÿñUÌ0=\x000euµúÿÇ>|øôñúv_x=zZ:\x0017\x0004\x0019¸\x0013\x001f(\x0012þ\x00136\x0015p.9n§/^¿<=ß\x000b8WÈ¼0:ðXn \x0010\x0015Ë2¡sSiâÅ?¼\x000fw¿~Dy7Ô#IÍYô%J§]~ºHW{ë\x0007½ç\x0018\x0002æû¨\x001c¸¡t<Lwè|òi¯/â{²+Ñé§ïo\x001f2O\x001c¿½¾ÿ}ßPb3\x000f\x0003Æä¶/èËk*ø=U_^üm\x0001O\x001dì\x0007øÜF@4³$¾Ò])òíjz½/hÜ.\x0003|zãÚ\x0010£2[ìðP\x0004Å®¦®KùR¬;}z\x00019\x00154Àí\x000eÃFzFe9 \;ÿ]'qúðÓÍ\x001d\x0002î\x000b\x0000E¿mçÖÌÚ·ôjØszùæì\x0015r\x0013¾l¤¿ÿðÇ?~ß=»7.e\x000c7È¢£$è\x0019\\x0013a*¿9Q©;2g\x0017PbOÎ"M¬tÉ¾Ô
QîH]@é4çrkTßñý K*ò´å\x0010åÙ\x0005Vbx7gÍZÞÀÖ±tÓ^\x000fC;2f\x0017P²±?P"\x0001±TÓýåÿºwM¶#7î}§²'à\x001dx$^ÑvSL\x0007Ù¤øè°î\x0017Åf§\x0012ø¥óÉÓð\x0010Î8îL<\x00042QU«Ö*dÕ¾ác\x001fÕá¢Ü\x001d¿B\x0001D"óé³ÿÇ/µ´tå½ÿüóýÛk\x001b1
(q÷òÖ¯z4»ÈYg·ÛÏ¼üÝÝ÷y\x0003¾ÄQ§~3\x0007\x001e\x001cA
uÙb2Ç§´t³·ph¼( 	\x0003Å¬³\x0001t\x0019±+ÇÇ\x0013%\x001a\x0010¼õü®<6X\x0017)}M}KýÐã\x0006!i);º\x0003\x000f\x0017å±u$ê¶\x0007Ä+\x000c\x0001qª×¦j\x0013\x0008ÖöÇV\x0010¼q\x0000ºÉ³Ü\x0014\x0007\x0014·\x0015òfÙ\x0016l\x000bÅðNyl\x0004	yDÌt$ÜÁ¥|Çµ\x0005$O-lÇ£6Î·\x0014+1¥ïf­âV\x001a¥¬\x0000$bÈ¡<¶3Ô¯(\x001f5cë\x0018ãyÑÀ\x001e¼[@\x0012:Øå±\x0015$o¦*M®éÆØñÔê-eeì\x0006\x0010«qáÖçV\x0012¬Ï¦Ù
£\x0010 |ï¬¢Ä Y×jõ¹\x0004;HU\x000bÏ3\x00147­\x0013KGm\x0013\x0008n\x000cõ¹yØÚJ<\x000f	6H¤>9ÜJÜz»#o!1*/úÜ<MRÍêÅãª \x001bN\x0013N[~\x001c6¹>7Û\x0012¨ ZWSó¶Ñ&Q³)\ ùÕþío÷ªyôOññûo÷¿â½nÌ¹yu5\x0018S\x0013\x0019ÃYL7I\x0000\x0017YÎïßÜ½Ä¶$sóêÍ97¥á%ÔH-\x000f\x0001ÞÔ
ïheåm«õÝRjq\x000cO+UÒ\x001b/éU\x0014pÃ¬Æ\x0010iÆp)A:ÊW$ÊSÀÿªñMM½Ã{°©\x001aéáò9\x000c
§dü<gPj¥\x001fÿgïy?\x001fz¦õ)à\x0003UßðûF^²Nñ°¼Ò\x001cåeü¢lü¼¯ç!lØ+pÀ×Óàv|ZUI\x0008Ùú¤\x0017]Õ\x0015ÈYp¾ñå	}\x000f
\x001fÈÆÏÜ\x0002©)¸6|\x0002Ï\x0018äQ:¬­Ïa:¼¨f¿\x0002\x000fl{Y|`3ÊW.!ÊSÀç\x001c'³\x0015ÅBâsÍº¤å&?Ê\x0017Êì\x000b²ÙM
µÄ@>\x0012ÈNm|{­\x000b^¿«OÉø>\x0018ü})gÉ·ÕáÎÄ	\x0006ù)IæFb]Ê!9\x000cmyüÊµ,¨Ý|%²<\x0005|"¦Dðí\x0002,poWçw_T¶ÿ®>\x0005|Ù% '8Öv/éÆ·Ìþ\x001aä³¨S\x0012>?ñiîì\x001a\x0012[Ü\x0019QÇQ>(\x0003ø\x001cç3*\x001b=>WQ$ºëmüÔ9ýåç·_Òß1fååñôþæÙýÿ¾¿bR°\x00053w´Ô¦î\x0018¨È±+íÏäÇÜÝ<»ûî.aD\x0008å±	\x0003\x0012VÒ\x0014
y÷5`d"®ð¶}B£\x001aåwõ¹
\x0003»Ç¨É$mx4Ôîã[8|áðÛ9XOÕsvµ÷)êøi8\x00060Â_þõO;+\x0008ùâ\x0013^\qÙ§Ð4&z¶äåÏJáÙj5ÅûÅs¼5¹Luª\x0003¹Ê\x0005\x000c¤\x0008$p­:\x0013²Ùôk÷'ùIÏò\x0012¿v\x000e¶\x0018­Qõ\x00163\x000f1Çó?A#¤Y~®gyU=\x0005þÛ¯ÿxûó,9p[Js>uÓu\x0007v_¦KéU"Uý/Oâéã\x0004æ%\x0004N?Ö$¹é/¾sS»rT¬ùøñÓÇû+\x0017Î(à-¼©E¨ÉaZ\x001aMåe\x0004\x0012\x000enî~øáù\x000fw ¾\x0013´¨çhQ£iL\x0015®«,ï×¤ °ô:£ìvÆj:§p¶³\x00028¯9¶ý:\x0012êtJ³¢û\x000cõS¶vkz
×}Ô(ø¨*\x001b%ªKÑ!Ñ
`ÊSÊ5Ó(Æ¶ê;4/\x00187,+£ª[·\x001cÇé#&¥3]°6~ÔÐÁ\x0005Á¸å=EUSª³ÿ^Ó	\x0012ßWtæ²oÓ°¥î&Á\x0017Õ\x0010¹Ûv6§·¤\x001d\x001a=Ûx\x0017®\x001f5­Ø

¾©c\x001fÅdSk\x001c}Sª¸Å]YJgbG
¤Ã\x0016\x000e\x000f\x0015¼R\x0013\x0017ë8O]®¬ÒË4°t¶³qøS0v=ªx^Î³\x000bËxÔV8×Ã6\x0007ÇëÁ\x0004EêFycç[&6²~Ò\x0005Á¤ËÛ:\x000b=Z­ÛgMiê©!¥Ëÿ®9\x001dÅÆ-¾å~Bª\x0019Q\x001f¬uì±K\x0015«-$\x001fPæhøs|à²H"\x0012Oòá Øy
K\x0015Çm\x0003gt7åð§\x000e0®Sè\x001c+M$oyA,\x000b¶²¥M2åÜä+%h#g¸¸Ci²Îv\x000e	þ\x0014\à	6E\x0016ÍßOgÒÆ7ÒAÿ]Aò]k<¬~W1ÚB\x0017ÚwUË\x000e[\x001bé|¿&¼`MXEy.:RâI;§ÙìJÇ®÷æÄ³ÙQ¢\x001d\x000c{ãQ¯\x000eEÝ\x0008pÚ]5&+p©ÛÀð§\x0000NqÌ\x0018°©\x0003-ØÄga-ý®ØHx\x0006?á ïýÔ*\x0008\x0005%Is=¶rí%)[éLO'Ø$P\x0000ÂaÖYî]\x0015\x0013¶&	Þ#Ì\x000fJà©;(µ'eì°+AõÔS"\x0019
«K»L\x0011U\x001d\x001d\x0016g
ÓyÎéR(liIÞW³WEÍBºØ}ÙR 5LZ%\x0014òkò\x000c79§¶¹\x000e£\x001e3º\x0012\x0004\x0019¥\x000bùs\x0006®Ó2j\x000c&¬:±ße£dõ\x0000-C ¯
ú²Ú²\x0002^êØaþ\x000e\x0004;E©9¥\x000bn,ô¤\B.0\x0002³L%Ü\x0008çú\x0013»`H\x0010\x0011+|­ÇS\x000fí±p¦\x0001ÆF¸h$÷ÅÜX\x0000¯\x001dåqqf\x001bÎF\x0019\x001d&qÍÏ×FB\x0017}\x0015cÃ÷V9ÝMN¬\x0008g:o£\x0003èèòÏaº\x000cw9ô\x0011ª÷Y3Àj7)\x0008W,æÉÌé¼À\x0016Ghw\x0014Ù«]#ÕR×&èJL\x0017P\x0002¼¤\x000cgÝ\x0006h\x0015ÆàZÊÂRf}#î£\x0013%gf.[à@\x0019\x0015*ÊÄ:õ`E©\x001bñ\-)3ãxÐ²/Ã\x0017[BJ´2\x001f¥dÈtx­,¹0%ª\x001aN,\x001c<õpÙ\x0004\x000eOâ\x0007$4%dóòw¦¬D\x0007|b,]ÂExúdehÑÊ ï\x0013-\x001e5sp®e³.Ë·¢Á	Àâ¥ ±\x0004²¦RÄ\x001aÞÁk\x001bíûx®w%Wf\x0010\x000feBÚM¶ª:Z-Ç.ÛÎnÄó'£çÇG\x000f«h¸\x001có(½If\x0007OèCÌ\x000e/Ï;<U9Ñ'ãê=»·,.w.g#^:\x0019½$\x0019=ì·Mi2Ö°Íóýcw¦(n+^<Á\x001bß1p¨jNuôªÆ±c\x0005ÞRßp\x001b\x001e¦ítáv3nó0uSÜònkèÛr³rÏäÂý\x000cv:º \x0018<ìÂF^(\x0016\x0007s	û¤&µzæd¿0ýÂk\x0016¯­	F\x001dÿ #Ý/l\x001f¯(¿Çñ°Å\x0001õÿñ¦6BÍ\x0005NmÏ£'ÜmÑ\öxoë='Gã·méO­ÞÌ-x6âéÞ¬ào\x0001^¸MÝ\x0016";ñQñÁÖyaP@[Ó\x001beü=Ô>nÝpãûéËÖÜáYÁ%×hThaä?jê¶«[¡Ð c¢X\x0007\x0007ãw¯âÝ6iÍ¢kÑ´U¥¬\x001bñÂÉ%^\x0018\x000f\x001f{SK+^`aV$o³[ Ümí\x000bo\x0005.¼Ï§W\x0016èÖí,Æ©	0j¡ó©¸ÇKã\x0001\x001foÀpÕWÂòïj±M\x0017ÞRïb\x001b;99ÁùÌæÆ|$ÃÎ\x0012(i]îØ\x0006O\x0006çû\x0018mù=\x000eÜÌ\x0015¨ò6ÚhÏpvn¼\x000e5 ætE\x0013j.hE6¥\x00052jâ"X\x001f9¯ÒyÖþ\x0002õ\x0006^~{GZUOß¿}÷ùþëûkÂ­áw(rÖÔq!qk!ëÏ\x00187I©êéï\x001f¿¼{ýd®Ýz
içV\x0006Á¨Y·þºãº\x0018X\x000fÁÆe÷\x0018#Ì\x0019AÄ÷\x000elUà\x001c\x000b
´aÔnéQ
!º9¢!*E­w\x0013~öDÃèÉ+5öLÓ1H?ô2H\x0017\x001b¤vÜ-\x000e<!ÏÜô
A9d\x0010B[[{j¸\x0000\x000c\x001b-·\x000f¥ªú\x0018c3Fá×[ZØÆ²¤D\x0008\x0014¥7y\x0013Ýù±Ó1É\x0018óÂ¶ÔFE%nL))\x0015\x000eÜR^}\x0008R«ÎD*\x0019%^d\x00192?R\x001eòÒæ\x0019yær±7ã2;ÞDJ±[
45*voòHî´ãº³ãZfÈ}²­¹QtÙ)9a	ÎTfQv\\x000bMy¦HKª\x000fÕl<Ê7DÙ\x0019s-´æ)¶¶NyS$\x0013Ä\x000eci¯º\x000f²³Zf(Qf\x0018hZb!qÝr¶üÁÓÃè\x0010eg)µÐTFËÇ\x001c\x0006\x001d!ÇúL$n²³Zf,¶·¥ÄÇ¿¸;ãH@ÎV\x001a­Do×ÑÚñºõÎUl,á,Á\x0018eg-ÌZbG\x0005X`W}|îâ>SgºzA\x000eÒÈ ³»F½ÐTëò\x001bg\x000ep&T2\x0004ÙYt#³èäaÈ
%Í\x0016=\x0019¦tf§ãk:nd\x0016\x001dÛSx\x001eËXÏ¯8+¿æôNÊÎ¢\x001bE\x000fØò®®\x001dÔ8¶Õ¤cÕ\x0002¥[
¥üpÿ×O_¾.!;÷ÜÈüsÔ\x000e4ÚsßÃ¤&m§nº}Ç\x0008÷\x001d,ê©#i55JB &[¦F¨Ûul×	Úp_6Ô±&¿¼7¶\x0006RË2ø1Ên×1Â]\x00074;¿\x0001L£ä\x000eÙ.¹\x001c´Ý®c¥»«YúµÅe¢I©Có+wî:¶Ûu¬p×\x0001_ûSä¡t
Ã}Ò+^ßaçÒ±Ý¶cÛÑXy[ýJÌÅ$Þ!\x0014;ÚEÙGû\x000e´6q\x0001xy,¹ÀËÅÇvû\x0015î;8\x0019ÉÑp®ÞdeJ\x000bì¤'»ówûî;©&¹b¦­U8Àk|ßAÂvÛ\x0015n;6´~ÞT	?9ÌGòLø~²Ûv¬pÛq¦íàÁ°Ï\x0019þ<;c\x0005¶Ûx¬pã\x0001ª?Ä±L·ìfð¾Ï\x0011;²Ûw¬pßÉë¥jh8\x000cZø
3\x0011vAB·ïpß±5p1ÈûÈÞï\x0019©ú1Ênß\x0001á¾ã÷\x001b³#¬XG °¼¶9Ö9DÙí; Üw²wèx,·©Î\x00067=i?\x0004Ùm; Üv0Ú[\x0003¿\x0005¢2\x0004Õ±\x001boÏdy£\¹Òþ&B¸ë\x0000`¼·6üÕm×qg¥Ý¹7B·ëp×
#-u(}½/.Ê	rchhm(»m\x0007Û\x000ez¿ä²¡¦\x0003{¿lÜÞà/tÛ\x000e\x0008·Ä÷\x0012¦	RªbïÎ$Ïd·épÓqê\x0006RS6YçcÀR1ml »M\x0007dNÔ¦\x0016#¡Ð¿bEüx$ÃÆ­qe$]·é8á¦ãÍ9úl(C;F¸¥ìÉÐPºnÓq²M'¢9¯s2åSïlân\x0013ÎtÜ\x001a£ì6\x001d'Üt<`Pº\x0006
JÛº5\x001aÞtÎ\x0014î
Avm:¨\x0016J^%æÉÛZ^¨[  Ø[£ëv\x001d'Üu0ï<6o¸\x001dvìUî¼£wý\x0005¸lÏyøIÙm:N¶éD¼À³t¶õ¨DEVm%¶\x0012ÛEÙm:N¶é<ü¬ì¶\x001d'Ûv0³ú? ÃA\x0005á*(vØÔÆ½q²ÛwlßI(DýQJ^s\x0019JJ\x00047!.ÕX\x0018}·íxÙ¶\x0013³+\x0019h$S «¼Ó4EÁb\x000fe·íxÙ¶©Ô-\x001bÖÖÑsÎe[
Av\x0006ÝË\x000c:~n\x001d[\x000f~ï\x0015/ÃwæÜËÌ9.\x001c§É§´ÓÂáuãÎHd\x000c
dgÏ½ÌcÛ\x001eMë&#ê\x0014¿6ùkaoöï,¥YÊÝ]H¥%p[lc\x0012*#ìLzð¡ôBC	Ñ±'T2¼¼ÃÎ;Ð­ \9ÝP_\x000eå>/#tK'ÈNÑã¯g¨miV¾¬	f©/;FÙ­ \;Ø­TÈ,
dàÞòiÙ\x0016n°óÌ\x000fB·"\x0004É(Ê%H\x001bR³\x0007²Ï\x0004\x0014-nÿ=5
õJ9\\x0019ÉÄa«\x0004gji(»Õ\x001dd«\x001b
%ÝÚ&«¹ÕfeÕì¬í¼ \x000b\x001b\x0014DnÃvTø£­Â½ØkÊ°à\x0019È\x0011ÈØy\x0018Qäa¦qÄûLk\x001a\x00178\x0002ö^ÆÎNFtù\x000cÏµÚª\x000c#\x0019y}i9FÙ\x0019Ê(2NYJ\x0007ôèí7Jk2\x0011ª\x001f£ì\x000ce\x0014\x0019Ju¤P£3¥a5,õ\x001e{ ;[\x0019E¶2CZÖäÀÊHþÞ\x001c¡¸{Vv¶2
m¥\x000f·$«­¦'½Ð¨ÛÒ	»ç±Ï\x0016YJ\x001d»CUüÑª\x001dk'ÈxFÓtÓ@jWD:§¢
lÅÄ&èÛÍïß}ûÇÍO\x001f¯ttÅ>TÜ,Õc\x0003_Jüô®%à¬Ä(ßÜüøäñ¿yñü×ëxfg\x0004xÑWå\x001aL\x001f0·\x0013UK\x001f8¶ÙFgçtV@g '7d×LÕ«îè¦D°«mx0Ç\x0003É·í\x000eÌä£M¤DTNL\x0004¿r¸
ÏÍñ\x0000Ï%\x000eSàè\x0005Â\x0003N\x0006eW\x0001:?§óo\x000b·>´$ CÉåO0àWR\x0004¶á9^\x000cåì\x001f_3¿jÍHÔ¬Û8Ç\x0012¼xËùÔØ¬û´+Õ"ÛàÒ\x001c.	àL©úâê\x0006O6OAxg´	7ãME"Å$+\x0001_><iÝ¶oÛrñÏëlÇëw\x000cÉ§Pú¸ÚVç \x0016\x0013\x0003·rÓº
¯Û1´`Ëpù$J)^yîs\x0010PH³swX=ÝY=-0{ÙâK`J\x0018T6Ç'<\x0000³áëú,L×\x0015-°+.µæß®ªÆÕÑãH\x001dØ-veáRÚ|r ªâ\x0015ïÑû_ßa×+-¶ó¦¹Â+D[5X·Â¹'juG{ôäÙclyò¸ÁÑÿß3jÓ1j#b_\x0018Ú¦£yøÞ¬óma´§Yìö4ýÑçOïÿ~öþË
Å°x1¨XÅpßí½¨öðRdöÑËçOþ\x001dÿüìÉ«WzÒTÉg7öô\x0006sÜø\x001dÖÑ±(&7\Ç{Éµ\x001e\x0006E$ìiDb\x0014\x001côTêÙåöÉp\x0005`¸\x0014ÁÝN®õI]wþ\x000b<"<úåÝ¯ï?fÞ/7/>ããÝOßþqå £\x0001XýÈ î0ù\x0007âz<~ô¯=ù!³¾ÂnÝùñøéó7ÿ~Æ´\x0012¨\x001a)¨iZ9:¶6\x0012yÐiB§3äGAÓ\x001c4	A±o\x001dg¨@9,ÉjÓòè`\x0011®X\x0001íU×rZjHKM6Ùó\x001cû\x0001V#l-ZìgçxêþÃãO!ª¦Tê\x00035\x0006+ÒãNv¨SnCAÅä\x0006ÙÇO©º (°kÉAN 9µ7I²\x001aEM=ªtjÌ
â¶\x0000±
Åàâ¢Ëx¦}Õ jê'@N\x0000UX²º\x0012Ð
¿÷¡©¬±\x0018)¬k¡À­xðfÙÓêçTß¨\x0016>Â è^@1\x0005]8¦\x0003D	iH9Ä\x0011Î\x0014þÚéJ\x0002Iñ§\x0014\x0012\x001d×c\x0002Ü_ËÅ	ð§\x000fj©ò5ÊzN±áÇ\x0006%dø±ß\x0018Ý¥føýR%r\x000c\x0015R7Kñ§pHâð\x001bv\x001e¦&9º\x0006üô1Tç»¯?e¨¨$DÑ$Ìc4@Ä¥ÂÎ¹?8ÚO\x0000'\x0000½Ô<å¾ä\x0001\x000egàZµÑ\x0019\x001dÎ1Toº}

Q!ðñÀçÕÏy\x001bÜÃ)ï\x000eKñATèæ*þ¢ê¦\x0006á5ïS(ôÇ5=Ël¼Í¨ö4ÚnK´ýY>Pÿ¿ÿ§\x0003^ÝûûußßæA\x0004²R[ABâ+ª õâÎâY>P?.Þÿ«»7?¿\x000c°§Ñv[¢íãx\x0011¸\x0002%¢måsÕF|ËÝ\x0001>;ç³¢áRÓóø9\x001e?Ýø\x0016Ûæ\x0000\x001eÌñ@4|¦vúD<ÒcÇáS©
ßÂ\x0001ÝÎ7\x000bîØ\x001aÜ\x0019\x0007ô¦J;×ñ\x000bõ´¥¤mü\x0016kd; í¿¯è\x0003O%o1:¾ï)B.´/Ý\x0001@ß\x0001z	`Æó«Ñ6\x0016ÀVî\x0016Ì)8óÙ3 ºìãyó£\x0010\x0019
vÖè,´¦ öðM7àÈ¶`Ï¤¢ÌTùø<Ï\x0010\ÄêÓ2\x000fg3 6Ý\x001a.³y\x0010%vy\x0015\x001b®Ê²Ð\x0012hõÒØNh»O?\x0005`y\x0017	U2¬1í\x001b/7åíÁõfFòuTU½\x0013+_\x000c\x0017:å¿ç\x0018h\º¸	î÷9-ÙéLu¼Ê:®=>
aËä\x000e~y³¼Ðtc?\x0005ch=Ë\x0014¢Ä¨¯+9oÀ\x0017Ê²KÀ\x0000aè	%»ö±|W\x00184°\x0014lßNh»¥?%ó°ä\x000cÔ^_%å]QxàÜèeíÃfBÛ\x0013Z\x0019!ñÔ0QØ¤|dîóq¶çâ\x0000 ë\x0001%Ó\x0010c*$ÉfPë\x0016¨XfÙl\x0007\x000cC?\x0005\x0001ªz"Æ§4W
incâRßí±['øS2%¾1±ª&"Fm8õ4zÑGV>üñD=&\x0014õ\x0018:>ýæý×r)±¡Ûxö»<_Úl\x000eë9\x000fÝ\x001a\x001aD³ô\x000bùìôäu¹¨­Ç× çL¡T2I 5°j­\x001d\x0005R±Í6f9#z®÷\x0017¾Ã\x0012Lì\x0006J\x0008V%Ù<YÔiy?9ïÎX¾¸\x0013ajlS?¹É{tmZ\x001a5'~i·\x0012[OÍ(K'ªqJ\x001b5«Ìæ\x0013\x0015Ð-I\x0008@	²:\x001fýVãz0C\x0019Ê×îtXs®I\x0012,cRÛw}&\x0003~òoß9%Å¿\x0012À\x0006\x0014ð\x0004«H¥9\x0004í-Ã®Ç:Ú{'w"©ÿâ»©­Ùïß!É5¶êÐ&Ù\x000f÷<¤ZfÍZ³\x001f<Æ¿<¸qz\x001dæèæy\x0004+\x001f\x0004¨Ão>\x0002@Pf¥ËfkôZ÷Á+\zPz­n\x000c,bGijQ8\x000b6d7û¬®©ø_å=W\x001cäÒ\x0006ÏvËsâk\x0008±5â3å\x0016[ÀÌÔCªÌ¯©ÔF0\x0007XCSkÊë\x000bÑ\x0006nÁW/ÛÀ|èÀ¦¾ÛÀJÓ²*<o\ AÎ<ï\x001cµ\x0014P°Ö¥ñ\x001aXð\x001dØÔï`\x0013\x00188g¹¡:f\x0001\x0008g0Ô\x0003Ñ¤Õ~`\x000cvÎN`DbNÆ¨,Æ'©Ë»¶tßM]hÞc£;ÑhÍf§ªÓ<ô\x0019ó¡(ÕùeZmLH\ÑaóÇM|\x001b»\x0001³qpÀ\x0012ª¼Ò=~ºu¸8§?­v²¼Æ:oÓ ÅOÉpfÎ®¼®Þq6@-ÿLýê\x00160èM>\x000cÚ|ÀÒ\x001cÅSÌÑåWÔ­å¼Ðâï¾#þ\x001cÃ²mÔUE²ÿÑ\x0012\ôZo+`Ît\x0006¬\x001cFÀtö%hæ+ìøÍgY%%´¬.\x000eljRµ\x0011Lªmi\x0001\x0014Ê´÷À\x0000k\x001d«¯pyè¸Àæ\x0010\x0017ÆgëTX{¡):Á*ëx©%\x0003óÐMÝø¶ap9ó¿ìâ:Aó¹ÆØÆ:ÛêÓmìgqÏ"eZ±Õ\x000fÒv­WÖU°Ð
N}cCÍØÎ`AqÖ¬mÏ1Ñ-Þ\x0002\x0016zo:\x000cºÓù,ê9\x001bNYÇ©äù´¯yî\x000býé\x0000\x0015\x000b0hÅL0Õ
CÑ\x0002ÓbØ¥rò¾$³ú¡7¯aÔ¼æý\x0006#\x0015¬¥[îoÁÖú(^\x0003ë\x001d0èð@öDøb'M×\x0012\x00006\x001aQÎQ\x0002Má\x001c\x000caû\x00122\x0016òÙÁóxE}FZq\x0013í¦~´Sßfï°°Ë\x000f]Y®Y\x0015Ïü\x0008ÝÉ(ÂØÉ\x0008ìÌê\x001bj\x0012wØ,m«S\x0004Lw2Jfìd\x0004ØmEL¤,KÍºÆ3ÉõÀf×\x0008VdmÀ<{®ÙÎÖºÞÌZ\x0006ªÌêkÝÏ°ò{ìd\x0014\x000c7ÔÕ\x0005$bÄ®ð«u?bå÷\x0010\x00196g¢LH"\x0017T\x0004\x0013[ñû¹*Mdþ$^á\x0007÷pyçZò\x0018Z	â\x0012\x0014Öú«]!3ÐM\x0003_3#±Ø\x000fv½T¸\x0001VûÒ]#sª's+\x0013Ç= È5º\\x0004Ìµ![\x000b\x0015®ÞM,¿Ç¸²¯Ã
\x000b xeÆÀéBçô¨·p%Ós¥AÇ:\x0018Ëã"ó¤ö\x000bÔ_\x0010±DÞX~Ç~áï1°ÚÔ¢\x0006\x0007|S½2t\x0008·êL4{#;!\x001b\Ed\x000e»ùÜ\x000bÔäG¬Â»{\x0011ÙÁQ¢u¤E÷F®%Í¾\x0019¹3uþ[È¢î¿fÔ_\x0013\x0013ë~étdÉYÝZ\x001aF9óZ\,SÄ\x0013ªAÿ\x0002E\x00124¬HX»kkþØY*k{*;\x0018LA*nºìÈªFEa1\x0013ó+¹~¼J\x001fñ\x00012Þa¨3ß)¾Ç[P_F\x0018\x001eÐ)öcVÔÚÈ@q\x0017W¬\x0019ó,ÃA9í\x0016¯¶%df&LUcèaÌðcÖ/ydÎG:dSA
2¬U²!3ª%ßc`Ù»ðuGÂÖ<$É	bÕx	+ò{öÝÇ,¿ÇÈ²\x0018\x000cî\x001dSmÌ\x000e¦'\x000bc»¥+erÕõÖÑÅCrt³Öiý¶	,¥\x001e,9±\x000eÃÁªZ~OËÒÈXé@ä\x0016,\x00037V~\x000fa\x0019M%Ò^\x0005ek[o¬¥¸ü\x000f­µD¿BfC?Çl\x0018c%Ý\x001a\x001bÅ%A9nnµlöÏk_*Ùà§Ì»NUJÉc¢÷59?\x0018òúÏéGmá:q.Ì¨sá,êË\x0018âRè\Qñ5\x0012\x0016@ÈÈB?Ëð÷\x0010\x0019¨ÀiM¥ÃFµ\x0017\x0011Uê*[¦Pn"ó'\x0017ô~0¦è°h¼~¬_òÕÆ&ß:Ç{Ñ\x0001.>b\x000f6\x0018YqÎQ®\x0008¶î.É-Øõ<'èc:8£ë±ìd[ò£ÛR)P§!KM@-%ªM±¨:)"K®_\x0000É
.\x0000Ül5þù\x0013Öû"áHcæ£\x0015\x00193ÛiQ`+.=\x0016Sw>X% T¼"4ÜÃþÔò\x00160ÝÉÊï!0\.Ñüwµ¥\x0015ÞÙ³ßïÎè\x0016m\x0002ë¿eù=\x0006g\x0019mäIC½°D0
`X¯ÎtfÙDæOÌ\x000eYôå\x001a#	îøü¯eGÖk»	,¦\x001e,\x000eîKxìµ4É°9oþ&2Y6¢\x001dÓ¤©ØÑ<\x0015\x0017°>¦u¥#\x000fYË\x0006ñFfe­1ÐAß\x001fÛÐ9Õ¥1QW\x000bëe~lù\x0017t`atúcO´âýh¹õS\x0006Îòé Èåh:­úS§U/>½ÿxÿåZXÏ
~#×\x001axßÚü¥æãÿûâù\x001fî^\x00195uZô§Nþ¶Ñ\x0019Ë*q\x0011EÅjØ33q9rX:gÛéâ.Jè<µÞÄ¡«\x0001Fß\x001ajø°Ô\x001eØÌ6+ÒÀs\x0002¸\x0010Y­Wa?j\x0012ÏáPv¼Îv\x0012k©`¶pV4ã\x000cÊýÕ2ºVã=ÿZJÌl\x001e·ÙÍ/\x00060½\x0000\x000f¯2§\x0002«@\x00028­V_/\x0013E6ÓMÝ(Î\x0005ÉàAÇq4¼\Y\x0006þRÍÈ\x0015ºØÍ¹(sØéÞ×½T«HÞw	Î$ouz¦[f\x000eëG.ï¦Æµ¢*ª\x0015	VñÝ¹¿T|xyè´6=ÄÔa0Ò²p­5e^¯\8ç\x0017)ÛùRÏ$ëBqJ>n­tâS+J\x000bËPÌf>è\x0016\x0006þ\x0014ðE¿×\x0014\x0004Ë%\x0003¥¤R\x00109qÛùúñ\x0003ÁøAL\ ÿ3U½M­]Ç¥êá+|¾w\x0003¼Ä,ÀÇ@¼ú'«\x001c>[yÙ¦ZmnÃsS%q\]\x001fZ]i4Ë\x0004í|±çø\x0002¡etdJà\x001bp\x001erÔr7JO
ä\x0005/Äº¸&÷
\x0016¤ó­\x0010­Dfe|¦_½F´zku\MRK\x0014\x001b/RÞ£vIÛá
^è|b>>û,\x001fÅ0OõÁp6dZ
\x0011nÆK¶ÃKV²v¡V#ÅôÈºx¹VRËãÅV>è÷\x000eì\x001d½CE:¶Þ\x000eZZpXÊlæ³q\x0001+0.\x0001i*o0íRÞqÐ¼hÂKñz\x000f$N_þ¾\x001cÔ1h¥ëìÃf¢|3©Fó2³íÃ\x0002×Ò\x0006J½pu«Xë9Åe\g3Û¿,r­©}É3\x001eð]á\x000bguISä2Ý<s,Ó%'Z\x0018ss1\x0015Êrú\x0018\x0015X^¢^sáTX\x0013TÓÞ÷åæõçOï¿Ü¼úôáÝû\x000fWèJP\x0015YpÙ\x001aÊ\x001cN \x001b_k1öêæõËçO^Ý¼zþôñ§ç\x0010N:%!æÔ)i\x0013õô\x001cMAO®_²Öq\x000eR´+Ý\x00166rêª&\x000e§J"PHU\x0017¨vT	,\x0003eâd\x0006W\x001aèlåÔÝxâO!§C\x0015ÕjpJàªªÀqB\x0004Jì\x0003\x0019m\x0004µN\x0008IÔg\x00031$WçÛò>³¾\x0007Ac\x000f\x001a \x001dÄ)L©éê\x0005Ç#
kRÆ[A¡_ñ [óò1YÓZÂ\x0000C]óØæèJ3Í¦Ç4RÌìæÐ®%0ù/òNñfÐÐ\x0006!¨ky2:\x001fK=-%Ëõ*)¹Ã\x001a\x0002É¾\x0002É¾Ê@CÕÒÄ\x0011\x0005ÎN1`8ýÏ¬õÍÚ\x000cÚ\x001bQ'5¢6ò®§þ?F·	zÆ\x001cãô½\x0011õR#
¦-ùì_V¹°dæÝ´Ö\x0003h+h¿{jáö	);!1N_Òß¢o_>I­½ò'÷\x0000Ø\x000c3/ùß»²õÏî?¼ýöþËëºär§°×N¤õÏ¯[\x0001eÆÁïßÜ=AåúgwO¿óäÕ«ó:%'òz\x0008\x0008\x0012À¸©H\x0006
ÜØû:Ä¥9\x001aÁós</Á\x000b»cW%C
¼º;s\x0018\x0001sÀ(\x0001tMóÊGBÕQçÐ±ÓË#ì&Àxâ\x000fç¿õ¢zöéÛ÷Wû}cïUM\x001f7pð$Û\x001c×¾îZ×gÏß<}r\x0001ËÌ±Ì \x0016æªÒ7­\x0001JÎß\x0014üj"ÂZ´Â *SÁ(\x0015å\x0012b\x0007¼\x0012\x0008ª­\x0004·Ò§öúX¹9\x001b¤È}ñâsó"°(å¼cs\x001dËÏ±ü(j\x001dÎTâ¢QT°çÑZéòz\x001d+Î±â(f \x0002à±èàwF;m#US¥Aªìì{n\x0007ÒÔ¾P,¨ÎélÂ®uP££åXÌá©NÓÜjM`å|«·Zf+ê&Q\x0010S}d\x0005¬WÂ@"û02\x000b\x001dÃJ:qwuguË¶o7Ó¶è\x001c«³\x0010zÐD$,\x0018ú\x000bµ\x000fË÷ÂB¾mT¡£
TØ|þ\x0010øà\x0018Øp­v´ZáºW'©#wª¦<ýô5ïÔï~}÷ñëÍ\x0007·¾:f5{\x0000\x001fn<·\x0003\x000biÙÏêéó×y¯~üìñ\x000f¯o¸õ\x0004É85sX#õ¾Ý\x0000\x0007KÆ\x0016¶|¹Ü.e¬vÎje¬Î;ò\x0016Ag1î\x001e
ÎbÈHaN
Â)\x0000xY]û-'\x0014ê+¬\x001c<G¡ÍÕÍa\x000c\x0016uy\a\x00175\x0005bXv
Áú9¬\x0017ÂÆ\x001aöÇ\x001bw`}ûÌØd`n§\x000c6Ìa\x0004Ö)Óú\x0006 Ê\x0010Xî\x001bQNj°Æ9k±:Ç\x001bcûqX¯8&ºÅÉ\\x0006æ°I6\x000b\x0012\x000bÚ\x00166§e|SDÚ< º\x0019(Ù¸ZÅÑX\x0014¥æõ¢>h¾ê~ç\x0012m]\x000e¯é\x0015u92|ã¢ÀÍbÃÑv[\x0016í].3¶ô\x0007,q x'\x00161ÓØ.Ëhñ¶íä \6·~\x0017ØMîß¾}ùúþ§kÉ®\x0011½MO+©\x0006k¼²AéV¸²0\x0006­Û\x0005öû·7¯^?yt&\x001bW¶nVµu³\x0004\x0012l=MdÈH¹j\x0019²eWCZ:|cv\x000eiÅ#Ù 5ö¡är®x¡aÜ\x0016ÈËL-C\x0005!û¨®ñÌQrsJ>8v9
Qú4§ôI6ùÌH\x0002MÑxW`¸ÊÙ\x000b
¸6PêYw{\x001cËèEèOQi	Ê\x0008ÚúÉ\x001dß	Û|8Ùi¦öÎeñ¨ ÃD÷(\x0013Æ¹\x000b¥æ|Î\oiµr(\x001ed*{%µ\x001cÀÙêäO\x001e\x0014\x0017*ØåuÖ\x0010eê&f¹\x001cÌLßtRñÒg¦æ
,©çÒ\x0006L;í\x0017S¤£\x0010Óð­p¿y> s\x0011ÃÒÅ\x001b¢
y
¥Wb»^\x000bsµ2¶6¯+ú³tÓ\x001aÔ¾ÍÇÆnóÁ"L¥¹²\x001fø¾NMk}äÚ¶e@r\x0004\x0013tgBÄ´Gö;tI»¤R\x001fMæq'Z#8õ7ÀÍ\x0013U~ûé\x001bÒ¦ÆWóÎóÁî\x000e°µQ
\x000cFÃQ\x0008ÿÔÊ\x0005Öo¿Á¿.Ï]`Á©Ã\x0001î;#¤¬w\x0007µ\x000b\x001c_Äh¹=;§r:içVi\x000cNiç+¹ñîLÏALc\x0010ÓqàXô:Æ\x0016ÜD×i'¥S:\x0019eÆ¨ë'c\x0006Etõõ/;\x0011ý\x001cÑK\x0017\x000f°ÚaðsÐb\x001bÈ3­é\x0006)Ã2\x0008\x00072ïZ(bz?o´ÄËÒAÊ8§Â±ä«tüÜ­ÉZH¤\x0010oP,b'fc&á`\x0002©j`\x000e©iéÌ\x0003 ÞQ\x0007\x001aÂÝ¨nTF9K~Gýæ®\x0012ó2âo®ãjÎÔFÊ~ó\x0011î>X\x0006È]Ã²]W­\x0010K(Ý²ÁÂ g·ýháþã0R[of£Õ­B\x0006¸Y²Ç>äû8»ýG\x000b7 §Õ-uËÍ¾\x001cõ\x0001ôM}Õñ3\x00071»ýG7 j»\x0019\x000b­\x001f%ª±á<Ó#}³Û´p\x000b\x0002¬M¥éÝ\x000e\x001cesê_\x000ebv»nC\x000f?Ý>¤\x001b\x0011X;u>Sõ²×ùÈ³óÌÁw\x0010³³ðZhâ\x001f~8Mg<Ôu8N­OV\x001160züéÛÍoÿ¼öµS¬I|\x0018ðp\x0014w\x001e»JÔËjµ&Ûò77/ÞüaY·_¡fE?(Ù1(Ì ®\x0017¶Ý
Lõ eg\x0014@Í«l5UÙ\x000ePÙ<TP·\x00170¦J`Y.M6«\x0012½©é¿\x0019¤Jµ´'UÐ\X6£3µ\x0001×©ÌLÉ[c|ÊQdJÖ`ÑXÖ¬ªÏ4
ÞB4G¢I&~\x001bµ|
06rù1·62úÌmÈ\x0006(i,`¶CPFGÜÿ\x0011JGV3&pç7\x0015Ö:\x0008]¢ÒÖu\x001f¯ü\x001eÀ*áwlú2XÔÜ\x0005s\x000b¶qMòs)OÅ@H,\x0017\x001fîÂ¦Yÿüt­[Z\x0008¡fDc\x0002'±ÏÆ#bÝy^<½{½²þðü\c¯x\x001aõ%ê1vòíb0\x0014¸ã¨ebÛ&$;G²££ä(F'JÂQj¹vK½MH0G±Qi\x0002kUziÎ³#ù!¤\x000f3Äw9Ø­¥o.+Ò.\x0013)ýÇNÏ\x0004'ºß3}¹¹ûuC\x001c¥è²r#MC'Vo¦^\x0011«aÈW7wÏ²°XwlÒ¿F2§FÉüTÛªj"`=ò;¾G¥\x0018ÒF´Ð¡q4§fý[é\3ù{\x0019È;%[û±ûqø{æÓ\ë\x0012#[öØÄ\x001a.Ý\x0010¯\x000c¶§¶ez¿úzóòÝÏï7Dh)E^q\x001ag>)süò\x0012\x0006\x001dÑW¯o^>þÝsþ§=ÉñF 3\x0006dØ;Û\x0016åÀö9\x0005°MLvÎd\x0007\x0007Ér¯\x000fjÜ$òb¸\x0012\x0016Ë `\x000e\x0005cP(rMPÁsÐ $îUìôù+ëPn\x000eåÆ °.µ2¹ÄâUQs£qHËd³mL~ÎäÇTK
ö¾E÷óÞ\x0018wÎò0g
Ã\x001f\x0002Sh²4GM¹M\x000bÑ
Ú\x0006\x0015çPq\x0008*\x001f§0ß¢BEÎ\x000f.ew|½4J#59\x000cÐ´³Â\x0002\x000fÎ"¨ÙÑÏN\x0019ðç®3RYJ\x0001Ís#v\x0010Ï×\x000b4ªÅþ§Ovt1åw\x001fzÿîãÇw7ÕY~~\x001dÈÖ÷¶¥g÷ËS\x0015\x0001Kñáyp±+æÇÇ?üðøæevã»\x001f«¹ßúÄÎâ\x001bØÞ D\x001en½5®7H¾½ÁqünÎï\x000eâm5ÖqDË.&{½gº2	ÞÀ\x001e«Lw¿üèÓ¯_¯º)xOK11¤XöÅÙó[\x001dú(?{}Îµ3§G+Ó](oÄÒ\x0019\x001cÐ³£\x0019`\x0011wëõùÄµ:^v\x000efÁ\x0014Â¼Ñ\x0018\x0006ãdpgWJt®\x000f\x0018Ì¹`K{6æH1ðÒK\x0007lõ^îÚ¹9\x001b\x0005Sa`\x001ekÁ
jáO»ÔÚ8`~Îå\x0005\\x0007ÌðÙ!s±3ìÎ(\x001co\x001c°0\x0007\x000bÃ`P\x0015^1;Aãek\x0005cõHw®Â¶\x0001s®8ÌÅ½àQ9/×Rl*ÜúÍïµ\x0001Ks°$\x0001mÀ&0Û\x0006L¸$gw¼¦¿ãÝ\x0004æçÈ\x0016Ü9
\x001b\x000b\x0007L÷6ÔèûÔZÐ\x0007m[:Qâ^[\x000eÎôÚÚ6bqÕ£Ö5ÿwò¢§\x001e`ÜÏÁº6Ç\x0015¬ÎéQ\x001bæ£k	$ØÔº¦E\x0016:pn¥¶ö\x0002XéÍ§Ü,\x0019=»\x001fº2üÛýçÏÛî°K\x0013åÄüGÒÏ*B\x0011õÎ.,ï\x0000fÑ»{ùrý2¬FFN"¨\x001b\x0012\x0005\x0004\x0013_.úõ¬Úm ÉÎAzÝÔ@QO6ÔÈõ\x0008aY2\x0006jæéØ Å	I£JÜÓO\x0019à\x0002J\x0005#fÙt\x0010Õú\x000eÕz)j\x001eT\x0015[«¥t¥õ#\x0015y,ë\x0006QC7Oñ§\x00105[CBóé¸*\x000eæÀRVÑ-\x001b£¡vIËê$iy\x00085\x001aÑ®¡Fª¡Ò=xF:d\x0010Õt£?e¨Ùáf¢Ùÿ¢m\x001dxùÇíË¿\x0017#LÛSü)§\x00152ïBÔûHkw§3:¶Ãiûá´òáT|iãI%ÝÚ;=<+¨\x0018K¡âO!*6\x0005 Ù­ìo{úô\x001b\x0004ÙNÔÐ£\x0006é×¯ÕñUÉp["íZcÍ°<\x001a\x000cÌRá(5ü	­½'Y#Ïê¬·f2î[ÇS«Ó\x0006¥\x0016r/>Ü¿ÿxµõN¤¨5¶÷#
4¨­»ßRs¹K®ñôîÉ\x000f³ÜúÓ>&5sÒÓzm¤ØXÚýåý*içv°L"\x0013Ú9éiÍÜÆ1
¬±è\x0014õÖÆ1ÕmP!R\x0011*ÌQOË6¡®éuP\x0001ÓTê~\x001fLân°Ìã\x0011¡º9êißÆQõ,fæT¬ÍañÂªe3êå¢­¤aNzZ¶4;|Ü)<¤ÛêA'Þ¬	K¡Ås¤Õ4­aÆ9æi5Õ6Ì¤YÓ7#³§,×ÈxÁnæLsÎÓâ´m\x001f^~m§©xcÂÀ3q¦\x000bg§­¦ F6C½­á:C#5X3º¨\x000b÷ð\x0003StÖ/\x001b\x0017ÓiÚ6Ö j8\x0012\x000b;M-\x0013È¬vj8»Ì²°úuQP·ÙHA3§µT fLêÎÃ_ßwFßË¬¾õµûCmá««²n¾-û\x000bþÓÈv3ÕËf*:&dKÃcTa
mòËvÃ"ÖÎz5u
jè\x0004? «Ù`Úø/\x001cI\x0007Xï,Õi±â¶e´u\x000e\x0000:VUÑ!4Ù\x0001c·m§&«vÝ j'Û£¥5åqMÑ *:<Û¼ä6Ùþ+ªCç¢è rR ¸ÛXg7Ò=0èC£jÝò\x000eL\x0000ktg«ð§\x0004ÖZª÷ÆªãÍ¹\x0008\x0015.\x001cM\x0007PMjd¨ª\x0014VÌ\x000e©Î_4aã²\x001aG\x0002ÛïWF¶aa+ZEùUW¯lCâÎÕþ½ÕôÖÕÈÌ«Må£¬¼ÎTÝ±¢²­\x0001ø\x00155°¡s\x0002ñ§hwmö\x0015Ãè$]ÿY*E-æ\x0005°xí:?X\x0005Ñq5\x001fLÚf KC\x0014õÑòye) &b=«h`M±®yXµ¬$yÎÞ±Ø\x0012å\x0008ÖÔyØv!\x0000±Õ§[ #«Ñ¤/òO`à\x0008ß\x0005l·Ç\x0015m²Æzv]±=)¨ù\x0016	È3÷I\x0000Ð-ü)5±\x0002(A\x0011Öq3¿ìg/\x0013\x0004°N	D°\x001a)i\x0016p§ä4ð$æ}\x0016\x001bîÎY­ÈÑ\x001e¸Y\x0018T½
«ÙÝ6ÇÀB\x001f¹\x0000Ñ m¨÷¹\x0018fi
®!Äæ\x0017\x001ebcëÂl%Q^\x0000\x0017?~
_Õ
\x0001f²5G¬/\x001fN\x000e\x0007¢i÷,\x000e°C^jÕÈZn;Ýí#ìVè\x0003­øS÷T\x000f] \x0014o\x0008 YI+{òG\x001cdBêL\x0001þ\x001c\x0005l\x0010H¾¡¶Ñb\x001f\x001bUËú|\x0001l´}\x001cËJvZH\x0018¾ª¶ o«­Ï5Ü%í<"æ\x0019GÄ	\x0016\x000b#\x0016¬Ïî¿|¹êu>À0]Ê'ï\x001av	\x0010¹;´^VÞu¤Ïî^½:'eS\x0001§-\x000b\x0001\x0017;Ö&À\x0010oIm\x0007\x001b½VÀ¨\x0003ëUÅ\x000bW×\x0001§N!\x0008èN\x0000Q5ÏTBªà/ªüñÇöñÂÚuBoæþÔn!´àni\x000cm
ªçÏ=µÚ>Óá\x000cáÉÕT¨íô\x001c\x000fó©|ØSÄ§\½äÏîo]Ýã²Ra3_ìù$kÄhwKýÜRÔm^æ g'?\x001fV/o@\x0017ø|7\x0001õBÔmÓ\x000c¤þÌyøò\x0004dÅi\x001bÌ Ï\x0005¼h;¼x\x001aÜ
0\x0005Oçí[ÕÛ§`9`\x001a.¥\x001a]Ãs=Þ©3´iöUÍ±<uó£Î<ÎÙÉ\x0007­+\x0002nØú\x0017%3\x000f
©à%Åhu§¬\x000fË\x001cÝí¦Å¨Î´àOm	.ì4¦æàùÁ\x0013\x0011.e½\\x001eA«;>ü9ÌçVMû\x000e#6$w\x0018xmxu9òqq\x0004mo]*[\x0008cPXæZ\x0008\x0003õ/GçÑó\x0008ÂRüë\x0008ºnÿµH×&>oèÄGÐÖ\x0014\x001cÔ8ä{àÂ\x001dØÎ\x0000ÚEDv\x0013b\x0006q4ù8CW±69^Æ{v`°Ý4Ä-\x0004LMjÏv&zÉºEà®Éÿ®cÝ\x0000Bì F\x0007Ê]Ë-\x0012ç\x001d®êF#Nw6Ú-\x0004u·9\x001eMK5Ó¦FÜ\x0017Èk$\9W­óyÓ­\x0011¿\x0008]o²ÓÀ½÷òçµ(&\x001bjàhpÌ§l)\x001ft\x001eViy?ÎE(\x0015Ï¦ÚIªÜ\x00070Z¦ooÅë=h/r¡\x0015¦zÐ.\x001c,«c\x0007Ó¦½PË~/ô\x000ej8¨¨ºÅÓO%}KÊ¾û\x0000\x0006%´s\x0006ïm>zt)SßãYDOmÂÞÿýÓûÏW\x000e\x0001ã*÷"÷0K*´®DË¤cn\x0011öôîÇçO^.¬^\x00033s03
fJ7¢*ãÀ=\x001e±ê\x000bò`éX]\x0001ÃÆrè\x0015à¹ïl\x000b÷ýû~Ù X\x0015ëåv®Æ£c>\x001bë\x000b[Ú«ïÞå_ã+)Ä9)D	©rþst¶f^2ÌÛIg:Ý4z\x0001©M­
	³wxL9
n@]Òm&Õ3°\x00082\x0019	j\x0008,Ié©y1Ù`ûËÙï[AgZ`\x0008j´\x0004\x0014N\x001d¡@-oA\x0005.\x001eYVPA={O¶ç´"NØ©:2ÿ¨O\x0004¥¬[6ç\x0011LR¥ÿø¶cýîí0ª\x000bVs\x0003o\x0015ÕÀÆÝ\x0014ó\x0017ÎòWÔ>
6ÿ\x0005ÚôY\x000fô\x000fÿýÿõøç\x000fï¯í9àQÒµ~z\x001b¸F-ÆÄµögZM}ÐÞ<þÝÓ'g}ZB´sD+D®	Õª"íÈH9[Xhr¡WûuF7gtBÆ\x0000·héV&æS=ogr
G\x0010Ã\x001c1\x0008\x0011¯Î#Ê*Ø:%Qµº³ï¸k\x0018Ó1I\x0019)D7Æ\x001aE£*£oÂ\x001dË0ì\x0000£îWtÉ8Ù\x00152ÂVl\x001d]Õ2ì¾
ò´nÞÎêæÑ|ôíóU¸Lä'
:w\\x001e\x0004qÙ^K\x0002Ñ|ôæå\x000503\x00073£`yéR\x000f8cgM$3IU¬\x0015¨_\x0007³s0;<b¶¦YÕ\x0011s´vÝ\x0004¶t»·Á\x001c\x000cFÁ¬­úVh\x00150c+JàVª;/¥S}¤æÚ\x000c/>Ü½ÿx]\x0014L\x0019\x0016ç,j-$Î	\Ù\x0005°Ò\x0000\x0017!=½{}÷ÃÙrtÚ7©¹BÃF8Ì Q\x001bGª!ª&ÑqF¡s3Ùñaþ68r³¥\x001eÃ4ÕÌÚâÜ\x0002\x0007s8\x0018óÀ}´Qp\x0006®µ4>sÚææhNæÚñ$j.#\x000eMÜ\x0002ÌR@p;Ãùq¸¼áSÑ:æÖ2×èSä=\x000b?¯\x0018.ÌáÂ8\x001cÖ_QoÕàné£ê¶çóâ\ÛØâ-³Y;	U\x0002©ÇÔlÈªlÃU´@BR@ÂV6ÔyáöÐ»V{ßüâ3é÷Ûé:\x0003§Ç-\x001c6\x0015¶ÓÐ%\x001a9IÈp××êI\x0014\x000bÉt\x000c+¿\x0007Ù|ñÖkWe7³-x·ºÅ\x000czyJ»\x0006\x0017OÏ;1Ì:É¿xÿîO¸«¾øôíÃu?]±`«7åh"ö ¯CçWT_ÞÜ¼xòø7¸·¾xþæézÎÄ[eôIÀ-o\x0019öwï7u\x0004åY\x0000À\x0000IL\x001bÏzzni÷ò\x000cþtÿ§û/_³kÁ8Å9\x0016lÇ²¨AÒ\x001cÊ\x0010ñð\x001dX}]-c§×°ô\x001fí¾Þ4^åV-àw7¯îßüzs÷ñOï>}Àßß¿ûüsÓ¤Ì©+âÇwßþþî_þôî_ÊAuvÉh·Ñ\x0001Þò/¬<¶\x0018ü§¼ïºægþðøÍÿå7ÿåûÇ/ÇZÁo^Ý=ùáõÍÝ\x000f¿yüü)þ.ÿíù\x000fÞ½B^ÈæWp¥\x0012¾MNjù\x0015p-W°Óú>ö\x0015ðz#Ú#Þ!dRÌMÂwÀà²+bSJMï`¦Ë²ß!MtG½jï@/a<z\x0007GÙ¸}\x0017Ã1/P[÷\x0017pz§\x00026hâwx WÈ#þçWp\x001aÅ\x0016ù\x0015ja	ö
m¯ðPË9ÏÔïÒ!&	Up0ªÁï ë;$¼¥wxWÐ\x0018Ð)\x0003Þ!"Þï\x0010ð\x000f_!bï§ú
zÒ½;ö\x001d0¯<\x000exD9\x001f'jÔ\x0006\x00131Ù ©©ÛÖ±oÕå±ÿ
¢ªiõø\x0012.[-\x001e^ôãKdÿ4=ÌKàS\x001e\x0007¼Dö^ó\x001a¨/\x0001T\x001b b[Ò>M×Ä¾Áòò8â%R9õáKXO%
ÕLé%¢z\x0005a²;ð]y\x001cð\x0012Ù¸ò\x0000ÍFÂôEz	û@_Ââ°Ç|	?íÒÚó&ðÆ²¾×\x000f³&\x000c^
Ç\x0001/Í+	]j½ÊKà¡¸¾}-¢¨GÇ\x0001ï\x0010ëe|y\x0007HVÉ)²°þ¡5ÚVsM·jmÂ '½\x0003¨z	ü\x0010þ\x000fêKä3Ä²TÂ\x0004Xz\x0007ò,f5Ç\x0001/»D]ÖÆ)²MZB§ò\x0012\x0018U|ÀÐuy\x001cð\x0012^ð\x001b¾e§C+¥p³Äßc_\x0002¯ËãmQ¦VØ&¹¾s\x000fã9\x0001nÕpÌ~bs:t^"X2N\x000e\x001eèK/\x001c±°
êðÂÖx.ªkB>Æå%ô\x0003­	ø%â\x0001_\x0002_Âµ/a=¯	m#­	H\x000ft°\x0006\\x000epÄ0ø/ã½N×R^Â\x0005Ã/ñ@ç!ÖÕ\x001dabóK¸Ð^BÙö%¼'\x0013\x000b\x000f\x0014¢)åqÀ;xßfS6Nµ\x0003ÖÁ\x0007~\x0007x\x0018ïÏáÔ\x001dq0Å\x0008ìu(ÓÐl
ìÂ{ u]êzÝ\x0011î_~à¦°ä:a\x001a:¿\x0004LuÇ¾\x0004º~î\x0008ÿ\x000f_¢º\x001cÊ³tA~\x0003ÓI\x000fõ\x0006\x0006ßà@
¾A\x000b6©ê}Ôí%\x001eê\x001dp*\x001d´ÏMu)Ú£}\x000eã\x0002ô\x000e\x000fc<.3ÄÙ:¿C2¼W+£ù;\x0018îw°I?ÐK aõÇX×bRk\x00009\x001fQèXªN´¦mäÒ}	4¬þ ëZß\x0000òá§Ñ|\x001ddý\x0003­\x0007VÕ\x001fcZµæ8
\x0014g^Â*þ\x000cþ¡æ\x0012Füü\x0011a¿ü\x0012\x0006ÚKxî7¬M;\x000bY\x0007K(\x0005P\x001eG¼¯o\x0000Ï\x0010\x0006ØsµXwð\x0010o\x0010Ð$cì®r,õ%|³K(\x001bO/a\x001fæ3\x0004Ü¡Ã1Û´\x000ePDqóKÄ\x0014ª#:â\x001c}5!>×ÏW\x0018\x0007WGD\x0007Êôü)|Jìö9\x001fh«V)<È²ÎÆ\x000fßÂ\x001dó\x0016ÙÆÑ\x001e]\x000bË\x0013*FòÀ±xèABf:â\x001eWûß\x0002ÛæV·	Ðå¨;]þkS\x001cPä\x000e|¿üôí/ÿø;%ÇõÊÀùeþþî?}(Ù,WC\x001b\x0011+ð3·i]Ü!Y
5®a­^CSéX~\x001f\x001fÿáåó§«y-3Þ"ºw¢¼7J\x000cÀn)= @ç\x0003D$èìº\x001e
\x001d0! Ä=Ã\x001cU´\x0019Hä\x0012"X\x001eh\x000c`\x001cÀÞ~ýâå<ùõ¯X;Xf÷»Ï5Sçz¼+\x001bvç\x000còÀ\x0015Dmùj'­à>yö\x0002ë\x0008Ë~üòåjÅLZç°\x0010ÕnR\x0015Êz\x0014¤vV\x0016\x00084o\x000béÿ\x0006P\x000c\x001fá¤_¿V\x0001+VnÚ_¯bÒÚþ(b\x0005¼¢ÿ¿bT=^ÅÿÏ%ýü§¿þüç·³|¸É\=½ÿøå~\x001bgB!ö²öR@Jù\x000c\x0001Õ¼æÃuSõôîWw[@qûíuÃGH¥ ;@¾\x0005¾¬\x000eLªW|\x0007	i>è &
tÏ¤n
½ûFºv1(!ÍÓ$\x0011©Á,\x0019SÃ\x000f@î|¯n>Bª9Â§`¦ø³eRX³Rã¤xpû®<d¨U\x0017§ æÕèÔä,:·\x0012E\x0010bZDy\x0008I\x001d]9fÒ\x0016Ô7¥m@E]K\x001e\x0015 \x0006D
RT¼9©çl§ÚMU\x0018t¸î»nFå° 3TxîO4ªAvô·¥#jAMaÅø£\x0016¥è\x0013¹è\x0001T£TCÅ¶f4ªÉ¥2Æ\x001d¶ª¦Ô\x000bÙ¨&×&@hwü6Ò\x0005T0\x0016V®\x0002\x0005¨8íËC\x001aL\x001bÕ8¡º\x0008\x0015Ö2t\x0004¨8M|®z ­*\x0014¢º\x0001Ø|*$T·v\x0015 â)¢<£\x001ax\x0002è\x0005ðì©`9ÉA¨º:å)ó\x0000\x0002¯aÕÔ;@k\x0015B3¬G­+§0é¡>Å³5ÑlÅl@³u\x0002vï\x0014/æþÛßJ¢tþú©?ý½¸ÿòÓýO\x001f·Àj¬\x000c¦ÛÑí2_³\x000bH\x0000uÄW¬ÀÌ±Îxt÷ôù\x000f×y5ZÖò\x0010\x0003\x0007Ígëh#Ý9[£]=]¡¼äõÀvà)â"\x0006ÆxE=¸`£Ãj¼¬qTPâµÛpt\x0019\x0001F£`öLd83\x0001Ö¢Å²b\x0002^Í%\x001c\x0001Vî/éWÿÇÚ·tßýñÓûéPaÞ\x0014\x001aJù\x0017]³ë°f«\x0016)xµDX;oýøüÉt,Ì¨¿[\x000b5X7\x0019å!¥2ál+GðE" à®&ÌJpKkòâ\x0006à;HG9¥>ybM:®Ø\x0006\x0011ksg¤¬¨uíU·J\x000fÍ3!éµ:\x0011.&d\x0014\x0017o\x001djÂ×\x001a´ª`¸&"­&<ÈpÙ­\x0011ã\x001a¬ý®¸Êçó?(é*Ù°ru%Áµ¸û\x0010\x0017¾Sò§7-8\x0000ß´%P\x0007®3öËî0bÙ)í\x001b\x00117ó\x0011\x000b@\x0007GTz8rtq\x0003.\x000f)n¶b¶nÂÞ«6ºÜ1ìæxàÜµØR\x001eR\ì6G¸ÑTùn¬\x0001ã\x0016Ìw>\x0010\x0017Ýa\x0019oÌ×´~Ä\x001ax©%s Ý²wàÚj\x0019²·Ñ1.yz-(¡\x0005¼í(\x000f)m(*V6{\x000eUØ%ÓRm¬ÇcÑ¸è9\x0014\x0017+ú\x00197²aÈ/ûç\x0006\x000eÜÔr\x000cìð\x0017B\x00133B\x0015ÊÙñq\x0002\x001c](\x00107fÜÖ\x0016ò	\x0016o°æéJh\x001d+å´-Çá´ ±\x0018)\x0005Æçiqàæ0
Z\x001eRÜ|<«c\x001buÓ\x0002¨º¥å\x0018¡õVÌa\x0004¨<Ä´=Ýh|¹R7=¦­\x001dÛ\x00126¥¸Ð\x0016¢ShËèjCSWÏTa\x000fÀÅ0syHq\x001dð7µ©N¼Ç{äQbÊÂâúVO
\`¬ç3{ZãpËEÎOÐNì Zñ\x001fÓÕ¬2\x0011-\x001e"ü\x0004fC\x0017T?U½ÒM^vÕ×J7$¨\x0001ÅÊCT«ÑÍ;q\x0007ª*ó\x0014\x000b\x0007NÛ\x0016&ì8EÄÔÒÏËå.­²H£7(ö~\x001c.º5aoÔ\x0014\x0019«wÑ\x0018(-	-{à*\x000b\x000e\\x001eb\\x000eíg'ãåy2Ð~fÒZàQDNXØáa§Ç7³ÚJÄ\x0016bM\x0007z\x0001÷±°c3Ã\x0006\x001e5\x0014âµ¤â¦ñhRqíZF\x0016·±°c/KÆQÈ´s.\x0015GB2í^XÀ&ìpqSö½"ÍZ<\x00063-¥¯{kÌ¸Ñ\x0015\x0001 \x001d¸yÿª\x0017è²®\x0016,m<ÒàF\x0005qÏTp\våµåºÆ®\x000bôÈcQWÚ±ó&Çwþ^»VQ¢\x001cM\x0005ÐGNþWÚá¥æa\x0017\x000bÎú)âÝ\x0015÷ÈoBóöØ°Ðhmù4*Rj>SÚ\x0003÷ÞW\x0010iÇ=\x0004²JV!ñ}*Ñ:¥\x000f¥ÅÁÝ\x0011bJ#bÞøI Q\x0006w«iî\x0002\]®~ëSÊ÷\x000f\x0013ÚóyWÆ{gÍc©ØãÚd^[Í®UîÖS¦T@uá\x0007òúÂ»g±¥¼fón(yÍ{ÿ÷8C¦Ë·ªO\x0011.f\x0005FN\x000bÃÜUÅ7®e°Ixu)ÍÐbË¹\x0003VÉpº%°_îÍþ.Põ)ÅE/¬òÓ\x0014Îsc!>\x001eèërªåªÈ«±íCÆÍ6ú½híI¾À\x0007k;\x0003ërç§å7\x000bE
\x001dym"ÙÖ<¼\x001cà\x000fGÞMe\x0017¤L\x0007ñÖò\x0010yk««ÍA¸u°IFÈ\x0007ï\x000f\x001cßrÑ£å×=¨\x0004¡°ß(òzì$L¼­C´kºr2ÞXxã\x000e^E
\x0017ÛÐæ\x0002óB8r|Ë|°{æÒc\x0000y¡åc¡\x000bD¼îHóPî¦´ü
ço5\x000e~æ9ÄÀ°~--W\x0006\x001b
lØ\x0001\x001bn«×\x0007Ïk:)Æ
\x0007Æó4T=JØ1\x0017<Ë)å]¡U}\x001a\x0014W¬¼i­\x000eZÆ[æØ1Ã¹ë¨ÖÖû\x0014nYÇMoR\x0007Þ¡h(b \x000eD£þEó{K\x0002\x0006å¿\x001b>\x000f§Ò{ê8^SxÍ\x000e^7À×bÊË¦7iw ^2ÑêS<}Yù({	¡\x0015Á\x001b*-óÉ®	ixSá\x0015Ûp|[¨,ÔN
5Óª ×é\*÷£öIªW\x001eea\x0004:W$w`8GÛJ-¿³¬14\x001b°¹	°$\x0002[x`$Rë?-¿\x0004D%
Ë§6¼\x0011æÙ\x0010\x0017ëP\x000e<Åû?-¿\x0005,z\x0013¥ó	òúÒ¿«ð&GIçÊ\x001d£})=òâ\x000bw,éñ¥Shá53a\x0006ªÉñ÷ù\x0013þñ\x001eOãî»{y(=11VKhë\x0018¾t·îÈä]ì.xbÞÿ_sqßÖ\x0001~+\x001f`õXÖ¢ÿ\x0007Ø\x001fÕPÛ7¦ÿ\x0007øëÏÿûOù:«ó-¬¿ýôù§w¿ÞoÓ#(µ³¾ùdïñe\x0014K<.\x0007{ûüå£ÇÏî.\x0008\x0011Ì\x0018«\x00101>aÈ¨¡ÕÌ\x00009\x000bÁ\x0019»CÙÉ·BHvpó@\x001aj¥½\x000c\x0019/&
AæS\x001e\x0008 1~§n=UJåËrU¯áú³pÑ°\x000eAV1\x0007ÑHzlJ^GÒRÓ<­Hîrq\x00082\x001fA½p$³§ô\x0011ZÉYHCùep Ã-#Ü\x0006
ÇØÄ%Ñ\x001f6ÙÝÂq´\x0018x©\x0003\x0019\x001a$ø\x0006¹¦?\x000eYU;\x0006ÈÒ×6ýÓl\x001cC^e@\x0016Ï_	r²@:¶è1§ÞcAÆQCu-Ùpª	
d²[\x001ayåØ¶ãÄÃÆ²4.\x0011Rz¬\x000c©êf¥Sí_LJ\x001c$\x0016©
â¡låä\x001a\Ûr.^v
Q8²h
²ahñ8*`A\x0017ã°±\x0017à
Rj®\x0015\x000c¨P\x0011#[ó¤Ú\x0016Y;F4©t\x0013$\x000fÃ²Zôä«­UdSb4U²é %pÑ0*34g-6<ß!J¼\x0000\x0010n;Z·ñìcxòÖP=}Ã(\x0013\x0016Z­¥¥­àÍ©\x0019Jk=)Ku°pßÉKÇéÉÏ\x0008¼z\x0019º\x0018Ë\x001b¢Ì{î;¡\x001dt¬¡Î´hø§5éqJ<é\x0008÷\x001dÍRFewdÙ\x001d¸ÝdtÛ!@koù[[öÍÓÅ\¦!BÀ2ÂQt·l(\x0003^IÖAdí¢ìb\x001cåø²n\x0008RÝ\x0002-\x001b\x000bØí´\x000e¥kÒ\x001d6\x001e\x000bÊ¶ÑîøméR¨sµæ<ð¦
]6ºÀ>F:ì¨½µtÓ-aR3Þ5Êaî!JÒþ\x0012 ÅP^=¼é$6çéb]á\x0008¥-µÑBÊt\x001bÚÎØìd°mg<QcA´\x0011¨4CF*Ïª¹Ù!¬±Â-';åºí!§Ï}ñ¦s\x0008\x0012kÂ=\x0007¿	2Ýz:éxÃV(\x001dfð0bÛ\x001c¡¼7r¾NPÓæxØ¬ÄRgé¾\x0013°åc¡\x0004Õ\x0019\x0011V­)ûSz,w\x0017åä\x0008åÝ1pG\x0016ÓÖÎJú8e^VºïÄ[ \x0007½ª\x0011×±ô<\x00175P #â\x000b²yCÖ·(A¶vÖZC&,ÀÛsZá`©')\x001aôÀCy1¥\x0012J?0áPúfB³Á·
üb5å\x0010d6º ÜvÐ ÓÒÉXÍý¥r<\x0017/ÿ(
\x0002\x0008)'g(oÍXÆv\x001e;,\x000e=åA¸ï I§8\x0001¸R\x001b\x001eËÃ>8^êH÷D6ewd[\x0019UÛÂ/
ð\x000cQ\x0016Y\x0005\x0019¥õ,(¨!5;\x0014§i¹¦|7Né±Y²yC 'HÒ8;rsÄë@\x0010n;Ù¢kò~±9ûE·êbmÙ\x0010dÄ}Â4·¼5N~e´áð½\x0011{³pÛÉ\x0006ÝÍ&¥=±èV],ç\x001f¡tE4C8\x0016µ~xslàn²èGAæ·uÒm'4H§p~A×\x000c\x000e\x001bJ\x0012\x0019b[iÈûuú\x0016èà\x0018(:X,m:\x0012°+ØVò¬ô3S9í:Aâ5½Ô «vGæ\x000c	©¡­äY©\x000f»5ÁH\x001aôÉÏÉgKmV^¬¡\x0018\x000c(-"ÞuøöÉÙÛÈ¶dX\x0010v\x000c$â½ô{\x0007Ò\x0018ÊùÜÃ#©xVêÃ\x000e\x0012¥²]h+³\x000cô½½G¿¨Rrn¦5e4a©LRj*ÉÿÇ¶µ,HÍ¢\x001fgÒ1£'
}tìùBGÇà8oT7Í^¬­\x001d,Õöâ\x00085¯\x0010ZïVß á¨,¥ÊÒ\x001dò±\x0006Ðê@r\x0014ÝÚp[É:Ê"H ÊïBÉåMH}½9Ñ(¥¦Âd±EOäY&©b4D	kÇ)K½¬tZÒ\x0006^U).Ä^»(d4ÂhjÑ©|$«­4ZqÖr\x001eI¶þ¨ K-åÞ\x0001wÎ¡õ\x000få[pë
þNM3$µ³G0FñÒ1ãb9ê{Z\x000biè×²
T\x001eHÏIÔÙÏà\x0005î¹èZ0&ÄtMÏßØY·UÏðÃRÄt)\x0014óÂ\x000f\x001e<7s0(VÆ­H9ÜT
kú¾ÓA8±uG1Þµ±ä~©\x0001.kI`úa©?õv5e°ÊÊ\x0019-Sªµ^ÍÃ½îù er\x001cÂ2¾Ý:\x001aß\x0006S\x001du5Æí;#ÝzRóLlÍ»çÐ*\x00188È`â\x0007úÎ\x0008­\x0011&©5²\\x0000\x001c3ÂEí\x0011ÆÖ\x0008GÂh¹a\x0017\x0006Yx(­QÀ
e¯p?ê*·ºù\x001bV±§\x000eî¨tô\x0013qûQLk\x001caÂ­'JÒ\x001dt<Q]\x001f¤Ì[ÚË­ûkâpT&I¹:°Â%>kycÁ´NR}"\x0008G%@Xô-­ÐÁDLKVqÈ cz\x001eÌrGC8B\x0007S§n4É{³­>2æQ\x001f½¤¼\x0008=Ì¼\x001f4cdZÑ4(ßFó¨° EÏÍ
Ý7cÜ4mû\x0001Ë~\x0011\x0004Ðfn]Ibj>üX\x0003\°\x0005f\x001aÍ£|\x000eæÒ
m¦1æ-»%ñi¤ä©éÌQ+¨oN0HÙz1çÁLí·ÝÜ\x001f\x0015\x001a,!\x0008+\x000c\x0015\x0015	³@Ùa\x0008ú\x0002î¨\x001cà"óbn¦Á;\x001e:X`Cñ@É\x001d
á°8\x000c¨\x000b!ÄôÓi25M\x0004\x0008\~\x0002Å\x001cÙõJ\x0018Ä\x000cÐ>º²Íj&®yË\x0002ã#XÙ\x0000Â\x0002\x0014O@v}\x001bëÙ\x0002b`sd*\x0001Ü~@º\x0007Ô@¡Åb q\x0019è£1¥\x0015"\x0008Ï\x0016V©67C¶uÂ>*P
¹Ajð
Vzþ#ôäæ+pT\\x0018Ð\x0016Ø E\x000e\x000c\x001bô6Én:Öc°GyqEòÄ	ë\x001fåiÆÈ\x0006¾çÃlc\x00181wÌ	\x0013È\x000bç["\x0008 ZÀu­Wñ0eè\x001a\x001d\x000cúÃÑLqB5.¦8áQ·S\x001e¿µ\x0017~pÌ+áØji
_\x0004\x001cå
\x0017)\x0013/4\x0018åàDÖ©jÞ0ù*\x0000\x000eÃì»/ÆXà(èh[0Ó·`¦\x0007m?\x001eC^\x001c'TÓe_SÚÏ+1ÍÎíÇ½
ÿë?þ</íùý·ûÏ_ß¿û|óèûÏ\x001b[Ob£hÚ&!b^\x000c(YßÊ\x0019íW¾úïßÜ½|ýäñËGÿz÷òRßÉ\x0013Ze¤Ámhgí³\x001d®^K@){P\x0008Ê[z\x001dRêF«¦\x0011]ñ6\x0005 «%\x0003õ®Z×æh¢ÖQ8¤+sT@Ê\x00122RàÝ(Â¤c¥&ÒÃfié:T\x001e"T¬"¯\x000b\x001f\x0002Ë½'ò^m{·ó?>`
  
  
  
  
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
<p><?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun</p><p>Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T</p><p>T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-6KyMaljSMQsdX7tNh0awRSvMsXM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-nrf/inGvBNNPsRxpEuxN8jRCmgc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-aLsBzZ6eVCGLnpqJiLe5RQDiEys`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-0xkAQmg3DmAJpJmrtZlPtlzhrpY`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-6Up5LpVEdu9YffpiEN2fhRN/pFg`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8105-/VVpB8fMPviSPvn5sH9x23dCVyQ`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-ZDv+pL5LmZCCRTBN5QD4jWrlFdQ`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-aLsBzZ6eVCGLnpqJiLe5RQDiEys`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-3AVFMQLLUfpBGnkTPsncUYWt71c`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `8f3c-Eah1KCechvTFD8nR17B8PKKgHZU`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��\x001a���1�cH�,u~�6\x001d\x001a�\x0014�2��</p>
  
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

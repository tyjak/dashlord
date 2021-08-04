
# ZAP Scanning Report

Generated on Wed, 4 Aug 2021 12:06:09


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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=zqñê[\x0004üÃÙù£\x0019)D¬U/bë¿Ø«\x0008S~9sFÒ
¿^Èf	ÙtCIo}
\x0007\x0003õyÐ\x0002âÉì>\x0015d»l»!ËÒs¾)T\x0005¾\x0010]µö÷BvKÈ®\x001b²\x0011Ä·ç=q&)[|xªµ©\x0017²_BöýR\x0011ÈRÖs=¹TB[^X/ä¸\x001cû\x0003\x001f,CVóó+Ë´}c5N'äEp\x000b:N÷ß\x000cZe@,ºNÎô%^>eõødÿëKÈ	\x000f0S7ÖOYUDu[ÿÉ¡ª¡ú/Æÿ\x0008fµÏÑ¡Ül°\x0001íÿÇþ|{óù°µöe¥1\x0011ÇVÐe[%ã\x0005¨G§ß½Ù\x0000U-¡ª>¨0E¼"ÖÓJ{aÊèñªý`!ÕK¤º[¨®!Óø´2µK¤¶\x000f©Ç$RW8%fØ Bí@êHýï\x0019i\"H
u\x0007\x0018\x0017¨Keâ­Íîºhô>ò¡Êúõw>ÿ\x0014¶ãje Ø+ó\x001c´?[´Æ¾ÆºP&u¨¦oû*2`Æ2g\x001a\x0017lk\x0006!U`}X**Ýù¬¢$\x0004\x0003)\x001c\x001aD¡¹¬F\x00136\x001fª©î*|Û«UiÜÈ¨ÒÝg\x0014åC|Ô\x0003VÆ=[\x0005Uo¾¹¼{ø257¼Ø=¼¿{¸ÿùèÍîæÓyq}}w{øY¢ïHü¤h\x000cI´¸u.®ÞNý\x000e/N®]\]~wôæäìÕÛ£\x0017§§\x0017ç?Z~\x00045þ\x0011L \x0016\x0014®AJ"ë	¢m\x000eß§ÿ\x0010zù!ô\x0013&e§tÉPN\x0004¥Óð±\x0011î\x000f\x0008³ü\x0010æ	NÂÒÔ2v{OÏ
?DkjbôCØå°Op\x0012:¥\x0007Va7¶÷­rëðpË\x000fáà$$m
PÉ\x000eeÑ\x001eDhõ ~°ü\x0010aüChOtIú3\x0011
fíS\x0004à\x001a\x001d\x001fBV'!à(¡í^\x0012¼ÂAîö?â:-\\x0005xØbüCÈ\x0016\x0010>àT¾#¶hhI{úOQéXó\x0004J\x0016¶kç\x000b\x001c²ãB\x001d/ÛV»éà°Õ}²Op$ÖJ¡\x0015¸G2/\x0001Á\x0010RÖð¨^¶}§-JÛÐ\x0012ÈóÀÅñéS´Ö8}
½g³ÅøR¾\x0010i\x0008Ç·-\x001d\x001dkª~\x000c_\x000cÿ\x0004§a\x0001ûô1RÐ\x0015qß\x0006:
ÕÚÃ4ø1Tå|hõ\x0004îGÞB2}LÔ,W.U\x0000cìcøXy³Sî}øcÁ\x0002	\x0015vÐ<ú³® \x0019þ\x0018ºþ\x0018O lÖ\x000eÝr9;\x0019Ì&?ê	]÷RC,gK^ú\x0019ô\x0018Ûi¨c÷ë§ÝCå®¿\x001c=O\x001féæövwhc¶\x000e\x0002¶\x000cV*t\x0002U´ø°­j­ß9ùÃ««\x0014Ì¾=z>ÇÙùùÉúâìØÔM'b\x001fp5!\x0006:\x0011kl\x001c°ºÉòß\x0007ÙÖm/äèÿs\=\x0011£K\x0000·Æû\x0000»\x001a°ë1:¤\x00008 ºO2FÛ\x000b\x001bár\x001fd_Cö½\x00179Dl¢ÁíBÉ\x000fÂÝ²V\x0016±o\x001fäPC\x000ecÒÝSJ\x0002ÞÃ\x0006¨t}%IY4J,c
9öJ9¹Ç.ßdS\x0006 ¡z*)¾­\x000cyâëéÓpÈÃ »û_\x0012d\x0019\x0011²mM£ö@Nfw	\x0019¾í|~°O.äa\x000c:éo bÝ¤íAìCeF|è5#>Ê\x0018h\x0011QÈ\x001a[dTa¸wï÷µÜûNÔÞå\\x0014 å6ÃÆ\x000bDÝ¢èE½ÛG½ëUÎHÙeíQÖ*Ä"ëq\x0003(¡%ÉèÙL»\x0017 1âú×yv÷p8M4\x001a6J\x000bEËx(Mìd+M|ú£ä
­g\x000b0_\x0003ó¿\x001b`±\x0006\x0016·\x0003³Z\x0003ÿJ\x0002&b\x0008¸ÐÆ)\x0003yÞúVóÈV`FTÀ¦¢Ê6`>Eb8æ-âD\x0000¸E3å­n5hmÆ%k\+·a%\\x001eP\x00030[5J|©\x001aÚ~Ñyìm\x0015Q9\x0016Oq\x0015
§z+.\x001b«o'Wß¨bF½ß.3Lþéß\x0013¸7>ýÔÓ%k@\x0019ÈvûÈvÛ%Ó \x00114Ð6¦&FÇô\x0010:\x0013ÊC{u.8\x000f*Éýp}ÿéïÿïÇM¤Ñp~N\x001dûÒ¾\x0015\x001a\x0019\ûáôòÕé·\x001b\x0010ê%BÝ0\x0014D©\x000c+Ãj\x0017Æff	Ð°\x0001&\x001cÔ~:\x0010ejÇ(©ÿ´Áë³\x0019 Ý?cK»q~üïÿøÏÛ÷×\x001fþx\x0008 1h6¬¶Ç\x0001»
eé?nU\x0007 ÷èäüÙéóï\x000fã3K|ÏÆcGC\x0007²æP´\x0008SÚ+ÜM\x0001Ú%@Ë\x0006(-\x0011#Yc1_æå¦"Ö\x0018ë7\x0003tK/A]\x0000'$ ¾®m\x0018Þ\x000cÐ/\x0001z.ÀiW\x000e\x000e\x000f+ê\x001e\x0016°r}ö©Â·ÒðàÂ\x0012\à¿\x000fuLR\x001dºA
À­\x0011Qn\x0015Þb²\x0015.·à\x0003g¯/${RÑ\x0003if\x0008Y\x0008UP±\x0011j3\x0008G\x0018vB¢yèz\x0010`¥b$_ÇÈ¤\x0011 ,^÷Ô¦\\x00185Ä
=ÉfÕ\x0013ü7,\hñ\x0002ó\x000cN¸Â§±º±c3ÂêHö;IÑ8µnZt­Lvm}ëVpªz#ýFVØd\x001d¬Ï\x001a¦<¸¶bQµ\x0001oÙ÷/\x0000KG´ÞpÿHCÇ5&©\x0002TªzÂJñß0´9\x0012ÃF>^Yv¶µM\x0019\x0001ú\x001a Û\x0000Ý­E|\x000egoh\x0008\x000eÙ\x0000C
oHR°V¦g¾ì-÷k\x0014ä!Æ\x001abäC\x0014´=Ã\x0016bþôuñµÖX(\x000fA|/§14ãç¢\x0007P·øÜÐxóij\x0013Ì±\x0004õæ\x0000P%,LîW\x001eÖÆ¡Â6Ñ´ÇºÎ^M}¹\x001a ="Sí÷¼k0\x000b¥wýùèÛ»Û×\x000e¯ò´\x0012v¤P%\x001e;\x001b<1iÓ¢kÊ\x0015¼Ó7Gß^¿<}õØL\x0004ª@U\x000fPQ\x0018>\x0013DC\x001fÊ#×¶Uäà\x00035K ¦\x0003¨tSC\x0019\x0001Å¥ëÞ©\x0002´ÅÓÅ\x0007ê@]\x000fPé\x0019<\x0003U\x0012ñ\x0002Ç\x0019@¢«
\x001c a	4t\x0000MQ(t#e \x0001¨\x0000(Ð\x000f\x0011ÐÖF\x000e\x0006P¹ÏÙ%õxy÷éËÝÃ¡Üô´(\x0012»lz\x0011Ù\x000c§\x00053Ø\x001cÜè\x0013ÉÁôËWo\­'¥\x000bD½¨ù\x0010-ÍZÀ\x0018'-
ÔjíìZÂd;B»DhBôK
1©IÜ= IZ\x0008Z\x0016HúÕ¬Óvq0þø>\x0003S\x0019J*\x0016ÐÂ·	Éç£g×?ÞÜ~ÎëÝÍí\x001fïnï\x000et÷ü\x0014émÉ¨+¥kçB£ s\x001eõ³ÓoÏÎß@IçõÉÙù÷\x0017ç\x0017!Ë\x001a²ì¬÷hÂì%®ÎH1%à\l\x0014¯{Aë\x001a´î\x0006-\x0015:xBB\x00149Ý[e4vã9è'\x0003mjÐ¦\x0013´Ú¤§lJ\x0006OËÜÏòumµ[Òs¦d½ë\x0015¶x©%P§çKmÈ`%?õë÷ÇD
y=ÇJªÅ°àÃÑó?î>þ\x0002ë³ëÛÛ»O\x001bÆä5qº\x0001ím¡ò§Æ\x001aA<\x000e·\\x001d=ÿþäåkð^_¼ztÈe?s-\x0017ë\x0002àn	Üý\x0013\x0001\x000fKàá\x0007ør\x0015µrÿ4È«×)ÿ§¬§ü'z²zrì\x0006"b51b\x001b~JêP¯O|ö ¯\x001e¨ügz¡ªâïÉw\x001d~Òÿ\x0001`wáqÃ±ði\x0013
\x0012¹¯
ÿ:þµ
 \x0004þËõý\x001exøÉ\x0000x,è§kã±-§dOÝ|%x3(x;mÖÈ×8,Z8ùÓëZ\x001dÇÝ]ì³\x0007\x0008·Ø_w~÷ðËá ÌQÚÊ¥G*\x001cEaXY·ëë\x0017Î/®^\x001f\x0000fÀ,\x001b\x0018r";pý°ÞZÖ¼Øë·\x0004öH\x0016u\x001e@¸o<\x000f	ïFKÊõÅèË¢¡°ºùc\x001b¸°\x0004\x0017~gàâ\x0012\üóÕ;vÁ»¿	£óÐ87a4\x0012hûòt1IÛ`æÚð&ÙKA\x0014ÒKÁÑé»Ûë)< %\x001a9¢Npj"HG\x001a¹
MN_¤àè\x0011\x0011"BµD¨Ø\x0008ãl1¡W:ò	I\x0008ÅÚâ\x001e\x0006B½D¨Ù\x0008=vXDJâ$KYÈMM#\x0018æB4Kæ÷(D»DhÙ\x0008af\x001dë\Â`ËS¦´sè\x0006s9\x0017¢[Bt¿G!ú%BÏFFÿ&£l!þ×k=E\x000ca0°\x0011zUd\x0008nIßSËZÛ\x0018Ï@\x0018\x0008#\x001b!Ò\x0011 $ÂRåEa*v+Eõí\x0008¬ôfîÝÙ\x000cÑ%U\x001dp±/û´vD"¥ÖÚ:\x0018\x0018k»Â7,	Æ\7tã]ô¥õ¤90ÂÄXémÉWÜAR\x0013£	¶Pæ\x0007G
\x0014k»n\x0019\x0010+­(ùj1Õz&¨b cé1
*D.ÆJéH¾ÖÚ\x0015ø°EAÂB.×V(20VZ²_5,ÃÁÁ}T\x0010ö«jbL\x0006æ¥aÕ¨ª'£ØOÆII»À¾ §oÒÙsk­ã±z2ýdôÄâ`£#\x0018j$k»á8\x0018kÒá	gqºWP¥ß*}\x0007Ô\x0014±\x0010\x0013.0F*hë¶h¤³ØVq\x001fiì\x0001ú\x000f4J:\H?Ã\x0005 ¯ü?\x000f×¦\x0014ÐÑ?\x0019GG\x0003%\x000e«h\x001cÅZ¸5±Vþ«ÓÇh¦	¤Y4|IzH3 l\x0001)\x0003ö¢øÐ"ã´¢~N §ïÙ8®Db¬Ö\x0018&'\x000eaFmr+Ì÷ÂOÃCòoRyv*ÿî>îîF\x0010ßì\x001e~»>TY7\x0010Îê]\x0000ÇbN\x0008k\x00172ÀE×hB:?yyrùÝ4~øæäêÿ>V\\x0001Jq.úÂ<&Lb>»»ù<u¡=|¹ß\x001dÌâÉiåÕ4ÞÎX¡\x0017Zâns"¯g\x0017go¦\x0006´«·'g}å^N@.HÐIÇ»û]\x0007A])éM¡ë!$VU³Î\x0000¸H9&\x0019?Úâ#÷«¥²]-Ý8]Rì&Öóæxa-õèÆðl/d½¬û,i
:HÔeAÂ*=7\x001f²YBn¶@¾w$Þf0ÛS\x001bnlsélm¿uf»\x000e+Y\x0018Å
QhE'VywÙÝ\x0012r³ÌµIÊº\x0008XDïhù)±4EoW9-Ùý\x0012²ï²¥L'4ZPCzrfIÊ\x0015d½ã\x0012rììÉ[\x0000)Kô\x0016\x000c
RF¿©\x001e·	²¬Õr¿^ªÄPÊ bÖÂÌêWÛ\x0005¹­.ó´¼\x00134¸àÈ&+\x001dö8¦Wg¨ði\x001býÌlÐj¿ûZù\x0013\x0000:¿^ÚÐHhI¿7.Ðè\x000fÅaWÀcðÃé«Ç:	Õ~ßµòÅËý}A4K
Q¹Âu\x001cuaÒ*C¶Ózè\x0003\x0010×ªûóÇ·\x0012ÀÝ/Gß^ß\x001e]<Ü<\x001cy´stºFU 4±k3\	å	\Éó£«Ë¸\x0011
Â&\x0011\x0006\x0001äµ9¿y=u¯=\x0003¯\x0003Haoo\x000e½D°\x001e×x(`¹Ëï'¹>_óüìÙéÔ¶6Ñy\x001dÆèj\x0011xøY\x0010\x0018Ar]e 6U6jqõË\x0011åå<¿ûx}{÷éçë/_\x000e\x00075B\x0011U]zHea·£U9Òêv\x0012úùÅËÓóWß]¾}ûèµß¯V{*ð*CI+g\x0002lÎ\x0016-Ln\x0000ºööÇ\x0015§\x0008\x000f¥´ÐiC©5QÖ7Ë&=)_~	Ô÷\x0000M\x001eÂÞ\x0004£
¹0¬7ÞO\x0007Ê°D\x0019:\x000f]\x0017iÝ7Ñ?­4ã\x0012gì¦'Òl¦Úß+$mÐu3Ð÷BM:É\x0017V\x001dØð\x0007ß¦ûó\x0007p;^_úñîáPj \x0005ÚDÂ\x0016=MÓh#ÂzÙð]¼y\x000eîÆëÓWß^\\x001d\x0002	G²\x00009\x0010\x0013dzCS\x0013¸¢Tt´VH\x0002jh\x000c/l\x0005)\x0011äÌj3Ë!ºË»÷»³~&y\x0018´\x0000 ÒG\x0002ª"ª$\x001bEc6i\x001e¡»<»¸zvòøÄ_\x0006«j°ª\x0007,\x000cá£TµÒXÐÐ³Bé\x000e4\x0003U6X]Õ=`u^³\x0001`Ó±cg ¸"\x001eÁ6:1z°\x001a«éÂÞ¾ÎµRÂ9`µ\x0001é
\x0002úè\x0001°à|îPS5|}ÿ{}wØ
M\x000cîñ4£f¨d¯Ë\x0010åZb\x001dZoÞÂÿ½¾xÔU\x0016û\x0005]±(è²âÊÉ	¨\x000fÔ $P[L[,¨jvXÔ\x001cïï6¨þ\x0014\x0006âvD\x0011Å«
OÜ<ÕPýõ.ÇËÇ¿RÃnVþZ3"ß\?\x001c}{ó¥xù¯ï\x001e\x000eÏ([\x000b;Ç±5ÂKFLôJæ¡Ñ(v~vzuôíÙÛâé¿¾¸zt\\x0019êAàR-ÒÄÉ§Zd/ïþòp°Êâ­ð­RÉ\x001bÈJÖ\x001bEóA4\x0011(I|yñ®\x001e¯\x0007ÙýÚ¹kç\x000fG/£Øø\x0007Cm0ò)le+ô:+ «£ÉÍ?ýæÃîÇÝç/é7Ñ?ìá3jÏ(\x001e>hf\x000b¸m4)SÝDÉ+AçD®MÍoÆg*|\x000fÛ`RLDä:)£ÀSÂÃ\x0017*|/½\x0011Z,\x001e\x0003\x0015~/}¼ªÅ©ÊÀ§d%?%\x00024Î\x0000\x0007£ÇNÒÏ«×Ø6\x0003t5@Ç!\x000eù'¶ä*SÙZJÅ\x0003èk¾\x0003 =\x0011IYüôéµ®ÅÍ\x0000C
y\x0007'¨cO¬¡¸r=3³\x0011_¬ñE.>Mi\x0004x.N¸$¸âZ1|+Àåx`æ\x0010\SÃ\x0010\x0018\x0002Hy)D\x001f\x0001¨}uÂð-OËÀê\x0003<á\x0014ë"'e,\x0008 [c\x0000Ú\x000c0Ö\x0000Gl¡îI\x0000\x0003-ì±p 9?öu¨\x0018¾e\x0002$î$9/\x0016
¯\x0016U0\x000b¬ÑI.:	¼ôB$/\x0014\x0002¥ÆÐ
\x000f ª\x0001rÝäs\x0013Å7sç6]@Ù\ZÁ\x0002hk	\x0010ö³ \x0019ÖÄq\x0007<LhCÖz¢7Ãó5<¦
±j\x001e¿Ho\x0019;ÿ\x000cRSë£
\x001b\x0001Ö\x001a&°mHÙ\x000c\x000bS?Ö
)©Þ1\x0015­cý~#WE{EF8½¢`L ?Ë­\x0011P\x001d\x0004¨öçÐUC\x0012}»ûû¿ÿ×}\x000eNß^üeËîeKåhkCñg¤/Æd¥\x0015èùÉååéePß¾|}¾yD=ÊN:¡ïw\x001f¯w\x000f\x0010@½¸{øõÃ\x001f\x000f6\x0004Y\x0011%Ñ\x001dëà0ÇoLÀÁ \x001eö×p¿?yyzr\x0005AÔ«?<ÿþôí*Ô\x0014¡ÖT¹)B¨r!,M8Ïï¶\x0014DÀídJdK]`T|òëëcQ\x000cº|©ý5ljMñ°\x0019¥} ¼IY'\x00184\x0010éÆÍd`ÓKl)7­d\x001blIé-Gòï`\Ø\x0001Í,¡\x0019¦Ø´Úv¦í\x0016å\x001aÃ»ièHí\x0012eÍ\x000b\x000cêTú\x000f\x0015kBºÐ´h\x0019ÐÜ\x0012cÍ8ÈÌçä¢±QImqA;÷µ+ÃÀæØ<\x000f>\x0017^pÉLÈ¦EÈÖI-,\x0005®Ô"õÛP¶<¥À.\x001fºkq	-2f\x0005R\x001d)á=©\x000fã1õ\x001eR@òµþÝ­$\³Ú\x0015L¹Yä\x0001r\x000b­\sRÑ0ní{e«m\x0002Ó(øH­jJ\x0000efö©#HÓCOAVFAr­Â<¾\x0015¥\x0005\x0003ãÿ\x0008Î1ÉUVA2ÍB0
\x0003°\x0012áÂäê]°¦áí1ÀUvA2
\x0003øï\x001aM4ÕuiAJr\x001aÔT\x000cl]LÃ\x0010¢G{¼¥HÙHç¨ö`§½Üýà*Ë ¦Áa·ä$9Øô4i\x0012j
V4Z»\x0019à*Ó ¶!\x001a^±\x0012JÐ$§\x0000-¹¡Coµ2\x000ei\x001d<ìÅÒè%)òØ&¾Kã\x001bT\x001d\x000cpyLû\x0010½+K1®É.\x001cìAÉÉF	i;8UÙ\x0007Å´\x000fa¦4¡¹X`EÉ
9qª²\x000fg\x001f<¬\x0000\x000e\x00184XË+\\x0008d¼¬i\x0014
\x0019àê i\x001f¢TÔ±\x0014\x0007}I ø R\x00149\x0004®²\x000fg\x001f¼Tª¨9\x0017¨×7ê"9Û\x0018>f«ìbÚÂL¥D\x0015È>x¨¤fÉ©F¯\x0002\x0003\¥\x0015S\x0007Ç A³\x001f)ìK*ÞÈ!'ØT¯Õ0_«/]r@ûHiPc¨Ög¢> \x000f\x0005ù¦z°éÐÅ(KH¼tRu\x001e[ÌSDÝ\x0018áåà³¡²að-Ï51P^Î\x0000£ÀÖÒô£0"4Ú\x000c9\x0000]%oy'\x001câqD¯3\x0002Sî¤\x0015mÃ1¡±L¯öØ\x001d×e·Îà´tÂ\x0012zówAQ\x001cÖ¨\x0004ñ\x0000\x001a ×\x0015Há>R_Gg±ûÁrÂ¦Å~Ä\x0001è]å
À·¼7¢K©ÊxCÃ.ì\\x001c²·àùJýÁ·<xBa2L	X"ÑAväçéF9¥bär<<*ø	Ë5z\x000bå\x0013
më\x000bÓ\x0002¥ì6¶qOû\x0018-\x0017âäæÐ{ò^ÁHM¸ÝÑm:oülI×¾û&\x0001È«\x000c\x0000ÂÁ©
O\x000b5æÅe@^F%ñ\x0010¿>æôGøëèTN1Ñ)Oþ¼a\x001aÜwï)G&}ck\x0019\x0007®Ði&ºÁ`%\x0003\x0012î8î1÷ªÇF)ÎTè\x000c\x0013\x001d,%Å
\x001a3e	\x001dÑhÈØhXä ³\x0015:Ëö|²\x0011}?\x001b£¤2Zhô|3ÐÅ
]d¢Sb§É-q\x0014kJÓL­i¸/\x001cp±\x0002\x0017¹àJ*Oç\x0019ð	Fr\x001fBÃùÛN.\?\x0008\x0003Á÷ãÝ»H\x0006ÁÄJºvT
ªî\x0008:[=
øyï\x0002Ú\x000b	.Ln9½\x0003e\x0003Scq\x000b\x0003Þ¢}\x0013àA\x0000ÃSÇF\x00063EnÕT¹Cr¿Æ1\x0003^­R$[§@K*\x001bËDcÎiäW8ðl
«T\ Þ\x0015\x0007-\x0004OÒwc\x0013-\x0007«á9.<]q µX\x0011MsiÔ\x0019ðBýp\x0003óáBW&?1b\x000bZ{±\x0005·\x0012åÀÓ5<¦µ!vO\x0003Ü(\¹\x0014Jo#¾\x000cõÓ\x0008Ì§aÒsEF(\x0018\³´V\x0012ÊS\x001bä\x0008¼úi\x0004æÓH\x000f­¶L±[!©\x0014nH\x0008<FàÕO#0\x0006Ì©a¶\x0005àÑÖ¾Ò6àI¯VË©Íb½¯	esi\x0019Ps,\x001a\x0003]¬\xøy¶~îøqµ$êx\x0008]­V"S­L\x000fc¤\x0008#Î4Äc²S5:fa \x001a\x0015lõ(\x000b\x0005Vi±Án§D¥Uà[\x001e<çJ?kÂÑ¢Á*\x001dêwlä©\x0018ðd¥Uà[\x001e¼ô\x0018\x001c-ÛL$ÖFUé§nLÆ1ÐéÊOoyè\x001a\x0014\x0019P¢+ÄóZ\x0015æÍFÓ\x000c\x0003©-|Ëç\x0003)\x0015+\x001c)i4ÃÓ5ð\x001cx²Ç}·Ñî7,j$]hUt2ªÆÆ}µNQl\x000bôÈ+ÍL¿¨ÇNV×ð¸®
8zÄ\x000e©\x000bÕ¯Ñ¥ÂW+\x0015ÃV*\x001eÆ¦\x0002I\x0017¥¡ÔPF\x0015\x000e¼Z©\x0018®RÃÄpÞ·@w¯\x001aåÀs5<®«´Êb\x0005ª<]8b#áÈA\x0017jtN\x0015
\x0012MM I#Ç²omÈÜ*[ë<ËM7úâ.y|´á
IÏÖ:Ïrs\x0017éµjäÏ\x0004rnDG\x001414(³8èêa¹á­7\x0014 ÁÎDtáµ¡yN×X=É@çê£uÜ£ueA
\x0010ÑQìMÝÇQ\x000f¥j«OÖqOÖL2\x0010¸¡ì#þ(=\x0014_Â¬Ð±\x0013\x0017æª´÷¥\x0016lv'ãÊsµÊsìÄE ÑHà;S$=¢\x0017U~ÈÍ«+\x0018]Â\x0008²>À¸å\x0018x¢lì,çÀ«oçÞ¼@mù\x0012ÖuJG<|¨òBlðVqàÕW3KF,\x0010¼9¥'ih
A\x001cxµ=óL{\x0006õ)W/\x0005@\x0016c[iu(¬B}õ\x0002»z¦Etj¸Bà0\x000f¡ÑÁÂW_=nF\x000fxaQ«À¬aAG3õa(c¦BíÄ\x0007nqÏjD:\x001f¥¤¤ áÒ¡ªÎ7*n¾\x00116×bB/EÐ-©xWC&£Î)nÆ\x000cøHÅ
¸)\x0014\x0016\x001f#¨6é9ð|
[ÈÐ\x001al\x000eèÄ'xõñ>¡\x00002Ôj%pÕ
NR\x0000*£(:ïÆ\P§-\x00023m¡@\x0002j \x001bRH\x0004	]\x0001®Î5*n®QKK±£t\x0011W÷ÚHKp}c¼\x0003®ÖwÜT£\x001fi#¶ê'pøb½\x001a*ª:Õ¨¸©F
ón\x0012Ñ\x0019\x001cOè(ºð²ÁÇÂWë»ÈÕw¢Slú.Á\x0004O\x000c\x0015½U¬\x0016[z\x0014Èiàiå\x0004\x000f[A\x0012¼ÁÃ­Ý(nÇ\x0016´Î^j¦ÖFK4À.e|bm,"×X\x0008\x0001óH\x0013<åpæ6ÁÃ.)PxC¶,ÖÆ"2ÉÔ¢R\x0001©ìm\x0004²ù\x000c/4Fl8ðjc\x0011Æ"½tªz§§qLè0ÙÐ5:á8èjsÁn\x0007\x001eÇÎ¤=DçÑ\¸±Â\x0016½oÍ*ö
I ¾ f\x0015C7oÌi!kxL\x0001Gi½R¸¸y\x0018]¸\x0006%\x0011\x0007ªÁ1
Æt²3µ¬CÙPÐ
e¹u]ÒÜÚò±ÀKÿèQ©(Wà
5hakxì\x001e®H\x0013-"ó\x000cæG±\x001b¼x®FÇÔÈÀwïB@\x001f#t\x0008N7Ú§9è|«\x0013:èl(M\yÉ\x0019QyZ\x001a\x001eW!\x0003Y¤Gx
\x001a\x0007\x0010\x001eYÛÖà\x0008\x0007^¬á±\x001bôF\x0016¥[ ÁÃ\x001dk	Þ§¢e­%W#§·ù(0ó³-\x0006C\x000e%|´¬µd7èijHR¡°âZßZ9ÉWk\x0015nÅ[ùdÄ²ðÊÈR\x0012\x001e¡s­\x0005[\x001ctµV\­â\x0003µ\x000bÀlf,*\x0019ß­\x001dsCµ¬Õd«\x0008=\x0002\x0013<A_ÒÃ â
CÝZÖjErÕJ
h\x0003J\x000f&½ñp©¯v¬qUËZ©H®Rñ\x0006àFºyhmíXVµVQ\­b\x001dÏÄh÷ÊFZ6\x000eS®CÒSµ§¸\x0014=Úð\x001c6\x000cÌ\x0001ë*ÞZÕêÈ\x000c`Å[\x0008Yç(\x0007oCÙ\x0003¯Öy\x001bÛJEÍy\x00022¡\x0004/\x000f/\x0002 XTÁã¦\x001aeÄ}Þ"çDs¾Ì\x0015{6xój¥¢¸F\x0019©á\Lx\x0008\x001e¹R­m¦\x000cxº~·ÏSÈô"a&P|ø¡ÒÖõ«ÕÜW«"mýÉ)Mèf?oÌUÑõ³ÕÜg«\x0015Í/§¿_\x00061¢¤£u~è]h]Ãã&ôt \x0011M©$.©Hð\x0013\x001f\x0006¥W;z=äi\x0001¨Tø*3Ê»±á$­k§ÙÓIbÇ)L»\x0016ä!c«k7OsÓy&RíGzA4\x0017ÓÐ\x0013fá\x001bÓÁ\x001cxµBÖ\ì<%U`\x0013\x0005mGÑj?¦AüÂWkdÍÕÈ.\x0010É®\x0004âÒåC5\x000c34ò¨ë®UÍíZ)\x0011ð£g¨SòÜ¶±C®î¼ÔìÎKiJ@Çc|\x0018±ÄfC÷®n»ÔÜ¶Ë\x0004BG%hEH±®7RÒu×¥æv]BEÔQÛÏ\x0015QêñIîÔØÁÖ*Ûu©Sð{¬\x00140^\x0019z\x00154ý£\x0006áÕ*Ûu	ðCx¡viZ\x001e¬:Íµ©5ak¼@G\x0015TÙM§©D\x0010ô9«B5·)TC¦\x0016e';2y£Ôh¡ÆÌ©\x0015á*<¯@\x0007ænÝ~Ohh­¬aÀ«[V5»e\x0015h\x0006ñaDEÌyÂRá1¡N\x0006]·¬j~ËêÚT@éÑ×òníX¶ÑÖöÂr}äà¯qÁ±9\x000fH¼\x0011ÞXøcka¹&Ã^ÐvtÝÂ\x0008×âUåÀ«m\x0006wZÙ\x0008AýÈÐÁUÖöö²¡!ymkl¹ð¦ä¹á
c¾2Ô\x0016
m\x0004]­ô,·\x0013>¬I=gt­Um\x000cpu³´æ6K»&^!ïVZ·ôØ±Ö­ÒÛ*$COV%»\x000cçéõ\x0012<5T×®Ö(©Qµ\x001eÃZe\x0003½	\x0005¤\x0007Øø6\x0016u»Z£8¦F±&æmq\x0000O\x0011!²3¼±«5cj\x0014;Ïþ(#Àãà¥¨¼Ç\x001c©º\x0011^s\x001bá\x001d¦{ Þ2§­ ¨Ûù)u\x0017¼ævÁ\x0003Ý?\x0007dLÊØà³Û\x0006FEuM\x001d¡¹Ô\x0011Ó\x000cañ¢p0ârÒ)C	\x000bWëbÇÔÅ°
gÓ¿µxhû¡^Z3\x0016¹Ú\x0003uL\x000fÔIA«½`s l©\x0007ÞÇ¡GQ\x000f8hîµB3\x0019\x0003ÁKñ*qíÐáÖ\x0003\x000e;à\x0000\x001cë¸Ð!Ý7¬ê¥\:ó\x0019:ÜBJs9¤,øï®H\x000f=PbßJèÆÊ\x0003õøæ_Lb'Î\x0004­c.ÒäOk¡
\x0007^­T<ø\x0000\x0014\x001d\x000eÄbÍ$m²\x0016C*ºn×Ü&xëJ\x0017
,ôÊ-H.y-Ä\x000f&Ø|tÝÉ­¹Ü\x0006Ø|[MQÜ*¢£\x0019\x000eÑu·´f\x00133¤Ø\x0007\x0005KÑü¹.ðæ/tÝ.­ÙÌ\x000cÐy[²´3Ñ¿rzÈÚÖÝÒÛ-
G9n\x0005ùl7B
¦iëniÍíÁi,`x3¯\x0019Ó¸Y7¨¡)`]·#kn;²\x0001²i´·A\x0014:\x0015/Ê@áPc£©B
·)\x0014V<á&M%¦äÏ¤U¸>¡ÀÖÔm¡Û\x0016ê`M
%¤ü1.ø5s¾gäâº?Êpû£`©\x001dÒ®NÍH¸å³ôûÂþá\x0001x¶Öy«ó¬±ÔdÇ¤\x0019ÔP\x0003«;j\x001d·£Ö&\x0013Ku=\x001dFEW&D\x001aû\x001f\x0019ðêö-Çmßø¼`Òy\x0001Éh
Ý\x001aëGöõLgÏtiG]¡&JÐÎ¹[ÀÎ; =+êNøé{vé\x0012Ép÷jÒ*¦s`OÚ8\x000bÃEºðí7o¾\x001cÜ¾¿9\x0000Ì8\x001fòôy²´\x0011ç\x001bÌ´~êÅ4¡±²ðÍÛ£óggmT>¾ûíCü÷þü.ïÔM:é÷þps{»û\x0019Ö®ÉÜm´ØËÝííßÿëî\x0013 &tëAóJk\x0013¨iÖÃ|ãDËÜ\x001føòäüüôâ\x0015 úáìüüä»­Ú\x0015\x000cHkÀÿu\x001céáÏ6\x001cQfK\x00048&>ë#\x0012\x000e¡{q@\x001aüùß\x0007¤:Õfyüãp@óþ\x001dÈ\x0003ZUôfy8äVÖ	\x0017cÀÎ\x0007\ï 2\x0003
 åÝ®\x0002\x0001:+øó¿-\x0010ð\x0017Ìïàájûn7\x001dÍî	Êüpwó.o9Ýç7×\x000fGßÞ|9ºÝ\x001d=ÛÝßß\ß?\x0006\x0008Z²w0:ñ{`1Ë®\x0019,TqKDg§WGß½=:?9zvryyvz¹\x0005\x001b¤há\x000f\x0017Ë¬ÁMe×Â\x0003\x0001'l~\x001c\x001aÍM\x000f4GÐ\x000cn^\x0004h}Ó.'\x0007û°Ý»\x001fúm\x0012[ú|ðç|wôúvwóé\x0011@6&YÉ8Ý,|iüÅ+ãðÕ+);
¢£×ç'g¯Vú8¼¼+Û3ñ\x0007ÓöÌ?^¼ùtôüæãõ\x0003R
ÑåLQº[°Ù0_wi°° SK1=ÿþôåÙ«£çg/Oß>*"!}W¶â\x000f¾Á­Ì¯ïÓ¿}óËîöÑè#Þ{B·\0J\x000fQc\x0006POýK32XàúúòìÕó³×'ç\x001bp©%.ÅÁÚÁkYa¼,ùz­'~ÜnPf	Ê°@!­\x0004à2¹KÉC;\x0015Þv­ªcäârK\K\x0017mê"&«@^Øæ U/½¸Â\x0012W`âÒh£]àBy©0µÄuâ¢ºô\x0005,dRØ\x0004,8]\x0006\x0001uÎ\x0007n½¬n½d]{ía\x000fë\x0004Ì#\x0005\x001c\x0000\x0013ä³À*¹~`º\x0002¦YW_\x001e£À[\x0015I`V".7Åg½¸ª\x0017)YORkÒ¬.!Á `J\x001eg`F¸\x0001`Õ¬7i}\x001emHÀd<FçS:\x0012\x000c\x0003¸T­WY7Lùã\x000cËZs /lÆÓ)<\x001e¸`ªº`uÁ,.\x0000LÀ A¡Q`Å%z@W¨ê)Ö
æ8 0=1 N\x0012sHu¤¥\x0019±yú¨\x0000³Lk4uô\x000f­ó0(X#ìÕrZkÔ
¬ºúuõ¥Ê<	ÌÎ\x0012Cja-µ\x001f0Gª2Ge\x0004rD&`2@«Ç\x0004Ìj:J dì\x0006¦«G©9rÚ\x0003G\x0012\x0013\x001f?\x0001SäðH5bDHÁYeÂw6\äM9o\x0011ú|êYaDñ
ê\x001f\x001f.\x001fn>¾Þ=<þ\x0011¹\x0008\x0014£[¢{E
#ì+o¯.¯ÎÞ¼9=¹:Ì,\x0019\x00162osë\x001f Såaê@÷?Ú}±Ù%2Ë@f\x0007@÷,ýÉs²\x001eZbPÉBÍi\x0004["s,\x0005[¯rB  kmÂ\x0011\x0018:M¿Dæy§)6³6Ñá4±¦¤å´}¯\x001fYX"\x000b<d*S¸g	|\x0001®YûJ\x0005,.E\x00160 øÆÃt¼EEpÈÜ¾\x0001à rLJ\x001e4á4C&{\x0002h\x0005î\x0013{q¸\x0013\x0014ÿx}ôíõÁDJÅUÅ4Ù¬3ä|Ëß÷Ë¾ÿ\x001dÈ¡\x0014`j	Lq%hy\x0002\x0001\x001cÙ0\x0007½EgHÿÕýç 3Kd\x000cjZèûK{q§`LSî¿éFæÈ\x001c\x000fYÈ+Ò õlóðëd4IfÂÈLV§)YÇ\x0019¼\x0016Cr5ÈÓ\x0010ªx\x001aûÜ6d~ßûÉ}üeÞd\x0002÷ùèÅíõÃýç\x0003®6t¨ãS¾ÀFÚê\x0002ÜÙË×'é]&to^^]¾yLrû27%Ê^ßî>L¢»ýïÿøÏÓoo>?*<§rk\x0012\x0008ÉÎ\x0003³\x0018I¯~\x000b¯ÏOOò;?:ýîüìÍ£'»0sSÂ/\x0005>'R ¼\x0014Ñ\x0016©K\x001e\x001døô\x0012fãK¶\x0014á%u\x0017ð|¥.ð¤\x001cçð\x001c\x001b^ð¹\x000fËÆÂ±'%M_Zxmºð½O1æÿó\x000fA¨<U\x0002vï1É~ôýîãã¶K&éMí#Éåð\x0006}$àAGx8a:§¶)Å~ôýÉK0_k)ng*x
ÏÀ\x0012Ò\\x000bÈí#Î
r\x001dèÂ»»Ïj÷áÏè+ôâúþãõÑ³\x0014·|þr\x0003çis÷Az{	ÑõÏw\x000f?^§ßäÀãÐØ¬dmâï\x0006>¢	Rz·JÄ§ß]\}{úÍÓË§GÏÒ÷oÞ­\x001dç\x0012\x0011¸Ëð\x0001ÉF\x0008\x0012$
\x0011AH!­Ó[
#rãEþÊÀ¤sr\x000fe¦ML>cb"Ð)îÜ\x000e
fºrÇ\x000e\x001eÇF¡÷
QàéAõ£ùt½Ûa \x0005áSôÝîçOw\x000f·×_\x001eÃ\x0004Iª)\x0017\x001eFÂõ¨¥ÎKm%ØÑÖñ}wòÝ««óÓ·[@¥Gâx Öè	\x0014¤ô\\x0006åèø¤¶v\x0014T2»\x0003*ýJ¢ÿ0Ê'P\x0013¦i`pÂ¤lóåq0QÏ
\x0003\x0014Ìäåf|\x0003£\x000c1KÊë\x001cdNù\x00169*ÝIøÃ\x0011TÈ\x001a``þcjæM²\x0001µÊ\x000bôP¥Ã¼\x0003ÄåG\x0019U\x0004¯bU´$«Ìf=*i\x0015øÃAe\x0005n<0J<fP\x001c&\x0001A®\x001e}@î¥\x0004\x000b\x000c\x000eÚKè\x0005|\x0006W«Â\x000bô£/\x0010lwÛeÀ4TB\x0005Ë\x0011,za¢\x001eCþ\x0003uÛÿqÚêóuüé/\x000eÃ£)(Ê¨n¯'wâúöv÷ù1qÁÞÔ	`râñFLº\\x0005'[Ò:?=z~òæíéùùÉZôQA«ü­Ð`Ð$O:'È84@Kè¢k©-.´Jsm&$våjÜS¡¹sý\x0012ÚÖ[­Ò_O4¹5y\x0011\x0011³Ø¢ÃW)lóUn&>úë_>¾;83²\x0004 ù­_\x001eók¤¹ÜéY¦¸Bå\x000cT.db,àA³-\x0015¾{yúvÝ¯!A)\
\x0016&.Ø\x0004	\x0006UF$s[CSÉ¤w#ªlõï\x0001\x0011Ô&f!´\x0002@[eÐyNç\x0001\à`3¾\x0007Óû\x001fã§?Þap
!õyºÞÜ}ÉÁÖêåöJåP?ù2Ò\x0000½ä¤¯<Å6*DWÁ{ýýÉÛõ4æ\x0012
ºáÏV,\x0012É®Î´\x0007\x0019É¢\x0001S\x0014¸XìþòÛßî0g\x0003Òöâ>E¢ÉÐ<ª\x001c\x0013ñÑåû°@?=e­JcÚË\x0014&K³k÷ËûÔûws£aÑIow\x001fßß=Üï~½ì\x001e%\x0017\x0006\x0013pÊ\x0018\x0017ó¾0paÈ	5ªéî%½=yùìâêòä\x000f«¸ðîö§Ý_w¿LGD$¯_î\x001f><fC:´¼\x000bV\x0003«Ö´$,êä	¡\x0012Wn/*}\x0014äåÕóU\x0014\x000f»Ïýr¿\x0008Ù·E¡ôÀ\x000cÐÍO\x000cU\x0011âeEÑz¨\x0005SB½µÌÁ\x000cìî¶¤ÂÑ:\x0006ä¢¤¡\x0008Ýû>\x0018Ëà|\x0013\x0010 ;µ(\x0010¤\x0013u\x0002	D[\x001e\x0012ùÛ?÷K\x001fi2¤7-)ÿ\x0002×E.'KWV¸=\x001b?ÙÏ³Én@G³
	ì*\x000e\x001e]¡©1#\x0007KB/´\x0017ð° \x000f´
N\x000e\x000ff(\zAùÂ&X\x000e-¹\x000bÖ\x000c`Agã	¥x6sø&_GÀÂìëdÞ>pv\x0004û~4_þü£\dJ6æHTëMQ:¦\x000c.AÇv\x001dû
0rnd\x001bÌÓ6áHçÓG\x001aº\\x0011²\x001fHÎl\x000bïÝ´ûn
YÈ»yÒõ\x0001£Ò{Æ\x0003\x001c«mÁsò\x0011\x0010'«y/ó8=¸\x000cA÷#Á§³M&)v÷$\x0013ÁV
h\x000cÞV¸;ýHðál	ð3d×\x0005\x0018iÈ\x001aÃ\x0010+è¿¯àØx:¦ Ñ£$\x0001Á9Ì\x0011jß
r\x001aÛ\x0008\x001cÌO8VËJ-Ãõ\x001f
e16áPÉÃE&EfÐÉ±C7IÄ=ãÇÂyÿ-Mò×ì/a\x0011>n
@`[P67FLÜÏ\x0010xÜö	û*d-\x0012z\x001cA!ã\x0016\x001cÉ¬áø¼\x0011Úb^IÚ\x0014RwÃ@u¶I\x001c^nz®&\x000f¢§xÌP<æ]½8(:Ü#HG\x0005\x001dHz#\x000eo":Ï6\x0008¦<Âo¿þ¤~]\x0018Èâqç(\x0016ý+\x0016&\x0013L¡¢ÐBÔ1á"¢Xw\x0003Þ'Ý¾èÔ\x0008ï²O¯çmsô|÷éËÝÃaï1âC\x0016T5>hzÊ{\x0019$7GÏO^½½¸ZOÁ\x0010¬<O°à	lÆ\x0005£8\x001eq9JÆ)¿\x0004Làr\x0015.ÇÀåJÕRÂb?©Hï\x0008×»\x0001}÷ Ü§?}XFUp/\x0011ýæüáÇ¿ÿ¿ÏSQ×Â\\¾R\x0016BCêþ	T\x0006\x0008:3¶]}{®ÐÁ¸Þ¾ûí§¿üû½[\îË»/SþÍîæSîÿþ_·7ïß¦+ÿéúçÝut!j\¬a§¨-\x000f{IX>Ñ¼º"£»|;Uëß½JþéùÙ¿Á·Ih¯N¿;IÚúîãÇO×ôÿ\x0008ø}ú/Ë¸Ô
In/v·?O\x000eùØ\x0005ÏüV\x0007·¥L- ù%*[!Ø^·o´ïîþøAú?-33\x0010@~úrói\x001d\x0003d\x0017C>¹dÁp2\x0002ëQ6ÈN!@èøêíÙ«\x0015-`ß}yÿÛ¾T3ë»£ç÷w\x000f{\x0004\x0000d:²\x0010´û*! %CÎ\x0010N_^\ýÛ*O?ÿéo¨r¢ìùÃýýõ=´\x0017=r\x00106"\x0015\x0015\x0010®áAxò4½Êa2çW§ÐT´â/Öüü7U]Ýç£}HÁ|\x0002òÈ\x0000-\x0008)I\x001aAJBbÂxsô¯W)OPÖ4³}÷ËûÏ\x001f©Cü« RtªÅ{â0º\
\x001bGÿoÃ¯Ïñáá_\x000fk£mþõÉ\x0012Ü}^\x0005Ý\x0008\x000bs}\x000b\x000fÿzGaGº*\x0007Éé×GG¿ÞÄØñëÉyÚ }Ét/}Þ÷\x0008Ò·Ð	Ùubÿ~bo8ôû!ê\x000b¨\x0012 3&7¿\x001aG,-çþ~Ì%\x001dþý2|\x0016Ú'rû	ÞbÐ=\x0012H½H'?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ý\x000e;ë¼Õ\x000e\x001bU±\x0015úå\x0019"H\x0003$&PógÂè\x000búîã4RÐÅÉs|Ì¦Æ«»Çë«Û\x000er\x0006BZÙ\x0007Ê\}Y\x0013ª
!ñv=µÖÏWÇç\x0007«ë¶ã\x001f\x001f¾ÿùeü§^Â>îKëîõôîþódÊy«Û¶7k)óÀ'U·7Ë®
zP\x001e\x001cýíÍÁÑËÑÑ\x0016óõÉñéëÑÉÚLÖ2'..®ßÞÌ%àÏ\x0006úõãäí.ãlh¿Ð®®\x000ba%L£:\x001eç{ØÜ`+'ØÁ÷\x0001µÜ\x0004(l\x0014iVe«Án%RÛ5´	ô}ÿÚo¹¼ÁÉûÇéöy\x0010 m\x0006N]H°¤\Î¾Ì1Ä\x0014p£\x0001w¢ø@\x0007£kítôÛùê¢ðøÇý×\x001fß¿^Í@siÁ/¸\x0010r[ìØK§½ñ¤t[\Àî»5ØãnÍ1\x0016ü\x0002K"·qBÆ¤1½8u&+¸p3ÎrÛ¼&\x0016v8N\x0010\x0010¿úgâ¯jD/\x000cB
bÿÆ¸+çÏ\x0017áöÝ|\i³Ød·íAº\x0014²bSsýdI\ªøGITôýÔÓ55[¬²£5·ßóÀ«&@gàd)]\x0018.±,Û6åp5\x001c}Ñ¦¡mÎ_?-¨ÿÍ#O\x001f·ãær\x0008àEyrÅ²¥Î¡9EM:×Þ\x0017ëûPo\x0004=Y­b4\x000f	\x0002úøh¯â\x001cÄ\x0017ÉH¤Rè}1ÔÃn÷\x001fÕõ§0_¿9GØ5\üHoyë÷Ô2¯QI\x001bÙúÛ¸÷Ïn(_øöæí\Êø\x0002êôîm\x0018áþ\x001ceZúÈÇiÖÜIèù×\x0004ñ\x0016\x0018OWg\x0017Î3J\x001f½vHèt*i\x0005ÒYª,Z	$Ò;Q¾3\x000féÇÊõ±¥.q%¯dnªT6(LÒÌÎ07Å`	KÍ1V¢bL©\x001c¶ëìÕ\x0019,\x0008´øÐ\x000fÖÅÌñ[\$·\x0002«9~[Lktnw¦ýS=|Þ¬\x0000\x001ck¼ï\x0010ltªl ÆÖ\x0017Ï\x0016Û|ÁeCf\'ém°õ÷¸Iàjä½êÜlc3:Ú¾Ì%
³7Ö
´Qãè3®®¿]Þ|ºÃp¹hJÎÏ_&_&?:M\x000b(r¥\x000beP0§c?ÆF\x0014õÆçoÇ'£
K\x000ec¾àþ®\x001asÈå\x001c¿z"s§+\x0008z\x0014\x000b&1rM'\x0016RC\x0013Ò]?âr%\x001eä²ö\x0018XÉ=î\x0013C\x0003g?`o$H\x001a\x001cË¹egb;ü\x0004dpä2#rïYá\x0015_¡éâzóQ9Dc\x001d­\x000c¬É¯é=Ìv.\x0018\x0016a¿CfO\x0012\x0010\x000cCÝ¡\x001e\x001fý\x0015FV£.~"	ã\x0017fªÎ,Ã£142øÎøèl\x0002	\x0017äbóÊ0s¯eÏqaV\x0017ïÆ\x0016íInV=À=Åãôîs@)¸æw9\x001f@T\x001fÊbÀ9\x001b¡?·\x0014ç'Ç¯×\x001d#s¼|\x0005Ô7d\x0012q ¹¬ÈÿÍFWÜ\x000enåVÜ\x000f·ïÞ¾5¸Y° ûyÙ\x0016í/\x000e\x0005mÊÅHèå}"1ØèÀµX\x0008æo06;\x0004ý'7ßß½}¿_42:ÇÐ¡E\x0000ç3h¸²p\x0014õ\x000f|5h­ÑÝfÆÖ\x0018ú\x000cYbè}S45:â-% fë]\x000e#\x001aC0ºþ\x001aþüºa\x0001þ~÷Ð%\x0000Ä\x0012=Ç²ä;YìØ©\x0013ú÷ã³µ©\x00043Z¨!4±7­¶Ðwh#ÇøËñ\x0011d·pÒµz\x0017ÚKo¾}Ïßÿ>^^ÝvØ\x0015ô0\x001c)r9äþ5nH\x000fßÿ¾òËÁ\x001a\x0019ýyÔ§\x0003ÛÀZ|N\x0012Ôh±úT£e\x0003À~J.n.Öo
¿»ýóñj2í°
{«I9®lÃå¤ölÏ³Re\x0008X¾|8;ÇxUýýøè\x001fçCRK?·íUV»M¯â©7ÔÙkN't¶f6s3Àÿ&\x0010½	;} èæ?
½»¢ÿ¾o\x0002gp;½­\x0017ÎÖ@Ë\x001az ¾Wôÿ=o\x0002>^Úé8º}\x0013z\x0011çý÷78\x0006üµÃD(Ju\x00124¿JWNÿÌW¨|ArðÐÄnéXx
Í']\x0012¼IÜÌ'é¤\x001cß²;\x00158Úk_Ôíhx
Gë>Û\x001fãk´"!Ó×,ZÝîû<ÖÙ\x0007º¨\x0006á9ö\x001cÝ÷Á]5fI\x0014È×û\x001bcÓ®ûf Ø\x0014T÷\x0003E9A\x0004ë¾À Æ2¨\x0013;þøóv\x001a±þ\x000c¯#æF\x0014àþ:¹Ý\x001eK÷ þ,bd-¸bÈ8\x0003Öt0\x0014©fépÿü\x0004î°·\x0011öxOb£\x0014©\x0008\x0000±®ëT\x000cL
L¼4\x0019l\x0018¾ØåÚ²i+Ç\x0011¤\x000f
\x0001ìòÕ?§¸Ì
¬Y½§e_Ø¾¹Å\x0004×ªî\x0002T&5\x001c¡e,%æè©±ÀÑáÑñ«Mó21¶¡Þ{\x000fTÐTçüØ\x001c¨¨ ÀÌ½;g|ºý\x001e´Äã<û0ÞmÏ]ñ.iÊ]ÙºDMÓ ê%·T§n[×Ùï£ãu¹+s¨ÜG°\x000f*\x0011©Ð%\x0001IMàMÖb?»áHs¡Ì=IæDr\x001e â\x0011n³YÉ6\x001b\\x0018\x0010\x0015:*>×ÉõbÅ6DÌê3çª8ë¨	ka\x0005ol8Vu\x0011¦ß¸zèÈUYëy+9a1v;¾6²ªÛ\x000býmºJ¿®0o&Ó÷· \x0014Ô!SÐ&Gêu	ªô©é\x001f(¬zÇw\x0006vóÝe±`ÞN~;\x0002Å µqÆ
üdu5\x0012;#\x0015¤eP-O\Èx´Lí©w'öWú~z^Hÿc©b²Âéøfr}÷øy\x000bmÎ4Ú\x001b%PöK
ûLéÈÚ|rèï\x0017ºW£Ããó×O©¨\x0019j\x0013êlÃ^wýp\x0003	\x0011B4ÅÎGÜHBÀ«ÆùlO\cø\x0012%BüKgÂå¦*\x001etò°¸³tþ~Ã8!êè ç1
/×&\x000b\x001aÂÃòBï\x0010|ôá-.\x000cé\x001d\x0012¯L\x0007î,¼a\x0010Þë«8}7ÖRq1¨ÿþúê¾CÉñI¬/\x000bN\x000eç=ÀiÙuµs\x0015õpoôÛáÁéÚ\x0014ÑJ*Vm?R(3Ðl|9Nf*o6b\x0001I9k¿\x001f©\x0013\x0001î$ÉLÌJ.£
hZ·Ýv\x0005}PSõåû|vË
ÐfÇ\x000cÂö|é\x0010<'7Ø¬$\x000fÓlÚ:¯á	y'ÿaî=8;È{hN,Ñ\x001eZåQ¤<å(îZ\x001f(ï÷\x001aß®§?Þý\x0017P ×\x0018Mo'÷\x000f{åoÞß§\x001dü6£ä\x0013$K³o\øH\\x001f\x001f!öÑÉÑèôl¯üÍoGû'¿l%Ö¾ÄÖ@Æ.\x0012k
mL8s\x0016õv}yJ\x000bðíÝs¤MÉýÍx¦t(¨\x00116\x001c\x000eôâÅ£\x0006	MÚ\x0001vý¼Ø\x001c"1.\x000ej\x0003£ç\x0006æ £á9WÇFnvíkûòÝ	%vßg\x0014%²\x0012ûk0r
eÝ`£\x0008'»ïÃh3µ¨\x0007FÍ5Âs\x0017$&\x000fE¸du'Ô±ÞïBZHâ\x001a©,10¬tÛñáñÓÝ·¯sîÎ PÃVÜ3Y2³0dUX¿!Aa^[hË!PQ%VÛ\x0015..8£©8<Æ4ëj\x0013¶\x001e_m´\x0012UìG\x000b\x0012\\x000ck*,÷Z\x0001X¿mßl-;õ½a]½§SZ×\x0000­\x0016ËÀÛmKª\x0016ö\x0010ÜGzÑ\x0016óËÙÙFO[TJ³i ½T\x0013}u÷\x0007¸û`á³JsõÂLRñèÐ/~s\x0014\x001bÊkc{Å@eÉ¼ÝªÖy(ÿd3¯Eý?zöâõ&
\x0015å\x0019gNÞv6\x0004CÀvåCòfäÍ½y5çY©äëÝlÙ\x000e7&=$/v/ g?^ðËIâ\x0002
;9ÿÎ:ËÑ1\x000f;¾\x001aÔQèÙ\x0017z8pQL®9åpàñMÊ\x000ekÀ|§gOÜ éªx<§¯ç­×$ÜÌ\x0006ä\x0005M(zöäÖ¯U±¸4O\x0007Ï¶IÔ³z0^\x000f¡\x001azöâóp­ÁÌs¼«\x00161\x001e«2$Ôl¼nG[czöC\x000e,\x0015ÊÙá9S\x0000ÚÎ#±F\x0001Ûõæ\x0017½þ9=ûÍ\x0011¸´Õ$­3çLMe\x0003½¶\x0007=Áu\x001f={nËÅ\x001fcO"\x0004É\x0005°!'¡½\x001d9ãDÉ½'\x001e04Ï²ÓQ×º\x0004³Þ=ou¨ÎGÏ~°ÅT3Lk\x0003Ì\x000fL¶È5c\x0010ïU\x0006£C½hMñÔø\x001a× 
Z<¢°áÊº\x001d\x0016\x0010èÙ\x000f¶ø\x001asðLâz@WÖ¬·¸!u´\x0007mFÚ¾\x0006\x0005¨#±^cÐ\x0015f\ùs]\x0007¸V£ÃÏ~´e\x0003Óâ\x001aÅÙØ²yYfB^ï\x001b·ÓBþ0=ûÑ:KÍÌVT&UW8(mFÚÞ3¡0ÙL°i½®3aÀU¦
Î\x0004Ó{&XGÝìa»u\x0019âP\x0000·[¿^U¶\x0007m@Ú¾g°\x0001ñ
Ùn
i·\x0003m
ÇõÁ»\x001e°8mMïi\x000buI¶N[N\x0019Ãj~¶\x0003n`\x001a®RèÙÖ`\x000b!Ce?ä:\x0011P u0ZÐ'¢gOZõw\x0004+lruÿ²\x0003\x001a	\x001a\x0003ðÙ\x000f¶ ¦4\x000bí8¦\x0005K6vÚi=N[ß{Ú*Wc|\x0010ÚáÛàüO9É"î\x0008½­òò\x001bÔCÆVÂ§ÎÔhþËfZ¬	¢g?ZïdyJÑ¤ -Á\x0001Ç\x00166Ó³\x001f­ËpÙD´$Åþò2¶Î
x\x0019<ÉLï\x000cBAÆ\x0016»RH²Z	3\x0018­Å±µ½Ç\x0016ÊÄel­(2%°»x&lÈwm§Å`/>ûÑÖMÊU\x001cß×»\x001e\x001b\x0006<\x0019\x000cäBÐ³\x001fªâö.@ëÙD\x0000ü*nÜ\x0010"NÚØwÒ*\x0008>ºzè\x0002¤l·ß£5Ãâ\x0002 g\x001fXWÎz£æq\x0005\x0017¥è,Û\x0001ípHVNÏ~´Á@ÀC¦-]P\x0006?[`~ÀíÀOÏ~°Qq
\x0016n\x00076/òËv0$-ì-ôìG$ëC»\x000cº°!ùºÕn¸Yk¦õ\x0010 g?Ú¬k
¸ªwU!×b\x00087¤³ö\x0006=ûí\x0008ÆKo
0h\x0014§'Ø:oý¦­G¯Á÷ö\x001a\x00144ï\x0016\x001fGq\x0012|¡µµ\x0000lÈ-Á{	¾¯ù¥¬]_³Hq\x0019uª\x0011¥\x0001Ï\1¥8÷õ\x001a\x0014ôteËÖûg´ÆbÖU¹À\x000c\x000egdïÌõôìyð\x0011åHBÂÛ*<ÊD·­_CÚ_!@å\x0006>{Ú_ªBË«Ä¨È¸3\x001bºé´ÓB\x0001=ûÑZ¹þÓ\x0011:O±µ\x0018%Á9?à2\x001a{è¾Bqë!i	i½\x0012,%)rI
8\x0013\x0012\x001a©·Áh -Íä\x001c×Ê9ed\x000bóaHC!áLH½g	Q¬ä3\x000b*
?Ï[\x001fô\x001bRFÚÞw9&zîk¢SÀÖxHë+m\x001aÒPÈ dBÏ7OVd
 \x0011Wté q` NjÂM+²Çt,zöCÎJôb²qÏ\x000cÝ?é,$ÁÆ-2^íÈ \x001bHÏ~©8ÆBkmDvIb¸ ëÆÈ>o\x0011òjF¶põ@Ï~w×åü¥lg£@\x0019F¹ü¼E\x0014{'ÑíõþA¦rù#\x0015\x0010Ç¾Ç[,±ÕDl\x0012´Câ\x001c\x0005XçAcè(=û\x0000G]]
\x000bÁrªø
ND¼@\x0018	Îã}J\x000cøÏýõ¿©¾¸¼þ8M \\x000e\x0006]tÇ{/Æ÷\x000fW\x001d\x0014\x0003·dûÆ¤µ§(Aèb\x001a\x0007Ë=0\x0000jôÛñ\x0006äý½\x0017ûeÂÿ²®\x001a¡B;¼ú[¼ùkÎ*Ð\x001e\x0017ápÓ.y¾§,;\x0005½¦£½W#ÐV\x001cØ\x001bìgú\x0012\x0017×8\x0011±¡\x0018@¡s\x000b\x0012[ü£çp@FP\x001fú"É¢\x0006ÉªlEJBA
ÌðÄ\x0011cïA¤\x0012
ÈëR¸9\x001e\x0000Ûá\x0018ÐwñåYw,ÙÊ¹ÿì²\x0001q!\x000eå\x0017Q-¸!\x0014d¶Oì\x001c¹l¸þ¶¬j\x001bGu\x0017{¯;\x0010DáYl\x000c\x000bÜC\x000c0È\x0018û0<2\x001cÔ1õFNØ\x0008\x0017\x0013äw\x00121×MA\x0006¿c`b¨3ÃGObÏ"\x0002e^\x0004Îúvàü\x000br\x001a8bTà£\x000fq(Ç&H\x001c¼d<åhdíð3\x0019ÒGÕsZò@÷
AR\x0002C)ã>Å=×CòÝûi¸÷0/4\x0016ÖÔýâÅÝãý\x001dôïCRµJsga¢°\x0004\x0002(äþýÁ/û£õù¨/	ýóµÚ÷\x0015\x0015ò¿^¨e+3ª´­\x000cJT¿^8\x0010ªÆ\x001dz6³\x001d4·\x0014$×Ó¼
¨ð¬6fÂ®,;¢fDÍ}PD\x001cD\x000c¢D3 ²×lðx8RPNÏVÒuÕ\x0017×wÜrØ±êA\x0019T=è rÙv\x0003jYK¾9wùê½ *A\x0005kgwÔoúó;\x0010AÏ°ÃæmöeÁú<ÞÞ®¡\x0018ÒvÉ\x001c\x001bÖDî/ P¥ôùá\x001e\x001cýrðæ`÷&\x001eÛX!è\x0017"¿ÝYå=Éä$%V\x001baà`½98>?ÜÚË«\x0014\x0014³ñÑ\x0014l0ÏæAxF\x0017Ã&³© !g@PMIÐÝA£°\x0008º\x0008¤8¤J±¨!¨3\x0010©¶\x0000IÏvÔâ¢S¡GL\x0001$fø&0xéåÑÕùOjK¹w4:³áxíFl\x001clUôl&öåT¢NH1[/­P R)°\x0018Iz½\x0012NGÔûO)@?\x0008Ùø·\^IÍo+­VÈT,.\x001a%º\x0019-«KGÅMçöI«o£éRh5tþáâý÷yµ\x000bfÆÎÁ÷÷ãÛ.\x001aºº\x001c	-R~éHÏÕ{÷íÉºçs½\x001d¶±¨A/ÖT\x000bë}Ùg5'æÙPYõÖK \x0016Vé1Ñ5z\x0008ãQ){aPMò
²}Xás_V%µ¬\x001e:\x0011²ÊÑuûuU\x000b+dýFß\x0015Rò2'µDI\x001bËÊÔ¤4è¸J9{/Vjú 5\x0012§<\x0017U
9_5\|á£\x000f¬JZ.Û¡zõÕÊµ[^ßr®\x000f,s!»6XX]<\x000b®WJ
ÛMÜêØ\x0002\x000bg«ãiÌ&u9³+ý(\x0019\x0016"\x001eÃÁ\x001aà£\x0017¬\x0013»[3@öX\x0013\x001dM<¬\x0016X"}GÖiÉxu19\x0013ý\x000cvC_Ý\x001e°Ð$\x001b\x001f½`IJ\x001da}\x001eQÉ%ÑaPX¸ü¤\x001bÐvXWvQI\x0019\x0003Í_ÏIXI2\x00184¶º-î×«ýßöötj\x0007¶\x001aÄ#´ê	\x001c¬HÙ8\x001dD%\x0004©ÞÐ1oMÍlMàÑá£\x000f¬\x000fZÒ°L¨rLÚKÆ»Ú3ëxUëífd]f ô:ñ=\x0007\x00183 Iâ\x0000¤°p\x00133ex¹\x0002ßi«·´ùjF6
üqzöAVÑH¼\x000bbHÒNÍ*1
Ï\x001cpû
ýö_§¬a©GÈ6àÂDã`¹\x0011³\x000fÛÚ©µ3c÷Szö`Êì<ÔU\x0016fÈ Ìý\ð³\x0015í¶;#ß¨øþÇ%lo\x0010T4a>ÆM\x0001/&×Ý×+ltx\x0018£\x0004n=Oèb¦A^ÃæÀ3÷ráÇ¶ ;XÎ«þè`MjÜ
8Å\x001c\x001c\x000bÙ\x001döó\x0019ýó\x001f\x001a´Ñpcr\x000b×\x000bì{¿\x001f;D÷ÅÃÞ	ÁsFrÙVx;¾W\x0017Øû}ÿ|]°ïââæí\x0005ÈÇ¢ÃÃýÞËéÝãÉCní©\x001c5T;l½Ö,î\x0011ËÉE!bïÅêÜ\x0002~º÷²ü²,u£>ã\x0005ÃÏ\x0019\x001em¼>pÑu\x001e»`#/ô¾"^\x001dÒ ¼ÚB»
zö\x0000N VFjekî~\x001dÁBâÙZí`|\x001c\x001fþ±;±ÕàãÑ³Ï\x0010Ã\x0014!='ý¥CVzVûüù¯û/NF¿oÊÝyA·þ9={ð\x0016W\x000eSÕÉ¼\x0013q ­\x0014=CB\x001d%\x001cU !Qi"ôÆ9R<sdf)\x001d,Ì~xf\x0010@¤g/fNa$YII^9$õÐÌNa\x0001RýærHpI«%ÍÌ*ÅÊ¬ÃðÌ¨9 tÏqNiDãlØ]	*H7\x00180FgöÚÕs[\x000eÉÕ&´åÀæ êt\x000eiø©¡±Ñ\x0003>û ÇTU3¬µ|xÈÄefEÓyïdÿhýMG\x0003nÆ²óÜsÞÉ®lr_"®j=E­éwÅýèÞêOÐ
HC¾óÁ\x000cl×Ù¡1cÙèÌådS\x0018Q¹^ftÝ6ô¶Õ\x001fXÍúåÝÕ·ïwØ]\x0014XírµÞèíÕ´ù¦,¤²Ã5G9ï8'Ø\x0007\x0011?Ô\x001aaÏ7ø­¨&üòàd+&^Ë?\x0011¥é\x0019\x000c4c6pÛEQ23Ê¼ò\x0003abª}\x0016Þ\x0011Ó²=	ý>ô3\x001eL©ÕVA\x0010k\x0018LH´ÃG\x001fLãø3[ØºÓpH¨Ì%\Mpzæ\NNîÊ©©ì\x0015n\x000c#KÝ\x0016N.\x0010)\x0006C\x001c\x0013\x000c}\x001bëÛ:rjKe7\x0013düy<5§ÿEËa8a<cÏñT±BRÓ²Òý\x000cr¨¥íWlê7\x0010XO93/u/º^\x0005\x0013]²a0Á"L=w$íë7\x00073S{YC~°¹é,ötê91QÙRÎÜÒä¥áHYéi¨­\x0013óxÜ¥®sÓPq
´36,\x000e^¾;×a\x0017C'Ç83\x0004\x001b9=¥E¨o\x0006ç\x0011NïÚãQ²Ý÷!pÞs1ê"\x0008@ÒÉmÝ´K»çwÿõOû\x0003û#ÁeÊL>ä×Éôf²÷bÜA+<FU»÷Ä2=)×9b¢!F4L`}Õ_G'¯F{/ö_þ¾\x0006wî\x0007Öð~x|¯ü|§:¬¿NÇ\x0017ÓÉ«ëë\x000e1;èÛÂYÅvö¬ \x0012\x0013-\x0019:\x0018#ø×Ááá¦×¯'s?µ\x0005ÛB¬Î.\x0004ìÚ¸¡Ó_õ®Âp¥O\x0014\x0015	\x0005©"?\x001bê"íäA#7tY&ìâµpDÆåÄ®
pº\x000eYN©NØ&Ë41)sÍrnHY6v³\x001d\x001c\x001b·\x001fïûcÛX{ «ÅéºAî6ÉÓ\x001a
ûS²ß¯Ì|«êoý>¾\x001f±AÑÝÕýÞe×¶\x0008YÐKÌ\x0003"eÐ¦(\x0018Î8MàçnjST=°ßËOì#¶÷âøàt¯þÀÖ)v¹É\x0003½\x000c´\x0010¤aå\x000c4z\x0019ni\x0015Ð§øï"jõC¼Õ¢\x000cSÞ\x0005¯ð]<§×dø2Òtc¨¡£+:Å
ô2NÞ%oì5¶ó»H_·AÞ¥x«?KõÃÌA
ÚüÜY\x0006yµÑ
õ2\x0005¯ËËh¸ÏÄ\x0011òeüÆ¦u;¿ÌL³]^ÆIÑvt^C¥\x0007¾L6Q¾û¹{\x0019Øi¨õ\x000fit¿ºGz\x0019é~\x0018pè~âËÍã@/\x0003­Gyý{\x000c\x0000c3<É\x0010._\x0006bg?ïe4äíh5Ð1cé\x0002=Âm6¾a¦ò\x001eö§~\x0014mÅôP?
\x001d\x001e¿Õ²)»±EáÎo\x0003Æè¼Îîno\x0003UrøÇú6\x0013\x000eËÛÀ=ËO|\x001býÈÚË²ç{¿²üQà\x0014ßÆÇzd¦ü6\x0010¶CmfÅ:®\x0019¦ÙR+WU¿ú©g&èZ?×CY3®X3N\x000eM\x0005-©\x0015élkv?ÕYE¼ÓÛHVJÄ\x001bfiÓj\x0007`îÞi\x0013a \x0006_ÁÔ¦y\x0017»l~kjê\x0004ùI
ô66T»\x0019DìèÛ$ÍEVÉ§¸±éíîo\x0003ÉõÉ\x000fô6Îq^@ù6wOoë·	?÷¼Y¾VÛím K*5PvIoc¹QEù6ú§¾
J&Ïë&ïö6QqÕFNËö4©çN>úºl\x000c¶N³\x0003\x00055\|c\x001fa\x0005i²uV\x0003\x0001ê§\x001e\x0006Ô\x0005\x001djK\x000bÛÂ¡aSv7|\x001b\x0017½¼ù©\x001b´qXÉ8Ø·IÜu\x000bÝg\x001bøÛÌ´k¦¡v\x0010>Ù\x0004\x0002ëyG\x0017ª)¬|\x001a³¹úÎ/\x0003> \x0019Ê\x0008\x0000Ï3èy{\x000ebÖØk¤\x0019¨a3i ç\x0006\x000eÀÛ3Ü&9lÄ¹ù¹k&cXs ÓA%8\x001b5\x0011åÿÈ¨õË¸j\x0006¬(RÙÉà®¼Ñq6¦$¯\x0002ÛÚO})¯C½®§&ÄÅ\x0013H²ýÜwpuCyPüÄ\x000b&\x001a£qNb4î§3\x0016ü\x0019;S\x0003¡
9eïéjh£~û2p¾Ø¡\x000e\x00190J\x001c
LÑGQ'\x0015êù©§Ì\x001c\x001d\x0003±.ÿ¬äÓ\x001cëÛä\x001ar¶°+Û¡¶fkUõ¡ïDàÛ\x0010ëÛü­yúî2ë\x000bh¾INi!Ëé°ü\r\x0010Xr>¦¬E\x000bÛ'¥X\x0016#\x001bÞâTpr~rvp´Q\x0013S$6\x0013;\x0003B\x0008ôl&%%\x0018çY0\x0014ü,"Ö\x0006\x0002±=LR\x001e;£bâ°O\x001cî¨ü¹ \x0006Ã½\x0012|2ì\x001dß\x000c
þ\x0019=û RÖS±$¥*i4¨4(iÀï\x001fú|ÿláVGP\x0013%\x0014^ j3$*6uíd;¢@\x001a'\x000b\x0017@VGòYäÅµ·\x0010Åÿµ¬©Bs¸÷j}rsGÖ]î1WfÕ±\x0008Zcpë¬Ò{B{é\x0017;³~²\x0017ß/\x000cf¿ÁEùB æÕÝíÃäj{Ù%äAÌq\x0006ÎK27é\x0005ÁãÈeRGg£
¢ò\x0003[`\x0003x×Á¸\x001e°Qe¹0)\x0019è
\x0008°Vl*ç\x0015u\x0014\x001e\x0010Ö\x0003¬ï\x0005\x000b"Ya\x0013·P
Öp·\x0001\x0007Í\x001e½È÷×7+dq&÷\x0008Ûp\x0000c	AàVå½\x0012ÌRÁÆaRFþmÓvpÈ[O]!×\x0006ÅÞ=¹brS¶-g1µµ,\x001bz4ôS`;{µtz|tt0Ü+P;?zîð
e	FH@ÅåHªÍð\x000e ®ÃÆ@kÊ\x0017Ç'ë\x0015Ò\x001bÉPIÏ]ÈËöÁkÓëCÆDÖ*q9qÆ±\x0019\x001c+{ÔbeO\x000fòäI*´\x0017ç
Q
9Ïy±\x0019Ä äxwîæoÐû
¥°B\x0014ÚÎfêc\x000bûaÉvÊí;æ4Y 5\x0000í0ä\x0015<
\x000eþ´in¿i.\x001doÊKÓ®¬9\x0014^|-ô¶\x0006\x0005Ú´\x000f¸Õ
\x0012A\x0011ÜjÞÈÓß\Faça¹\x0003\x000exØqÀ­5|s_¸ÅHÍ 3'äqè}E\x0007ìO\x001aÂ®äûÄ\x0017rWÉ\x0003ç\x0014òá'9vÑi×1/F×\ìïñ\x001clm¨õw\x0003£z×pê\x0007î5¤[Dr=ë$à\x0018×\x001dû©÷Ý»Ø+\x0007\x001cºC2w\x000e\x0002îõÐ|ßØ<E_OÐµÌ³1ÜEÀ«\x0018Þ\x000fñJÃ]ç¸+æ\x0015µ×*äÅè
DîÙZô*Á¡uÌszî\x0006®+xP\Mº\x0015J\x001e\x001cné¹\x00139Ø(ÈÁr1D\x001e¤Ýñ\x0003íÞÚë\x0000sÅ.tÞ:\x001aß_\Ý¯·\x0015$Äâþ9.QN!xÍÙü*iV	4NÏ_Rq\x0003÷ÞÑþé£ýÃµE\x0014ßÞÝL(©\x0002\¡DÑ£ñ÷é¸+\x001fAâb$)K\x0013o\x0012\x0007 uÒ¤ÇQ`þy²ImÍØ¾¿ùôn\x0002bç CKÏÙ¤x}}·½ÐÃ2o\x0013é\x0003j-G\x000cVs¡Yì)æ½><Þä£áooãÈ =9£\x0016MS­,K$âì±&UÊ$Ò³\x000bç÷ÛOF\x00133z±~æäîÏÇ.ZN`$Ñ½¹26sõ·M\\x0010`Ê¿	Îñ?6éÆìñïoÅtéza	brUµM¢ÇÏ!]8óÃíä"ÿ\x0001w (hæã¢×ãúx\x000f:SÛi
Ï°D\x0004¡`òQ<ä(\x0000¬\x0003±&ª\x000f,`§§ \x001cµ!7ÿS«Á¯¢¿u\x0018Æa=/ìu:¾¸î$\x001dñF>\x001br\x001d`èÔÁvóTÔN÷_\x001cnÖ®?±
\x0017*÷\x0016º·tÇ\x0005Í7M¶}V
®¡ù\x001eÃâl\x0018\x0002ÖÿHS}\x000b{\x0001\x0006ÔBËÓñÕíÃÞoÛ«É\x000f<Î¯\x001fö&\x000f-'\x000b*QvD\x000cÑEÞz­áì\x0008(x\x0005¥ûGgûÇç/V¼IyÓ³½ßFG\x0007£ãíøðlot¶õ«ïåñ½üÐï\x0005\x0013î´BçêLmû\¦\x0012­÷Z \x000cùÃ¾\x0016çC*\x000e¥åròN\x0018§úï\x0004ÉÌô\x001cô\NäßÃk\x0005Þ®l1V¬¼Wø¹ï9ázAö~o¥Pí\x0018ß\x000bzI«[eÙU\x0000«æç½A\x001bc~/\x00077n<
cæh5T\x0014'~/°-æky|­¡\x0016dWbí\x001dT÷,Dßè­´?uÇ0Xgal\x001aüµ\x0012ëÁ\x0004¸Ü§è¶E}\x000cz/èêö\x0013ß+A\x0011;=|/\x0010ÿ£¥\x0018mU<6\\x0006]JÔ\x0004ðõè'ÇG«L^ïõuòI]^¡±\x0003»a^´ÑNÇ××\x001dú¨y¸\Eã\x001c,5jP>Hbc2ÙÈ\x001d\x0001×7¡"Ûìtÿðpí0C]¾^k@u9Hÿ[\x0005Ò*=³³iHT\x0007%\x0006n¹A]×a3}6§¸sl95Âþýøè\x001fç[\x001bl\x0002þôõÃÉ'\x0018[\x0010Á÷yO'Ó\x000e\x0006d9\x001b°Â\x0006»+#\x001cår{ëp\x000el\x0013ì>\x001d¬5\x001d+bâ=|´Bbn\x0005éÔB·$\x0012¿på\x000fä\x0001ÍQd2¡ÿñh£´AGØ\x0008\x001bøh-~®¢|\x0000Ä5m/Q3¦ú
J«
nn&ÛfÜò»k.óè¥ÓuyAé\x000b\x0004ÒóÃÕ·O÷·Ø¾\x0014ú­¥-àÍøûý}'\x0007'Ò\x001d© N"ºÐö\x0001\x001f¸uÞþ?OO·®¬ÙOmáFº¼Üó¸\x001bS() 9Åauh^Ézâ!X÷\x0013ÀË^në?âå¿Ï¨W]ñy/ÃnÓ\x0004\x001e£þ\x0019#N2<ôì	^ÀøjWål1xbßØ$¥~
8&çéÅ\x0014½FðbÌr¿\x001am
Ý3&'­¶LÆº\x0000qSûO2·E4G'ÍÚJ|î`ÐÓ\x000fÓo\x001f(Ø\x000b£½`Ô½Lo'÷o\x001f»~t^l7åYûÏBkd6Þ"dF¼\x0019\x001cQúÞzæ¹YMlÞÇ\x0017\x001f0!
NA³p3
È\x001f¶ÿ"4±ÏHß§¬<ÌSVFÚU\x0000\x0002°x°\x0000Íï\x001bSsä'VÃ^z÷ñÝ\x0017Ô\A\x0015³¹SåÍÕøz<íÄlÎ,ûjl4ÎEÉÃ)¬\x0011)\x0007ËýÃýMÍ5êOlÁ¥hÇB²Yw^\x00174[mÅùI¬fªá´|\x0018\x0017tzñÑ×y1,\x0014}1¯«¼&
kà¦Â(×\x000f\x0017òOy:XÅi\x001f1g¾YvÐÔ`hÞ§Z¦oà¬bÆ\x0019Öß.ÓWW3Ó:\x0007ä\x000c2\x0013U?Þ©£há-®¶ãñ\Æh':øøB%\x0001>zÍ\x0007Ã7Æ¸8\x001b_N¶\x0019û\x0006å}ý¹](Pn\x000f¯^1}¥\x0013S\x0016Ííq\x001f/³·ïP#ÆàµÛüÙvu÷x=~ß×Ââ\x001eée§ -öâ'so\x0001åtm0ûÛú¾½p´ÑÏtà]n|×Æ[fã×8\x000fðfCñ!à\x0005\x000fPà'5ÞMÀ º¨?z1&9 9Z:ãÂÁ<0ðòÖ\x0008ì\x0005êA_LH`'`'=ÑÕ\x001f\x0014ØB69>zMä¨qT\x00016E\x0018\x001bW¦ðÝÛðÕ1\x0002Yö\x0011w\x0017ëÛ»­  \x001aÏGeÍ\x0005ÖçÄ@¯üÆ®.ç¸'ðïnÁÛ\x0011Ú\x0000cìä[W\
C¶Ñ,yó\x001a\x0004ÒÁí+<Z!½æ¾²§¨	\x0012äÒ*eÞòòÃ»\x001f.`Ø\x0014Å\x0018\x0012êì¦·\x001drWFÃh£b5ÓF¹>5î|Tó[¶aY\oÅú\x0019e\x0005Yoù(ÍJ,«lÖf3u\x0007\x0013,k!³Jqqµ$IÉ¾uÐHlW8¸pÄG\x001b\x001cdS9\x001e·À)²vVà°©uO¸·ßoß]ZÜS ª¢a#ëëB³}ÿ6á|<I¡R3ÅÚ^5
­*ÏÅ~YÌ_Öù¥3L\x0008@Ù~ 5kSZ\x0002\x0005Â¢\x0013Smè¬ÚÈ©qáÎ­Üî ^A\x001an®\x000b\x0017\x001eÜ	XMo\x0012Ä:\x0007\x0003­Òx=@µôªõVsÖ@ú·Âi7\x0004å[91»\x000b»Ú9\x000e0CgÝ+¨ÞÐ²º\x001bèÕW{ÿýÃ-ûqïåäö¡K\x0007Ê 5\x0007\x0002Ë\x0004È|wd¬0ÙxÍEÇÊËÑÑÙú\ÊX\x0015w[\x0019½4z-6\x0008_\x001a(Éýæ´£þ\x001fÜ¿»Æ \x000e´±s3Æ\x000fãÉøq;¤\x0005¿Ö¹6öYÀuît¤\x0004	H:\x000cn\x00047Vë ß?\x001bío£Äè\x0010>Z1
¨çÓ¶	f#y\x0012\x000e§Y\x0005[Õ\x0014®ÞæÓD}~\x0012«åp¿*åäæê¶[ÿÅ\x0014Ëò¡úr"F¹\x0015pAB¦X|´9h*°£W\x0007G.ÚOîï?ãY	Ûûü×wÛQ=\ßS~½í> ª+Þpºµ\x001d&èáñv@\x0003á£\x00110R=\x0014. *\x0015)|A×\x0005ävâ{xHcý\x0011·!àc¼w·÷\x000fãÛí|Ù\x001aS\x000b+Às\x000cll\x0004±Á×\x0017áÖÁÑéÙþÑ:¸t3}¸pà!Ì\x001cw_&ð(Ùoù¾eAKsJÜ|×BçpùfÔ\x0005\x0010J{\x0000:Ã«ÚbËX)©áºÎB¸¾N¢\x0010¼Jã{\x0010zî.\x0002¾\x0012¦$õ\x0010¸Wô'Ì>>ú	\x001e20s\x0012~½úÑ!wØ±¢<0PÐr v\x0017Ó3^\°ÕLûõà_ë\x0013+ßÂ\x0001Ó\x000fä?\x0008Ïi\x0010üC<)\x0015°Ðm\x0018<HëHíÃW\x001cgNe/\x00168\x001f+6EIB°\x00116\x0001ø4\Lâ£\x0011Ps
-\x0000*n\x000bhî6À¹7\x0008 ^*Çv@ËQò©Ó3\x0019PÉ\x0004Äú\x0010\x0000®U3 \x001cò-o69§\x00050\x000cô
^\x00127ârö²:~\x0019A\x000bÆ\x0018]XJß\x001có0\x0005Ú\x00015_J\x0015@iIW(\x0002\x0006úÄ}iW±JR}¬
\x001c	£$\x0017\x0006T[]«na°\x0006@óLÖþ\x0007Ä§d\x0011{·Õ£êÈ\x00071\x0013ù¢ôk/\x0003¨Aa}hn dQûk\x0008@èóV@
\x0000\x0015{ÎAæ?p\x0010:Ø\x0003}ó\x001e¨\x0002n|è1ÅÌu\x000e¢ÔmÁ¶\x0019\x000f\x0012¡ðÑÊ§¹p¹ðEV³±Q: Z\x001fï\x0002è\x001e.?]¼b\x0008bÔá×»ÛñÕm²\x0017«5K\x0003\x0016cZUcÚZ	yÆ¸¶ö´F\x001d~=>:Û?8Z\x001b yûøî:­\x0008\x0015ÿýñújÒ%¼èUÔ)Íö Ê^³¾$ ÿ~~x0Z\x001b`¬|\x000b\x0006k\x0003_°l\x000fZPÕ\x001cÍÕ^ÕkI;à%g¯,7Áç¿ó«ñÕ´Cù× ÿÊk¥\x0000f.%/Ym?Ëw~µp²¶hlYó¨Û9­¦«VàÔ\x0012ÿLQzÊY,\x001c\x0013erúq\x0016\x0017Ã´ ÚÊæW\x0010ãÆè.Ñä÷Ó÷÷ùjõê~5~è\x0014SÔÎ°!F\x001dÐe8%¦Øòl}DqF	ÇË½(}âDT
­$ÙØÎªRBÔ`Ø\x0017ÎôãÔ7ï²«s3§Ê©\x0006\x001cO¸ü÷¾\x0017'\x00144s\x001bö,¹e<¥uA\x0019ÞÝ8?_|¼,¯±ÒJ8ï÷^}>ti±\x0017¡¢kÄSTI\x00033èk:ÍyÉ$½YûôËðÿyr¶©»Þ\x000cÖ@Vê\x0007[,4nsTf&\)\x0000¬MÒ\x001eÈÄ-­4Úa¥\x0015`;¬Ê\x0016ì]5Ô\x0001+ìæ^F\x001da\x001fßÏWO.[\x001f÷^O'÷\x0017W\x000f]r]´B\x0007aËyèåâìbè/µ¾k4\x0005{^N_\x001c­Orã,Ð\x0014*!ãÊ>\x0001
\x001bZ\x001d7B¸~.dß\x00061\x001f\x001cQÐýË\x000c*Ú\x000b\x0016\x001a`\x000f\x0007]û\x0016³Éd\x0006
Ï¨¨ÝK\x0010£pÚõ=9!(\x001cs?NoÈÓæÑº\x000e¨­Í¸\x0013|»N'×o<âºÞ\x001fa~ç=½º¿Ûn\x0016«$?ã¨$4ed7ä\C\x001a\x001döý×'\x0007§ÇëLÑ\x0019em\x001eÜÒÌâ\x0006b\\x0003\x001bÛ£
ØÜ¼\x001f§¹ç~\x0016\x0004\x001bÙí!Àmw¹¬É\x001f\x0018ASÔ-\x000cçÉÝÛN)\x0003	ä6è&Þ÷f]\x000eõ¬7](O_®?ë?úoY?õ3\x001f÷Î>L¦w·ír0ÅvR|'¢¡¿µáÚ81IO[Ìúó½³ßG'ÇG¿ÖiÁÌ0\x0017Ìú6Ì(:L:B§\x001c.83CFÎm	y´`ÖÆ¥=FÓQ\x00010Èc\x0007®$*\x0016\x00149=$'Ô~gßÓÕá\x000c\x0005ÙðJ/;¯ ì¶øIÛ9\x001f¾¿½×úe_8ï\x001e§·\x001d(³Ñ÷#kmâ»ø,RéPN½1\x0000R\x0010ÏO:\x0000BÇà{\x0000*Ñ¡/¥¯:¬ÙIrÕ.x\x001f?Ý|þö\x0015¿³Â¼º\x0005MÇ_®&]ªtË÷\x000cÐ
Ã\x001f >â	0z\x0011-~K\x000céìdÿÍÁh}qn¥Ä¡M?LHÕ{cL\x0012ALg$ÔôZ)ÁVL\x000b!k«úaj¾|*ÎrUÇLvK\x0012bwJøÜºç7W\x0019n
É\x0019ÎøK)òVé\x0015Ê9ìy¡ÃuÍ\x001c¼\x0000-IÏcúb|ß%¼\x0019\x0014»m\x0016\x001aºÈe<+v`xsÓòy±zº/¥y¾Úø¢ç ¶uµµlIV"\x001bd"7ò?¦_?|úYJ
¬çÏ9¡\x0006dçî\x001e¦½_Æ7@h\x0013\x0011ç¯ï\x001eï\x001f>ÜÝ|\x0007¶P\ÛøÌ\x0017© QÌÞP¾{A\x0003íÓ\x0008"ïÏ_CåõïÇ¯þù3g@`îøì¤|ââ]nG\x0003'·\x0007S¤1VÐ²\x0016´²/\x0004bK(³3\x001côFé3n\x001cÄ,peiàÕb\x0019·$l\x0006Ò+vf£TØf¶-
ªzQµ¾\x000c\,\x0006\x0003ÁEØ]vàU\x000f8ª\x0006\x001a8Èç
<áÀ3@8¦Ø\x0019ä\x001dá¬§ZbrÂ\x0001ô-#Ã½;\x001cEøáÂÜgä«\x0004\x0010vròYá\x0016gW8õµÒõ«ÎGrLj¡Ü\x0016è²vCÐñÝR3]VÏhµB¹8Vûrt'tÙ\x000e1é4\x0016tµÃå²$ðâ¦Ð¨&:'	¤\x000c@Ç]3÷P-\x000btÅv"D¤KY>lð\x0003lÃrÔL\x0007¾Q$:ÃYZ¡xÙ^è¢\x001b`ÅÂé±(rÎÔE¡F¦yçP\x0003é AkOºøÍ<þÐ+þ×\x0013\x0010pý¯ÿï~\x0003[6\x0001Ê\x000bÖr crý´
Äö×E\x0017ÈOþndÅC¼Zµ¢ËBæL=¾Ö-î`Ë§~70hDÉC&>P\x0001ËFÎ®¨×m#ÝÉÏüd¼p8U=\x0015\x0005hË¨ÅVRëüîdË\x0007~'2(iò|ÞÕàiÌ.\x001b\x001e\x001f©vÝ\x0002íN\x0006\x001a\x0011ídàx9"+îe2§äkbíþdËvH7²rz6.£¢ëBæëÙ¸ûÒ¤ÒÍæyf 	\x0007É{Íc\x0016¡Àü\x0014w_\x0001ËæQ·1\x000bz\x00152U¬8\x001a2ÔSA0ì±\x001bèä¶Yñ«h\x0001\x0014#\x0008¼~\x001c2\x0010ó%²\x0010Ö\x0001ÝÉ\x0018mÈ /-¯\x0000\x000fýîèð,G*¯âÐ;¢q}ë i\x0014E´â$+hÚóé\x0014¡\x001eiW´'Æd·V\x0000\x000c\x000f®\x001b\x001a*G K»Ï4(:i?\x0005t@Û\x0016ÑA\x000bÉ\x0002\x001c\x0007»=±q»¥@Åô*@Ó,GçS²<Ëô<~\x0004ÿY¿36\x000eï\x001e®îï'7Ûnl hhçðÖQa1Ò²ßÅ^d;<>;8=\x001d½\x001a\x001d5ÐÑ¹ÞN\x0007Rà\x000cA{\x0010à¼×\x0012 ÚàÝáè\x0000m\x001cz+«4ä@¡Ã8&­ÒûÒ½¿|¿}³o__ßRÉøúËøjºÅ\x001d¥A\x000bÐß\x0006Í8±ÓbÎX¯\x000f÷_RIÉþáý5\x0017¸\x000bL4ÙZ¨Lµ`=-dÆÑJâ¾\x001b\x0016ÙµmXsla´8E¹`é\x001aWPK¶cW¬ðñûÕÍÕÓ/8Ù»þÿëÿü×ÿ~}u¿Ì»g\x001cK:9M\x0019;1ÐL\\x00056Ú;Ü\x001bývx°6j:\x0007¶ð\x0019»EG¢ð%#É\x0016²$ñ¤ýÊ/ÙB¶ð%\x001bÌ\x0000Ä%gd¡º(ØTe72ÚÉÉ@,Pí3`Ø´x5¾\x001b\x00189(í`\ã\x0000C&!_Õ[E\x000b\x0016m®ÍX×W§X¦UiµÒuù^`ß}û~Wí«¿Þ]MÇØitC0h6ñËÎjy¸RrÛvÖ_\x000fNö×ô\x0014]ZÚX·Ce¬`åR\x0010ÓÀóÛºå5Ûjg¦¥]µÓ@iR[JpsJ\x0003%ökRa×Zí\x001d¡,ÕCÑ\x0001ä<CÅº\x0006Í¾3\x0014ù»­SJóçóæéJ:¯Üå\x001b È¡l\x001d©º'(0.\x0014v*ß\x0005J\¶&*¨a\x001f7\x001a±ïAjqM\ #U¼±_¿þ¹ò Kß`×\x0004ºs\x0007¬,1Xwî|¥³rZmK\x000f$£\x001e¦½¾\x0002±æ½\x0017\x0013ªÑÙ\x0000æëWTÄæ\x0001L× _õ\x0015_\x001f8óÞÑººðÇ¾\x0008\x0017?æÀf=»Ç÷{/ïn.6ùâ©iöL"¡ ¨z\x0017ý!½´=ÌÉ½\x0012ö«\x0017]Ðh+mD\x000bFË×ôJSê^A°p@ù]ÉXã§LE\@\x0006YÄ´(\x0015t\x001c#4¿\x001cMïvÿÃ_|û¶ú{¾\x001d?Þn¹oM$\x000c\x0011\x001e#Q~lð¸´ëåþùª\x0005¨'_r+T*®¬D7u~fø>Î)JÙí\x0008E§bÓH¹\x0015ùTÔêY»_ñ´6;2=XÛk!!Mã©
\«\x001a-&[;á;BÑIÝ\x0004UV S\x0014kYE';ßy¤È*mrR\x0012a¤\x0002%ÇCBF
þf¿ëZèÊÐ	*dî\x001f_Fª\x001c\x00131
­ãì®P,rØôù"\x0011Á<¯1_êJ»~=.\x0012l\x001a(+÷}ÞGê-\x0008\x0003å$(\x0002å ;A=é#×Ê\x001a|S¹NtjÌ2ï¸wÖrÔ\x0016*èÐNPeKà{>\x0005Y4Tjéj´\x001dÃ¨MPÑK>7
\x0017j\x0016ÕÂ³k'*Éýn¢\x000bÚ?ãïgåâ1ì¼'<iØÓ\x0005ªWÙò¬²r¦¬xõ!¹\x001dçºd\x0004´Q©jô\x0015ÁO¨¹\x001eÕ'
Ä\x000fMë\ü\x000eÚÕmñ¿\x000co çºwi×¡zëÖm¡LK\x0016ý
Ê\x001dçúæJ¨\x0012U]*øï3#ßã·~Ù§ï\x0008õ-ß>\ØUÆ'uÜ:Lo¯n7Ç##±ç8²efÅµ»èéþÁÑ\x0019t£9:X]Á²·dvÆ\x000b^¬\x0000MÚ8(\x0019Ø¢Ø­rw¼%´3^¤UN£g­Ä\x0000}\x001d½8\x0004ÞmÚýãj*ôÑK\x0012ß2ÉËi\x0014ói×·d¥vÆ+.OÖuô\x0012\x0007vµ©!A5ÈÇ]²W»âe5KÔÕº¶\x0015¼E\x001c\x001d\x0004oÉrí>z¹ÆëÁ92WÝ´¬\x0007ù¸K6l÷ÑK$3\x000f£gI\x0016¿üÂÖ\x0008
(\x000c·dÎvÆôfW}7Ï\x001f×F·Í#iÂ[Ñ ¹#á&)0|±~]W7>r\x000eÀ'õù|Yå\x0004­EäRFÓ¹QÌ£zÉ°.rÑÆ'*ÍãgãlüðÙL\x001d¿!VÇ\x0013\x0017¡ëøiÈâáKb¥ø¹kÀ!Î
I\x0006i\x001f=,À«£Ç\x001e¡n}yi×Æ·ìËt\x001e=«%e<Àµ%§«(ñý»<\x0008\x00086_ÒÌ§\x0003\x0015
â%@]½qÍï×Õyü"+÷Ò%\x0005R©(qw\x0013\x0007Y½ m×ëð¬nGg[ÍÍV2ÿò\x0010'ï\x0013ÿ°óðe'Ï\%¹ä6e9ßÄWõH7gíÄ\x0007`)\x001bõ\x000eZ\x001fJ\x0010iåñÄíÊWþ8\x001d±ìj\x0010u¬yÚCÌ¾ªÒ<| *ËÏHF´W3³tÝ=F\x001bÞ²ÇÝ}ö\x0005ª\x0000-£ç¼ÔËÀ¦Í¥\x0001jM©
\x000f:àô8;²Vê*\x0002´@¡Ñ\x00132á¬ÙNT0ÚOÄñ¹P,D+£Ì½z¹\x001e\x0007\x0019¼2M¯lÌVWÁ.Ð²1ÕÖÞî5ñAé±í³³\x0018\x0015Ål	IÎµ\x0008r\x001f¼ñù!\x000fü*Ûgå\x001aSç\x001e9Ú£@g^N}iáS«ïóÁÇÎy&Åt¼!§@u¼°!+Y\x0015~9~wÞáò}\x000eÃ+Ý¯ù\x001c WÅ«ÞÔ\x0013,î\x0006Ä\x0001\x0011R\x000f\x001aM Mo\x0000b\x0010§åß\x00084×\x001b¦\x001bÏ\x0012 °@@^Ëc
v7 \x000et\x0007²ªFê \x000f\x000cÍíâ\x0010ÊÖ\x0010Ý	Ã$Ý\x0015døé$±9\x001fL=ÅC@\x001c\x0018é\x000eTl1Ë¬\x001cÜ\x001cr\x0000\x001bCË\x0017z@\x000b=Ë:\x0000i­1OÐrí\x0002²\x001b-û <sz\x001d¿\x0006c, ¹IÞ×rQµÕÒ\x0008T£\x001d
«ÌËµ~2µ\x0018Þk1\x0017r\±5\x0012Íë\x000fv#
^®Z kHf"#RÙú>ÚRo.DFËEg]¦µRmaÅ5\x0013½5fü-.fËòÀëï©¡k«ä1\x0013Få\x001e²R/»i\x0001/PÍ\x001diÝ©R®ißúÏN#{¶^¾êÁ5w²uçuRAN'o:Ô\a\x0015VìL`ËÝÏ:y%s\x000b3`ùKZWÁó
zÍ\x001d,ÝÁ t#(ÐÏNsÆHÔë\x000cõ\x001e`sûyw0SSm-\x0004
áZµauáºywuù0]¹ »$Ræú\x001d½%5qÈÙòµàA­`\x001bÓ(ç ×c\x0007(¯ä¸	Ò\x000f¬@ù,Q&»TºÕ\x000eµ¼\x0018»¥J&lÐâ"Ì2;½Fêû&Þä§Þ\x0001TCÝ=n$*ö®|}WoéL\x001d&½ì2³häèÅ}Ù³à\x001btÁ\x0015õ@.³Èqè\x001a[]/´á,x\x0006]p\x0004c\¢>\x001708®&¯BÝa\x0016¼.0zÃØD¹ï5Õ¿LÆî³à\x0013tÀ\x0001U
ÁQR*`fÁ¸ÓÄYp\x0008ºÐd\x0012l¦\x0002"Þ\x001aM½L`ï³à\x000etÀQ5L\x0006ß*ð²Ruæ\x0018»Ò=é³à\x000ct\x0019T\x0015b\x0012ÛÛ`VJu_*IkÄYð\x0005ºNª\x001c\x000b©)48¡\x000eÎro\x0013Í#Ðet¢\x0008ÙäêùUù[etçYt\x0003º\x000cO\x0016!\x0011ðsÂª]0Ùåñ6ÅæqÝÆG¤0ÔÜðÈÒò;í;K>I\x0017\x001c%r¹gÔLKï²²ê­eWã,TS£ºæ0¥°ÓçòÃ÷ë?'+Îó»ÇéÃø\x001aÛªo<´2èá"ùS+,'?0ÑñùÉÙþáþé\x000bP§z'(Èïâ9\x0014j±.æ<òêÓ¢;ÓâÑÞÉÖ\x001c\x001b\x0018(\x000eYLk9]¶iñïöñ=fk ÍU{¬ÓêÙÔiñïÄ\x0004ê\x001ck«\x001a%ÆÕ	¾ÊfmBZ<ë»}:U·È²'XP}'¦Å\x0003¿\x0013\x0013ð§º\x0013°XI"%2â»A-\x001eûÝ\x0006ªÖ\x0019@ðßËÇ3UaiG¤Å£¿\x000bRvJÒQ!PÂ³\x0000Îr~G+Ô²\x0005Ði @\x001d¡lH¸\x001a=«¬_¾½i¦Z²\x0003:¥nàð»Zd\x001a*Z\x001dTnZ2\x0006:
UHõµ,>N\x00087IÇ-\x0006Awª¥S¸ÓPi]+Çâ,\x001dÖújÅ­1¹»SÍµ\x0004îLehÛ`l ª\x000eJñgwÜÏkK\x0013T¤öoà×jëÖ{±èÔrjn+ÕB7Î\x001f0×¼¯²kU=É\x001aFRkÌÞ-T\x001f>ý¸û¬VÆ¶@ç|ó¦`UE$÷p&ØY p]À
¤Í·\x0003-Çµ¶\x0002\x0005]ýJãEôÇD±Ybv+æS\x0003ÐrLk;©A2B3 1XÖ\x0007»\x0001-\x0007·\x0002\x0015Ib·eíÉÞ4+ös+\x000cÍ\x0006åxòvT\x0004M\x0015+3¹Dæå|£F å8òV \x0012Z¬ËÓ\x0003UÕ§V¾Ç¾|4êÏ«§\x001e\x000bÐ4ÌöÂYk\x001aêM¼[í'\x0000Y\x0007\x00119Ê\x0005w¡2ç\x001c«ú¸0÷Æ£¦rÁXo¤ÌÐYv\x0016\x0012«Ið®æË¬¾Þl§\°[)U\x00032ó\x0017¯Õ¹å\y\x0016u¤ôdÆwKóò
ô*»<~ÙòÜç9'Q*«óLöêéVû\x0006Z\x001dÎßtàíý]yTÂâÂå¬|]ófW-Ü\x0016 Ùè\x00063(W,å0b½2;+ó=\x0006èB%ÃþÁ\x000b¸Þ*\x001fî?\x000e¯&{¿\=ìýÇ\Oö^Ý=^_Ýîý×ÿÝ{3¹}øÿøA\x001aeEAAf\x001bWð'\x000e¸T,x0:ßûåàlïp´÷êøüðàhoï
È¿mÃ6óØf7l\x001f¼\x001fÚsáÊJÔ\Ëä\x0007¢vóÔnGê\x000cKÔÅ¤Ó¬w!:ÈÖ.Ý7Rû?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9ô²ÈÆ\x001e¡n@c¹ç<·T\x000e_D{Öº¼	mÂ\x0000\x001a\x0004aæ£1sþA2Ç§Ô\x0006Ës³\x001a;wMhÖh \x0013ÑÆìÐêÏBïw¿ÌÝIô\x0002²Ao\x0002È@n¢
=º5ÕÅ\x001b1ôM\x000bÆ¦ZÓ\~"M´¤þ]gj=Ò\x0015här5käÊ94a¯¨"âYÎý\x0018\x0001ØD5ð±Ía\x001c2Çp¬Áuú_èñ	¹­\x001eOÑ89\x0019Ú94ÚÐé\x0003\<-\x0017¦jñ\x001a\x0001SÝ\x0008tâÃ\Uín<ì\x0010ØK\x0006Ó#_Ûf0Åh¯wÞ¦ä\x001d(¨Î­½\x001dØ\m7×f7148ð:K\x0013É¢Ïê\x0012Çák6ßÆFMU¬M\x0007`ÈÒÉUèãæòM`¢^¢mu\x0006÷UöûÀÖO9\x001fD3½Àqz\x001d¶u\x0000ª#\x001cç6Iß\x001eô1rã\x001cf°Õ\x001b»hÚÙSoqb\x001bzÛÜ.O½MlªÚ\x000càc\x000b\x001eÊ\x0015ÂRâæj\x0005çM³
M³¶!U3ë´¦½@9Í¶äØ!n\x0005·N7\¤ÒS*¾²Ô\x0002OA9é\x00024]£5y]g9Õ;F\x0008éï\x0018
²+·äH$t½\x0012tÛJ\x0010
´
(\x0013\x001f\x0005Ì ©ØÔcðÕ\x0019\x0017>6­\x001cyºEèATVXâ\x000b\x0016©dß-hJÑfe\x001dhÿE²\x001cV\x001fKü¶Éj\x001dÀÇ&2FºT\x0016¸QHdù\x001c%\x0017\x000c¨¶fk\x001bPii·\x0002Y?ÌÃö$Bç\x0017ø\x000f©j»©6»,\x0005<(5
7QRZ²\x0010¤ªí¦ÚìÆõ Ö0Áå!\x001b7\x000b¬÷\x0004Ù¶'\x001c)J¦úÙÈßçÜ\x0012«
Ê¬Ì·Ymx;ë;\x001aÄ
_r\x000e¶l¶m²ñ|Öh\x001cÙòBàKÈê©Ö\x0014Xd´ÔD))ßkü\x0002§«Xu2'ú\x0016¶\\x000e\x0013ßj×9ïù\x0002ï¡D5 Q¾£\x0001-Üàq\x001b5^R\x0007^)HH_\x0005\x001b\x0002$¤hºmDA8â÷%£BS©\_T½DUÛ\x0012\x0005?<PF­üÆ©ÝÔf	«ü\x001a|lA^~\x0015(ì&\Ö¨P~ÁM×Û¨nÛFc\x0007!T\x001aóø\x0000±\x0006ª\x0015ÎÚVg]øØÂfÙÆ<		{x³À·\x0019V
)|l`Ó67a
gKò\x001fá\x001e^3¶ eê\x0003¥i;P\x0010Ç.A:«IrI²§B-\x0018RSß¬LÛÍêE³µÕlÕÂ>Ö(tÓÃ9.²rP?eÉbk\x0006.Æ)ëAù|äLeÕ:¹`\x0015Øú`Û.\x0008PÏð°«C\x0018$®\x0002PNlvÁ"°µc³mM­\x0013ã¹JSshæ)W%OAVU;\x0015|lAsN)\x0005Ë¾C,´yYù5øØÂ¦\x0014©>	6\x0003&0O\x0018
^\x0017<RyUm\x0006ð±	,gÇ	cé\x0001ÑúV9K\Gøó§ñvðS£÷À§*\x001d®ÊZ£ûp$¶$@	t7cº&\x001f¢¨¥.l\.Í8ÎÕ ~¸àL)¤ùñq\x0004õ¦+ÏÅµá¯âFùÏ.vá@4dÓ	i×b<ÐcÄ¤\x0006·zÁ©ôW²q\x001fìVã}\x001c\x001bïcS°RS_\x0013h5\x001brCüÙ-;%Õx0õZð i\x0019úa­tÊé\x0002GL@¡l_`½ÆÖkY·\x0016R\x0018lÖ¨Á.÷ä¬¡Wö2ã}\x0018\x001bïCñÂ¦w{=ÄÖd¼eï\x001eµ[\x0001ãµ¸\x00153×\x000f§¹ü*tÔ@÷óîç¦(Ü¨\x0012¶Y\x0012Ug6«\x000b,z	x\x001dãýµéRèém\x0006Þ¢»4Õ1óqOãÍ«zp÷jzìÅPÚSÐRS¶ ¬F¹¶¹Å¨4¹_:÷nÇ{ÛôJÝ%]¸ðsôÉÞÓ[ªXèwc¯Òb;\x001d¦N\x000bCÂû\x0016\x001eó\x0014VÁªqµZ³évcÓµÐý±ï©°.>×EË~öÇ®\x000b°Þ¯cëýÚ\x0014\x0005ËÏ"ÐðSÌH´_:¸\x001fÆx-^Å=\x0016Õ@|
ãè&çeÈ%	@@÷ïcºo
8yR²÷2IoC\x0012È¶;\x0018\x0014>\x0006\x0004hwc´»\x0016Ã\x0005'çQbJqH¼I1ÄìQüÁCèDi¸V#\x00191­	Öwÿðy÷Â\x0001ÙeÑe%(Î/D> £:dùw\x0017çÇÓCK®d\x001cÕÏ`\x0004)u\x00199­\x0016qBÍx>ã\x001c\x000fÜ¶CÚ¼:"$\x00069åîI1%¹<\x001fRUª\x0003RyºK\x001a%©Ó+·'ÄTcÒùZZu@ªlI\x000fW¼\x0010\6\x0007TôçAÚÊ¶ÃL¢(@Ìé8wYêBð¡\x0001rHU\x0003Ho: 
ÝÍå
\x0003\x001brxò9Ð4c\x0016$\x001f"ñqá°q\x0019ð\x0008-­Ê¦ß!µ]ºrxí&9kwÚçütc%õô\x001dmrB\x0019x>¥¬m)Ûm©¡g[ðì\x0016/¹\x0019´SRçSz^Qúq?\x0019Â`/_píÒ`80wÆvz¤Ì\x0014¬òBµ»!Í\x001c=wXc3C½Ø³¼\x001eJSS¶/ñ?RT\x0003\x000e\x001f)¹£Åc\x0002íHÉM®ñK÷\x001dÐm+(ác+eXã¹?\x001e\x001aÅ-Ü¿æÛËÒµ#®(	R¶C:\x0005åå\x0011[x:kæz»ÐV8ëZâ¹\x000b¶	÷i©3AÑ¯ð3\x0016¯qÁ\x000bi\x0010»ö©ii©éñ\x0019çl\x00127Õ\x0014±	ôÃ\x0018ôÃW
ú8\x0006}üª@Ã¥>u/êSÇÓæl÷øx\x00101
øiÒVp\x0003DÇHôW\x0019=%erv|}}<%pºÓ­p\x0018­gt]´^äìÈö\x0013\x0004÷ñ\ÍçZù@í\x001cÃwØ5Üé,WÏ&ºôÌóõÈúÖõäô¡+\x0006¦:H\x0011&¡)¸Y|b(ð\x0002>øØÆ\x0007¥çG~Ñ©Üuªç
ñM÷Ýâ¬ÖÑ	_Ô½öR\x0001ëåýÇ_\x000f!j¡9	£ÊÎ\x0006Sá&ÃM\x001e)R\x0011ëåÅÉ÷ÓvDÎ¡÷*pVWgrqdÐ\x0007A]_Î
Eá=sSw°\x0006P«JP«:@9<ó©\x000c\x0016å\x001aÊx>Ù\x0017®\x0001Ôë\x0012Ôë\x001ePC2'±=`ÒÚäC£0ÏØÔq>(\x001f
Õã\x0014\x0015¢T#\x0016Ø³\\x0012~êxÑ\x0002ªjÐ®±ÿ3@Ìí\x0008ªY\x000f(,!¤\x000e%n8çTC\x0006)\x0007+ÊTöB+\NÚ d\x001f©Y*7Õn¹\x0005ÓÔSÔôLÑØ8ÌábRØô[¾ ¡ì°9T°jè\x0005ë\x0019z¦Y\x001ez¥Q¼&Íy7ÎÏé#Õ5ij\x0002]¾G\x0002{\x0004ZRð\x001fËXuòjk\x001d&®åèIuQëÃ[
j9?Õ\x0017²TØTØ\x001eRi1SWIpG\x0001GM
¥ñIM=MM×4e\x001aï")ÇWl°é\x0014f\x0013©¯\x000ePÂw\x001c¡`Á\x001c	ôPÂS¿MKÛ¨sbêÞ\x0002jjPÓ³,Ãz\x0005X\x001f%Í\x0017\x0000±_~0¼\x0002¼\x000b4\x001cJQ"SÊ,ärC7¥NÝD**\x0017\x0005\x001f;H¥Á\x0017ú(XRÐSê\x001bWÎtÔôÂ,E1~Ð/¤I:tÎ9ÿM(mMÙáàÌ7'Õ«­%­\x0002çÄ
#o\Mêºì)Ê9ê9\x001aTö|"OªxEªx\x0017©VÃoRÓ9H®¢9\x001aN¥ËÏzÊW>_ù\x000e¯ éÀ ²þÈ¥}ÔH7x¹ÂèkWÂÇ\x000eÒ,a	AwÒú×\x0004ü8e­ólRuäÄóIÕsövJ|[{ïó^ªìúJ\x0011á\x000b\x0012õ}ûëíÝío¿ÝlNv_n?Ý>\x001c´j<Pz±M:År \x000e¤LêÔwÛÍÛïOÏNß¾ÝnN¯Nß^¾)JLÑ\x0013|¸h·ÔY\x001dG¬Â)KNÙÉýMAÅ\x0007\x001b0Uä®MíªäT]\x0016U\x001cÂ-)Ë\x0011ç®êZ\x000b\x0002»0u©»0é!ÓÎ)ªr¬SÓÅhJFÓÉõtLÊÉ\x0003Nz\x0012Ö­aK[rÚ.Î¡KWØò
­t¢\x001c½\x0017õQºÒuQª#2&;¢yIw%=N2ëô%¤ï²\x0000\x000f\(¨²Ì\x001fw3¼ÑDN\,äÅ \x0007ÜhJyDÙû:7Æ²\x0008É«a6\x001b×;Pß\x0016Ä±\x0001Qª×À©r7P>Ö\x001féóíô¤(\x00152p¡¡¥ÐY\x0012P¦\x0017\x001aïò\x001cÕcA´>»\x0016ÂÉ²»¯Î´D\x0018Bîîð´ùáf÷ù ¤
\x0017:ÚÛyì\x001c\x001bPF\x0016î=ÏÎèôÃöøüe@Y\x0002Êv@qé¥ÌRc$Ëµx®¼<\x00170\x000cË²qøâ\x001b^µ0ysÿûÍçÍÕÍÃÃíÍÁÑªicîº£2@ïðl\N4¼}½¹ø·íùæj{yyº=0à;9\x0003®æ¸ÎR¶8¤Ú£\x001a£"Iõ0í§\x001aÃ4ÒVÆÕ_»q÷0À-ßÃÚp=5Ki©],ô! \¾?äÜËqê\x0016=#ÛxHÏ8kÅ34Z7ü£å:¸²º\öÎÝàù1ÑÃ]Jl°\x001aÌ?Õ§WÖ¼²7e#GÞ°Ö\x0018*8FöZ\x0005+ðÚ¾¦×¾°Ä4V4KÒ\x000c_SEóX\x0012¸wLD^Ç:y¦V@^(VP"pn^\x0001W\x000c]\x0018\x0000\x0017>váZ¯©]ä.µS	¼ x[Å¼e6Gäu½[§#\x0002¼c1¥¦À\x001f\x001b÷ïÅUÕl}¸c+Åà{y
¦\x0003/m\x0015¯â\x001c$«fd½³!ì\x0015K\x0008±*RÉât
ÿ­UÌ\x001b¼íp¨%÷»ëôgQ$®7ÐcE\x00119¬³\x00001åëM\x001b>:Ú\x0006WVêÜ\x0005¢ð×_oo\x000e\x001f\x001fWx|ÔÖ@JjNïþbJ'\x0010¾Ú¿|º=tÆERQNRGF\x0019ªgð6£ú)MÔFVY²Ê>Ö`KÖæ`àªèñ»)¡FTU¢ªN³zj\x001e¤)B\x0004fÍeþzªÌ¿U¬º\x0015û4\x0013T8à¡I/JÖCY ¦\x00045] ÐÍ\x0005·\x0004\x001d¶\x0004l/\x001eË£Q'u$\x001bYmÉjû\x001a\\x0014ªd(£RþG°+Ï;rBa¤\x0011Õ¨®ÛYahK"NUCÏAûÔu¢ú\x0012ÕwZQÛ\x0008¥,)°ú<\x0003¸ª$ocåõ\x001eÐ¹	èÜãBA\x0017Y°F&Ú\x0016e#låZy§o
§\x0000¼ÝÄ§6\x000cq1z\x001e`ÚØ°Ãâ\x001eK#<Êz¢GÀJíØ³Îv}¬CíXÜ³Ø×ë]]5\x0005\ç\x0014ø\x0013H¹©l
\x001f{P´ý+ *¦®¢N:\x000c\x001aÈì_¶ö\x0003¦Ï\x0011°\x0017¤:zá¢¬´ØÉ\\x001a3%IÔH+jÚ¾\x0013!Hr¦G#\x0011ónÒ#\x001cDfv²E\x0013me	§WÖ7\x0013Â¹\x001f_5u¹AAÁ"Ðé^c"úH\x0010ÛÅ¥+LÕsVuÎÙàðIP\x0006ö1­ý¨7
\x0004fÖ\x0005ÆU³À¸ÎY \x001dêË0¥sF\x0003G=ji'ux\x001baU
Ûw7 ys6¸\x0003zJX\x000c\x0012îæ|B¤ÖÕ´}§C©³\x00089ÎkÁðá\x0013TÓ×8\x0018ØÚ\x001dØ^w <¬¬DËPæ2ü\x001fM\x0004µÊùÐÖ§\x0018ÛyQD·\x0005<ÕÙdÚ(w<-¶®i'ò\x0005\x0013j½Àlï\x0002S\x000es¯×B<\x0015ÐIó¬\x0019na]=\x000b\ç,PÎB©1ÐBÅI»\x0002×ä\x000f7
\x000e\x0018s]dàs\x000f«æ\x001cÃZáÊ( Å9=5b\x000b$	ö^nYÎÝèJãúö\x0005
Ê\x0012iÎÆ¥KÅ7áò W¸s1:yÎmìOÂÕ#ëê^ë
éÃq2Ð»³ÅÞ0\x0019ÖpT\x0011)"\x00173#z¢\x0007´XÂ\x0007r\x0008Ê¬BÌÇÄ¼8ßËµ·ùªk,nëÂHüÇÇ\x0018Ó.á.d\x000eÝªbVx|\x001aÊ,\x001dK\x000cu\x001foÆ6#N§yØ~\x001dî\x0018JR\x0000ÌbÇXà\x001b¥¡@\x000bðÏ{{·ûHÙº/'yð<ucJ$f¡ä÷}-FÕdoÏOæ%y\x0010(ùD3\x001fes\x0001\x001efsés\x0002ìHÓ¥\x001dOx²\x0015iê½\x0005	ºÜ!\x001fU
ja^0ßá±U%ê\x0018[Oé®\x001cK/¡·;¥Q\x001aT»ñtÉ§ÇI.\x0001R3\x0015\x001a/7^^Ï|¦Oäæe>g5s¡´L¾Ï|¶O¦W\x0015JÁÅ}[Zº|T\x0017ÒçJ<×gÉaÃË°Bóe-3ÍGBÊ\x001dÓ¯È\x0016\x0013p×:Â²ø\x0012NZ(«Yø¡FüÐ()
O¥^\x000f5¢Z:Ê¦J\x0011\x000b\x0005¾øZ\x0006«)¸(öW7\x000f»/Ù¤Ì{Io\x001cÒAynýª÷ò«íõåñÕË\ªäRM\ìÄ¨\x001dÕ ±¡É¶âûL6\x0017ËX¦\x0005\x000b\x001aP¼§Qöln¤%ß·çÎår%k2\x0017k,%Ìz\x000cÇIG¹üRíÛkgr
ç\x001c3Ïç	\x001bpÂa\x001a«_d\x0016Ø\x001dÿ\x001b
V.Ïd´ayÎ²"-V\x001f+\x0016çÊ]ÇED\x0015Þ­Ê¡Cº>TTõm_6\x0017w·¿½y8\x0008§EzpSJ¡b7´:Q¤\x000bb¦$9¯6\x0017g§ïO·\x0007ì¾bô\x001dáÿI¥Á\x0014µ³=£4\x0013Sb\x001bó1¹±%&¯jZçr*\x000f·ûÈ)=¬áÈ©$qNiî6`ZSaZÓi(¥\x0018\\R
\x0006U\x0001s¢µ\x0001Óñ
Óñ\x000eLí!8a*\x00140FLÍ\x0017ONîëQ÷=£n)\x0007S\x000f\x0018ÞáÒ\x000enñ°\x000bYqÂÇön1Õ\x0019ÆRîeXë\x000eª
nÀT5¦êÄLB3í~óÌ¹xØ«Ê:õTnåT\x001añ*íØQÔm¡ÃËDYp\x0003æð\x001a1+¹Ù\x001e# qÊ\x0011¸Ø\x001d-vÍ&
[8eÍ);Ýã°\x001bòaØIUGOÉ+´pÖÃnz=eÉy::\x001c: Ð¸ëÅÞSØz\x0019ÙÎeàJ¢u´§Êö\ìdQÒ\x00188ác\x0017§§qwxo\x0001NR¥3Sê¬
ÜU¶ÂÜqw´Þ\x000cGIEK4O\x001cvÎ&
\x0003Z0EmNÑeN~¡Ù6\\x0008ÑääÍò=SÕÎSu9OçST1\x001a3ÕXóxL_ÍUÎÓ²\x000eç©T\x001eth,¬©,ZS³qÇ>TÝþÑ/UÊ\x000fsiM\x0016ý1(ñ§\x001c¶¬\x000f¬+lïF}d§ß5sÂ\x001b\x001c}\x000fvÆqZKV.ßáë\x000eséÈÔú'ÂÙ¸&Ãr;)SË¹xZNé'pZvù´¼Üß\x000b_£ê1ê\x001fî£ÂA~dTß3üp´W>\x001fí¡£½ÍGûå}©\x001fÆ3õÃW9Sý\x0014ÚN
FÕ.\x001bi2j©Ë\x000føáú>\x001aÓ5þ 'mòÞ!ª\x0012ù¦<¡<\x000fU\x001b\x0014»~øß*6ýËûO»ðo¯n\x001f¡HéúæóîþP\x000euQá¶\x0017É\x0002¿r¿úõåÅc>½B¥ëíùñÅÐC}(@\x0017å¡­Ð\x0019º(eò9ÕÉ!\x0004µ×Ä=ÐÚÐÚöCC(A³\x001c\x0012\x0019zâ²Ò\x0003í+h¿\x0000\x001aº¤áÅÚ¸TÛ
;\x0004=Wùý=ö1OÄ$#°\x0018D\x0005â|.T\x0005Zu8~§\x0008\x0013\x001a\x0005aµÃL:Íö_±;¬\T`Fè"Ú
­{ãxñò©D0Ã|Uî¿n÷0\x0017]ß¹ÐCh64Sx\x001c× 4\x001cGå´Íñý£=Ð¶\x001dvÁì\x0010Ôâ\x000c:xÐM\\x001bé3õÞÍ¹\x001a\x001e6Jw§D?µùH!,Nð'SýM\x0000z µ® µîö\x001eRÓ>(0I\x001bU\x0010_kÈÚIË\x0005^:ðå\x00002(æ$÷a¹Ï¶^mZ+Qù\x000føØM\x001dö\x0016\x0007yÉI^Ú2.ó\x000cÙ{ï¡6Õ.®Lÿ6\x001eøPNAY¬O;¢µ\x0016ã¸ãu?µ\x0011\x000bÝÔ2\x0007 '¶LQ\x001d'\x0004îíZ\x0013Ä¨\x001aZ-¶\x000eÃ5?EN¢¤+\x001fíZ³#,½*2«±LôLmNnÄ¡ü\x001fLmß/ÞÄ.ÇIy²LÊ{sûøxQ)a(Ý\x0003Þ\x0015æli\x0007èÄÇÚ7§××3¨DI%\x001a¨¸\x001f\x0004µ|ÎîPz\x0010UÛ\x0012ð\x0002\x0018ÛJ¸¬æ\x0019\x0006ôõÓÍãaª°è\x0005ÚÊqÒç\x0014\x0014ÝÓlüÝ\x0016ðõ»íõËT¢¤\x0012
T\àf%A	9=o\x0006÷µÇÌs1¿ÙP²ó¡$4Fé¾°~³©\x0018¥\x0002²qA[\x000b*©TË\x0000ªaZÉ#Ê¯3yüÆ[ t	¥[Lå¨Ø'_IÊdÊTc\x0016*SR6SQdës¢é\x0006Æ«ï\x0011ÔD§ßq
¢pYas8µ\x000cwZÖ$bd'eÇÕq-vªRÝ_ ÙÂ¹æÂBCçTv£"ç0=++\x0003\x0017\x000eâuð!|Q\x0006\x001fRrø·÷\x000f?Ý\x001enf\x0006M\x0001©9iTÍÁx£X2æ@\x001f»o/._\x001ejgF º\x0002Õ\x001d Â\x0008\x0012ñð\x001cµQT¸Ù\x0006ò\x001aÒÎ\x00065\x0015è¸_åWdQWNÏ²(\x0008iR\x001a\x0004½ô\x0008*èÅ\x0011z\x000e¬\x0000ê+Pß5ô±KAlKÂ\x001faè'Äé@È\x0007ªqoÚY JSç8/\x0004fñrnI"]ùÉV#- ¼\x0002\x001d÷®\x0005Ê$%\x0005\x0004*\x0011Täj\x0001¶EE\x0005:îI<\x0007s\x000eÊ¹\x0011tó\x0014glH:fS¢ó- \x001fU=~CÞ;
ýà8¥\x0019\x000bsû8+7ªzÜ(\x000fû\x0011©P¾\x000c¶BçþR>P[ÛÏ\x001bù¡fDkËæQ\x0013lõ
 Rÿøq´5}ìsP¨åR^<äÓÆ¤\x000eµÕ?ôÃ;\x000e\x000eþ®\x001dÙ\x0001\x0014\x001f±\x0017\x0012ÕâªpZc\x0013-J
Ð¨\x001f:ª-\x0006½ãñ7\x001d4]¥Í¬klO#»Ê.»0C\x0015]\x0000-=)pÇWÝóÕÈ®ªË®\x000cÚôQ\x0011\x0002=9³×¹XÂªb§]&è¥ú\x0006f§~Û}ùr\x0013\x001f\x001d/oþ~ûpóÒû¨Á£³°a\x001bÀMJhÌáh]OÓ7o¯®¶ñÕñrûþâôr{ðÕQ_\x001dU|ul\x0007u\x0002C%\x0002\x001a\x0002§¼ö\x0000\x0012\x0012ÒBQ]RPÃòur*]rÂ\x001eõrÓ|uLÄÂå!õAâ?a¹ÿ÷üçñ§Ï?Ýß\x001dnÉ\x000b}\x0008dZðÂFYß$\x001aâ%uîé\x0002«}süf{þêâìg|\x0008¼\x0000$|l§\x0014\x001eµDXì\x0006«ª\x001d\x0015ÛûQcÖvÆA-2rù\x00152\x0016·:`îkb\x000cÛE\x001d9gUKÞ>ÝÝ\x001e.ÏsPÁ\x0010#ß\{*2Ú­\x0014Sí¡ß\¼;;=$åx¶Ä³xRSA1áisd¢\x000cfÜ©¯\x0010@\x000f|cýó\x0001yN\x0005`ÊA\x001eC*ñ"åh344\x001fPV²\x00150\|1©1|Â<{(&Ä\x000bj\x00136\x001fPWº\x0015PrÀ'¨\x0008Íe¼t®¢sÍtSQ\x0003ªªoÿc~\x0003 ¯\x0000}ó
QX_\x001b& ;B\x0005*K2
FMöwÉgë\x0005ÜºÃVLyTáÌ¢Z öK\x001eÆ¨ý\x000f°³\x0001¥e\x0001-k&\x0014ÙÁÝ\x0008tÑv\x0018âÖtpB
IÚú\x0015+|\x0001¯XÇww71X}õ¸ûéæ0\x001aGï,D
,éc[G¤®\x0006ÇggÛ\x0018®¾º>~µ¶\x001c¢
e'\x0006U'-l AwWfÓÂâØtÇR£WÓ\x0011Ü!£ñBº\x0019\x0006Á\x00064\x001eîQ\x001a¯Á» Ý¬ÃT\x0005\x0005ÛÚ\x0002»qWÓ¹6:Á4&R¸eª:\x000f£jhÉ\x0006íÐ\x0015m0\x000e
[[l\x0017\x001c^Ê\x0003V»æ\x0001¶#m\x00105~ i£+: \x0000]ìÐB\x0007YJ)¬gL\x0015ÕÁvaDÎ÷¬tzü\x0010®\x0007Õø(Äÿùfsrÿðùöã¯\x0007\x00195¨o$AS\x0010·¦0¾ÆÂ6É÷êF\x0019þóíæäâòü48\x0017I\x0005¯Hy\x000fª4Á«ðt¥§6p$Eµ'	M§f°î_Ê\x0004ª*PÕeSx¶K²BÁ°Ä\x0014bBpÜÛ}²ÍVÕUuUulpÊ1TÇ,Hò\x0002Zv¬2\x0005\x0006¹`\x001dÔ[`àW\QÜ
\x001eDÃ.­w¡÷ëï6Ípµ(IácßÂbØWh¯@¦,­,\x0012°\x0014ëL\x0002)LI\x001b\x001bþöÐZ\x0005Â\x0006*4©ï*=nÖHkø(K&|1d\x0014;êû^º\x001dx¬Æ\x000cþÔd\x0001SA\x001bÕ¸æ$ 6ï·¯Þ\x001d8ÙYÓÁtÅ\x001cÝo÷O»Ï'¦
g\x001fç1+èêW(|1õ<³áäøíÅ»ãó\x0003V#.Qr&.1ÄÁ\x0019\x001cP<+?~>OãÉXûW	1ÉI¶01J½Y<Røò<af&.¡t#Fõ\x0013(¢&&AÚÄ3üle°\x0014uxvPHºI¸ÜXS´Ë\¾CÈ2rAwgJä¡²{Ö^æÒ\n!áHW«^\íÂ\x0015éÅà¿Ma,a¹ÍI\x0014\x001ald8wM´E¿Ú\\x001d;Ò¡È*"ZW"Z×ÎèÝ\x0011
ÛÂ\x001aÅµ$lË&+Íf"\x0016qÕhE¦:\x0018)Í^\x0018mQÛ	2Ûèl '\x001aÏÍ¢LÂ6ºhï\x0019\x000e1ÕóyRíz{{óððÂÑÐDÙ3:i¤È\x001eÎY4\x001då\x0014(jw½=Ý^^\x001e¨ÂÃKXÏ»`Ï=§½Âñ\x001c[\x0018hÕ±\x001cVÈ
VÈNZÆ0¢\x0019»Î\x0005Tç<iB\x00197UdÜ*E
\x001f{P#§\x0014£s©m¦¸0ÆùªD\x0013­3Õu¦oÎK\x0016tkKO©Q¾4ÒæÞ'á¤8õD=ñ¡FÄCÍÉýÓÃÍñÝÇÍéa7/\x0004\x0006\x0014áVM\x0001E®
% úQÂæÉÅ»Ë«ÍñÙ·ÛËëðÏþ¸ûi÷å1\x0018þ2f\x0013%hb\x0003M\x0016Ìà\x000f¿\x0011µN`b¼Éðq\x001aR#,Ùd£Ý\x0018ÖK\x001f\x001c'eOkAù'v\GÞÈ¦J6Õf·p%%6ÐyÃ1¥\x0017½à~Æ¯\x0014l®dsmv\x000bÛµ¤\x0017\x0014\x000bºÑnäo¤ZÄ6ÈãÅµÀÚà§§P\x000f;L©V,\x001bn\x001c]o«\x0016\x0003o[
 0LrÎS\x001f\x001dÛV\x001a6j\x0018ß
g*8Ó\x0006\x0017¤/l}\x0016(u9\x0019Ý\x0013ñ\x001aáª)Ç\x001bçÑðÐà4Ê\x0013£µêÆ¹bmp¢s¢mÎA\x0019[ûÀn¼BÓýMÛîõ Ç{ÎE+átxrÿéÃîñq÷ùñËfûysüó\x000b¯\x0012áú«u\x0016gÄ¿\
yö<\x001c_mN.Þ|{|}}|~}µÙo¿;\x0019YÈ¢\x001fÙPã)éÂQ\x001c\x001bG]4Ìe4|5fY2Ë~æà\x0013\x0019¥ó8ø"5M÷\x0015ut2ëY/\x001aÖç\x000fApÏsÆ\x0018_ÙÌ¶Y\x0019Ò\x001a\x0005Ijê+\x0000Á5\x001b{nÝ½Ì¾döýÌáyÎ«Ì¬rÉÝX\x0002\x00013¯ÝÆ\x0002¿a\x0019ôI¡r\x0007BúÞð¬íÎ/B*¯Â1$\x0001ªQZñÉÃÓÍ]ø÷ßv\x000f»ÍëÝï/hEëpmO]Îuø§c1\x0012\x0003çúYÈ\x000fÎï\x0008y\x0012~ÇYø÷·Ç³íæõñ¿\x001dÏø\x0001ºú\x0001ã\x0004îæ\x001f @ì:\x001d áá\x0011[H·{x\x0019xÎ°ä\x0007\x000c`à\x0007qíAû\x000fpÔ©[9\x0008
§S¶pøÅÊü¶â\x001f'¦·óÛX8Cü\x001aww;\x000cx~\x0003\ò\x0003æð\x0003Ü¸T¡ý\x0007hNZ9Ncp	,\x0000{^	²à\x0007ðá±\x0003~\x0000\x0017ã\x0012«Ö_ ¡cJ\x0013Öáî^i \x0001¹Á!p~OéÅ_ Yõ\x000bô¸R¨y\x000c$DÓ\x0010\x000fÛ\x0016é¯;ÌÊ×ô³æ/P®ú\x0005ðqá/\x0010Á\x000f¥à].
S \x0007U\x000fô8ípá/°¶òCðqá/àF¡FF,¡dl
ß£YÝÿ\x000bÊ\x0016`q\x0016ÕÊÐ\x000bÁ`æ]¸lS»=ãh%?ë¾¹ð\x0017\x0008ÃF+yé4^3¡¹Õ\x001crÖèuã6EÝ?!\x001cdëÔ\x0015è \x0019SWÞßßÂë§OOwwÏ`gf{
;	KJ\x0017\x000c½\x001cËQ\x001dàûÓíæ¤z\x001d2Ä§O\x0019âEÂ&xê å£}\x0011ysÿy÷ñ°¼ºÀÆA\x001d|f\x0014%2Y5-rÓ®`8Þ\\x001f:Ö~j>Äqs¶\x0004;÷
FöÔ\x001fÕPeSÕ7­ÔW¶µrÝÔÐG
\x0013Q!lmµ§àç8iì õ\x000b\x0004\x001aÛ\x0016àðq\x0001¸6¤¯
)©¤ÝåºaÃe¹_\x0002·Õ<©²-[ÁA0Íy\x001fN	ZÍi7UKÚÁ­\x000báÀ\x001dÅÅ»¹¡
ÖS\x0008ÉbZ\x001eît\x0001W{\x000e\x0008½äÆVäÆ. W
\x000eÅé|/¸¤\x001b\x0016§M)8iuø¦¥	\x0017¸ÚàlÙLat,\x000e>½ÁTÑdñ0V°¸\x0011£{­\x0011{îµïwwwÿúgÊX¼yx¸}\x000c§wQ¨@\x0014øäë\x0019ä´À.ª¤wis¨fúýÁ¸½¼<Ý^¾Hï*z·>ì\x0018¢\x0017Ê£\x0014\x001f\x0003IlÌ¹²/«=ðEÅ
ÀógB
ôV(\x0008?Ç1nR0$+\x0015HÉ÷\\x0007\x0017Ð\x000f\x0015öþY}+=¤§\x0013î­\x0014ät\x000føSZù]øb¨»\x0007|ñ¬ð¾\x0015ßr<>

i\x000fé\x0004L]ò¤´SÝqúèëy/N|'$æ	\x00033iÙJÒ`á¸&¾,òø ¢ÍÆ÷fã3T\x0012á?"9`|Mé|Í/\x0007ùÌHoÇaVãçp±°Ð>3-\©ñ\x0008)Õ~\x0001¼^ú!¡?Ò»q °yê\x0004d\x001e_¦ª::,µ/~ÐO_h<ÆíJï}­ô&Ï\x001c+\x001d8 HO\x0015ÏÄÓ\x0016Ò+^o¶Kç}Øm\x0015öç>õ6Âz|ÚM¥uákîK|ø¸ÐørÇa
ð´lÁ\x0019%|\x0003/\x0005+â«jæëg!ðæÏÒÔqÂ¦S^Roy½_µ\x0017^W\x001e\x001f>.·xm\x00150\x000c6½«Ijõ#Í¸\x001cb\x0019¾©=¾YêñáÅ\x0001õ\x0019@_\x0010_¥rÔTZ­/ª£\x001a|\8ó
æU\x000b¯yÞo!K8áûý
ÄøW3\x001f>.Ü±\x0004\x0014Á	]ÈÃ	\x000e×­]ÕåÛÚåÛå._S»[¦P\x0006®(4ó­[õ´\x0000e\x0015þRÛÿÉøµÓ´¦ÕôÎÌ|,'ø\x001c_L_(mÄÿÀøq¥K¾
_|\x0013?óêæï7á6~úùçý3\x0000?\x001d$¹¨»\x001d|zòÐ)\x0002 sY\x0011¿Ú¾ß+øéùwÛøn\x0006£\x001e1ê¯QI85z\x0019Ã\x0003>~óö!LoÝøÀ!\x0007!ý;=\x000f\x00081ê=|\x0019\x0006}{ùB$=°ù*-ï[¨àhnÌ¢Ýl¿üöpû~§ÐPö\x00193¿ÃBít9V)9nrg·Wo/O¯\x000fé\x0014\x001bÀt\x000c\x000b\x0011ÙåýÇ_7\x0017O7_\x000eÒi!\x001dV\x0002ÆTZ²T\x0012íÕ¨[D»¼8ù~sñn{5
\x0018LÚ\x000cí¤ùF¢ *¾¡üëv·a}ÿ×áddP\x0012%
[\x0008\x0012
/¹²GìþÞÒéñdûæø4¬ëKªÎIUEªzI\x0015×ÔMÜ?9ü')ÑQ\x001a6 j9Ê\x000e_å'ÙCÎ\Ö\x000b«keÖs\x000föÍU2ÜïI\x0011IÅúè\x001e\x0005>É[ê·:Õ·\x0012ÇÝ	£Å
ÒâÒ]\x0016Jï\x0010ÙMËÚ®^bäy¹Æqº\x0002\x001aOÙZRM[9¤0³"¦4.03Åkb9ähfT \x000ff(XÁ¬Ü¿ßßÿÃÿ\x0003ç2ÌàëÝßo\x001e¾Ðrûîþócðc°Òx.Uîëû§ÇÇ/ùòôð³û§ß"­°ÅÄ=#¼¥L!h0¥ÓyÛÔàúâÝååöúz{õ«w9»x÷öëËã÷ÛË+Zß]_\x0007\x001f7QµP¥!\x0016\x0005\x0008}p#¹H/óÐJ\x0018å2\x0002¹_üéîééæ¡°9äÄíª¸ã\x001fnÿ\x0016¾=¿øiæ\x000fàán\x0007¹ð\x0003´1áp\x00173XØÄmÊ°ÙÇ\x000f©rÇU¢Üñw§ÿ;|{~qùjÎÏ\x0008«F®õ3llP\x0019\x0012ñw8I3ÈDíÈ?æw\x0004ç¢×ú\x001dÐÚ¦ßálÃ\x0008¿C{¿Ãzýý`!»Òï\x0000Y\x000fÖ\x0005T¾Æ\x0003]øï`¸ÛX ùÇüà6ýZ¿"lª"-\x000e\x0015\x000eÂ¦_!ñQ6\x001c\x0002õ\x001f¶: ²Å×Zå¥¦sðC¸OºWðC0\x0014Å\x001dÓSnªóÀÿèpÖÁ/Àke!Ã§ÍÉ¯»ÇÝÓ\W\x000bâ5ñ'p¥RF\x0002tv¸2´1Ss*K\x001b¾Û||½=~÷2¶(±Å\x0012lxí\x0004hhM)\x0010\x001a\x000f\ÇëòjÐ²Ë c\x0014\x001a;v2a)Yñ0¶*¹ÕÂ9\x00029\x0014hïøF\x0018' {¯in]bëEæ¶±D\x0008ÍÍ9"¬ÍæV+rÛ,áf6å\x0000·L\x000fÊ\x0001\x001bå2\x00025r*=Ô¶¤¶K¨¡f\x001f\x0017%\x0014Æâ$¥¸c³ìÕ¸]ÉíþçpûÛ/Ý<æ\x001bÆYÂ!9+ÍnF[ë\x0015W%gÕÃ\x0016\x0019ÜåeÉ}jí\x0010¯%ÙÞ+bW¾/rÞÊD©\x0011Àö<in\x0013$§;aQ\x0019h!¸üùÿ>þí\x0001cD124Ü¤6oo\x001ew\x000f7÷s¹Px\tTÄ\x0015%VÆ*Ê\x0017¯Qï6o·×ÇÛ\x0019Ð<Þ¡\x0018ÿ\x001fF
Â\x0005ñÿQÔpeü\x000f ¾ýÛ½7òÇp¯\x0007©ÚôçÛÛ»Ù¨Ð¤\x00106ÖêM¬?Ã¶¦~äa§ò\x001boOO//\x000fÐý´\x0013¿þ\x0015\x0002\\x001cÊ"â\x001fgÿý\x001fÿùýÍÃ§Ýyx\x0006z\x0015á9\x000fMv\x0002òÒÐ4U\x0005íã;Û|¿½|s<!º\x0002Ñ\x0015ûïwü7<dDùåÝçû_nfÂYaM\x000c·ÃE\x0005ln\\x001bÜ+r]'Çá>òú]>	'Ýà_ÍtáÈz(né\x0014N(¢K²\x000bñ35ã)\x001d\x0013ä\x0003\x001e´ÝÅÛªCõeî~Àbº0¬²ghÃñE¥³¹¶<å`Åà%nK)V½\x000eR°mÏÐÂãNÚ4¡Ï²K6Ì;Üì<Ì\x000ex/.\x000bxø&þÑn½XA\x0019§¶)Ô\x000f7xZµaa¬0¸\x0002bYñV¾°à£+Ø\x000f^PðÆÅª0÷¦^\x0003	\x001cÿhÆ\x000b3N¥Ha"Ì\x001e\x001bÝÁ\\x0001\x000fniñf<h$ëYã\x0004\x001erT¢î$ú5áiÀë\x0019\Îb6
X/\x001c\x00151è$\x000cá±å|
VXü£Ïx§£0\x0013ð\x0005 ÷Pl\x001b%R×Î>:hêTÅ±ào²\x0014j\x0016dúá&>qÏ¢UI0ÐÆí.E²¬Ç·Ðpæp±ê¨\x0015~Ø\x001eONä¢$\x0017KÈ]XäøL#%\x0003\x0005\x0005§\x000cN÷Ë\x0012\.2¹Ôä#ï®m~\x001e0 ä¶"¹*ÉÕ²Ébc\x001fÄH\x001aÏ0Y°;ë©ÓZ\x0017¹.Éõ"rHüRHÎ18dÍ\x0000®V\x00057%¸Y6Yb×ë\x0004î$Î\x0015Co\x0017ñým=p[Û¥\x0016W\x0008îc§÷drÚ-«®OW»ÅsÅ#¹Hzf<\x000bS\x000f-=ä¾$÷\bz¥£õéÑæB3÷nMçèVÚØ"£ó\x001c\x0013\x001e%½\x0002:uóà6)ç¬^ï ¶PçY¬)Ïî>Ï\x0017áh
>ùÀØ^m¡|Ñ\x001e
\x0002e¦:¥Ë\x000e .îj\x0007åË¶Phk'\x000bOÁgê?0W¦N]àÕ\x0006Ê\x0017í î¡W\x001b(_¶¢83¦Å`àÜæ^0ºXÓ+òj'â¶¢Ø\:M\x0017	n\x0006-å\x0005*Wõ-CçË<ºÕGi}Bî§A£sN3]®:_Då\x0015Å2¯\x0008jW\x001eó-#z¶¹´+Ú<üãêé²È»Xç$f!åw[Ãò"5z*ºÑîk÷â\x0017ù\x0017\x001b.
SÀJ	ëÀ.È§[½âuN¸ÊÁÀÇ%ìáb/qBjcì3b\x000eÊõí£©Gl±~X´
ÚJ¡a\x000bÃä;I¯ýá(³â¬	¦NÝxKÛï\x0016à\x001bÁi¹*h	ðUø\x0005\x0014rd«úHQã\x0007ã/¡\x000f.\x0006$j7ôÊhI\x0017*xøÉWÝ\x0016úîöçùpCí6ßî¾<Þþ43G\x0013D²\x0015O)ÇaJM¡]%§\x000egÇo¯®O_m'\x0003D\x00190\x001cõáÁÈ÷\x0010*GyfP&ñ5YBK7ù"3\x0000NYðo\x001f¢>\x000cø¹øG¡<qqwû÷Û6\x0007qÔèÂ\x0011*Ùï\x0014Cp¦Åd¬m\x0010¡¸8;}º½\x000eÿCý¿ß\x001f.²t©Ñ(t~z¸ùe÷0×¸1¶Ê1Ü&¢Sz\x000eÇVÝÜHu(5:K¿»Ü¾>¾,'BY2Q3\x000f­½ÌÚÑÉO8º7Ä×NM·ÊÉÓv'r\x0015j¡eÚ\x0004dÉð\x0002ÌÎØ(¹¶¼Û^f#éÑ\x0007Â\x000e\x00180	{ËaÁÉ
¤9=.Îìl\x000c\x0019ØYÓtN=.×d\x000e\x000c·ÙÀSndVr7A»\x0003§c}È\x0010\x0018Á%Ì6VEfÏÙSüROGé;¡Å7)¶°\x0004ÚÃ,ÐZRH'ø=ZfíE\x0008×~¾ÌÙq\x001dN\x0012tC÷xW4á\x0018j_¾quBÃ+ìÂeh\x0018eÈ22\x001e*Â
¥'3d{¡Ý7Qz~%g
\x0018=ù;NþÎÉCùì\x001dÐP-\x0016.DèËs A´\x000c¡ýÚÐÐ¶\x0008ZÇ&\x0018\x0011ÚR\x0014Ák\x001fä¡û\x001eh8Ü-ÜÂáÉåí\x0010³¾}.\x0006:ôJÖ	\x001dÖX¸\x0010A0\x0017`YÜÂs M_¾;Ãd\x0013Ë!(æi£×.¥\x0011Á\x0001ýåÀ{\x001f4e\x0014-NýRRp	»°"Ê!¦/«ÌL±lBÃ'=+Ix\x001bSÈì3ôäm¥\x0017:Ì\x000c¹pvÞ\x0018\x0002\x0008­óì\x0010k;iñ¨e³Cp\x001fõ\x0005bý\x001d<¯¤(¹Ë\x001a¶ÊIzçW¿ÿR]fÏÂ-öÛ_Â5vnÆ\x0003U\x0012áð\x001e«± *8@\x0014Fz¿SWîpýv{ùú]¸ÁN	àBZË¿?°\x000f¿Ç¤Ýx®\x0013@º9Ù}þ|ó8×¨,çû$¨rÒp&É;éÜÎ \x001bâùùv¢Â¿ä\x0013,îÑ¬\x000f\x000cca4HFãUÄpGd¡ät&é|òî¯·ÜB".8ôçÉ¯÷\x000f»¹µ¹\x0002: Ê¸ú
áôH84¢â\O>Í|q	$§àþúé×ßï?Æµ\x0013ì¦X¨â9w[G¯õR	\x000c ¬ø
áú)¼³AÈs\x000ebØ`á_íÂª¨ý\x001eÃÃ\x001e³æ Ú`;Yý8\x0007PýCë¿YÔ-NjÅg»ÍÛÝÓß\x0003Ën&¡	[\x0011¦¼J®ñÉ#ÜrT>²L>E9îwïÃ·Ç?ÿü7ùð%êXé\x0007ÿ\x0002Ä»ÝgìÍ>\x0007Q)\x0016ð\x0012¶i\x000fó\x001dÇNíS|w¿Þß}úë©÷Eìxq\x0016\x0005wnQæb+Ô¡¬v¸é\x000b|¿°N`Ú°\x0008w²\x0003áÑ÷Çgà\x0007_&â¢ñvD\x0004Ã?C¢	­¸´çÿ\x0019|¿/ÎE\x0001`½ø\x0007¬÷·¿|¾»NÖêà\x0002-æ
2)ÔtÚ:¬÷§¯Ï/\x000e¬§\x000fÿpê¶\x0008Ó\x0005Gýþöîn÷ËìC²ð\x0014¬gÐ\x0012YQv.åü³\x0003\x001bÉûÓ³³ã×Ó&\x001cð@dß°\x001e>mbßõXÀÄF\x000c¶èÌ7íj^\x0004üýËÝ£ø\x0010Ó¯c\Ñ\x0018'S/!\x0016ý¢OG\x0006­¨7¼LqN¾¤\x000cÖS`D\x000bØÂ\x0017ß\x001axü÷üçé]<¥<ÜßÎ}ªÝ/m \x000fM "\x0015KgÂµîÅýælsz\x0016Ïi'\x0017§ÓÕlô\x001bxõ\x001bø
¿Á8|©t\x001ct£-%+%ë3\x000bÚ\x0002«þ\x0008ÎªàlùHX\x0016ö(~3\x0014#w\x001c/Qa6ÉúÞ\x001faê\x001faVø\x0011LBþOú\x0015\x00022Öc}Sø\x0015bjÃèý\x0015JV¿b¤ÅÜ÷+\x0004UÓ	¥RÏÈ0\x0016\x0002µ³ÂÌPéý\x0015ÚW¿Bû5ÀÃð+$l ?\x0003ýIaÎ_!*\x0005|\aY¨¼(\x0014\x000e\x0004Çò`X\x0014+\x000f\x0010¦þ	+,
Î\x0005&õ;èòa0\x000eW5f¦utzªÇA­1\x000eÊEíEø\x0011RS²¹SxÔ
¿bRÍ¨ùWý§Ö\x0007Øh©\x000f~Ä÷÷¿Ý>îîf]==õ\x000b\x0018\x0010|´ÑTz\x0019îú/ÈÃ/øþÿ§îíru¹-Á©ì	ô\x0006\x0019d\x0004Iøé\Yö\x0015 ?\x001cYB£_}m\x0001²tëÈ*\x0014ê©§ÑoýÜÓ¨ÔHAFðK¦ÊL\x0012¬z((·}­E~Áø\x0015}þÑ_^}|\x001e¶èa\x001a=4ÖDBbÉ·ü«=ô0ÆÐû-z?ÞñÅr÷\x0006ê®EF¯á6\x001dNáÇ-x\x0005O\x0017
UðñYëíÚÖ@\x0000§#ó·ÀÓ\x0016<Íç±TßÀ\x001bú¨U?8Ì'¡\x000f[ôa\x0001z\x0013áv´¨¥\x0012-´ÂáÔÂ\x0018ú´E¦¥>rf©¢÷LÓ/\x001a§Ýý¡s}\x000f}JQx\x000b\x001e¨\x000c\x0006¢õ+qè«÷ß}ÿãÿ¸\x0006\x001eWÜ3öp1ò²{u*Aù/hûÚ¿õêõ§}ù"÷Ø!ßP2 çæ#W¡#J;ºKÜ}T¡S8&¾\x001dú[¹[÷¨Ø#\x0013è¸be]¤feK/í*ìîÁ
ÅØùs\x0006{\x0006\½\x001cã¨A·FÝc
\x0011è®î¦ »\x00144åo¦â8y\x0004}åµ{o¶Øùs\x001c»§$\x000e²GiÒä\\x0014\x00079ÐJàØÉºÇ)Yw6JCJà±º¢a\>Õgz<\x0016>\x0000=u*?' \x0003{cUÅð\x0006\x001aZ9rBö`\x0010p¡ÁþÚqîÚy7C¹s°bP\x001d\x001a\x0019&ç
\x000båúK§¹K·\x0014dn$d!yF\x001eå%\x001cz2÷¡[cLoLÍÔ#ÖJ\x0007d4É>âD:\x0013¢&p\x001bÖ:ðzðfÀM~
~¼²\x0007TÉuÝæßÇ)ð\x0014¼\x0004N±ðç¥ª!MòMC®¼ù¸\x00138%6\x001c³¢¸\x0003Î\x0008³\x0011XÂ\x0014<,\x000fÌÃÌ\x0013\x0005IÜG®\x0006£\¼´îXW¤¯ÂîvØÝ4vÍe ¬aðFSÊá°¥e\x0008<ìÀÃ\x000cx¤ ¼Í\x0005|¶Ûj÷ý°¥v\x0008»ßa÷SØ9¹!ªÆJµ\x000c8ã$Øãá°×\x0008vÜ	
Î	
z1PYÉ0µ@VÓÆgYã{Øí\x000eûWà1FÈ¦
¥;\x0018¢1êHâ!%Ã\x0010x·\x0003?ã¾{Ô
V;jõ\x0007BjÈ\x000f'\x001bGÓîÖiêÖ)j\x0017O¾uYÒÕLþ\x000f\x0004»?æ\x001eº\x000fÞíô»Ôï\x000e¥.+ÛrÈ\x0010¸Çãò\x0011ði\x0007>M÷Ù"©qªg¸±\.þ:e\x0008»Ýa\x001aÏd\x0012"5lX«ÄS\x0000lÆi¡äU[ðü=\x0001Þl*vf\x0008.\x0001H	ÀUÏÐJìØ'
ì\x0004vÎÎH \x0005édÌ\x0017Ôôñ¤s\x0007<í²b4\x0016óeXLò3>\x0008\x000b[þ³¡øîW§\x001dø)/ÞE_6ä²®IB\x0010@R,Á!ñÎ\x0000ø¸SqNQfóö¬É¥Tó\x001c9ÜsÐî}%rÜ!\x0019ËSÔVdF{²3oUÓØÃÚÇ\x0008x\x001b{ð6N\x0005OÉËpHütÏ\x0004Ø$\x001brh¶RÕÄG\x0005¿ßðG#¿Ú\x000e¿¤\x0005#?íËY×³1î°Ç9ìH
´ÖÅVðNìØ#àwAr\x000c\LQë\x001e*] MN{&²\x000e^ùZ\x0013ì OÅ}|Ù\x0011ÌTyÏ¯@±§5\x001bËí\x000b[ìü==»î\x0014¤ðQ¬l\x0019k\x0014|\
¶i\x0017<¥¹àÉ\x0018]\x0014n²\x0016ËÀ\x0010jù90\x0007Àï¤&ÍI
f1\x0007i<c7¾¾Ö@Ô¼É[µº\x0010ìgî©ï§ ðV-M\x0008Ë[
Vo\x001dâºÌ\x001eÿ=v±¬6¢\x0014)y=Fªà:4t<É3æ5v?öfÊ3@©d\x0017\x0003 ¶z\x0006¨®°¥ñÿë'øÿ5\x001fÃ\x0003¿Süá×Âÿß~ÿ¿M9Ä¤d\x001b;ó%\x0014Q>Ã!ùÒP¤\x0011Ä<h$û7Fb¸³¬D#Ê¼Qæ­ÖÞÿÛÜÿÛ©hª\x0010YWù!Í±zGsåJ\x001f\x0007ÓîþÙ½¹ë7\x0015oåì\x0003ðI³ff¡¯À×¿\x0017\x001f\x0013\x001fgÞ×É¾\x001bpè\x001f\x001dº\x000b«:ùßñ×7ßüðÈÿ6ñ\x0013\x0013¶ü\x0004l¥ä\x0007Pfeñ8\x0011\x0016Ûx*ù\x000f°\x001dQå·/O¼|ýîÛw×[úì¯\x0019átw(ûoÈ[íèéx\x0019¡R<}üêéWüðã\x000fiµ¥âdr
~ÄIüùÑJS\x001ffý/C©Þ+±D²ç|¸·ðSfñG£ÛÌH"sòA	Âd-~êñÓ$þPÚl
~È¦Xß²ËÅ\x0018OICïàßÔ6\x0019)mNáO$s3ùþQì/å¿*íý\x0005\x0012Ë{øC?Ìã÷õý2×çf/ú÷l\x000c¾íáÛIøh6scm`ühÄý´Lú·\x0014ÿf>ñcÄÿØÃÅ[\x0013êô6\x0012ä¥_ ñ\x001aOöçÏ9ø2ùËUÃº$0´\x000fþx/ð\x0010ø\x0018;ð1NçÔàÏ¯ Õe3JÎð\x000fç	Çà'ßÁï\x0018EGá\x000bzT®
2Òfá\x001f\x000bÀwÖná»{\x0000>$\x0013bYò­²\x00109eWÈ§Zj¸\x001ctßÁ¤âçKA\x000cLIÚ\à±ªècm\x000cìñOJ?9Îjêõ\x001b\x0011þ ÜTY®½þÐù
ü9\x0007?x\x0008 n.ðÙÝTøÇ¬-#ð½éàóç\x0014ü`¬²Ýa²Ò8J\x0001­êNwØ>ßöøí,~[V·AÛD²ô \x000fóHßÃzüvxâOJ¬£\x0019õ\x001bÂùr[øC§}øsîþ)6Ûks?:%ñi­ü`ÿ8{ÿIT¿TýÄ ÃT)­ÕþØ8\x001b6F\x0016zq£TÞQï\x001f¸\x001fn)þ>lÄÙ°1\x001a-\x0011%nqD¹ÿ\x0008ÿ¸¡t\x000cèñYü9V*YiÖ\x0012\x0017eë\x0005~ðKÝ~òßL~ÒoN&6ëIzÕB¡ªâ\x001f\x000fhÇð?úì
~tø\x0011.vd¹Ü?=/Åï{üs¾sÌÞ¸ò*åÿ¦,S\x000f¥O·µaoèo}¾)\x0006åp
-kËlU*ÿxXµ\x0018Ã:÷?çîy­\x0004¿/{ù\x0018?8ÿÀ\x0003å+ñÇ>xÁKä)l\x0012.v\x00106ÚÐZyr\x000c°TùGß9\x000fü9>yeúÉL\x0008±\x0002 4ÄIfiÎ3N{òç\x0014þ²h½jÈQdÕ>\x0010eÇ\x001eÓráOýý§ÉûgV7¡f*ÿ:\x000f\x001c\x001cúf½\x000e+íCøSì´'ÎáOI÷
²\x001d®Òï¢t9@þ?^©|ìcÿMM9\x001b|½\x0001;F_nÁ3÷@Å\x001fÎ·\x000eÞÃïvøç¬ovÒ.\x0007©±Ly@Ý\x0005\x0011\x000f§\x000eÇ\x000eàû\x0005Oþ\x0000Qxu²\x0000y)ºdCTæ\x001e¬ñ´Ã?i¾ G_R´9z©«\x000fê=ÛµæË2³Yw0üÚßH ]\x0001I\x000epÌ\x0001?r\x00000ý\x0013àï¹\x0003X'\x000b¸¸;O^pþ\x000fôÔ\x001f6=Á÷ýýó÷ô\x0003¨]\x001bü\x0003H×LVAºË\x0019èÏhè\x0000\x000eú\x0017à`ò\x00058S§)]YO&44\x0001p\x0011Ò!ïçÐ\x0001¼íU·*ÈópS¬\x0007HÈ»\ù\x0000T31\x0012¦Ï­§Þñ÷Ü\x0001\x0002^CW8\x0015mµÂÁë\x001bppHv7t\x0000ý\x0013æï©\x0003`v=I\x000f`õ\x0000\x000bõ\x0000vm\x000c`¶Í\x001bZ½æ?ÍÀÚòeÌv¹&\x0012Q;ã¹~½4\x0012Î¡ã£IcÉ·Á<)o\x000e-d³\x0014\x0013ýG5Çk\x0011|7û#¼hÀ¶x+ª5\x001c\x001e\x00080Ç´R£¼G\x001bÖò^æ¤(Z­q-ÒH5I» ?\x001cQ\x0018-õ'àrØÜ	È\x001aiÜNd6¢èrÆT2ÆKó¡ûÇÌ9ÑÙÇ\x001cyùW\x0015#£o9\x0019YÈ\x0001Ìb³æ\x0010èiGl]Ò­Aøó{¦º²­e&Â/E(Þ\x0004æÐX÷KóìÏ¯gê\x001c1l\x0011Ã0bo%\x0002!,
©í9Oß^\x0005ì¶Ý8`Ðz\x0017\x0010éà\x0012z;Wñú-^?\x0017BÛ \x0015Ý­\x001bÚ§x¼[æ.bÜ"ÆaÄî±¼ô3 \x0017*TO\x0015ÈUÀ´\x0005LãWLZ\x0003¦5\x001b¶Je\x0018\x000fÉPn\x0003\x000e[Àa\x0010°%^\x0005Wk><àÁýÌlIÞÌH³
qÜ"£W\x001cr£Þpòºá\x001eË\x0005ìùòÓ«Ó\x0016p\x001a	ÓÊd²"ÄZÊB|¹Øö¶cÜxØÈ+:+äÈ½°\x0005rk¢p¾Þ÷*äÎxØQëÁ\x001a%\x0017aYI÷1¦ãÛx;ÛaGGV\x0005½Ò\x0019Ëæ®@\x000e ]~xØ¤~\x001br§í°6\x000e¼úM¶"Y'cxQéBÏ\x0013ÔW\x0001wºÍ*76iA\x001e\x0012éúHÒpØ²^^\x0018:Ý\x0006£Ê
\x0013x^ëU\x0005t>{ïe-\x0019ÛU\x0016:íF£ê
F3Q\x001bÎ¬¤
\x0019q\x0014\x001a*Þm¸\x0006²õ\x001fÄ£ÏëTÊÿS¥é\x001fm\x000bï\x000f÷\x000fÝÜ²\x001fe\x001e±\x0017BÄÈ$\x0007õóíË5û¸J%ï¬\x0008*\x000cÞ**kxoVAP\x0007qlIL-ÁìR'\x001a.
;ÉD%ñWí\x0016NôZ`ó4v
³½[\x001f1l£+\x0001FKIC'Di<²h\x000f]obæØ}«5hâ	zi5åL%WË\x000btÍ¬\x001c\x001eÃ\x001dÅSî;î\x0013\x0013«5áµ8²
^IóÓ>dÇ¼Øöí(âìd RH%f[ÆF­\x001eW\x0002ÞÃ\x001c¡3'ü9zË\x0008jO\x0012ÏýWw¹lM.Ý*W.úÎ/~Ø1üþäÁªO­ñÕ­»æþýÅá÷GX\x0015\x0005c¤dÒèTe8w¸ãî.äØ@þ\x001c½ælµk5r¸68!µ±<g\x0017@k\\x001fHñ÷°n\x0006å®àþÊzÍ\x0008jNx\x0003æ\x001aÌÖw)ò=ÙÅ²·1{r²?\x0012
*U\x001c-7ACÆ°ýèÚ=ÃmmÍ\x000bDÊÁì2pmtÄóÊÑ5Ì\x000eúx¿\x001f¡$mäm\x0001
ùEVÐù\x0000.Úa/Ñe\x0004n\x0010tôÒf]Î¤{w qs'ï×8üÖïDÚ4\x001aMh
Og2h\x001eÈóÞþ i\x0007AóæG!ÉÍP\x0018MÒ\Yäqdß¥\x0017i\x001fEÚg[X#ØèC¢\x0015Z¯Ä+¼Ïr\x0011èÔ§ÊlÕ h²JCm]\x0012g½\x001apsH w\x00133A/\x001c\x0004ÃÂÁëáx;G'Òoï@Ù¨RXÍ·äL\x000fÚ
»Ð¼°¶¾BÏM5½Áé$Á|¼ºö.æê aÕá\x0019¼vFFFB\x00014ãl®Ls_\x0004\x001dR\x000f:\x000c{Ñ.\x001a«DpÐ,¸oü\x0011aQqÊ\x0006è2ü=*Ñ\x0014¹ïA;çÇÑÇÔ8cÃy\x0007×EÐ;\x001d\x001dÆu4/Üª{|¢³FJÜ>\x001aTÐtè3vå{ô¦yõÎ±2ÜúØXÀ£_åwØ[\x0016þ\x001e}N33}Â7id¼Ó8Þ¡~\x0015ô.\x0001=\x001e³dV©³!{xQnZ92£9d®»9º\x001e3cnÄübV¢uÊÝU7 ÞÉs\x001cg.]
á\x0018÷AWGÉ\x0007Hªî.4?_\x0004Ý'íÊ÷(hj\x0014¤Y¸YJ
h²º¿×@/\x0002½qy¶ÙSrÊëmÄùÏîbh\x0017½HÛ¥]²?
gûÉ\x0004+i\x00193
¹±g§¯]ô"\x0003v~t\x001a÷£¹Ç;èn>GÐö°}Õ¸|ÖkDÙUª¶ðÁßCÇ5Ï\x0010,¸\x001e3\x000cwñl\x0000£°ñº¦ú\x000cÑ«î ãÕAwAã\x000e4Î\x0017
¼©¦$«½òM\x0007¯T´çÓfWA§\x001dèa-Í¼³Q\x0017Ö$nE* ò8Üµs\x00132ôE·ò=xÏ1FÞÊ\x000b\x001b«Dû¶r\x0004W³Þ¿B\x0007Ã¯0:)­dÌÊÙµE[å×xÑÀ%\x000er\x001c
À1\x000b\x0015æË­\x0001¸¤\x000b%ÓùèÃEÌ	{ÌiTCs\x001bºv\ø\x0016Ï\x001f2Z\x0011g³J60uáJù\x001e\x0004MWÐ\x0012éêNÐV¹,ì¢ë ïA¿\x001f¢çò\x0004É>=CÂ\x0006jÚ\x001b\TEv©OûïAÐÉ9Î\x0014(¯,¼\x0004ÛV¤Eéhmn\x000f:
÷$å°D\x0001#Añ9¸\Í·¤£?ï¿\x0004Ú\x001bß5ÌïQÐÐ\x0016pXhj#7­^¸È¹ËÑe_¯78\üÎ\x000e¿\x0012¬Rö¢yî·`Ö®K·*þöy\x0002úßÿ\x001dzCÐ¦QÃâÑ Ô\x000c\x0003\x000fÕyYö»\x0015oö¶\x0017\x000fþþ·¿ißç£Ë÷(ho¤X\x0011r|Yç$r¸¥4÷\Á_ÿ'·ù{ô\x001dÑB'P¢q~Jz`\x000b\x001fß\x0012Ì}Ý¾|\x000fÞ³IQ*Y1F¶>F]\é`ñ"æd{ÌiØ\x001abÖwÕ½ËÖÐ(!y°¦¶kj\x0015><h1
èàGk\x0015Ùì·á\x001d¦º±/ÇàÚq\x0017Î§A¯ö;Ð£ÒmµÎm:\x0010\x001a\x000fàbE7Í\x001d¤Ûi«Ò\x000eÖÏZÝlîhÓÏ\x000c¯n(Í\x001dAú\x001b-¯7_æåí\x0017Oo\x0018»gâ¾\x0016	$!ä´"Nx¸âã~ÏàcFO»\x0006_\x0006¯IÊjwX²¼Î¦öÓÈzÁüEñ8çH÷\x0017^ò¦ãÂb¥òñï\x001aÅÄsÖË#\x0015?Á>!*6[ÁgrSS\x000bÜçu°"Ò¢q\x001b¶0{àÅêK¹¥(ko\x0003ÏeÕ5ÕÀÃ""åöp-À¿ÙKùAY	µþYÚ6
´&dë´o\x0013Ïgâ/Ïdõ3\x000c?M¶B\x0005
\x0018´ó#\x0004ßºçAçëèçMó\x001fºyÓÏßÿßß}÷ö2ù	­Û;ÎJÆOU\x00148ÄÓ¼Óç¯?ûêÃO?¸\x0000¶ i\x0018tà~%}\x0018Q©æó3Õ¾ \x000b±QSz\x0002¶\x0003]\x0019¹±©\x000e%\x000bË4W¡\x0007K)£¥ô&ì\x001c\x0013iQÙ\x0002ë\x0004*å A\x0013\x000c\x0017\ªë¸c;Nàö^ø\x001cb\x0002¨¢Í-\x0016NÃõó±Î«°½í`óç8ì¤\x0019Ê=@\x0015\x0013ÒncyQÍ2Ü\x000e;Ü\x000e'p\x0012!G®(I#\x000eð\x0016ÖÝ÷Å³àîX<oâF$éÿ§,'n~SÜç.ÕuÜý}ûûÎ¶JiËÓ\x000e'BPÕíýá\x001aÒû¸{uâgÔ	e¿»NÖÆ¬\x0008ã {XIæ¸N÷« \x0011:Ð\x0008\x0013 Ç]@t \x000c\x0011féV\x001dxÞ`q\x001d7õ¸'LN~uµ@íÝÈ)Ù£s\x001eË°{ÙÆ\x0019Ù&×H\x001arxÌY[5`Zæ\x0010-jþ\x001cF\x001d²d8Q$\x001aPRÊ#\x0015à²Ë¦Ð)@
\x0013
0\x0006Ôúb\x0012ËÊ÷t\x000cÛó¹Ê«°\x0003tv2ÀÌ÷ªá$'}jã!\x000f"©l§sâúË¸{·$L¸%ìhW)	¦\x0005¶FGBó»YfÞCJ\x001dìf¤Dyºóu'¶ôUJh9_÷2é}xÃÃ¸!$y¾ÊD*Ýé<&»\x000e\x001bzØ\x0013²À\x0016#IÜêRQK«HÏÎ\x000bda»þ¶ÝÌms·8¯9ÆIBçL»îuÎTtýu»ë¶ð\x000c¢L¢vQbÆ\x000c¹ïóÆ­Ë¸±3\x0011Ç
%¤\x001c¾dcà$2k\x0013Jmß\x001dn\x0015¿ûÁ\x001bXpw´wï;ø6|@SyW
¶ë>_ºp\x0015v2\x001bÌ¸\x001bÈ£\x0010ÜkV²i\x0014dfÛ¸¶ 8Øóe\x000bq»NyóçpÇØô¬!¥y\x000eÂªg¢
æ<	x\x0019vì¯;_w4Ù®ËXRÊN\x0017vv£ÜWÎ\x001bW/âæ6.¥f`üYFÃd\x000f®¥/\x0005øcpÍÅe\x001e¬5ÎôÀÝÄÛìm[¹ñ\x001c_Öt1S*pwNè|\x0019xp=ð0®P¢%Éèlk\x0002³`\x0016àÉKC'XvãÖv1Cù¸q¯\x0014òÒò\{PàxNu\x0019x\x001f\x0011ïaàcZiM3mB\x001e¯
Ú9J;'¼\x000c|'ãvFÆg¤¶\x0010IâàxOÊ²Äµ}­|¯\x0000nm£w}LKû\x000bS\x001eûÝûÉ\x001b÷Ô\x001e§lÙÈ7®öÎ\x0007j®\x0002\x001dp\x0002\x001e\x000c×)ë'e6ö\x001abúxÞáz\x00197ö%\x001dÀª\x000eX~L6\x001aÛÊ·m¤èÏkÛÓ\x000e8M\x0001º\x0005¶°s¤<¸\x0018abÿ6Ý#\x001eó©¹ájÏ9KÒâJà´\x0003>!ÌQS[!ã2RÔ\x0005\x0002ÀuY:\x0019UzÜ\x0013\x0006\x001f¼WI§×\x000bn\x001eäwmHoû>#kýDJ6B\x0002¥\x0019÷¤JÌ+'Ç\x000cÅ>v\x0002·39ðèxOjÝSëB-Á\x0001r)e}¸\x000c8ÙþÆÉNÜ8&\x001d\x0016JL"Þ8¾\x0015ø²Ê%Ú\x0001(\x0018Ç\x001c½+­\x0019¯YªTò?êz§\x000b\x0013\x0017Ãp²T^Ð>E]êÇDôFó²Æ\x0002<\x0019«n<G}©ÛÌÈ8ï\x0002®í2)?IþÇ"*ÔnÜá*ß\x0010Ì®Fo&ªj±ì½®¾aLNCü\x0018î¡s¢Ï\x001bUã¿þm_7þÛD!3è
¿RÈÍï <\x001eÞ¯ËN týZ_ëú«þ}Kl\x0014à±2Bë>oGÞÛ\x0011%	¤íRsË³²\VAfè/{è/ÃÐCPÂg®ýa\x0014Mj\x0019­u	D\x0016÷7{q3\x000cÝg÷ÐI0ÄÄ*5Eî¼o­m\x000b\x0005ÂîÖ)ÌÜzÆkl£¬\x000cµ\x0006\x0014T;Z_
zËÒûÊ)ÐýD¯RÙ÷\x0012£\x001c\x000cÉ\x0006\x0017U\x0016ö\x001eô\x0017ýZÛ=AIibD1Kä4\x0011jåZ¸ÿ}/îÒî²\x000f¥hwQî>þ
ÊÝï\x001e*÷ ?T¢¶\x001a7\x001bkmÄÊ/¨%¸pé¥½¿ô¯§.=Ùvéb²I
íÖU=ùÖ_ö·>.ê\x0018Ì\\x0013o\x0000BOçcTwnýý­3ÕEð¸uíÈò¿#ÃÐßî¡»\x0002º&FÝîA\x0013F>-«#rh¯ÙKÒhFµ3­­.YöCÛdª»\x000fÌ9ëØ´\x0017ø\x0012\x000eK|ôÁµ«\x0012=j\×ëÄ2ó²Êû¹6~{\x0013÷õýì=v½ÇqÍ\x001e¹OZ\x0010\x0013H\MÉ¸Ö¥pÎ+yçÒßí/ýÝf§M×gÓìþ×Ñ1ÿØCÿÇ¼ho\x0008«Ç¨ò²\x001ezy£o~òF%&ë\x0011\x0010»äÓ\x0014RðØÏW`¸ÛÃÿÀ{>øÇ»~óÝÓ×?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Þ~Ä»\x0015]i,\x0010-[þ\x0001Á+@¡IÒ?Æ V}ºÔØ`°f\x001b¡à*o­ðy8ý\x000f\x0008P\x0001äÍÛë«³{°`ð'aí\x0005ÕÙÆd\x001aI­96[È;\x000f®\x0013\x0014uÒ#ÏS¯ö£Ñ¤\x00034ZäÑÆ@^ÒÚÐ¯\x0013\x0006\x000c_oµ\x001f\x000cJÈÐr"¿ð\x0001áïD9³&o_n\x001f¿ýAïS¹dtñ\x000c;úóãÃ×-,^\x0018s¥\x0006#·RXôä\x0019\x0006.få\x0006öòë«Ë©»pÅ\x0002_HïÏâèù\x000eXP$$o\x0018ó\x0005\x0014X|ØX\x0016\x0018øML\x0003LÌ3\x0014\x0000Æå¶{ø÷T\x0001`45æuÂ\x000cNÓ>4\x0012\x0010B¶AÚÜ>\x00001´Ææ×ô&<ÄÏúr}©ÞôáþÓâKÜ½Ö\x001cªÁr«ãàÒWRÑÓöÿ`ÍÌ\^¼:y$Ûvà-8UjîEâ(\x000b$\x0014\x000faç(÷\x000bÎ»\x0008$ê\x0017£m\x0018¦qÀå><?Þç\x000cÁô÷{¯#kgdºéánQ\x0014b\x0019¬Ê­PÐÕ^Þ\]L'
0d\x0019vúÑ\x000f\x0010êäî.\x0008þzô\x0012-ÎýóÝrëö1\x001eIÁ\x0016S]\x0006G@¥Ý\x0003Û§^¨óóÓübÿ\x0012MÏÅÍùéTZe©ª\x00073\x0015N\x0001#~!­	´ÅÚú|H34\x001dVfY=ä´
õ0ÍêÃ´CLÛ)B~,@÷kRÏ;bº`3äRÍaÈ\x0019z8-Á\x001a:KÉ\x0017F§\x000cõàã\x00010ã\x00103ö`Â\x00017y9Ï\x0005ö3Ç\x000fÖQeé<LÊ\x0008òA\x0017=p)\x0011ywOH9\ÀD©ÌIO[39kÔc°s&ÒzFÁëicYPwÏ.+${L\x0012N%Ë±S8vÛÒRn\x00138×ê>P]ê\x001eÛ\x0019DnÙ3ø¼ÆH'ó)<âÒÎ\x0007­Ì§ì²jÈ\x0001T¹\x0014ðá¦O\x00194\x001cbV\x0006TvYP¥\x000f3\x001cÓ7fÛ´<;Êõä\x0005Óu`bG´.?®ZÞ5OÏo6³(Uµ=UÏöLM¯Ù.ÁÔñ\x001c9ÚÞù\x0003 Rd×	]ô!&\x0001&\x000fo8\x000cáXÉøy~PëH?X\x000fé\x001eî>þxûëóÏ.u®¯5\x0016\x000bö½¢cäè²Ä"úcç/¿?ûï7ûpª!§êáëv¤K,±\x0014\x0019[¥õäoàÔCNÝÁóç\x0014Ý÷°¤0Ò\x000659Å¤¡oà4CNÓ³pzrøi\x0003K\x0000§ã¤\Ü
vÈi{ÖÓòïîÙ\x001f9)x=±vl>§\x001frú.NC
,è\x001c	Ï	\x0010s\x0014¡fN"g$©\ôG¾;ÖT\x001c3\x000e9c\x000f§±\x0019û¯I
È)°\x000b7YOµuq\x000e#e½\x0011)ïyàs\x0012#âDtúê6õÄU>\x0000emå{Ì<Þ;òîfÅsm2§u\x0007øê²²ëáçÞÛ·ñN»¡\x0017J«½uÚjeô\x0003òËLùo\x000fÏ\x001f\x0016\x001f¶CRåj7Ê#\x0012\x0001RGèÀÛOô»¼yqrõb\x001fD=DÔíÑðuX\x0004ÇF	ZH\x0013'³ 
~\x0008é!áRgaÂ\x000fÙ\x0016\x0019CÏ\x001f\x0018#Mðû@J¿\x001e"ùµ\x0010éõòþévq¿ÃSzÉéd\x001f,_Ýà¢¤É²0uÆ_^\\ìC©º\x0012ÐB¦´.ìÞÒJJ\x001f¦¬e\x0003£\x001d2Ú\x000eÆàJ¬º³96Ðr^rÚ7Pú!¥o§Ä	½ùªn]àgè=\x0005\x001c©
h6d\x001cBÆ\x001eÈpLÇá\x0014\x001cº°\x0005ZIAúe³ ÎÑ¯;Ç=)S£c~²¹w\x000f!Ñé©\x0008s\x001fF\x0011ÖN·\x0008k§ûäë/?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=>	¿{ñ8\x0012u\x0012pá~-2^ç\x0012{%=\x0016+I!(T ÛE
/"ç*ðÑz5>Ð4ÄíÊ5p7É5,ì
ÚKÈTÌ\x0018¦\x0012Gû¡\x000fÕz²\x0001e;;eoB¶"d×#\x00041l\x001e
µ\x0003\x0018Û1YÒgÆ»±7¡"ï\x0006\x0003¶\x001a!H.Æ-\x00041Z\r\x001aiëþ÷Yr¾!¿Ú\x000c9h/ÂWÌ%9u7Ó®\x001d<ÜNu\ûÕÎkÏ\x0018¶_\x000c|¨A¼ä¤\x0008\x001d\x0008ý.ë­l|\x0001G6[o~Í²^Ð£Êà
äÐÂèôrBÖíxzÂ´S&ñîù®Ï\x001cPÖd
k¸¤ÃÜ/\x0019l§vli\x000e\´­\x0004_Vðå\x0018|é%fO9É=M\x0019¾Xè¤]
ßV£oGG_pl®å¤"ANéLª.\x0008ðU[
«\x001b~\x0011Þ
ðwÂ»{,\x001eØ]ª\x0011ãhè\x0017jpÏCç*
J\x0015½Í\x0015o+ç×OÛnØvøD$(GDu" 0\x001dÉ\x0008/hð\x0017F^_lÞ\x001e»i¹DÛ©5S.Ö\x0015M\x0002RÉ\×S\(Äo¸cT\x0008\x001bì{jãé\x0017=esÁÜ\x001c~^øÈ\x0003~ø\x001c$\x0000\x001dyÓ\x001dö))3+\x000e	HHþ]@á\x0005\x0002R\x0012P>E·\x0000«'üzÂÈv}G7|]Ã×ÃðuNï\x0011IZ0á'åð$_À5Ó¬R¦y
©>QæôvD¦	tF\x0019\x001b./ËQ\x0004\n¦\x001bïéñR\x0001\x0014b§ 1)ø1Èb4\x00018\x001cÿ`\x000c
Í\x0013\G yòÇ#±Ý%±ý£\x0008¦´ÛÉ%\x000f'\x0005éLE¯æÑÓãÝß\x000f^ßoáTê3HÑÛA¾*\x0016\:ÇP\x000c;ü+æ«þ¢oóèâüäß\x000e^nàpåR\x0006]l\x0000»\x0006\x0019è^å2\x0019d¼Ì|õè\x001edJÆ@Fèf'¡\x0004\x0007IÐ\x000eã/Æ£º7èfÿ\x001e\¤VXdf\x001d.ÒPYoX[©H?üÁ£Â7Ü¿\x00072\x001cã^i±\x000e\x0017f\x000f%O\¼¦:S§\x0005ñ\x000bÔö cTIÆ¨uÈpyÈÐ(\x0007ùr"ãÉ(÷ìwZe$XZgÛu6
#M|\x0015\x000eeL\x001f
»4Øg

\x0007ø\ïð¹^§Å[«\x0005>y~øï²s\x0002\x001d>7ë\x001c\x0004\x000e5ÂÒÓT#ïòôð\x0019Iän:Îí\x00034ü'ÞÝoo"ËíýÝ/Ûg¸×Â\x001crôåJ\x0006j\x0011±ü-7®×¬}2¿;Ý\x001cE\x001aÓ\x000ff±óîõâÒõ2\x0004\x001f<\x001fèHStãÓ\x001aÉjn¾õ\x000eøZîïI(ßËò¼§Û®X A­\x0018KCçÔèsöÎ¶ëß²8o`0ë\x00125×{Ã¶\x001etD\x0012êðlMý ¤ð"~¡ó\x0012ÔEp@måÀ`C\x001f®Ú
ÀH%HÌ/\x0014B^º\x0008¹\x0006Ô,\x0011Ecí8\Óià\x0002ñ¢ÆØ\x0007ºZÖ~d]\x0017\x0011z£]ÒÈ\x000c{Æ\x0006ïí*Øn\x0000vrCFÁ\x0010á@;$Â¦¶ÞvÔ±\x0007vÑ×0nGåGp{ô9è.O\x00129ÎDÎLã¼.Ü¦ÚñhÝ\x001b7$w;ÔáØ¿LJo'}Õ\x000e\x0012^¯n>²¼9Hî°ÉíauÆmW[ÝWË\x0004>÷Í\x001dV¡á¦ë CËÄµk©ºp\x0017W»ÒàïÅ­PÕ-ÀØ\x0012NjÏÀvæaç\x001dYX½é¼Þÿ\x0004å[¼&9á\x0016<=«Â5éôj§	\x0000ßî\x0000ßî\x000f<À\x0015xU²	¹¤\x0001\x0010<\x001eG\x000eJéÕó\x001cBûð<äbÁ2ÿ°½\x000fÿØÝíS_¯u\x0019=cæ¶Ë}\x0004µÖY\x0001§­7>Æmþasz~vvr|ñRz\x000frj\x000bÔ.¯ÂEåä\x001ei'.Â\x001cÊ·#e/r\x001aWÑq+Ñ	\x0017\x0013$5åRQ°PR\x0011\x001b-§ç\x001elbü\x0015m|Âc\x0017o\x000eH>þt÷¹oZ 0\x001e²Z·\x0011¤£¥hîùÑqzpüæôäòÅàE	^\x000c×álÂ'S\x000emP ®hªMñ[ôôÑÚ¹ÝÑß<ÜÜÝ><Ü\x001eô3lM\x0003E?éV\x0013ÊÉÈ×.°-¨§÷ÉñÙÙñ<§8\x0011eÁÀ	\x0005ÿo\x001f\x001f¾ÜÒöxûÜµ1Àúæ¤\x0011
\x001d\x0008·RìÍÜÜ\x0018oÏÏÞç¼Ü·W­\x001dø\x0015/ñCà\x0010~«-é\x0015pIº"Ü8Jh\x0011¾]lÞO Hn\x000bð ¹m\x0000:¨Ã°ë\x0014ÿ\x0000ü\x0008_
Ý´¢»ás^ÁÏAüá¢0\x0014ÐWÉ)Í%½\x0005)Û~Ü~\x0002U\x0004Âç(\x0001Ee2Ü+¬2á&çà×úÊS j\x0006j¤t(#\x0018\x0005lÂ¿"úºDØC@Éb%cFñÿÍ6ßÜ=l»N!íIï9ª1á \x0003»Xµßî\x00137\x001b°\x0002OÎ6³$Ê¦Q2\x001a\x001a£$¨!nXG\x000c\x0005É8X¶´\x0013lózëãàbWßb/8ûJÔzpÏwÁjÚ>÷Ükáï<Ä\x0002P\x0010ÒÄ\x0006ò\x000eeÅ-´^^tupqu\x0012ì¥ÍÕ,"P\x0016\x0018ê/{2\x0008÷\x0019Ê'\x0007{\x0002w³È\x0004T[l\x000f\x0002ª" 	@u\x000cÃ"bò5ë\x0002\x0003¹¬½úr\x0006¢\x0010\x001fETªì;\x0007YÂ\x001aÒ3\x0002H!F
3ÇQ?²\x000e\x001a\x0016\x0011\x001fÞ\x0007&Üd©]\x0016.7ðr
\x0006sr-
ïDò\x0015üwáÑ³ý\x001a|ûôÏÿî\x0014PZa&¶æ\x0012Ý\\x0010ÀTy\x0013{)4,ÔðÞÙ¼I
L¾½8n+¨$
¢¢ V  -µþ\x0008#Á{È.%-'Þ®îâ õÎ¥ u%°\x0019(\x001cÿú©+Hd\x0015çÄ#v .X¹\x0018}¡ÇåÁñ_Þ4cD\x0011=,þ\x0002=|\x000eÁ nªò£9Õ¼	\x000b|Â«yiÍÛ"üà\x0001ørû´3\x0003ð!\x0016&wòQe\x0016&{e\x0016\x0017î%\x0012/ÔZe\x0006¥PhbP
îµ\x00171à\x0012×\x0011UUðvéäB\x0006E)<'&§\x001eêÈvrÁ<\x001f\x001cm\x001f¶=ª\x0012á6R\x0012©\x001f²t#{u¡]û}/W\x0007G³MKUÂò@oxNí
¢ß>ÿ|wûÔ'ËÍÝ!'9-\x0013 ½"5-ÙÖt/³Æ¯Þ\x001c_4Þ£¶G9\x001eþ(-\x001f§\x0011\x000cSjcí!­#Ésý1i*ÛÇÙXR?IZB\x0000|<Þ?m	,ºî\x0005\x000f]\x00101\x0005Û³x\x0007±wÍI!ÏËeÒ¿ÇûÍÀ¢u3$\x001eÒø\x0007|ó\x0010R  n
u»§Ö1·\x001b*õò`;\x001eIË
Xî¼\x0007&ÓcW·_á\x0018\x0018\x0018`-yÏÑ! J²­Î°Üz\x000fÌ¦óVËb"R\x001eµ\x000cüb\x0005>ÆáC¸q\x0010\x001aÒnÖ§ÍmÒË{±c\x0001z\x0011-ÀâÔ½¼½y|îÚí`f\x0012¸ñaÂû!_{ÍÅU\x001c»ÇGçWÍ­ÎìÎÒ
Û¼p·~>H¾ÖÏ\x0007G?]o¿|ÙvöÑPiA\x0012»y\x00072®@Óî¤NþÖKt·^\x001e\x001c¿}½yÿ~Ól-C¼dÉK®ÊËa\x0016dø?Ñ)Kõí\A^ºä¥×ä¥\x0014Ê¨î|Ëx®lßûòÒQ\x000eN\x0017m9Ã[JG5ø×Þ<m\x001f>¡§ç`\x0008':\x001caÜ!K\x0002_Ñòl¡¸,xÚÞ\lÎÞ ¿§uÚ\x0001'Îª8ñZ$n{$åî¬ ,ÏÙ¢Ö\x0017_!õuC3u&®Ê\x00149\x0013÷=DÃ\x0012|î|.FE\x0005\x001d!Ðí`<Y\x0005nYFñ{#uw5#\x001aª£qSäßëWðYOÊÑ?ÿ¿\x0014\x000c}û±GDZ2¨ÒJ¥î\x000e:h%\x000f\x0004tèå)ÇS³v²w5+Gç)4þúø¦¤´Iú
{Z¼ÒUÁÜÛ»\x001e?÷xEm0ËP\x0014ÏD='¼4\x0019pØ"2	b¼=¿l¹D\x0011½¬ÐËAô&`.Ç[
¥yJÕ65£¦\x000eæs84wý\x000f};B+fÐàW\x0006t^aCä4ôÆÏ4©®\x001eííàÕN´W±L:méÏ\x0007Ï?ßuÙ/ÚHJÚ"®¨¦(dV\x0011µmïCÚÏ\x0007çWïN\x000f.\x0004¯*ðj\x000c¼à¨·£v(ìÀ\x0004\x0014\x0000£bÓ\x0004úåØu]\x000fbWÔY%üÑ\x001e:°\x001b\x0007¾}!ìÁa¢~}ÑñÀ¼ânñéöÇ_{"aáí¤iÍhaÁü
&+pvúSyj~8ÿK3ÃÀì¤ÄûR~ç×Û§§í§¾¼~°\x0001\x0005
\x0003\x0008<+¥\x0017I´\x000f»Û!¤Éïüzsq±y3_Ú\x0012¿´£\x0004<Ãe\x001f«ÓQîÎkCupJ-læ´ª\x0008¨Q\x0002Í¡
Ö¾i\ûÒ£«\x0007jßz	¼°úMßMTcc\x001b°â²zþ|³í*fP­çIð\x00114\x001aR\x0006´¢&fËúÂeuuy´i\x001a
)v§JôR
¢÷\x0006E»c_\x001eìù¡@:$ygÚ·v ;ÉAFVÉAoï\x001e?uEà½
·+½w ê\x0018\x000e/\x000fòqeï¸`&¿y1áË\x0012¸\x001c\x0003îEv+l\x0012£¹|ãm×ò.îÙ1·%t;\x0004]3ßÎ\x000cË°É+\x000bµD+y¬|.~AlÛLýìñ©§îÙAe2\x0006ÆP§GC\x000fdiÛNñ®Ñgç\x0017­ÂçÈ¡\x0014\x0015
\x001cbØ 	íboDcQk´\x0018fj\x0017zX°¤õ>)óA\x0004\x0001>ÅÅíÏ}\x000fFhTûØåãÓ\x0004ÅÒ¡KÆ\x0012ø\x0017ÇïÎõ[ÑD3Enzx×±ÚÐyúÇöîþ>Æ¾\x0007V¤®q`ÛË°wS\x00039áÃ+1eLË\x00191§ÒØ¹ø÷
è8]´,Í,0U4x¸±j-¡÷Àbûô±g\x001aÓÚ\x0005\x00174V6pè\x00006¥\x0016öÊ¸<x\x000f,6\x0017ß4CÉ÷5¥Q»\x0014úöñ\x0001\x001aÿö½µ,äm$Y\x0016#\x0014ÞW\x0012ùV.\x000fJ|{~\x0006ÍÎ|\x0019\x000b\x001eÜäq
ÿ\x001dø¬\x0004à·÷ÛúBÞKzïJ§\x000f\x0004¿\x000cÏ©«âb	þÍéæíæòÕÍöãöóp¶Ó\x001f2\x0007\x0015W\x0014¼«Á¶Ïz.>wFU\x0014Ø=Ã\x0018gRFkØéÔ"ÏÊvFk5\x000f\x0010Qy@8|â\x0013¦P\x001fw¯xÝúæu¸à~ì"à8D©±ÒÇøCÛ´ÀòÞðèXæ»ÊÞðEO°\x0017ð
ö.*Øá\x000f¯ÑCðsn©ÄRÍ_-\x0016k%ü3SP6\x0000)Pz\x00034L\x0015Ö|j&=Ã\x0018gËÒ°z8¸\x001b\x0018)\x001c,ËeYÇù¶Úì\x001e\x001c¬­8X;>\x000f\x001aÔ~`\x00042¥3ÈËe\x0019\x001d\x001cn,À¡r´ïÇÁPFã`n;\x0012/F©\x000b¾ðUßÁÁ³gãkÉÖ\â`\x000f£Ç\x0019îi.\x0016·\x0005\ÈAêX\x0012bø\âÂÀa\x001a×\x0012(\x000e$
´¡õ²¾å\x0004¤¬\x000e%)G\x000f%ëÌ)°·{\x0008.åìXy3ÈÂ\x000e\x001c´\x001cçà²t§Í"ËÁ$\x0007K;\x001aÐGÁïÔ\x000eÓ»¬\x001d¾Eím×«Ç\x0006k\x0002£6\x0015Ðäð~\x0016Ï<ö±Rñ\x0018u7¹:ÇA\x0016©\x0003|rP
.µ\x0018\x0017`
"M)Á\x0015mn/ä¢:ÑÃK6FléÀ|I\x0000>G	XA*\x0016BF%ç¯/L»Mf/\x0001YÍ\x0000|\x0012\x0008¯þä2²á©F	ºÎbå|Fe«{\x0015©ÒW\x001a8'st\x0015I|¹YÉ©l#v(B\x000e²ÝW£ÏY¼ÛÂó_\x0016V\x0012Ô$Þ<>ÿr\x001bn=,\x001c£æ\x0002Z\x001bEj:±RMaÏ´Eöê\x0001¤É|8\x00069äYh·S\x0004\x0007U:X\x00047µ×xÛWÞj¬a¤¢ÇÃãÓúT\x0001ä©´R2ÕQ\x0005\x0007­s\x000cJËUp\x0003\x000cÂ£!YÜ\x000e\x001cjj¨z¦Ý ¢AYG\x0016\x0018ä:²\x0001
ÊAíU\x0015ëCKdäNíl¾~\x0006ªf Æ\x0019@\x0010Ô¶å\x001a4ª#\x0003#'mÕÕ(ØôV\x0008kWÕÛÿàÝÝíÓÓíÁÑãý=¤¶tzJÐ³yê_*5³=ÁÚ\x001a±\x0017ãÝÉñÅÅñÁÑùé)$¶Ìñ¯à\x0003ë\x0010=áÒ{TK\x0001-\x0012#!ïL"¤\x0004[èë[ÌH0Yg$\x0008ø¯îf¸|ØÞß?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=^-a{åóåß>®bÕ¡¾z»s_º·ÜNCsØnKkú¸\x0001¶4¤?ç·?ô;óîá\x0007ûeõñ©µy¸\x0012.M®âJ¬»§\x0016`ååK\x0013½ò\x0007?\x001cü¶æ=zÞ~Tún\x0010Á`\x0015fýTG<6\x0001\x0018\x001c¨Jc/ ñYÿÀGSÔî\x001dpãä¸þÛà\x001fÕ¨ðÛû*\x0015p»wzuù\x0005Ûêzº\x0012¿Vä
¤Ì\x0003\x000fnT\x000fÂ
ËéÉñÏØ­üø\x0005ú*Vï?®ë°êìÏ|Xm'÷XË&.\x001aC©¹\x0007\x0018¾\x0012ºÈ0âo\x0002sqvôüàäI,ÕåÙ	\x0002eÌùL\x00102\x001a
rûäø.?\x0005æò«üð»\x0018©³]úüp"ßdK3uîN£öh;ØÇzç,÷ô=\x0006Ç^þòùýÛÊ\x0015Ä\x000e' xm\x0003I9QÉÛµ\x0015q0LÅQ\x00065õElAòá÷Ö\x000fwõ¼Y_\¿[}y\x000e*â\x0006\x0006K­,1
ì¢|'ÒÉÜ<"õÃ\x001b\x0003òôòðàç£Ç¿ÒïãJÜ¦\x000et×uö×w¡\x00150¨s+õùäe1
i®3\x001eP\x000f»FàÒ0ÀcÄÅÛO_WÓ62AÕÕÎûCKû¿ÛGfÂ\x0007.èËñºN¦¦\x001aî\x0011ÍµÁô|\x0008Ma¯Yz´cÃCËW\x001béÐò<Ü6ÏàÜÊº\x0019Cp®ëàÜ>í]Í«Ú\x00136MUA%ý]½\x0011ö8iâE\x000f¶²Â!y`nQôÁðNX;*²5b3¸Ð1=:ÎÍ.wÂ\x0004Zò\x000b\x0007§¸à;ò\x001a±mèv§ÕðpádæßÃs£V%¸p£°¤\x0015\x001c.L\x000ep¼\x0004\x001a\x0005|ãFºà\x0002Î¥G¨**:\x0001Ñ¦\x001bGCDð\x001fñÐchÄ\x0016ÑISÔ\x0006\x0007ç(V\x001b\x0017Ó\x000f
v\x001b8)ÑÎÏvtëy.\x00055>+Y*õ87ààtTiúPõÞ9\x0012\x0008í¦îÜÕu7t_.ÕúïWø¡a¿Íý»ûõSk¶\x001c²áæ\x0019IçàÆ\x0011?¡Å­÷\x0014´Î24l¸9?<?ÃÍZch·¿:ÿ7=¨-í½Ø{u±^ßß]\a
ôêæúÃÿx*Áá8@5iú/ä\x000cGðìø_þ£³³ó7G'X\x0008=9}ùühêð#°®ÒÚT£ÿî»/\x0017×X¨Íkhy\x0007;xþ/¯±Ym;æ\x0000ª9É°\x0005\x0013A\x001dL\x0006ýÝìe\x001b9J<»ô\x0012«¶y\x0019-/b¿^\x001d¿ÄÖµÇ\x000bÍü
ºz\x0005=û\x0015L¤æüÄZÝÀ;èÍ;Ø\x0008ç¿­ÞÁÎ\x0007IT¦ð\x000e\x0002;ùÓ;Àoù\x001dÆÄ\x0011³ßÁWïàg¿\x0003øDH8¡Vr'©ç_\x0013Üü\x0019&ûÏ
þXá³ñ+GKi\x0000¿ÇÖÃô\x0002Âð=\x0012£Pfö7P8«ùâ,#sâ;¨ü\x000e6úò
£áÙ¯P³/ÎÒ\x0014.Wáh\x001d(¼`Q\x0018ï®ÿ\x000e8«ùâ\x000c2,ty\x0007U
¦\x0010é&ç¿C%Îj¾8cGkNÀÈHkã0ÏIÖL"¯ÍÒï +qÐ³ÅÁÇy¾òwP¤pÓèâïPÉ-\x000f>*j"ÇEIy\x001bFöà"\x000f£®ªùïPÉ-\x000f>\x0014$\x000fÙ3²V\x0017½´¸fÕ8èÙâàáþ(U^ÁZ2þ§L%
f¾4 ºù
ä(YMSø\x000e;J¦ºIfþM\x0012\x0008
á\x001d"W\x0011ÁÍì(Å\x001dVS]%3ÿ*á/ï\x0010è\x001d
;Ë©%3ÛYrÑÒpFz\x0007/ó;\x0018£Ë;,®l%\x000fv¶<¸@é¼äs\x000bz\x0005­ü?ï3ØÊ8ØÙÆ\x0001WÚ(S>C¦Ä
\x0008\x001bqX\-ÙJ¤ílÆ­,\x000eRPÜ@3Rÿ¤¯P	/\x000c8¶ñº}6o<ÏzuÄz9÷\x0015\%\x000bn¾,hWV?°\x001f²yÓ^\x001d
qq½ê*apóAyÚAäQXí+ï°üw¨ÁÍ\x0017\x0006éiGU¶oô\x000e&Èò\x000eÛhW/\x000eà¦zUÞÁ8h½ù\x000eG\x000e¾ºK~ö]²ÑÐM~\x0007\x00079¤\x0017WK¾ºK~ö]²ASÃCz<at\x0011\x0011Üì\x0017¨\x001c%?ÛQÂ¦\x001a~\x0001É\x0015TÛmXþ\x001d*að³\x0001I}\x0007ï@=9Ë$ø\x000e ¡\x00120_\x0018p<gXeîs2ÊHûÏ3Ñ¡0_\x0016\x00143=¦$±ÌÒª\x0008\Ü6J\x001cÂ|qÊ\x001fy=S¶
J
Þaq½\x001a*q\x0008óÅ\x0001cgvö4'YÿÄDw¬|¥8ÛW21l¶MÙ}Iï ä¦à°ø+T\x0012\x001dgK´:ÒÂ¬Líü¶E+-.
±è8[¢Ó$¤)¯\x0010²!C,\x0011èñhþ;T\x0012\x001dgK´)[á\x001d|Þï°)]¹å¯R%Ñq¶D\x001bïÇ*#²¦¥wð¦h¥ÅsÝRÔUP1_¤\x001dóS[¥$'%6ÒÑK,\x001e:HQ×AÅ|¡6
9FÒKhÍÛé%´âØAý\x0013^¢.ùb­¹9
^Y?À²\x0005.h½üKÔP1_®Â\x0010:½\x001c=àFH~Ñ&×ù/QCÅ|Á\x0006­Ê\x0007c8Å'`ï{iÕ$\x001f67Ì\x0017kL\x0003¥6zYàÅù\x001e/nÿ\x0012µXÏïo0Bb«Kz	\x000bº)¿Cà\x001a1£±ùïPKõüþ\x0006
þF ýj-1o\x0019±I/Å\x000bÓòAÃü\x0006\x0007d¤\x000bä»"«\x0019½²,\x0010î \x0012µTÏïrÐ¸T>¿CÔ©c(ÕD¿xOÖM\x000er~V¾ÄÔÁÐ1±\x001fu0ÏZ¬ç÷9haiA5îô òCÞk_"¶¹ÍZ®ç7:¨(hÑªÕbÃ8l,Ëu\x001c1\x000eÏZ®çw: 7\x001b1(j¤­Éë#+X+ÆK«f¿C-Öj¶X+,¢Ð+xò_u,\x001by­0ë×ºYCÎïÖHl$48\x001c¦\x0015'8H"@Ø\x0017\x0008ý \x0019q¶XËà÷óÔ¶´è\x0006ÞA2\x001d§Õnq¨»5äüv
8i¢EJ.w#jïT»\x0011\x0015Öü¨¥z~Ã\x0006n¦ö$\x0012Î\x0011§&¼Dd0Û\x0008mÿz§\x001f\x00034óUdÚnÝXOüOÚ«\x0012NÅsÈð\x0001Æïâx\x0017ëi\x0015E3ÁplµíÕqwy{Ëï?ù.Æ/+d]ÖWÞ9~ÑÞÎ\x0005Ê\\x000fß\x0004\x0002Éù/b#ÏzçBKNh¥cÉð/n>\x001c}\x0014ð\x000cç¿±dAÃÀìánÂÖÑ\Ê¬>dúÑí²KÜ.\ìeoåh\x0007P¶øVÍÁëä¬?Þýz=dÊ:º~wusKÛ~º¹½øüëv¨\x0011Zf6\x0005\I rªÀ[ËP~4Epôòðäô5\x0013+¾>zõãÄÔ\x0015ëÏoÃ`d\x001d®>Á	¾²|X±q´ËQ>r2#Ç`\x001d\x001e¼\x0003{65qç»«Á¨ÈÁ´øýÝÞ\x000f{g7pX_.®¶O¸»µ²\x000e¸w?ä@\x0012\x000eì«s\x0013NÚBüì
þ)§p^?\x001f¼Ù\x000eÖvÀ\x0003óï\x0015ËÆÞ2\x0019óãUíèòho\x0017:üUS]Ò\x0011<"c^L_áÑÊ\x000ex¸WÑé2\x0004dxnÝbi3¼Ì5Ð\x0003O[¼o	\x001eàÉ±Æk¶Y~Êü6ÃËþ]ð$i­dÞP'ËéM¤XZá1§Z\x0007>ï$K¹ iðÞX:» '\x000c~38âXë9<U\x000c\x0006®¹`-¬Xß¹0ÿæ1LÏÙÉµÒtxy¡BnÝõ||j¢£\x0019\x001f¯\x0013î8>p\x001c\x001cI®äí\x0000ÆK&,qa¢å§\x0019\x001fo\x0015îÁ·Q|»0¼ä¤Wbä
\x0008Ò:à¹\x00189h\x0004)¥NØ\x0010\x001cX:\x00168=¢Lë9=ìR&áP¦\x0017ÅæÆ\x000cI3>".ëÂg¸¡Ú*GTÄðcnüs\x0013}­ðÊ¬çëBC}\x001bi_PÏºd¯:\x0017øvàãÍÖíø\x0016Û³W ¹Í
wÌ.è\x00150áYÏùáÒ|~úú	\x0003÷D\x00067Ñ×\x000fn°êS~!X®XZp\x0011\x000c
?z\x001e~ô\x00139Ðfx\x0015¤\x000f÷Üf5íÂ¾ëÈèÂ8«Ö\x000c\x000fyA:uáE\x001fðu-+\x0017íUùº\x000b\x001eè\x0015Õ§[çä°\x0005 4$àlào;53Ó
7õÀÃô\x001c9}Æ\x0010q\x000f¶»\x0019Æ7Q¥mÆG;Ã:ða\x001bj¦\x0008±ÞKî«(<o2Ê\x0005ü>¦Wë9?\x001b÷#ûôû\x00027Cü~Ì'Ñ\x000f®\x0008þÕs~ ±4Üî£GN¤Ü?êÈ´E=¢¥ëÀg¿£AÅöó3Äíe­uû¡\x000c®gàÕÄ k3<P,ºO¹`Û')\x0017Üé¢¹evQâò\x0005ðÁ\x0017Ð}!¥\x0015§_píp.)\x001bU<«è&²Ó­øLÚ\x0017Þ\x000fw\x0011PY)hÞåidi ~¸\x0003çMzÁ&@JS!
¥þ9ÏÇç'záÁ¿Âôi\x0017\x001f4ïÿ²Xl4øÊ¼\x000e£\x0005\x001dèpY@n1Þn\x000eÏót´df>Ü54_÷ÁùÎô	/îh\x0011tù,îxKðØoq´å¶\x0003\x001dòrõ\x0005E^J,%¯ÞXV}ÆFÙ&ÒþÍð@«>ÍKhæ\x001a÷Rg©fÂN1Õ³ß\x000c¶wö(ß\x0016<QîÞ5Æi>½Zo+>È!ûOyf?HCý{o\x0001\x0005-çë=Âµ}n\x001fDÜ\¨qÖpã°áÝ£2È%ðÁ\x0005¶}\x000f³\x0018>¯\x0013´½Ï\x0018Å\x000bÔ\x001cQ´vàÃKÛâp:à\x0005æII3 N¤h\x0007zÅöé\x0016gÓj·Ï'æÝ\x0014\x0013EfL\x0008SÝ\x001cÍø\x0003³3"W´75\x0008N÷
"ò©FãV|8ë:Å\x0003)¡èú!½z\x0018S\x00111a\x0007>ø\x0004®ÏmÑpéÈíÃ\x0015ÏÔª7Q\x0017NwÀÃ*QáÅMÂÄê5\x0003Õ$èLkÆ\x0007WÏõ]?ëK!ÆkCÊYE
a¢¸Û
\x000fD}íÐÊpwb\x0004=ã¨¡ÌóÊã©Qêfx
I;ûàÉÂÕ\x0015Á)õ'\x000bâ\x0014ÙX3>pI}[ª-Ü>bØµÌ\x0015Ò2\x001b«`Zi\x0007_À÷\x000e\x000b®² l$v©Ñ4¤µl;b\àö9¤=íü¼X^\x001c\x0008Yvüàë\x0016
J5Áè×\x000c\x000fK¼}¦ÍêÀc\x0005\x001e)â5,bDôØ\x000f¬·ïó\x0015î4t|[ß¢eÁê|ËÑ¾Sõ©TÌÇW¦2\x0016\x000f\x000bDE\x0001ô^èÓ}*Ú}ËÀjs|TÉBê³ùÒ\x0011à_\x0011ú<\x0003+=ö\x0015déµ<¼©Øñ\x000cBÇ,ô)f\x0015$Õ9\x0012· Ö|åÜgg¿£ðö(©Q$VãdPä\x0019¨G¤ì\x001dø@ë>Í§\´r´\x001bYÒT°LG=ÞBÛ\x000fÄ+ô©>º%¯\x0005\x000fS²*0XÔ#Bê\x000exØÝÒ©ùlÊb¤ã3¼ÅBXØ¼í\x0002=\x00108\x0005\x001fúT\x001fn¥î  ,·¤aÎo\x0001ÃëÖc§æ3&ÀoQû¼W"\x0014.ô\x0011Á}\x0007<P,±S¹èDQá\x0005*ò\x0002>ÁnÕ\x0012UJ}^Òh?ð4©§\x0003Dr\x0004/,`wÑïºO\x0017rØ\x0000\x001e\x000cñÎI¥K"ÜÌ\x0017^ÿØ©ûÜ'Õ\x0007!Gn\x000c\x000f`ìøôæ+>ìQO+º{6\x0000\x001ebÊ\x001b\x000c 4Z@6@9ÅNÍWÆÉ@¶Mº|wSL±µ6Â?\x001e\x001bçúT\x000bXJ\x00079\x00101"þÐ	 ¢T\x000b\x0000Äæ9ÑçUé\x0002\x0010là\x000e
#ãrÙæÄõ\x001e='\x0018<\x0016ÿò	2­\x000e\x0006Z0¥1ÛuI\x0000éÑ\x0003Ð¹}?1nF\x000b4¦Rv(\x0015\x0016øÄØ¡&ú\x0014Èy¾\x00040Ñ\x0000ç9#\x000eqÓl\x0005Ø\x0003B ý\x000eb\x0015ihpTyÂX³\x00085ÁõÛ\x000c\x0010ÔDÿ¢\x001dïX²\x0011"K#	 Ñ¯*¡ç§­dníbë¸Ï*J^òãQ\x0004o¾\x0011I\x0013ý²³ÇTçí\x0019GiÉ¡\x0002ÐÌÏl$=%;LÁ¤1w_DÊ,bLÀÆPJëÎ/ËÔeÚÙf*d%£Ë\x0005U-&\x0019V\x0013¼³Íø|ZíÒwà\x0003\x0003%q\x001aåyñ4B/;;%q>\x0000(ÐxW,Á.ÌÿÀØ(;;\x0011U\x0008Ü\x0018Ð½háÜ|3§ÐÌ©>3[h(
Q.P]\x0010+Ô\x001aÐx¾Á>IÙÙ,)âi,¤GÈýV\x0018pÑ~\x00013ÅÅôh\x0007\x0008ßU\x0015qZq\x0016A[A\x0014Ê, L3õ²³aR!­2\x0015\x0002\x0006%y¨ÅLc\x00063ñit¦u3
ÅåÁSòä	\x001aÜÛÏOö uàC\x001dÓÙÑ©çÚj\x0004q\x0005ÄØ\x000ep\x0001?F§\x001dW]¾4\x0018ß'BV\x0017O'è5}a£ç×ö\x0013ììéDÆ%êº¸-R\x001d¡ì\x001a\x0014óþ$¦\x0012e_S'îc¡Æ+p

Wà¸§\x0013à/ cð_!ûº&ÁVÔ\x0014¼j
F\x000c\x0011º)cçáIl}]\x0010c:¾Ëø"å\x0013­Ú0ÀÑÂÆvØ1)ûÚ&SÇU®28
70oÐFyV2ãM\x001d\x0000QÉN%t!êÈf\x0013\x001eÖÎ7"ØÒ)ûú:mpWêèÙI´ù\x0000½ï'`¾X>?AB8,¨Î\x0005q] læ¦h\x0001¢/ÝÙ\x0013ð"|jÈWÐGvöH¨b/æw²³\x0003PbùðùÂ\x0012J±+,`æ0å.;[ìpÏ¹¢*È0qLyïüYAì¿MX\x0012©â³'#í¾0\x0016	rFÆ,\x0010Îa\x0003ììÂÂÍ¦ù\x0006Â7 Ñ\x0019í\x0002Í\x0006(eG{D;ð¡àúü\x0004A\x001bX¥S\x001ck:n~øxþà\x000c¿~']g$bÃ\x0017Â`\x0003\x0011åçÏE¥ÙôèÁ§\x0014«h\tÐBZ±@B\x001aÃdgÀöÝ,¼i]S¶\x001fNr¤®Åü\x000e6NFzô¸ÈMq&øÓâLï8\x0010ÚÐ\x000c\x0010Ãw	`s]*\x000cç6,mqÛX\x0006h\x0016°\x0005KöõaA\x001c'iä\x001cNÐ\x0014'5HÎfîùo\x001fÿà\x0006<%g÷\x0017ïÕýÛûõ½\x001f/Ö.Z¹\x000b>\x0016oKóçè¥ªà-Õ«UL}@\x0015À³ó#DøÃÁù÷§çgÏ÷~<:{q<½vw\x0011'k»1\x0007|\Ô"f\x0000ix¡}Têa¸Þ\x0007\x0012ÇTºA«@\x0011gÔ©=+ÔÜ\x00128ÞïÃyUz1r×bÔ\x000e\x000b\x0011	¢"êe$Îy(.}\x00183¹J'Fe©ÈBÒÈ
.\x001b©F\x0016¹\x000fd¦Xé\x0004i)Ç
\x0018i+\x0017\x001e$'Ñá>ôü»02I/HÁyLLÈ¹\x000cÿ¨G¾u\x001fFâ3éÂ³y\x0018yfÔ*\x0008_«î¸
f\x0011±aZÎ4\x0006\x0001%åãà(fÙÖ£dM\x001fJ"7é<K«yë<\x0012P%_[\x0005\x001bÄuK Ä¬R¿ÄµÅtøñó\x0007·E\x0007ÙÑÔH\x001fH":éUB:wÁyÁ=\x0004>ðIÆÑZÙ>_êUB2Bx½³\x0018e\x000f\x0002ÌV­¢\x001fñ\x000bwdRÞKÉS.ÒäéR¼qÔ®×;:1ÉÉ^ZúÜ©\\x0001\x0018m`ñË\x001cé\x0012 ÞKüßÎ«\x001e\x0010iõ¨2k?ÚG/Ëöc}{uïþ¨ª\x0017Ïn>­.¯\x0001é\x0005ñ\x0005f¶Ã­ £U\x0016@\x0006ÌÝåù\x0003\x001fU\x0003È\x0006òÙéãôH\x00033ÉáV87\x001e] \x001d\x0006]@
ÊÐ\x0002D:É¥@âNzôÌá+ 4Ä#\x0018\x0004òè8Ò\x001d\x0000H\x0002Þ\x000b\x0010'OuÂè=¤¦ 1ÙÎºR{\x001d\x0017\x0000i\x0012?é\x0005\x0019r\x0005#\x001d¤59O\x00114&~ó9YÌ{0âG6Ý_\x001a\x000c
JÂ\x0018
í\x000f:R²\x0011GÛ\x001eºB= qf"=ú@*CQN\x0010ùà&¦ÜGÒQj#)Ýü#Û£÷n®ßï]Üíýt$«úùÍõ;POàØ´eÈ`ßd&ì\x0006#IqÐcî\x001eTGÏ^¾|¶wôfï§säX\x0005øÏO_\x001e\x0002}ó(ómy\x0001=|\x0001=÷\x0005Àæ!yÜ3KÊZÊñÂ\x000bÚ\x0011f¿\x001d¾û\x0002`\x0001\x00024Ö^i\x0015á\x0005F«Õg¿\x001f¾û\x0002`rsS\x0017nP§v\x0006e5[	?Xú\x0005âð\x0005âÜ\x0017PÄjD \x000fM(+\x0005\x0002E`é\x000f k\x0019-ÄJ\x0012µ\x0011QÐÄ²\x0010âÒ\x001bÄQ©mö\x001bTB,gK±R\x0014öàßò
\x0014-p7rÛf½@%Är¶\x0014çq\#ÇÐ\x0010zÚ\x0008îÓl¿\x0017¾¹{ÿåÝ§¿
åÐHåçá¯\x0017à\x0019o,ÕO\x0017«ô»çë?ÿû'\x001cfd§âÕD#\x0010\x001c\x0003£IlðP\x001e\x001aÃ\x001fÀCÞ¬\x000eÒï\x001dýÇÑßìï/Ô×w\x000f\x0013\x0017{Wÿóÿuôáêò	*pø\x000f1Tim8-]Ìu\x0014\x0019\x0013GéS´w²wôüäøõ9\x001d`\x001aä\x000c\x001b09E3ÄØöA7Vzé\x000b¨I»³3¨Aþ­\x0001å <MÏ\x0001¢\®CL¦dgL×¸ù \x000c6Ü©Ô\x0012\x000f*7uÃÿ¨ÑäH\x000b(fmDeÁÌZîqÉç\x0018GdT.ÿM¨©µ\x00155´ëLk\x0011s
\x001aP)\x0005Ta4ö4*-.RÈÀµýáæþÝêþývÝ\x0006Úw]@\x0003b\x0018\x0015"·ÄñäÅÀ­ýáôüðàüÙ6`
séÑ
M\x0007IÝ²\x00025ï P\x0017ÿ¨	nÂ IíÔ\x0003g\x001bB78»WW«wm×\x001f|ºÀ×ßS\x0019\x0013tCnÅë?R_\x001c\x001cÖ\x001fõqcF0õ\x0010¦î	§\x0017ý\x0006¦Ê0­ÓKÂ´C¶\x0003¦ÅÞ^i)f\x000c\x0011æ(«×\x0001Ó\x000faú®ÓTyMØ"¶y\x001e\x0015ñÃx\x0007Ê0D\x0019QZ\x0011\x0004ï9Ò^ð~ùh\x0005Í»â üCái)E%Aâ\x001b=MY\x000bz¤ÿoÀT\x0015LõMÂ´åO'AÇß·_O,uf%YÝÜ|\x0014,ñVjáG%ãÝ:óùü¦\x0007\x000bhéªì=»¸Ú{¾Z¯/ßm=EhY\x0011!+ÑSYê^\x0015¸½á¡Ó|}æ½ç\x0007ggÇ\x0013Fg\x0003
'Ó£\x0011\x0014øÉ:G²
\x00113&i\x0019\x001bå\x001aw@uyùüOa~1=
ªÛ½ÓõÝö\x0000Ã²÷\x0000@¥KD\x00154E\x0002ªÑÌWAõzïôìÍTDQ@iLÂ§G\x001b(lÍI\x0017)\x0015M»Ú (å)\x001eq°4²\x0018¥GãI)ªPâ¬@îÀ\x0012¹&
\x001f`´%¶\x0001Ã/ç?\x001f\x0012$å\x000e\x0018ô¬ÙAÞ\x001f:)¤êê\x0007å±t\x001eM  ö£}å:JÍ'\x0005Á0Ýt5ê}nÁäôhÂdD D$Fh¦ÂBtÁ)\x000c1"½j\x0000\x0015PÙ¥G\x0013(\x0007¥Ô\x001c²\x000b$]ocH\x0010ÍäcÈµ~;¤?¢\x000b\x0015U9'CsæB¹\x0011\x000bC\x000b&¬/¤G\x001b&Ü}b
¦Ü
nq=Æ\x0002 d¢$ÉÏ&TJ:dO¨¢£!\x0018+¸\x0002'´\x001aõ·6¡²	UëRðgç\x0011c#ÁþVD%5+\x0004­G¬¹
¨2ÉBz¶¡Âê9	$§\x0006¾êFøFì\x0005OºVòëúr\x00108\x001f}^]¿ûõær½Ojq\x0004d¼!8j#9\x0018 F­Ê<ìH\x0004^\x001d¼<üñôøl\x0013¢N¶8Þ|ø\x0012Ä\x0017ÇìêGï®îoYÀíÕ*	`N[z\x0019,QzCSj\x001a°=L\x001c\x001d¿\x001e¦ý¶Âb\x0002ÁFX&Óç\x0013_\x000bb\x0002-CUg9^°\x000b¨÷¿ÙÕ¯×©\x0017äÌÌí\x001e.)\]]^¬ÈÌ÷\x0004Àpm¦¡W1ä6\x0019\x0004²(Lef^ïáVÂã£³É
0ÞU\x00070ÏQ4ÈêÚ3À\x0002å«)­/Ú,7f\x0000ºÒÑ\x0002\x0010ýcC\x0000Iá\x0003À\aD|Ó9ÉÝái§»àECþ°¸Ã;Ò¥ü$à\x001bõ9ì\x0004\x0010L¯ ÷æ\x0007ß©{}__|Z­·g¹\O'¬ÁY4Úl\x0016ÊZ87A\x0015=\ùúèÅÁÙ³-;I	ª\x0019B5]Pc}\x0007n\x001aÑâzÏïÎNLÍõ uC¤®\x000f©àS¢6\x0004Õyb4rf±\x0007j\x0018B
]PÁ\x0007×ÕÃØÍZ@Ë»\x0018\x0013êZr5	jÞ\x0011ØÕDj°&É\x000fa5¼§M-s\x0003d%V²O®L¡s1¸õ®¡ñ+éä\x0004YE\x000fÖJ®d`AlOu:£,-Á\x0006¬\§Ã\x0019ÆE°V%ûDK\x0015% Aã+:WÅ«\x0004m`éìÁZì-*\x001a	«×¼^ÆË²Ûº\x0017º°ªJ¶TlÂ|ªm`v\x001f/xÃ¥ °ëZ]WÕu]CðDäi¬t'\x000e	0µ\x0013ô÷=X«ëªº®k0Ü|`gÊ\x0015¤3$>c\\x0002³\x0008Öêºª®ë\x001a\à+ °ñVÄ±\x0000V]]WÝu]Ð¼Í\x0016y]é\x000eXï\x0018« !èÁZ\x0002Ýe
Òf®P°\x0012_¾uÁ\x0016¬È®dKwÉ\x00162÷ÒF¬t®\x0004UÅ\x0002u\x0011ÇEW¢¥»DË¤þ\x0019ª§cµÞ.|\x0005*ÑÒ]¢åCáüWmón\x0011\x000fÛTbeºÄÊC\Ì_ßR>Ýê_\x0018i%T¦O¨p2q\x0003Õ\x0002 Ì?"\x001dó\x0008õ@­Ã>ò]\x0004N·¡,\x0006µ)Ó'S/\x000e F*>ÖJ¦LL\x0015ý¿ùüª¨ÿQb¢\x000b§­dÊöÉ\x0014²Q³rÈÉ Ò&0[tê2P+¡²]B\x0005Wuc©</[5Ü*P\x0017ùü¶*Û%UiG"¬ÜÏd,R5\x001a\x0014ëZIí*ÜÉo©>p
SÎt4\x001bØ\x0007´\x0012)Û%RàëñZ3äß\x000b´¸)Ré\x0012±.\x0012\x0008ºJ¬\XÁP=a¥\x0015q%Sa­äÊõÉ\x000eØ¹[°æ;È\x0002ÅZ§®ú.«ôû®\x0015Ý\x0000ã7H\x0017qª|u\x0003|×
°1R¥\x0016b+©\x0004
v×/«\x0001|u\x0001|×\x0005°)
Ò©zÚb-ZøX+Åê»\x0014«õ¡øªp¬¼\x0019÷\x0016ñ¹.¢°|uY}×eµ Yíæ
xÚwÃ\x0005u\x0011Á
Õu
}×Õ\x0004\x001a¸\x0007¬&)rºÜe2¡º\x0003¡ï\x000eÂ´\x0005mÙRV´Å¨~×µº\x0003¡ë\x000eh¶\x0018°\x0006Þ¢+£ãsõËÄ¡N¶w\x0019Xp¥©\x0015Öâ*$Ú<(Ë¾n\x00139×XÝ×Øu_u,[ie\x001dñ}S´rP Vê5v©Wí$aYÝ\x000c´\x0014N³ßj'Èâz V\x0015»$KiîÙNP=íâà÷¸4n\x0011¨`Å¾ÜåÿN>P>(·tÕ[¬Õ\x0006	,²q\x0010§¦àc%ü"×UÙ.\x0002k{NVâÚÌ@Å!EkÆ´gÑrS+\x0016»¢×T½®#XüIW\x0008\x000eÌ ¥õ	¥B\x0004¯´íz8NÄ`\x000cJ|àyúØ(í¹\x001duUtV	\x001eBV®\x0013rðÖ\x000ek!y\x000f\x000e\x0004eìÌÄ	bâ®ÒÖCÄ\x0010ó÷!J0%?2ÙRñXrÓú\x0011\x001bS§0º\x0016½g:\x0007H©\x0005Ã\x0017YzÍá¸_&Ç	7ùîbýà&ãO:n²ð¼\
ÙÓ)Ñ­¤*1YeÞ±Ìf·ùAáµËí.W«ë'Û]´Ð\x001e§Ý°ÝÅ\x0003²´\x0001\x0010âµ\x000c\x0013­v©ÝåIz\x0008S7ÃTØÅ»­¼9q\x0000(EÎ\x001d\x0002Êñ¢\x001efÒt Ô.cC\x0015\x0019#8Ô\x0012¦Fnb\x000fD;h; ÚHé"éáêÜ\x001e\x0016È\x0001zd\x0015z`ú!Lß\x0001\x0013\x000c\x0016]Kç·'\x0006nÂRb2®\x0011e\x0018¢\x000cí(tÄ\x0019'=òNäN6¢$EÙ\x001cSoE\x0019(cÇYÊ@ë¥s1÷
ÃYjO­m³Q^¡¬DÏaZT?ùû}ê[\x000fSòm=0k}Ù®0éx\x0000&å°=L°\x0000Ñ®\x001eªÂ©:p*úä\x0002
6I__²ÄaVZ]v¨õ`¸  \x001dv]ä.ZÔoÂ¹­vgZ\x001dz=]Í|\x0016¾¹s,è`\x001bÃzpVº]v(÷`\x0004\x0005TÒ!?\x0012\x001f§âãtj\x0001$+å.;´{\x0000p9M\x0001qSd½©UàÛ9M¶Ù\x0008³Òî²C½'§|#ÚíÈë`ßÈLSD6â¬ô»ìPð\x00019;òí\x0004ëé«kêX~ä®;\x001fÁ¨*µ©:Ô¦Å\x0008Ya±¿
Aº¨véªÞ
c¥T6òQÒ¼$èG]ô	#­s~ªu~7«\x001e\x0019\x0016sJ\x000b¨|îO÷Â3È0M¿Ør)å¦íÌy!\x0007mÒFúè¤ã\x001e*¼ìjÊÑøiw$\x0007a&\x0005A\x000fÚþwõ\x0010©9Mz§3Ñ*ò·Ñý\x0004s:Ãª\x001báu\x0015­á\x000f\x0012}ÄúæÓÅõêýÅÞÙýåííÅê\x001eG¾¿¹¿ýíþbë(\x0015\x0011/BÒNÊxÞ*\x0015eÈàá&·ÏN_\x001c½<xv´wv~üúõÑÁ9Î\x0014}zþúßÎ¶\x000c1|5¯æÂ×Ô\x000c«_ô\x0012àó=à\x000b_\x000fáëð-W±	\x001að=þéô>|3Dof¢7êZpø2*Hr\x0013\x0019ýp.|;ogÂ²+8\x0003MúÑ[v\x001bãês.|7ïfÂÇR"]\x001d¦{EçÜóá»¥ï\x001f¢÷sÑ+Zu¦¬õÚBÚ&bº\x0012Ø%µ,ü0\x001fæÞ\x001d·\x0011\½|w\x0002_ý19Þ\øq\x0008?Î\Ã\x001eùô%-Y.\x0006>|1bÁ¾\x0004öÙfYðáo9jªPX\x0003vtú^Z>ýÑxÅ\üµÍktUÜ§Ó\x000fAZßyÇw<A?\x0017~eså<£\x000b~Ê½ÂÊRÜ»\x0001½\x001cS¨ÌD_\9Óæ\x0006,¿gÑEÂ¼a':rÏ#r».\x000c¿²¹rÑ¿¥©¡pd8âtá\x0018\x0002çÂ¯kµBÀÝ\x0004ßmô¾	|÷G\x0003gsáWj_ÎÕûÎ\x0016³å<
ÌÙ\x0012á
\x001d3ñ«Jsªy\x00134B"¬øyËmÄö_Öü£ÜÎ\üµ»?Óß\x0007·¦X-KVKû¢7GòYà\x0007SÙß\x0014bîñkªó&§ÇÒé\x0007#Ó³ÐíÊØÊãÄ\x001f Ç	8¯.¾¬Öï÷]\_Þî½Z}¾ÜN`@ßSJÝXÜ,É\x0006£aFáGëª\x0000ÞÉÑÏ\x0007gÏ\x0000ëËã×{¯\x000e^\x001d¿|\x001ak\x0018b
=X­RÄÂÁPê\x0008Ãâc.ø*|ÓX'Ó/\x000c´äÚ\x0012PÌµu*\x0016Ðó\x000el\x0010Ì>­c\x001a\x001d\x0008]\x001f¶­ô\x001dkQ 	-*\x000e´\x0018É%¨Ê3U§d\x0006z\x0011üh8`\x001aê»ÕûÕíÝúQ¨e<(AÅ&Þëª
Y\x0018¸\x000eVÉK-7Ù{ýÐBö\x001d¬«\x000eÖõ\x001d,\x000f´¬Ó¤f\x0016.CÉv@kGìº}h}Ö÷¡NÓòX8Û@\x0001RkÏG;;ÁÚ
¬í\x0003\x001bÔ~,÷À\x0013VÇ\x000còÞeîA¨N6t¬´\x0002×'ìçk \x0015µ3\x000bðïQ²±\x0002\x001b;/­\x0008û5ªHØÃF.¬²Ö\²Su!á'} RÃp0¡Ù|ÙÇÜ	·6\x000bªÏ.(Húòáú\â@¸Ì\x0002éÝh}S\x001f\W[üm\x000f\d\x0016à<!q\x0001\x0008£\x001d54v¡U²Ò\x0008øÛ>´/.vZ\x0018BË\x0004!qrÍt\x000fÔ\x0003Ûym5È¤[¦H3T[ìÂÌS\x0007«k´ºSÈ ¬ÓdÆ ÄÈQ©4QÊ¢l\x001fz¶}pk3¦:í\x0018\x0012]ä\x0006gÜõB¹Ø,\x001e-bu5\Ùg\x001c¡t\x001ddÓ2\x0014*àÆQÔÙqok£«:­®ÆI\x000c:Z¡i\\x0016fOÐ¶Ël¨Ñ>´Æ0£H2»63öÍnb´µ\x000b¬®Lw
\x0019x4åÖÂÑ¬l\x001dÏæ,æ+â
nçÙ\x0002\\x0015%Ë#å\x0008o­\x001f±_ôÁ55\Ó	×'N;Kp!\x0008ßQ=¢\x000fl}ouï½uÆõÓÙæ²­ô|ÄÖÑ6Öhc'Ú ©È\x000chÃ>ÕåÞúQ§N\x0017Z#+1Ãßö E&\x0016÷Ö\x0012¹7E'z#úàÚ\x001a®í«\x000cµr\x0018LÇ;Ú\x0005Á<~`ËsL\x001dïÎ×jâ\x000c·7æ\x0002Ü\x0011\x0017g\x001fÜÚNsf­CrÉìØxÝÈ²86aÄØ\x0007·4Ó)iÖ9"uLÈw7è\x0012GÆ\x001dm\x0015ÕMÀßvaÅÉ"Ò
:ìg~\x0004\x00196®ÂhO×ÉÚÚøÚNã\x000b°h5Sº\x0008¹ÙA\x0006ð\x0014ù"E\x000c­ÅÌvS÷çáá\x001bá\x001f.»ÈéºZçºN«B"é\4mÙDDÞ\x0017ä2%W+\x0005×©\x0014¼ååÅp-4Mñ)\x0008Ñ\x0019®\x001d
\x0016ôÁ­³5®3]]¹d\x0008p
o³ø²\x0000îhZ£\x000b®\x0017uÚNtnlÔt\x00170wÏpQC,\x0001·Î)øÎ\x0002¼\x0005Jä+^E\x0001§»;\x001aÙéû )Úywâ
ÌIG(Ë\x001bPDð#êä>¸õÝõw7 \x0011\x0005ÁÅ!³¼\x0012dìo\x0008Ëø¡¾»¡óî\x0006äø Ë\x00000.®þ \x0002\x001cu\x0017ôÁU5\Õ	7\x0008\x001aÅ±Ù\x0002W\x0006ÍE¨ÑPz\x001fÜÚÕ
®n\x0004w\fp\x0001×\x0018ä\x0019í½Ó]Fïâzâ!\×wº1×õ2\G¤J
Â\x001eº»Q,ãáZ3NÍ\x0015É@§\x001by7;.çB¢\x001euµûáAµ¤³\­§äÞ VÞóE¤\x0016bíéÆNO\x0017ç\x0010i«\x000bnßäEÀ\x0004Wø\x0014úàÖ®nìtu#|}Kh%\x0011*¤©iF»¦\x0006k:ÁzK+\x0014R\x001d=wñ*ÜBÆ*,ÌÏéÇ:í\x001cûÒÎVXÏkÅ\x001b0À(\x0003ÈédÍ2YòX\x000bYì\x00132\x000b\x001eRÑ_Q!©yk%K^&TuN,öåÄàt#n\x001b¯\x001d»
Fæ\x000f¯f7È\x0007í\x0014é÷]`£dÜ@$\x0015ÊxÞ0\x001fÍhh±çl¥0\x000fðö\x0005K\x0010^D6\x000e\x0006\x0010ï"¶L>èªH¿ïÂ+\x0014!\x001c²Åç ÂDN.Äy]\x0000o·É«zðjÉÉ\x0010<ßÜd¥¬b?7Ñ(H'^÷\x0000oWS¸=Û\x0010^É+ìFØZæ>Dÿ\x0000¯ïÃkyÓñ¸Ü-«^\x000b¦ðwtâ
\x000fðö5²IÍ\x0004ß\x0007A»\x0004á>p\x001cavôÅ\x001b\x001fÀíêZø_;^Y;dé÷ßòõB>ÀÛU\x0001\x0006õà1ÏW°)ÆEEý.áAJYÇé÷}÷¡ÄÁ^Aë\x0004Gjãñ>¼\x000fÌì5oÞsÊK&gS6(Yð.\x0011·\x0003¾\x0007÷ÁtÞ\x00189\x0003é­¦}yÊÈ÷!:ñª\x0007x»2á|V2ÝÀçkÊù.Ò'\x0004øô\x0003¼º\x0013¯¡\x0010È+Kë$õ¡ô\x0011X[»à*[\x001bþ¾«íY[v}6´àN9Kl\Â¦Ñz¥m0'½8üY\x000fj©8·ç-¯¢TNñjá\x0018Gó£½\x0015 °±
Ô:\x0015\x00027ãÌu _*+n©Æí¨U7è ÛÙÀU@>¿ôUsÔ$%E\x0018!\x000eÝ­÷¥
¯ó(=2/¤\x0010 Ü
<å
]\x001b2þä[=e/ìÃSÆJKç1ÿo\x0015[ð»_~øÍ¶ÖÚVt\x0005øï*ë÷juµw²ºþpñå	¬Î+±:
¿Rà1\x0011Q&î"#·(èW\x0007ç'{'\x0007/\x001fý¼\x000b^=Ä«»ñrÉÐi¡²Úø<%©öqÿ¸\x0006<M)hÍ\x0010­éE\x000b7×ññJò±wOwÄ\x0003Ý}ºv×öâu29-#\x0013ÏxÅX¿\x0011¯\x001bâux]4T\x0007Àf\x0016nhr\x0001ïöÓF¼a7ôâõ.÷N\x0003\IëBÓ¡\x0012\¹°Å!ÜØ{\x001d'gÞa×·¦Ý[Ì
\x000eÂ6âYë\x0005¼YÆ<Eï\x0001cÿ´'Ä\x00170\x0004ê\x0001À[Ó\x001b\x0001WêWöê_$Ù£\x001bQ²Æ0*\-ÿ+&{UÓ\x0015°B\x0016)ZÇáXÿ\x0011¯M7àJEÈn\x001d¡\x0005Í\x0019p¹\x0012àº1àÑhk7`_\x0001öÝF£\	)h¹;d\x001a\x0013D-±Ø¨ìÖjØ¹A\x0007,¨UÝ@Àçø·Ôå\x001a\x0001WjMöê5g#\x0003\x000e±ì\x0014
£\x0000À£­½U¥ÖT·Z\x0003?B\x0012`IÑ\x0000°¦zÒÞ>î\x000b7\x0002\x0015`Ù	ØFD\x001cníÊ£®ûªá§[Z\x0012\x001bñÖ^p¯\x001a¶XýVt%ßad\x000e.wx1Ä\x001f¬z\x001daë
îá5± +\x001dÛæmó,+Ë¡z-õ*up-ïIVas·g6"®¼aÕë\x000eã~\x001cI\x0016\x0010[UÎx1±«lêµuH)È8çÄf\x0002Ì|ýpÄ£\x0013Ý+c§z\x001dNkg\x000e\x00078bÍËÞòä\x0013k³e¾¸\x0011qeíT¯µKíë¤*¼Êù\x001fDm¬Û¶tU6\x0002®¬êµv\x0016B
AÂD: D
ð16Àº²vº×ÚY­h³S(=ïÉP±¥\x0014®Ìî5wHÓG\x0018û¿hC°¬'ÌböNWöNwÛ;¤Í&ÂÉ¢åÆzìFy\x0012q÷éµwHä(	±4ch¤S\x001cxèÅì®ìî¶w\x0018\x0012b\x001b(\x001fod,ªm[é¹\x0011qeït¯½\x0003½=ù\x0015õzÀÝõ®ñRù\x0014]\x0019<Ýkð\x000cøï\x0010ã¦Ð¬*¤E¹Øÿ»\x0011W\x0006O÷\x001a<»wC9ãÜÿc÷åò)teït¯½ÃiYIöÎJÞk]|Ä[*Ð+§{
\x000ez(ªÈ]­pî\x0011ë-°6Ä¦²x¦×âé\x0018÷m9bòåáÔåº\x0014¦2x¦×àiä§Ka\x0004Õ¡àD1ü»R\x0014¦2x¦×àéÀºpÄ,	+Þ2]Ò¸2x¦×à))ØÏÄT¦Î\x001bÙ\x0002ÄuËÜRnD\\x0017;z
PßÉ£Yv\x001e3ÞBpÕ¸2x¦×à)ÜdÄ \x001e@ÓÁL\x0010îC^\x0008qeðL¯ÁÓ8
Ãº-àq§3²hãÅ
S\x0019<Ókð$¨
O5\x001a-\x0011@û\x0010\x000c\x0017Á¶ò4"®,éµxXJ2\x001bu\x0019¬u¢è[:b2Å3½\x0016OZ#Õé\x0001¢ÎGìYðrKÙ\x000f[Ù\x000fÛk?DP¬µ5ä\x0006ýÁù6£·´á5"®Ô±íUÇ`*hO. ¨5\x0012bÍ¦Ñ[&{\x001a\x0011WêØöªãä^r¥F\x0011¿\x0018øF\}Öa´ï£\x001bq]}îUÇB3}6\ã@q4 gWÓèÅ\x0002[)7Û«Ü\x00046áiRnÚuµ+;^Áy^ìVTªÂöª
urY:>ÈäÙhY\x001do!hi\x0003ì*ßØõúÆ"\x001aÎiê ¨ãC»H\x001dçÊØÅ\x0004ÏUÊÍu+7\x000cñ¸§È×6ø#.èvwìz½cC«Ô§\x0012Êö_ç\x0004w&¸-H+uì:Õ±ÁâÞ·ì¹\x00056 ÖÀß/u:v½ê\x0018<À"xÈ$A&O\x001b¾Ç	f\x0019Ä:v½êX¸@$\x0011ø\x000cFN`-Ö
äên ^ç\x0018·½R½\x0006®\x00051¢ý`\x001bm\x0016ëfs«éz]M¡Â~ÜøA¤Ûd\x0001¬\x0017ó]e>\·§i,\x0017\x00134Äx6\x001f1ø\x0014|±(½\x000cb_Ù\x000fßm?dI\x0011¢oìI·	Ág¬\x0016ËUøÊ~ø^ûá\x000csVÜ	*Øhob	üJUøÊ|ønó!b1xZÑ
\x0018¼ÒØ&;âJ\x0019ûne\x000cçÊND\x0001¨­÷|Åbç+Ýæ;uM³ï®´\x0005åj¶n\x000eZ.\x001e.ã<aÝÆÝ*¤\x001eM\x0005ÚÎZN\x00152pµ\¦{\x0008ÜõãvÁÒºD8pK}cF	E0Û°TÏÍCØjÆyãF\J^xî7ZsG7ø\x001eKi\x000f\x0011\x001eâ\x000e3`#\x0011	é<Þ@apsUñ\x0017k=6£ëÝ\x000fÛ\x000bÇ~¨V\x0011(]\x0013Ãýr±U¨Ñ-\x0001ÛD®B¡þ\x0004;rÅ\x0001pÏ5ãÈÑpåª´\x0017mî]ýÏþ×ÁíçËw[(\x001dóx²äC)Ç\5\x0013¥¼ºrïdïàõ«ãÃ§\x0001ª!@Õ\x000eÐò<(µÌ!ä44u¥Í¨]³\x0015\x001eâÓÍøBî|Ü\x0013\x0004.1¯ÐÚ<¬Vf\x0008Ð´\x0002\x000cÑ1Q
\x001e $ò$Ã#z<RÞ
Ð\x000e\x0001ÚfÁ\x00109»Ð\^¥\x0014´b1\x0013\x001bâsÍø| b\x001c\x0000\x000cec\x000fpÔ¼Ø
0\x000c\x0001fNS\x000b6XM,o|×sàLÁ<e| +\x0019ÑÐ\x0002BS\x0010jÙ¼\x0003tãôéÝ\x0011VZF6«\x0000\x001aø^áÆ1Å\x000cL\x000c ÇëáZ\x0011Vb,Ûå\x0018\x0010JR\x0010så\x000e\x001dDH\x0000Õ¨êÞ
°\x0012\x0013Ù.'&2\x0017\x0004Üh6%\x0012÷fr® ËJNd» £5ûüYLÆ.çøö¢²Åøïªøô'øÅíÞóûÛ÷\x0017Û#\x0011ç\x0015¹<ÆâZé\x001c;ÉX\x001a·u+ü\x0004¿x½÷üüèõ³£§áª!\Õ\x0007\x0017\x0014
kG«\x001cs¢zðy`wË\x0000H\x001b\=«;O×ú2Å
!_.¢k;øt\x001f;Úà!\Óyºð·\x0012VÁ)M:,\x0013%o[	ÓÕ\x000e±ÚÞ£\x0015eáN\x0014Ä\x001fÄÿvK´
®\x001bÂu}pUpT[B29Ìa¥Óe«¾÷¿
¬\x001fõgk\x0004/°rßå
´´L$\x0008Gûx<Ñ6\x000cÑÎ£õùîpKrnU^\x0014®÷m¤ampã\x0010nì<\åÊæ¸Âw§%§Pàt·§7Á-~T6\x0010¢óxÚ§½|Æ{lMü\x0019o®Ù2öÜ\x0006·¶g½\x0006M:ê08·³Rmîî\x0016ï6¸=\x0006MYÃ\x000crÆ\x000b¦rÜó*ü¶±6¼A½\x0016
³Ã¾\x001c¯'&­,ç»Ôí­,ì4iØ7AÛl\x000bh1Òù:¶À~\x001b»d\x001bÞÊªÉ^³¶	ðñ|©\x0007A
WÌÚ\x0016FÁ6¼Y½vMÍ\x0015\x0006\x001dí3¬Í¼Zì|+Ë&;ME\x0001>_Ã\x0005$äû£ãK[eÚd¯mC'7k3\"ÅêÁ°¸y¹¥Óµ
oeÛd§qÃm\x001b¼Å\x0017b\x001eû\x0003\x0014\x0001w!í *Û¦zm*é>cÃA!-\x0010®XJ©Ê¶©NÛf='zÓéZº¼>`m\x000b?_\x001bÞ:Xë5np¼´ÈÕhAÓ\x0006p¾¼QÎÅ-ô9mx+ã¦:-Í\x0011\x0017\x0016wä\x0006+\x0016\x00125UY6ÕkÙp¾'ÁÅ.¢\x0019xe³Kª2lªÓ°á*Ì¢x=zéxKb8lQk[Ù5Õm×
S®öã\x0015DêÌ\x00162õ6¼]S½vMùÛ\x001b¨t¥ÁéãLÝÂÛÐ·2lªÛ°I^Û§¥Fr³3t¾z1UV\x00196ÕkØäà|#è\x0014´ðù.¤ÊteÙt·e\x0013´¢\x001e\x0002ËÁñ\x001a>^õx¾
neÙt¯e\x0000×ã%qQåA[¶áµá­,î¶lbßäë:§øxétÕ)º6´u\x0016²×®	Í\x001cvÈòÝ\x0018L±l[FyÚàVM÷Z6	7L\x001bxe2\x000e9÷Ü¶>ì6¼iÓ¦Í»@xñ|=¯wE÷náqmÃ[Ù6ÝkÛà|Y÷jYbbí©ìÄ9Û6¼mÓ¶ÍDQ®¯äÔit¡\_³ë +S¡;M\x0005î!¥\x0015¯¯CÙ8\x0008x\x0017º¾¦Ò½¦S÷\x001a_bLÌ>\x0010Ës,\x001bt\x0001ïBÉiSi3Ó©Í0\x0013\x000b\")F\x0016¸KeÌL¥\x001dL¯vp\x000b\x0015êå[Å\x0011ïB\x0019\x001dSIé6\x001c½'¸·ÇDe7p\x0017Rf¦6Ó+m Ìx¡2ÄAd,\x0002\x0013\x0011 ÝB·×VÒf{¥M0õ\x0005à\x0015ì\x0005§\x000bÞ¥´­¤ÍvJ\x001bN³{bHö÷Ý\x0004ëYmÛ×Õ·.\x000bvë"áuq?dõÒÒ\x0019¯ZJ=ØJÜl§¸éPZâ¬3\x0010S\x0010^Qðn¡FnÃ[Éí7í#ïoC*û..\x0005\x0016¹ïë*ysò¦cô\x0003h6MúA\x0015çlËÜd\x001bÜJÜ\¯¸Á¥jÅ!U+ËÚ¥ªm®6×+mNóO¤Ò¢ôØ¤\x001dòa\x0019¼´¹^i³¥»Î\x001aU¤M¸r¼KI«¤ÍõJ\x001bÒ¨1?}Yà\x0015(¶·°4áõ´ù^i3~¦Ñuå£æjÅRÅ\x0015_Éï5¸\x0001ÐªÈ}>ð¶1¿þ¶
o%l¾WØtYìgaÓæ(ËÁ*\x0006ùº¤WØTàõ<>£^-ÏÍûT¯DÍ÷\x001a2|Ò¡\x0013³aóÅ\x0010{\x001b\x0017r$C%j¡SÔ°úH\x000cø<ðjîÜóm¡¶Ð)mHÅJY\x0012\x0013ü~È¤W¼V×Û-S
mx+i\x000bÒ\x001d[J¯\x0010Ñ»ð cË,\x0015WJØB§°Ñ¥9C\\x0016ù\x000cËW~Ü7Þ·\x0012·Ð)n
	ò#7¼ÿÕ£J\x0019\x000bÁ´Å^ió¢ôïÁ/©cÛE^=çõBQP¬-ö
³Ä,dsT\x0007¸ªî\x0016\x0012Ë6¼°Å^a³)TËx%Ñ(\x0007a1·,Un´Å^i³ft\x0003îÜµUànYì×\x0006·n9ì\x00156\x0013\x000bÒ\x0018ì§ëà\x0015Û¶q³|\x001f^ù )]ô\x001bÀ
Ü÷ÂäÊ9öÓ½ØÂ\x0013Ò\x0006¸n\x0013½\x0002g\x0004F\x001bÞ\x0004ë\\x00118±Ðu÷4þ¶\x000f0\x0013×1È{ÃqìLº¸\x0017«
pÝ¸%zEN{^îgp¹\x001fuY]Ø2\x000bÛ\x0006¸n\x0012½BÛ4IèD@ß\x0000s\x000b\x0001ªE\x0000?ìí\x0015:íÐ°¥º\x0010vÀð~?Ná~\x0000×B×Û\x000b	É(ë°)dYÏB»e¬»1µ>×åôz=°Û\x0002Fò\x0018.\x0010i\x001d¥á$u\x000bY\x000f½ÙÆ°ëEh
°uiõDØjôB2ç\x0016b`Ë`M5Ù?ÀÉ¦ãO\x0001ÊÅÞóõÿÏÜÛekrÜV¢S9#8+\x0000ÄïòS,KåÅ?\x0017Yv·_¼JbÉ®»(R]$ûvû©§qGpÛãÐLîHn \x0013LÌSõ!ãk-½ØÔ-í\x000f\x0019±7"\x0002Øø7þ_\x001f~þ÷ÿûS&\x000bý¤)a^ü\x0016Öb¹m
\x0004ÃÕÉ«/¿éÿøòá·/¿~ý[þ_¯¿ýÝ?lêâÅ=^¼7\x000fû1îh[ïÒøéEÚ¸\x0001\x000f%<\x0001Ó\x001e0]\x0006\x001c%ië\x0001®P\x00050(`À§Ûï2à¸\x0007\x001c'VDXûû\x0003\x001b!'\x0001¬¾\x0004@ÛÕËÓ\x001epº
8\x0015p_\x0012Y«øöZÄÁà2à¼\x0007/\x0003ÖÇ\x001cP{qç\x0017ðÝ\x0002\öxËU¼qX6ñ·çÃcE<¼Ëë\x001ep½\x000cX'iæ´¿ÇÙ
Þ|86_ÆÛöxÛ\x0004Þ$ë¡\x000cNËÓèp%|\x0015/XÑ¸¬\x001a={×\x0015AIUcØ\x0003Ï½\x0013`CÂp¹lõ\x0012bWº&,ÜÕZ\x0010§ü4¿Ø\x001a\f5ÈÛ\x001anj\x0002\x0004c\x0011ß$À\x0004\fÕ£i\x0001«\x000cV%ö%\x0014Àå`yp\x0019±ÙupyÛñüAYÅ¹\x0004#\x0006E|H1¯"F³ïðò¾ã©h\x0012ã.ÓY\x0016\x0005\x0010\x001f¦U\\x0006lö\x001d^ÞwüÀ%!æ\x0012[Ñæ4\x0016ñ!\x001bö\x0002æäÚ¤Ãü\x00075ÝùæíÏ¿¼ûõÃG1.Ó\x0007×\x0004-ä ÔÀ×­«\x001a\x00033\x000eò»o^\x001a\x0016îa¡\x0007\x0016·. àÒÅÏS¢³à:sF¸\x0019\x0016ía\x0007V\x0000q,î°@AE\x001d.ÉÑ
WÚãJ\x000e\¹\x0011ÇhÅRÂÀ÷bã3NÅ+ïqeW¼ÔE»ãÊâ\x001d\x0011¹8Z?ã\x0003ÇÍ¸Ê\x001eWñÄûa\x0014\x0017Éíl:ºãuf¡s3°º\x0007V]\x001fR\x001f\x0011:°"Ùf\ÌÆ5`göW7\x0003k{`Í\x0003¬Tq\x0001Y"&3¯"JlØ¡Þ\x0003l\x0007¼\x0010Xp!Ó·´H¯\x0000\x001b\x0001;´\x0005¸pYbõ0+û¦O\x0019uºv\x00049JrÄÎ\nFf¸\x0015<äÊÞ{$ÈJÖ914EÖN\x001d¸nFfè\x0015<üs\ë¸wd\x000c»ÍðØ6\x0012y\x0001\x0016=Àú!%\x0008að¥L8-UÕtævt32Ãüà¢þ~Æ[ÛzÌ\±tÂöêìÐèBf¸\x001f<äÏÎ ¢ÄÖblË^\x001bìpYìBfØ\x001f\ô\x000fú\x00148÷\x0001L\x0014\x0007°Ã\x0018\x0018\x00170Ãþà¢ÿ@23uÙ:H6½<ô]¸\x0019ú\x0007\x0017ÿ³3±d>\x0005Ø0aA»
0Ã³hø\x001f=üÏ
å(ü¿:ã-È\x0006Á\x000ci Q\x0000ô(@ªE^K
Pdð4àØ\x0007\x000bx\x00172]{\x0014ë´5_¬êq\x0018Ç5gÙ¡XÁÌ(\x0000z\x0014 "î\x0016=fq\x0006ç \x0012³»\x000b\x0000ôH\x0000¿\x0014­\x0001ú)G?_\x000fØaÆ\x000báôðêbËðÔ5/¡X4ä\x001eòçZTåå-v¥ÜqMeØhÈ\x001f=äÎÂ\x0017:4¹@\x001d|1Ì°?zØKLîÊª§%ºö)LåehØ\x001f=ìúª/tDoª\x001b_Ìä²dØ\ì\x000fí1IúÓÏNuÕ%DyÃë1;Ìp!3ìO.ö§ÌE\x001ekÌtÈ
O\x001e1;µw¼\x0019ar±?DM\x0019!DqÃÃ@\x0016\x0008\x000e
F.dözÅÅþ¨Ïo=fc²2â\x0016³©\x000b\x00162ìO.ö\x000f¨÷d-ª_9[\x001eê2;µ¥¾\x0019árñPÃ\x001e²&Í\x001dæÿÄÇ	dF\x0002È#\x0001Rs¼Æ,Ë}m&å¼\x001dÙÁÆÎÌH\x0000y$ \x001fA¤»#CµC¦jN¼'\x0019	 \x0004DfW]gn\x0017d5\x000cdª6\x00172#\x0001äØ9LØ]ÇäcV\x001a\x001fóÔVüV`Ñ(@ô(ÀbÚVÍ@S3ÈR\x0018ÚÙl*ÿF\x0001¢G\x0001"ß\x0000³½ïËB\x0001EÆm\x0013È\x0002D\x0002ÄÔä\x0005FyQ±1a*ûÿ£ÿcRO\x001e±ÊS9\x0017`1º^ßÌðôð?\x0017Å®czÈÒG\x001f5%º\x0000f£f©HÃZGV¥ ".Wþlf£¡Ùè¢Ù¾¶ä\x0019@bs\x0010Ã8Ð±\x0006ÚÌYô\x0019åñÓOzÍÎÆôlj\x0003$CfÉCfÜK\x001d\x0005Wà$mXÐo9÷\x001e\x000c%\x000f\x0011W/¯Àz^+·!¯\x001c°\x0014Ì\x00003T<TF|ý£¤K$r3¨|ÉC÷®\x000bá²äá2\x001e+¼¶Ûô|\x001bùÂ¯¿mdñPì\x0002fß
=\x0019cÏ¦¥é®G¬È\x001aû'IÈfø"\x0019&K\x001e&#¶\x0019Ùv¥$?a¼\x0016>3ºäfdÉÉx nÎã[ÆÕ´²ÅFãcÎ0Y2	cò$l\x0016E\x0008õ^6PÕêÔ23\x001c<\x001cü#_3Fu¶\x001f5Ì=fSZ
Éf\x0017É¦¤e¿=ÓÑóoÀ\x0002Ìfb
Ëf\x000fË"\x0018íôu\x0001õ%\x000f=\x0014å¸\x0019Í.ZCÖcVÅ\x00157-g6~\x00172eOfÆ5ÿáví"Ò4Bv(\x000br\x00013<=<\x000b£ßrÑÌºVVöÉËl*d¶*ÃC´8\x001c[zÈ*ÛÔ­
 ;3áLú
Ïf\x000fÏ\x0002s²YÑà¥©¹4#\x001bÍ\x001eE>ËéÎlZUÛ0j1þgC³ÙC³ü\x0001\x0003U¶â*\x0005¶E6«\x0018-\x001eEöåT6JkÏÕ²âJ0³-áØâáX¾jmäØºÆÂPÌ©
b(¶x(½Çz"´7Öí\x001ecfO\x0016Ç\x0016O\x001e»\øk¼Ò\x0018¨[Ç
ûÑÞÉÌ0ñ0ÿï\x0016Ð´Ì)^KX\x0017\x001f[Í0fØ¢\x0018ê/\x001eêïY°Ì\x0014XÔrõ
¡Ñ'Ç»rj\x0019ê/\x001eê\x001c¶SI\x000fßºøu¬Øì©¤Ø<\x000fõó(;ÈÛÇ\·eÏo·\x0014{j\x0019ê/\x001eê\x0004°ELBV\x0012Þ'dúú{#\x0006		¸k=¤¦µo<§{\x0002Y5ä_=äÏ>Ç\x0006Q¥ÔFÌâLî_
ûW\x0007û§Æ] "´'åq'ÕÂÌÎ¬þ«þ\1\x000f!©?%\x001böó¹7#3
P\x001d
Zç\x000c©JZuâHR§óþ±\x000fý#.dF\x0001ªG\x0001úJx¬ãð+]\x0017¹i\x0019/óÇ\x000c0#\x0000Õ!\x0000©õ¬L·fKêeÆÎ«1¨ÿ«ÿ¹zQóØa¯æËXÿÇaM.dF\x0000ªC\x0000R£q*Çñ(±<iÌÚÔú·5Ù\x001e\x0001àÎ\x0008¨ÛM,³L#f§óLoEÖ\x000cÏ6\x0007ÏöeFzc O¬Ë.]E:b6³3cg¦\x0016>þ"OÑ]c\x0016"ÎÝ2¦ýtl¹\x0002å¿8ÎÀyKk\x0018ô3°\x0016´ÏÝFx/\x000f\x001fÜhõl«b'\x0014a{ÖªÊõ)¾\ñëGu(ã\x000e¡^ïá].\x0011Jy
°\x0014/À´KÛH¾/¤±içzu\x000e\x001fØù}¹ÿNÛ\x0016R\x001d-(y´\x0012ÍÕàÀÎÖAkø/R\x001cm,_*\x001eWÏï¾kGõv\x0013}|\x001a¿¾\x0000\x0002D­0dñëµBãâ¦îäËa\x0014ç\x000eºtb©l¬>ÎTÆYk*ÓÌ\x0000f\x001f>î\x0014+ºv^swâ;´âû®t\x000f\x0014\x0013}\x0000	·÷ã¤OZ-å\x000e7"\x001dÞ\x001dÒá¹v\x0008\x0001§\x0017n«ÎòÀ7\x001e8ÒÔ3B=,Àê\¢VyC§,·\x0010\x0004Jiª \x001e>pu~`Nß[\x0019[8&ÍßiäïS(\x0007
N
aëm©\x0015\x0006¨ãm!OS$Ú!iK"\x0017é\x0010@rf1lH«%ÍM\x0003¸´\x0015kIó\ñSN\x0011)cXéÒ=Õ¤ãLMÙ\x0000ëTõ$\x001eñ9\x0001¦57Ð*b)oÀ¢õ
Øæ
O\x000fi\x000c9óD 'ÝPIü²¹/tä	\x0007·÷\x0000Ö§-äuk!ÿþÝÏ\x000f¯ßþéÝÏ\x001fV\x0002mîuÒâRÇ`õ\x0012N{¢?ùíÃë\x0017_¾üöÓÈhÈò£KQëÜj	Ã|óTz\x001dàâ\x001e\ôãÙÞâ\x000cô\x0011ºÛ|Wá\x001dàÒ\x001e\rCÖ¢i\x000cnØx\x001dàò\x001e\vÓ6\x001e¹Ó×¢³c\x000bâ9À=¸â\x0004ùº'.Èg­ÃòüEÎ\x0001®îÁU7¸¨5êi·VR«êo¹\x0013[ÛckNlMÇóp\x0011tVlúQÓÁ¤Ñmë}¯»Þ÷[Ámöÿ»\x0004:¬r*\x000f\x000ep`À\x001b\x001az7Ð®ÚPÝþó48À\x0019q\x0000§:°s~V5Óëà²î|Úã@g\x0004\x0002
ª\x000fL\x0001Ä¹£SãÊÂt<Î(\x00048%¢\x0004Ië\x0016tÂÂ
Æ-§»\x0003\x0008pjD¦\x000e@*Ïb\x000b4¦6\x0016k8Ð\x0019\x0000§H\x0014\x001c3\x001aøLA\x0012»8\x0006vÖ¸8Ð\x0019\x0000§Jä:¦ò\x0000VØµ1 ã´ ÄÎ¨\x00048e¢S·&\x001c_\x0016uÝÕ0©\x0013hè\x000etWÆ\x001c·DAjâÎµ[¶§Ð\x0019FA'£,õ<\x0002K¤:º¦\x0003TáÔ(ÂÎ0
:\x0019¯ãeÒJÑ	¤±ñ\x0015Ô\x000eVè\x000c£ Q*J=Ç2siuÙìë.ëºÃ0Î0
:\x0019Ç9Ë\x0000+ij1ëg±ÃNhNÐI'
åýÛ\x001e\x0005\x001c×$ËW=}Ós3l>6áÞ'\x0019>êðgh	¶yîsÉ\x0013¬\x0013igKÒØ\x001f\x0017S\x0004ù®:T/\x001e¦¡û°É:ÉuB(rµ\x001dSCm k)ëÂtZÛí@gx<Ü÷Î{ÚDÓwÄ®zúÄí\x0000gÒNò¥\x0010Ú\x0018yÔÊ°¤cBêiÉ\x0003½ði\x0004\x0004Üf\x00076âXÁmió\ÖIF#È§\x0011\x0000¨ge®«l#t§¥Þ\x000etF#È§\x0011ÜJ?\x0006\x000f\x001fhû°±3\x001aA>\x0000HzÈl\x001d®±\x001b2QN}Ò\x001cèLO&ú\x001fqÓ=Êk9µ1q32AN\x0000­åáòÉÖõJÑ\x001dÆ~9Ñ\x0019 L\x0000\x0014\x001dÆ¤^n-WÍÎk³n\x0007\x0017ND§Nô#äyýÇ5t:\x000f N\x001e±£è	@
\x0010n"ÙÀ%%»ó«u\x0007:£\x0013Ñ©\x0013¨ó:¿ñEÅ
N×\L¢è	6Ï\x001a·\x0003ö¸çla2çöúÚ)\x0013\x001d]á\x0019¤Íz±ÕÁ&íôáÝÎÈDtÊ\x0004é¸{oDb«xOôØÍI4*\x0011*ÑÁ¥,¡Óºu\x0006§\x001aÖ&©.\x001aNàî8\x0019/t \Ôq\x001d¡\x001f´'Á\x0019Nà\x001a\x0014Yu\x001feWlÒî\x001bÎË\x001dØFD§FPÖNæúÿ\x0015[:\x001e¸Ó:ÛÁ%£\x0011É©\x0011\x000cN.ÁÈvè&ïÃ\x0011ä\x0014	)¥¡Kz\x000fÛ\x000eco§öR\x000epF#S#¨é\x000c¿\x001a´&v\x0019=t	q2<<\x001cQY{èHZ«Êta5Þ\x001býÛµÜêèÛõÍGÅ2¦'ó\mÁ\x0018£¦Å³/v\x0008\x0007à\x0006YÔ±'\x0012«ùBm$uº¸CJbÆ¿ÛþÀöñ/þû»\x001f\x0019ß¯\x000fß|x÷óûïßýøËÃ?¿ÿ¡cú(ÒJ0îgKSè\x001c£Üm÷#Ò¡\x001býÅ?½üÁ¾yøæõËo_}þò«ï\x001eþùÕ\x0017ýßü4lÚÃ¦	Ø=7]+ábO\x000edk­
á'3Hf`Ç=ì8\x0003ôÑ´õÃçÚþÀN5
;\x001eJ\x001cf`§=ìt\x001d6W^7=\x001a
{\x001e©¥¯px\x0015A÷¨óD°CÕë¸®R\x000fã(7\x000cO/äf`×=ì:\x0017l\x0019ÙYíQV6H-GÖÃsÎ\x000cê¶GÝ&P§ú(5E\x001dôÊ"ë¨>T~NÞß\x0017ò\x000b\x0013¨GÁ/'\x0008âÞ7Ë\x0017ÄÌà¶¤=ÁÚH ¥ü\x001cn\x0010Ü¤¥üxhp\x00066NÀ.i\x0018¹\x0002È=/û\x0001ií^¼ë21b\x0003\x0013j)É!k±Îº¼7/áC:>Û¨
LÈ
ö\x0004©kb?'®iH·3`:¸óÏà6Ä
\x0013ÌÍ5²ÚÉ\x0010ó#È:)y\x000cG¹ç21Ä
3ÌÝsæ($\x000cÓì°Ia×Ã\x0010¬	ÜhX\x0010gX0£:å±S|#Á­dÒ\x000e3_f`]S»rµ/fuEv¥6CÐ!Çm6%NmJM]61ÕÍc\x0012ád&\x0007Ä$0Ãæ@Ò!ÞqÖÝtxÁmÈ\x0004§Ètv
¿äe%\x0013\x001a-Ç\x0007OÃ\x0019ÜÅà.s¸qs£\x000bEw¥\x0016âçC³Ê\x000cnÃ8Åqxuõ´;(\x000bÆá\x0008t¸XÁm\x0012XÉ`yÜtf$}!gÑÑxÃ=ï\x0004n2ìMSì­³ÅOI\x0019
%b×\x0019Ø&¥\x0014kdðJOè¶¬\x0002\x0019Ü&¥\x001cvË©¸\x0007/È2Ù\x000c?Óág\x0006·½0QË\x0012!âêë©î<4îÈd´f´²àhùN_aVÜ£e9ßuq\x001b­¤\x0019­¬Úó &$Ð\x000bjØ\x0019Ã¡ro\x0006·ÑJÑJ\x001ea$\x001dº9<&]'Ã4ö×Sd¤f¤²nV\%!¨uA¸ë21RI3RÙ¶Ër±ÏZ\x001c\x001cXï(d¤f¤²i1YÂ ö29ã]SØh¤2N]÷äa<_I\x0006Éôu\x0002º¼Ûa$â\x000cn£qæ{2Å4$ªóÅÒK*ñ>4ìÍÀ6R\x0019g¤²áèÅåÃ,áV«ph÷m2Î¼-ðä_1BI¤	l¬ú¶À>\x0001wÄmß\x0016f\x001e\x0017¸sB6%Ê\x0015,OUSc;RI4J\x0019'²gôªÏó«bæ¥\x001aì»®m£qæq\x0001\x0002Ûã¯ÑV+\x0006~\H\x001aîxÇô5\x001a©\x0013RÉÝ2}	³úÕgC ñ¾çeO4\x0013'$ûú\x0005vjÌ*\x000bl\x001c\x000c\x000fmó\x0013°Q4¡8l)/æ]ÈoPº+Õ0Ò\x001d)0\x0019ÁI3Ã½\x001dÛ"Yõ&ZG÷ErÇÅà¤	Á!^\x001a4tDpjÓÅîùPâ¤	ÅvóSCxç<6å¡Nj\x0006·Q4£8¹nyI¾so¥y÷¡ãq\x0006¶}ÍÐÎÒ\x0006"\x0016\x0014Ø¥\x000c2¹ç3T2f4§\x0014\x0002\w%Z	0¶å=oÖÑ4¡9ºQâv³j\x001d\x001aÏ\x001bØdgiâxÆ#V([ÞEºè´\x0008Þs}\x001b­L\x0013Z\x0019;÷©Æ§ U95=Åßwd#yF,Ö\x0010pÞª:jÁÌåòwmÄ2Oedëh\x001a,(·\x000f9Ô\x0005ï¸¼³QË<¡ý ¦3µyyGI\x0005S\x0018ÛòGlÔ2Ï¨eNbòÓÜ÷"Óð=q\x001bµÌ\x0013j\x0019yðé¶Nt[f\x001aÙÉ=o³Ë<#Ôç\x001bcÒKØ»¬êGlË¿&ä2bÓKX:6\x0007i\x000fÜ÷¼]ËF.ó\VÐñ(¸\x0015÷ð5â>XqÏà6r'ä2RÕQ8¼/åa;ÕÅÞó$_ê	ÕÃÈf	÷PËÁÞé«»\x0018ö.3ìÍ5Iô¨Ãþ|
ûàG5\x0003Û`!Aö
ÒE\x0002ú2ÒÉ[s{F;\x0018·¾µÂÿ0SqÒÔ\x0001/ÛÖ\x0013½\x0018ÄrÏ2°\x0014Oa
=\x0011\x000cý2j¦S\x001a·ö÷¬\x0006Ëø\x0014~Æ)ø1$¾?\x0019§\x001f9µÅ<®e\x000fMâSûCôi\x000e>F\x0019GÍlãß4¹­÷Ø¯\x0011s1í\x0001ü\x0007n\x000føìßßýéý\x000fß¿{øöí\x000fÿýí¼ý(Ø¸ÔÌ,\x000b*Ï^Ø/Ù¤!\x000fÈ,ÚÏ~÷òËW_=|þòáÛ\x0017_üÓyñi¸\x0007£ i\x000fþFAÆ=Èø7
2íA¦¿Qy\x000f2ÿ,{åo\x0014dÝ¬£ Û\x001edûÛ\x00049Ú\x001dV2\x000f[(©â´KGÚëU%!>üÃ¯ïøáÝ/\x001f\x0005s\x00195ßª\x000cß<¯~\x0015È\x0014ÏÂÞ,ÿ
o^}ñÅËï>
\x0012÷ ñ\x0002È(O¬=ïS_\x0008:"/ÅzÚãïÃH{äÇµ;·\x000cÚê\x001fN$Mç½ô>q1^ÀHzÄåq¸(\x000cZ»\BML{É\x000fß\x00064ÃØìO\x0002yjÕí\x0004÷ ó\x0005¨\x0013õúAD=bû>o\x001aÉÓ¹ENe\x000f²øAÆ¢\x0011¼oÔq<é|ì\x0013dÝ¬\x0017@X%\x001eRµ\x0012\x0010I¾éÜ Ó±í16?Fj«OÖ²mB\x00144Vä¹Ù\x000bãÎÜ\x0016Ãfnë\x0000	Uçö\x001cÔ"qk«,ÉÓ\x0001×NVn.è
41WNü)öJËkAyx¿Òè
\\x0010\x0010\x0007s\x0005Äj\x0004A¨·S)\x001fî0/ 4\x0003~Éa÷¬å£\x001aU\x0012ê ¼tnËã\x0003i$\x0007üÃn-ý-Vß8FW¤|îêCi4\x0007ü¢ê(/ïûZ§v\x0013 Re:·7ð¡4|\x000e~BO¥ojG%ÛÎ9·×öA4L	~ªìt­µ TÆ \x0010¬8èüÜ<ÝÉBÆ+be¢á\x0015á!#Ð\x0002VS\x000b;Èè\x000e\tÀW°&~\x0010J*íQ \x0006ÔÔ-[æÞµ´y:ÿAóô\x0017?üþÝ_\x001e^¾ÿñç_Þ½¿¡\x0018R\x0006Õô´RV²ºZ¤v8ñ0È\x0017_üæåëï\x001e^¾úêÛïúÿø4Ì¸\x0019¯ÀD\x0018Q\x0019e>ö\x0008ÐÓqny3_ÁI ³Ï¨\x0016®Yïuö^ªxÁ¹Ö=Ðz\x0005(\x000fâV ¤·Ä±\x000cþ,Çø+@G´\x0000Õ$É\x000fgc\x001b©ñÊ¨UKåt
\x001b¨ÙIpi+q\x00127È^\x001b?SÐþàTNç¯»Í\x0004vSq£ö%$¬ypÓLL!×dúmø\x000fK¿Í«?ý¹\x0003y÷ð÷\x001fþòßÿå??¼ÿÃÃ·?ýúÃû¿üçG\x0001\x0017¬:3ËEdÜB\x0002å)Ä£;ú«/¿éÿøòáï_¿üüåëW=|ûõ/^½ü4èb@ë ¡Æõ\x0010¹[|mZéçõ¼8\x0011êÁzç9ÌxûýÛùð<æj0×@seh\AsWB\\x0003"°È w
ôhWY@s»ÊeÐ\µ  Õ)ËýnO7ÞeÐh@ã\x0004èu\x00126îÿ\x0007cI KúPëw\x0019s4ã\x0004fÈlv¶`Æ(Õåà²@¦C¶p\x0019³¡8A\x001dPôÏö8«£gâ~ÿ\x00153\x001c\©¯Çy8j¬ù/×Ã­\x0013+2; ¬÷Ñ)\x0011o8ø._g½§Ø©La\x0007vg¢mO®Ë;¨\x0003=ïÉéµd`þ&Á¿ûñ,¯úÃ¿¿ûðîí¯8Xt®atj6¹\x000cF-·XÏè¾ú{Ä×_ö»¯_¾xói°´\x0007K\x0017Á\x0016ñ\x001e^lk[\x001fï\x000b`ã\x001el¼\x000c6Ê1ÓS°G\x0007º`ó\x001el¾\x0004¶tHz\x0001[ÆÃEÜnqv|
¶ÿ\x0007¿ûósHÁ,X¸¸b[Ñ\x000bíØQËX\x0011Æ:N\x001aç±Þ¸Y±puÉ*\x001d$î* ]\x0005êbñ\x0006v5+\x0016®-ÙBé±V\x0001\x000bct¦ú¶BgÆ,¸Ñ%\x000b\x0017×,èÄÅ\x0014ù²{½h\x0018¯=I~foÍ6\x0003µ]Ü^H\x0017¨l³ M2â\x0010í;¾¸b\x0008¶bÿÀðâ\x001fþò«+éïÞþúËÏü$üÛ\x000foÿã-ßã|Ü£´..¾«¥BòÞQÜ\x0011ËÝ\x0016$}ñÅËÕ¤ôw/Þ|÷-¿\x000eÿöõyÁw:Ï[\x000eð´\x0007OàyîB,÷Që}DOÔ$5Î)\x001d:ÔæÐÇ=ú8>*ÇõÐ£^N¡¾#÷Ø\x001f
ÎæÐ§=ú4oûWð|eµVbã\x001f?äß\x0017{ÞcÏ³ë¦ùÖò\x001e\x0010%ò\x0011I#H'Ñ=ú2\x001by½Óæúd­hÇ\x0012uÕ£­È\x001cúºG_'ÑW$$óÀ°*{_\x000b$öÇvÁ)ôãnA¿øN.{9p±ñ´\ÕbË%_ô`ÐÃ\x001cz(îVÜ¹¡UîØ¤^\x001cs;Z¤ÌÁ7Z\x0005b\x0000âÎ
\x001cz[-*c¦£[Ô\x001c|£V0+Wý¨H\x0012}X¦I­kGµ¶\x001eÞí'Ñ\x001bµI¹B\x001cg©6\x0011d]ùùØ2\x0007ßÈ\x0015LëU\x0014÷Ö¾ôur^,eé\x001f®\x001b&á\x001bÅIÉâ«Vø¡ÈÐL4Òî¼ôdÁ¬fÕëä7Kº è\x000bÀÑ\x001bÉIÍb\x0003²ÆÚÑ¥å¦¯{/ýfà·Ù¥¯\x0014¹G_
úÒ×[NZ>¦à£\\
j%yÞt\x0004G\x001dm%\x001cî\x0002&á\x001bÍÅYÍÅÛ\x000bñä2\x001c%Åj¥\x0013\x0010ÝWrÑ\x001e\x000f'%x½W	~ÔT9xØõà\x001fèçà\x001bÉÅIÉE\x001aÌýø­¬O(vx^ sðæâ¤æ²å¤ú¯d½\x0005C\x001eÔ~_ôFrqRr\x0016×5ø /W=cÐØc£Ü\x001cz£¸8©¸üv¬\x0014þ.íºqF\x0004sðfá¤f±5ÂOQ&äð´\x000eÝ¸'î|sðfá¤f±\x0003Îê¬Õ%·êIe\x0014fvÉ=<ÕÎÁ'£Y4«Yß£,¦6l¨+\x000e¥àbÑ¬buJî\x0010j(Óæ\x0010Üûr>ÙKÁYÎoÇ¼¬´Ã^"«fÅAù÷M\x0017ÈP>MS~ÖçþÌÆð"¸QoÖJ¾sªLóió),\x0003TVÚ\x0019fP1l¹æqúÁ\x001c|sN¡És
\x0001±ÃÏ\x0002¿T9\x0011A3ý\x0012ï­!}=¨°wÎª¸§\x0005\x000f\x000b\Ik?;Þ\x0017¾!}$}Â´\x0013Î%ë¼´k¢\x0004¿â±·{
}4\x001fg9\x001f\x001cg_Ã(:\x001cèÙ8ï®è
éÇIÒ_Je%ø\x0015\x001e3i¾@
ÿ0x\x0012¾9§ÄÙs
T=§\x0014¦Mâ\x00115Á}\x001f²¢Ñ¬8­YA*k{ô«&!û
?\x001eæUNÂ·/YÓ¢\x0015õ\x0015±ö] Ñ¤ð\x000f¥SèfÅÙsJ\x000e2G«¯<æh%Íôk<ZwÍÁ7\x00078{Pé~Òào¼\x0003cé;g\x000cÑHn\¶ÛA~{Ô©\x0004$þz}ç\x001eZ	&á\x001bÉÓ;\x001eÐyñ Ü
6Mxúâ¹sôäÆÙs\x0016^Ô\x0010õ1^Ô\x0013³Ô)øÉhnÔ\\x001e3tdîIgôF´Òì{V\x0002ï¼¤kbAJ\x0011tçÞ÷\x000cç§Ù÷ JÒ\x0001+ \x001eT\x0008\x0007öã ¨É[Ù]\x0011§ÞÌ.^<S?¤¼¨\x001fWº\x0008\x0012êÕ2û\x0015#=ý\x0011æD)âdÛ)\x0008dV(ÁÿñÎ·Ôþ\x0008jÓ?úr\x0002ù\x0011A$ÙÈ¥ÝY\x0005úøåÝ'?ÿ2÷#PdrIé1F.Õ²ã°®ÉÃïáGù\x001fùQÀ]³ù¥¨Gà|hòþ\x0011OS_N0NÂK®\x001c\x0007Þ¢¤;Ý~ò ^c|²LæFôß¾ûéÃ¿uôýôë_Þýð¾û\x0018èD¡H\x001d)¿n	¥bR§Ý×ìáK\x0008ûòë×¿í¸?ûúÍëï^~ñê«T+\ÜÃÅp;y¦\x0015m]¬\x001d\x0016´:\x0003«£=-{½öhé\x001aZäbòuÊ/·J\x0014	.ýDápµs\x0015nÜÃ\x0017\x000bêÓ××Bö¾n©ht\x000fÒt\x0015nÚÃM\x0017£«\x000e\x0007@rÂ\x0012dðHî¡0ê*Ü¼¯î4ZM¦{pÜõ&\x001dw=¸§\x0016\x001aWÐ=Úr1¸©ÊÍR\x000fnãux\x001dÁ=ë¸¶îÑÖh¹(±	Ú \x0002E\x0017näWÆû m{´í"ÚXÄ§$ò`Ð5\x0007G._\x0015´÷Z	£\x000eqUp5¸ ÃÂ:\\x001c,mà=5Èº×*ÚEICLr/\x0017\x0001¢´\x001eqi³®\x0006gÝ\x0006Wð\x001aIÆ³à×\x000c®Ç·\x000eQ\x0003y~áõpÖop\x0005¯\x00115¸¨jÀs?ó\x0017\x0007ÞT¤é D<5,º×¨\x001a\5,juÐ×\x0003* ÌÛÅ½ð\x001aYºÆEúY¨´\\x0019S\x0012k\x001eßS³·+x®ÁEaã)Þuw­³ãÚF]\x000e\x0003ÈU´F×à¢°õäK<	;0W~\x001c#ztï¶Û²ÁUiK$§\x001eÞ¢ì+\x000e6;´=\Åk´
.\x001b÷1\x001b¿ä¯xÇì\x0012ïÔ
ºáUu°±ÎSãf÷0¡ö*^£nxQÝ\x0000²x\x0018:5¼@º|y\x0010Ü}àÚóÚUq#½ì]Â«ydÊ\x001a^¸×vC#nxUÜ8ÃíFIª÷0êÝzïYsí\x0015¸FÛðª¶aG¼\x001e^ÐSER¨Ê«÷^»Íh\x001b^Ô¶À
Ê\x000e7Þ\x0012Þ¬pé^©$\x001aiÃ«Ò\x0006m\x0005j\x00193\x0018=¼§=ÁWð\x001aqÃâ\x0016²LâìÑ­Êe1¦2Â{/¸F+ð¢VD#ó¥q\x0010#s C/åE¸d¨.RoÿÜòò\x0013y\x0002û9DÄ±x\x000fïVWáÚË§kT\x0016[
<\x0013j\x000bzC¡
¸wR
2TF×¨,6¶Ðè6=V`\x001aÞx\x0018w\x0015¯¡2ºFe\x001doÙV\x0003pÍô·±Ù\x000eÓ®â5\F×¸,¶Æu\x0019·\x0001¯
SÔÌ!\x001aö^Ák\x0012_ºøÆÓ\x0015/)\x0007B-zyJwÚmÑC¼F\x000e±eÐ´&fQÂ\x000b´Úîucf¬eÖ;>µSt¢.ÇÄ®n¹ï¿å-2Å(1R\x000f¥NÐ!=qiç?ècÅoÞþúý»\x001fÞ¾ÿðÉ,§ÉC]\ª@È K!S\x0013Àß¼xóùË/^¼z}\x0003<ÜÃC'<¨Ê\x0004\Ì\x0019$	#)h\x0008©f	\x001ex´GÞèU¾\x0011]¢ÇE"\x000e¤|º<èâ\x001e]ô\x0006¯p¢²\x0004/èN\x000e<@¥Jg&\x001exi\x000f/ù·f(È­ã¤ÁÓw(°ôË{pÙ\x001f;/ÛÒØ\x0017¤7q©ºzà=¼â×¤ù8r\x000bþjþÓáið:ýÌÂ«{xÕ\x000b/Ëlææmå%Ðèü=ðÚ\x001e^ó³Jä½]H£'Á;Âv¢Û¬DÓÎJÔ\x0013=Ò¡å\x001d^TÒË³¤\x0007V2¼ÑÃ\x0007ýæ 'ÍLÒ\x0011bÊ_\x0017f[4\x000cAü9â§ß÷ÜyÙ\x0003Ï°2¸iy$½Ç¼½ù´Ã$_/<C|àf¾NÆ²9jÕkUwG=½\x0006óà3Ô\x0002nn	úx¾\x000c(>¥¾|zíåÁg¸\x0005Üä¢Eh1ôÄôdõõsâ$5£a\x0017ô²KHzËÉùô,\x0008eró¢!\x0017tK\x0016á¥Æ¶q²=HpéüÉÎÏ&¤^r	ÒÕÒÃ\x0017d~x\x000f\x001fêY\x0004f£gòQt'¤Aî©qMÅ\x0013+<<\x0016Þyñ\x0019îC/÷¸ÕÁ´\ÆEO85óà3))ºsR®'[ãÇæ
¸D±¶\x0008xZ¦ãg¸\x0019½Ü\x001c±°kVÞÂ7´êéIØÏd¥èMKS\x0007\Ð$Í\x000b]¥xµ/¿iî3Ú^íèÇ Õ-12Üzü´R¨Þé{ð\x0019í@¯vä(õ Ô¸ßRð5\x0019³Ó¿ÎéÔ\x0015\x0007>2ÚAníÀGÙ½9ðAÓ*¶Yé CÍä¦fõæý;p
(_WÊä]\x0006\x0019ò#7ùA~ü¯Ú¡\x0019§¦û\x001e|fw;³ò\x001e¾GJOî\x000bðÔýÖ\x0001/Å\x0017ÝÇ¢À;b	\x001fE½l¡ 'r§~·7ÃKã¿Zn3ø_û\x0000¶e>ÁzO\x0019G5\x0017÷y:\x001d?µCøyþð_ÿxÀøGw~õî7H[.äñ2t:è0²%ª-fTØÛ¡¿ýñ/ÿïOï;Ô?¿ûðÑ\x000f©¬¥:zR³ ÒÒ\x0002´Ô|Çpè¡ÜL¹_|õÙ×¯KÔo^¾þèô\x0007{È8\x0001¹,Þ"+êÈ}´ñ³ÓæóNùnÐ´\x0007M3qnr¿Îzk\x001cWKyî\x00079î!Ç	È\x0015¥*µC®bdÔ·×\x0008ôáÁe\x0002tÚN3£¥0[El_\x001cÒ\x0014\x0013ñpí4\x0001:ïAç	ÐMGCeJiÆ\x000e%\x0013¨Ë\x001eu¢õ¥\x001f\x001cµ²ÉCÚ8cÏ;ú»A×=è:\x0013ê¦ýFTûíÙ#Ö;nÅ¶GÝ&Póc¢ nÚtÇE \x001aë|ÈY¯£ÞÊ®\x0017m	3ÁâxÌ±^§+$4ÖÚ¿	ÔV\x0011g$1\x0002K!Ãf'}Ñ\x0017LÒÍÅ¯÷CmD\x0011fT5²\x001dû±5\x0008j}oæ"¥ç'õ¸a\x001bY\x0019]\x0004ÌcÏ@,l\x0002EÝ\x000e£+&P\x001be\x0019iLA[/c\x0008R£ÏH\x0018kä~¨4Â6rÇ4H°TÔ\x0010BýÂÁ\x0006{\x0002¶\x0011GQGªDXª×ý¤[7Ö|Gò3B\x00033JZQÑ£Åg»ê\x001a9¶£]³q³\x0001x\î\x0002
\x0014e Ô\x0005õErp\x001bmÏ\x0004\x0013ôÇãOÄJ(öÍ¹Ö¯\x0010_\x0008l88LÀ6D\x0013D\x001bê<Èß
\x001b\x000cëÀtÇ\x0003\x0018\x001d\x0013;2×ª&1\x000fú&7à\x001dõ¡Åc\x0002¶Ù8±#y¨ØâÆ®ëÝ\x0015AU/÷DwH2;&vdîç0\x0012±Éõ\x0011³ÀNú~±&³\x001fif?ö#Æzõ^@¦Kî¸\x001fÉìGÙ)?¦(°«<=\x0011$µeJ1ÞoCÙ4³!ûQWlQb
bÂ×(µÏLñP<\x0001ÛlHÙ=Úe\x0004»\x0006F°ïD³\x001fãÌ~Ã(a\x0017¡(¥\x000cû~\x0007ßhvdÙQße:ìö(,By\x000böýt=Ú;¨
Ù\x000fcb\x000bÛs\x0013yJï°Ó\x0010ÈC\x0011Ö\x0004l³!ãÔj\x0012Õã*°\x0004cÀýîs¢Ùqf;Rá|o\x0015\x001aíñ'Ð\x0005Bw\ÖÉìÆ4µ\x001bZõGCh¢¯¤p40\x0001ÛìÆ4³\x001b{¶\x0017ò85å>¨ÿ\x0007ÎbÉlÇ4³\x001d³6e°7³´G\x0012\x000f\x0017ÔCM½#l³\x001dÓÌvÌôÇ-C\x0010îË8n\x0019\x000eÓ<'Pýföc\Æ%éQLnX!êÁ·\x001fÅî\x0007;\x001d'wäÿqØýg\x000bóù\x000f·:º¾[\x001d¾ûõ÷þëÑb:%fP\x001c÷ãnñGfk}÷æWß|Äéh`Ä=F¼±é\x0005HOä[ÁËÀø¼5ÓÍ i\x000fü ùS+ÈÅNAòly\x0001?bGv3È¸\x0007\x0019Ý {æ³Öåå­\x0019=R\x0019Á\x000f\x0017 ¦=Ääc\x0007\x0016¢Ä±ÉmWìÇìªqü)òÍ ó\x001edö\x000cU\x001e¸3\x0014}8Q;Z¸ííy#ÆA=Èr\x0001dÐÔ\x0011Ö:~xÓk,Ìw\x000b\x0008ë\x001eaõ/Çô\x000c%Ë~èJ>ÏÛÆÝ\x000c±í!6?Ä¥X¯\x0007±qN»@ÔZLÌð¼Yë­ ÇÓJâÁ²hÕO\x000fd\x001bãºÕ\x0015\x0014ëG5o\x0006iÆ/5Ëõ0dNcB3\x000eóä\x0003FiÀ/5ÆÔp×¬È óa±\x001cÞÏ/ 4R\x0003~­Éä]\x00112p±æúµÛCkð\x0005FjàÖðµ\x0017\x000eÌ²&\x001e¸;GÎoo0j\x0003~¹Ù].B?_£ÆR\x0013züwåÍ(Ü_orvÌîMYÆ°Áå#Võ74r\x0003~½éÂfÖ#MiÖëHÓæ%\x0007äÀ\x0005ÍékQüû\x0001h%\x000f^æ¥\x001b
¡ã\x0005BÏj=ÙcY\x001f )Èy\x0016BÃçxÏcÒçT6>KMê]17{Ï£´g\x000bµAµG2\x0007H\x000fe\x0018ßû#\x0003NnFiÈ\x0012/eÖ¡õ\x001d%H\x000fr¤VÇ1ìPö|\x0001¥¡!¼@C,ÛBéý$±Vt:\x0016Ó¡Ù÷\x0002J³ÃñÂ\x000eÏj¹ÕQTvã3/dö7]Ùß¨
NMê:D­\x000cÂø\x0011\x000fýA­CW¶\x000eh¡))%\x0012úªñP¶y\x0001¥Ù:taëôS¢Ê\x000e\x0016qãØM\x001f\x0019Ì~3F³qèÂÆIu\x001cj1ò\x001eZ0Ö±½é#\x0003IoFi6\x000e]Ø8ü\x001c%$ZCÐQêc<rÿè,Êh¶N¼°uxÎÜaäGùÚU«Ó:ÏïhvN¼°sR\x001cç1îÏ\x0014i¬Qï\x0007>2\x0008òfö.èÊÆ!é\ô;
×q´½~G³(ãE	ÒîÙ;h(~ß!õ
ygÉ"WBb'ï»pi ÷-³éC\x001d/_\x0006Úé×Þöò\x001fÔåå÷?ýúöÃ÷\x000f¿ùðöÇ\x001fþçG!ò\x001b\÷ÆX«T7õÃúÅÎÚ^~þõ\x0017¯?øÍë\x0017_}ñ_?
ö0é
Ìaã\x0017kæQ\x0015+Lí\x000f/ñ0Cø
Ì´®Á¤$0ã\x000efT§íBN`?ú¥¯\x001ed\x000fñTH1jë8Õh¤÷ã8q\x0016\x0013Îr%QçáE.\x0019,+Ì õ\x0010!×SïQ\x001fLØÊ»×p\x000b8{!ËøºmÁYdÐlX¬ªgab001\bÌ\x0013õáoÊáÑä\x0002J´(ñ\x0012Ê ÀÇÒH0KS\x0013txº3Zñ
Nh2\x0000\x00006~vUqÒ©g\x0013g6{hqâöâìg[±þà6¼5\u¬Â¯Æ\x0013ý?ñÝAHÍDÿ¥\x001faAµ²ã¡%ë\x00004(¨È=ã<ëQõ2ÚPÆK¡ä\x0017ÑµÙ=Ìd\x000få±4áP/éÆ¹ë\x0008]U(\Úé!Ê<§Øw»äP´,¡ÿÿ:¬=Aú\gèttnXÿè\x0007ËÃ@X^GÔCiêÏÐ\x0013¥;ìx\x000c{=e'5Úónü$FSs:Ýùjqv<¼9ðRKÙ¤vü\x0007Ní>û÷wzÿãÃë÷ï~ýÓÛÿë§_?\x00062Ê\x0013X×®~\x001a\x0013)[\x000ekG\x0006´z´4ùìw/¿|õÕÃëW/ß|ùâ\x001f¾~ói¸~QÞ#j×Wbb\x0007 ?BÚ#$/ÂÖAëU\x0002{7pYÕ0B\x0011pÐL?Ä¸\x0018ý\x0010I³ïä;gÜò.F?Ä´Ü\x00101+Ä\x0008IªZÎ¤QÄÃå\x001fbÞCÌ~Q¼ãúNbaÓ!¢~çC\x0015\x001faÙ#,nÅ-¼¤.§å2 ÒáÚÚ\x000f±î!V7Ä\x0018¥SÛüÅªe¹Y¾óÓC\x001fbÛCl~UüÕ;wÇ±[Úà£Eµ\x001bâ8O¬Ä\x001dÜ\x0018³:ñ±»ÄêáÚÊðP\x0003îGh¥Å­-lÔ!vY=½à+Â\x0005"®­\x001dc:\x0008 \x001f£Ñ\x0016pKë\x0012tGW]ÚXÓk\x0011¸_]rÖkâºÀ$\x0010a\x001dõØ!\x001e\x0014ü\x0018º_^ZäÖÙuOÓc\x0016±(í\x001cë\x0001ý\x0018¼__jB~\x0019ÅÜ°c\x0004À<¯Ò`ô\x0005ü\x0002Óc\x0015úim6è\x0010CÒ\x001ds¨\x000fóC4\x0002\x0003^éÿ\x0016<\x0006	c
ì\x0014i+í\x0018\x000f³ý\x0010ÀWa \x0010É(%~ÐyLB<m$;ñð áÇh\x0014\x0006¼\x0012Óÿ­ô(¼³Zó,\x0010\x0015`;<¸\x0001¢Ñ\x0017ôêK\x000fb\x0012#ö½I\x0010¶RîÇÞh\x0014\x0006½
Óÿ­Ì¯Ék\x0014³\x0018ô(ª
¶pðLóc´§\x0017¯Â,\x0018£ìBüQé»´§gl?F#1è\x0018èEª\x0000\x001eQ0**Ø\x0013ù8\x001aA¯Ä@-³íLN\x00024ípµïh\x0014\x0006½
Ó·\x000c>æU©\x0013\x0005©lé[¾\x001b\x001d¢ù1\x001aA¯ÂôOÅRHr\x001fÙ3µ<¶Ìá½ÉÑH\x000cú%¦#Y½)%µ©íGÔ,\x0012íØ\x0007æÇh4\x0006/h°SB\x001aäþ­È`Ã;l\x0019£1è×Ôä\x001eR§\x001e¹9YÎW+Ærhrc$#3ä\x0019öI&¡\x001eæ¹®ÐyPÏÁ¢ÇÑÈ\x000cùe&7½H­£}?b\x0015ÅØ\x000ev\x0003~FfÈ-3ýÏR:°p\x000f	ÆÚhpÏtvKöÌ/3¤P2T±ÞïßZ\x001fêúxzÏ\x0019òËL'¨\x001cÞôB´ªZ7:\x0018Mú!\x001a¡\x000b2Sô Ãµ(RØô»Ç`:½%#3ä2Ô:5\x0012³bÞÖ=ö´gÂÉÈ\x000cùe\x0006Âí%I&¤pF4óI8\x0019!·Êô8J=/eöy\x0002ÙÕ:¬"\x001c\x001d\x0010ý\x0018Êÿ²¬S¢\x0018+sýRÓsu\x0013càãh7ÄhD&^\x0010\x0019}ã&þAàQì²x¹OïhD&úoËúaZ\x001cn¹41È¹\x001aë\x0008ã\x001d0\x001aþ³LB±ùXâ\x0018E¬!\x000fæ9XJù1\x001aþë²ÔV\x001fè%ò©f	cÐWÂæsðhßbü\x001aCQª©ú§FæÚ	\gÞñìïiFd¢ÿ¶¬e$/ãÖ\x00079ZsëÆ1Ïc4"\x0013ý"\x0003Q
{\x001cÇ¶Öï!\x001e\x000c\x0007ý\x0008ÄDÿs\x000cÈ@\x000bv\x0017\x001c¯«±j\x0010±Ì/F#1Ñÿ\x001cÓ´\x001d¸º\³\x001bïpY\x0016ÄD¿Äô\x000f-o\x001d¹\x001f¶<\x0019Éõ2Ëà¡NÁ1\x0019Iþ÷Ü8ê ÅV ir\x000e\x0016H~Fc_c\x0000¶\x000ch\x0002eô*ge&i?F£1Éÿ"\x0013«>÷sWe\x0015#¹MmZbä\x0018¾#³-zöÏâdÄa<øbø1\x001aIþ\x0017\x0019®>Y£ÈCØy.Æ<ÏÞÉ>÷û\x0015&dMxøG®À;OÖqË3\x001fE£0Éÿ\x001e\x0013ªTlRnZß1êT~Ì'\x001e£1É¯1!òízb\x0005i
âÒ2NþÓ"È$¿ÈÁXÄ=©I	\x001c4¹MóBÈ$¿È\x0004\x0018à¡éMT&ÔÛÛcÙ\x001bc6"ý"Ó×cÕ\x0004¼ICPcP!¤ÃèG?F#2Ù_RÖÔçb+R 3ä7i\x001dÌFc²_cz\x0018Ü à8²ö0fÍ'æÔ³\x0011ì\x0016Ê\x0013Æ¤z¢ÒÀU+<êÁ,ÔÑL¾PUV$ÃÂõ^´Î¯F£2Ù­2µ¡µ8$B \x0005õ`'ìÇh«Ê.¨Ì8\x000f¦\x001a¥\x0015±1ê¥c/ÂÌFe²[ejÏÅ>XgUëÔª¾wL\x00034\x0012ý\x0012Ãô½Æ0o
C
/Íæe#0Ù-05&%o~ó\x0008æ¨\x0013íP¾îX¾\x0014·¾Ô¦M±Ëí7E%ï¨¹Ä|\x0018!ïâ¯\x0007.Y¼V\x0017L/\x001dP1CW\x001f£!Æâ&Æ¢^Ñ'¬%ßºhL»CYu1¬SÜ¬SÙ¶R_µm·¥\x0014õu0Ì\x0017xÄýÐz½Cá¿ø¯QTg(Êp7¾GÑôñ\x000eïoõ)Ò®bn¤\x0010¸X]ªÃw?Uë\x0004«p0s»\x0019hìÒ:÷-«t4Æþúðú×÷?ÿüîí¯\x000fß¿{øìÃOïÿÇÃW?}bæ\x0016_;çµ=¼t\x0011\x0014É ±\x0015Â\x0013ÄÒ~úæáõWß~ûòÅÏ_>|öúëWÿåá«¯?6kü\x0002Üÿ\x0002ÿ\x0005WÄú\x0013PÕ³DÔpÜkó?ö?&\x000212Û+e°l+5Dý
\oþ'ÄýO÷ø	Â&ìÉÖÆOhú\x0013ó\x0012ø	iÿ\x0013ÒôOà×
¯Pôé ÑXÿ	øÛÂÄOÈûç\x0002hU
TÐKÈ
mlçÃ³ëüO(ûP¦ÂFH=ur¹Úi_?Âs>K\x0013¿ îAþ\x0005öëH¡kÑBcþ7îþ\x0013Úþ'´Ù\x0000 *úWÈúîÜî\x0004:\x0014`MÿÍÌpÑµ0ÿ\x0013tB\x0007Û¶\x0000I¿Âs \x0013¿Ájó¬8\x0003{	Ö!ÎR\x0007×¶t¼¦ÿ	FaV\x0001¨òµéº"Ö,¿\x0001óø\x000cÏðNü\x0006#m0­m¼\x0005¤\x001d\x0008q-ù_~C:\x0014ÜÌÿ\x0006#\x000c0­\x000cPÇ­\x001cÆ¨­k=wR^-éî¤\x0004WaXÙ\x001epõ¬'dVµ\x0014õ\x0004]³JÑç½ÅËªÑ;«)ë:\x0016ëlÉWS[³gí\x000eý¿¢\x001f8ª93à¢uk£8ûÓüîí¯¿üÌÐ¿}÷áÃ'|j"7ùq\x001fráÂ¨<«W¬j/Õ,rnhf£ß½xóÝ·úÛ¯_Ä°f\x0000¦=`º\x000cXûry\x000c½Î\x0004çî\x001fñÖiNÃËÓ\x001epº\x00068qSH\x0014Ó¢Tä
)¥açwèÞ¼\x000c¸ì\x0001Ë\x001a¢Ö,õ1L·ñ0Dâ2ÞºÇ[¯®Ñî·8W	ðæ\x001c
\x0007&¿\x000c¸í\x0001·ËK8°'ü
8p«þ
Xg\x000föu}'¼#ÿZ9"\\x0005Ì¶£y\x0000^Oã}§Õ2\x0000ßkÏeµË´Æ¦Qb\x0014äÔ\x0014HD8\x001c\/\x0003F\x0003\x0018¯\x0002îúÝÔÚ¬ÉÔ*Ä
#Ä\x0007/»Ë
\x000fÃe"&\x001a\x000e!¬O«ü\x0002\x0018ïD\x0001G\x00038^\x0005\x000cml»PÄï\x000cQmtÃÁú2^£\x001bpQ8bíéf\x0007|l\x0017q,âÃ£ëeÄÙ ÎW#Ìë E¼ÖÐ,vwc\x0011ß'ÔÁE­5')"îÕ!	¡ÆÁ\x0013wÛuF:àªvÔÃÂ¸8\x000bàL3·¤+xÑ\x00101^%â
q8tª_\x000e\x0002\x000eóêp7@CÄxë.]ãùH«ÖÁð±>Ô^Ækh\x0018¯Òp©\x000f3$ÒØÃ'æÁ\x0014ó2bÃÃx\x000b_bÊ`&G\x000f×\x0001\x001b"Æ«DÌCÐì9\\x001aå\x0017À\x0004m,{%hh
¯ÒZé+!«\x000f²^Ðpín»£©ÍeÄ&Ç«I<Ï>ÑuÀl+¯-\x001d\x0018zê¸Û26LW\x0007ÿÖÍkzm\x000c³Æ\x0018\x000f\x0005ÿW\x0011Iãéj\x001aË2/bñb4³ Nñ`ò{\x0019±Q\x000fºª\x001eÜ{TÔ\x001b\x001dä¤Ä³óX\x0015÷ZÇdä®Ê\x0007#\x00166&>F¯xuÖ%\x001eË6/ãµ·)Wå#óì/µñ'1PZêðL?¸\Flä®ÊGßmâ½Ð\x0011×G\x0010À:¿\x0010éÐë~\x0019°\x000fº*\x001f©%\x001dH\x000c<ÿtu5­Ã\x000c:{¥\x0014dÒxºÆ§\x0012u\x0010;\x000f\x001c\x0008ã\x0006¸ÜKîÈÈ\x001d]»m§<Ö0\x000c&§¶±×Xbwu¬L¡F\x0017Èb3Ùïl\x0011.Ê`YØÈÞ\x0015gæmå\x0017?ýúþçÏßþ·_?=\x0010W{úÙ²2\x000c\x001cÇ¼øp°êÐA_|ýæU\x0007ûâ\x001fß|då@{¤x	)ªEÙTFR^V¥ðìØr\x001fRÚ#¥kHAìxÖé 2\x0015\x0019\x000e÷kPã\x001ej¼\x0004Zti\x0001\x0001\x0004#?KáÐ4q
jÚCM× \x0006¶Z¡V\x001cÚøþ÷\x0001÷@ó% !Ê\x0004Nöi\x0006\qVMÒ¹Dî.HË\x001ei¹\x001d2\x0014)HrÞ¢~|8<a\CZ÷Hë5¤¤\x0017:1¢<ëR(©)ÔÃqø\x001aÔ¶Ú.Aeã[A\x001aÅÐúÿå@z½\x000fú¯q?óT\x0015¨YLº§t1<;WÜÕP*\ãT6:\x0017Ez\x0003öD\x0005é>X
QÁE¦\x0002Me#»
\x00034{\x000e÷áT0\x0004\x0000\x0018 c´%¬*ªÛb=Üìº BÖùÿ ÚÿîÃoüþÝ\x000f\x001fXy\x0004\x0010¬G\x0019.(^Lò0YÁXÂ©ñùß¿|ýÕ¯>ùÅ§Áá\x001e\x001cúÀqaö
.µ&ö\x0000\x0019Î­ÎÇ±Np´\x0007G>p\x0001$ÎkeÏ\x0012¸¤·à%æÏ\x000elq-ú°EÒ?=Iæî©%p{r=½\x0002pK{pÉ\x0005.TÒÛøÜq5hÊc\x0018y	\x0007ßL'¶¼ÇSÍæxµôìqÓ·ÜNç¼8°=¶â[?°¥*qKr£Ê¯÷BÒ\x0005\x000eµNpu\x000f®ú\x0002·Îv\x001e\x001f5¯0xä`\x0017å\x0004×öà/r¤2Ë4¬²òH(M÷*ÎË¸\x001dÜ6\x0012gaàà\x000c]Ðì+÷\x0004Yt¤c\x000bN³òàÓ(FïYî\x0015ÐeéWîàÂÜw\x0005£\x000fà\x0014\x0008w³\x0005Ù"a½²Ïôµ·Ði\x0003\x0011\x0008ð)Dà¡®²aS\x0011óô~~Ñ!v\x0005g¿¬\x0008pj\x0004ªSuß±(uý»f\x001d^±9Ð\x0019\x0000§H\x0004í²\\x0014l5ÝÍtàc®y	\x0018\x0000§L¨§åÜs{ÑWÈcÝ±M¡3:\x0001.¡(-W\x001dÈ^ikÿ~O RÒØMr1\x0018¡\x0000R¦ãªòÖ¹!êtÙr<k8Ñ\x0019¥\x0000TôØé\x0004µr\x0016\x001eÏ°ÄNïÁ:ÍÌeuh\x0002}JÁ¶ JÁ\x0003ÍeÙáHè`\x0011êDg¤\x0002]R±NRTÒ:¬G.kèâé\x001b\x0003=Iø"ä¬]\x0005)Æã·¥âÓjG\x00076£\x0013èÒ\x001e¸q÷ºÆ®91Â¥ëx
Ñ	ôéDH8$,\x000b
·2äî\x001cF#Ð¥\x0011KÜ¤#ñ\x0011\x000c5n\x0010óËÑ\x001c:£\x0011èÓÐ\x000fÿR¸ØIæTjÄaZ\x0013\x0008tJDJ:.=ZMmÌåy¶sàB S!\x001dé20]h.¨|\x0015<øÄ;Á\x0019@§@Äqa²DNBk½SèÈ(\x00049\x0015s%\x0011×Îx ¡Ó\x000f[è´üÑÎ(\x00049\x0015ÆÀäDq}#MÇ'Hèæ\x0012N2\x0002AN\x0008£2]ëVG8N8U!¶ÑNtö®É)\x0011 ¯\x001e\x001c¸(\x000eÛ\x0016¹¹BK!JkðX\x0007ÑÉázKJzF7Íh\x000495
\x001dh[rq\x001ch¦>¿]FK#J«Qf\x0010,ÃÄÈ+D½59\x0001#£\x0011äÓZ\x0017Km
ÝZ!j£±èNkµ\x001cèHK$J+Q\x001anÓ«l× ée\x0016Ñ\x0008òiD-QïÒ¸TOUGÈòvÛ\x0012ÑhDtiDW0µÒÎ¨¤¦·É\x000bhï­TPFâåÌ\x0005Û8º\x0016Û®ÑItIOéÆ{DÊºþOEwD>´![toO\x0007\x0003+4Ã$ÑÉ$	T ú¶Írä/J$|"Ù«Ñ¹Wû\x000e:U®:\x0012&a÷H=\x001aÎmd¶Crn\x0007T»ñ\x001e¤ w9©QÑ%w¨|q3YIòe%Èç×ÈÕxÊ\x0004%½~­mò!'Ý|»µÖ¬åM)\x00069EÔF*|0Aw3;"ùv\x0004»cI\x0019l¢¤§ÃZ)
\x0012¼}Mÿú'7ð\x001d¬{.yS@}Ýäqcë&\x001féöSòà¤ew·bM,ºÌV½èdkâqY7©dõ)ÆX c< 0½Äôô\1I/ýCÿþÉþ½/UIãC£V,æ0\x001a+s;Ìóu\x0003|û\x0004àÛ¿Ëöþ\x0010L\x0002ÿA+\x0014^¿ýÃû\x001f?ê\x000f\x0010k?~É=E¬\x001dÊZïÖ²³ÃÌYè^¿øìUÿÇS¹\x001dp	oÇ¢6Óóe¶Øîår]×ÿ\x000e\x0003¯v>\x0019ª´n\x0015Ø\x0005ÅA\x001cHsJRnÆcÎØäVTeª8PAcu\x000f\\x001e°äA\x001dà¼JâVTmª9P\x0011Ê©°£\x0002±\x0019ëìÈþÿupÜvÀ\x0002³²À±´¸ô²ÈÒÂ(©yÏ5A{9>ñà"\x001c¸Ú²õ-©ÅâüÐ¯Kþè\x001dëÁ\x0015
®èÁ%¶@\x001d\x0016ð¼Ø\x0005\x0016IÝbuzZ¸\x0015ÙàÙäê·ãBi/Ì|fP\§\x0017Ó·âÊ\x0006Wvàâ\x0013}åÕä¡!\x000f÷Èë4%º\x0015á\x0008p\x0004»ÃµÞnå\¤LaÍ«\x001aXÕó\x0019cs"þ(^<S \x001c½=¨\x000cu»\x0012Ò`TLZ±×së´~êF\Û°ÜE\x0015ç#&9G-Ü%·ö¹DR\§µS·â²jíëÑ®.-nÎ¹\x0013â:}o¾\x0015áTtp*3Ëâ0²8`å\x0019@C©è T^^Q\x0017qJ¸ÚàÔrð~ôà2\x000eNME*ó¸Óý%\Ynçò\x00084\x000eFåeÒ¯¸üã\x0002\x000b2j>\x000ciñà2\x001eFmM¤ù!R\x000f:£JD\x000f×i×ê­¸\x000c¥¢RS\x0004±çàêÞÇ\x001c%^Uq×WÜË*:Hu\x0019·\x001c!ùYYIµ\x000b¦j¢	ò"Cªä!Õ´Ì:T =k4]ö3ù S\x00199e\x001c®uu~¶<¢ë¥FNûÎoe¨<TÊHSC\x0011ó\¨húg¸\x000cÕê¹tbõBèñ
RTû1M¿"Î°\x0004\x0019®'\x000f×ç*¶\x001d|Ó#>v¹$ Aª\x0013,AëÉÁõ/L$^9iEl­¨\x001aif}\x0019ö"\x000f{Uäù+K4­À.y¬ûtz\x001bv#®hX"zX¢¡äÏ¥§¬RgZj\x0018d?\x0011­hvctìÆÑ©Ç¯°2ø¶Ó{Ri§ïÂ·Â2>:\x0016ýÒë´&8
ÌJ©]$â\x000cIDJDG*ÑS\x0019f,%ÕuzUOS\x000b\x000cR¸ÀfÑGÇ¢g®_'-äµ:\x0019²¿*%\x001cKÑ£¬ù\d¬[îY¢\x001e±1O¥Ïû\x0019\x0008Bë­ômy!ð=ïªÛoÅ\x001fÒ8¤M­ý§è¢\x000f]î§Y¹fb_¡ ÁC\x001aô´@øæú\x0014^ÿ°.x©êí\x001c»\x0008IÏAÕêj\x0008Ç¶ù\x001bàa?\x0018Û¶þþ\x0007½þÝ»\x001f?¼øòí/ìaûQtøÜ¶\x0006\x000f¹Óeuçª:A9áaJ(ûÝË¯^¿zøòÅwì[ûi¸Ç~\ê²r	&\x0010ÃR¤^¨g³§\x000ebN´\x0007I~MÖ¯l°z!VI\x0003yj¢âÄ\x0018÷\x0018£\x001fcD±ï\x001f;©ÃR\x0019a¤;|ë´.±Éù\x001eÇÀ-\x001dK\x001ceêa\x0007	÷Xy\x000f2ûA.cå×0\x0006¹ÁÊ{Q¾õéqÔ±ì1\x00167F~@©\x0012GzmÛØ×§õºNu\x000f±^\x0008cÙ"Ë}]µ¯÷Ì<Æ¶ÇØüaìz§[ª-öä\x0014ãi)\x000fäÎ£·l\x001e½.\x0016Ï2,"\x0017jga@c×å5NVjüZ\x0013»P\x0007ùÞÖÑ
XurÏ2æ¿7\x0018­\x000bbÓ³Õ qln
ºsÎ­¤(Ø_mØÕfÈv\x0007ö÷X(ÜÀ\x0005½©$¥\x0002\x0011A;Þ±Æ ¢\x0018\x000eó\x0005/ 4\x0003~É\x001dK¦^ÄÕ>³ÁîóüÑÒH\x000eø5'\x0002êÅçn¹;ëBuY\x001e&í^\x0000i4\x0007.NÏ&Qx¨Søz6Ré\x000eª\x0003FuÀ/;ÈÇ÷æ÷LIÕÚ&ßwÐ\x001d0º\x0003\x0017'E¹\x0005ÁZä*\x001eÕ\x0017,¤rÚ\x001dïÃFvÐ/;\x\x0012È¢¹Z\x000b:n7aß8h\x000f\x000f~Bg»¢OO8
Æ\x0011N;(
U¢*clâ¯¿¤æ\x0005ä{£.J:=%:Q\x001a\x0012Â\x000b$Ô¦uuÛß#§\x0017øNfãýë8B$}"Å\x0016£sâi×\x000f%½C\x0017öNÑÎ«²çE2Ee¤ù\x0003#ÍC\x00176OÏ² ÌqC9ò£Ú\x0005fóÐÍÃgo\x0012·/^tóäÓ.\x0000'J³yèÂæé¨DÄ¢\x0004åùk¡\x0013¥Ù=te÷À£äè­ÿST\x0005×$½6eû@F³yâÍÓwÌZâ\x0019%(¶Y!ÕÓ§\x000b\x000fÊ4þëå*ÿµÕ³NaÓaï=®U\x0017f¹áôø·ß¿ýù\x000f\x001fÁù¯< ýã%¨úá8Cï¡ÖÓæèÛBÊ×\x0011æ¶ÿ°
¬zø§w\x001f¾ÿõãöc=t×ç½\x00148m[Û.zJ)ïBx\x001c\x0005¾z¥>üÓË×¿yÞxlÃ=8ôë´³Êw
ýh»îí%Ý]±å|>§ãfl´ÇF>l¨õÐ=pML&û>í\x0001\x00177c{lÑ­'\x0014«12{²>ÂÚtB\x0019{f¬ÐÍàÒ\x001e\ò(e'Kà$nZÀå=¶ìÃ\x0016Å9r[]{·¢v2pÜÎ=»oÆVöØ\x000f[P£À5nk*{\x001dß+pu\x000f®úÀL#éKr%Ñ\x0013mÁûDß\x000c­í¡5\x0017´Ø´^z,8¢-nç\x0003\x0010n\x0005·Íb]è78wC7Ê%r«§nß\x000eú\x0008Ø#7÷UÁO\x001d"\x0017
à4åõÔú^,\x0007F\x001dÀ'\x000f±e©½í±ËÜ¼~Y-Mé±;÷S¿\x0019Ñ\x0007ð	D¬Y\x000cØ%Ù¯*ý\x001c»9õ\x0002£\x0010àØ4n/±\x0003ý²[è&Á\x0019\x0000Dp+ÁêðphynòÃ\x001a\x0000HÄ
Rì°.\x0008¡¨]\x0000ÇnPJO&bAP³ÄNº|cx¯egd\x0002|:ÁÍ\x0018eÛ²«÷Èrup'¶3B\x0001N¥`g
n²Yùô)¥£Ã¹eF)Ð§\x00141·§kZ\x001eYÓÁÒÜ	ÍÈ\x0004:eb½µ\x001akN\x0002Wà^\x0012ö\x0010á~öN8b$vuL~V#\x0013è	Ú-º&öüÐ4¶Äi©\x0003	tÊD")8[b·Z¶ö/[ïµaÑè\x0004:u\x0002Pî~Ö
»ÃmSàä¦02NRºb"á^*F%Ð©\x0012Ú\x0008j6,|¯EgD\x0002"\x0001ð8È®<fý¬ºæÊ3s}n\x0006gD\x0002"Ñ#ÊXs#r#_?µº\x001d\x001c\x0019 §Fp\x001fÇXsY6\x000e±_sdT|*Acìêz\x0010\x0013t¡âäJO%\x0018]Ø.Èª\x000b\x0005ïtö'{ÙäS	j v­ëA\x000c\x0004\x001d{ÅÎ¨\x0004ùTj\x0016»Öå\x0010» pã â:sQ	ò©\x0004£[F,¹\x0013?
ØMî
#\x0013ä	.2ÚÝ¬Ø
Cb¤\x0013£\x0012äS	*EÆ,\'g	¬q$Ä§ïå\x000etF&È'\x0013â¸ºI°¸Ý3ÓÔn\x0006gd|2AlJI#tm%;¶ñ\x0018n
\42\x0011}2A\x0004ÜA½Kê*ÃÅÊ&ç\x000eZ\x000etF'¢S'Ö-¡KúYÇ%ì©ï\x0003èÐ¶Ã\x0004I§CZ\x0006Ö	º4\x0019:{ïï$â(¸¨<\x000c-o\x000f&si]4<\x001c<Èæ@ú]E$¸ÂJÀ=3Öõfp£±Õ­xh%\x001dmÇ_urÍ\x0019\x001aN\x001aæ¹kÊ%E
ï0à\x00100ÎÐpôÑ0Ö<\x001eÂúiQ×PÆ\x0001öÜ7ÛÎðptòpÛ\x0011±H5tß\x0012qÄn
[24|4¥m\x0002j\x0001	\x0006\x001c¦9Ñ\x0019\x001aN>\x001aÆÛ¥N\x0002ÎN»§0=3aþft»ºo)'ê«\x000eÄM_\x0019k}3:®'_º<]c¥t¦ÇnÜL¤ÉX2*|*Áeq{V\x0017§`\x0000Ä{ÅÎ>\x000fûdK\³\x001e°uLÿ²ãxnSé@gt"9u\x0002uZë\x001a»õËVÆQç´¢ÐÎ(Eò)\x0005F5\x0015ZÖlÙírâÜÑÁ\x0001Î\x0008Er
\x0005$ñ)XBVt¡¦r¯Ð\x0019¡H>¡àM¡¥ø7E»Sì²ì\x0007¡DTWÙPb¾Sì²ì
¶~Þ]ØºIÅÜù?\x001b©È>©\x0000îwßÖÝÊvýsÜ-tF)²O) ×ñ\x000eËI±ð	jGwW¹óD6J}J\x00015Ô\x0016¯\x001dÔ\x001cÅñ°sj|ë@g"û\x0002Ø{/©Ýêû\x0002\x0004¸Èf[Iä\x0013
àwØ<B·\x0016ÈsÝ\x0016º9\x0019ËF(²O({¦·´xíÖ­ÅQö7ùþRdRô\x00143ÆÍ|Y\x000cÛ9vrË\x001a¥È>¥à£P¬í¾±UµÛéd7÷a\x0011â\x0013
Hedí\x001dN\x0012¶\x0003ÚØnîÄS\x000c\x0015\x0017'\x0015§°;eëw
éNyg1L\LÜÓ\x0013Ü®'Ö\x0007»8,óú\x000c!ââ$âÑM·û¬}¿nblR\x000c\x0011\x0017\x001f\x0011w¡\x001f¯Ä|Ã.[\x0002c¹Ë!»\x0018\x001e.N\x001e^®4p5JàîtÂ.¶ ÓGÂ'y\x0011¶UÀbmqÃN}S\x001cè\x000c	\x0017'	sË³°£<Ä¶-¸¹¼¤\x0018
.>
\x000eÃ­c\x000bâ\x001bkÙ\x0012ÃÜ««dæØºæd;í±n«IÖ«/Yç2ÿQ¾¦¦ìÄî\x0015;£\x0010Õ©\x0010°Ý_°\Ú\x001d®ç\x0016]5\x0002Q}\x0002\x0011@ü):8¬Dã&ñÔ\x0018×\x0001Î\x0008Dõ	Dh¸/ù_oMb#\x001a§­ë\x000etF ªS Âv\x0018µÿ)V¼×;b5
Q}
Ñir<ÕEu*
òHN³\x001cèHTHä¶v8év][y2ï â0'aÕýûD¢ÌÇÐÿ¸¥Â§³=\x001cÐFTFä\x0016£\x0018=®kn%6\x0016>5Æ¸\x001d]3\x001aÑ|\x001aÁ7\x0011UÐõ/\å³\x0016Ý\x00124ù\x0018ÖD4DäYz}×wÄUú\x000b¶{]4#\x0011Í'\x0011Ë{ú®S\x0005llÉ®°fD¢¹D"7(cCDý¬e÷8ÍhDsj\x0004ÑãV{Ý$iÊÛ8\x001d1â\x0000g$¢¹$"·°µéÄ¥µn\Ø´ÿÔåÂÎhDsj\x0004neu«\x000f\x0010;ÉÖ{\x0005Î\x0008Dó	Dmi+©'î+gtÃot>nF\x001fS\x001fFI]\x0011÷¶®úed§î*7C`\x0018\x0018Ã®£S+û¿¬dî¡	lë+ÿKðG1¸]àÉ}DÝ\x001e$&KÃÀvò¿tÁ«ê^¹À"¯»\x001bYx¶G'¸6lî§­Q	³«Kwj\x0005Û)¹L\x0007õ@Ëq{ºn22²­Ï½4ÁD_G"»øo\x0017×M:ÂÙÖuìÚ:À?_Ó_GãZo\x0013×mQòÖÎ9wë\x000fOÚê|}u\x0007gê{N\x0017åãîû9'áÙmáë]ëð¶ÓDGR¼ÁJPàIw¯=lM<5z SÐ8ñÜ>îÔ\x0002l\x0007\x0016øZ°zr·\x0015ìtx¤yñ¸\x0001{«\x0003|Ò
ëÜ\x0019ÐF©Ó\x0018XÅOÇ\x001a¼2w\x0008¶\x0008|­DÇSë["ÃÌ8Ñ@7·1l³\x000eøºuÖôS7\x0006\x0007Ó>ý,s·b`;bÀ×\x0012ÓáÑ¨aOZvÂWR[ôæ4Ã¶¯ï¤+B\x0019\x000e\x001c½*9èÖ±3IÙÎ\x000eðµv,èô& ¯¼\x0016\x0005Ý¨³\zýh±s³ÖãºYß|ÂíÌ­±î\x000cEfkwÃS1xAÒ°*Ú\x001e´óäA#	z£òÖw\x0017\x0015ÇãbQi«m;\x0008¹Û¨\x000cO\x0003Á\x0019À¾æÚvw\x0001"¿1o\x0017¡s/>	l\x000cû1Ú\x0015Cö}B­½Ojø\x0000]Zîd\x0007Ô\x0001þþ	Àßûj¡ËæWtÖ*òQÍ3ûúÞWáï¬B\x0017@¾¤ÝEInºóönv±jj¶ÖôüÍìéç×oßÿøî_Þýü1|©\x001fçQ®SN·ÚÆ§Í\x0005 gvÉ·\x000f¯_¼úêåwß½üöÓ\x0018q\x0011ý\x0018¹'*­\x0018ù#¯\x0010\?R¨ÏX\x0018¸0Ò\x001e#ù1r³6I\x001cI<*úÑ.Æñ{\x0017\x0017È¸\x0007\x0019ý Ù¥S@\x000cßnYì(:ã9\x0011¦=ÂäGZØ¸¼¯5	#\x0005Åáü¬¾\x0007ùö\x0019¾Ö~A/ \x0004)nì\x001fZí\x0003Zÿ#§®xÎ0=Èâ\x0006Yk\x0011OèÒ?	S8Lò\x001eN!Î/tb¬{Õ\x001fÈ\x0010ääÞ\x0003©9lK­@>#~.m\x000f²ù\x0003ÚøÚ¡J×Cc++ä3¥¬\x001eãfåðpás·m×4æÊõs'ýÞ¹D](­Òø¥§\x001d®	ceáçiF\x0019\x001bX>ÒºP\x001a­\x0001¿ØÔTå:S»/®Dþ\x0017\x000b¥Q\x001bðËÍ_'FnÀ¯7µse¢±.×VK\x0001F,ÉÎ\(ä_sþ:±4²\x0003~Ý©Ã`rIÖÚëÆ=1\x0005=Ó¶îBit\x0007.\x0008\x000fDn\ÓXðÄJêw\x0010\x001e0Â\x0003~åYf K(\x0013ÉCT\x000feR§\x0003\x0013 ðÀ\x0005åù+D\x0012ðà\x0005áÁ*%(ã=ò¾M\x0000Ï¼¹P\x001aáÁ+ÂóW\x0008¥=ã\Ð\x001dlCwZêÏ h(é\x0019÷"\x0017J£;xEw¡­I[Ïß$a\x0010ú3þO.Fvðì\x0010'O.ákT\x000f¥¦èp>\x001dB#;xEvhä¿´ôÕ¬±\x0004òÌÕ\x000b¥!t¼BèI¼\x0017\x001a¥ÕTÅQSËz\x0007	GCx,Õ­§ð5KÕXF]ízx\x000fJ2<DWx¨ÏéçX©,ì(Å\x0017à\x001eDDö"ãÊ\x0016¯ëU\x0007YäÙ¨ÌºyàºV\x0017H³yèÊæiòzTB
òôÖQJ!\x0001ÞaÙ<taóôüWò\x0006âÓA6ýÞÏ¸åº0­C\x0017¶\x000e¢¼P\x0017\x0008\x0003d
ò\x0004LðL\x0013\x0007d4;'^Ø9=ù]ç2um\x0003\x0003ä3Ïè· \x000c]dÍU*ÿA¯RóöS¦þe\x0019\x0013ÆØØÓD[ÀIÉÐø'\x001f¡ýæÅÇ¬ü\x0007$ÜCÂ!%þëHÃf\x000e.÷ö¬g×\x00167{Pñö8µ"·\x00141 r)XªzºÒnÄ÷²\x0003Ó\x0018\x001b*<\x000e3p\x0016R¹\x0012â2¦ºÇT\x001d@çÿ¤	fõbn  NG¬ß\x0006jÜ5­<ÜªV9ËÇ\x001c´Odóþ\x000eõü%ãFTfÃí\x000b]µ×ÆÕªè#dDÒX?n\x0004eÖ98\x0016zÉÜÓ°¢Æþ\x0010\x000b(Ð|-úiÝÊ¬tp,õ\x0002:'0§<ï\x0003)*8ÍänC¨\x001c\x001f;\x0006ä\x0003ö
W¦¢&îÙüdq&7¢2_\x0010\x001d_05ñ¦är\x00015l¡*Ç\x001dÕéµï¨Ì\x0017DÇ\x0017ìMæQæVÙ\x0013uE¥[°¥Ó\x0006\x001bQ\x0019¶B\x0007]¥ø2>$õ¢ \x001a«|Ý\x000c]®Rkî½W,*:­ª\x0015 QÜ=ý+eéÓ¿µj<²ÖÙYÿ\x0013àJ{3ô?hÎðÙÛ?¿ûáÝ/\x001f©\x000f W(\x000e¿8ÒþÅ\x0002á\x0008ë³\x0017ß¼üâåw\x0006F{`ä\x0001Æ«kæP¸\x0001%\x0019¼ÂÖæ¥=°ä\x0002\x0006òzÎüÊ6ât¢k¿òÄÍÀò\x001eXv\x0001\x0013Cçþ%³<\x0008õÉÜ;Xúö'p=®âÁÚ\x001aÎ»àQ\0\x0014ëG£©\x000fY÷¸ª\x000bWÓ\x001c>ºs/çq×iÓÍ¸Ú\x001eWóàêÜ5âµØt­\x0001mÑØ­À¶li6x#2|\x0014`iPXÏáFìôoÆ\x0005\x0006\x00178pAk2g3é~J\x0014\x001f³²ð\x001f\x0019åò¤Þ&\x0017SoóÍ¿üï\x001f>~XNã¤Å\x0003Ø2¥%jPC>Ý|ýæuÇ÷\mÃ=8t[ÞÁÚ
®´ÕË\x0014[\x0011\x001f8¨\x0000Ï¸^\x000ep\x000c\x001eíñ7x \x0012x6RYð¥Z\x0004'\x0017÷à¢\x0017\x001c~Ùëz\x000bÐ¿,¬h=xí\x0019kÛöø\x0017_Èë­\x001e¤«ÕJ]Yw\x0005Ûgß8o÷ðòoomtZ¿mÑðá3íC·ã+{|Å¯ïK9<\x0001H\x0004Y{â{¦\x0010òv|u¯ºñ\x0001\x001bK,ËkÃ\x0015^\x0014xôìÍò­ðÚ\x001e^óÂ[çç¬ðp-ÓD¾/ï\x0019\x000bñm54\x000b/\x0007/@öqíËU\x001fëþ¥*Àø³Ùí\x0000­px#³Ñ´\x0004°®=§\x001d_Úð=S³~;>£\x001dà\x0015Te:ä*Y\x001d\x001ffÁáS\x001fø£Ü\x000cF8À«\x001c)\x001c\x0006;ûåõÁ\x001f\x001bµ¦ì\x0002Ï¾øß\x001a=CÎàeçâ!\x0006|ã'ìG\»,ìòeÒíø\x000cûþ\x0012×¾UÙ\x001e¸Þ¿#»(Àøluë'\x0000">¹|ç?¼êÿû_ÿÏ«ø\x001f\x00059Z\x001bw¹fG\x001dØúQªè!ÇÓ¯ûðêÛ/þë§á\x001e\x0018ºõCØújÑ.9<\x0007SN\x0015P`\x0006\x0018í\x000bX\x0008¹ d`ÒW×ÿcÚ\x0000vZkp#°¸\x0007\x0016]À é­Mã\x001eìµ£®\x001fÎ\x00060XÚ\x0003KÞÉ
D£¨í8\x0008ãS>ã\x001er#°¼\x0007}À3Î\x001a1½©ìÀJÕ\x001býÜ\x0008¬ì\x0015\x000f°X8ç\x001eØÕ\\x0002j\x001dKÿ4]º\x0011UÝ£ª.T­éÍ[KA½¸0¤±Àò\x000c°¶\x0007Ö\Àr[»ö\x0011rMkÃFr´kð}Gm\x0011î\x0011òôÚ¿d\x001eÈÎ{poDfißÅû|ñ\Å\x0012h\x0017ìèõ¼\x0003íFd÷ÁEü|QÆú?
ñÃTÎ>Ì\x0010?¸?²ã±ÆÆ:Ó×ê\x001e³ósÌÈ\x000cóúy>ÞY]+Ë"WHHÄhBÀ\x0010?¸¿ç°ùS\x001b¸\x0008°Eì<w¼\x0011a~pQD­-Ç\x0018\x0005öA=?³ÜÌP?¸¸*\x000cÎÈ \x001e4Az¡:°ó\x0016\x001b\x0019ö\x0007\x001fýsAÐA(#´ì¼ÝíFdþÁÅÿT`lÌ\x001e²uÖ|\x000cQ=Ó¡Îè8\x001a\x0001@\x0000\x0004
À%f²\x0001Â°Oé1;-µº\x0011\x0011\x0000t	\x0000eøÅ¾¼\x00122j[È&Ö?Ú¼ßÅÿT8~Fî]\\x0007ôõ_\x0006²s[\x001b\x0019þG\x0017ÿóì ´¬\x0004)\x0002 VtX54à4<.åY\x0015«ÏLd/¡µÐj\x001b&ßá|æÈ\x000cÏ¢gy$\x001f(Ïê°Å¾5uñÒ\x000e}\x001dáYtñ,¿ò\x0005Yg\x0015eä\x001dÕ:l Âù\x0018È\x001b\x0019¢E\x0017ÑR\FÜ¯ël¸£\x0011UÐN_ßo\x0005fx\x0016]<Ë/¶H#dEBVÆôÇsSÛ¡YrÑ,E}@è\x0011Cy·êÜKJ³Ï0ßÌ°\x0019ùØêÕ\x0004VP_/8\x001f}#*{áb2ä{dùYja¨Ò°ò\x000e3\x000792,¹\x0012YÂÈ¹Ø\x001a1õ|ì¸ÂXûç6¨7"3\x0014K.íD%ÃzÌTÉSÝ\x0006dS9\x0019%\x0017Åâ\x0005ÜcVuWö³ÓÙLMbÉE±=~Tmâ\x0003ÔÓÛáY\x0018ÎÛ\x001fn\x0004f\x0018\\x000c\x001dÒEú\x000câó\x0007ø[\x0019%\x0017Ã²­Î\x0012é©ãê\x0019²t<\x000828÷³»
Y4\x0014\x001b]\x0014Æ\x0011s=¡,1Ã1Â._³ßÌPltQ,ðÚ\x0012íá[ï=ûÎTòç\x001d0ÌÐltÑ,û\x0010©¯#?­ë,onØçÝÐ7\x0002³7Å.´q\x000e ãÃ¨TR\x001f8oE»\x0011¡Ùè¢Ùþo
CGDy Ô±.ì?\x001a.å&êË5\x001a!©Ð0\x000fÇs#ç\x001b\x0019\x001eM­&TÏ%u\x0012²2>f9ýFC³ÑE³¡r¾#ë\x001fÄ%6;]<÷\x000e½
X2d\d\x0016úñMi¶oL+°26s¿ÀudÌÌxI\x0011ç-2òH±éü­úFd33Ø\x0008¬èÇÌrcL9\x000ecºgzloDfvfòìÌÔ¸[§H1Ikx\x0003ÌÜe'³\x0001g\x0003¤Óf5\x0018¤öR,ÃÁjæÆ \x001d=; ñ\x0003ÎËá"×uk¦!ò\x0004Íf³\x0001²g\x0003¤ÖO\x0000º5³\x0004ã<M5³Û¾ßÌlìÙ\x0000©qB&\x001f³\x00141à\x001e\x0007%©+³lD3{D3Õ~\x0002Ð\x0019ô=MC\x00016©\x0004¹\x0011}_uíÌÚ\x000fMâàÏý)ë\x0001 ¦ÿL]åe#Ù%µK¦\x0001/E¨PZöÐ¿åLÈ\x000ced\x0017eT\x001e\x0015-ßAÊúÃô¸7çÞÌM²çljAyÌáR±î§H#Ïhaâk\x0016CfÅEfµÀð±®jáÔù-O\x001c4¹e/[öÄ½·$È\x001a*gPÑÇLl3OÅðlqñlåKEFâÎ¯ù"ç3°\x000cÉ\x0016\x0017ÉV¶$×Y.EnÿùI\x0016\x0019ñmÜudËËøõw\x0015¦¥×{ÍØ\x0002PÍ<ï
eµÐ`ø¡ÞX\x0004Qe.ÔòÖJò¢¥C\x0018 üâSý¿À\x0007B\x001aO\x0001EGXôøi\x0000¡Í$Ýù\x0010Áì`j4æ\x001c\x0014)£&NEêÜqý_ÿðäÀþ\x0007×é3È%Gb/½ 'v\x001cÆx>ÎíÖ7þÃòKÞå·öâiA\x0014\x0012vÒÛfîòS1;\x0001v
\x00195C\x001dw\x001e0.°pê\x001cY°~Þ·\x001ep\x001e«z -Û´>	\x0005\x0003:|^ò~^ÊZÈÄ½K\x000b·àVa5u+\x0013M°Æî÷Ø
\x001e»<¶FÄqÍ0SþBå@|ÅK|öÝ\x0018àøn<±ò¨\x001e\x0000V'@¬ÑÓz·\x001bôm£Ñ0Z¾ô|\x000c¥FSÌ0]_ï~ýó\x000fïß}øIì)Áz¼ï|\x0007¼Mø/\x0014y­
¡=3gãÛo^¾ùæW/_?_B=@Ò\x001e$]\x0000Yùx¿äù³+Æ*\x0013\x0003ðliq1ú1fgÝ1&yl¡I5"Oy¶\x000fâvi\x000f2ùAbed\x000bÈTÔ"8Du\x000f\x0000zÖÙÖ\x00012ïAæ\x000b-â\x000eáu^S\x000f$j é\x0001\x0017.e±ø1\x0006\x0011BÜ9¹Ö©·\x0000MAb¾Ã×®{Õ\x000f2ÊÕ5õô@\x001aa[ÿ¿l\x001aÈg¦À¸0¶=ÆæÆØPnW¨a«½\¦® ã¹¾¸@*ã$Ã}\x0013\x0007Kj\x000f%ï\x001bñíë(5ÿv ´TîçrÊI*î{,Ü\x0008Õ®2¿¼úP¢A\x0017¾8Xr9ìï \x0016\x0013N\x001d (â_rþ:±4\x0003~Ñ!&»géjX@ÖJ
ò¼ÔÄ\x0007Òh\x000eøEç¯\x0013J#:àW\x001dÊÄ\x0017"k(ë×Õ/\x0003Ò³Få\x000eFuÀ/;P\x001aÙ\x0001¿îPjl8¢«2Ä\x0012UxRz¶©ñfh8\x001dýNY_\x001c:Jõè(ÅY¿ø<§£aK¼À¤æ»}¯ãcu©-}Ýß!­DÃCxh·.ò\x0010

?/öôa4\x001b\x001c/lð¸x-\x0018yì\x0012­ ó ÿÜá¤³;/Êig¼ä8ð\x0004\x001ex£9pÃ\x0004/i\x000eülWëíXá)V¸U\x001bÔ©ðsÓú¤ö¬-ë§±b¬Opû\x001fôûÅÛ?½ýðËû\x001f?îiU\x001b×«Gì\x0007É°l¡~,\x0007¹!àæÎ\x0013_¼øòÅëï^}õ¼¯Õ\x0000{pè\x0002ÇÅ¢«'ÌANd)b;½ûq`£=6ò\x0005'çfÁ¦nÕ\x0019¾bú8 Å=´è¶Þq/ÐJäYçõÿÄ³Eç\x0000öà\x0013ÎéàÔw5ã¸oåt\x0003\Ù+>p<¢y½ÐÃäÂ'oÌ±
\x001dàê\x001e\uF\x000euÒ5\x0005g \x001e9½+K³_µí±5\x001f6Ú·è O\x0015[Ô©éÜ¾évp[/ìÂqÁ\x00199±úMÔI¸Hà²^Ó&ä8°\x0004ìdà¬üþY<!÷Ði\x000b\x0019'\x0010sè\x000c\x0003¡d¹\x0014KÄ\x0003ÒdGèô1>NÆÎp08I8E}J&Ò\x001dî¯\x0011õZü§Ð\x0019\x001a\x0006'\x000fWMª\x0012±_CQ\x0010\x001efÇâ9tÁKÄI_)æG\x0015í´sÝ-\x001blÙ\x00199m\x0011ì_0Kõ\x001a\x0017ëw=­wr3\x001a\x0001Nèò*\x0002ìÏ´-Ý\x000b\x0011\x0008p*\x0004»äÈvÈUª^{Ø´é?åÓ§Z\x0007:#\x0011àÔ~(OòQ³vØôÐîôðvth4\x0002\x001aÁ\x0019"\x0012Ä*¤ÇNKS9µ2s 3"N( p?\x000f¢KZ6Î}q\x001dèlî\x0014	.¶Øµ*>ý\x0010¡¡k§\x000f'\x000epF#Ð¨ÓêxÙ¿k\x0016§êþ]Q®\x0016\x001dàD S"Z®³\x0014\x0011GN7l:2\x0016\x001d9Ð\x0019@§Dô\x001c\x0018DÀZ6ª\x001e;ÏÒcwúþéIMö/Èè1ûæ­±xj¯9\x0000Ju\x0005v4C`À­¾b=Â¾õa\x0017ÃõrÖÏ°u\x001cbO[1]ø~oñýÞ»wQÏcUÊ±yïV=ò|YÎ\x001dàìÕ\x0004-³é×Õ÷åO?þòó_þóß~ýðQh©qÙtñuZIR(Xâè\x0015:=dùõWß}ûò·o^?\x001bº\x000e÷èÐ\x000eÎ{hýÈ#àêhJ\x0000:;9ÀÑ\x001e\x001cyÁÁ¨Ëf«©"èÆ\x0004p<mKv {tÑ®>×îaÔÄ\x0018é´ÒØ.íÑ%/:9d\x001d]\x0019µã5ní&sàò\x001e\vÃ0zÁ°¬°\x001cºQq\x001fOo\x0001\x001cèÊ\x001e]ñ.~\x0018Tcõepú@w&\x0018\x000etu®zcÒHºL\x001f
\x001e£À=v\x0005;Ðµ=ºæçÒ\x0006º\x0012J<Ôr;ºÍkuáâà
^\x001a{6Vy^ºø\x0005^:5\x0014sÀ³RáÕ
,&m\x00151jdÜº7ÏÕ\x001cð\x000c\x001dqäï!¡\,ÒÖÁOEÖ£d»DJÔLó(Ïæ\x0005-ôÍ£ÿcä¢xúöi\x0001²Í\x0005ø\x000f\x000b¼øáÝÿxûã÷\x001fÞ=|ûÓ¯úK|ÎÜý´1å¦FPqØ&\x0016:ã/^þ\x0017_}þúåÃ·_¿ùòcFö
öPé
Ô\x0012^a$>\x0013­\x000e\x001c1©ÿRÉ§7¢~¨i\x000f5]j­Ét¨EÝå"¬ÎNÓ|?Ô²Z®EU\x001dmS?|È
Gªº\x0014têh{z´\x000em³]
iÿä«_MJI>½\x0016DA9¯÷\x0004»®m§8ë_¼\x000f\x0017 Aý\x000bJ:í\x0011rx0Û	.í§¢ÌlIlå¾úSDjôt\x0002\x001f©ÙMpm;u\x001e
M®Q.ZW¬éL)ýXÍvKû)÷#\x0016ÑÀ%ªØ6¬÷Y\x0001fKÁ¥=ÅKtº\x0013\x0012Ô±óoÛTBf_á¥}:¡®5>\x001d*>u_Q(cµ¼ðc5û
/í«Äm»º¯@u
«¾*û,\x00004\x001b\x000b/m¬¾\x0016\x001f£®\x0000íf8\x001c
J:m\x0016ðc5\x001b\x000b/m,¶d^
jðLêÊ³>ïÌr¥kËµ@R¬eÁýøxjýãÇj³ªKË'jZU³Ì³ #£;ÖÓkz?V³^éÒz|\x001d¹B-UL\x001b#^Lx§%`+]Z®1$±qìâT_\\x001dúz^SåÇjt.é\x0000õý$·ÒÇP®\x00152*
àéÔ\x00147Öh¶V¼´µØ\x001fVvV*Ì³h<(\x000b¤ú¡\x0015/í,âþgª½N1®ì\x0002§Oé~¨fcÅK\x001b(è\x000blQ;È[Ó\x0012NçJ_Ð×ýÀHÑX=V;9v\x0014'/2+v¼X\x0003ÜEf@\x001dq\x001bÖD¿á>zþ÷íÛ÷?þòð\x000fïÞþøðý»ß~øËÿþON­áÛcéæ\x001bP\x0016Z\x001e\x000b£E\x001fÃÆ÷Û\x0017¯¾úîá\x001f^¾øêáó\x000f¿}ýò_öÓCô¶¢'¯\x0002­,7\x0001ÿøëÛ÷\x000f¯ßÿ·_?5&.â\x0008#\x001f±â:

Vdõ[ÿã\x0017¯\x001e^¿úÇ7\x001f\x001b\x0013§ÀÒ\x001eXò\x0000\x0003H
d1öã\x0019!ÐZ\x000e\x001eE.`e\x000f¬x%ÔkÅBê\x001eôWO³.Xm\x000f«9a­;xÜ(áÒ{â\x0016\x000e\x001dÑ\x001eXÛ]Ý²¾ÈÍ\x0006W\%;K¢&µÅÐð0\x0010É\x0005Ì¬/p-°ªÏM©´Åt\x0004éÔêÍÛ£¤\ÈÌ\x0002\x0003Ï
K!èÝfe{.\x001d1®'³\x000f\x0015î\x001edhÈ\x0002]lÁ>\x001ek²X»N1f\V«ejSî½\x000b1ø\x000f·ãë(\x0006]4rµ\x001e®\}«í)>ð\x0002ì\x0007íZåÓ<#öE§Ã\x000eÙ¶o\x001e\x0000\x0013àÿÏÜÛå
r\x001bY[©\x0015\Áà\x001füTî'\x000b¨\x001a%É@ÏQmm\x0001²ôMIj çi¶1;\x0018¯Ã;\x000c#3qUu\x0019Ì6ÚÝu¯PÒq$yND0~R/b+.s«)íÖ\x0006\x00018¼ÂN}aÿ§ÿó··¿¾{¯õ7¡ZÀíÏMµ\x0012÷©PµC\x001cö#=\x0007%M®VÏØÛ(ëvb^þç»ÈCùóß~øñÇw/^ÿðñÌqÅI¶ÒÑJ½z×£\x000cY\Zñå\x001f\x001f¿"\x0007å³?|ùêÕã×_~$ÿï<\x0019o0Ñ\x0002\x0013$±æçØ/\x001dc \x000cI@\x000bÌt,0±Ï^ÍwB$jÃçÁKÃK\x0005e9£,\x0016ªyeÚ×îÒxÖ>îhcyl*vüæ8³rXB³¢ÀüæaÝp4½ºAÞr\x001aSr"ÕSýÀ^æãû¦0,u±À\x000c
f0À¤Ù2+\x0007÷EÞ\x0016×Ë<!\x001eµÀT\x0017Ý[nz´~f³&D©éòIÜü0\x000eµàT7Ý[®zAÜ®>ð^ô\x0006³òx£û;Ì\x0015ÌlÙ>u\x0001]8tÃéû:ä£-8\x0015%y\x0003'µ¿':é±J-Ï\x0012×aª\x0005fU0«ÁiËéKå\x0017W§7\x0014¹\x001c'å\x001ap¢N0P'Íâ\x0019°>9.ÙH"esæa8¡\x0005§W8½ÅYz\x0010Ûÿj)½nÔÞk7§r\x000bNí%\x00198ÞÓ\Ý¹I\x0011ß¢,c¼B¹ãxâx°p|\x000bae&e¢Ä\x0018{s4\x0014\x0012Yp*\x0007\x0003É·ßJÉ\x000euÊTö²\x0004\x0017a((²À
f´9Çî\x0018¤Yù\x0016¡<æ11jÁ©´\x0008\x000cZä]ò\x001d/Û\x001bÎ"¹f¤õ(ë8\x0018Eö9_»G\x0017\x000e{\x0016ùìcúÞS\x0011XÄÈ;I5R\x001fr`/òÒþ\x000e\x000e\x001aEJÇfò<«xÈ²M*¦×q\x0006¥FÁ¢F>>TîJ\x000e@\x000f¹\x001bÎê¤Ó\x001cA\x0016JEJy\x0010.ó<ÄfNif	cÙ\x0002SQ°\x0011\x0015Ns«rtÝE®Ò"qØïgÁ©Ô(XÔ¨q\x0011÷\x00065LÒ'ïÔz4S[p*5
\x00165¢\x001cMà>*\x0010z¦2Ö7ÀT,\x001f,,ïû.\x0004ÀÞ¡î«øJ8&¼,8\x0015Ë\x0007\x000bË·xØ3ËÓvR\x0010g)\x000f½¯\x0016åå¡\x0008Îæµ?\x0000·®¹Þ·~\x0007É\x0007EòÁBòesÒølô°R\x001eæñ\x0018p¢"y´|ð"FÁË&øfÎ"ÝvþL"*G\x000bÉS\x0001ÙYF\x0002ø>"#;X	\x0015{¢=ÌU öY\x0011Í$s\x0015Â¸ÑSgf-ìÙ¤2KO4ô1\x0001^²\x0011Mp\x0016ÊG3O\x0019\x0006¹G4\Qb\x000eèNò0\x0014ÎSÑ'\x001aè<cî\x0006ynPÃ)mæ8nc³àTô\x0016úDÇÃgéñ¶\x000f¯¯îHÓ¡bO4°§w2)¯\¶¥é»5áP3*ö\x0016öñ\x0001°wy5CïÏwpQ±g4°§wFí®üV¿F½g\x0014Ó
·=*\x001f9Z|d\x001aã\x001b¸Ùq}{\x0002\x000e±ÜaNEòÑDò(\x0008\x000c°'q\x0017RJÃH$\x000bNEòÑBòÑ´5«;\x0019°Ø~VúDï(ë8\x0015ÉG\x000bÉû^Ô\x000eÙñNjZÖ(öÌñ\x0006_>*\x0016o¾¼Â*È\x001däË\x000bÉ¡\x001fÑSÑg´Ð'¸\x001ejÖ,âîky2\x000ew2àLà\x001aC¦\x0015_¾_w=ºïÉpß)³Ä@~\x0013ß÷"±QÒ\x001bîQRç3\x0010\x000e\x0012\x001bÅÉL[Rõ\]Éé/úå))ç±7
d-\x001cÚÉMï\x001c\x0003\oéhCFÞg¼u9nIÔ\x0001n1Áõ\x001eä-\x0016<_ý"\x000f±\x0008w¼y\x0004Ðe6\x0014ã_N#N\x0007&[ñH(µ¶\x0018ÙV
\x000c\x0018\x000cl;\x000e©pU\x000cDôAJ\x000e\x0001Ê
hÛé}bßvz-Æ¥e²X\x0012c\x0017\x0003'ùQÈÃLzS>ï©qyéÅ\x0017`é
\x0001Ù\x0015èIgwGZo8
Áv\x0016¼áÐ\x0011âñÖT%Í3\x0014Üê§`£\x0011l\x0004q\x0007Ü± ¥´åíÓX?ÐáZÒvÁþÎÛ[^þøóoï~ýõãUìÑåöé÷yÍe»\Ñï*ë«»ÞføøÍ¯¾þîñÛo\x001f?<y·C3D\x0018"?6Kg+7
\x0013Ä\x000fN]À\x0018Î\x0018ÁGTA\x000cÀEª\x0015]\x0012ázEÏ\x001cH<D!=Ïnì{Q0ì\x0008²dúÐ¼ò	ñ\x000c2Î¤ýZ-\x00199'^\x0003-cK^¶NLgi\x001ed3Üàd1JÓù* ×!æ3Äl°#<`7#ëP\x000f\x001fZ1\x0001±!\x0016\x0015·;ÆÐ/6x9áSß'@Ö3È:
2íý¾\x001bHás5½Gµ¼Ö3\x0007ò¨\x0000ÝXÜ\x0019¾¶$ï½ö
ÐN.
~pÆÿ\x0004H-5óZråé8
db?£´WP\x0013ÊËi`(ÚxÜP§\x0006ËMáÓn\x000e&A9$F\x000c(ÞøyÁ¡©\x0014È\x000cÔ=ÌJÏÇÝë ÞøyÁI5ÐëÖ\x00062\x0002? Ui< cý&Q*Áñóbà°Í\x00078VÚf'4´î_x%8~^qRÉ)e²G
9\x0011oð¼Ò\x001c?/:	åe³1zá}Ê5@?w\p¥:~^vR|#öSäê¸ãTÞ@Jv¼Aw@\x0006(o¦d.nÉõ\x000b\x000eJv`^v\x0012&®EnW'Ëîµ\x0000ýTâõÚÛ9JwÀ ;Üÿ´¡äý"Áù.áë
\x000e:È\x0014\x0012¯IÝÄ·?\x0006ß?8\x000eíO\x0006JvÀ ;ÿ
S*Ù\x0001ìÌÐÞ@\x0006\x001d×	\x001dÑ~ÁiQ¶
¼é\x0017\x0012xÿñç\x001f}ûÃûOÍ\x0011+¿¸a¡³Ü\x000bZeNuûÏ,þñëWß¾üòÍÝvhp\x0006SÐ|å±
ZäGàv\x001e]oj¿\x0010ø|hxSÐè?thl4õßþrGÐó¥3°4\x0003\x000ckå\x0017ª\x001d\x0018#ëíö«Èê\x0019YBFNCé\x0007mWº\x0016Å¸zÏAëaË~\x0007Ü\x001c¶ÊÏøÕöãÔv|Ï÷ôúzNÝO¤9òÇýLÜÐëüa¶+{>6u?ýÔ\x0005Å\x0002\³-ð'õ±\x001f¶Ë¹.ÏÇ\x0016\x0014¶0-yiù!»ío6¶\x000bv»­}SE\x001e~=\x001aÈ´ír»%(þzrËó±E-Na§Oìvã\x000e÷Ü\x001b\x000eW¯©â6?Gn)³îç-ó¬t\x0008ÂÚ7Í
[Âð\x0000Ù<Ç8®Ââ5-
Zû¤²dd7\x001bÒ\x0012kºöI(ø9U\x0008ñd¶Â}ö1ûn¶«ÈâÙÐ@\x0002ÌBE{Ù?iáu«f\x0003¥
0§
\x0010\x000e\x0006qÜw\x0019\x0003ÂqÜ®²çÏÇ¦½¶9UÀÈÔÝn}RL¸ÉnJ\x0015`N\x0015h}>ìe\x001a\x0011Þd7¥
0§
¨Î\x0017»~\x0017ÚÌ9lJ\x0015`N\x0015º¦,¦ u:ËfS¢\x0000s¢\x0010\x001f5÷(\x0019$Ö¬¦4\x0001¦4!\x0014D	Ý 7Pyª×YÁ¦\x0017¦ö\x0005Wqy=\x000fþpÄ	kÐ"Þ0E¼!»#$Í<à4ÂÉ\x0005\x0019JXæ°)â
SÄ\x001b``]Ô]>¿<\x001fbÝ0Åº!Ão\x001a%*öíØ.ðÏÇ¦X7L±npéo(&\x001eYÜ{\x0019YìÊÐb¢ ]Ö\x001ct\qÃ\x0014ã\x0010\x001e|g\x000e\x001e6\x0005Áße2E¸ap¡¤³\x001b¾¯w>c§%doÃ\x0014ß\x0006z­?R\x001fo'pÕ\x0014á)Â\©T¬Æ®OÒÔÒHm9\x0017\x001e¦¼p*pÅÓ\x0005Ýs\x000c4{¢Ûmé¢b\c\º ùÀæåvhKÈ\x0014­á\x0014­\x0001\x0015ØAG;Êá°]>=\x001f¢5¢5ªZÌ|\x0013bÑ\x000eäºZn\x0002êüä\x0014µQyºKÝn<âÏgß=¶Ë×¯çcSÜSÜæã!U©î{LiqS¿¤CÇ\x001c4En8En´àº»\x001eI<¶sBk)tAÅm8Åm¦ý¬Æ§ÍËÔe³)nÃ)n(/1Ùö:©xTÄz9,÷ùØ£Sî¶!¼\x001cvããæd9ØªÝ¢âÝ8Å»² |³\x001bçÄ}\x001fáì¯÷\?\x001fòtã§ÛäÛë7-uûÜöÚ{Hí¦T!Î©\x0002ù ¾³\x001b²ÝëZºtÜ¢\x00128'
\x0001xCËvÜÍVzÖÈ
S\x001eæ°)Qs¢\x0000á¡ðzÆ¦øûÚèüé8Ðc\x000e\x00128'

[JÝní[ºLiBÒ\x0004ÚÑÜ/\x0002SÙî}÷`IJ£"Þ8E¼Û\x0018¦Ã=Ú+q¨Ì?ÝM\x0011o#^\x001a¾åµÌcí³?\x0017¿hR´¦h×\x0013×\x001e_C\x0018\x0017j+Xâ¤h7MÑnP\x001e\x000eµÚã>¬\x0008Ý9ºÜñ|huÓ\x0014ëÒ\x000c5D0À\x0017!@W+XR¤h7MÑnóµûërJ\x000f{ÿ\x001bÖ¾ÁË\x000f]#sÐ\x0014ë¦)Ömá§|Q²\x001a_Ñ#S¿h4Å¹isi\x0010\x0015úsAÚ\x000f®cc]\x001aÙxÜÑ(Á\x0015ÜClIyâiÊ\x0013w´\x001bæ¸¢ûÚ÷Z5«­ASzæô fÞ´²9rEýá¯%\x0019Ò4¥\x00074Z9ÔÚ\9NÛÒ\x001dÍJ\x0011ò"`å!M{\x00008Hè2z¹|ùùÐ ä9AÈ®?"4& fëp¹SûùØ\x0014ëæ9Ö2ÍÝÙÝ÷{zÕÒÛKV¬çX7ø\x0007ÿD«\x001b~<¦
Û=æ )jËsÔ\x0006ñ	DötÓAmkVSÔç¨
K¯° \x000fºs[)>ÝôE\x0015·å9nÓ³\x0010Êv®ÝñIW \x0015E\x001fe>h¸}ÿ¢}d©§¢%²(þ(sü¡\x0017iÅÊ\x0005=Är¤üøãË'¡)²L94Ó«\x001c/Þ/i8j´Îä9lÚÊ\x001cµÐ\x0013ÏÍ\x0015Á=|)Çk¼[_â¶2Åmí<\x001cIñÈ¾\x0011Öo´ôv[KYæ\Ê ûG¶ÓÆÛþJZ£\x0016Þ¬M[#·F é 7Á¹gP×ÞrÊsäC\x000fI	Û\x000e-\x001e,§¥[Z\x0015¹Õ9r\x000bùLnìï£èn­R *n«sÜæò\x0003\x001c.å¾L¦­§fÜ0/}\x000e"·:GnÍ\x0001Ár
Øl§â¥P\x0015¹Õ9rsG$ßìÆÐ àM§Mq[ã6_\x0008&pE»¤\x00087M[!·Tk<ÇË±ùt\x0010ÈR,_SY§Êö§y;Ìf7«\x0010zò²\x000füùØ\x0014ñÖ\x0019âMµÔ~\x0015hv
\x0013ïé.ynU9uÊ©tîôr\x0015xp»
GûËåÊ×çcÓ
\x00133TR^ÌÆ[î«í\x0016íæ\x0012\x0005úqê.ÜíÆÏ\x001c\x0005\x0017¥R(ÿ¤£ÉÍÈB3Ü\x0011)îüK<Ôtå.xÝÓD?N\x0019\x000e=<\x0014!pÔ¨¬\x0010×]MÛg¹©ùh	Ü\x0015¿íOéuíÈéê7Cq
\x001cð\
g;½ú-AÓ\x0015önFÚ;©ÈÈvU¡SÜRáÒÜ4ÕÝ*GèàRåëÐëÿÝeçûóÁéë0ÕCÔÀêP[¯0çäê\x0012<éÓjÔI5¦ÎÀYb>\ß%dú.LµÂ4dîx\x000cÜûÚ\x001d¯kk,ò¤ßdªá$ÕSÉ\x0005\x0015\x001fñ7å*ûè´pm?Ï ;9æ{;\x001d\x001cw»}<Aþç·ß¿ýå×÷\x001fö§¿\x000càþ2ND_\x001a8\x0015ÀË)X\x0013õ\x0003§abRC \x001b²YFàSª§G½ZÐrT2.E]eXf!Òþ´p\\x000fÎ,Rþ\x0018\x000bBh÷Nõ[Ó/Ag/^¿ýë»~}ûql9\x0014jlØRrEª0(+¼a/ÝºÏ\x001f_¼~ùÅãWß¾ü4<8ÃIx(Ýb
^^Ìeª
Ý\x0007úÕ.ÑItqÛÆº££wÕ
\À*è.\x000b¦fÐá\x0019\x001dN¢K2
pû´ÈðxÇöi¯'¯=\x001f^<Ãð'õ\x0017xÜ?S,·ÁKgxiþä\x0001<Í¡íäñÂlHÄ0kðò\x0019^yKlJ\x0001\x0011åbtxÃfgÂ£EV¶ÍL+/üwï}ñíÏ÷_x ©ùh¼+Ò@æ\x0012v^¾\x001c©÷òÕï\x001fß|ûâÛ¯_?þû§!Â\x0019"ÌB\x0004'»\x001a\x0019WÞ6B\x0003Ä3Ë\x000es\x0010Ã\x0019b·âQ\x000bß¢!)©J²¦ÉÃåX9x\x0016+\x0002¯³¤EgüZ²ø¥a\x0018??\x000f1!F\x0015\x001d§ÊÚ_fùÐ½ì%\º1s\x0010Ó\x0019b(dM%/üÂC\x0013$ò\x0018÷qÍC,ge\x001ebüv
Qñ]êÁQ\x001a\x0008ÍC¬gu\x001e¢Ì~kg±räKÛ¾%òÅa\x0004î4Ä\x001eýî¼èæ1zYúK\x000fÜë^c\x001fØ.£ó9»
ä¼7¨FÇµXÍ½\x0014<®ÓWäí§ÙÛBµÖ\x001d£ÌLÛ´·Ýù2¯6Q±·7Ð·ìRmv7å±÷2Å²|«½¢o?ÍßdG8ö½*vuÄå²\x0002d\x000e£âoo ð ï	VË9Ü>]\x0016àÍaT\x0004îç\x0019¼ésáó\x0017~*³¡ºõ{\x0015Æl±#v\x0006ïW¦\x001a§Ë¢·9Jdü¼ÊÃf,Fn±\x0019e@|]W\x0019¯TÆ\x001bd&Èp}z= Ï%ÛS\x0018AÉ\x000cLË\x000c´pYè±ù<R²*¡³\x000f×5«s\x0018ÌÀ¼ÌÆÛìôÐ\x001aZi\x0018\x0010zëw9ÂÁ@áN\x0012t5o\x0015BOäÚ]N\x001fÃ¨(\x001c\x000c\x00149§NmG¼»îl0¹\x001e}5QQ8ÌSø¿â[+
\x0007\x0003o~ÄnGÙæI^Z·ãe1õ\x001cFEá0OáM®=/Ðp²¯äZì\x00083Zç0*\x000e\x0007\x0003Gî|´V\\x0019ìKaX9Qq8Ìsø¿à<\x0006Åáa>Th\x0018\x001f\x0003p×ãù<¸Qqxø\x001fÉáA
Á\x0010*àCÜÍ\x0018r
Qbë|ùZ\x0007ç\x0006¯\x000c-x¾>ÊXHyÙ¥\x0008JfAfPv\Ó.î í}r\x001aãzÀ\x0015Ê\x0004ÊàîàRê¤w \x000c\x0012r9i\x000e¢\x0012`\x0010\x0019\x0019ªÞB¬#¶Æ(ä.KÇç0*	\x0006	²uÝÞÉ	õrÐÅ\x001cF%2Á 2A¶sÒ\x000c\x0007qp\x0011å8¦²nG%2Á 2
óö`¦<$/\x00189G±M-_ÄJdÐ 2\x0012ÌDJ@E\x0014vÌiÙÁE%2h\x0010\x0019 \x0016=)\¾Ú0î]ùÃ¨D\x0006
"\x0003²ÃÚç,Ã\x001bFÙµ]nøÖJeÐ 2 ¹\x001er\x001eOv¬ËÁ5êç\x0004ÊHaUÜØ¼ÛQÎc½\x000b0QÉ\x000c\x001adÆóãV¤-¬Ã¥é!\x001b0*AÎø\x001e\x0014Ò¦\x0011Åý´s\x0018Î Ag\x00043í~\x001cw¦\x0007®ñ²Âo\x000e£Ò\x00194èçáE\x0011\x001cÒ.¡\x001d£\x000c/Âëâ¦9Jgp^gråF¸5\x0013.Å!]Ö[OaÃã<÷\x001dG4Âè¡9H\x0002q=¶\x001eã<=f¼Þ¤ÐsÙ:a+Ý:FEq\x001e+Ê\x0002M -p|\x001c£ô
aX¿ÖQ?·ÎÓ#Ù?5¹á£\x001d/\x000bcæ0*êóÔCÇé1{®Ý9A,¥ös\x0010\x0015óÄyæi\x0010eqv\x0003%\x0013rBáÐ\x001aqÝëy¢y,Ë%2ç±
£(aYRHÊÃMó\x001e.\x001dGYèeRªëÓH;¾¢H\x001d\x001d`¤ìYo«¨õúBR\x001en÷pû@Ë\x0008±ô<JYÚ\x0018o°£¢ðd ð\x001e%¯G"×^±\x001anx>JÂÓ<SH½A\x000cT¼*J(5=ñYR\x000c\x000c\x000c)ZÝÍX¹/Ì(>Ïz,tÁÌ¼KÛ\x0003v+\x0006|bE\x001dópÙm9\x0007QiL2hLð\x001f\åýy
£4°àõ¼Ð9JdAdë§c uraä=ÖF,cT"æEf\x001f1¹Ùí%Z$ÄsÃGV"M"³¯!íÎ\x001c>\x000c\x0012×ãì\x0014Æ·W³¥;@¥0Ù 0Q>4 £©É;À¾\x001c\x001c/÷$Î\x0019Q)L6(\x000cÊ	-F(bD/6ÌËÌÀdÀô°ÌdÖ±\x0012~ý(*}É\x0006}	Ä\x0015S \x0017r·¢ToÅx¹=x\x000e£\x0012l\x0010\x0018©ÚVÕÐ\x001cÆx9l\x000e¢\x0012l\x0010`\x000e-ÊAê\x0018×_ß²RlPÿþÓ¨\x0004&\x001b\x0004¦çÀCï¿:AéÓ¨\x0004&\x001b¢\x0018´\x001c&W²À¼ÜPÎS\x0014{\x0017\x0003{\x0003/=@	©ðäNS\x0007å2FÅÞÅÀÞnïÂ¡fép}!E,\x0003tæ *ö.\x0006öîIúm©X\x0005\x0006Ëåò÷9½½\x001d¯4èð¸ÒòZ\x001dËeì\x001cFEÅ@ÛÃå1~_@\x001cÛt=b{\x000e£¢Æb¢FöÇ|_âzxp9s\x000e .§7\x0010£Û\x0017DÚ;Yl(&¼\x001cn6PÑb1Ð¢,|§õJ\x000fÂÜÝ¥õ=FS\x0010«r»«ÁívÜ \x0013@Å'Vu\x0001¬º«º\x001dy²»\x0015£lOif\x0014wÌ¯§MªâÅjàE©rlÑ´Ò\x000eH\x0012\x0004ÒòÑUÊc¬ó\x001e#wd3RoÞ\x000eÑ\x000bu7\x001fm9|©rê<å47±/Çpnð=\x0006üôiüh\x000cXu{-f|õ\x0018c+ëÉ"Õ§~ÿ¤mÐÍ_\x0017\x001aÇ*Ñ\x000bö7AÚ\x00185Úë®¼m\x0018Ñ,ÈÂs\x000ci\x0007c¤îÃcZ¯pÄ|ê<\x0007Vé<¹ÚI<G\x001fúÂM\x0017dn\x0004õó¯?Æ<\x001amP\x000b·oE\x001a\x0018\x001c¤?Ëy\x0008%\x0014U\x0005jñ<-r+q½"Eª\x0014n(q-ð\x0014jû7Z¬êúj~y?«'¿|ýÁpøþÑ´÷,\x0010J·kè%]y½|Ïáðý-H©¢¦\x0010»¦GÙ¹\x000eériòdÑÔÔ[ ¦H\x0005\x0001ûI²ÏõùzÍ³[
õ)T¨¦Kõß_KËS¨Í8ÆKÅÞ;Â)\x0002\x0012¿s=Q£É¨´©¬òËb\x0010'>ô¯º\x001e	Uÿ§·O|ä·\x0006{V¸pãº\x001cjcRºúß _Ð¸ßÿüÛïþóíûïiìÂ\x001fþóç\x001fø8Ê\x0002Ò\x0014ÉW/¾ðÌRY¿ÿú»W|ùæs½ðæË?~ýêËO\x0002íïN\x001bPzwFJÛÉÃ>\x001e¢]ª$ÓYI[ìO/½\x0001h@eQúq\x001eir\x000bZR\x000eUø)Fvì!µÆ\x0006¨Ø{¬6¨ôã<Ô\x0016\x001bqÒ:eßwò=ÈcÐ\x0002´Àï@)ð\x0007J»â\x000eÔ\x0010)"¿·[5ÔyZ êÏ¦Ï\x001f}äÕ\x001aÍ¦Az0d±j\x001aö\x0016Z öêµ\x001d*Õ\x001fÍCí)S¢*ä=c\x0004j\x001cæ ê\x001aM'ÕyL½£ß\x001dªÌþÉièÕ°@í¦;Tz5gªR8hng5õ\x0003àB?\x0000Ãp\x000e\x0013Ô ¡\x0006\x0013ÔúÀ3w*RÄ·©µï?¬q° -Ú¨ÅdTrú\x0018éVç¶ÓÏ\x001f©^&¤U#­\x0016¤TºÊc é'\x0005C\x000eÃÄ\x000e\x0003ÒèMéG\x0003ÒèÙåkFíO!
R\x001cævXzÔ$JêÏ\x0011_²jRÿ§Î\x0005*h¨`
^®Té;\x0003øþù\x0001\x0019\x0016¤A#
6£rî¬!²'`W¼ÃM¨¢\x0005i([ÅÖ\x0006µ¹;R(A.?ä\x001bh*öþ\x0004F,6uÈÏ×
¨¬*iÇËA
Ãò\x0008\x000bÔ¨\x001aMF¥õâL©	x67\x0015:LI± M\x001ai2!MRDRìO"\x0010½Ôa¶\x0005©þhþ¡3*\x0016qSáp¨ÜP×e4ÔdJ«¿#O\x0003LÜ¼àÄ}©\x000c= \x0016 ýEq\x0007JÔ7\x000f´è)äø}ìc\x0015Ë2@ÍNÝþ­/b\x001ejsRöÚñ<Ê@\x001fD¦R\x001eju-PAE)Û=JÚÏwªÅ«Ü\x0004´í{g¨wÄ~Y³6±?m64AÍ÷Ìtõì¥¶«vuMQJyúê;ÔÀ\x001bÛ¢Ëô(5gýý³éûÓÃý¨ÆâP7¿R¾\x001c¨\x0006¨\x0005TìO?ÎC¥}v[\x0011zy9dJ\x000bw(UÑGµªGéeJ$u°-Å\x0003ùúP&&M8½Æi	üýþ(b\x0013)\x001f^e\x0003$?¼XpF\x0015KÑ\x0006ÁsÃP\x0013~äM:5%9¤nx>± ÕrZLrZj\x0010Ç¯¸¾3½:ñûK\x001c¦*Y V}ªå>ezÜÓ\x0013T%¸sTBRí¼Þðù«SÇ~GJcçöå*%ýa[üÇHc¹#Ru\x0016~4 MI>\x000b\x001bi\x0011ë´p¶\x001fâØíd\x001a4TKÎÇ%ÇÏç	«õv¥8±j\x001aªMP£j9©.\x0016n»lÞtîkp2×k5¨ÃÈ7\x0013Ô¤¡Z\?×\Ó½û¢@Y¿[¯·èiuYCµ¼¤¸(;\x0010\x0012åªd 7aÂE\x0015¸	iÕH-ôïB}\x0010Êô2,lâuIu~ªZòS©6qªµ#
¼\x0003DR\x001bÔ\x001b\x001c¿êõõ÷¦ëï\x0013\x000f=n¸e5ÄR1\x000cë`L8õÝ÷¦»ï¶õ\x001c;NÿàQ=?H7¨wxSÕ\x0017
Õ\x0010¡¦JÃÙ¤eë\x001eÞ¾>­~eZá~¨5l½}+F¥âÈ½Àëõ\x000fþÛ»\x001f_üñÝû¿¾ûåã()vÚ÷s¶8\
îQ9Bõõ=¯¿üì\x000f¯^üññÍ\x0017ß|\x001a#1Â4FOó£ù§Éè\x001e\x001c¼ò¦Ë¹ ñ\x000c\x0012çA¶ãè\x000b\x000c\x001cåÜU\x0001y9\x001f~\x0012d:Ló Éuâ]ì\xP\x0013\ÎTXÎ\x0010Ë<Ä\x0012x½y(SìB®UìxÝ¥2\x0007²³û~kÜ<ÊæØsî9CóA·ÇP¼d\x001fr¾,áD©î¿84ÈÅU®9àá\x000f¡Gùr\x0012É$Duküüµ\x0001z\x0017G¼_.Ð+8òåx³IêÚøù{Ó<u*ØPbe3\x0014Ùþ\x000cùzlÁ$JusüüÕû\x0013sí·¡:ßQ^î"DY\x0015Êjà *Ùð\"+N»à¡Gí\x0016s(A]p¿àÔ\x001f'\x0005±ò+h¨^â¡â.Ç\x0017N¢ÔÂh¸à{ùà²Åi\x0007	®+î\x0006Í\x0001uÅÁpÅKåu¯[j¡VF)¡E¹î¯D©®8Ì_ñà<7¶·c	\x000f\x000c\x0012yw
m\x0007¸\x0001¤ºá0Ã©Ï/8µï\x0001E»r(ýeáð\x001cÈ ®N¿:T·O\x0012K%ÈÎ&ôío0Ê<Ô\x0018Pª«\x0013æ¯\x000e\x0016ÙW
\x0002¯\C@Nåå"Iêêù«CY#~å*1)Á:<r\x001aPª«\x0013æ¯\x000eÕ\x000b²:´­ÈÜP¶ã((o\x0000©®N¿:\x00113=\x0012í \x0019!Æðrùú\x001cDT\x0017\x0007ç/N¤\x0016\x0019¢tÛ $)\x0013(õ²oi\x0012¥º88qbÎ\½ÞPfYóØ>6£¬\x0013Å&Aê`lþâ´0Q=G\x0014lµ«4Èz\x0019¤º78oRþ:@K\x000cw

½$¸º\x001b4\x0007ÕÅÁùÓþ\x000bèsóeòÖûç¾\x0001¤r*qÞ©L4\x0015o7flI	\x001aëåì9Q]ï8½©\x0006}¿Þû\x0008"\x000c¥ëb­ë×;ª|PO\x0008QÅ7?®5\x0017$Pb]¤5^6 N¢\x000c
e·eí(\x000be«÷SÙX\x0008$ou¹öåy(}¬NåÖè\x0017[û_?¿ÿõ·>µ
7UnFA*MÛ_üiWÛî»Jm#¼ÿõõo¿ûêÃ«p;08\x0003\x0019`ÍX¼3½}i±[\x0005.jÀ.µúÙÀÂ\x0019X\x0001\x0016%*lÀ{â°T¦\x00197TÇOÁÂ3,úÂwXAòÍ¦T1¬ËmWÏ\x0006\x0016ÏÀâ½Âg\ñÁók]\x0005u9WèÙ°Ò\x0019V²\x0014ä7\IÒÉÙä|Ká}6°|\x0006g¡Ô5`'ýÑûf?_9äg\x0003+g`eêC&.¹Ùe~x«7áªg\uÊ`í!?³Ñtw9b+Àõ\x001b·º)9ÙtLü&dB®Ó\x0006
Lþ\x0014ëSß\x0014ãBnF¡òqáe\x000bâ³)Ò÷S¬¿÷î
2~ÛÏ¼_-}JEú~õ!õCVd\x0000È\x00039\x001a²ËþÒg#S¼ï§?dÙHLÈäøgçïA¦ßO1?xaþêx06\x0016êÊ``ì
LQ¿â~*Ëª\x001dó\x000fÂý¸De^q¿"¼³\x001eåy÷G³¨åõ`äg\x0003SÜï§È\x001f¶'\x000f\x0001\x0016Ùë\x000b'dK\¦ØßOÑ¿ßRîÈ"ÏùÄ\x0012\x001c³ë\x0005ÏE\x0006þaþÛÇìÈ²$î
v\x00176^ºþÏF¦ø\x001f¦øßÅîõ×Ì½\x0013ÍfN)^\x001e}62íõO	Å	T@\x001dè;².×L)\x0000L)\x0000íR÷\x001d\x0014tÈÔ,,}M¥\x00000¥\x0000\x000e¸zî)/ãmÈzD²Äf \x0004\x0000&\x0004 )ït\x0017¸9¿árÂfq)¶\x0004%\x00000%\x0000ÎñÓ=ãèyÂ\x0019ér~ñ³)\x0001	\x0001h&±$S½\x0010Ócíßréü+\x0005	\x0005Hµ$^ÖlÆº$\x0001Í`´
KÑ?LÐ%\Ê4M
æºË\x0018/··?\x0017YPô\x001f&è¿!,Z3\x0018p/]CæåS¦¡;}
¢ÿ0Aÿò+¹\x0016»Í*{Ù¹§|ÒR¼\x0014\x0014ù	òO´Ï7Éµâýä\x001aD0¯+Lç|&È¿!kîOÃÏû|\x001a2ßm6ïx\x000e2ÊÊ¨ü\x001dýBòwýííû\x001fßýòâóß~üñ>¯ù_¼('A
\x001ciÔK\x0015B¹)ôÙ\x001f^¾yõøÍÏ¿{õêË¯>
\x0013Î0Á\x0002³÷Aooía²B¸®ô\x0019Î0
æ¾¯Y\x0013\x000fR\x000e\x001bÊå»ð,L<ÃÄy´1Ç_ÐGO\mèÄÅß2QF\x0003J\x001fxIijþ%¿Â\x0005\x001aÍÈ0ëÐþ6\x0001³}\x001f}4é\x0017r4¿÷âõÛÿëí_ß¿ý8ÆLKãe\x0015Vûà¼¤¤fÙ)´bdÄøùã×/ÿ_¼yù\x000cx\x0006³\x0000[ø%»5)ÈÙ{È6\x0007J\x0000^\x0019q
`<\x0003³\x0000]êK\x0002[H\x001dØA¡»¼2S\x0000Ó\x0019`¶`!\x000ft\x0007dOM}¦¸»,)\x0002Ï\x0000ó´\x0005\x001dµïcÁª\x000c\x0014¯RÛÞ\x0000º+ñ\x0002XÎ\x0000Ë,Àv3ô3{sxEè\x0016¼|o\x0002XÏ\x0000ë$Àr,w¥qÜ\x0019V\x001döKrÑÁwªÆÅ#\x0017<õSègWäÔ>¥û3è\x0015\x000fúY",9÷=4§foVï[þ²Vx
_PøÂ,¾\x0014\x001eä\x0008\x0006®ß¥¸nÀËìÀ\x0014@ÅÓ~¨KÈr3`ât©+¿,:B¨ÚÏ2u27£!\x0004Y\x001aVòÉ«\x0000\x0015QûY¦Þ\x0006ù\x001d&\x00141ô3xÐB¨ÚÏRuÁcÓ5%C\x0019`§\x0019¼z=Â§ÚÏ2u	 ËÂ¨Oy¦ ÄnÁU¦ö©ý4Up¬3C*gÝ\x0011.v¸*v ¸\x001af¹ºø¾á\x001a(¿¶«]ñ2$\x001eýÐ¼;Ð+~\x0016!dI#ï Ý\x0010Êü+Ú	·zO@{Õ³jéqElØ´y¿(¹öí\x001eþ2Ó0Pé	Lë/Üf´Ùç\x001d\x0015À~\x000e/SS\x0008 À¬ P·{ÎÝ</ç~SüªS\x0003JO`VO_ÈídSÃnaûmºÍ-\x0004%(0+(9\x0015q\ÉMBí&\¶¡\x0012\x0014\x0015,\x0008ó3çS?/³¾S\x0008¤À¬¤ä$U)Í}9JN}Ý¿â§\x0010*IYIÉT>ë»
«|åØÃÕc\x0018¢YEÙ:
\x0010y\x001aDÌ\x0018\x000f\x0013®\x0002T\x0012f\x0005%#rZxs¼vMÎáÐäË¢î)JOÂ´PiTéÐ³\x0005C\x000fýåþå)­Ã4[·\x000f+\x001b¢SÆT°SÍª\x0004ÅÖa­ÝR÷\x000ckb|é>ß:(²\x000e³dM<y
8xGÊ²!Lµ[ð²\x0004b
¡¢Â0KÛ\x0004OQä"Ã<SÜ¿ñ2Ó(*\x000c³Tú;Êæ»ò°ñµûÿ«Og\x0010¢âBåÂD/P¡Û÷6®î7y\x00189Py8ë\x0019&(\ð²sÍnC\x001a&>Ãr\x000cúõÝû'é\x001aúÍd8_eß\x0016¶ãM>Òurüyí\x0000½\x0007\x0013©Ú×ÞÔ"Ù¹RJÏ\x0010_¾¹?\x000b¨/ú\x0019~AÏh/üñÿh\x0018ÿ¿ÿûÿùòÿøéíÇ_*h\x001a\x0002¿½ÓLIÏ
\x0005BÞ®áÁöå«W
ã/\x001f¿zùixp\x0007ÓðB}àÊ°¿Òª\x0013V¬Í\x001c´p\x0016æ-½48D\x000eçå"\x0008¼azØ\x001c<<ÃÃixèx\x000e\x0013uSòx²¼ÞºaÂÉ\x001c¼x\x0017-Ö«q\x0017e²\x0000YO
\x0005üð7\x0007/á%õ¤&æÅzQ
Lýð*?\x0007/áåyëÅÞQdæ
R5s¯K_³^=Ã«ó·ÖSÐNðJó¯ùæ"÷?xWáSè\x0017òÜüÇ\x0005\x001a-u\=\x001cÂ\x001e\x001cúMçðiJçäf>®Ô¢Ü?÷p6ó±j¸:ÈÛ\x001c>ÅÉ~1ðà½^+ýzùQ|êjÍáSÄìç9ðÞ\x0001,´ZÌÇeëí\x000f
~Ö\x001c<EÌÞÀÌA*\x000eóõºáÑs\x000ebf?OÍ!ðªPj=ëÝ{\x0015Ù
ôqè)Ã§¨Ù\x001b¸9Hq¦áÒíWó¥Ã§¸ÙÏs¹>X\x0003<xa?äxÓ§a8É\x001c¾¢ð\x0015ý*ÛFüª"âQ\x0016ñ)ñð\x0006õ@Îþ6¥\x0007'öã@Îça É\x0014<Pê\x0001óêÑ'ä4óñ>b\x0011D<ÊðØ9\x0007O\x0007\x0018ÄC¶\x00194E\x0019÷ÐþZnï0±i\x000eöç
Ú{ë?mÝà¤/=á¾q\x0011Ü\x001c<%\x001d0-\x001d©T´í\x001aÐì«Íz+k}\x000b×ð)í\x0000v t¼æ\x0008\x000fâV¡¾±I}\x000e\x000e\x000er§Äzó\x0007ØþÃÌ×þoíð)å\x0000rÈ\x0016BÌÉó\x001b1O\x001cÓq"Ó\x001c>¥\x001c`P¼ï¡¡\x0015ñÒU_¡}ó%xÁ@Ìú&7|á:ª¬b\x001fÆ8L¡\x000bÉ«g·ª´àr¯Æ£M¼æ4$Êçð)b\x000e\x0006bÎ\`Ûð^\x001a¸¥°èö\x0005ÅÌÁÀÌZ<¥A0R\x001cÎQÇ°\x0006g\x000eN·\x0018¼úÌÔÜ¾)p½*Jge3ß°ýd\x000ebæ``æÞQ($Ob>ÎIúqú×\x001c>EÍÁàÕ\x000b¾Hc\x0013|\x0012óñ5¡.a\x000eâæ`àæÂo Ô^/öÑó\x0010Gß>ðÚ÷UÜ\x001cLÜÌO­Ç§ä\÷9|Ê«\x000f\x0006¯¾P(´i/½´Êù¤\x000fCµô\x001c>%\x001eÁ \x001e2\x0017¾y{ád?¡¿:tÂJ>Ð \x001fwÿbõéd?æ\x0017¿(¾¨ä\x0003çå\x0003='­È_&Ñè@v½»µD=*ù@|Tv\x000e°	$­¢ w\£3\x0007O©\x0007Î«G3_eßª¢øV´\ÌÖÌ§³õ\x0006ù¨p®\x0014õ\x0002P×¼\x0003Tò\x0006ù("\x001fÍ\x0013à'êv}å%+ÀZàJ>p^>¢\x0010-\x0002fµè\x0011zà¶vþ|à¼|´ÐÃqÅ\x0018ÍíY/«ûæð)ùÀyùÈEæ®@¼l>º¦\x001e¨Ô\x0003çÕ£]_ä"øR:;;×\x0017È\x000f­6Sø¢R8¯\x001eqë Úé¥ÈÜUØÙ¯åÔ¢RhS£:BN_/µ\x001bz\x001cæÐ)íóÚ\x0011c¯êíë·Éz\êò9|J<¢A<B¯G¥EL]<¤ú%\x000fuvsøxÄyñ©7\x0001>»Z\x001dØ~¸h?ýÖ;/\x001e´bQq%Ñõî²wJ<¢A<\x0012ç]|ô2\x001a¾Ø|±,½·E¥\x001dÑ \x001dQJÊ¯GÒT
\x001aå¬}^¥\x001dÑ \x001d\x001eQwû\x0015qíOö\x001b·SÍáSâ\x0011
â\x00117û¡,ÿ8
I|\x000cKìv$väÞ\x0003õoð@Ø9Ð(°\x0015|J;A;T\x0018OæãÃà9|J=A=rï*ûÉ~¢\x001ee-gz$z$^5\x0014¬\x0001 ¼$[/®y.IiG2hG>úº¤ö¬'·5ë)íH\x0006í¨\x0012xõzÊ>tó-qKÒuB\x0006éÈcåäÁ
¡?Ô;\x0007OIG2H\x0003¡öÁÑI¥d\x001cç%ÌáSÒLÒ!5±4ÈOÂ^É
;Øæà)åH\x0006åÈâø¡Ô5µOc\x001döXOáËJ:ò¼t¤mìÀöyç=(íô\x0014ÂÖ¡bw\x000el*Ç\x000fSàæ\x0005*uá¤sZ+ÌJ9ò¼r$ÏAo Êg±\x001eÞ¡:%¿/+áÈ\x0006á¨´ês³^vT³¡
|Â5xJ9ò¼r$\x0006®æ¢ôZï#iíA0+åÈ&åà¶t,Ø_\x0014\x001cO!÷´D{	</\x001díFìó"Ré5ã\x0003¹\x001bn[té¼tD'^sóõ¸\x0019ÌÇÔL;ð)éÈóÒAû\x000evn1ôÛ\x0001\x0012udX\x000bÊ³Ò<¯\x001dÑÉç´FMü>é¦Ø\x001a\x0016ð\x0015¥\x001dÅ \x001dE\x001c¿H#¤ùú\x0006	;2®\x00152\x0015¥\x001de^;bOù5\x0017ù8UîGõKâQ\x0014;yv&||?ë\x000f\x001eNÎ\x001fM\Â§è¯ÌÓ_\x0004~\x0010ÜîÔCxñL3,~_Å/ÅÀ/ð*¿>²áKýü­}_uáþÂ\x0003Ã+Ðs~ÇÅ6xÃº¾)xU]j¸\x001eA¢òX=O­¡z\x0003\x0017×ª] û¸~3ÿlÄÓ
kÞxq9ÊÆ\x0001ïëâ³G>÷ñÓ\x000cýf>=.#\x0011HVúóB\x0014ÌÐ-?é¨>µf\x00065Å\x0013DB,2\9"põ\x0011×\x0012m©<Ù¾\x0001f\x000bê8O+\x0010¥@û\x0008êòâSú\x0000\x0013M0QÖÀ´ÎõàÎË0m.^ËÌ\x000cÖD5Ãy[Ù\x001eÿP¥0nìp6\x0005f3!Ë!z`ÔÜ1^<ÖÜÙ5¹ÉÃGÏ¦Nkv¯\x0002«¬fi!\x001fç
SZ«BÉÃ7Ï¦oNs\x001dB\x000f­xCQ\x000c!÷Ðj­\x001a \x000c´Y,´Ù\\üjì¥\x0014ÞC/é\x0019\x0006ÉLz@OÙNå\x00025GèÂ\x000fJ÷øAq8ÑJI
\x0004âé\x0011E^¸óZ×M\x001e\x0004=\x0004\x001dk¿?9]dtâ°­dò­l°f6Ár2CðG¹[ÄÅîîm\x0012äx[ÈÖ¶Ñ\x001fö¤®Øòc¾\x001duÕ\x001bN¿\x0011ËßÿüÛÛ÷ß¿xýö§w¿~\x0014^D¤(©q$÷qBI\²ì²¿ì³üüëï^¾ùüÅë_=~ûip\x0006	ó [p\x001dö\x0008Ê1îËP2®4ßkx\x001d5\x000cga\x001ad Ê;FÚj(²¶¯\x0019røÐ\x0006xÆ¯]hÕþµEÁÛ×æ\x000c\x0003'AÆ3È8oHê+ÙË¬ÉÍ@þÚ(»2R¹\Ó8	2A&Ã×îQO3+ú·Ï»%Ô\x0001d>Ìó )Ø\x000b^\x0011\x001cï7mþ:%Çñ
\x0006å\x000c²\x0018>wá$Z³¤ã^@úÜ \x0017çrHØ\x001cÈcÛÙFÎÒKÏ\x001d]o/¦äqß÷\o¯xÒÏ\x0013%¡\x000c|uÐu\x0012E\x0003Ù]\x000e\x0019\x0004©8ÈÏP(Næ`÷Ô\x0006RÖ´]
\{\x001eDçjR¢H¿øÝ1/ìÇ&Ù/|ûþ?\x000ca¤Jx.dOMÿx¨vi2ÄòsýÐÇW/^¾zùæËÏ>
\x0011Î\x0010a\x0012"Ö\x001a
Ï\x000cK©] ]\x0012\x000bzîðmí\x0007æø<\x001fa8#\x000cóF¤:«}@>õpïS2K²\x0014!×\x000fÍñ|>D<CÄy#Rt`#VN]\x0015}9\x001dX\x0018Ï\x0010ã¼\x0015=»4O%í\x0010e?_3âåf)é0Í\x001b\x001eAØÕ±\x0012\x0016\x000c\ù×8äX¦!æ3Ä<oÄ\x001c¸±§\x0019Q¶\x001cXP¶Ï»\x000fP>ÄrXæ­Ø¾óÞ²uØî\x0015N¥IM\x0011+\x000e\x0015bÓ\x0010ë\x0019b·bõ\¦³/IûNì5+~hú³!vÞÛ\x0019ÌXÉØÍä¡mfQHgÕ^KË¼¶x\x000f|\x0014i[é\x000e0ïF\x001c\x000c§!*iñ\x0006mi×\x0005Å_Õ\x000bí\x0011#.g¥-~^\¼GYeÌ4+)°§ÓÌXÍ¨ÄÅ\x001bÔ%Ë\x0008»m[º\x0010c*IÌø¡Ý!ÏÇ¨ÔÅÏËD\x000eØnÇÂ-g¥\x0017fô\x001fÚÎñ|J_¼A`Ú\x0019\x000cÌ;Îñ¾½²\x0015³\x001dãò·V\x0002ãç\x0015Æ£ç\x0002ß½
íx[g³ã0Ñd\x001a£R\x0018?+1|N^
hoaa;VÁóí<\x001f£\x0018?¯1>F®vÛKâù^Ë¦ØfÇ¡"e\x0016#(Y!;JÊ,Ñ^Ê½Ï«D×£ü¡©ÖÏÇ¨T\x0006\x000c*£¸\x0013\bF\x0018³T.@\x0019+g¦1ê\x0008fVf"1ì\x0003Cl¸¯\x0014)òºÝ¬XWo5(\x0001ÊÈõ3©i\x001eÏ/¶\x001dÑ-F¥20«2þ	\ÃÕÌy"\x0004aÇò¡ùÛÏÇ¨T\x0006\x000c*ò\x0003±Y{\x0019WIUbÕ-k¶\x0008Q\x000cÌ\x000cü©G«ÍÍ\x0018¸Ì¸|\x001cÈEd\x0002W;¦B\x0004."SEdÒr0\x0008JdÀ 2\x0015øÅ½Z;]ZïúA\x000c\x0018D\x0006d\x001bT³cà)Íäô\x0019'(	ó\x001aC;\x0010ý	¢\x0016&8ñ\x001dÇùÓ\x0018Æ\x0004ÆP\x001f'[Ñ\x000c¦\x0000Bi9	JbÂ¼ÄPP±q/@k\x0018{ç\x00063ê4AdÚUö|cjá\x001aá|îv\åï 4&ÌkÈÍ§ÍEò¡	;D·¬1AiL0$ÊªÈ?×Èk(\x001añ Dér÷û\x0014F%2a^dZ\x0010 \x0004N\x0019ÀÁÿ)²ÊAiL0¤Ê
rÉuÓjGã>6\x001d\x0001`Íå\x0019ªg¦1*	ó\x001aã©å¤\x001c9ÝsL9÷\x0014Êê¥FÅßhàï´Íü\x0004²\x000cÖî9~péÈó1*þFÃ+G¬Ç©)Ê§NËq5*\x0002G\x0003gß	<\x0014¹ÕÙa«/\x0001OaÔ\x0008\x0006vlQ\x000f=ö\x0012%HºìØ\x001f\x0015ó yª\x000ch×z{Ù1\x0016±#^VPLaT×\x001a
×:\x0017þhùVåoíå8^®A\x0018Õ­[-]ú\x0003Î\x001eO]bã¨.L4\è\x001e\x0004aáÁÄD"1có4Du_¢á¾ÐðiÆè\x0003\x000fÞodÓ½<tNcT÷%\x001aîO"1Û.=Ð?õõªô)ê¾DK¨Uù%¡\x0000pEBórP>uùÐ¿OBD\x0008åOçwtú\x0005½£ö·wÿá'\x0002ùÍÛ\x001f~úv¤¼ÿáÝGÓ·¥æ¾bÍÓ®Í¿Í<\x000fØqªÞgx|ýåW\x0004õ_~õ-­Jyóåã§áÂ\x0019.\x0018á6åæRì\x0016&¦\x001dlè\x0006âp¬`ñ\x000c\x0016`Ë1\x0017¡nË[7¸§MÃt+Üx\x001bMp«\x000bY
È\x0003Ýª
mbü\x0008CjÀ
6Á&#Ø.\x0000ÒüÉã`Û|×QÈg¸Ù\x0008\x00173¾íÊRÒÆö2<0á\x0001Ù
·á\x0016#\ï¤5\x000cÓ´Ç\x0019\x0019ª\x00068È½\x0015n=Ã­F¸\x0011¥C£ý\x001fEHu1ô\x0011\x001fC¿\x0011n\x0002ß9×Ùo\x001aì\x001e"è«Fão«8×ÛH·Áí\x0017*Ð¶Æ\x001d®,ï&\x0007ö&¼Aá
F¼\x0019zß9¤·ù0\"\x000fC\x0015¯	oÓºÕb\x0015\x001e¸«¬\x001d_×É!ÜD½^é·
E\x0015\x0011FÜy6¸E¦§0¼°Yá*¥ðV©H¹IH|\x0016bí<waU¼ë­Ä[LIEzD`&+AzÖÝðâoÅ«×\x001b2áQº¹\x00027Áft}B¹Ë#\x0003Å¼`dÞö÷h|Û~v\x001d7\x0015çPûL0ª²âUÞ9ØÜó7ÊÐáèd\Þ¬sû\x0010ÔZñj÷Ü(\x0015\x0014=îÂFu÷{mRÆÐG\x0006P\q\x000f\¥\x0014`T
ïr7/D\x001eúÛÌ+SWó¸RÁW)\x0005\x0018¦û\x0015¦Þ}é7KOüâ°ÂUB\x0001F¡h¿à26c'\x001dûFmò=xRQ)\x001cÈ\x0003láû¾.ËþTç(+Z¥\x0015`ÔíÝ§ôù
­\x000b%È\x0004¡ÊÎ7(î
VîMEæÙ$ÚÐµû
H\x0015\x0010\x001bÞâ:_+^ÅeÁÊeI\x001e2bÊßÕ\x0008/_¶ÃK´	oì\x00188|§\x001bbª+òL\x000f\x0017ó-®x¦#ùç·ß¿ýå×÷\x001fqÔOíâ¬ÓolNO |²t®(g\x00191üP£n6ôþ2ú/6[\x0017'£ Rá¢tíT/R1Ý\x0007æ£_lûÿóÝOüíÅ\x0017ÿüÇOÿüÇû·?¾xõîÏ?¾{ÿñRÍBÎ,A3R\x001f1Nk7@~ùÇÇ¯(+ùÝ/\x001e¿z|óòÕW½z|óáädG\x001dÎ¨Ã
êÄÔ\x0016\x0016W~«Kâ_º<Î^°cÆ3f\À\x000cÔ@Î[ÖG¿×°´¸HF\x0013¹­vØù\x000c;¯À\x0006Çyö×ýR\x0000>Ü\x0010ØÙQ{}¬WÎ5PëÍÚÉs¢vOFMý8·Á\x0006\x0005\x001bV\x000evó\x001c/ÜÙ[¨·ëXú}\x001cKt\x0016p«ûèW.$ T¥7\x001f\x001de©Ãq\x0001\x001dtR Ó
hWe§%U9f¾^\x000eè¡ù6ØêBú¥\x001bc_Êä·\x0006
v\x0015ß¥;q\x0017»,]IijæF®fow²ï\x000bãl63î\x001aØpo\x000bEí¸,ÎÎ\x0005ØçK!H&Ùqr\x001d·¢@X¢À}¥lóU÷4WÂ>£Èqg«\x001d·â@Xá@\x00082\x0019\x001e·µ®|-±oÚ¾Ø£nÇ­8\x0010V80Ð0b>ßíî±W»²uCÆv\x0001¶rK`É/A)\x0015Ü`ï£¬\x0012¦\x0016Øã\x001b;î¨pÇ\x0015sG'4H^öRú½¸~\x001c\x000fgÇ­h\x0010h0Iz´Ù»ýO`7{z¼\x001b= X0,±`»ÙBJfAm\x001aqÝGA`X!Á\x0006g#£q¨\x0010ß©h9ï}·2(\x0012\x000cK$¸\x000foÞÍ\x001d8loæÆnïq\x0010§\x001d·\x000eÌVH\x0010\x000cb@ªô\x000clïÈ\x0015³ÍÞx\x001f\x0004Åa\x0005'«î¸)MÂä-Û\\x001b·ÍØa+\x0012\x000c+$>ÉZ{Ú{¾×'§PU]¬à²ãV®wXq½\x0003dî@Úã$æÚÎäm¸ï\x001dV|o\x0004?TV¿_ÊCßô=\x000e0³£V\x0013V$ÊKÄ£B©bOdÕ\x001b»\x0001\x0016pW»®X; \x0015\x001bîæ\x000eTÛ³Ù[¢aWË8î×\x001bVâV\x0006äÎv)+tRïEçÀ\x001b\x0013T¨´\x0012W´VÂï¶6\x0014e\x0015,½»O(Q	%®\x0008eÀÄ9W¤ºý½
°\x0019»v\x001f¾\x0016p+¡Ä%¡GTé»û¼\x0010÷XR»\x0000['1t¦ù?å¹µ\x001bÐ\x0005ç>¡D%¸$4fq{+ºWÇÁÜvÔJ&qI&Sì\x0004ä\x0015$E
£Dpîó¦PÉ$.ÉdN²w=»ÌâÍÚý4\x0016p+¡Ä%¡ÌßþqÝ´§Ö¢OØ\x0005çF{+¡Ä%¡,È3§:óLd(«c¬\x001dwTB\x0019²úNÞMt\x0005>à1kõ>ØJ(ãPVà\x000b¤¹\x001c{µ[jb)Ç$[Xì¸æÄ\x0015ÍNj/\x001a\x001d°{Ý4¾Jp£mí¸\x0015yÇ\x0015òN@G^\x0004R>@\x000f}þ\x000b \x0015\x0007Æ\x0015\x000e´°a\x0004Â©p\x0013«\x0017ûKí°\x0015Ä\x0015*¡µ){\x0011=¦9ÄÉôo`Ø÷¹®IÝÈ´r#ãÛÙQ\x0007\x001e´²çx²Á\x001eWêÙq«\x001bn$&îòk¸äº3tsã\x000cÔLK7Vk3î¸©Vpë=í¸Õ¥LK2õ¡°)#ÚÝp#Ê9¹Ñ\x000fLêR¦¥K"×;4\x001b?\x0000[\x001b¸w\x000edu+óÒ­l&örJ\x001cÏ¥O9v70ÔûneV·2/ÝJw»Ã¦Ý°\x000c;	sû;«+®dcë,¨eõZ»I\x000eI¸\x0013·®/Yº\x0015\x001f\x001c2nà\x0001b)Ë\x0000±{\)fÇ­îd^ºUÖh6ÜN^\x0016ruýp»û(°¨KYV.e\x0002/sÐ[dÃ%Ô3+þ\x0014Ûì¸UlVVb³Ø\x000e5²c\x0012A\x0012T\x0019Sî¸ï;'UÅ8u%ÆÙw§\x001bK¿}îüïOU¥ÕêJZ-\x0016ßÙ\x0004£d\x001eò\x0011*ø\x001b#áªòSu%?Ek×
³	Ê\x00008  §ÄËwí¸\x0015{×\x0015ö&ê\x0013{(\x000eUIâOÑæÁÛ`«\x0004U]IPm¢\x0003ln¢ÆeÈ>\x001fß[N]\x0011\x0016ÐP!Ï{_Ð¨Ò\x0007]êg[1`]aÀä¼\x0014ô¤%kWJ74#,àVJYW2ÓýNF\x001a«»§\x001dªT¾ºñ¶ÃíF»\x0015©ÌÔZ\x0003\x000c\x001c¥\x001a³ö÷§ïJït\x0015©[aïtÚ%¨Ü"F\x001a/.ìÐU±[Wº\x0015Ç»ñøDä|ÂkükãÃÛèÄëÒnúqÅàµ|pÜË
Ô
~#ð¨¯èNnñdÚ½ªX4\x000cm³NØâCûØ\x0002p]»ëV\x00180	KªÈôÏfðqÑ´\x001d·.ÞuKÊC3ÚSJäªÌì<Û5ßIºz×-©\x000fÖ®>\x001cÉ\x0018äbÞ\x0018\x0014{W5ê%í©ò\x0014\x001f\x000bp\x0006";H Ö¾¯lÍ{\x00154Ð\x000bÖY^t\x0012Õø0¡Èfðû®åÓ¶%ÉlQ1Û;\x0017®MÏ.ð4«æÅÞõöOú.\x001a/(eR81è{A\x0012ù\x000c¼\x000c]Ê\x000bÀµd.u^\x0014jWölñÈã\x001cÍ|dÇÛ|Yïµbú%ÅLu_\x0000Úìí©dp·ww­JºÑÞZ0ý`\x0016ÚcQÙÞÐ\x00053vÁ\x001cF0.àÖz¹ÔìöRúÍàíÈ8fpQ\x001d&q\x001bl-KÍ.4(Mä2;r\x000e7sËÜfî\x001buþI³ËR·KqÝ#¤s²Oyoç¤\x0013Ê8l\x0001¸VL¿¢\x0006´î¸Sä]á.\x0006Wð¾·m¯»tüRN¡
\x001födQö°g\x000fA\x000c\x001eî«9ñºMÇ/õékacÊ\)qÀ\x0006¿Q2áI«âdæX¥\x0014,Rý	õ!Å·º1æÑ}:~©Q§Dì\x0019\x0005xöGÌ\x0013nytÇ_jyi>¸¤îc½:¹ñX<ÜiqÍâ°Äâ-èñlqÌÜDi}¶\x0000¿ï­Äë^\x001d¿Ô¬Shª(³!m,\x0017\x0016/"?áFÜÄaÄk`-Òc>)QR\x0005nt\x000bu»_ê×©\x000exñ\x001f­\x001då1®Ù§('eÓ¶\x0000\³áRÃNifD
M;çR:Ó(¿Û?éÜ^aÃêAJP"ÕÛïÀ=­DÚûaÐô\x0002p\x001dA,µìnrûv$\x0005D7ånúûÞL¼îÙñKM;\x0015Pbd(\x000flïÚ_\x001fÆ½Ä\x000b°u\x0004±Ô³SRè~
:º¥»úÈ\x0003l\x0001¼Ï\x0015×=;~©i§¢â°H¦ß\x0012à\x000fß¨>ºmÇ/õí\x0014
è\x00198íLdG%ønñûÊ¿½îÛñK;µO¯l\x0016wTR½Y\ÊÖËCC¼îÛñK;Íâ=Ú\x000c^³^ªÃÊÞ^7îø¥Îm*_Íæ±ìA2È*Úfï\x001b³³ºwÇ/5ïTzÑs\x0012y¡ESûî¦øûzÏ½îñKm0UR@´l¯eÚ
\x0017Pk\x0006_j'©èe\x000fÖ­ýh'Bà,P.÷õJyÝNâWúIè1§ó«4|\x0003^Åâ\x0017KµíÀ£¶x\²85ð°;ëd1o»<ËâÎQU^\x0017û*ðê¨¢ï¥lá:ª{Ë£\x0015¨@ä\x000c;-\ËêÈ/áó\x001d¹ø'ÐÉÉY]MíWÊ©k\x000bá%9T!QxFª;.æ}\x0006ºÚ¯ÔS×æQR%Þ\x000e\x001ceU\x0004\x001dnñû\+]PíW*ªkã#^[4¤X¦Ò¦ÔÊÏ°Y»(yÁEÙÆðwà2;\x0015ò.-:*÷Q®©ö+EÕµýÏîwÓÓ }6¢\x0004ö¹Ü\x0018\x001fë²j¿RW]Û?BzÔõ¹>9GWÂÇu­\x000bÀõ\x0011_)Pn.Jê{l~í.ö-âd§0çûªÅ¼®Oö+\x0005Êµé\x000bo9k¸Ó\x000cÜí\o\x000cë>àeåÏäDZC¼ð\x0018ANx¾ÑI)Z5Ëjz\x000fRuEÀ\x000c
îná¸f|\x0001¸¾eåj\x0002-Z
\x000c\êórL!wà7Z\»eÁ-l\x0016oq&và2\x0004\x001b¤ºº\x0001¿ï\x0005¢h½/+z\x000f`õ)A2\x0012±r\x0001>¬°Z\x0000þdöàB*¥z\x0000ºE\x0016w2>ÿ\x000eàÅË
Óx¶$gÜ?\x0014¶¸lÖhÀotTtÛ_é{¨´«~Td
Ä\x0011úÜ75ÑW-?uI~bX\x0013ùÿ±Önð\x001b)ºcÃ¯´lPgÃ\x0001\x001cxw;\x001d\x000eÿ;N\x0016Îº$4ÍyÏ§Ð\x0006}^NcÀîßYf­{MüJ³I³x¢1²¸\x0017ç®ø÷yº×Ä¯4Thn\x0015ÏòÃiaÀfðpà¾1!®»6üJÛF\x0016ÕsU$f\x0019©ºß7;ÑëÆ
¿Ò¹±íèp¡s
È\x0010þÚesØîµ\x0000\«ÏJëF¥±xA®fß¢²ë\x0006\x001fKSêC?®EÜ-¹×µcÅ®÷·9X [N`¥å¤\x0006Ì2ò\x000c÷\x001dU;{©ûÍé¾\x0002ºå\x0004VZNZ\x001c\x001e"\x001e²\x001fñè{Øîî\x000cºç\x0004VzN¨\x0007÷§7÷\x0015$í`úÄûÞ¿A÷ÀJÏIïc?*9	ð\x0008±\x001facù\x0002p=¸w¥ç¤¢\x000bRãÔö¸\x001b¼x9)±ÜxÄÆ½\x0012µµsÖ3A\x0019y^|²bøf2Ì\x001aølÒPÏdúêÎ\»ÞÇûÒË {N`¥ç¤Â±\x000e,Î\x000eV%dñÛ ÛN`¥í¤b\x0000Ë±ò\x0011/½T"»Rí¸uÛ	¬´l9,y!LWTS\x000e«\x001fqwßIñOfÝ¯è&fÙýÛGòÊ7'é\x001cÌé¾dÐý\x001b°Ò¿Q£\x0007iX§¼©úÔOÊ}død)ÂJ¹u\x000bÚTÿ£ÂÑfr1tßwÄn\x0017XqTàMH'e\x001f¦ÓÜª	õ>\x00162§eP\x000b~ú\x0000\x000c¤n%}z|ck\x0015MXÍàc×z\x000eØrwgÇ-Ì\x000b µò¬\x0014þÖ\x0000}t\x0011&×s\x0012ýÑ'Þ÷®	º\x000c\x0015VÊP·øÁA§,áCWúûvÃ.æbÎ\x001aë]ùpÇ(\x0015\x00079`?Ýþ¾Ó­«"a¥*²â¥*shßì\x001c;ð\x001bO>á+ÅÍ\x000b/Ò@ÔÚËf\x001e¼oN?è\x0012=X)Ñ«HievÂ\x0001Ê[¡Ø;øç{(í\x001fþî\x0010µ¾+n
u\x001f\x0016Õ<Ù\x0003µôOg¼ÓÜOÃ¬ÜKN&I´ÿH6¼Ó Þ7í\x0019t¥\x001b¬Tº5wÐw:A6¤)£»\x0007õ\x0000bX@\·WµÐíÍÏ=%×Ô-~[\x0015õ	+'ê|å¾°¾Êv/wã«	¹j
÷Ác»\4xi?àµw¬7	ºÏ\x001dL\x0008Ó
\x0011R
¾<÷\x0004äÁ÷¹FiÔÜ´ó6àú¤¤¥ÒÔ\x0006\x0005ø4Ü'ß-~ß¦\x0001ÐÕ°T]¸MádR	^jÆjéÉð\x001b7eAÒlVØ0¦Ú}\x0006Ù°Î3ùIàúr¦¥Ë«ô&V¾µ¿÷\x001bÓ\x0011ºJ\x000fªôK½ ³y)ûpÈâB\x000fëÃÂõåÌ+3^ª\x001a£§²\x0003¯(G\x0005n|(\x001axY\x0002cçq_Ø\x000f?¹pßÈ+ÐÅW°T|h¥$;X~\x001bå±áþPåï[
º	jRÍ=qåã\x001ei\x00162Ç(ûrßÕ,OÖï­pJ\x0003ÖÉ~í¸û`Ëìï+½\x0002]O\x0003Kõ4999à^4wà\x0000òl¨ÿäÀG\x0017¥ÀRQJIO\x0002mMØ@>7Æ\x0005Ügm}ºW\x0006[þkqëÓ½TiÐøD\x0006[6Úæ9¢´¥û\x001e×\x001cÖ?ýÇ\x000f¿Á7 ßûe°¾³:ÁyÙCìóÙS¾±96>O}½KøkóR¸"56Àû<ÔFá²E«ÀÓj\x0006ø¾¬ÁÿWÎPqÉ?Åßw	~l¡>Ê6\x0005èCÁõéþ7Ö \x0014x
\x001c\x0015üfbev¾|åêÚöOîÚ\x00047n±ù)þ\x0017Íß\x001cF½\\x001dç.h»Lß\x001drç*6ÿ§_ß½WÜãG¿±sOFIg
¨wôÇJzß(c¢'èzàWZò8LÊ\x0002Z]Ì\x0003§îË »\x0014»\x001b\x0016\x000fOt2\x000f®\x0005}<ï0\x0007×W\ÜWÚçp8ú¸xô©ªÓv¹~N\x0016p¾ðìÆNý:À§ªÊ%æ	ÎÓ\x000b)¬t\ç\x0017ûãbºÏßq~Ä¿h~ ¹Á¼G¬$~N!÷íÔxã\x000eó\x0000úù\x000c¾Eo?Û¡\x0007}ñp\x0004!M$ë×ýïGÙ
Ý¢fÑv\x0000\x000e\x0003¡ð¤¡â²¬Ëpã²Ó<8yÑá$ª\x0014Íj®s\x00155}qT¸ÏÏG\x001c¬¸f}*½(ü¼I\x001aãKrý\x0015ï¾$°ÃÁ_ÆEw$W¶ûôP=kî±oñÆg\x001a?\x001e~¿xø¡i.J}L1¥jº^\x0004w¾Ö\x000cøã¢Ã\x0019½p%m#Â^|$M¹©Ü¸Q\x0000ã\x0003Ç'@ ©ÝOBÙÅ/ïÞÁÒ\x0000>-ñX\x0013',ÇÓHâ}¥\x001ant\x0019\x0016=Ò¢Â\x0007dâl~åÝ\x0008ç\x0001ÕñÆ2ª4\x001cö±×<\x001eß\x0017ÅPat6¤^ÿ\x0010ïË4¸8¸ËqÕ]nn\x0003¯ M5q\x0007iJ¹ï\x0002¹³O\x0000FáEáz<»¶«ËÂâQïsã^¤8\Þ¸zy=\x001cTeö\;<Ø\x0017îÞæíÃ&¡j®µ4\x000f\x001eYªÜ,ºÞâXâ­{w\x0007ã/ÂßF¤p îú²\x0016mõõ»÷ÕÌú4¸4xdéìS74Q×>BüÔ
vãTQÀ:q:©¡J*\x000fhÇ\x0016rJ\x0010ê\x000c÷UÐº8Ø?®ºüa[ü¹g	ã\x0003¯¬êJ5Â}Ö/#sEæL´¦EÞ\x000b÷\x0004aè=ÕþÆ=ßið\x0019Òj°¡å«¼wk+¥egb¶ëÇ^°üàñ«\x0019º§Ed$w[A\x0014Æ/3C$?\x0006¾\x0005üc^1=Ò\x0008\x0007÷\x0013ß|f~cN4«=å	º¿¡9°ÿîøÅïüï~÷fÇûíßþëï\x001fHuXûÀ±ö\x0007ÚÚèU<ôúH(CòõÍïÛ?üûë\x000f\x001eå\x000bÎ¸`\x0006\x0017Èbéö'3Mø%`P$§
CÝ\x0014®pÆ\x0015fpÀîkûÀ[Ñ\x0001ª<u4yúM§á\x0019\x0018Î\x0000ó2\x0007¹ýÉÄã·\x001e\x0000\x001bâ§Å3°8\x0005,±ÇÙþ¤c¹\x0001«ýK\x000e%9SÀÒ\x0019X\x0000VªTlGlÏ\x001d\x0003\x0004q\x0007 \x000c\x0014SÀò\x0019X±\x000bÜâ\x0013hÀè^¨\x0007\x0010û\x001c2S¸Ê\x0019W1X®rl²î\x0015\x001c\x0000Ð¹béFÖ3ª:ù\x0019\x0011úùÊ(1÷óµb®Þå·S«A"×24Ç\x000c8Ó\x0000àäe\x000bêÒÉ÷êJú;YúÙÅ*ßIH\x0007­WGßÏýBÅîI\x0004^6-À¸\x000ej
:e~ê\x0005·¯ßÈb/0\x0000ú\x001cÊ;fpÒo\x0011pÚ\x0010\x000f\x0016Û`Àã	Å¼\x000bQy\x0016ô\x000bò,>ûÛ»¿ÿðÓïß½øìç¿ÿÇ»\x0017¯øë?ÿß÷ï>\x00062£
»M(JÙûÑ;þ¬Ö«=}`ÿì\x000f¯¿üêÅç/>ûúõï\x001f_¼þòÇ7Æ\x000bg¼`Æ+Þ\x0007
éÝWÃlxñæüÔc¶â
g¼Á\x0012\x000b»}iÀf\x001doÜwÐ{Zßù\x0003­xã\x0019o´â²±áå\x000bÂ»\x0017ÿ\x0013ÞaM\x0015o:ãMV¼´]Ïïx+
^ï3ß\x001cÒ]öÍg¼Ù×çM;íh½«¯áÅ$÷Í
S×¬xË\x0019o±â¥%\x001e|\x001eßß£\x001a^\x000e\x001aÞ2l\x001b³â­g¼Õ7å\x0007>\x000eÎïÃbÐ7Ö\x0010zá¦ã{Ì\x0018Øè×YñVÇ¾}a_Ò\x0000C\x0015~\x0018]J+`­\x0017VÁF\x0010{]D;À \x0017.8Ìrï:\x0010^	·*\x0006ÄÜë?)NØ7\x000bg\x0014\x000bÛ\x0000+ÅðVÉZÝ¾ýy³pÚ$\x000fÎ©\x00150*Àh\x0005ÜÜÁÌgØ9Ê£oCÉýÒÝuÆy«ÈìÅ 3\÷KG\x000b.ä\x000c\x000f­Èy£Êy
RöHÊÈ\x0013ÑÕØÂ¸õÝ\x0002X©·Ê\ð{éídwÊÛÈû2êfa\x001crVÀJæ¼UçZ¬ÌÓ
`Zv(À:cy¦\x001f|É\x0014´Jä¼Uå«¤mûËýÆåîUÞD\x0010 D\x000eÌ"·\x0001Ø\x001bü>Ì¿9\x0011e/)jÆÍîiÂ
X\x001cXE.¸Àïi*\x0003\x001c·Ä*\x000fó7­uTd\x000e\x000c\x000cFiû\x0018Èfá®ÊMíy$>z|A)\x001cØ\x0015\x000e\x001f8&¢\x0001¾»qcf\x001f-Ã0\Ûj\¥o`Õ7W
1§Ú\x0017ã\x0006&3\x001as\x0013`¥o`Õ7ò *Ð]æA\x0004¹oCc\x0015°Ò70GqAòqÍ\x001eÕÂ|Ý0\x0014Ç
Xé\x001bXõ
b Øm³0µxö\x001crÛ\x0019V\x0001VÅhy¢}\x0003ö.(ò½\x001c1¯h\x0004\x001c\x0014\x0005\x0007+\x0005{\x001a¶Æx¹ë¶Ý¹Zª\x001cá!ÝhÅ«ó<VNóÍÀèiþå¾M\x0002ûêû»É§\x000c$=Ó\x0013$ó×ônOO¶;X8Õ2AÝ¹`½s®9=E9nÛ\x00026ÀNàìÇr#`TG\x0018G¸\x001dV¸¨§ÑBìµÐáÐbfµó\x000393\x001býÆ\x001cÏ!ûÂÈ­\x000f\x0014ÏÇb\x001c³{9ÀvvØ¾z®¿lnÛçí6\x000bN¼L¸â \x000c¸Ã¹©ðOÎux`_7þÑ±\x001eZÜÌÄñ\x001467wO÷áqnÛ¶Ã-=Îo2'\x0006Ïa{r~a3¶sÜ\x0017C­\x0000\x000fa·6 ô÷¡9c\x00126äTX$×+,Þ½øæ×÷où{ÿ×>\x001fÑø\x0017\x001e¥\x001f!\x0014Tnyè­D\x0005sº|p{|ñÍ·o^~óû¯¿{óÅ§A3È0\x000f2:\x0016\x0008
ïfÎ\x0010«ìâðÒeÑÅ\x001cH<Äy(+\x0007%\x0003WG6ÜIw%ã\x0019d\x0007Ù\à½Ï»Y\x0012x\x001bX¬ÒôÔ\x000cyù?11&\x0003Æ°\x0017ÚÑÎ,^Ù F9Tk³11æyÍ\x000fÛkG6;&þØ1vC\x000e-·\x0006å\x000c²ÌôÀ9éH«>öRûXC\x0015yx¦\x0007yª )[n\x001ae©£²vo\x001c7²EÚ¢&(V*\x0003J¯Púy!¶8lïÒ¥z9qèV3@TLîç©Fg\x0008ÊF@lÈR\x0012t\x0002ºás+*÷ó\^´Ew\x0007Béäs§aî\x0001¥âr?OærÝ;Ä$]­8n	3@TLîç©¼P×*tCî=|
eêÊ}\x0003OzÅå~Ì\x000bù;p\x001cÊ(KÄÃ¿¸¬ÎC©ØÜÏÓ9¡¬â`d®¸k(cç Á;6 Ttîçù¼\x0004\x0019Ðld*¿Çq
\x0001eU(«\x0001eä<æfËÊ¶Dìª3ìíG	JuÀ :}ÎôfK6eØ_ð	äuµì\x001cH%:`\x0010\x001dHÇ\x0015ç2\x000eBy\\x001e¿®; #\x0008îøm#ÔnÊÄ£jcÃñ\x001dZÊ\x000c(\x0015£Ã<£ç^í»£ÜeûmWÇõ»\x0003ÓaÓ3mÏÆî\x000b9\x0001¹×íl\x001eÛ:HEé0Oé9ËÅ\x00062Óñ\x00062C¿àÃâ\x001e\x0003JEé0OéM\x001f¹d3å>+fé\x0014$SÞ`KEé0Oé¹\x0005\x000f]ô\\x001eØ2\x0005Ácqëº\x0003ÑaÑ-¹çu3å>*£}ð\x001e3çQ\x0006ÅèaÑ3JgëfÊÌ(ÑùnËõc\x0019\x0014¥yJÏÙs\x000f_CéyçoÌ)u²\× \x0018=Ì3z\x000eå ¡Ê»Qb\x001eÝ\x001bÜ¡ BóD¦e\x001cÐM)\x001f<ö¬P¾nÅC©t'\x0018tÇ»ÎÅI(Ó\x0011;ü\x0006JxAx\x0010yøfË½\x000f,n\x0013¡ï;JxÂ¼ðP×(ïÒhs7drâ²p\x0003F%;Á ;>P(Ö³Èû$â
WGÉNDZÃâ¸¯lkï\÷*\x0012`\x0010\x001d\x0017¸Ö¤\x00192rßgL\x0005 |\x001d%*:Çy:§!\x0004;J\x000e\x001cSvG\x001c±~»Qñ9Îóy
\x0007S\x0016ÜKKBµ3e\x0019Ú\x0003\x000c(\x0015ã<§\x0012zf:\x00183ËÒ=¶¼îf ÎòÏóyò©kcé(ìÈ\x0005/7$PQ%\x001a¨V&²ð\x0017O3tC.\x0010\x0015
á<
EzK\x0015YRý\x0011cGyÃíÊ±óe¤¥Þµ£d\x0001»î\x000cUC\x0006êÇù+N;\x0012ÄUd'ú\x001aú@Ú\x001cHuwâüÝiV{¨¡£\x001d%r¹Íò\x0006\x0017ýül.¾%ýfVb:2D\IñD>Þ%Ö¯PtOÁFg\x0001\x001b÷½¨òh¶ï\x0011°ÿ¡aíù`\x001b\x001b;Õ\x000bH¿)\x0003¯©óío/þíÝû÷¿ýúîÇã¤n$Y~åÇþÑüãc¾÷Õ9}Ý~~|ùÝ{|óæ»o\x001f_}\x001a*¡	ªÏÇ\x0006&ñähâh\x001f
|éoÎC
g¨ÁfÕ(c8i%Àî+Qo½Ùªx\x0006¨©ÖÒ×.dÁÓb ¾¾\x0000\x001966¨ñ\x000c5¬\x001aLkBð\x000flÔìeæ\x000bù¸w Mg¤ÉÔLÖi¡9¯(hF­Çá{ æ3ÔlÚ,ÉSth#_ª\x0008}ëÆ°õÉ´\x0016QSßèX¸\x0007æ¸>÷J«æÖ3ÒjCZ¹k[ºV\x0004iN©®Ü¨i¨ý©çgÃZú~Ï<¦¤aí[`ÓåcÁ<V­U6±¢ö"±«Ûm	kß	\x0007Ãpi\x001bV%VÞ¨V g :¿%Z9ÙÃÅ©6¬J­¼E®h\x0007=\x000bî$ 3Ç\x001bqõå´~\x0018ãgÃªäÊ[ô*\x001f\x000bf\x000f
µb\x0016\x0015(ÃFq\x001bV¥WÞ"XÍ®sO»]\ý±\x001aè&»*rõ6v¥yXû\x0019 \x001dÏkd
õ-w\x000b\x0014g³\x0002>\x0008ÔÂ#3)îP1^6¨ÚgµÑ@ûî<\x001dæÜîyæ\x00130V¸¬Çª®\x0016Ø®VC$Ó0é\x001f²\x0001-\x001dèå y Ê»\x0002{\x0015û´éXrç«*;\x0012J¼G_A¹W`ó¯ZÔ*Ó\x000ed*#:Kºç6\x000fUQ\x0000Ø( \x001dPå\x001akä§°UÆ#t¼ò°Àæb¥>°;ùî·V×§._×ÓPb«`c«äûMÊ\x0002&ÚÀå@ y¬ÊÃ
6\x000fªZv¨y{ZäbËJy¨YYS|<DÓ{QJ;>\x0001C·£
«N\x0007Øò\x0001¹ç\x0003\x0012m«ÝoVõI\x0006~\x001bw\x0007V¥\x0002Á¦\x0002©oèN¾;ÕÉø¶RÕW6¬ÊÁ
¶@N²+§aKÍ*\x0019¡ê.\x001fç¡*Í
6Í¢1[lVêÐ\x0015C¿Z÷\x001cW¥YÁ¦YY
]¥ú\x0012+ÈLïö÷oª4+Ø4«Ý,\x000e\x0007Ró`û\x0011è¾`½\x001c7\x0015\x0010 M\x0008hN\x001d5dÞ}Öx-·H\x0016*\x0019@\x000cP~%+Õ~X\x000c¶®Ãö>\x001bT%\x0003h\x0001òTä¬\x0016.#Ä\x0015¬Ã	\x001bT¥\x0002hSº­WH¼èB| ³\x0014}ïÁª³Â6\x0015h' È	ð¼þ¸aEQ,¸,fÇªT\x0000m*Ð\x0000§/èÉz¯¤# §\x0015åØ6¬J\x0006Ð&\x00034­Í%UûlÔ
÷dP©\x0000ÚT Ö~³(Á\x0000ö=xù°>UÉ\x0000Úd \x001d\x0001Ù\x0002Q²\x0017§#pO@*rASäâ]_O\x000bC^\x0016Üs\x0002¢\x0012¬h\x0013,\x001a("\x000b\x0002ÜÏr\x0002\x0004Âeùó<V¥\x0003Ñ¤\x00034LÄµÄî¶Êëp;­Ãæ;\x001bVuZ£é´z<4\x0002i{Ü¬ÓÞË¾i¬Id:\x0003Þg¹Y´0×T\x0004êeAÈ<R%YÉ$Y:HöôE\x000e©»òèRË=YÁ¤\x0007M*@ã@y?oA\x001e]-ec»\x0005ªÚþ J Å\x000c³þ£ÙúWÍ\x0014\x0016.ØYë¦à)äP¬iõ.»[ÉqkuÓZyÙªþËù§½\x00151&12ú\x001eÏ¶s¤làÛæà)b°"ngA6àÄØSñ}ny\x000e÷_	"NhLwoïÂ±ëoÕ1µ.¾#·¹®xi¿?¼ûéý\x000f/¾ùõÝOßÿíí'^ÚzØo
ÁSQ+áÄ	\x0003@YCòÇ¯Þ|ùâo\x001f¿úü\x000f/\x0012Ï(Ñ²Ùp?nñ÷¶Èo9\x000bÌËúêYñ\x000c3Z'h0·v©
fäÝ\x0012
æeSû,Ìt\x000c0laM´Óq/\x0005G\x0008\&Ú`^®Ï0³\x0005¦~m0A2\x0019 \x000c¸Ý\x0000³a\x0016\x0003LÈiÝ`ú\x001eÁÐ0né.ËpfaÖ3ÌjÙ\x001c\x0017`k6\x0017K°\x0000\x000eµÁ0b\x0011)Å"S8i´6_u/Öè+¯*l8/Ó­³8½Âé-8«\x0010çîhoæt\x0007Ì;P*v÷\x0006zÇyVn	">gáww¹Å\x0019\x0014Î`ÀYe`¢ñ¾	ò2Å.ý
:ä\x0015Á{\x0003Ãc\x0001\x001e÷ËÜÝìÉ\x00057
çåKë3q¶sQªN¿ Uç]dýøö·ïß½øý»÷?½}ÿýÇÒÞ}[o\x000b£@òUÑs\x0007\x001a\?°þí³W/¿ûüñÅï\x001fß|õòÍç\x0006g°h\x00049¹Ë<ªMÁâ¶6Mg°É\x00066óJÀ5ñ®\x001aP;ÖÁ6b-g¬ÅÕñ)ðÝ¿¡8Ì\x0012°=­, ÜÎ6ñ\x000bf*TÒ\x0012\x0019mégö&ÓzuÁ¼í\x0016 M\x000fyç¬\x0018³JþÐ:òY´êyÛ\x0015+T*\x0018\x0018í6;rC½\x001dF°êyÛ\x0015+ ï
,OE¦2\x001cÎ]5´w\x001d[uÇ¼íÑ×g\x000föEíw,9.\x0014nbZPw\x000clw¬ÝønZ(R%<wã\x0000m9º\x0007­\x00161ã\x001dK²`£¡¬HA\x0002¿òÁåÃ³hÕ\x001d\x0003ã\x001d+¹³mXö54¦P\x0018!
Û5hÕ±\x0005Ó±Í´iO¼§\\x0013wS1¦èØðøf\x0003{xK\x000e·Í3ïf±;S*§\x0006¡ºg2ÂÛë\x0019ô\x000cUY4Ù\h\x0002ý\x0016iåö¡ØÕñ²ÐàÆ,¦Í°%ÑR\x0013\x0001mdQ Ù{\x000fAD\x0014­Ôg\x0003TïÔ\x0019 \x001fMX«H¡[\x0016¸\x000b\x0017øù¥Yö\x0003ugÑf6ÐÒKFàs\x001dµ@î½ì¼5¸:l±ÀõÚ÷¢-xkó\x0015\x0013\x001f$+5ÌZ\x001cÛô
óP`-F¬ÜSJ''\\x001eÇ`(Ê³\x0019¶<q\x0013\x0010Jóxjvè¸§(±{\x0010Æ¼Ë´YcÿïH·mLæ¬-h\x0004v\x000e\x001cpº ¬Ô¥ÆEïôuÚº=Ç
åÁíY×J
;[µùy\x0000ê8ðÔ\x0002ú§¿\x000cfþI"ç|v;¾é¡ð4Lì4¶&\x0010áiën8µîþÛûùßïÞ¿xýÏ¼ÿáïÿüÇGZc3©\x000clíãó$\x001bÌ¼{\x0016#^VÀþÛ¯¿ù·Ç7/^?¾ùòõã'Zw¨p
6¨±Ê|\x0013ºçÅøÑÅë0MHÃ\x0019i°!¥0\x00129ìÞL\x0006\x0019ÍQ¯[7§¡â\x0019*\x001aê©6s7ª¬æ%·¡\x0008ÔaÅ	j<C6¨\x0000\x001cÇ\x0002"`=\x0013¯ÉßbÕt·
Èû\x0001è]\x0010\x0019ýq\x0000n¹Uù\x000c5Û :dõ\x0014ÝrR&Is¯ùrÂÚ4ÔrZÌ×'M\x0014\x0008r§|ý«Ìì,L¯)ÕÆ©´go_¹\x0017)\x001cß§\x0014bêWªÜqL½bTo£ÔR
çQòeßÈ¹U¿e:ìE1aUêm¤º9/|§"ò\x0011L¾Ó½\x001cA;Uª·±jIF¦Ê	p{î0EßÀe#Ü4VÅªÞF«tVcé\x001d^dØ®pËyU´êm¼Jg@¼æ
ÈÍê´Z/«I§¡*Zõ6^%á\x000fbÖ$G t¯U\x0015­z\x001b¯nÛæY\x0002hüb\x0012¨Ý¬ÓÛ§±Vµ°æRe!\x0007µòG9µµ\x000e\x001b,X{.6;gíêÒ\x0003@B©|ÕÂæÀß\x0000U»Ö6!È5S\x001b¼`e%fÁæÁßU+ØÈµW²\x0012aÛ; '`Gz\x0007JEU`£ªÜ\x001bu¶KÅ3\x0006Zè×	 ^\x0010<\x0017«k¡¥\x0001é\x0017¿;òn/ßÿú·ß\x001aØß~üñç_?\x0011­bñM\x0015ú©äúû4LCàxõåoÿð]ÃúÝ«W_ûi¨p
&¨T¹×ÝÑf\x001eJeÖ/\x001fJ\x0013OB
g¨Á\x00045D)ÏÝvßìiâí¥{:nr°AÅ3T4A¥	n{ÉhMRâÔ¬ê9\x0007@;6o\x001aÏP£	*x©$¯¡0ýÓ9\x0000ùC\x000fFPÓ\x0019j²]+ \x0007e\x001aAæs\x0016yõ´çì\x0016¨ù\x000c5 Rï3ß*àÁX\x000e\x000eÎª
h9\x0003-ÖKÅ\x0003F*-s;Ånµ¯\x001fÊ_N"­g¤Õ4×Ê\x0019\x0000ê\x001f)ÅÎTÿgÚ\x000b3vþw¶K¨l·jáòÛv©`\x001d;lXµVÄ*×>\x0008\x0016È\x0001\x000f×¯Ä®\x001fz$ÄªÄÊÛÔÊW~)DÚÈÌ\x0000ÐÍ:,Ö¶AU
àm\x0012à"×84¨\x000bô\x001a\x0005\x001c\x00120ø6¬W½XsÝ\x0006`lXóVí°\x001f\x00019®@OÒ\x000bX\x0003¸¨Óë´õSA_ýöÓ_ßýòKó\x0003ßýúâ³üá\x0013^`þwß*!­ºäÐÊ9)r.^\x0017øÕw_}ñøÍ7Í\x000f|üöÅg_¿úòÓ`á\x000c\x0016l`Qã5°ö.\x0010Xê,\x0015°C¥\x0011l8
F°¶\x0003ì`Û)ØóÛÜ^\x0006;\x0014c\x0018Áâ\x0019,ÚÀ6ÝÁ¦\x0007d¬R].[ 
Pã\x0019j4Bõì¶¤PÌmØ¶£1ØËHÐ\x00006Á&\x001bXÍÍ®A
K)SÜ¯×=Xó\x0019k6bÝ^\wÃ&I\x0007PÍ1c½\x001caÀZÎX
«GâÔìÚëµiúX¿\÷`­g¬Õ\x00158ÑÖì\x001aäQ\x001b#ï\x0014\x0000\x001c·§ÛÀvWk×\x0003gBj:Mº^Üb\x0001\x0005ìåp$\x0003X-^Fõr uÛ¡:\x000e·\x0011Ñ\x000b\x0017ÜÄ[^·©Wâb7\x001aÌc1\x0010²Øu¬n1BUÒåmÚE\x000b&\x0012SAéÃ\x0007\x0011ª\¯|ùèj@«´ËÛÄ«91rd\x001aµø\x00148ÞI	ñzð\x0001­/oÓ¯D»0\x000eJSÝý9C8\x0000^\x000fJ3UòåmúÕDa\x001fð0\x0000oUlå^]þrX\x0001¬Ò/o\x00130\x001a!\x0002V â\x001e¦Ë©\x0013\x0006´JÁ¼MÂ\x001ayq'j_÷5´.m/G%\x0019Ð*
ó6\x0011K	y¡T³­ãv¨òT@s©n\x0001\x000bJÃÀ¨aÔÎÃ¦m18»¡ëÝ¤÷\x0000JÄÀ&bíTÊA\x0008¹7\x0017·\x0013,Bºì3 Õ!QÅhå\x0007{´±Ê%k'ù+Ë\x0005\x0015\x0006´JÈÀ(d4lMû\x0012\x0015\x000cÙç\x0015/§e\x0018°*\x0019\x0003£ÅÂiö\x0003H¥[(B_1\n"2 U2\x0006F\x0019k%ý¼¹ôSKý\x0010|j/GÑ\x0018Ð*\x001d\x0003£5\x001a`Ñm×Iâ°\x0005m\x000cñ&´JÈÀ(d¡JÔ\x0018J\x0012÷\x000cÝ}N\x001220
\x0019:\x001e\x0000¾1\x0002»¶äçvF¸é)!\x0003£"#Ec(çVJqì³¡
JÉQÉ¨P]ÛF\x000f\¤\x0011¢0X¼\'k\x0000«,X,ñãg¢É.< HÃ\x0001àué\x0001­\x0012²`\x00142Ú®"Ç6É¦ÐÇ;ÄpY®e@«F!¡\x001f\x0004È4·r·-n1ÎM¾mPR\x0016RF½þâ¡´Í\x0005¨\x0016.÷í\x0018Ð*)\x000bF)^²\x0008M\x00128_ßþ*ËIð7\x0011XPR\x0016Ræ §¾"H\x0012<xÉ$D¸)\x000cJÊUÊ°gÁ\x001bÚÌ¶Ò\x001cq\x001fZ%eÁ&eò\x001eÂ	þ	Ìu¬Ë?
X\x0005£ùH\x0014»ÇæÄïü\x0015zsÙ\x00181\x0016¡MÈ"íÎÅ\x001eqGu#~joâ/TJF%s(£\x0010·¤ýÉ\x00087)\x0019*m@6DjøäÜbw¼\x001c[\x0019²\x0012/Î\x000c`\x0015Ù¢lcA.äk`Q\x0006ÖAE![¸,:@[y|E?\x0008^\x001cv°oÞþ×ßþéûößßÿð×ßÞ}ü!7bÃÊ%RôT¾_1¨QÊ9\¼l=xóòß_ýÕçí¿?ÿòï\x001e¿ýÝß~ÿö_ß\x0018j:CM&¨°íÏÞ'XfV\(å\x0018]x9HmzÙå×qæ3ÎlÂ¹	ÎÈ8e)ð=8½þô¶oú"¶Ôî×\x001eßB
²ihý\x000c :¦G¾~Ã\x001alXs\x001f
ê
÷ý7¬E\x0006.Ç¡Ú5*¬Ñæ«nPÁq\x000bu»ýN¶\x0019$YÕQõ¶³
k\x0016æÀ«ß	ªL2Ï;"æ¡V\x0005µZ¡rdnU;V¹þ	i¨ .\x0016Ø.Vv\x001c\x001bÐ=·Ë6¨ \x000cP/ßç±Â
6V=°ºx°ªÓ)¹9¶\x0002Å\x0000`c\x000c4ªn\x0003#ñ@ïsþyBõI*\x0002\x0000\x001b\x0001P¶¡ò\x0000"ª<\x0008Ð·\x000fw\x0015mÍcU\x000c\x00006\x0006hñ@<°ú\x001djf²º\x000fªb\x000001@t}½a¦}áL¬CîÛ°\x0006E\x0001ÁD\x0001Ç,HÜFnm§58Wú\x0011¸|VÇªnV0Ý,\x0002ê\x0019ª¸\x0001¡]\x0004z½Ýp\x001ajTf6f­U&Ùg*ç\x001c×Ëm\x0016sdÕ§­ï®ªû\x001fíVgVs\x0014 ãg\x0011K¿<n£X^£,:w×ù¬éSÜSÄÉý\x000fìë`äú?\x0014²¯ #CúDß¿ûåÅ\x0017ïøÏw¿|\x000cdcY*9Ú\x0008\x00010È (R¯Mj}©8\x000cÏ ?~óâ7_þññOÃ3<ç%¹ÁÛã«\x001aÃ\x001e\x0007ú\x000flA\x0017ÎèÂ\x001cº\ã\x0003Kÿ\x001aýÞÈÑÀêfÑá\x0019\x001dÎ~Zy\x001a\x0002ÊQýÿÌ½[e7r-8\x0018A\x0018àãaú
©ª¤%¼Ifµ®~Ê¢!)ÛXÉº|¨uïWO£gÐ\x001afÒ#iø;Îö8ÈÌ\x0003ß×(IÁ"koøZ\x000e?\x0012ÙÞ\x0010×ÐÍ¯¦+èp\x000eWm\x0007\x001c@£÷ûÐÑ¹Nî
]>W¬ K{tiÕvÈ×e ópþdéé?\x0013\x0015xy\x000f/¯\x001aO\x0016§@,W\x00125ëõ¢a²^IÎ
¼²WV­'«2¨r»[côàà¥Ù£ä
¼ºW\x0017­7ödQ=¿ðRR¡0¼ùæ¡\x0005xñ­\x001b%»Õ¯+ë[ V\x0011ÓÌ×{n|Ý2BÇðiÉXÔ­!y¯&^Þì\x0017D3j=Oi_\x0014
R[WýøóòàÍ|³«Ã
<%\x001a~U5rár\x0008 h¼Ç\x0005'@5xó\x0005M+ðjøEÙ /&fDk7[äôÁtòË
>¥\x001b~U8òÖ*ÓÍWy5ïÞ|Ó"¨\x0015xJ8ü¢rs°r`tDÝ|0ð\x001dv\x000e¥\x001c~U:2rj
p´ÉÖXzÆºáÓø\x0015|J:ü¢vä²
ÎìöË´X£Þ*Þ\x001b§¥M+øvøUñ Uuü}1ó­´Ù\x000fåûâ´`p\x0001\x001f(ñUñ(Ûnª
_¦²f¿ÞJÒð¥ÃøxÀªxPu{\x00177l¦tÌ~%ýÒtÃÓ
>}áX\x0015vþàCK ÃËÓ·\x0015xJ<`U<Ê63l×B+ÖÞX¸å£ì\x000cJ=`ùÒ!£\x0018ÆË"\x0007Î¾\x000f\x0013õ´ü ýR\x000fXU)\x001eíød¨]£g7ðMcVð)ùeùð\x0012Ù·«\x001aÏ\x0006jßwÄ~0}úXÁ§ä\x0003o\x001eÈí@B£Ä¦Nè¥Z«Ø]¥3âöBÏ\x0019¹\x001fþùÝû¿Åo\x0003zÁ±£J¢íR\x0014.Ý\x001d>M7 ¿ùúÛo_¾þð\x0003üÀ\x0005{\°+ËtÂÔÄñ¾\x000fØ¥ÕK\QêÃ´¶øf`a\x000f,¬\x0000/BÍbêà	X(U¥i]ÈÍÀâ\x001eX\\x0001VÆ²&×\°BeùÃbaúVy+0Ü\x0003Ã\x0015`!Kó#Í{ïµ)!d©²ôiZîq3°´\x0007Î~Æw\x0017w=¶ÃÏ+µÁÇ«é'KÀò\x001eX^\x0001ÖX,ñ§ì6aó\x0017[=°²\x0002,9NR$\x001a#Ý\x0003Íf±\x0002l:Þôf`u\x000f¬.1æ

ßäIïº¿Z'±\x0002jä%:·º%seÊpvsÉµ0Ä±SÈã4§s32ÍúK´ß®	\x0018Ød[åÈf²*%ð>OkñnF¦xß¯\x0011ìùáMø]0\x0002â\x0010¤#dá\x0015ïû%âO\x001f­É8È¥£/J§Kío\x0006¦xß¯\x0011j`GíXÈÄ"\x001d\x0002¦xß/\x0011I_³ã0õ7
¿æi{ãÍÈ\x0014ñû\x0015æ¯M cGæ©¬ÇwdEÖOÒ³ä\x0011dùý
õWçx§\x001f­z\x000f\x000c\x000c¥²\x001bÈµ\x000e\x0000SÌïW¨¿Ò~©®â\x001edAÀ!@»p\x000f SÔï¸?Ë¸Íä±¢R]á²éÞ¾["YX"Ù\x000c2QÅJ&Ëd`¥¯H\x0016\x0014Á
Õ>dûÞóî2¤8ã\x00080E\x0019°B\x0019í..ºDkÎ«\x0000\x0013ú\x0007N¥¿\x0019rLXsL\x0019CÝ(#p¯\x0010mVó\x001f}LuþaåüW?\x001aÄ<fJ\x0014ud\x0012øÃ4ùw»0ýù/Ï¤é/kß3rQ"/§ï9\`^ëy;¸Çgà\x001e×¸6òU®UÈV£Ìkf\x0019Ü´HÆöT\x0001½Ûíó}?üÏ¿¾{ÿñAÌTgÝÒd>?\x000cepÎÞ\x0012\x0006¯þûç/_,¥!\x0000a\x000f\x0010V\x0001æP¸Ú\x0006Ûñ¥\x000e3H]ÜG\x000cnF\x0018ö\x0008Ã²	i{,
È¬ñ\x000c.Ób¸5q0®äzÏ\x0000¡rcgûÆcúnþpÖùf¸GË\x0008ÛÝ§C·+)ÏM!½\x000b'|å´G\x0011bbAÚØØSã¨$¯CLSõ_÷\x0010ó2DøÄ\x0010G­\x001b6á\x0010oNÓQ\x0014k\x0010Ë\x001ebY\x0003ï8l\x00103½Åm\x0010¥v\x0016W\x001c'ºX	§éo\x0014rÓ*3Y\x00031\x001f6°\x0004ñR°¶[6cÙÖpw¶Io\x00181ý\x001fÓòË5ZX%7/)²Li\x000cRÍ\x0014\x001au\x001f~*¼\x0019¢\x0016¿®-´äçç·øÁóiÌ8 N\x0007R®aTââÕ%û0F§{àM\x001fª»|êÃ\x001eã¼øu}IâÔÎÓO`Ø1Mé5J`ü²ÂdÚ\x00008¨²O14v{Ms\x0004k\x0018Äøuk6À\x0006&pï\x001dóëînÆ¨4Æ/\x000cíZObÇ@/\x0014\x001dqcÓìÔ\x001aD¥1~YdZ°ÀU\x0000H<\x0012wl\x001cÓ\x0016Õ5JbüºÆäÊ\x0013êÝúm\x0005\x001b\x001fR\x000f\x0017§Þ\x0011ÆÀ²ÆäX¸?\x001d©¢13Æ\x0010Æ>Ì; $\x0006%¦ôZÍ\x001cv\x00177ânêóû\x0004ÀÞ¬@_\ÖÕ%\x0005ZÞ\x0001b/ñm"ðÂñ`\x000c\x0014oÃ2o7¢ô´í\x0019"M\x0005d\x001f.¤½\x0019£âDXæD:{?sËóøsBý
ÓíQk\x0018\x0015áÀ2á´sÈÏ/
#pÊ¢è\x001fLçü¬aT\x0003ËÓÐÜ#jàD\sì±1D3+R1îo¿Ø§"¾yüáÇ¿ýåÕ)%ºévMÀ^\x001c Jar>F\x0012Äo\x001e^}ýÕg·@=Dø]B\x000c{a\x001d¢çMÌ4ç'»ÑEj÷ë\x0007¥åvq\x000f1þ.­{¸\x000c¨\x000b1[\x0000+[ÑK¥ÿàíåvi\x000f1ý.­÷\x0010óº\x0015\x0003_¥i0ÔÊS\x000eTÊm?\x0014ÎÞ°ì\x0011ß¥\x0011ë\x001eb]7¢çX\x0011\x0010\x0003\x000fè£eõbDü`Q×Í\x0010½fîuê¦ï\XHcù1öe	ñjñ÷:FÅ~\x0018\x001d¥¸æÊaì9\x0013ªm\x000f\x0005d·cT¬ã
´#	ö÷\x0007.J¨T  õÕ\x001f\x0012éOB¤J¥ô\x000bQÀWï~¡ÞÖ\x0005\x0010´\x0004/ù
\x0001z·\x001fÍç\x001c­÷ÓÚùW/¿ûîÍW·
Xa\x000f+,À
y,lsæm°¢$=}\x000f¿\x0015VÜÃ+Ö
²î¦P¼gkñ\x001cï§\x0002·¢J{Ti\x0005\x0015p}w,ÔâW\x0019\x0004ª\x001e¦«o÷°òÊ7L<ç7V?v­dêní°p:øVXe\x000f«¬XËSÚ²[+QÞº[AiõVPu\x000fª®wÏ«ô Åï1Ê&54¹\x0011ÖHLo°$1}«±ÆÑªcwzÍ¹\x001f¨
½\x0015W¸ü½
åÇ7{\x0005¸ØK*øù4ñ[q)6õKtêû´èHKÇ\x001d^kÚ$z+,Å¦~N}\x001dúåxH\x0006\x0018û/§£¨nÅ¥èÔ/ñ©çç·f¯*# 3õC1ÍOS\x0015·âB\x000b\x0017\x0017ãj\x0010/Çaåipv+,Åó~è=*5FÍ²_gw¼âtáê­¸\x0014Ñû%¦Ï\x001c(n;Kcx®Öó§è[q)¦÷T\x000fl/ZM$
T\x0007«NÓÚ·âRdï\x0017Ù\x0011\x001d=§±¹Æñ^On\x0005ìaì\x0003\x000c\x0011b-\x0018\x001at\x0004âzXäz\x0002Þq}ÎË¸\x0015\x0017¹>\x00069NU½ê\x0011\x0000Eö°\x0018;g&/j÷\x0013\ò\x000cnZt+.Eö°Dö 3jÀÁ^è½¦%p·âRd\x000fKdE³©ÓOB\x001c©\x000cv<\x0000K=,=ÏbªÑåøxIø§OÄ·âRd\x000fa}f²/iÄ\x0012ãtùékæ­°\x0014×Ã\x0012×\x0003=õwsmÓlUX?mÅ¹\x0015"zX"ú4vV/K#²L*lÆ>\x0017Ý+(J
KFø\Qæýæ8`M«n¥/ýKÌÜ\x001c×`U.i°¼¸"\m\x0014^Á¥\x0018",1\x0004J9e;
;\ræájÍí
.E\x0011a"Úgäê\x00072³>#zÈWkíWp)\x0008K\x0014òTï¨\x0002G(U6íé~Í[a)\x0008+\x0014A	þtK]KIÂTÏXâÏ¨X",±\x0004òm\x0003Ûørkä©ñÍ^á@ø\x001cU<\x0018WâA\x001a\ÈöªYV4¦g\ÁO«¯oÅ¥Ø+.±ôÐ6{áý0|Æ0mØ»\x0015\x0007ãJ<Ø>c\x001fÞùË-È\x00151×\x0001®Tã\x0012©zz\x0001éÖJ<Ö3æ¹\x000epDÔÔh0`ï\x001coÆª²wóò\x0011\x0003Lóö·ÂRT\x001f¨¾A\x0017"\x0017,7SÉ}\x0011pÚ×u+(Åóqç#/Â¦Í4qñ½?LwøÜ
KÑ|\¢yjs\x0018ò#Yë\x0003|\x001a\x0015Æ%>
|í§\x0011J²é¦á*ÂóÓ\x0017Ê\x001bq¡â-\â-à8º<%nX§­y·RôKô\x0000R\x0010æhÃF\x0012z8y+,å¸äÀÍ5HÍo!
,Ñ\x001e7-T»\x0015:ó¸tæ=·4´×=+bÀ¡Ó[Q©\x0013K'Þs«`dmÃ%lê§\x0013¦nÄÔOK'^¦\x0012¢÷À}H\x000bå§\x001bfnÅ¥\x000e}Z9ô Ë¿\x001b¡\x0002ï"ÍRÃN³\x0012\x000e Rg>-y/×ÆãV\x0016$Ñ\x0015æ\x000b#n}Ý]~&)»7¾\x0014÷w xäz\x001cõÁíã\x001ez×x¬]¬ ñ\x000bö<Üü§\x001b>\x000cbPµoô\x000bª}{ù·¿·ÿä§»/\x001eßß}öøÓÇç\x0011×v_\x001dïÅQêó*ÊMÈÕç±×Ë¯¾i?¾¸ûòÅÃë»Ï\x001eÞ|x\x0016ñÀ\x0008{`Àèäé± ´@eD¹\x0015ywµ_Ë\x00002ìAuÍ58aA­d½¢\x0019RZ\x001a]ÁçÙ\x00002îAÆeù±4Jâ5£\x000c\x001d¢¯}ÂçÆ=H4Y2ÉètäJÿfÉ$£ÓóUk\x0000ö Ó:HÚ%[:¡\x001aÛÈÍT\x001f\x0007÷ ³ÁnCÇÃ8y¶\x001cH¼\x000c\x0008ë\x001ea5 Ìä*\x001bÈvÝê)ä#Ï·eó¼\x0014\x0017l\x001cé\x000c\x001f»NTº^øcóî!ï®Û&\x000c(5\x001b¨¼q#l¤Ù·e}9íy®\x0006Ê½ËôÈÐí.gì7r*ÝU«\x0001¥âro ó)\x0014ì(³(Lðîº\x001eÎ\x0000Rq¹_'shöãg\x000eê\x001d­lÊÌHW¯§Ï\x0018P*2÷\x00066¯¯I\x0014ñ\x0008
¥Çr«¶V\x0003JÅæÞ@çÍwúX\x0006\x0006Ô°ïÈr±ëA	\x0006E,S	<¡fûà=ù\x0013'aé{\x001fwpP\	\x0006®Ì \x0016¹]¨P\§\x0008ÊrÕ\x0006g@©#J\x0003
ÕËÒ+\x001f%ìM½g×\x0013?
(Õ©\x0004Ã©¬\x0003"µãÊ\x0007ã«\x001a2\x0003Ju,aýX\x0006ºÏóV&¸Ê ·Àw8Ïó»êí CJ^·ø$ºë÷\x001bëý\x001f¿Ró¿þíÝG/`èr*ü´\x001f¨MGÒ^ä\x000e^\x0014'·°/\x001f>ÿoo©Ìùë·_½üðmlÀ=L0Àl_¼Ç¾!\x0007±%MzåsI\x0005T'À\x000c{ÁbÍÌ¤\x001e¨]Sæ'bÍiÖd\x0015&îa¢\x0001fÞ\x0006«vÀÃ*­9\x0013ÓRÚUi\x000f3\x0019`\x0016ÏG3dY\x0011e¥|ûæÓ$õ*Ê¼GmGÓÉ7O2Ä[ÅÓgUe\x000f³¬Ã,<\x001b3\Öïá@Óñ«(ë\x001eeµ\x0018\x0013xà~3¦\x001f\x0003Ï+ç´?Æ½§¦3\x0018³Ý¿;µ7k:~?©\x0008\x0005È»iî}\x0015§&w\x0003»Ó0\x0012`Ññ\x0013\x0001-¬\x0012G÷Ó!\x000b«8\x0015»{\x0003½Óx\x001c_=yÎ8T\x0018æ<ÁÓÇÅ¢Ã\x0016¹÷ì6qC<|h:\x0001z\x0015¦bwo w\x001aãÙ°32~°]\x0003qöê¸SÑ»7ð{iº¿ª\x000cyì*\x0005ç§ Wa*~÷\x0006§nr>É\x000fòÍÃ´>m\x0015¤bwo wÚ¥\x0019ò\x00082ÇqeHº®\x0012XÅ©øÝ\x001b\x0008rÀ\x0012z´{:ïóÁ±\x0003J¨ã\x0004Å`aÎfDaÎ\x0008Ñ
_ö,áÄñÏ\x001cýÙ\x0010ÌIÈ\x0016&eþð\x0017N+É\x0003øý¦Ç\x001eÄË;Ïª¾g?i+)8þ\x000cáÌÏÑ6¿·À-^\x001az\x001e\x0014I/paº?éF¸\x0010Ý³^Ëöqíøõ\x0006òÛÇ_ÿ×ý¿ßü\x0015-{/MbA*Ç$-W§M\x001c_¾}Õ0~ûðö_|q\x0003È¸\x0007\x0019- Gq{)ïFôå¼DNWy-¢L{É2ÉÖgê\x0013åÜFË\x0002L_\x0017Qæ=ÊlA)H#\x0017R¯Fo\x0018ÇA=ÈbûàAÚ5\x001d§\x001d®Þþ+Lï,¬{Õ\x0002ÒËFòR3×\x0013T\x001c}Fó;k /ï,\x0004rÜ7VM9\x000ee~nÈiAÍ"FP\x0018áwQQ7qPºO\=ïx\x0004\x00149÷hMfgÖ@¢\x0002\x00064
[>\x001eöøJ×Ô´)|\x0011¦"JobÊÊ£:"È\x0006!¡2\x001aýÏp\x001dÅÞBNÆ×ÇTÚÓ\x001dX¦#Ï\x0017a*®ô&²<+ª\x00118ÒhÖôbM¼zð]	ÀDD±ßéMêÊ[ 1\x001a
O\x0010\x001ePá\x0010\x0018â!ªy\x0012DZ\Ó×j\x0006,ÈÓnÛEÀÄF#l£Â×$\x0011\x001f½ÝÓq§0\x0015\x001f\R(ºfÞ\x0017ö \x0008QêLÏøèÊÑÁàè®\x0016/ÑÑk\x0001[3z©ÁsÓ­EÊÑÁ\x0018\x0015y\x001cEoE>ú(È¯t\©Â"0ÄEäBYÊeA:/.\x0014>pÿ]\x0019\x0014\x001f\x0005#\x001f\x000bQò=\x0008!5§
%(½BémÆääóÈ\x001e\x0014D*\x0003¥\x0010\x000fÃT\x0011\0Ep!\x000546Q¤rt\x0005¸\x0013â£ h3hÓÉåÚ~±\x0008LétÓn÷E66qx\x0010=Y\x0007I©rÎYD©¢¸`âÜøæ¥ÈL\x0012\x0013vÖ-ÂTä\x001eLä÷È\x001dZ1K9z½4\x0015à<m¸\x0006S{°»«RÔSkæW¶fM©§eIÇa*r\x000f&r£¸\x001feq\x0012µöKq®tZ\x0019\x0015mF\x0013mÑ<p\\x0014Ó+Ìq*Úh³T\x001aH¹Á¤<\x0007M\x001cB?^­¡ÔÙ7\x000bk¶û®¶8®kqhÎe[©X3XÓó\x00030s¼eµ}si$nþè¿\x0006SñQ4ñ6\x0014*\x0015:Áðñ\x0003¯éK(Q9\x0010\x001cHfÏ"\x0008\x0017\x0005-\x0017a:\x001fp\x0011£ò\x001e4ÝÕt±Q»\x0007ñ\x001e\x0019¦\x0017a*÷Aû¸¡æ8Z«ÌÎ ­eÇQ*ïA÷HÅ\x000cnE°ìã^|<Ò^Ã(UÌÂáÀ\x001dÄ4\x001dYNf\x0011^/Ón©EÊÇÑäãNºÈ\x0010ådâ°æ	0UÌ\x001bü»5\x0013·5ü\x001cÏu$uQK«iôíÕpÑréì
×Õ\x000611Wþæ\x0011Jt4Ä8t´\x0008SÝÔá¦FÖL0TÇtÔÀÛBý\x0019~\x0014g&\x0003g\x0012JÏÔî2o¬  ]éýqjOÊÏÅÏi[mw ÈÛ0ÏþÍ£\x00183O§ü®ÁÌÊò1\x000f±ºvÿÍÃ	O,YyP6z\x0010\x0016v¡,üÑaÀ,'<FgåAÙäAõ^¢ËÕBêÜ1ox|m+\x0019\x0010UdM÷r_{Ö\x0008\x001ae
\x0015órüÆgGI\x000eC\x0011\x0017\x0005®ôñª_ÀRE\x001cÙ\x0014qð³E\x0003Yv ,Ç/Y?ê¨Èà#¯Ø®:L¼îç5ÀT\x0001G6\x0005\x001còT²\x0015^0$ÊÄ\x0013RFY%9²%ÉÑ¬Øàd$L\x0005ÞÛÛ¢øé á5EÑz1Ñz\x001c"<ýÈÖ\x0014?¿nG5ÀT´^L´erS4®\x0016 Ï\x0016-ö<\x0001¦¢õb¢õ \x001bh-9R¤' äEñz1ñzà-1¢¸Êè7R÷ã(\x0015±\x0017\x0013±\x0007\x0019>\x0005\x0019yã
u5P­UÔ·.¼ûÕ-·\x00141ÇnE9]t±\x0008SéO1éOpTº­óbcPÒQ\x0000\x0015\x0000q	\x000f\x0008ã
$ßÓaU uUI~\x0002ïco¶ã*ÿÄ2/\x001b_©ä§äGö\x00024c&\x0019nRAb\x000eN\x0006\CYúTúpoü\x0016¬_l\x0019F°~üW%>Õ">lÈQFXÊpñpÂ÷®JyªIyÆ¤7¨;¾\x001c·È\x0013²­Uñe5ñ¥ìWÂÐ×!öS)Ñ\x0006â	ëªø²ø\x0012óç\x0006Å]î\x001a}<à¨/«1sà8ÄÌ·gÓ\aÍ\x0013ZU1f51¦$\x0005\x001c~¼\x0004\x0008\x0015Á	)öª+qM\x0019¸\x0015¹YsÌ\x0010®^¦Øcº\x0014´v'÷Nñ%ýÑð\x000e\x0010iMO·eåmä´;a°ÑQKz§Kq|ñpy.)<ø>ä5º\x001c×LYRÓ¸ýbM¨C$'9¼î	 ?\x0002äöñrû´0N\x0007.ÂÔ5¤ÎèèüÕ©ÔUÈ]\x001e¢q¾Ö`\x0005¦^(îG©"\x001dµâóéÅ«ä~2\x001d_'G\x000bÐbÔÛ«Ú=ÈÝkP;åqoßú9Xúü6´ã¹dô
eÜ%çÓz·P(\x0016§çê!å>Ú·ÿñ×_h¥ÞÝ«wûñ×ÿø(<¬}\x0002\x001c}ùPë© »\x0014Sº^pñõÛïh¥ÞÝ«_}ýö>lK\x0006¸\x001b-Yx´ä\x0002ÂH\x0013y]k;¦e\x0007\x0000äÍ-»6\x0017\x0011^R[pKm­Ø0\x0016äÍK¡xÇ\x001dJP[Ì=iºûEE}ä²úc\x0006.Ö
4\x0016¬ßv[P,\x0000ýõÂ÷Uê#ÅÑ\x0001¿QGXCIÛú\x001c\G_E
!."\x000cÇ
	"½o\x0008}àÅ5_\x0007À\x0008/W\x001eB¸]yV\x0010f_¹n#zjäí®\x000còc¼¾­\x0002
`üý\x0001L
`ú½\x0001ÜÅ»\x001bYoñî
\x0019Öéo÷\x0006\x0019\x0002Üî}|¯©^\x000fÆ\x0006ñcbâ½r\x0012ïW½ä··ànÙ°üî\x0010þÆ°ú\x0013ÍYïdí³2ñMNiZÐø).üè7\x0006\x001d0Àªüo° þÆ°øc_p§1Æ¹[0\x0014^dõ\x0011+\x0016\x000cú\x000bÅ/ü¿Á\x00014ÂE-i+iæÛî\x0005d½Rª?ÿÉpæãÖ\x001aÛ¢P\x0002GýxRâ´]\x0000\d{@X|ºÓ¸l¾¤!.
It%ÝbÖv82/Ð¢é\x0012\x001db.eB«\x0010«¸\x0018´FÐ\x0017å\x0004ß0õL\x0019¸ÜË\x0004ÈGÒ§ ~ô+GÍ2qehÃÑðá\x0018ù\x0015öÇEÁwÝ­±/h|«×\x0012\x001a XÙ~\x0000ÝIÀñc\x001c9É1tZã¢\x000eS÷ç\x0004Úr\x0012jç«XÏ_÷7-áË\x001a_^åì©Ñ®SÌ6H°k\Óç®ßðiï«ÞZ´ÏSQèÙ¨_Û\x001b,\x000e³b¹nÇXÚ9pÑ9Ú\x001d)òçm!\x001fp^ÉåÔ6|!û\x001eä\x0017Ôþ«þ\x001a®>UÈ%Ép7°
>©!}üþñgZWð!ÚEpÑEB*À·vÒ¶aÃ<lè>\x0019$|ÒÚKpÑKB¢Aã\x000c±fN}¸Æ<A ^÷X­BÔÒ :\x000eV}I§\9êñï\x0010ÃuÔ"Â¤}%-û
íO\x001d!f¸ç²ë³x\x001aÂ|=Áp\x0015¢öÕ\x0014\x0017¥Þ8=ã[8ÄýJ¶3ôp¡!ü|\x0012¢ö´*(Ø\x0018§çg\x001cxX={@ógHWì\x0015BLÚSÒª íÛÞý ö\x0006î\x0016\x0007zÖâP?Þú88í#iULZÀÌ*PSàI\x0012-\x0008\x000c,v4ÿÓo7³lÃÇ3Ë\x0016\x0000¦öÏ t\x001fiá5?¦§=æÉ´Ç5¶nVT{i¶LõNÿ%«s}³Qì*Ð\x0016\GëÚO£/\x0000×¼\x0005¯KµpÒ7þó¿\}õùÝ3Ô \x001f'è\x00172
ûÍÓûÿúÏ»/~þëãO¿<ýüñ³\x0019©o\x0003v%¸.ó$D7mà}óâ5áü¶ýþ»\x0017ß~\x001a'ìq\x0005'\x0004®{Kô\x000c-8+·êC?ð®â\x000c{Á³!¯7köìRtëìá\x0003m?«8ã\x001eg4}w~7kæL\x0003f¾sZ\x0016³
\x0013÷0ÑbÎ\:\x0013MçrG'{p\x0006?3íq&ãgObÏ1ðÇóCôÓ\x0011'«(ó\x001ee¶ lòØ£ÉfÍQïè¤D¯Ysº%w\x0015gÙã,\x0016Å]ÝÉ»¾<°Ùsúª»³îqV\x000bÎX¸*\x0001×;nï±Ýe:ïb\x0011äet÷ÆðÎäC³e)4I
\x000c4ðxµfÍi1Ç*P-E\x0016-¢f?ÌÉû\x001aarg4YtV'±
Ti·QÃ'@É¢|<\x0001»O;¾Vq*-ò&1¢Æ\x0005ñwwÏö\x001cÚ\x001eÊ´a\x0015§Ò"o\x0011#²çà¥"¥¤îBòÓöUJ¼I\x0011\x001d÷Xï{¿\x0005­»àï>-\x0017_©´ÈÄ(8^*(=^Ä\x0002=§#%V*9ò&=rÈËÚ\x0011p¡qÃbÐ8­Ó\\x0005ªôÈ\x0004¦n±EÁQ¥á\x00064Å\x0011%q@\x001ey µ«0°A³´
4\F\x000c\x0011§å@Ai\x00124©¹¹»ÄXùËã?§{«@&I<ÞóÏ[ÿèÃvâtÙ*N}=2IRûò.^\)Ë¿¸Ò	Ú	JÀ¦I \x0017\x0016å\x0001ãÌ \x001f>áJ 4	L\x0014\x001cOÎm_^6Æ\x0013Ëã´v\x0015¨\x0012%0\x0012­jçð®ÈíÉ\x0006=ã\x0004JÀ¤Jô\x000cÊ8såþ Pw@§;V*U\x0002*ÅØ÷¦7{&\x0019È´]f\x0019ç\x0019\x000fP¢\x0004&QÂÂ\x001b\x001b\x0012åB¯yoº,ÜÎPOPª\x0004&UÂÄµ}
h\x0019É\x0006Ã¢Wû

@R¥`»)\x001185Wâ\x000ej×ð\x000f_:DR¥`R¥TDif\x000f\x001b4\x000c²Ïî\x0004õ\x000cJI¨:
_JlP\x000cÃ ×U\x0010\x0006 :kgR¥²=¢vûq\x0010¶6ÿ®âTª\x0014li;ési+Uô¼ÝGæÃtW*U
&UªòüÛ~Ì\x001càµ/_%Ï`Ñ Ø>XØ¾¹äp\x001a%Éø\x0016w	HæÝµ«@\x0015Ý\x0007\x000bÝG\x0004^$Ô,ZÈ­\x0008(Ò\x0015\x0011\x0004E÷ÁB÷ÑËàÅfQñÙ®ðÚv óÇFE÷ÑB÷í/>Ê\x0014\x001fG\x0012¼L×­\x0002Ut\x001fM4(RÞzÇ;;¼\x001bt_ÎøòQÑ}4=Òär\x001f/8Å )/\x0002ÛGÅöÑÂö1dÉ;´Ï-\x0003]¼çÖe\x0017m\x0003PýHc¢{j\x000bfvËl8À©âIí£íc,÷òÝL{ðPì§\x0003aWaª+H´\AV ô9Ò5´GÌ¾^pNGÏ¬\x0002U¢\x0014M¢2aw\x0003Ê#\x000e}ä¡°p\x0006-)E\x0016EB_åtÝÆgwî\x0017Ù¨ô(ô(ËòìHùýÃ£ÄvèÎÈÛ¢Ò#´è\x0011U^\x0007\x0016Njbîï
\x0010xË\x0015 N9\\x0005ªô\x0008MzÔ.Gq|xÞ0ã3¯n¡/BÈJÐ¢G\x0018½¼ÊFÙ\x0014\x0018ém[ìy\x0002{¢#4ÉQ-\x0017o¯\x0012úR'M§¯\x0002Ur\x00169¢*µ\\x001eU6h\x0019/§<, ®\x001a°è\x0011Òb\x0007¶èe\x0000\x00048/?©ì4\x0000U&Ej\x0016urï¬ü°Ð,
¢ð'è\x0011*=B\x001e¡}\x001eTNÉ=á´+A\x001cél=*EB"aâº÷-\x000bÎc\x000b nÆxF\x0002\x0007&¡E\x0010p\=\x001a3ñ<[\x0018OÈè§þ\x0017&¥IÉ¤I1'O,²o¦\x0019RBúSèÒ¤dÑ$¤ùß\x001cD þ¯.uç\x0019¤¤D)D)HÃ}·(ð§¯0,zz&%KÉ"KHL=y×þ@o\x000cÝ¢Â¡ó9Û«8*%*y\x001c©&ÆNn\x001cÑéÔåU JIÚ-	XÒ\x0006²b\x00190^\x0017\x001aêb6Û=ÉÉ\x000bH#T¹%DS<#»*%*a[gR5\x0002i¡pF¸*%Sæ®¤Q\x001cA\x001cÉgtÃ¤c\x001dhVdM	1º)ñû\x0007:çÇóG8C=³¢ÐlÊ3áÖÕëp\x0012\x000fö4\x000eq\x001e
G =«Yn¿ å\x001f~xzºûþ×»o\x001a\x0003t\x001eX5#\x001dÒ>G $/;Ê¿\x001a÷ðêÕ\x0006ïíÝ7í\x0006\x0017öàÂ\x001a8èå\x0019\¢7Ù
,z/×î\x0016±Å=¶¸h¸|ÏvËç4»ñ¦+ájgÏ"6ÜcÃE»\x0015YS)JµRr\³âZÐ~ð£¦=¸´\x0006\x000e@ö\x0002b\x0001~i\x000bIÔÚxÕn·\x0008.ïÁåÅ¯*ky¨^¦o!n«â
×ó\x0002\x0016±=¶²h¸Ä¯\x0015\x0011«ã!|ÍpYÜ!^ó"¸º\x0007W\x0017
ü~Ú¾ªgkþ\x0010³»zZ\x0003w)/&pT^¼®]­ûåò£)\x0015tÉÃ«wýEt^¡ó\x001fVZ'Ûõ\ÇÑ>ìà¹xì]D§\x0004Â/*D\x0008\µC\x0015Oë£[+Od*éj\x0010í":¥\x0010~Q" rþdû²}I³\x001dúñe\x000f;ÅÃ~¡Èë&©C]sw]U°N\x0011±_dâe['\x000fJéÝ~\}ëJ½ºÚ/¢SLì\x0017©8\x0000¯¯Í\x0015xû\x0018{\x000c._\x0015.STì\x0017¹¸#\x0013VNÔ7\x0010pÕ\x001fT¯¨Ø/rqH|Í¤Â*)\x0008L¡éÊ1Ë¢bX¤b\x001aÉàjáÑ!5cÓÅ«(è\x0014\x0015Ã"\x0015·ËD/]h÷^'uó	\x0013È½ê\x0011_D§cõE*Î²7¦ÝJÛIªü¼î*^µ\x001f,¢ST\x000cT'±F\x001aÝÇ§.ñ]Çm\x000b)\x000eSL\x000cL\x0012õ[÷cÉÍ¶\x001d»«Í(è\x0014×Á"×Ñ,Fþ°\x0014\x000cSð
6W¯ç+/¢S|\x0002|R¤9g\x001bÆÃu»ÙÕrð:\x0011ËE-(:[ô|î¨ûÐyG
oÐ)
k.ë[PÂ±]nG°çPCö²¸»ÝVEAß¯\x0017]¶\x0006î©n¶\x001bWìr\x0012Û]õ\x0000/¢S7ì°vÅn'1Ó $¶/ëá\x0018£\x0004\x0015=µèÐõ¹TTÏ&Q{ö,\x0015Jû\x0000»\x0001\x0004\x0012\x0006Ðo¾osW` ýUY\x0012\x0001
ãUóôjüy\x00052-DÏ­@\x001cá
f	¦ÜU¯ïªæ>\x0007	°\x000c²q`à³\x0008[r¼³L°åªìvÕcl®¼üµA\x0016Ægªdå-Ã»]8\x001a1ãÕÇÆßß,W Ë2ÈäùÍ³E2ÀUb-Xp#¹\x001a5q\x001bHßþA¿øÞ=ý|÷ù?ýåÝÓO~J|\x001eÇpyJò\x0001\x0007üPÿâÛ»Ï¿~óÙË\x0017o>Z\x001e@Ã\x001eh°\x0000u\x0007:'\x001aß\x0017ùFÞ\x0010©í\x000c¸Ç\x0006±y\x000c7'ùRWOSÅÅ \x001fºÒ­\x0001Í{ Ù\x0004ÔÓP\x000et<)\x0014yR\x0000¼\x001aziÂY÷8«\x0005gáÑ7\x0004¤k~J\x0002¼z<¶àôÚ,®Ô\x000b\x0019âc%³>Éx\x0004À\x000f\x0008ùM@ÿg»ðªGÿNûG[\x0010ùù¿=ýíÝ{\x001aÑóÃãÝWï\x001fýø\x0006vþÚ´o@\x000eÉ2\x0015Käy¬ù:×õù\x001f_|õòõ6§çáî«×\x000fo?²ó`@
{¨Á\x0004µÝbzÇW\x0008T\x000fÌPyåR\x001a®Æ:Ú Æ=Ôh1sZ¦ôPñ\x0010A(#\x001eÛ ~hðÕ{¨hÚ®:lU(2Ì³6BàaÛ6®3¬öP	ªw2UÆál×\x001a*\x000fbËp\x0015.Ùæ=Ðl\x0002×nö/\x001aá³Ù4'ÒUÆÇ\x0006µì¡\x0016Ûç`	@ÛyÆç÷lÕëñ(6¨u\x000fµ ¦Â³\x0016U\x001d%üºUÇxúçñ	èx\x0013ÚÒ\x0005éåû#r¥}2Aµ¦rUcÃê\x0015Vo£*Ïû\x0015i\þÆTÝú×Nª¤Ê´*S¬Ç\x0007À3P.gn@ã9<åPyRå(ó\x0000bZÍ\x0018«ç	ÎQ*¯Ê¤*õþÄÍ¨Ô\x0015Òí\x001aJ\x0014¬×±
«*oÓª\x0010é5®Û5qé}Á_ÁUÿ§
«\x0000oÒ\x0000²káÃêP4 ÈLSús¬î®¦,­ô\x000bqi¥lÿþ.\x0006	¯®Ê±áÕsÄÑ\x0018Çt²úy²ò²ßû\x0010Ó`[u³înÛuàßÚ¿ëîûÿïÿþ\x001e~xúÇ÷ßÿôî\x0013º¨\x0010
û\x0015Ã6N§aÅX¥L3¹«iT\x000fzñúm»\x0012Ü=¼zñO\x000f¯¿xóò\x0006¨°
&¨±Ê×à\x000bO¥%J2ßëª/Ô4ì\x0006\x0013Òvo¥urQ£$Â1Q¿q7êõ\x00010A{¨ÑhÔÊ÷¬m"\x001d²MÇ Ñëñ\x001f&¤¸G¶7fÝÚC¿eW\x0010½4ÙÓù=\x0003jÚCMF£Q	Yd|k³ª>çpQó\x001ei¶\x0019µÝ²úÕ¥\x00195ós\x0017"H%M^Y-PË\x001ej±\x0019µé@N{àk6¶Øe´1_\x0015@ Ö=Ôj³*iloxÁ\x001aø1\x0007qt=¤týc:®\x0004ÿÑ¬YºÃ©×)0\x0003ø"\x000cp½õÁU	7*@\x0014ÛE»çÙ\x001aV\x0019EI\x000b1ÏÀªxÕÛ\x0015}!+4z\x0001ù¸2ú[¯Ê¡MX\x0015]y\x001b_Q½J«c¤=C\x001dë¥Õñª©ÄU±·Ñ\x0000¶Ë@\x001e­È;¹6f¢3\x0002\x0016P¾\x00056ßBÚÔ$½\x0010ÈOÎ\x0018ÛÑ^«G\x0013V\x001d\Ù|\x000bwÓ,èy\x0000/E§W |\x000b¾\x0015ÂhpkÖ@zÊ\x0001P\x0005FÇê\x000f6!hç61	ùèx]ìjªü
~·%®\x001djáÞGDÇ;{ÛEà\x000c
\x0008Ê­Ñ­ræÔPù¤
¦EÒGLog`Un\x0015nÕâ?\x0000!ß;Æ
AÌê¯\x001fü-X[\x0005£[µX;á\x001a¡òèº\x0016¶p];5ì\x0011\x000c\x0006åYÁæYT\x0000Ý×8$DÇ#·°Á3\x0000W5MXk\x0005kµóÈùÁUÒn8îØp5®Ô5*ß6ßJ-lá©H½Ú|\x0006k?¦WUùV´ù\x0016mb\x001aHçÑ#\x0016Ñ\x0001ZIq\x0006T}Ë¶¹VQºa\x0011X]Û=a\^Ï¸»Â>%\x0002»Õ\x0018bmz+âCëeXCÖ$ÒuÝk`Ê\x000b]!6\x0003n÷W\x0019¼Ù\x0018¡H*#]:¸Ï8\x000e.<G\x001c¬ÛÝZÖhÐ\x0001Ìa\x000eÆ\x0001>\x0007±ØÛ\x0011û8D.\x0016jñ¬ Ò±\x0003ÁgØ¤_È\x0002/\x001fÿú?~}úùîë_úåñãlN;
ïièH/È(/àÔP1\x001b\x0010ýåÃçÿííoï¾~ûæ»W	{`I5-\x001d¥¤âc)^úÈòU]\x0005eØ£\x000c\x0006a\x0005\x0004&7J\x0006ÌYÿñ*Ê¸G\x0019-(\x0013Ïàl\x0017\x0001/SÄ\x001a]]\x001aAfó\x0006Vaâ\x001e&\x001a`¶ktçÁ\x0018\x0012[Ð§\x0001óö0ÅC\x00063ðlÃÝ0æt¤Ð*Ê¼G
(©00\x000f<È¶Dð\x0003æ\x0019ß¼îaV\x0003Lø)6Ê ¾\x0012`Xó\x000c?\x001fÙÀNÎr6£tf$@*S0\x000eù¯î\x0015kz\x000bmúK\x000bdVOóK¥s¹\õñ[p*ÞôëÄ*½­°=C\x00188½4DÖ«fR\x000bLEÞÂ´©{£ªênNAy½)ÔR\x0011·0\x0003\x0005½\x0019Ó1qB\x001eÆMëX©\x0018É¯SRª9ò°\x000e¶Ì%À¹\x00069õªlÅ\x0002S1_§¤Tlp£9¶Ü]G½\x001dRâï¦³V\x0017q¢$X§¤T+È\x001c\x0014ñ^<(J'Ûu\x0011 \x0005¦
7a=ÞL´Ú1#µÐÇ\eÞìM8ÏpuÐñæ:s6Fò£m1zùìÅùñÙ§Ã\x0017Wq*æ\x0004\x000bs¢¬/¦yÐ2s3g7p^oÞ5àTÔ	ëÔÙ¼\x001d/8Ã}\x0011w\x0017%ª4\x000bý8N\x0015tÂzÔj3¢\x0004JínÌ#"3Ê®Ûê®:\x0013,8\x0015ÉÃ:É7?Jü\x0010E¥ê\\x001ceiðöÝO@@±<XXæ=ã}/ú£àôÓiq«8ÂY,~TyuÆöÝ\x0013Ï<èó\x000c5\x0002¥F`Q#W8¡\x001fS
\ì\x001b³÷âF0ö¿3(5
\x00165B\x0018ãA0p\x0016z]GÇü	¢\x0019\x001a\x0005\x001aG¨¨\x0011óªÌÓS©Q°¨QStÓ²Ó'£\x000cù©þ\x000cÕ\x000c:ÿaP£RG÷kÊòÛ¯eetéòUJE¢ccf^Vß)ÃÍª?ã.\x001c\x0014\x0005\x0014\x0016ÈàÌE|ô£Ør:õ{\x0015¥\x0012¢`\x0011"Ên1ô¤\x0008Á_L×È®âTB\x0014\x000cBTè<vÅ\x000e¥Tä£3ò4AéP°è\x0010HéFð½"6æ0®\x001b0Ý2¶S	Q0\x0008Q¡ø#²=%íÒ\x0018þ\x0010ÎHÔD¥CÑ¢CÔe$=»^veÇ50Dð'sQ	Q´\x0008QÚÔ§\x0013É¡6{"A$Ó¥«8\x0015ÁG\x000bÁ#[fÉ\x0012&m\x001bóÛpÔ)n\x0003Á\x0017j(Ï<9y¤XÈóë[Tì\x0019
ìYïðì\x001e¢%ÎË¶\x001f\x0007Î«\x0002
\x0003NT~\x0006?*©ë\x0006Í<`wRÓÅë«0U8©`y\x000cí[Ë&\x0014«Ü6â\x0019¯Y¨'Z'½óm¸Ê[Úâ6pN'ê.g\x0017vÏa ßX¢y\x0011¥X¸ ¸Eó(§Ôî|\x00057ÛàÒMC+¾/cPÃt¾îp]\x000fÝ¨Ñ~!o=þôÇ¿>¾ÿÄëp¥!\x0017îizW¯\x001d¡®\x0007¦ûè¦Sé?{xóÙÃç\x000f¯?òÍà.\x0005Ï\x0004N8nFç$GGS$rat«ùÀzÆ\x0005tÊt~ÑvíÎÆG\x000bÔ¹dÆ %:\x0017ÀE\x0005...ÊCÏ-0\x000e.ÊX¦+Ä\x0016Ð¡BkèâÅt-\x001aâ\x0012»*\x000bà\x001bºi\x0010¼.)tiñÃ¤ÞÈv=gÐlWaØî S\x0014®,¢\x000byñeAÙÜ\x001aÆÌ"ÛÑrYXtÙ\x0016ïËÖÄ5©4Ê	\x0005ÝtEí\x0002:¯Ðù5tIÖÙ´ð0ß³SxÞêNëTgj·\x0000NSñ*x¹"¯<+vo:¦þ\x0016Ð)BEB©#\x00064µÓS\x0004±ÝU¥é":å²°ê²QÂl\x0008	Fwñu\x0000ãt½ü\x0002º¬ÐåE2.ò\\x000bIØ;\x000b\x001dæé²\x0005hM`MÆhGh\x0011\x0017ÃIÖ\x0004ñj*×\x001aº Ø$¬²IâVÇ\x0008\x0018¹\x001b#9óMç\x000bà¿%-f'vl\x0019h WÇ&*³?\x0004N¹kXr×BoïAÐ{\x0016äÄrÓ¬È\x00026å¬aÉY\x001b¶v×ìÐ\x0014§Q\x0003@\x0015lÓ}8\x000bàC%(n,0æu6t\x0003'¯
½\x001d]T\x000e\x0011\x001c¢¸v£è\x0015³187Ü5Ëk[\x0017\x0001, S.®\x001eº*¯\x0018\x0001\x001c¿\x000e4ÛÉm"ÁÕ²EtêØÅÅc^^Öhåw\x001f¡¼¯®\x001c¼ëDuîââ¹ë{T7tqI·Ù§g5tqZÔ³®*tu1`\x001f\x0017ïd\x000c
VI\x0013lùÖ#àPEu¸\x0014Õ\x0015\x001aÅÎ¹@j\x0017¨\x0003Ütê\x00028¥\x0012¸¨\x0012!KT\x0017RâFÍäT\x0012¦!çXÙÁEpAóB\x000eÜÓ,'O;)M³Ò\x000bè\x0014à"D'ÑzÈ£u/ím
Ü´¢d\x0001ºÂâÒ\x0015¶\x0003:\x001d¶hèª?\x0016 ¢:\¤:b\x00106\x001cOZmD7°Mß\x0017 )ÃEû­Y\x0018\x0015Ïá\x0012Ï5Ã\x0015¹úÇ¦¯!3:I0¦zÕKµ.)õOêÒA\x0017\x0003Å&NBÎ&´Çî`IÑpZ¤áX%rN\x001aº\x001cÄv\x0007Ï]R<\x0016yÆÐ\x0006¶ìI\x001e` ;x
KÓ"\x0011£¬Ö4(Êzì\x000eFNIq]Zä:\x0004y%>r×K³äM²î³[@§È.­Æu2\x001a7Æ´M ëè¸íÍå£Ø¤îþiéî¿;Aç+×oÒ¹b»zQ\x0014\x001b§U6N<^0Æ&±5\x0016ä\x0019Úá¡SlVÙØI8ú| o¾\x001d]VlWÙ\x0018%&n <E·$vr¾ñ- Sl\x0017Ù6\x0012vmWE&Å\x001bÙ\x001f¼bgEÅy#uªtÃU¹Ä6ÏáÃfEÅyÊ	ºáâ\x0008P@
Ø3Lë\x0016Ð©8/ÆÄô\x000eÆ\x0001
MÙCçí¦Û\x0017Ð)¡È«B\x0011e¡XÓ1~N&\x0000±ÝU³é":%\x0014yU(%Ð<\x0017êéãðIlW\x000fNéD^Õq¸<¥ÿ5éÓö\x0002:¥\x0013yQ'¢ç½õ\x0011ÛBÄ"\x0013Å\x001f5¼(\x0013Tã\x001bé²D'\x0017Ë\x001dS¢T¢,ªD@ÉýÓXI\x0013W)ü*aÚ=ºN©DYU	/E\x0011¥ENØé\x00186%\x0013e5s\x0002ãÌ¥mD·\\x001cXaS"Q\x0016E¢ÝuäÈeÏã\x0002ÝFÌÇ.bEiDYÔ\x0008(÷È\x000b;3ÜgN\x0012:\x001e\x000cÒ²8)¼Ä»©¿çÊ=ºb\x00116\x001d´Ò²¨\x00114Sm×:\x000e9Û?SÆ\x0010àÁôQ4\ÖÄ]¢{ö"wr=\x000c~
\ULWW®^d'&hÃôÉçi	á\x0002:Åtu5;á$èÄvà×uïöà\x0014ÕÕEªóYbÎä@èDö5Ë]mÿ[\x0004§¸®®&ëP°Æ,\x00126QívGwT%ª"»ºHv-I\x0017#Zwy,/\x0007S\x0013Uq]]ä:pÑ-\x0017â¸¿JÌtPø«â¹ºÈs~{\x001bC-J4\x001c£é°ªáº\x0018\x000c7éÏ\x001cm^
°êØ\x000cGyNp]}!&æÑ\x0010 r·.uÚà|38ï\x0014	Ó\x001f×Ð¥}Ó½\x000fëG?æÕ\x0010þEx^Ã[¤áÆt<L\x0005\x000b"§<n\x0012x¬zÍëjXúãêë¿\x0014\x0018\x0013íIM§\\x0011?P`¼\x0000/hxKTk\x001d]¤ÿÏ\x001eî\x0002ðtÍ©3\x0014°á¶X+b¥:ÿjWÉ":]sê\x0016É¸QÜ'j\x001divù¨ñtÑ©[<ãØ3·gÙ\x001eÜ\x0005é¼	Ç"\x0014ï²·HÉõ|\x001cÑ]\x0001¡½0¢»C¯;Þé¢X·JÊn¬cO;\x0006áÔöÑÁ«\x001aÞbÂáãÛ¥©\x001ekÌº\x001b·\x0006ïYýZ¡ýF{£]v<Ê:¼´\x001cËyz¯EÃ/Fû¸ÒÄ
\x001bÒ\x000e\x000fÇX«AÇð´h¬5\x00024Ïå¡íoÆ\x0011¼1ñ$]m\x0013[D§5Ã¯k\x0006H@à¹	JcÇ`\x000ewÐxW[\x0001hÚ¾´ôa½F\x0013ô´Gf\x0001¦=¿Zºù\x0001WX¤\x0016×ËÇ÷\x000bP£\x001ec¯if£úâ>±8B¼Ô,FI»c<øÜSãÿòìö5éõ_Úm#JÌ,uFí¶qðM¥üù§%¸é7K\x0019D}2ý¶æÇã\x001f£éüÁ+\x0011ç\x001aÃâ§n7#'}=-\x001eà\x0019¯\x0014b·|°Ø-Õç S]\x0006ù[¿Ûê\x0019´Ó,ûLÎ÷\x001bUZ`wÐb\x000cþà#dy1uCfÙôLÃþG±TLîÁú÷æ×Ïüúq9ùR&Ùx0ûâS\x0000ÕÛH¿ÞFZû?=þí/?¾ûùÝÓO\x001fßK\x0006\x001e(e*r)ñ5Nß$i}î?¾yøê³¯_~ûòÅ¬ú\x0015¨a\x000f5 ¢aXh\x0001Io+	
CMqv\x0005X\x001a÷P£	jý#Íª2F\x000b«\x001bF½ÚðfC{¤hûþÓXÚ\x001d¦Ê÷çù~¾Î{!Ö¡¦=Ôd3jæ&üfTIî÷æU§\x0003q×¡æ=ÔlîÅ¨ÆiH9\x0011Ñ:­â\GZöH	iMøÇ\x001c\x0002?#bNßb\x0019Ñ¯C­{¨Õ\x0002µtÏ¿Ôæô\x001a®FÎ»âT®ëV\x0015V¥\x001a*V\x0015¬q:ÿk\x001d«WX½É¬£¨\x0017s.÷»s\x0015²
ÓÄÏ:V%VÞ¤VÕ\x0003WÐ4»\x0006Q«öåáä3 ÔÊäª¢ç¤F³+ò\x0014Z¬\x0005\x0012c«\x00036¬J®¼I¯j\x0004râô\x0010Vä÷ú\x0006uÚ[»\x000eUé7	\x00165Ç÷J ¤íÏ±ÊdR_ýôù~\x001d«\x0012,oR¬JCù¸n=\x0007±\x0004,óÜÂ:T%XÞ¤XÔÂÔcé\x0006µÒ#7ë,7-×¼\x0019kh·é0\x0016ý6!¼üÛß\x001b\x000e÷ÍÓÏOß?~\x0002)u÷Å#¦¥÷
T]F8!º«<ðË¯¾i?v¬o^|ûâ\x001b`=Ì`	¾¿¼¶o²XÂ	«BôçàÌ{ÙÓÓ@b\x00062{\\x0011Óôüp=ÎbÄ)+H	'\x001btìG:\x000bhÝ\x0003­\x000fï=iÛêÛ3èÒe­/ñåGÒ\x001dÉ<i¬ò
.÷²ÅvD9ëÞ\éêAÊ\x0004T{¼ÉåA/\x0012T5®V\x001di¨WYP\x0013RPHÁôñË=/\x001föòRÐ¾}\x0008ãÛ?¥L@\x0015;y\x0013=õ¯]½¬suUÈéº$Ô2*Ñ2ö\x0005~\x0013÷Õ ôé5W×=\x0013JT(ÑäGkö\x001fU¹¸#]%&LHB\x001eÏÚ	ßÙÈãE<á*«g\x0002ZF>¼C-ÿðß1ÖÇgX\x001foX}ªNÅNô\x000bÙ"õ?=}ÿôÓ»¿Þ}ûã¯?|bÝU;×H!mIàk\x0008¼\x000cÏy#Ý?¾yñÅ7/?¿ûöë·¯>²îj\x0000=P0\x0000m×Ov)\x001a\x0000ÃsK)­Æ8q\x001aä/ã\x000c{ÁbÐ"óÝ1õ\x0019A7^ù2ïKX\x0006\x001a÷@£É G.b"Ks\x0019@óô\x0011ì9Ðö}úû\x0007Qâ\x001e%ZÌI\x0015<±\x0013¥\x001d0ÒÏÒO«Íö@Ó:Ðì][è6s³\x000fX­¡ô7\x001cpó¹þË@ó\x001eh6X´ÐHnÐ¹û3bÜ)0-³\ÆYö8Å ^:·°Ð¡~>«¨\x0002\x0007Ów«@wÉ=¢PgA\x001aj¯ZEÊòõ±X¬vaZÆµ\x000cTs½ì\x000bÊ!¤]	2\7ð6ÆFöÓÔþ2REöÞÀöÍ¤\x0007YamW&\x001eN^3w·\x001bÕ´*s\x0019©¢{oáûR\x001c\x00186\x0006YÊ¤J®\x0011=é-#U|ï
}UíØ³{ýJïÒÕ-Ô\x0004TQ¾·p~i7:WØ¤Zs6Êæ¦fÒé+é2RÅùÞDú
^÷ü\x001ae~\x0013n£ºIó9§Tq¾·~má(\x0007%)ÒMë]\x0015Ç\x000fÖ]\x0006ªHßX?×'zà-ÂN^I§mlËH«BZM&­ü4¡\x001eyµ,îj6\x000ex\E
JÀ¤OyµÙ\x0014·zíÍ¦ Ëä]>/#Õ1¾ö[ÄÜÇz í\x001bCNCpùÆ¶.å\x000c õÁÂúµáØ9¥Xq\x0004Qy:µu\x0019¨"}0~ãÒþÞÐÄsäÆQî¡ÞM\x000bÉ**\x0005\x000bRÊ\x0004Øñ\x000brß/Òöáo¯¸\x0014\x000c\©Ù\x000f)mz\x0019;DAÔOû»*2\x0005\x000bB\x0008<\x0010,Ñ\x000cI.:qUÒP\x001e¦C­*2\x0005\x0003¶x¯ßñh
p¤/(\x001dÞt\x0011ý\x0014Ê 4Xfªæ¾0¾)\x0008OâD\x000fAì\x0019§uÕËHU¤\x001f\x000c~Q'w5^òO®Mo»Ü\x0012©¢ü`¡|ÈÈ\x000føZÿsº2<\x001cZu\x0006Ø1p~Ñ \x0019¨ÚÌë¡dÐÉ¶Gö\x000c¤ôô¡n£	6öZÍ¦\x0017.MÓñ\x0013ËHU¨\x001f\x000c¡~\x0013üH\x000fwÝ¦³\x0011$øbÓzJZ/(}
&}ji¯»O-lB\x0013\x001fäÉÎ@ªô)Xô	ã¾rª-z\x0008×"\x0015Ñüé&Ìe¤õõ\x0001d&dÚCóýI:A>3ù£ùË=¿<ù0*
=ÈÇ6K-¥J£"ýh!}äÎïÌ´6+6¼ã6àvÇ;%½\x0013\x0015éG\x0013éScMfgÂ{>¡íÂÇæô§Ü£âühá|HH
]Æ	õ+ó:SR\x0011û¦\x0016ÉïIíûZî$\x0005©ÞÝÖàöÔILqdøNIçx	nö\x001eiÞÆU\x000e%®(i¾0\x001dö·NªÏálÃK\x0007\x000b$¨G'£\9\x000fá\x0008ÞvÚô³\x001eýBõ^ýúýÿõî_ïþôøþî³§§_þíÇzÿQ°-Þ\x000cûE%Ð\x00066äÖ½zûÅÿñò\x000fwzx}÷Ù\x0017ßýñë?½xýiÀ°\x0007\x000cfÀÑ±\x001e -xíKxH\x0010äþ\x000fÓøÚ\x00069ì!\x00073dïxþ
µHpJÒ@rýã\x001er´[\x0019äa¥ºÌóI\x001a©y¹¿éL|\x001bdÜCF+äí]¥· ¾Ø]ÈuÆOÇnÚ §=äd·räáyHkÍ¼X\x0019Äýæû_ló\x001er6[ÆK±÷\x0005Î\x0015Ñ\x0014v±ñôÒ`\x0003\öàª<\x000eS»°ó
6nò1»Ù ×=äj¶q\x001e}@\x0006¡1d(â|Dþ'A\x001eO]FÝÌQ\x001eãh=gâQêà¸éÒC\x001bf-}fí£½¬læZôÉøªSÄ+ñófõ#É«áÄùæoÈ6¼Jù¼YúJLÄÄ\x001d¯¿[ì\x0016B
ra:ÆYI·k_»\x001b£°r\x0011Ì$ã9N\x001fAmöy»ø¡\Ú©ö\¨Óì,%ZuÞeÃ¬ÄÏÛÕÏ\x0003mÇè)]äJMZ=ì<\x001dÎbÃ¬ÔÏÛå\x0016¡1ÍQ³s7s	òòx¢üy³þêä	²R	\x0017[9&yØvhØ +ùóvý\x0003ÉQl\x001c\x001fA ûó0Ò?0ë\x001f]j¼\x0010\x001dkv(e\x0010Ýi¡\x001c(ý\x0003»þùf\x0007 \x0011\x0002Æ\x0011ÌXßýìòÖ¼wjN<å<D7NF¶Ù0+	\x0003\x0012\x0007Íaå\x0011\x0018áR­p\x001ai@0K`Á$Y\x0001\x000eìº£\²ã´@ÕYI Ø%V¥ÄñLE\x0002Q.Se: ÃYI %°`Êê\x0016\x0012q\x000be³³¤\x000ei\x0003èi\x0004]\x0002c.eZ9¤+e\x000bLël\x0008]\x0004ãe\x000eéz\x0002¼Ûy$Ò´\x0000ÏY© ØU0\Bý\x001aø!¹ÙY²FÆ¨9(\x0015\x000cv\x0015DîhØ"[Ù\x000f¦Ö\x0010Ù\x0010+
\x000cv
\x000c\x0003ºDS>ù0g?^¦Ó`l\x0008\x0003"/ï¡ßGB¼LgBÛ0ë\x000c¨]\x0004iM\x000f?æ\x000ccn¡Føt¾«
²ÒÀpH\x0003y®^\x000es2^\x0012&(	\x000cv	l§ÔIÐ^\x000e>Í2\x001e\x0019|¾Ù0+	\x000cv	ÍLKÃùõ¬Éö°3LÃÛ0+	\x000cf	¤é<òÂC;;d\x0010\x0007ôy:ÙÑ\x0006Y©I0«I.ëJ®xAì¥»Øóâ¹¨99')öÛ)ú\x0006Ò\x0000Eâ9?_}gÃ¬¨9©9×<\x001c0ÉÊt2´\x001ctZ.*fffÎABÐäiÜX÷?@©Zð'ZY¿M¹]FÉbIòl\x0012Fý·¯ç%è¢¢æh¦æ\x000cI\x0006\x0011x(\w\x0011 ò$âö?çEsQEÍÑ\x001c5·pMb#\x000f(r\x0002I
Ö\x0001\x0019U\x0004æ\x00084CåaãÉGÇcmØ9N·*Û0+¦C3Ó%ªÀbÌÛ\x00080ìÔaB9ïBèÐNtí¶*fn~ßüÙÌ,\x0017ª¦§\x001dgTLf¦£®\x0016A¡\x0005J<òÇä7\x000fn\x0004±aVTvªsx\x001fØÎy¤\x0015Áó$ßæç=«¡~7S]
\x0013^
öùÅµ±\x001e\x0007\x001ba:òÕ\x0006Y\x0005¡h\x000eBSE	B·jSf\x0011ìCÖ\x0018Ù0« \x0014ÍAh¢MÞ9\x00179\x001a>\x000c¦v\x0018Ø +AA³ ¤Æn\Ëé«Ôq\x0007_¥\x000b\x0016Êyé[T3\x0003ç\x0004£Ñb}1³Ó\x000cé¼J¤\x0004%Ù\x0005\x0005\x00027s%êâÐÙ{iæ|Z\x0018\x00149';9ûÄ\x0006ÚÑð\Ü.(I\x0004eZ9m¬¸9¹Ææóx!_$
3ÖÕA81A\x00145';5»Ê\x001b6	äû«#Ô¨çeè®2s3¶;Uê
5í\x0014H´ïdÖl³ó´ÛÓYqs²s³ó\ÁÓÎ|³+ò\x001a\x0018(\x001b\x0016fEÎÉLÎXd¹q;Ø·àö\x0017Ì\x0001N\x000bC"çd&g¬R@×ÎFà\x0019JÁei\x000c
þ¼.«\x001bJ6ßP0ÓÐ´
2"Ý¯6È(Å]´nà4ÈJO²YOh/\x0012_\x0004©¸Y¬,Iòp=¨È\x000eY]P²ùiÈ6PALO8»qß\x000e'\x0016d¥Ù¬X¤i4QFÿ\x001bÆc`óbý¬\x0004%\x0005\x000e³gAI\x001e·[+"\x0018Nt@]Áj&gZ|axà8\x001aÃ\x0003\x000fsô)©ÚfúÔ6ûøîý/w_>5Èß?Ý}öÓ¯}üåé.¡$¹¼¶\x000b«¬ C\x0019ki\x001dø5æo\x001f^¾þîîË\x0017
ó\x0017/î>{óöóï^¼ú4ê´G \x001e=<Íð\x001cÕ5ÔR/çS:¬°ó\x001ev¶Ã.ó\x001a2vÇ\x001c¤ÌòdS=ærÀÔµÐQî¦²ó\x0007A®°ÍÔ3Â³Â®{Øõ©!qyZ3uäò´ftÃ\x000cÓ¡÷FØ£Úy-ÕÎfsw\x0012¡ |ãhôMeZkÅ
7\x001cÀM31{³\x001aq7nÄ¸qúveÅ\x001d\x0014î`Ç\x000e%\x0004¡\x0019¼Z&Éº²v¼O='QáÇ¨o/i4¯\x00110\x0003¦<m¶³âVrã\x000fè
\x0002Ü;Æ\x001d
ÏI)KÙè6\x0017è<ÜJpü\x0001ÅÔGÃç¤ÝÊ\x0003+N\x0004ñËùV,+n¥8þä`ìD+f{\x0001wJU\x0015g7]þbÅ­TÇ\x001f8
¢7ÙñloéÍÏ~ZÀf­TÇ\x001f\x001d¤\x0002G>Þ0V[f/ì¦W\x001a#nP²\x0003\x0007d'b½G¶v ,ûfíZ\x0013\x0016\x001cuÆ\x001d¶?`î\x0016½ÆÀæ\x001e;·2ÊÓK;çgâVj	\x0007Ô2&Ùo(ÛÇjäR.hµâVj	\x0007Ô\x0016ñ1¡ò6w©â8m´ÂVb	GÄ2»WzÖßx\ú!S=38\x0001%p@,)ßÎs?è£¿x¥âÆí\x000cÃ,§cÅ­Ä\x0012e®÷¬9>ÓËÌfnãtOßÊ­°VÂ\x0001­ÜÌÝ½2SÖ¯¹¼Ë´ÌÆ[i%\x001cÐJtÍ\x0017%¦Ôc¶Ù;JdvÓ*H+n%p@,\x001bßI6F-ó\x0016í¥Q¤Ì«Ô¸\x0012Ëp@,Ñ#]möv²¥W¦®6sO\x0013ÚVØJ,Ã\x0001±¤ûdG]hÚzdòÆ¥jm¥áV"Í¼¹H|\x000fMÒÐ&ñ'r`PR\x0019\,k¥ir¹üÔ;'	¼«?34	J+Ã\x0001­ÄXùõ1µ«\x001aç\x0003³\x0017\x000eL5yJT#÷Êâxvk¢³>\x000e7åÑÄ\Ãtè\x0015·Êp@*1_2>óÈþC.C+Ï<&J+Ã{eòÜùÒ\x0010¶»\x0003\x0013ûp=5ß\x0013V#ZYêÈ\x000bR0Ën)Å¿©Lo¬°T#÷Êv\x0007\x001d6Íþ­\x001cyó
Wh×\x0013\x0015>*¥\x0007ª/òHfò%>×\x0011wi5\x0015¶RÊxäZÙ.	K¨µ9sj\x001cí|fø\x001aPÆ\x0003B ËC{rcwqBó>+l%ñP\x0006vÔ4ÐBÎÔÓ\x001f1w<I¢\x0012Êx@(\x0013\x0015\x0008Èdfî,ÖÆ\x0013;*¡\x00072\x0016 $ÝÜ<þîfÂ$y:8Ã
[éd< É\x0007©s§I|zHó®
+n¥ñÈßhcpd{;ºë¼uÃ[éd< tºAò¯&\x001dõÓ-usóí\x0002VØJ'ãg¿y}p377×%\x001aH0¸äDk£ÒI<¢4R^++½§â½ä_áÌW\x0011TB\x00072Bü+ÍÃâàx<«i:íÕ
[)%\x001eQÊ¾[|3wn\x001c¶¶LNÈó^\x000e+l¥x@)£÷E¬í%¯P¹§ë¬¸Râ\x0011¥l7xÉ\x001aG9Ù()ÌS.9 @³Òz0EMþüN)Ë ª;3?J%ñJ¶Í!`vÅ½\x000c\x0016Ég>>¡ÒH< 4à¸7'\x001a2\x0005lëXE#Ý´Ô[i$\x001eÑÈ@89_¹ÅÎ6ûÌ­\x0014\x0012\x000f($Dp»¼\x0004RTv)ÆVÄ\x001bq'%é Dr\x000bl\x000eE¤¦x7¬=m¥±âVZ\x000eÝÊêÀ^
\x0007
UJö´«?Ó)"ítÎõ¦]	äî^<­3ÜI\x0017\x0006\x001ea@ãMF²O:\x0000K8³.&).Iâm¸§\x0010äù§ô*å)äDeÏÊ)ó¡üÎ(\x000eÜÆ$¡$x\x0004v­'ÆÛY\x001dî|$É\x000b5ãIöÒ\x0003g!ìå°ÕáÎÅGQ%ZVøÁ,ÈËS·OäÀ¬\x000ew>tÅ(+©	wæÓí¥hþ\ÜE\x001dïrä¡/:)¦1Z\fª\x000c1¨ó\x001cVÜJsÊ'3\x0018\x000fÂ4Êñ\x0003|º§C\x0001¬¸[#né@ÕhPxÍò-É©\x0002'ÆTEùe9RïP¢\x00045"\x000f\x0007 çJñËræ£YÑ¥ÝGìR nÁASr¾Oªü²\x001e©V#tÃl?r¦\x001b³t¯{NªòËz¤ì\x000b²\x0014\x000e_f.jÄ\x000b¿¬Ê/ë\x0001¿\x000cy{Nxxh÷3¹ ¥Sí­ü²\x001ei\x0013¡
*,ó\x0012ûr·ö{yÌ®éÌØ»*¿¬Gz.ÚEÍM\x001dÀÝ-³\x000es\x0006Ú;åôG;ê\x0016zË°G©xÁ	\x000bb>O-½Ó­\x000bîHï\x0007É¾ÒìèÊö\x001eÃ0*NW,Yë\x001e\x0000wÄ/QVÕE^\x0003¢\x001bwù8\x001d¤c\x0005®éÝ\x0001Ç
\x0014½öjÄiúPG>È^·BÑ\x001f\x000fd\x0005LÔ)\x0005xFi
Yæ×¶èö<ÁôÏº´\x0015\x0001:aÂe\x001bg
´âHªN<)ÏÚô\x0015Ñ\x001aQ.-Gâ%\x001aí!\x0006?3y¼ÛÔ$	dÙÔdsOäê\x0007Z¯àX}Fæ§úÌ\x0000Wèá\x0018zÊ¤p\x000bn»8ðº)Ê¤HÂm:\x0007Æ\x0002¿²}:Þ\x001cú¹É>ñ¤\x0004ÊÍJMl9³_'çðC9\x0004\x001fÛÛ\x0000©I\x000b¶zïþÜÎ|È|uvò1ë{j¼L£¨%/$)Ï3\x0002\x0001ç­y¢_H+ôÃ\x000fOÿñøþûîþðë»\x001eýþS¡ËÖÒ¨}¿Åè\x0012\x0001 ùmòÃ5âW/þéáõ\x0017o^ÜýáíË7\x000fo¿ø4Ø¼\x0007`=\x0014ÄBåõÜj\x0019¹d°=\x0007jÙC-6¨!óî,bÃqqH90Ôy7«\x0001lÝ­F°³TíçK4UìZðC0t}\x0003+²¾6zÞ?µs<´Õvö6´³Í \x0003ªWP½
ª©ÿ±\x0014\x0019M"\x0014>\x0005~>¹Í`Ø Ð\x0006ã1(ü@þ¼¾¶[fF;_[o@«ËÛ«O^%'aZ){n¡×4Ci\x0000\x0014Ød\x0003äy:*\x00132¨IÏ¬GD\x0006´»¼¼ræÐ3nñ\x001b\x0010ðbÚ8-2UÜåäESÅùÔ\x001bUû±\x000e°§`\x0005E]`¤®T]	+½¾T9Â«ó¼×\x001bÐ*ö\x0002#{¡,útÉv2Ù\x000b6ÓN\x001fú
hA¡\x0005ã¡J²H¹£\x0004lÛ"§6ùNâZ0rm»ö(=R.°m\x000bmçuí\x0006´Q¡FÛ\x0016..T\ÈQ"JÈû<-ù5 UÊ\x0000FeH\x001f\x000b#íÚÉYfä\x000cÛN\x0017\x001bÐ*i\x0000£4PY2\x0004Éç\x0013É¶x\x0019ªè\x001bá7us%>\x00052\x001b®Ù5]ótö\x0001­\x001210X\x000b¸X\x0017*\x0006^kÜL+T[Ïr0%b`\x0014±\x001cïÙ¿hR O!ð~\x001ciâ:Ø t!\x0018u!W\x0004G\x000f!Ò\x0001>\x000fÓN\x0017L\x0018Ð*¦
F¦-2ð9Ò\x0016+\x001cs\x0018-tk\x000cººª»O¡½¤Y1ðûµy¶ÒV\x0011B0\x0012BéÃq[èÂ\x0010äzó\x0011ü\x0006´ÊÇÍÇbûK
*ÒV"®{Á(z;\x001d\x0011¹\x000e4*ÿ6ÿN2¿Øþ1R[\x001fÕ\x001bÖi¡¢\x0001­»¢-îí:Þ³¥M	ª¼Ù!mØÐnã\x0016OA«Ø ÚØ :Éw¡£7iy\x00069²xR¾+ª¸+Úâ.jêàå¨®\x0016®jÆZÅ´\x0010Î	»¢â®hã.\x001a\x0014Å+á\x001fÜ´D\x00149¶óÎ\x0019\x0003Z\x0015vE[Ø\x0015iTl?¶M°Æ8.'h?05ÖV\x00053Ñ\x0016ÌDº8ö=p\x001e7=ëu6¬aÛ;Ü)`\x0015ÑF+Ñ"';Ð;QP\x0018yU;¶ÓÇÙu´¨îäh»Çù)¹ÝH\x0017^z%ÑLéÔq\x0003Z¥
hÔ\x0018d¨oÚ S\x0012«D3´:ù\x001c´J\x001bÐ¨
\x0005y\x001f<
GG1­<.D?m¹´0Âî\x0019GXAq]M¶d¡\x000fIîºÉó>\x001fpÚ(oÈ~ùç ½·\x000e.s_WO4{N4W	ÉOK4û?ÿòôÓ3Ðô\x001b\x000bhï$|¤Õß\x001c\x000fA.=0ñtc\x001e¿ýÍa{\x001f\x0019\x0013»\x0003\x0005\x0010ý\x0018ùãÏOÿ·»÷ÿúÃã÷O\x001fE4 ®çZ¸\x001bÙ´PCîy¥vYÎ©øòëo_|óÇ»×xõðÅ\x000fÚuÀ=L0À¤òÿíØBÃÅ7_Ry£hü\x0004a\x000f3\x0018`ÆÀYûvÕIÜñDE\x0018aÂ´Ka\x0015fÜÃ\x0006t4Ù\x00189iÐxGóe\x001aË¬ÂL{i\x001d&]Àz5£ýÊÓ\x000b¡$\x000c3M3´«0Ë\x001ef1À¤+xÿèôÈ\x001cÙ\x001fC\x001bL+*\x0016aÇÅîéÎ3GfÑP<¯
ÒN*ÃÓNûUÊÓ½ÁÕé1)óWw_¾ \x0013ÓdÑ*LåBÞàC\x0001\x0003Ç¬!×È}kÄr8á\x0014s*\x001fò\x0016'À­<!ÀKù W9¯ÙX©|È[\x001eéÙ\x00198+\x0000¹ð³w;þùÏ^\x0015ÎjÀÙnØÍ	·øÐÀFvv¦\x001dÄ8A9;X\x001d¤\x0012³IyàL\x0000äÌE»ÎÕéÜ¬U*ü\x0000Cü\x00014\x0017½²=å¥\x0008rä×Xê4=<AÇ\x001f\x0016VrgH6\x001a­ÔÓ¿»\x0004 ®LýU*\x0000\x0001C\x0004\x0002ôþÙçÀ;F+Nð#Pô	\x0006ú\x0004ë\x0016;Î\x0000ý]\x001b²ç±/´fv
Y
&Z`n
ÔÍ÷Ù\x0013b\x0015sN÷¬âT,\x000f\x0006T¹\x000e8äÞP½á\x0019QÔ\x001bzÆñÌ
g¶à,|)jöô<¬p9ý\x0019æTj\x0004\x00065\x0002Ó0g`Ú°g?ÌyÆñTj\x0004\x00065"=ÚÍ3ã9mYÄ\x0019\x001a\x0005\x001aA(üJµÙ³Oq2\x000e{ FA©Q°¨QÃéØÆ¤`Â	bÏé.UJA\x0000¤\x001a¤³'wÉA=O`ù ¯Ã\x00165ÄÓ¦=eØ\x0000$ä>r²ç\x0019ß]©Q°¨Q»¬K0O3ºº'(\x00179:>£`#Ç\x0019ÇM"»Q\x000bë\x001aaN¥FÁ F¾:ÞèÛÌ\x0019y\x0005#$W\x0006}áEJA|\x0005\x001e¾¹ÅòÀ_]¦s9OÈ/\x0004¥FÁ F>ótþÍ½0\x0005°ÔaÌ\x001343*\x0006÷XÇE3$Þ\x000cxÑö\x001cÎÀ©¸3\x001a¸Ó74®ia±d<\x00118Q'Î¨st\x0006NòÞH\x001e\x0003/è\x0002Nvã¾å®âTÎ\x001e
ÎîÊE3[tÇ1\x0008uxÉÍ}Z´SyQ4xKEòJ¹¯.Ýp¢p¼÷gÜPù\x0011\x001aüÈæýP¼ôV@ÄaÏ0¬¶Sù\x0011\x001aü¨ÅÜ\x0003\x0012¨Qý=ÊvÒ¨ü\x0008
~´ÙÓ³±HìIìÏ8OñwT~\x0016?¢¹ÈIù¨q$\x0014óôen\x0015§ò#´ø\x0011Ê\x001eù\x0013øÙ\x0013b@y<7\x0010.âLÊÅb\x0016u§~Þ)ØpJfÉçiì­8\x001b\x0011ë\x00078¤ø\x001f~ø¯ÿ|ºûþéç»Wÿþø¾ýð1
f»\x0010õ`©]*3uÕ\x0001gê\x0002ÍÓ0\x001f^½zñâî\x0017ßÞ½zøÓÃëöÃ§aÂ\x001e&X`FGé\x000f	\x001d%\x0017\x001dÓ>â3P=Ê`2funµV&ùfÌ,8¯*I,0q\x000f\x0013-0]!lÞ7kZ½|óëÇ\x0003\x000bÎ´Ç\x000c8iwá\x0015Ùó#GõK \x001bÎ«2"\x000bÎ¼ÇMÝq\x0016¹áDÁÙ|\x0008\x0005çÕ¦\x001c\x000bÎ²ÇY,ö¤\x0011×<Ø!U®Æ©>$/8¯û,8ë\x001egµØ3¹û9\x0013Slin0¯\x001e9\x000c0//\x001bu:=¶7wÇûÒÍY¢|ö«ù\x001e\x0016áM\x0014_N¦ñÙ{(_]éÌÏî\x0015Ç{\x000bÉc\x000bdÔ\x000bñ\x0012Ï4p^­\x001a°àT,ï-4ßLÊÖ\x001dâÕ{ñ!\x0015'Y@F\x00052Ù\x0002:É/\x001cÕc\x0012÷Wþ\x0016J¼E&÷1N\x000c\á\}tÂñîªÑ\x0002Tq¼·<¶ÛzfÑl1hÏ4r21¸Cî\x001erv* £_HEÕ7?ýøóß~ºûêÇ÷¿<þëûÿúÏ9Ðø
)búÜ8\x0004ä1FLBÏoÞ|ýí7/ÞÜ}õõëï\x001eþðúÃÁçÀ\x001aöX
kR)>óSG³)/kóiÞI´5î±F\x0013Öè=?Â6¢%ÃôÔÍÅ)¥Ù\x0015~\x001dkÝc­6¬-$ñ½\x0015iR\x001a£µà)PöãêlXû½s;\x0000}\x0018&\x0006\x0019>ê?°Ds\x001d)(¤`Ez_Øª4£60Ø|\x0001{Yq è`·?Û+ó´yÄPiÈw.ißÎ~»½û×Çï\x001fþå§Àýó¿\\x0001þ\x0017+\x001dôIXH+½{qC\x0006\x001dL'a­»Ø¾<©VªW!»ÂAuìi¾F!Û:Í\x001aÈö9â`Faè\x0003\x0007@ÎuB¹\x00192\x0015\x0010)-ë\x0015E\äþ×{÷Ã\x000fOMtý×O¤Pê¥\x0019käHÆgp¯à|\x0016Éç|Ù·iîÛ?Ü\x0000\x0012ö a\x001dds,îÄ$³ªÃh2ve>Ll\x0011dØ\x000cË iv¯lIä²û\x0010<Ø\x0016÷ë®{qÝ-ªJÃÝÝ¨qZº¼\x0010÷\x0008qÝ%ò«Vî'!JÛs3ãôi\x0011dÚLëflPzË`\x0003\x001cxÕ&â5qú¼\x00082ïAæuK¦v]fK\x0016Ç6¡\x0005-\x0002rÞ{§0Î'\x000c	Àº\x0007X×\x0001bf¥ß<¦Om
\x0011\x001c\x000cî¶Y-Yñ2±i#HgrÈß:Ë-Î\x00133Îû¯×Pj\x001a_çq\x001aÊÃÃCJ]\x0015Í³y¼¥ÿ@ÝÀ"JÅãÞ@ä4b»\x000f` ýE|pä\x0007:,×P*"÷\x0016&¯\x0017g=(3Ø]s¬OËzW4î
<<ï4°¯ð¡Y \x0012ØÃTTî
\^ecL\x0008¼< ý,ïÕÝÀå\x001f7¤"roaräÈ2¦\x0016e\x001cHQ:r·fÇ¢@\x0016\x0003\x0005Évû¸­í`·	RlSò´fm
%(¢\x0004\x0003Qö"ô2ó.ûv&y\x0008_CyB\x0000\x0004:4P\x0010\x00150\\x001c§k\x000ebJcT~\x0003ë~S1ñ{aL.PÕo·ä  Î\x0011_ð\x001bP~\x0003\x0006¿	2å4ævìOÙÔpÊG²¦ygì!ãÁq¢#ÖÙPæýÅAX^'×Q\x0006å8Á\x0012alÛÃ7í¦Ý0(;v\x0010M\x0006å8Á¢ÝòÝPºû*¦äÄÃùÍ5J\x0017A\x0017ãEU\x0002IðòµS:ák+Ï	\x0006ÏÉAî\x0005\x0012/Mn\x000cTG¤6ït^AéÇÄ\x0003^ \x0013iÁ\x0015½1ËbvA-ÂÔ\x0001¥!¢¤fñÞ\x0004Ea\x0005\x000f(
Ôÿ:`\x001e\x0016pÿ,¢´%sóÆfMVðv\x0007\x0001ópxîE°ªh$Ð\x0000\x001eÙ\x001e¢ñÍËa\x0005÷Ï¢JKXI\x0003ÂY\x001e©¨·\x001bºÆ\x0005æ´ñm\x0011¦,
¡%ywåè7´P#1Léwlgâpîvô`¸9f)öÚô*i\x0002ô\x000bAú'ajG7ÈOiÑ%òÑ\x001cµs!\x0002/à!Ç\x001d=<»:\x001a\x001c=û\x000bÌ|Iº$\x0014ÓfÜEÚÑ
:IÖ¬qÀ\x0014><>útoë\x001aLÔg\x0013
g³HgsLuË\x000bn0e½¬kñÝá|G}6Ñr6¥ÖkdÚälÆùäÖ5úl¢Ed¡}Y¸U§|ó8z¸R\x001fM´\x001cÍ|ùæ2Ý\x0017ÇY3ëmï&\x001c³S»[/¦ É½æãù6õÉÌY¥X2R\x0017\x0019²'\x001e`Ô`âñoõÉÌéxöKÜºÜ£4åÕ<}õ_©f¶\x001cÍ(ù¬Ü\x0014={aMAy\²²!:_\x001e#5é \x001cS+\x001aÊãÔut
Ñ\x0011e©Å
×$´èH"âZS;Dåç\x0010-
Ô\x001c(r\x0006!pO á\x000bA8 ¨ZÑ¦@r2s\x0018'3\\x0012\x001dÓáI«Wßý¼/¾þy_+ùÂ³¶|G|¯#ßq<Q¨ñ«\x0001léUHe+\x000em¿ì	`×v\x0008aÛâ³ñEù\x0005Õ	A{~|÷óß~üéw}pÙ\x0007¥ÎJ½zª²ï§fä U\x0007ÓQ¦Ü\x0010A«{¾~ùíW_¿ùîå7\x0006
{Ðp\x0000ô¶äifÌÌW'c\x000e{Ìá\x0000æÌe\x0013\x001bæÈ+ÖA\x0016Î\x000b:îAÇ\x0003 Ëþt\x0004^°Î\x0015aþHWÏ*fÜcÆ\x0003+· uCó2°0ê\x0001O5tÚNvÐQÃ\x000eZ\x000c\x001dâo\x0001:ïAç\x0003 e7U\x0007\x0018´¼ 
Ú+?ôvGÄ$^0¹9Ê8ÑäÃ¨#z»'bj\x0017\x001b\x0001Í1ÿ\x0016\x001bz»\x001fRÝU~\x000eg\x000cY9¡·{!fÇoä\x0014ZÈ
ø\x001c\x000bü\x0016¨\x0017z»\x001bR	¿n¨\x000b£®ñ·@]\x0014êr\x00005ãA¨;ãe'¬sQWº\x001e@\x001døy°£U²íTÔ»o\x0014.¹\x0003¨ã ¼=ê¡ã§¢V)ØCSÌ(ÃÕ7Ô¼W\x0012cø-PëÐÔ\x001ebN´~gÈ Æ¼|¤Ãx\x0015µ\x0012E8 ´þ,\PGFÊoZ"ØE1»À%\x0005H=¾ý\x000eF×Oóe\x001cFÔJ\x0018á@Z<?@6Ô\x0013\x0004©q®á##'VA+i\x0004»4ÒVàÀÄ\x0017³,\x0013©^ö´ÂG\x0006P¬¢VÒ\x0008\x0007"Ôfjd
©^\x0006\x0012Fz"h¥`WF\x001a%É#ð\x0002F\x000c\x0012¦ùW#f¥`×Å«Ä1¦Èe©fÙ£æµ\x001e6ÔAéb°ëb¦õ\x001d\x000cÚq±aªí\x0002zÚÉ`\x0004­d1Øe1»<H¦\x0019°©=^ÈÎ£ê d1Øe1·Ð\x001bÊb÷}ÉS\x001d{\x0015S\x0016]\x0018Aë]\x0015iø,·ä´hZöüÔàåÌ7\x001a\x001bQ+U\x000c\x0007T&¥aê*¶\x001eé±ð±Y,«¨*\x0006»*ÒXå\x0003\x0002
ØPÅ\x0019	§[M¨,\x0003²Xd\x0000ÊF!ýé1oBN<!J\x0016]\x0016sÃÖ\x0007Ø"­þ\x001c7%7ØúDÞS²\x0018\x000eÈb\x0001®Û$Æ³¥óÀ<Ý\x0007d\x0004­t1\x001cÐE*óQ¸\x001caÏ{x5<áÈmàÏß?»\x000f|ohr\Ï¥§6UwÉÜ\x000c{ZV|¹ã>Ãì\x000e`\x001e÷®Äµä©\"\x0010®6@öUCnÒ\x000e9U*óÚP»BÃî;j'7Mh^²³fg\x0000tÉ#uã`<eTÉ°c¾\x0017/ öÑé^Uú¼r½øÛ»\x001fîþùÇ\x001f\x001e?
35ãÊM<8)8§R0>\x0011±âLQ^|õòÕ»þúÕÃ\x0007\x001dnÀ=<X\x0017Ç<\x0010B¯IRy\x0004)Ç
º°G\x0017\x0016ÑQ¡ñ\x0006\x000eréÐ\Pã´ m\x0005YÜ#«vK<$~³[¯Ijðæ\x0004Ãá\x001e\x001e.Âó^zå\x0003
\x0010îÆC©Rh§nê\x001c+ðÒ\x001e^Zµ^æE¶ÚzRK~õò\x001e^^×ùD¬×3ð\x0011¥¬7»±¯À«{xu
\x001e-uq|öÚ5Ì¥\x000e/E8\x000bÞh>íç\x0016ñ5ffJñk4#b\x0012×pÓöØ\x0015x\x0017\x00199S°)_wkPÛðÁÅ|Óê+ø\x0014#ûEJÞFÿ2>/û³c»úy±ßt*è
>ÅÉ~S	\è¸­ée01B\x0019övy­àSÌì\x0017©\x0006f\x000b¹xàb\x0018\x001föNYÁ§¨Ù/rs\x000b\x0010ï% ¨<Ð½ï\x0002oºÀa\x0005¢f¿ÈÍ\x001aã8~?oª0ÌwÔ=\x00147ûErNÃ\x0019äWØ|^°\x001aùÍn`+ðW\x0016ÍG{åôÅ\x000e\x000e%üÇë9`«àpøEåHíÊ
þBÍ¹ãsñBÍÇà\x0012\x000eX\x0015\x000e7J9èèU1¼ÆÒ¨×ørÀ¢r$¬R=Eæëo1ÈÈ$tÓ~Ç\x0015x:_\x0014vùäU;zrQFxz\x001a¨w\x0010\x0012\x000eX\x0015\x000e\x000cã®A\x0013äÅ|Òçn¦ZÁ§\x0003\x0016Þi¢xG»\x0016ññ\x0003\x001cÇoÓ^Á§\x0003VcKYùz­BäÂý\x0006nZ)»\x0002NÉ\x0006,ÊFãeÙ\x001eh#\x001f>sLû.Wð)ÙUÙ\x0008xFP\x0010zÐGiôa¾Ì\x000cJ6`Q6\x0012&Éfùø\x0006\x000e|Ó*¶\x0015|J9`U9 Êræ{P\x001aðïhT\x0010tEéhÿºØ/ßCeç\x0018ð\x000e\x0006\x0005A	GX\x0015F'Cw£0\x000bqËY!}PÊ\x0011Vc,jø
w¦ÆG.ÍM[DVðé4ÐªrÐ~x\x0018ÌÜ\x00131\x0004g)[PÊ\x0011V\x0003FaÄ\x0007\x001a»ùüaxJ8Â¢p`¹\x001c\x001b¹pH\x001fÀ&lAiGXÕÆÈE_½gß~¾z0,
J:Â¢t mQ¾ps¯0¦.É\x00115\x001fM\x0018\x0004¥\x001daU;\x0012µöM©»Þ4¼£\x001ee?¥\x001daQ;¨j8Á.}AiË¥hºsk\x0001^TÒ\x0011\x0017¥\x0003[ØÌu´¶§\x000bZ ¤Z§´#.jÇ®\x0000q\x0017\x0019@Åa¾éT¯\x0015|J;â¢vP1ªDÍ\x0010xIÃ\x0007oÞÂµOiG\Ô\x000eÄÂã\x0004·Ó'ør\x001cé´e|\x0005"ç¸JÎ4Ù<\x000fòë\x001bé"mÊ\x0014|\x0007É%*nÜyiû¼Èîù.îq4\x0016\x00159ÇUråri«Ü)\x001caH/-\x00049\x0006Oqs\äfláäê!sÑs\x0004ÂH¡ÁAnFÅ.¸Ê.!d)Õ\x0019õÈve
í8\x0008O9/®:/5\x0006´±ùâNÚ\x000e\x000bêg¶UçÒ÷\x001f6xß Û×½D\x0006Óh+ðsàªsÐ'MCÚ82\x0000Èé,mC\x0015\x0019àjdÐ\x0002¿Zvð­
|\x0019Þq4£w¤Eïu{^ëø¢Äõ¾2´í(>å\x001eiÑ=bÉãÒÁÙH_oøÃÉf·ëE§@éE¾9©ý8ÞÝók[¸xð´\x000fyIß£i\x0019%Æ(¡aÌf¢ÔßøÒÓ¹\x0018KWÆôëÆlW\x0011_ÆëG·Õ E\x0011õèUÉ+e\x001dæoû\x0008â®M¹\x000c&	kSv¡W ÄêÇ3Òá§ç aÝyR­÷PFÚMÞ2c¾¼\x001c}\x0010¹B¹nKz\x0017á"ô¢89XË8W\x000bÁÖ_¹ò¬þ~!õWßÿz÷ùãßßýòøîýÓÝ\x0017ïÿÏ\x001fýÔ5/Ê»f»2ë\x0004'NÊÓHì·w?|óò»¯Û\x001f\x001e^ùõÛ\x000f\x001au\x0000\x000e{ÀÁ
ûÇÛ\x0005&\x001aö;ó¨¯ÏÓò'\x0013ZÜ£E+Z¼O}[*Ó«ÔiÌÙhx.0\x0001Î{ÀÙ
8:\x000eÝ^SðeòH*ÓâR\x0013ÞºÇ[­x,%Ù/\x0013G¬\x0014F\x0011o^Ä,½v8³Çµèwô×\x0005G*Û\x001d="g\x001d	¯<Î[]®±¾ô \x001d>üÄv÷R9Íë¼ò:ou»H¬Ö\x0001Ó\x0005\x00048\x0006ôRo\Nó:¯¼Î[Ý.fT>BàªÿèS\x0012Äu:sÎXù·:^(ùÞSÌù£v±\x0018\x001bÓ¦E	6\x0013ïgÿ°E×-Ý"\x001cad\x001aWÄF\x0014÷«Ót+À#F=\x0007~A
ýù¿=ýíÝ{Âü§wO¿þGCþþñO\x0004\x0011-\x0002ï&Õy<R$\x001eí\x0008Í9_õ?ÿc\x000b!^\x0013â?½|ñö\x001aî×\x000f¯>
\x0016ö`Á\x00066Ô^ÃhÙ\x000b»]Hüb\x0001\x0014l5ì±\x0006\x001bÖvsík!\x001a¬$õ\x0006\x0010ÃçÑ\x0011lÜ&°ÔìVýÅ²\x001cð&/§à*ÙmÄZ÷Xëï\x0012+@x¶È\x001b\x001fS¶\x001eßß}öø÷_ÞýüËÓÝ\x001f~zúõ}|"X¤}üpØ¶¾ö-î\x0010{ùR\x0013¹\x0018¦m\x001e/\x001e^ß}öðÍw/¿ýîÅÝ\x001fÞ¼xûÏ\x001f\x0019\x000c&a\x000f\x0019¬k\x0008\x001cAÐj/.Ä\x0006¨½" Ï\x001b6MÃ\x001er0CvU\x0005Òæng¡?U\x0013d6- Ç=äh\x001c\x0003ß\x0002í®ìS,!ô-ïø\x001fìq\x0018Í©HAùEÒ8 8í\x0011'3bzå)\x001dquå\x0010x
AC~Ú­d÷³Ýùd	EìxÍUs>/|1\x001b°A.{ÈÅ\x000c9\x0001\x000f\x0010io\x001cí\x000f½Â iû®	rÝC®G/±óÕ@zÒ¯w\x0012äÓHù²Õ|Ó\x0011g\x0003k\x0013½\x000enc\x0014VÆù@>\x0013f­}fñ#ÿëå\x001dsWàëð¿é"\x0003\x001bf%~Þ®~í\x0008÷do@·MkÙ0§,§ù\x0003ý¯&ÌJý¼]þh¸
i\x000ei\x0018bÓU\x000c6ÌJþ¼Uÿ°©R\x001fu\x0012(Õ&f.½ßÌ|^áþy»\x0000fÏíhxqA\x0018§\x00056ÌJ\x0001½U\x0002·êø
055qQ%*ÊÓW \x001b^%Þ®ÅqX³qàajE\x0015ýKÓ&E\x001bf¥Þ*è¶
G\x001bäöS¿òCt#øÌÓæ\x0018\x001bd¥Þ*íXHm,­<âú¦v2p`Ï²`\x0006¥`UÀfæDµ\x0008\x001dsåáYÍÎã8óÔ\x0004\x0002U\x0001éU\x0019ãZYÄ¤äóÌ¬oV\x0001l^çäú¡ôq=\x0010}\x0014È´Hû,ÈJÿÀªÛÉà8Öª÷l!È\x0014{Â<­\x0015µaVú\x0007vý\x000bë[i\x0013'½7v;\x0017\x000eA«Ï3aV\x0002\x0008V\x0001lv®r9¡
°¾\x000f±a\x000e\x0002y>§Ç\x0004Yé\x001fØõ/:îÉ\x000f\x001c
GÚ Câ°¹úùì\x0018\x0013f¥`Õ@êÈ\x001asä©®è*È\x001aJ\x0003Á®±Ø(où£ÍÎAÌL\x0006?\x000b²Ò@°k`ØJ\x0003ûÑH<á¼\x001d
	5Úû´«vP\x001a\x0018ì\x001ag1\x0006,À\x001bì Æ9çAi`°k £!K\x0011ÚÑ,Liµ¨
³\x0012Á`\x0017ÁÆ\x0015¬U¦d\x0001y&CpÚq\x000e:\x0005j\x0017ÁXÿæÞ6I³ã6\x0017ÜJmàV$\x0012ù\x0019úÕ"KT{MNó#®æ£-¶lÆPMOT\ß_Þw0³»\x0013¯d\x0012'|\x000fê®®D\x001eß­°»Ë\x0012ý\x0014N\x0002\x000f\x0012	<`\x0005\x0003¤5ó\x0011Ä\x0003%j|D=ÒY ÚI0E~~jv®R \x000bT\x0016`;ª\x001aØ0+\x0012D;	6\x0017¬|©ªú×º\x000bb\x0014Ì§-\x00016Ì\x0005ÑÎÙItNÔÁÆdã´\x000bÇ\x0006Y ÚI0VV!Û\x0006 ls#Èî:3+\x0012D;	fé;G\x001a>\x001cÔ»j:}µ¶aV,v\x0016l.è\x0019³+¬)J.8NÆe\x001e\x0018\x0014	\x0006;	\x0016Q½GzfE&ÄÌù´AØY`°`\x001euýDãlñ±\x0007~DxÑY`°`É÷£\x0006z)\x001fÑ"b±óé
³bÁ`gÁ<Þ[i)íÍ\x0005ÅÎùº÷Ö _\x0002í,X#=ôlLûøPGRwÞcÃ¬X0ØY°ù Öq68wÎñv4.Ëb`gzï!n+w8jðÝ\x0006¹äë¬¬s°\x0007ç:ÖRÈÜ/Ù0\x000f\x0012¬x\x0007F\x0015é¢=ÒQ"Ç£*y¨Y¢s½îöªúæ¥+½[\x0014:ñÔ\x0004R·§¤£R|>mDB\x001e"GÍ[LßZaÞÝ}ÿîý¯?ßýáí\x001fßÿü$^º¡r\x000bxJ)r±¼`å97©¨4Ã<Ü}ÿðúÛ¯îþðâÍË×_}\x001a®ßÃõ6¸´\x001e±?Ç§\x0004²î¸ ôÆùtÔ0³ÂÅ=\´Z\x0017y\x0006¸\x0019×qëNAnK¥aÌu\x001aÍ¢
{´ÁhÜ\x001c\x0004-]YÑ\x0006\x001bð)\x001f¤`¬pã\x001en´\x001a\x0017HQb3.)ìx6n£ë\x000f£?V¸i\x000f7\x0019­ëý}áÞCÚ{¾GñùÖ'yØBi÷p³Ñº\x000e¥I2dÇ!s\x0013¸Ïî*G+{´Åh\\x0014k~Xh¤øÂû\x0011}»ÿ=ÓÓN'Z\x0006ÖºÇZXkæ6nXQ\x0006Ç[\x000c;\K¦\x001d#!\x0011¯Ûv¦\x0012Þ\x0000\x001f=Å°\x0017E\x0004Ðdfd³Ò\x00108yê¢î¦õ(\x0011ì@¿V¼ÍÀHg"lácë8[(~´øÆzPg²âUt\x0006F>+íjÄ³´6®2A°\x000fµO_Äg ø\x000c¬æDÃN.kµÃ+\x0016ªîV¼ÐÀÈh%yÖûOônB·¯ç-\x0016>ùËì«\x0018
«h8¤ÓðìX;¾bßP\x000f{¿¬x\x0015¥ÓZjÀ£XFBzÕ§ °Â±Oî£\x001dõ³x\x0015©Õ2\x0019µ\x0007¤±Wèöe	úvW>LZá*^\x0003+±aåÚe»ibKñlø\x000fí½F¼^\x00117\x0012[¦¼¦\x001f\x0007OÏ\x001d\x001d/ÄÂ)\x000eÖCÏ\x0015¯b7oe7\x0012"éùy\x0008En\x0013¾È]-C¡ÕWßÕ¬ì=?'%ô·ð\x000b<ßÒó¢Wäæ­äæBWLX\x001d\x0017\x001d\x001aY°"M\x000bf±++\E\x0016ÞH\x0016¹]Ñú¢ø\x0016\x001cÜ½Ä^Ç!\x001c·ÓYáªØë±7ÓPEçb$Í\x0006NuP¬\x001b\x000fë8­pUèõÖÐ\x001b o°H´ý£÷|\x0014È,;êÃQþÇ
W^o\x000c½¹%fåæjÂû<\í¢L\x0007UèEkè%òn_¶>ÂÍ¾"_äÛ/:½¨B/ZCoàÇüä¥å^ádn\x0010ë¡ÓÊ
WE^4F^ªç{§Öhf6'\x0013nxYá	uÌ\x0018z³LC·ÓP¥ãY\x001c¥\x001dô¸¬nE«®\x0015h¼V´k»Ü2¡op#¸®89¼î¢P(ÐJ\x0014¢uÕÎ®h!\x0015Úã'g÷²,r¯"%\x0007ú-Ù)ÜöB\x0011}8JväîV\x000ej4æ«ü?þÚVí®óô¿ßb?\x0018Ú
kKgha#I
¢JÒ~Õ\x001d®ýÏG¨Û¿¬¨Û¿H
fóAê\x0000b\x001fLÓ\x001f_áª\x000c\x0007Ø`?Õ=±N}Á(·exnÝï\uÇûGª;Þ\x000fÕ\x0017ïßþúóOïîþðáíû??ýI°\x0019kËú0^\x000cWd5B9í3xñúÅ·_½z¸ûÃ\x0017¯?ûøëÕé÷0½\x0001&ÊUéøö\x0016I~G`jsÏÂÄ=L´À\x0004ÑXªtf3Ãd	qïÊé\x0004Í,Ì¸\x0019-0+7=ÄÚü©¯l\x0017J¹[ºz:\x00191\x000b3ía&\x0003Ì0\x0007kcá¾B«Ád²\x0006ót\x0015Å,Ì¼-0(O×²eº\x001bÌ"Ï\x0000§Í³0Ë\x001ef±Áì\x001dEÍ¬ßM(ÙàNÑfQÖ=Êj@\x0019£lo©uÓ§Û`V>Í\x0017ÌñTÒ£¦³ÀLT4èß<°Y%a\x00018í«Å©£»%¼'ä\x001a¾k°Ò­Is\x0019\x000c36EÎÂTÑ\x001d,á=MôÕûÓHÃ	i|ö\x000bÂ;¨ð\x000eøD¦:9\x001fY¥%n\x0002²\x001dçù\x001aøYAá\x000c6ýx¶ï.½Kqèï8ñ´§f\x0016§
ð`ðY"|¢¡H`{òÒôv<\x000fwA\x000bL\x00159Á\x0010:\x0013\x00150úõÄÑS\x0018ÃL(Zïqz\x0015¼%*57bo"u\x0013Åç\x0013³\x0018UDòÔîL½Ý+QËv\x0010\x0001Q\½6/ÎâÔ	§)$yÎ\x001aNäcÛ~Åö<]Ç1S$o	IÎsöhÒ 0¯Ó*^Æy:\x0018?S$o	I8ZL\x001c©Ë1c¦$Ì^/`"¯2coHIt©·ô%Q(8\x00147:¾z[pªÓ\x001bÎ@£\x0003\x001c¼H8´¼~¤sç"*³8Uèô¬ú"ù«§\x001bË}\x0008NÇufAªÓ\x001bÎÐè²è$\x001aÀæ4	å\x0001ç\x0002V0Qw´w':ûÉ¥ÌO-tTÊ\x0005Ù\x0007ª\x0010\x0010\x001fh\x001bE\x0019Ùcsæuâ\x0015´ú²n\x0008! ¬b¬Ô¦ÕC<Ê\x000eäuj/ÎâTY\x0012\x001a²¤@\x0003²»Äö¬¾tE¯{]Kv%éó¦Àµöù³$uXäý\x0004Î!§\x0019þ\x0000×àÒ½Øsjïåb\x001c$W.§Kó¦	ô\x00007ØàúpÊ\FÊL±%¤\x000eÙÌÞãá1\0¢\x0005f}ên»çÛ<ï#ô-^p0jáy¤¼V^üðãûîÕþ'+ý\x0010Â@\x000bï{Å\x000eHx»ãÉ­ÿÍË×_<¼ù4@¿\x0007è§\x0001RæT;Â(ÃÅ-LÅ"\x0010O\x000fè\x001cÄ°\x0018æ!n³A,Ý\x0011·öt\x0008þP \x0018÷\x0010£å3o\x00071Tzµa!°8'F-0í\x0011&\x0011û;n3b\x0016\x000bXð	IçâË{|yÞ[ÛÔfB\x0004~[C¢\x0016 ]\x0000±ì!y\x0013Ênê@ÝÁ(çÐ³\x000c4à¡}\x001ebÝC¬\x0016+z¶b@ÞöÓ¬(bàí¾¶ì*;
Áä\x001ei\x0008>Ï\x0016SwgòÚRiÎrºw\x000e#*h±#°\x001d³Ì¯\x001dÙ¡ýùï9**!,:ñèêÝ½\x0004SÖ\x0017@|bþ¹\x0018UX\x0004C\µÍ·Í7;º"v<-½ÎaT\x0011æ#£¯¼ÿlÓ;\x0005¶#ÏöSäyBcê¹\x0018Upùè\x0008õ¾GZ®\x0015\x001bDLr\x001cáÜçBTÁ\x0011\x000cÑÑñ\x000cn d¬Ñq\x00143>¥ï÷\*:!<úA2$\x001a<c\x0010;Þ\x001d§0z\x0015\x001eý|xô\x0005jZ\x0008\x0017-J:¼¤\x0006Ê\x0013R\x0013ÏÅ¨ZoÈjå0bû(<êÙÎc\x0015;ú²ì2^çµómØvæt;.CÄ,+!?1ùË\x0018O»#\x0006@Å1ÞÀ1 Û\ZòD3glD¶!®ç^Q§\x00181`\x0016UÆv\x0010Ó À\x000fÕ?\x0017
ÝÞ\x0010º¥ÜO}«·¤QÖËøó½Âs\x0018UèöÄ\x0016zèT¯`#¢¬7ôá	9êç"TÛÏGnêÒáÈÍ¯OíêGH\we\x0015¶ý|Ø\x0006	Ñ
ªDEÄõ\x0011UØFCØ|9hÞ,;é
(G\x0011ã}.F\x0015¶q>lÓòã¾.ÒÅÄ­Òd\x0019c>4úÏcTQ\x0011ç£bs\x0012^\x0004O¯¡RÞEî1\x0005_O\x001fÁç0ª¬\x0016ç³ZÒ\x000bè­C®¿èt²ï\x001aÝaþz\x001e£
;hÈ\x0018lõu\x0015xèºa*\x0018O×æÎaT~\x0006¿N²qÓÑUIkå&°y\x0007å×Áà× ½Ð¼:ÆÌ©w\x000båË>\x0013_\x0007_
Óà<k>\x001d½Øñ	i¤çbTéXOÇZ\x000cïZ\x0011º
ª=\x0018Ð|.F\x0015{!ö$â£­Èã&<ë\x0000èã²_\x0007]\x000bOÉ ñ¸K\x0004A\x0015¿\x001b5)X,cTñ1\x0018âcä§ÝVxwì§Å§DA\x000bPåa>oÈ÷ÀH-ßñ\x0011Â£8É<B\x0015¾!|;¹a5<£æíÆ§6¯<\x0017£Ê\x001bÃ|Þ\x00082\x0017¡:i\B_\x0004ã\x0013ª[Ï¨\x0018&\x0018\x0018\x0006d\x000b1D7\x001e7ý:¤ç°1*ó\x000cC½ÝÞÅÁ0^6È·ßa9zGÅ0ÑÀ0²\x0008¡Ù±²` -l¨×³Û¨\x0018&Î3Lô<Å\x001a})Ô¿Ò/üÜ\x000e\x0002¡¬×¾£bh`\x0018GÃË=ðÛ·§,Ì­ó\x0018õSÖ|ôvN\x0016NCÆq©Áç[f_8*zÇùèÝ¼¤÷É6ËyÿC{\x0001\x001aìe*~ÇùøÝò\x0007q\x0018\x0012\x001aãïìbê\x0013\x0002Ï¨Âw\x000fß.ÊdAK\x001fÆû\x0001ÈËo<^ÍcTñ;ÎÇoWøé·ÅÆ2jduÄZlË:©øæã·\x000bÒ^\x0004*\x001dÙ_âaêm\x001e¢
ßi>|»Â\x001bÆ¢§û\x001cG\x001e3¥åãTøNóá»s²æ3\x0003#H½1^P)K*|§ùðíD6#z\x001cól²~;àú[R×4=hVdÁXî%vK\x0015*>%aþ\__2o]÷\x0001è\x0005³Cd=\x0004jXÿÎºWÂÀ0ÈË\x0018óFV¯o\x0018¥\x0008\x0015O»³ç *I\x0006Iü\x001e}Ël¥:\x000f|·lhý0*I\x0006AÙ¥Þ\x0012ÄqÍ\x0002¹hÅt\x0018oÇ¨\x0018&\x0019\x0018&ñÌr³c\x001d5Qà\x000e÷\x0016~Ö[´²bl`\x0018¸XLT"xIxòú·Îb²b"o=¤k!Í1\x0010bòzÿNV\x0014
\x0014ã¥%\x0017I\x0008@0JQÌOÈË?\x0017£¢l \x0018ÙÄÔn1é^¢£xuYÏ\x001b³¢l \x0018_8ß©ñæ1bÄrÁaT\x0014
\x0014\x0013Hhg3bu¼¬8®ec²âlà\x0018O'°±ê	ä;%-O²îÉ3´A5;ÊF\x0014
à|]
ç£Üs\x0018\x0015Éd\x0003ÉÀ}éß:]\x0006
£\\x0011;ãÃ¨H&\x001bHÆKñ\x001bÛÅp\\x0011ä:Hk\V1\x0016\x0015À!Ä\x001a9Ê¨Ú<\x0018EXx+*\x0017C\x0000Ï]J+\x0006_îAxPÞb\x0012<±jã9¢w1\x0004o¸Ô'\x0000Gl'6¿?×*6\x0016Cl\x0004\x001cj\x0018ã(Iu'OMÍATa§\x0018ÂÎ\x0018D\x001cW\x0004\x0019naüu¼ÏÅ¨\º\x0018\Ú
wéÚ\x0007qÜ´Ö\x000bôU¹tvi¬E?[¾FØq·|gý}µ*©Ó.5É·¦âhå
ªm¬ëßº*©Ó.CiN¸\x0013yñEÃ(íóé(·cÀ¨GtzyÄó zù\x0006'7}Î¼\x0006uýõ­<\x001a\x001eï¹xî#\x001c×Í ÌñK¦ÔHËzç;@5!¥}CÀÿ%\x001c÷\x0003(\x000b­zsª\x00161*´~¯ÏöÙÛßþÇ\x0000¡\x0006)ROÞVÛûÒ®×K\x001eÖ\x000cÝä >{ñÝÿ\x000c@Ã=4æ¼Ê\x0004\x0012\x0006Ê\x000cMÊ=±\x001c\x000eä#l´\ØÃ\x000bóË\x001c~bîKd\x001b¼(Íß$a´\x0008/îáÅ9x4gÂõï@ä\x000fÛÎ¡TP\x000e\x000bÈ§¾lÚcK¦s¢8ORY}V°a\x000b¼¤%Þ\x001f× {åÊ\x001e]´\x001c­\x000bë©\x0018B$¶Ï\x0012\x0008Ã¡e~\x0016^ÝÃ«³ðÆûPHÐ§­éÃJE>>µ}æYð@\x0005\x0014(% u3\x001fö[/´)Í7¶Y|*ªÀdX)ÉIô×·V\x001dÂ'7ü\x0014\x0010ÜÞðýùí\x000foùõÃÇñ©Ó\x0007³Ç/xºlø|\x000f*!\x000b¶x¨>LÚî&æ²ÃFZûÜ[BJS[Y¶Á\x0003éINåm7ÏÃ§Élòìå\x001c¸}¨}ÛþÈâiÓ\x001c½\x0011:z~öèa\x0014kþïq/$\x0019öüôÑû$>Åh~Ò\ãV©ÄRÙDÎh\x0013gûÕü>öóð)JóÖ.\x001dÒï²-Aï¡t;äø\x001d\x00063¦CË~¾ÃÖÙ|^\x0011/éý\x001ca`|æO$U$ô\x0018fGÙ®&ü\x000c\x00142ô¶Jâ\x0011V\x0017i$üquæ'AúâAºdóä\x0017{×þ]w?üv÷åÛ\x000fïþü/oºûß~|ÿ$ÌR[8nd\x000fÜ1½«2e\x0010óã¢ñï\x001f^·$úóïî¾|ñæá³?¾xu÷\x000fß½|ýIÀ·ù«
°³!nîRe.¾FÛÈ\x0008>xÊN.\x0002\\x0014àb\x0005ÜPV\x001ec$rdÄQF½;¼«Z\x0011ßúç	1E\x0013\x0013b\x001aGèÛPZ·\x000b`Î×µÿÐ¡ZfF\x0014âdDL/[Uä\x001c\x0002·ÌääÇúQæÒ8+ÄÙlãÄ×¯[¨ØÒ`²±;¼Ê\x0001«cÖcì\x001beuv
\x00053\x0016æÂþ®\x001ejVVÄAE`\x0014è`T\x0007P\x001aWr\x0012Í\x0014p¥^åxA\x0005ã`Æ\x0015i1M§8G9\x0014Ç\x0011S3â \x0010\x0007+bôC¥\x0004\x0002\x000fîæTAl\x000f)«\x0019±
\x0015Á\x001a*h3IWulÁ­ÐéæxN.(.\x001d$éÌç\x0005«çal÷¼2ÂqéÁ-·|[\x0010\x001f\x0004«¬£ò¼hö<Z\x0004#Á
xkÎ,JÙbÛ¡óÎ\x000cX9^´:^\x0000¹\x0015\x0007r.\x0006µ¨\x0019båxÑêxTur=Td§ÍÌ\x001f¥
âÃæ%3båxÑêxô2\x0018\x0005qT³8©_\x0016Ú¢r»hu»@,×áÆJÏ\x000c\x001b\Z'ØáÒÊ¾k\x0000'åuÉêu!D\x0016$¥j^§Ñ\x0010WQò\x0007¡\x00073båvÉìvU¦@B¾1t¡\x0006Ø\x001dúÐÌÛ%«ÛÅStQ¾éÅ©gA¥²]­×
åvÉêv±\åSá=Ïæêø"Ú\x0010\x001fÞæ­³:ÇÙzIÏ¸Ó]"-nâÊ\x0017<WÓaêÆWâl=Å1»{ìö«îwµ\x0004±p8Ì2\x0011£BVÄ%J\x000ebå+iqüÀçê±l\x0006¬Ü.Ý¤ZùLÐZD`\x0013s·«þ0BdF¬îwÙz¿K\x0018Ç¡ "éû®¶T­#>ÎÂ|\x000cñygL\x000bNù\x001cýÕX¥pcC`uì«\x0013tX«<kaô¨\x0011é\x0007"øÕo\x001f~úñí\x0004éE¦÷v\x0004êYåÊÓnîd{=½÷~õÝW/_|öi`¸\x0007SÀ
÷\x0005[â©Ðà¸Ìe8í#\x0013`\x001f{ò\x0018ÀÂ\x001eX\x0002½1+l½;Ü÷Ty"Ë¥rª\x0007ôlÅ=®8+&\x001e|Ùº%I\x0019\x000b°³Îg\x0003K{`iÊ`YÊ\x001cÔ\x00071¾$«-7;U×y6°¼\x0007gµ{I_2Ôò¼ 
$Z ;0<8è\x001eØi\x0010\x0019¨Ê\x001eUAUH/4\x001az\x0003ð\x001a-h:kky¶¹ê\x001eX\x0002æ¹5(\x0010FÖË¥\x001eº+\x001dÊÄ3¸ÔâK¤\x0016	,Ü÷\x0010Öþ,êÓA*®eî+\x0007ìéÀ`
ØVÜµ¼Üó§\x001c!,\x001f\x0016©O\x0001SA\x001f¦¢~õ¬á\x001aj\x001dJÍ"¬Ðê=\x001b
ú0\x0015õ©$ÚÓ¨¸éÌúý\x000e\x0006WÎw+=\x0017WgÌO1²Sb`èuñU»ÅCóÌ\x00142Mà3ß2Ò\x000c³L\x0000±q@\x001a6[cðÝË\x001d³¸´=ÈY§U\x0013¹\x0016\x0012_x/ÌâCñh_\x0013Çº<Í4Þ<Õ$x~\{×{NøD\x001e4£¿\x0005\x0011vp´aeí\x0003ß\x0016yò\x0007¦\x001fL\x0018P\x0004;\x0003\x0006NËiÑÇHÔNU>\x0005¯¥ÌZ~0\x00163~øëÛ÷?Ü½yûoïßþöÃðÚ­¡Þ³kÖ#t\x0004nÈ7\x001e\x0016¢nÊéo¾|ñúó»7/þôúÅw\x001a¤ßô\x0016I¢\x0002rÑ¿Á\x0014µN\x0008p*õ?	\x0013÷0Ñ\x0000ö"Â_à.ë\x0006Szô<jÌÂ\x000c{Á\x0002\x0013I-h³f\x0015º\x0006S\x001eÖ¨áö\x0002q\x000f3Z`J¯mt$Â\x001c\x0019æºýÈR¹Ii\x000f3Y`&Þ)Ü>ºhÒ\x0007\x0017äAê#r³0ó\x001ef¶}tÞÅI×m`ôÌÀÖ<_Õ6	³îaV\x000bÌ¡$Ô\x000e$_¸él\x000eÇ+\x0002\x0012è¨i	)Þ3ÌÀ³íßj\x0017WÄ#Pa\x0013,q3ãPlß¿r@\x001a
Â>ê£ÌâTq\x0013L3É6NZ.\x0016ÅCd=V
fqªÀ	ÈI	\x0006\x0007ø¸*\x0018ÆK®/§=³0UD\x0002KH*À\x0002Ü\x0011h\x0018}=\x0013áG¶NâT!	L1©\x000c5×,\x000bÚg\x001fÂÇåTÍu\x0016§I`	Jy¬
uû\x0014	çP~<¤éULòD\x0005\x001bYn0Ë\x0010#=ßÛ5Sy»7yû9kÿ{\x0014&\x001a\x001aå\x0019y>Í0æ¾çØ+4\x0003µqcÖ,Èrûa\x0013ê'´+R%ÿ\x0018®·¡Ãè¶9\x0005%\x001fû4½\x0013h¡}\x0017uå \x001fÐãÅO?ý¯ÿ÷ÝÝ\x000fï~¹ûìß~ýñw¿<\x0005³ñzÈÜ¬\x001d-äíA\x00158\x0015ÁùW¯\x001e\x001eî>øæî³?}ûòo>
ÒïAz\x0003HÚBS;ÈX¸3ª\x0014©\x0017Ó\x0008êá¥x\x001e%îQ¢\x0001e®\x001c2­êëéR©ß.)\x000fÄi@\x0019ö(åG®ql(û|_ûà|/j(Í.ó(ã\x001eeGIãÐbÊÈc¼¥\x0016\x001c§ò0~j\x0000ö \x0001$\x0000ÇÎ²ðÝ­ÔÊ­Y
å\x0015Ç2ïQf\x0003J\x000fTé\x0010\x000fï\x0017azñ\x001bÇò°ÈØ²ìQ\x0016\x0003Ê\x0000¬\x001eØQúR\x0004Æ¯Cu\x000f²\x001a@ÒGCpÙq¡c\x0013ì4Èñ¸Ð#º3 lnÍß»åï½ü[ÇÛsCyx,\x0007©iÇÀ;!gúÈ\x001bÊÆ©ÌÆµôè0Nd©\x0007\x000cÌCEþ 0E½´ºê\x0005f=hÊ\x001b`*æ\x0001\x0003õPÉ¿K7³\x0008&È¸~³f¸à£+ê\x0001\x0003÷´\x0014\x000f6kvQ
ÀýS'â÷\x0006zÀÀ=ô4!)\x0011 "À((Úc\x00130\x0003$¸Q¹\x0014ö³Z?ýç¿ÿÇÃ¿¾ûð·\x001fo÷´\x0006ãöÙI=3\x000eê«ÛB
GáÛÑ«»¯\x001fÞ|ÿò!ø\x0015÷XÑ5Â]GH¥¹þ]1÷°Ô°&|üñm`Ã\x001el0\x001a¶%
Û\x0012Î¾\x0008&c|\x0007K¬z	Ø¸\x0007\x001bÍ2¹t^{!¤bß¶³\x0019öã3XÓ\x001ek²b
ü@´ë\x0004{ jw¥aØCUÞ\x00066ïÁf\x001bØX3ïGÚi]¶·çêS!Ë>1Æ7\x0003¶ìÁ\x0016#X¬¿\x001e
|ìO«õåÙ°Ö=ÖjÃJ\x001d\x0006±R¢Ï<(q+\x001eXÕ\x0004öKmAÖ\x0019ÑfÝ,Y«·Qm¦½äÌ¦\x0004#'ÐæàÎ^H­¤\x0013ã{6´^¡õV´\x0013¶öÚ}\x0003{]ùØ\x0015v\x000fÇL\x000cô\x0003\x00137¸È\x001a\x0007èÐñÚ«5§åC=¹\x0004ýL?×ä/Þýüá)ùéÝ_ß½ÿó»·¿=YÊH¹\x000c+Ûcå¦HûÍ¹¾\x0017Oeø¾xøêÍ\x0017Í¼zøòáõg\x000f/¾û4\¿ëpIñ×¨<6z\x001f\x0007Ü³WF\x000bZÜ£E«qáwçDiK¤ñË`Óé.'\x000bÚ°G\x001b¬hëØ®\x0012«,Ýð^fN\x001bÜ«BÜÃöËO¹\x0008\x001fzÈ²#¤ö
Yà¦=Üd·.+\x0016Ñî\x001aÖ»lÖ\x001d+$N\x0014Yàæ=Ül·®ì}Ê²ÿ°\x0019W^'Ê©¨\x0005mÙ£-vã¦ÛY¸\x0019wh]\x0004¶îÁV»i+-þvpEÇ\x0005\x000fsÇF´·ìf#\x0008g·-?KC\x001e»Ov\x0007·*ýYðjB[`4YÁÔÒÈ\x0011u¼XÕÓ\x001e.\x000b^Åh`¥4²¯¬\x001cÉüv±·o=ÝaÁ«8
Ì¤6Ô)¡ûbß\x000e7kâZà*R\x0005Vcñp¨(Í®7ó\x0006
ï×àU¬\x0006fZòé]åq±Ýñ
ç-¦\x0016¼Ö`×$Õã\x001bú%V¼×ÀLlÀe¦èq[ºÑí{Û\x0006r:(aÁ«
\x0016¨m¬\x0019\x001bû°}Çy8]Æ`Á«È
Ìì6ºh1\x0003}à§ëå\x000cx½¢7¿@o,dë½gÁöGÙ\x0019\x0012üi×\x0005¯¢7o¦7\x001cxS\x0018YúmaC:T\x001e­xõmÞã/²ä´ÙWöÆà©ø·\x0005¯¢7o¦7\x0014\x0005EO©d\x0012ûØ÷²ó«øÍ/ð\x001bïï@Ïº;d^{¾ÜÈ\x0002WÑ7Ó-Bt­(r%\x0016¶ÈWÝ+¼b7of·2Öõ +ônB¢ÃQÔW±7³ÅVÎÈÝB\x0016IpÐEx\x0015»ù\x0005v\x000b¼ñ#\x0004+ÞGpºüÑW±7³\x001bp7þ¶¡\x0004âãì¡®¢1àEÅnhf·2kÌ2%t~å</\x0016³àUìfv\x0003Yë´áý
¼\x0008'\x001f¬x\x0015»¡Ý
?ª´l\x0007e­s3ïXçuÚrhÁ«\x000bfvs,PBë`nµ±-Ä«ð*vC3»\x0015Ù¶ã»\x001fÇW¸øtY\x0005­"7´\x001b2ÔöG±®\x001b\x001bN¯º\x000b¡b74³[±>Å.9KæI­§ +^Ånhe·fT.ùnU\x0008y¬pcOËi3²\x0005¯b74³[e#>û{¹ZÈàIÈWL+\Enh%7¹à¸ñ2\x001fÝþÃ\x0013±\x0011oPä\x0016Ìä¨ü4I9\x000e5]L\x0006EnÁLni\x0004³\x001adz¸ápvì\x0015³âUä\x0016ÌäÇN»fßà\x001fs=\x0015\x000b^EnÁJn¤È!«h\x0003MWôó+Ñ7\UH
ú¹ÍÊm\x0008òéç\x001e"zË\x001c¹úé
Ë\x0013¼§ã\x0015\x0003¬¢¶`¾·©²Y©Ç²ÙU±AQ[0SÛ\x0010Ø&iÚQ\x001a{VÏ×ôYð*ª\x0008fª¬Òb*ïË¾õªT'(®\x0008f®H²(\x0006®¤¬>fm¶%6à+¢+\x0002+K´E¼Q\x001c«ü®ºÈGÅ\x0015ÑÊ\x0015ÔOÆ»ÔÚù~\x001e`\x0008xÆ|ºeÉWqE4sE½-´*q\x0014vd»*öFE\x0015q*øÞFB\x0019áº±p»\UU+¢ù\x001ec%\£*)ö=_efÁ«{3Ì7!\x001cûÌHü6ûÕÇåªW¨è"é\x0002GÝ¡1]~Tô§\x0013â\x0016´ê\x001e\x0014Í÷ w/ÆM²­Å\x0006A[Û³õdâ\x0010\x0015±E3±¡¬¢Ë<ÈÉ
rrýU
fQ\x0011[´\x0012\x001bï¤ðÆ
¨yì¥½ÊÓ"¶d&6/\x001a\x000cñVÑÁqi;Æ·àUDÌDáå}\x0005C¥4HÌxñª;|R7#/È%Ôw\x0010ÛXÆyY\x00055é63s$sr)ÆTû²­Â'ÎAØ
Wd
\x000f0\x0016ªfg\x0014¢;|<n\x00080âÍÊÝ²ÕÝ`¨ PâÀ;%½\x001byY¹*ïÍÊÝ²ÕÝ\x001a^ÉsêèvpeððUÏYy[¶z[;\x000eçÐðl¼¬Êµ¢^umËÊÛ²ÕÛ`,í
ýlß±Çé°´ËW¹[6»ÛxÏ\x000c>³6×î<$¸ê\x001aT»\x0015³»ei£5¤UÎ¯ì\x001aJþª÷ Ww²\x000eÜÞ)²\x000e³¨}-Òó\x0000-¨1'Cl\x001dëéâYSá÷1j´Ã¦ÃÁ
àJ¤ Î72«Ê\x0007Ôa\x0005u\x001c.4â$G$òa´Õü${0¶³Ã¦¾ñð]åekôm\\x0005:Ç sY:!»ð!·ü}øX¬\x0008ûôH*~ Ã-?¼»{õó\x000folxÄ2HV\x0001»hMLA¤\x0010O­Kã7_½yóâeûûéÍhó{p~\x0012\&éºMl4§C<ë´ºöIÓá\x001e\x001dÎ¢óI:2\x0002¥uÙÉfå§\x0014S\x0000Ã\x001e`\x0005èTòH¾_%6©rI;Õõ\x0002ö\x0000Ó4ÀPVÊ}O+}béöõt0e
`Þ\x0003ÌÓ\x0007Uß#ÄM1¿ãKÒpN;§ð=¾2o,÷ngO\x001a>ñ^ºÙ-â«{|u\x001a_&«ÜË÷Í·IU|cr£G?7
p¼ë+BÙI5\x0016û0¦\x0011ª \x0003ÓQ\x0006<57 éÙnCY/\x001füi\x001e:PE\x0019\x000e3ÔÀ!jñÝR!Æt*w70*Ñðã­³V\x0000:iMü4É}\x0012 0\x001d\x0008=;I\x000bÓUàÉ\x0003\x0011¦Ó1)x*
Â|\x0018Ò\x000bå\x0003NF?2Õèïì*?PÅA\x000eÞ3\x001d)±
å\x000cnÁ\x0002¨\x0002!ÌGÂÂ\x0003®>Ô"Å\x0019\x0005Õ³\x0000½~:\x0012Ò³µ\x000c¯Ué×Ìîv\x0013;ÕûB¨2U?ªæ[AÉÇ\x0016¶ÅO>Ñã6P§«Óùª\x0007Vb@»\x0016Ò#\x001b\x0006wÚÁ?P±g:\x001aUR­\x0019zÀ¥g\x0019¡b\x0013?Í&ô
R\x0007ßyAÇÉé{ã\x0014B\x0015¬ý|°F¹2Ñ\x001cL¡m\x0008åQ)øÃâÓi*^ûéxíeaoô5Ê\x0006\x0012\x0012\x0016Ó7æ)*^ûùxÃ\x0011d\x0018#;¹\x0004<ôB¨\x0002¶\x000eØÍ|ßK»#\x001eå\x0013ªpóá:ÜÆ\x0001Æ³q»|ªÈrê*\ãt¸n¾±{(ÖH:¬ÛPk\x000f×[{K'\x0014O¯ðlÃAÊ«g\x0010ua¾ÂàÇ\x0019D/O(íZ£Î¸PEkÖñþF'Bx£;¾ALáS?Ngþ-ÎtÅÎaÈ\x001d\«¼¡\x001eÖÃO#T±\x001açcõb&}s'n"¹uÌ§uû)*Vã|¬Nc®¶l×åþå\x001cN\x0007!¦\x0000ªPó¡:²ªTÄ*ÆäÇbÂr>E\x0018T´\x000eÓÑ\x001aÖûZGúïeF¨§J\x0016Ï.³\x0006\x0015ªÃ|¨N¬Ã\x0014+2Éysãxa¶Ôa>R\x0017º\x0017w.ÉÒ
AF\x001b\x0007®^@
Õa>TWÖ\x000c$±#ø¸\x0012|:\x001c2N\x0017çÃtÍ	H2aòe4\x001aV\x0011ª@\x001dæ\x0003õ­(\x0017ynm\x0016búò÷UINúÑÉ09ÉÑóò¼\x000cQ\d9£\x000eGÂ4ô-k\x0001K\x001cU80)­[PÑH¦ÁôT\x0019IÊ .\N%¾¦\x0000*\x001a	Ó4£\x001fhÛÛ(AF¤Òù\x0010Ò\x000cÂ¨h$ÎÓç¥f¡/#g\x000b\x0011¦\x0001*"ÓDB*~bÂ$ÍÂyè¸}d¯ð\x0014BÅ$qI0Ýs±u[«\x0017½êu\x001bªX\x001d§c5fÖÉn6\x000cüfÒn\x0002Ã§ª\x0015sÕÝC·T\x0018ä¡ûù/Ç!JÄF·	\x0012oEáÝìò·\x0003P0\x0000¥êuâ«2	7Ê+T\x0019óËÉÚtÂOÝó8\x001dH'¸#ýÂÏµciáùFÛ9\x0012|³ýêó@q\x0000Ý:\x0011ùÂ¸TåÓõ) p\x0000
\x0006 >ËÜX \x001dv#¯-£CÙúå1F½5~ Ý\x0017_ÿøîÃö¿~ûçw¿>0´Ý\x0006Ò¶%;qµ\x0013\x0003½âçU÷¯_>¼yÓþ×w_<|ûi~\x000fÑÏB¬P8\x001e\x0005¬Ò¢-¼]ñ§{s\x0010q\x000f\x0011ç­÷¼j<&.wbðE¶ôúÓÜg\x000eaØ#\x000cÓ\x0008k¼Ï\x0018X<\x0016©<Â6<Ë\x001eç\x0000Æ=À8
ÐÉZ \x0005é½"Ôï2í¬[Eö\x0008Ó4Â\x001cø\x001fTØL\x0018dãl*pVO÷\x0010ó,Ä\eao`µ¿ö_U6â\x0006¿îÊe¯Xü¤«\x0002Ð\x0002·\x001b"\x0010#®°î!Öi\x0013¦Â+ÄÂÏ¡\x0014\x0015Oßê§ ÞÎo1ÛYÌÈ\x001fºT~¯ÇÛºò\x001cO«s\x00105­LóJñ^¬Xø9\x001c}M V<m¨h\x0005¦y¥D\x0019$\x000btÝê51\x000c"ÏÖÌxúf?Qñ
L\x0013K;m¬íÛ>µãÊ"ú\x0002ñ¸\x0016d\x001e£b\x0016§à8\x001bÛì9.:\x0017\x001d\x001a\x0014¹À4»ÐÅ·­\x0002\§Þª,v¼à[+zy~ñAqSäé-Å
§²Ós\x0018\x0015¿À<Á´\¬·«5;"Ïf£\x000fuÐôi¥v\x000e£â\x0018'FÎIÖøI&\x0006ÆÓ\x001bö\x001cFE20Ï2\x000eG.Q"zÐ#·49-õLaôeü<Ë´ë c4Ïfä:£ëâ2DÅ2~eRõ·ðFx\x0014aùfÆÓ·«9úö2M3¹:I("¸ûÄÇ\x0011GÎ³~\x001a½b\x0019?Í2Ée¹¾T¹N·\x0007å0÷5ÍAT$ã§I&·¨ÝE7\x0015å©¼}ê<NãzÎã\x0015Éøiíb9/«²`vôI\x0000Oþ¬ 5Q&Ü¢ÍHzªx\x000cÞ\x0002OZOo½"\x0019?M2%\x000f;r\x0000w\x0005ã°ãú·V$ã§IÎ£\x0010asp¹®ú<\x0002øiûË\x001cFE2~dbò4)ßºwÍÒ\x00124<	#8*ÁiÙ\x0012ÜÀ\x0011<\x000f",0î2¸\:A\x0015Áq>rcÃXä¾åS\x001a	îr\x0004G\x0015\x001eq><z?Î¢g|1[uZÿÎ*îà|ÜÁÂ£-~\x0017aAøt9ÕÃ¨|\x001aç}\x001e>º¿Dï9áñY¬XN;¤§\x0010\x0006å-aÞ[ÐI¾\x0013©eó\x0014$ê¿aÎaTÞ\x0012æ½:+ùK£t·ÓÄõ´\x0007y\x000e£.Î»\x000b\x0014±o¬Ý_cê©öò\x001cFå1aÞc úÙ79UL¨\x001c&Ì;LËg%³E¹øû0.þ9/Æ¨<&Î{«¬aÒ.1^Jó\x001eËÈwNWâÌaT\x001e\x0013§=&¥mÓgßç8\x0011\x001f<}:¿4QyLöDã·\Ë¢òâF©Ä2MGå0qÚaRp÷\x001c\x001bc;\x0018`d¶ë\x0010ÃÄiI>ØØNcöCÀQ\x0016]'JÊaÒ´Ã$WåCG*R°\x0019!Ãx*>Q9Lv\x0018ºhydÍa\´$î,\x0007ï¤Ü%M»KLÅç7Ý£Û?uÜùOçç ê×¬iwiÿu\x000f\x0003a\x0017KBZ.\x0010×;»'t)ðÈ\x0013ú[\x0017yI¨Àk\x0007Zà	#ù¶\x0007ppê
\x001d¶}·äg?½ýíww_þüþ\x0013\x0008\x0003=$ôøM\x0002\x000bÜùFÚÆ¼E´x>{õâ»Ï\x001fî¾üêõs ú=D?
±8î¿ÄqÂã½¯¼«¹Âé{Ì\x001cDÜCÄiAVµSËß¤\x0002Ë«yK³#9\x00071ì!y+FÚË°AÌî3\x0015ùºYÑÅÌA{ÑbÅ$V,üÐáEÏ¬x*Ò5\x00071í!¦i\x0015yà \x0019.2ÃÐ\x00162þÐ\x0015OK's\x0010ó\x001eb·bäé0\x001aÛ`IâfEYm^Ê©Ü\x001cÄ²Xæ­¨lXeò¥YQÖÚ×\x0010×!Ö=Ä:oEÜ$Asù(ÖþEú¸§×)·½[ävóV¥ è#t+F'g1ârÐ\x0001Í.\x0006z	´¨¼Û1qêÝìyu}=¹Ã¨è\x0005¦ù¥ÒÝªë\x0004¢Ýì(a§¦Ó÷¬9_``²ìÏÞ80±ÇøA§í¢s\x0010\x0015¿À4ÁTX£\x000e\x0013M¥öLÂ\x0011ÏÛ\x001aç\x0010*zy~iD\x0017Þ(P·/yPàrØ\x0001Å/` \x0018Çóbí0Ö{6b\x0000ñétÁVü\x0002ó\x00043a\x001a\x0007\x0002)Ã§½Zs\x0018\x0015ÁÀ<Ã\x0014\x0019ân1Rs\x001eçò©Ïõ3ç0*y¡z<gd\x0015åScÐ\x0018NÇ\x0005±}\x0001-oF?\x0018
¶o?üõÝû_Û%æI|9Å$úC4BÆðiìåhéØé]õÅ/\x001f^Ûî0ç÷ðü\x001c<êOæ\x0011iz)ùÖA©§yÎ\x000c<ÜÃÃIë\x0005's\x0019úW7ë9YÙUNuifÐ=º0i<\x0018s\x0012¹¯,èmý"¶Ñüg\x0011]Ü£¶kÇ­?¬mo/<xÜ\x0012î*öüño\x0002^ÚÃKðÒ\x0011vx \x0003I:AñNu¯fàå=¼<	\x000fFã~¦ÜµÛí­wÞn0\x0001¯ìáÙ°Ò\x001c\x001eFÑZMc\x001cµNóÎ «{tu\x0012+t}ïÆ²É0¦á¶ËQåÖ@»Åd7Þù\x0004=·±Rm©ñ´:7OsÆ$iÄZïåìU¾Ä\x0018euZuçÏ\x0001\x0013ð\x0014gÀ$i$RþñyY:%a½Sõ\x0019x3`4"õ ö1Ï\x001cA8\x0006\x0016Å|çï¸\x0013ø\x0014kÀ$mP³\x0015«\x0019\x0010>^Ý¶-á\x0011|«Þ¡x\x0003&#Òô3ÃKT\x0005Ùày\x0019B­îT i\x0006â
$Hs\x0003b¾*C²4UÎøà¼sr\x0002"\x000ed\x000eº\x0015¹2ð±Y\x0004\x001e¨"|«î¡\x0003&©£9ª,uàQ\x0007Â·é?0¾å/ìëþ=±\x001aeÿç:I»f²2NûâbÅ\x0014DQ£«\x0017O\x0005Ç(Ûÿ¿Y
\x001c?DmÎÂq¤÷ÕnôJï\x001fÃôÓ(©ù}DDAÙøBuç\x000ff7çÚ\x001f-qS\x0017$ú\x0001]>ûwýñ=MI~ùöÿùíÝû_¾Ãm»Û¥a\x0004ø\x0004c4í¤3è³?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=fb>ÛóY)Ñ­'\x001a®þ\x0000°­=ÌæÀ$¾\x0007ôbÀH'yþ	ø\x00124

ÇNûÕ*NKâPjôÇÇ_f\x0010!\x0005ªÈÃØ¬g	\\x0007üìsÈ\x001f/¯Þ\x001eÍnÆi©Q\x001cÞó`±µÛ`i I</p><p>\x001añ}u6¾\x0014Ìô`F\x0004Æ\x0005é\x0006Â@MÛ9&3¤\¶ç²".ÇÕ\x00038iÇ1\x0017´¢1µ	Ìõ`N\x0004¦¹\x001d\x000bC\x001cJ_Ú^¨\x0001fþ~)ïÁ¼Ôbt\x0007Ô\x0005²Å¸n,ØMK,ô`A\x0004¦X*ËG\x001aak#-ýù¥\±ç\x0012®\x0010)µ\x0016µ,1s±è°Ô¾+õ\IÄå¹<\x0005ì\x0018O`<²9ÍTÃ.çêjâXk´\x0000,ÔX¹ÜÝÁHÅ\x0000/ï³¯KÁF¯/rû¡=\x001cá\x0004\x0003^úÊ7ga6
n\x001fD~\x001fó\x001dd³\x001c\x0013·|G+NI¾åàÅ@äÆB{!qJu&coáæ$)
Þ\x0002Dî"\x000c\x0016_Ñ"k¯\x0012ÉÅMrØ Ý&´ÒDÛ¦rª%Î<N,'ÓÃò×ÒåÏål¡êUm)½eé!¶Ð¢à"ß[=Mjúõ£óêw³ÁöR°aõkÑê7-
=ZäÊPJk\x0013Ã&ßï»WðrßHË&9à4÷SÔR\x0008[v2}/u
\x0017ñ\x0017\x0018ÛîZk\x001d\x0016Ð×\x0018gÀ¥9Mçñ@»Éí\x000e®å~ýÚä6\x001eoî¹=¹zxúåès£^±bh\x0013oÉ(~!Kû;ââ¢Io\¾{vruyýöHã\x000bãÚ\x001e×®ÃÕU/\x0007ìY"+råh|úÞ!ÅUqb]\x0015Ýxùöí</p><p>¸ÄA^©Ýµ¯\x001dþö÷ûøñøªtÓ\x000b\x001b/0ÏåÒrÉlàÚöö\x000cl\x0002ó=\x0017YP¯vu©üþØÌô¡(n\x0019î=+s\x001aÌ6±%¯ðl2mÂs~ù\x0019¶iFÙ©âÊ¯Ø­v¬Ù\x001cõ¸©Ë$~Ý6gxÙèÂ!7\x0017Ø¬v$¤¦\x0019\x001ae§+\x000b\x0000!rý)\x0007o\x0015\x0019â\x000c\x0019«&Öàù\x001eÏñ,·v\x0018|'`>hâ¶0ÿ\x0014(\x0000=`\x0014\x0003ê&©ã-\x00159æ\x000fÜsôAÍ¥Ý\x001dÇÖ;\x00100Mª·8âü±Öî\x0017\x000fiÖ<O8MR^õêÿç¿ÿ³ïùÔ8¶}QuÖ\x001fðë¸</p><p>üb\x0015û»÷äâäìS>)'Ó=åOK¡¶µ/p\x0019H´q\x0013éÉ,\x0007|Ô%zÝ@EÐ$,â\\x0012b9íÑ¬\x000cM[n«3©uðäÛ>O?¯4·\x0014Í÷h^Hß\x001f[=¸Q&ÇQÜ;Ûñ·\x001c-öhQøA\x0013{\x0011\x0006l5ìæp´â\x0006´Ô£%\x0019Zbe</p><p>lYç</p><p>MH¶åzguñ\x0016u¾Í«A°o	å÷m</p><p>9Ô±\x000e¨Iùñ°Éjý½Ç÷÷ßÔ4:\x0000Ã\x0001hBÿa®óõy:v0ÙHî\x0016Nóû¶\x0015\x0004¶Û[\x0013]-&î\x000ejûðJ\×^DâÊ¼Ö¹&Or«x§G\x001aø¾¼úâæo\x000fwÇ[Nç'\x0008T\x0001®Çmà¢ ¼gò×ï§ËócÏÓó\x000c|_eý,\x0016æÓ\x001d¿%qÓIZ7¬ÜÝr,Óc\x0019µrÌ	tÀÙá\x0010<ûä4ë\e{,+°\x0016¸\x0015ÐÃöhCþq\x0003ë±ÀZ¥-ê§Ö·`Û-(^Jå{*¿*Æ\x001c'ñ¦Ì!p­àÉÓ7©·¦ÝåX¡Ç</p><p>Ë±R4Ü~\x0015'ôzc°\x0019k¶w)Vê±\x0000\x000bëÔYrÎ¸\x0005ªäö~I=¥í´øÒ\x0016·õáëÍÛ7w÷ßOþôôõîöþØe&\x0013°¶\x0005&!~D[]ft®\x001f.Nß|<=ÿéäO×\x0017çgï§Ó=Ò¦m¯\x0005-X\x0019KÅÖ\x0000\x001eÐ\x0001#÷;¢6\x0010ÝÛ l\x0005´= \x0015\x0003ÊRsk\x0000]\x000fè¤'d£øYÓ\x0005ÛRaó\x001aô= \x0017[\x0010¸\x000eßìö(\x0013Ôöz+`ì\x0001£\x0014P¦nèý+úÂ¡ùb
[`×UAé\x0008!`\x001b5Õ\x0015\x001cö\x001c\x000ccþ\x001aÀÁËØÍ D\x0017´sÃzNµscë\x0017a\x0013x\x0017k1\x0013n\x00122¡WíÉ"lþÆÃ&\x0001ñ.\x0001Û"\x0002­¨&Ñ$¸ªjó'\x001eö\x00087J|ÎeªöÆÈGptc"`\x0005 \x001e6\x0016o\x000c¨\x0018Ðriic·\x0010¦ei\x0010»H!0ïn\x001ek°¡ÞNâèãP«iÙ±ÌªÒå æÝéÕQý5\x0016¦AìÂEh\x0016Z«$v,ÓÊÛ
®rffo\x0008ÐLfDhÉÓhNÌìpÏò­/èðEf{4+³Zh£PK%Íx?d³m"s=av}\x001d>m7	\x0019ö$>Îl\x0004\x0001ïÑ¼ÈhÎ xpÍ\'*cÏ±Jë¤¶f&\x0012 \x001e-ÈnóG²ó,	ÔÊÃ\x0003\x0016Å,Ê\x00169\x0007ó\x001d9§\x000e±#¦m®#õhIæÕl{	Ë?²ôÔîsMÛs\x00176AìÃ¦Ehu´\x001c?Òñ<\x0019Ït>(gì0\x0008±	</p><p>àôIÔ|ØGû\x000cÞ
ÇÔëüÒ«usò\x0013ªã\x001eO\x0015&ÅMïÙ¸)\x000b×~ÒWtzò\x0013</p><p>ã\x001eË\x000e6*ÝSéåTùïÓ¬N\x000cÓ</p><p>Rðó94\x001bLÏd$L
9\x0013ª/	Jt|ö&°\x0001ËöXVð\x0001!¶\x000f¸ÓOZ®¼ÌQ¹ÊI\x0015¨.Ù)ã*x</p><p>0¼¨l</p><p>±|å\x0005Ær°tù?%"¢{70\x0019\x0002+Ã</p><p>=VXµzÜ¶îp$\x001el&nõòØð³\x0001+öXQb-ômS+Æô)aé\x000cÔZ]÷Q±×Ír¡d\x001e\x0019Ìñ>\ÿl°I½ÔEdf1\x0019z\x0006CCE³ý,?Ô\x0007K*kÞ¨ÉPÑ\x0005dé/ÿyÿ\x001f\x000fßú¹\x0017·'\x001fò\x0008tJ\x0008òýöæ)ÿ§\x0007\x0005Pd!\x001fr¬jÿ¯lù\x001f«\x000b=¤6!èÓÙéõ\x001fòßÿ\x000fÿ×ïÿþýæ¦ÿûýàó×7ù\x001f¾-bÅ³89ZÁé|å{%_.\x0019\x0007§ã/àÌÜ\x001e§{þúôêòýû³jÅ\x0003ÝdÈøRºú¥</p><p>^(á
âyà</p><p>9
/78¾\x0018cl½ù+xÒ}Ùzþe¬7\x0019>¾\x0018/ïÀòq½Êç6\x0010\x001dåúi½1kè¾þõïÿ1¬üo'W\x000fßîn\x001f\x000f"Ùâ\x001fbIaÓ$êCâòWææùÔÂÑòÿxruùñüìj\x0011\x0008-²e ê<\x001cê¡jM |à`ùz\x0010ZNË@\x000c¢( X,\x0016	$2ë9hÝ,ã\x0008¤)çòùA[MçuCÁ]²Ü}½\x0006&Õ/\x0003
Ä*ì*\x0008EsÉ©°Ó/ã`1ÇÌN²bÐ\x0010êÌá7|\x0018\x001aH¿Cóð$çQ?TÀ}òzÃJ¥!ô@òQ\x0018ÄÑY¡UÔl\x0011Ï-mk@hòü"üçRh ´RÛq¸Õ\x001cmØü"ü=tãÈ\x001fAóNÛ\x000cÒæË/û4ºaòZ5¯<}@\x0019¼XÍúÅÚfÊ/#\x0001*\x0018v(4ÈÁ³6·GT!É¿«¿ÝÿÛ¯s1Î»ûï\x000f_ïî\x000fâ\x0005óJÕ¨\x000fòº\x001c(\x0013D</p><p>7\x000e§(Í\x001cï.ßº¼8?\x001e&Í\x0002¦0¥L¸·Ë~Æi¿ÔéhÛ\x0010ËõLpf\x0001\x0013&51Ñ¶\x0005Êb)meÄ0Ï3åX\x000b R­.L[B­q~+\x0014K\x0012¨VNòw4)ªË¡^Ç\x0014Ãßb8\x0014*¿ùõæñçû#±^þ5¥L]¶\x0010\x0012 È7\x0007\x001dà` üæÇÓ«\x001f.ß\x001fÙ;¶@ôy6lÒ¦X+af·ø\x0004ipzvuIáèp\x0017Â©"(Ud(]î\x0008\x0017wpÉ¼\x0008\x001c\x001d´2¸|</p><p>P]­/\x0001kYnÙ*¾`D½þ³þÝÝÛ½;þÿþ?N\x001fÎ×êï]}Êû³Vq;SÏ¾üOr¸è£õb\x0017'*ß«O\x000f	±
\Ó­°K{|8«\Ù~ÕiC#[¼ó×\x001e\x0011ÙôÂ¸,FäN\x001c¾¦y_£@ê1¾Mò\x0013©ðkú|;'\x001f¾>\x001cd1!ß¢_Aõø\x001eÊüy</p><p>a\x000cÕyæKQ&"..?ýáËÍÏ7ß¾?\x001e\x0005(-\x0019¢\x0008ìüÿÄqÈ\x0010¿üòî~Ù»~ùõöHÐã4Ê ;GÁ\x0004MeÈ«g?|zóãÁî«\x0001£¿\x000b\x001eÇ\x0008*R`à ¯a]#ýÄS\x001d¼f?v*\x00187_nÿ:eøò\x001fÎOnè'\x001fnþ×èÃÁ\x0003\x000ec#ÖÚs\x0011¥"JNC\x0001>äcd<t1?y²Ë÷\x0004Qþ÷>\x0001_Í\x0010ä¨ºö\x0010¢>V¤\x0015\x0002 \x0003hÖ\x0010ð]x	AP\x00145º\x0002&,</p><p>A \x001bF\x0000\x0005z
Ânk.Bº\x0016\x0012\x0014!§à91\x0007°às>ãº·¨ô×ù\x0017¸ 0qzóË-=¾IuSmÝ£.¡r2îQËí\x001d¾ÌmÞÑ ÈéÛ³çöjãÒ=\x0016p¡,`}^ÇÚúú¡lö§º\x00066\x001eÌH\x000c\x0006¸´<pP-ã\x001c«ÅÞ\x0004f{0+\x0000Ã¹ÛõK\x0006_*íËi~þÉîÏmáò=\x0018Ì'¾\x0004UªKÁP=¹iH[ÀB\x000f\x0016\x0004`£|Kk_¿r>9>³ÝÄ\x0015{®(1QmRjZ÷¤á\x0015¶íÉÔ%Á\x0003N[}EöR}EÓÖZÅEe\x0008ìÃÄbÊP\x0010NX­X12V°°\x0006\x0017\x0006\x0012\x001f\x0006&SX\x001c¢\7$NÓ%.7Døb®ÁÄ)¯i\rÑX\x0004d\x0001%2å7
.\x000c$>\x000cônKbg\x001aq!}Þ[V>Éø0\x000cë2ié×)\x000c\x00087\x0004	¤à¶xW\x0018¼+HÜ+¦ºÂ¼)#^xÉXË?ïÊ¤·
î\x0015\x0004þ\x0015¤ô\x001ejQa(U2\x001e\x000eávãH×
þ\x0015$\x000eVyGú6Ç¡ø]×äU\x0006~ÉôàÈ´Ä)ci,£Å01V_\x0006>XÞ[V\x001e£1+Ã×½@`¶T\x00160Míyå-\x001fSÙ&Ó"\x001füÅòà\x0007øjæ5`TV
ç,¥=xØÄ\x0017¦|AÆ\x0007.bv¬86\x0015°É±\x001c\x0006+	«¾¬rvÿQ</p><p>«än¿ß}¿=ÁÖ¯×_oîk¡ÜË)è@õ\x0013\x001e³RØ×\x001cÑ|¬÷Ð³OçÎN°ûëõÅéûÃ¥r\x001dîñ´\x000cOç³ÓQþÓBÝ­¥®"\x0012V[ñlgÖC\x0011\x000b®\x0014H\x0002Í·*Ï\x000ccÞx
ïñ¼\x0010/RcfÞ¢</p><p>íXè\x0002µ\x001a\x0006í¼ÙH\x0017{º(¤ó\x0006u¸L=V3S¢\x001d3z+ðvQeÙ\x0019JÈÃõhkäm«èãjà¡ìF¼agpk\x0000«tºtÞWJnØ\x000c:ù;\x0003\x0001Â­¡ò«m9³¨\x0014Vø¸)>»Å°qñÁ°5@¸70\x000e¨u\x0000\x001fOS·H0Qo]}Ãæ\x0000áîPÆPRÙC¾9\x0007CÏò´ú\x000f+=KS¨æc£(TwRg_\x001e¾\x001eËgb.µUrxLg}á9JÎõh,luöæòâHju¢<öÇÃÂ>\G\x00157Jq¥K¾rqý\x0000\x000cEeR,Óc¥X&{¶Àu\x001eùKç»¦³#á¡ZÊd{&+0byqçó¥ËWÏk\x0014gep®Ó\x0006,×c9©ÀÑøc\x0017ªÙµl-í9?\x001bÇ')ï±¼`½\x0007G	\x0006çQF¢,ö]uLØ²ªBÏ\x0014*ZûÒÈ9¸TÕR_ ço¶\x0018*öPQ`(¯ª²Áj©A\x000eß4\x0017xÅ!Ó'dj'yuVê÷\x00015¬(X¼¤òJÏª\x0003c>\]èª\x0014³[°\x001bÜ\x0002\x000cß\x000f\x0016À¼ªðE¢m\x001d±¡§,+ÖÅ×	»ËL\x000f\x001cÓk×¼yøí·ÛÇ/GÎÂüñ¸2\x000c»C½\x0005\x0004O¬Ç</p><p>º)×õÉËwïÎ®Þ\x001c;	ÍôÈ1½zÍ\x0002°6Á*»Oµ\x000b£ñwXM²·\x000f%\¦ç2\x0012.Óª>µ-ÚD\x0005Ls^È¥=ÿ.ár=\x0013p\x0015³j/ã±P¿p9È`yCnú¾\x0007ó\x0012iÝV÷\x001cm\x0005\x0000\x0006\x0003p[ÀB\x000f\x0016D\x0016³ÔcçP&<s±Y,m\x0002=Xá$\x0004ME\x000f­×{~<ôFï\x001d\x0012°Ô%\x0001Á\x0003\x0015¬La®Áãl;\x001c\x0005`ÝIdé\x000bLòMD\x001dm5Bun>À~,!!\x001bý«ÄÁb§p­Ê6\x000bøbWmÆ±s0jÏñwd³u</p><p>
kð® q¯Vy®:5I×hò¼+v>åà_Aâ`I\x0014\x0014É,?\x001ff2®fðm<ì:0;YÉT\x0015öÇÊ¶Ä\x001c?P\x0007£·x~\x0018<?H\¿Á¹ñu¡h³â%FCp<ÖQm!\x001b\?H|¿Á±A@deäF!3ü"\x0016¬Ùô1\x0007ß\x000f\x0012ço¨¥\x0013e$M]bÖ+Þ>nÂ\x001a<?H\?zXE\x0006ÓÏ<\x0013\x000fëô&²ÁõÈ÷ÛvZZ\x000fµQ1Y\x000c{ñ¾L\x000f¾_K|¿Á±mµúÉ¢28ù\x000bÓ>fÚâúõàúµÄõë\x0014yõ\x001b5ò±<ÑÈã;Ê\x0016²1¶xwj\x0006Ñ¡&\x0013m\x0000§\x001cËýl\x0004lpþZâüu Ñ Î9ËO&&q\x000f\x0019\x000c»\x0001lpþZâü£µjÜcSb7ÂØZ\x000f\x000eV\x001c¬kÁ5\x0019«×J\x0012àd0Ð[\¿\x001e<\x0016y2\x001b¹mÞ¦¸ó\x0017É4l9.Íà/È_hK3\x001c\x000e\x001a£Ef\x001dWtE»Å_aW\x001aÉ®Ä`¿h9¼ýRö×òüÉ¼úí©b÷ØJ69eÑMNyÚ\x001aåoª£õå\x0019¼6ð¸U½]Êo\x0004h`iÊ(¾\x0011ÖwôLÙj¨\B 45\x001d$í&Ç§ó{Çç*kü$ÿc\x0006íâßo~>êm¡µ\x0005ê2³¾¸Û\x0018¸ÖÌÝç>~:ýa\x0001îôr¤HkÌ£d\x0016\x001f\x0000öIsîl!íìb äySz\x001bkïF5ôÙ¦V\x0019ëÜb¢ü©¨$/&LÕ{ª</p><p>`õz$ß#ùÅH8\x001dÊ¿m^HÕH. !_Ïg\ê3Dzú6èÛV\x0011ñw7wwÇv]^C±Û|\x0006±\x0018\x0002Û}4MJEE:üÝéùÕù\x0002:ÓÓ\x0019!ÑJÄA\x0014Ux~*j|\Açz:'µáÞ</p><p>\x001b\x0014ÕÓkkU\x000bz\x0006©5x¡Ç\x000bR¼|XíZ5¾\x0019opøkèROdt\x0018ú×Q\x0000\x000eg(hZyº¹ûä6~[\x0018÷pcä£\x0011\x0005²êÇMÅ6ÑòÕDY³oX{ \|\x001aKíiçÆf?\x0013i\WkÍÆÏ\x000bÃâ\x0003áêC)@z¸t éT0\x001f¿Pêv#Þ°ú@ºü£ê$\x0007\x0011Ðê)Ê{£)V­w{}<T]\x001fþBæý<U\x0016ïWtv5±¹¿K\x0010«\x000bG\x000fóYèb\wzPµ,VO­þ9ìBÞ</p><p>xó{\x0001TÓÃWÕ¸òáé{àþ^'£\Þ}C¨\x0003 ù¼ÅË|Y9s­Á×OKCÇ"ÀÐttuyý©ðÈ?Â\x0019)ç\x001fñÿö,±îõjâ 
=§ùPk`\x0014P¤nÝÌ î²	ÙöÈv5²Q7à+\x001b\x0015x\x0000¯Ä\x0012±¾\x0010¯ïyýj^íÆ\x0005\x000bÃÐ/ð\x0012¬_lUt\x001b­¬uÔ8\x001dÁq9\x0018àâ6å¨ó\x0015¿9êÏ#õç-Ë¹\x0016zì\x0010­oy9S¬\x0019³+	/Gýe¤þ²:µ\x0002'ZmÄZfxéÙ</p><p>­¦\x0005\x0014ª\x0016P¼ùõö·»{¼ú¼~¸ûvòÃÝí1÷éZð¨µ«=Ù½%.È´c=ë\x001fÏÞ¿Ç+ÐëwòÃùÙõá.q5-¤PµB\x0004\x00185MXv)\x0007¦õé</p><p>¢</p><p>\|2\x0014ÉÏá=k?ÛãY)\x0002\x0008ñÊÀ\x0014ùBHMwM­®\x0007tB@­Ây9\x0018««R\x0014\x0006<u·\x0002ú\x001eÐ\x000b\x0001C°­× ZÊ@°kZ\x0007Wº/ö|QÊ]e\x000c\x0001[40ªû¡4»Õ¸ù\x0003§/	ùòU&.{þ4MP¬´~àè¶\x0002îª\x001b\x0014U7\x0008óiC¹:\x0007g%\x0004g\x0002\x0013ª!W·ptR/CXÞÅX\x0014ªòJ -àÇtÆ*ÀÁ	Ô\x000b:ù1dÂø;¹q.[0m¶àà\x0006Aê\x00071³ÈÊ\x001eQ$\x001d	ç¶:i\x0018\\x000cH}\x000c8Ï!±Ñ¥uRk;p>nþÀa \x000c2Â2\x0000¬V9{\x000cE*\x0000WöûQÿj\x0015áà\x0006Aê\x0007±\x001f÷¨\üL²¼\x0006ÃfB=ø\x0019-õ3*o\x0012MÐaD\x0001tme½«\x0000\x00077£n&Æ|¾U\x000bZ_t/\x0011Ð%nm</p><p>Êl]zµ¤n&ß\x0005Ú*´E\x0011³ý K[÷±\x001e¼z¼B¨²Öç\Uð,âG!×U§ÑBO\x0013QnÚÑ6¶U¨!\x0003\x001am_l\x001ba\x0018á&Éh\x001aùé±¨&Øw¤ë\x001f|ð	Eh0GV9L­\x001fÙâ\x0008Õ*ÈÏ=¶a\x001aR.«\x0008ehË0f§GÞ½­ÙÞB¨¸K,¨ÍA¿\x0019¡.Ãè\x0003½Ùz\x001b\x0003uÈªrÌUB­¶ne3\x001c'FxÄ\x0008\x001dòÚ3õQ9\x0014¤#9¸ÍÎÐ\x000eëÐJ×aðüîí3LmÇ@dZÉ«­\x001bÅWOé2Ì'Û+â3\x000fdH¼</p><p>Kx³5jíå\x0014¹âodÁkäëfUw§Ú\x0012\x0006eU÷'øË÷ÛÇ1\x000b¿\x0010B\x0002wVb,[÷4Xz,\x000f6ÕÚM3Òn:\x0004ûÝÍÝ·û6RúÀ\x0007·ªòRLÔÝ¯ßÐ!ýU¾\x001b(ýîôüãåû£Ó¤;NÝsê\x00159´æ±\x0007y	q$ï(Üì\x001eÔ¬1¨áÑuErAUëÔC)ùjPÛÚ5 ù\x0002ÓiÖ:i,rkÚ .¼\x0004¨ëAÝ\x001aPÅ¯ÇE9¢4eaµ!)há§\x0011Pßú5 ºä+(µfÐÄi\x0013{	ÐÐ\x0015 \x001aå×9ÃH56:ï\x001fÓÃcãjÐØÆ\x0015 Æ\x001aÛÊ´¡jÑ\x0018
gB_s*^T­²¨"e\x0018¯êë^µ(°E}O\x000f\x001f5\x0014p,A}«O´)mÊç>;|ïÒK|{\x0018ÞÄËé¿oª û\x0003ÊÓ\x0001eSh\x0007Ô&Ëæ¯?yòáÉ£¾ÍÞ¹»½ßM7?$`\x0014=Ý,\x0001Éâ´$6÷Í\x001dùø4súþÍùÙûãsÎ;\Ýãêµ¸9\x001c
¤h]\x0002érj®9(·ôM´fj\\x0003÷¤\x000f_oò¿fä³£O_9'Ý\x0008ÕÉ³;eM×üßd6úpqÿõäè£\x0017C\x001eÒ¬Ô\åc;~WJª²q;¤ë!Ý\x001aÈ¦ó\x001eP\x0017\x001e\x0011
K=tÍ01¬b¬\x0015¦3Z\x0019º1:Ù_Bÿà$lÖcØütòÇ§Çÿú(®þô÷CV¡r,Iq;¸ÕÀ·\x0016Ë8Jõ5·t}òÇËë«SW¿þóó¤º'ÕkH±¡ÑµÎ\x0003ïq­,&o÷ÙèI</p><p>j{P»Ê¤ÆRG¡«o'\x00054µ>\x0004;{ÖK9}Ïé×p:ÓDMPjªñò\x0011ÏÕx>Í^E\x0016¦é"MS§¹Hþ9QUtà«§Àïcà\x000fù"~\x0016O÷xZgùÑE,\x001b!ujF·ÏÇ-Ç3=\x0011â%;º8É¼{jÓ­Ò\x0015¹T:tÜ,Æ³=\x0015âáÃ\x000e	+nsR4k¬Xç{</ý¸MÆ&`@½Xe¥?åÂÖ\x001b{¼(Ãó\x001f$
óé8ó+-\x000f<|.ÀV§h3Év|Ë1ÙÓã±\x0011H(ä\x00149ØAµtOqkÔ|Ï |ÌñØõÕÑYH
Ñôf
"µ\x0000b¨SdDÇ\x001bÄù+y8ßË¯§\x00154ÚLÒ\x001bør`ËS¤°6¹VXäc¬5oXÐõNLh\x0015_k0\x000e3,ØÅ\x000e:\x001fOó×Å\x0016ô=\x0017óåëKb)*>ã\x0014Î\x001c&\x0003Î_\x0012%\x0006\x000c=`\x001bÐ¼\x0002úÄ\x0015^ yîÚMix_aÀØóEù\x0012tXÅ]-È=\x0005<\x0006#û ð,Ý!\x0003~VÞ\x000c\x0001ÂëüÉìÖ\x000f·'zøúõöØ8\x0019üÆZ\x0018-½è"2MZ4ãdÀÝt \x000fWg'º¼¸8;¦\x001aKºÇÔ+0u KµÓH\çxÅ¶½\x0019®©k1Miä8øF\x0017kÇ6</p><p>Üt9f¨×bÚ\x001eÓ®ÀÄ7d²¦×ÔoAqS¹Wãd®ÇtrL¯¹\x001c\x001a;ñ«Í\x0001bbcÎ\x000fÞ\x0013RúÒ¯ \x000f\x0015ÊZ¥du\x0013¨p1½Ä7\x000f=fXÙ"</p><p>m¡êB#&Ï"±H1AMüQþE?\x001eæÍÃÓ÷ûÃºÕùÂ³(\x0004)ÅÛX§IÙÓ0HC°nõËëO§ï\x0017é\x001eL\x000bÀ"ð(!¯\x0002÷ ç»?§t\x0003³\x0005Ìö`Vb±¼Ú(1\x000eJñc¼å,\x000e¦E·p¹Ë	¸òñKç(6N9°\x001cË\x0018î\x0007áÜ\x0013ù\x001eÌKÀ|à[\x001cT\_å\x000c\x000f£\x0008ø´½+ô\AÀ\x0010\x001d
´Î\x0017u^úz~JÀb°ØEÁl¢\x0000Õ«¤Ú\x001d8*þ~vàÉb°Ô%ÅpO·µØiP,¦øö«¨³\x0014¬\x001f\x0010c\x00011ÏÌp-B
ÐsÑ\x001ebs\x0016[¸\x0006'\x0006\x0012/æ\x0005½ÊÁ<=IçÁÌ\x0016g\x0001\x0013\x0003\x0017ÃNª=â±\x000cj\x0003I­%\x0018\x0005sÓ</p><p>\x0016s
N\x000c$^\x000ckÄ<Ï°sì]óí5\x0005p\x0017l \x001b¼\x0018HÜ\x0018¶\x000eæ`ªÑ{±óm\x0014jÜD6¸\x000bø\x000bâ*X¨ D#÷%\x000f´
[°ô°'µdOZT'²¼
¨¼S¹4;\x0007O\x000c6F\x0016Mi±&:äCË/,¿sÀ¨P*&\x001bv¥ìÊ"Hmù]Ç#åû,O´\x0005kÖ\x001cIxzO^ZóqÞ=¾`0oä¯Ô\x0011ýX=|¬£®°o\x000b\x0010cMÙWoçÒ=på?\x001f[Ñ\}aØºÒèør}V\x0001&×ü\x0000å³DØ?ßãé°\x0003:v\x001d¿ÛA®ââtáÀ\x0001BÒ=^\x0014C¤¼\©âª='1¤Vr4\x0014</p><p>K©LOe\x0004mæ<&\x000eéu¹MëÔv\x0010ÉRÙÊ.§Âe\x001bZ(
cÕ<Û¨6`¹\x001eË	R·t\x0002ùRSåùJª#\x001b°|å\x0005ÖòÊMÍQ:0qi­±vµB\x0015\x0004\x000b\x001e\x0002UTk9ÏPV|[Xq\x0003Sê)Gö¤bëÏ\x0016ø\x000búq(¸\x000c\x000bFw%ðWX`xLOl\ÞíJQÍ\x0006®aÁ`Å'\x001b[µÛõ]\x0007\x001e¢^´¦Ös
K\x000b\x0016¯-®Ë\x0015¶TÉ\x0010eÛ`
û\x0010Å\x0005W\x0017»Ñ¤\x0008\x0010H\x000b\x00064\x0007\x000fù3¯8xòa1Uö\x0014nàÐ_2Û÷ç^
ÚäOääT½åòï\x001ago3ã§ã/\x001bLizJ³2FÞ¡\x0001ÃéH¯/\x001fFYýµ®Çt+0£éÉ.`ùX"L®ÉV£dÅZÌÐcuj÷Xi4cúöX9_:.ÃL=fZ\x0019<ç5p¸ ix\x000eÆÜbMT¢Dßz¨süV¢Ü#Î×</p><p>Ã5tó<O<æ%9[Ùø±\x0004¹\x000b¸LÏesY¼q\x0017iÒÒ\x001bZ\x0005Ëz:j¶Çp9ëÑ\x0008ÍÒÜsT  \g\x001eMFÃ³[ÈBO\x0016$d>fÇ\x0018í¹Í'ßY6q¥+É¸sU!º61</p><p>X\x001b!GTsÅ#\x000bÐÂ´Î7LªªÞüzóxó\x001b\x0000ç\x0004Òá#Ï«n-£@ë3v\x0007CÞüxzõþô_3=ÁPÉåÁÁÖPÚ=\x0007t\x0007Z\x0016¹ÌÈ ß©êëÅa?4¡×D¯OyÝm\x000b=\Á\x0019ÕàðóÖ</p><p>èÄã\x0015Ý*63Xîµh¯\x001e¾ÝÝ\x001e,ÍÆÌåÊmÝ¢\x001aX9©!"\x0011Ñ«Ëù\x0014x\x001eÊ÷P~1Tvò¬+ìðì§Q8²¦BÍ¨ñ/E=R\¤}+Ægg*ßÌ4'_½i×\x0017R¾Z\x0008QÏòÆ®\x000e©QÖ_inÔR*=PéåTX´Å¦\x0002JíÊÊb¾­²\x0003]\x000c\x0015Û­óðrgìîqâzïR¨aÃÒu·v×»Qºô¸+SÙõ\x000f\x000eK:f^4g^pî$î\x0007ÏuÇ	üú\x000f¨µ®¯uliæ¡8BlÅo%9$S+ÖºÖ@«4*.¾~xúò_ÿû°_pÑñbÇó'Ò`²l#*y8 \x0000øúòúÂ¸\x0016?«4ê*>Çew#</p><p>TþQl<P\x0012Û[³yÇ¹n°ßª·×)þ¹ïwù\x0012òÛí})\x0016yÖªîÔqíªdvKlèñ¿¸ütï ïÎÞZg>jÔ=¤^\x0001©ybWg»)Ój\x0013ÇéV+!M\x000fiV@Z¬Ü-`w­\x0000P\x000f²"+!m\x000fiW@\x0006\\x0005\x0012\x000f\x0002gØÏ°¤ë!Ý</p><p>ÈÄmUå\x001d\x0008Òs-¯}\x0001CúÑË\x0019Q\x0010Ûç|ùkÕ\x000b01È\x0019­ãÁ@Þy\x001e</p><p>¡RÛÛÞ½ÀÇ=düB¦\x001e2ý>![ðY]¹úR\x0007Î\x0013Ç&\x001cÿái ¦\x001cbìÌÝ0Hk%åpâÀ#'£A¬e\x0019Ò\x0006¹ÞùKOsÛ\x0013ué7w÷??\x001eI¹ç[*	®:p\x001aFPgË;Ç:î\x0016S¼9ÿÃÕ±¤ûTD\x001a&"ÒÏaiåÂkZ½åÌf£ÝÄez.#á</p><p>m	¨zéÇÙ¢t4ÛÉ¼;)í±¬\x0004Ëk~\x0000ªoYìÕÆWÙ`V©ª¯ªúþtwûô÷ÿöîáéëÝÁÎ)\x001cCÐ.6;\x0017G\x0016g>\x0003º¯?]ÿùäÝåõÅùî)3í2Smß©Íñ±.ò³\x0005¤\x001eâ¼ÈÒôf\x0005e\x000e\x0014¨ðÓ:K¯ÚXÛ¦Î\x001dèÄ\x0016aÂøÍÅ\x001f\x001d_e\x000b¨pÈ\x0008å2òí>ºwv9õt>öS "ýÿõ&o#òÿ&|\x0017 ù1	¯1µ§ÔX..ùò \x0000pq÷Ðñ)\x0000~Ú:ç§\x0012AKQm»36½ïá\x0010ÚÖ;ß<.Fu=ª[\x001aÜBAutÈ¡\x0005\x0017i\x001dî1ëQC\x001aV¡&î"(ukTk=\x000b%ù\x0007´¥¨*N\x0012qrPÿzó·Ç/¿Þ\x001eyàðVñíUbï\x0014½åQî£\x0006ÜÎÉÿxúÓÕeÞ^Ç\x001aÃTåu³pîþëµ1\x001aon\x001e\x001fóÿÿðAdÇ®b*\x001es,
\x0005N³ªÿ8ÚîÃùY¤ñæô</p><p>×Îv</p><p>îüÃ®>ÑNElß,òîáþûÃ1Ï?£¡\x000e&\x000bÊ½Ú\x000eæ(btÙs%ï.ßºDWô,îÉ´,$\x001a\x0012§PÍ°Ä.ÝÙñ¹ONfz2#"Ë{#&"\x000b4àºh@3ÚF£Ù\x001eÍJÐ\x001cx*iÎ\x000b/P\x0002\x0011ËßØjÆÍ§/Gs=¡±7f__J\x0016éDÉAÐloÆ3dá/¿|yúöù¯´\x000bÆ!n(òË×»oesÚ</p><p>\x0015\x0010êóÍ=21ÁQì,ÎëÌLQëÓÍîÎÓ|}ú¾\x001br5\x0002ç\x001f\x000f9·)/,ó{cÊÍýÞòª\x000c¿\x000b¦Ï*ô
x\x0001¶ö\x001bïn®ª[µy\x000ePgúÊÀ$Ò@ô­à\x0003T\x000fÅ]Éï\x0008>Áó³\x001fªèÖÁæ\x000eT÷ Óà% &²\n\x000cÞ×Íà\x0001¨²"ÅÀ5êÛ@M\x000f:m</p><p>^\x0002ê
§DäBi-}o¥¹ír\x001b¤í!§-Á¬\x000fyúìE±Ã\x0016NÅp	+^\x0002Ôõ Ó¦à% Î²¾Z6§¯5Ñà¡RÌ"kwl\x0003õ=è´/xÑFÂX´ît|®p´BUXÌ>Ú\x0017ùô¡\x0007v\x0006/\x0001
QÑé\x001b±½¢Ô¾÷ÂQÔâz\x0014{Ðø;¶hêAÓ\x001a6¹|#1õr/tF}cøð\x0012 \x001ffg¯ÖúøÊCýöÚb#{ùötµË_¹·§ÒcÉ\x0007SÓ¯1`ÿ[ªn4Q\)Øõ0J°æX</p><p>8HñýÔ×oï\x0014\x001fKù`z	ÒÁãÃ\x001aïX¿S]¾áooæUê^Æ¦Ëu>^°_áU¨6Íÿ0\x0006ý\x0012\x000e</p><p>\x0006\x000fk|¾G·TÒ£Ñ§ôª$8\x001c,Ú²ð\x001b\x000fQ\x001aÞ×Ñ\x00156
JIbÊw\x001c[YM¨\|sõ[:)×\x000f­\¿ÔÜ|z|¸ÿ¥</p><p>VÌÇÉ8\x0001µÉª¶\x0010ä0Y·0ÙÆni³OWïß\x001e\x0014©èt¤#YGuf)/¹ÿºwÉ®ëHÒ5§	\x0004¿\x001f-BPÌ\x0005\x0002¼ ¨\x001d-HD\x0004\x0002</p><p>)ZÕ­!T·ZýAÌ¤FRfîf~|\x001fýpßû®«÷æ\x000e%3CñÉ»ÛÃÍ~Kz$\x0012Ë\x0007
1éÚ1neÒ5^Îä\x0004e<ÉåÑç2
­)PýL¦f2u²5ýs¬«Ür&TÇPÄ$³\x001a0¹\Ä0e?¯¡|Ã\x0017©ï=ê\x0010)üó8\x001e¡é</p><p>5ThX)\x001am\x000eL\x001a\x001b\x0013-;Jù\x0015L±f
\x000båéª\x0007(ÿ\x000c\x0005£ÒB\x0019É\x000b%ú¯¨âÙå[S,§RÊs£ö"WÊ\x0000\x0015\x0015Z\x0003UQî¡\x001aÞå
9\x0016í\x0004¢²Y\x000f@Ï;]Æ\x0015k5¸ÎeÃ}.5¥¸#^\x000f9\x0000k%ø\x0017\x0014,\x0011ØC5¸<eÃí)\x0002uTEm©´
¨TÖQ0¢§ËÁÝ)_*r[Rÿ\x001dz&$á)%cuú©\x0006·§\~}*p°\x001cÝ</p><p>à\x001fò.ùú;uÅZ
®O¹üþx´l*áx«³j\x0019PÙ.Ü/\x0005°7êåËÕÑ_ïî?'\x001eÑÒx$\x00010p©¬âÝîêå\x001a¾ýõübT?¿ÂS5Þ\x0007Ü\x0019<­³\x0002Ð 2Ð\x0005gNùtº¦{òf;GgIñÈ}É\x0017øZõA­Ä³5ÞwÚ\x0019<å)y\x0007«\x00179©ìCY¼°vñ|M÷äiv~ñr~)-^qñLY<Ù·WóìKÍóË/wßþãúêöèÅÕ/\x000f7ß\x001e®^Ü|:¶Ù)DÆRÞ\x0005ÇÖ\x0007ºL³ÓúòôüÝÑ\x001c\x001d½8~{ùúÝåÉÑ×ßMà½ºg_êAÐT</p><p>\x001b\x001d</p><p>Àå"7\x000cZ/f?¨®Au\x000f¨\x000cÇ*Ã\&½\x0012B8çÚ\x0002ÔÔ ¦\x0007TEÒg¨s+²Ë¤\x000c\x000cZ»\x0001ý ¶\x0006µ= ÚÑÓ2ìQÒ(\x0001P\x001ajÇ6YQWº®^=</p><p> \x000eSô¡nr|
ê»N=bF§©-\x0011\x000f\x0013§\x0019ÜàÑ£\x001f4Ô ¡gE!*Ë©:XQ%*ø\x0015Õa\x000bÐXÆ.Ð4­>zÅ¡\x001a¾.1hÜ\x0002´ÄG¥2º\x0014.¥À÷åTY~Lp^Ù-H¦©Ç6¡F¯tAÑ|> umS0\x000elì2N^RîP\x0017('4·l|ô[\x000elì2NØ!M¤¤±4\x0008&-Ã`×\x000eì²N(LE\x0007</p><p>\x0002zCf4D&
8&r`dyI$>f±á\x001c%òz!·¸LåÀ<É.ûïÆ\x0004*³¢/ò]\x001aí\x0016fT\x000e¬ì1OZH^¨g\x001càò¹÷ÒlòÓ\x000f¬ì2O\x001d
º¬¨,É6ç~`dyÒu¯¢àMQnÅ\x0012'ÜU[\x001c{5°NªÇ:an*·\x001fÃOoÙàïrS8½g\x000bÒuR=ÖIã{'mR\x0008C9·Gº\x0013@ª·!\x001dFN=Ö	s£ü]ÆVGÏ¿þ& \x0003ë¤z¬Öj\x000e£Ç·\x0014Îw\x0017P»E@¢\x0006ÆIõ\x0018'
Þ½Én)Ê^ÈO=¼KÜâà«qR=ÆI;K\x0005Ã8Û"ÏKÂ÷\x001fÞ¤ÛNj`TmÂL´äß¦"(g5½ÝÄ-U\x0003ë¤z¬Á\x000e\x000b"u³ÂÆh&õbó40OªÇ<á\x001f¥Ô±x¶©Ñ\x001fón\x0013ÏD
ìê±OFKlÁN¤^QOMr´¦['=°OºÇ>\x0019¸õ\x0015Ù'Ü±¯%`\R·Æîf°?ßýAU=ðòóÕÃõ	:MrÑ\x0008\x001b,¤çE4Æ<}®xùýñåÉé<ªÔb :°Ûa÷ü~\x0019>Ê-\x0005Ò5^\x000cÑç\x0015ß\x000eo©þ0F>}\x0010_dj$³\x0018	5\x001d=\x0012\x0006þÑ¬4eÔÓ§¥H¶F²\x000c\x000f\x001e:jÎ\x000fÈ\x000f_p×=}!\äj$·\x0018	¢,MoqË³½-\x000f©¢kû\x001aÈ/ÿÙô3§v\x0005\x0003~6Å¥:º6­H¡F</p><p>K¬vÏè
ðJ¸ãÙ}ÒeX|\x0007Q¬ââE¨@´÷Ym\x000f\x0016:(qoË§51\x000bäð\|IZ¡K© ·¾lniº7·\x001cÜJrñµô?ip\x0007ÈÅ\x0000üJÏ\x0014UÄX$øEwPÐ¹IîÛ·'#Ç¯^Üã\x001b\x001b5<\x001ed£±ré\x001aG\x001f,ß\x0006«=¬\x0010µ\x0015Þ
ï>>zq¯lã½\x0015£­\x0019m;£õü\x0010îÈYAÏ\x0001ÆE½Ñì¯£\x0019ø	÷×ß¾]Ý~ÊÝCëð1<ásÈvpü´\x001bÅ÷âäÝ»ã³W'\x0007\x0007\x0008V\ªæRM\NòQÀÛlO)äAqú)¬Ù\x0015Ó5n"\x0003ï</p><p>/à\x0002Ë\x0012)7Áh:¬C35i[´rÏ 0q\x0017Í\x0004^5·\x000eÍÕh®	ÍgÙ»1àJ8\x000e-©C®D\x0003Y¨ÉB\x0013\x0019ÎÙË.\x0005m4æ	Í°qJÂW íÙÒá\x0014-l¨\x000fÄf,n»þ&²AW\x0007ÙàxÊ¦ó©¬â Òâ\x0010E~?â§
aÝª
Nl:\x0006øöNÞ½½{%\x001cý¢î \x0019]Â\x0016ö¯ÛðÔl½M\x0016áúËq 4
¤</p><p>GÓ\x001bzrçÚIp*ÍMHÅ!\x0017'§§SF!ì_qa Ï±R</p><p>C*"QÉTaÂ²åWªvÌý</p><p>y1¨\x0001¿3éÖ\x0004¹^1\x0017lV3m¿y\x001aÁ½ßx\²¶bR5ZÎ$\x0014?\x0004\x0018£ùþx n¼ÅPºÒË¡tDÑ</p><p>¶¤£8cQX±R¦2¡,ÊÓ\x0011ÓÊA</p><p>M2ÂK÷W¹\x0018ÊÖPv9\x0014lxJ?ÁenÖ\x0007ÞSæ@¡õ,Ü÷u¥¬÷ù»«Û£·w÷\x001f®r'þH,î1\x001fÜp­Kz@ð;.b9\x0015Û»ã×gGoÏß_¼<\x001e ©\x0010U¨Z\x00111G`9©b¸ ßèR\x0012n\x000e\x0014_·"ê\x001aQ7¯"F	ùF\x000b*÷'y«<ß»Ú>=	­¦\x00064ÍBð«±ÕËrV¹$¦\x000e¸ã­®FtJÄP#vÄ\x0012Ô`k	\x0019XceIÊ§S#bÕ£ \x0007nÝRFþEù>ç©ý\x0010\x0018KM­<8Úc,ò\x001ac\x0003-O4Ö«Ò-­Ë\x0012Âµé\x0000ÿ}õ\x0003#ÛO3\x0014X(HgÚñ\x0016ñi\x0017Q+âàÀÈö\x0013ã5oG)\x0015¿\x0011[Íý\x001f2¨Õ'F\x000eNl>2\x0018^d\x0005Å(P-PGÒvú@jµQ
j>2\x0016+òv\x0004{Ç>+¯.RÚ§iÄVÆ¡
l>2Î²X\x001cæ{JJÊ&}-VïG582ªùÈàÜÔ¼Á\x0005À\x0018\x0014lÔÜ§kÃ\x0017¢æ\x001büÇÃ;ücóå£°\x001a9_>iQóåÃ­xÚ\x001fè0k¾Äüiï\x001aÿ©ù\x001e¥\x0011¢uîp»{ü@¯nûb^
\x0017óª\x0012|FîkÄÈ¤4ð5\x0019åj\x0008?
)×R;,ÎN®ã×¤ÌENî&\x001bóÃòC3eDûÁUd\x0007H\x000f©»7æÕÞÆlþÉ±:"\x0006©¹È3åÄ3¦;Ðô»\x0014\x0013âë½àÝ\x0011\x001d¯Ìû·7×÷÷\x0013ÂPX¡Byh\x0008\x0008éé£\x0014'_T­é\x0013a(æ~}r1*\x0003[QÛú°ªÖRjUB\x001e¥²âfÊRì~­!±\x0016Û×Ø·bk.©Æ¡`ÛÒ$·Xí¸¿GâpþÏ¨:\x0003¶Æü4}\x001c\x000c½Wìw>
Äq Æ\x001c\x0003³èEÿ¯e15YÆª9\x000c\x001eÃ\x0004£bÉ\x001c>ñÒf`ÒÛ~'½ýÈÝmï®~º{|âÂ,µã]'z`á{äpK\x001cÈ \x001eÃ6zq~9ýÀ5\x0014àö;\x0001î\x0006<
>·àÊ</p><p>[Êô\x0014ç1MÏÒgj<Óñ´*xt\x0010È\x001bKxkWÏÕx®õÇõü\x0004¡qÂ0Wà\x0017<Ùýã\x000e\x0007Òå?Øí½oIòßÿ=èÇ\x001c0ÅÐ`×H\x0011\x000b|/Î·Zý4)ö.©SL¦ùý~\x0016ØWn	ñüDèá'åw|Q</p><p>­x
Tº¦ÒM«¥¸ëÃZÇop¦ÔÕÚ 8\x0004
\¦æ2
\©Ï\x001f(øyTñ	:o0¹ÓW^e~üz%><Z:S¬YI\x0004};zy÷k­Pl_~¾û5\x0012\x0019M\x0013\x0002ør4O³\x0012±ò6K|ÿúüìì¤V\x0007zwôòüð«xú&\x001eûã/\x000f?Ýÿ\x001ci»\x000f¥çßÜ=~û\x001c9C¥öùåÝýÃõ¿®n¾Á\x0003Ãú-xïG-ÀåK\x001e~J\x00118:×^æ×¶óËÿ:~ý®\x0012!sþþÝ;Ì\x0015Ý}ýú\x0008ÿô¯õñ÷« ¿VX¬äüíèíõýÏW\x000fß&¸$îîÔ7\x001c\x000c©T\x001bË U Âb0A\x000f¸XÌùÝÑÛ\x000b¬\x0012y7\x000f\x0006'O5)Ì\x000f¤ÒlX;</p><p>ü\x0010ÌL"\x0016®å·«U`Y&¶\x0015:\x0004\x0011LaÇP\x0002$ ÉùU`°\x0017L+\x0018¾*¤\x0004PL|Øà¸Å\x0004·Û /ëWe\x0011ÛF0kÒ\x0008ª6UÞúÂP©fêZYÍ\x0005\x0017kåJ|éÚÂé¢èD#±y¬1<\x000bu\x0015XVØm\x0003\x0003w+ë«Ãá¸JÀ¤ Z\x000b#E·</p><p>\x000c,Xh\x0005óÜ\x0018µ\x0011\x0003'\x0004³$ú\x000f+\x0016r¯Ì*00a±yÅ°$E'0+#ï1¥²p\x001d¬\x0013«o\x000b¬L­\x0017¬BUÊ\x000cGjÊ¼dÎjÚdÖuÞ¯Füãã/·\x0007.~0ßná/ ¤<þò%Ï\x0004\x001aÁ\x000b\x0011§\x0002¥¢\x0008F:ÒýoÁyÍ·UA\x001e^80ïÎà/OOq4Ð,äÐ\x00084BÒ D3\x001bCTôÖs\x000e/b3äÐ ´A*§å!$Û\x0005ë"½MâÐ Ã×\3äÐ8´@\x0018={\x0013ð1\x0019]Õôfµ\x001erh( q*íI\x0008¨°ô\x0001!
å6,+¸­g\x001c\x001a¶³¬ò:êÚNë¨¨Ößj=bk\x0019ö£\x0011{ïR\x0008b+</p><p>Ë?¶Ö¼#­\x0010\x001bA\x000emIÛBÂ\x0005\x0014òBâD\x0019ZH\x0012°°Ú¸
âÐª´­£"EyXGfP¤u\x0014Ô´`­t=¾VH|NïÐ]\x000bç§t\x001a\x000f\x0010RZO¶ÙjR\x0000ZO¹g\x0007(]\x0010¹I\x0006çI</p><p>\x0004FJEñ¾µFo´pÉN{§;¯#ºÑÙ"Â±áuj£u\x0004K#;­MÀÔTé\x0014­(Äg(\x0005µ\x0004Z'G\ÄfJ¸ke¯¹	Yí2Ýä\x0002õ¯ÓRJP²FÈmì6¾èËÞ«<XÊõ\x0000$\x00016/¥¡ç?k °Ú\x0006\x0012®HÙ{M¢MLOV\x0000	÷¤ôl\x0013y)ÍF\x0017%'[únJ8Ý(£â¥Lm2Èm,\x000ez)ª÷x{EM'x[6ÞZ²a·qÐKQ½'\x0007NÒk\x001a0\x0006\x0008hò5©(]d­\x000bCÓeÿ\x0010¿Zù¹\x001dNÆY¨¼(sG¹§È\x0014\x00139\x0000Ü»\x001bOë8æp¦o@å4$a¯\x0016¡Ðhj}12ÛÝ89\x001cXÓûDÆq8\x0010*z\x0006nhÂ1>¬ÂÉÿâÕ\x0001»`è·\x0012´ÍaulÉ"½ôF+Nvâ$
dOé)åT)
$(Óez\x0015NöâûÁ?\x0016NdñùÇR\x0004\x0013\x000cë\x0016'»Äÿk·Î?½ò\x001fê\x0014ìÞ@ÂÛë©\x0016ç¥\x001fLx4}á\x000er\x0011\x001c Öw~/|ØFøúìdäú©¸ònäÂ\x0019®\x0004æ$¥\x0003\Ô$)\x0005`F®\x0006Ë»\x0011\x000c\ðÔ\x0004`8Ü)q½ÑÄ\x0015]Í÷U\x001bW6¿\x0000\x0002W4ùè\x0001¡hUÂîë\x0004ût\x001d¾ýQ?\x000cÁ^Ü=þq;TÆáBÈb1Q¢à°Ê¿fÐäÙ(é&Í\x0017çïÿvm*³À"@Øü9á/q,o\x000eÿ\x001c,¤#@+·\x0001ÌÖ¦\x0003Ðè<¯\x0000\x0000±Á\x0000Y¶NqUåjÀCu\x0011 ö¹«\x0006\x0000CjFNÔÍ¥¤\x0011Ûð\x001d:³Ë\x00160â\x0003SâS\x0002}\x0013_Èd\x0012aê¢[Îwèì.ãsô\x0016\x0006|8ë;ÿ¾tß)\x0011M?¸~üüé`\x001a\x0019gL^ÿ|uûáóâ\x001c¨q2G;Ñz\x001a_yÄH,'Oþzq|öòûYïµBÞK*w ÃáÈmp9\x000fis0\x0010$-.Ôq$ÛØ¼bîZåõyÉÌXïIa	\x0007ñn</p><p>¼nîYcås!0êg{,aHkÌ¢ªàæØÃÏF½È{Éç®máé¥Ë8¸½dÎ\x0006Å¬tcòNä½\tç*Ë¼-tÏ\x0002/²¡E6c!c'ñ^Ò·g#\x0007ÏgO¡;Nï:/qwoIü$½Ú\x001cðÕ${+ÊæìwÓÊùMOß<f\x0007³U*w¯@Lè\x001cçØ¥.t­hRÖfÌû)Ã\x000ef¬ÄO\x0005<\x0018å[òña\x0007G*ÿ\x0000gz$ßÕÂl~ûíú÷Ç\x00035=É4¿ººÿ8\x0013â\x0013\ÄHã\x0010åøíÔÉ!ã ÃúÕñÅwcFùúáÆýýîQ~óxõ0\x0011I</p><p>vùÇ\x0006>\x000cG\x0000</p><p>§H*O	c/SoÞ_\x001c_Î\x0003íÜ\x0019 ¸°Ø>¿æ9'¯%+xH\x0004¶gÏ<Íò Î\x000eÚ~=¥ÉGa9n½|\x0007§ÓçÈ\x001f«póc§CG9ÿ^qô%q!ÏÞ5=»àhQ\x000eWEÍÁ¢×ôn´Óräf</p><p>è×_ï¯?C;úÅãï7ÿþî¯¿¥²>\x000ce'2%¹·J\x0001ÌENX¯\x0010Ùù#WÙ÷ÿ	÷ÀÉ»Tâ\x0011íX]EEºçªµ:\x0012\x0017\x0005T°Çü4¾v­\x0016ad!{X÷\VVO}¢X\x0017`1\x0015\x001dwÁ^rì\x0011¤uïM»5Ø\
\x000e¬8Üý_Þ\x0002zÌ3ëAÝ{6nD2å\x0005ÓåxYÃ®LÀ]6\x001d¬OÞe[aU¤\x0015à"\x0002»ýG®\x0016ÐcÍbÔ{ýõËÏö`²\x0008ëy\x001fï\x001f&³¤!`WxR¿\x0012\x0015[órâËbF\x0004ÓgqÄ.\x0012Æ²Þ÷\x0017ãåT\x0015Ü~¢h\x0019\x001c´6ÃÙ&&y,QZsa\x000b¸ý$Ñ28è \x001c\x0007§¡l·²q,\x00018Ëvýõ_\x001fÿþápíÍõ·\x000fÓ©
*WùU\x0000þ\x00068ï/\x0000Å[\x0019O½¼9y÷r4­QQ=ÉZÍSI£s?\x000c\x0016nsNÒ\x0006G</p><p>a(	×õÞýl¿ì²·7_îæ~H§UîNNàh|ùÉàò\x000fé</p><p>qô|ûúô|â|\x000cßÀý=d£/¯ïoÓU2á8H|d¢,_È"Ð´Pó\x001esÎØ»Ë3¼Bæ¹öÏE\\x001aÎÙ3ñ	ËqKªÒ!\lË±ö|ÐEXÊ[ÎÚZ!s¸\x000e?o¤ëB\x001bµzµö|e«\x0015UíÒ\x0019OÙîà#Ù\x0003Ó¥Gr5Ë¹ö\ä%\"ÐÎ=&Á+âò®<®øý»¿kÏ/Y¸»bq»\x000b'PÓö¢7hØ^a$±kÏ_¶^`Í³\x0004ë\x0015¨Â;GRH(²9\x000eázpÿ|øûï\x0007û:^%º½ùpõ0íhhÚO¥
VG~Wäúl\x001cû%ßa.\x001bØ^\x001e_ú\x0018\x0015Ý~\x000fÅB:¸@¹ÚÏºHx¨¹/Ø\{²n¿aa\x0019]ð&ÉãÐ'A¹_\x0015iö\x000búHc\x0001MtûÍ\x0001\x000bé3T¹ë,\x001c[£\x0012X$¼8R\x0003Ý·È[Ì\x0017]ÌÝÞÈgPi3íZÆó[ü¶û9»åxp÷¦FR8Z^\x0013¥\x0014.j3Ö,0Ï\x0017¿üóFÑ\x0010Ç\x001fÂûÓ®£îÅÍ«Ç7×Sw</p><p>¾#¤zÏÈn÷LÎ\x001a*\x000bîUpp[Ý×§Çï¿KÊX­ºsægw0AÙæ.<¡uVôÃ`\x0002Û^(jsEIïaEwxé*¶=\x0007d\x0011\x001bøp§dã¥À\x000fBo\x0004Ø¨èØjéåXpÕÀ¶®X¸n*wÇc7¢À¶£´lÞfpûXÚ¶ç -]6Øe:\x0007¥¬ÄyliÙx`¤\x0016ÒØ°\x0016¶=od![\x0000-\x0004lùÈyElà'mÁ¶gùþ¤°ÿs(*¢Sda½0\x0014'K,\x001c]Íöä5e1Î³Ô\x0001\x000e\x000b13\x001b§\x0019dJ¬fÛ5YÌ&©â)JI\x000f%\x001eÿïMùr-lû¯#Ï©¥W_õ\x0000à$=%)ÉN8óû×_oêrÐÒi}uôêñæËO\x0000H\x001a\x0003£°ÄÊ¢\nèeJù£#l5µr\x0018­ãaão!ï_¾\x0000Æ	µ\x0001%ÕeþÉ)©\³\x0012_Có\x0019Ñ\x001e'@äàÐr'¯v{^Þ\x001aÊ\x001c$v­¥\x000fT£¬Rbàý\x0010v
&\x0015þ)1ïÿ¡ÄÏÃ\x0002æäò}3\x000c©G\x001cjÅÜv\x0000Ný~)urò^-¡àBáy</p><p>ÔkP9C
ñNî\x000eèà¾ÐA[k\x0001°Iü#·¡]\x001b*'ÊU\x0010ûÅÁË1¸NyÁjÀ\x001d+
õPY~)\x000fZr¾Þùýòå\x0018\<\x0001qÌÓñå(O\x0006q\x0000å:à¶ÚK?¶`paò\x001f\x0005|\x0007¥è­ÍSYõ&òÓmìÇ`ïaÙæðÏ\x0004õ(\x0007ÛáCsûo4ª<E\x001côØ°îÊqôèÙ\x0002Ã&õÝ½eÛ#òÃb*G¡IV¨´ZîE:-\x001cÔIµ\x0003Nj GC\x0014Å `»²µ¶û5ëË1¨Wj\x0019å»#hn2s\x0015­C÷-Ê3\x000b0B¹ÏM¿ÌgÖ8ÊZCÒÔË1>Øë;÷¯CÅ)ß.1¡p}õøûÇ(wý¿Ò+z(H¢N»ïEòwGN89~ÿc\x001eãíoöÛ§CÑ:N&¸~¸Á\x0001|÷Ì8µ`z\x0003»c\x000eµÛ©Gß\x000cÒn$hÇ\x0019\x0005'¯q\x0012ßÅû¿Mø¶;Ò½Ø½\x0014U´r7N¢,,&¡#OàÄ´øH¾¾t/\n#ÕY\x0006IázËÑ\x001f\x000f´0ÐÛ­é^ðÜúës(\x0008¿~.
Â\x001f^Lá;öäÜ\x0001º\x0017I·Ê#ÑÖÀ®·H­Bq¬|u)çýç¿ùº\x001f¯<\x000b>ât¯¯¿°Fä¿ÿÏ«Ûk\x0008l\x0014¸0É\x0011Î\x001a\x000eaQ.Gv¿¦²¼\x000f¾Ç_oÞLäåñÙ«\x0011X{÷øõÏ#gy\x001cæ¹\x001bÌãXcCq\x0018eëLj<¶¦\x0003§|\x0016òé±_\x000c©"ËÝx)è\x0002
\x0006l</p><p>C5Ý6CîåîZbEt\x0004é¨"</p><p>ë8XÔcÕÍO¯¥Å+\x001aï\x001cv+ªr\x000bT/Q 6Æ§\x0017RKÐ­iKB(i!Yw\x0004 åHö§\x0019òée´\x0018R[ª\x0016ôÂSd"\x0014b\x001c-þ_Æø{üí\x001f¿èÝÜÞÝN×ÀàC¶ÉbG:Ib
L\x001aOÅÔ\]pöúìülìõâ³V¿ýëcuÉ\x0019ÊRÊ\x0017w_¯¦ô÷P8ÎÐÓ\x0006Ç»Ì81"î]7ä\x000beÜó7Ç£\x0002|\x0015Y>\x001fdÆÒÖ\x0008_\x0012Mõ¨¼f:ÆÐIöíã£ýòuäÇ|qõå\x000b\x000eáº\x0007\x0014JåÑC\x0011õ\x001cQä\x0011÷[©·²\x0013õV/OOq\x001a×ÅØOZá=­YW\x0012Ýø¼ÃÅ</p><p>Gx+ëÆÊtÚøöK\x0016ò\x0008\x0014Jbtd\x0003¢$=u+gìxµÎ,à??ý®Õõ\x0001C\x000cG\x0015®I28\x00118(µ=iIeâA\x001a
cðgp,@Ú/\x000eEòZÑb\x0019+-\x001922}dÇÔø\x0016\x0012í«=Î\x0012Áÿ£çb\x000c#±.-åäð#ú%ök\x0014æð4Ò-â\bê°Ç00*×¹h_àqHbò2Z#x#Aç_ÍÄEö+%f×\x0008ã³\ý8¼F«\x0010`F0\x0017"í:Î"¡.4Åd(fm²¢#Ï3ÄÛíëðåÛÕ\x000b\x001eë}¿»¾½ù×¤½Î\x0019\x0002R\x001d0,l\x0005N$;áÊÜXéûÝÉÙëÿ\x001a7Ø\x0015Ûðv_Ê¦¼¤UíJ×\x0012~3\\x0018©Ym\x001bÖÓ.Ó`m<	aj\x000e_0#ÉÊ#ûÒ¡}pC»³\x0018\x000e,µ§Si¶Ic}\x001b;Ü°¾\x0000îãÇ\x000föï?
²ûKµR¬\x0012-1Ë¾«§^ÊÆ=\x0019µÓ¡\x0011\x001cË}û»Òä<ÙãÑ«û«Û¹úæzºé\x0005~DêJZ)ÂfºéµÂú¯C¹²÷G¯.Ï¾Ëõ7'cÝ/\x0015âÀ{mAÄ</p><p>\x0008ª!Á2VªoÑ|\x001dø·*H/AüÕÃUýá bJ,A\x00146æ\x001958Û Ù©ôDm5ÕkXï\x000e7Ä½Ïi¹Uüç·/_þ\x0018Õr¸¸ûðùúáa2|r¥¢D[\x0014\x001eÌªÒè\x0015Õ1\x000c#¨s ¾¼\x001c®~ºÿIý>âÑ¾ü|u{7ÓåÒåÉÅ\x0006z«"?1ì\x0015¨
êô¿?></p>
  
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

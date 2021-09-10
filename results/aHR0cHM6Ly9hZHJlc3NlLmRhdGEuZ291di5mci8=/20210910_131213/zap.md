
# ZAP Scanning Report

Generated on Fri, 10 Sep 2021 13:06:14


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=>9=8=~·8{;!\x0013?B²üGH¶\x001f\x0001¯ä\x0018¬ÇÎhT5ý±ïÐÿ\x001bxñ\x001bø>~¡Z\x0004\x001e=\x0015\x001dzZëì_ _ ö±\x0004)@\x0005Ä­$Ó5ÏW!fÿ\x0008Yü\x0008¹\x001f\x0001bÅ\x001cÏÚpï³JVïø9ØÔ²|\x0005løoqÿp3¤©_ßßí*©s^k|¨ÑÞ+z¨QÎàc9Ñë%ðóðï )ýúü\x000céçòD%s*ÙL¥0¥½I\x0005ùÊá\x001cÞzz T\x000e¥Z¡¼ÅG\x0008Ã G\x000c+¾%uø2]µ
M£Ò9n¥rPd\x001aWÊ¤\x000e\x0000²lðÆºO\x0006er(Ó\x0006åC$\x0001¾` \x0002/2Z\x0012\x0015¯êg¦QÙÊ¶RÙÊHåXÀæI\x001cU	iP>òP¦öMå`òlìÕõ´ÓMe0&A¥Ä\x0001
\x001e\x0012Û¨´À(=¡0`(\x0007$hÏê(}\x001a\x0016/°x3§Ác\x000cj.<V)Òl
mZÓ°
\x001bÊ\x001b¨çáN5ß!8$ÕVkÓjéêæ>
«0¢¼Ñ\x0006ihü\x000fËyÄr©\x0016©ª@v\x001aVaFy£\x001dõ"¸	GOQ¯-f EØnUX,Þj²U
TÆ8g$bùªìb+V\x0008)øZm¤áEço1þüçÇåír;
Vd¦\x000b³JÕÃU9©51\x0004\x0015Ç/\x0017§\x000bD\x001bþç:ÈùD\x0007ó+>µJS_rà«â¶&>óÉ\x000e>íH»Èz,ÂWÊÉp²z¤iÂÓ9îÀ\x0013\x0006*í£°Å¨B)µR\x001aoëÂgr>ÓÎç`D\x0004Nóc\x001e4\x0013E>3>\x0017`Oþõæç/·¿.ñÐÑ¶üzýp÷	
%>ÐÉ\x001fÞ<<Ý|r 1LE1¯\x0010ó\x0008átÔJÕá\x0016%ýB\x001c¦1\o.®N@\x000fùt\x0011"è³WcÕË\x0005BØöâ;#-¿\x0007ÂçßÍ­ü{þ!þÏÿúßÛ¯\x001fý}B;
Õä\x0003E¸û\x0018J)ë\x001c\x0014!J\x0014\x0007Ó\x0017ÇoÆæo\x0014\x0018ø1¾7\x0006~ïñå×¯\x000fMþQ@KüþóÏC\x001fûæÁ\x0005dVí°3X0ÄÃ 8Í\x001d©Z\x001aYl\x000cP\x000e?ýb´i½ Àoò=(`øËÏ\x001f\x000bKqðrù´õ@\x00146\x0014äÂH
\x0017oµ*Ü$£b\x0016B\x000cÓVäàåâjÛ)É ÈV|{?î¿|ºý%[7÷O¿Üß~\x000cmñ[Èp9\x001cGö8mLÃHd\x0004oÎ¯þýütüKd\ï÷÷ÇÃùÿ~ÿýêsSùæÏÞ\x0006\x001fú0n\x001añx~ \x0000Ý2\x0017	TL\x0019\x0004\x0000?T[$ãÓã\x0017ãf!\x0003À\x0005ø~\x0000Áé«ï
\x0010b-ýí\x0001>?ÝÚ\x000f.Û\x0003GË§Ï×[ö`¸îØð×\x000cfÀ1}\x0008WVå¬Rä:8îÂ
\x001c-®^\x001foÙÙß\x001fÏà÷ûûã\x0016ü~Üßïï\x001bðûýýaÛoþ÷ÿÆsîk¾ÿ\x001e\x001fïÇc#\x00186È1[ïa\x0012Úà\x0005\x001däM¿[eóówtuy¹\x0018ó(þzÜþßë¯ÇÝÿMÿzùËýûe(ôîæþéaùaK\x001câ¸Í8\x0001Þ\x0018Óh\x0001£\x001ev\x0016¼;9¿ºXü8\x001ed\x001c)\x001aúÎ\x001ct}úÞ\x001cÑ(}h¾?G4RßÃþ0Hd|\x001f\x000eñUÿýo+Ïíû§ÛQ\x0008(\x0017±8ÀIè\x001c
«T¸^¡áPÚ\x0015¡+tk_Î(\x0010ÒýÆ\x0008ÿõÛÍý¾vûéæöf\x001c\x0001ÚbrÌ\x0005?*¡0\x001c'N\x001cÑð°ªJNNO&!¤Uø~\x0008Éf}c\x0004ÿóÍû_?d\x001fâõòû-nÌKè{\x0018\x0008`øc,;\x000bA\x0015HàüÐoB\x0004¯\x0017ÿ~~±Åe\x0000ñ3|Gh°¿5@\x0008\x0001>Ø"ýy}pº¼ûpóç?Ç\x00105ÄÎPÇ\x0019w±BBc\x001a«<´0¾È2A×ØÙ[öA\x0006Aùï
çáûB \x0003ÿ\x000e\x0010üMsï\x000bûx÷åéúý§-&\x001afDÆd0hß³h¢5×\x001e/·¦´Ðgo¯^M! óøý\x0008È:~cìï¿þ±æ¥Þ~ºÿ\x000c&\x000fãVÚ0;\x000cG\x000cñ\x0003t
Q±\x0010#D
­\x0019é·¯Î_Ã;ÉÅ=Ñ$õ,hïú~4æã¯_·¥
ýËß?/\x001fÆÏ,¼òÆ3+4\x001bj	àÌ\x000eMÑ*xeÏ\x000fíÿ\üåõâb
D²¡ß\x0013"ÙÐo\x000fq÷ûçÏdãøñËòæîãøÉ)}C'*³(ç¦àÖÓ³I8¾|»89{9\x0005 ~o
ðÛ/_ù¯E~xùaùðq¹%AmBh§Àµ\x0003j±ÂãU\x0003\x0000çÉÉÅñì\x000cûúù£Së\x0017»;\x001aÙ\x000bj¨fwLCÏ¢ÂvÏ\x0014­Ýw^mÑ*0²ËÆ÷ÄHæê;`üü;^\x001fåtùôp}÷~KÔï Ì{Ó"ÈàÖ,*wà"Ö·g\x001c§«ã³£-\x00063\x0003Iå»ÜÇ¯ËÜT?ÝÜ~ÚvN\x001cHt"|ÌØ¨×QÆBË`Ïò`ëüêäôÕs\x0001ÄøÖ\x0000Lüö÷åïå8Z>|¸¿Ûv\x0011d ª\x0012_\x0014CÈI`³uÌ&ûÈÚæ<Z\üx~¶åSd iO|\x001f¥õ¿ñµìÀòã})¹
«\x000e\x001ecáQ¿QçKk¦­/!~Zê\x0017\x0000«ÜÀw\x0002Xe\x0006¾%ÀýûÇ³O°xºû4~)6<~­\x000ba²üP\x000cOý\x001a&k\x000eg\x0002ÇÕÓ_\x000fÛ[®ÄÙß\x001e×ÿþíè¼¿+Þõ¾.ï¶e\x0004åà!>\x0001RÐv\x001aÏ\x0012Úägàhñnq6
\x001eö¾-À×¿ßð¯å\x0001|µ\x0004¹¶w7\x001f¶Å÷ÚKoÃ_=<s¸\x0010W\x000e¦Êy\x001eÛ\x001e°zÍI¼ZTÛ»W[cü\x000c*\x001dÊï\x000e%ÔÝ§ÏÓì×á >ý|ÿô0\x001al\x001a\x0006jR6¦7Q×\x000bZMñsI®xq	:\x000eõêÅùÕÅxÀÉ?}\x00117Å¦}ø°¼¹½Ýrl0\x000c³Ü:\x0017Ø°mÂnÂ\x0002\x001dÅl"\x0018îÅÉééó3+ô]å__°¨ïúzùxðâúáËx½vÞ(²å8\x000c²1¹)=N9ø¯Êój\x0007//ÞæõBë\x0014"§\x0010ßKS®\x0005[Ã]\x0000²\x0018C¯àËåÃ\x0003lÞ-o¶á#Åqwáh\x0007Ó\x0016ï\x0005N8/\x001cmW\x0004]o £1´\x0005¾\\\Àö\x001d<\x0012 È\x0001Ås\x0001dU\x001fÑÿøÇZ½×Ãò.:B\x001dqXÀùó_oîP)zÀN)\x000eï\x0014F\x001aÅ.oPe¡Ág\x0016BØêøÝÉYÔ~uW\x0017³Q¿X\x0010­¿¾+Ñ/Lúß\x0007"(^Q\x0006cß¿ÜìFòLÚXén\x0010\x001c;gåP\x0007\x0000L0\x0003obúiñ·Á*nîG\x000b«\x0014þ;Üm¹J¯ïnÃ¦Ù½L^à[QÐØ¢\x0004w­Eä\x0015Óëó«Ó°Ã6C9÷×XsÿK#JJã\x0007þ¿ïïoo®\x001f>?àÏó\x0006\x001e\x0007\x001fÿíry»|\x0018àÂ\x000eã¶LX#Ç,ò\x0014aÕ·ôp\x0003b\x0018í.Â\x000eÿ·ËÅéââr%5~yp|t~\x001aG¶|Ie\x0005Ï\x0012K_#åW\x0017üè§"	óø\x0018¢h(x?\x0002Ã¶Ðib'Ü\x0008\x001fû-ÂÅFÄ²MadË[\x0012BÁ{\x0008­¡äý\x0008,Ü\x0014<,á{®xX_÷¬ð~ñÁÆÝæÕ_i|ÏË\x0010.ß~Xîâ\x0003}Þ8{¡\x00079L\x000bôÎp}6í¾«à¼Þ-N\¯Þ/÷ÿxxÊ/P_¯ï¢BÀ 'ÿ\x0008b%»ÏÓ(PÂ\x0010Ã\x000egDÆ\x0001£a
«ÏÈâÝñÙUÔ\x0006\x0018ôå/A­dË1Y¡Æ\x0012ÿ+Pc\x0015Çÿ
¨\x0010Ë\x000f¢¡ÿ7°5åÏz]¯?Ü>Þç\x0017ÅÝ0Þïàòéöö÷\x001d!Ivetw±&Ö{ÜjQ\x001fúÅÙ0Úïàòêôô/?¼¿ÿüù)Ä1øÏ5\x0015f,¨ä\x0010{\x0001r6æÐÂMÕÅ£\x0001K`\x0008=\x0003+\x001aÉ6,+\x000fe¤eT^áÄ\x0008n²s©¢gi£"V\x001f±´
å\x0001KÄ.¹åqq³°Ð\x000e6ay\x001eÕ\x0013\x0000KC\x0004;`\x0019°0+<\x0003\x000bm^\x0013\x0013ô
MX·\x0008\x0015Ë¶Â¾\x0002]¸yLÐ·Í\x001bO!H<A¸7\x001cCÍÃ\x001d1b9\*k}ß)üå7yýó}f\x001b@\x0016ìÇû/×;\x0015EÊ®ÁtqH&\x000eÁ
3ÉtÙiÐ\x0002»8?y;r=+â^VHÁ\x001a»çDûéY1¡\x0003ÿþLöæ·'þ9Ûào\x001f Kô¤ÈO\x0001.fB·[\x0005\x0003 ?È@-hp8%?ÈkÃðö\x0002\x001aH/Iüt\x0011H!7ºù,~þrÿÇ]^\x0018w\x001bGA£û§÷w_v_\x0014Ù¡\x0015ñ¢\x0008oótQ
/\Õ¦5ï<j:GçWG¯\x0016goGW7CÞòù#ÿö=Ý!/¯ï¾Ë÷\x0010¹]Þ?=¼¿Þ\x0019µiã\x000eã5\x001cþÕ².ì[Ü«Âc¾%G½<>{\x001bîÞCÔvy~uqôÿ3÷.Ëq\x001d»÷«pÖ£ÃÈû%4*É´L\x0007%j¢ãøLv$Z¢M2EÚGý\x001aýzý$
d\x0002Y+«V­Ê\Uß·\x001dÝ^Ç\x0016·­ò
 ?¶EñÑ¨¿þÃ×´U·ËåÓÇåÝÎå\x001a¢Ë9C°\µÎr°\³X\x000b¬V§6Wëª¿Ûåâêåâõ¶u: [\x000b¸´ÓÜY\x000bo3Ú#\x001dy\x0012æ}s®gà­EZñÉÍ¢\x000cV\x0000\x001dÓV\x0017lËõwö¦£\x0012¤^º(BÖú6XE²	Ï	¶\x0005¢R³ñ~}ÿ1üýuøZw|±üüåè{ðoÞïÂÄ6ëY]XF\x0018L{\x0004NyÚ#°\x00007)×\x001aN¾X¼zsô=x8[^Oj^X1q\x000f^\x0001\x000eÄk³:\x000e\x0000K2\x0001xsÒ÷áEU!ük\x000fàkÅ\x0001\x0018\x001f3\x0019Ø{\x0002F5Ç\x0012Ã^mh;­¡NO\x0012å¶Ò»Ç4p&¶#N[?ñøüá8Wî=rÿôõñúq·EbÁ\x001fÏ½_¤/^SÆQ¸ËL¡¶q~uùöäíu¢¿ùßíõÐ5¿yÈáÂû§\x000f×\x000f;G\x0014ü]\x0004¾
ê\x0016s.\x001dTÎ\x0011oåô"\x0007\x000bÏ¯¾;¹x±å \x0018{ÞI¦C\x0016¡C´7{:¥àb´8â ÷¢å3ª{Ð\x0003ÐÀ­RäâI>ß]n>¾'\x001aE\x000f:Ñ`\x0016\x0015¡É@{:`éÞÆûh&Ú»ßäã÷CO¯t[~{¸Þei|íÒy;Xzx!au.åfjÕPnñóÅÉvl@çóH§óHFNò?L>ÈðnXñÓýM\x000ebMÈNÛZ¢¤Sîhª\x00148Z©÷`M\x001f\x0010üõõÓùibÈa=Ë§Ú?\x0014.¯¶(\^pÿ$8\x001dï\x001eõ0ýqõ²ÖÉîí\x0010s.\x000f»XÀ*)pk³$\x0000giømO[hÀØr'¬àjg®\x0011\x000eî(\x0012}Çäö6:\x000e(å\x000eÍëMw³\x0011N|ÑwËÏ\x00038Ø¼½h\x0008ØÈ$\x00026"'\x0010Ûæ\x001d!jì\x000c¹:9z{~1a\x0010
xVÁ¿ÿ ÏÖ¼ÃÓ,7\x0006¿\ÞÜ=^ÿ×÷÷»\x0002·*\x0018\x001f*à µ1·\x0006÷ÁJòÄ
f3®_.N_Ãûýù\x0016A\x001a\x001eÄÿQxwâ×_Ô»ñÑû¯\x001f¯w;ñÀ\x0013Ï¢³Ø¨yÕlk-7í¡\x0001ÞÑ'×-xÙyü§âq÷Å÷øñ¿­ø°&þþéf×e óÇô¡-EWè¨Ø¾e	kãÏ¯N·å½ÉßÞÅ?¿`\x0002°µàS§Ï«åçë_ì)	(7\ÿ½|OÙeÖç4<ç°\x0007qÖÉV^ë¬ÞêÙE9ýéä\x0016/½Z¼:ùqKþB\x0010\x0010!4!\x0004oE\x001e\x000cm&p	´\x0003à\x0004üÞé³\x001bÀÓïî-5RÞ
K¿½\x0013³\x0006ÀaW¸ôiøýén\x0003(Hë\x001a\x0010¨LÏ\x001b\x0002¥ÏnhsgQ\x001c\x0005X*#\x0004Áà(­¥\x0017\x0001\x001fUÓg76)ì`?\x0004êK£¼ ÝûHý~û	0\x00151}v\x0013`k¸¼\x0017¬u¤d¯¼$%ôhgAÀ1\x0008McºÁy%Xù°@	O\x0004&È9\x0008\x001e¯ôi\x0006¬BF@Ù3Z	äü£uó\x0008°íjú4\x0010è|\x001d;Ìy_­\x0004ÅÓàmì@\x0010÷Füý\x0005Oè\x0008¿{´éúp	¤×Û9´
>\x0007CÁüt:7oÆàC QÔ\x001c)Áõâ$%î¦Ñx6¦O#Np\x0012\Ó\x0008%Aué`gº#óq\x000c¶AIF\x000e#\x001cã¨v#\x000bÙ\x0007Ç!ëÀ±"\x001e!5ÐpÆäT\x0018 ñÖìAãÆwÐ8q¬eÆ1©. á¸\x0003\x00038Qì«Æt,èE~jÂÑ1Ç1d\x001co\x0018ÇSJÎ<\x001c\x000cb¦O+\x000e8FGÓLE\x001fÊº	óY,^øéÓÊ\x0012©MA^ÆIZK®|Áq{àà>ÍCã
O£GÇÐ®RJï±pÐÐ|>Í86÷\x0004\x0002`rv\x0012âä¶\x0004\x0013öÂqÓ¼p@%q\x001a\x001dÔÏ£#U\x0019\x001d­ö8-ê
§O+ZíòHÍ{\x0001G;\x001e\x001dm÷ØV\x0016ÎôiÅ\x00111e!Ëñ8:¹*\x0003qâ>;\x000b\x000e±géÓ<Y2KZ£îÊò\x0010cig)kô|\x001c|é}>Í\x001bÝd\x0017\x001c\x001dyìh2Wf¥ã0P>Í·§Ê§88>wÄÛSÁñ{
NDø\x000f\x0019\x001c|/MV\x001aÒþÓà\x00182\x0000ñ2wtE¨@\x001eû<\x001c<ÿ\Ï!¨ENÑDxì	GC0¸=®\x0008ïßéÓj\x0007¢YçÊI°\x0003m¶\x0003]NF6R\x001b½ÇÒñhVø\x001e³TÇã<W\x000e¬|$»(\x001c-dlh6& A\x001a:¬ÒT\x001cd\x0017©mÄ=Fg ¡pÌïîîGô ð&§ÛüùÃýÓ×¯\x0013,VbSÀlu\x0005arÄ\x0006/ÖX__]^¶àÐ¸4H\x0013g]ðÞåÄY\x0019¬´d¬ëû»\x0004c\x0013¦yLTÈOqLlîö\x0008$J3Úv\x0012">­$p²\x0018YÆ$\x0015\x001dH<o\x0014Z÷_ÚIð¡Ä7
¹ü\x0001ÆDRW8 qIX.t\x000e	îäÐ<&NaßÇ<&2\x000b#Iîx
»'Ùc"ñv¢yP\x0002­\x00128â"qD¾\x001d©Ãï<\x000e\x000cÉ¥O\x0013\x0012T¦C\x0012²r¦\x000c«¹\x0011\x001bÇ[\x0007	Hóq¢\x0004á}ãd\x0008<"~þÌ` 8}Ú80RÒ\x0016vtÄ\x0006ñ\x0016³\x000f\x0013>¶ôí("E!×#4Â~­5~öì(t"hFÁ\x001e[\x0004ë\x0017ó\x001evì	57{\x000b«tét,HÜ\x0010&Ë\x0012[,Ñ\x001e¶1ÌGÁE¢ÚW
Í+\x0005\x000cüf\x000b(Aéâ}\x0001*<èUói¯À]y~"\x000bàÊàÁ\x0007a8¥à5>m(J\x001eÛ¼h#& è<*:ÒZ\x0001+f>
\x001eõªù¼WV²Ù\x001fµË]\x0000Å{ ãæ¯\x0015\x000cx§Oã¨hÜ5	ÅP_F@\x0001ëPììóM£q­eûN¶¹Û\x00018G±»à\x001cY(p\x0019îAb¤ãÄÏò3@\x0002×±àC¯cÇ\x001aYsPÐdÓÍv\x001b\x001cYÝ\x0004L{¡(\x0008(4;^Ì7e5nbÝ¾9Ð\x001báâÊÚ3¸d9\x0004äsËóY$\x0006#Ól¢(eóË!n*gw¦%Ë(nþñ\x001e=nF1ÔíØE\x0014	åú¡\x0010µ:g£$\x0003¿}¥(CÖlD\x0007H:\x001e\x0015:S|t³Í\x0003òaÚ'H¬¸
(0A¼¬"g0Ì\x001eËÝ¶\x001fùF\x001dt¤D¥T1"Ës@ÜÃ´ègØvg#\a\x0004(Ú³ï¿\x001e¥==\x000e\x0017k_)Ês°Æ5R¬\x001b\x0017-]ÑÏ\x001fÕkãJ±ôè\x00195\x000b¡áJ¡E\x000b§_ìÝ?_ïþ~ònÄd\x0011þ\x000c\x0018\x0004¶\x001cFLÉ%\x0015\x0006DÛ·\x0017«ÿn@(u\x0016M\x000câ9p%{·Îà6¢¶­\x000c\9±AÀ\x001a5\x001cáJq
\x0004vv´Ý0KÚ\x0018\x0014n\x0013å[ L°\x0011<ÜÃ1CÀÿ£²ÒÌvÞ3\x001d\x0018¼Süq\x0017(¸\x0016åsÃÄuS¤Á [cDË0paVPb"g\x0002SìîIÑ5\x0019ä¯¿ýV\x0005Ó®~º~øpsý0±&ðd\x0004­KH V£R¬\x0004N~:¹øîôdÜô¤°H¤â\x001a{3e\x0012>AÅÕ\x0003ò¶D+\x0008\x0008\x0004BÝ\x0003$¸7,U\x0011MR"XM$Æó3¡BaÂ<$QK&ñk!é\x001e\x0012\x001cNü«DI\x000eN(0%-\x0013ª¸\x0001\x0012\x0013çÏNÉ\x001fi"±.Z !±F\x001c@Æ°vöHÎóæ¢rÿê$^\x0001¾D"\x0002\x000f\x000f\x000euÙ<&¡\x0004\x0004à\x0014ÆäDâ£æ11³7ñ Öâ,?ê(¬\x001f£ÍÃ¶\x0007øGr6	ÆåÓ§qóD\x0012Ó\x000b\x0018ÏR´N\x000c´³AVÑ´&\x0010¯²°\x000bh%\x001a"q¹øÜÀ­lfï\x001dí{>GÉ¥\x0008\x0002\x001b	î^8Øüì%¿å3Ý|ÈZ\x001fÙ\x0016AÉê\x001cb\x0004Ï&\x0017\x001a\x001b\x0011Öm²\x001eçÛ\x0012Ë+\x000e\x0016f\x0004{Å$®wzÞýòÙ>ý3'·ãßty;a-{Ô¦Ð,N)_\x0015Õ(KÑ\x0018±n¼¿_líì5 Q¸\\x0015Ew£XL\x0010LcâÀÉ£ÔYiÁDÈ(#\x0011¬f*\x001cÐâI,\x0018s7SR5¢847)wsÃzoG\x0019fçýg'¨ÊÌk\x0018À[Y2ÄåQaYÎhâF8­\x0003\x0005KÄé MÉµr¢\x0002§YoÄ\x0003IV	÷mó£sê?&¼\x001bÊòsDm¤
µ´ûÆ\x0012(Å\x0015fDd«\x001aH4ØÈ\x000bl'ÁÃ>}ÚHà>Ö*Hê$ÒõæÓc\x0007
zà±u#c!ÃjG\x0012
¼{ÄÆ\x001bu3C/ÜÉæQÁVGT!dn (¹N\x0004ëËýì5»*PhCñ\x001c0\x0007¿ë18\x001a\x0014½V£ÐErbéÓDâ¥Ì=w2I¤í\x0013e\x0014»\x0007
fNéØ\x000f8D\x0012òË=J£ä¢D$}âÃ|c,­yvÀ6 Â\x0001í)\x0014Ñ\x0008ÄÍß=\x000e\x000fèôi\x001bbº¡P4­\x0013p<ÄûÙGÊª¤Dx®i??\x0006Rò:Qb÷Ø<ø¯:ßé~D"r\x001f\x0001\'|	êÇ­va ³evôqÎ#\x00002`Ú<=IL}¶á\x0005öÌ7ÛKÞ\x001a>fqPT\x001e\x0014úåA\x0011ëèv\x0014Â\x0017­(\x0001­ÈL¢cV¬Äÿ\x0015I¬G­Õì}:D¤ÏÊr\x0003\x000fáö\x000f¦5ÚüÒç÷O\x000fwî&"à\x0010Ò9ëµ\x0017\x0014õAf\x0004#^w±×Äë\x001fÎ¯-\x001fÞ_Ù\x000eÇZú4¹Z \x0003\x0008øê.'Ë\x0006AI}\x0002;Í#qh)¥O\x001bÂHJÚÈ°¸·$\x0018¸È$:Êõ[#Çh\x0017Í$pzÐ+5¬\x0019¦\x0013PJª0ë\x0019²í\x001c«tÔ6\x000enO\x000f\x001c¨\x0014GD+\x001b°ïgÎGÓ$}\x001aIà÷³FDp®\x0016¼\óæ\x0006ý\x001cnkG1÷ÿ\x0006£	Sêrm\x0014e¯ÁÝ!¶\x000eÉ®M,EJ_\x0013\x001dÃâCVÈÊ,´N\x000c%\"ÌÖ]¼\x001b&EºDû"£'sòwWK \x0018qëºm I\x0019ÚöÐX¢Ñt\x0003%@4fû.ÚMcÒØ´r¸\x000c/\x001aO)~à±ñkIø]4!Mh\x001f\x001bé(¤ïÒ\½¡ãE¼n³4Ð<ù?ïÞ¿_Ë^þñ>åt?L=ÏâõCÇn\x0008.V$êèÑ!ãÅFìçÔä£¦¼º4ÒDËG\x001eæâSè8xz"\x0005õ·â\x000e\x0018je;±âæÉÆÜ[Qb
UY5\x001bo»i>üõÁ¼\x0013é\x0019\x0008µ£}Z4\x0017÷O¯©\x0015éÄ3:mo
óä
çñEm×÷ÓÅùÕ«íýH\x0007(\x0012Ò§%r×p\x001cë¼f¼	l½$/o&ÌJ\ 
ÆÃÉK·5öÂÌç\x001eØvë¡Û\x000eUH¡Å\x0016\x0016oMF)\x000bFk·~;u°¬b
m,3\x001e\x0012K~\x0010Ê\x0019Ãì10¸§m\x00012ËáI\x001bhÅD\x001d,]Û\x000bóíöÛg±ÖòÅýçwSE,Vm\x0017éa\x0017@\x0014vKRÝF2ñóWÏ'
X\x0006\x0014«\x0016»(P\x0008_Ü±~Xò\x001b\x000c\x0017êê
W±\x001d£´§Ü=\x0018Ñq·Éùi4S<\x001aq#)¦\x0019#KµF(£\x00114§pEøÿa7Ó 1V	B;1¤(\x0005¹"¬\x000f\x000c\x0017rof¥4Sä6\x0001m\x0014¡PHÅgkb#Å¯\x0014l[(£àhH!cZ ¢PÌ\x0010òi[\x00181+¤"Eä|ÇÈ«3l$s·S¤\x000b¯ÂÄ¬*)x,ôJAÏÞ%ÃÄ­\x001cNd±%T\x001ar\x0019MÙ­QÍ>4¸ÉL\x0013G0d£%]\x0019O\x0006+Èl;FÄì6\x000c+\x001c'p\x0019£s\x0008Rb\x0006u,\x0012"³\x0003ËÓTã"Eùs\x001a
Ëv\x0019vñãºùÍ¤Ïv\x000cA¥F\x000cÏ\x000eWÒ<Ê.N\x0014±\x0014¨o¼!4càò&%Ý\x0018pSvqü>ÀàrH¥Ôº\x0005ßÌ1ð%þ£\x001cº¿ÿ\x0000{üöÎ$U4ª¨	ö\x0002\x001bÁÝMìÖÑ\x000bzÍ^Ò¤\x0003çk{¹¼õ\x0002û¾mQg«8ÇÙÂáe©»\x0008©X'¹\x000eØÐ#×]\x0004¿î:4s\x000c2üvs£IW\x000böTÊú\x0012Ásª\x000bb=õ¤\x0019£Ê6ax
¬E¡\x0000\x001a\x000e­¹ÎA¹õlV·Û\x0000¢
õG=\x0017LJ¥-¯7âjÍ\x001cxðHJ\x0001Ý= ÉÀØ\x0010XÏLéüÄaÄzÊV3Çª\x0014³e<B)µó-t¸ð\x0018DÙ\x00133Ì×Ú	Ïä¹ª\x001b\x0006("'\x0008{£æîZfÓ7,­`é®\x0005\x000bëR}Ps·J§Xë1\x001e~\x0016hÑpY\x001em1ÁÅR&¬AApªÖuj\¤±(µÍBêhq2l?16ån·r\x0004Ee\x0011ü¤cGÆ)õ8Ã§Ù\x001bfP\x0006Ú\x00021!gÆªâÒzv¼ÕsOAiA\x0003\x0008Ú6·¦ZË\x0004âÍÜ«Ð+O&\x0010ÅÏ7	b\x001epÌ«\x00022{D°\x000c<}@4\x0000Bòh¢rÕ÷s7¯ÆÅ>M\x001c^\x0018i"UÇ&\x000e½SùZ{÷§ë)}@à\x0014±\x000cÏ¡±$ÃD#2wójtmÓ§Ã±ªTZ!¾\x000cg\x000e»þ¬Ö\x000ea ÙºTM(Ö!*f\x0013c\x0002/Ù\x000b\x0004½¹ôiôROwV\x0003\x0002".Dñv#Û\x000c\x0007ªn=U­Q$`\x0012QùËÒÖ]\x0015ZâÍ7\x0013dÜpcE§*\x0018\x0002T0\x001dN¦Waî\x00192(Tj<Þ
ÛËëÆ"\x000b#¡|Ól
Üt¨F\x000eLE\x0014í¤­«8úO5sAVÀM3#ÐÉÎõý\x0008ø4ìØ9+fM5SÍkÕrêzÄß÷.ëc¸\x0004fU:r\x0013¤¥
aÊ¢=#Y\x0006¢w©>=,¿þe\x0007QÜÒävw­%*ä%\x0018'JÌÎ
[Ê\x001cëÒÒ|dWÝë>Û¡\x000c*Pr\x0001¨\x0013\`¯
ýu¬\x000bíæPQ@±
EÜÉ%÷\x0008Ç
»>p5f­ÖÔOµ2àz°b-6ìJ×S/\x0003Ø {Náª\´\x0003\x000b<@ÖqÂ\x0003He%HW\x0004ôÜZ:h?Öê`îÀrJ\x0015å ÀZqøN7u@£\x0019K~úû½ù0,[,TÏ¯O\x000f×\x001f\x000f\x001f¦Àd¿ \x0008Ï $È¢²ãXÏO\x0016W\x0017'/\x0017\x0017ßí&ÃV\x0000ÏÒ§\x000bÍÂ¥;zÀ²÷\x0014X\x0003Üd\x0004ç·ìÆ\x001e6-Rpì\x001fÉ¶Ê\x0002ëcSp¼§äE\x0014Õ\x0014E¥J\x001aIljËáÚ\x0005ôéÓ.7_Ã¢äºn.\x00018]§\x0011öÀ½ÿ|ýNþ>¬j.íh¯¿\x001e½yXÞ<Ü\O=cYq²^<ÖT²BDY\x001eàdGWÚÏ\\x001e½¹X^nkR4¤é=\x001c?½xØ"7d<iË{\x001b+²\x0001Ð\x0007ÀCûôéÄ³p¤\x001e®hÝÁØ9^w¢Î\x0017ð4}:ñPüt|l6Ôc°KlJøùC÷é÷\x001bwÿ0ÈtÀ¦E|-Ü^ß~º\x000eý\x000bNy@«Cÿ>\x0016«£\x0016NM¯éb8;9ûá|»6\x0000[uwj\x0007ÃX/ao\x000eÖ(á\x000b^­]ð³¸¨ã_\x001f\x0017\x001c¸\x0019\x000bkAé\x0004±++M\x001fúýuq)Ihy"#x;ÃÕæU¹?-m±ÚÁV9\x000b\x000eû=\x0015Ù5\x001e±àöçÊÝû¸£Æ\x0005ÎéÜ\x0007åúa+êêüy\9µ£s¼\x0014¿äÃÅÄ&z\x001dÔ\x0001¸PÚ¡K¦fÔ\x0019+æ:AÔ/b¹á\x0010\x000esPú°bß)Q´{"Ç
µSûoÈâÎu9Où¨ð|aZOeý¨Ð\x001c÷'£>20\x001aÅJïÈä-iZé\x001dùýÉ¨²½sÌ|QbRãóÖ³\¤vþ\x0000cFù=d¦¯(MKëÌsÔO\x001fb2
>öÙ \x001b\x0001ë\x000c\x001f\x0018®Î#ãÈAï\x0006 $\x001cìdÏq\x0016VQ\Ox\x0007æÐ\ì\x00053\x0005Â|ÄZËI[ºnµÔ\x0001öîóÍ»Ô¯\x001cógñ/ê·	`Ï\x000f×_§eÔÚR^e6ÂV\x0010\x00148¤:'\x001d¢¯\x0003vÔh\x0013eÑ\x0016\x0017'IM}¤×æÌ`#ôéDÃgªtaÂ\x0011&Yê0Æ¬!£\x00039öE+1ÅN4ã)/\x0000÷#f\x000fß95&Ëyh_ã¯ËeÀft©ÓgÐÏýÿþïÿ³¸ý{ªÃjØ\x0003jÚa\x0000I\x0003(XÖÉ\x0000§o\x000c
ÛÑâìÎ¯v\x0005ü÷Ó§\x000fÌjqé"Ê@ÏKN²\x0004«íÅ~0lÒ>`Ö>he¾¢ÜÍøÑÉl\x0006\x0002xó·Ì\x000f%iÔº\x001d¬¢(H\x0014À:9ì\x001d\x001cüdeä_x7LÛ`ùùËÑóûÉå¯¢¤s6j0eÉ\x0004ò½¥®-Æ\x0017?,^½9z~~1Ì#[GQ\x0015jEÑ,	ÅÌ)N¡Wb-Ó°EWÃ¢ÛÅG*+°Ã,#\x0002bí\x0011¦ÅT,¦EcÇ¢ìþÃ
fqpÏw!v´\x000b½,¶b±\x001dËEõ:#lÉ{I©Óà\x0017^\x0016D«n;Lîn`ðáÝ\x0011\x000c]ÅJJÝ;IÒÙ
\x0006Õb\x001ba¬ ÎI1iæpÐ!0¯Ê§`à·\x0016Õ¦Æ_\x0018¾	=\x001d½¹¿{<úÐrüÌ CäÕ\x0013$?XÉñ×«£7ç¯ß\x001e}GÏ6¥ÚÔÎ"õfUASòFÌXH¿TUcªæ)v'&Rp!¹¼\x0005S*3©\x0007\x0018S]ê¤uÑ5ÖQ\XóÛ)¾ÁíOj*R3ÔK:å\x0002B_o\¹T×§Ì#õ\x0015©G\x001a\x0007¬æ¶\x001eaÕ¶RÖ{3I«\x001dåçí(¬¡dRÁ|pqETcO\x0016¤¡\x001aÓ0sL-Õ:hmmeè¢N¬?\x0000g¬8ãLÎò¤­±)'QEÜWDU
VØ4Îû@!J½3hH\x001d7¬Ñ\x0018{Mî\x0003]]ÝtAÍÜù¥\x0005¢¶ÜPó*E\x0007@M¦è
5JfL¿à\x0010\x0016²\x001c§Æ³>¬_\x000bKÌB­\x000f~9óäGÔ¼¥Tp\x001c@	óÌEÿ?´>øåÜëP_6Ò4ÇÒÅZzïLÐÚ>1³STs£Ò\x000eåKMð\x001c-\x0013fÿ½ª8%åç:Ré\x000fÊúrEyÎ!\x0013k"góP]êæ¡ª@VPÆDDÁ	B\x0003 Ö'ª{¤:R´\x0008J®\x001eÙ] Â÷\x0018ãþ\x0017¿ª~5Óê÷mið\x000fòzQQì¿«\x0014è\x0015ªê9\x0001\x0014%x<WÎSs\x0018\x0011ÝÿøÇb¸!ªwü\x0003j`T¹B¥ôn¸ü\x000fpûããô\x0010ÕÎ4ý\x000cwzNÔå÷"\x001eÂ?Ñµ-­g\x001aÓÎ²¶íïÂ\x0002Éf4ë­\x00135VC:ÌÌëºü#Ï¾ÀwiÞþôò%Rûªq²ò¥ð5a¦Uà¢-ýäu¬vãôþ·¿­~;Óë\x000f\¨<TÅ\x0016µ= Ä\x0014ÿðÿPÒÚP±ó\x000cÿ\x001fHÁØ©
jüç\x001cªPV¿0Ls\x0002À·7Óm¼âm\x000fg\x0011+ì{\x0011Kÿz?ú\x0014ytòòìôr$¸ÇPj\x0008¥z¡D~\x001b%±\x0006/V\x001dÚÃècòN\x001c=ÄÑ8|Ó\x0018Ñ\x0003·¾\x0004øÑ\x0004¢Pf\x0008ez¡t8lpBY:y(|³\x0003eP¶wâ|\x0011@}[\x000e s[ò5\x0019ñf&7drLF³±h±s/+\x0015Á\x000b7þØ¾\x0013Ê\x000f¡|÷
ç\x000c\x0018u\x0004¼Î]\x0019)5oI!Tè²²hèâWaÐ Ö«V¨8½P\x000e1frÌ{;«µæ­L+?$\x001d¢wM)j­kXÊÉr ¸ÑÄPõIÞ{có::\x0011P.\x0013V¹ÆK©0ïµª:ÊeïY®U½ñ\x0012e9"µ¦dÜLUè²÷H7¡Hxa²*çöU¥çAU'ºì=Ò1C c
+ø\x0001ßÅj&Uu¤ËÞ3]\x0007ª.
(ìÈe\x000b¥´\x0012qÞ²ª\x000euÙ{ªcQ\x000cmAkK½\x0002µ6I38ª:Õeï±®bQ\x0013**»ØÜð\x000cYÇº¬uÙy®cë$*r2¦Ä ä\x0007=µV\x0000ÐLUë²÷`Wû_£Tæ®¬ý¬Äx~ý.*UìªódÇ\^KP\x0015;(§\x0010³¶ ªNvÕ{²K?\x000eã\x000cc#øíxÞ\x000eTµÞy°KT41\x0004e©6Ø"Ñ$ãx\x001dÂNªê`W\x0007;ü®<{cÁR×EüÎÌZêª:ØUçÁ×ôúkåR\x0012¬|a*7ËQÕÁ®:\x000fvø]Wb¦\x001c¡Ur°<s\x0016Uu°«Î]²V,\x001dl\x0003Ë² Lø,¤êTW§:,rª\x000b_bc,\x0003%æ­ôêTW½§º\x000bÅ\x0001\x0014dGcÅé$ó|RUéªóLØr^\x0010£*²(i\x000eÖÍ:>uu¦ëÞ3\x001dìNÁãË¥ªh\x000eH3ÏÙÒÕ¡®{\x000fuá8w®fQ¾¤ÙèY~©®NuÝ{ªGÉ\x0002vcá\x000eò%\x001e\x0004îò¬µ®ë\x0000L¯¹®d®NÅô\x0019Q,\x0018Ã
n¥
³\x001c.]\x001dëº×^\x0017¥Ç¬.ÆzÉéè¼g]åa®\x001eñ<¡`b.æ}±üvû4UN©
ÝÉ°¼È\x0005ô«;ÙÍðÙ\x0015J'æbÞ\x0017Ï®¶\x0017T\x0016J5¤Ts(½áwQ|w¦Ã+V´Ò\x001c\x00143@õ\x0010TÏ\x0001\x0005÷¢G¨bK\x0006¡g\x0005n¸ºÕæDÏ\x00005CP3\x00074ð
¥ùÃÐ\x0012\x000fçH)á\x000cJ;¤´s(#}À$ÆK6÷eÞ£Ü´fº!¨µ@mñz¥åHfÉÛ\x0000î \x001bÉ\x000f9ý\x001cN±òÎa}R\x0018Ø[\x0013ÊúÜ¼Ef!h\x0003ê<ª~dPÁ¦]P±vf³Lr\x0006h\x001cÆ9 Òrv	êÍ_Þ\x0014iÑúA\x0007\x0001H<éÅ\x001cR«Ë!*Y÷+\x0004ÉávûC,RYßI³.%aË¶ÏÕëy²\x0003¤8Ä*Õ½$g]Lklàò	ÆT¨2¦qÓVAZ]LrÖÍ$¨ËJ0VrË\x0017ÏÙ\x001aðoMh\x0006hu1ÉY7v%¤¢©ÑHðEnü Û^V7s5©\x0018©ñlÀNìl;\x0015éÚÑèë\x000cÒêj³î&°#GdW6Éêm¤¬u\x0006hu7É9Ê>`\x001eRM"FÁkST\x001eä(­.'9ëvRë^M~ÃÌCÊEüJCØ%²ºäë	Ç/|´QX#Ìk%m3AUu;©Y·ä\x00172ÃÃÜ°\x0018\x0012\x000fa5«êfRsn&\x0015VÝKäau§ñ<Ä^RµÃ4ëb\x0002.PÉ8xL¯P>î­=\x0008hu/©9÷r¥û­\x001c<mòÞ>\x0012AZ]LjÎÅ¤b(\x001dJ0Q\x000eüòkF3@««IÍº¼(r\x0001«¨¶\x0017G¤¼9ÈäWWs5aÁ-÷mðÞU}I Ð#ê\x001938«IÍº\ µë`X-RöïT<õ¤ªIÍ¹Ve °ï#§e{<h;\x001dfV7u39bAÔZ®ÇòÜ\x0013WjqÙ×ÕÕ¤ç\M*è2¦ª\x0013½R|=3Ì ­®'=ëzr+\x001cmÎ$ÏcÊ\x001d¥ôa.R]ÝOzÎýëT`PÁ*\x001d¼â­\x001fÄ!\x000c(]\x0007ôæÝO_Ãð\ÞºÊæC\x0011ÜCV÷u?\x0005Ö[\x000fVûÁò\x00055¦,5´º ô¬\x000bÊI~Bq":¤\ÑÂÅ\x001aöCV\x0017{A±\x0019ý\x0016(º£À8ó¤«+JÏº¢¬£Â1gJm³+Ê´:Øl¨êÒón(Í\x00013lUPNSîM¤åH"Ç\x000cÒêÒ³n(«Ùr6­\x001fTÑ\x001ds\x0008ê2ón¨R/n£àD"/\x0003K\x0003	1Í ­n(3ë*©.D®Äuû\x0018e\x000e1ù¦º Ì¼\x000bJ¢êB¶*é\x000e0¤¼¡¬?Äijª\x001bÊÌº¡*ÊâØÆÓ}8ÅX{eZ¿9Í»¡\x0004:­WËÔ³ÂÚa\x001c\x0013SÝPfÖ
%ûìc÷\x0019~À" ~$[i\x0006iuCY7\x0014\x0016\x000c}bEÉ¡\x0017Ü"Il¯\x0019¤Õ
efÝP²\x0014·z_j\x001b.âéb$Ý\x0006iuEYW×\x001c4CIÓÈcÊýÍAS[ûvVÐ\x000c3yò]ê±\x0015\x0003Ç$8Û,S[\x001d§vÖq
	\x0015Å¸ KúJd	\x0006#ã!&ßVuHÙxLI\x0011°¸\x0007\x000b6Rä1=ÈäW;ßÎÚùvuî½O\x0019%cÐÆ:Ì\x0000­¶µLy\x001c÷0¸ô¤ãâ§	#Z¤ý¤®ÚOn\x001de$\x001e&R4©\x001c'¯{>¢ö
F®IY%èúþ×ÔëtR\x0000\x001d5ãYÙ\x0015·?©áÊâãQm ËÔòtBÿé\x0011H#=tìØP4­d¿^«Qñv8]
î\x001c:¡ø¸´¡jÈ\x000fLzMC²ÎVt¶N\x0000&ÿ\x001d. òßWmkdØo^C5¯¡o^_éu©\x001f4_ä\x000bç×_¼}VuË@)ÚûÉ.6xùe%>\x0017=¿r¡ôXÖe7&F¥h/ÎO·7fa¾AÔÃSÔ£ÏGCïÑ+Áú3ËÒ\x0014¶\x0007ÚÏT|f\x0006_$¼Èf\x00149R¨Ø¹\x001f­¦×vOo¤°&ðY\x000ek¦WAâ\x001b­àïàó\x0015ïås®èeÑgFC§w¢·S\x001b_5½\x001b=vñ)}ìsÿco=ËÉIÅ»c=)±\x001b/Tx¡\x001b&£G_Gxù¢\x0018½4ù¤¨øR³Ö.@MU"Ñr0KCèÊ¬;.Ý|²Z~r£áÙ.>ÌèÉ¢¨\x001eK9ip\x000eÒ£
'\x001d|õé"{Uï³\x00180\x0001\x0006pÐ*	\x001bt\x0000Öçì>`ð-\x0001\x0005Gú á\x0015\x0000ÜÒÎ¨\x001dPÕª\x00130rÄ¢» ø	J5u×~@W ë\x001dÁ¨¹-O\x0010óË\x0014«Ï\x001aeg_Àz=\x0001RÛº%àåÝãòayw7}o°Ã(Õ¡Lw\x000e{Ì)âñ%øbñúíâbñúõÉND[!Ú~D\x0005Þ\x0007=2\x0007j¤\x0002NR©Q
£zz=6È
1È^FÏ\x0017\x000c^Qw\x001c¸TøA\x0004þû£]	\x0014%Èªu`\x001bdpÜ¬\x0013¯æ¬ã
®§¤÷%ëã¾nð¸Åü{!áLá\x0017Ð \x0004%¹z\x0014#HmÇ·t\x0007¤©V¤3ÝKÒ"\x0016T q{¸¤9\x001f\x0013\x0015ëöRÕ;[ªnJAº|øàÉ9ñZ^ä[ÌÃ\x000eH½\x0006©g@ªkj!¯\x0018_´}ÜÒÐ²Ñ¬1öO7ÜìÇÔ\x0007\x0019Ü¨Óê\x0015}{\x001e@ÀdÖ\x0018M7#jxQs¥(4\x000fn\x000b\x0017}-Æb\x0007¤]\x001bÈþ£\\x001aEÚ\x000c0Û<\x0002\x0018IU¦{ïtk®\x001fÒZ*Ò)zä\x000b'ì=q1ö3JOq\x0008F\x0013\x001fåªým&Û)ÕÚÞVý{[8.í8óÀ±°c=²¾\x0015Ó?÷QêÔ>²\x0010\x0007sû­ûQ\x0019Ü\x001eJmkJmû)M`gA
ö\x0006½\x0000'O¡½OJcuEÿÜI\x0019°Ç#\x001dAQßdÔ\x0019â³Ò
uöQÚ5Êî±DÇÐÊ2¹<\x0005w»á±tãq§\x000eJ¿Féû)±_«^­Ë\x0004\x0019"5áe9*%Ü\x0006	÷¿«BY,w*¥×_~\>|¸¹Ûõ\x001eDo\x0002\x000e\x001c@ï,Ë'ÀL\x001b©Ý½<úqqñÝéëÈ'£©!êC3¤lý\x0016Ë\x000b)Ý·ìHù|\x0007\x001eé.2St\x0002(¯ÒÎ¯\x001e)F^ÑzÐÌ\x0010Ít¡ÉP²zôJO\\x0019¿\x001f\x001dÙ.2ÅaÎ¼ÒX\x000eH6R]Ðæh®\x000bÍùU£7ËÚ«\]¬ÔØÌ\x000fÉ|\x0017\x0019ö(¦>²XÕHÏµÊ\Â1aÃ\x000e´8D=h2\x0016µÔV,nc/´Mhn½{\x0013\x001bo&\x0017ËowËÛ\x000fS}zG)ÈtðÂE)\x001c÷§\x001c'%ýöÀðÅâç×³ïN§ÎÞõw'¹öîÔ\x0019$»%\x001e3\x0006-½î\x0004~=fkøp¹|xýe\x000bã @ìêõ\x0000q\x0003¤pOè|U;\x0004k-wÉr£Pú\x0006s¨Ý ëØ&P8\x0000\x0003c\x0012Í)=´\x001b?îãtÕÚÜ\x0008'6Í:ºòB\x001a{·ä läâÖgÛ¤Ûz,í±4\x001e{9æwGáX­PÀÁ\x0019ÕzþÍ±\x001cÄÃ\x0012gÃ\x0019!èdàÒJ\x0011\x0005íteÝþ ÎU øý."µ\x000e\x0013q\x0002íu~)UQï¿\¬V§sV§àvÉÑÅ\x001fÍ$øÉyÿ\x0001õ\x0003³Õa&9cæ`§Ï9:à=Ùÿ0[Lë>J[SÎYY\x00175QJu¼)ðÈGItrªz4ÕÑtü\x0012èd	\x0005a] Îg\x000eÎz<ÕñDKZN\x0015PÃ¼®áÊÜ\x0005ª«mäõ\x001c\x000bÄ\x0019~yÃ\x000cFr\x0014\x0004K`*­\x000f1ó¶\x0006]\x001el\x00025«\x0014\x000e	¹\x0012ÏO\x000c\x0001\x001d\x0000³x;gâU¥<Ëü.øÒÔãíØ:9C½Â$J\x0007B2=}\x000c%cGoOéh\x0006
¢÷ æÌ»`5Ôàùñ\x001fAÓoyïêã¬Mä9'(ø\x0018=\x0006ëÓ³á£-\x0019F[\x001ejº8e=ëy
MQP¾zôÚð\x001b\x0003\x001cG¼8ÀÖ'Ss2¹¢¹\x001e}i\x001bâ£¦Üjù\x0003ØÉ¡¶AÃ\x001c\x001bÔYÃ&Gá;Z¡\UÉe\x0007\x0018Ñú\x0008
sP«\x0012óÔÇ\x001c®ò!Ú2ófÿË3øs=«\x0013#DÄnq@\x0007_²ÍÄþ¦]¬·|µåQ\x0012¼\x000f\¬y\x0006\x0016õT\x001bÅ³@u
ºúØ\x0004*¸::|\x0018Ë¯ÈÁRQºRÞ\x001d\x0000´ÞJqÎV²au{\x001aê\x001eàÖdª0\x001fÜÇi«Û\x0013ÿq\x0006'?ËÃÁéÊÌkNøRî\x00103_»sq;gQ¼9Iï\x000fK\x0014p<÷?B±\x0012{éç'&\x0010dLmIÎ\x00070µì¶'Ð5p5[GQcPöiùx½î\x000bV:Ê`j\x000bÉ5ª¢.hG+\x0011X¼=YLõ\x0003²ëZX¶ÖÂÚÍeEiR\x001d@\x0008L&ÕcO#ídÄ\x0010[«
í&«k0\x0018Ç­Ù£dao7"VÝAVê\x001a3SÄY°1\x0019WéGVæ[ô\x0004\x001aÉ\5f®kÌ°£çÅ#J?W¬~ÙÌWd¾LEQTÁ©añ:>7[w©LõyW4/zß.¥\x001fy}h'ÕÅ®1slÄ¤¶ì²è*±Ò§\x0019Wh#k§F×±½¨\x00147¸\x000e«\x0017ÕÈò³`tìV\x001f\x001b²ëÜP\x0000@ïÚÉÒ~Æ\x00179ë8ZS×HVo\x0001Ù·\x0007`w²þ·VåqP¦\x0000Bï3h¡ÏÐ5YC8¡	G9¡ÆKMø}¶ç \x0007l:leÏ¨IÇ2Vônm(-ÊÃ{\x0007Z}\x000ftí\x0002ìò\x0010ó¦Ô9$oci ìä>hkWT×\x001dz\x0005hB+w\x0014\x001a÷K·{M¨©ÑL\x0017u,Ç£-âü®ôG7ãhõõ©ºîO	²Üd<RJ\x001089üÜ+ÜH?´v´úðP]Ä¸\x0000ÉRYrßÅúëO\x0017\x0016\x0015\x0016=dà\x000e6ÒÑðk\x0002×\x000bç÷A«Ï\x000eÝuvÀ1ô ¼)Õ¢\x0019W)jDÓ5îBsEvXÁ1BzÆ*>ÖÖ\x000bâ:ÑlÖ³Ae\x0017XÃ»)BÃ0'£\x001a\x001fh¡\x001eµÐ5jÒµ\x0016,?ê".,Æ²X\x001aÐÀÚ[Ë13Ãf\x000co\x001e®¿¾ûöxý°«é\x0008ÝSÞR+\x0016)sÇ
#ÇJäß\\>ÿùíÉÅlÖÓÌÌ°	C\x001b£ë=\x0016	YëÙZ³qÌaéAÓC4ÝæW½><UÍ\x0000\x001d§sImÆ\x000e\x001e<3Ä3xøMM?À¡CÄ\x0016Á#i÷Æ³C<Û;zûâa;(y¥&
Þ\x001e<7Äs½£gX	\x001d?rã­+'fßÑóC<ßÇRå\x001a»Bz¶EØaVjì¨ë¡\x000bCºÐI§\x0000FgèÅÒ\x0016](9Öò·\x000f/\x000eñbÿÒs4·Fñ\x001dfK?#9zOtÐ
\x001e«LÕ2¡
\x000f3XùDÖåÔ3¬\x0001\x0004£»ç±'ëû¢÷Â(	èAËak=½Hoólzøª\x001bCö^\x0019Fø+1\x001bk\x000cÏ¯\x0016û_u.ËÞYsÁjê\Å\x0004?ïI¹^±ÚÏW|²÷èSú8Ð½f5÷À°¬y\x0000|ûî^Y\x001d.²ótÁ\x0002±°
â°	\x001a%ï\x000fLÞÙOUûWõî_mJÌ\2~¥\x00047È|µEÕ»?`R)Ù\x001bÕ/U<g$\x000f½¯Ú\x001fªw \x0010\x0008í1Ç-\x0003\x0011Ft=|ÕþP½û\x0003æ7g¤"Î|\¬({þ	Å|\x0006¢\x0007âY]|sÿôË/7wÛñ<Jnè´ü\j"Ç\x001füÏ\x0008OGøõ-%ÈçWßúz\x0017\x001a\x0008\x0006\x0003Ò¦\x000b/Yw¯³B¥\x0017%-`l¦3Al©Ol¤\x001bê1 è£sÞH\x001cæ¥§$&À£\x0006pBØRN×çj<×g\x0002Y¥\x000eüìü­Y\x000f\x0004ñÂ^xZU+O«¾¥\x0017$ËÀÙ\x0018²/	xÔL\x0003ðßRæ·\x000bOú5ù²\x0014Ñ^
ÞÓÑåõûû§ÛådU\x0004V*qÑRÑÚ°\x0000X
6Æ\x001e[¯.O\x0000ðl1U\x0017á×\x0004Ì¤¯\x0004ÌÚøa¥+LX!ÃÅDÇµ.ë}n»ùt5~º{üÜ/Rv
\x001f%\x001e\x0003ß¨T\x0007­øl/\x001f\x0018¦\x0005I}©pÜ^ÇÑÊÈ\x000e>Wñ¹^>-P4/ñaÖ\x000c
\x001fÛ\x0005F\x0016ÁvàùjùùÎå'òMxÁò;	|¯\x0019%ö\x001b>)Ö¶o÷ú\x000bl8c¢!\x001bÎ«\x0019\x0015\x000bë\x00004Õ\x0000\x000ek\ÚF0\x0014DLÚ%@ãY\x000eÂøÑTÈ\x000eÀzÈî\x001d"\x0002å<\x0007íiY°(Qµº\x000eÀX`ì\x001dAØ\x0017\x0004;£ã¨±,ØiåXÚN;ª ê]É÷È3e\x0018Tóg\x0002\x001f1i1î\x0005hj@Ó
X^¸)m\x0003Pf\x0000Ý~[DÕ[Duo\x0011lj¡
\x001fKM\x001aÅ².nÔÀê\x0000¬·êÝ"\x0002c¥4¶421EªÀz³0xNK¾\x0017Ð{~SÃ/ÆrØÙ®»GÝ¡\x0006\x000c½(IAA³ÿf¸µº£F`\x000f_½\x0004Cï\x0012\x0004#u¤\x001e´aX\x0018Ç1\x0007¤\x001dO5#«{ø\x0004ë\EQÂFó«\x0007\x0018©ûYZVã§eïøiÅ
rCä@\x0010#>±ß\x0011­×Ô^+U`ø%oà¨,I\x0013\x0018Á¡q7.nÕÁWºû\x0004\x0014<¹\x0015´\x0017'×ï9zµª{mT°qY1;j\x00160\x000b8Õ\x00048ZÅÓÁWÛ¨ºÓH5\x0011Õ3äNxº(9å÷;M½yMçæ\x0005<Áº\x0018Ñ\x0016\x0017N+Î\x0017të\x0018ý¶\x0006ì\x001d?lÅLÓ[,T-¸±3j?\x0017ÎèO÷òI-c1Ø¡óöU.òöµ{.@S\x001bX¦ÓÀ2Q[G\x001f8åLùH\x0006\x000b{¨\x0003ñ\x0004h{GP\x0014\x00135ÚÒIq^¨ÛÓ\x00004µu`:­¬'o\x0018K Ò@ââ\x0016´©]\x0010Óé\x000b$Ù\x0005¾ÔÊXV 7û\x0019\x0008±ÞÂ±w\x000b;ÅQ\x0005OÙ^I*ñE;ZÒÒÁWoáØ»Q\x000c%a¢F<ª¶ò,î\x0016Ã¨¼[3 µ\x0001(e§\x0005\x0008¦¨aB°±H\x001d	\x0001ªm¤Ü/Ò!aµÔ1v\x0012ÚÈ\x0005kÆ9cÇ^\x0008\x0010Î\x000e\x0005\x0013¼W^øÛJÙáûå\x001fËéÞtË¿P¿X¶T§\x0006×àx\x0018úûÅOl8QÂ¬gwÂÁeeI	n¡æ-å\x0004\x0003ÜxÃf8[Ãu\x0006^ÒÈEAeI0rä+LbÛ\x0007NÖ#';GÎ\x001dX;xnøJGN>\x001b/BkS5êÓaä\x000cWüÀ¡B{ÖÊ-µ­põ´ªÎiÇ¹8\\x0013²(Çp[$9\x001aÙB=p¡oà°TØìª¥\x0014uu[JáÚà¬\x0006ÎÈ®3î2/¤l
P%¾W£7m3­Él\x001f\x00198\x001a*á}G-\x001aÖ\x0005Auì=Øl¨Ølèb\x001dIU\x0019NQß½(\x0002«gy1\x001aÃØ
'×\x000bó$\x0017æUe__¿N
=E|ÙÍ6:\x0005EËN¸\x0000ÓoB´âÍâòr²úÒ®É?&J³Þb7'¸Ý:A{-r¬@¨¨\x0015£Ù\x0013uá\x0003{9aV»·	\x00136®'ÙÃ¦8öéI_`\x00048ÝØS#g\ãÜ&Ú=àgíaÉáùýWDÉØwkoÌµYßÔ¤ÚiØü7d\x0003\x00150
©ºÁy»å\x0015½Óz8í¦\x0002HÃpø\x001c\$*;r8ÓÚ}r
sSXc7&xÄfÝÅ\x001cïÅPVç U#§[ãÜuÛÍé8óÄ+\x000caÒxÒó+ê\x001coí¥Ò¹¶:G\x0014Óvbâ\x001b]n\x0017á\x0015ì'Òw&a7ßÞ{4Ý ÷Ø¦\x001b¾\x001f\x0013\x00035´:QUÞeNK¥áX§9¡XÐÈ©êYwJ»g=\x0018ª^ôÒkÚE2%8'N1)¦ÒÊi×8gL;¸Ê9óÈËHO³Ài\x0018sôQ§Ò®æ¦JÃâôÒì9\x0003¥i¶·;kæ\ÛënÆ^(æ1\x0015¥`â&â]èímÅ1ý\x001aæ¦àKÃ¤[JUöhþJÞDÔÓ\x0004{O\x0008è´qúµÈÏ¸$éùèÄ$%G^3§Üß\x0000ñkËsD+m7'\x0018Æ¹\x001aÛ\x0010çà¬RSþYSj\x001a­a
3tc*áHïÀÃ}ET\x0000Ó/
öÅ\ÛD~Î&*\x0015\x001eNI>âSA\x0018
çô\#çyìûÍc\x0018NA9\x000f\x001e<,@0ÝèZ\x0017f\³b¿äP\x00191\x0007	¼ö°d²?l =¤öÚBQ¬\x0015\x0002¢9ÿìÙégÄJQÇn®þ:zñézJ\x0011ßªXZûZø[n^Âóº\x0016A=}d)òøÓéÉÕ\x001f½øádR\x00148ÕSÍáíí©eEdBq5¶u.â\P=\x0004Õ3@u\x001b\x000cÎ8në-g³l\x000f\x0001j f\x0016(Ç`D}	M\x001a~ºÔuUÏ\N;ä´s8±ã*É®cw?
\x0004ZÇYB\x001ddº!¨\x0003
\x0006\x0012%êXì:O\x0003\x001a9ÕI+w\x0010P?\x0004õ³F4rÎ\x000b\x0013v¼+y²\x000e'Í\x0005
CÐ0kDå±¦\x0004n)
hd9ªõ\x0018Ý !i4\x000f¼\x000e¸Ó\x0001doî\x0012éõÍíírJ}ß{Ì¡Èá\x001a£=W`xÏ'½VµÐ$P½:}(ONÏÎ\x0016\x0002üz½â[§o\x0006¼þzôæúáþÃÍdOe]Ú\x0005\x0003{fà,\x0000ø÷F\x0001O.Þ\w:ÕVY®wMÔ5±\x0013\x0011\tJ6VR\x001a\x000fE¦d«?\x000bÑV¶\x001fQp\x0003\x0008ã,\x0016dÆÒØQÕËq\x000e£©Ñô\x000f£+ÒZÆzÌ\È3Í*°.õÞÕ8þq´¯H\t\x0007ÉiÓJ\x001b·/£«ÆÑõ#>\x0007Ü¸\x0015\x000cyë\x0005×³\x0010«atýÃè<+\x000e\x00189ñ#°å¦Ö2gæ Æ
1v#\x001aLhÌ7"¾\x0010Ð±Ã×Êú}	%\x0006;\x0011%»°\x0018Ë#(&+ób¬{¡ÎT5¤êÔ´\x0014 ×ÍÀ0ì{z\x000f^C3aÿLcy\x001aù\x00110éäGÄÒ\x0006\x000cõ½!ë³Qö\x001fÆ
®$6Á²nRÔ\x000fðµl¸9õÁ#ûO\x001eã\x0005\x001b=\x0006|ËD[óbaû~ªÞ5ª×Xi¸ï-=9+.Â­lm7ÿ*K°¶yÒ­XÙØíí~Zó\x001b\x0007+KaÉJXL­\x0005	\x0006¦#6{;Ò\x00072k>-â©N<¸ÉUn¥Õbx·¬\x0005©gÐé!î§s´KÊ#Ð±\x0013ûÒ!é¤3±\x0002¤.r\x001eÑ©µft3ðì\x0010Ïvâ9Áéò&¬ðÜà¸Þæ]µâ¹!ëÄÓ,ÿd¢/b\x001e©Ôäø\x000c:?¤ó½ÛÖpE\x0001gex+fÜwnÃ\x0010/ô.=Ë·\x001cÎ­¤aËÌnsG\x001bá\x0006é\xäÞm«9\x0013Øø\x0012Ë³
ÀfÝsåÉêÌ½\x001ex¡tû:Á\x001cë9>\x0002®É¶øÈN<µæ%§ÊløoÝ.ß'¶ç÷OøÏn®§ç·TÓÙ¸£4\o\x001dDoÎ\x0016/\x0012àóó«·øÏNO\x001a0Õ\x0010SÍÁ4¬·\x0004Gñ1\x000bÞ8ÜÙZÐh&¥\x001eRê\x0019ÊàÝ\x0007³´0²u[´®Ïéfif`¢<O1E>\x0010KÔÎ\x001ebÆí\x0010ÒÎ4¢°Å\x0001¹Ìp;Ó¹Bý\x0007ÀtCL7gÊ5çaóNË\x000b\x001cû¶~\x000fHpî\x0010lP.&Pdíaæûû»ÇíÆê@b8^\x001bÍ-L r@M	·=Ë|þúíN<SãN<«(\x000fÜcÌÎP_\x0008\x0019é¥PmKlÄs¡Âsë¯o;ð°Ï(%¦¥ö\x001ayô°r"ãaS¨}ðo×\x0002\x001b¼uâyÎ\x0019öØª&GD`)YÁL4Õh¢5ÝúàN:NïrÎU
püöoð¡`\x001f:UÓ­çÎì¢+f+àIª\x0014óZ\x001f\x000cÞö\x001dx*k¬B\x000cV\x0015=ë¹¼Ta2ª¸3,GADQÉ\x001b/#:»\x0002Çsq:©\x0012\x0001\x0007[Cak¬^@[Êdµ*úÅRÄxëØ\x000eÀA²(ÉnÂ 0\x0006\x0008%=è\x0015\x000b v»ï\x0001´5 í\x0005\x0004ó;V ®u\x001eÂ(¸ý®ÜÒ0¶\x0003q £Jö.C´dÌjU\x000e|$	If;^PÙhdhd'"j\x001diÒkÔôÊ¢4ìâIáÇ\x000bÚÚ\x0011mhû\x0011Ý1Ëø\x0007ÃEimÑÊ\x001fm\x0016ÚCèkBßM ¬\x0016\x001e©ü$J_Dß¼ßwcµ[TìÝ-¨yD²¦Ê²\x0014¹\x0011\x0004\x0017m¼f¬\x0003±Þ-±w·¸Um%VBåXHT\x001f\x001eáÈÙ\x0013q¨¾ ÖÕ\x0017\x0010ñ%dþ­ §9*Qdþ±÷ËõÍ'úGmÖ|,æVåMO¸-\x0005Í®\x001eE×=¨\Ak\x0011uö
\x0017½\x0008qK\x0019r;¢®\x0011u7¢\x0016T¬\x00100G8·­ÖÐ«£\x0008aT'±\x00031új¢£ïh\x0007Ç\x0014I9\x0006Ì
×\x00191rèPà=3\x001bÑf½¦Õ¹\x0010qx.¾yº~ÿi;1PpÎ)\x0019²«\x00019AZJ\x00163^\x001d½¹:yñÃ.4%+4%;ÐÀ\x00139ªéRrz\x0006#¹}\x0004\x001b5­ÛÀäð\x0014L¿}u\x000cî"Ãò,p`±{NùÕÜ
@ Ç\x0015,Ðô _
üç\x000e´ÀMÕ,vÅ6,FÅd£
[Ñd=jµìÌN´¨èm\x001bFÍå#Oi#s\x00022²m9Ov±uÁé@ÓLöÓõÝãÑÿû¿ÿÏâéq9%~½Ø³³é°0õãi72nfýtòúíÑwG«·)\x0005Ì°Ö\x000bI+\x001b¡T±ÝïRë°/jÏD\x001aG½ö>Òa\\x0006¥\x0004õ,T[\x001e+vÓ\x0013¹\x001aÆÄ2\x0000¨a¤c\x0017ª­Qí<TË²WiTsÒñ±\x000cê\x0016a³FR¿®Lí³2õ0nùíë×åSï-ýe}fÂp#Ü¨·fú-~¾¼\L¹õp¨^bvq\x0017!Ù³á\x0000×¥"ù5\x001fdBo·¦Ë6\x0012ºj\x000c]÷\x0018J>%#\\x0018:&kyÛkh+¡¯ÆÐw!öP¤1ô\x0012D|`¡Qµ®ÚO(EEJïû\x0010s.Z\x001eDC&¬÷\x0015>yÏE\x0014ëMqÄ )N
}½X><Ü\ß<,'ÌCØ»,D	_ôlë8|£Û\x0014OÁ¯\x0017ÓÓÅnB5$TÝ)°ÊT"!»Ò\x0003\x0004»oïM¨ºP\x0008Ñ\x0019_Ò\x001aåé{¤eZ/¢\x0019"~D_Ò½ÀQ¡^x`ysÖû¢\x001d"Ú^D,Ã%KGÐM­þ^<7Äsý#(K»pA\x0000\RF\x001aùô"ú!¢ï\x001eAÏDè9ÊÆæÖ´Cæ !bè?n(ÁÆDVÁ³0ý\x000f8äÝCh,k[|'£'f\x0005Tq¤çK'á0ÙaÐ5§\x001d\x0011{YR&\x0004ø5Áòî\x001b=Ôç0ÖJ÷­"WA\x0007,[Rô\x0006Î¯¶r¤óF/au©Èî[\x0005ûò(¢\x0001F)-;kk1Ò¹±:³e÷¡-M`
>\x001blIæã²Y©Õ\x001e¶ëÑXYGc\x0001\x0013Ü\x001fî\x001fnþ¾p\x0008à\x00044TÁ\x0010Qk1¿>FL\x0014"áõ\x001eåå\x0005íèóÓÿ9r\x0007äz°SÖÁÎfÈ"Y\x001e#\x0016tû\x000c©=k>ÙQ§¿\x0003\x0012åò\x0006I=¯\x000f\x0012.ÏoâÄ\x001dQë:CÂQ¹¥v²\x0001RzcKt\Ù¥9\x0003öý§ëûÉ²\x001fì?éH¥\x0005\x000bH_¥+\x0005öG\x0018µis\x0012ì\x001fN.Î§KrÔÎ"5bÜ^eo&\x000b ¸¢Ý ô\x0001HCE\x001afjI	v^\x0006{,¦~'¬7°ö24TzöÅÜA­\x0017I\x0006Ù0b½\x0017*Ì|\x001d\x0001Àmð¨!»·ËÉDm'ÌÊ\x0014\x001c\x0007#
J;ª}s´xýòlq1¥øðÙ}À^á»\x0000ç\x001e2p-&-\x0002á\x0012\x001fM5ó
ôo¨ÜÄç\x001c6À%\x001d:\x0014iÌâAÊCÀ]\x0018;Ó[ñÀ\x0012Õðá?÷_DÓ'\x001fèÖr[ãhYÿ\x0015»\x0005=\x000eõLð¿ëS¼ìcD?:§Â¶>NF\x0010·È°£¡ù\x0006<rÖÔàA\x0003)\x0007\x000f\x001a°_-o¯ï¦+\x0019b(¾\x0002¶MÍ\x0002ØÑIÁÝïÜxZÎåÑ«ÅÙÉëéjèy\x001bàp
ÓZ\x0010\x001dvF«÷\x001c1¼^?."Ù'yP«S,B} ¾|XÞ}bÄ´NJötII/\x0005nU(R\x001cfMH|x\x001a¾¼Ùn\x001cmÍé%¹ñlt&û\x0000é\x000c½\x0013Áb\x001c\x000fµ@
¹E\x000eNEô\x001cLÝoSÛÄúcA¹%`\x000b*ª)\x0003ðo?c=\x0007+÷çgË÷×_ò·f\x001a6!u\x0013²ÝPÎ\x0006ôñKÊ;eÄRéc¶ô¸Ù\x00055PDë]\x001dvBÓB\x000f¥)gHÒ£=\x0007ë¼\x001e\x0010ßÁ4lâöµì\x0019(¿JPKj¾ôJï]É¾WãïË» êÙÓ]³çQ\x001fEÓõ\x001fFaê\x0004«moTÓLRÖLé¡Æé<ðÇCq\x0007¼Rá\x000fJî[º\x0012Røïo7K}\x0013)É0¥\x0016j6r1o¯\x001f\x001fñåÒsÁ¹}ó°üps·üH("a1¥0É©ãÈða/E\x000e©
ôÍÅâ»Ó×ËÕßº6r6ÏNÞ¾=yöþþóç§»kþ¿\x000e(]?¥.[ÇH©ó­s*\x001bBâ\x001bë %þÓ§{,a\x0000S$\x001dµßcÎ¨QÎÉ¤ð\x000f±³£\x0017g«ÿÞ\x0017\x0013­ôéÅ´Bd£\x00040]zmN6G\x00013uº<£\x001f|Ê·'ûgz\x0010MnP\x001d³,\x0013¦àZ<÷\x00104ì²«äÉ§ñÄ4úyáÝ_¿Ä§gJ\x0019á)\x0005h·S|(	\x001esFK×t9ê¡,Üüpì-^¿z~²IwB4³]`©GwútÁlfé\x0018²;¹ÃrÑDfÃ1|Fa"`è¥S¿«O_o\x0006`*¬Ïí§åãòæãÝõÃòfr[cY²¡Øº'AMgÉéU`PaÑ\x001b®Ä7gç[×á\x000f·Ó¯O.\x0016§Û¦Yþ¼´ßþ\x001bC>ÛXgË»\x000f\x0013\x0002\x001bÄÐñãE¤ü\x001fp0Ó­«	s\x00014¯¿\x001bê¶\x000b\x000f¥õ|7Ò|;O&\x0000OÑ>1:¹ºàKRéÓ\x0007(UÞ((I¯rX\x000b\x0000ÉFFCê@ã§p(¹¾\x001ewñ\x0005Ø..ãiûDÃ\x001eqñ"ÔAøÐ¥J>>ðÏ<\x0001*C´EÕ\x0002Löñ\x001e÷>»,q\x00023aÜð°ysýõ÷§ÉmlL*ÌÊ%e1¿ÏÂõlù$ÄWÆÉðÍÉå¿®¶nÞ_¯¿_\x0001\x0013\x001bB]²»¼K®Ï\x00168å
\x0015ãé (\x000f$9\x0013\x0004n»A°|Æ,^ÞvåG;ø4f£¦O\x0007 \x00162äTa¸å¤ë88js§0%r?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=O¹J&°\x0014ìO\x000c®^\x0006\x001bE¤åæ\x001bqÞß-¯\x0013xÖò¸\x001c~ã2\T®ãeðõýÃTQ\x001e÷Úï8w\x001e&X¸Âò\\x000b\x001cèõfhp+¹÷Á×gçW[êÒ«Oz\x0002\x0017$=+ÀLw]À»Ö\x000fí-9Ò\x000c´\x001d\¯L©\x0002
\x001e+Øõè\x0002ÊÂA\x0001!É¦Ôºòú|g26\x0014c(\x0000¿ç_ï×³\x000f÷\x000f\x000f\x0013ålJYÒ16VXüËd/âôËüÝòlq9ûpv~>UÍEO\x0005¡«'TtÎ²aÂÐ3C8
z£÷$´\x0005¡­%t\x0012\x0012ì\x0006ÝRû|!½b9·m!ô\x0005¡¯%ô¶Ãð-n¼éL¹ôÊL\x0015¡ç9¡çë\x0013\x0004LEx\x0000\x00186ÿä×4òa~ûC\x0011~96N¿ÁéÓ*¸¢\x0012½¤Cøá
<¾¹}^ýº~Nv8×\x000f«ÇÜ\x000ceâ\x000b®"µ©CÙe\x0014lu\2,õVÎ%«·ËùÇÅ2yá\Ï/sS×±]í±¥÷X\x0000=O'x6·¸+Ua\x001d2ûS\x001b®\x0006ù=®Þ\x0014·Pw±zþ÷§Õýä\x0007<\x000c\x0018^i0NÖºÊ3_\x001a©>+?9¾þ÷Wçó³©í\x000fÁº\x001cÖµÁàð.+¬¨=¤5±ÑK¢jTerTeXE/\x001b\x0016Î®\x0014¿5;èHií·\x0000[:ì\x001eX¨qMå|`\x000b`HëEQÑ£p£·Õ´¦\x0008­i\x000bmØ;áV8^Ãðdª=H²6ÓÚ"¶¶1¶\x00165MÒ¸Ó
]ºãb[W\x001dm_å\x001e¿0ÕH+qþ²P"¢H\x001fÏ*º{W\x0007¢-&/×8{Aí)Ñv
Ú-v[\x0015K\x001d-Ï®ì8\x0014ÜÈÆà*µ".w°ÅNÁÅt\x0018h7Óòb$D/Ô¦¥\x0008\\x0019\x001cÈ@¤ÙÖ-ûüie1'DÕ&ZNFtPÁH-Ú4æ\x0007\x0019¸<s`¸¾q(0§óá´Ej\x0016\x001b\x000c âá ÑýA\x000bpá±m5ÓÐ \x0016OÒ\ÑÈÕÌÒÕîË\x0006\x0019ôð\x0003dÐSñÝ\x0005ä\x0008V/\x0013P§.	^s²\x0013\x0011VQ*\x001aji6Êî\x0002Ùéb~÷:È±D
#	¯%\x000eK'\x001cù\x000ehæG*\x0016	kk¯¢\x0019_\x0000¬À^=áe\x0019añ±BÊ£¥r,U\x0013-\x0003ÝKé2
ÔRÏ\x0005Ý'Ô îer,SÅÉAÝ[î°£±%JàÚ±íÒø\x001fv§óäáçµ@\x0011c\x0018b¢\x001bb#\x0005§¯Òi7Ø_jö}KÍùê\x001f«çõì¯«×?=ý0qòt\x0014µ9;8w\x001a*Ïá_²¥§æ|þ×ùr1ûëübqùÝÕûí_\x0016-8Egïö\x0016þðøæ|\x001d\x0015+^ÍÇMRÊyY
WCqÃ®|±l%ç¨RñJB\x000eÁ¤(Ààqg0¾KÏ8%àL\x000cBá(\x0019§]Y
YmA\x0010L¹\x0002\x000c\x001ew\x0006\x000b\x0003+½Óaã>Qr1\x0015®­óU	$üÕ!]¯^\x001efh\x001fw¹nä\x0012Òaùcé@ãÀæ\x0005¿	?fæ~=¿;'Ï¸Ëyß©´Òæ¶RÂ\x0001\x0006û¥ª{ïPåC\x001aÉÆ.¥7I'R\x001cÉW¥\x0008)o)¬¬©-e#éÚ9§\x001cÍÏÎÝM7ÐêV7Ñ*\x001e=jcl\x001dÙ½û0Îq\x0010\x0018?Z\x0000Ù@[\x000c\x0004Þ8\x0012 ­\x000fGBØ\x0011RÂ¸»ö\x0007?ëÐö\x0005(@T\x0004Ã¨å\x0018<ðÐ`Î\x0019åâ0°ÙõO¬m (NM²áÜ{CÏ¡ÀFEáêiU1\x0010TÛ@\x0010áh4.\x0002­\x0006\x0018Z§m\x0017Û1ã¹zZSL	¦mJ¶3\x0018g\x001a-34ùQzZ'rZ'Úh9Í.\x0004\x001a'T¥\x0014b«Æ4#+\x0017\x0006W\x000c\x0003×8\x001f\x0008]\x0010yÖ+©®uÔú´:®|0yµÎ^Ê¦4ÐäÀ´óÝyÂÑ!h-+§Ú¶	A:ç\x000c\x0007÷\x000c\x0016/8Ã*AvÔÁ³\x001a×Óm¿¤r4j!º\x000e5¢,µæ\x0019á\x000fòqæ{\x0018ß0\x000f}j"\x000eû|EÄ\x0002\x00123IÑè\x001d¨\x001d5}g»\x001aâ®\x0010W0_ví\x001f
Û¸Ó¿ÿòüÛO©ÝªLqÚQ>L\x0006\x000cU\x0016Ã±qTäô/×Ëíbñ\x0011Ë\x0012K\x001e
(¹Ä±pË\x001c\x000b+¹Üp¹r|¹ºñ¥\x001d)\x0010kgð~ÒÇ²A\x0002\x001b±4ëÀ¶NxMôåþðGøßcYØ\x0001\x00161Ï5`à[Æ;2´\x0016Õk.3BuAcáW*Þ|þÃf¤\x0018dÃtÁË[ü)\x001d\x0006©@C	õB<¡YoiÓ=èÚÎ/î/æ\x001b¥þrPS\x00078â\x000fÇ9üÃqT£jp¢"%nÍMWªöCë)n\x000ftN¤ÈäDæ}eõÓR\x000c\x0010<×\x00109Ñmc¥Ài	401gh\x001cÛZ\x001c3\x001a$î\x0007v²áh]÷Å®ï¿¾Ò\x0017/\x0005inG5\x00044	3Ú÷\x0015ßr1\x000bå¿Ë³é¾x0û£\x000b$ä-Îèo×Ïß~Z?<M´G+PRF\x0018P#K\x001aÛ>ìúñR>\x00157\x001coß.·ß-Î¯¶É>'(¡
(xÜ
.\x001b\x0014Ö\x000fê$zèáä\x000f4â¨ÝC½\x0012,Ñç&"Q;si&,jÁG5
xõµµJ¹Bé¹À²'ã\x000e>;Ç+âÒ=qºËBQÍª³\x0013oñõÑ;³ÆñµÚ\x001dÍXòz
\x0010I%Ù\x001bGR\x0006\x001b·3»
.`ú4`úô\x000ez+\x0006\x0017áÎKþ%\x001c\x0019\x001fV÷Só5<égXøHçp\x001fJ\x0013{Ñ»pJ<ML\x000f\x0008Õ÷w\x0002P5T¨\x0004)ð\x0003\x0015N« «Yõ)LÒ°{÷ý\x0005ãoà\x0011.âÝ\x0010ê[­\x001f?O\x000epï\x0015\x000ehxqi4á¯K=J
oâ%\x0011*\-.OGtÁ¼v1\x0001Ðë	i÷g.\x001cI­çbõò|?Egà=¦
"\x0005ÊQ,\x0015l:tLz7fKr=\x0017ó»åÙé~bÄ\x00144SÀ\x0014Y\x0016è0e?ç\x0002¦Ì\x0012ÂÇéûm,`úÌ©`wL<
 )eÿ\x0012-A¶x,ûWCÉ³\x000644®Æ\x0014^`2|â.Õ\x0008Áf.\x0019\x001cÁÒ1*9Ç'Â\x0004	îö9$<\x001fá+çR
8U=§NÚ¸úJÇ£;W\x000c¦Iw@\x0016©c9ÔÝ8?q\x0001KìäzÞ\x001fÞÀãó\x0015Èß<ÃD~úÓoÿï·ÉZ\x000e%´Ã
Aè¿Àtë.ªlÙq>\x0007í%Ìæ§ßÍornu÷üù:ÜóSíËuØ\x0018?ÇJ°Ó§OkHNÜÃw}AabÇþè.´#5V×aw¼¥`§Ww°BO%¢%70±÷SQøá
7¥ÖÁâï
1]}Ô¿q$gU\x00141Äª\x001d©Ò~\x000bl-Ç\x0000¢å_N¿\x000b¿Ê\x001dJyU\x001d~ÈìÜ¿_¯\x001eCT\x001f~þt?¹x«´[u:PÑÊNBhùî÷ùeæùÕÅÛ³×\x0001M\x0001h\x000e0³°ó2;:@W¼bWý-¶Ý8íxê\x0004pÂòqø G\x000c¨\x000b¾-Æ=4þòò1\x001c}kÐÎ\x001e[%ê\x00144è|Èâ8o ä"\x0015¹uï\x0018~ï¸8£ÿ\x0004|:£+pI
A\x000e<RË³|+¹ÛÒPq\x0003cøãÝÄ\x0019½Ãt\x0005¦kÀô\x0006Æ`Ä>]ÁI.ÕÛí)­Î)í0á±S0=y'Zé;J5J\x000c´0\x001a9hÚhBÝqJ«Y­ÐîÃ	N¢á¼Ü\x00005RúÒ·½s\x001c4Ø]ÔNmÞ\x001dÓ\x0017_oø~Ï`Â]J\x000f?@\x0006\x001e\x000e±ó/O\x000f¿ü´½[ÿ°zþqªÎÜ'I:Ê*
¥fq\x0016ÜA:Ê
¹»¿»:¿þ\x000e8ßÏ\x001f¦úðÅ \x001b\x0008E=!K\x000e`ðÑ\x001d¶!¥)\x0000¹¨&9¡l¡ä\x0018DsB1DÙ?ð*ÙÈRT\x0013êP×\x0013]®Á>H/Ù
íøZ@^\x0000òzB9Ä8\x000eÐ£\x000b¹ëbøê[Þ\x0019£Ï$ËÅ\x000fåSu\x000c
H¥(Ñ¡"¼fK¯Yòý?\x0015å\x0014#åêx¾ç¿±úúYR_Ï\x001d¥Þ>¬\x001e?Oä¡èR`î\x000cêªFø\x001d\x000bZA~½8qeRoÏç§\x001b\x0007®\x000eKäXâÆbÊÀ9Ð~¯\x001d\x0016}xÌ\x000fVwV'Vp:%?`Ë e\x001cß§±zÂì É*;RÝ½N,\x001fZrù\x0008?\x000cäDÏÃ\x0019ÿiÊªÇxÃ \x0012\x001dðC«0­8x.f\x0008GñÎA&åräÀD\x000e&\x0008Læ`òÀT\x000e¦þx0.Ò<æ2³\x000eñ&\x0016&"Úùú	ìN_>¯^\x001e&®&¬\x000cp.0(\x001býuléÆæ=éÌ¨¥ðùâ
NïNçwç\x0013rÅ\x00113L¬ÀçZNÓµSye<xûihÍÀKi\x0015á±\x0004H¹ÍÕ\x000eæ^fsïòéçÕ\x000c4{¥]gÐÊqÂ³íÀã$äWáçWØDÎ&êØàæ0éËxÎ<\x0008\x001bF65ØJ\x000fBWË&s6YÉ&
Zx.\x0004ÕKÅ °\x0017ÊÙT%R¨z\x0013â&O$¢u¯TIÖM´í«=+u#®BÓ\x0003ÏRÿmÄ³Ý[\x0015å=mäLÎfjG\x001cI0xf 5#\x000e¿U=hQØ\x0011-\x001cèKóRøáMç_ònõó*\x001c çÏV/_&NÚ\x0018T	1ÝçVwþ\x0006%]Jü¾_ÌÃ\x0001r¾|;¿{·}é7ÌM4áØDCçÛÕó*Ù(=MÝjá\x0004\x001cZ£D:9Æ95BòÁM6p/æËyrNºº§ENÅsNÅ\x001b8­&ÉL#u²ë\x0003!RjBàÖ6SïÈi\x001f6%ù\x0018O[Amô×©Ë\x0012ey:äjÆ\x0011,ØPa.\x00104¬FÊ\x0007¡Ñûz~w3yÞtWt\x0019~xÃ7\x001aèoVß\x001e^iHãO:är¬mÒt\x0014¬\x0013\x0002 7óËÛ«óÉft\x00046\x0007\x001b\x001a\x0015;\x001aN:0<,*©­+Ì8\x001açÕ¬Kºí\x001a/
Isª
q8á÷n\x0001h\x0008£\x001d[X½ÕjwPÃsPÃÛ@\x0015n¾,C£\x0008í%½ù­¶5\x0015¶\x0008§m\x000b'4\x001c*Ô÷ã¨ák
åÀLiBÿgWÐb|Ú¶ñé4¶\x001dÚ°ÕîJßÈà+ìj÷í¾\x0008¨o\x000c¨'5\x0012ÃHÄ0Oß\x0011XãíÍYÄÓ7~ï´;³\x000cò28B\x001d§\x0017ÏíÒÎs\x0013gÅ§\x0004M°H,åÒäd:m"¶ST_%lÛ\x0008\x0008Û"#U8¼è$S¼Ú)²SC\x0000ÚÿrRµ!³\x0013©í\x0011Jç\x0018²£Ó\x0016Ýiz-ª½NYbÝ\x0010ÎÙÑÖÎ;â\x000cVÓj´Þ{}®\x0018«ÒµU\x001d\x0005Ò¼oP½ÐjcIõKï\x0017T´3\x001d\\x0015kö;R¨Ä{¬ÄSÂ3HU\x0000£Óá!±urïm1\x001er¼åd ãÃû\x0015ÞÝ¯ð§Õ·oO÷Sæt>U9ù¨ÓW`ÕûN=ÒK\x0003\x0012Âoç··Wg\x0013D§r:UM\x0017v\x001a\x001cI'\x0006¥ MxcB
Ò\x0015B
Ó\x0015\x000faã~ö<Yh)Hf%L\x001c§\x001fÅÈAt èÐÎÃ¦ýl9ñz;B\x0013jB¸×\x0015½®ÇÝ¦@#:9ðÑjc9£¬g²¶¨<\x000b "1\x001d½5}±;£Ê\x0019U\x0003£\x0003+ØÏ!\x000cygéÎ-Ö«×ã¸¥S):\x001aþþ7ðøæOÏß`.¼\ÿø¼þ:u<\x000b[`ÉQ8ë%YÜ\x000c)!t«Ü?-oa\x0012¼\|X.nnÆÊiý`r	?dËÍê×é¹9	iÞ\x000b{2\x00104IÕ#ª»Òcâä7óÓë\ÂÒ>ÇÒ~w.\x0010nbT°M.Ñ\x000f¹Ôæ%Ù.\Ü\x000eáx-mß¢·¼ÿÇýúyÚÄqTàR`·\x0000\ZLp3åÕ\x0008ÚÍlyö×³Åd^¢ã}·1Ðñ¼Ýx\x0007<èOºe
lM¢Sè \x001dNr£)`'º¿	]Þqÿ\x0019ðG&ùÏ«ç¿?<L~¥uâj\x000cQRv´#à[óÇðÎ/æË¿OÍ&\x0004«rØÙä\x0018`9Ó¶èÑ\x001f°G®^^f·?=MÉ\x0017;Ae`A²4VóBu'±)3jr7»ý.w\x0019ï¸½
õ"\x0018ªÐ!|7¿¬\x001f&+9=ié:§4Õ*IMÀ`çSõc!r7×óíQ[1^æç8Ó¯øCi¾~,8Õ£çÒÈ\x0019þò^\x001eHb
^ñ0çÜÜN|;È*»á\x0018Yá±ÖJlßò öÓi\x0014n	=ß\x0019¡\x0007=¹BÓ¢\x0012u\x0019V\x000f³·á¿±ê\x0002\x0004Ã´Tð²#l_é\x001e¹ná¨È0?½½º¼\lk\x0005":ÓéZ:mñB!Ðét ï/)7*Y\x0006p[£ÇS	ê{\x001bEz¥~«_^>ßO]¤eQ­ÔDZ5'F?(?-Ê¾æ×w§gcw¼\x001eE½U_ÆâA+»W\x000b	sÍòþËT±{ò$4_@ÙpÒ3pA\x0019Ñ¸¥Âl?Ù,ÏÞMI\x00172\x0015g^©\x0015ê:%î\x001bÎ_¾<ýzÿy6ü2e¸\x0012ð<©°0q¿\x001fv\x000eØ\x0014§Ø<ß½»úxv:_¾²\I|ºW\x0002>x¬\x0003t¤\x0007Ç7Ü¢\x0006>ª\x0015r³¶¦äÛR¡p®sG\x0005çK¸ÚWû»ÂeF?\x0000×If\x001e\x0007\x001c/áøQÁ\x0012N\x001c\x0013)áÌqÁÉ\x0012N\x001e\x0015*áÔQÁé\x0012N\x001f\x0003Ü§hûÂÃv\x0017áÞåK|îÛèf\x0016Î¿×OÏßV\x000fÓj+p\x0013~^Zö\x0003^\x0012`\x001dvßFW³p
¾¾ZÞÎ§=Àe,uäÌ\x0004577ÿñ\x0002ÂÀ\x0017«¿??=®¶Óiã\x0018ÖÙl*P
ç}r\x001bða#Óÿ\x0003zÀ\x0017ó¿,¯.ç¯õH\x0000\x0006½i»#LÙf%E*\x0015Í1ÇË\x0006ïÊR\x0001ÙváîD¦©ªýNdrC\x000c\x0015v\x0006JLÕ¿}¾ÊM)n\x001c
ÛÇâ\x0006\x0015Và	RAevV\x001cÕÛåÙ
}\x0014\x00032©	\x0000\x00005J:\x0011ö¨ämt×æd\x001d%öà>äUºÝ0SeÒ\x0011~4\x0001¾ÓùãçûõcØ­?ý\x000c9ðÕã·¯³ùIØ _N\x001cÏ\x000cdèUW\x0002¥Ó\R&Wò²äææOaB9=[\mûÕ\x0005dÄç·7³9l3ÁeúÃ\x0010Ýæèv/tÅ\x000c§\x001bzÈ\x0006bõ¼!ï\x001b)£ë¡ÐE.öf÷¨º	â=tÞ4¼ëïÐeíË~ìåì \x000b°×ñ]M\x0005ï4b°ÝUÕÓ\x0001ÉuA®÷ºvT\x0011\x0015³ñJ½}R:vÈ¨\x0017#Fî;bÀò\x001dÙArIbÂ()Í\x0001öcW²cä¾qg´DvKÙ\x0015Xv\x001bs-¦?µÙð/í\x000em\x0001|6ùô¼j\x0008;\x00158§«UwbcA8î<ä@Ï*í´\x0002ël~÷v9?}÷Ô@\x0007UxtÍ U\x001cr\x000c<¾pU±~CeW¶ìýé æGàY|þòãËW7}ÿ¼þú¸~Ú\x0005r\x0003Ê+pË/½B\x001fðHN{\x0006\x0010ä\x001a\x0002Îï>ÜÝ²éûåâærqþ*¤Õ9¤Õ
\x000eG£\x0001\x0005ÃÔG\x0019(±[H0±\x0019ÆjÊÌ43P:ó\x0012\x001ek1µsI\x0014ÈHN¾3{\x0012b\x0003ß6JQRzJK	T\x00136®2÷±\x00006¦\x0000½ßÔ.Ú\x001dS¨Áµ&è*äúù9æPßýöÏÇßþùeZ]ÀÓµ³Ð=\x0008àcI,eÎn\x0017Ë%&P/\x0017ïÎ&à\x000c/'t\x0011KîºËwë_VÏßbJõ0»Ô\x0013á \x001a,\x000e¾î$\x0015nÃV\x0005ç\x001f/Ù¸ÒÅõ|y\x001bSúósø7¼Æj]Î
ýÜÕ¬p<Á\x000e\x0001\x0017"G¬\x0002ÕÙ¤\x0017£)ßJÒÌ¤\x000bH£IW\x0003*|é©I^Z$c\x0002*YÌË0NÇÚ|jaT9,<6À:Ëð¼\x0000*\x0003L·\u×nLß¦\x001eV°º	V[<$\x0006X\x001a¨\x0002,\x0015ÀûZf5kø'\x001f~ø\x0001>ü·O/\x000fë_WÏ_f\x001fÖOÏ?®¿Î®~þåþËÓ¤&\x000frA0Ge\x0004ü\x001bÐÅ}{uw¾ø8_¾}X\-?,nf×W\x0017×gï®î^åå%o+0\x0003=¸ä\x0018d8ui:­©\x0004Uxï\x000eDÜ_O\x00011\O5\x0011sPyN«\x0016\x001asÂæ\x0013×TÁË:vbÞ7ÀÆ\x0018C\x0003l\x001brØZjat'm<Þ\x000bWîG÷A%²lEæ,ÉuêÓÂ³-fÛ\x0014r9.xûÀ\x0008£!Ý^\x001am9\x001eiÐ\x0014d]n\x000fö îi#1{ÚÑ\x001e¶>§êÆ±w\x0007+`éÉymëd\x0001Í\x001e¸\x0003ÓÐ.JGo²P\x0015\x0003Ï=]ùé¹æO\x000fT.ÓldçÖ\x0000;´,9?Ô¨på¨pí£Â ô1¨Ñ-¼	GD\x0016ò@S²(\x0017½(=Ó¶­y\x0012\x000fQV¨Û\x0019\x0016n¦)Êe
ä\x001eÈý9""Ã9¢1Ê(ym\x000c\x0018'\x0019\x000c2eÆ¥.]¬÷ îSH\x0018rHmAÖ\x0002ZD"²6$^\x0016¶\x0019,\x000fE¬Ë\x0018ëÖ\x0018%\x0015Ú\x0011\x001ag¨3ZÛ¤æ@Ë\x001e\x0001\x0017Ä­ß\x001eó\x0016;kM¼£Ã$§ä´ö@ßäÅ\x000c\x0007ÈÃY8"+{"pR´RÝ8\x0010²*Æ\x0005<¶\x000bµûÆ)ç\x0010eAêÖþPë*?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=!tòZì{\x0000Ì×`¾\x000b,pÛ\x001d\x0005
'0kÅM+\x0016j°Ð\x0003fEjÊÒm_Z©\x001d++ÛH¥Ç\x001bÀb
\x0016»À¤E×R\x001e'r;¬ãG0jWØ´b©\x0006K]`G
Yº]\x0015¦)t\x001b\x0007«Þp¼Àz2wÈ\x0014\x0002°µ\x0008ÞI*N;¹\x0016L7`ºkÉ<'âð~Y²\x0010
²3ûzÉz°Æ¼ê\x001eûjì'0*å.
'{Ì|KVe=iÀLá§[cÃïÈtLß\x0005±°^m9º±üºËô{Ë×i\x0004+m°hñCù-L¬R3ý\x000er\x0003M¶¦ÄÔ[ø+"K\x0016\x001f²x*8B#]Ò9ÚÚ\x0006'\x001aÎA'£ë¼´väÓili;ñÛØ¼­Ù¼ícKÒ\x0011F58¬/nÅm\x001a\x0013î\x0019\x001e6m|ó£\x001aß\x0005§K\x0017"Þ¥ä]Þ$ð®Å\x001aFðlg{ñB(E:Ö?G·î
\¼'\x001eÔ\x0005wÈ}Lp.×*8WjÂ·ò<ÿãÊ¥åìN\x0017o×Îw®\x000f<\x0007;\x0005)°ÖÎ¥5~ÛÆÍ¥?vÑÑ$\x0011É~È\x00047xÎºM?-¨æ§¥?vÑá5\x0005\x0013ñTÖ&i\x0015³ÎÝ{SíÂ\x0016\x000fúð@iÑÈÅ(oU\x0018c\x001aÉ\x001cM\x001b\x000f¯¹
]ês\x0015¤ Í\x0012÷\x0002ñÍÊÈ@\x0011W+å\x000eàYÝiªE\x0007Jz;Hã\x000bØÉz+xî¾ûïÂæ`Ð\x001fûð´Ojm¥å?x/R5ÎnÃ3ÍÖ³¦oë(ïù\x0006F.3Å°®Ègy½ÉaXc[¼>gkðf/©¤ºÊã\x0015\x0010\x000fäÇõþÞù:<ogMÅø\x0001?þ~ø0UH¾ºùËÑu¯¢A(ê%Èõ7A\x0017\x0019ºÂåúíå³gSaä«ß/\x0005NÏz\x0013^õï>ÿýog?¾¿ýx¼MMn\x0002ßØA^dï½k_Ê/^<¹¾<ûñêòÅb\x0013\x001dsAÍ\x0005=\Ær:4ùR}°hZ{ã6pËt­\x0012©\x0015\x0003-\x001b»¢\x001cfJî}\¶æ²=\\x001ad0±2Á	c¸ \q6¼¸ËÕ\®Kº
eµ"cIQa\x0008[v¯©|\x000f\x0015õÐ\x0004^-Ë\x0011è@G=\x0015j¬ÐådÉCb&,'Â{!Î÷ÖrÅ¹b$~|ÿõæÃÙë»Û»ÏÇ¨¨g\x0017ËÑøÀ¥y1ÉÍÆ°ÿxõæâÙÙë·o¯OBUù\x0018\x0017Ë`UT_2h.Ô\x000bÊ|\x001a¥ý\x0000\x0012¤Y^\x0001}>t¼þzóîhù"L\r4µe\x0019!¼îÙÒR7\x001b7¶ýõ'Keçp½#\x001eã×ò\x0018i§\x000bEO\x000b
¨hBé0ûÕNóX=\x0013Ã\x000fja\x001fn>¿;Ú\x0008Á\x0014ËLsAyX¸\x0000üMïËnþpqýd1±!P¦2\x001dPCAz>dY\x0003\x0013¼$êoéÈ¯r5[\x000fw^.\x0015§	ë¹z\x0006\x00082SR÷\x0005dV3)¬grbÈ)ñÃ\®@ÝWDYÉ\x0004\x0007\x0005gb¢?®¦
V~>¤JQ¸ç}P÷Ô\x0000W`\x0001L9C\x0014\x001f4S\x0013.¾ûõÓÇ£âDz8@¦\x0000ä\x0010ÁÉcÁOïKÚ\>~ûüå%Y"©i5TÀ¥\x0010µIÞ%Ï$dË	\x0005÷ÏßZ.j2«\x0017Ëù\x000e0ªÌ\Þ³R\x0002:c¹Oxð÷ÃÓ\1ÍêðJ2ñ_ÐÅü\x001f·GÝEss\x0013\x0016­¹Êµ­\x0016ø\x0008Òãù=a³A\x001fó¿].ù4kQ#"¿¨Û\x0003\x0014\x001b\x0005k¸\x0015\x0019\x0012Ì\Þ\x001a"§fýJ*w&zöéîý\x0017¤º}ÿåè/q\x0012Bä}[^³h£­~oÊ³o¯^#ØåÕëN°|å\x001f\x000cV¬±âCÁ:DR%Ô\x001a.zç¡\x00124îß\x0002µ-ópfÅ¢ë°|´å\x000f\x0019LüàwôÇr_Îò¸ÿßÏ¿Ü\x001e\x0015âò¤0U{ýá\x001a\x0018\1ÙÞ\x0002§;s\x0016É}üýå\x0014\x0017pÅÊAÿ\x0010rUØpwöôæ/G¡¬gu0ü\x001dEËh"$ôuUÃ-%
oÏ^üþ4­ìZ Ë#\x0003©r\x000f^zËR÷\x000bÉV\x0002ù\x001aÈ¯\x00062\x0002\x0014HBØ3H\x001bÓº\x0002\x001a(¬\x0005Ré\ó
À\x0013¬!¨$+dî\x0017e­ä5O\Ë3õ8MëÑyî\x0001ê\x0011äõ	ÕP>\x001dYÓ	 i½\x0007
ª\x0010ÉüC<tÝD^Ï\x0006hW«Qß½"I¥Ïd\x000e¥óðâÄs9ÖAabåÜ¼©=ÀÒ5\x0019Óx¦Æ3xP4<I\x0015å"H×s 7â¹\x001aÏõâqT\x001aO\x0000\x0012»`sö¾¨r\x001f]¨éB/AlZ9ycåéÑYw_a´\x000bO7¿­îýq\x0015-!\x001a< |¦ì½ûâ¶ëèô)Òõ\x0004#ý;úc[%þø»?þñv¡AR\x001fàó©¥8ç~¸(·²¨ïÚ<÷ãû·O^.ö	dLãCIìÆÄC,\x000eÓ]É¥B\x0011RüFÁîZL¼Îë\x001býÀLùýÍñ_:àMvbp\x000bBLT^²%¶\x0012h\x0011µ¶LøýÅòFL¹7¥üÔøA3òëú\x00161?\x001f¿\x001dÊ'_ÛRòò«
J°»'îýúìú\x0012\x0019¯®GÌ\x0015bÍ\x0015b\x0007\x0017»\\x001fN¾ö³I¢ý\x001c¿1uò4\x0017®Tûr@KÇWïG7wïð¿þXx]t\x001dpÛË;«Ô§à\x001d¼5v.Þ>Á¿=âk\x0014¿\x0006%Aàb\x0014\x0003x,¹oG6±ÍãX\x000b\x0012k¸
\x0004Cû( ^\x001ebñú/sìêiF]kRO/ÊëB\x001f¬Y\x001a%ÒL:\x0015ªA\x0006®ùz´ø\x001a"\x0013É\x0006\x000eF
#yh®\x0019?}xÿëñ©zäD\x000e1ñN6Ö\x0005~\x0003\x0003
Ü2\x001e¿|võ|±|\x001af	SüâI}ø?n>¿;{úþ3ÙÑg·º»=.%ñ\x0018ä\x001a\x0018VÇz%Jv*)âIøÇë'gO¯®É>»üîíåßý|óîæË×Ï·åoæP\x0013B?!ÆøÜ+â1 '\x0002í%µ\x000bU\x001fä0¤©!Í\x0010¤Ê	\x0014d;7f\x000eYÍ\x001ff´5£ígD\x000bø§Öe|h2R\x0014£uÜá×v5¤\x001bT$©\x00172_\x001bäAH×\x0013\x0013!}
é\x0007 ã¹\x0001^Iyÿ0ÉJVQÚáç\x000e5d\x0018ú¹\x0003ÿÜô\x0010\x0011åç\x0011Æï°±Ý4o0×¸yª.Î[r¤\x0019]\x0015»
3¦1u3RÖ#²¢­#eÓ°­U\x0003\x0011qÕ\x000féLÔæÜq¢Ë\x0013¶n;eëlú½MTGÝàR:ÑNHÒ\x0019kiwXËÆáè~Ck©Ù\x0006©À'Ç*õð²»ÃR6\x000eG÷{\x001c¼ùp[
.¥\x0011Åä\x000fÇÛlwºq9ºßçÐl#Í?¸JÒÕ3É\x0015ñ¶T;P6>G÷;\x0008®¼R[4«+EYIØî\x0017uãrt¿Ï¾tWzfÍ¹*Uò\x0005ZUôaÊÆçè~§C7pyÉ5ç1áÝRµÔ;P6\x0006]\x000fXttA(U9;¥þVªYu\x0012\x001ac	\x0003Æf¼ó	§AMlTÙv lì\x0010\x000cØ!\x0017D\x0019ÏCä×L;M|aÊ°ýô@sÂaà{Ã)q×g4%^ó;06g\x0007\x0006Î\x000eÍ÷ç;\x0004BrÑqÛ!hÎ\x000e\x000c\x001dî'¿·£1\x0004\x0013¥-7F°\x001bb_\x0007s!dÈBÈ×î¾æûöóï¿\x001cWµÂ\x000fD!âM,æP#%º$e_e%^¾}ïÛÏ/^\½Æûö)2¯k2¯»È\x001c©|Od4mÍ0\x0017ùx[ËEtESQOêj2Ó7\x0013Y\x000cRðnZ\x0006\x00128»,5kzÖLãEýYû`"ÓRGb\x0013Y³ÏRÏ>ÃÛ2¥\x00013eÙmkE<
\]×\x000f\x0016\x001a°Ð\x0003\x0006Jò\x0011¯;sD©Ùâý iÕüôÇ\x001e4ÈVØÄÃ\\x000bQF:ø*K2@æZ²®_\x0013ñ'\x00052UØ\x0016¥>ðuæ°\x001f-´h}¿g ·f9XA4)¶\x0004¿eÑtûsê¾³Ì:\x001e\x0012¬ü¡~ìG3-ZE3J:¬èu^,-ÓCÙp<µnOÝõ{â
ÃdÃAS\x0010#7\x001d,Gp\x001bLö\x0007®\x001f\x0014/¼hÚJ
Qé8D²-ÆVCû{BßïéÏ\x0015ÏD ½AlZ¨Bá\x0001²öç¾SZo,Iÿ­ueÞQÔ[Îg57cBK=hVË\x0003M:Ô^YQ]F4·\x0005Í´h¦\x000fÍÉ³\x0010%Öµ¾ØÛ¶8)ß¢ù.4\x000cÃ\x0005Í\x0015\x0014¬\x000c\x0001×j+\x0000ÕIpb=\x001a@b:á\x001e\x000eëK±Ð]¥0fZ4Ó\x0006^®\x0005\x00186&	Ô<= MhT8v£lûÌu\x001fäg®÷_Î\x001e}þË
þõÃ§¿ýýÿ>\x0006Ff¦²|Cµ>¥:éxõúìÑõï/ð¯Ï^>~}v±Ä\x0006s6ø&Ûã£hnj¯%4ï\x000cÜääMÍ£Ñëñi.Ss>®Ä]¢5,¬Þ,Ôd¡,+>!ç).ÖËÓK\x0016WÞj´ôÐt»Ï:7ÚoÄ¦ççSçóùòó_ÿ2A=¾ùð+x\x001dCsÁqå2$gÀ)-µçªBþòúß~?1=¾xö$¼NAM\x0006\x000fÌÔdæ!ÙÌ>$2W¹Dæk2ÿÈBM\x0016\x001e\x0012Y¬Éâ snfÏkíÙ+üç÷bH]Ê\x0011äÿS\x0006\x0007¼©T7Ï\x0003Ù«×o¨ô$\x0018Ô`ðÀL
f\x001e\x0010­Áì\x0003\x0002s5{@`¾\x0006ó\x000f\x0001ÌÏ£\x000c?2ð¢r¬ÏgÐVà%å_O\x0013AM\x0004\x000fÈÔDæ!\x0010ÙÈ>\x0004"W\x0013¹@äk"ÿ\x0010BM\x0014\x001e\x0002Q¬âC J5Qz\x0000D¥,[Hõ_ôÒÄ\x0004ÈñD\x001bTJóì\x001b3
â}*Ê\x001e²î\x0005þøþ^²ró*¸ICzµ¿¿¼~~ù»ûã	NÂ\x0006.ôÀ©Äm\x001dJ{K\x001d\x0013ç6;\x0015aªeÛD\x0017\x001bºØC§u\x0019áU\x0016Ä :\x0000¡
q6Ñ¥.uÑ\x0001o7Übji3Á\x001e:l¥+\x0003[&:R¬ë sÔÍ6ÑÙSúDW\x0006y¨i:Á&:ÓÐ.ºÀeÜH§ÎUÈte&ªÕ6Á5'ÖtX¸Eiãré$Á\x0015ÉÍXè|Cç»ìfi^zó!qLÇùs¤Ó×®1(¦Ë á!ôVûÄëóUÓóÛ&ºÆ .\x0002æROtëjÈ\x0018«Bg7\x001fÙÆ .\x0002Rì®h(Uäµ<¥\x0010é¦±-tVÕtø§\x001eºHü\x000e¨¶8ÓYÙwa³¹³¹³]æNcRB9\x0014"Xpfë¶³µ³]ÖF@ñÒÅõÇ§¡JâeíÔ(»®1w¶ËÜ)Ïµ\x0019Þæ4\x001f
.µQ4bq+kà\\x0017èI'+\x0008ÎÊÒåöñMtµ³}á\x0013üÃ2Y4è´\x0004(.m^»ÆÚÙ.k§4¿ ](NVôÄ\x0014ÏÆÜD×X;Ûcí(ÍkÏ\x0014q¹Äè¢Àmõ±®±u®ÇÖ¹$ã\x0014Í#!£¨U\x000c\x0003O×Ø:×cë\òbNèY8r|bM¡é ¡.:Mo­\x0013\x001dFOW\x0013.Æ­»Î5¦Øõb\xÀÄüNtåMz«£p)v=¦ØÑ\x0004líÀÜhKt,tnëuÌ5¶ØõØb¢ì\x001cÓ¹\úHt¦ÐmßwM\ìzâbGê|*\x001cWÙ\x0012æ\x0010 )³®ñ\x0014®ÇS\x0010âSáì¹âëQÎmÚ]ã)\§p§w)zc·lP4TÊ
Nà\x001aGáº\x001cE4$\x0006=Ñy(G\x0016¸-Y
X\x0017þðïæ¿ÿôç?s
üwE¾ô:>¾# \x0008þÔ×·¿¾ÿðá/ÿí\x0002ÿúþçOw¿\x00125)°\x000e³Ã\x0008&1à
#AÌ»Î;­¹WèùÕ³g¿?»À¿^=~ùöú\x0008¢<þþâ\x001aÿöÛ=ò-#~M3ÄH
lÓmÛi*óDP\x0012^\x0013³Ø·4åe/Hü\x0017ÙÁÔ¹\x0016Òä~d\É¶q%\x0015K!ï\x0000VÏ
®¤\x00069\x001d©\x0016ceï¤\x0018w`DÛçÇ\x0016Ò3#(\x0008Ù\x000eÒ:æªaZGØ\x00110Æhl\x000e°p!iÌlf¬ÿAú<Ü»¶\x0003#ÚÁ8¸¼\x001bAå\x0008\x0010	9õËNw ÄQ\x001aÛt]Ky\x0015\x0001òõ\x0003·ã\x0001RqÿÆvHÊÂk5¶²ÞÓJj;\x0000q%++ÉÝ³;@â¦ÑfÜúÜ\x0001{>Ò
dØo%ñÛêA;\x001e¢üÞÔâä"ÛqÃf<Ä½,$¥\x0010õ \x001d»gqS\x0006wÎ?·våh³PÔ\x000ehÃõ \x001d\x000f»ãq%iÊN^HsXI½¤.i=hÈI	m¤Íãp%a¨¬ßmOâ¾Ñc|jé\x000e¼>\x000bÒRr\x0000dÑ¼ï¶)qãè1[\x001eSÈ\x0017+\K£sÃ'R\x0006Òp\x0001vÛhÊõ 9ÿÇ-%
S1sNçezöÂ¥¤ä\x0018!lJv/ßM©=Ð\x000f~-éî0æub(a\x0010íP\x000fLÏ(0ßm_RÐ\x0007c\x0016=\x0006Gi\x0011å$¿)óSâD¹Û/\x0016
Æ¬eô.4sty(\x0014R\x0002;\x001e´éa¯8\x001e±aÐ\x0010!¥ÑãJ¤}\x0019ösf £`Cç\x001eð½1dØ0Êú»QhÏëê×5¹s¶ \x0014,ñ\x001eð±x#·WÎ\x0000bfÅÝ:Êú\x000fÜ°þ\x000f_o?O\x000bKÿ{d\x0013(ë¹I¹^¼|ë9*\x0019E½wÁÿÌETºùÝçx½\x0012Ï¨IÔ.\x0019ôïkÑ\x0004
©#Å×o\x0003~w}ñ\x0002\x0001WÂådV'\x000e!gÆ\x0011t'§\x0010)\x00029á	.Þ\x0005.'záTÌ\x0012L\x000e\x0002eÙòÊi%\x0001\péÈOÛ\x0007.\x000f\x0014.g2:áTYI\x0001áð\x000baæ.g8\x001f$2ºà$?ÐK\x0017X¥ÌQÇ8½¥Nt.ñ½;\x0004{äÓGÇ^:\x0017ø¾
$z<	* ÉïöH\x0017Õ.kÇí^:Ãý\x0006\x0019ä\x0006SÉR\x0014ºcaY\x001f\x001d_`»é\x000e¿,Æâ®\x0002@Ú²vi\x000fs"wÂ^:zqv.Hà\x001dRCÅÝ]prËê^ºÅbiép\x0007òÒBü°»Ðñ½åA.\x0002\x000e\¦¸¥\x0013\x001e± Û<\x000cP²¨?É)\x001b¶*>ø=Î­Ò\x001c¯LáÊ\x0003\x00054\x0007«#ëø2¾ûå\x0017ûÇÛ*úûÿõó»/·gSmäI¸©ö&\x001bgü§ W\x0006¥`M.¬öÞ:rÃ¿|üìíëKúï9ÍF¥ôÿ\x001f\x0010ûÕÿòïhBÛÿZý÷¯ÁKÖp:l>3Õhà¹\x0003å¨Ì\x001bHõ·Ç^U1b¬Ú\x000fù\x0003ú«\x0008ÿëüÏ«\x000f\x001f¸7òôF$3h²ÍÑQçV~¯\x0015´p5e\x000eÆ=ÞjVÂ\x0019~:õM\x001e[Ø\x0002\x000e58l\x0001$#-\x0011Æ:U\x001aÁi\x0016ôà¦\x00067ÛVÜóû\x0017]\x000c|â\x0015·^V\\x001f1¡Cà¶\x0006·VÜðØS\x0007\x0010sW%y5öØ[Ó\x0010µ«©Ý¦åvòhËísá\x000f.w\x0014¯
öX¤9\x0004îkp¿	<I6xj4ùBÙÀ±
úâ#Aè\x0010x¬Áã&p*7°\x0019\x001c\x0003iÈ©W¥²Ö4®x:b Ç\x0016\¦A\x001c\x0016>Ø°ÍÑuwy&$â»(\x0005â;ç\x0010¿óëüÿ`#µ>ØbØyV(®Ò$qËi1+\x0006öà7Nµ®\x0014?¨\x0006½¾}wóq]f,\x001eÎ©ãée)\x0019ÎP\x0018µüøúòÉÅ	#5%ÔÐOiéæ£ò\x001bÀÊ\x0003·	âtÂç¦æ4C«\x0019r+­¦ÏÓé'ÐzxkX	jkP;´ 6\x000b»Sy\\x0006-¨§Ñ´©=@]
êFVÔL#(Êymý\x0005:î]8}Íé\x0016ÔI:
ã<ì\x0016\x0014¢,¨Þå\x000f5h\x0018YPmÎóz\x001a¼°óÓ
(ï$ð»pÆ3,(é/Ç\x001fÎ!)\x0019@H»,¨V\x0005UC+<4äöâ©²EL¾ßcêÖÔØúè4¤	Ôs®u¢0«åñû8\x001bc¯\x0007¬½IÉe¡
G=¹E|R\x0005Õû6æ^Øû¶3çA\x000c%¬åZaÙZ½ûÔ\x0011Õ#V4*;W\x00114ø%åøÁÖYcv!mÌ¨\x001e°£fÌ\x0006Þ£4ß5ÿöZÁ· ßkW6vT\x0018Ò@hóoÁ\x001bR¼K­?ñ\x0008¾´±¤zÀ\x001a\x001a\x001dÊ±·R\x001cèÊ¹ß\x000335idA!åV\x0008\P$Zpo^öT9É:Rh,>X|ÊoÛÄ?½å\x0015U\x0000å7»6\x0016\x001fF,¾ÇxTe'jiô\x0014=E¼Nñ:í«V¶\x0001þÍ·;ërj>ÇOÑkK¼Èmo$ml>Ø|>R¦4gîâ!EüËÅ\x0004+A\x001bS
#¦ÔRî('s½·$A¤.&Þ¦>º=Ü(4¦\x0014FLé4¡>:\x001aQ\x001f¶b¹69o÷õ 1¥0bJÑýpôì\x0013Ë'ã\x001aNNàõi\x000f\x000f-\x0011[êRÈC/pE-lÄËi\x001b³\x000bÇJ\x000fºHMc¢Ì¢\x00163¾89Ü°ÙB\x0005¯ÄBÅ]î#¦±PfÄBaøL³u¦·\x0011\x001d³úG6&^Ò`v±¥¦MBX(Ò;âË½ó-¦5-¹WìrÊJÒ&\x000ba\x0006Ò\x0010Æ8/\x000f²Á*JDMkêÄSM\x0001+I\x001bcjFi IPìòé:*yI'\x0011ô&´u ¶MìHlbv¹é\x0019>\x0008²¤i\x0000Ú6'ß|\x000bJZk<M\x0015c\x001aÄîs!µÍÑ·#G\x001f"ëMá&Ï­sÑØXEO\x0014¯$m¶©\x001dÙ¦ÀÙÇ¨mV±¡ò\x0006Ù£QflmÄlÜ¨\x001dq£\x0017&Ý\x0013nÍ¬Ø"\x0004)Äv®m\x001c©\x001dº\x0004/É\x001d«M\x0016¡X_ñ&µÎìAêãäFÓ?´ñOnÄ?A
rÑ\x000b§=â>õéP ¶G6Â5©\x001b	L§\x0011\x0006ÙF\x0005ç|îµ'½KXê]êFv)^ó\8:ùPÎSJZNþ\x001eq©o6©\x001fÙ¤@C²xA¡ÜñÑþ%Ý%ß¼Jæ±ªÊ½'©\x000fç\x0013:H\x001f­ñåõýT;àÚdù7\x000eò¢Y¾äÌ¤Ìål§¹»·¼n÷\x001fe²t¸\x0007\x001c\x001e40¨?¼%©Þ=ÔU§{\x0006\x0017\x0017O\x001b\x0016Y\x001bØØ&/O6Ú]rUê\x000f?ÍÖö§\x0011VÇ×RABEr²\x000fß\x0016d«ùó¾:<ïß=ÿt÷áýÚ\x000c ¥ÈZ_\x0002mYñükz¬Úz\x0002}{öüåÛgW+HMMjFH\x0003:.à>=\x0008Ü¤\x0013\x0013ÆË
E°\x0018d¯Gµ5ª\x001dB¥_?:ËMÃ1 íonÑÝ®'u5©\x001b"U«Þ4Ý\¸R7
°I\x001d«7íDõ5ª\x001fÚ©Tß´vÙyÅèø6hãÑÂ¥NÒP±3eH\x000b)©²S#O§§Cµ\x0013j¬Qã\x0018*dDBuâ\x0003¢\x000f\x0005Õ/\x0004ëQSÆPñVÀ¨ô\x0002I\x00037jZJ\ïAZ=ø«êÁ¿\x000bÕQ\x0014·ªàòc\x0005f]î(^ÚÿAû¯Ø©ê\x0000å¦\x001dY6Àb\x0001ÍzÖÆ\x0001è!\x000fà½\x0004,ÚÇ(í\x0019ø(¬jñEu=kcWõaõ^\x0017Ö0ÉiN¬¬\x0017[ ¦¥\x0008`=kcXõeýGyVÝV=f[ã¬¦¿ågÄvr´Õ
÷\x0006,¸iC!÷\x001aH²oZY\dÅ1+%óÊêÅu\x0005­\x0007¶®ó¼¾¹[ÝÜ1Õ\x0004®*\x001dÛÓÄO\x0016\:¡et}ñ6ÿù$.Ô¸0kI¤_5\x0006±ºÜfK%°^¾\x000f¬Ç55®\x0019ÄÕTÍ§ÕM».1RJ«ýb õ¸®Æu¸JXT¬\x0019üè¦]\~l_ÏêkV?º´VZF,ë\x0015#®VeÜ\x001f{-m¨qÃèÒ**WV7jvcT¾ÆÏoÚ¦åç·õ¸±ÆÃ;Úx¦Õµ^êpßJ¡¥ËwÙõ¸©ÆMV,:\x001aG2­®µY4%HÒ{­õ*¡Õ¸U¤hÒÐîåå\x0000m]9kF8Aåøõ¼­\x0018ö\x0012 -d#o\x0007åÜæBõ¼Ð£nB9¾\x0001\x0004g\x0011"Sê®Õ\x001cýzÜÆKè17Ëk xÑx1J\x001e=µ:ÖÐÕÍk\x001b^;º¼\x0007Ûk\x00127¬âòÝ{âv=nãÕô[û\x0007Æ8ºñlzÔµ)) Öù­!¯®ä5u(îÛx6½ÅµqÐÔ¨WªôT:Ö¶ÚÍÛ¸6=æÛp;Ø\x0012CZ+G\x000eâÚôb¦¶ñlzÌµáê&I*«<¥)ïTV÷D³Ëj^h\\x001b¹¶É±\x001eÖ¥<è°9Y^³íÆµÁkÃ\x001bE<h¹\x001a\x001aZo\x0014NÖ÷âM7n{ÿ\x0019ól¸¼Å6hSö®ò\x0012è¸éÆ³Á°gô\x000em\x00032{Þ
VdISØÉ6@ãÙ`Ì³a éóD*\_trÒª':\x0010h_Ûx6\x0018õl!\x0014áJÇã3H¾»hîÙÝvoczaÔôRæ9ûpâ®¨äÊ}\x0018vrmÐ\x0018_\x0018½WxMm9I\x0016ÅµQ\x0001¥$ÉN´È¬æ5ñ5£ÆD÷dû\x0016W\x000cI¤´?Q8»·1¾fô^A\±$!sc7­¯,/ì´}Mc|Í¨ññ°¼±\ÛÜ+t8ñ\x001a½·±ffØ)¹\x0006©\x0018òÐIÚ\x000eZ|±;Qì¿·1gfØy\x0010\x0005æ\x001b!/Ö°×µØ4º\x0019\x000bÔ7¤\x000e¢sÖ!4§¶'<×ã6Ö×Z_ô\x0016\x0003õ Å\x0019C,YS­«ymcÍìpDådt\x0011Òö§)\x0017¡p\x001bcfG\x0002î«B;àòèI6\^ªÚ·±fvÔávÝK\x000fWì,¢Ð^ºmBI;\x0018JÆ ¸\x0001\x0018o±S\x0001Ö\x0008´!ìå,lc|í¨ñ%cÆY\x0007©\x001bÄÉòÂ^I\x001dÛ\x0018_;h|ñwgaRíÖ¬>e;¡û±·1¾vØøzÒÏëDÂ»^ß½r¶IØ±4EµI>\x001eÇêZD\x0016l8¥Z±·ñ\x0016v8Vw"¯BW7\x001dÊô¢´WJÝ6¡º\x001d\x000cÕñwÏc´£\x00057^'/Õ\x0017z/_ì\x001aßæ}§\x001a±vð²{
qB3×8\x000b7Q×¥Ü²<XHúÔ¸­õ´íu£	j9\%u8Mb¤\x0019[´×nhl\x001bÍø\x00021\x0019>Ñ(?f:\x0011¤·uN=¼mp£Ï z½:²\x001b¬d¡Ôn¾9l~ô°éÈ½\x00182&1½Æ\x001cên¦×7Í\x000f\x001f6ÅÊ\x001c:ÙCF\x001d¤WóÔP¶õ¸ÍióÃÏA%\x000b+¯ '4)z'Þ¶r`ø}Et6³òç«¢ü¿W\x0016Ê7§Í\x000f?Æ[îÙF@5Ó¢z¤H®g\x0017ÞÐ\x001c·°á	Àó~P®T½PR#§uÒn¼Íq\x000bÃi\x001d%ëKó$P/ó½|Úé"\x0014ã\x0016F/\x0016ÞÑ3ENúñTà%POöÆÌzÞæ¸Ñ@xMá
÷qwº\x0016æ´Ñ¸Z7x\x0005îNà¬ä|Í	-Õ¼±9mqô´9SÆB\x0019]îAÖÉX(8Ñ.¿·9mqô´QÁ\x000bó¢_æ\x000770FÞ,Ë#{xã\x0016G\x001bºÈÛfwd\p²\x001dÔÙëqÓ\x0016GOáÒSjM\x0015ØU}\x001d=¨mÙèI3gRhR\x000662ý1HÂ,íUdFO¶b\x0019\x0002
«ä	W1I7JØ+=FO
âIA×òàÊÀ­È{Båk=o³uÓàÖ¥Q²\x001f\x0016A:m¹\x0002\x0015ÿ÷N,5Û7
nßHâYÜ4MCÊ´Ü\x0008n#ìTö¢Õ¬æppûÆàÄQ\x0004¼ÂË6#
*Q­»\x001e¸-âSû7\x0016ÕmM}@2\x0013¼d|Ób;E\x000fp[\x0016§\x0006]Eô[\x0000=Mã\x000c.9¨xLæ¹·­3S£\x0007¼\x000bòØ¦µf°Ó-H·\x0015ÉôÇÁ\x000cBio"õ´ç\x0004ª\x001c¸°×k¦\x0015ù\x000eVù"°ê\x0001\x000f^ü`\x001bìÑ}ëÛ\x00037X6k¢$öZq¤®"\x000bFØ`v\x001fô¬\x000cu°\x000e\x0015y
?\x0001hß
3°Äf\x0001Nh\x001b¬\x0007n\x000fÜ`e'\x0002k~Õ.\x001ayÇÀZÎ:Ñ"Þñ¤ÙtàçgÍª\x0003¿\x000f;E. úÅÌ ô¥aÜîä\x0003Ì±\x0003\x000ccÿÃîõ*Í©Ó\x0006èª!Ié:$\x0011éÛïYKÅzÎÁ\x0014È×£4»3´44s©·®,µWÅ2þu¾­ÕøR\x0014\x001a¿{Öî£÷o©æ1'\x0014zVzF\x001dG¡q¥#g¦Î\x001c\x000e;yo ¶ö=ý¤\;é\x0011~@ý¯n¿¾ÿzÆ`k`\x001d^êå®o}"-lKÄ#"çUÞ¿º|sõæÿÓ¨P£Â\x0008* ãÞ]k¦6^BÅ\x0018û\x0012gø¾NR[Ú±Eõ<.\x000c\x0017UÑ\x0018Ì¼¨Ò\x0011íü±\x001eÈNTW£º\x0007\x001ajÔð ·j¬Qã\x0010jð\x0005ÕNu\
R¥l=vQîDM5j\x001aBEÃÅ§ðG÷VUJÎ¬sÇ\x001eûPKÄm\x001abMZÒ%Ö\x0018*ØUúnèË\x001c	Î:Y[»:fXS)²vêXuÝje%;YMÃjFX-H©Ñ}fõQÖ\x0015Â÷NÖÆ´ê!Ûjéý2£ªDOÜ\x0013j\x0012>	öAmL«\x001e²­*dùhaLÜÄjT1XúX\x0005I\x001f+4G\x000b%¡É¡\x0001\x000e.\x001bWã%çoéÊ¶\x0007ks´`èhá]uüµ\x0002¬UÄ±l:V\x0016ÙÚ,C1£\x0006«Ã²z&\x0015\x0019£C¤
!\x001bà¬
\x000c\x000bÓ]Bµ Åo$C¸\x000bkc\x0003`È\x00068²W®l\x0000Å¬JÒ66\x001d+¿èdm\x0000\x000c\x0019\x0001geBÂä\x0007T\x000e\x0005ÐÿøcOí¬¾aõC¬&HÙÅë¢
¼\x0007$ç
&w²6Á \x000cEø?\MHa\x000bð²Z\x0011ssÇæ
v6± \x000c\x0005\x000e/¬Es\x0008´ç\x001d \x0001\x0016ì\x0013aC\x0013\x000bÂP0è<Þ·Ùc¡¹²Ù²Z.»±$¿\x0007ªi\x0019s\x0002eFvà¨qBMR\x0004àõ1µüNÖÆ\x000b1/@Û|®(ãÌÕ\x0018ûh\x0013`'kã\x0007Ì\x001fÀ@ »\x0001Ü¸$BG¨NIÙÛc5æ¨\x001b0cn^ø`Ñë)» ÄeyØådÆ
17p¨¸Â¸<m^WIuz³\x001b0Á2c\x0006+z2­k
¤A\^ã>mÂV;\x0014¶ÒneÅ  x^Vq\x0003ÆùíÁÚX\x0001;d\x0005Ð"±¤vÊõ'T#± ÷ÇRô¨M `Ç\x0002\x0001[ÂV+ 	\x0012±À±G±Þ`så´ }0\x0019¤F\x0008±4ÐÞ2AÞÍIa\x0017âzî0ç\é\x0007ËJó5Nkl(Ê ã\x0002R1\x0011§ VÁÙ}Ö8Í×8®1)\x0005°{ gSÎjh9p{yÝF·wÅà\x001aÿÆ»ªõ[]B*ßÏÍ\x001f>L*>M_åô+VJJÒAE\x0004·\x0006·~NBQÇ^9=d\x0014\x001f½¼z}\x001a\x0016jX\x0018M¢ü\x001cK\x001f%ú\-ï\x000bM÷]¬®fu¬!Ï*Ó	©\x000b«ä8Iùd\x001fÖP³1VÄ¥E\x0012ºàM\x0010äÙ9ùÊáU°ZÍ6\x0001\x0015Wâ/go¾Ü~þx»\x000eW¡Ûå:ç\x0004Ó\x0018Ð	\x0017¤vr\x000b/s¯Ï\x001e_¼¾¼~q¹\x0002ØÖÀv\x0014\x0018.KÀÒ!c],«Ýá-Ö{ô\x0000»\x001aØ
\x0003k\x0010¤©¶çÀÚfmÒµ¸=À¡\x0006\x000e£ÀÖÚáä¸P(µÙq¹ã¾\x00078ÖÀq\x0010x²»¼Â²c³+\x001bb¹ô 6Õ´ity\x0016]àDýlÍL¿9!ìÖ\x0001|ÐQÔµìö\x0003&VÍD|ì\x000eE\x0007\x000f\x001bæÜ°\x0004t±Éyê!ÚäPLÜòÔÃ5Ü ga\x000f~PÍåøþæ×Û»5´\x0006oéç!·´ûÄõw\x0006ødØ e\x001cX8úûç\x0017oOBM
C¤¸	\x0002\x0005K}âjLÁòÇ\x0012¤¤¶&µÃkë©hîEö\x0019´¨2Wl¹j=ª¯Qý(ªÉcÎ½
Ü\x000f\x0011m\x0019\x001eîÃb\x0001üzÔ¦60ïÖrÂúÙRÞ(\x0011çGÿæe\x001b,ÊÑ&Öqv¶ðJêüÃÍÙÓO\x001f¿Þ¼ÿx»7"$\x0007\x0010ÑÉ¹¤èMÙ\x0013ªÏ.Î¾|ñæâêÅåifW3»qfÜ
/\x0018°±F]QðÞû.èPC\x0012èXCÇaè@6¡'
\x0007yI´fN4Vö@\x001fjÌ§-­ÆZë2Ètf¸\x0008ÚöÊå¤.fß0ûíÑLzËûºª¾ìÞ%Ôä!»ÄQ\x001ae\x001aï\x0010ía,×p¯bù°/h}=ý|ûe\x001d¯¥*bÑH¦ÖES¤;\x0016-ôÓëË×k@¡\x0006\x0011Pñ\x0007nË·e°¢+²Òj±\x001fe=©©IÍÐz©vÖT®\x001dø¤âñ²åzT[£Ú¡EEë ù×wZÄ¤mV©Ì¢(ÙzTW£º¡U
ªmòªZ-Ú¢üÔzP_ú±5\x0005z\x000eÌkªè\x001d;¯i*×äEùõ¨¡F
ckê4\x0007U\x0008ñÌOTÎï\x001akÔ8¶ª®\ÕMvj(v
\x0016\x000bÛ×£¦\x001a5
­*õhðNE÷%«jèß¸EÕ¨\x0018\x0001Ú±d=Ë
¡HõXqWÉÆ$¬°Ø»³µõTc®
ý\x0013?¹¬\x001c,[ÖÕ.Ê×®gm\x001eóVÙ÷çu5ÒMëè+8qY_ËÚ¸+=ä¯´*eøÉ\x001bn²eª²iÓõ¨»ÒcþÊD\x0019MfJrÒt¢J
ríÚø+=ä°4\x0015
2+õ¦rþ<F±XfQAs=kã²ôÏÂÊ\x001f\x0012»*[W\x0012\x0006(\x001aMûl×Ægé!§ES/¸Z89àyàúõd]\x0017³æëY\x001b§¥Ç¼£Z\x000beâ´ô)zkQ\x001b§¥¼ÖÔ.f5·/ªb\x0003¾V³Bãµ`ÌkÑ]@Öµ½:\x0003EòjQØ~=k{m\x0019ó\x0004$bn
+?ò8Sn\x0003z±p=kc^aÌ¼\x0016QÏIª-eWà\x000e¡«>1Iq-kc²`ÌdÅ ´\x0013+ß\x0007\x0003\x0014Y¹Åöùõ¬É1\x0015KR\x0000ãóàd]\x0015Ì>¬É!\x0005¶LÿN¹ÓX§D\x0000¯«Úg\x000f46\x000bl\x0016@>'
\x0007¸a^J+Èkíb\x0006Lc²ÌÉ2\x0007y\x000e\x000c²\x0019ÊÈõUí\x0012¸&Î6Cq6L2l\x0012\x000bäsåi\x0014¥Ø«åºkI\x001bÛjlë?jQÛÐPmprÛH2AÔ_B\x000cÅeíc\x0002Lã\x0006Ì\x001b04Tùà^³\x0017pð®\x000bU@=¨MmlkÉ16úYoxUË5Ëìs}5\x00130CNÀ@ÀäK\x00023øXT|\x0017õ¶:X÷»Ì[=àu!\x001béÏnÜÀÈòä¼<(±ãV0'Ö£ÄZ+º\x0015Êpr-ÑÙÇ%À=d\x0018F¦é©\x0004\x0007\x001c\x001b\x0014öÍ\x0014\x0018so[Ñm¡JKI¢0>uF0qk{>Â\x001aìì]÷ùÍûÏï×¦ãá0´ËPßNNÇ»ÃÔ£ÏºÏ/®®¯V\x0000C
\x000cÃÀ9BeBxÂ{¯h¼\x0010\x001eéà55¯\x0019åuFÄêi9h²À'\x001fF×\x0002Û\x001aØ\x0002GÍW\x0007 â\à\²)9ùF·\x0016ØÕÀn\x0014\x0018±d&%®0\x000fTòJ\x000b|ò\x0015w-o¨yÃ0¯:Àòv\x0008öpÞå :hÛR\x0015ÛªôïÀiÐ<}NK\x0011[á^¼ø¬â6Á·vDÈN|ºû:!ÿP·¿=¹ý_Ïºûë§«ð©iÖËÈ A[e¦ÁÑòâoßLü?âg×¯ño¼xñæìùË·ÿöòÅéïbêïbvù.Öÿ0PçG_ÞúHwç7ù2¶þ2v/ã\x0000¿\x000c7NÒ,¹¥IÉ\x000b»µñèjãqõqÿÜ»,Ôß%ìó]l,O^áo2}\x0019jq·ïcvjãwõw»l2*µK¼É0|àÖY¤{ÇÆ£ÆkãIõIÿÔ?L%ìßezPÝá15c
­Úª\x000e!þèp_F7_FïóË`ä$oZ&g×B¢\x000eÀÝøe\x001a'£÷ñ2\x000e\x0019\x0019ôJîÜD«ÉZy6£ïÉ\x001b¿Mãeô>nÆê(OxF%Ñú\x0000WDtèÕé7ù6Ñûø\x0019U`Ý¤\x0015·¬S¹ü6ñháâÆoÓ8\x001a½§qTÐÈ­jÉjçôm¼H­'Tªzã·i¬³ÞÇ<»Î¥:SÑC!}\x0019¼©Ju¦
¿Í±Æ<Ã>æÙ&â\x0007Hú+&$'\x001aö¸ìùÆoÓØgØÇ>\x0007\x0005¢)\x001d¨\x000394R£\x001cýÑ\x0012öß¦½Ñìr¥qN9É\x0001\x001e%L0ÜÐGý;¿Í·iÜ
ìãnhê+?®\x0006'!Ê\x0018öh«ÉÆoÓ¸\x001bØÇÝà#\x0006\x001aH
G°¸\x001bõ\x001b\x0002Ð¸\x001bØÇÝü×ý6¾ù6~ßÆ(¤DûÏªPÎÍÑ\x001aôß¦¹ÙÀ>W\x001b4ÅÜ\x000ehÒøfCoTòe\x000eÊÝzåld§kç\ÚåSn7\\x001eJó\x0006KýÒÎ7\x0002ÜÓ³6©àJ:ýýÿyùñìÑÍÚ¦{©\x000e\x0000Mij~_	RÉ\x0000pLófJ]¾8{t±ÔåÉ¨¦F5c¨v2K\x0013*ÕqA\x0013p'ÆûÝ\x0003ÕÖ¨v\x0008U%%ªî´ªÒ?kE´{ñ9e5¨«AÝØ(9R´'t\x0015Ì,R{§ÓbÜjÔP£1Ôh¤³ªF\x0003ÿüÁJÒ<-Ö1¬F5j\x001cB\x0005\x001atÆ¨t¾¸¥áë°ØY¶\x001a5Õ¨ipUdf1\x0010Y©.§´8þn-jÕþ\x0016Ü¡´½sYæ\x0018\x001eõ(\x0015Þªò.µÇù×­U\x001d4«IjqY*q2ÂºÓ÷@\x0006\x0015\x0006W5q\x001f\x0016®ª;wVêÃÊªú¥¢Õ¬\x0007Ðc.\x0000ð:dy\x001a\x0002ÆDÜÜæÉ\x0013fÖ¸¨K°µq\x0001zÌ\x0007ÜëªI	3×]\x0019YÖ]n\x001eó\x0002 '§\x0000\x0015¹sÙ×\x0012Áè£zÍ}¬\x0017Ðcn\x0000\x0003\x0012*µÉ¬ª,+ÅXÌºøª·µ±­zÌ¸ñ&\x0002jwâá.4^ü[*\x0005YË
Å1EÛÕÏÒTÏÛUÌ@X\x001c®´µ1Y0f²¨L\x000b*\x0014Þî"W	\x0006Ù\x0002°X&¸\x001aµ±X0h±.GKÌööIBA}TV´µ9Z0v´¨\x000cÈÈy±®Á\x0008ª;zéBmN\x0016,\x0003I",\x0015\x0014
 OJÚ.ö¬ß\x0002M/yÞ\x0006¥ ¡s'D(6M­Ï\x0013²*1Á²xÆz?;GÖãÈÊóå\x0000×Õt¼·Ý\x0002\x000cq^c\x0015kI¾ç7_y»J\x0004¯1ªÔ¸ã¿dµä	Ë-´
jÜó7ß_].É¨Äy©RR¥~N[:ó\ä¹Y® ¹Y]¨¾Fõ¨þ\ï¨*;³Nòã\x0019´NØXÃÆAØP:ôÑàr/9	ú
ìÀD\x000f¬n6«\x001eÛ­t	<ôÙÕ áÖRA`\x000fí!0\x001e\[	\x000e§öw
¼¶P:\x0017Æ6¯§5x¿¯i§?1é!q*EùS¶p£íÛ¸M±Z¬Æ¼u3Ç©®.Û/+Q£2@6b\x000b}«Õ\YIÅZ`äÑÝ×Û¿®Cu©\x0014âÍVZ ­*\x0019£csh¸VøÑÛ7ÿv\x001a\x0014jP\x0018\x0001¥Úkñ^®¤\x000bu*\x001a¿\½\x0012ÔÔ fhEÃ¹+^VzÉ\x000eÖ ¨p_ÉikN;´ áÜ»·tÀôæèt´ð¥ÓÕnh=­p\x000b¢3ÆËì.¾æô#:òä!\x001aâ(UQ6aÅx{¹-g%h¨AÃÐ\x000fXI\x001a¯á\}©®^\x0003WsÆ3\x000epª$\x001d¤@%ì|¬Ôÿà½p¹»e%gª9ÓÐzbbJÆ\x001dªvêïåÌu«H\x0007(Æÿ|yUÞÛØÊG;}ª3%ië¼C­7\x0006)"ÏQ:\x0000Ü¢ðçjÒÆ+é!·¤T¹dã\x0015 ²ó%y\x0011ö8õºqKzÈ/©Ä¢ìSE¤¤RL|læ`\x001fhãôc¢_<\x0017d¢iÄ¼¤V:\©:s\x000fÒÆ3é!×¤¢<\x000b(ôRi.Ï¥áäçJÒÆ7é\x0011ç¤RÑQÅË<`På[¹£ìb¤\x001aç¤¼)öÓmÊÉÊ³ðlàjÒÆìë\x0011»OkêÙâ\x0015Ðð[{y\x0016>^Ö\x0017èÕ×\x001cìUm=6µÄ¥ÚJ6Ð)écÄKê¦ø\x0019\x0000f=\x0000ÕäÙûÏ«æ\@JïN¢æFì\x0001\x001f;)üpÙ >»º^r!¦Æ4\x0003hBCÞ¦T%»¨BR"Ç2©\x001clÇt5¦\x001bÀ¤©!Ùb(ÊAi¿\x001d~¾Çj\x001a3\x000c`âäP\x0002ò-4Äb¨n\x0007ÌTc¦~L\x0002`r¦'ÑtL©egÂ	¥Uº=@\x0003'(\x0006©ÍD\x001a§\x001eB\x0012!ê¤ý\x001eÍ	Ò\x0003G(â¹qy5#úÁfÎ ¯¿I-\x0016«äÏ³fÍóÏ¾~])xK³A"ôZyø£9<RR½`ês>çúå7K
óy6àÛäy\x0007¬×ì@'ì,î4åß\x0018v¡º\x000bÖÖ°v\x00106Ètéh½dÊ4\x001cVvAÜ®\x000bÖ×°~\x0010ÖTTÌ\x001d\x0003\x0019¶Ì\x0003±\x000b}É]°±c°4sWÖL#¼óU2óÁÀ>+[É\úr1í?a^ý&Zò<¡\x001dÈÒÂÉ·\x0013´ÊÍ3¦.\x0003)\x0017}tó×[ª\x0018]õf\x000cX©[x\x000bP2íAÔB¢>zÊ¤JôÑÅ¿]R¡èÒ8&7Ï:Õô#wBÊ\x0006\x0002¥¨yDölq1Ì:æf\x0007 M
m6¬´£ÜÏ´Ò\x0018tñ°
+ý,.úµß+ õ|{èÙöxòéî¯«ü\x001aþfÕÞ)SÍidt)½8ZÕ$ÀO^¾ý·\x0005×¦ç+¬g+ü\x0010a}
ë`\x001d"1,i iû´¢T7t²p~%l¬aãÃ­1jÛbi\x0001îÓê³:E;Ç´oDc¨áO\x001fÞY«\x0006Q\x001c\x0006éuÉåÛ@Á[¼1\=;»üîÙÕë¥\x0001\x0004óLûF4¦\x00178\x0015}t[Í`
¢\x0000Qy\x000f°©Í0pÎh£É\x0003é â¹\x0017°­í00=rã\x0006(©oA'rj!è\x0003v5°\x001b\x0006\x0006#Ó\x001cAËû±®ðú\x0013ÂG«yCÍ\x001b\x0006yMJ±\¨MËüï\x0014'\x000eöì¦êÉ7I¯þuöé¥ý¬\x0013Á\x001b«\x000e
^þpÌúu®æÓòZÓ\x0007£ûÙf~­¨T>ïgS¦¶íf1Â|¹Ãåþí¹ñdÌy<*xX\x001eÿL\x001f{ÆÑ{ÐóÉKå¡\x0016Å\x0014\x001bÕ±Íñø{üìÅªz\x0016Ã#+\x000c²\x0006\x0007áI
Ø3,·Úa¨vÄ`ô²Õ±ZÃ\x0017$í½î\x000e\x0000FiÃÑ|s/¬­aí\x0008ìÔá\x0013X\x0005DyNE%\x0006=&\x0000Ð\x000bëjX7¶²Þó\x0018½[^Y'\x001dÁ\x001dós½°¾õc°ÎH)§·@\x0011Ð\x0004+¶ ¸°Ó
5k\x0018cÅ;±ããE×û\x001aD\x0005"Ð¼Ì]XcÍ\x001aÇXéñ)Û-ÈCaºáh÷ÔZX´³x\x001dOHecÙ/|ýåÓ/7ër<©è\x0010ÃÌ
-â\x0007n\x0012Ì[D\Ãï_~q\x001a\x001bjlxðØhfÙj\x001d[IÍg7~ÿñv¥Z^\x001eñïs^\x001bz§´yÄ'?M{kNªT>»xuõârYèOÏV°a\x00036Þ w9cX08ZÉáÂ¢\x0006o/µ©©Í?\x000bµ«©Ý\x0006ê$Ñ\x0004©\x0010I
D¢\x0004{±Î¢\x0017;ÔØá¡/6
`n#Låª×#ê¼¨ÀÖpk\x001fXÃ\x000272\x001fvjqÌÉ×¥mJq?©?;	njpóO\x0004nkpûO\x0004îkpÿðÁRÁ6Æû\x0011µÜ\x001d\x001e\x001d|ºûéÃºâ\x0012\x0013ðÎÇCèµ)ëNDô6òg\x0016îØ\x0013ñË·-Ô\x0014X[ÃÚ	«\x000cÌrøAe=^Ý~}ÿõf\x0016¤jNò;^yÎM\x000bu;\x0004ûêòÍÕ%=\x0015å9	\x0016Æ`íaàWt¥`\x0013í\x0014{¢{k5¬©aÍ ìaÂaô®Ve<9^XÞÅêjV7ÆjJªlCAñÿDÇî¨S'k¨YÃ\x0018+\x001e/.Â!×$åËÐSÖk5l¬aã\x0018,õ\x0014ðñJZÔ~T(#\x0014Â^» Õ°éÚ\x00025WöW²§f\x0006)Cç2$j<~\x0008¼ÅèÍ¯é?þùæÝÍ¯oËßÌQM:(Eäæÿe}It4÷È\x00133Àªfù¨¶F\x001d"¢Ö\x0012FuEz[´Û\x0011\x0017PW\x000eJ\x0011%Uô2B\x0010\x0001\x0002\x0017¥¤\x000fÌâØÊÕ¨¡F\x001d"JQvª\x000ee@Kâµ`±\x0005n5i¬IG§Å\x00035\x001e8náÖ2dòV{ ¦\x001auP(É]ÜE}À%é6\x0007½Xo¼\x0016µj±jX\x0008$ý;-«h\x001c:xVÉûDmê ®6<Û\x0005÷êA×CûbªÖ\x0008%D\x0006uP\x0008WUsÏ\x0001Z ËZ:\x000c×:dm\x001cÀ¨\x0012\x0011©3Ën
E\x001b¡L\x0002}ln<À¨\x0012Q.çËëZjyë¤#Ò,vò¬fmÀ°\x0014ç\x0016S{Ø«Öâ],@ã\x0001FehZ1Ayà!OÞù¢E¸Jî$jcWGU¬-\x0015[4Ý)2kYÕÅÄîZThÕ¨\x0008\x0011\x0010îaZÜUt{+ÐX«Q\x0011";Õ¸ä\x000e©©zÒs9(û,Wc¬fm¬Õ°
Q(\x001ao:HTP\x0007q§ÅÕ¬ÍÉ\x001aV!JE:\x000fÿV¤}l5\x001ciumÖ¨\x000cq<\x0004\x0012Tòç\x0015¢d\x0004´Û\x001a^ÏK\x0001ìT
ðÝçïnÏ¸7[\x0016wÌ\x00050¬è\x0011\x0001D,PGÚ7©¿»¾xñäò,ÃWü\x0002¶þ\x0002vó\x0017 Îùì'HÝ9×òE
\x0012*p¬9qø\x000bøú\x000bøÂ/\x0010ë/\x0010·~\x0001Jop bâ/\x0005Rá¨\x0014Ä(~\x001dµë)jßÈ\x001f4
¨h\x0016Ûô\x0005Bù\x0002ÇA¿@sõæ3¬|8çõAÖß\x0001ûtüÛ#\x0019³aþæ\x0004ëÍGXQüdy\x0003á\x001d\x0000]~cZ
Ã_ 9Ázó\x0011|>\x001faÒd·ü\x0005ä^\x0015Î2\x0018þ\x0006Í\x0011ÖÛÏ°.³Ò®¹.\x0005¹\x0016D}l\Îè7Öm=\x0004Ð
q\x0010îµ\x0014\x0002añ78Ú\x0005Úý
Ì\ÇÜT:æE:~UÐ`IKÏu¾:&]dõô¢\x0008@Q?
ëjX7\x0006kl\x0012e\x000c\2åö ÂN°¡
c°>I
¢9Ò9ÌM^z¬Ñk-×°¬M5l\x001a%³ÇUÆÁÂBòòBc\x0017']¯g­çUzÖ°IKÛeÂ;\x001aª¥T4àömÎ\x001e;`¢+~õ°Sö+ÏR¥ÕÃ.W|¬¦m\x000e\x001e;a\x000eï\x0010¼²0I.æ¡e¶<Ñf¼\x001a¶9`zì9\x0006\x0007k#-?ò\x000c\x001e÷9]º9]zìx¹hÏ¹?\x0014O\x0017OèÒ:ÉP+·(·°\x001e\x0016ã\x0005cÇË+àû¹\x001exÖ\x001b
E)\x0005\x0006ié\x001eyö'²UÕ°GX )ËøO}¸¥±'wÿyÆ«¨\x0003\x0015Aóp*´\x000f|Îâ§P\x001bÍ
»|ñæúòìÙ%
<yû¯güO\x001cøÏ\x000f_þò§¯üÌXI<ÿt÷á==jF\x0005\x0015¿Ï{õéë/ÿÛí\x0017ÕøË¬\x0018áý¹!sLå´BÀe75-Á½zùæûËË×¢\x001eðüåÛgWÇB\x001bJ\x000cl`\x0012>Pr\x000fRê(º\x0011\x0003ÜD?¾\x001b¤46\x000fbðÞ\x001a[Å2».¼¨&O»	\x0012-\x001f´1G.\x0004rÖÛM=ùB¹\x001b$þÂ(¤Í½Ê\x0008± \x0012H`F\x001dvÛ¸oÒ(¤Ë2p\x0008é9ËE7e0M}Æ\x0016JºÙWRu}î\x0019§æÔ	3É®t°\x0017$Y¡A3\x0004Öç!F\x0008\x0019b¾tÑZZYËV¿b\x0013&~_=jp-Ox\x000cÔ×2Èá±i¯ÓCA^¥\x0006Ó¿	¹rhZÍ n·ÿ"=j/\x0011Ó\.Ã!L'«é×¢Mh-õ°ÅÄ@)ïMA©ec2d°ÛÎÄ½£-fYK§|î)Ö1\x000f»ýäx§Ññ¡¯%þô°a÷çÙù8ísqÈä!Åûæ\x0005«òßùSü÷»*p{õáæg
¿]þñ>¾ûü~ÒôXÃJJù¤O3Ë¦#äÀuDI¿ÍúêÙÅc
_]>}úòÅë«£º\x001e
râ¶ 'È)BdqRÿBä`@ö°=ÑmÈxû\x0006×y?U8ÄÌl
s
Çìþ(3Z>»qg¤ÜÙFÌöÜÊ:+#Ìæu\x001deÎQé&æ \x00114P÷sF\x0000Ú&»71î´¸8Ï\x0002!à§\x0011q®x$d,R\x001dDPp\x000bsp¹º\x001c¡Aç\x001c=\x0019
ÅfØ)µË:ü£	\x001fþô\x0007ÿ>\x0004Î}ôéÃ¯>~í°Ä&±»H¹ôLq²â0ü1[ñèå³ç/_\x001cëÚ Vª¦\x0002>P)X>¾û|»R\x0019\x0007t¼Ò\x001bxº÷\x0019
)µ=º	Øa<~{}¬ª"u5©\x001b"E\x001fa\x0018Ô\x0011@=Â a\x001dh¨AÃ\x0010h´ç>0)ð\x00165:?Å\x0013¨>qkY\x0007jÐ4\x0004jU®yÍKªù·WÉ	©9\x0011,¬#=/*;µR¯í\x0001ö¢f`Ï®Ì f\x0014`{"\x0006;\x0001¬ëf¨üAöy|óá?nÞ¯§Õ:\x000b#­Q\x001cÖÒ+/\x001f-uÜ\x0000\x0008íÅ³\x001f/®Ö\x0010Ø\x000c\x0013+\x000c\x0015b&\x0010×É¦}\x0015ÚDkkZ;J\x000b¸g=õÙ"(kËú¸Ï®\x0007v5°\x001b\x0007ö¹ÏdZÞs^`V\x0010\x0016øaX
ìk`?\x000cL:Ü×¹üBä \x0004\x0008Z+¿\x0017p¨Ã00Z4Ë\x001bØBî"qæ${øhxÞ
\x001ckà8
\x0017\5DKòd\x0013ÂMFØîµ¹Þ«\/²³u!XNÐ@,\x0011\x0018ß\x000bY7Èzx[`<.AåYL¤2m\x0005yÊïÜø\x000e=ì<¦é|ÙVDØy@d\x0005_Dö§^
Ö#7ÎC\x000f{\x000fRígïA
Éù>OµLLö²nºñ\x001fzØh0\x0005T\x0004,¯±Ü2uS±ïjäÆ ëaL²ý k\x001có´	\ã$1N~U\x000e8ôÿå\x000fª'ºÇ¿Ü|½½¹[	l½>X\x000bÍ\x0016Ù@ð²+@\x0002þþâÍåÅ±9h\x0015/Ô¼0ÈK\x0006yÑ6Oëk+×¡vã\x0016\Sã¿¼¶æµ£¼!eE0âüGòÅyøSþn-¯«yÝèv°:ël\x0019ö$©?ñÆâÝI«¶7Ô¼áá¯oªyÓèúF-Çì\x0019Çð2Lð©í\x0004îOÊºÆ:<Â\x000fZ-¨\x0017·wüõæýO+sìÆ\x0010\x00062\x0003O¦B¿aä%MÃÑkèA\x000eêÅåÛ§Ï/®^¿<k/ì¶f·ÛØin=\x001b\x000c\x0017s\x001aÕëJÍ\x0004:}Ù]Íî6±+Ï3Â½#F<\x0003\x00186vÊ«cù1v_³ûmì\x0018zN_)ÇU à/ìéX¬1Æ\x001ejö°Ý=3éc2{\x0002_ÖýXÎµ\x0016iîÉÝAIì\x000b\x0006K\x001f?®Î\x0014'ßÁÀ{É8¥Ål;³\x001c=ã\x001f_¼x±\x001f.¬¶fµÃ¬*·ï\x0010nÈUÏ\x001b%ìp'r\x001d¼¾æõ¼1Æ<\x0005\x0003y1ìÔsè}Fh¾u¬¦
µôVþ@bÐç>~½=»9»¾ýÓçÛÙx\x0005Þd9%ÜÃ1ó
0IªSÙÅK+eã/Ï.Î®/¿»¾\ÊËù\x0006\x000ee\x0003aãêTRFCÔ Ü!--u/·©¹Í\x0016n§%\x0007N*µùüAFLÆbZ£\x0017;ÕØi\x0003¶¦È\x000e(2<{\x000c`ÆxpåNj¶MªíÜ7\x001f¾~úù÷7+Ï#MÏB\x000b´M$"1Ú¨²M_qðÏ?^<{óòñ÷W\x0017K§2©ÍKª¶y\x0003Üë»Ð+\x0002{\x0016âNÅ³ìÉ\x001dkî¸ÛNOÓ>¡òéÀ/'Rä§ÀîÈ]eîR¥o1\x0004!TÈ\x000bîÏâ\ô¢\x0004ÜS¦\x0007¼ÙàzÓ\x000e\x000f@=\x0002nxÅi/6àÍ\x000e×¶8Þpøh\x0012¸å×@ñìÈ½Pèäö
·ßÂ"8\x0005wüÞ\x001aì\x0014¼¤í\x0008Þ\x001cM½ålZ\x001d¹Þ\x0005mxÈÚ\x0008Îv\x0007\x001b¾\x000bx4³\x0008\x0005ÿK9Bùòéî\x000b>E\x001ftóþãÊäÆðï\x0008Sys¾Q£\x0014âuyüõË·¯IÙô)z¡«\x0017K\x0019¾¨æìµ4ákdþ:ÍîúÓÝíç÷_××\x0012\x0004.rÑKA\x0017ZsÆ\x0007µ+!i²×ýfãõÝÛËë«££¼ª¯`ê¯`¶àK>\x0002¯ö¿×\x001c·^
Ä\x0007¿«¿Ûü\x001d¬2\ßAùô\x001dRJå;,\x001cÞïàæ[ÉÕ[NðÔ\x0010úåìÏïÞ\}#\x0002à·R\x000ffR¢\x001bÑRêï4,Ô&L\x0002øÑÔ\x0013úúìë'W/\x000e³\x0007d®¿Üô-\x0002×)-×P£¥²ÕÆSÛiä[Øú[Ø\x001d¾Qù+XÇ\x0019fJ1s9[Ì0~X¸ÃWy$ø-è5\x0017A\x001a%ï&Î\x00057Üý-âüö\x001a]õòææ×>Ý}^}}\x001eJ)ÒDÝ?S )Ýtª½àÍÅóG/ß^æ\x0017Fyµ)OTàùä¢ÿ\x0015\x0013ªÃ©ú§Õ¼¦æ5Ã¼Q2\x00031Y	t\x0000\x0014oðHá\x0016^[óÚa^{.\x0019sÃ©"\^[\x001e-ýÆÕ¸¾ÆõÃ¸.ë?yÒ}ø\x0017ÊnHn¯Õ5n\x001cÅò ·~îÃÝ`e7èS½\x0008kyusÚôðq£Æ½|1J4ü¥\x0008
ì©²­Õ¼ÍîÕÃÛ\x00177-_ùd²\x0001ç%Jô÷$õAô\x001cwïÿ¸ö2A±\x0012(ëý!ùª\x0002jquñÏ?¼½zºä*ü<òðM*¨\x000bÄ¬ùñÏ³°\x0003%ÝT¡MõëiMMkFiUyBó¥P«¼[S×ù¨¶Fµ¨4À\x001fü¢âÚc\Ø(%½f)\x0018í¡u5­\x001b]XuxV\x001c\x001a¤ 7wm{ÖÓúÖ®m kzY:2ó¶Ôô.×u¯§
5mxèk\x001bkÚ8H\x001b\x000f\x0015Yè×L®^PÆË¾õñÔCÍJÚTÓ¦Ñµ\x0012)P9º7\x0003yVÒÖJ­£Õ­g\x0018u
NÉ5;¤¹\x0012®+¸Ë¥!+pa^\x0005u!ÖO\x001f~½]Û\x0017HÃÕuî±ÔÖgÍpjö\x0007\x0019kNÕº=yùìùåÒã-ÌË° .Ãê£
òÒïi"µáç[êEÉ´zÙ=¬§55­\x0019][+>¤q«=¯­ä¦1¦<\x0011¯¥u5­\x001b¥5ÜõAáytàÔv©emó£ëiCM\x001bFw\x0002\x000bxOrw&\x0013OÉ)¤5zvÊ®\x001b[ÛÑ§ëRç@©\x001eÃ,?²D-fW\x001f½¢IÚ©ù§\x00157ÔÜ°;\x0016fKh.#¨zþhü8Àmjn³;$VXÁõ\x000eYütj
;¦{pÇ¹5¡Î÷fõ-H'\x0004S|\x0008Ñ\x0018Îª"z¼Õ-_,(ÑÿæÄµmnchÇòuðâ|\x001e\x000c÷j[J¥\x0011¯NrÍ´x¹ß×Ô¼f\x0017bY_#enNXÂÂr(±\x001e×Ö¸v\x0018Wê\x000e<
ÊÈxp\x0016ìåX:xCÍ\x001b\x0006yñ^û\î´\x0018e«O<Æ®Ç5n\x001cÅÅ5eå\x0006rÐYíD\x0019eyÁ,­çM5o\x001aåõ\x000bîpy!Íqh\x001bÊiûÿ©{»åºn$A÷Uø\x0002Í\x00002ñ\x001b¾¢eZf$êNÕÜ8X6Ûf·,US»j®æ5æv®N?G½É<ÉA.db\x0003K{¯½µí££]6[]þ\x000bùDþèS\x001dßª´¬\x001a\x0005N\x0017ä ç!°Ç³ÊËË¥ÑË=A\x001dÀ­ù\x001dµ¿Ô\x001dÆ7 H9y«4Gò:ëy\x001bó«Gí¯£ÃwjÊËãf¢\x000br"NDÛ\x0018_=j}}²	Èú¦¥¬Ç*S¼:r[\x000fÜ_=j©¶.ðX\x000f­y\x001c-\x0013w¡ðTçÁ6Àv÷	Ø\À®áuÃ\x0016Ø\x0016Fk@<[àbOäÞtãÞô¨sÎq£yºuL¦mR7+	?\x000c'ò\x0017ºñozÔÁ¥ð\x001c­Ée]&Áxè\x000fVÆ÷:8Ý4óO!piæï\x000e{L\x0019I¦
rQ¼\x0005U¦àò@¿5Øz_×U~ýìkzVþõÓê
\x001d\x001bå=?\x0005¿ìQe8?xÓ`à¯é1ùÍëÅö»yâZWënâ ÏC.	bø\x0018c!>¥ZCÌkY«bm³+ÖþéîÓÛµ3S\x0002 \x0004jTAÌ#itP¥ØÀ/)Þóë§\x0017¯-\x0016\x000cÏ\x0007<m·½¤qW\x0001OãË8\x0016dª%±®\x000655¨\x0019\x0002¥tO,"Õ2H.ÇÔr
RWº!Ò,ÇÜ\x0004¡K²\x0014\x000eX\,b^KZ¼~×\x0007ÿe}}^^\x0019­Ðö¬=y{÷ë?V¦GLÒ{ya\x0001Ï·\x001f\x0004êÇæ9\x0019\x0007_¯ví;O]¼ùËqbW\x0013»ab+ÉjKoà\x0012ÎÒ+\x0007¯kë½eT½ûlv.q3åZs«¢¤+iÌ¾å¡O(Ó_ó:2~\x0003þC\x0007g(ßÁÕ¿Ã|PäÀï@mv\ªønOKGùWpq9ø\x0019ú\x0015|ý+ÌÇHþA>C¬ùøÆ±ß!ð T\x0017Îy(&J!_¬X\x001bû\x0015ªËjú\x0015>\x001b4;ð;\x0004K\x001e'\x000fsu\x0012zÈ ×êúJüó	´cßÀ	?r\x0007}\x0004\x0019§iÖM&íú%\x001aôÙ|Ú_"ÈeFÕ:#ÊPFÕþC4úüÙ\ØßÁç§<"V\x0014Z\x001b\x0019\x0011{lvÒÀ/Ñ(ôg\x0003YG~\x0012MÃYù4Y{Þ\x001f«}ZûK¸ïß½ûý7"(vxF½\x0014\x000f¿>äý\x0005\x0000\x0019×\x0011îÝ'Ù\x0000àC\x0004ÚMÆFÌf\x0007ö¸\x0012£S\x000eåíêâuüOo®Þ\Ñ®ýî¶¡É³A¿\x0014<Có\x000b¡ñÿ­8ÿþ\x0008Ö¾ãû\x001cÝâ¾}{÷%î\x0015Y7
-\x0013¡m=#±át¬\x0013ZY~$\x001cß>»8|r+|r\x0002X7
àÎ\x0000¼3
À^"\x0000­;\x0000f/}®yé{ùäõð·»·÷HQº§µNå%\x0000éäPZ[$Òð7W/\½¼xvè²]ÁA
\x0007=pQ¥[öMpvÎMl1\x0007x.E×h¶±Íô±!NKðÒI\x0002NlBú~¼ÕT¡µ\x001bÙ\ÍæúØLWØÒ¥o\x001a	4*UäæåÕk-Ôl¡ÍaîHMpQçeã²Z§LÙ^<\x0008§[mèR\x0008éÄÙ	.ië¹\x0014\x00141h\x001c\x0015Þok´A÷©Nn9kOBFðAº\x001e\x0003\x001f9\x0013ôF8là°Or\x0016ólüdã\x0013çq$#/Ä)©Ö\x0019¥kU÷i«¦¢Ë²<\x0012?É\x000e½|X\x0015·©nÔU÷é«N²ÃlQ9ÞJt\x0001ÎÄ°Î7t¾\x000eÁ²pdMV
\x000bÏ×z£ì\x001as¢ûì	M·Ï\x001f68\x001ftÆ"ïRÖIø(\làbèhºD\0ç*klr\x0018%çì¶ï*ÿbv®ª\x000fN\x0016$:çsí"ß\x0012:«¶¹~h,1ôYb¤î·)ft´6\g¥z/¦\x001b\x001d,´I)þíe×Øbè³Å¿½ì\x001a[\x000c}¶8Ùç=EÐçlNgsâ¼ÑÛàl\x0003gûàÒ×æÁP%Ïè.Hx\x0012p£ÆQ@£@ùù4\x001d;\x0004q\x0014§Ð)ÞèÆ 1ÅÐgi¸K\x000e×ÓW$ÆlîB\x0014¥mæ\x000e\x001bsæÎ%ºl©2ÅZþ²(J\x00116\x001acl\x000c
v\x001a\x0014ïò\x000cv:wXd\x0017\x0003kEØ*ºÆ`§=¡\x0011ÕÙÚMiÝÉÔY\x000eì¦µ±Ð\x001acÆ-°¾\x0006%w\x001dG1EÕ\x001bé\x001akÖ\x0004|~7º]N,æIêt\x000e¥a®	ì°3°£\x0011²Y_±ô\x0003»¼\x000f.ÑÅ¶\x000e\x001bkÖÄ\x0017k\x0002`äBay:Dú²Qoì°ì°3²Sß*ì¨¿]¬b­ÐÓm{\x000biléµu67X&ÙyÆj/\x0016ç®^¸&²3wlZM5±Q!×y$Á\x0019·í³Æ\x000cÞ¸ÎçúÐdé\x001cärKra(*¡Ý6¸Æ\x000cÎ+6µk,9ÊSä¯jbnuSuÕ6º6\x001fÖiÓ\x0015Ûf\x000fF:\x001dûW\x0008¢\x0011Û¢:ÓÄM¦3nR*Z¢3e²êræÂÆÏÚ\x0018:Ógè ê\D@ÕÒ¦¬\x0011AèÜÆ4'ìöÚìî\x0013R\x000b×\x0011=ñÙKÒÊ}
dQäJ\x0011\x0000Õ6ÎØ±jWyòóÝßþv¿ü¾4¯¡(­çËÏCÒîa£Òï.^¾<8Ý³bÃ
»ØÒçbP\®\x001cLñ	z#lq^ô°Íô±ÑàxÄö6Ou´We£àl
gûà¤ó(ÁyÅ~Â+
û\x0002»\x001e6W³¹.6«x
Sl>q>HX\x0007ó\x0007­^6_³ù>6\x0005¹É,±\x0005¨Î{/\x001f\x0015aãG5\ì\x0014\x0016M
NÒ&>æ©nÚò¶M·V¤ÏXTåÄEÌÒA;ö`Êìóa=tÐÐA§²Úü4\x0017çï­\x0011ÑßãÃzà\x001aC¢û,«¿¹/\x00010\x001a].:¸'\x001cî¡k,î3%)ðÝÑÙ<\x0005\x001ahÁa\x0010ºQ¶0w]A\×ww>\x001eÉ\£Ï+\x001b¨'ÑËå\x0010\x001cËLY·/K÷ÝÅëcî*$¬p5öÀç÷/,\x00048ÉÍÑ¨¡a$S#µHTP³Ëxñ\x0003I)Á¾+êJ [\x0003Ùõ22òb\x001eÓQ7ÙJ¤~Rq\x0019¹\x001aÉ­\x0011íGäÄUò¦j\x0014ÞÊ£ßs1Xäk$¿^J<09IÉAnu&)yþp4\x0004j\x0018)ÖHq5RP\x0012í¤ÀF^cPÒ\x001dÊkµ'yº\x000eI«Æ\x0004¨Õ_.1ÉÛZ0bBy!r{Þ\x0011V256@¯6\x00024	ò\x0008|CÚþ§H
Ðë@ä¾Øtû@·¯LI\x0003ÉÊÓ*ÐQ¦Fçôj¥CåòVÇÄäuy\x0002RÀ¹øPv|\x000e05J§Wk\x001d]%9L\x000fTü\x0006\x001f´	ö¥\x001bW"\x0006)¬\x0016æAÞfZÞ,©(].Áíñ¾+\x001aC W[\x0002C)jbç/g¢Ty\x0004«
4\x0000V\x001b\x0002zP\x00141Ywlk#)ê}ïØ+ø\x0004V\x0007(ã\x0004f¢Q½l\x0008b\x0013îÍ8Sc`µqB
|\x0014« ?h¢òÃ6\ÍÒ$¡Zÿ»&\x0014mú<[B')\x0008³\x001eÍ\x0001¨9YÂXFé\x0018ùlÙ<\x0013ò#Z^pô¾òBÓs4Ý#4üêe£§`ðÊ¡qÛà>\x0003s=2S\x001f©\x000eÅZÅwAµ÷±ð\x0018Y¬ç=æ\x001fTc²Ýýúþáq
m.Ì¦Ø3ä!CÓ{Äz_¸ðÍë³g\x0017o®¯\x000euVhP£A\x000f\x001a\x0004(hÉXpæÜ¸åú¯\x000e4S£.©éX
\x000eÏS\x0011Éh Ä¢j_Éa\x0007«Ñ\\x0017G.INh<ÒªA>¨Ú÷Ô\x0016j´ÐFº©Ë=\x0007X\x0003\x000cg.ÓYÛw\x0017\¦çj ÛùDÓäì³'¹?{É®Y)\x000f`%·j\x0011ÂÒ­?»Ø?»È\x0013²Ï\x001cnÉ®@±\x0006ÅAPÇ!Ø=\x0016:#\x0005ð´©z\x0013è¼Ô:úÙTøçwo\x0017Ó§·jcl´åÆf±¼\x0006ï¹\x001dÉ¼ñç\x00177Ï\x000eõ0V|¦æ3|´<:.B4ÿ+G# )&e?ÿÚ«\x0001ÍüHNáW¿üíîÃ\x0007ùÚOÞ?Þ<â7\x000c:Ot,\x0005:öóf·á`ví½zþòâöV¾öëËWË>ÄÌÏ¤¡39@J­Ëìà@â\x0015¯K¡ÉnÒyr,NÉ±]§m\x0002ýúîññáþñH¸îCÞmKwSÏï\x001eù\x000cü<¹¸ë®M¤__ÜÜ\]\x001e\$<Á\`¦?«Ú\èc\x0006E.P\x001eò¨yÜSÙ&'ôX»K45¤é¤Ý>l¨÷ïÖ3\x000c{\x001a>º!C
\x0019ú!9ç\x0014s\x0012K`é\x0011pnÏ\x0013F/c²I²éLþ\x001fZl4!¯ÜMZ
TÜàµ\x0003ÒÍ¤£#ÙêùËû\x000f\x001fïëõ=\x000búB
ÃIpä¥7T\x0000_\x001e­Â\¨­Â¿¼|uõêòØÒ\x0014u§ÿ¢ïMìþ5m\x001bþù«7\x000foßÞýtvûéÇ#q.pA|
\x001bM^%A¾¨ã<ÇúæêÙ³§g·¯¿9Ð/e¾\x001fâ¿þ,sÁÉh>£Ý5~MDÃpc¤ùêYþåþã¿|ûöî¯wé_\x0015\x000c%Ï!Ûöèb\x000e¾#R
¡|ï	þåòÕ¿|ûìâë¯¦E5¯ß$¼\x0003BkÐ¤ïp=\x001aÒ\x0010j\x000e¾£ÅÊ\x0019MÖ:·\x001fAûð\x001f¿>þçdÊ©\x0008ÉpÛßwù°Fl4sxÚ\x000ci0RÍ*)39ü:o}¤Då~¶Û³ï^'\x001fsHMÌ÷\x000fýñ?ïád>¥ð	íý×äRÞ}\ç0rÊ\x000c\x0017äEC_8·äE+~öÒ}sõí·É±¼xµ0ý÷¸!B%®=Õ±L^\x0010]\x0008\x0010?üçýÃÇ¿±¯&\x000fýìÎÞ\x00072køÒ@5$\x0015!\x001dM|àä\x0016?¥i÷ò]Ðá»%£¸\x0006ÛûàvÄÓ¸ÌFgRòEy¿ç\x0010ÛO\x000f\x000fá=ÉÿÞãTôöÇ¸\x0019\x0004¦ï\x0008ù
É\x0006à§Ï°ò_\x000f\x0019¸\x001dPº\x0016}º\x0008Ò¿\x0017(]D§»\x0014
ÉOHHåùN¢Ùüö²7Í:{óþíý\x000fªii\x0018°©£¸®\x0001ÑZ£¬4^æÉVî®TÓ ¨³7×Ï.\x000fÛÙ¾\x000b\x0006àh
x¶4\x0004î
ø~\x001b=\x000858n\x0001Ï\x0013ù§ú4Y\x000cÀ<\x0008\x0001õ3\x0010ÜÔàf£ÄEàÓÂB\x0016¸\x0017çfÎSqÛÛn\x0012x©.²ÁäFÏIà\x001cý\x0000\x000fÉ;\x0015¸«ÁÝF[¾¨Ñ¨y-\x0012gkûýÔ v¨±ÃVìP°£\x0014-Ôê¤Ü±æ¸½\x0014:j4`Åô\x0017ªxÊcÂ÷%1áj£Àh&\x000fz\x0004^$®÷;AòÖùló>_\x000ei²\x0012bÅç7Sq7&\o²áZK\x0005WÛÚ\x0012¸¢\x0015ä.§"ol¡Þd\x000cµrF¯!W#Ä]÷\x0011\x0006»?¸\x001c\x0004ol¡Þj\x000c¹À©@1Ë\x0004Ú¨Oé6uc\x000eõ\x0016{ÑñÍ9äÔ`"È\x000e\x001f5î¿±CcX`aÁXZÕQ¹È¥\x000eá¤¦\x001cÚàpKtHälX\x000cVàbËá´"ob,Ø\x0012d\x0011x\x0014GË¥<òC£ °YA<pÃÊäDæ«?\x0015y£ °-`)í,^s#\x0005J¶çàØè'nÓÏ oL\x001eõ9_Ðp|hÔIo\x0012Ø¨'nSO×\x0010¸)úRÅD×Ï\x00137ê[ÕÓ³Äi*x!Ð2n\x0007NyëÄF=qzR	>\x0006&¯
K!?ö\x001a$oÔ\x00137ùÏàóz¢Dî ×M\x0011y9R=MsÊÍ¦SN;¬27\x0015£fl¶ê1¹ioù¸Wr
ÊäòH#sÄª¸pJå4Í\x00117x:\x001d*\x0007Z4PÜ3y\x0010¯o;Ì¦´)!RÝÐÑ§é?^¼Oä\x001fW9\x001ftÒ%c\x000c=Ëäcâ=Bú\x0003¡_=Mÿñâ:Q\x001f+]\x0001Û\x001aØ\x000e\x0003+)\x001eÆÈ]nNáã¡\x0015.¤úxcÍ\x001bGy\x0001ÎÁs§\x000f§¬ÓÇ±wWKùÍ.ÜÝ½pµ\x001eå¥½4Ìk
eRr\x001cå9#;-«9\x0011qsõð\x0011VAnÃÂ\x0010Å¢fb^åz
âæ\x0008ëá3">9\x0013à\x000fPd\x000c\x0007©\x0006}Cì\x0007i· 	Zí yz-EÖS\x0002ïDÄÚéQ½ÃP^\x0016¦õ\x0019âFx:hô\x000b\x0019.^hô\x000eFõ:OC)¶ZGË¥È®\x000f\x0018\x001a`Ø v¥ÂÌÓyfµb(Ü©L\x001b4\x0002F
\x0005gr\x000e']Ài\x0006N±3èOEl\x001abó\x0007qcÚ`Ô´¡\x00079ÆÛ¼IÂ\x0010EÂ'\x0013°kpÝ\x001f@À%aK\x0017-å\x0012\x0007.gX3¼\x0013ë\x0003\x000e
pø\x0003¸q\x001d0ì:¦\x0001\x00052ª\x0008Ø\x0014óVÁ$bãO\x0015bî1S\x000c¯¾|\x0011cãípØÛ¹Às\x001dèÈU0IÆ¹5d|²(\x0013\x001bw\x0000wíÍnØÝÑ(K\x001e\x001b¥mnm&\x0019\x001b	)0ÊT`ãîpÔÝQÌÆãßÐ¼O.ÉXIªEùÕ»RÂr¸qw8ìî\x0013S¡QÈG©7C¿\x0002í\x0013qãðpÃãQ'N8>9\x00159ÅKùý>àÆßá°¿sVÊ'@k!6\x001eÄá¡=U`ÃÃqÇ[©µAå5Rt»ÊReõÉl[ãðpØá%e\x000b[CCîê%\x0019k±Æ§±i<\x0019õx\x0018\x0002Õæ\x001b´.Y UÎ±v§4MãñÌ¸Ç3yé$ÉØÑ@ß,c"c}2\x00197\x001eÏz¼ßSÆÇ3ã\x001e¯q¤\x0003ñxéYÆ\x0010O&ãÆãq÷ûÉ¸ñxfÜã!Õ\x0010d\x0019C]\x0010\x0007\x0007Ó\x0007\x001b\x000fbÆ=\x0008uRªi\¶ÇD|2\x000fb\x001a\x000fbF=Èô\x0006Â¹ H]
|\x0001)¹ xªäi\x001c\x0019w Ååâ¹½Ë¡8U¤i\x001bÿaýG:Å\\x0014\x0003¨åQ/Yc¹ãYs*\x001fm\x001bÿaÇýaá:ÓÄ¶¹rOu)µû°Ãî#Ý$eL±1ó\x0016	ãÉ2°¶ñ\x001evÜ{hñ\x001e:r'uN<4,Õ1ö\x00117ÞÃ\x000e{\x000fË+d&ÃÆ5iÆ¢uödg¢}»\x001bw\x001eZ\x001etÔyÒ"ØJ~PS¹;ÛÜìè}	¢ä¨¯6?é¦µ\x001cb½:h;v!µ³³ãÎNK×*íRå\x0010\x0017b{2µk\x001dvv\x000ew3ßu^£6\x0005\x0014rùP\x0007\x001a\x0006\x001bog7y»Ý4\x0011®¨¤ê-ñÉÞ ínîÉî$Å÷ýöb\x001a\x0000G%YºòeQÜ4\x0005â§²p-à"Í\x0004`óh[r&'/°mm"S´sÖß¾÷#PÏkn%>
í­6ÎHÒ §F\x0015\x0019¹a\x00163ß^¿øêB¨\x0019öpwq5:þ¡Ðmn· 'w-ÕÉ:«\x001c'E\x0015d];ºÑ]îþPR÷5ºß&u-íèÁ§¸Ï°Ô¥ëÆÂòI7z¬ÑãVt\x001e\x0018Ò½\x000b\x001d£K1å¡¤§B×­Ùdb=OõI÷ïR\x000cEÛ,}©u½11zq6H{Y@%}q!îÊå¯åÝìÑÛ\x001cx\x00073Å\x0002\x0019]ÆûèN{d\x001aEÕÛ4\x0013³¦æa]\x0019¿îfo4UoSÕÄn\x001dè\x0001ÙeÛèÄÈjvel\x001b\x000cPö¬í4KÁüÃº®uí´°\x000b×>\x0007±Ç&ú£í \x0017·¯®º×\x000b2ÔÈ0¬ÒeGN¸Y\x0000Þ±¡¬ZÊèt"c[¤,å·ù`£ ¸\x0014w"\x001aÙü!¤lkd;.e\x0006¾dó,\x0017²cÓgõñ6ÕÈ®FvãR.¯[Á¼¤,kö¬öG+ÊW#\x001a9#{ÙøD9ÙÜ¤\x001fEwº\x0011kä8~0,=uæ0*p]R(MÀK_}¼Uç2\x0019eµÉ^èùE!`	YíñëÕÌ­#ÙàI\9Ê¡t¡&§\x0012DÊÇ#V37fYo°Ëf$Nr\x0006U\x000e\x0003ë\x001e:}ÃìG-ÍRËÈÑKcx2\x0014wBíÓöéaõ³Áóì]¯¨\x001eO³*wGã6¬eæ4Ãði¶å\x0011Æ+äEÙÑz/ãò;aæ4ÃðiN7*JQNÌNK×2ãbÑS!7\x001e\x001b]vrÉ<óZEøâ)ãÌã×\x0012¬Ì\x0002Â¸\x0002R\x0019J>\x001a´ xx\x0005²ÞÕÛíÆ\x0019ÕlQúAò{ópÿðöìåãý¿þãcjyÛOÞ:7ÛGITz/µ?¨íb¦òÍÕåÕ³³7·_ÿåÕá)\x0015<Öð¸\x0011Þñ¾\x0019|ø­àM
o6Â{-\x0015åª+\x001fÔ®ç~ñNÞ\x000fokx»
ÞJ«&
:àæ\x000foe¤5ê%ã=Âîjv·QðZÊL	\òïEDXNZö³ûÝoc§AÓrh'·%3#Éb<?ë\x000f5|Øxhì¹6eVxSÆD]¬åì5|Ü\x0006¯Ê3\x0016S\x0010¼+ËM\x0010KFºáw×ÉÊ«môÌôVÉÈ#er\x0010,E#ôÐÐÃ6z\x001a	o\x001eB98§=7ºñQz£JðüÒàl¹¶ùR]àOlolým}õ9¦¹%âhG\x001b\x001f\x001f#MÁ¨kèÖÿ\x000e`f!Nú\x00018Ó¨ûÿû¿þwú%Öw©\x001a§e;ÁÉ~U}ÀLæq÷ú8!ÔÐMHCøíÌ*}®ùþ£%vÑQíO
w býB´Z\x0010©ëWÔ\x000eeÅ:4\x0002£\x0003ÑÔ¦\x001fÂ×\x001c\x0018e
¢ãuÞô÷\x0007"\x001d¶F´ý4è«ëÑç9Ý¤;²ÔP\x0003{\x001d®FtýÑz'%QD¡¼Ê=PÕèkD?p\x0016ËeÚ<#þK¦(ÈúÑ-¡&\x000c\x0003B´¼Ke\x001ai9\x0007S\x0016²Á¡~«\x000eÄX#Æ\x0001m\x0001~\x0005¤ \x001eÆãË6Ku(}±p\x0017´Lv[
HQÖ[ÒÆ¼Ä¤(Ñ9xØí`l}ËsqFfa«$
d]´\x0007\x0014:\x0018\x001bï¢ûÝ¸cáAÉbð\x0007:\x000b:\x0018\x001b÷¢\x0007üKÕ=G+ñ$&Æ[Å¸ù[7þE\x000f8\x0008rÑUVjý|\x0014Ä\x0014QlFlü\x001ep0É\x0007ZÙ\x0006nòf\x0005RëP\x0010·«uã`ôùÍÅØ8\x0018Ýïaè	+7]X\x001dx\x0001Åcâ\x0003Õ\x0012\x000eÄÆÃè\x0011\x0017#û5.ï¾L[\x001dhì7ØoÍ.Æ\x0001Ò[1#Ê¼ÔCÛ\x0016:\x0010\x001bó
ýæÛ¥<ï#´¨w_Zb	Ð\x0007F\x001cu0¶\x0011ó­J\x0007¼0&Ë(ÍC\x0003:\x0018\x001bó
ýæäÈvî¸Üèä(®\x001a\x000e¤¼;\x0018\x001bó
#æ[ñ+KÑ·´H$9ëæ 4ö\x001búí7É\x0007ÿXC\x0005"G	\x001cQmÖÆ8Âqt\x0014tO´­èXG<°|¦±	n¡?º%ÏÂáu\x0007\x0005-\x000f`7\x0011\x001bÓ#¦g
\x00173¢W¢$F6`\x000e´t06¦\x0007\x0007L\x000fW~¹ d4%9¾=´Å6+1bw,_U±Ü²´$2áÀO\x0007_£Ï8¢Ï¦øX>r¸5À&\x001eÃx,ÞQÖòÄ\x001awkLâVÿÍÁ\x0011cÎåKÇ:ª8½ù$6ñ\x0018\x000eÄcÁJ%6í½\x0002¢¬¦=ã[\x0019\x001b«#VÑÈ&aJKxÉ3\x001a²´iF3\x00104þö§Ñ4¦ÛnJ&\x001b¤\x001cåB½Ù\x0001Ær\x0011Ë|qT\x000edEòJrhTJ\x0007bc»ÍínN#¿C5§q+bQ\x001e\x0008\x0019i\x000e#¬¦Å	å0Ê\x0015fûuÚ4.Æ¸\x0018V\x0004\x001bËê Ã-Á\x001fxé@l<\x0019ñ0²QÀµ{Ie«ÍöÜi\x001c\x0019q0 \x000e&\x0006^\x001cW\x000bñ@ib\x0007aã`Ì	å,pî½\§¥åD\x001fsÓÁØ8\x00183â`\x0014/²\x0012Rú[&­B<°;b=£mÌ\x001dÈ4FUâîòÖV ª­~Ú¶¯D\x0003Y<ÚÀÁ>Ð9\x0018Íõrã7\x0007¶nu06
c\x0007\x001ea~\x0007Ææ8Ú78íZË±D©w\x000c
Ë
æÀ ¾õ®%ÜÀ\x0003B\x0004Éã\x0005/ï0AIQ4\x001eèxï l\x0014Æ(\x000cH\x0014-lÒò\x000c\x0003\x0012ù\x0003%\x0017\x001dÆ¸\x0011Ñ\x00125zÚÒT\x001eÜ$Þ9Ð7ÛØ(\x001bQ\x0018\x0002E¯uÞ$]¿	b8°Õ ±Q\x00187¦0\x001cy0»")jÆ¸ùÊï\x001bñ#Á·\x0015ìÞCQê71¸9Õè\x001bñ#¡­âöÞë¢Ô%ýdðÀ¨Ð¶.ìáð~²-Â5îó\x0008wóå_ÏQ5\x0019@m\x0012f¶$\x0001ª|ÙVcø\x0019)þæY\x001fíç¨Ú¡zÈlSÄ¦Jé$Õý\x0003+PµÕo¥\x001fÔ¨òòÝ»û_îÞ­[5eJÕ¥M×\x0008^F\x0011Ëu\x0011H]=;»|ñâòùÅÁ}ñ\x00151ÔÄ0Ne\x001dÅT¶ÈcwK(ÀÒ\x0010Û>d¬q
­tÈÉ}Å¯l,©ý#\x001bÔ:M
l6ÈØò##\x0005ÉfÝ U8²TªØÖÄvÓ9f	û©\x001c,¸<Ø\x0003åK\x0003Ä®&vdÌ\x0013ò,Í#4"dyN1K­ë}È¾FöãÈtx±dYÊNzPÁ\x001dx3\x001d \x000e5qØ$d.l¶.HM¦XÎ9c\x001cÇ}(åÌPBF'TK\x0013¤»uëD6xßí`èÆèq72õÀñC\T²æÊÅj;ä©NnÜ\x001e÷#TMáä&\x0011K}¡)#\x0018vGõ17D»\x0012Ki}~Á±¼sÎù²=Ô\x001cé4ì n<\x001ew%\x0014\x00079¾\x000b\x0019SJC@à±\x0001æÆèqgò{æÆ4ëqÛü;2ïª®¦ØS3CºË;Îºc©5WR6dÔÉÎjîM9\x0000-]&c1(\x0017êPo¡Ä \x0012\x0003³4\x0005r\x001d8Ìgä@5#çÓÙó»·?=Þ½zÿiÕ?\x0007 ¬¢÷2+X{\x001d\x0016Û7_<{zsyöêúõÂ?ÏÈjFN7rð7\x0011úd9n¦Áã^Ú×w)t!cÃR¶(¥Ö1¸Ýð'¹ª:X^bÒljd3,e'×IÊá|2Ï4Ú4\x0014!/¬ì"¶5±\x001d\x0016²S¥ôü<­b¥±\x0006È®FvÃB¶_ã'!ç	UN{ØIùdÄ¾&öãBöfQ\x0016E-3
\x001cm,?\x0015q¨Ã°âÆ¥$cÏóî.K[Þ\x0015Ó\x001ckä8,ä\\x0012\x000cRH\x0012¡X8\ÞúØ\·ºØº?·WÌÉx+bÎ2FygY(Ò	Ü:¾qÏGr,V®°\x000f´è07O»>\x0015ùjì¸6ÆimLóé\x001b×§Ç}\x001f=Þ1L'ßç-É8¡\x001bß§§j\x0014Çr¶üÒî\x0014-/e9/\x000fìbn¼\x001ew»V)\x001aÄC\x001aciçr¸¼\x0004²¹qzØÿå\x0005éYÌÚ¹\x0014æ\x00171ãÉL³n¼\x001ev'ôp§\x0019¤Áf:ÅÂ| áy\x0019\x001aÛ\x000cÃ¶\x0006\x001c{`f<÷9bVÅÒÙåÖý.ä6Æ\x001f¶t\x0013P"æ©dBr/±KÉ®NæÆjÀ¸Õ@äj\x0003ne´
r4ìé,\x001d4\x001a\x0008ã\x001a\x0008pÎN[¸FÇ\x0004ùdÀþÁ¸þi©EHÄe\x000fRôA&ÓsØè\x001f\x000eë·nzE\x0013\x0008¹,£wÆ,jÆF\x0001qX\x0001\x001duµòÉ ^Ã£ 1¨Y\x001eÏÝÅÜ( \x000e+ óª\x000c¶Sª¸@Ð"çÅ1Ì\x0002â°\x0002Ò8nn"·Í£%ãÎ8£=\x001ds£8¬49(ûÄ¥ü9È; Ã\x0003/ï\x0003Ì¦ÑA3®É8\x0003+×ü¹\x0012j,¾gw"7*hÆU\x0010¦ñì5âJø`õ.kt:æ6k4®É&ó\x0004Oê1Å±yy¿×:d=\x000b£«º\x000fg×¿Ü¯k®\x001dÕÛÉ< )¨Eñ~¨\x0017§JÞ]ß<¿\\x0018g. ¶\x0006µC Qº6hÈ\x001eo\x0017
Å\x0018#,)ÜzPWº\x0011Ð\x0014\x0012{yreî-\x000fQKK@ÖsúÓ\x000fqJ<áV\x0010Ç2\x0006mi\x000fözÐP\x0011P«Ë\x0011F:\x0019C-\x0019è\x000e4ËwÆ\x001a4\x000eI4],d4;\x0007~H0¥þ\x0012\x0016\x000b-ÖVé*]ë"u 		*
.ybyGG¿\x0014Ù¬'Õ
©\x001e!
r	r\x001e´\x0014ãE\x0010kô©Þf5i£özDï©­w¹ ãGF*\x0012\x001d\x0000ônp\x0002ÐFïõâ{TçÈsôUð\x001e£§Ew
uÒÞë\x0011Å÷ÆÉVÄR\x001dFEeMËÒfõ¤âë\x0011Í÷f'R\x001f1L 74t;(4\x000f#\x001fÀJZ=DÙ¡à4JW¸5\x0007Z|:I\x001bÅ\x0011Å÷4W4&æ¼ç^åÛûÅ\x0011ù«A¡\x0001!Z\x0019\x001a2,RÑûtÃ]*IZ
ÚDz0\x0012êù ù
îèÑMIÚ.\x001f'1úÐ(>(~ aý\x001cõ'uÊãqHå\x0019êOAÚ(>(>ÍI¦ÎL5²\x001aOáò±9¦8tLQKý}DIsÑZ7ÙëáFö®$Õµ
NÔºu¹0*D©&\x000fåäÕ"¶3V;ÈJY{v¦ò´©\ª;M\x0014\x001d)@ÝÕèôÄSÉr¿q¦Ëê3+F\x0000>¹ÒaÎ"!`o]YîBs²
'îD+u}ÇyÃ|Jm
âÿô÷³W÷¿ümí.\x000c%SLm\x0002ç­xÉòê§¥²­i¼îë?½º|þri{@C

ãÐTk&]\x0003VÖWQ\x0002¿Tá\x0019kf\x001cgNjÇåÖÆvêâu\x0001,}Ì¦f6ãÌ)Úv"çOv^ÖÑöpØ\x001aÚn8\x001c ¾$­Ëá(M%Gìw@»\x001aÚ
C¨$e@C®ø~.åÒWË©Î>h_CûM\x000e»3-\x0013Ê-âø\x0016\x000eæP3
GºD¦ÉâgéûéP'\x0014t¬¡ãÓa$ûî;Tå0A;)Õ\x0001\òÐºõ,ã®Å\x0004[Dm@º{
wz\x0017>\x0019tãYô¸kIZ9Ótç`Qâ\x000fñÀàñ!êÆ·èqçb¼/CY)¡Ø¼\x0003Ó\x0011¨\x001bï¢ÇÝ±þ\8zêì uió\x0002·XÑ\x0007Ýx\x0017=î^RTWDM3Õ\x001alé\x000bu\x0005\x0003}Ô{Ñ\x001büK²uû\x0016ÁË*J§Ê\x0008)½\\x001a¼:]#gÍ¡XB¦'ï\x001fþN«­¾½ÿå5ÌÉ<hªðKÌ\x0006¼@ZB&êT[X±ôäæúêÏ´ÚêÛËçÏW û\x001aÙÿ!c\x001cÿ\x0008ÈUW\x001dî\Ë\x0017ÎÜ\x001cfý8ÍU\x001aî,ô\x0017Îl\x001bf;ÊLKW22:Ï4Îfd°\x000bþ»\x0017Ù5Èî\x000f!æÆÐéqKg\x0002Ï:JÐ§#8ï¢ÉÈ¨\x0016^¹ºÅÜ´{eQKjæ\x000b687ËÒ8÷Uõªp{ÿøÓÃÊMî4ËAV
ÒwÛ
6_~¨»½¼yzµ¸Ã]p¡ÆQ\%¸Û9¥K;_\-ÞC5-\x000eÒB«\x0015ãâ\x0007¯ËþhNkj\³\x0001W¶\x0019à¹.i$ÃQ?ëq\x0015Î.Í¥£ûòíÝ\x000f¥¿òâñW\x0006Z\x000e/í6\x0008Ü³¯J¯\x000fÆ~ùìâ	÷W^Ü<ùni*Î\x0003\x0001ã00]\x000céïÇe8é¡C½ý¼¦æ5Ã¼Ô¶\x00130\x000fÙM\x0016\x0018÷'\x0016ûm
l¿|\x0001»×
óRîB.àhO\x0005ìk`ÿå\x000b8Ô¼a\x000b¯¤\ TÓR»û©us"ôø°»qÿ\x0006dí
mZ.­ýéÏ¸ûñîÃÇÇ\x0003Äõß¤sÓß¨££cÌKÏë\x0008'·\x0013úû»ÖwÜ
Ë\x0019Êr8R='ÃSvª·ÿ¡gàdÔ1&\x000eúÉ¸×Ûe[¼8½ò\x0004q(Û²\x001b4Ì\x0002Ì$¨þtöòáíûÇU1E²\x0012òö\x0010yªÁ²\x0004ä@o>Ó¾>{yõìúæê8,Ô°0\x0006»ôU²ùÅC	ð@ùo7,Ö°8\x0008;%\x0008³4Ò#Ãà\x0007\x000f0tÃ\x001aÖ\x000cÂ\x001a)¯µÎÉC»/[AáÐFnX[ÃÚqX¬Ã=°fû5s\x00053õ4Á»³ïßÞ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=|:¢À1c?2>LR¨á´\x0014ç\x0005
!t=Nz(bÝõ0SÆ|¨© ìº-ÚR§\x0000cÈK\x001fl1ñº\x001eçæ_]¾¹øøm\x0017\x0005\x0014§\x0017\x000fßv&Da
¾03\x000bê²äN\?mà\x000fa\x0001ÿ}K3^ýûGÉí»¤7®À\x001eô­~\x0008Sà		Æ\x0014eór\x0010éÅ	ËMØá<üÍØ3\x0003F¹òø©'NVé b\x0014*ëR\±am\x00161nÉâÉP¶ ÈR7(¨\x0012ôX\x0012ã\x0012\x0017åÓ¸!Å¤1×ø ãI722§qÔÇY<ðæ\x0012Ãðk1¢öä]àÜÓÓ]Ò«XQ/M)aÜ´r\x0018\x000c,&\x0014Úôãâ\x0006\Æè¶×jÖüÐ\x0012|\x001fÒOù¡
¤À«îwÆÈE©VP1\x0018
\x0014#*¸â§\x001eÑy¹À^bÁnÅ> ÜåÔP;*d^úC¯\x0017@V\x0010Z{Ö'\x001e:<k­\x0007SÑ,î@ÔÐXUs6	QÉÜ~C\x0019j¿Á±9¹"-?ô\x0017/oo¢æ-\uí\x0002Fö¯««]\x0006Xøq1\x0005XÇ1¶ª²t*J·½\x0018#ÙØ/^-wóQ§Äz¾`"Xt\x0015
RXc\x0013ÇÜ¦m{YA\x000fpËoL|\x0002\­Bé	Ê:CÏ\x0012T#!×Pc	ÅÓ§á$ÔjÊï\x001bî=2°£ÇjÏ0|¯Yo(W?±Ï\x0019Z7Ð8Usg8	>È\^ÀÄØAS\x000eè\x0000pÊ
tÜ¡p:F»\x0000"À-\ÊgÁ\x0003lBn¥|j\x000câ\x0004bvb®ÀhÞ®5ø'{ÿÃÞeìÎùã¢¨¼úþzççi\x0019BBÈ,IâiÕÛËocà$¯>}¾ÕÝ@\x001b\x0015ñJ1!\x0007\x001díØ`s\x0005'y9Ê!Q;Â;;(ß+)bì$óû¹»ç]À»½ÜnÃiqÂö5Hç²»ëõ2¡Ônêe\x0000;=ÚÞqÅ\x001fM\x0001ó(«ë\x0019=é&yF®×£ ÕdxÃÕe	òpQHgò­ÛÁ¶ltUØZÊ®Út\x000c)j¼Âí¶\x0016²»¦ìÛÛw\x001f?è¸È Eä
ÿ³\x0015½Ö\x0014Ýð3xã*MmdÍÆ¾Éá?w÷[óß\x001f\x001e^Ç9ií\x0003\x0007BØ¥¯.Ã\x0016½¿ß\x0019
\x0016>\x0015iZM'²å\x0004èGó§Â6}u\x0014öèÙÙáÖWû§ÕÇîzS³ø÷\x0005!#TX\x0008J" qúSéÑ³d×où$$µÅO5 â67\x0004ñ&%®C{ÞU>bîÜ\x001d\x0019\x0010äx÷U¿ú«\x00180Ø\x0000"\x0019,*RÂ&ÓT·È,0Le&\x0001
·@éTÁH.ÑrM§\x001bKÜ	x#¯~\ÜõîÁ}vp{sùmïÉÕêúÍ]óva1\x0005Í¥ÖÞ`\x001f(O)h;RT\x000eNOþ¾÷äxù<üã­[¦ã¥þ\x001b
À<Þ\x0003±@c!X\\x001e[Õp\x001f\x000e¦Yé4Lì9K\x001b VdÄ*
A\x0005âq»¡\x0012C
LüLcÐ÷NÄ\x0006ô(Sõ¢´ø2\x0015=üøñCýsì Ò&7Ø,öp
Y\x0004g:\x0005çÃvãt\x001b\x0005ÛlË
¾óß±A9fÕl°±\x0004¶UôÓqß½þÜ¶öÓålñáR?oÎYrw²ð·Ê¢ÿåVÛÚñîDûú'bÙ'lôa&\x0015fAïrh\x0007SÌcO\x000bB\x0006±·2>\x0006Ì·\x0018ówÑ&ô¾\x00186¢,¤óÔs\x0010l
:c\x000cõ)\x001aÍÙ-Å@wüÔã9LLb Bý²©!L^¿]xÛ4¿>û5öò~l¡=YÝ¾.ñÁ
J©ì¸Î\x0007+sdtýî\x001ehO§O®¯G'K&í¼¦¡ú«pÆ=<RS\\x0000­I¹ÉXúýâóêÍ×x5J@\x001dÖ
|XÝ_¬Â/ððng.\x0015EëE0¨²NYne­õh!ÆoË³ÃåùóÃó_·ýø³¨Î¬':ê\x001d!ÂísÞ\x0005éöSq,ÀW\x0005
'cüL\x0003
\x000f/¤ÊÂDË\x0008Rüf\x0003ÍÅÝÓ@QaLNFÄ&@Ò\x0008"Õc¥\x000e\x0003ÒÍçR\x000f\x0014\x001d¬
ª4	^\x0000(VïJG­YpW~ñ¯ÿ¼\õã©ý\x0018ôê®Ü°pT,&`ßSK	ûöºõôò~\x0018zùrçMÙ±n¨lªbµ,)\x0014\x0006V\x001bwJXÜ¬×neÝ²T3,ÜÛøJ«eÊ6·<¼è]\x0014S£\x0013­\O²:³\x001c*ãg*¬Ôt\x0017`\x001dÌr$ªÄÕè\x0019P\x0005Û¯§ÁB\x0002ÊBâÌ:hd!N\x0010Wc%YeËàõWûãÍ]ß\x0015ØÏé	\x0007Áëp\x0010ìH£¬n¼\x0000\x0013ÔÿÄpÚZÚÍéK8\x0005 Ëãï»\x0019sa\x001a#³´§T¸¯\x0018ænyæÑn½KËFÈÍ?zÇHª\x0013\x00189hÌ¥c_i\x000bï È¨É×v½ð}\x0012#y¹&2&Aþð¤È9f:K\x001c¿\x001bUG)g\x0004é/=Ñ9ìÐ\x001e6¶ 6æu$ÜÉøáíkãÞDõO
êñÍ±úüåbWè\x0006
jQB(ìÞÄ\x0005ý¡H;ÂêM~å³\x0017Ç[Má\ÇM(¡Ñá9Òë -ý%£²d~õv»hÞ\x000f\x001fb'4ãüû=ì½¼¸Ýy@[HLG\x001e@¡\x0003å\x0006*R¯{£óOw¾÷òðtÄ0g\x000fïÞ~ÜÚÏÜ>¼ÿçÿÛy8`P$
n´$\x0005Òp5£Ã×í*ýKÕçONÏn¿K^zÿñ~Õ/\x0010¢¨ÃÙíÍÃåÕÕN÷¾àÊzµ±ÔB{Ê&3v}¿Ràáìôäüèø¸¡ÿhF;>jMQË\x0007
©é=&´ãÔòA;ì<§[¯7/çSúþÍÇø\x0014\x0003­9øëìvõõâ¶{5\x001f{÷El¹D\x000fî¤ àdçóÚV9;]¾:<í^ø;o#ýv÷íýíÛ\äq:ñ`+ï7ÔÖK+Avx0ti/«õê¥ãtÒÁ~Þ>ìí\x001b%\x001eúnÞ«
Oá°3v¨F&Ãé°öÙÔ¿ôñëúÛêÇ\x001f\x0017ÑQ\x000eDûû/®Voèç|¶º¼½Üùk;*ÙÜëä\x0002\x0000¡YÚ¹Pÿ\x0018ìÅñò~ÊgË£Ó£m;öûê\x001b*ÍBI\x001eÊCþ\x001aËjÞì8$\x000cd7¥®gP |Ð®o¤ê×XTs°uþ~Ü~½6\x0017\x0004Ðâ´O`)
{Ê+/(\x001bpCNeÏZ^½]ÝÝÿ\x0011ú\x001bZbÌ\x00184îº°?\x0008!ÁOû"¬»\x0002ÆØ7\x0006õåXr@\x0010Ie}¹õ\x0014øÁ©ü"¬À1hÃÑ£]«Ä/¥u\x0012\x0010\x0004·©
Òè\x000eUiE¸[ü\x0016úñôh\x0007íyªpÁU¹ÜáHÄ®Vñ´Zï\x0004;Ö\x000ci\x001fK\x001d\x0015Ò*ÆQ'^\x001ck
\x0014ÁeB¯\x0004>\·|êÂ
§N'Þ3m\x0011&håî\x0010\x000c*\5\5ur]`w¡Ùh-ÑÑdÌrZ7¤}\x001c\x0003«¡%\¶Pk´Û\x0015wkhõàPàzâ©  \x0017I`ÉD>g¤\x0016\x0015ÚmWi¯ÂCÜÇ:Å¸\x0016ÓØ#.J\x0006¤c\x001dÞ\x0016ÂZ=\x001dæ\x0010WÀjÅ\x0015áPIü\x00042H7Hw,ÇµCÜÇJ\x000e¥¸&Î\x0004x\x0013­eÔ\x001eËî\x0010ï+¤\x001dÞf|êu¦A;:\x001d¹Lª$\x0012ócI|Òf¹~¸rýÔ\x001b,AÎóõý\x000fÏ
õÌBÞpÀôyá\x0013çWÓ;MW§¢\x0016¡Åz\x0001ç\x0014^PÙéñJ3õØõV/s*÷óc¹åN\x000bÿú\x0001î¨n\x0005.6dFÒ¥æ\x0019Ud+¾þ\x0016«ø\x0000W­%ÙV¬\x0006¸Ræ\x000e\x000bÚm¥GÙøjPfÈk¦òË\x0001\x0017\x0003§b|ïÉ¾ã¥DÅ´âÙ£]×*¥u\x0002Ó¨¼s$å\x001eÏõ»ý
VG+´\x0013O2 U\x000eq£_\x000fqIXY­×&OãÕCÞ×0ð:(rô-\x0002¯#ÞyNÞp#
y'ÞÃ&)bÆÅ+TÒoÎR4\x001bäx¯ä
^?ä},®T<¿<9_`~\x0005Õ0nðf²ô©¶\x000fwÛZ"`1¯L=US²\x0003ÜrÄ»[5w¸~ùäõ« z=òZOÚ£Á0¡ý¶KC¯W\x000c^ðÇi¼áåîñ|èZ?D\x0001ïÄ+f1$µ\x001a\\x0015ZM¼* xDâMYv«/&ùz¨nÊÜB<¨\x0007kÔÄµ\x00009m
{Íe¡°SÄ8­\x0000ÁêF^\x00163zk7c|¸vKý²°\x0018°s\x000fçV.0]QbcÙx=\x0007í¶ÀR2ÛgUÚNbÂYõ\x001c h¢Ì,¹\x001cK~ëÃfçãfZ?¤õÓhÅòOèÊ?9´¶¥ò\x0013>&f_:µZ
VÓ\x0002½àÌjKY×Êr*Xcñ«RX(7ìÁÆêÃ)° õd¢\x0016¯_?Òb½\x001c\x0016
òz°êóÊ7óT·\x0005Ý±áâ\x0012MÇð¾,\´ã°|\x0008Ë§ÁúÜÛZ\x0007;fÎªs¬mÍj\x0019\x0007Ý?x\aS\x0018ärJ`þ5Íh(µ yÊ×[\x000b0Öc]\x001bQµä}T=P
-f
ÁP¿±¤ÕÇ³ãÆü³:=`\x001dh<³î\x0012ÊBqA¶\x0017Ï\x001dq\x001d\x001fñà\x0015³B½V\x0015þ8U2t;\x001b¡¨
\x0000sù\x0018\x0018¹\x000eI!££GêÌ¤YÕÐ½Ï`Hç¦ñ¤Á\x001a\x0016óöðC\x000fut[9;$µÓHíM &wd\x0017ÔÉ©\x0011 Ô368\x0000\x0006-n*ÂÜ\x0012U\x0011!¼­XEßÇT*Q¥\x0019Uf\x001a*ÃxfR·äJ¿¿ç#çjéR
»t°\x0000â§ÀÊ¨£`5u'ðÔ\x0006\x0013`\x0016ë\x000eX-°zÒ5\x0000ºzÜâõÊH&Îkru8owVøq\x001eMì´£U>uÛe° \x0014Nlî\x0002âÆ^¥¬üÑ"à\x0013\x0017\x0001\x0008Ö#+èsZ1\x0005¶è\x001a\x0018gÕlÈª'\x001d\x0004Â)\x0015Ô°Õy2\x0005ÆD\x0010
X9\x001c\x0004ªçëdæ5_WYòv\x0006º{Ã{ËRµ<<g1È\x0000åË;:Á¦eX;]ë]S\x0004k8õ^â.ØXX=Ê\x001cêHo·ëÎnÎsÚL+ÜV<\x000e0\x0014Òæø
\x000f·ôB¢Eb1LîêX³\x00033\x000fÆkç	ÿ`\x001fE1Ë­´s4L`ëhîr«r©¨~]¯«±Ç\x000c·õ ¸¤ësåjËb.F­T¡¡%
DÝuäZwÁ\x000e¹hA>Âê]\x0005±®*,è;\x0012\x0016!â)Ý$¤vÑÛ\x0012\x0016wN\x001dL­®ðúÐ]«h?£v¹UôzMNÉtõ"\x0000qºà¦­âb\x0006srÂ¯è©¡{n&,X×t\x001d.&ãtùÎó(ý¾\x001f4týmõp_üÆta\x0007áOÊ\x0019¤c×G?éFÕÏ.¡í·åùYÉC\x0013©õZ·P»¬¦
\x0019Hm1¼&Ç\¦ëÔ[ÏÃÍ­écÃ\x001f§sCÐu?K¬¦CÑXJ æÛ{?ÔR\x000b1løãdj\x000eyµXBêU
ÅÇtèéÅ¤ÍkDÅÜ½¯ º«­Ëçwj\x001f [¹­Ö£X\x0005\x0013Û²ªV2\x00079S×]èá\x001aîßÿó\x001fÿõÏÿ|uy·³ôß9lI¤|^\x000fªÖ¹ó£ ½Ã§ÇG/GrêÃÑü{JÆíþÁþã(ÐOËË\x001dÊ1¥ÄÜ­6ö,Ð@ºV\x0004P
\x0017f$\x0015I¨?\x001dº(¤-Õ\x0006	òM¤[þ\x0019w¿Cè@@\x0013TrÂIöáùÍåî:áÜ)¨¦¡È¢o\x000f\x0015\x0013Ã$¯ï©,õðüä¨´û8ñ?3þ~\x001f¯¨!'ü³:ÔðPBRåè¬'nx{<"ÝZ¢\x0010îèt¡3%ÔÛÀ\x001béøbïéíêúíÞËÝî\x001c~q(%ÈNÜI`=1äøpïééòù/{ON^nM~~\x001d®ÁßSv=Ñ\x0005	¢¨X¨Pç&2ô,
Û\x001eC;:Kü0½¾Õ±Lak¸¤+~§¯/>º¸ß¡I\x0008Ö(@Ù\x000cÌÀÄ\x0016±ÿruy}ÿ·Wá§¸\x0008ÿùöâoOV··ÿüé¤Ádaðkûpbé\x000c/ðh³\x0018ã\x0018¸Üö_.ýíÕÑóÃð¿\x001cþíÉòô
\x0017 xfóûMüþõ\x000fwùGt;Ã]\x0017
p\x0017Å¨RDÈdù\x0014Þ
 KÞ¤Ëßÿ\x0013C9Û\x0010\x000fàB:Ü,\x0003(~ÿøñòË\x0017ðá¯ëÞS}yývu\x001dµü\x000baÃ[OÐ|*x¿\x0003×\x001d~wcc>ß\x0008k:öÂb]>ß¢ðßVp\x0011©þm4
ê§\x0002´BbZð/ÿlÈ\x001aÔOâ§	\x0019\x001eb:[@æYHîEqÒù¨AEµò<ZºTÔ"Q«d«Dj3#uW¿ÔB-½²4×£#Âxíàz±ù¨yÔJß&lëÓLkmp}@\x00171Ì"VaÍÆ\x000caÄômcvX\x0008\x001a°ÏØÌ\x0013öÌIDh "4Yc°¨Åå\x0001¡,Z©ñó¹\x0012\x001bÜ´éÛ
 ´Bb[X°Bìñ¯úÛ¾z\x001eÃ÷1óíû*æp\x00009:¨ÃC$¥\x0016«PåÛ»²©>}zX\x0000\x001dÿmñÓD­½Á\x0005\x0012.pT)¢:\x0011ÞßºpYBÿzýZlW|ÄÏð\x0006Ü_/®\x0017§t\x0018ÈÌ\x0017[07\x000c]3áDÁ	×Üêc\x0004\x001eoÿêð¸ï}\x001aàÏ·võ6JvÇ6¨&ýþâzU\x000enTx\x0015éd@³X[a\x0005L¥«äìðùr'-¼¯´jÄ\x001co¸\x0012ÖxÄµ©V0\x0000[Y¶\x001b\x000b±-w\x001b²MÎ¾4Ã±!% §\x0018
 G¡­¹!fd#2\x0008ï¤\x001a\x001aq0DöIy\x0010\x0005/ÜEÈPpëX\x001b²\x0016l\x000f®4xB(:<|T'nD~¯î®Þ]ÆG\x0000ÈQªGÌ?.¯/A â]%ug\x001d
4óò,=\x0002\x0011²\x000cúßS½î¶ÇUÇ
þîøiæV\x001aÐ%¾þ\x0003ºH©h\x0001Ë²U½\x0003ýã¥ºú\x0018\x001bDmÒX}r\x0015ÞØ(G\j[KïFîU*Õ\x0006A$gOý\x0014
ê%hk?Lñ.úÇÍb§ã»üp\x000c #[k\x000f\x001a\x000e?Áüø\x000eÞ3à+¡È\§Ü5ã
K­º@ÙBÏÿþÓçÕØ?\x000eRWÄ %E­W\x000f÷5\x000f\x001cÁñö	\x0016NªI\x0006"Øé(WZ»EþËó³£-ä}¸º\x0003#%&qðaIj:­²õ8ïFrA/Êð Ló\x001e\x001e\x0011²lÞS7ØPk';I\x00146²E;Ö\x0008ëò§K_cKç9Ù75½6ïTN\x0017Ö8H	¥õ®Y*¯4áolaXÁ\x000e©Ê·¯\x0019ÅE\x000bu¡è8Ñ2eô\x0007ðTí3\x0003¸ý|õãC\x0014Ò\x0005\x0007/<ç^@ée¶]Â\x001ak§\x001bÇã]ø\x0012\x000b1rø\x0003;èõ¦q\x0013  S\x001bî$ÐECÀxYäï)æ\x0010@ã,¹)Ô$Æ8C%IÒ·dÏ

¾aëú	ÐPL<'Ð°9½ µ)hiL°Æ\x000f"j(Làº3Z  ÖÆáÒt¸ªÝ.ßv-u\x0016Cm¡\x0016QÎLZ\x001d\x0006ûÉ\x0004dmfE\x0016pÓµë¦\x0016ÙYZÓLÒ;\x0019lª\x0016¨£8äÔpÞÖC\x000fÚO&jë½Ç\x0007\x001bs#/êâÃºÚ\x0002µmë´\x0015S\x0014ã\£ïÕX[ôü)§\x0006á\x0014¡\x001aO=\x0011C}Ì'À#Ï(KË£ìÙS¼Aõn\x0002²Êá\x0004ÈÁÓÃÈ|z@zE;õ[{ûî"9¦ ïb?±$üÝ×UO-¼0é&Î@´¨\x001dj?\x001bímÙw\x001e¨\x000f_-G\x001cj\x001d773ÝÛlp!2xÉt×Së6ð°>ÐÐ»\x0005z¾EpÖ\x0003¸.ðÕpW´ß\x001ag*·H;\x001e\x000cöv\x0018§\x0007W%&_\x0005· µdª\x0015\8E¯\x0003'l2²!  ðu`eQ\x0018¸Ü@\x0018Çôc9ÓÈAË$Ý8FsFä\x001aÃª:<g^*\x0006n0£×
wùA¦ïÀ%rU\x0012\x0010ÞMno¯¬II¬a¶í£´Ûû\x001aá¥Rj|\x001fp+5\x0019­)wmç\x0001þrïàäüôl«·ízýéGì}±¡ÛæÕjïÕçá\x001c}U ÝMØáÿ'>kRvï\x001c/÷~Y>Ûæçé¨!\x0014'L+5\x0013dðX°\x0008Yx\x0004\x001a¦bØÅÈ\x0006Â×f­³QõD;
?A+F37NxUY­¥ÔQuMT¦\x001aâ}i¢}í\x0013²Ât\x0012m¡ÔÈð\x00185î±S-²Utì9Ð¢Gj\x0019Ú:V\x0018ç+£\x000eih:ú¸0¤Zã\x001d£$Y# áÈEç]1±[Ñ­©UV\x0012CÚ+]éé\x001b¡\x0005Ý/û9N7+}{\x0017ù wÉ
Ë[\x000fW\x000fßö\x000e®VUÙ%Òñ¡<y+¹äè\x0015ú Eg5èï\x001d\x001c/¶Gz\x0003\x0008¿¢ó³\x000c@Ð\x001a·<XSñ	l<´H¤Sÿ\x0001ÄffñÓ>\x0002\x0010¼Ç\x0013\x001chãÃ2\x001cùÞQ1Yî\x0011Høá70d^YmX:g`\x0011i|±ZÍü#0`¥\x0018;Ço ­4´
bó\x0006Ìöá\x0006·:T3@>|ÕobO,0;õp\x001fÿºJâð5óo-7\x001d\x0014àùÃ\x0014ó\x0014´·%öm ÿu\x0019ëÕvóØ=wÐ ~"ºOþ	.³YÎ,ù¾Kwn15ÄÀ¹bÍÔáÆ ·,×&O8jÊ\x0007t¥
·l1:ØüPÀ4t#\x000eN\x001ba
D@O\x0005Ã³¢ûÞvt­³\x0007_Zòvres°¤(¹­
Úµ¢[Ö¡KZ0á÷ô.æY0¯¿\x0018óm:[\x001eö^¬*âÇ:Ú\x0003)	½ËYa\x0002¤V`¯<=\x001e.·E;Z¸J\x001dN«Â£qìU¼*Ô×ÓèðØ/±ÐËp×\x0003Ýõ¼±º<ÀR5Je\x0012
såuÏ­\x0004VFÿf\x0013¬Ó&ÇãÌ\x0007µÇ¬0\x001dÎñù&WÂQ!iáuyéJÃª\x001cp\x0005Þ²üªR^pg\x001a×²\x0018¤\x0017±äÖ\x0003w\x0012\x00132³en\x0012^\x0005©%±\x0016^Îñ\x0012	Q;qàãù0x!  t\x0013oÎ\x0006K\x0002!aý\x000e^æ\x001fá}ûM~õ<º·¡æfàúû-¼'W\x000f\x0015þ3ÉòU\x0017N\¼¥¹·Ò0yQ"\x0006Ô­>\x000b\x0016éNd\x0015D\x001b²èPCg\x0004\x000fG\x0004eqËÂ\x0000H)2¶jkeäµÙ\x000bå©B(ð\x0016î¹Q^ù^½ÿó¸*à\x0014\x001eïþÏü×o7\x000fu®\x0006eòSËSÖ9\x0006>>µneHÝþíä|««¡Ã\x0006êr
¶ \x000f	\x0008Ý&f­1Þ«dÑmWÁ\x001c~8ãgê\x0014\x00183\x0002»\x000eÂT£+Ê¨ÔL­\x0015û¿»\x0012ÐìMÅM8\x00144ý7¨¼¬)\x0000>\x001fuÂ¤ê\x000f¡<åÍÕ4\x001dîýÛòåÙ¶úá>òÚÑ<	ÙQ©	¨T³"\x0014AkS\x0016¥\x001e^½ùøæóçß{(»ãÙê.\x0017T¼¾¸¼ºªÁø\x0014$Y\x001a¡Éq ±L¢z½ó½gËXOñäðèøxç\x0018x¬&3\x000e§LQã%&\x0019;Í@QV\x0017^çÕÃ\x0003\x000fOñ¶a0ò\x0006ÆÐÏ\x0002û0¢ÐÓ@7^nç\x001bÎÕ«Ú÷\x000c¥¬[Ù»6	ÓÎ6kqõémÜ\x001e ã.jº«\x001f\x0017WØ²°x\x0000Fb8ÍØþ\x0000È\x0006·¢Èæ:\x000c\x0003ø÷X`´\x001c\x0002Å·\x000b:øÃÌSÎ½Sáh%w~a\x0016l\x00059$ÁÊvr¬¥OXé¹DCÐ;Â2Y\x0016>)'_\x000bELs\x000c­qþc\x0007"']èÃ/ÇîÚ<7r+\(NçÞIOÏ ëÊ¼:\x0015Üp\x0015òa\x0002ï4n+r4\x00132\x0007\x0011Ý\x0018³\x0015MÕ CrÈ£Æ?ÓÐÓ}\x001b,\x0004O+\b£­ÀmË|;¹ÃUbÿvà¡Þ·C§g7\x000fW×\x0015/
ásF,ÈbçÇ\x0006í°ÀËRg\x001f\x001f=ßÅ\x001cÝG^6fA7\x0007RrJpàOÌV\x0015ÅD
ylfÆ\x0007-Í&@ó¨ßì½\x0010äà"i \x00025ã,s!ã!2Ìd«'fä[ó±Æ(=õ­Æ\x0012\x0000\x000bFñÐ1WZXÖ\x0004Í,%
zx÷'ß0\x000f«C\x0011´/{ìA«\x0018BP¦iAkP+Â\x0005-mÖ,u\x00167.öÞ\x0013ÚFhÛ\x0008M a¦\x0019kÆi¦£ÎõlÐFÆ\x000bFª&hgè¸ó¿-Øù¸<\x001cÓE)¼; ¹~x¸\x0007Å­hI
;ðp¿¸¸½ø~{Sx¬È\x0019>VZªµdò\x001bÃ=S¶¨_kå\x001f§'Û23·C_\x000eÓ\x001bë¹%ôcÂô\x0013\x000b,R2ÑdõqQöT(åR«ýøiã\x000e\x00178z½ Ý\x0018ç¤\x0017)*¯à£Z
Ïë)Ü\x001cm¾TU\x001c¡\x0005¹X¬õ³L¶üüiõÇûM\x001a\x001b\x00179\x0010W8:5ç\x0014¯¶Â°\x0014ÇS\x000e]\²bÊ\x0017À»ÕÑI¼\x0010qÛçº
å\x001a\x0000ì)J-&fUä(f^OçÀ¬³Px©N§þ¯¼_Ì×ë\x0018²ÃR\x000ey//no/®Q
¯\@ÒI\x001d\x0015]AÀ\x001a¬Î\x000eï²GÀ`H\x001e¢ ß8ºÊøøiFÏé\x0000aCRÀAK\x0012
'\x0003ÎN\x000fÉjá8Þ£{ÄXW\x000eèX\x0002`Öe\x000fÞ
ôØ#*~ZÑMÒ2è\x0012uk\x0003½G/-M7ª£÷ûÕM¤§YTì\x0012,x,v	/²Lµ*t8¼µaÍä$ñY4\x0004bÞ	±©ÔÜè0ë~Y\x0007z²½Óe\x0014'Þ`ix_^Båô\x0006:s\x001a6Ç)	atÔÈ$v\x0017é±\x0011\x0018ájöýj cÃ\x000cÅ\x0014¦\x001e5¬{Þ£§\x0013[ÎBÿ^?\^G\x0011\'á{`i]ÝÜWåDPé<vÌ1\x0010¼KuÖáñÉÙn\
-¸á\x0019O\x0011N.(0Ë=ÕZ*-ËRdÊp\x001fy]ëqy\x0017Üä9£G0ï2nÙ³²\x000c÷Qº÷Å@f
È\x000cä)n)¬J­î\x0012\pRzÞdì\x0012®¦Ô9!:ÜÂÜ¹\x0012ÜõÔÐz^åòÊ¥¥ Ïqîù`%\x001cr\x0018ñ«
öuz6ZÐ Æµ\x0010n\x0015RÎå~É\x0011^uûõógµAµ.Á·«û¿½\o\x0005³V¹:ØÉ\x001eoÆD\x0002È(;Og{/á»\x0013\x001b¶Ã£{{
·2éHs\§#Í@!"®bST¨ZÍY\x000cÍ³vnAYÎÁ\x0016E;Ïxí£5RTÔ\À.Ù\x001f\x001f¿^DvðQ²AÉÖéåêòêêÿ]ãYUN:é5E
ÀÀL0\x0001uÙ¬\x001e-GÂ½\x001d6dªq)Z±e®#\x0002ß*zü\x000c#Ý@Á\x000b­ÓRl¸Nø h\x00126£¤5\x001b¦RÄZpÀ»½p\x0014bo\x0012Ð¨Ç%â±âÉ¥h\x0015Þbàuí)À.ßßaLg%9Ui\x0015U`W`;Àv­ØÒ K<¸r¤+\x0019þvÖ\x0008åûñÓ¶¤y^Ò )4-d/Ì
MlÅ°í¤%\x000f\x0010a9­\x0010EÑÆ`Ì{\x00080jâ§	ÛåÜ5+´ÊD\x0016\x0016çEá
l\x0005Øª\x0015[S<Èç\x0012¶tèù3¬ôA;ýá\x001bÿôöKLÉtPÏÜ§~¹ºZ}]}¯Ì)¢ìWc:ýsåH¸ØðBIÃËãå«å?¶¾c3ø¦¬)ä
\x00023)¶¤½¥\x0014\x0017©Q}LÊK\x0015¯¾N\x0004ÏASc¹¦d(a)&f\x000bÍrp¨zÃÒ÷)àRgµ\x0012ëD\x0006ç6«²YA\x001eumW¹t\x0014ü\x0000éóm\x0018ÅLY5p\x0005¶âgX)V
Ä1áO8Ò`t¬ð\x0004¯ J\x000b/ÚÎäRfrî(á¯4«\x001cÁ^5[Ó¸´§4®ðv74çq§br
\x000bE·¯\x0016ÉòèRª+s\x0017§v¢PZ·ÜÓ±æ£\x000bj.\x0014Þt[/¨ÒÐÈw(t2Ú´­g¢ð©yÁr÷\x0018ãÓYZ\x0015fYsÃm¾Üò j-uÑÆ\x0015-W Ç{5_üáå\x000fsK¥\x0001]Ð\x000e
V×¼\x0017(ÇÚ|Þz,
o}Î&Î²\x000e\x0016,CLà.ÊY¬!i^ÃRñëÅå\x000cnÇò¤kM\x0007ºâó\Eï.ì»O«Xn\x001d#e}·æKÕT¥.²,0ÉEO6d1\x0019+óÃ¾(ÍN`¸6½h\x0002Î-r¬g\x0012D­%õQã\x00141\x000b×}\x0013½ÌÊ£ÂÓÛØ	\x0012&ã³\x0002ó´[\x0005: ¼É®@çh=¹zJiAØë¦\x0005!LôÑôz5+á\x0014)2¹K¡æ<~\x001a½Èu¶¢vÜë,Ug\x000b\x000bÛËc'o[;»ÉA![Ä%ß°-zý\x0016Â®»*'À
k¹Ë\x000bÂç
\x0007ÍCæ#^óL t5\x0017 \x0012þÝDìLY
y\x001917B6mºðîÊ²Õ<%0JL¹83âÂ\x0005'Ún9©
Fï\x001c\x0013z"1i³øs¡h\x00191âÂ6ÁÒÊ®=\x0019jé,\x001c\x001f[ÎG\x000cë¶SMª\x001c!õÊ&ÜÜ%Ë¢rÚR\h$\Ó­¬ºØ\x0011èãã2\x0013ÛÂ
BbØs®mÏY<¥ë­\x0007GëaÎ;C@pmwéº\x0008(ð\x0007b:Ô\x001c/¬ï-"\x0006U}ÉÚV°Ã
§»3ØáãÊ\x0006âÂé Û\x0008ÐÐ&=0ð¥HÎXnxPX\x000eSD\x000cåüûj R¿çÈq\x0004~.×
(ÑÈ2`3î9
f»n³Ýæ\x000b¡ØäÞºDúYËõlÙ	ÄV-\x0014\x00113ÐüNé&âB\x0015¢BbèXÈ¬\x001fåÌÂ"p>'bzrâ-L\x0004*ä5ÀÛ¶ï´]dL@&²¸&(Öé£´ëlÄ 5©mÛ¾Ó&ï»Ü& #<¦\x0019ç8öY1¼é(V>·Ñ\x0004\x0003 	r¨$)K½+#@²\x0011M'î^\x001dð¾Ã9\x0016:\x0013ËÂº¢Bbz\x0017M'ÖYO26GI÷GÇìèTT3\x001b1¼òMÛS\x001fÎ6|uHÃrkS¯©Ïp©]\x0019ql[eÚÎ6Pw\x001av\x0018Ýß©\x0012C76c^Ïªë³\x0015óÙXk\\x0015\»Y-\x00107\x0019Q2)ÇÊwsl$u/Ë\x0002+$êå®íÖ¹û\x000b\x0004O7isïz6ã\x001c¯ËO VÙÖTÜÄB8TÏ\x000eØ\x0019mÌ4oZ\x0015ZRíËòÐPf\x000f&+¬q=L¯oc}*Úå\x0017ð¹ù»ÑõÊc³Øô\x001c^õÔÓÛ{Â\x0018VòÓ²Pá°\x0018®»ômdgé°°,­	I\x001d­bv;É\x0007þ	\x001d Øc\x0007\x0001±³vq{SUÎx#ºöÜ N\x0015\x0006ÃÎÂáðôd[M{FæQ¥³Væ,
n
ÏIZQ\x0010%uYâQ)·;I9ÙÆmàÁ0*kbìC¬¿PE5íåÜ±ÈAÆ5\x0012¸mN(ö*G\x0014µ|\x0017eö}
7<û	S¸³Ø\x000btqÊb/Y[;\x001c~e5
ÅÜ ®íí¦p3FM{dî\x0017Â]~³rWíZÊm êÚ\x000cK¯'pKAiä½ÖÒ|Çwæ¬Ü`ôËÖõ-S?A+-\x001d&\x0010mðä_X/^\x000e
5²õ0:{Z¥¨\x001f©`\x0014\x0014¥É®åØð\­{2Öà\x0019È%9A\x0015\x001dþåÐðbºyaw\x0007·í)]1âö\x001dwpøðçÃ§o1\x000c\x000cåoÃæ×g·«7\x0017\x0015â
ÊÈÜFËxK\x001dÇ\x001dù\x000c@â¼pºO\x0007GÛ\x0014\x001c2uÌ\x0011C±Â	ÔLÐég¡uLR~q\x0002ÂÚ\x0015yqË©Á\x0012\x000c©jjíÉw\x0010\x0000ÚÅ8FKÛðB=àBj
§ÔÆú\x001cTs\x001a
yjùagéË\x000b{ýÇ»(R\x000boÁàÕåûëUM#UÛ\x0015Á©Üe<oÅÂ¢WGO/·	ÕtÈëºçõÈZæZæ2\x0017å£ºð©X¼Þ$c\x0002²Ï­¢\x0003O\x0018Rä¬0©h\x0014ÙÝ¿¹ºO\x0019(n
ÿï8öe¼¼®éÊ\x0018X\x0016¤æÔB¤û[QJ¼õz4\x0003ô8vd<z¾µ\x001f£÷éîcdc"1Né¢QgUr\x001a½péÐÖ\S\x001eïnÂ/n.Þ|û\x000cRrÂ_G¿¬îî.båûËÛ
`­:ë\x0019O%Évöz4ùèÙåË±¿ËòéÑáénlj¡Û-³Ê\x0012KI\x000eI=·þÕ£ð	Ø®g»kÖÅ\x001cêó\x00026BQ¯h1ôý´Z½õõPj
g7×÷ÿüïxL\Ü¾¯ëúk8¥\x001e
Fþ\x0019F9$Ìî¼g'Á\x0016:ÄáéÓ­M\3²x~ü´ «®µ¨ µÁ©ø;ü\x000bf Öözõö\x0012,\x000bÈË>ñåÕÕê}f¿ÌÏX+©Ñ3ÔÔAÑÅÑ£>:>^>ÝæXê°Á{\x0012?MØ1 Ø,w¶²Îç2d?vÔcC3ÔøiÃÎy%ÁÔÐ¤ybÉgÀÇæUSK\x0008YÅO\x001bµ5¹öQQê\x0003\x0003-	*Ù\x001c}z×cCòNü´aç&£\x0016bÔE#[Í\ÚÂ
Y\x001dÕ}ã§mG²®ÒÔé-(m«Ñ\x0016	õØpê©ÇGß´\x0004õ\x000cXï ¡üðÄõ QPa\x0016?mØ©\x0007EmNZ.N«JvÔSkü´QKïFgó\x001aÉV?\x001f\x0017¨ªÆêzñÓ\x0015#¶\x0010d>y©¨ÒÞfÔcçÒ»6lPÓÂ>çI-bç¾Lê\x001aLÀ&\x0011¹Flu
 ù\x0000mlOi\x000c\x001egÄ6 ò\x0018?mØÁîÃó\x001b\x001b69I³-Gû\x0012NÀ\x001fÑj¨byvõ2g)ÜÅÆ\x0005·ê±uì3Õ~lÛÜ
Zq2þÈÈ\x001eW«gøidf	87\x0006\x0008o\x0019\x0012\x0019I²B32ç¼Æ{Æåå³øá!=\x00176Ú"¥\x0014ûãÛ÷¸èQrLð(L\x0011ö\x000e÷Ç"elû-L,\x0007ô\x0002úÄ'£R£Á­ãÃ]bÍ=Nò|L\x0013òV\x000beá´ÃVæ*ÿÇ{DTQ\x000fil·]Hj\x001db\x0016.pxÅH¶Ûª±ß~7ç÷¯öþõÇ¿z\x001a³
<\x001a\x001a\x001eªb!°\x001f¬äx]\x00086\x001a8Þ!ÅÜcìýâYFè=ødü±úCÞ½íýÖ/®Voâ¡tðáÿ÷¾ªc°#³\x001b®S\x000e§\x0012õ¡gz4EüÅñò \x001eJ\x0007¿-Ï¶·tüóó®\x0006ÈÔæëðýÕå]ÝÙ­(¥¬Éò%)6ú~qZ{\x001d>=>z¹í\x0010½z{ûãÇÅ¦)~ñpy_åxãÝ{uvºäY5hôÍóûâüèl«Û­£M\x001bk:­ÌáNã(\­¤ÈÊÆU=jiÓ\x0016NS'£B\x001a95
9SØh!_\x0011ì·÷_o\x001eÖ\x0017BX»«½³Ûëª\x001euae¶\x0002ö\x001b\x0015ê¤ÖÈ» Ã\x0002^î>?Ü®$Õc\x001f,\x0006öìûî³kJÔaãò@\x0013Ù\x0007d:;ÏM`9Ç#C`ÉgxhæO\x0004f»sçJ?Î(Hgöãµª\x0013Á¥Ó\x000cÎòS?\x001cÉùñÉI¾Ë»Ñ ßDöp<vöè84\x0018.ñ¹-õÄÔ±«ô<ìÆß_ñÏ½\x0013æÿ<¬nï//n÷?.¯ÃÖ\x0001¥\x000bx*õâ|d\x001c§þ0L\x001býóåéÙÑáéÞòß\x001f\x0004\x0003{ÔélùW£N§Ê¿\x0004µxøn®¿õVw¦¾6\x0004\x0005knM\x001aÓ¥ÒaL+ò\x001cZ?*¿±ch\x001bâÛ¸ïß~|ûåý¦
Ü«o{\x0007W«ËºI\x000f\x0016õB`\x0012 õ\x000b´Þ,'1WÐ;,¥\x000föêß÷\x000eGÛç¾7Gë|ú\x0018I\x0018\x001eª>GÜTj%\x0013È8ÚØ¡v\x000cßÔû·Ìl\x001eÃÞéåÅÃýÍíÛ
|è.çºÄÂ]ã¥Ë¾P9ZËÝ£ß;=:<?;9ýe7ø£í:\x0011\x001c\x001c\x0004h{É0\x0006ä°ÆÔháÊ4òd\x00054O9Ç²ØpÀÈLIk ½Au¾pÕW'3 \ÛNvW¸=\x0017Æ#95ÛÑ¥üæ\x001bws·é¸U\x0016Óz6ê°=±§ð°x¢D·ãÔí\x0016ÀeúXq±³9_o\x00046ê¿Ê\x0008.õ÷ÿcÓoÉßjr\x001eÃ{Ùa{\x0010pÅc²l·\x001aMKÈà<ø÷ÝÄæü¯JÌïÍÇOïzÄ\x0013v¥ä~a0%\x0018lP U¶øhÕúØ\x0003LÇöcÃ¹\x0005WÙÇ¯Ó%£X\x0017\x0002\x001aM¥)'LÜDÂÔ[*l¡ðZ@@ÌmÕP;4\x001dðæíëwæc?iíôæá>å~U\x001b|²s\x0019Mõ\x001eÌ*j\x000c¨Æ[Ö¥Ü¯Qk/#K(¬\x0006fHg\x0006`§
ùuá>3\x0010\x0007\x0013\x0018ÞrñÓ\x0002¬rs í"5£(\x001aÔ\x001dÏ\x0008\x001cÎ`TÀ§\x0001iN~\x0005×åÆHG2nÐªsNfP\x0016fIí\x000b­s&3\x001b\x0012Â2~4
©\x0019´áâ§9'j@_bt©J+Hnl¼\x0000¨¹ë7¹ßéÊ'ej\x001dåè¨FÌÇ\x0006ÊñÛ\x0000­4¹\x001c~\x000f·¯Â"o³£¿v=´Ðm3
.lÔ+àZãzC÷°7£Þàjf\x0015'Z5N´RÝD;ì(à
ÉóÂ&\x001c½+¡ckú6@K/©rs»\x001b\x0019Ç\x0017£ùRÕÐ:BëFh\x0002YFPÉæzôè¯\x0018Þ\x0001éÛBÌé´sñFLkCY't°ç\ÐZè¨ÀÚtw+Î¨¯¬cà\x001cKkC0ê£âÜ×7·×~úNNäÀ¢×)À)%7Å\x000cÄ«\x001fw?þ&\x001dè½|yÿzs{qw	5*\x00157¡å*Wý\x0008NbÍ]ÿDaF;ü%è_OÂßÃ3i?½\x0006½Âøif9>® £i*ªçYU{Kë¡áÉäd\x001b4ù4Ó ëf:\x001cT_%FÃFµÐÑm\x0016?m3msóRÎrQ\x0018£èbx^ï>ï* ÁàWÕ?\x0011:kßÎ5éBò<Ó£\x0001ójhhN\x0013?mÐ\x0016©Ï&\x0017Ùý\x001fw\x001f\x001dåÄ\x001aä8â§Øä^0Í´6löúË[ÖCCõ+o<:ÈåKZxÚ27	f´$¯\x001a:§:·@{A8V+C3\x001d\x001en´ íhOÞzhiß8Ó^æ\x0002zHQÇ.hh'ÅÈÄ|Ä±gü4­
º8VàÊe)jTÎ¹\x001a\x0018Íâ§	Øçua \x001cgYÌ<¸_	Í\x0019´wMß\x0006j\x0003M\x0008ñNñ¬SVÐ\x0014i\x0003Ù\x0019©£8Aú¶PKL\x001e´ÒwúïÞ¦eÙ_,EêeÚ¶\x0003
\x001fãY\x0007Î¹¨»áäÏY\x001b*6oß&dÐ
ãYVÔRûUÅG%´+©\x0005È3ï§o\x000bµq²ëÒëI.P)²Guo´:<@¡ÑYü¶PkAf\x0001yjÔÿæ:ú0>ZWHÍÍ÷ë¯w± 
\x001cw¼çæØ{vñý®*Í92G
tjÁd7Å\x000cµfã²Äa°÷ìð\x001f/·æfb\x0007Þ\×wéV\x0013«Ø
;=Úä\x001ae6·{âEþqÜ¯\x001f.¾]ßû
L3îÕjïÅe\x000cS¾¸ZÅ2Ç¬IíK£c\x000bê&\x0007ÛxNë\x0007KÊ·zq\x0014#/P/±k \x0006®Úøg Vgý!i\x0015µh\x000bOÏÅñ¨ÐäqtºóCó,ÿ\x0014v\x0002ªä8x.¡M5\x001a5<\x000e\x001e\x001bí¦ïL?\x0008ÃJ!%©%(ÊQr{dÊ(¢oØØÙF!XÎ¥T<\x000fÄ¹\(JÜjSFâãHül#á\x0016\x0016\x0017äðv9\x001fÁ°qqÅé#\x0011Qó*~gÚ"&çÑ±\x0018ñ®ºèaÑ \x0006ÿS!!\x00070}g\x001aÊn\x0018ªÂþÀÆRn´Q?g«GOpúÎ5\x0012J­7^ZºDÂÿ\x0000µÇ´\x0005¾I#\x0001Uôi$"7Wõ\x001cãoñôÅôc7®\x0012Ñ0\x0012(ALßFbÉ\§VþMÈ*q|´UÃ@ Ô6}g:·,½$\x0005îé\x0004¶\x001a\x001bî\x0004ûd´¸wúH ãÌ~úÎôÐ0¸¦Ý®Á,IÃ0EÝêa\x0008è\x0006¶¾3ý Pv»LÕ©\x000e*ØÒ0@gåç\x000cCFÍ\x001d9Áh(j\x001d%7ÑÐ
'\x0015^$ãiNÇÁ!ú¾ó\x0003ºnÃ @,(À¡É«Åx?Àéc×Á~úÎõ
¡Î\x0000GÇ®Æøfj´J¨a àKß~\x000cHÚÏ)íµË¯\x0010ïÒ.W~´æpú@¢æHúÎµªÈG£½Dm0\x0010ë-\x000eäç<§DL \x00114ÆmÝ6Á\x000caùú~ <\x001bm=}$Qs'}çzáæÄ	
#a\x0018áWáo½(Âk\x0007FâfÛîVÑ®­gÙéà°ôY'ö§\x0004}÷Ów¾àob­¤mbÈ\x0001«`%¹|Å#ñ«×zªbÂ\x000eé6ÉÃ
\x0001Ë³4¡æRF¼&ßOxü\x0016XVç»Ê\x0003:fÝtñiÐÆgÑU),å@yÁrÿ¨\x0006É\x0004hTlé.å3¶¥Bè¬ÇËAÏmVh\x000fM÷Ú \x001dË®At\x0016~\x0016º\x001aU\x0015«|Ï^Îç´åayVôö27\x0014Ôã	öÕÐ\x0010öíB¿\x0013¡¹Ê©.gh!)\x0001C\x0018ÕåÐPÅ¼/º´iÔÚe±<bÞÖwÚÇ£Mëë!'@t\x0001S³\x0012t&:l>:<Æk\x0018ë©áw&ê|ÉØ`Î 	\x0003Ð¹ýBÉ%SCíbÀ¬ZvêØÞW n!id\x0005SË¨è-\x001bW\x0008dæ oQ
s5%`\x000b6Úx\x00025ÔlÈÆSOõ\x001fJejî)ø!JÜV5ÔØº®0¹\x001dÌövý)øh;	ÔPÒÓº®A2"Sª\x001c$3Óòà¾ å¥\x0006\x00192Î¤j¼_zò!ÂÛÐìI\÷\x0003@
[QµnEz8Ý=n\x0018¾?\x0003òÌk\x0003l\x0019©\x001b¯DÕå\x0008pMO´pz~,+ò*UPçvÐMÔ¶SóÑÙ¤6ä\x0013¹â³Z§
L0%Zì´z\x0015jâÄÔ|<ó¸p\x0005.
jHÅP²u+2Ó®Ôyð¢8u
5Ìuë­\x0018úNï)\x001f{ªÓ{ò£2\x0013¨!¤õV\x0014.KÂð\x0003!uDZ³Õ1xÓà´^ \x000b|#à')QÖªf\x001eÃ¾Ûp"sîÃÁ\x0012Á[ÑÒVd£
%ê¡!R\x0012?m÷¸y\x0014Ö\x000f÷xVóÞ1K·\x001e\x001eÒwTBç#OÒ	5ëó\x0005]÷µi¼\x0014¥K7"óÎâµÈù\x0013¬ C±\x0006\x0019\x0004Úã§mA^\x0014\ÍâòvÞ×¸$(í[÷ s\x0007Êdgj\x0012*ñr^\x0017\x0013¤òìÇOÓÚ0Ø\x001a¥k\x0008¦¼ê\x0012 f%\x00063Ú´ÚÒð*¤¬
/p¥IUÅêMN­¦tìsëÙw÷·´4ãç=8\x000c\x0014º\x001aÕ|÷\x0003s®bTâÃxIÆR
5¨|©FkZØü\x0016g>\x0017bJjym GÏ¼Ô ¡®\x001a_µñÇSy/3xPçö\x0000ÝxLKeº3OæeMºïÚ+1«µd MØèæ\x0013$;ÆbNsÔ¡8Þ;§Øig[í;)\x0015å\x0012y'º3\x000f/ñpÝÎ:Í1i[ÝÓR!
\x0002\x0004Ô\x0002Q9Ù\x0011\x000eþnVj
Ôá-iTN¥³ÙC;w©×¯\x001e\x000b¬ã§íÌ3]Ê¾ ÃTR\x0018T»_µ\x000e\x0012àhÜBå\x0012Ò¨oïCÅHkT\x0015ÔFSó`ëBi\x0015kÆÎ»Ñò´\x0015%¥¹\x0017LIªL\x00053 éÛÄ¬-¡@\x001d
^/Rc>¸6bÖ÷V0\x0017bö´h¼`DNÑ5Ú:zCvLÂÖrTC¯\x001a[ÄôuaZ¶j\x000842\x0003²D\x001cï¾U\x001dWE«ë{\x0012\x0019
¦£¦G¹0X¶«\x0015\x001fíÓQ\x001d=Ô¼ÙOÍs¯\x001f#]vD
Þ\x000fX#³b+°PÓ·	\x001b*Ã01Z$±y_Ê\x001etvÎø\x001c9]¼Ù5		Ò²0Ü+Z$Li<Iø¼O\x0019\x000eîûéÛ-}îAcUáH	 Pó6\x0007õ»·ß?Ü¤Þ¥à¬î§ÅG¼½'«\x001fUÜBuù6T\x000b
0vT	\x0018ÿ\x000b{Oçÿ~´U;ã\x000bÈá\x0011R©üÌuÁsGeLqòM
Uâ\x0017©ä`H1Ãü+ïs±\x0012¹\x0001¤ R\x0010*Ê_¬ã\x0007q-ÙWØÎ¯³Z\x0014¤ÓÁÎ\x0001Ó²|ñJ|\x000fø~\x000e|{tAº\x0019á3I=OÊï*ù¡]*>\x0003¿³6wAézÌrÈ\x0018ÁØ^6[\x001dÿÚ«s:¿I¤<lR?\x0008P%©\x001c²ä_\x000fq¡øiÆ×w)\x000cHH-¡\x0014Ë@ï~Å\x000f\x0005¨Â\x0003:0\x0018\x0018öXz\x0003jFEE\x0012uüpX?ÇâQ./Üí\x001eýzjLE¥Cüà½ðr\x000eþ®Ð\x0011\x0004ÉÏí¬ zû'ð\x001fcP\x00121yýd[-	Ka
\x0018§`·,­ã\x0007Gë~üÌ0ÿÙöÑ&'Þ\x0012\x000f
U²âßJ~H5jõÕÈÈÁ7NC~[ ìUË\x001f\x001dTÏqþ@\\x0019Ã\x0016Zb´.%fgÙ¼~\x000e»
d/ií;Ô¼Ì½¦*\x0010 ª\x0017\x0000?ÇÂ\x000fvO"·ùÔW>\x000b\x000eÑ&zSá\x0015ÀÏ²êYn+m%Ç¯6.«yI
x5¿\x0001þ\x0019^,
)xk\x0019çsÈ\Q¶EºÅUüÉè³,ý\;\x0006KM
Å?¿ÉÏA2t?}gà×ùØ×\x0017*Ìgü2í:|èï¾ÍøÂç$wí³Ó\x0012dóq\x0000%e\x001bü\x0002|
éÛÌ\x001f{Û j¾Ëmn \x0017¯jü¹\x0007°IÝaê\x0000Ë½\x001c­g-1»ÙÏ£)¾­\x0003¶\x000b¼{¥s¥¡§z\x0014\x000b\x0011Ö\x0006ðþRÿù\x000et8FG\x001eóÿíxõþâ¶Âã#yÏãuß¡W\x0004zL¤«°ú¡áóé.vhª³oÄÍ\ÏîòÑ\x0019{\x0003`£G¸±\x001c-«V­`÷íç`Og%9\x000bÖua\x0017TN\x0018T±j
Ù-°¯½ÔëÙ5\x0015 ;Á]îÔa³½/©*¬d\x0007;Y¬ÙÉõì¢=.¦¹¦¦\x001dV¾º\x0019í
Z~iô÷/®_|ú+honQNûùÍýêõUU£\x0006èWÉÑG\x0015é\x0016\x000eyåxMÅy® =9Eqíç'gË'Ç[åµ»ð¨b>ãH(¾kËéÜá;^-ãTæ\x001c\x0007VHà¹Çóø\x0001Ô2\x001c³g\x0010Òç^\x001a"ußb)ú1Ø¸\x0011Ý2\x000exTÃ_³ý\x0018,\x000cpMgcJvH©Ö\x000fåÃ×Ï\x001f>÷»4=$úÓÏ_V·u­¢Eq\x0017Bæ¦ál	æÇ} çøôðÙåéÖnÑ\x001d1¤sÛL«tfEÕ°þw¯
\è2\x0002µàêl­	Ûµû¤\x001e<?Ç
þZd\x0010±­È6\x0017¤YÝC¦ê®pµ#ÿ)ßê_\x00019f¦åê*Q/ß_^ÜÖõ<Ï:Ì¼%uÚçÐãM\x0014Î¡\x0015qÄ^>=:<-\x0006%\x0014;\x00034¥ßÛ\x001etn¶ãè¨d¢µ­\x0013Ý\x0015vEf<ºµêG½ÞÕÐàHT®\x0011ºSõWGKæÆë\x0015\x000b¡ïÜ·û+ßëHÜcþç¾ùpóåKÝÝÒEg¹w\x0019;Û^ÌçývØ\x0007¿¼x±õJéÀy|æµ\x001bÃ{+Ûí-L!ï®6òìÕï¤LN7¢\x001d7Ø'Ã3Ö[¶çjù¼3}NmßQÒ?\x001c\x0004ºt;¹ÍqXÁI>w¥gw1øp\x0012¸Ë!@Á\x00155Þóâ÷Á2{Ä^ÙkrÔáé!ä\x0019\x0019$)Ä5/3ToË\x0019M·Lr²gì\x0004'ãÌä*ÖBÏ°NººbR÷uB§¡\x001f/:\x0000\x000ee\x0010z\x0005îÑØVù\x0010÷BéºCê}\x000268Hí\x001c«ÛtÕç:ïËî}ÉgpÈSsn\x0006òîAfDvÓyK¶÷xFM1ø»Ï\x000fìµ÷&¸Öû¶ÊÞÕÿüÇýó?ß_]V5\x0006P&ÇeD×\x001cÓk\x000eßfEeïxïðéñÑV­ý\x000e\x001cü5ÂÍ\x0002+ÅuÔäÝâªÈ0,§^;¿'SwG6Ùï¥Ïù\x000e[¥ä«»?®Ôç^ëòãÔv½Õð\x0000¨°?­0(Kk¹µÔñÉQ	À\x0019Û¬ï&L¿ÿÊ©ó÷_\x0010´\x001dþüýñp3XwÐþkÕK\x0010´\x0003\x00166\x0012L¸\x0019bùx8¯(ýÀÊqµ®ãp²._m\x0003ö8i5þ%9_ßr÷Ç\x001f=ÎWï¯WUUvaâ³\x001aÒ\x0018\x001a\x0010Â\x0012dì¬¸\x001dòÕÑÓçËí]UÄÅJ><\x000cOWWW«÷5çd8)iU¿"µAcVÙ\\x0012ÎÇ'rïÕÑ1Ä]vSæÓç/MO ¿\x001e%¼Ëb7G¾ßý}øãþÁÏ×è°?¾øZ%\x0004«¤<qç4µÃ\x0014«õè¹tðÛá³£çè¤?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9{@o¼ýÓç?ù¥Þxy¹]o0W\x0002ç¹\x0012@o8ª60Aïu\x0000_°®\x0015hÜ}þë?.ÿ6
®\x001eþÀøîæúý3
øÇ%òÉ\x001d
\x0002ÅI\x0008«B¬¼ï^¾xVá\x000e@\x000b@Ä÷ù¼tFÛPÇ²\x0018M¨ÈN(%0Á»Û\x001fýÚ¹K\x001bpóÙäÎ!k\x0001ys!\x0017!íV\x001e\x001aÞÜþÚ&Xäm6ÁÒ"%-ÒÛqq»öê®
¸Þ_]ª¿¼_xßãmßp±ÀQ#ª,°×a×(?n-ù?Áìm}WýkµÀÈíx\\x001d\x001dEÆ¡\x0018ôsö5¶ãáóf@à»\x001cf/\x0001mrôÑQ2È½Ò´\x0001\x0010å·ï%@åC.\x0000Æ ½·|dbìÈ8»}¤E\x0018	´Òè ÷&­\x001a\x0010Á¿?Û\x0011!m]¤SóèAå|²1HîS/
(ÜRç{d\x0008Õ¼G"!â\x0004rÃ©\x0008ÀIN­¨Àú^c¿\x0001\x0011e\x00197#B\x001d¢È#·cØZ@û  ¼¦é\x001a!é\x0010=~°ü¸x¨Ts\x0004¹7ÜÖ\x0008þuÓt|$³)¢\x000c0ñ{ãjÛ\x001190Kð§á\x001aQ×tô\x0019MOã|{«F\x001bðÀ¿î\x0014%\x000e´ÇSAkmÂØ-Â)I®M¥E\x000e\x0011Yç\x0001àzG/í¾ øfDX\x0007û$}¶CÂ\x0012u#ûCCáD]êVÝÞÚÇ ÉÏùùSX\x0006¹/ÞÞÜ]ÜÜmÑjî0¦üUð^ñ±éH\x0015tzo éèéËó£iÌkH\x0014ÎÞ\x000e	ä´Î.
îÐãW'ú½áÇðàqýP(gé\x001f¤jí»ODöçë-GX$ÀY?"ì2·79þòü
Ñ¢ý×Ñª\x0007U`ª%LÕ\x0001\x0013äfé6\x0006ÇÖ\\x001bê\Ø[bÐ\x0008S/aê\x000eà'\x0018)5\x0017RYÇ\x000fÂ	³·ð·\x0011¦YÂ4_ínú%LÿÕîfXÂ\x000c_ënJ±zéâ«Å¹H="é79v¹\x0012I²C&a¯Ì5á\x0001íÌlDa	\x0005\x0015íØý¥ô8W2Iv\x0008%ã
råX\x0008\x0006\x000be\x0012Îrîv¿±×s%dTúöÓ®pÚ\x000e^£}q\x001an¡pNsIªÝ_øÙÓ­pº¯v?ã
glÇiÀfË5Gp\x0013\x001d\x0007½â$¿{58ÕJ~ª\x000eùùÛì§ZÉOÕ!?y:'ùÓ~êlÒù\x0010LÙÏ	r^­Mº¯V~ªüT\x001dòÓ\x0018áPuÅ&²·p\x001a¿7]Ós%?UüÄ
a\x000b«1-'²\òcCÆíï:kÄ¹ªC~\x001a\x001b©qÏzPMÔRè=W2\x001b³¿´\x0011çJ~ª\x000eùiðRf½	Â\x001dnï8\x0004iFa®dÕa%@#F±WH\x001cJ*4´¥UÈÍ8õ¬:¬dÍ\x001bù\x0015¹h2#!ÖÉ°r_)#Õ¡À\x001c¦Duà\x000fSqi0Ü$¬ãÇ®WÊHw(£4¸>Ãt6;\x0006(Ë0Ã\x000c·]¯ýá\x000eÙ	ßºÃB|ê8p:5óí}¿ý)ùíÇ\x0017?ÿõ#Â|zsýaIÇauë0\5§òR¤½Ý[Q|ôÝ«×òéË\x0017Ï7 ´KökEé(ý×2.QÆ¯\x0014¥^¡Ô\x001d0288)Á³+^³í¡õ^½
§,á¹§9¶ :JAÉ;d¿Ôaã%ã4axoÄ)Wï<if&°³a£(åN±@~ñÑüÔS3Ðê¹ã?øªn)Æ@îÇ\x0015Æ_]]¼Ë³*þ÷¿ÿçßÿ÷ýÕ[28Ú\x001e\x0006Ê)9ÅµÚÚF
Êì¼¿:=:Î3*\x000eN>]/\x0016*pÕ\x0012®êk\x0015µ\9l.°D\x0010¸$¨ý\x000fíxõ\x0012¯þê·×,á~¸*\x0004\x001báZ.à\x000eÆîmhÇkxíW¼½îþcs\x000bz\x001dæ?û\x0011@\lH+Ik%Ív£J\x0000OÞ³\x0016fo§\x0016õä1÷Ù7\x0007ð}\x001c´ZVý \x0015\x0004Ä[Ám<\x0012¥2ß õ\x0012´þ\x000f\x0001m Í\x0008h·\x0004í\x0006ît¤)\x0018v\x000b@\x0017¶¡ ö{\x000b] Ã\x0012tøÏØée\x0012È-ilÚQ#Éu.ØÃÙ$Ü³m» Ê½å©}¨WâC\x000eÉ\x000fSPck\x0018ûZ®ú!b¥FÔ«§(GÞ¢VLý¡0\x0001ã¹ÔÎ1j÷\x0000çR#êÕ[\x0003Q	Á
\x0006»Ûb ÇèÉø~Ú\x0005Q«k­F®5öräªFËd\x0013èà5iÅ\x0007/\x001a%\\x0018ù¤Î\x0017­ÿ\x001d[¢,l¸|¹YúÙ16c÷5zDþüç¿^|ü¿ºý÷¿\x000eo~þùnÌ\x0005ô"ï¶.\x001d~¯È~þÝ«£×¯\x0013ðWg'\x0007Ç/¿ûîüAO%Þ×\x0011µc7j\x001cìF½ø\x000b¡Rj!ß[ÓûJwÿ\x0000
£««ÿ+ß\x0011ð\x0007[ÜÁ(pÆ\x0005Ïq\x0017çÀ½>ËÑééI¾#à\x0018nò\x000bå*\x0012pû\x0001Ü°áTeá7ê2ÇÞ\x0017æða\x0000ìÅ\x001d¸ã\x0008n\x0011\x000bUM,¼\x0017^\x001a&øI¤©ã¸ÕýZ.%\x0016®AÛÍ¶r×\x001c\x00192¸µ\\x0017í\x0003L"nµº_+¥ÄÂ¼n|:?ÁG5èðW±÷\x001eà\x0015i\x0001k`m'XçJó´\x0012yÌ\x0006@\x0015\x001c:òa¯Ðè@ëh]'Z\x0013¹\x0015}qjõÖ³||\x000b­\x0005­_¢õ½\x0017\x0012\x001b1·\x0019)
ïÈÞâÖ\x000e´a6ô¡UÂºW]ø\x0013-h¥z'ª\x0005m\¢{\x001bm\x001e!½)ß
\QÑñ\x0001K®\x0001íÂ;Qbé´m®æÆ¹ÄËÈ\x0016E(4 ©ëw\x0006Üµ¼í\x0014¸J<÷\x0008
 MGù.Òõ<\x0016´jV}åRA®ÔìÕ\x000f¿\x0019Ü½\x001aâ·ÛÝëwxá{|m¨¥¿\x001fûôhà\x0014óýòãÁ]ÜþøázCË/òRÙb2DâªÔ®Ø\x000c{\x000b	é~òúà¿Î¾yþ¢Þ÷[ðª%^ÕW\x0017?\x001a-2bÂ¡ÇÅ"×,ñ¯\x001f¯]âµ_?^·Äëzñâ\x0018wRÇ8C\x0002÷àÞs7ØÞ\x0016¾FÀöþ³ë\x0007GÙw7Wº{Cá®»\x000e­-M"noý\x000e2æG_>\x001e±÷]?¹6Ä;\x0007\x001fy¹Ö]ó&{¿Q¿\x0007ñ½(¥(P7pÁÒM:\x001c\x0014pz\x0019\x001föVs5à~Éi´wu\x001eð\x000e±\x0002üéÍ-^d\x0000óáêj\x0003Á?:¼.\x001c*ÈÒDÁ¶°·EîéË3¼ÃðËsð\x001f`_` a\x00054t\x0002µFw!\x0019(Ùhzo~+N\x0014ßl¦¸ïùôO¶f!MÊKeó\x0010MLê"ËöWÉoNBû¯Ì|Þ×	Õ,¡>¨*`ª\x001dwfµ;RËý	­Pí\x0012ªýªwÕ-¡º.¨ð09Ã/°¶Û¬]é\x001cÜûü·B}KQö`ÊóÇ<Ýùîøy\x001fßmk\x0002\x0005Æ"r?\x0011¸¤2Y\x001b~\x0001íø"y¯\x001flBì
d\x0013 pyu{ñ)Õý´t²ÚCùc<Z8\x0014È4²x÷U$\x001d½Iµ?¥´V©\x0014"\x0005-Î\x0019@?øÙÅÏ\x0017\x0004÷O7×àYí%\x0002«'2
6"\x0007J­v}vôÝ\x0011ýýË\x00175\x0002<ÿÃÛ[!?p­Rj\x0008¾<X4)»Í/°\x001d_|ütù)3he%S\x0000^QÌeñ"à\x0000¿,ü£¼7Láøèõ7HzÃÊ\x001bpQWp\x0013.¤Q\x0005Ê¸\x0014q>\x0003®{¬7]¸Ó²\x0005Wne~\x00198Àlí\x00010â×8ñv\x001c\x0017X¶áÒeÜë\x0018rq\x0000Â
¤Ã£1ã°@jÛ¯q»J³
W`ëÌäTnÂå37A\x001c\x0006Ç#5\x0003\x000bô EÌ6n\x0002Æ\x000fò~g\x0017°<\x001c©
4yø\x001e\x0002SYä\x00020/Ë\x0015ó\x0013v,Fj\x0004æ©VÑ\x001bI÷ËÝrãâ«0 6¡\x0002
å4mÁ)Ò	X°ñÏ#ÚÂ¼_\x0006S¦	Y\x0014eÏâ\x0004d4\x0010©\x0011b¾m#lÎs 2JÏ\x00012éÆ\x00119U\x001b2#*ïÍ\x001aàì\x000bÍ§¹adÄRÕÌºÃHL;$dJÈâ=Sq\òó0¤6dÑSXd6\x0003c\x0012Q|\x0013®\x0019Ü\x0007Ù,û\x001dØ¢´ÌÀ¨¶kez¯&\:\x0013If\x001d®°³\x0001IN¡\x0013vh¾\x001a¯D³¶,ï\x0017³´è´uÃ°ëë«»aXo¥?2\x000f"ü
m£fSìëadDFÖ¸e4Ù\x001aï\x0018\x0011oârÇü¸¸À~gÕ,ü#ðI\x0016¬Uy\x0000\x001b·øyÊVÛ»\x0004]$\x0019\x0019µb\x0003²À¼(&l\x0019ü\x0011ªUöëÂ.çu\x0008©@\x0004qq{\x0008~Â-£á_À\x0002Eñ=\x000e´¢£Tö\x0006À&$H}Õ*ùµ)Lï(0\>IÌñ»qûi(ÙW·c ¥U«ä×H©\x0018	Í\x0004ïðoIQîØ=î¹\x001edØâ«[e¬Ö)NÅþH6cAC=nñ¤´Æ=Å\x0015§Ø\x0014n*g\x0019Ç­Xtu«ým\x000e\x0006¸5
A\x001e	%tdIg©'¼K¬FÔÍæµ×4k\x0014Kq\x0019>Ë¨Ã\x0004`4V®ÑWÅö\x0001(\x001c\x0012YvÌN¸dðGèfëZ9"\x0000\x0002`"óy&Çm\x001f­Æã\x0004\x0018ÖÍ¡\x0015Å
4à*ÅL3±Xöl{¶°n²X'îéúk:Y\x0001á à`µn5°¥ç8\x001e®<¶\x0000&`²Wd\x001c?K\x0003ß´[Øù÷ñ]Òõçyø.Ç\x0015&ÒsÆfcñ×WäèÐÇv[ñ×ÇÁ»Ö+¦}w¢Ó«³J*>\x001cüG%öðôiCæd10$MËÊ\x0012(Ã\x0006Fb\x0013HFD\x001e"b9\x001aåR\x001a\x0017\x0012êéÓ¨.#O¢K#YÉ%±÷Lá{&1H>ö¢¢äqeS:ÖK÷'\x0012÷@CûB6\x001b\x0019è`\x001aS\x0014¤Ç\x00190\x001b2à\x0014%¸º\x0017í!Y±\x000bÉfß\x0017C²%1Ã÷MWM+6-R\x001f\x0018\x000eKJ\x0007sc¼¬÷D¯~z÷ù:Mÿ± lÒN8{åÝÅ§\Ró04¤mJOã¨Ë\4*T¤ ¬ÂU,
\x001c½r|ô¦ZQãxÿËO?Þ¥ä?ÆCðçÛS+ÝåÁñÍÝUn¦{\x0018=ÏRW	\x001b5\x00139@ËÁ\x0005áöë·Gß¥6:¬j=?­¶Ò-Qò§\x000e\x0018uO\x001d\x0005p"M\x0017\x001a'fn@´\x0003¥Óx\x0007a7/º¶S\>\x0001Û\x0019\x0004·f\x000bOCG¯¤_7\x0003ýÓÇ_®ÿyÒ\x0008§7ÿ¸ýpy»á8]£ÑYÇ\x0003¤«;öª§/ÿxöü¤:ns\x0005æÇ|] hzÌ×\x0005æÆ}\x0005 B¸½u©$Ç\x0010ñ+AòúòöÃ\x00069g\x0018Äe9b°\x0000!éûà\x0003å÷ûMÝÅ}rö¼.ì\x0016\x0018á\x0001áO\x0007FopÊ^Æ\x0018òøD\x0001ö.\x0005ã\x0001ã~;®\x0003#<\x0001üiÇ(|\x001aU0J\x001a
\x0008û(©n\x001f1ÎÚGÆ)º Û\x000cÓÆÌ¦[éÉ$\x000e.R8\x0004`º½þàV\x001fþ$ÿ~jðP^âÏéÅÁw7W7\x001b°E$èÏÙ3\x001c)âsZ\x000flO²\x0006|Å¹?:øîåéË-à\x0004ðg3$\x000bÿ\x0019»õ\x0012i»³\x0019 ,Õi¯õ~\x000f0ù\x0006uL°&üÙ¾MAI
N*«)eè\x0008÷ûmÍí»\x0004+Â\x0013\x0019,1¡T4JûûL¢íh$ÍöS\x0014&ÂbLí\x0004ð\x0001í¿äÛ\x0001á[m7I{\x000eªIvýª\x0018x\x0008¯Øk1a\x000cøIú4\%+©ÆÕk'\x0018çqK:`aîàeBa\x0005×é¢å>a_¤¤óy:2\(KÜe:ñ\x0003\x000e^¨ÔÕ
ÿÿWs¯!\¦
\x0017l\x0019\x000f\x0017\x0003Q òp1Ø2\x000e@¨\x0018=H\x000eÒ¶\x001c¤\x0015A\x0013ë\x0018*Bz«,¾\x0012I~\x0004Öútc5Æ£]ù ³~d£\x001c\x000eÉ¶XÀá½ÙS#=-Å^DHuP\x001da½\x0002\x0004¢.¨\x0016@6`=\x0003²l*LEØ\x000f¸÷è¶#¢Ñ²\x0011!Ír¤-2¢ìÑDÒÃØáÕè­uÂÿ=Ý%çõêÃ_·D	ân~¦34^àQU`Á½\x001aïÕóWuÓù§»»pñ·$Êa-1G\x0016sÛ¦<\x000c4Ï\x001bÁQT=h\x0000°\x0012·È½mãgâ\4\x00023k®ZP¡ ü Á\x0006·>`WæR]SÇBêSxzs÷ñ\x001döm±;ñàr\x0014*:°æEOFSy3x\x0019ûó\x0010O_¿>ÆÞ¯×YQ+d`G\x0005×ÌÓ¸Ñ\x0008Æ/W\x0014\x0018M}\x001e6ý\x0001Ï6d`Oå\x001e´&d:?£Ók\x000c\x000f°Q½Æç\x0006dôñ\x0019\x0019hÒ`3²¿ÝmX1®)¨ãH>\x0004vgUØ[N¸þp\x000e³\x0001\x0015ÍKnAå]nNHVÆ)\x0003Çh«µ\x0011\x0014\x0016ÕâO\x000b(°Ð³ 8\x0006ÄgK\x0006­ÁÊ+ß*üìßªOi«hJòÓ[¸W\x0017ï6Ïæ:Xò qñ0vít\x0006Wêè¸èú­\x000fúçeT3\x0007ß~Ü\x0012 ±&w°)\x001c[Õ°)@¢5GßöAå[mô\x0012\x00120·CRVåi\x0013
Öc\x000f]äN5RË`Zíuj\x001eÃô×Oþ~¥1×ÿþ×ÖP>y0Z\x001e-jJ\x0018¤Rü=ö
(@³\x001d\x0010ØRÉ}\x0000@ÁÒ\x000bç#:ëã^A°\x0019\x0010Ec6\x0003\x0012Þæ\x0011`J\x0018ð·$\x0007a(y\x0005ºÞ\x001bBx\x0018Ð[x§)[õü\x000fOá\x001f<Áö´7wï0øòêòööf8°©J 9!(Ë}dðâx»Ñ{À7çÇ\x0018zyurvöò\x0001\x0003qº\x0015N×\x0013¹\x0011%ã\x000c\\x0010<Q\x000b`Ú½ï±\x0011¦_Áô\x001d0%ó®\x0018íavÇ¤ñ\x000cÓîï0k\x0019V0C\x0007L%hæ\x0006&ÛÊüw[pºýáËFq3¶ãÔ*\x0010ý^\x0014Ñr°Kq\x0002Þ×þ\x001cH\x001bN\x0006qâ\x0010ÝæýDýå\x0008§!2-ûTpîO·6â+²çÜ
e7Á\x0002ç¶B:Å¯Ýí/»oÃ\x0019W¯=v¾ö<@/
¬÷¢ÇNU\x0012VcÒs\x001cæêµÇ×\x001e\x001dµ¹G°ôó  NEÖ0ø\x0012ã§ÎÝÂ\x00043u\x000b7?#ðÁ\x0004\x001d;XÊz\x0018©Y-_O¿×rØ
TêäCïbÅ`
ü5O®\x0001[2Ü`Taá	*K\x000cNæ	\x0001`N\x0019ï´Ø|§VñgG³\x0008x\x0011#Ôá»s7ö	Z»Ø,~ðÍå§ãnî®·¨u\x001cëh³áicÞÔJìpïÞ\x0008ÀÙÑ\x001búæàøÛçU>\x0005Ö°Â\x001aº°º95\x0015úð¹\x000f\x001fÞh¤"\x0015°+÷\x0017Â6c+¬±\x000f«"ý\x0019c\x001c- Ç\x0017l¥ýUÎÛºDæeTA
xL	þþú\x0006ïê7o/®·øQ&\x0004î+Ô&pLÈj»ÿñ\x000f¿½ÄÛúÍÉÓ£:ð\x0019«^aÕ=X\x0001
·\x000ea·\x0002y¢ç\x0013"Ö½·µ\x0015k\x0014K¬Qtí«g±k\x000eõ©XJðÝþ\x0004@3Ö°Â\x001az°:çÉxöZé<a
ì\x0014Ueôþè{#V)Ì\x0012kâÿj7VÊÕ%À_{n¬»\x001b«²¹¦ÒRfÕ[`Ô\x000f\x0017÷dÁEÏÞJ®]ë¹i\x0010Ãw\\x0008+÷UÛÑæÉ+nw\x000f0¤ºdf¹ºLä,O¯.®7\x0004\lô&wø*ø<s³\x0008\x0004
fàþ\x0002ÂÎrz\x0008Z\x001e½¨Ñ³ø2)ìÞ\x001a\x000eü\x000e9ò\x000fÛ{uðtSÜ1\x0008´\x0002z.YÔº\x0012\x000fEË¡\x0016ý­==xú@éÛ[b\x0015s;í\x0019ÿøåÞ&¸Ä|óH¨FFÈö\x0016ü %»\x0014h\x0014Ô67A¯Óß¸\x001fþ|áþvw»`i9þð)sã\x001dÝ\x0002ª+Ü[#2V\x0007Xo/>Â\x001fð»w·¿;ºýðïÿ÷ý%â
È\x0016xàÆ:\x0007\x001b1Æ\x000b/â0¼ æ³£×Ç/_üîõùÙïÎ<;yrüüM¦È\x0003ãëù³§µ^¡ÍÜ-½huL<m	-ò e°ÈÓ@`ÕT°Ð¥\x001b, Äy\x0002k\x0019¬\x000cÀ8\x0015lfyé\x0006kQxe¬*G\x0018mÌ/\x0019¬
6s¿tÅ2uÑB\x000b\x0019l
¯g°f&ÖÌ\x0007Ó\x0015\x001co§\x0008«Ïõb\x0016ë\x00074SÑfn´Z&6\x000fDk"Nh\x001d\x00128%´òÐfæK²io52Yç[un\x0019mzk3L7Úìù&¨,\x000f,OLÍÜZ¦éV\x000cÂ$\x000b7I\x0004Ò
V\x0017Fc£'a%âîu6Uv#V­ò=XÏá*òr&Á%6þ \x0016Ã\x0012R¾	¯­¢tÎ$¸DQÓ¯tmb«A¸ÊåÆ\x0008ÔºM\x0004\x001a×7	-ÑÖÌ0\x0011¤9\x0014Ð*¾\x000b¦\x0012MK\6ýpC\x0011a`ê*Þ\[î*\x0015á¦_*\x0008Ö\x000f\x0018$\x00180áJ?uwø¦\x001b®Fë ¡
"';\x0000mâKh\x0005¹\x000fÐ\x0012\x0019Nÿ]ði(U«3³#n®aSAø©rHrF^Î/
sæï¦«k)u:gÈ\x001cÏh}ÈE?(tqHÞ\5S¥1N¿JÓì	cQDdÆf£õS]\x001dæØé¹Òîú¢Ò02L»+§î.\x0011ïô;\x0010!u¢§Ý5ÙM\x0007Ã\x0011Ërhw§\x001aåLÇÓ¿»Å§þ?Ü\¹ÛÜ©h£§s\x0015ÖåÍÕ¹É\x0013Ý3\x001fxsÅL©ËÔ=ý+Ê]À\x0008''"²ÁÀ¤¢à\x0012O¿ÏS\x000c\x0006\x0011â¡pìó°\x001bÁ\x0014»à\x0012ÍÏ\x0008\lFN\x0006C,îoJAeûFÌ4\x0018P(ª\x0011&UâÀJ>\x001aué\x0003\äe!Ò?µOúöý»eð\x0019Á/\x000eoo>|Æ¿ÿÃÝËb;n\x0004øA©i\x000eüÜ¢­^æ\x0007?:8>{ùüÿàßÿáüy­Py\x0005<ÆFËr7Ë3
\x0010¹)È«=<ÇÉ\x0006\x001bx|ÌÙ°Ä.èP	QÓÎ\x0003ÈsÐl\x00109øÇÅGÈ¹ Ð\x001fâ6\x000f[v\x0003Ès\x0008m\x0010¹Å:ÆÁ(´ç²xJÒÿ
÷<Óþ\x0013÷<ÖÆÃ_ø,³wJ,ÍÜìªz$ýÈ9r5
Ý$Jt];\x0004¡«¢xÔtè\x000eã6é3zaÒ@vÖñtÕåÎ$µK/t[<Òwpß£J¤ißun\x0014\x0000ì¡Ä_dü\x0015ºüáÓå-êRüÿê[ívåúñ+èÓå¡î;£\x0008<m~ò\x0001¤\x0005È\x0019\x000bøÿá\x0000¤ übÂ\x0002~CÑsû£yûËõ2ÿwñþ:5^l\x0001*\x0000\x000eEp\x001cmÊ%v?!N4Êª\x0001£g/êéé\x0005,Êô}m°(©÷ÁâVî6\2\x001c\x0000,iì\x0012,oé¶=¹Í°öó\x0002¬`ÁVÅÖíÊY\x0005Û1XGÛ¥UÕÚ\x000b\x000c\x0018\x001aq)¬Ú\x0004Ì\x001ef\^\x0005Í¸üè~íhØÚÎ\x0011)Î²æDÏH[º_ù\x001c­õ\x0000åF`\x0001Ë=Ó§	\x0018rã,­¤ú1La³S\x001cc=á¾\x0011YÄ´Aú´mËN\x00188\yØ\x0010(4Ü1Á2â\x0007ù\x0018,ÚÇò·\x0005	 xiÇ\x00132Ór½p£L&ümó³3â¢Ìóù°,Lz+M=µ»\x0019Z¢ÔÃoÛ®)\x001d<oEfZ\x0000kR+OÈ¢\x001f>O^¦o|Æ{\x0010ýY9iòK\x001b¥\x000bt¾G ¥«æ\x001b¯Å1ÂÚ\x00104ÛÌ@Î

E`²cðqJ¬¿mç	ÉÓ®Y\x001a×
\x0007ª(-\x0012­ÛÜ\x000c-$hÃx°ËL¾kNSe<\x001chô| !V£¨[¡t ¡YvxZ6\x0010\x001a`ñù®©ÀwMzw3´DÇ\x0019\x001aUº	àÛù,Ö¼&ÒK\x001dR+\x0016ê	ÊÐ2sLú¶A³£C.8vÍy\x0016\x001e¦\x001aÛ\x000c
MümSR>\x0015Mä\x0017\x001a2\x001b9è)#\x000cß5=*qU"1Mß¶]3òT¨ó\x0002ë}Ò®%âã´kª\x001eîÞ

s¶ùÛ¦§ppÖS \s\x0003 E¶oËÚ ^v²\x0019ZHÐ\x000fTÝ®)Npò@µì\x0014k×·W\x001fµ\Ä×ÈOoî®¶º NÂsYô*°E\vAã`©¯lËZä§/Ïá×-xi_7^°(j¤çWà²PÏ\x0012í[ó³
\eéÓ
XIØpÁ¡\x0010\x0019p4ìãûU\x0013\x001de&PÎ\x000cÊ#{L\x0015}«=æ4òÜM\x0006o\x0005­ôíße!S·2î²Kv\x0019lÞå &î2>;$BÚÖþ]\x0006õMÙo$éå\x0005Ká· ªeß½ß"ä·_ûÅøåÒüÓýô\x0003Î4À\x0001-ø9»üøáÇËëwØÐúÛË÷w\x001f®¶B\x000e:±=H,=y\KüÛ\x0019²\x0016ÕÚ£³×Ï¿9yqÝ­<;yvþüt\x000bf\x001cÝÿ\x001cÌ!ßf¤\x000cº\x0018m°¿-Ý\x000e£Ëa/ð4$UÛëXueûvÚÇô\x0006áO\x001dA\x00033S\x0010Üe×i¯\x001dW\x0004+W­\x0008nAýçÏ½ú|±Èä\x001fýr	ÿéÁÉÝûËk\x0002}ðêæîSB½Å¶ðXêCa3Cý8\x000e\x000c»sª\x001aý>úþäÅùÉÁÉù³\x0017\x0004þàÕËó7Õ¹Ô+ü¹1g\x001c¿ÖlxXEµJßXÆ/eíºáÏ\x0006Ó8~dF¢è ¥;uj7Ëà«û1ð9\x001a=\x000c\x001e¼\x001dÖ=¹¥Ë£¼eOÃUÇðç,ù8~/FXFÔ\x0019¿\x001c
¾fóáÏ¹òqüÆ§ñÔ¸ÿ1°WºÄëÝ3cøscÊ8~K1KM\x0005²XÓâJÌò×ÎÉþqìJpIÇº\x0004_ÐÖK_M;\x000fàÈæô$W\x0000²3QÙ¥\x0015HN|JcË\x0012ª\x001eoÇ\x0012nþ¦Þ|\x0014.ÎåÂÏñO?¸N£
.®?]¾¿Ý®m½å²9ì K5NÂö»\x0019L½mìÛï¿HC\x000b^¼9yvöº]`ÙD\x0018Àa\x0003¨Á4H²´U\x000f®\x0007³*¹pjl£NtC¸Ñª\x0014AEO1r\x0013´®Söm´ËÖ\x00182¼Ü\x000f(3\x0010¶ÔÕ\x0007¯\x0008ì`ÔcÔ
¨/>}ºù,\x0017\x0002ý\x000fw\x0017·>\Þö\x0015®*\x000e(Jë¹Ç4x®ðóº\x0006ù\x000fçGgom,\x0006UWú^§=]9wCÌ¢\x000f»õØåô¢\x001a`<]BÜÏ9·­Ä\x000eH\x0012(UÁHÉMÌ;1Æj:¸\x0015#Îz*Ác)þ
\x001eðÔÄ@	ÅZØ½\x0015`®Ôè\x0001hM\x001a\x0000jN¨PJ{bµ\x0004¡\x0015#Åóz:ubrJ\x0018\x0015ç\x0017Á,\x0018gAÌFs\x000fDé\x0013¥{jmÕv\x001b öËàft¶{ *[\x000bÒ¶\x001aJ¹\x001bVN®jÎ´bÌ¢²\x0007£	iÊHÂ9Ðð2*>h/«Q£FÙ¼í\x0018\x0004Õ `7{ æJU
±|µÿ¯\x0011"±]ÂÛrnY:yéQzóIj³\x0011"5YwÉ\x001dË-2\x0012,SÃ-2\x001cuzÖQsku\x000fHÞI\x0006©1ù6Ì®ñwÖNRCu×a{ì\x0016à^jÊ FË\x0018ëÅ\x0017­\x0018©º\x000bc)àIY¾å°]ÍoÅH½Ó=\x0018¥å"W	ïjE@ýí
Ó'a¤é\x001e` ]¯´£³öK\x0003©`æ¤6é\x001eè®q©¹CÐ\x0004²tBºªÛß£».¤ã,\x0010æÒ½cû\x0015v½ÿ±\x0015$µDw\x0019¸k#\x0004Øl<j*\x000f56V]àFÜ\x0008Ý%#U9mâXFJnÙ\x00049÷?wi\x001bÇ>.\x000e«ãæ\ýF Ý,ÔõÜå+"u%Ë³\x0011Ì<cm5ÓZ»6R¥a\x0008RÆLø\x001bÉÄ\x001dÖÄYW\x001a;-]Á;)E`×m¦ÝHjkîòiJµÀ!4:EiÆ$¸¹Ë\x001a×ìÔ\x0008/òtSÄXº&ªÁÃVÔÀÜQîú,rRf;>*{H+Hj[î\x0004)¸Ï0r¹VðÜêTµ}½\x0015$5+w½\x001a\x0006E¶ÑRÒJ²Ù³Áa63@Fä²MNK2*ªB
ì7Dk"W!Mò\x001b"\x000e@H.Í\x001dÙ&G2\x0008*¥\x000bÙ«9¢\x001c­ü'éÓeLêD µçúÆè96eëÝ'­(=¢ì|àØ­HÍ2 NQ¾"Í«l(ÑOJN{â|J
f|\õh¼ªVØ¶¢Ä)=®ÓÂ%.¤øLô`$GLe½*§\x0011%>q×ùÄ¡\x00137ÁY®\x0013»L½Æ»\x0011eé\x0010éº\x000cSÊ¤`Êqd×Æ9Ú\x0011GÙ?I½\x0004½m<í¥Î\\x0019.×\x001eÑ^V;7PÊdgäo\x0007Lk9\x000fö£Èeài¶}Mµ\x0008¼\x0015ej;è´5\x000cÎ£ÝñnrsrAOyäRØ<ë´Ï´´ºñDJ6D\x0010ÅÙ©²Ï´ÂL\x0012¶Ó\x0005·ñ0×á`d\x000bcD	¤ZQmÍiDéR Õuº·Æ²TF°úÙ1\x000fy3Ç¾©#2;µ¤4To©ØÁÈúH%¢CÏüO~¹¾þû"ÓôôâúâÓ6l*\x001aÃ¡^\x0010ù¤­i*\x0014\x0016!»VO^\x001cÕÄ­PåÜR\x0013*­Ùq@TÙqpQATµ0ÕfT9Ô
 äø^ÔªlpTê¦uÕQØ\x000c*'@ÉÄ"PÉD@¨Bð|Ò\x000f£Ê)£\x0016TØ9¤²\x0002Bgî[\x0017HýÂ+Ð5³p3¦#jÂä\x0003\x0011af\x000fvì~\x0004U³\¶â¬P\x001b*álD\x0015¢?¤ã3.ÂÉ¨(\x0011ÔÊËâÉEËÉ\x0015p9\x0010$¯\x001b\x0015\x000búi\x0005¦\x0008L!¬lÉ;Ç)5z±8ÒtÂà¨¥\x000cËP\x000bóÖ)\x0015jzh3,Ê4ÁÂÒ\x001bÚ-Z3\x0013,\x0017Ê!êáC¤tI\x0013,#9Þ\x000bæ\x0005±´ºÀô¨Õ¯<%H`!§iFM^Yå\x0004É
ÚU#,QQJ¤
UDvþ\x000cKæÆ.Ôá\x0005\x0019¾ñ\x0004iå\x000cÖQ$Xð·vKEª<Ö¶Záµ\x0015\x0016§=Ú©"
`\x0005J\x0013Â}/°\µ\x001a}3,Jt´ÁòlôG\x0010÷9¡å0kÀ°ªTfaQj£	\x0016úò±<DzÖØò\x000eÏ\x0019M\x0006
N!5­Yj\x0005oØöóÕVÍ°(}Ñ\x0006Ë\x0008BI\x0013D\x0011¦Õ>¯Í°(\x001bÐö\x0010\x0005Á\x0002ÿÌ\x0014óO\x0019V=±Z\x0005±\x0019\x0016ÅÖÛÄ"\x0019\x000f°\x0001\x001fd9ÄX­ÄÙ\x000c¢éM°Àn§w\x0018$M=q>
¾ñ^^-½n­RK©"\x001e'uÇ^,\x0012Y\x001e!ÖêV¡%\x0015õaÆ¨QÁz(B«>¿b3,Xn\x0015ZZ\x0016L\x000e0\x0004U0
Rt\x0002t£È
\x000bIÓmÏÁz8@í¦Ýv¬>Ö­f©´Ùr;bf8AÊ!XS¥\x0014ß
n´J=NÐõ÷E\x0003Nª+\x0012kÔÐB³V·
Rï,±\x0014\x000bRÏ}l:V\x0013üQy,¬oE%\x000fc\x0001%è\x0004­2\x0005Õð\x001b\x000cØèÚÊsÓbÄN\x0010G\x0017«èBWMo
\x001fÒ\x001dI^ØT6X|ïb¹j\x001dÉVT87Ñ´ºÒNqy]Ìé²\x0004K\x0018>C_­ÊØ\x000c\x000bþ\x0000Ó(³¼\x0006ãP	Õ$OÚJú8°Û4,¯\x0014W^D\x001fr7=Æ\x001d,ëB°OGaÁ\x001f`ZeÒTG¹.¾ð\x000eþâw8|p5Mã3ôpË@.*Á2ÓNÎüaì×¶
R\x000b\x0011f\x0015tàRÕÒ½­0Wà\x001a-,oDQÐ`\x0002R4Ës<ÒÈay©i×jaÓ%\x000b(WA°³jdµ\x0014j3*¸®ÕAá%\x00038]4¡\x0008öJÑf)_­<Ø\x000c\x000bvÛµ\x001a3V¤9Üä¬²ÿ%ûUedÛ
þ\x0000×\x001abÃ|-ò\x0002Þ\x0016ËÏW	K6ÃÂDEë\x001béu¢Ôc}.E\x0015\x000e;:Ø3ã\x001a­\x00194ý¼.æ\x000c\x000b,ãu1go<ü\x0001®ÕA.zÔÖ;7:yãfTñI\x001a4Ûvá}âL¾Nä\x0010\x001b{:Õ\x001e¿­ 0æä#YT\x0013È"C,\x000et\x001bcG\x0015!\x0016\x0013øVÐ:ÃhÀç!Ù JfÎ\x000cï\x0015H+ß(±LU<9_\x0018DÒ!YÉ\x0017ÝvdCþ6²@¬K²f¤StÄKc\x001f(èØ+Ur´'Öç\x0004à
\x0003ÈÇ(ª\x0004¯[á}Ïß6`f\x000c&ó¯d,Lq\x000e\x0007C\x0012é;äoú\x00114ªÑ	\x0015wN«à÷(\x0007\x0003\x000f2\x0015¿æoÓ\x0015syLzÒ\x0008\x000c¸c¶ÄÿlgÚâ:Hû9®i\x000cZÓÁß¡ \x0012N+ºÓ\x001dÓ_=@ Í-é\x001bà\x0015ÆVxÊ³ØÀòTi!`\x0017\x001dW\x0008U§lÇ·b'h\x0005¨C«¥à²5\x0014½ÜÝoê$\x0001üóç¿ÿ%¤ºTu©FòîÏ7WWÙøq¬f*]\x0002ÅKÿ°À\x001bÏ3x\x0005Ýù½<==©û9¾ÿû»O\x001cË\x000fàç÷7w·×\x001fþý¯mØ	\x001a{Gr±\x0006èôô^C¢#P­«úýËó³\x0017Ï7`Ã*'éÓ\x0008\x000e;¹©\x00005J4\x0006ÇmwZt\x0014LÉümÝ:ïùÕbþ%zÚ:Q¢äÕVÊíè|*íóí{\x0007\x0002ïT}H|Û\x0008ÎzjÔÇ1ªµ'±\x001d\HÕ%øm>XKÅ8.Ui\x0007>X6puµé¯\x0001]Ò¬ømÝ:L\x001bl\x00011ÇÇ«\x00121lG\x0017zÅoëÞ9Í3Ëbà¡§ÁÑ8;8Øñ­S)\x0001¾­[\x0007\x0002(m0à28P`]õª%·\x0015\x0005a\x0007ÿ[éÛúbáù\x0019\x0011v1Û\x0000Ák\x001b\x000bÓ	ÎþóÇ\x000f\x001f~À\x001a\x0001ÌMâçôÿûoÖ\x0011\x001eð(2\x0001¼È
^ÈºÇ= Á×Ù\\x000f? !\x0016È0=6d`ÓÔZcD	\x00010ÁÄJQWih\x001e\x0006öùó_þü<¬"\x0011,¸½xwóóÛÀÌ\x0015¬F)Ë^m¹bÇúzÑÿÑñËïnÂ\x0004lÆåÙyO´¦6?\x0001-\x0018­w¯oÆó=Ú !gpög²Zô°\x000bÃ±N
»\x001d[b×Øàª+ªýÀþ6=5X
\x0019èÇ±¥\x0015¦yß´D»-ç-\x001du-ÃÝçè±U\x0003³\x0001[®âo¿nÚ\x000cð\\x0018úµ¯ÖknÆòûIú´)r\x0010æÐô\x00162\x0015\x000f¨òLMÝ½\x0001FlÍ÷ÍGÅo\x0001¤âa%¯|ÝFÁY¦`[¡U+\x000fCNHK$BÌzJG\x001eÄt(ÃàveÚÅ#pA2¸|«\x0004n\x0006'Ó4ôm\x0003Á\x0010
?H$:IØ¸I\x0004\x001c±qd©¢:}Û®¶ÚÔÀÖähyÜM¾oÕy\x001fÁ©¤IU*5§vÈ4»Ëá¾ÑÄDì·êU\x000báÝåçO?¦Ì\x001dH\x000f$Èn/¶2RbG\x001f5ªÆb³\x0008\x0007¡ed"T3§G¿?;:\x0014LõùÛ\x0004
Ë9) dÏ\x001c^\x000eÞ\x0013Ý5a«\x0010éä#à·\x0005Fq\x001fHÂKlêºÌñr\x000f¼ÐvñÔ¶M\x0003cR\x0007W!#sÈì9ý>x\x0010Ù_¾º\x0013)o
kÃÓ\x000blº¼¾ÙØ\x0014\x0005\x000e³ÇBùÜ÷°k<Bj\x0005j|¨?\x0002l:yñ²Þ\x0012µÃñÏÔÜÜ\x000ffò­b)E¨X§nj\x0002\x0018ð®\x0007 ÆUÙ«W¶BÒvvMë,Û\x0001ÊtÂùÛ
Qc£ËÞ\x000cö"¸d,yÁSI¬Rõñ(Â\x000b÷Ù¿®È\x001f.þq{s·ÕÕÂæP\x000c^¦H!0Q»Â;#i\x0015x<{yþ»µ\x0003·»-à0\x0000r¨ro°ò_-éV\x001dBµ6»\x0005[¹{ØöÚ Ñ+X­ÒÁU#è-ààÏ°±\x0003\¤ùh\x0006Y©ÁÖ*:\x0000¸ú$íà¸\x0008¥\x0015\x001cò\x001b)\x0002çw§J\x0015u-¡\x0001\x001aU¢4CÓTy\x0005ÐÏ
 i¯\x0002´:ÃQ\x00038\x001c­:À9j3
¬`Iû¦Ë¶Õ£"
Ø¨X¦\x0019[ ÁU\x0006G/ñ¾Qi\x0018`±mT0Ó

\x0008)æ\x001c[&\x0000mã²fl<b\x0011À¹ì¬\x00028#Ë¾Õã\x000fÛ±QíL36CU=Íó\x001aSö­Î\x001eÑ
hå\x001bBÈØàæ±|¡hjä²\x0001\x001bUÑ4c3<ñF9ê°ElÀ×Á×v\x001bÀQ1MFÍyU\x0000'ò¹¥F}ÈÞÍNð\x001dzÁ:x\x0019\x0005f]Ñ¨Ä­\x000bàêD
à¨à§CÝKÒ\x000c¶LZ\x0000uÏ/ÕWË2ZÀQÝO3¸@Ýb\x0006^\x000c]9eXÝ»\x0019ê\x001e§´ú\x000eÕ\x0000¶$9be.²Fp\x0001p\x000f8`ÛÁQmR³Þ\x0012î	j°Ê³\x0015çê\x0004
ààjø\x000eíà8¯\x000cÏ B;\x0011W\x001dÌÓ
\x001e¼ïÐ\x000e ÚøTMsÕ*C«³y4@C"\x000eå\x0000
D\x001cv3\x00132#XÆ¹\x0019J\x00159U|rÀöe:Sæ\x0016ÂßÉ¸\x0019g
Áw(\x0007Ï-xI9H223µ\x0003æîCvðLmÔªeS©ø[¾NÚ\x0000\x000e4CèÐ\x000eg\x0014\x00008mAd,\x0015p3\x001a4jBvð¶Øæ\x00185$l¶8ªõ\x0008Évh\x0010éÐ
cs\x0000-fR Äæ
¶	Ò\x0017u_èñ\x001b\x001c1$/(sÜ\x0006±\x0015ÕPmÂiÁeJ=~§y\x00139ø@:Õ\x0004¶Fê3©[À9Ìrum\ \x0001\x001ch\x0000AÚ¸->@\½\x0019Gbôi\x0004\x0007ÿ%¾q\x0001g	åpdR]Õ\x0000\x000eÙÛÒ§Ã:Ïå]FzçÅ$#T(W¾\x0019\x001d	Ò§5T\x0008Ú4WP\x0019\x0001»HC^½cOÚù\x0007ÒIÛÑ¡bÕ=LKÍöÆ`¡£@f\x000c\x001cÈ| ¡´\x0019\x001d\x00061}O$3W(Bä\x0005»i#S\x001cú:+ßfhÈÁÆ6oæ¡Î:JsE°·D\x0007 ­{ Ä¿\x001d\x001cÊ`Ñqç0\x0017´>Ê[ìºÈè(M¨Öt\x0014LT\x0018ùûµ\x001d«L\x000cÞùÛü\\x0015å¥Ó4X\x001diëH \x00155¬À¤Ä"üm\x0015Ä¥\x0000\x001d6ZÙà½:\x001eë\x0004`X\x00010àµkX¬Ý\x000f\x000cÏ²-ì0+á=0¨\x0001^ª?7í:\x0016ùÈTkIá\x000cçø	W\x001d\x001aÚ\x0002Ï'x\x001dZ\x0016Û½5Á¹è\x000bà±í\x0004ðì°0\x0006`i\x000c¥éÑ\x0015Ú(¥v\x0005]QmÌhgSÙmwu@Ë³«c0+L)ë¨
¼\x0019è\x0012!m÷ub"èËà\x0002\x0006O\x0012¸À\x000f"NÈ\x0012«6ò·\x0019\x001dWã\x0018+\x00044exåæÕ§?4 Ó	]»¿\x0013£fë\x0013j.¤Ft¦l^}Þ^\x0003¼$mLÜB\x0008ð,J\x0004R¶®ÊÐÕ.dÛ!Á¬Ë³H½G\x000b!¼"óÆcÀ$²íÈÁ³Â°8\x0001¶Ðð¦ªÞatI wØ1\x001bO	T4ä\x001bIT\x0018Ý\x0003u\x0012Ûá%ÜL`\x0001PXÌ
5Ù\x0018ð¬mãx\x0018¥
¿tzôÃ;éÙoál¹yÕ¾û\x0006x\x0005Zv$Ôc6PXæEB§È«Ï\x0005k@ôEGN\x001d$3ONR\x0018|¶¶8f8g\x001c^R\x0018\x001dYõ­\x000f¶([Ïõauí\x000ce
_eG^\x001d+þØJ&w-!:\x001e,eÑ%}ÑZG#²à\x0002\x0015;ÊJV\x0018õ.Í\x0016xIatd×±áKDf
E#eJ¨R\x001d·Kú¢#½\x001edmfB('k\1òÆKM\x0000XR\x0018\x001d\x0019öhéÉâpäü\x0018É[ç§\»¤-:2ìÑZ:zI)\x0015à4SÉ	©\x0000ÐOò·\x0019¦^>'sË\x0017Âã¹\x001b\x000f
ØÎ'eÑeVrÆ\x0013ýnË5ÄÚ\x0017¿{%(\x0006dG\x001d9#{¥8K\x0001]½'­\x0001]R\x0016\x001döh¨Ã5\x0005\x0005(ÏîTP3\x0002>)L{4\x0003ï\x0006.«r´\x00132í2±DåoGèC\x0016ë\x0000|´n<»\x0008¸²èH¶'v\x0012Ò\x0016ÌÝÙ>P§»\x001d^R\x0017\x001dùö¨\x001dW\x0015\x0019¤ ÷BÚ\x0012Q©\x000fFjÔEGÎ\x001dgU°ç\x000c×&:YÂe3â=>)¬{Ô\x0015\x000cF¦28dBàü\x0004KÀ'}ÑvG\x001b/"òèdm9Ù)"/õÍË¼{\x001a}³Ór¤1èú"5ÎËÌ;R;]­bÏ±H\x0019Ê6$}ÑzOÝòÅP\x0011\x0004Î\x001b?ÓP	I_tdß1dÁ2\x0005FXbåÍØ»¤.:òï\x0018îa\x001c\qºàMÉ®axI_t¤àS¬L\x0016û=j\x000e\x0015÷b¼G¦aÙùÛ\x000cÏPâ\x000cCÜÍ\h\x000b¬\x0005[R\x0016¡CYÄbEEÍ)ø\x0010ÊÆ=Ð¬¾\x001d\Ò\x0015¡CW#kwñmÅ×NïÂ\x0015\x0013ìEèP\x0016XQÁá
»x\x0015Åå\x001e/õ2&m\x0011;´\x0005ºÐ\ü¼Îh'\x0002`I[Ä\x000em\x0001Þ¬äÃåq¹z3âx1iØ£-\x0014W\x001ca	\x0003µ*8¯J°g	\x001aº=ê¢ØïÁgÏ°-7o\x0005\x001aº\x001dêÂ]ýå£u®,&\x0018 1)Ø¡,¼#ª\x001c± u¦D,fdVÒ|¾ômÍF\x001edc¬\x000elã\x0005,GÏÙ\x0001Õ_#xýóøûOie/.\x0000ÚÇ7Û°)­#ÏsÇeÔá	¢3r\x000bjU½8\x0002h¯_¿Ü9Í\x001bÁ9«xö"Î\x0010$¦nëeW5ðZÀ\x0011x38sH¬¼¨p%a+´ùUEÑ\x0002
´?þ´\x001e*ÎëËÔCXH.èP-³"©úpù\x0006pÜ<ÙºoA\x0015..i3¡ÃHEa»\x001a>Sò·\x0015\x00164\x0016ÐE\x001e³f*d\U^\x0006x)¼¾Íð"u´9¡
}©å.EWÓ°¢{÷×¿½ûé\x0015­ä«ËÜ^¾¿k`m¤Â\x001c*Ø,çÀÃ\\x0012U
½:ùãÙÉ³ó\x0007H\x001bwðÐËNVxÒ$TQ&AÏ	æ¼4¶jBcpðÓ¼ypy´Á)vi¾ÑUÛ®\x0001ß®±\x0019Ñ¥\x000c,cP[Ùu\x0014ÕI\x001bð}?Iá±<\x0002÷Õ-ü¶NÀ\x0005g©×iKÅî *\x0014iYÔ\x001a\x000f
g~uvôÍÑ\x0003\x0013pw\x0008K£V+Ä<vÆÒàÀkbã÷ÌÊbôC£\x001b\x0010rCT;B­©R\x0000\x0010R8
\x0019)ø3ÕÁ9-\x0010e¿= 
.\x001c\x001c/\x000f5\x0008ì\x0014è¡ÉëÛAî¨¯;@bNÔ´Ä=\x0012
ã»©\x0017þ6\r'vô\x0004ÙMC¥¢ã¡\x0015VVÇ
o\x0001ù÷_Üí'½ìÉ?»{÷Óåfx.F"HÝù\x0006ÈhQYåª³·ÏÎ¿=Ù\x0000mi*´ó"ð¢\x0010$\x000fóto!\x0018õµ[ø\x0018¸?}öÍ²¹æõåíVæ'mø<qÑæ\x001e8¤)#[\µFïõÉYÝÓX¢®í ,v4äò-°©Þ\x0017gl0\x0001«¬\x0007C·?
 0*Kdàar¢\x001bì\x001f\x0006ådíöo\x0005S­C\x0013(l¸§9\x0003\x001egäAî£\x0014VjÙûFP\x0018wÂ;¥Â\x0002$'°¢Ø\x0012¹°ÒÚzEïVP \x001cð§\x0001Æ:@©\x0011#ÍMÙ(V\x0003Õ\x0012÷m \x000cF
Ò§áü\x001a\\x0010U\x0017\x0016Rä\x0010àª:\x0016e\x001bªFtú4ìÁ\x0015Dä$(d<Mí9@[QáûsM\x000fÐ8\x001bÉ ÇáRé¢\x000bU\x0006\x001ejýVH\x0011!Å¦ãÊ\x0011¬Ú\x001df9s¦ð\x001c{}\x0001=ïôiØ§P\x0008A3õPâ¸8§ð
Ý)^Jþ¶*ä\x0011Îá\x0019\x0007ò=OÊA\x0004¢jØ\x0008+¦o\x0002´,\x0017RéfVÌ\x0001lï2\x0001¨jym5Ó·a·4ÈPI*\x0010k6mÞ-íÙQÕ$þVXé\x0010]\x0014Ú\x001f2}\x001aµáâÍßªe#[Q\x0015VÒ\x0016T8ô"Xà\x0017ç±òà°§¤ª\x00126ÂJõ\x0004éÛbÆ` 9Û|hþeBApÑCáa\x001cDÒ¹¢Íâ³©¦ß¡Ì<Ë8÷BRVsj\x001baÅd#ÇFKæ×\x0016\x000fR¦l3E¥rÌ¶ï qje±RéA©0-¿M[\x0015Xë rå\x001bn\x0015\x0000Ðª\x001aß
+ØQm\x00062\x0006x
¸Ñ\x0014eêÿ:
É¨®ºüø~\x0011ì\x0001HW\x001bý.§±\x0005XZqÔIJpc3\x0013I¬\x0007*f\x0000\x0015¸­[páæF\\x0012ÓÙ	Âbí\p\x001c%³ý*gÖ#¨>Ê¾[óí\x001e|ÿaó°\x001a'\x0003\x0007\x0016Á"ÖÜ\x0012\x000bßÿôÎ\x0007ß?hZÍ\x000eÜ¾¨	\x0008S\x0015Ø9C]¾ËP¬¨G\x0015[À\x0015:\x0016pi\x0008¤Ëâ^\x00038â¨p $èPUu\x0014øvpXÄ÷$}Z·N[îê\x00013YQ8h¬z '»\x0015Â\x0018Fú´n\x001d¸4ÙÝ\x0018_úµ(Ë½b38Ü}iÛv\x000e'Ùæ\x0017atÈ¹»Ô Jç\x001aë¡ö\x0016t\x001aÑ5?4ÔÂ\x0012FKî±´+\x0001Ðð\x001fF§QH¦OóÕ<Tä.éü`\x0015\x0015Ý!Qp/:l:NâW>Ùý'ñèËë»ËWï~úp}ù\x001bFy
¼	&×aà¨\x0002
vÕT \x001e}òâüäàÕÉñ·Ï_üñÉkø_\x0000\x0008åoî#VKÄª\x001b1\x001a$9CxL¼XZ/Luo\x0001ë%`Ý¿Å¥Í&$\x0017¼Å\T}åÍxÍ\x0012¯éÇk\x0011\x0014ý
æUã\x0006zþ´\x0019°]\x0002¶Ýá\x001aD"Ô½æ
æ\1ªª\x001f\x0011»%b×¿Å\x0000gZJæ¤`Ñõ±\x0008Íý\x0012±ïFì<Í©É¯N1/æWW-IhF\x001cC?â¥	±.

\x00015ìq¬¸\x0019q\"ý5QñÀ\x0004kRÐ5Ö
Wê\x0010ýx\x001d\x0013·\x0007-²§¿`K5ºN\x0001Ö\x000cy­íúÕ\x001d\x0006\x0019r,\x000fOri­®²D7#^i;Ù¯îÀ º½ v,·XN»\x0015+m'ûÕ5Pã[ÁDw8T¹\x0011¯ôìWxN23\x0001 gI!)êh´wÓîñJãÉ\x0001·¬d.ÁJ\x0013bv$rÓ ¯Tì×yðô\x0002ï²B£3ï2W>ëjýi3âÊý:Ïìì
!Nv\x0010¬¥]eWÈÎýJÏ:î]
Â\x0015iñ?l§A^)=Ù¯õ´åQo
9\x0003XrXVs­ÕJï©~½g-Ím7\x001eé$HUb½Ù0Ë\x0016R+½§ºõ\x001eÖ-\x0016±¨EH^xn\x0015²:f°\x0019òÚÍëW|V³ýæ£æ¶:\x000c]ò.O³êÕJõ©nÕ\x0019Òzb\x000eIÂÒü\x001cªIµfÄ+Õ§úU\x001fØe÷ß\x0007\x0010\x001d$/8¨n´©\x0006È!¯TêV}È\x0010É\x000cÞ\x0011C\x0014¼8î\x0001©sk7#^i>Õ¯ùL¤Üñ¾ô6XÁU«Óü\x0010µR|ª[ñE°;\x000f¬9¶.¢á¾G[í{l¼R|j@ñ)¦#v^>E&+S-ti¼R|ª[ñápw
½a\x000cR¶43©j
Z+b½R|zÀáS<Èa8û"Ôkbæ>éâÓý\x000f®2Mz2R\x0017¶ûhù*Ëi÷B¯\x0014\x001e\x0008p*¾\x0017N\x0012|[hyÔ´\x0000§^\x00078\x0007ô^qùt`Fk&¡Õ1L\x0013pz¥öô@ÓcÕYÚb!Ùæ´\jd5\x0011Ùx¥õt¿Ö\x0013ÚF°pÚø-\x0017\x0017êèªÉïfÄ+%¢\x0007\x0008·òð\x001c?<§ËÃu+Ìêáî¥ÀÄÉª\x0003µ\x001e$nÈ\x0017¹:¸\x0019ò:Tß}£*ÍÎÚ\x001aÖ!È±Ì÷BÌºÉa¥öÂÚûMîô?¼ýðñ^,\x0000ÿÉW\x000f<~\x0001<\x000e\x0000\x0007ùË\x00193\x0017-\x0016Ñd\x000fÙÀÔ¼ ÷êþº·<{éÔ 0z\x0006h¼<x}qw{ñ©Á\x0008Íù|\x0011\x0012mÚçH}Â&q\x0011Õº\x001dN\x000e¾99x}t~vôæq°j	Võ5\x0018ÒJháV°çÇ¶S¶¦Q\x001aÁê%XÝ\x000bV¢¹·6°M\x0004[«yk«!F´vÖö¢\x0015ÑÑÖ\x001a\x000e\x001b¦\x001b­×e6bõK¬¾\x001f«25r\x0012ÇÄr
fmlX
½`-wâc+c,4Ùm®Þ\x001dØ6.ÑÆN´à÷ç*\x0010)4Òjä%ÿÎéIÒ@®EW¯ì2\x0008\x0018`ký¡fáUä©¶¯4Â]É\x0003Ù+\x0010$®
+1÷H\x001b,ï®­'5Â]	\x0004Ù+\x0011t$7\x0014à2­¹a\x0002³Ä\x00156\x0003ì"ÂAtULÜdeá11\x0000Ó×ô\x001aÑ®nê½	hÝä\x0002Dikd×,on}G#ÜÕMP½7\x00016:/$<JÚ]Ã\x00177VYÚ\x001bá®´êU\x000f*¥p\x0013\p-Ý\\x001bXâÆj\x000e¬\x0011îJâª^+\x0015&7òÕ54Hüctw«ôJmpõJèê^¡+ü\x000en8tàrZÆ*CJ\x0013\\x0013Í\x0012.þÚ)u=1÷Z©æ\x001d-YGTIzàZ³¶ÂL·\x001dÆö­c²×\x00116ãÞJ,Y_êTÂÞUÈ[«A·¹Ür\x0011y$=«ÔÂÁmc\\x0003ÝO-Ò\x0000lÕó4Ç\x0019$CyjÕ8e«øáâ¢¸èeö\x001e\x001bwÊ£äåZ\x001a\x0017&ºrí\x0004g£\x000cÿI¯]fU1yÙ<§Nu´xç\x00084eïí²íÞåLsÆ(o3\x0017»:#«eöÅ6ÛþmÖ½a	0)§o|ñÝ\x001f¢QØZ8»\x000e4\x0008\x001c\x001fS¢h¿¿½¸þ÷ÿsóáãÁéÅû»ËÛÍ
HÑ:ª«±
Ô`Rk®«ñªJ-LAß\x001d½8~ùüõÁéÑ³ó³³Ç\x0017¡P\x0013\x0016\x0001\x0012Ú9Ây\x00079uî\x001fÈw,B/\x0017¡',\x0002®{.ôF\x00062BS/\x0018Äc¥Þ\x001d°ËEØ\x0019\x0008}Lª9ÐâUµO²
~¹\x0006?a
ÞQu\x001c¬Á\x0014wÃÉ`/\x001f+ÄèXDX."\x000c/\x0002¦k$Ù`¿ÆkîsáWx×q¹8á$ÀäÛ\x0014\x0012Çxnq\x0012|duÄH÷"våÍIÂ	G\x0015\x0005$aåà\x001d'ANM?
¹Ö\x00133\x0014E\x0014¥Mn=Ïf`"#t6¦ËX¹±r\È:xhÜ1-½.«ÀQØäV)ÌúW±\x0012²r\Ê:!
+mÉlrw+Q*Mÿ*VbVËY'Tª×d\x0011EuB³è ¡æ/b%¡ä¸Jó}©UZÅC^¹ò¸\x001f+ji_Z=n5þ¸ÑT¥	\x000e ¢¸*\x000eÌ'¾OÞLPjõ¶Õ·mw*Ï²ÞðlJç«sÛ{W
ÀËUø)7Ê,*]L	\x0000\x000eçt§[­"¸\x0019`¤±\x0016 .\x001c'\x0004)î}µÃ¶ºÒÓZõv>hö.Æ\x0001ÜY ì\x001e1Ó
¬£:³s@ÒÞ[\x001f_\x0008Ü*µS$-WÉ»:/ûÀZ¯\x0002oÕó\x0000[u\x0006\+®e¸%ßWG1\x001cÇÛ{ÇñvÂqØ\x0012\x0018Ç\x001aY"eP<xÐÕç
Ø!Ë\x0007Ù"ê\x0001s$bÄ1+rË-¿^¨]Rbâb´»\x0017\x0008AÙòäÉñO?¸>øñîàøæîöb3c±p4\x001d(e(hÈ|â\x0012¡\x000bUÓ|Çß|÷üÅÁ7ç\x0007Ç/ÏÏN\x001f¬u7d,
0ü¹\x0013ÊòjW
ú·#¶KÄv\x0000qØe­\x0014\x0017\x001dj\x0017ª6R;d¿ì\x0007î¡¹\x00009òTÕ2¥ÄÕ\x0019ÎÚ!%äÐ¿ËÞ\x0010=³Åj>[xvÐ`Móv9.!Ç]Åñ]ã Uq*«1/\x001c{\x0018¢æj"­ËÐXïyB{0jÌk1×/çD(Yy	zÃ =IWSí Õ
´úO¸Ñr%êä¬Ã¹9Ú£A¡\x0014ÌÌË\x0013êcµÚA¯\x001cv¿\x0016Tn\x0019í\x0006}\x0003¾D¤ÈQbúoãå,Ð\x0012	}W²#öK\x000f	ÆR$\x0012³@ª0(öî¬ò]u\x0008é½\x00045þ¯þÜKä\x001b.ÀU 1"J\x0018Ù\x00074	{.ý}^%x?|Â\âëO\x0007g7ï~ÚèæX\x000cQÃmlF
>ê0©\x0007d¿Álâó\x0017o\x000eÎ^\x001eû8bµD¬º\x0011KGZÆ)ÅÅÖà\x001dÓkD
µYõ\x0012±îF,,±T\x001ag<RÀcK¬Î8hFlM/bã\x0003w 7*\x0005¯\x0010×\x0007­6#¶KÄ¶\x001b1æ4s§×ªÄæ\x0007\x0012°\x0016o\x0006ì]/`í\x0004Ïìà¢ÇL\x0013\x001a\x0005\x000fØ1¾Ú)ÕØ/\x0011ûnÄ¶
\x0012ì\x0002!æ\x001c\x0019ÚÐ³\x0010%âÐÃ\x0005Xû³\x0017i\x0019±«¼mE,WÂMöK7\x0011xr\x000f+íD©\x0017ÖõòæfÈ«,»o²É,Ê×äJwØâÀU4ZWç¼7ã]]cÙ}A\x0018p\x000b¶Ç9y*\x0003\\x000b&lÐÕ6£fÈq\x00059v_d\x000cÄ\x0010¹\x0012òÇg¾qdo`æ¸ºIÔ\x0008yQí3ùH'de&*Qh¹ÛÖ\x0018l \x0004ye
©n[H\x001bÇíÁ ÕòèI\f\x0001\x001b3K¾©µ)Ô--PÀQ[e\x0008èñá&3Å¤®üiF¼2T·-dàx<qâ7dkX$×ûx!¯l!Õo\x000c!q$\x0017í\x0011YÄÂ=2ï^¬!Õo
).\x0002È>Ç\x0014\x00112{PÚV³\x0017ÍWZDõk\x0011m(m\x0018¡\x0014Kå¢ølµ¿\x0019òJ¨~Eâ8<·ä\x0015\x0014zG!W\x001dóÛ\x000cye\x0010©n\x0008gÇ0gªHÅB	2\x000e7z¬¨\x0019òJ÷©nÝgÃ bV×7æd»ÖÕ\x0004o+d½Ò}º[÷Á£CªçLÈ&9¤PÌn6Í©Ö+Ý§»u\x001fNHgúFa8×#ÊÈjx~³\x0010¯tî·µb\x0003ÃÛÒc)%÷SézÈ¶\x0015ñ:\x000cÐ¯û@\x0014;â
Ón	Ï\x000côZÌ»\x0015+Õ§»UEn>z{Ja¯0y#¤GT}VX3äêÓÝªÏJÍ&Ãa
¶DË¡\x000b9ÍîÔ+Õ§»U\x001fÞd)îã\x0014=Üd\x000f0ËÓ+Õ§»U\x001fóQ,Àù@WYù»ÊØY^^i>Ý­ù,ÒïÓ½\x0008ö°H\x000bgl«¼ÐÍWOw+>\x000cÍr \x0013t`0\x0004YóµÐÕù­­ÍJñnÅgm\x001bºL& [v­ª66C^)>Ó\x001f\x0000wYï\x001d\x0016Á\x0005Ìuº\x0018\x0018\x0005y¥ùL¿æ\x000bIuUÔÝ(\x0003\x0013+Um$nF¼Ò|¦?\x0002\x001e\x000b­§\x0003ÉAf§äQ\x0008²^\x000bÝx\x001d\x0000ï×|FfN\x0004c1öB"Y³\x0005\x0007rcâ3+-b\x0006´+>t{ªLl&,V:Äôë41k=[2OJ\x0016­7ïR¬té÷"\x000fg[7î*f\x0016O6+%b\x0006"Y#Ø\x0016â³Ì¿m\~¢\x0015±]é\x0010Û\x001f8teE\x0014äï¥å(\ð§
²ë§~ï½\x0019RR[fâ§õ\x0014#rÝLÄIu?ÓÐkÐQÓ\x0003Ä9\x001fÏ1L÷jä¤\x0007\x0008\x0018õ=ÌÝ\x00041ó|\x000f\x0017ó\x0013L 9\x0012.'\x0019E\x0000ÒÜ\x0003Ý­L\x0010´§\x0011\x001f`Éq\x001eÊ §¬×qµ¶÷@w;RévPDÀ\x0019Þf\x001bõjô6Äê^Z'ýÞ-#1¬ «
µ \x000bo9êR-=¿\x000f¹Zÿ_RÀ\x001eô\x0004¾è\x0016vºÌ\2!7¡£°Ûù#Õ}AÞêTëÒéh["\x000fKlÑ\x001c\x001b\Õ õ\x0004\x001f0ÞëEGâÞ]\x0017Ò÷\x001fÞ}º¹=xõáê§­£\x001dmÌ¶Q*2%\x0002j=Ãöö±¹\x001fß??~óòìàÕóÓoO^?]-±«1ìÂómö)
zp\x001c
«þHù{#v½Ä®\x0007÷ÝÒ\x0010\x001eÀnË`&$=ÊØÝc=SØÍ\x0012»\x0019ÜwCF\x0014`ßÑñ
ïªJ§\x000f»]b·û®¹VYÉôlxWÛÛÜ-»Á]W\x0014L\x0000ä%,f-W?{_e#ëÃîØýà®\x0017Ú7e=Ó¾YÇ,9}î	KìapßENâpÍ¼ïEBúÇè\x001b±Ç%ö8=
&\x0000KR\x0013í\x001fk\x001do¾P\x0016W-ü=Ø\x0003¸j4ú[9_¸³-3\x001búðØ4Fðk­:¨VáÒ\x0010-£
º\x[Ú0\x001fkNnÄ¾ÒªrL­\x0006B¡{[î»á\x0008 lJN#ôRcZ5 ³i©ÙÂq¦\x0011ÌJÏÍ\x0016U¢Ñ>ð+­*ÇÔj;ðÎð(Apð;³ÒªrL­þæ\x001b¿R¬rL³b­Päùæ®¾Ó¡\x000c8l\#øfcª5ð¶MÀoµLöÀÞü©ÈWzU)Ö\x001avÀçÙ/e`mnª	,WUiV\x000c\x0011)\x0002ït\x0019g,¹¤(87õÂ«jUª5pu¸Õ`\x0011GÕ»fÇë\x001bÁ¯T«\x001aS­\x0018ç¢VíE\x00115¥E#x=Õ\x000eVkuP·b¹ª¡\x0016FÉS°\x0014\x0013\x0006ýØÜ®Fì+åª\x0006«SLÏ¥\x0017\x0003±¹37jis\x001fönUº\x0015é\x000b¥SMELã7\x0015úJµªAÕ#²²¤12ró<Â9N\x0016j¥Ô vÒÌ¥n¬]<Ó[Å0ßTì+ý¤\x0006õ³¨]m(\x000e\x0014Ü½æäÜ[³ÒOjP?)\x0010h­P<1\x0019ëPòÆ?Ê\x000cÑ]¯Ô\x001eTO¿ñÆëzÒê	äf)	Ö$[ñÆP\x001e×
Y­\x0011ë\x0003¿ROzP=\x0011I·F#\x000fwÁ&Y{kÖ\x0001Õ1õäc,7\x001e4\x0015IE\x0004í\x0016`*özÒêÉXæa¤)ìòÃ\x0005QN¾ñ+\x0005¥Ç\x0014\x0014v\x0001\x0010Ã
Ma#\x0004\x0016\x000c¹ØW®\x001etý0ç/Q;ri&gê±ùºØWºUéVïY·b¥ÌF¼æÙ:È>\x0017ûJ·êAÝ\kÙ 3HÊûÎ\x0005Eq²!¬WºUéVï%sH9åf"KdûjÒf5U¥ÂÉ´í®Ì3)hçÚÁf¥XÍbõA2Ùs¦\x000c\x001c§¶#+õÜ YéU3¦WQ7Ñ± q(wcì\x001b,´¹\x00193³ïfP¾ã\x0010¯,ß],üØ)\x0005Ctî­Y	x3&à}X`­\x0002ã³r"CØÖ\x0007ôa_	x3(àMñåUiõÑ<\x0015\x0005\x0011ç7c\x0012Þ{\x0018È*%õ¤#©VÌ<SÁ¯$¼\x0019ð\x001a\x0014j®,ðVc¸)×4ÄÞªÉBÞ®¼\x001d\x0013òI=eðNúÜ·\x001aeM|lúb#ö·B^	yÌ\x001b"qÒ
­¬F°+!o\x0007<È\x0017Eû\x000eæ
åüÀáçZ
Ô\x0007~å=ÙAï	ãÀ\x0019|\x0010
2-©\Úªjal\x001fö÷dÇ¼'\x000f^+Åâ
Å\x0012öÅ4Pqj
]×£iW\x0017\x0002ßx,¤\x0002,\x0015h8Õ²:¶­\x000füJ»ÚAíjËsu+fÓ@ë'£·+õjÇÔ«\x000bM\x0010\x0004¹+fæ³ZU[¬ûÀ¯Ô«\x001dT¯
 ÒÎcÎvçNQVízé\x0003¿R¯vL½:ãNw\x001eÐÎ;VQºÞ/×\x0005Þ­Ô«\x001bT¯" \x0007[RQØy7[Æí\x0003½~}ØW*Ê©(ÓÛiã\x000e/KyÅ!\x0003å«Ô
}ØW\x001aÊi(l1É\x000cQi¾´Ê\x0011me#ÝxíææýÜJE¹1\x0015å¢`üD%IyËê5TGðõ_©(7¨¢À°¡ \x0019ü÷¹JqæÏê ¦\x001a\x0007n]59¦¢\(eðvIÄS
<Ö\x001dLÕOn¥Ü ~¢ÉZ\x0011s Y¾+#É¦ÑÎKiCîW"ÒHç5\x000fEÄ"\x000fò@ã°ûRýÊ\x0003ñc\x001e\x0003ôRc¦JØ\x0007btÖ­\x000füJ¾ûAù®B¹ìÑ\x0014Fì\x0014ëÜI¿\x0012ð~PÀkOó7°o¢('l»Ê;?9ãW\x0002Þ\x000f
xk8:\x0019µ.&
ë&_åPë¾\x0012ï~P¼ëT\x0002ö]9îRWXâ­±Õ\x0011¦}àWâÝ\x000fwã9W\x001c­ät«ÒR±såäº*~LÂÛÂåã\x0014¬ûÀKXøiè}àW\x001e\x001fó@PPR
':M\x0015YP\x001a\x0016b®1éW\x001e\x001fô@J·\x0016«,\x001c#!2øh§^°R¯aP½*OôØÏWl\x0003Así@PÊ©\x000f6¬ôk\x0018Ô¯"fä¡ÔË èÂ[9÷µr
Ê\x0015½\x000e\x0012
\x0003ì}§]wbªã\x0017Vº5\x000cêVä\x0019LØq¾\x0006Õ\x0017HîÔGn©ª5¬Tk\x0018T­"y{iã±/
&qîÃTð+å\x001aÆ+h%\x001a·í¤Ò\[%{yãëÝû}ØWº5éVëä÷¥×ª\x0008:Q\x0010âc}Ý´5¦,UùÆsFZNûY]eìîÂ\x001eWò=Éw\x000bú!\x0001×\x0006\x0013r\x001e¦}gs¯{\x001c\x0013î\x0016\x001c¿üRáybOE¦!ÆX¸PsÖ¸\x0012ïqL¼[ï)6æpx ð£\x001c v§Úðq%ßã|·^Pa\x0007ü%Ê­¡nblÍªâJDÆA\x0011	Vp$+XH\x001a]-9\x0000ÚT)\x0013W\x00122\x000eJH/Ù\x0012Ös[jÍÕÏMÞÄ÷\x0011G½\x000f\x0015ißuâ²'ïÌHgævúÅ|ò\x001dgk³¨þËà9ç5\x001eSÁ¯»r\x0007½l!x3:I;¹@qø¹m¹R¬\x0013þ:´ó¥\x001cÈ)eÓÊãh¬ÓSVyíB\x000cj("@[x6\x000chx\x0011(°ÇfÌ7¢_wæA\x001deõ¡ædæ\x0005YB5ÎN5Éä¿\x0000\x001d{³À
Ü \x0015GÉ\úfå\x0005\x0000\x001dCï)×íTÅWlÜ¸¨gÊzy¯~°\x001e-3¯½T\x001c[&\x001eJb ï5¤\x000fv¤cUG®¹ª,ÇV5{ÞrjtUÞk.\x001eì.FÓ,\x00133;í
OÇå¥÷S[qä½\x001eÝÁ&]¹	<Î	!\x001elé¹%¨*§{\x0017øuç\x001cló¢\x000cªóQar!çê5g]M[k\x0008+¡7n]è\x0006­\x0004-ir$\x0008T.Ã|}l\x0013ö\x000f£÷
ùÒïcPf¿!;²¡ríâÇ
93\&ïE\x000fÒïc	ûÈºAX¤«Ë\x0012Þq=Ücs¢®ðaÅGÃó\x0019Ñ}\x0011zÉ\x001cSû²°J\x0015±9Ua\x0001¸ ËáÖ±0·Äç\x0014~qÇë9îgÕäÆ×ûG üè\x0011\x0004xÃú\@øS&\x001c	¬©ãÂU\x0007	tVAß_Ãk\x0010å\x001aáÄ	?¼Ê,E§f\x001bâ\x0017/!\x000e¿\x0004l\x0008dgQÜ³:±¾bê5Ò_\#=|\x0004¿1½øb
ÃKJqÍBæ\x0003jÁ\x000fé&G\x001bì\x0017/Á\x000e¿\x0004l\x000bÈ\x0011\x0013\x001bE(õ#&Ú¹a¶/Ö\x0010×`qe6*¢)OÍEê ÷¦üâ5Èÿ´×`õ\x000f.oWWI?Á2d_\x0018jÞ\x0004%ÀÖ*R'Õbn¾\x0017÷àÅð\x0012¼ä%`ÈxÙ5HÝ2S{5¾xÐjøAÛXª¨=tÔaå
×¯Ë¹
ïîcpÃÇàÁ×¦´ÌDîÜX´ÌÌmÚÿÂLÒãf\x0012zÄõG\x0019­B^æÉ}Øö5Øá»\x0004\x001e¦ÙµÁÓ¨R#¹Äwr\x001b|«´²¶á"VßåTØ\x0018ÁÅw\\x0010£æÖ\x0018ñ¡*oô4ÉÔPXF
÷KèýÜÀ\x0017/!\x000e¿ß¼$ì\x000b©ê¥*\x0018Ù¥^\x001cÇ¾SÐ(:ÍfÒÌ«d\\û\x0018w\x0019s<qZ»p¹»Ø\x0005zç>\x0005øÛ{GàÆeæ:`b§Y\x0014Þ[LjO
Þ_\x0001\x0006M×À
Ä\x000e|¢£Ï~rjè\x0011M¤û/aX"9\x0000Nd@é%puªå%Ìm?÷í\x000b\x001b£öÜ\x001bóÚäô¤TuGgmÁ\x0017RuX7ÿ¶%\x0006Æ}q
nø\x0014@¡±uá\x0015Æcòæ|7ÇsÛD¿8\x0005;n!IW ¼=dê\x0014\x001eQ3²gºÏRÙµbÀtÂbðÂ2c)JX^@)¼Uv®×f¾«f\¬þÆ\x0017I|a`{m¿©vCKûí=Kûí¥
ð/îÁ\x001f³¤¤X*¨\x001bvûÁOæâs?·[Ä~\x0011´Ã±Ho
\x0015¦6XQ\x0018mlé»\x0006ûE\x0000É\x0007$¥×UPÓN(²tn}kø"(\x001fÆò!P\x0018\x000f®<kt¹àRÏ=\x0005ýE(R"CN¡LìäJnD\x0017î»¹#
¾¥ò?H¤\x000e\x0016If±]ôêâîêàû\x000fWW\x0017×\x000eoî>ÝÝ~Hofkª0§¨L4\x0019@À2å!yá±
WGç§\x0007ß\x001f=?==zñæàøåùsøÏÏ\x001e_^®GOZ\x000fH CKÓDñ}¤`\x0006Tc,õØåzì¬ó\x0011èÁ\x001e`\x0017B\x0016ZQ«\x001fk?é^[.ÇÍ:\x001e-ÛJÇ%=8\x000eù¤\x001f1d»×\x0013ë	\x0013×C2\x0000{\x000eÆE
ÄÆÙÇÊÇ»×\x0013ë³ÖS\x0018\x0000VÌo/M¤õØÇ\x0018³{#×Òmxíç\x000c¼ÐIì¤ve=%íº\x0017´\x0012or|sÇã\x0008+Ó\\x001ar\x001aä ú\x0016´orÿ£Þu$¶ã|ÔÔ»n0`ò+-È¯\x0016äg-\x0008ÔhC[pÔWrÑqRæw/h%\x0012ä4¼\x000e4]Gz6\x0011¤,#ÈT|$Ø» åè\x000e±\x001cÝ1*´ý¡ Ù^Â\x0017!'y´úµZ	95OÈ\x0015¥ªpÔ\x001d\x000fÀ&àåctÆÝë1«õiçcF/¯Ç\x001c*2\x00128Ð\x0002\x000búµ\x001eµzAjÚ\x000bÒÓkZ©1Rh®º¨Ní\x001d[ñ+%dü4-$\x0003\x0013ÛêàÙ,Å\x001eÚ¼ ðX$¬sAÎ¯¬8ççÙq±,HèÒ`!©bØ\x0004ñX\x0002´{Eq½¢yw.r¤F\x0011ÄM\x0017lh{÷k\x001dQX	9\x0017fI9\x0003\x001dr\x0016<oI¤\x001d³=Z%P[Ð\x0003\x0005ÆyAë\x0013
ÓNÈ{\x001aÇdbÀ\x0015P/\x001b\x0005¢ov\x001eQð+ß.øYÞ1»!\x0018ÊäÒo8¢ÈÂ£lg½\x000b+C!ÄY\x0002öpx\x001e\x0012ï¸9¸$´Íãý3+bµ¢(¦Ù>'È#µ\x0012s\x0001
\x001fy¬:¿ßÃ[à·\x0008ÁûET\x0007%^\x001ea?ÏÿZ^ÐË$\x0001\x0006².fYu`æ\x0005a\x001eÙ\x000cDñ\%+\x0015$ö2kEøÛIk\x0002Ýªi"*Õj ¹Ë´\x0016÷ë-êâþ¢f\x001d\x0014\x0006æh\x0012\x0016Ô,"\\x0019\x0018õh£W¿\x0018_¯	\x0005ù¬5ÁãAR`3\x001f\x0005[àA<V\x0019Ù\x001feøBJØR\x0002<%\x000e\x0007ÅPjÄ4Gzû·[L|)ý&.+\x0018\x0012ê&bJdç(¤\x0015õ»µ/ËßOJø8Å¼¾øpýéòà\x000fw\x001f>}ºelÍ\x0008Áá\x0010\x0011 ¼×2Ù&ò`P'j8\x0015¼>zþâÍÉÁ\x001fÎ¿ys\x0002ÿøqèj	]A7Ô\x001a`\x0005\x000eÖäA<èÜUY}Èõ\x0012¹\x001eDî¸ÍJ8]ê£f#4V%r\x001fv³Än\x0006±\x001bvÚ\x0004Îäá\x000bCµÏ=ÌÝw»Än±kÞwAÀy\x0013\x0012aN\x0005îÀÝ\x0018p\x001d¹\x0014	³ë\x001bÆ^Ë\x0010ôA÷Kè~pÏ\x0005Ï¿\x0015XÇ@ÈK. L¾.a	=\x000cîºà¦Z¬\x001d!ú
C\x0015\x0000½Ú·Ó\x0007=.¡ÇAè¡è\+¹\x0013[\x0018{Íê¾ @$Æ°KÈN-»nCÙö©È×ºtPbû,ÝuSJ±gÏÕú8wÛWÚT\x000eªSì_&ÁC¿h.¢ãh­\x0002÷_)T9¨QctçÆ2 /¯R¹õ_i%9¨°]ó¿Ñ\x0018\x000c\x0018îH|9\x0013üJ3É1Õ\x0004Wz\x0017\x0003\x0010ef²&.7\x0000oæ^nÊIÚØÕ»;o-ï¼«¶¯ô_i'9¦pV\x001c_\x001b#yøQÎü:\x000fV­¼\x001a\x0013ò>XÎÎà%§ÐÈRóP·Ö§\×® gWpÈu²\x001cW\x0011Þ07<°\x00032éò`QòÊíC7
4Õ«Û/¯/~¼<¿®þ÷¿ÿámÂï4X"½\cp\x0002\x0002Â\x000cÐ\x0008_5o^½üîäÅÑ7'\x0007ð×é\x0001ýÓGñ«%~5\x001f§9\x0011~efó\x0002$Ø\x0008W\x001dRÙ_/ñëqüÚÐ\x0018c`)"düÌÂoU5Õ¹\x0000³\\x0019_\x000cÒ7F3Û\x00122ëÑ\x0003]sc;\x0017`\x000b°ã\x000b\x0010&V\x001a¤Òù\x0004àâP\^h]\x0013B\x000bpË\x0005¸á\x0005¨È\x0003ÍÁnR\x0017P*ÇD5ÇÝß/ñûqü wÍø¢J1uá_TY6:\x0017\x0010\x000b\x0008ã\x000bÀ\x001aäüuÔÃ+¤¹7:Ö#9\x000bË\x0005Äñ\x0005\x0018O³oÆ	Ù\x0002Ñ[Z@¨\x0016Nõ-`ç*&-&ÆW =Q3·²%\x0011\x0003ÅauôÕàHç
Özx\\x0011+IåÆ\x0006ËsE¶#°}\x0016`c-\x0006Û¹"ãXFÆi´²2gc"Gøu¬\x0017Lw®`¥å¸..Ð\x0004]£àþ(\x0014_"Y¥1ï\ÁJ\x0017Ëqe,µ¥@>x\x0000e²\x000cè¸¬õdA*WªXëb¬{Y\x0010)ìÎ±\x0013ìè ü®\x001a(ì\ÁJ\x0015Èq]É­@+@ÒRZ¤,¿\x000eº\x001aºê[Yic3¬mÔbûFD¯Ã´\x0000_\x001fLÛµ\x0000iÖÔL\x0010¥YoÖË!\x001a>\x0003pÕ¦4kYj&\x0008Ó\x0010©k\x0017©â\x001e­È\x0004¬ L«n}ç\x0012ÖOÙLxËÞ%Àã##×Áé¨æ:\x0006Xq²ZÂ¸e-\x000b±	x\x0006Ó\Q\x00086ìä4ïØÈ{Þ1¼\x0003
åþxwðìßÿºþ÷¿n/®p\x001dÏ.î®®6Ë#Ïõ¢ÆYÍEþ>pÝÒÕÎ]O|s~ðìäÅÉÙÑ)®ãÙÑùééUèå*ôUXsaÑ<NÇ[â\x00107JÉ\x0012\x0002}«0ËU\x0019«på\x0012ÒÒD#ï¸\x0002L©\x0007óì}«°ËUØ\x0019«\x0000/*órLë5
\x00136ª^\x000eÚ¿
·\±
0/ró\x000b¬Âp®ÀXVQm\x001fë__®ÂÏXbb\x0004\x001cdä¸y\x000e\x001e%ú¢Ù\x0008ËE)\x0017Ûv\x000cöé+ºOJò"ª<jýËEÄ\x0019ÄUoÒØ2Z\x0004NJÍ\x0008UîE,h\x001cì&¦¬ó8XMÀó\x0011=2#åexÿP4»o\x0019rµ\x000c9¾\x000c\x001bc#\x001cTÇ¡#\x001bÖsMª\x000cÕþe¬T·¢»á&Å¬/l(Þ\ðÆÍ^ÆJwË	ÊÛF\x001c8DÊ©r\x001a©O¥©é_ÆJyË	ÚÛÆ¨¨­\x0003kó\x001a\x0002ç\x0019¤õÓ\©n9Aw½\x0015w\x0000o \x001f,Âé[ÂJoË	;±Âçz\x001cÌÐr¶Ö\x0011O\x001f\¦\x0007ëqúV±ÒÛrâ\x0006áêqRZ)¥9Nqï­TÕîèþe¬4· ºÓ\x0010Ý@oÂÂQg¹ZYÖi\x0013û±ÒÝrò¶Qsk·±hÒfµçDàKUíÌè^Z)o5AyÃãfF\x0004}4¡ËéòÀÕµ}ËX;¬\x0013´\x001e\x001c§¢~8\x000cÍ-à[>j>«\x0019+u¡¦¨\x000bå¨ÌÔX©x¬=Zì´\x000cQmÉê_ÆJÜª)âVÆòÂûÿ¨{»äºr#ßw*{\x0002Ä7¢vI,\x0015}©¢ÄãóâØ%±]KK>,Ñqú<õ4z\x00047<\x000eÏ¤Grkeb\x0003»\x001ak/\x0000«\x0014RDG·É.Û?XDæ?ÙPEûÅÏ»¡ª=\x0010Jåe\x001a\x0014NqÆ`|+h\x0002\x001fVú\x0013\¦\x0004Ëõ&m\x00018­ÓT§ÿêð´>£\x001c?\x0002°©sP.\x0019'«ªÙL~µ¿]J<1¥Ì)e\x000f¥çjvÖL¥<\x000eL¢´K\x000em%¥Ê)U\x0007¥²4%î¥âa\x0008Nr·\,ÖY	©sHÝ\x0003©¸«)\x001at	¶Ro@irJÓC\x0019(e÷\xæ¤O{¹[IisJÛGÉåqñ\x000fNR¥¿øÒMp%¥Ë)]\x0007¥\x0016©\x000eÎÓT¬Q`añ²º\x0012Ñç¾\x0007\x0011È\x000fDÄpÌú¥CYÏæ7P2ôPJ\x001aº'á\x001f§\x0000L]~y=dVæ\x000eÇ2÷6Jêò½B4c*Hñ
0K¿ÓãxðÛá&\x001f~\x0008NH­Uãf\x0008
¿\x0003=\x0007ÛyÈ\x000e9ÇI\x0012§8×ca±nz%fáx ÇóÄO7Ó\x0004£_y¼J-%\x0008Wb\x0016®\x0007z|6©Þ)ÎÕL\x0003fé^-!hÀ,|\x000fô8\x001fÍsúª÷fÊÔu\x0019ªsú\x001a(\x000bß\x0003=Î'^òY`Ë¦Ajç\x0016iìU\x001eÇ,\x000fty$ÊsÔqì4¤\x0012ò-¾ Â\x0001A\x0007
É\x0003\x0019Â"
©_rñBµ\x000eS\x0016Æ]ö\x0018÷¬V{\x001eèâ¼Üs5îÍe\x0019­÷XM#±ºÛ\x00064ÿÍÓ\x0017äªSFWcêò;×]\x001fºéæÃot¾å·ëµ1GÑ\x00130Å\x001d|×lÛQÃ#Ð¿\x0007úØ5?\x001a¿ÅW\x0004(óìØñ7_\x0017­ð¦¼ú¢h\x0001E ×÷§ß~;|XjÓuHÚôÆ©S\x001cb\x0016o×ûgûÛ·o÷ÏWðÊWvózî/\x0006ìé¢R\x0005p\x0017\x001fù[pU«zq±5×Óö¦î''CÒQÝ
Wç¸º\x0017\x0017\êÇê4ò\x0002B¦dÈVÁä¸¦\x00177ÞåIÕ\x0015@¥èT¦Ó \x0017ß[xmÎk{yEºÕÃ<z~r\x0004¾Õ+³ä\x0017Zx]Îëºy-_¥ Õ\x000eXïâgUsº\x0015×ç¸¾\x001b7ø\x0003x[L-úÜ\x0016ØÃnXÀ\x000bÀ¼·ö­çç\x0004\x001bmp³B\x0006ô\x0013b\x0006#â·F
×\x00118}kÕFVàÒ±uz6\x0013¢\x0001#Ñ6ô\x0014B³.]¶ôèy\x0000uâQV1âþôt¸ßí\x001fÿvøøa÷öß\x001fþq7©ð­}\x00110|\x0005\x001bp*Èô"à\x000càz½ÎO·û«ÝþæåþÕóÝÛ?_ÿ|ùöÝÍ
zÓËQzÉ«^³»:Ãgz_\x0015Eè¤W9½\x001a¥\x000féÄXÁó\x001aMÒ³Uq¨NxÃëAxI#ê\x000c\x0018M}v\x0002ep½Þ¢Ó	orx3
\x001f81\x0002\x001aØ1â¯~Ò\x000fÝôÜd\x0012cÓÉ9-À\x0004¾ñ¶lÍeàsïªùÛÞÝ/®*Ó_\x00001vü}:A\x0001ï/túù\x0004ÕµXº×ß
§5à/¾5àPw\x000c³Tß9\Ý}üüxhx7\x0005ÔÖ
áá:\x000f\x0007ôp¦¼K®õÙå«w7ûÅ_
\x0005lèJ1%êlò\x001bç\x000e°u[Ë
Ù\x0005\x0001ÿ;é\x0005éç\x0017\x000b­´á{8BâVE¥õ°¶µ°§Vñk¨½Ìh¦Vd\x000bZ(·\x0016ú¶\x0016;*=u¦K\x001d¿-j©d!\x001e!«
\x0005mU¥i}IÛ÷ILd\x0010\x0000ª{Q\x0013qªM\x0010¶ª$ØDkeAkeß7ÆÃq´ôIvÏ±jAüÆªM\x0007Á¹\x0002Ö¹>X;.\x0015c?jêt.5uÊÅ\x0017õ¨å)è5´ÖíÂ¶/~1p!µ}-V7®
%l§¡G64\x000c-^_¸ÃËTÇê5ÑzQÐzÑG«5\x0016ÏÌ¦V±è·3$°\x0014i\x0007}\x0018èÓ\x001f
~>Üý¶»¹ûÛß\x000fW\x000e9(ä$-ê$Ëý\x0005nÄÔFV\x0007wNÅJow7/ßìoÞ-M8Ó§å?:ÿô0£\x00004K\x0014N©ÙA¤»!\x000eâØYåÌªÙ¸y6¤\x000e1.&µ~.á:,zà6d#ë\x0001dHÛÌ@mÞG=ÅåÆ&f3~fÐ\x0017$¹/UÂ½TtÒf¹R¸	ÙæÈvà4k2Æ\x0001\x0015Á¹\x0019=©S
OË]?rôËó-O{Çj<Â§á\x0013h¨7cö9³ïgV\x001b
Cô(l¸PÖ`T±\x0015rÈÃÀa¶sýAÜåñÒñèFY¥×\x001béc¹Q×6KzòÓX)Î.Í/ÓÙç6æÂÀ?Á:\x0019gO\x0017TA¡Ãâkz\x001btaaÀ:KãyghÅz¹âP/)´!\x0017\x000e\x0006,]<ÏdQõ3«hëåz6æÂj@¿Ù\x0010Á¦m\x0006ÍCÁ½àDm\x0017ß[ - ñÇþiôt8$wXj\x000f«]w}|ÎLíÊ\x0008É
ÄHÂ±®LÀ«4íuªî®\x000fÖë7Û\x0014s¤Úÿ>\x001fN×ê)õo)Tâ\x0007cm·4{§èyßB\x001f»fqû41Æ³.©eÑ¶\x0003eé\x001fFB=Ê\x0016Æ\x0012ë¯)Öóéo`µÍéÓ1Ùlæ\x000f¨èùK^Åi¿¤áæ´çÉwRpM®\x0012çÆ>G5Ïï#ôyf3Ë~f4{óWéP2&H\x0003k¿Ê°!³ÊÕÀ>{¬0Z³\x0003kåEfÁº\x000b¶z\x000fhgÖ9³îg
ïXÓ>SC¦NMéüYa
À&\x00076CÀÜqí<»F© u+ØÖÀlsf;pù}J[úI¤Ô|uµ7§ÙåÌn`mjÐ7"
)S,3 ª\x0006º\x001dÙçÈ¾\x001f9\x001adaI\x001aAq5]4ÍÜè6´\x0019!g\x000e\x0003ÛÌ\x001aË8\x0005;B¥b\x0012ýäfÌÙuËÌµ(Ý\x001b­PÊt¶¬\x0008"5+éCU\x0011½¹ô\x0003N0F¤¤\x0003Óê¨IAj~¨JíÈ\x000b\x0001\x001f¨4eïp\x000e"`\x0000\x0006º\x001aM·#\x0017\x001e\x0010\x0006\`¼k²\x001aB°0Ô|ctºÝ>\x0017.\x0010\x0006| veì\x000cÜÎ,^\x0012À¹ù]
Ð\x001b\x0001?\x0018£" Ó1Åµ\x0011Zñ>3«\x0001ºð0à\x0008UR\x00136RPI£4\x001c \x0001*>nÅ\øA\x0018pZ°±C
mêhKùh«kùvæÂ\x0011Â'Ä,{ìl'ÛaØ@z\x001d[;tá	aÄ\x0015&\x0011\x001a\x0015R~7ºB¶\x000cÕúÜfhY¸B9à
5¤Ó\x0011+2¤I
ë\x001bÐ²ðrÀ\x0017\x001aAo{¤õüh¬«3|ÚËÛà+ÔI%ÞSX<WZ¶\x001cÂÂf&Z\x0016~E\x000eø\x0008M\x0007:ÆÐél\x001c¡uµ/²\x001dº0ÑrÀD\x001b`Ù=2\x001fc{W}m.ì\x001c°w¨ùDÎ\x0010ß¿¥Mc\x0002DUÛ­\x0019Z\x0015¦C
\x000e\x00138É«PíÎ´\x000bÇ\x0012ÍïP
|Vð{ÒöÂÒéðÔ¨Æc3æâ3T\x0003¡
|ÅRè\x0017É¯\x0004.è	õÚùvèâ3Tý¡pT÷KWFqEÚ.&UÅg¨\x0006>C¬'Iáô\x000e.âJÊ\x00106:tñ\x0015ê¯\x0010'\x001béTîe\x0019:ûínºø\x000cõÀgèý±f5pëÂÊ,ªY=7w5´×ÅÆ\x001fûý¡¢¦\x0018+i°ÓøT´\x0019uSÒ\x0003:H\x001e¬<`»æ´×2	eûÍBP&IñÇ^j¦ÖiE@4¹>8ÖÆU\x001dßQ×ßâfê2.
C©äàÃ\x0018>Fëæ^uÊaó^Ër¯åÀU\x001c~8é\x0011¨ý@
®²ÿ![\x0005\x001fA\x0015·Zü±?'-/HûL)®zÀCH\x0001ª/ÌÐ ËS=ý<r±¥Lº¤qÌzÄS½Ñ\x0013\x000bÈÔ£\x001cH>¢6,ëþ)Í\x0019&0\x001eÒno\x0016B9\x0008pÎfCáÛ¯å¬ô¡M4àT÷(UÆTÈfÙ±¢±fÎáo\x0006d.36)¡K¡ÅvèÂe¯ÌÓËË¡û´à\x001b³M3´\x0008<\x0010\x0000¢wÛ.^==,1f\x001d9,Ö§YUâhV\x0002p\x000e\x0007ªCë;`NÙÃ\x0008ºÇ©Ì\x000f\x0004´
@¦|j¨Îé\x0008NÊ³áI÷iqseï6KJ"Êk¾jÁ^Ç#îé¡-wéó4ÑóÓ\x000c¸$\x0002¾á%Gú¿ürmø¥?L1é{r$Ns+ßÐ®üÎ$YD	ì@§\x0010\x001ehÒ@BpÛ¥³åÉ1\x0003§ÜFóM§\\x000bêA¼æ¶¨ê\x0018÷\x0018-\x000f#[>Y\x0013ÂCªh\x0007Á½û1\x0014ÝîÕCýÎù«!{~|éÕñ\x001eDºË2ZHNoo,þ/c¾\x0008kàÉ$v«ÿLæxÑ\x001ct\x0019\x001adt\x0010\x0017@×7+Òìâí\x0002F)·ïrlß5\x00176cÐÅÕ.&¤±¿ÝNË\x0012ç÷ö¡óîÒU\x000e\x001fXSÀ\x0004º«m_=\x0011ãç2büÜoÕ5§'ª¸(*pQÔvgð»°\x000bÆâ.vO2BñFò+\x001bú£Ï'þ¨Ç­¹PDí ÕúyËQ«ê·õ\x001c_ÊÒ\x001f¹ÄË§\x0007x\x0014Çâr#Ç×~¹]Ä%ôéAÑCfR7ÑNLº¨sä\x0002ÑªW;wäáÊÈ\x00053qý×¹\x0010xv55(¥à2mYïÒí¹@~C\x0011úd\x000fé	\x0013¥4ùy{®DôDãìÎ;ÇÛ/5¾=<üãðáÓãnÿðp÷qµüw´ÉbÌ\x0005\\x0000atòýa±Yóíþúçýó×7»ýõõå«E\x0015"b9»\x001ccGùTQ@÷9#ù¸Lãç·DW9º\x001aCW!5ú{Ï~H\x0007ëÏ}ì:g×Û\x001e¸6I£\x001f"
Ô½"Übß;»ÉÙÍà¾+ª\x0014Ô^s´\x0018\x0003GÐzÚÑmnÇÐ­IQú1Z42eè¶=ì.'wÃ\x0007ÞÂuüdY°JòÄi\x0011[²ûÝ\x000fîzà8 ^Ø®\x001bÅÍì¢>Ð¼=äìaõ9´N]fF:>1jq¦@3zV5nI\x000cú%r¦G\x0005\x000c£¼L\x0017ÒM­#\x000euÐ£ZH§\x001dü\x0005\x001fö$8\x0003Kíè?Aêø©+bò¼é¸í!¥¶ÝöÂ¡Â GuÇw)+áz½§¨\x000f¾ð¨0èR\x001dÐªH\x001eU%Å\x0017·¨øÒÎ^xT\x0018t©øÁ\x001b\x000f\x0017Oþ£6¾ðL0èp¦Kê5T\x0013áùvjªeø}ðkQßdIët\x0012
¢;jçÊ§mÍ{á`Ô5}Ù}o¾ÉØ$y\x00039\x0012#}äøÙªmáË;Ó ×Å¥äGj#h:
ËRÙUñµªÁ¯5\x0018NöbE6\x0007c6$¡¼M¼//ÚøãèÎÓÜ9e¡$ÞoØPn\x0019\x001aøòª?úW.Ý9\x001b-y¦Ø ^*ÅðùpÿaßÒ¹Ç~+*©3Ç®¶jmZÛÞ£dkæÀ´AQ¿øð_ÿñûüô´zü"ÞÈX\x0006%y~aáM­]Uñ÷[ºÞíÿ|óúvQiØuÎ®Ø§óìµH\x0019Ð]ÍB\x0017S¦:´Ýæìv=Þ¨ÝÍIÇ½\x0014\x0005¶ä{\x0003¹ÏÉý\x0018y4â,
`c@)IðBñ\>©«\x0003;{Ø3ív´jb\x000c^dåã÷yaì,iù\x0006\x0005ª¤é/>U\x0018ûV¿4|09|0\x0007ÞYÖ¡æ$TÀ«ª6¾\x001d²\x0001\x0005Ó©	g>2J*ïqEÝ½M]"ÕDM\x000f<\x0014\x0006`ÐÔÈ °Fs.ð¹¦
¦¶'ja®\x00066]ð®w£g^¢¤ê|æ55~B*ë\x0005µ¥±\x0001Y\x001a\x001b9jm`Ê\x0003Ï\x000fÙÚA8Ã/ÂjE½L\x0003=ôðmÑ«^
Òkª}Q§yúd\x0001v
@uO\x0017½.é\x0007C/M_~´rô£µ^BÄU3¼JõJ¾bí÷%ü`|óáKG%\x0007\x001d2³¬!YË¸%é*²¢²`=¼*Í¥\x001a5_\x0016¾´jÔZ~Yø2°T£å/-½\x001aµô_ôU¥¡W£þËÂ\x0012~0¦ÿÂðeX¬\x0006Ãâ/\x000c_Úy5jç¿(¼.í¼\x001eµó_\x0012Þ\x0017\x00127x!1\x0001+°ç¨ØÏ\x001d\x0008x\x0015´)*Ö°B\x0011êH_¦1ÓÞÒ+Å\x0002\A\x0005®ß³\x0002ræÃÄS^	7'ÊB¸ë¬à1ÍÚ\x0004Ã\x000føF£ÐØoy-çåXÈ\x0007è0ö7ðp\x00114 ¤6g-\x000fbÑ°Íùwü>ÌºDïÓîå§ß\x001f\x001eþ¶vÛµÂ×(\x0016ñs>\x0004ÁIz'\x0016Åbow/_¿z÷lýò<±Ìe71H.á3õñañD\x0013s7\x0002V9°ê\x0006Ö\x0010¨.\x0018S}táN\x0011Î\x000c·h!Ö9±î%\x0006\x001fHÖ[GÃBUAòo±<Ìµ	ØäÀ¦{­¤ÙÉÑÔQ8DïÄ\x000f^ÉxmÎk»7Ø9~×Rñsp\x0000H#¦õé[]NìúíM\x0015nj¡íN\x0015jQ¾8äÄ¡8:BR\x000cÖÖ'boùPØ­\x000c\x001b¦¸Û\x0016Cð\x0017ÆÑw'¸A&¤S¬\x0016k\x001e\x000bË\x0006Ý¦
¼ ±ÏÑ½)®É\x0008Iß}zÝ\x0008¹0mÐmÛ\x000büB§aÿq\x0014Òå¼MÄmnã\x0006.½Ì¡H
½C\x0007a¸ðÅûÍÎEaÞ Û¾	\x000c\x0008\x0019\x0000;4çgÐTg$\x0017G*7!\x0017ö
º
\¼ò³¬#¾\x0005¨\x000b^\x000cÎ½\x00055\x0013ûØwo²ô4Ò^KïX/Ì)ÉÄbYç¿\x0005¹0ÉÐmáØ"¥¬;nr*Z¬öv·\x0012gÕ[\x0018lîMÆÁHó\x001eãÓþï\x0006\x0016nµÃ²ð!²ßà\x0010*ð3\x0011f?¤\x000fÏVû¡\x000b\x001f"»}\x0008'(tÙ30\x001c\x00153·2n²°Ç²Û\x001e\x000b¯YYA\x001dk<<÷© 6\x000b7eaÜd·q\x0013Æ¦=\x0007:M\´¬xWW$jF.Lì6\x0015bn\x0005ï\x000cÞ¬'dãxÅb»S\x000b²*¾=ÕýíÅO_÷d¼KSTï¨Þ-Ú­*/¦ý^¼*ORwJ;¡ÔÝbÓD\x0013rññ©ÞoÊÓQÃ§Ä\x0011=³A¶¤dTû·:ÉªøøTïÇgÂ±Ú]b£Ä\x0010×Èøªx3qñí©ÞoÏD\x000bÆ\x0011'ÌyÑ89=¨J·\x0012ëâÓÓ½ÁI^$é	6Më5\x0004ý\x000bËã±Ö £\x0010EY§\x0019¯zÆÚüüéãýÇÝ÷Oï]0Ä`®{ÑÝ]\x0008Üåx¾\x0015\x0015÷Æ\x0008©:m\x0005÷¯Þ½~uõj÷ýí³\x001fòD­sjý­PÛÚ~+Ô>§öß
uÈ©Ã7B}Ì½à¿äÜË×]\x0018\x0011øV¬È1o4a«o\x0005»0~0bý´eí hâ¥	Þ§©Ïz1ühÄ.¬\x001f¿/]?\x0018±_\x0012;+\x0012E¿.¾\x0015ìÂ\x0000Ê\x0011\x0003øE±Ë(jÄ\x0000~QìÂÈ\x0011K\x0012\x0004?Yy\x0008ó\x0000h\x00005ÏÚSvñ~Û]X\x00129bIp¢ù¼Û~\x001aç\x001a·:°§®\x000f®ë`.Ì\x001c1#FÓÔí\x00000\x000b§ 5?gj³á\x0001Q\x0015Q#V\x0004õºi\x0002­Òè,glÉ#ÙÝb*o-¶\x000be5AüEª&¸ûm÷§Ããû+'¸Nâ³
½ÁòÔP!
u¥k+6owÚß<¿zµ0ÀeN,»µ£92\x0006ÀóÔ,Íú\x0005Vº½\x001aXåÀª\x001fØS\x0002Ä@¼¦¤ÒÍÓ}írÁF\x000b±Îu?±\x0005tf`µ'ÀÙ\x0016`\x0003~`E¯W\x0006=n1Y9ë\x0016\x001bÍm\x000el»Q^¶XOÓ+HyÎó\x0016Wû\x000e}Nìû%=\x001c\x001bÀ.[:\x0014I\x0011Úå\x0014SÓ\x001e\x0017ÅjÓ>çÃµ[Á-\x0016R
®ÀÃ1¼Õ`ÄI\x0011åêÃîæ_ÿüûÓ/\x000f÷ÿû©E1³À"ARÝ,ókê"\YÚ~wsùæöûë«nÔh	2_\x001c_7\x0017^Ñ\x0012<®fnÉæº\x0019ãô\x0006Û¶%¨|	j|	V\x001dÿ
À#\x000fãwK\x0007ÈX¿ù_AçKÐ\x001b\x001c$Gï\x001cq	½¼QRò\x0012V\x0008¹6.ÁäK0ãK0áÂÛy	8\x0002\x0015PA°ýA²ù\x0012ì\x0006\x0007)[\x0001\x0016Vÿ
i¨[»õ
\¾\x0002·Á\x001fÇ¬NKÐ,,bå\x001f·\x0004/ÁoðG$Uk\x0004ø¤\x0011\x0001<\x000cÔ\x0018{^Ã³q	!_BØà¯ ñåo^åG@´¯¼\x0015S²Û\x000fË\x0016§Íÿ½\x0016É±E²G\x00192>HnM\x0017zÛ\x0012Jç¼wÆbæN\x0012ù\x0005\x001d|ú3Ø­*\x0014Þ\x00196pÏ\x00068ª\x0013ØÞäj4¯\x0001ÎË\x00087®¡pÏ°NSâ\x001a$OAÒû\x0010Y1e¥q

\x001c4Nt¥5à\x0013¿¥³Ä¤fÍàûÆ5\x0014\x000e\x001a6ðÐ
HvÝ`
\x0016ù7í8kó\x0007X¥ÂAÃ\x0006\x001e\x001aËøÏ0
\x0012«Á\x0018µbìMã\x001a
\x0017
\x001bøhÌQgQpIuØ¤XOUï;Ýk(|4là¤¦[C\áQ8Ú'³¤Ìæî¡pÒ°ÆtO!\x0019b-9`ÕVYxi¹EðBHÌÚ)¾ú¨í×P¸i9î¦]°8bn^Càú#­iUnó5è
Ü´Td0¼àþ\x001em\x001d%\x0019VHÇ´­¡pÓrÜM;\x001c\x0008´­r¾bÝ\x001dÿ\x001dVÌo\Cá¦å\x0006n\x001a\x000cÏ
Þ¥5\x0014jÈ\x0015ÓÅ\x001a×Pø8¹\x0013iZ.~ÓíO>nÅ´ÜÆ5\x0014þAnà\x001fð\x0000±Hù\x000c´£ã=bë5¨Â¶ªqÛêIßtPósâdÒ\x0012VtÏ¶-¡0Kj\x0003³ôÅ/qªø¢Õø\x0017í¼åéÁÙ4,@J¶JU%ïÎ%2X2\x001bDK¸\x0006ê \x0008N\x0018y\\x0002\x0007K°õÇ\x0013óÌÛà2m\x0005çÆì1A	ÜÔlV\x000cVkµIålÉ.´Ä+ßÄéJÔéh¡N\x0003%yR_pr.øÂs\x0015Ò§±b8âº¥ü"Ä¥\x0004þ¼¿¿ø.þôÝ»÷¿â
}zºx8¬}\x0017\x000e\x001d\x001bþ\x0011´UóT\x0004\x0013¼dm\x0008\AsùìG\x0004öúöêúz\x000eÙ;#ã_;3 hÆ<ýÜ\x000b=Ù9^-Õ\x0004
­ÜpÓØ¯´Ó¿toµ m´ó7j\x0010·ÚêÚÉîÀ>b\x001fz±-
\x001008êc\x001a 005-ÝúÃ)õob³ßb¿ÿz?Gü\x0012OÅTÊóì×»¿ÝDæ>Þýõqµ$\x000b(J#ê ô\x000f$ÉbXDÚTóWÏ~¼|yõ
±_¾¾}uùâfQÐä¤ \x0007¹å·Ã­rnõípë[;Ü&ç6ß\x0008÷¤ìÒg7:VRi*7<ÆÞGKÎZCµÛ^\x000b8\x000eÇ,k\x0003±¯K~vßß=þu­ýsÑèi¾\x00189\x001cvÀ*°jO¼¸,6Á]î¾¿¼y±`üUæ¬²\x0015t*¼´ôzR|\x0001\x0012Ë\x0016«QUªúP&
h\x0013NÕÊ§r\x0018µÜ<½\x001aUç¨º\x000bÕ\x0006ÅÓÖ\x0017óL	\x000eÿµ¯>·¡\x001cÕôí*Þ´\x0008Õ\x0000?\x0001ªTP\x001e\x0016G+­Gµ9ªíCÕö\x0002éh®Üñuf\x0003àrT×ªRn$8ì;w5]\x0000ë2÷m¬>gõ¬ñÏîÒ\x0011i\x0007)k\x0013ëâ¸õ¬!g
§uJásæ/Ð\x0011°Yêo±#z-k>±Á¥Y}­V@ºÔõàTV÷Éµør#ØÒgõ9-µ@NÖsS±T<úS\x000b¿4¦l=lá	 Ó\x0015(Á½üÁ'½\x0004eÒÞäÄBa_¡ÓÀÊhµ(áF3ªæ)F.NÖYÏZX-è6[¤ \x000cÍk8jnâ
 °\x0003Ði\x0008â}D@5ÀñIÌ³~Ø²0âú`à/ÅÇâ=´1^á\x0007\x000b¬@£CF1ÇØkPÿå$zÑ]¶ ~SpìÆ!Ñ\x0017\x0019¸QD»\x0002Xý\x0017Sâ¾hK§«6\x0017\x0002p{m´¾[\x001d÷%îû¾[\x001dCnÃªEJI\x000edÅb7p\x000bî/%î/_±ý:Ùu$³Ûs\x001ea­0ïÕ°äÊ\x0002\x001f_µq8\x001b|è;\x000f\x0002Ó¿óy,»¥dHw°Á\x0010\x001cÜÉÌµø¬?áíáþãçÝÍ§÷¿®\x00046Áòë\x0006VLb
à<Mêæ¬ÎÚ¦×·û«Wïv7¯ýxZåÔjZrqW=\x0006x~øVq§·£Ö9µ\x001e ö<ÏÏ
x3´°\x000c}N(º\x0005ÚäÐf\x0004úØ7«ýq«S»o¨JÉuPÛÚmµ%³a%ß-À\x000b¾
W
]\x0007´Ë¡Ý\x0008´Âçùa°SevIÊ½.>ÙAísj?@í\x0002
RÃ&'²\x001f_¬uý\x0012×Á\x001cræ0ÂÌ5ë:\x0008waf·
&%uÎÖ{7Pç³âíØÖ³
e\x0000JW36gMÎ×\x0007´`C
\x0003Ø¨çH	\x0014e¹Ô
¢æ\x0010´ìÀ.<#¸F\x001dÒÅT[Î¥âþßhY¶³|P¸F\x0018ñ8-\x0018Ø35\x000eð<¯l¥Vù\x001d:tü¹\x001b£åÜT¥D
\x0008,p¬}=îDb)\x001aÉjE:\x0002\x0012ÃéL\x0014Å\x0000:+!~urÃ³\x0002ÇX¾ÍÃM,+\x001d¤Á.\§Ä=W\x0017¼\(sò"æwß½y8¼»}úøÛÓÃÊnf\x000b@µEFpO^¾\x001a¼¹Þ?{ãÿãííõR\x00136\x0011ËXö\x0013\x0010(7\x001f¡Sí²\x0017©\x001f!Øêû;µÊ©Õ\x0008µ¦Ó\x0011o²&é¯\x0006î\x0004Á3¾\x001dµÎ©õ\x0000µô%&jÔü§AÌ\x0013J8nt;jS\x0011êc\x0003gE\x000fç¸ÎÊjSi3´t¢8ÖñÇþO\x0011¦©\x00196^&YT§\x0015àà­°*ö\x001a\x001c8Ù@	ý¸Ûê(§Ï/õwÝ]äC¦Ã¿è?)\|d§\x0012(<ßü|jaS[r
¯ÆàñîÎ\x001f' Í¼ñÜLcëÏÔ-ð§R\x0014b¢xóéñs¤þ¯ÿøÏËßþ~øëÇÕã¢ÍÑ¤D7éXÕó$ÆVGË¼y}ó.Rï.ß¾Ù¿xµT¶pª=!fínæ Rr\x0012Åw\x000cï4Õ*fd#«\x0001d+R#®\x0004®Cw&5OÚªPW3³ÎõÈ6ËcÊZ³Môi«×öff3}XËÂ½óÕq1\x001eäfáj\x0007O3³ÍíÈ>kVÐÿ<çtÜñ%#Tg\x001073»Ùì3\x000b\x001b!B:\x001b6\x0015ºª¼s3³Ïý\x0000s\x000c>tº­SÅ\x000b^`êÎ¥\x00159äÈad\x001dI)NM¦T\x0010ç¬æmÖ1CéQF\ÊìýæúÔsãl8vYW#§VèÂ>Ãv"]\x0017ñe1A§\x000eÌ­Î3\x0014¶\x000eF\x000fé@{\x000eóR\x0012Çm¶ÉÑ\x0011«·.:\x0019ØzÌ;ð'èªåqí»\DwóNOá]7;ÇÕ³ú#{CÃ9J_¯so>Õ¿cWcìÎ^\x0010zü6\x001d]Àø&cê3ÁVðeX\x001açA°EéåýZ`ã½8öÖÓ=Wù$É¥¡VçÃ¡4v&½¼Z¬rd5\x000c\x0017âÈ\x001cèÔ¹#ó¹»Ëzf3~fmé
\x000c%a²bEø\x0003]Îì\x0006e\x0002¦j5emòõ0º\x00198äÀ¡\x001fX¹\x000bB'ò)+RDZ·y­ÈP~~\x0003ßJ\x0002½ÑÇÐ2©ÿZús¹õÌÅYÃÜ]\x0003ÒÈ\x000cRÌøó\x00085½\x0006«ç\x0016;Äæ\x0011¦zmÆ¶'Øvà(\x001aH-Éé¤p	60\x001cÂÃIªÃ\x0003w;üéîð\x0011[4\x001eî?®$F¥éy¾Q3e!%¹\x0016~\Ò\x0015þÓåþ\x00156h\_½:\x000f,s`Ù
ÂÞÔ\x000eè81c%\x000b"âTÄ­U\x000e¬ºâ\x001c\x0007?Ô4±mó4m#`\x0003ën`\x001d¨g'\x0008Çá¨MÁVÃfb\x0013nbÏ£ùP_lr&¾Þ#ÚLlsbÛM¬<«iTÄ?»x¶i»LC\x000e\x001cú·XÐÔx£æ\x001e©iy6¸·%æ-ÀYý>\x001a6ÑM.d6l8·ä"=a\x0013Õ`3pi¿\x0001S\x000c)~[\x001c%âÀq'ö#0rµ.¯\x0019¹0ÆÐoILÇ3AÅÑV³kÅ9©M¼e~Óöå\x000eEaÙ Û´yÏ3ã§2	ëJÕe#\UÅ®\x0019Ù\x0015È®5OÈ&éÒã\x0008BÖÕrfd_ ûoà\\x0014\x000e\x0004º=\x000f'XLåt.´ecaÝV>O\x0016.Dv»\x0010o
ÝB×UzQ3¤Ç\x0018£ùÅA÷MÄyÝæÍcu&\x0011£z\x001e\x0011K`äåæ&ä"ÚÝá&
ÙR¥\x000c6¯\x0004R\x0004sl/`3s!\x000b,»m2*Û³(IB'Yt.ìV\x001f,²ì7Êñb:ËzØà:ª¥¶v\x0003¶úþ×L\\x00188Ùmà¼ä×lã$pw;N\x0013"d¿ØÈÔ\X8Ùoá¥V¼Ýq/\x000e\x000c¬«1­Àª°oª?DþbND\x00151²êQ1zntÆÂsù¢v?½øOl\^ÿûM²4¤Ø8Üo\x0012ê¶@~\x000fßÊ$«ÂÀ©~\x0003\x0017?8*\x0017Àv]w"\x0019ïS\x001bdÐeX¯\x0007²,Ë5t?µ¬ï\x0019ÀlsA\x00058½ïõßø¼Ó\x0005°ÓèQ\x0016ÛÇ å	t÷¥Ïc3\x0005C§Éæi$tÕ¶aV'Ìýß e­ÈÈ,<¡°¹*ß\x000c­O û\x0003#ãX:8\x001eon6ÅÚ.¾H\x001b\x000ePÓk9fîã3h8>=}\x0012à?=ÝI¯oßMéïn¯2ö\x000bÂé\x001cwú¹\x000b\x0018-ábxº %9\x0016Ã×Ûy\x001bþ\x0003d{6ëÏb,ggA¼¸áI%¾\x001eâ7@ã¡Èú\x000eæcqè?\x0017ÎÅd§s¡Ò¹\x0018Üf\x0011NßD\x0002d
P×{<<­\x000e1\x001c)EèÓ@\x0007²¨V4Ü°úç\x000f7ûÛó´2§ý´@FB*îZ´çEËÖ@«rZÕIk5©\x0013L´ô²\x001e/ÔioÏ	A­¥Õ9­î¤õá\x0018\x001eK\x001eO\x00123§äbÆ¢Öä´¦Ö9V÷9¬Ñ§«¿ÜúÜÚÖöÒÎ×Q£\x001c76b$Ì\x001b»ok@u9ªëC±\x0001O<{®6\x0007X'Ú3\x001aki}Në;i±6\x000cÑ³²JðÞÕZ[K\x001brÚÐEÝ¬ôk0D#XÏ\x0017I7|\x000bØìQ)@.
õuî-¬Ï¡n\x0006\x0016\M¸Ä\#n`c[/ún¤-\x001c\x0019ôy2l-ã\x000bã\x000c×¨[^¸Õi¸'>W6ÔÓ|clxÖsJÍiË¸ºÚtÖ[¸2èóe1$}Ç6Tc*\x0005Ç	îÌ ÛÕ¸/^g&|rüÃ_ðÄ\x0011®£\x000f(X²	máË Ï¡¢)N	³îsÎ)NñD;¶
ná! ÏE §å¬ø¯y\x0006S)ïWïtoÃÕ}Vwjª |C¼¤QÌè´Wis7Â ¨/n\x0010ÑWy~9e6ýÌÅ$£A\x0003nj7Ò°EÅ\x0015ÐàeyM\x0003TL¢Sñ´{ûééÃ§§ÇÇ\x0002ç©D
ï\x0012ÚÂ©j^\x0005µ¬$x»{ûúöùëÛó¼*çU½¼x=qE$µI+/j
¸&Ç5½¸10'%.\x0019x¼
\x0004TAT§|®¦5'wv0pZ\x001bÓ1QÅ¤Ï>°)\x0017"\x001eØ.Å¹vÓõHN.Æ¸\x00005¾\x0000Á:þ£X;OÜ`-Õ"ÿ\x0005è|\x0001z|\x0001s­1¾H¯£§\x0018b
sã\x0005|\x0001fx\x00011V¦j©Ñ\x0012Ü2i 5¥Ç-ü6ç·ãü)Ù-0LYTY\x001fVu´ðÃ_>ß=1þbô\x001ci*\>\x0004\x0006ÐCú\x0010ÖTÛ·­£\x0018)Ä\x0001À7³\x000e\x000c\x0007Ê4¨0ýþðøøïk¯ºi\x0016i\x000cZv4°j'+9ï÷77>Ï*sVÙÍJ\x0015ÖÑ[±Ò	Üãà`Y¢u5«ÊYU\x001fk¼ñ¶\x001a\x001e-5*åYW£ê\x001cUw¢\x001a.ä\x0003\x0002o\x000b\x0010\x0012ë¢|èjV³NÖ£A\x000f·Æa+(³mXmÎjûXqú8\x0001àë=nëbÞ`5©ËI]ç®ú\x000bÞTqÁ}\x0000Æ3h5\x0012i#õ9©ïÜS\x001eïiâ-Ml\x0002l\x0008ÛìjÈYC÷ßjôÀùÿæï¿Ø^±\x001a5×Á7Çg#k\x000c§\x0005U\x0007Üe\x00157*Ø°X·\x001e¶tY>ËôaÅCÀFã\x0019ØÄ¶Bá\x0006 Ó\x000fÀåm\x0010£d*±±Ò§\x0003»XC¸\x001e¶p\x0004Ðé	¸Q:Þ£$¿,Y"z¿ü\x000e¶µp\x0004Ðé	ânÊùm	Px`5kCX¯·ù¼
O\x0000]®ÀÆsÏï¡øyQ]
ÜilÏË¯-\x0001tz\x0003{<²V\x001f»'¯Ö~\x001b\x001b\x000b?N@ý` \x001d_A­K\x0007Ömt\x0006
o\x0000î ^
8ÌÒôDãX}ÅÚmöT\x0016Î@v:\x0003¬±£\x0003Cr¨÷Òi­Î\x0006lc-|ìò\x0005xI§g@I
É\x000fjG¢¬f-¯/]÷Èj¹Ü\x0012°\x0018\x0002\x0002ïø¸Úm.\x0005²p\²Ëq¡¶,
!7Ñ¤ª´xL\x0019ÖTçã¶Á\x0016Kv9.j\x0008
\x0001eP"|ÞYV'±vy>ÒjØÂsÉ¯ÛsÉÂsÉNÏ%&qøyg%\x0017»G\x0017ÀÎ`\x001bÇ%\x000b_ »|Átd©Ã\x0004¤OñKvd·_TadU*"8!5\x001f³)ñ\x0012¿¯M¬*,ê´\øfO°ØxMB\g\x0010Z½üf¿\x001a¶0\x0006ªÓ\x0018H\x0016î°g_8Ô$Øª¦c\x001blñ}©Î$\x0005®ÀK¢à\x0017\x0007[[Ý\x0012,g·`\x000e.= v¤áÈ\x0005~ó4,DîâÕa\x000cÌ)°í\x0006þR{\x000cù°\x0019ÌÈ\x001eúö×q#	ø#®8â.W\x001f­¿Ùî0ôn18Þ\x0019,O{7ñtÍ]£w\x0019Ìépc3
7NuÊ³BúûÇO\x001fWJÖ\x001ae\x0005K\x001cè/¨Ý\x0007.û¬¾ÿ¤jåY#ýÅÕÍëW\x000b¢µ3»ÏªÙ#»/Ù{èc¼Ëôñ4¼#¾\x0001Æ¯Ðü÷üï\x000f\x001f\x000e¿}~¬ðóO?\x000f-\x0000¨%Æá\x0008õyó
\Jc\õìÜýãd0Þÿ÷c\x0000ìµÔ©^4Ðù1\x000bq¡^üÑ¶\x0018w¼÷Èã{\x000f*5ÿzøûÝÃýÝãj±f£Sj\x0012ÒDY§Óë¹®wpÜTóû7×W7+¸eÎ-G¸=°d
.e*}öæ¹\ÑÔÆ­rn5´ßÛ\x0019QWJnI)\x0015¬5ß[çÜzÛº£"y\x0012ålÊ[\x001bÚÆmrn3´ßfÐÆà\x001a8-à4\x000f\x0002²õA@íÜ

n\x0005CäÑ{ÒIÉõëmJ\x0014Á^äîôËtéË¼zü×??þëw»gÖÚÂx\x0015à\x000fSêôÖ¥@SÌí\x0016g)_Ý\¾º¼Ü=»y½\x0002YåÈª\x001fÙD[2/2òXW\x0016£\x0017~¢UõMÌ:gÖýÌÖ§Ât©<7TÈ@*qnãMÈ>Gö\x0003ÈÂcGÍL=V´½Z¬.h\x0001ÎÁÜñ\x0019¬ë`èx\x001d§³\x001cÿñX\x0002ðõf±»¦¸øø`àëÃªj\x0000À\x001bY\x001fÆ\x0017\x0006ØèT ^?ö\x000b°4o7~~\x001fÆ¤àI\x001d®.¾ÚHâe\x00195þØOÝ\x0000>Àô#"¹ÓJXMÔ²¤\x001e8\x001f\x0016ÅyeÚk2uÒD½x\x0001n¢\x000e%u\x00181Ð$Xòi*^Êâ,¿´0[S0[3r>\x000cßÑ\x000fR-´,\x001dëZ
Ú,tq}¬4ßÞ»Ðc ÄZ¦Ùâ\x0012´Kþp3ty.¿\x0019t}®ÇÐ½ ¦\x0007©\x000c'V¥çÓµWUoÎ¿ø7\x001d¤./¾WÕï¾»úÛß\x000f¿ý6e©Þ<\x001e>Ü=Ü}^Iíà\x001bFejâPEOUõ\x0003½zùfÿöí¬zs³~y}ùî<¹ÌÉå\x0010¹T¨o´\x0017¬øÅs\x0014®6ót«\x001c\
;Ç]SÚN¡ÕLÎ;^oOì\x0002×9¸\x001e\x0001\x000f¨QO»IXT\x0007W\x0015 îÂ69¶\x0019ÚoËj\x0017q¿\x0003\x000b\x0011\x001báXt¶>l©Üæävì¤\x000bÁäIW\x001bcZ>*zÓÓ\x0016õì\x0013=þbd\x0001\x0007Ö j5ÎÄP ©VWýu. /d\x0016¿\x0018\N\x000b )AÅ\x0002jñmÓ\x0002=ãfEÑ¼üÇáÃ¿þù\x001bffx<||¿zÔHÃ\x0016¥H\x0002@Ö±<JK>¹üyÿçùåîý«gKeøötâ\x0015yº­{\x0011^s\x000eHâhhXÂóË\x001do]0ù"Ì\x00060»kâéI³tª*^~&ìZÍ×`7XC¼WÓ\x0012¬e\x0011:g¹(ÖùºM÷\x001a\¾\x0006·Å\x001aÒ\Fi\x000c\x0011Î¦Ñ(O÷"|¾\x0008¿Á"Bêd.M\x0011q£6·¬ëÕ·/"lñY;\x001e\x001a'MàjEç\x0015/Â-\x0002÷,\x0002J\x0003»
ééHj}aè)#<9»xÃí[*V¡¾I\x0013\x000b¾ø´ñÇ
,ðíq\x0016Ì\x001büùN\x0010ÿ\x0016\x001b\x0016 ¡ø¶§Çâô<\x0016|\x001a.\x0006×!Åö^»T\x0001ÂcGýÀZ¤ \x001azêL\(Åwb»½ç¶§\x000b±Û,Ä8ôÚs(å¸\x000cÅéÔ\x0019(\x0017e	;?ôßýQÔ6ß;+\x0017þ8ZY¤Çj»xûb\x0000ìÉ\x0015\x001al¦¤öæþá×»ÕIP\x001eÖ\x0002J\x0011izàù\x0016ê¬ÂÄ«ë\x001f/r,D«sZÝIk$?`÷\x0013éO\x0003?\x0003FÚsb9kiMNk:iµ`áÍ\x0010/;T´$¸hÉ¨³ú(kimNk;i)Ù\x0016´%7\x0011m\x0011õL\x0001ÁjT£ºNÔh/æi¢\x0006gÍ\x0008à9=F¹êÜÖFZÓú>Zím:\x0006Jð»Ptç5¦\x001aXCÎ\x001a:w\x0016SQ>°4©\x0000H\x001fØr=öjÚãs*ÒfBjm¸ø\x001a\x0019\x0008×s\x001b4XÇ\x0007!Tgo6âB\x000b¸\x0000=\x0008.y	aù$h8=X\x000bBùrwUçÑ5Jaâ?4*"\x0017g*Ä\x000fíÚ:`)\x000b_6ýÜ	l¸\x0011\x000e«r)¨ÿ.Í\x0007¢:Z±ÕäþåÒèþÒ	,9y\x001d|tÅì#ä#±8r¬	øP\x0002\x001f:\x0015©°©¦º	O\x0013\x0015£Ï«¦ W\x0002\x000bw¢î$ÌDx\x001f\x000e»\x0017\x000f\x001eïï>^+a\x001dÐ`d\x000c0S-¡®îèO\x0016\x0007°ÌÂ\x0019/®_Ç_½{·\x0014e\x0012¹ÌÉå\x0018¹#--+px=[Ã\x0016ã\v¥\åäj\x001cÝÇäI,\x0008M5#RQ\x0019¿YøÝ\x0005®sp=¶å\x0012\x001b¼¦-\x00111uKÃSYô¹«{#¹ÉÉÍ\x0010¹ö(=m¹ôì¼¥¤â\x0018=/\x000eíi&·9¹\x001d"·\x0002Mß´çÑ
R\/µâÓ\x0002g.èä.'wCäÊS\x0005c9µ â%ã{ZÁ}\x000eîÇ¾Ouü>\x0005_üPC¾O³é\x001c<îøÜgÁtÊÓ°\x000bÔ­Ú<¯ûy ÚõZR\x0017±\x0000éùNJ\x001e\x001f\x0011½ýY9Ç\x0016ôÂ\x000fÁ#»îé«i\x0004sF7çâ6ôÂÃAWª\x0017-è\x0017ÀæÆ³z-èY1»=8³/\x0002j¥à\x000b	gÒJ­KY|$ó&¾¾\x0005\x0004àW:\x001c2A\x0019déÙÌh¥7];]\x001b]\x0000\x0016ëÒ_ ºW. Bay:<ç.\x0014\x0001Øé\x0002Ôè\x0002\x001c\x0012Ç41\x0010Jn§4(!»i4sÊo68Aì§T¿+=g$p\x0010Ï&\x000b°ê´b@ñ­\x0003SÁÿúÿ>Ýÿ¶{vøÛÝÃJr¼1ÏAvp\x0014
\x0000"×Ò/\x0016°MYà×WowÏö//¯ÏË\x001c\\x000e\x001b \x0006ËÑ¸\x000c	\/Å\x0006­à*\x0007WCàVÑÇ\x001aÁeÒÕ×*/Îh\x0005×9¸\x001e\x0003÷T5
sIÊKóC\Î³´\x001cÜ\x000cÇ¯s~ÄÑ6\x0008î·\x001b0äò\x000ba+¸ÍÁí\x0000øTÈ3g¶4ZH\x0016É\x0008¤c¯¥öKiÙVp»±\x001dTk¯ñÖdX<u}¥Z|åo\x0005÷9¸\x001f\x0002wz´Å\x001d:*iô»M\x0002­à!\x0007\x000fcà\_ªQ%Ö,×UÄpl)jo\x0004Ïî\x001bèÄ\x0007ÍGµá$®"<ÕH_\x001cÌÙJ^ºÎ1ß	vZtü!i?û\x0004\x001e-Ìàë1ß)\x0015Ï®!{*F\x000e\x000cb\x000cc\x0002ÞVòÂwÂó[Î¦\x001cÏá=§\x0015	sg[É\x000bç	cÞSXzÃÖÖ\x0004®\w,Î$Uµª·\x0007¼p0æ=\x0005*ftBæ8/»y¶uBPxO\x0018qÆ£Ø\x001cTßdÌÑï/vOµ\x0017î\x0013ü§¸s6@£0\x0004Zæè\]£¼ð0æ@Y\x000e\x0005òÒX
gÓaY¼Ó
^øO\x0018s @ñ9ÎhKG\-vø7RËÂyÊ1çS¯4¹}Ïï\x0000¨®Æn±z£¼prÌy¢04\x0005Z6©V&á~)\x0017+([ÁË{çóT6]<Eà·EB3ôm.>\x001aµ\x0017ÎS9Oíy\x0002¬\x0003Ám_Vr\x0015´ô[:OY8O9æ<1+Da¹O/æÖ¤èÖ,fèZÉ\x000bï)Ç¼§³T\x0005¤±m¹åNz©\x0016[\x001b[Á\x000bç)gÀ+þ\x001ciag=;OG\x00034\x0018·%yá<åØåSÈDîEjýrâòÅjÁVòÂyÊ!çé ©IN$5\x0000RqnñÍ¨»ðrÈwz£yÇ1¥Å7!®å¢¤k#¸*Ü§\x001ar8=Fû\x0004îyè-ÑFð
Ã\x0015U¸O5æ>\x0005OdÒ$*b,+GH¿IN\x000b/\x0013Î8¶6k x{x|<üßûÕraA)\x0014¬Bl?0Ì}EØ;Süvs³ÿ_WjgD-sj9Bí±Çc¢KgOÌ°¬XÜÆ¬rfõ­ì´Î©õ·±Ó&g6_ýNÛ\x0013ù;°æ8AnRî»û\x001f?=Ýþ|÷¸zX½s©6\x0006÷\Q­Ùn\x001bSõ8ó´¦I¹oWÿîÝåÍÒÐzÆ9¾\x001cÄ÷\x0000Ôf\x0012\x0003\x0008×¡
PÙØjÕr/¾ÊñÕèî{Ç\x0002â³Õ\x0003\x0015cÏ\x000c_kç×9¿\x001eæ·¬1,Pw^1?0ÿáwíü&ç7Ãüi\x00126_Ñ­\x0002ó¶Ì_\x0015lëåw9¿\x001bþz\x0015:þßbUÝüõj2<¦:¢ \x0017?äøa\x0014ß
\x001eÁ\x001aÙÖ«ÔÏjêÝÑüY=¿åÑÆ\x0016`l\x0012Ëê\x0014×h\x001c>½Ñ\x0002v'ïçq»âî<ûõîo÷\x001fw\x000f÷w»çO1ü°\x001dE1xj\x0008ZR»Gj\x0005\x0013ÕÝg?^¾¼zµCqÅÝóÛ\x0018G>?­sl=í\x0003÷ãáX\x0016Ò>\x0015Æ¤±,Õ÷¹\x001ensÛ\x0011î /\x0014Ó©ÀÕ
øpÁZÕ¤Q\x000f·Ï¹ý\x0010wà	~"¥\x00171§H­UåÂ.êc·ÂÌýË\x00188û¦Í¨3xÒ>ê(¯>òCI~\x00189â\x0007{!¹æ£"}Bß\\x000c$Æ\x0019­ÕOOû©\x0008ê¿þã?\x0019k½Â¢OS¤9DéÃ¬¿øÿt»¿J vô³Ð2cÐæ¨\x0001-X\x0018ÂÈ$°§ª&¼\x001d[åØj\x000c[§!\x001f Ø\x0018É\x0017%«eÍ\x000c¶cë\x001c[aC:"Rp¥¨ih®êú¶c\x001cÛ\x000ca[F\x0016I²Dp\x0014R®væ´cÛ\x001cÛa\x001b\x000eO@iÔ±uZ#jñU;¶Ë±Ý\x00186P9ñ4 Ê¦d"ïv}ÚN;¶Ï±ý\x0010¶	i·µMDðeÂºj	h;vÈ±Ã\x0018¶Iq ¬PdDò6\x001b|\x0000§©\x000bR\x0017ûÜÅj÷æîß\x001fïþqÿá°:k«U\x001a×<ÿî=Þ±<8Î\x000fúï¡÷?_¾º½Ü½¹üóÍåÏWÏ÷K©O8½òÃtåï¦V.«è¶jâ¨Úì\x000ejSë\x0011jAÈ6]ÝñPmaï@69²\x0019@Æ\x001a!KB*©FH\x001b¾\x0016;¨6vPÛÚ\x000ePãÜ®xÉ¡)\x0003\x001aÃ&Úk_{Éï v9µë§v6]%hNÁÅ ¥æTµY¨ÚçÔ~Ú$1N)þ©ò<_ÀÕÃ§\x000eêS\x0011êÀÑT\x001b³W¬Ê®«Ùñvê\ú`Ntckr\x00123¶ã+»:
ÈUåú;¨K\x00173àc\x001cÎX'Q)õ\x001e3tÒ÷ªff; e\x0001-û¡­
é\\x0007Ú%¤sí·t1P8F\x0018ð6ZiJ\x0004JÌEQ³dåêz\x001e\x001dØg\x0001×h13Q+âTîMÕ^UGv@\x0017¾\x0011\x0006#ª{HR~¢¨)¹à¸\x0004(Èjx\x0007uá\x001baÀ9bw¤±\x001e¾©iÜL]²ºð0à\x001c±*,ÂyòIø¬¯×v`\x0017Î\x0011\x0006¼#ö\x000fÐKu|\x0016À5^m¹Ûw\x0001÷h¢{¤[z?æQp8/µV½¯f Ú±eá\x001eå{i·u2~àY¨\x001aÉvØ\x0003þÑÌ)¾Y#ÙpÇ#\x000e\x0018%C¢ªó{;°\x000b\x000f)\x0007<¤e2úBÌ70p,æ· rÕÁ\¸G9à\x001e¿¤Éw\x0003ÞÑÄ\x000b#Å"Ê¤i¹À³
ãfW+\x001f;°\x000bO#\x0007<
V\x000cÒ\x0018eR©`ÓÛj®¯\x0003»p5rÄÕ ã¼Û\x0016uDés´,\x001e\x0004bÃ{,\\x001cp5Æ	\x001eY®ä\x0014%h£ëëª\x0007íØª°ÙjÀf£Â#Ýz\x0015¾Ö\x001c%\x000fMó¾Ú.ÐA]Ø>5bû¤á\x0004\x0016vüwq\x0010\x0015Âf\x0019\x0006í3?ö{H
éHÏ¥ñ."íjfµçÞ[Cï¾øË
Iv;.
!ÍöÕF»P*W{©_\x0006\x000e£_
þÂòYIN\x00076¼\x0000r\x0003ðëDä¡<6ÍaÌ\x0012%Õ©j]\x0007æ\x0004>\x001e!z\x0011ø¸K
£\x0014%9{Y\x001d\x0014ÓP;e÷cèZ§q\x0007*\x001ew ¬>¦z6ÜxøÝÆÃ\x0018½\x0014Ç×¬«T\x0012àvÕðð^ª!ú\x0018q'ëîõ±Â\x001frÝÎºÇ{ÄïèÇö>\x0017\x00122\x001ac\x0002Öð$vS}ê¹ßÿîÜ¸1ö/\x0018ß\x001d±SóEÓAîw®Õ
¹Ö/
\x001freÒÉ¹\x001eúÁ£]§)fÊ§\x00064ß1¼Úà!ÔÉØ¸ø\x000bnÝxsxzØ=¿{x¼¿{ZÉ¬b\x0018 ¸Ê]ÏN\x0015\x0007½s;¸%
Á7ûÛëÝóËëøÛóÈ*GV\x0003È Äj¶)H¬BB^jîiCÖ9²îGÆAÝ61;ÞeNbEæ¥\x0016Í6f3Û\x0001fÅº@È¬y9\x0015ú\x001f3á\x0011<Íb\x0000Z§F\x00083ËGEè¥V6èò\x0013\x001cø\x0006c4\x000b¼ÓrîÉÐi.ºÅnï6hY@Ë\x0001è\x0018	Ú\x0004m%AÚ5B/µ5¶A\x0017\x0003\x0006Là\x0019ZñNs9c^h.l\x0007\x000c\x0018\x000fÅsß&hàv©}jqÜX\x001b´) Í\x0000´¤G\x0012åÎ\x0012t2ÒÚ´MÌª8ÒjàH'Åùy\x00168BoæYTa¥ÕVJÐ'èé\x001d\x001e¡er-Õnfhí
wèú¡qþ"Ac\x0015æÌì\x0013rõu=2øÓ!µ^g­\x0015\x001fvo?\x001f>¬Vôs°6Ô¬$¶%LX)«çÊ·ßîÞ¾Û?_ª§ó§Óiý\x0014&u\x0012Ç`t®vX\x000bHÒ$}*¡úôÞ«s\ÝémÚ`-8=rTVâ\OÂzb\x0013^b\x001cáN\x0005­\x000eÂqþ\x0007IµCýñº\x0019ØæÀ¶{Q,pz&jâ§ríx]ÎëúO°Ç°b>ÂUü©\x0016>\x001eás
\x0013kyA\x00176\x0002ì%ÆBxMÄÀâ\x001a2ÍX°Ý(Änç¿øº·\x001a±ódÁ¿øZ±?åëÅ±=ûOw»?\x001d\x001eÿõÏÕ]å\x0010\x0008
gTÀ\x0003¢á§\x0003ík·ª¹¹ðOûW»?íoo\x0016Ç\x0010¶Ì±å\x0008v¼Wqî=\x0006\x001c<1Ük.­4UuÛ\x000elc«¡ÝV\\x0006\x001f=t\x0012¹s2=\x0019T#\x000elcë\x0011ìè\x000cÓ!±¬%\x001cWÃsfKlcÁ³-
Uh{Öµ56ìªÞw\x0007¶Í±íÐn\x001fg×Î"`³ÐHg»·ëÀv9¶\x001bÁ>Ö\x0006@TæÝ¶ÄfûÚP\x001f§(â[\x0012½ÆXHö¯:ë¯:Ë*¡Õ\x0016#ØØÌØ\x000b1¬b1½Ý\x0019ÒÛ¹\x001bÉÜØÂBéJëDuê[\x0007wa·aÈpËT¯\x0003ñêEEñæ8ÓTT\x0013¦\x001dÜ\x0005!\x0013\x0018¹i\x0006\ü\x001f¾ÆdÜõ\M\x0007wa\x0002aÈ\x0006ÆM\x000ed\x0003Áaõ,hw\x001cî»å~\x00176\x0010`¼+ÒD8)ÒD8+4oY}ÜmæÖ¦àÆ\x001fÇ"\x0013\x0006WI\x0003>Þ$yÃMuêTÏA)&cÌ\x00053`Æ
v\x0005qP\x001aÓæ½+½a¢NñÕ =$×)Qëö]¬¶dõxÎSv?È®M*gA9Å´<Q\x0008ÕÚbÃSz3ºóÑ®³}tI~'\x001clxûß\x001d\x001b\x0018>7_"ÀIV\x0010\x0003¡ã/¾â¢\Öf÷ìápÿx·{~÷ûÕ³ÂñÕcÖ\x0017Ô2©Ü:ÏÙb±ÌOÊ6Ï®÷W7(qöóÕõõ¢>Ï¼\x0012[®Än²xá§ù\x0002:\x001a#zlÿátµ\x0013çn¤=k_Ë×2ý¼ÉEÐß$uÒ±5\x0012²ú\x0002?´\x000e²\x000e¿É:,\x000cK1$?ä\x001c7ËO¹?`-ád-aµ\x0018jNkQéSq4ï\x001dgÍ.D}ÉÊ§Å(±Íb4OnÑR²DK¯D¢®Ë=´\x00188Y\x000cl³\x0018Á"©\x001a\x00022ëÓ\x001fF¬7l]<YÜÆyz÷ÀÚ\x0004z§qkÎ\x0005T{ÉÖ¢NÖ¢¶YK\x000cL2dV§ÅØ?Â)}²\x0018½Íb4
è\x0018«;^\x000c»ºÒÔÐZÌÉZ¶ñúÚ§?|vFò\x0017cª
ñC±'ÙÆñk{\LÒ\x0001÷%
ãbÿÅ8~µã×*2ñ'»¬]Z]¥\x0015Úº\x0013ï¯¶ñþ\x001a°×g^L\x0012®tZ§ÅTg÷
-æÄý«mÜ¿bu¨¸\x0018MÍ@NsM¨öA,E8½óWôçµ\x0006Îo;®\x0014z\x001cmëRN\¿ÞÆõ+}ÁàöT§U®ëº
­åÄõëm\¿\x0002.Ñ
§#Æ)\x0014±Nå¸u)'_oáùM\x0008ÇahçØ&[ÏÝ-ÂÁ¦_Xyò,õ¼\x001fî\x001eîÿÏîÅáññþ¯V$Y\x0017zR­
üRè\x0005?¹\x0019_UaWðÃåõÕÿÜ½ØßÜ\½x½TJEè2GCè¨\x0015¨YqW°Ýõ\x0010\x0012û¦ä*'WnhbA·NR
.ðå\x0017KÅ6e×9»\x001eÜõ$\x001f(T\x001a±ë%+;\x0019·ñ¾Ýí»\x000fø6Á\x001aÍôÀì\x0002?SúpÆ>v³Û±}5YÞ\x0012 ^±Ú¤qÕè>v³»±}w\x001c\x001bôd6?&HPUiSv³ûÁ}×é[Å¡öÛ[®j\x001d÷±=í»õ¬Z Li\x0012«*B6dÏ\x0007©Êìå¹óc\x0005¾ðàÈcjðv\{ª:ófÞ
_zÕA·jeòM*ù&\x001e[«ªöÁ\x0017~\x0015Æ\x001cëävÞÐ;\x000b\«`TØ\x001dNc\x0002i°ÍÓîÙáñáþsÃ]>ê
\x0007kÎÁLÈÊ.Ïß{~»{¶¿¹¾zwUç¬úëfµ9«ýºY]Îê¾rÖâmâÅ_|È6Þ\x0018\x0002·M¾8üòx÷°ûáðô¸úò\x0006\\x0010¤£çãô@z\x0015¦Z®À/ößÇ\x001f®w?àSàyhCË\x0011hÁsÑ°×O]ü·ÍÛ\x001c´\jCl¤V9µ\x001a ïüÆqI,ï$LµÔ \x0003ZçÐz\x0000:HÔ´¥tRîq
fãVW}G\x0007µÉ©Í\x0000µZ§½\x0016IÚÎ9V?\x0014¢:ú§ÚæÔ¶\x001ah£¹ÑÅ:RHR(Sµ\x001d±ËÝÀ>cK\x001c\x000eïÓ=Àówâ=Aû\x001cÚ\x000fl³aµÆ\x0008
ÇÙ¾·ºwï\x000e9t\x00189ÑîÂÏ!\x001cJQi>Ñ¿C·8æ¼:\x000fûCjcîÚkí¸a<
\mIê&nùâì¹FêÒ'8E/iø³Â3ÎæPu
¶ªÜÐA]8Eè÷S
!gúáª\x001e+ÓëØò°íFìÂÁ@¿°©ñ\x00134c³¤¨¦\x0012:¨\x000bS
#¶úKR\x0017\x000fL_HGÄ¸D­Y\x0001IÔ\x001b2Ú±eaEä\x0015Æ/ÕH\x0005Î\x001cXJXÌbop#v\x0019¥|>PÎ`*í¢¢uë]Û\x0019?Y|r(â©Ã¤)86°,°ÐU¯\x000eìâý\x001f$v¬R÷Ëô¤Æ!\x001f¤GÛz£\x0003»ø"eÿ\x0017iãÑe;\x0012}8güEb\x0008±\x0015¶*¾HÕÿEb¡.\x0017È)¬õsT¼\x0010\x001d;læk°Ç»°Ú#]h®\x001bEÅCÁ×\x0019
X}¨¾ïu`«\x0012{äê(ø­@KLòFÉª°á}\x0006;¿\x000bî![Â#@5*þsñ\x0000>&b»¨\x0015Åe
î\x0011?éBºõc;KÜJ%mØ®<&®ÿÄ \x0004Ð^Ï60^\x00124GÇ²Íîc8ëºJF¾JËÃ©âåÆ\x001c¯ëÇ\x001bÙvY(ìÕ.¸GwôÊ\x0005Pp<ÕnsJGÍ>K§s?\x000e\x0013Åù3,pâ.@y¬	Ú,xu¦\x0008§ðÇ\x0004äg\x000c\x0013\x0017ÈH\x001e¨-Tµ	°\x001bÜé80g8Ã:ÕüOï]¹Ó\x0006\x0002,yaøÄSA;­LµÑ\x0002§jÝÍëg?Ç9®ìÅµ²×ÚáC\x0011IÐ\x001båwéâÛkr\Ó«

¥Â©\x000f\ì\x0002K(×Kvº×ç¼¾7ø\x000bP´½1ú aÅ$[¬ªU"m¸A\x0016§!ÈîóCáhcL­HI§(¨ºø	ðûÃÃo\x001f\x00173ýJB>ô2k,¨7Ùs\x000b(ÓiÉª]\x0016êÄDà-iÞãÇýóý¯ÝõÝû»Ç÷+±qÒ!ÕiãäqHs%\x0019[V»÷\x0011ûåþæòÙûëÝõå³ëËgçáe\x000e/\x0007á}*ÌvX¢@S
·Ý*µxÕmW9¼\x001awÜE9í<
CéSÞy½\x0014¤¶Ãë\x001c^\x000fÂ\x001aq{HpFNÚømÙMÎnÆØ\x0010d]=öô§bú\x001c>t£ÛQtCó»§mçÎ[\x000e´Úö¸»\x001cÝ
¢kqüVS¢ÄB²3âíì>g÷ìÊrÀG\x0006Xâ$ÅSõÆ¼>øÃAxÃE¢\x0005¼!Á/%Öá¡tOþ	ó|f¨ÝÙ\x001aÕ¼\x001dº>
¾u
¾?Üý¶»¹ûøùþîqm£³GUè¹É\x001ck\x0006è¢£Mª(®O¯ê1.ßîn._½»º¼YêsÖ§\x0011¸N\x0011x\x000fsÒ+Ì©¦U[CÉîÉ«nÅ¬rf5°ÏU \x0004ð@[\x001ebLU¯\x001dXçÀz`µb¼IkÚª¼OkC69²\x0019Øcê´Q§QÑ6óü\x0007c\x0016÷ÚmÎl\x0007\x0003Ë±àå´\x001aµå\x001b;OnÆìrf×Ï,4+xbï\x0014éQaK{ª±Ýîl9\x000c0{Ê³\x0018¸r~Xk\x0016Ñ2¾Ú±ÚÌ\x000c¥m\x001e0ÎÂ]x2\x001aN¤ÒÅäñf¼\x0019taè ßÒ9\x001f.fO\x0018¡càG_a«jS~mÐÅ#
,Slâlæ\x0006Ùt,ç[ ñM67wzÀx(I:¯\x0002Â<ç|bæo+hWiü±«EòÞs¼7\x001fêTkí\x0017_<Ú¨KÏâF|K\x0012|E¹\x0008ÊSêÔ\x001c£¿í¨CI=`õÀ%ï\x0012-µ¡\x0013\x0012ïÄl©\x00173=mº\x001c)4E¥©F¸Ï`\x001bj\Â
V
@tìfÇäTbw
BFÐcPê]òéìkxô1ÕÖÕ\x000e÷xJ\x001eÆ6=ã·I]·Zs§jü67\x0008TÅém@d·ÝÃ!ÞÀþ±ö¥Æ9Ç2¨\x001fèè\x000bn\x0014vb1eüürw½×¯Û\x001e<Äé]@dwvâ\x0018°&ÅnÚåbJ¾	XçÀº\x001bØsÙ\ÜbÁ\x00135\x001c%\x001aÅò©h ¶9±í'V\x0017~6\x001eà\x0014'\x00124ðmÜÅúÄ&b\x0013»¯ýP,Oñôs/s4Ñä] X´PR²4 ,&ä×AÃéC\x0002L\x000f	<¹\x000b'RüéÓÓûCÃ\x0018=~`§\x0017\x0000½Ø¤ª¶©ñì.Jñ§×·Ï®÷ç¹eÎ-\x0007¸½\x0006ÂLmU
@<ç­¯\x0016
÷pë[pKE\x0000Ñ£P9Qü\x0000i»­«Ö÷`»\x001cÛ
`[\x001dx\x0012fôIà?McÄá \x001br;pÇíÖÇ|\x0002å®¥t)°é1å4C<âù4ÃSî.\x0004yóxã¥Ó\x0012OK¨¾x4ÑKwbT0¼L\x001dxo\x001e\x000fw\x001fþë?þsÿ0¯nUÓ´\x0017ÊÅQV"$ñ\x0015¨ª|PcÛý»ÝóÝþúû«¥èØeÎ.ÇØ¥ä$T¼\x0005®\x000f\x001b¾ÅäH+»ÊÙÕ »Ð\@gbÜM9 ù¡	âumKv³ëÑ}·üÞaDJX¤2\x001a#¬Åä_+»ÉÙÍ·uÞmÎn\x0007ÙQ\x0001ö]*ÖI
«L\x00006Ew9º\x001bD7îñ*Ìë½ç·IqæBßîst?\x001e¯gZÿîK Óz¦õ·=äìa]ñ3Ö6±ûc\x0011º­êêõ°\x001fÛË&Ï$F?ÕcOKp|\x000bïo",6\x00037ÃnuØ¯BêZ@\x0015l¶3pTÝÒFBáWaÐ±N!/;Öø/ùsMÇ\x0006¥=6/\x0013\x000cz'@µzªÝÅqê\x0004oR]~æi/,<x©}\i°N \x0019Þ-
\x0014\x0012F-¥Êä\x00155wsyÉ+nùÁÊÂÚÈQk\x0013·;Ø¤Ùë\x0014ùTò-\x0017«Ú?Øâ
2´6Eïwûß|´ö\x000fùhOÏSd6Ìÿ3áNG;]¤üîåá~m2	¥wi¢Þ<»wJ&\x0001åeL\x000c\x0013ÎXøß¶¿:ÏªrVÕÅj£Ú6,hã¤\x000c.M\Î9¯fÕ9«îd\x0015,åPOmFõô\x0002\x0014Q\x0017{\x0015×£\x001cÕô¡by&\x0005É%Ò¥\x0013à\x0016'z¯Gµ9ªíCuYY
÷\x0011IË»êß¸W£º\x001cÕõ¡b\x0000EÛ*hO
M³2`Ý\x0019c¼\x0012Ôç ¾\x000fÔLÕ\x00023(W\x001cIC¥ôqO\x0017\x000bu×£\x001c5ô¡F¯<;èø}¥j\x0012©$o«	°f2\x0013hXE7,Éù9¬'N°ü]-o_ÏZ:>/`cØFÕú4,I
þ®ê³ZXqPvÎj:Më±<Çä\x0006xÀ]=5[\x0007ëàØù1áF3xès±$Èc\x000c?Ç³5ìa«óGVòZ8\x0006,ä¥©?|úøùðñîáánm\x001cíT5\x0019k\x0012MW¬¢zagÞ£xýêÝþÕåõõâ\x001c!"9¹\x001c 7Á³Ü»QÝîQÁ3O¦à*\x0007WC[îì¿@\x0015¯!Às*<Ý=0þÝ\çäzlËST[ÎÓ=S)sÜósgMä6'·C{\x001eÏ¶%ð¶\8`ðMOy®]\x0004G§ÒGÊæGtÇ\x0012J'ô
OÌæ7â\x0007
fè¼\x0004ïc\x0013;¾\x0004MÛ¾ìÃOÐ«ý{3ºÑ>GÇ\x001fG¶Ý\x000b«'¶\x001dÿS{¶ý\x000c{ÜçÌ\x0003ÑÆ\x001fvÞPþ}ÚyîÂÇ.Þùs\x0005üM_*üåÒ%ý2²÷1Þ\x0017dÙ±úL{PÉ@+©k`ÑByN^âÕszÜL'HîÉçÝ7Õ	 »(wàè`!q28NsK×ó®:F©	\x001eÂiÝIêN®þö÷Ão¿Ýí~¾{üp?Í·_Ut\x001a6\x0008§üna\x0000T»at¨^½|³ûör÷óåÍó«ËóÀ2\x0007ÝÀ\x001a\x0012pÒe\x0012\x0006oEàê]¬\x0019XåÀª\x001b\x0018\x0002Å[³q¿JAÓu\x0010¸fQu\x000e¬»lèt¦Éé§\x0001FW\x001dÍÀ&\x00076½Àøt\x0014\x0017¸é\x0003;U×Ëi\x0006¶9°í\x0006ö¼Ì¤vJ¯ëB\x0006ÞáP\x001d\x001fÐLìrb×MìXXl:Ät¡\x0014 Ä[\x0001û\x001cØ÷\x0003s1Ý$¼ïé\x0010KÀÕfâ\x0013^b¼³KKÄÀv\x0002\x001c	#Gb±Í\x001e<ñ\x001døs·q\x0003\x0004<	\x0001è°2ãêºõÐâ´&J¸Üá}xÚ½üôôpÿq÷êîéßVû=¶\x0019ÑÙñà\x0014HÇ#ºðÚ¹ßî^¾¾½¾zµ{uyûÃy|ãËQ|	9ü\x0016õg§BåðÈÎæµò«_
òÇhhN¨Oø¤'8÷\x0001ÔVôp2¥	åÑ)óó&^-îV\x001eõéBIR\x0013\x0012]:ÅwV\x0014>;/Äw\x0011ûÝåíÒ1?\x001dÀ\x0000Ç\x0001\x000c¤hIH(O¹4X$R³Øi¿Tå¤ªT+ÙµåÀ9¨Uùú\x0018ô&Rê.RéYU\x000eÍSGãÉ3êL¾o5©ÉIM\x0017©ñ\Ì\x0004>$}Ç °(´µ\x001aÔæ ¶\x000bÔ\x0001¥P5X\x001c©7qz>¥.,
Ç\x0005\x0015óÿÊr¾ØÂ\x001cA?=}¾ß­\x001fïÿúñ°VDÁ kcHz`.½\x0000,¨}¾¾}woÖ7W/^í\x0017$\x0014Y\x0019K ¾\x0005hW@»~h­\x0002~`Ók@Ps¯	Á"ºn¿Z¡C\x0001\x001dú¡QøútQÊq2e&^K©å$º´ú{f#´)\x00198\x001e_\x000c\x001a*¿Cü¹ÿT\x000bÅØ\x0006Ål)èT\x0014t
U\x0002ÐF-³G\x0000¤Æ¨
A»\x0007°\x001cô`3ã&ÔØ'^\x001c\x0010ü¹ÿc\x000cÌh³Ù\x0000êv5¨à3
ê4ÂWSÿÓÓá\x001eãËïß¸ûí·O«E#\x0019	3\x0007\x0019\x000cD ôy¼\x001bÖÎÇO·û+-¾zöüòíÛ×Ky8u\x001a×«)®ïVÞl#¨ãþ\x0018í¹ÃUÛj]`\x0007µÊ©Õ\x00085×pÄûi5µc¡tmªT\x001dÔ:§Ö\x0003ÔÒÆ\x0008c\x0016G\x000cçùhÇ=Tõ*Æ\x000ehC\x0001hðÔ\x0002\x001doOS\x0007rh-«Jú\x001dÔ6§¶\x0003Ô\x0018×ªò|S=*¨PÕ[ë v9µë§FOê;B\x001d\x001cn7WÜ\x0011 \5\x0004i \x0016Z¨Z\x001cË\x0012°éõùáéñðaµÈn°4¥*x\x0013\x001dù\[)¸U×¨\x0015ÝÐÏ÷·7ûç\x000b/o\x0004-shÙ\x000f
B²4JwÓ±ö ×F.×C\x0017Ôg·ZåÔjZÍÍ£\x00134\x000f"\x0015Ie¹o¡YçÌz\x001f7#´b)\x0019\x000f<!ÛÀ\x0019ý&êBtc>ØÇÇÁ³íIp\x0012Ï¶äÙØ©ëUU³£-ìÒ|ñ?>Èg¿\x001e\x001e\x001fîþvøëÇõ£O4!\x001e;¢h.æ\x0001}Z-ªÁ=ûqs}ùrÿâÕ
b\x0013Ë~bO7/B\x00054=ÉjÏ\x001aõ·fb\x0013«oauN¬»\x001d\x001c]N¯ô§¼+·(¨ÐDlrbó-ì±Ímÿ\x001e\x000bÖ¼ÌFaæ¼Çõ^ófb\x0013»oaCN\x001c¾fb\x0010'u à(ÖýðËÝÊ[lt}³UÃ!ZÜ.\x0006<3\x00015Ê\x0016H_î¯¿¿\l=)ÑDHÙ\x0003	Tý2¹gJ1{iX\x0012kÉ,¬T9¤ê\x0014i\x001e5Nê¤p
Ò0me9Ùu&ç4]cak¹ÈËô7_VYérL×ù7·\x0014YÏ¥¡þ(ú\x0002f)]¿3ä¡S\x0006\x0016Íf#Sì¨Ó\x0000x¹ØÞ½z?³iO9hlÃÅy0ÿ1\x001fÎüâ³¸æäm\x0001ÍºËÞ\x001e~9<~þõîÿ6<ÙÐü\x0000á\x0018s<jÓA=58×¿¿Ý¿¿y÷ãåÿ:Ï,sfÙÏ,ÇZÅ0<Íý\x00114n$2ë4k`V9³êgVêj5\x0016\x0008ÚgV-Unyòc\x001b³ÎõÀ>Ou×3³IãÃDK#óâ´¶6f3~f\x0006{OÌÆ¥a?@EzÊÅ©\x000cmÌ6g¶½ÌS8#iµ¾°kôé\x001b´~q\x000cF\x001b³Ë]?s\x0010ì<\x0004Ê\x0013qÁ/\x0019åÈ¼,½YÚ:q´u/þõÏÇÃãÝåoÿûéþñÓÃÚ7\x0005Ô´Õé9½JÆÅ8&_,öû¼¸¼Ùß<ß]¾ýéöêæõõyt£Ûo
Ýçèþ@\x00078
Ú!\x0005í?Þ=~zzø¼ö|c¬9\x0017\x0008èp¡h¸\x000bÎUkË÷ÇË×·×ïÎsÊSvqJC;V3Q\x0015\x000bf¬\x0008t±î~5§Ê9U\x0017§\Â\x0002Ø2Môvì³ÕRzg5©ÎIu\x0017é±Eà;U&IÐ²mBjrRÓEeódàJBk}]½ú¸Ôå¤®4ð`LÆÐ\x000b.aZxÈ]\x0003*üÉ#.Î\x0007MvO\x000f»ëÃ¿ýÛ§+iqf;?,b÷=u&8
!´\\x001e\x001b=í]ïÀóÈ2GýÈ*pØc½å\x0016a§¨p^/\x000f¸iCV9²êGß\x0019Eñ\x000eåê¸§Ýb³V\x001b±Îu?ñQ\x00110¾<âÚá#\x00111/ÞìÚMÎlú5U»jºzT9\x0014dXìsoC¶9²íGu.ffÍÊ\<l9"/Úß6d#»\x0001dÇÚD12ÀÒÂ\x0019û\ônmÌ>göýÌB³h\x001e6¾§=ÎSjûÕzdpÓ\x0000ñLü\x000cûëåW8§ñéñ°Ö3äð\x0005?\x0015_¡\x0013¤Ôº\x0011¾~ëpNãíÍþ\x001c1Ä\x001f
bü¹Y\x0008nÀ6øÄ\x0015&hÃ3¡±b¬jèÚ !¸rë¶æ\x001b\x001b\x0003Ìé1.î´Ien¡imù\x0004ÚðÝôs/4
kÑN{9Û
\x0013xZ\x0011¦®PÕ¼ÑE®7{J\x0017ö ë`ÒH
,Z¡C¢\x0002)X\x001aiêJ«Ùýé4oÊw\x001ajÒ\x001d%9
6Î¦4\x000bK9Ø3ÃÆðIüÝëÅbo:\x0010Á\x000cDhÁÍ\x0006\x0019VPvhæì\x0019½§\x0006\ãªnÜ@%<µ\x00189S¸|\x0006³ÜN½×ä¼¦\x00173@¬\x000b.R×òiöÕ±$ëyËy*Þü®´£\x0005[©4IÊ(.uIªßÅ¶5Øñ^v\x0012*edýzø|wxBôëÃß>}þuuI
\x000e9²é@s§ä\x0017Ðx¢Ï¤ý¸w¹¿Wñòõ»\x001f^oi\x0015&_ùÖV\x0001pZ
Ðöýû©ý^íÞÞÝÿõãÝÓÚ\x00011Sû:Ý\x0017µö8±b~Cá\x0017\x001f±\ºÂWÏ¦.üøß}yõâÕåíâ¨\x00188­HBt»{\x001dFôà\x0008tNzyEeÀ*ÔÛ@GÖaòu-þ\x001eÑûSwÆÎ\x0013ºYô÷PÕ\x001eçuØ|\x001dv¿\x0004
h°2/oX"Ló=ëpù:Ü&ç*)GÀÙ\x001fÔåæsõ\x0007,#»s@)¸<ð÷H\x0019\x000båEú{\x0018zØ³ªË-\x000b\x0011§CmE9Ôöòý§\x0006\x0010¬aôÿM\x0011#Wx+b|»»|özYÚät ­(\x0007Ú6ñb6_ÑC\x001aºå¥N¼g%MÖòªWõòJÅï»ÁùT¢\x0014@çf\x0015­çÕ9¯îæMIà=éJz&¬ª³3ðÖâ\x001c×t\x001fjU¢k¢\x000eh/S)\x0017SÝëyÕq\x0010åt\x001còA\x001bÌ%ÃÓÔ­y{M*,_6y
Û{Rë|:`°Y¤Ö\x0010<Çñ\x001exäÑgG«Å§}\x0007Rdå+Ï°÷aíd)U¨
]<<{\x0016\x001bl\x001aÍ·øN\x0001$öò^/ÍÅab\x0013ËoXåÄªX[
C$æ[\x0016TÎµx[\x0011ëX\x000b{lsbû-\x0010ûØw\x0013Kwô\x001fiô«cõ.´pgF	¬$\x0006llÉm\x0005þÜ½Í\x00028#¤á\x0011\x00026pÇ 97\x0015é<3¸Ó~RçÊ,ÛÛÃßï?Þß=®¾$³0VV âÍ|¹¤\x0007þ`ýùLÛÛý«WW7KcwÚRê\nkæV@³j5öz\x000bN
i&7¯eÍä*'WCäÚòt\x0015$I\x001a$$òóÍJ
ä&'7Cä2UY 40Ê:ÉïìA-ËZ·»Ü
£Æ\x0002O TÂã¸»ùÓÔ¼çpFxt%¹\x0008\x0012oÙÃ\x001fÖgãÏß=ûõîo÷\x001fw×ÿ÷ðñ°²²ÉJ¡f1'%\x0018¦\x0008á¿2UMÀg?^¾¼z\x0015±ÿý«ýRMÓ©4Ì\x0002Òo\x001e\x000eïñáþãçÝËû÷¿Þ­E\x0006%Ètè¿RG§l¸®us½/
W¯Þí^^Å\x0015¬à9·\x001câV4Ô.rË,\x001dÂYñº6G\x000f·Ê¹Õ\x0010·%\x0015Æ\x0018U»Ô°n²º:X­\x0007[çØz\x0008Û\x001d±Sv\x001c\x001f,ùXõ<=Ü&ç6CÜáÈ-\x0013í¦f½¸¥=9ÞÒ#'?üë\x000fwk\x001f/½4W*\x0007y¡fË=ÍÝ¨Ãd¢\x0016sKØ_z}¹ô\x0002HÈ*GVÝÈ!)\x0019\x0018å\x000e½ñIÎÝ\x000b\x0001×#ë\x001cY÷#G»¡fs­¥`E\x0000c¸è!?\x0019^lrdÓ0¢ÉHÈ_ZæB© ïä-È>Göý»3Òæ¡qh¤âY>\x001aärÌº
ÙÛÓ×ì¢
æóáÃ\x001c êÌ¿c­âú¸Õáç7½\x001e`\x0014L±ÝfY,W¶¿ôSH²Ûÿ\x0019K\x0017")jF|Ñ\x001aó­­CåëPßî:t¾\x000eý­®\x0003l(¾\x000f\x001b6X	>ÕÇ*|KCu/Ó³?×úÑ°\x0010áNç§¸TÒÿâðøxÿ×OOk¹Ar?\x0013Î£.W\x0013ø^çüâÜ§\x0017û«\x0017¯oÏ³ÊUö±:Ã\x0017&V#Ð\x0003Lìø­É-È£­cÕ°Ê^kÔw*Åçñ@Ø½<<þ\x0016ÿ¯+©]<\x0019ôB1#E1Z¦ÞGU\x0015'c¯x8ð¿vóvþ¯]Æ\x0007)u?ý<¶\x0000'XêÃI|´øEª\x0008©·îöðãßl\x000e@\AüÅw±\x0015\x0018\x001eÎd\x001a­x¶\x001d*m³\x0002\x0013Á\x0012\x0000_h#ßý¶\x000bÁQ\x0006«¥¼K4	çÛrHUB()ó^¾ÝÅUà ÅùöÔ¢Ø<E\x0017íá\x001e?¯¶Âs§´¥m08í·óç$v?¾¾y·h\x0001í©U±yj®7Z¹XKb\x0007ór{º«Þþ[u\x000e¬¿b`8}ââçÍ§x\x0007ýùþîéÿ¬¾\x0019\x0005D\x0003JrA\x0010ÆÅT\x001diÎMB|ó:^A¾º¼ýç©UN­\x0006¨-P*\x000b°YZÉ\x0014o³µgË4\x001a u\x000e­\x0007 ±;vÚsnÅ\x0002+xY[Õ[ì¶9´\x001dÙi­zóVÔ¸EÍÖU\x0013\x0014\x001dÌ.gv\x0003ÌÑ\x001fz fÏEUVóuç\x001a~×PpjÃd/ûûÃá#G¬Ýõý/ØúùþÓÇµá·OSó&Ù}.Òsä\x0017m½Hïòmt*¯8dÝï®¯¾¿¼Ù¿»zýêüBd¾\x0010¹ÉBppý¼\x000e©YµÃÙTymªâ\x0007#ëÈç\x0015MÃ\x0016KqÇ\x001b£je½p£É©}½]k\x0001ü$ÔñNSßðGNýÇu|õû\x000f>þõií½NB\x0012çÇf\Ê7¢V;\x0007\Õbmz\x0002+ø\x001e«ø¯_¿zq»äWaz\x000fÕ.ç~\x001e[\x0004VÂ\x000fÇÑÞÓó\x001c\x0005íÕ\x000cSó\x0002N+ÚÀ\x001c2:ÞsQá!í<\x000fsSùÖn
uW<BÃiU\x001bïä\x00083°\x000cöÓ÷«\x001dCWó¼\x001dÐ:Ö\x0003ÐÚ_ð\x0011w<Çiî¦ÝÌ6g¶#Ì\x000f¬lëÅÌ-Ða.6\x0015GãèòÄÏ?½Ç±\x0004»ëOO÷ñ:ôëýÃýßÿ¾6ðuÖ^\x0000½\x001a
YÓ\x0008\x0004×cå\x001aÈÛÝó×ÏpRÁîúõíU¼\x001aýxu}õæÍâëè¼\x001c_,Ço³\x001c\x001c\x0007L'\x001fg\x0003P_§¢nu-[Q{W\x0003¨,¯fR\x001aÝäÏ#=eæñÊB\x0001ÊJú\nj_2'\x00030° 0\x001b\x0005öæîß\x001fïþqÿaíëµqÀºð\x0010\x001c?)Éj\x000eª1\x001d_¹ß\þùæòç«çK/Øírl7­\x0002¿<IaøMDÀÜ²fêáö9·ÿf¶Ûæ¡óIÁ_|#ôþÞ\x000bôÑåD\x000bÑY¹¶W\x0003)¸ú+þÓìyæÆrp.ùq>ÅNÐ:Ö#Ð\x0012·|¿
6!³\x0005Tk©´95þØÍ=ÔPÒ]Æû\x00089\ËD¡8ûZîº9sg7*"? +ÖºÊ'ùdÉE\x001e'Ù\x000eo¹Á\x0010ÍÈLË|?f#>â­°AÉÕÅÊÀ)J\x0013iT6R4S×/¢	\x001fñ"8	¹Ö÷ u	­\x0007 ?VD\x000b\x0014ÈðµUsæúìV»Ú
P{\x001a;¨ãÕwZa¬GÐuÑÄµÐ ÃÉ\x000cÙý\x000e\x001f\x0004¢Õþx×4yN:i6µû¤ôhª¯`\x0014Äã@4Û¯.\x0017ç\x001a\x0013·Ì¹å7Ã}¼}Lû-¾~p¡¦ÇG8n´µÇìä³O\x000f\x000f\x0013ÔJß\x001e¤cåT¤h\x0012h<Úçªz½¾¾Æ\x001fëFd\x0006Î,_\x0004Ð\x000bl½Ä²	X\x0001?Nf/u¨Ö\x001féZU\x0001¬º-PÆZã{\x0017	ÜH'Ò¬EQ\x0016bS\x0010nb£¹Ü\x0002«¾\x0008Ø²Ô½Öþ\×
\x00019Ä¦<\x0013fàPôûÂ-\x0006\x000c\x0019óÏn
!{?¼ÉýÍÐð0Õ\x0018Uó.ûñ/ïtæ¼gÎ\x0013ðõá\x001fîW\x000b>X\x001eÎ½º©\x0004Ç\x000b¡SÕR\Â½ÞÿüújIïÁú©ìæHâ\x001dXü=\x0006sÿ@íÌ\x0017_\x001eïï\x001ev?\x001cÖ\x0017ö\x000b¸Sxç<8!9¼\x000bU©ï1¦û\x0019õ3_ì¿¿ºÞý°¿½ÉvÿÅé\x001aT¹\x00065¾\x0006qé´ ¹)M
¢Z¾Ý½\x0004].Ao±yú_\ã._'¨Ü_UGw¯À+ð+0Á\x000bV*SfzWëX32ØjWNï\x001a\yÜèA®i,·d\x0011,7¹h¡«âT½Kðå÷ìÇ¿g\x001bÒÁ¥\x0000ç\x0002·»øªúZ÷\x001aÊÁ\x000cXFè\x0007¸\x0005Ðð;ö$¼°é\x001a.\x0012þ8|\x000cÏ«Fé\x0016ÇgÉ¥³T½\x0015õ®ÁÈb
8Zcðï %Ëhe9npR&¹ê\x001cæ58yÇé&ñkØÿãîãSç@v\x0017cK5W\x0016\x0018-R\x001eÝyõ«K'ì¾|uû»ìgéeN/\x0007é¤¨Í\x0018¼1Ñ½Z+«jÍtÂ«\x001c^
Â£dÞ\bb
%=\x0013BUÑ¤ÞæôvÞ:Í}\x0006Ækn¾G\x0008£OØÞåônÞ*Ê"ÅÈ\x001f8c'MÚ{_ÍØuÒûÞÓ¹ZÌ$,Ñ×\x001b\x001f;éCN\x001f\x0006éMê··Ê¡¦èD¯I­Å¨Fr}ôY\x0006
¦\x0018Ä\x0007àï \x0015>@ ÷/\x0003®ÚJÐ\x000fP\x001eéç¡\x0005 ¨jÏbçØ|\x0013\x0000ky4¼®ªÏ´ò{õ6\x00085·A\x001cñ§NÕá3·6á@Ö\x000bz Ài\x0000ô°Qu\x0004º\x001fªÈ¹J)þ5	y?Uù`Òýç»]cÏÔT:«Q¼Úq\x000f>w\x0011Ä\x001d¯ö\½»üýcF\x00056å@&XL|Í°ªU_7¬)`Í×
k\x000bXûuÃú\x0002ÖÕ°Jä°ñ§\x000eXT¾p4/"xnü·ÜQ¤ª\x001aÃm¨²@_3ª.Põ×Z|ZªëÓúB¨º8«ºë¬~±\x000fK\x0017§UwÖ/\x0007[x.Ýå¹¾Ô!(>-Ýõi}¹}-¬îr²_j_\x000b; ¿n\x0017k
K`¾f¯e\x0008ÖtE°_
µ¸\x0019®A¼³§Yº`]J|4\x000b»¢7µÅ¾ÚÞ}5¤/¯ÁÛ\x0004«©h^y±Íyµ}µöÕú\x000bÒþ7òÔ(eùÈK¨ö4Á\x0016FËv\x001a-7\x0015yL\x000fZp\x001c!æHÜQyU\x001dñÙ\x0004\x001b
w.¯¹<O	ÁoW,'WoÍn!P\x001cXü±\x000b5(®£A)u\x0016Rå,¨e	ÚPeÚ\x0019¼üñ¨ Eá¶¦û+\¡\x0013à°ízþ¶ \x001djÞn%îÔ5éK¸Ø5©\x001cÑ>ÜíÞüzx8|üís(£\x00061\x0015HïÞ(5A×'æëËÝ\x001f÷×ûWoß].<ÍÌè\x0000BçèÓÏ#ì(Lªgv­Ò;¥äGûIÔg\x001cþ¸GÅóÀ÷ñ\x0017ø<ðìðwê.|vøåðñ#Ö~7¼mÌÛn±ôô'\x0015+£RõhïßP[á³ý÷ûW¯°üû\x000c; UÏØ§Gð½\x0007\x0011Ow¸ ­\x0012 G=
zÛÐk,G\x0006å\x0013=ªFÆ\x001f¿ûá¯³üÚÝî§§ûÏñÐÜ¯®d\x0012:õu
¸òÓÜ*,«>?¼å×.w?Ý^½gæê,º6GÇ\x001fGÐ¡Ì´À2jz\x0010\x0013¬ÕçjG¦\x0007Üè\x0002\x001c§JöÇ/g\x0006AééA\x0006<pW¹©¾Æw±Ý\x000c±Ç`\x00144´Æ\x0007É	=µê9SíÍèAO!é1éÀy\x001e¤\x001eðVEÏ¿Ò\x000bÚvcª£zØ}ydüÐQ\x001eGª8 \x001fÞ%ÔO­Ñ[¡ÛiÐñÇ¡ÏÔ_ÌïÖ\x0012à]ù:Uªè"\x000f%y\x0018:ëNò»TÓÙ\x000e»áÒ_§Õìåa·]I\x0012F6ñ®Ä.U¦\x0016Îh6<ì6]Ç]
±CòI¨ÙëéC¥\x00194ÚU{ÜÛÈíÔ¢âÇïã/¾~þîúðo§Ý§µÊ7Ó\x000ezçÅ'_Ï±9=úàëý\x000f7ûÛÝûÛw\x000b´ dQRò}ü\x0005IÝÞ\x001aÞÜ?üº^¾)úzÒ05Vò|\\x0015­\x0016ñêj=Æë¸ÅS\x001bÒ«ë\x001fÿêÞ5¹#É\x0012Þ
V\x0000÷Ãø\x000b¤P,Q¤\x0006$Ë¦û\x000c\x0014!*@¢J¥_³YB¯£w2+ùâx¸Gf÷"#2¥>³aVQÓª87\x001e'Ü=Ü¿XÅÜ^\x0019*f³\x0019t°
íag)çeânÏ\x0010Ú¼Gæv\x000ct\x000b2\x0011h¯7.ÔÌJv\x0001\x0002C," 2\x0013`¹¦\x0003\x000fNj\x000e:©í3íý)mæà´Býn%\x000f¾å}B{Ãß\x0006³no{\x0019Ý<Ó.IzW²îÔ²m¢å\x000côÛ¡n1óÚ¹í'1ÛæS.~\x0004\x0017HG®ñÖ\x001eõ9GQ\x0014E¨ñ×Í\x001bd{NÑ(j×2B\x00085þº\x001d5ea_Û²Ã-£vl\x0001ú{UHF@k8ôó
¿oFðIÍB(å1tbãÏßÓm\x001c¶¹\x0003{;[oO\x001c\x001aGï Þ¾EþçH¤\x001aKêÃßÿÜ°ïh\x0002=Ô¬	tsù\x0019\x001f]þ»7Ze²öÜä®\x001cÅ\ÛèøäâF}´Aø7\x0017g/\x0001÷ÑÙÜ\x0017§b¥l?\x001dD{cøôêÓÉÅ»ëÛO'WOÎ?¼¾¾ýwï<[´5¯ÍÍ|®\x0016ù\x00177AI:_áíca§ç/N.<õâäüåÉù×\x000f¿ú{'ÛÔt>=OÿÿË\x000fðPØMaÿbEá¯\x000fj§oÞ]Ýt\x00077±lúYvò,S\x0018¶Õæ¨+V{\x0004|óäüâÞÝBZ\x0016iFÛÐ±0
íÅõw?tEWlëT\x0016c-õGðBìòZu´è¥b½xþè¯«Hg\x0006*ÂB\x001dFZÖ]|´ü`\x001dW¶8}<ìÚ\x000f4k3\x0007¿\x0003-Ûò´àxoD¥^#6Y\x001e/\x0006\x001c\x0001\x001a@Ã\x0019E'%ßªÎ¤t\x001fzR9÷[Li\"\x001b¢®\x0013\x000bWàbö\x0000EãÉc7Æ\x0000R»Ø¥Tù8TQÀ¦  nÅKôè³\x001bérÚMÛ4\x0004<"×9ÒQ#Æsz4L7tæ{\x0000)|
H
ÛPCkõ\x001aÚÊ¢p\x001fün*FÍ\x0002)ý}ËjíëiõwåHq\x0014Î¨£®Æ\x0000Ô)pX¡"r8\x000e\x0015­¹ÌÎ\x0007Ò:dVÝÑÖ§\x0003P}XBõJ¹¦$JYUcEÁ\x001dmâ5\x00025Þº©"\x0014Ûê\x0006HÙ´\x001e'­\x0000Ó»9U«PQM5\x000eµ0)·-À±b3Å¦¦\x0001\x0015ª\x0012õAIô\x000cjx¿\x0016¤·O¾ºzòòê]¯ÌóCÄ6P-\x0005¦\x001c\x0007¦¬»çX½\x0001þôäåù§ëhó\x0012mÞÖ:w« \x0000\x001eþ(øW¬*~Ü¶þh#\x0011´^)5GKß\x0004\x0017²UqÐ&¨ÎóÛâUëÂÑ°_\x000f`÷í§ôëKöÇà=ºüð_°ÿr}ûñó\x0003Âè\x001e¼¸ýõò#@sd\x0003B½Á\x0014S<å*
RþÑl1« Á]þ/\x001f<:ûú	¿Kÿåù«g/\x001f|wýáÃíÇ+ùÏ/ ÀgÀ\x001e\x000cå4s\x0001\x000cHc¢F´ËÄmN\x0018ß\x0001á\x0004J¶îÀ 
%ÿ\x0011\ÿ\M¨\x0018( 2\x000e\x0001W1åÏv@P¤?L\x0010Ê(À¿\x0015\x0002i\c#àû¶Íªy	\x0003Bj\x0000):\x0015\x0003\x0019«ã\x0018bØ7\x000f6YüxÂàtmÉP0Ð\x001b\x001b0x¸½\x0003\x0018ôO·7ßsÁ@-\x00130<¾¼¹þôéú\x0000
Ôû:\x0013^:w9gläÕ\x000c·9Çg\x0017Ï_¼x¾ÃÀ¤O\x000fÂ)î´âÀ+R°£0H¬8R RÞ\x0003ëabçXÈ}g\x0006bÙã*@r±\x0019+èÇ&äçï.Uü
üÊñ¦\x0000yzùéäåå¿¿û¡l«\x0002èÀú((Ú×\x0003KÝëiÑ	ñ`À±ÚÝÙ©/N^ýÇ£¿­r^`­¢>ôé\x0007¥I0V6-å*)\x001dùøØ»,2	sdÇ&
#\x0012\x001b*¦dÁ	zÅäô.PHe¢Ï\x0008(E	Ö\x0004Ê²ì:ÜcÏ `rìÀä áG\x0001L)[$'WL¹Ïd¨FVLT8»\x0007T\x0004¨8\x0006*)jª\x0003PN¢~\x0017 ð?Ã ÌmþË/?¼ýé{®Ì~Esîo×®~úáäïW7oÿû¿\x000e^\x000f¸-¿ñàz`
ð\x0004£XLîoÏ_ó×¿_@!j\x0005\x0006¦EÇ^\x001cÅm"R¾"Tâ«Ò´\x001bÂ
á\x0008W?ü\x0001):Qa\x00005_£ï~8\x0008\x0002{8\x0012`|®\x000e3Ã¹zØ­³Ñ-æâÑ_\x000f#ðß¾1:þòË]Û
\x0016&ú7^}F07°éùú\x0006V%Ô\x001c)ã\x0016ÃìKìH=¨9µ9ÅÌùê\x000f/Î\x0005ÉÓÚ¡ñå1¿\x0005\x001aÜU#h\x0012\x001aA\x0010\x001c««9	81V8	\x0015è{à#m\x0007àxÅ\x0003ûîN´­ierè}e\x0007\x001a\x0018w#£ÐµàäX\x001bf\x00148\x0010ó©p\x0012ÚoS8Ø\x000fÀ±Mÿb¥²Î/à(\x001dË±Þ­pÊJ~8Z\x00194\x000e\x0007\x001cØ.ÃÉ5¢S¶­pÊR§\x00018Ú¡Ç Á)\x0007Ë\x0011\x001a£kU¦=½\x000b&ìrÒñ\x001fÝK7öºd¾\\x000cô¦W 8ÏKV<ø
\x001bZÝÄ·îv¶¡ñôèýõgzM"3½úº×·>S\x000fÄàñ\x0000ý\x0004U,Âæ³Ý\x001dfë£GO¿¤#²Þ«{ûüÕGû\x001eÎ8\x0015}v`mPM\x0016¬¶aM¿!Ö\x0004¬i;ÖZï\x0007°
¸\x0002\x001fºÀbÞì\x0005ûæíê'ê\x0008ë\x0002^üýÝû÷¤&y\x0008W@ÓëPq\x0005Øp«xÌrD²â±ëäïO>={|ìÁm\x0001iò\x000fèó?\x000fÂÿòï?}\ÜÃ77Wïn®¥\x0012àú¶ÜÚ×Gá \x000b[½ÿBàÈ4º@\x000be©"¬\x0007ôââüÉÅsÉ÷þêëWÏ?(\x0006ÇÕOõû%(¹@!¨R58]\x0003O	I\x0001Næ(¤] äÞ\x0019\x0002\x0004ýÉÚÍµ`
I&Êì¨;ü:6_7\x0008=¥^¯l\x0018aß"Vlf\x000b6<"$^KPÔ
¦¢`Sq\x001cÛëÛ÷ùêÐ®\x0007?\x0015Håoo2TH.®\x000eíz\x000f\x001b@Å,Ð¤\x0013ö\x0014Êß¾*Ìt/¨;»¾\x000fOp\x0008\x0014®#)-3e³Û\x0005JLÑ±ªÊ\x0004ÊU­kT\x000bµå³áàòÝ\x000f
îÓ,
§þ;\x0001àG×å9
+RW:ÚT¶zãh¸\x0010DþÂj¯\x001bª\*Ç/@Aeæ¨Ì\x0005£²\x0003¨PÚÅ° DùÆÑ¶±Ý\x0001ËÏaù?Ëd9ª0*rÐ\x0010\x0005ßì\x000f\x0016Xí>üÂá\x0019\x0000\x0015ç âf\x0005Ó\x001cV\x001aC»¦Ñ
5UX6·%t_8@\x0003°ò\x001cV\x001e\x0015)-a\x0019ÞYNM°¾ðúa±´PêÇÑ¹Ñ3.sjª\x0005QÃuä\x000båìwàZRé\x0000¿S;p¡¯![¤I5\ÖíÀµ S=Ä¦ÞÌÙªIIb³jÒùZÐ©\x001eáÓ4O¦\x0008Ö\x0005À¶·uºã4j·Àå\x0006Ö1jô\x0010"\Pl¬þ,\x001aÅð:¦¸g\x001d\x0017<¯G¾ÐÎcùjÖ)½÷mÆµ`zÝOõDîÙ´Ai"ÏW\x0014V-NõùZ½\x001e`û"øÔ¼\x001f¡Ueºâ\x0017!\x0001X\x000b²×ýl\x001f\x0015*8
\x0002'\x0014ÊÁCi.I·ÚË,èËÐ\x0017\x001cj.dØÖUt^VQe¶ÁZ°\x0019aß½Ìâ4þÓH1Ý»P1£ËJ
¢¶ëõöeÔfÉ^f¾@«r
\x0015§JA\x0013¦9_
GèûM9ts\x001bÝnn+'2vsï°Uµk½\x0007'ÖoAÖ\x001ex^cÕ\x0013@yÛt\x0004Ô\x0004Oí0x¾\x000bÏè1x1¡ÿy\x0000X>¡²¬æÛ²ºÇ}¾º¹\x000cÿ¤:|Å\x0015dN%¿\x0007[ºëÙ¦;-ô÷_ÿ÷Ý\x0017ó\x000b§\x0010%ÑÞ|àe\x0001¸ ¯ÿðüÙ½kîz¸é»®\\x0004J\x00087ºXÓ.q\x0011Ô:\`\x001e6ûûÑÙ9:;:wòW®\x001c[\x000eíd¥e¿EõÅ#Ñ\x0018:7GçFÑYø®\x001fVÂ­Q|`\x000e\?º0G\x0017\x0006Ñ%Í\x0017eîâ)\x001bjºùsñð
ß\x000f.ÎÁÅ1p\x0019Ñr\x0006Ô)_\x000fïù¬¬=xVûÁå9¸<\x0008®8NÁEÛNl¬õµ
\x0007)¸\x001b^òÉ ¡ Íw\x001drÕØóÌFN¬õ\x0007m~t\x000b>Ñc\x0012rp¤·ÇðR%Â'Aàðü\x0002\x001fä»ªßP×Ó\x001c\x0013eYÛ´QôâXèÑs8ãÙãìC¸}©-îa»©\x001fÞâ`è±Q3\x001aª½\x0019½iö&ÈÉ8\x0012çëg\x0016'Ã²¸:òÐâêª\x0006'ÐO\x0007w\x001f­åU;x×\x001a¤8×XCRT>\x0008xNGY\ö-®YÜµfì²ý\x001f·¸lÍØm[îÿª\x0010B{OÕ\x0002]ô¸f[ ì½´ïB3ÛÖ]·ÅÑrÔW\x001eðP\x0014Ïð\x001c\x0007l²Ò;'/-Ð¥At6q"_¼TàTt¶öf\x0005ºÃánxVÍáY5\x0008/PEB¼Xg#µX	<ãö\x001d\»8¸vôà¢'9Ã+þO½3bÚ»\x000fÜÒD\x001e<¶\x001aâm3{ &hå\Ø´ÏZ±ck\x0007­Ñ¡qrªÂ$Â}÷]\x0018\x0003vÐ\x00180Ho­Æ\x0000e)0ã© \x0017vÞ¶vA)vR~wB¶\x000bN±ò{ÃÓËs¡\x000fÏT¢/¦^Mx4>\x000b©Ø}Î£^\x001e\x000c=z2TPò´²|'ù¡Í\x0014Uw\x0003¤·\x000cö\x0010ñÝ	öüá«,ù(\x0010Æ ÈßßcSî.È/¢z\x001dá\x0002ÝP9	<¦,é9ØûA\x001eQ)w'
¤Ü"iúáåçÛÏGAy×ây"ý\x0010É
N9\x001cHÃ}xöòÕË{&!Ù9$Û\x000b\x0000øm\x0002\x0015Xu1Cä¬¤¿|bêäæ\/$4jäÇqÄÙsM6\x000b¤¶CòsH¾\x001bR\Ã¢¨\x0005`
\x0003Ä,ë\x0016¿|îF\x0014æB÷ºQü\x0018Qì¹P·RÈIí\x000eHq\x000e)vC2Óü¼¶üÊ\x0005aÉ1O\x0007rº;\x0001å9 Ü½j\x0003\x0014¯2rÜÊõddÙ¾î÷B%3@EGuOÔí\x001e³d4[AÞgÙÜ1é5wcZ°î¦%\x001f¼¥½I5\x001bÊ2MêP]I'¤\x0005\x0005èn\x000eðÖÉ\x001dCêÒ¹Ü\x001efÞÀÆÝy`ÀËõ\x000cÒ£û³³m±`9ã×z}Z/go%\x000b¥ü×\x0003\x001e­å\x000b*3GeFPéS-¨\x0014Sx´Àò\x0007
\x0005ºaÙ9,;\x0000Ë[©±Úó
\x0006¯¤¨Â¨\x0003û¼\x001b£r\x0003¨bËp2µCd,FåóÏV\x0003¨ü\x001c\x001fYBIè3!Kí÷RS.\x0003\x0007°\x001bU£
ý¨RòÆg|\x0010\x001e}X\x0019V\x0007®nXq\x000e+\x000eLVh>.0Ô\x0000A!S­¬\x000f\4Ý°Ò\x001cV\x001aÙYt\x0000+²B\x0005`I®ÿ2ia\x0000U£Êcû=M[+Év\x000f¿ÅÎÝæÎ\x001d¸ºá­X/\x0006ÝyÇ;Óvü!¨\x0001\K\x001fax¤çxÞòKLÊI´Y¶ü^Ã\x0000®\x0005Åë\x0011ÏZfu1ØmÃÅï­yù6\\x000b×#$\x001f\x001c5§\x0002.OÍò,ºö¬ãåõ\x0008Í{Ã¦(`IÍdÞ\x0017T{fkÁòzæm\x0010 ÙªÎ}F`Å\x001dÄ¥\x00174¯\x0007xÞ\x0016\x0003+\x0008,«&\Å·\x0017\a\x0001¡\x0017<¯G>E.ÜÓ^µ½å¤ÒÄÅ=wµ^ð¼\x001e!ú\x0014$|®]æ¬9_Q`í¹~ôèõ\x0008Ó\x0017X^7X¡áj«¨wPYP½\x0019¢ú*9Ê¸¸Õ»iw}\x0019x\x001bÀµ z3dÌ\x001by:×.ÕÎ\x0014t\x0005¥k\x0007¬¥1?ÂôÅvàR&ÀòltY×¦Kí°#ÌéÍ\x0010Ó{äÝ\x000b.B9¨áÚq\x001aÍéÍ\x0010ÓÛiÛ§æý(qÊÜ¤¥\x0001\\x000b®7#\oDrµÓ§&2©2ªðeÊÍ\x0000ª\x0005Õ\x0011ªWZÊÑ²ÂUNu®áraÏ®_P½\x0019 zSì\x001bËö¦ÞË\x001a\x000e°9»Çz6\x000b®7\x0003\o\x0016'V« 	,Î\x0017ëì\x001e»Ë,ÈÞ\x000c=ÞÒ\x0012OWB}&x¤s;PÙ\x0005ÕÛ\x0001ª7Á"\x0008\x0014\x001e*uÙ,iîÎ|YE1\x0000kÁôvéáa0,UöY\x0010\R/GÏ+Ûq-¨Þ\x000eP=\x001c²ªlLÙ¨l.óå{í\x0000®eàfêO\x0012#Q)Vm`Ì¤;}H,¤\x001b×êí\x0000Õ\x001b\x0017pï\x0010®Ø²g­$º¹6Â8¬\x0005ÓÛ\x0001¦7Ö³PP\x0019ûÅ3Q\x001d2wãZp½\x001dàz¨[àeÔâ3J©SÛmz½4#ô\x001daÇ\x001dRÕÚÃ"N{kûYÔË³¨G\x000e£5«·Ñr\x0001]h»+\x001e\x0012é\x0006¶ôdGvýï\x0006,ßç¥\x0016Õ»\x001fÑïõX¾x\x0013\x0006Æ¼l¯È07{ ØêéÉ7Oþ¾®÷\x0006éóÝpx^ÊR­\x0001ã%P9Ém²í0\x001eºúQÙ9*;
k7\x001dFÖ\x0018
:7\\x0004ºq¹9.7ËZÖVD\x0003)	\x001b'±çr\x001d\x001dRñê\x0006æçÀü\x00000£Zå\x0010hUnmÓn¡=¨Â\x001cU\x0018.\x0004âf»¾ÞÙV«Ðhõ®W7°8\x0007\x0016£'ñy.Ïi£ÍùU7°4\x00076>)v¶\x0013xç·xÉ¾\x0013©\x00046Ä`È\x0003j3fxç{96\x001fz°î\x0007¶ 
=Ä\x0015V\x001eÒË$ cEHtXw\x0000[p\x001e"\x000b­¥2\x0013S&I^Úêì[ÛlA\x0016z-Tò§ºMY=
:fó®ËH/øB\x000f\x0011Fh5\x0006Øþü¶gR3Ãâc©\x0017|¡G\x0008C!3Y¬|Ê:£)sIîo}(DÑlA\x0018z1;(w\x0013_ì¹æ\x0001Ö¼\x000c°®ÏX\x0014=&)\x0013 ÎXl×=Èæ!Ö¼\x000c±®slð	q,«ÇßÉ±fÁ±fc	\x0007¨\x0001§$ÖëTúîÜ\x0015@#È\x0016\f¸Ì;yF¦9cûµ9ßêKa\x0011`\x000b*3CT¦hu\x0016G»jÍ¦ ²\x0019\x000eùýÈ\x0016\fF¸\x000cÈ$¾\x0006Qµ§]k¹à23Äe¿/°\x0005!*\x0013¬ì0ÃLæS³\x0015\x000f=1ôÃZ0\x0019a2X>i¢Øfú/v\x0000³\x000b"³#D¦ìô\x001c$Qè¦!åRÞsÛ\x0005Ù!cÑ¶GRL\x0019?\x001aç\x0003wP²¶\x001bÙÂÝµ#þ®*ãó3iqàB*AaØ|(·\x001fØÒã\x001d1c!:Ìk\x0019h+híÛs÷®	[0¿\x001da~>(ü4S,m\è)zî\x000fj3w#[P¿\x001d¢~×ÂúÆW©s,¥\x0008²8·o)\x0017Ìoß\x0005±bñàÀ\x0015mº)8ûe]Â\x0008²\x0005õÛ!ê\x000fZÂåd²hAÐæïÌ.+Ö.¨ßP?LDyuÀk
/fS`e\x000f°\x0005ùÛ!36G	(*\x0016\x0018ÖyFc{®J· ~7dÃª,"\x0005\x0014\x0012\x0015nÕÂû\x0012£û-¨ß
QÙñÆ},7äËrÎ\x0011d\x000bêwC¡NÛr+p)I5¢îñ/+qF-¸ß
q?^BÊB±ÈØWjR:Ò\x000fl\x0019î\x001c"¨Â\x00080+fÿÌÀØ\x0003kÁünùn\x0004\x001b$DþËÒ\x000eûq-ß\x0011f_\§ \x001bL·té= \x0016ï8¿ÜFLùH\x0000\x0016PB¬ûb=nAùnòW\\x000bÆwÀèHOÿàn=ÅÇÏïnîK1Ï\x0008U×Ú \x001a\x0012^rÃ?>úìåû_·DLzÌ\x000c!3Zêt¬\x000b"qèSú\x0005w(:<\x0000ÍÎ¡Ù!h®©H¡\x000c)¬\x0018°­àãP«\x0001hn\x000eÍ
AóFêä¬Í@IÐä\x0007÷¥ ê\x00104?æ \x000cº.¨GOYæ\x001a²t8Ù¢\x0017Y#\x000bcÈ\x000c#uCadV27\x0003d-ö@shq\x0008Z6"j\x0003ÌR\x0011!N³väñ¹\x0017ZCKcÐ2wqDßZyé
\x0012X\x000f&ïÛiy, ó*KÔj^Îì9ì¾ã9¯ºP_T]¬@3Ò´Nq* °E--¤dÿõ"[^\x0004C7/\x000e/\x000bkXÝò%£nÌ¡\x000fy\x0003Ø\x0016WÁÝÚ5l\x0001¨*$\x0007¹?ñ´ÃØßu\x0017èÅ]p·þb\x0005\x001b²ø*þ/?ãÄÖ\x000bQÐ]Ø\x0016ÁÝ\x001a\x0015lÎL°)f7ÇÌbS9GËä]Ø\x0016·ÁÝJ\x0015l(ïahY87:Íú|$Íz\x0015¾[6©ïM^þzùáúöæ~\x0007]qcµèå)¿ØßR{(
ôèì?Ï¾~þêâ^{Mß-\x0008Ôw
\x0002W±iÓ\x0012b½÷¬Wþ&þS²_ª0Kspi\x000c\\x0003á\x0015v3)´¶T\x0007ÏB?¸¹àÝÂ²utÅÝä:]¡V\x0012!T~\x001fªØ\x001fA·ØszlÓéVZÎTX%/1Sç\x0016àÜ\x00108[¼c®bDs?~IñÍ\x000f-^ýÎ©ó\x000bt~\x0008\x001dÚR²°\x000bîeÜ\¢÷W½8¯zìÀ\x0010ñHà\hY Yîx°ÕÞ\x0008º¸@\x0017Ç¨®È--gª8ìáä  Ý¹°\x000b:Ñc|b öÅ]\x0013mdmÐ*Êÿÿ>p³\x0017}·¨jýLè$b\x0004\x0005\x0011Ú*Ô¼PÉD\x0016Ø>tfÎ\x000c¢3mÛAô\x000b'¼\x0004C¢9è\x0008\x000e [\x0019#;[®|éÎ©ðYy4úÐ\x0003Ð\x0008¸\x0005Ù1²3Pä\x0013«%tZ|@¡b{°, \x0007¹+°mÒ2ç¬¦÷Ç\x0005må
ÔMÕCÉH­¨ó¡'=2®Ã2sXf\x0000Vë¬lrÜU$d%	øÞ\x0001ËÎaÙ\x0001XÊIp\x001e-(ù=i©BæPýj7,7åF`ID\x0017[ý¬Ô|¶§ÛQù9*?
µ{\x000c«¸ÏZx&ªyB½°â\x001cV\x001c\x0006?|\x0016u3C°D@(\x001e¬VèFæ¨ÒØ9äÇ\x0015CZ-fñç÷LVÃÊ\x0016z=Ò2ì±Ë{Ëay§5JuØÕµ\x0007ÔJÿ4\ª\x0017\ªGÈô÷Åµ S=À¦\x001eáªÆ\x000fµ3\x0019¢}\x001f\x000e\x0012ºa-hK\x000fð\x000b\x001e
ø*®Ö\x0007£ÜÖ­íøÁÞÑ}¸´Yîy3°é#Ô¹ùNl½â³\x0015ñ\x000eæE¬àz]\x0014¸Z×CP+þúàé%w9¾ú|òþêÓÉãëÛï¿÷þýõí±\x000e×ÔÑAÚ"ùÈ	Bè7ÑB	
áÓ3np|þò\x0004m\x001f?õ¿<yúôù«ã­®\x000bX»XÜ¸Ëëâ
VÑ®î½bqû9´OL4áóâ]\x000c±
¶Mê±6Ä3ê9Î¨Çq¤ý\x0015m9Né\x0002ó­8Í\x0002§ù³âÌv3Ûqtr¤ú[I!/@+hN»qj»Xwm7,<Êa¹ëwYØQ\x0007I\x0019Nfßþ\j®=d5Ïã-Î\x001e¤¨DÚÛÕfZtB\x0016¶´³6)ÇÛ¯AÕ-&APWzÇ\x001f?õ	áêÂ¶]\x001a§&÷hªý[MK°÷6?þ\x000cÐ4Ý]ÍT­Ï\x0000­q¼\x0005R6Õvá;>Ä]^¶ê××·ïß}<yóÿþÏÿ=ÿø}Ù³GýÚ\x0010¸ÊÑkÉnD\x0017
QëY$ªìÐ§O|urþ¬\x0000¼x¹\x0006L\x001b³\x0000pÅ\x00004ÏT \x0019Û\x000cê$bª|¿\x001d_Bó#ÐRH\x0012ÓÖ.p\x0007ÙÈ-µ}ö\x001a0\x000e-,¡\x0011hYSÍ×¢óµçQÔIB<>¸m\x0016\x0016n÷CÄ?m=\x0013/.on®o¿ûá\x000eÆZ²\x000cLi»Hzs°/ÐªIzy_]\<õè¯çt0Z·²\x0015¨Úú9Tüu\x0003Øâ\x00017á©©soç¥\x001bÀ*×Y¤;Üi:MLsÔZ3I¤ñ\x0002N\x0016ÔöDÒÔØm\x001b;îf\x0001û\x0001AÝ\x000bÐ}*yÆ( {w°SÄq@þnúW³.eó\x0015=)µìÂ;£ªû&%AÙ¿|û/å\x0017°ì·\x001f®n¿O×dx\x0015¾»º=ùê\x001d\x0019\x0006\x000f\x000b ·7o
\x0014Çì\x0017·7¯/Ë0>Yj³[HWç\x0010¼ªiLe¡m.`TøâÕÅÃ³\x0007O¿:ùê	Y\x0005\x000f\x000b¢Çg\x0017_\x001d1¯\x0017¸Ê¢áÏ\x0018®Lm\x000b®â"UÁ\x001fìvÆ\x0015£³\x0017W*n	þ\x000cáâª0à*î/m*àª~zßÜ«\x001cdüùÓá*t?#¸¼!vÂ4¦H¸\x0002,\x0014\ie{5¾:\x000e«?þÀ\x0010\x000b\x0004\x000bòÑ¤Û\x0004¹öªXv$
¶g¶4^Wè3ËåD
8*è!ÓÃÒÌ<]ôf³\x000fWzÀFäÈ2ÆªÊùJ¡F}Ê2¦ú\x000e\x0007YdøO;e\x0000\x001bäXö=ÏWÙöuºÐ`a\x0005·½¨Ñ.}#äÉMÅ¥ü)³\x000fqÕÃ]¸`FT[bdºÐÂqéT£ûeÂt\x0014º§\x0004¯]¸<ö½\x001fÜ÷ /\x0018©©ÑeÂR}\x000bAC`·\x001b\x0018
Wè3´ñË-­ë\x0006ó+(ÊÆ·YVÒîæU\x0016ô\x00191å(Æ\x0019ln\x0019ÓB\x0014µ¢{\x0017.äLÐghÂª%]W2Ôb\x000báW^ÉÝ'\x00126\x001e6tBDYÅå\x001a®\x001c¬à
û'\x000c\x000c6jé$Eyí*Øíìv\x0014`.ìæ
3}V²`më[Ähëûf\x001aÖî{\x0019\³ô\x0019"1\x00040\x001c/%kìøÈbç\x001eóÅ¬(CÑwháúm-Ùj\x0015$kù\x001bX­æÛ×d½\x001e´,"¥Ce\x0011N=\x001b\x00165Í\x0007Åo`\x001e~{IÀ.Ç¶R¤ãDÀè5åZ×\x0007df¯iQ,j¦\x0007¡¹Tû4\x00124_E¹
´Xó\x0005É\x001aÛ=k1\x0003ZY1heAÖ³Úû	
·õÂôÍÞO\x001béìË×þ'\x000e±P`\x0005~öÍÛ«cP2ª%*\x0014\x001d¹\Ú'ÍïÉû g\x001eþõÅãóáË\x000fp\x001dÃ\x0017÷\x0017Éz__G2ÛÑD»exïàÏÊø\x000eJ¦|\x0011Zrñ­õuÿú²©õñsá¬þÀñË¿?kã+\x0008jÔé×,/àr}·\x000c¯\x0011z£ÏêøÅÔöuû¦rýýÆk¾
BÎn\x000b\x0000Dté³¶\x0001³HÂª\x0000ôiªû_iÿÅ30>îlÓqþóbÓ;\:L\x0005Ñ9>\x0000Á¦-\x0000ðoÑgu\x0002ÐäA¶@Àf¤	p6Ë\x000cèM3ªuú¬S@í_#`m+\x0000r`K¥ðÒ\x0016
Ð¨O§Ïê\x0012Ç6\x001cR\x0007Ù\x0018GÝ$/ó[(tté³¾\x0004Ò)y	ª\x0014wS¢%Ø6\x0003pæðY]\x0002¨V\x0000\x0006!E¾\x0004´\x0013\x0000Æn\x0001HöÒgu\x0006<)þÖ\x0019HUç¡Ìõ\x00066M\x0000Ä-é³:¾¢¬x\x001a¿X4¼\x0005r\x0014£\x0014á¯-\x0000\x0010 ¤Ï*âÕ°TöTsXHÜv\x0008QõHµñÑÕÕ2\x000bPB\x0015
o­ÜÂ\x0010 Ú0<8 ã\x001a.VH>õl¤ZÚQöWÍ\x0008IaËø¸¼tÇ5hË/åkP§ÈîeÒ¶\x001fÃ&\x0012<·\x000e\x0006÷\x001fW\x0010\x0003\x0004¹í¦ýË>«\x0000ð´Á\x0004àÅ\x000eøM0qÓò£û\x0014}VG·F\x0002HhrG¢hxW;(\x001a¿íçã\x0012Ì=`vö¦ß\x000fÛù'\x0019¾\x0002Ûd%r\x000f\x0012¹\x0007!
\x0008Å\x0014]PHÐÈ$XÊ\x001cËH¹mÂ\x0001[ìó/×á_¢B\:Ò1?2xø\x001e\x0014®\x0010¡rê8\x0013/zÚõ{ìma60â\x0013k\x0003{/O/njþh\x00198è6pöã\x0003Wßëþ\x0016»«\x001cóÓê8\x0007¹qËlña«Ïuÿ°`:~\x000b(\÷Y12Ùõô©ö \x001e\x001c¸L_\x0019ØMGÌk#!<dÃ\x0005.s\x0014ÖÆ
ô}h\[kAË¸Þ»=\x0003Û8®
lýi=Ð>h	Ö{í$Î¥»3nÇQ*PóÚ¸&Ó+5­°×²Ø®\x001d¥»\x0003¯ÿ`ddãÏý#'K²Ä<Õqé8>0Èc=\x001cL\x0016\x0019óËÀ6Ê¦Þp4y«\x001cú\x0012\x0019jÊ[\x0019ØeyvÃ\ÃjX£\x000fçÓ)&'OT¥¡Ð	]m\x0018\x0017/\x0006«ÇXó<G[SeËòÊ\x0005µ\x001fßÒØ\x0013zõ,\x0015/ÝÈaµûtù½¦\x0005õìÉ·{dX\x0007iudz¯#··foÚ#¥Vw÷VÇÈ°WÏq1\x0004åfÊ_G]¹¶þîaZ\x001f\x0017â¾fõ0\x0015T¼µ²ªbUXä ap»á\x0017#\x0014cÖN-Ìu¶r\x0017»Û\x0019¿\x00111«§I×ÞÏ4²©JEøÍ6´Çw6Àõóä¨øÞæs­#ÃÈI~³Éã;\x001b~fõb,Léxä¨k\x0011A\x0019¹9}YÛ
#MiVOsÙÙÞ·mÚÖvmooírÍêi¶\x001ecd\x001fÚE¡ÅÊN9\x001b\x0003ðMÏi¹ýf~+¿9¶ß<>Û(Í°«·rùÍüD\x0003CD·ßl!bÇG.,bW¥rè7{l¶º·Õô\x00069Îa¨l±«çYÕld\x001eYË©âg)<¾ÃpÛ5ûÚÆÐn*Ï\x001aYed×&ûî*¯ï/ÄÞì:(ÉY\x0001wFëvOÙ
§\x0019*²vGlJÍ\x0006JFîfçfcÆ=
("Úu\x001eÉ§b\x0014ïBæ:éÆ#\x001b\x0016¹`µk4bË½È^¤áÂ\x0004æs£Î
\x0006'båvF\x0012ôyå'gùÅínvã«\x0018¹[eßÚîCDÅõ0Î±m¿÷îÞê\x0018¹L[·E¸¡Pw³Eüf7ng]\x000fuýö?\x0019UêJ-e\x0004iolê:Î\x0001ÇO¾{OtüärÝú9NÝ³üÉfÏO.ÿ[=ÈÅà°·\x000f¦­²ÕíjÔÃ?ÙSòÉÚÀÞ´K9yq];Çæ\x000bk càÕ÷¨Ù\üå\ßµÖç\x001a`ýêrz²l­u)l§d¼
\x0018¤*úuK÷7æ.¸^¾çvJI¨Z®ãv7ÜMå`<ð«&n1ëÕdÖ×\x000eH=¦fÖße®ËÊøÕ»ÉªÉ¡p§ÓU¦z|k\x0005ÒÕk±\x0008¯q}Bíù(C]exàrÂêiú=\x0006.\x0007)¬\x0006,I¡Ô
G½÷¬7Ø\x0001ÐQ	«×Ó-:\x0010Ú#7ÓOÖ\x001b~rÙaÕÂ5í\x001cÛ¦¼ _ÖaÃoF\x0004y?F\7vqñRUg[+¹
Q>\x0014õ\x0018²:µ\x0007NTÜs¢
U\x0016ñe[È³B¢·yO\x0010\x0019\x0015 ¡Eä\x0000_\x001b	_7ÛÚPo\x001f{\x000e³X^ÑJ@Ä«ÙU1¾ÁP*\x0010W\x001f¡ðÜV÷\x0017j¨ù
JI\x000e^2_x«ë¤¸z-eàÊOxj\x00117íï\x001a@\x001d?¹ëÆ¦FhQ"º¯)èé7üæÂ!qG¬¡.DL\x001cJÖÍ¾Ö\x001bM4­k4B7\x0004Ó\x0008BÉVÊpdÇýd]GVw6óä¯Ê2·\x0010Ã;x^¯¿S \x0019oëÌ1 o\»©Ôð\x000eÓ0êÕ0#\x0004\x001e¤:Rëæ¥;/[Ì?uRL>+KmäzÈ¶ãÂ$FXr_D¾ÖaNUæ\x0007^\x001fÄþó¶\x0015	©/Â÷ëC£º>+\x0016>Rv\x000e¹)IãK)ÿd\zõ,»\x0010w#Í6¶[ÝcZlííø/\x0006éU\x0016óÆ0\x00031wæôÕ\x0018\x0013ËÀaY£z>+®«¦ÖÎt¦[\x000e¹,ÀÔ;Ýï½y£¾ÇdPàþðêæíå§OT
}0c\x0005:ûÓ&Q¬M	+Á
\x0016Ïn³wþâäáùÅã³\x0017/Î_t\x0000iÅª=@Ð¶½6YÉÞ²Jâ\x0016ÑÏ\¼%cT3CR®ä;èZMI<É±\x0005ì2É 	q;²)¯\x0003M\x0005Ädµâ\x0013Q||\x0006£×Åf$X×l»\x0017'Jv/b\x001eÔ¼\x0014G6´ÔÂy1å(²®ÙuÎI¶~º~	\x0014%ù`æI£HÊ\x0016ÉÛÄë\x0016¡&aí\x0006if!´}¿"Ý.wn²8NB\x0014¶ÜX×Æèø¼\x0015\x0007½Ó§\x001b\x0008G¥lt²_­xXtñ\x0018¬C¡L\x000eÝË&È?æ'Bc"S×8¸Aoß&¤UÔ\x0004Ö¡5áwR#"ÀÈe	\x0013hÔæB²nUÛ­o<µ GÞ\x0006æX1×\x0001½}ðH>nÌ:¤
&®\x0017ðÍ\x001b÷;ö
ÞèÓ5+ÆÔö\x000cX ß\x0016¨ù0aÇùÇG¾9±MpÃ
&\x0012hÅu-|7Cñ\x0017Ô{\x0007\x001aÓÀÏ§§¤]nûéE?\x001a\x0008L\x0013Ým\x0018¯aIru¬ö×âø\x0005k·/\x000e²CèóGÏÉjþÇ\x0002)F,Jl\x0019ûºe3=ZW£ÍH\x0005X`¥J\x0018myû1¶T»
r»ì<ÉAÉf©Q¡Z\x0008ãÚAg¢\x000fßÉ\x0004¦ÜÊ}`
ë{©Õ¶h°Å¬¯m3\x0010Ìf4X§KZ§N0¿ç:\x0015ûÒä}÷2åÚ0\x001a&\Ê­j.iY'\x0017w\x0018Ø\x001e;¸éÛÁÅ²­Ýì8~XãÓÅ²mÙ Víñ;¨¡wÏ\x0014Û5´÷'dÕy.¨f³ëñ³~ûù6RþsùWk9ÇÃ«_.?\x001e-e0¹¬º$Ù0Öj	ý°¨§zxþ¿Ï\x001fW\x0003'é]\x000fâbð;IñÏ%íÜª¦XÞ@#\x0005>k\x0010L\x0001ø\x0005BTàXZ\x001d6\x0004ëü6\x0008(Ïê,Xx:òø¹®	MIZ°5¥M\x0010À;ôY@\x000eh]\L#[cå¤ò,\x0018½¬mì\x0000kÄ®È¤5\x0008q\x0017b!ï5\x0002\x0001\x0019Ì¦ç@h­¤¾&!I«>1hz­ë\x001dDuð°\x001e}Õ¼\\x0006\x0015mÞ\x0000\x000fJôY\x0003k\x000flEÝê|sòv\x0013\x0004Äè³\x000e!5r6Êë©Q²\x0013ÈÙ\x0004\x0001~\x000b>ë\x0010BÓDÐl­\x0010tjnaÛqHMß³\x0017Uô¬*Wx)\TaÆÜxi\x00139kÜÿôé \x000f"P¬²<\x0007-KÓùMÑ±\x001eÐ§\x0003\x0001æ\x0010\x0002ëøºåJeÁñ
\x0002û>üüÉÐõ9Pu\x000e\x001e]ß~¸¼¹z÷þýÑ²Cô.´QER\x000c¸­E¨\x0011æÕ¢äïÑóW_]?yúô87ÿºyû3\x000e¤\x0002Aå§*zÔh@Ñ«èask\x001cÝztä¸¨QåP_t`\x0000f=\x0018Ð\x0010!(\x0013±CØ¡×z\x0013\x0006Ò\x0004¦OÇDÚý\x0017\x0013áb3\¢ä2ò\x0000·®«5\x0010å`J9UVJ¸ÚH|0jQ;\x0000\x0002Î\x000b}:Ã2	$rd­+QïYÈD
aÀ»¥³]\x0013\x0011Z]r®
¾âò\x0011LÔy\x001b\x0008äÙÐg\x001dÁ¾¬G4å \x0015ë\x0008Ëb°
CD\x00040ª¾\x001da©70PÏøº!ø±)h7.\x00064rtîÂ`jj(\x001dbKpÕuJîNm&âû_þ\x001d?Ä3¼#ú<}÷ñè{[!÷±é¬T(S\x0007¿oÎ%\x001a<;ë\x0018ª*µº`]l\x0015)n,#\x0005¾¬¢Ô&¥dõèÀù|ß/.ÿP~nÍ­\x000f9µ!Íu¡:G©fòÊ¨ÑÈDYZ9øR#Ò¼\x0010+í\x001a\x0018\x001b>÷\x000clrÖR}\x0006é°ZUÎ½\x0005¶ã¿\x0018©$ô¹w`4«X.ÜfÚäáIúÜ7.
G%Ó
}7ÉEE\x0003ÄÖ6÷Ô;\x0007ÆÆ
«\x001b+Ê$ì\x000fhÉ9q~»t\x000ey\x000e+ó\¸²UÄê¸­Z$¥yÐ±o\äÑçÞõÕSY´·5Ö\x0019R%F\x000cßHE³÷3IK¢C\x0008ººQËgÌ~xàL«÷\x001fa<ÊUë	Öìk¢5;Ï\x001dì\x001aWÓ3|ýÞK´T¥ô\x00135Í,(×y1Åd=ò ô\x000f\x001eà®¼¸½:ys{òøêãÕÍå{(Ù?¾¼=n`[dO¶ÜQ#ùö$Õ+¹£Ó!»xu~òÕ«ÇçÏÎ/ÎBÑþñÙ+ØÚÇ"c\x0015'I]ÎpVéËQ¤ÎL\x0015ºUeú)\x000b1ìAúº,"\x0013\x001d#}\x0008M\x0001<tssùùäéõÇ·GùLrQµ%áÄ\x0002¬8ëò^^,Ái?}sqöòäéóg;|ûú\x000e×=`´ä3(\x001fY¨©T:77\x0003À\Þ\x0001sÙ\x0007¦N²Ü\x001a°00sXÖ¡H\x0004îzWÿ\x0001i/\\ß~¾Â\x0006zqy[ \x001d¥uT\x001eÐ¹xòªIoÅd\x0010ùs¯g!Ïç¯^cß¼8{U ­¡2j
íåª¢S<ÅÓ&J!ZiÆF½¨^+U\x000bùC[44 	´ßÝ¼»ú\x0004\y]}wÔ÷JqÌ$=\x0018u}Ó³R²~O.¿\x0000¸¿<}^Ð=ZEã\x001c\x001d¬\x0001teGËÛOY7¾-SJ\x0012¡>Ü>ty.¡\x000bj-M"Ø²\x0008WúÙóË\x0006pº\x0011j]Xðé\x0008ºHþ	¡\x000bÃ\x0019å2s\x001fwMnÑé1t©	K\x0014S­¡³"66×ÒÞÎ,Ñ!tÇyFç\x001c³Hq|å\x0012÷n³	]Â³cS»1ÇZÙ~R=¿\x000f[Âs§V¢N¦vEÂ©@»m[àÙåìÙÁÙaÁÇ6Kü;¥Vpéç&é&xËÙ³c³G²\x0001,Â¾æY\x0018YÒ\x0012æ:[à¹\x0005#ã¯CðL\x0012@££¨dÆI%Së}'×/áùAx¿ó}fGÃ\x000c\x001e
ÒµÉmq5º[&j\x0001½çhÌpWð\x0011|64\x0005@M"\x0012Ï5\x0005@­vò²Ù|o\þ©¨ÙÚ;\x0008\x000b½\x000c!tÆJ=¦)Öh}òNÑHn`ÐfÛ\x001cÞé5^ÿ\x0001$ààeýíêòãIí¬w4xé½ä¨Cnãú\x0005tÄ\x0005qá[ýíüìÙIm«·).1
B^n^·­ÒÒVÀØã¨%ñ·îÆ~?:a\x0015CúÒcPñ÷8uÂ»©/Þ\x000cË§\x0005,D¸:ai¯ùA"Û(y\x0004å@âðv&:¸x}£BC¬Þ5\x00106¸ÖÛÉ¶Ì8+\x0003\x0019Ee|;m\x0011/ûW1K
N0\x0019r)u\x0015Eð1\x0007»y¾Ê_"+¾\x001b	A<ø\x0000\x0005Ä»ÞËËÒü\x001eè\x0007\x0016\x0014m¯)\x0010\x0013ó\x000c\x001dÉM\x0005Ë\x001fïq¢}\x0010%2W|\x001cIWñ\x0019Ô,5¹«øëÉÙÉÃ³g÷úÒÚ¼º0Í]¹üB\x0015¥¯/ßhh\x001c­:r­©\x0006\x001arM]Sy9¿C\x0019_½ÂÿêÙú¿zÏ\x0005@ëÓDÿé\x0001{¿yùîãU\x000fõ\x0017{ÒLÖ©SÒR±\x001cô,ýÍÓ³'ÏÎçÄ,\x0012ÈÈ´Z Ã_\x0007 é±n!¬Â7»Ör+¥¼\x0007^BÓcÐ¬p-òpYy;jßRØSÞ\x0001Í¨\x00054´¸ï\x0006]©$%\x0007ÒZ	­íå!h^¾9\x000emîÈ$vdºg-Dy\x000b4^AAf-\x0019´¹5l\x0016"\x00052ö"3ÞHi·À©æRü\x0019)¾\x0019Ù< TQD©{ÎåG\x0001ë\x0014ÇMST­HÓÌÃI£ÈZ¬¦Q#«iåô¼`æWåò82ýí§+\x0017\x0003Ñ­è·=¼}õî\x0017ÏÇB?xQnªË\x0017!KA#S.4+ó²Ç«$tÖ*Væ/\x0017ÑÙ³\x0007\x000f_==ò¿\x0010êbtÖp[\x001bÝ(jÄÑ­­Ä^F7JF\x000f5ÕattÖq[\x001b½XTz\x001a\x001aÙÑ]ÕëÃèµvtt\x0016s[\x001d]QÉ4F7©>ÀÑm­Ìè@¼it\x0016t[y
é}\x001aÜ¶eçG+\x000c^÷\x0007\x0007\x0017Q·µÁµ§\x00173®sõÙËèZVÝÕitp®#^\x001d\FÃÇÚ¡\x000b×~¾iÇ¾ÛÊè1×DH\x000e!ÁL£Ç\5Ëè6oÙñ"ò¶6zðlêè,!XFg\x001d.\x001e6ýv\x0016z[\x001b=V-\x001d\x001eDVÊèØ´}ôò/¹u¦+æ\x0005UrÑQ
K\x0010Æ\x0015D£k[%^FG/ÿ[g:äþò²£Z\x0007×'^³\x001cêèà,t·¶å'a\x0008"ùD©\x000feÇû¶ãã¦\x001fÎRwkÓ^\x001c\x001f+g]×D²²èüã¦7^N[§¹lÛo·[M­¤í¶ãDioõ #c­\x0012,ÇýpÎ½ÙÅq¢¶·ú³³ìup­ò|Îmã¸-\x0007M\x0004÷V	¶æ¬ÑO\x000fUÊÛ
.®-ë$yßCpµ~¸%Æ6ënÓà\³ÊoºýpÝl)H*ÉèiÓ´£ÏE\x0007¿ùª*É;Î0»:;Ýª[\x0006g©ÃÕÁIêFÖ\~º
Bí¾IÎ«£+A)Åfdl¿|ÛcÝÃ±õdÆñnÖMo\x001aµ\x000fW÷;ýÜv¥ÊA×¡q\Ü0ºè\x001f®^©¶\x0013ÖË\x000b{Aæûß."k£;7ï©ÊçßnB\x001bÝo9n¢¸:zl÷ZÙ\x0002½õ\x0018¶\è¢¸:x>ezGøYÎ6#2-§
/ð¡æ LÌDãmMÔÇªkÓ\ÆM«Îrk£[L6
^\×È\x001b^eÙðyÓq\x0013EÆµÁÑå·\5[\x0017£ËÕó¦ÓÆ¢«{áØ¬f\x001bæXm¶ýtVf\w"7ùé¼ßu¶bÀª-[\x000eÉ±hlM¼Áà(
2ïòÓõ&F\x0004\x001aWi®ÊÓè±
âµ[®V\x0011i\\x001d=RÑ7-»©\x0005\x0018ÝDYöM]\x001a;FgW\x001d£ë$£g\x0019}SFÔ\x001a×¼¦rÄ3_0ÑóÐ\x001c6ýrÖkìð\x0017
ÿrÓ¼Õâ/Ëæ6HD´±ct¼Ðè¡í9¹Yµ³¦ëÒVÆQ|\x0007o§Ñ·0
²ãb\x0007Óv¯£El\x0016 ¶iÓoÏÔ3}}tCÙ8\x0018½\x000cÇ,\x001br0ßâ·¡\x001bkêà9Dåâ½&°ß¦CíË3:º¦NöÌè\x0016í¸aBrBöu\x000fü\x0002\x000f{Nmzì\x0010ú¬¹­!z\x001d\x0019U\x001a±ù\x001a	¢$jË¯ÇÑ§cßIX²\x0018õòës»`Y²tlxpå\x0003×aÔ¡#¹\x000c°8ÂSl¶ô¶°$©­ fÕA7Jñc<Ûò1OÉMþ#©½xÝ1~mF%¾;¿\x0005\x0014ß=6ß}\x000b\x0000\x0000 ø	«\x0000R¹c¢¸ïTª^#ò2¾\x001fpf´ùáõ÷ßÎ\x0014\x0002ÿzùáêòöäÍÿû?ÿ÷ìæÍ»ï~¸úx\x000cË*vQV¡/7!¡Å¨P\x000cÉý	¿}}~öêä«³¯<úëù±l\x0005ªr\x0005áÏ\x0010*íÄ\x0008ËÉCÿP%\x001fTÞª°\x000bþ\x000c¡òÃº\x0019þ aòÖÈ5q'$tÞÌ£\x0013eÙA\x0002W\x001eÁ<Éå9·Z6`¢¬túÍk¾IlÀò±±Ý	\x000bEqø\x000cÁ*~4Ï\x000e5{\x0003¨\x001aåç}[²Ðé36W^\x0019U¹jTw?kúÍUàv¡ªÊUP ÑôìÍNT\x0010nÀg\x000cgçõ°É5\x0007ÁîÝU"lñgÂ$"§c$lÑ\x001f¯jÞ»Ê:í\x0004%ÕìC Á\x001b(ÅTi¨örUzP³¦ÆPù*²¿m¼Ò\x0014v^4Ö\x0018­æ YWb^Ï-ö¤w¿¦\x000b0f,\x0004*gXrÝÄ8ÁÚIVMH÷Oµ³Z\x001f\x0011T){	gÐdUf/æyã\x0006ívÂ\x0002êQ\x000e-\x0006¿OmÇ\x001bÏìà\x001b,µÏ´ÛFÏ¡ng/\x0007qºÓNÒÂÖ¤Ï\x0018¬H\x0005ý\x0002Q\x0019ÿ¡\x0012¹æ±­9'#ZÉ\x001b«Y}èì&P`R=Ê¤HÖÍ
bÎa²döÎ\x0015¨T\x000fRiÊ®Å4­ãÇÊ2[Ílç>VÛa!å>c³å¨·\x0002[î5à\x0017\	¿X³s¶\x0000ËÐlÙöæ½Çf×Âqzç}h¨éý Ã§âyñK?0ÏØÒ¸´É;I\x000bÉô\x0019\x0005¹Ø(>°ú1iSõ\x001aÛðv:ªö}ÄoDº×'l2_C¨ý\x0012×j\x0014T&µwDëwÂ=c\x001b«¶-¢7\x0007yÔ.\x001b«ÙÊa¯«Ú\x00044ÇfkJ\x0017Í¬ Ùj¯®i¯íÐ`9x\x00132Y×Pµ vRië\x00180v
\x0004Ó²1U`°À²IÈAÙ½°¤{À\x0018¬|jM»x4¯!\x001aùñÅcwÒCk\x00145¶ãk+\x001bbÙ*El³eöÚðpyé3\x0006kb-Êç(;^¬:múÃ(ç°xòµvXKÞ´Ùy\x001dõè3J¦a²iØ\x00004¡Å×ÜÞÉ\x00125³1TD\x001fè6T Õ
Ë4ÒÚ=YÒ:cÌ¤±-ì¸Ív1iRX²q;o\x001eäÿÓg\x0004\x0016²³\x0004þXø±À²Íiuû!eÚºQ\x0007Ymò2d2g²Éj6NûîC\x0017(z\x0014s-ç/$N¤/¤5=ìäRO)x~4L\x0003#ÞÕÇ²lþEÅeö\x0006Im¬­\x001dPz:ºÃ·.U9+¬¢nO\x0015»¥,
"C
£DpWó¦·íªÞk×\x0014`¯+°×cÀ²ÜÊòQûª\x0001k·õ^C° û®"ûn¿tK\x000e)ü\x0015²\x001cÉva»M´úá»wÞ~@e\x001bëM6¼º=ùêÝçÇ7ïÞ¿¿¾=ú~	¹&Î
ÔYKV "`R.ÎÝÄ§OÎ\x000b¢'/O\x001e_<yúôù«\x001eH\x0019ò\x0008¤b\x0005ÚºFµ4ÉÄ0¤4S\x001dd½EnH*d¹\x0010
ÙÉ¹@k¶j=ÚóVD(]{@¡IªUÖMÜû2Ilü¡\x001aj×$¡ñÃ\x0003úüi¶\x0012µA¥Ï\x0006R9k`O\x001c¹Ë?\x0017ª×\x0015Õë\x001dHeOµ âðrÉnÙäæû¯óG¼ÓC\x0005õ;ùæúãç£@(V ·HÕØTÇ¿0ßÚç'ß<vLÇ`1>µ?^\x001f\x001f^®ZNÁ°\x0014j\x0019_ñÕ¦ \x0011³i|u_Î3_`PéP5{2ëÀ¿?-l\x0007Æ'o®cþ-Ä\x0015)\x0001\x000e\x001coZR6Ûæ_\x0014þ×Æ×Qê
C #ÆwÇâij`xxB¡cx;ý|Ô]ÖÓ¦V²ýæñÜñI·cüb\x001ap|-Àáé¶ò/ømÛznô\x001d¿\x000f\x001c¿¸óø\x001apÏøQ²X¨ÒñYý¨oÒ¦ù7Ôn£g|MÒ_eü¨\x0003Ûå÷[æÁìó¦ß°é 7uøbüÛÄÃgYþ8\x0013\x001a\x0018¾pé`\x001f¸\x0019³\x001fÑ\x0007(ðøòãÝ¶Ñ\x000bï\x001eî||=|Q)ÉÏ,è^ÆwÞn\x001a¿ 6=Üã¢¼\x0003àð)}NbÆáÛ¶ù\x0002îãñ5µ^¢Ùµu*~¿ù_\x0004f\x0007Æ/ÄcºÈÇiBùÜüû£oãmë\x000fÇ¤|àäòï/ÎfîÓî·È\x001f7¶é!\x001fÇ'ß²<Öbñ\x0017¢\x001aý#\x000cn{ÇU\x0011\x001b_Ã$üãeòÛ´ù`·Ù\x001eæq-W3â\x0012rødül7Ý<\x0008lÛ\x001eê)ÌÏ!«ràÅ.ÎYÉáOÛ6\x001f"Ø¶||BàèZMh¡^1<Ò¶\x0007±jÛE>-¾\x0019£á2ÿ­ü{ÁÛ=¾E\x000f\x000c»ØWO\x001b \x00069}rørÚB>\x000eEuË/7Ë7ª6\x0001ÎËÕ¯ã¶
à¾}ýî\x0013-\x0002þ³ã\x0012¨sÎïr\x0008[yªÚv\x0003è\x001a\x0001Ô\x001asÍ\x0002"î\x0013\x0015·3\x0005\x001aä\x001cøù\x0013Ê\x001a\x0004mþ¡Í'@ \Ûòïý÷½½|ùéØø\x001eK4\x0003NAí¨\x0006CË\x000cT\x001a4ÚÙ6xqþøìéÙ±~áaüÃã\x0014üÃ£¢ã\x000f\x001c\x001ej\x0004ÿÓÃÿ.oÒÙÖhéÕÉßÑhîãÕí?¯BQ	cÓ1@ü­^\x0007\x0006=\x0018ë1(P\x000f<ü\x001d\x001dç¿úû±\x0006\x0013\x000b`uSþé\x0019hÐg\x0008NIW4$cjð;9+±S}(9c\x0014\x001a<\x0019?º:;É×.KºbòªAs\x0007^\x000cF¡a9ýèj<ð3²H\x000e1Ì\x001cx1\x0018E\x0006\x000fÈÛQd¾ÕêEÕR$iåÆß`«y@óÃÐª 0 )· &§ \x001eÊ{\x001b\x0006¿ÉQh.\x000b¯ZÝ¹i*>Êßâ\x0014À¥òq\x0014Z \x0004\x0012\x0006
¿ú\x0006$i·pÿ
 ÁÛ?vÎ\x0013Ï_y-ÜQ\/\x000eüXã÷\x001fPÈÐg\x0010Z/^¡\x0019É)¦T\x000c-ì5hÐg\x000c\vW ±Îy\x0016YÊ¥@û\x0001.]ú\x000cBk)\x0000ZiäÎ24+'ôPzñ(4ðZ\x0018æ5\x0004Ö-Pr\x0015ÛÈ¬xà]{\x0014\x001a>Á
P+iUènÛ	\x0015ò8T\x00084ÂAÃ´f,º¢×IË\ã^&Íe´Ý;tè3f\x0011As×µóÉ«9]\x0005\x0007³\x0014\x0006ER\x0007\x001dæÛ²òNê¢$'ÕÞI\x000fß\x000c!ø'iün\x000fR¹®]KIKJÌH§ÒoAjõRÏÒ;úÐ¡Ã\x0004¯(7Y.KÄð°vóÄeÿ!éë^ÁÃëÛO.fP\x0004\x0003U<²9l.nGïzy\x001aÒT«óÏ_½xqv<bè®;°(pÊªÍYîòJ åÃ¾À\x0000¤ê·@J¼¯,ÚÆöë\x0005>¸¯\x0006 U_v\x0000QÔ. YySS¢&Y \x001d*¹\x001eTýÛ\x0011HÀ
$'z²e¯\x001bd\x000f$ã\x000cAjË\x0018$Ç9ª\x0005¯]Ô\x0000E²
$¿w/\x000b"A¢8x\x00148eÉ©ÀÌ\x000eM}¦î¤ý Êÿ9'ÍÚlrÛMÐb­ ¬;xE\x000fÂ[eÌC3F\x0015SÈòpU8\x î<t\x001a:4ô\x0019ÃT3\x0019
(/â$\x0005TfP!í\=üûô\x0019¡'Åz1eK\x0019Ñú,g\x001b\x0017ì\=D©é32S\x001f½â\x0017o%4eNì\x0002Ì4Dâ:\x0004d{ÖuÛpç	§°¨S\x0000}\x00060åÄ^CWfÖÄK¥Lß\x000b
9ôiÇ5r$L\x0005¥IE@éØVï°ÿ5\x0000
#)1fMÐ\x0012¼jZ¾ìÚL\x001d*Ü\x001f\x0002\x0005ÚLc´ur%3\x000c´\x0018OúP=à\x0010$J0\x0019»^ ö[!ÙÜ6ãò\x0007£í¡ò!L ò4Fäå\x0016öL\x0005Î4P>\x0005\x0001µÏT)\x001b\x00160cDn%âLäv	ÓDÅ}¯FÛ
úJH\x000f!Påvql\x001bPw±ÕÓA\x0017a\x0000\x0014<\x0011¹3\x001cXyÉzCÅRòáÒÞå\x0003qæ1ó· \x0011âDÏ\x0015¾`²£ç\x000e¯\x0006@8ó\x0001ì,?¶\x0016>P§¼zÞ\x000ev¯\x001ex3\x000fñ¦\x0003·¸YÎL7HêpDy\x0000\x0012X3\x0019å(\x0007áiÒ­åFñe\x001fy\x001c\x0018\x0000\x0005ÞÌc¼	 5P,°©-§Ã\x0012VC ([o8-\x0012¶ô´¡x¦$\x0018\x0017ÌÁpc7(£(o9-\x0012Ib»b9
L9÷msC!\x00035DRÖ'ydEOM²*\x000e©Ü0n§u@-\x001a28Ë>å\x001bÆÆÚG\x0011,Ýé{R\x0007V£xÓ¢ÖéÀ\x0006É,â}°\x0013\x0013â°j¢lv§nÂÄÙáF30QûøÀ n`Ô\x0010I\x0003Ç)ó0ÇåA¨Aí¤\x0003ÀQC\x001cecæî%\x0014«ãV\x001aHdÿÂP\x0006ZLF
q\x0014ZØ¹)\x0010ÅâófÂ\x0014w.\x001e
\x001c\x001e¢(t}W<QY´'\x0010ºkÁ±°sõ4¥\x001e\x000f\x0019w\x0016-­Å4wÜE§É\x0008ÞÉ\x001e\x001b=ÆFU\x0003£ù~\x0011K£Í!¯!P M=FÊó£i¹ØÅôÕí&Þ;SàM=foâuO^0é\x0016a9T9	\x0019\x0003zÌÜÌ¡\x00057S\x000bk)X+ä²£PÜaô½	\x000eà£\x0017ý)ï(ç\x0005SL{'
\®
NÍñ±à$\x0005½Ø)²z_ù\x00060Ëõ½\x001e\x0015\x0017\x00014§Û~
{I\x0013D®Ç¼ôb®È,ùv»hÕ¶SØ{î¨^Ä¹éIr°\x001cÉ1²rJvþÆØ\x0010&\x0010¹\x0019óÒ²%ÕÛjØ\x0015§EbÀ~¯\x0001\+KÆ¼ô ù\x001c´\½l(Y=ïöÎ\x0014¨Ü½y\x00116²È\x0004ç.{*gy\x0011
ôT@ÊÍ\x0018#U.6PÝô¬Û>ßËå(æ3fË­o´éE\x0016Ø)©Ò1ô>´\x000f\x0014¸Üqùï~øÀåfË«\x0012\x0015\x001f>9y\x0002hg\x0008ßPQ\x0019$òÌÑ\x000cKzÅrðdáü^ç
mÌ\x0010k´Üslj*d¸Ôg\x00166;\x0015\x000co\x001d3Ê\x0008Ê\x000c¥\x001cûÃåBbëÃù\x000f\x0003 ÀåvË5^c+\x0019 £M\x0015¤ìqµwù`Ö\x001b;ÈåòÈèÊÿ,\x001f\x0014Ë[Ôn'\x0019X*\x001e\x001cãò Y7¥Ò\x0012bºL{Ù»|àr;\x0005§,È¹ÇßÊÑCZ«±c\\x000eû@fÊJ¹«6²§´:¤28\x0004
\nÇ¸¼\0:7\x000f¦=-\x0008u¦C\x0002¤\x00030Þ\x0003úÜÄ
Ý+M¥\x0011ÓoõX\x0005\x000bÿ\x0001}FÞ­EÇÙB*+¶àÍðL¹@}íX ØdÃ)±ôú\x0019ùðI\x0011ÑÔ\x0000w\x0007(tfà\x0006\x0003Á1¡¢±Ê"oaÜä¨«}{ÊæÜq®«ºZ\x0004+îdP.)¸Ó)vø÷ÝÑ<p¶îÐ«/s<*HËvntG=ÝX41k®+3E\x0014Èö¸àvºÅZ¦ú±g~ëNù:6ëô]%
æ²Ûyóy$Wù0FS>s\x0005·E=q»ù¬$"ùÃµ\x000f#AsJ)UaRººhñËÁ»Æ(¬l\x0011êÝé\x0007T`Ò\x0010,d&:æ*§¹²ÀÑ$ñ	Ü\x0019Ü(» \x0016âõ\x000bÿeäjÎUM{>ósh»\x000f©\x001d®#ûá§·?iãO¯®oß~¼üî\x0018\x0010O\x001dÆê-cu¨OÅÖ\x0005©Kvqî­õüÕãggzÆ]Ïúø³³,ÀÇ72|Ö±Ïêð:Ë%kçXS\x0019_úº45
\x0000aÏúï·õìX*ÏL<¾ôb8Í¦ñI\x0014"®\x001f¼\x0011¯Ñj/DWnÔ +`¶­\x0000\x001cX|Ö' H¼È *3\x0019\x0010qgç·-\x0000U|VÇwO¢5Å\x001e5¼\x0002Èíæñç4ý\x0000ÎIU\x0000e\x00058\x001d\x0010\x0013P»ÜÙ©»Im\x0000àâ³
 \x0018q=cÎ¦õE\x00157±\x001d\x0018\x001f\x0014z(\x0008µUÇ7\&@äìÛ\x0003\x0000ÀA©Í_¯Õ²ckåuI\x001c:§¶
\x000f/\x0012õ\x0013Ðº»\x0015Êàç\x0013[W\x0016À¦m\x001b\x0000$zHÐjq^\x0001_)]l,lÓ¦K\x0000ôYgáB¼\x0003j¹\x0011\x0001hÖ³vÛ\x000c\x0005S\x0007\x000b\x0004\x0003T\x001b?·[Àm#Ad'Ògu|è²1	B:·@!wVm:HE¤Ïê5>8\x0002À³2uMéØÑe²\x0001\x0000H(wPð\x000bà,Þ]]¥a+EIÅ\x0007°î\x0001¤\x0018Òg\x0015@Ð\x0005äÐZµÐÀ¢\x001c»\x001bÃÛ\x0017}Ö÷\x0017\x001a´(}\x0008²\x0007Ä\x0012ñ[Î\x0000þý\x0007ôY\x0019ÆûOs5¦VÝ\x0017 øw0Ty\x001eÈÓ\<º¾ýp¼&Í8*A"\x000b.JK¡\x0015~,nÁ§g'¿úúx!Úûpûù39¤(õ¡Ï£\x001f®>¼û\x0008ãüÅå»OþvuÜ>/·¯çB1´\x0014ðyi¾â\aûÑ_Ï¿~ò\x000c\x0006ú³'Ï^üíü\x001e\x001b}B\x0002sú\x000c!ÓZ³
Åxåþ\x000eQIhçZ\x000bCÐnÿáÿyM£ðë\x0012-Û§w¯¯\x0014¹ÛD¡k<$ÃIQ6m0óxÂÓ³\x0017'\x0017O\x001e\x001fW\x0015!(÷\x0016þ¬#Àë>/Uùt\x0005ÏY3FíÃ\x0008ËÛ¾ùñ¡ü{øóÍõíÍç«ï~8\x0006¡`ä!Öá©ÈË£¨§ÁÏ_ò¾yþêâåù£¿\x001eß"ÿ|÷éú\x0013ÅWaEãóÍÍåË÷Çµ]Ð0¢öÞ)öj@ò/ÙPIrüüÂûæâì«³§Ç§ \x0001° nú¬\x0001 î\x0019\x0015DC5"It\x000085¯&ë\x0006@Ö?}Ö\x0000@Ð³®\x000be2j\¹\ ,0eB´\x0003\x0000ÞÆïÓn\x0011â.\x0014öøêõÍÕã$::/ÿXr +$-8ìñùÃó¯Î\x001f|W~Ú§Ï7÷ hþd\x0007
\x001cIárC«C\x0011¼o.v\x001baØ\x001a\x001f²\x000fuÍpc¡(ÀØ9Ø¯m·s!Y_XÄN$)\x001bq³\x000b³×\x0006®\x0010"hqyr`\x0007Oöç\x001b"BàøóòæòÓ§«£\x0018¢N­,µð"¿¦kM,æê«//Î^¼8¿¸èÀ`abÒ§\x0003D¹3¸À2(Ã¯Ä¾0\x0014SUôóLîu\x0010·7Ný;ÐE\x0011ø<úáòæóå»·×·G%©½«O\x000b_En5eµ<WÛzqO×ØÙÅË³'¿:;.G=AAÌ>]PÃ	\x001eÏ\x001b,\x001dÇ	987=» Ä·?üð, ô­£ÏÓ«O'\x000fon\x0012X,\x001fgÑ\x00199'A\x001c_,à¹\x0001úôüÅÉÃWÇ\x0019l8\x0018}Ö!\x0014ïÏ²'\x000cæ¨\x0008´v~^`³à2þ|m=M\x0002Ì@ÇöÄ7ï/ß~<~\x0017O °7ê¼V,Òa­çû\x001cW_Þçß<={üì¾\x001b] ûï\x0001}º¤À.C2ðÂ9Ð\x0011Õ[q =>]8i\CÅ!HVz1ª9<RüÅùÓr\x000f7×îÍÍO\x0003ó\x000fÆ»rÄq\x0003\x001d23\x0014(,ñ¼=\x000bÿ²|,Â\x0005³Ë
ÿq\x000e½£ þõËwï1³búÂâ\x0017~:z\x0004Õ\x0003â\x0015
Ó)PU¼vâÙI!¯oº\x0000ÔÒù\x000e\x0000¾ÖñskØâm\x001b?l\x001b\x001e-åÿ°á\x001d\x001aÐg\x0015@Ì\x001c«vÈ,ànåÿ-,»(+\x001b@\x001c úüa+`È¨¦Äÿè&üGáxIj.Uá\x0003ýÐËÛ7G\x000fb\x0019R4TL]å¥r³óQè½új\x001d\x00002\x001eÐg\x001dbK§Z[O\x0000¤´\x0017Ý´m?ïonÿ¡-Y1¸*ñytýéóÕ§«oïÙÚà?P§J-JNFÚí¨0ïãðèùç/Îÿ×«ãëpýUÿþyy\x001a\x001f]~ø	Ì|Ü÷5Fú\x000e\x00173N\x001eñå¨	RÌöþ£³¯¿\x00015\x001fµ´\x001b\x000c\x0003%Zút\x0000
É+b´Éìý¡Û)«;Û|Ç¼í\x0007bá}Ò§gFbö"Kæ]æ°Iá
i¦Tp¬.>0}þ` e-re\x000e$Vz¯mË/Ý¤o\x000b[§¤6ø²Ôàë^ÚÓËRO¯?\x0006ýQ¸ú°@dÙ¥CÎûË×·7Ç9Í\x0004I\x0010GR¡aRµVú\x000f¦ñ-\x001dr
¬Ï_]ô@B Ú{!¹äQÓZ)Î\x001b¯S¶æ\x000bw±\x001bÒ§\x001f|÷ÃOt \x0000	wÅ?úõê¨jµÎH\Ã\x0015ªáGâ\x0002\x001dâ\x0017Ìnþ'Å7úÏóã²Õ
CA\x0016}Ö!ø$iH÷ª\x0015bÅ)7*¿x!Yð\x000fó/÷\x0013\x0019\x001fø×èsq}ûáÝÇâ*\x001e\x000f5!·í¥2[+-û\x0016í.¿úúÉ³â(\x001e·Ä'\x0018Ø\x001aôéQ,\x0000\x000bÕ:9X4î$\x0014FÏ{\x0019t x÷1Ä_.)Q\x0000$i'pûãå==¥Ð\x0000¶ÎE
©°º\x000fò^ç!rR2õ·³ç¯^9
I.\x0018B#\x0005Ú³\x001c\x0004»ò¼sü\x000cFÏd]\x0016Y÷u 5ÕH{ |\x0003rWÙý~ 7áû\½Á| tK§+Ñ 
g()J\x0008!fS\x0016eEÐS	î\x001c[	\x0002è³\x000e!h\x0016í±9\x0018\x0016_³I2jPÕ\x000f@è\x0005ºìBø­Nª3tõKÉµ\x0011m\x0007Püäo¯þ\x0019aÁQ¢Ï_n®þýÝ\x000fÇ\x0019+;£\x0016Ö\x0015V0-¡¿Iî*äÇ5\x0004¹8ÿG½°æ\x0008ÈYq0@ÖA\x0018I"Ö!´ã¡ªtYÊ9Ï\x001fVAÜ¾~ou ë\x000cGÔF\x000e`sñéú(_\x0015RàUÜ}ÖétRÁ^þxçær.^<¿çHp8\x0018¦®Z§\x001d8Bà\x000eDÞiUQ$»³Ö-£â#( ßK>\x0014³8½CùL\x0007×¢Yk\x0007gÃ¾ýá§\x000fÐ
¡Oá+Ø\x0016×Ç\x0011Ñ%°ë"õ
\x0016Âßìºùksa+Ø\x0014Ï?\x001dÎ1Ð1uLk0¼æg_ã­Zo¸£øÒ]ñÏ¿þðã/\x0014Õ@\x001a¹S5èùèýõíç«ÏG×$¡\x0017/\x0016¼ú\x0004\x0016Mðò>\x0010Ìâ2{qòèéóW/Ï_\x001e_	
âbôé¢[/Tj4:\x0016\x001bYÒÁÂ²II\x0007}ÿ¡ð;®4¤àÏÃ«÷>h*ß2S`\x000bÃOÊZÍoÕç\x0017Ïî{Ï_ö&þ¬FÍ^Êi4Ç8¼ÖRN£Õ<Ò³6þåOï~ýYÜ¤gx\x00128~\x001fê¥_\x0010& Z¼øÕâ\x000fØ¹u×{®òÛ7\x001fß»È¦@¨±üyY\x0006ÿå¤\x0002:Dam¯
û:yJÚË2ôÿî\x0019»ÜZôHtÿØZ\x001er-zô×áDõ¢=üý#Û¼}óñ_t[ ²Cm¢j\x001aÈõq§ÇÓ©=ø<&H>s'º,çG\x0011ø×·þ
\x0004S÷÷2ü
\x0002Ý÷%Â I¥¤Ùk~§+F]S\x0012±óÍ_\x0010\ Ò}öè¨\x00195\x0001é%JFYáL+SLÔÄ\x0002(ÊÁ`+Çyø\x000cÅúd\x0016éÓ"5AVäJ\x0007!\x0005jÞ\x001ey\x0004Åô°Þµ$Iª1¢â¢ä²¡øî.s1wþFVÄF
bß\ø$\x0012f6\x0016S¢6\x0013±&I¦lQôlÏ©S{ÏtØ&\x0002Rx\x0013v/Ékbæo¸2=ðw­K¬=,¼Mqå\x000eÖelÞüðã\x001fÞ\x0011\x0010ØÙ6/ã%ß¾½úüùPh²«bvGNd4Ù;1»í"¬4|SþÁÿzuþòå=ÎHÓCQxÁsn.çW²·²\x000e¬ÅDá}2o~zKæ9\oúÀ\x0002;\x001eI(Ë£×bòöÊø$¸piÝ\x0013F\x00087ïó?~;I­sysüY3S©\x001e^Ô¨h\x0014µwôÙ\x0013ÂÙÅ=¯mX\x0007Ë>+\x0003»¦ÅmÑ.èQ/R\x0007_4\x000eè\x001e\x001c>[ûÕ	a\x0013ÎVsAÏ#\x0014«8U,Î	õþÁ/ßÜþû£'»ª\x001c3ü9»yó®øGímWìGI³Teÿ¹È^Ä9Gg\x0017_=)\x000eá³Gå¿| ì\x0013üé@\x0010¥\x0005wN^:]8Ò:Ìë-F\x0010Û\x001dÖ\x0011L­\x0010s&àÅ¶%(\x0017tØ\x0000OG¹k\x000e²¼	 LÃ-Rð\x0005Á¶UÐú°«\x001e\x0008Ñ´e(6Wâ\x0004W/©YzÑ²k\x0004\x0002ÔfñY\x0010| 4_cx\x000c\x0008\x0012àÀ\x0008\x0004hËâÓ1\x000b­!vá#nÈ
ÖwÄ4F\x001c\x0000Yp|: D30)4ñÍõTq\x00085\x0002\x0001b¶øt@\x0008\~aRq7Bb\x0008LÆjÑ\x0015{\x0004\x0001kU\x0017-\x0005uÊ\x0000b³¿ì\x0004ä97nÜ	Ð©Åg\x001dA¹	e\x0019µíx\x000e¬I\x00088AÃQ£Ï:\x0002«VRHPôgbÌ¶©¼Ý8	ð}T\x00173\x001a+or%	ßeé\x001aÍF\x0004p{T\x001f3z6
\x000cÒX\x0019Ëµ)Ë0ïÿ0\x0000\x0001ºôé ä\x0007ïnUu\x001eÂ(\x0010æÕP#\x0010@Kºtà¢\¢¥ \x0010ÚB¤­³\x0000ZÒ=´ éÇ³-GÄ\x000b\x001c ,{!n\x0000ZÒ]´d%\x001b±Ì\x001cVX®\x0008@KºZôÜd£¹&¨ØÇíVsÁø\x0011\x0008à%ÝÅKFª\x001bÊ=­äHzt²à{ZoÜ &ÝCLeÛ±°j\x0005Þ	b«/UdF\x0010t\x0017/©pÊs§ \x000f\x0008F\x0010¸m¼(útÌt§2ØÉ9´x öÛÁL\x0017/\x0015&àFÙkn®uhfë6\x0000°×L½<\x0014ËÝp$Ô¼ØXÒ>lÛ\x0008¸Uè³\x000eÁ'iùgÌî\x0016×M»\x0008À¦\x0017qÐ,F'\x000e¼sR°¿ìÞ2\x0002\x0001¬dzX)e\x0011Ë5
Õnv>·Ä\x0010½í8@>\x001d³\x0010ø½\x000c\x0005¦fç¤`VEµ\x0018\x0011ý Ï: ¥zB.FE 'µõ8L\x000f'a+FÎ@Ì^f×¼HRÚ\x0004\x0001¤dºH©xðìÈ¦\x0018Û\x001dÝ
çOí\x0003\x0010:E`åýG&%éV°q§Ðg\x001dBÒ°*5·v\x000eiíLÍ\x001b\x0007ÛôéZ\x0008n÷à¬IÐyã:l\x0017-!ûDÖ!Ks÷ÂÍíÞ¸\x001bQxO\x0003©NC3T"/QíTÛ.(h\x001aÑ§\x0003\x000eéØ	'\x0001:\x000c!lsdñJAu0\x0008dÔë!³\x000cÒ>äHfµ\x0011\x0002Ñv\x0011£I\x001cÓ5°_Ùy°IË\x001d¹hå5\x0002AÞÐÖ!èÖ¤;«$Á%\x001bÚ,¤¼i7¢Tîë²¡ÚÅ-ÌNe\x0016DQ¡6Ø\x0000\x0001q\x0000útì\x0005ËïÅ¡Oü8£âÐoZ\x0008õ£Ï*\x0004?åAØÍV
)Õd\x0002=äËæ÷?Øw¿Rù%Þ?ðyxysóîèsG,ã{Vu°SYr³\x001372><»¸x²>¸×BÁ£4±"A\x0005µ±âÇ/ºEÝ?´~÷óí[z.eEW7o?óxMq"§PÛ\x000eÿ&¢$î2Ï_x|~tð·ïßýDÕZS?Íõ\x001eu^D½²µõÕ´í¼ý°¨u\x0000Þ==\x0017¹0GÑ4rÊ¶FqÞî©\x001f@k¹.<ì¶6Ü\x0018±MÆzþV;\x0000@b®·¿3S7*Ô§Zòáý\x0006ÆÞë³?5®(>
w\x0003^¨oÛðÒér½éI:9\x000bõ"§µÐv_kkÙÓÌ²µõâòëéa`ÃàÒ¾ruð&ÑÝÀ\x0018íä\x0015#(o\x001a^\x001aUL~\x0016\x001d\x0015ô¯nã6\x0000Òrý÷GdçÓïo\x001eSf´ÎÛN´ \ßýý\x0001}l'ÕÔîj\x001b÷H¿ÉuÝIÝÚÊ9×::J
B\x00017mÁÖ\r\x001d@d¡\x0001j)\x0019x	hôR\x0015Õñ¥d\x000f÷IßÖÐJ{ZòÑa\x001e«\x001a\x0000 =#×õ¹_\x0000\x001aÈK\x0015Õ	\x0001Èá¥;äºN«\x0016=TG/kºöuh-!õ¶ùFë\x0012Û$S	0ñK\x0012z8È\x0006ÐaÛüK×ÇuuSÕ:uê ÒÕZ\x0016Ön\x0013	µ\x001eë\x0000"*\x000b|ÊB¹¦õèÕÛH°µs\oXáZ?«5ç´ØèÀ©7\x0001Öë:Ý\x001aå»Æqëd= ñ[\x0000Lm\x001a{úûyÞS³Ö²{ä\x0010xµå\x0010N-\x0019×\x001b1ªÖ\x001d²\x0000àkÀL\x001dG½Úr\x0008¦þë]\x0017ukìk[û°©\x0013¤ÝDS¯Åõ\x0015\x0008MbØf~5q:7õã¸å\x0016ú*®«B§©Ã£á\x001cn\x001fòû·XS\x000bÅuYñ\x0004Ç+pO¹À­8£nGÀl!©_âú\x0006¢Ã÷À\x001bÀ¶4Í´§Þë­#3ò«\x0002wDäñ\x000fn1¦>ë¶èÔê!7!ªâÔqÓ\x0016h=\x000f×Û
úÖ\!¦Sca³É\x0014\x001a\x001cö´54r
ÅÖä4Æv\x000fm\x0000¤á*&Õ@Î\x00087ÛÐ­ÉªÚ8¾ô-\o¡\x0018¥qSVxJ¯ÃOÝ
Í¶
 =
×¯Á$E	Ú%J\x0018"m;\x0001Ò°§o2k;çb\x0013i\x0019ßH¶h·øâSïÁuCÄCr ÆAZý8hQç5\x0000@\x001a
®wëñ­I0¨,©¦àÔ`p76õ\x0015\\x0007 X¤\x0000(\x0006 Ü4\x0003Î\x001eëKDZ7×WjµBÔMG µ\x000bìi\x0002Äúæ\x0019\x0001i\x001e¾µ*sÛ8°u\x0006\'Ú\x0001hc#ãë\x0016paÓ\x0011h]\x0000{zÿe¾\x0005ÑY½áÜÊyBØ¶\x0002ÒñoÝ\x001bJhj\x001d²jG`Ó\x0011lÍýÖÝAÃ\x0011):\x0001LªÝÂ\x001bO`ëã·NÂ\x001ddL;\x0000M2i?40¾ôìëé\x001e(;Ðv\x000b[ñ\x0004
¿	ôè[?®\x000cÃ5TA¢áz
F\x001b·m\x0005¤!ßz@Ô·\x001cÞfù=ÀÖ^9lZÖ|o½ïªÈÉ\x0012ÒÛ8 õÙ[ïæ#\x0011)²tÎARÙÛÑÖR¯ç\x0016´ì)+ÍU\x001a±m\x001a^çõ4\x000eÊ¾=\x0008(v\x0005U[e7Ö(o="éX®«\x0000Pâ*+7ùb­)Þú\x0011\x000cÓ9mðÚ\x0004l3D[
cOHN\±ú&Ë!¹æ\x000bn"a\x000cSÝ­\x0003ü$H-î\\x0002®#ì\x0019\x001aÛ­\x0007\x0003¯ú&\x0019¸Ô¢l\x0001¹Ü&;hêa×\x0013\x0011sÓ\x000ep¼\x0005ngpSTxêW×Ó¥N\x0000\x0014\x000eä\x001eÄHc\x0015gPo!Á©7Ý\x001a\x0000\x0005uWÏÎH\x0012áÀ\x0014/²§6të@ëô2\x0013æà Y¼yÑj©üÖqnm|\x0008'ò\x0002xtªg\x0010»\x001dã\x0016\x0016Ë­¿)\x001151	j-\x0015Ý*nY©\Ï5Àëo³´v.P;~à\x0008þøëß×\x0013
Ï£Ëï.__~¼¼GË¶B5*kb+®°Ns¯¸r\x000fÌ+\x001b\x001e]<:{xöììÅQ\x0018ö\x0017_×^\x0013`\x0002ª­¿¼¹¹GÛ\x00015n£e­²ÒëÄL­F\x0016\x0012Ø\x0005ÃÅB¶ê\x000eëw¿{\x0005\x0016\x0018}^<zyûëåq93_(ÈsJ{J\x001c´¦¥nê8oîùôüäÑÓ³Wÿyöò(\x001fÞÆë|Oó\x0000DË:PÒ<~ &RÓ´b4¬^ÎL\x0004:ØÌ@@máÅËã*îöGuIRMx¢¡Ï£ëÛãJ8¨¸\x0015³\x0014Í«9i1eÖÏ4v¡öðèù«çÇ÷A\x001bÔ¡ésÿà\x0010éb\x0004ï¥,úm¥òÙ,Ú­Ü?öåë¾ÿù3~8*ÂéSæþ/×·\x001f\x000b3\x0005\x0008Hî®lÂ²ó$WQ-åÂÎNþòüÕ³ãËûöúÃåk:ÔÃ§jôc\x0010²J\x0002\x0013H\x0018ªY*IùÖûÏÌ¢2þ\x0005êÏÄüó\x000f?Rr\x0018Óçñåûã\P,\x0002\x000b\x0019iÔÂ£%7?\x0013\x0017· eoç\ðøìé}40
\x000e\x001cÁ¡èíyðâ\x0014¶\x0017ºÄy\x001fâîÁaã³68'¨ Ö¸Å¥ù}\x001ccÏºÇ1ÏÊØ^Êàm%Á¼ÞôÃaãsÿàºlõú0¬u¶§\x0013­ÌúBÔ¤{pXáø¬üòZ¸C{5CxÙo¦\x001da\x0008|V\x0006wÒäNS\x0013^'¡pùåÖlùå\x0008Aàsÿàh\x0003\x0012y³kQ`sfÚp:¶ÎÁ-°é³òË³áäx­oí}MM\x0007Ãëõ_üxùÝ'²y\x001cl\x001elö«×÷]ö\x0001ÍÄ¸¹°NM£YOáa^¯¶\x001f÷]öÿúÕ°¤$\x0005o>|RÊëû$ßÁ\x0001 ¸\x000fmü<\x001d\x0014oÐJyxÏ3\x0003\x0002I«Ú¦\x0007HàÙ(@L+¯
ÇÝÖ
\x00038æë8\x000cç¨CÑòP\x0010\x0017\x0019Å¦è\x0001òñÍwþýgò\x0007\x001cü\x0001Ø?èûquóæ¨Ú+ãsÑ·E¾v_EvXf¡¦\x001fç\x0017_=?
â&§¨uTq¶°?Ëçëë«ãÂ\x0016µµ5YÍ9/ZSeVØ+E6ÿàëç\x0017ç\x0017Ç
°_õ?þ}©¾\x0012E¹ÿrÕÛú\x001a*>÷ ÐNÒ\x0014,?Wâïq²\x0002Ý%N¾O\x001f2wÙvPeäÄ½OÊÔð	J
m\"ö£pðÌè³\x000e£ÜJt×[Î²w\x000eú\x0015Fá2?\x0004ã\x001féæ\x001faR±ü¿gÿý_7÷©ÿ¡\x0014\x0007*U¡«ÊÔÑEi\x0002S<Ù~xVÆ~yüL|\x000eßû\x001f?ÓvôØÐöÿïÿú|¼\x0015:ô\x0019\x0002FÕ8@å4lJ&Zç/ÏseN¿ÿõêÛI\x000e\x001a+Ü#Ë\x0013$e©£ÂÔÑK_\x0003íô<BEm\x0015ÿôÙàµ»Èý\x0017\x0013¼©Þé\x0010k5!ÚºñÐJm\x001aºö\x0015Y\x0019:$Í,ò\x0016Y{R¥Ö®+ø¸eðÚÇ`upñÇËÖ]\x0019\n¦rròøàSGµák¿¥zî5Û±\x001c{!`7ï¶2üwo?|øþ5Y&¸ñ\x0011Yñ£JÅ\x0005r#ºÂÅItÅ¥Ä?Ø¹<¿èÿõ¸\x001fþãü/³
¢÷ÕñxDÒQdå ¢f\x0019Bë\x0001ãÜ\x000f"=ïóãÇîõ§üÙÖÐ(\x0002\x0001¹\x0006\x0002^ &rO4,\x001biå\x0012hâ#RËjã¼	wá½\x0017\x0008|u\x001fýÚü9Rt,â\x001fýÑî9úñ.,\x0014T\x0013bH­}b÷þ|yÏ\x0016ÆEb\x000b}î\x001b·0\x001b'ÊZWLÓú,\x0011£\x0013­Õàz\x0007~óécúú 4
Þ7\x001f®~½ü÷ÛÛã\x0008àôr\x0004¦DUÕ^C\x0000¤ÃH¹{\x0002pqöõùýÇãW÷ ùùóëw1Ñú#\x0018U\x0015»¹¾ýxN4ÜÖ=qÎ\x0007®ã5!Ícb\x0010+ûðÙ=Ñ\x0000}ýë¿ÿMçÀã\x0010¿£¿ÔÇ«ÛÞc$-ò/¨#à&°ÖrtÐ¹4c£¿£¿Ô³óW?¾\x000fg(\x0010À§\x000bEæÈ Ã0\x000cg\x001aùdÁÀUO\x000fyohï¹¨8 Ñ¢®z\x000c\x0002b\x0014øô@p;]ÉI´&J\x000e¥x\x0017\x0004\x0011\x0003|z`T¥<¡FVÒÜf\x0016r\x0017\x0004,O×lÄÚ}Êÿ?\x000e\x0019Éà\x0005±\x000eÕc \x0010CÀ§kW(æ,£j\x001fÍánd¹n|\x0002|z`ø&aÔÆÄgDp7í6ÂÛD.\x0018û¶\x0018z°4LRFv±[w\x0006^TèÓ\x0003Ã8QPSAzµ+\x001dkµÐt\x001fC\x0001Â\x00084k>%¾íÏÈ¢Ùx«Ýº3¨L®¹ÐüÔ\x0004_1ÄÐ$ÌÓÇ` ÄO\x0017;ÑdgÁ]=ã¼3Dp¶\x001eW\x0015ôé\x0000£²ÎT\x0002ÙÈm6ÔÆEÁSÅ\x0003útÀPQzÏ¢íÀ)ïO%\x0017«5[	ÔmèÓÅã#þøÃ0ip98^b¶]'P0¥Hhç\x0016-÷)·K+¤!ÜÅùxèJ4¶A_[\x0007@\x0004\x0007ê?xNO\x0014+¨
Ý¿yw_³\x0012ôLáJ\x0005~2ç\x0014§{\x001bRû¸óäÞ~%
QX"
<¢¸D\x0014ÿxDy(w#²XÇ¦}Í7`qæ=
F Y¥æð×^H¢\x0002C-s¥6Iv+"½D¤»\x0011\x0019¨¡.W³~¢yÆÁ\x0018 ³\x0004d:\x0001ù\x001c¤&E§ Î¶mÊ\x000cÖÏK\x0013Ç Ù%$Û\x000b©à\x0008!¹¦n¯$ðe\x0017ÂcÜ\x0012ëäP¹]cqÔÒ\x0013Z\Æº°ñ¸!²½ÔK>LR+&2SdtÑÚj\x000cRXBêeI\x001f|ã$%\x0004\x0015sF4\x0001K@½$é¡\x0013\x0019\x0010Òl\x0005ô ³ÑozY²0@ìk}kæ¯	"èjãæeÓKÔ½,Y0ñÅ#4wñ+\x0016°ÒÂ$\x001b´¤\x0000ÝM\x0001S\x0017;7Î\x0006ò¢\x0014d]Ø<IK\x0006ÐÝ\x000cP|]ÎØTå¬ñ²Ò[\x0011-	@w\x0013@lÕÅñ?åóÌö[¯[½<ÿºûüG©q¦92¼lYO´õ¾ÕK\x0006ÐÝ\x000c|Ëé	"\x0017»D Y½õz+q\x0001)
\o\x001cd%û_3$Ó ÙÍ[iIJºÒtÜPãdL%·\x0011Y\x001aJ¦×PòÐãgRBO\x0017ÞÝò\x0008dUÚzá¥¥dº-%è&Õ\x0011­Ã)\x00137·çÕ&o¢%InôÃ_\x0000yV+¼-:õ&oæm³dIÓÍÁJy¥ì\x000c/[\x00144Û-n³¤IÓM¸ÙNBÀÁò,á-¤B
i«Ím<iºyÒ[!%¼±\x000bWf)l%\x0000³¤IÓM^É­¢ta)TüÍË¶dIÓÍ6\x0004ÍÈ×k\x00191§!Hi¹¹S¿	\x0010XÇÈªªeÁ&ô\x0019v[)À-ý\x0012×ï@ÎÆ±é¦8Ìâ­¨9\x0001[\x0011ù%¢îãf\x00147"V1\x00038Ñ´În4KÜÒtsÝ¦[@\x0012\x0007ÜhuÄ6<
\x00157\x0012[n®ßtK
zå4IÞU®\b(¹­d\x0017N\x0000þÚ»n¡\x0005&¤=!éE\x0014\x001aíÆãæÂ\x0012QèFd¤\x0001 \x000cÀ5FëÊÞÞjº¹¸\x0014G&Û»)¡¨T7w#nm¶Z%\x001a]ï\x0018o½!\x001cM]­·$½\x000bGµ\x001c©´Õ4QwQ©~T°ÚØ÷®Â/¼¡$0låoc¾}ýîÓ]#\x000eÿ¨Æ[n\x001däÈ4\x0003óí®3q|\x0011=ÚÌAm_P\x0015CÄ÷_\½E6ð	¢ð÷(¤ÚlX!Ëf¼,s_I×\x0014B\x0017MØ^Sbð	ñg;%03\x0000lÊAo®Ä	R©ìæo\x0003Ã°ì\x0012\x001dÕÚD\x0015X\x0011\x000e\x0015á2Sýä¼^d\x0018[\x0002s#ÀÐ\x0016z(I\x0006«n*C6î1¿\x0004æ\x0007\x0015Æ6®(|«Ï¡9¶Ã\Ü\x0001,,\x0001`)"ï0ô9æÒ£hdÆöÀKXqd¾Â© J­3%\x0017(\x0000Õ<\x0007r\x0018WZâJ#Ó\x0015YÏÓ";Ö;.×¥=;?/å\x0001`ÅÑ¢­c%÷ g+2¿HãÚ\x000cÌ«\x00050$Pu\x0003\x000bÞDPâ\x0002RV8\x0003\x000b{-Iß¾I\x0012
Ê9q~µi*Îóªq-9ßp~¡
Qghm
,ÑçX$á\x000fãZ¾\x001f!ýâ\ø©f=ÈÖoÜ\x0016ÎÅ(°%éû\x0011Ò·
zWþw$_¿Õr\x001bÝ\x001e`KÒ÷#¤ï\x0014\x0003«\x000fóJÆ8i_ïÙaKÎ÷#ïfÀªáJM\x00149î }¿$}?Búex\x0011I\x000c¦ÈD¦s¡\x00129\x000clÉú~õåúX§\x0010­åë(f1ö¬äõý\x0010ë;N×wZ%.ä+¬/Zz\x0017%ë\x0011ÖwÔÀëHñR&N®1f\x000f%é\x0011Ò÷sü¶íeÂDþÊì:aÉúaõ­\x0011xôS\x0017Ö3îÁµdý0ÄúëT«p¬\x0016`M½Xí ×°dý0Äú®·5Ò#u\x0001l©\x001f¬\x001fFX¿\G\ä	Ö×þ©¯Õ"t2
lIûaÈÔ7M\x0000\x00148î\Zë=[lIûaöËMóÕ\x0016RÄ\x000fÊ5¹õÃõÃ­ÿ;\x001eÉ¸äÖ8Â­ÀõÿQ÷fÉm%I¢öV°¦Å< 
©d\x0019E²I1­«^dIJ\x000eÊL=õ6z\x0007÷_Gï¤Wò»G¸\x0007NP\x0007ÀsPYª¶K´¤[Õø\x0018Oá\x0003í£\x0007îé>*?Á7òµlõ-²U³îöZÑ¥2SvÑ×Õ7
Vnÿî\x001d6@¥ãU\x001aàÇ)ËUKVß$Y5Å*p\x001a\x0000\x000fÌåØÛ)È×Õ7
VÃ\x000b&±ÓY0;AâûZ°ú&ÁJåIÀå­SªÀùàHúZ®úF¹Zf|hNîä\x0005«ÓSÚÀt\x001dtÒMA'ÍÑC£êx¸Û
¨ñH»ÊlÅ¿\x000e\x0007¶5©<!\x001az6ÃÎOãÝ\x000fí+ymTØ0ÞCBÇz\x0013cÓ&zÊì5\x0012»Æ±wKm\x0010\x0003ÖÑÕ\-§^HJâÿ\x001aÏöQQKöº­\x001e/W¨\x000e\x0011-K§\x000e:	Ìkjh³^0a'¨G\x000c¸w¹t¼·U×Ev"\x0015/àvã\x0013o\x0005Ö"ð¹\x0001\x0001Ù~@XÖ³§V\x0015ê´bÕiÓ\x001268°bùø®3E(1`åÇK/SÛ9¦ÉÎI)ÿy½\x0004¥#£üâõ\x0012ã
\x001d[{¶ÍÔÅ¼Ç²/ÖB¥§f\x0018/(líAÚ6\x000fÒ`]\x000e¸µz\x000cëàÉXGRz÷[6<üENt¶M\x0008»M\x0018§°§l¦
;U+:ÿ^\x0010rÓ\x0004,Ô=Qü\x000fÙÏ¯|v·|½Z~X¾ÛØ¡ÀaÇ \­3¥wr_o³óùëÙ«ùËùá»hì:\x000e4©Ò0\x001aC­¤4Ý64_ÛéËÂ¢
\x0008¤pjXQÄ\x0003¾äKìãøyö~5;[Þmé \x0011
W^j0\x0017¨7%á\x0015lÕÈ:Í^,fgóóÅÅ\x0000 õYÊHËLRqË}µ\x001d	I;É]\x0005b·Ë0$øåð\x0008uR'ÓãDJ¼Ãm\x0003¨ëåìðîöñ{ãP({*yBÔ«ôº°¢Nè:ÇÝ\x00036ìüx~zù_»ñLgÚðÊÈ(
òhhÂ{¸\x0014ÆÑÉ S\x000e\x0018NÑÄ¿>{yûø°\x001d.ï\x001fVw \x001fV\x000f³ãå»í1p»$z'ÈXòô\×é~yzùz1;_¼^¤X¼\x0006Ú]°Ò¦ÃWv\x001aþáNÝ,?­f/V×³óÛÇÍ\x001748LÏâ"ªUn©â
o²ë¾Ç\x001f^¾ZÀ*\x001eÏjÛ%:ïp±õeê^\x001frQ\2\½\x000cù·ÛÇSy\x001d&Çp\x001a?Gj|2÷(¿k]óæâÒeÖ¿^\x001eíÆ5flÆD#·L×¨B£§»¢Jf¯ã1uH\x001d²ÂÚ"
âY ¦!³ÔA
îÍêns\x000b5ç\x001c¹æ\x001a;ªç$?ã\x0014·íÂjã5\x001fv\x000e¥6jpm\x0016çÝ>j\x001bÑ:4Ã-[èl,\x0013ÀqòO¦+yJtG.|K·ymH·£8wø¨d±ÙéÍýnÁìáìQ\x001e"&"ç§\x0008/ãºª¥ûlùÃéÉÅ\x0000ÑÌH®ä\x0006#iÉy"Ä\x001c!ö KqDw¡Ìúõ-%ãàëÛP¦@½*±ì®(@-Õ=[\x0003¡À¯OçªXÛØ¡
§\x0019Ïá(Ý>âµ<[ýy\x0007ÚæC\x0015\x001dsÉly§SåÊb©î`U<K§x#Ï\x0016?\x0007[msývfÃcÞaÃ¿6À\x0005a8ÍNH1<ã#\x001b¯k¸\x001aà¤Ì}ìÄZ!gøWR	Ë¯ËëÍ7\x0011³%iò7©\x0002¹À.!çÉûoõÁáü\x001fóãÍ-Þ*\x0019kñP|\x001dß>¾½[~x\¥\x0015»^®6+*/ÑÃ4åäçr\x000e>&st\x000c·ãÓËççó´dÇóÅáæ\x0016\gdmãó\x0014\x0014½$¼Ò\x0017Qùn·Ø&>mSçØ©gÉíY[K?]}¸ÙÜ¨ÏUákÜU£<7æ	T2 öÙJ?\x001d½<ÙÐ²\x000fûÍÇ\x000fo\x001f~C\x0005IáÏËO«å#\x0002å\ÓÕÝÍ\x0015v\x0007kìYú/!Öêêÿ8¿\x0005\x001fëzð°_\x0018÷
Â	´¹ÊZ
\x001e\x0001.ãÐâè¿þãü\x0014\x001c©ãÅ³\x001fç¯\x0016óKäÌY¨\x0017ó£^ò\x0016v\x0002ÆÒbÌ*÷ægcH¬ÄD+9\x001e³\x001fZø??£×VP°M\x0006£©i)¬-¥\x000f
\x0010\x000f{][8ø36Díe¤õVî\x0016»\x001eÆIçaã\x0001³ym£ÝþX%¶uH\x001f£a\x001d¥ùÉ`-Yú°qÜãÒJ±¥Ñ·+À£\x00134þBJ®oÀ\x0004¾°O\¸z\x0002.k\x0001lEM´$,O&û¡ÅÙâø1Ö	îm\x001epØ¤³À\x001dÒ¤ânGûÁÅIàbÄµ\x001e<eÐt?\x0002auÿ~hql¸ q½"e+\x0003¶OçË\x0017M×~pqÊ¸ r1©<w{÷Ø_\x0016Wó\x0015áö¨\x001f$¾\x0013¥±´8-Ï#ðÞÒ¬x´4\x001c\x000f¤ØçÉÅ¨kú\x0018}\x0016¸ô "xq×gAíSE \x0000O\x001f\x0013´¯§¾t' ÃÙ¢\x0000¡ü>m\x0005lþ÷,}>¹:sHï¸YäÁ\x00181¿ï\x0011\x0017U "Ðm!\f7áÒâ
ã÷z\x0016PEÈ	*\x0002hM$ZÎè.®Ù§\x0010ÃÚÐô1å(¸B\x001bxmUY\ÎÿÝ\x000f.*49A¡aËXE¸¼lÄ-´{]\ThrBÃa\x0007\x0005Öó5å$Ä½\Ôgr>+\x0018j\x0008Ák+ËQû\x0014b
5 !°e°.¸O®,´ûaØ`$}L0\x0016¢,´\x0017W¬Õ¯Þ'.j\x00085ECp["ÀuÅç1Ü»QX±O³\x001c\x001fØÒÇ\x0004\c
nàÕeØ½:hØ"$}Leíë=6ê|b7QåûÁE«¦\G­\x0013®÷[ÜãE[O{àþf!\x0006ÿÁrÏã8·{<\x000b
¹ÒÇ\x001euPmÑ|ë¬ïÑ¶I-·ô\x0014õë\x0014ê\x000btüIÇ¸ÊïQ,¤v\zþuM±PJu\x0000×spAý\x001d\x0006+0Æ?Çòb0Ì»\x001e©Ü\x000fÃ¹\x001cr\x0014nºÁàí½}÷HÕY¹&ëðãêÓÕÍìxùø5íÙé0¬\x001c_0½#å7H_\x0003üêQe?.^\x001dÌp¼æbCË\x000ek²ÒG#U)¶(c\x000cBÐP\x0001\x0011<A\x000bÊ#ÚNö\x0000~´ÒY\x001c·è0î»ÀtL§ûdi;\x001cjüh31w´\x0001:_F'­ë\x0010dès´ÚéPÙãG+\x001dÎÎ°ÎYC!ná1A ãi»ÅCõæ6âÄÑFiñxð54\x0007^½½Ð¡6ÇÖsMAu¦sTY#Bn1\x0017¶ïå¥\x001d\x000eý%üh>w\x001aí\x0004\x0007·WÒÕðdô{Y;tðc\x0004\x001eö\x0004!¼Ü
\x000bðxcc\x0016i§CiìÚ¥±ÁW5ÚY\x0019¨x]àm`<³\x000fqe\é£\x0015Oæ×\x0013Ä³i<fºµ+DG¯ïaª\x001d\x000få±\x001f!q(\x0014á\x0005C}ÅD \x0004g{Â\x001fít(}»@Æùéö\x0016\x000f!]\x000cl-HÊLíãb`fBúhÄ\x0003S2uJ{«)(0
JxªÇ\i§Ã\x001c~´Òa<+ÐÖ
r\x0005\x000bì<Æ`:\x001eê\x000b?B_þ\x0017¤§¶&ÂGa\x0008OìÅB>ZW\x000f'L¦VÃê±ÔSNôÚñ°wúhÅ³2öhHÔ#á\\x000eV\x0001^{X½ÔX8}|gOá\x0016¤F<ÌËu}8KJß%ÇQCp^îÁ\x001eP\x0018ÇH\x001fÍb/é±¼¹º\x0008eÏG/ôÅÊéÊHªÖÅS\x001akÂpñp&;èè\x000b6ÓQ@#\x0014\x001a¡ØÞP²BóE¡íA£­G\x00045/^ Æ1ByG%F\x0012?2\x0017}±º\x0011æÀe6\x0008c®ndÁ§(<'xJ".`ØÃþ"áÛLø¶ÝâKi\x001d\x0010GËç\x001d\x0016ìh¨Þ\x0017¦â·÷>Ej*[Éü°üeRä¶Sakö\x001a!°&duü\x0019\x000büò[ûÃüoùån4S'}\x000cÅ\x0011\x001aù	ßCÂ\x0002®\x0007©W+ú|¡8\x0006\x0002ÒÇP\x001cL"
´:2O\ÄF¯\x0017G÷ÜÊ\x001d4þç÷o¯îÒaBÇ\x000b?^/SMÅn<dñê¤¢\x0017J0É\x001dÁØçç¿o(§xÇ\x0006?¡¨\æ\x0004(6·ëK(6´\x0012ªÏk\x001e\x001e\x0015~üëQ0Ç9}|\x0007(è)¥\x001a=
ºEø1\x0008\x0005Ë²CF\x0001ëS\x0005\x000f/\x000f\x001eÄõøcæXúø×ß |pO\x001fP\x0014ø&ë{c<%ÊÀªäEX2X¾\x001dEáSAú\x0018¶A8­3Ûä £ØlóÊ\x0012J°aôª(ì9>\x0006\x001e[RÉpÀÀÍf\x0006\x001c[Í\x0011%e{tä@\x00143ÍðË,8Âà´£n\x0002RÂ2F!Û9¹jhè}¶Ùº±ðG%ù>ñyã\x0005®ÏV\x001fJsÒ\x0014\x001a\x000e xÅÒEö%"
\x0016ÿ&\x000e_\x001b{7
K\\x001d:v)Aºô\x00190[a\x001e®ÌïË\x001bªº}
#\x001e®îïWV7\x000f³÷ÿ÷ßÿs_¾ËHð$%f`Å9M¯ÖsádÇq|úúèâbñjqòzöbÓ\x0015`Â\x0005uÿ\x0006 \x0007ü¿\x0001&\ìðÝcJ&\x001e\x000b*J\x0017*¬y¥F\x0003ÒÍ\x001fbp}ö8P4èðc$¨ VèàÖ(\x001a\x000b ¹ \x0003@ì	W\x0002Å­I\x001fã@§f¡\x0012\x000fÍ\x0004F{ZÑ(b \x001a\x0003ª0],}\x0004M±\x0013(ü1÷$\x0007Ð<o\x0002@{UÛ8P-Go=(\x0017I `ÅR¼ËhÍ ¥Òr2(\x0006äÓÇ÷\x000e#<ÒÇw\x000f\x0003ÂõXå <ì@\x0000DâÌÉÃÈizÌãq8B\x001c?FstrZ®9%söÕDãÄÐ\x001d~áÔ1Fj\x000b\x0013\x0001¤hÔ}>ã@1|¬GJÑÔùÜ\x0015Îh³`îKâÔô1\x0012S¤XwÒó\x000b÷t\x0018*ûRÇ¦ÙÝz4höyqAyv¦Ä\x0019\x0006´ eÜütN< fô\x0001Åh\x001f§K> ÚÊ\x0011+zBm
 öý\x000b]£þjõ8{qõ­WÎ\x001e¹\x001dtÝÁ+Í»"U	Ð5
\x0014Ò>ùy´¸½8Âö&³³Ë¿\x000eÄÑÿ\x0006pÓíHL\x001f\x000frC\x0011â\x001cU«$YLÊ÷vã0ÉE\x001ai9\x001fQ\x0004l`I«\x0019Y(aRÉ0Ó0óôñ}n{üúÇ×øåM\x001eÂG/\x001fÞ>Þ­°sØ»wÜÅ4\x0007\x00043
\x0014F\x0005©6[R».Àï}ý=½<_`\x0013±ÃX¿~øóËÇÔt\x0001+\x0013ðg\x000e_ºâ¾J×Ë«\x0001ï3ÁÜ0X`I+%õ*Oª\õ}àÇû,\x001dÏ¶½ÑÜÇÛÛ7yþRºD	§gËkìU1ä
	¯I¶ßp8s\x0015)\°$Î­ì³ß(Õôl~ý+\x0006!âï>\x0011Õ8M\x0008\x0011\x000f\x001cªâ¸Y´qKÞùnÂet¿ÿÊÓµòL­îM9\x001c\x0006i$èlÍ!©¸¥0\x000eM b\ßfwoÊá`PL\M\x001f£@£+].\x0019Ab§\x0012ÇL\x0003ýôk¼<ñ$Ï99Æ\x00168;¯³Âj_^Ä sm*K)+6¾Àþ1¶ÂÙ|Wú³ù¢Ó	Ä·Ì<\}xÜ¹T\x0002û%JêªáD\x001eÇ'½sÔ\x0007S`»\x000b|þúèååæåy÷öËçð\x001bT¾\x001dy\x001eïv/\x0014Vsý\x0005Ò\x001cU>àà¼8J÷Èºùå9,Î¦\x0006$\x0005ëi¥0Êq\x000b\x000f\x0010c¹\x0014\x0013ËBrï8¸JôlÕP\x0018¬ºL\x001fCWÆcòy\x0016\x0010.·±ï®5¦o\x0006Â`ªô1\x0010Fkj³#U´¹x\x001dV&8qrÂÊ \x000f>ÁH\x0015\x000ehapÈmÞ¥(æé+G\x001eÈb°ô)}\x000c\\x0018#¸¨AJ\x00076ÂÂÄH[Ç¾§í0ïã{\x001bM\x000b»\x001fÏïn\x001fßá·æ[Û"æíP(\x0010GÝ¢ý \x0001%Ïj\x000cÑ\x0007Õ£ýcï>ü\x00136àÚöÙ½W\x000f)Zâ\x001a?\x000ewW·»UàñE
¦\x0013§AYòXìò­]3¿|\x0005ëutº\x0011êÏ??¾»N"øl>Þ¸^}\x0018b\x000cJ2\x0006¥Á\x001cl\x000b:AÉ»¾RÀ¤,\x0017/\x0017\x0003ð\§áLR\x0008Ö\x0018Ê¤\x0019Ó9:Î6õ½y»;¡Ì÷¿~Í±{ìpóìÙâþÝíÃî\x0003¥¢p\x0018>%çÂ(PeÓ\x0011×Ý »<ÃÓ×Ò\x001a&=~úÁ4\x0006Î´ \x001aéóK\x000c*D¦}¹Ãi0Ä9|m0}>\x001b\x001e\x0012C\x00082Áh\x001f9\x0011'è3=\x0014Fb(<}\x000c¤Á¼VópÅËFó£\x0011}ù\x000cCip\x000cí³ô1FK²q\x0001\x0003-5hsã5×R©¾\x0004ïÁ8æ>\x0006âØÜ\x0002\x0000@#\x000e\x00063	Ç\x0004Î×Ö÷X³;pþüóWýöS2|Ð.\x001fîWï>®\x001ev\x001aØ\x0012Ô°umrA\x0012r>\x0014Û§¯ÈûóùÑá×Cð¡Æ6\x0012I²Æp±4\x001192£ïó[RO\x0003\x0011NG£À1¦à¥²}pÞ\x0004%|Fce_jÙ`"\x0016]ú\x0018$#¦\$é5x2#IWìù¾$HN}ºýåKõb9,´)±®¼P²0T\x0013^({4X\x0001\x000e@á7ÉaÁIÐ\x0013¹ó¹Äaí¹H\x000cû×3ï[(åÕq`<×PxéÀ.Ë]>±
Ýó+c­1\x000ceý®8l§m§8Ý\x001bûN8~FìSCIøápà¢ØTÁcQ*ut\x001cåîÓ\x000e\x0003IÊËà0\x0012ë\x000e\x001cÕ.Ã\x001d
ô.`\x001cÝ{×#h\x0006¢·¿\x0011uEc\x000e$6\x0014£û£+íú²Ý¢ðëÞ`\x0014)Ësî].ùöÄÞ ÕP\x0010~¾\x001bxd\x0005\x001f\x0014§JW\x0004#ø^õ	Ý¡$ü@7ø+ðæ8:h#JßÃÌP\x0014~\x001bÂÃÓ%¦ºY~\x001büè¦úa\x0003QÊ3ÛÀ\x0012\x000f¨	¾úJ:'®dÏô\x0015¼\x000e%áw´"_RàMº¨\x000eèÄò\x0010éû9ðKÙ0\x0012P~ºÈìã=î4uiÝ/Wáª\x0000V1üïÿ\x001bR
G¡í«}àn\x0007´rué{\x000c¡úÝ@¥À` \x000c\x0005\x0008I­\x0003\x0014×U8Ë%e½MÜ\x001a¸eÀp [7§n\x0001kð¢`¯²ÿ©}8\x0010·	\x0018\x000cd¢H±08\x001b¹A\x0008¢ÝAö\x0019R
@Ü\x0019 \x0001È¦>E\x0008\x0014¸?³\x0008FrË\x0002××±\x0001\x000c'Òªcc\x001e¢,R>D¢/0Ñ\x0000Äõÿm@¨ó=ð(®\x0016j\x001a\x0010×ü\x000f\x0007BhJù£¢fÔ½¼DÓ.>ù\x000f'RÙ*OÍ\x0011"Ú:9?2îÍÁ\x0018NÄ¥ý
D>uë¤ªyjua×ý\x001a¦àRþá8¹Ä»GD.âç{\x000f{×÷\x001e<«÷\x0007\x0013é\x0010(HÁT¼ð\·ßÛç©+ö\x0013YSX8\x001eâ)c}¦tÁÞ@ÄEúÃÀ\x0006$¬§\x001c=á)åù}¥!
D\?HBd$6Ì
\x0003¸FPÉ¾Ög
D\ß°FI\x0002%"\x0011ùÙéÀ"¡/\x0000×@Äå÷Ã\ê	ûyDÌ\x0001§Â{Ö±±¯%Øp¢Rqßp×dê÷:\x0015p3@¸k¥%Æ)*d]dß@úÿäm)\x001b
Q}±\x0006"®«\x001fnÌ
~Â\x0006«\²»\x000eâÎs½9ÛJ)ýpãQåtwê`¸³Ià»Ö\x0017i\x001a\x000eTªç\x0007\x0003%\x001e\x00020êxhdo¦Ä` R0?ü\x0014aëù,âZtáøaBiÇºÈ\x000f?D¨Éò»
>(QÓk\x0011¼æâø¾\x000eW»Þÿúåáî.ÅQà
­îg¯7÷÷\x0003JÁ^åN \x0018iNÍÞð_ÚtÔ½É\x0019\x0017³Wó-/¥ï¿üqsû¹JcÊÉAÃ6\x000f{FQþ\x0012O9\x0010Î¿Ô/½N\x000bÚ
U\x0012\x001a ¼Xp½ØNÂ\³\x0014zÎøn*8ª¿ü¶P%\x001f àÛÓPí»\x0017À\x0004pÈ'T\x001e¹"ç\x0007\x001d'ÙcÙÁ_7\x000cÖ©h$\x001aêéc \x000el\x000f­\x000f¾áä\x001b\x0007² ì}ÞÑ`\x001c¬6I\x001fCWGZJ­\x0001«Håâflr'HhÇØ×b(\x000eZ5ÏÒÇP\x001cØ!^\x001d$ËÞÐÛd\x0014¶Ï\x001d^cú\x0018¼:Æs\x0015ës'EÀ±üø\x0006âdÊê`$=}\x000cÅ\x000b\x001b8J\x0017'\x0018JX\x000c1ôuP\x0018LùaécèI\x000e<^Q`,-§û\x0004¯\x0014-\x0014}Öþ\x000e¯+é\x001e~O×\x001cY¾Ww·;ÜÀKóSÎ©Óy>+öh\x0015|³Bß\x001b
ð¼n~rë\x0010¡\x0001b[£¼\x001f
¤D¾\.rBTñ2h\x001d\x0010\x001e\x00148>
¾«Ï\x0003÷pÓøý@¾Vy;Ä»w®mèYãÇÅÿþ\x001fn\x001fw'²(\x000c`å|:P\x001fùiEFË\x000f¥¡/6s±xyz¹%¥^·m\x0003\x000e^tzLÖ!`j\x0002ò`N]\x0006r¾ï¥\x0008\x000fü\x0018Nd\x001dÍJ\x0012ÓGÀÃ¦síBÆh\x0000Âð\x0015~\x000c\x0006²à
e\x0015o`b^!Ç\x0019\x001bèû÷\x0018\x001epâô³ô1|¢â\(­-öõB¢ ¹"Ëé\x001ec8\x0010\x0006ÓÇð\x0015ò\x00144Vä®°Dkî¼DrûÓÇp"Y\x0000±·XE`q¾_\x0010}Ïu»îþ|Ð¿`±Ð©Ø"
¿½XÝí6\x0014\x0015f!Qn»tk\x0004MOiãZ÷VÌ±¹ó\x0016;±C\x0004+j\x0011\x0007\x0013QÛ+$2&\x0007Ô°u(Ikíú\x001eÌZpÓt\x000b\x0001,óXê	+#&P\x0010ïë\x001b:\x001c(
mK\x001fÃàvÑ\x000c¡C®\x0001¤`Ù\x0015²¾×a\x001c¯UÊ5£(\x000f<#0¨é`\x001bË&£îíÛ«äV)qÎ\x000e£¤TÈh(q\x0001|ê^\x001b¿\x0001	[ã¤\x0006$MC¦%&³J"by¤Ñào'úøQ½ý=tê\x0000/°ºàf@I5\x000e	GÅüb/±\x0005â±ç\x0002«\x000bN6»Ó\x001d\x001cØ
8Øy%kXp\x0012I\x0004\x001d\x0015\x001fk\x0017{®~\x0003N.?\x001ccp¤#Mý\x0001G³e­C_V\x0003\x000e\x001cÓ³N\x0012`Äl3j[.}o\x0019Ò`\x001cìjü\x0018\x000c¤=úñ9'²8­»´Ãýêsé\x001bÐMÄá@'Ëa¶±! ï¸\x0004ªwÊàp S¦¡@(\x00149G\x0013ßÑòVl\x000f\x0019Ù×¯{\x0017_¯n}§N\x0015i®\x0006Ð8\x001bò|c\x001c»HE*ÁZjf\x001auoi¤9ÚBóðQÜÈ/)¦oØãnõç»W××·;{\x0011J\x001bS÷³b³¯hlä-½mº\x0016?üñèøøtóXã\x0002¥°º)}4P9G-ODäCm
ùÁö¹¯ML\x0006\x0011~´¬\x0014ÖÐì\x001bÍ4¡ÓàÄ÷¶jÂÂqühÁÂ¦¸Ô3\x0000\x001c6éI&Q\x0011V}3S\x0007PÝ|üå¼ý4ùÌ§\x0002¾×·w·;gg\x001fh\x001a¦\x00088Õ(ï ÎàÚæ¾hÑñböúôòüôd\x0008S*\x0013iaØzë­ma
Ô{>Âë3E3)´ÒÓGÃB\x0005K5>°P.÷KÔôì\x0010Ódö\x0011Pï?_Ë·&ÚðKé\}ù\x0013ÖS\x000fp°®/Ï!\x0012\x0007XÊ*òrtMöGùg?a=õ\x0016\x001f©C\x0005W/5óh 2>åÒ$*oª´Yÿzÿþ5Par»k£Â*þ\x001c¦\x0005©õ	ÊêõüÉTX\x0013ïÛ¨Åô§D¥¨è\x001c¨\LÕûÞ×BecøÓB:ä
¤&f\x0000\x0015(³\x001b6°ÿ¨70a\x001f^ÙÄ\x0004>\x0000\x0003\x0008\x0013éa\x0014«\x0013È÷Æîç}¾w\x0013\x0015ü\x001f0ºJzn\x001a`ñ¥¨¸¡\x0012>þõå 5Q¡åÛ&\x0017¤(m-(@É\x001cÜÇ>
Ýç:5Qa9i\À:Ò\x001cY¶&
[MPj}ªz3G @$6± ¥ÁÔ|\x0001
VLf*N"C¬©Tp[L£XÀÇÑ¬\x0002m®ÖK<ð´_'7 ÁöãOËBxÊ\x0005wdÔÜÝCg¦\x0016(Á?-PZsþÅþÜtÐKÖØ;å°
~-Û(\x0014ã¾6\x000e¤Ú.çÊ÷f\x00007Q@°BÁ:\x001eà¤eU¯+L5Uÿám	\x0000{\x0011
'ò«ÄÄ2ÁM>êøla\x001be\x0002Xç$Uz¾LPM£éÍNn\x0002¥`CãJI*\x0018u^ËtV1Mß\x0004ñB×¤A*Ñf
j
?*æ<¼`ú\x001aK´QÁUqRÁH,ÂÏ²Jçr=¼^\x001euoY\x0013\x0015H\x0004×&\x0015\x0014aÛër÷ñTZr_À®
~-×x\x0001qð.
Îqt\	SÎUo3Ð&*l½Õx\x0003¦^ª\x0002\x001fîò»xLy¦t\x0005';6jî\x001a¯ 4»\x001avÐ`Jl^+\x001ex\x0017{CfmTðÀµ)fAÙy:\x0008ìÊ\x000e\x0010\cûJ\x001f[ª¶@@íñ
Ä¡ET\x0001N#\Ñªê-\x0016hÀR\x0018\x0010N\x001fMÞ\x0016\x000fEÆ\x0001\x0004¹\x0001\x0019z[E\x0005ºÞÔê\x0016,´\x0016l\x000cÁRdOà´\x0006²Ed'"¾
¯&¬¢Ú±Ø\x0001ç=fk«5ÕQ)/N5Ú1Zs\x000cë\x0003¿SÍWdÃäÕ*AÇ&KÐ\x0003,Ã"\x000b|\x001eÞDc&,Æ±j¶%7/D³ÝfÃ\x0001¨6Ä­caízúhrpx$5xÝ3VdQ;Alh\x001eÖ!ÚØäwÉh<Ï¹²95<u\x0018R®\x00166\x001e\x0007céô®&n¢vBp>¨å'lXBÃEx0
Ë l0\x0002"ÝDJ5*÷lMgo¢ïë14\x0000ë­\x0014^hó?<¸\x0015Ïb¶z\x001d.?}^~¸\x0019ÐÖÑ©\x0003Ê°ó\x0006Je9¾múú{å¿Î\x0016¯góWgó'ûÃ\x0015TÛEµ#Q¹\x0001\x0007°*ª³ÊqO~ì.µ\x0017XÐOÝuÕ£h½Q,ð"¦\x000eñTyÏ/¾½SåÇÐÖ¤
ëÔ\x001dM³¤,Ý*´ë\x000bõÐ3»¶:\x0008rÜIøëÖÖU´î;§õ\x0015­\x001fG»nÞ\x0004\x0002*Gü@{óCÎÝ\x0011°¡
ã`E(°`¼R»\x0017Á¦ZõIØ1°±#a\x001dÇR££FÕeiû¿FÐ*Ñ¥Å~¿chäÜëèBÎÛÇ²\x001dYÖ¶/\x001e=¶Òbj\x001aóÊR.$ÐFîX+øV§ê}Àª
V¾bä(ã\x0015ã¥EØª>÷o\x000cm¥ÈÔHE¦eiC^	\x0004¹g *E¦F*2eÙµõda[ÆìÂ¯¯Ù\x0018ÚJ©LiÎ/NP\x0017J\x0011\x000cY4ZöEâÆÀVzLÔc`ÄZ^Ú@Õé ÆX"¨Þ§#hu%\x0011ôH\x0000\x000edi[úo	¶luoW1°DÐ#%Â_\x0005[	\x0004=V \x0018zþÊÑx;\x0007ûý¾&\x0005c`+y GÊ\x0003é(K\x0016þ3F}J\x001c\x0000À´}Í\x001fÇÐVò@\x0007:é=QºvÏJWW\x0002A7l=\x0008&WÑ&Ã6ò±í«5\x001eC[\x0019¶z¤a\x000b²vm!(^¥I¡V}µ\x0000c`+ÃV4lá µõÅJ7|áÞÑÊch+ËVµlÿ\x001añe*ÃÖ4l±§9É//\x001a®\x001c¾zô1´\x001a3c
[Ò±-\x0012¡ÔÔ¨¾ê¾1´\x001e3#õ\x0018û7^³b\x0000\x0007§,lß01¨b0ã\x0014CÀ½÷Åu\x001cLZ_°=J/zAêb;î\x0008\x0011BÛs6¶Ò\x000bf¼¡X\x001c]_,\x0004/ÊAèk3¶Ò\x000bf¤^\x0012«Uø Ð`Já¢.´û±\x0010L¥\x0018ÌHÅ ÅZÔºü´Eçöõ¬\x001a\x0003[é\x00053V/\x0004~=Oá\x0019^Zgö\x001c±b°#\x0015(¹H+¶Ø^}\x0012ÇÀVzÁuoJf\x0010\x0006Ê©]Ç\x0010úùÆÐVzÁõoÒ U¦hü½ÕX#h+\x0007ÇtpDÊêe»ÖQ\x000c;h íÖ¶~\x0015\x0019«\x001bâúØ"\x0011|\\x0007êö\x0003[©\x0006;V5\x0018\x001aµTaE¦Ë%ë-<\x001bA[©\x0006;R5üU{[©\x0006;R5üe´n°#uÃ_Eë*ÝàFêì!´X\x0019h-J}Ã÷ñ>æ*åàF>êzOÓËÓÚº,\x0012W¥\x0010¿/í~ÌÚVÊÁS\x000e!ø\x0003MA\x000fL!Ë°¡\x00142÷å²a­T\x001b§\x001a"eÅ<[Pjáø\x0004ìë©ÜUÞ\x001bçÝD\x0011K`98~ÏÕkÓ[=¶Ran
û+VµÒ^nöÖ©_FpÀK\x000c\x0004Ó×\x0008m\x0010¨\x001b§¼0YG\x0017Vwi«åY+ÕåÆ©.RaU.Ç~òg«¾æch+ÕåÆ©.nM\x00176òDR\x001b\x001e\x0006¾ßí¢õêòãTWÄ¦^ÔëÐ7r\x001fÃ´{:	¾R]~¤_£\x001df!åx½Í©±h\x0016G¦ÐÛ\x0008 ] øJuùªK¢\x0011\x001c²BFLé1Ñ;\x0013wÌÊVªËU]±8ã8ª¨\x0004ö\x0013ö\x0014Hôþò#õW\x000c*Kä_,\à\x0010Á@Ý^¶Ò_~¤þÂ\x0011!Ô\x001dÆH¶\x000e4±¯=ÑVZÌÒb\x0006GÄiÒbXþ\x000f­Qf­\x0019öD[©\x0006?R5hÃÃq´±ì1jMã""\x0018ÞûqÆ}¥\x001aüHÕ\x0000´ª\x0007Öì\x00196T²6µÙÒJÖq²ö¯£­¤m\x0018)mÿªPIÛ0ò\«\x0012\x0003¦%?Gò=%$JÚ±Þâtï\x0018L\x0019g&¸\x00156{*JÚ>\x0003Î2kµK\x0013éx^\x0001ªÝýCå4NÃ_d$J5ªá¯­4C\x0018§\x0019þ¢DûX¹\x000cqË\x0010B\YQ2íCñÊ÷*\x0011+½\x0010GÚàÎsY@Ä~8^rY/¨¸'Q\x001b+½\x0010ÇéàC\x0011^NÐ0l©|É¦Ü×ÛB¬\x0014C\x001cùH\x001eã:WBóÄ9µ\x001es®÷ó+ë+&GÞ±hÖz,¨2^Òô)#ö5#c]\x0017\x0010Ç©¿F$àÓZ\x0005;N3\x0004gY&\x0004\x0011L·gC*³²ORíGJ[[\x000e.ö£\x0012Ösíé«ëk÷qT]2øGá1éÖpy¢\x0003qw¬.>
W¸ß·)®ê4E5!Oñ¯xjRuê\x001aû\x000e\x0003\x0017£*rßC¬êëD2âèÚ'\x0019ìc«ò4¦J¤Åµ:÷MÁ£[\x0012©d_ç\x0011[¿ª¤¹®U¢5ÇnïíNß[ÇÅÕØÀø_ä=¨Ú{PcÝ\x0007<\x0001yq}I\x0008Ö{\x0000»¸\\x0004U\x001b7j¤u2\x0010¨Ç<¦\x0004Óã/NzèëWÞ\x000b\x001eI\x0017\x0017ÿ:ê¦IWz\x0008Ã)¦É²Å\x0014\x000b½-úÅ®ëIõÈÒÓ\x0014ÓÁÅoæ©U\x001eöcÝèº T¬(8\x000e®Â\x0004»|Í\x0002¸Ü/S\x0017\x0012Á9|ub[LÓyI§R{²svoÕòºgËqrAðØ(=
%KÇp\x001aömû\x0004Ø\x0004þËRX£©A[á¿*ÌäU
\x000cFÔ(`ty¸Ìµ\x0008¥ô@y6`ß>Yá·ßy´^á`G®0NU%#,GqJ\x0016ÛÏSj\x0014OÎ°\x0018{\x0003ÕÅh\x0008¹"Úfì\x0011;\x000c@í'\x0019¤\x0006vcÅÚ_\x0016ÛODüÎÝ3ì¾÷3le
\x000c¢iâø§çe\x000b&>¨bIà;+fsýçãòîáju7;Ñ³WËÇ/«¯Îß>Þ½_î¤vsD\x0004fãÅ<z\x0016V<²AÑ×'í?/çç¯\x0016çé\x000bç?-þñ÷ÙóÓËó\x0017óôZtéqÊÐ$zYBSQæyc
]}¦·}E\x0011ãé¥Ñ]züë$|¥\x000e¨uzÔGè*ô}HSèMMo¦ÑÃ)§JÅs±(Y³ì\x001b7ÞÖôv\x001a=8¬4</µ\x0017¢ò`Á³Mî\x000b¼MÁw5¾o°HØ¯ïm\x001eôí=ÏqQ¦¯7Ã\x0014|_ãûIø°¸<5ÀÁÙÉ¥\x000bÂ	¶\x0001AÈíùð\x001a?LÃ\x0017{®{ísH\x001c[ªfxÙ÷
==ÖìÓ$>.=O\x0010\x0002äØÈà]__Ó	ô¶\x0012øiä\x0004z\x001dÒ¹\x0007Ï¡\x0010¡\x0003W(ßo5^Öôr\x001a½J!þ\x001c2å\x0000¯Ð&\x001e%}Å\x0004SðU¯¦ãË²ø¹$\x0019ðË¬½¯~­nítuk³Ii|$\x001b\x0018¬\x0005¯Ãÿôµ´\x001fëÃ\x0013§\x001d\x001e/4«ú ó`*40yøµ´n¯ø \x0014*CSLÓXX[Çó}(m\x0018¸Çl\x0014®¯y
¾¯ñ§i¬¯\x0008ßç~¡Oð÷Jokz;\x001e§ñÒ8\x000e¯\x000c%\x001fÎè Ñ\x00177ï+©ts£/m¯\x001d\x000f¢Gßúiº¾nêSèeM?íâZÅüùÖÁl=öMkÂnjöiF>ÎÕ4§\¥A3Ov&*²ýâÛ\x001ad&5¶¶æÀz¾µ<ô½7^>\x0005¿~Ì\x0004%1Icá°oòÎ]XOAÚ«±¦Be/à_'á£LÍ=°Ô×qÓà°gUë[5QßZ%xÚE\x0010rûE0ü\x0012 ûÂÔãéµ¨Ì|üëÞN~à\x0017YÁG\x0007N~_ÀoRpa\x001dGãðÂrÚoà¸³£%×\x0004~\x0003¶wß«ÊóSÿ\x0006*Nû\x0005rünñ\x001dmèözWâ;{Ý\x00028Bõ/ ÅÔ_à/O9äï\x001að½Ýó?S³÷³3|÷qÐ\x000bS¾¹ÒFÃÊrl'liÂw½¸Áÿ÷á\x001fÍÙwý\x0004fIu»Ò¦\x0011«9õËÌík°¾yç:.s\x0018Ïì"\x0015Ág\x0019óØwæA÷¼ÇBÇ.t°Ðn¥Äy¢¬4õ ûr?FBKÑâßZVÔòßZUÔj\x00025[]ÒIÁE}ÊrQ_\x0014}-øFR«J~¨)\x0002Ä'­/5\x0011\x001d¡ç·\x0007´[¨ªÎ5þõßá(%kì­¢®°£þ·À\x00065Ó5GPÑ,ÿ=¸]Íí¦p\x0007ê¥\x000eË\x0013\x000fñR:ò?CozÙøõ~[¯÷Ûïz½`±¾éN3\x000bL·zöìøöáêþ~õiuó0{¿ºÙáÇÕ§\x0001ÓéÁaü,fp,|¤\x0010/ýÂ\x0010û·ÜÇ§¯..\x0016¯\x0016'¯g/\x0016\x0017ø}?.^áÀúþ\x0014YuÕ$d0²%Ï_¶p\x0006ÈªLî\x001dÿÚ¬»Èz\x001a2Ø×4;É¤ÀbF.1-Ý\x0017\x0018lºÈf\x001arÉÎ\x0000KùèËìmë÷s0l\x0017ÙNCöeÖ-æzJB.-]_×õ\x0011È®ì¦!G¬\x0003HA\x0007)©ý\x0014övâ 9~Ã>}\x0017ÙOC\x000e\x0007âúæ÷¦UÖü\x0012Ý\x0017Ø\x001f\x001cºÈa\x0012²(ÏpøxÎ\x0007F¡uÚ7Å³8vã$b­ðµ0/rä(r,M­\x0001y/\Ü­¬IÄ4æÈó$PÞÑh±Èiìà$Mº}H[Ý¾¤\x0007áö?®fgwð\x001f¿ú¼¼\x001eÒÎP&\x0014p©w)¸\x0000\Vê}\x000fçùåbvv~trxt6?ÞrÆ%° 1®ÚJiìúåXs+"	\x0010§ÐöÕ

§Ì	Ê~Miae\x0017Rþíö~õùãìpùøvõ°\x0013\x0014s
©EÂ*!j1\x00109=Â>ß\x000fAÿvz±8ûqv8¿|¾x½ÅVSiiÇR&Mê9^Î\x000eoï\x001fVtx±¼»[Þÿö¸\x001bXiìûM¾Ìi2\x001aëK_ÍÐ7o>;<½x½ÀÄÃùùùüâ?/zs°©ß¼{Âýn$¸1ªýu.æ¡±J¦\x0019Òô \x001aúdB?ø£ÁåN\x001a\x0008ÿÎÆûÕìz	61Ðï6du\x001c\x0002T\x001a¯×u°\x001bNðÅ\x000c¨ÏzË±âI\x000b¤\x0017ÈÜç ¸n\x001f\x00012/îÍ\x0000ã]â(D»_4\x00084èÈ\x0002¡o¶Ìs\x0010Y§\x0000\x0017ö¤}>\x001dCH´è\x0016ü\x0011Åí\x0018ÜÔæ)ûH kq®\x0004àz<¹tå´î"áí<ë\x0002,¾\x001eá\x0015^ñÄ<\x0015sò\x0017àjÎóµ®oé\x0008\¹®uKËµn#x\x0005V8	*vÃG¡4
ÙÃíâõu}Éõ#©N/þuÔ\x00022>S¢
ìòðtåøÍ9à\x0013Ð^×ÍH\x00120z-£±ixn´æMzk\x000b'8`\x0008~ç~n\x0016Õ	Æ¿\x00036®D8£Ã³i}¤XaÔ}Ïâceu$ð¯ãá\x001chEÀ\x0012Ë\x0012°å\x0012Ø;ºc\x0004°QÕ¥Ã¿\x0013j8V\x001aõÏ>*VË\x0016k[&\x0002+´Íd'¬à[0È{¸üº¼¾GÜWËåg`ß©Ý\x0004\x001c¥\x0014\x0001Ín\x0010eIªù£ú&ú\x001cÎÿ1?¾@ÚWó×ó3@ß\x001bjÜ0\x0012W\x001f$¦$Vm\x001a¢ÍV\x001a¸\x0013½åÆchcM\x001bGÑ*¬e´¸³-ÆÐòâê¾\x0007É\x0011¸â
ÄÅê\x0011¸Zr5\x0016àrOV\x0001&dÜ¾Ô\x0018\YãÊq¸ÊÒË)à
NÆ¦
S¤ísÔÆÐªV£Å.\x001fh%%\x000b¾e½C<Æ°êU\Ù@á\x001c8¶SÅ­Ëï»+ûÜö1¸¦Æ5ãp150f\ð©¦\x0000ùL+ú¢chmMkÇÑúH'8µ\x001cwát\x000cÓ}fÙ\x0018\WãºQ¸6r\x0008G\x0002\x001b-.ú\x0012Vº¾.@í´à]uiñ¯£\x0016\x0017\x000c@
"r%aCä&û¢"#pe¥}Ó0¦1k\x0003\x0016\x0017ÜbÁI¢.\x001aë{¹hÊT\x0012\x0017ÿ:\x0006\x0017,q*c!H
àL5\x0012¹`®õxlm¸9ÖÔQ¿1M_>¼}üüö\x001f»­0l$\x0007V J\x001d?Ðºôvè+W8<½|ö\x001fæÛ­¯ø4\x0013S\x001c§PXÞycDÀ\x0005\x001c\x0019õ²/ÇªÑW¾Q`:AÞn³Óbf,Æ·7}-\x0011\x001a\x0019«öÍ;-0 ÉÞÎ\x0001\x000fðb8hgû^+\x0000ÕnÞi\x0019c,E|]
\x0019²d\x0003\x000cz\x001aU¬V\x0011ÿÚºØ£2çÀ
L/{\x0000Yê\x0004|èkÔ\x0004©;Ùgð6
$iÝkG88!'âvs|Ë\x001b×ã[
)T\x0014×:>gã~±¼º\x0001ÿouwsu3 Þ­°½6ê\x001fØîu\x0017@\x0012R¹Þ&8ó£\x0013pü\x0016ç'G'»	]Eè	=ö=J*\x0007Ä9Wï\x0006Rxé§\x0002ú
Ð·\x0002JGÓ­d°iXv\x0002´|<)û¢@m¡"\x000c­\x001d\x000f ,M¯7°w
n\x0013a¬\x0008có&íãPQëF°+|YÂ¾¦\x000f
²c®E\x000c\x0001fBÉÏWØg§4\x0007IF»L1®iªFT­.²j	!Éüv£{híôÀ´!ê\x001aQ·"@\x00162%/\x0012¢\x000eÅ ë\x0012ÚhjDÓ\x0008z\x0005\x000cHÓ\x001c-å\x00191Õ5OCt5b³Htá¢\x0002O¶ÙDÄ8úT@_\x00036DÜÛ\x000c(c\x0019³«ØK\x0010½Õ@m¡&l\x0016!òô\x0000-Í\x0006®3hÉw%ÖÍ2\x0011\x0010³ZñyÔH&¼n2¡¬e¢lApK:O
¸¥ó¤SÒÄÀx²ÆÍxüp+=¾#pÆ\x0001\x000eàeö5ºiB¬E¶l\x0016ÙÑQàJzk<´\x001c[\x0011ºwÐI\x0013b-²e»È\x00064\x0013:eéù\x0018r\x0004[è¾z6ÂZbËfí4NaÊ¥§¶¬qÞýDB[\x00136[ÙÞP\x000f\x0017é½æêXB%¶¬UlV)Á²°ñsò¥ö\x0001ûJØÚ\x0008k"Ûuä×a4\x0013\x0008LWFt}dÚ\x0010k¥"
hcM\x0007\ÏPª¿ù®ôæn6!ªZd«f3Vk\x0003½\x0019¨s³ Ö\x0012ØÛ\x0017»	±\x0016ÛªUl{ì³CÞ
Hpj¿\x0010
ÄþöÇMµÔVÍR\x001bD5{+Â\x0017#Lô½]y\x0010k©­¥¶f©\x001dá¦tØvmD5ÕxPµLTÍ2\x0011.K®ûûlX±ÀeYßç©®ª¢j\x0015.*\x000e2y\x001aø(T¹)zjàA©JÞà_[Ï¡*\x0007\x0019x®\x0008N\x0004g;»·k|\x000b¢­t3þµ58Bïßi9ò`¢,<
P×O·+>[!ö,æöj1(öëåDÍ§kÍ§Û5Õ\x0007Äï´uµ\x0005±¯\x0013V\x0003¢\x0015ut$ý½õ6;`"¯Y ã7M)ú2\x00072ª'E×G)Å%5¿¼}ü¸º¸Ú\x0019Ü6ÎS²t9«sHV+Î13Zöê¿âº_^þ¸¸x}´\x001b×wqýH\ë9^¢±¯\x000feHì¡X¼ïK\x001d\x001bº¸a\x001c.ö¨';W\x0001$)]+§²¦ý\x0011¨f\Õu]Õ3]×v`\x0005ë+h\x0008Yb@Û®ØØ\x001f»m\x0007î<h"°#\x000f\x0004¦}ç\x0015ÖJä{\x0006\x0007Bó@1\x001b{Ûã\x000165°\x0019	\x000c\x0012ãµ)\x000f5Zqö´{:ÁÊ\x001axä\x0019V(mir\x000c(¯\x0010éHèÀõ½ÓBF\x0000ÛX\x0001Û8òÒiAs\x001c\x0015FW3¯,
\x0019¬ëk\x00167WËjµ\x001c+$t¤\x001eYRáDâ,¥qèúR\x001eeJ¦WÝÉïúJ£ß¯><®nR\x0016Á5\x0003¤ç¼ÿûïÿ?Þíl3ÑAn×!ÁôÊÏôA9.a1¦Wy\x001c½¼\¤|T\x0014^÷fóËóù¶_ 7zéÌB
Ïò¸¢Åþ´ú´ºßÉ\x0016+:(©9
xö>¿ãÃ\x00055§é}·¿¸\ÐJ¿Z¼Z\ì$55©\x0019ªÑ<³	K]ÎÖð ù^{\x0008©\x0016âüä?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-15.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-15.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ýî`a0ÂµC1Ñ{\x0002\x0014á\x0005¢hû|i~º:\x001de'ñÁ¤ÉÈ\x0001V\x0016$ì#\x001cB¨f\x000e|*Z\x000ei¢Ô
ÈlX\x0018À\x0003\x001c\x0012&¯D\x000e¶q\x001d×pÄÓ<)¼uJ\x001d×Ãêxë(%­iå Þ±ûCwó}¸ÆGFûáþJ6cÅGoSïèÈí"ôZâz0[ù]>þbÕ&³n\x0017¿ß|[u\x0001pï¸8I\x0008`xv¹vÎXt\x0007`¶g\x000erñ7ËóQ$ñà#É!:újZKôÕ´§%ÑrÃ¡®\x0002ÉX\x0010\x001b\x0015­!ÿà #\x001fA<Þ<Ênl*hDÆ~\x001c\x0005¢Ý;°;½ðq\x0004È)\x001f':'c×$yk\x0019¨kbi(å+InÔêécÿ:~±ú¶ú>ü6\x000fÿþ(	\x0010n\x00184\x0017c\x0015Ò	|W Ý<9/\x0016o\x0016ÿ,X·Z~ëø×«Û÷Ë]\x0017w<*Ê\x0007\x0000+b¼\x0002òL\x000f»\x0019XÏ^/N_Ìî½&\x0019ú¿\x0004M2÷\x0005\x001aHñ¿Îâo.Ä3Îãà.Ï
½~Z½ûô\x0005´\x0016:-¡h\x0006ZCP\x001eåá¦î\x001eíÝ\x0008\x00078T\x0002g¯<W£\x001f_ÂÙÕ\x0018\x001e\x000c7åÑNÄÈpÈMA\x0004ÕàÂólÃ«åÁöþÑë\x0013þ­*.ôhføV
¯VÕ°<×ï¹ýÇÞ,oPud -4hã\x000c¨\x0011FÇ	|¾­µaßÌO:m\x0011\x0014Ñø¢P"ÖøÃ0e\x0003o£\x0002i#¶¶"\x001a½1\x0014>øúB!E'_ÛÅõ\x0015:sáØ\x0008ï¤øîÞ÷Ô¶W³×w«å d/A´Kw§Çà4F§-s\x001b¾þböúìr1\x001f\x0005o1 \x0012æ[ué\x0004ÇÂ}-;ÇÅHh¤ë@Ü\x0008\x0004V`Úv\x0014]\x001a\x0019><$\(«n'Áäæ(\x0012\x000b\x0012²>®6\x0007>~\x001b®5¦\x0014 d[IòÛõÏ¿ö\x001cÝàÎ\x0017røwÅåJ-\x0013ã\x0007
\x0006Kv\x0010$XYûóË²\x001dûüûêÎe»ãèîËÛÕ»å·Á;',:>m°ë\x0010k\x0002#\x0016\x000c
%yôÆSðèìÕáâhþ¦|áû¯ïÍ@\x000eïVïn\x0006C;Ý\x001b\x000cC>XwcK_°§}WÿðüjñÓÙÕI9¶D+6\x000b\x001d\x0007÷2(,¼\x0013c|3	4ðv\x0002£P¢uáa\x001c:)\x0017è¬Dáì£ú(7Ì\x0019\yV\x0015N0ðæu'&\x000bÂtpN?·"pßáX\x001b\x001cð>ïòÂ·\x0011,Þ1Ì6~\x001a%M\x001dÆõÓ7÷÷ã|õáþi8\x0010	Ñ­hA<3\x0006ºIàÁáe,Ð\x000e\x000feûÜ/~8/j£õHÒ%áD\x0011L ²\x001d$\x0019Õ1 ÒM\x0013Äâ\x001bÌsM$P9ÛLu\x0015£H$Ç\x0016ÜsPcÀ(1<V:\x0012gÌ³ÍºdåÝ'»eð.}º_Þ>î
B±¨±6×)~uÆDbGiÃùô/®Îç§\x0003>}FÞ¦ãhéÚ
\x0002\x000cÜ{Ñ(\x0010k}X"~²Ëw½{ïí]xè¤>ògr Ó\x0014;0 E>¸ñ\x0014Û1Ñ®Ã³ðÒÁ\x0012ÐÛï\x001f¿¿Ëç­A\x001dõjpÃ\x0018fºÉ'°awXbà!òÖg×Fv#XØEy³d\x0008?ÞÀYÜáÞZzÛxæq-¬Âþ©±\x0008?ÿvg\x001eïí×ÛëÕoC	\x001fKWAñEO\x0011Z<\x001aWååfÄþôxñc\x0018hîdNk\x0017½fèÀµñ
áµ¤\x0012ö\x0004\x001ed\x0008g>oÆÐWëzy÷ôø¸ºÙ]1\x0014àÖÙ}\x0005¶\x000e¾\x0011}¢p)÷7ÉºU0üíååbG±P"\x00159©h#UÒuÃQ:R'=xuÂïUæ¬²\x0015´¡±2 \x001c=\x0019í#ëô«cÉÛÏ²ª\x001cU5n\x0000\x001eÏ¨\x0005Í\x001b\x0017\x0015GÁ¢J·\x0017Rê¶EõÁ)G9,+e¼`p\x0002²J¾U59«i[UË¨\x0006\x00025æt¡	Sïy]]ÎêÚXÃ=µhp°¢ãÃ&\x0010é`Ù}°b\x001f\x0005+Ö\x0004\x001bn\x0003å?\x0002äQ»\x0007U'_ß±²·C-«à\x001b¦UðdZ/×·³«ûåÓûAH£-<kº\x0015\x0015\x00026-¬¨C\x0011W°ª[ÎÿÅüøôrörq>¿*	5f|"ç\x0013|6¸²Ê¥\x0007²÷ñD\x0002ò)3Oæ|²OR«Gûé!}\x0008|:]Fi5Oå|ªvýÂM),~_	¼àeqNëg§~_óÙJ>\x0018\x001e9,\x001b\x0007w\x000fJ®JêÆçs>_Ë§xªÃÃ¡ÈØpõü\x0000W¡ñÞÑàµg\x0003Z;ÑYsVBk\x000bàYíÐ#
çÖ°\x000e°·÷xíæë>.úAPÁäéãÒ
n>\x0004ë\x0001M\x000fÐÔ\x0002jÍZ\x0018à*\x000f\x001e>Xbm'\x001a\x0017îz|®O8tÎ\Jz{\x0005-,E÷\x0013ù\x0004ë\x0019gV½~"Ý\x001e¬S\x000b¬ó6ï±\x000e°{Ô\x001e\x0011\x0018ìÜÚ\x0011C@ÆéÑ ¦.`o\x0003Ú
ÈU*ò·ÁÒÈha¸eÊY£y\x001b\{pØy`]¬âèÓò+ÜC_öáÝÓýÇÛ\x001d©6ÎxLý\x0005LÎc\x000bÎLÂ\x000c\x000fÃÍÐÅÑó×P\x000f}ØgWç/O\x0007<Vä´¢V9-)Ñ\x0001Wüèá=k\x001c;»ýÀÊ\x001cV¶Á\x001aúG ¸é  \x0003°Âx*\x0014çìYQZ\x001b­ÊiU\x001b-¼\x0011q#8­â\x001bÌ*\x0016E\x0006iÚÒ×Þ\x0017\x0004£â\x0005\x000f³Åýòí®X±ñPù°qU\x000c¤0H<Æ{Q±mÏïY8QCQD's:YI\x0017¾2z´0Çª;æR\x001f\x0016z\x001aÊéT\x001d·,ª:GNµ\x0014E×àD:ÓéÊµó,jÃ\x0015±\x0007¨k\x001a£\x000f»ÅWÁ\x001cÎT.]8\x001b\x001e§\x0002\x0014âº¥Ó|oKgs:[»t:Å¤ O\x0011·\x001d\x0017ßêÇit>§ók'\x000c^vt\x0018\x0019ç:¥ë9¶v¼oP*-

ú´Á\x0011³t(è)¿Ù?SA·\x0019\x001eÕ½ðèÿû\x001fÿkññæz8oàâÀö\x0000æ¸èÇ:©o3M¡ÙâåÉñ@0?ñOTó9×áçãÉ\x0008|Ð<·=\x001e:Oæ|²/8\x000cg©»Â;N]@ÁIÜfV*ðT§Z>¯¥\x0018-FàóÊäeómÛ¯Oç|ºOz:¼ÁáÂrånÀ\x0012.¸|&Ç3Õx\x0010¢A<ß3wËê	 é3Ïæ|¶~÷é\x0003¥Ð]X!\x0014¶¥íÇôö\x0000ìh>ó¹úÏk©\x001aÝFåÓøy\x0015ÆE[u?Ú:\x0012UÃG\x0013±J#\x0000\x001aj%/FÛG\x0003öÌ\x001f¯¶P\x0008§ñ|(ì\öV¦\x0008»Ø\x0012Ã\x001cÇç7¯\x000fß]\x001fGV_¢v\x0015¦\x001fÉ\¤\x0018¦2±ï{é°p0<B7º\x000f~\¼"5¶.'¼Pæ²\x0010\x0002I.u\x0019ã\x0011QÖ(z$ÙÉ:'ÔÕ:\x0016£Së\x0018ìÆ\x0018\x0008q©\x0014ßÊ©6\x0007´µ*\x001c\x0012\x001e­ f\x001egº@5Ç\x0015\x000c+,¦\x0002º\x001cÐU¯`|nt»0\(ñ!ì¡^í~ê7æ½]È«·¡ð
\x0015»\x0002qH\x001c£I`Á±@\x001c%Ó¦ ª\x001e¢ªGd\x0014Ö b*ò\x0014(¡=\x0005±wRxõQ\x0011 ¨\x0019Í¡\x0014"Ö÷Ád:+b3®Þhz¦\x001aQ	((}®þ\x0000\x0017Q\x0000:O!ìf^}E¸è°¼Y\x0008Oy;ÐFÄÍî×\x0006DßCôÕ±ÇÑr(q\x0016[Â<µX]kìÔ%\x0014½[OT_{°2ZDæ,ªExñGD¶QoSh7/fÛ]ÌÇ_¾B]\x0016ÄÛ^.a(ìð\x001dÆjF{#âÍ.T\x0004Y	l·Þ8)Ç¯^Cq\x0016Ú^Îa\x0016ìnB\x0013zBFñ@aº\x001d\x0019	ée\x001cþ3|*¡Ì	e-¡\x000f\x001dµð\x001bCÍ¥ámGkh6\x0014J\x001a\x0008UN¨ª	¡q\x001c?2;ÕÎÜPY\x000bØÊ§s>]ýO(Ô\x001a\x0010\x0003)è\x000b\x000b;Ðä¦e\x0005µKÖ*ç@ÿ±\x001cþ ïbßl/\x0003\x0002ÙF®©¶NË¤NclÙÞìn4K¤2'eRª&RN/«ðÞ\x000eHûT»äÊ·`\x0005¨ÎAõ_yIMNjZH¥bôÖ²*ZKãRøéòµ]isLÛ©D\x0012îclÖ<>Ug\x000c8º\x0015¤.'uM\x000bª=%-¬Ðð	>GR_\x001ax^WúÔ7­©fP\x0006\x001e?½=À¯ïL_ßß7ãIyß6\x0019Så<yè\x0016Ú
â¢:b\x0016v "PÚ3¦¼Éà3³¨wåÈHy}¼Zo°5¢ö\x0014o²RÚ+Ò>4Î@\x0012: á®/äù\x001bQ{V7©ð\x0004Ãb`(\x0017]Â(<\x001c¦by»ã¿.?\x0001R(?©&uÐ\x0016\x0019~eQ4Iÿ:*G\x0000ÿ>P{[U4mU\x001b\x001c)\x0014Ù°\x0002û9\x0014&àçW\x0003/¢
ÒÞN\x0015M;ÕZ´/Â_ÊîPq!©\x001b  îãæ\x0017½J4ÝT3¤UUQVJ¤©Ý5ö¬¿h2ÿÞ¦â\x000eí\x0019L<êÎIcíÃ¦Êù-æß1Rb]R
Rbj³[µ\x0011µïK·)\x0007ô\x001aµÛ¼bÜîød¬\x001cíª í)Ùr¦\x001c<@´þ0¯TÈ¸¨\x0012QJ})Ù;S²åL¸\x00039©ÊÂE7ò\x000eQÙ´ë?¬çFüFêüÕ÷\x0004¥S»úÜ\x000bwTìR
îªBÊðì¡âzÉùvÊ+¨\x001aìwO"'\x0014µ^fD Ô±üºÕC=\lÿä\x00152'ÕP\x001fGy\x000bIkÈÜt\x0005C?³Í·=[W_<ÍNßîµLÃÕ*-TÕÄ0¬_WðmM\x001eWa\x0013¾9\x001bP3Md"'\x0013Udá0c®Â\x001ajB<[W¯O\x00019¬[2NUëáR\x001bWê:5lÃÅ¬\x0004Ó9®\x0003cTg\x0005dY$\x0013>=)¶Y'39©!ëÆ¢R¨¥¼ÓTa\x0011þ£[\x0012Ü#È6«pRV¾E¼¼¿¿\x001bäÓNÄ\x0001&ºST§\x001e\x001e»"\x0015Ü\x0016bÑ\x001cÏÏÏÏvSÊR6PjKýÎ0\x001dÓðÁ\x0004®ßa~:¥Î)u\x0003eøÀ\x000e¿5äòâ·¦Ñsà/º	-Yoô¸Pî"\x0010¼Õ \x0006\x0018Ë-¼_7Mzðvu´ñÍ,Î7ÚZÇà±´ÎÚø2\x0008ÅQÓå¶Ô|;Oå|ªÏÁÄzÔ±×"ß@!&\x0003z"ÎùtíúÁ¨z¬\x000e.\x0001VùY\x000cïí-\x0006z\x0014\x001f\x0019\x001dÉòòið\x0007×\x001fo¯W÷ÃõÚè8\x0019*j8¥î,K\x0015?bkEÜEç\x0012Ì_\x001e/Îª2ý¦çâõfÑÊNu!\x0011¿1¼Tâë)AÊªÞ\x000eQT cgÃ1\x0015¹Ërx÷ôû\x000e.ÃIl¡D+40FP¹á[]Ã³«\x000cVîÍdX\x001fqdÁ3 \x0017áÑ·ÓôQ-ßR&µ\x0013ì-Kº§ñ\x000f\x000e\x0019ýýï'×«§ÙëG8\x0017o®Ð\x0006±S4CÙ`ãÃ\x0013úÄpçYÒX³Ï5\x0017W³\x0017Çp:Þ\x001cÏ¡
bX>#,ÚfWoÏ'½X¾½{\x000cçcø\x0008«nxz<Â2j°þ\x0000y¥Öliª\x000c+y1?<»\x000cGc7ÈéD\x001dQ8¶\x0014ø\x0019µ|º$³hå6\x0003]C§r:U¹v¤º\x0008siÒñðÒØÒÐ;Nl®È.ßÙÅÝÓý»\x001dèÂäÕkX`Í\x0002¬\x0018Öb\x0016Z[.Î®Î*ÑÅæñ\x0015Ùñ\x001dKÇ)|\x0008
\x0010Ø\x000b-Ìº\x0017z{wÆ.¶·LÙÞ8\x000c¤4a"-hE\x000e
tb:W\x001aßèD1M\x0014¯\x0014JoQ¡\ä\x0016&\fl"g\x0013Ulà>³(ô©Fa\x0013\x0010Ö\x001f\x0015
Ñý$6³Éºu\x000b\x0004]m-¨lÚ\x0018\x0013ì«l¶uÛ|{\x001fâÛ;Ó/\x001a\x0004ëÔ,ª\x0017\x0003÷L¼hSVq­^TRÿ¥]}¹¥­Öm°åõÍÍò>¸L\x0000Ó\x0011Â?\x0018`>|¸^¾\x000bÿ\x0002\x001bÞuNÅ)é»\x001a\x000c\x0007fÌ\x0019\x001fGNÂ\x0012FñÃ\x000fÇó£¿¿\x001fÌÏ£TÚñ=\x0010\x0014i\x001d\x0003\x0002Å»\x000cA`àKÇáiÔ/(]év\x000e\x0014g\x001dµ ð/ï&Ë7 s©Ãp\x001c\x001c\x001a.rÔ\x001ch\x0002ZFã@oØ\x0006àõ\x0018\x001fA4¸þsÛ\x000e\x00125QÇHº½ZµqEpükx3±	 Q\x0003z\x001c\x0008LÎ\x0012\x0011D8È\x001aæ^JÜ#¡©\x0019\x000fòóÏ·ì×\Ððõýêöqõqyÿ~U\x0004áá\x0006Æ\x0004@$ôÂüP\x0018£Íã,N\x0008ëõöÈùâôrñr~þ¢ä:õ@p³\x0001\x0001ÛuK¯;Ìº=Ò\x0015!\x0008N¹­\x0000Yúåê![ÞÐÒåìtùôX&\x0012"\x0000ñ\x0018³`Ëº¹×áí\x0000	íiD½Ñ¤óÙéüêr\x0014\x001aêÕ¡I3£=\x00031&\x0019Ñ¤åfÙ>Ð\x000f#\x001dÆ%\x0019?\x0006È"\x0019sÈ°¾f\x001aÙó¡£»ÉóñÉ\x0010È¢ð- A£#¢9©öö|ºè\x0008´°ÕhV ]R¼kÌh~\x001fhÏÇ@S]T\x0016.\x0011\x001d?(\x0017\x0002-\x0015Sf\x001fhÏçAó1%!÷]ýkD³x¿1\x0012ÉÒþuhZD77 9	µ\x001c\x001däÆü>Áó¥\x0015´4w¦ò*¼·\x001eøEé~fýk±mËàÔ\x0011lÐ~ëæÃ]\x0015Ñ8Ù5Áô\x001eÈhLN%á\x0001\x0003\x0018±\x001eÙ¤Ý\x0003Z8J¼ú6ECI\x000eÒH\x0011
T\x001dF=ÏilÁ\x0002ñúû\x0000¤|è¦Òè\x00056òÁÝa#ëJ4îãK4 §Lt\x0014s\x000eíÿgîÝ²ë8{ï©`\x0002÷Ëê'(xáöá¢uº_zm\x0010	5\x0008P¸Èüê!x\x0006¶§¡x$'"3¢U{×®Ìª}üé¬³l6¬\x0016Êø\x0014j\x0017Ç4±É\x0018÷s&ð¾ÝHÃ»2ßÅ\x0016_O6\x001f\x0008Ò,\x0013®#,~,ñHlÂ1ZNÚLªÙ±	K
\@ÉtÀë3j3ÞÏÅ÷\x0000Õì×`-ñåLjA±\x0007\x0004á\x001d³×ÚÍ¯Ï?Ü\x0015aî\x0001\^~Ï¹¿Í<\x0006rö\x001a¼KÛÒ\x001a¯3¸»ü\x0007p1ºþûxÂÏüÃ²½YJFûvûøðò´å¦£åx\x0011«\x001b0«£§|é#É0A;?º8»¾ÜrK+`xxE
\x0011/\x0001§]´´±ÝV\x0012õa	\x000cK­×Y\x0006bTG0\x0010ã[-zy\x0012êÇ­0,·^\x0007\x0003¡&\x0018\x001fÉWÂ"é,ÃÓ·fÂ°âzÝg\x00126Ë<ê4ûLðÝW\x000cÅ{,ÆÓF
8\x0002ÙÑ1Â2L\²dº(ªv\x0001ÜC§C£i\x0001[¦qÖ5Ó|yüåö?[;å\ÝÞ;<cÌ¯2Ú+¡é\x0004Ã:\x001cr0x$i\x001eçÁÑé¸+0h\x001fÕ`ÈtÀ{é=û\x0016')\x0008×:(7VI
\x0003ê#¥c)Í^	)<C±;O\x0018²\x001f½bt©Û\x0001F¿Êë¼þõ!ØWÙ"Â¥\x0002\x0011DQîp{ïeMq}t®<ì?úÝ¿\x000c|ÿÇÛ»-.E\x0019Rä×1M·¥k´t
QN
×êÃë£ã*WW;	gaN\x000b(åp&ZN¦XJóÀ%|¸\x001b8(RÅ¡\~\x0011\x0006\x0010\x0004:\x0013ê@üm\x0000yu÷Ó \x0002}E\x0006	\x0016ãôe"§Tó9(=RµBP\"\x0007èØé\x001féî:ªÄÑ\x000bR\x001aA^i\x0010Tªa¸O+Usf]E3<p\x001a8(óQÅá=G*\x0006¾\x001d;Å;&ê\x0005\x001c¯Ç^Åùa\x00169$_\x0001\x001494ü.C/RÏÑå4ª@ð©\x0012ëV`V#taµÖq¾\x000f)ÏÞ
\x0018ò¬@")tC8LïÉ£ó\x0015µ{Æe¯ªá¥ê8[§µïÌºìD\x0013ñ¹g\x0005
\x0006:æ5¢Ø"~¾3ëR\x0011ukdô\x0011¤Ëk×q´úç¾|
¥w¿}ø}ë[ÑÒä	\x001d|\x0008yS\x0006'Ù§À,hÓ[ Gg§¨1£?îÅí/7Ïã\x0000:ÐÄ$åCÌoÛ1*\x0019iÓFÙ\x000b
/~8¼úëêñãÍ·ü?é¯\x001d´®EÊN.n?¬·Ü<1Á½#Tì½ÍÏ¥\x0006ÌC\x0011jÏRµÉÅÑ«-wÏAµéZ¬+ÒøÄ4ø\x0019\x00042Íø\x0012 pÌð\x0002,[bÙ\x0006Séd Ä2\x0006&F\x0019ÈVq±\Iå\x001a\x0005\x001f0
Å\x001b»Ù®_/ì½\x0002V*_Rù6[å'Ö`DÄ	d+^WQ-1V(±B\x0003ÒeS½P¢âxÛt×ó¨bI\x0015ë©\x0002ÄÛ"_ QÎÐ±\x0004=º\x001a\x0017{Çf#\x0016)Ü±k\x0010
\¨IiN)sñq\x000eær\x000bÌ%û.«Ág\x0005¸+¹ÌåRåcæÖ<ì
µKõ¸T\x0003×t´áØ]<n\x0013\x0012	éå\x001eZ±t\x000fK·`É}Z]VÐµ\x001b¬å-[+.±VÏÊ\x0006w\x0005ò9"	ØXBXs#^-9{dÏÊz
^cÚ(Kv\x001fQ³ðøÄ4«çPeG@e_æCÑAPé-Û¹t/ÊoåêyTÙàRqr¦Ï\x0018`_&,ì',£\x0016Õ²çReOÅ~bÚAa\x0016ÌåØ\aÁ¹¨z¾K5ø.\x0004AXÒó]>.?é\x0004\x0011ªçºTëò^e\x0018t®®²>ÒK/X«WöÓÕs]ªÁuý¿µV/>Uõ\x0001ªNm*¬ª¹èö¢ó¹tï+ê¯\x001b\x0005pnö©.h\x000e\x0006Yb\x001eWÏ^ºÁ^.g%r\x001e<ò«s\x001a`LßQÍ:üðîã{w_àv{óH\x0005½#Ux3±ùDaäYáâR\x0002¥ô&«½ýþà\x0012«îSYï$¤*!U;¤õYf]ÃE3	¥oBoòg¦4íZÓ3¹ô\x001e_à\x001eë)É ÃÆÏÜÈèJF×Ì(­â8yîäS¤q!½Þ\x0001¤/!}3$xòý\Ü¢DJd!£´_àcMî¸1¡Ýæµð\x0000ÛÏM6¤%g\x0002ÂÝ6ÈâòâûZKbÑq··sÑ(îxßíí%Á\x000e\x001cPè
AÈççm¨è\x0014Y1Àµ\x0005Ã:Ì\x0003E+9~²ëÑùáe"<¼ºÚòLØÁ\x0012ÎÔÃùôeM.#yÆ|\x0017¡X8¬yÆ68[ÂÙF8ÇÁã!\x001c±\x0018,Ã©Ø\x0005Ä\x000b-çJ8×\x0008Gr6x¹qûÄ&ê.7kÞºÍl¾
¶Q\x0006´kñÒË¡\x0012\x000b­&ÿñáö©¿!ð\x0007=a\x001bÖä
ûðòñÎïV÷7¿o£Ã{+m\x0000÷é4.\x0006~j4ekB\x0014=rv}ùÎ\x000fN\x000fÿ^§J<Õ§\x0014U]AxE:Z1zOÏ&xã\x0016âé\x0012O·á¹h¸~\x0019µ©X=üTr\x0012\x0015nz!)ñL\x001b\x001e¶ØJ¢óX§©\x000eË@øºôÛÚÎ6\x001a\x000fÇ\x0008ñ°·V'<Ø
ñú9\x0019x®ÄsÆÓ*wÆcÛwùÓ:¾\x0015ÁnËèh\x0000÷­hÄ\x0013>Ï:Á«òdtô5?®]j=Ù[z²qí¥<ïv®´ôu=?Jy½Ð~Âõ|súÂÉ7ÿ)>r¿¿Ûôû»íÇÏ÷[\x001fõ F¡Jz|Õ3ô¨'^\x001fõ6E+?\x001c^¼?ÝÂµêË\x001e\x001cìÁß\x000fÞ¢\x001cÃÉÃýó·»ÕíýÞ]eÙ\x000fªågò4ç.äê=WòSGãJ\x0017Ï»Ã½³Ó+0âÑéÞ \x000eh\x0012\àj	8ì KàC.2µ\x0019Ü	³Kp]ë\x0005àÆÉ<I§IÙ\þæ¨¸I÷+F\x0016sÛ,áF%Ì\\x0017ÃÕ\x001cqÃª!nÙk"]\x000cnKp»\x0008ÜÓCG!º|ÅYuTÙ\x0016ýN\x0017+¹Ý¢"èÉË\x0007\x0013©Æ:z\x000e×\x0010üÙ]rûÛ/áÆ§ß¼ÀÁ-óy\x001a>|;õ(¡ä\x000eK¸dW\x0018¡Úa\x0019ÛîÔÜ±Ä\x000b°±müIì\x001awÛÒ
\x0005;\x0004ïâ|ôEä6K\x0000yV­ÏäT\x001aeð|äýCsÉ©	`\x0001õ\x0001çâLî\x0003Û\«Ú¼wjÊ%Ç¦ÆjIMäÞ«4	 @éuø-&ï\x001d?rÉù£±}8\x001bWèÑ3¹ásÓ÷\x001e:\x0016÷ü¸\äÈ\x0005Éb¨â¹wÄFÍ\x0007
;µyÏËE®\rÉ Ç×NNº¡TÀNÉ{¾\.ræF¡è4kPAÿn=KÏË%ÞÜÀÒÎõf\x001eo7.{\x0016GD¼kïò\x0014R=g®8óÿeð/WK|ùÿ2xÿ\x0002´Ä\x001bë²LµNzêâCð+D®Â.\x0003[Õ»\x0001©EW <T#GÁNg<Û¼ß2¶¼w\x0008©E `(î\x001d
3Pl\x001bùÖ\x0019úå^É{ µè\x0016ô¿C>Ð6=-éK\x0000~Þ{¿º\x001bÅÔ
\x00165?Ãá£¨ó\x0011VÁ\x001f\x0007KÀ»Ú{06¼ªR%ªRÜBEä\«)"­áËÝð	¥\x0001JPºÁR\x001c=G	´$a\x0010m¹\x0015g(ná\x0012ÇÔãÀí)RgR8(-÷¥ó»Zfj°-¡l=1äÛ£Â':\x0016OÝãµ\x001bÚn&W\x0012¹j"\x0019\x001ck¡HX Ó&Sj\x0016l0/|\x000cs¨nË)Öý\x0004IBI\x0014êä»¥
[\x000b\x000f¹d%­»*\x0018;ßLEâ^¼>ã×P9IÕí@ÅÕí&Ü\x0010\x001bVZ5PõýeÃäFI\x001cZ\x0011H§ÂwÞÒÎ÷²ç-e½»*vu\x000e@µn\x000f«0\x001bzÞIÖ»')b\x001eð¡r
&Ü_â+Ô\x0002ª{õþI(·¯;g\x0010TV¥0F.÷\x0006²ç d\x0012êÕRGr\x0014ÜIØoñlê¹(Yï£à¿KÕiï\x0005-%eg)7¬i ê¹)Yï§\x0004fP:KåL>vèv\x000e!,Ø}±\x0007\x0015k¡\x0014N/
¯ß/§_1gòú\x0001ç¯tÕsªÞy
\x001féÁ\x0013¨<© \x0018KçÒ×Êg\x001b¨zÎSU;Oåìºw¥Ë\x0005ãº«\x001aS<:q\x0016S?Ö¬÷Âê®×[Å¬^\x000c¥ço?Õ\x000b5Uu¬íåûí$yûÈM¬pÎT=®ê}:|ª.Ò)­Le-×¡êµÆ®\x0006ªOWÕ>]y%(Û\x00071§'¡
m^©ä\x000fØsêªÞ©\x000bõÚ·sgø¤Q|ÑKUÏªjÿ©PÇUÔñ7Qv
V;Ð­§êyOUï=±éa\x0017(ÈÓp©ò\Ijå®õÒ=ï©«½'øtÉ"(6üµçÜ7|>?ÿ¤Ñ=O¥«=ðwSCyÒrËîÓ® U/ðéºç\x0015tµW\x0000*=L5Upú¬ê¨æ{uÝÛºz\x0003ª(¹\x0014\x000e¨X%I{!dG5ÿTÖ½
¨\x001b6 t]bCs\x0011\x0005Pu^a­K°\x001eÊô\x0016»iXì,Q»\x001eÕ$\x0012b_¥o*ÓOoÔ/«¤³ÎÝp°çÐo­\x00168\x0006Ó[V¦~Y\x0005MSá²_ÊF÷ê×çoAÛû¶þ\x000bâxgKT2U¨¦#Ð½\x000bq¾­lÏ]Ùzwå^£ua$AI§WÒÌ÷¡¶÷\x0001mý\x0007\x0004\x001crÃÞ\\x001cHÏÐ%¨æ\x0007V¶ç\x0016l½[À\x00067Mí\x0014ÑQ®Öª;Ë\x000bÃÌpxmJSR=ö8ÀB:JacM{ÂRÎÒ²óp
+ÏcJÕØÓ`ª\x0004S-`ø¨\x001cªûZ\x0002³[r½Ú¯\x0001L`º\x0005Ì{¢ò\x001d¦ä\x0010P­5\x000f·@\x0012Ê´@H\x001d\x001e;9bZòÊZòïÀ\x0015ÖKê\x001bÀ\	æêÁPÅª[_ûtåîtµ½Ö Ó\x0002æK0ßb1\x001cK`Òð´iÈ{^ø~­÷´\x0005,`±Åb^Pÿ·ÆQ²"@íå¾z0Ùw\x0015M¾BèLDª¹PÖP
Y»°Þ\x000bÞBÖÛ²iOâäÊü1
N8 m©\x0018Ì¬]¥Àl\x000fÌ¶¹×L\x0015\x0014Éÿ\x000b#\x0014m¹ÖF\%ü Ë\x0005~P8ýïP¡énT(uÄvâD"h¾¯Ó\x001b¨¾C¦ãÃ±éq\x0005*©T\x0003\x0015ö½Ò\x0001i4MíVqÃ¢péK7pé,SÀ¤Í	-±Ý	0¯õj¶`\x0012Ë´|D%ó¬=\x0014Ö$×'-wQY¹©y¯\x0001Ì`¶iué<\x0017\x0007?hTiÈ«<+¸\x000e±èCº\x0012ÌÍ·Xë\x0016Û\x0010ëÔù\x0012ÌÏ_a^­/±E[2`¡\x0005LkV\x001eDå÷péb\x0007&ýÓ»\x001aìõÙ0y0ÑD\x0006$&2¼¯\x0005"ã~yp!\x001b\~=YÏÉ\x00167d$Áß'\x000bÈV°#\x0007m*Â®
\x0000ªÒ,Ô¾{	F\x001e\x0012UôMïµÑô´Ñ\x000b¹¾INUr\x000eç?TqºÐ%}¦T´]ÎÉ*jáÔ%çp\x0018D¬èÊk´è\x0014me'Ý {W¨Ù ¦\x0004\x001dN¨\x0003
üì-ùe£Tà¼;1¨-9c"jµ,¹( (rFî¹ÔÑ\x0001\x001b- ®\x0004\x001dÎ¨\x00135ÝN
\x0011\x0005vò
¼\x0019\x001d3Ð\x0002êKÐá\x0004:E]nWZ\x0018­ÔÝ§;1h(9óª8q\x0002.a¦$\Âìôvûjês)cI9\x001c5T­\x001cMò\x001dÑ³n^¡\x001c\x001dÇ§K4\x0016]!Â®\x000f\x001eª"5\x0007Ðáæ7¤qmxZbï$ÍÙ?æ\x001cI¨	Îr¾Ê°ô´\x0012¤2fµt»X ²w&­
%ª\x0013üøvò,¨*=\x000fØÑ;ñ¡²w(­(ªs¢óÅÚi\x0006U¢S\x0004¶;9dïTZ\x001bXT÷ñ\x001d{Q$\x0015ôñ%ël\x0003éè ¦}_4GÓÞÇ\x001fÌà
ÔC\x0008^?tÛ_vµXAïÄO!oÇ¦WwÅ^Ç¬X\x0015x\x0001\x0008 Ù\x0008Ýe#Þ~YÝ?ßür»%CF\x0007Q\x0004uRóL\x0017ijþ¿\x001f.¿ýþàôêð£m)\x0012=¼ôëîÒ_\x0003·Ìd\x001d=Ââ\x000b\x000cÕÒ;½"i`²%­fÂbü,\x0005P3õj·~Iú\x0000æï}½7¨ÔTØ÷Î\x001fs_þÁãÇmÃjlSmùh-
.¬,ç¬\x0007zý{ç\x0017¹5ÿà\x0002V×øÒêàT	§\x001aá:ùdìÈ/T©¨qÖ*·\x0010NpúOf9SÂ&8b\x0000,Ç*ÝÆ\x0006Vr0<.³%ýYÎp®ÍrÌ\x0001\x000e\x001cn¾h9)YWY÷J­gÀù\x0012Î·ÁáLb\x0012}ÆwHZ¬ùe_Æ\x0016K¶ØÆ\x0006×R\x001aG	¡ig8Ç:ÙbÙ7}'×æåð¹/¨Á:AÂZpb±îSa!]ÏÈ6OcÑIb<y<úªÊ²él?n§ëy\x0012ÙæJ¬vø1\x0013é.ô¦Sw|ZD×s%²Õ\x0018\x0012á\x00086\x0018îó\x0011ÁÍþÎö$ÓfÐõ|ls&VênâT\x001cm×\x0003,_¶çLd7±^Qô\x0016¬Ü0e!D!Ûép¡\x0007\x0017à\x000cDç´eM\x0010Ü©dt§ooÝÂ\x000fÛóu²ÍÙÙN³\x0006\x001cJ÷a­b-27HÊ4Ó©»SA|
VØnËzÁÇïOTn§ë¹;Õæî\x000cÜcríf@%\x001a¦3ªû²zYl¢zBµm
\x0014!å{£57éÈRî°¥çÑaµëð®%úw­½Û»Õý8\x001b\x000em\x0015TFæM\x001eÏ£ï2~­\x000e0_"öN\x000fN§ÉTI¦È#\x0011é\x0008×¿®ò<r\x000eH¹µ¹64]¢é6£½¶4\x0004\x001eÊ®_;Âü4\x001b)ÉL\x001b  \x001dîöJ2¬3ZX+ÌmC³%m@SÑ[.
ÝÊ%Ã].W
\x000b¥Ú¸\ÉåL¢·\x0018ÁìµÃ6´P¢&YTµËdi`p2å$-Öj¥êÈ¤\x001eêêô$÷öËÍ×Û{[>¿ùøåæe\â\x001dî.ª+_4\x0011«GtRî3zÕÛï\x000fONQjùü\x0010þ|½Mä]\x000fU=uzÝja\x0003¦iV<ø4IJÕÎñ\x001cû~>~\x0006+á\#äbÔ4Ø8¹	]h¸P²F6O\x00157ÂpaáIñ=Âv®¢%Xç×\x00060lg£¡#\x0011\x0001YªÔ <F»Ôh=¡LÍ¹ÕFÛIKÆó\x0014\Ê4\x0003ì×kaC\x0011ãØS\x001d¿Â\x0002ÑoÒðôÔ®\x0018Òø\x0016O"¬áé6Tx]î]a\x0001Âõ¶T/Ì4Á¡ÀêÅ&mÕ$À\x000b;Ðú/¦íh¶D³Mh( ÂF\x0003\x000fmæc§Îº\x0016\x0019µ¹Ìµ}Îe$Ìkl\x000f¢ÏIß3J¹^ªÚæK4ß¦^\x0015ejKh<\x0007.Ô$YëÉBI\x0016È$¿\x0005Xï¨ÈhE±¡°\x0001¬ðn±¬\ª!s>ì3Ä¼H\x0001fõó(6*´W ©¡ßP=¿q¾úöðró<~sQ\x0002,EªjxÏ9_å¦Ç\x0018XëÅ{ç\x0007çg×§WÛn.fx?0=ñß·\x000f[5í-üõôåáfg3
\x0017y&°ó\x001bJ/÷ÞMÈÅ\x000f»'LºNÇÀËÇ/«çñÏi°c6'hàJÅ\x000bMñì\x001bø²cçÀ5DoWg×[\x0016×½(Ê/úÝÃý3\x000eCßb8$ù`óL1¸Ðr3¶Ý0¼\x000b¬öÝÙé\x0015\x000eDßö9ãðsÆÞç¬$£µ¶Ká#\x001cE»V­él4Âé\x0012N7Á\x0005ÌkZo.£\x00126îÖÛ&Û\x0000gJ8Óh9½¯23=°ÜªyX\x001fOÕ\x0006çJ8×\x0006¡	\x000e³44Exº)8»¡ü±	.p¡
\x000eÎxêÍôÂqá»âùÕníæ×\x0016K´Øæ] ý6@Kêðèá¢çK³~Ýb[ô"¢qÉ\x0019ªä\x0005×\x000eÂól9»>û²®ïãÚww«\x000b${DdYgë]H×Û­²m»¢m$Ûu42\x0001/YJ×Û®²m¿¢î8\x0006z%)·\x0005ë.ttëÃVÛèzûU¶mXo\x001d
Ê\x0016ÃËüa¹ÚÙsv*àÔ \x001aPÌû\x0001¢¸Õçmç~P2 ô
<¬ÃûnÃzÖõÞ\x000f\x0010Å\x001d¼?Üvè«Aýt"SMd£¸\x0000×\x0017¬­JdÝVÐëÍMh®Ds-hQDjÁ\x0008ðuyô\x000f¶\x0014{»~è7¡\x0012-´¡Y~\x0006Ä©ÃÖ\x0011èæèn\x0012XOöê~°å¤³*4OÞ\x0017®2\x001aß3\x001a%_¿ÿ5¡õl[kAÓ
w=Å\x0017ú`ù%Æ°æÜØLÍ´°aË|N½\x0005\x001f\x0004ÎS~v\x000ejÓ¸Ì
6aq¹MqùÑ×o«§§½Ã¯·w7{o_\x0000eË¹àéí4zË\x0002@p.°|\x0005ö\x0016xG'ç\x0007{p8>Ü{{}y	?DÔ%¢nEBÑ\x0007@\x0014YÜ³îEo\x001eÈ<B[\x0012ÚfB*sæÞK*\x0019Ò³ÜïëMÍCô%¢oF´\x001eB\x0002\x0016?ä\x000c°\x001ct&\x0015±¥±$Íàï¨
W¢!DQ¬D·\x0014Qö7KónI\x001f:Ç)AÜµT~ç~ÝR#â0ã*b\x0019\x000c|÷0\x0008Æ©DX3\x0002\\x0006£&,HS<9@Ôußp¢}w¶-\x0003Ì<ºäÑ<Fóü:\x001cwB9\x001fÁºFQ¸
ÃEël	dkl`I±hH5\x0002iI\x0015,6\x0004¿ar\x001d+\-\x0010ôyÔ:f}ñøJ\x00162$Û\x000c\x0016Ú4Ó¼\x000eÈ@¾\x0016ÈËîaÇF6\x0010?\x0011
çµà\x0012'TâhêÞÞ?\x0019Génùl\x001a¬^ESÞ@{!Ð\x0004N7ê\x001d3¢\x0003MD"R¢(ÊõK@-ê\x0011©Úï¥ºæÓøOµ\x0013d£õ·Z"Ó#2µ6R1Wu\x001aü¥ð¥\x0016$\BH¯(L\x0011­àèyÅT*6&þéq[fÙàkO®Øñ\x0016Lë°´Jwåé	Fï.¶å;`U\x0002N\x0003\x0002ÆE\x00026Ü?ã¤!qMíe¯/a\x0011°.G\x0000LZ8P¥»ÇâÙ|y¶ï=+,â5%ï¨ôÿ$¯ãÙgXã\x0018xEp;C°;ãu%ïèÔ)^ÇNÚ\x001bÔ&¢\x0005áy¨sfé
\x0016rx±¶ð?øúuËHôÀÊ\x0013}B\x0008Ý·W\·\x0017×õÓ\x000bÎÙÉÉÄ\x000c\x0002;\x0014t²½\x0005ZÝdIgy°®gµ70ªÙS¯G3%iB{m'h\x001dº×º³Úú\x0011ÜæJ4×öA»êdÌPh~17lµu=ÁJ´a\x0006Læ\x000cØëã×ûÕÝçmfBkdä£Æwe\x0003Ëî\x00043RwóþàxBkm88·æ7 \x0019÷ý-ºYªÈ	\x001e¬\x0018¬Ü\Þ2¦;Tõ®þÀvòðrw;Vå\x0005_T·s.ÕÚ O/\x001aºTz¿Ë/2vrv}|´­þløA(eîþçßþãàÃ\x0007¸iÝÝ<~\x001eo4Óp©ê$H½ qf8~Ë\x001dÝF-±½7oàªu|xñ~[\x0013Ü0»)D©\x0012T\x000f©\x0014?H(öµëf8»I·®
Rz\x0006¤\x0011´w\x0001ÒÒ\x0006ýÚ	ä»M\x0012cm¦d4íxi¥Ë\x0013Î6½îôò7	Úµ!º\x0012ÑÍ@\x001b6«w;AÕÞ:ÊnÀÝ$Ó\x0008\x0019JÈ0\x0003\x0012n¹T óv\x0014Uâv×ne7ÉjµA\x0016\x0017(ÑÓËi ¤å\x0008´eÐùÝXÙ5ÁÿvÄÞÆ3v6|YÎ9*+;JÇù2e×\x0013ñÕÒ
\x000f=}dý²wq;QNÍÊb?O\x0007³Î\x0010\x001a¸CÁbýî\x001a}½wq´-ÌLªdRÕL(\x001ehÖ5XRúæ\x0019R§6(]BézCA¨Â]Ý1t|, áOr>)¡L5\x0014º:Ëúæ%(ç:ýB¿i@ü$Ô°óA¾v>\x001c?¼ì¯\x001eo·4\x0008TD\x0015 Ñ\x0012pD°DC\x000f||v½w~pq´-¸\x001bv\x0016È×Î*(MÖ\x0010\x000b7<Än4H\;]+ Äpó	×+P;üøåvË¸5\x0005·-zH\x001e¨¯\x0006\x000e­ÀÓÛTÎtøöû£m0c\x0012+TcÁ÷¡ü¾ÇÒ´ÜP«Lì¢à¾¬R#Uáò]¿Ðp\x0012\x000bbK
áâçL\ºi±aoÓÃþ$\x001c~Di{\x0001pÅ|»úúáåiÊ)l»n&\x0000êSä2!'\x0002Ï\x0004¶º08éc¾=8ys}¹í0Ã|µ´åÛR-dû¤~§Å>ß©W9µ1R¯CC;JÙÛ\x000cÇ·OO«ÇOÛêJà¡BØLV¨\x001bHÅ\x0011rã\x0007>>º¼<¸x·ÍyÈ¡ï¶¬«@ógÄSå:+)Ù©¹µÙ~udÂ
\x001f^Ý `óÝÃÝ×--6é\x000cÈ"\x0004|­¡#Ç\x0006÷u\x0003^ïïÎO\x000e·]¾Ü° Ò~Í$û¤w\x001d<5ÿÀ\x0005A°³Q{\x001ejÉLIfÚÈ<©¡`¹·¥c\x0013,ydrXÞ*òÖ½Ë«OãYo¬\x000eR¥\x0016}ÎE¤ò e¹*8lª&¹¼~{ðnk.^\x000e\x000bHeQ@Z\x0005ºü´ïiØ@m+~PÝð>PÏeK.ÛÄeº2j<A5sùk\x0011/Á|\x0013\x0018-1à¯öê°6\x0015ÔcÅ\x0012+¶`\x0019noH\ùÕBD+_Á6<«TÉþÊoZú6¾\x0016øné;¾nÂÜPãUAfÇµ½Q³7{\x0017«O7\x001fî?mÕÈ\x000fTyã­b<\x0003Äv\³[\x001avp¸wqðîðýÙé»m'§\x001dÞ¬í
­CÌº¶`<Azsp\x000ct\x001aëkíxºÄÓÍxÖ²Çþ{G¡.bù8üºí¦\x00044Í\x001c\x001bÁ¥EÅpòáç±ÍÃ\x0003«\x0008\x0019&	MY\x0002ùöáåÓÍã¸\x0004¯ÀÇFzOÇ÷\x0010
.aGPÅWnÃ¹ðöìúÝáÅ6m`3L¹×[
\x0016²do\x0012¢Ú×\x001c\x0014Ñ3¿Úô°^
åJ(×\x0002Õ¦\x000c.MmOTgã\x0005±>Ò¢\x0006Ë\x000f#5ßÔrBèðãÃÝØ\x001aÃâB,vì\x001elnÉ\x000b2\x001bø`´!îÀ\ÐáÛ³ã­\x0002úÃ`Í÷µ*8L¶¨
\x001c wIÕáÙôøÑ@§K:Ýj:&sé#\x0019ª\\x000f\x0010t×ÿ¦Õ¦®¤\x001aºá\x0001!^\x000fóÛÇÇ½w7w·7[\x00121p²&æóì
Ì\x0014u)¾µYFçG\x0017I$ãøâèpkiæÐu¼\x001e\x000eõxThqPâ.|N}¬µçµ²éM·²¹îI!¸\x000e_=ÂZçO5\\x0018~×°á^Ï%ûã\x000bÏuéH¸\x0017H,ÜIíÛ\x001b±ªZó­\x000b÷§1U©Ú1mÔ]·¯NÕ©l/hî\õ½òý¹¦Ä4s¬	ÞYR)¿fkÈ\x0015ÌzcÕc-¥j\x0010Ia½@I	ýÕ/«ûO[Þ¨1Û\x0015~yüµ\x0013«ÞHÎ+µ©N8Ýù\x000f~88}7ñR-\x0019V)z/@	ÁÊx¸\x001eXaâh\x001e»¡,k¯óØG^]\x0001ïp[À,V)z_º\x0002.§í\x0013sû^<¸ó\x0000n\x001bfS
s\x0003+á\\x001b\x001cJïS¢\x000eåIÈr]ot\x001bW`=[(ÙB\x001b\x001b*ïá\x0000ÆÒ\x0004VÍ\x00190\x0008l7®»j¸¢Í[æ¹z:\x0015QîCuéCËóµù!Kõý
t½
!vÂÚ`z\x000cÄ#GZsm¿ì£-tÃñDÒÕÔ81iõô\x000c\x001eeïûÕËA\x001ap/áÈÔzá_ªJ\x000f\÷iÍz\x000fîutpy\x0005\x001eeïûë-\x0011ª\x001cÎ\x0005¾,²®Ç4å«-\x0004\x000eÔÆ¡µìú7ÝÄ1Mif`b:Q\x001a\x001aU 5\x000boX«6\>!m	ig@úÈ\x001bÚj~¡ÚK¦\x0014krVs0}éÛ1%NJ$LX¤D}\x0004\x000b°.0\x00033q\x0006¦d©W\x0018Ü>É"I.42\x001b\x001e¦ê)?\x000cËßPyðñ«&ùÞáÓ8\x001eÎ¦\x0015úÂ- }cTo:Z¡E¾wx¹íæ9¬Ð\x0012¹B\x001e\x0016××\x000fÛîÄ\x001a§*¡í1\x000f* ëî'\x001e\x001a×Éí×b5¼y*Q¼õWÁÉÀ·\x0013ÕÍ\x001cAÁ\x0002bÓbÃs\x000b)ÙL\x001b\x0013_Ö(u\x0019aÍñc¶v\x001b
$ªàäð«ÊaÝÝ­ÓÚ±xfl\x0005E/?p\x001a{cB¯¨8ïÞ\x001cn+\x0008\x0014ÃA§"Í\x0017-ñs×íÑ9çG)ø#g#ÞÖEùý¸ú\x0004\x001eáñ¦ûC¢ÓÿxÑ?Þod¸´9árùw·Ï{ç\x000f/?= ¹ÊH\x001aV÷÷7OI9À¿¬\x001eÃ;\x0008øa#rt1\x0018\x000c\x00061¶\x001ew\x0003\x000em\x0016*P\x000fNO\x000f/ÿÒ|99¸øÛ_áÆ¹÷îèjïüìú_ÎÆØÃ\x0004Ë©yÑEÌ$ fpI\x000b1}Z{iÀËøaB gZ\x0013\x0015\x001bM¶&\JRf\x0006¬\x0019P7,YSQj|\x0017°{Í,L#Ú.[\x0013n\x0000©ÌÈ phD²¦¢¶¶]`Â/lgZ\x0013\x001d\x000eYS»Ü}\x0007FuÙlM.	Ù\x0005&üÂn¦55	£5E®/\x0007k*\x0013ØRí\x000c\x0013~a?ÓÞæ¢\x000cÀIP<Y\x0013Óæ\x0012\x000fÀ]QË\x00083õ"´4­ÃDb2fÄF¹Ã	§Ué¤ÏÝ\x000e@¢wù'­L	ÿ]aâÅ4ÍaMóÀhizÏ;(¦a\x0005Óî\x0013\x000f¡§PÌª£3¤»~rïÒ±C"í]`Â/,çBè"s\x0001\x000eIê,S°V9a\x0006\x001a+½\x000bNØ@ræ&RNå>!ä¤×\x000b£0ÿÇ;;Óñ!çí"£²n{çß]ÆÔ:²;;-\x0001æ¯jæ.J3¬è³CT\x00147Ó\x0008H>Õ\x0005M	Þ\x0005'ÆH3'Äå¹b\x00068EJ!§òÝòô~wö®æEISÒòLJôÄi3î.Ã05/þÀ\x0016\RI8q\x0006ÇAg»ûîp¬©\x0001Ñ©\x0008;{Ï¤A\x001açX±÷ÜÙ~Çæy5/\x00021\x0006BC\x0017\x0010¦±lN/væ=±NÍô8sÈK:4UÖð\x0004Në_\x000f÷Ým#X@j¦û48ÝÝuAHÐ3
^¡Ã}g\x001dï¨zÞán,>eæm\x0014tªjEÎ<û=qJ»0¦ûWùÓ/¿\x00147á.«\x0001·ó÷«ô\x00067Éõ-y\x0006L\x0019µnEð«câ\x000f8½\x0016z$XêR\x001dpe0ú(×\x0003ÍwáY ^¥Ø\x0003Aá¢"÷\x0008*5ùy¯ýØ\x0003¯ó@µÊÙs\x0000Åj|\x00065-\x001aÆ\x001cÓ\x001cÐ|Ñ\x0005\x001aÜiËGdÎ\x001e\x0014/ëdQ+G\x000e¤9ù
7\x0013Ü{à,wYô
îi"Oâ´c7â\x0019 |ñGªMÊÿ\x0002¨0\x0014ÂáÁ{ÉD9rtÎ\x0001¥~\x001e¨s\x000cÑdQIÎÞÃ¿aÄ9Í\x0001$gn¦Ô¶7}Ð\x001aa\x0008jÓ\x001c\x0004\x0004u".õNß~U\x000f?}Ø©{·úDZ\x0015Wx¸}ÄdÒ º°^$Wára*ÓðþøàÝ\x0016Ç\x001eê [×»ù\x001e\x001f´%Õ\x0002ì1jDT\x0007«c*ÂkA\x001ddì\x001a­ªÓ8\x0007¸vØ.ã1(\x0019UÙ© ¤t´k3*lý4\x0006@\x0006B¤B¾%;#É¨rì\x001c:HÜµ\x0019ÕçwS0ª¨RÝåÙ¨r2"m!\x001däîÚªÔ¾Ë+U¡XÍFE\x0001ÆdT\x0019å.7Õ 5Ö
(y¾\x000c\x0012â(\x0015)K\x0012=¡²0ùNP×ÒNm¬XËî2«§\x0012,ø\x0005¢f³ª±\x0016+¬&9ÛYI\x001cBvµ\x001aëÚ\x0013kjPN¬Âìp	àE9Û\x0007HÿA¬=¡Ä£\x0015´\x0006\x0004\x000b®.`}þ×¿Ý­6\x001dWØþ÷øpûk
*ü#Ý¶I\x0008\x001bî|\x0001Ø²·r~Ê[aGàÅÙÑÿ©!\x001d\x001c\x0001m¤Xç\x0017«»JÔS8íõSµ\x0005uàXÛP£É¢Ý8Àe)`
·iÉVEÖÝ¡\x000e<k\x0013ªãÑ0\x00195\x001d\x0002¨)\x001b:Ò]~ÿÁËH\x001b©ä|\x0014ª\x001c«â88z\x0004uÊ©4y\x0003êÚ»C\x001b+§Öªû&£úÀ1|xhA\x001dæôÛP\x001diC#ªÙw5HÉA ºîux\x00064±\x0002\x0016]\x0000\x0003ÜNñè\x0002VTmdV1âma¥ûÊ<VX¹X\x001cì*\x001c\x0016\x000e£]£ð¼³:¯ZXçU]c \x001fvê \x000fÚUâ4²«Ûåz\x0005¿*gûV¸UQú<¤\x0016\x0006í\x001a\\x0017_OæÓZXÁ±ÊÙÎ5*RuÀ»ÊrXX1Ë¬\x0010\x0012ìr½\x000eßÌÚì

ÅW
BØôº§cJy]Çr\x0016³X\x000fgmvõÝ+ªý¤§	¬~ç½±ÌîX×\x001eÏÚìjl\x001e¦G{Ëf»êî\x0015yê\x0016VðÕJÎ¶+¾ð\x001a²«ãõ\x0019\x0001¶ëò¸å§»n\x001eÜ\x0014·<üvd²§A5ªM\x001b+J¦éb\x0001l\x0000=9ûÛé¨pv¹\x0016	4pª\x0018(k\x0005Çh~Ø×\x0010½xÊZÉ¢zÊáÁÚB\x0019B¥BL±=*\x0004\x0003\x001d¥\x0000ê1çTËG\x0017*ëì\x0002¦§y\x000cÀ&c'Î(§<ÿ\x0004ç·Ç»½ßt§:¾yúv[S8^.=ôé$^âÓ.2ÒÔµ@·l¢ÃËóñî&ýO¿Üù~.ó\x000fÏ·OO7_oîÁ¢«O/÷_êl*46räð\x001fU\x0013Òc
,O¼K§äÔè·?»:º¼<<9<\x0005³\x001e¼»>ý~a\x001f\x001fï_m*ÖÄ~Ïïo\x001e¿Þ>¯>×e%Ï\x0008Êï?^\x001c¬·rNjïûÃ£«Q=µ\x001eòð~Ý¬uH
å° Pä/¿[DÔ	Ë\x000bÂNu5\x0012\x000fïÙÍÄ(\x0003#Bí¢æª>ðµÃô"nC\x001eä\g £<p^\x0016Xã­dà8yiã\x001dæ\x0007y­÷xÝNÀFe©~#§ú\x001f\x0005Ç.²·æë¦uüvu÷K]BKIÇIm«0þÎÁ¡ñ:_¼´Ñ5+o\x000fØÎ*0\x0007+¡\x0001\x0013õ\x0002S\x0008#9|ÁìRËÉ«l=åàû·\x0018\x0013ÕTÆ&\x001f·\x0011KÍROÖõÖS\x000e2Ù-ÆåÆWiBtYv\x001f>98L\x0012g·ï\x0008s-ÄjáÄÁ¤é£c©q.§\x0002NEïm\x001a.SÎµsmoá´\x000f0øèjòÅ8Áö\x000c²ê1	¡¦Ï®²Ô>`ÂA\x001bò\x001e2TÍ
;hòI°\x001es\x0018²6:¤\ãiÒù\x001d\x001dR¾¬j\x0011'k\x0012ë1i &kú<©\x00191mn5ÀMDÇ(pÝ}õaª¢É%Ez´Æ1uy¬\x001eú¤Hþ\x001dõwÆ9LS´pú$l8a³\x001b\x000e­-ùÎ|©Ü\x0011ç0EÑÂ\x0019%\x0015}\x0019/M\x001e 
TU¨s°+ÎµôÄL{JIWªÈ\x0015J*N?«Öc\x000eK{0-¥þs~_\x0006Â¤\x001a:\x0014]Ê¡Lpþ&¿Üü´)J:yxyü¸úíñá®\x0015gi¤>Aéièh.R\x0012ôªîEEjâúâíÁß.ÎFG¢÷\x0007% ÍÀ1õ@!°\x000bËÔPå*\x0003;\x0017§¯ÕMÀÛI»]V`\x0003àh±.ÊÀ,\x0001|E\x0013ð "m·pÌJ'\x0000ltN\x0008 #\x0003k·c\x000b\x000fÓfà.¿ê\x001d*\x0000\x00130Êtfàé\x000bk#ðZ*°
8
Ò@\x0001`á©ÈVè@}SÖ	½ãM7xÉl¶0ì´ìx½S¦ó\x0012ë­aê k\x0004\x001eÜ\x0004Ú-Ì"\x0008\x0010Â>\x0015
Fº\x0000Zk'\x0001Úx×Bíf`©©}Ò[\x0011°q)\x0013\x0007²°l·Äë\x0019ØFb\x0015¨/Õ\x001bT¦IÕ8Âp1¦5v2ön$\x001eF¶s\x001c[n\ó\x0016V±&?\x0011¤$\x001bO§0\x001a×ÓÇ­-ã\x001ag\x0011â3ì+'\x001b®\x001ai\x0011y3­v\x001cKh¼>fà®\x0003X{=k\x0004\x001eæí\x000bÂQ?½72 {>éøh6zòa®x-øm_\x00102\x0002`AI8\\x0013\x000c¬&1À°ßÔ¢=ã'ò\x0000àÜú³´ÁÀ;¶ð°¬\x0015Ø£TK\x0002Vò\x001e\x000662¹\x0008åÂ.BO\x001fÿùaÓ\x0003Ã\x000f7÷·¬8tÖ¨0\x001dP¨u¼\x0008S\x0010?\x001c^\x001eU¢\x000e®\x001aM¨X\x0000\x000fd\x0007§/jÌàË
ðQ?Ó\x0011D\x000bê foCå±7`Ua².\x0004Îl¤Ò\x0002ãXÚq\x0001j\x0008ßÂóË&Ô·«ß\x001fîVÏUOBË}ï(Igös10ôP£¥ªH ÿýìøàê¯«Ç7ß¶@®%¹«!ñ3ËÖafVò]3ÆN\x001d\x000bLYaÍµ<w5îRZq	\x0014ÜÔL¥ÎÖÔnÈ!7Ô\x0004ºðT\x000bò >òRËÑ\x0016¨9¤ëYäzR\x001f\x0014¤\x0015mê½ò\x0013´5
¤ëä\x0006*ÇäoF1ÛTD6étZ¾s=Ü`Qmé\x001d\x000e,f{ §sÝvRwÇ\x0006Òõdr=)X»ØYÔf?\x001aTàä¼,)l \x001dÚ-¤83Ó0)%ÁÀ¦Âv\x001f²¬tXOØdSEfðùÈñÎ]¾¯]¦\x0013\x001eC¶m×+rù¨#8Üôz²§¨Þ\x001b\x0012µ
 2æùlÊµ/ÞÔèÝ¹§5Õ¦%
{Ýär\x0012«Ê6µ\x0002i­*
«AýøM ÆeEq\x0000õ2ß©\x001aí%5È¨'Õ°BõÜUj\x001dM³\x0007RÙí%c»]ï&ËÞ§H?ÿó7\x0017o\x0007aÞ^\x0006}zZALúò{]Ê»\x001d+lðü4µÐ¹òÉÉj²·\x0007\x0007\x0010^ÿ}¼ü¢\x0000~
ùf\x0001ã["5¡t¶£\x0007dI	-g¦uC\x001a_C¿yÀ!ìçâg\x001b#öCå'Z¦­8\x0001h_SÈóhU
¥y¥á§0\x001dhñºT ±Sà×ì,`jnp8,Q¿3\x0003ËI£\x001a`¸ç}øð<ÒgöÝÃã\x001fÿ]å\x001c0õÀ%jç0+í=*ÐB\x0001©r'¼8\x001c÷\x000e\x0005ëz§Y\x000b«ôÂC"ós8¶\x001bÓâUZÔôÄlgÕ¿<üüûFýÊÕíÝÊQº0¹r±i	ø@ï¢6¸ÉÓöüàèøû-\x000f£\x0005æP¿²\x0005\x0013prÍ¦GI.\x001fpàDq\x001aÔ»3Ð¡e\x000b(\x000e:2hÈê7`QCÊb?Ôî@ª
 V¦\x0017Üb*)ý£Ö©µDThÛÕ\x000e\x0015
[@½£wy ×h\x001a!{
¼Øá\x001a\x001d\x001a¶|zøÞ,Ü\x0010\x0005\x0014\x0005Çç«ÐuÅõ ërM¤*);)©]K¸iýÅ	ÒO?ýö¢î6\x0016lßì½¹©j'1Þ¥aXè­Y]DyÇw+ëät%üÞÃñf\x0002sx8Õc¢L¦âV§ñý"É`à\x0008)&\x0015¯ê1\x0007¾©\x00013\x0008·OÆÔÄuU¦3æt¹p5åðô¬§\x0000:s¬©\x0008
1
+uàkÛdÛc5æ°\x0006»\x001eÓá\x001bv ¥éñ"NqÂÏºÉ\x0002ÂzÌa×sÃ\x000e²,\x001efñµDÎ<Wµ5'_Oê1\x0007¾³ei\x0006û\x001bðù)wæ\x001b|§<¯Ö\x0010¨\ó
Ñyª¹\x0000LIÊ\x001c\x0010Ê\x0005ÞçnR§s­Ï¹Ó
øÒY=\x0002Ö¦£ê\x001b-¼bsºÉ^=çZs=¦t$pJ\x0016²\x0018r=pïßÙâ\ïon°§Q$\x000c
"_\x000c8'n^\x0000Î\x001dCkÏ»
2Ò¨)¦ø\x000eZv\x001dÿË»â\x001c¦Î\x001a8Uì\x0002ßëT´Ñ\Ôl¦V'8o~ùÝ0õ77w_ó¼\x0010ÙS:*88×½£\x0010díð7²çÃã\x0013\x001cBP\x0001:82Û@C\x001e
 $ÃR,Ï a2k\x0000\x001d\x001cm "%ÔÝ Ü\x0018Xb×MÇ
À&N|e&Ó·Äé"§FìäãS\x0003èàÜl\x0003UùúÝ«"Cfâ¬õky- ©á:÷ÞÊhxzA×M\x001cºµ;®\x001d-¤à}¨9\x0004iIÐ&W¢1\x0004ïtx,5ZÏ*Q(\x0008léë³ºóÓ\x001dVS¤"þä~ß8$å\x0004(ï\x001e^><¼Ô°Â!\x000eNd5N`5\x0007Vñ8\x001dÉªzRú\x001d9Ï®ß
êìÑ®\x0015á7Ñ*Øô\x0019VjO\x0012|"\x0000/Ýa5ìv­\x0002¿Ù¶ô\x0010!dn´CÓ\x0006jÁ6RL\x0017Q¶Ð®ß·ÙÖ
NHï³\x0005\x0018WFÂ²¢æ³\x0005w­ø¾	WàT>² bÅ80	bûr¶®­¨¡lÁ]+½o³®\x0011ôØ\x0017$9.°®è\x0014cìdÃX\x001bîZá}£uí¾É!\x0016ÜJ¸QÀ\x0006Áh\x0015Õ-´kU÷mÆÕîÕ¸$\x0004Å« |ëo£]+¹o³­ïcp¢¯ÎgÁ83]=Õ»\x0016\x001f´º1\x0015©,
üX\x001aÀü£â¹Ôê°SÞõêõ6û\x0006p¶ô>iI_8~\x0000Ç`wkÞaJ3®¦	8À8\x0015\x0004¼ycEõú$ïç{¥~
\x001b_¥\x001eW÷Ï·+ÅZTÐÞ'1?§bí:%[\x000cD?ÙôÓ«£÷Û\x0004[
ÜáëT\x001b.Ê»<D\x0002E\x0004¨¬:½M$\m&«ÛpoTÖµÜ*âUn·!åfÆÝ)ípY#-jåªjÏVÔÇà¨%2
\x0018Ù)îð]­\x0011\x0017vZòc6âx@Z¹
\x0001 \x001cô»m´Ã¡fm´\x0011â±\\x0006`\x0011äpãÙ¢b^G\x0013îð­	WK\x001ds7õ!îç\x0016'/H\x0018UG\x0017vºÍÖ§5\x001a\x0017;\x0016rJ.`«tn\x000f1D0àoM¸k¯Æí­[ºÈ¸¾+À\x00052ù0ØÄ»6M¬}ífÜ`\x0002ß|¥«&eÛpyFó*ìdÉ\x0017\x0005^3®t\x0007Ö)Ç°KÜaÓj]/»Å«lî7fºqz¶i\x0013î0\x0017Òh]\x0014uÎ\x0013\x001a-¬^n&Óß~ò\x0015©
w\x0018µî5Ëór¬×^°þVCc\x0013)fò\x000e	\x001bySüªdá<6¤èÅÃ\x0010±Gor\x000eQ\x0013ïÚ\x0004¿Fû:MÿÖ\x000b:'4?8]ØÔ\x0002»VÝìx#ÃÂÂÐ,ñ:©\x001e/ÚÄ»6'¯\x0017Uß³"\x0001ì5n{ÄÌ
=\x0001ùN=ïÚ³X+¯µøÚyM§Ö){y7ù×Æ»67¯×Á]òlôØZ¼ZÑÝ]Ã¡±[Þµùy¼Zï³o¨²qYCËO'LÛp×æÓµá¢FQÖ©µV³>\x0005J,Qí¾ßñmm}N]£y¡\x0011°\x001c$/HXñv-FM¼kUü­öÍ:0\x0017SÒy=$ÅÌ+uÃ\x0015hccL\x0001»6\¯\x0011\x0016KN\x001cû²¼\x0012xZ!öqíô\x0014ÆøY/p¼\x0001\x001c\x0003G\x0019Ô°Í2ÖS}©ÆAÅ;åÅ<Ã×\x001bNð\x000b6$]*
ï37©\x0007ÝF\x000bÿ6½Àízìé!Z#¸ÆÜbþüÂn¯¨£\x0017¸Ý\x0018Y+*\x0015Nåiß¾«q»ÈpÏê\x0005\x0011$Ä´Tåeò=3\x00197peËû.q±\x001dÀ,Xº\x0011¢rI¼RÒ<`é%¥ûñÌÛÁbÀa(\x000be©3¾\x0006Qà[£\x001e~OçöÝÌMÄ\x0011©\x001f¾\x0006+'FÿtXù\x0015òÏõÍ}úÉþsc½\x0011N}º­\x0014ÓÆZ\x001cUG¢¹ù\x0011V"D;yl¾Á©OGÛ$Ê_Q\x0007)ä&TP\x0003Ô(Ë\x0001*¸GC¶ÄÉÔS½\x0005uX\x001cÕdUË\x0015ÅQ	L°ªrKO&\x001f\x0019[P\x0007©î6«Â5ËEìÎ¹íÙÀVUq¨ÃJ®&«\x001aOÏø\x0011Û2\x000cuJjõÂN\x0016ñµ \x000ek¤PìÆ\x0013(ðÁªp"T3]vVºmc\x0015>Ï©Jª|\x0002TG>8«Éj\x0016Ôµ:©¶\x0015\x0010÷y[qû Ç1k]E×ÔqÞºV(Õ´¯¬àIÊÊ¥\x0002	dÕQpõÙäËò$êo·\x001fÿ¹zÙôðùþñöÇ\x001fo^nïîªú2
ÔZ\x0010à°ÃóÔ¨¡åî09Vóâè»ï\x000e¯Çû2\x000bàá\x000cØfà®\x0014j³R
Zt­d^«\x0011x8	¶\x0015\x0018î¤¹=3H')±­|à¹µ(û¿[àá@ØV`«rä\x000cäM	<huz¬N#ï N¦\x0017<®¦V¸@Â=\x0000,¨W×	cv\x000c<¸Ú
\x001c"uù\x0008×Té3pìFÙªÉ|[\x001bðÚÃb»5)å\x0005U\x0010ÈKÈ®FQO\x000fßm#^\x0014ÛH\x001cáÖX\x0014Ú·Ô=Co6é¦mÀkãbÛ1\x001c#á9¼
¦!aFKáy\x0010·|\x0018o\x0004\x001e¾×µ»	IÏ·>BPÆ\x001b¢p<åÚîøäXrÛjbÏs¸ÀÆ\x0001Ë©\x0015UW'ÓoÄÃW»æU,5U}Á*æ\x000f\x0005a\x0005w¢Ç89F¸xø\x000eÖlcÐJë\x0018F.MÒ"¾n¼É6\x001aâçßÿôëM\x0011\x0000½¹yzºAÇ:NìS¢7\x001amp°<Õÿ\x0005ºüÈàÇT®ß\x001c^^\x001e¢¾c\x001d^¾¢ÿiñr4öçÂ\x0013æåúçÆ>Õï7·Uq¸>òüU¯,5pÆDÍb'\x0007?<ºØ\x0012?<ß¥ÛÜÒýf\x0019>áÖ©ê\x0012üS\x0016ùñ¨?BÓ­%b³"L\x000f\x001c\x001f^¦¸{Æ\x001bæÿùA}{\x0014cè\x000f¸FXÁa«©\x001d\x0008¢Z\x001aÆÏ5ugãÂü,ýÛúöpÍ®>U6
C³ãmtGHM²fÌÝ\x001e®Þw[\x000c[ ¯õÎ7"C<È\x0019áÕ\XÑà8ØyU¡x8Ô¬\x0018BCOuÂ²&\x0008+'§çÇ6\x0012\x000fg7\x0013cS¢ZO·OSd=\x001d¯ðÓÝ¬¯«_\x001fíèÞì¯\x001e\x001fê:¯ôú8û:ÏºÔv\x0015Çß\x0005\x000e÷Î\x000f.ÎÆÛ­
*ÊÍý\x0019¨>|¼ù²yø"âUª»¥Y1¹±\x000e\x0015\x0008hþz4ÅØé\x0002ôºMÞ­@]÷¢Õ¨\x0012b#ñE¡÷üR\x0010\x0013ªr®-¨ë\x001eõV\x0015\x0000Q\x001b½\x001d\x0013|Qnz´M\x000bêº°GUQu¬J>4%ÜPÅòI\x0016Ò5×ÙBç(\x0019ÕZg®<Õ¨6-¨k>³\x0011Uä]¥âQÖ°B\x0003¡¢ëÜ\x001dêºÆG\x0003ªI¥6	\x0015NÒª\x0012TÆ¯*&\x001b5 nRú¨gÅRø¬6\x0007kÕç$,õÖòZ¬hjaÝ NÑÀ
ÏJ¤Ø`OÝêBÑ\x000c\x0002\x0015*fN±>ÝùP\x0001÷_nïëN&àâï	¤\x0019¬£*xíÇÚM\x000eOß_\x001fn9
®ìðÿ|\Ù»ÿI¸~üôøçÆÛÑÇç/µ
T®ª"r¤\x0005ç vÏwMpÓÂ\x0018\x0017Wß×q®	c4pâË#NM2ÒÑrø.swkº\x0018
ÊQmuDE\x0013]q:KÂ\x0004Ç¾ónõõgóë¨Ð\x0019 þVµ2­ñT,g,Ü-R¢\CtI3q´WÅ
\x0013aÿ6Êú¯úþãÇÉãÕÇÕ×oU&
¨\x0018Ç9c-\x0005UTkË6\x0005úi¹Ð·\x0007'ç5\x0000®\x0005\x0013^2p3¼ÖT K×\x0017Q>~ºùåÅnúðÇ«ûUUë¨ÀêÞôÖ\x0000g5Î\x001dËoý&PÑ¡~~:>8=\x0018o\x001a}ùpÿ-üºñß<}ÅY©k"y>\x0013Dí§{:Ö´TÚO*ÚÂåñ\x001cVçc\x0001;4h\x0013¬ÂQ!9pK/ÃZçi+áUx°Ã5ÚfY!¨`\x001a k\x0013%Yv¥üä\¦&ØÏoµ¤2DiÚ§sÔü\x0001Â¤ØH\x0013ìà¦Ñ¸\x000c¢$Q9Êü&\x0007¬nªTMÙÀ:8¤Z
ÛÍv\x0013g¥\x001c³ÒÓïKÓ°ÒÕ×\x001bO*Ô`¾¾­JãÍîp\x001eÕú\x0002ÅP(«Íd~Ò`>½:\x001aÏ\x0017°\x0004£ëaEè\x0006µ©@c\x000f<åJÉáiØøòÏç\x001bM<ÖæàS"\x0007\x0015Ï
I^Q"Ç%¬ûÆÅ¶¤S\x0001»®ÒÙ\x0000\x000b\x001bh_Ê®PQÕÔàbMÒv
ö§Gëã/Å\x0001vñðò|³÷éþí?\x000e>®îo+Ó÷\x000bitqßüÚ`\x0015k\x001eÄ±\x0016Æ³ë«Ã½w{o\x000fN¶S~\x0005ÍK`\x0016¨Ø½´ÆyºÉû(i\x0016=cYÚZÐ\x000fþîß?orZ=þürSõñáÓz<«0®åÉÓù\x001c{W©äd\x001b ü§ÿïz\x000cûW÷Ûç±`õéiõù¾Î\x0005h¥x èÜ\x0015ÖôÒÂ\x0015àååÁûÓq\x0017ðëJø&6/Ô\x000bªHËÐ\x0002fI\x0004!¹ÚÆ±\x0004i·\x0000¦nª\x0005êÚRmºK{J=é.­UêÐ(\x0018ÏÂ\x001cc=\x0012s@s5\x0017ÔtSî\x0014E\x0010)ÇXF±ÊjTÿóÝ×W·7w\x000f[¹XópÃô.*\x0003ÕT£\x0001=ºÉÒ«£Ãã3\x0000\x001e_¬\x0005íàpm¥5\x000bÿ£÷T«\x001c0
I¸j2ñX«Ü/ÝS"kñ¨8BÆäÞ|©öÑ\x000bnL\x0010cmGSn´`¢ôØÿÿL?Ù§»õÀc¦	&ç/¿×üñá¾îêl
É\x0013håC7<ØÑW9ù>¿þ\x001bxM\x0008Faoú \x001eÇ\x001e¼Ïookg\x0001ÛÄ\x001fP\x0015Dæ$V¬\x0010\x0004jE¤¿w~xu´-|.7<w7\x0001ÛÀêû\x0011\x0005ãs\x0007±´eàªçî)à¼}¾,üÃÃÝ·Û»/5Þ8ý:W\x0017JLWäÔ¢ð¿89wõìøüèøû-%¿~¸ÿyu³~x¾`Lò|{_\x0017ÈTèIµ\x0013I7\x000c.ÕÜê-ÛÎkI®N·\x0004%\x0005iïìl%õD;½±º\x0011¢êJ61\x0005¸CÔìäç¡H\x001aÞÀe//U)\x000c\x0007OzL³µ\x0001ô\x0017ï\x001e6f%ß<Ü>íýp{s[Õ¦\x000cV>å\x001fNßaYë¹Rk²­ðÍÙÑåÞ\x000fGGã\x001diàm8Ì{ýAZ³/É¸Ï«Oc¢¼¤F\x001f\x001cÃÇo¡Zó ñ6ÈëdÙË«wÛ*Ë"\x0007$\x0005¨\x0003Mò\x0004
¾ \x0010¨	\x000c:ª\x001fØ\x0006ªKP=\x0007\x0014T²\x0003p!vOö«à\x001f
@M	jfYT¢\x0006T\x0002E\x0001t¶(	ßÃ-o'_Þv\x000e§´(Ò\x0000ÊC ¨£T\x000fÜ¨v\x0002êJP7k/\x0005\x0012\x0010õ\x000eÕ95\x0019ãfgÇ4Ú@}	êÛAe4Æpú\x0000Á
MÅX#j\x001bg(9Ã,*jìò.Ú,jS·Æ2þM Rô¼¨µé%[÷^îÓKÊZ¸ì´çFå,?ÚI\x0008{oÒ\x0004´"M²^íäãËÞn3¶\x0013á¢\x0018dZ¥¡KôÃ¢ Ucnv\x0000Ú[¥rÆ2ÑºÜÕé±®ÄÒn
4ßÆÂmj\x0007ª·HÕE
ÛÞr¹sª\x001cåmOy=\x001bF¥m¤=ÿ¤f9(G©\x001cç\x0004\x001bª%ó¶ûöc\x000fz¤\x001b¥e:ÌÞW³><\x000bÉãÜrlKÆÍ£²S\x0015J\x000e"<%Eq+¹\x0000úÓË}íõÉJKQiÀz¢\ðäµå©\x0007nl48EÐ\x0010A¿»>ÝvêMIlf\x0013kÉm§\x001es|DìIý\x0011"±¾þ\x0019È®DvK\x001d!\x0007A9\x0000Df+±kê\x000cd_"ûÙÈ¥²B4\x0007rëÀ#FüX%ä\x000câP\x0012ùFÖ\x0014
\x0006l4DÌÅÎNÃ\x001cKä8\x001b\x0019Ìd\x001b{®áõXbC\x000fjcjdíÀ¯Lò\x0016bþ²H\x0013¤1\x000f\x0017iY\x0018êðõø\x0016´+æ¾ïâ¼¦\x0017á\x0010\x0003ÍÇ\x00023+
\x0016]\x0018KZÏ@V=d5ßÌ\x001dr\x001be3S\x0019*yläÜ\x000cfÝcÖ³£¡¢»\x0010!&'fÃº±\x000ee¿vÆÜ;Jäü³Äni\x0008\x001a\x0002\x0011$n£tvggÛc¶s½ôÔO\x001d%^³×pý\x001cÜáv·\x0005{ç\x0000BØF]ëp`)\x0016¼\x0007Gåöf0÷\x000e@9û\x0004ô>R\x0016$i²ä·Nß©\x0007é§î\x0016âÞ\x0001(g^®@\x0003|^n´ð\x0018mÒÊ\x0010cS?ÛUï@Q³\x000f\x0014¯X½9
CSP\x001f£¹àÇDDf0÷\x000e\x00145û@	X\x0015G\x00128\x000bï½\x0017TbäE\x001c«ÁÜ;QÔì\x0013Å;CÚ'àÜ:æ®8ÎE¿»[õN\x00145ûD	\x0015q¢×³6¯
5&LZ{'}¢Èâ\x0011QâÀ+6s§æÃî{\x0007} \x0004¬BÏÌ:k¢&3ó 1%ß;cî9g5Û9£XR~¢Ú¹üæQÜÇ*=g\x0010÷³í\x0016ûÂÓð´òÞèÀy¬ao\x0006sïz¢fßO\x0002x<%j¼j[23\x001fÒu\x0018µ3ëÞ¢g\x001f(AwZz*r\x000f'Ød´ÀÎc
\x00003{\x0007{ HÛ¸à\x0012¨©\x00128ÀH¤lTr\x0006oÏÉéÙN.tz¹Ñ¼&<ëR{|AÚ\x0019s/\x0004Õ³CÐ\x0010\x0014]O"ü\x000eç Ç"¯Ü{>CÏ÷\x0019°³c6yHZBVÔã	¡ÓhZ¶\x0019Ùô¶¿ý\x0002W9DpmX%5ò\x0003óîéÅFfvl½Wìõ\x0004ùÐ\x000enT^±¾¶\x0019Ì½ålæ.g{ùr\x0012X¤J\x0007ª)ò6îÀÇ	7È3Ã\x000fÊ<óÓÞÛ/ü÷}¥¾r\x0010tfí=¸öQ\x000fAP*uNíÐÛ/÷Þ~xºMuI¬g\x0013[E\x001dÖ8\x000ck_\x0013q ÃÏi9úºÜLlKb;XhªKÃvM®ÎTÊvc\x0013aÛ]Iìæ\x0012Koyà6¸}:úX¼È\x00191úÓ\x000cìK`?\x001b¸È\x0010\x000cÎÌÄâ\x001d¸	\O\x001cKâ8ßÄ±À¥¤x-\x0016EïXö]Ål_7'I\x00136%)a?\x0004¿=à¸¤¥ÈZ\x000f¼ÖÉ»\x001d}ý¶zzJÏ}Rî>üróõÃãÍ\x001e\çB
;lA½\x000b¤½\x0010û.·J© ¸Òc4§tr~py^ÿð/>ûáðäÍÅaþ'\x000bUþ\x0016j\x0007¿Ò$Ùà=J'd§en}\x0012ÔÛù¯¡Ë_Cïâc8J.Á\x0015ÜQc
^¿¸ìF\x001c~\x000bSþ\x0016f\x0017\x001fÃÐÍ1(þ\x0016¡« ùñ-\ù[¸]ü\x0016<ÌÓ\x00031%ú¢r,fëF=ç¢_#¿FØÁ¯w\x0007E¥\f_D³\Ï3æMü\x0016¯¯wÉK]|
K-Ó©Ä
½R;/øu!/ú=zJîbUIOÃ£½×\x001e5Eóç Ö9É«ößcsá\x001d:[mW¹üÃíÍË¯{ç\x000f÷UµË"bF(ÇððOsJ\x0016}s\x0014¯¥Ù~#½Æbàëÿ³w~v:^¿Üa\x0012Û,Á\x000e<\x0002\x0002ìO;À\x0007Oï|\x001ee\wíJl·\x0000ÛZ\x001cW°¥#m\x0015\x001fYÈëQµYØ¾Äö³±¥\x0010<5oÉÓÑ\x0001ÛÒ½	6ìÉ,ìPb\x0005Ö3¨Mã À~µöÔú,ìXbÇ\x0005Ö\x000bá¢[ª£æ'Ï;r¬\x0017s\x000eô«S·ºW1c\x0004ÖÒÒ¦\x001d\x0019YR\x0002ööt@\x001b·ìqË\x0005ÜÚPftp\x001e9ê54\x0019
\x0007 ì\x0010»ç¶å|¿
DPT´\x001b9ÀÜ4®ÇëÑ	\x0018³¸{~[ÎwÜiq+ZÜ(t¨ius6_ù³¸{[Î÷Ü\x0012¯Tì\x001d\x0015?\x0003Â*q¼+'»|Z¸{[.qÝà\x0003UvÝÎ\x0019n?\x0015Þòò6cC]fq÷\·ï»¥ÅKB£Ó4È\x001e¸¹\x0001Ðã\x0000Õ\x001dr÷|·\â¼ã«;	I`nJð\x001b7¦6\x0007[õ¼·Zâ½=KkEß=²\x0005a9ûlÇ»Xæp÷¼·Zâ½mà¬y@E|âV4ì\x0003ùÈÂ,î~Ô½Ä}».~
N±æ
\x0007&NM(\x0018ÔQëaò\çäùÛ/7_oï1Û~ó\x001b\tÞÜ­î?~©zWø´;ÓÜø\x001cºi°Î\x0015Q½ýþðäè\x0014ÓþçKÎãSøÙ\x0016|3Ì+^^éüæééaï\x0018[ñ\x001f*\x001eQÛ\x0002Sz\x000e'Ã/´\7jÆ*øv~xyy¶ZñÏ¦¹MÉm\x0016qçÔ©Ó\x0012_<óJ!ý3L\x001f\x0004±ó¨]IíP[¾\x0015\x0003¤§ö(ðàWÇÉÂ»\x0004\x000f%xX\x0004´\x0005\x00138jaÅY¼ÉY3Ö-5\x000b¼È«~^¥ÜDÜ©Ä_DJ¨7ôL>:
{\x001eyogÊE[Ó8:Wº=\ÓËcäbè\x0012Eß%>íüöðôð\)SáÅI½©¦ÔI|FRyf\x001e×\x001b±EÞ¹ÃË½¿]]mQ­è°U­\x0016`ãF¤cß\x0015ý{ÊX987GJ\x0013¶ðÃ×[?´öÛÇ\x000f·üçcÝ³1°:\òá\x0016ßFu\x001e\x0003Ç\x00120qìÀ/Èß]_¼9:¼Øö6#\x001dNRößf\x0000þÿvûñÿZU*ØyK/JpÛQ\x0014G/-§;Ý_AöÃó£·\x0007\x0015àª\x0004WËÀ\x0005vòÊPïBômv\;»
|¸7¥\x0018¼õÿñï\x001f\x001fj§§\x0004Ïõ\x0014\x001e~\x0005ºhÂbgh7Ù	\x0000ÈoÏ¶MéUI¬f\x0013\x001bEi¾i¶²0ß&ôô;t-°.õ|\x0013\x0007R
ÿ\x0003\x00120\x000e'à©\x0002z`S\x0002ÙÀ/gÞi¥ 8v;ptpp;±-í\bøE3Ê\x00114U'JÍ²\x0012jB\x0004¥\x0001ØÀn&°\x00128¢V±´Ý¥\x000b\x0003s¢Ä»ØÄ~¶¢VN0±å}']×\x001c?Õ\x0016Y\x000f\x001cJà0ÛÄÊQÌámÀ÷=ëuÚ0i­'~M/\x0016³Á\x0019k²±T|CcW16/²ø¡wz¼úë_ÏW·w_þø¯§½ïW/\x0012£ÎS{w\x001a\x001aÏ:\x001ee\x0003Áô8?8:þ\x001e@¿?¸.îäC<Uâ©?\x001d.ñô\x000eÏxîO\x0017J¼ð§Ã%^ü³áÉþÎýÓl]a·\x0018o1,È°ú\x0000÷®ÇªÃ&\x0015×Óñ\x0018\x00055`Èóµ­óchYáà
Ü¹\x000e/Æ]7ãª\x0012WÍÄÅ¾_òÛQ¬UFv\x00127Sú[Õ¸ºÄÕ3qµí¢%°.eU£°ª³î®pMkæZ'ox\x0003ò\x0008×\x0018^\x000cÁL(TãÚ\x0012×Îµ®¦Q?\x0010(\x0019\x0012\x0014\x0001ëòýDÖ.´ÒºÖÍÝi\x0003QlIÍ-§æc4\x0017ÖëK\?×¸5e\x001c¶q¥ì"ý)MjÜPâùk4º¼ÐÔa\x0001kAuÖP?ª¦%mI\x000bq½#¯«iÄ
Ø%Ú\x001cü\x0012»¡-´º¼èiuµù\x0005À\x0004Ñ²Ç\x001bkö\x000b"vw¨\x001d\x001d\x0012²¦Í=Ô|¤rcÔ>¤rôèX³ËMhi¦í\x0011rî!á\x0002©xß²u\x0003ir´qºW\x000e½®Ì^·È{~ÿÇ?Wæ<e\x0012&)%Q!´s4ú"Öè\x00159Ïï\x000f¯¶æ;Íð±Ðô\x001f\x000b_ö.^nnêÆöXðxBdõ)ÆÕ\x001a-\x000cuMÛ06¬¯÷.®./\x000f·LîéU¬\x0016 \x000b>1\x000e9?\x000bÌU½ÔXUí\x001cf]2ë\x0005Ì<,ÒÃÊÍ98´3W\x00073Vêß\x0002-Ì0o\x0006\x000fÉ­\x0013Ãñý;OÆÐ(I\x001e p\x001e ðÉp*¿W5;\\x000c\x001fé¿´£[M/\x0010\x001a"µ\è\x0006èç:\x0004;vÌD×%º^fu\x0016U×\x0006<µòluR-\x000ffL¨\x0011ÝØáÎ´ko\x0010\x0017/\x001f¿Ü<Vy@-5¶\x001c¤^\x001cîN\x0006nÏÊ-ÆÍ&)\x001f .®á·¸ØöÊ\x0016aX/ñð5Ù»ê2*Q#'»í\x0018ºÜ­aå\x0008°úXf±(8;IÆV%´\x000f­x2\x0015Hà)îq¬Ay\x000e³)Í|fï©&EäÎß]¤
N­õØz\x000es(Ãlfáy\x0000ÖQ\x0017µ¥aZ1É\x0016h5|RSý'5|¢ÿôð´÷æáq\x0005ÿ»*\x001aÑÊa)uêåÃô9ôï\x001cÎªÞÌÅWúwg{oÎ.\x000eàOã«\x0012_-Ä×vßS³§ÍõK@\x001fe×Ö7\x001a­Î¥×%½^H/x40àKìÈJøbm0þ¤VX+¾)ñÍR|O/É\x0001+ò©©R[3Xê´[|[âÛeø
.:y^\x001e!u9p,¡iÄÎ¾/ñýB|÷j}ùFÖ\x0017&vÎS\x001a;­ø¡Ä\x000f\x000bñE\x0012!Løkm°³Ë÷Ôh2r.~,ñãB|[\x0016hí+L«&|\x0017_\x001b§ô\x0012\x001añ\x000b½ÍÁëÝ\x001c~÷$_a\x001bSâ¬Ò;\x001a;ÎÆïZ\x000b-X>$\x0017\x0013,Ä¾Yþ6ÀoÅô£÷¹ø=¿/\x0017:~\x000c\x0012\x0004Àã\x0000\x000f{Î]{\x001eÙóûr¡ã¨éà­+u\x0017Àë]º²ç÷åBÇ/-­o¨<±\x00155j¬{6¿ëñ»æ\x0007£hï.]+\x0005UÍýwí:eïà\x000bO.,ÉÕ¶sýô\x000e%´ïì?ÌÉ¯zË_-[þpq÷¤\x0001\x0010ðÑ'?MzÅ
¯NOÕ?Tãëáè\x001d\x001d%çÀ½ª¬Ü01¢å<É²D8\x000bTð406¥È=\x0003ôÁÖz\x0013=\x001c\x001b£cÿFØ-yÁø`B>l\x0001[Ó\x00049,NNc«áÓ°òýûÕÉÃýó×»ª"h\x0015å6[oE!&ã×VÝ\x0017\x0013ËääìôêäúxK\x0005´\x001a>\x000f+ß¿Sµ!GÏíN^;|\x001eÌîIjÒÃEwR>¼\x001aYÈz.rT¥ñ½Ø\x0010rÜê$ãîMlf#c¯xîròpû¦aArÓè¨v`[\x0002ÛÙÀø<H+Y"\x0001/¨tG<©sWìJd·\x00049WÕaI6ë52Ò°!Õ¤Y5²/ýldËÊ2XÇö\x0002²æ^Ã8­g]M\x001cJâ0ßÈÜ2\x0018Yæ·7 B3ò´0_5r,ãld§:\x000f'l·è¬¼;§\\ØüàÂÖ¸0\x0002MÈ\x000e\x0005ñ\x0007ªx\x0013ô¤6t5sÿì}øE\x001fY\x001aÃEês\x0003fG1\x00120Oió50÷\x000e?9ûôÝS2üÉæ)¥¸6øô3c\x0005g3{{úi8X\Â¹Ú	9jî«v;4sïôó¿\x0010YÇÃÁmi9{j\x000eóøà¹3æÞi"ç\x001e'\x001a%<õÝ+RZ6\x0002Î=f\x001e¯çigî9g9ß;£ú¡!uè×@Ñ5¯K9=¢¹çå\÷ì\x001fÙ¢õ!÷ô&;ûN-egvV=W§æº:Z\x0012Ô´ti²ábËR)rt\x0012c=³¶Ã ]ë_;¿yùvw[ù\x0008RP¤:é<¦2s\x000eDuvvÄs°ç×çÇGÛaíPÏöøÉQÁ\x0012ºçú/ñ*¢
ä.È?\x0008ëú=\x0008ð4­wú\x001c³ÄØ	¬º)ã\x0010$+TïOzµ2²Ég+=:¶û 59fi±\x0013X5åñ!®.qõ|\-9ì\x0008\x0006o,9G©=ÝS\x001eÍ5áÚ\x0012×.À«\x0014½¥AÌLòP\x00014?d½4ÑúÖ/  HpþÚÐ\x001a6\d|ö|Z¡eIÊ
®Ø«§çÇ\x000f/u
Æ\x0012+MòÃSº©£Þ@7¦UÃ/¯.\x000eß\ok0flSbÙØ"f©\x001c¹¼|q¸g^\x000f\x0010NO ¨G\x000e%r}®y\x000e©Ã\x0018ÔÖ¹¢\x000et=b;Ä%v\`é ÈW8l2 I\x0014\x0010+i2öhÑÆ\x001cìâbå\x0017«FsãçÍ
ñFãðAÚÎÜè\x0016nÙã\x000bì-¹¸Ñy%öi¦ izðN=uÏÈùnD`qîÍt8³Z°(>©@µ§#ÿ\x0006nÛã¶\x000b¸­ 9\x000fÎÆnÖ&Ê³enp0;tÅÅ
ï,mÜ(íëÈÞRó(:§HUÎ@ ´Ëuâ{Ü~½µ¤N\x001aFñðø\x0012°wÅ0¬zî\x0013\x000b¼`\x0010T×°i\x001c'Ut¤Þá£z>P-ð6°Ã±ùpGÑ\x0013æ¶nzfh=·êq«\x0005Ü¨WÀÜzl¼±W­\x0018§WÏÝój\x0017tÑQo³r68l\x0002UX'\x0013ramÜ½`J-¦¬N\x0015é\x001b'ùòÀÅÈëDïòÔQ=ï­\x0016xo\x0008Y©ÑÍáRÏ>àÇ\x001da»]FTºwÄë\x0005G¼5ìÕ\x000fË$¹UÅ¤º
n5|óTb0´ \x0000úí\x001eNt¯Ê;	|¡Í½d8É0··hÁ­oÞµA\x0016òÙðW\x001e\x001cå¿r\äj\x00119vje\x0019ðJè®\x000cÖfùf¢ë\x0012]/3º £\x001e.©\x0010\x0016G\x001c²hy¨®ÐnJt³\x0008\x001dåäÈê\x0018 Ñ5/±ºà¶\x0004·ÀuDñìÜadéà*p#b\x0010cb¬3Ñ]îÙÜÒ«9±*waF\x001eÆ1ê\x0014ç¡\x001776%Ó\x0006z$­d0»£¢it0®3ûô<\x001av9l6f(ÓöÝãê§çº®\x0017¬:Ëó\x0011àÎcù\x0019Ï)Ê[*éÆâ¢å»9¼Ú&õ2«fXzÓ\x0002-³Ò:B£±\x0015õê\x0004]¢RrlþS\x000b´\x001966ßÞÝ*U\x000cU5F	´©Î Î¡\x0013æi¨è&ö\x000fR½Ð¶¦¨a7\x0019ø52\x0017L§¦UÍÓ¬!®¥N\x001d\x001cò¶\x0018Y\x000c\x001f\x0011\x001d4¾yÀvÅº²,éÍ~ÌYèà~\x0016JçZÚ£þïµ[ñÍ\x0019¶+]o\x001d\x001cv	;è\x000bm¤x0\x000e;\x001cß$ÁjÓ¬ÓÝa\x0012Û,1¶¥	Ñ.Âo\x0010;cÛq¢Å¨	ÛØ~\x0001¶¬!Ï1U£©QªzÔ±¤\x000b¨âó\x0011sßIË\x0003'Ö² Tc--Ø\x001fä ø~#sð}¾º[=ï½©\x0013t\x0001\x000c&û\x000eû*ëBç¡ÈÏ\x000f\x000f®öÞ*\x001d3\x00032ø,ýÝ{éï®{ë\x0017ô(£'4|Ï¥f¥ÌXDþ¸þ8
§J8Õ\x000e§<Åo\x001a«JéQßX
=ál#N·\x0006Npzå<\x0015	j\x001c?Ï]«<³±ZÃfJ6ÓÎ MÇ&\x001dWÈ\x000enÄñ×ÀÙ\x0012Î¶ÂÁr\x000f4¬Y\x0007\x001cá¬§VL\x0005\x0011ïHò°\x0006Îp®\x001dNZÚª\x001aãîHûÁQ½B
Àùp¡\x000bípVPbJã#ÈsÂS¬'ÍX»\x0002Nö6«lÞ­ZÀù\x0017t¦S¿+vx\x0012\x0018\x001b5RC×Û\x0011²yKh£ ³/qôi.\x0012\x0018­w«¡ó=:ßN\x0007HY1G['s.	èx¤\x0019\x00165¤îjèb.6ÓÉ<üN±xGxvÂ2±Ã-hÂ\x000c{ÿÍ°÷?AÜÀ\x0019ûø¡*@WØfC\x0002cZ³ÜsT`16õû½Fèépà^¼Ùv±\x0008CM0\x0010hf7pßÌs±{F%Äà8\x0005*ÆPÍe7%»Yfwpâ\x0006.F1\x0004\x0012þ2NiSÍe÷%»_fw¸_\x0004Nk,þI\x001aÙÍ´dD\x001b{,Ùã"v\x001d\x001cEG.MËz\x0017\x001eö&çÍÇþ[áÕPóBÁ\x0005ïäáåî¶ª°Æ8ØùU\x0008«ci¢Â­\x001c
[\x0008D§"÷³ëã£Ói`S\x0002À^rÙ¿\x0005gG*.ÊSAº6zlòW=¯\x001dß[Ùïkº[í]=®~¹y|ªZ\x001bI*Ü¤\x0019Ü²v j³\x001a»î;Ø»º8øáðârËÊ°Cñ{+ûÝMÍà\x0010ççø+ëYçEÍ#0SÕ¥MØºÄÖK°ád´,Ã\x001d)E.;©ÆvÔ¾¤ö\x000b¨±=\x0006©âCg\x0002\x0012e7×Ö1õyà±\x0004KÀ£y\x001a\x0000n¨)J¯ÉàÖOëZ4Ëþ¾\²1£U<ÂzOsí¢\x000cüøfÇ\x0005ig÷V¸\²ÄS\x0002lEYD\x001e\x001d»ÝÛ\x001e¹]BîYÄÅ[ËÒ¤]`\x0008?l@l\x0002ïmO¹`*Xxlrc¸\x001e\x0019Åý3¸±£ºMàjø¢ò3ÊùÝêcÒ\x001cñ®ð´×:w(C7øÁFR>ðë°\éhVéüøàmÏ\x001cñæpÿÎñü·D\x0013¤KU¿?Ü®înòL¤*k[¡yÔZ[
õ0Ã­çPy1V¶\x000eVþáèàø0C*,=Ä4%¦3	\x0013Ó\x0006ÌÈ½ù^@ªÆ\x000c%fO\x000f$[\x0015ËS\x0013 6þuRÓÈ®«Å½.g~u%;èH 
8£#`äBsÊÞW3?»
Û\x0013#è¬©%
úp¨\x0001¼Óõ8Ý<N­\x0004ï¢!ÍßÝðè	\x0017Fo%S\x00008\x001cXäÖ¢ä÷«ûÏ1\x001bjyò|(DËYyD\x000c«\x00086ß_\x001c¾ßâ\åP4Uºµ\x0008¹\x0005\x001aö\x0012+®³&S\x0014ßÜ0ã\x001cd]"ë\x0005ÈvÇNoAÌ\Âm]\x0016\x0013©6%´\x000fîv\x0019\x001aÖÉ\x0011½0\x001cÑ±ÉMÌ¶d¶\x000b-ó\x0010/ì
Ï©ñj²x»ÙÌn>³çÓ\x000cëpIå
.ª\x0016´cî\x001ch_BûùÐ\x0010ÿ
R;Q!û8fi1ëãd·M\x0003t(¡Ã|è`8%\x0010´ï,\x001d5KDWÝ­+¡AFÃ\x0006ÖõÑÝñTi\x001e÷\Â%'å\x0000\x001a¨{\x001bqxçh »\x001d®¤âãÄ>
\x0017à)bQN«?M3+=¬\x000bÕùi:Gí	ùduûx[\x001c}'Ó£ü9\x0018>YFµ)dOÐ'\x0007G\x0017G\x0015ÐªVó¡QÕÕÒ\x0011.¸¥0Ún\x0000SÛï\x0019MÐºÖó¡]ès\x00014[\x001aÅ\x000b\x0018zä\x0010\x0003mJh3\x001f\x001a®q<ÞÑ;:\x000faI;>ÄíX\x000e´-¡í\x0002K«}EË#7HfèÈ\x001dFEç@»\x0012Ú-XÓ¢\x0001\x0004F÷4HÅv9ÐÑ79Ð¾öó¡CêºÊÐ:ËáLn>ÉèôÏ9Ð¡\x000e\x000b \x001dÇK8`'Ò 
ÿ:\x0001t9²\x0019Vï\x001bÕ¿³¿Ü|ü²w¼ú±®/Yù(\x0008Z+K*çF¨@ML\x0012\ÊTfÿüúðí÷\x0000ÿÝÙ'	3,Þ7ªoi\x0005wASyÆgü,yrtjò¶ÕÄmJn³;ZV\x0002EÜ4µ4Tt\x0001àcEHmàz¨m§\x0007Ã÷Îoo\x001e\x001fá×¨«\x0001R¨.Bf*fÖèElh,X=?:¼À_âoÓÔª¤Vó©eêö¤Ð<´ÙîI"Í3­Kl½ÀØÒð|&¸ge53°¶¤®p;EmJj³ÀØAñü6ëY_\x001b\x0002\x0011Õ=F5ÍÂ¶%¶­¡\x0017do)µì\x0014\x000f¼µ£]W-Ì\x001f¤´òJ¼\x001cüõ¯'\x000f¿Ý¯>VOHVGê)®¥ÉïÁ±d\x0015ÄzcCÈOÎþvzðvtã0¡,SB¹\x0019ÏðlÛà ëUpxôe<iFò\x001cUx¾Äó3ðpQÖ\x0001\x000e\¿®á\x0002E³Wv$;°
OÈañ\x000cb¨Õó/\x000f÷\x001fkÛs\x0015\x0006ñ	Ò}¸;õ7¸MUår7ÿrvúv[×È°\x0004Cµ	/-È\x0001Ûr22\x0004\x0011Ôº©nzê\x0018ënA\x001eJãÊ(úóåW÷ê\x0004fµÒ<ß*(9ì	ÔÈu\x0001\x0013½pþ¾Û:9\x000eÓq0¬½×XE=PA\x0005ÒÛ0RxÊ¶À½trx-o(yÃL^ó\x0010i~Xð¬mé<'ÃãèhÌZÞ\x000fÒøÁ[\x001dÞ"!zO\x0001ÙÇçº©³pÚÒKåº9\x0005×f$\x001b\x000b\x0011r\x001cöæðâêlÓ">Sò9|ÒÑ³­Æ±lÞ\x0012 ÝàÀ¥©nÖ\x0001º\x0012Ðýy\x0000\x001dv\Y1¨\x0013»Jç|Ýt\x0004*}1w\x0011\x001aá%g\x001c¢iwÎù-OöbpuG`7\x0013Xaá\x000f\x0001+ÇrÒ>(N°Æé¶¥ZàP\x0002¹ÀØ¶cmL³\x0010[5S¢Ý\x0015ÀÃnG»\x001doo^þòîö\x0019íÝ×ûê^\x001a%¦*jïó88\x001dáZL\x001a rtbÖñÑáõÞ»£+X¾Ç¨ç×ï«Y\x000bZ÷_­½¥§\x000f·O7ÏµªxÂCp\x0015Åb:ÂHVÂRÕE5æcNÍÓ³£ËÃ«	A¿a7²V½U=\x0003\x001d¬,\x0011á\x0008£æu|¤GÝ8¦:ÞH>l·\x0012r-¹ûû?þýyuÿ¹2¼
T"\x000b«'yBxk(ÎI¾\x0013ø½Ã«Ó÷ÓÌºdÖó2´+£T§\x0006%ÑñÌì¦\x0007¿L1a\x0005»\x0008©o\x001f^WwuD&¥fºµ£'ÉV#9giÇBàWOòöìúòêàx3ÑÃjS-×öäêñ#Îó¬×\x0003"±ieø×{I¹\x001d\x0004ô&\x0017öÁÅ[è¹mGÊáÅ]\x000e{¾\x001bÁ5×~G\x0014­Ì7w®Ã\x0004>\x0016\x000f·Ëá{Ôë=Ôßÿ\x0006¾ºRò8;\x000f¾ì==øâÝÞïïÀÃÿi[/õ\x0010]ôÐïÀæ4Ï³2Dö8L-\x0017®Ãÿ£VIi\x0014£¡n×öä\x0018lNã<·Ù\\x000c_n.\x0017Ë\x001cpÎ¼Zã\x0003iPKÃ«\x001cû¡¶§yúà°Po¾RÛÚ.¡Öi$G¢ÆçT©­dêQM·yæv%¸[\x00023£ÉÜAá6Mà®~\x001a[ñw\x0001n\x000fÀF\x000fÄ\x0002.n?\x0000v\x000f7ÖEÒ
°*}·3ÔS_\x0016\x000b¸8z\x00132·6îçÕð\x0007Å	\x000f\x0007ÏíW\x0008LþøÏÇÊ&\x0018§è*\x0000xu¨\x001dym=-áà9:IqÉ6_\x0012¾$\x000e}É»_þøÏß+\x0008V\x0004v%<å\x0007,m;W2VtX,w?\x001cþ}Û\x0002±ÃhÊ®)Gýpóø¹n»\x0006¼}SÚÛNh$ö\x0012>L«ºüpxñ~ëäùáäk3|ý´\x0007+åëíç´D*µ\x0002ÀåÄq\x0005lÈìÿ %\x001dº0Ý\x0019x¹\x0007Ëåäèý5®m{rXJmÖ\x0014iÚùÓÝ,,ç>åB$ýr\x0013åXÃt;ÿ°\x0011ÉÈ¡ýÏ\x001fÿø/ø-n>=ÜW¦Ât²9.vm]
#G"\x0003øç\x0017ø;\x001c¾;;Ýaòq´\x0007 ËæÕÃËãÍí]íeS3§+½6ÑPÃµTú2a
	ÕtÍ«³ëÃ£ãíM1\x000cl\x001cNM_}º½¿]}¬\x000e\x001d6<äÁ\x00028\x0008PdyN8üùºæ&5÷ÝÑéÑÁ[:îÓÿL¸ê\x001f¿Þ¼ü\x001a~%K'ç}ûù>¡%U ügàG\x000f_ÿòÇ>ý\x0005úW\x0012Ñ¼Ô`ÆÔMìÀ¢.Ï98[0p\x0005§âÊ·£³¿\x0000\x001aÞÓ\x000fÞ\x0003$üäý)Ðl6a	ì¦P@Ä\x0013\x0013¶çÄÄ$\x0005\x0016¨¢
W\x000cù\x0019liC@Ô\x0003\x0002ç¢¤\x0014yÇ\x0000\x0010ø\x0003PÊÏ% \x0017õ\x0012 Øn¦	\x00087Sl\x0000@*%V©v0}5)\x0017\x0001Á'·m@Zå\x0007\x000c\x0004¹¥Çi8£\x0014\x0001°\x0015¨b\x0019AØàÚð~«<í:0RÀ±)é«©\Ê:×Hp¡ómË(R\x0015"\x0002ù\I\x0004@\x001eug\x0012\x0010ªå,3\x0012D)¡Éem'üZ*ðA&A{
\x001f\x0018	Üql\x0003{Òs$d*ÕtyÂt6Qûo"ì\x0016m>R
åqûÞ¯Ãµ­xû>\x0012K[eÛ\x0003oqjCDgCaKTfò¹zx\x0001\x0013ì6Ù¶ã úÌ\x001eøíb\x0016\x0018FÇ\x001dx\x001bµôëÁêm+<MÈ!;IfJ\x0003ÙNrá·Ó?«I7,(\x0015ó\x0019l:â\x0015-¨`ÉN!ß\x00160áÛvèÊ,¢`ß¥WsØxÖÐ\x0019\x0017ÌvG0\x0006e¿ý®Ì·"89Æ\x000büÝêù9EÛ`Ú\x0019RÞtJHêÔ3xhâÿa\x0004*]Ù\x000f®®6çGzX9>iÅ2(éN<³\x0005Ò´\x000cçP¶"s9¡6Ä\x0012­Âh9Xi¦3¾&ÐQ[3\x0016DÛ¼\x000f[Ìf°@¡°Ã!9ùÖ
`)?dð¯Ø|(· åð¥\x0019-Æ<l\x0001ÐP/ÛLÑélQíx1Y\x000ebÉÒÐ&\x0004óÀÈK-\x0008Edb$nh!ËÑLóæT<\x0019|BËë\x000có:3zz¡Ul\x001cE4Ã¡&'ÏA@Î¥ÉsÙuµ6MïrÆV@Ç¦Ù8^oFP¬*\x0015¦6<>Zñ,f©ón°Ô\x0010BÓ¢³zó%¬\x000eN\x00045ãT0Þà\x0007Mxp÷ 7\x00124ÓiµOËçh;]\x001a\x001e]ÅGt4Hp)\x001dlX5cÓâø:Iþ\x0004¥þépðv­¡÷Yxüå,\x0011\x000f\x001f¿\x0000àÿ¥îíóº<ï­p\x0005\x000c|D_Q\x0012-«\x0012õRRÅTÝtP\x0012Ë¢M6?\¯f\x001b³uôNf%oæA&\x00038Ï\x0001p:b<\x0013Ó­ÖTÛ¿\x0007\x0007ÈL$2ÿ5ëø\x0004jrN-Ë\x000e+\x000b)ÞÆ¨(ù¨(\x001bû}(rúüG@Ä"Ãlñ>Ý|ýúpý\x0004\x001d¥%Zé È
éÙÉYo\x001dz\x0014x«´zQPÂ\x001e:âªóQ¢yõ"Ö2ÈÄ\x00077º0y\x000b\x0015£a>é*×Þ6>JZ4óa£2ôu©GÌ© éèÆZH×ôq)Ñ\x000e§Íab\x000b~ìl>jÚy°tkÖn\x000f\x001ce2ÚáBLÛ\x000e[\x0016)\x000ePÁQB\x0003µ_*÷\x0016:Jk´ï;1U"³Om\x0008*e\x0012àN#ÖÚ½ûR\x001cí|ØuÎETú0m»èùÓBt·É± G»Yñ&= YÑI@\x0019ïÎ\x0014äYÑãF\x000f\x001bSóoóÞóiøiÚzôm§·_Úy}ÓâaÒRv\x0019½ dêÅkñ`:¸Þ3 «Ä\x0003\x0014êu\x0000\x001aú¦a\x0001=UOÂ
ò56*Ò\x000e\x001a\x0005äüH»Óu>Õñ\x0001`\x000cIÉÂå<`T¾ö\x000eÐÆ\x0007ÛDö\x000f­ÅÓÓ\x000f
¼^zv\x001bµ7&¾ÌiçÃä\x0012\x0007-2àÊyÃ\x000bhÃ&\x0014/÷DUã\x0016Tñ·/J^>¹Å\x0001É§ý§(1`Á$Ù{T\x001d'>³IT\x0015AªËÂà|#A\x0007XÑð4\x000cJEö\x001f\x001c\x0010ü¨®ÐeÙJ\x0007\x0004\x000bòe\x0002tÁ2 Þ\x0004.\x001d=:\x0015\x0010! çÀ\x0014n¼¼\x0005EØÂ`Yõ\x00185å9BHo¡Êè\x0018p\x0005Ä¯ »¾°1\x0001U¼Ï«L]BNimt¨½C´\x0001Â×Õ]_xz\x0008	\x0010G,¤/¬¢e\x001b\x001d712SÒ]_Ø@x\x001fm\x0002\x0004'âÒ
ª ÉÊLC×z\x0001/ìWóïÉ\x0005Öó|¾
zöÂÙi<cÊÀK|fbÀo'^ÊZ\x000f«x^¼:>{:Ç7Ãâ\r\x0013\x0013&\x0007À'/ÊE\x0000k\x001aH2éÊm|\x0006VK\x0016ÌØ8Ü¶dQd°HëE!\x001fpÕ\x0018{±îÄ·/RÍ°9ÿx{ópy
°÷\x0019\x00056µM;ï§9Eæ=Ô\x0010M§½Ùó\x001f~xuR¯».ðÒU²\x001dÏhò\x0015\x001eÃI{\x0008A2óOÓF>É¤ê\x0001\x000cÒ{\x001ekÙ§FS\x0000\x000c1\x0012 ª<o¶\x0002Ò£\x001d04\x0007\x001b\x0000ñ°ú\x0004\x0018½'@ó´/kå£\x000bG3Æ²î@\x000b¨\x0011\x0015ùr\x0017ðéÓÑÊG\x000f×\x001dëçSÙ9ð¥b/{§Õ&\x0007DÚÿüxy71âïØ"	\x001a¹I+o\x001a¶û)+6f\x0015åÇ?ýç¹¿8?xy\x0003&|¥ñWv¨\x001fb\x001aUi\x0004zâó¡.@%«Ó³çÇO;\x0019\x0013=¶0\x0019\x001dSñ/VºYÌB"¡\x0018Þ;W@W3\x0003kZ'\x0012hÄ§¨p¨É@¨DËT{ÖÎL+>\x001fù®\x0016,ì§\x0011A&
{ðgF¦`\x001d¼n%RZ½Tô\x0006ÚÂäÀf¤27ì\x001bJÊ*\x000eîeäQ½3~ðûÑóg\x0013\x0014ÎiÕi¥N*À8Î<xZ)c\x00077:½|6mt£Rí5ntêÅq£[Ë;Ýï*zôlâr\x0006ÇL§/(x±R«Cúj\x0006.. jÛîp
mÚïRO&uÚïHï­<®7/jÛ^*b¿õ´½L¤´\x0017ÊO\x0011Õ¥/©\x0013R\x000fjû ÖñîÎQ¡'\x00185Í\x001bMW²JË»ÿúúÛýo\x000fs×syñp\x0015Ù¨Øusuµ2\x0000×\x001eÍ¤+©MÝ¿ÎY¯¤1VN'×c£f×éÉI\x0011÷ª\x0019,ù¤^XT\x0011X5ìÁa*)c~:æxõ©<û\x000c\x001cU/¨\x0014O¤VÕ\x0004Å¤\x0015çÐ\x000eJ®«\x001bTÓÕ)GÏ\x0002.{±h®ÁvPòg\x0003 é;\x0005\x000e%%ÇÒï¶r\x001fë\x0000%\x001f×	
1ÓXr\x0000Õ\x000bj¬§Ò\x0001\x0000­d(:HÉñõÊ@¦É¡pMÇÉFrÌÑÔ^#;HÓ_7)ðd¤p©Î9,n$R_±¡O>ú¡×îEÅ>búüR¦ÆmæEõWÊ\x001eV~
ìU\x001a'ã%XOwLp\x0004T[\x001bÁ^­ß«{a9ìè¶\x0000.\x0007Åíêð\x0017Z\x0000rô°]ãz[µ\x0017ò\x001eýV@¦y¡h®\x000cÕ!\x0015pìª[ïV÷ÂR\x000e¤ß\x0010hìe`Ûêhe£ê°­{Y¹Ö®{ËJJÛL» oYÅU
·,UÐwÃZê¥Åóeè\x0005ÙnU\x001aXº`a÷Ë\x0011wàT\x0012\x0004CX-å²#¸;®w\x0007{aé»Û\x0018½¬ãÔ±³N°­Ö÷ÀÒwÿ
Tì\x0014\x0016Ñ9Ê~»ÍÕ¢Ý¾\x0014<ðÑ$ôµ>Ç/ÛùÚ\ÙÍêòM¯Ïë© |Ý\x0010\x0016ª\x001a°\X^¥È%øp¨ÓõXµ`µßÎÌò+t?¬ÅçÉ	6z6\x0006XED°¶¾ï¥\x0007ß~c`Ô\x001e~zÅ>Á¢¾>Ý¶*¥9=°8gK1ÛN\x001cê\x0018Rÿñü¹åÂâî×#÷mEjO¸°2\x0017¸ç×V¸Ænw¾ðî®GîÜp3H/NÓv±f\x001dØÎÙâ?J\x000f\x0018\x0003\x0000K
!\x000ee¤£Î\x0001%Ù#\x000cG17×_?Ý?jÛz}þçÅýÊî\x0001\x0008XR±\x0007+Ê\x0019±}òj^Ú«ñ»×Gÿ<~_/1±í\x001aØ¢T-JöQ°[)KêM-©ÖÄ¶ëBj`\x000bÑPï;°ÑüÉÌÓ\x001b·µOÛÄ¶ëCjb\x0013ô¨m&E\x001aMlÂñºÕ²ËMltÙoü¦àq­1Ú\x0007¾1y\x0019)Q\x001a\x0016Z¤ö }ùíF}\x0012³£pöpqðòâæö'ì»8¿?¿¼ºZÍbäÔ\x0016b Å*\x0011G:\x0014\x0001¼C¥FðÃñÁËãÓ³ØqôþèÕÉI=ñ<ã¥\x001en^ëø=Ï	I¥\x001f.©QO¼ªÒÇÒËK=\x000fý¼êíù\x000eB\x001b\x0014nÕÄi//õ@ôózz´ArJÂ¡6}Â­\x0016ÄuâRWDÿöõi¨2ðzGár\x0012@k·Ý¼Ô&ÑMë=Ýñ`uURY\x0003Ú ø°ÊÓD//5Ntó\x0006A×<Ø¼ê.û!o\x0006YS«èÄ¥>þåµôs!(\x0004qêÙÁ4mWú*úW\x0005J\x000c\x000e`çôD\x0008lÊjÏÈ¼¹Ó¢\x001b8\x0006*FÅú6¾z\x0016x\x0008ÂV\x0002¨^`ÖÅè\x0005Æª|z{v8ê¢ªI'59·Z\x0003K'0åXû£T±ÎS1(¾U§\x0013çk	á^^nnéæ!M9\x0004^å©üwj6%^W«Oî\x0004æfn`¸R¥Ä°AáEJ\x000c{E²I>ªJÿu/0«¨ôÛ4I\x000fEÆ`¬«ÉÁq1@T¾R\x001eÜ	Ì\x0012+ÝÀÆR±pæ¬-3Ä>ZÍ'0%\x0007"©Øi\x0002ÆAÏ´Â\bïãÆFÛ¡F"´Ôu\x0004g.æ\x0014¼õl#\¥²\x0017û£ºÓ£ñ\x0004¬-É\x0002aJC3p%YÜ	\x001b¦úM\x000eÓdv\x001b.\x0017èE[ëÜë\x0004æ\x0006ª\x0015Î[Ø\x001dr××V¤Uzq¹¡ªßkl"À\x0008+6ÂÃÊJ>áIÞ'f°Ü]ÕÃiª%z\x000ccöÝêÖ4XzWò\x00031\x0004M?À F6 Ã.ÁÛ­.·õûãfhÃêb=\x000co\x0005ÃÞBn|Ôà[©\x0011÷\x0016Á[DGAûÄ>\x0001sW/ÄÀzÃÍËmý{ÁRÕÖdÉ(»ãQl\x001aZhW,/7ºõGìZ.!\x0000v\\x0014å­çÓ\x0016k=½w"*Æ\x0017S!äIóÔK=Ýå8®Ôù*ç6
zIØf\x001amçìçÌ.>=æüÉ\x0006÷oòÓ¿Ý£d%Ê\x0004\x001fß¼Z×&§\x001d\x0017¡òf£©(\x0016\x0006ÂÖÓ\x0014ÅÏ\x001c×3ª3È]²\x0015ÒcKòIFâÉãrN:mv!»ÓÈ¸ËJ¶3zÒD¯â§3!ùû¬C#å.\x0017ÙC)©\x0019\x0001<eJ®°¯\x0014\x001bu@î2í\x0014\x001e\x000c\x001cJ\x0015äØ@Æ
ÂÄz$ÞH¹Ë<6Sâ+b2M`î8kc\x001cïJ\x0013+}a\x001d»|c;¥àNÔ*t¾\x001d?äG;ä.ËØn"ÙKÒrt10Æ1¤Ùn)wÉÅæ¥T\x001eEs\x0015R|ß2\x000bô-6?oC9O)6cb
ú\x0008`òé|ï¦\x0001s[PÎòí]¤S\x001dôT!\x0004÷ú¸P\x000fÿ\x001b1gÙÃvLMJ\x001aFxÇßÜb/aÚêa\x0007æ,iØ¾5\x0003?×
§PC5}sÖä¶fáµ±\x0011s*lÇtür+Pà@ò	b»¾ð\x0008ÖH9Ë\x000f¶SîÜ6\CnBvr3O>Ï
¶c
ìqLþåü\x00013{É!Æ_>«\x0007{9\x000b.ß¦\x0013ûÕ­P>*ÕX®I\x0018·Kçµ\x000cªrQ~\x0003&¼¹Í`R\x0010¹\x001e\x0006eª'\x00160Ï\x0014îÁ¡Ömé]¥Òg\x0015K
\x0016\x001bX¸1.x35ï%\x0018\x001d\x0008ÆT^!ÞÖ'o\x0014<),là	ð\x0004\x001eEêÀ¼.òTü×ò¤\x0008p=\x000fN¹¡õ±òpBº\x0000NMlq-N
õÖã`\x001d\x001b-\x000fæªTâ1ÁòÞ©¸ûµ<)¨[Ï#5
\x0008Øà G9^\x001f_)eZË"£Õ<\x001eÛ¾éãh\x001fâÁÌ`:ç¢"\x0016²£\x0005\x0012¤3\x0010p¸`^ T*@CÇÃ\x0006C¨Ò\x0014]à\ºg0	pdåiG=ü\x0014ÝÜ.¿¼¼yøc
Bþ$;¨c¤I¢xõÓ|a©Tø¼|uúá<m\x000cg4É07ÐèÈÓh¢á&\x001d8\x0º"²µ\x000e'Ùæ\x0006\x001c+°r\x0011qgÁ%\x0013\x001c'È´«L£XLsËê\x0004¼«¥Õ±i`-®N¾¶éÊfN8+vO²>-DI'z`6ülcl¥\x001ah5Kº9¶ìdH\x0003wHßJRç\x001cldýôÝa-\x0010â
DFSÌ\x0008Û§ôÀ÷ò·O%\x001e[Fú"¿\Ý^\x001a\x001d¯Ïoï/®ÖP\x0019ú»iâ0\\x000fBÓÄ\x0017WÛEX3|töþød
YVêh"ÓT¡Eî\x001a\x00002j{ÆÔtµ\x0017\x000fÙý¿¿êÏW3\x000bùîòæ§£1,ªyj4<Ü\x0008Åï¹É½RxñîÕéËãÚ\x0019Rú-HNù\x0014Âºi¨I"
[î¯!L´bR Ö\x0002ýõÔµ\x001e\x0004Ï[´HNU:\x001aR°Ö\x0013¸ªß>!7RúØGõé«ùE~z$s{~ýÓªÇ\x0000\x001c>\x0013T§Ì \x000e<B,óø°\x0010Ø²ºüËÙÑõ\x0007\x0019ØN¦\x0001\x000cû	ð\x0016·¬¤\x0014Æ2¹ºÈj²8M\x0003æ~s¯Q)­\x0008×\x000c+QÉv
5
d¨fD¢ >ÁÖl\x001a¨8ùZ¯C\x000bÙN\x000e¦LÂ\x001dÅå¯þíôlÊ_³Ò4Ö@ÛÈ\x001bÑ¦ôDB\x00138O3¡ÅV	õÐ¸µ¹\x0011ÍàEa:Q\x0015 åÓijB!-hÜÉÜ¸ÕX\x0002Ô+¬o&4oøxêZË}\x000bÚLH§\x0005Õ£\x0000Çç\x0000\x001a/^\x0010ÿZ&3p3¹\x000b3çýüêüëÍÃ«¸$ÊË¥^DøçXJêÈ#å\x0002¦s\x0004{~rôúôÃ?+\x00033¨ä\x0000 \x001cÜµR\x0011\x0015ÑñË\x0010¹\x0013\x0004óôËP+\x0016+Å`m¥4\x0005VhÏ*ô¥2û{\x000b\x0017ij¶}DI×fàÒÔÞ\x0000ôx*jÃ\ÉÂ6q\x0005&.Ã¥\x0008\x0006Lçõªèu4pqÎ£
\x000c+C±°j}pr1ÈZëN\x000b\x0018«{¶í0N÷[¡\x001c®Qç\x0015òß=`öw¥e¡§xqwðþöâë$øxq»..5.W:\x0012.$4\x0008\x000f'ù$@[Sæ;~wðþìøõ$û8Mu~zäÖr7x®R\x001f4\x000b\x0004¶XãréA/XUÓü\x000esÅzîÚ,ÛI\x0015j.\x0013)\ÑSJPÃ
Êu_\x0018Õ´T?.nÅ£/ÿææÏËµ`T¸­\x001aL\x001d·\x000f\x0006\x001eÌ\x001aÔB÷àÓ¾ªî\x0019Úîs· \x0019ìVMë\x0007q§\x0012Ã XþÁÙXkOÃ­XºÝ¤Á&>\x0008&é*\x0003×©ÈZ\x0010½Ñ­ÝÚÊ3ãþÅûÅßÝËâ»\x001e<¿yø|q{¿.$A\x0019Éõ\x0003ÀÙ9)#Õ¯àª2:Ç\x0007ÏO?¼8>{¿\x0017¿j\x000bÆ4\x0002M¸BeÄ$ðf­§Ú\x0006°Ò4ð\x000c¬Þ±e½ï¦EC	*Z3ãòè(\r²\x0016a®_³¬õÝÄÍ³	L¢:t\x0002Z\x0010µùB
`Ü²Ý\x0004æEäÉ\x00152F\x001ah\x0005Ì`U-×õ`Ü¯Ý\x0006\x0006AS2j\x0016õMÒÈ
\x0003AùSV¦\x00060\x001e\x001bÙ\x0006]÷ö\x0018Ï:²
\x0000\x0006«Ú\
Æ]äM`\x0011è\b½^ºÃ\x0018	\x000cA×n~ëÁxe\x001b\x0018Î%K+æ]¾-\x001b®yÂí7\x0018OÝ/¿û?ª\x0017}\x000bÖÿöâào\x0017ç×\x0007g\x0017_¿­+=ð+¡´å,\x0008®#\x000bR/t§½\x0005'pv|ð·ã£7\x0007àñÿQ5n3Ü]åh\x001f.Ü\x0005©\x0017\x001f#¾HE<>ÿ\x001eÜ]\x0011i\x0017.ª-zW×Pÿêlq·ÅÝUöá\x001a~v5Úx\x001a+2P¤\x0014\x0011kÃ:qwu¥¸d\x0017
¦s[\x001a÷ø°P\x0002ÛÃ»«0íä4\x0008µ¹®Ø\x0019ï3o½¯wWkÚÇë5M\x0018É5ê«\x000c,\x001c²T××»«:íÃ\x001ae4¶ÒòJzËðAÖ\x0006´wòîêOûlQlzMä*\x0010¼nqWeEÇ¬\x0013w^Úé*Ô®ÍKÒ´>pgl{#Ä(\x0002ÏjRû±!"Rç¥Çe\x0014êàÖ\x001e¹PñÙ\x0003<«Níôn¬,bË´ÝE¬É­÷òÎÊTûNæ
S®H.Êñ%Ò°ÐÎÑ\x0003<+Xí4\x0011\x0002\x0005P&`Ë¥!(ÊH\x001e#ÄÎë\x001eàYíj\x001f0¶ðÎ\x0004M#^»­	\x0017±vº8Ç­3\x0006'Û±ø)wÓ\x0005¿1ð¬µ½\x0013X2°vEÛ'~r\x001a\x000bý
=À³Þö>`¸ÞÓÃ\x0008\x0002ó\x0016¶Ü`\x0001Àõ6¯\x001eàYo{ç
+Ôdà3G\x0005í°Â&¹z\x0007]\x0007ð¼·½;LË+,P×­\x000cÓ\\x0010Àè\x0001õ¶÷¹
ËÕÈ:º¬n5å¾ý$¸\x001axÏsÞÚÞG+5\x0015O-¡:\x0007¼cZY8½ö§_>þñËóÂå«óO\x0017\x0007\x001f\x000e9ÿúëÁç\x001fn.o×½Æ\x0010yÿF\x0014\x0011 ¬!1 kò"oO\x001f\x001f¼øpðüÇ£×o\x000f^\x001c\x001füpúê¬þ\x00122£¦zâ\x0011j+ènd!°&aLÕøý4V\x0014\x0004\x0006¨©êø¯EkÿbØ\x0014»
aÃ\x001d?Á\x0006G\x001aFf§fÇ­+¯­ØîÁê?géª£««Ô&sryu¾®I\x0006¬\x0005¿¨L£!Y\x0016Xê2!âxöèää8uÊ¼:9ª?ªÌ(Sª\x0012\x0007ªPÿ£´\x001cÃO\x0012ÉºÊÆ\x000eÊê¢´\x001fÎp0<éÀì0jy©\x000eÈê\x000c\x0004½{!¹XYUõ\x000eÊä&º(!L\x0019¹¡}a&ÊÊ­¸2åú(#¥È!D\x0010¬±)d.Ñ¯5\x0008uP&çÕG	±mj\x0013º\x001a`)¹[Ï
R\x0007dÊ5õmKëù¤#'dîÂ®Ì¥éL\x000eµo%\x0005O%^pâyº/QHøtDØ\x000eÉi¥.J¯r¯«È\x0003SD§hB%áÜIn¾o19¤#V\x0016!\x001217)T*E;0)ÔëzH3
ktèmDh\x0012÷ôµÖ\x000eJÊÃô}sÉú\x0002ÖÕë14{Î[UÑéÀ¤lF\x0017f4%)©kÐÖ´[rÍf.S\x0002}eÍ\x0004
Ó9gùNì½ß¯Õ}ßÜ4R*°\x0012Æf\x001dJãC\x0007&]O{Í\x0011©¸ËäÕÉ\x001cñ\x001cNY)rë0çÃ%û`
=ÎLêóté\x0017eÁt¨¨f÷ø¡\x0004\x001b\x0007`%Ú£¤½ Y¢\x0013\x001b&ø4ù§³l\x001d°ò??â\x001dãc/hZR;ò*)WO¦$
ÀO\x0008ø©óÀk%41jË"O\x0002+\x0012£^i¤¼·¿|û}^Wpópw·~ð¶sg_Á²Õô.ÐVÄQõO¦vN?¼{·<w{F5\x0004mhÚG¼m=ÜÑÃäw¼<âH¨lZ\x0013\x001b=¹6.\x0014<r\x0005"rÎ½#\x0005¸§×ªkØòóT\x001b\x001cv\x001e¦aê6NïSÈæ\x0003\x000f\x0005R¡2Á¨\x001fJÚØòÔ\x0007íÈC°<ËÐWº"ÛàøU¤\x0011\x000e\x001c2UÿDkèfè£'w\x0012\x0015ª¥\x000cÃ\x0019ðÉøÿÚà,X\x000c*ær\x0002ëòt*õ\x0014ÓFí+óÿÚC6Æ­§\x0015R
¨Bn0nÔî\x001aEmzÚ\x000co¯c;Ü¸tÒLE©©±\x0014«.qåT ñ\x001aQZ\x0015Ç\x001e´Ûo÷@1/\x0001å9C'ðo¿¹^\x0003\x0007@S\x001d¨Ç\x000eÉDC\x000f²QÊÎílÄÐË7§oêVý"¯õc
À·@±ÊYl+"a[¼í§K²,\x001c\x0014½[7úpð\x0016þb
ÝLW¯Î	.q°:p2\x0007+\x0005ÎÕl\x001bÝLª®\x000eB').ßCÁp=\x0003¾\x000bo@7Skú²¼±&ðX\x0014å\x0004ÃUòml¨7¤zàPýämàhY\x0019Ãµ+aI<o\x000fÞy¼÷¿ÙYÔôÃÅí-þËWf\x0017,)b*­Ô!g9iB ¾R\x0006ôÃñÙ\x0019þi
V:«mXÒR\x000b°\x001c
Û\x0004\x001aAÀ?=mæZ¸kâòÇB+mäçÃ@wI§kã	2×Æw\x0006LG#\x0014LÁF&P1¹«6ºµ,VÊQ7rqÃ"¾Sæ¹8V+qé¼F\x000bW2fM\*DªÃQZ(î¤\x0000?Å«¦CÒÀÅÉ¶\x0005SØP¯%\x001a\x001c\x0018§\x0003Ê½`öîýûÛÜH__^%,h\x0013U\x0000ÇNÝw
\x0007º%ý!\x0008$+{þèÍÉÑÊ\x0011}h"R)Î\x0008Æ;\x0012\x001cSÆ²à\x0015{V,SºJ5A	\x0013ò:$­´MÃ£JWÞa\x001b¨süêæúß?_~Ô@wtûqm\x000f\x0018N¤M7;ªV© Ó+¡i³\x001bÔ¯õ\x001d=«vÍÀvís
`ZÅC2ñpkOJ^qÝ¦Ó¡¦°k×6×²`A\x001d5@°\x0004ÕCÃ_/´Ì\x0011ÖO¹\x001b@Ù´b\x001a
Tô\x001d\x001dÝHà;Ê½ëµ\x0002[`ÚÀt¤W\x0013{ÓC\x0014XYªiÅþÊ¤-Y4ÂÁM.\x0010À6µÄ¦%ï³ã
¶»ßïýÍ·âl\x001e<¬¿1!ZÎ¸(ë)Ç\x0007\x00014U:\x0004§*é ã\x000f\x0015á¢\x0019Pn~\
9ÛÔ`\x0005A\x0017þq\x0002bQç\x0013ªäïEÐÚ ¬ÇïýÅõùõýÁ³»»uW_\x0015S±^*g1$=m­ä60]Í>¦\x0018\x001fïÀïß\x001c½yðìøÝ»[ð»¸\x0005÷r[à0Q	º9\x00017Õ\x001bÂv¬%±\x0006¸ûq'wÐà½\x00127>=R]\x001c7Pj\x0013\x0017¯T]ØÅÅ¹\x0013\x001bgõFR\x0016\x0011$¶k\x0001Ü±²È$}\x000b÷åÃ¿¾þ[>.Sòýç¿_^g¥4vªR
¸´ÌRéYJU*\x000eX øäèïGo^,\x0018«\x0019è¬<¹\x001dÔ
\x001e< $Wn\x0015«ª»J?~\x000fç¬*¹\x0013`Ò \x000ce©Á\x001c·@V_\x00188Û\x0008:¯Fî\x0000õ,\x0013¨ÍF\x000bj¹\x0012\x0019þ´\x001dè¬
¹\x001dÔ\x0019n\x0004\x0011¨YOAü\x0008½gðH\x000bå¬ú¸ÒxJ*ëIeÚ¡2a¡r¾s6S«Óì8§\x0007µÔ\x0018æ¸X+T&v÷ÎfiµÂm9HèhrGX\x001e\x000bQé\x0018çÏçêæóü=ò\x0007\x00008xyq½rÀ¸ÂiìÎ$%A\x0008bRB\x0017Ã\x0018\¬
´ÿ\x0001þtðòøÍÒñ\x0019\x001d%²\x001aé¤0é\x0012íàrCíáÆ°øi´ªr¡X\x0003w¯ýþy\x001eòkÂ\x000f·\x0017ßî/Öu°ãÄø\x0014!;ÃÕ¬K7ÄJ@_\x0013~8;þÇûãJ\x0013û"Ò.B¸!&c®à?GE\x001b&ã\x000f\Ñäú\x000erÅJnB\x0017§â6IóV'	i\x001bi°5VÃTbè\x000eNºªuqBL$(5û!­'G\x001bNÔ`:8óµ­\x0007Tãd.E9DV3÷&p©(t²"a\x001f¨§¶o¸sÅxO²
¢&4Ù\x0001Êú] ÖQWÔÒà>ëC%[Ü\x0003J\x0011q\x0017¨Q\s-£È2iëF­­åC{@)"î\x0003ÕÜA?ÍÒ vËinë÷=Ç6pRDÜÇi"5°È\x0000·QRáö9+SR:09ëÃô.Û&\x0008RÂ³mÒ²æÕ Bün~ºyÍÞ\_\x001c\x001cÝÞ_Þ__atðîüáîn±Æ/r\x0001s¿ôî(5×z	ÿyúæøàèìý«wGoN0\:xwôáÝ»\x0005qã\x0019{ò§Mö\x0014Jý5ÙSîö/ÄþKü,¯?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=xqüÝÑÙëû!e
)' u(ù¨HMåÉÑ5ókf)uM©'(,b\x000c8Ñ(\x0003ÇÃ®\x001dÁ;ikL;é5
eLÃ÷jçÊlFiÌbº\x001aÓ
c¢jQÖW\x0010bL¥©Kq%iãäYL_cúý£X,]X]fµÛ¢À\x0001\x000fbÍPc	kbu2µÇHËªXt¥Q©ÞÁ¸ã%-\x0003V÷HôCbÜ8´V¥\x0002\x000ei¼gí(ë¸aÒÐºË	\x0019p¦\x0017U§*ÁIP>-
XÏÙxLp\x0001S³ä£wüve\x001fdûTMäT\x0013\x000bSx*È7	îÇ\x000f%¥lÝ³qí0áÛã5sW1:&yPt­o
f1\x001b×\x000e\x0013¾=à(\x000b6'·í© ùEÕ:ù\x0000G\x00104N\x0013Æ½&²àâø\x001fB\x001cÓ\x0014\x0015(+\x001fÂ×\x0019·im®Æ±ø>»ù¢\x0015ÿ\x000bl(\x001bâóãÎÓci¯Ì6XÚí\x001a\x000c3+\x001f\x001e`·ËÆ{ÊqïéQjÅ=Õ¦\x001a\x0019µV²=è8îålãÍqïé\x0005Þø)ø°rSß]Ôvä\x0003\x0004²qrÆy\x0006Ub$ìÜÌÖÔüBbüCøxÙ8O9î<ã.2yV+ \x0005¹5*	²ÓW³]6ÞS{O°Õ\x001aÓWÒ¢Ló°mYÿ,gã=å÷\x000cSS¨æèË.Ò,pm\x001e`qªÆwª	ß	Þ²OòyÒSòI»JÛçØILÝ¸N=å:}\x000e\x0000¤Pe@Ää<öþ\x0001®ÀºqzÂuþ{ÌÙxN=á9ÿMæl\§pÿ\x001es¶)	×â Ö9\x0015÷DEs*6§y\x0003S7.IO¸$\x000c@H/Ó\x0019ÃÝ1\x0000asjù\x0000¦Ùíf2Pòù³»x\x0014YK|}Ó2<ÀuÝ4ßÝÌ|÷àr.)\x0007tý\x0000Çãzb@÷\x0000\x0001²iL3qd"'äín­§lää÷ieÕ\x0003lwÓ¬O3³>ùU"rêÒ¦\x000b·»Òð\x0000G»mÜ§qÖe1¨È)\x000c&Ý\x0013§\x0006¶gûÊ9ÅiXì#1{å´,Ë\x001cÄ\x001dÏI©\x0007ØIR4ùzg8fRq\x0003ÓÓqÕú\x0001\x0016*ø%n¼\x001dOáæQP	7.]\x001a\x000c\x0011,+X³Òºbùz ðõà,¿i<ùé·ÿý|q~»;Ñ C(SÃ±RúWdÎØôÉå7'8|}tøæ~,YcÉ\x0001,sg¨^Û\x0003Aæ³Ðv¸\x000fB©\x001aJ
ÙJQRÎ\x001e\x0006Q¦$\x0007½K×\zË£ÔKÂÂªbª\x001d\x000f<ÉQ4\x0011Ð(©©Ì\x0008U.Àb,Ás*\kV¨¹Â\x0008\x0017vûÓäK<ÝÈP
=nX»â#Öésõ»¹æº\x0018är<\x0018\x001dxª°lzxFÁ­\x0008#{Q£ø
¥\x0000Ã\x0019ý2+=µâG`Ív¡ýè<kï¥\x0019³Ôvâm\x001dºÆyA³\x001fahCÀÃ"µ\x0014¸C9Äz«=ó\x0005ù\x0003.Ì³º/ÎÖìï¡L©Õ¯Õâ\x0018Â\x001dq¥\x0002Ï®oöÏOR¨\x0011×XR*il\x0011O>Q­`ê#$ðìôìÛ}ÅèÄ%k.9Âå\x0002ÏÅñTä\x0007ÖðÔà¶\x0000q\x0018LÕ`j\x0000\x000cåzö\x0016d­PænÙ#Tº¦Ò_Ïg´5ý
¸\x000c,=ê\x0010U!ø§oÏüñúvç@<}¤å´(Ø\x0011¡¬0'¶Æ³¯\x000e¾=|öìôÍ«ûñd'\x0007ñ°)ÓR+áfíÖw¨\x0001:UÓ©A:(£8ç¢káU9Ë·^\x0006\x0007ètM§Çè¤\x001cád;\x0019ÂfÐæjÛÎ\x000cÒ¹Íü^ïØµ2¤^È­¹ü\x0001:[ÓÙA:#¹¢\x0014\x0005Ä\Þ±I©$7µ»ÂÕtnÔvI\x000f0wä:zN¶+x~û%t\x0000Ï×x~tá	\x0014LÎÝ®\x0001·¼òÊ|·µë.ÔpaôË\x0002ÕÑ),±&"¸%èíÃ¢úéª\x0018\x001cÝ±\x0018Ä¶îÑ\x0014d;Wø`{!Ã\x0000_{\\x000c\x0017RúÒ\x0000\x0019\x0013ñ|	àÙW\x001aÀk\x000b\x0018</$HndOZ\x00196Í{AmÍÇ\x000fð5\x0007\x0006\x000c\x0018\x0012õøCi´\x0016ìCi\x0005\x0017+7\x00074G\x0006\x0019B4å©ð#ÞåKwÝþÄ:À×\x001c\x001a0zj¨ÀÃ\x0012ãªC\x0017íW¤\x0012¶×Q\x000cà5§\x0006\x000c\x001e\x001b\x0010DÓÙJæ+Ús^«µækÎ
\x0018=8T\x001aQøJÓP4$ã¹{6ÇÚ=BkÎ\x000c\x0018<4p\x0018\x0000÷å`e)í\x000c¹
+wl\x001c³\x001ctÌIz%Íâ2@©«\x000fÛ\x0013©\x0003x_~\x0019pz7UB¡ÎiÂóåÌÅ\x000bÛJ¼6\x001fôË`\x0002W¯ÇX47ÁÄ¨H\n/\x001c\x001d k¼²\x001côÊ°Qk\x0013\x000eðá$á\x0015µ@\+ù\x001a¯,\x0007½2\x0018U´v*|Aºu»òTW^\x0019âMÔ\x0016\x0005\x000e&È{×;¶
fíêkÜ\x001ct{ 4÷9au(¹½x\x0005.\x0013Üþ
:À×¤r0&\x0005¬\x0000¦âïx\x0000STà-÷ÖÙµAj|\x001aõ-Òä,T~ó2d>ÃÇ\x0006\x001e,+ùÚ[øhP\x0015ý±æ±\x0012;(SLÏâ5i\x0018Û:¼fw¨ÑÝ¡,W¤c²7Ç¦4y]H\x0000¦Í¨köà°\x0016(¤*sÁ­Ñ÷8çÝ}Y	PªÖù©ÑÔ\x0007Îc\x0018C«O2\x0003\x000b0V\x0019PÉ&pQr4rAµ\x001f\x001e'à¨?þSýÊÓM-·ÇèþP¦¤©ð=îÞq\x0016Mm/ªé\x0005l\x001e\x00050\x0013Ô\x0016\x0002t]Ûl\x001161<\x0000.^Û<ß^V13ïÏÛ4éùXª\x000fU\x0013(\x0013\x0019\x001cM^QàhxÀºÑ\x0017£ï?_Ü,.GøwÆ. P"¸mryBÜÌEE®¼ÿF÷Ò&Çij\x0013:ôÅé\x0008¾(q\x001e!:U^\x0011`¥zÍòÇÁsOe9x®8jÖÇ^©ÛK\x0010Gåå'Góð'4Z\x000bOgKò\x0019\x0011S
vmºMÁò+\x0018ÿàÎãÑ; \x001c_dÜ\x000ck3\x0012¾»¸@½\x001dtã²w*Nã% ¶Ëµ/!¨n¾@üa\x0010Ñp$áYí5þClÄ]\x001dCç\x000bÂ17WãÀãp]YË£ÚÞ84ønønø2ÅãÄe6\x0015*Z¬uäw<äð~Á<0\x000bãlLråñfõu\x001e¾¿XñbÐG\x0017Ñ7æ¹Çxeæ±Ü0¥\x0012Ë×|¡êgÍÿûÇÿ\x001cÞ¾Û÷Üª\x0002OÂ´¨nN¯æ1\x000eÏgµ­øàðÍÓ½âwË7s¡ê\x0007Ãû±aÙ¤I\x0016è1C­­jP¦2\x0003P\x0012eòw´XpMï!´,¼Üz\x000ewR¹ÊPÅ84ÛlÜ£%`å\x000fh×P*P¡¶LÞ6l+]lå·ÆÑ÷`\x0001,^ñ\x0001 -^y}sqyuµWR`D\x001fÜ$K\x0016J\x0016Dkß<6å\x0005¯ÏONvi\x001b3¬¹ä\x0018\x0017"+\x000bñ±\x001fÛ5ì^£©\x001aN
Â\x0019\x0016kÃq¤<\x0019MÙ\x00156Ó5\x001eÃ\x0012+kâõ*·\x0015\x0004S\x001e(·×tÌÔlf-pÓº\x0012¡Ô\x0008ò¬û îÔ
ØÌÖ\vØf\x0012Í4ÛL\x0017ÝXq§¬lÌh®sÃpªØ
l <¯²¯±ü\x0010ÂN\x0006ªp\x0000SÖYmÐJON,ÔlaÍáÈ\x0014~%ÍÍ\x0015£_\x0005\x0007­³\x001dó¶*^¬
ÓYzënc:±½ü­®q¹0æsSi8ï\x0005Å­û\x0010ÿº\x001c\x0006ûWÜ½tÏ1§*áx7M\x001a¥¸\x0010\x0019ÖíTh\/ù^e\x0005§¡ÐÐÐÜ¥¿Ú@ã{aÌù¦\x000fKÓÕwÝXnÝY
\x00031\x000f\x0013\\x0002Zk¡ARós§x|\x000c®qÀ0æ
ø¦%±S¿I3|o\x000e`öngé\x001a?\x000c\x0018gÀQIH¼ô\x001cÄ+JYu~(r¯í\x001aO\x000c®Ø§©4\x0019?lñ&wkÜàdãMä 7A¡¶PâK\x0012»\x0003¹)q\wÉf¿ÊÁýª\x001dç\x0019p*En½pMw·
\x000c®Ù¯rp¿êj¦bñ.(³\x001cS+M×lX9¸a#ß\x000c¯²ü]Ë\x001c\x0000\x0003ë|l¶\x001cÜ\x0012zqÚd­¡R\x0001gÖ}VÕ^i\x00067ò4¤Qé2l	¸é3XØ\x0011¼­ù¨jð£*Õ;rI-w
@\x0019\x0012ÔÖrOÐ5\x001fU
~T\x0019ÊUÕJ\x0016Ý\x0003Q\x001c\x0017ëBNÝz0äEPYYÍÍl T)øël§U§\x0007Wô<\x0001\9(W\x001cQâ&¿ò.¡\x001b?¬\x0007ý°\x0002\x0016àÅ\x0010J3\x0011¶ô®tuºÙ\x0015z|WPl¢¼,§\x0011³\x000fÁ¯\wÍ®Ð»B¹2\x001cÍërÕ\x0001ÅÝ!B¬ëT{L¨ás¢Èád´ÀÞÍd4³Æxõ»vJÒìÖk¾jÛÊ\x0012\x0015Ý87EW?5PhæåÜ+°EodÔ^	Ælî\x0015ë\x000e
)7¯^é´ßü0ömivÐë6&¦W\x001b",gÅ\x0004Ùjß]Ü\x0010Ö1^§F\x0007Ì£S£¥,\x0013Ä\x000eQ³Ó\x0017{\x0013Õa9(&ÈVîö^®¡)EÃ`ª\x0006S\x0003`ØM¡'¡ÅæY&\x0015¬®\x0000Ó5\x001e±\x0018Ø2ôÇk~P\x0006 \x0001l×ñé\x0004s5\x001b±+zÞ2^c)K
¶Tí¥©½`¡\x0006\x000b#`VJ|\û|1ôeÎÔ/Y5Ñ\x0004¹Ð½\x000f\x000cKK¨C@>"{\x0015í\x0006Ø.w©v·å\x0018Çô#É2êVcÖ"\x0010Á=ÿ;ÞJ{mÕø	\x0018q\x0014ÊÇ\x0006ü?bq`«ü\x00044~\x0002\x001c\x0005NMÈÙ.1\x00089
Misï¾Êd£\x0011OãC\x0003{
5§kJ\x001eNø}Kì^2ÛÙ\x0011²x/µt\x001a25ÞéùÖ¼]¨Ë7\~Èb£4¢¢\x0013\{[vz¶¤l¼\x001cò\x0012²\x0014mbêÈQ\x0002DÀæm»d¹d{v\x000fíIYÓ4Xj=
¶L3Ý^vÖI¦¥¯¾.ª8èÆH³:.0WüØvUà\x001e²¦4-Õ¤î='Ëq¤ã\x000eu\x001cÆ^l;ù=½YÄÞ,bÄË\x001f.ßG¿ïsôÎ,±\x000b&;\x000c[Æ7ûVó¢";~|ümü»ÿu?¬éä ¢Dº\x001c\x0002Np\x0016Õûõª\x0006TÁ$!÷lAàü½·\x001cjx¿½Ï~\x0004P×z\x000cÐ\x000b\x000c¨|Ù)®¦T%\x0016r;¡~@S\x0003A@ØLÆ®]GºÎºä`{Yð\x0008 ­\x0001íWhAW\x0003ºA@,K7|ì\x0017\x0005o©XH1H±]#y\x0000Ð×~\x0014PùòÜ³$ó'Fý¿Rh°z\x001a0\x000c\x0002jÏ7Rf¤3²¤\x0008å\x000eIä~ºêÊ.Z|mxí	2xx#Lé\x0019òç5zs¥W;\x0002ânBÛ\x0010ÚQB¬®®Ð,1©\x0006V.Ø\x0011\x0018÷\x00136ç\x001d<è<öNêÍ]\x001aHïÚæq±½ôw°q2vÜË\x0008n¤Äöö¬¡qúp)-Y{\x0014Ûf\x0013ÛÑ]üo tÍYìF\x000fc)Ëã!^$yêÒ\x000e\x00180òZG\x0018Ã8ÆÿzBhOcüË¯\x000c±	÷1¢Yû\x001dQõFf\x0006;@é&nSê/»nâ\x001dÚ-Â~|å©\x0001]ßÞüõöbO|@yýÜ¥\x000c\x000f\x0003\x000eÀJ.8sw+Þ³Ó7gÿùæh_<Ñ©N
Ñ%eXÊ\x0016`Ï» ![kJ\x001fÄahýxºÆÓxBü é¼SAÒò¾ÃW÷ã\x001aÏ\x000câùeÖ¹©\x0017H¦G\x000bÍ
LÖoï9\x001eÀ³5\x001dÄÃ!X¤\x0006b4oFv+·CF½\x001fÏÕxn\x000c/ú£ÒG\x0005'<Ë
ÖmWÁ\x0019Àó5\x001f´\x001eJ¡Ò·\x0015´qã]¤\x000cëq;4ýûéBM\x0017\x0006Âd;E\x001dVxãOkÍJ·R\x0005ÒèôÄ \x001e¸ü ÓÜQ¹;;íZ¾Ö)yåxO*\x0002[id\x0014Ýdé<µ;îIý|[A¿,½Ê5ö42\x0002,\x0017Ê¨¨íñU?^ãaÐ/\x0003J<{ú¼F\x0005uEO|Gr²\x001f¯qË0è1Ã\x0006aÓù¤.ËÂvÑÃ\x0001¾Æ/Ã cÆð^\x000fRß3Ï¾\x000c,Ûéçk\x001c3\x000czæ¤éF»Ãj©âêS%*\x0010Ûcª~¾Æ3Ã kÆïkù`\x000bT\x001a¿o(\x0003ô¶7F\x000eð5¾\x0019\x0006³¤ \x0019ep,\x001b¸\x001dO¢Ýl²ñ|rÔó¡Ö>Ù.\x0006¹ÔHËÀ)\x0004»+^îçk<\x001cô|ØB[\x0017\x0004u×éMGÊÚ¥¹q`Ä·¸qô\x001cm&×Bç£®h\x0016Øµ¾¯)ç¡ýÛ}ø·ðRpX§VÅWço/RÛð³«Û=w"É¥1·:ú?Í\x001ddµÉ¡ÑJyyrøä(u
?;9zsÖ&k4ùU¡©\x001aM}UhºFÓChKð!u#\x0005¡hà7é q2S¯Êh¶F³ch¢tAa
£\x0015~áå*4W£¹14àñ\x0014ø=é\x0017ë\x0017Ë\x0007ushrYl'e3*¦\x000c¶¹¹¾ÜõÑJó yBT©¥d\x0001wj*q@\x0019lsvz¼/ñ#µwR6£cF0ey+÷LÉ_¸}.¥T5¥ DÝ%\x000cX	Tµ@GÆ»í3\x0013¦f4_!c;ÓB.gZôb¢4O\x0003ñeã+Å\x0011jÕºôKQ\x000cG\\ß~N¥´/¯?ïÛ×ÒQ²\x0014P{I3\x001eµâ{'ÛÞÓ7¯S\x001díËÓçûvµ_N¸ðyÂE'\x0016mÐsB\x0017sî¥1Ô­êuhÞ}G±T¥\x0006¬¥Ä#^Û\x0000\x0015åIågN5ÖÒ5\x001eÁ¹\x0005\x00140£Lg-þU¦²Î®¡25\x0019¡ò$ \x0008R©2 &Ä{gÛ±TT¶¦²_\x000b«©Ü\x0000\x00156ÛL#9é\ÐÔìé=¨5X¡Æ
\x0003XÎóÔBFN¶ÌÙð¦\x0019g9\x0005­Ó\x001aðZFXþ8$"õÅú}\x0010zwfiÁÈÚÒ&K:æ\x0011­,E
\x001dÞ\x0019·â\x001bVù\x0011¤ò\x0003Æ×SíÈXæQ[\x0017<[KN»\x0007hë"W>#{í\x0015L~	\x0003¥\x0003;yÉ&Þ¯Âj®Ìz`~O:ç\x0017Çµóx\\x001f~¹øH­/ÿ÷ÿ9½9ÿ|}y³·Hòð3ë\x0005)?cã\x001fkFÙFz÷ð»£\x0017Ôÿrpzvøúôøl_m#AÊ\x001aRC\x001akiá¥ë\x000ciH© Ë%p5¢ª\x0011Õ\x001dqlE"\x0010%Õ\x0008\\x001d\x001aÏõfÔ5£0cô¼¤+¢%¿(e\x0002ßlp\x0014åZHSC\x0005i¸\x001fÅá»,\x0005lØé-ù\x0010\x000bÒÖvÆ®4ó\x0006\x001eÊ,¡ø};ÊÎÏÕ|nÂZðX7ËQq+4\x0005½ð\x0000«Ñ×~Qã\x001bm^\x0006tùÐÅÎ -ç¬^\x001aÑ=\x0019K2çK
\x0008\x0000\x000fTv­%ekÉ<\x001d¥¨ßó=.^',OâIÒëÕî÷aäð'W\x001f\x0008\pÜ\x001cCfö®y{ÀlÂôÉÅÔGÿ\x0017n\x001f\x0013\x0016\x0007wô\x001aÍCËÉù\x000fçû:\x0011<¦_\x001d7¢jzÍK
¶\x0017
\x001c>>ÜÛ@d²&#d\x000e_Ì¨\x001d\x0019[9ò24¾T¹Úí:þÝhªFS\x0003h\x001eÇ2P;\x000ef*¨G(p7¡æ[g5]£é¡ïiÊa¢\x0015KUc´ÍÑÍ:©^2S\x0011²`$OSÕZ±öÖqÑøuh¶F³CFsÅ>´
<Ý\x000f\x0015\x0019m»¾w7«ÑÜÕ´k:<Ëy+ØjnG]^/¯Ñü\x0010ZR%»À\x0011`ô»<\x0014qGq@/Y¨ÉÂÑR`"\x000bÀ<ÞpÖ\x001dÄ.¾N´zh^XÔ\x001cÝÏÆ³ðÉ\x001a½Ueºêºï	íQ0v\x0016\x0004Ï}7F²3V\x0012\x001b(¹êBs\x0018ÀÐiTó rÝ¶ù)Ñë\x0016\x001b4\x001e\x0017\n°\x001as®\x0019
XtÌ{¹\x0019»nµ5
<[¨\x0006A\x0000ÏêQAx>ßå>Û^¶Æ}ÀÿÀwÃr  >+ÕÌÚ
Úöâ§N4ÙlR9²Iq||q ÒP[~Àj1:Dw4Øô¢5«M¬¶%»lÛky{ÙÕ&GV\x001b\x0010æ¡\x0004ZY\x000eÙa%lavA÷²5«MVëÛµö$jà]Øì:2Õ,65v" 9\x001dñNñ\x001eõNð\x0017õë¢IÕ¸]5ævQ,\x000bè^íXy/^Té\x0007iVù]Õì\x00045æwf1*£b@w©\x0017åÎ¯Öù6Õì\x00045æwÿµlr±K\x0007·i<	J²$`£hö¼üø$)×À¹\x0016n,àÅñhÅH2+OèfG]]'kn}ø#\x0001-m\x001eøÎÙ\x0015ð Aær¥`ìzB@®\x0008OÑ\x0018xÒ\x0017u±\x001db2pº½.ë±\x000b³´,y®s G\x0007C¹`íè¶ìk'z;µ÷f\x001a0Hâ\x0002§\x0012÷ZËÏ\x00161:\c:æÕ\x000cNÂ\x0014M37éwÏÒ,f&!`[Èù»\x0001úeË·	®O\x0007g_Î¯ö¾Ê:Ng\x001a_f¡mþÀë\x001d³ÐÎ¿;<Ùû¨·Ìqù6Çu?\x0007>\x0015°aF
]\x000c+Ûzµk\x0018_/ªÙÔ\x0018°¨4\x000c\x0017oÑ*\x0007èqÿò\x0010¹íÍ\x0013ýlºfÓcl>p¤épð|þ¨FñUU9Ø1¹©\x0017ÎÔpæë2­Ùì\x0010.6\x0014½2WÆòë§ò»Fº÷Â¹\x001aÎÁ¡¬­'8Ã{ñjÃï#~{\x0002¢\x001fÎ×p~\x000c\x000eÓ©ùõe,¯2<Ë«°c\x0006`/[¨ÙÂ á\x001cÊìfÃ)ªß4ÞòS_¹\x001bjµEÂ«\x0003Î\x0016µ\x0014­Åùð·$mý®½líÙ0v8Äÿ1fbÔ¬æ\x001b«\x0016»ÆÉöÑIÙ|U)\x0007¿«
¬\x0006\x001c?"$\x0001\x0015[N­²4\x000bÆ¿\x001csÂÀ*\x001fÑkP\x000fLtÂ_×Ý\x0012vY×lå¢ÖãüàäòßþysþùòúãnÆ\x0014nþS.«ç
6ì\x0000Üñ.|xprüøèìðõñéûAU
ªfAS=\x0005x\x0013ã¢\x000f©y.¯	aÇ;á\x0018©®Iõ\x0014©q¸së\x0013<rù³ËÒomÓ3;MjjR3E\x001a¯ÞºSQ5Àrí\x001bwnË`\x001fÔÖ¤vîë+ÔÎË µyuiÖòfG\x0011È\x0018¨«AÝIå#K
ÝXhA\x0016eQ\x001akýú\x001aÔÏY4ä\x0011®¹±LÐ~2ÜÙí@=È*
5i]¥;ø
õxã*å.`÷ >ª:Ã­\¯t\x001bµ<uÄÿÏ1P\§dÔèòÍC B
sV
eP¼R\x0014¯y²T¼ <Ä÷ÆKÁÒcò\x0018Z2k#J\x000fä¸~hv?Ìm½Ñ#@åb*ê/2,íëå,©l*'}ÿf
n»²uú EåEqd\x000cITEå¹òß³,x\x0008*\x001b7%çü\x0014*oÊñ\H\x000e®è\x0017upî¨TL(ùWGQz.à\x0007!Ñve¹®\x001ceÛÓú\x00078óv-ëÜ··¢xþÈjÕ\x0016ý¶{µÉZn\x00181¬áÙZB\x000b®DÙhJÚqR¢Éæ
ÿÎ[%\x000f`ÇÞQ<ZgM3*þ¯ð\õbF\x0015u+<2~¸8¿ÝHÅì\x000c5ÛbÚú[t\x0019\x000e\x001a±>Ül
\x0019\x001f\x001d¾¹\x001fOÖxr\x0014\x000f¥£è\x0001$Þê³LRÒ\x0017<³­¹{\x0000OÕxj\x0018Ï°\x0006òs[JrÆÐø¥	<]ãé¯îãÚ\x001aÏ~=x°ì}\x0001ßtzß¼ÿÂù/ûÞ$'ñ±\nf-áN­íÓgOO_¼8üÓýpªSCp^h®Ò\x00131Î$ËÙÀÁ¥mLÀé\x001aNYÎ\x0002ïYaXÉVY.!AºØÚ0Ý\x000fgj83f¹xà±å\x0014ð\\x001a'7§³»3×o\x000cÎÖpvpÍ\x0001\x0018I½§¬9V\x001c\x0014Û[öûá\
çÆ,\x0017\x0011h?HÇµz8M
×¶³ùÍ±-÷ÂèT¸ÈQì7ëàª{6ä6!Ë\x0001Â"sßwÜ­é¬[K×ú¹1GçCÈ²â()\x0014ø¢ê\x0005Oº¶¦y\x0003 
\x001c¢Ã\x001bO\x0019Tï¸»Æ\x0003\x000fE´í\x0014	ºÆ
Ã\x001f\x000eü¶tæ\x0011Õ¯jÖ¶M]þ\x0008]vV,^ÈOÎ¿|wyq³Oÿ\x00155¦yú[°x%M]?26´íRÉ¯b\x000cúÝá§ÇGg{Åì2Ä³bñVÞ\x0015rPJH\x0008\x0016ëÈÒïx¯\x0019¢T5¥ À:C:#Ê`}Ñ|Ù®F<È¨kF=Î\x0008vÓÀ	ú`e\x0010Üê¸Öc\x001aÓÌ`\x0006\x000e®P\x0018)+FL[¬¹«|£\x000fSØÅöÁS¹®\x001ez|qõ\x001f7{bP</Ë¨RNg\é6ØUûøèäàðøì~8YÃÉ!8ó\x0008©0G8dËÃöÊn8UÃ©1ËÀù\x000f5XÙçXÉïý"ìPíÓ5\x001eGTàg-ýgÊÏº½\x0012±\x001bÎÔpf\x000c.\x0006¤T)ª\x0013\)\x0011xóÆq{ÉZ7­áìW¶æ\
ç¾²Ýêk8?\x0004\x0017/c<MËÄ$MN6Fs\x0007YùUCÍ\x0016ÆØ¼àv
ã&)âVàÌ:ÃU3®>ñ­¹¶F2\x0012mäï¹ôÜ2\x0008tm\x0010xðüüÓ§ëÏ÷\x000e\x0015\x0015¹
\x0016Bº¿Q\x000eR3vfÇA{ðüðÕ«Ó×¯÷vS/?×\x0006]x67E<êAd@q3r{Ó\x0000ªñÔ\x0018ò>]E:\x0007<ÇÓóc£ÙQ\x001c6\x0000§k8=h;YjK|\x0000\x001eî F¼ÙáVúéLMgF¿¬ÉªjHç6òe|52vGYý½x?Ä±Ù\x0017ãß ¼÷åÇ||v\x0015ùÎwÃÅ¨ävLÑBT\x001d\x0016Úyâ/O\x000e_¤¬ã³Hv¸ý±«0ÉI\x000e0Y\x001f\x0014=\x0019P\x000c¥ázº¶~JÕTj*Zd¦0!¥\x0018ü¯	+L¥k(=\x0006\x0005,\x0017o\x000c4OÒX\x000eoaÉÔLfIgu\x001f\x0010.ég$ºÁZ¹ÂP¶²CPØ¹\x0015\x0017E¼þK©HÎÚ·[pÊÕTnË3\x0001pô\x0006Ù{\x001d[U¼A*_Sù!*	4+þ\x001f©
HÀ\x001f°©~\x001b
5T\x0018 _ç\x00014\x0017HËµvS(Yvb\x0008Ë\x0018Ri\x001fPS± ´,ÐÿË4VëÕGÜºEY\x0005\x001fÊ&Å\x000fk6!4\x001d<{Ð²[EK¹ @²ð\x0015+Õ8v\x0018óì(ßiÉµ{*ú%EÚ¤ï VãÚaÌ·KG\x001do5¼´\x0004\x0015½\x0015\x000b¾qî0æÝ¥ \x0011\x0005Hóx|ë\x001dZÕýA¬Æ½Ã\x0017ÄXãÑEceiÌ6ÆÌRk©Ü\x0010CÝ®t#²Xú?¡â:-snöp½=wþéóÍ®¸\x000f5¿\x001a´\x0011/ï\x0004*Áä
\x0012ì\x001dÏ-FÒinÍ2w\x0014Ù\x0007áB\x000b7âí\x001dÖÞRc@Ð¿§\x0003[(\x0011\x000fÃùÖ·ú±9:WG\x001aN>k´\x001cKTÆ#r\x0015[ë`ýëÍQ'*$ÙdI\x0001=w\x0003\x0006å÷ú{à¤n\x001cþåÈnðò'á5OÚ0RK\x000ew¤ßÿQï¹\x0006I\x001dZ¶á\x0015'YxÔÒ\x0008zéD\x0011ÝµjÅ^­Ôr@Ô¾\x0012Ë!Ì÷?ÞÁûñkáC\x001füýùÒ\x000bÿþx8Ù³Mü@~ÀÀwÓ×7ç_.n>]þöÿöªçÅ[\x001bI­)ÔÉÈÉÍ^·,^y}vøÝÑÙ+|öÙQm
Ë·\x0001Èo\x0003\x0003Pøn!K¯} I?-x¬¬]>æÖT÷ZËÖ`v\x000cL\x0015Í<\x0015¸d\x0005*ywêiÈ\MæÆÈ<OP8l\x0002ÈdÄeÅ*ýÑ×L~ÉéGW
PÓ
 bÂ>ª=	c½|RÔm2öêüàñ9\x000eFÚÍ&­¦Ä\x0005VrJ<ü¸\x0015Öì\x0014\x00109x|î\x00075 \x001c\x0004T1úÎûÒÅs-D´\x0019ñ\x0001ìÒéèæS5úøY|à\x0018>S%Í\x001f¯?]üüÓÁÓ«Ï\x0017WûÛ4P¶ç:\x0006#4<}uôò\x000f\x0011ñäõÑñÉýtª¦St¨dOU±²\x001f¾\x000b0YºQ:]ÓéQ:Éú5*\x0017Ng<j^î;\x0019Å35\x0019ÃS\x0001ÊÌ¬ý\x001f\x0003\x0004×ªÚFe\x0006ÏÖxv\x0010o#	§æDà×ÓË*©Q:WÓ¹Q:ÍS
ËUéhuå¤Xÿm}çGñ\x0002GÙx¥±\x0008\¥²³¬Ï\x001bÅ\x000b5^\x0018ÄsEÝAiÏê\x000eÅed=¿\x0012¯¾4¥º±¯\x000c¢Æw®5¼sÝÊ\x0001­O\x001etÊÊ*\x0016îPVp@ M	6ïÔqâÉ\x0006OZOqq¨áö\x0014°­ëåÚ¯Û\x001c\x001a0xj`X\x001c
\x001ep¨\x000ePðÁú(^sjÀà±W	\x001a±\x0017¯³,-\x0006e\x001akðk\x0017_sjÀè±A=õÊò¤X\x000cÜycx·òÄæÌÑC\x0003?-E\x0004®Hdñ<.\x0017Z×\x001c\x001a0zjhÇ\x0015Gâ	 Í¦=då¡\x0006Í©\x0001£Ç\x0006JêÓíÇ\x0003é³$9]îýY×
 j&\Ì¢©b\x001f§Ê°gñª\hW{>ÓJ¥ýæÞ\x000cQ¨²iR\x0006ð4Å5;X-K@¨\x001bm®o¿\|ü¼'$
P®·ZRý\x0012<Å6Ø­\x001d\x000f§o¾;zñú~*]Sé\x0001ª*rÊ ÊºÛÖ#ÒKej*3@å ²1^¡2(éxtr¤ÚÖEÐek,ûûB·¸+Fãs×ÅÅ§£·×WûÊ
\x0016\x000b\x0018¢J\x0002T2«×m°TG¯\x000eì­z&*YSÉ~*\x001d\£«\x000cO`ÃÁ:|Atw5¥j,5`,åJ\x000f\x0003(î§g\x0017¯wåïôº
`é\x001aK\x000f`då0%%i¦¨ÒG\x0016ô]8\x0000ek(;\x0000%5÷A)\x0000RXÔL¶ºÓ2@åk*?@e=ÒKîjS¡ôðÂvÀ\x0001¨PC~(\x001bMEËJâFµ¥\ó>¬ØÕ
]\x00180V¼RÐ(¤¨\x0002û\x0016ÉXr\x0005Tã\x0019`À5\x0018k¸\x0010W¢$-uê\x0006Å(·´­ð/û¹p ]ÆÂêåü	A±­ÄÜ&ôËT¯O©Þã\x000f?Ç?\x0019Ï³·{Vp6sG(ìÒ¼\x0007Qì¸>	¿<ÿ\x0013Ï³£'÷SÉJ\x000ePA	³tô¨$1¯à¶\x000c#Ì
,Uc©ß\x001fKå	\x001d6'têN?zuùi_\x0005k\óÉ4»-é0´¶ËÀ4õ¦\x001f}{rüj_¢ÐT¦ÆÐâIMAM\x000cñéb¤D5ñþ®\x001f Ó5þªfj4óU¡Ù\x001aÍ\x000e~Ï"À¤³¢Dþ ¾\x000cB\x0011wýë\x0000¯Ñü\x0018Z¼ÙÊÍDHE·
\x001fXF\x001b\x0005ægÐY¸³\x0018\x0010Óôüúã§Ë÷\x001f/no\x000e^^]í×/òåÙ ú\x000fò¶XNÊAkXF\x0017ÏO_¼::þöÅÑ³§Ç''{5VÜòÝÅw1L ÒÄzî\x0004W2àwª\x0019L]cê	L%Q\x0003ßÀYYS	>QÛñl³¦Æ43Öa$g6L\x000b%H²w.3¶Æ´3Ö,3@Ò£\x000c[So^e{g\x0002³`¹IÞ\x000fqb±\x0019gÈKWªP20ê\x0001¾zÅw,þ=-U+¥Ì-ödÎ`nr³qI0ã"
lrÒ,úª8\x0015âï\x0004ñ3K\x0019¤Êd0| ³ºÕþò)½¼³ñI0ã´gu\x0000\x0015\x0004\x000fÁ\x000b¸S3ÃÙìvÙîÈ¹\x0011[0fÉ	ò\x0001¼R³võ(§ç\x0011]n£K\x0016xn¼óÜ9Ä\x0019ÚKÁ/®O¯Îo¿DØ})Õ½àÕáï"j\x000f¢¬\x0011å×\x0008jaEÜðÄçù»\x0017ûÊ)Çwö\x001c\x0017¤\x000bw\x001d`±Ç¼çáÓ£\x0017G'»ô\x001cHÖDr(ÆßÆT¬!E\WrÛòÃ]Dª&R#6²aUªHLD¦ä\x000f¿mÙ0Ýûét¥G\x000c\x0005¬árÖd(k7Ùám²2½X¶Æ²\x0003XZâ&]8É"v\x0013ì×Ì\x0011,Wc¹\x0011¬M,¨SS²ÄXF¯ù¡¦
_ËÒf\x000fÂÈ&!)WGâú;!©Ù*\x001c×Ëe\x001a.3Â%
×f\x000e¥8MÃÔ\x000f);å61èoð\x0015ãìúösº\x0003¿:¿üøù?\x000e?¾ÛSS\x001aÀ)ºdJLRåÝÄÍé·mÆé×é\x001aüêðøÅëÃ\x0017O÷V&F©MÍ9\x0008)AbÂ\x001f!\x0003z¾1\x0011!E£\x001e2\x0007i[H;lIër
¢Ôñ3g\x0015¥¸)´'FÝFðãÍ«yd¤WóÁÏ-éi@¢»æÏM5/aÑ÷<H)u¦ÒTª­ø¦ùñíåÕEÜ3:ßWéâ	¤³#«K°(¦þÔ3ñuóÅã£¸y^ÿá°TÕ¤jT$ÁÀßòìu ø2TzÐç\x0004ª©QÍ\x0014ªá9¦¨e\x0018n-\x0017Úé\x0007áô5§âÄ\x0014\x0008Tsð)ÁA»þAP«£F\x001an|\x001deEõnW¬°Å-;÷Àj_rÙ2ÉÚ\x0015æìjeyGaØ²\x0002Ô²\x0011|\x000eµcØâkFmV[\x0001¶\x0014wcÖ¯ÆgYE·½ÎWXhå\x0000øãÕùÏ\x0017{d|´\x0011<\x0005\x0014su4{N\x001aYÊD·Å¯\x000e¿;z}|´GÄÁd
&GÀ¢éøI?^Ü99gKñï\x0002µ«ÉfQ\x0017LjÈX²TX
µä'KIí`­ßVºæÒ¶âôµ1ÔòVÙÊm©ê´©Ì­,
Wåd °ú,åÇ~[ÀÝo«PsA[Y.ÍRE6¾®b ½È\x0010ª\x0000)õ÷\ÿ²W4HX[óºr¼	cP2§wÓ\x0016¹¹çôO{\x0005Ä²¬F¸ú®\x0003\x000c6EÚ'fC\x000cgwÕ(pUe²x
v\x0003`iÓ÷å]	Xc\x000fÔ®Ê²²
Re\x001bO?À«ÜÍåûç{òb&8*;`8ØÓeWÍk\x0002=ÀÛÜÙñ·/\x000e÷&Å\x000b\x000c\=A®Îú,w,£±-\x0007#ZpM/Ê\x000cªñÔ¨ñ$\x0017\x0015KQZÈt\x001c£·¸©àöV]éA2'I\x0000\x0000ç
rþN\x000böúnûø\x0011Ã\x001aÏáá|VCÃYªç*«®)\x0012\x001c6­Éì á|\x0019±\x0003`¸ÚS\x0003ÛÍµvó5\x001f§£î\x001d¤ó\DÅÊmÊó&ð Ù®0¸_£uX=\x0013¼g;­¹ÌÞK»mN\x000f\x001fÀ2h\x0004Q\x0017	\x001f¼¾ýxquu½ç`p«@ñusÚ\x000b7´ßV\x001dqxðúÍ£Ól?DfK<Æ÷SÔà»¾ýpý\x001f/.¿\Üì.{ö`Õ÷HP'riàÛ!ºè
ëÉéç§\x0007/¿;:{½GÒ!\x0013K"ÂK/R\x001e\x001f\x00001bõä×4HIDª­\x0002\x001dAàk$üËN¦ør	ÊOJÒGÓ¥:Ü´wè\x0011¦ø_­1\x0013Î&êµÍC#!«âýh(\x001ee M;u}\x0004ÊÈ\x0006ÊÈ~(+\x0019"h9InÔ¶h>ÄäZ&×Í\x001f´÷cx&d2åë95»¢h ð/{¡°Q)¯rì±¦U®IoßÅÐGÎ2ÉÆ\x0015à_ö®r¡¨i\x001e\x0007Ùd­u\x0015J<æ`zA)ÕÚI
}<\x001dµ\Â\x0018?\x001e%\x0004j5-\x0006 \x001aÑ\x0019ô)\x0001Üi©\x0018¹ÒÞ\x000b\x0010ð<ù\x0003#X´´­	\x001fôU¯\x0014ûÎ¤5ü¯v{Î\x0018\x001cy&+ÑÒx8ã_~óôâËùÇÏx\x0002~wyuµçþá­¡JT\x0013/·Ô\x001cíÄâÇ®yª|zôÝá×xþ}w|rr´±\x0019ÿ/\x000b2hÉ`Ì\x0005¼@&4lÕ A?SN\x0008Ù X¼ùÕ`øý`(\x0018
l3ÉÓÉ
WÝ~\x0005jL®ZýdX\x0010Dúó*Ðð¸\x0013¹r\x001dôä×Ô6Å~}ïHñ/¿ÉÏ1<ÿðaw¿NÃÁ(-àDêQ\ÖsÝWÐT%æg?\x001e>~ôê~(h¡ \x001b*\x0014±¶xeÌ3­·>£RÍ$â.¦x?[Ö¥hO\x001a.Iðéú\x0016åQ>ÞÓ\x0012á#\x000fW÷¤é[ÉQÈ2u\x0016\x0016ÕIðéô
j£¼~\x001dÙò5(ý.©TM¥Æ¨ 2\x0014'\x000b¬i ¨%Ü4©¡Ì(áõ.lz\x0017ÏP|ói\x001e¥Æ°\å\x0006±¼C)¥|ÑöT6ª9ÕÔæ¡Ç¨|Må\x0007©âÙH5ê\x0000\\x001a¬\x0007:;ý
«\x0002VíyD@?+K\x0000\x001esø9äâ\x0005oÃ\x0018ÿ^/ïßÓÍ°Òxz|q~ûéú*73³7óß¼¼øõâã'z9Ö&×ÈÄ»\x0016Vñä÷máóKW¼©Ò\x001büÑ^¼b}¢ÇGo^ìnenâ×#H¨4§"vï28è9#Ù\x0005hW E_ ¬)ÔL\x0014£Ü¤h\x0000òL\x0002$Êî|\x0005QtrzHØuÓIg9'éÐy\x000erDÊÙ£\x0015Dñß7CD\x0001òñ\x0012°äDe#i[äÚÏ\x0016ÿ};\x0014¯ÈýB$àJ+Õ/De\x0011+¢\x000fq#H2rhÚoR±aa¡äÄÚý\x0016ÿ}?d%çùÃ¡6¶\x0019Ie\x0011°¤W»èÑÂÎÍ'ÑJBsù¤7~¸<¢d\x001e	v5Û¥IGy-	\x00141Èk):\x0006ö\x0001rÿZÚ­mxÐq\x000fyniÓ¨ª\x000cdIiÝH·\x0011h­\x000bÀ\x000b\x0007\x000c¹nýubJ×¿DÃQ"È	÷\x0015Hñ³Ãë!ß÷"òK0Ò\x0019ZIÚÞW E+Ã§DQ\x0000}@}ì\x0003dqKâ¸\x0015LÑ'Á_RÒæz\x0007-B\x0010¤¬c\x0014hZÞÆä\x0012û\x0015Lñß!/ â-%éF¦<¢-3)þvR­\áhg9´ëP¡3ÍÿLovF8Wd\x0012zå\x0012Arh+ì\x0013õ)\x0006º¾Uôí´7+·\x001d¦îäØ\x001a÷\x001cÄ	Ìu2SàøDO®ñ\x000f?¾ÿé£­B]|úx|quuñ%Épn£Ñ\x0002¥\x0013Ò½I¥¡R¹tÀ\x0006¤1*÷\x001fg\x001a|ôx|trrôÝNùÍ\x0006$\x0007¸] ñ.qU\x000c\x0019=åxpd\x0016£¥óó 9¬í³ñL6bÙ
\x001b¬cÈ:Æ\x001eåÈÁlA¬È44\x0008ô¾qfH5\x000fcØ>8å2£E"H\x001eÅ\x0011OwO_&û0\x000f#×Î%b²'\x0016\x0001M;Çá\x000b\x0018Y¦ïÍäxµÏ"^¦ÊçÈ\x0011XkÍÀ+Õ{=cÔ>{Äë²Ï[Æb!o\x0018ª\x0012Hô)+ì#Ó>\x0010)pn}6#¹m¯¨d Ì4\x0008Ç£KÄ1µ,î\x0004I®DPî\x001c	E¢}$ÉÇGø@\x0017u'LY!ó;CÏßßpÄÙíÞSj$qürî]\x0012	iyÏP Ùi\x0013\x000b\x001e#R$t\x001em\x0005»"RóîÃË>\x0012_¶Åûx^%\x0000L¢L\x0008Ó$*n\x0019Õ½mþ\x0005ëä/ïÔÇÿ®ÃßþùéòÝÅÇ·\x0017\x0007W\x0017\x000eÿ|ù\x0019¹>íIR<
\x0004ïº]\x00079I}ðú\x001djÿvôêøéÑ'G\x0007'G¯\x000e\x001c¾<~»Ä\x001aBS¾bB
`¾bB
mÆ	-]d\x0002W®Æ"Ï¬M«\x000eº­\x0019
	4ñ"õ`i ®)çk«o\x000fÓt\x0014\x0001M|ZÉ÷wüh\x0015?,g]\x000c)I¯£¨h\x001c\x000eçy¢ó%{\x001e4ß\x0006\x000fGÑÒ\x0004ÌSï"\x001eªÎPØ;¾@{ý\x0010x\x0014Cã¡Ø\x0018¥f$©9D:¾¶\x001aïz6íVº÷?þ\x0014þz»¸&¾»=ð\x0007ÏÏ/w\x001e\x0010ñöí\x0015\x000f\x0008aèÍ/FXâªøO,âª§oð?òðx§ë¨@6×Äß\x0003äV\x001f?|¸\x000b\x0002!ÜìúHñ\x0016\x0010ýiÈá·ÑI\x001d&]\x0003\x0004ÞiXá\x0004ÿ3\x000fÏvûÓesUìbÑ\x0008\x0005\x001fd\x0018ESt%©ÖxesIëb¡Î\x0008\x00134Ýä7vQÂÂ\x001a\x0016óý\x000fèÎèÆÁÄOÆ_¤\_Á3àyñ7ð²^3Üúäüöï;YMõ>Å{É7XË­äR[\x0011ê(Q\x001c¾ù¯\x001e\x0014Z2_\x0003
­¯\x0001E¦b­øõïFtý7áo~¬¹ç77»¢ò\x001c»\x0019:¤~DgTp\x001cºúmõäèàåáÙÎ¾ºæÏÏëäwûóùF/Ät\x00138ñ3ä4\x0003^ós\x0007³`{ù^C@7ùûMoï\x0000}<Ú°
æþxºÃw|\x0001Kmð%\x000b¨8F \x0006ø%KN\x0012Äï\x000f=k@\x0004º·ãC±¥q/FH~n´rò\x000bÐÇýk l\x001cH:Iý\x0006¬â7X©Â\x000c\x0001öÖ~î·A4}0ô\x000c\x001cH×
 ·nûþø\Éï_\x00052d­4ÜI*}\x0003Ç\x0000Äì2Ì\x0011²küwû\x000b÷\x0016S\x0015\x0012\x001b\x0018ÒÏÉùÁóËO\x0017{\x0010¢Å²\x0016F7JóóQò¤âuB8<x~üj÷(¸\x0001ES¾I?÷3 W²	\x0001$\x0017£\x001a\x0008Î\x0006½a×÷øáý[
ï«Cóäúóå§O\x0017\x001f.°Ð3Þ\x0017^_ÜÜ Õ'vÝ\|úëíÅ®ç%-Mjz¸-çéõÖ\x001bU,\x0004UXzrú:Ý\x001a^\x001f¡¢Õ+\x000c~Å\x001bÅ¾Ù©Åâ¿ÿÛ{wó÷TÕîôsxõëùí.9Ô3É+8z\x001e\x0001<vÆ9))¿ä\½\x000fOþ|øfGe¥ÿ>ü÷_Ñ©Ý\x0000½oú9Áis>]^ï´
*]Ë| »ÒMlñå6çF×çy0÷êÕñi\x000f\x0003®]ëz\x0018Ð&O\x0016\x0019\x0002kôYéÉ\x0008Úxé'!<Bø\x001e\x0008\x0014H\x0015Ë\x0011\x0002»òõÉ±\x001d\x001f³Ã/Þª«´1\x000c\x000eùL{rþáÃùÎË­÷Êü
\x001f\x000eR<j¼Êµ\x000eýÉáóç»*m\x001b\x0006|\x001f\x000eê÷eÀ
\x0011ôïÀpãoßû´\x001c09~\x0012Ã¯çW\x0017wîL\x001c·Lyykx0Oô¨å¶¦êª«DñçÃ£×;14üzáÀ\x0004V\x0002§\x001fÄ¸¾ºþðÃåoÿÜix9Ëý\x001a8L ·à6áG×àZÓÓçw\x0015ªûïùùýÕ\x000f·Uöï$úÏg·\x001fÎ?ï¾)\x001a\x0005¹	¿#
U´^Ðë¢m\x0011^\x001d<{óüðõîïQ\x0011_ï 0ë:\x0010ÜW|¶Øàü,DÎEõ@ÄS-ä\x0003\x000eë¹rÈ\x0017]£\x0013¤®Tê@xw«åÍçtÆZ<c³¿þ6F\x001aïw>IDïdC^\x000f\x0011È{*'ÑVÑ\x0015Ì7ªqUßÆhãøÛ7»ÄÍß|w}ÑZhç×Wi\x000cíîÝø.\x0015\x001fã\x000fÇÝi*\x0013ãù¶X\x001aÏOOp\x0004íÍºaÁ\x0002\x0012o:Y\x001cö6æøGb\x0014©áD8º\x0011æ	|\x0014\x0005ÏSo{QPç
%þ¯9w/w\x0014\x000b\x0005z¥:Oº>Q((\x0000ÐÕ`ÞVTÓÅò÷¿üåo?%GµPø\x0013×íËËçïö\x0004ÉÔ\x0002ñòh¹":®ál\x0015\x001d¤k×íË£³ã\x0017Ow¯Û
\x0004?¿;\x0008´Nõ8®\x001f\x0011Êñ
\x000e(2\x000bÒHu	¿¼O \x0001Aò=òìâëÛ«Ëw×;ãP«UjlKKÖ\x0003Í'\x0003g(þ±\x0011J5çÌÙÑãÓ7'ÇOOwÇ£æó¨þ~¢U^_D=·\x0008LÎæÂ+t¸ìêq\x000e\x000b¹7|\x0016«òúèMZ°;9n¯¿ÜþpÝ7©Iìüýîw_%\x000c\x0017]\x0005í¸ØÉÐØïxÞÈöFÍaßö0`¾Yë.\x0008UÖTNã\x0002%9âÎµÒoJ\x0003(°aÄ>
ÔµË÷&§ù¼Á:x¦Àj9
\x0014ñ¾ÂËÜÅ\x001eÃ±`¨âÜâ[\x0019UôX=\x0007\x0001x·H?=\x0014ä'ñÏÓ(\x0000(¯	ÊÌ2`ÒGv~\x000f©²hdFÑMÅça2Xìj'¿\x0007`YDúéÁÀ÷7ª'âIÖÖ\x0006.[QM7É\x0018\x0005~\x0010Õ÷AðXäxl°uÞx~kÒn\x0012C£1t1ðeÇ\x0011¦x|Ø	L\x0001j"å#ûüÇn|W¡©ìÍsL""\x0013\x0014ø~z>IÝ\x0017ie`jò,º¬\x000cg`\x0016#3.ø_77\x0018båÃbgÄÐ¶T3ÉéÝ\x0007PúéÁÐI\x001d*û-Oj_\x0011\x0003ßý&ø/¦\x001e
¥²&\x0016D
*»\x001eÌò7ñËì\x0000\x0006º®Î£\x0004¥²\x000c¹Ï\x0018pdeÜ\x0018\x0008P^\x001c')0\x0008M?=ÆëÜ¬2Ô\x0001\x001e!h ÜÓ,E¾\x0010\x0003°q\x001fì-ÍC²X\x0017Y\x001eìg\x0006©Ðy°JÐ¨"38K\x001d\x0013V³ë²40jBBêèü&(ÐDuv1&ÏmwÖ\x0008Uª mÅÀ;-ôù®Ô E\x0018(z£\x000cí5\x0013;\x001bq¥q\x0013\x0012úö\x0012Uï|\x0004£OÃYéAì4d\\x000f&/
\x001f¯¹TÉê`\x0019ÃÉY\x000cÔXH?]t	ã
ayî[ëÞú¡áñ3\x0018\x0010ì\x000c5â}$§ \x0010ÃaGOÂ0à\x0019cÒk$\x0019ôôÓõM\x0014ú{àqKñÐõ\x0008ó³ÆÀc9ýtm\x0014\x0005?q£8l*Ì\x001b^ÿâFñ³\x001b\x0005ËßÒO×Ò\x0008|vY¹/a8îIÑ³·¤~ºNW£°Ê¿ãÂÇönÒã·oÒO\x000fF\x000cBéÄØ´\x000bS\x0013\x0002\x001fòaölÞQznj*7âª©©	Ä\x0019¾µJPcÖð¿êKýsUwòîàùùÇ_¯w&ï­Ñ\x0005ä¬Wü\x0007hÒ\x0004"p¡\x000e@\x001e<?|ñçÓ×[D\x00120õü7¸4ðååÅÍÍÅÁÅg¬²º¼8xr\x001bwZÅáèVªýÂ}\x000bTÒÎ'TuZ\x0003­^\x001e\x001f\x001d\x001d\x001c½Æ«ã£'oâïÎÇ*kT9\x001acA¾äê\x0018£p÷Lõ\x0001½y\x0010TU£ª)«J\x001awå}@ÞÐ	GÃ¦]\x000f\x000fªkT=gU%Y#ªñ¤®\x001b­ªx\x0001¸\x0007Z\x0000P$¸ÊzMõ]ãÄQ§»u´sÉdÓj\x001bzx·ÖÚ\x0016±ÍÆÒec]\x001f<;ÿ\x0005\x0015QöÊÐ\x0002Úµ¼Zs¤YÀ\x001c\x001e<;ü\x0013ª¡ì± ^n!]¶Ðï\x000e¥j(Õ\x000femi`ñ¬©í½Üqåêz\x0014J×Pú+±©¡L?\x0014jìÈMó"\x001dAÞ43Ïdk&;ðõ6ÞÞ/ÞG¸ýÈ\x0019=\x000fåj(7`(Ë\x0015/\x0000ÓäÙPåâêÝY#P¾ò\x0003
y¢|n,ô\x0004åKºÇÏ\x0007aá¦ LØ~vóÛ?ßýöÏË·X\x0017õùæ|wé4\à\x0012vÉ!¶ô8\x0019v±8¦\x001d==:;~5R¯Ï\x000ewW\x001c\x0015DU#ªqDmxõ{\x0000\x0012·å\x000fËå?hjD3¨,·\x0015x\x001c°C\x001bTvkaÔZDW#ºqÄ\G;Â}¹(Ë\x001f\x001a%»V"\x001a1L r©WsÕZ±K1°Ü½ÃÐný"\x0015\x0007Ë^yÎ\x0006iU®ÚRÉµÍ~
#E\x001eY9\x001a Ç[K\x001aöhÖ#6\ÆäPî+[nêæH-j³gÒ@ÏkZq²\x001cÁÖÂ\x001dNÆK¥#-\x000cä¢ôG\x0010I&5jqæ2\x0014ë=öX\x0010\x001eQjÛ«çW¬\x0015¢¼ZpQµÇý8²Æ\x00038tªX-¹r¬âÁ·ì9\x001eUó¨N\x001e\x001cäCMrÆy§¬P|µ
4º¦Ñ½41¤£Ø\x001cÛ\x000b±/Ú`äì×25éýZ(¡F²\x0019VhS;~±Ëh³ÇÖ<¶ûkY\x00121\¬r·w³_ËÕ4®ÆÈò\x0006#¤\x0018 ÑÁ©äR\x001e¡Ç×<¾\x0007\x001b>%_Ï%?¦Y_Ò4jywó't¯f;òç¢\x0007W[J4ïÈ\x0014õât*{BÑÉc°\x000c0\x001f&8¨n¾Îsµ&8g&\x001a_\x0008½Î\x0010\x001bP\x0005Ð\x0007+QoãÊäúÆ\x0017B¯3ÔBÐY	)zI°×³tË6ÝnÆ\x001bB¯;ÔF¶#PÙ`\x001b\x000cMM\x00025î\x0010zýa<\x0017¸\x0004<èæaÎ\x0008Hëåv \x001dI/¢iÜ\x000fôú\x001f\x001bO\x000bA4¸õI(Fï¥íì÷jü\x000ft; Ùúiü\x000fô: \x0019l\x001cìu@1Î¡
)Üîtºc*¿ôÏ²	
eolø¯³O\x001b\x001böúÃ¸µó4J4 '\x0011\x0019b Y Æ!ÊßÝ!ÊÆ!Ê^Ê-i\x0005å·½´ã=ÛG.¯CÝ<?½þÐã²\x00048$½¶è\x0007'ªlâCÙ\x001b b+Ø¼Te\x0007í ¼xJXêu\x00035.QöºD\x0017dè`!>P-\x0004K\x0011þìûÏiÒe\x0015áßè[Ø\x0016\x001eÑFÓ²ÔÎJNØJ³|\x0003\x0018 j\x001e¯Ó÷S©R¡5T×a±è×YcÙ%íÇJ\x0003L)\x000cq¸\x001a¸êå®dHÿ-q¥\x0007°â½¥³r°ÃÙøÏ\x000fZ,â\x0011-69o#ÓíÕåÇD1Î­%¥\x0013TÚè¤r®KÿýôMzsr¼k\\x001d"¸åÃ óqu\x000eôÁw\x0017\x001f÷ôha¡¼f\x0011;ÖXqñ\x001fæ<¶R\x000b\x001fõôè\x0015þ§\x001e½x½[Õ¤`É\x001aKöcy¡Qÿ;W£ò\x0008S\x0007Úó¼£C3¥j,5`­ KÙ]\x000c¹MñWüj²Ì¨\x000fQéJ\x0018KQ55~ÂÜ²\x0014må6:~\x0005©©Ì\x0000UQX¨1\x001eÌ\x001eð­ãGKíÖ\x0018ËÖXv\x0000\x000b4¿Äû\x0011¿ÒåN\x0015-©È!,Wc¹\x0001,\x0005¨A­¥1kÑ¹iTkµÆZ¾Æò#K\x000b{@,MkKó#¯Xf)°B\x0015F¬å9Á\x0016ÁÖ
¼¶äòA|\x0004«J 8_\x0012(]þÁ»ÜÉÂÂ:\x001c'q,_Çj}ü÷Æ\x0015¥Rà\x0019^N*Ø°bqAãMaÀ¢P¸Ö~çÖ\x0007Óÿ8ýnW\x001c>Ðx.\x0018q]ñx¦w\x0015kùý9./(â¿+¨\x001a\x000f\x0001#.\x0002ó=²´\x0010	Ú¦tS5sM¹½\x0008\x0003Ñ\x0005Ä_q£>«¸ÞX-ÃÒ±C±\x0001ÓÁÈ1`ß)\x0014P«ûIø\x0014\x0017\x000fv`Ë7>:±,t\x0010¡Ò@||~sóËÞLô°ôàãÃ³³?Ý\x000f$k Ù	·SîðpEÝ²°ôÒvó¨G}\x0005\x0006Ò5î5\x0010X®±N\x001ba5VnYÜ×\x000fdj Ók!»ÙsñâL\x000fNz~z
°ôÝ@¶\x0006²½@Áq¶µêrN°Ë\f\x0016úy\Íã¾%äk ß\x000b£PuùbÔ7äT(\x001d¹0
\x0014j Ð	ãCÂfN\x0006ðû-W¬Ù\x0015TÅO&º×´ÍsòÐB\x001bFbm'\x000c3KÔ¸EèõÚhn\x0010ÝÜ\x0015¢ä+\x000cÆê³Dc^Ï¨âu=P{ÑGí<\x001e ýDg^×¨s*:Ç\x000b	K©;÷n Æ3B¯k\x000b¸T6b\x000bçgp¾\x001b¨åp~¢Æ5B·oÒ\x0017)aA\x000fu;Ð5,kú\x001aç\x0008½ÞQYà§C§
\x0017upHtç!¼\x001f§qÐë\x001b±°Cn&)p®\x000eç¢óªÞùonçhþ?uïeÇqd\x000bN%'ÐXþ~,|%$¼@\x0002\x0000¸ºî\x000fW\x0012LQÙ\x0002\x0013R\x0002P·êKÓ¨\x0011tÕ88\x001aI»EY¸Ç9q2Ì#(±õq jQ\x001eîöÜ¶-\x0011\x0003\x00156XÔ³È\r½_Ì4ÆÑ¬5\x0016ÛÃ\x0011\x0005Ò¶\x0008TûuÖ\x001cj\x000f¯\x0004ÔÄ°fm\x0010k]¦ñ¾\x0008{èÆ[ä.à\·m4m\x0010»ÖZÛÈLÍâVà%2Ë`\x0007É÷j@±6«5,~®µKxDGês÷\x00115ÆÚ¬5Ö¶üïZ´ÅÛjBD¾ó©û\x001akmV[ëjãð\x0014ìSÑ8ÈLÍ\x0003ç»\x0003kÓ\x0018k³ÖX[§Ù\x0016P\x001fù¾>²C\x000b¾û¥5ÆÚ¬6ÖÖâÅpDLR¡#êõ°¦1fµqüÍ¾n\x001bQ£åtÿ_y»Í\x000fýzSw\x0014GËs¥ÓU$L\x0008\x0005qGdJ"è9×ý\x001dÍüØ\x0011\x001c[9«\x0014¹ôú\x000eAf¢³¹;3±s`v=.\x00172W%@ã\x0000s\;U\x0007ç#\x0016kOdæLa30Ïÿv{å¤G\x0014
cråfQÁ©T£Xæª^sþýÅ\x0015\x0016PÚpù¼Ì5l\x0006Ö°\x0000Îã¼¤+ùgº¥ò"ò&h¶fEÐ"³K
7Ñ\x000eH*Ôµ\x000ed®FæDÈ,­fW È1â)Ì¡^WÕ\x0001Í×Ð¼ìªq
:kË£Ödö}³\x0010½\x0003Z¨¡\x0005\x00114Ö-§æ©\x0010
[\x0004ñÔü¶GjdIú>-ªz\x0017(¦Æ3}Om6\x001dZUÙ0#µVÍá)H²RÉ\x000e°á#¨ì;5CËLGÄY@ÐBwXY{4\x001d%°5\x000fTË^hTO\x001c$¬äb;h\x0002¡Df^¨n½\x0010I\x0018³xÎj\x0001 asyÉÕÍCÐ²\x0010,Múgï\x0004t\x0007å¯\x0011Õ\x001e©i¾©}ÓqÔf¼o¿)¯+\x000cºV\x0001É?üX£ËO\x0014 ó%±uôNY"/YªÖ\x001cN¢[=h£òô7êØãëÙ_ÿûþ×ÿ~¸ù\x0008Ke^Ü|ýøñ\x0004oN1\x0015\x000c\x00166a\x001cR>
UÛu8bMÞ½¸¸º¸>	+f^¿ùò\x0014ÙÉÐæå
°é\x0006\x000czÈ\x0015Í¼µS2\x0006\x0002Þ	®­áÚ^¸!\x001aâù\x0004­'ª-%¶Y²	°«\x0001»îó\x0005õ>¬T+jPEh£±Õþ)ê\x0002ìkÀ¾û½£Ú\x0008ìÕÂ_\x000eD,±&\x001c	
»\x0000\x001apè>a L2¢\x0014_\x0007ªwY}Ìw\x00015àØ\x000b\x001855\x0007òì^2\x0014ÛZçWðij´©ûxIÛñ>¨'!a$Îë\x0003Ùëxs
8w\x001foyfH{ý}:\x0008^#f\x000fÜ:ä\x000cMÈ)5iMZ9k5_¾n­9âÖº\x0010·>®ÛÉ
C\x000e8\x000b©k\x0012i/©·ÞídÒtããt·s@	Å+\x0011=\x0016 K^Î¬¡¸\x0017àÆËén77(k!\x0017Ò+\x0014À-GL#7Öï\x0015FèÆÍén?÷Ï;âÆÍén?ç'iJXÍME¬8Ýâ´¡hüîvt0Ïâq\x001bCµ÷Éz»×\x00197Nw{:hÓ\x0013\x0019&\x0004*ÙÇi1g8VëBÜ8;Ýíí¼ææYð¬r<]p$§íÂÛø:Ýíì\x001chúÓ¤{dvfï\x001cÕNwÂ4îÎt»;xwtÂÁàª;xwdÚÂ^ñ¥iÜéÏé´"bã¼Qñl5n§[aÚ®ßßÁ®\x0014º\x0015,E\x000cÏ8í%ÆánWîÅÔRPDè	\x0015\x001bÒ^yi\x001céwx%q\x000eÓËCµè2¿<½\x0017âÆãngó´ó!McéÎ°¬j-2»	qãñL·Ç\x0003â\x0019q¡UÁÄ32ÇÑ\x001d©v!n<éöx6¦±\x0002dÂ\\x0007fÊíf\x001bgº\x001d+^ôô'[ÃäÐ7âd&j\x001bCl»
±5Ì³°q\x0008KxÚ+(¶\x001d¶¿ÿ¼Ã¶Õµn3lµ§5m?àyº×ù66ØöÛ`ëI~\x0013¼\x0006q¯ò4àp¬«Ô¸±Á¶Û\x0006\x0003)\x0007k<m\x0008eRf3±	ocm¿\x0005¶\x001aTMÉ>`"\x001aX\x001fÌ&»Sìc\x001b\x000bl»-ð?/Z³	¶ý&\x0018\x000cé-«g¥Ê\x0008ï%¹&wÝ1¼Ó)!M\x000cõà&öÞk,±ë·Äç±\x000c}«e÷ª\x0011»¶mÐmÚlN\È,u\x0000:°Ì¹ß	pc)\·¥°°mOó<\x0017¨\x000cáó^õ\x0014å\x001bîÒÐì¿ÑfÍ5
^ö]n5/\x001bØ¯`ìæ¸µÛ\x0002\x001cj¯xC@\x000c6É:n#ìuEfZC´\x001f÷?Ï@ë¢·Ü\x0014Èª\x0013Þp§¹Ö\x0012\x0002\x001fø^áÜ74L7à\x0006\x0005Ò©lÑ¤HI÷+\x000f|!Ê\x000fsö^°m\x0007ýÍÃíç»`Ûýÿº½¿¿ýiZhl¢\x001591ð\x0016wçIZÎùx4Bzs}ñöòùÅÕ»³ÿuquuñü\x0014\x00032Ì\x0019}Á¶ýs\x0001\(É"Z\x0003fd@;ñÈýqÏÝÖÖhm\x001fZXHpØâ1 µ\x001cË¹p\x001eÖÖÕh]çÙä	I¹08\x001aGO:j\x000fÑ¾µ¾ê;¡ªL\x001a\x0011°>Z£.ïDqé¸ïë8ÙPÃ
½'(Ë\x000b÷\x0003L<zu´pÕ\x00016Ö`cï¥5è³¡\x001cÏòÈ¿o.6ÁM5ÜÔ{¶ú	N\x0003ÅLÍ\G[ªËáæ½\x000e7×hsçáb\x0005\x0013ä´qó©
ÔOòÚît²U«<ØY«\æ\x001bx\x0003ÅÆ¾ó\x0008Û£\x000e¸­'ëteÚ;*· \x000cê@Ãñò;óúx²ß·qeº×\x0019V-Å\x0013DËi%\x001eÏé:à6ÞA÷º\x0007«©Ç\x0001:\x0017´LÏñàÝ^&W7fA÷ÚäÓ&DÅke½l÷r\x0011mÔ;xµ6x\x0014Üá\x001c¦ý6\x000eÙæÌ¼R'lççñ®Ä\x0017óZ\x00101DvÓ\x001cA¦ã%øÕí/jC­ëvþáæÃÝÍ2\x0015ÚÊ\x00117ºéLyrÉ(h\x001c¤yg¤{rþìüÙåù)­³Bm¨uÝ\x001eUü\x0006\x0003,KÊ:CK\x0012a¹#?«aÙ\x001a\x0015ÀrjPN/¨`C\x001ar£\x001cíÏé@,BÊÕ¨\x0000UT<Òã#Í\x0016³^¾\x0004'[\x000eË×°¼\x0000Æø¾À²È\x000bYûi]à|BR\x0002+Ô°äÆÛqB\x001aâ
]ìI\x0005/\x001dlá\x0013¡5ª¸\x001eÏy\x001cãÃÊ,­u Ã:&qµ\x001aVªa%ÁaY?¶<á°25\x00103k6%c\x0008¨­kXYpZ o1N\x0006hçiÇs
ü\x0011ª5­UÅ64ºn_ùÄ/1ò\x0016Ù¬©\x0012]\x0002Û°\x0001Wkä\x0005VÞûLvËó¬Äv+©-w^7F^K¬¼Â?È«\x00140.ÆKO
\x0013é¨"åj\×\x00023\x000fh\x0013Ù \x0006</ê$m¶|ÅÆÌk÷ÉÑdN\x0019w\H6mxº±óZ`è½U4§£ËÃÄnF\x001aVz¸ô\x0016\¡×\x0002KïAN\x0014¯}4(\x001b\x00187¯Ñop×º1õZbëËÿºÆóJ6z$CÒ¢%?;"³¸\x001aWcëµÀØ{\x0018ð\x001e£Ñ%)@\Ì­Oá@ßM«1öZbíKÔ1ªQ4?\x0017\x0012ó6ßË4ÖÞH¬½#wpÜ\x0005\x0016prç)
\x0001i¬½Xûq²güG\x000eØLù²*\x0011¬6¤X{ ³f<.¢Èà\x001c#\x001d×\x0004WcíÈÚç±\x0019;\x0016\x001d2	R\+q\x00172¹7°\x001eVôi~b/ÄH\x0007k£D¸\x001asoDæÞP\o¦6QFÒ|ÿ\x0008Vcí(®Ço¨\x0018=­Oa\x000b2©7\x0012So\x0014T pÓp
F\x0012ÃÎ~X¥7°\x001eæ\x0016-ZTO½Ãhv5ùùÎ\x001b\x0011®ÆÒ\x001b¥\x000fj\P	Çew[\x0005ª9oð¶±ôVbéS\x001eU"á¼Ô´#H³\x0007:Õàj,½Xú\x0014ÇÍrc¥\x001f\x000b\x0012å\x0001RãHÕ6¦Þ
L=D^\x0006#/X&7c$sLx5®¶|#©ß¨<ÖìÇÅ¼7feø¼¶Dö¶1©VR*)\x0011tpS$¦ÞÐØsqA[î}c¾¬À|rH\x0011ï\x0017hÿZ,xEv[Ìªmì\x0015Ø@Û×\x0001#	ÐLË(R<¦¼½\x0016k£\x0014SËst\x0014¨2é¨Ät½ü>¡\x0004WsíàÚæÂHBÑs G¸æ\x000b×d	GS.\x001fZ{{M^«ñöX)\x0006`\x0016V¥¤·TsÂ\x0001¼ \x0007%\x0013J×X3YËéZÞ`üu<\x0017eðt¤· ³~B\x0012Ï\x0014ø¸>Ô¬­\x0014µ\x0015Þ=ÜÜÿõëÝ)\x000f4j<Î<3½\x0011juHñQsçw×çWÿöþò4\x001b	1\x001aY	\x0002\x001dÜz\x0013ïÖ<Ãªæ\x0005V	&[c²ëÏi\x001c|\x0019\x000fÊP%À&\x0016\x000eÖj\x0003(Wrë\x000fJ³þ\x001cøñ@-+\x0012\x00040Á,búpóÓÍç/\x000fË|É¯?¨À£ÞF¦]\x0004^\x0019éç)$\x0007\x0015jPa=¨¨\x001d\x0016¦M±6PÒaMý b
*®\x0007å#Q=T£Ç{>\x000cÁ'eç3ÉçK5¨$x{Å\x001eàçf>vÇ5uóMPÉIå\x001aT\x0016b-\x0014¹<è\x0014+­«yJ\x0000ªê!åT¿K¥[{.0è%1CÍ\XzGïÏS-B§ùo	ªÆ¢kI\x0007Á»q\x0002ËM\x000bø¡6PÉ=B÷]×M×\x0002£þ~ÁÆ¨ëõV]gGâ\x000eByrÉxRnÞ\x0001TcÔõz«þÛ¾ÀÆj\x0005ÍÔüK¼NÕÃ\x0002\x0018DåúA5¶J¯7V:F¤öBÕ\x0019\x0007µl¤Ú\x001el\x00122U0\x0002«\x0010õæòW(\x001dd#céùîD	ªæýßÉûSm²3xAÖÿÕØ´cÓF\x0002î7}³©!\x0010\x001d§=-¡¤Ö#\x000cìæÛ\x001aDò\x001c\x0013aC\x0019\x0014\x001f\x00125¬#áI\x0013ç9\x0005lÓ¥ý,ù\x0002\x000b[)'}üüçÅ×O91\x0002Ë³|J©È5$-òg/Ï.Þ_¿~sêÐ\x0010©á\x0019!¼`\x0002/(Ñ.Ùdí=6É)gkxVzzu\x0008a¶\x001b\x0007?\x0012\x000bþº&íçjxNzzÊO;yÐ\x0015³cª Iàù\x001a\x0017¢\x0005ÛÑ±\x0012}rT\x001e\x001bÀ\x000b5¼ ÇlÅ~@é	ûÜ¼â\x0018T\x0002/Öð¢\x00147P\x0001\x001eO/£Ä]HWøc*»\x0002t©FÄè\x0014m'jâ¢õ¬êL£S\x0002/×ð²\x0014^\x0001ðeø0QwxÉ­×Û¾mØUV\x001dø'^®!IiKCÚv|ºõ\x001ab·a¦å\x0003 \x0011Z=×µc\x001a\x001c\x0012|ÛÐR¿\x0001Õ\x001f²|0-ÅØ\x0012³\x0013>³ñû6~CK\x001d+¾\x001eoJ,\x0017yyCR\x001b¿oã8´Ôs@µ\x0018ýZ¢=½° K\x001b?ocµÔ4»Ìr\Àð\x000f4ÔÊ{ËM}Hà5¶OK\x001f¨,\x0011ºL\x0001rtüxó1!+	¼Æöi©ñs%	CÄÒñ!\x0004ëi8í"õzx¦±}FjûMX/ï"å\x0003
x©cÃ´\x0012xé3RÓW\x0002ø'4fiñbpNÓÚ\x0008¯
¥ÏAkÌðÇEËW¾Ä\x001fwã×m,Z>\x000b\x0002S8ujÜ´f
½ÖÛLi,Z>ØôèûjêýÈ\x0006àTÞø}ÙHfÐêò||$9gH\Ìëi,³\x0011[f¨µN\x0017\x0003r~y/|MÐl¤Q3¬sÌÓóÅÛ§õôz·%l¦ñ\x001cFì9Tâã³\x0006\x0006PÆã£tÜëG^ïÉRm\x000c³\x001af\x000b¹q®ÎðF<7Ý1QxÁÙÙÆòY©å³É×µµg\x001cSBð\x001aÃb¥ÅÆ@R3	¶R¢×å\x000f·=Û¼[+}·6\x0018RYH%vV´ÅªÙÞ­n­)®­\x001e\÷>`ä\x001bm=V<ü­6¦\x001dÆ\x001e ´rp\x0013#Û@Mr¿µÞX\x0015sQ\x000erV?ù ~°-NP\x0007GÙq\x001e¼\x001d,&Ça\x001e\x0017y\x000b§Ù\x0018\x000cª0G\x0019z2aÞ1¿Òq­£Û©Ä9¿&ªzl÷Íí×¿|¼»}X¢ý`\x000b>\x0007®V\x0012u3\x000e}ÀëØì÷o^^^\¢þÄ9¥%ªzFv
4\x0003ëp\x0006hÑ£¹WDÿm´G\x0008S\x0002h¾æEÐpS S_²ÖHÐ6\x00015°(\x0002\x0006jNq\x0004æ=j]ú\x0012\x0014y\x0004¦æ!!´\CË2h4­£9\x0004\x000f[kGhþ`
´\x0008nßè\x0011ã©%¼#	V_R%CÐñ²\x0005ØG E¯@Yá\x0003\x0005q0bóhOÇÆJ\x0004ØW EÏ@\x001bDU­´Á\x0012³	\x001dÄ\x0016\x000eVyÊ°5\x000fA^6\x0001¹öº\x0018!¶\x001e\x0001§½
6½íÜ EOAÐ\x001a\x0019´«Í\x0008,"\x0007-øíì"\¦y\x0007Fö\x000e\x001fWÿ\x0016h%\x001a
ø\x000eÈªy\x001bÐÇ\x0005Ðg`dÏ d;qdÏæ ª]N-õ0Ç¸Ú\x0002lÍ30²g\x0000#½=»øDã±%Æ¦Õ&Ó6Ó>\x0019UMí]cD\x0014ÛÞdq\x001fZ1p¨ÚS¼ü1i\x0007\x0001BýÃM\x001bÜ\x0008ÖÈ+×ð\x0006Ñ\x0019\x0002çM\x0007¬\x0001gô,:Çñôé³?Ýþrw\x000f\x0002,ß>Ü~þë×ÛËù7ÔãË0û{\x001d4é)::zöWW »òíõÅÛ{ñòql¦ÆfDØ`«\x0007\x00122¬H¥\x001e#l¦Ð{ÀÙ\x001a\x0015Au\x0014W\x0000:rÃ¬@"âQõ6p®\x0006çd'ç\x000cµå3QwhÀÁÖ6¸\x0007¯Áy\x00198\x001bI\x0010¬ü4	rtvã\x000b5¸ \x0003\x0017íH<\x001awi"©;qý)Ä´ñÎÅ\x001a\=Ö\x000câOméà¢#ÕÐlÛèÁjlIxpFì\x0014\x0010ã1æÉÒÔÆ+kpù÷õXë­rzèvK\x000e6xÒÑeK)ówÝxçtë d\x001e\x0002\x0004ïa1'Ú,im|LnÛ­ÓÐ2\x001f\x0011KöpªÇ*,ÛENº
º¼íÚéÆGhA·4éï`3\x0000Ì\x001eëïämè\x001a'¡^"NÛÚµfÝ\x000f`\x0006à½Ûú*\x001a/¡en\x0002vò&Ò
XSjR³h¸[=è\x001aK¬e¦8v,iÌXLr
dOÓý6n´Å3\x0015l1ñïÄêåyà©,÷âöÓÃÏ%,~öñ×ÿþåöþÃíÍ×\x0013qJ\x0002êÑP(.fÆã
´Z\x0016!Î"ã\x0017\x0017¯¯_èøÙËW\x0017WÏ.Îß?ÒÔ(\x001c¥K\x001b\x001791\x0019¥Ð|\x0013\x0013ô¢´5JÛq!ÓÎ\x000f8K\x001cÜK\x0018I>Ì+c=(]Òu 4¶f$pBÒbrCÔ; ô5J/G\x001cï«NååY\x0011l\x0000¢&óLF\x000fÊP£\x000c=¯gúâÙÐ4|"Fµsy¤\x001e±\x0006\x0019¯O<Õ(SÏã	4·\x0005GéxI§ã³4QÖAbæY7\x0011LÁÊ\x000cÓ¦²Ù.\7öRw\x0018L\x0018f¶Õib@K»"ý(i\x000fÊÆ\x0012é\x000eS\x0004{Ò£\x000e\x0013Å]´\x000e3lÙ<rÝñÊ5LØÈ¼O¶ûÂl\x001eîxAÁ3a\x0017`¢û!\x0014¹Ý°æ\x0005\x0017\x0004{ÑúWó1æÊMþg®¸Ò\x0003³8:^P\x0006\x0012Á\x001cº\x0003Ìh'g®·ÃléxB MÎÜbÎ\x001fµ{ÚvÓ¼ ÓñUÄ\x0018Ë
m{	3Ýñ\x0001æ\x0001\x0007\x001cóÚ2u\x000f£\x000bQÎ%ºÌ6©ÈHI\x0010û¡#\x0008±&éÊ¦ézî\x0010\x0011×5÷!¿¸é>\x0014+¡w\x0014¹\x0010J8ýCq\x0005\x0008»fÓ~>{ó÷Ûû_ÿûvYÄZCGYN
;\x0017ÐXÄ$Í¤£3@oÏÞüûõÅÕÅÅÉÞEå?0\x000e(ÄgJÆ³ãPUÆÙÕ\x0002K¢D<FÔà³5>+=?3)^TÕ\x0008ÏS¬aB]LîçjxN||¶Oyí)F÷ñÙ£c@\x0012|¾Æç¥Ç\x0007bö?/]?\x000e|Ëç=FÕà\x000b5¾ >¿0và\x000b>ÅTý\x0002ÎO\x001ftà5¾(>?ì(\x0017|F#%´ä<t|öØ>\x000b\x0011¼TÃKâã#×ç#J¨×\x000coóãÈ5º,=<Æ"\x001a|\bñ\x0004Î\x001cÛh$AW%\`ôðàÈPË#Q\x0013ÍkÛÒyëééÖs]G1}8\x001bì`\x000b4Ú\x0016\x000e¹ÍQÖ\x0004_ã9´ØuÄÈR\x001a·T{ET}
úÛ\x00006®Cwø\x0011]T*¤ZòQB²\x0004]ã9´ØuD=6^
@Ë\x000e<>ºIM¯ñ\x001cZê:À4cÌ\x0015¨ìÚ\x0002\x0001ÌÇ6;\x00006®C}Gpd^\x001cH<ç¨Ï¬ßú\x001b×¡¥¾\x00033.°r\x001cû/Ã)|\x001fGÇä$\x0000\x001bó¬åö9>¡\x000bq®ÞøuMcýÔúAKÃPO&\x000f\x001fe\x0004è·~^ÓX\x0017#µ.&zâÃL\x0015\x0003$ó¬½Ý\x001aZµéÜ\x0010=7Üíµ^Äf\x000e #GÐ#èç¨Ì\x001c¦Ãü'ä!z\x000eSwæoÎ¹9ÛËijº}w{s_0þÏ?þóüáÃÉh?Ò\x0000S"=Xï¹È ç¥ï.Î¯®
Â³óëgC354#h®/ÐÔkÆ{÷ì\x0016d¶FfeÈ\x000cîöÉ ^n\x000be#\x000cË®Ê ù\x001aÿ=\x001dZ¬Åß\x0013²\#Ë2dv¿uêé>pÛÌê-o@·ÏSø>­¢%ù@ú>\x00104§NÚÂè£óXfþj\å\x0006JP(Óà.7ße ;³æ	há\x001b°ÓÆh©ÙT°Ñ¡\x001dðÍeW­õ
É¥éj\x0003b¸o-ñ»ÊEã­óÝ+\x0011Úùp­£Î^~ºÿùÃn~ùË²·J%ÀsÈvLv\-
õ{\x0004\x0016çby0³õúêÅ³?¿zsR²y®@lÕ´Õp\x00150çh\x0007ÊÄç\x0006¼ad\x0007rÍ"h¶fEÐ\x000ci\x00024e¨´ÐÂ
·\x0008«¡9\x0011´ò\x0014p\x00136¤'\x00155»c:\$ækh^öA3m|S Ñ§Æ+I\x000f\x001a×Bd¡F\x0016dßÓÐv"\x0005\x001dADÆôF¯\x000f&\x0007DÈb,Mû*U±º£ z4D^¢=\\x000c)khY\x0004-$Ú×¢R¦÷i\x000c¿O?çKÈ éÖ¦ÉZð¼-O\x0011û \x001aÙòHÎ\x0016héÐ2Û\x0011í}ãºV\x001bH\x000b4b\Æx8$ÂÖ<P-{¡Þ>	È·´v·\x0018Eº.1\x001fn\x0017\x0010ak\x001e½\x0004ëFª\x0006\x00186\x001a\x0019(MñBÙÃÙJ\x0011¶æ%hÙS(ùs@£\x000bë[ÑÄë[Í&/j§`dOAã\x0007\x0005!\x001cô\x0006A\x0011°t8v$\x0002Ö<\x0004#{\x0008Z\x0003\x001fu|£®gO\x0015\x000e\x0017+°5\x000fÁ\x001eBÌ\x001eU£m3X·Úò#usîÅZlÊÎÂ"0éåôñæÃíÙùÃÍÏË\x001fu]A\x0014*¢.µuÖ½7/Ï]ØñüÅëÇÑØ\x001a]F!ë\x001e²»\x0008×@£éjy]óÚEp\
Ç­£¡Ä\x0011ýÀ\x0003\x001cã&½	w\x001cÎBÊX|ÅÿË&ÔpÂÚ£	$¤\x000c5	àÆ°\x001cï9TCIk¡8j\x000e*Ê&\x001b
½Q=_©jòÁ]VkÁ \x0001*BÚã\x00194oÜÂW:}.­@òpáo¬C(º8\x0006¢«ñx\x0002ën¥(Ì,;,ÿÈFëíûÛ¾Þ¨_ëQj\x0001ôQ\x001cñ#]¦M0Î\x001eWñûþâúùû«\x0013×\x0019\x001a\x0011\x0000³nºÓ0÷;¦ÓÉ$ÊºàZ\¶Æe%\x0007\x0012õ;cÈÌUÐ57õQMËµÀ\
ÌI\x000eL1G&\x0006Cb¯Þ¶óþ¨>ËZ`¾\x0006æ%'\x001dÆ\x0018¸2bÈXºp\Ýf-°P\x0003\x000b\x0013\x0003þI~\x0016ë]N±úlØt`±Æ\x0015E\x0007fÇ\x0004\x0002tI-D{Mêr®Ùèv\x0000ì´¥H5ª$:-Ï÷+:î\x0004;Zlí\x001a½\x0018ùqå\x001aX\x0016\x0001äÉ3	¶y^ÔìÒquò¸êÝ5f&qü\x00180ãhÞ\x0000ôe\x001d\x000f\x0002ëËn1aºµù\x0012£oAò\x0011C)ÅÌÎ\x000fæòÉ\x000bö(²ÆèkÕ/É\x0015çÀÀ\x0002q]:.÷½\x0016XcõµÄì[\x0013èö'mÈVx\x0016|TGiB«5V_Ì¾ÏL~\x00059c´#X~\x0013¬ÆækÑ\x0016)WÉK=5`X	Pm»üÑ×"«_L½ÆV\x0002\x00102PyW±ô©=* ¸\x0016XcõµÄì[PóÎÜ·E`>NQ¼Ûô1\x001b\x0003«E\x0016Ö9Ò\x000f8ú|¼>Ãã*z+Æ\x0019%s\x*IAO¢\x001dÉÞ\x001e\x0017¥[¬1\x0018Fd0JüJ\x001d+¯Hû|
`±Ýò\x0000Ló4èiÿ}çø\x0001àBJÏ{¸½=¾ñaµ-«\x0018ý£5»ùÝý³½;fÎþø\x0017§Kåì~Ý¿³íf\x001d­èð¬
<\x0005{+Ñ»óµ1Û^Ä\x001cñB|.\x0011Ù¬Ä\x0019$\x000bã\x0013q½ÛÚ\x0003ÂË\x0007[ëhUf|S"å:3¼8\x001fôÃ ÿå/¹ùüùöìíÍÝý³7E\x0008 \x0008AzYæ\x0002=K`¸`*×uùêÍùÛ·\x0017goÏ/¯Þ½y}J Î'Òã0.¦0\x0008T¹\x0007h\x0014ëÄj\x0013´PC\x000b2haì¯Ð:Í;\x0000
´Ü\x0007M§Ù\x0007ÑÏ±<þíÃÍý¯ÿï§»Ïgßß}üøéÔk0D¡É°Û\x0006CÞÈ
NvÎîùöúüêÙëË·gß_¾|ùúÔC|¦Æg¤øÊ%Âç¹\x001f´gá°ä6â³5>+Å\x0017p¨\x0015(_\x000e,XE±\x0011«ñ91>c\x0019ï%GÖ8Ïù*bx¾ç;àá6è\\x0012Da:GÃy¾NQ/Ôøøú%Ê¡3+×ôF³úÚ|Õ\x0018_¬ñE1¾LÅ\x000c|$Gc\x0019Aå°\x0011^ªá%1<ÍrXJ\x00136ð\x0006ò\x0010çj2|%!WÍõ?\x000b!BfÊj\x0010CÏA/$ÍõtÅGØ£&Ú\x0000fB7<ëvù4\x001fÎ\x001bÁ9FÛñ··~\x000eÓ÷Á4d\x0013\x001d\x0005XÙ\x0011AÍiBëaæ¹KÎ©Vñ¼=ûxsöêÓ×w÷\x0010=,BL!r^ãÙq]_,3í¾m\x0014dIîéâìåùÙ«×ï_^^A\x000cñ8L_ÃôryZ´\x0000;Î\x0011¦uTd±Êm\x0019Ý<bupc\x000bî§¯g×¾~þ|úcÃñ¡\x0005(T*Z\x001bI{\x0019[Ê±\x0015÷üýÙõë÷oß>ö±\x0011­áY)<3Úo0ÖFfEsC!Öþ¯\x000b¯áy!<TXV[ñÙÐAá )Ä\x0016klQ
\x0007 \x0000^IðË\x001aV©lF\x0012»àå\x001a^\x0016Â+ip\x000c\x0008ÏP[ Cå\x0000áÙ´
nßôaL\k0ÖðQ\x000ek¢6âk\x001e¾\x000cÃ2N =®P«\x0012ö( >×Ï])7\x0005\x0013§77_?=ûxóõ§²·È¯M¾ÂD:X®Y\x001e\x0004\x000eäÍùûgÏ^¿~R\x000fq\x001a\x0011àÑHÚò
\x001e\x0004£ýh¨6Ô((ÈÙ\x001a\x001cáK\x0004YTÔîPOlÅÉ¹\x001a\x0013\x0000j|Ê¬!DSõ|b²72`¾\x0006æE'¦¹\x000f;­;S­å`RI\x0006,ÔÀäÄJFDÀ\x0012S\x0002Ó]ïx\x00015°(91\x001dV\x0017
ËsÄLÁ3v\x0013°T\x0003K\x0013\x000bfF
\x001aä'pp%»éå\x001aW\x0016\x001d\x0018K»Eø¥ÀûæÄM\x0011°ª¥\x000eæUINÌO%Ð\x001a1}Ê4×¿!k
¿Èò+Å;Ü-iÅ\x0018y=Ò\x0001_¬±°Zbb]	À1\x00166cë:z^.oç{~dÀ\x001aC¦%Ì¦.\x0002s\x0006\x001bÑÛ©²ÅéÆ^hÁ\x0000	vâx9ÇßÒ1qÃÍõãdÈ©%/ÓEÏ÷\x001fº=´t{<\x0007[&DÈLsÿäþ»b(,}LÅ«õ×|Í¶\x0000k®¿\x0011]Ã»0a	ú\x0004ªì^m¹f¦¹ÿFrÿ-|L,ÿ\x001b^rZmïö[,iî¿Ü\x001b\x001déE\x0015£O\x0011vÐ4íP<ù¦[ÖÜ#¹ÿ`ÿ17\x0001j\x001cé¹d²tÑmAfûo%÷ß:ÖùãÚslÐ¥-&c¶±q|\x0003TßZ÷\x000c\x0014ó\x0011¢KÄ[\x0005ª\x0004Y\x000e»Å
\x0014_n\x001ff\x0000áï¬?À<yñ+\x000f\x0000!×îRk\x000fó.©Vôo_o¾|zøÛ³ï¾¬óöËòù\x0005Ã\x001b§Y.\x001aæ3ÙCý¿½?÷úú_}÷¾ä\x0017ï&sl¶Æf'ØÒ0\x001aí+Â¨~ê1¼}÷pó·ÛÏw¿þ×Ãr\x00110/jiµ\x000f\x0015\x0012¢ÕÜØ"\x000fM½»>ÿþâúíåÅõ©â\x001f\x0002Ë
°,\x0000\x0016­zÃ\x0012\x0010yÄU(âïT[\x0007+ÎïY\x000c\x0015\x0015l\x0007_ü?_ÿrûð÷Edº¸ñÄBâÇ¦Wñ\x0013hD¬;¢26/þÏ÷o.®ÿýq|¦Æg¤øJÐIùD\x0013wÈ2gÚDsÈ\x0004\x0013\x0002´5@ûû;ÀPã\x000bB|Ã¨Îx!Gªw8CiÍ\x001c\x0018!¾TãKR|\x001358Bí\x0014'Ð¸\x0005ØF|¹ÆÅç7U?\x0014\x0017'¦â)ø\x0000kAÁP3¾×``\x0018°°h9ÌêÈ¸\x0010asZzýØ\x000c¦Q\x0007IÃº¸G\x0000.\x0018Ðùµ\x0012KÃ\x0019VD§µÇh`\x0008
-\x0006\x001c²6ów>$ÃJ-á\x001c§ÃIeÔÕ
\x0006\x0001­¦äÚ4ÎBjîPT¨iY Uõìæ/w_nKppJþ#Ë8\x001cóè²h\x0012C®¨Ä2\x0002µªgço.ß]èàä¸ëÜ«¨Á«AºÁlÃ¢D\x000b´£ä14\x000bz1Ú\x001a£c,\x000f[a[	F­#jh>È\x001d0º\x001a£ëÀH°¡2óÄÎ\x0005oSLá\x0008¥L
Ò× ½\x001c¤ãEÅ_óÌü±Ó\x000e\x00172Ô\x0018C\x0007FËóáJ£TÁÈk³¢sÛAÆ\x001adÝO( £2mÏ2J\x001b\x0006úf©\x0006:@\x0006uPãâÈXàå£1\x001eá®\x0006éçL\x0000ï¨c÷
ÜÔÇw÷gç\x001f¼}XÎ`³=ò>vOp/\x000cHü\x0010§b\x0010¼:¿~V]^¿üæâúÝãøLÏHñ¹a§Î\x000f!*ñ[º­Ógä\x0000m
Ð\x0001æ'i\x001a=¬/!Tü°@¡Ù\x0008ÐÕ\x0000\x0014 xôÓ¸µRSÑÈ¤Í§çkp^|z\x0006d! íI5²[\x0001\x001a`ø=^ÃÔÓSÄÔ\x0013¼_M@®È\x0001¯\x001fÕ¶¬\x000bO\x001d`üpóÓÍç/\x000f'0þðÇ\x0003ÂôÄ÷\x000e@ÉÄWâ¨AjÝQ-9Êù\x001a<?¬ÁûæÓ×·»yø	¸[oîîOúl%\x0018#&!¡÷¡òÊß¼~ÿòâûóëç@ÚzsyuÒBÏ)ü~ ð\x000bZñ\x001dÐB
- I\x0008$û'eCyoS]ÃïjhI\x0002
q\x001a(ÈuÜç\x001e\&1 Ì&hu\x0017w\t&À6}£Ô$Ï\x00168Ã3®N:°5Ï@ÞQL\x0001%/Gª!±Õ³,\x001dØ E/A§@É\x0014

³0sÌûÚQ\x001cB[HÛý|\x001fIÎ¦CYùÒ)æ ºÐc9ÚÞGF½\x0015Á+Mxl0V61M¯ôä¹=þ\x0014æ\x0008±â!y\x0011ªF ¾-gxë5¿y¾¿(G¦´ÝÝ><`{æúî¯_O´\x0018b(Ö\x0004kFzÚ¯¥HPW;3ó]o./®¯±Is}ùoï/Ny¯<_b#óÛ\x0004 \x001aNAË>"/5jCÓÀú`¡Z\x000fH[´r^Ò´+\x001f=ârºD«þô|^\x000fFWctrq \x0007)gÓl\x0003uHsº`\x0007H_ôr%ÔCßë\x0002ÚåpöÞè\x0003ùé\x001e¡\x0006\x0019:¾¶¥ÕP%\x0008Åw
ë\x0011c4sòA\x0007ÆTcL\x001d\x0007i)|v%\x001bå IYM\x001f\x0008Vv¬Â\x001c'Ò\x0000¥N´\x0016Õyr3Q±þNjûÃÑ\x0005Ò\x001d&HÙiÝGzáÒ\x0004úàÉî²yÞZþ¾ae=nEu%ÆáÎ,õ(J1gët l¿\x0010¹Ä\x0011¥¥\x0011@ØñG(ç3l=(Ç£å¯'\x0018\x0012ÄÒGÎT\x0015. ·û\x001cÓ<\x001e#<\x0001"Y\x0004\x0019hØ3GZu­ó|°©\x0007dë½åo'@]\x0018í\x0010ì9Gb?5\x0001t+÷léx:ÿl^éx9ÿ\x000cÍÃ1\x001d\x000f\x00078!ør`l	Ó¾\x0001\x001dV\x000b)Í\x0008Ñ6ÏÆv<\x001bÏÝp\x000810Îº\x001aTÆ¶\x001e¤mÞíx7G¥&Qç&áKl¾\x0003ÊæáØãy	4N¦çíçÝ=(c{^\x000e\x000btº\x0012_*\x001c»KSùò\x001eÍÓ±\x001d\x0011*(iëfÿm9bóz{á×ã:"6cAÅj¼T0ÁÎö{é×ã:"6L­\x001d\x0015ÑK´éøñì`*+YÑXþ(äñÁð×$ª4\x0002I>ù|\x001bs\x001fÐ\x0019Ð.ßwÓòð\x00080üwLÂmh*.ã[g>¬$\x0010Ö@¢\x001f¿~"*Læa*}HÛ]íô\W\x001b^ÜòõìÙÍ7\x000f?ýú_'$Êa\x0006®8Ð$\x000fSn&MáÄù:çïÏs~ýüdÃTÏyµáµ-«`A³\x0014çõÑ\x0006é»m\x0011.[ã²"\¸o$å\x0018´6ÆIbJ\x0011.Wãr\x0012\ -¸¬_1ôAÌnËgô5,/5²\x0019æËI\x001f$)?×æÀ
5¬ Ç1\x0012À)ÖÔ\:Ø\x0019 Á\x0015k\QËFbQé8Ýú °\x000bÌÁ¾\x0000	®TãJ\x0012\%Gv+\x0010\x0014ê²ËÎ\x0017z\x0008pUE\x001bm¸h³ò9q\x0004\x000eÌàÖ)\x0015äSÎk¾ E«±^Zd¾JTgðÀ\x0012iYÆ¡«0à²ó\x0001u¸Ô¢rþp÷ùËÝO·gß<ÜÝÜÿtâÄ\x0002\x0010Gî²øn|tõ­·3Ãz~}ùöÝåó³o®/Ï¯?\x000eÏÔð\x0010^ñAX\\x000fåàµU<1Iz$ç6Âs5<'\x0017À1o\x0019%J³ç)/\x0015¶ÓÍÙiéáýæß¶â\x0004\x0003¾,Ã°·\x0003Ò\x0019ø$´§\x0019|kçwä\x0017¯\x000e\x001a.\x001f
\x0007­þÀÀOÈÈÏü\x0003\x000bù©ùJÇ\x000eÍb\x0007`\x0011J ð ,{Zî\x0008ÑÄïÓeÖ£tsª­«\x00078õ{yû·û\x0013üÄBé¹dZ\x000be[Ü1Áû÷gÐj¼:\x0015»9¿ÖÕ\x001b\x0003\x000bÊ|d\x001e)\x0003°ÌsBÇ¶þ®Çåj\Nr`å!a§X\x0015N"ÊàÜ\x0011¡Üõ¸|ËKÎ«b¼d¹d[85-Y	Ö\x001fQR]\x000f,ÔÀ\x0004\x00184Ús\x0002+D1÷sä#ê¥rX±\x0015%°c%·ê9*Æ0+Ú\x001eÓü^\x000f,ÕÀ\x0004ç
\x0001 Eç\x0015Ø\x0019ì±Ý\x0005ëå\x001aX\x00005\ÀÞj1cDUÿb\x0003°*®tÍÍ
d%Ê¥7Yî~Ä»\x001fyÁ#*é+ÙyºnÍ4&úâëßïo\x0019\Ø\x0012GMóê®\x0018ys9÷PAo5Î`¾xÿïW\x0017¯.®\x001f\x0007ekPv=(ØúÌyZºüs\x0007\x0012bë1ù\x001a_Ik\x001aóMÉñ&_ÇZòáp)ÓzP±\x0006\x0015×RÓzá \x0019nÆÝ9\x000cjË×Ë5¨¼\x001aIå¦\x0017]qUßO;Æb>	[I·×|ý=7É°j^ñÚ¨¦àY"Ñ§Ã-lëQ5÷\¯¿è¦+ÜC^\6>>ij±)J15÷\¯¿è&Z*-4§Ccæ;bÿëÓÍE×ëoºAu²\x000cò8TBáÓ+Õ\s-¸ç>±E×G:Y9ÇçC!FFµP{
ó¥ÙAUµ×70\x001d~öòæÃ§nîN\x000cÃN-åÌ´Ð\x0018ì\x0002ï£ó$§ysq
BÏ^_??¿<91\x001eæ\x001b´ªJ±«QoJ}al	oZöÜ\x001d©µÌQ>H[C´\x001d\x00103«Ã$Eë677\x000e\x001dl9î8HW£t\x001d(}~ø\x001cñk»\x0018¼à\x001c\x001f\x0005ék¾ç(-¯ÑNZ@G±yÎ\x001fì\x0001\x0019j¡ç$#)¥\x0012?âTôöv.7Ø\x00032Ö c\x0007È\x000fÛi_\x0006\x001a\x001e¯Y°î@b¼\x0007eªQ¦£dídX$2J·s¸\x001e¹\x0006{Rs¤©#å\x000béÁ^ÍÛæ\x001d(ukÎ;ì9Ä	´Ê\x0011ã¤¸dbªë¹®\x0008¥×-×¿»¹)É\x001f\x0019¹¬±DÅX6rÈ\x0011ºFß_Áhäãpl
Ç®ciª=MâìÎOno^\x0010$4K­P=;\x0019øóIÒO\x001fïî¾»=9Ó¢yn$1CÌq¥È¼8KzýúååÕËdy;\x0007j5Ç
öõ\x000bÐùòåè\x001fëÐ\x000eD¨i4\x001eôF\x0007Íë\x0017 0óîÝÉ¯©g±BAfdÈLäùõiñ\x0019_þh\x000e\°\x0010­±Y\x0019¶èÇ\x0001RÀfY\x0013\x0015'£Ù\x0006ÍÕÐ\x000c3ã<\x0010BÃcs\x0014F\x0010lÛ\x0004Î×à¼\x000c\V<\x0001\x000es\x0005ØÆUDW:ÎÛBp¡\x0006\x0017dàyB2áÀe\x0015ìãÁÔ²\x0014[¬±E\x00116\x0010Iø\x0018\d6¹qÀ\x001dô\x0001àR
.É\x000e.©ê\x000eà<·:²ap\x001b\x000f.×Ø²ìà\x000cJÆç0\x0003Çr^ê¼Ó&\x0004WÕ\x0006Áø*á{Hc'\x0001NÎ JóÛ\x0006­õ\x000b2Ç\x0000S\x0016	\x000fÎ%âø\x0018ø5lÃÖX_-3¿ÑêqãpÁfi|TT'°¬l\x0013¸ÆÄiÅo\x0019Ò]ÑÜ±w\x0014\x0001<×k[n>\x001bgc%ÙöúÃ»/%RZ¾mÚì\x0001LT`Vµçfßí¯=»|WÂ¥ÇaÙ\x001a]\x000fËG]\x0000û
qÎ<³\x0008Z\x000cý´õ°|
ËKNËÃèåØ¢·4¥_N\x001b¸~\x000b¬XÃÿzX~^òª\x0016&9{{sÿóýÝÉ\x0002b¦\x0002b*¡$íU\)·ó
] \x0017pööüêÅÕåÉ×¼ª5IV@K\oµiÊö¸bg¬ßÌÖÈ¬\x0008Y¤m\x0002Ì
\x000b\x0005¸y\x0016*Äåk\^Ë<v_Dø\x0011Zä©ò¹]\x000b-øy©ÓW«p\x0006\x0013ûæáSy\x000c\x001fNß\x001b¤)Q£(gb·5«Ýq£Æ`cß\¿.\x000fâÙÉÜÝÏ+¾Ú³\x0012_ªðe ¼a®ex«zø|ÏKñ\x0015³
FQµ\x0000\x001e®t\x0011\x00025À(\x0004\x0018µ\x0019}(ìLQØL*æE=hÛH\x0001æ\x001a`\x00024t1sö4q¬\x001c,¶^AÝ>\x0011é\x001b0¡$di\x0002^YRÙ-ÿáÚ\x0019!Âæhé+\x0019\x0018zx\x000bK>M\x001cUKE¸b¡\x000f÷\x001e	\x00116ÏDKßIT¬`\x001eZq8ñm>Áæhé3\x0001Ê\x0016õì¢G¡ò\x0015ÝB\x000f\x0017[­EæÁfí\x0006¸7·\x001fþtöüÓýÍ2ûÁë×\x0001`ÈMáiÊÔêi¯Úg8{þúêü\x0014\x0003"ÍE\x0018Ò Â \x0002hL¦Y(I\x0005\x0006-Î\x000b¶¶æ\x0000õ\x0001´5@+=A\x001fÇ4\x000cN0\x0011$(Ê­u³6¶\x000f «\x0001ºßá	Æ\x001a`\x0014\x0002ô0ð<\x001aBãG%ù\x00142>cÙ
0×\x0000³\x0018` ¾õ\x0016*)\x0003ÀHÎN5mn!À<\x000f·²g9ê$\x0010Ç4¡r2h\x000côK7ÕçZ\x0010\x0005ËIÎ\x001215\x0018³
Ì@!\x001c±\x0000³\x0011\x0019qfoã<_\x000bÅÖPìºs)¡±ø4TåFY4*ýºùÌZ,®ÆâV~£S1ªØLlR"\x0011´hó|$y%\x0016_cñë°Áu\x000f]þ\x0012c$r`Éâ;ïK¨Áu`b¤)&øH$±\x0017üôær+Á¤\x001aLZ}cH@¶d\x0006È÷Izàñp¥Ë:0µHDJ\x001eAc3KÅøÁÐÎ¿\x0018	MèDÓ¼k½îa{Â|kh;\x001cQ]Ë¥/Hy\x000c\x0013#½i{b¯>Ý¹ùùþöìêÓ©æë$a\x0000
ýÅLI\x0012]õA»\x001d\x0017Â^½;quqvõútÿÕÏ'\x001b½i[dkFEê(¹\x0004ýD¯NTEöy>©Þ\x0007ÔÖ@m×Nd<\x0013ø\x0003\x000b6Xâï`X®\x000b¨¯ú\x001e À´À\x0013U<\x0003©Èóùùf\x0017!L7÷ÉÎ7Û_ÞÜÿüõö§O\x001f\x0001Â\x001bFºó$Eá\x000c\x001d¤Q\x0007¤Tà\x0014_½xñüõ³Ç±Ù\x001a\x0015b\x000bÖ\x0019^]\x0010o¥>ºÎV\x0000Î×à¼\x000cÜHm\x001cÁ9l\x0007@\x001fµ²\x001bÁÅ\x001a\\x00035\x000cZôBû\x00153'sZ÷~T3Oå\x000ckê}{óãC÷?ÿøÏ?\x0016C}w¢ôìPÔÙk^e\x0018
)\x001b;¼ßs] ]¼(\x0018ß]¬>y.gXPO\x0010:U(-\x00021NÆÖf3H[´\x001d ­â}\x0016FS0;}híæ\x001dú\x000e®\x0006é:@ÂÌ$n0¶½EOaÆ\x0005¿\x0019¤¯Aú\x000e9Ó`N2FV/Só\x000eª\x0004¤\x0007\x0012\x0003óùÓ§ûÏ·gÏaIØìÝâ.Ëq\x0007F½]j>$ov\x001dÏ_¾ùÃë+ \x0001Á°SaG\x000f£Õè@
\x0018Áå'&Ò¸\x0005Õ· \x0003·
®DÓûQ||æÈéíw|º\x0012\x0010\x0019\x0000Þ\x0008\x0001ÆQé\x001eVC(â\x0001ùÈþ8\x0017\ÐÏ¶5'üî\x0003Ä4WN1Ê0\x0015\x0013æ \x001c6V¹\x0013ü\x0011þàå3g®^´æöÚÇ
¾\x0002/\x0006\x0006{\x0010iXJELÜÆcdV\x00016Ý`ÓBpwC\x0003ó\x0012\x0007Ý¦QJ¯ç²"t­|¬4äW\x001f\x001e\x0017Ýb´SâÏ»hÃ1êwï~|<Ôµ~üj¦wcIÆ\x0015&½1òêË\x0003âÍÚ#Lsíø4hÇ×¥óïïn\x001f~>Í\x000f¤\x001eïiÂÒñÃðK
Äï//®_¬ÀæjlN-Ø4ÊyÇÑ°ÐùZ\x000b-ÕÐðØ4w«S¤ÒA\x0004xî,\x001c¨ëÀÅ¹³³¬ýú×ÿþË×\x001f?>Ò2¾@\x0011c
\x0002ÑÃ¼ê3¢»¾xóþ ô8B[#´bÅ\x000eãHS,`qé¼WÌÞ\x0008ÇÙ\x0012®FèÄ\x0008C$=y\x0010Ñ\x000e<Caý|e¹\x001c¡¯\x0011zù\x0019Në®Ó$®î\x001d\x00135×!ó£ï\x0007»¾-xøröí-}äâ2`WÊøL¨Îá­5íûú¢üáúÝ)Êw£/\x0007[\x0001pê\x001bj÷Äá;¦\x0011\\x0017jûà¹\x001aÂ\x000b'6i\x000e\x0007¦}ª}èB.\x000f/¢XiÉØH/ÎEÃCaÓ¿\x001e_ªñ%)¾\x0012jÃþ\x0003e3JfÌëGúÏÏÏ+W~ê&xâöë2£¨¼OZÅ
SÄÄGò\x001dV½»xå4o'ù©ô(ÈE*m¹Ázb>y\x0017g-\x001c[Ã±+áXM³Ó\x0005\x0018\x0005êZq\x0005w^[YÆÕhÜJ4AÃ ûX2Ü1-A%U¢:Áø\x001a_	\x0006\x00140°Ô9pnF,LÂÐé`úJ4¡F\x0013Ö\x001e
/\x0014\x00068XyM&\x0005ÎóæÉZ8±\x0013×Â©B\x001c&Ï5Ãyûo-TI+ÁDC~9{KL\x0014(ú
Fþ©²=ñléÿéãÓÓÐ¿UtÞ8x1N°y\x0016
~ÿúå»Gæ\x0010­\x0001Y	 ÌÚ`%'@4Àéæ\x000bÖ\x0003r5 ·\x0016u\x0014\x0007z'\x0006£*õÎÍg5WàQs\x0017¡üÙ¹\x000fð\x0013ªwÙq¾¼8\x0013ÒÖÒUrõæ ÙàÜ3øÃIñ»¹ßPþp\x0007ìc\x0010ÖÜQ$H©=Ñ\x0000!XÜ\º\x001a¡­\x0011\x001el}\x001c¡Ôz\x0014
hÏêF¶.uBt5Ä\x0005°B4%¾ÜP\x0015\x001f Âô(âv¾x°þõQnà¨ÖHá2U«AÖ	0Ô\x0000\x000fv¿>\x000e0àp¶	:`ÈõB®!\x0000\x0018k\x0007{_\x001f\x0005\x0008ë\x000eI.
­L4Ê²ÈV\x001dOH\x0011Ú437 VSÃ·7÷gßÝ|}8Íy5ª\x0003½s¤\x001fhrY~îÍ¿»8¿:ûîüýõ\x001aP¦\x0006e\x0004 @ #M¥QDÅÖ\x000fÖðlekXV\x0000+\x0006\x0016ÙÒ¦£#*¢Ïs÷%åjXn=,oü8¶9Nwà0@R$Pþû´\x000ck¹\x0010°B
+\x0008`)\x000f-\x0015JÃ"~Ä8¥a)l9­Fûq81Ò~üí\x000fm\x0019]?ÇÀÏñõÜÜßü²¶Â¬\x001cN\x0019O[e§e£v>Dúú_¿z\x001c©±-\x0016[c±ë°àJ!`@R1½¬QR$ÑÎ\x000b­ö ÐúùîóSÄsÐÀ"!ÌâèLú\x000f<²7\x000fõ©\x0004÷öòí»óÓÄó8ù£myQ«\x0010fM¼éPIMb)ä\x0016m¶GIQ\x0012®F8/´>ÐjEá\x0019H\x0000X#UL7ÿ´\x001dGXu7C¼bT\x0011Ú®\x0003ÆbòIrHÊM\x000bã¬\x0007içõÓMü\,ØÃO§VP:(á tmäfDD²qî¼!¦øîüúy³r\x000eÇÖpì¿\x001c¯áø\x001d\x001c=7\x001bzf6}úú\x0005DZ\x001eîN]y]MS\x0004á\x001dûþø,þ³×ïß\ËõåINÉü:\x0019¾NÏþtóðñö\x0017`þ-§%\x000bÔR5Hxi$îÌÄI{öóë\x0017¯ò÷8,SÃ2\x0002XÊ+M\x0001'á\x000c7;Ü|\x0008­aY\x0001,\x0013ÊYr
$ZÅ\x0012V`PïÌÒ¼\x000ev³òS±>X~z~{÷ùìÍÍ_îî\x0017`Y(\x000bCoNe\x0003w\x000b`\x0015,\x0018t\x0005æû+_\]¾={sþæòêØ­/|×õÂ÷5£RRÉ1\x001d¯<ô\x0010¾ÓÜ\³ÉMM_?\x0016»ðííÃÃß\x0017?\x001b,µR\x0018Ø¸ÄôÇ\x0018É*ø°ïýËb\x0017¾½¸¾þ÷\x0013ÍÍõú\x001dëõ¯U2\x000bR\x0000pFMJAZý\x0007û¡D°l
Ë
`Û|LI
¨`hrÈùØI
kA[ÊÍw\x00078Þ\x001d°î¨Ì´ÖÀ=13á!æ÷i=$_Cò¿c5¦øûÀkLù÷I7éà`\x00148\x001d\i\x0017&³@û\x0017i½j±
sý´UÏÏæyÚÌ«O_?.Îqòjî	|×ý|6dÈQ_½~ÿ²ØÎó²sîÍMiæ\x0011L>*\x0012Ö3«)pÐnÍÜRUNäs>]`>ÝõÍS\x001cX\x0013\x0014ºDÐ]¦~4ÉVAÙ²Et}þì4ñ5Í\x00177¤ÀM»\x000f_>=ýáëÏNÔX%>&Oìèh\x001eÅÅyùêûËgï^_ýáý×§¬ù</t¶)Û={u÷ÓÝ",]°DÚi¢I³°\x0018LÊ\x0008?ÖSxöêòùåã°l
Ëþëa©ùþX5í\x0004âÛ¯¿Ü`\x0011Ä4Ì\x000cÌVØÞyÙÔA_,ÂûWçïª¢\x001aýÅ\x0014vÎ÷mzßÖ·\x000f·ÿúõöãòó\x000b\x0019íTNX >ù~ÓrNßdôßÞ_¼<ÊÍË\x0015Ug\x0010Mù\þo0ËÈRb¾¼gFaJ$\x0008\x0001gw\x0000
þÉç×oÇò£ð\
Ï	áeOÌ=\x001f=Ii§LSÚ&\x001d¤Rx¡\x0017dðÊw£Åµ>\x001b^C£\x0000a\x001bQ#\x0019¼\x001cf^¨øÛGýÍ§Ï'7.&\x001dRè¼ÇJWÔaZã~¸=ð×o«EKL
È¬\x0006&u\x0000\x0004<±¢
Ù\x000bÒá\ÈÖ¬àÌ¸¢¬ *Ñ;µhÞ
¢£=üxë\x0010¹\x001a[F\x0019 ;áQY\x0015Å´³{*DÞ$_òë	ÄDh¡pÆ¹ñ¨=:f¼V5¨¸þ¤r ²±\x0003& ö\x001d¯wÁt~»T#Jë\x0011Ù<NnÃLÃÉí\x0008:H«^D¹F\x0005g¤hÝ\x0019wä"zXù«å\x0007÷Øw«'¸C½±ðQPMl ìGÇ4çÓ­=&ÝZÊõ¦2m.\x001a¥Ú\x0012½E\x0013\x0017ü4¤ÆVj±T<Èk¡yO"H$\x0003 ÕAýZðí\x001a{©×\x001bÌX)t>àAi
c´ê5áº1Z`1H")õ¬ô­\x000eFÁ$çÔ\x0018L½ÞbÆh¹¹õS\x000cª(/-ÿ¸~©C*¬Ge49`\x000bD¼SheÅÐo¸S\x001d×\x0002C^\x000e\x0008\x0017:ÙF$ÚØ\x0018\x0019Ôá´ÍjP)×\x0002[\x000e«-IÙÆàaT&Ó\x0007LyÃQ5æ\\x000bì¹\x000f´\x001c& \x0003\x001d\x0015UúÕ%)kAÆõö\x001c¤¼s\x000b¬<\x0005uM3\x0003 ÇÛg\x0013LcÏÀ;E¡/lÁ²ä-ÆujM0mô+°èÚ³X±|¥H\x0007[\x001dÔÐ\x001e;¦q¦õd:Ï!ì?>`
  
  
  
  
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
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=>9=8=~·8{;!\x0013?B²üGH¶\x001f\x0001¯ä\x0018¬ÇÎhT5ý±ïÐÿ\x001bxñ\x001bø>~¡Z\x0004\x001e=\x0015\x001dzZëì_ _ ö±\x0004)@\x0005Ä­$Ó5ÏW!fÿ\x0008Yü\x0008¹\x001f\x0001bÅ\x001cÏÚpï³JVïø9ØÔ²|\x0005løoqÿp3¤©_ßßí*©s^k|¨ÑÞ+z¨QÎàc9Ñë%ðóðï )ýúü\x000céçòD%s*ÙL¥0¥½I\x0005ùÊá\x001cÞzz T\x000e¥Z¡¼ÅG\x0008Ã G\x000c+¾%uø2]µ</p><p>M£Ò9n¥rPd\x001aWÊ¤\x000e\x0000²lðÆºO\x0006er(Ó\x0006åC$\x0001¾` \x0002/2Z\x0012\x0015¯êg¦QÙÊ¶RÙÊHåXÀæI\x001cU	iP>òP¦öMå`òlìÕõ´ÓMe0&A¥Ä\x0001</p><p>\x001e\x0012Û¨´À(=¡0`(\x0007$hÏê(}\x001a\x0016/°x3§Ác\x000cj.<V)Òl
mZÓ°</p><p>\x001bÊ\x001b¨çáN5ß!8$ÕVkÓjéêæ>
«0¢¼Ñ\x0006ihü\x000fËyÄr©\x0016©ª@v\x001aVaFy£\x001dõ"¸	GOQ¯-f EØnUX,Þj²U</p><p>TÆ8g$bùªìb+V\x0008)øZm¤áEço1þüçÇåír;
Vd¦\x000b³JÕÃU9©51\x0004\x0015Ç/\x0017§\x000bD\x001bþç:ÈùD\x0007ó+>µJS_rà«â¶&>óÉ\x000e>íH»Èz,ÂWÊÉp²z¤iÂÓ9îÀ\x0013\x0006*í£°Å¨B)µR\x001aoëÂgr>ÓÎç`D\x0004Nóc\x001e4\x0013E>3>\x0017`Oþõæç/·¿.ñÐÑ¶üzýp÷	</p><p>%>ÐÉ\x001fÞ<<Ý|r 1LE1¯\x0010ó\x0008átÔJÕá\x0016%ýB\x001c¦1\o.®N@\x000fùt\x0011"è³WcÕË\x0005BØöâ;#-¿\x0007ÂçßÍ­ü{þ!þÏÿúßÛ¯\x001fý}B;
Õä\x0003E¸û\x0018J)ë\x001c\x0014!J\x0014\x0007Ó\x0017ÇoÆæo\x0014\x0018ø1¾7\x0006~ïñå×¯\x000fMþQ@KüþóÏC\x001fûæÁ\x0005dVí°3X0ÄÃ 8Í\x001d©Z\x001aYl\x000cP\x000e?ýb´i½ Àoò=(`øËÏ\x001f\x000bKqðrù´õ@\x00146\x0014äÂH
\x0017oµ*Ü$£b\x0016B\x000cÓVäàåâjÛ)É ÈV|{?î¿|ºý%[7÷O¿Üß~\x000cmñ[Èp9\x001cGö8mLÃHd\x0004oÎ¯þýütüKd\ï÷÷ÇÃùÿ~ÿýêsSùæÏÞ\x0006\x001fú0n\x001añx~ \x0000Ý2\x0017	TL\x0019\x0004\x0000?T[$ãÓã\x0017ãf!\x0003À\x0005ø~\x0000Áé«ï</p><p>\x0010b-ýí\x0001>?ÝÚ\x000f.Û\x0003GË§Ï×[ö`¸îØð×\x000cfÀ1}\x0008WVå¬Rä:8îÂ</p><p>\x001c-®^\x001foÙÙß\x001fÏà÷ûûã\x0016ü~Üßïï\x001bðûýýaÛoþ÷ÿÆsîk¾ÿ\x001e\x001fïÇc#\x00186È1[ïa\x0012Úà\x0005\x001däM¿[eóówtuy¹\x0018ó(þzÜþßë¯ÇÝÿMÿzùËýûe(ôîæþéaùaK\x001câ¸Í8\x0001Þ\x0018Óh\x0001£\x001ev\x0016¼;9¿ºXü8\x001ed\x001c)\x001aúÎ\x001ct}úÞ\x001cÑ(}h¾?G4RßÃþ0Hd|\x001f\x000eñUÿýo+Ïíû§ÛQ\x0008(\x0017±8ÀIè\x001c</p><p>«T¸^¡áPÚ\x0015¡+tk_Î(\x0010ÒýÆ\x0008ÿõÛÍý¾vûéæöf\x001c\x0001ÚbrÌ\x0005?*¡0\x001c'N\x001cÑð°ªJNNO&!¤Uø~\x0008Éf}c\x0004ÿóÍû_?d\x001fâõòû-nÌKè{\x0018\x0008`øc,;\x000bA\x0015HàüÐoB\x0004¯\x0017ÿ~~±Åe\x0000ñ3|Gh°¿5@\x0008\x0001>Ø"ýy}pº¼ûpóç?Ç\x00105ÄÎPÇ\x0019w±BBc\x001a«<´0¾È2A×ØÙ[öA\x0006Aùï</p><p>çáûB \x0003ÿ\x000e\x0010üMsï\x000bûx÷åéúý§-&\x001afDÆd0hß³h¢5×\x001e/·¦´Ðgo¯^M! óøý\x0008È:~cìï¿þ±æ¥Þ~ºÿ\x000c&\x000fãVÚ0;\x000cG\x000cñ\x0003t
Q±\x0010#D
­\x0019é·¯Î_Ã;ÉÅ=Ñ$õ,hïú~4æã¯_·¥
ýËß?/\x001fÆÏ,¼òÆ3+4\x001bj	àÌ\x000eMÑ*xeÏ\x000fíÿ\üåõâb</p><p>D²¡ß\x0013"ÙÐo\x000fq÷ûçÏdãøñËòæîãøÉ)}C'*³(ç¦àÖÓ³I8¾|»89{9\x0005 ~o
ðÛ/_ù¯E~xùaùðq¹%AmBh§Àµ\x0003j±ÂãU\x0003\x0000çÉÉÅñì\x000cûúù£Së\x0017»;\x001aÙ\x000bj¨fwLCÏ¢ÂvÏ\x0014­Ýw^mÑ*0²ËÆ÷ÄHæê;`üü;^\x001fåtùôp}÷~KÔï Ì{Ó"ÈàÖ,*wà"Ö·g\x001c§«ã³£-\x00063\x0003Iå»ÜÇ¯ËÜT?ÝÜ~ÚvN\x001cHt"|ÌØ¨×QÆBË`Ïò`ëüêäôÕs\x0001ÄøÖ\x0000Lüö÷åïå8Z>|¸¿Ûv\x0011d ª\x0012_\x0014CÈI`³uÌ&ûÈÚæ<Z\üx~¶åSd iO|\x001f¥õ¿ñµìÀòã})¹
«\x000e\x001ecáQ¿QçKk¦­/!~Zê\x0017\x0000«ÜÀw\x0002Xe\x0006¾%ÀýûÇ³O°xºû4~)6<~­\x000ba²üP\x000cOý\x001a&k\x000eg\x0002ÇÕÓ_\x000fÛ[®ÄÙß\x001e×ÿþíè¼¿+Þõ¾.ï¶e\x0004åà!>\x0001RÐv\x001aÏ\x0012Úägàhñnq6
\x001eö¾-À×¿ßð¯å\x0001|µ\x0004¹¶w7\x001f¶Å÷ÚKoÃ_=<s¸\x0010W\x000e¦Êy\x001eÛ\x001e°zÍI¼ZTÛ»W[cü\x000c*\x001dÊï\x000e%ÔÝ§ÏÓì×á >ý|ÿô0\x001al\x001a\x0006jR6¦7Q×\x000bZMñsI®xq	:\x000eõêÅùÕÅxÀÉ?}\x00117Å¦}ø°¼¹½Ýrl0\x000c³Ü:\x0017Ø°mÂnÂ\x0002\x001dÅl"\x0018îÅÉééó3+ô]å__°¨ïúzùxðâúáËx½vÞ(²å8\x000c²1¹)=N9ø¯Êój\x0007//ÞæõBë\x0014"§\x0010ßKS®\x0005[Ã]\x0000²\x0018C¯àËåÃ\x0003lÞ-o¶á#Åqwáh\x0007Ó\x0016ï\x0005N8/\x001cmW\x0004]o £1´\x0005¾\\\Àö\x001d<\x0012 È\x0001Ås\x0001dU\x001fÑÿøÇZ½×Ãò.:B\x001dqXÀùó_oîP)zÀN)\x000eï\x0014F\x001aÅ.oPe¡Ág\x0016BØêøÝÉYÔ~uW\x0017³Q¿X\x0010­¿¾+Ñ/Lúß\x0007"(^Q\x0006cß¿ÜìFòLÚXén\x0010\x001c;gåP\x0007\x0000L0\x0003obúiñ·Á*nîG\x000b«\x0014þ;Üm¹J¯ïnÃ¦Ù½L^à[QÐØ¢\x0004w­Eä\x0015Óëó«Ó°Ã6C9÷×XsÿK#JJã\x0007þ¿ïïoo®\x001f>?àÏó\x0006\x001e\x0007\x001fÿíry»|\x0018àÂ\x000eã¶LX#Ç,ò\x0014aÕ·ôp\x0003b\x0018í.Â\x000eÿ·ËÅéââr%5~yp|t~\x001aG¶|Ie\x0005Ï\x0012K_#åW\x0017üè§"	óø\x0018¢h(x?\x0002Ã¶Ðib'Ü\x0008\x001fû-ÂÅFÄ²MadË[\x0012BÁ{\x0008­¡äý\x0008,Ü\x0014<,á{®xX_÷¬ð~ñÁÆÝæÕ_i|ÏË\x0010.ß~Xîâ\x0003}Þ8{¡\x00079L\x000bôÎp}6í¾«à¼Þ-N\¯Þ/÷ÿxxÊ/P_¯ï¢BÀ 'ÿ\x0008b%»ÏÓ(PÂ\x0010Ã\x000egDÆ\x0001£a
«ÏÈâÝñÙUÔ\x0006\x0018ôå/A­dË1Y¡Æ\x0012ÿ+Pc\x0015Çÿ
¨\x0010Ë\x000f¢¡ÿ7°5åÏz]¯?Ü>Þç\x0017ÅÝ0Þïàòéöö÷\x001d!Ivetw±&Ö{ÜjQ\x001fúÅÙ0Úïàòêôô/?¼¿ÿüù)Ä1øÏ5\x0015f,¨ä\x0010{\x0001r6æÐÂMÕÅ£\x0001K`\x0008=\x0003+\x001aÉ6,+\x000fe¤eT^áÄ\x0008n²s©¢gi£"V\x001f±´
å\x0001KÄ.¹åqq³°Ð\x000e6ay\x001eÕ\x0013\x0000KC\x0004;`\x0019°0+<\x0003\x000bm^\x0013\x0013ô
MX·\x0008\x0015Ë¶Â¾\x0002]¸yLÐ·Í\x001bO!H<A¸7\x001cCÍÃ\x001d1b9\*k}ß)üå7yýó}f\x001b@\x0016ìÇû/×;\x0015EÊ®ÁtqH&\x000eÁ</p><p>3ÉtÙiÐ\x0002»8?y;r=+â^VHÁ\x001a»çDûéY1¡\x0003ÿþLöæ·'þ9Ûào\x001f Kô¤ÈO\x0001.fB·[\x0005\x0003 ?È@-hp8%?ÈkÃðö\x0002\x001aH/Iüt\x0011H!7ºù,~þrÿÇ]^\x0018w\x001bGA£û§÷w_v_\x0014Ù¡\x0015ñ¢\x0008oótQ</p><p>/\Õ¦5ï<j:GçWG¯\x0016goGW7CÞòù#ÿö=Ý!/¯ï¾Ë÷\x0010¹]Þ?=¼¿Þ\x0019µiã\x000eã5\x001cþÕ².ì[Ü«Âc¾%G½<>{\x001bîÞCÔvy~uqôÿ3÷.Ëq\x001d»÷«pÖ£ÃÈû%4*É´L\x0007%j¢ãøLv$Z¢M2EÚGý\x001aýzý$
d\x0002Y+«V­Ê\Uß·\x001dÝ^Ç\x0016·­ò</p><p> ?¶EñÑ¨¿þÃ×´U·ËåÓÇåÝÎå\x001a¢Ë9C°\µÎr°\³X\x000b¬V§6Wëª¿Ûåâêåâõ¶u: [\x000b¸´ÓÜY\x000bo3Ú#\x001dy\x0012æ}s®gà­EZñÉÍ¢\x000cV\x0000\x001dÓV\x0017lËõwö¦£\x0012¤^º(BÖú6XE²	Ï	¶\x0005¢R³ñ~}ÿ1üýuøZw|±üüåè{ðoÞïÂÄ6ëY]XF\x0018L{\x0004NyÚ#°\x00007)×\x001aN¾X¼zsô=x8[^Oj^X1q\x000f^\x0001\x000eÄk³:\x000e\x0000K2\x0001xsÒ÷áEU!ük\x000fàkÅ\x0001\x0018\x001f3\x0019Ø{\x0002F5Ç\x0012Ã^mh;­¡NO\x0012å¶Ò»Ç4p&¶#N[?ñøüá8Wî=rÿôõñúq·EbÁ\x001fÏ½_¤/^SÆQ¸ËL¡¶q~uùöäíu¢¿ùßíõÐ5¿yÈáÂû§\x000f×\x000f;G\x0014ü]\x0004¾</p><p>ê\x0016s.\x001dTÎ\x0011oåô"\x0007\x000bÏ¯¾;¹x±å \x0018{ÞI¦C\x0016¡C´7{:¥àb´8â ÷¢å3ª{Ð\x0003ÐÀ­RäâI>ß]n>¾'\x001aE\x000f:Ñ`\x0016\x0015¡É@{:`éÞÆûh&Ú»ßäã÷CO¯t[~{¸Þei|íÒy;Xzx!au.åfjÕPnñóÅÉvl@çóH§óHFNò?L>ÈðnXñÓýM\x000ebMÈNÛZ¢¤Sîhª\x00148Z©÷`M\x001f\x0010üõõÓùibÈa=Ë§Ú?\x0014.¯¶(\^pÿ$8\x001dï\x001eõ0ýqõ²ÖÉîí\x0010s.\x000f»XÀ*)pk³$\x0000giømO[hÀØr'¬àjg®\x0011\x000eî(\x0012}Çäö6:\x000e(å\x000eÍëMw³\x0011N|ÑwËÏ\x00038Ø¼½h\x0008ØÈ$\x00026"'\x0010Ûæ\x001d!jì\x000c¹:9z{~1a\x0010
xVÁ¿ÿ ÏÖ¼ÃÓ,7\x0006¿\ÞÜ=^ÿ×÷÷»\x0002·*\x0018\x001f*à µ1·\x0006÷ÁJòÄ</p><p>f3®_.N_Ãûýù\x0016A\x001a\x001eÄÿQxwâ×_Ô»ñÑû¯\x001f¯w;ñÀ\x0013Ï¢³Ø¨yÕlk-7í¡\x0001ÞÑ'×-xÙyü§âq÷Å÷øñ¿­ø°&þþéf×e óÇô¡-EWè¨Ø¾e	kãÏ¯N·å½ÉßÞÅ?¿`\x0002°µàS§Ï«åçë_ì)	(7\ÿ½|OÙeÖç4<ç°\x0007qÖÉV^ë¬ÞêÙE9ýéä\x0016/½Z¼:ùqKþB\x0010\x0010!4!\x0004oE\x001e\x000cm&p	´\x0003à\x0004üÞé³\x001bÀÓïî-5RÞ</p><p>K¿½\x0013³\x0006ÀaW¸ôiøýén\x0003(Hë\x001a\x0010¨LÏ\x001b\x0002¥ÏnhsgQ\x001c\x0005X*#\x0004Áà(­¥\x0017\x0001\x001fUÓg76)ì`?\x0004êK£¼ ÝûHý~û	0\x00151}v\x0013`k¸¼\x0017¬u¤d¯¼$%ôhgAÀ1\x0008McºÁy%Xù°@	O\x0004&È9\x0008\x001e¯ôi\x0006¬BF@Ù3Z	äü£uó\x0008°íjú4\x0010è|\x001d;Ìy_­\x0004ÅÓàmì@\x0010÷Füý\x0005Oè\x0008¿{´éúp	¤×Û9´
>\x0007CÁüt:7oÆàC QÔ\x001c)Áõâ$%î¦Ñx6¦O#Np\x0012\Ó\x0008%Aué`gº#óq\x000c¶AIF\x000e#\x001cã¨v#\x000bÙ\x0007Ç!ëÀ±"\x001e!5ÐpÆäT\x0018 ñÖìAãÆwÐ8q¬eÆ1©. á¸\x0003\x00038Qì«Æt,èE~jÂÑ1Ç1d\x001co\x0018ÇSJÎ<\x001c\x000cb¦O+\x000e8FGÓLE\x001fÊº	óY,^øéÓÊ\x0012©MA^ÆIZK®|Áq{àà>ÍCã</p><p>O£GÇÐ®RJï±pÐÐ|>Í86÷\x0004\x0002`rv\x0012âä¶\x0004\x0013öÂqÓ¼p@%q\x001a\x001dÔÏ£#U\x0019\x001d­ö8-ê</p><p>§O+ZíòHÍ{\x0001G;\x001e\x001dm÷ØV\x0016ÎôiÅ\x00111e!Ëñ8:¹*\x0003qâ>;\x000b\x000e±géÓ<Y2KZ£îÊò\x0010cig)kô|\x001c|é}>Í\x001bÝd\x0017\x001c\x001dyìh2Wf¥ã0P>Í·§Ê§88>wÄÛSÁñ{
NDø\x000f\x0019\x001c|/MV\x001aÒþÓà\x00182\x0000ñ2wtE¨@\x001eû<\x001c<ÿ\Ï!¨ENÑDxì	GC0¸=®\x0008ïßéÓj\x0007¢YçÊI°\x0003m¶\x0003]NF6R\x001b½ÇÒñhVø\x001e³TÇã<W\x000e¬|$»(\x001c-dlh6& A\x001a:¬ÒT\x001cd\x0017©mÄ=Fg ¡pÌïîîGô ð&§ÛüùÃýÓ×¯\x0013,VbSÀlu\x0005arÄ\x0006/ÖX__]^¶àÐ¸4H\x0013g]ðÞåÄY\x0019¬´d¬ëû»\x0004c\x0013¦yLTÈOqLlîö\x0008$J3Úv\x0012">­$p²\x0018YÆ$\x0015\x001dH<o\x0014Z÷_ÚIð¡Ä7
¹ü\x0001ÆDRW8 qIX.t\x000e	îäÐ<&NaßÇ<&2\x000b#Iîx
»'Ùc"ñv¢yP\x0002­\x00128â"qD¾\x001d©Ãï<\x000e\x000cÉ¥O\x0013\x0012T¦C\x0012²r¦\x000c«¹\x0011\x001bÇ[\x0007	Hóq¢\x0004á}ãd\x0008<"~þÌ` 8}Ú80RÒ\x0016vtÄ\x0006ñ\x0016³\x000f\x0013>¶ôí("E!×#4Â~­5~öì(t"hFÁ\x001e[\x0004ë\x0017ó\x001evì	57{\x000b«tét,HÜ\x0010&Ë\x0012[,Ñ\x001e¶1ÌGÁE¢ÚW</p><p>Í+\x0005\x000cüf\x000b(Aéâ}\x0001*<èUói¯À]y~"\x000bàÊàÁ\x0007a8¥à5>m(J\x001eÛ¼h#& è<*:ÒZ\x0001+f></p><p>\x001eõªù¼WV²Ù\x001fµË]\x0000Å{ ãæ¯\x0015\x000cx§Oã¨hÜ5	ÅP_F@\x0001ëPììóM£q­eûN¶¹Û\x00018G±»à\x001cY(p\x0019îAb¤ãÄÏò3@\x0002×±àC¯cÇ\x001aYsPÐdÓÍv\x001b\x001cYÝ\x0004L{¡(\x0008(4;^Ì7e5nbÝ¾9Ð\x001báâÊÚ3¸d9\x0004äsËóY$\x0006#Ól¢(eóË!n*gw¦%Ë(nþñ\x001e=nF1ÔíØE\x0014	åú¡\x0010µ:g£$\x0003¿}¥(CÖlD\x0007H:\x001e\x0015:S|t³Í\x0003òaÚ'H¬¸
(0A¼¬"g0Ì\x001eËÝ¶\x001fùF\x001dt¤D¥T1"Ës@ÜÃ´ègØvg#\a\x0004(Ú³ï¿\x001e¥==\x000e\x0017k_)Ês°Æ5R¬\x001b\x0017-]ÑÏ\x001fÕkãJ±ôè\x00195\x000b¡áJ¡E\x000b§_ìÝ?_ïþ~ònÄd\x0011þ\x000c\x0018\x0004¶\x001cFLÉ%\x0015\x0006DÛ·\x0017«ÿn@(u\x0016M\x000câ9p%{·Îà6¢¶­\x000c\9±AÀ\x001a5\x001cáJq</p><p>\x0004vv´Ý0KÚ\x0018\x0014n\x0013å[ L°\x0011<ÜÃ1CÀÿ£²ÒÌvÞ3\x001d\x0018¼Süq\x0017(¸\x0016åsÃÄuS¤Á [cDË0paVPb"g\x0002SìîIÑ5\x0019ä¯¿ýV\x0005Ó®~º~øpsý0±&ðd\x0004­KH V£R¬\x0004N~:¹øîôdÜô¤°H¤â\x001a{3e\x0012>AÅÕ\x0003ò¶D+\x0008\x0008\x0004BÝ\x0003$¸7,U\x0011MR"XM$Æó3¡BaÂ<$QK&ñk!é\x001e\x0012\x001cNü«DI\x000eN(0%-\x0013ª¸\x0001\x0012\x0013çÏNÉ\x001fi"±.Z !±F\x001c@Æ°vöHÎóæ¢rÿê$^\x0001¾D"\x0002\x000f\x000f\x000euÙ<&¡\x0004\x0004à\x0014ÆäDâ£æ11³7ñ Öâ,?ê(¬\x001f£ÍÃ¶\x0007øGr6	ÆåÓ§qóD\x0012Ó\x000b\x0018ÏR´N\x000c´³AVÑ´&\x0010¯²°\x000bh%\x001a"q¹øÜÀ­lfï\x001dí{>GÉ¥\x0008\x0002\x001b	î^8Øüì%¿å3Ý|ÈZ\x001fÙ\x0016AÉê\x001cb\x0004Ï&\x0017\x001a\x001b\x0011Öm²\x001eçÛ\x0012Ë+\x000e\x0016f\x0004{Å$®wzÞýòÙ>ý3'·ãßty;a-{Ô¦Ð,N)_\x0015Õ(KÑ\x0018±n¼¿_líì5 Q¸\\x0015Ew£XL\x0010LcâÀÉ£ÔYiÁDÈ(#\x0011¬f*\x001cÐâI,\x0018s7SR5¢847)wsÃzoG\x0019fçýg'¨ÊÌk\x0018À[Y2ÄåQaYÎhâF8­\x0003\x0005KÄé MÉµr¢\x0002§YoÄ\x0003IV	÷mó£sê?&¼\x001bÊòsDm¤
µ´ûÆ\x0012(Å\x0015fDd«\x001aH4ØÈ\x000bl'ÁÃ>}ÚHà>Ö*Hê$ÒõæÓc\x0007</p><p>zà±u#c!ÃjG\x0012
¼{ÄÆ\x001bu3C/ÜÉæQÁVGT!dn (¹N\x0004ëËýì5»*PhCñ\x001c0\x0007¿ë18\x001a\x0014½V£ÐErbéÓDâ¥Ì=w2I¤í\x0013e\x0014»\x0007</p><p>fNéØ\x000f8D\x0012òË=J£ä¢D$}âÃ|c,­yvÀ6 Â\x0001í)\x0014Ñ\x0008ÄÍß=\x000e\x000fèôi\x001bbº¡P4­\x0013p<ÄûÙGÊª¤Dx®i??\x0006Rò:Qb÷Ø<ø¯:ßé~D"r\x001f\x0001\'|	êÇ­va ³evôqÎ#\x00002`Ú<=IL}¶á\x0005öÌ7ÛKÞ\x001a>fqPT\x001e\x0014úåA\x0011ëèv\x0014Â\x0017­(\x0001­ÈL¢cV¬Äÿ\x0015I¬G­Õì}:D¤ÏÊr\x0003\x000fáö\x000f¦5ÚüÒç÷O\x000fwî&"à\x0010Ò9ëµ\x0017\x0014õAf\x0004#^w±×Äë\x001fÎ¯-\x001fÞ_Ù\x000eÇZú4¹Z \x0003\x0008øê.'Ë\x0006AI}\x0002;Í#qh)¥O\x001bÂHJÚÈ°¸·$\x0018¸È$:Êõ[#Çh\x0017Í$pzÐ+5¬\x0019¦\x0013PJª0ë\x0019²í\x001c«tÔ6\x000enO\x000f\x001c¨\x0014GD+\x001b°ïgÎGÓ$}\x001aIà÷³FDp®\x0016¼\óæ\x0006ý\x001cnkG1÷ÿ\x0006£	Sêrm\x0014e¯ÁÝ!¶\x000eÉ®M,EJ_\x0013\x001dÃâCVÈÊ,´N\x000c%\"ÌÖ]¼\x001b&EºDû"£'sòwWK \x0018qëºm I\x0019ÚöÐX¢Ñt\x0003%@4fû.ÚMcÒØ´r¸\x000c/\x001aO)~à±ñkIø]4!Mh\x001f\x001bé(¤ïÒ\½¡ãE¼n³4Ð<ù?ïÞ¿_Ë^þñ>åt?L=ÏâõCÇn\x0008.V$êèÑ!ãÅFìçÔä£¦¼º4ÒDËG\x001eæâSè8xz"\x0005õ·â\x000e\x0018je;±âæÉÆÜ[Qb</p><p>UY5\x001bo»i>üõÁ¼\x0013é\x0019\x0008µ£}Z4\x0017÷O¯©\x0015éÄ3:mo
óä
çñEm×÷ÓÅùÕ«íýH\x0007(\x0012Ò§%r×p\x001cë¼f¼	l½$/o&ÌJ\ 
ÆÃÉK·5öÂÌç\x001eØvë¡Û\x000eUH¡Å\x0016\x0016oMF)\x000bFk·~;u°¬b</p><p>m,3\x001e\x0012K~\x0010Ê\x0019Ãì10¸§m\x00012ËáI\x001bhÅD\x001d,]Û\x000bóíöÛg±ÖòÅýçwSE,Vm\x0017éa\x0017@\x0014vKRÝF2ñóWÏ'</p><p>X\x0006\x0014«\x0016»(P\x0008_Ü±~Xò\x001b\x000c\x0017êê
W±\x001d£´§Ü=\x0018Ñq·Éùi4S<\x001aq#)¦\x0019#KµF(£\x00114§pEøÿa7Ó 1V	B;1¤(\x0005¹"¬\x000f\x000c\x0017rof¥4Sä6\x0001m\x0014¡PHÅgkb#Å¯\x0014l[(£àhH!cZ ¢PÌ\x0010òi[\x00181+¤"Eä|ÇÈ«3l$s·S¤\x000b¯ÂÄ¬*)x,ôJAÏÞ%ÃÄ­\x001cNd±%T\x001ar\x0019MÙ­QÍ>4¸ÉL\x0013G0d£%]\x0019O\x0006+Èl;FÄì6\x000c+\x001c'p\x0019£s\x0008Rb\x0006u,\x0012"³\x0003ËÓTã"Eùs\x001a
Ëv\x0019vñãºùÍ¤Ïv\x000cA¥F\x000cÏ\x000eWÒ<Ê.N\x0014±\x0014¨o¼!4càò&%Ý\x0018pSvqü>ÀàrH¥Ôº\x0005ßÌ1ð%þ£\x001cº¿ÿ\x0000{üöÎ$U4ª¨	ö\x0002\x001bÁÝMìÖÑ\x000bzÍ^Ò¤\x0003çk{¹¼õ\x0002û¾mQg«8ÇÙÂáe©»\x0008©X'¹\x000eØÐ#×]\x0004¿î:4s\x000c2üvs£IW\x000böTÊú\x0012Ásª\x000bb=õ¤\x0019£Ê6ax</p><p>¬E¡\x0000\x001a\x000e­¹ÎA¹õlV·Û\x0000¢
õG=\x0017LJ¥-¯7âjÍ\x001cxðHJ\x0001Ý= ÉÀØ\x0010XÏLéüÄaÄzÊV3Çª\x0014³e<B)µó-t¸ð\x0018DÙ\x00133Ì×Ú	Ïä¹ª\x001b\x0006("'\x0008{£æîZfÓ7,­`é®\x0005\x000bëR}Ps·J§Xë1\x001e~\x0016hÑpY\x001em1ÁÅR&¬AApªÖuj\¤±(µÍBêhq2l?16ån·r\x0004Ee\x0011ü¤cGÆ)õ8Ã§Ù\x001bfP\x0006Ú\x00021!gÆªâÒzv¼ÕsOAiA\x0003\x0008Ú6·¦ZË\x0004âÍÜ«Ð+O&\x0010ÅÏ7	b\x001epÌ«\x00022{D°\x000c<}@4\x0000Bòh¢rÕ÷s7¯ÆÅ>M\x001c^\x0018i"UÇ&\x000e½SùZ{÷§ë)}@à\x0014±\x000cÏ¡±$ÃD#2wójtmÓ§Ã±ªTZ!¾\x000cg\x000e»þ¬Ö\x000ea ÙºTM(Ö!*f\x0013c\x0002/Ù\x000b\x0004½¹ôiôROwV\x0003\x0002".Dñv#Û\x000c\x0007ªn=U­Q$`\x0012QùËÒÖ]\x0015ZâÍ7\x0013dÜpcE§*\x0018\x0002T0\x001dN¦Waî\x00192(Tj<Þ
ÛËëÆ"\x000b#¡|Ól</p><p>Üt¨F\x000eLE\x0014í¤­«8úO5sAVÀM3#ÐÉÎõý\x0008ø4ìØ9+fM5SÍkÕrêzÄß÷.ëc¸\x0004fU:r\x0013¤¥</p><p>aÊ¢=#Y\x0006¢w©>=,¿þe\x0007QÜÒävw­%*ä%\x0018'JÌÎ</p><p>[Ê\x001cëÒÒ|dWÝë>Û¡\x000c*Pr\x0001¨\x0013\`¯
ýu¬\x000bíæPQ@±</p><p>EÜÉ%÷\x0008Ç</p><p>»>p5f­ÖÔOµ2àz°b-6ìJ×S/\x0003Ø {Náª\´\x0003\x000b<@ÖqÂ\x0003He%HW\x0004ôÜZ:h?Öê`îÀrJ\x0015å ÀZqøN7u@£\x0019K~úû½ù0,[,TÏ¯O\x000f×\x001f\x000f\x001f¦Àd¿ \x0008Ï $È¢²ãXÏO\x0016W\x0017'/\x0017\x0017ßí&ÃV\x0000ÏÒ§\x000bÍÂ¥;zÀ²÷\x0014X\x0003Üd\x0004ç·ìÆ\x001e6-Rpì\x001fÉ¶Ê\x0002ëcSp¼§äE\x0014Õ\x0014E¥J\x001aIljËáÚ\x0005ôéÓ.7_Ã¢äºn.\x00018]§\x0011öÀ½ÿ|ýNþ>¬j.íh¯¿\x001e½yXÞ<Ü\O=cYq²^<ÖT²BDY\x001eàdGWÚÏ\\x001e½¹X^nkR4¤é=\x001c?½xØ"7d<iË{\x001b+²\x0001Ð\x0007ÀCûôéÄ³p¤\x001e®hÝÁØ9^w¢Î\x0017ð4}:ñPüt|l6Ôc°KlJøùC÷é÷\x001bwÿ0ÈtÀ¦E|-Ü^ß~º\x000eý\x000bNy@«Cÿ>\x0016«£\x0016NM¯éb8;9ûá|»6\x0000[uwj\x0007ÃX/ao\x000eÖ(á\x000b^­]ð³¸¨ã_\x001f\x0017\x001c¸\x0019\x000bkAé\x0004±++M\x001fúýuq)Ihy"#x;ÃÕæU¹?-m±ÚÁV9\x000b\x000eû=\x0015Ù5\x001e±àöçÊÝû¸£Æ\x0005ÎéÜ\x0007åúa+êêüy\9µ£s¼\x0014¿äÃÅÄ&z\x001dÔ\x0001¸PÚ¡K¦fÔ\x0019+æ:AÔ/b¹á\x0010\x000esPú°bß)Q´{"Ç
µSûoÈâÎu9Où¨ð|aZOeý¨Ð\x001c÷'£>20\x001aÅJïÈä-iZé\x001dùýÉ¨²½sÌ|QbRãóÖ³\¤vþ\x0000cFù=d¦¯(MKëÌsÔO\x001fb2
>öÙ \x001b\x0001ë\x000c\x001f\x0018®Î#ãÈAï\x0006 $\x001cìdÏq\x0016VQ\Ox\x0007æÐ\ì\x00053\x0005Â|ÄZËI[ºnµÔ\x0001öîóÍ»Ô¯\x001cógñ/ê·	`Ï\x000f×_§eÔÚR^e6ÂV\x0010\x00148¤:'\x001d¢¯\x0003vÔh\x0013eÑ\x0016\x0017'IM}¤×æÌ`#ôéDÃgªtaÂ\x0011&Yê0Æ¬!£\x00039öE+1ÅN4ã)/\x0000÷#f\x000fß95&Ëyh_ã¯ËeÀft©ÓgÐÏýÿþïÿ³¸ý{ªÃjØ\x0003jÚa\x0000I\x0003(XÖÉ\x0000§o\x000c
ÛÑâìÎ¯v\x0005ü÷Ó§\x000fÌjqé"Ê@ÏKN²\x0004«íÅ~0lÒ>`Ö>he¾¢ÜÍøÑÉl\x0006\x0002xó·Ì\x000f%iÔº\x001d¬¢(H\x0014À:9ì\x001d\x001cüdeä_x7LÛ`ùùËÑóûÉå¯¢¤s6j0eÉ\x0004ò½¥®-Æ\x0017?,^½9z~~1Ì#[GQ\x0015jEÑ,	ÅÌ)N¡Wb-Ó°EWÃ¢ÛÅG*+°Ã,#\x0002bí\x0011¦ÅT,¦EcÇ¢ìþÃ</p><p>fqpÏw!v´\x000b½,¶b±\x001dËEõ:#lÉ{I©Óà\x0017^\x0016D«n;Lîn`ðáÝ\x0011\x000c]ÅJJÝ;IÒÙ</p><p>\x0006Õb\x001ba¬ ÎI1iæpÐ!0¯Ê§`à·\x0016Õ¦Æ_\x0018¾	=\x001d½¹¿{<úÐrüÌ CäÕ\x0013$?XÉñ×«£7ç¯ß\x001e}GÏ6¥ÚÔÎ"õfUASòFÌXH¿TUcªæ)v'&Rp!¹¼\x0005S*3©\x0007\x0018S]ê¤uÑ5ÖQ\XóÛ)¾ÁíOj*R3ÔK:å\x0002B_o\¹T×§Ì#õ\x0015©G\x001a\x0007¬æ¶\x001eaÕ¶RÖ{3I«\x001dåçí(¬¡dRÁ|pqETcO\x0016¤¡\x001aÓ0sL-Õ:hmmeè¢N¬?\x0000g¬8ãLÎò¤­±)'QEÜWDU</p><p>VØ4Îû@!J½3hH\x001d7¬Ñ\x0018{Mî\x0003]]ÝtAÍÜù¥\x0005¢¶ÜPó*E\x0007@M¦è</p><p>5JfL¿à\x0010\x0016²\x001c§Æ³>¬_\x000bKÌB­\x000f~9óäGÔ¼¥Tp\x001c@	óÌEÿ?´>øåÜëP_6Ò4ÇÒÅZzïLÐÚ>1³STs£Ò\x000eåKMð\x001c-\x0013fÿ½ª8%åç:Ré\x000fÊúrEyÎ!\x0013k"góP]êæ¡ª@VPÆDDÁ	B\x0003 Ö'ª{¤:R´\x0008J®\x001eÙ] Â÷\x0018ãþ\x0017¿ª~5Óê÷mið\x000fòzQQì¿«\x0014è\x0015ªê9\x0001\x0014%x<WÎSs\x0018\x0011ÝÿøÇb¸!ªwü\x0003j`T¹B¥ôn¸ü\x000fpûããô\x0010ÕÎ4ý\x000cwzNÔå÷"\x001eÂ?Ñµ-­g\x001aÓÎ²¶íïÂ\x0002Éf4ë­\x00135VC:ÌÌëºü#Ï¾ÀwiÞþôò%Rûªq²ò¥ð5a¦Uà¢-ýäu¬vãôþ·¿­~;Óë\x000f\¨<TÅ\x0016µ= Ä\x0014ÿðÿPÒÚP±ó\x000cÿ\x001fHÁØ©
jüç\x001cªPV¿0Ls\x0002À·7Óm¼âm\x000fg\x0011+ì{\x0011Kÿz?ú\x0014ytòòìôr$¸ÇPj\x0008¥z¡D~\x001b%±\x0006/V\x001dÚÃècòN\x001c=ÄÑ8|Ó\x0018Ñ\x0003·¾\x0004øÑ\x0004¢Pf\x0008ez¡t8lpBY:y(|³\x0003eP¶wâ|\x0011@}[\x000e s[ò5\x0019ñf&7drLF³±h±s/+\x0015Á\x000b7þØ¾\x0013Ê\x000f¡|÷</p><p>ç\x000c\x0018u\x0004¼Î]\x0019)5oI!Tè²²hèâWaÐ Ö«V¨8½P\x000e1frÌ{;«µæ­L+?$\x001d¢wM)j­kXÊÉr ¸ÑÄPõIÞ{có::\x0011P.\x0013V¹ÆK©0ïµª:ÊeïY®U½ñ\x0012e9"µ¦dÜLUè²÷H7¡Hxa²*çöU¥çAU'ºì=Ò1C c
+ø\x0001ßÅj&Uu¤ËÞ3]\x0007ª.
(ìÈe\x000b¥´\x0012qÞ²ª\x000euÙ{ªcQ\x000cmAkK½\x0002µ6I38ª:Õeï±®bQ\x0013**»ØÜð\x000cYÇº¬uÙy®cë$*r2¦Ä ä\x0007=µV\x0000ÐLUë²÷`Wû_£Tæ®¬ý¬Äx~ý.*UìªódÇ\^KP\x0015;(§\x0010³¶ ªNvÕ{²K?\x000eã\x000cc#øíxÞ\x000eTµÞy°KT41\x0004e©6Ø"Ñ$ãx\x001dÂNªê`W\x0007;ü®<{cÁR×EüÎÌZêª:ØUçÁ×ôúkåR\x0012¬|a*7ËQÕÁ®:\x000fvø]Wb¦\x001c¡Ur°<s\x0016Uu°«Î]²V,\x001dl\x0003Ë² Lø,¤êTW§:,rª\x000b_bc,\x0003%æ­ôêTW½§º\x000bÅ\x0001\x0014dGcÅé$ó|RUéªóLØr^\x0010£*²(i\x000eÖÍ:>uu¦ëÞ3\x001dìNÁãË¥ªh\x000eH3ÏÙÒÕ¡®{\x000fuá8w®fQ¾¤ÙèY~©®NuÝ{ªGÉ\x0002vcá\x000eò%\x001e\x0004îò¬µ®ë\x0000L¯¹®d®NÅô\x0019Q,\x0018Ã
n¥</p><p>³\x001c.]\x001dëº×^\x0017¥Ç¬.ÆzÉéè¼g]åa®\x001eñ<¡`b.æ}±üvû4UN©
ÝÉ°¼È\x0005ô«;ÙÍðÙ\x0015J'æbÞ\x0017Ï®¶\x0017T\x0016J5¤Ts(½áwQ|w¦Ã+V´Ò\x001c\x00143@õ\x0010TÏ\x0001\x0005÷¢G¨bK\x0006¡g\x0005n¸ºÕæDÏ\x00005CP3\x00074ð
¥ùÃÐ\x0012\x000fçH)á\x000cJ;¤´s(#}À$ÆK6÷eÞ£Ü´fº!¨µ@mñz¥åHfÉÛ\x0000î \x001bÉ\x000f9ý\x001cN±òÎa}R\x0018Ø[\x0013ÊúÜ¼Ef!h\x0003ê<ª~dPÁ¦]P±vf³Lr\x0006h\x001cÆ9 Òrv	êÍ_Þ\x0014iÑúA\x0007\x0001H<éÅ\x001cR«Ë!*Y÷+\x0004ÉávûC,RYßI³.%aË¶ÏÕëy²\x0003¤8Ä*Õ½$g]Lklàò	ÆT¨2¦qÓVAZ]LrÖÍ$¨ËJ0VrË\x0017ÏÙ\x001aðoMh\x0006hu1ÉY7v%¤¢©ÑHðEnü Û^V7s5©\x0018©ñlÀNìl;\x0015éÚÑèë\x000cÒêj³î&°#GdW6Éêm¤¬u\x0006hu7É9Ê>`\x001eRM"FÁkST\x001eä(­.'9ëvRë^M~ÃÌCÊEüJCØ%²ºäë	Ç/|´QX#Ìk%m3AUu;©Y·ä\x00172ÃÃÜ°\x0018\x0012\x000fa5«êfRsn&\x0015VÝKäau§ñ<Ä^RµÃ4ëb\x0002.PÉ8xL¯P>î­=\x0008hu/©9÷r¥û­\x001c<mòÞ>\x0012AZ]LjÎÅ¤b(\x001dJ0Q\x000eüòkF3@««IÍº¼(r\x0001«¨¶\x0017G¤¼9ÈäWWs5aÁ-÷mðÞU}I Ð#ê\x001938«IÍº\ µë`X-RöïT<õ¤ªIÍ¹Ve °ï#§e{<h;\x001dfV7u39bAÔZ®ÇòÜ\x0013WjqÙ×ÕÕ¤ç\M*è2¦ª\x0013½R|=3Ì ­®'=ëzr+\x001cmÎ$ÏcÊ\x001d¥ôa.R]ÝOzÎýëT`PÁ*\x001d¼â­\x001fÄ!\x000c(]\x0007ôæÝO_Ãð\ÞºÊæC\x0011ÜCV÷u?\x0005Ö[\x000fVûÁò\x00055¦,5´º ô¬\x000bÊI~Bq":¤\ÑÂÅ\x001aöCV\x0017{A±\x0019ý\x0016(º£À8ó¤«+JÏº¢¬£Â1gJm³+Ê´:Øl¨êÒón(Í\x00013lUPNSîM¤åH"Ç\x000cÒêÒ³n(«Ùr6­\x001fTÑ\x001ds\x0008ê2ón¨R/n£àD"/\x0003K\x0003	1Í ­n(3ë*©.D®Äuû\x0018e\x000e1ù¦º Ì¼\x000bJ¢êB¶*é\x000e0¤¼¡¬?Äijª\x001bÊÌº¡*ÊâØÆÓ}8ÅX{eZ¿9Í»¡\x0004:­WËÔ³ÂÚa\x001c\x0013SÝPfÖ
%ûìc÷\x0019~À" ~$[i\x0006iuCY7\x0014\x0016\x000c}bEÉ¡\x0017Ü"Il¯\x0019¤Õ
efÝP²\x0014·z_j\x001b.âéb$Ý\x0006iuEYW×\x001c4CIÓÈcÊýÍAS[ûvVÐ\x000c3yò]ê±\x0015\x0003Ç$8Û,S[\x001d§vÖq</p><p>	\x0015Å¸ KúJd	\x0006#ã!&ßVuHÙxLI\x0011°¸\x0007\x000b6Rä1=ÈäW;ßÎÚùvuî½O\x0019%cÐÆ:Ì\x0000­¶µLy\x001c÷0¸ô¤ãâ§	#Z¤ý¤®ÚOn\x001de$\x001e&R4©\x001c'¯{>¢ö
F®IY%èúþ×ÔëtR\x0000\x001d5ãYÙ\x0015·?©áÊâãQm ËÔòtBÿé\x0011H#=tìØP4­d¿^«Qñv8]
î\x001c:¡ø¸´¡jÈ\x000fLzMC²ÎVt¶N\x0000&ÿ\x001d. òßWmkdØo^C5¯¡o^_éu©\x001f4_ä\x000bç×_¼}VuË@)ÚûÉ.6xùe%>\x0017=¿r¡ôXÖe7&F¥h/ÎO·7fa¾AÔÃSÔ£ÏGCïÑ+Áú3ËÒ\x0014¶\x0007ÚÏT|f\x0006_$¼Èf\x00149R¨Ø¹\x001f­¦×vOo¤°&ðY\x000ek¦WAâ\x001b­àïàó\x0015ïås®èeÑgFC§w¢·S\x001b_5½\x001b=vñ)}ìsÿco=ËÉIÅ»c=)±\x001b/Tx¡\x001b&£G_Gxù¢\x0018½4ù¤¨øR³Ö.@MU"Ñr0KCèÊ¬;.Ý|²Z~r£áÙ.>ÌèÉ¢¨\x001eK9ip\x000eÒ£</p><p>'\x001d|õé"{Uï³\x00180\x0001\x0006pÐ*	\x001bt\x0000Öçì>`ð-\x0001\x0005Gú á\x0015\x0000ÜÒÎ¨\x001dPÕª\x00130rÄ¢» ø	J5u×~@W ë\x001dÁ¨¹-O\x0010óË\x0014«Ï\x001aeg_Àz=\x0001RÛº%àåÝãòayw7}o°Ã(Õ¡Lw\x000e{Ì)âñ%øbñúíâbñúõÉND[!Ú~D\x0005Þ\x0007=2\x0007j¤\x0002NR©Q
£zz=6È</p><p>1È^FÏ\x0017\x000c^Qw\x001c¸TøA\x0004þû£]	\x0014%Èªu`\x001bdpÜ¬\x0013¯æ¬ã
®§¤÷%ëã¾nð¸Åü{!áLá\x0017Ð \x0004%¹z\x0014#HmÇ·t\x0007¤©V¤3ÝKÒ"\x0016T q{¸¤9\x001f\x0013\x0015ëöRÕ;[ªnJAº|øàÉ9ñZ^ä[ÌÃ\x000eH½\x0006©g@ªkj!¯\x0018_´}ÜÒÐ²Ñ¬1öO7ÜìÇÔ\x0007\x0019Ü¨Óê\x0015}{\x001e@ÀdÖ\x0018M7#jxQs¥(4\x000fn\x000b\x0017}-Æb\x0007¤]\x001bÈþ£\\x001aEÚ\x000c0Û<\x0002\x0018IU¦{ïtk®\x001fÒZ*Ò)zä\x000b'ì=q1ö3JOq\x0008F\x0013\x001fåªým&Û)ÕÚÞVý{[8.í8óÀ±°c=²¾\x0015Ó?÷QêÔ>²\x0010\x0007sû­ûQ\x0019Ü\x001eJmkJmû)M`gA</p><p>ö\x0006½\x0000'O¡½OJcuEÿÜI\x0019°Ç#\x001dAQßdÔ\x0019â³Ò</p><p>uöQÚ5Êî±DÇÐÊ2¹<\x0005w»á±tãq§\x000eJ¿Féû)±_«^­Ë\x0004\x0019"5áe9*%Ü\x0006	÷¿«BY,w*¥×_~\>|¸¹Ûõ\x001eDo\x0002\x000e\x001c@ï,Ë'ÀL\x001b©Ý½<úqqñÝéëÈ'£©!êC3¤lý\x0016Ë\x000b)Ý·ìHù|\x0007\x001eé.2St\x0002(¯ÒÎ¯\x001e)F^ÑzÐÌ\x0010Ít¡ÉP²zôJO\\x0019¿\x001f\x001dÙ.2ÅaÎ¼ÒX\x000eH6R]Ðæh®\x000bÍùU£7ËÚ«\]¬ÔØÌ\x000fÉ|\x0017\x0019ö(¦>²XÕHÏµÊ\Â1aÃ\x000e´8D=h2\x0016µÔV,nc/´Mhn½{\x0013\x001bo&\x0017ËowËÛ\x000fS}zG)ÈtðÂE)\x001c÷§\x001c'%ýöÀðÅâç×³ïN§ÎÞõw'¹öîÔ\x0019$»%\x001e3\x0006-½î\x0004~=fkøp¹|xýe\x000bã @ìêõ\x0000q\x0003¤pOè|U;\x0004k-wÉr£Pú\x0006s¨Ý ëØ&P8\x0000\x0003c\x0012Í)=´\x001b?îãtÕÚÜ\x0008'6Í:ºòB\x001a{·ä läâÖgÛ¤Ûz,í±4\x001e{9æwGáX­PÀÁ\x0019ÕzþÍ±\x001cÄÃ\x0012gÃ\x0019!èdàÒJ\x0011\x0005íteÝþ ÎU øý."µ\x000e\x0013q\x0002íu~)UQï¿\¬V§sV§àvÉÑÅ\x001fÍ$øÉyÿ\x0001õ\x0003³Õa&9cæ`§Ï9:à=Ùÿ0[Lë>J[SÎYY\x00175QJu¼)ðÈGItrªz4ÕÑtü\x0012èd	\x0005a] Îg\x000eÎz<ÕñDKZN\x0015PÃ¼®áÊÜ\x0005ª«mäõ\x001c\x000bÄ\x0019~yÃ\x000cFr\x0014\x0004K`*­\x000f1ó¶\x0006]\x001el\x00025«\x0014\x000e	¹\x0012ÏO\x000c\x0001\x001d\x0000³x;gâU¥<Ëü.øÒÔãíØ:9C½Â$J\x0007B2=}\x000c%cGoOéh\x0006
¢÷ æÌ»`5Ôàùñ\x001fAÓoyïêã¬Mä9'(ø\x0018=\x0006ëÓ³á£-\x0019F[\x001ejº8e=ëy</p><p>MQP¾zôÚð\x001b\x0003\x001cG¼8ÀÖ'Ss2¹¢¹\x001e}i\x001bâ£¦Üjù\x0003ØÉ¡¶AÃ\x001c\x001bÔYÃ&Gá;Z¡\UÉe\x0007\x0018Ñú\x0008
sP«\x0012óÔÇ\x001c®ò!Ú2ófÿË3øs=«\x0013#DÄnq@\x0007_²ÍÄþ¦]¬·|µåQ\x0012¼\x000f\¬y\x0006\x0016õT\x001bÅ³@u
ºúØ\x0004*¸::|\x0018Ë¯ÈÁRQºRÞ\x001d\x0000´ÞJqÎV²au{\x001aê\x001eàÖdª0\x001fÜÇi«Û\x0013ÿq\x0006'?ËÃÁéÊÌkNøRî\x00103_»sq;gQ¼9Iï\x000fK\x0014p<÷?B±\x0012{éç'&\x0010dLmIÎ\x00070µì¶'Ð5p5[GQcPöiùx½î\x000bV:Ê`j\x000bÉ5ª¢.hG+\x0011X¼=YLõ\x0003²ëZX¶ÖÂÚÍeEiR\x001d@\x0008L&ÕcO#ídÄ\x0010[«</p><p>í&«k0\x0018Ç­Ù£dao7"VÝAVê\x001a3SÄY°1\x0019WéGVæ[ô\x0004\x001aÉ\5f®kÌ°£çÅ#J?W¬~ÙÌWd¾LEQTÁ©añ:>7[w©LõyW4/zß.¥\x001fy}h'ÕÅ®1slÄ¤¶ì²è*±Ò§\x0019Wh#k§F×±½¨\x00147¸\x000e«\x0017ÕÈò³`tìV\x001f\x001b²ëÜP\x0000@ïÚÉÒ~Æ\x00179ë8ZS×HVo\x0001Ù·\x0007`w²þ·VåqP¦\x0000Bï3h¡ÏÐ5YC8¡	G9¡ÆKMø}¶ç \x0007l:leÏ¨IÇ2Vônm(-ÊÃ{\x0007Z}\x000ftí\x0002ìò\x0010ó¦Ô9$oci ìä>hkWT×\x001dz\x0005hB+w\x0014\x001a÷K·{M¨©ÑL\x0017u,Ç£-âü®ôG7ãhõõ©ºîO	²Üd<RJ\x001089üÜ+ÜH?´v´úðP]Ä¸\x0000ÉRYrßÅúëO\x0017\x0016\x0015\x0016=dà\x000e6ÒÑðk\x0002×\x000bç÷A«Ï\x000eÝuvÀ1ô ¼)Õ¢\x0019W)jDÓ5îBsEvXÁ1BzÆ*>ÖÖ\x000bâ:ÑlÖ³Ae\x0017XÃ»)BÃ0'£\x001a\x001fh¡\x001eµÐ5jÒµ\x0016,?ê".,Æ²X\x001aÐÀÚ[Ë13Ãf\x000co\x001e®¿¾ûöxý°«é\x0008ÝSÞR+\x0016)sÇ</p><p>#ÇJäß\\>ÿùíÉÅlÖÓÌÌ°	C\x001b£ë=\x0016	YëÙZ³qÌaéAÓC4ÝæW½><UÍ\x0000\x001d§sImÆ\x000e\x001e<3Ä3xøMM?À¡CÄ\x0016Á#i÷Æ³C<Û;zûâa;(y¥&
Þ\x001e<7Äs½£gX	\x001d?rã­+'fßÑóC<ßÇRå\x001a»Bz¶EØaVjì¨ë¡\x000bCºÐI§\x0000FgèÅÒ\x0016](9Öò·\x000f/\x000eñbÿÒs4·Fñ\x001dfK?#9zOtÐ
\x001e«LÕ2¡
\x000f3XùDÖåÔ3¬\x0001\x0004£»ç±'ëû¢÷Â(	èAËak=½Hoólzøª\x001bCö^\x0019Fø+1\x001bk\x000cÏ¯\x0016û_u.ËÞYsÁjê\Å\x0004?ïI¹^±ÚÏW|²÷èSú8Ð½f5÷À°¬y\x0000|ûî^Y\x001d.²ótÁ\x0002±°</p><p>â°	\x001a%ï\x000fLÞÙOUûWõî_mJÌ\2~¥\x00047È|µEÕ»?`R)Ù\x001bÕ/U<g$\x000f½¯Ú\x001fªw \x0010\x0008í1Ç-\x0003\x0011Ft=|ÕþP½û\x0003æ7g¤"Î|\¬({þ	Å|\x0006¢\x0007âY]|sÿôË/7wÛñ<Jnè´ü\j"Ç\x001füÏ\x0008OGøõ-%ÈçWßúz\x0017\x001a\x0008\x0006\x0003Ò¦\x000b/Yw¯³B¥\x0017%-`l¦3Al©Ol¤\x001bê1 è£sÞH\x001cæ¥§$&À£\x0006pBØRN×çj<×g\x0002Y¥\x000eüìü­Y\x000f\x0004ñÂ^xZU+O«¾¥\x0017$ËÀÙ\x0018²/	xÔL\x0003ðßRæ·\x000bOú5ù²\x0014Ñ^
ÞÓÑåõûû§ÛådU\x0004V*qÑRÑÚ°\x0000X</p><p>6Æ\x001e[¯.O\x0000ðl1U\x0017á×\x0004Ì¤¯\x0004ÌÚøa¥+LX!ÃÅDÇµ.ë}n»ùt5~º{üÜ/Rv</p><p>\x001f%\x001e\x0003ß¨T\x0007­øl/\x001f\x0018¦\x0005I}©pÜ^ÇÑÊÈ\x000e>Wñ¹^>-P4/ñaÖ\x000c
\x001fÛ\x0005F\x0016ÁvàùjùùÎå'òMxÁò;	|¯\x0019%ö\x001b>)Ö¶o÷ú\x000bl8c¢!\x001bÎ«\x0019\x0015\x000bë\x00004Õ\x0000\x000ek\ÚF0\x0014DLÚ%@ãY\x000eÂøÑTÈ\x000eÀzÈî\x001d"\x0002å<\x0007íiY°(Qµº\x000eÀX`ì\x001dAØ\x0017\x0004;£ã¨±,ØiåXÚN;ª ê]É÷È3e\x0018Tóg\x0002\x001f1i1î\x0005hj@Ó
X^¸)m\x0003Pf\x0000Ý~[DÕ[Duo\x0011lj¡</p><p>\x001fKM\x001aÅ².nÔÀê\x0000¬·êÝ"\x0002c¥4¶421EªÀz³0xNK¾\x0017Ð{~SÃ/ÆrØÙ®»GÝ¡\x0006\x000c½(IAA³ÿf¸µº£F`\x000f_½\x0004Cï\x0012\x0004#u¤\x001e´aX\x0018Ç1\x0007¤\x001dO5#«{ø\x0004ë\EQÂFó«\x0007\x0018©ûYZVã§eïøiÅ
rCä@\x0010#>±ß\x0011­×Ô^+U`ø%oà¨,I\x0013\x0018Á¡q7.nÕÁWºû\x0004\x0014<¹\x0015´\x0017'×ï9zµª{mT°qY1;j\x00160\x000b8Õ\x00048ZÅÓÁWÛ¨ºÓH5\x0011Õ3äNxº(9å÷;M½yMçæ\x0005<Áº\x0018Ñ\x0016\x0017N+Î\x0017të\x0018ý¶\x0006ì\x001d?lÅLÓ[,T-¸±3j?\x0017ÎèO÷òI-c1Ø¡óöU.òöµ{.@S\x001bX¦ÓÀ2Q[G\x001f8åLùH\x0006\x000b{¨\x0003ñ\x0004h{GP\x0014\x00135ÚÒIq^¨ÛÓ\x00004µu`:­¬'o\x0018K Ò@ââ\x0016´©]\x0010Óé\x000b$Ù\x0005¾ÔÊXV 7û\x0019\x0008±ÞÂ±w\x000b;ÅQ\x0005OÙ^I*ñE;ZÒÒÁWoáØ»Q\x000c%a¢F<ª¶ò,î\x0016Ã¨¼[3 µ\x0001(e§\x0005\x0008¦¨aB°±H\x001d	\x0001ªm¤Ü/Ò!aµÔ1v\x0012ÚÈ\x0005kÆ9cÇ^\x0008\x0010Î\x000e\x0005\x0013¼W^øÛJÙáûå\x001fËéÞtË¿P¿X¶T§\x0006×àx\x0018úûÅOl8QÂ¬gwÂÁeeI	n¡æ-å\x0004\x0003ÜxÃf8[Ãu\x0006^ÒÈEAeI0rä+LbÛ\x0007NÖ#';GÎ\x001dX;xnøJGN>\x001b/BkS5êÓaä\x000cWüÀ¡B{ÖÊ-µ­põ´ªÎiÇ¹8\\x0013²(Çp[$9\x001aÙB=p¡oà°TØìª¥\x0014uu[JáÚà¬\x0006ÎÈ®3î2/¤l
P%¾W£7m3­Él\x001f\x00198\x001a*á}G-\x001aÖ\x0005Auì=Øl¨Ølèb\x001dIU\x0019NQß½(\x0002«gy1\x001aÃØ
'×\x000bó$\x0017æUe__¿N</p><p>=E|ÙÍ6:\x0005EËN¸\x0000ÓoB´âÍâòr²úÒ®É?&J³Þb7'¸Ý:A{-r¬@¨¨\x0015£Ù\x0013uá\x0003{9aV»·	\x00136®'ÙÃ¦8öéI_`\x00048ÝØS#g\ãÜ&Ú=àgíaÉáùýWDÉØwkoÌµYßÔ¤ÚiØü7d\x0003\x00150
©ºÁy»å\x0015½Óz8í¦\x0002HÃpø\x001c\$*;r8ÓÚ}r
sSXc7&xÄfÝÅ\x001cïÅPVç U#§[ãÜuÛÍé8óÄ+\x000caÒxÒó+ê\x001coí¥Ò¹¶:G\x0014Óvbâ\x001b]n\x0017á\x0015ì'Òw&a7ßÞ{4Ý ÷Ø¦\x001b¾\x001f\x0013\x00035´:QUÞeNK¥áX§9¡XÐÈ©êYwJ»g=\x0018ª^ôÒkÚE2%8'N1)¦ÒÊi×8gL;¸Ê9óÈËHO³Ài\x0018sôQ§Ò®æ¦JÃâôÒì9\x0003¥i¶·;kæ\ÛënÆ^(æ1\x0015¥`â&â]èímÅ1ý\x001aæ¦àKÃ¤[JUöhþJÞDÔÓ\x0004{O\x0008è´qúµÈÏ¸$éùèÄ$%G^3§Üß\x0000ñkËsD+m7'\x0018Æ¹\x001aÛ\x0010çà¬RSþYSj\x001a­a
3tc*áHïÀÃ}ET\x0000Ó/</p><p>öÅ\ÛD~Î&*\x0015\x001eNI>âSA\x0018
çô\#çyìûÍc\x0018NA9\x000f\x001e<,@0ÝèZ\x0017f\³b¿äP\x00191\x0007	¼ö°d²?l =¤öÚBQ¬\x0015\x0002¢9ÿìÙégÄJQÇn®þ:zñézJ\x0011ßªXZûZø[n^Âóº\x0016A=}d)òøÓéÉÕ\x001f½øádR\x00148ÕSÍáíí©eEdBq5¶u.â\P=\x0004Õ3@u\x001b\x000cÎ8në-g³l\x000f\x0001j f\x0016(Ç`D}	M\x001a~ºÔuUÏ\N;ä´s8±ã*É®cw?</p><p>\x0004ZÇYB\x001ddº!¨\x0003</p><p>\x0006\x0012%êXì:O\x0003\x001a9ÕI+w\x0010P?\x0004õ³F4rÎ\x000b\x0013v¼+y²\x000e'Í\x0005
CÐ0kDå±¦\x0004n)</p><p>hd9ªõ\x0018Ý !i4\x000f¼\x000e¸Ó\x0001doî\x0012éõÍíírJ}ß{Ì¡Èá\x001a£=W`xÏ'½VµÐ$P½:}(ONÏÎ\x0016\x0002üz½â[§o\x0006¼þzôæúáþÃÍdOe]Ú\x0005\x0003{fà,\x0000ø÷F\x0001O.Þ\w:ÕVY®wMÔ5±\x0013\x0011\tJ6VR\x001a\x000fE¦d«?\x000bÑV¶\x001fQp\x0003\x0008ã,\x0016dÆÒØQÕËq\x000e£©Ñô\x000f£+ÒZÆzÌ\È3Í*°.õÞÕ8þq´¯H\t\x0007ÉiÓJ\x001b·/£«ÆÑõ#>\x0007Ü¸\x0015\x000cyë\x0005×³\x0010«atýÃè<+\x000e\x00189ñ#°å¦Ö2gæ Æ</p><p>1v#\x001aLhÌ7"¾\x0010Ð±Ã×Êú}	%\x0006;\x0011%»°\x0018Ë#(&+ób¬{¡ÎT5¤êÔ´\x0014 ×ÍÀ0ì{z\x000f^C3aÿLcy\x001aù\x00110éäGÄÒ\x0006\x000cõ½!ë³Qö\x001fÆ</p><p>®$6Á²nRÔ\x000fðµl¸9õÁ#ûO\x001eã\x0005\x001b=\x0006|ËD[óbaû~ªÞ5ª×Xi¸ï-=9+.Â­lm7ÿ*K°¶yÒ­XÙØíí~Zó\x001b\x0007+KaÉJXL­\x0005	\x0006¦#6{;Ò\x00072k>-â©N<¸ÉUn¥Õbx·¬\x0005©gÐé!î§s´KÊ#Ð±\x0013ûÒ!é¤3±\x0002¤.r\x001eÑ©µft3ðì\x0010Ïvâ9Áéò&¬ðÜà¸Þæ]µâ¹!ëÄÓ,ÿd¢/b\x001e©Ôäø\x000c:?¤ó½ÛÖpE\x0001gex+fÜwnÃ\x0010/ô.=Ë·\x001cÎ­¤aËÌnsG\x001bá\x0006é\xäÞm«9\x0013Øø\x0012Ë³
ÀfÝsåÉêÌ½\x001ex¡tû:Á\x001cë9>\x0002®É¶øÈN<µæ%§ÊløoÝ.ß'¶ç÷OøÏn®§ç·TÓÙ¸£4\o\x001dDoÎ\x0016/\x0012àóó«·øÏNO\x001a0Õ\x0010SÍÁ4¬·\x0004Gñ1\x000bÞ8ÜÙZÐh&¥\x001eRê\x0019ÊàÝ\x0007³´0²u[´®Ïéfif`¢<O1E>\x0010KÔÎ\x001ebÆí\x0010ÒÎ4¢°Å\x0001¹Ìp;Ó¹Bý\x0007ÀtCL7gÊ5çaóNË\x000b\x001cû¶~\x000fHpî\x0010lP.&Pdíaæûû»ÇíÆê@b8^\x001bÍ-L r@M	·=Ë|þúíN<SãN<«(\x000fÜcÌÎP_\x0008\x0019é¥PmKlÄs¡Âsë¯o;ð°Ï(%¦¥ö\x001ayô°r"ãaS¨}ðo×\x0002\x001b¼uâyÎ\x0019öØª&GD`)YÁL4Õh¢5ÝúàN:NïrÎU
püöoð¡`\x001f:UÓ­çÎì¢+f+àIª\x0014óZ\x001f\x000cÞö\x001dx*k¬B\x000cV\x0015=ë¹¼Ta2ª¸3,GADQÉ\x001b/#:»\x0002Çsq:©\x0012\x0001\x0007[Cak¬^@[Êdµ*úÅRÄxëØ\x000eÀA²(ÉnÂ 0\x0006\x0008%=è\x0015\x000b v»ï\x0001´5 í\x0005\x0004ó;V ®u\x001eÂ(¸ý®ÜÒ0¶\x0003q £Jö.C´dÌjU\x000e|$	If;^PÙhdhd'"j\x001diÒkÔôÊ¢4ìâIáÇ\x000bÚÚ\x0011mhû\x0011Ý1Ëø\x0007ÃEimÑÊ\x001fm\x0016ÚCèkBßM ¬\x0016\x001e©ü$J_Dß¼ßwcµ[TìÝ-¨yD²¦Ê²\x0014¹\x0011\x0004\x0017m¼f¬\x0003±Þ-±w·¸Um%VBåXHT\x001f\x001eáÈÙ\x0013q¨¾ ÖÕ\x0017\x0010ñ%dþ­ §9*Qdþ±÷ËõÍ'úGmÖ|,æVåMO¸-\x0005Í®\x001eE×=¨\Ak\x0011uö
\x0017½\x0008qK\x0019r;¢®\x0011u7¢\x0016T¬\x00100G8·­ÖÐ«£\x0008aT'±\x00031új¢£ïh\x0007Ç\x0014I9\x0006Ì</p><p>×\x00191rèPà=3\x001bÑf½¦Õ¹\x0010qx.¾yº~ÿi;1PpÎ)\x0019²«\x00019AZJ\x00163^\x001d½¹:yñÃ.4%+4%;ÐÀ\x00139ªéRrz\x0006#¹}\x0004\x001b5­ÛÀäð\x0014L¿}u\x000cî"Ãò,p`±{NùÕÜ</p><p>@ Ç\x0015,Ðô _
üç\x000e´ÀMÕ,vÅ6,FÅd£
[Ñd=jµìÌN´¨èm\x001bFÍå#Oi#s\x00022²m9Ov±uÁé@ÓLöÓõÝãÑÿû¿ÿÏâéq9%~½Ø³³é°0õãi72nfýtòúíÑwG«·)\x0005Ì°Ö\x000bI+\x001b¡T±ÝïRë°/jÏD\x001aG½ö>Òa\\x0006¥\x0004õ,T[\x001e+vÓ\x0013¹\x001aÆÄ2\x0000¨a¤c\x0017ª­Qí<TË²WiTsÒñ±\x000cê\x0016a³FR¿®Lí³2õ0nùíë×åSï-ýe}fÂp#Ü¨·fú-~¾¼\L¹õp¨^bvq\x0017!Ù³á\x0000×¥"ù5\x001fdBo·¦Ë6\x0012ºj\x000c]÷\x0018J>%#\\x0018:&kyÛkh+¡¯ÆÐw!öP¤1ô\x0012D|`¡Qµ®ÚO(EEJïû\x0010s.Z\x001eDC&¬÷\x0015>yÏE\x0014ëMqÄ )N</p><p>}½X><Ü\ß<,'ÌCØ»,D	_ôlë8|£Û\x0014OÁ¯\x0017ÓÓÅnB5$TÝ)°ÊT"!»Ò\x0003\x0004»oïM¨ºP\x0008Ñ\x0019_Ò\x001aåé{¤eZ/¢\x0019"~D_Ò½ÀQ¡^x`ysÖû¢\x001d"Ú^D,Ã%KGÐM­þ^<7Äsý#(K»pA\x0000\RF\x001aùô"ú!¢ï\x001eAÏDè9ÊÆæÖ´Cæ !bè?n(ÁÆDVÁ³0ý\x000f8äÝCh,k[|'£'f\x0005Tq¤çK'á0ÙaÐ5§\x001d\x0011{YR&\x0004ø5Áòî\x001b=Ôç0ÖJ÷­"WA\x0007,[Rô\x0006Î¯¶r¤óF/au©Èî[\x0005ûò(¢\x0001F)-;kk1Ò¹±:³e÷¡-M`
>\x001blIæã²Y©Õ\x001e¶ëÑXYGc\x0001\x0013Ü\x001fî\x001fnþ¾p\x0008à\x00044TÁ\x0010Qk1¿>FL\x0014"áõ\x001eåå\x0005íèóÓÿ9r\x0007äz°SÖÁÎfÈ"Y\x001e#\x0016tû\x000c©=k>ÙQ§¿\x0003\x0012åò\x0006I=¯\x000f\x0012.ÏoâÄ\x001dQë:CÂQ¹¥v²\x0001RzcKt\Ù¥9\x0003öý§ëûÉ²\x001fì?éH¥\x0005\x000bH_¥+\x0005öG\x0018µis\x0012ì\x001fN.Î§KrÔÎ"5bÜ^eo&\x000b ¸¢Ý ô\x0001HCE\x001afjI	v^\x0006{,¦~'¬7°ö24TzöÅÜA­\x0017I\x0006Ù0b½\x0017*Ì|\x001d\x0001Àmð¨!»·ËÉDm'ÌÊ\x0014\x001c\x0007#
J;ª}s´xýòlq1¥øðÙ}À^á»\x0000ç\x001e2p-&-\x0002á\x0012\x001fM5ó
ôo¨ÜÄç\x001c6À%\x001d:\x0014iÌâAÊCÀ]\x0018;Ó[ñÀ\x0012Õðá?÷_DÓ'\x001fèÖr[ãhYÿ\x0015»\x0005=\x000eõLð¿ëS¼ìcD?:§Â¶>NF\x0010·È°£¡ù\x0006<rÖÔàA\x0003)\x0007\x000f\x001a°_-o¯ï¦+\x0019b(¾\x0002¶MÍ\x0002ØÑIÁÝïÜxZÎåÑ«ÅÙÉëéjèy\x001bàp
ÓZ\x0010\x001dvF«÷\x001c1¼^?."Ù'yP«S,B} ¾|XÞ}bÄ´NJötII/\x0005nU(R\x001cfMH|x\x001a¾¼Ùn\x001cmÍé%¹ñlt&û\x0000é\x000c½\x0013Áb\x001c\x000fµ@</p><p>¹E\x000eNEô\x001cLÝoSÛÄúcA¹%`\x000b*ª)\x0003ðo?c=\x0007+÷çgË÷×_ò·f\x001a6!u\x0013²ÝPÎ\x0006ôñKÊ;eÄRéc¶ô¸Ù\x00055PDë]\x001dvBÓB\x000f¥)gHÒ£=\x0007ë¼\x001e\x0010ßÁ4lâöµì\x0019(¿JPKj¾ôJï]É¾WãïË» êÙÓ]³çQ\x001fEÓõ\x001fFaê\x0004«moTÓLRÖLé¡Æé<ðÇCq\x0007¼Rá\x000fJî[º\x0012Røïo7K}\x0013)É0¥\x0016j6r1o¯\x001f\x001fñåÒsÁ¹}ó°üps·üH("a1¥0É©ãÈða/E\x000e©</p><p>ôÍÅâ»Ó×ËÕßº6r6ÏNÞ¾=yöþþóç§»kþ¿\x000e(]?¥.[ÇH©ó­s*\x001bBâ\x001bë %þÓ§{,a\x0000S$\x001dµßcÎ¨QÎÉ¤ð\x000f±³£\x0017g«ÿÞ\x0017\x0013­ôéÅ´Bd£\x00040]zmN6G\x00013uº<£\x001f|Ê·'ûgz\x0010MnP\x001d³,\x0013¦àZ<÷\x00104ì²«äÉ§ñÄ4úyáÝ_¿Ä§gJ\x0019á)\x0005h·S|(	\x001esFK×t9ê¡,Üüpì-^¿z~²IwB4³]`©GwútÁlfé\x0018²;¹ÃrÑDfÃ1|Fa"`è¥S¿«O_o\x0006`*¬Ïí§åãòæãÝõÃòfr[cY²¡Øº'AMgÉéU`PaÑ\x001b®Ä7gç[×á\x000f·Ó¯O.\x0016§Û¦Yþ¼´ßþ\x001bC>ÛXgË»\x000f\x0013\x0002\x001bÄÐñãE¤ü\x001fp0Ó­«	s\x00014¯¿\x001bê¶\x000b\x000f¥õ|7Ò|;O&\x0000OÑ>1:¹ºàKRéÓ\x0007(UÞ((I¯rX\x000b\x0000ÉFFCê@ã§p(¹¾\x001ewñ\x0005Ø..ãiûDÃ\x001eqñ"ÔAøÐ¥J>>ðÏ<\x0001*C´EÕ\x0002Löñ\x001e÷>»,q\x00023aÜð°ysýõ÷§ÉmlL*ÌÊ%e1¿ÏÂõlù$ÄWÆÉðÍÉå¿®¶nÞ_¯¿_\x0001\x0013\x001bB]²»¼K®Ï\x00168å
\x0015ãé (\x000f$9\x0013\x0004n»A°|Æ,^ÞvåG;ø4f£¦O\x0007 \x00162äTa¸å¤ë88js§0%r?></p>
  
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

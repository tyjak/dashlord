
# ZAP Scanning Report

Generated on Thu, 20 May 2021 04:03:23


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 5 |
| Low | 4 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Hash Disclosure - Mac OSX salted SHA-1 | High | 1 | 
| Content Security Policy (CSP) Header Not Set | Medium | 10 | 
| Reverse Tabnabbing | Medium | 8 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| Vulnerable JS Library | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 10 | 
| Absence of Anti-CSRF Tokens | Low | 5 | 
| Cookie Without SameSite Attribute | Low | 2 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 6 | 
| Base64 Disclosure | Informational | 10 | 
| Information Disclosure - Suspicious Comments | Informational | 13 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 11 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 5 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 9 | 

## Alert Detail


  
  
  
  
### Hash Disclosure - Mac OSX salted SHA-1
##### High (Medium)
  
  
  
  
#### Description
<p>A hash was disclosed by the web server. - Mac OSX salted SHA-1</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `010101010101010101010101010101010101010101010101`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that hashes that are used to protect credentials or other resources are not leaked by the web server or database. There is typically no requirement for password hashes to be accessible to the web browser.      </p>
  
### Other information
<p>010101010101010101010101010101010101010101010101</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage
* http://openwall.info/wiki/john/sample-hashes

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.numerique.gouv.fr/uploads/DINUM_SchemaPluriannuel_2020.pdf" target="_blank" rel="noopener">Consulter le schéma pluriannuel d’accessibilité 2020-2022 (pdf - 1,7 Mo)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a style="color: #ffffff;" href="https://www.numerique.gouv.fr/dinum/" target="_blank" rel="noopener">direction interministérielle du numérique (DINUM)</a>`
  
  
  
  
Instances: 8
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=?|>>?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=?|>>?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library jquery, version 3.4.1 is vulnerable.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `/*! jQuery v3.4.1`
  
  
  
  
Instances: 1
  
### Solution
<p>Please upgrade to the latest version of jquery.</p>
  
### Other information
<p>CVE-2020-11023</p><p>CVE-2020-11022</p><p></p>
  
### Reference
* https://blog.jquery.com/2020/04/10/jquery-3-5-0-released/
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 10
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-horizontal login-form" action="https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp" method="post">`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form class="form-horizontal login-form" action="admin/mail/privateMailPassword.jsp" method="post" name="requestResetForm">`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-horizontal login-form" action="https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp" method="post">`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-horizontal login-form" action="admin/mail/privateMailPassword.jsp" method="post" name="requestResetForm">`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-horizontal login-form" action="https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp" method="post">`
  
  
  
  
Instances: 5
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "JCMS_login_16214833906770" "JCMS_password_16214833906771" "redirect" "JCMS_persistentCookie" "JCMS_opLogin" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie Without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr](https://osmose.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/](https://osmose.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `JSESSIONID`
  
  
  * Evidence: `Set-Cookie: JSESSIONID`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 16
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `evAl`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Fjalios%2Fux%2Fjalios-login.css&css=plugins%2FAgora%2Fcss%2Fagora.css&css=upload%2Fagora-custom.css&v=20210511224258](https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Fjalios%2Fux%2Fjalios-login.css&css=plugins%2FAgora%2Fcss%2Fagora.css&css=upload%2Fagora-custom.css&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/robots.txt](https://osmose.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Fjalios%2Fux%2Fjalios-login.css&css=plugins%2FAgora%2Fcss%2Fagora-private-login.css&css=plugins%2FAgora%2Fcss%2Fagora.css&css=plugins%2FDINUMThemePlugin%2Fcss%2Fprivate-login-page.css&css=upload%2Fagora-custom.css&v=20210511224258](https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Fjalios%2Fux%2Fjalios-login.css&css=plugins%2FAgora%2Fcss%2Fagora-private-login.css&css=plugins%2FAgora%2Fcss%2Fagora.css&css=plugins%2FDINUMThemePlugin%2Fcss%2Fprivate-login-page.css&css=upload%2Fagora-custom.css&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/images/jalios/icons/ajax-wait.svg](https://osmose.numerique.gouv.fr/images/jalios/icons/ajax-wait.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Fjalios%2Fux%2Fjalios-login.css&css=plugins%2FDINUMThemePlugin%2Fcss%2Fdisplay-page.css&css=upload%2Fagora-custom.css&v=20210511224258](https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Fjalios%2Fux%2Fjalios-login.css&css=plugins%2FDINUMThemePlugin%2Fcss%2Fdisplay-page.css&css=upload%2Fagora-custom.css&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Ffff-sprite.css&css=css%2Fjalios%2Fcore%2Fadmin.css&css=css%2Fjalios%2Fcore%2Fbootstrap.css&css=css%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.css&css=css%2Fjalios%2Fcore%2Fcomponents%2Ftopbar%2Fjalios-topbar.css&css=css%2Fjalios%2Fcore%2Fcore-theme.css&css=css%2Fjalios%2Fcore%2Fcore.css&css=css%2Fjalios%2Fcore%2Ffont-icons.css&css=css%2Fjalios%2Fcore%2Ffonts%2Fwebfont-roboto-condensed.css&css=css%2Fjalios%2Fcore%2Ffonts%2Fwebfont-roboto.css&css=css%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.css&css=css%2Fjalios%2Fcore%2Flang.css&css=css%2Flib%2Fanimate%2Fanimate-custom.css&css=css%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.css&css=plugins%2FJLearnPlugin%2Fcss%2Fjlearn-icons.css&css=plugins%2FJLearnPlugin%2Fcss%2Fjlearn.css&css=plugins%2FOsmoseImportPlugin%2Fcss%2Fplugin.css&css=plugins%2FRefreshUIPlugin%2Fcss%2Frefreshui.css&css=plugins%2FSyntaxHighlighterPlugin%2Fcss%2Fprism.css&v=20210511224258](https://osmose.numerique.gouv.fr/css/csspacker.jsp?css=css%2Ffff-sprite.css&css=css%2Fjalios%2Fcore%2Fadmin.css&css=css%2Fjalios%2Fcore%2Fbootstrap.css&css=css%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.css&css=css%2Fjalios%2Fcore%2Fcomponents%2Ftopbar%2Fjalios-topbar.css&css=css%2Fjalios%2Fcore%2Fcore-theme.css&css=css%2Fjalios%2Fcore%2Fcore.css&css=css%2Fjalios%2Fcore%2Ffont-icons.css&css=css%2Fjalios%2Fcore%2Ffonts%2Fwebfont-roboto-condensed.css&css=css%2Fjalios%2Fcore%2Ffonts%2Fwebfont-roboto.css&css=css%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.css&css=css%2Fjalios%2Fcore%2Flang.css&css=css%2Flib%2Fanimate%2Fanimate-custom.css&css=css%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.css&css=plugins%2FJLearnPlugin%2Fcss%2Fjlearn-icons.css&css=plugins%2FJLearnPlugin%2Fcss%2Fjlearn.css&css=plugins%2FOsmoseImportPlugin%2Fcss%2Fplugin.css&css=plugins%2FRefreshUIPlugin%2Fcss%2Frefreshui.css&css=plugins%2FSyntaxHighlighterPlugin%2Fcss%2Fprism.css&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 6
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949)
  
  
  * Method: `GET`
  
  
  * Evidence: `2Fjalios-dropdown-repositioning`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�Xږ*,����0��ަ�"�*'�x</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jalios/core/jalios-i18n-js.jsp?lang=fr&nopackfirst&v=20210511224258](https://osmose.numerique.gouv.fr/js/jalios/core/jalios-i18n-js.jsp?lang=fr&nopackfirst&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jalios/core/jalios-i18n-js.jsp?lang=fr&nopackfirst&v=20210511224258](https://osmose.numerique.gouv.fr/js/jalios/core/jalios-i18n-js.jsp?lang=fr&nopackfirst&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jalios/core/jalios-i18n-js.jsp?lang=fr&nopackfirst&v=20210511224258](https://osmose.numerique.gouv.fr/js/jalios/core/jalios-i18n-js.jsp?lang=fr&nopackfirst&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jalios/core/jalios-properties-js.jsp?nopackfirst&v=20210511224258](https://osmose.numerique.gouv.fr/js/jalios/core/jalios-properties-js.jsp?nopackfirst&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jalios/core/jalios-properties-js.jsp?nopackfirst&v=20210511224258](https://osmose.numerique.gouv.fr/js/jalios/core/jalios-properties-js.jsp?nopackfirst&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 13
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "'ui.adm.admin\-notes.error': "La connexion au serveur a échoué ou une erreur s\x27est produite lors \x22 + \x22de l\x27enregistr", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251951)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251950)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251953)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251949)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251952)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="#" class="btn btn-default btn-cancel">'+I18N.glp("com.lbl.cancel")+'</a>`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/displayPage.jsp?id=c_2251954)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="top" style="display:block;"></a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/](https://osmose.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr](https://osmose.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `401`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/)
  
  
  * Method: `GET`
  
  
  * Evidence: `401`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/sitemap.xml](https://osmose.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `401`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/](https://osmose.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `401`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins](https://osmose.numerique.gouv.fr/plugins)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/](https://osmose.numerique.gouv.fr/plugins/)
  
  
  * Method: `GET`
  
  
  * Evidence: `401`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://osmose.numerique.gouv.fr/robots.txt](https://osmose.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `86400000`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `010101010`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `01212121`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `123456789`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258](https://osmose.numerique.gouv.fr/js/jspacker.jsp?js=js%2Fchannel.js&js=js%2Fjalios%2Fadmin.js&js=js%2Fjalios%2Fcore%2Fcomponents%2Fanimate%2Fjalios-rippler.js&js=js%2Fjalios%2Fcore%2Fjalios-ajax-refresh.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete-wiki.js&js=js%2Fjalios%2Fcore%2Fjalios-autocomplete.js&js=js%2Fjalios%2Fcore%2Fjalios-browser.js&js=js%2Fjalios%2Fcore%2Fjalios-clickable.js&js=js%2Fjalios%2Fcore%2Fjalios-collapse.js&js=js%2Fjalios%2Fcore%2Fjalios-common.js&js=js%2Fjalios%2Fcore%2Fjalios-ctxmenu.js&js=js%2Fjalios%2Fcore%2Fjalios-data-broker.js&js=js%2Fjalios%2Fcore%2Fjalios-data-toggle.js&js=js%2Fjalios%2Fcore%2Fjalios-dropdown-repositioning.js&js=js%2Fjalios%2Fcore%2Fjalios-emoji.js&js=js%2Fjalios%2Fcore%2Fjalios-i18n.js&js=js%2Fjalios%2Fcore%2Fjalios-init.js&js=js%2Fjalios%2Fcore%2Fjalios-modal-forbidden.js&js=js%2Fjalios%2Fcore%2Fjalios-modal.js&js=js%2Fjalios%2Fcore%2Fjalios-polyfill.js&js=js%2Fjalios%2Fcore%2Fjalios-popin.js&js=js%2Fjalios%2Fcore%2Fjalios-prefs.js&js=js%2Fjalios%2Fcore%2Fjalios-prototype-conflict.js&js=js%2Fjalios%2Fcore%2Fjalios-single-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-portal.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable-widget.js&js=js%2Fjalios%2Fcore%2Fjalios-sortable.js&js=js%2Fjalios%2Fcore%2Fjalios-submit.js&js=js%2Fjalios%2Fcore%2Fjalios-tab.js&js=js%2Fjalios%2Fcore%2Fjalios-table-data.js&js=js%2Fjalios%2Fcore%2Fjalios-tooltip.js&js=js%2Fjalios%2Fcore%2Fjalios-treeview.js&js=js%2Fjalios%2Fcore%2Fjalios-widget-chooser.js&js=js%2Fjalios%2Fcore%2Fjalios-widget.js&js=js%2Fjalios%2Futil.js&js=js%2Fjalios%2Fux%2Fjalios-caddy.js&js=js%2Flib%2Fbootstrap%2Falert.js&js=js%2Flib%2Fbootstrap%2Fbutton.js&js=js%2Flib%2Fbootstrap%2Fcollapse.js&js=js%2Flib%2Fbootstrap%2Fmodal.js&js=js%2Flib%2Fbootstrap%2Ftab.js&js=js%2Flib%2Fbootstrap%2Ftransition.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fdropdown.js&js=js%2Flib%2Fbootstrap-3.3.7%2Fpopover.js&js=js%2Flib%2Fbootstrap-3.3.7%2Ftooltip.js&js=js%2Flib%2Fbootstrap-datetimepicker%2Fbootstrap-datetimepicker.js&js=js%2Flib%2Fbootstrap-notify.js&js=js%2Flib%2Fbootstrap-tabdrop.js&js=js%2Flib%2Fbootstrap-typeahead%2Fbootstrap-typeahead.js&js=js%2Flib%2FelementQuery.js&js=js%2Flib%2Fhandlebars%2Fhandlebars.js&js=js%2Flib%2Fhistory.js%2Fhistory.adapter.jquery.js&js=js%2Flib%2Fhistory.js%2Fhistory.js&js=js%2Flib%2FimagesLoaded%2Fimagesloaded.pkgd.js&js=js%2Flib%2Fjquery%2Fjquery-3.4.1.min.js&js=js%2Flib%2Fjquery%2Fjquery-fix.js&js=js%2Flib%2Fjquery%2Fjquery-migrate-1.4.1.js&js=js%2Flib%2Fjquery-ui%2Fjquery-ui.js&js=js%2Flib%2Fjquery.ajaxQueue.js&js=js%2Flib%2Fjquery.console.js&js=js%2Flib%2Fjquery.cookie.js&js=js%2Flib%2Fjquery.idle-timer.js&js=js%2Flib%2Fjsonrpc.js&js=js%2Flib%2Fmodernizr%2Fmodernizr.custom.js&js=js%2Flib%2Fmoment%2Fmoment-timezone-with-data-1970-2030.js&js=js%2Flib%2Fmoment%2Fmoment.js&js=js%2Flib%2Fprototype.js&js=js%2Flib%2Ftwemoji%2Ftwemoji.min.js&js=js%2Fwidget.js&js=plugins%2FJGuidePlugin%2Fjs%2Fjguide-polyfill.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism-ajax-refresh.js&js=plugins%2FSyntaxHighlighterPlugin%2Fjs%2Fprism.js&v=20210511224258)
  
  
  * Method: `GET`
  
  
  * Evidence: `01010101`
  
  
  
  
Instances: 5
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>86400000, which evaluates to: 1972-09-27 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `JCMS_login`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `JCMS_persistentCookie`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  * Parameter: `email`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp](https://osmose.numerique.gouv.fr/admin/mail/privateMailPassword.jsp)
  
  
  * Method: `POST`
  
  
  * Parameter: `opRequestReset`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `JCMS_persistentCookie`
  
  
  
  
* URL: [https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F](https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F)
  
  
  * Method: `GET`
  
  
  * Parameter: `redirect`
  
  
  
  
Instances: 9
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://osmose.numerique.gouv.fr/plugins/DINUMThemePlugin/jsp/front/privateLoginOsmose.jsp?JCMS_login=ZAP&JCMS_persistentCookie=true&redirect=https%3A%2F%2Fosmose.numerique.gouv.fr%2Fjcms%2F</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [base] tag [href] attribute </p><p></p><p>The user input found was:</p><p>redirect=https://osmose.numerique.gouv.fr/jcms/</p><p></p><p>The user-controlled value was:</p><p>https://osmose.numerique.gouv.fr/</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

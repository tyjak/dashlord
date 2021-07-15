
# ZAP Scanning Report

Generated on Thu, 15 Jul 2021 07:42:14


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 6 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 4 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Dangerous JS Functions | Low | 2 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec) | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 7 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 7 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 9 | 
| Storable and Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 10 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 17 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h](https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
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

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fingenieur-developpement-de-services-data-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-btn" target="_blank" href="https://www.ssi.gouv.fr/agence/missions/paroles-agents/gaelle/">Voir plus</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h](https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fstagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fpilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fdata-scientist-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__top-link rf-mr-2w" target="_blank" href="https://www.linkedin.com/company/anssi-fr"><svg class="svg-inline--fa rf-icon fa-linkedin-box-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#linkedin-box-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__top-link rf-mr-2w" target="_blank" href="https://www.linkedin.com/company/anssi-fr"><svg class="svg-inline--fa rf-icon fa-linkedin-box-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#linkedin-box-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fcoordinateur-sectoriel-institutions-publiques-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fingenieur-conception-de-services-data-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Ftalents.ssi.gouv.fr%2Foffresdemploi%2Fcharge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h' target='_blank'>
<svg class="svg-inline--fa rf-icon fa-facebook-circle-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#facebook-circle-fill"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__top-link rf-mr-2w" target="_blank" href="https://www.linkedin.com/company/anssi-fr"><svg class="svg-inline--fa rf-icon fa-linkedin-box-fill fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#linkedin-box-fill"></use></svg>
</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/confirmation/new](https://talents.ssi.gouv.fr/admin/confirmation/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,500|Roboto+Mono:400,500" data-turbolinks-track="reload" />`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/sign_in](https://talents.ssi.gouv.fr/admin/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,500|Roboto+Mono:400,500" data-turbolinks-track="reload" />`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/sign_in](https://talents.ssi.gouv.fr/admin/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,500|Roboto+Mono:400,500" data-turbolinks-track="reload" />`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/password/new](https://talents.ssi.gouv.fr/admin/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="stylesheet" media="screen" href="https://fonts.googleapis.com/css?family=Roboto:300,400,400i,500|Roboto+Mono:400,500" data-turbolinks-track="reload" />`
  
  
  
  
Instances: 4
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?q](https://talents.ssi.gouv.fr/offresdemploi?q)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?q" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=7](https://talents.ssi.gouv.fr/offresdemploi?page=7)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?page=7" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=6](https://talents.ssi.gouv.fr/offresdemploi?page=6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?page=6" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=2](https://talents.ssi.gouv.fr/offresdemploi?page=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?page=2" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="rf-search-bar rf-search-bar--lg" action="https://talents.ssi.gouv.fr/offresdemploi" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=3](https://talents.ssi.gouv.fr/offresdemploi?page=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?page=3" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&amp;contract_start_on=2021-07-15&amp;job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&amp;job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&amp;job_offers%5Bcounty%5D%5B%5D=Paris&amp;job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&amp;job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&amp;job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&amp;published_at=2021-07-15&amp;q&amp;q=ZAP" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=4](https://talents.ssi.gouv.fr/offresdemploi?page=4)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?page=4" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=5](https://talents.ssi.gouv.fr/offresdemploi?page=5)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?page=5" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form data-turbo-frame="job-offers" action="https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&amp;contract_start_on=2021-07-15&amp;job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&amp;job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&amp;job_offers%5Bcounty%5D%5B%5D=Paris&amp;job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&amp;job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&amp;job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&amp;published_at=2021-07-15&amp;q=ZAP" accept-charset="UTF-8" method="get">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "056ddee9-75b0-49e2-a8db-bfb2263602d6" "87e2a6fb-1f64-49ac-ac65-0f6abacb77e2" "a05a0d42-53b7-4e22-9beb-bfd5a22d4273" "commit" "contract_start_on" "d595b2ca-899d-420f-aead-6d1b402dccba" "d7422709-11ef-44fc-9d66-a77c71052850" "d8e7b0d8-ebd6-4d50-88bc-7a7a842bb6c7" "f27f212e-6133-428b-b96a-040ed992552a" "f53745c0-0923-49c5-b6c8-ae413154c21a" "fe79237f-d5b1-49f8-98a3-16393f954549" "job_offers_category_id_09b8690a-6213-498c-bfd1-f87bf5ff4c8d" "job_offers_category_id_0d1f0b9f-37ec-4b1f-b8cd-660c34163c5e" "job_offers_category_id_1163b336-2f50-44ca-a283-7b4f383d083c" "job_offers_category_id_12da2ff4-964a-491d-b5f9-17afa178deb6" "job_offers_category_id_1c05273c-fba6-47d4-ae62-939c16d1c7bf" "job_offers_category_id_1fcd7771-765b-4799-8d80-a7323e097fcc" "job_offers_category_id_220f9334-798c-43e7-9059-9a3108d9e951" "job_offers_category_id_2912e734-a935-4afe-8ca6-73cf6244c339" "job_offers_category_id_38488bc7-c110-4d00-bbdb-b4c3db428094" "job_offers_category_id_3a21135f-2b81-47f1-846f-a37ce19fd0f4" "job_offers_category_id_3b999c77-8e64-4bba-bada-1e07dfccd231" "job_offers_category_id_3bc7cdc3-76da-4d05-8641-2ed8729e88d4" "job_offers_category_id_46b5dace-f5bf-4327-ac17-59f2ae851b22" "job_offers_category_id_4ba7df95-09bc-4bb2-9e1e-905e46a8b5bc" "job_offers_category_id_6b9941ee-0053-4307-9086-aabb7b8a8a87" "job_offers_category_id_845db656-7956-4d6e-a09f-af0f8ff4b476" "job_offers_category_id_84798f72-9a82-4a03-8fbf-399e76b53203" "job_offers_category_id_87cc9c77-6386-49e2-a818-080f3e89b085" "job_offers_category_id_98735417-3106-489d-8c20-0f8ebb229448" "job_offers_category_id_ac605936-b4b4-496f-a273-8adbe98a6d5c" "job_offers_category_id_b2b90d0e-ff79-4b34-a1fd-1b51ac477cc7" "job_offers_category_id_b2c63167-5b36-46a2-9c11-9a19af2a4536" "job_offers_category_id_c28bbb2b-9774-45a7-8474-5a4269202488" "job_offers_category_id_c9202e2f-d563-435e-8ff2-e6353c1fafbd" "job_offers_category_id_f2627226-e2a6-4774-bbf0-662a1fda2b95" "job_offers_category_id_f63980ce-7988-4daf-ac18-652cf7b67e7d" "job_offers_category_id_fc0dccc8-285f-4252-b123-ebcca6224f56" "job_offers_contract_type_id_20b56e96-b90d-4f4c-bb70-a2f3273eff62" "job_offers_contract_type_id_53a4839f-53f8-41dc-a582-3d682f7b681a" "job_offers_contract_type_id_8694950d-52d1-4710-8550-d7007d3ec33d" "job_offers_contract_type_id_d43e1201-bd91-4891-84ce-96a6ab2823fe" "job_offers_contract_type_id_e4b9ff00-8acc-474c-9796-0cfb375512a2" "job_offers_contract_type_id_fcaa7225-91f0-4f22-9b88-1b50a4a08820" "job_offers_experience_level_id_074c8493-92e7-4010-bd44-c1de19ca1399" "job_offers_experience_level_id_27f087cf-a563-457d-8c5b-ef8b21632e5d" "job_offers_experience_level_id_42ee2414-0137-4617-9aff-791a42889ce5" "job_offers_experience_level_id_78904ebf-d344-4b08-91ac-6a2cd7a6da15" "job_offers_experience_level_id_879fd308-3514-45aa-a788-b573b23268a2" "job_offers_experience_level_id_de2c7c08-854a-485e-89c0-846931d1d7f5" "job_offers_experience_level_id_e22e6311-a0a4-407a-86b3-725f1cd2899e" "job_offers_study_level_id_16eaeba0-5809-4dee-aa58-b67331280f91" "job_offers_study_level_id_3988f1f8-601d-4871-afe7-6c0f5fbfe7af" "job_offers_study_level_id_5a5b7e3d-682e-466e-bb87-5ea476e56a30" "job_offers_study_level_id_7e912f53-e383-43e1-9ccf-2393c3ebc78e" "job_offers_study_level_id_b3199283-8a67-4cb5-9ad2-d38222441632" "job_offers_study_level_id_b43cf357-0154-4166-a527-fac28033b5ee" "job_offers_study_level_id_b8238013-0215-480f-aa00-d8e11048265b" "Paris" "published_at" "q" "Seine-Saint-Denis" "Île-de-France" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/bundle-4874975059d550fa9035.js](https://talents.ssi.gouv.fr/packs/js/bundle-4874975059d550fa9035.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js](https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 2
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/sitemap.xml](https://talents.ssi.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h](https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/robots.txt](https://talents.ssi.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, private, must-revalidate`
  
  
  
  
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
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h](https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h)
  
  
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

  
  
  
  
### Strict-Transport-Security Multiple Header Entries (Non-compliant with Spec)
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) headers were found, a response with multiple HSTS header entries is not compliant with the specification (RFC 6797) and only the first HSTS header will be processed others will be ignored by user agents or the HSTS policy may be incorrectly applied.</p><p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL).</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/robots.txt](https://talents.ssi.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin](https://talents.ssi.gouv.fr/admin)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/sitemap.xml](https://talents.ssi.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that only one component in your stack: code, web server, application server, load balancer, etc. is configured to set or add a HTTP Strict-Transport-Security (HSTS) header.</p>
  
### Reference
* http://tools.ietf.org/html/rfc6797#section-8.1

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/media/images/favicon-16x16-9c9bc8736e64d77f6a958361f4c11d79.png](https://talents.ssi.gouv.fr/packs/media/images/favicon-16x16-9c9bc8736e64d77f6a958361f4c11d79.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/css/admin-style-52a86b1c.css](https://talents.ssi.gouv.fr/packs/css/admin-style-52a86b1c.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/bundle-4874975059d550fa9035.js](https://talents.ssi.gouv.fr/packs/js/bundle-4874975059d550fa9035.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/media/images/favicon-32x32-3926cca26e32cb59f943c98541e1f447.png](https://talents.ssi.gouv.fr/packs/media/images/favicon-32x32-3926cca26e32cb59f943c98541e1f447.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/devise-bundle-2d1a2da61f6a1a18d897.js](https://talents.ssi.gouv.fr/packs/js/devise-bundle-2d1a2da61f6a1a18d897.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js](https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/css/style-965923ee.css](https://talents.ssi.gouv.fr/packs/css/style-965923ee.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 7
  
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
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BpOnE9lSAGUmjxceeAShrTjaMnesU0MlosHP2uuxBWikfQxOB4ez8riQn3boT`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `UYkLnhCdry5ADBKaoOqXWwRfJszYFgu1wEMrIfcTzoKpJAhy`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FlAR03fo6osabvbY4Kl8fnhje7mvwl`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `JbFsjhoMt743HgC2fBWZsd5xmwUPDoNQKujnII`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin](https://talents.ssi.gouv.fr/admin)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FPriuikh3XlYMFwS146kWmuuvX6xoFq5M8krP7yUR0vhqs`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `2B7n0aJ1hGbfWW8hDbSVLnRsjmatG2ijYQ2kyVu`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  * Evidence: `nQpa9KC1O2RVAX-pz4jwgpCEHOdpBEpqFjdWoW2iaItLN0VXMR_MfInwnTQNJFEMERi-TryGqINmgQgoj09htw`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Evidence: `u2CWMToOkQdSBvae6QFQj5dQ8Lu1gMN8rS7lsir`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `BBxsEXS3QDabmDfrwZPTjOWxRTmHnK66mBlw0h8WW3JjJNDzNQoJADuJx86E0xeRcLIklgbxP3Rh0ZFTNiM8QoV6fJ5CcL4QJekPKdo3wURCNjFSlDAl`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BxCV4SXVj1Rb740MUKLbxGP4eXRgNhKirKv84UvaJ`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `2F0ShFiBdIqXRnElHYeEt4coTyC0RXJqrSL9fZPZFSRsposXvzxL0xkLGNCFkmgMgkNoWub441iuBOMTXOhJNOgB`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  * Evidence: `t9N7Pd2gC3atxuYEXtoGeJNwweZW9REOKz-BRItrhYXxW7jVVyOL_tp9HxXpqJfyJ7D1I8XWxfYo9YiWvMQ10Q`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�\x001aN�OeH\x0001��<\y�\x0012���h�ޱM\x000c��\x0007?k��\x0015���18\x001e\x001e���B}ۡ</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/sign_in](https://talents.ssi.gouv.fr/admin/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/sign_in](https://talents.ssi.gouv.fr/admin/sign_in)
  
  
  * Method: `POST`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/bundle-4874975059d550fa9035.js](https://talents.ssi.gouv.fr/packs/js/bundle-4874975059d550fa9035.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/password/new](https://talents.ssi.gouv.fr/admin/password/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin/confirmation/new](https://talents.ssi.gouv.fr/admin/confirmation/new)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js](https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js](https://talents.ssi.gouv.fr/packs/js/admin-bundle-8ab177a6214615f93977.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
Instances: 7
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "<script src="/packs/js/admin-bundle-8ab177a6214615f93977.js" data-turbolinks-track="reload" defer="defer"></script>", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__brand-link" href=""><img alt="ANSSI - Agence nationale de la sécurité des systèmes d&#39;information" style="width:auto; height:5rem;" src="https://osu.eu-west-2.outscale.com/erecrutement-anssi-production/organizations/operator_logos/893/049/fa-/original/20180613_logo_anssi_m.png" />
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__brand-link" href=""><img alt="ANSSI - Agence nationale de la sécurité des systèmes d&#39;information" style="width:auto; height:5rem;" src="https://osu.eu-west-2.outscale.com/erecrutement-anssi-production/organizations/operator_logos/893/049/fa-/original/20180613_logo_anssi_m.png" />
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-developpement-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__brand-link" href=""><img alt="ANSSI - Agence nationale de la sécurité des systèmes d&#39;information" style="width:auto; height:5rem;" src="https://osu.eu-west-2.outscale.com/erecrutement-anssi-production/organizations/operator_logos/893/049/fa-/original/20180613_logo_anssi_m.png" />
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf-footer__brand-link" href=""><img alt="ANSSI - Agence nationale de la sécurité des systèmes d&#39;information" style="width:auto; height:5rem;" src="https://osu.eu-west-2.outscale.com/erecrutement-anssi-production/organizations/operator_logos/893/049/fa-/original/20180613_logo_anssi_m.png" />
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h](https://talents.ssi.gouv.fr/offresdemploi/stagiaire-charge-d-analyses-strategiques-et-de-prospective-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-conception-de-services-data-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href='#' onclick='window.print(); return false'>
<svg class="svg-inline--fa rf-icon fa-print-solid fa-w-16 rf-icon-xl" aria-hidden="true" role="img" xmlns="http://www.w3.org/2000/svg" viewbox="0 0 512 512"><use xlink:href="#print-solid"></use></svg>
</a>`
  
  
  
  
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
  
  
  
* URL: [https://talents.ssi.gouv.fr/admin](https://talents.ssi.gouv.fr/admin)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/sitemap.xml](https://talents.ssi.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/](https://talents.ssi.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h](https://talents.ssi.gouv.fr/offresdemploi/charge-de-mission-veille-analyse-et-management-de-l-information-reglementaire-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/pilote-technique-specialiste-en-traitement-d-incidents-informatiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/robots.txt](https://talents.ssi.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h](https://talents.ssi.gouv.fr/offresdemploi/data-scientist-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h](https://talents.ssi.gouv.fr/offresdemploi/coordinateur-sectoriel-institutions-publiques-f-h)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://talents.ssi.gouv.fr/*/apply](https://talents.ssi.gouv.fr/*/apply)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/mes-candidatures](https://talents.ssi.gouv.fr/mes-candidatures)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/css/style-965923ee.css](https://talents.ssi.gouv.fr/packs/css/style-965923ee.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `0909090909`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=5](https://talents.ssi.gouv.fr/offresdemploi?page=5)
  
  
  * Method: `GET`
  
  
  * Evidence: `98735417`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=3](https://talents.ssi.gouv.fr/offresdemploi?page=3)
  
  
  * Method: `GET`
  
  
  * Evidence: `98735417`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi/ingenieur-e-projet-en-detection-de-la-menace](https://talents.ssi.gouv.fr/offresdemploi/ingenieur-e-projet-en-detection-de-la-menace)
  
  
  * Method: `GET`
  
  
  * Evidence: `20024458`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=4](https://talents.ssi.gouv.fr/offresdemploi?page=4)
  
  
  * Method: `GET`
  
  
  * Evidence: `98735417`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=2](https://talents.ssi.gouv.fr/offresdemploi?page=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `50000146`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?page=2](https://talents.ssi.gouv.fr/offresdemploi?page=2)
  
  
  * Method: `GET`
  
  
  * Evidence: `98735417`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/packs/css/style-965923ee.css](https://talents.ssi.gouv.fr/packs/css/style-965923ee.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi](https://talents.ssi.gouv.fr/offresdemploi)
  
  
  * Method: `GET`
  
  
  * Evidence: `98735417`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?q](https://talents.ssi.gouv.fr/offresdemploi?q)
  
  
  * Method: `GET`
  
  
  * Evidence: `98735417`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0909090909, which evaluates to: 1998-10-22 21:15:09</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[contract_type_id][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[county][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[category_id][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[region][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `published_at`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[category_id][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[county][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[region][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[study_level_id][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `contract_start_on`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[county][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[category_id][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `q`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[experience_level_id][]`
  
  
  
  
* URL: [https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP](https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `job_offers[region][]`
  
  
  
  
Instances: 17
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://talents.ssi.gouv.fr/offresdemploi?commit=Rechercher&contract_start_on=2021-07-15&job_offers%5Bcategory_id%5D%5B%5D=f27f212e-6133-428b-b96a-040ed992552a&job_offers%5Bcontract_type_id%5D%5B%5D=20b56e96-b90d-4f4c-bb70-a2f3273eff62&job_offers%5Bcounty%5D%5B%5D=Paris&job_offers%5Bexperience_level_id%5D%5B%5D=27f087cf-a563-457d-8c5b-ef8b21632e5d&job_offers%5Bregion%5D%5B%5D=%C3%8Ele-de-France&job_offers%5Bstudy_level_id%5D%5B%5D=b8238013-0215-480f-aa00-d8e11048265b&published_at=2021-07-15&q=ZAP</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>job_offers[contract_type_id][]=20b56e96-b90d-4f4c-bb70-a2f3273eff62</p><p></p><p>The user-controlled value was:</p><p>20b56e96-b90d-4f4c-bb70-a2f3273eff62</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

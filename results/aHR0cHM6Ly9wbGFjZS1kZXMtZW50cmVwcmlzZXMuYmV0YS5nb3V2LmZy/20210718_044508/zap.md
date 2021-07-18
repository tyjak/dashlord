
# ZAP Scanning Report

Generated on Sun, 18 Jul 2021 04:38:19


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 7 |
| Low | 5 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: style-src unsafe-inline | Medium | 4 | 
| CSP: Wildcard Directive | Medium | 4 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 1 | 
| Source Code Disclosure - SQL | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 12 | 
| Absence of Anti-CSRF Tokens | Low | 2 | 
| CSP: Notices | Low | 4 | 
| Dangerous JS Functions | Low | 11 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 10 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 10 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 16 | 

## Alert Detail


  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-eqX9aGgB2FX8l29aqyeFxA=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-eqX9aGgB2FX8l29aqyeFxA=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-klGx0kIiWtRZvZ1lqt+v1w=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-klGx0kIiWtRZvZ1lqt+v1w=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-0tre5yEmu4LEVbcSOCk0wA=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-0tre5yEmu4LEVbcSOCk0wA=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-Qm4HVwRoVk/iq56NSC29tw=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-Qm4HVwRoVk/iq56NSC29tw=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-0tre5yEmu4LEVbcSOCk0wA=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-0tre5yEmu4LEVbcSOCk0wA=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-klGx0kIiWtRZvZ1lqt+v1w=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-klGx0kIiWtRZvZ1lqt+v1w=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-Qm4HVwRoVk/iq56NSC29tw=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-Qm4HVwRoVk/iq56NSC29tw=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-eqX9aGgB2FX8l29aqyeFxA=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-eqX9aGgB2FX8l29aqyeFxA=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Page Linkedin de Place des Entreprises - lien externe" target="_blank" rel="noopener" href="https://www.linkedin.com/company/place-des-entreprises"><span aria-hidden='true' class='ri-linkedin-box-fill'></span>
<span class='visually-hidden'>Linkedin</span>
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

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/tutoriels/Guide_entretien_Place_des_entreprises.pdf](https://place-des-entreprises.beta.gouv.fr/tutoriels/Guide_entretien_Place_des_entreprises.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#dRC4`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#dRC4</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/book.pdf](https://place-des-entreprises.beta.gouv.fr/book.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x0019aÉ\õëÆ+Äµkck}4dc\x000cqô×}7Q7\x0016Í»ò\x000f¨=bx×Ã÷\x0002!¨,'Êgpè\x000f¥c§í#æteõ\x0015)Û£8\x000cÐq~õ!L#\x0012À\x0010q·¹¨ñ^+Mn{ÂR´bR\x0002H£i[j\x0002[ÐS]J±\x000c0GjØð¤\x0006}Oåþ\x0004gý?úõtáî%aÐ±"¥KÞ±´©¥IO«d&TVv
³\x0013\x00079¯Ið'ÂÝOÄ3F÷\x0011 '%O\x0007ñÿ\x0000
Ö\x0014ÜÞ5J¦¯#Òt«ÍVàAc\x0003Êýð8\x001fSÚ½SÂ?
Ù&ÔÆó×h\x001c~_Ôñ^ç¢x/Hð\x0014,d\x0003î \x001bûû}k+Äw2+G
-ø"4ïî{õ®êXu\x001dYä×ÆÊ~ìtG+p4½\x001e?&\x0008£.#Ç÷©ú.\x0005qÖ­s©£C+í´RvÃ\x0008Ú~¯ã]·¶_Ü5Ä6QZ¦Ñ£ÈN\x0007$gMqq\x0012¢ªÄíÉ\x001eâºÇ\x000cæÞç'8\x0008ÿ\x00007^§×>¬ËÄù$\x0018Á µoÞÚ\x0014;²\x0007\x001cs\x000fnµ©Äâââ@Åò»\x0002N0ÀZÂgm\x0007}Nvyd*È¡v\x000e\x0017¡/8\x000bÓéÖ´gèAôÇj£(Á9?sTG§M¢¹ëIN#84Ó\¬Ü(÷íIJ)\x0001jû\x0003âOúUu\x0004s»:"Â\x000c\x000f¦sýkwÁI¦Çâ\x001eo\x0011+bý¥>ÒÊ3ò\x0003\x000fùÎ)=\x0015Ê^ô¬}Uð\x000fÃ¶
>\x0016^ø»Ä
!¹¼í2n\x001f2@?Õ ÷cÎ?Ú_Jùß]ñ\^5ñ\x0006¡wâb·3\x0019#%\x0006KPz(þò\x0001ö\x0007¡¯Dý¤þ+Øø¢ÖËÃÞ\x0017ºY´èÏu$`w\x001fuA d/_©\x001eà¼6[!qÚ°ÁÒnN­E«+\x0011¤yVåï\x0012ø~ëA¹')5´éæ[\ÅÌs§÷ÿ\x00001Ô\x001eµÒ»¿
êöóéèÒ4ÚDÍ¸\x0015\x0019ÖOùêþ«ÜW1âM\x001aãCÕ$´¹*ã\x0002H¦O¹4gîºB?Â»*CU±ËN§7º÷2h¢ÌØ(¢
)Ñ©v\x0000
Ú@º\x000f4DÛOCQ:ÄÍ©P_\x0018tUW`xªæ©4õFs í$%\x0014QLEL³Èª\x0006ãÓÚ¡¥Áô LNô \x0012x¢¥A>Ô\x0014\x0013¹!A8ëíI"\x0005à\x001cÖ®ÝH
£¡'©÷ª-ÓNÀÒ[\x000c£¯µ\x00154\x0011ù\x001d)\x0002"Áô :³!TÜ:ÿ\x0000\x0015Vlç\x0000N´´¤\x00111\x0004ö Dt#\x0003\x0003e\x0000\x001dêX\P;\x001e\x0005EU$\x0010AéU\x0017Êî&®k%Ão¼Ä;î4Û85{XM«\x0001w¥3×Ó\x0015ç°Ió)=Ez\x0017à·¾¸+\x001câ\x000b7F	<;~5ëaçÌyXøZ7]\x000fPðN°§öW!òËüÐÈÃ\x0019\x001fZìaÑtèâH½	-¬àC\%½uªY>z\x0014^Bp\x000e\x0008#ÐÓIñ%ê£\x001dÃoB§õ®¹Eu<zsô<§âG¿²5Éâ±F%ä\x0019÷®\x0014ÄA í_ox;HÓuÛ\x0018^þ\x00105\x0008AICÛ&¾{ø¿ài4mN{\x00083m\x001b\x0015fAÆ3ò~ÃR[=¼.&MrÈòi¤+¸(ÀÚ6¨\x001d>~µ:éò¾%ê²yQÈ\x0011?7=êå¼I2Ä\x001dç'§½1£hCFÁ$á\x001e8¬\x001d\x0003µUìnx"ßÊÒu½A\x0016(v)÷ è?:¡á?\x0006ë>+¼0é6HócäLöÏsì9¯eømð­ï|\x001b&©âMJK?\x000f\¾øí`mÅî1 ýÐHÀ<9às^ã ¤\x001e\x001bð ³ÊÛG°Éh­ 8¯¡nÙÇ,y<Ö\x0010ÃZM²±8èFbº\x001e_à?:~%k·igíâE
¨Aç~\x001fz\XévâÓGT\x000e²ÉúzW%­xÄÝ1\x0014"\x0004'j¯\x000bê}ë\x0001|H¾hYVH×?3\x0003éÞ½*tl¯ö¹ÜÝ°÷\x0012rFI'9¬»û\x0013!ù\x0010\x001fZÍÓu´s	wìÀÛ´å¿Ãñ®Öh®£È<ôÅSV&.ç!©ÚfÙUåSÉÏëã.¬Qf\x0011´¬!e\x000b!PN\x0006yÈïô¯SÔl<ÍØãw\x0019®_SÓÎ×FQ°\x0010·\x00185&«SÍ.ì\x001dI\x000cG#\x001cc?aÉ\x0018	r²d«¦Ð16A\x001fËµwúh(FÌ·©çzn·à½VËÃúÕÝ \x001a|ì\x0004Dã89ÛÔ\x0003-\x0019­\x00157w\x0005±æsÛ©Ó/\x0018d4h\x0018ý\x0018}k2	\x0018ç½w¶Â=\x001eeQ×#9ç\x0018þ¼×/{m'iëÿ\x0000U`á{ðªË\x0019\x001eµ~Xx?)VÏJªè\x0007LóÓç;\x001d±ÈkJÇJ¹¹·á"&)g\x0016Èç2\x0011	¬üWMá\x00116\x0004Ú}äku£ÝöWèHèêcQN)½B£i]\x0019Zþ©h:¬úv³i5­ìXß\x001cz\x0011ØØ*r4g\x000fJ÷w¹Ò5ï
[i~*¹÷CÆÍ/Ä\x0001w\ézCp?3øzc¨òO\x0019øWSð¨lõX\x000e7Ã<gtS§gFèGê;ÕT¤á©\x0014«)è÷24(eÁ\x0004ò§ü÷¨°ÝJç¸¨Ó«Ð¤·XäÒ5Ø¶ùUÙbÎ_-Àlt®ÒÊÕ|Q \x001d\x001dòu\x001bey´çÇÞ#èØÊú7Ö±î´Û}0Í
4¾L²«7ð¸QõäÀT:\x001dìÖÒÅ$e£\x00182889\x0007Ý«¡FëS¬\x000eUÁRA\x0018#Sk²øa\x001fÛ­õ8Â[êet\x001d#­_nHaìÕÆäy]ØMN*HJ(¢¤²ÕªL\x000bv®®×^8<¼î\p
q`ÐÔâr\x0017\x0000óXV¡\x001a\x000f\x001aðéÄÐÔ.Ä±êy¬94®å4ÊÒ\x0010QV9±\x0015Ýis0¢*Îp§Sih\x0001ÉQøÒæF\x0007N;ÒA cÎ=)sôày=³ëLnµOa
 tLCuê)ª)qZH\x00077P{ÔmÖíóQõ¦À\géR»eF8ÅGÛ8¥\x0007R@!¤ëÚ\x000c¶*B@áF\x000fLÐ\x0004l1MïJyïH=i\x0001§¢Å\x000cÏq\x001cÊÌþK\x0018ðq\x0002¶tb\x0004&EÅ:ÈAÅs\x0010Èñ11±V#\x001czVÅËäBØ\x0019*yàßZéÂÉ©\x001cøó@ôß\x0007=¶¡|³j7M\x00061¹±Îs^®Þ&_\x000cy?ÙwßÚKFìì5ã~\x0017ÖßO¶#O[Q$§rÄ{\x0013ÅMk,Óê\x0019)´\x0017Úxùw}kÚMIj|Üá(É¨£Üü\x0013"jú»êÑÜI\x0015¸Þ*\x000e\x000f\x0015»ãí"Ã^ðåÄ|ê&hýÿ\x0000oÒ¹»[©ôo\x000b¬{D²\x0010\x000b®0\x000fOÖ±ôï\x0018\é°HÂÏ&vE"±ß\x001dÇ<
Â¥>gsªeOsÀçðî¥
ÒÄ-$ó\x000b\x0014À\x001d\x0008¯Nð\x0007Ã¸âÔÐÍm\x001e³©4q¨Í¼\x001d>gÏÞ#Ó¦}k»Ð¼#¨ë\x001dGZÙÙ¹ÜÒ°ÃIì«]\x0005Þµm¤[6áÈ|ÇÞà³V=þ*We¸T®å¶ñ.§Ø¼0¦îúq©k$X¸èúc¨®+Ä\x001aú­ãÌy\\x000e\x000f§\x0014±Gu¨Ü\x0014@eYÀQî{\x000fjí4/\x000c5ÉÞÝî'8ýéL(\x0007z{óUe
dõ9[u4KCÑ<\x0015ª\x0001%Ã<\x0011à-p\ý{\x000fçYú¿b·UxîTGýôahêP\x0011Ãû§¯å^°×\x001fÙ×FÞy\x00166þ\x0016è	íøÕÛ3ûRÙ®\x0010yW8À\x001coíÏøÔ:®.ý
\x0015
5GÏ·ú]Í[«YRæØä%Ô\x0019\x0003\x0000ã$u\x0004t ò\x000fZ×ÐµV\x0002á9qÃ°ù$ëù\x001aéµ­\x0016ïI»ö0ÞVQqnNÅú\x000cDróò¿FèÙÍ`jZ\x0004\x0013íOe¥$,2
Ït+ü\x0012\x000fîô=WÛNe"9\x001c]ÑÓÚ_	ÐG!Û&;÷¨ï´ñ *ª	<\x000eù®BÂðÚ\x0018a¸}î\x0006ÇÁY!lð0zö®»M½Þ\x0002±óc<g¾}Çô©±¤döfU_SÖlìÖ2<Ç\x0008äv\òqì3]/Ç{ÞÆÃ@µÂA
äP8\
¨¿Jë<\x0005§Göõ9~ìJQXç\x0001üëÎ¼Y,±wy!?¼rT\x001eÊ8\x0003ò\x0015Ã%ík§Ñ\x001e¢°ÃÝo#Æµ+7Xlr·\x001cc#\x001fÒ¹{ËdF!»ôÇA^±©Ù_8ÎÜã«{}+Ô´ð\x0016BX:¨^¹®ÞTyÊnçM\x00048ÍÊÆ2#9ÚU\x0018cê\x0007<{Ö-Ü|W\x001e¾æ»K»"Y¸`\x00019'ùV\x001då¶\x0011ð GSÈ¬'Nèï¡èÎi\x0003ßµM\x0012î_å×X
¬<ÐÅIç\x001f_çUçP'v]#ÜJl:p2qì+Ç7¼+â\x001b\x0016êFG-¬ªR{ièæNáë^©£O¦jÚ<ZL5O\x0008ÜÉo5Â¥Þ)\x001f~7n©üÇ\x0004zøiv\x0004#¿B~´y\x0003
 \x001cc¯l­fa:\x001cÎëFhk¶ÖvrÛi«xäe\x0017\x001bvyàÇ\x0015sI¬íRg*®î\x000e\x000erG§Ö °µ6Ñ5Ýá+B\ý
:iÚ\x0019\x00149ÿ\x0000H²ª[" Ýþ´ ÷6ä¹\x0016¥ù¥c\x0014­;.R\x0017óC}ÔR0ª1ß=ê¼¥\x0013|`m#·?½AovÚN©r\x0004fX*C\x000fZ
ä\x0013N¿fÂ\x000fÞ%ò\ú~\x0015qlfÒå¶k¦Æ¾!ð«¤xí¶¾d`QþònüTW0äî¼!}.¬Ãr\x000e|Wùº7<=FGãX;Ò\x0017DñV£g\x0017ü{¬d'Ö'\x0001Ðÿ\x0000ß,*1\x0011ÚA,¥OæsÔQErÁE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0003\x0011N\x0007àÓhRE\x0000w~8ðàï\x0007ëtÓÊºÅ¬8\x0012dl0\\x0001Èàú\x001aá;×´ßÄ5ÙÆu;¥Ñu¶ÿ\x0000³\x001cÀ\x0016e¯\x0016¨§'$îmZ)KCÙ¿g\x0007h^2O\x0015Yë6­q{\x0016ÓYívS\x001bFáÉ\x0004§^?:ñéc^ßû!j\x001feø£öf8\x0017SB\x0007©\x0018ý×ø¶ÄiÞ$Õ,@#ì÷RÂ\x0001ëò¹^*IûÅI'\x0004bÍ ¥#\x0004\x0011\x000e+Cx\x001c{ÓIçéSK<2¶â£\x0000ã¥Bç'\x0006íÐNôìe9\x0008Ï#"T±ô§`/¹ïN@Ø\x000b\x0014qà`ì$çëièi\x0000äRyý{U«[IÊ»O"¢,¼þµFã©ÈúÕFN.è%\x0014ÕÒ[ê6F$FvóõÅz7à½ºÑäM*d¾¶,ñ(
ã\x0007O9\x0018\x001d\x0006kÅb]Ì\x00018\x0004þ5Óø_\¼Ðµ\x0011=¤Îª0Ä/\x001d±ïÍvÒÅki\x001cUpÊÔú.ÇÃZ«*.±}ö+E\x0000,j\x001dñïÏ½t\x001a%¯ô\x001bXbûmâ¶ß>ä û à\x001f©¯6ðïÆ»{k-ÕÍÅ\x0012\x0016æx\x0015Tv}Ï§¯­t:¼öº}ÍÌVÍ{\x000c,\x0001¸x\x0015\x00046\x0001È ä\x001f¥w¹)»\ð¥F¤#ÎÑÔßëW×× I!\x0012\x0016Ùµ9ÏNx\x0003ÛÃñ\x0014ñi3:7\x0016
PbcÓw}½óéX~*Ö&Ôôñ}c0\x0004|-\x0018!\x0003>ÙþyªZ]ÜÚÇÖ+÷SÚ«C\x0011Î§æ0¶«)öÇ¥7\x001blU$¥¤µÝZU¹\x001dUÊÛ$ØÉò§^pÃv	=\x000f88í]_> ÞÛ3Øj\x0017ßhL\x0014ÎáÛ\x0007¶q=ù\x001dëó<·\x0000" IVLðJàu\x0000äzU\x001b½4èî¢ægO¼ËÙj¥UñÕ]y(ã¸ê:ò\x00085\x0012jÖgT)s+GcèÉ¯å¾H$¸+&\x0001\x0008À\x000cv÷ÿ\x0000ëWG _H,S®c\x0000ç?Â}9õþuâ\x0004»ñ\x0006ñ¤âÞòÁÁ`b¸ù\x001e½Üwþ~g¬Û\x0013Q÷eárHúñÒ±SV.\x0010mîô:+È!I-æPFÝÜn\x000c§ø_Ôzf¼÷Å\x001e\x0011\x0002ðµ\x001e]Òüè­Ê:v^ø=FkºKëV·WûGîØÝ¹zÙÎjxomîåH\x001dÃcË*	*zp}3Åg\x0016áª\x001c°ï³û#¼½Óµ\x0019!Qéú¶\x000c~c.âèç¡\x0018ä\x001a®]ÆâK\x0017\x000f7aê%B3æîèFxÇPqÚ½3Tð<zÿ\x0000hºha¸/Ú\x0004Qe]ðËAÆ\x0007çW,ü7ebövRÈo,a;\x0002Ñ\x0010r¼v\x0019À§*é­
\x001a*wÜ[ÙÃ¾\x000c²±BÝÜ®äóËýp\x000e+\x0018®£vFR¸É\x001fÊ§ø¬'ºÖí®¸Òá]h¾o-¹$z
æ4ÝEF²å\x0019¸f#å'ê?ýT°´ä£ynN:ªsIlêzoÊY¹\x000c\x000fÒ¹KMà\x000e\x000f\x000c==+Òá\x0011ÞB\x0013x³È-íÔ\x000fJÅÔ4Ò\x001b\x0000\x0000\x0001$Þº\x000e;u<UÓUp\x001c¯\x001cç?rº®,çÉÀÚA'ÐöMWO>bÌcû¤p \x0000@Çaôæ¸ýVÇ|ÈWçËn98ç$Q¸Ó¶¨òýFÒ$O(Êñ\x0002v\x001b[\x001eøà\x001aÁºªýà>cÆ\x000e\x001aô
FÎ%¸*3"¹ 2£¾?É®cPµÝ¡èsÓ>Õátwañ\x001aÙ&°ÑàðúÜI¨<ú¬À\x0014¶0°ÿ\x0000\x001b\x001e§ØV\x0000ÇzÐº¢Q´å[8ãg½RhÈ\x0019þuÃ88³×öÑXÑæmVî\x000bi\x0008XÝ!Gækb-5\x001e6,còÙ°{¹®zÞXà$Í\x0017Ë.àÙ\x001b\x0002\x0001éÔþ½s¬ô32À,lze³0\x001d\x0003×­]9¥ñ\x001cµiMÙSÑ\x0015u+}A7Á\x001c­5¿L/\t§\x0015\x0005ì¶pÛE\x0004QÈ\.î~]®x9ã'¥YÓ®tå+rc7ÜíÖf¯t·w!6]þö;Óº\x00154å.WÐ³kvV\x0018Ùq½xç¡\x0015Ñ|Ií6~\x001fÕ	\x000cÓZ}L\x001cáâ8äÿ\x0000ºËùW\x001fd[ÎÀÉ\x0004`2q^© x_QñÖ¥hÖ*
ÁÔ\x0012\x0011ÄQ4g|ì6)?\x001diÊiÒmÃ´mÔ_Ùïá~3ÖfÕµäÙá3çíY\x000cù{»\x0000>f=\x0007ñ\x0003\GÄ»Ý\x0012ÿ\x0000Æº¤þ\x0016´[]\x001cÉ¶\x0004Q´\x0010 \x0002Àv\x000cA8÷¯iøõâ­?Á^\x0015´øcàæÙ\x00141(Ôf_¼sÉB¼Çæob\x0007Lù¸×EÊmÍíÐô¦ÔcÊÑE\x0015Ðb\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000H=i½è\x0007\x0002Æ7-<Q«Ùø[Pðý½Ù]"úDâ
ªC²\x0011´ç¨è:uÀ¬!ëFp1Uö¡h7&÷:¯¾-Àþ2Óuø­èÚ3\x0016¾ß1YYXg\x0007\x0007\x000c{zRjz¼>'ñ³rY&©%ÄÛKåbf%Ônÿ\x0000{\x0003>õËÃéHÃ¿\x001f.U¹j£JÃß\x001cã\x001cÔúnw©Nb±¦
ÅF:Ulü¤R/×\x0014Éº¾¥«ë\x001b\x0019+	"\x001c0Ü\x000e\x000f^Æªñ´ äô§"þõr2	\x0014Fí\x00126\x0004\x001a@y®Ç¶0éÞ0Öm-b\x0011A
Ó¢"ôUÉÀ\x001eÕÏPÕÂqpvbôÅ(;NG§qHzS=H4É$F \x0010\x000fÐ:Ó\x0001ÀÏ\x0014\x0012sÒà*å£\x001f1²xÇÐÕD+í«\x00101Tc1Ú8/5éô¬Àì\x0010÷\x0004Ã\x0007µz.ãÆ\x0011Å<\x0012±ã\x001eµã6rælà==«zÖf\x0018ã÷g\x001b¸\x001c\x001fP}k®k{²8±xe5Í\x0013Úô½{GI¤ìaO´\x001e£8ÝÙ8\x001e-ÿ\x0000ÙõÙQbQ\x000c£Ë\x0011ò\x0016\x0019È#Ñàþ&¸.L½üÔ\x0019\x000c§;mF-JÒ)Ô\x0005½\x0005\x000fã\x0018ûàû÷¯F\x0012<iR³45`Ö7\x000fï!\x0007È\x001f|g®;7¯¡¢;è­|È­­äÊë\x001fk°Éb:2èÃ}FE]¿¶thö£\x001bu\x001c1\x00046\x0007Þ\x0007¨'£\x000eü\x0011È9Ê>Ñhë´nn!Ý\x0018ÏSê¹?Q¦¹Ç
¹¡a%æ\x0001Ô4yæ»Ð¼Ð¥P\x001eÖFè"ö\x000e0¯Û\x0007Seã{Ø¦=¼\x0003Í 0,_\x001d0\x001b#w¶?\x001ekð¥íïöå²Ø+\x0019ðêñ¬^h,\x0013"<xÄ´\x0013´÷\x001cs]¿ü!ñÏ:\iJíjÁhbÞÀÉ\x001e"N@!\x0000ò\x0006A'Qmm#¡T·¿\x0007©è^\x001dÕmï ky¾ø*À""çÜã úö®ªÚ\x001b2^¤c>bÃÊ¼7D¶¸³ ¸!K3 Tàü¬\x0008<Þ·ì5M@8ÌÓ$\x0013æ2Å@y\x0005NOÊ}\x000fN2*%Cá4úìÞ²g¯ÚO(+\x0014ò
½ÁÏ¶F*¯Ù¢ÓÄí(7D\x0006qý9"¸-
æUwí33\x0006\x001fòÕq¸ë×­z.e\x0019Ë)Gd*G^½r;×=Z^ÊÒ"gR\¯[c6¬ºi`±Ïs\x000bªQ×\x0018<þx©ãÑìoôØnô¦ÙÜ³Û\x0011È\x0000\x001c¨\x001f\q]n­áÃ2\x0000\x0015J\x0000F@ÁÆs×Ö°ô«	´Ôsl\x0003:³¼¦E;P\x0015
 ãwÎ?:Ö5.´\x001c¨FNç\x001d§Ü¼2`ÁPeyúcÒºåå\x0016)O\x001bw\x0002;Ô×vV:ä"kF\x0010Þ6Or\x000eF3Ï\\x000f\W&ÓÝXÜ²Ü¡É$´mÆyëìkuilyþô\x001f¼iê\x001anà\x001c.Pÿ\x0000\x0010è=«Õ4ï-\x001dUHùºú}+¶²¼\x0017VÁÝ\x0016í¹ÿ\x0000kÐûÓu+\x0008Þ"U\x000eàAÏÖ÷W<{QÒÕX¬6''\x0019\x0007\x0003¨úû×\x001dªéÊZW@T\x001eòyè2=«Ù¯tÌ,:@\x001d=«Õ4ÒÞcmÀf$\x0013v¸O#¿Ò\Yý¦LªoXÐwc±ú\x000e\x0007ÔÖ\x0008³FºH¤!Gl\x0019\\x0012«êN\x0001?¥z>³a5ÜÑC·s*ùi\x0018^\x001b¿Ëîk¹Ó_Ìh¢Gv9;Bä\x000c@ì95Ï:w=:\x0018±É2£*ÅÍÊµµ¬JÊ±îy3üR\x001e2=°\x0000üêåÝ¨ä\x0000ä\x0001Þ³Z>>ú×\x001dJV=(TRD
qñ«6OvN²,qÛBfvlô\x0004\x00008îYüj©\x0018þ¢¬Cw4V\x0016Ñ±ÎW\x001c¤3éÀV:";PÍp¡à\x0005äúW×z-»ü\x0016ø9}«]¢ÉâËØ<ÕNL 
§Ô&à[Õ¸éóÿ\x0000ÙÓÁ\x0016v·_\x0011|\\x0016\x001d\x0017J
% pò/Y\x0000î\x0014ð¸êäzU\x000f\x0017øÊïÆÖ~.Öo\x0003Ç\x0013Z\x0008í c&\x001f9B©êOr}1X®jòöqÙn\x0015%\x001a)Mîô<WP»þò{»ÉkÝ¤G9gbrI>¹5Zñ\x000eE6´µ´\x001bwÕ(æ
îîzP	\¥%)æ\x0005\x0014Q@\x0005\x0014Q@\x0017uK	ôËùìî,Ð9FÇ ûÜ\x001e úUNÜÖ¦¡{.«öf8ÄÀ\x0016AÌxRÞø!xì¢«ý¨
7È¸ÎM;\x0014Ò¾03Û\x0008ÚH5#d(À>½ê0=z}i\x0012\x0003¥\x0014à¹¥XÙÏ\x0000Ð\x00033ÔV¢ê:ÜÅ¤ÚKu$0½Ä\x0018ÉXÐeý+<¤ç\x001fzÿ\x0000ìÃ\x001fÚ|u¨ÛÏ}&ê<}TTÎ\©³JpRãùÆA¥FÃ\x000côþT²pÌ=ê3Ö«tK÷dt_\x00105{MwÆ\x001a¶§§,©iu15\x0000À\x0010:às\èëÍ\x00189æp}hJÚ\x0004¤äîÀôÇjzòØ\x0002O=±OO½ß\x0018&"X­äu,ªJ¨9=ª<`\x0012@ükÙ~
ë:\x001eá/\x001aÏªÍhÍ¥½½¤3ºf \x0007©È^¿ZñÛ½¦áö\x0013¥LdÛ±­JJ1¹\x001a\x001c?=*Ä,\x0002ùÿ\x0000óÒªëORpx5FH»aó\\x000eØëÅoÛ\x001c[¼ú«³Îõ`Oø×Ie\x0014¯nò\x0008ÜñEÒ.1rZ"=+Q6SÛ\x0002,àqÓ×ð®qq
ý²!Î\x001dIãµÅ]\÷$ñÇ_Êµ<9®\x001b\x0019~Ít¾e³ü»[µwQ«Ñf&ø¢zjöî·6CÌ¹ØO\x0004w\x0006´®ôò­\x000e¤!Øè¥°9\ö<àÔ\x001e\x000f¸ËW\x000flçänê{]F·$FÖÖÍQ\x0014C<þðKqÛ§å]½å5\x0017w3ÖQío¢¾²\x0013ÀJ£Å`HéÇFÇ\x0007×ñ®ÏÅúçÚãï \x0017`£Z5Wù\x0010¨\x001cîTõâ ºvÕ4»¸ÔD¬Þ[\x000c,¼IÁôã\x0003¥s\x000ce²¸;¹¤((\x001bã<®OCn½k~U%ª3sä{îze¼\x001aèûG ÔÜ\x0019.´È	p¼$\x0003×¹N½Ç¡~(DÌµ®î\x0007ð:ç¦zW)¦ê>k}¢Ýä@:3*\x000c=×0}½k¦k÷¿½I$6~A/>JÎ\x0006\x000bö\x0004ã\x0004àg¿­BN.Ý\x000b£5~§Wa\x0014pÜ\x0013
ÍÁÕãö÷ë^á¾Ù~hÛnT`\x0010G¨9¯-±¿f1;J.¡]ï\x0013È]¢\x001dÇ¨÷ÿ\x0000&»¿\x000bÈ0\x001c>Õ=ÎAoÎ²ÄÅÊTj*uoc¶
1qU\x000eldÚ$c'

Y÷ 4ó^=Ú>(É&sm¥Úhëyr6n\x001cª¹\ìSÔqÓ¡çé\\x000e¡qe¯M&vÑÚÞ\x0007%%ngOzõ«ØVâ\x0006ÆTõ\x001eµæ~2ð×\x0015ìE4d2°\x0019ÈôÇÖ»ðNêOSËÇ§t­¡Å^ZK ßºLùL\x001bö}À?ZÙÒµD\x0002¯\x0004\x000c:1éôõ\x001eôÛmR;¶m+_Iîel¸0\x0008{t$ñëúVN«£]hÓ«¦öÝNÎ»|æM8ìæÎ)Ô´dí\Åæ\x0004\x001c\x001d¤pvþ­m/Uo,\x0013²lr¬F×÷\x001eÚ´æ)²ØRývÁ÷¤;ÜòMSKC\x0010¯æ\x001dÀ\x0005Â÷ÏøW\x0019¨ØeFíê
o\x0007\x001c`ä~_{}þ7î1\x0017#½r:Æe`0z"¹ÿ\x0000>´hÂílxÅÅ\x0015ÉÉp\x000bpz`ÞY2äÆ2¬ÇÆkÔum\x0011¡w(É$\x0010Ã\x0003\x0007þ®Êê\x001ad±îIw+`íÈÇ\x0003¾}ë9A3ªw\x0017©ÁÏ	½û\x001aunákÆØ8ó6\x001c6Üò\x0001õÆkjâÕ\x0015FB¹ã
só\x001aÌ\x0017wvdP@$áqøW\x001cé\x001e½*êZ¥ñâ¯4­+Ã~\x0015µOðÝiX\x000520\x0018P@'åQïÉ$Õk\x0011´øe«MÆt\x0012AÈÉ\x001fä+·¸ÚÖEû$2Îù\x001el¤°PF>UéslWc¬Iö/Zuªð×rùî¹ê¨8ÿ\x0000ÇR¡IA4ÅÍÎPõ<é¸4ÿ\x0000xÓEr½\x0019ÔI\x001eÁËþBÜÈÙ&+WÃZ¶«Ewy§Ã¨BÌ\x0013}ÖúÔ³HZME»#(JÛñfµ\x000e¹ª\x001b«m:×NhQ\x0005º£ò¬ZkmER1ºî \x0014TBó6Ô\x00194ëwýM+­\¼ÖÐJp¦A³lÐÃ\x0011b Èy\x0019\x001cUk¹Zr\x001cçÞÖÊ³\x0000G^£°«\x001aQÇ\x001d¬Ð,Ñr:üÀàÖ©[q»É]t2Üå¹Í
¹àúé\x000f-Rt`qúVopE»X\x0011Üc©ÇzlÒ\x0005;c\x001bP÷õ¨¡%A\x0000ã4p§éJ¸Ç¨!s®óà¿-|\x0007ãhõûYîm\x0012ÂÑÀFó¹p\x0008Ï\x001dqþx®\x0008rã5#&\x00088ëYI'£*7Z¡ò~öf(1$\x0001ü¨\x0011\x0018Ë\x001e+ODÑõ-^ëìúMÅíÀVÇo\x0019vÚ£$àsYó\x000cu\x0007\x001e¿ý~õqK I=Ù^\g\x0000¨Å9M/ðç#éI \x001fþª±o\x0011eãî¡?Ëüj\x0018ýMhÚqgxëÙ\x0011sî\\x0016*;å\x00065Û	\x0019À?Î¡<þu,¿ë0~R\x0000\x0006>Z¦µ±7\x0019°\x0012?:QÂ\x001eGãJÄõîy§¤%\x0014ðiX\x0012¹©á\x0014_\x0010Ø­Ûª@%\x000eåº`sý1ø×©Ç=µÜ77?.$y\x0018c¸É\x0003ô\x0015ãúz
Ç­tö\x001aédÑ©<
 ×5Z.rRLõ0X¸Ñæ=îD¹\x0000\x0011¨ª\x000e\x000eîIúVæ\x0001ÆO \x0000þVtKu\x001c\x0001Åv-\x0011äÉÞM?<K6åÆÝAáá÷Oô?Î½RÏÄpê\x0016 K\x001dÿ\x0000	ôÍxBrBçéôJk@È\x001cù=G\x001cúW]\x001aéi3\x0013æ÷¢z½£ý¯÷S1Ê\x0003²By#\x001d\x000f\û\x001a½.
õº$ì\x0004øçrçpü\x000f^?Î+Ï\x001eîc\x0014N²6Ç]àÓñô÷®GÖ¦ºMÒ³ÆB»9ì\x000fà
zjIê\x001aTå±q<?\x001cY\x001b\x001b\x000bmlã~¿lÀtßßp\x0019P\x0002\x00158Y\x0007OqéÓ½fOv\x0012âE\x0019uõ?ýoÒªÍ4\x0012ÇºØl`~îqÏ¨>¾½«E\x0015-ÙÌç(icµú'X±çìHÖ11;¤sÁ\Ôm'\x0018®ÃúóÏ*FæmÊrã8\x0012óÃ(ç\x0007\x001eý«Î|=r&ýÝü°[¨;\x0000¶ñdý?:ôí*Þ\x0014&\x0016"\x0018£aæF0òãLt89=>ø¬ç\x0014·.2ç=3H½A8f\x0003ÐñÇ#Ö¶Á\x0004\x0003ë\?lÈ»6</ÖA÷ÈÏsî+¦»º'+\x001a|ª0\x000fl×^S´Oo\x0007p¥yì*«{\x0004\x0012Bþr\x0006]§=Gò¬s¬:HV@\x0014çi9à\x001fQ´¼XrsÓv2\x0001ô8ÿ\x0000<Ô{)ÇSU£UòIâ>7ûN\x0010«*\x000069ôç9£D»±´³M>ãSK]ts@aÁïn½}*ìüKmn²£\x0008\x0012\x0006ùU\x000f×\x0005Xä\x001e à×ë}³´\x0016VñË(Ú]÷nÏ\x0000\x0011Ð\x000fÃW|gÌ
b:L·®i\x0002ÍÖâÎDMc,xa\x001fýó×\x001eµ&«\x0006EI]ÑØp}\x0003{ûñ\gõ\x001dGÂ<íq§È1%»ò\x001bý¥'ß\~5ÛÏ¥Ùj0E©èëi Ì±yD²qýÐy­ô<ºe\x001bÉ-
è:²ò\x0006\x00085¨éË Ç¸ºªsúV.©y_$ÍæB>ëó¹;síú×_gr'R¬ñ®\x0014¾òHÝÓ\x0003ñ¤Ñ0ô8
KGbÊfv~WS·\x001eâ¹}kEóT$Qª\x001dÁaiÎ1zÚ½îËÌß0#k\x000eïL©8<\x000crséM.ârkcÂ5\x001d	£\x000f%°T\x0017\x001dNsÅss\x0002	\x001a9<·\x0004©òÈV#Ðóé^í©i\x000c©	¸1ûÊ\x0008\x001cuä×;y§;<\x00115¤\x0018
óKº(9'ÀéééJQ¾ÆkrîÏ\x0018°Ñeº\x0010¦U.ì\x0011´Ål|NÛmym¦ÄùÊ\x0005`÷\x001c·þ<qøW£é\x001aH°[ÝbñQ"°_3Ì \x0000ÌyU\x001e¼ãõ¯\x0013ñ\x001dü£qu+\x0016gcÉïr>k*B'v\x0016¤±\x0015nöF+sH(4å\õ8¯)î{\x0008o4ö9àt¦@Ä¥¤¥ \x000b\x0016·RZ¹h±zifÜçVW¹|òqå¾péÐÑðæ¨xYµÒ´{Y.on[dq§êIè\x0000\x001cx\x0015õ\x0016ðëáW4Û}+Ç·ö\x0017> ('¥Ónîª½\x0014còzñ+:4ê8Ss>VrLhyéµ³ÛüÜÖ2OÊxçSEÎS'\x000c8úÔ\x0012\x0002	Èç½u½®b\x000cf¦aò\x000c{~\x0015
õÉ\x0015µ é3ëzµfP\^M\x001d¼[Î\x0017s°UÉì2EbÝ¬"å±\x001fãK!ÏóíZ&Ð¯<5®ßé\x001a¢ª^YÊa)Êäw\x0007¸#\x0004{VD¿¥h¥îµf\x0010d\É¯«¼\x0005à½\x000bUýoîäÓmßQ6×s\x001b@d\x0012FX¡ÝÔ`\x0001À÷õ¯"Îñ·®kí\x000fÙìÿ\x0000h|\x000bÕm:áîàÇûÑÿ\x0000³Wm%c·\x000eí\x0006×tyOì£òüKhÿ\x0000ç¥éÿ\x0000¸kÄu4\x0011LÉÝ~\ã®+Úÿ\x0000eÇ1üYµSüV³üt\x001fé^3â%1ê×HF\x0018ú1­é;\x0012ØËïÚ¹<v¦\x000fÇ54kÎ;JÕkQsúV¸#C½|u$\x0007ðsý*9ÀëùV©\x0001<"ÞKö\x001fÆ?øº.8õ1äûÓqÉ\x001d©éR\x0011ÓéUrB \x000b\x00003ô­\x0018â\x001bð{zU;T
2ñÓÒ~ý\x0000QÇ¦?Ïõ¡ì\Q\x001c\x0011\x0004¼\w\x001cÖµ´j\x0011²9ÎF\x0005PµÆ\x0001\x0004`ð;w­8A\x0008@ÁúÒ@Õv¿¼ÈçëÍ_m&\x0008¼\x0012uYÕÍÅðßæÀÚ«8úY÷;ddyÀ­?\x0012k_è\x001fÓ,¡$Ó q!|~ògbY;c\x0000UJú$:\x001cJRÞÚ\x00181s·©ç\x0018Ílç\x0004ñÐ\x000cÈ·Úp©\x0019Íusèó[è6.äxâL|Ä/VÏ¦r(¶äÓ¦]
vóË\x0000fÎÜà¡<~\x0015©¥ê\x0003d\x001d\x001b8#Ü\x000e.Ed\x00001d{ÐËÊ\x0013¸=\x000f=ë¢w\x001d\x001eÇ-\<g¬w;];XgØ¶S÷%S×ëÛÛÞ¯ËÜ½¸
øùOÞ\x001eÕÄÙJeÀCÏ1¹áÏ×Ö¶ôíNX$\x000b+0Mß31ùöÏ·NkÐne¡ãÕÃ¸¿xé4é#2®71<pW\x001cõèk­Ño×Lx®\x000e\x000c\x0000\x0006ZN>à\x0007ï~|\x000f|Vw-tíkTþÏ¿ÛÍ:þém\x0012°çÓð#ùÕ­OK:eÕÄ\x000c\x000eÔl7ËqÛëÇZÞ5ÕùYÍ<\x000c¥\x001fi\x0013ÖtO\x0010FÚ{ÜBèìà}×áO8^psè\x000e>¦¨ÃâëÈ!/ï	v\x0005\x001bæ8ï\x001dÕåt÷\x0016·ßi	\x0014`*w\\x001eÿ\x0000Ö*c<\x00121L\x0000¨@\x001b~é\x001dÿ\x0000úõ¬hS¹æÊU!£Ðô§Ô\x0017QB¾X]KÌÌÈqqý1É­->êF¸Xïí#Ø~Y#q³æÉØrO×½yÖ«½ÄAe1Ê#MÀùÛÐö#5µf,Ð)QæÈ\x0018<®\x0011\x0014÷\x0018Áõëü¨«EZÈª5w=FãNö \x0012k²¸\x001b¡EÊþò·¯áõ®\x000fZðÆ«\x0004Ó\x0018äi-±GLÈ\x000f®W¼\x000cU\x001b]nëI¼+\x001cæÚ6\*H	VÆ@Ú{gë]\x0005§¢¸Y\x0011Ó\x0008ed\x0000g\x001c\x000e_zóeBt\x001eÝ<Tj+3Ëîl~Ò¬Ñ¦ÉÌ.\x0003\x0010\x0007l\x001eQÈ«ú%ôÞ\x001c\x0018tYD24æâFE2ÈFÑ´u\x0010|¸ÆY·tâ½\x0012é´ÝN6Hb¸\rÈ\x0001>ä\x001bõ®n\x001d\x0012É%7@Íq J¾â
\x0011Ç*x`8ùZM½Îª\ªéuî\x0017V\x0010êé=Þ\x0019î6e¸µ`A$c±\x0003ùs­£N#-\x0014Ò¬1©Î\x001c1eol\x0003ùV°ÓÅ×W\x0012<WqÈÏ\x0015ÌN0ÃxàA'\x0004`Þ¸©'¶Mr\x0011w\x0004Me¨.Wm\x001fCüù­¡QKC¶\x0015Ò|Û£CO¸ó#BÎ¬\x0018\x0002\x0019\x000eGëVäµó{.ì×\x0013m}%¼Ëòm*vÌ9ÉË\x001fö¹ú`W¦i°o\x0012pÝ~µr|ªìå½ôG-y£1\x0008¥±Ís:!g	îl\x0010Ãþ·\x0015é×q¢8êIà\x000fZð\x001f\x001f\x0012`Óí¦Ò|?*\x0019¤ÊMp\x000exäa}½ûÒ¯¨ã\x0007Qò­Î\x0017ã\x0017-Ø:;o\x0003\x0013;«}÷è\x000eßy\x0004Í¸·+ï,ìAbIÉê}jÀØÅ­rb%t}\x0006\x0016¥\x001eT@y4R×u\x0014ô@~ñÀÅN^\x0014Mª¥\x001c\x0003±RR\x001ei(\x0010b¤·Í<q©PÎÁAb\x0000\x0019=ÉéQR÷ \x0011ôôÚþ\x0001x@ZéOmªøóR\x0019n\x0007Ì)ä}\x0010\x001e«Æ\x0005|ß«jW¶¥q©O-ÍåÃ%FË3\x001fZ¤I=M8`÷?g
J-¾¬Òu/¢&\x0000Aç¨4ë \x000eÙ\x0017£~½êÉ´(Á \x001c\x001eµ\x00109\x0013\x0004\x001c\x0003­o	]XÃR®9\x001dþÖxb
KINñ\x0002Ù]\x000b+{¸Ùn¼¦\x0011\x0019\x0011í\x000fÐ·\x001d:×;%»E f\x0004/PHÆkéE<Mû3ø§IÀiôÂ×(\x0017\x0000\x0016QÅ\V\x0015î´:0©^ïú¹çßµ\x0006-þ-ßÜ ýÝü\x0016÷+C\x0018Sú¡¯\x001f\x0015l:÷¿1kh\x000f5ÎY¯4a\x0004êñm'õv¯\x0019¿ÓZ\x0018\x0015F:ÕSw\x0015£gc*!óðyãû\x0013öIÏð>·kª^\x0003ÿ\x0000}D\x0007ô¯ß*ÝÀÍz¯Áïw\x001f\x000eàÔà[\x0001{\x0015îÇ\x0000É°¤\x0008\x001d¹\x0007<jÇ\x0013MÎ:\x0017FZ8_³¡0|jÒ£õûDg\x001fõÅÏþËÒ¼·Ç\x0010y\x001e&ÕW°»G¾$a^û:Ü\x0019þ2è\x0012\x001eY§l\x000eÁ.qù×\x000fñB=¾+ÕûcQ»_üiÒ[×lãWï
3Ó\x001cw¨Ç^Õ 'óÜáLþ|	Ç\Ð×\x0012µ´væBaGgXû\x0006 \x0002\x0010£ò¤ÜDmÏR;úT~úU%`lHÀÈÏ­Z¸#¨\x0004\x0010FF
V\x0007?hK`\x0000\x0003ÿ\x0000<þ´jØ(/9\x0004ûúUè\x00173J\x0001$\x000fQYðI°øûU»V
X\x001cA\x0019ÿ\x0000&WEEÙCó]¯Ìx\x0007JÕvG\x0007#\x001eõhC]\x0002\x000f\x0018ãüö­¨°Ñ\x001e;qI!Ëc"ìb~1~¾ª£æÈ\x0004\x001eÆsZ7é2s:VtäG=³ZÅ\x0008[¢S%eK6\x0015I8\x0019ö¯Cø%¼ZÍ¾a {=&Ö;Ed9\x000cøË~qú×&>P9\x0019îkb0q3êHëúÖSÚg]*Ü´å\x000bnJ\x00026yõ\x001fÒc¾{Sò\x0006p}é{öäôªFLDÛ\x000c·Ëä©a­2Êa¼.ê§åOÎÝ~aõæ´%Ç \x001dHî{×+\x0016
Ôç?ãZ)¸+£\x0017MMÙ¦Þ´Vá¡&·ÎwFN\x0001þjzW`|as5KìI(M¾{\x000f\x0001ÓxÏ-î9¯#ÒgÞ`ðJQÏÞî\x0008ô#¿ã]E½gs9KµKi±·Ìçk\x001e\x0007ü\x0007ñâºib!-%¹Ë[	R½7¡ÑÛëW¦`]Ô£d®Tqîr\x0008õ­
ÝÆ\x0019?~9\x0004\x0013Ï± ×=%Ú©`K+\x0013\x0015?áü©ö7ÒA&è]Eä£\x001aôaRÛ\x001e5Z\Ú5©ÓC©Imæ=Át¸å*\x000e\x001b\x000e\x0008íÆqÏZÍ}rkk£.ù\x0011e]®¹Ü\x001c÷ôÇô¬íC\{`\x0015dùN\õ8íÓ\x0015Jòx¦(±0\x001f8ÈÀ#½ò+«Ú]\óþ®ã+3¡·×_ÝÊÐß+BXõ#>Ã\x0003¢·\x0012â\x0011lÒÙÝº\Ç.6\x0002'<27ÞëONÂiv©.¡\x001eïº\x0008%wm\x0007Û=¿ZÜ³¶\x0016á¥
åBdç\x0018\x001e¾½ê$ùJ*¼NÂËÄ×)m\x0005³¬?xñ2q\x0013ø×ga®M\x0011¶\x00122J²©xÑÎÆ\x0003Fzûò+H\x000cdÂìTüÄ:\x001b®>(\¾½»m<ÙK¨YIþ²Ö1µÇO\x0018gc\x000cuèz05ÉRþ\x0013¿\x000b^òµGd{\x0006¡âÛIt\x0003qfÆ8í'ÅÌ\x0013Ç³`-ÐpA<ç\x0014\x001e­\x001e£cpº|>Y\x0012\x0007iÙ!b=\x001b\x001cñé\.¤êñÞùºÜ-n\x0011íÍ\x0010k\x0008ùVl\x001d¹^Ç=Æ1½o£Ái\x0010£D\x0007\x0013O!b«Ü.xQì 
Æ4z³ª¶*+Ý¦¥åÞj\x0017RGY\x001c\x001byoË¹þµÝ]jºü;\x0015Æ¹y\x001d¤1DªYÛ\x0004:\x0001ÜûWjß\x00134o\x000eÇ!Òÿ\x0000âa¨Æ8oõQ\x001föT}æ÷'\x001eÕáÞ+ñ6¹âÛ·Ôu{©¦@~@ä\x00009è§åENÌ\x0018wW[Xôß¿\x0019îµÃÃêöº{\x001d»Û&\x001e§Ð{W²Ï{0yYòÄäÓ¢É2e\x0000HjÐO9b\x0000+Üp£ß\x001e´^êÇl!\x001a:Ejg\x0005×t\x001f4®@\ðOb}»ã½c;\x0017bÇ©«ó¤*\x0011íøtZ{´jÍÀ5ÃVóvGlZo"\x0014¦t©\x000bÆ\x0001Q×Þµ\x0004\x001auÔì\x0004P±?Jæ~îÞ)Í^%?­\x0015bòÖ[I|¹×k`\x001cuâ«Ð' QK@\x0005\x0014 g¥oh\x001e\x0019Ôõ«'M°º½!Åk\x0013HÁGr\x0007AJRQÜÒ)Tvok$çä\x001cw'*y"¶´Å\x001c\x001cR]\¿Í\x0012\x001cc¿ãTªUÞ¬·(SÒ*ìõz>©øN·Öæ·Å¦\x0006v@±~b¤öÈ\x0004\x000f­Rñ\L:î¥&n±ÚÉ,Ú,±ÇUNy<b³fÚ3G\x001b|\x0006ÿ\x0000¼¡ÏåUt],õ9üûHî¢ÖkvI\x000eÜoB¡³Ø©Á\x001fOzªPw¹ug\x0014¹Yª\°ÍÉ+òóV¼M¬èq]ÚiÓZÛêQy\x0017)\x001b\x0000%B\x0008Áôê}ù>¦°n
NqéN?-¼N¿x\x001c\x001aÒ­¤ìsR¨÷ÍyQý</z>vÒõ[7î@pì\x0007°å?JñB_9' pEiÛø«UÂW\x001e\x001dK¡ý=ÒÞ<^X'Ì\x0000\x0000Cuì8ïÅy\x001fiÑ(ëÔæÕ\x0019
#Ò lVmµ\x0014ß|r3V]íöÆ}9¨ÔQZ\x001a¾\x001eÖo4MZÚÿ\x0000L¹Òò	7E4g\x000c§\x0018ï×xô5\x0006½u5ìpÝ]HòÍ<Jò9Ë3\x0017É$÷9ÏçT#b¬¤gÖ­êÉ·LÒÏ÷SÇýt#úUI-\x0018ÔM\x0019Kß^Õ<Iæ8\x001d\x0001?W\x0007µnû\x001bp\x0018\x0014¢µ%ìZ\x0016èZG\x0018\x001c\x0000;ÕI\x0000B(^\x000e;Õ©\\x0008F\x000eFNO¯µgÈrO¥k-\x0008Z8=_j¶A\x0008§8öéPùl#z8ÿ\x0000>ýÄ®\x000fAï®Sv\x001aXm$äñ;ÔÊNÌ/\x0015\x0002
Ò(\x0003©íZF\x000cÈÃ°<N)=È´ò~Ò\x0018\x001e:ÿ\x0000]\x001c\x0018òØ\x0002{ñ\íeoy\x0018ã¥tVcå$góÿ\x0000\x001aI\x0014ÌÝA~q×¨ézÌeÃÇÖ¶/ãùr@Èâ²\x001f\x000eH<õïZ-:)`S<cÛ[1\x000eIÇãYq7CõÈà×QáÙìíu«\x0019õkWº°eiàS·Ì@rW>ÿ\x0000Ë"¢mØÖ»³#¹³Ö\x001bv¸·$<ÈüÄ+½s÷£Þ¡8ã@À®Ãâo\x001fÆ:òÝÇ\x0007Ù´ø#\x0011Z[ñNå±Üú\x000e\x0001\\x001c(Ï'¶jbÛWfµ\x0014S´Hç\x001f¸<\x001cz×'\x000eEÄ¹$WZã1J1ÐW)\x001aææ^é:¹|&1øÍ60JÉ'ÚªÜd9É$þ5b\x0011ÈÚ0G\x001dHª×\x0019.I\x001c¹¬\x0013Ôì¶¯_i\x0012¢K\x0001æ\x00179Cþ\x001fwÚFµ¡kô
:ì\x001a@LdýG"¼©X\x0000¹\x0000\x000eÙ«Q\x001c\x0000\x000e:gÿ\x0000UtB¼©0ënMñ7u\x0010\x0012ö\x0008<ëv\x0018Kvócltù@>Ç\x0007Ú¹Obd\x00176¤î?xb®ü?×5+\x001dI¡¶¼"'"1!\x0019Û¤vë×5ÝKâkGÀ¾Óç8_Çó{ãøâ½l<ÝHó#ÀÆQxyrî\x0017K¸+)\x0016ÑO6ïàE\x000cqú×£èw÷\x0005eO\x0005\x0018#ínÌãß\x0003¿Ö±¤ñ]Á;BÏ4n>\x0002Þ-Ô¤D{(Ò(íG1ðÍÇ\x001dë¢ìó'\x001e}FµÑmå·Xî\x0018ÈPçËL¤g@yüM\x0017º¡A#_ß[ZÂÝ\x001c
\x0019ÿ\x0000ïïõ¯.Ô/üOx÷kss'j\x000eð\x0006\x0014\x001fJóÛ¸]e\x0006ç\x001f8Ï\x0007'\x0015\x0012¨áù·g¬ë¿\x001aìtýñøgJó_ ¹¾Ã~*\x0005y<iâ/\x0015\u=Jg\x0008×åP>²¤sJì
¤CûñÅZ\x0011ãb¤x=K\x001fóÅavÙéF\x0014é/u}åh!R\x0002Êq\x0008;\x0013÷ùïWon¯2«P±FF\x0015\x00060\x000f½iXÙA,/6\x001a[ÁbAË6=;ÿ\x0000õ«Q<2ö_é~$w3\x001fìH3!ôÝýÁìzÒ²fÍ+³±°à\x0019IHãÉfvà\x001cT:¯²$\x001eC\x0003	ËÄÿ\x0000Jê5Ôû@F«\x0012`\x0004EèOáé\ìú|«!i\x0000
§\x001csÒCÜ®s²Ã$aduã°8­;;¸Ø\x0008ØÚ¦½µ¢p\x0010ñÔ\x0002pk\x0019¬îF\x0018C/Ô!®g+\x001d\ª´»2\x0014wòF1ØÖrk·6ð¼h®NVAÊsúþ5»¦Ïl¶þEØ*äs¿\þ±jÌÍ\x0010;3Æ9®yÆ554¡*q²ÅÌ·N^áÚGõnµ	\x0018çµ\x0004ð\x0000þTªØàô¨ÓcfØÊQR4y\x0019^ì
þ\x0010&¡¦ÂWãûìo	Â¢_Þ]\x000eØî\x0014úõ=\x0014sä ®Ê\¶9¯ÿ\x0000\x000bu:kqö=\x001a\x0006ÿ\x0000IÔ%_\x0000äªôÜØíÛ¹\x0015èÞ4ø¡|>ÑfðÂe_0ÖC<\x0012Üÿ\x0000µÐs´w®gâ¿Æ\x0007Ö´õðÏ-ÿ\x0000±¼%n¾RÃ\x0010Ø÷\x0000wltSýÞýI=¼pÉAÔ|ÓÛ±³¦¹c¸®ÅØ³\x001cÉ>´Ê^¦Vç>ç@fm\x001c¢\x000c('8\x001cgñªË$~q}y¥$-×89¨î7\x0011ÎsÔþ½ëzvH·*^¯;§£\x0011S[¦û7È\x0000\x0003ÁÍ. »3\x001f21¨àÿ\x0000*È\x0006@rNzzu¨¨µ* ò0pO ÿ\x0000>Õ*eÈR;c¨lr:åM7%\x001bv\x0006\x0001ÇåT±-k©ézß,áTè&ÒÖîKù¯'µ½\îPT¶Í \x000e8\x001f5Äµ´f\x0016X\x001d\x0008ãç\\x000eµ×¯íeø5/¥ax ¾_Ç³fÒ¾¹ÎOB9®"ÜlxÇqõR[Råû%\x0019\x0006ÆÇ8=\x0007LV¦¼¡t}	±$\x0012°\x001föÝÇô¬Û9\x0000ñ~Þ¶|Pt/\x000bÿ\x0000µc)Ï¯úTÂö2Ñâ`Ð
°ÃiÉ'?LT\x0011pÃ°üªÄ¿:d\x0007Ozdî\x0017!W'©5\x0011\x0007©<zõ§ËHóÜn\x001fLÓ#\x001f)ïÒ­Êú\x0013k\x001aSÃ\x0018y\x0004ôÆyª$k]×ug¯ËÀ\x0018íYR)\x0004sÓ>´-
¸Ä£«ª(­\x001e_µI&@
×=EdÛeUÚ\x001a3ÔVþ2mùFz\x000fóïPTFÂo@Ú8ê\x0000ý3Zö\x00149\x001czÕ\x0001\x001e/\x0011±Ï<zµ§h\x00041B\x001bØ§¨\x0001¸=\x0006=k
$Á\x0019\x0004ãë[ú\x001ccAíÞ±]@\x0019À<Ù=\x000eg¸°°<qÔw­¸ä?/\x0004vÿ\x0000
Í´¶]ÞLNû\x0006æ\x0008¤à\x000e¤ûzÖÇ\x001dFqè*\x001bLÒ\x0011kq6\x00079Àë\x0015H=pzt§¨ÈÇò \x000cø÷üªK³\x00128Ù£&æ8ã¹ÿ\x0000õÕ/\x0013ø7]ðÜ\x0003_°Å®ãó \x000cÀå{ç\x000722:×±þÏ~\x0011\x001aÿ\x0000þÝs\x001eí?LÛ;äpòdùjxõ\x001bÓÞ¸¿^7_\x0018øþé­dß¦Ø\x000f²Ú\x0011Ñ?3ÿ\x0000À'è\x0005a*ÍÏ\x001bÓ¤Å¹ÁÂ>CÆ\x000fçU.1¸\x0003ÓÖ® +\x0018\x0005qéÓÿ\x0000¯U.q¿\x0000dzh×¡\x0002\x0002NO\x001cã¥^³BÎ£¦8\x0007üôªQ\x001cc\x0003§¿\x001fçüjê\x0002¹$ñ¤\x000cZl^ÒoVÇWåpPnNºËßùÔ:ÝÓ]êÒL\x0018ãiööüj¤¬Tç¡=ùúR\x0008Lg ÿ\x0000\x000eÓìA8éí]ØZ¶\\x0006.æöYádîîÙò\x0014%ù\x001eNßëô]3Nû=IÔ"XÚG2 Q¹%\x001cqÜó
Äù¾[³\x0003aW$ó^¢.k\x0016ù­î&<æI'Âð2 Zõ¡¬OÄ5Î^¸Ð'³æ\x001býn)¤»û[ýîps^a®XÅ
ìm(\x0013ùûÇÔf½ßXÓ
ºÁo£Ú£+\x0012\x001b' ÿ\x0000:ÎÚÊvÍe;\x0011S¹ïÉýzÔÚMN\x0010Z3Ê´í2[éÖ+xÚY\x000e0¨9'=z÷\x000cü\x000bó´E¼ñ\x0015ÿ\x0000Ø$|6Ås¨÷ÏCíÍG£ë\x0010Ù¨ÒÞ\x000bR\+M\x0012)l\x0001÷AÎvúµÔÚøÞÊCkæ4(\x0003:ÈÙhÉìA==ë*ÉØÞho-NlÙØx~Y¬<-§I\x0004­û¶¾¹;î$$óÈ1ýÑÒ¼ÿ\x0000^ÞYcísÉcùÏ×¢ê:¼"ÎöïgïÁÀã$\x001czWß^ üÂ\x0010I\x000e\x0008Á>ßç­g\x0015#¥Ô§%fÊ-içG
< Í\x0018\x001bI\x0018\x0003\x0003Ò±/^),¥
³î'$ïÒ­êzRÐnÚ£®\x0008ÆdÏdóÆ³2I\x00199\x0019¬åMÞò:©ÖMrÃVEi¯Geæ¤¢AíC÷O\x001d3?Æ¡>+@î"´E
IûµKYÓ^Ûk?(Üî\x0015r\x0006æ*¸Ï5°ð§U,EH.PÖo\x001aöðÊêª{ìï]$\x001aß "A¸¾uè÷÷/â¨\x0000®A¿5\x00198ü+\x0017NÚ\x001bF£Õèß¡-ø_´»"*+\x0012ÁW8PyÀÍUïR³\x0018nG­0zVr]Wêu\x001f
u­\x0017ÃÞ-´Ô¼I¤¶­c\x0000f\x0016¡À
&>RAá<àÿ\x0000õ§ÅOÚ×Ä-OÍ¿³éÑ1û5Mû¸b¼ØêÇðÀâ¸#IY8¦îËSiY\x0001æ\x0005møSÃ:¿õ´Í\x0002ÆkË¹?1Â\x000eôU÷<S½ÌP2kÐ<7ðÇ^%ÒbÔô\x000fO-¿êäXáÞ=T;\x0002Wß\x00185ÞÇ£x#àäbo\x0012<\x001e+ñº\x0000SMÿ\x0000¢Y?c!þ&\x001eã=>QÃW\x0005âO5×µYo¥ñ\x0005õo-ì¦xbG@ª§õ9>¦¦íì_*_\x0011lªo"fû½ú\x001eJõÿ\x0000^\x0006µÁ¾\x001cñgt¤JOA}ä.\x0016)A\x000b¹zÅsê3^.X¨Rr
\x001fé^ùð+Ä·~$Òu\x001fÚDö:ÊÚ\æ#=}>ócÔ\x0013JM§sZvq³>|	ÓHï\x0004¼}\x0018§Zn\x0011\x0002\x0001éjÔ²ê7\x0016r®Ç1á¸Û <\x000f®A\x0015J,¢ºòw#ø×Eù¢Ì×$Ú\x0012ãæ\x001d>lçúAp1È\x0003ü*ÄiO¡^>µ\x000eï2<"sÝ³BVB½Ù\x0000\x001cmÎ=³W-\x00196\x0006yäw¦y(ÛÓoùþ´»Ö6bO#¦\x0005)\x000e.Á:åwc<çQß]Op±G<Én\*Ä\x001aXè2Äþ&¥8ÑØ\x000eTu5^Q9þè?N\x0005JZ
²%ÆáþEZEÝ8ííU]v;U|ä÷¤Â$W¤»x*£h÷\x0014ÈyÆsö«\x001aÍrN;\x0003Q&@SßÊV¢fÒôU\x00039Èã\x00150Ý 9ÎïNz
­\x000eKn^¤g§\x001fOþµWuFÁ\x00046=*\x0006ÐË[vfWLø\x001dÿ\x0000*ÜÑQÃ¸ Ö³¬Ü$KÏÌÞÝ­-)±ryç\x001d¿Æ\x0012¢õÐF.F8\x001cÖª\x001eü÷æ³!}×\Ç½lÚ§ËÀíß¹©E³7TB\x000f~÷Ç§õ¬eRÒ\x001bN9èkwT\@Î;bÂ:4¾ ñ6¦[æ^\$ p	ùû\x0000	ü*¥.H9\x0018Æ\x001cÓHú;àÆeàï:õ8½Ò=ÖHå¢QÓþ\x0004r}÷
ùÝÛt>Õ]Ä\x0007N¹Àöæ¾ý¥µ¨4_\x000bèÞ\x0011Ó¿v©# 8Û\x0004*/âÃ?ð
ùö>G9àW¼¯Qõ;*?u"þ§O¨ß[YÚFd¸¸a¼ìp\x0007ækÞôÏ\x000bxoÂÞ%»Õ~Ìaá\x001d9MÜäö»ö\ô9\x0019PF\x0007f}+Îþ\x0010jN­^jÚ¡2^Z[1Óí	3Ü6UT\x00100\x000e2\x0006½ÕÒü^½BðÆá\x001f4K©Ý9Õ5w^²Ï!$/¿ÌN\x0007¢%kQ¶ì](¤½NÆ\x001aü+ÿ\x0000Oj(¼Câ\x0007âs\x000e\x0014#HwJF;*\x001dðkäE|jNø\x00041jïu)o\x0019ö_É+É\x0014a\x0014K!rØ\x000c>À\x0005ÍôÙÀç\x001c\x001at©rE¾¦s©y¤\x0005à\x001ex\x001fJÎº<å'±­%ùr
ýïóùÖ}ÈåqÛóü©­Ío¥ÆZ&é2ÿ\x0000up[üÿ\x0000\bp_\x001c·oOóéM\x0011ù	ä°]Ü3C\x0007áýiê¹áGQéÏÒ­èg\x001du*¸\x000c\x0006@çT¶ÄÇË¸\x0011§¿<~4ù\x0010î#4å\x001d=³Þ¶µBSÑ/å´]ÆèÊ±\x0010H0IO÷×¿ÔWCa<R+Ä\x0019\x001c\x0011Ã/\x0001°xÅqú\x001d½Üú¼6QK%ÌåF\x000b\x0016cÑ@ï]CéwVz«iwÐ6¬FFlæ!\x0015\x0019\x0005O \x0013×\x0019Á¯_
÷dx\x0018ü¶KßÆµî\x0015wäeF8çÛçÏ5Ð\x0010±J²D\x001c\x0010GûÀ×+£Zj÷:ÊXiR> äâØF\x000bp\x000eIÎ1ë¥ZY¸ÙmgI \x000fWÎC\x0000qúï´G:S»Z\x001bË1.­3Ä\x0019HD	ÎqÈ\x001fýz½©jQ\x001cd\x0012È0UäB»ö\x0007\x001cc½sv\x001có¤h\x0014»º©\x000c­\x001e;\x001e~j\x001bûÖiOçÆ\x001fj°\x001d\x0000à\x0001¸g\x0018üj¬f/Ï©¨°¹-+\x0003\x00047\x001d}:å/%-&Ö¾ÕôÜ\x0000\x001dÔ×7	\x000bÀ<çwP?ÎjÍ¾M§#d\x0010\x0007\x001dxÿ\x0000"¡¤´\x001bCï´K{+YîÂÅ\x001cØØÅ°2sÆ\x000fçX/ku5Ñµ·Yå9!bBÌ@\x00078\x00035Ø5¾±¯ÝÙøwMîÞF_*!Ï\x001dØÀu$ô\x0019¯EÔõ
+àÎ6¢¼7Þ6¼mÕöÝÉd¤p {v^ý[
óç^ÍGvÏ \x001a\x000fÞ\x001f9Þ³ÂG-ÈÉ"²g<ÄñíÒµo¤\x000eîYÝòNORNk:XÙ³òûà\x001a¶M\x001cm÷\x0015\x001b\x000exëVd\x001c÷úTe\x000eÒÄ6ÜõÅc8Ic\x0003´ÜúÔ§iîE0ííÆ¹¤h2áÁ58{aÝ±õÉ¨>PG\x0004hÀÏ\x001f­c%sHÏt¥¾UÀ¯@Ò¾*ëZ\x001fSÃ>\x001cÓHG,n¯­T¬ÎO\x0018\x0007\x001c`àqóÜú\x0001HI¥as=ÇHí#³»\x0016f9$}éw®×Áß\x000f®¼S¥É}o®øvÁRc	QÔV		\x0000\x001dÁOo\x0019ö4\x000bVÌÝfÚk\x001bË;+<nc\x001e\x0008u$\x001füx\x001aÂ>%½ð¾µgªiþ_Úm%\x0013&õùX AÉ\x0007Ö·¼q¨\x000f\x0015x¿TÕá³\x0016{9B­¿i q\x000cääç\x001dMa¾\x001caá\x000cg`9cj¨ÆêÌ¹¶¥tRñ\x0006¡>«­ßêÖk¹o%Jª³±ov\x00005"\[ÞFYr\x001dGgî?\x001eµb;ö;«h\x0010\x00014A[q$FÜ\x000f×\x0019\x001fE§hÞÚ|¬\x0013\x000c\x0013ýÆþ\x0016ÿ\x0000\x001fjÖ*ÞéõJfh¶\x0011»=1Å\x0004m\x000e\x0007¸Ç½XÂXî\x001a&C¹xãkÚË\x001c?½^G¿"º	>¥½:ÊëP»·µÓíâêv\x0011Å\x0014i¹Ý\x0001@õ¨µ»9lîåµºK{«whåEÚÊàà;\x001cÅvß\x0007n\x0016ÏÇ¾\x001d¸'hP$öRáIüû@Ú\x000b?%T\oºóxÿ\x0000i\x0011óúÊS×Ö4/1çPH\x00169P¨öâ­iÚ}Ö«©ZXéÐ½ÅÝÉHb\x000f.Ç\x0000/çYå¾bÀà\x000ek´øKªXh¿\x0011¼9«N°XÛÜG$²H@3É\x0003g\x001fÎmEØ ¤9­OO¸Óïnl¯¢x/-¤heñ¹\x001dI\x0004\x001fÇ5Nßå}§¦qzé¾%êVº¯üG¨ió	lîµ	æ@\x0008\x000eääg¥ríýñË\x0003I6ÕØKIhItÁçb1È\x001fË­\x000c\x0008HÏSÏåQÊríÎ@5hA4vÜ<2\x000bw,!C±c*\x000fB@#§­Q\x0016»:Iü7u§x\x0017Lñ+ÜÆaÔ.^\x0004·\x0003æ\x001bw\x0002Iÿ\x0000Ò°)/\x001b\x0010!3\x0001¸1À¯Døÿ\x0000bøkðûNQm^íûà\x001cÿ\x0000ãÆ¼ãO¹Þq,,C\x0001Ï|ÔVt*9+³zôã	¤`|«\x0003÷Æ?ÏzÑÓA\x001cc¡úV@c\x001dË\x0012s¼ç­wÿ\x0000
môëï\x0019hÖÚ´hö2ÝF¡È\x000c	Æ\x000f¶qÒnÄR±m\x0010[ÈàÖõ\x001bX\x0003vÎOë]÷í\x000bá};Ã>6µ:E´v¶÷Âo*>\x0015\1VÀì8_Ì×\x0011k¨ÈÚ,Zr¤K\x000cs¼åÕ~y\x001dWæ>.\x0000\x001e§ëQ\x0017sYE%{\x001a !r§§JO\x0008xëÁþ$³Ö¬bI \x000fû¹	Ã\x0006\x001bHÏn;Òê\x0019ÈÏ?jÁKIî+n^hÙüRGIã/\x0016ßxËÄ3jÚ"Ë TX×;cE\x0018
3øúPAÂ\x000cã¦}¿ÏJÅHÆ\x000f\x001cv­¨ÈÇ\x0000:f³PPV¯´çwgUðïXÒ4_\x001biþ IÚÆÏ3\x0001
o&P?wé\x001f¨\x001d«'Rñf©ªøÛP×feón$i\x0014¸F:*÷W\x0000õë5£IP,#¯\x0014y+\x0000Ä|\x0006õæ§Ù¦îjª´´&i\x001aC#ÊÛ$Þ¹+X÷js(<ôýkª\x0007\x000b)\x0018û½qV¾\x0012x2çÆ~9]:\x0010él1%ÔÃþYD\x000f'êz\x000fsíN~ì.D\x001f5MM'á·«x\x001bPñDfÞ\x001d:Ò7yìCN¨2å8è0G=O\x0015À:\x0008ÃM äª\ç-ëø\x000e~¸¯¤h?\x0017[XXAà\x000fìÆÝ\x0017í¦3¸+\x0017Ó¹õ8\x001eµóeëùò\x0006\x0014\x000f}\x0007ÿ\x0000_­cM½ÙÓ/y[ú±\x000c+ÏbÇ¿ç5aBî%'ßùSmPc¸=ñÖ®2àç1Ç<\x001aw¸$V~IÚ8éÈãõ©m¢f*\x0014\x0012ÝqlªI\x0007å?é]OÃ½rËÃ\x001e(²Õµ\x001d4jQÛnuÉ·\x000fº\x001eTúý{
zØ4¹ì\x001e\x000eÑ¬>\x0012x]|Uâh\x0012O\x0012^)M:Áøh²:·£c?Â>^§\x0014×¯õ/\x0012ëóßj\x0006K­BîA îfÎ\x0015\x0014\x000fÁ@\x001eÕ½­xïÆþ4P×\x001brI* \x0018í\x0010ÿ\x0000ê×ð'ä^¯ñ\x000fLÐþ\x0019kzî
·öÄjº=\x001bÕ¶âK\x0007òQëSx¶Í\U¬úÿ\x0000V9­[]\x001f\x000fô\x0015ðíÔÒ^xî
¥Ôn\x000bØÀFVÙ\x001bø>÷?ÝÇ\x0011ö!<-u¥N\x0011*å\x000eÖQèGjåo.e¸¸âåäi\x001d¤ä$³±$O¹¤y-åY ¢O\x000f\x001b\x0015oÌW©Ä:\x0011äã°P®¬¬u&ºlîÂÅ\x001cóÙPÈyc¸©"Il
Á%@ÛwM0VcÔàc'¯S\Ó^%Ö\x001bPOÞw¸·!\x001fêÃî·è}êx2Q£â;¸Û3åL¦v1ù¾ôá\x0006®]R\x001b\x001aMµPfUfeè\x0007l÷=*m\x000fG¾ñ\x0006©\x0016¥Û4÷7
ò¨Px\x0007,~è\x001dÏ¥sí<±HÑÊ²°\ÀëÈ¯IÒ>"h¾\x0010ð\x0014v¾\x000eY[Ä÷ñÿ\x0000§ßÏ\x001e<ö#Ï_lqÜóÀõd£î+²°¸DæÝGd¿\×tßÚKhº,±ßx²â0··Ê\x0006-Æ>âû ~'°¯\x0008Ô¥7W\x0012Ï+$\x0019Ý²å$O$Ô\x00177ÒI;I,¬ò9,ÌääROSÍVi\x0010w\x0011CúÖThª~óÕ³§\x0011^U_*Ò(r<\x0010É½ã\x0013/ÝÛuÏ4L4yÊ\ÀHç¿Óéÿ\x0000×¢Þ\x0015»\x000f\x001a2çp`GOpk*uXätg\x0019\x001cpzý*ç\x001bêU
>é\x0005ôvñÎ~Ï)3\x0012¸ÛéPBhQP2^ íøSe\x0007¨\x0003=øÁªÏó\x000223YM]Xí³¹iõ6xÊ\x0018¡Ûþà9ÿ\x0000\x000f¥f¹\x0004ðJyN9ýi\x0003µrJ67æor2jx¢SÛ\x0004æ¡?ZLV,¤Ë\x0005-Ô®f>ËUØäfJw\x000e´dÑÞ¦ÞiWtp»¯ª©4íq\x001dÍÍØ·÷\\x001fïw¬içó\x0014ÈÇ9<äúóüóV$o1BÔ~¿çùVmë\x0019GÓüÿ\x0000õÕ\x0008ØÂsrvDV*ndcÑ³èÎkzÒÖ#\x001ee8V\x0019À\x0015Ïè²\x0004¹>¯Ò¶÷\x001eTç ã®3Skê_2ë¹·[Á,\x0008\x0015]$à|§òþUÌd¸\x0017·<sÇô­$|Ås\x0017;<ÁÇ9_ÿ\x0000Y¨¼\x000bi\x0006«ã-2ÆöWÚêæ8duÆåVp¤ñ\x000f\x0019ª©h+ÒN¤¬[ðÌYÝA4AY¢$@Ç\x0003*C\x000få[\x0013µÅñoïµËdµ{­èñÈd	µ\x0002ýì\x000cÒ¬xÿ\x0000BO	øÏXÑ-ÞGÒ}±3ãyYr@\x00198aÓ\x001d+«Ä¹8b¾\x001e£ð¬ã\x0015/xÚu\x001d?tÁÔ\,Å#P«qþ4±Å	äåOõÿ\x0000
õ\x0017øE-ÇÂ\x0006ñÊj[§\x0013ìû\x0017³Îò²_?{<ôéï\\x000f-$9ÖÚA\x0007\x001e¦¥4Û±R*W3¥µ}Ê\x0006I?/=êÚØ¼zEÃ;í_65#ðcS<Ël!U9 w«W1øB'¸\x0003©G\x0018ãÒ\x0016'ùÑ+ §­íØç
îl/$\x0003^ãxÍ§Â¿ö]\x001at¼Ô\x001dß*þ\\x00059På\x0003$ÆGZö\x000f\x0016Q7ü
¢\x0011Í¦§[\x0015ïºF,Ùÿ\x0000¾«
¯c£\x000e·1>;¿­èjp:T\x0011è}?A^fWiõ8ú×¡üf¸ûgÄ-a\x0013$\x0000g² þ¤×\x001d\x0015¡pI;T~\x0015xxZ\x0008T¯Qð\x0007\x0019\x001dkON¡ÍG"U?.	Îr*¨HÓó\x000cð;?¯ù5<I|ÆB@;f¶Q$ÓÐèu-wV×&ç]¾¹½¹	åî¸rì\x0014\x001càg§ZNmÊO ús\ýã1V;±úWAb
§Ì{ôÿ\x0000=j\x0014RØÒSrÜÿ\x0000¯N+\x000eN[Á=zÖæ¤
\x000fn\x0001¬vP®N1ô?áZ#KQ`äùö­Æ\x000e8\x001càô­¯~\x001a\x001e)ñ®¦I\x0013Im$»®\x0014>Ò"^\ätã©\x001dëoâ­¦øÊþÇÃ0¼66ª°º´¦@f\ï ·8É\x0003¯U5ÝÁ¨Üã\x0015\x0004óïA e\x0002î)ÏqåC\x00106ã)Ø÷$Æp\x0017\x0000t«ÿ\x0000\x000bþ!êþ\x0005¿Ö#Ñá´ß*\x0007iÐ\x0019]Øa÷\x0007H\x0000c|\x001c¦¹í4\x0008õ	ælp±Sëø9G:%Ë-
­vækdkÌÊÆI¤cf'''êIúý+:ÒÆK¹.Gæ8éÅX¹MÄ6H\x001dqïEäöq\C\x0003·1ùRgrÿ\x0000\ïÈîW¼-cÏ'\x0019ÿ\x00009©åP\x000eG\x001fÖ¶ü	¢GâO\x0011Øéo{\x0005Nä5Äç\x0008\x0004L±Æ\x0000õ=kÓ> Ú|9ðÇn´}\x001d\x001fYñ\x0003®>Ü%È·n9È;à \x001fBj
Hñ$á÷\x0010\x0018~às÷OsÚyl >£h\x0003(7r}OJÑ\x0018ôùZ\x0019ÃÈ'¯Oþµzÿ\x0000í\x0013¨Yj:¶wcs\x000cæm26o-Ãcæb:¼*ñxØîèqLTÄ\x0012\x0006Ñ××5\x001c©ÙjW'æà\x0011èxüêU_³Ï\x0018\x0000qLÛ¹°OSëS"Ã*:Ý#\x0006Æm \x00009\x0019ëÖ ·ÊÊ\x0008ô=
J\x0003\x0013Áú
zÎ3õ­\x0011aDUA+\x0010#qÜ\x0007Ð\x001câ¬m¦\´\x0018cÔÆqçR$jNGQW``u?A[FM\x001có^æ4º\x000bû½§°3øqT¥Ðµ$ÎÇUí#ðù±]z&\x0010
öäÒ0`©«ö!ScKÕc_øôvÏR¤\x001fëÒ¨½¤\x0000ÿ\x0000Bº?ð\x0002qùW¡ÇsÛ\x0006ÛCp\x000eZ´\x0017*]\x000f1k\x001dC'u×ýúja±¿`BÙ\ëä·øW©\x0002ã¥N\x0002OãI¶Çí-ÐòOìQòWN½#Ú\x0006?Ò¥Ãú¼¤mÓnN\x0006èÊÿ\x0000:õ¬\x0011ïH\x0006\x000fËYû;îÁ×k¡åËá\x001dl2ÿ\x0000~E\x001fÖ´,¼\x0005©Ü6$Ò\x001fc!cÿ\x0000?Zô\\x0000	ã>Õ-¾ààcëG±HQ¯&ìÎ\x0012ßáðó
Üê8ÁÁ\x0011C~¤ÔÁ:=¸a ¹Çi$\x0000ã :ôo\x000exQ×µ\x0003\x0006jóJ>ô\x00160{±è+CÇzW¼\x001f \x0005Ôu)gÖ&oXþ[dÁ\x001b\x00123!Ç§¯nðÝ8½MU:³M£ÊK°µ}Î\x0008È\x001c|¹?É©T°P\x0001l\x000fzÉÕ|]¦£H¶-Á\x0000aÀÚûgùVQñÎ\x0016ÁH\x001d3/ÿ\x0000Z­TL½Þã\x0010®Ì\x001eüôúÖF¢Nì\x000eZÑ%×w\x0004\x001cv\x0007üö¬ËÂ\x001f8ÛÇP\x0007J/¡Q½q?ññ\x001eõæ¶]þë
ÀgµcY)Y¹ã®=«fávÄÁF\x0002\x0010WÜ\x001e(Ðu7\x0018\x0004¾Ý.U»ðxþµSJ¬u¸åQ\x0014G]§?Ò«ÜH\x0008<Àÿ\x0000õ­//ÍÔ×Ì\x0007Ë\x000c\x001bû»çéJ­¥\x001b\x001aPN2Lö?Ú=T|Gkè0êV6×QÝvÏþ:+Ç5\x0007ÚÀ\x001c\x00018¯aøäâóÂß\x000eõs÷®4sjç°xJgõf¯\x0015¾&hÇÌ\x000f§\Î÷K®­4Ï¥<%x?²N·\x001f£ì¯"ã=\x000f\x0007þ=ú×Îº3¬Dçw8>µmsr=¼sÈHÀ¼{V#¡#¡"¯Þ£=¥´Ìw6\x0018\x001féSF\x000e/SJÕ\x0014Ö\x0010ºÉ\x001dÛ0;U@÷®ú"\x0007ôÙÜk\x0018÷	\x0004]ÿ\x0000àF°a:~¨à|«°ò=k°ñ=¸¶ø'àVÿ\x0000«ýFoËÊOý³³±¤W-;®¨ÄðVuâ\x001dRÓH°KqtY\x0015w\x0018ÚK\x0012O@\x0002^½ã\x0006ÿ\x0000ÕÊÒâÔ ^\x001a@
ïòÌV\x0007ìÙiçüDÓØç1ÛÜH\x0001ë÷\x0002ìõìº\x0006¦ëß\x0012¾ øTWfÒ¦û=»+\x0010#dk·\x001dHU\x0003SXUÛHÞRomÏ¼Uyöß\x0017k\x0013±'Ì¼ý~r?\x001e\x0000ª±8\x0011±#¢ëTælÝ¼9r[=Oÿ\x0000^§?,2\x001cqÈÇJî¥ð¤yõ×¾È1÷G8,kMm±\x0010\x0003\x0004ã<t5\x0005"gXðNrFEo\x001bs
ÄjøË lt\x001eÆØS]Q`\\x0010ÄÓèm\x0017\x000cg¸ªB5ûJ0\x001b{\x001e+OOSN\x000ek4QWVR\x000e1Ðþf±F\x0004\x0007\x0000\x001e\x0008­ÝN<sÓ&±\x001b\x0001ð¹'8àÕ­Q\x0012ÑóðSÁ\x001f\x000cõï\x001bÜ\x0000/nÁ°ÓC\x000f¼sÜo\x0004ý#5äm#M3»±g~K\x0013rrN}ÎMV:ëé±iò^\Ic\x000bÝ¤c\x001a¹ÎæUè	É«\x0010®=qdÖ|6u\x0013VDl¤qÇ\x001di\x0019rI#\x0019ü*ÑL¡ëÇJ`qàd\x000fz³28×p`1¼çµsÖÅdÖ$Pp¨¡TwÅtÉ\x0019\x0011¿\x0000\x0016^§Ò¹­=³­\ÉÀæð\x001f\x001afê»xäÿ\x0000µQ\x0000à\x0016÷ïZ\x0017#hÉËg õ¬öËÇñ5Ïc¬±\x0007
N3Ç|RLÙ;qÎ=*{1µ\x0018\x0018^\x001aRÇ\x0000¾¹¡DnZ\x0010±.x\Þôí¥¸\x001d~¼\x001aTÆ\x000e
\x0000\x0012ÌHäéOa\x0004jX
2+¥Âz>\x0013ÄW\x0011Ç\x000e,ÿ\x0000gÈøcýä\|Ê0rÙìzÖÏÃo	ÛjqÜëþ'í|-¦×\x0012dæâNÐGêNFqë§ß\x0010üauã
Y%5µÓíÉ²²î[Ä8\x0000\x000e\x0003'\x001dè\x0005MîìµÙÇ®\x000b}p
L¨½éíTò9\x0019ã­L
\x0007|b·±Qê¿/^=jHÔç#z\x0002\x000cöÍM
|¹\x0000`ó´øïô\x0015x\x000eSùUxÂ¨ç
K\x0011ù\x0007\x001eµW3¹4`¶w\x001e\x0005,9=i\x0000\x0000î#WPT·\x001cÓDÀÆXuæAÈ=³ÈÅ Ë9ÀëÖ¥
ÁqßÒªä1\x00061½}GZ5\x001d9àõªóÜÛZ®n®a\x001fùèàgóë\ýï¬`wKX%¸Çñî\x0008§ó\x0019¦ää(9lu¤Ãm(]Ý:ú\x000eMq-ãèÌLFÂCÐ\x0019_ÇåÍsº¯uMC*Óù\x0011Ï8>Qø§ñ5>Ú(~ÆLô½CS°Óãúî(þyçsß#&áíZ_\x0012ëqé\x001e\x0015Ó®õ+é9Uâ4P\x000f,ÌOÊ£×Î¼lNK\x0013Ö­éösö6òâÒ}¥<È$(ÛOQØúV3­&¬©ÐZr>±ñ÷ÄÍ/ÀÚXÒ\x001cYO©Ä¸:>ì-¡úo)ù¤on3GzùÆ~/Õü_¨\x000b½bçÌÙ$\x001bcº:\x000e5Ï»n$}iµË
J/»³²uÛ$tBQÅ\x0002ÔÀúóÁ\x001agÂ§øc\x001cÚê@.Ì,n¦rÌ\x001c\x0003/\x001d@þ\x001cdz×Ì\x0002ÒÈ­"nÊçw¦@õãó5¬úýì?a\x0012ÿ\x0000£\x000fnÏcéYp\x0012®\x0000Ú@#\x0004:p§%~czµi»rjzWÆß\x000fXÛkz>½ YÁi¤k¶\x0011_E\x0015¼acP\x0002Èª\x0007Õ\x000f\x001dÉ®
æ=èp@%qÏÓ§ÿ\x0000ªºmCÆSê^\x000fÑ¼3ui\x0011]2y&·»Üwps\x0011\x001d1ú-sWå²9\x0005qÐ\x001f­kOE©ÍZÍÝ\x001cã±8\x0018=ñþs^ùàÑá=CàF¿\x0005âéÐëÖ£ÏYJn0¨~ñ\x0019\x0004`{Þ¼BîÜFòo\x0007L\x000cqHÎÍ¤ásòJG^ÿ\x0000
R3.E
Í
næ[«\x001bi|Æxãg@¥T'\x0004àvÏ_zÇó	\x001b'^Õ{OQ6y\x001eÒY\x0019$ÇR9Áþcòª0!ó\x000fNÖ´µfR3w\x0016(ðw ÊÆµ¦\x001b´¸ù9\x0001þ[éÓ®u\x0007\x0006Û	{ywmõÎÞiÙÿ\x0000@\x0018ÁÃ0é×\x0000UibetìË6Vûü+¯Oû³\x0008¬S«ê\x0017\x0016\x001auÕÜÒØXïkh\x0019²°ï`Ï´vÉ\x0019®³Ikuð\x0017ãyQn\x001eHLq±ùq;×\x0019k\x0017'9î=x\x0015Ë\x0014ÜäÙÙVIS»\x001eçû3J¶&Ôõ\x0007L¥Ò\x001eqÁ	\x0019ú\x0003]Oü¦¿Âo\x0017EÌZÍü÷W\x0001\x000cB,ê\x00150ØÆ\x0007#×"¸¯Mö\x001f\x0005xûP<4zjÄ=2Ë#AUþ\x0016øbo\x0012xkPÑíä\x0010ÉªßAhe#pDD29Ç|\x000cþ8®:¯m´b¥M'×_¸òu\x001bæ;G\x001d\x0007\x001fÏð­\x000bvÛ\x0000[üÅv\x0013¼\x0002Þ\x0004ñJéßj\x0017qË
\#íÚpÅ\x0018g\x0000åOç\þ¡oòGêNsïµèÑSG^-KÞ!Ñà\x0006õwp\x0000
{ý\x001aÖºq>§q"&B¯°\x001c\x0001ù\x000fÖªéÀ¤²0\x0018$à\x0003V-~k×=»UI
2²²\x0017Ë?i^9Ï\x0006´ôø¸r8ÉÆqþ}*« 3ÆS®qÍlivòÈb(ÚIª/ñ18\x0000~b³z\x001a%vu\x0003O¶Ó>\x0018êú¥í¼R^j®gæ.Z5_Y\x0017?@¹\x001dÇZòg\Ì[ø»\x000c+×~2\¥¥ÞáÛW
m¢Û-»û­;|ò¿âHüs^K.UÉ=\x0007 {jtWVN!­\x0010"Ã\x0019À8\x001eõ­\x001a`qòãëïYP¼q×\x000fJØ·\x0001È\x001ctª\x0010%1ª\x000e}Æ;ÓBeùáFK\x001eõddûÒH»PqË|ÇØvÿ\x0000\x001aW,©ÉYY\x0018Rsæ¬­e·ñ\x0005Ì\x00171¼Rª©(ã\x0004\x000228÷È5ØÛ8·Í\x0008\Æ7(À °Á\x0019\x0007·|w®BÖI'ñ
ãÎí$\x001dò;\x001cbyÉ¥-WO©¡xI<ôÇ§j£ú^©x¤c\x0000}sYÛp@\d\x0008ÿ\x0000?bÞº\x0017-ÆcãÇ\x001cT\x0013ç.OAÐw®·Mðü¾
»ñ
ÃÃk§DDp¼ä»8Û\x0018ÇÌF\x000eON\x000f¡Ç+:üç\x001fvîÆâÒ+¢®3ÉÇz¿¢Ce6±g\x0016±rösÊ\x0004óÇ\x0019v>¤:ß|UU^\x0006>P1È¦\x000bêqÆqN×%;\x001d¯Ä\x001f\x0017.¿-¦¢Âl<5¦\x001d êzæWõvëíRIäÖ?<zb£H8#\x001csVÒ.\x0001\x0018ªR	MÈ®A-ÐÔÿ\x0000O\x0012çosè
\x0002?\x000ct«vñr§\x0000\x001eçÖ´Jæ
B\x0008É_Ï½K\x001ae°z\x000fJ¼°a\x000b9Àõc?\x001aÂÕµí>ÃtpK\x001cÓu;\x001b*§Ü¿AW¢FMêjªüÝ±ïÍ+ìNd*þû\x0005¯7½ñ\x001e£p\\x000b¹\x0011\x000fðÄ6\x000fÓÈWËÊí#¬Ç$þu\x001eÒÅZç¬Ë¨ZDHêÝ\x0000ç\x0014Vuï´v*²Ëqÿ\x0000,Wú¶\x0005yiTdñRê\x0002ÖÝøÒrÄY[G\x0018ÉÃÉóvã§ó¨l®<Kâ½F=;M[ËË¾U·µB2>Æ=I®Çá¿ÁÍKÄ#[ñ\x0004é x^0$úï
dOúf\x000f_÷\x001eé]>¿ñ[Bð66ðO\x0016áËráwOp}W#õ \x0001\x0015ª·¢6\x000e¬ñ\x001dJÔ4-^ëMÖmä¶¿·mÅ&7)Æ}û\x0010sY½êÖ¡{q¨^Mw{<\x0017S1y%3±êI=MVE.À($\x0007z~¤;_@«N¬^Çg¥YÜÞÝÉ÷!·¤vú\x0005\x0004×ªxOàÌãM]{â&£\x001f|>0GÚ?ãêqèõ\x0007ê	ôSWõúoôé´_zBhö¬6KªÜ({Ë|íï×8Ï\x0001joØ¥\x000e¬ñk«y¬îæ¶»H.!s\x001cH¥Y\x0018\x001c\x0010Aä\x0010A\x0018­\x0017ÛÙ[ÞY&\x0008\x001bOµy\x0000bÛ¤h»sêI8éX÷w\x0013]ÜËqs+Í<¬^I$bÌìNI$òI§ê2\x0019&\x0019pø\x0017#Ù@Å>£M(´T¥\x0014
îôï\x0005[iv0ê¾=ºJ²\x0004Ú|@\x001bûÕ'x\x000f?¼î¦BW9ß\x000cøoUñ. lôkFDS$¯±Ã\x0018êò9ùQG÷\x0002ºá§|6Ñóe­j^ Öoãÿ\x0000[s¢c´ÏuC*p\x000e~|\x0000{\x000crq¼OãKNÃû\x001fIµEðâ6õÓm	Ã·gÏÍ3ôå¸\x0018ùB×"in=\x0011Ó\@«3RcbqÓÓùSP¨!³\x0013WöXH\x0017rIÉ\x001e×ó®ãÃ\x0008|I¯èrj\x0010D-d\x0005íÄ¯µ¤õÀ=»sEtÖ©
jòf4©N¦Ç!¦É§ÙiòK$l/mã½Ô\x0016Â³:2±8åZ2\x000f¸¯¡<=à/\x000føÃàLÓéÚ|'_$\\x0001ûÓ:eçû¥p\x0000éÈ=kÇµ\x000b	%øz±ÝFÑßh\x001a¬#\x000c2Cp¥×9ô'\x001fW®àïÅsàHn ¼´òÊè(\x00041È:0Ïb\x000e\x000fÐzb¹îæ®Ö½ägê)å88;H\x0004qéÅG\x001a\x0007ÒîÑG*Qóß©^¾Ö®çRº¼\x0018\x0010ÒK7?X´{\x000fä+;KÈuîñ7O¦¥tFéjqÕZé°h\x0000ù²¯\x001f¼B\x000e{ê´»o\x000c¯ÃÝV{¹\xL«m\x0018È\x0002<®p1}üý\x0005wß\x0005¼\x0011¦ë\x001e\x0016ñ£u\x0014s\C§46èÈ\x0008FVo1}\x0018\x0014\x0018Åy4©ûò@ù%\x001bÀÿ\x0000ysüêa%Qrö5Ò¿kß¹^k»§
<J\x0012ÏÏûFÍ!öíÎ~©\x000e\x0017JB¼ì\x000f\x001dð*6fPy]ÜqÓÚ§\x0007O3òùñÇD­ÒÒÇ-I¹4Ù\x0015»n¹e\x001b]p3é*ö¥¥Æy 'Ï¹\x001fç<ÖVJJ\x001b8Æ\x000f=zhÁ¨Ke-À¤ \x0006\x0004pyÍg4ÚÐÚ£\x0019ûû\x001dï¯e°ø=­\x0018¶í]Q,ÝdùknY±ï9÷¯Týl\x0003Cg0\x001f,mwqå"_Ówë^/~ÆÓáGá$nT¾½ö¬Q~´¿
þ#ë\x001e\x0004»m7É9cò\x0013î*\x0006íÀ®:\x001cç?ZóêÑH]os½V_'è_\x0015Bx³ãàÒw7×\x0016ö,TàQÇæõÂxª\x000bH5Ëû[
æÎ\x001b\x001dÇqÚ\x001b\x001d{ô5µðþmOâUÿ\x0000597ÉeiwªÊÝ\x0006â\x0008þr\x001e=«7²É:´ªÁä;Û=äû÷5®\x0016ñ|¯¡'Ù¦ÖTvûÄûÔú~\x001aè\x0010GÍÇy_å|\x000c\x001c\x001cõG5Äg¯Í]r8a©¿$`^Æ¹äó]o5;m\x000fÄVZí»\ÃjæA\x0012\x000b8S°äö
øW/*\x0003z\x00186*üñe\x0008\x0008Á\x0000ñYµsdìîVñ\x0014òß\Ïsq',îÒÊÝrÌIcù\½Èo0¦\x0006{zq]>«±W(\x000e\x0000Ï<ó\Ä\x0019YÏQ>µ¤\x0015Wv(ï´\x0003ó­1z\x000fÖ²#ÀéÑr~¼ÖÔ\x0003j(<1\x0000ñI\x000eÅ¨\x00143|ÃäPY¾¯ø~4×ýáÞÝs
a \x0000\x00119?îþ¿ò¦d\x0013Â´-;ÚÚMtdKt,B=Tuf=õ?Î¨xGÂ_n»×õ9o£IÓ×oÚ6Ù¤ê\x0015C`þÀïZze¥Æ¥}\x001däùar@õù½2~?õkk[Ë_\x0007è?K\x001bîd\x001fòñpy%¾?û¢°«'ð£®!nyô9Ñï2~µ¿ðãMðõÝõÕ÷u\x0004·ÓlQekU?¾½'81ÔõÁ\x001d2HÃ¼ùÇ²ÕDä0ã\x001dirè\x001cÖw;o\x0018ø¶çÅWë4%¥²ùvvQàGm\x001f í\x0006Oò\x0015¬xbÿ\x0000KÑlu=GÉ·[çÅµ¼#Æ|Ðá21rr01ÍXðÎ§\x000e©ÛßM§Ûê\x0002\x000c°·¹È\x001f)`:àóøüj¿¬Þë½Æ¡«\½ÅÜä\x0019\x001doE\x001d\x0000\x001d\x0000\x001c\x000f­LU¤¤nÌµSñMe=\x0006síVã,\x0006W¡îNj\x001bH"i%eDNäô­v9Ûº\x001doÎW\x0019Ïj÷X±ÓÆÙ&ß(àÇ\x0010Ü\x001eÃùÖ\x0016­xöû­H­\x001b43ÿ\x0000­¯\x0000|=Ä\x0016\x0017Zî½|º'¬óçê2¦ã#ö$þ7?§×\x0000Ëè\x001cZXÄºñLìçìG\x0012¿Ì~¾Æª\x0011êÅ\x000bÆ_@¨ *É¸\x0011¬Ò\x0008 Çi`\x0001#<d\x000cãó5\x0010§ve×RýÕÝÅûÿ\x0000¤ÝK)Îs#?úÕb}\x000eí.ÒÚ$ûLï÷\x0005¹ó7ý6õÿ\x0000ëWwðïàî³â[?íbht\x000f\x000cÆ7É¨ß|Õ\x0014ãwÔà{ö®³Pøáo¶é
4á=ñ\x001b&×¯|ï\x001aÓð\x0003ºzÖrnú\x001d09_2Ôðw·\x0019«\x0002ASÔ\x001eõ\x001eÃW®õ\x0019¯¯¦»¼¥¸FW~K3\x001c~¤Õ«Anü61Û?ÏôÜ#B5>\x0016býk²ø_â=\x000bÂÚìt\x0001­ùq\x001f²ÂòmD `A\x000c;sÓ9ÇJÈL\x0006C°R~^#©ç<t¬ë»GA\x0003Üt¦¦¥¡2£:zØì>"üKñ\x000fo|Í^è¥ª\x001cÃe\x000fË\x000c^^çý£Íq\x000eY³SÃ/\x000b#[ÆûC09\x001dG\x0015[¥4"rmn \x0015ß|3øoà8o®­|;a¯9\x001fdÔ.Ø°´\x0018ÁÛ\x001e:ýìÛ¥p=ø«\x0010ÚI.\x0008\x001bWÔÓmu&\x0011¢O\x0016x«Zñf¦÷þ Ôg½¹làÈxAèª8Qì\x0000\x0015ÙÐ|=¨k¤Z~o-ÍÌu"BÄþ\x0015ìéðëÁ\x000e­RóâUû^j[CÇ¢YÉ\x001bÓÌ`~QøbzTó¥¢6XyËYhx7Ù§û1¸òdò\x0003l2m;wuÆzgÚµ</áSÄ×o¤Û\x0011'q<®#Þ1ÕäÔQÏ$û\x000cõ={â\x0006âí\x0013ËÖî-ô_	ØËO
é\x0011´\8\x001c\x0012ämEç>øBkÎüQãKÍbÍ4»\x0018!Ò<=\x000bK³È7\x0003|ÒÉ>w$õÆ\x0007\x0014ÓlÎP^æÈÕô\x000f\x0003á<0!ÖüB-¬ÜÃ{f\x001fóí\x000b\x000fÒY\x0007lªµÂêW×Zì×Ì×Ws1y&Ë»·©'j¾ryëM¦fØQE1\x001e¤Z\x0018®£ÇÊq\x000cþ5÷¯ì£±ðÖj\x0015bµ0\x0007L(¯ôYá7¶÷\x001dc\x000cÜc\x001d2+ík/\x0017èï E¨­äBÔD\x001cÀc\x000b}{b±Æ4¤½8óR÷;;êö-«üFñÆ\x0002þë]â\x000b|\x001fíp¿	?ð(ØÀ«Ìï|+=§í¼AçG5÷mn#\x001b¨=OL\x001cVÄ¾&ÇÆqë\x0005ù\x0017«v¨O9Y7ãñ\¯ã]å\x001a\x000fÅ\x001f	[\x0010ëaqý±§\x0001yL7¨\x0019ÿ\x0000`'ýõV¹¨¥m´¹+s_txµ¤d\\x0017QÊ~÷B\x0008ä~DÔþ\x001aðýÖ£®YYÛ(i&B¹8\±Ú2àB­ØªÈ¹#Ãü»¦êRÙê\x0010J®WÉpÃo\x001c©ãõ\x0015Ù;¥sÏM¨3µøi§êÞ\x0010ø«\x000f5+9äÖæ\x0004r\x000b$tn õå­hÁm\x000f3åÇ*HþUï\x0015\x001a;?Þ\x0011×b8ý¬îC\x001f÷¼³ÿ\x0000°¯1×,\x001e\x001f\x0010k\x00160 2E$j:ur\x0007ëÎ±¡e&tbStâq
¥É¹@\x001bxÇ_þµ2;Há·¸S.â²\x0012vôû¿á]§Äm\x0002óÃ:íæ}åùñ*8òßrá#\x001c\x0003ê:W\x0007\x0003 ¾nÆDü2\x001cWl,ÕÏ:¢iò\x000c\x0005°@'å\x001d½ªÅÝ«1R9b\x0007\x0000c·Z½b±]Ã8QÇ~zúàB±\x0014p;TXwJ×.øµ\x001e/\x0005x"Û\x001c	.\x000e3ÖIå?È/å\I\x00079É\x0004\x000eµÖx«VµÕ¢Ðb³ghm4øm\x0018²àïU%ñê2Ýk\x0012ÞÐÍ!8\x0004øúø¬ã\x000eX¤oV§4ô;¯\x00047öoÂï\x001ej¬v´éo¥ÂqÎ]·8üü«²ØÅ4ÿ\x00004÷D´{!\x0014c?ãð¯AÕ4æá\x001f4Jõ­^{?¼\x0017÷J~?*óo³î%
æA\x001cEU¹Áç¨ô\x001dë\x001a1¼ó:ñ/	5Ð¾Ô@ËÙÅZÒÈö7\x0007+¸\x00023Þ¤ÅæD\x0000c\x0019\x0007#©õ§%UÝ !O\x0003\x001eõ»W<ø»\x001d\x0005ÃùzÌÙ\x0007¯ÓÖï7'#oQÚ¹gmA¼ß¾pI\x0007òúVÞÎÏ±óÇ=q\x001b§ jÙ\x0011¯_¿zçfÁ\x000büæ·õI\x000eIÇ\x001d<zV ,Y¾æ}+H­\x000cj07?BqÉ­uf* æFÀ\x001cð	¬­åT ã×Ú¶¬\x0007\x0004eFÄ9êÇ¿à3ù\x001a\x0014X\ËX!;GÊ¹þèàgùþ5\x0013IÇ#'\x00199¤Uà¿óæ·ü\x001f£Å¨ê\x0012Ï¨º]ù÷r7M£¢gÔÿ\x0000 k9ÊÊìè¥\x00079(£gE?ðxeõIpºÆ¦;5=bÉÙàÿ\x0000ß>¦¼M\ksc¸®I=zò~µÝëÚ¼ºÖ¯s}?Ê\x0019vC\x0016q±\x0007AÔû×	g¬Ü®qòäÏùTB\x00164«RóPÈÕºbàw·øÕdRÍ}8íSJ7g?wùÓâNç¿8<TØ«¤Îm<·TUÎì\x0019=y'¯åÅU(\x000e[©íÏZ°äÈà~\x001fäW-¨ë,ÌñÚJ!N\x000b\x0003n¼éKa¶Ùµ}{o§C¾á¹þ\x0014þ&ú{{×;gâ\x0018Eä·:ºe\x001f¸·Ë\x0019õ#\x001cÖS}grîÝÏ<þ5«àû½\x0002ËÄ6^$²ÿ\x0000M.öÐ¸C+\x0001ò«\x0013ü$ã=ñY¹s"à¥	&;\x0008øa5]4øÃâ\x001dËéþ\x0012±\x0014KÄ·î:E\x0002úqÝ¹çWøãûÏ\x0018]A\x0004PÇ§h6CË°Ó ?º:\x000f÷÷nþÕWâ\x0017µ\x001f\x001bjës~É
¬+åZYÂ6Ãk\x0018è½\x0000À\x001cõ8®OnA>£\x0014µg'½üÆ÷®ûá_ü/áI¯µ\x001f\x0010xuµ½M\x0002ÿ\x0000g¤®\x0005¼mÎYÔõ=1Áú\x0003\
.9â¬çNÌì¾!|Gñ\x001f/|Ýrôt$Åi\x0016R\x0018¿Ý__sï\mtOàÍ~?
\x0011Í§K\x0016¹Un$!78\x0005Aå¸\x0015ÎRVèTù¾ÐSO\x0004m9W ÿ\x0000*d«ô/Zj/\x000br\x0003\x000e{~µ¤6÷0\x0005m¡ã9à~uÏ²\x0015<E%O\x0007\x0018¬åM=be\x001d%©«$hAÎN\x000eÐ	Ç\x001cöªSÄS ç½L%ó\x001069\x0007JvýËp9\x0019=)+£I(M\x0014\x0010|Ø¯eðÂ«Ë&-wÇºxgÃ\x000c¯p1<ãÒ8úóØà\x001aò\x0007À\x001b\x001f©­\x001dsÄÆ»*K­jwòF\x0011®%22@MT1)û-Ï\Öþ+é¾\x001aÓåÑ¾\x0016i¤[8Ù6§(Ýyqï»ø{÷ã¶Úñ}JöâúæIî¦y¦;»\x0016f'¹'jº1n	¡ïºcaÔ¬æ¬´DT¦\x0014»\x0005QN\x0000­\x000eQ(é^á¿¾+ÕíEýý´:\x000e0ZûX[ \x001eÁ¾cíÆ=é¾4Ðü\x0005¡hmm¤xP×|E¹}\x0004\x0002+$\x0019ùÝó1ÇB\x000e\x000féJèÑSm\ó)Ì¥@È###=Å6ÛxzåL \x0013\x0004NÆ¶d¹2~r\x0007qÛ>µKHð¾©iá\x001b_\x0010J\x001d2òáí¢ts,2C¨û¹\x0000ê\x0007Ò3ï\x0000|Ãó®È8Í\Â§=-\x0013±\x001e«/Úa.£÷Ã\x000fZö/>"·¶ñoµmBX¢´Öti4K·ð¾u³l\x001b8å\x0004=½^+p&×éxm[\x0001µ#\x0004ÆW!Çãòô­\x000b-BÚ÷ÁSi¸aq\x000e¢öß.@
\x0019u'·\x000b\x0013\x000f]¦¦­?h¡7FüÛ4kë6ÑXë÷öq:Í\x0014RÈÈ!3\x0005#\x001dx\x0002²®Ù¼ØX6@oñþF­³Fñ[ÝJ\x0018¬dÇ ^:ùÖ%Üí\x0011YW¬C\x000fn£ú×J·+9%RòçÚøÏÇrëÞ\x001cð\SZ,o¦Dñý¤>ZL\x0018È\x001bqòà îzV§Ä\x0006\x0016ÿ\x0000\x0011<Cå`\x0019÷\'»\x0014\x0012/ê+º.|!#Çôk7w
Ý?ô/Ò»\x000f7YÖtmTt¹°³¿\x0018T\x001fäÕ¢¡Q%ÔêXRoì³£ý¤îGü'v.X^évóuõ2\x000e?!^-§ k\x001dAPùdßøñÿ\x0000\x001a¿â[ËÉµ\x001bQ}s=Ç©\x000co4¬ûcRB¨É8\x0000\x001e\x0007OJ§£\x0002zDü¦,\x0011ô+jPä\¬ÆµU?z=Y±S00*MN@À.N\x000cC§Ó­:hxb\x0008ùA#ó\x001fýz¯yûÕÇ\x0003ÊoÐPãm\x000cSæ³-Ýê7½âßj3\x0019®¤f\x000f&ÅRv"(ÈP\x0006p tÉïÖA\x001cÈd,bV\x0005°sòç5F\x0005"\x0008N\x0007ßãþù­\x000eX\x001dWÄ:N\x0017þ?.â·#Ø¸\x0007ô&³©¢gE5ÍQ\x001d¯Å\x000bÉ4mOÃ:m\x0005IÒb@YAÚò«\x00168=\x000e\x0008÷\x0004ÑáÏ2Þø\x0007Yñ,·	o
*F¬¤c+ñ÷ïÉ¬?¼wß\x0013õË½«,1ÞùH°
GÀú|µôwÂ{­?[ð\x0015µ¦£c\x001aid_k»óhåv,ËÜ\x0001ó\x001cÿ\x0000³\1æUN£äÓéÐùBé^;díÎ9§D/ÍÆ	Î;vÅZñ\x0004]kwZD°[É+¼q\x000fàRÇjþ\x0000øTðl `\x0012À\x0003þ\x001aên7<ê±Qf[`5\x000bS(!\x0018\x000c°\x001cíøVÔ­ÍÔóG\x0019,ùq®: ÿ\x0000?­E5¶ÛËrÍÁ8úUäd3Ô\x000f\x001e½M\x0016/NTcjch\x001cdu$þ2
sÛ õ®Yt\x0014\x001c¥`ê\x001fëJp£\x001bAÅi\x001d*^ö \x0019Ü\x0010y?çð®©_.ÙFD+îçü¸\x001fgiàBrÊ	C\x001e¯Ô~]\x0001ëZVËvaÉ#­)+\x000e:²(mä¹(-É+°8ÇRÄñ]O\x001e=+LÃvR\x0006\x00115ô«ÿ\x0000-f \x001d¿AÇéSxz%Ð´×eAöÉ·C§£\x000fûê\z\x0001Ðÿ\x0000sR©fgv,Xfn§?ÔÖ\x001f\x001c¯Ñ\x001d·ö0·VW@píÇÝÀÇô®RÀÄæpp\x0007ÓìàBÌÙ\x0003<\x001aå¬þ&÷
½9ëÎxô­\x001eÌæKÞEÌ\x0016|\x000cõÆ@éWíâ\x000c\x000fÓ·5P´q7ïd :/ó5auí\x0016Ò/ßj0\x0016þì`Éûä\x0011úÖ7:\x001b0üsxö\x0016±ÚDÀ=À%\x001eB0>§ùW\x00089R\x000fsÔ×WâýKFÕR9!çí1©
Â\x001f»NX~cÖ³¼!áÛ¯\x0011ê/\x0005¼ÛÚ@{»ÉÉXma\x001fyÜút\x0000u$95\x0012`µf/íÊ¯à(U+»~\rzWQâýoI¹{}?ÃÖ	\x000eb¬ÜÈ\Ý±Æéeaë:(àsy¶\x0013¿j«`\x0000\x0002ñÿ\x0000ë©W)¨®¤\x001bNqÅ\x001bO\x0015#HK\x0012\x000e3L$\x001e­Í\x0004è
§5ì>\x0003áï¼-mâ\x0012Ü'¼A6æ¶Ðââ8\x0008$\x00036F;\x0003Ï\x001cð\x001b¨ñâqÒØ\x0014¤¹u:¿^=Ö¼s©\x000b^p N ´+\x000c\x0003ÑWúäiIÉ¤¦¢¢¬ØQJO\x001cSiJ\x0015>¢¤q\x001c !»PI¥bº\x0013Ú¸Î@$ý)®ß9éÍC3E§¥3Ô\x001ai\x001e´Ú2iÝÅ&u¤¥\x001dh\x0011«¦h\x001a¶«a{§i×WV
\x001eêh£,°©Î\x000b\x0011Ó¡ümø\x000bÇzÞòm\x001a×N7\x0001BÝÜ[,³[íÏú¦<.sÏ\x00078\x001eÒ|\x0002øÿ\x0000\x0008\x00175\x0003æh:!¾®à\x00078\x000fUÉÈî	\x001e[ãß´_\x000eøÙÏ/í.ô«øÜ+o(@\x0018 ôã#Øëfl£hó­Ê§¯<U|\x001fU³þÐ¹þýÝÔ¯ Ü\x0000\x001eÀ\x0001\æ°Ö­-`¶qÚ"ÇùZÞ\x0011ð6©¯X¶¡msoih§iG ûð?\x001e¸¦øÃºNi&5¨®¯\x0007\x0001#Æ\x000fåç\ÜÔãS=~g¨j9§\x0015êì¾ã9<W©ÿ\x0000Â>ú-ÛÃ}§+\x0002]Ä%k\æ\x0017?4@prr
`R\x001e¼Q]ÝÏª¬´û}BÇÇ\x001e\x0018ÓÀ6z´~+Ð¸\x001cÅ\x0014zÿ\x0000\x0007ü\x0004×¸;Y0,7c©\x0015é~\x0015×Çnü/\x001e§0MgÃº[0E%ntÉÆòêý
©.G³tª\x0018´WÓ<gªÂ»JC/\x0018P\x0006è_æC9ãåÿ\x0000ÕÐ¼dâËÆ(Î
¢gß!}Ì3¹N\x001b\x001d­.Z\x000bäu#pz0ë±r²I+J \x00121¸\x001e2;fkdê©u\x001ce­ËíWê3èk¶ö<í\Z;M>ÆÞñ¦æX-¦X©l¸\x001b\x0000;ErwÂÏ\x0010\x0007%wcÜröaøWC¥\y\x0010ec\x0011ÝQÜ?ÌÕO\x0012Û¥½Ü7qüðHÄôíéøkx«£¤3Àà^ÿ\x0000ihî7}²Ù0yýäy#\x001fQÊ·|H/|++dÓ\x0004gÜÇ<ú\x0007Zä4t=fÞú ]¬n\x0016AÇÞPy\x001fB¿Î»b\x0019\x0005ÍÆ\x001c=µ\}Z9HN}\x0008ÛþM'\x001ek>Æª¢{3Ô#3¥¶K3\x0018\x0001'ÊÜ~j$ ÕoÍäH}¸ ç?_9<òIYÔ¬ñ\x001e¤0\x001cà}\x0007þ;Rèöê·vÑB¾eÍÄ\x000f\x001a\x0001³4l\x0000Ï×\x001f?6Lv²!Õ¢?cD\x0019Þ¼}3Óõ¬8òÖ2\x0006þ\x0007e\x001fB+Ðuï\x000e_hþv«F"¿³l2«\x0006\x00000
Á\x001dxa\\x0016ÍöÁm(\x0001$WP@êÄ\x0012\x000esÏ57RjÀ¢à{¢¸P,mñÁùÏCÝ¿úß¥w_\x0008!QãKéÆbÒíî5\x0007Ïý3ãõa\g-åÎ§.EÅÌñ['\x0019\x0001B¹>¼Åz5¶\x0017t¯kpf[D:\x001cS\x0015Ú]b¬p:\x001c%rbd»ÔïÁAÊ\ý\x0011åª³j\x001a\x0016yî\x001b~OvvÏójô}CZ½Óíol,ï."°1Ë\x0012>\x0016E@\x0011r?\x000cþ5Íø"ÁN¨·l¸Tì\x0007ûÊ­'éüêÞ¢¥ÑdíÀ÷ÍtÆTµ9gR^Ù[ÔËÏÊ[v<ãÍÙØ'ðé¿CWP\x0008\x0001ÇJ¬¥äÉ;»¸N¤äà\x000c\x0001lTI\x0001\x001d3×\x001fçÚ²JÈÖrRÑ×ßB\x001eúÌ\x0010\x0007v>Àf£*YòùÅZ¹\x0019{i\x000e\x000b\x001c/\x001fNh¸\\x0015\x001cd\x000eÞ¿ç\x0014\x0005"¯NCgö	fs?\x0000
þÞÝ}«1îøÁf=\x000fjé5[$u¬\x00191oi$­òùbp1üGÓÛñªÐU¥ÌîöuÂ©ýÌC\x000bþÑî\x001c~X®Âº_ö½úÇ)\x0011ÚFmÄø#\x001d\x0013Ðõ«U±a\x0010¹W\x0001!\x0006BÍè1Çµt7×BÐãð®í\x001e±yµõ\x0019\x0000\x0003ÊR2"\x0007=@ãñ=ÍcViû«vtaéÛßÈÅÞ9ÒdÔ3\x0013\x001c\x0003ÈÞ\x0004Ý±\x00173À\x0004÷çÛµp÷Þ<vb¶6(«Ùçbäþ\x0003\x0003ù×-q\x0010VýÑÜ\x0007Ê¸\x0015íÿ\x0000\x0006<\x0001a§hÓxûÇ« Ø¯o\x0004	¹\x001c\x000c\x0003Õs\x0007B}Î3§¡´`ë¾fpþ'½Öt}\x001aÂ{Ôµ¾½\x0006O²Ç\x0002\x001c}'$\x001fñö®\x000e]BîgfæVfëó\x001ekgÇÞ Å\x001e*Ô5YbX\x0004ò\x0013\x001c	÷bOáQì\x0007õ®up\x0018\x0016\x0019\x0000ò3Ô'&µ
ª*VÐOsÍ\x0000â\x0006==«°øqð÷Zñî°,4x\x000by\x0001òáSÝn\x0003©íì^Ä(¹lcøWÃ÷$Õ>ÉdcQ\x000c×\x001736Øm¡_½,ü*?R@\x0019$
Øño,×N_
ø[Ì@ÃË;®Ùu\x0019\x001et²v'!AîÄ½ñ\x0002úÛCK\x0006xjhäÒ­å\x0006öö&\x0005µ9×øØùf¤	\x0003É'5àÏ\x0002xÆ-\x000ft©ï6rò\x000c$iþó¶\x0014\x001flæ§Í8µ¢9lTöv\x0017×Q[YÃ$÷2°HâK3±è\x0000\x001c_Hü=øAeáÄöú×Âù±é
 6¶)ÿ\x0000=®äåp1÷yÏ`Ý¹ß\x0011øï@ð\x001dÎ¡\x001fÃèl®|Gxî×zìp\x0004ßqæ+8ú*\x000e¹Èþ÷\x0004.{»"½äÏ\x001fñG5_\x000bê­¦ëÖgz¨²4,ÊÄ+\x000c®v\x0001ÇnµVoîç¾»êòi'¹É,YRIä­Vb÷Ð)*Àh\x001020pNç
§cP\x001a\x0004%\x0014S¶àdÿ\x0000õè\x0001´ ã§Z\x0000ÉÀäÑ@\x0007ZJ( \x0005¥\x0000úu£\x0015bÚ=çÃÞv.\x0010rv+#­'Jµy\x0019S:qôªárzfî\x0013¬74â=©\x00052\x0000Rç4Ú(\x0002qq(Ê\x0012?íÜq¥DI=M%\x0014¬7&÷\x0012(¦#ê\x000f\x001aøn\x001bÍB\x001b8%póhÒ©\x0001	't¶9þé'Ì@½ê·Ö]gÀ\x001e\x0016ñ\x001e\x001bíA´\x001bòË·
\x001fÍ\x0019#éç»U¿\x0007Ë\x0017¼\x00196s&éìÊ}Bp@\x0019ò_>ÜÂO§é]\x0017ìÏ´\x000f\x0015há5»«o6XöàËu\x000fú»ô-\x0001ÝAèÕÓ'tT\x001cKá§\Y¬4öê7\x000e$\x001c`z\x001f§\x001f¥w×Zm¥ýÎ²qÃ\x0005¾­a\x0016½c\x0000Âª¹\x0018%ì0êã\x0003ÐW\x0017\x0003iÕ\x0019ùXzÚºIí\x0005÷ÐGúUá1·L[\õ\x001fÉøyT^ÒÒA±rCf12É\x0019Ê±È\x0007¸ô?\x0015bÜÇ}\x0001°sHi\x0017Ïºà}A©e6ÖÑÞË\x0016»[f\x0011+Göyx\x000b/Ë×\x001d6\x0003U¼1\x0003Kq\x0015©åÖU3¸<Èçð5×	ò«t¨ûFê1´É­¼£q\x0013FÒ!s\x000e	\x001cñ5Ô+	,|=©©\x0005ÌFÎlKBÛFí'å]?Å\x000bx×CY­k¬á\x001eÿ\x0000Ö¿s>\x0016Q{¥jºbÊ%å¨\x0007å\x000eGâ\x0017\x001f\QB§µ×SLv\x001da¦£{x«Âúoíu²²ÚÍ3\x0008¦\x0004rQ\x0018ê:6=y¤ð\x001d·â}\x001f*_(Ï\x001cpF?\x0002+Ó<\x0013â»\x000bë7Añ:Ø\x000e\x0006k´{ò\x001aB\x000e\x0015³Æ2Iéè+Öõ=%<i{¨èG\x001ekªC²8×jí\x000c¼Ø\x001c7n¬o97\x0006ÔiÅF¤^Æe\x0007âf®\x000e9d\x0007§C\x0002yöáþÆÿ\x0000òÑg
\x0008\x001d«¹ñF³ñ\x0013]»µ´\x000bæ\x0012p\x0019j\x0008Ù\x000e\x0003pHôÏ¯5È\x0004\x0004/t;í"´Ã§\x0014|[qe¿ö]üOðÛ±\x0002\x000b{¿¶³\x0013©\x0010BñÊæêWøOjÌÛn|C®\ßËÎITLèMIà|Ú&»¨3gá«¦CÜI.Ø«Ç[]RÛÂe½³Å\x001elmØ\x0016\x0007Ìv³¸ÇcÇù5ËV\x000e¥{ôGm	Æ\x0016ÏvvºdúD~	µ×N
[N¶u»wÉ;ÌÊ\x0017ä°\x000b×ã­a\x0008S.\x001b¨$ÿ\x0000Î¶~Î°øHÉÈ7W ã¹XÓ ~oOñÆ\x001bÖaÓVå¦¸6ÑKq¹@	#\x001eÀW\Úå8`§Yºò9F¶ù¥\x0000z\x000fñ¨¡ý""AÀ9¯ZÑ¼\x001fg\x001fÃ
WÄ²Å<Ë´Q7Ì\x0007C×'=+NËPk{ÈdX\x001b÷H¤2ã\x0007\x0004zôüë\x0008TRv7©IÂ<ÆýÚF³Z¢\x0015\x0006O×\x0019?ÒKbYORFN*î§Gu
åíô\x001d¥\x001bÜ¦7<®q\x0014c9êÙ'Ð)éT¼Ui©iÞ\x0002W\x0017Kg;f¹þàcÎ;ä\x0017#¦jì%	Zç\x0017âk·ûìVRÇ\x001c&eÝ´ú\x0001üÏlWøYÛQx§Ýa\x0001\x0010»îÈëÇ[wÚ¢ÙÚfC´ÙË¸9e\x001c1Ç`OÊ>X÷×¨$\x0016ÒÄcBDª{'Ý±Ç^U[ZÈ))7Ìö2`Kic\x0007d\x0018:2\x0010AÈ4û»ng{^kÈò9Ë\x0012OR}M\x0018\x0005í;\x0017¦sør+µðçÃý_Ázî.b±±ÄVË*{¹3¨?A×'Ä95\x001dY×N2»\x0013¬ýþ\x0019ÿ\x0000Âe¨6µ­å<=a Wìn$\x0018>RãØ¼rr,þÑ_\x0011_Õ@ÑbÑ4¯ÝªC(ãq\x001c\x000eÝHã\x0015ØøcÃ\x001e$Ò¼+.àÛi\x000e¹xïn^M°iñ÷7\x001fÍ=öäö\x0001kæýVIZîHgòÙ¡b\x000fxê>;ÕÞÇm[Q_ÈÏùcÉ4À¥Xxð7ÉÀ=\x0007÷¿Ï­\Ð4kí{RÇMÉ4­µA8\x0003\x0000I=\x0000\x0000O\x0000\x0002O\x0015Õ(ØóÖ§gðá¦¡ãû×\x0008©g¤Ú×z$KÔxfÇn1Ô+²øñ#LÑ43àIöM\x0011>[«å8ôô'w\x0007iî{ô\x0018^\x000ewÅ?Í [x/ÁpÅ§øzÎ5vµ'\x0017r\x00007\x0010Ä\x0002SvNO-ÔûxÎK7'zÃÈëö¦¬·=¿Âþ\x0011ð\x0007ôK\x001f\x0010xû]W½ºgCÓ$\x000c@# JÀðGB>P\x0008#-Ò»ï\x001fü|Ò|7áø´_1Ù´æ0<ûx6[Z\x0003ü1©\x0000»{ä>QÝ\x001fZi$|n­ú\x001d¾µñ3ÄZ¯ÓDèEd]¥¹ò²¯y#\x001cº»têqÀã\XWl°\x0004ôÁ]W|-s¬[O¨^ÝG¥xzÙ¶]jW
J+c>\kÖIHä ú\x00074ZÛ\x000bÔ~ñÊQZþ$HVøzÚîßNP\x00161w(WÇWl\x0000\x0001n»G\x0003¦OZ§g\x000c2ó¤\x0008@ÈÉÅQ\x00113²*w§¤lü\x0000êOAR\x0018Ö0L¹Î2\x0014uü}*6bÞÃÐt\x0014É\x0014²¨Â\x000c·÷ô¦ry&q\x0013Å \x0005b¼©Çn)(4v \x0002¶|)ac©kP[j_eµlîp_Ã'õ5)éÔ¤®¬¦ÔdWG°]è
ôÕÛ&¨÷exÿ\x0000ZÏùlP?ZÎ]WÁ\x0016mM=æ#¡1ùîoé^dw\x001e2:±bë\x0015Ê3¢È\x0015(Ý\x0018zqÏå\\x001fSë)ÉüÏV\x0018õÌi¥ò:-JÙüG«,z\x00064Kð¦÷cì¨+¦¶øKw§Ã\x001dÏ5m7Ã6íÙw.ûSÝ`L·àqMÔ¾,ëdÖ^\x001fK?\x000eX0\x0001­ôD\x0005îdåÉõ;«Ï//¥¸vi\x001däcfl}MtA4¬­*nNrßúþº\x0017¢ðU­6Þ\x0014Z¼¾WÌ÷·"Æ\x000f	\x0010\x0005x9fã\x0007xãiIÉ VëCÍÒ\x001f\x00042O*Ç
41Âª~¦t
A\x0013tÐyK×.@¬Ø¦xd\x0012Bì§S)×\x0017SÜ±iæF=K147BéºI{é¶E"b¤ôãm.i*âQOÀÛM G»i\x001ahºµ¦³\x000c[lf&\x001bÈcé\x0016ïõ¾ÄbD÷\v¯rÑîF4!¶H.¤i\x0016Úã+Æ×ÆÉU»o\x0018_Ö¼\x000f\x000f%¹S,¶îÿ\x0000dFròÊ7t\x000c\x0008$g¯>¦»OwQG\x001dÎª:\x0018cû\x001cËù¶²«u>Äà\x001f÷+\RÚq/\x0006÷¥/Ïüpð±²ñcßi°F¶wè&#L\x0002ÛrÀ{õlqÁÈïOØ¿Õ±.\x0014µ®­\x000bÙ3©ÃFÍ­ø:¡öý+Ó¼W\x0004øNÎ×Ä\x0012Éskgqý}t2Ò¤|½­êÿ\x0000´¼g×{\x000fjà-´ÛÝ+_d*j¬$ß	ù.\x0000ùhÏNF\x000f¿Ô\x001aÚ\x000bã¹Îäã^ÓØÌñ¾?µia¾®#h¤¶\x0011¶çzqìv0õÅ]ø9áF×|K\x0012-ÄP5\x001bÃ¡a!\x0004|Ï\x0000çOzõ/\x001al>'ðæ®Dª\x0005Ìb)eq~¡ò¯;øm|<=ã\x000b	a#G!#þY¶TþY5pm\x001aÁrÍEôØè>*C\x000c~-JTXí.í|èÕq, \x000c\x0001ÓMyWåÛQ­Éá¡4$ýÙ¢"T\x001fcñ5ê?\x00194¡¥øÞk´\x000c±Kò?ºxoÈ^uª/ön°eq\x0014sEy=
à~\x0004×v\x0016\x001c´Õ;\x001bQÎ«R6.´Èõ
{I:y\x0011YjÛ^ß"
"Oø\x000b7OAU|Y \x001f\x000cx»ÄZ+ÜãÛ\x001b,¥vç(¬¤Øn?:Öð£$:é6_K½[«v>¾Ù\x0007Ñ¢ÚßT\x0015ÖüTðÖµñ\x0016[¨dtýRÉüpêÞTCpÀè}?\x001aujòTö\x0015
\x001eÒÜò]e
Ä	T¨{©8?í¨8ÇÔâª\x0001¾Þà)þ\x0016\x0018éÞ·|K\x0001¸ÓW\x0003æÛi<¼\x0011\x0015¿ÆÂ\x0005Î³¯OalSt*\x0006s\x001egB}ºþUSM¶Di¶î;í\x0012ßCø-o«yò½ß\x001eÞÑâ`6,I3H6¹>XÉ=«Ï¼4b±Ö ¸#!| \x0000äá[ð8>µêÿ\x0000\x001c-ÎáO\x0006xsz³YDÆC\x0019ùY£@\x0019ìYØ×É§¼<·»?Ò.nÌVäç2Íÿ\x0000}:Â¸pòæ¼Vzx4ÔcÑ\x001eá½ êz¬\x001dYíØ©Û\x0007i\x0001°'é\x001aÆ¹}Riü]ãû¹¡RÓ_^º@\x000f\nØ \x0015ìZµÈðï\x001aT Ka¤(_k\x0014~!Wõ¯\x000eð\x0016¥6â\x0018uHB`\x001eå·Ãh\x0004cñÈ\x001e´å'ZRé BÔ!\x0018Ë®¬ú'Æ:}¶¦i6Í".áÕ[«¸öópÈDôÉm¤úï¯\x0002Õ.w»Ôµ\x0017\x001elÌeCýârß©\x0000
ôozÅì>\x0006ÑloÝ?´uOøê\x0003;6®w"`öÎÕ\x0003þ×\x0019ðóK:×£¹Õ×n §Û®Aä;.J)õ%ùÇ¢\déÆU\x0019µUí\x001ci­y­è^\x0007Ñâ	ÁKÍFåã$¤².Tz~î!×Õ\x0015Söñ\x0005¼·\x001a´I¶iÚgÉ3³gt¡rîÇ¾ÅÜIþó7p+ÔüAâ\x0016ðOouëÍ¿Ûú­åGÅfacÒ4\x0001qê¤ujñ\x001f\x0011x~k]\x001eËB¶¶_\x0015^ÊeÔ¯]CÉ	e\x000cÐïÇ
É»]ÍM*·jS:'E¸òÁy#Åµ¹CHÎªÉ\x0011À\x0008û¨8Aùr}ë;\x0006(\x0006Aß/O÷úçùWQâ+[Iõo²Ù³5µ¶b7
ÉoßÒ³ìt\x001býoU³³°Éu|Á`\x000e\x00153Øpyô\x0004×L¥Íï-?e(>N¦ÿ\x0000ÃO	¿uhí$"
"Èy××9ÀHÇ'Aé{\x001aö?\x001ax0jw­Ï-¶áõ\x0011èÚ,06gùqöôÏP2F:\áñðÂK\x001f\x000børÒÇT6¶©=Ê\x001cÓ\x000fNÉïÓ¦3á>%xïPø­¤úB-íPÇ\x0012Ã\x0017»3ä\x000cú×"¥*³¹è:¡NÝS¡øñXñM³Øiè4	²©cjÄ4Ãý¶À-N\x0007×­yM³}êSyJ°9\x0019\x0011ú\x001e¼UíF9lÑ\x0002O(À\x0004üû}@ì?ZH°&ô´ÄyQ}÷ÚYW?Â\x0007vô\x001fvª
\x001aDó¥]ÏW¡{M´Òïm}N+«hÓ¬°°Ãz\x0000§¿Òº\x001df[[\x001d&ëEðKý³Í]·÷°ró/\x0007É}ï(\x001eIÇÎÃ\x0000®SYº3:Ä*8X³´ûäÿ\x0000\x000f­"½×,à¿¿N·Ps)!cõ'nN\x0007ùõ\x0019ÖèÍ©Uº÷¢µ2\x0012	¼¢%ÎÝ¸9Ï¦=i<¶2\x0008¶°;vãôÇ×5î×^?Ð¼+$v~\x000bOíØs\x001bëºýó\x0003Á[aÖ%ëó\x001c·?C\¤:\x0006¯j±ÞX\j6·óÜyokr\x001a}Ó¾J\x0001bIç\x000c¹ÏSÎkÛ%º6ú«zÅ`ÊU°äqSG\x000eè^W`\x0011~QêÇÐé^ë¯|\x0001M\x001bSê\x001e-Òô»YeýÄ7\x0004ËvËÀ]± \x001bØð¾ÜúMy\x001fÂºÂöºüC\x000fÌË1D·OB½2?ºCãóÅ/jÔËÙ5«ØóM\x001bÃ6\x001aFo®øÜË\x0015ËæÙéQ6ËñÙ³ÿ\x0000,¡'þZ\x00113´\x001e£#Å^(½ñ\x0014ð\x000b\x0015½ªìì-d\x0016¨Nv¢ú¥Y$í¼iñ\x0002ãÄ\x0012ê.\x0019Ð´ÆÔ\x0017\x0012Þ]ÇçÝ\x0010Wo\x000f'Ýàc(£\x0018¯51ZG÷çy}|´ÀüÏ?¥i\x0008É«ËFEIE{°w*Y¸äÓ¶r¼¿céWc\x000b;µ´U\x001d±bè+b×F°$,\x0018ÿ\x0000\x000ch\x0007ô©©Z?
6G5\x000cRÜÎD$®ÁUTd±=\x0000\x001eµÜ¯Â?\x001d2nÿ\x0000cT\x001cg\x0006\x0013·§èÒY¼RÀ<©PY\x000bí`AÈÁÏ\x0018<×¤i\x001e*ñæ£:ÛÙxy¤\x0000n\x001eim£Õ0?\x001aàa\x0005ðô²öÖ§k&¥ ê\x000fc¬Ù\Y^ \x0004Å<e\x001b\x0007¡Á¬ð\x0006y¯¤<U\x000e¢_SÇÉ¯x )lÏvÝñÎpGü\x0006¼CÆÚÊkúÜ·â;xÚL
ñE\x0003°Ï'ë[ÐÄûm#\x0006¨«¹\x001cé\x0018àÒfºï\x000cø#Ä6¿þ\x0011­\x0012æâ&sóªí1Ø4\x001f¯Tµø#áÏ	À·_\x0015<_kbøÝý`ÁæolOä¸÷®¤qªmì|ûNVé[\x001e1\x001a ñ%øð·Úÿ\x0000±¼ÏôoµeÛãß8öÆk\x001d\x0006M\x0002³NÄè\x0003\x000c~´¸ qõ¥\x00102\x0000§7#Ò¢çJ?t& z°F\x0017¨#ØÕgÎsÕDÊ¦ÃE*ã<ÓjB6¨$`ûÕ\x0019!­×Ö\x000cô='Àº:iö·þ&ña
ÄBU¶³Ý}r23µ>T>ÌÀâv*\x0010svG5-½´×2íây\ôTRÄþ\x0002½\x0015µ\x00122é^\x001dÔ5ë­£\x0017\x001aÍ×\x0018oQ\x000c8Èú½AyñkÄ²A%¦-¯ì\x001cäÛèÖéh?ï¥\x001bÏâÆ7cOd¢ýæpNG2*½Y²¹<æ«SDTµô?An4m\x001fÄ>³o
F¬ÀKr\x0007Î\x0019F\x0011=S\x001c÷Ê¶z×ÙYÝXÞKöõÎ­¢7Ù¯\x00161>Õÿ\x0000s×O¨_ZÜð\x0016«w¤Ü_h×\x0011:ê\x001a<­r¶Ù,Å8óâN~e SÔýkkÇ\x0011Ak¨ØøÔù¶i\x0012Åxbÿ\x0000Ú|Çå}Lm\x000f^\x0014Ö0q{\x001b´¥ªÜÜµ\x001dsB¹±,­5Õ»@­¥OÞF~eã^Q¡ÜGâ\x0007±Ñ¯'{k¤V° 7<[³%·ûÀnhóÜ\x0011ÜW[§$öZØ"í,-7Gó,RgÌ¶@ÏÉ=6È ýÓY\x001e4ð\x0015ü÷¶7\x0019Ñî¡´Ô#\x0012Ko\x0008ØÖ7Jya6ô#Ðãµvá¦¢[91PsµHæa\x0012ÙøÁúÂ\x0002Ê.m¤f\x0003r9Â¸ì\x000eà¤Ð:×4\x0006åÍÔ,¼¹þ\x0016è\x001bèz¥ªê>&ÓôýNñLZÞ$ÚF®ª\x0006ý\x000cL\x0000þë\x0008äÀÿ\x0000k\x001d*»x^÷Hñf¯ºÇ\x0015ÝÔfê,|°¶@'=6å~µT¤¡~aV¦ãÈrZÖ©w¯ÛCq¬N&Ý\x000c\x001c&>éÏ>¹V9úV\x000bÅiu¥|³#Û\x0019Þyd#ê?
èõ+
BX/\x0011.®nÄ$ÿ\x0000\x0017!?ª\x0007ü\x0004W\x000e&ÏT\x0010æ@¸ ÿ\x0000\x0011\x0007Ï\x0003ó¯W\x000fË(&\x000f\x0018å
KrÆrÇÄÚMòª¯Úap\x001dÝIÇþ:?:õØgm/ÁñÅ"¼Öðß£Æ§, Fà\x0012;t\x001dkÎt>9ïtYmy¶:Ë\x0011ô`®Ëÿ\x0000\x0001hßó®ÁS\x0003â+\x0019:	,î÷\x0011þäÊ²ÅÑæû\x001beøJw8íl]Ë£Á
¬O´´ûCF»!B	#øyi\x0015ºÕ´ý_OCÚº­\x001c1¡nP7\x001d\x001b5¿­k\x001aôæÉ£\x0011ÝZA\x0004É¸íÝp2=ñüêÁ\x0014ûwí#²Ê×\x0003<à\x0004þ@UU ïØÞ£9ÇÝßî*|q¾óÆóÀÄ\x00184è¼ãÝõ$çò§ëú#·<)áH÷,Ekk?\x001d&¼Ùäã?îÕ Ä?\x0013táp7Cyz\x000c¹#î#³¶à+[ß\x000f\x001e_\x0011|MÔ5,nÜ_Ç;*!£\x001fûæ¹\x001aöqÓ¢;£?k'æÿ\x0000#GãUø[\x000b[%\x0003ý:úK\x000bÿ\x0000<â\x001eT
Mp¿\x000f´\x0001ª_iyÉQ½Ìç°¶oÀ¶Õ®Ç1ÝxÆ2ØhÈ'Ò&³\x0016\x0000\x0001
ÄÀçwéJvxcÁº­êÇÜãD³ÇÞ,Av\x001eäqÜ
µjt|ÙR­þêý\x000e[W»â'Ä«$\x0013Å,â\x000bD$\x0005\x0011Gà\x0002FàB½\x0016ÇKo\x0005øilõ\x0005¯Fü1\x0004I.â-¡$vÊïodnÆ¹/\x0006xXYøØê-\x0011·Ó\x0015.oÌX+\x001a¢1}w²¡ÿ\x0000uªßÆ\x001f\x0010ê±´Ò¡
6¢Nß*0\x0006fsÄ\wPÁ9çýeyõR4ôêvÁÉ'RÚìwG»æk¯\x0014j\x0005¯,´©KZÇ!È»¼bY\x0017\x001dþlÊØì¢²<Y}«i¦[S¨:ù¨wW\x000c\x0000/;ÈZg'¨ùú\x001fJôMSI±Ð4¿\x000bx^Ú\x0008/%Ó·j7×D}Î	,=\x000c²aGû 
ÂÕ´«{ÝFâËRS%¥¯&é¹ÏÌÀcûÎØÇµBkDwÓ£mv<oPÓáòêX	¶Òæ¼\x0001\x00070§\x000cWÔø×yqzÞ\x0003ðá¹eX|U«B\x0004QàgNµ<\x0002é¡Àü~6`²Óa¹Åºª+ZY\x0015ËOVáæ\x001fê£
\x0007
¤äú¼ÏÄ7÷º­w}­9{ÌLð\x000fdAè\x0006\x0000\x0015ÙN´It_ÅZ·²n}^ÞG;ûÉ\x001ePÎ@vÜÄç¹<Î¯&mcVl`À eÜIõÁàåOµ´\x0012\x0016¸\x0014G÷2qïíïI\x001cm¨]K²EHc\x001b®.î öþ@\x000eMwªj\x0008ó\x001dG7èIgj÷o=ÅÌÁ\x0010s$Ìw7?Xô\x0015Ùß|8ñxZã_M\x0019ìt{d\x001b\x0016V\x000b.Ü¼)ùòØç<t­/\x0001%Î-,4¿Ú]öZlê[ÍF\x001b|Ì\x000eL¤Tö\x000bÀéHñßÄ]kEÿ\x0000l]ÛÏâWtv0Ç®;gþzMÏ|üüìMI©(@ô0´âãí&xm¶¤épý¨ë#R¼7­¬íe
¸SÃK&Üa¶ç
{àÖ\x0007¼1{â«ÙÄ2GkelK»éÎØmc'«\x001fRx
9cÀÍu\x001a&&¯%Î§«Ý\x000bm&\x0007Î¡:î\¶O\x000e^V\x0004á\x0007CH\x001c×¨xOME¶Óõ¡<¾\x0019ð6Â{KG_ßÞLÃib2egÉ\x0003v¢\µj{5n§L){gÍ´Nw@ð4>+=;Hµ:WtéKNê$\x0017·ò¨!qâ4\x0003 (;P\x0012[sWmoñ\x0013O³´>\x001eøO¥Çs¨Z«¨¿\x0015mm#\x0003ç3\x001c¼Èø\x0007ß89·ZÄ&¹ðý·ðïìcIobb±´q\x00037/ÊÅ¹\x0011.O\ã­y¿Ä_\x0011hqX>à§\x001f
)1òÂ\x001bÙ\x0013%¥oâl»w\x0003ÀÍg
R¼þâ¥Z\x0011MAiù5¿\x0013Ùé\x0012ÞÉa«\jºÝÁ+}®!ýä¬F\x000cp;«\x0004Ê\x000b°þâñ^q6¬ø)§Á
g¯2íõsü°=ª£Ë%Ë\x000e\x0015#A^G§ùëQ¼Sl`täã­u¨¨ìpÎN£¼¹i¾s'îMZÑíb»Ì¨ÏÊ»{u\x0014í\x0013O¹¾Ô-Ö(È¹`8\x0003"º;M%íÄQØ\x000cª3»\x0007\x0007úW."ºµõ:pÔ\x001c3Z\x0013[-1\x0014\x0019ãwÚ¨=p\x0007ZÑi$Ù
l¿
°®]¾än+kBð]åõ°¼ÔÞ=+KQ¹º`\x0006=\x0015{z­«ø÷Jð¼\x000f§x
Ï÷äm}Råríþâëùw¯1AÖv§­)*qæÜA²Ð¬Åÿ\x0000/\x0016É\x0018\x0006É_uÄö\x001d3úzÇÕ¾0Ëf>Ïá++}:Õ7*æ0îÙèäþ¦¸ýoÃú½ç-<_}~·ÐÝÜÉkpw3Ëm2ò© #Ëó.	\x0018\x001dºW5\x0012¦\x000eÐ8é»ÿ\x0000Ö®¨`i­g©É,lß»MYw\x001dys}u,ÓÊí$¤³¼X±õ$õ5êß\x000eu^\x001cðÜZ¿¢ÞëÞ%,ÄÛÎ\x0000¶L1ÛpF1Àçòó\x0014`ï<p8\x001dÿ\x0000:l\x000c\x000c8ÁÆ\x0001®½6¤½êç¬ø¿ãçuX>Ç¢¼\x001a\x0016\x0006Øíì\x0013c*öùúø\x000e+É%{íV÷-ç\ÝJÞîîOêMz\x001emðßJÒm/üA{ªëÚ±\x001fM³ì°ÂÝãVå¾©Å[ºøËw¦Dö¾\x0005Ñt\x000cZ°+¾Ö\x0011%Ë/£Ìüî\x00004Ö\x0013%u«²8=oÁþ!Ðmm.u­\x001eöÂ+²Â\x0013s\x0011¾ÜgÈê:ÖdVòFÃpÅ}\x0015ðWâïb2§¬¡:\x0001F­$Mq,ÃÂFbHí£\x0018¯c½ñ?ÂmsG»â÷A{IlÊÈ"f\x001d}\x0003gÓ\x001cÔ¹¾¥FV±Mù\x000bm ±
\x000f¨ë\x0018ÿ\x0000\x0010<\x0013\x0001Å_ñ\x0007Ø£Ö¯ÎúxÅ¹só4[Üûã\x0015òqÅ\x0011×Rª5
\x0006ÌÃ$p>\x0003\x000c\x001a\x001dÄä:³ö­QÅ7}A\x0006X
r3Òh'¿ojoSLW²°\x0001N\x000cqÁ?7?¥\x0000ûÐ$ì\x0004æ¥\x000fQÁíQ\x0001SàmàÒeC»:
&ëÂñØ¬ZÖªMsí5\x0004\x0011>F¿>Õ¨µ©¾éë2Y>RÎC8^Û\x0000\x0013ô\x0015]Îi´$TêsicíT·Yðí¾¿ákv·ñ'¤Xf¶vËÉ\x0014cý[rw|¹*}7/8®M0\héö\x0018LÚsÆ×Öp\x0011Ö²qskÓ\x0019C\x0017Ù\x0007A\¿Ã;Û=?ÄÚD×/§ÝÚ±dL\x0013¢«:H£©\x0001Y£$w®Äº¯ö\x0007ì5IáY\x0012K{+\x0004á2\x000f\x001dU×9õ\x000c}(«Km\x000e_k\x0005.ä'Å>!ÒüDñ\^éßØöÈ³7\x0000LZ\x001cl88\x0018#Û¨®ãÄ:{xDº¶¶½(u\x00086Ç4\x0012äL¼«\x0002\x000evþ¸\x001eµÅêkik©	|ëHmâ=òßKá uòÏÎ\x0006zcÞ±|5>£¥¾µá)/$qbCÛM\x001c 3Ch¤\x0004\x001c\x0001LöÚßìÕÅ'¢"Påw¾ç;ðS¼ÑüS¨xS­.®U­¼É\x001fî\FKFÄ¸;ß+]ÿ\x00005©5Í\x0006Ò\x001d\x0018®-¤\x00122A\x0013@Ø.¼íåá®3Æc}\x001e{¬ÀEÅÂ½¼Öã÷©<X\x0005z8d*ÛzõÅoÉæÛøWûA<¹ÅÜ\x001a3Ær²¬U\x0007ß\x001c¿5w{\x0004í>ó^-ÚPÙ¡¾<âûÂÒj°K$ºuüwÈÈ£0Ï`Û²\x0007o­yíÄ\x001a¼70|ñ\x0001\x001cÎaq\x000c
ú[À­\x0010Ñ\x001fKp\x001e(2\x0010\x001fã¹_Ð×_è\x0006ÇL¸´7g4±÷¢Y\x0006ßÉ\~UXJ¾Ï\x000c]\x001f¬J5\x0011cÁ:m´>\x0012·¹»N\x001aõÙIùQâÊ®ßL3õ¨¼7\x000cPj\x0016\x001b%fC~»p\x0014\x0008Ü\x001eùÉ5³à«gÂZä-Æå¥Ïû2C\x001b\x001fÏ\x0004þ5>©¡¦âÙ­¢w3mq:\x001cñ0Çæ+IUæz\x001c?³¯\x0019Ehyö¿\x0019¾ðÕ9hííóÙ£¿öqP|\x001d¬oõÍW\x0004tß%W¡\x0012Ë DþF´<Eþu¥Ø\x0002\x0014M\x0004¡½ö(\x0007æj\x0008Ò<\x001b©Ê7\x0003q©B2\x0006\x000eØÐ¾\x0007ü	Çã[×\ÑF\x0018\x0017ËROÔÆ¿´¬¢½X\x0018Ú\x001bÍ\| ²d.}p¤×©ü\x0019´M\x001bÁú×.T+3¦F7G\x0002ÏÐÈÇô¬K½?í_\x000f´}2Ò`%¿Õ¤xR\x000f@?îï'è
w'Ksák
hî´ñÛØFÀº#Ìä»O®k\x0015UrüÏC	IÆ{ô9½\x001bN_
øI5Û©d}SQ¶²¶0ªìev\x001eåWõ\x0015Îx_KÕôßí9$¹O\x000béãT¾\x0008oæmÑB\x0000õrÏð­z¥üV7\x001a¥õÅê\x000fì\x0016\x0004@\x000fE*\x0016Wã¾\x0011!_ø\x0019¯\x001bñ\x0004W7¾¸¶µ¼¾õ½A$s½Æ-á
\x0001?,~¼\x0002õÃMÊ«W=NUM6C­ð|3iþ\x0011·³uªê2ý²rÀ:fv\x0010¡ÏmÛä=°¦ ð\x00065\x001dfã^÷¶vâ²ÏúÖäMpO¹;A÷cÚ¯£i~\x0011Ñôxu\x0015þÓÕGÙÖé¤Ü°#&\x001cô\x000bS\x001eGZ½ãKË\x001d;Bÿ\x0000jÌÓ,ÑRö\x0018N\x001fh\x0019H\x000b\x000fãnIÇL±<u\x0016\x001au%Ë\x001e¡,D(ÓçBm	mµ­J7Ì\x0013Êu\x000b@æå!û¸ôC @£º¨õ®\x0003ÅW
g©\x001d\x0006"óÎ}·QW>}ìOM±þYìk¢ð6µ&¦êú£ps¶(`vªG\x001e \x0007°®_ÄZD°¦Ð]î¥fy\\x001c°F\x001cãÕù\x0013ë[G\x0004Õ^E²3úûö>Ñõü\x000cÉ-`R\x001400E¤\x001fõ²\x001f¼ÞçÓ\x0005dë:
Üm[hAÀ-æ\x0011w$úóÇ½t~\x001aÓÒy¤Q[iºr\x0019ï&\x0003rÛ§e\x0007ø¤n\x000erj}GÄé©Î\x0005­¨µâ\x000bkU\x0000\x001cd	þö2Ìz\x000fÂº\x001aöR²èb­^\x001cÏKÖae|¾D\x0016!@¥\x0016ã«\x0012G#¿Ôú×[ed_É´°¶
	\x0002(¢+;ö<\x000e¿ÈV·´\x0002YÈ¶ÿ\x0000mÔn\x0014Me`§h¸ÁâyT¶_á\x001c\x0019\x000f>ïWb\x000b­"êâs\x0015ÂÛ\x0018PHÆ\x0017#æØOÌT\x001f¦{TO\x0018¤ì>¥É¬ãJ"ðl°2\xÔg\x001f2Ú\x0003ÕSÕýMy$Þ\x0007¸S¼Õuf¼:\x0002HÒ$ëæÜÝ1Îè¡S¿]Îrª9<àWµÙxv-OSi,á¹{\x0002s\x0004R¾É.\x0000à»°ûç?7SÑrzlê7Vº\x000b£ùwZÁD²¢mÝ;G\x0012ÿ\x0000\x0002þ§¾I¬ï¤ulèlï="º\x001eO\x0016iiamâ?\x001fÅo¦è¶ ÿ\x0000dø~3á\x0007\x0004³ç$cÄäËg\x0019Z«wâøÇ|G{7|\x0019\x00032[Î£ý&ï±Ñ\x000fñ\x001c`Éù\x0002£Õ|KàM:þK/\x0010ø¶\x0019¯/Ä\x001f¹Ó\x0018¾ÇnqæÆ:"\x0012\x0006	è}\x000fkÚ.¥ã\x001f\x0014¼þ%ÕY"]ðC\x0000H`}ÕTÎ\x0011\x0007§~ç½cK
Ìîµ}Íq\x0018¸¥®·sñ%Ö´Ø´­*Íto	Û¹k]2\x0017$ÌÝåÏ2?\x001fxôè;äî-Ä\x001f½Ô²$ÀÙl\x0015\x001d·t{u?kØ¬¾\x0016£Ìe·ÕópqûÉ­7mÿ\x0000p\x0006\x0000~=;RÝ|!È\x000cÚ¤ns\x000bf\x0019üÜ×zÃE+&y³Å¦îö<>Yå\x0015G\x0000\x000e\x0000®ëL½JÑá_ÜI ù4[öQSÿ\x0000ë®¸|$[Èê
è\x000fúíXgÿ\x0000\x001f®ÂÇá.hë>µ}}s(\x0019û<E#ÝìØSì
pc0Óg¡ÅSrgxi5o\x0013jö§M³2,s#6\x0014$qG$:}\x001aÝ¸Ãþ\x0013»M{^3:(\x0003\x0016ð\x0010Äàu,F{~è×MöÑÙG\x000cXFFÛ[i5È ã\x001b×"¼cã6©øÇ\x0017Tk<\x0010É	T(n\x0003±bÀõ#s\x0011ÿ\x0000\x0001®'~öô\x0016gMÅòjÑã_\x0014_êE©y\x0007Ü?å°Pp¿SÍp«/Þ+¬Ü·áNÒDbn\x001d#çË­Cº$æ=ÏÇWãô®t\x0015(Ù\x001c51\x000e´¯#¾øcâ\x001b\x001d>úïE×Ù5ÈÅ­ñêb9Ìw\x0000z6ù»ðO\x0015Îø³B¼ð¿¯´}D\x0001sk&ÂÊ~Y\x0017ªºÿ\x0000²À\x001eÆ°Õð¸ÉÛàtÍz«Áãß\x0000£\ykÞ\x0015÷?ÖÝé¹ëÎ~hIÿ\x0000¾\x001b¾(µµ5Sç²<Ô± \x000068ÉþU\x0019;³\x0012Nzõ©®ÞL-¬S!õPü~Bµ</á­GÄ\x001a½¦¦DÓ\ÜH¨ªªHBN2ç\x001f(\x0019É'ÒV;JnÛ®¼&Ö¿\x000fí¼Owv±\x001bÛÖµ´´1Ó¢.d6xUb«ÜOãÈ>8Æs^£ñÞím¼Ikáû(4­\x0012Õ,lñæ*ýùp8%ßqÏp\x0005y¸~÷\x001b)2¦Üóó)9Çü\x0006ª\x001b\Î²ÖÅ@JJe¼qõ¨vàÒÍSIFN=Gù=\x0006=\x000f4×rÇ\x0018\x0003è*î£jZþ£\x001dcsxù+
¼eØÔàv\x001e½+»OßÙ,\x001bÆÞ%Ñ|>\x0015¶Éoç}²ìÛ\x0018sø\x0013
Z \Ó<Ô\x000c¶*ÍÎ¡u\x001d­¼×7\x000ep±BÙ¾d× i|8Ð\x0007üK´]WÄ·aHóuIÅ¬\x0001à¢ùög¨o¾-x­$´Ñd´ðí~Ï¢[­ Èã%×çoÅ¨¿b¹\x0012Ý¯|5¬øj[huí6ãOâ/:(î\x0013cÉ\x0019ÛÔr\x000fZÄ©îîf¼çºI¦sF,Ì}I=j\x000cU#)Zú\x0005\x0014b\x0004*ñA&\x00003E\x0015×øWÀ\x001a×ôÖ¾ÓcÈY\x000cYrFH\x0000ÞõJ.[	ÉE]õð½-í|BcÔ/î4è6Å"\x0001µe\x000c6ï\x0007 \x00078=ì3^ã'<û\x000bý\x0006çdÚ\x001dÊ­Ý\x0000V³9Âîîù\x001d9SÆ+É%[u\x0000ÿ\x0000jÙI\x0003d\x0018ï-d@=\x00058"»/\x000fxXô)4{Û{§³&[{«iÌÑ*ã\x0005D©09\x0001¹\x0018ô\x0015ÝÃÊO'\x000e\x000f\x0019\x0015\x001fg-\x0019FÞÊæßHMóªxzf¹\x001bï=«q,xþî\x0008`Fr6Ö\x001fJé³øsÄöÒ\x0007\x00163ä¼\x0018c\x0018oPPÉ\x0019'º­u½Íü+e«"$º¶\x0002Éu·ä¼µ`BL@ê3Ãr¤Ø®j&WÓ§ÑÉ\x000b#Æ'´x
-å\x0011ß\x000f»\x0019õ\x001eÏN¿7C¾¥HÛú½\x0016hÉ}áýrÖ\x0019\x001eTbÕläQÆÀ0Ì\x000f®Æ\x001f\V7®ñáÏ\x0010Ú^ÃçÛ,\x000bq$
ÅFðãq_Bxaï]'n],t¸n\x0014°ì\x0012é%´ò÷\x0003ýÒJÿ\x0000ÀO¥7GÐ!Ó'ñ&À$ÐXÊ»Güµ°1¸÷\x0003 þ\x0015¼*(§	|>½\x0017RJ¤zîhé\x0017çJÓ,/ì¥\x00176êVÕån3\x0011pw£!eÏ¶kmàÿ\x0000Ã1I\x0012ºO0¨ãkº\x0018Ø~\x000e¦¸¿\x00042 ÖtKóþq\x000bJ¤u\x0005F\x000b\x000fÃ\x0007ð®§Âm=.¬î$wxËD¹Ê©ÈrWêYãQZ¼äº\x001bá«%\x0015N[~\x0008³óôOs!7ZzÇ)S$E \x001c÷ù]Gü\x0006µuÔïÆ:<à+¬ed\x0003Ñ¹\x001f 5\x001e¦É§xU°]Ëlñ¹t\x0005J«~H«\x001a\\x0016i}`gEÔ&³d<|¡S<ýpß¥RO+[SÈ>$L5=sí±A
ª@¶0à`cpÀïç¥AâÄû>¥Ú\x0001ÌòIqbF?Ïµ\x001aÅ³]j\x0016×\x0000¬¡¢ü$ª«3VüV¢c¢F Xà ë´{È£ëïq÷RG\x0005:·r:>Ê(ôí\x0001&ùÚ\x000b(Óiâ[eºÂOÓuIá\x001b¨u_\x0018x³Å\x000e\x000fØ­_l'n2¨W\x001eø\x0004þ"¨Ê'×öÃ\x0010-c\x0008(²\x0004ò\x0015ýqÂhëWÂ6ik¡ÙiPÃn%»¸{¹b\\x0001ä«lôm«õÉ¯'\x0013+FÝOo\x000b\x000ekKdVñ:\x0008¼7¦é\x0017Í³ûFG¿ÕX\x001f»\x0002\x001f6UÏûLR1^at×\x001aÕýÍä±·ÜÈ2½³'ÊØ*ã=±^ã-FÚòòo>ÒY"Ú\x0011$$\x0013ökvãðywqBÓü\x0019áX¯.ã¸s¾ÊU}ØáycúãûÆº0(9HçÇÊud¡\x0017cðìrjZ¥×¯§\x000fe¥Æ¶¶\x0012Ê ©d\x0005\x0015ö }à£«\x0011îkÛSÔãD,ÊÌFöÜÙsv?Å#÷=±À\x0015è~.±Ô5{³nñ.¤ÀïäZÆ,zn`8Î0\x0000ì?\x001aÍÑ|5\x001dµáûp²\x0008R%Ã\x000e@ÏRGSÛò®Ú~êæ<êõ\x0014íNú\x000cð÷./,µ\x001dJ}¢ÔÊ«e\x0014ªXÜH\x0006\x0002\x00009#¹Ç_ $G
öZ<Ò%ÐÃ]4c\x0008ÛN\x001dÆ@\x0000\x000e§·\x0000WeâRU×O°´)¨I\x001f\x0014)ÿ\x0000.q0û ÏF\x0018Éþ\x0015àu¥Ô|5\x000e¢Á§Ë,ê\x0017WìÖä+M èKv9'±ý+Ï©Ûz\õ¨PÕ#Än"_º³ðÏQ×JÈv\x001bAýíäÇ²¨Ï^\x0018äâ»\x000bÍ\x001bFÐ'Ñìt/ûcÄ\x0012Âb²óºë'-q2ç	n\x0008àp\\x000eNÜ×HöPø^Ê+\x001d\x001aÕ5\x001dnùs\x001c`ae\x0000ðîOÝ·CÎ	ýáË\x001e+"ÖÒ\x000bM'P¾¹Õ$0]65¿\x0010/úýEÿ\x0000çÒÏ8Â\x001ccpÇ\x0003QËZ¤¥îÃDwR§\x0015ïÌÖÐµVÐæe¼±a%üEâ\x0019ÐÈ³Üô\x0010@8ÞS UùWäT\x0017$¸Õk¾"M7Ã\x0016Ã0YÜä´Ùû³L\x0007,íü\x0011/'=ó\x001dcÄv^ º
RÒâ×Ã)²ÏHÓÆ\x0000ç\x000b\x0019oï6~g\x0019<àUÛuï\x0010jÏ5Í½½ÕÌóK![=\x0002#þÑÎû:[·¸Î4$¼S«N×ÞG²]ë2N#Ó´\x0018¤iî1¸íËâí;p\x0014\x000cq·á=
Ín&v»KØpÒÜ\x000c°çþyçï7\¹àqkÍ~\x001ej1-Óø[Â\x0016W¦ùLój3äK;\x001f¼ï"¹Âç'©êkÑ-ü;k\x0006n/oc\x00108\x0016ýX¼\x0000Ïsøv®¥\x0014£e§æpJRæ¼ÿ\x0000#©]§km\x0006ØÞÝ
Ó\x001f¸tÜÇ¯ÿ\x0000®¼§_ðPÑ\x0017íò\x000b§lMp\x00079Â~v>ø\x000bõ8®ÞÛÅ/e\x0004¶ö\x001a}´Q\x0006Ìdg\x001fêÇÜ×WXñ\x001f%öêkAá\x0003äSì£jéR]ú\x001cõ«SkvËZD\x0001OÊ\x001a¤½µ,Ç\x001f/×Û´±ÌìyQî³\x001a|Û>¬8\x0007Øf¢¾\x000bu\x0007ÚºÔáiY¶ÆKCXï#i8Æ\x0005\Ú[²±ª´9ÂªIúw©¾Í\x0003\x001cdö÷­È\x00168 x,\x0012ãlqÝWû©úþOÈTäí«Ð¡
¼zQýÆÙµ\x000eó\x000eR\x000fdõöº\x000eÞµ\x0006¹mkâ+\x000fìï\x0010ÚE©Ú%>Ð»¤ÈÆä~\x0008éÓ85°,S,\x000eÿ\x0000"@3Â}ê=kRþ±(¿wD|ã\x0002ê\x001e\x001cÕZÖîÌÆ¬7Cy\x0013\x0016·g¥þe>ªI>Øæ\x0004ü)ñ/\x000cí¡[Gs\x0014\x000c#vG\x001a1\x0019ÆOS:\x0003Ö¾ÃÕ<=câM2]/Wµ[«I¹(z«`áÔõV\x0019àñ\x0015å7?\x0008¼Uá{û±¤ë÷6Þ\x001c·\x0017´y\x0004Årp\x001e4À.\x0007ñ\x000e\x000f§jã¯OcÒÁ×Uei\x001c¼_³N£ihn<EâM\x001bMLdrBýXí\x0015Ãx\x000bÂþ/µñ\Z¡E®©zËy\x0013?xeÑ#¡à×u©=$¯£øCÄ#¿Cÿ\x0000\x001fº¥Å\x0001ëWÿ\x0000e_­TÂÿ\x0000\x0017¼|ë\x0015Í¤F'ðNâÖ!ìS?5Ä½´´Q±éÎXjJòß/ü\x000fáiZ_\x0013êÿ\x0000ÚÚIû\x0006ºHþ¬¿JôOz|Cos/¼5¦èÚAXm..\Çºb0\x001d6¯ÌWp@'qÖð/ìë¢èW)}â±®N¸e·\x0008c·SþÐä¿>àzöH\x001cZ\x0000¶êª'ª\x0000Eì\x0014\x000e\x0005oO\x0005ÍïMÜà­(¾JJÈøëâg¬|/ã»X<Zþ"¿¶kpnïFØþÓ>\x000e|pA|£'\x000f\x001d+,xÀQ2Yø&K©3Äº­+ÿ\x0000ã±\x0008Çó¯³µ\x0018`¾²ÒöÞ+Y\x0006$d\x000f\x001býT\x001að?\x00024Vg»ð¤ñé\x0017-Éµ\x0016¶cê§O¦\x0008ôÅk,#KFE<Ñ6Üã¯sÂü[â«]vÆ\x000b[o\x000eèzJÂûéöì²?\x0018Ã;;\x0012?­r=ëÖ5\x000fþ0¶äi×\x0013òAt77¸Þ\x0017ükÕ<	â}3Ì7\x001fÕ#EÆdû;:sÓæPA¨öRBxÔw¹J#akfÚßÞ%ë&Ù\x0015Sh\x0019ê3Ed3OÌy4æEvÑEê¬0GáQ\x0010FEE¬k*É$¬\x0014å
TäÝ½)È\x0016¦\x001d\x0005«xm ÜG©É.>p®3íÁ¬k¶®$kTt±Ø®Û\x000fsPw§`ã4±¬ês¤¬Åt:7üG¬Ä³éÚ-ô¶§´\x0018B>²6\x0014~t\x000f5}\x0002Õ¡ÑæÕ\x001bµÜ\x000cã1RàqÐ\x0011T5}oUÖ¦\x0012ë\x001aåü££\ÎÒ\x0011ôÜN)êu\x0016\x001e\x0000\x000fwmmªxC´¸A\x001aÛÁ9½±ö2\x000fø\x0013_Eè:.£höt3j\x000cñÜ±G\x001eãÔ3\x0013É$þ5âß\x0004ü:cÖ#Õo£\x001b¼¶6ÊÝ³Áæ\x0006}Oµ{c(Ï&»°ôZWêp×¯\x001bò¤u§I¼3JÑÅ¦L¼L º[Oü%ÉXù#wð÷Èæ¸-NÓWðÏ%Úåí¤ÊÊ;1Àù]OÊÀÌr+ÐmüE.±cöKÈí¼ì%­êÆ\x00167õxÎ@Ï ýxâ ò¬õ\x000by4]q\x001aÎâ\x001d°G¿;­? /ÎèÆÖìNÓÔQB¼àùjl\x0018,*CåÏ
Iæi±¶!DÚ7³vÝ\x0012ÊGÏ\x001açø\x001ccåíFpEgj\x0004p²\i­8òË
?úÈ×£ õ(ÀqÔ~9¬:ÖçJ¼ºÆY7y\x0017Vòð	\x001d3qÃ\x000eGQ]Õm_Ix£f\x0008Úwqç\x000e>ä®á»»\x001eÆ¶y%Ì¶g\x0015:­Ã_\x0012Ø«c,7ÖW×1³Etñ\x0019\x0008\x000e%\x000cë·<îÆà?Úzì¯ím¯¦ýKybc·?»A9ÿ\x0000¾Er\x001e\x0019¹VÖà\x0012BVbÅ_\x000b\x0008ù¨É\x0019÷ú×dAeªAfª\x00129àÛ\x0010Ï\x0007Ëã\x001f\x000fò+¼\x001d9XôhVU£~½N\x001bÃÚ`EÔ\x0011±-â@Ê	"
·þ;Í^Ó4÷{\x0015\x0017-\x0015ö$}é\x00113³\x001fU \x001fcIáÙ\x0006¯K§Ï´Ç3½¹ÏRFvÅx«wB[}Yv³3«C)U\x001c¯±½ÍlÛwìa8¨8É\x0017¯nUüGlbV\x0013Å\x001eÖÈáÙHÇÓÄÔídV´º
6h£Ç\x0007x`	öÉqëo4ýÚÝÔh\x0006\x0011ÒB=8+ÈÕ=rÍ\x001aÂÚ7Ø&Q³i?yK.ì\x000eýE)®d«FOR<ûÅzzÏzÚPäKæCpWþz !Oü\x0008`ÖC´ÞÅ|±þîÊW¸*OðÂoà\/ç]Æ¨Eu éº|ð\x0002Qí\ò¯Õ\x000e=x\x0015ÉOhl¼?©´\x0012&-±þÑ³~]ñ\x0007*´]É¼\x0013\x0004fàe®äY\x001a7êLqÛàk¾[\x0015Ó­¯.âù'xÖÚÝºìE\x001b#ü3¹ÿ\x0000\x001açü\x001dáö}$ïâ\x001fj\x000c\x001f¾¨7\x000fnYá[>/¿\x0013ªX[³!X1|¬ÿ\x0000`>æN\x001cõ,~5yi®\x001bifñÆßg,Q \x001c´kÂ/Õºÿ\x0000À«ÐaifYí2©\x001b±Æì\x0012\x0007Ðssn¤U\x00173 V9tö'îî\x0007ó¬ë£=õÿ\x0000\x0006%bØó\x0001ùTz'©õnµ¼PÈåøbêOvpúÝ¤×ÍÄ«3!·Ú	'\x0008\x0001åôõÍuzzlÒéãmÀm¶,{1\x0007\x0001üÏ=\x0005trév	j//
J«¨\x001be#¦}@ôªZ}å³ÝÍtåå¸8xã8Þäð0;\x000fONMiíï\x001b-ÏõkÉ7¿õ©\x00041xR\x0016Ôõ\x0015kÍnë÷vÖêrîç°÷9É=ë
¾Sí\x0013Í$7ºôä¥À\x0007÷q\x0005ë\x001eî\x001aÿ\x0000\x0017©ãØëjd÷7k<e\x0017Rpcô|ÆÑ\x0008ÿ\x0000W\x0008þñé©=As\x0006¦Ú[i©oþÇ\x0011Z'-9\x001dYÏR3É=\x000fAàs»½$©ÇCOæÆkíFúGÓ.\©\x0018î5GSþ­r>K`y\x0003òÏ\x001bêwºî «q\x0014pCmû«;8ø\x0004è6¯L9ëú
õ\x001f\x0014K&¡¨C\x0004.0Q\x000cCrí\x001aÇ\x001eÙ\x001eýé³h°xy¾ßu\x0014W~*ò´´\x0000:[±èïêGnÃ¶zÖªÔõ{ÕÓ¡ËxwÂÚo4Ñâ\x000f\x001eÝ%µÑO2\x001b8úA\x0004\x0011ÀÎC\x001eFî0:\x0010rjßS³³mB\x0015Ð|.%?ÙÚT#2\·÷ÕO.Ç¼¯Àíï«u¥Á©Þ\x001bÙ±¬k%ò\x0012oÞ$RgøÇñw*ÞðûR\x001aÚÎµ\x0015Ýþ¤Ã]7íôHÔô\x0000gæà\x000eëKÔwJ\x0010 ´ÕÙGgq¦/ö}IÇ¢@qç>x{\x001cÈO\x0018^£VÕ<Gqj¦\x000b{8¢^c[£·ôûÜI\x001aþ[¯°è°\x0004r\x0004Gê­ß.{öØ£"·Ò´ÍÑ¿zËµL7\x0012Üq\x001a\x001c3ô¨uáMÝ\x0016èJ´m-\x000e.ê9í K\x0013x­7çdvá÷È?éc\x0019\x001fí7Ëîk\x000eãÆÑØJË¢´ÖÐ0ÃdãþºH[w¯
\x0000úÒjú\x0007{%÷õI,\x000c\Àí\x0017÷\x0003<\x0010â1ÈÇ¥aê\x001az«i^\x001dÑ`Óm\x001dt§ý"òR9\x001bå=:gj\x00009î*þ±&îcõXÅZ?yÜxkâ\x0016Ó¬z7V$yÎ¡\ÿ\x0000xWò?Î»ùeP²ÚÈÂü¬ÁÕ¾I\x0006¼V\x000f\x0002=IsâItÛsÈY	y?ë]¾¦º_
_¶ºÛáæÖÌÿ\x0000~òä	er;²ðüëHâUícysJ÷=:ËNù\x000f`Ê¶Ý WÏ^µ-4áb\x0016W<×ñÈª~\x001d
N\x0007¹½Zê&\x0002ê\x000bsæ\x0008¤ÆJüÐê4ýFÑ\x001cC\x0004/MÊ3ú÷ªuÙÔçúª÷ô(\hòÝ
\x0013©5T[Ansu.[ûò:Û×µ¾èçùO\x001b\x0001Æk'
:÷«¤å8Ýõy)ÊÉ\Ü´½	·cSß©5j{éÁçëX6¯ûÅ\x0015n{# rÂ«Ù«Êr+ÜÊæN\ÿ\x0000ßUbÉþ\gÖ²`ò\x0002ÙÆy\x0000à×U§-Ô¹³(àxüóEI¨-QThûMq1\x0018æªFeÈ\x001aFôQVÚiöÓ¹Ú^x\x000f\x000bõ5-£I¨[ºÛJ¨­ÌQ¯$c®zÒ¡Õ²ºFÑÃkfõ0æs\x0001Éìyæ«}Yd\x00028dr{\x0005<Öý´Vö÷Jð}¢êtä\x0005P«ÓÞ}â\x001bÈ'hþÊ0þ\x0017$Y·h£EUæÎvæ\x0019bSçFÑ2Íf³\x00159F+à[ú¶©&¡\x0008à\x0005
r6ð	õ5Î¾7\x0010Ä\x000c\x001eÕ¬\x001bkS¤T_ºÌ{BÒu¸6êúe¥àÁ\Ë\x0018Ü2;0Ã\x000fÀ×ëÿ\x0000\x0006t\x000bÂ[Lº¼Ó\x0010ââ1ôÜC\x000fÌ×¯L>LcµCic-ôÆ(Z%`»¿{ AÇëÒã\x0017¬§)­"|µâïºÞ\x001c\x0010Æº\x00192Ú\x0003\x001fí!\x0019\x0003ÜdW\x0000Pã{×Ýáó÷\x001eÌØ¹JóÏ\x0017ø#E¿¼=[L¶ûb<ð8SÓ#æC×¾}+ÒR~ã;IÁ~ñ\x001f*\x0010sÚ½*×à¿AëO¤hK0
\x0019Ôõ\x0008ãf\x0007¦\x0011K>}¶çÚ·µoºc9:v¥ul\x0008'dÑ¬?QU´\x000f\x0004k>\x0019×ìµ#U²{)Rh¾Ñ\x0013\x0005f\x001cà:ÞÕ¨ÍlkN½&ýædÉá\x000f\x0003é1\x0013®xí®®öF$ðRúVÿ\x0000\x001bàÌ"6ºÅ¦¼4ã\x0019+y©]p\c\x0000Ç\x0002\x0001çÇ\x0018¬Ý{ÀzÇ5ûÝ[R¿Ó£¹¾ºyåX\x0011ÊìX\x0007êxÏãZZ?Â«XFëÈ¯¯Ü®6¬l\x000f¯ËÉüê=Þú\x001b{h'î«£Ô,|3ð\x0006öãÈ´¸3ÊyØ²Ýp?.\x0005Gâ\x0004|(±ÒäºðÜLÚ¼xh\x0007+®r3ütÏ=zV-olà\x0010éÚ\x001dÔ1c\x001bb´q»ê@æ©êv·V\x0013ùwÖÓÛÈFåY£(HõçµmN¾äUÄ6¾\x0017o?øb×v¶7\x0012NÆçÖ»&àô®+ÂDÂA\x0016\x0006r+¾\x0008¾µèÃcÄ¨ýáÓÂ\x000eý£n\x0005Ê+\x0008¯b#­÷Z@;1¼{wÍZ´»ò+{{ù°aRZ1\x0010\x0001qüQ_þ½mÿ\x0000Â={ovntX¦ÂmÞG\x000cJ\x001e \x001eµ\x0006\x0005ÿ\x0000évEÁN¸Çû¬2GµeÈª#xâ\x001d\x0017¶­izÍe{\x0017«G\x0019c¿× äF[¿bé×ÔÒÒãÃUY\x0011Zhao\x000e\x0015«p}r\x0008õ\x001eõ¨ºy{{p½``Öò"^»3Ý}=+ª¹Ð­ï/¾Ù\x0014£,\x0014H§\x0004n\x0003ÿ\x0000{\x0018¨rö~ì¶fÕ½èîëOoSQcq\x000cd\x0003 ÷\x001fCõ§éöÂh\x000bí­um19\x0014òy$0ôàGô"µm-c¶·\x0010 ýØÈÁ9¦-¶.\x0005
\x0001ÎGñ\x00021Ír9ÝYF¹ßsñuÁr5$L²²ºzÈ:\x0013íýkFç\x0006[=R1\x000c?ì¾\x0003~D\x0003Z×Öës\x0003Û²ä\x0015È'±\x001d*¶l#Ó~Ë&\x0008RHúg"«ñ]Í%\x001dlj\x0003Ã×ãi%µ\x0017î\x00123Ü|éþ\x0007ò­µ`r;§w\x0017êÇ¦Ò1ïk:oW\x000cF´ÚG\x000b¥éÑ¼\x0017¥D8£<`\x001dÊ8ÿ\x0000¾ãF·\x0018¿]5-c\x0019Ô\x0003]°÷òÇ¯¶ãÍmC\x0000··`fI<÷\x0006L%«©k	\x000f,eí­#=òv®\x0001ì©ZÎç
IÙ\x0018ú<ÒË¦½ºË\x0011(]Ù\x0018Lç¯\x001954\x001a_ÚuÒ n·de\x0008\x0011Åñ~1ìk¥Ö56ñ¢ªÇ\x0016[§ ÀþtË8ÒÆÎIX`ãsAõþ¤×;«­ãÔïäw÷¶F7îä\x0000i¶ïq0ùN	çóéôÍFÚt¶q¬w\x0001w®Ö(1°w úÀ÷$ö«z<\x001fn¿kù\x0014*¯¨ûÍþ\x0003Ò§>«s°-c8\x000eyÜÞ¿Z|âù5Ïï?Ëjº¤Q4Ûy\x001a\x0010¡F>XÐ\x0003 ¼u«úlqhR®$\x0013ë\x0017?4c÷Kõè8þUÔÂ°Åb>ÄÑ$>x÷?Î°lôHL³]_9h\x0018îgÍß'Ñ}»õéjª³Ñ\x00138Ê\x0016åÕþ\x0008MBÿ\x0000íV¢ÓLG\x0016òf?52\x000b\x0003×iôõ=ë¸´¾»Ô\x001bL²{E[²p¡;*·8OR:ôç¥ww¯5ó\x0018\x0016ºZ\x000fÉÚ_Ðcú~~â9\x0005¾Éj\x001e\x0008\x0001\x001b¡Kt;+7U^z\x000eHÈâöÔn|ów¿õ¡Q\x001bLð­½¤ðÍ~Á£3\x0015Ï*9	ì;÷'\x0003¯N\x001aææ[û©Ôf&I¥vÃËê]¿@íÐ\x000eµ³má~ñZñ¥9À\x0011B<¸bUè Û\x001fÌíôÿ\x0000\x0005éZm©	m\x001c\x0019·\x000c ñzÔ\x000eäö§'N?\x0016¬Ò\x0012©m48Ý:ÊÏHµ¶ÕoÄ\\x0011öxí¢"âç\x001cÏÜ`\x0010\x000f^§\x001d+b
OV×VU\x0017\x0011XÚîùHX¯³H\x000eY½h\x001d7WF|<.®L×jN\x000bçæy1ÙÏ§\x001d\x0007\x001d*ö¡jfÑÁ¸`:¾;\x0011éø~uÉVN[\x001dÜcæÏ>×5}\x0007ÁÐ¹¼o
\x001c\x0019@y¾\\x000b çhõ-\Ä¾$ÕõX\x0004Út\x0007I´\x0014þñÚ'ÏhÂ.óôqþÕz^\x0015ÑVêY#Ó­ZåÈvXØrÀàýrkBM\x0016ÜLd\x0008\x0001n$lüòqÐ¿\W7±êÍ½ºêxEÃ$¿¹ûEÕýìVÇ"V4ûDò\x001eq\x001c`¶Ì}ö-ÜÒµî¿koo§øÃí¡ØF\x000bG5Ê&OÞbíÀcÜò{q^éo\x000cP[ªZE\x001cqòª®Ð3ô®Äº\x0004ºâ$ww\x0012\x0012±ÃêFA<öà\x001aÙE½\x001b3UÔ]Ò<_Hðýî¦"y\x000eµªÉ&	y\x0019!
~i\x000eIàt\x0019ô­ß\x0018è·ZN0Ô<E¦iF1iöQm\x0012\x001fL¹½3}+ª·ðµÒ$öÈ¢Ùâl¹_ß,\x0000|Ì1¼gð¯9ñW®tk¨Þþi.\x0016Vù¤2¹\x0019ç¨ô<\x000cýM\x0013¥ªiè(âouoëÔç<%¯j~\x001eÔ-fÓµ(íÒá±<\x00049>@Ë¢¯§ ¨=?
÷-\x001fÆZ>¡4Q\jº\x001bÞKÂ*LRF=\x00067*^a}§Xh¶bé<1yu\x0011#ÊU¸Úã<C\x001e\x0001üIªºÝ÷+ÚÙýJ=î4¨"TØGñ\x0018÷:ñ×&´ìEJi§Î{½í¬ò\x0013Ëcû¤\x001aÄ¼¶,EQÜ©¯ øaâo\x0016ý¦=\x0012ÎÉuÈDDÂ·2\x0018ÞÝ@\x0000f\\x001fÝo^\x000fA]üM¬xJløm2T\x0001 ÓZT\x0011ÉÉ26\x0019qì¼ì[hÙãO\x000cïî¦u\x0016$y\x0015ôøf\x0003ñ®6ÓâoCfK¨ÈRHkr~jÓ²×ôÍl3éö÷<\x0006(ó®zåN\x0008­\x0014Óz3)RW¼ÑJ\x001aB7tü+¢Ó$">\x0019`ägÊBPJXczéì^8­º^ê\x000fQN[\x0013O}
o&_\x0019ãÒ­i4\x0017HèÄ`þbªêQ\x000bk¡å6ø%_2&Îr§ú>¬ó\x0017,}\x0005\x001aJ%ûÔçètWÚÄ6ÊM¼`»rI\x001fç5©k\x0011ßÚ4sZ¨cdýßëS_ir0+\x001a¤}ÚI\x0002Õhôcp×:ªç ç®u\x001aqØëu*ÍldÝ\x0000#\x001b«<ÆX\x0017\x0019 \x001c\x0013á[Z)¶+³ÇÎ0Hÿ\x00009¥Ôu(nmÂÑ$·±È/°$9ëÏõ­\ØÆ\x0014Ó¿3±27ÉªööÐË+«¨­£^Iu.Oûª:þ8®GÓ ~âôï}¤\x0002JÍM6e`¦B\x000e\x001bÎR3Û8^j\x001dN°¢·¹YçÒì0X½ì¬½m©ÿ\x0000~×¨úçõ\x001b[+ h ±Â¾:ã¾+©;{;e¸kW¿¼<¤&&ò¢÷n>síÒ¹RîïQºy¯eyf=Kñ`;\x000fjPßCJå÷+ÇãT_'\x0007\x0015£z \x0011¸T_\x0007<ó[Üä&Óµ[­\x0017RúÁ."ÎÖe\x000c0A\x001d\x000f±­ù~'xVù#ÏLA\x001fõ\x0006¹\x0019Wå\x001b»{`U6 ° ôã¯jB/VtS«8«#¬¸øâÎ5R\x0007lC\x0018ÿ\x0000Ùkñ\x000e·¨k·\x000b>«t÷2¢ìRø\x0018\x001e\x000fSUfë9n»@?Êª¹fË\x0011géIB\x0011Ø©U©=\x0019¯à¿ù\x0018à\x0007<«
ô¯³¨?t\x001aç|\x001d¡hÑk\x0016ÓÃâ	¦(s\x000fÙ¥R\x000e9\x0019#µwÇLRO©X2ú3ÿ\x0000­#Z)\x0018TÃODiM«é:êf¸Ô´éÎ\x001d£ÈÏ]À¯Oåí[/m\x0006»¥5¤¤W7\x0011âd¹- ÐõÃ\x000eÇiÇÒªëZ4××ºbËûµ·fs&ì3\x0012\x000e\x0014v<ãöéW|9¥Ç¥ßJÂ\x0006I²XÄÄG!ë\x001fEn:åVR6§&ÿ\x0000wU\x001cÚY_CsåG\x00133¹]>hÜ\x001fâSß>Ýèöfd±-ØñéÎ¯$j\x0015\x0015UG@\x0006\x0005ISR¼ª+2éa9s Å\x0014QX\x001dBQZ(\x0002ºô¶NÛ\x0001úóRº¦»wz^´ÉåÒÅ\x0008ìQ¼`2²Øÿ\x0000«1[Ç\x0011%\x0017\x0019bçëS\x0001Z\x001c\x0014i¤åmÆO@=Iª´-s\x0002[¦Gãsz\x0001É5\x0015\x001bü£\x001eÿ\x0000J\x00165tRxÛKs°mÁìBôÏãÍ\x000fdJ¥¼måÚ\x0001Uà°ôÏ¿þ½h\x0005\x0003 \x00148éè(»\x0017)Vâ4\x0008î\x0010\x0000"UàßµT»"ÝjER\x0018¾eNXÛæ¯ÜL°Æ\x000b[<\x000cÖmæ%øV¨Àþ!Àü*áo´cRNö¬äµ¯\x0013]_®4«vEr¨î»Üÿ\x0000¸½2\x001aÎÒK\x000bx¦Õ....\x001cBçÌ`\x000fEô\x001fSØt®ª\x001d)#â "ã\x0006@?xG ?Â>r+\x0018!R\x0014	·;N9\õ"·x¥Ë\x0005c(aäß4Ùm}5Å\x000cÑ,m'"\x0008LcÑqË\x001e'Z6s!\x0012ÈÝ8;\x000fÍ#¼z\x000fÂ¦û:Û£}%ó\òÌV=MP¼ó\x0015\x0004W¤ÜåT\x0015E\x0000órÀW\x001cÝÎø¥k\x0013\jp\x0000ÑÅ*ù§¡R\x0018\x0003Th]Üñæ1ÁÏ\éHÐÄ¢(Ö2c\x000c\x0006ÔÊ¨ÉÇnMY±\x0012É\x000fÎ\x0012\x0001\x0011\x0014qÔ\x001fÀÓ^cv[\x0016b<\x0001ÿ\x0000}\x001cøÔ¨A\x001cr?:,jé»i\x0019\x0019ëé\x0008Õ\x0018\x0013óqÛ~ð08§SyÉ? \x0004`6\x0010@ sÒ«NÈ+÷yR\x0010\x0002sé%ºT¹KvBK®I8Æ:cüñP\x001bãº·É|2\x0012JGûµÇ@X\x000f§ãNÄ¶sÚ-ÛËw§ÚÃ\x001dÌ¹dk¥/1Éù	ç±ô®'Pð<6i-Åð¹\x0004\x000c¿Ø­öç=~s×¡ê7BÆvófxÙä
"ÂùÎ@\x0003\x0000ééO±-b\x0007à\I\x000bc"WÊ8\x00073üªog¡ªm«Èæt\x0019´ÿ\x0000\x0006x\x000e}f\x001b6[¬I\x001c3OºY»"ä¸Ë`\x000e2kÅ|uãÝKÅÊ÷\x0016\x0010¤Ê´$4©»dòF:ãÒ½sãUî¤ú.¦\x0010];Dª\x0010\x0000\x0017\x0007v\x001c'\x001c\x000c\x000esÔcz^k\x0004\x0017V\x0011K; yahn¤ñÜ|ÝF1æÄVqv:ðÔ`ãÏ'f|ç$ÓG<2Í f`§gA1x#¿½U¶KýFåaÓí®¥v\x0015aøë¹"¾­Ðü\x0011 A4ÑG¢i¿`?´¸ò°Àá
·M¸<íÆk¥\x0016zfg{\x0016¢Ò2\x0015Ú=¨\x001c $\\x0002z\x001fNÕÎë7­Í¤é­-sÇ<\x0007oã;\x0008ã\x0013@%Òf;c¸»Vx°¬~æ2ËòãæÃ\x0002{×sª^\x0012-´«%HÌò\x0018T1\x0019P@Sò±à0?ÐÓõÖ½{è&*cå|¡'q\x0004goC\x000fb\x0001<\x001cÔ\x001a]Ø{Ñ\x00126Ûw@\x0018;~ll`Ù\x0019Ü\x0008È\x0019ázqJYT¹S3WJOÄÌò<Y#È
iÑaA"»¹#8Ë°\x000bïÛ½[Ó ñR"Ë\x001e±cq#¡ÁÍR4o9\x001c¹+\x0014cqî\x00009éôéâ\x0015e&ÁWVR¡GAò¸éÔ\x001eV½´*\x0019\x000b`îÀ q;c§ÿ\x0000®£ëµ¥¼\x001e68Kñpe¼ÊñØ ÁÌJ7wÎI8ÈíëR[ÞêÐÏ(GY#C<±Üí^¤q¹\x0001=\x000f×Óô!%cc\x0003-èqÉëì\x0005%´ziQ\x001aDÈ\x0001à3p{qÍm\x001ceH+ó\x001có¡FzÊ\x0007j\x001a×¶]6Péþ°¬«µWÕIÆî1Ðzú\x001a]^ÛÆÏ¦áXGÁ\x000fd\x0003Óå÷98\x001cW[¨iê\x0011H\x0008òb%;õÈÁ,{ð\x0000\x0003¥dL\x0003Î\x000c©½QCÁ°ÙÎ\x000f\x001b³\x001e¸\x0019\x0015³*Ý\x0019­<·\x000f%~_Ä«mâ-VÇí[i\x0016$Ció.2¤¸$\x0003Æyã =j	¾#xmüØ´Fm¡¼¸ÜîïÈô\x0019\x0003½]³"]Ec\°$gqc÷³ÎFHç×¯k¢K}#[Yü»ÈØîØ)I$c9ä\x001fÄÖ/\x001dVO}N¥¥Mm¢ O¾!¸\x000e±ÚÛÅ(:Æ\x001bs³\x0013÷@ÛÀb\x001b88=+>}}.¤}OÃöÏ+3+ÉbóY@ÜW#\x0007\x001d	Æ3ÀÍjê~\x0015ºÒ¤ód\x001bH¹d;³ß©ç\x0000\x0000\x0007Ö³Z8\x0005à|EæB@YNôBI\x0019ÇO-ô\x0007½DñÕ ìÝpÂQ¨®hÅ¾Óo.ç?ÙÐÅo\x0014êEË<P ¹\x0014\x0003×*èwñ1ÞÖûÐcedVÈ8RÄñÿ\x0000ëã¥wL¾XFÚx} ãôÏaút=¨}Ãîfo0î18lõ\x0005Iô-È
o1¬Õ¹Y}\x0014ïÊr\x001aoçy­ïdi$eÌf1³iÆH=IíÛ\x00078ã\x0015uô[)µ1\x001c¶â5\x0016P¸Ç¹
£\x000bÐ\x0006Ï^Ãêk¢··1Ê^e,±\x0003\x0013Ëcäç'¹úVx6×\x000f!\x0019i#UT\x00048\x0011«\x0010I\x001cá?¯^k\x0019c+=\T¤QÊxßìºOîîfÞÕ6DtS¹Ø`à\x0002N@Ç\x001e½\x0000çæËzóûZk»Ë¯µ6\x0015ß$·pqÒ½¯ã¡
è\x0007\x0016Rrê½$È\x001c\x0003Ó\x0003`r}«Åô\x0008êÚÝ©ºÓ­\x001eíY\x001d§\x001bB\x0012Iàc®+ÑÀ9UÅ<*Z#©Ðþ!>'Ú	®\x0017"6#
2:°\x0007§½I?õMRSss5ÌÜ\x0003\x0006=\x0000\x001d\x0007µrIá=nÖ@·µd_hÿ\x0000xsÈëR²²\x001dLYWØ<×Mu'esÌx*Nk©úA1~aò¤d\x001a\x001b5]Ð»ª\x0013Ìdå\x000cô«bè\x001d»¢(((¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000)\x000fJZ(\x0002\x0001\x0002yñìO8©-\x0014\x0012[	÷ g'¦)h ¢9#Þ¤\x0016`\x000f¥Fð# \x0010\x000f\x001d@éV( 
ïm\x0019L*\x000e8\x0004d¶ò:\x0000\x001cpA\x0004g}jÝ\x0014\x0000Ò 2;Ó¨¢\x0018îª2ä(êI8¨7ls/î\x0000\x0011ªç^9þch,\x001b\x0003=z^\x0007&+]£Mfê­±Ùp\x001b\x0004\x0015Ï·ZË]"îX\x0002\_8\x0003\x0000*ò6GBHÁÏ­nõ\x001c~u\x0017\x0001ó´äM13o\x000fØC(&Ú{
ýö'húÅmiÁü£æD*ü¨ª»p¢¬!f<«s×µ9\x0014ª\x0005$¶\x00062i\x000eç\x001aÖ©¨|L{.-ÈÓìv,\x0002BÒ\x0002ì\x000eö\`\x000c\x0002\x00079«ú0ùò¼ç|`	D{qd\x001dÄîôÀÇ­EáØíÄÞ#ºK\x001eæG\x001e(Îã\x001a*¤u9'\x001eÕyÌ"îHË\x000c¯ÌF9;OÓ\x0007óæ¼ìJÖçL[ON¥swik\x0016\x0002HZ5x¹rHÆ\x000e8õàý+Õ¯f,QÚ\x0016çV\x0016ªÒya@'v	È`\x0000\ãìµ8ÂÀ÷	`·\x000e\x0011°c©9\x001d±íÏ\x0019®.è¹¹{+\x001bvy\x0015fx&mÀ\x0001´8ÉÁúç$àªÜt;°©KT§dúF¢-NS\x0013ÎÒÆOß\x0000eÇ\x001d=2@=»Ôþ\x0016Kè¡·\x001aB3\x001d¾c¤¥dØ\x0000ÀOË#×$\x0012NMtR]^Â\x0019H®¡òÜþù\x001aN\x00060yç> ó>µf\x001dJöÕY\x0016èÇåUUX÷÷\x0007;\x0011X(«Ý³ªUeËÊ¢¾òì\x0017³E(x7v\x0018pzõãðúÕÈ'yb\x0000Û&æàY_Úä7P8ÀP?\x0011\x000f~;Uøo§pvÜ+åw.Ñ×\x0007ÕÐ¦³¥7½ZHÌù\x000f¯\x001dý³YV4tgØÁI*á{îGå[7\x0017rðÒí
×=@þ<ñ\x0018üß6Þ¼ÿ\x0000ëúÔM¥±¥\x001efµ-iv\x0016wbæUy\x00036c\x0007hÆx\x0004\x001fl~9©_@·µ\x000böK\x0015\x000c\x000c=Ãqp}ë½\x000cLK\x0010HÁèpO<úqÏ±ªöºýßîçÊ*LlÆ\x000c\x0000\x000f©ÎM/kNÖ5\x001e¤µ¾F¬×[=>Þ2tùr¹$ð\x0007RH©§V8ç±ÓmrwFªH\x0007¸\x0019ÉõÇzÀiYî&Ë\x0015;ÇÞu\x0004ã\x0019À<})e·$ù`\x0003\x0008ßæSíéÁ9<qXªÔÙá·ü?êtÖÞ"Ô`ÿ\x0000´ô¦U^^(?È?¯8ÕU?´î.\x0004&\x000f´HÒ$y
	!'ýØì=*Ù¾Ô Ç\x001dÝÀÌ *«´c#gwStÆzV}Ö£ªÛÃö¤#BãÎ`J¤u^AíÜÕ½µÐÒ\x001fc'$¤ÂòMÒ,\x000b&6Ê³,Ùíp¸Ç=O\x0015¿g:K
ºcÊc¸îR\x0001\x0018ôük"ÏJ¼Ô¡öÑ\x0017Ê7!8\x000cF\x000f\x000bÜw<~5jÒ}\x001eÂªw½\x0001\x0003\x0018öê>¹ö¢1äZ¹)»"Ö¤âÞÎ\\x0016HÈSÜb¨Å\x001a¶\x0014DÒM+0?)P\x0002ëëo­YÔäÍýÊR\x0018JóïTté
Y©6QY\x0019ýàÆA^ø\mÅCv¸nÑá\x001e%>\(\x0018\x0002É\x0019\x000cF3îÃ×õßz4v¿\x0006,¥ciï¼ÙõÃP}\x0000\x0003ù×|q,bå}¬ï!
	\x0000ð:1ÙÏpkè_\x0010\x001b\x001cIÀ\x0019³/ò\x0003÷X³\x000fÇ\x0007ó¯£Éõ£så8-(¥ÔðoÊF¬_\x0019Bý9?áßëÞ¼½åXÈV88í^Ïñ1tK\x0017[ÉâdÔÎÑ±ò´æA+88B|Á·¦rzã\x0015Å]j
#£i~0b8É½~q[ÕÖGÃ:´ÓºûÏ¾(¢Ðõ( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002*A\x0019\x0006ÒwÇ4\x0000c\x0000)qÅ\x0014P\x0001HùÚp2})j·2[é7rK·`²	\x001f0ÇA9=\x000741¥wcð¤\x00170êzü´SÏ:3\x00136ðß Á\x001e\x001ccÚ ÕoÖÞIÚ\x00049âBq·9\x001c\x0001éÏäs\ßÂ	fO\x000e^HË![¦\x000b6[\x0007ÉêxéRëF¼»p¨72FÂPÄóç\x0007 \x0002p¸\x0004x\x0006¼:õoª=xaíYÆDºnÏ¶wÚ\x0015¸L\x0014@
\x0018ç\x0004ýãÁÈ\x001dEB/.³\x000ef\x0013)\x0019\x0001R	ÆÜ`®pO<|Â¹v¼y£i,²òÑ89ÁéûF\x0006OÓ\x001d
ì¶ß*m[È¶Â\aA$À\x000c.sÉÁÀÇ5Ãí\x001c·=\x001fc\x0008i\x0014X±·½(É ó
Lå1é¼à\x0001é}*õÝÚÏ*\x001biC&Fõp`Àr§\x001dG\x0019\x0007®+>\x0019.#òÃ)ISj°øÁ=89÷üñÖ¤»[ÿ\x0000&2DÛ.\x0017z²:\x00103×\x0019ÿ\x0000
9´Ñ\x0019¸Kt[ÙåvY\x001d".\x0000&c³#¾\x00068è8àòy­k{K§÷¶ÎË\x0015ppN0~¸üóX2\x0018åmÆi|Ì1%U°F9ëÀ5ÒiÚ¤&Ø5ÂF&'ø"è:dþ5­\x000eGñ¸i\x001f]\x0011]Ú_yr\x0014³î\çÓü+2Gi\x001br¯ÈpÃ\x001cs×±ö?¥t\x001fÚVÈø äÿ\x0000v!ÏëPÍ{g$\x0012DÐÊ\x001dFØÔ\x001fÃVÓ§\x0006½ÖaN¬ã¼N^þF\x0010ìSÚÙ\x000bÜñòçÔ?Éª7ÒíÞæ6\x0005²\x0002¶9#q\x0000\x0001ÆqÞõ¡©ÊÂ@\x001aHnrûGCè;ÿ\x0000Z§w\x0000`»\x0004ôÜFÜ\x0010\x0007\x0018ükG«Mè*Å¾&\x0000»K"!'÷\x0004ð8ã=\x0005U¾G:;D\x0015K!À>_Q\x001b¾½ªíÙHVufRóÂnûÇ\x0000\x000fô¬ëi¤÷»$S\x000bE\x0007¹<ãõíYÞÚ\x001aÚúZÇö\x0015\x0002*YNv¡èsÄzu+÷¦ê*\x0016ábTX"fgç{\x0012H\x0000å½=\x0008«pä\x0005lvÑ¶ß5K\x000có\x0007$8\x001c\x000cñëUî\x0007)*ÊQy
çå\x0018è:ëÉú{!Zåh.®-VEa²F\x000eÈ¥¶¶p7\x001fÏô©Vl\x0006\x0000áå\x0003åÝ» 
¼c¨Ï8ãëU.ÖC&Ì¡iYÎår¥So\x0018õa1øÕxA_1BýHÎd\x001dH\x0007hî8àçëíY¹¹\x0016 :7."Û**:`à÷ãÒ©G6-Ä\x000bæJoðsÆÒ\x000f ätïô¨\x001dTY(ÉläàIèH\x001cã88«a\x0008y¸åYví,Ä\x0010\x0006\x0006z\x0003×½RdÊIXðï\x0008\x001aÕW÷·$o\x000c@\2\x0006^µôÂì\x000f~\x0018Ã\x0006\x0003KØ\x0015ó\x0017Çv	©\x0018¼\x0011\x000bìdR\x001c\x0010GÝÛÓ±úõ¯eý|Y\x0016µà?ìkC^é\x000ccÙ¡c?@r¿¯©Ê\x0017-\x001b\x001f%ÄÔåì1ø÷\x0004¿ðGqËE° g	À>øèxãÕá\x0017$2OÞ5ö7Å(ü/&¬j>\x001b7·R\x0003å+êò[yÍì\x0018\x0018Ýø×êZÿ\x0000Ã>úk[ß\x0017°ÜFØt[\x0010~kiTµF­©Ëá%\x001a*wM3ï:+\x0005uÄá^N;
}¾®%-EQÜõ­yMÓmÚÆÝ\x0015m¨yÒ°\x001fpuvâ¯$èÀ|ÀgÖV%¢sÈ¢
(¢
(¢
(£4\x0000Pi¬ê¼±\x0000{Ôw%´3ómÈ Ñp%'\x001dH¦´±¯WQõ5ÄêóÇ÷÷\x0002>¼Ö\x0005Þ©*§ÌÜûÑt>Vz^Ú¯Þ¸ÀÅFu+0Û~Ó\x0016z}êñù5RÌ\x0003»*eº+[Åº|ºUWö\x0006æÂL\x000f0c*ONÿ\x0000®¢ý=\x0015õ­9~õÜ_FÞ ÒÇ[Ø¿Zð{ÝojþíÈe\x001f0ÍPþÛ\x000cyc·¾ãRä©6}\x0000þ*ÑÓx¹\x001eÇúUy<g¢ÆÄ5ËdzFßá^¯j\x001e\x0016Õ|1&©c<:mýºd[\x000b½±Âmþ,ö#ñ¯)ºÖ\x0018e²\x0008=Å\x000eh¨Ð>³ñu7a\x0018ô2)P\x0013[\x0017Wb+6¸).T
Áa*K\x000fl
|s.¿(Rw\x0015\x0000ñÍtZ_µ;]\x001aDþâÞ'R[dÈ#ôúÖR®¢Í\x0016\x0016ësÜ[âvc\x0012%½ë!ÿ\x0000e\x0001\x001fê¡'Åí HR;\x001bæ#þ¹ãÕóÍ×ôaP÷p\x0000ÆÑÔsÚ²¿á1ÒmÆæ-¿0ÚN;Ô{yv-a£ÕJ¿Åû\x0006`#Ó.[|Ò(ç\x001fD~0Ø	ÕN1R¥¸OOÓð¯\x0017Ç\x001a0f;ï\x0010Hò»ãþ\x0013m!\x0000\x0002D*ªÉ,øT:Õ:"Ö\x001eV}L¿\x00164³\x0018caz\x0006qÁBhiß\x0011ôkÛÛxcóV)¸\x0012¸ÆÓÓ\x000c:­|þ;Ó7BËpdî\x0004vã\x0015«á\x0018i
\x0000·3+NÓ0\x0003\x0004±SÎ};â¥â*-Z4XJRÑ3íaX^6ºÓÃ\x001aÅæ§ë·8ÉÚqÏjå~\x0017xÀ_øEÖí¼Ë>O³n\x0007>b\x0011Ûñ^\x000fºæ¾8ëû¼3\x001e\x001btWV¬Ê\x0007\x0004\x001eÏ±\x0003­tT«\x0015MÈå¡¬ ûü.ºsáK	Íº(*vÛÕOr\x000fo¥k^H·m¶áÕæ\x000bâ]Ì¥S\x0000m\x0019#,yÏ@\x000f5Á|9øuá½.
:kh®­A%\x0014¹äà÷\x001dzÆ»è|cà\x0011@MÙ:mÃ)`íû¢3üJËÆxë^\x0004g\x0019ÆÜÚùE¡ZW7Mò÷Z¼;u\x0003é7\x00176±¬NBì ¸c6`¨\x001d¬k{«VÝ,ÊbG*w\x0010eq½×\x000b´ô=ÇLq\ïÄ½R\x000f\x000bÛèº\x0006pWa:P\x0003!f>^GcÁ'ç\Î«\j²ÛÛ,ðZ¼c½ÌÂ5\x0005NGÎyÎw\x0001õük*q´l]\x000c,§\x0007[£üg³ÒñÄßkÓùf5ËmtVbp\x0007=ð\x0000ÿ\x0000d}+~ê	&Ó-à¶Ù3Æ\x00197\x00121g=z\x000f¯5ãZÔ^ ²Ì<Îd`Ó[þú7Rr\x0006äbBç¿\x001fsIâÉ\x0019\x0014°\x000b\x001b\x001c\x0005QÀ\x0003\x001e½~´ý¿"³\x000b.gÍ\x0019§oê{¤Zf¡\x0014 ËbF\x0014.P\x0004\x001cóÝPs×Ñr°\x0006ÆX¤QÏÈp\x001fé^\x000b ø¦Iõ»%õ­-L¥\x001aRÌB\x0003»ÈÏ${sV·¼Iâ-\x0007Vm*úâVE0®\x001fdÈx\x000c¼\x001cäiF¤m~W÷®_WEÉ_æKQI\x0019WvÕ,Îz`ã¤äRµÜH¨ÅÈTV
\x001e\x0001\x0000ýzñÓß5â\x001fðÎÐ§J>YJ»ä/ÍÉ\x0007¹âµ4\x001dcÄ\x0017-&©¤XOu\x0015³a8\x001e¸Ûßèzö¨u]ìÑýã\x000eihzTº´Ì²F6:ðNF\x0001\x0019çðïEµíªÜ óÌ@6Öf\x0004\x0019ë®\x0007°ÍsZOmÊíñ\x0006¦n\x0011Ö4\x0003\x0014®prÍÉÚ§\x001bGrzp+\x001açÅ¾\x001c¸µK
6öÂõÈVçÍ9Ï;¹ü\x0000¥UÙsE\x001a¬ß$ ýUFÖ­&IÕ®\x0002<\x0019ó"\x0000GN
u\x001dk¿¹´´(\x0013\x000b\x0012¦â¤|½~ñ\x001d[¾GøWCá}KPøxeZÞ<Î&\x0007;Ô§\x0000¡'\x0018o¼x#\x0007½y'Ä)®4ûÿ\x0000ßØj6{nK]TÊ£epz\x001ek9ÂvM-Ç«RT[WÒ:§× ò#óîüù\x000e\x0014R©\x0001Èî\x0000 \x001e9¨Nµ\x0002¾fÌ0åAl\x001d\x0006=Àè0\x0005xÝÖ·0	\x001c/\x0007\x0018\x0004òq;{~5SûnxÜà¶áÆ3Ðzgò«T*=OBY}ºPéþ\x0019´×tèî´­^	g(\x000eÎªä\x0003Î?!\Åß|E¡©7\x0016\x0012^D¬\x0002=\x0012l\x0018%Î	íÆ¼\x0005|Ey\x000c«$\x0017\x000f\x0004«®C.9àWoá¯*ÒJ¥ÅÒ_À8	t»ýô0ß®¥^ò³ò8'ÄÁ¿g%%ÙèwO¯Cló#ü¥	WÜ6\x001c88é×¥3Qñm²ZÛ y
´xdàã\x0007å\x0003vç\x0004\x001aó\x000f\x001exòãÅZ«ßµ¼6¬Ñ,F8É ãø8Éç¿jæ5\x001dZv\1
æ%ù÷G c©ê}MDpón×5úSÑ>*êÑjZøKco÷¸nH\x0007\x001d2\x0000Á=êïìõâá\x0016fF\x0002ÖýZÒ|ú7*}¾`¼ýkÕÝR]·1=MS³¸Öê\x0019áb²ÄáÕb\x000ekèð±öpK±ñ¹\x0015IÊ\x000cú#ãî³\x0005üP¤jk\x000c:A\x0018\x001f_Ó\x0015àz¾¥{q\x001bß]K;Å\x0018\x001aVÉ\x0008:\x000cþ5Ûx²ðêv\x0010Üny\x0019ÓxÀãNEp2\x0015-Ï'Ú­ËW<¼%7Ar¦~j7\x0010iZgÙ"!åpíìF	ÿ\x0000
ç\x0016ã\x000c9Àô=«2YËmÁ'µX5û\x000c÷7\x0012\x0014ÁÛ\x0012ã=ÿ\x0000
Jg®©Ø×ûhÂªÔW²1\x00185ËAv£9À÷­\x000b+ÈxÄ¤Ë
ØôÏ4sì!ºËV;ç®8&´âºekÕ5´\x000b<-ºciéþ\x0015R
TÄsI8ç¥.c7\x000b«³»óP\x0010§ä\x001eÊÛjs`\x001fJ5fvÀo¹õ¦¤c-6:\ÑXË©¨êAç\x0015n\x000bµ@Ü´Ìùõ±t°\x001dMW¸»X9`H=ë3R¿òZD\x0007%\x000fê9¬µ!s\x001b#\x001fqÍ
ê;××(ÌoþíFº²i³¬P\x0019\x001e8ÉbN\x0000\x001fç5Ê]ÝêØ"¥²ñ\x000c\x0016ú]ü\x0012ûDë±\x0019G\x0018Æ9>Ù5
\x001bSfUÕôÁWp\x000fj òýªÚíå\x0013
\x0005F3U{é\x000f¹ÏC×5.¡=¬rF\x0002È0O­K\%\x001bÝÓÀ2Å#KsÍXÑemVúÓH¿ÕdGw%Â8À8Êõàe±Î1üë»{rÙ$ç­A¤é®»~ðh¶Ò\¼cy
@\x0000zHëRôFù/ü\x001fuáW\x0012¡{6VÂOTÿ\x0000uýý\x000fCúWÜ^¡v,Üöÿ\x0000ëWQ®|B×­|;?ïÖ3±Äryè|Ô
Àìü\x0008î+Ï®5H¥?½:\x000f\x0007ü))\§tµ,\ßI¹8\x0019Ï"³¦¿`§.H54g¹â\x0006v¸'
äú\x000cu&µ|{àm[ÂÐiSÝK\x0015ÌZ\x001ejù`,à\x0012¤\x001er7\x000ehm\x000e2g!=è-Ç\x0003½hø¯S{_\x000cË\x001c\x0004ðªéÁ\x0015Í_\x0016I6I\x0003p3V<a3Iáè[\x001c®@>Ïµgdä\x001b|<\x0016Îi»=ª>ô­\x0006Üç½vØó\x0014âH¯tðÀdñí5\x000cø¦ÂëSxÏc"m\x0010·÷\x000b\x0002H#\x001d×\x0007±Ç5á Ö¦®êZ\x001dìwzUìö1ýÙ!r=²*dB©¸í#KÆ~	ñ\x000f¯>Íâ\x001d2âÌB;\x000cÆÿ\x0000î¸ÊÀÖ
ÃZÞC:\x001f7\x000c0}
zG>4xÆ\x001e\x000e_\x000fkÎx|Åî<JÅzr\x000eÑõ\x0000\x001f×>`>õ\x000bU©R´dYõ\x000fÁ­G#Ä±\x0007>Q·e\ã\x0007{\x000fÃï\x000fÎ¨üOÕ_ÙÃ³*¯Ê7d <\x0007¡=}køI©¼Wú´q:ªOaÈn¥©\x001fÌÔ^8¸i\x0016VfÎSîíÔþ9¯6Q÷,Ïvª¤R·¼Å¬\x0007Ì\x0000á²	è?ÎJÏVÏS´¡\x0013E\x001cêï\x000eìy\x000epN;?¥z·Ãß\x000bxçÁP_|>¸6ÚÅ´Jfµ¸±fÇ!³÷I=\x0018|§ùxÜsi÷²Ás\x001bGs\x000b2HyF\x0004§\x001d9\x0006¸\x001dEÜúZ8Êxâ´kt÷:\x0016øO\x0010øïZ¼UîY]"gÎÄ\x0003
¹úwõÏ\x0015oUÉ|¬ßxàm\x001eÃ¿~+\x0000Ü»¸O9ííÒel(ÉÆx\x0000ÇÊR»»6¦á\x0018¨Çdv\x001aOu-\x001af}&ökIN2aÿ\x0000\x0002_º}zWS¨xoRñ\x0016ÿ\x0000	4×ãS¼S9¢©x(\x0018\x0005ÀÝòç§ë^]m9`¤2\x000f=ñ^Û{¢ëáõí
Äk§ØL.\x001c­ ?wø\x0004Ör¤ùZG5z£85däíÐä~\x001eÇáöñ!Æms
´±þâ@Jª¿bÄ\x000e\x0006?\x000cõ®ïâ\x0007Âín}.ÖçÃ\x001a×4»HÛìÖí.%\x000f$#\x0003\x001c\x000e8é^!©j\x0011G\x0005Ì"ÂÍ´·ÞÉ<ÿ\x0000J½áß>#ð»4Z6¥q\x0005»\x0018¶«§N¡[ \x001f~µµ(+{Èu:¼Ê­)ÛÉê¿à\x0014-çhÑáeY\x000er\x001b=>µ×ø7Æúç.çÒC\x001aîýýÄ)p1È?29Æ
yäÝÕ½Új\x0008äÞ	<Ñ#Ç~IÝõÏ?Z[ÿ\x0000\x0011>£4OxäH¤[nÎ\x0007\ûç&«ØKâ´±4&½kZÝO¢\x001fÇ¾\x0003ñ8ñv4ýEW"î\x0010NHéQ»ð`ExÅÜq^Ì,äv\x001dNËdÉÁÇ©\x001dk\x0000\\x0016\x0019VÈö4)Ýýj].o¬%:xkû&ìú_Eèvú\x001f5]\x0011ÃéóÛ±;\x0006!Iõ+Óô®ãþ\x0017íÞu§ëºU¢% wù\x0006HêË\x0008úb¼E¦ì=1Q´wz!KDV"\x001e³RSk¯_¼³4ÄMU.sÔÇ5\x001b5m\x0018Xî=\x0019\x001d(Wã¨Ç¥@I¥\x000c1ZrÞ×[¹à`c4Ë÷]Ü.ÕÚ0­ôÿ\x0000&ª³\x0006\x000e
2r¸%\x0001\x0003\x0003¿|S52«^éúe\Õ\x0010y\x0015bðüøàÕ~õéAh|V&\Õ\x001b;=\x0012µx{Èb?wº2OaÔ?ç\½Âæu\x0018À5ÃW\x001b'\x0006<H¹\x0004úþ¶i×Lä¶ò{í\x001cT½\x0019ÇnY\x001fux¢}bsn\x0015\x0010\x001d¼`\x0002GSXsÉò0,H\x001d9éM¾»\x0002CódôúÕ6)\ÊG¯Éb\x001f1Ñ¾ÿ\x0000\x0006®Ãr\x0000^zöª\x000f\x000e@lñõ 1aÚ´¹-\ÙûNÐ\x000f$\x001fÎºþ"y=\x0005Sr¤	\x0006BåWéYÝ´®Q\x0018`rXÐ¤Dé½ßü¸SSV`½Âç95ÉÅp\x001aS%\x0007zºnJ\x000c\x000cî\x001c\x0001þîa(t:#¨að\x0018\x00008æ­Ã­Éhþtd\x0016\x001caºs\Ë¢Ëþ9=OÈjYá¼1ãìóg?ÝéÅZf\x0012¦ÓÐßRkÜå\x001aËkÆ^¼
Î³ûZÝ\x0004zb¢»ûH90¹
Ó#E;¡{'sFúèK\x0016å8`+\x0012{¸<ÓZKäÛ$L\x0001éÎ¿\x0013+nT|\x001föx\x0014s\x0017\x0008YØ³6 ÈJÉ¸ã±¬­BO0\x0017Cÿ\x0000\x0001&©Z^Ø´gP·\x0006wGæ!\x001b¯5²Kæe+×Ö¦OC¢\x0010mïa>^Iä®x\x001d\x0005wÿ\x0000\x0000nãÄ¶¥²nmøÏª¶\x001aØøËkkqáÍ'Xµ#YFJ>VPÊ?\x000c\x001añß\x000eë×>\x001cñ\x0005®§eð¾JC©\x0004\x0010~ þum3t£êt?´Fö\x001f\x001cM2\x0016ò\x0014cq´ÍkÆn'ÆFxý:×{ñ?Æ^0Õ!»¼\x0018\x0016(¼¨â\x0014g'$õ9æ¼ÚäFÎÌr}û´_[m\x0012fïu·Ð<I¦ê\x0003µ¬é&ÆèÃw?Ïóí^ñûM¬¯4/\x0011éwAôô|m\x001dq*¯ú`zùwÏ1ç\x0007wnÂ­ê>$Ôî´ht¹¯î[NùÛ\x00197¨\x001d3É¨³ØÒ*-©v*KªÜt¬¸çç\x0019ü+©ñ}µ²x\x0016\x0006#/e+Û#áÒ\x0011,\x0012Köu(\x000fÈï?AÞ¶u­Iæð­³m$àñØ\x0003üèq|Ñ±IÅB^\x001aÊ¹ù\x001b?^)¬¤dñji\x0014\x000c®ãÇ
;ÓZG
 <\x0000((Áí9\x001dF:P2lÄaÏÌ%\x0007\x0018\x0003S	ÉW+Ïài¨Ç
¤ç«±éì1öiUO÷ÆÑù­'dR»èz'Ã+§þÛ¸t#V²*UF\x0000\x0019_ëNñ{43\x001f¹^}½?:¯à(!°¿}STÓ-#h\x000cxä\x0013\x000e\x00179éV5¼5$²}§Ä±\x001cæÒÒI\x000cØ6Ð>¹üëpocÙXGVÌ¯\x000eëºp·Z]ÜÖ·\x0000`<LTãð¨..'¿ºIYæ¸Ë»\x001fäSM¾ñ'­`h4m\x0016{à-Ö£pK}Di\x001fBZ±/¼Qª]§'\x0016Ðd\x0015²\x0008zð ~´\x0019·s²YÍ(/u]ïgq\x000b+\*@\x000f Ná?Bi¥­Ê½õz|¥ù\x000cW\x0012ew}Ò1ry$µØxsÇ+¢Øµ²økÃw©òÌË'æ[Â©átÜÆ9Ü¶±Óè\x001a\x000cºoÓ¤k ¸'ìð4¤ÀG?+éSû'àH³¿­Â\x000cî¬>sS®q_\x001cxF\x00195_\x0011iöP\Gi%ÕÊD³\x0012Ub,À\x0006Èä\x0001÷ï\x001dAáËíFËÆ·Ú¾²<	íî\x0012Þ92
ÁÛ¨*A\x000bß½qU§*MÛ[ètÔÄýoïg¸ñ½^]>\x001b\x0004ZËà4,¹üûV<ón`\x0011£e j¯s\x000c³¹òZ\x0000ÇûÛçUmH]Pá£cò·P+¦\x001eÑ¸êæù\x001eÆó"É\x0010\x000e\x0001\x0004tôª3X)\x0004ÂvÙº~usp>¹4Çp\x0017,@QÜÖqÐô«Ò¥R>ÿ\x0000Þb³ÜZI·%}³Á«Pêc\x0000Ì¸ÿ\x0000hU=Rñ'!b\x0019ÛüUZØ,­±Û\x000cz\x0013ë]¾ÍJ7>kër¡YÂ®¿\x0003¢ur\x0018{SÙ\x001cW> 	ARJú­j4äç$¶g­ÇN¢j¤lÑ1Þ½C»ÒÀ\x000e´¹M][\x0017ÉþÆlTm ¦oÉªQ0dL_I§HäÆ	 ½¿­@Çv1N-ÁÇ¯>´ìO´ÜÈ»ÎþMWïVnþ÷LUjìÇÌ×øÙ%´¦\x0019ãz£\x0003[w%L»\x001d¬7\x000c\x001e¹¬
Òµ¸\x001eJ)^\x0006Fx¥8ÜÅ£ìÕ$1a;\x001a¤K,»wg#ÓÔ5®à\x0011Hêî\x001b\x0013\x0007?ZÊbª7óã#ÚWAòJBÎÓì*'\x0012p}j¬óËdâ©Mw¸m^«Ö´æ3q/OvZ/+$¯·J®å0ÚH\x0007\x0015An\x001f\x0001z)ê)ÌXgúé¦>SN\x0019\x0019\x0017(7\x0011Î\x0001æ¤¼ÔÍ´?+´ÊOÌ\x000f*;ûÖKÈñ°Ëp¼Õë[k­.+obYTy~_ñ\x0001OJ¤õÔÍÂëB\x0018µ9]þy¥cþÓSÝ^þè
Ç9=ÍeÇ\x0014qÌ\x0014H	õ<múÕ&PZâ#øÙXâ9\+ò\x001cíàg¦i/oi1¾\x0018ÿ\x0000#Sÿ\x0000fBÌqy\x0002ãçNH·\x0011!:ªÏ,ØÇçïD§\x00145B{¶÷«ç#Þ·¼?s.¥y\x0014"G*>f9à(ëY2èñFÏ{\x0013*­Ú·4Û7Ñ´bð¤òôa	^BûV3¨­¡ÑN×cÒ¾*}ªk](é¢êf/³v\x0017h9útçé^M}¥j\x0011I$MØÆÆÆß¦85©/äÓt«\x0008¯OÚUBË¼ýÀOÝ\x001fJÄ\x0011\Ìª\x0012i\x000cG×éS¬¤\x001aynM¬Ý_jZ-¾u)þÁjCÇ\x000c°2\x0006Xrq^w\x0015ÐÎ\x001a\x0017\x001d7oÁ?t\x0012ø¢\x0007»{g\x001fgFâ²7\x001f­RÐ|Oig¬I#$\x001e[\x0005\x0012Æ\x0018dðN
h£mÆå\x0019%c¿³ºXØ*n9ÈÁ\x0018\x0015ÎÝ[Þ$<ÚÇ \Î½fêM!¢âãìé\x001ckÇó¯+ñ/!»L³\x000bpp\x001c®]½ý\x0007Ój7ØIAjf´2ä~éÉÿ\x0000p×¡ø_á6¡âO:Çí¯"V°.\x0005î"\x0007n{pÜ\x000c\x001cãÞ¼ÚÞãQ¼*a\x0013±ÝÃ¦qÏoJúöjÔ­4Ý7YÑõÍF\x001f.ê16&}0»\x001drO¡\x001f¤Õ§xÞ'Ëcp§h¾½ªÍü7-§$+lÜ\x001dÜrqZþ%Ðîa¾ìLÓ@\x001d¼¶Áä\x0002pGáÎ¹¹
å·\x0012${\x001e}}iÇÞÔ*4®º\x0015£ÓnÙÂµ¼Üÿ\x0000°sS®z$\x0001m§É8\x0019LsRE{rÿ\x0000òÕÉ\x001d>j±-ÝÏRGbW\x0011Vç+\x001a\x0010jä0iW.T­ãsêùÓJ¬²]é×(ÀdnÊÇAÖ.íWÈvD\x0003#'Ozë-µ\x000bß;\x0012zçñXÎ£½Q®p·\x001aì°(Æ\x0018m@ï\x0012|ßæ NÖõÙðÙÞ]3]"b?>`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=\x0019aÉ\õëÆ+Äµkck}4dc\x000cqô×}7Q7\x0016Í»ò\x000f¨=bx×Ã÷\x0002!¨,'Êgpè\x000f¥c§í#æteõ\x0015)Û£8\x000cÐq~õ!L#\x0012À\x0010q·¹¨ñ^+Mn{ÂR´bR\x0002H£i[j\x0002[ÐS]J±\x000c0GjØð¤\x0006}Oåþ\x0004gý?úõtáî%aÐ±"¥KÞ±´©¥IO«d&TVv</p><p>³\x0013\x00079¯Ið'ÂÝOÄ3F÷\x0011 '%O\x0007ñÿ\x0000</p><p>Ö\x0014ÜÞ5J¦¯#Òt«ÍVàAc\x0003Êýð8\x001fSÚ½SÂ?</p><p>Ù&ÔÆó×h\x001c~_Ôñ^ç¢x/Hð\x0014,d\x0003î \x001bûû}k+Äw2+G</p><p>-ø"4ïî{õ®êXu\x001dYä×ÆÊ~ìtG+p4½\x001e?&\x0008£.#Ç÷©ú.\x0005qÖ­s©£C+í´RvÃ\x0008Ú~¯ã]·¶_Ü5Ä6QZ¦Ñ£ÈN\x0007$gMqq\x0012¢ªÄíÉ\x001eâºÇ\x000cæÞç'8\x0008ÿ\x00007^§×>¬ËÄù$\x0018Á µoÞÚ\x0014;²\x0007\x001cs\x000fnµ©Äâââ@Åò»\x0002N0ÀZÂgm\x0007}Nvyd*È¡v\x000e\x0017¡/8\x000bÓéÖ´gèAôÇj£(Á9?sTG§M¢¹ëIN#84Ó\¬Ü(÷íIJ)\x0001jû\x0003âOúUu\x0004s»:"Â\x000c\x000f¦sýkwÁI¦Çâ\x001eo\x0011+bý¥>ÒÊ3ò\x0003\x000fùÎ)=\x0015Ê^ô¬}Uð\x000fÃ¶
>\x0016^ø»Ä</p><p>!¹¼í2n\x001f2@?Õ ÷cÎ?Ú_Jùß]ñ\^5ñ\x0006¡wâb·3\x0019#%\x0006KPz(þò\x0001ö\x0007¡¯Dý¤þ+Øø¢ÖËÃÞ\x0017ºY´èÏu$`w\x001fuA d/_©\x001eà¼6[!qÚ°ÁÒnN­E«+\x0011¤yVåï\x0012ø~ëA¹')5´éæ[\ÅÌs§÷ÿ\x00001Ô\x001eµÒ»¿
êöóéèÒ4ÚDÍ¸\x0015\x0019ÖOùêþ«ÜW1âM\x001aãCÕ$´¹*ã\x0002H¦O¹4gîºB?Â»*CU±ËN§7º÷2h¢ÌØ(¢</p><p>)Ñ©v\x0000</p><p>Ú@º\x000f4DÛOCQ:ÄÍ©P_\x0018tUW`xªæ©4õFs í$%\x0014QLEL³Èª\x0006ãÓÚ¡¥Áô LNô \x0012x¢¥A>Ô\x0014\x0013¹!A8ëíI"\x0005à\x001cÖ®ÝH
£¡'©÷ª-ÓNÀÒ[\x000c£¯µ\x00154\x0011ù\x001d)\x0002"Áô :³!TÜ:ÿ\x0000\x0015Vlç\x0000N´´¤\x00111\x0004ö Dt#\x0003\x0003e\x0000\x001dêX\P;\x001e\x0005EU$\x0010AéU\x0017Êî&®k%Ão¼Ä;î4Û85{XM«\x0001w¥3×Ó\x0015ç°Ió)=Ez\x0017à·¾¸+\x001câ\x000b7F	<;~5ëaçÌyXøZ7]\x000fPðN°§öW!òËüÐÈÃ\x0019\x001fZìaÑtèâH½	-¬àC\%½uªY>z\x0014^Bp\x000e\x0008#ÐÓIñ%ê£\x001dÃoB§õ®¹Eu<zsô<§âG¿²5Éâ±F%ä\x0019÷®\x0014ÄA í_ox;HÓuÛ\x0018^þ\x00105\x0008AICÛ&¾{ø¿ài4mN{\x00083m\x001b\x0015fAÆ3ò~ÃR[=¼.&MrÈòi¤+¸(ÀÚ6¨\x001d>~µ:éò¾%ê²yQÈ\x0011?7=êå¼I2Ä\x001dç'§½1£hCFÁ$á\x001e8¬\x001d\x0003µUìnx"ßÊÒu½A\x0016(v)÷ è?:¡á?\x0006ë>+¼0é6HócäLöÏsì9¯eømð­ï|\x001b&©âMJK?\x000f\¾øí`mÅî1 ýÐHÀ<9às^ã ¤\x001e\x001bð ³ÊÛG°Éh­ 8¯¡nÙÇ,y<Ö\x0010ÃZM²±8èFbº\x001e_à?:~%k·igíâE</p><p>¨Aç~\x001fz\XévâÓGT\x000e²ÉúzW%­xÄÝ1\x0014"\x0004'j¯\x000bê}ë\x0001|H¾hYVH×?3\x0003éÞ½*tl¯ö¹ÜÝ°÷\x0012rFI'9¬»û\x0013!ù\x0010\x001fZÍÓu´s	wìÀÛ´å¿Ãñ®Öh®£È<ôÅSV&.ç!©ÚfÙUåSÉÏëã.¬Qf\x0011´¬!e\x000b!PN\x0006yÈïô¯SÔl<ÍØãw\x0019®_SÓÎ×FQ°\x0010·\x00185&«SÍ.ì\x001dI\x000cG#\x001cc?aÉ\x0018	r²d«¦Ð16A\x001fËµwúh(FÌ·©çzn·à½VËÃúÕÝ \x001a|ì\x0004Dã89ÛÔ\x0003-\x0019­\x00157w\x0005±æsÛ©Ó/\x0018d4h\x0018ý\x0018}k2	\x0018ç½w¶Â=\x001eeQ×#9ç\x0018þ¼×/{m'iëÿ\x0000U`á{ðªË\x0019\x001eµ~Xx?)VÏJªè\x0007LóÓç;\x001d±ÈkJÇJ¹¹·á"&)g\x0016Èç2\x0011	¬üWMá\x00116\x0004Ú}äku£ÝöWèHèêcQN)½B£i]\x0019Zþ©h:¬úv³i5­ìXß\x001cz\x0011ØØ*r4g\x000fJ÷w¹Ò5ï
[i~*¹÷CÆÍ/Ä\x0001w\ézCp?3øzc¨òO\x0019øWSð¨lõX\x000e7Ã<gtS§gFèGê;ÕT¤á©\x0014«)è÷24(eÁ\x0004ò§ü÷¨°ÝJç¸¨Ó«Ð¤·XäÒ5Ø¶ùUÙbÎ_-Àlt®ÒÊÕ|Q \x001d\x001dòu\x001bey´çÇÞ#èØÊú7Ö±î´Û}0Í</p><p>4¾L²«7ð¸QõäÀT:\x001dìÖÒÅ$e£\x00182889\x0007Ý«¡FëS¬\x000eUÁRA\x0018#Sk²øa\x001fÛ­õ8Â[êet\x001d#­_nHaìÕÆäy]ØMN*HJ(¢¤²ÕªL\x000bv®®×^8<¼î\p
q`ÐÔâr\x0017\x0000óXV¡\x001a\x000f\x001aðéÄÐÔ.Ä±êy¬94®å4ÊÒ\x0010QV9±\x0015Ýis0¢*Îp§Sih\x0001ÉQøÒæF\x0007N;ÒA cÎ=)sôày=³ëLnµOa</p><p> tLCuê)ª)qZH\x00077P{ÔmÖíóQõ¦À\géR»eF8ÅGÛ8¥\x0007R@!¤ëÚ\x000c¶*B@áF\x000fLÐ\x0004l1MïJyïH=i\x0001§¢Å\x000cÏq\x001cÊÌþK\x0018ðq\x0002¶tb\x0004&EÅ:ÈAÅs\x0010Èñ11±V#\x001czVÅËäBØ\x0019*yàßZéÂÉ©\x001cøó@ôß\x0007=¶¡|³j7M\x00061¹±Îs^®Þ&_\x000cy?ÙwßÚKFìì5ã~\x0017ÖßO¶#O[Q$§rÄ{\x0013ÅMk,Óê\x0019)´\x0017Úxùw}kÚMIj|Üá(É¨£Üü\x0013"jú»êÑÜI\x0015¸Þ*\x000e\x000f\x0015»ãí"Ã^ðåÄ|ê&hýÿ\x0000oÒ¹»[©ôo\x000b¬{D²\x0010\x000b®0\x000fOÖ±ôï\x0018\é°HÂÏ&vE"±ß\x001dÇ<</p><p>Â¥>gsªeOsÀçðî¥
ÒÄ-$ó\x000b\x0014À\x001d\x0008¯Nð\x0007Ã¸âÔÐÍm\x001e³©4q¨Í¼\x001d>gÏÞ#Ó¦}k»Ð¼#¨ë\x001dGZÙÙ¹ÜÒ°ÃIì«]\x0005Þµm¤[6áÈ|ÇÞà³V=þ*We¸T®å¶ñ.§Ø¼0¦îúq©k$X¸èúc¨®+Ä\x001aú­ãÌy\\x000e\x000f§\x0014±Gu¨Ü\x0014@eYÀQî{\x000fjí4/\x000c5ÉÞÝî'8ýéL(\x0007z{óUe
dõ9[u4KCÑ<\x0015ª\x0001%Ã<\x0011à-p\ý{\x000fçYú¿b·UxîTGýôahêP\x0011Ãû§¯å^°×\x001fÙ×FÞy\x00166þ\x0016è	íøÕÛ3ûRÙ®\x0010yW8À\x001coíÏøÔ:®.ý
\x0015
5GÏ·ú]Í[«YRæØä%Ô\x0019\x0003\x0000ã$u\x0004t ò\x000fZ×ÐµV\x0002á9qÃ°ù$ëù\x001aéµ­\x0016ïI»ö0ÞVQqnNÅú\x000cDróò¿FèÙÍ`jZ\x0004\x0013íOe¥$,2
Ït+ü\x0012\x000fîô=WÛNe"9\x001c]ÑÓÚ_	ÐG!Û&;÷¨ï´ñ *ª	<\x000eù®BÂðÚ\x0018a¸}î\x0006ÇÁY!lð0zö®»M½Þ\x0002±óc<g¾}Çô©±¤döfU_SÖlìÖ2<Ç\x0008äv\òqì3]/Ç{ÞÆÃ@µÂA</p><p>äP8\
¨¿Jë<\x0005§Göõ9~ìJQXç\x0001üëÎ¼Y,±wy!?¼rT\x001eÊ8\x0003ò\x0015Ã%ík§Ñ\x001e¢°ÃÝo#Æµ+7Xlr·\x001cc#\x001fÒ¹{ËdF!»ôÇA^±©Ù_8ÎÜã«{}+Ô´ð\x0016BX:¨^¹®ÞTyÊnçM\x00048ÍÊÆ2#9ÚU\x0018cê\x0007<{Ö-Ü|W\x001e¾æ»K»"Y¸`\x00019'ùV\x001då¶\x0011ð GSÈ¬'Nèï¡èÎi\x0003ßµM\x0012î_å×X
¬<ÐÅIç\x001f_çUçP'v]#ÜJl:p2qì+Ç7¼+â\x001b\x0016êFG-¬ªR{ièæNáë^©£O¦jÚ<ZL5O\x0008ÜÉo5Â¥Þ)\x001f~7n©üÇ\x0004zøiv\x0004#¿B~´y\x0003</p><p> \x001cc¯l­fa:\x001cÎëFhk¶ÖvrÛi«xäe\x0017\x001bvyàÇ\x0015sI¬íRg*®î\x000e\x000erG§Ö °µ6Ñ5Ýá+B\ý
:iÚ\x0019\x00149ÿ\x0000H²ª[" Ýþ´ ÷6ä¹\x0016¥ù¥c\x0014­;.R\x0017óC}ÔR0ª1ß=ê¼¥\x0013|`m#·?½AovÚN©r\x0004fX*C\x000fZ
ä\x0013N¿fÂ\x000fÞ%ò\ú~\x0015qlfÒå¶k¦Æ¾!ð«¤xí¶¾d`QþònüTW0äî¼!}.¬Ãr\x000e|Wùº7<=FGãX;Ò\x0017DñV£g\x0017ü{¬d'Ö'\x0001Ðÿ\x0000ß,*1\x0011ÚA,¥OæsÔQErÁE\x0014P\x0001E\x0014P\x0001E\x0014P\x0001E\x0014P\x0003\x0011N\x0007àÓhRE\x0000w~8ðàï\x0007ëtÓÊºÅ¬8\x0012dl0\\x0001Èàú\x001aá;×´ßÄ5ÙÆu;¥Ñu¶ÿ\x0000³\x001cÀ\x0016e¯\x0016¨§'$îmZ)KCÙ¿g\x0007h^2O\x0015Yë6­q{\x0016ÓYívS\x001bFáÉ\x0004§^?:ñéc^ßû!j\x001feø£öf8\x0017SB\x0007©\x0018ý×ø¶ÄiÞ$Õ,@#ì÷RÂ\x0001ëò¹^*IûÅI'\x0004bÍ ¥#\x0004\x0011\x000e+Cx\x001c{ÓIçéSK<2¶â£\x0000ã¥Bç'\x0006íÐNôìe9\x0008Ï#"T±ô§`/¹ïN@Ø\x000b\x0014qà`ì$çëièi\x0000äRyý{U«[IÊ»O"¢,¼þµFã©ÈúÕFN.è%\x0014ÕÒ[ê6F$FvóõÅz7à½ºÑäM*d¾¶,ñ(</p><p>ã\x0007O9\x0018\x001d\x0006kÅb]Ì\x00018\x0004þ5Óø_\¼Ðµ\x0011=¤Îª0Ä/\x001d±ïÍvÒÅki\x001cUpÊÔú.ÇÃZ«*.±}ö+E\x0000,j\x001dñïÏ½t\x001a%¯ô\x001bXbûmâ¶ß>ä û à\x001f©¯6ðïÆ»{k-ÕÍÅ\x0012\x0016æx\x0015Tv}Ï§¯­t:¼öº}ÍÌVÍ{\x000c,\x0001¸x\x0015\x00046\x0001È ä\x001f¥w¹)»\ð¥F¤#ÎÑÔßëW×× I!\x0012\x0016Ùµ9ÏNx\x0003ÛÃñ\x0014ñi3:7\x0016</p><p>PbcÓw}½óéX~*Ö&Ôôñ}c0\x0004|-\x0018!\x0003>ÙþyªZ]ÜÚÇÖ+÷SÚ«C\x0011Î§æ0¶«)öÇ¥7\x001blU$¥¤µÝZU¹\x001dUÊÛ$ØÉò§^pÃv	=\x000f88í]_> ÞÛ3Øj\x0017ßhL\x0014ÎáÛ\x0007¶q=ù\x001dëó<·\x0000" IVLðJàu\x0000äzU\x001b½4èî¢ægO¼ËÙj¥UñÕ]y(ã¸ê:ò\x00085\x0012jÖgT)s+GcèÉ¯å¾H$¸+&\x0001\x0008À\x000cv÷ÿ\x0000ëWG _H,S®c\x0000ç?Â}9õþuâ\x0004»ñ\x0006ñ¤âÞòÁÁ`b¸ù\x001e½Üwþ~g¬Û\x0013Q÷eárHúñÒ±SV.\x0010mîô:+È!I-æPFÝÜn\x000c§ø_Ôzf¼÷Å\x001e\x0011\x0002ðµ\x001e]Òüè­Ê:v^ø=FkºKëV·WûGîØÝ¹zÙÎjxomîåH\x001dÃcË*	*zp}3Åg\x0016áª\x001c°ï³û#¼½Óµ\x0019!Qéú¶\x000c~c.âèç¡\x0018ä\x001a®]ÆâK\x0017\x000f7aê%B3æîèFxÇPqÚ½3Tð<zÿ\x0000hºha¸/Ú\x0004Qe]ðËAÆ\x0007çW,ü7ebövRÈo,a;\x0002Ñ\x0010r¼v\x0019À§*é­</p><p>\x001a*wÜ[ÙÃ¾\x000c²±BÝÜ®äóËýp\x000e+\x0018®£vFR¸É\x001fÊ§ø¬'ºÖí®¸Òá]h¾o-¹$z</p><p>æ4ÝEF²å\x0019¸f#å'ê?ýT°´ä£ynN:ªsIlêzoÊY¹\x000c\x000fÒ¹KMà\x000e\x000f\x000c==+Òá\x0011ÞB\x0013x³È-íÔ\x000fJÅÔ4Ò\x001b\x0000\x0000\x0001$Þº\x000e;u<UÓUp\x001c¯\x001cç?rº®,çÉÀÚA'ÐöMWO>bÌcû¤p \x0000@Çaôæ¸ýVÇ|ÈWçËn98ç$Q¸Ó¶¨òýFÒ$O(Êñ\x0002v\x001b[\x001eøà\x001aÁºªýà>cÆ\x000e\x001aô
FÎ%¸*3"¹ 2£¾?É®cPµÝ¡èsÓ>Õátwañ\x001aÙ&°ÑàðúÜI¨<ú¬À\x0014¶0°ÿ\x0000\x001b\x001e§ØV\x0000ÇzÐº¢Q´å[8ãg½RhÈ\x0019þuÃ88³×öÑXÑæmVî\x000bi\x0008XÝ!Gækb-5\x001e6,còÙ°{¹®zÞXà$Í\x0017Ë.àÙ\x001b\x0002\x0001éÔþ½s¬ô32À,lze³0\x001d\x0003×­]9¥ñ\x001cµiMÙSÑ\x0015u+}A7Á\x001c­5¿L/\t§\x0015\x0005ì¶pÛE\x0004QÈ\.î~]®x9ã'¥YÓ®tå+rc7ÜíÖf¯t·w!6]þö;Óº\x00154å.WÐ³kvV\x0018Ùq½xç¡\x0015Ñ|Ií6~\x001fÕ	\x000cÓZ}L\x001cáâ8äÿ\x0000ºËùW\x001fd[ÎÀÉ\x0004`2q^© x_QñÖ¥hÖ*
ÁÔ\x0012\x0011ÄQ4g|ì6)?\x001diÊiÒmÃ´mÔ_Ùïá~3ÖfÕµäÙá3çíY\x000cù{»\x0000>f=\x0007ñ\x0003\GÄ»Ý\x0012ÿ\x0000Æº¤þ\x0016´[]\x001cÉ¶\x0004Q´\x0010 \x0002Àv\x000cA8÷¯iøõâ­?Á^\x0015´øcàæÙ\x00141(Ôf_¼sÉB¼Çæob\x0007Lù¸×EÊmÍíÐô¦ÔcÊÑE\x0015Ðb\x0014QE\x0000\x0014QE\x0000\x0014QE\x0000H=i½è\x0007\x0002Æ7-<Q«Ùø[Pðý½Ù]"úDâ
ªC²\x0011´ç¨è:uÀ¬!ëFp1Uö¡h7&÷:¯¾-Àþ2Óuø­èÚ3\x0016¾ß1YYXg\x0007\x0007\x000c{zRjz¼>'ñ³rY&©%ÄÛKåbf%Ônÿ\x0000{\x0003>õËÃéHÃ¿\x001f.U¹j£JÃß\x001cã\x001cÔúnw©Nb±¦
ÅF:Ulü¤R/×\x0014Éº¾¥«ë\x001b\x0019+	"\x001c0Ü\x000e\x000f^Æªñ´ äô§"þõr2	\x0014Fí\x00126\x0004\x001a@y®Ç¶0éÞ0Öm-b\x0011A
Ó¢"ôUÉÀ\x001eÕÏPÕÂqpvbôÅ(;NG§qHzS=H4É$F \x0010\x000fÐ:Ó\x0001ÀÏ\x0014\x0012sÒà*å£\x001f1²xÇÐÕD+í«\x00101Tc1Ú8/5éô¬Àì\x0010÷\x0004Ã\x0007µz.ãÆ\x0011Å<\x0012±ã\x001eµã6rælà==«zÖf\x0018ã÷g\x001b¸\x001c\x001fP}k®k{²8±xe5Í\x0013Úô½{GI¤ìaO´\x001e£8ÝÙ8\x001e-ÿ\x0000ÙõÙQbQ\x000c£Ë\x0011ò\x0016\x0019È#Ñàþ&¸.L½üÔ\x0019\x000c§;mF-JÒ)Ô\x0005½\x0005\x000fã\x0018ûàû÷¯F\x0012<iR³45`Ö7\x000fï!\x0007È\x001f|g®;7¯¡¢;è­|È­­äÊë\x001fk°Éb:2èÃ}FE]¿¶thö£\x001bu\x001c1\x00046\x0007Þ\x0007¨'£\x000eü\x0011È9Ê>Ñhë´nn!Ý\x0018ÏSê¹?Q¦¹Ç</p><p>¹¡a%æ\x0001Ô4yæ»Ð¼Ð¥P\x001eÖFè"ö\x000e0¯Û\x0007Seã{Ø¦=¼\x0003Í 0,_\x001d0\x001b#w¶?\x001ekð¥íïöå²Ø+\x0019ðêñ¬^h,\x0013"<xÄ´\x0013´÷\x001cs]¿ü!ñÏ:\iJíjÁhbÞÀÉ\x001e"N@!\x0000ò\x0006A'Qmm#¡T·¿\x0007©è^\x001dÕmï ky¾ø*À""çÜã úö®ªÚ\x001b2^¤c>bÃÊ¼7D¶¸³ ¸!K3 Tàü¬\x0008<Þ·ì5M@8ÌÓ$\x0013æ2Å@y\x0005NOÊ}\x000fN2*%Cá4úìÞ²g¯ÚO(+\x0014ò</p><p>½ÁÏ¶F*¯Ù¢ÓÄí(7D\x0006qý9"¸-</p><p>æUwí33\x0006\x001fòÕq¸ë×­z.e\x0019Ë)Gd*G^½r;×=Z^ÊÒ"gR\¯[c6¬ºi`±Ïs\x000bªQ×\x0018<þx©ãÑìoôØnô¦ÙÜ³Û\x0011È\x0000\x001c¨\x001f\q]n­áÃ2\x0000\x0015J\x0000F@ÁÆs×Ö°ô«	´Ôsl\x0003:³¼¦E;P\x0015</p><p> ãwÎ?:Ö5.´\x001c¨FNç\x001d§Ü¼2`ÁPeyúcÒºåå\x0016)O\x001bw\x0002;Ô×vV:ä"kF\x0010Þ6Or\x000eF3Ï\\x000f\W&ÓÝXÜ²Ü¡É$´mÆyëìkuilyþô\x001f¼iê\x001anà\x001c.Pÿ\x0000\x0010è=«Õ4ï-\x001dUHùºú}+¶²¼\x0017VÁÝ\x0016í¹ÿ\x0000kÐûÓu+\x0008Þ"U\x000eàAÏÖ÷W<{QÒÕX¬6''\x0019\x0007\x0003¨úû×\x001dªéÊZW@T\x001eòyè2=«Ù¯tÌ,:@\x001d=«Õ4ÒÞcmÀf$\x0013v¸O#¿Ò\Yý¦LªoXÐwc±ú\x000e\x0007ÔÖ\x0008³FºH¤!Gl\x0019\\x0012«êN\x0001?¥z>³a5ÜÑC·s*ùi\x0018^\x001b¿Ëîk¹Ó_Ìh¢Gv9;Bä\x000c@ì95Ï:w=:\x0018±É2£*ÅÍÊµµ¬JÊ±îy3üR\x001e2=°\x0000üêåÝ¨ä\x0000ä\x0001Þ³Z>>ú×\x001dJV=(TRD</p><p>qñ«6OvN²,qÛBfvlô\x0004\x00008îYüj©\x0018þ¢¬Cw4V\x0016Ñ±ÎW\x001c¤3éÀV:";PÍp¡à\x0005äúW×z-»ü\x0016ø9}«]¢ÉâËØ<ÕNL </p><p>§Ô&à[Õ¸éóÿ\x0000ÙÓÁ\x0016v·_\x0011|\\x0016\x001d\x0017J
% pò/Y\x0000î\x0014ð¸êäzU\x000f\x0017øÊïÆÖ~.Öo\x0003Ç\x0013Z\x0008í c&\x001f9B©êOr}1X®jòöqÙn\x0015%\x001a)Mîô<WP»þò{»ÉkÝ¤G9gbrI>¹5Zñ\x000eE6´µ´\x001bwÕ(æ
îîzP	\¥%)æ\x0005\x0014Q@\x0005\x0014Q@\x0017uK	ôËùìî,Ð9FÇ ûÜ\x001e úUNÜÖ¦¡{.«öf8ÄÀ\x0016AÌxRÞø!xì¢«ý¨
7È¸ÎM;\x0014Ò¾03Û\x0008ÚH5#d(À>½ê0=z}i\x0012\x0003¥\x0014à¹¥XÙÏ\x0000Ð\x00033ÔV¢ê:ÜÅ¤ÚKu$0½Ä\x0018ÉXÐeý+<¤ç\x001fzÿ\x0000ìÃ\x001fÚ|u¨ÛÏ}&ê<}TTÎ\©³JpRãùÆA¥FÃ\x000côþT²pÌ=ê3Ö«tK÷dt_\x00105{MwÆ\x001a¶§§,©iu15\x0000À\x0010:às\èëÍ\x00189æp}hJÚ\x0004¤äîÀôÇjzòØ\x0002O=±OO½ß\x0018&"X­äu,ªJ¨9=ª<`\x0012@ükÙ~</p><p>ë:\x001eá/\x001aÏªÍhÍ¥½½¤3ºf \x0007©È^¿ZñÛ½¦áö\x0013¥LdÛ±­JJ1¹\x001a\x001c?=*Ä,\x0002ùÿ\x0000óÒªëORpx5FH»aó\\x000eØëÅoÛ\x001c[¼ú«³Îõ`Oø×Ie\x0014¯nò\x0008ÜñEÒ.1rZ"=+Q6SÛ\x0002,àqÓ×ð®qq
ý²!Î\x001dIãµÅ]\÷$ñÇ_Êµ<9®\x001b\x0019~Ít¾e³ü»[µwQ«Ñf&ø¢zjöî·6CÌ¹ØO\x0004w\x0006´®ôò­\x000e¤!Øè¥°9\ö<àÔ\x001e\x000f¸ËW\x000flçänê{]F·$FÖÖÍQ\x0014C<þðKqÛ§å]½å5\x0017w3ÖQío¢¾²\x0013ÀJ£Å`HéÇFÇ\x0007×ñ®ÏÅúçÚãï \x0017`£Z5Wù\x0010¨\x001cîTõâ ºvÕ4»¸ÔD¬Þ[\x000c,¼IÁôã\x0003¥s\x000ce²¸;¹¤((\x001bã<®OCn½k~U%ª3sä{îze¼\x001aèûG ÔÜ\x0019.´È	p¼$\x0003×¹N½Ç¡~(DÌµ®î\x0007ð:ç¦zW)¦ê>k}¢Ýä@:3*\x000c=×0}½k¦k÷¿½I$6~A/>JÎ\x0006\x000bö\x0004ã\x0004àg¿­BN.Ý\x000b£5~§Wa\x0014pÜ\x0013</p><p>ÍÁÕãö÷ë^á¾Ù~hÛnT`\x0010G¨9¯-±¿f1;J.¡]ï\x0013È]¢\x001dÇ¨÷ÿ\x0000&»¿\x000bÈ0\x001c>Õ=ÎAoÎ²ÄÅÊTj*uoc¶</p><p>1qU\x000eldÚ$c'

Y÷ 4ó^=Ú>(É&sm¥Úhëyr6n\x001cª¹\ìSÔqÓ¡çé\\x000e¡qe¯M&vÑÚÞ\x0007%%ngOzõ«ØVâ\x0006ÆTõ\x001eµæ~2ð×\x0015ìE4d2°\x0019ÈôÇÖ»ðNêOSËÇ§t­¡Å^ZK ßºLùL\x001bö}À?ZÙÒµD\x0002¯\x0004\x000c:1éôõ\x001eôÛmR;¶m+_Iîel¸0\x0008{t$ñëúVN«£]hÓ«¦öÝNÎ»|æM8ìæÎ)Ô´dí\Åæ\x0004\x001c\x001d¤pvþ­m/Uo,\x0013²lr¬F×÷\x001eÚ´æ)²ØRývÁ÷¤;ÜòMSKC\x0010¯æ\x001dÀ\x0005Â÷ÏøW\x0019¨ØeFíê</p><p>o\x0007\x001c`ä~_{}þ7î1\x0017#½r:Æe`0z"¹ÿ\x0000>´hÂílxÅÅ\x0015ÉÉp\x000bpz`ÞY2äÆ2¬ÇÆkÔum\x0011¡w(É$\x0010Ã\x0003\x0007þ®Êê\x001ad±îIw+`íÈÇ\x0003¾}ë9A3ªw\x0017©ÁÏ	½û\x001aunákÆØ8ó6\x001c6Üò\x0001õÆkjâÕ\x0015FB¹ã</p><p>só\x001aÌ\x0017wvdP@$áqøW\x001cé\x001e½*êZ¥ñâ¯4­+Ã~\x0015µOðÝiX\x000520\x0018P@'åQïÉ$Õk\x0011´øe«MÆt\x0012AÈÉ\x001fä+·¸ÚÖEû$2Îù\x001el¤°PF>UéslWc¬Iö/Zuªð×rùî¹ê¨8ÿ\x0000ÇR¡IA4ÅÍÎPõ<é¸4ÿ\x0000xÓEr½\x0019ÔI\x001eÁËþBÜÈÙ&+WÃZ¶«Ewy§Ã¨BÌ\x0013}ÖúÔ³HZME»#(JÛñfµ\x000e¹ª\x001b«m:×NhQ\x0005º£ò¬ZkmER1ºî \x0014TBó6Ô\x00194ëwýM+­\¼ÖÐJp¦A³lÐÃ\x0011b Èy\x0019\x001cUk¹Zr\x001cçÞÖÊ³\x0000G^£°«\x001aQÇ\x001d¬Ð,Ñr:üÀàÖ©[q»É]t2Üå¹Í</p><p>¹àúé\x000f-Rt`qúVopE»X\x0011Üc©ÇzlÒ\x0005;c\x001bP÷õ¨¡%A\x0000ã4p§éJ¸Ç¨!s®óà¿-|\x0007ãhõûYîm\x0012ÂÑÀFó¹p\x0008Ï\x001dqþx®\x0008rã5#&\x00088ëYI'£*7Z¡ò~öf(1$\x0001ü¨\x0011\x0018Ë\x001e+ODÑõ-^ëìúMÅíÀVÇo\x0019vÚ£$àsYó\x000cu\x0007\x001e¿ý~õqK I=Ù^\g\x0000¨Å9M/ðç#éI \x001fþª±o\x0011eãî¡?Ëüj\x0018ýMhÚqgxëÙ\x0011sî\\x0016*;å\x00065Û	\x0019À?Î¡<þu,¿ë0~R\x0000\x0006>Z¦µ±7\x0019°\x0012?:QÂ\x001eGãJÄõîy§¤%\x0014ðiX\x0012¹©á\x0014_\x0010Ø­Ûª@%\x000eåº`sý1ø×©Ç=µÜ77?.$y\x0018c¸É\x0003ô\x0015ãúz
Ç­tö\x001aédÑ©<
 ×5Z.rRLõ0X¸Ñæ=îD¹\x0000\x0011¨ª\x000e\x000eîIúVæ\x0001ÆO \x0000þVtKu\x001c\x0001Åv-\x0011äÉÞM?<K6åÆÝAáá÷Oô?Î½RÏÄpê\x0016 K\x001dÿ\x0000	ôÍxBrBçéôJk@È\x001cù=G\x001cúW]\x001aéi3\x0013æ÷¢z½£ý¯÷S1Ê\x0003²By#\x001d\x000f\û\x001a½.
õº$ì\x0004øçrçpü\x000f^?Î+Ï\x001eîc\x0014N²6Ç]àÓñô÷®GÖ¦ºMÒ³ÆB»9ì\x000fà
zjIê\x001aTå±q<?\x001cY\x001b\x001b\x000bmlã~¿lÀtßßp\x0019P\x0002\x00158Y\x0007OqéÓ½fOv\x0012âE\x0019uõ?ýoÒªÍ4\x0012ÇºØl`~îqÏ¨>¾½«E\x0015-ÙÌç(icµú'X±çìHÖ11;¤sÁ\Ôm'\x0018®ÃúóÏ*FæmÊrã8\x0012óÃ(ç\x0007\x001eý«Î|=r&ýÝü°[¨;\x0000¶ñdý?:ôí*Þ\x0014&\x0016"\x0018£aæF0òãLt89=>ø¬ç\x0014·.2ç=3H½A8f\x0003ÐñÇ#Ö¶Á\x0004\x0003ë\?lÈ»6</ÖA÷ÈÏsî+¦»º'+\x001a|ª0\x000fl×^S´Oo\x0007p¥yì*«{\x0004\x0012Bþr\x0006]§=Gò¬s¬:HV@\x0014çi9à\x001fQ´¼XrsÓv2\x0001ô8ÿ\x0000<Ô{)ÇSU£UòIâ>7ûN\x0010«*\x000069ôç9£D»±´³M>ãSK]ts@aÁïn½}*ìüKmn²£\x0008\x0012\x0006ùU\x000f×\x0005Xä\x001e à×ë}³´\x0016VñË(Ú]÷nÏ\x0000\x0011Ð\x000fÃW|gÌ</p><p>b:L·®i\x0002ÍÖâÎDMc,xa\x001fýó×\x001eµ&«\x0006EI]ÑØp}\x0003{ûñ\gõ\x001dGÂ<íq§È1%»ò\x001bý¥'ß\~5ÛÏ¥Ùj0E©èëi Ì±yD²qýÐy­ô<ºe\x001bÉ-
è:²ò\x0006\x00085¨éË Ç¸ºªsúV.©y_$ÍæB>ëó¹;síú×_gr'R¬ñ®\x0014¾òHÝÓ\x0003ñ¤Ñ0ô8
KGbÊfv~WS·\x001eâ¹}kEóT$Qª\x001dÁaiÎ1zÚ½îËÌß0#k\x000eïL©8<\x000crséM.ârkcÂ5\x001d	£\x000f%°T\x0017\x001dNsÅss\x0002	\x001a9<·\x0004©òÈV#Ðóé^í©i\x000c©	¸1ûÊ\x0008\x001cuä×;y§;<\x00115¤\x0018
óKº(9'ÀéééJQ¾ÆkrîÏ\x0018°Ñeº\x0010¦U.ì\x0011´Ål|NÛmym¦ÄùÊ\x0005`÷\x001c·þ<qøW£é\x001aH°[ÝbñQ"°_3Ì \x0000ÌyU\x001e¼ãõ¯\x0013ñ\x001dü£qu+\x0016gcÉïr>k*B'v\x0016¤±\x0015nöF+sH(4å\õ8¯)î{\x0008o4ö9àt¦@Ä¥¤¥ \x000b\x0016·RZ¹h±zifÜçVW¹|òqå¾péÐÑðæ¨xYµÒ´{Y.on[dq§êIè\x0000\x001cx\x0015õ\x0016ðëáW4Û}+Ç·ö\x0017> ('¥Ónîª½\x0014còzñ+:4ê8Ss>VrLhyéµ³ÛüÜÖ2OÊxçSEÎS'\x000c8úÔ\x0012\x0002	Èç½u½®b\x000cf¦aò\x000c{~\x0015</p><p>õÉ\x0015µ é3ëzµfP\^M\x001d¼[Î\x0017s°UÉì2EbÝ¬"å±\x001fãK!ÏóíZ&Ð¯<5®ßé\x001a¢ª^YÊa)Êäw\x0007¸#\x0004{VD¿¥h¥îµf\x0010d\É¯«¼\x0005à½\x000bUýoîäÓmßQ6×s\x001b@d\x0012FX¡ÝÔ`\x0001À÷õ¯"Îñ·®kí\x000fÙìÿ\x0000h|\x000bÕm:áîàÇûÑÿ\x0000³Wm%c·\x000eí\x0006×tyOì£òüKhÿ\x0000ç¥éÿ\x0000¸kÄu4\x0011LÉÝ~\ã®+Úÿ\x0000eÇ1üYµSüV³üt\x001fé^3â%1ê×HF\x0018ú1­é;\x0012ØËïÚ¹<v¦\x000fÇ54kÎ;JÕkQsúV¸#C½|u$\x0007ðsý*9ÀëùV©\x0001<"ÞKö\x001fÆ?øº.8õ1äûÓqÉ\x001d©éR\x0011ÓéUrB \x000b\x00003ô­\x0018â\x001bð{zU;T
2ñÓÒ~ý\x0000QÇ¦?Ïõ¡ì\Q\x001c\x0011\x0004¼\w\x001cÖµ´j\x0011²9ÎF\x0005PµÆ\x0001\x0004`ð;w­8A\x0008@ÁúÒ@Õv¿¼ÈçëÍ_m&\x0008¼\x0012uYÕÍÅðßæÀÚ«8úY÷;ddyÀ­?\x0012k_è\x001fÓ,¡$Ó q!|~ògbY;c\x0000UJú$:\x001cJRÞÚ\x00181s·©ç\x0018Ílç\x0004ñÐ\x000cÈ·Úp©\x0019Íusèó[è6.äxâL|Ä/VÏ¦r(¶äÓ¦]</p><p>vóË\x0000fÎÜà¡<~\x0015©¥ê\x0003d\x001d\x001b8#Ü\x000e.Ed\x00001d{ÐËÊ\x0013¸=\x000f=ë¢w\x001d\x001eÇ-\<g¬w;];XgØ¶S÷%S×ëÛÛÞ¯ËÜ½¸</p><p>øùOÞ\x001eÕÄÙJeÀCÏ1¹áÏ×Ö¶ôíNX$\x000b+0Mß31ùöÏ·NkÐne¡ãÕÃ¸¿xé4é#2®71<pW\x001cõèk­Ño×Lx®\x000e\x000c\x0000\x0006ZN>à\x0007ï~|\x000f|Vw-tíkTþÏ¿ÛÍ:þém\x0012°çÓð#ùÕ­OK:eÕÄ\x000c\x000eÔl7ËqÛëÇZÞ5ÕùYÍ<\x000c¥\x001fi\x0013ÖtO\x0010FÚ{ÜBèìà}×áO8^psè\x000e>¦¨ÃâëÈ!/ï	v\x0005\x001bæ8ï\x001dÕåt÷\x0016·ßi	\x0014`*w\\x001eÿ\x0000Ö*c<\x00121L\x0000¨@\x001b~é\x001dÿ\x0000úõ¬hS¹æÊU!£Ðô§Ô\x0017QB¾X]KÌÌÈqqý1É­->êF¸Xïí#Ø~Y#q³æÉØrO×½yÖ«½ÄAe1Ê#MÀùÛÐö#5µf,Ð)QæÈ\x0018<®\x0011\x0014÷\x0018Áõëü¨«EZÈª5w=FãNö \x0012k²¸\x001b¡EÊþò·¯áõ®\x000fZðÆ«\x0004Ó\x0018äi-±GLÈ\x000f®W¼\x000cU\x001b]nëI¼+\x001cæÚ6\*H	VÆ@Ú{gë]\x0005§¢¸Y\x0011Ó\x0008ed\x0000g\x001c\x000e_zóeBt\x001eÝ<Tj+3Ëîl~Ò¬Ñ¦ÉÌ.\x0003\x0010\x0007l\x001eQÈ«ú%ôÞ\x001c\x0018tYD24æâFE2ÈFÑ´u\x0010|¸ÆY·tâ½\x0012é´ÝN6Hb¸\rÈ\x0001>ä\x001bõ®n\x001d\x0012É%7@Íq J¾â</p><p>\x0011Ç*x`8ùZM½Îª\ªéuî\x0017V\x0010êé=Þ\x0019î6e¸µ`A$c±\x0003ùs­£N#-\x0014Ò¬1©Î\x001c1eol\x0003ùV°ÓÅ×W\x0012<WqÈÏ\x0015ÌN0ÃxàA'\x0004`Þ¸©'¶Mr\x0011w\x0004Me¨.Wm\x001fCüù­¡QKC¶\x0015Ò|Û£CO¸ó#BÎ¬\x0018\x0002\x0019\x000eGëVäµó{.ì×\x0013m}%¼Ëòm*vÌ9ÉË\x001fö¹ú`W¦i°o\x0012pÝ~µr|ªìå½ôG-y£1\x0008¥±Ís:!g	îl\x0010Ãþ·\x0015é×q¢8êIà\x000fZð\x001f\x001f\x0012`Óí¦Ò|?*\x0019¤ÊMp\x000exäa}½ûÒ¯¨ã\x0007Qò­Î\x0017ã\x0017-Ø:;o\x0003\x0013;«}÷è\x000eßy\x0004Í¸·+ï,ìAbIÉê}jÀØÅ­rb%t}\x0006\x0016¥\x001eT@y4R×u\x0014ô@~ñÀÅN^\x0014Mª¥\x001c\x0003±RR\x001ei(\x0010b¤·Í<q©PÎÁAb\x0000\x0019=ÉéQR÷ \x0011ôôÚþ\x0001x@ZéOmªøóR\x0019n\x0007Ì)ä}\x0010\x001e«Æ\x0005|ß«jW¶¥q©O-ÍåÃ%FË3\x001fZ¤I=M8`÷?g</p><p>J-¾¬Òu/¢&\x0000Aç¨4ë \x000eÙ\x0017£~½êÉ´(Á \x001c\x001eµ\x00109\x0013\x0004\x001c\x0003­o	]XÃR®9\x001dþÖxb
KINñ\x0002Ù]\x000b+{¸Ùn¼¦\x0011\x0019\x0011í\x000fÐ·\x001d:×;%»E f\x0004/PHÆkéE<Mû3ø§IÀiôÂ×(\x0017\x0000\x0016QÅ\V\x0015î´:0©^ïú¹çßµ\x0006-þ-ßÜ ýÝü\x0016÷+C\x0018Sú¡¯\x001f\x0015l:÷¿1kh\x000f5ÎY¯4a\x0004êñm'õv¯\x0019¿ÓZ\x0018\x0015F:ÕSw\x0015£gc*!óðyãû\x0013öIÏð>·kª^\x0003ÿ\x0000}D\x0007ô¯ß*ÝÀÍz¯Áïw\x001f\x000eàÔà[\x0001{\x0015îÇ\x0000É°¤\x0008\x001d¹\x0007<jÇ\x0013MÎ:\x0017FZ8_³¡0|jÒ£õûDg\x001fõÅÏþËÒ¼·Ç\x0010y\x001e&ÕW°»G¾$a^û:Ü\x0019þ2è\x0012\x001eY§l\x000eÁ.qù×\x000fñB=¾+ÕûcQ»_üiÒ[×lãWï</p><p>3Ó\x001cw¨Ç^Õ 'óÜáLþ|	Ç\Ð×\x0012µ´væBaGgXû\x0006 \x0002\x0010£ò¤ÜDmÏR;úT~úU%`lHÀÈÏ­Z¸#¨\x0004\x0010FF
V\x0007?hK`\x0000\x0003ÿ\x0000<þ´jØ(/9\x0004ûúUè\x00173J\x0001$\x000fQYðI°øûU»V</p><p>X\x001cA\x0019ÿ\x0000&WEEÙCó]¯Ìx\x0007JÕvG\x0007#\x001eõhC]\x0002\x000f\x0018ãüö­¨°Ñ\x001e;qI!Ëc"ìb~1~¾ª£æÈ\x0004\x001eÆsZ7é2s:VtäG=³ZÅ\x0008[¢S%eK6\x0015I8\x0019ö¯Cø%¼ZÍ¾a {=&Ö;Ed9\x000cøË~qú×&>P9\x0019îkb0q3êHëúÖSÚg]*Ü´å\x000bnJ\x00026yõ\x001fÒc¾{Sò\x0006p}é{öäôªFLDÛ\x000c·Ëä©a­2Êa¼.ê§åOÎÝ~aõæ´%Ç \x001dHî{×+\x0016
Ôç?ãZ)¸+£\x0017MMÙ¦Þ´Vá¡&·ÎwFN\x0001þjzW`|as5KìI(M¾{\x000f\x0001ÓxÏ-î9¯#ÒgÞ`ðJQÏÞî\x0008ô#¿ã]E½gs9KµKi±·Ìçk\x001e\x0007ü\x0007ñâºib!-%¹Ë[	R½7¡ÑÛëW¦`]Ô£d®Tqîr\x0008õ­
ÝÆ\x0019?~9\x0004\x0013Ï± ×=%Ú©`K+\x0013\x0015?áü©ö7ÒA&è]Eä£\x001aôaRÛ\x001e5Z\Ú5©ÓC©Imæ=Át¸å*\x000e\x001b\x000e\x0008íÆqÏZÍ}rkk£.ù\x0011e]®¹Ü\x001c÷ôÇô¬íC\{`\x0015dùN\õ8íÓ\x0015Jòx¦(±0\x001f8ÈÀ#½ò+«Ú]\óþ®ã+3¡·×_ÝÊÐß+BXõ#>Ã\x0003¢·\x0012â\x0011lÒÙÝº\Ç.6\x0002'<27ÞëONÂiv©.¡\x001eïº\x0008%wm\x0007Û=¿ZÜ³¶\x0016á¥</p><p>åBdç\x0018\x001e¾½ê$ùJ*¼NÂËÄ×)m\x0005³¬?xñ2q\x0013ø×ga®M\x0011¶\x00122J²©xÑÎÆ\x0003Fzûò+H\x000cdÂìTüÄ:\x001b®>(\¾½»m<ÙK¨YIþ²Ö1µÇO\x0018gc\x000cuèz05ÉRþ\x0013¿\x000b^òµGd{\x0006¡âÛIt\x0003qfÆ8í'ÅÌ\x0013Ç³`-ÐpA<ç\x0014\x001e­\x001e£cpº|>Y\x0012\x0007iÙ!b=\x001b\x001cñé\.¤êñÞùºÜ-n\x0011íÍ\x0010k\x0008ùVl\x001d¹^Ç=Æ1½o£Ái\x0010£D\x0007\x0013O!b«Ü.xQì </p><p>Æ4z³ª¶*+Ý¦¥åÞj\x0017RGY\x001c\x001byoË¹þµÝ]jºü;\x0015Æ¹y\x001d¤1DªYÛ\x0004:\x0001ÜûWjß\x00134o\x000eÇ!Òÿ\x0000âa¨Æ8oõQ\x001föT}æ÷'\x001eÕáÞ+ñ6¹âÛ·Ôu{©¦@~@ä\x00009è§åENÌ\x0018wW[Xôß¿\x0019îµÃÃêöº{\x001d»Û&\x001e§Ð{W²Ï{0yYòÄäÓ¢É2e\x0000HjÐO9b\x0000+Üp£ß\x001e´^êÇl!\x001a:Ejg\x0005×t\x001f4®@\ðOb}»ã½c;\x0017bÇ©«ó¤*\x0011íøtZ{´jÍÀ5ÃVóvGlZo"\x0014¦t©\x000bÆ\x0001Q×Þµ\x0004\x001auÔì\x0004P±?Jæ~îÞ)Í^%?­\x0015bòÖ[I|¹×k`\x001cuâ«Ð' QK@\x0005\x0014 g¥oh\x001e\x0019Ôõ«'M°º½!Åk\x0013HÁGr\x0007AJRQÜÒ)Tvok$çä\x001cw'*y"¶´Å\x001c\x001cR]\¿Í\x0012\x001cc¿ãTªUÞ¬·(SÒ*ìõz>©øN·Öæ·Å¦\x0006v@±~b¤öÈ\x0004\x000f­Rñ\L:î¥&n±ÚÉ,Ú,±ÇUNy<b³fÚ3G\x001b|\x0006ÿ\x0000¼¡ÏåUt],õ9üûHî¢ÖkvI\x000eÜoB¡³Ø©Á\x001fOzªPw¹ug\x0014¹Yª\°ÍÉ+òóV¼M¬èq]ÚiÓZÛêQy\x0017)\x001b\x0000%B\x0008Áôê}ù>¦°n</p><p>NqéN?-¼N¿x\x001c\x001aÒ­¤ìsR¨÷ÍyQý</z>vÒõ[7î@pì\x0007°å?JñB_9' pEiÛø«UÂW\x001e\x001dK¡ý=ÒÞ<^X'Ì\x0000\x0000Cuì8ïÅy\x001fiÑ(ëÔæÕ\x0019
#Ò lVmµ\x0014ß|r3V]íöÆ}9¨ÔQZ\x001a¾\x001eÖo4MZÚÿ\x0000L¹Òò	7E4g\x000c§\x0018ï×xô5\x0006½u5ìpÝ]HòÍ<Jò9Ë3\x0017É$÷9ÏçT#b¬¤gÖ­êÉ·LÒÏ÷SÇýt#úUI-\x0018ÔM\x0019Kß^Õ<Iæ8\x001d\x0001?W\x0007µnû\x001bp\x0018\x0014¢µ%ìZ\x0016èZG\x0018\x001c\x0000;ÕI\x0000B(^\x000e;Õ©\\x0008F\x000eFNO¯µgÈrO¥k-\x0008Z8=_j¶A\x0008§8öéPùl#z8ÿ\x0000>ýÄ®\x000fAï®Sv\x001aXm$äñ;ÔÊNÌ/\x0015\x0002
Ò(\x0003©íZF\x000cÈÃ°<N)=È´ò~Ò\x0018\x001e:ÿ\x0000]\x001c\x0018òØ\x0002{ñ\íeoy\x0018ã¥tVcå$góÿ\x0000\x001aI\x0014ÌÝA~q×¨ézÌeÃÇÖ¶/ãùr@Èâ²\x001f\x000eH<õïZ-:)`S<cÛ[1\x000eIÇãYq7CõÈà×QáÙìíu«\x0019õkWº°eiàS·Ì@rW>ÿ\x0000Ë"¢mØÖ»³#¹³Ö\x001bv¸·$<ÈüÄ+½s÷£Þ¡8ã@À®Ãâo\x001fÆ:òÝÇ\x0007Ù´ø#\x0011Z[ñNå±Üú\x000e\x0001\\x001c(Ï'¶jbÛWfµ\x0014S´Hç\x001f¸<\x001cz×'\x000eEÄ¹$WZã1J1ÐW)\x001aææ^é:¹|&1øÍ60JÉ'ÚªÜd9É$þ5b\x0011ÈÚ0G\x001dHª×\x0019.I\x001c¹¬\x0013Ôì¶¯_i\x0012¢K\x0001æ\x00179Cþ\x001fwÚFµ¡kô
:ì\x001a@LdýG"¼©X\x0000¹\x0000\x000eÙ«Q\x001c\x0000\x000e:gÿ\x0000UtB¼©0ënMñ7u\x0010\x0012ö\x0008<ëv\x0018Kvócltù@>Ç\x0007Ú¹Obd\x00176¤î?xb®ü?×5+\x001dI¡¶¼"'"1!\x0019Û¤vë×5ÝKâkGÀ¾Óç8_Çó{ãøâ½l<ÝHó#ÀÆQxyrî\x0017K¸+)\x0016ÑO6ïàE\x000cqú×£èw÷\x0005eO\x0005\x0018#ínÌãß\x0003¿Ö±¤ñ]Á;BÏ4n>\x0002Þ-Ô¤D{(Ò(íG1ðÍÇ\x001dë¢ìó'\x001e}FµÑmå·Xî\x0018ÈPçËL¤g@yüM\x0017º¡A#_ß[ZÂÝ\x001c</p><p>\x0019ÿ\x0000ïïõ¯.Ô/üOx÷kss'j\x000eð\x0006\x0014\x001fJóÛ¸]e\x0006ç\x001f8Ï\x0007'\x0015\x0012¨áù·g¬ë¿\x001aìtýñøgJó_ ¹¾Ã~*\x0005y<iâ/\x0015\u=Jg\x0008×åP>²¤sJì</p><p>¤CûñÅZ\x0011ãb¤x=K\x001fóÅavÙéF\x0014é/u}åh!R\x0002Êq\x0008;\x0013÷ùïWon¯2«P±FF\x0015\x00060\x000f½iXÙA,/6\x001a[ÁbAË6=;ÿ\x0000õ«Q<2ö_é~$w3\x001fìH3!ôÝýÁìzÒ²fÍ+³±°à\x0019IHãÉfvà\x001cT:¯²$\x001eC\x0003	ËÄÿ\x0000Jê5Ôû@F«\x0012`\x0004EèOáé\ìú|«!i\x0000</p><p>§\x001csÒCÜ®s²Ã$aduã°8­;;¸Ø\x0008ØÚ¦½µ¢p\x0010ñÔ\x0002pk\x0019¬îF\x0018C/Ô!®g+\x001d\ª´»2\x0014wòF1ØÖrk·6ð¼h®NVAÊsúþ5»¦Ïl¶þEØ*äs¿\þ±jÌÍ\x0010;3Æ9®yÆ554¡*q²ÅÌ·N^áÚGõnµ	\x0018çµ\x0004ð\x0000þTªØàô¨ÓcfØÊQR4y\x0019^ì</p><p>þ\x0010&¡¦ÂWãûìo	Â¢_Þ]\x000eØî\x0014úõ=\x0014sä ®Ê\¶9¯ÿ\x0000\x000bu:kqö=\x001a\x0006ÿ\x0000IÔ%_\x0000äªôÜØíÛ¹\x0015èÞ4ø¡|>ÑfðÂe_0ÖC<\x0012Üÿ\x0000µÐs´w®gâ¿Æ\x0007Ö´õðÏ-ÿ\x0000±¼%n¾RÃ\x0010Ø÷\x0000wltSýÞýI=¼pÉAÔ|ÓÛ±³¦¹c¸®ÅØ³\x001cÉ>´Ê^¦Vç>ç@fm\x001c¢\x000c('8\x001cgñªË$~q}y¥$-×89¨î7\x0011ÎsÔþ½ëzvH·*^¯;§£\x0011S[¦û7È\x0000\x0003ÁÍ. »3\x001f21¨àÿ\x0000*È\x0006@rNzzu¨¨µ* ò0pO ÿ\x0000>Õ*eÈR;c¨lr:åM7%\x001bv\x0006\x0001ÇåT±-k©ézß,áTè&ÒÖîKù¯'µ½\îPT¶Í \x000e8\x001f5Äµ´f\x0016X\x001d\x0008ãç\\x000eµ×¯íeø5/¥ax ¾_Ç³fÒ¾¹ÎOB9®"ÜlxÇqõR[Råû%\x0019\x0006ÆÇ8=\x0007LV¦¼¡t}	±$\x0012°\x001föÝÇô¬Û9\x0000ñ~Þ¶|Pt/\x000bÿ\x0000µc)Ï¯úTÂö2Ñâ`Ð</p><p>°ÃiÉ'?LT\x0011pÃ°üªÄ¿:d\x0007Ozdî\x0017!W'©5\x0011\x0007©<zõ§ËHóÜn\x001fLÓ#\x001f)ïÒ­Êú\x0013k\x001aSÃ\x0018y\x0004ôÆyª$k]×ug¯ËÀ\x0018íYR)\x0004sÓ>´-</p><p>¸Ä£«ª(­\x001e_µI&@
×=EdÛeUÚ\x001a3ÔVþ2mùFz\x000fóïPTFÂo@Ú8ê\x0000ý3Zö\x00149\x001czÕ\x0001\x001e/\x0011±Ï<zµ§h\x00041B\x001bØ§¨\x0001¸=\x0006=k
$Á\x0019\x0004ãë[ú\x001ccAíÞ±]@\x0019À<Ù=\x000eg¸°°<qÔw­¸ä?/\x0004vÿ\x0000</p><p>Í´¶]ÞLNû\x0006æ\x0008¤à\x000e¤ûzÖÇ\x001dFqè*\x001bLÒ\x0011kq6\x00079Àë\x0015H=pzt§¨ÈÇò \x000cø÷üªK³\x00128Ù£&æ8ã¹ÿ\x0000õÕ/\x0013ø7]ðÜ\x0003_°Å®ãó \x000cÀå{ç\x000722:×±þÏ~\x0011\x001aÿ\x0000þÝs\x001eí?LÛ;äpòdùjxõ\x001bÓÞ¸¿^7_\x0018øþé­dß¦Ø\x000f²Ú\x0011Ñ?3ÿ\x0000À'è\x0005a*ÍÏ\x001bÓ¤Å¹ÁÂ>CÆ\x000fçU.1¸\x0003ÓÖ® +\x0018\x0005qéÓÿ\x0000¯U.q¿\x0000dzh×¡\x0002\x0002NO\x001cã¥^³BÎ£¦8\x0007üôªQ\x001cc\x0003§¿\x001fçüjê\x0002¹$ñ¤\x000cZl^ÒoVÇWåpPnNºËßùÔ:ÝÓ]êÒL\x0018ãiööüj¤¬Tç¡=ùúR\x0008Lg ÿ\x0000\x000eÓìA8éí]ØZ¶\\x0006.æöYádîîÙò\x0014%ù\x001eNßëô]3Nû=IÔ"XÚG2 Q¹%\x001cqÜó</p><p>Äù¾[³\x0003aW$ó^¢.k\x0016ù­î&<æI'Âð2 Zõ¡¬OÄ5Î^¸Ð'³æ\x001býn)¤»û[ýîps^a®XÅ
ìm(\x0013ùûÇÔf½ßXÓ
ºÁo£Ú£+\x0012\x001b' ÿ\x0000:ÎÚÊvÍe;\x0011S¹ïÉýzÔÚMN\x0010Z3Ê´í2[éÖ+xÚY\x000e0¨9'=z÷\x000cü\x000bó´E¼ñ\x0015ÿ\x0000Ø$|6Ås¨÷ÏCíÍG£ë\x0010Ù¨ÒÞ\x000bR\+M\x0012)l\x0001÷AÎvúµÔÚøÞÊCkæ4(\x0003:ÈÙhÉìA==ë*ÉØÞho-NlÙØx~Y¬<-§I\x0004­û¶¾¹;î$$óÈ1ýÑÒ¼ÿ\x0000^ÞYcísÉcùÏ×¢ê:¼"ÎöïgïÁÀã$\x001czWß^ üÂ\x0010I\x000e\x0008Á>ßç­g\x0015#¥Ô§%fÊ-içG</p><p>< Í\x0018\x001bI\x0018\x0003\x0003Ò±/^),¥
³î'$ïÒ­êzRÐnÚ£®\x0008ÆdÏdóÆ³2I\x00199\x0019¬åMÞò:©ÖMrÃVEi¯Geæ¤¢AíC÷O\x001d3?Æ¡>+@î"´E
IûµKYÓ^Ûk?(Üî\x0015r\x0006æ*¸Ï5°ð§U,EH.PÖo\x001aöðÊêª{ìï]$\x001aß "A¸¾uè÷÷/â¨\x0000®A¿5\x00198ü+\x0017NÚ\x001bF£Õèß¡-ø_´»"*+\x0012ÁW8PyÀÍUïR³\x0018nG­0zVr]Wêu\x001f
u­\x0017ÃÞ-´Ô¼I¤¶­c\x0000f\x0016¡À
&>RAá<àÿ\x0000õ§ÅOÚ×Ä-OÍ¿³éÑ1û5Mû¸b¼ØêÇðÀâ¸#IY8¦îËSiY\x0001æ\x0005møSÃ:¿õ´Í\x0002ÆkË¹?1Â\x000eôU÷<S½ÌP2kÐ<7ðÇ^%ÒbÔô\x000fO-¿êäXáÞ=T;\x0002Wß\x00185ÞÇ£x#àäbo\x0012<\x001e+ñº\x0000SMÿ\x0000¢Y?c!þ&\x001eã=>QÃW\x0005âO5×µYo¥ñ\x0005õo-ì¦xbG@ª§õ9>¦¦íì_*_\x0011lªo"fû½ú\x001eJõÿ\x0000^\x0006µÁ¾\x001cñgt¤JOA}ä.\x0016)A\x000b¹zÅsê3^.X¨Rr</p><p>\x001fé^ùð+Ä·~$Òu\x001fÚDö:ÊÚ\æ#=}>ócÔ\x0013JM§sZvq³>|	ÓHï\x0004¼}\x0018§Zn\x0011\x0002\x0001éjÔ²ê7\x0016r®Ç1á¸Û <\x000f®A\x0015J,¢ºòw#ø×Eù¢Ì×$Ú\x0012ãæ\x001d>lçúAp1È\x0003ü*ÄiO¡^>µ\x000eï2<"sÝ³BVB½Ù\x0000\x001cmÎ=³W-\x00196\x0006yäw¦y(ÛÓoùþ´»Ö6bO#¦\x0005)\x000e.Á:åwc<çQß]Op±G<Én\*Ä\x001aXè2Äþ&¥8ÑØ\x000eTu5^Q9þè?N\x0005JZ
²%ÆáþEZEÝ8ííU]v;U|ä÷¤Â$W¤»x*£h÷\x0014ÈyÆsö«\x001aÍrN;\x0003Q&@SßÊV¢fÒôU\x00039Èã\x00150Ý 9ÎïNz
­\x000eKn^¤g§\x001fOþµWuFÁ\x00046=*\x0006ÐË[vfWLø\x001dÿ\x0000*ÜÑQÃ¸ Ö³¬Ü$KÏÌÞÝ­-)±ryç\x001d¿Æ\x0012¢õÐF.F8\x001cÖª\x001eü÷æ³!}×\Ç½lÚ§ËÀíß¹©E³7TB\x000f~÷Ç§õ¬eRÒ\x001bN9èkwT\@Î;bÂ:4¾ ñ6¦[æ^\$ p	ùû\x0000	ü*¥.H9\x0018Æ\x001cÓHú;àÆeàï:õ8½Ò=ÖHå¢QÓþ\x0004r}÷</p><p>ùÝÛt>Õ]Ä\x0007N¹Àöæ¾ý¥µ¨4_\x000bèÞ\x0011Ó¿v©# 8Û\x0004*/âÃ?ð</p><p>ùö>G9àW¼¯Qõ;*?u"þ§O¨ß[YÚFd¸¸a¼ìp\x0007ækÞôÏ\x000bxoÂÞ%»Õ~Ìaá\x001d9MÜäö»ö\ô9\x0019PF\x0007f}+Îþ\x0010jN­^jÚ¡2^Z[1Óí	3Ü6UT\x00100\x000e2\x0006½ÕÒü^½BðÆá\x001f4K©Ý9Õ5w^²Ï!$/¿ÌN\x0007¢%kQ¶ì](¤½NÆ\x001aü+ÿ\x0000Oj(¼Câ\x0007âs\x000e\x0014#HwJF;*\x001dðkäE|jNø\x00041jïu)o\x0019ö_É+É\x0014a\x0014K!rØ\x000c>À\x0005ÍôÙÀç\x001c\x001at©rE¾¦s©y¤\x0005à\x001ex\x001fJÎº<å'±­%ùr</p><p>ýïóùÖ}ÈåqÛóü©­Ío¥ÆZ&é2ÿ\x0000up[üÿ\x0000\bp_\x001c·oOóéM\x0011ù	ä°]Ü3C\x0007áýiê¹áGQéÏÒ­èg\x001du*¸\x000c\x0006@çT¶ÄÇË¸\x0011§¿<~4ù\x0010î#4å\x001d=³Þ¶µBSÑ/å´]ÆèÊ±\x0010H0IO÷×¿ÔWCa<R+Ä\x0019\x001c\x0011Ã/\x0001°xÅqú\x001d½Üú¼6QK%ÌåF\x000b\x0016cÑ@ï]CéwVz«iwÐ6¬FFlæ!\x0015\x0019\x0005O \x0013×\x0019Á¯_
÷dx\x0018ü¶KßÆµî\x0015wäeF8çÛçÏ5Ð\x0010±J²D\x001c\x0010GûÀ×+£Zj÷:ÊXiR> äâØF\x000bp\x000eIÎ1ë¥ZY¸ÙmgI \x000fWÎC\x0000qúï´G:S»Z\x001bË1.­3Ä\x0019HD	ÎqÈ\x001fýz½©jQ\x001cd\x0012È0UäB»ö\x0007\x001cc½sv\x001có¤h\x0014»º©\x000c­\x001e;\x001e~j\x001bûÖiOçÆ\x001fj°\x001d\x0000à\x0001¸g\x0018üj¬f/Ï©¨°¹-+\x0003\x00047\x001d}:å/%-&Ö¾ÕôÜ\x0000\x001dÔ×7	\x000bÀ<çwP?ÎjÍ¾M§#d\x0010\x0007\x001dxÿ\x0000"¡¤´\x001bCï´K{+YîÂÅ\x001cØØÅ°2sÆ\x000fçX/ku5Ñµ·Yå9!bBÌ@\x00078\x00035Ø5¾±¯ÝÙøwMîÞF_*!Ï\x001dØÀu$ô\x0019¯EÔõ
+àÎ6¢¼7Þ6¼mÕöÝÉd¤p {v^ý[</p><p>óç^ÍGvÏ \x001a\x000fÞ\x001f9Þ³ÂG-ÈÉ"²g<ÄñíÒµo¤\x000eîYÝòNORNk:XÙ³òûà\x001a¶M\x001cm÷\x0015\x001b\x000exëVd\x001c÷úTe\x000eÒÄ6ÜõÅc8Ic\x0003´ÜúÔ§iîE0ííÆ¹¤h2áÁ58{aÝ±õÉ¨>PG\x0004hÀÏ\x001f­c%sHÏt¥¾UÀ¯@Ò¾*ëZ\x001fSÃ>\x001cÓHG,n¯­T¬ÎO\x0018\x0007\x001c`àqóÜú\x0001HI¥as=ÇHí#³»\x0016f9$}éw®×Áß\x000f®¼S¥É}o®øvÁRc	QÔV		\x0000\x001dÁOo\x0019ö4\x000bVÌÝfÚk\x001bË;+<nc\x001e\x0008u$\x001füx\x001aÂ>%½ð¾µgªiþ_Úm%\x0013&õùX AÉ\x0007Ö·¼q¨\x000f\x0015x¿TÕá³\x0016{9B­¿i q\x000cääç\x001dMa¾\x001caá\x000cg`9cj¨ÆêÌ¹¶¥tRñ\x0006¡>«­ßêÖk¹o%Jª³±ov\x00005"\[ÞFYr\x001dGgî?\x001eµb;ö;«h\x0010\x00014A[q$FÜ\x000f×\x0019\x001fE§hÞÚ|¬\x0013\x000c\x0013ýÆþ\x0016ÿ\x0000\x001fjÖ*ÞéõJfh¶\x0011»=1Å\x0004m\x000e\x0007¸Ç½XÂXî\x001a&C¹xãkÚË\x001c?½^G¿"º	>¥½:ÊëP»·µÓíâêv\x0011Å\x0014i¹Ý\x0001@õ¨µ»9lîåµºK{«whåEÚÊàà;\x001cÅvß\x0007n\x0016ÏÇ¾\x001d¸'hP$öRáIüû@Ú\x000b?%T\oºóxÿ\x0000i\x0011óúÊS×Ö4/1çPH\x00169P¨öâ­iÚ}Ö«©ZXéÐ½ÅÝÉHb\x000f.Ç\x0000/çYå¾bÀà\x000ek´øKªXh¿\x0011¼9«N°XÛÜG$²H@3É\x0003g\x001fÎmEØ ¤9­OO¸Óïnl¯¢x/-¤heñ¹\x001dI\x0004\x001fÇ5Nßå}§¦qzé¾%êVº¯üG¨ió	lîµ	æ@\x0008\x000eääg¥ríýñË\x0003I6ÕØKIhItÁçb1È\x001fË­\x000c\x0008HÏSÏåQÊríÎ@5hA4vÜ<2\x000bw,!C±c*\x000fB@#§­Q\x0016»:Iü7u§x\x0017Lñ+ÜÆaÔ.^\x0004·\x0003æ\x001bw\x0002Iÿ\x0000Ò°)/\x001b\x0010!3\x0001¸1À¯Døÿ\x0000bøkðûNQm^íûà\x001cÿ\x0000ãÆ¼ãO¹Þq,,C\x0001Ï|ÔVt*9+³zôã	¤`|«\x0003÷Æ?ÏzÑÓA\x001cc¡úV@c\x001dË\x0012s¼ç­wÿ\x0000</p><p>môëï\x0019hÖÚ´hö2ÝF¡È\x000c	Æ\x000f¶qÒnÄR±m\x0010[ÈàÖõ\x001bX\x0003vÎOë]÷í\x000bá};Ã>6µ:E´v¶÷Âo*>\x0015\1VÀì8_Ì×\x0011k¨ÈÚ,Zr¤K\x000cs¼åÕ~y\x001dWæ>.\x0000\x001e§ëQ\x0017sYE%{\x001a !r§§JO\x0008xëÁþ$³Ö¬bI \x000fû¹	Ã\x0006\x001bHÏn;Òê\x0019ÈÏ?jÁKIî+n^hÙüRGIã/\x0016ßxËÄ3jÚ"Ë TX×;cE\x0018</p><p>3øúPAÂ\x000cã¦}¿ÏJÅHÆ\x000f\x001cv­¨ÈÇ\x0000:f³PPV¯´çwgUðïXÒ4_\x001biþ IÚÆÏ3\x0001</p><p>o&P?wé\x001f¨\x001d«'Rñf©ªøÛP×feón$i\x0014¸F:*÷W\x0000õë5£IP,#¯\x0014y+\x0000Ä|\x0006õæ§Ù¦îjª´´&i\x001aC#ÊÛ$Þ¹+X÷js(<ôýkª\x0007\x000b)\x0018û½qV¾\x0012x2çÆ~9]:\x0010él1%ÔÃþYD\x000f'êz\x000fsíN~ì.D\x001f5MM'á·«x\x001bPñDfÞ\x001d:Ò7yìCN¨2å8è0G=O\x0015À:\x0008ÃM äª\ç-ëø\x000e~¸¯¤h?\x0017[XXAà\x000fìÆÝ\x0017í¦3¸+\x0017Ó¹õ8\x001eµóeëùò\x0006\x0014\x000f}\x0007ÿ\x0000_­cM½ÙÓ/y[ú±\x000c+ÏbÇ¿ç5aBî%'ßùSmPc¸=ñÖ®2àç1Ç<\x001aw¸$V~IÚ8éÈãõ©m¢f*\x0014\x0012ÝqlªI\x0007å?é]OÃ½rËÃ\x001e(²Õµ\x001d4jQÛnuÉ·\x000fº\x001eTúý{</p><p>zØ4¹ì\x001e\x000eÑ¬>\x0012x]|Uâh\x0012O\x0012^)M:Áøh²:·£c?Â>^§\x0014×¯õ/\x0012ëóßj\x0006K­BîA îfÎ\x0015\x0014\x000fÁ@\x001eÕ½­xïÆþ4P×\x001brI* \x0018í\x0010ÿ\x0000ê×ð'ä^¯ñ\x000fLÐþ\x0019kzî
·öÄjº=\x001bÕ¶âK\x0007òQëSx¶Í\U¬úÿ\x0000V9­[]\x001f\x000fô\x0015ðíÔÒ^xî
¥Ôn\x000bØÀFVÙ\x001bø>÷?ÝÇ\x0011ö!<-u¥N\x0011*å\x000eÖQèGjåo.e¸¸âåäi\x001d¤ä$³±$O¹¤y-åY ¢O\x000f\x001b\x0015oÌW©Ä:\x0011äã°P®¬¬u&ºlîÂÅ\x001cóÙPÈyc¸©"Il
Á%@ÛwM0VcÔàc'¯S\Ó^%Ö\x001bPOÞw¸·!\x001fêÃî·è}êx2Q£â;¸Û3åL¦v1ù¾ôá\x0006®]R\x001b\x001aMµPfUfeè\x0007l÷=*m\x000fG¾ñ\x0006©\x0016¥Û4÷7
ò¨Px\x0007,~è\x001dÏ¥sí<±HÑÊ²°\ÀëÈ¯IÒ>"h¾\x0010ð\x0014v¾\x000eY[Ä÷ñÿ\x0000§ßÏ\x001e<ö#Ï_lqÜóÀõd£î+²°¸DæÝGd¿\×tßÚKhº,±ßx²â0··Ê\x0006-Æ>âû ~'°¯\x0008Ô¥7W\x0012Ï+$\x0019Ý²å$O$Ô\x00177ÒI;I,¬ò9,ÌääROSÍVi\x0010w\x0011CúÖThª~óÕ³§\x0011^U_*Ò(r<\x0010É½ã\x0013/ÝÛuÏ4L4yÊ\ÀHç¿Óéÿ\x0000×¢Þ\x0015»\x000f\x001a2çp`GOpk*uXätg\x0019\x001cpzý*ç\x001bêU</p><p>>é\x0005ôvñÎ~Ï)3\x0012¸ÛéPBhQP2^ íøSe\x0007¨\x0003=øÁªÏó\x000223YM]Xí³¹iõ6xÊ\x0018¡Ûþà9ÿ\x0000\x000f¥f¹\x0004ðJyN9ýi\x0003µrJ67æor2jx¢SÛ\x0004æ¡?ZLV,¤Ë\x0005-Ô®f>ËUØäfJw\x000e´dÑÞ¦ÞiWtp»¯ª©4íq\x001dÍÍØ·÷\\x001fïw¬içó\x0014ÈÇ9<äúóüóV$o1BÔ~¿çùVmë\x0019GÓüÿ\x0000õÕ\x0008ØÂsrvDV*ndcÑ³èÎkzÒÖ#\x001ee8V\x0019À\x0015Ïè²\x0004¹>¯Ò¶÷\x001eTç ã®3Skê_2ë¹·[Á,\x0008\x0015]$à|§òþUÌd¸\x0017·<sÇô­$|Ås\x0017;<ÁÇ9_ÿ\x0000Y¨¼\x000bi\x0006«ã-2ÆöWÚêæ8duÆåVp¤ñ\x000f\x0019ª©h+ÒN¤¬[ðÌYÝA4AY¢$@Ç\x0003*C\x000få[\x0013µÅñoïµËdµ{­èñÈd	µ\x0002ýì\x000cÒ¬xÿ\x0000BO	øÏXÑ-ÞGÒ}±3ãyYr@\x00198aÓ\x001d+«Ä¹8b¾\x001e£ð¬ã\x0015/xÚu\x001d?tÁÔ\,Å#P«qþ4±Å	äåOõÿ\x0000</p><p>õ\x0017øE-ÇÂ\x0006ñÊj[§\x0013ìû\x0017³Îò²_?{<ôéï\\x000f-$9ÖÚA\x0007\x001e¦¥4Û±R*W3¥µ}Ê\x0006I?/=êÚØ¼zEÃ;í_65#ðcS<Ël!U9 w«W1øB'¸\x0003©G\x0018ãÒ\x0016'ùÑ+ §­íØç</p><p>îl/$\x0003^ãxÍ§Â¿ö]\x001at¼Ô\x001dß*þ\\x00059På\x0003$ÆGZö\x000f\x0016Q7ü
¢\x0011Í¦§[\x0015ïºF,Ùÿ\x0000¾«</p><p>¯c£\x000e·1>;¿­èjp:T\x0011è}?A^fWiõ8ú×¡üf¸ûgÄ-a\x0013$\x0000g² þ¤×\x001d\x0015¡pI;T~\x0015xxZ\x0008T¯Qð\x0007\x0019\x001dkON¡ÍG"U?.	Îr*¨HÓó\x000cð;?¯ù5<I|ÆB@;f¶Q$ÓÐèu-wV×&ç]¾¹½¹	åî¸rì\x0014\x001càg§ZNmÊO ús\ýã1V;±úWAb</p><p>§Ì{ôÿ\x0000=j\x0014RØÒSrÜÿ\x0000¯N+\x000eN[Á=zÖæ¤</p><p>\x000fn\x0001¬vP®N1ô?áZ#KQ`äùö­Æ\x000e8\x001càô­¯~\x001a\x001e)ñ®¦I\x0013Im$»®\x0014>Ò"^\ätã©\x001dëoâ­¦øÊþÇÃ0¼66ª°º´¦@f\ï ·8É\x0003¯U5ÝÁ¨Üã\x0015\x0004óïA e\x0002î)ÏqåC\x00106ã)Ø÷$Æp\x0017\x0000t«ÿ\x0000\x000bþ!êþ\x0005¿Ö#Ñá´ß*\x0007iÐ\x0019]Øa÷\x0007H\x0000c|\x001c¦¹í4\x0008õ	ælp±Sëø9G:%Ë-
­vækdkÌÊÆI¤cf'''êIúý+:ÒÆK¹.Gæ8éÅX¹MÄ6H\x001dqïEäöq\C\x0003·1ùRgrÿ\x0000\ïÈîW¼-cÏ'\x0019ÿ\x00009©åP\x000eG\x001fÖ¶ü	¢GâO\x0011Øéo{\x0005Nä5Äç\x0008\x0004L±Æ\x0000õ=kÓ> Ú|9ðÇn´}\x001d\x001fYñ\x0003®>Ü%È·n9È;à \x001fBj</p><p>Hñ$á÷\x0010\x0018~às÷OsÚyl >£h\x0003(7r}OJÑ\x0018ôùZ\x0019ÃÈ'¯Oþµzÿ\x0000í\x0013¨Yj:¶wcs\x000cæm26o-Ãcæb:¼*ñxØîèqLTÄ\x0012\x0006Ñ××5\x001c©ÙjW'æà\x0011èxüêU_³Ï\x0018\x0000qLÛ¹°OSëS"Ã*:Ý#\x0006Æm \x00009\x0019ëÖ ·ÊÊ\x0008ô=
J\x0003\x0013Áú</p><p>zÎ3õ­\x0011aDUA+\x0010#qÜ\x0007Ð\x001câ¬m¦\´\x0018cÔÆqçR$jNGQW``u?A[FM\x001có^æ4º\x000bû½§°3øqT¥Ðµ$ÎÇUí#ðù±]z&\x0010</p><p>öäÒ0`©«ö!ScKÕc_øôvÏR¤\x001fëÒ¨½¤\x0000ÿ\x0000Bº?ð\x0002qùW¡ÇsÛ\x0006ÛCp\x000eZ´\x0017*]\x000f1k\x001dC'u×ýúja±¿`BÙ\ëä·øW©\x0002ã¥N\x0002OãI¶Çí-ÐòOìQòWN½#Ú\x0006?Ò¥Ãú¼¤mÓnN\x0006èÊÿ\x0000:õ¬\x0011ïH\x0006\x000fËYû;îÁ×k¡åËá\x001dl2ÿ\x0000~E\x001fÖ´,¼\x0005©Ü6$Ò\x001fc!cÿ\x0000?Zô\\x0000	ã>Õ-¾ààcëG±HQ¯&ìÎ\x0012ßáðó</p><p>Üê8ÁÁ\x0011C~¤ÔÁ:=¸a ¹Çi$\x0000ã :ôo\x000exQ×µ\x0003\x0006jóJ>ô\x00160{±è+CÇzW¼\x001f \x0005Ôu)gÖ&oXþ[dÁ\x001b\x00123!Ç§¯nðÝ8½MU:³M£ÊK°µ}Î\x0008È\x001c|¹?É©T°P\x0001l\x000fzÉÕ|]¦£H¶-Á\x0000aÀÚûgùVQñÎ\x0016ÁH\x001d3/ÿ\x0000Z­TL½Þã\x0010®Ì\x001eüôúÖF¢Nì\x000eZÑ%×w\x0004\x001cv\x0007üö¬ËÂ\x001f8ÛÇP\x0007J/¡Q½q?ññ\x001eõæ¶]þë
ÀgµcY)Y¹ã®=«fávÄÁF\x0002\x0010WÜ\x001e(Ðu7\x0018\x0004¾Ý.U»ðxþµSJ¬u¸åQ\x0014G]§?Ò«ÜH\x0008<Àÿ\x0000õ­//ÍÔ×Ì\x0007Ë\x000c\x001bû»çéJ­¥\x001b\x001aPN2Lö?Ú=T|Gkè0êV6×QÝvÏþ:+Ç5\x0007ÚÀ\x001c\x00018¯aøäâóÂß\x000eõs÷®4sjç°xJgõf¯\x0015¾&hÇÌ\x000f§\Î÷K®­4Ï¥<%x?²N·\x001f£ì¯"ã=\x000f\x0007þ=ú×Îº3¬Dçw8>µmsr=¼sÈHÀ¼{V#¡#¡"¯Þ£=¥´Ìw6\x0018\x001féSF\x000e/SJÕ\x0014Ö\x0010ºÉ\x001dÛ0;U@÷®ú"\x0007ôÙÜk\x0018÷	\x0004]ÿ\x0000àF°a:~¨à|«°ò=k°ñ=¸¶ø'àVÿ\x0000«ýFoËÊOý³³±¤W-;®¨ÄðVuâ\x001dRÓH°KqtY\x0015w\x0018ÚK\x0012O@\x0002^½ã\x0006ÿ\x0000ÕÊÒâÔ ^\x001a@</p><p>ïòÌV\x0007ìÙiçüDÓØç1ÛÜH\x0001ë÷\x0002ìõìº\x0006¦ëß\x0012¾ øTWfÒ¦û=»+\x0010#dk·\x001dHU\x0003SXUÛHÞRomÏ¼Uyöß\x0017k\x0013±'Ì¼ý~r?\x001e\x0000ª±8\x0011±#¢ëTælÝ¼9r[=Oÿ\x0000^§?,2\x001cqÈÇJî¥ð¤yõ×¾È1÷G8,kMm±\x0010\x0003\x0004ã<t5\x0005"gXðNrFEo\x001bs
ÄjøË lt\x001eÆØS]Q`\\x0010ÄÓèm\x0017\x000cg¸ªB5ûJ0\x001b{\x001e+OOSN\x000ek4QWVR\x000e1Ðþf±F\x0004\x0007\x0000\x001e\x0008­ÝN<sÓ&±\x001b\x0001ð¹'8àÕ­Q\x0012ÑóðSÁ\x001f\x000cõï\x001bÜ\x0000/nÁ°ÓC\x000f¼sÜo\x0004ý#5äm#M3»±g~K\x0013rrN}ÎMV:ëé±iò^\Ic\x000bÝ¤c\x001a¹ÎæUè	É«\x0010®=qdÖ|6u\x0013VDl¤qÇ\x001di\x0019rI#\x0019ü*ÑL¡ëÇJ`qàd\x000fz³28×p`1¼çµsÖÅdÖ$Pp¨¡TwÅtÉ\x0019\x0011¿\x0000\x0016^§Ò¹­=³­\ÉÀæð\x001f\x001afê»xäÿ\x0000µQ\x0000à\x0016÷ïZ\x0017#hÉËg õ¬öËÇñ5Ïc¬±\x0007</p><p>N3Ç|RLÙ;qÎ=*{1µ\x0018\x0018^\x001aRÇ\x0000¾¹¡DnZ\x0010±.x\Þôí¥¸\x001d~¼\x001aTÆ\x000e
\x0000\x0012ÌHäéOa\x0004jX</p><p>2+¥Âz>\x0013ÄW\x0011Ç\x000e,ÿ\x0000gÈøcýä\|Ê0rÙìzÖÏÃo	ÛjqÜëþ'í|-¦×\x0012dæâNÐGêNFqë§ß\x0010üauã
Y%5µÓíÉ²²î[Ä8\x0000\x000e\x0003'\x001dè\x0005MîìµÙÇ®\x000b}p
L¨½éíTò9\x0019ã­L</p><p>\x0007|b·±Qê¿/^=jHÔç#z\x0002\x000cöÍM</p><p>|¹\x0000`ó´øïô\x0015x\x000eSùUxÂ¨ç
K\x0011ù\x0007\x001eµW3¹4`¶w\x001e\x0005,9=i\x0000\x0000î#WPT·\x001cÓDÀÆXuæAÈ=³ÈÅ Ë9ÀëÖ¥</p><p>ÁqßÒªä1\x00061½}GZ5\x001d9àõªóÜÛZ®n®a\x001fùèàgóë\ýï¬`wKX%¸Çñî\x0008§ó\x0019¦ää(9lu¤Ãm(]Ý:ú\x000eMq-ãèÌLFÂCÐ\x0019_ÇåÍsº¯uMC*Óù\x0011Ï8>Qø§ñ5>Ú(~ÆLô½CS°Óãúî(þyçsß#&áíZ_\x0012ëqé\x001e\x0015Ó®õ+é9Uâ4P\x000f,ÌOÊ£×Î¼lNK\x0013Ö­éösö6òâÒ}¥<È$(ÛOQØúV3­&¬©ÐZr>±ñ÷ÄÍ/ÀÚXÒ\x001cYO©Ä¸:>ì-¡úo)ù¤on3GzùÆ~/Õü_¨\x000b½bçÌÙ$\x001bcº:\x000e5Ï»n$}iµË</p><p>J/»³²uÛ$tBQÅ\x0002ÔÀúóÁ\x001agÂ§øc\x001cÚê@.Ì,n¦rÌ\x001c\x0003/\x001d@þ\x001cdz×Ì\x0002ÒÈ­"nÊçw¦@õãó5¬úýì?a\x0012ÿ\x0000£\x000fnÏcéYp\x0012®\x0000Ú@#\x0004:p§%~czµi»rjzWÆß\x000fXÛkz>½ YÁi¤k¶\x0011_E\x0015¼acP\x0002Èª\x0007Õ\x000f\x001dÉ®</p><p>æ=èp@%qÏÓ§ÿ\x0000ªºmCÆSê^\x000fÑ¼3ui\x0011]2y&·»Üwps\x0011\x001d1ú-sWå²9\x0005qÐ\x001f­kOE©ÍZÍÝ\x001cã±8\x0018=ñþs^ùàÑá=CàF¿\x0005âéÐëÖ£ÏYJn0¨~ñ\x0019\x0004`{Þ¼BîÜFòo\x0007L\x000cqHÎÍ¤ásòJG^ÿ\x0000</p><p>R3.E
Í
næ[«\x001bi|Æxãg@¥T'\x0004àvÏ_zÇó	\x001b'^Õ{OQ6y\x001eÒY\x0019$ÇR9Áþcòª0!ó\x000fNÖ´µfR3w\x0016(ðw ÊÆµ¦\x001b´¸ù9\x0001þ[éÓ®u\x0007\x0006Û	{ywmõÎÞiÙÿ\x0000@\x0018ÁÃ0é×\x0000UibetìË6Vûü+¯Oû³\x0008¬S«ê\x0017\x0016\x001auÕÜÒØXïkh\x0019²°ï`Ï´vÉ\x0019®³Ikuð\x0017ãyQn\x001eHLq±ùq;×\x0019k\x0017'9î=x\x0015Ë\x0014ÜäÙÙVIS»\x001eçû3J¶&Ôõ\x0007L¥Ò\x001eqÁ	\x0019ú\x0003]Oü¦¿Âo\x0017EÌZÍü÷W\x0001\x000cB,ê\x00150ØÆ\x0007#×"¸¯Mö\x001f\x0005xûP<4zjÄ=2Ë#AUþ\x0016øbo\x0012xkPÑíä\x0010ÉªßAhe#pDD29Ç|\x000cþ8®:¯m´b¥M'×_¸òu\x001bæ;G\x001d\x0007\x001fÏð­\x000bvÛ\x0000[üÅv\x0013¼\x0002Þ\x0004ñJéßj\x0017qË</p><p>\#íÚpÅ\x0018g\x0000åOç\þ¡oòGêNsïµèÑSG^-KÞ!Ñà\x0006õwp\x0000</p><p>{ý\x001aÖºq>§q"&B¯°\x001c\x0001ù\x000fÖªéÀ¤²0\x0018$à\x0003V-~k×=»UI</p><p>2²²\x0017Ë?i^9Ï\x0006´ôø¸r8ÉÆqþ}*« 3ÆS®qÍlivòÈb(ÚIª/ñ18\x0000~b³z\x001a%vu\x0003O¶Ó>\x0018êú¥í¼R^j®gæ.Z5_Y\x0017?@¹\x001dÇZòg\Ì[ø»\x000c+×~2\¥¥ÞáÛW
m¢Û-»û­;|ò¿âHüs^K.UÉ=\x0007 {jtWVN!­\x0010"Ã\x0019À8\x001eõ­\x001a`qòãëïYP¼q×\x000fJØ·\x0001È\x001ctª\x0010%1ª\x000e}Æ;ÓBeùáFK\x001eõddûÒH»PqË|ÇØvÿ\x0000\x001aW,©ÉYY\x0018Rsæ¬­e·ñ\x0005Ì\x00171¼Rª©(ã\x0004\x000228÷È5ØÛ8·Í\x0008\Æ7(À °Á\x0019\x0007·|w®BÖI'ñ
ãÎí$\x001dò;\x001cbyÉ¥-WO©¡xI<ôÇ§j£ú^©x¤c\x0000}sYÛp@\d\x0008ÿ\x0000?bÞº\x0017-ÆcãÇ\x001cT\x0013ç.OAÐw®·Mðü¾
»ñ
ÃÃk§DDp¼ä»8Û\x0018ÇÌF\x000eON\x000f¡Ç+:üç\x001fvîÆâÒ+¢®3ÉÇz¿¢Ce6±g\x0016±rösÊ\x0004óÇ\x0019v>¤:ß|UU^\x0006>P1È¦\x000bêqÆqN×%;\x001d¯Ä\x001f\x0017.¿-¦¢Âl<5¦\x001d êzæWõvëíRIäÖ?<zb£H8#\x001csVÒ.\x0001\x0018ªR	MÈ®A-ÐÔÿ\x0000O\x0012çosè
\x0002?\x000ct«vñr§\x0000\x001eçÖ´Jæ
B\x0008É_Ï½K\x001ae°z\x000fJ¼°a\x000b9Àõc?\x001aÂÕµí>ÃtpK\x001cÓu;\x001b*§Ü¿AW¢FMêjªüÝ±ïÍ+ìNd*þû\x0005¯7½ñ\x001e£p\\x000b¹\x0011\x000fðÄ6\x000fÓÈWËÊí#¬Ç$þu\x001eÒÅZç¬Ë¨ZDHêÝ\x0000ç\x0014Vuï´v*²Ëqÿ\x0000,Wú¶\x0005yiTdñRê\x0002ÖÝøÒrÄY[G\x0018ÉÃÉóvã§ó¨l®<Kâ½F=;M[ËË¾U·µB2>Æ=I®Çá¿ÁÍKÄ#[ñ\x0004é x^0$úï</p><p>dOúf\x000f_÷\x001eé]>¿ñ[Bð66ðO\x0016áËráwOp}W#õ \x0001\x0015ª·¢6\x000e¬ñ\x001dJÔ4-^ëMÖmä¶¿·mÅ&7)Æ}û\x0010sY½êÖ¡{q¨^Mw{<\x0017S1y%3±êI=MVE.À($\x0007z~¤;_@«N¬^Çg¥YÜÞÝÉ÷!·¤vú\x0005\x0004×ªxOàÌãM]{â&£\x001f|>0GÚ?ãêqèõ\x0007ê	ôSWõúoôé´_zBhö¬6KªÜ({Ë|íï×8Ï\x0001joØ¥\x000e¬ñk«y¬îæ¶»H.!s\x001cH¥Y\x0018\x001c\x0010Aä\x0010A\x0018­\x0017ÛÙ[ÞY&\x0008\x001bOµy\x0000bÛ¤h»sêI8éX÷w\x0013]ÜËqs+Í<¬^I$bÌìNI$òI§ê2\x0019&\x0019pø\x0017#Ù@Å>£M(´T¥\x0014</p><p>îôï\x0005[iv0ê¾=ºJ²\x0004Ú|@\x001bûÕ'x\x000f?¼î¦BW9ß\x000cøoUñ. lôkFDS$¯±Ã\x0018êò9ùQG÷\x0002ºá§|6Ñóe­j^ Öoãÿ\x0000[s¢c´ÏuC*p\x000e~|\x0000{\x000crq¼OãKNÃû\x001fIµEðâ6õÓm	Ã·gÏÍ3ôå¸\x0018ùB×"in=\x0011Ó\@«3RcbqÓÓùSP¨!³\x0013WöXH\x0017rIÉ\x001e×ó®ãÃ\x0008|I¯èrj\x0010D-d\x0005íÄ¯µ¤õÀ=»sEtÖ©</p><p>jòf4©N¦Ç!¦É§ÙiòK$l/mã½Ô\x0016Â³:2±8åZ2\x000f¸¯¡<=à/\x000føÃàLÓéÚ|'_$\\x0001ûÓ:eçû¥p\x0000éÈ=kÇµ\x000b	%øz±ÝFÑßh\x001a¬#\x000c2Cp¥×9ô'\x001fW®àïÅsàHn ¼´òÊè(\x00041È:0Ïb\x000e\x000fÐzb¹îæ®Ö½ägê)å88;H\x0004qéÅG\x001a\x0007ÒîÑG*Qóß©^¾Ö®çRº¼\x0018\x0010ÒK7?X´{\x000fä+;KÈuîñ7O¦¥tFéjqÕZé°h\x0000ù²¯\x001f¼B\x000e{ê´»o\x000c¯ÃÝV{¹\xL«m\x0018È\x0002<®p1}üý\x0005wß\x0005¼\x0011¦ë\x001e\x0016ñ£u\x0014s\C§46èÈ\x0008FVo1}\x0018\x0014\x0018Åy4©ûò@ù%\x001bÀÿ\x0000ysüêa%Qrö5Ò¿kß¹^k»§
<J\x0012ÏÏûFÍ!öíÎ~©\x000e\x0017JB¼ì\x000f\x001dð*6fPy]ÜqÓÚ§\x0007O3òùñÇD­ÒÒÇ-I¹4Ù\x0015»n¹e\x001b]p3é*ö¥¥Æy 'Ï¹\x001fç<ÖVJJ\x001b8Æ\x000f=zhÁ¨Ke-À¤ \x0006\x0004pyÍg4ÚÐÚ£\x0019ûû\x001dï¯e°ø=­\x0018¶í]Q,ÝdùknY±ï9÷¯Týl\x0003Cg0\x001f,mwqå"_Ówë^/~ÆÓáGá$nT¾½ö¬Q~´¿
þ#ë\x001e\x0004»m7É9cò\x0013î*\x0006íÀ®:\x001cç?ZóêÑH]os½V_'è_\x0015Bx³ãàÒw7×\x0016ö,TàQÇæõÂxª\x000bH5Ëû[
æÎ\x001b\x001dÇqÚ\x001b\x001d{ô5µðþmOâUÿ\x0000597ÉeiwªÊÝ\x0006â\x0008þr\x001e=«7²É:´ªÁä;Û=äû÷5®\x0016ñ|¯¡'Ù¦ÖTvûÄûÔú~\x001aè\x0010GÍÇy_å|\x000c\x001c\x001cõG5Äg¯Í]r8a©¿$`^Æ¹äó]o5;m\x000fÄVZí»\ÃjæA\x0012\x000b8S°äö
øW/*\x0003z\x00186*üñe\x0008\x0008Á\x0000ñYµsdìîVñ\x0014òß\Ïsq',îÒÊÝrÌIcù\½Èo0¦\x0006{zq]>«±W(\x000e\x0000Ï<ó\Ä\x0019YÏQ>µ¤\x0015Wv(ï´\x0003ó­1z\x000fÖ²#ÀéÑr~¼ÖÔ\x0003j(<1\x0000ñI\x000eÅ¨\x00143|ÃäPY¾¯ø~4×ýáÞÝs</p><p>a \x0000\x00119?îþ¿ò¦d\x0013Â´-;ÚÚMtdKt,B=Tuf=õ?Î¨xGÂ_n»×õ9o£IÓ×oÚ6Ù¤ê\x0015C`þÀïZze¥Æ¥}\x001däùar@õù½2~?õkk[Ë_\x0007è?K\x001bîd\x001fòñpy%¾?û¢°«'ð£®!nyô9Ñï2~µ¿ðãMðõÝõÕ÷u\x0004·ÓlQekU?¾½'81ÔõÁ\x001d2HÃ¼ùÇ²ÕDä0ã\x001dirè\x001cÖw;o\x0018ø¶çÅWë4%¥²ùvvQàGm\x001f í\x0006Oò\x0015¬xbÿ\x0000KÑlu=GÉ·[çÅµ¼#Æ|Ðá21rr01ÍXðÎ§\x000e©ÛßM§Ûê\x0002\x000c°·¹È\x001f)`:àóøüj¿¬Þë½Æ¡«\½ÅÜä\x0019\x001doE\x001d\x0000\x001d\x0000\x001c\x000f­LU¤¤nÌµSñMe=\x0006síVã,\x0006W¡îNj\x001bH"i%eDNäô­v9Ûº\x001doÎW\x0019Ïj÷X±ÓÆÙ&ß(àÇ\x0010Ü\x001eÃùÖ\x0016­xöû­H­\x001b43ÿ\x0000­¯\x0000|=Ä\x0016\x0017Zî½|º'¬óçê2¦ã#ö$þ7?§×\x0000Ëè\x001cZXÄºñLìçìG\x0012¿Ì~¾Æª\x0011êÅ\x000bÆ_@¨ *É¸\x0011¬Ò\x0008 Çi`\x0001#<d\x000cãó5\x0010§ve×RýÕÝÅûÿ\x0000¤ÝK)Îs#?úÕb}\x000eí.ÒÚ$ûLï÷\x0005¹ó7ý6õÿ\x0000ëWwðïàî³â[?íbht\x000f\x000cÆ7É¨ß|Õ\x0014ãwÔà{ö®³Pøáo¶é</p><p>4á=ñ\x001b&×¯|ï\x001aÓð\x0003ºzÖrnú\x001d09_2Ôðw·\x0019«\x0002ASÔ\x001eõ\x001eÃW®õ\x0019¯¯¦»¼¥¸FW~K3\x001c~¤Õ«Anü61Û?ÏôÜ#B5>\x0016býk²ø_â=\x000bÂÚìt\x0001­ùq\x001f²ÂòmD `A\x000c;sÓ9ÇJÈL\x0006C°R~^#©ç<t¬ë»GA\x0003Üt¦¦¥¡2£:zØì>"üKñ\x000fo|Í^è¥ª\x001cÃe\x000fË\x000c^^çý£Íq\x000eY³SÃ/\x000b#[ÆûC09\x001dG\x0015[¥4"rmn \x0015ß|3øoà8o®­|;a¯9\x001fdÔ.Ø°´\x0018ÁÛ\x001e:ýìÛ¥p=ø«\x0010ÚI.\x0008\x001bWÔÓmu&\x0011¢O\x0016x«Zñf¦÷þ Ôg½¹làÈxAèª8Qì\x0000\x0015ÙÐ|=¨k¤Z~o-ÍÌu"BÄþ\x0015ìéðëÁ\x000e­RóâUû^j[CÇ¢YÉ\x001bÓÌ`~QøbzTó¥¢6XyËYhx7Ù§û1¸òdò\x0003l2m;wuÆzgÚµ</áSÄ×o¤Û\x0011'q<®#Þ1ÕäÔQÏ$û\x000cõ={â\x0006âí\x0013ËÖî-ô_	ØËO
é\x0011´\8\x001c\x0012ämEç>øBkÎüQãKÍbÍ4»\x0018!Ò<=\x000bK³È7\x0003|ÒÉ>w$õÆ\x0007\x0014ÓlÎP^æÈÕô\x000f\x0003á<0!ÖüB-¬ÜÃ{f\x001fóí\x000b\x000fÒY\x0007lªµÂêW×Zì×Ì×Ws1y&Ë»·©'j¾ryëM¦fØQE1\x001e¤Z\x0018®£ÇÊq\x000cþ5÷¯ì£±ðÖj\x0015bµ0\x0007L(¯ôYá7¶÷\x001dc\x000cÜc\x001d2+ík/\x0017èï E¨­äBÔD\x001cÀc\x000b}{b±Æ4¤½8óR÷;;êö-«üFñÆ\x0002þë]â\x000b|\x001fíp¿	?ð(ØÀ«Ìï|+=§í¼AçG5÷mn#\x001b¨=OL\x001cVÄ¾&ÇÆqë\x0005ù\x0017«v¨O9Y7ãñ\¯ã]å\x001a\x000fÅ\x001f	[\x0010ëaqý±§\x0001yL7¨\x0019ÿ\x0000`'ýõV¹¨¥m´¹+s_txµ¤d\\x0017QÊ~÷B\x0008ä~DÔþ\x001aðýÖ£®YYÛ(i&B¹8\±Ú2àB­ØªÈ¹#Ãü»¦êRÙê\x0010J®WÉpÃo\x001c©ãõ\x0015Ù;¥sÏM¨3µøi§êÞ\x0010ø«\x000f5+9äÖæ\x0004r\x000b$tn õå­hÁm\x000f3åÇ*HþUï\x0015\x001a;?Þ\x0011×b8ý¬îC\x001f÷¼³ÿ\x0000°¯1×,\x001e\x001f\x0010k\x00160 2E$j:ur\x0007ëÎ±¡e&tbStâq
¥É¹@\x001bxÇ_þµ2;Há·¸S.â²\x0012vôû¿á]§Äm\x0002óÃ:íæ}åùñ*8òßrá#\x001c\x0003ê:W\x0007\x0003 ¾nÆDü2\x001cWl,ÕÏ:¢iò\x000c\x0005°@'å\x001d½ªÅÝ«1R9b\x0007\x0000c·Z½b±]Ã8QÇ~zúàB±\x0014p;TXwJ×.øµ\x001e/\x0005x"Û\x001c	.\x000e3ÖIå?È/å\I\x00079É\x0004\x000eµÖx«VµÕ¢Ðb³ghm4øm\x0018²àïU%ñê2Ýk\x0012ÞÐÍ!8\x0004øúø¬ã\x000eX¤oV§4ô;¯\x00047öoÂï\x001ej¬v´éo¥ÂqÎ]·8üü«²ØÅ4ÿ\x00004÷D´{!\x0014c?ãð¯AÕ4æá\x001f4Jõ­^{?¼\x0017÷J~?*óo³î%</p><p>æA\x001cEU¹Áç¨ô\x001dë\x001a1¼ó:ñ/	5Ð¾Ô@ËÙÅZÒÈö7\x0007+¸\x00023Þ¤ÅæD\x0000c\x0019\x0007#©õ§%UÝ !O\x0003\x001eõ»W<ø»\x001d\x0005ÃùzÌÙ\x0007¯ÓÖï7'#oQÚ¹gmA¼ß¾pI\x0007òúVÞÎÏ±óÇ=q\x001b§ jÙ\x0011¯_¿zçfÁ\x000büæ·õI\x000eIÇ\x001d<zV ,Y¾æ}+H­\x000cj07?BqÉ­uf* æFÀ\x001cð	¬­åT ã×Ú¶¬\x0007\x0004eFÄ9êÇ¿à3ù\x001a\x0014X\ËX!;GÊ¹þèàgùþ5\x0013IÇ#'\x00199¤Uà¿óæ·ü\x001f£Å¨ê\x0012Ï¨º]ù÷r7M£¢gÔÿ\x0000 k9ÊÊìè¥\x00079(£gE?ðxeõIpºÆ¦;5=bÉÙàÿ\x0000ß>¦¼M\ksc¸®I=zò~µÝëÚ¼ºÖ¯s}?Ê\x0019vC\x0016q±\x0007AÔû×	g¬Ü®qòäÏùTB\x00164«RóPÈÕºbàw·øÕdRÍ}8íSJ7g?wùÓâNç¿8<TØ«¤Îm<·TUÎì\x0019=y'¯åÅU(\x000e[©íÏZ°äÈà~\x001fäW-¨ë,ÌñÚJ!N\x000b\x0003n¼éKa¶Ùµ}{o§C¾á¹þ\x0014þ&ú{{×;gâ\x0018Eä·:ºe\x001f¸·Ë\x0019õ#\x001cÖS}grîÝÏ<þ5«àû½\x0002ËÄ6^$²ÿ\x0000M.öÐ¸C+\x0001ò«\x0013ü$ã=ñY¹s"à¥	&;\x0008øa5]4øÃâ\x001dËéþ\x0012±\x0014KÄ·î:E\x0002úqÝ¹çWøãûÏ\x0018]A\x0004PÇ§h6CË°Ó ?º:\x000f÷÷nþÕWâ\x0017µ\x001f\x001bjës~É
¬+åZYÂ6Ãk\x0018è½\x0000À\x001cõ8®OnA>£\x0014µg'½üÆ÷®ûá_ü/áI¯µ\x001f\x0010xuµ½M\x0002ÿ\x0000g¤®\x0005¼mÎYÔõ=1Áú\x0003\
.9â¬çNÌì¾!|Gñ\x001f/|Ýrôt$Åi\x0016R\x0018¿Ý__sï\mtOàÍ~?</p><p>\x0011Í§K\x0016¹Un$!78\x0005Aå¸\x0015ÎRVèTù¾ÐSO\x0004m9W ÿ\x0000*d«ô/Zj/\x000br\x0003\x000e{~µ¤6÷0\x0005m¡ã9à~uÏ²\x0015<E%O\x0007\x0018¬åM=be\x001d%©«$hAÎN\x000eÐ	Ç\x001cöªSÄS ç½L%ó\x001069\x0007JvýËp9\x0019=)+£I(M\x0014\x0010|Ø¯eðÂ«Ë&-wÇºxgÃ\x000c¯p1<ãÒ8úóØà\x001aò\x0007À\x001b\x001f©­\x001dsÄÆ»*K­jwòF\x0011®%22@MT1)û-Ï\Öþ+é¾\x001aÓåÑ¾\x0016i¤[8Ù6§(Ýyqï»ø{÷ã¶Úñ}JöâúæIî¦y¦;»\x0016f'¹'jº1n	¡ïºcaÔ¬æ¬´DT¦\x0014»\x0005QN\x0000­\x000eQ(é^á¿¾+ÕíEýý´:\x000e0ZûX[ \x001eÁ¾cíÆ=é¾4Ðü\x0005¡hmm¤xP×|E¹}\x0004\x0002+$\x0019ùÝó1ÇB\x000e\x000féJèÑSm\ó)Ì¥@È###=Å6ÛxzåL \x0013\x0004NÆ¶d¹2~r\x0007qÛ>µKHð¾©iá\x001b_\x0010J\x001d2òáí¢ts,2C¨û¹\x0000ê\x0007Ò3ï\x0000|Ãó®È8Í\Â§=-\x0013±\x001e«/Úa.£÷Ã\x000fZö/>"·¶ñoµmBX¢´Öti4K·ð¾u³l\x001b8å\x0004=½^+p&×éxm[\x0001µ#\x0004ÆW!Çãòô­\x000b-BÚ÷ÁSi¸aq\x000e¢öß.@
\x0019u'·\x000b\x0013\x000f]¦¦­?h¡7FüÛ4kë6ÑXë÷öq:Í\x0014RÈÈ!3\x0005#\x001dx\x0002²®Ù¼ØX6@oñþF­³Fñ[ÝJ\x0018¬dÇ ^:ùÖ%Üí\x0011YW¬C\x000fn£ú×J·+9%RòçÚøÏÇrëÞ\x001cð\SZ,o¦Dñý¤>ZL\x0018È\x001bqòà îzV§Ä\x0006\x0016ÿ\x0000\x0011<Cå`\x0019÷\'»\x0014\x0012/ê+º.|!#Çôk7w</p><p>Ý?ô/Ò»\x000f7YÖtmTt¹°³¿\x0018T\x001fäÕ¢¡Q%ÔêXRoì³£ý¤îGü'v.X^évóuõ2\x000e?!^-§ k\x001dAPùdßøñÿ\x0000\x001a¿â[ËÉµ\x001bQ}s=Ç©\x000co4¬ûcRB¨É8\x0000\x001e\x0007OJ§£\x0002zDü¦,\x0011ô+jPä\¬ÆµU?z=Y±S00*MN@À.N\x000cC§Ó­:hxb\x0008ùA#ó\x001fýz¯yûÕÇ\x0003ÊoÐPãm\x000cSæ³-Ýê7½âßj3\x0019®¤f\x000f&ÅRv"(ÈP\x0006p tÉïÖA\x001cÈd,bV\x0005°sòç5F\x0005"\x0008N\x0007ßãþù­\x000eX\x001dWÄ:N\x0017þ?.â·#Ø¸\x0007ô&³©¢gE5ÍQ\x001d¯Å\x000bÉ4mOÃ:m\x0005IÒb@YAÚò«\x00168=\x000e\x0008÷\x0004ÑáÏ2Þø\x0007Yñ,·	o
*F¬¤c+ñ÷ïÉ¬?¼wß\x0013õË½«,1ÞùH°</p><p>GÀú|µôwÂ{­?[ð\x0015µ¦£c\x001aid_k»óhåv,ËÜ\x0001ó\x001cÿ\x0000³\1æUN£äÓéÐùBé^;díÎ9§D/ÍÆ	Î;vÅZñ\x0004]kwZD°[É+¼q\x000fàRÇjþ\x0000øTðl `\x0012À\x0003þ\x001aên7<ê±Qf[`5\x000bS(!\x0018\x000c°\x001cíøVÔ­ÍÔóG\x0019,ùq®: ÿ\x0000?­E5¶ÛËrÍÁ8úUäd3Ô\x000f\x001e½M\x0016/NTcjch\x001cdu$þ2</p><p>sÛ õ®Yt\x0014\x001c¥`ê\x001fëJp£\x001bAÅi\x001d*^ö \x0019Ü\x0010y?çð®©_.ÙFD+îçü¸\x001fgiàBrÊ	C\x001e¯Ô~]\x0001ëZVËvaÉ#­)+\x000e:²(mä¹(-É+°8ÇRÄñ]O\x001e=+LÃvR\x0006\x00115ô«ÿ\x0000-f \x001d¿AÇéSxz%Ð´×eAöÉ·C§£\x000fûê\z\x0001Ðÿ\x0000sR©fgv,Xfn§?ÔÖ\x001f\x001c¯Ñ\x001d·ö0·VW@píÇÝÀÇô®RÀÄæpp\x0007ÓìàBÌÙ\x0003<\x001aå¬þ&÷</p><p>½9ëÎxô­\x001eÌæKÞEÌ\x0016|\x000cõÆ@éWíâ\x000c\x000fÓ·5P´q7ïd :/ó5auí\x0016Ò/ßj0\x0016þì`Éûä\x0011úÖ7:\x001b0üsxö\x0016±ÚDÀ=À%\x001eB0>§ùW\x00089R\x000fsÔ×WâýKFÕR9!çí1©</p><p>Â\x001f»NX~cÖ³¼!áÛ¯\x0011ê/\x0005¼ÛÚ@{»ÉÉXma\x001fyÜút\x0000u$95\x0012`µf/íÊ¯à(U+»~\rzWQâýoI¹{}?ÃÖ	\x000eb¬ÜÈ\Ý±Æéeaë:(àsy¶\x0013¿j«`\x0000\x0002ñÿ\x0000ë©W)¨®¤\x001bNqÅ\x001bO\x0015#HK\x0012\x000e3L$\x001e­Í\x0004è</p><p>§5ì>\x0003áï¼-mâ\x0012Ü'¼A6æ¶Ðââ8\x0008$\x00036F;\x0003Ï\x001cð\x001b¨ñâqÒØ\x0014¤¹u:¿^=Ö¼s©\x000b^p N ´+\x000c\x0003ÑWúäiIÉ¤¦¢¢¬ØQJO\x001cSiJ\x0015>¢¤q\x001c !»PI¥bº\x0013Ú¸Î@$ý)®ß9éÍC3E§¥3Ô\x001ai\x001e´Ú2iÝÅ&u¤¥\x001dh\x0011«¦h\x001a¶«a{§i×WV</p><p>\x001eêh£,°©Î\x000b\x0011Ó¡ümø\x000bÇzÞòm\x001a×N7\x0001BÝÜ[,³[íÏú¦<.sÏ\x00078\x001eÒ|\x0002øÿ\x0000\x0008\x00175\x0003æh:!¾®à\x00078\x000fUÉÈî	\x001e[ãß´_\x000eøÙÏ/í.ô«øÜ+o(@\x0018 ôã#Øëfl£hó­Ê§¯<U|\x001fU³þÐ¹þýÝÔ¯ Ü\x0000\x001eÀ\x0001\æ°Ö­-`¶qÚ"ÇùZÞ\x0011ð6©¯X¶¡msoih§iG ûð?\x001e¸¦øÃºNi&5¨®¯\x0007\x0001#Æ\x000fåç\ÜÔãS=~g¨j9§\x0015êì¾ã9<W©ÿ\x0000Â>ú-ÛÃ}§+\x0002]Ä%k\æ\x0017?4@prr
`R\x001e¼Q]ÝÏª¬´û}BÇÇ\x001e\x0018ÓÀ6z´~+Ð¸\x001cÅ\x0014zÿ\x0000\x0007ü\x0004×¸;Y0,7c©\x0015é~\x0015×Çnü/\x001e§0MgÃº[0E%ntÉÆòêý</p><p>©.G³tª\x0018´WÓ<gªÂ»JC/\x0018P\x0006è_æC9ãåÿ\x0000ÕÐ¼dâËÆ(Î</p><p>¢gß!}Ì3¹N\x001b\x001d­.Z\x000bäu#pz0ë±r²I+J \x00121¸\x001e2;fkdê©u\x001ce­ËíWê3èk¶ö<í\Z;M>ÆÞñ¦æX-¦X©l¸\x001b\x0000;ErwÂÏ\x0010\x0007%wcÜröaøWC¥\y\x0010ec\x0011ÝQÜ?ÌÕO\x0012Û¥½Ü7qüðHÄôíéøkx«£¤3Àà^ÿ\x0000ihî7}²Ù0yýäy#\x001fQÊ·|H/|++dÓ\x0004gÜÇ<ú\x0007Zä4t=fÞú ]¬n\x0016AÇÞPy\x001fB¿Î»b\x0019\x0005ÍÆ\x001c=µ\}Z9HN}\x0008ÛþM'\x001ek>Æª¢{3Ô#3¥¶K3\x0018\x0001'ÊÜ~j$ ÕoÍäH}¸ ç?_9<òIYÔ¬ñ\x001e¤0\x001cà}\x0007þ;Rèöê·vÑB¾eÍÄ\x000f\x001a\x0001³4l\x0000Ï×\x001f?6Lv²!Õ¢?cD\x0019Þ¼}3Óõ¬8òÖ2\x0006þ\x0007e\x001fB+Ðuï\x000e_hþv«F"¿³l2«\x0006\x00000
Á\x001dxa\\x0016ÍöÁm(\x0001$WP@êÄ\x0012\x000esÏ57RjÀ¢à{¢¸P,mñÁùÏCÝ¿úß¥w_\x0008!QãKéÆbÒíî5\x0007Ïý3ãõa\g-åÎ§.EÅÌñ['\x0019\x0001B¹>¼Åz5¶\x0017t¯kpf[D:\x001cS\x0015Ú]b¬p:\x001c%rbd»ÔïÁAÊ\ý\x0011åª³j\x001a\x0016yî\x001b~OvvÏójô}CZ½Óíol,ï."°1Ë\x0012>\x0016E@\x0011r?\x000cþ5Íø"ÁN¨·l¸Tì\x0007ûÊ­'éüêÞ¢¥ÑdíÀ÷ÍtÆTµ9gR^Ù[ÔËÏÊ[v<ãÍÙØ'ðé¿CWP\x0008\x0001ÇJ¬¥äÉ;»¸N¤äà\x000c\x0001lTI\x0001\x001d3×\x001fçÚ²JÈÖrRÑ×ßB\x001eúÌ\x0010\x0007v>Àf£*YòùÅZ¹\x0019{i\x000e\x000b\x001c/\x001fNh¸\\x0015\x001cd\x000eÞ¿ç\x0014\x0005"¯NCgö	fs?\x0000</p><p>þÞÝ}«1îøÁf=\x000fjé5[$u¬\x00191oi$­òùbp1üGÓÛñªÐU¥ÌîöuÂ©ýÌC\x000bþÑî\x001c~X®Âº_ö½úÇ)\x0011ÚFmÄø#\x001d\x0013Ðõ«U±a\x0010¹W\x0001!\x0006BÍè1Çµt7×BÐãð®í\x001e±yµõ\x0019\x0000\x0003ÊR2"\x0007=@ãñ=ÍcViû«vtaéÛßÈÅÞ9ÒdÔ3\x0013\x001c\x0003ÈÞ\x0004Ý±\x00173À\x0004÷çÛµp÷Þ<vb¶6(«Ùçbäþ\x0003\x0003ù×-q\x0010VýÑÜ\x0007Ê¸\x0015íÿ\x0000\x0006<\x0001a§hÓxûÇ« Ø¯o\x0004	¹\x001c\x000c\x0003Õs\x0007B}Î3§¡´`ë¾fpþ'½Öt}\x001aÂ{Ôµ¾½\x0006O²Ç\x0002\x001c}'$\x001fñö®\x000e]BîgfæVfëó\x001ekgÇÞ Å\x001e*Ô5YbX\x0004ò\x0013\x001c	÷bOáQì\x0007õ®up\x0018\x0016\x0019\x0000ò3Ô'&µ</p><p>ª*VÐOsÍ\x0000â\x0006==«°øqð÷Zñî°,4x\x000by\x0001òáSÝn\x0003©íì^Ä(¹lcøWÃ÷$Õ>ÉdcQ\x000c×\x001736Øm¡_½,ü*?R@\x0019$</p><p>Øño,×N_
ø[Ì@ÃË;®Ùu\x0019\x001et²v'!AîÄ½ñ\x0002úÛCK\x0006xjhäÒ­å\x0006öö&\x0005µ9×øØùf¤	\x0003É'5àÏ\x0002xÆ-\x000ft©ï6rò\x000c$iþó¶\x0014\x001flæ§Í8µ¢9lTöv\x0017×Q[YÃ$÷2°HâK3±è\x0000\x001c_Hü=øAeáÄöú×Âù±é
 6¶)ÿ\x0000=®äåp1÷yÏ`Ý¹ß\x0011øï@ð\x001dÎ¡\x001fÃèl®|Gxî×zìp\x0004ßqæ+8ú*\x000e¹Èþ÷\x0004.{»"½äÏ\x001fñG5_\x000bê­¦ëÖgz¨²4,ÊÄ+\x000c®v\x0001ÇnµVoîç¾»êòi'¹É,YRIä­Vb÷Ð)*Àh\x001020pNç
§cP\x001a\x0004%\x0014S¶àdÿ\x0000õè\x0001´ ã§Z\x0000ÉÀäÑ@\x0007ZJ( \x0005¥\x0000úu£\x0015bÚ=çÃÞv.\x0010rv+#­'Jµy\x0019S:qôªárzfî\x0013¬74â=©\x00052\x0000Rç4Ú(\x0002qq(Ê\x0012?íÜq¥DI=M%\x0014¬7&÷\x0012(¦#ê\x000f\x001aøn\x001bÍB\x001b8%póhÒ©\x0001	't¶9þé'Ì@½ê·Ö]gÀ\x001e\x0016ñ\x001e\x001bíA´\x001bòË·
\x001fÍ\x0019#éç»U¿\x0007Ë\x0017¼\x00196s&éìÊ}Bp@\x0019ò_>ÜÂO§é]\x0017ìÏ´\x000f\x0015há5»«o6XöàËu\x000fú»ô-\x0001ÝAèÕÓ'tT\x001cKá§\Y¬4öê7\x000e$\x001c`z\x001f§\x001f¥w×Zm¥ýÎ²qÃ\x0005¾­a\x0016½c\x0000Âª¹\x0018%ì0êã\x0003ÐW\x0017\x0003iÕ\x0019ùXzÚºIí\x0005÷ÐGúUá1·L[\õ\x001fÉøyT^ÒÒA±rCf12É\x0019Ê±È\x0007¸ô?\x0015bÜÇ}\x0001°sHi\x0017Ïºà}A©e6ÖÑÞË\x0016»[f\x0011+Göyx\x000b/Ë×\x001d6\x0003U¼1\x0003Kq\x0015©åÖU3¸<Èçð5×	ò«t¨ûFê1´É­¼£q\x0013FÒ!s\x000e	\x001cñ5Ô+	,|=©©\x0005ÌFÎlKBÛFí'å]?Å\x000bx×CY­k¬á\x001eÿ\x0000Ö¿s>\x0016Q{¥jºbÊ%å¨\x0007å\x000eGâ\x0017\x001f\QB§µ×SLv\x001da¦£{x«Âúoíu²²ÚÍ3\x0008¦\x0004rQ\x0018ê:6=y¤ð\x001d·â}\x001f*_(Ï\x001cpF?\x0002+Ó<\x0013â»\x000bë7Añ:Ø\x000e\x0006k´{ò\x001aB\x000e\x0015³Æ2Iéè+Öõ=%<i{¨èG\x001ekªC²8×jí\x000c¼Ø\x001c7n¬o97\x0006ÔiÅF¤^Æe\x0007âf®\x000e9d\x0007§C\x0002yöáþÆÿ\x0000òÑg</p><p>\x0008\x001d«¹ñF³ñ\x0013]»µ´\x000bæ\x0012p\x0019j\x0008Ù\x000e\x0003pHôÏ¯5È\x0004\x0004/t;í"´Ã§\x0014|[qe¿ö]üOðÛ±\x0002\x000b{¿¶³\x0013©\x0010BñÊæêWøOjÌÛn|C®\ßËÎITLèMIà|Ú&»¨3gá«¦CÜI.Ø«Ç[]RÛÂe½³Å\x001elmØ\x0016\x0007Ìv³¸ÇcÇù5ËV\x000e¥{ôGm	Æ\x0016ÏvvºdúD~	µ×N
[N¶u»wÉ;ÌÊ\x0017ä°\x000b×ã­a\x0008S.\x001b¨$ÿ\x0000Î¶~Î°øHÉÈ7W ã¹XÓ ~oOñÆ\x001bÖaÓVå¦¸6ÑKq¹@	#\x001eÀW\Úå8`§Yºò9F¶ù¥\x0000z\x000fñ¨¡ý""AÀ9¯ZÑ¼\x001fg\x001fÃ
WÄ²Å<Ë´Q7Ì\x0007C×'=+NËPk{ÈdX\x001b÷H¤2ã\x0007\x0004zôüë\x0008TRv7©IÂ<ÆýÚF³Z¢\x0015\x0006O×\x0019?ÒKbYORFN*î§Gu
åíô\x001d¥\x001bÜ¦7<®q\x0014c9êÙ'Ð)éT¼Ui©iÞ\x0002W\x0017Kg;f¹þàcÎ;ä\x0017#¦jì%	Zç\x0017âk·ûìVRÇ\x001c&eÝ´ú\x0001üÏlWøYÛQx§Ýa\x0001\x0010»îÈëÇ[wÚ¢ÙÚfC´ÙË¸9e\x001c1Ç`OÊ>X÷×¨$\x0016ÒÄcBDª{'Ý±Ç^U[ZÈ))7Ìö2`Kic\x0007d\x0018:2\x0010AÈ4û»ng{^kÈò9Ë\x0012OR}M\x0018\x0005í;\x0017¦sør+µðçÃý_Ázî.b±±ÄVË*{¹3¨?A×'Ä95\x001dY×N2»\x0013¬ýþ\x0019ÿ\x0000Âe¨6µ­å<=a Wìn$\x0018>RãØ¼rr,þÑ_\x0011_Õ@ÑbÑ4¯ÝªC(ãq\x001c\x000eÝHã\x0015ØøcÃ\x001e$Ò¼+.àÛi\x000e¹xïn^M°iñ÷7\x001fÍ=öäö\x0001kæýVIZîHgòÙ¡b\x000fxê>;ÕÞÇm[Q_ÈÏùcÉ4À¥Xxð7ÉÀ=\x0007÷¿Ï­\Ð4kí{RÇMÉ4­µA8\x0003\x0000I=\x0000\x0000O\x0000\x0002O\x0015Õ(ØóÖ§gðá¦¡ãû×\x0008©g¤Ú×z$KÔxfÇn1Ô+²øñ#LÑ43àIöM\x0011>[«å8ôô'w\x0007iî{ô\x0018^\x000ewÅ?Í [x/ÁpÅ§øzÎ5vµ'\x0017r\x00007\x0010Ä\x0002SvNO-ÔûxÎK7'zÃÈëö¦¬·=¿Âþ\x0011ð\x0007ôK\x001f\x0010xû]W½ºgCÓ$\x000c@# JÀðGB>P\x0008#-Ò»ï\x001fü|Ò|7áø´_1Ù´æ0<ûx6[Z\x0003ü1©\x0000»{ä>QÝ\x001fZi$|n­ú\x001d¾µñ3ÄZ¯ÓDèEd]¥¹ò²¯y#\x001cº»têqÀã\XWl°\x0004ôÁ]W|-s¬[O¨^ÝG¥xzÙ¶]jW</p><p>J+c>\kÖIHä ú\x00074ZÛ\x000bÔ~ñÊQZþ$HVøzÚîßNP\x00161w(WÇWl\x0000\x0001n»G\x0003¦OZ§g\x000c2ó¤\x0008@ÈÉÅQ\x00113²*w§¤lü\x0000êOAR\x0018Ö0L¹Î2\x0014uü}*6bÞÃÐt\x0014É\x0014²¨Â\x000c·÷ô¦ry&q\x0013Å \x0005b¼©Çn)(4v \x0002¶|)ac©kP[j_eµlîp_Ã'õ5)éÔ¤®¬¦ÔdWG°]è
ôÕÛ&¨÷exÿ\x0000ZÏùlP?ZÎ]WÁ\x0016mM=æ#¡1ùîoé^dw\x001e2:±bë\x0015Ê3¢È\x0015(Ý\x0018zqÏå\\x001fSë)ÉüÏV\x0018õÌi¥ò:-JÙüG«,z\x00064Kð¦÷cì¨+¦¶øKw§Ã\x001dÏ5m7Ã6íÙw.ûSÝ`L·àqMÔ¾,ëdÖ^\x001fK?\x000eX0\x0001­ôD\x0005îdåÉõ;«Ï//¥¸vi\x001däcfl}MtA4¬­*nNrßúþº\x0017¢ðU­6Þ\x0014Z¼¾WÌ÷·"Æ\x000f	\x0010\x0005x9fã\x0007xãiIÉ VëCÍÒ\x001f\x00042O*Ç</p><p>41Âª~¦t
A\x0013tÐyK×.@¬Ø¦xd\x0012Bì§S)×\x0017SÜ±iæF=K147BéºI{é¶E"b¤ôãm.i*âQOÀÛM G»i\x001ahºµ¦³\x000c[lf&\x001bÈcé\x0016ïõ¾ÄbD÷\v¯rÑîF4!¶H.¤i\x0016Úã+Æ×ÆÉU»o\x0018_Ö¼\x000f\x000f%¹S,¶îÿ\x0000dFròÊ7t\x000c\x0008$g¯>¦»OwQG\x001dÎª:\x0018cû\x001cËù¶²«u>Äà\x001f÷+\RÚq/\x0006÷¥/Ïüpð±²ñcßi°F¶wè&#L\x0002ÛrÀ{õlqÁÈïOØ¿Õ±.\x0014µ®­\x000bÙ3©ÃFÍ­ø:¡öý+Ó¼W\x0004øNÎ×Ä\x0012Éskgqý}t2Ò¤|½­êÿ\x0000´¼g×{\x000fjà-´ÛÝ+_d*j¬$ß	ù.\x0000ùhÏNF\x000f¿Ô\x001aÚ\x000bã¹Îäã^ÓØÌñ¾?µia¾®#h¤¶\x0011¶çzqìv0õÅ]ø9áF×|K\x0012-ÄP5\x001bÃ¡a!\x0004|Ï\x0000çOzõ/\x001al>'ðæ®Dª\x0005Ìb)eq~¡ò¯;øm|<=ã\x000b	a#G!#þY¶TþY5pm\x001aÁrÍEôØè>*C\x000c~-JTXí.í|èÕq, \x000c\x0001ÓMyWåÛQ­Éá¡4$ýÙ¢"T\x001fcñ5ê?\x00194¡¥øÞk´\x000c±Kò?ºxoÈ^uª/ön°eq\x0014sEy=
à~\x0004×v\x0016\x001c´Õ;\x001bQÎ«R6.´Èõ
{I:y\x0011YjÛ^ß"
"Oø\x000b7OAU|Y \x001f\x000cx»ÄZ+ÜãÛ\x001b,¥vç(¬¤Øn?:Öð£$:é6_K½[«v>¾Ù\x0007Ñ¢ÚßT\x0015ÖüTðÖµñ\x0016[¨dtýRÉüpêÞTCpÀè}?\x001aujòTö\x0015</p><p>\x001eÒÜò]e
Ä	T¨{©8?í¨8ÇÔâª\x0001¾Þà)þ\x0016\x0018éÞ·|K\x0001¸ÓW\x0003æÛi<¼\x0011\x0015¿ÆÂ\x0005Î³¯OalSt*\x0006s\x001egB}ºþUSM¶Di¶î;í\x0012ßCø-o«yò½ß\x001eÞÑâ`6,I3H6¹>XÉ=«Ï¼4b±Ö ¸#!| \x0000äá[ð8>µêÿ\x0000\x001c-ÎáO\x0006xsz³YDÆC\x0019ùY£@\x0019ìYØ×É§¼<·»?Ò.nÌVäç2Íÿ\x0000}:Â¸pòæ¼Vzx4ÔcÑ\x001eá½ êz¬\x001dYíØ©Û\x0007i\x0001°'é\x001aÆ¹}Riü]ãû¹¡RÓ_^º@\x000f\nØ \x0015ìZµÈðï\x001aT Ka¤(_k\x0014~!Wõ¯\x000eð\x0016¥6â\x0018uHB`\x001eå·Ãh\x0004cñÈ\x001e´å'ZRé BÔ!\x0018Ë®¬ú'Æ:}¶¦i6Í".áÕ[«¸öópÈDôÉm¤úï¯\x0002Õ.w»Ôµ\x0017\x001elÌeCýârß©\x0000</p><p>ôozÅì>\x0006ÑloÝ?´uOøê\x0003;6®w"`öÎÕ\x0003þ×\x0019ðóK:×£¹Õ×n §Û®Aä;.J)õ%ùÇ¢\déÆU\x0019µUí\x001ci­y­è^\x0007Ñâ	ÁKÍFåã$¤².Tz~î!×Õ\x0015Söñ\x0005¼·\x001a´I¶iÚgÉ3³gt¡rîÇ¾ÅÜIþó7p+ÔüAâ\x0016ðOouëÍ¿Ûú­åGÅfacÒ4\x0001qê¤ujñ\x001f\x0011x~k]\x001eËB¶¶_\x0015^ÊeÔ¯]CÉ	e\x000cÐïÇ</p><p>É»]ÍM*·jS:'E¸òÁy#Åµ¹CHÎªÉ\x0011À\x0008û¨8Aùr}ë;\x0006(\x0006Aß/O÷úçùWQâ+[Iõo²Ù³5µ¶b7
ÉoßÒ³ìt\x001býoU³³°Éu|Á`\x000e\x00153Øpyô\x0004×L¥Íï-?e(>N¦ÿ\x0000ÃO	¿uhí$"
"Èy××9ÀHÇ'Aé{\x001aö?\x001ax0jw­Ï-¶áõ\x0011èÚ,06gùqöôÏP2F:\áñðÂK\x001f\x000børÒÇT6¶©=Ê\x001cÓ\x000fNÉïÓ¦3á>%xïPø­¤úB-íPÇ\x0012Ã\x0017»3ä\x000cú×"¥*³¹è:¡NÝS¡øñXñM³Øiè4	²©cjÄ4Ãý¶À-N\x0007×­yM³}êSyJ°9\x0019\x0011ú\x001e¼UíF9lÑ\x0002O(À\x0004üû}@ì?ZH°&ô´ÄyQ}÷ÚYW?Â\x0007vô\x001fvª</p><p>\x001aDó¥]ÏW¡{M´Òïm}N+«hÓ¬°°Ãz\x0000§¿Òº\x001df[[\x001d&ëEðKý³Í]·÷°ró/\x0007É}ï(\x001eIÇÎÃ\x0000®SYº3:Ä*8X³´ûäÿ\x0000\x000f­"½×,à¿¿N·Ps)!cõ'nN\x0007ùõ\x0019ÖèÍ©Uº÷¢µ2\x0012	¼¢%ÎÝ¸9Ï¦=i<¶2\x0008¶°;vãôÇ×5î×^?Ð¼+$v~\x000bOíØs\x001bëºýó\x0003Á[aÖ%ëó\x001c·?C\¤:\x0006¯j±ÞX\j6·óÜyokr\x001a}Ó¾J\x0001bIç\x000c¹ÏSÎkÛ%º6ú«zÅ`ÊU°äqSG\x000eè^W`\x0011~QêÇÐé^ë¯|\x0001M\x001bSê\x001e-Òô»YeýÄ7\x0004ËvËÀ]± \x001bØð¾ÜúMy\x001fÂºÂöºüC\x000fÌË1D·OB½2?ºCãóÅ/jÔËÙ5«ØóM\x001bÃ6\x001aFo®øÜË\x0015ËæÙéQ6ËñÙ³ÿ\x0000,¡'þZ\x00113´\x001e£#Å^(½ñ\x0014ð\x000b\x0015½ªìì-d\x0016¨Nv¢ú¥Y$í¼iñ\x0002ãÄ\x0012ê.\x0019Ð´ÆÔ\x0017\x0012Þ]ÇçÝ\x0010Wo\x000f'Ýàc(£\x0018¯51ZG÷çy}|´ÀüÏ?¥i\x0008É«ËFEIE{°w*Y¸äÓ¶r¼¿céWc\x000b;µ´U\x001d±bè+b×F°$,\x0018ÿ\x0000\x000ch\x0007ô©©Z?</p><p>6G5\x000cRÜÎD$®ÁUTd±=\x0000\x001eµÜ¯Â?\x001d2nÿ\x0000cT\x001cg\x0006\x0013·§èÒY¼RÀ<©PY\x000bí`AÈÁÏ\x0018<×¤i\x001e*ñæ£:ÛÙxy¤\x0000n\x001eim£Õ0?\x001aàa\x0005ðô²öÖ§k&¥ ê\x000fc¬Ù\Y^ \x0004Å<e\x001b\x0007¡Á¬ð\x0006y¯¤<U\x000e¢_SÇÉ¯x )lÏvÝñÎpGü\x0006¼CÆÚÊkúÜ·â;xÚL
ñE\x0003°Ï'ë[ÐÄûm#\x0006¨«¹\x001cé\x0018àÒfºï\x000cø#Ä6¿þ\x0011­\x0012æâ&sóªí1Ø4\x001f¯Tµø#áÏ	À·_\x0015<_kbøÝý`ÁæolOä¸÷®¤qªmì|ûNVé[\x001e1\x001a ñ%øð·Úÿ\x0000±¼ÏôoµeÛãß8öÆk\x001d\x0006M\x0002³NÄè\x0003\x000c~´¸ qõ¥\x00102\x0000§7#Ò¢çJ?t& z°F\x0017¨#ØÕgÎsÕDÊ¦ÃE*ã<ÓjB6¨$`ûÕ\x0019!­×Ö\x000cô='Àº:iö·þ&ña
ÄBU¶³Ý}r23µ>T>ÌÀâv*\x0010svG5-½´×2íây\ôTRÄþ\x0002½\x0015µ\x00122é^\x001dÔ5ë­£\x0017\x001aÍ×\x0018oQ\x000c8Èú½AyñkÄ²A%¦-¯ì\x001cäÛèÖéh?ï¥\x001bÏâÆ7cOd¢ýæpNG2*½Y²¹<æ«SDTµô?An4m\x001fÄ>³o</p><p>F¬ÀKr\x0007Î\x0019F\x0011=S\x001c÷Ê¶z×ÙYÝXÞKöõÎ­¢7Ù¯\x00161>Õÿ\x0000s×O¨_ZÜð\x0016«w¤Ü_h×\x0011:ê\x001a<­r¶Ù,Å8óâN~e SÔýkkÇ\x0011Ak¨ØøÔù¶i\x0012Åxbÿ\x0000Ú|Çå}Lm\x000f^\x0014Ö0q{\x001b´¥ªÜÜµ\x001dsB¹±,­5Õ»@­¥OÞF~eã^Q¡ÜGâ\x0007±Ñ¯'{k¤V° 7<[³%·ûÀnhóÜ\x0011ÜW[§$öZØ"í,-7Gó,RgÌ¶@ÏÉ=6È ýÓY\x001e4ð\x0015ü÷¶7\x0019Ñî¡´Ô#\x0012Ko\x0008ØÖ7Jya6ô#Ðãµvá¦¢[91PsµHæa\x0012ÙøÁúÂ\x0002Ê.m¤f\x0003r9Â¸ì\x000eà¤Ð:×4\x0006åÍÔ,¼¹þ\x0016è\x001bèz¥ªê>&ÓôýNñLZÞ$ÚF®ª\x0006ý\x000cL\x0000þë\x0008äÀÿ\x0000k\x001d*»x^÷Hñf¯ºÇ\x0015ÝÔfê,|°¶@'=6å~µT¤¡~aV¦ãÈrZÖ©w¯ÛCq¬N&Ý\x000c\x001c&>éÏ>¹V9úV\x000bÅiu¥|³#Û\x0019Þyd#ê?</p><p>èõ+
BX/\x0011.®nÄ$ÿ\x0000\x0017!?ª\x0007ü\x0004W\x000e&ÏT\x0010æ@¸ ÿ\x0000\x0011\x0007Ï\x0003ó¯W\x000fË(&\x000f\x0018å</p><p>KrÆrÇÄÚMòª¯Úap\x001dÝIÇþ:?:õØgm/ÁñÅ"¼Öðß£Æ§, Fà\x0012;t\x001dkÎt>9ïtYmy¶:Ë\x0011ô`®Ëÿ\x0000\x0001hßó®ÁS\x0003â+\x0019:	,î÷\x0011þäÊ²ÅÑæû\x001beøJw8íl]Ë£Á
¬O´´ûCF»!B	#øyi\x0015ºÕ´ý_OCÚº­\x001c1¡nP7\x001d\x001b5¿­k\x001aôæÉ£\x0011ÝZA\x0004É¸íÝp2=ñüêÁ\x0014ûwí#²Ê×\x0003<à\x0004þ@UU ïØÞ£9ÇÝßî*|q¾óÆóÀÄ\x00184è¼ãÝõ$çò§ëú#·<)áH÷,Ekk?\x001d&¼Ùäã?îÕ Ä?\x0013táp7Cyz\x000c¹#î#³¶à+[ß\x000f\x001e_\x0011|MÔ5,nÜ_Ç;*!£\x001fûæ¹\x001aöqÓ¢;£?k'æÿ\x0000#GãUø[\x000b[%\x0003ý:úK\x000bÿ\x0000<â\x001eT</p><p>Mp¿\x000f´\x0001ª_iyÉQ½Ìç°¶oÀ¶Õ®Ç1ÝxÆ2ØhÈ'Ò&³\x0016\x0000\x0001</p><p>ÄÀçwéJvxcÁº­êÇÜãD³ÇÞ,Av\x001eäqÜ</p><p>µjt|ÙR­þêý\x000e[W»â'Ä«$\x0013Å,â\x000bD$\x0005\x0011Gà\x0002FàB½\x0016ÇKo\x0005øilõ\x0005¯Fü1\x0004I.â-¡$vÊïodnÆ¹/\x0006xXYøØê-\x0011·Ó\x0015.oÌX+\x001a¢1}w²¡ÿ\x0000uªßÆ\x001f\x0010ê±´Ò¡
6¢Nß*0\x0006fsÄ\wPÁ9çýeyõR4ôêvÁÉ'RÚìwG»æk¯\x0014j\x0005¯,´©KZÇ!È»¼bY\x0017\x001dþlÊØì¢²<Y}«i¦[S¨:ù¨wW\x000c\x0000/;ÈZg'¨ùú\x001fJôMSI±Ð4¿\x000bx^Ú\x0008/%Ó·j7×D}Î	,=\x000c²aGû </p><p>ÂÕ´«{ÝFâËRS%¥¯&é¹ÏÌÀcûÎØÇµBkDwÓ£mv<oPÓáòêX	¶Òæ¼\x0001\x00070§\x000cWÔø×yqzÞ\x0003ðá¹eX|U«B\x0004QàgNµ<\x0002é¡Àü~6`²Óa¹Åºª+ZY\x0015ËOVáæ\x001fê£</p><p>\x0007</p><p>¤äú¼ÏÄ7÷º­w}­9{ÌLð\x000fdAè\x0006\x0000\x0015ÙN´It_ÅZ·²n}^ÞG;ûÉ\x001ePÎ@vÜÄç¹<Î¯&mcVl`À eÜIõÁàåOµ´\x0012\x0016¸\x0014G÷2qïíïI\x001cm¨]K²EHc\x001b®.î öþ@\x000eMwªj\x0008ó\x001dG7èIgj÷o=ÅÌÁ\x0010s$Ìw7?Xô\x0015Ùß|8ñxZã_M\x0019ìt{d\x001b\x0016V\x000b.Ü¼)ùòØç<t­/\x0001%Î-,4¿Ú]öZlê[ÍF\x001b|Ì\x000eL¤Tö\x000bÀéHñßÄ]kEÿ\x0000l]ÛÏâWtv0Ç®;gþzMÏ|üüìMI©(@ô0´âãí&xm¶¤épý¨ë#R¼7­¬íe</p><p>¸SÃK&Üa¶ç</p><p>{àÖ\x0007¼1{â«ÙÄ2GkelK»éÎØmc'«\x001fRx</p><p>9cÀÍu\x001a&&¯%Î§«Ý\x000bm&\x0007Î¡:î\¶O\x000e^V\x0004á\x0007CH\x001c×¨xOME¶Óõ¡<¾\x0019ð6Â{KG_ßÞLÃib2egÉ\x0003v¢\µj{5n§L){gÍ´Nw@ð4>+=;Hµ:WtéKNê$\x0017·ò¨!qâ4\x0003 (;P\x0012[sWmoñ\x0013O³´>\x001eøO¥Çs¨Z«¨¿\x0015mm#\x0003ç3\x001c¼Èø\x0007ß89·ZÄ&¹ðý·ðïìcIobb±´q\x00037/ÊÅ¹\x0011.O\ã­y¿Ä_\x0011hqX>à§\x001f
)1òÂ\x001bÙ\x0013%¥oâl»w\x0003ÀÍg</p><p>R¼þâ¥Z\x0011MAiù5¿\x0013Ùé\x0012ÞÉa«\jºÝÁ+}®!ýä¬F\x000cp;«\x0004Ê\x000b°þâñ^q6¬ø)§Á
g¯2íõsü°=ª£Ë%Ë\x000e\x0015#A^G§ùëQ¼Sl`täã­u¨¨ìpÎN£¼¹i¾s'îMZÑíb»Ì¨ÏÊ»{u\x0014í\x0013O¹¾Ô-Ö(È¹`8\x0003"º;M%íÄQØ\x000cª3»\x0007\x0007úW."ºµõ:pÔ\x001c3Z\x0013[-1\x0014\x0019ãwÚ¨=p\x0007ZÑi$Ù
l¿</p><p>°®]¾än+kBð]åõ°¼ÔÞ=+KQ¹º`\x0006=\x0015{z­«ø÷Jð¼\x000f§x</p><p>Ï÷äm}Råríþâëùw¯1AÖv§­)*qæÜA²Ð¬Åÿ\x0000/\x0016É\x0018\x0006É_uÄö\x001d3úzÇÕ¾0Ëf>Ïá++}:Õ7*æ0îÙèäþ¦¸ýoÃú½ç-<_}~·ÐÝÜÉkpw3Ëm2ò© #Ëó.	\x0018\x001dºW5\x0012¦\x000eÐ8é»ÿ\x0000Ö®¨`i­g©É,lß»MYw\x001dys}u,ÓÊí$¤³¼X±õ$õ5êß\x000eu^\x001cðÜZ¿¢ÞëÞ%,ÄÛÎ\x0000¶L1ÛpF1Àçòó\x0014`ï<p8\x001dÿ\x0000:l\x000c\x000c8ÁÆ\x0001®½6¤½êç¬ø¿ãçuX>Ç¢¼\x001a\x0016\x0006Øíì\x0013c*öùúø\x000e+É%{íV÷-ç\ÝJÞîîOêMz\x001emðßJÒm/üA{ªëÚ±\x001fM³ì°ÂÝãVå¾©Å[ºøËw¦Dö¾\x0005Ñt\x000cZ°+¾Ö\x0011%Ë/£Ìüî\x00004Ö\x0013%u«²8=oÁþ!Ðmm.u­\x001eöÂ+²Â\x0013s\x0011¾ÜgÈê:ÖdVòFÃpÅ}\x0015ðWâïb2§¬¡:\x0001F­$Mq,ÃÂFbHí£\x0018¯c½ñ?ÂmsG»â÷A{IlÊÈ"f\x001d}\x0003gÓ\x001cÔ¹¾¥FV±Mù\x000bm ±</p><p>\x000f¨ë\x0018ÿ\x0000\x0010<\x0013\x0001Å_ñ\x0007Ø£Ö¯ÎúxÅ¹só4[Üûã\x0015òqÅ\x0011×Rª5
\x0006ÌÃ$p>\x0003\x000c\x001a\x001dÄä:³ö­QÅ7}A\x0006X</p><p>r3Òh'¿ojoSLW²°\x0001N\x000cqÁ?7?¥\x0000ûÐ$ì\x0004æ¥\x000fQÁíQ\x0001SàmàÒeC»:
&ëÂñØ¬ZÖªMsí5\x0004\x0011>F¿>Õ¨µ©¾éë2Y>RÎC8^Û\x0000\x0013ô\x0015]Îi´$TêsicíT·Yðí¾¿ákv·ñ'¤Xf¶vËÉ\x0014cý[rw|¹*}7/8®M0\héö\x0018LÚsÆ×Öp\x0011Ö²qskÓ\x0019C\x0017Ù\x0007A\¿Ã;Û=?ÄÚD×/§ÝÚ±dL\x0013¢«:H£©\x0001Y£$w®Äº¯ö\x0007ì5IáY\x0012K{+\x0004á2\x000f\x001dU×9õ\x000c}(«Km\x000e_k\x0005.ä'Å>!ÒüDñ\^éßØöÈ³7\x0000LZ\x001cl88\x0018#Û¨®ãÄ:{xDº¶¶½(u\x00086Ç4\x0012äL¼«\x0002\x000evþ¸\x001eµÅêkik©	|ëHmâ=òßKá uòÏÎ\x0006zcÞ±|5>£¥¾µá)/$qbCÛM\x001c 3Ch¤\x0004\x001c\x0001LöÚßìÕÅ'¢"Påw¾ç;ðS¼ÑüS¨xS­.®U­¼É\x001fî\FKFÄ¸;ß+]ÿ\x00005©5Í\x0006Ò\x001d\x0018®-¤\x00122A\x0013@Ø.¼íåá®3Æc}\x001e{¬ÀEÅÂ½¼Öã÷©<X\x0005z8d*ÛzõÅoÉæÛøWûA<¹ÅÜ\x001a3Ær²¬U\x0007ß\x001c¿5w{\x0004í>ó^-ÚPÙ¡¾<âûÂÒj°K$ºuüwÈÈ£0Ï`Û²\x0007o­yíÄ\x001a¼70|ñ\x0001\x001cÎaq\x000c</p><p>ú[À­\x0010Ñ\x001fKp\x001e(2\x0010\x001fã¹_Ð×_è\x0006ÇL¸´7g4±÷¢Y\x0006ßÉ\~UXJ¾Ï\x000c]\x001f¬J5\x0011cÁ:m´>\x0012·¹»N\x001aõÙIùQâÊ®ßL3õ¨¼7\x000cPj\x0016\x001b%fC~»p\x0014\x0008Ü\x001eùÉ5³à«gÂZä-Æå¥Ïû2C\x001b\x001fÏ\x0004þ5>©¡¦âÙ­¢w3mq:\x001cñ0Çæ+IUæz\x001c?³¯\x0019Ehyö¿\x0019¾ðÕ9hííóÙ£¿öqP|\x001d¬oõÍW\x0004tß%W¡\x0012Ë DþF´<Eþu¥Ø\x0002\x0014M\x0004¡½ö(\x0007æj\x0008Ò<\x001b©Ê7\x0003q©B2\x0006\x000eØÐ¾\x0007ü	Çã[×\ÑF\x0018\x0017ËROÔÆ¿´¬¢½X\x0018Ú\x001bÍ\| ²d.}p¤×©ü\x0019´M\x001bÁú×.T+3¦F7G\x0002ÏÐÈÇô¬K½?í_\x000f´}2Ò`%¿Õ¤xR\x000f@?îï'è
w'Ksák
hî´ñÛØFÀº#Ìä»O®k\x0015UrüÏC	IÆ{ô9½\x001bN_
øI5Û©d}SQ¶²¶0ªìev\x001eåWõ\x0015Îx_KÕôßí9$¹O\x000béãT¾\x0008oæmÑB\x0000õrÏð­z¥üV7\x001a¥õÅê\x000fì\x0016\x0004@\x000fE*\x0016Wã¾\x0011!_ø\x0019¯\x001bñ\x0004W7¾¸¶µ¼¾õ½A$s½Æ-á</p><p>\x0001?,~¼\x0002õÃMÊ«W=NUM6C­ð|3iþ\x0011·³uªê2ý²rÀ:fv\x0010¡ÏmÛä=°¦ ð\x00065\x001dfã^÷¶vâ²ÏúÖäMpO¹;A÷cÚ¯£i~\x0011Ñôxu\x0015þÓÕGÙÖé¤Ü°#&\x001cô\x000bS\x001eGZ½ãKË\x001d;Bÿ\x0000jÌÓ,ÑRö\x0018N\x001fh\x0019H\x000b\x000fãnIÇL±<u\x0016\x001au%Ë\x001e¡,D(ÓçBm	mµ­J7Ì\x0013Êu\x000b@æå!û¸ôC @£º¨õ®\x0003ÅW
g©\x001d\x0006"óÎ}·QW>}ìOM±þYìk¢ð6µ&¦êú£ps¶(`vªG\x001e \x0007°®_ÄZD°¦Ð]î¥fy\\x001c°F\x001cãÕù\x0013ë[G\x0004Õ^E²3úûö>Ñõü\x000cÉ-`R\x001400E¤\x001fõ²\x001f¼ÞçÓ\x0005dë:</p><p>Üm[hAÀ-æ\x0011w$úóÇ½t~\x001aÓÒy¤Q[iºr\x0019ï&\x0003rÛ§e\x0007ø¤n\x000erj}GÄé©Î\x0005­¨µâ\x000bkU\x0000\x001cd	þö2Ìz\x000fÂº\x001aöR²èb­^\x001cÏKÖae|¾D\x0016!@¥\x0016ã«\x0012G#¿Ôú×[ed_É´°¶</p><p>	\x0002(¢+;ö<\x000e¿ÈV·´\x0002YÈ¶ÿ\x0000mÔn\x0014Me`§h¸ÁâyT¶_á\x001c\x0019\x000f>ïWb\x000b­"êâs\x0015ÂÛ\x0018PHÆ\x0017#æØOÌT\x001f¦{TO\x0018¤ì>¥É¬ãJ"ðl°2\xÔg\x001f2Ú\x0003ÕSÕýMy$Þ\x0007¸S¼Õuf¼:\x0002HÒ$ëæÜÝ1Îè¡S¿]Îrª9<àWµÙxv-OSi,á¹{\x0002s\x0004R¾É.\x0000à»°ûç?7SÑrzlê7Vº\x000b£ùwZÁD²¢mÝ;G\x0012ÿ\x0000\x0002þ§¾I¬ï¤ulèlï="º\x001eO\x0016iiamâ?\x001fÅo¦è¶ ÿ\x0000dø~3á\x0007\x0004³ç$cÄäËg\x0019Z«wâøÇ|G{7|\x0019\x00032[Î£ý&ï±Ñ\x000fñ\x001c`Éù\x0002£Õ|KàM:þK/\x0010ø¶\x0019¯/Ä\x001f¹Ó\x0018¾ÇnqæÆ:"\x0012\x0006	è}\x000fkÚ.¥ã\x001f\x0014¼þ%ÕY"]ðC\x0000H`}ÕTÎ\x0011\x0007§~ç½cK
Ìîµ}Íq\x0018¸¥®·sñ%Ö´Ø´­*Íto	Û¹k]2\x0017$ÌÝåÏ2?\x001fxôè;äî-Ä\x001f½Ô²$ÀÙl\x0015\x001d·t{u?kØ¬¾\x0016£Ìe·ÕópqûÉ­7mÿ\x0000p\x0006\x0000~=;RÝ|!È\x000cÚ¤ns\x000bf\x0019üÜ×zÃE+&y³Å¦îö<>Yå\x0015G\x0000\x000e\x0000®ëL½JÑá_ÜI ù4[öQSÿ\x0000ë®¸|$[Èê</p><p>è\x000fúíXgÿ\x0000\x001f®ÂÇá.hë>µ}}s(\x0019û<E#ÝìØSì
pc0Óg¡ÅSrgxi5o\x0013jö§M³2,s#6\x0014$qG$:}\x001aÝ¸Ãþ\x0013»M{^3:(\x0003\x0016ð\x0010Äàu,F{~è×MöÑÙG\x000cXFFÛ[i5È ã\x001b×"¼cã6©øÇ\x0017Tk<\x0010É	T(n\x0003±bÀõ#s\x0011ÿ\x0000\x0001®'~öô\x0016gMÅòjÑã_\x0014_êE©y\x0007Ü?å°Pp¿SÍp«/Þ+¬Ü·áNÒDbn\x001d#çË­Cº$æ=ÏÇWãô®t\x0015(Ù\x001c51\x000e´¯#¾øcâ\x001b\x001d>úïE×Ù5ÈÅ­ñêb9Ìw\x0000z6ù»ðO\x0015Îø³B¼ð¿¯´}D\x0001sk&ÂÊ~Y\x0017ªºÿ\x0000²À\x001eÆ°Õð¸ÉÛàtÍz«Áãß\x0000£\ykÞ\x0015÷?ÖÝé¹ëÎ~hIÿ\x0000¾\x001b¾(µµ5Sç²<Ô± \x000068ÉþU\x0019;³\x0012Nzõ©®ÞL-¬S!õPü~Bµ</á­GÄ\x001a½¦¦DÓ\ÜH¨ªªHBN2ç\x001f(\x0019É'ÒV;JnÛ®¼&Ö¿\x000fí¼Owv±\x001bÛÖµ´´1Ó¢.d6xUb«ÜOãÈ>8Æs^£ñÞím¼Ikáû(4­\x0012Õ,lñæ*ýùp8%ßqÏp\x0005y¸~÷\x001b)2¦Üóó)9Çü\x0006ª\x001b\Î²ÖÅ@JJe¼qõ¨vàÒÍSIFN=Gù=\x0006=\x000f4×rÇ\x0018\x0003è*î£jZþ£\x001dcsxù+
¼eØÔàv\x001e½+»OßÙ,\x001bÆÞ%Ñ|>\x0015¶Éoç}²ìÛ\x0018sø\x0013</p><p>Z \Ó<Ô\x000c¶*ÍÎ¡u\x001d­¼×7\x000ep±BÙ¾d× i|8Ð\x0007üK´]WÄ·aHóuIÅ¬\x0001à¢ùög¨o¾-x­$´Ñd´ðí~Ï¢[­ Èã%×çoÅ¨¿b¹\x0012Ý¯|5¬øj[huí6ãOâ/:(î\x0013cÉ\x0019ÛÔr\x000fZÄ©îîf¼çºI¦sF,Ì}I=j\x000cU#)Zú\x0005\x0014b\x0004*ñA&\x00003E\x0015×øWÀ\x001a×ôÖ¾ÓcÈY\x000cYrFH\x0000ÞõJ.[	ÉE]õð½-í|BcÔ/î4è6Å"\x0001µe\x000c6ï\x0007 \x00078=ì3^ã'<û\x000bý\x0006çdÚ\x001dÊ­Ý\x0000V³9Âîîù\x001d9SÆ+É%[u\x0000ÿ\x0000jÙI\x0003d\x0018ï-d@=\x00058"»/\x000fxXô)4{Û{§³&[{«iÌÑ*ã\x0005D©09\x0001¹\x0018ô\x0015ÝÃÊO'\x000e\x000f\x0019\x0015\x001fg-\x0019FÞÊæßHMóªxzf¹\x001bï=«q,xþî\x0008`Fr6Ö\x001fJé³øsÄöÒ\x0007\x00163ä¼\x0018c\x0018oPPÉ\x0019'º­u½Íü+e«"$º¶\x0002Éu·ä¼µ`BL@ê3Ãr¤Ø®j&WÓ§ÑÉ\x000b#Æ'´x
-å\x0011ß\x000f»\x0019õ\x001eÏN¿7C¾¥HÛú½\x0016hÉ}áýrÖ\x0019\x001eTbÕläQÆÀ0Ì\x000f®Æ\x001f\V7®ñáÏ\x0010Ú^ÃçÛ,\x000bq$</p><p>ÅFðãq_Bxaï]'n],t¸n\x0014°ì\x0012é%´ò÷\x0003ýÒJÿ\x0000ÀO¥7GÐ!Ó'ñ&À$ÐXÊ»Güµ°1¸÷\x0003 þ\x0015¼*(§	|>½\x0017RJ¤zîhé\x0017çJÓ,/ì¥\x00176êVÕån3\x0011pw£!eÏ¶kmàÿ\x0000Ã1I\x0012ºO0¨ãkº\x0018Ø~\x000e¦¸¿\x00042 ÖtKóþq\x000bJ¤u\x0005F\x000b\x000fÃ\x0007ð®§Âm=.¬î$wxËD¹Ê©ÈrWêYãQZ¼äº\x001bá«%\x0015N[~\x0008³óôOs!7ZzÇ)S$E \x001c÷ù]Gü\x0006µuÔïÆ:<à+¬ed\x0003Ñ¹\x001f 5\x001e¦É§xU°]Ëlñ¹t\x0005J«~H«\x001a\\x0016i}`gEÔ&³d<|¡S<ýpß¥RO+[SÈ>$L5=sí±A
ª@¶0à`cpÀïç¥AâÄû>¥Ú\x0001ÌòIqbF?Ïµ\x001aÅ³]j\x0016×\x0000¬¡¢ü$ª«3VüV¢c¢F Xà ë´{È£ëïq÷RG\x0005:·r:>Ê(ôí\x0001&ùÚ\x000b(Óiâ[eºÂOÓuIá\x001b¨u_\x0018x³Å\x000e\x000fØ­_l'n2¨W\x001eø\x0004þ"¨Ê'×öÃ\x0010-c\x0008(²\x0004ò\x0015ýqÂhëWÂ6ik¡ÙiPÃn%»¸{¹b\\x0001ä«lôm«õÉ¯'\x0013+FÝOo\x000b\x000ekKdVñ:\x0008¼7¦é\x0017Í³ûFG¿ÕX\x001f»\x0002\x001f6UÏûLR1^at×\x001aÕýÍä±·ÜÈ2½³'ÊØ*ã=±^ã-FÚòòo>ÒY"Ú\x0011$$\x0013ökvãðywqBÓü\x0019áX¯.ã¸s¾ÊU}ØáycúãûÆº0(9HçÇÊud¡\x0017cðìrjZ¥×¯§\x000fe¥Æ¶¶\x0012Ê ©d\x0005\x0015ö }à£«\x0011îkÛSÔãD,ÊÌFöÜÙsv?Å#÷=±À\x0015è~.±Ô5{³nñ.¤ÀïäZÆ,zn`8Î0\x0000ì?\x001aÍÑ|5\x001dµáûp²\x0008R%Ã\x000e@ÏRGSÛò®Ú~êæ<êõ\x0014íNú\x000cð÷./,µ\x001dJ}¢ÔÊ«e\x0014ªXÜH\x0006\x0002\x00009#¹Ç_ $G
öZ<Ò%ÐÃ]4c\x0008ÛN\x001dÆ@\x0000\x000e§·\x0000WeâRU×O°´)¨I\x001f\x0014)ÿ\x0000.q0û ÏF\x0018Éþ\x0015àu¥Ô|5\x000e¢Á§Ë,ê\x0017WìÖä+M èKv9'±ý+Ï©Ûz\õ¨PÕ#Än"_º³ðÏQ×JÈv\x001bAýíäÇ²¨Ï^\x0018äâ»\x000bÍ\x001bFÐ'Ñìt/ûcÄ\x0012Âb²óºë'-q2ç	n\x0008àp\\x000eNÜ×HöPø^Ê+\x001d\x001aÕ5\x001dnùs\x001c`ae\x0000ðîOÝ·CÎ	ýáË\x001e+"ÖÒ\x000bM'P¾¹Õ$0]65¿\x0010/úýEÿ\x0000çÒÏ8Â\x001ccpÇ\x0003QËZ¤¥îÃDwR§\x0015ïÌÖÐµVÐæe¼±a%üEâ\x0019ÐÈ³Üô\x0010@8ÞS UùWäT\x0017$¸Õk¾"M7Ã\x0016Ã0YÜä´Ùû³L\x0007,íü\x0011/'=ó\x001dcÄv^ º
RÒâ×Ã)²ÏHÓÆ\x0000ç\x000b\x0019oï6~g\x0019<àUÛuï\x0010jÏ5Í½½ÕÌóK![=\x0002#þÑÎû:[·¸Î4$¼S«N×ÞG²]ë2N#Ó´\x0018¤iî1¸íËâí;p\x0014\x000cq·á=</p><p>Ín&v»KØpÒÜ\x000c°çþyçï7\¹àqkÍ~\x001ej1-Óø[Â\x0016W¦ùLój3äK;\x001f¼ï"¹Âç'©êkÑ-ü;k\x0006n/oc\x00108\x0016ýX¼\x0000Ïsøv®¥\x0014£e§æpJRæ¼ÿ\x0000#©]§km\x0006ØÞÝ</p><p>Ó\x001f¸tÜÇ¯ÿ\x0000®¼§_ðPÑ\x0017íò\x000b§lMp\x00079Â~v>ø\x000bõ8®ÞÛÅ/e\x0004¶ö\x001a}´Q\x0006Ìdg\x001fêÇÜ×WXñ\x001f%öêkAá\x0003äSì£jéR]ú\x001cõ«SkvËZD\x0001OÊ\x001a¤½µ,Ç\x001f/×Û´±ÌìyQî³\x001a|Û>¬8\x0007Øf¢¾\x000bu\x0007ÚºÔáiY¶ÆKCXï#i8Æ\x0005\Ú[²±ª´9ÂªIúw©¾Í\x0003\x001cdö÷­È\x00168 x,\x0012ãlqÝWû©úþOÈTäí«Ð¡
¼zQýÆÙµ\x000eó\x000eR\x000fdõöº\x000eÞµ\x0006¹mkâ+\x000fìï\x0010ÚE©Ú%>Ð»¤ÈÆä~\x0008éÓ85°,S,\x000eÿ\x0000"@3Â}ê=kRþ±(¿wD|ã\x0002ê\x001e\x001cÕZÖîÌÆ¬7Cy\x0013\x0016·g¥þe>ªI>Øæ\x0004ü)ñ/\x000cí¡[Gs\x0014\x000c#vG\x001a1\x0019ÆOS:\x0003Ö¾ÃÕ<=câM2]/Wµ[«I¹(z«`áÔõV\x0019àñ\x0015å7?\x0008¼Uá{û±¤ë÷6Þ\x001c·\x0017´y\x0004Årp\x001e4À.\x0007ñ\x000e\x000f§jã¯OcÒÁ×Uei\x001c¼_³N£ihn<EâM\x001bMLdrBýXí\x0015Ãx\x000bÂþ/µñ\Z¡E®©zËy\x0013?xeÑ#¡à×u©=$¯£øCÄ#¿Cÿ\x0000\x001fº¥Å\x0001ëWÿ\x0000e_­TÂÿ\x0000\x0017¼|ë\x0015Í¤F'ðNâÖ!ìS?5Ä½´´Q±éÎXjJòß/ü\x000fáiZ_\x0013êÿ\x0000ÚÚIû\x0006ºHþ¬¿JôOz|Cos/¼5¦èÚAXm..\Çºb0\x001d6¯ÌWp@'qÖð/ìë¢èW)}â±®N¸e·\x0008c·SþÐä¿>àzöH\x001cZ\x0000¶êª'ª\x0000Eì\x0014\x000e\x0005oO\x0005ÍïMÜà­(¾JJÈøëâg¬|/ã»X<Zþ"¿¶kpnïFØþÓ>\x000e|pA|£'\x000f\x001d+,xÀQ2Yø&K©3Äº­+ÿ\x0000ã±\x0008Çó¯³µ\x0018`¾²ÒöÞ+Y\x0006$d\x000f\x001býT\x001að?\x00024Vg»ð¤ñé\x0017-Éµ\x0016¶cê§O¦\x0008ôÅk,#KFE<Ñ6Üã¯sÂü[â«]vÆ\x000b[o\x000eèzJÂûéöì²?\x0018Ã;;\x0012?­r=ëÖ5\x000fþ0¶äi×\x0013òAt77¸Þ\x0017ükÕ<	â}3Ì7\x001fÕ#EÆdû;:sÓæPA¨öRBxÔw¹J#akfÚßÞ%ë&Ù\x0015Sh\x0019ê3Ed3OÌy4æEvÑEê¬0GáQ\x0010FEE¬k*É$¬\x0014å</p><p>TäÝ½)È\x0016¦\x001d\x0005«xm ÜG©É.>p®3íÁ¬k¶®$kTt±Ø®Û\x000fsPw§`ã4±¬ês¤¬Åt:7üG¬Ä³éÚ-ô¶§´\x0018B>²6\x0014~t\x000f5}\x0002Õ¡ÑæÕ\x001bµÜ\x000cã1RàqÐ\x0011T5}oUÖ¦\x0012ë\x001aåü££\ÎÒ\x0011ôÜN)êu\x0016\x001e\x0000\x000fwmmªxC´¸A\x001aÛÁ9½±ö2\x000fø\x0013_Eè:.£höt3j\x000cñÜ±G\x001eãÔ3\x0013É$þ5âß\x0004ü:cÖ#Õo£\x001b¼¶6ÊÝ³Áæ\x0006}Oµ{c(Ï&»°ôZWêp×¯\x001bò¤u§I¼3JÑÅ¦L¼L º[Oü%ÉXù#wð÷Èæ¸-NÓWðÏ%Úåí¤ÊÊ;1Àù]OÊÀÌr+ÐmüE.±cöKÈí¼ì%­êÆ\x00167õxÎ@Ï ýxâ ò¬õ\x000by4]q\x001aÎâ\x001d°G¿;­? /ÎèÆÖìNÓÔQB¼àùjl\x0018,*CåÏ
Iæi±¶!DÚ7³vÝ\x0012ÊGÏ\x001açø\x001ccåíFpEgj\x0004p²\i­8òË</p><p>?úÈ×£ õ(ÀqÔ~9¬:ÖçJ¼ºÆY7y\x0017Vòð	\x001d3qÃ\x000eGQ]Õm_Ix£f\x0008Úwqç\x000e>ä®á»»\x001eÆ¶y%Ì¶g\x0015:­Ã_\x0012Ø«c,7ÖW×1³Etñ\x0019\x0008\x000e%\x000cë·<îÆà?Úzì¯ím¯¦ýKybc·?»A9ÿ\x0000¾Er\x001e\x0019¹VÖà\x0012BVbÅ_\x000b\x0008ù¨É\x0019÷ú×dAeªAfª\x00129àÛ\x0010Ï\x0007Ëã\x001f\x000fò+¼\x001d9XôhVU£~½N\x001bÃÚ`EÔ\x0011±-â@Ê	"</p><p>·þ;Í^Ó4÷{\x0015\x0017-\x0015ö$}é\x00113³\x001fU \x001fcIáÙ\x0006¯K§Ï´Ç3½¹ÏRFvÅx«wB[}Yv³3«C)U\x001c¯±½ÍlÛwìa8¨8É\x0017¯nUüGlbV\x0013Å\x001eÖÈáÙHÇÓÄÔídV´º
6h£Ç\x0007x`	öÉqëo4ýÚÝÔh\x0006\x0011ÒB=8+ÈÕ=rÍ\x001aÂÚ7Ø&Q³i?yK.ì\x000eýE)®d«FOR<ûÅzzÏzÚPäKæCpWþz !Oü\x0008`ÖC´ÞÅ|±þîÊW¸*OðÂoà\/ç]Æ¨Eu éº|ð\x0002Qí\ò¯Õ\x000e=x\x0015ÉOhl¼?©´\x0012&-±þÑ³~]ñ\x0007*´]É¼\x0013\x0004fàe®äY\x001a7êLqÛàk¾[\x0015Ó­¯.âù'xÖÚÝºìE\x001b#ü3¹ÿ\x0000\x001açü\x001dáö}$ïâ\x001fj\x000c\x001f¾¨7\x000fnYá[>/¿\x0013ªX[³!X1|¬ÿ\x0000`>æN\x001cõ,~5yi®\x001bifñÆßg,Q \x001c´kÂ/Õºÿ\x0000À«ÐaifYí2©\x001b±Æì\x0012\x0007Ðssn¤U\x00173 V9tö'îî\x0007ó¬ë£=õÿ\x0000\x0006%bØó\x0001ùTz'©õnµ¼PÈåøbêOvpúÝ¤×ÍÄ«3!·Ú	'\x0008\x0001åôõÍuzzlÒéãmÀm¶,{1\x0007\x0001üÏ=\x0005trév	j//</p><p>J«¨\x001be#¦}@ôªZ}å³ÝÍtåå¸8xã8Þäð0;\x000fONMiíï\x001b-ÏõkÉ7¿õ©\x00041xR\x0016Ôõ\x0015kÍnë÷vÖêrîç°÷9É=ë
¾Sí\x0013Í$7ºôä¥À\x0007÷q\x0005ë\x001eî\x001aÿ\x0000\x0017©ãØëjd÷7k<e\x0017Rpcô|ÆÑ\x0008ÿ\x0000W\x0008þñé©=As\x0006¦Ú[i©oþÇ\x0011Z'-9\x001dYÏR3É=\x000fAàs»½$©ÇCOæÆkíFúGÓ.\©\x0018î5GSþ­r>K`y\x0003òÏ\x001bêwºî «q\x0014pCmû«;8ø\x0004è6¯L9ëú</p><p>õ\x001f\x0014K&¡¨C\x0004.0Q\x000cCrí\x001aÇ\x001eÙ\x001eýé³h°xy¾ßu\x0014W~*ò´´\x0000:[±èïêGnÃ¶zÖªÔõ{ÕÓ¡ËxwÂÚo4Ñâ\x000f\x001eÝ%µÑO2\x001b8úA\x0004\x0011ÀÎC\x001eFî0:\x0010rjßS³³mB\x0015Ð|.%?ÙÚT#2\·÷ÕO.Ç¼¯Àíï«u¥Á©Þ\x001bÙ±¬k%ò\x0012oÞ$RgøÇñw*ÞðûR\x001aÚÎµ\x0015Ýþ¤Ã]7íôHÔô\x0000gæà\x000eëKÔwJ\x0010 ´ÕÙGgq¦/ö}IÇ¢@qç>x{\x001cÈO\x0018^£VÕ<Gqj¦\x000b{8¢^c[£·ôûÜI\x001aþ[¯°è°\x0004r\x0004Gê­ß.{öØ£"·Ò´ÍÑ¿zËµL7\x0012Üq\x001a\x001c3ô¨uáMÝ\x0016èJ´m-\x000e.ê9í K\x0013x­7çdvá÷È?éc\x0019\x001fí7Ëîk\x000eãÆÑØJË¢´ÖÐ0ÃdãþºH[w¯</p><p>\x0000úÒjú\x0007{%÷õI,\x000c\Àí\x0017÷\x0003<\x0010â1ÈÇ¥aê\x001az«i^\x001dÑ`Óm\x001dt§ý"òR9\x001bå=:gj\x00009î*þ±&îcõXÅZ?yÜxkâ\x0016Ó¬z7V$yÎ¡\ÿ\x0000xWò?Î»ùeP²ÚÈÂü¬ÁÕ¾I\x0006¼V\x000f\x0002=IsâItÛsÈY	y?ë]¾¦º_
_¶ºÛáæÖÌÿ\x0000~òä	er;²ðüëHâUícysJ÷=:ËNù\x000f`Ê¶Ý WÏ^µ-4áb\x0016W<×ñÈª~\x001d
N\x0007¹½Zê&\x0002ê\x000bsæ\x0008¤ÆJüÐê4ýFÑ\x001cC\x0004/MÊ3ú÷ªuÙÔçúª÷ô(\hòÝ
\x0013©5T[Ansu.[ûò:Û×µ¾èçùO\x001b\x0001Æk'
:÷«¤å8Ýõy)ÊÉ\Ü´½	·cSß©5j{éÁçëX6¯ûÅ\x0015n{# rÂ«Ù«Êr+ÜÊæN\ÿ\x0000ßUbÉþ\gÖ²`ò\x0002ÙÆy\x0000à×U§-Ô¹³(àxüóEI¨-QThûMq1\x0018æªFeÈ\x001aFôQVÚiöÓ¹Ú^x\x000f\x000bõ5-£I¨[ºÛJ¨­ÌQ¯$c®zÒ¡Õ²ºFÑÃkfõ0æs\x0001Éìyæ«}Yd\x00028dr{\x0005<Öý´Vö÷Jð}¢êtä\x0005P«ÓÞ}â\x001bÈ'hþÊ0þ\x0017$Y·h£EUæÎvæ\x0019bSçFÑ2Íf³\x00159F+à[ú¶©&¡\x0008à\x0005</p><p>r6ð	õ5Î¾7\x0010Ä\x000c\x001eÕ¬\x001bkS¤T_ºÌ{BÒu¸6êúe¥àÁ\Ë\x0018Ü2;0Ã\x000fÀ×ëÿ\x0000\x0006t\x000bÂ[Lº¼Ó\x0010ââ1ôÜC\x000fÌ×¯L>LcµCic-ôÆ(Z%`»¿{ AÇëÒã\x0017¬§)­"|µâïºÞ\x001c\x0010Æº\x00192Ú\x0003\x001fí!\x0019\x0003ÜdW\x0000Pã{×Ýáó÷\x001eÌØ¹JóÏ\x0017ø#E¿¼=[L¶ûb<ð8SÓ#æC×¾}+ÒR~ã;IÁ~ñ\x001f*\x0010sÚ½*×à¿AëO¤hK0
\x0019Ôõ\x0008ãf\x0007¦\x0011K>}¶çÚ·µoºc9:v¥ul\x0008'dÑ¬?QU´\x000f\x0004k>\x0019×ìµ#U²{)Rh¾Ñ\x0013\x0005f\x001cà:ÞÕ¨ÍlkN½&ýædÉá\x000f\x0003é1\x0013®xí®®öF$ðRúVÿ\x0000\x001bàÌ"6ºÅ¦¼4ã\x0019+y©]p\c\x0000Ç\x0002\x0001çÇ\x0018¬Ý{ÀzÇ5ûÝ[R¿Ó£¹¾ºyåX\x0011ÊìX\x0007êxÏãZZ?Â«XFëÈ¯¯Ü®6¬l\x000f¯ËÉüê=Þú\x001b{h'î«£Ô,|3ð\x0006öãÈ´¸3ÊyØ²Ýp?.\x0005Gâ\x0004|(±ÒäºðÜLÚ¼xh\x0007+®r3ütÏ=zV-olà\x0010éÚ\x001dÔ1c\x001bb´q»ê@æ©êv·V\x0013ùwÖÓÛÈFåY£(HõçµmN¾äUÄ6¾\x0017o?øb×v¶7\x0012NÆçÖ»&àô®+ÂDÂA\x0016\x0006r+¾\x0008¾µèÃcÄ¨ýáÓÂ\x000eý£n\x0005Ê+\x0008¯b#­÷Z@;1¼{wÍZ´»ò+{{ù°aRZ1\x0010\x0001qüQ_þ½mÿ\x0000Â={ovntX¦ÂmÞG\x000cJ\x001e \x001eµ\x0006\x0005ÿ\x0000évEÁN¸Çû¬2GµeÈª#xâ\x001d\x0017¶­izÍe{\x0017«G\x0019c¿× äF[¿bé×ÔÒÒãÃUY\x0011Zhao\x000e\x0015«p}r\x0008õ\x001eõ¨ºy{{p½``Öò"^»3Ý}=+ª¹Ð­ï/¾Ù\x0014£,\x0014H§\x0004n\x0003ÿ\x0000{\x0018¨rö~ì¶fÕ½èîëOoSQcq\x000cd\x0003 ÷\x001fCõ§éöÂh\x000bí­um19\x0014òy$0ôàGô"µm-c¶·\x0010 ýØÈÁ9¦-¶.\x0005</p><p>\x0001ÎGñ\x00021Ír9ÝYF¹ßsñuÁr5$L²²ºzÈ:\x0013íýkFç\x0006[=R1\x000c?ì¾\x0003~D\x0003Z×Öës\x0003Û²ä\x0015È'±\x001d*¶l#Ó~Ë&\x0008RHúg"«ñ]Í%\x001dlj\x0003Ã×ãi%µ\x0017î\x00123Ü|éþ\x0007ò­µ`r;§w\x0017êÇ¦Ò1ïk:oW\x000cF´ÚG\x000b¥éÑ¼\x0017¥D8£<`\x001dÊ8ÿ\x0000¾ãF·\x0018¿]5-c\x0019Ô\x0003]°÷òÇ¯¶ãÍmC\x0000··`fI<÷\x0006L%«©k	\x000f,eí­#=òv®\x0001ì©ZÎç</p><p>IÙ\x0018ú<ÒË¦½ºË\x0011(]Ù\x0018Lç¯\x001954\x001a_ÚuÒ n·de\x0008\x0011Åñ~1ìk¥Ö56ñ¢ªÇ\x0016[§ ÀþtË8ÒÆÎIX`ãsAõþ¤×;«­ãÔïäw÷¶F7îä\x0000i¶ïq0ùN	çóéôÍFÚt¶q¬w\x0001w®Ö(1°w úÀ÷$ö«z<\x001fn¿kù\x0014*¯¨ûÍþ\x0003Ò§>«s°-c8\x000eyÜÞ¿Z|âù5Ïï?Ëjº¤Q4Ûy\x001a\x0010¡F>XÐ\x0003 ¼u«úlqhR®$\x0013ë\x0017?4c÷Kõè8þUÔÂ°Åb>ÄÑ$>x÷?Î°lôHL³]_9h\x0018îgÍß'Ñ}»õéjª³Ñ\x00138Ê\x0016åÕþ\x0008MBÿ\x0000íV¢ÓLG\x0016òf?52\x000b\x0003×iôõ=ë¸´¾»Ô\x001bL²{E[²p¡;*·8OR:ôç¥ww¯5ó\x0018\x0016ºZ\x000fÉÚ_Ðcú~~â9\x0005¾Éj\x001e\x0008\x0001\x001b¡Kt;+7U^z\x000eHÈâöÔn|ów¿õ¡Q\x001bLð­½¤ðÍ~Á£3\x0015Ï*9	ì;÷'\x0003¯N\x001aææ[û©Ôf&I¥vÃËê]¿@íÐ\x000eµ³má~ñZñ¥9À\x0011B<¸bUè Û\x001fÌíôÿ\x0000\x0005éZm©	m\x001c\x0019·\x000c ñzÔ\x000eäö§'N?\x0016¬Ò\x0012©m48Ý:ÊÏHµ¶ÕoÄ\\x0011öxí¢"âç\x001cÏÜ`\x0010\x000f^§\x001d+b
OV×VU\x0017\x0011XÚîùHX¯³H\x000eY½h\x001d7WF|<.®L×jN\x000bçæy1ÙÏ§\x001d\x0007\x001d*ö¡jfÑÁ¸`:¾;\x0011éø~uÉVN[\x001dÜcæÏ>×5}\x0007ÁÐ¹¼o</p><p>\x001c\x0019@y¾\\x000b çhõ-\Ä¾$ÕõX\x0004Út\x0007I´\x0014þñÚ'ÏhÂ.óôqþÕz^\x0015ÑVêY#Ó­ZåÈvXØrÀàýrkBM\x0016ÜLd\x0008\x0001n$lüòqÐ¿\W7±êÍ½ºêxEÃ$¿¹ûEÕýìVÇ"V4ûDò\x001eq\x001c`¶Ì}ö-ÜÒµî¿koo§øÃí¡ØF\x000bG5Ê&OÞbíÀcÜò{q^éo\x000cP[ªZE\x001cqòª®Ð3ô®Äº\x0004ºâ$ww\x0012\x0012±ÃêFA<öà\x001aÙE½\x001b3UÔ]Ò<_Hðýî¦"y\x000eµªÉ&	y\x0019!
~i\x000eIàt\x0019ô­ß\x0018è·ZN0Ô<E¦iF1iöQm\x0012\x001fL¹½3}+ª·ðµÒ$öÈ¢Ùâl¹_ß,\x0000|Ì1¼gð¯9ñW®tk¨Þþi.\x0016Vù¤2¹\x0019ç¨ô<\x000cýM\x0013¥ªiè(âouoëÔç<%¯j~\x001eÔ-fÓµ(íÒá±<\x00049>@Ë¢¯§ ¨=?</p><p>÷-\x001fÆZ>¡4Q\jº\x001bÞKÂ*LRF=\x00067*^a}§Xh¶bé<1yu\x0011#ÊU¸Úã<C\x001e\x0001üIªºÝ÷+ÚÙýJ=î4¨"TØGñ\x0018÷:ñ×&´ìEJi§Î{½í¬ò\x0013Ëcû¤\x001aÄ¼¶,EQÜ©¯ øaâo\x0016ý¦=\x0012ÎÉuÈDDÂ·2\x0018ÞÝ@\x0000f\\x001fÝo^\x000fA]üM¬xJløm2T\x0001 ÓZT\x0011ÉÉ26\x0019qì¼ì[hÙãO\x000cïî¦u\x0016$y\x0015ôøf\x0003ñ®6ÓâoCfK¨ÈRHkr~jÓ²×ôÍl3éö÷<\x0006(ó®zåN\x0008­\x0014Óz3)RW¼ÑJ\x001aB7tü+¢Ó$">\x0019`ägÊBPJXczéì^8­º^ê\x000fQN[\x0013O}</p><p>o&_\x0019ãÒ­i4\x0017HèÄ`þbªêQ\x000bk¡å6ø%_2&Îr§ú>¬ó\x0017,}\x0005\x001aJ%ûÔçètWÚÄ6ÊM¼`»rI\x001fç5©k\x0011ßÚ4sZ¨cdýßëS_ir0+\x001a¤}ÚI\x0002Õhôcp×:ªç ç®u\x001aqØëu*ÍldÝ\x0000#\x001b«<ÆX\x0017\x0019 \x001c\x0013á[Z)¶+³ÇÎ0Hÿ\x00009¥Ôu(nmÂÑ$·±È/°$9ëÏõ­\ØÆ\x0014Ó¿3±27ÉªööÐË+«¨­£^Iu.Oûª:þ8®GÓ ~âôï}¤\x0002JÍM6e`¦B\x000e\x001bÎR3Û8^j\x001dN°¢·¹YçÒì0X½ì¬½m©ÿ\x0000~×¨úçõ\x001b[+ h ±Â¾:ã¾+©;{;e¸kW¿¼<¤&&ò¢÷n>síÒ¹RîïQºy¯eyf=Kñ`;\x000fjPßCJå÷+ÇãT_'\x0007\x0015£z \x0011¸T_\x0007<ó[Üä&Óµ[­\x0017RúÁ."ÎÖe\x000c0A\x001d\x000f±­ù~'xVù#ÏLA\x001fõ\x0006¹\x0019Wå\x001b»{`U6 ° ôã¯jB/VtS«8«#¬¸øâÎ5R\x0007lC\x0018ÿ\x0000Ùkñ\x000e·¨k·\x000b>«t÷2¢ìRø\x0018\x001e\x000fSUfë9n»@?Êª¹fË\x0011géIB\x0011Ø©U©=\x0019¯à¿ù\x0018à\x0007<«</p><p>ô¯³¨?t\x001aç|\x001d¡hÑk\x0016ÓÃâ	¦(s\x000fÙ¥R\x000e9\x0019#µwÇLRO©X2ú3ÿ\x0000­#Z)\x0018TÃODiM«é:êf¸Ô´éÎ\x001d£ÈÏ]À¯Oåí[/m\x0006»¥5¤¤W7\x0011âd¹- ÐõÃ\x000eÇiÇÒªëZ4××ºbËûµ·fs&ì3\x0012\x000e\x0014v<ãöéW|9¥Ç¥ßJÂ\x0006I²XÄÄG!ë\x001fEn:åVR6§&ÿ\x0000wU\x001cÚY_CsåG\x00133¹]>hÜ\x001fâSß>Ýèöfd±-ØñéÎ¯$j\x0015\x0015UG@\x0006\x0005ISR¼ª+2éa9s Å\x0014QX\x001dBQZ(\x0002ºô¶NÛ\x0001úóRº¦»wz^´ÉåÒÅ\x0008ìQ¼`2²Øÿ\x0000«1[Ç\x0011%\x0017\x0019bçëS\x0001Z\x001c\x0014i¤åmÆO@=Iª´-s\x0002[¦Gãsz\x0001É5\x0015\x001bü£\x001eÿ\x0000J\x00165tRxÛKs°mÁìBôÏãÍ\x000fdJ¥¼måÚ\x0001Uà°ôÏ¿þ½h\x0005\x0003 \x00148éè(»\x0017)Vâ4\x0008î\x0010\x0000"UàßµT»"ÝjER\x0018¾eNXÛæ¯ÜL°Æ\x000b[<\x000cÖmæ%øV¨Àþ!Àü*áo´cRNö¬äµ¯\x0013]_®4«vEr¨î»Üÿ\x0000¸½2\x001aÎÒK\x000bx¦Õ....\x001cBçÌ`\x000fEô\x001fSØt®ª\x001d)#â "ã\x0006@?xG ?Â>r+\x0018!R\x0014	·;N9\õ"·x¥Ë\x0005c(aäß4Ùm}5Å\x000cÑ,m'"\x0008LcÑqË\x001e'Z6s!\x0012ÈÝ8;\x000fÍ#¼z\x000fÂ¦û:Û£}%ó\òÌV=MP¼ó\x0015\x0004W¤ÜåT\x0015E\x0000órÀW\x001cÝÎø¥k\x0013\jp\x0000ÑÅ*ù§¡R\x0018\x0003Th]Üñæ1ÁÏ\éHÐÄ¢(Ö2c\x000c\x0006ÔÊ¨ÉÇnMY±\x0012É\x000fÎ\x0012\x0001\x0011\x0014qÔ\x001fÀÓ^cv[\x0016b<\x0001ÿ\x0000}\x001cøÔ¨A\x001cr?:,jé»i\x0019\x0019ëé\x0008Õ\x0018\x0013óqÛ~ð08§SyÉ? \x0004`6\x0010@ sÒ«NÈ+÷yR\x0010\x0002sé%ºT¹KvBK®I8Æ:cüñP\x001bãº·É|2\x0012JGûµÇ@X\x000f§ãNÄ¶sÚ-ÛËw§ÚÃ\x001dÌ¹dk¥/1Éù	ç±ô®'Pð<6i-Åð¹\x0004\x000c¿Ø­öç=~s×¡ê7BÆvófxÙä
"ÂùÎ@\x0003\x0000ééO±-b\x0007à\I\x000bc"WÊ8\x00073üªog¡ªm«Èæt\x0019´ÿ\x0000\x0006x\x000e}f\x001b6[¬I\x001c3OºY»"ä¸Ë`\x000e2kÅ|uãÝKÅÊ÷\x0016\x0010¤Ê´$4©»dòF:ãÒ½sãUî¤ú.¦\x0010];Dª\x0010\x0000\x0017\x0007v\x001c'\x001c\x000c\x000esÔcz^k\x0004\x0017V\x0011K; yahn¤ñÜ|ÝF1æÄVqv:ðÔ`ãÏ'f|ç$ÓG<2Í f`§gA1x#¿½U¶KýFåaÓí®¥v\x0015aøë¹"¾­Ðü\x0011 A4ÑG¢i¿`?´¸ò°Àá</p><p>·M¸<íÆk¥\x0016zfg{\x0016¢Ò2\x0015Ú=¨\x001c $\\x0002z\x001fNÕÎë7­Í¤é­-sÇ<\x0007oã;\x0008ã\x0013@%Òf;c¸»Vx°¬~æ2ËòãæÃ\x0002{×sª^\x0012-´«%HÌò\x0018T1\x0019P@Sò±à0?ÐÓõÖ½{è&*cå|¡'q\x0004goC\x000fb\x0001<\x001cÔ\x001a]Ø{Ñ\x00126Ûw@\x0018;~ll`Ù\x0019Ü\x0008È\x0019ázqJYT¹S3WJOÄÌò<Y#È</p><p>iÑaA"»¹#8Ë°\x000bïÛ½[Ó ñR"Ë\x001e±cq#¡ÁÍR4o9\x001c¹+\x0014cqî\x00009éôéâ\x0015e&ÁWVR¡GAò¸éÔ\x001eV½´*\x0019\x000b`îÀ q;c§ÿ\x0000®£ëµ¥¼\x001e68Kñpe¼ÊñØ ÁÌJ7wÎI8ÈíëR[ÞêÐÏ(GY#C<±Üí^¤q¹\x0001=\x000f×Óô!%cc\x0003-èqÉëì\x0005%´ziQ\x001aDÈ\x0001à3p{qÍm\x001ceH+ó\x001có¡FzÊ\x0007j\x001a×¶]6Péþ°¬«µWÕIÆî1Ðzú\x001a]^ÛÆÏ¦áXGÁ\x000fd\x0003Óå÷98\x001cW[¨iê\x0011H\x0008òb%;õÈÁ,{ð\x0000\x0003¥dL\x0003Î\x000c©½QCÁ°ÙÎ\x000f\x001b³\x001e¸\x0019\x0015³*Ý\x0019­<·\x000f%~_Ä«mâ-VÇí[i\x0016$Ció.2¤¸$\x0003Æyã =j	¾#xmüØ´Fm¡¼¸ÜîïÈô\x0019\x0003½]³"]Ec\°$gqc÷³ÎFHç×¯k¢K}#[Yü»ÈØîØ)I$c9ä\x001fÄÖ/\x001dVO}N¥¥Mm¢ O¾!¸\x000e±ÚÛÅ(:Æ\x001bs³\x0013÷@ÛÀb\x001b88=+>}}.¤}OÃöÏ+3+ÉbóY@ÜW#\x0007\x001d	Æ3ÀÍjê~\x0015ºÒ¤ód\x001bH¹d;³ß©ç\x0000\x0000\x0007Ö³Z8\x0005à|EæB@YNôBI\x0019ÇO-ô\x0007½DñÕ ìÝpÂQ¨®hÅ¾Óo.ç?ÙÐÅo\x0014êEË<P ¹\x0014\x0003×*èwñ1ÞÖûÐcedVÈ8RÄñÿ\x0000ëã¥wL¾XFÚx} ãôÏaút=¨}Ãîfo0î18lõ\x0005Iô-È</p><p>o1¬Õ¹Y}\x0014ïÊr\x001aoçy­ïdi$eÌf1³iÆH=IíÛ\x00078ã\x0015uô[)µ1\x001c¶â5\x0016P¸Ç¹</p><p>£\x000bÐ\x0006Ï^Ãêk¢··1Ê^e,±\x0003\x0013Ëcäç'¹úVx6×\x000f!\x0019i#UT\x00048\x0011«\x0010I\x001cá?¯^k\x0019c+=\T¤QÊxßìºOîîfÞÕ6DtS¹Ø`à\x0002N@Ç\x001e½\x0000çæËzóûZk»Ë¯µ6\x0015ß$·pqÒ½¯ã¡</p><p>è\x0007\x0016Rrê½$È\x001c\x0003Ó\x0003`r}«Åô\x0008êÚÝ©ºÓ­\x001eíY\x001d§\x001bB\x0012Iàc®+ÑÀ9UÅ<*Z#©Ðþ!>'Ú	®\x0017"6#</p><p>2:°\x0007§½I?õMRSss5ÌÜ\x0003\x0006=\x0000\x001d\x0007µrIá=nÖ@·µd_hÿ\x0000xsÈëR²²\x001dLYWØ<×Mu'esÌx*Nk©úA1~aò¤d\x001a\x001b5]Ð»ª\x0013Ìdå\x000cô«bè\x001d»¢(((¢\x0000(¢\x0000(¢\x0000(¢\x0000(¢\x0000)\x000fJZ(\x0002\x0001\x0002yñìO8©-\x0014\x0012[	÷ g'¦)h ¢9#Þ¤\x0016`\x000f¥Fð# \x0010\x000f\x001d@éV( </p><p>ïm\x0019L*\x000e8\x0004d¶ò:\x0000\x001cpA\x0004g}jÝ\x0014\x0000Ò 2;Ó¨¢\x0018îª2ä(êI8¨7ls/î\x0000\x0011ªç^9þch,\x001b\x0003=z^\x0007&+]£Mfê­±Ùp\x001b\x0004\x0015Ï·ZË]"îX\x0002\_8\x0003\x0000*ò6GBHÁÏ­nõ\x001c~u\x0017\x0001ó´äM13o\x000fØC(&Ú{</p><p>ýö'húÅmiÁü£æD*ü¨ª»p¢¬!f<«s×µ9\x0014ª\x0005$¶\x00062i\x000eç\x001aÖ©¨|L{.-ÈÓìv,\x0002BÒ\x0002ì\x000eö\`\x000c\x0002\x00079«ú0ùò¼ç|`	D{qd\x001dÄîôÀÇ­EáØíÄÞ#ºK\x001eæG\x001e(Îã\x001a*¤u9'\x001eÕyÌ"îHË\x000c¯ÌF9;OÓ\x0007óæ¼ìJÖçL[ON¥swik\x0016\x0002HZ5x¹rHÆ\x000e8õàý+Õ¯f,QÚ\x0016çV\x0016ªÒya@'v	È`\x0000\ãìµ8ÂÀ÷	`·\x000e\x0011°c©9\x001d±íÏ\x0019®.è¹¹{+\x001bvy\x0015fx&mÀ\x0001´8ÉÁúç$àªÜt;°©KT§dúF¢-NS\x0013ÎÒÆOß\x0000eÇ\x001d=2@=»Ôþ\x0016Kè¡·\x001aB3\x001d¾c¤¥dØ\x0000ÀOË#×$\x0012NMtR]^Â\x0019H®¡òÜþù\x001aN\x00060yç> ó>µf\x001dJöÕY\x0016èÇåUUX÷÷\x0007;\x0011X(«Ý³ªUeËÊ¢¾òì\x0017³E(x7v\x0018pzõãðúÕÈ'yb\x0000Û&æàY_Úä7P8ÀP?\x0011\x000f~;Uøo§pvÜ+åw.Ñ×\x0007ÕÐ¦³¥7½ZHÌù\x000f¯\x001dý³YV4tgØÁI*á{îGå[7\x0017rðÒí
×=@þ<ñ\x0018üß6Þ¼ÿ\x0000ëúÔM¥±¥\x001efµ-iv\x0016wbæUy\x00036c\x0007hÆx\x0004\x001fl~9©_@·µ\x000böK\x0015\x000c\x000c=Ãqp}ë½\x000cLK\x0010HÁèpO<úqÏ±ªöºýßîçÊ*LlÆ\x000c\x0000\x000f©ÎM/kNÖ5\x001e¤µ¾F¬×[=>Þ2tùr¹$ð\x0007RH©§V8ç±ÓmrwFªH\x0007¸\x0019ÉõÇzÀiYî&Ë\x0015;ÇÞu\x0004ã\x0019À<})e·$ù`\x0003\x0008ßæSíéÁ9<qXªÔÙá·ü?êtÖÞ"Ô`ÿ\x0000´ô¦U^^(?È?¯8ÕU?´î.\x0004&\x000f´HÒ$y</p><p>	!'ýØì=*Ù¾Ô Ç\x001dÝÀÌ *«´c#gwStÆzV}Ö£ªÛÃö¤#BãÎ`J¤u^AíÜÕ½µÐÒ\x001fc'$¤ÂòMÒ,\x000b&6Ê³,Ùíp¸Ç=O\x0015¿g:K</p><p>ºcÊc¸îR\x0001\x0018ôük"ÏJ¼Ô¡öÑ\x0017Ê7!8\x000cF\x000f\x000bÜw<~5jÒ}\x001eÂªw½\x0001\x0003\x0018öê>¹ö¢1äZ¹)»"Ö¤âÞÎ\\x0016HÈSÜb¨Å\x001a¶\x0014DÒM+0?)P\x0002ëëo­YÔäÍýÊR\x0018JóïTté</p><p>Y©6QY\x0019ýàÆA^ø\mÅCv¸nÑá\x001e%>\(\x0018\x0002É\x0019\x000cF3îÃ×õßz4v¿\x0006,¥ciï¼ÙõÃP}\x0000\x0003ù×|q,bå}¬ï!
	\x0000ð:1ÙÏpkè_\x0010\x001b\x001cIÀ\x0019³/ò\x0003÷X³\x000fÇ\x0007ó¯£Éõ£så8-(¥ÔðoÊF¬_\x0019Bý9?áßëÞ¼½åXÈV88í^Ïñ1tK\x0017[ÉâdÔÎÑ±ò´æA+88B|Á·¦rzã\x0015Å]j</p><p>#£i~0b8É½~q[ÕÖGÃ:´ÓºûÏ¾(¢Ðõ( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002( \x0002*A\x0019\x0006ÒwÇ4\x0000c\x0000)qÅ\x0014P\x0001HùÚp2})j·2[é7rK·`²	\x001f0ÇA9=\x000741¥wcð¤\x00170êzü´SÏ:3\x00136ðß Á\x001e\x001ccÚ ÕoÖÞIÚ\x00049âBq·9\x001c\x0001éÏäs\ßÂ	fO\x000e^HË![¦\x000b6[\x0007ÉêxéRëF¼»p¨72FÂPÄóç\x0007 \x0002p¸\x0004x\x0006¼:õoª=xaíYÆDºnÏ¶wÚ\x0015¸L\x0014@</p><p>\x0018ç\x0004ýãÁÈ\x001dEB/.³\x000ef\x0013)\x0019\x0001R	ÆÜ`®pO<|Â¹v¼y£i,²òÑ89ÁéûF\x0006OÓ\x001d</p><p>ì¶ß*m[È¶Â\aA$À\x000c.sÉÁÀÇ5Ãí\x001c·=\x001fc\x0008i\x0014X±·½(É ó</p><p>Lå1é¼à\x0001é}*õÝÚÏ*\x001biC&Fõp`Àr§\x001dG\x0019\x0007®+>\x0019.#òÃ)ISj°øÁ=89÷üñÖ¤»[ÿ\x0000&2DÛ.\x0017z²:\x00103×\x0019ÿ\x0000</p><p>9´Ñ\x0019¸Kt[ÙåvY\x001d".\x0000&c³#¾\x00068è8àòy­k{K§÷¶ÎË\x0015ppN0~¸üóX2\x0018åmÆi|Ì1%U°F9ëÀ5ÒiÚ¤&Ø5ÂF&'ø"è:dþ5­\x000eGñ¸i\x001f]\x0011]Ú_yr\x0014³î\çÓü+2Gi\x001br¯ÈpÃ\x001cs×±ö?¥t\x001fÚVÈø äÿ\x0000v!ÏëPÍ{g$\x0012DÐÊ\x001dFØÔ\x001fÃVÓ§\x0006½ÖaN¬ã¼N^þF\x0010ìSÚÙ\x000bÜñòçÔ?Éª7ÒíÞæ6\x0005²\x0002¶9#q\x0000\x0001ÆqÞõ¡©ÊÂ@\x001aHnrûGCè;ÿ\x0000Z§w\x0000`»\x0004ôÜFÜ\x0010\x0007\x0018ükG«Mè*Å¾&\x0000»K"!'÷\x0004ð8ã=\x0005U¾G:;D\x0015K!À>_Q\x001b¾½ªíÙHVufRóÂnûÇ\x0000\x000fô¬ëi¤÷»$S\x000bE\x0007¹<ãõíYÞÚ\x001aÚúZÇö\x0015\x0002*YNv¡èsÄzu+÷¦ê*\x0016ábTX"fgç{\x0012H\x0000å½=\x0008«pä\x0005lvÑ¶ß5K\x000có\x0007$8\x001c\x000cñëUî\x0007)*ÊQy</p><p>çå\x0018è:ëÉú{!Zåh.®-VEa²F\x000eÈ¥¶¶p7\x001fÏô©Vl\x0006\x0000áå\x0003åÝ» 
¼c¨Ï8ãëU.ÖC&Ì¡iYÎår¥So\x0018õa1øÕxA_1BýHÎd\x001dH\x0007hî8àçëíY¹¹\x0016 :7."Û**:`à÷ãÒ©G6-Ä\x000bæJoðsÆÒ\x000f ätïô¨\x001dTY(ÉläàIèH\x001cã88«a\x0008y¸åYví,Ä\x0010\x0006\x0006z\x0003×½RdÊIXðï\x0008\x001aÕW÷·$o\x000c@\2\x0006^µôÂì\x000f~\x0018Ã\x0006\x0003KØ\x0015ó\x0017Çv	©\x0018¼\x0011\x000bìdR\x001c\x0010GÝÛÓ±úõ¯eý|Y\x0016µà?ìkC^é\x000ccÙ¡c?@r¿¯©Ê\x0017-\x001b\x001f%ÄÔåì1ø÷\x0004¿ðGqËE° g	À>øèxãÕá\x0017$2OÞ5ö7Å(ü/&¬j>\x001b7·R\x0003å+êò[yÍì\x0018\x0018Ýø×êZÿ\x0000Ã>úk[ß\x0017°ÜFØt[\x0010~kiTµF­©Ëá%\x001a*wM3ï:+\x0005uÄá^N;</p><p>}¾®%-EQÜõ­yMÓmÚÆÝ\x0015m¨yÒ°\x001fpuvâ¯$èÀ|ÀgÖV%¢sÈ¢</p><p>(¢</p><p>(¢</p><p>(£4\x0000Pi¬ê¼±\x0000{Ôw%´3ómÈ Ñp%'\x001dH¦´±¯WQõ5ÄêóÇ÷÷\x0002>¼Ö\x0005Þ©*§ÌÜûÑt>Vz^Ú¯Þ¸ÀÅFu+0Û~Ó\x0016z}êñù5RÌ\x0003»*eº+[Åº|ºUWö\x0006æÂL\x000f0c*ONÿ\x0000®¢ý=\x0015õ­9~õÜ_FÞ ÒÇ[Ø¿Zð{ÝojþíÈe\x001f0ÍPþÛ\x000cyc·¾ãRä©6}\x0000þ*ÑÓx¹\x001eÇúUy<g¢ÆÄ5ËdzFßá^¯j\x001e\x0016Õ|1&©c<:mýºd[\x000b½±Âmþ,ö#ñ¯)ºÖ\x0018e²\x0008=Å\x000eh¨Ð>³ñu7a\x0018ô2)P\x0013[\x0017Wb+6¸).T
Áa*K\x000fl
|s.¿(Rw\x0015\x0000ñÍtZ_µ;]\x001aDþâÞ'R[dÈ#ôúÖR®¢Í\x0016\x0016ësÜ[âvc\x0012%½ë!ÿ\x0000e\x0001\x001fê¡'Åí HR;\x001bæ#þ¹ãÕóÍ×ôaP÷p\x0000ÆÑÔsÚ²¿á1ÒmÆæ-¿0ÚN;Ô{yv-a£ÕJ¿Åû\x0006`#Ó.[|Ò(ç\x001fD~0Ø	ÕN1R¥¸OOÓð¯\x0017Ç\x001a0f;ï\x0010Hò»ãþ\x0013m!\x0000\x0002D*ªÉ,øT:Õ:"Ö\x001eV}L¿\x00164³\x0018caz\x0006qÁBhiß\x0011ôkÛÛxcóV)¸\x0012¸ÆÓÓ\x000c:­|þ;Ó7BËpdî\x0004vã\x0015«á\x0018i
\x0000·3+NÓ0\x0003\x0004±SÎ};â¥â*-Z4XJRÑ3íaX^6ºÓÃ\x001aÅæ§ë·8ÉÚqÏjå~\x0017xÀ_øEÖí¼Ë>O³n\x0007>b\x0011Ûñ^\x000fºæ¾8ëû¼3\x001e\x001btWV¬Ê\x0007\x0004\x001eÏ±\x0003­tT«\x0015MÈå¡¬ ûü.ºsáK	Íº(*vÛÕOr\x000fo¥k^H·m¶áÕæ\x000bâ]Ì¥S\x0000m\x0019#,yÏ@\x000f5Á|9øuá½.
:kh®­A%\x0014¹äà÷\x001dzÆ»è|cà\x0011@MÙ:mÃ)`íû¢3üJËÆxë^\x0004g\x0019ÆÜÚùE¡ZW7Mò÷Z¼;u\x0003é7\x00176±¬NBì ¸c6`¨\x001d¬k{«VÝ,ÊbG*w\x0010eq½×\x000b´ô=ÇLq\ïÄ½R\x000f\x000bÛèº\x0006pWa:P\x0003!f>^GcÁ'ç\Î«\j²ÛÛ,ðZ¼c½ÌÂ5\x0005NGÎyÎw\x0001õük*q´l]\x000c,§\x0007[£üg³ÒñÄßkÓùf5ËmtVbp\x0007=ð\x0000ÿ\x0000d}+~ê	&Ó-à¶Ù3Æ\x00197\x00121g=z\x000f¯5ãZÔ^ ²Ì<Îd`Ó[þú7Rr\x0006äbBç¿\x001fsIâÉ\x0019\x0014°\x000b\x001b\x001c\x0005QÀ\x0003\x001e½~´ý¿"³\x000b.gÍ\x0019§oê{¤Zf¡\x0014 ËbF\x0014.P\x0004\x001cóÝPs×Ñr°\x0006ÆX¤QÏÈp\x001fé^\x000b ø¦Iõ»%õ­-L¥\x001aRÌB\x0003»ÈÏ${sV·¼Iâ-\x0007Vm*úâVE0®\x001fdÈx\x000c¼\x001cäiF¤m~W÷®_WEÉ_æKQI\x0019WvÕ,Îz`ã¤äRµÜH¨ÅÈTV
\x001e\x0001\x0000ýzñÓß5â\x001fðÎÐ§J>YJ»ä/ÍÉ\x0007¹âµ4\x001dcÄ\x0017-&©¤XOu\x0015³a8\x001e¸Ûßèzö¨u]ìÑýã\x000eihzTº´Ì²F6:ðNF\x0001\x0019çðïEµíªÜ óÌ@6Öf\x0004\x0019ë®\x0007°ÍsZOmÊíñ\x0006¦n\x0011Ö4\x0003\x0014®prÍÉÚ§\x001bGrzp+\x001açÅ¾\x001c¸µK
6öÂõÈVçÍ9Ï;¹ü\x0000¥UÙsE\x001a¬ß$ ýUFÖ­&IÕ®\x0002<\x0019ó"\x0000GN</p><p>u\x001dk¿¹´´(\x0013\x000b\x0012¦â¤|½~ñ\x001d[¾GøWCá}KPøxeZÞ<Î&\x0007;Ô§\x0000¡'\x0018o¼x#\x0007½y'Ä)®4ûÿ\x0000ßØj6{nK]TÊ£epz\x001ek9ÂvM-Ç«RT[WÒ:§× ò#óîüù\x000e\x0014R©\x0001Èî\x0000 \x001e9¨Nµ\x0002¾fÌ0åAl\x001d\x0006=Àè0\x0005xÝÖ·0	\x001c/\x0007\x0018\x0004òq;{~5SûnxÜà¶áÆ3Ðzgò«T*=OBY}ºPéþ\x0019´×tèî´­^	g(\x000eÎªä\x0003Î?!\Åß|E¡©7\x0016\x0012^D¬\x0002=\x0012l\x0018%Î	íÆ¼\x0005|Ey\x000c«$\x0017\x000f\x0004«®C.9àWoá¯*ÒJ¥ÅÒ_À8	t»ýô0ß®¥^ò³ò8'ÄÁ¿g%%ÙèwO¯Cló#ü¥	WÜ6\x001c88é×¥3Qñm²ZÛ y
´xdàã\x0007å\x0003vç\x0004\x001aó\x000f\x001exòãÅZ«ßµ¼6¬Ñ,F8É ãø8Éç¿jæ5\x001dZv\1</p><p>æ%ù÷G c©ê}MDpón×5úSÑ>*êÑjZøKco÷¸nH\x0007\x001d2\x0000Á=êïìõâá\x0016fF\x0002ÖýZÒ|ú7*}¾`¼ýkÕÝR]·1=MS³¸Öê\x0019áb²ÄáÕb\x000ekèð±öpK±ñ¹\x0015IÊ\x000cú#ãî³\x0005üP¤jk\x000c:A\x0018\x001f_Ó\x0015àz¾¥{q\x001bß]K;Å\x0018\x001aVÉ\x0008:\x000cþ5Ûx²ðêv\x0010Üny\x0019ÓxÀãNEp2\x0015-Ï'Ú­ËW<¼%7Ar¦~j7\x0010iZgÙ"!åpíìF	ÿ\x0000</p><p>ç\x0016ã\x000c9Àô=«2YËmÁ'µX5û\x000c÷7\x0012\x0014ÁÛ\x0012ã=ÿ\x0000</p><p>Jg®©Ø×ûhÂªÔW²1\x00185ËAv£9À÷­\x000b+ÈxÄ¤Ë
ØôÏ4sì!ºËV;ç®8&´âºekÕ5´\x000b<-ºciéþ\x0015R
TÄsI8ç¥.c7\x000b«³»óP\x0010§ä\x001eÊÛjs`\x001fJ5fvÀo¹õ¦¤c-6:\ÑXË©¨êAç\x0015n\x000bµ@Ü´Ìùõ±t°\x001dMW¸»X9`H=ë3R¿òZD\x0007%\x000fê9¬µ!s\x001b#\x001fqÍ
ê;××(ÌoþíFº²i³¬P\x0019\x001e8ÉbN\x0000\x001fç5Ê]ÝêØ"¥²ñ\x000c\x0016ú]ü\x0012ûDë±\x0019G\x0018Æ9>Ù5
\x001bSfUÕôÁWp\x000fj òýªÚíå\x0013</p><p>\x0005F3U{é\x000f¹ÏC×5.¡=¬rF\x0002È0O­K\%\x001bÝÓÀ2Å#KsÍXÑemVúÓH¿ÕdGw%Â8À8Êõàe±Î1üë»{rÙ$ç­A¤é®»~ðh¶Ò\¼cy</p><p>@\x0000zHëRôFù/ü\x001fuáW\x0012¡{6VÂOTÿ\x0000uýý\x000fCúWÜ^¡v,Üöÿ\x0000ëWQ®|B×­|;?ïÖ3±Äryè|Ô</p><p>Àìü\x0008î+Ï®5H¥?½:\x000f\x0007ü))\§tµ,\ßI¹8\x0019Ï"³¦¿`§.H54g¹â\x0006v¸'</p><p>äú\x000cu&µ|{àm[ÂÐiSÝK\x0015ÌZ\x001ejù`,à\x0012¤\x001er7\x000ehm\x000e2g!=è-Ç\x0003½hø¯S{_\x000cË\x001c\x0004ðªéÁ\x0015Í_\x0016I6I\x0003p3V<a3Iáè[\x001c®@>Ïµgdä\x001b|<\x0016Îi»=ª>ô­\x0006Üç½vØó\x0014âH¯tðÀdñí5\x000cø¦ÂëSxÏc"m\x0010·÷\x000b\x0002H#\x001d×\x0007±Ç5á Ö¦®êZ\x001dìwzUìö1ýÙ!r=²*dB©¸í#KÆ~	ñ\x000f¯>Íâ\x001d2âÌB;\x000cÆÿ\x0000î¸ÊÀÖ
ÃZÞC:\x001f7\x000c0}
zG>4xÆ\x001e\x000e_\x000fkÎx|Åî<JÅzr\x000eÑõ\x0000\x001f×>`>õ\x000bU©R´dYõ\x000fÁ­G#Ä±\x0007>Q·e\ã\x0007{\x000fÃï\x000fÎ¨üOÕ_ÙÃ³*¯Ê7d <\x0007¡=}køI©¼Wú´q:ªOaÈn¥©\x001fÌÔ^8¸i\x0016VfÎSîíÔþ9¯6Q÷,Ïvª¤R·¼Å¬\x0007Ì\x0000á²	è?ÎJÏVÏS´¡\x0013E\x001cêï\x000eìy\x000epN;?¥z·Ãß\x000bxçÁP_|>¸6ÚÅ´Jfµ¸±fÇ!³÷I=\x0018|§ùxÜsi÷²Ás\x001bGs\x000b2HyF\x0004§\x001d9\x0006¸\x001dEÜúZ8Êxâ´kt÷:\x0016øO\x0010øïZ¼UîY]"gÎÄ\x0003</p><p>¹úwõÏ\x0015oUÉ|¬ßxàm\x001eÃ¿~+\x0000Ü»¸O9ííÒel(ÉÆx\x0000ÇÊR»»6¦á\x0018¨Çdv\x001aOu-\x001af}&ökIN2aÿ\x0000\x0002_º}zWS¨xoRñ\x0016ÿ\x0000	4×ãS¼S9¢©x(\x0018\x0005ÀÝòç§ë^]m9`¤2\x000f=ñ^Û{¢ëáõí
Äk§ØL.\x001c­ ?wø\x0004Ör¤ùZG5z£85däíÐä~\x001eÇáöñ!Æms
´±þâ@Jª¿bÄ\x000e\x0006?\x000cõ®ïâ\x0007Âín}.ÖçÃ\x001a×4»HÛìÖí.%\x000f$#\x0003\x001c\x000e8é^!©j\x0011G\x0005Ì"ÂÍ´·ÞÉ<ÿ\x0000J½áß>#ð»4Z6¥q\x0005»\x0018¶«§N¡[ \x001f~µµ(+{Èu:¼Ê­)ÛÉê¿à\x0014-çhÑáeY\x000er\x001b=>µ×ø7Æúç.çÒC\x001aîýýÄ)p1È?29Æ
yäÝÕ½Új\x0008äÞ	<Ñ#Ç~IÝõÏ?Z[ÿ\x0000\x0011>£4OxäH¤[nÎ\x0007\ûç&«ØKâ´±4&½kZÝO¢\x001fÇ¾\x0003ñ8ñv4ýEW"î\x0010NHéQ»ð`ExÅÜq^Ì,äv\x001dNËdÉÁÇ©\x001dk\x0000\\x0016\x0019VÈö4)Ýýj].o¬%:xkû&ìú_Eèvú\x001f5]\x0011ÃéóÛ±;\x0006!Iõ+Óô®ãþ\x0017íÞu§ëºU¢% wù\x0006HêË\x0008úb¼E¦ì=1Q´wz!KDV"\x001e³RSk¯_¼³4ÄMU.sÔÇ5\x001b5m\x0018Xî=\x0019\x001d(Wã¨Ç¥@I¥\x000c1ZrÞ×[¹à`c4Ë÷]Ü.ÕÚ0­ôÿ\x0000&ª³\x0006\x000e
2r¸%\x0001\x0003\x0003¿|S52«^éúe\Õ\x0010y\x0015bðüøàÕ~õéAh|V&\Õ\x001b;=\x0012µx{Èb?wº2OaÔ?ç\½Âæu\x0018À5ÃW\x001b'\x0006<H¹\x0004úþ¶i×Lä¶ò{í\x001cT½\x0019ÇnY\x001fux¢}bsn\x0015\x0010\x001d¼`\x0002GSXsÉò0,H\x001d9éM¾»\x0002CódôúÕ6)\ÊG¯Éb\x001f1Ñ¾ÿ\x0000\x0006®Ãr\x0000^zöª\x000f\x000e@lñõ 1aÚ´¹-\ÙûNÐ\x000f$\x001fÎºþ"y=\x0005Sr¤	\x0006BåWéYÝ´®Q\x0018`rXÐ¤Dé½ßü¸SSV`½Âç95ÉÅp\x001aS%\x0007zºnJ\x000c\x000cî\x001c\x0001þîa(t:#¨að\x0018\x00008æ­Ã­Éhþtd\x0016\x001caºs\Ë¢Ëþ9=OÈjYá¼1ãìóg?ÝéÅZf\x0012¦ÓÐßRkÜå\x001aËkÆ^¼</p><p>Î³ûZÝ\x0004zb¢»ûH90¹
Ó#E;¡{'sFúèK\x0016å8`+\x0012{¸<ÓZKäÛ$L\x0001éÎ¿\x0013+nT|\x001föx\x0014s\x0017\x0008YØ³6 ÈJÉ¸ã±¬­BO0\x0017Cÿ\x0000\x0001&©Z^Ø´gP·\x0006wGæ!\x001b¯5²Kæe+×Ö¦OC¢\x0010mïa>^Iä®x\x001d\x0005wÿ\x0000\x0000nãÄ¶¥²nmøÏª¶\x001aØøËkkqáÍ'Xµ#YFJ>VPÊ?\x000c\x001añß\x000eë×>\x001cñ\x0005®§eð¾JC©\x0004\x0010~ þum3t£êt?´Fö\x001f\x001cM2\x0016ò\x0014cq´ÍkÆn'ÆFxý:×{ñ?Æ^0Õ!»¼\x0018\x0016(¼¨â\x0014g'$õ9æ¼ÚäFÎÌr}û´_[m\x0012fïu·Ð<I¦ê\x0003µ¬é&ÆèÃw?Ïóí^ñûM¬¯4/\x0011éwAôô|m\x001dq*¯ú`zùwÏ1ç\x0007wnÂ­ê>$Ôî´ht¹¯î[NùÛ\x00197¨\x001d3É¨³ØÒ*-©v*KªÜt¬¸çç\x0019ü+©ñ}µ²x\x0016\x0006#/e+Û#áÒ\x0011,\x0012Köu(\x000fÈï?AÞ¶u­Iæð­³m$àñØ\x0003üèq|Ñ±IÅB^\x001aÊ¹ù\x001b?^)¬¤dñji\x0014\x000c®ãÇ</p><p>;ÓZG</p><p> <\x0000((Áí9\x001dF:P2lÄaÏÌ%\x0007\x0018\x0003S	ÉW+Ïài¨Ç</p><p>¤ç«±éì1öiUO÷ÆÑù­'dR»èz'Ã+§þÛ¸t#V²*UF\x0000\x0019_ëNñ{43\x001f¹^}½?:¯à(!°¿}STÓ-#h\x000cxä\x0013\x000e\x00179éV5¼5$²}§Ä±\x001cæÒÒI\x000cØ6Ð>¹üëpocÙXGVÌ¯\x000eëºp·Z]ÜÖ·\x0000`<LTãð¨..'¿ºIYæ¸Ë»\x001fäSM¾ñ'­`h4m\x0016{à-Ö£pK}Di\x001fBZ±/¼Qª]§'\x0016Ðd\x0015²\x0008zð ~´\x0019·s²YÍ(/u]ïgq\x000b+\*@\x000f Ná?Bi¥­Ê½õz|¥ù\x000cW\x0012ew}Ò1ry$µØxsÇ+¢Øµ²økÃw©òÌË'æ[Â©átÜÆ9Ü¶±Óè\x001a\x000cºoÓ¤k ¸'ìð4¤ÀG?+éSû'àH³¿­Â\x000cî¬>sS®q_\x001cxF\x00195_\x0011iöP\Gi%ÕÊD³\x0012Ub,À\x0006Èä\x0001÷ï\x001dAáËíFËÆ·Ú¾²<	íî\x0012Þ92</p><p>ÁÛ¨*A\x000bß½qU§*MÛ[ètÔÄýoïg¸ñ½^]>\x001b\x0004ZËà4,¹üûV<ón`\x0011£e j¯s\x000c³¹òZ\x0000ÇûÛçUmH]Pá£cò·P+¦\x001eÑ¸êæù\x001eÆó"É\x0010\x000e\x0001\x0004tôª3X)\x0004ÂvÙº~usp>¹4Çp\x0017,@QÜÖqÐô«Ò¥R>ÿ\x0000Þb³ÜZI·%}³Á«Pêc\x0000Ì¸ÿ\x0000hU=Rñ'!b\x0019ÛüUZØ,­±Û\x000cz\x0013ë]¾ÍJ7>kër¡YÂ®¿\x0003¢ur\x0018{SÙ\x001cW> 	ARJú­j4äç$¶g­ÇN¢j¤lÑ1Þ½C»ÒÀ\x000e´¹M][\x0017ÉþÆlTm ¦oÉªQ0dL_I§HäÆ	 ½¿­@Çv1N-ÁÇ¯>´ìO´ÜÈ»ÎþMWïVnþ÷LUjìÇÌ×øÙ%´¦\x0019ãz£\x0003[w%L»\x001d¬7\x000c\x001e¹¬</p><p>Òµ¸\x001eJ)^\x0006Fx¥8ÜÅ£ìÕ$1a;\x001a¤K,»wg#ÓÔ5®à\x0011Hêî\x001b\x0013\x0007?ZÊbª7óã#ÚWAòJBÎÓì*'\x0012p}j¬óËdâ©Mw¸m^«Ö´æ3q/OvZ/+$¯·J®å0ÚH\x0007\x0015An\x001f\x0001z)ê)ÌXgúé¦>SN\x0019\x0019\x0017(7\x0011Î\x0001æ¤¼ÔÍ´?+´ÊOÌ\x000f*;ûÖKÈñ°Ëp¼Õë[k­.+obYTy~_ñ\x0001OJ¤õÔÍÂëB\x0018µ9]þy¥cþÓSÝ^þè
Ç9=ÍeÇ\x0014qÌ\x0014H	õ<múÕ&PZâ#øÙXâ9\+ò\x001cíàg¦i/oi1¾\x0018ÿ\x0000#Sÿ\x0000fBÌqy\x0002ãçNH·\x0011!:ªÏ,ØÇçïD§\x00145B{¶÷«ç#Þ·¼?s.¥y\x0014"G*>f9à(ëY2èñFÏ{\x0013*­Ú·4Û7Ñ´bð¤òôa	^BûV3¨­¡ÑN×cÒ¾*}ªk](é¢êf/³v\x0017h9útçé^M}¥j\x0011I$MØÆÆÆß¦85©/äÓt«\x0008¯OÚUBË¼ýÀOÝ\x001fJÄ\x0011\Ìª\x0012i\x000cG×éS¬¤\x001aynM¬Ý_jZ-¾u)þÁjCÇ\x000c°2\x0006Xrq^w\x0015ÐÎ\x001a\x0017\x001d7oÁ?t\x0012ø¢\x0007»{g\x001fgFâ²7\x001f­RÐ|Oig¬I#$\x001e[\x0005\x0012Æ\x0018dðN
h£mÆå\x0019%c¿³ºXØ*n9ÈÁ\x0018\x0015ÎÝ[Þ$<ÚÇ \Î½fêM!¢âãìé\x001ckÇó¯+ñ/!»L³\x000bpp\x001c®]½ý\x0007Ój7ØIAjf´2ä~éÉÿ\x0000p×¡ø_á6¡âO:Çí¯"V°.\x0005î"\x0007n{pÜ\x000c\x001cãÞ¼ÚÞãQ¼*a\x0013±ÝÃ¦qÏoJúöjÔ­4Ý7YÑõÍF\x001f.ê16&}0»\x001drO¡\x001f¤Õ§xÞ'Ëcp§h¾½ªÍü7-§$+lÜ\x001dÜrqZþ%Ðîa¾ìLÓ@\x001d¼¶Áä\x0002pGáÎ¹¹
å·\x0012${\x001e}}iÇÞÔ*4®º\x0015£ÓnÙÂµ¼Üÿ\x0000°sS®z$\x0001m§É8\x0019LsRE{rÿ\x0000òÕÉ\x001d>j±-ÝÏRGbW\x0011Vç+\x001a\x0010jä0iW.T­ãsêùÓJ¬²]é×(ÀdnÊÇAÖ.íWÈvD\x0003#'Ozë-µ\x000bß;\x0012zçñXÎ£½Q®p·\x001aì°(Æ\x0018m@ï\x0012|ßæ NÖõÙðÙÞ]3]"b?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - SQL
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - SQL</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js](https://place-des-entreprises.beta.gouv.fr/assets/application-10d6bec9b76415a7a6d4146cf1b23e346c35b90bf44dfa3733f5eb7b2b12ab71.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select blank values from multiselect`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>select blank values from multiselect</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e](https://place-des-entreprises.beta.gouv.fr/e)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/sante-securite-travail](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/sante-securite-travail)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/contactez-nous](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/contactez-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/cession-reprise](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/cession-reprise)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/e/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 12
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/stats" accept-charset="UTF-8" method="get">`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats](https://place-des-entreprises.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/stats" accept-charset="UTF-8" method="get">`
  
  
  
  
Instances: 2
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "commit" "end_date" "start_date" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### CSP: Notices
##### Low (Medium)
  
  
  
  
#### Description
<p>Warnings:</p><p>The report-uri directive has ben deprecated in favor of the new report-to directive</p><p></p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-klGx0kIiWtRZvZ1lqt+v1w=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-klGx0kIiWtRZvZ1lqt+v1w=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-eqX9aGgB2FX8l29aqyeFxA=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-eqX9aGgB2FX8l29aqyeFxA=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-0tre5yEmu4LEVbcSOCk0wA=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-0tre5yEmu4LEVbcSOCk0wA=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self'; base-uri 'self'; font-src 'self' data: https://github.com https://fonts.gstatic.com; img-src 'self' data: https://voxusagers.numerique.gouv.fr https://stats.data.gouv.fr https://www.google.com https://www.google.fr https://googleads.g.doubleclick.net https://www.googletagmanager.com https://www.googleadservices.com https://www.gstatic.com https://adservice.google.com; object-src 'none'; style-src 'self' 'unsafe-inline' https://www.ssa.gov https://fonts.googleapis.com; script-src 'self' blob: https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net https://www.ssa.gov https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-Qm4HVwRoVk/iq56NSC29tw=='; script-src-elem 'self' https://browser.sentry-cdn.com sentry.io https://stats.data.gouv.fr https://cdn.jsdelivr.net www.pagespeed-mod.com https://www.googletagmanager.com https://www.googleadservices.com https://googleads.g.doubleclick.net https://www.google.com 'nonce-Qm4HVwRoVk/iq56NSC29tw=='; frame-src 'self' stats.data.gouv.fr browser.sentry-cdn.com cdn.jsdelivr.net https://bid.g.doubleclick.net; connect-src 'self' *.sentry.io https://api-adresse.data.gouv.fr/ https://www.google.com https://adservice.google.com; report-uri https://o548798.ingest.sentry.io/api/5747178/security/?sentry_key=d975e83e2bee46cd8b3ca7be531a0a6b`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/robots.txt](https://place-des-entreprises.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, s-maxage=31536000, max-age=15552000`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store`
  
  
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FWgx5QJIP4ghWMiXbUhFPltj1K9XKR73XT3yFKHlICooRPfOw4uc6mxkhmw8jYXl1nXpntvHhIqwc1OefvcyCDgLcN4a8sTPObIIiAv6F5jVecBqcqxzT`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `z02wg2qZczzbyRaCVAUL0xn7PjtFi3gbIiGZKY0`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BEqxx7ZtttdeUIZBJyHsrgFQr2YgBIwfv4imv3rYnsv6l2x0ZbksfuTKgHHlG5IixUaJR1mLxio`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `DNl5hZUBug6ZPXrjsFbttI9DL0jCSBLfELBfHlR`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `2B0kV1xT8fTQJxuPqfHdJJ28OpDRCB7`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `2B3eExHNtzpNReVB6uFCHxNnaE2FNpD`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `2F2ZvQwhWKrrkwb95W4kF23eNvRzBVlUXPIMDWL2`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `z0BDkApf1St3GpyTsBkyu1vmAhzdzHmvmIlyCWU2I8ea0ZzYHgRFFtropdfU9QWHV6vtAK6MbiHxVzRsbDFDZLhGk81mfPGeOTZL1quFxkyc9T1YbCJ6tre25I`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `2F9wQxGb5R4rvHetdqVN5yMC4KncyKyR7vqv`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BgRMubxQOz6ayVJoh5fZRAwUpu8z1PU`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `2BQVBWj44VPojG3eyYZsGofTCC57GLYrY3Y3Py`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `2FmEEptXrCeLXWyLMeW4LyfEUptK9Zz8KeHfhjcrCGQRVICl0yrhC36wxyS`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�U�ǔ	 � �c"]�!\x0014�m�R�\�{�t��R�����\x0013�;\x000e.s���\x0019��6\x0017�Yצ{o\x001e\x0012*��Ny��� �-�xk�\x0013<��" /�^cU�\x0001�ʱ�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "<script data-turbolinks-eval="false" nonce="EBu368zueqZBqKdKaQoo0w=="></p><p>//<![CDATA[</p><p>  var _paq = _paq || [];</p><p>  // Configure Matom", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/internet-web)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/environnement-transition-ecologique)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/droit-du-travail)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id="open-cookies-box" aria-label="Ouvre la fenêtre de gestion des cookies" href="#">Gestion des cookies</a>`
  
  
  
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/entreprise-en-difficulte)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/financement-projets)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/e/](https://place-des-entreprises.beta.gouv.fr/e/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/sitemap.xml](https://place-des-entreprises.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/robots.txt](https://place-des-entreprises.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `s-maxage=31536000`
  
  
  
  
Instances: 1
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `415474841`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/recrutement-formation)
  
  
  * Method: `GET`
  
  
  * Evidence: `415474841`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `415474841`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/relance)
  
  
  * Method: `GET`
  
  
  * Evidence: `415474841`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/comment_ca_marche](https://place-des-entreprises.beta.gouv.fr/comment_ca_marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr](https://place-des-entreprises.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `415474841`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/](https://place-des-entreprises.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210329`
  
  
  
  
Instances: 10
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>415474841, which evaluates to: 1983-03-02 17:40:41</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126)
  
  
  * Method: `GET`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126)
  
  
  * Method: `GET`
  
  
  * Parameter: `start_date`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `user[email]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126)
  
  
  * Method: `GET`
  
  
  * Parameter: `territory`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[full_name]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[phone_number]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126)
  
  
  * Method: `GET`
  
  
  * Parameter: `end_date`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_options_slugs][]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[landing_slug]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `solicitation[email]`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126](https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126)
  
  
  * Method: `GET`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in](https://place-des-entreprises.beta.gouv.fr/mon_compte/sign_in)
  
  
  * Method: `POST`
  
  
  * Parameter: `commit`
  
  
  
  
* URL: [https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial](https://place-des-entreprises.beta.gouv.fr/aide-entreprises/developpement-commercial)
  
  
  * Method: `POST`
  
  
  * Parameter: `commentaire`
  
  
  
  
Instances: 16
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://place-des-entreprises.beta.gouv.fr/stats?commit=Chercher&end_date=2021-07-18&start_date=2021-01-01&territory=126</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [data-disable-with] attribute </p><p></p><p>The user input found was:</p><p>commit=Chercher</p><p></p><p>The user-controlled value was:</p><p>chercher</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3

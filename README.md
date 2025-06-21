#### protect-wordpress  For Paranoid bloggers on wordpress.
Protect wordpress with .htaccess
* AI ROBOTS/SCRAPERS:  https://github.com/tinaponting/ai-robots-scrapers

* No one of these htaccess 1 or 2 makes any diffrent in speed! *
For us who are paranoid bloggers or use it as CMS, we want to sleep with peace! use these .htacces and adwises and you will be safe! 

* If you want something on the maybe text; downloads add it with, noteplus + or what you use:)
* works best with Apache, 5.0 + Wordpress, 6,7+

* You can use both htaccess and Perrish Press firewall at the same time with no impact on speed! Name PR to htaccess2 and it is ready to protect.
WORDPRESS - FORT KNOX:)


Wp.config.php file:  //Se also my core - single user or wp addon on here:)

require_once(ABSPATH.'wp-settings.php');  
Add this after this:
* define('WP_DEBUG',false);

define('DISALLOW_FILE_EDIT',true); 
define('DISALLOW_FILE_MODS',true);
define('DISABLE_WP_CRON',true);
ob_start();?>

Set to: 444 in wp.config.php Also gets some speed!  //important!!

* Protect: wp.contents folder, plugins,themes and uploads.
* Protect: wp-admin folder.

Core .htaccess for protection and speed.  Set: 444 files rights or of it possible: 440

* Example 220906 : Robots.txt - even if the wp sets up robots.txt, it is not enough! To cover all boots and if you hate: semrush, ahrefs, add more id you don not want!

* (220922) BBQ Custom code: Protects your blog:) If bought BBQ!
* If you got trouble or don´t like folks looking inside your plugins root, this works, set the htaccess in plugins Example: Wpschema root, set 444 .-done!

**** IF You use. perrrishpress 8G Firewall, name it: .htacces2 if use it with my other .htacess in root.

Plugins I recommend:
* disable wp rest-api:  // So they cannot se who is the user: https://wordpress.org/plugins/disable-wp-rest-api/

None above takes power fron your blog:)

PAYED Firewall: 
* BBQ Pro   // I love the custom - place in protection for strange files!   https://plugin-planet.com/bbq-pro/

* BLOCK BAD BOTS  - Blackhole Pro   Works very well:) same adress as above:)

* 404 controls: - so GOOD /Payed version best:): https://www.cminds.com/wordpress-plugins-library/404-console-plugin-wordpress/

*  Login IP  country restriction:  login-ip-country-restriction Payed:https://iuliacazan.ro/login-ip-country-restriction/
Free version: https://wordpress.org/plugins/login-ip-country-restriction/  * Both versions Works very well:) 

* Protect of your JS files: https://domainlockjs.com/     works very well:)  // If your under attack, otherwise not needed!

* Simple Login Captcha:  https://wordpress.org/plugins/simple-login-captcha/    Really godd against Autobots, does not take poer from your blog.

* None above takes power from your blog!

If you got google / bing XML files, set them t0 444 0r if it works: 440:) for safety
Set you robots.txt to 444. Do not use: humans.txt, it mostly slow down your blog, ads.txt? Set to 444 or 440.
Blogs I Love:
* Perishable Press: https://perishablepress.com/   Always something new to read about security.
* Wphacked blog:  https://secure.wphackedhelp.com/blog/

* Strong password generator: https://www.f-secure.com/en/home/free-tools/password-generator   // Choose Password length: 32 and after that use some greek, some russian, some norwegian,swedich,Deuch words here and there = Very hard to break!
Happy safe blogging folks:)

* Block IP by country:  https://www.ip2location.com/free/visitor-blocker   //very good if you got to mutch of for example: Hongkong!

* Sitemap Validater: https://www.xml-sitemaps.com/validate-xml-sitemap.html

*  Information about IP adresses:  https://threatbook.io
*  OR https://www.abuseipdb.com/   Abuse IP

* Remove not used files:
readme.html
license.txt
changelog.txt
All files .md

Do you need?: wlwmanifest.xml /  /wp-includes

+ wp-config-sample.php

Wp-admin:
/wp-admin/install.php

*****VERY IMPORTANT
*' To protect: wp-includes/js and css from curious! eyes and hackers, take wp-content: index.php and put it there!

**# If you want to annoy scrapers, ai scrapers and other annoying. Use both or one of these:

https://wordpress.org/plugins/wp-browser-update/
http://browserupdate.org/

https://wordpress.org/plugins/real-cookie-banner/

AI SCRAPERS HERE: https://github.com/tinaponting/ai-robots-scrapers

* * IF YOU WANT to change something: use: Notepad ++ -to your taste:)


Love ///  Kristina Sweden  :  

***UPDATED FILES AND FOLDERS: *******

* Updated: 250621  htaccess1 updated:)
* Updated: 250621 perishablepress.com8g-firewall with Latest Aibots - NO Thanks:)
* Updated: 250611  htaccess1 updated:)
* Updated: 250610  perishablepress.com8g-firewall with Latest Aibots - not wanted:)
* Updates: 250607 - AI Alternative to use - If stubborn:)
* Updated: 250606  perishablepress.com8g-firewall with MORE AI -no wanted:)
* Updated: 250605 htaccess1 - More Speed and security)
* Updated: 250605  perishablepress.com8g-firewall with Latest Aibots - not wanted:)
* Updated: 250527 wp-includes - wp-admin, ERROR  on my I  use..
* Updated: 250531 perishablepress.com8g-firewall with Latest Aibots - not wanted:)
* Updated: 25027 wp-content, more speed.
* Updated: 25027 wp-includes ? wp-admin, more securtity.
* Updated: 25025 htaccess1 - More Speed and security)
* Updated: 250525 perishablepress.com8g-firewall with Latest Aibots - not wanted:)
* Updated: 25018 wp-includes, more alternatives to use.
* Updated: 25016 htaccess1 - More Speed and security)

* Updated: 250101 - 250431 
* Updated: 240102 - 2411225 
* Updated: 230306 - 231220
* Updated: 230206 - 230505. 
* Updated: 230202 - 230101.
* Updated: 221225 - 221230.
* Updated: 221225 - 221124.
* Updated: 220915 - 221124.
* Updated: 2020 - 2021.

VERY IMPORTANT: Core  .htaccess + .htaccess1 for speed and protection  Set: 444 files rights
in core. No one can write to any files!!

...............................................................
På Svenska:

Protect Wordpress och andra bloggar med php.
med htaccess 1 + htaccess2 - om möjligt BBQ Pro - 
[plugin-planet.com/bbq-pro](https://plugin-planet.com/bbq-pro/)/ 
som är ett utmärkt plugin och firewall. Inget påverkar fart och cache. Utan fungerar som firewalls:)

...............................................................
In Enlish:
Protect Wordpress and other blogs with php.
with htaccess 1 + htaccess2 - if possible BBQ Pro - 
[plugin-planet.com/bbq-pro](https://plugin-planet.com/bbq-pro/) / which is an excellent plugin and firewall. Nothing affects speed and cache. But works like firewalls:)

...............................................................
En español:

Protege WordPress y otros blogs con PHP.
Con htaccess 1 + htaccess 2. Si es posible, BBQ Pro 
[plugin-planet.com/bbq-pro](https://plugin-planet.com/bbq-pro/) /, que es un excelente plugin y cortafuegos. No afecta la velocidad ni la caché. Pero funciona como un cortafuegos.

...............................................................
Auf Deutsch:
Schützen Sie WordPress und andere Blogs mit PHP.
Mit htaccess 1 + htaccess 2 – wenn möglich BBQ Pro – 
[plugin-planet.com/bbq-pro](https://plugin-planet.com/bbq-pro/) /. Das ist ein hervorragendes Plugin und eine Firewall. Es beeinträchtigt weder Geschwindigkeit noch Cache. Funktioniert aber wie Firewalls. :)

:::::::::::::::::::::::::::::::::::::::::::::::::::::::::

#### protect-wordpress  For Paranoid bloggers on wordpress.
Protect wordpress with .htaccess
* AI ROBOTS/SCRAPERS:  https://github.com/tinaponting/ai-robots-scrapers

* No one of these htaccess 1 or 2 makes any diffrent in speed! *
For us who are paranoid bloggers or use it as CMS, we want to sleep with peace! use these .htacces and adwises and you will be safe! 

About me: A blogger since 2002, been on blogspot as on wordpress, made all mistakes through the years, I learned not only a free firewall can protect med, so I made my own, follow the latest trends in hacking and some blogs on to get it in order:)  
I gone throught everything  i could find in google, gibhub and forums for all .htacces security, some things didn´t work, some did works! Some old htacces tricks that still works.  Use it free but come back time to time to check latest updates.  Love //KP Karlshamn sweden

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

*****VERY IMPORTANT:
Very important; If you got an older blog!
On:
WP-CONFIG.PHP
define('DB_CHARSET','utf8mb4');  //works well in sweden, somehoq:)

******Change it to: 
define('DB_CHARSET','utf8');

*' To protect: wp-includes/js and css from curious! eyes and hackers, take wp-content: index.php and put it there!

**# If you want to annoy scrapers, ai scrapers and other annoying.
Use both or one of these:

https://wordpress.org/plugins/wp-browser-update/
http://browserupdate.org/

https://wordpress.org/plugins/real-cookie-banner/

AI SCRAPERS HERE: https://github.com/tinaponting/ai-robots-scrapers

* * IF YOU WANT to change something: use: Notepad ++ -to your taste:)


Love ///  Kristina Sweden  :  

***UPDATED FILES AND FOLDERS: *******

* Updated: 250401 perishablepress.com8g-firewall + my htaccess2 +  gone Througt all Updated:)
* Added: 250401 - LIST OF common browseers used/hackers, Tzt stealers.txt
* Updated: 250329 perishablepress.com8g-firewall + my htaccess2 +  gone Througt all Ai- uppdated!
* Updated: 250329 perishablepress.com8g-firewall + my htaccess2 +  Delated GE
* Updated: 250323 perishablepress.com8g-firewall + my htaccess2 +  new  AI
* Updated: 250319 htaccess  - updated
* Updated: 25019 htaccess1 -updated =  security:: Delated, wp.user/json - do not work:(
* Updated: 250313 perishablepress.com8g-firewall + my htaccess2+  A new AI
* Updated: 250309 perishablepress.com8g-firewall + my htaccess2+  A new AI
* Updated: 250308 perishablepress.com8g-firewall + my htaccess2+  A new AI
* Updated: 250307 perishablepress.com8g-firewall + my htaccess2+ new AI
* Updated: 250306 perishablepress.com8g-firewall + my htaccess2+ new AI
* Updated: 250304 htaccess1 -updated = More security:) 
* Updated: 250225 perishablepress.com8g-firewall Latest Ai someAdjustment in firewall:)
* Updated: 250218 perishablepress.com8g-firewall Updated:)
* Updated: 250218 htaccess1 -works well, checked with lynx:) 
* Updated: 250213 Updated, wp-includes folder protection.
* Updated: 250210 perishablepress.com8g-firewall Updated my own with Ai.
* Updated: 250207 htaccess1 -all:) delated some doubles:)
* Updated: 250206 perishablepress.com8g-firewall Updated, with Old browsers not wanted:)
* Updated: 250128 perishablepress.com8g-firewall Updated, used by me + Ai block, all updated with new 8G firewall.
* Updated: 250127 htaccess -with more alternatives for speed.
* Updated: 250124 perishablepress.com8g-firewall Updated, used by me + Ai block
* Updated: 250119 htaccess1 -all:) 
* Updated: 250123 perishablepress.com8g-firewall + new Ai not wanted!
* Updated: 250119 htaccess1 - my own, i use!
* Updated: 250115 perishablepress.com8g-firewall + new Ai not wanted!
* Updated: 250117 maybe.txt
* Updated: 250114 Updated wp-admin
* Updated: 250113 htaccess1
* Updated: 250113 perishablepress.com8g-firewall + new Ai not wanted!
* Updated: 25009 updated: htaccess1 - one error!:(
* Updated: Noway allowed-Do not see
* Updated: 25006 updated: w-includes, but still have smeissues with admin, working on  it:)  But works.
* Updated: 25006 updated: htaccess1, delated som code not needed year 25:)
* Updated: 250101 qp-includes protect to the new folders and so on  
* Updated: 240102 - 2411225 
* Updated: 230306 - 231220
* Updated: 230206 - 230505. 
* Updated: 230202 - 230101.
* Updated: 221225 - 221230.
* Updated: 221225 - 221124.
* Updated: 220915 - 221124.
* Updated: 200220 - 2021.

VERY IMPORTANT: Core  .htaccess + .htaccess1 for speed and protection  Set: 444 files rights
in core. No one can write to any files!!

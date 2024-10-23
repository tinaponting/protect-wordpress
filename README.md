#### protect-wordpress  For Paranoid bloggers on wordpress.
Protect wordpress with .htaccess
* AI ROBOTS/SCRAPERS:  https://github.com/tinaponting/ai-robots-scrapers

For us who are paranoid bloggers or use it as CMS, we want to sleep with peace! use these .htacces and adwises and you will be safe! 

About me: A blogger since 2002, been on blogspot as on wordpress, made all mistakes through the years, I learned not only a free firewall can protect med, so I made my own, follow the latest trends in hacking and some blogs on to get it in order:)  
I gone throught everything  i could find in google, gibhub and forums for all .htacces security, some things didn´t work, some did works! Some old htacces tricks that still works.  Use it free but come back time to time to check latest updates.  Love //KP Karlshamn sweden

* If you want something on the maybe text; downloads add it with, noteplus + or what you use:)
* works best with Apache, 5.0 + Wordpress, 6,1, 6.6+

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


Love ///  Kristina Sweden

***UPDATED FILES AND FOLDERS: ***

* Updated: 241022,  Perishablepress.com8g-firewall - my own that I use.
* Updated: 241022, Updated: htaccess1 for better security, delated som not used studd, added some.
* Updated: 241014, Ai bots/ai scrapers on own ai folder updated:)
* Updated: 241007, Ai bots/ai scrapers moved to own ai:)
* Updated: 241006, updated: ai texts new AI scrapers:(
* Updated: 2410910, updated, block ai.php scripts, do no intefere with speed, and ai acrapers.tt to the Latest:)
* Updated: 241001,Noway allowed-Do not see. updated.
* Updated: 240929, updated robots.txt, user agents,checked all dissalow for not in use, long gone robots, set latest useragents, download it on singe user:)
- Updated: 240929, Updated ai scrapers, txt, new ai:(
- Updated: 240927, Updated Perrishpress 8G . my own, with protection for ai bots,scrapers, working on more chrome/firefox scrapers.
- Updated: 240927, updated htaccess1 for btter protectin, ai moved to: htaccess2. with block for scrapers.
- Updated: 240924, only allwed useragents list. htaccess, good in folder you do not want noosy useragents.
- Updated: 240922, BLock ai.php Updated new ai scraper.
- Updated: 240922, Aiscrapers txt, new ai scraper bot:(
- Updated: 240921: BLOCK ai.php, new ai bot!
- Updated: 240917: BLOCK ai php.zip  with the Latest ai bots, not wanted.
- Updated:240911: htaccess 1 - I use:)
- Updated:240911: perishablepress.com8g-firewall  -I use:)
- Updated: 240909, forget one file in BLock ai....
- Updated: 240909, block ai.php with latests ai blocks, works great, not intefering with blogs, an extra layer of protection:)
- Updated: 240908 ai bots/scrapers list.
- Updated: 240901: aiscrapera, common and maybe updated:)
- Updated: 240830: perishablepress.com8g-firewall /htaccess2 - I USE, firewall.
- Updated: 240830: htaccess1 my own htaccess with block ai.
- Updated: 24083- Updated,240830:th Ai/hacking - no thanx updated, my own htaccess1. 
- Updated: 240827: perishablepress.com8g-firewall /htaccess2 firewall.
- Updated: 240822 Not Allowed, so it works better:)
- Updated: 240820 wp-content/uploads with working stop stealing my images from: [AwarioRssBot](https://perishablepress.com/)
- Added: common hackers tools, use all or take what you need:)
- Updated: 240809:  Mu htaccess1 with ai. 
- Updated: 240807: Updaed Perrishpress 8G extended version.
- Updated:240804: htaccess1, small errors on my htaccess1.
- Added: 240803, small php script, exit ai, as extra layer on blogs. Not sure it works. 
- Updated: 240802: ALT- if you only want some user agents to visit, ready to clip in.
- Updated:240802:  htaccess1, better performance, delated some not in use useragents.
- Updated: 240729 wp-content security.
- Updated: 240729, htaccess1, for better performance.
- Updated: 240725 Noway allowed-Do not see  files, works better:)
- Updated: 240717, htacess1 for better security
- Updated: 240705, htaccess1 - my own, a error in block, china/singapore hell:)
- ROBOTS.txt moved to: Single user.
- Updated:htaccess1 for better security.
- Updated: Noway allowed-Do not see with hellodolly plugin, need for it work good! and How to change tou your favorite song:)
- Updated: htaccess1 more secure site:)
- Updaeted: htaccess1, more secure:)
- Updated: 240519, htaccess1 with the Latest, Ai, not here thanks!
- Updated: 240517: No way - do not see, with hide all.
- Updated: 240517, htaccess1- I use, withoout Ai, better security.
- Updated: 240506, htaccess1 for better firewall:)
- Updated: 240505, robots.txt, htacces with deflate, wepg.
- Updated: 240429, updatet htaccess1, my own, when I hate these HK/China hackers.
- Updated: 240428, htaccess1 for better perfomance and a error!
- Uddated: 240426, beter choises for wp-includes
- Updated: 240425, htacces1, for better performance:)
- Updated: 240423, Robots.txt extendes version, with some new ai - no thanks:(
- Updated: 240416, do no see folder for better performance.
- Updated: 240416, wp-includes to works for wp:6,5
- Updated: 240416, htacces1  for errors, checked and good working:)
- Updated: 240410 htaccess1 for better protection:)
- Updated: 240321 maybe text:)
- Updated: 240312, wp-includes for better protection.
- Updated: 24010 htaccess, better deflate and filesmatch:) - FASTER!
- Updated: 240308: htaccess1 updated -Checked for errors! Works no impact on speed!
- Updated: 240304: htaccess1.
- Updated: 240304, wp-includes
- Updated: 240303, wp-content
- Updated: 240229fuckdevtools:)
- Updated: 240225 htaccess1 udated:)
- Updated: 240223, htaccess1 updated:)
- Updated: 240201, htaccess1 with 2024 Security headers:)
- Updated: 240201, perssishpress firewall updated:)
- Updated: 240127, htaccess1 by accident, I blocked, google.....:(
- Updated: 240125, htaccess1 for better protection:)
- Updated: 240125, updated, wp-includes for more power and security.
- Updated: 240124 htaccess1.
- Updated: 230116 htaccess, errors....Checked:)
- Updated: 230115 htaccess1, for better Security.
- Updated: 2410110: w-admin for more security:)
- Updated: 2400102, my strongest; htaccess1.
* Updated: 230306 - 231220
* Updated: 230206 - 230505. 
* Updated: 230202 - 230101.
* Updated: 221225 - 221230.
* Updated: 221225 - 221124.
* Updated: 220915 - 221124.
*  Updated: 200220 - 2021.

VERY IMPORTANT: Core  .htaccess + .htaccess1 for speed and protection  Set: 444 files rights
in core. No one can write to any files!!

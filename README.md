# protect-wordpress  For Paranoid bloggers on wordpress.
Protect wordpress with .htaccess

For us who are paranoid bloggers or use it as CMS, we want to sleep with peace! use these .htacces and adwises and you will be safe! 

About me: A blogger since 2002, been on blogspot as on wordpress, made all mistakes through the years, I learned not only a free firewall can protect med, so I made my own, follow the latest trends in hacking and some blogs on to get it in order:)  
I gone throught everything  i could find in google, gibhub and forums for all .htacces security, some things didn´t work, some did works! Some old htacces tricks that still works.  Use it free but come back time to time to check latest updates.  Love //KP Karlshamn sweden

* If you want something on the maybe text; downloads add it with, noteplus + or what you use:)
* works best with Apache, 5.0 + Wordpress, 6,1, 6.2+

WORDPRESS - FORT KNOX:)


Wp.config.php file:  //Se also my core - single user or wp addon on here:)

require_once(ABSPATH.'wp-settings.php');  Add this after this:
error_reporting(0); 
ini_set('display_errors','0'); 
ini_set('error_reporting',E_ALL);
define('DISALLOW_FILE_EDIT',true); 
define('DISALLOW_FILE_MODS',true); 
ob_start();?>

Set to: 444 in wp.config.php Also gets some speed!  //important!!

* Protect: wp.contents folder, plugins,themes and uploads.
* Protect: wp-admin folder.

Core .htaccess for protection and speed.  Set: 444 files rights

* Exemple 220906 : Robots.txt - even if the wp sets up robots.txt, it is not enough! To cover all boots and if you hete:semrush, ahrefs, add more id you want

* (220922) BBQ Custom code: Protects your blog:) If bought BBQ!
* If you got trouble or don´t like folks looking inside your plugins root, this works, set the htaccess in plugins Example: Wpschema root, set 444 .-done!

UPDATED FILES AND FOLDERS:

- Added 230717 better moemorry leak deny, better error deny:)
- Added 230706 an alternative htacce core for more speed.
- Updated 230706 htacces1 for better performance
- Updated: Not allowed folder:)
- Updated: wp.includes so it works with wp-6.2.2 and keep protection for under 6.1. 
- Updated: 230616 persishpress G8 for more speed. Delated and double om htaccess1. 
- Added protection for empty refers, htaccess1.
- Updated 230611  .htaccess1 smallchanges for better security!
- Added: 230605 with Memory/without in core .htaccess.
- Updated: 230605, htaccess1 - removed proxy, added it on maybe if wanted!
- Updated:230607 IPlist and mabe tzt.
- My most powerful htaccess1 yet! tested and works well, also added a blank htacces for you who wants your own! Happy wordpress blogging!
- Added 8G 230601 [perrush](https://perishablepress.com/)  optimized for speed, tested on my blogs!
- Added 8G 230530 [perrush](https://perishablepress.com/)  Firewall without logging. Works well, tested on my blogs!
- Updated: 2305v31 wp-content to latest protecrion.
- Updated: 230531 htaccess1 for better protection and speed with the latest threats!
_ Updated: 230630 htaccess for better speed:)
- Updated: 230530 htacces for laatest protection
- Updated: 230529 htaccess1.
- Updated: wp-includes, core  folder, some small errors and tested with, 6,2, works well.
- Added, protection, for wp 6.2 includes folder html.api.
- Added: 230510, wp-includes, an extra htacces, that I use, more layers of protection.
- Added: 230508 alternative plugin protection
- Added: 230508 wp-admin, no index!
- Added: 230507 wp-includes, protection, extra with 3v layers of protection, I use it on all my blogs:)
- Added: 230503 at better index.php/index.html for content/uploads/plugins/themes folder.
- Updated: 200429, wp-includes folder, core files, soms js/css was not protected!
- Updated: 230429, wp-content -core folder, minor error.
- Updated: 230427 wp-content, checked all files for errors, works fine!
- Updated: 230426 wp-content protection with altiernative and better security.
- updated: 230425 htaccess1- A small error.
- Updated: 230425, wp-includes core folder with a small changes.
- Updated: 230423 .htaccess1 for more security.
- Updated: 230421: Folder, wp-includes, core folder and alternatives:)
- Updated:230415 .htaccess1 with better speed and some moore security, the only thing missing is feed stealers!
- Uppdated: 230401 .htaccess 1 updated with protection, wget/curl/postman download site.
- Updated: BBQ PRO customs codes with protection.
- Updated:230324 htacces1 updated:) Works great!
- Updated: 230316 htaccess1 - Some old stuff gone, new theats added!, works great, nothing to see on google webmasters tools!
- Updated: 230316 htaccess1 - Some old delated som new on.
- Updated: 230314: htaccess1 - At last, viewing css,js,php and so on = GONE!
- Updated: 230313; BBQ Custom codes updated!
- Updated: 230313: wp-admin, with alternatives:)
- Updated: 230308: htaccess1, minor errors gone!
- Updated: 230308: wp-content, minor errors gone!
- Updated: 230307: wp-includes minot errors gone!
- Updated: 230307: wp-admin, htaccess.
- Updated: 230306: .htaccess1, minor errors gone!
- Updated: 230306: wp-includes, minor errors gone!
- Updated: 230306:.htaccess1, minor errors gone!
- Updated: 230305 .htaccess1, minor errors gone!
- Updated: 230304: wp-includes updated! better security!
- Working: 230303 on better security on wp-includes:)
- Updated: 230302 .htaccess1 small errrors! fixed
- Updated: 230227, htaccess1 - A small error! fixed
- No changes in 230227 .htacces -wp-admin, works very well on all my blogs!
- Updated: 230227, wp-includes, more alternatives to use.
- Updated: 230227, updated .htaccess1 small fixes!
- Updated: 230222 wp-content .htaccess updated! all tried and working!
- Updated: 230219 htacces1 for better protection, gone through all and madesome small changes:)
- Updated: 230216 htaccess1 - double thing:(
- Updated: 2302015 htaccess for better speed.
- Updated: 230207 .htaccess, for better performance:)
- Updated: 2302006 .htaccess1 for better performance and protection for ALL .htaccess files:)
- Updated: 230202   - 230101
- Updated: 221225  - 221230: Delated:)
- Updated: 221225 -  221124:  Delated:)
- Updated: 2200915 -221124: Delated:)
- Updated: 2021: Delated:)

VERY IMPORTANT: Core  .htaccess + .htaccess1 for speed and protection  Set: 444 files rights
in core. No one can write to any files!!


Plugins I recommend:
* limit login attempts reloaded:   See: https://wordpress.org/plugins/limit-login-attempts-reloaded/
* disable wp rest-api:  // So they cannot se who is the user: https://wordpress.org/plugins/disable-wp-rest-api/
* wp-cron http auth: // Small very good protectin for  rest api:   https://wordpress.org/plugins/wp-cron-http-auth/

None above takes power fron your blog:)

PAYED Firewall: 
* BBQ Pro   // I love the custom - place in protection for strange files!   https://plugin-planet.com/bbq-pro/

* BLOCK BAD BOTS  - Blackhole Pro   Works very well:) same adress as above:)

* 404 controls: - so GOOD /Payed version best:): https://www.cminds.com/wordpress-plugins-library/404-console-plugin-wordpress/

*  Login IP  country restriction:  login-ip-country-restriction Payed:https://iuliacazan.ro/login-ip-country-restriction/
Free version: https://wordpress.org/plugins/login-ip-country-restriction/  * Both versions Works very well:) 

* Protect of your JS files: https://domainlockjs.com/     works very well:)  // If your under attack, otherwise not needed!

* Simple Login Captcha:  https://wordpress.org/plugins/simple-login-captcha/    Really godd against Autobots, does not take poer from your blog.

* WP CSRF Protector: (mostly in forms, if you use that is Mostly on Multisite then it is in good use!, this works fine!) https://github.com/mebjas/WP-CSRF-Protector

* None above takes power from your blog!

If you got google / bing XML files, set them t0 444 0r if it works: 440:) for safety
Set you robots.txt to 444. Do not use: humans.txt, it mostly slow down your blog, ads.txt? Set to 444 or 440.
Bloga I Love:
* Perishable Press: https://perishablepress.com/   Always something new to read about security.
* Wphacked blog:  https://secure.wphackedhelp.com/blog/

* Strong password generator: https://www.f-secure.com/en/home/free-tools/password-generator   // Choose Password length: 32 and after that use some greek, some russian, some norwegian,swedich,Deuch words here and there = Very hard to break!
Happy safe blogging folks:)

* Sitemap Validater: https://www.xml-sitemaps.com/validate-xml-sitemap.html

* Remove unneeded files:
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
define('DB_CHARSET','utf8mb4');

******Change it to: 
define('DB_CHARSET','utf8');

*' To protect: wp-includes/js and css from curious! eyes and hackers, take wp-content: index.php and put it there!

Love Kristina Sweden

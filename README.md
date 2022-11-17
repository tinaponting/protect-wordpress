# protect-wordpress  For Paranoid bloggers on wordpress.
Protect wordpress with .htacess

For us who are paranoid bloggers or use it as CMS, we want to sleep with peace! use these .htacces and adwises and you will be safe! 

About me: A blogger since 2002, been on blogspot as on wordpress, made all mistakes through the years, I learned not only a free firewall can protect med, so I made my own, follow the latest trends in hacking and some blogs on to get it in order:)  
I gone throught everything  i could find in google, gibhub and forums for all .htacces security, some things didn´t work, some did works! Some old htacces tricks that still works.  Use it free but come back time to time to check latest updates.  Love //KP Karlshamn sweden

* If you want something on the maybe text; downloads add it with, noteplus + or what you use:)


Wp.config.php file:  //Se also my core - single user or wpaddon on here:)

require_once(ABSPATH.'wp-settings.php');  Add this after this:
error_reporting(0);
ini_set('display_errors','Off');
ini_set('error_reporting',E_ALL);
define('DISALLOW_FILE_EDIT',true);
define('DISALLOW_FILE_MODS',true);
ob_start();
?>

Set to: 444 in wp.config.php Also gets some speed!  //important!!

* Protect: wp.contents folder, plugins,themes and uploads.
* Protect: wp-admin folder.

Core .htaccess for protection and speed.  Set: 444 files rights

* Exemple 220906 : Robots.txt - even if the wp sets up robots.txt, it is not enough! To cover all boots and if you hete:semrush, ahrefs, add more id you want

* (220922) BBQ Custom code: Protects your blog:) If bought BBQ!
* If you got trouble or don´t like folks looking inside your plugins root, this works, set the htaccess in plugins Example: Wpschema root, set 444 .-done!

Updated files:

- Updated:221117 for better security .htaccess1.
- Updated: 221115 Themes folder with morealternatives.
- Updated: wpincludes files for better performance.
- Updated: wp-includes, js folder ALTERNATIVE, if uo got a theme that is sensitive to js.
- Updated: 221111: wp-content for better security for themes and plugins:)
- Updated: 221110 wpincludes core htacces and tried every folder - If I get in:) Every file:) WORKS!!
- Updated 221109 Wp-includes files with new: style-engine and better protection for files, php/js/css.
- Updated htacces1 with protection, wp-cron/wp-links-opml/wp-json
- Updated 221107:Wp- includesm,more js alternatives:)
- Updated 221106: wp-contet for better plugins and themes security:)
- Updated 221106: wp-includes folder, to protect js/css files, all php in all subfolders.
- Updated 221105: wp-content folder  + htacces1 + Maybe txt.
- Updated 221104: wpincludes, protection for js.
- Updated 221104: wpcontent with protection for themes:)
- Wpincludes 221102 folder:  2 alternatives to  protect js folder, sometimes the alt.1 doesn´t work if you got js based theme.
- Updated 221101 wpincludes, if needed folders:)
- Updated 221101 maybe txt, more if needed:)
- Updated - .htaccess for more speed.
- Added protection for thos ewho had: Wellknown folder, if needed!
- Updated: 221029 updated wpcontent for more security!
- Updated: 221028 .htaccess1 updated for more security and some wrongs! Works perfect on my blogs =Tested!
- Updated: 221025 htaccess +.htacces1 for more speed and protection:)
- Updated: 221024, .htacces1 for more speed and security:)
- Updating: 221020 BBQ custom codes.
- Updated: 221019 wp-includes, works! = Ready to work for you!
- Updated: 221017 wp-content folder! = Ready to work for you!
- Updated: 221017 -htaccess1 = Ready to work for you! On your blog, look in now and then for updates!
- Updated: wpconten/uploads folder for better speed and security.
- Updated: wpcontent folder for more speed and security:)
- Updated: 221014: .htaccess1 for more speed and some files not needed (doubles)
- Updated: 221013: wp-content .htacces so it protect themes js files:)
- Updated: 2201008: .htacces1 for betrer spam preotect wp.login/register:)
- Updated: 2201007: wpcontent uploads folder, no you can only download if you are admin/photo, prevents stealers!
- Updated: 221004: All folders/htacces files checked -checked Lynx checker:)
- Updated: 221004: wpincludes/js for better security!
- Updated: 221004 wpcontent/themes for better security!
- Updated: 221002 wp-content uploads and wp-content for more security!
- Updated: wp-includesfolder, .htaccess for more security.
- Updated: 2209928, .htaccess1 - gone google walk for latest threats and made a very good cheking of .htaccess1 checked with lynx htacces checker!
- Updated: 220927 Wpcontent folder with protection for themes and plugins! 
- Updated: 220927 .htaccess1 for better security and som wrongs!And changed name to firewall.
- Updated: 220926 Found a thing to mutch, checked the .htaccess (http://www.htaccesscheck.com)
- Updated: 220925 Some not needed in .htaccess1:)
- Updated: 220924: added protection for, wp.load.php file and some more goodies for protection.
- Updated: 220922: wp includes all is included.
- Updated: 220922: .htaccess1 for better security.
- Updated:220922: wpcontent folder, htaccess with protection, no insert of infected images!
- Updated:220917 Added Css/Js folder protection - that works! 
- Updated 2200915: .htacces1 for more: No fake bots, only allow real google botsand som on!
- Updated wp-content folder:)
- Updated: .htaccess1 for more protection, did I cover all? 
- Updated: .htacess for more security and newest protection, added, block for semruch/ahrefs, who the most bloggers do not need!
If needed, add more evil bots - just copy one line and ad it!

- Uppdated: 220914: Js folder / wp-includes that protect js files! Works well!
- Uppdated: 220906: htaccess1 - false boots protection and extra protection, admin, manifest files:)
- Updated: 220828 : htaccess1 for more security and some dublicates gone:) 
- Updated: 220731:  Protection for images, uploads folder, stealers and no way you see what I got!
- Updated: 220730: .htacess for more speed and for mobile!
- Updated: 220722: .htacces1for protection of: Js, Css files:)
- Updated: 220719: .htacces1 for more security and doubles.
- Added Protection, wp.-includes/fonts follder (They download font til´you die!:(
- Updated: Wp.content folder. 
- Updated: 220715: protect plugin folder.
- Updated: 220715 wp.content folder
- Updated: 220709  Works! And added som protection for theme:)
- Updated: 220702 
- Updated: 220625


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

If oy got googleI bing XML files, set them t0 444 0r if it works: 440:) for safety
Set you robots.txt to 444. Do not use: humans.txt, it mostly slow down your blog, ads.txt? Set to 444 or 440.
Bloga I Love:
* Perishable Press: https://perishablepress.com/   Always something new to read about security.
* Wphacked blog:  https://secure.wphackedhelp.com/blog/

* Strong password generator: https://www.f-secure.com/en/home/free-tools/password-generator   // Choose Password length: 32 and after that use some greek, some russian, some norwegian,swedich,Deuch words here and there = Very hard to break!
Happy safe blogging folks:)


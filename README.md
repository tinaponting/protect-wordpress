# protect-wordpress
Protect wordpress with .htacess


Wp.config.php file:  //Se also my core - single user:)
require_once(ABSPATH.'wp-settings.php');
error_reporting(0);
ini_set('display_errors','Off');
ini_set('error_reporting',E_ALL);
define('DISALLOW_FILE_EDIT',true);
define('DISALLOW_FILE_MODS',true);
ob_start();
?>

Set to: 444 in wp.config.php Also gets some speed!  //imporrtant!!

* Protect: wp.contents folder, plugins,themes and uploads.
* Protect: wp-admin folder.

Core .htaccess for protection and speed.  Set: 444 files rights

* Exemple 220906 : Robots.txt - even if the wp sets up robots.txt, it is not enough! To cover all boots and if you hete:semrush, ahrefs, add more id you want


- Updated wp-content folder:)
- Updated .htaccess1 for more protection, did I cover all? 
- Updated: both .htacess for more security and newest protection, added, block for semruch/ahrefs, who the most bloggers do not need!
If needed, add more evil bots - just copy one line and ad it!

- Uppdated 220906: htaccess1 - false boots protection and extra protection, admin, manifest files:)
- Updated 220828 : htaccess1 for more security and some dublicates gone:) 
- Updated 220731 Protection for images, uploads folder, stealers and no way you see what I got!
- Updated: 220730: .htacess for more speed and for mobile!
- Updated 220722: .htacces1for protection of: Js, Css files:)
- Updated 220719: .htacces1 for more security and doubles.
- Added protecton, wp.-includes/fonts follder (They download font til´you die!:(
- Updated: Wp.content folder. 
- Updated 220715: protect plugin folder.
- Updated 220715 wp.content folder
- Updated 220709  Works! And added som protection for theme:)
- Updated 220702 
- Updated:220625


Core  .htaccess + .htaccess1 for speed and protection  Set: 444 files rights
in core. 
- Updated: 220625
- Updated: 220731  borth are in best Shape!


Plugins I recommend:
* limit login attempts reloaded:   See: https://wordpress.org/plugins/limit-login-attempts-reloaded/
* disable wp rest-api:  // So they cannot se who is the user: https://wordpress.org/plugins/disable-wp-rest-api/
* wp-cron http auth: // Small very good protectin for  rest api:   https://wordpress.org/plugins/wp-cron-http-auth/

None above takes power fron your blog:)

PAYED Firewall: 
BBQ Pro   // I love the custom - place in protection for strange files!   https://plugin-planet.com/bbq-pro/

BLOCK BAD BOTS  - Blackhole Pro   Works very well:) same adress aas above:)

404 controls: - so bad: https://www.cminds.com/wordpress-plugins-library/404-console-plugin-wordpress/

* None above takes power from your blog!

Happy safe blogging folks:)


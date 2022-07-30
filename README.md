# protect-wordpress
Protect wordpress with .htacess


Protect wordpress with htaccess:)

require_once(ABSPATH.'wp-settings.php');
error_reporting(0);
ini_set('display_errors','Off');
ini_set('error_reporting',E_ALL);
define('DISALLOW_FILE_EDIT',true);
define('DISALLOW_FILE_MODS',true);

Set to: 404 in wp.config.php Also gets some speed!


* Protect: wp.contents folder, plugins,themes and uploads.
* Protect: wp-admin folder.

Core .htaccess for protection and speed.  Set: 444 files rights

-Updated: 220730: .htacess for more speed and for mobile!
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
- Updated: 22-06-25

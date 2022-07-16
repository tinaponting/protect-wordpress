# protect-wordpress
Protect wordpress with .htacess


Protect wordpress with htaccess:)

require_once(ABSPATH.'wp-settings.php');
error_reporting(0);
ini_set('display_errors','Off');
define('DISALLOW_FILE_EDIT',true);
define('DISALLOW_FILE_MODS',true);

Set to: 404 in wp.config.php Also gets some speed!


* Protect: wp.contents folder, plugins,themes and uploads.
* Protect: wp-admin folder.

Core .htaccess for protection and speed.  Set: 444 files rights
- Added protecton, wp.-includes/fonts follder (They download font til´you die!:(
- Updated: Wp.content folder. 
- Updated: protect plugin folder.
- Updated 22-0715 wp.content folder
- Updated 22-07-09  Works! And added som protection for theme:)
- Updated 22-07-02 
- Updated: 22-06-25


Core  .hrtaccess + .htaccess1 for speed and protection  Set: 444 files rights
in core. 
- Updated: 22-06-25

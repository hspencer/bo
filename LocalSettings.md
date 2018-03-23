# Code to "LocalSettings.php" for using the bo flavour to the MediaWiki Chameleon skin

```php
# Chameleon
// Composer
$egChameleonLayoutFile = __DIR__ . '/skins/bo/bo.xml';
$egChameleonExternalStyleModules = [
	__DIR__ . '/skins/bo/bootswatch.less' => $wgScriptPath,
	__DIR__ . '/skins/bo/variables.less' => $wgScriptPath,
	__DIR__ . '/skins/bo/bo.less' => $wgScriptPath
	];
$egChameleonExternalLessVariables = [
	'font-size-base' => '18px',
	'font-size-large' => '20px',
	'font-size-small' => '14px',
	'font-size-h1' => '22px',
	'font-size-h2' => '20px',
	'font-size-h3' => '18px',
	'line-height-base' => '1.5', 
	#'navbar-height' => '80px',
	'navbar-margin-bottom' => '10px',
	'navbar-default-bg' => 'rgba( 94, 157, 200, 1 )',
	'navbar-default-border' => 'rgba( 94, 157, 200, 1 )',
	'nav-tabs-active-link-hover-color' => 'rgba( 255, 255, 255, 1 )',
	];

## Default skin (optional)
$wgDefaultSkin = 'chameleon';
```

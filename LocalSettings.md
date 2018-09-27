# Code to "LocalSettings.php" for using the bo flavour to the MediaWiki Chameleon skin

```php

## Default skin 
$wgDefaultSkin = 'chameleon';

# Chameleon Overrides for BO

## Define Layout
#$egChameleonLayoutFile = __DIR__ . '/skins/bo/layout-navbar.xml';
$egChameleonLayoutFile = __DIR__ . '/skins/bo/layout-tools.xml';

$egChameleonExternalStyleModules = [
	__DIR__ . '/skins/bo/bootswatch.less' => $wgScriptPath,
	__DIR__ . '/skins/bo/variables.less' => $wgScriptPath,
	__DIR__ . '/skins/bo/bo.less' => $wgScriptPath
	];
```

For overriding Bootstrap variables:

```
$egChameleonExternalLessVariables = [
	'font-size-base' => '18px',
	'font-size-large' => '20px',
	'font-size-small' => '14px',
	'font-size-h1' => '22px',
	'font-size-h2' => '20px',
	'font-size-h3' => '18px',
	'line-height-base' => '1.5', 
	'navbar-margin-bottom' => '10px',
	'navbar-default-bg' => 'rgba( 94, 157, 200, 1 )',
	'navbar-default-border' => 'rgba( 94, 157, 200, 1 )',
	'nav-tabs-active-link-hover-color' => 'rgba( 255, 255, 255, 1 )',
	'input-border-focus' => 'rgba(0, 0, 0, .1)'
	];

```

You can add this code if you wish to recompile css after modifying the less files:

```php
# for testing and customizing
\Bootstrap\BootstrapManager::getInstance()->addCacheTriggerFile( __DIR__ . '/skins/bo/bo.less' );
\Bootstrap\BootstrapManager::getInstance()->addCacheTriggerFile( __DIR__ . '/skins/bo/botswatch.less' );
\Bootstrap\BootstrapManager::getInstance()->addCacheTriggerFile( __DIR__ . '/skins/bo/variables.less' );

```

# Bo
**Bo** is a flavour of the MediaWiki [Chameleon skin](https://www.mediawiki.org/wiki/Skin:Chameleon) specially crafted for [Amereida](http://www.amereida.cl) and later for [Casiopea](http://wiki.ead.pucv.cl), which have separate layouts.

**Bo** is named after the poet **Efraín Tomás Bó**.

## Using Bo

To use this flavour on your wiki you will have to install the [MediaWiki Chameleon skin](https://www.mediawiki.org/wiki/Skin:Chameleon) first and clone this repo in the "skins" directory of your wiki.

For making it work you need to modify your  "LocalSettings.php" as follows:

```
# - SKINS
wfLoadSkin( 'chameleon' );

# -- BO SETTINGS

## --------------------------------------------- layout ---------------------------------------------

$egChameleonLayoutFile= '/var/www/casiopea/htdocs/skins/bo/layouts/layout-2022.xml';
# $egChameleonLayoutFile =  __DIR__ . + '/skins/bo/layout-tools.xml'; // esto no sirve!?


## --------------------------------------------- theme  ---------------------------------------------

# $egChameleonThemeFile = ''; // empty restores bootstrap's default
$egChameleonThemeFile  = '/var/www/casiopea/htdocs/skins/bo/scss/bo-riables.scss';


## --------------------------------------------- bo     ---------------------------------------------

$egChameleonExternalStyleModules = [
    '/var/www/casiopea/htdocs/skins/bo/scss/bo.scss' => 'afterFunctions'
];

```
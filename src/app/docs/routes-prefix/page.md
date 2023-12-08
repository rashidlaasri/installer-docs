---
title: Routes Prefix
---
The Laravel Web Installer conveniently prefixes all existing installer steps routes with the **install::** route prefix.

However, if this clashes with an already existing route in your application or if you prefer a different prefix, you have the flexibility to make adjustments. Simply edit the **routes_prefix** key in the **config/installer.php** file to set a new route prefix according to your requirements.

This straightforward customization allows you to integrate the installer seamlessly into your Laravel application without conflicting with any existing routes.


```js
/*
* The default route prefix for all the routes.
*
* You can change it to anything you like.
*/
'routes_prefix' => 'install::',
```

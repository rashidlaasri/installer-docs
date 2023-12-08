---
title: Installer Permissions
---
Much like the default server requirements, the Laravel Web Installer includes a predefined set of folder permissions essential for the proper functioning of a typical Laravel application. However, recognizing that project structures may vary, you have the flexibility to modify, add, or remove these folder permissions as needed. The configuration file, **config/installer.php**, is the central location where you can seamlessly customize these permissions.

```js
/**
 * The folders to check for permissions.
 *
 * You can add or remove folders as you wish.
 *
 * Available options: 'storage/framework/', 'storage/logs/', 'bootstrap/cache/'
 */
'permissions' => [
    'storage/framework/' => '775',
    'storage/logs/' => '775',
    'bootstrap/cache/' => '775',
],
```

This feature ensures that the Laravel Web Installer is adaptable to diverse project setups, allowing you to fine-tune folder permissions according to the specific requirements of your application.

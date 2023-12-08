---
title: Redirection
---
During the installation process, the Laravel Web Installer, by default, redirects to the home page route. If your application doesn't have a route named **home** or if you prefer to redirect to a different location upon installation completion, you can easily customize this behavior. Navigate to the **config/installer.php** file and modify the **homepage** key.

Change it to the desired route name, and the installer will redirect users to the specified location, providing you with the flexibility to tailor the post-installation navigation according to your application's structure and requirements.

```php
/*
* The default homepage route name to redirect to
*
* when the installation process is complete.
*/
'homepage' => 'dashboard',
```

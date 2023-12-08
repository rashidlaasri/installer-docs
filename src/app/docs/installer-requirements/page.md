---
title: Installer Requirements
---
The Laravel Web Installer is equipped with a predefined set of default server requirements that serve as a baseline for ensuring the smooth installation of your application. If you need to customize or extend these requirements to better suit your project, you can easily do so by navigating to the **config/installer.php** file.

Within this configuration file, you'll find the ability to add, modify, or remove specific server requirements according to the specific needs of your application.

```js
/**
 * The server requirements to verify before installation.
 *
 * You can add or remove requirements as you wish.
 *
 * Available options: 'php_version', 'extensions', 'apache_modules'
 */
'requirements' => [
    'php_version' => '7.3.0',
    'extensions' => [
        'openssl',
        'pdo',
        'mbstring',
        'tokenizer',
        'JSON',
        'cURL',
    ],
    'apache_modules' => [
        'mod_rewrite',
    ],
],
```

This flexibility allows you to tailor the installation process to match the server environment where your Laravel application will be deployed, ensuring that all necessary conditions are met for a successful installation.

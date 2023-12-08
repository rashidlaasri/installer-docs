---
title: Environnement Variables
---
The **Laravel Web Installer** simplifies the configuration of environment variables and application settings by providing an intuitive and user-friendly interface.

This UI allows you to effortlessly edit the values of environment variables, ensuring a smooth and accessible experience during the installation process. For further customization, you have the flexibility to add or remove specific values by modifying the keys within the **environment** array in the installer configuration file **config/installer.php**. Each key corresponds to its own input field, providing a straightforward mechanism to tailor the configuration settings based on your project's requirements.

```js
/**
 * The environment variables to set in .env file.
 *
 * You can add or remove variables as you wish.
 *
 * You can also set default values for each variable.
 *
 * The installer will ask you to provide the value for each variable.
 */
'environment' => [
    'APP_NAME' => 'Laravel',
    'APP_ENV' => 'production',
    'APP_KEY' => '',
    'APP_DEBUG' => 'true',
    'APP_URL' => 'http://localhost',
    'DB_CONNECTION' => 'mysql',
    'DB_HOST' => '127.0.0.1',
    'DB_PORT' => '3306',
    'DB_DATABASE' => 'laravel',
    'DB_USERNAME' => 'root',
    'DB_PASSWORD' => '',
],
```

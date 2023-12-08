---
title: Ordering Steps
---
You have the flexibility to customize the order of installation steps by modifying the configuration file.

Open the **config/installer.php** file, and within the **steps** array key, rearrange the lines to reflect the desired sequence. By simply changing the order of the lines in the **steps** array, you can effortlessly control the presentation order of each step during the installation process.

This straightforward approach allows you to tailor the user experience according to your specific requirements, ensuring a seamless and intuitive flow for your Laravel Web Installer.

```php
return [
    new \RachidLaasri\Installer\Steps\Welcome,
    new \App\Installer\Steps\YourCustomStep,
    new \RachidLaasri\Installer\Steps\ServerRequirements,
    new \RachidLaasri\Installer\Steps\Database,
    new \App\Installer\Steps\AnotherCustomStep,
    new \RachidLaasri\Installer\Steps\Finished,
];
```

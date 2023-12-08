---
title: Migrations and seeding
---
In the **new \RachidLaasri\Installer\Steps\Database** step of the Laravel Web Installer, the installation process takes care of running both the migration and seed commands.

This automated action ensures the creation of your database tables and the population of these tables with the necessary data, eliminating the need for manual intervention.

The installer seamlessly handles these database-related tasks to streamline the installation experience. However, should you wish to disable this automatic migration and seeding process for specific reasons, you have the option to do so by removing or commenting out the corresponding line in the **steps** key within the installer configuration file **config/installer.php**. This level of control allows you to tailor the installation steps according to your project's requirements and preferences.

```php
DB::transaction(function () {
    Artisan::call('migrate', ['--force' => true]);
    Artisan::call('db:seed', ['--force' => true]);
});
```

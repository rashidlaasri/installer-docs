---
title: Adding Steps
---
To add a new installation step to the Laravel Web Installer, follow these steps:

Run the following command to generate a new step class named ApplicationConfig:
```bash
php artisan make:step ApplicationConfig
```

This command creates an **ApplicationConfig** class in the **app/Installer/Steps** directory, in the generated class (`app/Installer/Steps/ApplicationConfig.php`), customize the route, title, and description for your new step:

```php
<?php

namespace App\Installer\Steps;

use Illuminate\Contracts\View\View;
use Illuminate\Http\RedirectResponse;
use RachidLaasri\Installer\Steps\Step;
use RachidLaasri\Installer\Steps\StepInterface;

class ApplicationConfig extends Step implements StepInterface
{
    public function __construct()
    {
        parent::__construct(
            route: 'step-route',
            title: 'Step title',
            description: 'Step description',
        );
    }

    public function view(): View
    {
        return view('web-installer::application-config', [
            'step' => $this,
        ]);
    }

    public function process(): RedirectResponse
    {
        return redirect()->route($this->next()->route());
    }
}
```

It also creates a controller for the new step in `app/Http/Controllers/ApplicationConfigController.php`:
```php
<?php

namespace App\Http\Controllers;

use RachidLaasri\Installer\Controllers\Controller;
use App\Installer\Steps\ApplicationConfig;

class ApplicationConfigController extends Controller
{
    public function __construct()
    {
        parent::__construct(new ApplicationConfig);
    }
}
```

Finally, it also creates a view file for the new step in `resources/views/vendor/installer/application-config.blade.php`. Customize the content of this file to suit your specific installation step:
```blade
@extends('web-installer::layout')

@section('content')
    Your custom step content goes here. Build something amazing!
@endsection
```

After generating the step, proceed to integrate it into your installer by executing the command to publish the configuration files:

```bash
php artisan vendor:publish --tag=web-installer
```

Next, navigate to the *config/installer.php* file. Within the steps array key, include your newly generated step. Place it in the desired order to determine its visibility during the installation process:

```php
'steps' => [
    ...
    new \App\Installer\Steps\ApplicationConfig,
    ...
],
```

By following these steps, you've successfully added a new installation step to the Laravel Web Installer. Customize the content and logic within the generated files to tailor the installation process to your project's requirements.

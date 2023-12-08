---
title:  Installation
---
With the Laravel Web Installer package successfully integrated into your project, you can now your users through the installation process. Follow the steps bellow to install it.

## Setup
Currently, the installation of the Laravel Web Installer is limited to a local package. Please refer to the guide below for instructions on how to proceed.

### Setting up the Package:
After downloading the package, move the folder to the root folder of your project
and then add the following entry to the repositories section (create one if it doesn't exist):

```json
"repositories": [
    {
        "type": "path",
        "url": "./laravel-installer"
    }
],
```

And change the **minimum-stability** to dev:

```json
"minimum-stability": "dev",
```

### Install the Package:
Return to your Laravel project's root folder in the terminal and add the package to your project's dependencies:

```bash
composer require rachidlaasri/web-installer:@dev-main
```

This command installs the local version of the package in your Laravel project.

Now, you have successfully installed the Laravel Web Installer package as a local package in your Laravel project. Customize the installer as needed and follow the usage instructions to integrate it into your application.

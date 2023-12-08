---
title: Middleware
---
For security reasons and to ensure a single installation on production environments, the Laravel Web Installer incorporates a check for a file within the storage folder.

The filename associated with this check is configured in the **installed_key_name** key found in the **config/installer.php** file. For added flexibility, you have the ability to customize this filename to any value of your choice.

To gain a deeper understanding of this security measure, refer to the **RachidLaasri\Installer\Middleware\ShouldBeInstalled** middleware, where the installation status is verified.

{% callout title="You should know!" %}
It's worth noting that in local environments, you retain the freedom to install the application as many times as needed. This mechanism ensures a secure and controlled installation process, particularly in production environments, while accommodating development and testing needs in local environments.
{% /callout %}

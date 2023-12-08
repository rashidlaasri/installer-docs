---
title: Events and listeners
---
Throughout each step of the installation process, the Laravel Web Installer triggers events, providing a convenient hook for developers to execute additional custom code.

This event-driven architecture enhances extensibility, allowing you to seamlessly integrate any extra functionalities or custom logic into the installation workflow.

The list of events currently being fired during the installation process is:


|Event | Description  |
|--|--|
| \RachidLaasri\Installer\Events\InstallationStarted | Fires when the installation process starts. |
| \RachidLaasri\Installer\Events\ServerRequirementsStepFinished | Fires when a successful server requirements step finishes. |
| \RachidLaasri\Installer\Events\PermissionsStepFinished | Fires when a successful folder permissions step finishes. |
| \RachidLaasri\Installer\Events\EnvironmentStepFinished | Fires after the user submittes the environment values form. |
| \RachidLaasri\Installer\Events\DatabaseStepFinished | Fires after a successful database migration and seed. |
| \RachidLaasri\Installer\Events\InstallationFinished | Fires when the installation process finishes. |


 By listening to these events, developers can tap into specific points within the installation lifecycle, ensuring a flexible and extensible platform for incorporating project-specific requirements or customizations.

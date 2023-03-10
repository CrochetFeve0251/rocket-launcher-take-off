# rocket-launcher-take-off
Rocket Launcher Take Off is the library containing the CLI command used to initialize a Rocket Launcher project.

To install the library first launch the following command: `composer require CrochetFeve0251/rocket-launcher-take-off --dev`

Then at the root from your project you can create a `builder` file with the following content:
```php

#!/usr/bin/php
<?php
use RocketLauncherBuilder\AppBuilder;

require_once __DIR__ . '/vendor/autoload.php';

AppBuilder::init(__DIR__ . '/../', [
        \RocketLauncherTakeOff\ServiceProvider::class,
]);

```

## Usage
To initialize the project run the following command: `initialize`.

On the command the following options are available:
| Option        | Short option | Value              | Default | Description                                                                 |
|:-------------:|:------------:|:------------------:|:--------|:---------------------------------------------------------------------------:|
| name          |     n        | your name          | false   | Name from the plugin                                                        |
| description   |     d        | your description   | false   | Descripton from the plugin                                                  |
| author        |     a        | the author         | false   | Author from the plugin                                                      |
| url           |     u        | the url            | false   | URL from the plugin                                                         |
| php           |     p        | PHP version        | false   | Minimal PHP version to make the plugin running                              |
| wp            |     w        | WP version         | false   | Minimal WordPress version to make the plugin running                        |

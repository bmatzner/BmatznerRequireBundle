RequireJS Bundle for Symfony2
=======================

## Current Version

RequireJS 2.1.6

Plugins:
cs: 0.4.3
domReady: 2.0.1
i18n: 2.0.2
text: 2.0.6

## Installation

### Add bundle to your composer.json file

``` js
// composer.json

{
    "require": {
		// ...
        "bmatzner/require-bundle": "*"
    }
}
```

### Add bundle to your application kernel

``` php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Bmatzner\RequireBundle\BmatznerRequireBundle(),
        // ...
    );
}
```

### Download the bundle using Composer

``` bash
$ php composer.phar update bmatzner/require-bundle
```

### Install assets

Given your server's public directory is named "web", install the public vendor resources

``` bash
$ php app/console assets:install web
```

Optionally, use the --symlink attribute to create links rather than copies of the resources 

``` bash
$ php app/console assets:install --symlink web
```

## Usage

Refer to the desired files in your HTML template, e.g.

``` html
<script type="text/javascript" src="{{ asset('bundles/bmatznerrequire/js/require.min.js') }}" data-main="{{ asset('js/myapp.js') }}"></script>
```

## Licenses

Refer to the source code of the included files for license information

## References

1. http://requirejs.org
2. http://symfony.com

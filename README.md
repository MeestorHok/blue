# Blue CMS

[![Build Status][ico-build]][link-travis]
[![Quality Score][ico-scrutinizer]][link-scrutinizer]
[![Latest Stable Version][ico-stable]][link-packagist]
[![Latest Unstable Version][ico-unstable]][link-packagist]
[![License][ico-license]][link-license]
[![Total Downloads][ico-downloads]][link-packagist]

Premier SEO driven CMS powered by Laravel

## Install

Via Composer

``` bash
$ composer require meestorhok/blue
```

###Update the Laravel Framework

Add the following to config/app.php

``` php
'providers' => [
    Collective\Html\HtmlServiceProvider::class, // HTML generator
    Artesaos\SEOTools\Providers\SEOToolsServiceProvider::class, // SEO generator
    MeestorHok\Blue\BlueServiceProvider::class // Blue CMS
],
'aliases' => [
    'Html' => Collective\Html\HtmlFacade::class, // HTML facade
    'Form' => Collective\Html\FormFacade::class, // HTML Form facade
    'SEO' => Artesaos\SEOTools\Facades\SEOTools::class // SEO facade
]
```

then, run this cli command to setup the database

``` bash
$ php artisan migrate --path=vendor/MeestorHok/Blue/src/migrations
```

Make sure you don't have any routes in your app/Http/routes.php file. **ALL** routes should be auto-generated by Blue CMS.
If you wish to edit the absolute routes, you can find them in [vendor/MeestorHok/Blue/src/Http/routes.php](src/Http/routes.php).
*Edit with caution*

## Usage

TODO


## Security

If you discover any security related issues, please email jake@jmitchell.co instead of using the issue tracker.

## Credits

- [Jake Mitchell][link-author]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File][link-license] for more information.

[ico-stable]: https://poser.pugx.org/meestorhok/blue/v/stable
[ico-unstable]: https://poser.pugx.org/meestorhok/blue/v/unstable
[ico-downloads]: https://poser.pugx.org/meestorhok/blue/downloads
[ico-license]: https://poser.pugx.org/meestorhok/blue/license
[ico-scrutinizer]: https://scrutinizer-ci.com/g/MeestorHok/Blue/badges/quality-score.png?b=master
[ico-build]: https://travis-ci.org/MeestorHok/Blue.svg

[link-travis]: https://travis-ci.org/MeestorHok/Blue
[link-packagist]: https://packagist.org/packages/meestorhok/blue
[link-scrutinizer]: https://scrutinizer-ci.com/g/meestorhok/blue
[link-license]: ./LICENSE.md
[link-author]: https://github.com/MeestorHok
[link-contributors]: ../../contributors

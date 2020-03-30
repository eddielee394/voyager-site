# Voyager Site

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Build Status][ico-travis]][link-travis]

The package is an implementation of a simple but useful subsystem of a basic content organization for the [Voyager Admin Panel](https://github.com/the-control-group/voyager) package.
Using this package you can rapidly and easily build small and medium-size scale web-sites.   

## Features

- Basic Page management module, including systems pages.
- Basic SEO implementation - Seo title, Meta Description and Meta Keywords parameters.
- Breadcrumbs implementation. 
- Flexible Block / Widget management module, to build parts of your site pages.
- Page layout construction using flexible Blocks/Widgets. 
- Form management system, including AJAX sending.
- Localizations from DB table, where you can easily keep and manage your translations.
- Advanced site settings module, including mail smtp settings and a mail sending test out of the box.

## Installation

> #### Requirement
> You should fully install the package [Voyager Extension](https://github.com/MonstreX/voyager-extension) before.

Via Composer

``` bash
$ composer require monstrex/voyager-site
```

Then run install command:
``` bash
$ php artisan voyager-site:install
```

Publish config if you need:
```
$ php artisan vendor:publish --provider="MonstreX\VoyagerSite\VoyagerSiteServiceProvider" --tag="config"
```


## Usage

### Config file

- **route_home_page** - Route name for Home Page ('home' by default).
- **default_model_table** - Default model table name to find records ('pages' by default).
- **default_slug_field** - Default slug field name ('slug' by default).
- **use_legacy_error_handler** - If _false_ will be used voyager-site 404 error handler. 
- **template** - Root folder name where stored view template files ('template' by default).
- **template_master** - Master template name ('layouts.master' by default).
- **template_layout** - Main Layout Template name ('layouts.main' by default).
- **template_page** - Page template name ('pages.page' by default).  

### Site Settings 

Site settings is a flexible and extendable easy to use settings subsystem integrated in the package. 

![Site settings](/docs/images/settings-1.png)

You can use and modify exist settings and group and add you own group and settings.
To retrieve certain setting you may use helper function:
```php
$mail = site_setting('mail.to_address');
```  
> Some of the site settings used by internal package functions and override Laravel .env settings.

The settings have built-in SMTP mail parameters and the mail sending test function.
![Site settings - Mail](/docs/images/settings-mail.png)


 

## Security

If you discover any security related issues, please email author email instead of using the issue tracker.

## Credits

- [author name][link-author]
- [All Contributors][link-contributors]

## License

license. Please see the [license file](license.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/monstrex/testpackage.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/monstrex/testpackage.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/monstrex/testpackage/master.svg?style=flat-square
[ico-styleci]: https://styleci.io/repos/12345678/shield

[link-packagist]: https://packagist.org/packages/monstrex/testpackage
[link-downloads]: https://packagist.org/packages/monstrex/testpackage
[link-travis]: https://travis-ci.org/monstrex/testpackage
[link-styleci]: https://styleci.io/repos/12345678
[link-author]: https://github.com/monstrex
[link-contributors]: ../../contributors

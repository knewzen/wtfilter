<p align="center">
<a href="https://travis-ci.org/kaankilic/wtfilter"><img src="https://travis-ci.org/kaankilic/wtfilter.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/kaankilic/wtfilter"><img src="https://poser.pugx.org/kaankilic/wtfilter/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/kaankilic/wtfilter"><img src="https://poser.pugx.org/kaankilic/wtfilter/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/kaankilic/wtfilter"><img src="https://poser.pugx.org/kaankilic/wtfilter/license.svg" alt="License"></a>

## Introduction
`WTFilter` provides an expressive and fluent way to filter profanities from the content with using it's own engine. `WTFilter` is the simplest stable profanity filter for Laravel.

## License

Laravel WTFilter is open-sourced software licensed under the [BSD-2 license](http://opensource.org/licenses/BSD-2-Clause)

## Official Documentation
It's simplest way of filtering profanities with the capabilities of Language form. You can set multilangual profanities on each language that you are using on your Laravel project.

### Installation
To get started with WTFilter, use Composer to add the package to your project's dependencies:

```php
composer require kaankilic/wtfilter
```
After installing the `WTFilter` library, register the `Kaankilic\Socialite\Providers\WTFilterServiceProvider` in your `config/app.php` configuration file:

```php
Kaankilic\WTFilter\Providers\WTFilterServiceProvider::class,
```
Also, add the `WTFilter` facade to the `aliases` array in your `app` configuration file:

```php
Kaankilic\WTFilter\Facades\WTFilter::class
```

### Basic Usage
```php
<?php

namespace App\Http\Controllers;

use WTFilter;

class CommentsController extends Controller
{
    /**
     * It's filtering your comments that contains profanities.
     */
    public function createComment(Request $request){
    	$contentOfComments = WTFilter::filter($request->get("content_of_comment"));
        
    }
}
```

phpThumb for Laravel 4
========

This is the [phpThumb](https://github.com/JamesHeinrich/phpThumb) library wrapped inside a Laravel 4 package.

Installation
--------
Add [this](https://packagist.org/packages/matteoantoci/phpthumb) package to your composer.json

Add this service provider in /app/config/app.php

```
    'Matteoantoci\Phpthumb\PhpthumbServiceProvider',
```

Use
--------
A new route will be created /phpthumb

Use the library as described [here](http://phpthumb.sourceforge.net/demo/demo/phpThumb.demo.demo.php)


phpThumb Helper
--------
Add this alias in /app/config/app.php to use phpThumb Helper in your templates.

```
    'phpThumb' => 'Matteoantoci\Phpthumb\PhpthumbHelper'
```

The helper class consist on a single static function with this parameters:

```
    get($img, $w = "", $h = "", $crop = true, $params = array())
```

- $img -> path of image
- $w -> max width
- $h -> max height
- $crop -> if you want to use zoom-crop feature (true by default)
- $params -> array of additional parameters. Eg: 'fltr[]=gray'
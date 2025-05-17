# Installing Omeka S

## System requirements

- Linux
- Apache (with [AllowOverride](https://httpd.apache.org/docs/2.4/mod/core.html#allowoverride){target=_blank} set to "All" and [mod_rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html){target=_blank} enabled)
- MySQL, minimum version 5.7.9 (or MariaDB, minimum version 10.2.6)
- PHP, minimum version 7.4, with [PDO](http://php.net/manual/en/intro.pdo.php){target=_blank}, [pdo_mysql](http://php.net/manual/en/ref.pdo-mysql.php){target=_blank}, and [xml](http://php.net/manual/en/intro.xml.php){target=_blank} extensions installed. PHP 8.4 is not currently supported.
- Optional, to create thumbnails: ImageMagick version 6.7.5 or greater, the PHP `imagick` extension, or the PHP `gd` extension.

[GD](https://secure.php.net/manual/en/intro.image.php){target=_blank} is a basic graphic library installed by default with PHP. It can create thumbnails for common image formats only (jpeg, gif, png). [Imagick and ImageMagick](https://www.imagemagick.org){target=_blank} are the same library and can create thumbnails for more than 200 formats. For more information, see the [Configuration page](configuration.md#thumbnails).

## Installation methods

### Docker
参考：
https://github.com/grandgeorg/docker-omeka-s/tree/main?tab=readme-ov-file

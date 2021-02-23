# FatSmallTools
A series of small tools to do strange things. 
# Installation 
Ensure that the PHP version is above 7.0.

It is recommended via Composer to install

Please refer to the official configuration for the installation of Composer.

After installing Composer, create a composer.json file in your project: 
```json
{
    "require": {
        "tianhe1986/fatsmalltools": "*"
    }
}
```

Then execute under the project folder: 
```bash
$ composer install
```

After adding autoloader: 
```php
<?php
require "vendor/autoload.php";
```

# Navicat password save encryption and decryption 
For the principle, refer to [how-does-navicat-encrypt-password](https://github.com/DoubleLabyrinth/how-does-navicat-encrypt-password)，, if you are interested, you can study it by yourself^^ 
```php
use FatSmallTools\NavicatPassword;

//Need to specify the version, 11 or 12

$navicatPassword = new NavicatPassword(11);
//$navicatPassword = new NavicatPassword(12);

//加密
$encode = $navicatPassword->encrypt('123456'); // verstion 11 15057D7BA390, version 12 833E4ABBC56C89041A9070F043641E3B

//解密
$decode = $navicatPassword->decrypt('15057D7BA390');
//$decode = $navicatPassword->decrypt('833E4ABBC56C89041A9070F043641E3B');
```

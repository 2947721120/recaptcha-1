##CN 机器翻译,请参照    EN下原文理解
＃验证码PHP客户端库

[！[构建状态]（https://travis-ci.org/google/recaptcha.svg）]（https://travis-ci.org/google/recaptcha）
[！[最新稳定Version](https://poser.pugx.org/google/recaptcha/v/stable.svg)](https://packagist.org/packages/google/recaptcha)
[！[总Downloads](https://poser.pugx.org/google/recaptcha/downloads.svg)](https://packagist.org/packages/google/recaptcha)

*项目页面：http://www.google.com/recaptcha/
*库：https://github.com/google/recaptcha
*版本：1.1.2
*许可：BSD，请参阅[许可（LICENSE）

##说明

验证码是一个免费的CAPTCHA服务，防止垃圾邮件和滥用网站。
这是谷歌编写代码，提供第三方集成插件
使用reCAPTCHA。

##安装

###作曲（推荐）

[作曲]（https://getcomposer.org/）是PHP一种广泛使用的依赖管理
包。这验证码客户端可在Packagist作为
[`谷歌/ recaptcha`]（https://packagist.org/packages/google/recaptcha），并且可以是
可以通过运行`作曲家require`命令或添加库安装
你`composer.json`。为了使作曲家为你的项目，请参考
项目的[开始]（https://getcomposer.org/doc/00-intro.md）
文档。

要使用命令添加这种依赖关系，从​​运行中的以下的
项目目录：
```
作曲家要求谷歌/验证码“〜1.1”
```

另外，添加的依赖，直接到你的`composer.json`文件：
```JSON
“规定”：{
    “谷歌/验证码”：“〜1.1”
}
```

###直接下载（无作曲）

如果你想手动安装库（即无作曲），那么你
可以使用链接主要项目主页上要么复制回购或下载
在[ZIP文件（https://github.com/google/recaptcha/archive/master.zip）。对于
方便，自动加载磁带机脚本中`的src / autoload.php`提供您
可以要求到脚本，而不是作曲家的'供应商/ autoload.php`。对于
例：

```PHP
需要（'/路径/要/验证码/ src目录/ autoload.php'）;
验证码$ =新\验证码\验证码（$秘密）;
```

在该项目中的类是按照结构化
[PSR-4]（http://www.php-fig.org/psr/psr-4/）标准，所以你当然也可以
使用自己的自动加载磁带机或直接在你的代码需要所需的文件。

###安装发展

如果你想在内部推动这一项目或运行单元测试
您自己的环境，你需要安装开发的依赖，在
这种情况下，这意味着[PHPUnit的]（https://phpunit.de/）。如果克隆回购，
从回购中运行`作曲家install`，这也将抢PHPUnit的所有
其依赖你。如果你只需要自动加载机安装，那么你
可以随时指定作曲家不要在发展模式下运行，例如`作曲家
安装--no-dev`。

*注：*只需要发展这些依赖关系，没有
他们要求被包含在你的产品代码。

##用法

首先，在https://www.google.com/recaptcha/admin注册为您的网站钥匙

当您的应用程序接收到包含`G-验证码-response`一个表单提交
现场，您可以使用验证：
```PHP
<？PHP
验证码$ =新\验证码\验证码（$秘密）;
$ RESP = $ recaptcha->验证（$ gRecaptchaResponse，$ REMOTEIP）;
如果（$ resp-> isSuccess（））{
    //验证！
}其他{
    $错误= $ resp-> getErrorCodes（）;
}
```

你可以看到在端至端工作的例子
[例子/例子-captcha.php（例如/例如，captcha.php）

##升级

###从1.0.0

此客户端的前一个版本仍然可以在`1.0.0`标记[在
这种回购（https://github.com/google/recaptcha/tree/1.0.0），但它是纯粹为
参考，并不会收到任何更新。

在1.1.0的主要变化是：
*现在可以通过安装作曲;
*类加载还可以通过作曲;
*类的命名空间现在;
*旧的方法调用是`$ RC-> verifyResponse（$ REMOTEIP，$响应）`，新的呼叫
  `$ RC->验证（$响应，$ REMOTEIP）`

##投稿

我们接受通过GitHub上引入请求的贡献，但所有贡献者需要
标准的谷歌贡献者许可协议所涵盖。你可以找到
在此说明[特约]（CONTRIBUTING.md）

##EN
# reCAPTCHA PHP client library

[![Build Status](https://travis-ci.org/google/recaptcha.svg)](https://travis-ci.org/google/recaptcha)
[![Latest Stable Version](https://poser.pugx.org/google/recaptcha/v/stable.svg)](https://packagist.org/packages/google/recaptcha)
[![Total Downloads](https://poser.pugx.org/google/recaptcha/downloads.svg)](https://packagist.org/packages/google/recaptcha)

* Project page: http://www.google.com/recaptcha/
* Repository: https://github.com/google/recaptcha
* Version: 1.1.2
* License: BSD, see [LICENSE](LICENSE)

## Description

reCAPTCHA is a free CAPTCHA service that protect websites from spam and abuse.
This is Google authored code that provides plugins for third-party integration
with reCAPTCHA.

## Installation

### Composer (Recommended)

[Composer](https://getcomposer.org/) is a widely used dependency manager for PHP
packages. This reCAPTCHA client is available on Packagist as
[`google/recaptcha`](https://packagist.org/packages/google/recaptcha) and can be
installed either by running the `composer require` command or adding the library
to your `composer.json`. To enable Composer for you project, refer to the
project's [Getting Started](https://getcomposer.org/doc/00-intro.md)
documentation.

To add this dependency using the command, run the following from within your
project directory:
```
composer require google/recaptcha "~1.1"
```

Alternatively, add the dependency directly to your `composer.json` file:
```json
"require": {
    "google/recaptcha": "~1.1"
}
```

### Direct download (no Composer)

If you wish to install the library manually (i.e. without Composer), then you
can use the links on the main project page to either clone the repo or download
the [ZIP file](https://github.com/google/recaptcha/archive/master.zip). For
convenience, an autoloader script is provided in `src/autoload.php` which you
can require into your script instead of Composer's `vendor/autoload.php`. For
example:

```php
require('/path/to/recaptcha/src/autoload.php');
$recaptcha = new \ReCaptcha\ReCaptcha($secret);
```

The classes in the project are structured according to the
[PSR-4](http://www.php-fig.org/psr/psr-4/) standard, so you may of course also
use your own autoloader or require the needed files directly in your code.

### Development install

If you would like to contribute to this project or run the unit tests on within
your own environment you will need to install the development dependencies, in
this case that means [PHPUnit](https://phpunit.de/). If you clone the repo and
run `composer install` from within the repo, this will also grab PHPUnit and all
its dependencies for you. If you only need the autoloader installed, then you
can always specify to Composer not to run in development mode, e.g. `composer
install --no-dev`.

*Note:* These dependencies are only required for development, there's no
requirement for them to be included in your production code.

## Usage

First, register keys for your site at https://www.google.com/recaptcha/admin

When your app receives a form submission containing the `g-recaptcha-response`
field, you can verify it using:
```php
<?php
$recaptcha = new \ReCaptcha\ReCaptcha($secret);
$resp = $recaptcha->verify($gRecaptchaResponse, $remoteIp);
if ($resp->isSuccess()) {
    // verified!
} else {
    $errors = $resp->getErrorCodes();
}
```

You can see an end-to-end working example in
[examples/example-captcha.php](examples/example-captcha.php)

## Upgrading

### From 1.0.0

The previous version of this client is still available on the `1.0.0` tag [in
this repo](https://github.com/google/recaptcha/tree/1.0.0) but it is purely for
reference and will not receive any updates.

The major changes in 1.1.0 are:
* installation now via Composer;
* class loading also via Composer;
* classes now namespaced;
* old method call was `$rc->verifyResponse($remoteIp, $response)`, new call is
  `$rc->verify($response, $remoteIp)`

## Contributing

We accept contributions via GitHub Pull Requests, but all contributors need to
be covered by the standard Google Contributor License Agreement. You can find
instructions for this in [CONTRIBUTING](CONTRIBUTING.md)

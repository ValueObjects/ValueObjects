# ValueObjects

<p align="center">
<a href="mailto:www@mehmetogmen.com.tr"><img src="https://img.shields.io/badge/email-www@mehmetogmen.com.tr-blue.svg?style=flat-square"></a>
</p>

## About Value Objects

<p>Beyond OOP ...</p>

Today, we software developers apply the OOP techniques we learn while writing code. Methods, classes, inheritances, etc. While this is a nice thing, should we be content with these while the technologies we use allow for more?

### What do I mean?

Let me explain a little more about what I mean. Let's assume that we are doing a weather project with the classical OOP approach and we want our users to be able to see the air temperature in Celsius, Kelvin and Fahrenheit temperature units. Most likely the code we would write would look like this:
```php
$celsius = 23.45;

$kelvin = $celsius + 273.15;
echo $kelvin;    // result 296.6

$fahrenheit = $celsius * 1.8 + 32;
echo $fahrenheit;    // result 74.21
```

In short, we need to create a smart class to make meaningless (stupid) data significant in the classical approach. Well, can't we do more? Instead of creating a variable and assigning a value, wouldn't it be easier to convert the value we assign to an object and make our operations with this object? For example:
```php
$celsius = new Celsius(23.45);
echo $celsius->convert()->toKelvin();    // result 296.6
echo $celsius->convert()->toFahrenheit();    // result 74.21
```

ValueObjects library has been created to prepare objects that software developers often need or may need. It is grouped according to their types and divided into sub-packages. This package is the main package in which all sub-packages are collected.

## Requirements

PHP 7.4+. Other than that, this library has no requirements. ValueObjects will not provide any support for PHP versions not supported by the language itself. There may be dependencies for a feature. See the documentation for more information.

## Install

```bash
$ composer require valueobjects/valueobjects
```

## Sub Packages

This git repository is the main package in which the sub-packages listed below are included. If you do not need the entire package, you can choose one or more of our packages below and include them in your project.

- [Common](https://github.com/ValueObjects/Common): It is the auxiliary package used by all sub-packages. You can use it to create your own ValueObjects package.
- [Metrology](https://github.com/ValueObjects/Metrology): The package of Metrology. You can use it for measurement sciences such as mass, temperature, length.

## Learning ValueObjects

If you know OOP, you can use it very easily and integrate it into your projects. If you don't know, you can learn relatively easier than frameworks and find out what OOP is capable of.

More details and documents will be prepared soon, this area will be edited when ready.

## Contributing

Thank you for finding value in improving the ValueObjects library. To contribute, you can contact me at [www@mehmetogmen.com.tr](mailto:www@mehmetogmen.com.tr).

## Security Vulnerabilities

If you discover a security vulnerability within ValueObjects, please send an e-mail to Mehmet ÖĞMEN via [www@mehmetogmen.com.tr](mailto:www@mehmetogmen.com.tr). All security vulnerabilities will be promptly addressed.

## License

The ValueObjects library is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
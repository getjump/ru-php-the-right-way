---
title: Сообщения об ошибках
isChild: true
---

## Сообщения об ошибках

Логирование ошибок может быть полезным, при поиске проблемных мест вашего приложения, но он так-же сможет разоблачить информацию о структуре вашего приложения. Для эффективной защиты вашего приложения от проблем, которые могут быть вазываны выводом этих сообщений, вам нужно настроить сервер по-разному во время разработки и во время режима продукта(production(live)).

### Разработка

To show errors in your <strong>development</strong> environment, configure the following settings in your `php.ini`:
Для показа ошибок в вашей среде <strong>разработки</strong>, сконфигурируйте следующие настройки в вашем `php.ini`:

- display_errors: On
- error_reporting: E_ALL
- log_errors: On

### Продукт

Чтобы спрятать ошибки в вашей среде <strong>продукта</strong>, сконфигурируйте ваш `php.ini`, как предложено ниже:

- display_errors: Off
- error_reporting: E_ALL
- log_errors: On

С этими параметрами в производстве, ошибки будут добавляться в лог ошибок веб-сервера, но не будут показываься пользователю. Для получения дополнительной информации о этих параметрах, смотрите руководство PHP:

* [Error_reporting](http://www.php.net/manual/ru/errorfunc.configuration.php#ini.error-reporting)
* [Display_errors](http://www.php.net/manual/ru/errorfunc.configuration.php#ini.display-errors)
* [Log_errors](http://www.php.net/manual/ru/errorfunc.configuration.php#ini.log-errors)
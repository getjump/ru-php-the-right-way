---
isChild: true
---

## Установка в Windows {#windows_setup_title}

В Windows PHP можно получить несколькими путями. Вы можете [загрузить установочные файлы][php-downloads] и до недавнего времени вы могли использовать
'.msi' установщик. Установщик более не поддерживается и остановлен на PHP 5.3.0.

Для изучения и локальной разработки вы можете использовать встроенный в PHP 5.4 вебсервер, так что вы можете не беспокоится о его конфигурации.
Если вы предпочитаете сервера "всё-в-одном", которые включают полноценный веб-сервер и так-же MySQL, тогда вам нужны инструменты, как 
[Web Platform Installer][wpi], [Zend Server CE][zsce], [XAMPP][xampp] и [WAMP][wamp] , которые помогут сделать быстро окружение для разработки в Windows.
Но, стоит сказать, что эти инструменты будут отличаться от продакшна, так что будьте осторожны по поводу различий окружения, если вы работаете на Windows
и деплоите на Linux.

Если вам нужно запустить конечную систему на Windows, тогда IIS7 даст вам лучшую стабильность и производительность. Вы можете использовать
[phpmanager][phpmanager] (плагин для IIS7) для легкой конфигурации и управлении PHP. IIS7 поставляется с встроенным FastCGI,
вам нужно просто настроить PHP в качестве обработчика. Для поддержки и дополнительной информации посетите [iis.net][php-iis].

[php-downloads]: http://windows.php.net
[phpmanager]: http://phpmanager.codeplex.com/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[zsce]: http://www.zend.com/en/products/server-ce/
[xampp]: http://www.apachefriends.org/en/xampp.html
[wamp]: http://www.wampserver.com/
[php-iis]: http://php.iis.net/

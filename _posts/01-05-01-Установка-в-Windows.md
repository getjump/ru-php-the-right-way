---
isChild: true
---

## Установка в Windows {#windows_setup_title}

PHP для Windows можно получить несколькими путями. Вы можете [загрузить установочные файлы][php-downloads] и, до недавнего времени, вы могли использовать '.msi' установщик. Начиная с PHP версии 5.3.0 установщик не поддерживается.

Для изучения и локальной разработки вы можете использовать встроенный в PHP 5.4 веб-сервер, о конфигурации которого можно не беспокоиться. Если вы предпочитаете сервера «всё-в-одном», которые включают в себя полноценный веб-сервер и MySQL, тогда можете воспользоваться такими инструментами, как [Web Platform Installer][wpi], [Zend Server CE][zsce], [XAMPP][xampp] или [WAMP][wamp], которые помогут быстро развернуть окружение для разработки в Windows. Но, стоит сказать, что эти инструменты будут отличаться от продакшна, так что будьте осторожны и учитывайте эти различия, если вы работаете на Windows и деплоите на Linux.

Если вам нужно запустить конечную систему на Windows, то IIS7 даст вам лучшую стабильность и производительность. Вы можете использовать [phpmanager][phpmanager] (плагин для IIS7) для легкого конфигурования и управления PHP. IIS7 поставляется с встроенным FastCGI, вам нужно просто настроить PHP в качестве обработчика. Для получения помощи и дополнительной информации посетите [iis.net][php-iis].

[php-downloads]: http://windows.php.net
[phpmanager]: http://phpmanager.codeplex.com/
[wpi]: http://www.microsoft.com/web/downloads/platform.aspx
[zsce]: http://www.zend.com/en/products/server-ce/
[xampp]: http://www.apachefriends.org/en/xampp.html
[wamp]: http://www.wampserver.com/
[php-iis]: http://php.iis.net/

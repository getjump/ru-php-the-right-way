---
isChild: true
---

## Виртуальный или выделенный сервер {#virtual_or_dedicated_servers_title}

Если вы знакомы с администратированием системы, или заинтересованы в изучении его, виртуальный или выделенный сервер даст вам полный контроль над средой продакшна вашего приложения.

### nginx и PHP-FPM

PHP, через встроенный в него менеджер процессов FastCGI(FPM), очень хорошо сочетается с [nginx](http://nginx.org), который является легковесным и высоко-производительным веб-сервером. Он использует меньше памяти, чем Apache и может лучше обрабатывать конкурентные запросы. Это особенно важно на виртуальном сервере, который не имеет много памяти. 

* [Подробнее о nginx](http://nginx.org)
* [Подробнее о PHP-FPM](http://php.net/manual/ru/install.fpm.php)
* [Подробнее об безопасной установке nginx и PHP-FPM](https://nealpoole.com/blog/2011/04/setting-up-php-fastcgi-and-nginx-dont-trust-the-tutorials-check-your-configuration/)

### Apache и PHP

PHP и Apache имеют длинную совместную историю. Apache 
PHP and Apache have a long history together. Apache is wildly configurable and has many available [modules](http://httpd.apache.org/docs/2.4/mod/) to extend functionality. It is a popular choice for shared servers and an easy setup for PHP frameworks and open source apps like WordPress. Unfortunately, Apache uses more resources than nginx by default and cannot handle as many visitors at the same time.

Apache has several possible configurations for running PHP. The most common and easiest to setup is the [prefork MPM](http://httpd.apache.org/docs/2.4/mod/prefork.html) with mod_php5. While it isn't the most memory efficient, it is the simplest to get working and to use. This is probably the best choice if you don't want to dig too deeply into the server administration aspects.  Note that if you use mod_php5 you MUST use the prefork MPM.

Alternatively, if you want to squeeze more performance and stability out of Apache then you can take advantage of the same FPM system as nginx and run the [worker MPM](http://httpd.apache.org/docs/2.4/mod/worker.html) or [event MPM](http://httpd.apache.org/docs/2.4/mod/event.html) with mod_fastcgi or mod_fcgid. This configuration will be significantly more memory efficient and much faster but it is more work to set up.

* [Read more on Apache](http://httpd.apache.org/)
* [Read more on Multi-Processing Modules](http://httpd.apache.org/docs/2.4/mod/mpm_common.html)
* [Read more on mod_fastcgi](http://www.fastcgi.com/mod_fastcgi/docs/mod_fastcgi.html)
* [Read more on mod_fcgid](http://httpd.apache.org/mod_fcgid/)

---
title: Установка на Mac
isChild: true
---

## Установка на Mac

OSX идёт вместе с PHP, но в основном, его версия отстает от последней стабильной. Lion поставляется с PHP версии 5.3.6, а Mountain Lion с версией 5.3.10.

Вы можете обновить PHP на вашем OSX через несколько [пакетных мэнеджеров][mac-package-managers], с рекомендованным [php-osx by Liip][php-osx-downloads].

Другой вариант [скомпилировать самостоятельно][mac-compile], в этом случае вы должны убедиться, что у вас установлен Xcode или его аналог от Apple ["Инструменты Командной Строки для Xcode"][apple-developer], который можно загрузить с Apple's Mac Developer Center.

Для полного набора "всё-в-одном", включающего PHP, веб-сервер Apache и СУБД MySQL с хорошим GUI, попробуйте [MAMP][mamp-downloads].

[mac-package-managers]: http://www.php.net/manual/ru/install.macosx.packages.php
[mac-compile]: http://www.php.net/manual/ru/install.macosx.compile.php
[xcode-gcc-substitution]: https://github.com/kennethreitz/osx-gcc-installer
[apple-developer]: https://developer.apple.com/downloads
[mamp-downloads]: http://www.mamp.info/en/downloads/index.html
[php-osx-downloads]: http://php-osx.liip.ch/

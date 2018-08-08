# Общие вопросы

## В чём разница между Z-machine и Glulx?

Это два формата файлов, в которые можно компилировать игры на Информе. Более старая, классическая Z-machine поддерживает размер файла игры до 256 Кб (формат .z5) или 512 Кб (формат .z8) и 16 цветов. Glulx — более современная 32-битная система, поддерживающая файлы размером до 4 Гб и расширенные мультимедийные возможности. Компилятор **inform** умеет компилировать игры в любом из форматов.

В английской версии Информа библиотека единая, но в русской версии пришлось разнести её на два отдельных проекта.

* Glulx: <https://github.com/yandexx/rinform-glulx>
* Z-machine: <https://bitbucket.org/yandexx/rinform/>

Начиная с версии **0.9** Русского Информа Glulx считается стабильной и рекомендуемой версией. Разработку стоит вести под неё. Версия для Z-машины считается вторичной.

Glulx имеет следующие преимущества:

* мультимедиа-фичи: картинки, звук, ссылки.
* расширенные возможности типографики.
* возможность разделять окно на произвольные области.
* полная поддержка UTF-8 как в исходниках, так и в готовых играх.
* файлы игр до 4 гигабайт.

Известное ограничение: в онлайн-версии Glulx (Quixe) нельзя в коде игры задавать цвета или размер шрифтов, кроме глобальных настроек через .css.

## Какие плееры открывают игры на Информе?

* Glulx (файлы **.ulx** и **.gblorb**): [Windows Git](http://www.davidkinder.co.uk/glulxe.html), [Windows Glulxe](http://www.davidkinder.co.uk/glulxe.html), [Lectrote](https://github.com/erkyrath/lectrote), а также онлайн.
* Z-machine (файлы **.z5**, **.z8** и **.zblorb**): [Windows Frotz](http://www.davidkinder.co.uk/frotz.html), [Lectrote](https://github.com/erkyrath/lectrote), [fizmo](https://fizmo.spellbreaker.org/), а также онлайн через [Parchment](https://iplayif.com/).
* На Android плеер [Fabularium](https://play.google.com/store/apps/details?id=com.luxlunae.fabularium) поддерживает все существующие форматы.

## Как опубликовать игру онлайн?

Чтобы запустить произвольную игру в Parchment, нужно указать параметром для сайта **iplayif.com** путь к файлу игры, уже залитому на какой-нибудь сервер. Например: <https://iplayif.com/?story=https://rinform.org/games/photopia/PhotopiaR.z8>

Очень просто и разместить игру на своём собственном сайте, даже статическом, т.к. Parchment работает полностью на клиентском JavaScript. Достаточно [скачать](https://github.com/curiousdannii/parchment) и разместить у себя на сервере файлы: 

* index.html,
* lib/parchment.min.js,
* lib/parchment.min.css,
* lib/jquery.min.js
* lib/zvm.min.js

и отредактировать index.html. В .css файле можно поменять шрифты, цвета и прочее, на что хватит вашей фантазии. Несколько примеров: [Винтер](http://pavlenko.biz/winter/), [Delightful Wallpaper](http://eblong.com/zarf/zweb/wallpaper/), [Dreamhold](http://eblong.com/zarf/zweb/dreamhold/).

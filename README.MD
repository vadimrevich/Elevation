Elevation
=========

Набор макросов и дополнительных программ и пакетов для повышения привилегий программ, запускаемых в учётной записи. Основные программы из данного пакета добавляют в контекстное меню папки проводника пункты (на английском языке) «Запустить командную строку», «Запустить командную строку как администратор», «Запустить командную строку с системными привилегиями», а также те же пункты для запуска PowerShell.

Внимание! Данные пункты меню имеют эффект, если только учётная запись имеет права локального администратора. Если у Вас учётная запись с пониженными привилегиями, сначала либо смените учётную запись, либо войдите в неё с консоли командой RunAs.

Внимание! Данный инсталлятор оптимизирован под установку дополнительного модуля SysInternals, необходимого для запуска некоторых макросов, с помощью менеджера пакетов Chocolatey. По умолчанию пакет SysInternals устанавливается совсем в другое место, и после установки пакета Evolution этой версии возможно появление ошибки. Поэтому устанавливайте и обновляйте пакет SysInternals исключительно в менеджере пакетов chocolatey командой:

> `choco install -y sysinternals`

Описание составных частей пакета
================================
Смотрите файл descript.ion в каталоге Elevation и комментарии в файлах макросов.

Инсталляция пакета
==================
1. Скачайте ZIP файл с данного сайта и распакуйте его;
2. Скопируйте Весь каталог Elevation в корень диска C:\;
3. Перейдите в каталог C:\Elevation;
4. Запустите файл InstallAllPowerToys.cmd и следуйте командам установщика (как правило, нужно всегда нажимать клавишу «Y»).

Вместо пунктов 1-3 можно просто запустить "тихий установщик" пакетов, дважды щёлкнув левой клавишей мыши на файле Exponenta-Plugin\Elevation.SFX.exe

История изменений
=================
Second Commit
* Немного изменена структура пакета, с тем чтобы он лучше собирался программами автоматической инсталляции.
* Добавлен файл автоматической регистрации каталога установки в оболочке Windows. Это сделано специально для организации плагина Exponenta.
* Добавлена автоматическая "тихая" установка программного пакета.

Initial Commit
* Подготовлен пакет, отличающийся от оригинальной версии наличием исправлений в коде и поддержкой менеджера пакетов Chocolatey.
* Теперь код частично оптимизирован под Windows 10 (оригинальный пакет был разработан под Windows Vista)
* Добавлен макрос для запуска командной строки из терминала в текущем каталоге от имени суперпользователя, даже если его учётная запись заблокирована Windows. Учётная запись должна иметь права локального администратора.
* В качестве бонуса в дистрибутив добавлены пакеты BLcm, CopyIP, cports, ele, fab, HostEditor, PortScan, PortScanner, touch.
* В качестве бонуса в пакет добавлены примеры макросов для запуска и остановки основных служб Windows, отвечающих за удалённый доступ к компьютеру, серверов Интернета, основных сетевых служб, а также макросы для выгрузки Skype и основных программ обмена сообщениями.

Лицензия и авторские права
==========================

Данный пакет распространяется под лицензией GNU GPL v.2 (смотри файл лицензии). Авторские права на пакеты принадлежат их создателям.

Дополнительно
=============
Для создания файлов для «тихой усановки» пакетов программ автор использует следующие дополнительные программы и пакеты:
1. Архиватор 7Zip. Установить его можно из менеджера пакетов «Chocolatey» командой:
`choco install -y 7zip.installl 7zip 7zip.portable`
2. Сторонний, неофициальный пакет 7z.SFX.Builder, позволяющий создавать пакеты с «тихой распаковкой» программ. Ссылки: [rsload.net](<https://rsload.net/soft/cleaner-disk/11772-7z-sfx-builder.html>) (login: rsload.net password: rsload.net) [sourceforge.net](<https://sourceforge.net/projects/s-zipsfxbuilder/>)

Полезные ссылки
===============

* Менеджер пакетов <a href="http://chocolatey.org/" target="_blank">chocolatey</a>.
* Статья «<a href="http://www.outsidethebox.ms/12219/" target="_blank">Как открывать файлы из контекстного меню с полными правами</a>».
* Программа <a href="https://www.nirsoft.net/utils/nircmd.html" target="_blank">NirCmd.exe</a>.
* Программа <a href="http://winreview.ru/obnovlenie-ele-1-0-1-utility-dlya-eskalacii-privilegij-otkrytogo-okna-komandoj-stroki/" target="_blank">Ele</a>.
* Основной дистрибутив программы <a href="https://technet.microsoft.com/ru-ru/library/2008.06.elevation.aspx" target="_blank">Elevation PowerToys</a>.
* Модифицированный вариант <a href="http://www.outsidethebox.ms/blog/wp-content/uploads/files/CMDasAdmin.zip" target="_blank">этих программ</a>.
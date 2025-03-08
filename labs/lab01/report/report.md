---
## Front matter
title: "Лабараторная работа №1"
subtitle: "Отчет"
author: "Славинский Владислав Вадимович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

# Задание

Установка Linux на Virtualbox
Установка операционной системы
Обновления
Повышение комфорта работы
Автоматическое обновление
Отключение SELinux
Настройка раскладки клавиатуры
Установка имени пользователя и названия хоста
Установка программного обеспечения для создания документации
Контрольные вопросы

# Выполнение лабораторной работы

Добавление образа в VirtualBox (рис. [-@fig:001])

![Установка Linux](image/1.png){#fig:001 width=70%}

Устанавливаем Fedora (рис. [-@fig:002])

![Установка Fedora](image/2.png){#fig:002 width=70%}

Установка средств разработки и обновление всех пакетов (рис. [-@fig:003])

![Средства разработки](image/3.png){#fig:003 width=70%}

Команда для удобства работы в консоли, и введем команду для автоматических обновлений (рис. [-@fig:004])

![Консоль,обновления](image/4.png){#fig:004 width=70%}

Запустим таймер (рис. [-@fig:005])

![Запуск таймера](image/5.png){#fig:005 width=70%}

Отключаем SELinux (рис. [-@fig:006])

![Отключение SELinux](image/6.png){#fig:006 width=70%}

Отредактировал файл с конфигом для настройки клавиатуры  (рис. [-@fig:007])

![Настройка клавиатуры](image/7.png){#fig:007 width=70%}

Задал имя пользователя и хоста (рис. [-@fig:008])

![Имя пользователя и хоста](image/8.png){#fig:008 width=70%}

Далее установим pandoc (рис. [-@fig:009])

![Установка pandoc](image/9.png){#fig:009 width=70%}
 
Распаковал файлы pandoc-crossref и перекинул их в нужную папку (рис. [-@fig:010])

![Установка pandoc](image/10.png){#fig:010 width=70%}

Установка texlive (рис. [-@fig:011])

![Установка texlive](image/10.png){#fig:011 width=70%}

# Выводы

В ходе выполнения лабораторной работы я приобрел практические навыки по установке операционной системы на виртуальную машину. 

# Ответы на контрольные вопросы

1. Учётная запись пользователя в операционной системе содержит следующую информацию: логин, пароль, uid, домашний каталог, настройки окружнения, права доступа к файлам и каталогам

2. Команды терминала

    Получение справки по команде:
Команда: man <команда>
Пример: man ls (открывает справку по команде ls)

    Перемещение по файловой системе:
Команда: cd <путь>
Пример: cd /home/user/Documents (переход в каталог Documents)

    Просмотр содержимого каталога:
Команда: ls
Пример: ls -l (выводит содержимое каталога в длинном формате)

    Определение объёма каталога:
Команда: du
Пример: du -sh /home/user/Documents (показывает общий размер каталога Documents)

    Создание / удаление каталогов / файлов:
Создание каталога: mkdir <имя_каталога>
 Пример: mkdir new_folder (создаёт новый каталог new_folder)
Удаление каталога: rmdir <имя_каталога>
Пример: rmdir old_folder (удаляет каталог old_folder)
Создание файла: touch <имя_файла>
Пример: touch new_file.txt (создаёт новый файл new_file.txt)
Удаление файла: rm <имя_файла>
Пример: rm old_file.txt (удаляет файл old_file.txt)

Задание определённых прав на файл / каталог:
Команда: chmod
Пример: chmod 755 script.sh (устанавливает права на выполнение для владельца и чтение/выполнение для группы и остальных)

    Просмотр истории команд: Команда: history
Пример: history | grep <команда> (поиск в истории команд)


3. Файловая система — это способ организации и хранения данных на носителе информации. Она определяет, как данные хранятся, именуются и извлекаются. Примеры файловых систем: FAT32, NTFS, ext4.
1.FAT32 Широко используется на USB-накопителях и в системах с низкими требованиями к безопасности.
2.NTFS Используется в Windows.Поддерживает большие файлы, права доступа, шифрование и другие функции.
3.ext4-Широко используется в Linux.Поддерживает большие объемы данных и улучшенную производительность.


4. Как посмотреть, какие файловые системы подмонтированы в ОС?
 Команда: df -h Пример: df -h (выводит список всех подмонтированных файловых систем с их размерами и использованием)


5. Как удалить зависший процесс?
Для удаления зависшего процесса можно использовать команду kill или killall:
Найдите PID (идентификатор процесса) с помощью команды ps или top.
Пример: ps aux | grep <имя_процесса>
Удалите процесс:
Команда: kill <PID>
Пример: kill 1234 (где 1234 — это PID зависшего процесса)
Если процесс не реагирует, можно использовать более жесткий вариант:
Команда: kill -9 <PID>
Пример: kill -9 1234 (принудительное завершение процесса)


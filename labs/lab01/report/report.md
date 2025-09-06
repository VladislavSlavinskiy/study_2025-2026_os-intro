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

Установить и настроить OC Rocky.

# Выполнение лабораторной работы

Добавление образа Rocky в VirtualBox. (рис. [-@fig:001])

![Добавление образа](image/1.png){#fig:001 width=70%}

Устанавливаем Rocky (рис. [-@fig:002])

![Установка Rocky ](image/2.png){#fig:002 width=70%}

Установка английского языка интерфейса (рис. [-@fig:003])

![Язык интерфейса](image/3.png){#fig:003 width=70%}

Настройка установки: выбор программ (рис. [-@fig:004])

![Выбор программ](image/4.png){#fig:004 width=70%}

Отключим KDUMP (рис. [-@fig:005])

![Отключение KDUMP](image/5.png){#fig:005 width=70%}

Включим сетевое соединение и в качестве имени узла укажем имя пользователя.(рис. [-@fig:006])

![Установка сети и имени узла](image/6.png){#fig:006 width=70%}

Установим пароль для root(рис. [-@fig:007])

![Установка root пароля](image/7.png){#fig:007 width=70%}

Установим пароль для пользователя с правами администратора (рис. [-@fig:008])

![Установка пароля](image/8.png){#fig:008 width=70%}

Запуск установки OC (рис. [-@fig:009])

![Установка OC](image/9.png){#fig:009 width=70%}
 
Подключим образ диска дополнений гостевой OC и запустим его.  (рис. [-@fig:010])

![Подключение и запуск образа диска дополнений](image/10.png){#fig:010 width=70%}

Посмотрим вывод команды dmesg | less (рис. [-@fig:011])

![Вывод команды](image/11.png){#fig:011 width=70%}

С помощью этой команды мы можем посмотреть различную информацию, давайте посмотрим версию Ядра Linux. (рис. [-@fig:012])

![Версия Ядра Linux](image/12.png){#fig:012 width=70%}

Посмотрим частоту процессора. (рис. [-@fig:013])

![Частота процессора](image/13.png){#fig:013 width=70%}

Посмотрим модель процессора. (рис. [-@fig:014])

![Модель процессора](image/14.png){#fig:014 width=70%}

Посмотрим объем доступной оперативной памяти. (рис. [-@fig:015])

![Объем ОЗУ](image/15.png){#fig:015 width=70%}

Выведем тип обнаруженного гипервизора (KVM). (рис. [-@fig:016])

![Тип гипервизора](image/16.png){#fig:016 width=70%}

Посмотрим тип файловой системы (Mounting V5 Filesystem). (рис. [-@fig:017])

![Тип файловой системы](image/17.png){#fig:017 width=70%}

# Выводы

В ходе выполнения лабораторной работы я приобрел практические навыки по установке операционной системы Rocky на виртауальную машину. 


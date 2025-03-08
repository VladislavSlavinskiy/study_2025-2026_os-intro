---
## Front matter
title: "Лабараторная работа №4"
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

Получение навыков правильной работы с репозиториями git.

# Задание


Установка программного обеспечения
Установка git-flow
Установка Node.js
Настройка Node.js
Общепринятые коммиты
Практический сценарий использования git
Создание репозитория git
Работа с репозиторием git

# Выполнение лабораторной работы

Установка Gitflow (рис. [-@fig:001])

![Установка Gitflow](image/1.png){#fig:001 width=70%}

Установка Node.js (рис. [-@fig:002])

![Установка Node.js](image/2.png){#fig:002 width=70%}

Настройка Node.js (рис. [-@fig:003])

![Настройка](image/3.png){#fig:003 width=70%}

Подключение репозитория к Github (рис. [-@fig:004])

![Подключение репозитория](image/4.png){#fig:004 width=70%}

Редактируем конфиг общепринятых коммитов (рис. [-@fig:005])

![Конфиг](image/5.png){#fig:005 width=70%}

Инициализируем Gitflow (рис. [-@fig:006])

![Инициализация](image/6.png){#fig:006 width=70%}

Загрузил весь репозиторий в хранилище  (рис. [-@fig:007])

![Загрузка](image/7.png){#fig:007 width=70%}

Создание релиза с версией 1.0.0 и создание журнала изменений. (рис. [-@fig:008])

![Создание релиза и журнала изменений](image/8.png){#fig:008 width=70%}

Залил релизную ветку в основную ветку и отправил на данные на гит (рис. [-@fig:009])

![Отправка данных](image/9.png){#fig:009 width=70%}
 
Создание ветки для функциональности (рис. [-@fig:010])

![Создание ветки](image/10.png){#fig:010 width=70%}

Создадим релиз с версией 1.2.3(рис. [-@fig:011])

![Создание релиза](image/11.png){#fig:011 width=70%}

Создание журнала изменений и добавление журнала в индекс(рис. [-@fig:012])

![Создание журнала](image/12.png){#fig:012 width=70%}

Зальем релизную ветку в основную ветку.Отправим данные на Github. Создадим релиз на github с комментарием из журнала изменений (рис. [-@fig:013])

![Создание журнала](image/13.png){#fig:013 width=70%}

# Выводы

В ходе выполнения лабораторной работы я приобрел навыки правильной работы с репозиториями git. 




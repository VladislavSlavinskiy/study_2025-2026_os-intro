---
## Front matter
title: "Лабараторная работа №2"
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

Изучить Идеологию и применение средств контроля версий. Освоить умения по работе с git.

# Задание

Установка git
Установка gh
Базовая настройка git
Создание ключей ssh и pgp
Настройка github
Добавление pgp ключа в github
Настройка автоматический подписей коммитов git
Настройка gh
Сознание репозитория курса на основе шаблона
Настройка каталога курса
Контрольные вопросы

# Выполнение лабораторной работы

В начале установим git (рис. [-@fig:001])

![Установка git](image/1.png){#fig:001 width=70%}

Установим gh (рис. [-@fig:002])

![Установка gh](image/2.png){#fig:002 width=70%}

Задал имя и email своего репозитория (рис. [-@fig:003])

![Данные репозитория](image/3.png){#fig:003 width=70%}

Настройка utf-8, задал имя начальной ветки, ввел параметр autocrlf и safecrlf (рис. [-@fig:004])

![utf-8,autocrlf,safecrlf](image/4.png){#fig:004 width=70%}

Создал ключи ssh (рис. [-@fig:005])

![Создание ключей](image/5.png){#fig:005 width=70%}

Добавление ssh ключа на git (рис. [-@fig:006])

![Добавление ключа](image/6.png){#fig:006 width=70%}

Настройка автоматических подписей коммитов git (рис. [-@fig:007])

![Подписи](image/7.png){#fig:007 width=70%}

Настройка gh (рис. [-@fig:008])

![Настройка gh](image/8.png){#fig:008 width=70%}

Произвел операции над сознанием рабочего пространства (рис. [-@fig:009])

![Сознание рабочего пространства](image/9.png){#fig:009 width=70%}
 
Настроил каталог курса, удалил лишние файлы, создал необходимые каталоги и отправил их на сервер (рис. [-@fig:010])

![Настройка каталога курса](image/10.png){#fig:010 width=70%}

# Выводы

В ходе выполнения лабораторной работы был установлен git, его настройка, были созданы ключи для авторизации и подписи. Был создан репозиторий. 

# Ответы на контрольные вопросы

1. VCS-это инструменты для отслеживания изменений в файлах и управления проектами, позволяющие сохранять версии и координировать работу.

2. Хранилище-место хранения файлов и их истории.
Commit-сохранение изменений в хранилище.
История-последовательность всех коммитов, отражающая изменения в проекте.
Рабочая копия-локальная версия файлов, с которой работает разработчик.

3. Централизованные: имеют одно центральное хранилище, к которому подключаются все пользователи.
Децентрализованные каждый разработчик имеет полную копию хранилища, включая всю историю.

4. Создание хранилища.
Внесение изменений в рабочую копию.
Выполнение команды commit для сохранения изменений.
Просмотр истории изменений.

5. Клонирование удаленного репозитория.
Внесение изменений и создание коммитов.
Синхронизация с удаленным репозиторием (pull/push).
Разрешение конфликтов, если они возникают.

6. Отслеживание изменений в коде.
Восстановление предыдущих версий.
Совместная работа над проектами.
Управление ветвями.

7. git init: инициализация нового репозитория.
git clone: клонирование удаленного репозитория.
git add: добавление изменений в индекс.
git commit: сохранение изменений в хранилище.
git push: отправка изменений в удаленный репозиторий.
git pull: получение изменений из удаленного репозитория.
git branch: управление ветвями.
git merge: слияние ветвей.

8. Локальный репозиторий: git init, git add ., git commit -m "Initial commit".
Удаленный репозиторий: git clone <url>, git push origin main.

9. Ветви позволяют создавать параллельные линии разработки, что упрощает работу над новыми функциями или исправлениями, не затрагивая основную ветвь

10. Файлы можно игнорировать с помощью файла .gitignore, чтобы исключить их из коммитов (например, временные файлы, конфигурации среды), что помогает поддерживать чистоту репозитория.

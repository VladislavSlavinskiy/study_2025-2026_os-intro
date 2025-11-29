---
## Front matter
lang: ru-RU
title: Фильтр пакетов
subtitle: Часть 1
author:
  - Славинский В.В.
institute:
  - Российский университет дружбы народов, Москва, Россия Россия
date: 29 ноября 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Информация

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Славинский Владислав Вадимович
  * Студент
  * Российский университет дружбы народов
  * [1132246169@pfur.ru]

:::
::: {.column width="30%"}

# Вводная часть

## Определение текущей зоны по умолчанию


В терминале получим права администратора, определим текущую зону по умолчанию, введя: firewall-cmd --get-default-zone.

![sc1](./image/1.png)

## Определение доступных зон

Определим доступные зоны с помощью firewall-cmd --get-zones.

![sc2](./image/2.png)

## Доступные службы

Посмотрим службы, доступные на компьютере, используя firewall-cmd --get-services.

![sc3](./image/3.png)

## Доступные службы в текущей зоне

Определим доступные службы в текущей зоне: firewall-cmd --list-services. 

![sc4](./image/4.png)

## Сравнение вывода информации

Сравним результаты вывода информации при использовании команды firewall-cmd --list-all и команды firewall-cmd --list-all --zone=public. Вывод у нас одинаковый, так как первая команда показывает текущую зону по умолчанию, по умолчанию у нас зона public, а вторая команда показывает конкретно зону public

![sc5](./image/5.png)

## Добавление VNC в брандмауэр

Добавим сервер VNC в конфигурацию брандмауэра: firewall-cmd --add-service=vnc-server

![sc6](./image/6.png)

## Проверка

Проверим, добавился ли vnc-server в конфигурацию: firewall-cmd --list-all.

![sc7](./image/7.png)

## Перезапуск службы

Перезапустим службу firewalld: systemctl restart firewalld.

![sc8](./image/8.png)

## Проверка

Проверим, есть ли vnc-server в конфигурации: firewall-cmd --list-all. vnc-server пропал, потому что служба была добавлена только во временную конфигурацию.

![sc9](./image/9.png)

## Добавление службы в постоянную

Добавим службу vnc-server ещё раз, но на этот раз сделаем её постоянной, используя команду firewall-cmd --add-service=vnc-server --permanent.

![sc10](./image/10.png)

## Проверка

Проверим наличие vnc-server в конфигурации: firewall-cmd --list-all.

![sc11](./image/11.png)

## Перезагрузка конфигурации

Перезагрузим конфигурацию firewalld и просмотрим конфигурацию времени выполнения: firewall-cmd --reload, firewall-cmd --list-all.

![sc12](./image/12.png)

## Добавление порта

Добавим в конфигурацию межсетевого экрана порт 2022 протокола TCP: firewall-cmd --add-port=2022/tcp --permanent. Потом перезагрузим конфигурацию firewalld и проверим, что порт добавлен в конфигурацию.

![sc13](./image/13.png)

## Запуск интерфейса GUI

Откроем терминал и под учётной записью своего пользователя запустим интерфейс GUI firewall-config: firewall-config

![sc14](./image/14.png)

## Изменение параметров

Далее в конфигурации выберем permanent. В зоне public выберем http ftp и https. Во вкладке ports введем 2022 и добавим протокол udp.

![sc15](./image/15.png)

## Вывод информации

В окне терминала введем firewall-cmd --list-all

![sc16](./image/16.png)

## Перезагрузка

Перезагрузим конфигурацию firewalld: firewall-cmd --reload. И потом опять выведем список сервисов. Как видим, они добавились.

![sc17](./image/17.png)

## Создание конфигурации

Создадим конфигурацию межсетевого экрана, которая позволяет получить доступ к службам telnet, imap, pop3, smtp. Через командную строку добавим telnet.

![sc18](./image/18.png)

## Добавление сервисов в графическом интерфейсе

Далее делаем в графическом интерфейса GUI.

![sc19](./image/19.png)

## Перезагрузка конфигурации и проверка


Перезагружаем конфигурацию firewalld и смотрим список доступных сервисов, как видим, все добавилось.

![sc20](./image/20.png)

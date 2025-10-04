---
## Front matter
lang: ru-RU
title: Управление системными службами
subtitle: Часть 1
author:
  - Славинский В.В.
institute:
  - Российский университет дружбы народов, Москва, Россия Россия
date: 4 октября 2025

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

## Переход в режим суперпользователя

В консоли перейдем в режим работы суперпользователя, используя команду su -.

![sc1](./image/1.png)

## Проверка статуса службы

Проверим статус службы Very Secure FTP с помощью команды systemctl status vsftpd. Служба отключена, так как она не установлена

![sc2](./image/2.png)

## Установка vsftp

Установим службу Very Secure FTP: dnf -y install vsftpd.

![sc3](./image/3.png)

## Запуск vsftp

Запустим службу Very Secure FTP: systemctl start vsftpd.

![sc4](./image/4.png)

## Проверка статуса службы

Проверим статус службы Very Secure FTP с помощью команды systemctl status vsftpd.

![sc5](./image/5.png)

## Добавление в автозапуск

У нас служба работает, но у нас она не будет работать при автоматическом запуске операционной системы, давайте её добавим в автоматический запуск с помощью команды systemctl enable vsftpd. И как видим, служба добавилась в автозапуск.

![sc6](./image/6.png)

## Отключение службы

Теперь удалим службу из автозапуска через команду systemctl disable vsftpd. Теперь служба удалилась из автозапуска.

![sc7](./image/7.png)

## Вывод символических ссылок

Выведем на экран символические ссылки, ответственные за запуск различных сервисов: ls /etc/systemd/system/multi-user.target.wants. В данном случае мы не видим vsftpd.service.

![sc8](./image/8.png)

## Вывод символических ссылок после добавления vsftp в автозапуск

Теперь снова добавим vsftp в автозапуск и проверим, появился ли vsftpd.service. Как видим, у нас vsftpd появился.

![sc9](./image/9.png)

## Проверка статуса службы

Снова проверим статус службы Very Secure FTP. У нас служба будет включена после перезапуска системы.

![sc10](./image/10.png)

## Вывод списка зависимостей юнита

Выведем на экран список зависимостей юнита: systemctl list-dependencies vsftpd.

![sc11](./image/11.png)

## Вывод списка юнитов, которые зависят от данного типа

Выведем на экран список юнитов, которые зависят от данного юнита: systemctl list-dependencies vsftpd --reverse. 

![sc12](./image/12.png)

## Установка iptables

Дальше установим iptables: dnf -y install iptables\*.

![sc13](./image/13.png)

## Проверка статуса firewalld

Проверим статус firewalld: systemctl status firewalld.

![sc14](./image/14.png)

## Проверка статуса iptables

Проверим статус iptables: systemctl status iptables. Здесь мы видим, что служба инактивна, и не запущена а автозапуске.

![sc15](./image/15.png)

## Запуск firewalld и iptables

Попробуем запустить firewalld и iptables: systemctl start firewalld,systemctl start iptables.

![sc16](./image/16.png)

## Проверка статуса firewalld

Посмотрим статус firewalld. firewalld у нас теперь не запущена.

![sc17](./image/17.png)

## Проверка статуса iptables

Посмотрим статус iptables. И тут уже понятно, что одна служба диактивируется, а другая включается, поскольку iptables запустилась.

![sc18](./image/18.png)

## Ввод команды для анализа ошибок

Введем cat /usr/lib/systemd/system/firewalld.service, чтобы посмотреть ошибки. И вот мы видим, с чем конфликтует служба firewalld.

![sc19](./image/19.png)

## Ввод команды для анализа ошибок

Введем то же самое, только для iptables: cat /usr/lib/systemd/system/iptables.service. Но тут, мы не видим никаких ошибок.

![sc20](./image/20.png)

## Выгрузка iptables и загрузка firewalld

Выгрузим службу iptables (на всякий случай, чтобы убедиться, что данная служба не загружена в систему): systemctl stop iptables, и загрзуим службу firewalld systemctl start firewalld.

![sc21](./image/21.png)

## Блокировка запуска iptables

Заблокируем запуск iptables, введя команду systemctl mask iptables.

![sc22](./image/22.png)

## Запуск itpables

Теперь попробуем запустить iptables. Видим , что у нас ошибка, так как мы эту службу замаскировали.

![sc23](./image/23.png)

## Попытка добавления iptables в автозапуск

Попробуем добавить iptables в автозапуск, но сервис будет неактивен, а статус загрузки отобразился как замаскированный.

![sc24](./image/24.png)

## Список целей, которые можно изолировать

Дальше перейдем  каталог systemd и найдите список всех целей, которые можно изолировать:cd /usr/lib/systemd/system, grep Isolate *.target.

![sc25](./image/25.png)

## Переключение операционной системы в режим восстановления

Переключим операционную систему в режим восстановления: systemctl isolate rescue.target.

![sc26](./image/26.png)

## Перезапуск операционной системы с изменениями

Перезапустим операционную систему следующим образом: systemctl isolate reboot.target.

![sc27](./image/27.png)

## Вывод цели по умолчанию

Теперь вводим команду systemctl get-default, чтобы узнать установленную по умолчанию цель. Видим, что запускается система по умолчанию в графическом режиме.

![sc28](./image/28.png)

## Запуск текстового режима

Для запуска по умолчанию текстового режима введём systemctl set-default multi-user.target и перезагружаем.

![sc29](./image/29.png)

## Возвращение на графический режим

Чтобы нам обратно вернуться в графический режим, нужно перейти на root и ввести команду systemctl set-default graphical.target.

![sc30](./image/30.png)

## Запуск в графическом режиме

Перезагружаем и видим, мы снова в графическом режиме.

![sc31](./image/31.png)


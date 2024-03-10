---
## Front matter
title: "Отчет по лабораторной работе №5"
subtitle: "Дисциплина: Операционные системы"
author: "Иванов Сергей Владимирович"

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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Целью лабораторной работы является настроить рабочую среду и научиться пользоваться менеджером паролей.

# Выполнение лабораторной работы

Установим менеджер паролей pass. (рис. 1, 2).

![Установка менеджера паролей](image/1.png){#fig:001 width=70%}

![Установка менеджера паролей](image/2.png){#fig:002 width=70%}

Просмотрим список ключей GPG, видим что он есть (рис. 3).

![Список ключей](image/3.png){#fig:003 width=70%}

Инициализируем хранилище (рис. 4).

![Инициализация хранилища](image/4.png){#fig:004 width=70%}

Создадим структуру git (рис. 5). 

![Структура git](image/5.png){#fig:005 width=70%}

Так же создадим репозиторий (рис. 6). 

![Создание репозитория](image/6.png){#fig:006 width=70%}

Зададим адрес репозитория на хостинге (рис. 7). 

![Задаем адрес](image/7.png){#fig:007 width=70%}

Синхронизируем репозиторий. (рис. 8).

![Синхронизация репозитория](image/8.png){#fig:008 width=70%}

Так же можем вручную закоммитить и выложить изменения (рис. 9).

![Синхронизация вручную](image/9.png){#fig:009 width=70%}

Проверить статус синхронизации можно командой (рис. 10).

![Статус](image/10.png){#fig:010 width=70%}

Включим репозиторий Corp. (рис. 11). 

![Corp](image/11.png){#fig:011 width=70%}

Устанавливаем программу, обеспечивающую интерфейс native messaging. (рис. 12). 

![native messaging](image/12.png){#fig:012 width=70%}

Подключим плагин для Firefox (рис. 13). 

![Подключение плагина](image/13.png){#fig:013 width=70%}

Добавим новый пароль, отобразим пароль для указанного имени файла, заменим существующий пароль (рис. 14). 

![Добавление пароля](image/14.png){#fig:014 width=70%}

Установим дополнительное программное обеспечение (рис. 15). 

![Установка](image/15.png){#fig:015 width=70%}

Установим шрифты (рис. 16).

![Установка шрифтов](image/16.png){#fig:016 width=70%}

Установим бинарный файл. Скрипт определяет архитектуру процессора и операционную систему и скачивает необходимый файл (рис. 17).

![Установка бинарного файла](image/17.png){#fig:017 width=70%}

Создадим свой репозиторий для конфигурационных файлов на основе шаблона (рис. 18).

![Создание репозитория](image/18.png){#fig:018 width=70%}

Инициализируем chezmoi с репозиторием dotfiles (рис. 19).

![Инициализация chezmoi](image/19.png){#fig:019 width=70%}

Проверим какие изменения внесёт chezmoi в домашний каталог (рис. 20).

![Проверка изменений](image/20.png){#fig:020 width=70%}

Соглашаемся с изменениями (рис. 21).

![Применение изменений](image/21.png){#fig:021 width=70%}

Проделываем тоже самое на второй машине. Установим свои dotfiles на новую машину с помощью одной команды (рис. 22).

![Вторая машина](image/22.png){#fig:022 width=70%}

Извлечем последние изменения из своего репозитория и посмотрим, что изменится, фактически не применяя изменения (рис. 23).

![Извлекаем изменения](image/23.png){#fig:023 width=70%}

Включаем автоматическое фиксирование и отправление изменений в репозиторий (рис. 24).

![Автоматическое отправление](image/24.png){#fig:024 width=70%}

# Выводы

В результате выполнения лабораторной работы мы настроили рабочую среду и научились пользоваться менеджером паролей.


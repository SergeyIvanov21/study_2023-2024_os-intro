---
## Front matter
title: "Отчет по индивидуальному проекту №3"
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

Продолжить выполнение индивидуального проекта. Заполнить данные о себе на сайте в соответствии с требованиями.

# Задание

Добавить к сайту достижения.

Список достижений.
Добавить информацию о навыках (Skills).
Добавить информацию об опыте (Experience).
Добавить информацию о достижениях (Accomplishments).
Сделать пост по прошедшей неделе.
Добавить пост на тему по выбору

# Выполнение 

Запускаем локальный сайт (рис. 1).

![Запуск локального сайта](image/1.png){#fig:001 width=70%}

Находим файл index.md который нужно редактировать (рис. 2).

![Краткая биография](image/2.png){#fig:002 width=70%}

Добавляем информацию о навыках (рис. 3).

![Добавление навыков](image/3.png){#fig:003 width=70%}

Посмотрим как это выглядит на локальном сайте (рис. 4).

![Локальный сайт](image/4.png){#fig:004 width=70%}

Добавляем информацию об опыте (рис. 5). 

![Добавление опыта](image/5.png){#fig:005 width=70%}

Посмотрим как это выглядит на локальном сайте (рис. 6).

![Локальный сайт](image/6.png){#fig:006 width=70%}

Добавляем информацию о достижения (рис. 7). 

![Добавление достижений](image/7.png){#fig:007 width=70%}

Посмотрим как это выглядит на локальном сайте (рис. 8).

![Локальный сайт](image/8.png){#fig:008 width=70%}

Напишем пост о прошедшей неделе. Создаем папку и пишем пост в файл index.md (рис. 9).

![Пишем пост](image/9.png){#fig:009 width=70%}

Посмотрим пост на локальном сайте. (рис. 10).

![Локальный сайт](image/10.png){#fig:010 width=70%}

Напишем пост на тему по выбору. Я выбрал Markdown. Аналогично создаем папку и пишем пост в файл index.md (рис. 11).

![Пост на тему Markdown](image/11.png){#fig:011 width=70%}

Посмотрим пост на локальном сайте. (рис. 12).

![Локальный сайт](image/12.png){#fig:012 width=70%}

Отправляем файлы папки blog на GitHub. (рис. 13). 

![Отправляем blog на git](image/13.png){#fig:013 width=70%}

Отправляем файлы папки public на GitHub (рис. 14).

![Отправляем public на git](image/14.png){#fig:014 width=70%}

# Выводы

В результате выполнения данной работы я продолжил выполнение индивидуального проекта. Заполнил данные о себе на сайте в соответствии с требованиями.


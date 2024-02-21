---
## Front matter
lang: ru-RU
title: Лабораторная работа № 1
subtitle: Операционные системы
author:
  - Иванов Сергей Владимирович, НПИбд-01-23
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 17 февраля 2024

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'

 ## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
---

## Цель работы

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.

## Задание

1. Создать виртуальную машину
2. Установить ОС на виртуальную машину
3. Настроить систему

# Выполнение работы

## Скачиваем дистрибутив

Необходимо скачать дистрибутив Fedora Sway 39
https://fedoraproject.org/spins/sway/download/index.html 

![Скачивание дистрибутива](image/1.jpg){#fig:001 width=70%}

## Создание виртуальной машины

Укажем имя машины и подключим наш скачанный образ Linux Sway. 

![Создание виртуальной машины](image/2.jpg){#fig:002 width=70%}

## Создание виртуальной машины

Укажем объём памяти и количество виртуальных процессоров. Я указал 4096 мб оперативной памяти и 2 ЦП. Далее укажем обьем диска 80гб. 

![Указываем характеристики](image/3.jpg){#fig:003 width=70%}

![Виртуальный жесткий диск](image/4.jpg){#fig:004 width=70%}

## Запуск виртуальной машины

Запускаем виртуальную машину.

![Запуск виртуальной машины](image/5.jpg){#fig:005 width=70%}

## Установка ОС

Выбираем диск для установки операционной системы, создаем учетную запись и начинаем установку.

![Установка ОС](image/6.jpg){#fig:006 width=70%}

## Обновление пакетов

Обновим все пакеты командой 
- ‘dnf –y update’

![Обновление пакетов](image/8.jpg){#fig:008 width=70%}

## Установка tmux и mc

Установим программы для удобства работы в консоли командой 
- ‘dnf install tmux mc’

![Установка tmux](image/9.jpg){#fig:009 width=70%}

## Автоматическое обновление

Установим программное обеспечение воспользовавшись командой 
- ‘dnf install dnf-automatic’

![Установка ПО для автоматического обновления](image/10.jpg){#fig:010 width=70%}

## Автоматическое обновление

Запустим таймер командой 
- ‘systemctl enable --now dnf-automatic.timer’

![Запуск таймера](image/11.jpg){#fig:011 width=70%}

## Отключение SELinux

Необходимо отключить SELinux.
- В файле /etc/selinux/config заменим значение SELINUX=enforcing на значение SELINUX=permissive.

![Отключение SELinux](image/12.jpg){#fig:012 width=70%}

## Установка драйвера для VirtualBox

- Войдём в ОС под заданной нами при установке учётной записи. 
- Нажмем комбинацию Win+Enter для запуска терминала. 
- Запустим  tmux, переключимся на роль супер-пользователя. 
- Установим средства разработки ‘dnf -y group install "Development Tools"’

![Установка средств разработки](image/13.jpg){#fig:013 width=70%}

## Установка драйвера для VirtualBox

Установим пакет DKMS используя команду  
- ‘dnf -y install dkms’

![Установка DKMS](image/14.jpg){#fig:014 width=70%}

## Установка драйвера для VirtualBox

- В меню виртуальной машины подключим образ диска дополнений гостевой ОС. 
- Подмонтируем диск командой ‘mount /dev/sr0 /media’

![Подключение Диска дополнений гостевой ОС.](image/15.jpg){#fig:015 width=70%}

![Подмонтируем диск](image/16.jpg){#fig:016 width=70%}

## Установка драйвера для VirtualBox

После чего установим драйвера 
- ‘/media/VBoxLinuxAdditions.run’

![Установка драйвера](image/17.jpg){#fig:017 width=70%}

## Настройка раскладки клавиатуры

- Запустим tmux 
- Переключимся на роль супер-пользователя. 
- Создадим конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf. 
- Отредактируем его.

![Редактирование конфиг. файла](image/18.jpg){#fig:018 width=70%}

## Настройка раскладки клавиатуры

Отредактируем конфигурационный файл /etc/X11/xorg.conf.d/00-keyboard.conf

![Редактируем файл](image/19.jpg){#fig:019 width=70%}

## Установка имени хоста

Необходимо установить имя хоста 
- ‘hostnamectl set-hostname username’. 
- Проверим что имя хоста установлено верно, после чего перезагрузим систему.

![Изменение имени хоста.](image/20.jpg){#fig:020 width=70%}

## Подключение общей папки

Подключим общую папку.

![Общая папка](image/21.jpg){#fig:021 width=70%}

## Установка pandoc

- Запустим терминальный мультиплексор tmux 
- Установим pandoc с помощью менеджера пакетов ‘dnf -y install pandoc’

![Установка pandoc](image/22.jpg){#fig:022 width=70%}

## Установка pandoc-crossref

Скачаем необходимую версию pandoc-crossref (https://github.com/lierdakil/pandoc-crossref/releases). Распакуем архив и поместим их в каталог /usr/local/bin.

![Установка pandoc-crossref](image/23.jpg){#fig:023 width=70%}

## Установка TeXLive

‘dnf -y install texlive-scheme-full’

![Установка TeXlive](image/24.jpg){#fig:024 width=70%}

# Домашнее задание

## Версия ядра Linux (Linux version).

Чтобы посмотреть версию ядра, можно воспользоваться командой dmesg | grep -i ‘linux version’. 
Версия ядра: 6.7.4-200.

![Версия ядра](image/25.jpg){#fig:025 width=70%}

## Частота процессора (Detected Mhz processor).

Частоту процессора можно узнать командой dmesg | grep -I “MHz”.
Частота процессора: 2688.004 MHz.

![Частота процессора](image/26.jpg){#fig:026 width=70%}

## Модель процессора (CPU0).

Модель процессора можно посмотреть командой cat /proc/cpuinfo | grep “model name”.

![Модель процессора](image/27.jpg){#fig:027 width=70%}

## Объем доступной оперативной памяти (Memory available).

Объём доступной оперативной памяти можно посмотреть командой free -m.
В моём случае: 
Всего – 3894 Мб.
Используется – 779 Мб.
Свободно – 3115 Мб.

![Объем оперативной памяти](image/28.jpg){#fig:028 width=70%}

## Тип обнаруженного гипервизора (Hypervisor detected).

Тип обнаруженного гипервизора можно посмотреть командой dmesg | grep -I “hypervisor detected”.
В моём случае: KVM.

![Тип гипервизора](image/29.jpg){#fig:029 width=70%}

## Тип файловой системы корневого раздела.

Тип файловой системы корневого раздела можно посмотреть командой findmnt.
Тип файловой системы корневого раздела: ext4. 

![Тип файловой системы](image/30.jpg){#fig:030 width=70%}

## Последовательность монтирования файловых систем.

Последовательность монтирования файловых систем можно посмотреть командой dmesg | grep -i “mount”

![Последовательность монтирования файловых систем](image/31.jpg){#fig:031 width=70%}

# Вывод

## Вывод 

В ходе работы были приобретены практические навыки установки виртуальной машины и операционной системы на виртуальную машину, а также настройки минимально необходимых для дальнейшей работы сервисов.

## Список литературы{.unnumbered}

::: {#refs}
1. Dash, P. Getting Started with Oracle VM VirtualBox / P. Dash. – Packt Publishing Ltd, 2013. – 86 сс.
2. Colvin, H. VirtualBox: An Ultimate Guide Book on Virtualization with VirtualBox. VirtualBox / H. Colvin. – CreateSpace Independent Publishing Platform, 2015. – 70 сс.
3. Vugt, S. van. Red Hat RHCSA/RHCE 7 cert guide : Red Hat Enterprise Linux 7 (EX200 and EX300) : Certification Guide. Red Hat RHCSA/RHCE 7 cert guide / S. van Vugt. – Pearson IT Certification, 2016. – 1008 сс.
4. Робачевский, А. Операционная система UNIX / А. Робачевский, С. Немнюгин, О. Стесик. – 2-е изд. – Санкт-Петербург : БХВ-Петербург, 2010. – 656 сс.
5. Немет, Э. Unix и Linux: руководство системного администратора. Unix и Linux / Э. Немет, Г. Снайдер, Т.Р. Хейн, Б. Уэйли. – 4-е изд. – Вильямс, 2014. – 1312 сс.
6. Колисниченко, Д.Н. Самоучитель системного администратора Linux : Системный администратор / Д.Н. Колисниченко. – Санкт-Петербург : БХВ-Петербург, 2011. – 544 сс.
7. Robbins, A. Bash Pocket Reference / A. Robbins. – O’Reilly Media, 2016. – 156 сс.

:::







 

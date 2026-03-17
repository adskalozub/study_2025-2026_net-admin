---
## Front matter
title: "Отчёт о лабораторной работе"
subtitle: "Лабораторная работа №7"
author: "Скалозуб Александр"

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

Получить навыки работы с журналами мониторинга различных событий в системе.

# Задание

Поработать с журналом мониторинга событий в системе

# Выполнение лабораторной работы

![](SC57.png){#fig:001 width=70%}

Рис 1. смотрим логи

![](SC58.png){#fig:002 width=70%}

Рис 2. Смотрим логи

![](SC59.png){#fig:003 width=70%}

Рис 3. запускаем httpd и смотрим логи

![](SC60.png){#fig:004 width=70%}

Рис 4. Создаём файл конфигурации и редактируем его

![](SC61.png){#fig:005 width=70%}

Рис 5. перезапускаем httpd

![](SC62.png){#fig:006 width=70%}

Рис 6. создаем файл конфигурации и редактируем его

![](SC63.png){#fig:007 width=70%}

Рис 7. перезапускаем службу и смотрим логи Рис

![](SC64.png){#fig:008 width=70%}

Рис 8. Смотрим логи

![](SC65.png){#fig:009 width=70%}

Рис 9. Смотрим логи

![](SC66.png){#fig:010 width=70%}

Рис 10. Смотрим логи

![](SC67.png){#fig:011 width=70%}

Рис 11. Создаем файл, настраиваем его и выводи логи

# Вывод

Научились работать с логами

# Ответы на контрольные вопросы

1. /etc/rsyslog.conf или /etc/rsyslog.d/  

2. /etc/rsyslog.conf или файлы в /etc/rsyslog.d/, связанные с auth или authpriv  

3. Зависит от настроек, обычно — несколько секунд или минут, сразу после триггера ротации.  

4. *.info /var/log/messages.info  

5. tail -f /var/log/messages или journalctl -f  

6. journalctl _PID=1 --since "09:00" --until "15:00"  

7. journalctl --boot или journalctl -b  

8. Использовать systemctl restart systemd-journald после настройки /etc/systemd/journald.conf.
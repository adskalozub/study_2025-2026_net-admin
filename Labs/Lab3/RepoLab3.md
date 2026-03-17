---
## Front matter
title: "Отчёт о лабораторной работе"
subtitle: "Лабораторная работа №3"
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

Получение навыков настройки базовых и специальных прав доступа для групп пользователей в операционной системе типа Linux.

# Задание

Получить базовые навыми для работы с правами доступа для пользователей

# Выполнение лабораторной работы

![](SC13.png){#fig:001 width=70%}

Рис 1. проверяем директорию data

![](SC14.png){#fig:002 width=70%}

Рис 2. выдаем разрешения main и third

![](SC15.png){#fig:003 width=70%}

Рис 3. создаем и проверяем файлы

![](SC16.png){#fig:004 width=70%}

Рис 4. делаем тоже самое

![](SC17.png){#fig:005 width=70%}

Рис 5. управление разрешениями

![](SC18.png){#fig:006 width=70%}

Рис 6. создаем файл и смотрим разрешения

![](SC19.png){#fig:007 width=70%}

Рис 7. выдаем разрешения main и thrid

![](SC20.png){#fig:008 width=70%}

Рис 8. пробуем удалить файл защищенный от удаления

# Выводы

Научились управлять правами доступа

# Ответы на контрольные вопросы

1. chown <пользователь>:<группа> <файл>  

2. find / -user <имя_пользователя>  

3. chmod 770 /data  

4. chmod +x <файл>  

5. chmod g+s <каталог> или chmod o-g <каталог> 

6. Использовать umask, чтобы ограничить права при создании файлов. umask 027 — владельцы и группа получат rwxr-x--- права.  

7. setfacl -m g:<группа>:r-- <файл или каталог> Чтобы установить для всех файлов в каталоге: setfacl -R -m g:<группа>:r-- .  

8. chmod g+s <каталог>  

9. umask 077 — новые файлы имеют права 600 (для файлов) или 700 (для каталогов).

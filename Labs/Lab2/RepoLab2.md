---
## Front matter
title: "Отчёт о лабораторной работе"
subtitle: "Лабораторная работа №2"
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

Получить представление о работе с учётными записями пользователей и группами пользователей в операционной системе типа Linux.

# Задание

Поработать с учетными записями

# Ход выполнение лабораторной работы

![](SC1.PNG){#fig:001 width=70%}

Рис 1. Определяем пользователя и его принадлежности 

![](SC2.PNG){#fig:002 width=70%}

Рис 2. определяем принадлежность админа 

![](SC3.PNG){#fig:003 width=70%}

Рис 3. открываем файл sudoers в редакторе vi и изменяем параметр  %wheel

![](SC4.PNG){#fig:004 width=70%}

Рис 4. создаем пользователя alice и даем ему пароль в принадлежности wheel

![](SC5.PNG){#fig:005 width=70%}

Рис 5. Создаем пользователя bob и делаем те же манипуляции 

![](SC6.PNG){#fig:006 width=70%}

Рис 6. проверяем create\_home на параметр yes

![](SC7.PNG){#fig:007 width=70%}

Рис 7. проверяем usergroups\_enab на значение no и меняем его на no

![](SC8.PNG){#fig:008 width=70%}

Рис 8. создаем директории

![](SC9.PNG){#fig:009 width=70%}

Рис 9. работаем с имеющимися пользователями

![](SC10.PNG){#fig:010 width=70%}

Рис 10. Работаем с пользователями 

![](SC11.PNG){#fig:011 width=70%}

Рис 11. Работаем с группами

# Выводы

Мы научились работать с группами и пользователями в linux

# Ответы на контрольные вопросы

1. Команды для получения информации об идентификаторе и группах пользователя:  
id (например, `id alice`)  

2. UID пользователя root: 0.  
Команда для узнать UID: id -u или id alice.  

3. su — переключение пользователя, требует пароль.  
sudo — выполнение команды с правами другого пользователя (обычно администратора), требует пароль.  

4. Параметры sudo определяются в файле /etc/sudoers.  

5. Для безопасного изменения конфигурации sudo: использовать команду visudo.  

6. Пользователь должен быть членом группы sudo или wheel (зависит от дистрибутива).  

7. Файлы/каталоги: /etc/passwd (для параметров учётных записей), /etc/shadow (секреты паролей).  
Примеры настроек: shell по умолчанию, домашний каталог.  

8. Информация о группах хранится в /etc/group.  
Для пользователя alice: строка вида alice:x:1001 (группа основная).  

9. Команды: chage, passwd --status, passwd --expire.  

10. Используйте команду vipw или vigr — для безопасного редактирования /etc/passwd и /etc/group. Они обеспечивают предотвращение повреждения файлов и проверку синтаксиса.

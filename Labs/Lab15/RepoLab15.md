---
## Front matter
title: "Отчёт о лабораторной работе"
subtitle: "Лабораторная работа №15"
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

Получить навыки управления логическими томами.

# Задание

Научится управлять логическими томами.

# Выполнение лабораторной работы

![](SC140.png){#fig:001 width=70%}

![](SC141.png){#fig:002 width=70%}

![](SC142.png){#fig:003 width=70%}

![](SC143.png){#fig:004 width=70%}

![](SC144.png){#fig:005 width=70%}

![](SC145.png){#fig:006 width=70%}

![](SC146.png){#fig:007 width=70%}

![](SC147.png){#fig:008 width=70%}

![](SC148.png){#fig:009 width=70%}

![](SC149.png){#fig:010 width=70%}

![](SC150.png){#fig:011 width=70%}

# Выводы

Научились управлять томами

# Ответы на контрольные вопросы

1 RAID

2 vgcreate vggroup /dev/sdb3 -- physicalextentsize 4M

3 pvs и vgs

4 pvadd /dev/sdd

5 lvcreate -L 6M -n lvvol1 vgname

6 lvextend -L +100M /dev/vgname/lvvol1

7 vgextend на физический диск

8 ключ -r

9 lvs

10 fsck /dev/vgdata/lvdata
---
## Front matter
title: "Лабораторная работа №4"
author: "Кочан Лина Романовна"

## Generic options
lang: ru-Ru\
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

##Pdf output format
toc: true 
toc-depth: 2
lof: true
lot: true
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt

polyglossia-lang:
   name: russian
   options:
   - spelling=modern
   - babelshorhands=true
polyglossia-otherlangs:
   name: english

babel-lang: russian
babel-otherlangs: english
mainfont: Times New Roman
sansfont: Arial
monofont: Courier New
mathfont: Times New Roman

biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
    - parentracker=true
    - backend=biber
    - hyperref=auto
    - language=auto
    - autolang=other*
    - citestyle=gost-numeric

igureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"

indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} 
  - \floatplacement{figure}{H} 
---

# 1. Цель работы

Освоение продвинутых методов работы с git-репозиториями и механизмами создания релизов.

# 2. Задание

- Выполнить работу для тестового репозитория.
- Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional commits.

# 3. Теоретическое введение

Gitflow Workflow, опубликованная Винсентом Дриссеном, предполагает строгую модель ветвления с учетом выпуска проекта и включает создание отдельной ветки для исправления ошибок в рабочей среде. Семантическое версионирование (SemVer) задается в формате МАЖОРНАЯ.МИНОРНАЯ.ПАТЧ, где мажорная версия увеличивается при несовместимых изменениях API, минорная — при добавлении новой обратно совместимой функциональности, а патч-версия — при обратно совместимых исправлениях. Conventional Commits — это соглашение о структуре сообщений коммитов, которое тесно связано с SemVer и регламентирует основные типы коммитов.



# 4. Выполнение лабораторной работы

Устанавливаю nodejs, пакетный менеджер для него pnpm и gitflow. (рис. 1)

![Установка необходимого ПО](4.1.png){#fig:001 width=70%}

Устанавливаю через pnpm commitizen и  standard-changelog. (рис. 2) 

![Установка через pnpm](4.2.png){#fig:001 width=70%}

Создаю новый репозиторий и делаю первый коммит. (рис. 3)

![Создание нового репозитория](4.3.png){#fig:001 width=70%}

Инициализирую и конфигурирую общепринятые коммиты в созданной директиории через редактирование файла package.json. (рис. 4)

![Конфигурация package.json](4.4.png){#fig:001 width=70%}

Делаю снимок изменений, создаю коммит и отправляю на удаленный репозиторий. (рис. 5)

![Отправка коммита на github](4.5.png){#fig:001 width=70%}


Инициализурю в репозитории git flow и создаю 1 релиз в только что созданной ветке develop. (рис. 6)

![Использование git-flow](4.6.png){#fig:001 width=70%}

Создаю список изменений через standard-changelog, заканчиваю релиз и выгружаю на удаленный репозиторий изменения. (рис. 7)

![Создание списка, выгрузка изменений](4.7.png){#fig:001 width=70%}

Инициализирую ветку feature для работы над новой функциональностью, готовлю релиз и загружаю на github. (рис. 8)

![Итоговая выгрузка](4.8.png){#fig:001 width=70%}


# 5. Выводы

В результате выполнения лабораторной работы были освоены навыки корректной работы с git-репозиториями.

# Список литературы{.unnumbered}

::: {#refs}
:::

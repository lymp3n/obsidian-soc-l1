---
tags:
  - soc
  - hub
status_danya: 🔴 To-Do
status_vadim: 🔴 To-Do
status_andrey: 🔴 To-Do
module: Модуль 2
---
# Без названия

> **📊 Прогресс команды:**
> Даня: `INPUT[inlineSelect(option(🔴 To-Do), option(🟡 In Progress), option(🟢 Done)):status_danya]` | Вадим: `INPUT[inlineSelect(option(🔴 To-Do), option(🟡 In Progress), option(🟢 Done)):status_vadim]` | Андрей: `INPUT[inlineSelect(option(🔴 To-Do), option(🟡 In Progress), option(🟢 Done)):status_andrey]`

## 📖 Обзор темы
Здесь описывается общая логика модуля. 
Например: "Основной протокол для раздачи IP-адресов — это [[DHCP]], а за доменные имена отвечает [[DNS]]. Главная уязвимость тут — это [[ARP Spoofing]]." 
*(При вводе двойных скобок Obsidian предложит создать или привязать атомарную заметку)*

## 🗂️ Карточки в этом разделе
*(Этот код автоматически подтянет статусы всех атомарных заметок, которые ты упомянул в тексте выше)*

```dataview
TABLE status_danya AS "Даня", status_vadim AS "Вадим", status_andrey AS "Андрей"
FROM outgoing([[Архитектура и безопасность Linux.md]])
WHERE contains(tags, "atomic")
```

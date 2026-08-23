---
tags: [soc, hub]
module: <% tp.system.suggester(["Модуль 1", "Модуль 2", "Модуль 3", "Модуль 4"], ["Модуль 1", "Модуль 2", "Модуль 3", "Модуль 4"]) %>
---
<!-- Статусы: 🔴 To-Do | 🟡 In Progress | 🟢 Done | ➖ N/A -->
# <% tp.file.title %>

## 📖 Обзор темы
Краткое описание связей между атомарными заметками.

## 🗂️ Карточки в этом разделе
```dataview
TABLE status_danya AS "Даня", status_vadim AS "Вадим", status_andrey AS "Андрей"
FROM outgoing([[<% tp.file.title %>]])
WHERE contains(tags, "atomic")
```

# 🛡️ Учебный Дашборд: SOC Analyst L1 (Даня, Вадим, Андрей)

## 🟡 В процессе (Кто-то изучает прямо сейчас)
```dataview
TABLE type AS "Тип", status_danya AS "Даня", status_vadim AS "Вадим", status_andrey AS "Андрей"
FROM "База знаний (Справочник)"
WHERE status_danya = "🟡 In Progress" OR status_vadim = "🟡 In Progress" OR status_andrey = "🟡 In Progress"
SORT date DESC
```

## ⏳ Отстающие (Ждем остальных)
```dataview
TABLE type AS "Тип", status_danya AS "Даня", status_vadim AS "Вадим", status_andrey AS "Андрей"
FROM "База знаний (Справочник)"
WHERE (status_danya = "🟢 Done" OR status_vadim = "🟢 Done" OR status_andrey = "🟢 Done") 
  AND (status_danya = "🔴 To-Do" OR status_vadim = "🔴 To-Do" OR status_andrey = "🔴 To-Do" OR status_danya = "🟡 In Progress" OR status_vadim = "🟡 In Progress" OR status_andrey = "🟡 In Progress")
SORT file.name ASC
```

## 🔴 Общая очередь (Никто не начинал)
```dataview
TABLE type AS "Тип"
FROM "База знаний (Справочник)"
WHERE status_danya = "🔴 To-Do" AND status_vadim = "🔴 To-Do" AND status_andrey = "🔴 To-Do"
SORT file.name ASC
```

## 🟢 Полностью изучено (Закрыто всей командой)
```dataview
TABLE type AS "Тип", date AS "Дата"
FROM "0_База знаний (Справочник)"
WHERE status_danya = "🟢 Done" AND status_vadim = "🟢 Done" AND status_andrey = "🟢 Done"
SORT date DESC
```

# 🛡️ Учебный Дашборд: SOC Analyst L1 

## 🟡 В процессе изучения (Уроки)
```dataview
TABLE module AS "Модуль", status_danya AS "Даня", status_vadim AS "Вадим", status_andrey AS "Андрей"
WHERE contains(tags, "hub") AND (status_danya = "🟡 In Progress" OR status_vadim = "🟡 In Progress" OR status_andrey = "🟡 In Progress")
SORT file.name ASC
```

## ⏳ Отстающие (Ждем остальных)
```dataview
TABLE module AS "Модуль", status_danya AS "Даня", status_vadim AS "Вадим", status_andrey AS "Андрей"
WHERE contains(tags, "hub") 
  AND (status_danya = "🟢 Done" OR status_vadim = "🟢 Done" OR status_andrey = "🟢 Done") 
  AND (status_danya != "🟢 Done" OR status_vadim != "🟢 Done" OR status_andrey != "🟢 Done")
SORT file.name ASC
```

## 🔴 Очередь тем (Никто не начинал)
```dataview
TABLE module AS "Модуль"
WHERE contains(tags, "hub") AND status_danya = "🔴 To-Do" AND status_vadim = "🔴 To-Do" AND status_andrey = "🔴 To-Do"
SORT file.name ASC
```

## 🟢 Полностью пройдено (Закрыто всей командой)
```dataview
TABLE module AS "Модуль"
WHERE contains(tags, "hub") AND status_danya = "🟢 Done" AND status_vadim = "🟢 Done" AND status_andrey = "🟢 Done"
SORT file.name ASC
```
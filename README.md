# Скрипты для взлома электронного дневника

Эти скрипты позволяют менять оценки учеников, убирать замечания и добавлять похвальные комментарии от учителей.

Проект дневника: [e-diary](https://github.com/devmanorg/e-diary)


## Запуск

- Скачайте файл `scripts.py` в папку с проектом дневника.
- Из папки с проектом запустите команду:
```
python manage.py shell
from scripts import *
```

## Внесение изменений внутри shell
- Изменить отрицательные оценки на 5:
```
schoolkid = get_schoolkid("Имя ученика")
fix_marks(schoolkid)
``` 
- Убрать замечания:
```
schoolkid = get_schoolkid("Имя ученика")
remove_chastisements(schoolkid)
```

- Добавить похвальный комментарий от учителя. Комментарий добавится к последнему уроку.
```
create_commendation("Имя ученика", "Название предмета")
```

## Цели проекта

Код написан в учебных целях — это урок в курсе по Python и веб-разработке на сайте [Devman](https://dvmn.org).
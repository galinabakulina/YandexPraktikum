## Аналитика в Яндекс.Дзене

Почти всё рабочее время в Яндекс.Дзене занимает анализ пользовательского взаимодействия с карточками статей.

Принимается решение, что процесс пора автоматизировать этот процесс - сделать дашборд.

Дашборд будет основываться на пайплайне, который будет брать данные из таблицы, в которых хранятся сырые данные, трансформировать данные и укладывать их в агрегирующую таблицу. Пайплайн будет разработан для вас дата-инженерами.

План исследования:

1) Краткое ТЗ
2) Подключение к БД
3) SQL-запрос
4) Выгрузка данных
5) Ссылка на дашборд
6) Ссылка на презентацию
7) Общие выводы

Используемые библиотеки

```python
from datetime import datetime

import pandas as pd
from sqlalchemy import create_engine
```
## Исследование объявлений о продаже квартир

В распоряжении аналитика данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. Необходимо исследовать, какие факторы влияют на рыночную стоимость объектов недвижимости. Работа с выбросами позволит построить *автоматизированную систему*: она отследит аномалии и мошенническую деятельность. 

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем:
- total_images / количество фотографий в объявлении;
- last_price / стоимость объекта недвижимости;
- total_area / общая площадь;
- first_day_exposition / датапубликации объявления; 
- rooms	/ количетсов комнат;
- ceiling_height / высота потолков;	
- floors_total / этажность дома;
- living_area / жилая площадь;	
- floor / этаж;	
- is_apartment / квартира или апартаменты;
- studio / ялвяется ли квартира студией;
- open_plan / свободная планировка или нет;
- kitchen_area / площадь кухни;
- balcony / количество балконов;
- locality_name / название населенного пункта;
- days_exposition / сколько дней продается недвижимость.


Вторые — получены автоматически на основе картографических данных:
- airports_nearest / расстояни до ближайшего аэропорта;
- cityCenters_nearest / расстояние до центра;
- parks_around3000 / количество парков в радиусе 3 км;
- parks_nearest / расстояние до ближайшего парка;
- ponds_around3000 / количество водоёмов в радиусе 3 км;
- ponds_nearest / расстояние до ближайшего водоёма.

План исследования: 

1) Ознакомление с данными.

2) Предобработка данных: работа с пропусками, преобразованеи типов данных, выявление аномальных значений параметров, добавление новых признаков.

3) Исследовательский анализ данных.

4) Общие выводы.

Используемые библиотеки

```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np

from pandas.plotting import scatter_matrix

import warnings
warnings.filterwarnings("ignore")
```
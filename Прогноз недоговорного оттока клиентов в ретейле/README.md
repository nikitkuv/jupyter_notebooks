# Прогноз оттока клиентов в ретейле
Представлены данные сети продуктовых гипермаркетов по клиентам, ассортименту, магазинам и транзакциям, сделланых клиентами в этих магазинах.

**Статус:** Завершен

**Цель:** вывести методологию определения отточных клиентов и построить модель вероятности оттока клиентов по выведенной методологии.

**Используемый стек:** lifetimes, sklearn, statistics, imblearn, pandas, numpy, matplotlib, seaborn;

**Целевой признак модели**: churn - ушел ли клиент или нет - yet to calculate.

**Выводы:**
 - Были использованы два подходя для решения задачи прогноза оттока клиентов во внеконтрактовых условиях: BG/NBD модель и алгоритмы классического машинного обучения с использованием результатов BG/NBD.
 - В ходе анализа признаков модели BG/NBD были выделены интересные закономерности, среди которых факт, что в последние 8 месяцев не было притока новых клиентов, несмотря на довольно высокую лояльность старых. Предлагается разработать улучшенную маркетинговую программу для привлечения новых клиентов и увеличения их базы.
 - Классические модели с использованием RFM признаков показывают около идеальные результаты, что вероятно связано с утечкой данных, т.к. целевой признак расчитывался на основе вероятности, что клиент останется, которая в свою очередь была расчитана из тех самых RFM признаков.
 - Классические модели без RFM признаков чуть хуже, но в целом также показывают хорошие результаты, особенно сильно увеличивают метрики таких моделей созданные на основе дат транзакций признаки.
 - Несмотря на это, классические алгоритмы также показали свою силу, поэтому рекомендуется использовать модель BG/NBD в комбинации с обученными моделями классических методов машинного обучения.

## Описание данных
Данные состоят из следующих файлов-таблиц:

- `transactions.parquet` — чековые данные;
    - chq_id - ID of transaction
    - plant - ID of store
    - chq_date - Date of transaction
    - chq_position - Position of material in transaction
    - client_id - ID of client
    - material - ID of material (item)
    - sales_count - Count of item in the check position
    - sales_sum - Amount in rubles by the check position
    - is_promo - Fact of selling the position of the check for promo
    
- `clients.csv` — справочник клиентов;
    - client_id - ID of client
    - gender - Gender of client
    - city - City where the client makes the most purchases
    - birthyear - Year of birth
    
- `materials.csv` — справочник товаров;
    - material - ID of material (item)
    - hier_level_1 - 1st level of items hierarchy
    - hier_level_2 - 2nd level of items hierarchy
    - hier_level_3 - 3rd level of items hierarchy
    - hier_level_4 - 4th level of items hierarchy
    - vendor - Vendor of item
    - is_private_label - Own brand mark
    - is_alco - Sign of alcoholic beverages
    
- `plants.csv` — справочник магазинов;
    - plant - ID of store
    - plant_type - Type of store (HM - hypermarket, SM - supermarket)
    - city - City where the store located

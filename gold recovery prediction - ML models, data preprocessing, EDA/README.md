# Восстановление золота из руды
Предоставлены данные с параметрами добычи и очистки золотосодержащей руды от компании, занимающейся разработкой решения для эффективной работы промышленных предприятий.

**Цель:** подготовить прототип модели машинного обучения, предсказывающую коэффициент восстановления золота из золотосодержащей руды.

Целевой признак: коэффициент восстановления золота в черновом и финальном концентратах (rougher.output.recovery + final.output.recovery).

Модель поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.

## Описание данных
Технологический процесс:
  - Rougher feed — исходное сырье
  - Rougher additions (или reagent additions) — флотационные реагенты: Xanthate, Sulphate, Depressant
  - Xanthate — ксантогенат (промотер, или активатор флотации);
  - Sulphate — сульфат (на данном производстве сульфид натрия);
  - Depressant — депрессант (силикат натрия).
  - Rougher process (англ. «грубый процесс») — флотация
  - Rougher tails — отвальные хвосты
  - Float banks — флотационная установка
  - Cleaner process — очистка
  - Rougher Au — черновой концентрат золота
  - Final Au — финальный концентрат золота
 
Параметры этапов:
  - air amount — объём воздуха
  - fluid levels — уровень жидкости
  - feed size — размер гранул сырья
  - feed rate — скорость подачи
 
Наименование признаков:
Наименование признаков должно быть такое: этап.тип_параметра.название_параметра
Пример: rougher.input.feed_ag

Возможные значения для блока этап:
  - rougher — флотация
  - primary_cleaner — первичная очистка
  - secondary_cleaner — вторичная очистка
  - final — финальные характеристики

Возможные значения для блока тип_параметра:
  - input — параметры сырья
  - output — параметры продукта
  - state — параметры, характеризующие текущее состояние этапа
  - calculation — расчётные характеристики
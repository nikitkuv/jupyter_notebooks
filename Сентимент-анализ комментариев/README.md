# Сентимент-анализ комментариев
Представлен набор комментариев различных товаров с сайта интернет-магазина с разметкой о токсичности правок.

**Статус:** Завершен

**Цель:** Обучить модель классифицировать комментарии на позитивные и негативные.

**Используемый стек:** nltk, re, sklearn, imblearn, lightgbm, itertools, pandas, numpy, matplotlib, seaborn, tqdm;

**Требование от заказчика:** Постройте модель со значением метрики качества F1 не меньше 0.75.

**Выводы:**
  - Таким образом, лучший результат показала модель Логистической регрессии с использованием внутренней балансировки классов
  - Кроме того, результат выше заявленного значения показала модель Логистической регрессии с использованием техники SMOTE
  - Остальные модели показали значение метрики f1 ниже 0.75

## Описание данных
Столбец text содержит текст комментария, а toxic — целевой признак.

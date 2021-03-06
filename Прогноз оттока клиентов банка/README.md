# Прогноз оттока клиентов банка
Предоставлены исторические данные о поведении клиентов и расторжении договоров с банком. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

**Статус:** Завершен

**Цель:** нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет.

**Используемый стек:** imblearn, sklearn, pandas, numpy, matplotlib, seaborn, itertools;

Целевой признак модели: факт ухода клиента (Exited).

**Условие заказчика:** нужно довести F1-меру как минимум до значения 0.59.

**Выводы:**
  - На имеющихся данных протестированы 4 разных модели, подходящие для задачи бинарной классификации
  - На каждой из моделей были протестированы 3 разных метода борьбы с дисбалансом классов
  - Финальной моделью выбирается модель Random Forest с использованием весов для классов: f1 = 0.63

Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

## Описание данных
  - RowNumber — индекс строки в данных
  - CustomerId — уникальный идентификатор клиента
  - Surname — фамилия
  - CreditScore — кредитный рейтинг
  - Geography — страна проживания
  - Gender — пол
  - Age — возраст
  - Tenure — сколько лет человек является клиентом банка
  - Balance — баланс на счёте
  - NumOfProducts — количество продуктов банка, используемых клиентом
  - HasCrCard — наличие кредитной карты
  - IsActiveMember — активность клиента
  - EstimatedSalary — предполагаемая зарплата
  - Exited — факт ухода клиента

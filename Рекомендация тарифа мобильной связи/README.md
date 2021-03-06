# Рекомендация тарифов мобильной связи
Даны данные о поведении клиентов двух новых тарифов оператора мобильной связи - тарифы Ультра и Смарт. Компания выяснила, что многие клиенты пользуются архивными тарифами.

**Статус:** Завершен

**Цель:** нужно построить модель машинного обучения, способную проанализировать поведение клиентов и предложить пользователям новый тариф.

**Используемый стек:** sklearn, pandas, numpy, matplotlib, seaborn;

Целевой признак модели: тариф пользователя (признак is_ultra).

**Условие заказчика:** качество модели по accuracy должно быть не менее 0.75.

**Выводы:**
  - Каждая из лучших моделей была проверена на тестовой выборке, отложенной еще до обучения. Модель, показавшая лучший результат на тестовой выборке выбрана как финальная - RandomForestClassifier, accuracy по тестовой выборке = 0.8
  - Модель проверена на адекватность с использованием константной модели по преобладающему классу

## Описание данных
  - сalls — количество звонков
  - minutes — суммарная длительность звонков в минутах
  - messages — количество sms-сообщений
  - mb_used — израсходованный интернет-трафик в Мб
  - is_ultra — каким тарифом пользовался в течение месяца («Ультра» — 1, «Смарт» — 0)

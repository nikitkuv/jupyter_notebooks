# Анализ закономерностей успешности видеоигр
Рассматриваются исторические данные о продажах видеоигр, оценки пользователей и экспертов, жанры и платформы.

**Статус:** Завершен

**Цель**: Нужно выявить определяющие успешность игры закономерности. Это позволит сделать ставку на потенциально популярный продукт и спланировать рекламные кампании.

**Используемый стек:** pandas, numpy, matplotlib, seaborn, scipy, math

**Выводы:**
  - Сделать основной акцент на игры для платформ PS4 и XOne, жанров action, shooter, sports и role-playing и E и M рейтингов ESRB - для всех регионов, кроме Японии, и на игры для плаформы 3DS, жанров role-playing и action и T и E рейтингов ESRB - для Японии;
  - Дополнительно можно рассмотреть вариант с играми платформ PS3 и X360 тех же жанров и рейтингов для всех регионов, кроме Японии, и вариант с играми Playstation платформ PS3, PSV и PS4 тех же жанров и рейтингов для Японии;

## Описание данных
  - Name — название игры
  - Platform — платформа
  - Year_of_Release — год выпуска
  - Genre — жанр игры
  - NA_sales — продажи в Северной Америке (миллионы проданных копий)
  - EU_sales — продажи в Европе (миллионы проданных копий)
  - JP_sales — продажи в Японии (миллионы проданных копий)
  - Other_sales — продажи в других странах (миллионы проданных копий)
  - Critic_Score — оценка критиков (максимум 100)
  - User_Score — оценка пользователей (максимум 10)
  - Rating — рейтинг от организации ESRB (англ. Entertainment Software Rating Board). Эта ассоциация определяет рейтинг компьютерных игр и присваивает им подходящую возрастную категорию.

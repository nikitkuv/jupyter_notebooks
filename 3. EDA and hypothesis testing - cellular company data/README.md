# Exploratory data analysis and hypothesis testing

## Assessment of the most profitable tariff plan for cellular company
There is the dataset containing data about two tariff plans of cellular company including cellular data, data on SMS and web traffic data.

**Goal**: Assess and define the most profitable tariff plan in terms of revenue and which one should have bigger advertising dollars.

Data analysis will be done based on sample of clients from 2018 containing 500 users of the company and their data regarding how much data in different communication types (cellular, messages, web) they spend;

## Data description
  - Table users (information about users):
  - user_id — user id
  - first_name — user first name
  - last_name — user last name
  - age — age in years
  - reg_date — date of registration
  - churn_date — date of churn (if contains missing value then user used the plan on the moment of data collection)
  - city — user city
  - tariff — user plan
  - Table calls (data about calls):
  - id — call id
  - call_date — call date
  - duration — call duration in minutes
  - user_id — user id
  - Table messages (data about messages):
  - id — message id
  - message_date — message date
  - user_id — user id
  - Table internet (data about web sessions):
  - id — session id
  - mb_used — web traffic used in mb
  - session_date — session date
  - user_id — user id
  - Table tariffs (information about plans):
  - tariff_name — plan name
  - rub_monthly_fee — monthly subscription fee
  - minutes_included — free minutes included in the plan
  - messages_included — free messgaes included in the plan
  - mb_per_month_included — free web traffic amount included in the plan
  - rub_per_minute — price of a minute above free plan in rubles (for example, if plan has 100 free minutes and user spent 101 minutes then user will pay addition fee above the plan)
  - rub_per_message — price of a message above free plan in rubles
  - rub_per_gb — price of a gb above free plan in rubles (1 gb = 1024 mb)

*Comments on tariff plans:*

The cellular company rounds seconds to minutes and mb to gb:

- each call is rounded separately: even if it lasted 1 second it will be paid as per 1 minute;for web traffic single sessions are not counted: instead total monthly amount of - - web traffic is rounded ahead - if user spent 1025 mb then it will be paid as per 2 gb;

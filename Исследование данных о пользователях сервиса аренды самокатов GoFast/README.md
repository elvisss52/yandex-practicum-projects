# Исследование данных о пользователях сервиса аренды самокатов GoFast

## Описание проекта

Я аналитик популярного сервиса аренды самокатов GoFast. Мне передали данные о некоторых пользователях из нескольких городов, а также об их поездках. Проанализируем данные и проверим некоторые гипотезы, которые могут помочь бизнесу вырасти. Чтобы совершать поездки по городу, пользователи сервиса GoFast пользуются мобильным приложением.

Сервисом можно пользоваться:

- без подписки
    - абонентская плата отсутствует;
    - стоимость одной минуты поездки — 8 рублей;
    - стоимость старта (начала поездки) — 50 рублей;

- с подпиской Ultra
    - абонентская плата — 199 рублей в месяц;
    - стоимость одной минуты поездки — 6 рублей;
    - стоимость старта — бесплатно.
  
Для анализа нам предоставлены 3 таблицы.

## Описание данных

В основных данных есть информация о пользователях, их поездках и подписках. 

Пользователи — users_go.csv
- user_id - уникальный идентификатор пользователя
- name - имя пользователя
- age - возраст
- city - город
- subscription_type - тип подписки (free, ultra)
  
Поездки — rides_go.csv
- user_id - уникальный идентификатор пользователя
- distance - расстояние, которое пользователь проехал в текущей сессии (в метрах)
- duration - продолжительность сессии (в минутах) — время с того момента, как пользователь нажал кнопку «Начать поездку» до момента, как он нажал кнопку «Завершить поездку»
- date - дата совершения поездки

Подписки — subscriptions_go.csv
- subscription_type - тип подписки
- minute_price - стоимость одной минуты поездки по данной подписке
- start_ride_price - стоимость начала поездки
- subscription_fee - стоимость ежемесячного платежа

## Цели исследования

- ознакомиться с исходными данными;
- подготовить данные к анализу: проверить на наличие пропущенных значений и дубликатов;
- описать и визуализировать общую информацию о пользователях и поездках;
- объединить данные о пользователях, поездках и подписках в один датафрейм;
- рассчитать помесячную выручку по каждому пользователю;
- проверить предложенные гипотезы, которые могут улучшить работу бизнеса.

## Используемые библиотеки
*pandas, matplotlib, numpy, scipy*

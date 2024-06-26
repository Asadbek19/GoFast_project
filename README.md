# Статистический анализ данных #

Вы аналитик популярного сервиса аренды самокатов GoFast. Вам передали данные о некоторых пользователях из нескольких городов, а также об их поездках. Проанализируйте данные и проверьте некоторые гипотезы, которые могут помочь бизнесу вырасти.

Чтобы совершать поездки по городу, пользователи сервиса GoFast пользуются мобильным приложением. Сервисом можно пользоваться:
- без подписки
  - абонентская плата отсутствует;
  - стоимость одной минуты поездки — `8` рублей;
  - стоимость старта (начала поездки) — `50` рублей;
- с подпиской Ultra
  - абонентская плата — `199` рублей в месяц;
  - стоимость одной минуты поездки — `6` рублей;
  - стоимость старта — бесплатно.


**Цель исследования**

Проанализировать данные и проверить такие гипотезы как:
 1. Тратят ли пользователи с подпиской больше времени на поездки, чем пользователи без подписки.
 2. Не превышает ли среднее расстояние 3130 метров за одну поездку, у пользователей с подпиской, т.к. оптимальное с точки зрения износа самоката - 3130 метров. 
 3. Будет ли помесячная выручка от пользователей с подпиской по месяцам выше, чем выручка от пользователей без подписки.
 4. Какой тест понадобится для проверки гипотезы, чтобы узнать, снизилось ли количество обращений в техподдержку после обновления сервера, с которым взаимодействует мобильное приложение?
 
 **Ход исследования**

Данные о пользователях сервиса получу из файла `/datasets/users_go.csv`, данные о поездках из файла `/datasets/rides_go.csv` и данные о подписках из файла `/datasets/subscriptions_go.csv`. О качестве данных в файлах пока не известно и по этой причине, перед проведением исследований, необходимо провести обзор данных.

Я проверю данные на пропущенные значения, ошибки и дублированные значения. На этапе предобработки данных, я поищу возможность исправить все ошибки в данных, которые могут привести к искажению конечного результата исследования. После чего, создам необходимые столбцы, исправлю формат некоторых столбцов в датафреймах и приступлю к проведению исследовательского анализа.

Моё исследование будет проходить через следующие этапы:
- Обзор данных;
- Предобработка данных;
- Описание и визуализация:
  - частоты встречаемости городов;
  - соотношения пользователей с подпиской и без подписки;
  - возраста пользователей;
  - расстояния, преодоленное пользователем за одну поездку;
  - продолжительности поездок.
- Объединение данных;
- Подсчёт выручки:
- Проверка гипотез.


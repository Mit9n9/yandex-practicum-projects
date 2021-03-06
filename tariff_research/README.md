# Сравнение тарифов
## Данные
В данном проекте данные представлены в нескольких таблицах `.csv`.
Описание данных:
### Таблица users
- Уникальный идентификатор пользователя
- Имя пользователя
- Фамилия пользователя
- Возраст пользователя (годы)
- Дата подключения тарифа (день, месяц, год)
- Дата прекращения пользования тарифом (если значение пропущено, то тариф ещё действовал на момент выгрузки данных)
- Город проживания пользователя
- Название тарифного плана
### Таблица calls
- Уникальный номер звонка
- Дата звонка
- Длительность звонка в минутах
- Идентификатор пользователя, сделавшего звонок
### Таблица messages
- уникальный номер сообщения
- дата сообщения
- идентификатор пользователя, отправившего сообщение
### Таблица internet
- Уникальный номер сессии
- Объём потраченного за сессию интернет-трафика (в мегабайтах)
- Дата интернет-сессии
- Идентификатор пользователя
### Таблица tariffs
- Название тарифа
- Ежемесячная абонентская плата в рублях
- Количество минут разговора в месяц, включённых в абонентскую плату
- Количество сообщений в месяц, включённых в абонентскую плату
- Объём интернет-трафика, включённого в абонентскую плату (в мегабайтах)
- Стоимость минуты разговора сверх тарифного пакета (например, если в тарифе 100 минут разговора в месяц, то со 101 минуты будет взиматься плата)
- Стоимость отправки сообщения сверх тарифного пакета
- Стоимость дополнительного гигабайта интернет-трафика сверх тарифного пакета (1 гигабайт = 1024 мегабайта)
## Задача
Необходимо подготовить данные, провести предобработку, посчитать необходимые для анализа величины. Описать поведение клиентов оператора, исходя из выборки. Проанализировать сколько минут разговора, сколько сообщений и какой объём интернет-трафика требуется пользователям каждого тарифа в месяц, посчитайте среднее количество, дисперсию и стандартное отклонение. Описать распределения. Проверить статистические гипотезы: средняя выручка пользователей тарифов «Ультра» и «Смарт» различаются, средняя выручка пользователей из Москвы отличается от выручки пользователей из других регионов.
## Используемые библиотеки
*pandas*, *matplotlib*, *numpy*, *scipy*

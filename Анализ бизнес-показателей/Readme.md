# Анализ бизнес-показателей Яндекс.Афиша

У нас есть данные о посещениях, заказах пользователей и данные по рекламным расходам для каждого источника трафика. Ключевая залача: изучить как клиенты пользуются сервисом, чтобы перераспределить бюджет в сторону более прибыльных источников трафиков. 

Что было сделано:

**1 Продуктовые метрики**
- Посчитали продуктовые метрики: `DAU`, `WAU`, `MAU`. Посмотрели на их динамику за весь период.
- Посмотрели, среднюю частоту посещений пользователей за день и как долго длится пользовательская сессия.
- Посчитали `Retention Rate`, сделав когоротный анализ. Посмотрели, пользователи каких когорт имеют наиболее высокий рейтинг.

**2 Метрики электронной коммерции**
- Выяснили, сколько времени в среднем проходит с момента первого посещения до покупки.
- При помощи когортного анализа посмотрели, сколько в среднем покупок приходится на пользователя за 6 месяцев.
- Посмотрели на средний чек в разрезе каждого месяца.
- Посчитали средний `LTV` по когортам.

**3 Маркетинговые метрики**
- Посчитали общую сумму расходов в разрезе каждого месяца, каждого источника трафика.
- Рассчитали средний `CAC` на покупателя в разрезе каждого источника трафика.
- Рассчитали `ROMI` по когортам в разрезе источников. Посмотрели на динамику метрики во времени, проанализировали, какие когорты быстрее окупаются.

**Выводы:**

Наиболее перспективные источники:
- *source_id = 1*. Эти пользователи приносят хорошую прибыль компании. `ROMI` около 5 на последних месяцах когорт
- *source_id = 5*. `ROMI` не такой высокий, но затраты окупаются стабильно начиная с 4 месяца.
- *source_id = 9*. Тоже быстрая окупаемость при самых низких затратах.

При выборе наиболее прибыльного канала привлечения использовали коэффициент `ROMI`, который учитывает и `LTV`, и `CAC`. Иногда в пример приводили низкие затраты и хорошую эффективность - это к тому, что следует пересмотреть направление инвестиций

Итак, наиболее прибыльными оказались **первый, пятый и девятый источник**, если  смотреть соотношение `LTV/CAC`. Наиболее же прибыльные когорты клиентов с точки зрения месяца первой покупки оказались: **июньская, сентябрьская когорты** (смотрели `LTV`, среднее количество покупок на пользователя). Следует более детально изучить поведение этих когорт, чтобы перенести их успешный опыт на другие когорты.

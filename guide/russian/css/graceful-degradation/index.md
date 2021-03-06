---
title: Graceful Degradation
localeTitle: Изящная деградация
---
## Изящная деградация

**Изящная деградация** – понятие достаточно широкое, в общем можно сказать, что это способность системы продолжать своё функционирование в случае отказа некоторых её компонентов. И чем серьёзней отказ, тем ниже качество работы системы и работы с системой.

Изящная деградация может выражаться в возможности работы с отключенным JavaScript, в аккуратном отображении сайта в браузере без поддержки спецификации CSS3, в адекватном отображении сайта с отключенными картинками. Все эти отказы не должны влиять на работу веб-приложения. Однако, если все работает, то пользователю гораздо удобнее пользоваться сайтом.

Если рассмотреть конкретный пример, например в области проектирования веб-интерфеса, то этот принцип можно сформулировать как «система может работать и с полностью отключенным JavaScript, но с включенным с ней будет работать намного удобнее». Вопрос не в том, может ли быть такая ситуация, что JS отключен или не функционирует полностью, или почему это происходит. Эта ситуация берется как данность. Дизайнер должен разработать такой интерфейс, который будет так же продолжать работать, пусть и с отключенным JS.

Часто для следования этому принципу приходится переделывать логику серверной обработки форм. Однако, такой подход будет окупаться, если задуматься об отказоустойчивости еще на этапе планирования формы.

Соблюдение принципа graceful degradation позволяет пользователям (а каждый пользователь — это потенциальный клиент) иметь возможность работы с сайтом в любых ситуациях.

Советы:

- Создание отказоустойчивого интерфейса является достаточно трудоёмкой работой.
- Затраты на создание такого интерфейса намного ниже, если предусматривать отказоустойчивость с самого начала.
- В некоторых случаях приходится усложнять серверную логику, чтобы такой интерфейс работал так как нужно.
- Практически всегда усложняется клиентская логика и логика отображения.
- Так как не нужно показывать пользователю элементы, которые он не сможет использовать при отключённом JS и не нужно показывать элементы, которые избыточны при включённом JS.

#### Дополнительная информация:
[Заметки об изящной деградации](https://htmlacademy.ru/blog/6-graceful-degradation)

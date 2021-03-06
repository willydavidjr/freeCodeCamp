---
title: Tuples
localeTitle: الصفوف
---
## الصفوف

في الإكسير ، الصفوف هي بنية بيانات يمكنها الاحتفاظ بأي قيمة أو خليط من الأنواع. يتم تعريف المجموعات بواسطة الأقواس المتعرجة ، وتبدأ الفهارس الخاصة بها من 0. ولما كانت الصفوف يتم تخزينها بشكل متقارب في الذاكرة ، فإن الحصول على البيانات منها هو عملية سريعة جدًا.

```elixir
iex> tuple = {:atom, "string"}
{:atom, "string"}
iex> elem(tuple, 0)
:atom
``` 

## ثبات

تعتبر الصفوف في Elixir غير قابلة للتغيير ، لذا فإن إجراء تعديلات سيؤدي إلى ظهور مجموعة جديدة تمامًا - مما يوفر النص الأصلي في الذاكرة.

```elixir
iex> tuple = {:atom, "string"}
{:atom, "string"}
iex> put_elem(tuple, 1, true)
{:atom, true}
iex> tuple
{:atom, "string"}
``` 

## نمط مطابقة

الاستخدام الأكثر شيوعًا للصفوف في الإكسير هو بمثابة عودة لوظيفة. على سبيل المثال: `{:ok, "Hello World\n"}` هذا أمر مفيد للغاية ، لأنه يتيح استخدام مطابقة الأنماط للتعامل مع هذه العوائد.

#### معلومات اكثر:

*   [elixir-lang.org | العودية](https://elixir-lang.org/getting-started/basic-types.html#tuples)
*   [hexdocs | التعداد](https://hexdocs.pm/elixir/Tuple.html)
+++
date = '2024-12-25T01:40:24+03:00'
title = 'Применение автоматических отступов flexbox'
categories = [ "css", "flexbox" ]
+++

Алгоритм расчёта размеров флекс-элементов и их распределения внутри флекс-контейнера включает три последовательных этапа. Этот процесс значительно сложнее, чем в традиционной блочной модели.

### Шаг третий - Применение автоматических отступов

Если во флекс-контейнере остаётся свободное место, то автоматически применяются отступы с помощью свойства `margin`, установленного в значение `auto` для флекс-элементов.

Во флексбоксе автоматические отступы `margin: auto` функционируют значительно эффективнее, чем в стандартной блочной модели. Во-первых, они применяются во всех направлениях, в отличие от блочной модели, где они работают только по горизонтали. Во-вторых, автоматические отступы могут взаимодействовать между собой: если на одной оси присутствует несколько таких отступов (у разных элементов или с разных сторон одного элемента), то свободное пространство распределяется между ними равномерно.

Рассмотрим пример. Здесь проявляется эффект от использования автоматических отступов: `margin-top: auto` и `margin-left: auto`. Эти свойства смещают элемент, заставляя его занять оставшееся свободное пространство по вертикали и горизонтали.

```
.flex-container {
  display: flex;
  flex-direction: row;
}

.flex-container div:nth-child(2) {
  margin-top: auto;
  margin-left: auto;
  width: 200px;
}
```

![](/images/margin_auto_flexbox.png)

Браузеры всегда преобразуют значение отступов `auto` в конкретные пиксельные значения. В нашем примере браузер уже «определил» размеры свободного пространства в пикселях по обеим осям. По главной оси он вычел ширину элементов из ширины контейнера, а по поперечной оси — высоту флекс-элемента (включая высоту строки текста и вертикальные отступы) из высоты контейнера. При этом расчёты по поперечной оси проще, так как у каждого элемента своя собственная поперечная ось.

По главной оси присутствует только один автоматический отступ (слева у второго элемента), поэтому его размер стал равен всему доступному свободному пространству. В результате это свободное пространство полностью перешло в отступ, и вдоль главной оси его больше не осталось. Второй элемент отодвинулся от первого, а третий элемент прижался к правому краю флекс-контейнера.

По поперечной оси второго элемента также присутствует только один автоматический отступ (сверху), поэтому его размер стал равен всему доступному свободному пространству. В результате это свободное пространство полностью перешло в отступ, и вдоль поперечной оси второго элемента его больше не осталось. Элемент прижался к концу своей поперечной оси.

Первый и третий элементы растягиваются на всю высоту контейнера из-за свойства `align-items`, которое по умолчанию имеет значение `stretch`. Это значение растягивает флекс-элементы вдоль поперечной оси, если им не задан фиксированный размер по этой оси и если вдоль поперечной оси есть свободное пространство.

Второй элемент перестал растягиваться на всю высоту, несмотря на то, что ему не задана фиксированная высота. Это означает, что вдоль его поперечной оси не осталось свободного пространства — оно полностью перешло в автоматический отступ сверху. Из этого примера важно запомнить, что свойства для выравнивания и распределения применяются после автоматических отступов. Если бы отступы работали после выравнивания, второй элемент не уменьшился бы по высоте.

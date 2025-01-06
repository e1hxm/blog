+++
date = '2024-11-23T18:53:24+03:00'
title = 'Свойство align-content'
categories = [ "css", "flexbox" ]
+++
Лекция в HTML Academy про align-content

Свойство <code class="code_line">justify-content</code> управляет распределением флекс-элементов вдоль главной оси,
а <code class="code_line">align-content</code> — выравниванием рядов флекс-элементов вдоль поперечной оси. Оба
свойства имеют схожие значения:

 1. 1 <code class="code_line">flex-start</code>
 2. 2 <code class="code_line">flex-end</code>
 3. 3 <code class="code_line">center</code>
 4. 4 <code class="code_line">space-between</code>
 5. 5 <code class="code_line">stretch</code> - доступно только для <code class="code_line">align-content</code> и является значением по умолчанию.

Свойство <code class="code_line">align-content</code> переопределяет значение <code class="code_line">align-items</code>, которое управляет
выравниванием отдельных флекс-элементов вдоль поперечной оси. Это происходит как для
одного ряда флекс-элементов, так и для нескольких рядов.

Однако есть один нюанс: <code class="code_line">align-content</code> перестаёт работать, если для флекс-контейнера
установлено свойство <code class="coe_line">flex-wrap: nowrap</code>. Это происходит потому, что в таком случае
высота строки равна высоте флекс-контейнера, и на поперечной оси не остаётся
свободного пространства.

В результате <code class="code_line">align-content</code> не может применяться. Вместо этого будут работать
свойства <code class="code_line">align-items</code> и <code class="code_line">align-self</code>, если размеры флекс-элементов позволяют, и мы увидим результат их выравнивания.

### Свойство align-content: stretch и align-items

Когда одновременно задаются свойства <code class="code_line">align-items</code> и <code class="code_line">align-content</code>, <code class="code_line">align-items</code> не отключается полностью, а может влиять на отображение флекс-элементов внутри рядов.

Это особенно заметно, когда для <code class="coe_line">align-content</code> используется значение по умолчанию —
<code class="code_line">stretch</code>. В этом случае ряды флекс-элементов растягиваются, занимая всё доступное
пространство поперечной оси, а оставшееся свободное место между рядами делится поровну.

Поведение строк при <code class="code_line">align-content: stretch</code> зависит от значения <code class="code_line">align-items</code>:

1. 1 Если <code class="code_line">align-items</code> имеет значение <code class="code_line">stretch</code>, элементы внутри строк растягиваются на всю высоту своей строки.

2. 2 Если значение <code class="code_line">align-items</code> отлично от <code class="code_line">stretch</code>, элементы внутри 
строк сжимаются под своё содержимое и выравниваются в строках в соответствии с заданным значением
<code class="code_line">align-items</code> (например, <code class="code_line">flex-start</code>, <code class="code_line">center</code>, <code class="code_line">flex-end</code> и т.д.).

Таким образом, <code class="code_line">align-items</code> продолжает влиять на выравнивание элементов внутри строк,
даже если <code class="code_line">align-content</code> установлено на <code class="code_line">stretch</code>.

### Свойство order, порядковый номер flex-элемента

Еще одно свойство - это <code class="code_line">order</code>, которое определяет порядковый номер флекс-элемента.

```js
.flex-element {
// этот элемент станет отображаться первым в контейнере
order: -1; 
```

По умолчанию порядковый номер флекс-элементов равен "0", и они сортируются по
возрастанию этого номера.

Это свойство очень полезно, так как позволяет изменять порядок следования
флекс-элементов в потоке, не изменяя при этом HTML-код.
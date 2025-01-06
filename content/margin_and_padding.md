+++
date = '2024-10-12T18:53:24+03:00'
title = 'Margin и Padding в CSS'
categories = [ "css" ]
+++

<p>Лекция от HTMLAcademy про margin и padding в css</p>
            <h3>Свойство padding</h3>
            <p>
              Внутренний отступ — это пространство между содержимым элемента и его границей
              (рамкой).
            </p>
            <img src="../images/padding.png" />
            <p>
              Внутренние отступы элемента задаются с использованием свойства padding. Если отступы
              одинаковы со всех сторон, можно просто указать:
            </p>
            <pre><code>.main__content {
  padding: 15px;
}</code></pre>
            <p>Такой способ записи называется сокращённым.</p>
            <p>
              Если отступы на разных сторонах отличаются, используют полную запись, где указывают
              внутренний отступ для каждой стороны отдельно:
            </p>
            <pre><code>.main__content {
  padding-top: 5px;
  padding-right: 10px;
  padding-bottom: 15px;
  padding-left: 20px;
}</code></pre>
            <p>
              Свойство padding-top добавляет внутренний отступ сверху, padding-right — справа,
              padding-bottom — снизу, а padding-left — слева.
            </p>
            <h3>Свойство margin</h3>
            <p>
              Внешний отступ — это пространство между внешней границей элемента и границами его
              родительского элемента или соседних элементов.
            </p>
            <p>
              Для управления внешними отступами используется свойство margin. Оно, как и padding,
              поддерживает как краткую, так и полную запись.
            </p>
            <pre><code>// Краткая запись
margin: 20px;
// Полная запись
margin-top: 0;
margin-right: 5px;
margin-bottom: 10px;
margin-left: 15px;</code></pre>
            <p>
              Свойство margin-top создаёт внешний отступ сверху, margin-right — справа,
              margin-bottom — снизу, а margin-left — слева.
            </p>
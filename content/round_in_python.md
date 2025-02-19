+++
date = '2025-01-21T12:05:24+03:00'
title = 'Функция round() в Python'
categories = [ "python" ]
+++

### Number

Функция `round()` в Python используется для округления чисел. Она может округлять как целые числа, так и числа с плавающей запятой `float`

Синтаксис функции `round()`
```python
round(number, ndigits)
```

>`number` — число, которое нужно округлить

>`ndigits` (необязательный) — количество знаков после запятой. Если не указано, число округляется до ближайшего целого

Округление до ближайшего целого

```python
result = round(3.14159)
print(result)  # Вывод: 3
```

Округление с указанием количества знаков после запятой

```python
result = round(3.14159, 2)
print(result)  # Вывод: 3.14
```

Округление до ближайшего большего целого

```python
result = round(3.7)
print(result)  # Вывод: 4
```

Округление отрицательных чисел

```python
result = round(-2.7)
print(result)  # Вывод: -3
```

Округление до ближайшего четного числа
если число находится ровно посередине

```python
result = round(2.5)
print(result)  # Вывод: 2
```

Если `ndigits` не указан, `round()` округляет до ближайшего целого.

Если `ndigits` указан, округление происходит до указанного количества знаков после запятой.

Если число находится ровно посередине между двумя возможными вариантами (например, 2.5), `Python` округляет до ближайшего четного числа (это называется "банковское округление")

### ndigits

Примеры с `ndigits` - вторым параметром функции `round()`

Округление до одного знака после запятой

```python
result = round(3.14159, 1)
print(result)  # Вывод: 3.1
```

Округление до трех знаков после запятой

```python
result = round(3.14159, 3)
print(result)  # Вывод: 3.142
```

Округление до нуля знаков после запятой, эквивалентно округлению
до целого числа

```python
result = round(3.14159, 0)
print(result)  # Вывод: 3.0
```

Функция `round()` часто используется для:

>Упрощения чисел для вывода.

>Ограничения количества знаков после запятой в расчетах.

>Подготовки данных для дальнейшей обработки.
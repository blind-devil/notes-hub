# Заметки по Python

<a name='1'></a> **Базовые понятия:**

* [Комментарии](#1.1)
* [Именование](#1.2)
* [Ключевые слова](#1.3)
* [Присваивание переменным](#1.4)
* [Перенос длинной строки кода](#1.5)
* [Подчеркивание в числах](#1.6)
* [Возврат Null значения](#1.7)
* [Удаление](#1.8)
* [Исключение](#1.9)
* [Завершение программы](#1.10)

<a name='2'></a>**Операторы:**

* [Арифметические операторы](#2.1)
* [Операторы присваивания](#2.2)
* [Операторы сравнения](#2.3)
* [Логические операторы](#2.4)
* [Операторы принадлежности](#2.5)
* [Операторы тождественности](#2.6)

<a name='3'></a> **Данные:**

* [Типы данных](#3.1)
* [Идентификация данных](#3.2)
* [Числа и строки](#3.3)
* [Списки](#3.4)
* [Кортежи](#3.5)
* [Словари](#3.6)
* [Множества](#3.7)

<a name='4'></a>**Условия:**

* [if-elif-else](#4.1)

<a name='5'></a>**Циклы:**

* [Цикл while](#5.1)
* [Цикл for](#5.2)
* [Управление циклами](#5.3)

<a name='6'></a>**Базовые функции:**

* [input()](#6.1)
* [print()](#6.2)
* [len()](#6.3)
* [range()](#6.4)
* [min() и max()](#6.5)
* [enumerate()](#6.6)

<a name='7'></a> **Пользовательские функции:**

* [Своя функция](#7.1)
* [Функции без возврата значения](#7.2)
* [Функции с возвратом значения](#7.3)

<a name='8'></a> **Строки:**

* [Экранированные символы](#8.1)
* [F-строки](#8.2)
* [Индексация строк](#8.3)
* [Манипуляции со строками](#8.4)
* [Методы объекта строки](#8.5)

<a name='9'></a>**Списки и кортежи:**

* [Индексация списков/кортежей](#9.1)
* [Манипуляции со списками/кортежами](#9.2)
* [Методы объекта списка](#9.3)

<a name='10'></a> **Словари:**

* [Манипуляции с элементами в словаре](#10.1)
* [Методы объекта словаря](#10.2)

<a name='11'></a> **Множества:**

* [Методы объекта множества](#11.1)

<a name='12'></a> **Файлы:**

* [open()](#12.1)
* [Методы объекта файла](#12.2)

***

### Базовые понятия

***

#### <a name='1.1'></a> Комментарии [🠕](#1)

```python
# Комментарий кода

'''Это
многострочный
комментарий
'''

"""Это также
многострочный
комментарий
"""
```

> Важно знать, при частом использовании комментариев с тройными кавычками `'''`/`"""`, в большой программе будет наблюдаться нерациональное использование памяти, поскольку будут создаваться строковые объекты, а вот комментарии через решотку `#` никак не обрабатываются и в памяти не откладываются.

#### <a name='1.2'></a> Именование [🠕](#1)

`Hi` `tool_01` `_name1` `BigOne`

~~`25tor`~~ ~~`your name`~~ ~~`keyword`~~

> Важно знать, в именовании лучше избегать использования знака подчеркивания `_` в качестве первого символа имени, поскольку такие имена имеют специальное значение в Python.

#### <a name='1.3'></a> Ключевые слова [🠕](#1)

`and`     |`else`    |`import`   |`pass`
:--------:|:--------:|:---------:|:---------:
`assert`  |`except`  |`in`       |`raise`
`break`   |`False`   |`is`       |`return`
`class`   |`finally` |`lambda`   |`True`
`continue`|`for`     |`None`     |`try`
`def`     |`from`    |`nonlocal` |`while`
`del`     |`global`  |`not`      |`with/as`
`elif`    |`if`      |`or`       |`yield`

#### <a name='1.4'></a> Присваивание переменным [🠕](#1)

```python
room = 666                       # Присваивание целого числа
value_1 = 37.15                  # Присваивание вещесвенного числа
name = 'Василий'                 # Присваивание строки
sum += 1                         # Добавление к данным переменной с присваиванием
num_1 = num_2 = 3                # Присваивание двум переменным один объект
x, y = 8, 9                      # Множественное присваивание
x, y, *z = 8, 0, 12, 3           # Множественное присваивание с включением лишних объектов
swap1, swap2 = swap2, swap1      # Рокировка объктов между переменными
```

#### <a name='1.5'></a> Перенос длинной строки кода [🠕](#1)

`\` - разделяет длинную строку кода на несколько:

```python
result = 3 + 5 * \
    1 + 3 - 8
print(result)

text = 'Длинный \
    текст'
print(text)
```

В круглых скобках разделитель не используется:

```python
mondey = 10.6 + 45.66 + 77
print('Продажи в понедельник составили',
    mondey, 'долларов')

num = (5 * 103.58 - 47.13 + 55.45 *
    13 - 4.36)
print(num)
```

#### <a name='1.6'></a> Подчеркивание в числах [🠕](#1)

`_` - разделяет цифры в больших числах для удобочитаемости:

```python
num = 1_000_200
salary = 20_123.23
```

#### <a name='1.7'></a> Возврат Null значения [🠕](#1)

`psss` - возвращает `Null` в тех местах, где это синтаксически необходимо, например: в инструкциях, где тело является обязательным, таких как `def`, `while`, `for`, `except` и пр.

Заглушка для функции:

```python
def get_sum():
    pass
```

Заглушка для цикла:

```python
for line in text:
    pass
```

#### <a name='1.8'></a> Удаление [🠕](#1)

`del` - удаляет переменные, кортежи, списки или части списка, словари или части словаря:

```python
x_list = [56, 78, 1]
del x_list[0]
print(x_list)                    # Вывод будет: [78, 1]
del x_list
print(x_list)                    # Возникнет исключение
```

#### <a name='1.9'></a> Исключение [🠕](#1)

* `try` - проверяет блок кода на наличие ошибок.
* `except тип_ошибки` - обрабатывает ошибку, обработчиков может быть несколько, если не будет указан тип ошибки то будут "ловиться" все ошибки.
* `else` - выполняет код при отсутствии ошибок.
* `finally` - выполняет код независимо от результата блоков `try` и `except`.

```python
from subprocess import run

try:
    run('sudo pacman -Syyu --noconfirm', shell=True, check=True)
except:
    print('Обновление не удалось.')
else:
    print('Обновление выполнено без ошибок.')
finally:
    print('Блок try и except выполнили свою работу.')
```

#### <a name='1.10'></a> Завершение программы [🠕](#1)

* `raise` - принудительно вызывает исключение.
* `SystemExit` - исключение завершающее программу.

```python
raise SystemExit                 # Завершает программу
```

***

### Операторы

***

#### <a name='2.1'></a> Арифметические операторы [🠕](#2)

* `+` - добавление: `4 + 2`.
* `-` - вычитание: `8 - 5`.
* `*` - умножение: `2 * 2`.
* `/` - деление: `9 / 3`.
* `//` - целочисленное деление: `10 // 3`.
* `%` - остаток от деления: `17 % 4`.
* `**` - возведение в степень: `4 ** 2`.

#### <a name='2.2'></a> Операторы присваивания [🠕](#2)

* `=` - присваивание: `x = 5`.
* `+=` - добавление с присваиванием: `x += 3`.
* `-=` - вычитание с присваиванием: `x -= 3`.
* `*=` - умножение с присваиванием: `x *= 3`.
* `/=` - деление с присваиванием: `x /= 3`.
* `//=` - целочисленное деление с присваиванием: `x //= 3`.
* `%=` - остаток от деления с присваиванием: `x %= 3`.
* `**=` - возведение в степень с присваиванием: `x **= 3`.

#### <a name='2.3'></a> Операторы сравнения [🠕](#2)

* `==` - равно: `x == y`.
* `!=` - не равно: `x != y`.
* `>` - больше чем: `x > y`.
* `<` - меньше чем: `x < y`.
* `>=` - больше чем или равно: `x >= y`.
* `<=` - меньше чем или равно: `x <= y`.

#### <a name='2.4'></a> Логические операторы [🠕](#2)

* `and` - возвращает значение `True` если оба утверждения верны: `x > 5 and x < 10`.
* `or` - возвращает `True` если одно из утверждений верно: `x < 5 or x < 4`.
* `not` - меняет результат, возвращает `False` если результат `True`: `not(x < 5 and x < 10)`.

#### <a name='2.5'></a> Операторы принадлежности [🠕](#2)

* `in` - возвращает `True` если последовательность присутствует в объекте: `x in y`.
* `not in` - возвращает `True` если последовательность не присутствует в объекте: `x not in y`.

#### <a name='2.6'></a> Операторы тождественности [🠕](#2)

* `is` - Возвращает `True`, если оба операнда указывают на один объект: `x is y`.
* `is not` - Возврашает `False`, если оба операнда указывают на один объект: `x is not y`.

***

### Данные

***

#### <a name='3.1'></a> Типы данных [🠕](#3)

* `int` - целые числа: `some = 1`.
* `float` - вещественные числа: `some = 1.12`.
* `str` - строки: `some = 'Привет мир'`.
* `list` - списки: `some = [1, 2.2, 'text']`.
* `tuple` - кортежи: `some = (1, 2.2, 'text')`.
* `dict` - словари: `some = {'key1': 643, 'key2': 974}`
* `set` - множества: `some = {12, 54.56, 'text'}`
* `bool` - булевые: `some = True` или `some = False`.

#### <a name='3.2'></a> Идентификация данных [🠕](#3)

`type()` - индентифицирует данные:

```python
type(15)                         # Вывод будет: <class 'int'>
type(49.11)                      # Вывод будет: <class 'float'>
type('Просто текст')             # Вывод будет: <class 'str'>
type([1, 32.5, 'текст'])         # Вывод будет: <class 'list'>
type((1, 32.5, 'текст'))         # Вывод будет: <class 'tuple'>
type({'key1': 234, 'key2': 345}) # Вывод будет: <class 'dict'>
type({123, 643, 'текст'})        # Вывод будет: <class 'set'>
type(True)                       # Вывод будет: <class 'bool'>
```

#### <a name='3.3'></a> Числа и строки [🠕](#3)

* `int()` - преобразовует в целые числа.
* `float()` - преобразовует в вещесвенные числа.
* `str()` - преобразовует в строки.

```python
num1 = 16                        # Переменная с целым числом
num2 = 33.45                     # Переменная с вещесвенным числом

f_num = float(num1)              # Преобразование целого числа в вещесвенное
print(f_num)                     # Вывод будет: 16.0

i_num = int(num2)                # Преобразование вещественного числа в целое
print(i_num)                     # Вывод будет: 33

s_num = str(num1 + num2)         # Преобразование суммы чисел в строку
print(s_num)                     # Вывод будет: '49.45'
```

> Важно знать, если в строке `str` имеются буквенные символы, а не цифры, то преобразовать в целочисленное или вещественное значение не получиться.

#### <a name='3.4'></a> Списки [🠕](#3)

`list()` - преобразовует некоторые типы объектов в списки:

```python
text = 'Hello'                   # Строка
text_list = list(text)           # Преобразование строки в список
print(text_list)                 # Вывод будет: ['H', 'e', 'l', 'l', 'o']

num_list = list(range(5))        # Задается диапазон через range()
print(num_list)                  # Вывод будет: [0, 1, 2, 3, 4]

name = ('Вася', 'Пупкин')        # Кортеж
name_list = list(name)           # Преобразование кортежа в список
print(name_list)                 # Вывод будет: ['Вася', 'Пупкин']
```

#### <a name='3.5'></a> Кортежи [🠕](#3)

`tuple()` - преобразовует некоторые типы объектов в кортежи:

```python
text = 'Hello'                   # Строка
text_tuple = tuple(text)         # Преобразование строки в кортеж
print(text_tuple)                # Вывод будет: ('H', 'e', 'l', 'l', 'o')

num_tuple = tuple(range(5))      # Задается диапазон через range()
print(num_tuple)                 # Вывод будет: (0, 1, 2, 3, 4)

name = ['Вася', 'Пупкин']        # Список
name_tuple = tuple(name)         # Преобразование списка в кортеж
print(name_tuple)                # Вывод будет: ('Вася', 'Пупкин')
```
#### <a name='3.6'></a> Словари [🠕](#3)

`dict()` - создает словарь:

```python
x_dict = dict(
    name = 'Вася',               # Ключ = значение
    age = 37                     # Ключ = значение
)
print(x_dict)                    # Вывод будет: {'name': 'Вася', 'age': 37}
```

> Важно знать, значения в словаре могут быть объектами любого типа, но ключи должны быть неизменяемыми объектами, на­пример ключами могут быть: строковые значения `str`, целые числа `int`, вещесвенные числа `float`, кортежи `tuple`.

Конвертация списка в словарь:

```python
x_list = [['brand', 'samsung'], ['price', 120]]
x_dict = dict(x_list)
print(x_dict)
```

#### <a name='3.7'></a> Множества [🠕](#3)

`set()` - создает множество:

```python
x_set = set()                    # Создание пустого множества
print(x_set)                     # Вывод будет: {}

text = 'Hello'                   # Строка
x_set = set(text)                # Создание множества из строки
print(x_set)                     # Вывод будет: {'H', 'e', 'l', 'o'}

num_set = set(range(5))          # Задается диапазон через range()
print(num_set)                   # Вывод будет: {0, 1, 2, 3, 4}

x_list = [12, 67, 23, 12]        # Список/кортеж
x_set = set(x_list)              # Создание множества из списка/кортежа
print(x_set)                     # Вывод будет: {12, 67, 23}
```

> Важно знать, в функцию `set()` можно передавать только один аргумент.

***

### Условия

***

#### <a name='4.1'></a> if-elif-else [🠕](#4)

* `if` - "если" условие `True` то будет выполнятся вложенная инструкция:

```python
if 4 < 10:
    print('if сработал')
```

* `elif` - в противном случае "если", которое ставится после `if`, и выполняется когда предыдущие условия являются `False`:

```python
x = 15
y = 9
if x == y:
    print('if сработал')
elif x > y:
    print('elif сработал')
```

* `else` - "иначе", ставится после `if` и `elif`, выполняется когда все условия `False`:

```python
a = 56
b = 30
if a < b:
    print('if сработал')
elif a == b:
    print('elif сработал')
else:
    print('else сработал')
```

***

### Циклы

***

#### <a name='5.1'></a> Цикл while [🠕](#5)

`while` - цикл с условием повторения:

```python
x = 1
b = 11
while x < b:
    print(x)
    x += 1
print('Конец')
```

#### <a name='5.2'></a> Цикл for [🠕](#5)

`for` - цикл со счетчиком повторения:

```python
for num in [1, 2, 3, 4, 5]:
    print(num)
print('Конец')
```

С помощью функции `range()` можно задать диапазон:

```python
for num in range(10, 0, -1):     # range(начало, конец, шаг)
    print(num)
print('Конец')
```

#### <a name='5.3'></a> Управление циклами [🠕](#5)

* `break` - прерывает цикл, в котором он объявлен:

```python
x = 1
b = 101
while x <= b:
    if x == 51:
        break
    print(x)
    x += 1
print('Конец')
```

* `continue` - пропускает оставшееся тело цикла текущей итерации:

```python
for val in 'строка':
    if val == 'о':
        continue
    print(val)
print('Конец')
```

***

### Базовые функции

***

#### <a name='6.1'></a> input() [🠕](#6)

`input()` - обрабатывает пользовательский ввод с клавиатуры:

```python
name = input('Введите имя: ')    # В скобках указывается подсказка для ввода
```

> Важно знать, пользовательский ввод всегда является строкой `str`, даже если ввести число.

#### <a name='6.2'></a> print() [🠕](#6)

`print()` - выводит сообщения на экран:

```python
print('Привет мир!')             # Обычный вывод "Привет мир!"
print('Привет', 'мир!')          # Вывод нескольких объектов через запятую

num = 2 + 6                      # Переменная
print(num)                       # Вывод переменной
```

Аргументы функции:
* `sep='separator'` - указывает как разделить объекты, если их несколько, по умолчанию стоит `' '`:

```python
print('Между', 'объектами', 'будет', 'спецыальный', 'символ', sep='-')
```

* `end='end'` - указывает что печатать в конце строки, по умолчанию стоит `\n`:

```python
print('Вывод будет', end=' ')
print('в одной строке')
```

* `file=some_file` - контролирует то, куда выводятся значения функции `print()`:

```python
with open('some.txt', 'w') as some_file:
    print('Привет мир!', file=some_file)
```

#### <a name='6.3'></a> len() [🠕](#6)

`len()` - возвращает длину (количество элементов) в объекте:

```python
len('Привет мир!')               # Вывод будет: 11
```

Аргумент может быть последовательностью, такой как строка, байты, кортеж, список или диапазон или коллекцией.

#### <a name='6.4'></a> range() [🠕](#6)

`range()` - возвращает неизменяемую последовательность целых чисел в виде объекта `range`:

```python
range(1, 11, 1)                  # range(начало, конец, шаг)
```

Обычно функцию используют как диапазон в циклах `for`, также для создания списков `list` или кортежей `tuple`.

#### <a name='6.5'></a> min() и max() [🠕](#6)

* `min()` - возвращает минимальное значение из последовательности.
* `max()` - возвращает максимальное значение из последовательности.

```python
x_list = [7, 4, 1, 89]
print(min(x_list))               # Вывод будет: 1
print(max(x_list))               # Вывод будет: 89
```

#### <a name='6.6'></a> enumerate() [🠕](#6)

`enumerate()` - объединяет данные проходимого объекта (например, списка, кортежа или строки) в последовательность, состоящую из индексов и значений элементов.

Обычно функция используется в цикле `for`:

```python
x_list = [90, 17.3, 'World']
for count, value in enumerate(x_list):
    print(count, value)
```

***

### Пользовательские функции

***

#### <a name='7.1'></a> Своя функция [🠕](#7)

* `def` - определяет функцию.
* `return` - возвращает значение.

```python
def имя_функции(аргументы):
    тело_функции
    return значение
```

#### <a name='7.2'></a> Функции без возврата значения [🠕](#7)

Без аргументов:

```python
def main():
    hey_you()

def hey_you():
    answer = input('Привет, хочешь со мной поболтать? (y/n): ')
    if answer == 'y':
        print('Я ведь программа, и не смогу с тобой поболтать xD')
    elif answer == 'n':
        print('Ой все, вечно у тебя нет на меня времени.')
    else:
        print('Ладно, вижу ты в не адеквате, потом поболтаем.')

if __name__ == '__main__':
    main()
```

С аргументами:

```python
def main():
    x = float(input('Введите первое число: '))
    y = float(input('Введите второе число: '))
    get_sum(x, num2=y)

def get_sum(num1, num2):
    sum = num1 + num2
    print(f'Сумма чисел: {int(sum)}')

if __name__ == '__main__':
    main()
```

#### <a name='7.3'></a> Функции с возвратом значения [🠕](#7)

Без аргументов:

```python
def main():
    first_name, last_name = get_name()
    print(first_name, last_name)

def get_name():
    first = input('Введите своё имя: ')
    last = input('Введите свою фамилию: ')
    return first, last

if __name__ == '__main__':
    main()
```

С аргументами:

```python
def main():
    number = int(input('Bвeдите число: '))
    if is_even(number):
        print('Это число четное.')
    else:
        print('Этo число нечетное.')

def is_even(number):
    if (number % 2) == 0:
        return True
    else:
        return False

if __name__ == '__main__':
    main()
```

***

### Строки

***

#### <a name='8.1'></a> Экранированные символы [🠕](#8)

* `\n` - переводит позицию печати на следующую строку:

```python
'Первая строка\nВторая строка'
```

* `\t` - переводит позицию печати на следующую горизонтальную позицию табуляции:

```python
'Между\tобъектами\tтабуляция'
```

* `\'` - печатает одинарную кавычку:

```python
'Выделяем \'объект\' в одинарные кавычки'
```

* `\"` - печатает двойную кавычку:

```python
'Выделяем \"объект\" в двойные кавычки'
```

* `\\` - печатает обратную косую черту:

```python
'Печатаем косую черту \\'
```

#### <a name='8.2'></a> F-строки [🠕](#8)

* `f'Привет мир!'` - обычное форматирование.
* `f'{some}'` - вставка переменной.
* `f'{50 - 20 * 2}'` - вставка выражения.
* `f'{18.13 / 2.14 :.2f}'` - округление вещественного числа до сотых.
* `f'{45.76 * 22.12 :,}'` - вставка запятых в качестве разделителя.
* `f'{0.5 :%}'` - форматирование вещественного числа в проценты.
* `f'{some :10}'` - указание минимальной ширины поля.
* `f'{some :<^>10}'` - выравнивание значений в поле.

> Важно знать, правильная последовательность f-строк: `[выравнивание][ширина][,][точность][тип]`.

#### <a name='8.3'></a> Индексация строк [🠕](#8)

Все символы в строке имеют свой порядковый номер(индекс). Первый символ имеет индекс 0, второй символ - индекс 1, третий - индекс 2 и т.д.

Обращение по индексу в строке:

```python
x = 'Hello world!'
print(x[0])                      # Вывод будет: H
```

Обратная индексация в строке:

```python
x = 'Hello wold!'
print(x[-1])                     # Вывод будет: !
```

Взятие среза строки:

```pyth5n
# имя_строки[начало:конец:шаг]

new_text = 'Hello world!'        # Строка
print(new_text[1:5])             # Вывод будет: ello
print(new_text[4:])              # Вывод будет: o world!
print(new_text[:7])              # Вывод будет: Hello w
print(new_text[1::2])            # Вывод будет: el ol!
print(new_text[:])               # Вывод будет: Hello world!
```

#### <a name='8.4'></a> Манипуляции со строками [🠕](#8)

Добавление строки к строке:

```python
x = 'Hello'
x += 'World'
print(x)                         # Вывод будет: HelloWorld
```

Объединение нескольких строк:

```python
x = 'Hello'
y = 'worl!'
print(x + ' ' + y)                         # Вывод будет: Hello world!
```

Повторение строки:

```python
x = 'Hello world!'
x *= 2
print(x)                         # Вывод будет: Hello world!Hello world!
```

#### <a name='8.5'></a> Методы объекта строки [🠕](#8)

Методы проверки `True`/`False`:

* `str.isalnum()` - возвращает `True` если строка содержит только буквы и/или цифры.
* `str.isalpha()` - возвращает `True` если строка содержит только буквы.
* `str.isdigit()` - возвращает `True` если строка содержит только цифры.
* `str.islower()` - возвращает `True` если строка содержит символы только нижнего регистра.
* `str.isupper()` - возвращает `True` если строка содержит символы только верхнего регистра.
* `str.isspace()` - возвращает `True` если строка содержит только пробельные символы.
* `str.istitle()` - возвращает `True` если каждое из слов строки начинается с заглавной буквы.

Методы работы с регистром:

* `str.lower()` - возвращает копию строки с символами приведёнными к нижнему регистру.
* `str.upper()` - возвращает копию строки с символами приведёнными к верхнему регистру.
* `str.title()` - возвращает копию строки, в которой каждое новое слово начинается с заглавной буквы и продолжается строчными.
* `str.capitalize()` - возвращает копию строки, переводя первую букву в верхний регистр, а остальные в нижний.
* `str.swapcase()` - возвращает копию строки, в которой каждая буква будет иметь противоположный регистр.

Методы удаления пробелов:

* `str.lstrip()` - возвращает копию строки, с начала которой устранены пробельные символы.
* `str.rstrip()` - возвращает копию строки, с конца которой устранены пробельные символы.
* `str.strip()` - возвращает копию строки, с обоих концов которой устранены пробельные символы.

> Важно знать, в скобках методов можно явно указать набор удаляемых символов.

Методы разбиения и объединения:

* `str.split(разделитель)` - разбивает строку на части считывая строку слева направо, используя разделитель, и возвращает эти части списком.
* `str.rsplit(разделитель)` - разбивает строку на части считывая строку справа налево, используя разделитель, и возвращает эти части списком.
* `'разделитель'.join([список])` - возвращает строку, собранную из элементов указанного объекта, поддерживающего итерирование.

Методы работы с подстроками:

* `str.startswith(пoдcтpoкa)` - возвращает `True`, если строка начинается с подстроки.
* `str.endswith(пoдcтpoкa)` - возвращает `True`, если строка заканчивается на подстроку.
* `str.find(подстрока, начало, конец)` - возвращает индекс подстроки в строке, поиск проиходит слева направо, если подстрока не найдена, возвращается число -1.
* `str.rfind(подстрока, начало, конец)` - возвращает индекс подстроки в строке, поиск проиходит справа налево, если подстрока не найдена, возвращается число -1.
* `str.replace(старое, новое, счетчик_замены)` - возвращает копию строки, в которой заменяет одну подстроку на другую.
* `str.count(подстрока, начало, конец)` - возвращает количество вхождений подстроки в заданной строке.
* `str.index(подстрока, начало, конец)` - возвращает наименьший индекс, по которому обнаруживается начало указанной подстроки в исходной.
* `str.rindex(подстрока, начало, конец)` - возвращает наибольший индекс, по которому обнаруживается конец указанной подстроки в исходной.

***

### Списки и кортежи

***

#### <a name='9.1'></a> Индексация списков/кортежей [🠕](#9)

Все символы в списке/кортеже имеют свой порядковый номер(индекс). Первый символ имеет индекс 0, второй символ - индекс 1, третий - индекс 2 и т.д.

Обращение по индексу в списке/кортеже:

```python
x_list = [10, 20, 30]
print(x_list[0])                 # Вывод будет: 10
```

Обратная индексация в списке/кортеже:

```python
x_list = [1, 65, 'Hello']
print(x_list[-1])                # Вывод будет: Hello
```

Присваивание по индексу в списке:

```python
x_list = ['Hi', 0, 65]
x_list[0] = 100
print(x_list)                    # Вывод будет: [100, 0, 65]
```

> Важно знать, присваивание по индексу в кортежах и строках не работает.

Двумерный список/кортеж:

```python
name_list = [[1, 2], [3, 4]]
print(name_list[0])              # Вывод будет: [1, 2]
print(name_list[1][1])           # Вывод будет: 4
```

Взятие среза списка/кортежа:

```python
# имя_списка[начало:конец:шаг]

new_list = [0, 'Hi', 78.56, 22]  # Список
print(new_list[1:3])             # Вывод будет: ['Hi', 78.56]
print(new_list[2:])              # Вывод будет: [78.56, 22]
print(new_list[:3])              # Вывод будет: [0, 'Hi', 78.56]
print(new_list[1::2])            # Вывод будет: ['Hi', 22]
print(new_list[:])               # Вывод будет: [0, 'Hi', 78.56, 22]
```

#### <a name='9.2'></a> Манипуляции со списками/кортежами [🠕](#9)

Добавление списка к списку или кортежа к кортежу:

```python
x_list = [1, 2, 3]
x_list += [4, 5, 6]
print(x_list)                    # Вывод будет: [1, 2, 3, 4, 5, 6]
```

Добавление строки к списку:

```python
x_list = []
x_list += 'text'
print(x_list)                    # Вывод будет: ['t', 'e', 'x', 't']
```

> Важно знать, добавление строки в кортеж не сработает, возникнет исключение.

Добавление объекта к списку/кортежу:

```python
x_list = []
x_list += ('text',)
print(x_list)                    # Вывод будет: ['text']
```

Добавление нескольких объектов к списку/кортежу:

```python
x_list = []
x_list += (1, 'text')
print(x_list)                    # Вывод будет: [1, 'text']
```

Повторение списка/кортежа:

```python
x_list = [0, 1, 2]
x_list *= 2
print(x_list)                    # Вывод будет: [0, 1, 2, 0, 1, 2]
```

#### <a name='9.3'></a> Методы объекта списка [🠕](#9)

Методы добавления элементов:

* `list.append(объект)` - добавляет объект в конец списка.
* `list.extend([список])` - дополняет список элементами из источника.
* `list.insert(индекс, объект)` - вставляет указанный объект перед указанным индексом.

Методы удаления элементов:

* `list.pop(индекс)` - возвращает элемент (на указанной позиции) удаляя его из списка, если не указывать индекс то удалится последний элемент.
* `list.remove(имя_элемента)` - удаляет первый обнаруженный элемент в списке.
* `list.clear()` - удаляет все элементы из списка.

Остальное:

* `list.copy()` - возвращает копию списка.
* `list.count(имя_элемента)` - считает и возвращает количество одинаковых элементов в списке или кортеже.
* `list.index(имя_элемента)` - возвращает положение элемента первого индекса в списке или кортеже.
* `list.sort()` - сортирует элементы списка на месте.
* `list.reverse()`- перестраивает элементы списка в обратном порядке.

***

### Словари

***

### <a name='10.1'></a> Манипуляции с элементами в словаре [🠕](#10)

Получение значения:

```python
имя_словаря[ключ]
```

Добавление элементов:

```python
имя_словаря[ключ] = значение
```

> Важно знать, в словаре нельзя иметь повторяющиеся ключи, если присвоить значение существующему ключу, новое значение заменит существующее.

Удаление элементов:

```python
del имя_словаря[ключ]
```

Перебор элементов в цикле:

```python
x_dict = {'key1': 12466, 'key2': 86543}

for key in x_dict:
    print(key, x_dict[key])
```

### <a name='10.2'></a> Методы объекта словаря [🠕](#10)

Методы обращения к элементам:

* `dict.items()` - возвращает все ключи в словаре и связанные с ними значения в виде последовательности кортежей.
* `dict.keys()` - возвращает все ключи в словаре в виде последовательности кортежей.
* `dict.values()` - возвращает все значения из словаря в виде последовательности кортежей.
* `dict.get(ключ, значение_по_умолчанию)` - получает значение, связанное с заданным ключом, если ключ не найден, этот метод не вызывает исключение, вместо этого он возвращает значение по умолчанию.

Методы удаления элементов:

* `dict.рор(ключ, значение_по_умолчанию)` - возвращает из словаря значение, связанное с заданным ключом и удаляет эту пару `ключ: значение`, если ключ не найден, этот метод возвращает значение по умолчанию.
* `dict.popitem()` - возвращает в виде кортежа последнюю добавленную в словарь пару, этот метод также удаляет `ключ: значение` из словаря.
* `dict.clear()` - очищает содержимое словаря.

Остальное:

* `dict.copy()` - возвращает копию словаря.
* `dict.update({словарь})` - обновляет словарь элементами из другого объекта словаря или из итерации пар `ключ: значение`.

***

### Множества

***

### <a name='11.1'></a> Методы объекта множества [🠕](#11)

Методы добавление элементов:

* `set.add(имя_элемента)` - добавляет в множество указанный элемент.
* `set.update({множество})` - добавляет в множество элементы указанного множества.

Методы удаление элементов:

* `set.pop()` - удаляет и возвращает произвольный элемент множества, если множество является пустым, то вызывается исключение.
* `set.remove(имя_элемента)` - удаляет указанный элемент из множества или вызывает исключение если такой элемент отсутсвует.
* `set.discard(имя_элемента)` - удаляет указанный элемент, если он присутствует в множестве.
* `set.clear()` - очищает множество.

Методы специфики:

* `set.union({множество})` - возвращает объединение множеств.

> Важно знать, вместо метода можно использовать оператор `|`: `set_1 | set_2 | set_3`.

* `set.intersection({множество})` - возвращает множество с элементам присутствующими в обоих множествах.

> Важно знать, вместо метода можно использовать оператор `&`: `set_1 & set_2`.

* `set.difference({множество})` - возвращает элементы множества которые отсутствуют в указанном множестве.

> Важно знать, вместо метода можно использовать оператор `-`: `set_1 - set_2`.

* `set.syrnmetric_difference({множество})` - возвращает элементы которые присутствуют в обоих множествах, кроме тех, которые являются общими.

> Важно знать, вместо метода можно использовать оператор `^`: `set_1 ^ set_2`.

* `set.issubset()` - возвращает `True` если множество эквивалентно указанному множеству или является его подмножеством.

> Важно знать, вместо метода можно использовать операторы `<=` и `>=`: `set_1 <= set_2`, `set_1 >= set_2`.

Остальное:

* `set.copy()` - возвращает поверхностную копию множества.

* `set.isdisjoint({множество})` - возвращает `True` если у множества нет общих элементов с указанным множеством.

***

### Файлы

***

#### <a name='12.1'></a> open() [🠕](#12)

`open()` - открывает файл для чтения или записи при помощи файлового потока:

```python
file = open('путь к файлу', 'аргумент')
```

Аргументы функции:

* `r` - открывает файл на чтение.
* `w` - открывает файл на запись, содержимое файла удаляется, если файл не существует то создается новый.
* `a` - открывает файл на дозапись, информация добавляется в конец файла, если файл не существует то создается новый.

Чтение файла и вывод содержимого на экран:

```python
log_file = open('/var/log/fail2ban.log', 'r')

for line in log_file:
    print(line, end='')
```

> Важно знать, при чтение файла, данные являются строкой `str`.

Запись в файл:

```python
hello_file = open('Hello.txt', 'w')

print('Привет мир!', file=hello_file)
```

> Важно знать, перед записью в файл, данные должны быть строкой `str`.

Автоматическое закрытие файла оператором `with/as`:

```python
with open('test.txt', 'a') as input_file:
    print('Добавляем эту строку в конец файла', file=input_file)
```

> Важно знать, после открытия файла и взаимодействия с ним, файл нужно обязательно закрыть, иначе при чтение многих файлов будет утечка памяти, а при записи будет потеря данных.

#### <a name='12.2'></a> Методы объекта файла [🠕](#12)

Методы чтения файла:

* `file.read()` - считывает и возвращает весь файл.
* `file.readline()` - считывает и возвращает по одной строке из файла.
* `file.readlines()` - считывает строки файла и возвращает список из строк.

Методы записи файла:

* `file.write('строка')` - записывает в файл.
* `file.writelines([список])` - записывает элементы списка в файл.

Остальное:

* `file.close()` - закрывает файл.
